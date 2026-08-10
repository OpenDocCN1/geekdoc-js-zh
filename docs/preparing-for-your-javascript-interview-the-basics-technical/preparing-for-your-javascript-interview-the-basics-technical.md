# JavaScript 面试准备：基础知识：技术问题与答案 (你的技术面试)






## 引言

在今天，你不可能成为一名 Web 开发者却不知道 JavaScript。它最初是一个小小的客户端脚本语言，现在已演变成每个用户网络体验中无数框架和库的一部分。所有现代网络浏览器都实现了 JavaScript 语言，使其成为唯一部署在所有个人电脑和移动设备上的语言。

随着演进，JavaScript 拥抱了许多特性，如原型继承、模块、命名空间、匿名（lambda）函数、Promise 甚至甚至是元编程。得益于 Node.js 等框架，你现在甚至可以在服务器端使用它。

JavaScript 的增长给新开发者带来了挑战。一方面，入门门槛很低——任何人可以在浏览器中打开开发者工具窗口并开始编写 JavaScript。另一方面，当你开始探索庞大的 JavaScript 生态系统中可用的功能时，其复杂性会呈指数级增长。

现在，技术初筛包含 JavaScript 问题已成为常态。作为一名候选人，你应该从哪里开始学习呢？

其他书籍倾向于关注技术面试的编码部分，而本书旨在介绍候选人可能被要求口头解释或描述的一些常见基础性 JavaScript 面试题。本书专注于原生 JavaScript（Vanilla JS），涵盖了 JavaScript 数据结构、错误处理、UI 操作等基础知识！能够简洁且自信地回答这些问题将有助于你成为一名更出色的候选人。

祝你好运！



## 通用练习

本节重点关注原生 JavaScript 的基础。

## 问题：什么是 JavaScript？

JavaScript 通常缩写为 "JS"，是一种高级级、动态、无类型、解释型的运行时语言。

JavaScript 既是客户端也是服务器端的脚本语言，可以插入 HTML 页面并被网络浏览器理解。JavaScript 也可以是一种面向对象的编程语言。

## 问题：JavaScript 中的两种基本数据类型组是什么？

- 原生类型：string（字符串）、number（数字）、boolean（布尔）、null、undefined
- 复合类型：object（对象，包括函数）

## 问题：JavaScript 有哪些类型？

JavaScript 中只有**六** 种类型：Object（对象）、Number（数字）、String（字符串）、Boolean（布尔）、Null（空）和 Undefined（未定义）。

对象包括数组、函数和普通对象。

数字可以是整数或浮点数，或者是特殊值 NaN 和 Infinity。

字符串包括空字符串。

## 问题：哪家公司开发了 JavaScript？

Netscape（网景）是开发 JavaScript 的软件公司。

## 问题：什么是未声明（undeclared）和未定义（undefined）变量？

未声明变量是指那些在程序中不存在且未声明的变量。如果程序尝试读取未声明变量的值，就会遇到运行时错误。

未定义变量是指在程序中已声明但未赋予任何值的变量。如果程序尝试读取未定义变量的值，将返回一个未定义值（undefined）。

## 问题：什么是全局变量？

全局变量是在代码范围内可用的变量，也就是说它们没有作用域。使用 `var` 关键字声明局部变量或对象。如果省略了 `var` 关键字，则声明一个全局变量。

使用全局变量面临的问题是局部作用域和全局作用域变量名的冲突。此外，依赖全局变量的代码很难调试和测试。

## 问题：JavaScript 中的 `this` 关键字是什么？

`this` 关键字指向调用它的对象。

## 问题：`isNaN` 函数有什么用？

`isNaN` 函数在参数不是数字时返回 true，否则返回 false。

## 问题：什么是负无穷大（negative infinity）？

负无穷大是 JavaScript 中的一个数字，可以通过负数除以零得到。

## 问题：JavaScript 中用什么符号进行注释？

```javascript
// 用于单行注释

/* 多行
注释 */
```

## 问题：什么是 `===` 运算符？

`===` 称为严格相等运算符，当两个操作数在不进行任何类型转换的情况下具有相同值时返回 true。

## 问题：JavaScript 中的类型转换（typing）是指什么？

变量类型转换用于给字符串赋值数字。

## 问题：JavaScript 支持自动转换吗？

是的，JavaScript 支持自动转换。JavaScript 是一种“弱类型”语言，这意味着每当运算符或语句期望特定类型时，JavaScript 都会转换数据。

例如，自动转换经常用于检查 DOM 元素是否存在：

```javascript
var element = document.getElementById("whatever");
if(element) {
  // 元素存在
} else {
  // 元素不存在
}
```

## 问题：JavaScript 中的 NULL 代表什么？

NULL 值用于表示没有值或没有对象。在 API 中，当期望获得对象时通常会检索 null。

## 问题：JavaScript 中的 `undefined` 值代表什么？

**Undefined** 是 JavaScript 的原生类型之一。未赋值的变量类型为 undefined。如果一个方法语句尝试使用它，它也可能是 undefined。最后，如果函数没有返回任何值，则返回 undefined。

## 问题：JavaScript 中所有的循环结构有哪些？

回答：在 JavaScript 中，我们有以下循环语句：

| | 描述 |
| :--- | :--- |
| while | 只要条件为真就循环执行代码块 |
| do...while | 循环一次代码块，然后在条件为真时重复循环 |
| for | 运行指定次数的语句 |

## 问题：什么是 `break` 语句？

**break** 语句用于退出当前循环。

## 问题：什么是 `continue` 语句？

**continue** 语句继续执行循环的下一次语句。

## 问题：解释如何检测客户端机器的操作系统？

可以使用 `navigator.appVersion` 字符串（属性）来检测客户端的操作系统。

## 问题：`void(0)` 有什么用？

`void` 运算符计算给定的表达式并返回 undefined。`void(0)` 用于防止页面刷新。调用它时传入了参数“zero”。

## 问题：什么是转义字符？

JavaScript 使用反斜杠 `\` 作为转义字符，用于：

- \' 单引号
- \" 双引号
- \ 反斜杠
- \n 换行
- \r 回车
- \t 制表符
- \b 退键
- \f 进页
- \v 垂直制表
- \0 空字符

## 问题：解释 JavaScript 中的计时器是如何工作的。

JavaScript 代码通常是同步执行的。计时器允许我们延迟任意指令的执行：

### setTimeout()
如果你希望在指定的延迟后调用**一次**函数，通常使用 `setTimeout()` 函数。

### setInterval()
`setInterval()` 函数通常用于为执行多次的函数设置延迟。

### setImmediate()
在 IE 中，可以使用 `setImmediate()` 函数代替 `setTimeout(fn, 0)` 方法来执行耗时操作。





## 问题：typeof 运算符的用途是什么？

'typeof' 是一个运算符，用于返回变量类型的字符串描述。

| 类型 | 结果 |
| --- | --- |
| Undefined | 'undefined' |
| Null | 'object'（见下文） |
| Boolean | 'boolean' |
| Number | 'number' |
| String | 'string' |
| Symbol (ECMAScript 2015 新增) | 'symbol' |
| 主机对象（JS 环境提供） | 取决于实现 |
| 函数对象（在 ECMA-262 术语中实现 [[Call]]） | 'function' |
| 其他任何对象 | 'object' |

## 问题：哪些关键字用于处理异常？

try/catch/finally 语句用于处理代码块中可能发生的部分或全部错误，同时继续执行代码。

`try` 语句允许你定义一个代码块，在执行时对其进行错误测试。

`catch` 语句允许你在 `try` 块发生错误时，定义一个要执行的代码块。

`finally` 语句让你无论结果如何，在 `try` 和 `catch` 之后执行代码。

```javascript
try {
  // 尝试运行这段代码
}
catch(err) {
  // 在此处捕获错误
}
finally {
  // 无论发生什么都运行这段代码
}
```

## 问题：如何创建通用对象？

通用对象本质上是对象的空蓝图。你可以在 JavaScript 代码的任何地方定义它。下例所示：

```javascript
function Employee(first, last, ssn, salary) {
  this.firstName = first;
  this.lastName = last;
  this.social = ssn;
  this.pay = salary;
}
```

这创建了一个名为 Employee 的对象的通用蓝图。要获取 Employee 的实例，你需要调用：

```javascript
var john = new Employee("John", "Smith", "050529994", 72534);
```

## 问题：JavaScript 中 Push 方法的用途是什么？

`push` 方法用于向数组的末尾添加或追加一个或多个元素。使用此方法，我们可以通过传递多个参数来追加多个元素。

## 问题：JavaScript 中的 shift() 方法是什么？

`shift()` 方法类似于 `push()`，但它作用于数组的开头。
该方法用于在数组的开头前添加一个或多个元素。

## 问题：解释 JavaScript 中的 pop() 方法？

`pop()` 方法与 `shift()` 方法相似，不同之处在于它作用于数组的最后一个元素。在数组上调用 `pop()` 将返回最后一个元素。

## 问题：JavaScript 中有哪些类型的错误？

从 ECMAScript 2016 开始，JavaScript 中除了通用的 `Error` 对象外，还有七种核心错误构造函数：

### EvalError

在执行全局函数 `eval()` 期间发生的错误。

### InternalError

当 JavaScript 引擎抛出内部错误时发生的错误，例如“递归过多”。

### RangeError

当数值变量或参数超出有效范围时发生的错误。

### ReferenceError

当对无效引用进行解引用时发生的错误。

### SyntaxError

在 `eval()` 中解析代码时发生的语法错误。

### TypeError

当变量或参数不是有效类型时发生的错误。

### URIError

当 `encodeURI()` 或 `decodeURI()` 接收到无效参数时发生的错误。

## 问题：什么是 JavaScript Cookies？

Cookies 是存储在计算机中的小型文本文件。Cookies 在用户访问网站时创建，并用于存储网站可能需要的用户信息，例如购物车详情。

JavaScript 可以通过 **document.cookie** 属性创建、读取和删除 cookie。

## 问题：JavaScript 中的“严格（Strict）”模式是什么？如何启用？

答案：
ECMAScript 5 的严格模式是一种选择使用受限 JavaScript 变体的方法。严格模式刻意与普通的 JavaScript 代码有所不同。

严格模式对普通的 JavaScript 语义进行了几处更改。首先，严格模式通过将某些 JavaScript 静默错误改为强制抛出错误。其次，严格模式允许 JavaScript 引擎执行以前无法实现的某些优化。第三，严格模式禁止了在未来 ECMAScript 版本中可能定义的语法。

## 问题：解释 JavaScript 中的闭包（closures）？它们何时使用？

闭包是一个内部函数，它可以访问外层函数的变量。闭包不仅可以访问自己的作用域（定义在大括号之间的变量），可以访问外层函数的变量，还可以访问全局变量。

你通过在另一个函数内部添加一个函数来创建闭包。内部函数可以访问外部函数的变量和参数。

```javascript
function sayHi(firstName, lastName) {
  var greeting = "Hello ";

  // 内部函数可以访问外部
  // 函数的参数和变量！

  function name() {
    return greeting + firstName + " " + lastName;
  }

  return name();
}
```

## 问题：对象属性是如何赋值的？

属性是与 JavaScript 对象关联的值。

假设一个对象已经存在，你可以像这样直接添加新属性：
myObject.myProperty = 'Property Value';

## 问题：如何向数组追加一个值？

这是一个微妙且棘手的问题，因为它既有一个基础答案，也有一个更好、更完整的答案。

乍看之下

但为了得到更好的答案，不要忘记所有可用的数组方法！

- 1. 使用 `push()`
- 2. 使用 `unshift()` 在数组开头添加
- 3. 使用 `splice()` 在数组中插入
- 4. 使用 `concat()` 合并

## 问题：解释 for-in 循环？

`for-in` 循环用于遍历对象的属性。它会在属性耗尽之前继续。

```javascript
var item;
for (item in myObject) {
  // 执行操作
}
```

## 问题：描述 JavaScript 中的匿名函数（anonymous function）？

没有命名的函数被称为匿名函数。

存储在变量中的函数不需要使用函数名。

## 问题：JavaScript 中可以使用哪些逻辑运算符？

“与”、“或”和“非”运算符可以在 JavaScript 中使用。

例如，给定 x=2 和 y=6

| 运算符 | 名称 | 示例 |
| --- | --- | --- |
| && | 与 | (x < 3 && y > 1) 为真 |
| || | 或 | (x == 5 || y == 5) 为假 |
| ! | 非 | !(x == y) 为真 |

# JavaScript 和元素

这些 JavaScript 问题专注于元素。

## 问题：如何更改元素的类（class）？

使用原生 JavaScript：

```javascript
document.getElementById("MyElement").classList.add('MyClass');
```

```javascript
document.getElementById("MyElement").classList.remove('MyClass');
```

## 问题：如何更改元素的样式（style）？

使用原生 JavaScript：

```javascript
document.getElementById("p2").style.color = 'blue';
```

## 问题：解释如何使用 JavaScript 提交表单？

使用 JavaScript 提交表单：

```javascript
document.form[0].submit();
```

## 问题：在 JavaScript 中使用 innerHTML 的缺点是什么？

不当处理处理 `innerHTML` 属性可能会在包含标记为延迟执行的脚本时允许脚本注入：
<script defer>...</script>

设置 `innerHTML` 会破坏绑定了事件处理程序的现有 HTML 元素，在某些浏览器中可能会内存泄漏。

你无法在所有浏览器的所有 HTML 元素上设置 `innerHTML` 属性（例如，Internet Explorer 不允许设置表格行的 `innerHTML`）。

最后，innerHTML 内容每次都会刷新，因此速度较慢。

## 问题：JavaScript 中可用的所有弹出框（Pop up boxes）类型有哪些？

JavaScript 有三种弹出框：警告框（Alert）、确认框（Confirm）和提示框（Prompt）。

### 警告框（Alert）

警告框通常用于确保信息传递给用户。
当警告框弹出时，用户必须点击“确定”才能继续。

### 确认框（Confirm）

确认框通常用于让用户验证或接受某些内容。
当确认框弹出时，用户必须点击“确定”或“取消”才能继续。

### 提示框（Prompt）

提示框通常用于让用户在进入页面之前输入值。

当提示框弹出时，用户在输入值后必须点击“确定”或“取消”才能继续。





## 问题：blur 函数有什么用处？

blur 函数用于移除指定对象的焦点。

## 问题：如何获取 CheckBox 的状态？

使用你输入字段的 ID，可以检查以下内容的值：
document.getElementById('my-checkbox').checked

如果为 True，则复选框被勾选状态。

## 问题：定义事件冒泡？

当事件在元素上发生事件时，它会首先运行该元素上的处理器，然后运行其父元素上的处理器，一直向上传播到其他祖先元素。换句话说，它会向上“冒泡”。

这是因为 JavaScript 允许 DOM 元素之间相互嵌套。在这种情况下，如果子元素的处理器被点击，父元素的处理器也会像被点击了一样同样起作用。

## 问题：在 JavaScript 中是如何利用事件处理程序的？

答案：
事件是用户活动产生的动作，例如点击链接或填写表单。事件监听器或处理器是计算机程序中的一种过程或函数，它负责等待事件发生，然后对该事件执行相应的操作。

# 比较与对比

本节侧重于要求你解释概念和方法之间相似之处与差异的问题。

## 问题：列举 Java 和 JavaScript 之间的区别？

尽管名字非常相似，但这两种语言完全不同，且设计意图也非常不同。JavaScript 主要是一种用于 HTML 页面内部的脚本语言，而 Java 是一种编译型编程语言，它具有并发、基于类和面向对象的特性。

Java 由 Sun 开发，旨在作为一种通用计算机编程语言。

JavaScript 由 Netscape 开发，最初是作为客户端脚本语言。

## 问题：JavaScript 和 ASP 脚本之间，哪一个更快？

JavaScript 更快。JavaScript 是一种客户端语言，因此不需要 Web 服务器的协助即可执行。相反，ASP 是一种服务端语言，因此总是比 JavaScript 慢。

## 问题：ViewState 和 SessionState 有什么区别？

**ViewState** 特指会话中的某个页面。

**SessionState** 特指用户特定数据，数据可以在 Web 应用程序的所有页面中访问。

## 问题：解释“==”和“===”之间的区别

“==” 仅检查值的相等性。

“=== ” 是更严格的相等性测试，如果两个变量的值或类型不同，则返回 false。

## 问题：警报框（alert box）和确认框（confirmation box）有什么区别？

警报框只显示一个按钮，即 OK 按钮。
确认框显示两个按钮，即 OK 按钮和取消按钮。

## 问题：解释 window.onload 与 onDocumentReady 的区别？

load 在所有资源（包括图像）加载完成时调用。此时，文档中的所有对象已在 DOM 中。

ready 在 DOM 准备好交互且其元素可以被你的代码进行操作时触发。这意味着它的运行速度会比等待 load 快一点。

# Bonus题

这些狡猾的问题迫使你对 JavaScript 了如指掌。
注意陷阱！

## 问题：可以将 JavaScript 代码拆分成几行吗？

在字符串语句内部进行换行可以通过第一行末尾使用反斜杠 `\` 来实现。如果你在不在字符串语句的情况下换到新行，那么 JavaScript 会忽略该换行符。

## 问题：3+2+"7" 的结果是什么？

由于 3 和 2 是整数，它们将进行数值相加。由于 7 是一个字符串，它将进行字符串拼接。因此结果将是 57。

## 问题：如何在 JavaScript 中将任何基数的字符串转换为整数？

parseInt() 函数用于在不同基数之间转换数字。parseInt() 接受要转换的字符串作为第一个参数，第二个参数是给定字符串的基数。

## 问题：JavaScript区分大小写吗？举个例子？

是的，JavaScript 是区分大小写的。例如，函数 parseInt() 与函数 ParseInt() 不同。

## 问题：.call() 和 .apply() 有什么区别？

.call() 和 .apply() 函数在用法非常相似，除了 apply() 允许你以数组的形式调用函数；.call() 要求显式列出参数。换句话说，当你不知道参数的数量时使用 apply()。

