# JavaScript 初学者指南：JavaScript、Python、SQL 与 Java 基础完全指南

## 引言

HTML 并不是很智能。它主要让人们查看文本和图像，并允许他们移动到其他页面，在那里他们将进行更多相同的操作。为网页添加智能的是 JavaScript。它通过让页面在访客与内容互动时做出响应，使网站更具吸引力、更有效、更有用。

本书假设我们已经知道如何使用 HTML 来指定网页的结构和内容。如果我们熟悉如何用 CSS 来设置页面样式（独立于网页结构），那将是额外有益的。如果情况如此，那么我们就准备好使用 JavaScript 为页面添加一些行为，使其更具动态性和交互性。否则，没有 HTML 和 CSS，JavaScript 对我们不会有多大好处。它们被视为网页的三大基本支柱：结构、表现和行为。

## 第1章：什么是JavaScript？

JavaScript 是 Web 的脚本语言，其唯一目的是为我们的页面添加交互性。除了交互性，现代版本的 JavaScript 还可用于从外部来源甚至网站用户那里加载和解析信息。
JavaScript 本质上是一段嵌入在网页 HTML 结构中的编程代码。当网页浏览器读取此代码时，它会激活一个内置的解释器，该解释器知道如何解读这种语言并处理其命令。

虽然编码过程中涉及编程，但 JavaScript 不是一种编程语言。在传统的 Web 编程语言（如 Java 或 .NET）中，代码在执行之前必须经过编译。编译意味着代码必须首先发送到在服务器上运行的特殊程序。这个程序也称为应用服务器软件，负责翻译代码，创建请求的页面和/或功能，并将这些内容作为 HTML 返回。像 JavaScript 这样的脚本语言不是编译的，而是实时解释的。这意味着不需要特殊的软件，因为用户自己的浏览器在遇到代码时就会运行和执行它。

注意：JavaScript 诞生于 Java 非常流行的时代。除此之外，这两种语言没有关联，并且***除了基本的编程逻辑外几乎没有共同点***。

### 实施JavaScript

既然我们已经对 JavaScript 是什么有了大致的了解，我们就可以开始使用这种语言了。由于 JavaScript 代码是 HTML 文档的一部分，我们需要知道如何告诉浏览器运行我们的脚本。当我们要在 Web 文档中包含 JavaScript 时，有两种常见的选项可供我们选择，在这两种情况下，我们都将使用 `<script>` 元素。`<script>` 标签用于告诉浏览器在 HTML 文档中 JavaScript 代码从哪里开始以及在哪里结束。因此，此标签可以包含在页面的 `head` 或 `body` 部分中。

第一个选项是将代码内联放置在文档结构中。为此，我们将首先打开一个 `<script>` 标签，输入 JavaScript 代码，然后以 `</script>` 标签结束。理论上，我们可以将文档保持原样，因为几乎所有浏览器都会默认假设 `<script>` 标签之间的脚本语言是 JavaScript。但是，为了最大限度地兼容性，我们将使用 `type` 属性和 `text/javascript` 值来扩展此标签，以指导浏览器如何确切地解释代码。

```
<script type="text/javascript">
//A JavaScript comment
</script>
```

第二个选项是从外部文件将 JavaScript 代码加载到我们的 HTML 文档中。为此，我们可以再次使用 `<script>` 元素，但这次除了 `type` 属性外，我们还将在 `<script>` 元素的 `src` 属性中包含外部文件的 URL。外部文件必须是仅包含纯 JavaScript 代码的文本文件，其扩展名为 `.js`，不包含任何 HTML 元素或 CSS 规则。例如，要将外部 `scripts.js` 文件调用到我们的浏览器中，我们将使用以下代码：

```
<script src="script.js" type="text/javascript"></script>
```

当我们希望在整个网站中共享功能时，我们将 JavaScript 放在一个外部文件中并将其包含在网页中。否则，如果我们只需要添加一些本地交互行为，我们就将代码嵌入到页面中。

注意：脚本文件按照它们在 HTML 代码中放置的顺序加载。



## 第二章：JavaScript基础概念

通常，当我们听到“编程”这个词时，马上会想到别人在敲打一串难以理解的字母和数字。编程看起来像是超越凡人领域的魔法。然而，编程中的概念并不难掌握，因为它们总能在现实生活中找到应用。JavaScript虽然不像HTML或CSS那样简单，但也并非一门过于复杂的语言。与其他语言不同，它的“语法”或多或少具有描述性和直观性，使其适合作为入门编程语言。基本上，学习JavaScript就像学习一门新语言，但这门新语言与英语有些相似。一旦我们掌握了新单词，并理解如何将它们组合成“句子”，我们就能顺利进行下去。

### 语法

每种语言都有自己的字符和单词，以及一套将这些字符和单词组合成正确句子的规则。这些规则也被称为语言语法，正是语法将语言凝聚在一起并赋予其意义。

在开始介绍一些JavaScript语法示例之前，让我们先设置JavaScript的环境。如前所述，JavaScript代码始终是HTML代码的一部分。因此，为了使用JavaScript，我们首先需要创建一个基本的HTML文档。那么，让我们打开一个文本编辑器（如记事本），输入最基础的网页HTML代码。除了基本的HTML标签外，我们将在`<head>`部分包含一个`<script>`元素，我们将开始在其中放置JavaScript代码。

```
<!doctype html>

<head>

<title>JavaScript入门</title>
<script type="text/javascript">
</script>
</head>
<body>
</body>
</html>
```

让我们将这个文档保存为firststeps.html。如果使用记事本，必须记得将“保存类型”字段更改为“所有文件”。

### 语句

在日常通用语言中，我们使用句子作为基本的交流形式。类似地，在JavaScript中，我们也要组成句子来表达我们的意图，这些句子更正式的名称是语句。JavaScript句子是基本的通信单元，通常代表程序中的一个步骤。就像我们把句子组合起来表达一个观点一样，我们将语句组合起来创建一个程序。

让我们看一个简单的JavaScript语句，看看它能做什么。在HTML文档的`<script>`开始和结束标签之间放置以下文本：

```
alert("JavaScript开始有点道理了。");
```

在后续示例中，除非必要，我们将不再显示完整的HTML代码，但作为初始参考，您的文档应如下所示：

```
<!doctype html>
<head>
<title>JavaScript入门</title>
<script type="text/javascript">
alert("JavaScript开始有点道理了。");
</script>
</head>
<body>
</body>
</html>
```

我们可以保存firststeps.html文档，并在网页浏览器中打开它。页面打开后，我们将看到一个警告窗口，显示消息“JavaScript开始有点道理了”。

现在我们知道效果了，让我们回到JavaScript语句，将其解释成通用语言，以便更容易理解。

alert("JavaScript开始有点道理了。");

JavaScript语句是由网页浏览器执行的指令。该语句以一个由关键字表示的命令开始。该关键字标识了需要执行的操作。在这种情况下，关键字alert使网页浏览器打开一个对话框并显示一条消息。如果我们只有语句alert(); 对话框将是空的，但在我们的例子中，该语句包含一个特定的输入，即实际的消息文本，也称为参数。最后，就像每个句子都以句号结尾一样，JavaScript句子以分号结尾。分号明确表示语句结束，一旦解释器执行完它，就应该移动到下一个项目。

现在我们准备好翻译这个JavaScript语句了。它的通俗英语解释是：“打开一个对话框，并在该框中显示文本‘JavaScript开始有点道理了’。”

注意：传递文本参数时，我们可以使用双引号（"sense"）或单引号（'sense'）来呈现文本。

在继续之前，让我们看另一个JavaScript语句。在`<script>`元素中，用以下代码替换之前的代码，并在网页浏览器中预览以查看结果：

```
document.write("<p>JavaScript开始有点道理了。</p>");
```

从结果中我们可以看到，之前为空的文档现在有了一段文本。根据之前对JavaScript工作原理的解释以及网页浏览器的结果，我们可以正确地推断出document.write关键字命令浏览器直接写入网页。类似于alert()，它将写入括号之间的任何内容。

### 变量

JavaScript，以及任何编程语言的一个基本方面是变量的概念。变量是一种声明和存储信息的方法，这些信息可以稍后使用。这些信息可以随情况变化，因此得名变量。

让我们看下面的语句。

```
var name = "Martin";
```

用通俗的语言来说，这等同于说“我的名字是Martin”。关键字var是JavaScript中“创建一个变量”的说法，或者用编程术语来说，是“声明一个变量”。后面是变量的名称，这个名称可以是任何我们选择的东西，但有一定的限制。用=号为变量赋值，这不是立即需要的，因为可以稍后进行。我们可以在一个语句中声明一个未定义的变量，然后在后面的语句中为其赋值。例如：

```
var name;
name = "Martin";
```

如前所述，变量名可以是任何东西，比如name、abc、R2D2，但有一些规则。变量名可以包含字母、数字、美元符号（$）或下划线（_），不允许使用其他特殊字符。此外，变量名不能以数字开头，任何其他允许的值都是可以接受的。最后，变量名区分大小写，这意味着网页浏览器中的解释器会区分大写和小写字母，使得'score'与'Score'不同。

注意：虽然我们几乎可以使用任何内容作为变量名，但明智的做法是使用有意义的名称，因为这将帮助我们和其他程序员更好地理解编写的代码。

### 变量类型

根据数据类型，变量有不同的种类。三种最基本的类型是数字、字符串和布尔值。

数字变量由数字字符表示。这个变量可以接受整数、负整数和分数整数。数字经常用于计算，因此我们的数字变量经常包含在数学运算中。以下语句声明了一个名为age的变量，并为其赋值35。

```
var age = 35;
```

字符串变量用于表示任何字母序列，如单词或句子。字符串表示为一系列用引号括起来的字符，引号向解释器指示后面是一个字符串变量。JavaScript允许我们使用双引号（"）或单引号（'），但我们必须注意使用相同类型的引号。

```
var location = "California";
```

布尔变量相当简单，因为它只能接受两个值之一：true或false。当我们创建JavaScript程序，希望程序能智能地响应用户操作时，会使用这种变量。

### 用户变量

如果JavaScript不允许我们分享想法并直接创建或修改变量，那就没那么有趣了。提供输入的最简单方法之一是使用prompt()命令。

```
var name = prompt("你叫什么名字？", "")
document.write(name);
```

prompt()命令的结果是一个对话框。与alert对话框只显示消息不同，prompt对话框还可以接收答案。因此，在prompt对话框的语法中，有必要在括号内用逗号分隔提供两个参数。第一个参数是显示在框中的提示文本，第二个参数是文本框的默认值，因此也是变量的默认值。

在上面的例子中，框中显示的提示文本将是“你叫什么名字？”，框中显示的默认值将是空的，因为引号之间显然没有内容。一旦我们在框中输入一些内容并单击“确定”或按“Enter”键，变量就会接收到在字段中输入的值。因此，名字将显示在网页上。否则，如果我们单击“取消”、按“Esc”键或关闭提示框，返回的值将是空的，屏幕上将没有文本。

注意：除了prompt()，我们也可以使用更正式的window.prompt命令。

### 运算符



#### 数学运算符

JavaScript 中内置了基本的数学运算符，例如加法（+）、减法（-）、乘法（*）和除法（/）。它们可以用于独立的语句中，也可以在声明变量时使用。例如，通过对变量 `currentYear` 和 `yearOfBirth` 进行“运算”，我们可以确定变量 `age` 的值。

```javascript
var currentYear = 2015;
var yearOfBirth = 1979;
var age = currentYear - yearOfBirth;
document.write(age);
```

注意：“调用”变量以在网页上显示内容非常简单。只需使用 `document.write()` 命令即可。

数学运算符，特别是加法运算符，可用于组合两个或多个字符串。这种组合字符串的过程称为连接。在以下示例中：

```javascript
var firstName = "Martwan";
var lastName = "Jenkins";
var fullName = firstName + lastName;
document.write(fullName);
```

`fullName` 的值最终将是 `MartwanJenkins`。为了确保格式正确，我们需要将空格作为字符串包含在引号中。例如，我们可以使用以下声明：

```javascript
var fullName = firstName + " " + lastName;
```

我们可以看到，运算符在连接文本和/或组合变量时也很有用。实际上，我们可以用它来构造更合乎逻辑的句子。例如，我们可以将“My name is”文本与计算变量的值组合起来。

```javascript
var firstName = "Martwan";
var lastName = "Jenkins";
var fullName = firstName + " " + lastName;
document.write("My name is " + fullName);
```

> 注意：在单个语句中执行多个数学运算时，适用运算符优先级规则。

### 赋值运算符

就像现实生活中事物会变化一样，JavaScript 程序中的变量也是如此。而在 JavaScript 中改变变量，我们将使用赋值运算符。我们已经熟悉了基本的赋值运算符——等号（=），它用于给变量赋予初始值或新值。还有其他赋值运算符也能改变变量的值，但方式略有不同。

例如，随着时间的推移，我们年龄增长，年龄值每年递增 1。为了在 JavaScript 中实现这种变化，我们可以采用几种不同的方法，效果都一样。为了尝试改变变量的各种可能性，我们可以尝试以下代码，其中 `age` 变量值改变后会显示在浏览器中：

```javascript
var age = 35;
document.write("<p>My age is " + age + "</p>");
age = age + 1;
document.write("<p>A year has passed, so now I am " + age + "</p>");
age += 10;
document.write("<p>What? Are you telling me that I am a grandad now? But I am only " + age + "</p>");
```

虽然这些操作起初可能看起来有点令人困惑，但从编程角度来看它们仍然是合乎逻辑的。例如，如果我们反向阅读语句 `age = age + 1`，其过程是：将 1 的值加到当前年龄 35 上，使 `age` 的新值变为 36。此外，我们可以在语句 `age += 10` 中使用复杂的赋值运算符（+=）来将变量的值增加 10。我们还可以将相同的逻辑应用于其他运算，如减法、除法和乘法。

```javascript
age -= 5; // 等同于 age = age - 5;
age *= 5; // 等同于 age = age * 5;
age /= 5; // 等同于 age = age / 5;
```

此外，当我们想将变量的值增加/减少 1 时，也可以使用以下赋值运算符：

```javascript
age++; // 等同于 age = age + 1;
age--; // 等同于 age = age - 1;
```

#### 比较运算符

顾名思义，比较运算符用于比较两个值。比较完成后，会根据比较结果是否精确返回 true 或 false 值。

## 第三章：JavaScript 的历史

JavaScript 是网景公司于 1995 年创建的一种语言，用于开发在浏览器中运行的产品和应用程序。JavaScript 与 Java 语言本身毫无关系。这只是为了借用当时更流行的 Java 语言的名字而采取的策略。微软也试图创建自己的脚本技术，如 VBScript 和 JScript。

1996 年 11 月，JavaScript 被确立为标准规范。ECMAScript 是官方标准的名称，JavaScript 是其中最著名的实现。此后，该语言经过多次修改和更新，以确保它仍然是最流行的客户端脚本语言之一。自 JavaScript 于 1997 年被采纳为 ECMA 标准以来，它就遵循 ECMA 标准的发布周期。

以下是 ECMAScript 语言的版本信息。

| 年份 | 名称 | 变化 |
| :--- | :--- | :--- |
| 1997 | ECMAScript 1 | 第一版 |
| 1998 | ECMAScript 2 | 仅编辑性更改 |
| 1999 | ECMAScript 3 | 添加了正则表达式和 try/catch |
| 2009 | ECMAScript 5 | 添加了“严格模式”和 JSON 支持 |
| 2011 | ECMAScript 5.1 | 编辑性更改 |
| 2015 | ECMAScript 6 | 添加了类和模块 |
| 2016 | ECMAScript 7 | 添加了指数运算符 (**) 和 array.prototype.includes |

基于 JavaScript 语言还开发了许多流行的框架。下面列出了一些最受欢迎的框架，并附有每个框架的代码简要示例。

### 2.1 AngularJS

AngularJS 是一个用于创建动态 Web 应用程序的结构框架。HTML 可以用作模板语言，AngularJS 允许你扩展 HTML 的语法以清晰地表达应用程序的组件。AngularJS 支持数据绑定和依赖注入，这消除了为执行这些任务而自行编写代码的需要。

**示例 5：** 以下程序用于展示一个简单的 AngularJS 程序。

```html
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.4/angular.min.js"></script>
<body>
<div ng-app="">
<p>Hello World</p>
</div>
</body>
</html>
```

### 2.2 Node.JS

Node.JS 是一个开源、跨平台的 JavaScript 运行时环境，用于在服务器端执行 JavaScript 代码。通常 JavaScript 用作客户端语言，但 Node.JS 通过实现可在服务器端框架上使用的 JavaScript 改变了这一点。

**示例 6：** 以下程序用于展示一个简单的 Node JS 程序。

```javascript
var http = require('http');

http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello World!');
}).listen(8080);
```

### 2.3 ReactJS

ReactJS 是一个用于构建用户界面的开源 JavaScript 库。它由 Facebook、Instagram 以及个人开发者和公司组成的社区共同维护。

**示例 7：** 以下程序用于展示一个简单的 React JS 程序。

```javascript
var App = React.createClass({
  render: function() {
    return <div>Hello World</div>
  }
});
React.render(<App />, document.body);
```

### 2.4 JQuery

JQuery 是一个快速、小巧且功能丰富的 JavaScript 库。它通过一个易于使用的 API，使 HTML 文档遍历和操作、事件处理、动画以及 Ajax 等操作变得更加简单，该 API 可在众多浏览器上工作。

**示例 8：** 以下程序用于展示一个简单的 JQuery 程序。

```html
<!DOCTYPE html>
<html>
<script>
$(document).ready(function(){
  $("p").click(function(){
    $(this).hide();
  });
});
</script>
<body>
</body>
</html>
```

### JavaScript 的特性

JavaScript 具有多种特性。我将在下面介绍其中几个：

#### 3.1 对象处理

JavaScript 中的数据以对象的形式表示，这使得在 JavaScript 中处理各种形式的数据更容易且更具扩展性。下面是一个使用定义为变量的对象的简单 JavaScript 程序示例。

**示例 9：** 以下程序用于展示一个简单的 JavaScript 对象。

```html
<!DOCTYPE html>
<html>
<body>
<h1>JavaScript Example</h1>
```



##### 3.2 数据类型

JavaScript 的工作基于其作为动态类型语言的特性。一个变量可以先被设置为数字，之后再被设置为字符串。下面是一个处理数据类型的简单 JavaScript 程序示例。

示例 10：以下程序用于展示一个关于数据类型的简单 JavaScript 程序。

```
<!DOCTYPE html>
<html>
<body>
<h1>javascript Example</h1>
<p id="demo"></p>
<script>
var value = 1;
value = "Hello World";
document.getElementById("demo").innerHTML = value;
</script>
</body>
</html>
```

##### 3.3 结构化语言

JavaScript 遵循结构化编程语法，你可以使用普通的循环语句，如“while 循环”和“if 语句”。下面是一个涉及决策和循环的简单 JavaScript 程序示例。

示例 11：以下程序用于展示一个关于循环语句的简单 JavaScript 程序。

```
<!DOCTYPE html>
<html>
<body>
<h1>javascript Example</h1>
<p id="demo"></p>
<script>
var txt = "";
var i = 0;
do {
    txt += "<br>The value is " + i;
    i++;
}
while (i < 10);
document.getElementById("demo").innerHTML = txt;
</script>
</body>
</html>
```

##### 3.4 面向对象

JavaScript 几乎是一门完全的面向对象语言，能够为变量对象定义属性。下面是一个处理对象的简单 JavaScript 程序示例。

示例 12：以下程序用于展示一个使用对象的简单 JavaScript 程序。

```
<!DOCTYPE html>
<html>
<body>
<h1>javascript Example</h1>
<p id="Name"></p>
<p id="chapter"></p>
<script>
var Tutorial = {Name: "Javascript", chapter: "Features"}
document.getElementById("Name").innerHTML = Tutorial.Name;
document.getElementById("chapter").innerHTML = Tutorial.chapter;
</script>
</body>
</html>
```

##### 3.5 定义函数

JavaScript 有能力借助函数将代码拆分成模块。通过在 JavaScript 程序中定义函数，可以划分程序的逻辑。下面是一个使用函数的简单 JavaScript 程序示例。

示例 13：以下程序用于展示一个关于类的简单 JavaScript 程序。

```
<!DOCTYPE html>
<html>
<body>
<h1>javascript Example</h1>
<p id="Name"></p>
<p id="chapter"></p>
<script>
function myFunction() {
    return "Hello World";
}
document.getElementById("Name").innerHTML = myFunction();
</script>
</body>
</html>
```

##### 3.6 事件处理

JavaScript 也可以处理事件。因此，如果你希望代码在点击按钮时运行，这是可以做到的。可以使用函数来定义在事件触发时运行的代码。下面是一个涉及事件处理的简单 JavaScript 程序示例。

示例 14：以下程序用于展示一个处理事件的简单 JavaScript 程序。

```
<!DOCTYPE html>
<html>
<body>
<h1>javascript Example</h1>
<p id="Name"></p>
<p id="chapter"></p>
<script>
function myFunction() {
    document.getElementById("Name").innerHTML = "Hello World";
}
</script>
<button onclick="myFunction()">Click Me</button>
</body>
</html>
```

##### 3.7 操作 HTML DOM

可能最重要的功能是能够通过 HTML 页面的 DOM 结构来修改其元素。正是这一点使得 JavaScript 成为如此流行的脚本语言。下面是一个操作 HTML DOM 的简单 JavaScript 程序示例。

示例 15：以下程序用于展示一个操作 HTML DOM 的简单 JavaScript 程序。

```
<!DOCTYPE html>
<html>
<body>
<h1>javascript Example</h1>
<p id="Name"></p>
<script>
document.getElementById("Name").innerHTML = "Hello World";
</script>
</body>
</html>
```

##### 3.8 操作浏览器

JavaScript 也设计为与多种不同的浏览器协同工作，并且能够获取其运行所在的浏览器窗口的信息。

示例 16：以下程序展示了一个可用于与浏览器窗口交互的简单 JavaScript 程序。

```
<!DOCTYPE html>
<html>
<body>
<h1>Javascript Example</h1>
<p id="demo"></p>
<script>
document.getElementById("demo").innerHTML = screen.width;
</script>
</body>
</html>
```

##### 3.9 变量作用域

JavaScript 中的变量也遵循全局与局部作用域的概念。变量的作用域在其定义的代码块内。下面的示例展示了一个具有局部作用域的变量。

示例 17：以下程序展示了一个使用局部作用域变量的简单 JavaScript 程序。

```
<!DOCTYPE html>
<html>
<body>
<h1>Javascript Example</h1>
<p id="demo"></p>
<script>
function demo() {
  var val = 1;
  // 变量 val 只能在这里使用
}
</script>
</body>
</html>
```

##### 3.10 内置函数

JavaScript 能够使用一些内置函数。下面的示例展示了一个内置数学函数的使用。

示例 18：以下程序展示了一个使用内置函数的简单 JavaScript 程序。

```
<!DOCTYPE html>
<html>
<body>
<h1>Javascript Example</h1>
<p id="demo"></p>
<script>
document.getElementById("demo").innerHTML = Math.PI;
</script>
</body>
</html>
```

##### 3.11 操作数组

JavaScript 能够将元素作为数组来处理。这帮助程序员处理连续的元素集合，如下所示。

示例 19：以下程序用于展示一个使用数组的简单 JavaScript 程序。

```
<!DOCTYPE html>
<html>
<body>
<h1>Javascript Example</h1>
<p id="demo"></p>
<script>
var val = ["1", "2", "3"];
document.getElementById("demo").innerHTML = val[0];
</script>
</body>
</html>
```

##### 3.12 处理错误

JavaScript 也能够通过使用 try、catch 块来处理程序中产生的错误。下面的示例展示了一个使用 try、catch 块的简单程序。

示例 20：以下程序展示了一个使用错误处理的简单 JavaScript 程序。

```
<!DOCTYPE html>
<html>
<body>
<p id="demo"></p>
<script>
try {
    funcA("Hello World");
}
catch(err) {
    document.getElementById("demo").innerHTML = err.message;
}
</script>
</body>
</html>
```

##### 3.13 处理 JSON 的能力

JSON 被称为 JavaScript 对象表示法，它像 XML 一样被用作中间语言。JavaScript 也可以处理 JSON 对象，如下例所示。

示例 21：以下程序展示了一个处理 JSON 的简单 JavaScript 程序。

```
<!DOCTYPE html>
<body>
<h2>JavaScript Example</h2>
<p id="demo"></p>
<script>
var text = '{"Names":[' +
'{"firstName":"John","lastName":"Doe" },' +
'{"firstName":"Peter","lastName":"Smith" }]}';

obj = JSON.parse(text);
document.getElementById("demo").innerHTML =
obj.Names[1].firstName + " " + obj.Names[1].lastName;
</script>
</body>
</html>
```

## 第四章：CSS3 基础

层叠样式表或 CSS 提供了网页的呈现方式。尽管 HTML 能够为网页提供基本结构，但 CSS 为开发者提供了大量的设计选项。除此之外，它快速且高效，这使其成为更受欢迎的设计工具。

CSS 据信是从 SGML（标准通用标记语言）演化而来。这一方向努力的目标是标准化网页的外观方式。该技术的最新版本是 CSS3，它由 50 个模块组成。

CSS 最强大的特性是其层叠能力。简单来说，它允许一个网页从多个样式表中获取样式，这样在后续读取的样式表中对样式的更改会覆盖先前一个或多个样式表中已实现的样式。

如何定义和应用样式

样式的定义和应用涉及两个方面或部分：选择器和声明块。选择器决定了网页中需要被设置样式的区域，而声明块则描述了需要应用的样式规范。为了说明其工作原理，让我们看下面的例子：

```
body {
    color: white;
}
```

在这个例子中，选择器选中了网页的 body，声明块定义了字体颜色应更改为白色。这是一个简单的例子，声明和选择器可以比这复杂得多。

如何添加注释

可以使用以下格式在样式表中添加注释：

```
/*write the comment here*/
```

### 如何创建内联样式

每个元素都有一个关联的全局属性 `style`。该全局属性可以在该元素的标签内进行操作，以修改该元素的外观。这种类型的样式不需要你指定选择器，只需要声明块即可。以下是实现示例：

```
<body style='color: white;'></body>
```

这个 HTML 标签实现的功能与上一节中指定的 CSS 代码相同。使用此方法的优点是，以这种方式给出的样式信息会覆盖任何其他样式信息。因此，如果你需要为某个元素使用不同的样式，而文档的其余部分需要遵循不同的样式，那么你可以使用样式表，并在该元素的标签中为其指定样式。

### 如何使用嵌入式样式

另一种实现与内联样式相同效果的方法是使用相关元素中的 `<style>` 元素来定义其样式规范。以下是操作方法：

```
<!DOCTYPE html>
<html xmlns='http://www.w3.org/1999/xhtml'>
<head>
<title></title>
<style>
body {
color: white;
}
</style>
</head>
<body>
</body>
</html>
```

### 如何创建外部样式表

当你希望为整个网页或多个网页使用相同的样式时，最佳方法是使用外部样式表。

可以按以下方式将此外部样式表链接到 HTML 页面：

```
<!DOCTYPE html>
<html xmlns='http://www.w3.org/1999/xhtml'>
<head>
<title></title>
<link rel='stylesheet' type='text/css' href='Content/mainstyle.css' />
</head>
<body>
</body>
</html>
```

你必须在 `Content` 文件夹中创建一个名为 `mainstyle.css` 的文件，并将下面指定的样式规则放入该文件中。

```
body {
color: white;
}
```

### 定义媒体类型

需要注意的是，一个样式表可以包含任意数量的样式规则。此外，你还可以为不同的媒体类型链接不同的 CSS 文件。不同的媒体类型如下：

- all
- embossed
- braille
- print
- handheld
- speech
- screen
- tv
- tty

可以按以下方式定义使用的媒体：

```
<link rel='stylesheet' type='text/css' href='Content/all.css' media='all' />
```

### 定义字符编码

你还可以使用以下格式定义所使用的字符编码：

样式表：
在样式表中的样式规则上方放置以下行。

```
@charset 'UTF-8';
```

HTML 页面：
你必须将此行放置在 `<link>` 元素上方。

```
<meta http-equiv='Content-Type' content='text/html;charset=UTF-8' >
```

### 导入样式表

随着网页变得复杂，使用的样式表也会变得复杂。因此，你可能需要使用多个样式表。你可以使用以下方式将一个样式表中的样式规则导入到另一个样式表中：

```
@import url('/Content/header.css');
```

这里导入了 `header.css`，`url` 给出了要导入的样式表的相对地址。

### 导入字体

可以使用以下格式导入字体：

```
@font-face {
font-family: newFont;
src: url('New_Font.ttf'),
url('New_Font.eot'); /* IE9 */
}
```

### 选择器、特异性与层叠

选择器可以分为三种类型：类选择器、ID 选择器和元素选择器。元素选择器类型最简单，只需要命名要使用的元素即可。例如，如果你想更改 `body` 的背景颜色，那么使用的元素选择器就是 `body`。

在声明任何元素时，你可以使用 `id` 属性为其分配一个 ID。你可以使用以 `#` 为前缀的此 ID 作为选择器。例如，如果你创建了一个 ID 为 `btnID` 的按钮，那么其 ID 选择器将是 `#btnID`。类似地，你可以使用 `class` 属性为元素分配一个类名。类名可以以点（`.`）为前缀使用，例如 `.className`。

然而，如果你想选择网页中的所有元素，请使用星号（`*`）选择器。

#### 使用后代选择器和子选择器

你可能希望将特定样式应用于选择器的后代。这可以通过指定完整的选择器链来实现。可以按以下方式完成：

```
li a {
    text-color: black;
}
```

另一方面，你可能希望仅在元素是选择器的直接子元素时才应用样式。这可以通过指定父元素和子元素并用大于号（`>`）分隔来实现，如下所示：

```
li > a {
    color: white;
}
```

#### 伪元素和伪类选择器

既然你知道如何为特定元素应用样式，让我们继续学习如何为更具体的区域（如第二段的第一行）实现样式。为了样式化那些无法根据名称、内容进行分类或不是 DOM 树一部分的元素，可以使用伪类进行样式化。可用的伪类包括：

- :visited
- :link
- :hover
- :active
- :checked
- :focus
- :nth-last-child(n)
- :not
- :only-child
- :nth-child(formula)
- :lang(language)
- :first-of-type
- :only-of-type

如果你想访问 DOM 树中通常不可访问的信息，可以使用伪元素。伪元素包括：

- ::first-letter
- ::first-line
- ::after
- ::before

##### 分组选择器

一个样式规则可以使用多个选择器。这些选择器必须用逗号分隔。示例实现：

```
body, button {
  color: white;
}
```

#### 使用相邻选择器

如果你想为 `div` 中的第一个标题或任何类似的相邻元素设置样式，选择器使用两个选择器之间的加号（`+`）来构建。示例实现：

```
div + h1 {
  color: white;
}
```

#### 兄弟选择器

兄弟选择器与相邻选择器类似，不同之处在于所有匹配的元素都会被样式化，而相邻选择器只样式化第一个匹配的元素。选择器使用两个选择器之间的波浪号（`~`）来构建。示例实现：

```
div ~ h1 {
  color: white;
}
```

#### 使用属性选择器

此选择器选择所有存在指定属性的元素。选择器的书写形式如下：

```
a[title]
```

此选择器将选择所有指定了 `title` 属性的链接。此外，这种选择器类型可以通过指定属性值修改为属性值选择器，如下所示：

```
a[title = value]
```

### 浏览器的内置样式

每个浏览器都有一个内置样式表，该样式表应用于使用此浏览器打开的所有网页。实际上，此样式表在任何其他样式表之前应用。你可以使用“工具”菜单中的“辅助功能”选项为浏览器定义自己的样式表。但是，用户样式表是特定于浏览器的。因此，如果你打开不同的浏览器，你定义的样式表可能无法访问。

如果你希望你定义的用户样式表覆盖 HTML 页面中指定的任何其他样式，则可以使用 `!important` 修饰符。此修饰符为指定的样式语句设置最高优先级。示例实现：

```
body {
  color: white !important;
}
```

### 样式的层叠

样式的优先级和权重由以下参数决定：

- 重要性
- 特异性
- 文本顺序

### 使用 CSS 属性

既然你已经熟练掌握了选择器的使用，下一步是了解 CSS 属性。

#### 颜色

网页中使用的最关键属性之一是颜色，可以使用 ARGB、RGB 和颜色名称来定义。RGB 值通常定义为 0-255 之间的十进制数。



##### 颜色值

- 白色 #ffffff
- 红色 #ff0000
- 黑色 #000000
- 绿色 #008000

颜色值也可以替代颜色名称使用。下面给出一个使用示例。

```css
body {
    color: #ffffff;
}
```

指定颜色的另一种方式是使用 RGB 函数，它通过 0 到 255 之间的数字或百分比来指定参数值。此类声明的示例如下：

```css
h1 { color: rgb(255,0,0); }
```

其他指定颜色的方式包括 RGBA（接受 4 个值）和 HSL（定义色相、饱和度和亮度值）。

##### 透明度

透明度或不透明度由一个介于 0.0（不可见）和 1.0（不透明）之间的值来定义。

### 文本

关于文本，可以指定 font-face 和 font-size。这些属性可以按以下方式定义：

```css
h1 { font-family: arial, verdana, sans-serif; }
h1 { font-size: 12px; }
```

### CSS 盒模型

CSS 盒模型假定一个网页可以看作由若干盒子组成。这些盒子之间的间距由外边距（margin）和内边距（padding）设置决定。这些属性可以按以下方式赋值：

```css
margin: 15px;
padding: 25px;
border: 10px;
```

### `<div>` 元素的定位

用于创建页面布局的元素是 `<div>`。虽然 HTML5 推荐使用语义化标记代替 div 元素，但对于无法使用语义化标记设置样式的具体内容，它们仍在使用。div 元素可以被想象成一个矩形块，并按以下方式声明：

```html
<div>
<!--other elements are enclosed within this area-->
</div>
```

用于定义 div 元素位置的属性包括：

- 可以使用 top、bottom、left 和 right 属性（以像素为单位）来定义 div 元素的位置。
- 一个名为 position 的属性用于定义指定的位置是静态的（static）还是相对的（relative）。
- float 属性可用于让元素向右或向左浮动，定义为 `float: left` 或 `float: right`。
- clear 属性在浮动元素之后放置一个清除元素。
- 还可以通过 box-sizing 属性更改浏览器计算宽度的方式。该属性可以取三个值：content-box（默认设置）、border-box 和 padding-box。

### 内容居中

如果使用固定宽度，可以使用 margin-left 和 margin-right 属性来居中 div 元素。如果固定宽度并将外边距设置为 auto，外边距上的额外空间将被平均分配。可以按以下方式进行：

```css
#container {
width: 850px;
margin-left: auto;
margin-right: auto;
}
```

## 第五章：慢慢思考，保持谦逊

编写代码可以很快，特别是当你知道自己在做什么，并且对你编写的 JavaScript 字符串中的代码有很多经验时。你可能会进行得很快，而这可能导致你犯错。如果你对 JavaScript 变得非常有经验，并且觉得自己能用它做更多事情时，情况尤其如此。你可能还会发现，当你编写代码的水平提高时，你会对自己所做的一切非常有信心。有信心并不是一件糟糕的事，但它可能导致你忽略一些本可能犯错的地方。为了确保你能出色地完成代码工作，即使在练习时，你也应确保尽可能慢地思考，并且不要对自己的能力过度自信。

### 放慢速度

在编写你正在构思的代码时，确保尽可能放慢速度。一开始这样可能花费更多时间，但在回溯并处理你可能因错误而需要处理的不同事项时，它会为你节省大量时间。通过放慢速度，你将更不容易产生错误。

即使当你回顾代码并逐行检查每一行 JavaScript 时，也要慢慢看。阅读每一个字母和符号，这样你才能知道你在说什么，并且能够发现是否遗漏了什么。这就像你在高中或大学写论文时可能进行的校对一样。放慢速度，逐行校对你写的代码和你做的工作。这种慢节奏将帮助你发现可能犯下的任何错误。

同样值得注意的是，放慢速度将帮助你在工作中避免任何重大错误。如果你的节奏更慢，你将更清楚每一次击键和你输入每一行代码的内容。这种慢节奏不仅在你回顾写下的内容时有帮助，在你编写代码时所做的每一步也同样有益。确保你准备好尽可能慢地进行，不要仓促完成工作。

### 休息一下

从你正在做的工作中休息一下总是有益的。连续查看代码数小时后，不仅你的眼睛会疲劳，你的大脑也会开始感到疲倦。休息将帮助你更新状态，并让你有机会在脑海中一片空白时重新开始。拥有清醒的头脑编写代码有许多好处，而休息将给你提供完美的refreshment。

总的来说，每编写一小时代码，你应该花 5-10 分钟远离电脑，站起来走动一下，做一些与 JavaScript 无关的事情。利用这段时间到外面呼吸新鲜空气，或者只是走动一下锻炼一下身体，是个好主意。做这两项活动都有助于血液循环，并为大脑提供所需的氧气，使其在你决定再次坐下来开始编写代码时能更高效地工作。

提醒一句：在离开电脑屏幕休息的时间里，尽量不要使用手机。虽然屏幕小得多，但手机屏幕发出的蓝光与电脑屏幕相同，都可能对你有害。在工作时为使用手机设定专门的时间，这样你就不用占用屏幕休息时间和朋友聊天或查看非工作邮件了。休息时最好将手机放在够不着的地方。

### 逐步检查

一旦写完了想写的代码，你需要确保逐步检查它。这个过程应像编写过程一样缓慢，以便你能发现自己可能犯下的任何错误。你应该在写完最后一行代码后、测试不同功能之前进行这一步。确保缓慢进行并查看每一行代码总是个好主意。

确保你检查了编写的每个字符的一种方法是大声读出来。对自己说出每个字母、数字和字符，以确保它们书写正确。大声朗读总是个好主意，因为它能让你看清自己实际写的内容。大声朗读会比在心里默读花费更多时间。如果你在心里默读，可能会遗漏许多事情。

虽然大声朗读编写的每一行代码可能看起来很复杂，但你仍然应该尝试这样做。这样做能让你有机会发现可能遗漏的内容。如果你擅长阅读并确保自己没有犯任何错误，你将能高效地完成，而不会浪费太多时间。实际上，它所花费的时间会少于回头修复所有错误所需的时间。

### 平衡自信

虽然在你刚开始学习或学习编码时可能不会遇到这个问题，但对于编写 JavaScript 的人来说，自信可能是一个大问题。你认为自己对它了解得足够多，在编写代码时基本上放松了警惕。这是一个问题，因为你在编写代码时不会那么快发现错误，并且可能认为你编写的代码没有任何问题。

重要的是要确保控制好自己的自信。即使你觉得自己非常擅长编写代码，永远不会犯错，你犯错的可能性仍然很高。在编写任何类型的代码行时，任何人都可能随时犯错。确保你知道自己在做什么，并且不要对自己的技能变得自恋。在编码方面，总有更多的东西可以学习，没有人能完全掌握它。

你的信心甚至会欺骗你，让你忘记自己学到的代码知识。信心告诉你，你知道自己在做什么，你知道编写代码的最佳方式。它告诉你，为每一行代码反复编写相同的内容没有问题，但它也告诉你，无需尝试不同的编码选项来做得更好。确保你对自己的技能有信心，但不要让这种信心过高，以至于阻碍你通往成功的道路。

### 不要信任自己

不要信任自己。你的头脑会试图告诉你，在检查自己编写的代码时，你没有犯错，也没有遗漏任何东西，但很有可能你实际上遗漏了一些行，并且犯了一些错误。务必始终质疑自己是否在进行最佳的编码工作，以便能够写出你期望的准确代码。不要相信自己能完成，但要始终检查自己是否在做正确的事情。

一个好方法是在编写和检查代码之间休息一下。确保休息时间足够长，以便真正恢复精力。把它当作一次休息，但要花更长的时间，这样当你开始测试和查看代码时，才能真正以全新的状态回来。如果你盯着同样的100行代码看了5个小时，然后试图编辑它们，你将很难找出你犯的错误。

本书第一部分各章节中的所有技巧都涉及在实践中学习你能做什么。它们本质上是你可以用来提高编码实践效果的思维技巧。在本书的其余部分，你将学习如何在开始编码时应用这些技巧。真正的乐趣在于你在本书的第二部分学习到最佳代码时。

## 第六章：基本运算符

### 什么是运算符？

运算符基本上是充当函数的符号，尽管它们在语法上不同于函数。它们接受输入（操作数）并根据操作数产生特定的输出。例如在“5+2”中，“5”和“2”是操作数（输入），而“+”符号是运算符，结果为“7”。

### 运算符的分类

运算符通常根据它们执行的操作类型进行分类。像typeof、instanceof等运算符是独特的，因此无法归入以下将要读到的类别。

#### <u>算术运算符</u>

顾名思义，这些是对操作数执行算术任务的运算符。下面列出了算术运算符。

加法[+]：如果两个操作数都是数字，此运算符对两个操作数执行加法操作。如果其中一个或两个操作数都是字符串类型，则此运算符连接/连接两个操作数。

示例：
4 + 2//结果为6
‘example’ + 5//结果为“example5”
‘thisIs’ + ‘Example’ //结果为“thisIsExample”。

减法[-]：此运算符对两个操作数执行减法操作。示例：“4-2”产生结果“2”。

除法[/]：此运算符对两个操作数执行除法操作，其中左侧的操作数（被除数）除以右侧的操作数（除数）。示例：“15/3”产生结果“3”。

乘法[*]：此运算符对两个操作数执行乘法操作。示例：“4*2”产生结果“8”。

取模[%]：也称为余数运算符，此运算符产生两个操作数相除后的余数。示例：“5%2”产生结果“1”，“5%3”产生结果“2”。

递增[++]：将其数值操作数的值增加一。此运算符的位置很重要，即它放在操作数之前还是之后。如果放在操作数之前，则称为前缀（例如++x），并且值在递增操作之后返回。如果放在操作数之后，则称为后缀（例如x++），并且值在递增操作之前返回。

示例：
//假设x的值为5
console.log( ++x ); //打印6
//此时x的值为6
//假设y的值也为5
console.log( y++ ); //打印5，不是6
//但此时y的值为6，所以递增操作完成了，但表达式返回的是递增前的值

递减[--]：将其数值操作数的值减少一。与递增运算符类似，后缀和前缀规则也适用。

示例：
//假设x的值为5
console.log( --x ); //打印4
//此时x的值为4

//假设y的值也为5
console.log( y-- ); //打印5
//此时y的值为4

指数[**]：此运算符产生将第一个操作数提升到第二个操作数的幂次方的结果，即FirstOperand**SecondOperand。示例：“2**3”产生结果“8”。

### 赋值运算符

这些运算符用于为变量赋值。值被赋给左操作数，这是基于右操作数的值。下面列出了赋值运算符。

等于[=]：此运算符简单地将其右操作数的值赋给左操作数。示例：“x=5”将5赋给x，因此现在x的值为5。

加法赋值[+=]：此运算符将左操作数和右操作数的值相加，然后将结果赋给左操作数。示例：假设x=2，则“x += 3”将使x的值为5。

减法赋值[-=]：此运算符将右操作数的值从左操作数中减去，然后将结果赋给左操作数。示例：假设x=8，则“x -= 3”将使x的值为5。

乘法赋值[*=]：此运算符将左操作数和右操作数相乘，然后将结果赋给左操作数。示例：假设x=5，则“x *= 2”将使x的值为10。

除法赋值[/=]：此运算符将左操作数（被除数）除以右操作数（除数），然后将结果赋给左操作数。示例：假设x=10，则“x /= 2”将使x的值为5。

取模赋值[%=]：此运算符将左操作数（被除数）除以右操作数（除数），然后将余数赋给左操作数。示例：假设x=5，则“x %= 2”将使x的值为1。

指数赋值：此运算符将左操作数的值提升到右操作数的幂次方，然后将产生的结果赋给左操作数。示例：假设x=2，则“x **= 3”将使x的值为8。

### 其他运算符

这些运算符无法归入上述类别。下面列出了此类运算符。

typeof运算符：此运算符以字符串格式返回操作数的类型。示例：

```
typeof 2//结果为“number”
typeof 1.23//结果为“number”
typeof “2”//结果为“string”
typeof ‘hi’//结果为“string”
typeof true//结果为“boolean”
typeof false//结果为“boolean”
typeof {ob:1}//结果为“object”
typeof new Date()//结果为“object”
typeof Math.cos//结果为“function”
typeof function(){}//结果为“function”
```

instanceof运算符：此运算符检查第一个操作数（应为对象）是否属于特定类型，其中要检查的类型在第二个操作数中指定。它根据对象类型是否匹配返回true或false。

示例：

```
new String(“Astring”) instanceof String//结果为true
```

```
["this", "is", "array"] instanceof Array//结果为true。
new String("Astring") instance of Array      //结果为false
["this", "is", "array"] instanceof String//结果为false
```

delete运算符：此运算符从对象中移除一个属性。
示例：

```
var myObject = {
prop1: "test",
prop2: "test2"
};

delete myObject.prop1;//删除对象myObject的prop1属性
```

in运算符：此运算符检查指定的属性（第一个操作数）是否在指定的对象（第二个操作数）中。它根据属性是否在对象中返回true或false。
示例：

```
var myObject = {
prop1: "test",
prop2: "test2"
};

"prop1" in myObject;//结果为true
"prop45" in myObject;//结果为false
```

本章解释了JavaScript中的运算符。希望你觉得它有用。



### 结论

以上内容应该让你对 JavaScript 中事件的使用方式以及为何一开始就需要使用它们有了基本的了解。需要注意的是，事件是应用程序中发生的任何事情，我们可以为事件附加监听器，以确保在事件发生时能够获知，从而在此时执行一些代码。

非常感谢您下载 *JavaScript: Beginner JavaScript Coding From The Ground Up!* 请留意本系列的下一本书，*JavaScript: Intermediate JavaScript Coding From The Ground Up*。要拓展您的编码知识库，还有更多内容有待学习。对我们而言，学习之旅不会停留在初学者阶段。

如果您喜欢这本书，请在亚马逊上留下积极评价以示支持。非常感谢您的反馈！
