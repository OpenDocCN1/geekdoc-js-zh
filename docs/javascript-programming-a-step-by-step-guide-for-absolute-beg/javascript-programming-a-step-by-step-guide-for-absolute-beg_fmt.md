
# JavaScript 编程：初学者循步进阶指南

## 本书目标

以下是本书的目标：

- 帮助你了解如何开始 JavaScript 编程。
- 帮助你理解组成 JavaScript 脚本语言的语法和结构。
- 帮助你从 JavaScript 初学者变为专业人士。
- 帮助你理解如何使用 JavaScript 提高网站应用程序的交互性。

## 本书读者

作者针对以下群体：

- 任何 JavaScript 编程或通用计算机编程的初学者。
- 任何需要提高 JavaScript 技能的人员。
- 寻找以最简单的方法向学生解释 JavaScript 的教授、讲师或导师。
- 学生和学者，特别是关注计算机编程和 Web 开发的人员。

## 学习本书需要什么？

请确保你拥有以下物品：

- 一个文本编辑器（如记事本）。
- 一个现代 Web 浏览器。

## 书中内容

本书分为若干章节，每章探索 JavaScript 脚本语言的不同功能。作者提供了 JavaScript 代码，每段代码执行不同的任务。每段代码旁都提供了相应的解释，以帮助读者理解代码各行的含义。此外，还提供了显示每段代码应有输出的截图。作者使用了简单的语言，以便零基础学者轻松理解。

## 关于作者

Brian Jenkins 拥有计算机科学博士学位。他曾针对磁记录系统和远距离光通信系统进行编码研究。拥有二十年教授新手编程的经验，作为这一代最有才华的 IT 专家之一，Brian 博士担任研究专家，兼生物信息学家。自 2015 年以来，Brian 与妻子和女儿住在日内瓦。他正在编写一系列关于计算机编程和数据科学的书籍。

> “JavaScript 是一种坏部分过多的语言。” —— Douglas Crockford

## 引言

JavaScript 是一种每个 Web 开发者都应该熟悉的脚本语言。JavaScript 为 Web 开发领域带来了许多变化。它为 Web 开发者提供了一种让网页更具交互性的方法。这是大多数访问者所寻找的。如果你了解如检查用户填写表单时输入的详情是否正确等验证，JavaScript 是实现此类功能的最佳语言。它是 WWW（万维网）的技术之一。JavaScript 的优点是它受所有现代浏览器的支持。这意味着你不需要安装任何插件即可运行其脚本。你可以轻松开始编写和运行 JavaScript 脚本，因为你只需要基础元素，如文本编辑器和浏览器。

---

## 第 1 章 JavaScript 基础

### 什么是 JavaScript？

HTML 用于内容，CSS 用于演示，而 JavaScript 是为了交互而开发的。最初，JavaScript 的开发是为了为小型网页添加交互性（如动画和悬停效果），但现在它可以用于几乎所有场景，包括大型应用程序、游戏和服务器。

JavaScript 程序被称为脚本（scripts）。你可以在网页的 HTML 内部编写 JavaScript，它会在页面加载时自动执行。脚本以纯文本形式提供并按原样执行。它们不需要经过编译或特殊的准备即可运行。今天，我们可以在浏览器、服务器或带有 JavaScript 引擎的设备上执行 JavaScript 代码。起初，JavaScript 被称为 LiveScript，因为它让网页变得活跃。这个名字后来被更改为 JavaScript。

JavaScript 是一种基于对象的脚本语言，可以被所有现代浏览器解释。这意味着所有浏览器都自带 JavaScript 引擎。这增加了 JavaScript 的普及程度，使其成为当今最流行的脚本语言。

### 环境搭建

为了编写、测试和运行你的 JavaScript 代码，你需要以下工具：

- 编辑器
- 浏览器

你甚至可以使用像记事本这样的基础文本编辑器来编写 JavaScript 代码。然而，获取一个高级文本编辑器对你大有裨益，它可以提供语法错误高亮、自动补全等功能。此类编辑器的示例包括 Visual Studio、Eclipse、Atom 等。这些可以帮助你提高开发速度。你也可以使用一些在线 JavaScript 编辑器来编写脚本，`jsfiddle.net` 就是一个很好的例子。对于浏览器，你可以根据喜好安装任何类型的浏览器。此类浏览器包括 Chrome、Internet Explorer、Safari、Firefox 等。JavaScript 可以在运行于任何操作系统上的浏览器上工作。

### 示例

我们可以在三个地方放置 JavaScript 代码。我们可以将代码放置在 `body` 内部、`head` 标签内或外部 JavaScript 文件中。这里是我们的第一个示例：

```html
<html>
<head>
<script type="">
document.write("");
</script>
</head>
<body>
</body>
</html>
```

JavaScript 让网页具有交互性！`script` 标签指定了我们正在使用 JavaScript。这有助于浏览器识别它所处理的数据类型。代码简单地调用了 JavaScript 的 `document.write()` 方法，打印我们传递给它的文本。该方法用于使用 JavaScript 显示动态内容。如我们在上面所述，我们可以在三个地方添加代码。以下代码演示了如何在 `<body>` 和 `</body>` 标签之间添加代码：

```html
<html>
<head>
<script type="">
document.write("");
</script>
</head>
<body>
</body>
</html>
```

这是另一个示例，显示我们可以显示警框（alert box）：

```html
<html>
<head>
<script type="">
function hello() {
  alert("Hello World");
}
</script>
</head>
<body>
<p>JavaScript</p>
<form>
<input type="button" value="" onclick="hello()"/>
</form>
</body>
</html>
```

我们在 `script` 标签内创建了一个名为 `hello()` 的方法。该方法在被调用时应该返回一个带有 Hello World 消息的警框。我们在 `<body>` 标签内创建了一个带有按钮的表单。`onclick` 属性指定了点击按钮时调用的方法。运行代码后你应该得到如下结果：

点击“点击我”按钮。你将看到带有 Hello World 消息的警框。

JavaScript 文件的文件名是在 script 标签内通过 `src` 参数指定的。

## JavaScript 注释

注释为我们提供了一种传递信息的方式。注释有助于引导用户、添加描述代码的信息、建议或警告，让读者更容易解释代码。JavaScript 引擎会忽略注释，这意味着它会跳过这些内容。

JavaScript 注释可以跨越单行或多行。要写单行注释，请在其前面加上双斜杠（`//`）。例如：

```javascript
var x = 3;
document.write(x);
```

这是另一个示例：

```javascript
var x = 5;
var y = 25;
var z = 60;
document.write(z); // 打印这些内容
```

多行注释包含在 `/*` 和 `*/` 之间。这也可以用于单行注释。例如：

```javascript
/* 这是一个多行
注释，引擎会
跳过它 */
document.write("Be syly");
```

### 大小写敏感

JavaScript 是一种大小写敏感的脚本语言。这意味着名为 `x` 的变量与名为 `X` 的变量不同。名为 `age` 的变量与名为 `Age`、`AGE` 等变量不同。

---

## 第 2 章 弹出消息

JavaScript 有许多内置方法，可以帮助为了各种目的显示弹出消息。让我们讨论 JavaScript 提供的各种弹出框：

### Alert 框（警告框）

用于向用户显示消息，特别是在需要强调的地方。它带有一个 OK 按钮，点击后关闭弹出窗口。它是通过调用 JavaScript 的 `alert()` 函数创建的。

例如：

```html
<html>
<body>
<h1>Popup</h1>
<script>
alert("Display a number");
alert(true);
</script>
</body>
</html>
```

当您运行代码时，它将显示第一个带有字符串 "Hello World!" 的 alert 框。点击 OK 按钮，它将显示一个带有 123 的 alert。再次点击 OK 按钮，它将显示一个带有 `true` 的 alert 框。这表明 alert 框可以显示任何类型的消息。

### Confirm 框（确认框）

有时，需要用户给出确认以继续操作。例如，您可能希望在完成处理之前，让用户确认删除或更新某些详情。这可以使用 JavaScript 提供的 `confirm()` 函数来实现。该函数将向用户显示一个弹出框，其中包含两个按钮，即 OK 和 Cancel。下一步由用户点击的按钮决定。

例如：

```html
<html>
<body>
<h1>confirm()</h1>
<p id="demo"></p>
<script>
var userChoice;
if (confirm("") == true) {
    userChoice = "OK";
} else {
    userChoice = "Canceled!";
}
document.getElementById("demo").innerHTML = userChoice;
</script>
</body>
</html>
```

### Prompt 框（提示框）

在某些情况下，您可能需要接收用户的输入并用它在页面上执行后续操作。例如，您可能需要根据用户想要结算贷款的月数来计算每月还款金额。在这种情况下，可以使用 JavaScript 提供的 `prompt()` 函数。该函数应接受两个字符串参数。第一个是显示的消息，第二个是当消息显示后输入文本框中的默认值：`prompt(message, defaultValue)`。

例如：

```html
<html>
<body>
<h1>prompt()</h1>
<p id="demo"></p>
<script>
var age = prompt("Enter your age:", "26");
document.getElementById("demo").innerHTML = age;
</script>
</body>
</html>
```

---

## 第 3 章 变量

变量是存储位置的名称。根据它的名称，它可以变化。变量持有变化的值。在 JavaScript 中，我们使用 `var` 关键字来声明变量。每个变量必须赋予一个唯一的名称。您可以在声明时为变量赋值。这可以通过等号（`=`）完成。以下是 JavaScript 中声明初始化变量的语法：

```javascript
var variableName;
variableName = value;
```

这里是有效的示例：

```javascript
var x = 10;
var y = 20;
var z = 30;
```

我们使用了 `var` 关键字声明了三个变量。其中两个变量已经赋值。注意这是在声明时完成的。

我们也可以在一行中声明多个变量，并用逗号（`,`）隔开。演示如下：

```javascript
var x = 1, y = "a";
```

注意，在 JavaScript 中，人们可以不使用 `var` 关键字声明变量。然而，如果您这样做，请确保立即为变量赋值。演示如下：

```javascript
x = 1;
y = "a";
```

但是，我不建议您不使用 `var` 关键字声明任何变量。这是因为您可能会在不知情的情况下覆盖一个全局变量。如果不使用 `var` 关键字声明变量，它将自动成为全局变量，无论它在何处声明。

以下示例演示了如何在 JavaScript 中使用变量：

```html
<script>
var a = 10;
var b = 13;
var c = 5 + b;
document.write(c);
</script>
```

代码将返回两个变量值之和，结果为 23。

### 局部变量

这些是在块或函数内部定义的变量。它们只能在定义它们的块或函数内部被访问。

这是一个示例：

```html
<script>
function xyz() {
  var a = 10;
}
</script>
```

变量 `a` 只能在函数 `xyz()` 内部访问。

这是另一个局部变量声明的示例：

```html
<script>
function xyz() {
  var a = 16;
}
</script>
```

上述示例中的变量 `a` 只能在其声明的块内部被访问。

### 全局变量

这些可以在任何函数中访问的变量。全局变量通常在函数外部声明或通过 JavaScript 的 `window` 对象声明。

例如：

```html
<script>
var val = 12;
function x() {
  document.writeln(val);
}
function y() {
  document.writeln(val);
}
x();
y();
</script>
```

代码将返回：

```text
12 12
```

代码演示了函数可以从不同的函数中引用，且其值将保持不变。

如果你需要在函数内部声明全局变量，则必须使用 `window` 对象。例如：

```html
<script>
function xy() {
  window.val = 12;
}
function xz() {
  alert(window.val);
}
xy();
</script>
```

这种变量可以在任何函数中声明，并从任何函数中访问。我们在函数 `xy()` 中声明了变量 `val` 并为其赋值为 12。然后我们从函数 `xz()` 访问了同一个变量。这返回了值 12。在函数外部声明变量后，它会被内部添加到 `window` 对象中。该对象可以同时通过 `window` 对象访问。

这是一个示例：

```html
<script>
var val = 12;
function y() {
  alert(window.val);
}
</script>
```

---

## 第 4 章 数据类型

每种编程语言都支持多种数据类型。它们代表可以在编程语言中操作的值类型。JavaScript 支持 3 种原始数据类型，包括：

- 数字，例如 `1`、`8`、`345` 等。
- 字符串，即文本，例如 `"My name"` 等。
- 布尔值，可以为 `true` 或 `false`。

JavaScript 还能支持 2 种简单数据类型，即 `null` 和 `undefined`。它还有一种名为 `object` 的复合数据类型。注意，在 JavaScript 中，整数和浮点数没有区别。在 JavaScript 中，所有数字都以浮点值的形式表示。

---

## 第 5 章 比较变量

在 JavaScript 中，可以用不同的方式比较变量。我们可以使用双等号（`==`）来比较两个变量是否相等。

示例：

```html
<script>
var x = 30;
var y = 30;
if (x == y) {
  alert("x equals y");
}
</script>
```

执行时，脚本将显示一个带有 "x equals y" 文本的弹出窗口。这是当两个值相等时（即 10）。如果不相等，脚本执行后将什么都不会发生。

除了数字之外，我们也可以像下面所示比较字符串：

```html
<script>
var firstname = "John";
var lastname = "Doe";
if (lastname == "Doe") {
  alert("Correct!");
}
</script>
```

注意，在进行比较时，我们使用双等号（`==`）。如果你使用单等号（`=`），则等号右侧的值将成为左侧变量的值。

---

## 第 6 章 运算符

JavaScript 支持运算符的使用。运算符对一个或多个操作数执行操作以产生结果。例如：在上面的示例中，`2` 和 `3` 是操作数，而 `+` 是运算符。`2` 是左操作数，`3` 是右操作数。`+` 运算符将两者相加得到结果 `5`。

让我们讨论一下 JavaScript 支持的各种类型的运算符。

### 逻辑运算符

这些类型的运算符帮助我们连接一个或多个条件。以下是 JavaScript 支持的逻辑运算符：

- `&&` - 与运算符（AND）。它检查两个操作数是否非零。如果是，则返回 `1`，否则返回 `0`。
- `||` - 或运算符（OR）。它检查是否任一个操作数为非零。如果是，则返回 `1`，否则返回 `0`。
- `!` - 非运算符（NOT）。用于反转操作数或条件的布尔结果。

例如：

```html
<html>
<body>
<h1>Logical Operators</h1>
<p id="1"></p>
<p id="2"></p>
<p id="3"></p>
<p id="4"></p>
<p id="5"></p>
<script>
var x = 2;
var y = 3;
if (x && y) {
  document.getElementById("1").innerHTML = x && y;
}
if (x || y) {
  document.getElementById("2").innerHTML = x || y;
}
if (!x) {
  document.getElementById("3").innerHTML = !x;
}
</script>
</body>
</html>
```

代码打印以下结果：

```text
逻辑运算符
false
true
false
true
false
```

在上面的示例中，我们使用了变量 `x` 和 `y` 的值来运行各种逻辑运算符。

### 算术运算符

在 JavaScript 中，你可以对变量执行算术操作。这些操作包括加法（`+`）、减法（`-`）、乘法（`*`）、取模运算（`%`）、自增（`++`）、自减（`--`）等。

示例：

```html
<script type="text/javascript">
var First = "Edwin";
var Last = "Peter";
var Name = First + Last; // Name = EdwinPeter
b = 10 / 2;
c = (10 / 2) * 2;
d = 10 / (1 * 2);
</script>
```

各行的结果已在注释部分显示，即 `//` 之后。两个正斜杠即 `//` 表示 JavaScript 中注释的开始。

### 赋值运算符

这些是帮助我们为变量赋值的运算符。它们包括以下：

- `=`：将右操作数的值赋值给左操作数。
- `+=`：将左、右操作数的值相加，然后将获得的结果赋值给左操作数。
- `-=`：从左操作数的值中减去右操作数的值，然后将获得的结果赋值给左操作数。
- `*=`：将左、右操作数的值相乘，然后将获得的结果赋值给左操作数。
- `/=`：将左操作数的值除以右操作数的值，然后将获得的结果赋值给左操作数。
- `%=`：获取左操作数除以右操作数的模，然后将得到的模结果赋值给左操作数。

这里是一个示例：

```html
<html>
<body>
<h1>赋值运算符</h1>
<p id="a"></p>
<p id="b"></p>
<p id="c"></p>
<p id="d"></p>
<p id="e"></p>
<p id="f"></p>
<script type="text/javascript">
var a = 10;
document.getElementById("a").innerHTML = a;
document.getElementById("b").innerHTML = a;
a += 1;
document.getElementById("c").innerHTML = a;
a *= 5;
document.getElementById("d").innerHTML = a;
a /= 5;
document.getElementById("e").innerHTML = a;
a %= 2;
document.getElementById("f").innerHTML = a;
</script>
</body>
</html>
```

代码将返回以下结果：

```text
10
10
11
55
11
1
```

表达式 `a = 10;` 初始化变量 `a`。表达式 `a += 1;` 将 `a` 的值增加了 1，因此它变成了 11。表达式 `a *= 5;` 将变量 `a` 的值（11）乘以 5，返回 55。表达式 `a /= 5;` 将变量 `a` 的值除以 5，返回 11。表达式 `a %= 2;` 返回变量 `a` 的值除以 2 的余数，返回 1。

---

## 第 7 章 决策

JavaScript 带有决策语句，有助于控制程序的流程。通过这些语句，所采取的操作基于所满足的条件。JavaScript 支持以下决策语句：

### If 语句

该语句应在需要根据特定条件采取操作时使用。只有当条件为真时，内容才会求值。该语句的语法如下：

```javascript
if (condition) {
  
}
```

示例：

```html
<script>
var x = 10;
if (x > 5) {
  alert(10);
}
</script>
```

代码执行后将返回弹窗 `10`。

### If...else 语句

该语句将评估条件为真还是假。该语句具有以下语法：

```javascript
if (condition) {
  
} else {
  
}
```

示例：

```html
<script>
var x = 18;
if (x % 2 == 0) {
  document.write("even number");
} else {
  document.write("odd number");
}
</script>
```

在上面的代码中，我们正在检查变量 `x` 的值是否为偶数。代码返回：

```text
even number
```

表达式 `x % 2 == 0` 检查 `x` 除以 2 的余数。如果余数为 0，则 `x` 是偶数，否则它是奇数。

### If...else if 语句

有时，你可能有多个需要做出决策的选项。该语句帮助我们在 JavaScript 中实现这一点。该语句的语法如下所示：

```javascript
if (expression1) {
  
} else if (expression2) {
  
} else if (expression3) {
  
} else {
  
}
```

示例：

```html
<script>
var grade = "B";
if (grade == "A") {
  document.write("Excellent!");
} else if (grade == "B") {
  document.write("Good!");
} else if (grade == "C") {
  document.write("Fair");
} else {
  document.write("Poor");
}
</script>
```

`grade` 的值为 B。所有要执行的语句都是条件求值为真的语句。代码将返回："Good!"

### Switch 语句

该语句帮助我们根据各种条件执行多样化的操作。当你有许多取决于单个变量值的分支时，它非常适用。

通过 switch 语句，一个表达式会根据表达式的值来评估要执行的各种语句。JavaScript 解释器必须根据表达式的值检查每一个 case，直到找到匹配项为止。如果没有找到匹配项，则选择默认项。它的语法如下：

```javascript
switch (expression) {
  case 1:
    code
    break;
  case 2:
    code
    break;
  default:
    code
}
```

例如：

```html
<script>
var name = "ODIE";
switch (name) {
  case "Alice":
    output = "one";
    break;
  case "Bob":
    output = "two";
    break;
  case "Charlie":
    output = "three";
    break;
  default:
    output = "unknown";
}
document.write(output);
</script>
```

代码执行后将返回以下内容：

```text
unknown
```

---

## 第 8 章 JavaScript 循环

当你需要重复执行代码（无论次数是已知还是未知）时，循环是非常有用的。通过循环，你可以自动化那些手动执行可能非常繁琐的任务。

一个很好的例子是当你需要在表格中填充值时。你可以使用循环遍历表格单元格并填充值，而不是手动填充。

让我们讨论一下 JavaScript 支持的各种循环语句：

### For 循环

这种循环用于固定次数地迭代代码块。当你清楚要迭代某个代码块的次数时，它非常适用。循环采用以下语法：

```javascript
for (initializer; condition; increment) {
}
```

初始化器（initializer）设置了一个我们需要开始的计数器变量。条件（condition）指定了执行下次迭代必须满足的标准。增量（increment）可以增加或减少计数器。

这里是一个 for 循环的示例：

```html
<script>
for (x = 0; x < 5; x++) {
  document.write(x);
}
</script>
```

循环中的变量 `x` 首先初始化为 0。条件规定 `x` 的值应该小于 5。在增量部分，变量 `x` 的值每次迭代都会增加 1。这意味着循环应该从 0 运行到 4，产生如下结果：

```text
01234
```

这是另一个示例：

```html
<head>
  <title>Length Converter</title>
</head>
<body>
  <table border="1">
    <tr>
      <td>Length in Meters</td>
      <td>Length in Centimeters</td>
    </tr>
    <script>
    for (length = 0; length <= 5; length++) {
      document.write("<tr><td>" + length + "</td><td>" + length * 100 + "</td></tr>");
    }
    </script>
  </table>
</body>
</html>
```

使用了一个循环在转换米时迭代一组值。代码返回了一个填充好的表格。

### While 循环

这种循环可以用于无限次地迭代代码。当你不确定执行循环的确切次数时，它非常适用。只要指定的条件为真，循环就会执行。一旦条件变为假，循环的执行就会停止。它采用以下语法：

```javascript
while (variable <= final_value) {
}
```

例如：

```html
<script>
var x = 0;
while (x <= 5) {
  document.write(x + " ");
}
</script>
```

只要变量 `x` 的值不大于 5，while 循环就会运行。代码返回以下：

```text
0 1 2 3 4 5
```

这是另一个示例：

```html
<head>
  <title>Length</title>
</head>
<body>
  <table border="1">
    <tr>
      <td>Length in Meters</td>
      <td>Length in Centimeters</td>
    </tr>
    <script>
    length = 0;
    while (length <= 2) {
      document.write("<tr><td>" + length + "</td><td>" + length * 100 + "</td></tr>");
      length++;
    }
    </script>
  </table>
</body>
</html>
```

只要 `length` 的值小于或等于 2，上面的循环就会一直运行。一旦循环发现违反了这一条件，它就会停止。

### Do...While 循环

这是一个用于无限次的良好循环。然而，无论条件如何，代码必须执行一次。它的语法如下：

```javascript
do {
  statement
} while (condition);
```

while 循环可能永远不运行，但 do...while 循环至少运行一次。这里是一个示例：

```html
<script>
var x = 0;
do {
  document.write(x + " ");
  x++;
} while (x <= 5);
</script>
```

### break 语句

通过此语句，可以提前退出循环并跳出大括号。执行将到循环之后的块。

示例：

```html
<script type="text/javascript">
var p = 0;
while (p < 20) {
  if (p == 5) {
    break;
  }
  document.write(p + "<br>");
  p++;
}
document.write("After");
</script>
```

这就是在 `while` 循环中使用 `break` 语句的方法。`p` 的最大值本应为 20。然而，我们指示 JavaScript 解释器在 `p` 的值为 5 时跳出。循环的执行将在该处停止；输出应显示 0 到 4 的数字：

```text
0
1
2
3
4
After
```

### continue 语句

通过 `continue` 语句，我们可以中断当前的循环，然后处理下一个值。假设你需要将一个数字除以从 -5 到 +5 之间的任意数字。你需要跳过除以 0 的除法，因为这是非法的。可以使用 `continue` 语句来跳过它。实现方式如下：

```html
<script type="text/javascript">
for (p = -5; p <= 5; p++) {
  if (p == 0) {
    continue;
  }
  document.write((10 / p) + "<br>");
}
</script>
```

通过这种实现，整数 10 将不会除以 0。代码将返回以下结果：

```text
-2
-2.5
-3.33...
-5
-10
10
5
3.33...
2.5
2
```

我们跳过了除以 0 的操作，因为如果不跳过，将会产生错误。

---

## 第 9 章 JavaScript 函数

JavaScript 函数用于执行操作。函数是将代码组合在一起的好方法。此类代码在它们应执行的任务应该是相关的。你只需要将代码组合在一起并分配一个唯一的名称。从该点起，你可以根据需要多次调用该代码，有助于代码复用。

通过函数，你可以享受只需重写代码或完全不需要重写代码的好处。

### 函数定义

JavaScript 函数的定义和调用采用以下语法：

```javascript
function functionName() {
};

functionName();
```

如所示，函数被赋予了一个名称，在调用函数以执行其预期任务时会使用该名称。

函数有一个位于大括号 `{}` 内部的体。以下是一个示例：

```html
<script type="text/javascript">
function HelloFunction() {
  document.write("Hello World");
}
HelloFunction();
</script>
```

我们定义了一个名为 `HelloFunction()` 的函数。在函数体内，我们规定了函数应该打印文本 Hello World。在函数体之后，我们通过其名称调用了它。代码返回以下内容：

```text
Hello World
```

注意我们调用上述函数的方法。该函数将在网页加载时立即被调用。然而，很多时候我们需要通过点击按钮来调用函数。

```html
<script type="text/javascript">
function HelloFunction() {
  alert("Hello World");
}
</script>
<input type="button" value="Hello" onclick="HelloFunction()">
</body>
```

我们使用了之前的函数。但是，我们创建了一个带有 Hello 文字的按钮。`onclick` 属性规定了点击按钮后应该发生什么。它规定点击按钮后应该调用 `HelloFunction()`。运行代码并点击按钮。你将得到带有必要消息的警告框：Hello World

### 函数参数

函数可以接受一个或多个参数，也称为参数。参数应由调用代码提供，并可以在函数内部使用。JavaScript 以作为动态脚本语言而闻名，因此函数参数可以接受任何数据类型的参数。考虑以下示例：

```html
<script type="text/javascript">
function MyFunction(arg1, arg2) {
  alert(arg1 + " " + arg2);
}
MyFunction(10, 12);
MyFunction("Hello", "World");
</script>
```

我们创建了一个名为 `MyFunction()` 的函数，接受两个参数，即 `arg1` 和 `arg2`。函数的作用是将这两个参数的值与文本拼接并在警告框中显示它们。然后我们又调用了两次同一个函数，每次传递不同的参数。运行代码后，第一个对话框如下：

```text
You passed 10 and 12
```

注意，参数将按照你指定的顺序传递给函数。这里是另一个示例：

```html
<script type="text/javascript">
function calculateCube(x) {
  return (x * x * x);
}
</script>
<input type="button" value="Calculate Cube" onclick="alert(calculateCube(3))">
```

我们创建了一个带有 Calculate Cube 文字的按钮。点击时，这会调用 `calculateCube()` 函数。在参数中，我们指定了函数并向其传递了参数 3。这意味着它应该返回 3 的立方，即 27。只需运行程序并点击 Calculate 按钮。注意，在调用函数时，你可以传递更多或更少的参数。如果你传递的参数比函数预期少，其余部分将保持未定义（`undefined`）。如果你传递更多参数，多余的将被忽略。以下示例演示这一点：

```html
<script type="text/javascript">
function MyFunction(arg1, arg2) {
  alert(arg1 + " " + arg2);
}
MyFunction(10, 12);
MyFunction("Hello", "World");
MyFunction(10);
</script>
```

### Arguments 对象

任何 JavaScript 函数都可以使用 `arguments` 对象。该对象为每个参数都持有一个值。它类似于数组。你可以像访问数组一样使用索引来访问它的值。然而，该对象不支持数组方法。

考虑以下示例：

```html
<script>
function MyFunction(arg1, arg2) {
  alert(arguments[0] + " " + arguments[1]);
}
MyFunction(0, 'e');
MyFunction('a', 'b');
MyFunction(1, 2);
</script>
```

代码将照常运行。在调用函数时，我们可以向其传递参数。JavaScript 解释器会将第一个参数视为索引为 0。表达式 `arguments[0]` 表示调用函数时的第一个参数，而表达式 `arguments[1]` 表示调用函数时的第二个参数。

我们可以使用 `for` 循环来遍历 `arguments` 对象。例如：

```html
<script>
function MyFunction() {
  for (var x = 0; x < arguments.length; x++) {
    alert(arguments[x]);
  }
}
MyFunction("Nice", "day");
</script>
```

函数被传递了两个参数，我们在 `for` 循环中使用变量 `x` 遍历了这些参数。

### 返回值

在 JavaScript 中，函数可以使用 `return` 关键字返回零或一个值。

考虑下面提供的示例：

```html
<script>
function MyFunction() {
  return 5;
}
document.write(MyFunction());
</script>
```

该函数将返回 `return` 语句中指定的内容。

这是另一个示例：

```html
<html>
<body>
  <p id="result"></p>
  <script>
    function Addition(x, y) {
      return x + y;
    }
    document.getElementById("result").innerHTML = Addition(10, 12);

    function Product(x, y) {
      console.log(x * 7);
    };
    document.getElementById("result").innerHTML = Product(10, 12);
  </script>
</body>
</html>
```

该代码将打印以下内容：

```text
22
undefined
```

我们创建了一个名为 `Addition()` 的函数，它相加并返回两个变量 `x` 和 `y` 的和。调用代码能够获取返回值并将其赋值给变量。我们还定义了第二个名为 `Product()` 的函数，它不返回任何内容，因此它的结果是 `undefined`。

### 函数返回函数

在 JavaScript 中，我们可以让一个函数返回另一个函数。这是一个示例：

```html
<html>
<body>
  <p id="p1"></p>
  <p id="p2"></p>
  <script>
    function myfunction(a) {
      function product(b) {
        return a * b;
      }
      return product;
    }
    var db = myfunction(2);
    document.getElementById("p1").innerHTML = db(2);
    document.getElementById("p2").innerHTML = db(3);
  </script>
</body>
</html>
```

名为 `myfunction()` 的函数正在返回名为 `product()` 的函数。

### 匿名函数

在 JavaScript 中，我们可以定义一个没有名字的函数。这种函数被称为匿名函数。你必须为你的匿名函数分配一个变量。

例如：

```html
<html>
<body>
  <p id="p1"></p>
  <p id="p2"></p>
  <script>
    var sum = function(x, y) {
      return x + y;
    }
    document.getElementById("p1").innerHTML = sum(10, 12);
  </script>
</body>
</html>
```

代码应该返回 10 和 12 的和，即 22。此输出将来自 `sum(10, 12)` 表达式，其中我们使用赋值给它的变量来调用函数。表达式 `Addition(10, 12)` 是无效的，因为我们通过函数名调用它，而它已经被赋值给了一个变量。

我们创建了两个匿名函数。第一个不接受参数，并被赋值给变量 `helloMessage`。消息应该在弹框中返回 "Hello World"。该方法在程序中通过 `helloMessage()` 表达式调用了两次。

```javascript
var helloMessage = function() {
  alert("Hello World");
};
helloMessage();

var message = function(name) {
  alert("Hi " + name);
};
message("Nicholas");
```

代码将显示两次 "Hello World" 和一次 "Hi Nicholas"。要从一个弹框移动到另一个弹框，请点击 OK 按钮。

### 嵌套函数

JavaScript 函数可以拥有一个或多个内部函数。嵌套函数应该在外部函数的作用范围内。内部函数允许访问外部函数的参数和变量。然而，外部函数无法访问在其内部函数定义的变量。

考虑以下示例：

```html
<script>
function OuterFunc(name) {
  function InnerFunc() {
    document.write("Hi " + name);
  }
  return InnerFunc();
}
OuterFunc("Nicholas");
</script>
```

我们定义了一个名为 `OuterFunc()` 的外部函数。该函数接受一个参数 `name`。虽然 `name` 参数属于外部函数，但内部函数成功地访问了它。代码应该打印以下内容：

```text
Hi Nicholas
```

---

## 第 10 章 JavaScript 对象

### 数组

JavaScript 中的对象是一个既有状态又有行为的实体。在 JavaScript 中，一切都被视为对象。数组是一种表示相似类型元素的对象。它具有固定的大小，且元素按顺序存储。在 JavaScript 中有 3 种构造数组的方法：

- 数组字面量
- 数组实例
- 数组构造函数

#### 数组字面量

使用数组字面量创建数组采用以下语法：

```javascript
var nameOfArray = [val1, val2, ...];
```

值用方括号 `[]` 添加，并用逗号分隔。

示例：

```html
<script type="javascript">
var array1 = ['Nicholas', 'Samuel', 'Vickie'];
for (j = 0; j < array1.length; j++) {
    document.write(array1[j]);
}
</script>
```

我们创建了一个包含三个值的数组 `array1`，这些值是人的名字。我们使用 `for` 循环来遍历数组的值，然后将它们打印出来。`.length` 属性通常返回数组的长度。执行后，数组中的值将如下所示：

```text
Nicholas
Samuel
Vickie
```

#### 直接创建数组

可以通过下面提供的语法直接创建数组：

```javascript
var nameOfArray = new Array();
```

通过 `new` 关键字，会创建一个数组的实例。

示例：

```html
<script type="javascript">
var x;
var array2 = new Array();
array2[0] = 'Nicholas';
array2[1] = 'Samuel';
array2[2] = 'Vickie';
for (x = 0; x < array2.length; x++) {
    document.write(array2[x]);
}
</script>
```

在示例中，我们使用 `new` 关键字创建了名为 `array2` 的数组。下一步是向数组填充元素。请注意，数组元素的位置使用索引表示。数组中的第一个元素位于索引 0，第二个元素位于索引 1，以此类推。

考虑下面这一行：

```javascript
array2[1] = 'Samuel';
```

该行代码表示我们要在名为 `array2` 的数组的索引 1 处存储元素“Samuel”。然后我们使用变量 `x` 来遍历数组的这些元素并打印它们。

#### 数组构造函数

我们通过直接在构造函数中传递参数，而不是显式地提供值来创建数组实例。下面的脚本演示了这一点：

```html
<script type="javascript">
var array3 = new Array('Nicholas', 'Samuel', 'Vickie');
for (x = 0; x < array3.length; x++) {
    document.write(array3[x]);
}
</script>
```

在上面的示例中，我们创建了一个名为 `array3` 的数组。数组的创建和元素的添加是通过构造函数在同一行中完成的。`for` 循环帮助我们遍历数组元素并将其打印到屏幕上。

### 数组方法

JavaScript 带有许多内置数组方法，我们可以操作数组元素。让我们讨论这些方法：

#### concat()

`concat()` 方法合并数组并返回新数组。数组可以是两个或多个。注意，初始数组的元素不会被改变。

```html
<script type="javascript">
var array1 = ['Nicholas', 'Samuel'];
var array2 = ['Vickie'];
var array3 = ['Joel'];
var output = array1.concat(array2, array3);
document.writeln(output);
</script>
```

该代码将返回以下输出：

```text
Nicholas,Samuel,Vickie,Joel
```

#### copyWithin()

当使用此方法时，它会将给定数组的一部分复制到自身的元素中并返回修改后的数组。注意，修改后数组的长度不会改变。

该方法采用下面提供的语法：

```javascript
array.copyWithin(target, start, end)
```

`target` 是复制元素将发生的位置。`start` 参数是可选的。它表示方法开始复制元素的索引。它的默认值是 0，意味着复制从索引 0 开始，即数组的第一个元素。`end` 参数也是可选的。它表示方法停止复制过程的索引。它有一个默认值 `array.length - 1`，即数组中的最后一个元素。

该方法返回一个修改后的数组。考虑下面提供的示例：

```html
<script type="javascript">
var array1 = ['Nicholas', 'Samuel', 'Vickie'];
var output = array1.copyWithin(0, 1);
document.writeln(output);
</script>
```

发生的情况是索引 1 处的元素被复制到了索引 0。这就是为什么 `Nicholas` 元素被 `Samuel` 元素替换了。数组的其余元素没有受到影响。

让我们看看如何只提供目标索引和起始索引：

```html
<script>
var array1 = ["Nicholas", "Jane", "Alice", "Alice"];
var output = array1.copyWithin(0, 2);
document.writeln(output);
</script>
```

代码应该返回以下内容：

```text
Alice, Alice, Alice, Alice
```

我们也可以只提供目标索引：

```html
<script>
var array1 = ["Nicholas", "Jane", "Alice", "Alice"];
var output = array1.copyWithin(2);
document.writeln(output);
</script>
```

代码将返回以下结果：

```text
Nicholas, Jane, Nicholas, Jane
```

#### fill()

此方法用于用某些指定的静态值填充数组元素。使用它时，原始数组会被修改。它采用以下语法：

```javascript
array.fill(value[, start[, end]])
```

`value` 参数表示要填充的静态值。`start` 参数是可选的。它是从填充开始的索引。它的默认值为 0，即数组中的第一个元素。`end` 参数也是可选的。它表示停止填充值的索引。该方法返回一个被修改后的数组。

考虑以下示例：

```html
<script>
var array1 = ["Nicholas", "Jane", "Alice", "Alice"];
var output = array1.fill("Joel");
document.writeln(array1);
</script>
```

代码将返回：

```text
Joel,Joel,Joel,Joel
```

数组中的所有值都被替换为 Joel。让我们看看如何提供或指定起始索引：

```html
<script>
var array1 = ["Nicholas", "Jane", "Alice", "Alice"];
var output = array1.fill("Joel", 2);
document.writeln(array1);
</script>
```

在上面的示例中，填充将从索引 2 之后的元素开始。代码应该返回：

```text
Nicholas,Jane,Joel,Joel
```

接下来的示例演示了我们如何同时指定起始和结束索引：

```html
<script>
var array1 = ["Nicholas", "Jane", "Alice", "Alice"];
var output = array1.fill("Joel", 2, 4);
document.writeln(array1);
</script>
```

#### every()

此方法的目的是检查所有数组元素是否满足给定的条件。如果所有数组元素都满足条件，该方法将返回 `true`，否则返回 `false`。该方法采用以下语法：

```javascript
array.every(callback[, thisArg])
```

`callback` 是测试条件的函数。`currentValue` 表示数组的当前元素。`index` 参数是可选的，它表示当前元素的索引。`array` 参数表示我们要应用 `every` 函数的数组。`thisArg` 是可选参数。这是在执行 `callback` 期间使用的值。该方法返回一个布尔值。

考虑以下示例：

```html
<script>
var marks = [20, 25, 30, 35, 40];
function confirm(x) {
  return x > 10;
}
document.writeln(marks.every(confirm));
</script>
```

代码返回 `true`。我们定义了一个包含一组整数值的数组，即 `marks`。所有的 marks 都大于 10。`confirm` 的目的是检查所有 marks 是否都大于 10。由于这是真的，`every()` 函数返回 `true`。让我们将其中一个值改为小于 10，并看看会发生什么：

```html
<script>
var marks = [20, 5, 30, 35, 40];
function confirm(x) {
  return x > 10;
}
document.writeln(marks.every(confirm));
</script>
```

代码将返回 `false`，因为索引 1 处的 marks 小于 10，即 5。

在下面的示例中，我们正在检查数组中元素的索引：

```html
<script>
var marks = [20, 25, 30, 35, 40];
function confirm(item, index) {
  return index < 3;
}
document.writeln(marks.every(confirm));
</script>
```

输出如注释所示。在第一次执行中，我们传递了一个包含两个元素的数组。由于我们只有两个，这将带给我们 `true`。在第二种情况下，我们的数组有 5 个元素。由于这些超过了 3 个，它将返回 `false`。

#### find()

此方法将返回数组中满足指定条件的第一个元素。它采用以下语法：

```javascript
array.find(callback[, thisArg])
```

```javascript
function checkPrime(item) {
  for (let i = 2; i <= Math.sqrt(item); i++) {
    if (item % i === 0) {
      return false;
    }
  }
  return item > 1;
}

document.writeln([4, 5, 7, 11].find(checkPrime));
```

该函数将找到质数 5。

#### forEach()

此方法帮助我们为数组中的每个元素调用一次特定的函数。它采用如下语法：

```javascript
array.forEach(callback(currentValue, index, array))
```

`callback` 是用于测试条件的函数。`currentValue` 表示数组的当前元素。`index` 参数是可选的，它表示当前元素的索引。`array` 参数表示要应用函数的数组。`thisArg` 是一个可选参数，它是执行回调期间用作 `this` 的值。

```javascript
var array = ["Java", "C", "Python"];
array.forEach(function(values) {
  document.writeln(values);
});
```

我们使用了 `forEach()` 方法来访问并打印数组元素。代码将打印以下内容：

```text
Java
C
Python
```

我们也可以使用相同的函数来创建一个斐波那契序列。

```javascript
var addition = 0;
var array = [1, 1, 2, 3, 5];
array.forEach(function(item) {
  addition = addition + item;
  document.writeln(addition);
});
```

该代码将返回数组元素的斐波那契序列。注意，斐波那契是元素的顺序累加。以下是输出：

```text
1
2
4
7
12
```

#### pop()

此方法将从数组中删除最后一个元素并返回该元素。它具有改变数组长度的效果。其简单语法所示：

```javascript
array.pop()
```

```javascript
var array = ["Java", "C", "Python"];
document.writeln(array);
document.writeln("" + array.pop());
document.writeln(array);
```

该代码将返回以下内容：

```text
初始数组: Java,C,Python
弹出的项目: Python
最终数组: Java,C
```

我们可以使用 `for` 循环来弹出所有数组元素。例如：

```javascript
var array = ["Java", "C", "Python"];
var len = array.length;
for (var i = 0; i < len; i++) {
  document.writeln(array.pop());
}
```

代码将打印以下内容：

```text
弹出的元素: Python
弹出的元素: C
弹出的元素: Java
```

#### reverse()

此方法的影响是改变数组项目的排序方式，并按反序返回项目。

数组的第一个元素将变成最后一个，而最后一个元素将变成第一个元素。其简单语法所示：

```javascript
array.reverse()
```

它返回按反序排列的数组原始项目。

```javascript
var array = ["Java", "C", "Python"];
var rv = array.reverse();
document.writeln(rv);
```

该代码将返回以下输出：

```text
Python,C,Java
```

数组元素已按反序顺序返回。

---

## 第 11 章 字符串

在 JavaScript 中，字符串是字符的序列。在 JavaScript 中，我们可以通过两种方式创建字符串：使用字面量和使用字符串对象。

字符串字面量是通过使用双引号创建的。要使用字面量创建字符串，请使用如下语法：

```javascript
var string_name = "Hello";
document.write(string_name);
```

要使用字符串对象创建字符串，请使用 `new` 关键字。语法应如下所示：

```javascript
var string_name = new String("Hello");
```

我们使用了 `new` 关键字来创建字符串的实例。考虑下面的示例：

```javascript
var st = new String("Hello");
document.write(st);
```

代码将返回以下结果：

```text
Hello
```

让我们讨论与 JavaScript 字符串相关的各种方法：

### charAt()

此方法有助于找到位于特定索引处的字符值。索引从 0 开始到 n-1，其中 n 是字符串中字符的总数。索引值不能为负值，不能等于或大于字符串的长度。该方法采用如下语法：

```javascript
string.charAt(index)
```

索引代表字符。

```javascript
var st = "JavaScript";
document.writeln(st.charAt(5));
```

我们也可以使用该方法而不向其传递索引。下文所示：

```javascript
var st = "JavaScript";
document.writeln(st.charAt());
```

代码将仅打印字符串的第一个字符，即 `J`。

### concat()

此方法有助于将两个或多个字符串连接在一起形成一个单个字符串。注意，该方法不会以任何方式更改原始字符串。该方法采用如下语法：

```javascript
string.concat(string1, string2, ...)
```

注意方法的参数是要连接的字符串。

考虑下面的示例：

```javascript
var a = "Hello ";
var b = "World";
document.writeln(a.concat(b));
```

代码执行后将返回以下内容：

```text
Hello World
```

我们创建了字符串 `a` 和 `b` 并使用 `concat()` 方法将它们结合。下面的示例演示了我们如何将三个字符串结合：

```html
<script>
var a = "Hello ";
var b = "World";
var c = " JavaScript";
document.writeln(a.concat(b, c));
</script>
```

注意，我们在编写字符串时创建了一些空格。还有另一种实现方法，如下所示：

```html
<script>
var a = "Far";
var b = " ";
var c = "3Away";
document.writeln(a.concat(b + c));
</script>
```

### indexOf()

此方法可以用于搜索并返回字符串中某个字符的位置。始终记住，字符串字符从索引 0 开始。如果未找到该字符，该方法将返回 -1。

例如：

```html
<script>
var st = "Hello JavaScript";
document.write(st.indexOf("a"));
</script>
```

代码返回 1。这是因为在索引 1 处找到了第一个字符 "a"。我们可以提供搜索开始的索引。演示所示：

```html
<script>
var st = "Hello JavaScript";
document.write(st.indexOf("a", 8));
</script>
```

代码返回 9。这是因为我们规定搜索应该从索引 8 开始而不是从索引 0 开始。

除了单个字符，我们还可以打印某个字符串第一个字符的位置。

例如：

```html
<script>
var st = "Hello JavaScript";
document.write(st.indexOf("s"));
</script>
```

代码返回 6。这是字符 's' 在脚本中的位置。注意，搜索是区分大小写的；因此，JavaScript 中的 Script 将被跳过。你可以在搜索中使用 `Script` 而替 `script`，你将得到不同的结果。

为了避免这种混淆，我们可以为 JavaScript 提供搜索开始的索引：

```html
<script>
var st = "Hello JavaScript";
document.write(st.indexOf("s", 6));
</script>
```

现在搜索将从索引 6 开始而不是从索引 0 开始。

我们可以尝试搜索一个不存在的元素并看看会发生什么：

```html
<script>
var st = "Hello JavaScript";
document.write(st.indexOf("Java", 1));
</script>
```

脚本将返回 6。因为 "Java" 从索引 6 开始。

### search()

该方法用于在字符串中搜索正则表达式。如果没有找到匹配项，该方法将返回 -1。该方法通常具有下面的语法：

```javascript
string.search(regexp)
```

参数 `regexp` 表示要搜索的表达式。该方法通常返回你正在搜索的字符的位置。考虑下面的示例：

```html
<script>
var st = "Hello JavaScript";
document.write(st.search("Java"));
</script>
```

代码返回 6。字符串 "Java" 从索引 6 开始。注意，search 方法是区分大小写的。下面的示例演示了这一点：

```html
<script>
var st = "Hello JavaScript";
document.write(st.search("Script"));
</script>
```

代码返回 10。这是因为它正在搜索一个大写的 S。为了忽略搜索的大小写敏感性，我们可以如下所示使用 `i` 标志：

```html
<script>
var st = "Hello JavaScript";
document.write(st.search(/script/i));
</script>
```

代码现在返回 6 而不是 10。这是因为搜索不再区分大小写了。现在让我们搜索一个字符串中不存在的正则表达式，看看会发生什么：

```html
<script>
var st = "Hello JavaScript";
document.write(st.search(/programming/));
</script>
```

代码返回 -1，因为没有找到该正则表达式。

### match()

该方法帮助我们将字符串与正则表达式匹配。`match()` 方法可以使用全局搜索修饰符来获取所有匹配元素，否则该方法将只返回找到的第一个元素。`match()` 方法采用以下语法：

```javascript
string.match(regexp)
```

`regexp` 是你需要搜索的正则表达式。考虑下面的示例：

```html
<script>
var st = "Hello JavaScript";
document.write(st.match(/Java/));
</script>
```

代码将返回 `["Java", index: 6, input: "Hello JavaScript", groups: undefined]`。我们可以演示如何使用全局搜索进行搜索：

```html
<script>
var st = "Hello JavaScript";
document.write(st.match(/Java/g));
</script>
```

`match()` 方法是区分大小写的。然而，我们可以通过使用忽略标志将其关闭。演示所示：

```html
<script>
var st = "Hello JavaScript";
document.write(st.match(/java/gi));
</script>
```

代码返回 `["Java", index: 6, input: "Hello JavaScript", groups: undefined]`。这表明搜索不再像以前那样区分大小写。

---

## 第 12 章 JavaScript 事件

事件是 JavaScript 可以检测到的动作。一个很好的例子是 `onmouseover` 事件，当鼠标移动到某些对象上时，JavaScript 会检测到它。`onload` 事件在网页加载后触发。在 JavaScript 中，事件和函数一起使用。函数在事件发生后触发。其他事件示例包括关闭窗口、按键、调整窗口大小等。

### onclick 事件

这是 JavaScript 中一种常见的事件。它在用户点击左键时发生。可以针对该事件添加警告、验证等。示例：

```html
<html>
<head>
<script type="text/javascript">
function helloFunc() {
  alert("Hello World!");
}
</script>
</head>
<body>
<p>点击下方的按钮</p>
<form>
<input type="button" onclick="helloFunc()" value="点击这里"/>
</form>
</body>
</html>
```

在示例中，创建了一个简单的表单。点击“点击这里”按钮将调用函数 `helloFunc()`。一旦点击，你将看到如下所示的弹窗：

```text
Hello World!
```

### onsubmit 事件

当提交表单时会调用此事件。可以在事件中添加表单验证。这将帮助你在将数据发送到 Web 服务器之前对其进行验证。

示例：

```html
<html>
<head>
<script type="text/javascript">
function formValidation() {
    return true; // 或 false
}
</script>
</head>
<body>
<form method="post" onsubmit="return formValidation()">
<input type="text" value="5"/>
<input type="submit" value="提交"/>
</form>
</body>
</html>
```

一旦点击提交按钮，将调用 `formValidation()` 方法。

### onmouseout 和 onmouseover

这些事件可以帮助你为文本和图像添加吸引人的特性。`onmouseover` 事件在鼠标移动到对象上时触发。`onmouseout` 事件在鼠标移出元素时触发。

示例：

```html
<html>
<head>
<script type="text/javascript">
function overObject() {
    document.write("Over");
}
function outOfObject() {
    document.write("Out");
}
</script>
</head>
<body>
<p>将你的鼠标移入区域内并观察：</p>
<div onmouseover="overObject()" onmouseout="outOfObject()">
<h2>区域</h2>
</div>
</body>
</html>
```

该代码执行时会产生以下结果：

```text
将你的鼠标移入区域内并观察：
区域
```

按照指示移动你的鼠标并看发生了什么。

我们定义了两个函数，即 `overObject()` 和 `outOfObject()`。这两个函数在接下来的行中被调用：

```html
<div onmouseover="overObject()" onmouseout="outOfObject()">
```

一旦鼠标移到区域内，将调用 `overObject()` 方法。一旦鼠标移出对象，将调用 `outOfObject()` 方法。

`onmouseover="overObject()"` 指示 JavaScript 在鼠标移入区域时调用 `overObject()` 函数，而 `onmouseout="outOfObject()"` 指示 JavaScript 解释器在鼠标移出区域时调用 `outOfObject()` 函数。

这是另一个在悬停后改变文本颜色的示例：

```html
<html>
<body onmouseover="overObject()" onmouseout="outOfObject()">
将光标移到这里
</body>
</html>
```

当你将鼠标光标移到文本上，文本颜色将变为黄色。如果你移开光标，文本颜色将变为黑色。

### onload 和 onunload 事件

这两个事件在用户进入或离开页面时被调用。我们可以使用 `onload` 事件来检查访问者的浏览器类型和版本。

以下是另一个在页面加载时根据 Cookie 处理的示例：

```html
<html>
<body onload="inspectCookies()">
<script>
function inspectCookies() {
    var txt = "";
    if (navigator.cookieEnabled) {
        txt = "Enabled";
    } else {
        txt = "Disabled";
    }
    document.body.innerHTML = txt;
}
</script>
</body>
</html>
```

运行上述代码，结果将取决于浏览器是否启用了 Cookie。

### onchange 事件

`change` 事件通常用于表单字段。以下示例展示了如何使用该方法：

```html
<html>
<head>
<script type="text/javascript">
function test() {
    var a = document.getElementById('name');
    a.value = a.value.toUpperCase();
}
</script>
</head>
<body>
<input type="text" id="name" onchange="test()">
</body>
</html>
```

运行该代码后，你将看到如下表单。在输入框内输入小写字母并点击外部，你会注意到你的姓名被转换为大写。

`toUpperCase()` 方法在用户更改输入框的内容后被调用。

### onfocus 事件

`onload` 被使用时，会显示一个警告。例如：

```html
<html>
<head>
<script type="text/javascript">
function displayMessage() {
    alert("Page Loaded");
}
</script>
</head>
<body onload="displayMessage()">
</body>
</html>
```

页面加载后，`onload` 事件可以让输入框在获得焦点时改变颜色。这里有一个示例：

```html
<html>
<head>
<script type="text/javascript">
function myFunc(col) {
    col.style.backgroundColor = "yellow";
}
</script>
</head>
<body>
姓名:
<input type="text" onfocus="myFunc(this)">
<p>点击输入框内看它的颜色变化</p>
</body>
</html>
```

执行该代码你将得到以下结果：

```text
姓名：
点击输入框内看它的颜色变化。
```

输入框的颜色将变为黄色。

---

## 第 13 章 JavaScript 验证

通过 JavaScript，用户可以在提交表单之前对其进行验证。最初，表单验证是在服务器端完成的。用户填写表单并发送到服务器。如果发现详情错误，服务器必须将其发回给用户进行修改。这个过程太耗时了。

然而，JavaScript 改变并改进了这种方式。表单验证可以在提交到服务器之前在客户端完成。在表单验证中，我们应该确保所有必填字段都已填写。对于电子邮件、手机号码等特定数据格式的字段，应该检查其是否符合格式。表单验证通常在提交（submit）时完成。

示例：



```html
<html>
<head>
</head>
<script type="text/javascript">
function formValidation() {
    var name=document.detailsForm.username.value;
    var password=document.detailsForm.userpassword.value;
    if (name==null || name=="") {
        alert("Please enter your name!");
        return false;
    } else if (password.length<8) {
        alert("You must enter a password with 8 characters and above");
        return false;
    }
}
</script>
<body>
<form name="detailsForm" method='post' action='' onsubmit="return formValidation()">
Name: <input type="text" name='username'><br/>
Password: <input type='password' name='userpassword'><br/>
<input type="submit" value="Login">
</form>
</body>
</html>
```

该代码返回如下所示的简单表单：

| Name: | |
| :--- | :--- |
| Password: | | Login |

在不在任何输入字段中输入值的情况下直接点击 Login 按钮；你将得到以下警告框：

You MUST enter your name!

这意味着你必须在继续之前输入你的姓名。

现在，输入你的姓名但不输入密码。你将得到以下警告框：

You MUST enter a password with 8 characters and above... 这意味着你必须输入 8 个字符及以上的密码。你现在可以输入短密码并查看验证是否正常工作。输入一个少于 8 个字符的密码然后点击 Login 按钮。你仍然会收到上面的对话框。我们创建了一个名为 `detailsForm` 的表单。该表单要求用户输入姓名和密码。我们创建了 `formValidation` 方法来验证表单中输入的值。必须提供用户名，而密码不能少于 8 个字符。属性 `onsubmit="return formValidation()"` 意味着一旦用户点击“Login”按钮，就会调用 `formValidation` 方法来验证表单中输入的详情。如果不符合要求，它将返回 false，因此用户必须重新输入详情。

### 验证重复输入密码

当用户创建密码时，通常会被要求重复输入以确保他们已经牢牢掌握了。这种逻辑在 JavaScript 中可以这样实现：

```javascript
<script type="text/javascript">
function passwordMatch() {
    var firstpassword=document.myform.userpassword.value;
    var secondpassword=document.myform.userpassword2.value;
    if (firstpassword==secondpassword) {
        return true;
    } else {
        alert("Passwords don't match!");
        return false;
    }
}
</script>
<form name="myform" action="register.jsp" onsubmit="return passwordMatch()">
Password:<input type="password" name="userpassword"/><br/>
Re-enter Password:<input type="password" name="userpassword2"/><br/>
<input type="submit" value="Submit Query">
</form>
```

这返回了如下简单表单：

| Password: | |
| :--- | :--- |
| Re-enter Password: | | Submit Query |

### 数字验证

当要求用户在特定的文本字段中输入数字（如年龄）时，验证输入内容以确保他们只输入数字。如下所示：

```javascript
<script type="text/javascript">
function formValidation() {
    var number=document.form.num.value;
    if (isNaN(number)) {
        document.getElementById("num").innerHTML="Input must be a number!";
        return false;
    } else {
        return true;
    }
}
</script>
<form name="form" onsubmit="return formValidation()">
Number: <input type="text" name="num"><span id="num"></span><br/>
<input type="submit">
</form>
```

`isNaN` 方法在 JavaScript 中用于检查一个值是否为数字。我们在上面的脚本中使用了它。运行代码，你将得到一个包含输入字段和一个按钮的表单，如下所示：

在输入字段中输入非数字值然后点击 Submit 按钮。你将看到以下消息：

Input must be a number!

如果输入不是数字，代码将返回指定的消息。

### 电子邮件验证

JavaScript 可用于验证电子邮件地址。以下是有效电子邮件地址的属性：

- 它必须包含 `@` 和点（dot）符号
- 在 `@` 之前和之后都应该有字符
- 在点（dot）之后必须至少有两个字符。

示例：

```javascript
<script type="text/javascript">
function emailValidation() {
    var i=document.form.emailAddress.value;
    var atposition=i.indexOf("@");
    var dotposition=i.lastIndexOf(".");
    if (atposition<1 || dotposition<atposition+2 || dotposition+2>=i.length) {
        alert("Invalid email address!");
        return false;
    }
}
</script>
```

```html
<form name="form1" method="post" action="" onsubmit="validate()">
Email: <input type="text" name="email"/><br/>
<input type="submit" value="Submit Mail"/>
</form>
```

代码执行后返回以下内容：

Email: | 提交邮件 |

尝试输入一个无效的电子邮件地址并点击提交邮件按钮。看看会发生什么。你应该得到以下警报框：

请提供有效的电子邮件地址

在位置:-1

点位置:-1

### 带图片的验证

你可能需要根据输入是否正确来显示不同的图片。

![](img/9481f3f28a383c4a6640042d4f3a3962_140_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_140_1.png)

可以通过 JavaScript 如下方式实现：

```javascript
<script type="text/javascript">
function formValidation() {
    var name=document.form1.name.value;
    var password=document.form1.password.value;
    var status=false;
    if(name.length < 5) {
        document.getElementById("namespan").innerHTML="";
        status=false;
    } else {
        document.getElementById("namespan").innerHTML="";
        status=true;
    }
    if (password.length < 8) {
        document.getElementById("passwordspan").innerHTML="";
        status=false;
    } else {
        document.getElementById("passwordspan").innerHTML="OK!";
    }
    return status;
}
</script>
```

```html
<form name="form" action="" onsubmit="">
<table>
  <tr><td>输入姓名：</td><td><input type="text" name="name"/><span id="namespan"></span></td></tr>
  <tr><td>输入密码：</td><td><input type="password" name="password"/><span id="passwordspan"></span></td></tr>
  <tr><td colspan="2"><input type="submit" value="登录"/></td></tr>
</table>
</form>
```

脚本执行后返回此简单表单：

输入姓名：

输入密码：

登录

![](img/9481f3f28a383c4a6640042d4f3a3962_142_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_142_1.png)

在不输入用户名或密码的情况下点击登录按钮。你会在相关消息旁边看到图片。

输入姓名：

请提供你的姓名

输入密码：

密码长度应至少为 8 个字符

登录

![](img/9481f3f28a383c4a6640042d4f3a3962_143_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_143_1.png)

## 第 11 章 - 文档对象模型 (DOM)

文档对象指的是你的整个 HTML 页面。当你将一个对象加载到网页浏览器后，它立即成为一个文档对象，即代表 html 文档的根元素。它同时包含属性和方法。它是 window 的对象，这意味着拥有 document 就同于拥有 window。

方法是你可以在 html 元素上执行的操作。属性是人们设置或更改的 HTML 元素的值。以下是文档对象方法：

- `write("string")` - 向文档写入字符串。
- `eln("string")` - 向带有换行符的文档写入字符串。
- `getElementById()` - 给出具有指定 id 的元素。

![](img/9481f3f28a383c4a6640042d4f3a3962_144_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_144_1.png)

- `getElementsByName()` - 获取所有指定名称的元素。
- `getElementsByTagName()` - 获取所有指定标签名的元素。
- `getElementsByClassName()` - 获取所有指定类名的元素。

DOM 是获取输入字段值的好方法。很多时候，你需要从用户那里获取输入。可以使用以下属性完成：`document.form.name.value`。

其中 `document` 是代表我们根元素的 html 文档。

- `form` 是带有字段的表单名称。
- `name` 是输入文本的名称。
- `value` 是一个返回输入文本值的属性。

考虑以下示例：

```html
<html>
<body>
<script type="text/javascript">
function readValue() {
    var name=document.memberform.memberName.value;
    alert(+name);
}
</script>
<form name="memberform">
    输入姓名：<input type="text"/>
    <input type="button" value="点击" onclick="readValue"/>
</form>
</body>
</html>
```

运行代码时，它会给你这个简单的表单：

输入姓名：| 点击这里

在输入字段中输入你的姓名并点击这里按钮。看看会发生什么。

![](img/9481f3f28a383c4a6640042d4f3a3962_146_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_146_1.png)

你会得到一个带有你名字的警报框：

你好：John

我们创建了一个带有输入字段的简单表单。`readValue()` 方法帮助我们获取输入的内容。考虑以下行：

`var name=document.memberform.memberName.value;`

`memberName` 是表中文本字段的名称，必须匹配，否则你将无法获得结果。除了名称，我们还可以通过 id 获取元素。这可以通过 `getElementById` 方法完成。然而，输入文本字段应该赋予一个 id。例如：

```html
<html>
<body>
<script type="text/javascript">
function computeSquare() {
    var x=document.getElementById("integer").value;
    alert(x*x);
}
</script>
<form>
    输入整数：<input type="text" id="integer"/>
    <input type="button" value="计算" onclick="computeSquare"/>
</form>
</body>
</html>
```

![](img/9481f3f28a383c4a6640042d4f3a3962_147_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_147_1.png)

这应该在弹出框中返回数字的平方：

在示例中，我们定义了 `computeSquare` 方法，它帮助我们获取输入到文本字段的数字。考虑以下行：

`var x=document.getElementById("integer").value;`

`getElementById` 方法接收输入字段的 id 作为参数。

`document.getElementsByName()` 方法可以帮助我们通过名称获取元素。方法的语法如下：

`document.getElementsByName()`

需要名称。

![](img/9481f3f28a383c4a6640042d4f3a3962_149_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_149_1.png)

示例：

```html
<html>
<body>
<script type="javascript">
function getNumber() {
  var options = document.getElementsByName("option");
  alert(options.length);
}
</script>
<form>
  Yes:<input type="radio" name="option" value="Yes">
  No:<input type="radio" name="option" value="No">
  <input type="button" onclick="getNumber()" value="Available Options">
</form>
</body>
</html>
```

执行后，代码将返回以下内容：

| 是 | 否 | 可用选项 |
| :--- | :--- | :--- |
| @ | @ | |

![](img/9481f3f28a383c4a6640042d4f3a3962_150_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_150_1.png)

点击“Available Options”按钮查看发生了什么。将显示如下弹出窗口：

总选项数：2

我们创建了两个带有 Yes 和 No 选项的单选按钮。注意，这两个输入类型被赋予了相同的名称，即 option。

考虑以下行：

`var options=document.getElementsByName("option");`

该行帮助我们统计名称为 option 的元素数量。如输出所示，该数量应该是 2。

### getElementsByTagName()

`document.getElementsByTagName()` 属性返回具有指定标签名称的元素。它采用以下语法：

`document.getElementsByTagName("name")`

![](img/9481f3f28a383c4a6640042d4f3a3962_151_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_151_1.png)

例如：

```html
<html>
<body>
<script type="javascript">
function allparagraphs() {
  var pgs = document.getElementsByTagName("p");
  alert(pgs.length);
}
</script>
<p>这是一个段落</p>
<p>这是一个段落</p>
<p>这是一个段落</p>
<p>这是一个段落</p>
<button onclick="allparagraphs()">Total Paragraphs</button>
</body>
</html>
```

代码执行后返回以下内容：

这是一个段落

这是一个段落

这是一个段落

这是一个段落

| 总段落数 |
| :--- |
| 4 |

![](img/9481f3f28a383c4a6640042d4f3a3962_152_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_152_1.png)

点击“Total Paragraphs”按钮查看发生了什么。你将看到以下弹出窗口：

段落总数为：4

这意味着代码能够数出我们拥有的段落数量。

主要逻辑在于以下行：

`var pgs=document.getElementsByTagName("p");`

我们将标签 "p" 作为参数传递给方法，该标签代表一个段落。有四个标签为 "p" 的元素，所以输出应该是 4 个段落。这里是另一个例子：

```html
<html>
<body>
<script type="javascript">
function count2() {
  var h2count = document.getElementsByTagName("h2");
  alert("+" + h2count.length);
}
function count3() {
  var h3count = document.getElementsByTagName("h3");
  alert("+" + h3count.length);
}
</script>
<h2>A</h2><h2>A</h2><h2>A</h2><h2>A</h2>
<h3>A</h2><h3>A</h2><h3>A</h2><h3>A</h2><h3>A</h2>
<h2>A</h2><h2>A</h2><h2>A</h2><h2>A</h2>
<h3>A</h2><h3>A</h2><h3>A</h3>
<button onclick="count2()">Total h2</button>
<button onclick="count3()">Total h3</button>
</body>
</html>
```

![](img/9481f3f28a383c4a6640042d4f3a3962_153_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_153_1.png)

代码执行后返回以下输出：

| h2 | h3 |
| :--- | :--- |
| 4 | 5 |

我们有 4 个 h2 标签和 5 个 h3 标签。点击“Total h2”按钮查看发生了什么。你应该得到以下弹出窗口：

h2 标签数：4

点击“Total h3”按钮查看发生了什么：

h3 标签数：5

### innerHTML

该属性可用于向 HTML 页面中添加动态内容。当需要生成注释表单、注册表单等动态内容时可以使用它。考虑以下示例：

```html
<html>
<body>
<script type="javascript">
function displayform() {
  var data = document.getElementById("area");
  area.innerHTML = data;
}
</script>
<form name="a">
  <input type="text" value="" onclick="displayform()">
  <div id="area"></div>
</form>
</body>
</html>
```

![](img/9481f3f28a383c4a6640042d4f3a3962_154_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_154_1.png)

### innerText

我们可以使用此属性向 HTML 页面添加动态属性。注意，当使用此属性时，你的文本被解释为普通文本而非 HTML 内容。该属性的一个良好场景是需要根据长度编写密码强度、编写验证信息等。例如：

```html
<html>
<body>
<script type="javascript">
function validatePass() {
  var message;
  if (document.form.userPass.value.length > 5) {
    message = "强";
  } else {
    message = "弱";
  }
  document.getElementById("area").innerText = message;
}
</script>
<form name="a">
  <input type="password" value="" name="userPass" onkeyup="validatePass()">
  强度:<span id="area">弱</span>
</form>
</body>
</html>
```

代码执行后返回以下内容：

强度：弱

只需开始输入密码，观察在你输入时输入框右侧文本发生了什么变化。如果你输入的密码少于 5 个字符，消息将变为“弱”，如下所示：

强度：弱

继续输入密码直到超过 5 个字符。你将看到消息变为“强”，如下所示：

强度：强

这就是该属性的强大之处。

## 动画

通过 JavaScript，我们可以对元素实现动画。我们可以根据公式使用 JavaScript 移动页面上的元素，如 `<img> />`、`<div>` 等。以下是 JavaScript 动画中常用的常用方法：

1. `setTimeout(method, time)` - 该方法将在若干毫秒后调用指定的方法。
2. `setInterval(method, time)` - 该方法每隔指定的毫秒数调用一次指定的方法。

通过 JavaScript，人们可以设置 DOM 对象的某些属性，例如它在屏幕上的位置。可以使用 `top` 和 `left` 属性来设置对象的位置。下文所示：

`object.style.left = 点或像素单位的距离；或使用字符串“距离屏幕顶部的距离!";`

`object.style.top = 点或像素单位的距离;`

![](img/9481f3f28a383c4a6640042d4f3a3962_160_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_160_1.png)

### 手动动画

在下面的示例中，我们将使图像向右移动动画：

```html
<html>
<head>
<script type="text/javascript">
var image = null;
function init() {
    image = document.getElementById('myImage');
    image.style.position = 'relative';
    image.style.left = '0px';
}
function moveImage() {
    image.style.left = parseInt(image.style.left) + 10 + 'px';
}
window.onload = init;
</script>
</head>
<body>
<form>
<img id="myImage" src="house.jpg" />
<p>点击按钮移动图像</p>
<input type="button" value="Move Image" onclick="moveImage()" />
</form>
</body>
</html>
```

你应当在以下这一行中使用你图片的正确名称：

`<img id="myImage" src="house.jpg" />`

在我的案例中，我有一个名为 `house.jpg` 的 `.jpg` 图片。当我运行代码时，它会返回以下内容：

点击按钮移动图像

| Move Image |

![](img/9481f3f28a383c4a6640042d4f3a3962_162_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_162_1.png)

点击“Move Image”按钮。图像在每次点击时应向右移动。如下所示：

点击按钮移动图像

| Move Image |

考虑脚本中的这一行：

`image = document.getElementById('myImage');`

我们正在通过其 ID 获取图像，然后将其赋值给变量 `image`。`init()` 方法帮助我们设置图像在窗口上的初始位置。该方法会在窗口加载完成时被调用。`moveImage()` 函数将在点击后将图像向右移动 10 像素。要让图像向左移动，则应将值设置为负数。在这种情况下，动画是手动的，因为我们必须点击按钮。

### 自动动画

为了使元素动画过程自动化，我们可以使用 JavaScript 提供的 `setTimeout()` 函数。示例：

```html
<html>
<head>
<script type="text/javascript">
var image = null;
var animate;
function init() {
    image = document.getElementById('myImage');
    image.style.position = 'relative';
    image.style.left = '0px';
}
function moveImage() {
    image.style.left = parseInt(image.style.left) + 10 + 'px';
    animate = setTimeout(moveImage, 20);
}
function stopAnimation() {
    clearTimeout(animate);
    image.style.left = '0px';
}
window.onload = init;
</script>
</head>
<body>
<form>
<img id="myImage" src="house.jpg" />
<p>点击 Animate 按钮启动动画</p>
<input type="button" value="Animate" onclick="moveImage()" />
<input type="button" value="Stop" onclick="stopAnimation()" />
</form>
</body>
</html>
```

代码执行后返回以下内容：

![](img/9481f3f28a383c4a6640042d4f3a3962_164_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_164_1.png)

点击“Animate”按钮。动画应该开始。当你点击 Stop 按钮时，动画将停止。`animateImage()` 方法调用 `setTimeout` 方法，在 20 毫秒后设置图像的位置。这将导致图像的动画。`stopAnimation()` 方法有助于清除由 `setTimeout()` 方法设置的计时器。对象（即图像）被设回初始位置。

### 鼠标悬停 (Rollover)

我们可以在 JavaScript 中使用鼠标图像来实现图像的悬停切换。一旦你将鼠标移动到图像上，它将变为另一张图像。示例：

```html
<html>
<head>
<script type="text/javascript">
if (document.images) {
    var img1 = new Image();
    var img2 = new Image();
    img1.src = "house.jpg";
    img2.src = "house2.jpg";
}
</script>
</head>
<body>
<p>鼠标移过进行悬停切换</p>
<a href="#" onmouseover="this.querySelector('img').src=img2.src" onmouseout="this.querySelector('img').src=img1.src">
<img src="house.jpg" />
</a>
</body>
</html>
```

我们使用了 `if` 语句来检查图像是否存在。我们使用了 `Image` 构造函数来预加载一些名为 `img1` 的对象。对第二张图像 `img2` 也执行了相同的操作。`src` 被赋予了外部存储的图像名称。

![](img/9481f3f28a383c4a6640042d4f3a3962_167_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_167_1.png)

## 第 12 章 - 浏览器对象模型

BOM（浏览器对象模型）用于与浏览器进行交互。默认的浏览器对象是 `window`，这意味着你可以直接调用所有窗口函数，或者通过指定 `window.` 来调用。我们已经讨论过这一点，所以不再重复。除了 `window` 对象外，还有许多其他的 BOM 对象。让我们来讨论它们：

### History 对象

该对象保留了用户访问的所有 URL 数组。你可以使用此对象来加载网页、后退、前进以及任何特定的网页。可以通过如下方式访问此对象：

`window.history`

它也可以如下所示访问：

该对象只有一个属性，即 `length`，它返回历史记录 URL 的长度。history 对象包含 3 个方法，包括：

- `forward(-);` - 它将加载下一个页面
- `back();` - 它将加载上一个页面
- `go(?);` - 它将加载指定页码的页面。

![](img/9481f3f28a383c4a6640042d4f3a3962_169_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_169_1.png)

history 对象可以以以下多种方式使用：

1. `history.back();` // 用于上上一页
2. `history.forward();` // 用于后一页
3. `history.go(2);` // 用于后第 2 页
4. `history.go(-2);` // 用于上第 2 页

## Navigator 对象

该对象用于检测浏览器。它可以帮助获取有关浏览器的信息，如 appName、userAgent、appCodeName 等。navigator 对象是 window 的一个属性，我们可以如下方式访问它：

`window.navigator`

也可以通过如下方式访问：

`navigator`

该对象带有各种属性，包括：

- `appName` - 返回应用名称
- `appCodeName` - 返回代码代号
- `appVersion` - 返回版本号
- `cookieEnabled` - 如果启用了浏览器 cookie 则返回 true，否则返回 false

![](img/9481f3f28a383c4a6640042d4f3a3962_170_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_170_1.png)

- `language` - 返回语言。仅在 Firefox 和 Netscape 中支持。
- `userAgent` - 返回用户代理字符串。
- `userLanguage` - 返回用户的语言。仅在 IE 中支持。
- `systemLanguage` - 返回系统语言。仅在 IE 中支持。
- `Plugins` - 返回插件。仅在 Firefox 和 Netscape 中支持。
- `mimeTypes[]` - 返回 mime 类型的数组。仅在 Firefox 和 Netscape 中支持。
- `online` - 如果浏览器在线则返回 true，否则返回 false。
- `platform` - 返回平台，例如 Win32。

navigator 对象具有以下方法：

- `javaEnabled()` - 检查是否已启用 java。
- `tlsEnabled()` - 检查是否已启用 tls。自 JavaScript 1.2 起被弃用。

请考虑下面的 navigator 对象示例：

```javascript
document.writeln(+navigator.appName);
document.write(""+navigator.appCodeName);
document.writeln(""+navigator.language);
document.writeln(""+navigator.cookieEnabled);
document.writeln("+navigator.userAgent);
document.writeln(""+navigator.platform);
```

该代码返回以下详情：

appName: Netscape

appCodeName: Mozilla

appVersion: 5.0 (Windows)

language: en-US

cookieEnabled: true

userAgent: Mozilla/5.0 (Windows NT 6.1; WOW64; rv:52.0) Gecko/2010101 Firefox/52.0

platform: Win32

注意，输出取决于操作系统的类型、你使用的浏览器以及其他细节。

![](img/9481f3f28a383c4a6640042d4f3a3962_171_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_171_1.png)

## Screen

此 JavaScript 对象保存有关浏览器屏幕的信息。你可以用它显示屏幕的细节，如高度、宽度、像素深度、颜色深度等。它是 window 对象的属性，因此我们如下访问：

`window.screen`

我们也可以通过如下方式访问：

该对象有许多属性，包括：

- `width` - 返回浏览器屏幕的宽度
- `height` - 返回浏览器屏幕的高度
- `availWidth` - 输出可用宽度
- `availHeight` - 打印可用高度
- `colorDepth` - 返回颜色深度
- `pixelDepth` - 返回像素深度。

下面的示例显示了如何使用该对象：

```javascript
document.writeln(+screen.height);
document.writeln(+screen.width);
document.writeln(+screen.availHeight);
document.writeln(+screen.availWidth);
document.writeln(+screen.pixelDepth);
document.writeln(+screen.colorDepth);
```

代码执行后返回如下：

screen height: 768

screen width: 1366

screen availHeight: 728

screen availWidth: 1366

screen pixelDepth: 24

screen colorDepth: 24

有时，你可能需要将特定网页的内容发送到打印机。这可以通过添加用户需要点击的按钮来实现。

![](img/9481f3f28a383c4a6640042d4f3a3962_172_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_172_1.png)

## 打印

有时，你可能需要将特定网页的内容发送到打印机。这可以通过添加用户需要点击的按钮来实现。这可以使用 window 的 print 方法实现。当调用 `window.print()` 时，当前页面将被打印。

```html
<html>
<body>
<input value="Print" onclick="window.print()">
</body>
</html>
```

![](img/9481f3f28a383c4a6640042d4f3a3962_173_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_173_1.png)

## 第 13 章 Cookies

Cookies 指存储在计算机文本文件中的数据。在浏览期间，网页发送到用户的浏览器，而 Web 服务器会忘记这些。Cookies 有助于记住用户信息。一旦用户访问了网页，cookie 就可以帮助存储他的姓名。用户下次访问页面时会被记住。它们以如下键值对的形式保存：

username=John Joel

`document.cookie` 可用于 cookie 的创建、删除和读取。还可以以 UTC 添加过期日期。关闭浏览器后，cookie 将被删除。

![](img/9481f3f28a383c4a6640042d4f3a3962_174_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_174_1.png)

![](img/9481f3f28a383c4a6640042d4f3a3962_175_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_175_1.png)

![](img/9481f3f28a383c4a6640042d4f3a3962_176_0.png) ![](img/9481f3f28a383c4a6640042d4f3a3962_176_1.png)

示例：

`document.cookie` = `这就是你如何指定 cookie 的过期日期。也可以指定 cookie 的路径。`

示例：

`document.cookie` = 下面的脚本演示了这一点：

```html
<html>
<head>
<script type="javascript">
function CreateCookie() {
    if(document.form1.field.value == "") {
        alert("");
        return;
    }
    var value = escape(document.form1.field.value) + ";";
    document.cookie = "name=" + value;
    document.write(value);
}
</script>
</head>
<body>
<form name="" action="">
Name: <input type="text" name="field" />
<input type="button" value="Create Cookie" onclick="CreateCookie()" />
</form>
</body>
</html>
```

该代码在执行后将返回以下表单：

Enter name [ ] Create Cookie

在字段中输入名称，然后点击“Create Cookie”按钮。

你将看到：

Creating Cookies: name=John;name=Joel

cookie 将被创建。你将在计算机上拥有一个你输入的名称的 cookie。如果你需要一次创建多个 cookie，请用逗号分隔它们。

### 读取 Cookie

可以使用 `document.cookie` 对象读取 cookie。cookie 的名称会被传递给该对象。当你需要访问 cookie 时，可以随时使用该字符串。字符串 `document.cookie` 以 `name=value` 对的形式存储 cookie，并用分号分隔。name 表示 cookie 的名称，而 value 表示字符串值。

通过 `split()` 函数，可以拆分字符串以获取键和值。

示例：

```javascript
<script type="javascript">
function ReadCookies() {
    var cookies = document.cookie;
    document.write(cookies);
    var myArray = cookies.split(";");
    for (var x=0; x<myArray.length; x++) {
        var c = myArray[x].split("=");
        var name = c[0];
        var value = c[1];
        document.write(name + ": " + value + "<br>");
    }
}
</script>
```

### 删除 Cookie

有时，你可能不需要读取某个 cookie。这时你就删除它。删除 cookie 涉及给它分配一个早于当前日日期。

示例：

```html
<script type="javascript">
function DeleteCookie() {
    var time = new Date();
    time.setMonth(time.getMonth() - 1);
    var value = escape(document.form1.field.value);
    document.cookie = "name=" + value + "; expires=" + time.toUTCString() + ";path=/";
    document.write("Cookie deleted");
}
</script>
<body>
<form name="" action="">
Enter name: <input type="text" name="field" />
<input type="button" value="Delete Cookie" onclick="DeleteCookie()" />
</form>
```

在示例中，我们通过将 cookie 的过期日期设置为一个月前来删除该 cookie。该逻辑在代码的以下行中实现：

`time.setMonth(time.getMonth() - 1);`

## 第 14 章 面向对象编程

JavaScript 支持面向对象编程的概念。让我们讨论一下：

- JavaScript 类是一种特殊的函数。
- 类可以像函数表达式一样被定义。
- JavaScript 类有许多成员，包括方法或构造函数。
- JavaScript 类在严格模式下执行。因此，任何带有静错误或异常的代码都会抛出错误。

类语法由两个部分组成：声明和表达式。要声明一个类，我们使用 `class` 声明。这是通过 `class` 关键字后跟类名来实现。JavaScript 的命名规范要求类名必须大写字母开头。

以下是 JavaScript 类声明的示例：

```javascript
class Student {
    constructor(admission, name) {
        this.admission = admission;
        this.name = name;
    }
    detail() {
        document.write(this.admission + ": " + this.name);
    }
}

var student1 = new Student("John", "Joel");
var student2 = new Student("Mercy", "George");

student1.detail();
student2.detail();
```

该代码执行后返回以下内容：

John: Joel

Mercy: George

我们创建了一个名为 `Student` 的类。然后我们初始化了一个带有两个参数 `admission` 和 `name` 的构造函数。接着我们创建了一个名为 `detail` 的方法，它应该返回学生的详细信息，包括入学号和姓名。

考虑代码中提取的两行：

`var student1 = new Student("John", "Joel");`

`var student2 = new Student("Mercy", "George");`

我们所的操作被称为实例化。我们只是在创建 `Student` 类型的实例/对象。这意味着 `student1` 是 `Student` 的一个实例，因此它可以访问 `Student` 类中定义的所有属性。这同样适用于 `student2`。每个学生的详细信息已作为参数传递。最后我们调用了 `detail()` 方法来返回每个学生的详细信息。

在这种情况下，`length` 提供了数组长度。

以下示例中演示了这一点：

```html
<script>
class Student {
  constructor(admission, name) {
    this.admission = admission;
    this.name = name;
  }
  detail() {
    document.writeln(this.admission + this.name);
  }
}

var student1 = new Student();
var student2 = new Student();
student1.detail();
student2.detail();
</script>
```

上面的代码无法运行，因为我们在声明类之前就尝试访问它。一个类只能声明一次。如果你尝试声明多次，它将返回错误。这里有一个示例：

```html
<script>
class Student {
  constructor(admission, name) {
    this.admission = admission;
    this.name = name;
  }
  detail() {
    document.writeln(this.admission + this.name);
  }
}
var student1 = new Student();
var student2 = new Student();
student1.detail();
student2.detail();
</script>
```

上面的代码也无法运行，因为我们声明了两次类。

### 类表达式

类也可以使用类表达式（class expression）来定义。在这种情况下，类名不是强制性的。这意味着你可以有一个命名的或未名的类表达式。类表达式允许你获取类的名称。然而，类声明（class declaration）不允许这样做。

这是一个无名类表达式的示例：

```html
<script>
var stud = class {
  constructor(admission, name) {
    this.admission = admission;
    this.name = name;
  }
};
document.writeln(stud.name);
</script>
```

执行后，代码将返回以下内容：

undefined

类被赋值给了一个变量而不是被命名。通过类表达式，我们可以重新声明类。

```html
<script>
var stud = class {
  constructor(admission, name) {
    this.admission = admission;
    this.name = name;
  }
  detail() {
    document.writeln(this.admission + this.name);
  }
};
var student1 = new stud();
var student2 = new stud();
student1.detail();
student2.detail();
</script>
```

类表达式可以是命名的。在这种情况下，类名的作用域取决于类体。要检索类名，我们使用属性 `class.name`。考虑以下示例：

```html
<script>
var stud = class Student {
  constructor(admission, name) {
    this.admission = admission;
    this.name = name;
  }
  detail() {
    document.writeln(this.admission + this.name);
  }
};
document.writeln(stud.name);
</script>
```

代码成功运行并返回以下内容：

Student

现在让我们尝试按照如下编写代码：

```html
<script>
var stud = class Student {
  constructor(admission, name) {
    this.admission = admission;
    this.name = name;
  }
};
document.writeln(Student.name);
</script>
```

代码将生成一个错误。

### 对象

JavaScript 中的对象是一个既有状态又有行为的实体，即属性和方法。对象的示例可以是椅子、鼠标、键盘、笔等。

JavaScript 是基于对象工作的。它将一切都视为对象。它是基于模板的，而不是基于类的。创建类不是为了获取对象，但我们可以直接创建对象。JavaScript 为我们提供了三种创建对象的方法，包括：

- 使用对象字面量（object literal）
- 直接创建 Object 的实例（通过 `new` 关键字）
- 使用对象构造函数（通过 `new` 关键字）

#### 对象字面量

使用对象字面量创建对象，我们使用下面的语法：使用冒号（:）来分隔属性和值。

```html
<script>
var student = {
  admission: 380,
  name: "John Joel",
  age: 28
};
document.write(student.admission + student.name + student.age);
</script>
```

代码返回以下结果：

380John Joel28

输出清晰地显示 JavaScript 解释器能够理解这种语法的含义，即属性在前，值在后。这就是为什么它能够获取我们想要访问的属性值。

#### 创建对象实例

这是通过以下语法实现的：注意我们使用了 `new` 关键字来创建对象。

```html
<script>
var stud = new Object();
stud.admission = 380;
stud.name = "John Joel";
stud.age = 28;
document.write(stud.admission + stud.name + stud.age);
</script>
```

下面的示例演示了我们如何直接创建一个对象：

#### 使用对象构造函数

这涉及创建一个带有参数的函数。每个参数值都可以通过 `this` 关键字赋值给当前对象，`this` 表示当前对象。考虑以下示例：

```html
<script>
function stud(admission, name, age) {
  this.admission = admission;
  this.name = name;
}
</script>
```

```javascript
<script>
function stud(admission, name, age) {
    this.admission = admission;
    this.name = name;
    this.age = age;
    this.updateAge = updateAge;
    function updateAge(newAge) {
        this.age = newAge;
    }
}

var s = new stud(4380, "John Joel", 28);
document.write(s.admission + " " + s.name + " " + s.age);
s.updateAge(29);
document.write(s.admission + " " + s.name + " " + s.age);
</script>
```

该代码执行后返回如下：

4380 John Joel 28

JavaScript 允许我们在对象中定义方法。但在定义方法之前，我们应该首先定义一个与方法同名的属性。接下来的示例展示了我们如何在对象中定义一个方法：

```javascript
<script>
function stud(admission, name, age) {
    this.admission = admission;
    this.name = name;
    this.age = age;
    this.updateAge = updateAge;
    function updateAge(newAge) {
        this.age = newAge;
    }
}

var s = new stud(4380, "John Joel", 28);
document.write(s.admission + " " + s.name + " " + s.age);
s.updateAge(29);
document.write(s.admission + " " + s.name + " " + s.age);
</script>
```

代码后将返回如下结果：

4380 John Joel 29

我们定义了 `updateAge` 方法，它可以帮助我们更改学生的年龄。在示例中，学生的年龄已从 28 更新为 29。

### 原型 (Prototype)

JavaScript 语言基于原型工作，允许对象从相互获取特征和属性。在这里，每个对象都有一个原型对象。在 JavaScript 中创建一个函数后，`prototype` 属性会自动添加到该函数中。该属性是一个持有构造函数（constructor）属性的原型对象。

这里是 JavaScript 中创建原型对象的语法：在创建对象后，对应的函数会被加载到内存中。这意味着每个对象都有一个函数的新副本。因此，所有函数都会一次性加载到内存中。

#### 原型链 (Prototype Chaining)

每个 JavaScript 对象都有一个原型对象，并从那里获取方法和属性。一个对象的原型可能有另一个原型对象，而该原型也可以获取方法和属性，以此此类推。我们可以将其视为原型链。接下来的示例演示了我们如何向构造函数添加一个新方法：

```javascript
<script>
function Student(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
}

Student.prototype.fullName = function() {
    return this.firstName + " " + this.lastName;
}

var student1 = new Student("John", "Joel");
var student2 = new Student("Mary", "George");
document.writeln(student1.fullName());
document.writeln(student2.fullName());
</script>
```

代码返回如下结果：

`fullName` 函数结合了 `firstName` 和 `lastName` 以返回学生的全名。

让我们创建另一个示例，演示如何向构造函数添加一个新属性：

```javascript
<script>
function Student(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
}

Student.prototype.school = "ABC";

var student1 = new Student("John", "Joel");
var student2 = new Student("Mary", "George");
document.writeln(student1.firstName + " " + student1.lastName + " " + student1.school);
document.writeln(student2.firstName + " " + student2.lastName + " " + student2.school);
</script>
```

代码应返回如下结果：

John Joel ABC

Mary George ABC

我们为原型了 school。

### 构造方法 (Constructor Method)

构造方法是 JavaScript 中的一种特殊方法，用于初始化对象。它使用 `constructor` 关键字声明。类只能有一个构造方法。接的示例展示了如何声明构造方法：

```javascript
<script>
class Student {
    constructor() {
        this.admission = 4380;
        this.name = "John";
    }
}

var stud = new Student();
document.writeln(stud.admission + " " + stud.name);
</script>
```

代码后返回如下结果：

4380 John

注意构造方法用大括号 `{}` 表示。在构造方法体内部创建了各种属性。

### 静态 (Static)

JavaScript 为我们提供了静态方法，它们只属于类而不属于类的实例。这意味着我们不需要实例化即可调用静态方法。直接在类上调用这些方法。

静态方法使用 `static` 关键字声明。方法可以取任何名称。JavaScript 类允许拥有多个静态方法。如果使用同一个名称声明了多个静态方法，则最后一个会被调用。静态方法可以通过 `this` 关键字在另一个静态方法中调用。静态方法可以用于工具函数。这里有一个静态方法的示例：

```javascript
<script>
class StaticTest {
    static show() {
        return "method has been invoked";
    }
}

document.writeln(StaticTest.show());
</script>
```

代码将打印：

method has been invoked

`show()` 方法使用 `static` 关键字声明，使其成为静态方法。让我们看看如何调用多个静态方法：

```javascript
<script>
class StaticTest {
    static show1() {
        return "method has been invoked";
    }
    static show2() {
        return "method invoked again";
    }
}

document.writeln(StaticTest.show1());
document.writeln(StaticTest.show2());
</script>
```

该代码执行后将返回：

method has been invoked

method invoked again

我们创建了两个静态方法，`show1()` 和 `show2()`。我们调用了它们以获得上所示的结果。

我们可以创建多个同名的静态方法并调用它们。下文所示：

```javascript
class StaticTest {
  static show() {
    return;
  }
}
</script>
document.writeln(StaticTest.show());
```

静态方法也可以在构造函数内部调用。下文所示：

```html
<script>
class StaticTest {
  constructor() {
    document.writeln(StaticTest.show());
    document.writeln(this.constructor.show());
  }
  static show() {
    return;
  }
}
var st=new StaticTest();
</script>
```

代码返回以下结果：

静态方法已调用

静态方法已调用

静态方法方法也可以从非静态方法内部调用。例如：

```html
<script>
class StaticTest {
  static show() {
    return;
  }
  show() {
    document.writeln(StaticTest.show()+"<br>");
  }
}
var st=new StaticTest();
st.show();
</script>
```

代码返回以下结果：

静态方法已调用

### 封装

封装是指将数据与作用于该数据的函数绑定的过程。它是控制数据和验证数据的一种良好方法。

要在 JavaScript 中实现这一点，你应该使用 `var` 关键字将数据成员设为私有。可以使用 setter 方法（set）来设置数据，可以使用 getter 方法（get）来获取数据。

考虑以下示例：

```javascript
class Student {
  constructor() {
    var name;
    var score;
  }
  getStudentName() {
    return this.name;
  }
  setStudentName(name) {
    this.name=name;
  }
  getScore() {
    return this.score;
  }
  setScore(score) {
    this.score=score;
  }
}
var st=new Student();
st.setStudentName('John');
st.setScore(78);
document.writeln(st.getStudentName()+st.getScore());
</script>
```

代码执行后将返回以下结果：

John 78

让我们看看如何验证学生的分：

```html
<script>
class Student {
  constructor() {
    var name;
    var score;
  }
  getStudentName() {
    return this.name;
  }
  setStudentName(name) {
    this.name=name;
  }
  getScore() {
    return this.score;
  }
  setScore(score) {
    if (score<0||score>100) {
      alert("Invalid score");
    } else {
      this.score=score;
    }
  }
}
var st=new Student();
st.setStudentName('John');
st.setScore(78);
document.writeln(st.getStudentName()+st.getScore());
</script>
```

分数在 `setScore()` 方法中进行了验证。如果分数不在 0 到 100 之间，它将是无效分数。我们将分数设置为 105。代码的执行返回以下结果：

无效分数

让我们修改分数并将其设置为 78：

```html
<script>
class Student {
  constructor() {
    var name;
    var score;
  }
  getStudentName() {
    return this.name;
  }
  setStudentName(name) {
    this.name=name;
  }
  getScore() {
    return this.score;
  }
  setScore(score) {
    if (score<0||score>100) {
      alert("Invalid score");
    } else {
      this.score=score;
    }
  }
}
var st=new Student();
st.setStudentName("John");
st.setScore(78);
document.writeln(st.getStudentName()+st.getScore());
</script>
```

代码执行后返回以下结果：

John 78

我们也可以使用基于原型的方法来实现封装，如下所示：

```javascript
function Student(name,score) {
  var name=name;
  var score=score;
  Object.defineProperty(this, "name", {
    get: function() {
      return name;
    },
    set: function(sname) {
      name=sname;
    }
  });
  Object.defineProperty(this, "score", {
    get: function() {
      return score;
    },
    set: function(sscore) {
      score=sscore;
    }
  });
}
var st=new Student("John",78);
document.writeln(st.name+st.score);
```

### 继承

通过这一 JavaScript 特性，我们可以基于已有的类创建新类。它为子类提供了一种使用属于父类的方法和属性的方法。

在 JavaScript 中，继承是通过使用 `extends` 关键字实现的。通过这个关键字，我们创建一个基于父类的子类。之后，子类将能够获取父类的行为和属性。

继承维护了“是一个”（IS-A）的关系。继承也可以通过基于原型的方法实现。考虑以下示例，其中 `Current` 继承自 `Date`：

```html
<script>
class Current extends Date {
  constructor() {
    super();
  }
}
var c=new Current();
document.writeln(c.getDate()+"-"+c.getMonth()+1)+-"+c.getFullYear());
</script>
```

代码将返回所示输出：

今天是：20-2-2019

代码返回今天的日期。另一个示例：

```html
<script>
class Current extends Date {
  constructor(year) {
    super(year);
  }
}
var c=new Current(2019);
document.writeln("");
document.writeln(c.getFullYear());
</script>
```

执行后代码返回以下内容：

年份是：1958

这表明该方法能够成功提取出提供日期的年份部分。

这里另一个示例，其中我们正在创建一个子类来继承父类：

```html
<script>
class Car {
  constructor() {
    this.manufacturer = "Toyota";
  }
}

class Model extends Car {
  constructor(name, year) {
    super();
    this.name = name;
    this.year = year;
  }
}

var m = new Model("Harner", 2012);
document.writeln(m.manufacturer + " " + m.name + " " + m.year);
</script>
```

代码返回以下结果：

Toyota Harner 2012

让我们演示如何实现基于原型的继承，在这种情况下，我们不需要使用 `extends` 和 `class` 关键字：

```html
<script>
function Car(manufacturer) {
  this.manufacturer = manufacturer;
}
Car.prototype.getManufacturer = function() {
  return this.manufacturer;
}

function Model(name, year) {
  this.name = name;
  this.year = year;
}

var car = new Car("Toyota");
Model.prototype = car;

var model = new Model("Harner", 2012);
document.writeln(model.getManufacturer() + " " + model.name + " " + model.year);
</script>
```

### 多态

这是面向对象编程范式的一个关键特性，它允许以不同的方式执行同一个操作。通过多态，我们可以在各种 JavaScript 对象上调用同一个方法。JavaScript 不是一种类型安全的语言；因此，任何数据类型的成员都可以传递给方法。考虑下面的示例：

```html
<script>
class Parent {
  show() {
    document.writeln("Parent class invoked");
  }
}

class Child extends Parent {
  show() {
    document.writeln("Child class invoked");
  }
}

var ch = new Child();
ch.show();
</script>
```

代码将返回以下内容：

Parent class invoked

Child class invoked

这里另一个示例：

```html
<script>
class Parent {
  show() {
    document.writeln("Parent class invoked");
  }
}

class Child extends Parent {
  show() {
    document.writeln("Child class invoked");
  }
}

var p = [new Parent(), new Child()];
p.forEach(function(message) {
  message.show();
});
</script>
```

`show()` 方法的行为根据调用它的对象而有所不同。代码打印出以下输出：

Parent class invoked

Child class invoked

我们可以实现相同的示例，但这次通过基于原型的方法。演示所示：

```html
<script>
function Parent() {
}
Parent.prototype.show = function() {
  return "Parent class invoked";
};

function Child() {
}
Child.prototype = Object.create(Parent.prototype);
Child.prototype.show = function() {
  return "Child class invoked";
};

var p = [new Parent(), new Child()];
p.forEach(function(message) {
  document.writeln(message.show());
});
</script>
```

## 第 15 章 - 多媒体

JavaScript 拥有作为 `navigator` 的子对象的 `plugins` 对象。它是一个数组，包含了浏览器插件的某些单个条目。Firefox 和 Netscape 等浏览器支持使用 `navigator.plugins` 对象。考虑下面的脚本：

<table border="1">
  <tr>
    <th>插件名称</th>
    <th>文件名</th>
    <th>描述</th>
  </tr>
</table>

<script>
for (var x=0; x<navigator.plugins.length; x++) {
  document.write(navigator.plugins[x].name);
  document.write(navigator.plugins[x].filename);
  document.write(navigator.plugins[x].description);
}
</script>

一旦执行，该脚本将向你显示浏览器上安装的所有插件列表。每个插件都表示为数组中的一个条目。每个条目具有以下属性：
- name：指定插件的名称。
- filename：这是一个可执行文件，用于在安装插件时加载它。
- description：这描述了插件的描述。

在我的情况下，我在 Chrome 上运行了代码，它返回了以下内容：

| Name | Filename | Description |
| :--- | :--- | :--- |
| PDF Viewer | | |
| Shockwave Flash | | |

通过上述属性，人们可以确定已安装的插件，然后使用 JavaScript 来播放必要的多媒体文件。

示例：

```html
<script>
var vid = navigator.mimeTypes["video"];
if (vid) {
  document.write("<embed src='" + vid + "' width='300' height='200'>");
} else {
```



## 第 16 章 错误处理

JavaScript 是我们拥有的弱类型语言之一。它没有编译阶段。错误通常在编程过程中发生。你可以尝试访问未定义的变量或函数。错误被分为语法错误、运行时错误和逻辑错误。让我们来讨论它们。

### 语法错误

在 JavaScript 中，语法错误发生在解释期间。它们也被称为解析错误。考虑下面提供的示例脚本：

```html
<script type="javascript">
  window.print()
</script>
```

JavaScript 语句应该以分号结束。`window.print()` 语句没有以分号结束，因此这将导致语法错误。如果一个语句存在语法错误，与其处于同一线程中的所有语句都会受到影响。其他线程将正常执行。

### 运行时错误

这些是在运行期间抛出的异常。执行发生在解释之后。

示例：

```html
<script type="javascript">
  window.printFile();
</script>
```

在解释期间，不会产生错误，因为脚本具有正确的语法。但在运行时会抛出异常，因为脚本将调用一个未知的方法，即 `printFile()` 方法。

### 逻辑错误

这类错误发生在你未能于脚本中实现正确的逻辑时，这意味着你无法获得预期的结果。它们对人们来说很难追踪。它们不是由运行时错误或语法错误引起的。人们无法捕获这类错误，因为它们取决于要实现的业务逻辑。

### try...catch...finally

在 JavaScript 中，你可以处理错误和异常。当此语句与 `throw` 结合时，可以更有效地处理错误和异常。该语句的语法如下：

```html
<script type="javascript">
try {
  // break
} catch (ex) {
  // break;
} finally {
  // break
}
</script>
```

`try` 块后面应该紧跟 `catch` 或 `finally` 块。当 `try` 块中发生异常时，异常将被添加到 `ex` 中，然后执行 `catch` 块。`finally` 块是可选的，它在 `try/catch` 之后会无条件地执行。

示例：

```html
<script type="javascript">
function checkFunction() {
  var check, val;
  check = document.getElementById("check");
  check.innerHTML = "";
  val = document.getElementById("check").value;
  try {
    if (isNaN(val)) throw "Enter a number";
    val = Number(val);
    if (val < 10 || val > 20) throw "between 10 and 20";
  } catch (ex) {
    check.innerHTML = ex;
  }
}
</script>
```

在我们的案例中，我们使用 `try` 和 `catch` 来验证我们的输入字段。输入应该是 10 到 20 之间的数字。如果不符合这一规定，将抛出异常并由 `try` 和 `catch` 处理。

### finally 语句

该语句指定了在 `try` 和 `catch` 之后执行的代码，无论结果如何都必须执行。以下是它的语法：

```javascript
try {
  // code for try
} catch (err) {
  // code for handling errors
} finally {
  // code for finally
}
```

示例：

```html
<script type="javascript">
function checkFunction() {
  var check, val;
  check = document.getElementById("check");
  check.innerHTML = "";
  val = document.getElementById("check").value;
  try {
    if (val == "") throw "The field is empty";
    if (isNaN(val)) throw "Enter a number";
    val = Number(val);
    if (val < 10 || val > 20) throw "between 10 and 20";
  } catch (ex) {
    check.innerHTML = ex;
  } finally {
    document.getElementById("check").value = "";
  }
}
</script>
```

## 第 17 章 正则表达式

JavaScript 有一个名为 `RegExp` 的类，有助于程序员处理正则表达式。通过这个类，人们可以对某些文本执行模式匹配、替换和搜索函数。要定义正则表达式，我们使用 `RegExp` 构造函数。如下所示：

```javascript
expression = new RegExp("pattern");
```

参数 `the_pattern` 是一个字符串，指定正则表达式的模式或其他任何正则表达式。`flags` 参数是一个可选字符串，具有 "i"、"m" 和 "g" 属性，分别指定不区分大小写、多行和全局匹配。

让我们讨论 JavaScript 中正则表达式的各种方法。

### exec()

该方法将在字符串中搜索匹配 `regexp` 的文本。如果找到匹配，结果将以数组返回，否则将返回 `null`。

该方法具有以下语法：

```javascript
regexp.exec(search_string);
```

参数 `search_string` 表示要搜索的字符串。考虑以下示例：

```html
<script type="javascript">
  var text = ".47";
  var reg = new RegExp("\\.");
  var output = reg.exec(text);
  document.write("+" + output);
  reg = new RegExp(":");
  output = reg.exec(text);
  document.write("." + output);
</script>
```

代码执行后返回以下输出：

第一次测试，返回的值为 15: express
第二次测试。返回的值为 `null`
我们首先搜索了字符串 express，它在 expressions 中被找到了。其次，我们搜索了字符串 language，它在我们的句子中没有被找到。

### test()

该方法在字符串中搜索匹配 `regexp` 的文本。如果找到匹配，它将返回 `true`，否则将返回 `false`。该方法具有以下语法：

```javascript
regexp.test(search_string);
```

参数 `search_string` 是要搜索的字符串。

```javascript
var reg = new RegExp("nameertipaths");
var output = reg.test(text);
document.write("Output" + output);
</script>
```

代码返回以下结果：
第一次测试返回：
`true`
第二次测试返回： `false`

在第一次测试中，找到了匹配项，因此输出为 `true`。在第二次测试中，没有找到匹配项，因此返回了 `false`。

### search()

该方法用于搜索字符串，与 `indexOf` 函数类似，不同之处它接受的是正则表达式而不是字符串。它返回一个整数，表示字符串的位置。注意，0 表示字符串的开头，7 将匹配第 8 个字符，以此此类。如果没有找到匹配项，则返回 -1：

```html
<script type="javascript">
var myString = "|example";
var m = myString.search(/Best[0-9]+/);
document.writeln(m)
</script>
```

脚本在执行后返回 6。在使用时，该方法将以正则表达式字面量的形式返回相关正则表达式的字符串表示。该方法采用下所示语法：

`RegExpObject.toString();`

该方法随后返回你的正则表达式的字符串表示。

例如：

```html
<script type="javascript">
var text = "DeepLearning";
var reg = new RegExp("ee");
var output = reg.toString();
document.write("Output" + output);
</script>
```

代码在执行后将返回以下结果：
第一次测试返回： `/ee/`
第二次测试返回： `'g'`

## 第 18 章 图像映射

JavaScript 可用于创建客户端图像映射。要启用图像映射，我们使用 `<img />` 标签的 `usemap` 属性。我们使用 `<area>` 和 `<map>` 标签来定义它们。形成映射的图像通过 `<img />` 标签和一种名为 `usemap` 的特殊属性插入。该属性的值应与 `<map>` 元素中 `name` 属性值匹配，并且应以井号（#）开头。

`<map>` 标签为你的图像创建一个映射，它应该位于 `<img />` 元素之后。它将成为定义点击热点的 `<area />` 元素的容器。`<map>` 元素只有一个属性 `name`，用于标识映射的名称。这有助于 `<img />` 元素识别应该使用哪一个 `<map>` 元素。点击热点的坐标和形状通过 `<area>` 元素定义。

考虑以下示例：

```html
<html>
<head>
<script type="javascript">
function showLanguage(name) {
    document.form.lang.value = name;
}
</script>
</head>
<body>
<form name="f1">
<input type="text" name="lang" size="20">
</form>
<img src="map.gif" alt="Map" usemap="#map1">
<map name="map1">
<area shape="rect" coords="0,0,50,50" href="english.html" onclick="showLanguage('English')">
<area shape="circle" coords="60,60,20" href="spanish.html" onclick="showLanguage('Spanish')">
</map>
</body>
</html>
```

代码执行后给了我一个界面。我得到的结果取决于下所示我指向的部分：

## 第 19 章 页面重定向

有时你会遇到这样的情况：你点击某个 URL 访问特定页面 X，但内部被重定向到了另一个页面 Y。这就是页面重定向的工作原理。你有许多理由可能需要将用户重定向到另一个页面。一个很好的例子是你移动到一个新域名时。你可以使用页面重定向将访问者引导到新网站。在这种情况下，你只需要维护旧域名，然后添加一个带有页面重定向功能的页面，这样任何访问你旧域名的人都会被带到你的新网站。

有时，你可以为不同版本的浏览器或当页面针对不同国家时创建不同的网页。与其依赖服务器端重定向，你可以选择使用客户端重定向以确保每次访问都落落在正确的页面。当你的网页已被搜索引擎索引时，页面重定向也同样重要。当你移动到新域名时，你不必丢失你的搜索引擎访问者。在这种情况下，客户端页面重定向将对你有所帮助。但是，不要将其作为欺骗器的手段，因为这样做可能会导致你的网页在浏览器中被封禁。

客户端页面重定向可以在 JavaScript 中轻松实现。要做到这一点，你只需要在代码的头部添加一行即可。这将完成重定向。让我们演示一下：

```html
<html>
<head>
<script type="javascript">
function RedirectFunction() {
    window.location="http://www.google.com";
}
</script>
</head>
<body>
<p>点击下方按钮进行重定向</p>
<form>
<input type="button" value="Click Here" onclick="RedirectFunction()">
</form>
</body>
</html>
```

代码执行后将返回以下内容：

点击下方的按钮进行重定向

重定向

点击重定向按钮查看会发生什么。你将被重定向到你指定的 URL。在上面的情况下，我将 JavaScript 网站指定为 URL。你可以更改并查看它将你重定向到另一个网站。

在重定向到新页面之前，你可以向访问者显示消息。不过，加载新页面需要一点延迟。让我们演示如何实现这一功能：

```html
<html>
<head>
<script type="">
function RedirectFunction()
{
window.location = "";
}
document.write('');
setTimeout('RedirectFunction',10);
</script>
</head>
<body>
</body>
</html>
```

运行代码后，你将看到以下消息：

你将在 10 秒后看到主页面

10 秒过期后，你将被重定向到 JavaScript 网站。

正如我们之前提到的，页面重定向可以根据用户的浏览器进行。以下示例演示了如何实现操作：

```html
<html>
<head>
<script type="">
var browsertype = navigator.appName;
if(browsertype == "Netscape") {
window.location = "http://javascript.com";
} else if (browsertype == "IE") {
window.location = "http://ie.com";
} else {
window.location = "http://browser.com";
}
</script>
</head>
<body>
</body>
</html>
```

用户将根据他们使用的浏览器类型被重定向。注意，我们使用了 `if` 决策语句将用户重定向到不同的页面。

## 结论

本指南到此结束。JavaScript 是一种非常强大的脚本语言。JavaScript 是一种解释型脚本语言。该语言通常在客户端执行。这使其成为 Web 开发过程中验证的最佳语言。Web 开发者使用 JavaScript 来验证 Web 表单中的电子邮件地址、电话号码和其他信息的有效性。

JavaScript 改变了工作方式。最初，在填写表单后，必须将其提交到服务器以检查是否有任何异常。如果发现异常，服务器会将表单返回给用户以修正细节。然后用户将重新提交表单中填写的内容。使用 JavaScript，验证在表单提交到服务器之前就可以完成。用户能够了解填写表单时发生的任何错误并进行相应的纠正。这让用户的操作变得更加简单。JavaScript 还允许你创建可以由某些动作触发的各种效果。这些动作的示例可以：
- 鼠标悬停
- 键按压
- 网页加载
- 等

更多信息可以在 `www.testing.com` 获取 美国制造
