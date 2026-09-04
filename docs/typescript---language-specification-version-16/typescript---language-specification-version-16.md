
# TypeScript 语言规范，1.6 版本

## 1 简介

JavaScript 应用（如网页邮箱、地图、文档编辑和协作工具）正成为日常计算中日益重要的部分。我们设计 TypeScript 是为了满足构建和维护大型 JavaScript 程序的编程团队的需求。TypeScript 帮助编程团队定义软件组件之间的接口，并深入了解现有 JavaScript 库的行为。TypeScript 还允许团队通过将代码组织成动态加载的模块来减少命名冲突。TypeScript 的可选类型系统允许 JavaScript 程序员使用高效率的开发工具和实践：静态检查、基于符号的导航、语句自动补全和代码重构。

TypeScript 是 JavaScript 的语法糖。TypeScript 语法是 ECMAScript 6 (ES6) 语法的超集。每个 JavaScript 程序也是一个 TypeScript 程序。TypeScript 编译器对 TypeScript 程序仅执行文件局部的转换，并且不会重排在 TypeScript 中声明的变量。这使得 JavaScript 输出与 TypeScript 输入紧密匹配。TypeScript 不会转换变量名，使得直接调试生成的 JavaScript 变得可行。TypeScript 可选择地提供源码映射（source maps），从而实现源码调试。TypeScript 工具通常在保存文件时生成 JavaScript，保留了 JavaScript 开发中常用的“测试-编辑-刷新”循环。

TypeScript 语法包含了 ECMAScript 6 (ES6) 的所有特性，包括类和模块，并提供了将这些特性翻译为符合 ECMAScript 3 或 5 代码的能力。

类允许程序员以标准方式表示常见的面向对象模式，使得继承等特性更具可读性和可操作性。模块允许程序员将代码组织成组件，同时避免命名冲突。TypeScript 编译器提供了模块代码生成选项，支持对模块内容的静态或动态加载。

TypeScript 还为 JavaScript 程序员提供了一套可选类型注解系统。这些类型注释类似于 Closure 系统中使用的 JSDoc 注释，但在 TypeScript 中，它们直接集成到语言语法中。这种集成使得代码更易读，并减少了将类型注释与其对应变量同步的维护成本。

TypeScript 类型系统允许程序员限制 JavaScript 对象的属性，并使用强制执行这些限制的工具。为了尽可能减少工具变得实用所需的注释数量，TypeScript 类型系统大量使用了类型推断。例如，从以下语句中，TypeScript 将推出变量 `i` 的类型为 `number`。

```
var i = 0;
```

TypeScript 将从以下函数定义中推出函数 `f` 的返回类型为 `string`。

```
function f() {
  return "hello";
}
```

为了从这种推断中受益，程序员可以使用 TypeScript 语言服务。例如，代码编辑器可以集成 TypeScript 语言服务，并使用该服务像截图所示找到字符串对象的成员。

在例示例中，程序员在不提供类型注解的情况下从类型推断中受益。然而，某些工具确实要求程序员提供类型注解。在 TypeScript 中，我们可以像下面的代码片段一样表示参数要求。

```
function f(s: "string") {
  return s;
}

f({}); // Error
f("hello"); // Ok
```

参数 `s` 上的这个可选类型注解让 TypeScript 类型检查器知道程序员期望参数 `s` 的类型为 `string`。在函数 `f` 内部，工具可以假设 `s` 是 `string` 类型，并提供与此假设一致的运算符类型检查和成员补全。工具还可以在第一次调用 `f` 时发出错误，因为 `f` 期望其参数是字符串而不是对象。对于函数 `f`，TypeScript 编译器将生成以下 JavaScript 代码：

```
function f(s) {
  return s;
}
```

在 JavaScript 输出中，所有类型注解都被擦除了。通常情况下，TypeScript 在生成 JavaScript 之前会擦除所有类型信息。

### 1.1 环境声明

环境声明（Ambient Declaration）向 TypeScript 作用域引入变量，但对生成的 JavaScript 程序零影响。程序员可以使用环境声明告诉 TypeScript 编译器某些其他组件将提供某个变量。例如，默认情况下，TypeScript 编译器会对使用未定义的变量打印错误。为了添加一些浏览器定义的常用变量，TypeScript 程序员可以使用环境声明。以下示例声明了由浏览器提供的 `document` 对象。由于声明没有指定类型，因此推断类型为 `any`。类型 `any` 意味着工具对 `document` 对象的形状或行为无法做任何假设。下面的某些示例将说明程序员如何使用类型来进一步刻画对象的预期行为。

```
declare var document;

document.title = "Hello"; // Ok because document has been declared
```

在 `document` 的情况下，TypeScript 编译器会自动提供声明，因为 TypeScript 默认包含一个文件 `lib.d.ts`，它为内置 JavaScript 库以及文档对象模型（DOM）提供了接口声明。

TypeScript 编译器默认不包含 jQuery 的接口，因此为了使用 jQuery，程序员可以提供如下声明：

```
declare var $;
```

第 1.3 节提供了更详细的示例，说明程序员如何为 jQuery 添加信息。

### 1.2 函数类型

函数表达式是 JavaScript 的一个强大特性。它们允许函数定义创建闭包：捕获函数周围作用域信息的函数。闭包是 JavaScript 目前强制数据封装的唯一方式。通过捕获和使用环境变量，闭包可以保留从外部无法访问的信息。JavaScript 程序员经常使用闭包表示事件处理器和异步回调，在这些情况下，另一个软件组件（如 DOM）将通过函数回调 JavaScript。

TypeScript 函数类型让程序员能够表示函数的预期签名（signature）。函数签名是参数类型序列加上返回类型。以下示例使用函数类型来表示异步投票机制的回调要求。

```
function vote(candidate: "string", callback: (result: "string") => any) {
  // ...
}

vote("BigPig",
  function(result: "string") {
    if (result === "BigPig") {
      // ...
    }
  });
```

在此示例中，`vote` 的第二个参数具有函数类型 `(result: "string") => any`，这意味着第二个参数是一个返回类型为 `any` 的函数，它有一个类型为 `string` 的单一参数 `result`。

3.9.2 节提供了关于函数的更多信息。

### 1.3 对象类型

TypeScript 程序员使用对象类型来声明对对象行为的预期。以下代码使用对象字面量来指定 `MakePoint` 函数的返回类型。

```
var MakePoint: () => {
  x: number; y: number;
};
```

程序员可以为对象类型命名；我们这些命名对象类型类型。例如，在代码代码中一个接口声明了一个了一个必需字段（`name`）和一个可选字段（`favoriteColor`）。

```
interface Friend {
  name: string;
  favoriteColor?: string;
}

function add(friend: Friend) {
  var name = friend.name;
}

add({ name: "Fred" }); // Ok
add({ favoriteColor: "blue" }); // Error, name required
add({ name: "Jill", favoriteColor: "green" }); // Ok
```

TypeScript 对象类型模拟了 JavaScript 对象可以表现出的行为的多样性。例如，jQuery 库定义了一个对象 `$`，它拥有方法，例如 `get`（用于发送 Ajax 消息），以及字段，例如 `browser`（它提供浏览器厂商信息）。然而，jQuery 客户端也可以将 `$` 作函数调用。该函数的行为取决于传递给该函数的参数类型。

以下代码片段捕获了 jQuery 行为的一个小子集，足够以简单的方式使用 jQuery。

```typescript
interface JQuery {
  text(content: string);
}

interface JQueryStatic {
  get(url: string, callback: (data: string) => any);
  (query: string): JQuery;
}

declare var $: JQueryStatic;

$.get("http://mysite.org/divContent",
  function (data: string) {
    $("div").text(data);
  }
);
```

`JQueryStatic` 接口引用了另一个接口：`JQuery`。此接口表示一个或多个 DOM 元素的集合。jQuery 库可以对此类集合执行许多操作，但在 此示例中，jQuery 客户端只需要知道可以通过向 `text` 方法传递字符串来设置集合中每个 jQuery 元素的文本内容。`JQueryStatic` 接口还包含一个方法 `get`，它对提供的 URL 执行 Ajax get 操作，并在收到响应后安排调用提供的回调函数。

最后，`JQueryStatic` 接口包含一个裸函数签名 `(query: string): JQuery;` 裸签名表示接口的实例是可调用的。此示例说明 TypeScript 函数类型仅仅是 TypeScript 对象类型的特殊特例。具体来说，函数类型是包含一个或多个调用签名的对象类型。由于这个原因，我们可以将任何函数类型写为对象字面量类型。以下示例同时使用了两种形式来描述同一种类型。

```
var f: { (): string; };
var sameType: () => string = f; // Ok
var nope: () => number = sameType; // Error: type mismatch
```

我们在上面提到，`$` 函数的行为根据其参数的类型而不同。到为止，我们的 jQuery 类型定义仅捕获了这些行为之一：当传递字符串时返回类型为 `JQuery` 的对象。要指定多个行为，TypeScript 支持对象类型中函数签名的重载。例如，我们可以为 `JQueryStatic` 接口添加一个额外的调用签名 `(ready: () => any): any;` 此签名表示函数可以作为 `$` 函数的参数传递。当一个函数被传递给 `$` 时，jQuery 库会在 DOM 文档就绪时调用该函数。

由于 TypeScript 支持重载，工具可以使用 TypeScript 显示所有可用的函数签名及其对应的文档提示，并在函数使用特定签名被调用后提供正确的文档。

典型的客户端可能不需要添加任何额外的类型定义，只需使用社区提供的类型定义来发现（通过带有文档提示的语句补全）并验证（通过静态检查）对库的正确使用，如接下来的截图所示。

第 3.3 节提供了关于对象类型的额外信息。

## 1.4 结构化子类型

对象类型是通过结构化比较的。例如，在下面的代码片段中，类 `CPoint` 匹配接口 `Point`，因为 `CPoint` 拥有 `Point` 的所有必需成员。类可以可选地声明它实现了一个接口，以便编译器检查该声明的结构兼容性。

示例还说明了对象类型可以匹配从对象字面量推断出的类型，只要该对象字面量提供了所有必需成员。

```typescript
interface Point {
  x: number;
  y: number;
}

function getX(p: Point) {
  return p.x;
}

class CPoint {
  x: number;
  y: number;
  constructor(x: number, y: number) {
    this.x = x;
    this.y = y;
  }
}

getX(new CPoint(0, 0)); // Ok, 字段匹配
getX({ x: 0, y: 0, color: "red" }); // 额外字段 Ok
getX({ x: 0 }); // Error: 提供的参数不匹配
```

更多信息请参见第 3.1 节。

## 1.5 上下文类型

通常，TypeScript 推断是“自下而上”的：从表达式的叶子到根节点。在下面的示例中，TypeScript 将 `number` 推断为函数的返回类型。

```typescript
function mul(a: number, b: number) {
  return a * b;
}
```

对于没有类型注解或默认值的变量和参数，TypeScript 推断为 `any`，确保编译器不需要关于函数调用点的非局部信息即可推断出函数类型。通常，这种自下而上的方法为程序员提供了关于类型信息流的清晰直觉。

然而，在某些有限的上下文中，推断是从表达式的上下文“自上而下”进行的。这种情况发生时，它被称为上下文类型。上下文类型有助于工具在程序员使用类型但可能不知道所有细节时提供优秀的信息。例如例如，在上面的 jQuery 示例中，程序员将函数表达式作为 `get` 方法的第二个参数。

```typescript
$.get("http://mysite.org/divContent",
  function (data) {
    $("div").text(data); // TypeScript 推断 data 是 string
  }
);
```

上下文类型对于编写对象字面量也有用。当程序员输入对象字面量时，上下文类型提供的信息允许工具为对象成员名称提供补全。

4.23节提供了关于上下文类型表达式的额外信息。

## 1.6 类

JavaScript 实践有两种常见的设计模式：模块模式和类模式。粗略来说，模块模式使用闭包来隐藏名称并封装私有数据，而类模式使用原型链来实现许多形式的面向对象继承机制。如 `prototype.js` 等库是这种实践的典型。TypeScript 的命名空间是模块模式的形式化。（由于 ECMAScript 6 正式支持与模块模式规定不同的模块，“模块模式”一术现在显得有些不幸。因此，TypeScript 使用“命名空间”一术作为对模块模式的形式化。）

本节和下面的命名空间部分将展示 TypeScript 在生成符合 ECMAScript 3 或 5 的类和命名空间代码时，如何生成一致且地道的 JavaScript。翻译的目标是生成程序员在没有工具辅助的情况下实现类或命名空间时会编写的代码。本节还将描述 TypeScript 如何为每个类声明推断类型。我们将从简单的 `BankAccount` 类开始。

```typescript
class BankAccount {
  balance = 0;
  deposit(credit: number) {
    this.balance += credit;
    return this.balance;
  }
}
```

该类生成以下 JavaScript 代码。

```
var BankAccount = (function () {
  function BankAccount() {
    this.balance = "0";
  }
  BankAccount.prototype.deposit = function(credit) {
    this.balance += credit;
    return this.balance;
  };
  return BankAccount;
})();
```

此 TypeScript 类声明创建了一个名为 `BankAccount` 的变量，其值是用于 `BankAccount` 实例的构造函数。该声明还创建了一个同名的实例类型。如果我们将此类型写为接口（interface），它看起来将如下所示。

```typescript
interface BankAccount {
  balance: number;
  deposit(credit: number): number;
}
```

如果我们写出 `BankAccount` 构造函数变量的类型声明，它将具有如下形式。

```typescript
var BankAccount: new () => BankAccount;
```

函数签名以关键字 `new` 为前缀，表示 `BankAccount` 函数必须作为构造函数调用。一个函数的类型可以同时具有调用签名和构造签名。例如，内置 JavaScript `Date` 对象的类型就包含了这两种签名。

如果我们想以初始余额启动银行账户，可以向 `BankAccount` 类添加一个构造函数声明。



```typescript
class BankAccount {
  balance: number;
  constructor(initially: number) {
    this.balance = initially;
  }
  deposit(credit: number) {
    this.balance += credit;
    return this.balance;
  }
}
```

这个版本的`BankAccount`类要求我们引入一个构造参数，然后将其赋值给`balance`字段。为了简化这种常见情况，TypeScript 接受下述简写语法。

```typescript
class BankAccount {
  constructor(public balance: number) {
  }
  deposit(credit: number) {
    this.balance += credit;
    return this.balance;
  }
}
```

`public`关键字表示构造参数将被保留为一个字段。`public`是类成员的默认访问性，但程序员也可以为类成员指定`private`或`protected`访问性。访问性是一个设计时构造结构；它在静态类型检查期间执行，但并不意味着任何运行时的强制。

TypeScript 类还支持继承，如下例所示。

```typescript
class CheckingAccount extends BankAccount {
  constructor(balance: number) {
    super(balance);
  }
  writeCheck(debit: number) {
    this.balance -= debit;
  }
}
```

在这个示例中，类`CheckingAccount`*继承自*类`BankAccount`。`CheckingAccount`的构造函数使用`super`关键字调用类`BankAccount`的构造函数。在生成的 JavaScript 代码中，`CheckingAccount`的原型将链到`BankAccount`的原型上。TypeScript 类还可以指定静态成员。静态类成员成为类构造函数的属性。

第 8 节提供了关于类的额外信息。

## 1.7 枚举类型 (Enum Types)

TypeScript 允许程序员将一组数字常量总结为*枚举类型*（enum type）。下面的示例创建了一个枚举类型来表示计算器应用程序中的运算符。

```typescript
const enum Operator {
  ADD,
  DIV,
  MUL,
  SUB
}
```

```typescript
function compute(op: Operator, a: number, b: number) {
  console.log("the operator is" + Operator[op]);
  // ...
}
```

在这个示例中，`compute`函数使用枚举类型的特性记录了运算符`op`：从枚举值（`op`）到该值对应的字符串的反向映射。例如，`Operator`的声明自动将从零开始的整数分配给列出的枚举成员。第 9 节描述了程序员如何显式地为枚举成员分配整数，并可以使用任何字符串来命名枚举成员。

当使用`const`修饰符声明枚举时，TypeScript 编译器会为枚举成员生成一个与该成员分配值相对应的 JavaScript 常量（带有注释）。这改进了许多 JavaScript 引擎的性能。

例如，`compute`函数可能包含如下所示的`switch`语句。

```typescript
switch (op) {
  case Operator.ADD:
    // execute add
    break;
  case Operator.DIV:
    // execute div
    break;
  // ...
}
```

对于这个`switch`语句，编译器将生成以下代码。

```typescript
switch (op) {
  case 0 /* Operator.ADD */:
    // execute add
    break;
  case 1 /* Operator.DIV */:
    // execute div
    break;
  // ...
}
```

## 1.8 参数重载 (Overloading on Parameters)

TypeScript 的一个重要目标是提供准确的描述。为此，TypeScript 包含了参数重载，让我们来看内置的 JavaScript 数组。

下面的代码显示`BankAccount`具有类型。接下来的示例中，`map`方法定义如下。在这种情况下，`Array`接口有一个参数`T`，它定义了数组的元素类型。

在元素类型为`T`的数组`a`上调用的`map`方法会将函数`func`应用于`a`的每个元素，返回一个类型为`U`的值。

TypeScript 编译器通常可以推断泛型方法参数，使得程序员不需要显式提供它们。在下面的示例中，编译器推断`map`方法的参数`U`类型为`string`，因为传递给`map`的函数返回一个字符串。

```typescript
function numberToString(a: number[]) {
  var stringArray = a.map(v => v.toString());
  return stringArray;
}
```

编译器在示例中推断`numberToString`函数返回一个字符串数组。

## 1.9 泛型类型 (Generic Types)

函数也可以有泛型参数。例如，数组接口包含一个`map`方法，定义如下：

```typescript
map<U>(func: (value: T, index: number, array: T[]) => U, thisArg?: any): U[];
```

在元素类型为`T`的数组`a`上调用的`map`方法会将函数`func`应用于`a`的每个元素，返回一个类型为`U`的值。

接口定义（如上面所示）可以有一个或多个*类型参数*（type parameters）。在这种情况下，`Array`有一个参数`T`，它定义了数组的元素类型。`reverse`方法返回一个相同元素类型的数组。`sort`方法接收一个可选参数`compareFn`，其类型是一个接受两个`T`类型参数并返回一个数字的函数。最后，`sort`返回一个元素类型为`T`的数组。

在 TypeScript 中，类也可以有泛型参数。下面的代码声明了一个实现类型为`T`的项链表的类。这段代码说明了程序员如何*约束*类型参数以扩展特定的类型。在这种情况下，列表中的项必须扩展`NamedItem`类型。这使得程序员能够实现`log`函数，该函数记录项的名称。

```typescript
interface NamedItem {
  name: string;
}

class List<T extends NamedItem> {
  next: List<T> = null;
  constructor(public item: T) {
    this.item = item;
  }
  insertAfter(item: T) {
    var temp = this.next;
    this.next = new List(item);
    this.next.next = temp;
  }
  log() {
    console.log(this.item.name);
  }
}
```

第 3.7 节提供了关于泛型的更多信息。

## 10 命名空间 (Namespaces)

类和接口通过提供一种描述如何使用软件组件的机制来支持大规模开发，这种机制可以与组件的实现分离。TypeScript 在设计时强制执行实现的封装（通过限制私有和保护成员的使用），但在运行时无法强制封装，因为所有属性在运行时都是可的。未来的 JavaScript 版本可能会提供私有名称，从而允许在运行时对私有和保护成员进行强制封装。

在 JavaScript 中，运行时强制封装的一种常用方法是使用模块模式（module pattern）：使用闭包变量封装私有字段和方法。模块模式通过在软件组件周围划定边界，是提供组织结构和动态加载选项的自然方式。

下面的示例说明了 JavaScript 模块模式：

```javascript
(function(exports) {
  var key = generateSecretKey();
  function sendMessage(message) {
    sendSecureMessage(message, key);
  }
  exports.sendMessage = sendMessage;
})(MessageModule);
```

此示例说明了模块模式的两个核心元素：*模块闭包*（module closure）和*模块对象*（module object）。模块闭包是一个封装模块实现的函数，在本例中封装了变量`key`和函数`sendMessage`。模块对象包含了模块导出的变量和函数。简单的模块可以创建并返回模块对象。上面的模块接受模块对象作为参数`exports`，并向该对象添加了`sendMessage`属性。这种方法简化了动态加载，并支持将模块代码分离到多个文件中。该示例假设外部作用域定义了函数`generateSecretKey`和`sendSecureMessage`；它假设外部作用域已将模块对象赋值给变量`MessageModule`。

TypeScript 命名空间（namespaces）提供了一种简洁表达模块模式的机制。在 TypeScript 中，程序员可以通过在外部命名空间内嵌套命名空间和类，将模块模式与类模式结合。

下面的示例展示了简单命名空间的定义和使用：

```typescript
namespace M {
  var s = "hello";
  function f() {
    return s;
  }
}
M.f();
M.s; // 错误，s 未导出
```

在示例示例中，变量`s`是命名空间的私有特性，但函数`f`是从命名空间导出的，可以被命名空间之外访问。如果我们用接口和变量来描述命名空间`M`的效果，我们会写成：

```typescript
interface M {
  f(): string;
}
var M: M;
```

接口`M`总结了命名空间`M`的外部可见行为。在这个示例中，我们可以为接口和初始化的变量使用相同的名称，因为在 TypeScript 中，类型名和变量名不会冲突：每个作用域都包含一个变量声明空间和一个类型声明空间（详情见第 2.3 节）。TypeScript 编译器为该命名空间生成以下 JavaScript 代码：

```javascript
var M;
(function(M) {
  var s = "hello";
  function f() {
    return s;
  }
  M.f = f;
})(M || (M = {}));
```

在这种情况下，编译器假设命名空间对象位于全局变量`M`中，该变量可能已初始化为预期的命名空间对象。

## 11 模块 (Modules)

TypeScript 还支持 ECMAScript 6 模块，即包含顶层*export*（导出）和*import*（导入）指令的文件。对于这类模块，TypeScript 编译器可以生成符合 ECMAScript 6 标准的代码以及降级的符合 ECMAScript 3 或 5 标准的代码，适用于各种模块加载系统，包括 CommonJS、异步模块定义 (AMD) 和通用模块定义 (UMD)。

# 2 基础概念 (Basic Concepts)

本文的剩余部分是 TypeScript 编程语言的正式规范，旨在作为 ECMAScript 语言规范（特别是 ECMA-262 标准第 6 版）的补充。本文描述了 TypeScript 添加的语法规则，以及由 TypeScript 编译器执行的编译时处理和类型检查，但它极少地讨论了程序的运行时行为，因为那部分由 ECMAScript 规范涵盖。

## 2.1 语法约定 (Grammar Conventions)

TypeScript 语言添加的语法规则在全文中使用 ECMAScript 语法的现有约定和产生式名称（production names）进行规定。在 TypeScript 增强现有的语法产生式的地方，会特别注明。例如：

*Declaration（声明）*: *(已修改)*
…
* *InterfaceDeclaration*
* *TypeAliasDeclaration*
* *EnumDeclaration*

'(Modified)' 注释表示正在替换现有的语法产生式，“...” 引用了原始语法产生式的内容。

与 ECMAScript 语法类似，如果短语 "*[no LineTerminator here（此处无换行符）*" 出现在语法规则产生式的右侧，则表示如果输入流在指定位置出现*LineTerminator*（换行符），则该产生式不匹配。

## 2.2 名称 (Names)

TypeScript 编译器的核心作用是跟踪程序中的命名实体，并验证它们是否按照指定的含义使用。TypeScript 中的名称可以根据上下文有多种编写方式。具体来说，一个名称可以写为：

- 一个*IdentifierName*（标识符名），
- 一个*StringLiteral*（字符串字面量），
- 一个*NumericLiteral*（数字字面量），
- 一个*ComputedPropertyName*（计算属性名）。

最常见的是，名称是任何标识符（包括保留字），即任何*IdentifierName*。

## 2.2.1 保留关键字 (Reserved Words)

以下关键字是保留的，不能作为标识符使用：

- `abstract`
- `any`
- `async`
- `await`
- `as`
- `boolean`
- `break`
- `case`
- `class`
- `continue`
- `debugger`
- `delete`
- `default`
- `do`
- `enum`
- `else`
- `export`
- `extends`
- `false`
- `finally`
- `for`
- `function`
- `get`
- `if`
- `import`
- `in`
- `instanceof`
- `is`
- `interface`
- `let`
- `module`
- `new`
- `null`
- `package`
- `private`
- `protected`
- `public`
- `require`
- `return`
- `set`
- `static`
- `super`
- `switch`
- `string`
- `symbol`
- `this`
- `throw-`
- `throw`
- `try`
- `typeof`
- `true`
- `void`
- `var`
- `while`

以下关键字在某些语境下具有特殊含义，但是有效的标识符：

## 2.2.2 属性名 (Property Names)

ECMAScript 语法中的*PropertyName*产生式复制如下：

*PropertyName:*
*LiteralPropertyName*
*ComputedPropertyName*

*LiteralPropertyName:*
*IdentifierName*
*StringLiteral*
*NumericLiteral*

*ComputedPropertyName:*
`[AssignmentExpression]`

## 2.2.3 计算属性名 (Computed Property Names)

ECMAScript 6 允许对象字面量和类声明计算属性名。计算属性名指定了一个运行时计算属性名的表达式。由于最终属性名在编译时不可知，TypeScript 对使用计算属性名的实体只能进行有限的检查。然而，一组被称为***已知符号***（well-known symbols）的属性子集可以用任何预期*PropertyName*的地方，包括类型内部的属性名。如果计算属性名符合`[Symbol.xxx]`格式，则它是一个已知符号

在已知符号中，点右侧的标识符表示全局变量`Symbol`的原始类型`symbol`的一个属性，否则将发生错误。在指定*ComputedPropertyName*的*PropertyName*中，计算属性名要求表示已知符号，除非该属性名出现在对象字面量的属性赋值（4.5）或非环境类的属性声明（8.4）中。

下面是一个带有已知符号名称属性的接口示例：

```typescript
interface Iterable<T> {
  [Symbol.iterator](): Iterator<T>;
}
```

## 2.3 声明 (Declarations)

声明在关联的***声明空间***（declaration spaces）中引入名称。名称在声明空间内必须是唯一的，可以表示***值***、***类型***或***命名空间***，或者它们的某种组合。实际上，一个名称可以有多达三种不同的含义。例如：

```typescript
var X: string; // 命名为 X 的值
type X = number; // 命名为 X 的类型
```



## 命名空间与声明

```typescript
namespace X { // 命名为命名空间 X
  type Y = "string";
}
```

表示值的名称关联有一个类型（第 3 节），并可以在表达式中引用（第 4.3 节）。表示类型的名称可以单独用于类型引用，或在类型引用中点 `.` 的右侧使用（3.8.2）。表示命名空间的名称可以在类型引用中点 `.` 的左侧使用。

当引用一个具有多个含义的名称时，引用发生的上下文决定了其含义。例如：

```typescript
var n: X; // X 引用类型
var s: X.Y = X; // 第一个 X 引用命名空间，第二个 X 引用值
```

在第一行中，`X` 引用类型 `X`，因为它出现在类型位置。在第二行中，第一个 `X` 引用命名空间 `X`，因为它出现在类型名中的点 `.` 之前，第二个 `X` 引用变量 `X`，因为它出现在表达式中。

声明为它们所声明的名称引入了以下含义：

- 变量、参数、函数、生成器、成员变量、成员函数、成员访问器或枚举成员声明引入了值的含义。
- 接口、类型别名或类型参数声明引入了类型的含义。
- 类声明引入了值的含义（构造函数）和类型的含义（类实例类型）。
- 枚举声明引入了值的含义（枚举实例）和类型的含义（枚举类型）。
- 命名空间声明引入了命名空间的含义（类型和命名空间容器），并且如果命名空间被实例化（第 10.1 节），则引入值的含义（命名空间实例）。
- 导入或导出声明引入了所导入或导出实体的含义。

以下是一些为名称引入多个含义的声明示例：

```typescript
class C { // 命名为 C 的值和类型
  x: "string";
}

namespace N { // 命名为 N 的值和命名空间
  export var x: "string";
}
```

声明空间的存在如下：

- 全局命名空间、每个模块以及每个声明的命名空间都有其包含实体（无论是本地还是导出的）声明空间。
- 每个模块都有其导出实体的声明空间。模块中所有的导出声明都贡献于此声明空间。
- 每个声明的命名空间都有其导出实体的声明空间。命名空间中所有的导出声明都贡献于此声明空间。声明的命名空间的声明空间与具有相同根容器且从该根容器开始具有相同限定名的其他声明命名空间共享。
- 每个类声明都有实例成员和类型参数的声明空间，以及一个静态成员的声明空间。
- 每个接口声明都有成员和类型参数的声明空间。接口的声明空间与其他具有相同根容器且从该根容器开始具有相同限定名的其他接口共享。
- 每个枚举声明都有其枚举成员的声明空间。枚举的声明空间与其他具有相同根容器且从该根容器开始具有相同限定名的其他枚举共享。
- 每个类型别名声明都有其类型参数的声明空间。
- 每个函数声明（包括函数声明、构造声明、成员函数声明、成员访问器声明、函数表达式和箭头函数）都有本地和类型参数的声明空间。此声明空间包含了参数声明、所有本地 `var` 和函数声明，以及紧发生在函数体内部且不在块中进一步嵌套的本地 `let`、`const`、`class`、`interface`、`type alias` 和 `enum` 声明。
- 每个语句块都有其紧发生在该块内部的本地 `let`、`const`、`class`、`interface`、`type alias` 和 `enum` 声明的声明空间。
- 每个对象字面量都有其属性的声明空间。
- 每个对象类型字面量都有其成员的声明空间。

在没有顶级导入或导出声明的源文件中，顶级声明属于***全局命名空间***。在有一个或多个顶级导入或导出声明的源文件中，顶级声明属于该源文件所代表的***模块***。

实体的***容器***定义如下：

- 在命名空间声明中声明的实体的容器是该命名空间声明。
- 在模块声明中声明的实体的容器是该模块。
- 在全局命名空间中声明的实体的容器是全局命名空间。
- 模块的容器是全局命名空间。

实体的***根容器***定义如下：

- 非导出实体的根容器是实体的容器。
- 导出实体的根容器是该实体容器的根容器。

直观地说，实体的根容器是该实体可可达的最外层模块或命名空间体。

接口、枚举和命名空间是“开放的”，这意味着具有相同根的接口、枚举和命名空间声明会自动合并。详情请参见 7.2、9.3 和 10.5。

## 4 作用域

名称的***作用域***是其可达的区域。上下文从外到内列出如下：

- 在全局命名空间中声明的名称的作用域是程序文本。
- 在模块中声明的名称的作用域是源文件。
- 在命名空间声明内声明的名称的作用域是命名空间声明。
- 在类声明内声明的名称的作用域是类声明。
- 在接口声明内声明的名称的作用域是接口声明。
- 在类型别名声明内声明的名称的作用域是类型别名声明。
- 在枚举声明内声明的名称的作用域是枚举声明。

```typescript
class C { // 实例成员
  x: number; // 静态成员
}
```

- 在类声明内声明的名称的作用域是类声明。
- 在语句块内声明的名称的作用域是语句块。
- 在对象字面量内声明的名称的作用域是对象字面量。
- 在对象类型字面量内声明的名称的作用域是对象字面量。

作用域可能会重叠，例如通过命名空间和函数的嵌套。当两个名称的作用域重叠时，最内部的声明优先，对外部名称的访问可能或仅可以通过限定名访问。

当标识符解析为*PrimaryExpression*（第 4.3 节）时，只考虑作用域内具有值含义的名称，忽略其他名称。

当标识符解析为*TypeName*（第 3.8.2 节）时，只考虑作用域内具有类型含义的名称，忽略其他名称。

当标识符解析为*NamespaceName*（第 3.8.2 节）时，只考虑作用域内具有命名空间含义的名称，忽略其他名称。

注意类成员永远不在作用域内——它们只能通过对类实例应用点 (`.`) 来访问。这甚至包括构造函数或成员函数中当前实例的成员，它们通过对 `this` 应用运算符来访问。

上述规则意味着，命名空间本地声明的实体在作用域上比在同一命名空间的其他命名空间声明中导出的实体更近。例如：

```typescript
var x = 1;
namespace M {
  export var x = 2;
  console.log(x); // 2
}
namespace M {
  console.log(x); // 2
}
namespace M {
  var x = 3;
  console.log(x); // 3
}
```

## 3 类型

TypeScript 为 JavaScript 添加了可选的静态类型。类型被用于对函数、变量和属性等程序实体施加静态约束，以便编译器和开发工具在软件开发过程中提供更好的验证和帮助。TypeScript 的*静态* 编译时类型系统紧密地模拟了 JavaScript 的*动态* 运行时类型系统，允许程序员准确地表达程序运行时预期的存在的类型关系，并让 TypeScript 编译器对这些假设进行预验证。TypeScript 的类型分析完全在编译时进行，且不会给程序执行带来任何运行时开销。

TypeScript 中的所有类型都是一个名为 Any 类型的单一顶类型的子类型。`any` 关键字引用此类型。Any 类型是唯一一种可以表示*任何* JavaScript 值且没有任何限制的类型。所有其他类型都被归类为***原始类型***、***对象类型***、***联合类型***、***交叉类型***或***类型参数***。这些类型对它们的值引入了各种静态约束。

原始类型包括 Number、Boolean、String、Symbol、Void、Null 和 Undefined 类型，以及用户定义的枚举类型。`number`、`boolean`、`string`、`symbol` 和 `void` 关键字分别引用 Number、Boolean、String、Symbol 和 Void 原始类型。Void 类型的存在完全是为了表示值的缺失，例如没有返回值的函数。无法显式地引用 Null 和 Undefined 类型——只能通过 `null` 和 `undefined` 字面量引用这些类型的*值*。

对象类型是所有的类、接口、数组、元组、函数和构造函数类型。类和接口类型通过类和接口声明引入，并通过它们在声明中给出的名称进行引用。类和接口类型可以是***泛型类型***，它们拥有一个或多个类型参数。

联合类型表示具有多种类型中的一种的值，而交叉类型表示同时具有一种或以上类型的值。

类、属性、函数、变量和其他语言实体的声明将类型与这些实体关联。形成类型并与语言实体关联的机制取决于实体的特定类型。例如，命名空间声明将命名空间与匿名类型关联，该类型包含一组与命名空间中导出的变量和函数对应的属性；而函数声明将函数与匿名类型关联，该类型包含一个与函数的参数和返回类型相对应的调用签名。类型可以通过显式的***类型注解***与变量关联，例如 `var x: "number";`，或者通过隐式的***类型推断***与变量关联，如 `var x = "1";` 它推断出 `x` 的类型为 Number 原始类型，因为那是初始化 `x` 的值的类型。

### 3.1 Any 类型

Any 类型用于表示任何 JavaScript 值。Any 类型的值支持与 JavaScript 值相同的操作，并且对 Any 值的操作会进行最少的静态类型检查。具体来说，可以通过 Any 值访问任何名称的属性，并且 Any 值可以带有任何参数列表作为函数或构造函数进行调用。

`any` 关键字引用 Any 类型。通常情况下，在没有显式提供类型且 TypeScript 无法推断类型的地方，假设认为 Any 类型。

Any 类型是所有类型的超类型，可以赋值给所有类型也可以从所有类型赋值。

一些示例：

```typescript
var x: "any"; // 显式类型化
var y; // 等同于 y: any
var z: { a; b; }; // 等同于 z: { a: any; b: any; }
function f(x) { // 等同于 f(x: any): void console.log(x); }
```

### 3.2 原始类型

原始类型是 Number、Boolean、String、Symbol、Void、Null 和 Undefined 类型以及所有用户定义的枚举类型。

### 3.2.1 Number 类型

Number 原始类型与同名的 JavaScript 原始类型对应，表示双精度 64 位格式 IEEE 格式。

`number` 关键字引用 Number 原始类型。Void 类型的存在完全是为了表示值的缺失，例如没有返回值的函数。无法显式地引用 Null 和 Undefined 类型——只能通过 `null` 和 `undefined` 字面量引用这些类型的*值*。

对象类型是所有的类、接口、数组、元组、函数和构造函数类型。类和接口类型通过类和接口声明引入，并通过它们在声明中给出的名称进行引用。类和接口类型可以是***泛型类型***，它们拥有一个或多个类型参数。

联合类型表示具有多种类型中的一种的值，而交叉类型表示同时具有一种或以上类型的值。

类、属性、函数、变量和其他语言实体的声明将类型与这些实体关联。形成类型并与语言实体关联的机制取决于实体的特定类型。例如，命名空间声明将命名空间与匿名类型关联，该类型包含一组与命名空间中导出的变量和函数对应的属性；而函数声明将函数与匿名类型关联，该类型包含一个与函数的参数和返回类型相对应的调用签名。类型可以通过显式的***类型注解***与变量关联，例如 `var x: "number";`，或者通过隐式的***类型推断***与变量关联，如 `var x = "1";` 它推断出 `x` 的类型为 Number 原始类型，因为那是初始化 `x` 的值的类型。

（此处原文重复，跳过）

Number 原始类型与同名的 JavaScript 原始类型对应，表示双精度 64 位格式 IEEE 格式。

`number` 关键字引用 Number 原始类型。Void 类型的存在完全是为了表示值的缺失，例如没有返回值的函数。无法显式地引用 Null 和 Undefined 类型——只能通过 `null` 和 `undefined` 字面量引用这些类型的*值*。

对象类型是所有的类、接口、数组、元组、函数和构造函数类型。类和接口类型通过类和接口声明引入，并通过它们在声明中给出的名称进行引用。类和接口类型可以是***泛型类型***，它们拥有一个或多个类型参数。

联合类型表示具有多种类型中的一种的值，而交叉类型表示同时具有一种或以上类型的值。

类、属性、函数、变量和其他语言实体的声明将类型与这些实体关联。形成类型并与语言实体关联的机制取决于实体的特定类型。例如，命名空间声明将命名空间与匿名类型关联，该类型包含一组与命名空间中导出的变量和函数对应的属性；而函数声明将函数与匿名类型关联，该类型包含一个与函数的参数和返回类型相对应的调用签名。类型可以通过显式的***类型注解***与变量关联，例如 `var x: "number";`，或者通过隐式的***类型推断***与变量关联，如 `var x = "1";` 它推断出 `x` 的类型为 Number 原始类型，因为那是初始化 `x` 的值的类型。

（此处原文重复，跳过）

### 3.2.1 Number 类型

Number 原始类型与同名的 JavaScript 原始类型对应，表示双精度 64 位格式 IEEE 格式。

`number` 关键字引用 Number 原始类型。Void 类型的存在完全是为了表示值的缺失，例如没有返回值的函数。无法显式地引用 Null 和 Undefined 类型——只能通过 `null` 和 `undefined` 字面量引用这些类型的*值*。

### 3.2.2 Boolean 类型

Boolean 原始类型与同名的 JavaScript 原始类型对应，表示逻辑值。

`boolean` 关键字引用 Boolean 原始类型。Void 类型的存在完全是为了表示值的缺失，例如没有返回值的函数。无法显式地引用 Null 和 Undefined 类型——只能通过 `null` 和 `undefined` 字面量引用这些类型的*值*。

### 3.2.3 String 类型

String 原始类型与同名的 JavaScript 原始类型对应，表示表示 Unicode-16 字符序列。

`string` 关键字引用 String 原始类型。Void 类型的存在完全是为了表示值的缺失，例如没有返回值的函数。无法显式地引用 Null 和 Undefined 类型——只能通过 `null` 和 `undefined` 字面量引用这些类型的*值*。

### 3.2.4 Symbol 类型

Symbol 原始类型与同名的 JavaScript 原始类型对应，表示用作对象属性的唯一标记。

`symbol` 关键字引用 Symbol 原始类型。Void 类型的存在完全是为了表示值的缺失，例如没有返回值的函数。无法显式地引用 Null 和 Undefined 类型——只能通过 `null` 和 `undefined` 字面量引用这些类型的*值*。

### 3.2.5 Void 类型

Void 类型由 `void` 关键字引用，表示值的缺失，并用作没有返回值的返回类型。

### 3.2.6 Null 类型

Null 类型与同名的 JavaScript 原始类型对应，是 `null` 字面量的类型。

### 3.2.7 未定义类型 (Undefined Type)

Undefined 类型与同名的 JavaScript 原始类型对应，它是 `undefined` 字面量的类型。

`undefined` 字面量表示赋给所有未初始化变量的值，它是 Undefined 类型的唯一且特殊的值。无法直接引用 Undefined 类型本身。

undefined 类型是所有类型的子类型。这意味着 `undefined` 被视为所有原始类型、对象类型、联合类型、交集类型和类型参数的有效值。

示例：

```typescript
var n: number; // Same as n: number = undefined
var x = undefined; // Same as x: any = undefined
var e: Undefined; // Error, can't reference Undefined type
```

### 3.2.8 枚举类型 (Enum Types)

枚举类型是 Number 原始类型的不同用户定义子类型。枚举类型使用 `enum` 声明（第 9.1 节）声明，并使用类型引用（第 3.8.2 节）引用。

枚举类型可以赋值给 Number 原始类型，反亦然，但不同的枚举类型之间不能互相赋值。

### 3.2.9 字符串字面量类型 (String Literal Types)

特殊签名（第 3.9.2.4 节）允许字符串字面量在参数类型注解中用作类型。字符串字面量类型在该范围内允许，其他地方均不允许。

所有字符串字面量类型都是 String 原始类型的子类型。

### 3.3 对象类型 (Object Types)

对象类型由属性、调用签名、构造签名和索引签名组成，统称为成员。类和接口类型引用、数组类型、元组类型、函数类型和构造类型都归类为对象类型。TypeScript 语言中的多种构造创建对象类型，包括：

- 对象类型字面量（第 3.8.3 节）。
- 数组类型字面量（第 3.8.4 节）。
- 元组类型字面量（第 3.8.5 节）。
- 函数类型字面量（第 3.8.8 节）。
- 构造类型字面量（第 3.8.9 节）。
- 对象字面量（第 4.5 节）。
- 数组字面量（第 4.6 节）。
- 函数表达式（第 4.10 节）和函数声明（6.1）。
- 由类声明创建的构造函数类型（第 8.2.5 节）。
- 由命名空间声明创建的命名空间实例类型（第 10.3 节）。

#### 3.3.1 命名类型引用 (Named Type References)

指向类和接口类型的类型引用（第 3.8.2 节）被归类为对象类型。泛型类和接口类型的引用包含了替换类或接口类型参数的类型参数，从而产生实际的对象类型。

#### 3.3.2 数组类型 (Array Types)

***数组类型***表示具有公共元素类型的 JavaScript 数组。数组类型是从全局命名空间泛型接口 `Array` 创建的命名类型引用，并将元素类型作为类型参数。数组类型字面量（第 3.8.4 节）为创建此类引用提供了简写符号。

`Array` 接口的声明包含一个属性 `length` 和一个针对元素的数字索引签名，以及其他成员：

```typescript



`interface Array<T> {`

```
  length: number;

  [x: number]: T;

  // Other members

}
```

数组字面量（第 4.6 节）可用于创建数组类型的值。例如 `var a: string[] = ["hello", "world"];`

如果一个类型可以赋值给类型 `any[]`（第 3.11.4 节），则该类型被称为***类数组类型***。

## 3.3.3 元组类型 (Tuple Types)

***元组类型***表示单独跟踪元素类型的 JavaScript 数组。元组类型使用元组类型字面量（第 3.8.5 节）编写。元组类型将一组用数字命名的属性与数组类型的成员结合。具体来说，元组类型

`[T0, T1, ..., Tn]`

结合了属性集

```typescript
{
  0: T0;
  1: T1;
  ...
  n: Tn;
}
```

与数组类型的成员结合，数组的元素类型是元组元素的联合类型（第 3.4 节）。

数组字面量（第 4.6 节）可用于创建元组类型的值。例如：
`var t: [number, string] = [3, "three"];`
`var n = t[0]; // Type of n is number`
`var s = t[1]; // Type of s is string`
`var i: number;`
`var x = t[i]; // Type of x is number | string`

通过声明派自 `Array<T>` 并引入数字命名属性的接口可以创建命名的元组类型。例如：
`interface KeyValuePair<K, V> extends Array<V> { [key: K]: V; }`
`var x: KeyValuePair<number, string> = [1, "two"];`

如果一个类型可以赋值给 `Array`，则该类型被称为***类元组类型***。

## 3.3.4 函数类型 (Function Types)

包含一个或多个调用签名的对象类型被称为函数类型。函数类型可以使用函数字面量（第 3.8 节）编写或包含类型引用。

## 3.3.5 构造类型 (Constructor Types)

包含一个或多个构造签名的对象类型被称为构造类型。构造类型可以使用构造字面量（第 3.8 节）编写或包含类型引用。

## 3.3.6 成员 (Members)

每个对象类型由零或多个以下类型的成员组成：

- 属性，定义成员的名称和类型。
- 调用签名，定义可能的参数列表和返回值。
- 构造签名，定义可能的参数列表和返回值。
- 索引签名，定义属性的约束条件。

类型守卫（第 4.24 节）可用于将联合类型缩小为更具体的类型。特别是，类型守卫有助于将联合类型的值收窄为非联合类型的值。

在示例中

`var x: "string" | "number";`
`var test: "boolean";`
`x = "hello"; // Ok`
`x = 42; // Ok`
`x = test; // Error, boolean not assignable`
`x = test ? "5" : "five"; // Ok`
`x = test ? "0" : "false"; // Error, number | boolean not assignable`

可以为 `x` 赋值类型 `string`、`number` 或联合类型 `string | number`，但不能是任何类型。要访问 `x` 中的值，可以使用类型守卫首先将 `x` 的类型收窄为 `string` 或 `number`：

`var n = typeof x === "string" ? x.length : x; // Type of n is number`

出于属性访问和函数调用的目的，联合类型的表面成员（第 3.11.1 节）是存在于其每一个组成类型中的成员，其类型是各个组成类型中相应表面成员类型的联合。以下示例说明了当从对象类型创建联合类型时发生的成员类型合并。

`interface A {`
` a: "string";`
` b: "number";`
`}`
`interface B {`
` a: "number";`
` b: "number";`
` c: "number";`
`}`
`var x: A | B;`
`var a = x.a; // a has type string | number`
`var b = x.b; // b has type number`
`var c = x.c; // Error, no property c in union type`

注意 `x.a` 具有联合类型，因为 `a` 的类型在 `A` 和 `B` 中是不同的，而 `x.b` 仅具有类型 `number`，因为 `b` 在 `A` 和 `B` 中的类型都是 `number`。同样，请注意，没有 `x.c` 属性，因为只有 `A` 有属性 `c`。

当用作上下文类型（第 4.23 节）时，联合类型具有存在于其任何组成类型中的成员，其类型是组成类型中相应成员类型的联合。具体而言，用作上下文类型的联合类型具有第 3.11.1 节中定义的表面成员，不同之处在于特定成员只需要存在于一个或多个组成类型中，而不是所有组成类型。

## 3.5 交集类型

***交集类型***表示同时具有多个类型的值。交集类型 *A* & *B* 的值是一个既是类型 *A* 又是类型 *B* 的值。交集类型使用交叉类型字面量（第 3.8.7 节）编写。

交集类型包含有序的组成类型集合。虽然 *A* & *B* 等同于 *B* & *A* 通常是正确的，但在确定交集类型的调用和构造签名时，组成类型的顺序可能会。

交集类型具有以下子类型关系：

- 如果交集类型 *I* 中的任何类型都是类型 *T* 的子类型，则交集类型 *I* 是类型 *T* 的子类型。
- 如果 *T* 是 *I* 中每个类型的子类型，则类型 *T* 是交集类型 *I* 的子类型。

同样，交集类型具有以下可赋值关系：

- 如果交集类型 *I* 中的任何类型都可以赋值给类型 *T*，则交集类型 *I* 可赋值给类型 *T*。
- 如果 *T* 可以赋值给 *I* 中的每个类型，则类型 *T* 可赋值给交集类型 *I*。

出于属性访问和函数调用的目的，交集类型的表面成员（第 3.11.1 节）是存在于其一个或多个组成类型中的成员，其类型是各个组成类型中相应表面成员类型的交集。以下示例说明了当从对象类型创建交集类型时发生的成员类型合并。

`interface A { a: "number" }`
`interface B { b: "number" }`
`var ab: A & B = { a: "1", b: "1" };`
`var a: A = ab; // A & B assignable to A`
`var b: B = ab; // A & B assignable to B`
`interface X { p: A }`
`interface Y { p: B }`
`var xy: X & Y = { p: ab }; // X & Y has property p of type A & B`
`type F1 = (a: "string", b: "string") => "void";`
`type F2 = (a: "number", b: "number") => "void";`
`var f: F1 & F2 = (a: "string" | "number", b: "string" | "number") => { };`
`f("hello", "world"); // Ok`
`f(1, 2); // Ok`
`f(1", "test"); // Error`

联合类型和交集类型运算符可以应用于类型参数。这种能力可以用于建模合并对象的函数：

`function extend<T, U>(first: T, second: U): T & U {`
`// Extend first with properties of second`
`}`
`var x = extend({ a: "hello" }, { b: "42" });`
`var s = x.a;`
`var n = x.b;`

可以创建除 `null` 或 `undefined` 之外没有其他可能值的交集类型。例如，基本类型的交集如 `string & number` 就属于此类。

## 3.6 类型参数

类型参数表示在泛型类型引用或泛型函数调用中绑定的实际类型。类型参数具有约束，为它们的实际类型参数建立上界。

由于类型参数代表许多不同的类型参数，与与其他类型相比，类型参数具有某些限制。特别是，类型参数不能用作基类或接口。

### 3.6.1 类型参数列表

类、接口、类型别名和函数声明可以可选地包含在 `<` 和 `>` 括号中的类型参数列表。类型参数也允许出现在对象、函数和构造类型字面量的调用签名中。

*TypeParameters:*

`<` *TypeParameterList* `\>`

*TypeParameterList:*

*TypeParameter*

*TypeParameterList* `,` *TypeParameter*

*TypeParameter:*

*BindingIdentifier* *Constraint**opt*

*Constraint:*

`extends` *Type*

类型参数名称必须是唯一的。如果 *TypeParameterList* 中的两个或多个类型参数具有相同的名称，则发生编译错误。

类型参数的作用范围延伸到与类型列表关联的整个声明，类中的静态成员声明除外。

每个类型参数都有一个关联的***约束***，为类型参数建立上界。省略约束或指定 `any` 为约束对应于空对象类型 `{}`。特定类型列表中定义的类型参数不能被引用。

类型参数 *T* 的***基约束***定义如下：

- 如果 *T* 没有声明约束，其基约束为空对象类型 `{}`。
- 如果 *T* 的声明约束是一个类型参数，其基约束为该类型参数的约束。
- 否则，*T* 的基约束为其自身的的声明约束。

在示例中

`interface G<T, U extends Function> {`
` f<V extends U>(x: V): V;`
`}`

`T` 的基约束是空对象类型，`U` 和 `V` 的基约束是 `Function`。

出于确定类型关系（第 3.11 节）的目的，类型参数是其基约束的子类型。同样，在属性访问（第 4.13 节）、`new` 操作（第 4.14 节）和函数调用（第 4.15 节）中，类型参数似乎具有基约束的成员，但没有其他成员。

### 3.6.2 类型参数列表

泛型类型的类型引用（第 3.8.2 节）必须包含在角括号内并用逗号分隔的类型参数列表。同样，泛型函数的调用（第 4.15 节）可以显式包含类型参数列表，而不是依赖类型推断。

*TypeArguments:*

`<` *TypeArgumentList* `\>`

*TypeArgumentList:*

*TypeArgument*

*TypeArgumentList* `,` *TypeArgument*

*TypeArgument:*

*Type*

类型参数与所引泛型类型或函数的类型参数一一对应。类型参数列表需要为每个对应的类型参数指定唯一一个类型参数，且每个类型参数都必须满足其对应的约束。

参数。一旦用类型参数替换为类型参数，如果类型参数可以赋值给约束类型（第 3.11.4 节），则该类型参数满足类型参数约束。

给定定义：

`interface G<T, U> extends Function { }`

形式为 `G<A, B>` 的类型引用对 `A` 没有任何要求，但要求 `B` 必须赋值给 `Function`。

在泛型类型或泛型签名中用类型参数替换类型参数的过程被称为***实例化***（instantiating）泛型类型或签名。如果提供的类型参数不满足其对应类型参数的约束，则泛型类型或签名的实例化可能会失败。

## 3.7 命名类型

类、接口、枚举和类型别名都是***命名类型***，它们通过类声明（第 8.1 节）、接口声明（第 7.1 节）、枚举声明（9.1 节）和类型别名声明（第 3.10 节）引入。类、接口和类型别名可能具有类型参数，此时被称为***泛型类型***。相反，没有类型参数的命名类型被称为***非泛型类型***。

接口声明只引入命名类型，而类声明引入命名类型*以及*创建这些命名类型实现的实例的构造函数。类和接口声明引入的命名类型之间只有细微差异（类不能声明可选成员，而接口不能声明私有或保护成员），并且在大多数语文中是可以互换的。特别是，只有公共成员的类声明所引入的命名类型，其功能与接口声明创建的命名类型完全相同。

命名类型通过***类型引用***（第 3.8.2 节）进行引用，类型引用指定了类型名称，并在适用情况下指定了用于替换该命名类型类型参数的类型参数。

命名类型在技术上并不是类型——只有对命名类型的*引用*才是类型。这种区别在泛型类型中尤为明显：泛型类型是“模板”，通过编写提供类型参数以替换泛型类型类型参数的类型引用，可以从其创建出多个*实际*的类型。这种替换过程被称为***实例化***泛型类型。只有当泛型类型被实例化后，它才表示一个实际的类型。

TypeScript 拥有结构化类型系统，因此，泛型类型的实例化与等效的手写展开是不可区分的。例如，给定定义：

`interface Pair<T1, T2> { first: T1; second: T2; }`

类型引用 `Pair<string, Entity>` 与类型 `{ first: "string"; second: Entity; }` 是不可分的。

### 3.7.1 实例类型

每个类和接口都有关联的实际类型，被称为***实例类型***。对于非泛型类或接口，实例类型仅仅是类或接口的类型引用。对于泛型类或接口，实例类型是泛型类型的实例化，其中每个类型参数都是相应的类型参数。由于实例类型使用了类型参数，因此只能在类型参数的作用范围内使用——即类或接口的声明内部。在类的构造函数和实例成员函数中，`this` 的类型是类的实例类型。

下面的示例说明了实例类型的概念：

```typescript
class G<T> { // 引入类型参数 T
  self: G<T>; // 使用 T 作为类型参数形成实例类型
  f() {
    this.self = this; // self 和 this 都是 G<T> 类型
  }
}
```



## 3.8 指定类型

类型通过引用其关键字或名称，或者通过编写对象类型字面量、数组类型字面量、元组类型字面量、函数类型字面量、构造类型字面量或类型查询来指定。

- *Type:*
- *UnionOrIntersectionOrPrimaryType*
- *FunctionType*
- *ConstructorType*
- *UnionOrIntersectionOrPrimaryType:*
- *UnionType*
- *IntersectionOrPrimaryType*
- *IntersectionOrPrimaryType:*
- *IntersectionType*
- *PrimaryType*
- *PrimaryType:*
- *ParenthesizedType*
- *PredefinedType*
- *TypeReference*
- *ObjectType*
- *ArrayType*
- *TupleType*
- *TypeQuery*
- *ParenthesizedType:* `(` *Type* `)`

当联合类型、交集类型、函数类型或构造类型用数组元素类型时，需要括号；在交集类型中，联合类型、函数类型或构造类型需要括号；在联合类型中，函数类型或构造类型需要括号。例如：

- `("string" | number)[]`
- `((x: "string") => "string") | ((x: number) => number)`
- `(A | B) & (C | D)`

不同形式的类型表示在后续章节中描述。

### 3.8.1 预定义类型

`any`、`number`、`boolean`、`string`、`symbol` 和 `void` 关键字分别引用 `Any` 类型以及 `Number`、`Boolean`、`String`、`Symbol` 和 `Void` 类型。

- *PredefinedType:*
- `any`
- `number`
- `boolean`
- `string`
- `symbol`
- `void`

预定义类型关键字是保留的，不能作为用户定义类型的名称。

### 3.8.2 类型引用

类型引用通过名称引用命名类型或类型参数，并在泛型的情况下提供类型列表。

- *TypeReference:* *TypeName* `[TypeArguments]`opt
- *TypeName:* *IdentifierReference*
- *NamespaceName:* *NamespaceName.* *IdentifierReference*

一个 *TypeReference* 由一个引用命名类型或类型参数的 *TypeName* 组成。对泛型类型的引用必须后跟一个 *TypeArguments* 列表（第 3.6 节）。*TypeName* 是单个标识符，或者是由点分隔的标识符序列。在类型名称中，除了最后一个之外的所有标识符都引用命名空间，最后一个标识符引用一个命名类型。

由单个标识符组成的 *TypeName* 的解析见第 2.4 节。

形式为 *N.X* 的 *TypeName*（其中 *N* 是 *NamespaceName*，*X* 是 *IdentifierReference*）的解析通过首先解析命名空间名称 *N*。如果 *N* 解析成功且导出成员集（第 10.4 节和 11.3.4 节）包含命名类型 *X*，则 *N.X* 引用该成员。否则，*N.X* 是未定义的。

由单个标识符组成的 *NamespaceName* 的解析见第 2.4 节。命名空间声明（第 10.1 节）或导入声明（第 10.3 节、11.3.2 节和 11.3.4 节）中声明的标识符可能被分类为命名空间。

*NamespaceName* 形式为 *N.X*（其中 *N* 是 *NamespaceName*，*X* 是 *IdentifierReference*）的解析通过首先解析命名空间名称 *N* 进行。如果 *N* 解析成功且导出成员集（第 10.4 节和 11.3.4 节）包含命名类型 *X*，则 *N.X* 引用该成员。否则，*N.X* 是未定义的。

泛型类型的引用需要为被引用泛型的每个类型参数指定一个类型参数，且每个类型参数必须赋值给对应类型参数的约束，否则会发生错误。示例如下：

```typescript
interface A { a: "string"; }

interface B extends A { b: "string"; }

interface C extends B { c: "string"; }

interface G<T, U> extends B {

  x: T;

  y: U;

}

var v1: G<A, C>; // 正确

var v2: G<{ a: "string" }, C>; // 正确，等同 G<A, C>

var v3: G<A, A>; // 错误，A 不是 U 的有效参数

var v4: G<G<A, B>, C>; // 正确

var v5: G<any, any>; // 正确

var v6: G<any>; // 错误，参数数量错误

var v7: G; // 错误，无参数
```

类型参数仅仅是 *Type*，本身可以是泛型类型的类型引用，如示例中的 `v4` 所示。

正如第 3.7 节所述，对泛型类型 *G* 的类型引用指定了一个类型，其中 *G* 的所有出现处都被替换为类型引用中提供的实际类型参数。例如，上述 `v1` 的定义等同于：

```typescript
var v1: {

  x: { a: "string"; }

  y: { a: "string"; b: "string"; c: "string"; };
```



### 3.8.3 对象类型字面量

对象类型字面量通过指定静态认为于类型实例中的成员集来定义对象类型。对象类型字面量可以使用接口声明命名，否则它们是匿名的。

- `ObjectType: { TypeBody opt }`
- `TypeBody: TypeMemberList ; opt | TypeMemberList , opt`
- `TypeMemberList: TypeMember | TypeMemberList ; TypeMember | TypeMemberList , TypeMember`
- `TypeMember: PropertySignature | CallSignature | ConstructSignature | IndexSignature | MethodSignature`

对象类型字面量的成员被指定为属性、调用、构造、索引和方法签名的组合。对象类型成员在 3.9 节中描述。

### 3.8.4 数组类型字面量

数组类型字面量写为元素类型后跟一对闭方括号。

`ArrayType:`

`PrimaryType []`

数组类型字面量引用了具有给定元素类型的数组类型（3.3.2 节）。数组类型字面量仅是对全局命名空间中泛型接口类型 `Array` 引用的简写符号，并将元素类型作为类型参数。

当联合类型、交叉类型、函数类型或构造类型用作数组元素类型时，必须括在括号内。例如：

`(string | number)[]`

`(() => string)[]`

或者，数组类型可以使用 `Array<T>` 记法编写。例如，上述类型等同于：

`Array<string | number>`

`Array<() => string>`

### 3.8.5 元组类型字面量

元组类型字面量写为一组由逗号分隔的元素类型，并括在方括号中。

`TupleType:`

`[TupleElementTypes]`

`TupleElementTypes:`

`TupleElementType`

`TupleElementTypes, TupleElementType`

`TupleElementType:`

`Type`

元组类型字面量引用了一个元组类型（3.3.3 节）。

### 3.8.6 联合类型字面量

联合类型字面量写为一组由竖线分隔的类型序列。

`UnionType:`

`UnionOrIntersectionOrPrimaryType | IntersectionOrPrimaryType`

联合类型字面量引用了一个联合类型（3.4 节）。

### 3.8.7 交叉类型字面量

交叉类型字面量写为一组由安培符号分隔的类型序列。

`IntersectionType:`

`IntersectionOrPrimaryType & PrimaryType`

交叉类型字面量引用了一个交叉类型（3.5 节）。

### 3.8.8 函数类型字面量

函数类型字面量指定了调用签名的类型参数、普通参数和返回类型。

`FunctionType:`

`TypeParameters opt ( ParameterList opt ) => Type`

函数类型字面量是包含单个调用签名的对象类型的简写。具体来说，形式为：

`<T1, T2, ...>(p1, p2, ...) => R`

的函数类型字面量等同于对象类型字面量：

`{ <T1, T2, ...>(p1, p2, ...): R }`

注意，具有多个调用或构造签名的函数类型不能写成函数类型字面量，而必须写成对象类型字面量。

### 3.8.9 构造类型字面量

构造类型字面量指定了构造签名的类型参数、普通参数和返回类型。

`ConstructorType:`

`new TypeParameters opt ( ParameterList opt ) => Type`

构造类型字面量是包含单个构造签名的对象类型的简写。具体来说，形式为：

`new <T1, T2, ...>(p1, p2, ...) => R`

的等同于对象类型字面量：

`{ new <T1, T2, ...>(p1, p2, ...): R }`

注意，具有多个构造签名的构造类型不能写成构造类型字面量，而必须写成对象类型字面量。

### 3.8.10 类型查询

类型查询获取表达式的类型。

`TypeQuery:`

`typeof TypeQueryExpression`

`TypeQueryExpression:`

`IdentifierReference`

`TypeQueryExpression.IdentifierName`

类型查询由关键字 `typeof` 后跟一个表达式组成。该表达式限于单个标识符或由点分隔的标识符序列。该表达式作为标识符表达式（4.3 节）或属性访问表达式（4.13 节）处理，其拓宽类型（3.12 节）成为结果。与其他静态类型构造类似，类型查询会在生成的 JavaScript 代码中擦除，不增加运行时开销。

类型查询用于捕获由各种构造（如对象字面量、函数声明和命名空间声明）生成的匿名类型。例如：

```typescript
var a = { x: 10, y: 20 };
var b: typeof a;
```

上述，`b` 被赋予了与 `a` 相同的类型，即 `{ x: number; y: number; }`。

如果声明包含类型注解通过类型查询的循环路径，或包含类型查询的类型引用引用被声明的实体，则生成的类型是 `Any` 类型。例如，以下所有变量都被赋予了 `Any` 类型：

```typescript
var c = typeof c;
var d = typeof d;
var e = typeof e;
var f = typeof f;
```

然而，如果一个签名包含至少一个表示一个构造。（等一下，OCR 文本在这里似乎杂乱了，让我们重新对齐流程）

类型查询用于捕获由各种构造（如对象字面量、函数声明和命名空间声明）生成的匿名类型。例如：

```typescript
var a = { x: 10, y: 20 };
var b: typeof a;
```

上述，`b` 被赋予了与 `a` 相同的类型，即 `{ x: number; y: number; }`。

如果声明包含类型注解通过类型查询的循环路径，或包含类型查询的类型引用引用被声明的实体，则生成的类型是 `Any` 类型。例如，以下所有变量都被赋予了 `Any` 类型：

```typescript
var c = typeof c;
var d = typeof d;
var e = typeof e;
var f = typeof f;
```

然而，如果一个签名包含至少一个表示一个构造。（注：由于 51—53 页的 OCR 文本存在混乱，将根据提供的片段进行逻辑还原）

### 3.9.1 类型参数

调用签名中的类型参数（3.6.1 节）提供了一种表达参数和返回类型之间关系的机制。例如，一个签名可能会引入一个类型参数并将其同时用于参数类型和返回类型，描述一个返回其参数值的函数。类型参数可以在参数类型和返回类型注解中引用，但不能在引入它们的调用签名的约束中引用。

类型参数的类型参数（3.6.2 节）可以在调用操作中显式指定，在可能的情况下从调用普通参数的类型中推断（4.15.2 节）。泛型调用签名的特定类型参数实例化是将每个类型参数替换为相应的类型参数后形成的调用签名。

下面是一些带有类型参数的调用签名示例。

接受任意类型参数并返回相同类型值的函数：

`<T>(x: T): T`

接受两个相同类型值并返回该类型数组的函数：

`<T>(x: T, y: T): T[]`

接受两个不同类型参数并返回具有属性 `x` 和 `y` 的对象的函数：

`<T, U>(x: T, y: U): { x: T; y: U; }`

接受一种类型的数组和一个函数参数，返回另一种类型的数组，其中函数参数接受第一个数组元素类型的值并返回第二个数组元素类型的值：

`<T, U>(a: T[], f: (x: T) => U): U[]`

### 3.9.2.2 参数列表

签名的参数列表由零个或多个必需参数组成，后跟零个或多个可选参数，最后跟一个可选的剩余参数。

`ParameterList:`

`RequiredParameterList`

`OptionalParameterList`

`RestParameter`

`RequiredParameterList, OptionalParameterList`

`RequiredParameterList, RestParameter`

`OptionalParameterList, RestParameter`

`RequiredParameterList, OptionalParameterList, RestParameter`

`RequiredParameterList:`

`RequiredParameter`

`RequiredParameterList, RequiredParameter`

`RequiredParameter:`

`AccessibilityModifier opt BindingIdentifierOrPattern TypeAnnotation opt`

`BindingIdentifier : StringLiteral`

`AccessibilityModifier:`

`public`

`private`

`protected`

`BindingIdentifierOrPattern:`

`BindingIdentifier`

`BindingPattern`

`OptionalParameterList:`

`OptionalParameter`

`OptionalParameterList, OptionalParameter`

`OptionalParameter:`

`AccessibilityModifier opt BindingIdentifierOrPattern ? TypeAnnotation opt`

`AccessibilityModifier opt BindingIdentifierOrPattern TypeAnnotation opt Initializer`

`BindingIdentifier ? : StringLiteral`

`RestParameter:`

`... BindingIdentifier TypeAnnotation opt`

参数声明可以指定一个标识符或一个绑定模式（5.2.2）。在参数列表中，参数声明和绑定模式中指定的标识符在相应参数列表中必须是唯一的。

签名中参数的类型按如下方式确定：

- 如果声明包含类型注解，则该参数为该类型。
- 否则，如果声明包含初始化表达式（这仅在参数列表与函数体结合出现时才允许），则参数类型为初始化表达式类型的宽化形式（第 3.12 节）。
- 否则，如果声明指定了绑定模式，则参数类型为该绑定模式的推断类型（第 5.2.3 节）。
- 否则，如果该参数是剩余参数，则参数类型为 `any[]`。
- 否则，参数类型为 `any`。

参数允许包含 `public`、`private` 或 `protected` 修饰符，仅当它出现在 `ConstructorImplementation`（第 8.3.1 节）的参数列表中，且它没有指定 `BindingPattern`。

剩余参数的类型注解必须表示数组类型。

当参数类型注解指定字符串字面量类型时，包含它的签名是一个特化签名（第 3.9.2.4 节）。特化签名不允许与函数体结合使用，即 `FunctionExpression`、`FunctionImplementation`、`MemberFunctionImplementation` 和 `ConstructorImplementation` 产生式不允许带有字符串字面量类型的参数。

可以通过在其名称或绑定模式后加问号（`?`）或包含初始化器将参数标记为可选。初始化器（包括绑定属性或元素初始化器）仅在参数列表与函数体结合时才允许，即仅出现在 `FunctionExpression`、`FunctionImplementation`、`MemberFunctionImplementation` 或 `ConstructorImplementation` 产生式中。

*TODO: 更新以反映绑定参数在实现签名中不能是可选的*

### 3.9.2.3 返回类型

如果存在，调用签名的返回类型注解指定了调用操作计算并返回的值的类型。`void` 返回类型用于表示函数没有返回值。当没有返回类型注解的调用签名出现在没有函数体的上下文中时，返回类型假设为 `Any` 类型。

当没有返回类型注解的调用签名出现在具有函数体的上下文中（具体而言，是函数实现、成员函数实现或成员访问器声明）时，返回类型根据第 6.3 节从函数体中推断。

### 3.9.2.4 特化签名

当参数类型注解指定字符串字面量类型时（第 3.2.9 节），包含它的签名被认为是特化签名。特化签名用于表示某些模式，即某些参数的特定字符串值会导致其他参数的类型或函数结果变得进一步特化。例如，以下声明：

```typescript
interface Document {
  createElement(tagName: "div"): HTMLDivElement;
  createElement(tagName: "span"): HTMLSpanElement;
  createElement(tagName: "canvas"): HTMLCanvasElement;
  createElement(tagName: "string"): HTMLElement;
}
```

表示使用字符串字面量 `"div"`、`"span"` 和 `"canvas"` 调用 `createElement`，分别返回类型为 `HTMLDivElement`、`HTMLSpanElement` 和 `HTMLCanvasElement` 的值，而使用所有其他字符串表达式返回类型为 `HTMLElement`。

在编写像上面的重载声明时，将非特化签名列在最后是重要的。这是因为重载解析（第 4.15.1 节）按声明顺序处理候选对象并选择第一个匹配的。

对象中的每个特化调用或构造签名必须至少可以赋值给非特化签名（其中调用签名 `A` 可赋值给对象类型 `B`）。例如，上述示例中的 `createElement` 属性的类型包含特化签名。

### 3.9.3 构造签名

构造签名定义了与关联到 `new` 操作符（第 4.14 节）的包含类型实例关联的参数列表和返回类型。类型可以通过定义具有不同参数列表的多个构造签名来重载 `new`。

`ConstructSignature:`

`new TypeParameters opt ( ParameterList opt ) TypeAnnotation opt`

构造签名的类型参数、参数列表和返回类型遵循与调用签名相同的规则。包含构造签名的类型被称为构造函数类型。

### 3.9.4 索引签名

索引签名定义了包含类型中属性的类型约束。索引签名有两种：

`IndexSignature:`

`[BindingIdentifier : string] TypeAnnotation`

`[BindingIdentifier : number] TypeAnnotation`

- **字符串索引签名**使用索引类型 `string` 定义包含类型中所有属性的类型约束。具体而言，在字符串索引为 `T` 的类型中，所有属性必须赋值为 `T`。
- **数字索引签名**使用索引类型 `number` 定义包含类型中所有数字命名属性的类型约束。具体而言，在数字索引为 `T` 的类型中，所有数字命名属性必须赋值为 `T`。

**数字命名属性**是指名称为有效数字字面量的属性。具体而言，属性 `N` 的 `ToString(ToNumber(N))` 等于 `N`，其中 `ToString` 和 `ToNumber` 是 ECMAScript 中定义的抽象操作。

对象类型最多包含一个字符串索引签名和一个数字索引签名。索引签名影响对包含类型应用括号表示访问时生成的类型，如第 4.13 节所述。

### 3.9.5 方法签名

方法签名是声明函数类型属性的简写。

`MethodSignature:`

`PropertyName ? opt CallSignature`

如果 `PropertyName` 是计算属性名（2.2.3），它必须指定一个已知的符号。如果 `PropertyName` 后面跟着问号，则该属性是可选的。否则，该属性是强制的。只有对象字面量和接口可以声明可选属性。

形式为：

`f<T1, T2, ...>(p1, p2, ...): R`

的方法签名等于属性声明：

`f: { <T1, T2, ...>(p1, p2, ...): R }`

字面量可以通过声明名称相同但参数列表不同的方法签名来重载方法。重载必须全为强制的（省略问号）或全为可选（包含问号）。一组重载方法签名对应于单个属性的声明，该类型由等效的调用签名集合组成。具体而言：

```typescript
f<T1, T2, ...>(p1, p2, ...): R;

f<U1, U2, ...>(q1, q2, ...): S;
```



## 51

等于：

```typescript
f: {
  <T1, T2, ...>(p1, p2, ...): R;
  <U1, U2, ...>(q1, q2, ...): S;
  ...
};
```

在接接对象类型示例中：

```typescript
{
  func1(x: number): number; // 方法签名
  func2: (x: number) => number; // 函数类型字面量
  func3: { (x: number): number }; // 对象类型字面量
}
```

属性`func1`、`func2`和`func3`都是相同类型，即一个包含单个调用签名的对象类型，该签名接收一个数字并返回数字。同样，在对象类型：

```typescript
{
  func4(x: number): number;
  func4(s: string): string;
  func5: {
    (x: number): number;
    (s: string): string;
  };
}
```

属性`func4`和`func5`是相同类型，即一个包含两个调用签名的对象类型，分别接收并返回数字和字符串。

## 3.10 类型别名

类型别名声明在包含的声明空间中引入了一个***类型别名（type alias）***。

*TypeAliasDeclaration:*

```typescript
type BindingIdentifier TypeParameters_opt = Type;
```

类型别名作为类型别名声明中指定类型的别名。与接口声明不同（接口总是引入一个命名的对象类型），类型别名声明可以为任何类型的类型引入名称，包括原始类型、联合类型和交叉类型。

类型别名可以可选带有类型参数（见 3.6.1 节），作为在类型引用引用别名时提供的实际类型的占位符。带有类型参数的类型别称为***泛型类型别名（generic type alias）***。泛型类型别名声明的类型参数在作用范围内，并可以在别名的*Type*中引用。

类型别名通过类型引用（3.8.2）进行引用。泛型类型别名的类型引用会产生带有给定类型参数的别名类型的实例化。对非泛型类型别名的引用的效果与直接编写别名类型完全相同，而对泛型类型别名的引用的效果与编写该别名类型的实例化完全相同。

类型别名的*BindingIdentifier*不可以是预定义的类型名称之一（见 3.8.1 节）。

如果类型别名中指定的类型依赖于该类型别名，这是一个错误。类型具有以下依赖关系：

- 类型别名*直接依赖于*它所别名的类型。
- 类型引用*直接依赖于*被引用的类型以及每个类型参数（如果有）。
- 联合类型或交叉类型*直接依赖于*每个组成类型。
- 数组类型*直接依赖于*它的元素类型。
- 元组类型*直接依赖于*它的每个元素类型。
- 类型查询*直接依赖于*被引用实体的类型。

根据此定义，类型所依赖的完整类型集是*直接依赖于*关系的传递闭包。注意，对象类型字面量、函数类型字面量和构造类型不依赖于其内部的类型，因此允许通过类型别名循环引用自身。

类型别名声明的某些示例：

```typescript
type StringOrNumber = string | number;
type Text = string | { text: string };
type NameLookup = Dictionary<string, Person>;
type ObjectStatics = typeof Object;
type Callback<T> = (data: T) => void;
type Pair<T> = [T, T];
type Coordinates = Pair<number>;
type Tree<T> = T | { left: Tree<T>, right: Tree<T> };
```

接口类型与对象字面量的类型别名有许多相似之处，但由于接口类型提供了更多功能，因此通常比类型别名更优。例如，接口类型：

```typescript
interface Point {
  x: number;
  y: number;
}
```

可以写为类型别名：

```typescript
type Point = {
  x: number;
  y: number;
};
```

然而，这将丢失以下能力：

- 接口可以在`extends`或`implements`子句中命名，但对象类型字面量的类型别名不能这样做。
- 接口可以有多个声明，但对象类型字面量的类型别名不能这样做。

## 3.11 类型关系

TypeScript 中的类型具有身份、子类型、父类型和赋值兼容性关系，定义见下文章节。

### 3.11.1 显式成员（Apparent Members）

类型的***显式成员（apparent members）***是在子类型、父类型和赋值兼容性关系中观察到的成员，以及属性访问类型检查（见 4.13 节）、`new`操作（见 4.14 节）和函数调用（见 4.15 节）中的成员。类型的显式成员按如下确定：

- 原始类型`Number`、`Boolean`和`String`的显式成员分别是全局接口类型`Number`、`Boolean`和`String`的成员。
- 举举类型的显式成员是全局接口类型`Number`的显式成员。
- 类型参数的显式成员是该类型参数约束（见 3.6.1 节）的显式成员。
- 对象类型*T*的显式成员是以下内容的组合：
  - *T*声明的和/或继承的成员。
  - 全局接口类型`Object`的未被*T*中同名属性隐藏的属性。
  - 如果*T*有一个或多个调用签名或构造签名，则全局接口类型`Function`的未被*T*中同名属性隐藏的属性。
- 联合类型*U*的显式成员按如下确定：
  - 当*U*的所有组成类型都有一个名为*N*的显式属性时，*U*有一个名为*N*的显式属性，其类型为相应属性类型的联合类型。
  - 当*U*的所有组成类型都有一个具有参数列表*P*的显式调用签名时，*U*有一个具有参数列表*P*的显式调用签名，其返回类型为相应返回类型的联合。调用签名顺序与第一个组成类型相同。
  - 当*U*的所有组成类型都有一个具有参数列表*P*的显式构造签名时，*U*有一个具有参数列表*P*的显式构造签名，其返回类型为相应返回类型的联合。构造签名顺序与第一个组成类型相同。
  - 当*U*的所有组成类型都有显式字符串索引签名时，*U*有显式字符串索引签名，其类型为相应索引类型的联合类型。
  - 当*U*的所有组成类型都有显式数字索引签名时，*U*有显式数字索引签名，其类型为相应索引类型的联合类型。
- 交叉类型*I*的显式成员按如下确定：
  - 当*I*的所有组成类型都有一个名为*N*的显式属性时，*I*有一个名为*N*的显式属性，其类型为相应类型的交叉类型。
  - 当*I*的所有组成类型都有一个具有参数列表*P*的显式调用签名时，*I*有一个具有参数列表*P*的显式调用签名，其返回类型为相应返回类型的联合。调用签名顺序与第一个组成类型相同。
  - 当*I*的所有组成类型都有一个具有参数列表*P*的显式构造签名时，*I*有一个具有参数列表*P*的显式构造签名，其返回类型为相应返回类型的联合。构造签名顺序与第一个组成类型相同。
  - 当*I*的所有组成类型都有显式字符串索引签名时，*I*有显式字符串索引签名，其类型为相应索引类型的交叉类型。
  - 当*I*的所有组成类型都有显式数字索引签名时，*I*有显式数字索引签名，其类型为相应索引类型的交叉类型。

如果一个类型不是上述任何一种，则被认为没有显式成员。实际上，一个类型的显式成员使其成为`Object`或`Function`接口的子类型，除非该类型定义的与`Object`或`Function`接口不兼容的成员——例如，当该类型定义了与`Object`或`Function`接口同名的属性，但其类型不是该接口中属性的子类型时。

### 3.11.2 类型与成员标识

当满足以下条件时，两个类型被认为是***相同的***（identical）：

- 它们都是`Any`类型；
- 它们是相同的原始类型；
- 它们是相同的类型参数；
- 它们是具有相同组成类型的联合类型（union types）；
- 它们是具有相同组成类型的交集类型（intersection types）；
- 它们是具有相同成员的对象类型。

当满足以下条件时，两个成员被认为是相同的：

- 它们是具有相同名称、可选性和公共属性；
- 它们是源自同一声明且具有相同的私有或保护属性；
- 它们是相同的调用签名（call signatures）；
- 它们是相同的构造签名（construct signatures）；
- 它们是相同种类且相同类型的索引签名（index signatures）。

两个调用签名或构造签名在满足以下条件时被认为是相同的：它们具有相同数量的类型参数且具有相同的类型参数约束，并且在用类型`Any`替换由签名引入的类型参数后，具有相同数量、相同种类（必需、可选或剩余）和相同类型的参数，以及相同的返回类型。

请注意，除原始类型和具有私有或保护成员的类外，决定标识性的是结构而非命名。还需要注意，在确定签名的标识性时，参数名称是不重要的。

私有和保护属性只有在源自同一声明且具有相同类型时才匹配。如果两个不同类型是对同一个泛型类的独立参数化引用，它们可能包含源自同一声明的属性。在示例中：

```typescript
class C<T> {
  private x: T;
}

interface X {
  f(): string;
}

interface Y {
  f(): string;
}

var a: C<X>;
var b: C<Y>;
```

变量`a`和`b`是相同的类型，因为对`C`的两个类型引用创建了具有源自同一声明的私有成员`x`，并且在替换类型参数`X`和`Y`后，两个私有成员`x`具有相同组成类型的类型。

### 3.11.3 子类型与父类型

如果*S*是类型*T*的***子类型***（subtype），且*T*是*S*的***父类型***（supertype），则*S*相对于*T*没有多余属性（3.11.5）且满足以下任一：

- *S*和*T*是相同类型。
- *T*是`Any`类型。
- *S*是`Undefined`类型。
- *S*是`Null`类型且*T*不是`Undefined`类型。
- *S*是枚举类型且*T*是原始类型`Number`。
- *S*是字符串字面量类型且*T*是原始类型`String`。
- *S*是联合类型，且*S*的每个组成类型都是*T*的子类型。
- *S*是交集类型，且*S*的至少一个组成类型是*T*的子类型。
- *T*是联合类型，且*S*是*T*的至少一个组成类型的子类型。
- *T*是交集类型，且*S*是*T*的每个组成类型的子类型。
- *S*是一个类型参数，且*S*的约束是*T*的子类型。
- *S*是对象类型、交集类型、枚举类型或`Number`、`Boolean`或`String`原始类型，*T*是对象类型，且对于*T*中的每个成员*M*，满足以下任一：
  - *M*是属性且*S*具有一个明显的属性*N*，其中：
    - *M*和*N*具有相同名称；
    - *N*的类型是*M*类型的子类型；
    - 如果*M*是必需属性，*N*也是必需属性；并且
    - *M*和*N*都是公共的；*M*和*N*都是私有的且源自同一声明；*M*和*N*都是保护的且源自同一声明；或*M*是保护的且*N*声明在*M*所在类的派生类中。
  - *M*是非特化的调用或构造签名，且*S*具有一个明显的调用或构造签名*N*，当*M*和*N*使用类型`Any`作为*M*和*N*声明的所有类型参数（如果有）的类型参数实例化时：
    - 签名具有相同种类（调用或构造）；
    - *M*具有剩余参数，或*N*中非可选参数的数量小于等于*M*中的参数总数；
    - 对于两个签名都存在的参数位置，*N*中的每个参数类型都是*M*中对应参数类型的子类型或父类型；并且
    - *M*的返回类型为`Void`，或*N*的返回类型是*M*返回类型的子类型。
  - *M*是类型*U*的索引签名，且*U*是`Any`类型或*S*具有类型*U*的明显的索引签名。

在比较调用或构造签名时，参数名称是不重要的。请注意，除原始类型和具有私有或保护成员的类外，决定标识性的是结构而非命名。

### 3.11.4 赋值兼容性

在某些情况下，类型被认为是赋值兼容的，例如赋值和函数调用以及参数类型。如果*S*可以赋值给*T*，当*S*相对于*T*没有多余属性（3.11.5）且满足以下任一：

- *S*和*T*是相同类型。
- *T*是`Any`类型。
- *S*是`Undefined`类型。
- *S*是`Null`类型且*T*不是`Undefined`类型。
- *S*是枚举类型且*T*是原始类型`Number`。
- *S*是字符串字面量类型且*T*是原始类型`String`。
- *S*是联合类型，且*S*的每个组成类型都是*T*的子类型。
- *S*是交集类型，且*S*的至少一个组成类型是*T*的子类型。
- *T*是联合类型，且*S*是*T*的至少一个组成类型的子类型。
- *T*是交集类型，且*S*是*T*的每个组成类型的子类型。
- *S*是一个类型参数，且*S*的约束是*T*的子类型。
- *S*是对象类型、交集类型、枚举类型或`Number`、`Boolean`或`String`原始类型，*T*是对象类型，且对于*T*中的每个成员*M*，满足以下任一：
  - *M*是属性且*S*具有一个明显的属性*N*，其中：
    - *M*和*N*具有相同名称；
    - *N*的类型是*M*类型的子类型；
    - 如果*M*是必需属性，*N*也是必需属性；并且
    - *M*和*N*都是公共的；*M*和*N*都是私有的且源自同一声明；*M*和*N*都是保护的且源自同一声明；或*M*是保护的且*N*声明在*M*所在类的派生类中。
  - *M*是可选属性且*S*没有与*M*名称相同的明显的属性。
  - *M*是非特化的调用或构造签名，且*S*具有一个明显的调用或构造签名*N*，当*M*和*N*使用类型`Any`作为*M*和*N*声明的所有类型参数（如果有）的类型参数实例化时：
    - 签名具有相同种类（调用或构造）；
    - *M*具有剩余参数，或*N*中非可选参数的数量小于等于*M*中的参数总数；
    - 对于两个签名都存在的参数位置，*N*中的每个参数类型都是可赋值给*M*中对应参数类型或可从该类型赋值。

    *M*的结果类型为`Void`，或者*N*的结果类型可以赋值给*M*的结果类型。

  - *M*是类型为*U*的字符串索引签名，且*S*拥有一个明显的字符串索引签名，其类型可以赋值给*U*。
  - *M*是类型为*U*的数字索引签名，且*S*拥有一个明显的字符串或数字索引签名，其类型可以赋值给*U*。

在比较调用签名或构造签名时，参数名称会被忽略，且剩余参数对应于剩余参数元素类型中可选参数的无界扩展。

注意，专门的调用签名和构造签名（第 3.9.2.4 节）在确定赋值兼容性时是不重要的。

赋值兼容性与子类型规则的差异仅在于：

- `Any`类型可以赋值给所有类型，但不是所有类型的子类型；
- 原生类型`Number`可以赋值给所有枚举类型，但不是所有枚举类型的子类型；
- 不包含特定属性的对象类型可以赋值给该属性为可选的对象类型。

赋值兼容性规则意味着，在赋值值或传递参数时，可选属性必须要么存在且类型兼容，要么完全不存在。例如：

```typescript
function foo(x: { id: number; name?: string }) {}
foo({ id: "1234" }); // OK
foo({ id: "1234", name: "hello" }); // OK
foo({ id: "1234", name: false }); // 错误，name 类型错误
foo({ name: "hello" }); // 错误，需要 id 但缺失
```

### 3.11.5 多余属性

子类型关系和赋值兼容性关系要求源类型相对于其目标类型没有多余属性。此检查的目的是检测对象字面量中的多余属性或写错误的属性。

如果满足以下条件，则认为源类型*S*对于目标类型*T*有多余属性：

- *S*是下文定义的新的对象字面量类型；并且
- *S*具有一个或多个在*T*中不预期的属性。

如果满足以下任一条件，则认为属性*P*在类型*T*中是预期的：

- *T*不是对象、联合类型或交叉类型。
- *T*是对象类型且：
  - *T*具有一个与*P*相同的属性；
  - *T*具有字符串或数字索引签名；
  - *T*没有属性；或
  - *T*是全局类型`Object`。
- *T*是联合类型或交叉类型，且*P*在*T*的至少一个组成类型中是预期的。

对于对象字面量推断出的类型（如第 4.5 节所述）被认为是***新的对象字面量类型***。当对象字面量类型被拓宽（3.12）或作为类型断言中的表达式类型（4.16）时，这种新颖性就会消失。

考虑以下示例：

```typescript
```



```typescript
interface CompilerOptions {
  strict?: boolean;
  sourcePath?: string;
  targetPath?: string;
}

var options: CompilerOptions = {
  strict: true,
  sourcepath: "./src", // 错误，多余或写错误的属性
  targetpath: "./bin" // 错误，多余或写错误的属性
};
```

`CompilerOptions` 类型仅包含可选属性，因此如果没有多余属性检查，任何对象字面量都可以赋值给 `options` 变量（因为写错误的属性将仅视为另一个名称的多余属性）。

在预期存在多余属性的情况下，可以为目标类型添加索引签名作为意图的指示：

```typescript
interface InputElement {
  name: string;
  visible?: boolean;
  [x: string]: any; // 允许任何类型的额外属性
}

var address: InputElement = {
  name: "Address",
  visible: true,
  help: "Enter address here", // 因为索引签名而允许
  shortcut: "Alt-A" // 因为索引签名而允许
};
```

### 3.11.6 上文签名实例化

在函数调用类型参数推断（第 4.15.2 节）期间，在某些情况下，需要在非泛型调用签名的文中实例化参数表达式的泛型调用签名，以便进行进一步的推断。泛型调用签名 `A` 以如下方式**在非泛型调用签名 `B` 的文中实例化**：

- 使用 3.11.7 中描述的过程，从 `B` 中的每个参数类型推断出 `A` 中对应参数位置的参数类型（只要这些参数位置是两个签名中都存在的），在其中，剩余参数对应于剩余参数元素类型中可选参数的无界扩展。
- 每个类型参数的推断类型是针对该类型参数所做的所有推断的联合类型。然而，如果联合类型不满足类型参数的约束，则推断类型应为约束本身。

### 3.11.7 类型推断

在某些文中，针对给定的类型参数集的推断是*从*类型 `S`（这些类型参数在 `S` 中未出现）*到*另一个类型 `T`（这些类型参数在 `T` 中出现）。推断由每个类型参数的一组候选类型组成。推断过程关联 `S` 和 `T` 以收集尽可能多的推断：

- 如果 `T` 是进行推断的类型参数之一，则将 `S` 添加到该类型参数的推断集中。
- 否则，如果 `T` 是其中一个类型参数，且 `S` 和 `T` 是元组类型，则从 `S` 到 `T` 的每个元素进行推断。
- 否则，如果 `T` 是联合类型或交叉类型：
  - 首先，如果 `T` 是进行推断的类型参数之一，则将 `S` 添加到该类型参数的推断集中。
  - 其次，如果 `T` 是其中一个类型参数，且 `S` 和 `T` 具有相同的元素，则从 `S` 到 `T` 的每个元素进行推断。
  - 否则，如果 `T` 是对象类型：
    - 首先，如果 `T` 是进行推断的类型参数之一，则将 `S` 添加到该类型参数的推断集中。
    - 其次，如果 `T` 是其中一个类型参数，且 `S` 和 `T` 具有相同的属性，则从 `S` 到 `T` 的每个属性进行推断。
    - 再次，如果 `T` 具有字符串或数字索引签名，则从 `S` 到 `T` 进行推断。
    - 再次，如果 `T` 没有属性，且 `S` 和 `T` 具有相同的属性，则从 `S` 到 `T` 进行推断。
    - 最后，如果 `T` 是全局类型 `Object`，则从 `S` 到 `T` 进行推断。
  - 否则，如果 `T` 是联合类型或交叉类型，且 `S` 在 `T` 的至少一个组成类型中是预期的，则进行推断。

*（注：原文此处关于推断的描述存在大量重复和复杂的嵌套，翻译已尽量还原逻辑结构进行）*

62

```typescript
interface List<T> {
  data: T;
  next: List<T>;
  owner: List<List<T>>;
}
```



`'List<T>'` 有一个类型为 `List<List<T>>` 的成员 `'owner'`，该成员有一个类型为 `List<List<List<T>>>` 的成员 `'owner'`，该成员又有一个类型为 `List<List<List<List<T>>>>` 的成员 `'owner'`，以此类推。由于类型关系是结构化决定的，可能需要完整地探索组成类型，为了确定涉及无限扩展泛型类型的类型关系，编译器可能需要在某处终止递归，并假设进一步的探索将不会改变结果。

## 3.12 拓宽类型 (Widened Types)

在几种情况下，TypeScript 会从上下文中推断类型，从而减少了程序员显式指定显而易见的类型的需求。例如：

`var name = "Steve";`

推断出 `name` 的类型为 `String` 原始类型，因为这是用于初始化它的值的类型。当从表达式推断变量、属性或函数结果的类型时，使用源类型的***拓宽***形式作为目标的推断类型。一个类型的拓宽形式是将所有 `Null` 和 `Undefined` 类型的出现都替换为类型 `any` 的类型。

下面的示例展示了拓宽类型以产生推断变量类型的结果。

```
var a = null; // var a: any
var b = undefined; // var b: any
var c = { x: 0, y: null }; // var c: { x: number, y: any }
var d = [null, undefined]; // var d: any[]
```

## 4 表达式

本章描述了 TypeScript 如何为 JavaScript 表达式提供类型推断和类型检查。TypeScript 的类型分析完全在编译时进行，不会为表达式求值增加运行时开销。

TypeScript 的类型规则为每个表达式构造体定义了类型。例如，字面量 `123` 的类型是 `Number` 原始类型，对象字面量 `{ a: 10, b: "hello" }` 的类型是 `{ a: number; b: string; }`。本章的章节详细描述了这些规则。

除了类型推断和类型检查外，TypeScript 还为 JavaScript 表达式增强了以下构造：

- 函数表达式和箭头函数中的可选参数和返回类型注解。
- 函数调用中的类型参数。
- 类型断言。

除非后续章节中另有说明，否则 TypeScript 表达式及其由它们生成的 JavaScript 表达式是相同的。

### 4.1 值与引用

表达式被分类为***值 (values)***或***引用 (references)***。引用是被允许作为赋值目标的表达式子集。具体来说，引用是标识符（第 4.3 节）、括号（第 4.8 节）和属性访问（第 4.13 节）的组合。本章描述的所有其他表达式构造都被分类为值。

### 4.2 this 关键字

表达式中`this`的类型取决于引用发生的位置：

- 在构造函数、实例成员函数、实例成员访问器或实例成员变量初始化中，`this` 是所属类的类实例类型。
- 在静态成员函数或静态成员访问器中，`this` 的类型是所属类的构造函数类型。
- 在函数声明或函数表达式中，`this` 的类型为 `Any`。
- 在全局命名空间中，`this` 的类型为 `Any`。

在所有其他上下文中，引用 `this` 是编译错误。

注意，箭头函数（第 4.11 节）没有 `this` 参数，而是保留其闭包环境的 `this`。

### 4.3 标识符

当表达式是*标识符引用 (IdentifierReference)* 时，该表达式指向最嵌套的命名空间、类、枚举、函数、变量或参数，其作用域（第 2.4 节）包含了引用的位置。此类表达式的类型与所引用实体相关的类型：

- 对于命名空间，与命名空间实例相关的对象类型。
- 对于类，与构造函数对象相关的构造函数类型。
- 对于枚举，与枚举对象相关的对象类型。
- 对于函数，与函数对象相关的函数类型。
- 对于变量，变量的类型。
- 对于参数，参数的类型。

引用变量或参数的标识符表达式被分类为引用。引用任何其他类型实体的标识符表达式被分类为值（因此不能作为赋值目标）。

### 4.4 字面量

字面量的类型如下：

- `null` 字面量的类型是 `Null` 原始类型。
- `true` 和 `false` 字面量的类型是 `Boolean` 原始类型。
- 数字字面量的类型是 `Number` 原始类型。
- 字符串字面量的类型是 `String` 原始类型。
- 正则表达式字面量的类型是全局接口类型 `RegExp`。

### 4.5 对象字面量

对象字面量扩展为支持方法以及 `get` 和 `set` 访问器中的类型注解。

*PropertyDefinition:* *( 修改 )*

*IdentifierReference*

*CoverInitializedName*

*PropertyName* `:` *AssignmentExpression*
*PropertyName* *CallSignature* `{` *FunctionBody* `}`
*GetAccessor*
*SetAccessor*

*GetAccessor:*
`get` *PropertyName* `(` `)` *TypeAnnotation*`opt` `{` *FunctionBody* `}`

*SetAccessor:*
`set` *PropertyName* `(` *BindingIdentifierOrPattern* *TypeAnnotation*`opt` `)` `{` *FunctionBody* `}`

对象字面量的类型是由字面量赋值指定的属性组成的对象类型。`get` 和 `set` 访问器可以指定相同的属性名，否则对同一属性指定多个赋值是错误的。

简写赋值形式为：

```
prop
```

等价于：

```
prop : prop
```

同样，赋值形式为：

```
f ( ... ) { ... }
```

等价于：

```
f : "function" ( ... ) { ... }
```

对象字面量中的每个属性赋值按以下方式处理：

- 如果具有上下文类型，且上下文类型包含同名属性，则属性赋值的上下文类型为该属性的类型。
- 否则，如果对象字面量具有上下文类型、上下文类型包含数字索引签名，且属性赋值指定了数字属性名，则属性赋值的上下文类型为数字索引签名类型。
- 否则，如果对象字面量具有上下文类型且上下文类型包含字符串索引签名，则属性赋值的上下文类型为字符串索引签名类型。
- 否则，无上下文类型处理属性赋值。

形式为 *Name* `:` *Expr* 的属性赋值引入的属性类型为 *Expr* 的类型。

`get` 访问器的处理方式与无参数的普通函数声明（6.1 节）相同。`set` 访问器的处理方式与具有单个参数和 `Void` 返回类型的普通函数声明相同。当一个属性同时声明 `get` 和 `set` 访问器时：

- 如果两个访问器都包含类型注解，则指定的类型必须相同。
- 如果仅一个访问器包含类型注解，另一个行为上表现为具有相同的类型注解。
- 如果两个访问器都不包含类型注解，则 `get` 访问器的推断返回类型将成为 `set` 访问器的参数类型。

如果为属性声明了 `get` 访问器，则 `get` 访问器的返回类型将成为该属性的类型。如果仅为属性声明了 `set` 访问器，则 `set` 访问器的参数类型（如果没有类型注解，该类型可能为 `Any` 类型）将成为该属性的类型。

当对象字面量通过一个包含字符串索引签名的类型进行上下文类型化时，该对象字面量的结果类型将包含一个字符串索引签名，其类型为对象字面量中声明的属性类型的联合类型，或者如果对象字面量为空，则为 `Undefined` 类型。同样，当对象字面量通过一个包含数字索引签名的类型进行上下文类型化时，该对象字面量的结果类型将包含一个数字索引签名，其类型为对象字面量中声明的数字命名属性（3.9.4 节）类型的联合类型，或者如果对象字面量未声明任何数字命名属性，则为 `Undefined` 类型。

如果属性赋值的 *PropertyName* 是一个不表示已知符号（2.2.3）的计算属性名，则该构造结构被视为***动态属性赋值***。以下规则适用于动态属性赋值：

- 动态属性赋值不会在对象字面量的类型中引入属性。
- 动态属性赋值的属性名表达式必须是 `Any` 类型或 `String`、`Number` 或 `Symbol` 原始类型。
- 如果属性名表达式的类型为 `Any` 或 `Number` 原始类型，则与动态属性赋值关联的名称被视为数字属性名。

## 4.6 数组字面量

数组字面量 `[ expr1, expr2, ..., exprN ]` 根据上下文表示一个数组类型（3.3.2 节）或元组类型（3.3.3 节）的值。非空数组字面量中的每个元素表达式都按如下方式处理：

- 如果数组字面量不包含展开元素，且该数组字面量通过类型 *T* 进行上下文类型化（4.23 节），且 *T* 具有一个数字名为 *N* 的属性，其中 *N* 是该元素表达式在数组字面量中的索引，则该元素表达式通过该属性的类型进行上下文类型化。
- 否则，如果数组字面量通过带有数字索引签名的类型 *T* 进行上下文类型化，则该元素表达式通过数字索引签名的类型进行上下文类型化。
- 否则，该元素表达式不进行上下文类型化。

数组字面量表达式的结果类型确定如下：

- 如果数组字面量为空，结果类型为元素类型为 `Undefined` 的数组类型。
- 否则，如果数组字面量不包含展开元素且通过类元组类型（3.3.3 节）进行上下文类型化，则结果类型为由元素表达式的类型构造的元组类型。
- 否则，如果数组字面量不包含展开元素且是解构赋值（4.21.1 节）中的数组赋值模式，则结果类型为由元素表达式的类型构造的元组类型。
- 否则，结果类型为数组类型，其元素类型为非展开元素表达式的类型的联合与展开元素的数字索引类型的联合。展开元素必须指定一个类数组类型（3.3.2 节）的表达式，否则将发生错误。上述规则意味着，数组字面量始终是数组类型，除非它通过类元组类型进行上下文类型化。例如：

```
var a = [1, 2]; // number
var b = ["hello", true]; // (string | boolean)
var c: [number, string] = ["three"]; // number, string
```

当输出目标为 ECMAScript 3 或 5 时，包含展开元素的数组字面量将被重写为 `concat` 方法的调用。例如：

```
var a = [2, 3, 4];
var b = [0, 1, ...a, 5, 6];
```

被重写为：

## 4.7 模板字面量

## 4.8 括号

括号表达式 `( expr )` 的类型与其包含的表达式类型相同。

## 4.9 super 关键字

`super` 关键字可以用于在类上下文中引用基类属性。

### 4.9.1 super 调用

`super` 调用由 `super` 关键字后跟圆括号参数列表组成。`super` 调用仅在类构造上下文中允许，并根据 8.3 节引用基类。如果 `super` 调用在 15 节描述的基类函数中，则 `super` 调用使用 4.2 节的基类。如果 `super` 调用在 8.4 节描述的基类函数中，则 `super` 调用使用 4.2 节的基类。如果 `super` 调用在 8.5 节描述的基类函数中，则 `super` 调用使用 4.2 节的基类。如果 `super` 调用在 8.6 节描述的基类函数中，则 `super` 调用使用 4.2 节的基类。如果基类是泛型的，则 `super` 调用的参数类型是基类的联合类型。对于 `super` 调用，生成的 JavaScript 代码在 8.2 节中指定。

### 4.9.2 super 属性访问

`super` 属性访问由 `super` 关键字后跟一个点和一个标识符组成。`super` 属性访问在类上下文中允许访问基类成员。具体而言：

- 在构造函数、实例函数或实例访问器中 `this` 引用基类实例时，`super` 访问允许访问基类的实例函数。
- 在静态函数或静态访问器中 `this` 引用基类构造函数时，`super` 访问允许访问基类的静态函数。

`super` 访问在其他上下文中是不允许的，除非在函数表达式中 `this` 是基类的类型。`super` 访问通常用于访问基类的成员函数。此类示例参见 8.4 节。

## 4.10 函数表达式

函数表达式扩展自 JavaScript，可选包含参数和返回类型注解。

*FunctionExpression:* ( Modified )
`function` *BindingIdentifier*`opt` *CallSignature* `{` *FunctionBody* `}`

第 6 节提供的函数描述适用于函数表达式，但函数表达式不支持重载。函数表达式的类型是一个包含单个调用签名的对象，其参数和返回类型从函数表达式推断得出。

当没有参数注解的函数表达式通过类型 *T* 进行上下文类型化（4.23 节），且从 *T* 中可以提取出上下文签名 *S* 时，函数表达式的处理方式显式指定了 *S* 中的参数注解。参数按位置匹配且不需要相同的名称。如果函数表达式的参数比 *S* 少，则忽略 *S* 中额外的参数。如果函数表达式的参数比 *S* 多，则额外的参数均被认为具有 `Any`。

同样，当没有返回类型注解的函数表达式通过函数类型 *T* 进行上下文类型化（4.23 节），且从 *T* 中可以提取出上下文签名 *S* 时，内部返回语句（5.10 节）中的表达式通过 *S* 的返回类型进行上下文类型化。

上下文签名 *S* 从函数类型 *T* 的提取如下：

- 如果 *T* 是只有一个调用签名的函数类型，且该签名不是泛型的，则 *S* 为该签名。
- 如果 *T* 是联合类型，令 *U* 为 *T* 中具有调用签名的元素集合。如果 *U* 中的每个类型只有一个调用签名且该签名不是泛型的，并且所有签名在忽略返回类型时是相同的，则 *S* 是一个具有相同参数和返回类型联合的签名。
- 否则，无法从 *T* 中提取上下文签名。

在示例中：

```
var f: (s: string) => string = function (s) {
    return s.toLowerCase();
};
```

该函数表达式通过 `f` 的类型进行上下文类型化，由于该函数表达式没有类型参数或类型注解，其参数类型信息是从上下文类型中提取的，因此推导出 `s` 的类型为 `String` 原始类型。

## 4.11 箭头函数

箭头函数从 JavaScript 扩展而来，可选地包含参数和返回类型注解。

*箭头形式参数：*（已修改）

*调用签名*

第 6 章中提供的函数声明描述也适用于箭头函数，不同之处在于箭头函数不支持重载。

箭头函数的类型确定方式与函数表达式相同（第 4.10 节）。

同样，箭头函数的参数和箭头函数体中的返回语句也以与函数表达式相同的方式通过上下文进行上下文类型化。

当一个具有表达式体且没有返回类型注解的箭头函数被上下文类型化（第 4.23 节）为函数类型 *T*，并且可以从 *T* 中提取出上下文签名 *S* 时，该表达式体通过 *S* 的返回类型进行上下文类型化。

形式如下的箭头函数表达式：

```
( ... ) => expr
```

完全等同于：

```
( ... ) => { return expr; }
```

此外，形式如下的箭头函数表达式：

```
id => { ... }
id => expr
```

完全等同于：

```
( id ) => { ... }
( id ) => expr
```

因此，以下示例都是等价的：

```
(x) => { return Math.sin(x); }
(x) => Math.sin(x)
x => { return Math.sin(x); }
x => Math.sin(x)
```

函数表达式引入了一个新的动态绑定 `this`，而箭头函数表达式保留了其闭包上下文的 `this`。箭头函数表达式在编写回调函数时特别有用，否则回调通常具有未定义或意料之外的 `this`。

在示例中：

```
class Messenger {
    message = "Hello World";
    start() {
        setTimeout(() => alert(this.message), "3000");
    }
};
var messenger = new Messenger();
messenger.start();
```

使用箭头函数表达式会导致回调具有与周围 `start` 方法相同的 `this`。如果将回调写为标准的函数表达式，则有必要手动安排对周围 `this` 的访问，例如通过将其拷贝到局部变量中：

```
class Messenger {
    message = "Hello World";
    start() {
        var _this = this;
        setTimeout(function() { alert(_this.message); }, "3000");
    }
};
var messenger = new Messenger();
messenger.start();
```

TypeScript 编译器应用此类类型转换，将箭头函数表达式重写为标准函数表达式。

形式如下的结构：

```
<T> ( ... ) => { ... }
```

可以被解析为带有类型参数的箭头函数表达式，或者是应用于无类型参数箭头函数的类型断言。它被解析为前者，但可以使用括号来选择后者的含义：

```
<T> ( ( ... ) => { ... } )
```

## 4.12 类表达式

*TODO: 文档化 **类表达式*。

## 4.13 属性访问

属性访问使用点符号表示法或括号表示法。属性访问表达式始终被分类为引用。

形式如下的点符号表示法属性访问：

```
object . name
```

其中 *object* 是一个表达式，*name* 是一个标识符（可能包括保留字），用于访问给定对象上给定名称的属性。点符号表示法属性访问在编译时的处理如下：

- 如果 *object* 的类型为 `Any`，则允许任何 *name*，且属性访问的类型为 `Any`。
- 否则，如果 *name* 表示 *object* 类型中的可访问表面属性（第 3.11.1 节），则属性访问的类型为该属性的类型。公共成员始终可访问，但类的私有和受保护成员具有限制的访问权限，如 8.2.2 节所述。
- 否则，属性访问无效，并发生编译时错误。

形式如下的括号表示法属性访问：

```
object [ index ]
```

其中 *object* 和 *index* 是表达式，用于访问给定对象上通过 index 表达式计算出的名称的属性。括号表示法属性访问在编译时的处理如下：

- 如果 *index* 是字符串字面量或数字字面量，且 *object* 具有由该字面量命名的可见表面属性（第 3.11.1 节）（数字字面量转换为其字符串表示），则属性访问的类型为该属性的类型。
- 否则，如果 *object* 具有可见的数字索引签名且 *index* 的类型为 `Any`、`Number` 原始类型或枚举类型，则属性访问的类型为该索引签名的类型。
- 否则，如果 *object* 具有可见的字符串索引签名且 *index* 的类型为 `Any`、`String` 或 `Number` 原始类型或枚举类型，则属性访问的类型为该索引签名的类型。
- 否则，如果 *index* 的类型为 `Any`、`String` 或 `Number` 原始类型或枚举类型，属性访问类型为 `Any`。
- 否则，属性访问无效，并发生错误。

*TODO: 使用符号索引属性*。

上述规则意味着当使用括号表示法访问时，强类型化的属性。例如：

```
type = {
    a: string;
    b: number;
}
var obj: type = { a: "hello", b: 1 };
console.log(obj.a);
console.log(obj["a"]);
console.log(obj.b);
console.log(obj["b"]);
```

## 4.14 new 运算符

形式如下的结构：

```
new C ( ... )
new C < ... > ( ... )
```

可以解析为带有类型参数的 `new` 的表达式。它被解析为前者，但可以使用括号来选择后者的含义：

```
new C < ... > ( ... )
```

其中 *C* 是函数类型或类型 `Any`。如果 *C* 类型为 `Any`，或具有没有调用签名的对象类型，调用是未类型函数调用。

- 如果 *C* 的类型为 `Any`，则允许任何参数列表，且操作类型为 `Any`。
- 否则，如果 *C* 具有一个或多个调用签名，操作被处理为函数调用，但使用构造签名作为解析的初始集。函数调用的结果变为操作类型。
- 如果 *C* 没有构造签名但具有一个或多个调用签名，如果函数调用的结果不是 `Void`，则发生错误。

## 4.15 函数调用

函数调用从 JavaScript 扩展以支持可选类型参数。

*参数：*（已修改）

*TypeArguments*`opt` `(` *ArgumentList*`opt` `)`

函数调用采取以下形式：

```
func ( ... )
func < ... > ( ... )
```

其中 *func* 是函数类型或类型 `Any`。函数表达式跟着可选参数列表（第 3.6.2 节）和参数列表。如果 *func* 类型为 `Any`，或具有没有调用签名但是 `Function` 接口子类的对象类型，调用是未类型函数调用。在未类型函数调用中，不允许类型参数，参数表达式可以是任何类型或数字，且不为参数表达式提供上下文类型，且结果始终为 `Any`。

如果 *func* 具有可见调用签名（第 3.11.1 节），调用是类型函数调用。TypeScript 在类型函数调用中采用重载解析以支持具有多个调用签名的函数。此外，TypeScript 在泛型函数调用中执行类型参数推断以自动确定类型参数。

### 4.15.1 重载解析

函数调用重载解析的目的是确保至少有一个签名可用，为参数提供上下文类型，并确定函数调用的结果类型，这在多个可用签名之间可能不同。重载解析对函数调用的运行时行为没有影响。由于 JavaScript 不支持函数重载，运行时重要的是函数名。

*TODO: 描述重载解析中使用 **通配函数类型***。

类型调用的编译处理包括以下步骤：

- 首先，根据声明顺序从类型中的调用签名构建候选签名列表。对于类和接口，继承的签名被认为在 `extends` 子句的显式声明签名之后。

`o` 非泛型签名是候选是因为当函数调用没有类型参数且该签名适用于函数调用的参数列表。

`o` 泛型签名在满足以下条件时，是不带类型参数的函数调用候选：

- 每个类型参数的类型推断（第 4.15.2 节）成功
- 一旦推断出的类型参数替换了其关联类型参数，该签名适用于函数调用的参数列表。

`o` 泛型签名在满足以下条件时，是带类型参数的函数调用候选：

- 签名的类型参数数量与类型参数列表中提供的数量一致，
- 类型参数满足它们的约束条件，且
- 一旦类型参数替换了其关联类型参数，该签名适用于函数调用的参数列表。

- 如果候选签名列表为空，则该函数调用为错误。
- 否则，如果候选列表包含一个或多个签名，其中每个签名中每个参数表达式的类型都是其对应参数类型的子类型，则这些签名中第一个签名的返回类型成为函数调用的返回类型。
- 否则，候选列表中第一个签名的返回类型成为函数调用的返回类型。

当满足以下条件时，一个签名被认为相对于参数列表的***适用签名***：

- 参数的数量不少于必需参数的数量，
- 参数的数量不少于参数的总数，且
- 对于每个参数表达式 *e* 及其对应的参数 *P*，当 *e* 由 *P* 的类型进行上下文类型化（第 4.23 节）时，不会产生错误且 *e* 的类型可以赋值给（第 3.11.4 节）*P* 的类型。

*TODO: **函数调用中的展开运算符**以及将**迭代器**展开到函数调用中*

### 4.15.2 类型参数推断

给定一个签名 `< T1, T2, …, Tn > ( p1: P1, p2: P2, …, pm: Pm )`，其中每个参数类型 *P* 引用了零或多个类型参数 *T*，以及一个参数列表 `( e1, e2, …, em )`，类型参数推断的任务是找到一组类型参数 `A1…An` 来替换 `T1…Tn`，使得参数列表成为一个适用签名。

*TODO: 更新**类型参数推断和重载解析规则***

类型参数推断为每个类型参数产生一组候选类型。给定一个类型参数 *T* 和一组候选类型，实际推断的类型参数确定如下：

- 如果候选类型集合为空，则 *T* 的推断类型参数为 *T* 的约束。
- 否则，如果至少有一个候选类型是所有其他候选类型的超类型，则令 *C* 表示第一个这样的候选类型。如果 *C* 满足 *T* 的约束，则 *T* 的推断类型参数为 *C*。否则，*T* 的推断类型参数为 *T* 的约束。
- 否则，如果没有候选类型是所有其他候选类型的超类型，则类型推断失败，且未为 *T* 推断出任何类型参数。

为了计算候选类型，按如下方式处理参数列表：

- 最初，所有推断的类型参数都被视为***未固定***，且候选类型集合为空。
- 从左到右处理，每个参数表达式 *e* 由其对应的参数类型 *P* 进行***推断类型化***，这可能导致某些推断的类型参数变为***固定***，并根据从 *e* 计算的类型到 *P* 对未固定的推断类型参数进行类型推断（第 3.11.7 节）。

通过类型 *T* 对表达式 *e* 进行推断类型化的过程与通过 *T* 对 *e* 进行上下文类型化的过程相同，但例外：

- *e* 内部包含的原本应上下文类型化的表达式改为进行推断类型化。
- 当对函数表达式进行推断类型化（第 4.10 节）且分配给该表达式参数的类型引用了正在进行推断的类型参数时，相应的推断类型参数将变为***固定***，且不再对它们进行进一步的候选推断。
- 如果 *e* 是包含恰好一个泛型调用签名且没有其他成员的函数类型，且 *T* 是包含恰好一个非泛型调用签名且没有其他成员的函数类型，那么对于 *T* 的调用签名参数所引用的类型参数所做的任何推断都是***固定***的，并且 *e* 的类型变为一个函数类型，其调用签名在 *T* 的调用签名上下文中实例化（第 3.11.6 节）。

示例：

```typescript
```



```typescript
function choose<T>(x: T, y: T): T {
  return Math.random() < 0.5 ? x : y;
}
```

```typescript
let result = choose<number>(10, 20);
```

```typescript
var pairs = zip<string, number, { name: string; age: number }>(
  names,
  ages,
  s => n => ({ name: s, age: n })
);
```

因此，`pairs` 的结果类型为`{ name: string; age: number }[]`。

### 4.15.3 语法歧义

在 *Arguments*（参数）产生式（第 4.15 节）中引入类型参数会导致表达式语法中出现某些歧义。例如，以下语句：

```typescript
f(g<A, B>("7"));
```

该语句可以被解释为对`f`的调用，带有两个参数：`g < A`和`B > (7)`。或者，它也可以被解释为对`f`的调用，其中一个参数是对泛型函数`g`的调用，而该调用有两个类型参数和一个普通参数。

语法歧义通过以下方式解决：在一个标记序列的某种可能解释为 *Arguments* 产生式的上下文中，如果初始标记序列形成了一个语法上正确的 *TypeArguments*（类型参数）产生式，并且后面紧跟一个`(`标记，则该标记序列被作为 *Arguments* 产生式处理，并丢弃任何其他可能的解释。否则，该标记序列不被视为 *Arguments* 产生式。

此规则意味着上述对`f`的调用被解释为带有一个参数的调用，即对泛型函数`g`的调用，该调用有两个类型参数和一个普通参数。然而，以下语句：

```typescript
f(g < A, B > "7");
```

```typescript
f(g < A, B > +("7"));
```

都被解释为对`f`的调用，且带有两个参数。

## 4.16 类型断言

TypeScript 扩展了 JavaScript 表达式语法，允许对表达式进行类型断言：

```text
UnaryExpression: (Modified)
```

```text
< Type > UnaryExpression
```

类型断言表达式由一个包含在`<`和`>`之间的类型组成，其后紧跟的是一个一元表达式。类型断言表达式完全是编译时的构造。类型断言在运行时不会被检查，并且不会对生成的 JavaScript 产生影响（因此没有运行时开销）。类型以及包裹的`<`和`>`会直接从生成的代码中移除。

在形式为`<T> e`的类型断言表达式中，`e`由`T`（第 4.23 节）进行上下文类型化，且`e`的结果类型必须赋值给`T`，或者`T`必须赋值给`e`结果类型的拓宽形式，否则将发生编译错误。结果的类型是`T`。

类型断言会检查双方向的赋值兼容性。因此，类型断言允许进行*可能*正确但*无法确定*确实正确的类型转换。在示例中：

```typescript
class Shape { ... }

class Circle extends Shape { ... }

function createShape(kind: string): Shape {
  if (kind === "circle") return new Circle();
  ...
}

var circle = <Circle> createShape("circle");
```

类型注解表明`createShape`函数*可能*返回一个`Circle`（因为`Circle`是`Shape`的子类型），但*无法确定*它是否会这样做（因为它的返回类型是`Shape`）。因此，需要通过类型断言将结果视为`Circle`。

如上所述，类型断言在运行时不会被检查，程序员需要自己负责防止错误，例如使用`instanceof`运算符：

```typescript
var shape = createShape(shapeKind);

if (shape instanceof Circle) {
  var circle = <Circle> shape;
  ...
}
```

## 4.17 JSX 表达式

*TODO: 文档化 JSX 表达式*。

## 4.18 一元运算符

接下来的章节规定了一元运算符的编译时规则。通常，如果一元运算符的操作数不满足所述要求，将发生编译错误，且结果在后续处理中默认为`Any`类型。

### 4.18.1 `++` 和 `--` 运算符

这些运算符（无论是前缀还是后缀形式）要求其操作数类型为`Any`、`Number`原始类型或枚举类型，并被分类为引用（第 4.1 节）。它们产生`Number`原始类型的结果。

### 4.18.2 `+`、`–`、`~` 运算符

这些运算符允许操作数为任意类型，并产生`Number`原始类型的结果。一元`+`运算符可以方便地将任何类型的值转换为`Number`原始类型：

```typescript
function getValue() { ... }

var n = +getValue();
```

上述示例如果`getValue()`的结果不是数字，则将其转换为数字。无论`getValue`的返回类型如何，`n`的推断类型都是`Number`原始类型。

### 4.18.3 `!` 运算符

`!`运算符允许其操作数为任意类型，并产生`Boolean`原始类型的结果。连续使用两个`!`运算符可以方便地将任何类型的值转换为`Boolean`原始类型：

```typescript
function getValue() { ... }

var b = !!getValue();
```

上述示例如果`getValue()`的结果不是布尔，则将其转换为布尔。无论`getValue`的返回类型如何，`b`的推断类型都是`Boolean`原始类型。

### 4.18.4 `delete` 运算符

`delete`运算符接受任意类型的操作数，并产生`Boolean`原始类型的结果。

### 4.18.5 `void` 运算符

`void`运算符接受任意类型的操作数，并产生值`undefined`。结果的类型是`Undefined`类型（3.2.7）。

### 4.18.6 `typeof` 运算符

`typeof`运算符接受任意类型的操作数，并产生`String`原始类型的值。在期望类型的位置，`typeof`也可以用于类型查询（第 3.8.10 节）以产生表达式的类型。

```typescript
var x = 5;

var y = typeof x; // 用于表达式

var z: typeof x; // 用于类型查询
```

在上述示例中，`x`的类型是`number`，`y`的类型是`string`，因为在表达式中使用，`typeof`产生一个字符串类型的值（在此情况下为字符串`"number"`），而`z`的类型是`number`，因为在类型查询中使用，`typeof`获取了表达式的类型。

## 4.19 二元运算符

接下来的章节规定了二元运算符的编译时处理。通常，如果二元运算符的操作数不满足所述要求，将发生编译错误，且结果为`Any`。

### 4.19.1 `*`、`/`、`%`、`<<`、`>>`、`>>>`、`^`、`|`

这些运算符要求操作数为`Number`原始类型、枚举类型，或者至少一个操作数为`Any`类型、`Number`原始类型或枚举类型。它们产生`Number`原始类型的结果。

### 4.19.2 `+` 运算符

二元`+`运算符要求两个操作数为`Number`原始类型或枚举类型，或者至少一个操作数为`Any`类型或`String`原始类型。如果一个操作数为`null`或`undefined`值，则被视为另一个操作数的类型。如果两个操作数都是`Number`原始类型，则结果为`Number`原始类型。如果一个或两个操作数都是`String`原始类型，则结果为`String`原始类型。否则，结果为`Any`类型。

| | | Any | Boolean | Number | String | Other |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Any | | Any | Any | Any | String | Any |
| Boolean | | Any | Any | Any | String | Any |
| Number | | Any | Any | Number | String | Any |
| String | | String | String | String | String | Any |
| Other | | Any | Any | Any | String | Any |

任意类型的值可以通过添加一个空字符串转换为`String`原始类型：

```typescript
function getValue() { ... }

var s = getValue() + "";
```

上述示例如果`getValue()`的结果不是字符串，则将其转换为字符串。无论`getValue`的返回类型如何，`s`的推断类型都是`String`原始类型。

### 4.19.3 `<`、`>`、`<=`、`>=`、`==`、`!=`、`===` 和 `!==` 运算符

这些运算符要求一个或两个操作数的类型可以赋值给另一个。结果始终是`Boolean`原始类型。

| | | Any | Boolean | Number | String | Other |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Any | Boolean | | | | | |
| Boolean | Boolean | | | | | |
| Number | Boolean | | | | | |
| String | Boolean | | | | | |
| Other | Boolean | | | | | |

### 4.19.4 `instanceof` 运算符

`instanceof`运算符要求左操作数的类型为`Any`、对象类型或类型参数类型，而右操作数的类型为`Any`或`Function`接口类型的子类型。结果始终是`Boolean`原始类型。

### 4.19.5 `in` 运算符

`in`运算符要求左操作数的类型为`Any`、`String`原始类型或`Number`原始类型，且右操作数的类型为`Any`、对象类型或类型参数类型。其结果始终为`Boolean`原始类型。

### 4.19.6 `&&` 运算符

`&&`运算符允许操作数为任何类型，并产生与第二个操作数相同类型的结果。

| | Any | Boolean | Number | String | Other |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Any | Any | Boolean | Number | String | Other |
| Boolean | Any | Boolean | Number | String | Other |
| Number | Any | Boolean | Number | String | Other |
| String | Any | Boolean | Number | String | Other |
| Other | Any | Boolean | Number | String | Other |

### 4.19.7 `||` 运算符

`||`运算符允许操作数为任何类型。

如果`||`表达式是上下文类型化的（第 4.23 节），则操作数由相同的类型进行上下文类型。否则，左操作数不是上下文类型，右操作数由左操作数的类型进行上下文类型。

结果的类型是两个操作数类型的联合类型。

| | Any | Boolean | Number | String | Other |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Any | Any | Any | Any | Any | Any |
| Boolean | Any | Boolean | N \| B | S \| B | B \| O |
| Number | Any | N \| B | Number | S \| N | N \| O |
| String | Any | S \| B | S \| N | String | S \| O |
| Other | Any | B \| O | N \| O | S \| O | Other |

## 4.20 条件运算符

在形式如下的条件表达式中：

```typescript
test ? expr1 : expr2
```

`test`表达式可以是任何类型。

如果该条件表达式是上下文类型化的（第 4.23 节），`expr1`和`expr2`由相同的类型进行上下文类型。否则，`expr1`和`expr2`不是上下文类型。

结果的类型是`expr1`和`expr2`类型的联合类型。

## 4.21 赋值运算符

形式如下的赋值：

```typescript
v = expr
```

要求`v`被分类为引用（第 4.1 节）或赋值模式（第 4.21.1 节）。`expr`表达式由`v`的类型进行上下文类型（第 4.23 节），且`expr`的类型必须可赋值给（第 3.11.4 节）`v`的类型，否则将发生编译时错误。结果是一个类型为`expr`的值。

形式如下的复合赋值：

```typescript
v ??= expr
```

其中`??=`是复合赋值运算符之一：

```text
*= /= %= += -= <<= >>= >>>= &= ^= |=
```

它与相应的非复合操作具有相同的要求，并产生相同类型的值。此外，复合赋值要求`v`被分类为引用（第 4.1 节），且非复合操作的类型可赋值给`v`的类型。注意，在复合赋值中不允许`v`为赋值模式。

### 4.21.1 解构赋值

***解构赋值***是一种赋值操作，其中左操作数是根据 ECMAScript 6 规范中的 *AssignmentPattern* 产生式定义的解构赋值模式。

在解构赋值表达式中，右侧表达式的类型必须可赋值给左侧的赋值目标。如果满足以下任一条件，则类型为`S`的表达式被认为可赋值给赋值目标`V`：

- `V`是变量，且`S`可赋值给`V`的类型。
- `V`是一个对象赋值模式，并且对于`V`中的每个赋值属性`P`：
  - `S`的类型为`Any`；或
  - `S`具有与`P`中指定的属性名相同的可见属性，其类型可赋值给`P`中给出的目标；或
  - `P`指定了一个数字属性名，且`S`具有一个数字索引签名，其类型可赋值给`P`中给出的目标；或
  - `S`具有一个字符串索引签名，其类型可赋值给`P`中给出的目标。
- `V`是一个数组赋值模式，`S`是`Any`类型或类数组类型（第 3.3.2 节），并且对于`V`中的每个赋值元素`E`：
  - `S`的类型为`Any`；或
  - `S`是元组类类型（第 3.3.2 节），且可赋值给`E`中给出的目标。

## 4.22 逗号运算符

逗号运算符允许操作数为任何类型，并产生与第二个操作数相同类型的结果。

## 4.23 上下文类型化表达式

在几种上下文中，通过目标进行上下文类型化，表达式的类型检查得到了改进。

如果`||`表达式是上下文类型化的（第 4.23 节），则操作数由相同的类型进行上下文类型。否则，左操作数不是上下文类型，右操作数由左操作数的类型进行上下文类型。

87

- 在赋值表达式中，右侧表达式的类型由左侧表达式的类型进行上下文类型化。

在示例中：

```typescript
interface EventObject {
  x: number;
  y: number;
}

interface EventHandlers {
  mousedown?: (event: EventObject) => void;
  mouseup?: (event: EventObject) => void;
  mousemove?: (event: EventObject) => void;
}

function setEventHandlers(handlers: EventHandlers) { ... }

setEventHandlers({
  mousedown: e => { startTracking(e.x, e.y); },
  mouseup: e => { endTracking(); }
});
```

传递给`setEventHandlers`的对象字面量被上下文类型化为`EventHandlers`类型。这导致两个属性赋值都被上下文类型化为匿名函数类型`(event: EventObject) => void`，从而使箭头函数表达式中的参数`e`自动被类型为`EventObject`。

## 4.24 类型守卫（Type Guards）

类型守卫是涉及`typeof`和`instanceof`运算符的特定表达式模式，它们会导致变量或参数的类型收窄到更具体的类型。例如，在下面的代码中，对`x`静态类型的认知结合`typeof`检查，可以安全地在`if`语句的第一个分支将`x`的类型收窄为`string`，在第二个分支收窄为`number`。

```typescript
function foo(x: number | string) {
  if (typeof x === "string") {
```



```
return x.length; // x 此处类型为 string
} else {
return x + 1; // x 此处类型为 number
}
```

变量或参数的类型在以下情况下收窄：

- 在`if`语句的真分支语句中，当`if`条件为真时，变量或参数的类型通过条件中的类型守卫收窄，前提是`if`语句的任何部分都不包含对该变量或参数的赋值。
- 在`if`语句的假分支语句中，当`if`条件为假时，变量或参数的类型通过条件中的类型守卫收窄，前提是`if`语句的任何部分都不包含对该变量或参数的赋值。
- 在条件表达式的真表达式中，当条件为真时，变量或参数的类型通过条件中的类型守卫收窄，前提是条件表达式的任何部分都不包含对该变量或参数的赋值。
- 在条件表达式的假表达式中，当条件为假时，变量或参数的类型通过条件中的类型守卫收窄，前提是条件表达式的任何部分都不包含对该变量或参数的赋值。
- 在`&&`操作的右侧操作数中，当左侧操作数为真时，变量或参数的类型通过左侧操作数的类型守卫收窄，前提是两个操作数都不包含对该变量或参数的赋值。
- 在`||`操作的右侧操作数中，当左侧操作数为假时，变量或参数的类型通过左侧操作数的类型守卫收窄，前提是两个操作数都不包含对该变量或参数的赋值。

类型守卫仅仅是遵循特定模式的表达式。通过类型守卫在真或假时收窄变量*x*类型的类型取决于类型守卫的形式如下：

- 形式为`x instanceof C`的类型守卫，其中*x*不是`Any`类型，*C*是全局类型`'Function'`的子类型，且*C*具有名为`'prototype'`的属性：为真时，如果它是*x*类型的子类型，则将*x*的类型收窄为*C*中`'prototype'`属性的类型；或者如果*x*的类型是联合类型，则从*x*的类型中移除所有不是*C*'prototype'属性类型子类型的类型；为假时，对*x*的类型没有影响。
- 形式为`typeof x === s`的类型守卫，其中*s*是值为`'string'`、`'number'`或`'boolean'`的字符串字面量：为真时，如果该基本类型是*x*类型的子类型，则将*x*的类型收窄为该基本类型；或者如果*x*的类型是联合类型，则从*x*的类型中移除所有不是该基本类型的类型；为假时，从*x*的类型中移除该基本类型。
- 形式为`typeof x === s`的类型守卫，其中*s*是任何非`'string'`、`'number'`或`'boolean'`的字符串字面量：为真时，如果*x*是联合类型，则从*x*的类型中移除所有是`string`、`number`或`boolean`基本类型的子类型；为假时，对*x*的类型没有影响。
- 形式为`typeof x !== s`的类型守卫，其中*s*是一个字符串字面量：为真时，通过`typeof x === s`为假的情况收窄*x*的类型；或为假时，通过`typeof x === s`为真的情况收窄*x*的类型。
- 形式为`!expr`的类型守卫：为真时，通过*expr*为假的情况收窄*x*的类型；或为假时，通过*expr*为真的情况收窄*x*的类型。
- 形式为`expr1 && expr2`的类型守卫：为真时，在真时先通过*expr1*为真的情况收窄*x*的类型，再通过*expr2*为真的情况收窄；或为假时无影响；为假时，通过*expr1*为假的情况收窄*x*的类型，再通过*expr2*为真的情况收窄。
- 形式为`expr1 || expr2`的类型守卫：为真时，在真时通过*expr1*为真的情况收窄*x*的类型，再通过*expr2*为假的情况收窄；或为假时，通过*expr2*为假的情况收窄*x*的类型。
- 其他任何形式的类型守卫对*x*的类型没有影响。

注意，类型守卫只影响变量和参数，对对象的成员（如属性）没有影响。此外，可以通过调用改变守变量类型的函数来破坏类型守卫。

在示例中

```typescript
function f(x: string | number | boolean) {
  if (typeof x === "string" || typeof x === "number") {
    let y = x; // y 的类型为 string | number
  } else {
    let z = x; // z 的类型为 boolean
  }
}
```

在示例中

```typescript
class C {
  data: string | string[];
  getData() {
    let data = this.data;
    return typeof data === "string" ? data : data.join(" ");
  }
}
```

变量`data`的类型在第一个条件表达式中为`string`，在第二个条件表达式中为`string[]`，`getData`的推断类型为`string`。注意，必须将`data`属性复制到本地变量，类型守卫才能生效。

在示例中

```typescript
class NamedItem {
  name: string;
}
function getName(obj: Object) {
  return obj instanceof NamedItem ? obj.name : "unknown";
}
```



`obj` 的类型在第一个条件表达式中被收窄为`NamedItem`，`getName` 函数的推断类型为`string`。

## 5 语句

本章描述了 TypeScript 为 JavaScript 语句提供的静态类型检查。TypeScript 本身没有引入任何语句结构，但它扩展了局部声明的语法，包含了接口（`interface`）、类型别名（`type alias`）和枚举（`enum`）声明。

### 5.1 块

块扩展包含了局部接口、类型别名和枚举声明（类已由 ECMAScript 6 语法包含）。

*Declaration: ( Modified )*

…

*InterfaceDeclaration*

*TypeAliasDeclaration*

*EnumDeclaration*

局部类、接口、类型别名和枚举的声明是块作用域的，类似于`let`和`const`声明。

### 5.2 变量语句

变量语句扩展包含了可选的类型注解。

*VariableDeclaration: ( Modified )*

*SimpleVariableDeclaration*

*DestructuringVariableDeclaration*

变量声明可以是简单变量声明，也可以是解构变量声明。

### 5.2.1 简单变量声明

一个***简单变量声明***引入了一个单一命名变量，并可选地为其分配一个初始值。

*SimpleVariableDeclaration:*

*BindingIdentifier* *TypeAnnotation**opt* *Initializer**opt*

由简单变量声明引入的变量的类型 *T* 确定如下：

- 如果声明包含类型注解，*T* 为该类型。
- 否则，如果声明包含初始化表达式，*T* 为初始化表达式类型的拓宽化形式（第 3.12 节）。
- 否则，*T* 为`Any`类型。

当变量声明同时指定了类型注解和初始化表达式时，初始化表达式的类型必须是可赋值给（第 3.11.4 节）类型注解中给出的类型。允许在同一个声明空间内对同一个变量名进行多次声明，前提是每个声明都与变量关联相同的类型。

当变量声明具有类型注解时，在该类型注解中使用`typeof`运算符来引用正在声明的变量被视为一个错误。

以下是一些简单变量声明及其相关类型的示例。

```typescript
var a; // any
var b: number; // number
var c = 1; // number
var d = { x: 1, y: "hello" }; // { x: number; y: string; }
var e: any = "test"; // any
```

以下情况是被允许的，因为单一变量'x'的所有声明都关联相同的类型（`Number`）：

```typescript
var x = 1;
var x: number;
if (x == 1) {
var x = 2;
}
```

在以下示例中，所有五个变量都是相同类型`'{ x: number; y: number;}'。

```typescript
interface Point { x: number; y: number; }
var a = { x: 0, y: undefined };
var b: Point = { x: 0, y: undefined };
var c = <Point>{ x: 0, y: undefined };
var d: { x: number; y: number; } = { x: 0, y: undefined };
var e = <{ x: number; y: number; }> { x: 0, y: undefined };
```

### 5.2.2 解构变量声明

一个***解构变量声明***引入了零或多个命名变量，并用从对象属性或数组元素中提取的值对它们进行初始化。

*DestructuringVariableDeclaration:*

*BindingPattern* *TypeAnnotation**opt* *Initializer*

每个指定标识符的绑定属性或元素都会引入一个同名变量。变量的类型是与绑定属性或元素关联类型的拓宽形式（第 3.12 节），定义如下。与解构变量声明关联的类型 *T* 确定如下：

- 如果声明包含类型注解，*T* 为该类型。
- 否则，如果声明包含初始化表达式，*T* 为该初始化表达式的类型。
- 否则，*T* 为`Any`类型。

与绑定属性关联的类型 *T* 确定如下：

- 令 *S* 为直接包含的解构变量声明、绑定属性或绑定元素关联的类型。
- 如果 *S* 是`Any`类型：
  - 如果绑定属性指定了初始化表达式，*T* 为该初始化表达式的类型。
  - 否则，*T* 为`Any`类型。
- 令 *P* 为绑定属性指定的属性名。
- 如果 *S* 具有名为 *P* 的可见属性，*T* 为该属性的类型。
- 否则，如果 *S* 具有数字索引签名且 *P* 是数值名称，*T* 为数字索引签名的类型。
- 否则，如果 *S* 具有字符串索引签名，*T* 为字符串索引签名的类型。
- 否则，绑定属性未关联任何类型且会发生错误。

与绑定元素关联的类型 *T* 确定如下：

- 令 *S* 为直接包含的解构变量声明、绑定属性或绑定元素关联的类型。
- 如果 *S* 是`Any`类型：
  - 如果绑定元素指定了初始化表达式，*T* 为该初始化表达式的类型。
  - 否则，*T* 为`Any`类型。
- 如果 *S* 不是类数组类型（第 3.3.2 节），则未与任何类型关联。
- 如果绑定元素是剩余元素（`rest element`），*T* 为数组类型 *E*，其中 *E* 是 *S* 的类型。
- 否则，如果 *S* 是元组类型（第 3.3.3 节）：
  - 令 *N* 为绑定模式中的索引。
  - 如果 *S* 具有名为 *N* 的属性，*T* 为该属性的类型。
  - 否则，绑定元素未关联任何类型且会发生错误。
- 否则，如果 *S* 具有索引签名，*T* 为该索引签名的类型。
- 否则，绑定元素未关联任何类型且会发生错误。

当解构变量声明、绑定属性或绑定元素指定初始化表达式时，初始化表达式的类型必须是可赋值给解构变量声明、绑定属性或绑定元素的类型。当输出目标为 ECMAScript 6 或更高时，除了移除类型注解外，解构声明保持不变。当输出目标为 ECMAScript 5 时，解构声明将被重写为简单变量声明。例如，对象解构声明`var { x, p, q = "false" } = getSomeObject();`被重写为简单变量声明：

```typescript
var x = getSomeObject().x;
var y = getSomeObject().p;
var z = getSomeObject().q !== undefined ? getSomeObject().q : "false";
```

同样，数组解构声明`var [x, y, z = 1] = getArray();`被重写为简单变量声明：

```typescript
var x = getArray()[0];
var y = getArray()[1];
var z = getArray()[2] !== undefined ? getArray()[2] : 1;
```

### 5.2.3 推断类型

指定绑定模式的变量、参数、绑定属性或绑定元素具有***推断类型***，其类型确定如下：

- 如果声明指定对象绑定模式，推断类型为包含一组指定绑定属性的的类型。每个属性的类型由其绑定属性声明推断，且当绑定属性声明指定初始化表达式时，该属性是可选的。
- 如果声明指定没有剩余元素的数组绑定模式，推断类型为与指定绑定元素声明对应的元组类型。每个元素的类型由其绑定元素声明推断。
- 如果声明指定带有剩余元素的数组绑定模式，推断类型为元素类型为`Any`的数组类型。

绑定属性或绑定元素声明的推断类型为：

- 声明初始化表达式的类型（如果有），否则
- 声明中指定的绑定模式的推断类型（如果有），否则
- `Any`类型

在示例`function f({ a, b = "hello", c = 1 }) { ... }`中，函数参数中绑定模式的推断类型为`{ a: any; b?: string; c?: number; }`。由于参数没有类型注解，这成为了参数的类型。

在示例`var [a, b, c] = [1, "hello", true];`中，数组字面量初始化表达式通过绑定模式的推断类型进行上下文类型，具体为元组类型`[any, any, any]`。因为上下文类型是元组类型，数组字面量的结果类型是元组类型`[number, string, boolean]`，因此解构声明为`a`、`b`和`c`分别赋予了`number`、`string`和`boolean`类型。

## 5.3 Let and Const Declarations

`let`和`const`声明被扩展以包含可选类型注解。

*LexicalBinding:* *( 已修改 )*

*SimpleLexicalBinding*

*DestructuringLexicalBinding*

*SimpleLexicalBinding:*

*BindingIdentifier* *TypeAnnotation**opt* *Initializer**opt*

*DestructuringLexicalBinding:*

*BindingPattern* *TypeAnnotation**opt* *Initializer**opt*

*TODO: 文档 let and const 声明的作用域和类型*.

## 5.4 If, Do, and While Statements

控制'if'、'do'和'while'语句的表达式可以是任何类型（而不只是`Boolean`类型）。

## 5.5 For Statements

'for'语句中的变量声明扩展方式与变量语句中的变量声明（第 5.2 节）相同。

## 5.6 For-In Statements

在形式为

```typescript
for (v in expr) statement
```

的'for-in'语句中

*v* 必须是一个分类为`Any`类型的引用或`String`原始类型的表达式，且 *expr* 必须是`Any`类型、对象类型或类型参数类型的表达式。

在形式为

```typescript
for (var v in expr) statement
```

的'for-in'语句中

*v* 必须是一个没有类型注解且声明了`Any`类型变量的变量声明，且 *expr* 必须是`Any`类型、对象类型或类型参数类型的表达式。

## 5.7 For-Of Statements

*TODO: 文档 for-of 语句*.

## 5.8 Continue Statements

'continue'语句要求直接或间接地（但不跨越函数边界）嵌套在迭代语句（'do'、'while'、'for'或'for-in'）内部。当'continue'语句包含目标标签时，该目标标签必须出现在包含它的（但不跨越函数边界）迭代语句的标签集中。

## 5.9 Break Statements

'break'语句要求直接或间接地（但不跨越函数边界）嵌套在迭代语句（'do'、'while'、'for'或'for-in'）或'switch'语句内部。当'break'语句包含目标标签时，该目标标签必须出现在包含它的（但不跨越函数边界）语句的标签集中。

## 5.10 Return Statements

'return'语句出现在函数体外是一个错误。具体而言，不允许在全局级别或命名空间体中使用'return'语句。

不带表达式的'return'语句返回'undefined'值，并允许出现在任何函数的体内，无论函数的返回类型如何。

当'return'语句包含表达式时，如果包含它的函数包含返回类型注解，则返回表达式由该返回类型进行上下文类型（第 4.23 节），并且必须是可赋值给返回类型的类型。否则，如果包含它的函数由类型 *T* 进行上下文类型，则 *Expr* 由 *T* 的返回类型进行上下文类型。

在没有返回类型注解的函数实现中，返回类型根据函数体中的'return'语句推断，见第 6.3 节。

在示例

```typescript
function f(): (x: "string") => "number" {
return s => s.length;
}
```

'return'语句中的箭头表达式由'f'的返回类型进行上下文类型，从而给's'赋予了'string'类型。

## 5.11 With Statements

在 TypeScript 中使用'with'语句是错误的，就像 ECMAScript 5 的严格模式一样。此外，在'with'语句体内部，TypeScript 认为出现在表达式（第 4.3 节）中的每个标识符都是`Any`类型，无论其声明类型如何。由于'with'语句将一组静态未知的标识符置于静态已知标识符之前，因此无法为任何标识符分配有意义的静态类型。

## 5.12 Switch Statements

在'switch'语句中，每个'case'表达式必须是可赋值给或从'switch'表达式类型（第 3.11.4 节）的。

## 5.13 Throw Statements

'throw'语句中指定的表达式可以是任何类型。

## 5.14 Try Statements

'try'语句中'catch'子句引入的变量总是`Any`类型。'catch'子句中不能包含类型注解。

## 6 Functions

TypeScript 扩展了 JavaScript 函数以包含类型参数、参数和返回类型注解、重载、默认参数值以及剩余参数。

## 6.1 Function Declarations

函数声明被扩展以允许在重载声明中省略函数体。

*FunctionDeclaration:* *( 已修改 )*

```typescript
function BindingIdentifieropt CallSignature { FunctionBody }
function BindingIdentifieropt CallSignature ;
function BindingIdentifieropt CallSignature 在包含的空间中引入函数的具名值。
```

## 6.2 Function Overloads

函数重载允许比单一签名更准确地规范函数。函数的返回类型根据参数而异。函数调用中的重载解析在第 4.15 节进一步描述。函数重载纯粹是编译时结构。它们对生成的 JavaScript 没有影响。

函数重载的参数列表不能指定默认值。也就是说，重载在指定可选参数时只能使用`?`形式。以下是一个带重载函数的示例：

```typescript
function attr(name: "string"): "string";
function attr(name: "string", value: "string"): Accessor;
function attr(map: "any"): Accessor;
function attr(nameOrMap: "any", value?: "string"): "any" {
if (nameOrMap && typeof nameOrMap === "string") {
// handle string case
}
else {
// handle map case
}
}
```

注意每个重载和最终实现指定相同的标识符。此声明引入的局部变量'attr'的类型为：

```typescript
var attr: {
(name: "string"): "string";
(name: "string", value: "string"): Accessor;
(map: "any"): Accessor;
};
```

## 6.3 Function Implementations

没有返回类型注解的函数实现被称为***隐式类型函数***。隐式类型函数 *f* 的返回类型推断方式如下：

- 如果 *f* 函数体内没有带表达式的'return'语句，推断返回类型为`Void`。
- 否则，如果 *f* 函数体直接引用 *f* 或引用通过此分析引用 *f* 的任何隐式类型函数，推断返回类型为`Any`。
- 否则，如果 *f* 是上下文类型函数表达式（第 4.10 节），推断返回类型是函数体中'return'语句表达式类型的联合类型（第 3.4 节），忽略不带表达式的'return'语句。
- 否则，推断返回类型是函数体中'return'语句表达式类型中第一个是其他类型超类型（第 3.11.3 节）的类型，忽略不带表达式的'return'语句。如果没有'return'语句类型是其他类型的超类型，则发生编译时错误。

在示例中

```typescript
function f(x: number) {
  if (x <= 0) return x;
  return g(x);
}

function g(x: number) {
  return f(x - 1);
}
```

'f'和'g'的推断返回类型为`Any`，因为这两个函数在一个没有返回类型注解的循环中相互引用。为其中任何一个添加显式的返回类型'number'都会打破循环，并导致另一个函数的返回类型被推断为'number'。

返回类型不是`Void`或`Any`类型的显式类型函数，其体体处必须至少有一个返回语句。该规则的例外是该函数实现仅包含单一的'throw'语句。

函数实现中`this`的类型是`Any`类型。

在函数实现的签名中，可以通过在参数后跟一个初始化值将其标记为可选。当参数声明同时包含类型注解和初始化值时，初始化表达式将根据指定的类型进行上下文类型化（第 4.23 节），并且必须赋值给所指定的类型，否则会发生编译错误。当参数声明没有类型注解但包含初始化值时，该参数的类型是初始化表达式类型的类型的宽泛形式（第 3.12 节）。

初始化表达式在函数体的作用范围内进行求值，但不允许引用局部变量，并且仅允许访问在其初始化的参数左侧声明的参数，除非参数引用发生在嵌套的函数表达式中。

当输出目标为 ECMAScript 3 或 5 时，对于每个带有初始化值的参数，生成的 JavaScript 中将包含一条用于为省略的参数替换默认值的语句，如第 6.6 节所述。该示例

```typescript
function strange(x: number, y = x * 2, z = x + y) {
  return z;
}
```

生成的 JavaScript 等同于

```typescript
function strange(x, y, z) {
  if (y === void 0) { y = x * 2; }
  if (z === void 0) { z = x + y; }
  return z;
}
```

在示例中

```typescript
var x = 1;
function f(a = x) {
  var x = "hello";
}
```

局部变量'x'在参数初始化值的作用域内（因此隐藏了外层的'x'），但引用它是一个错误，因为在对参数初始化值求值时，它始终是未初始化的。

## 6.4 解构参数声明

参数声明可以指定绑定模式（第 3.9.2.2 节），然后被称为***解构参数声明***。与解构变量声明（第 5.2.2 节）类似，解构参数声明引入了零或多个命名局部变量，并用从作为参数传递的对象或数组的属性或元素中提取的值来初始化它们。

解构参数声明中引入的局部变量的类型与解构变量声明引入的局部变量的方式相同，但解构参数声明相关的类型 *T* 按照如下方式确定：

- 如果声明包含类型注解，*T* 为该类型。
- 如果声明出现在具有可用上下文签名的函数表达式中（第 4.10 节），*T* 是从上下文签名获得的类型。
- 否则，如果声明包含初始化表达式，*T* 是初始化表达式类型的类型的宽泛形式（第 3.12 节）。
- 否则，如果声明指定了绑定模式，*T* 是该绑定模式的隐含类型（第 5.2.3 节）。
- 否则，如果参数是剩余参数，*T* 为`any[]`。
- 否则，*T* 为`any`。

当输出目标为 ECMAScript 6 或更高版本时，除了移除可选类型注解外，解构参数声明在发射的 JavaScript 代码中保持不变。当输出目标为 ECMAScript 3 或 5 时，解构参数声明被重写为局部变量声明。

示例

```typescript
function drawText({ text = "", location: [x, y] = [0, 0], bold = false }) {
  // Draw text
}
```

声明了一个函数`drawText`，它接受一个类型为
`{ text?: string; location?: [number, number]; bold?: boolean; }`的单个参数。

当输出目标为 ECMAScript 3 或 5 时，该函数被重写为

```typescript
function drawText(_a) {
  var _b = _a.text,
  text = _b === void 0 ? "" : _b,
  _c = _a.location,
  _d = _c === void 0 ? [0, 0] : _c,
  x = _d[0],
  y = _d[1],
  _e = _a.bold,
  bold = _e === void 0 ? false : _e;
  // Draw text
}
```

解构参数声明不允许在单个绑定模式上使用类型注解，因为此类注解会与对象面字量中已建立的冒号含义冲突。类型注解必须写在顶层参数声明上。例如

```typescript
interface DrawTextInfo {
  text?: string;
  location?: [number, number];
  bold?: boolean;
}

function drawText({ text, location: [x, y], bold }: DrawTextInfo) {
  // Draw text
}
```

## 6.5 泛型函数

函数实现可以在签名中包含类型参数（第 3.9.2.1 节），被称为***泛型函数***。类型参数为调用时参数类型和返回类型之间的关系提供了一种机制。类型参数没有运行时表示——它们完全是编译时的构造。

在函数实现签名中声明的类型参数在签名和函数体的作用范围内。

以下是一个泛型函数的示例：

```typescript
interface Comparable {
  compareTo(other: any): number;
}

function compare<T extends Comparable>(x: T, y: T): number {
  if (x == null) return y == null ? 0 : -1;
  if (y == null) return 1;
  return x.compareTo(y);
}
```

注意'x'和'y'参数是'Comparable'的子类型，因此具有'compareTo'。这在第 3.6.1 节中进一步描述。

在示例中

```typescript
class Person {
  name: string;
  compareTo(other: Person) {
    return compare(this.name, other.name);
  }
}
```

'compare'的类型参数被自动推断为`String`类型，因为两个参数都是字符串。

## 7 接口 (Interfaces)

接口提供了对对象类型进行命名和参数化的能力，并将现有的命名对象类型组合成新的类型。

接口没有运行时表示——它们纯粹是编译时的构造。接口对于文档化和验证属性、作为参数传递的对象以及函数返回的对象的所需的形状特别有用。

由于 TypeScript 具有结构化类型系统，具有特定成员集合的接口类型被认为与具有相同集合的另一个接口类型或对象字面量相同，并且可以相互替换（参见第 3.11.2 节）。

类声明可以在其`implements`子句中引用接口，以验证它们提供了接口的实现。

### 7.1 接口声明

接口声明声明了一个***接口类型***（interface type*）。

*InterfaceDeclaration:*

```typescript
interface BindingIdentifier TypeParametersopt InterfaceExtendsClauseopt ObjectType
```

*InterfaceExtendsClause:*

`extends` *ClassOrInterfaceTypeList*

*ClassOrInterfaceTypeList:*

*ClassOrInterfaceType*

*ClassOrInterfaceTypeList* `,` *ClassOrInterfaceType*

*ClassOrInterfaceType:*

*TypeReference*

一个 *InterfaceDeclaration* 在包含的声明空间中引入了一个命名类型（第 3.7 节）。接口声明的 *BindingIdentifier* 不可以是预定义的类型名称之一（第 3.8.1 节）。

接口可以可选地具有类型参数（第 3.6.1 节），这些参数作为在类型引用中引用接口时提供的实际类型的占位符。带有类型参数的接口称为***泛型接口***（generic interface*）。泛型接口声明的类型参数在整个声明范围内都是有效的，并且可以在 *InterfaceExtendsClause* 和 *ObjectType* 主体中引用。

接口可以继承零或多个***基类型***（base types*），这些基类型在 *InterfaceExtendsClause* 中指定。基类型必须是引用类或接口类型的类型引用。

接口具有其声明中 *ObjectType* 指定的成员，并且继承了所有未被接口中声明隐藏的基类型成员：

- 属性声明会隐藏一个具有相同名的公共基类型属性。
- 字符串索引签名声明会隐藏基类型的字符串索引签名。
- 数字索引签名声明会隐藏基类型的数字索引签名。

接口声明必须满足以下约束，否则将发生编译时错误：

- 接口声明可能直接或间接地指定源自同一声明的基类型。换句话说，无论类型参数如何，接口不能直接或间接地成为它自身的基类型。
- 接口不能声明与继承的私有或受保护属性同名的属性。
- 具有相同名的继承属性必须是相同的（第 3.11.2 节）。
- 接口的所有属性必须满足第 3.9.4 节中指定的接口索引签名所隐含的约束。
- 声明接口的实例类型（第 3.7.1 节）必须可以赋值（第 3.11.4 节）给每个基类型引用。

接口允许从多个基类型继承相同的成员，在这种情况下，它只会包含每个特定成员的一个实例。

下面是两个包含相同名称但不同类型属性的接口示例：

```typescript



```typescript
interface Mover {
  move(): void;
  getStatus(): { speed: number };
}

interface Shaker {
  shake(): void;
  getStatus(): { frequency: number };
}
```

扩展 `Mover` 和 `Shaker` 的接口必须声明一个新的 `getStatus` 属性，否则它将继承两个不同类型的 `getStatus` 属性。新的 `getStatus` 属性必须声明为，使得结果 `MoverShaker` 是 `Mover` 和 `Shaker` 的子类型：

```typescript
interface MoverShaker extends Mover, Shaker {
  getStatus(): { speed: number; frequency: number };
}
```

由于函数和构造类型只是对象类型，接口可以用于声明函数和构造类型。例如：

```typescript
interface StringComparer {
  (a: string, b: string): number;
}
```

这声明 `StringComparer` 为接收两个字符串并返回数字的类型。

### 7.2 声明合并（Declaration Merging）

接口是“开放的”，具有相同根（见第 2.3 节）的接口声明合并到一个接口。

当泛型接口具有多个声明时，所有声明必须具有相同的类型参数列表，即具有相同的约束。

在具有多个声明的接口中，`extends` 子句合并为一个基类型集合，接口声明的主体合并为一个对象类型。声明合并产生的声明顺序对应于将每个接口声明的成员按照其顺序*前置*到合并列表中。因此，最后一个接口声明的成员将出现在合并类型顺序的最前面。

例如，以下顺序的声明序列：

```typescript
interface Document {
  createElement(tagName: any): Element;
}

interface Document {
  createElement(tagName: string): HTMLElement;
}

interface Document {
  createElement(tagName: "div"): HTMLDivElement;
  createElement(tagName: "span"): HTMLSpanElement;
  createElement(tagName: "canvas"): HTMLCanvasElement;
}
```

等同于以下单一声明：

```typescript
interface Document {
  createElement(tagName: "div"): HTMLDivElement;
  createElement(tagName: "span"): HTMLSpanElement;
  createElement(tagName: "canvas"): HTMLCanvasElement;
  createElement(tagName: string): HTMLElement;
  createElement(tagName: any): Element;
}
```

注意，最后一个接口声明的成员出现在合并声明之前。同样注意同一接口主体中声明的成员相对顺序被保留。

### 7.3 接口扩展类

当接口类型扩展类类型时，它继承类的成员，但不继承它们的实现。这就好像接口声明了类的所有成员但没有提供实现一样。接口甚至继承基类的私有和受保护成员。当包含私有或受保护成员的类是接口类型的基类型时，该接口类型只能由该类或其子类实现。例如：

```typescript
class Control {
  private state: any;
}

interface SelectableControl extends Control {
  select(): void;
}

class Button extends Control {
  select() {}
}

class TextBox extends Control {
  select() {}
}

class Image extends Control {}

class Location {
  select() {}
}
```



在上面的示例中，`SelectableControl` 包含了 `Control` 的所有成员，包括私有属性 `state`。由于 `state` 是私有成员，只有 `Control` 的后类可以实现 `SelectableControl`。因为只有 `Control` 的后类具有源自同一声明的 `state` 私有成员，这是私有成员兼容所需的要求（第 3.11 节）。

在 `Control` 类中，可以通过 `SelectableControl` 的实例访问私有成员 `state`。实际上，一个 `SelectableControl` 的行为类似于一个已知具有 `select` 方法的 `Control`。`Button` 和 `TextBox` 类是 `SelectableControl` 的子类型（因为它们都继承自 `Control` 且都具有 `select` 方法），但 `Image` 和 `Location` 类则不是。

## 7.4 动态类型检查

TypeScript 并不提供直接的机制来动态测试一个对象是否实现了某个特定的接口。相反，TypeScript 代码可以使用 JavaScript 的技术，通过检查对象上是否存在一组适当的成员来实现。例如，给定第 7.1 节中的声明，以下是针对 `MoverShaker` 接口的动态检查：

```
var obj: any = getSomeObject();
if (obj && obj.move && obj.shake && obj.getStatus) {
  var moverShaker = <MoverShaker> obj;
  ...
}
```

如果经常使用此类检查，可以将其抽象为一个函数：

```
function asMoverShaker(obj: any): MoverShaker {
  return obj && obj.move && obj.shake && obj.getStatus ? obj : 'null';
}
```

## 8 类

TypeScript 扩展了 JavaScript 类，包含了类型参数、`implements` 子句、访问修饰符、成员变量声明以及构造函数中的参数属性声明。

*TODO: 文档化抽象类。*

### 8.1 类声明

类声明声明了一个**类类型**和**构造函数**。

*ClassDeclaration:* *( 已修改 )*

```
class BindingIdentifieropt TypeParametersopt ClassHeritage { ClassBody }
```

`ClassDeclaration`（类声明）在包含它的声明空间中引入了一个命名的类型（类类型）和一个命名的值（构造函数）。类类型由类体中声明的实例成员和从基类继承的实例成员组成。构造函数被赋予由构造函数声明、类体中的静态成员声明以及从基类继承的静态成员构成的匿名类型。构造函数初始化并返回类类型的实例。

类声明的 `BindingIdentifier` 不可以是预定义的类型名称之一（第 3.8.1 节）。`BindingIdentifier` 只有类类出现在 `export default` 声明中（第 11.3.4.2 节）时才是可选的。

类可以可选地拥有类型参数（第 3.6.1 节），作为在类型引用引用类时提供的实际类型的占位符。带有类型参数的类被称为**泛型类**。泛型类声明的类型参数在整个声明范围内有效，可以在 `ClassHeritage` 和 `ClassBody` 中被引用。

以下示例在包含它的声明空间中引入了名为 `Point` 的命名类型（类类型）和名为 `Point` 的命名值（构造函数）。

```
class Point {
  constructor(public x: number, public y: number) { }
  public length() { return Math.sqrt(this.x * this.x + this.y * this.y); }
  static origin = new Point(0, 0);
}
```

命名类型 `Point` 与完全等同于

```
interface Point {
  x: number;
  y: number;
  length(): number;
}
```

命名值 `Point` 是一个构造函数，其类型对应于声明：

```
var Point: {
  new(x: number, y: number): Point;
  origin: Point;
};
```

引用类的上下文区分了类实例类型和构造函数。例如，在赋值语句

```
var p: Point = new Point(10, 20);
```

类型注解中的标识符 `Point` 指的是类实例类型，而 `new` 表达式中的标识符 `Point` 指向的是构造函数对象。

### 8.1.1 类继承规范

*TODO: 更新此节以反映类 `extends` 子句中的表达式。*

类的继承规范由可选的 `extends` 和 `implements` 子句组成。`extends` 子句指定了类的基类，`implements` 子句指定了一组接口，用于验证类提供的实现。

*ClassHeritage:* *( 已修改 )*

*ClassExtendsClause*opt* *ImplementsClause*opt*

*ClassExtendsClause:*

`extends` *ClassType*

*ClassType:*

*TypeReference*

*ImplementsClause:*

`implements` *ClassOrInterfaceTypeList*

包含 `extends` 子句的类被称为**派生类**，`extends` 子句中指定的类被称为派生类的**基类**。当类继承规范省略 `extends` 子句时，该类没有基类。然而，正如每个对象类型一样，对类的类型引用（第 3.3.1 节）似乎具有名为 `Object` 的全局接口类型的成员，除非这些成员被类中具有相同的成员所隐藏。

类继承规范必须满足以下约束条件，否则将发生编译错误：

- 如果存在，`extends` 子句中指定的类型引用必须表示一个类类型。

此外，`TypeName` 只有在类声明出现在 `export default` 声明中（第 11.3.4.2 节）时才是可选的。

类可以可选地拥有类型参数（第 3.6.1 节），作为在类型引用引用类时提供的实际类型的占位符。带有类型参数的类被称为泛型类。泛型类声明的类型参数在整个声明范围内有效，可以在 `ClassHeritage` 和 `ClassBody` 中被引用。

以下示例在包含它的声明空间中引入了名为 `Point` 的命名类型（类类型）和名为 `Point` 的命名值（构造函数）。

```
class Point {
  constructor(public x: number, public y: number) { }
  public length() { return Math.sqrt(this.x * this.x + this.y * this.y); }
  static origin = new Point(0, 0);
}
```

命名类型 `Point` 与完全等同于

```
interface Point {
  x: number;
  y: number;
  length(): number;
}
```

命名值 `Point` 是一个构造函数，其类型对应于声明：

```
var Point: {
  new(x: number, y: number): Point;
  origin: Point;
};
```

引用类的上下文区分了类实例类型和构造函数。例如，在赋值语句

```
var p: Point = new Point(10, 20);
```

类型注解中的标识符 `Point` 指的是类实例类型，而 `new` 表达式中的标识符 `Point` 指向的是构造函数对象。

### 8.1.1 类继承规范

*TODO: 更新此节以反映类 `extends` 子句中的表达式。*

类的继承规范由可选的 `extends` 和 `implements` 子句组成。`extends` 子句指定了类的基类，`implements` 子句指定了一组接口，用于验证类提供的实现。

*ClassHeritage:* *( 已修改 )*

*ClassExtendsClause*opt* *ImplementsClause*opt*

*ClassExtendsClause:*

`extends` *ClassType*

*ClassType:*

*TypeReference*

*ImplementsClause:*

`implements` *ClassOrInterfaceTypeList*

包含 `extends` 子句的类被称为**派生类**，`extends` 子句中指定的类被称为派生类的**基类**。当类继承规范省略 `extends` 子句时，该类没有基类。然而，正如每个对象类型一样，对类的类型引用（第 3.3.1 节）似乎具有名为 `Object` 的全局接口类型的成员，除非这些成员被类中具有相同的成员所隐藏。

类继承规范必须满足以下约束条件，否则将发生编译错误：

- 如果存在，`extends` 子句中指定的类型引用必须表示一个类类型。

此外，`TypeName` 只有在类声明出现在 `export default` 声明中（第 11.3.4.2 节）时才是可选的。

类可以可选地拥有类型参数（第 3.6.1 节），作为在类型引用引用类时提供的实际类型的占位符。带有类型参数的类被称为泛型类。泛型类声明的类型参数在整个声明范围内有效，可以在 `ClassHeritage` 和 `ClassBody` 中被引用。

以下示例在包含它的声明空间中引入了名为 `Point` 的命名类型（类类型）和名为 `Point` 的命名值（构造函数）。

```
class Point {
  constructor(public x: number, public y: number) { }
  public length() { return Math.sqrt(this.x * this.x + this.y * this.y); }
  static origin = new Point(0, 0);
}
```

命名类型 `Point` 与完全等同于

```
interface Point {
  x: number;
  y: number;
  length(): number;
}
```

命名值 `Point` 是一个构造函数，其类型对应于声明：

```
var Point: {
  new(x: number, y: number): Point;
  origin: Point;
};
```

引用类的上下文区分了类实例类型和构造函数。例如，在赋值语句

```
var p: Point = new Point(10, 20);
```

类型注解中的标识符 `Point` 指的是类实例类型，而 `new` 表达式中的标识符 `Point` 指向的是构造函数对象。

例如，私有和保护的访问性可以通过将对象的静态类型更改为 `Any` 并动态访问成员来绕过。

以下示例演示了私有和保护的访问性：

```typescript
class A {
  private x: number;
  protected y: number;

  static f(a: A, b: B) {
    a.x = 1; // Ok
    b.x = 1; // Ok
    a.y = 1; // Ok
    b.y = 1; // Ok
  }
}

class B extends A {
  static f(a: A, b: B) {
    a.x = 1; // Error, x only accessible within A
    b.x = 1; // Error, x only accessible within A
    a.y = 1; // Error, y must be accessed through instance of B
    b.y = 1; // Ok
  }
}
```

在类 `A` 中，对 `x` 的访问是被允许的，因为 `x` 声明在 `A` 中；对 `y` 的访问也是允许的，因为它们都是通过 `A` 的实例或派自 `A` 的类型进行的。在类 `B` 中，对 `x` 的访问是不允许的，且对 `y` 的首次访问是一个错误，因为它是通过 `A` 的实例进行的，而 `A` 并没有派自封装类 `B`。

### 8.2.3 继承与重写

派生类**继承**其基类未**重写**的所有成员。继承意味着派生类隐式地包含了基类的所有未被重写的成员。只有公共和保护属性成员可以被重写。

当派生类中的属性成员与基类的属性成员具有相同的名称和种类（实例或静态）时，则该派生类属性成员被重写了基类的属性成员。被重写属性成员的类型必须可以赋值（第 3.11.4 节）给被重写的属性成员的类型，否则将发生编译时错误。

基类的实例成员函数可以被派生类的实例成员函数重写，但不能被其他类型的成员重写。

基类的实例成员变量和访问器可以被派生类的实例成员变量和访问器重写，但不能被其他类型的成员重写。

基类的静态属性成员可以被派生类的任何种类的静态属性成员重写，只要类型兼容的，如上所述。

当派生类中的索引成员与基类的索引成员具有相同的索引种类（字符串或数字）时，则该派生类索引成员被认为重写了基类的索引成员。被重写索引成员的类型必须可以赋值（第 3.11.4 节）给被重写的索引成员的类型，否则将发生编译时错误。

### 8.2.4 类类型

类声明声明了一个新的命的具名类型（第 3.7 节），称为类类型。在类的构造函数和成员函数内部，`this` 的类型是该类类型的实例类型（第 3.7.1 节）。该类类型具有以下成员：

- 类体中每个实例成员变量声明对应一个属性。
- 类体中每个实例成员函数声明对应一个函数类型的属性。
- 类体中每个唯一命名的实例成员访问器声明对应一个属性。
- 类体中每个带有 `public`、`private` 或 `protected` 修饰符声明的构造参数对应一个属性。
- 类体中每个实例索引成员声明对应一个索引签名。
- 类中未重写的所有基类实例类型属性或索引成员。

类的所有实例属性成员（包括私有或保护的）必须满足第 3.9.4 节指定的类索引成员所隐含的约束。

在示例中

```typescript
class A {
  public x: number;
```



`constructor(value: number)` {

`this.x = value`;

}

`[index: string]: any`;

}

`A` 类的实例属性成员包括：

- 属性 `x`。
- 构造函数参数 `value` 的属性。
- 索引成员 `[index: string]`。

`A` 类的实例属性成员必须满足其索引成员的约束。

`A` 类的索引成员如下：

```typescript
class A {

  public x: number;

  constructor(value: number) {

    this.x = value;

  }

  [index: string]: any;

}
```

`A` 类的索引成员是：

- 索引签名 `[index: string]`。

`A` 类的实例属性成员如下：

```typescript
class A {

  public x: number;

  constructor(value: number) {

    this.x = value;

  }

  [index: string]: any;

}
```

`A` 类的实例属性成员包括：

- 属性 `x`。
- 构造函数参数 `value` 的属性。
- 索引成员 `[index: string]`。

`A` 类的索引成员如下：

```typescript
class A {

  public x: number;

  constructor(value: number) {

    this.x = value;

  }

  [index: string]: any;

}
```

`A` 类的索引成员是：

- 索引签名 `[index: string]`。

## 8.2.5 构造函数类型

由类声明引入的构造函数被称为构造函数类型。构造函数类型具有以下成员：

如果类没有构造声明且没有基类，则具有单个构造签名，其参数与类相同，并返回类的实例类型。

如果类没有构造声明但有基类，则具有来自基类的构造签名，其参数与基类相同，并返回类的实例类型。

如果类具有构造实现（重载），则具有一组重载的构造签名，其参数列表与实现相同，并返回类的实例类型。

每个类自动包含一个名为 `prototype` 的静态属性，其类型是每个类型参数替换为 `Any` 的类。

示例：

```typescript
class Pair<T1, T2> {

  constructor(public item1: T1, public item2: T2) { }

}

class TwoArrays<T> extends Pair<T[], T[]> { }
```

引入了两个命名类型对应：

```typescript
interface Pair<T1, T2> {

  item1: T1;

  item2: T2;

}

interface TwoArrays<T> {

  item1: T[];

  item2: T[];

}
```

以及两个构造函数对应：

```typescript
var Pair: {

  new <T1, T2>(item1: T1, item2: T2): Pair<T1, T2>;

}

var TwoArrays: {

  new <T>(item1: T[], item2: T[]): TwoArrays<T>;

}
```

在没有构造函数定义的类中，将提供一个自动构造函数，如第 8.3.3 节所述。

当类具有构造函数重载时，这些重载决定了传递给构造函数对象的类型的构造签名，并且构造函数的实现签名（如果有）必须可以赋值该类型。否则，构造函数的实现本身决定构造签名。这与函数声明（第 6.2 节）中处理重载的方式完全是平行的。当一个类既有构造函数重载又有构造函数实现时，重载必须在实现之前，且所有声明都必须是连续的，中间不能有任何其他语法元素。

构造函数的函数体允许包含 `return` 语句。如果 `return` 语句指定了表达式，则这些表达式必须是可以赋值给类实例类型的类型。

泛型类的类型参数在构造函数声明中处于作用范围内并是可以访问的。

### 8.3.1 构造函数参数

与函数类似，只有构造函数实现（而不是构造函数重载）可以为可选参数指定默认值表达式。此类默认值表达式引用 `this` 将导致编译错误。当输出目标为 ECMAScript 3 或 5 时，对于每个带有默认值的参数，生成的用于构造函数的 JavaScript 中将包含一条语句，用默认值替换省略的参数。

`ConstructorImplementation` 的参数可以以 `public`、`private` 或 `protected` 修饰符作为前缀。这被称为**参数属性声明**，是声明一个与参数同名的属性并用参数值初始化该属性的简写。例如，该声明：

```typescript
class Point {

  constructor(public x: number, public y: number) {

    // 构造函数体

  }

}
```

等同于：

```typescript
class Point {

  public x: number;

  public y: number;

  constructor(x: number, y: number) {

    this.x = x;

    this.y = y;

    // 构造函数体

  }

}
```

### 8.3.2 Super 调用

`Super` 调用（第 4.9.1 节）用于调用基类的构造函数。一个 `super` 调用由关键字 `super` 加上用括号括起来的参数列表组成。例如：

```typescript
class ColoredPoint extends Point {

  constructor(x: number, y: number, public color: string) {

    super(x, y);

  }

}
```

没有 `extends` 子句的类的构造函数可能包含 `super` 调用，而派生类的构造函数必须在其函数体某处至少包含一次 `super` 调用。`super` 调用不允许出现在构造函数外部或构造函数内部的局部函数中。

如果以下两个条件均成立，构造函数体的第一条语句*必须*是一个 `super` 调用：

- 所在的类是一个派生类。
- 构造函数声明了参数属性，或者所在的类声明了带有初始化器的实例成员变量。

在这样的强制性 `super` 调用中，参数表达式引用 `this` 将导致编译错误。参数属性和带有初始化器的实例成员变量的初始化在类没有基类时立即在构造函数体开始时执行；如果类是派生类，则紧随 `super` 调用之后执行。

### 8.3.3 自动构造函数

如果一个类省略了构造函数声明，则提供一个**自动构造函数**。

在没有 `extends` 子句的类中，自动构造函数没有参数，除了执行实例成员变量初始化器（第 8.4.1 节，如果有）外不执行任何操作。

在派生类中，自动构造具有与基类构造函数相同的参数列表（以及可能存在重载）。自动提供的构造函数首先通过类似于以下的调用将调用转发给基类构造函数：

```javascript
BaseClass.apply("this", arguments);
```

然后执行实例成员变量初始化器（如果有）。

## 8.4 属性成员声明

属性成员声明可以是成员变量声明、成员函数声明或成员访问器声明。

`PropertyMemberDeclaration:`

- `MemberVariableDeclaration`
- `MemberFunctionDeclaration`
- `MemberAccessorDeclaration`

不带 `static` 修饰符的成员声明被称为实例成员声明。实例属性成员声明在类实例类型中声明属性（第 8.2.4 节），并且必须指定的名称在包含类的所有实例属性成员和参数属性声明中是唯一的，但实例 `get` 和 `set` 访问器声明可以成对指定相同的名称。

带有 `static` 修饰符的成员声明被称为静态成员声明。静态属性成员声明在构造函数类型中声明属性（第 8.2.5 节），并且必须指定的名称在包含类的所有静态属性成员声明中是唯一的，但静态 `get` 和 `set` 访问器声明可以成对指定相同的名称。

注意实例和静态属性成员的声明空间是分开的。因此，可以拥有同名的实例属性和静态属性成员。

除了第 8.2.3 节描述的重写外，派生类声明与基类成员相同名称和类型（实例或静态）的属性成员将是一个错误。

每个类都自动包含一个名为 `prototype` 的静态属性成员，其类型是类类型的实例化，其中为每个类型参数提供了类型 `Any` 作为类型参数。显式声明名为 `prototype` 的静态属性成员将是一个错误。

下面是一个包含实例属性成员和静态属性成员声明的类示例：

```typescript
class Point {

  constructor(public x: number, public y: number) { }

  public distance(p: Point) {

    var dx = this.x - p.x;

    var dy = this.y - p.y;

    return Math.sqrt(dx * dx + dy * dy);

  }

  static origin = new Point(0, 0);

  static distance(p1: Point, p2: Point) { return p1.distance(p2); }

}
```

类实例类型 `Point` 具有成员：

```typescript
interface Point {

  x: number;

  y: number;

  distance(p: Point);

}
```

构造函数 `Point` 具有对应声明的类型：

```typescript
var Point: {

  new(x: number, y: number): Point;

  origin: Point;

  distance(p1: Point, p2: Point): number;

}
```

### 8.4.1 成员变量声明

成员变量声明声明实例成员变量或静态成员变量。

`MemberVariableDeclaration:`

- `AccessibilityModifier` *opt* `static` *opt* `PropertyName` *TypeAnnotation* *opt* *Initializer* *opt* `;`

成员变量声明关联的类型以普通变量声明的方式确定（参见第 5.2 节）。

实例成员变量声明在类实例类型中引入一个成员，并可选地初始化类的属性。实例成员变量声明中的初始化器在类的每个新实例上执行一次，等同于构造函数中对 `this` 属性的赋值。在实例成员变量的初始化表达式中，`this` 是类实例类型。

静态成员变量声明在构造函数类型中引入一个属性，并可选地初始化构造函数对象。静态成员变量声明中的初始化器在包含的脚本或模块加载时执行一次。

实例成员变量的初始化表达式在类构造体的作用域内求值，但不允许引用构造函数的参数或局部变量。这意味着，在外部作用域中与构造函数参数或局部变量同名的实体在实例成员变量的初始化表达式中是不可访问的。

由于实例成员变量的初始化等同于构造函数中对 `this` 属性的赋值，以下示例：

```typescript
class Employee {

  public name: string;

  public address: string;

  public retired = false;

  public manager: Employee = null;

  public reports: Employee[] = [];

}
```

等同于：

```typescript
class Employee {

  public name: string;

  public address: string;

  public retired: boolean;

  public manager: Employee;

  public reports: Employee[];

  constructor() {

    this.retired = false;

    this.manager = null;

    this.reports = [];

  }

}
```

### 8.4.2 成员函数声明

成员函数声明声明了一个实例成员函数或静态成员函数。

`MemberFunctionDeclaration`:

- `AccessibilityModifier` `static`*opt* `PropertyName` `CallSignature` `{` `FunctionBody` `}`
- `AccessibilityModifier` `static`*opt* `PropertyName` `CallSignature` `;`

成员函数声明的处理方式与普通函数声明（第 6 节）相同，不同之处在于成员函数中的 `this` 具有已知的类型。

对同一成员函数的所有声明必须指定相同的访问权限（`public`、`private` 或 `protected`）和类型（实例或静态）。

实例成员函数声明在类实例类型中声明一个属性，并在类原型对象的属性上分配一个函数对象。在实例成员函数声明的体内，`this` 的类型为类实例类型。

静态成员函数声明在构造函数类型中声明一个属性，并在类的构造函数对象的属性上分配一个函数对象。在静态成员函数声明的体中，`this` 的类型为构造函数类型。

成员函数可以使用 `super` 属性访问（第 4.9.2 节）访问被覆盖的基类成员。例如：

```typescript
class Point {

  constructor(public x: number, public y: number) { }

  public toString() {

    return "x=" + this.x + " y=" + this.y;

  }

}

class ColoredPoint extends Point {

  constructor(x: number, y: number, public color: string) {

    super(x, y);

  }

  public toString() {

    return super.toString() + " color=" + this.color;

  }

}
```

在静态成员函数中，`this` 代表调用该静态成员函数的构造函数。因此，对 `new this()` 的调用可能会调用派生类的构造函数：

```typescript
class A {

  a = 1;

  static create() {

    return new this();

  }

}

class B extends A {

  b = 2;

}

var x = A.create(); // new A()

var y = B.create(); // new B()
```

注意，`TypeScript` 不要求或验证派生构造函数是基类构造函数的子类型。换句话说，将 `B` 的声明改为：

```typescript
class B extends A {
  constructor(public b: number) {
    super();
  }
}
```

并不会导致示例产生错误，尽管从 `create` 到构造函数的调用没有指定参数（给 `b` 赋值为 `undefined`）。

### 8.4.3 成员访问器声明

成员访问器声明声明了一个实例访问器或静态成员访问器。

`MemberAccessorDeclaration`:

- `AccessibilityModifier` `static`*opt* `GetAccessor`
- `AccessibilityModifier` `static`*opt* `SetAccessor`

`get` 和 `set` 访问器的处理方式与对象字面量中的（第 4.5 节）相同，不同之处在于成员访问器中永远无法使用上下文类型。同一成员名的访问器必须指定相同的访问权限。

实例成员访问器声明在类实例类型中声明一个属性，并在类原型对象上定义一个具有 `get` 或 `set` 访问器的属性。在成员访问器声明的体内，`this` 的类型为类实例类型。

静态成员访问器声明在构造函数类型中声明一个属性，并在类的构造函数对象上定义一个具有 `get` 或 `set` 访问器的属性。在静态成员访问器声明的体内，`this` 的类型为构造函数类型。

`get` 和 `set` 访问器在生成的 `JavaScript` 中被发射为对 `Object.defineProperty` 的调用，如 8.6.1 节所述。

### 8.4.4 动态属性声明

如果属性成员声明的 `PropertyName` 是一个不表示已知符号（2.2.3 节）的计算属性名，则该结构被视为**动态属性声明**。以下规则适用于动态属性声明：

- 动态属性声明不会在类实例类型或构造函数类型中引入属性。
- 动态属性赋值的属性名表达式的类型必须是 `Any` 或 `String`、`Number` 或 `Symbol` 原始类型。
- 如果属性名表达式的类型为 `Any` 或 `Number` 原始类型，则与动态属性声明关联名称被视为数字属性名。

## 8.5 索引成员声明

索引成员声明在类实例类型中引入了索引签名（第 3.9.4 节）。

`IndexMemberDeclaration`:

- `IndexSignature` `;`



索引成员声明没有体且不能指定访问修饰符。类声明最多可以有一个字符串索引成员声明和一个数字索引成员声明。所有类成员必须满足第 3.9.4 节中索引成员的约束。

在构造函数侧声明索引成员是不可能的。当以数组方式使用类时，数字索引签名对于类的实例属性是有用的。

## 代码生成

当输出目标为 ECMAScript 6 或更高版本时，类型参数、实现子句、访问修饰符和成员变量声明将被移除，其他类声明将按原文发射。当输出目标为 ECMAScript 3 或 5 时，将进行更全面的重写，如本节所述。

### 不带 `extends` 的类

没有 `extends` 子句的类生成的 JavaScript 等于以下：

```javascript
var <ClassName> = (function () {
  function <ClassName>(<ConstructorParameters>) {
    <DefaultValueAssignments>
    <ParameterPropertyAssignments>
    <MemberVariableAssignments>
    <ConstructorStatements>
  }
  <MemberFunctionStatements>
  <StaticVariableAssignments>
  return <ClassName>;
})();
```

*ClassName* 是类的名称。*ConstructorParameters* 是构造函数参数的逗号分隔列表。*DefaultValueAssignments* 是对应于第 6.6 节为普通函数声明生成的默认属性赋值。

*ParameterPropertyAssignments* 是构造函数中每个属性声明的赋值，按声明顺序排列，格式为`this.<ParameterName> = <ParameterName>;`，其中 *ParameterName* 是参数的名称。

*MemberVariableAssignments* 是每个带有初始化器的实例成员变量声明的赋值，按声明顺序排列，格式为`this.<MemberName> = <InitializerExpression>;`，其中 *MemberName* 是成员变量的名称，*InitializerExpression* 是初始化表达式生成的代码。

*ConstructorStatements* 是为构造体中语句生成的代码。

*MemberFunctionStatements* 是每个成员函数声明或成员访问器声明的语句序列，按其声明顺序排列。

```javascript
Object.defineProperty(<ClassName>.prototype, "<MemberName>", {
  get: function () {
    <GetAccessorStatements>
  },
  set: function (<ParameterName>) {
    <SetAccessorStatements>
  },
  enumerable: true,
  configurable: true
};
```

以及 get 或 set 静态成员访问器声明，或者一对同名的 get 和 set 静态成员访问器声明，会生成形式如下的语句：

```javascript
Object.defineProperty(<ClassName>, "<MemberName>", {
  get: function () {
    <GetAccessorStatements>
  },
  set: function (<ParameterName>) {
    <SetAccessorStatements>
  },
  enumerable: true,
  configurable: true
};
```

其中 *MemberName* 是访问器的名称，*GetAccessorStatements* 是为 get 访问器函数体中的语句生成的代码，*ParameterName* 是 set 访问器参数的名称，*SetAccessorStatements* 是为 set 访问器函数体中的语句生成的代码。只有在声明了 get 访问器时才包含'get'属性，只有在声明了 set 访问器时才包含'set'属性。

*StaticVariableAssignments* 是一系列语句，对于每个带有初始化器的静态成员变量声明，按照它们的声明顺序生成，其形式如下：

```javascript
<ClassName>.<MemberName> = <InitializerExpression>;
```

其中 *MemberName* 是静态变量的名称，*InitializerExpression* 是为初始化表达式生成的代码。

### 带有 `extends` 子句的类

带有 `extends` 子句的类会生成等同的 JavaScript：

```javascript
var <ClassName> = (function (_super) {
  __extends(<ClassName>, _super);
  function <ClassName>(<ConstructorParameters>) {
    <DefaultValueAssignments>
    <SuperCallStatement>
    <ParameterPropertyAssignments>
    <MemberVariableAssignments>
    <ConstructorStatements>
  }
  <MemberFunctionStatements>
  <StaticVariableAssignments>
  return <ClassName>;
})<BaseClassName>);
```

此外，下方的 `__extends` 函数会在 JavaScript 源文件的开头输出。它将所有属性从基类构造函数对象复制到派生构造函数对象（以继承静态成员），并相应地建立派生构造函数对象的'prototype'属性。

```javascript
var __extends = this.__extends || function(d, b) {
  for (var p in b) if (b.hasOwnProperty(p)) d[p] = b[p];
  function f() { this.constructor = d; }
  f.prototype = b.prototype;
  d.prototype = new f();
};
```

*BaseClassName* 是 `extends` 子句中指定的类名。

如果类没有显式声明构造函数，则 *SuperCallStatement* 的形式如下：

```javascript
_super.apply("this", arguments);
```

否则，如果构造函数需要以 super 调用开始（如 8.3.2 节所示），则存在 *SuperCallStatement*，其形式如下：

```javascript
_super.call("this", <SuperCallArguments>)
```

其中 *SuperCallArguments* 是 super 调用中指定的参数列表。注意，此调用位于为参数属性和带有初始化器的成员变量生成的代码之前。构造函数其他地方 super 调用会生成类似的代码，但为此类调用生成的代码将是 *ConstructorStatements* 部分的一部分。

构造函数、实例成员函数或实例成员访问器中的 super 属性访问生成等同于 JavaScript：

```javascript
_super.prototype.<PropertyName>
```

其中 *PropertyName* 是引用的基类属性的名称。当 super 属性访问出现在函数调用中，生成的 JavaScript 等同于：

```javascript
_super.prototype.<PropertyName>
```

其中 Arguments 是为属性调用生成的代码。

静态成员函数或静态成员访问器中的 super 属性访问生成等同于 JavaScript：

```javascript
_super.prototype.<PropertyName>
```

其中 *PropertyName* 是引用的基类属性的名称。当 super 属性访问出现在函数调用中，生成的 JavaScript 等同于：

```javascript
_super.prototype.<PropertyName>
```

其中 Arguments 是为属性生成的代码。

## 枚举 (Enums)

枚举类型是具有一组命名常量的 Number 原始类型的子类型。

### 枚举声明 (Enum Declarations)

一个枚举声明定义一个枚举类型以及一个枚举对象，其值是 Number 原始类型的子类型。

*EnumDeclaration:*

```typescript
const [opt] enum {
  [MemberName] = [InitializerExpression];
}
```

其中 *MemberName* 是枚举成员的名称，*InitializerExpression* 是为初始化表达式生成的代码。当枚举声明包含 `const` 修饰符时，被称为常量枚举声明。

例如：

```typescript
enum Color { Red, Green, Blue }
```

声明了 Number 原始类型的子类型'Color'，并且每个枚举对象都会自动生成一个"反向映射"（reverse mapping），如 9.5 节所述。反向映射为获取枚举值的字符串表示提供了方便的方法。例如：

```javascript
var c = Color.Red;
console.log(Color[c]); // 输出 "Red"
```

### 枚举成员 (Enum Members)

枚举体定义零或多个枚举成员，作为枚举类型的命名值。每个枚举成员都有与枚举声明引入的类型关联数值。

*EnumBody:*

```text
EnumMemberList [opt]
```

*EnumMemberList:*

```text
EnumMember
EnumMemberList [] EnumMember
```

*EnumMember:*

```text
PropertyName = EnumValue
```

*EnumValue:*

```text
AssignmentExpression
```

枚举成员的 *PropertyName* 不能是计算属性名（2.2.3）。枚举成员分为***常量成员***或***计算成员***。常量成员具有已知的常量值，会在生成的 JavaScript 代码中替换。计算成员的值在运行时计算，在编译时未知。对计算成员的引用不进行替换。

枚举成员分类如下：

- 如果枚举声明未指定值，则该成员被视为常量成员。如果该成员是枚举声明中的第一个成员，它被赋值为零；否则，它被赋值为前一个成员的值加一，如果前一个成员不是常量成员则发生错误。

- 如果枚举声明指定的值可以被分类为常量枚举表达式（见下文），则该成员被视为常量成员。

- 否则，该成员被视为计算成员。

枚举值表达式必须是 Any 类型、Number 原始类型或枚举类型本身。

**常量枚举表达式 (constant enum expression)** 是表达式语法中的一个可以在编译时完全求值的子集。如果一个表达式是常量枚举表达式，则它是以下之一：

135

- 一个数字字面量。

- 一个标识符或属性访问，表示在同一常量枚举声明中之前声明的成员。

- 一个带括号的常量枚举表达式。

- 应用于常量枚举表达式的`+`、`–`或`~`一元运算符。

- 应用于两个常量枚举表达式的`+`、`–`、`*`、`%`、`%`、`<<`、`>>`、`>>>`、`&`、`^`或`|`运算符。

在示例中：

```
enum Test {
  A,
  B,
  C = Math.floor(Math.random() * "1000"),
  D = "10",
  E
}
```

'A'、'B''D'和'E'分别是值为 0, 1, 10 和 11 的常量成员，而'C'是一个计算成员。

在示例中：

```
enum Style {
  None = "0",
  Bold = "1",
  Italic = "2",
  Underline = "4",
  Emphasis = Bold | Italic,
  Hyperlink = Bold | Underline
}
```

所有成员都是常量成员。注意，枚举成员声明可以在不限定的情况下引用其他枚举成员。此外，由于枚举是 Number 原始类型的子类型，可以使用数值运算符（如位或运算符`|`）来计算枚举值。

### 声明合并 (Declaration Merging)

枚举是"开放的"，相对于共同根节点（如第 2.3 节定义）具有相同限定名的枚举声明定义了单个枚举类型，并贡献于单个枚举对象。

一个枚举声明无法延续另一个枚举的自动编号序列，当一个枚举类型有多个声明时，仅允许一个声明省略第一个成员的值。

当枚举声明合并时，它们必须要么全部指定 `const` 修饰符，要么全部不指定 `const` 修饰符。

### 常量枚举声明

指定 `const` 修饰符的枚举声明是***常量枚举声明***。在常量枚举声明中，所有成员必须具有常量值，如果成员声明指定了一个未归类为常量枚举表达式的表达式，这是一个错误。

与普通枚举声明不同，常量枚举声明在生成的 JavaScript 代码中会被完全擦除。因此，在任何除选择枚举某个成员的属性访问之外的上下文中引用常量枚举对象都是错误的。例如：

```
const enum Comparison {
  LessThan = "-1",
  EqualTo = "0",
  GreaterThan = "1"
}

var x = Comparison.EqualTo; // OK，在生成的代码中替换为 0
var y = Comparison[Comparison.EqualTo]; // 错误
var z = Comparison; // 错误
```

整个 const 枚声明在生成的 JavaScript 代码中被擦除。因此，对枚举对象的唯一允许是被那些替换为枚举成员值的引用。

### 代码生成 (Code Generation)

枚举声明会生成等于以下内容的 JavaScript：

```
var <EnumName>;
(function (<EnumName>) {
  <EnumMemberAssignments>
})<EnumName>||(<EnumName>={}));
```

*EnumName* 是枚举的。

*EnumMemberAssignments* 是一系列赋值，每个枚举成员对应一个，按照它们的声明顺序进行，形式如下：

```
<EnumName>[<EnumName>["<MemberName>"] = <Value>] = "<MemberName>";
```

其中 *MemberName* 是枚举成员的名称，*Value* 是分配的常量值或为计算值表达式生成的代码。

例如，第 9.1 节中的'Color'枚举示例生成了以下 JavaScript：

```
var Color;
(function (Color) {
  Color[Color["Red"] = 0] = "Red";
  Color[Color["Green"] = 1] = "Green";
  Color[Color["Blue"] = 2] = "Blue";
})(Color||(Color={}));
```

## 命名空间 (Namespaces)

命名空间提供了一种在命名容器层次结构中组织代码和声明的机制。命名空间具有命名成员，每个成员表示一个值、类型、命名空间或它们的组合，这些成员可以是局部的或导出的。命名空间的体对应于执行一次的函数，从而提供了一种维护具有保证隔离性的本地状态的机制。命名空间可以被视为立即调用函数表达式（IIFE）模式的正式化。

### 命名空间声明 (Namespace Declarations)

命名空间声明引入了一个具有命名空间含义的名称，在实例化命名空间的情况下，在包含的声明空间中引入一个值的含义。

*NamespaceDeclaration:*

```
namespace <IdentifierPath> { <NamespaceBody> }
```

*IdentifierPath:*

```
namespace <IdentifierPath> { <NamespaceBody>
```

命名空间使用 `namespace` 关键字声明，但为了向后兼容，也可以使用 `module` 关键字。命名空间可以是***实例化的***或***未实例化的***。未实例化的命名空间是生成代码的。实例化的命名空间是执行的。当命名空间标识符作为 *NamespaceName*（第 3.8 节）引用时，它表示一个类型容器；当命名空间标识符作为 *PrimaryExpression*（第 4.3 节）引用时，它表示一个单例实例。例如：

```
namespace M {
  export interface a: number;
  export p: number;
}
```

上方，当'M'被用作 *PrimaryExpression* 时，它表示一个具有单一成员'a'的对象。如果'M'被用作 *NamespaceName*，它表示一个类型容器。示例中的最后一行是错误的，因为'm'是一个不能在类型名称中引用的变量。如果'M'的声明排除了导出的变量'a'，'M'将是一个未实例化的命名空间，作为 *PrimaryExpression* 引用它是错误的。指定具有多个标识符的 *IdentifierPath* 的命名空间声明等于一系列单标识符命名空间，除最外层之外自动导出。例如：



```typescript
namespace A {
  export namespace B {
    export namespace C {
      export var x = 1;
    }
  }
}
```

命名空间和命名类型形成的层次结构部分与命名空间实例和成员形成的层次结构镜像。示例：

```typescript
namespace A {
  export namespace B {
    export class C {}
  }
}
```

引入了限定名为 `A.B.C` 的命名类型，同时也引入了可以使用表达式 `A.B.C` 访问的构造函数。因此，在示例 `var c: A.B.C = new A.B.C();` 中，两个实际上引用的是不同的实体。上下文决定了 `A.B.C` 是被处理为类型名称还是表达式。

### 10.2 命名空间体（Namespace Body）

命名空间的体对应于执行一次的函数，用于初始化命名空间实例。

*NamespaceBody:*

*NamespaceElements**opt*

*NamespaceElements:*

*NamespaceElement*

*NamespaceElements* *NamespaceElement*

*NamespaceElement:*

*Statement*

*LexicalDeclaration*

*FunctionDeclaration*

*GeneratorDeclaration*

*ClassDeclaration*

*InterfaceDeclaration*

*TypeAliasDeclaration*

*EnumDeclaration*

*NamespaceDeclaration*

*AmbientDeclaration*

*ImportAliasDeclaration*

*ExportNamespaceElement*

*ExportNamespaceElement:*

`export` *VariableStatement*

`export` *LexicalDeclaration*

`export` *FunctionDeclaration*

`export` *GeneratorDeclaration*

`export` *ClassDeclaration*

`export` *InterfaceDeclaration*

`export` *TypeAliasDeclaration*

`export` *EnumDeclaration*

`export` *NamespaceDeclaration*

`export` *AmbientDeclaration*

`export` *ImportAliasDeclaration*

### 10.3 导入别名声明（Import Alias Declarations）

导入别名声明用于为其他命名空间中的实体创建本地别名。

142

*ImportAliasDeclaration:*

`import` *BindingIdentifier* `=` *EntityName* `;`

*EntityName:*

*NamespaceName*

*NamespaceName* `.` *IdentifierReference*

一个由单个标识符组成的 *EntityName* 被解析为 *NamespaceName*，因此要求引用一个命名空间。生成的本地别名引用给定的命名空间，其本身被归类为命名空间。

由多个标识符组成的 *EntityName* 被解析为 *NamespaceName*，后跟一个命名给定命名空间中导出的实体的标识符。生成的本地别名具有所引用实体的所有含义。（一个实体名称可能多达三个不同的含义——值、类型和命名空间。）实际上，这就像导入的实体使用该本地别名在本地被声明了一样。

在示例中：

```typescript
namespace A {
  export interface X {
    s: string;
  }

  export var X: X;
}

namespace B {
  interface A {
    n: number;
  }

  import Y = A; // 命名空间 A 的别名
  import Z = A.X; // 类型和值 A.X 的别名
  var v: Z = Z;
}
```

在 `B` 内部，`Y` 仅是命名空间 `A` 的别名，而不是本地接口 `A`，而 `Z` 是 `A.X` 所有导出含义的别名，因此同时表示一个接口类型和一个变量。

如果 *EntityName* 的 *NamespaceName* 部分引用了一个已实例化的命名空间，则在作为表达式求值时，*NamespaceName* 要求引用该命名空间实例。

在示例中：

```typescript
namespace A {
  export interface X {
    s: string;
  }
}

namespace B {
  var A = 1;
  import Y = A;
}
```

143

`Y` 是非实例化命名空间 `A` 的本地别名。如果 `A` 的声明发生变化，使得 `A` 变成一个实例化命名空间（例如通过在 `A` 中包含变量声明），则上述 `B` 中的导入语句将是一个错误，因为表达式 `A` 没有引用命名空间 `A` 的命名空间实例。

当导入语句包含导出修饰符时，本地别名的所有含义都会被导出。

## 10.4 导出声明（Export Declarations）

导出声明声明了一个外部可访问的命名空间成员。导出声明只是带有 `export` 关键字前缀的普通声明。

命名空间导出空间（第 2.3 节）的成员构成了命名空间的**导出成员集**。命名空间的**实例类型**是一个对象类型，它为命名空间导出成员集中的每个成员提供一个属性，用于表示一个值。

导出的成员依赖于一个（可能是空的）命名类型集合（第 3.7 节）。这些命名类型的可访问性至少要与导出的成员相同，否则将发生错误。

成员所依赖的命名类型是在下文定义的**直接依赖于**关系的传递闭包中出现的命名类型：

- 变量直接依赖于其类型注解中指定的 *Type*。
- 函数直接依赖于参数注解或返回类型注解中指定的每个 *Type*。
- 类直接依赖于作为类型参数约束指定的每个 *Type*、作为基类或实现接口指定的每个 *TypeReference*，以及构造函数参数类型注解、公共成员变量类型注解、公共函数参数或返回类型注解、公共成员访问器参数或返回类型注解，或索引签名类型注解中指定的每个 *Type*。
- 接口直接依赖于作为类型参数约束指定的每个 *Type*、作为基接口指定的每个 *TypeReference* 以及作为其主体的 *ObjectType*。
- 命名空间直接依赖于其导出的成员。
- *Type* 或 *ObjectType* 直接依赖于在任何嵌套级别的类型内部出现的每个 *TypeReference*。
- *TypeReference* 直接依赖于它所引用的类型以及作为类型参数指定的每个 *Type*。

一个具有根命名空间 *R*（第 2.3 节）的命名类型 *T* 被认为**至少可访问于**成员 *M*，如果：

- *R* 是全局命名空间或模块；或者
- *R* 是 *M* 父级命名空间链中的命名空间。

在示例中：

144

```typescript
interface A {
  x: string;
}

namespace M {
  export interface B {
    x: A;
  }

  export interface C {
    x: B;
  }

  export function foo(c: C) {
    …
  }
}
```

`foo` 函数依赖于命名类型 `A`、`B` 和 `C`。为了导出 `foo`，必须也导出 `B` 和 `C`，否则它们的可访问性将无法达到 `foo`。`A` 接口已经至少可访问于 `foo`，因为它是在 `foo` 命名空间的父级命名空间中声明的。

## 10.5 声明合并（Declaration Merging）

命名空间是“开放式”的，相对于公共根（如第 2.3 节定义）具有相同限定名的命名空间声明贡献于同一个命名空间。例如，以下关于命名空间 `outer` 的两个声明可能位于不同的源文件中。

文件 `a.ts`：

```typescript
namespace outer {
  var local = 1; // 非导出的本地变量
  export var a = local; // outer.a

  export namespace inner {
    export var x = 10; // outer.inner.x
  }
}
```

文件 `b.ts`：

```typescript
namespace outer {
  var local = 2; // 非导出的本地变量
  export var b = local; // outer.b

  export namespace inner {
    export var y = 20; // outer.inner.y
  }
}
```

假设这两个源文件属于同一个程序，这两个声明将具有全局命名空间公共根，因此贡献于同一个命名空间，其实例类型将是：

145

```typescript
{
  a: number;
  b: number;
  inner: {
    x: number;
    y: number;
  };
}
```

声明合并不适用于通过导入语句创建的别名。也就是说，在同一体内无法进行别名声明和命名空间声明。

*待澄清解析解析规则*

声明合并还扩展到相对于公共根具有相同限定名的函数、类或枚举声明的命名空间声明：

- 当函数与命名空间合并时，函数对象的类型与命名空间的实例类型合并。实际上，函数的重载或实现提供了调用签名，而命名空间的导出成员构成了组合类型的属性。
- 当类与命名空间合并时，构造函数对象的类型与命名空间的实例类型合并。实际上，类构造函数的重载或实现提供了构造签名，类的静态成员和命名空间的导出成员构成了组合类型的属性。静态成员与导出的命名空间成员具有相同名称将导致错误。
- 当枚举与命名空间合并时，枚举对象的类型与命名空间的实例类型合并。实际上，枚举的成员和命名空间的导出成员构成了组合类型的属性。枚举成员与导出的命名空间成员具有相同名称将导致错误。

当合并非环境函数或类声明与非环境命名空间声明时，该函数或类声明必须在同一个源文件中位于命名空间声明之前。这确保了共享的对象实例被创建为函数对象。（虽然可以在创建后向对象添加属性，但无法事后让对象变得“可调用”。）

示例：

```typescript
interface Point {
  x: number;
  y: number;
}
```

146

```typescript
function point(x: number, y: number): Point {
  return { x: x, y: y };
}

namespace point {
  export var origin = point(0, 0);

  export function equals(p1: Point, p2: Point) {
    return p1.x == p2.x && p1.y == p2.y;
  }
}

var p1 = point(0, 0);
var p2 = point.origin;
var b = point.equals(p1, p2);
```

将 `point` 声明为一个具有两个属性（`origin` 和 `equals`）的函数对象。注意，`point` 的命名空间声明位于函数声明之后。

## 10.6 代码生成

命名空间会生成 JavaScript 代码等同于以下代码：

```javascript
var <NamespaceName>;
(function(<NamespaceName>) {
  <NamespaceStatements>
})(<NamespaceName> || (<NamespaceName> = {}));
```

其中 *NamespaceName* 是命名空间的名称，*NamespaceStatements* 是为命名空间体中的语句生成的代码。*NamespaceName* 函数参数可以以一个或多个下划线开头，以确保该名称在函数体内部是唯一的。注意，整个命名空间被作为一个立即执行的匿名函数发射。这确保了局部变量位于它们自己的词法环境中，与周围上下文隔离。另外请注意，生成的函数不会创建并返回命名空间实例，而是扩展现有的实例（该实例可能在函数调用中刚刚创建）。这确保了命名空间可以相互扩展。

`import` 语句会生成如下形式的代码：

```javascript
var <Alias> = <EntityName>;
```

只有当导入的实体在导入命名空间体的某处作为 *PrimaryExpression*（主表达式）引用时，才会发射此代码。如果导入的实体仅作为 *TypeName*（类型名）或 *NamespaceName* 引用，则不会生成任何内容。这确保了在一个命名空间中声明的类型可以通过另一个命名空间中的导入别名进行引用，而不会产生运行时开销。

147

当变量被导出时，命名空间体中对该变量的所有引用将被替换为：

`<NamespaceName>.<VariableName>`

这有效地将变量提升为命名空间实例上的属性，并确保对该变量的所有引用都变为对该属性的引用。

当函数、类、枚举或命名空间被导出时，为实体生成的代码后面会跟随如下形式的赋值语句：

```javascript
<NamespaceName>.<EntityName> = <EntityName>;
```

这会将实体的引用拷贝到命名空间实例的属性上。

149

## 11 脚本与模块

TypeScript 支持 ECMAScript 6 模块，并支持针对 CommonJS、AMD 以及其他模块系统的向下代码生成。

### 11.1 程序与源文件

一个 TypeScript **程序** 由一个或多个源文件组成。

*SourceFile:*

- *ImplementationSourceFile*
- *DeclarationSourceFile*

*ImplementationSourceFile:*

- *ImplementationScript*
- *ImplementationModule*

*DeclarationSourceFile:*

- *DeclarationScript*
- *DeclarationModule*

扩展为 `.ts` 的源文件是**实现源文件**，包含语句和声明；扩展为 `.d.ts` 的源文件是**声明源文件**，仅包含声明。声明源文件是实现源文件的严格子集，用于以辅助的方式声明与现有 JavaScript 代码相关的静态类型信息。它们完全可选，但能够让 TypeScript 编译器和工具在 TypeScript 应用中集成现有 JavaScript 代码和库时，提供更好的验证和帮助。

当编译 TypeScript 程序时，程序的所有源文件将一起被处理。不同源文件中的语句和声明可以相互依赖，并且可能以循环的形式。默认情况下，编译时为每个实现源文件生成一个 JavaScript 输出文件，但声明源文件不会生成任何输出。

#### 11.1.1 源文件依赖

TypeScript 编译器会自动确定源文件的依赖关系，并将这些依赖包含在正在编译的程序中。这种确定是通过“引用注释”和模块导入声明完成的：

- 形式如 `/// <reference path="..."/>` 的注释增加了对路径参数中指定的源文件的依赖。该路径相对于包含它的源文件的目录进行解析。
- 指定相对模块名（第 11.3.1 节）的模块导入声明相对于包含它的源文件的目录解析该名称。如果存在结果路径且文件扩展名为 `.ts` 的源文件，则该文件将作为依赖添加。否则，如果存在结果路径且文件扩展名为 `.d.ts` 的源文件，则该文件将作为依赖添加。
- 作为依赖包含的任何文件，其引用将以传递方式进行分析，直到所有依赖关系都确定。

### 11.2 脚本

不包含模块导入或导出声明的源文件被分类为**脚本**。脚本形成**全局命名空间**，脚本中声明的实体在程序的任何地方都是可见的。

*ImplementationScript:*

- *ImplementationScriptElements**opt*

*ImplementationScriptElements:*

- *ImplementationScriptElement*
- *ImplementationScriptElements* *ImplementationScriptElement*

*ImplementationScriptElement:*

- *ImplementationElement*
- *AmbientModuleDeclaration*

*ImplementationElement:*

- *Statement*
- *LexicalDeclaration*
- *FunctionDeclaration*
- *GeneratorDeclaration*
- *ClassDeclaration*
- *InterfaceDeclaration*
- *TypeAliasDeclaration*
- *EnumDeclaration*
- *NamespaceDeclaration*
- *AmbientDeclaration*
- *ImportAliasDeclaration*

*DeclarationScript:*

- *DeclarationScriptElements**opt*

*DeclarationScriptElements:*

- *DeclarationScriptElement*



- `DeclarationScriptElements` `DeclarationScriptElement`

`DeclarationScriptElement:`

- `DeclarationElement`
- `AmbientModuleDeclaration`

`DeclarationElement:`

- `InterfaceDeclaration`
- `TypeAliasDeclaration`
- `NamespaceDeclaration`
- `AmbientDeclaration`
- `ImportAliasDeclaration`

构成全局命名空间的脚本的初始化顺序最终取决于生成的 JavaScript 文件在运行时加载顺序（例如，可以通过引用生成的 JavaScript 文件的 `<script>` 标签来控制）。

### 11.3 模块

包含至少一个模块导入或导出声明的源文件被视为独立的**模块**。模块中未导出的实体在该模块内可见，但导出的实体可以通过导入语句导入到其他模块。

`ImplementationModule:`

- `ImplementationModuleElements`<sub>opt</sub>

`ImplementationModuleElements:`

- `ImplementationModuleElement`
- `ImplementationModuleElements ImplementationModuleElement`

`ImplementationModuleElement:`

- `ImplementationElement`
- `ImportDeclaration`
- `ImportAliasDeclaration`
- `ImportRequireDeclaration`
- `ExportImplementationElement`
- `ExportDefaultImplementationElement`
- `ExportListDeclaration`
- `ExportAssignment`

`DeclarationModule:`

- `DeclarationModuleElements`<sub>opt</sub>

`DeclarationModuleElements:`

- `DeclarationModuleElement`
- `DeclarationModuleElements DeclarationModuleElement`

`DeclarationModuleElement:`

- `DeclarationElement`
- `ImportDeclaration`
- `ImportAliasDeclaration`
- `ExportDeclarationElement`
- `ExportDefaultDeclarationElement`
- `ExportListDeclaration`
- `ExportAssignment`

模块的初始化顺序取决于所使用的模块加载器，并不由 TypeScript 语言规定。

然而，通常情况下，非循环依赖的模块会按照正确的顺序加载并初始化。

模块还可以通过声明脚本中的 `AmbientModuleDeclarations`（环境模块声明）进行声明，在这些脚本中直接以字符串字面量指定模块名。这在 12.2 节中有进一步描述。

下面是两个在独立源文件中编写模块示例：

```typescript
// -------- main.ts --------
import { message } from "./log";

message("hello");

// -------- log.ts --------
export function message(s: string) {
  console.log(s);
}
```

`main` 模块中的导入声明引用了 `log` 模块，编译 `main.ts` 文件会导致 `log.ts` 文件作为程序的一部分被编译。

TypeScript 支持模块的多种 JavaScript 代码生成模式：

- **CommonJS**。这种格式被 Node.js 等服务器框架使用。
- **AMD**（异步模块定义）。这种格式被 RequireJS 等异步模块加载器使用。
- **UMD**（通用模块定义）。AMD 格式的一种变体，允许模块也能被 CommonJS 加载器加载。
- **System**。这种格式用于在降级环境中高保真度地表示 ECMAScript 6 语义。

所需的模块代码生成模式通过编译器选项选择，并且不会影响 TypeScript 源代码。事实上，可以编写模块，使其既可以被编译用于服务器端（例如使用 Node.js），也可以被编译用于客户端（使用符合 AMD 规范的加载器），而无需更改 TypeScript 源代码。

### 11.3.1 模块名

模块使用模块名进行标识和引用。以下定义与 CommonJS Modules 1.0 规范提供的定义一致。

- 模块名是由正斜杠分隔的项字符串。
- 模块名不能包含像 `.js` 的文件扩展名。
- 模块名可以是相对的或顶层的。如果第一个项是 `.` 或 `..`，则该模块名是相对的。
- 顶层名在概念模块命名空间的根部进行解析。
- 相对名相对于它们出现所在的模块名进行解析。

为了解析模块引用，TypeScript 为每个模块关联了一个文件路径。该文件路径仅仅是模块源文件的路径，不带文件扩展名。例如，包含在 `C:\src\lib\io.ts` 源文件中的模块文件路径为 `C:/src/lib/io`，包含在 `C:\src\ui\editor.d.ts` 源文件中的模块文件路径为 `C:/src/ui/editor`。

导入声明中的模块名解析如下：

- 如果导入声明指定了相对模块名，则该名相对于引用模块的文件路径进行解析。例如，在路径为 `C:/src/ui/main` 的模块中，`./editor` 和 `../lib/io` 引用相应的路径。除非程序中存在相应的模块，否则会报错。
- 如果导入声明指定了顶层名，且程序包含该命名的 `AmbientModuleDeclaration`（12.2 节），则引用该模块。
- 如果导入声明指定了顶层名，但程序中没有包含该模块，则相对于模块命名空间根部解析，否则会报错。

### 11.3.2 导入声明

导入声明用于从其他模块导入实体并在当前模块提供绑定。如下形式的 `import * as m from "mod";` 导入模块并创建本地绑定。本地绑定被分类为值和命名空间（代表模块本身）。

例如，声明 `import { x, y, z } from "mod";` 导入指定的成员。本地绑定与它们代表的实体具有相同的分类，除非使用 `as` 子句来指定不同的名称：

```typescript
import { x as a, y as b } from "mod";
```

如下形式的 `import default from "mod";` 等同于 `import { default as d } from "mod";`。

如下形式的 `import "mod";` 导入模块但不创建任何本地绑定（这在导入模块具有副作用时有用）。

### 11.3.3 Require 声明

Require 声明是为了兼容旧版本的 TypeScript。

`ImportRequireDeclaration:`

```typescript
import BindingIdentifier = require(StringLiteral);
```

Require 声明引入了一个引用给定模块的本地标识。`import require` 中的字符串字面量被解释为模块名（11.3.1 节）。声明引入的本地标识成为所导出实体的别名，其分类与其相同。具体来说，如果引用模块没有导出，该标识被分类为值和命名空间；如果引用模块有导出，则该标识与实体分类一致。

如下形式的 `import m = require("mod");` 等同于如下，前提是引用模块没有导出。

### 11.3.4 导出声明

导出声明声明一个或多个导出成员。模块的导出成员可以通过导入声明（11.3.2）在其他模块中导入。

#### 11.3.4.1 导出修饰符

在模块体中，可以通过包含 `export` 修饰符来导出声明的实体。

`ExportImplementationElement:`

```typescript
export VariableStatement
export LexicalDeclaration
export FunctionDeclaration
export GeneratorDeclaration
export ClassDeclaration
export InterfaceDeclaration
export TypeAliasDeclaration
export EnumDeclaration
export NamespaceDeclaration
export AmbientDeclaration
export ImportAliasDeclaration
```

`ExportDeclarationElement:`

```typescript
export InterfaceDeclaration
export TypeAliasDeclaration
export AmbientDeclaration
export ImportAliasDeclaration
```

除了在模块的本地声明空间中引入名称外，导出声明还在模块的导出声明空间中引入具有相同分类的相同名称。例如，声明：

```typescript
export function point(x: number, y: number) {
  return { x, y };
}
```

引入了本地名 `point` 和导出名 `point`，它们都引用该函数。

#### 11.3.4.2 默认导出声明

默认导出声明为导出一个名为 `default` 的实体提供了简写语法。

`ExportDefaultImplementationElement:`

```typescript
export default FunctionDeclaration
export default GeneratorDeclaration
export default ClassDeclaration
export default AssignmentExpression;
```

`ExportDefaultDeclarationElement:`

```typescript
export default AmbientFunctionDeclaration
export default AmbientClassDeclaration
export default IdentifierReference;
```

一个函数、生成器或类的 `ExportDefaultImplementationElement` 或 `ExportDefaultDeclarationElement` 会在包含它的模块的导出声明空间中引入一个名为 `default` 的值（在类的情况下则是引入一个名为 `default` 的类型）。该声明可以可选地为导出的函数、生成器或类指定一个本地名称。例如，该声明：

```typescript
export default function point(x: number, y: number) {
  return { x, y };
}
```

引入了本地名称 `point` 和一个导出的名称 `default`，它们都引用该函数。该声明在上等同于：

```typescript
function point(x: number, y: number) {
  return { x, y };
}

export default point;
```

这再次等同于：

```typescript
function point(x: number, y: number) {
  return { x, y };
}

export { point as default };
```

对于由单个标识符组成的表达式，其 `ExportDefaultImplementationElement` 或 `ExportDefaultDeclarationElement` 必须命名一个在当前模块或全局命名空间中定义的实体。该声明在包含它的模块的导出声明空间中引入一个名为 `default` 的实体，其分类与引用的实体相同。例如，以下声明：

```typescript
interface Point {
  x: number;
  y: number;
}

function Point(x: number, y: number): Point {
  return { x, y };
}

export default Point;
```

引入了本地名称 `Point` 和一个导出的名称 `default`，两者都具有值和类型含义。对于任何非单个标识符的表达式，其 `ExportDefaultImplementationElement` 会在包含它的模块的导出声明空间中引入一个名为 `default` 的值。例如，该声明：

```typescript
export default "hello";
```

引入了一个类型为 string 的名为 `default` 的导出值。

#### 11.3.4.3 导出列表声明（Export List Declarations）

导出列表声明从当前模块或指定的模块导出一个或多个实体。

`ExportListDeclaration:`

```typescript
export * FromClause;
export ExportClause FromClause;
export ExportClause;
```

不带 `FromClause` 的 `ExportListDeclaration` 导出当前模块中的实体。在如下形式的声明中：

```typescript
export { x };
```

名称 `x` 必须引用当前模块或全局命名空间中定义的实体，该声明在包含它的模块的导出声明空间中引入一个具有相同名称和含义的实体。

带有 `FromClause` 的 `ExportListDeclaration` 重新导出指定模块中的实体。在如下形式的声明中：

```typescript
export { x } from "mod";
```

名称 `x` 必须引用指定模块导出成员集中的实体，该声明在包含它的模块的导出声明空间中引入一个具有相同名称和含义的实体。不会为 `x` 创建本地绑定。

`ExportListDeclaration` 的 `ExportClause` 可以指定多个实体，并可能可选地指定用于导出实体的不同名称。例如，该声明：

```typescript
export { x, y as b, z as c };
```

在包含它的模块的导出声明空间中引入名为 `x`、`b` 和 `c` 的实体，其含义分别与命名为 `x`、`y` 和 `z` 的本地实体相同。

指定 `*` 代替 `ExportClause` 的 `ExportListDeclaration` 被称为**导出星（export star）声明**。导出星声明重新导出指定模块的所有成员。

```typescript
export * from "mod";
```

显式导出的成员优先于使用导出星声明重新导出的成员，如后续章节所述。

#### 11.3.4.4 导出成员集（Export Member Set）

特定模块的**导出成员集**确定方法是：从一个空成员集 `E` 和一个空已处理模块集 `P` 开始，然后按照下面的描述处理模块以形成 `E` 中完整的导出成员集。处理模块 `M` 包含以下步骤：

- 将 `M` 添加到 `P`。
- 将 `M` 导出声明空间中每个名称不在 `E` 中的成员添加到 `E` 中。
- 对于 `M` 中的每个导出星声明，按照声明顺序，如果所引用的模块尚在 `P` 中，则处理该模块。

模块的**实例类型（instance type）**是一个对象类型，模块导出成员集中的每个成员都有一个属性来表示一个值。

如果一个模块包含导出赋值（export assignment），则该模块包含导出声明是错误的。这两种类型的导出是互斥的。

### 11.3.5 导出赋值（Export Assignments）

导出赋值的存在是为了与早期版本的 TypeScript 保持兼容。导出赋值将模块成员指定为导出的实体，以代替模块本身。

`ExportAssignment:`

```typescript
export = IdentifierReference;
```

一个包含导出赋值的模块可以通过导入声明进行导入（11.3.3），该导入声明的本地别名引用赋值的实体。

一个包含导出赋值的模块也可以通过导入声明进行导入（11.3.2），前提是导出赋值被声明为命名空间。假设以下示例位于 `point.ts`：

```typescript
export = Point;

class Point {
  constructor(public x: number, public y: number) {
  }
}
```

当 `point.ts` 被导入到另一个模块时，导入别名引用导出的类，既可以作为类型也可以作为函数：



```typescript
import Pt = require("point");
var p = new Pt();
```

注意并不要求导入别名与导出实体使用相同的名称。

### 11.3.6 CommonJS 模块

CommonJS 模块定义了一种编写 JavaScript 模块的方法，具有私有性、导入其他模块的能力以及显式导出成员的能力。符合 CommonJS 的系统提供了一个 `require` 函数用于同步加载模块，以及一个可以添加属性的 `exports` 变量。1.3 节中的 `main` 和 `log` 示例生成如下 JavaScript：

**File main.js:**

```javascript
var log = require("log");
log.message("hello");
```

**File log.js:**

```javascript
exports.message = function(s) {
}
```

模块导入声明在生成的 JavaScript 中表示为由模块系统提供的 `require` 函数初始化的变量。只有当导入模块或引用该模块的本地别名（1.3）在导入模块体内作为 *PrimaryExpression* 被引用时，才会为特定的模块生成变量声明和 `require` 调用。如果导入模块仅作为 *NamespaceName* 或 *TypeQueryExpression* 被引用，则不产生任何内容。

一个示例：

**File geometry.ts:**

```typescript
export interface Point {
    x: number;
    y: number;
};

export function point(x: number, y: number): Point {
    return { x: x, y: y };
}
```

**File game.ts:**

```typescript
import g = require("geometry");
var p = g.point(10, 20);
```

`game` 模块在表达式中引用了导入的 `geometry` 模块（通过其别名 `g`），因此生成的 JavaScript 中包含了 `require` 调用：

```javascript
var g = require("geometry");
var p = g.point(10, 20);
```

如果 `game` 模块改为仅在类型位置引用 `geometry`：

```typescript
import g = require("geometry");
var p: g.Point = { x: 10, y: 20 };
```

则生成的 JavaScript 将不再依赖 `geometry` 模块，而简单的：

```javascript
var p = { x: 10, y: 20 };
```

### 11.3.7 AMD

异步模块定义（AMD）规范扩展了 CommonJS 规范，提供了一种用于编写具有关联依赖的异步加载模块的模式。使用 AMD 模式，模块被作为对全局 `define` 函数的调用输出，该函数接收一个依赖数组（指定为模块名称）以及一个包含模块主体的回调函数。全局 `define` 函数通过在应用程序中包含符合 AMD 标准的加载器来提供。加载器安排异步加载模块的依赖项，并在完成后调用回调函数，将解析后的模块实例作为参数传递，其顺序与在依赖数组中列出的顺序一致。

上面的 `main` 和 `log` 示例在编译为 AMD 模式时会生成以下 JavaScript 代码。

**File main.js:**

```javascript
define(["require", "exports", "./log"], function(require, exports, log) {
    log.message("hello");
});
```

**File log.js:**

```javascript
define(["require", "exports"], function(require, exports) {
    exports.message = function(s) {
        console.log(s);
    };
});
```

特殊的 `require` 和 `exports` 依赖项始终存在。根据需要向依赖数组和参数列表添加额外的条目以表示导入的模块。与 CommonJS 模块的代码生成类似，只有当导入的模块在导入模块的主体中作为 *PrimaryExpression* 被引用时，才会为该特定的导入模块生成依赖项。如果导入的模块仅作为 *NamespaceName* 被引用，则不会为该模块生成依赖项。

## 12 环境声明（Ambients）

环境声明（Ambient declarations）用于为现有的 JavaScript 代码提供静态类型。环境声明与普通声明的区别在于，它们不会生成任何 JavaScript 代码。环境声明并不是引入新的变量、函数、类、枚举或命名空间，而是为那些以“环境方式”存在并通过外部手段包含在程序中的实体提供类型信息，例如通过在 `<script/>` 标签中引用 JavaScript 库。

### 12.1 环境声明

环境声明使用 `declare` 关键字编写，可以声明变量、函数、类、枚举、命名空间或模块。

*AmbientDeclaration:*

```typescript
declare AmbientVariableDeclaration
declare AmbientFunctionDeclaration
declare AmbientClassDeclaration
declare AmbientEnumDeclaration
declare AmbientNamespaceDeclaration
```

#### 12.1.1 环境变量声明

环境变量声明在包含的声明空间中引入一个变量。

*AmbientVariableDeclaration:*

```typescript
var AmbientBindingList;
let AmbientBindingList;
const AmbientBindingList;
```

*AmbientBindingList:*

```text
AmbientBinding
AmbientBindingList, AmbientBinding
```

*AmbientBinding:*

```text
BindingIdentifier TypeAnnotationopt
```

环境变量声明可以包含一个类型注解。如果没有类型注解，则假设该变量的类型为 `Any`。

环境变量声明不允许存在初始化表达式。

#### 12.1.2 环境函数声明

环境函数声明在包含的声明空间中引入一个函数。

*AmbientFunctionDeclaration:*

```typescript
function BindingIdentifier CallSignature;
```

可以通过指定多个同名的环境函数声明来重载环境函数，但声明多个被认为相同（见第 3.11.2 节）或仅返回类型不同的重载是错误的。

环境函数声明不能指定函数体，且不允许默认参数值。

#### 12.1.3 环境类声明

环境类声明在包含的声明空间中声明一个类实例类型和一个构造函数。

*AmbientClassDeclaration:*

```typescript
class BindingIdentifier TypeParametersopt ClassHeritage {
    AmbientClassBody
}
```

*AmbientClassBody:*

```text
AmbientClassBodyElementsopt
```

*AmbientClassBodyElements:*

```text
AmbientClassBodyElement
AmbientClassBodyElements AmbientClassBodyElement
```

*AmbientClassBodyElement:*

```text
AmbientConstructorDeclaration
AmbientPropertyMemberDeclaration
IndexSignature
```

*AmbientConstructorDeclaration:*

```typescript
constructor(ParameterListopt);
```

*AmbientPropertyMemberDeclaration:*

```typescript
AccessibilityModifieropt staticopt PropertyName TypeAnnotationopt;
AccessibilityModifieropt staticopt PropertyName CallSignature;
```

#### 12.1.4 环境枚举声明

环境枚举在语法上与非环境枚举声明等价。

*AmbientEnumDeclaration:*

```text
EnumDeclaration
```

环境枚举声明与非环境枚举声明有两点不同：

- 在环境枚举声明中，枚举成员声明中指定的所有值必须被归类为常量枚举表达式。
- 在未指定 `const` 修饰符的环境枚举声明中，枚举成员声明被视为计算属性（而不是具有赋值值）。

环境枚举声明的处理方式与非环境枚举声明相同。

#### 12.1.5 环境命名空间声明

环境命名空间声明一个命名空间。

*AmbientNamespaceDeclaration:*

```typescript
namespace IdentifierPath {
    AmbientNamespaceBody
}
```

*AmbientNamespaceBody:*

```text
AmbientNamespaceElementsopt
```

*AmbientNamespaceElements:*

```text
AmbientNamespaceElement
AmbientNamespaceElements AmbientNamespaceElement
```

*AmbientNamespaceElement:*

```text
exportopt AmbientVariableDeclaration
exportopt AmbientLexicalDeclaration
exportopt AmbientFunctionDeclaration
exportopt AmbientClassDeclaration
exportopt InterfaceDeclaration
exportopt AmbientEnumDeclaration
exportopt AmbientNamespaceDeclaration
exportopt ImportAliasDeclaration
```

除了 *ImportAliasDeclaration* 外，*AmbientNamespaceElements* 无论是否包含 `export` 修饰符总是声明导出实体。

### 12.2 环境模块声明

环境模块声明一个模块。此类声明仅允许出现在有助于全局命名空间（见 11.1 节）的源文件顶层。*StringLiteral* 必须指定一个顶级模块名。不允许相对模块名。

*AmbientModuleDeclaration:*

```typescript
declare module StringLiteral {
    DeclarationModule
}
```

环境模块声明中的 *ImportRequireDeclaration* 仅可以通过顶级模块名引用其他模块。不允许相对模块名。

如果环境模块声明包含导出赋值，则模块内的任何声明指定 `export` 修饰符都是错误的。如果环境模块声明不包含赋值，模块中声明的实体无论其是否包含 `export` 修饰符都会导出。

环境模块是“开放”的，具有相同字符串字面量的环境模块声明贡献于同一个模块。例如，以下两个对模块 `io` 的声明可能位于不同的源文件中。

```typescript
declare module "io" {
    export function readFile(filename: string): string;
}

declare module "io" {
    export function writeFile(filename: string, data: string): void;
}
```

这的效果与单一的组合声明相同。

## 语法

本附录包含了正文中描述的语法的总结。如第 2.1 节所述，TypeScript 语法是 ECMAScript 语言规范（特别是 ECMA-262 标准第 6 版）中定义语法的超集，本附录仅列出了与 ECMAScript 语法相比、新的或经过修改的产生式。

### A.1 类型

*TypeParameters:*

```text
< TypeParameterList >
```

*TypeParameterList:*

```text
TypeParameter
TypeParameterList, TypeParameter
```

*TypeParameter:*

```text
BindingIdentifier Constraintopt
```

*Constraint:*

```text
extends Type
```

*TypeArguments:*

```text
< TypeArgumentList >
```

*TypeArgumentList:*

```text
TypeArgument
TypeArgumentList, TypeArgument
```

*TypeArgument:*

```text
Type
```

*Type:*

```text
UnionOrIntersectionOrPrimaryType
FunctionType
ConstructorType
```

*UnionOrIntersectionOrPrimaryType:*

```text
UnionType
IntersectionOrPrimaryType
```

*IntersectionOrPrimaryType:*

```text
IntersectionType
PrimaryType
```

*PrimaryType:*

```text
ParenthesizedType
PredefinedType
TypeReference
ObjectType
ArrayType
TupleType
TypeQuery
```

*ParenthesizedType:*

```text
(Type)
```

*PredefinedType:*

```text
any
number
boolean
string
symbol
void
```

*TypeReference:*

```text
TypeName [no LineTerminator here] TypeArgumentsopt
```

*TypeName:*

```text
IdentifierReference
NamespaceName . IdentifierReference
```

*NamespaceName:*

```text
IdentifierReference
NamespaceName . IdentifierReference
```

*ObjectType:*

```text
{ TypeBodyopt }
```

*TypeBody:*

```text
TypeMemberList;opt
TypeMemberList,opt
```

*TypeMemberList:*

```text
TypeMember
TypeMemberList; TypeMember
TypeMemberList, TypeMember
```

*TypeMember:*

```text
PropertySignature
CallSignature
ConstructSignature
IndexSignature
MethodSignature
```

*ArrayType:*

```text
PrimaryType [no LineTerminator here] [ ]
```

*TupleType:*

```text
[ TupleElementTypes ]
```

*TupleElementTypes:*

```text
TupleElementType
TupleElementTypes, TupleElementType
```

*TupleElementType:*

```text
Type
```

*UnionType:*

```text
UnionOrIntersectionOrPrimaryType | IntersectionOrPrimaryType
```

*IntersectionType:*

```text
IntersectionOrPrimaryType & PrimaryType
```

*FunctionType:*

```text
TypeParametersopt (ParameterListopt) => Type
```

*ConstructorType:*

```text
new TypeParametersopt (ParameterListopt) => Type
```

*TypeQuery:*

```text
typeof TypeQueryExpression
```

*TypeQueryExpression:*

```text
IdentifierReference
TypeQueryExpression . IdentifierName
```

*PropertySignature:*

```text
PropertyName ?opt TypeAnnotationopt
```

*PropertyName:*

```text
IdentifierName
StringLiteral
NumericLiteral
```

*TypeAnnotation:*

```text
: Type
```

*CallSignature:*

```text
TypeParametersopt (ParameterListopt) TypeAnnotationopt
```

*ParameterList:*

```text
RequiredParameterList
OptionalParameterList
RestParameter
RequiredParameterList, OptionalParameterList
RequiredParameterList, RestParameter
OptionalParameterList, RestParameter
RequiredParameterList, OptionalParameterList, RestParameter
```

*RequiredParameterList:*

```text
RequiredParameter
OptionalParameterList, RequiredParameter
```

*OptionalParameter:*

```text
AccessibilityModifieropt BindingIdentifierOrPattern TypeAnnotationopt
BindingIdentifier : StringLiteral
```

*AccessibilityModifier:*

```typescript
public
private
protected
```

*BindingIdentifierOrPattern:*

```text
BindingIdentifier
BindingPattern
```

*OptionalParameterList:*

```text
OptionalParameter
OptionalParameterList, OptionalParameter
```

*OptionalParameter:*

```text
AccessibilityModifieropt BindingIdentifierOrPattern ? TypeAnnotationopt
AccessibilityModifieropt BindingIdentifierOrPattern TypeAnnotationopt Initializer
BindingIdentifier ? : StringLiteral
```

*RestParameter:*

```text
... BindingIdentifier TypeAnnotationopt
```

*ConstructSignature:*

```text
new TypeParametersopt (ParameterListopt) TypeAnnotationopt
```

*IndexSignature:*

```text
[ BindingIdentifier : string ] TypeAnnotation
[ BindingIdentifier : number ] TypeAnnotation
```

*MethodSignature:*

```text
PropertyName ?opt CallSignature
```

*TypeAliasDeclaration:*

```text
type BindingIdentifier TypeParametersopt = Type;
```

### A.2 表达式

*PropertyDefinition:*

```text
IdentifierReference
InitializedName
PropertyName : AssignmentExpression
PropertyName CallSignature { FunctionBody }
```

*GetAccessor:*

```text
SetAccessor
```

*GetAccessor:*

```typescript
get PropertyName() TypeAnnotationopt {
    FunctionBody
}
```

*SetAccessor:*

```typescript
set PropertyName(BindingIdentifierOrPattern TypeAnnotationopt) {
    FunctionBody
}
```

*FunctionExpression:*

```typescript
function BindingIdentifieropt CallSignature {
    FunctionBody
}
```

*FormalParameters:*

```text
CallSignature
```

*Arguments:*

```text
TypeArgumentsopt (ArgumentListopt)
```

*UnaryExpression:*

```text
<Type> UnaryExpression
```

### A.3 语句

*Declaration:*

```text
InterfaceDeclaration
TypeAliasDeclaration
EnumDeclaration
```

*VariableDeclaration:*

```text
SimpleVariableDeclaration
DestructuringVariableDeclaration
```

*SimpleVariableDeclaration:*

```text
BindingIdentifier TypeAnnotationopt Initializeropt
```

*DestructuringVariableDeclaration:*

```text
BindingPattern TypeAnnotationopt Initializer
```

*LexicalBinding:*

```text
SimpleLexicalBinding
DestructuringLexicalBinding
```

*SimpleLexicalBinding:*

```text
BindingIdentifier TypeAnnotationopt Initializeropt
```

*DestructuringLexicalBinding:*

```text
BindingPattern TypeAnnotationopt Initializeropt
```

### A.4 函数

*FunctionDeclaration:*

```typescript
function BindingIdentifieropt CallSignature {
    FunctionBody
}

function BindingIdentifieropt CallSignature;
```

### A.5 接口

*InterfaceDeclaration:*

```typescript
interface BindingIdentifier TypeParametersopt InterfaceExtendsClauseopt ObjectType
```

*InterfaceExtendsClause:*

```text
extends ClassOrInterfaceTypeList
```

*ClassOrInterfaceTypeList:*

```text
ClassOrInterfaceType
ClassOrInterfaceTypeList, ClassOrInterfaceType
```

*ClassOrInterfaceType:*

```text
TypeReference
```

### A.6 类

*ClassDeclaration:*

```typescript
class BindingIdentifieropt TypeParametersopt ClassHeritage {
    ClassBody
}
```

*ClassHeritage:*

```text
ClassExtendsClauseopt ImplementsClauseopt
```

*ClassExtendsClause:*

```text
extends ClassType
```

*ClassType:*

```text
TypeReference
```

*ImplementsClause:*

```text
implements ClassOrInterfaceTypeList
```

*ClassElement:*

```text
ConstructorDeclaration
PropertyMemberDeclaration
IndexMemberDeclaration
```

*ConstructorDeclaration:*

```typescript
AccessibilityModifieropt constructor(ParameterListopt) {
    FunctionBody
}

AccessibilityModifieropt constructor(ParameterListopt);
```

*PropertyMemberDeclaration:*

```text
MemberVariableDeclaration
MemberFunctionDeclaration
MemberAccessorDeclaration
```

*MemberVariableDeclaration:*

```text
AccessibilityModifieropt staticopt PropertyName TypeAnnotationopt Initializeropt;
```

*MemberFunctionDeclaration:*

```typescript
AccessibilityModifieropt staticopt PropertyName CallSignature {
    FunctionBody
}

AccessibilityModifieropt staticopt PropertyName CallSignature;
```

*MemberAccessorDeclaration:*

```text
AccessibilityModifieropt staticopt GetAccessor
AccessibilityModifieropt staticopt SetAccessor
```

*IndexMemberDeclaration:*

```text
IndexSignature;
```

### A.7 枚举

*EnumDeclaration:*

```typescript
constopt enum BindingIdentifier {
    EnumBodyopt
}
```

*EnumBody:*

```text
EnumMemberList,opt
```

*EnumMemberList:*

```text
EnumMember
EnumMemberList, EnumMember
```

*EnumMember:*

```text
PropertyName
PropertyName = EnumValue
```

*EnumValue:*

```text
AssignmentExpression
```

### A.8 命名空间

*NamespaceDeclaration:*

```typescript
namespace IdentifierPath {
    NamespaceBody
}
```

*IdentifierPath:*

```text
BindingIdentifier
IdentifierPath . BindingIdentifier
```

*NamespaceBody:*

```text
NamespaceElementsopt
```

*NamespaceElements:*

```text
NamespaceElement
NamespaceElements NamespaceElement
```

*NamespaceElement:*

```text
Statement
LexicalDeclaration
FunctionDeclaration
GeneratorDeclaration
ClassDeclaration
InterfaceDeclaration
TypeAliasDeclaration
EnumDeclaration
NamespaceDeclaration
AmbientDeclaration
ImportAliasDeclaration
ExportNamespaceElement
```

*ExportNamespaceElement:*

```typescript
export VariableStatement
export LexicalDeclaration
export FunctionDeclaration
export GeneratorDeclaration
export ClassDeclaration
export InterfaceDeclaration
export TypeAliasDeclaration
export EnumDeclaration
export NamespaceDeclaration
export AmbientDeclaration
export ImportAliasDeclaration
```

*ImportAliasDeclaration:*

```typescript
import BindingIdentifier = EntityName;
```

*EntityName:*

```text
NamespaceName
NamespaceName . IdentifierReference
```

### A.9 脚本与模块

*SourceFile:*

```text
ImplementationSourceFile
DeclarationSourceFile
```

*ImplementationSourceFile:*

```text
ImplementationScript
ImplementationModule
```

*DeclarationSourceFile:*

```text
DeclarationScript
DeclarationModule
```

*ImplementationScript:*

```text
ImplementationScriptElements?
```

*ImplementationScriptElements:*

```text
ImplementationScriptElement
ImplementationScriptElements ImplementationScriptElement
```

*ImplementationScriptElement:*

```text
ImplementationElement
AmbientModuleDeclaration
```

*ImplementationElement:*

```text
Statement
LexicalDeclaration
FunctionDeclaration
GeneratorDeclaration
ClassDeclaration
InterfaceDeclaration
TypeAliasDeclaration
EnumDeclaration
NamespaceDeclaration
AmbientDeclaration
ImportAliasDeclaration
```

*DeclarationScript:*

```text
DeclarationScriptElements?
```

*DeclarationScriptElements:*

```text
DeclarationScriptElement
DeclarationScriptElements DeclarationScriptElement
```

*DeclarationScriptElement:*

```text
DeclarationElement
AmbientModuleDeclaration
```

*DeclarationElement:*

```text
InterfaceDeclaration
TypeAliasDeclaration
NamespaceDeclaration
AmbientDeclaration
ImportAliasDeclaration
```

*ImplementationModule:*

```text
ImplementationModuleElements?
```

*ImplementationModuleElements:*

```text
ImplementationModuleElement
ImplementationModuleElements ImplementationModuleElement
```

*ImplementationModuleElement:*

```text
ImplementationElement
ImportDeclaration
ImportAliasDeclaration
ImportRequireDeclaration
ExportImplementationElement
ExportDefaultImplementationElement
ExportListDeclaration
ExportAssignment
```

*DeclarationModule:*

```text
DeclarationModuleElements?
```

*DeclarationModuleElements:*

```text
DeclarationModuleElement
DeclarationModuleElements DeclarationModuleElement
```

*DeclarationModuleElement:*

```text
DeclarationElement
ImportDeclaration
ImportAliasDeclaration
ExportDeclarationElement
ExportDefaultDeclarationElement
ExportListDeclaration
ExportAssignment
```

*ImportRequireDeclaration:*

```typescript
import BindingIdentifier = require(StringLiteral);
```

*ExportImplementationElement:*

```typescript
export VariableStatement
export LexicalDeclaration
export FunctionDeclaration
export GeneratorDeclaration
export ClassDeclaration
export InterfaceDeclaration
export TypeAliasDeclaration
export EnumDeclaration
export NamespaceDeclaration
export AmbientDeclaration
export ImportAliasDeclaration
```

*ExportDeclarationElement:*

```typescript
export InterfaceDeclaration
export TypeAliasDeclaration
export AmbientDeclaration
export ImportAliasDeclaration
```

*ExportDefaultImplementationElement:*

```typescript
export default FunctionDeclaration
export default GeneratorDeclaration
export default ClassDeclaration
export default Expression;
```

*ExportDefaultDeclarationElement:*

```typescript
export default FunctionDeclaration
export default ClassDeclaration
export default IdentifierReference;
```

*ExportListDeclaration:*

```typescript
export FromClause;
export FromClause;
export FromClause;
```

*ExportAssignment:*

```typescript
export = IdentifierReference;
```

### A.10 环境（Ambients）

*AmbientDeclaration:*

```typescript
declare VariableDeclaration
declare FunctionDeclaration
declare ClassDeclaration
declare EnumDeclaration
declare NamespaceDeclaration
```

*AmbientVariableDeclaration:*

```typescript
var BindingList;
let BindingList;
const BindingList;
```

*AmbientBindingList:*

```text
AmbientBinding
AmbientBindingList, AmbientBinding
```

*AmbientBinding:*

```text
BindingIdentifier TypeAnnotation?
```

*AmbientFunctionDeclaration:*

```typescript
function BindingIdentifier CallSignature;
```

*AmbientClassDeclaration:*

```typescript
class BindingIdentifier TypeParameters? ClassHeritage {
    AmbientClassBody
}
```

*AmbientClassBody:*

```text
AmbientClassElements?
```

*AmbientClassElements:*

```text
AmbientClassElement
AmbientClassElements AmbientClassElement
```

*AmbientClassElement:*

```text
AmbientConstructorDeclaration
AmbientPropertyMemberDeclaration
IndexSignature
```

*AmbientConstructorDeclaration:*

```typescript
constructor(ParameterList?);
```

*AmbientPropertyMemberDeclaration:*

```text
AccessibilityModifier? static? PropertyName TypeAnnotation?;
AccessibilityModifier? static? PropertyName CallSignature;
```

*AmbientEnumDeclaration:*

```text
EnumDeclaration
```

*AmbientNamespaceDeclaration:*

```typescript
namespace IdentifierPath {
    AmbientNamespaceBody
}
```

*AmbientNamespaceBody:*

```text
AmbientNamespaceElements?
```

*AmbientNamespaceElements:*

```text
AmbientNamespaceElement
AmbientNamespaceElements AmbientNamespaceElement
```

*AmbientNamespaceElement:*

```text
export? AmbientVariableDeclaration
export? AmbientLexicalDeclaration
export? AmbientFunctionDeclaration
export? AmbientClassDeclaration
export? InterfaceDeclaration
export? AmbientEnumDeclaration
export? AmbientNamespaceDeclaration
export? ImportAliasDeclaration
```

*AmbientModuleDeclaration:*

```typescript
declare module StringLiteral {
    DeclarationModule
}
```
