
# SAC '21：第 36 届 ACM/SIGAPP 应用计算研讨会（韩国虚拟会议）论文集｜SecureJS 编译器：JavaScript 中的可移植内存隔离

## 摘要

内存隔离机制在为 JavaScript 程序提供安全实施方面发挥着至关重要的作用。现有的安全交互库，如 Google Caja、SES 和 VM2，依赖于 Node.js 和浏览器提供的内置内存隔离机制，然而大多数其他引擎，例如为物联网设备实现的 JerryScript 和 Duktape，则不支持此类隔离机制。

在本文中，我们报告了 SecureJS 的设计和实现，这是一个可移植的 JavaScript 到 JavaScript 编译器，用于强制执行内存隔离。由于它仅使用标准特性，其生成的编译代码可被任何 JavaScript 引擎使用。我们通过使用 ECMAScript Test262 测试套件中的 10,490 个测试程序，经验性地验证了 SecureJS 编译程序的语义保持和内存隔离性。我们还开发了一种新颖的实验，通过插桩 JavaScript 引擎来评估编译代码的内存隔离特性。

## CCS 概念

- 安全与隐私 → 软件安全工程；Web 应用程序安全；
- 软件及其工程 → 语法；语义；

## 关键词

编译器，内存隔离，JavaScript

## ACM 参考格式

Yoonseok Ko, Tamara Rezk, and Manuel Serrano. 2021. SecureJS Compiler: Portable Memory Isolation in JavaScript. In *The 36th ACM/SIGAPP Symposium on Applied Computing (SAC '21)*, March 22–26, 2021, *Virtual Event, Republic of Korea*. ACM, New York, NY, USA, Article 4, 10 pages. https://doi.org/10.1145/3412841.3442001

## 1 引言

多年来，JavaScript 因其易于操作和部署而迅速发展。该语言的动态特性为代码集成提供了流畅的环境，并有助于复杂应用程序的轻松快速开发 [10]。

尽管 JavaScript 的动态特性通过简化应用程序开发在语言普及中发挥了重要作用，但它们也使得恶意 JavaScript 库能够利用这些动态特性来破坏应用程序的完整性和机密性 [3]。在单个 JavaScript 程序执行中，所有组件共享一个全局对象和内置对象，如 `Object` 和 `Object.prototype`。由于 JavaScript 特有的语义，其基本操作会隐式访问这些全局和内置对象，因此构成应用程序的所有组件都紧密地绑定在一起。这为恶意第三方代码提供了机会，使其能够歪曲或从其他执行中提取不当信息。

迄今为止，已经进行了各种研究以通过内存隔离提供安全实施 [2, 8, 9, 11, 13–16]。完全隔离是运行程序而无意外交互的最简单方式。然而，需要程序间交互的更复杂程序无法享受隔离的好处。实际的 JavaScript 安全编程解决方案，如 Google Caja [9]、SES [1] 和 VM2 [13]，依赖于 Node.js 或浏览器提供的此类隔离机制，并通过控制交互来提供隔离程序之间的安全交互。尽管如此，其他流行的 JavaScript 实现，如 JerryScript¹ 和 Duktape²（它们是用于微控制器的 JavaScript 实现），并不支持此类内置隔离机制，因此限制了这些安全交互解决方案在实际使用中的应用。这促使了需要独立于 JavaScript 实现的可移植隔离 JavaScript 环境。

JavaScript 内存隔离的基本构建块是*领域*（如最新 ECMAScript 规范³ 所定义），它由一个全局对象和内置对象组成。在同一领域中运行的程序共享全局和内置对象，而隔离的领域最初不共享任何领域间的引用。在不同隔离领域中运行程序可保证它们的内存访问不会相互干扰。然而，一个领域中的程序能够通过有意导出一个值与另一个领域中的程序交互，这破坏了隔离。因此，隔离领域是安全程序执行的基本和必要单元，它们可以通过与现有的 JavaScript 安全编程解决方案结合来实现进一步交互的安全实施。不幸的是，JavaScript 领域仅由某些 JavaScript 实现（如 Node.js 和浏览器）支持，这限制了现有安全编程解决方案在其他 JavaScript 实现中的使用。

¹ https://jerryscript.net

² https://duktape.org

³ https://www.ecma-international.org/ecma-262/#sec-code-realms

### 我们的方法

在本文中，我们提出了一种基于 JavaScript 到 JavaScript 编译的新技术，用于在隔离领域中运行 JavaScript 程序。我们的方法专注于重写给定程序的隐式字段访问语义，并通过使用修改后的字段访问操作来实现内存隔离。为此，我们定义了 JavaScript 语言的一个子集 `JS<sup>explicit</sup>`，其中基本操作不涉及隐式字段访问。从 JavaScript 到 `JS<sup>explicit</sup>` 的翻译将源程序的所有隐式字段访问替换为显式操作。`JS<sup>explicit</sup>` 程序旨在在专用的安全运行时环境中运行，该环境创建一个隔离的虚拟领域，并提供隐式访问该隔离虚拟领域的安全基本操作。

我们已经实现了一个安全的 JavaScript 到 JavaScript 编译器 SecureJS。它将程序转换为等效的程序，但这些程序将像在隔离内存中运行一样执行。编译依赖于翻译到 `JS<sup>explicit</sup>`，并将基本操作替换为安全版本，从而在模拟 JavaScript 领域的隔离内存中执行。在隔离内存中运行的程序可以通过有意将隔离内存中的值导出到外部来与其他程序交互。该编译器是可移植的，仅使用标准特性，因此可被任何符合 ECMAScript 5.1 规范的 JavaScript 引擎使用。因此，该编译器提供了独立于 JavaScript 实现的隔离机制，使我们能够在任何 JavaScript 引擎中使用现有的安全交互库。

### 贡献

- 我们提出了 JavaScript 语言的一个子集 `JS<sup>explicit</sup>`，其中基本操作不涉及隐式字段访问，并提出了从 JavaScript 到 `JS<sup>explicit</sup>` 的翻译（第 3 节）。
- 我们提供了一个安全的 JavaScript 到 JavaScript 编译器 SecureJS 作为工具。该编译器将程序转换为等效的程序，但这些程序将像在隔离领域中运行一样执行，而不依赖于任何内置机制。此实现可移植到任何符合 ECMAScript 5.1 的实现，并且隔离领域支持 ECMAScript 5.1⁴ 的所有特性（第 4 节）。
- 我们提供了插桩 JavaScript 引擎，用于检测隐式字段访问和对内置对象的字段访问。我们使用它来经验性地测试 SecureJS 编译程序的语义保持和内存隔离性。插桩引擎可独立于 SecureJS 用于测试内存隔离。我们的工具和插桩引擎的补丁是公开可用的⁵（第 5 节）。

## 2 概述

我们通过一个极其简单的示例概述我们的方法，该示例仅使用涉及动态类型转换和原型链字段查找的字段访问操作。

我们演示了一个 JavaScript 程序构造的评估。单个 JavaScript 程序构造的评估由一系列 JavaScript *内部基本操作* 组成。我们考虑以下代码片段：

```javascript
1 Boolean.prototype.x = 10;
2 var o = {toString: function() { return "x"; }};
3
4 true[o] === 10;
```

第 4 行测试中使用的字段查找操作 `true[o]` 的评估由一系列 JavaScript 基本操作组成，如下所示：

- (1) 它对 `true` 应用 `ToObject` 以动态将值转换为对象。`ToObject` 的语义通过调用 `new Boolean(true)` 创建 Boolean 内置对象的实例，并且创建对象的内部字段 `[[Prototype]]`⁶ 被设置为 `Boolean.prototype` 的引用。
- (2) 它对字段名指示符 `o` 应用内部操作 `ToString` 以动态将值转换为字符串。`ToString` 的语义*隐式访问*对象 `o` 的字段 `toString` 并调用它。正如我们在第 2 行定义的，该函数返回字符串 `"x"`。
- (3) 字段查找操作从 Boolean 内置对象的实例中搜索名为 `"x"` 的字段。由于该实例没有名为 `"x"` 的字段，它*隐式访问*对象 `Boolean.prototype` 的字段 `"x"`，该对象是实例的原型链对象。由于对象 `Boolean.prototype` 的字段值如我们在第 1 行定义的为 10，因此字段查找操作的结果被评估为 10，相等性测试成功。

JavaScript 中字段查找操作的评估涉及两个隐式字段访问，其中一个字段访问读取了内置对象 `Boolean.prototype` 的字段值。

我们的目标是*像在隔离领域中运行一样*运行程序。为此，我们将实际在依赖于两个要素的隔离*虚拟领域*中运行它们：*i)* 新创建的受控全局和内置对象，以及 *ii)* 将隐式字段访问从原始内置对象重新路由到受控内置对象。

为了重新路由字段访问，我们使用两步代码转换。首先，我们将程序转换为等效的程序，但其中的隐式操作已被等效的显式操作替换。例如，在上面的示例中，隐式字段访问涉及动态类型转换。例如，代码 `true[o] === 10` 被转换如下：

```javascript
1 // ToObject(true)
2 var r = new Boolean(true);
3 // ToString(o)
4 var s = o.toString();
5 // 实际字段查找
6 function Load(o,s) {
7   if (o.hasOwnProperty(s)) return o[s];
8   o = Object.getPrototypeOf(o);
9   return Load(o,s);
10 }
11 Load(r,s) === 10;
```

其次，我们重写代码 `Load` 以重新路由字段访问，如下所示：

> ⁶在 ECMAScript 规范中，内部字段和方法名称用双方括号 `[[Name]]` 表示。这些方法和字段名称不允许从 JavaScript 程序直接调用或访问，但可以从其他内部方法或操作调用或访问。

⁴我们有意不提供 `eval` 和 `with` 构造。

⁵ https://gitlab.inria.fr/securejs/sjs-compiler

```javascript
function SJSLoad(o,s) {
  if (o.hasOwnProperty(s)) return o[s];

  o = Object.getPrototypeOf(o);

  if (o === Boolean.prototype)
    o = isolated.Boolean.prototype;

  return SJSLoad(o,s);
}

SJSLoad(r,s) === 10;
```

这段代码使用 `SJSLoad` 代替 `Load` 进行字段查找操作。关键点在第 4 行。当字段访问到达内置对象 `Boolean.prototype` 时，它会将字段访问重定向到受控的内置对象 `isolated.Boolean.prototype`（第 5 行）。因此，重写后的代码运行时，就好像代码是在受控的内置对象下运行一样。

在本文的其余部分，我们提出了一种核心 JavaScript 语言 `JSexplicit`，它不涉及隐式字段访问，并且我们展示了从 JavaScript 到 `JSexplicit` 的转换（第 3 节）。然后，我们实现了一个安全的运行时环境，该环境由一个隔离的虚拟领域和安全的原始操作组成，这些操作将字段访问重定向到虚拟领域（第 4 节）。

## 3 `JSexplicit`，一种核心 JavaScript 语言

在本节中，我们定义 `JSexplicit`，一种 JavaScript 的核心语言，其语义比 JavaScript 更简单，因为它的原始操作不涉及隐式字段访问。

### 3.1 语法

我们为 `JSexplicit` 使用以下形式语法：

```text
e ::= x | x_g | v ∈ V_prim | this | e ⊕ e | ⊖ e
    | ◇toString e | ◇toNumber e | ◇toBoolean e
    | ◇hasOwnProperty e_1 e_2 | ◇getPrototypeOf e
i ::= var x | x = e | x_g = e | x_1 = ◇alloc(x_2)
    | e_1[e_2] = e_3 | x = e_1[e_2]
    | x = λ(x_n).i | return e
    | x = ◇apply(x_1, x_2, [y_n])
    | while x do i | if (x) i_1 else i_2
    | try i_1 catch(x) i_2 finally i_3
    | throw e | {i} | i_1 ; i_2 | ε
    | ◇defineOwnProperty(x, e_1, e_2)
    | x = ◇getOwnPropertyDescriptor(e_1, e_2)
```

其中 ⊕ 和 ⊖ 分别是 JavaScript 语言的二元和一元运算符。

### 表达式

表达式 `e` 可以是局部变量访问 `x`、全局变量访问 `x_g`、常量值 `v ∈ V_prim`、`this` 值、二元运算符或一元运算符。

### 非标准表达式

名称以 ◇ 符号开头的运算符是非标准运算符。它们的语义遵循相应的 JavaScript 内置函数，但不涉及隐式类型转换。字段测试运算符 `◇hasOwnProperty e_1 e_2` 在 `e_1` 指定的对象具有名为 `e_2` 的字段时返回 `true`，否则返回 `false`。此运算符要求 `e_1` 为对象值，`e_2` 为字符串值。运算符 `◇getPrototypeOf e` 返回给定对象 `e` 的原型链对象。此运算符要求 `e` 为对象值。原始类型转换运算符 `◇toString e`、`◇toNumber e` 和 `◇toBoolean e` 分别接受一个原始值 `e` 作为参数，并分别返回字符串、数字和布尔值。

### 指令

`JSexplicit` 对字段查找和更新操作使用非标准语义。字段更新操作 `e_1[e_2] = e_3` 将对象 `e_1` 中由 `e_2` 的值指定的字段更新为 `e_3` 的值。请注意，更新操作不访问给定对象的原型链，也不涉及动态类型转换。因此，`e_1` 必须求值为对象，`e_2` 必须求值为字符串值。字段查找操作 `x = e_1[e_2]` 读取对象 `e_1` 中由 `e_2` 指定的字段，并将结果赋值给局部变量 `x`。与字段更新操作类似，字段查找操作不访问原型链对象，也不涉及动态类型转换。因此，`e_1` 必须求值为对象，`e_2` 必须求值为字符串值。

其余指令的语义遵循标准语义，但这些指令不涉及动态类型转换。变量声明 `var x` 在局部作用域中声明一个变量。赋值指令 `x = e` 和 `x_g = e` 分别将表达式 `e` 的值赋值给局部变量 `x` 和全局变量 `x_g`。当指令将值赋给全局变量时，如果其可写属性为 `true`，则更新为新值；否则，忽略更新操作。对象分配 `x_1 = ◇alloc(x_2)` 分配一个原型链指向 `x_2` 的新对象，并将新分配的位置赋值给 `x_1`。函数声明 `x = λ(x_n).i` 分配一个具有参数名 `x_n` 和函数体指令 `i` 的新函数对象。我们假设函数体 `i` 中的所有程序流都以 `return` 指令 `return e` 结束。`return` 指令 `return e` 将表达式 `e` 的值返回给调用者。函数调用 `x = ◇apply(x_1, x_2, [y_n])` 使用 `this` 值 `x_2` 和参数 `y_n` 调用函数 `x_1`，并将函数的返回值赋值给变量 `x`。循环 `while x do i` 在条件 `x` 的值为 `true` 时迭代其主体 `i`。分支指令 `if (x) i_1 else i_2` 根据变量 `x` 的值执行指令 `i_1` 或 `i_2`。指令 `try i_1 catch(x) i_2 finally i_3` 执行指令 `i_1`，如果指令 `i_1` 抛出异常，则捕获异常值，将其绑定到局部变量 `x`，并运行指令 `i_2`。然后，执行指令 `i_3`。`throw` 指令 `throw e` 抛出一个异常值为 `e` 的异常。一旦抛出异常，它会忽略指令，直到到达 `catch` 子句。序列 `i_1 ; i_2` 按顺序执行指令 `i_1` 和 `i_2`。空操作指令 `ε` 不执行任何操作。

### 非标准指令

`JSexplicit` 使用非标准指令：`◇defineOwnProperty` 和 `◇getOwnPropertyDescriptor`。在 JavaScript 中，它们由内置函数 `Object.defineProperty` 和 `Object.getOwnPropertyDescriptor` 支持。带属性的即时字段更新操作 `◇defineOwnProperty(x, e_1, e_2)` 将表达式 `e_2` 的值赋值给对象 `x` 的字段 `e_1`。表达式 `e_2` 的值要么是具有 `value`、`enumerable`、`configurable` 和 `writable` 属性字段的数据描述符对象，要么是具有 `get`、`set`、`enumerable` 和 `configurable` 字段的访问器描述符对象。即时字段查找 `x = ◇getOwnPropertyDescriptor(e_1, e_2)` 读取对象 `e_1` 的字段 `e_2`，并将字段值记录作为对象赋值给变量 `x`。

为简单起见，我们在本节的其余部分使用以下符号：`x = f(y_1, ..., y_n)` 表示 `x = ◇apply(f, null, [y_n])`，我们使用如下定义的函数 `isObject`：

```javascript
isObject = λ[x]. {
  return (typeof x === "object" && x !== null) ||
  typeof x === "function";
}
```



当`if`语句的`else`分支为空时，我们将其省略。

### 3.2 语义

我们通过大步语义来定义程序的语义。`JS<sup>explicit</sup>`的语义遵循`JavaScript`语言的语义，但不涉及动态类型转换和隐式字段访问。配置的形式为`$\mu, l_s, i, t \Downarrow \mu', t'$`，其中`$\mu, \mu' \in \mathbb{M}$`是内存，`$l_s \in \mathbb{V}_{loc}$`是当前作用域对象位置，`$i$`是指令，`$t$`是正常状态或异常状态，其值为`$exc(v)$`，其中`$v \in \mathbb{V}$`。状态标签`normal`表示程序状态处于正常状态，状态标签`$exc(v)$`表示程序状态处于异常状态，异常值为`$v$`。内存`$\mathbb{M} = \mathbb{V}_{loc} \rightarrow \mathbb{O}$`是从位置到对象的映射，对象`$o \in \mathbb{O} = \mathbb{V}_{fld} \rightarrow \mathbb{R}$`是从字段名到字段值的映射，其中`$\mathbb{V}_{fld} = \mathbb{V}_{str} \cup \mathbb{V}_i$`，`$\mathbb{V}_{str}$`是字符串，`$\mathbb{V}_i$`是用于命名内部`JavaScript`字段（如`@env`和`@proto`）的特殊值，`$\mathbb{R} = \mathbb{V}_{str} \rightarrow \mathbb{V}$`是从记录名到值的映射，我们用`$\{name_1 : v_1, name_2 : v_2\}$`表示一个具有两个元素`$name_1$`和`$name_2$`及其值`$v_1$`和`$v_2$`的记录。

表达式`$e$`的求值形式为`$\mu, l_s, e \Downarrow_E v$`，其中`$\mu \in \mathbb{M}$`是程序内存，`$v$`是表达式在内存中的值。

辅助函数`$Put(l_s, x, v)$`要么用`$x = v$`更新当前作用域对象，要么沿着由外部作用域`@env`指定的作用域链更新局部变量`$x$`的值，定义如下：

```
$$\frac{\mu' = \mu[l_s \mapsto \mu(l_s)[x \mapsto v]]}{\mu, Put(l_s, x, v) \Downarrow_A \mu'} \quad x \in dom(\mu(l_s))$$
```

```
$$\frac{\mu, Put(\mu(l_s)(@env).1, x, v) \Downarrow_A \mu'}{\mu, Put(l_s, x, v) \Downarrow_A \mu'} \quad x \notin dom(\mu(l_s))$$
```

图 1 展示了仅包含基本规则的形式语义摘录。它展示了对象分配、字段查找和更新操作的语义。与标准`JavaScript`语义不同，字段查找和更新操作仅接受接收者是一个对象，并且字段名指示符求值为字符串值，并且这些操作不在给定接收者对象的原型链中搜索字段。

- **分配规则。** 指令`$x_1 = \diamond alloc(x_2)$`将参数`$x_2$`求值为值`$v$`，在新位置`$l_n$`分配一个原型链值为`$v$`的新对象，并将分配的对象引用赋值给局部变量`$x_1$`。此指令要求原型值`$x_2$`为位置值或`null`值。

- **查找规则。** 指令`$x_1 = x_2[e]$`首先将接收者对象`$x_2$`和字段名指示符`$e$`分别求值为位置`$l$`和字符串值`$k$`。语义不搜索原型链，而只是读取接收者对象`$\mu(l)(k)$`的字段。在此规则中，字段必须是一个记录，该记录具有四个字段`$value$`、`$enumerable$`、`$configurable$`和`$writable$`，并通过调用辅助函数`Put`将字段`$value$`的值赋值给左侧变量`$x_1$`。

- **更新规则。** 指令`$x[e_1] = e_2$`也将接收者对象`$x$`求值为位置`$l$`，字段名`$e_1$`求值为字符串值`$k$`。它将表达式`$e_2$`求值为值`$v$`，并将值`$v$`作为具有`enumerable`、`configurable`和`writable`字段的记录赋值给由位置`$l$`指定的接收者对象的字段`$k$`。当接收者对象中没有名为`$k$`的字段时，应用此规则，并创建一个新字段。

非标准指令和运算符的语义遵循相应的`JavaScript`内置函数的语义，但不应用动态类型转换。图 2 展示了三个额外的语义规则：

- **hasOwnProperty1 和 hasOwnProperty2 规则。** 二元运算`$\diamond hasOwnProperty$`测试对象`$e_1$`是否具有由字符串名`$e_2$`指定的字段。

- **getPrototypeOf 规则。** 一元运算`$\diamond getPrototypeOf$` `$e$`返回给定对象的内部原型链值。

一元运算`$\diamond toString$`、`$\diamond toNumber$`和`$\diamond toBoolean$`接受一个原始值作为参数，并返回其对应的类型值。转换算法在`ECMAScript`规范`<sup>7</sup>`[4] 中定义，这些转换算法不涉及隐式字段访问。

### 3.3 JS<sup>explicit</sup> 中的 JavaScript 原始操作

在本节中，我们展示用`JS<sup>explicit</sup>`编写的`JavaScript`原始操作。每个原始操作都由`ECMAScript`规范中定义的相应内部方法或操作设计。我们用`[[A]]`和`B`分别表示名为`A`的内部字段或方法和名为`B`的操作。

图 3a 展示了`ECMAScript`规范的`[[Get]]`内部方法，它定义了`JavaScript`中字段查找操作的基本语义。对于给定的代码`o[s]`，`o`作为`$base$`传递，`s`作为`$P$`传递给规范。图 3b 展示了`Get`函数的代码，该函数在`JS<sup>explicit</sup>`中模拟`[[Get]]`内部方法的语义。辅助函数`Get`的每一步都是根据规范设计的，并用`JS<sup>explicit</sup>`编写。

首先，规范的`[[Get]]`内部方法通过调用`ToObject`操作将接收者值`$base$`转换为对象（步骤 1）。在`Get`函数中，它调用函数`ToObject`，该函数模拟规范中`ToObject`操作的语义。如果输入值的类型已经是对象，则此操作返回输入值。否则，如果输入值的类型是字符串、数字或布尔类型之一，则分配一个类型化的对象。此语义由用`JS<sup>explicit</sup>`编写的辅助函数`ToString`定义。然后，它调用`[[GetProperty]]`内部方法，从对象`$base$`及其原型链中搜索名为`$P$`的字段（步骤 2）。结果要么是未找到字段时的`undefined`值，要么是描述符对象。如果结果是`undefined`，则返回`undefined`值（步骤 3）。如果字段是普通值字段，则描述符对象具有`value`字段。否则，描述符对象必须具有`get`字段，它是`getter`值。因此，它首先检查描述符对象是否具有字段`"value"`，当描述符对象具有该字段时，返回字段`"value"`的值（步骤 4）。

`<sup>7</sup>ToBoolean`: https://www.ecma-international.org/ecma-262/5.1/#sec-9.2,

`ToNumber`: https://www.ecma-international.org/ecma-262/5.1/#sec-9.3,

`ToString`: https://www.ecma-international.org/ecma-262/5.1/#sec-9.8

1268

### 3.4 转换为 JS<sup>explicit</sup>

当使用`base`作为`this`值并以属性名`P`调用`[[Get]]`内部方法时，将执行以下步骤：

(1) 令`O`为`ToObject(base)`。

(2) 令`desc`为以属性名`P`调用`O`的`[[GetProperty]]`内部方法的结果。

(3) 如果`desc`是`undefined`，则返回`undefined`。

(4) 如果`IsDataDescriptor(desc)`为`true`，则返回`desc.[[Value]]`。

(5) 否则，`IsAccessorDescriptor(desc)`必须为`true`，因此令`getter`为`desc.[[Get]]`（参见 8.10）。

(6) 如果`getter`是`undefined`，则返回`undefined`。

(7) 返回以`base`作为`this`值且不提供参数调用`getter`的`[[Call]]`内部方法的结果。

```
1 Get = λ(0,P). {
2   var result, getter;
3   0 = ToObject(0); /* (1) */
4   var desc = GetProperty(0,P); /* (2) */
5   if (desc === undefined) return undefined; /* (3) */
6   if (¬hasOwnProperty desc "value") { /* (4) */
7     result = desc["value"];
8     return result
9   } else {
10    getter = desc["get"]; /* (5) */
11    if (getter === undefined) return undefined; /* (6) */
12    result = ◇apply(getter, 0, []); /* (7) */
13    return result
14  }
15 }
```

(a) `[[Get]]`内部方法

(b) 用`JSexplicit`编写的函数`Get`

图 3：`[[Get]]`内部方法的规范及其用`JSexplicit`表示的含义

否则，它会加载字段`"get"`（步骤 5）。如果`getter`函数是`undefined`，它只返回`undefined`值（步骤 6）。否则，`getter`函数是一个函数值，它以`base`作为`this`值调用该`getter`函数并返回结果（步骤 7）。

图 4a 和 4b 展示了`[[GetProperty]]`内部方法的规范及其用`JSexplicit`表示的含义。`[[GetProperty]]`方法定义了在原型链中进行字段搜索。它首先尝试从给定对象`O`访问字段`P`（步骤 1）。如果对象`O`有一个名为`P`的字段，它直接返回该字段记录（步骤 2）。否则，它加载对象`O`的原型链对象的值（步骤 3）。如果给定对象没有原型链对象，则查找字段失败并返回`undefined`值（步骤 4）。否则，它从对象`O`的原型链对象递归搜索名为`P`的字段（步骤 5）。辅助函数`GetProperty`在`JSexplicit`中实现了该语义。

当以属性名`P`调用`O`的`[[GetProperty]]`内部方法时，将执行以下步骤：

(1) 令`prop`为以属性名`P`调用`O`的`[[GetOwnProperty]]`内部方法的结果。

(2) 如果`prop`不是`undefined`，则返回`prop`。

(3) 令`proto`为`O`的`[[Prototype]]`内部属性的值。

(4) 如果`proto`是`null`，则返回`undefined`。

(5) 返回以参数`P`调用`proto`的`[[GetProperty]]`内部方法的结果。

```
1 GetProperty = λ(O,P). {
2   var prop, proto, result;
3   prop = ◦getOwnPropertyDescriptor(O,P); /* (1) */
4   if (prop !== undefined) { return prop } /* (2) */
5   else {
6     proto = ◦getPrototypeOf(O); /* (3) */
7     if (proto === null) { return undefined } /* (4) */
8     else {
9       result = GetProperty(proto, P); /* (5) */
10      return result
11    }
12  }
13 }
```

(a) `[[GetProperty]]`内部方法

(b) 用`JS<sup>explicit</sup>`编写的函数`GetProperty`

图 4：`[[GetProperty]]`内部方法的规范及其用`JS<sup>explicit</sup>`表示的含义

图 5a 和 5b 展示了带有提示`String`的`[[DefaultValue]]`内部方法的规范及其用`JSexplicit`表示的含义。`[[DefaultValue]]`方法定义了当给定值是对象时的动态类型转换。在字段查找操作`o[s]`中，当给定的字段名指示符`s`是对象时，它通过调用`[[DefaultValue]]`方法将字段名值`s`转换为字符串类型的值。在`[[DefaultValue]]`方法中，它首先以参数`toString`调用`[[Get]]`内部方法，我们在图 3a 中定义了其对应的辅助函数（步骤 1）。如果结果是可调用的，即如果该值是函数（步骤 2），它以`0`作为`this`值调用结果函数（步骤 2a）。如果`toString`的结果是原始值，则返回该结果（步骤 2b）。否则，它以参数`valueOf`调用`[[Get]]`内部方法（步骤 3）。如果结果是可调用的（步骤 4），它以`0`作为`this`值调用结果函数（步骤 4a）。如果`valueOf`的结果是原始值，则返回该结果（步骤 4b）。如果`toString`和`valueOf`的结果值都不是原始值，则抛出`TypeError`异常（步骤 5）。在用`JSexplicit`编写的辅助函数中，它创建一个`TypeError`的实例，该实例指定了`TypeError`对象的一个内置函数。

当以提示`String`调用`O`的`[[DefaultValue]]`内部方法时，将执行以下步骤：

(1) 令`toString`为以参数`"toString"`调用对象`O`的`[[Get]]`内部方法的结果。

(2) 如果`IsCallable(toString)`为`true`，则，

    (a) 令`str`为以`O`作为`this`值和空参数列表调用`toString`的`[[Call]]`内部方法的结果。

    (b) 如果`str`是原始值，则返回`str`。

(3) 令`valueOf`为以参数`"valueOf"`调用对象`O`的`[[Get]]`内部方法的结果。

(4) 如果`IsCallable(valueOf)`为`true`，则，

    (a) 令`val`为以`O`作为`this`值和空参数列表调用`valueOf`的`[[Call]]`内部方法的结果。

    (b) 如果`val`是原始值，则返回`val`。

(5) 抛出`TypeError`异常。

```
1 DefaultValue = λ(O,hint). {
2   var str, val, toString, valueOf;
3   if (hint === "String") {
4     toString = Get(O, "toString"); /* (1) */
5     if (typeof toString === "function") { /* (2) */
6       str = ◦apply(toString, O, []); /* (2a) */
7       if (!isPrimitive(str)) return str else { } /* (2b) */
8     } else { }
9     valueOf = Get(O, "valueOf"); /* (3) */
10    if (typeof valueOf === "function") { /* (4) */
11      val = ◦apply(valueOf, O, []); /* (4a) */
12      if (!isPrimitive(val)) return val else { } /* (4b) */
13    } else { }
14    throw TypeError();   /* (5) */
15  } else { /* hint === "Number" */
16    /* 它按顺序调用 "valueOf" 和 "toString"。 */
17  }
18 }
```

(a) `[[DefaultValue]]`内部方法

(b) 用`JS<sup>explicit</sup>`编写的函数`DefaultValue`

图 5：`[[DefaultValue]]`内部方法的规范及其用`JS<sup>explicit</sup>`表示的含义

图 6 展示了在`ECMAScript`规范中定义的`ToString`和`ToNumber`操作的语义。如果该值不是对象，它分别通过`◇toString`和`◇toNumber`操作将原始值转换为字符串值和数字值。否则，它以提示`"String"`或`"Number"`调用`DefaultValue`，这模拟了`[[DefaultValue]]`的语义。然后，它再次使用`DefaultValue`的结果调用函数本身`ToString`或`ToNumber`。由于辅助函数`DefaultValue`总是返回原始值，此递归不会创建循环，并且辅助函数`ToString`和`ToNumber`分别返回字符串和数字值。



```text
1 ToString = λ(x). {
2   if (!isObject(x)) { return ◦toString(x) }
3   else {
4     x = DefaultValue(x, "String");
5     x = ToString(x);
6     return x
7   }
8 }
```

### （a）辅助函数 `ToString`

```text
1 ToNumber = λ(x). {
2   if (!isObject(x)) { return ◦toNumber(x) }
3   else {
4     x = DefaultValue(x, "Number");
5     x = ToNumber(x);
6     return x
7   }
8 }
```

### （b）辅助函数 `ToNumber`

图 6：JS<sup>explicit</sup> 中的 `ToString` 和 `ToNumber`

所有涉及转换和字段访问的 JavaScript 函数都以类似方式包装。

### 对 ECMAScript 内置函数的支持

ECMAScript 内置函数也依赖于上述定义的原始操作，其语义涉及隐式字段访问。例如，让我们考虑 String API 的 `slice` 方法。根据规范 [4]，当调用此方法时，`this` 参数必须转换为字符串，参数必须转换为整数。这些转换也必须受到保护。为此，原始的 `slice` 函数（`String.prototype.slice`）通过一个定义如下的 JS<sup>explicit</sup> 包装器进行保护：

```javascript
1 wrap = λ(old_slice). {
2   var new_slice = λ(start,end).{
3     var s;
4     CheckObjectCoercible(this);
5     s = ToString(this);
6     start = ToInteger(start);
7     if (end !== undefined)
8       end = ToInteger(end);
9     return ◦apply(old_slice, s, [start,end]);
10  }
11 };
12 /* 包装后的 String.prototype.slice */
13 slice = wrap(String.prototype.slice);
```

我们展示转换函数 `compile[[P]]`，它接受 JavaScript 代码 `P` 并将其转换为 JS<sup>explicit</sup>。

首先，我们考虑对全局变量的显式引用，例如 `Object`、`Function` 或 `String`。这些显式引用将被替换。

## 4 实现：SecureJS

在本节中，我们将介绍 SecureJS 的实现。SecureJS 编译后的程序在隔离的领域中执行，这些领域与其他领域不共享任何引用。因此，如果编译后的程序不向其他程序导出值，其执行过程将保持完全的内存隔离，并保证运行编译后的程序与其他未编译程序不会相互干扰。

这种隔离依赖于一个安全的运行时环境，该环境由一个隔离的虚拟全局对象和内置对象，以及安全的原始操作组成。这些操作将全局和内置对象的字段访问重定向到相应的虚拟对象。本节将详细阐述安全原始操作和运行时环境的实现。

### 4.1 安全原始操作

SecureJS 编译器重写 JavaScript 程序的方式，使得任何表达式都无法显式或隐式地访问未编译代码创建的对象。为此，编译后的代码用自定义操作替换了正常的对象字段访问和正常的原型链查找，以强制执行内存隔离。让我们详细说明这些操作。

首先，对全局变量的显式引用必须替换为对代理这些全局普通对象的安全对象的访问。为此，编译器将全局变量访问 `x` 转换为库函数调用 `SJS.Loadvar("x")`，定义如下：

```javascript
SJS.Loadvar = function SJSloadvar(id) {
  return Get(SJS.global, id);
}
```

对象 `SJS.global` 是全局对象的安全版本。它确保与全局对象的所有交互都不会暴露给未编译的代码。

其次，必须拦截对象字段访问，以防止正常的原型链检查访问未编译环境的对象。为此，我们提供了一个安全版本的 `GetProperty` 辅助函数，定义如下：

```javascript
SJS.GetProperty = function SJSGetProperty(O, P) {
  var prop;
  prop = SJS.getOwnPropertyDescriptor(O,P); /* (1) */
  if (prop !== undefined) return prop; /* (2) */
  else {
      O = SJS.getPrototypeOf(O); /* (3) */
      if (O === null) return undefined; /* (4) */
      if (SJS.securePrototypeOf(O) !== undefined)
          O = SJS.securePrototypeOf(O)
      return SJSGetProperty(O,P); /* (5) */
  }
}
```

关键点在于第 8 行。它确保字段查找永远不会逃逸到编译环境控制的内存之外。如果字段搜索命中属于未编译代码的全局对象，它会将搜索重定向到 SecureJS 控制下的另一个对象（第 9 行）。

为了与当前的物联网平台（如 JerryScript [5]）兼容，SecureJS 编译并以 ECMAScript 5 为目标，但它也支持受限版本的 ECMAScript 6 模块导出形式。导出指令用于在编译和未编译代码之间建立通信通道。编译器将声明 `export id` 转换为：

```javascript
id = SJS.Loadvar("id")
```

其中左侧的 `id` 指定领域外的全局变量 `id`。

编译器的最后一个作用是为编译后的代码创建一个安全的执行上下文。为此，编译后的代码将被嵌入到一个匿名函数中，该函数将首先创建安全环境，然后执行客户端代码。也就是说，所有编译后的程序都具有以下形式：

```javascript
(function() {
    var SJS = SJSbootstrap();
    ... client compiled code ...
})();
```

SecureJS 编译后的代码保证任何未编译的表达式都无法访问编译代码创建的对象。变量 `SJS` 隐藏在编译代码的局部作用域中，而函数 `SJSbootstrap` 是不可变的，每次调用时都会返回一个新的隔离领域。

### 4.2 安全运行时环境

SecureJS 编译后的代码通过在执行开始时调用 `SJSbootstrap`（见图 7，第 42 行）函数来初始化安全环境。该函数定义在库 `sjs.js` 中，该库捕获原生内置对象并为编译后的程序提供安全接口。在本节中，我们将介绍该库的实现。

`sjs.js` 库在任何其他计算之前执行。它捕获标准 JavaScript 函数（第 2-5 行）并将它们存储在函数局部变量中，这样它们就不会被库外部篡改。它创建一个不可变字段 `@call` 指向 `SJScall`，其值为 `Function.prototype.call` 的内置值（第 6 行），这样调用表达式 `SJScall['@call'](f,obj,args)` 的语义也无法被篡改，并且 `SJScall['@call'](f,obj,args)` 在 JS<sup>explicit</sup> 中实现了 `«apply(f,obj,args)`。该库定义了函数 `SJSbootstrap`（第 9 行），该函数绑定到全局 JavaScript 变量 `SJSbootstrap`（第 42 行）。函数定义需要两个步骤，因为这是 ECMAScript 5 提出的定义只读变量的唯一方式。

```javascript
(function() {
    var SJScall = Object.create;
    var SJScall = Function.prototype.call;
    var SJSObjProto = Object.prototype;
    var SJSFunProto = Function.prototype; ...
    Object.defineProperty(SJScall, '@call',
        { value: SJScall, configurable: false,
          writable: false, enumerable: false });
    function SJSbootstrap() {
        function securePrototypeOf(obj) {
            if(obj === SJSObjProto)
                return SecureObjP;
            if(obj === SJSFunProto)
                return SecureFunP;
            ...
            return false;
        }
        var global = SJScall(null);
        var SJS = SJScall(null);
        SJS.global = global;
        function CheckObjectCoercible(o) {...};
        function Get(x) {...};
        function DefaultValue_S(x) {...};
        function ToString(o) {...};
        function ToNumber(o) {...};
        function ToInteger(o) {...};
        SJS.Loadvar = function (id) {...};
        SJS.GetProperty = function (O, P) {...};
        global.Object = function (v) {...};
        ...
        global.String.prototype.slice =
            function(v) {...};
        var SecureObjP =
            global.Object.prototype =
                SJScall(null);
        var SecureFunP =
            global.Function.prototype =
                SJScall(SecureObjP);
        ...
        return SJS;
    };
    Object.defineProperty(this,
        "SJSbootstrap", {
            value:SJSbootstrap, configurable:false,
            writable:false, enumerable:false });
})();
```

图 7：`sjs.js` 的摘录。

函数 `SJSbootstrap` 创建一个常规 JavaScript 对象（第 18 行），该对象将作为安全代码内标准 JavaScript 全局对象的替代品。

## 5 评估

本节旨在通过实验验证 SecureJS 编译器保留了原始程序的语义，并且编译后的代码符合内存隔离。首先，我们使用 Test262 测试套件测试 SecureJS 编译在实用 JavaScript 引擎 V8 [6]、Hop [12] 和 JerryScript [5] 中是否保留了原始程序的语义。其次，我们通过测试编译后程序的执行是否会导致隐式字段访问，来测试 SecureJS 编译后的程序是否符合内存隔离。为此，我们在 Hop 和 JerryScript JavaScript 引擎中使用了 Test262 测试套件。

### 5.1 实验设置

我们在开源 JavaScript 引擎 Hop 编译器 [12] 的前端之上实现了 SecureJS。SecureJS 接收一个 JavaScript 程序，并生成一个符合 ECMAScript 第 5 版规范的 JavaScript 程序。执行使用了最先进的 JavaScript 引擎 V8、Hop 和 JerryScript。

我们使用 Test262 测试套件，并采用其 GitHub 仓库中的 `es5-tests` 分支。由于 Test262 测试套件的测试程序通过 `assert` 函数来检查程序状态和流程，因此比较最终状态可以确认程序的等效执行。Test262 程序还测试了所有 ECMAScript 内置函数的语义以及严格模式函数的语义。我们将 10490 个测试程序作为 Test262 测试套件的目标测试程序，并从目标程序中排除了 1082 个测试程序。具体来说，我们排除了使用 `eval` 函数和 `with` 语句的测试。SecureJS 不支持 `eval` 和 `with`。此外，我们还排除了检查语法错误的测试。最新版本的 ECMAScript 规定的语法规则比 ECMAScript 第 5 版规定的语法规则更宽松。由于 SecureJS 的前端解析器为了兼容性支持最新的 ECMAScript 规范，它会解析遵循最新 ECMAScript 规范的程序，并在可能的情况下将其翻译成兼容 ECMAScript 第 5 版的程序。

### 5.2 测试语义保持

本实验的目标是展示 SecureJS 编译器保持了原始程序的语义。为此，我们编译了 Test262 套件的目标测试程序，并在 V8、Hop 和 JerryScript JavaScript 引擎上运行它们，然后检查原始程序和相应编译后程序的结果状态是否等效。

在 10490 个测试程序中，V8 成功通过了 10386 个。104 个失败是由于源语言 Test262 所假设的语义与 V8 支持的最新 JavaScript 演进之间存在差异。SecureJS 保持了这一结果。也就是说，10386 个成功的测试在 SecureJS 编译后仍然成功，104 个失败的测试仍然失败。Hop 通过了 10414 个测试程序，76 个测试失败；JerryScript 通过了 10474 个测试程序，16 个测试失败。SecureJS 也保持了这些结果。

### 5.3 测试内存隔离

SecureJS 编译后的程序运行时，仿佛运行在一个隔离的领域中。如果编译后的程序没有有意导出值以与外界交互，那么编译后的程序和其他未编译的程序将无法相互引用。在本节中，我们测试不使用 `export` 的此类 SecureJS 编译程序是否遵守此隔离属性。为此，我们通过实验验证编译后的程序是否曾访问受控领域之外的对象。

在实验中，我们修改了 Hop 和 JerryScript 的实现，以记录所有对遍历原型链所需的 `[[Prototype]]` 字段的访问。我们使用了两种截然不同的 JavaScript 实现，以降低未被注意到的 `[[Prototype]]` 访问（这些访问可能被 JavaScript 引擎优化器移除，与 SecureJS 无关）的概率。此外，我们还修改了 JerryScript 引擎，以记录所有对全局对象和内置对象（它们位于受控领域之外）的访问。

我们使用插桩的 JavaScript 引擎执行了 Test262 套件中的所有 10490 个程序。我们确认没有对全局对象和内置对象的字段访问尝试。我们观察到一种情况，即 SecureJS 编译的程序隐式访问了 `[[Prototype]]`。在程序初始化期间，表达式 `Object.create(null)` 创建了一个具有空原型链的空对象。随后，该对象被用于优化 SecureJS 的字段访问。由于该对象没有原型链，这些访问是无害的，但被插桩引擎记录了下来。

## 6 相关工作

迄今为止，已有许多研究致力于在 JavaScript 中提供内存隔离。

Bhargavan 等人 [2] 提出了防御性 JavaScript（DJS），这是 JavaScript 语言的一个小子集，满足静态类型约束。DJS 通过使用不涉及动态特性的 JavaScript 语言小子集来实现内存隔离。DJS 的主要局限性在于，遗留代码需要手动重写为 DJS 子集并具有可类型性才能实现内存隔离。用 DJS 编写的程序不依赖于领域，也不能使用 ECMAScript 规范中定义的内置函数。

Swamy 等人 [14] 提出了 JS*，这是一种支持 JavaScript 各种动态特性的编程语言，同时在存在不受信任的 JavaScript 程序时确保类型安全。由于它要求受信任的程序进行类型注解，遗留代码需要手动重写为 JS*，并且在内置函数支持方面，它只支持 JavaScript 语言的一个小子集。它实现了一种有限形式的接口用于相互通信，因为接口需要类型注解，并且必须使用编译后的解释器程序来实现接口函数。

Terrace 等人 [15] 实现了一个用 JavaScript 编写的 JavaScript 解释器。它支持使用原始值、类型化对象以及具有类型化参数和返回值的函数进行交互，并且它不能在 JerryScript 引擎上工作。由于这些原因，它尤其不能应用于物联网环境。

Vasilakis 等人 [16] 提出了 BreakApp，它提供了程序之间的隔离和交互策略。它依赖于各种级别的内置隔离原语，但隔离机制强烈依赖于 Node.js。BreakApp 所依赖的隔离机制之一是 Node.js 支持的隔离领域。

Guha 等人 [7] 提出了核心演算 λJS 的形式语义，并提供了将 JavaScript 归约到 λJS<sup>explicit</sup> 的步骤。这个归约步骤类似于我们到 JS<sup>explicit</sup> 的翻译，但我们到 JS<sup>explicit</sup> 的翻译侧重于将原始操作重写为其安全版本，以模拟 JavaScript 领域。

## 7 结论



我们提出了`SecureJS`，一个安全的`JavaScript`到`JavaScript`编译器。它将程序转换为等效的程序，但这些程序执行时仿佛运行在一个隔离的领域内。该编译器是可移植的，并且只使用标准特性，因此可以被任何`JavaScript`引擎使用。为了重写`JavaScript`语言动态特性的语义，我们提出了`JS$^{explicit}$`，它不涉及隐式字段访问，并提出了从`JavaScript`到`JS$^{explicit}$`的翻译。

在评估中，我们展示了编译保持了使用`ECMAScript 5.1`全部特性的原始程序的语义，并且如果给定程序不导出值，则实现了内存隔离。为了展示编译后程序的执行保持了内存隔离，我们使用了插桩的`JavaScript`引擎，并且据我们所知，之前没有人尝试过通过`JavaScript`引擎插桩来测试此类属性。`SecureJS`编译器为使用依赖于隔离领域的`JavaScript`安全执行库提供了一个基本构建块，特别是，它使我们能够在不支持内置隔离机制的`JerryScript` `JavaScript`实现中使用此类库。

## 参考文献

[1] Agoric. 2020. SES: Proposal for Secure EcmaScript. https://github.com/tc39/proposal-ses.

[2] Karthikeyan Bhargavan, Antoine Delignat-Lavaud, and Sergio Maffeis. 2013. Language-based Defenses Against Untrusted Browser Origins. In Presented as part of the 22nd USENIX Security Symposium (USENIX Security 13). USENIX, Washington, D.C., 653–670.

[3] Martin Bodin, Arthur Charguéraud, Daniele Filaretti, Philippa Gardner, Sergio Maffeis, Daiva Naudziuniene, Alan Schmitt, and Gareth Smith. 2014. A Trusted Mechanised `JavaScript` Specification. In Proceedings of the 41st ACM SIGPLAN-SIGACT Symposium on Principles of Programming Languages (POPL '14). ACM, New York, NY, USA, 87–100. https://doi.org/10.1145/2535838.2535876

[4] European Association for Standardizing Information and Communication Systems (ECMA). 2011. ECMA-262: `ECMAScript` Language Specification. Edition 5.1.

[5] Evgeny Gavrin, Sung-Jae Lee, Ruben Ayrapetyan, and Andrey Shitov. 2015. Ultra Lightweight `JavaScript` Engine for Internet of Things. In Companion Proceedings of the 2015 ACM SIGPLAN International Conference on Systems, Programming, Languages and Applications: Software for Humanity (SPLASH Companion 2015). ACM, New York, NY, USA, 19–20. https://doi.org/10.1145/2814189.2816270

[6] Google. 2018. V8 `JavaScript` Engine. http://developers.google.com/v8.

[7] Arjun Guha, Claudiu Saftoiu, and Shriram Krishnamurthi. 2010. The Essence of `JavaScript`. In ECOOP 2010 – Object-Oriented Programming, Theo D'Hondt (Ed.). Springer Berlin Heidelberg, Berlin, Heidelberg, 126–150.

[8] Zhengqin Luo and Tamara Rezk. 2012. Mashup Compiler: Mashup Sandboxing Based on Inter-frame Communication. In Proceedings of the 2012 IEEE 25th Computer Security Foundations Symposium (CSF '12). IEEE Computer Society, Washington, DC, USA, 157–170. https://doi.org/10.1109/CSF.2012.22

[9] Mark S. Miller, Mike Samuel, Ben Laurie, Ihab Awad, and Mike Stay. October 2007. Caja - safe active content in sanitized `JavaScript`. http://math.ucr.edu/-mike/caja-spec-2008-06-06.pdf.

[10] Nick Nikiforakis, Luca Invernizzi, Alexandros Kapravelos, Steven Van Acker, Wouter Joosen, Christopher Kruegel, Frank Piessens, and Giovanni Vigna. 2012. You are what you include: large-scale evaluation of remote `JavaScript` inclusions. In the ACM Conference on Computer and Communications Security. CCS'12, Raleigh, NC, USA, October 16-18, 2012. 736–747.

[11] Joe Gibbs Politz, Spiridon Aristides Eliopoulos, Arjun Guha, and Shriram Krishnamurthi. 2011. ADsafety: Type-based Verification of `JavaScript` Sandboxing. In Proceedings of the 20th USENIX Conference on Security (SEC'11). USENIX Association, Berkeley, CA, USA, 12–12. http://dl.acm.org/citation.cfm?id=2028067.2028079

[12] Manuel Serrano and Vincent Prunet. 2016. A Glimpse of Hopjs. In Proceedings of the 21st ACM SIGPLAN International Conference on Functional Programming (ICFP 2016). ACM, New York, NY, USA, 180–192. https://doi.org/10.1145/2951913.2951916

[13] Patrik Simek. 2020. VM2 npm package. https://www.npmjs.com/package/vm2.

[14] Nikhil Swamy, Cedric Fournet, Aseem Rastogi, Karthikeyan Bhargavan, Juan Chen, Pierre-Yves Strub, and Gavin Bierman. 2014. Gradual Typing Embedded Securely in `JavaScript`. In Proceedings of the 41st ACM SIGPLAN-SIGACT Symposium on Principles of Programming Languages (POPL '14). ACM, New York, NY, USA, 425–437. https://doi.org/10.1145/2535838.2535889

[15] Jeff Terrace, Stephen R. Beard, and Naga Praveen Kumar Katta. 2012. `JavaScript` in `JavaScript` (`js.js`): Sandboxing Third-Party Scripts. In Presented as part of the 3rd USENIX Conference on Web Application Development (WebApps 12). USENIX, Boston, MA, 95–100.

[16] Nikos Vasilakis, Ben Karel, Nick Roessler, Nathan Dautenhahn, André DeHon, and Jonathan M. Smith. 2018. BreakApp: Automated, Flexible Application Compartmentalization. In 25th Annual Network and Distributed System Security Symposium, NDSS 2018, San Diego, California, USA, February 18-21, 2018. The Internet Society.
