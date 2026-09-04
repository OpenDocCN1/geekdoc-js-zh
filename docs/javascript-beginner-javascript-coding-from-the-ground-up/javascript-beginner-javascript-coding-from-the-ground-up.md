
# JavaScript 入门指南：从零开始学习 JavaScript

## 第一章 JavaScript 简介

JavaScript 被称为“网页语言”，因为它被用于大量的 Web 和移动应用程序。它是让 Web 变得动态的语言，使用户能够与之交互，提供丰富的用户体验。

当 JavaScript 在 1995 年左右诞生时，网页中的大多数逻辑计算和输入验证主要是使用 PHP 等服务器端语言完成的。这个过程非常漫长，并且涉及不必要的双向传输：首先向服务器发送请求，然后将数据/错误返回到客户端计算机。这对用户体验（UX）来说是一个巨大的遗憾。当时的需求是在发送到服务器之前，直接在客户端计算机上进行验证，从而减少带宽——这在当时是一个主要问题，用户不需要为了查看自己在填写表单时是否输入了任何错误而等待。

JavaScript 由 Brendan Eich 在 1995 年创建的，最初名为“LiveScript”，后来被更名为“JavaScript”。它最初被命名为“Mocha”，但后来改为 JavaScript，以获得当时流行的 Java 语言的关注度。第一次重大标准化是以 ECMA 标准化的形式出现的。开发的第一个版本仍然缺乏 REGEX 和 JSON 以及一些重要的内置函数。该语言不断发展并向其功能库中添加新功能。

ECMA v3 见证了 AJAX（异步 JavaScript 和 XML）的诞生，如今它是每个 Web 应用程序和框架的核心。

目前，该语言充满了许多令人兴奋的新特性。让我们来看看使用 JavaScript 带来的优势：

- JavaScript 是一种轻量级的、解释型的编程语言。
- 设计用于创建简单及复杂的 Web 应用程序
- 增强了网页的功能
- 可以轻松实现动画和视觉效果
- UI/UX 的改进

由于该语言的成功和易用性，开发了许多如 jQuery、Angular JS、React JS 等框架和库，使得编写 JavaScript 代码变成了一件享受。

JavaScript 是一种全球开发者都在积极使用的脚本语言，用于创建视觉上吸引人且功能上类似于桌面应用程序的交互式 Web 应用程序。

这意味着网页在本质上不是静态的。通过这种语言作为脚本工具，可以对元素进行修改并使其具有交互性、功能性和动画。

JavaScript 最初是客户端脚本语言，但现在也以 Node.js 的形式用于 Web 后端。在此期间出现了许多库和框架来简化开发者的生活。

JavaScript 有内置以及用户定义的方法/函数，允许它们绑定到某些按钮或元素上，并随时随地被调用。这些函数被积极用于自动化任务，例如 `setTimeout()` 或 `setInterval()` 函数，它们可以在一段时间后调用以执行某些任务。JavaScript 可以直接写在 HTML 文件中（如果写入 `<script>` 标签中），也可以作为外部文件附加它。JavaScript 程序的扩展名是 `.js`。

JavaScript 通常缩写为 JS。该语言的一些主要特性如下：

- 高级、弱类型
- 解释型
- 函数式
- 面向对象

面向对象的设计也许是 JavaScript 最重要的特性，因为它允许我们创建对象并建立它们之间的关系，通常被称为“继承”和“封装”，你将在后续章节中了解到这些内容。

## 第二章 JavaScript 的主要特性

JavaScript 的大多数特性在某种程度上与其他编程语言相同。几乎所有的编程语言都具有这些特性。主要特性如下：

### 1. JavaScript 变量

JavaScript 的非常重要的特性之一是变量。它们充当值的存储容器。换句话说，它们是存储值的内存位置名称。这些值可以是整数、小数、字符串或单个字符。变量名必须是唯一的。这很重要，因为否则将造成巨大的混乱。变量名可以从字母、美元符号或下划线开始。名称对大小写敏感。你将在章节中了解变量命名的精确规则。

一些变量的示例：`var abcd; var $abc;`

### 2. JavaScript 对象

对象无非某些数据值的集合。它们通常以键值对的形式编写。例如：`var name = {firstName:"Amit", lastName:'Kumar', age:70};` 要访问对象中的值，我们使用点符号（dot notation）。例如，如果你想访问 `name` 对象中的 `lastName`，我们可以写成 `name.lastName`。数组是对象的一种。

### 3. JavaScript 注释

注释是初学者经常忽视的特性，但随着编程经验的增加，他们意识到它为代码带来的巨大价值。这些基本上是在代码中创建笔记的方法。这提高了代码的可读性。它们不会被编译器执行。

注释有两类类型：

- a. 单行注释
- b. 多行注释

  - a. 单行注释：顾如其名，用于注释单行内容。例如：`var name; //name of the customer`
  - b. 多行注释：如果注释长度超过一行则使用。例如：`/* This program calculates the factorial of a number */`

### 4. JavaScript 函数或方法

函数是任何编程语言不可或缺的一部分。函数帮助我们以高效的方式编写代码，不仅提高了代码的可读性，而且在维护方面做了巨大贡献。函数是一组用于执行特定任务的语句。例如：

```javascript
function addTwoNumbers(num1, num2) {
return num1+num2; //Calculates and returns the sum
}
```

你将在后面的章节中详细学习函数。

### 5. 条件语句

当我们根据某些条件做出特定决策时，就会使用条件语句。例如，如果有一个程序用于判断某人是否有投票资格，我们输入人的年龄并将其与 18 岁进行比较。如果大于 18 岁，我们就说该人有投票资格，否则不具备。

例如：`if(age>18) alert("eligible to vote"); else alert("Ineligible to vote");`

### 6. JavaScript 中的循环结构

循环用于反复执行代码的某部分。我们有多种方式来实现循环，例如：`for` 循环、`while` 循环、`do-while` 循环。

例如：`for (i = 0; i < 10; i++) { alert(i); }`

### 7. JavaScript 中的事件处理

事件发生在网页上的某些活动。例如，网页上的鼠标点击、网页的加载等。事件处理是一种处理当此类事件发生时发生了什么的方法。一些常见的事件处理器有 `onclick`、`onload`、`onmouseover` 和 `onmouseout`。

这是一个非常重要的概念。如果没有事件处理，开发任何 Web 应用程序都是毫无意义。

本章简要介绍了 JavaScript 的主要特性。本书的后续章节将详细解释这些特性。

## 第 3 章 JavaScript 的现实用途

JavaScript 几乎用于网络上的几乎每一个网站，为什么不呢？它为任何使用这种脚本语言的页面增加了许多功能性。如果没有 JavaScript，我们可能仍然停留在 90 年代，那时网站不向用户提供任何功能。从用户体验（UX）的角度来看，它完全不直观，而这也许是该语言带给我们最好的东西。

JavaScript 实际上无处不在。从你提交的表单到现代网站菜单上的下拉按钮，从你留空空白字段时显示的众多错误，到最烦人却实用的警告框，它们都是使用 JavaScript 制作的。

到这里，你可能已经猜到了 JavaScript 能带来什么。

是的，一切。

学习该语言的基础、简单语法可以让你拥有构建一个看起来相当体面的计算器的能力，如果你恰好洒上一点 CSS 的魔法，它看起来将非常惊人。这正是该语言实际用途真正开始的地方。

让我们来看一些 JavaScript 证明是有益的实际现实场景：

### 案例 1：表单验证

一个良好的互联网表单被认为是利用 JavaScript 的力量来验证用户输入，并在任何空字段或发生不当的字段输入时显示错误。让我们假设没有使用 JavaScript 的情况。在这种情况下，填写表单的用户必须先提交表单，由于他还不知道自己是否犯了任何错误，当提交时，它会被发送到服务器通过 POST 请求进行处理，然后服务器响应可能发生的任何错误。这是一次双程旅行。

如果我们使用 JavaScript 进行客户端验证，就可以节省很多这些工作。JavaScript 的力量就在这里体现了，当用户在填写表单本身时犯任何错误时，它可以在几秒内做出响应。

### 案例 2：DOM 操作

大多数时候，服务器返回一个静态 Web 页面，浏览器对其渲染并在浏览器中显示它。但是，如果我们获得了操纵网页上几个元素的权力呢？如果我们能够改变事物的状态、顺序、属性甚至它们的特征，并且它能变成一个完全全新的东西，难道不觉得很兴奋吗？事实证明，JavaScript 为我们提供了所有实现这一切的因素。非常棒。

### 案例 3：事件监听器

用户真正与网页交互的唯一方式是他们被允许点击按钮并获得响应，例如打开新页面，或者更改网页上的某些数据，或者允许他们进行即时计算。JavaScript 允许我们通过将函数附加到网页上的按钮或元素来实现该功能，这些通常被称为 DOM（文档对象模型）元素，它们将自己绑定到该元素，并仅在执行所需操作时才执行或触发。这让用户体验感到非常满意。

JavaScript 有许多用途，丰富了网页的 UX。在当今的现代网站中，客户端渲染（Client Side Rendering）已经产生了一类新的 Web 页面，称为单页应用程序（SPA），它们能够仅使用来自服务器的 JSON 数据动态生成 HTML 页面。这弥补了 Web 开发中前端和后端之间的差距。

Web 的未来在 JavaScript 手中看起来是光明的。

## 第 4 章 你的第一个 JavaScript 程序

HTML 为网页添加结构，CSS（层叠样式表）添加使页面看起来优雅所需的相应样式。

但是，你如何让页面说话呢？你如何让它动态起来呢？

这就是 JavaScript 的用场。

JavaScript 为相当静态的网页增加了额外的功能，并允许用户与页面中存在的各种元素进行交互。

在本章中，你将编写你的第一个 JavaScript 程序——著名的“Hello, World!”，它将向你介绍这个巨大而简单的语言，它通常被誉为“Web 之语言”。假设你已经熟悉 HTML 和 CSS 语法，因为它们将贯穿全文。

浏览器渲染 HTML 和 CSS 并将其显示在屏幕上，并内置了一个 JavaScript 解释器，可以理解该语言并执行它。

为了让浏览器知道何时开始解释，我们需要使用 `<script>` 标签。但为了让浏览器知道 JavaScript 的起点，我们需要使用 `<script>`。

为了直接在页面中嵌入 JavaScript，你可以使用 `<script>` 和 `</script>` 标签，这些标签通常放置在 `<body>` 标签之前。

为了让页面加载更快，可以使用 `<script>` 标签。

### 你的第一个程序

让我们创建一个让警告框显示“Hello, World!”的程序。

```html
<html>
<head>
<title>第一个程序</title>
</head>
<body>
<h1>这是你的第一个程序</h1>
<script>
alert("Hello World!");</script>
</body>
</html>
```

结果：

![result](9a74f6e8b0)

如果你使用的是 Chrome 或 Safari 等现代浏览器，它们支持 HTML5。但如果你在旧浏览器上，则需要添加 `type` 属性，如下：`<script type="text/javascript">...</script>`

`alert()` 函数接收括号中的字符串并显示警告框。在这里，我们希望警告框显示“Hello, World!”。

恭喜！你刚刚完成了第一个 JavaScript 程序。虽然 JavaScript 提供了许多功能，但这是为了开始学习这种被恰切称为 Web 之语言的语言。

## 第 5 章 在 HTML 中嵌入 JavaScript 代码

你可以将 JavaScript 用于 HTML 以获得动态且愉快的用户体验。在本章中，我们将学习在文档中嵌入 JavaScript 的各种方法。

为了直接在页面中嵌入 JavaScript，你可以使用 `<script>` 标签。

`<script>` 标签的语法如下：`<script> //JavaScript 代码在这里，例如：alert("Hello from JavaScript!");</script>` 有许多可选属性可用于 `<script>` 标签。

**type**: 此标签用于指定 `<script>` 标签之间编写的语言，但由于 JavaScript 是所有浏览器主要的脚本语言，因此没有强制使用此属性，因为它是默认设置。这是一个示例：`<script type="text/JavaScript">JavaScript 代码</script>`

**src**: 如果你想从外部加载 JavaScript 代码，那么这就是你应该查看的属性。外部 JavaScript 代码的 URL 是此属性的值。

```html
<script src="url/to/external/JavaScript.file.js"></script>
```

**defer**: 如果 `<script>` 标签中存在此属性，则与脚本关联的 JavaScript 文件将在页面完全解析后执行，即在触发 `DOMContentLoaded` 事件时。示例：`<script src="path/to/file.js" defer></script>` 注意此属性仅适用于外部加载的 JavaScript 代码，即在同一个 `<script>` 标签中存在 `src` 属性。

**async**: 如果 `<script>` 标签中存在此属性，则与脚本关联的 JavaScript 文件将在页面继续加载时异步执行。如果没有此标签，则脚本会先执行，然后页面继续加载。示例：`<script src="path/to/file.js" async></script>` 注意此属性仅用于外部加载的 JavaScript 代码，即如果 `src` 属性与 `defer` 属性出现在同一个 `<script>` 标签中。

在 HTML 中嵌入 JavaScript 还有另一种方法，是在元素的事件处理器属性中编写 JavaScript 代码。这种情况下，当事件触发时，作为属性值编写的 JavaScript 代码就会被执行！

```html
<button onclick="alert('JavaScript from event handler');">Click me</button>
```

在上面的示例中，当点击按钮时会弹出一个带有消息“JavaScript from event handler”的警告对话框，表明属性值中的 JavaScript 已被执行。

如果你无法理解上面的代码示例，请不要担心。事件和事件处理器属性将在本书的后面详细讨论。

本章的内容就到这里，现在你已经准备好将 JavaScript 嵌入到你的 HTML 文档中并使其变得更强大了！

## 第 6 章 JavaScript 基础显示操作

以下是 JavaScript 显示数据的几种方式：

- 使用 `innerHTML` 将内容写入 HTML 元素。
- 使用 `document.write()` 写入 HTML 输出内容。
- 使用 `window.alert()` 写入警告框中。
- 使用 `console.log()` 写入浏览器控制台。

### innerHTML

顾如其名，“innerHTML”代表 HTML 元素的内部内容。因此，基本上我们可以使用 `innerHTML` 属性来更改任何 HTML 元素内部的内容。然而，这里有一个小陷阱。JavaScript 如何知道我们实际上想要更改的是哪个元素呢？如果它更改了网页上所有元素的内容怎么办？为了解决这个问题，我们为感兴趣要更改内容的 HTML 元素分配一个 `id`。这样我们就能确定哪个元素应该反映变化。我们面临的下一个问题是如何根据 `id` 访问 HTML 元素。在这种情况下，我们使用名为 `document.getElementById("ID")` 的方法。

更改 HTML 元素的 `innerHTML` 属性是 HTML 中显示数据的常用方法。

让我们来看一个示例。

```html
<!DOCTYPE html> <html><body><h1>Chapter 6</h1> <p>Use of innerHTML to display data</p> <p id="new"></p> <script>document.getElementById("new").innerHTML = "This is how it’s done";</script></body></html>
```

### document.write()

这是另一种使用 JavaScript `document.write()` 在网页中显示数据的有趣方法。整个网页可以称为一个文档（document）。正如该函数的名称所示，它是用于在文档上写入内容的。如果在页面加载后使用它，它不仅会写入，还会用新值替换现有的（旧）值。因此，在使用时必须非常小心。它主要用于测试目的。

让我们通过示例来理解这一点：

```html
<!DOCTYPE html> <html><body><h1>Chapter 6</h1> <p>Use of document.write() to display data</p> <script>document.write(1+2); </script></body></html>
```

正如我所说的，在 HTML 文档完全加载后使用 `document.write()` 会**删除所有现有的 HTML**。让我们通过一个示例来看：

```html
<!DOCTYPE html><html><body><h1>My First Web Page</h1><p>My first paragraph.</p><button onclick="document.write (1+2)">Magic Button!! </button></body></html>
```

### window.alert()

你可能在很多网站上看到过“你似乎输入了错误的密码”（You seem to have entered a wrong password）的警告。这些以小对话框的形式出现，通常用于提醒用户某事。

```html
<!DOCTYPE html> <html><body><h1>My First Web Page</h1> <p>My first paragraph.</p> <button onclick="window.alert(1+2)">Add 1 & 2</button></body></html>
```

`console.log()` 是开发者的救星。它被用于调试。`console.log()` 的结果不会显示在网页上。相反，它显示在控制台中。这是一个非常有用的功能，因为有时你不希望测试数据显示在网页上。这些数据被开发者用来判断一切是否运行正常。如果你好奇控制台看起来是什么样的，请在 Google Chrome 浏览器的目标网页上按下 `ctrl+shift+I`。

```html
<!DOCTYPE html><html><body><script>console.log("it is in console");</script></body></html>
```

当你开始用 JavaScript 创建应用程序时，你将更加熟悉 `console.log()`。

以上是我们在 JavaScript 中显示数据的四种方式。然而，必须记住，它们的用法取决于需求。你需要根据所需的结果选择合适的方法。

## 第 7 章 变量、数据类型与常量

### 变量

变量始终是任何编程语言中的重要方面。它们被用于存储值，稍后可以使用变量名来访问这些值。JavaScript 也是如此。让我们来看创建变量的语法：

### 语法

```
var <variableName>; // 声明变量 <variableName>
<variableName> = value; // 给变量赋值
var <variableName> = value; // 在同一行内声明并赋值
```

在第一种方法中，我们先声明变量，然后在程序的后续某点给它赋值。这里必须记住的唯一一点是声明必须在赋值之前。但在第二种方法中，声明和赋值都在同一行内完成。

让我们来看一些示例：

```javascript
var abc; // 声明
abc = "New variable"; // 赋值
var num = 33; // 声明和赋值
```

在上面的示例中，变量 `abc` 将存储字符串值 `"New variable"`，而变量 `num` 将存储数字 33。

让我们再看一个示例：

```javascript
var marksScience = 85; // 变量名
var marksMaths = 100;
var total = marksScience+ marksMaths;// 相加并存储结果
```

在上面的示例中，变量 `total` 将存储计算后的值即 185。

程序中使用的所有变量必须具有唯一的名称，否则在执行代码时可能会产生混乱。这些唯一的名称被称为标识符（identifiers）。为变量命名时，必须遵循某些规则。

### 变量命名规则

- 名称必须以字母、美元符号 (`$`) 或下划线 (`_`) 开头。
- 变量名中可以包含字母、数字、下划线和美元符号。
- JavaScript 中的变量名对大小写敏感。
- 你不能使用保留字/关键字作为变量名。

有效变量名的示例如下：

`Marks1`

`$abc`

`_fun`

`marks2`

你可能已经注意到我们使用“等号”符号来给变量赋值。这个“等号”符号被称为赋值运算符，用于初始化变量。

### 需要记住的几点重要提示：

- 1. 当你仅仅声明一个变量时，它不包含任何值。

例如：`var abc;` 这里，在我们赋值它某个值之前，变量 `abc` 将不包含任何值。

- 2. 可以在一条语句中声明多个变量。这样做，我们以 `var` 开始语句，并用逗号分隔变量。

例如：`var firstName="Amitabh", lastName="Kumar", age=70;`

- 3. 变量的声明可以跨多行。

`var firstName="Amitabh", lastName="Kumar", age=70;`

- 4. 大多数情况下，变量只是被声明，并在程序的后续某点进行初始化。正如第一点提到的，在声明之后，变量不包含任何值。准确地说，它持有的值是 `undefined`。例如：

```javascript
var name; 
```

在执行上述语句后，变量 `name` 将包含值 `undefined`。

- 5. 即使你重新声明一个 JavaScript 变量，它也会保留先前的值。

例如：

```javascript
var name="Amitabh";
var name;
```

即使在执行这些语句后，变量 `name` 仍然具有值 `"Amitabh"`。

### 数据类型

数据类型（Data types）顾如其名，表示变量可以持有的数据类型。JavaScript 变量可以持有多种类型的数据。例如字符串、数字、对象、布尔值等。

```javascript
var age = 70 // 存储数字
var lastName = "Kumar" // 存储字符串
var name = {firstName:"Amitabh", lastName:"Kumar"}; // 存储对象
var case=true; // 存储布尔值
```

数据类型是编程中一个重要方面，因为它规定了变量持有的是什么类型的数据。这有助于编译器理解可以对它们执行什么类型的操作。加法运算符应用于两个数字时会得到不同的结果，而应用于两个字符串时则会得到截然不同的结果。例如：`var name="Amit" + " " + "Kumar";`

`var age = 30+40;`

变量 `name` 将存储两个字符串拼接后的值，即 `"Amit Kumar"`，而变量 `age` 将存储 30 和 40 的相加值，即 70。

现在考虑接下来的示例：

`var abc = 70 + "Amit";`

如果我们尝试将上面的示例与普通算术联系起来，它并没有太大意义。在普通算术中，向字符串添加数字是不可能的。然而，看看 JavaScript 如何像所示处理该示例将很有趣：

`var abc = "70" + "Amit";`

当我们尝试将数字与字符串相加时，JavaScript 会将数字视为字符串。然而，如果我们的表达式是多个数字和字符串的混合呢！在这种情况下结果是什么？让我们来看下面的示例：

`var temp = "Amit" + " " + "Kumar" + 30 + 40;`

`var temp1 = 30 + 40 + "Amit" + " " + "Kumar";`

在上面的示例中，变量 `temp1` 将存储值 `"70Amit Kumar"`，而变量 `temp` 将存储 `"Amit Kumar3040"`。看起来相似的表达式产生了不同的结果？让我们看看 JavaScript 如何从左到右处理上述两个表达式。在第一种情况下，当我们遇到字符串时，它将所有剩余内容都视为字符串本身。因此，30 和 40 变成了两个独立的字符串。但在第二个示例中，由于数字是先写的，它会将它们相加并与剩余字符串拼接。

在我们深入研究每种 JavaScript 数据类型之前，我必须指出 JavaScript 具有动态类型。让我向你解释这意味着什么。在 C 语言中，我们使用如 `int`、`float`、`char` 等数据类型。这些是静态数据类型，意味着在程序执行期间它们不能接受任何其他类型的值。然而，我们在这里没有看到此类类型。我们只需使用关键字 `var` 声明变量，然后按照我们想要的方式进行变异。即使我们在变量中存储了字符串值，在程序的后续某个点，也可以给它赋值一个数字。因此，JavaScript 的类型在本质上是动态的。例如：

`var rand; //rand 是 undefined`

`var rand="Random"; //rand 存储字符串`

`rand= 70; //现在 rand 存储数字`

现在我们已经看了数据类型的属性，让我们详细查看每种数据类型。

JavaScript 中有两种数据类型：

- a. 原始数据类型 (Primitive data)
- b. 非原始或复杂数据类型 (Non-primitive or complex data)

原始类型是语言内置的预定义数据类型。JavaScript 中五种原始数据类型：

- String（字符串）
- Number（数字）
- Boolean（布尔）
- Null（空）
- Undefined（未定义）

非原始或复杂类型不是默认提供的，而是程序员定义的。例如数组、对象等。

### 字符串 (Strings)

字符串仅仅是一系列字符。它们被单引号或双引号包裹。在它们上进行加法操作只是简单的拼接。

例如：

`var name = "Amit Kumar";`

`var name2='Javed';`

字符串内部的引号没有问题，只要它们与包裹字符串的引号不同。例如：

`var xyz = "It's done";`

`var xyz1 = 'Friends call him "James"';`

### 数字 (Numbers)

与大多数其他编程语言不同，JavaScript 没有整数、浮点数等概念。相反，它只有一个数字概念，数字可能包含也可能不包含小数：

`var x = 74.00; // 小数`

`var y = 33; // 不带小数`

如果数字极大，可以使用科学计数法编写。例如：

`var x = 333e5; // 333000000`

`var y = 23e-5; // 0.00023`

### 布尔 (Booleans)

布尔的概念与其他编程语言几乎相同。布尔值只有两个——`true` 和 `false`。这些值的主要用途出现在形成条件语句时。

```
var a = true;
var b = false;
```

### 空 (Null)

Null 意味着“无”。值 `null` 表示任何对象值的被刻意缺失。可以通过将其设置为 `null` 来清空对象。

```
var name=null; //值 变为 null
```

### 未定义 (Undefined)

未分配任何值的变量将包含 `undefined`。例如：`var abc; // 值是 undefined`

我们也可以给变量赋值 `undefined` 值。

`abc= undefined;`

人们通常会混淆 `null` 和 `undefined`。我将在本章的稍后部分解释它们的区别。

这些是原始类型。现在让我们来看一些非原始数据类型。

### 数组 (Arrays)

数组仅仅是某些值的集合。这些值的集合使用大括号编写。像所有其他编程语言一样，索引从 0 开始。

```
var names[] = { "Ram", "Rahim", "Jaspaal" }; //names[0]="Ram";
```

### 对象 (Objects)

JavaScript 对象以键值对的形式编写。例如：

```javascript
var name = {
  "firstName":"Amit",
  "lastName":"Kumar",
  age:70
};
```

在我结束关于数据类型的讨论之前，我必须解释一个名为 `typeof` 的运算符。由于 JavaScript 是动态类型的，在程序的各个点，我们需要知道变量包含什么类型的数据。我们可以使用 `typeof` 运算符来确定这一点。

### typeof 运算符

正如我之前提到的，`typeof` 运算符用于确定变量所包含的数据类型。

```javascript
typeof "70"; // "string"
typeof 70; // "number"
typeof "Amit"; // "string"
typeof true; // "boolean"
typeof null; // "object"
typeof undefined; // "undefined"
```

### 常数 (Constants)

正如名称所示，常量是那些值不能改变的变量。它们使用 `const` 声明。例如：

`const pi=3.14;`

## 第 8 章 基础运算符

### 什么是运算符？

运算符基本上是充当函数的符号。它们接收输入（操作数）并产生特定的输出。例如在 `5+2` 中，`5` 和 `2` 是操作数，而 `+` 符号是运算符，结果为 `7`。

### 运算符的分类

运算符通常根据它们执行的操作进行分类。像 `typeof`、`instanceof` 等运算符是独特的，因此不能归类在你将读到的类别中。

### 算术运算符 (Arithmetic Operators)

正如名称暗示的，这些是在操作数上执行算术任务的运算符。下面列出了算术运算符。

- 加法 `[+]`: 如果两个操作数都是数字，此运算符对两个操作数执行加法操作；如果两个操作数中的一个或都是字符串类型，则此运算符拼接/连接两个操作数。

示例：`4 + 2` // 结果为 6

`'example' + 5` // 结果为 `"example5"`

`'thisIs' + 'Example'` // 结果为 `"thisIsExample"`

- 减法 `[-]`: 此运算符对两个操作数执行减法操作。示例：`4-2` 结果为 `2`。

- 除法 `[/]`: 此运算符对两个操作数执行除法操作，其中左侧的操作数（被除数）除以右侧的操作数（除数）。示例：`15/3` 结果为 `3`。

- 乘法 `[*]`: 此运算符对两个操作数执行乘法操作。示例：`4*2` 结果为 `8`。

- 取模 `[%]`: 也称为余运算符，此运算符产生两个相除后的余数。示例：`5%2` 结果为 `1`，`5%3` 结果为 `2`。

- 递增 `[++]`: 将其数值操作数的值增加一。此运算符的位置很重要，即它是放置在操作数之前还是之后。如果放在操作数之前，则这种情况被称为前缀（例如 `++x`），在执行增加操作后返回值；如果放在操作数之后，则这种情况被称为后缀（例如 `x++`），在执行增加操作之前返回值。

示例：//假设 x 是 5

`console.log(++x);` // 打印 6

```
//value of x at this point 6

//say y value is 5 console.log(y++ ); //prints 5 NOT 6
//but value of y at this point is 6 so incrementation was done but after the
//expression returned value
```

- 递减 `[--]`: 将其数值操作数的值减 1。与加运算符类似，这里后置和前缀规则同样适用。

示例：//假设 x 的值为 5

`console.log(--x);` //打印 4

// 此时 x 的值为 4

```
//say y value is 5 console.log(y-- ); //prints 5
//此时 y 的值为 4
```

- 幂运算符 `[**]`: 此运算符通过将第一个操作数增加到第二个操作数的幂次来产生结果，即 第一个操作数** 第二个操作数。

示例：`2**3` 产生结果 `8`。

### 赋值运算符

这些运算符用于为变量赋值。值根据右操作数被赋值给左操作数。下面列出了赋值运算符。

- 等于 `[=]`: 此运算符简单地将其右操作数的值赋值给左操作数。示例：`x=5` 将 5 赋值给 `x`，因此现在 `x` 的值为 5。

- 加赋值 `[+=]`: 此运算符将左操作数和右操作数的值相加，并将结果赋值给左操作数。示例：假设 `x = 2` 那么 `x += 3` 会使 `x` 的变为 5。

- 减赋值 `[-=]`: 此运算符从左操作数减去右操作数的值，然后将结果赋值给左操作数。示例：假设 `x = 8` `x -= 3` 会使 `x` 的变为 5。

- 乘赋值 `[*=]`: 此运算符将左右操作数相乘并将结果赋值给左操作数。示例：假设 `x = 5` 那么 `x *= 2` 会使 `x` 的变为 10。

- 除赋值 `[/=]`: 此运算符将左操作数（被除数）除以右操作数（除数），然后将结果赋值给左操作数。示例：假设 `x = 10` `x /= 2` 会使 `x` 的变为 5。

- 取模赋值 `[%=]`: 此运算符将左操作数（被除数）除以右操作数（除数），然后将余数赋值给左操作数。示例：假设 `x = 5` `x %= 2` 会使 `x` 的变为 1。

- 幂赋值 `[**=]`: 此运算符将左操作数的值提高到右操作数的幂，然后将产生的结果赋值给左操作数。示例：假设 `x = 2` `x **= 3` 会使 `x` 的变为 8。

### 其他运算符

这些是无法归入上述类别的运算符。下面列出了此类运算符。

- `typeof` 运算符: 此运算符以字符串格式返回操作数的类型。

示例：

```
typeof 2 //评估结果为 "number"
typeof 1.23 //评估结果为 "number"
typeof "2" //评估结果为 "string"
typeof 'hi' //评估结果为 "string"
typeof true //评估结果为 "boolean"
typeof false //评估结果为 "boolean"
typeof {ob:1} //评估结果为 "object"
typeof new Date() //评估结果为 "object"
typeof Math.cos //评估结果为 "function"
typeof function() {} //评估结果为 "function"
```

- `instanceof` 运算符: 此运算符检查第一个操作数（应该是一个对象）是否属于特定类型，其中要检查的类型由第二个操作数指定。它根据对象类型是否匹配返回 `true` 或 `false`。

示例：`new String("Astring") instanceof String` //评估结果为 `true` `["this", "is", "array"] instanceof Array` //评估结果为 `true` `new String("Astring") instanceof Array` //评估结果为 `false` `["this", "is", "array"] instanceof String` //评估结果为 `false`

- `delete` 运算符: 此运算符从对象中删除属性。示例：

```javascript
var myObject = {
prop1: "test", prop2: "test2"
};  delete myObject.prop1; //删除对象 myObject 的 prop1 属性
```

- `in` 运算符: 此运算符检查指定的属性（第一个操作数）是否存在于指定的对象（第二个操作数）中。它根据属性是否存在于对象中返回 `true` 或 `false`。

示例：

```javascript
var myObject = {
prop1: "test", prop2: "test2"
};
"prop1" in myObject; //评估结果为 true 
"prop45" in myObject; //评估结果为 false
```

本章解释了 JavaScript 中的运算符。希望你发现它是很有用的。

## 第 9 章 JavaScript 中的函数

函数是任何编程语言中不可或缺的一部分。如果没有函数，我们的程序将包含大量的冗余代码。函数帮助我们以高效的方式编写代码，不仅提高了可读性，而且在维护方面提供了极大帮助。让我们探索什么是函数以及为什么需要它！

函数是用于执行特定任务的语句集合。简单来说，你有一个可以执行两个数字相加的函数。因此，在程序的任何时候，如果你需要计算两个数的和，只需要调用这个特定的函数并传递要相加的两个值。该函数将返回所需的值。让我们先看看声明和定义函数的语法，然后我们对其进行详细讨论。

```javascript
function functionName(parameter1, parameter2, parameter3) {
  //要执行的语句集 
}
```

如上所示，函数的定义以关键字 `function` 开始，紧跟着是一个唯一的函数名，然后是括号 `()`。函数应该执行的任务写在大括号 `{ }` 中。每当函数被调用时，大括号内的所有语句都将被执行。如果你注意到上面的语法，括号内有一组用逗号分隔的参数。这些是函数产生所需结果所需要的值。换句话说，这些是在调用函数时必须传递的值。

让我们来看一个简单的函数示例，它接受两个值并返回它们的和。

```javascript
function addTwoNumbers(num1, num2){
  return num1+num2; //计算并返回和 
}
```

必须注意，函数在主程序中被触发或调用之前处于休眠或非活动状态。将这些比作厨房里的面包机。除非你需要它，否则它处于非活动状态。当你需要它时，只需把面包放入并开启。它就会执行通常的操作。函数也是一样。它在被调用时执行。每个函数都应该有自己唯一的名称。这很重要，因为当你调用函数时，不应该出现模糊的情况。

参数在函数内部表现为局部变量。如果你了解其他语言，可能听说过过程（procedure）或子程序（subroutine）。子程序对应 JavaScript 中的函数。

函数在被调用时执行。这可能由于以下场景之一引起：

- 从 JavaScript 程序中调用。
- 自动调用。
- 当某些事件发生时（事件通常指网页上的活动）

每当遇到 `return` 语句，值将返回到调用它的地方。函数中 `return` 语句之后的任何语句都不会被执行。因此，将 `return` 语句放在函数末尾是非常重要的。在某些情况下，我们可能必须将 `return` 放在开头，但那是条件语句的情况下。

让我们来看另一个计算两个数字乘积的示例。这将有助于更好地理解函数调用的概念。

```javascript
function productCalc(num1, num2) {
  return num1 * num2; //计算并返回积
}
var prod = productCalc(5, 6);
```

在上面的示例中，调用了 `productCalc` 函数，返回值存储在变量 `prod` 中。然后你可以根据需要选择使用该值。

现在我们已经看了什么是函数以及如何根据我们的使用它们，让我们看看函数在当今高效编程的世界中是多么重要的。

函数的优点：

- 1. 重用性

函数的主要优势是它可以在整个程序中重用。你可以编写一个执行特定任务的函数，然后在需要执行该任务时只需调用它。例如，如果你必须对某些数字进行排序，你可以写一个执行该操作的函数，无论你需要对数字进行多少排序，只需调用该函数，你的工作就完成了。你避免了重复编写排序代码。

- 2. 可维护性

维护性是指后期对某段代码进行重构的任务。在某个时间点，假设你编写的用于对数字列表排序的代码有一个 bug。现在想象你没有函数的概念。那么基本上在任何你使用了那段有 bug 代码的地方，你都需要搜索它然后修复 bug。然而，有了函数，你只需要看一个地方并修正代码。你不需要访问多个地方。这节省了你大量的时间精力。

- 3. 减少代码长度

有了函数后，你就不需要在每个地方都编写相同的代码。这显著地缩短了代码的长度。

关于函数的几点记忆：

- 1. 你可以使用 `document.getElementById()` 在 HTML 页面的任何地方显示函数的结果。

例如：

```javascript
function add(a,b) {
  return a+b;
}
document.getElementById("result").innerHTML = add(7,14);
```

- 2. 始终使用 `()` 运算符来调用函数。如果漏掉了它，返回的将是函数的整个文本。

在上一个例子中，如果你只是简单地调用 `add` 而不是 `add()`，HTML 将包含整个函数文本。

- 3. 函数可以直接作为变量的值使用。

例如：

```javascript
var x = add(5,7);
var printString = "The result is " + x ; 或者，
var printString="The result is " + add(5,7); 在两种情况下，输出将是相同的。
```

始终记住，如果你编写了一组在程序中重复多次的代码，请为它创建一个函数。此外，函数的长度应该保持尽可能小。

## 第 10 章 理解对象

JavaScript 是基于 OOP（面向对象编程）范式的，因此它中的几乎所有内容都是对象，或者至少表现得像对象，无论是数组、函数还是正则表达式（regex）。对象是 JavaScript 中最基本的构建块。

### 什么是对象？

对象是属性的集合并具有类型。就像在其他编程语言中一样，人们可以通过将其与现实中的物体进行比较来理解对象的概念。以汽车为例，相同的型号可能有不同的颜色，即具有不同的属性，但它们属于同一个类别，即汽车，也就是说它们具有相同的类型。

这里是一个例子，可以更清楚地理解上述描述的对象的概念：

```javascript
function car(color, numberPlate) {
//这就像对象的蓝图，而不是对象本身 this.color = color;
this.numberPlate = numberPlate; //
//创建对象：var car1 = new car("Green", 1234);//它们是相同类型
var car2 = new car("Red", 5678);//但具有不同的属性
console.log(car1);//在控制台上输出 car1 的详情，即 Green 和 1234
console.log(car2);//在控制台上输出 car2 的详情，即 Red 和 5678
}
```

### 访问对象的属性

在 JavaScript 中，你可以通过两种方式访问对象属性，即点符号法和括号表示法。这两种方式的语法如下：

`myObject.propertyName;` //点符号法

`myObject['propertyName'];` //括号表示法

注意，如果对象属性是整数型的，则只能通过括号表示法访问，例如：`myObject.55` //错误

```javascript
myObject['55']; //正确
```

### 在 JavaScript 中创建对象

下面列出了在 JavaScript 中创建对象的方法：

- **对象字面量 (Object Literal):**

这是在 JavaScript 中创建对象最常见且可能最简单的方法。

示例：

```javascript
var myObject = {
objectProperty1: 45, objectProperty2: 'something else', objectMethod:
function() {//使用调用作为对象属性 console.log(this.objectProperty1,
this.objectProperty2)/在控制台上打印对象属性
};myObject.objectMethod();//对对象方法/函数的示例调用 
```

- **'new' 关键字:**

你可以通过使用 `new` 关键字调用对象构造函数（一种用于初始化新对象的函数）来创建对象。

示例：`var myObject = new Object();` //用于初始化新对象的构造函数 `myObject.property1 = 45; myObject.property2 = 'something else';`

`myObject.objectMethod = function() { /* ... */ };` 你也可以定义自己的构造函数来创建新对象；构造函数就像是你对象的蓝图，你可以创建许多对象并确保它们都是相同类型，尽管它们可能具有不同的属性。

自定义构造函数的示例：

```javascript
function students(name, age, class) {
this.name = name; this.age = age; this.class = class
//使用‘new’ 关键字从自定义构造函数创建对象：var
student1 = new student("Sam", 14, 2);//一个名字为 sam 年龄为 17 的学生
var student2 = new student("Joe", 17, 11);//一个年龄为 17 类级为 11的学生
}
```

### 嵌套对象

你可以在对象内部创建一个对象。这可以通过将一个对象赋值给对象的属性来实现。这被称为嵌套。

示例：

```javascript
var student = {
name: "Mark", marks : { //嵌套数学: 80, 英语: 95
}
};
//嵌套对象可以这样被引用：student.marks.maths; //点符号法
student['marks']['maths'] //括号表示法
```

### 'this' 的使用

`this` 关键字在对象内部用于引用对象。这可以通过将一个值赋值给对象的属性来实现。这被称为赋值。

示例：

```javascript
function Constructor(value) {
this.objectProperty = value;//赋值
console.log(this.objectProperty); //访问属性
}
```

### 删除对象的属性

正如第 5 章所学的，我们可以使用 `delete` 运算符删除对象的属性。要从对象中删除属性，你必须编写 `delete` 运算符，后跟对象及其属性。

示例：

```javascript
var student = {
name:'Joe', age: 16
}; console.log(student.age);//16
delete student.age;//删除属性 console.log( student.age ); //给出‘undefined’
```

### 遍历对象的属性

你可以通过 `for-in` 循环遍历对象的属性。

示例：

```javascript
var carList = {
car1: 'Mustang', car2: 'Beetle', car3: 'Viper'
}; //遍历对象的属性：for(var property in carList) {
console.log( property ); //输出 Mustang, Beetle, Viper }
```

遍历对象的属性另一种方法是使用 `Object` 类的 `keys()` 方法获取键数组，并遍历该数组以访问对象的属性。

示例：//使用上面相同的对象

```javascript
for (const propertyName of Object.keys(carList)) {
console.log(carList[propertyName]); }
```

你已经学习了如何在 JavaScript 中操作对象。我希望这一章对你有帮助！

## 第 11 章 变量的作用域

变量在 JavaScript 中创建是作为存储数据的容器。与 C/C++ 等其他编译语言中强制要求显式定义要存储的数据类型不同，JavaScript 没有这种划分，并使用相同的构造函数 `var` 存储字符串、整数、浮点整数、布尔值等每类型的数据。

```javascript
var x=2;
var y=0.04; z='A';
```

所有这些变量都有作用域和生命周期，即它们所包含的值有效的时间。

### 范围

首先，我们来谈谈变量范围。JavaScript 有两种范围：

- 全局范围 (Global)
- 局部范围 (Local)

如果我们说一个变量具有全局范围，意味着该变量可以在整个脚本中使用，即脚本内所有函数中都可以。它可以在任何地方被访问和修改。而对于具有局部范围的变量，它只能在定义的函数内部被访问或修改。

在函数内部声明的变量是局部变量。它只在函数执行时被创建，在函数运行期间一直存在，然后自动销毁。变量无法在函数外部的任何地方被访问。

```javascript
var myVar= "Something"; myFunctionFunc(){
var myVar= "Another thing"; }
```

如所示，我们可以拥有同名的局部变量和全局变量。区别在于它们被调用的位置。

例如，如果在函数内部打印变量 `myVar` 的值，我们会在屏幕上看到 `"Another thing"`。另一方面，如果我们尝试在函数外部打印 `myVar` 的值，我们会在显示器上看到 `"Something"`。所以我们可以看到，完全是变量的位置决定了它是局部变量还是全局变量。

当 JavaScript 开始执行一个函数时，它会首先查找函数内部的所有变量声明，例如 `var foo`。然后它会创建所有初始值为 `undefined` 的变量。如果变量在函数内部声明时带有某个值，它仍然会被初始化为 `undefined`。然后，JavaScript 开始逐行执行当前语句。当到达变量声明所在的行时，它会将该值赋予变量，从而移除 `undefined` 标签。

示例：`var something=100; foo();`

```javascript
function foo(){
console.log(something); if(false) var something=112; }
```

这里的 `console.log` 将打印 `undefined`。原因是当函数执行时，该 `if` 语句内部声明的变量被提取且其值被设置为 `undefined`。然后执行该 `console.log` 语句。

如果没有那个 `if` 语句，我们会在控制台得到 100。

### 闭包

在 JavaScript 中，嵌套函数存储了与函数相同作用域声明的变量引用。这组引用被称为闭包 (Closures)。

示例：

```javascript
function foo(name){
return function(){
  bar(name);
}
}
function bar(name){
  console.log("Hello"+name);
}
```

当使用类似 `foo("John")` 的参数调用函数时，控制台将显示 Hello John。

这是如何发生的？再次过一遍这段代码片段。`foo()` 调用了函数 `bar()`，该函数的签名带有一个参数。当 `foo()` 被调用时，内部嵌套函数获取了 `foo()` 参数的引用，在这种情况下是 `"John"`。这种嵌套函数 `bar()` 获取的对变量的引用在 JavaScript 中就是闭包。这就是闭包的工作原理。

## ES6 规范

ECMA script 是 JavaScript 的超类，并充当该语言的标准。JavaScript 在 2015 版本的脚本中添加了新功能，包括引入了块级作用域变量 `let` 和 `const`。对于这些变量，`{..}` 定义了一个新的作用域。当这些变量被初始化时，它们只会影响它们定义所在的作用域。

示例：

```javascript
let a=2;
const b=3; {
let a=3;
console.log(a); }
console.log(a);
```

这两个 `console.log()` 语句将打印不同的值。原因是两个变量 `a` 是定义在不同作用域中的。

## 结论

JavaScript 变量是最容易处理的，因为它们不涉及像编译语言那样的类型设置，因此被称为弱类型 (weakly-typed)。它为我们提供了许多可以使用的功能。这种语言不断增强，自 2015 年以来添加了 `let` 和 `const` 变量，让 JavaScript 程序员的生活变得更加简单和有趣。

## 第 12 章 在 JavaScript 中处理数字

大多数编程工作都涉及数字处理。无论是处理银行账户余额，还是向其他用户发送加密消息，或者几乎任何其他内容，你将执行算术运算、尝试寻找平方根等，或者寻找随机数使用。JavaScript 让这些任务比许多其他语言简单得多，而且这些操作中的大部分都非常直观。

### JavaScript 如何存储数字

在我们开始学习如何处理数字之前，有必要学习 JavaScript 确切是如何看待它们的。JavaScript (JS) 将所有数字存储为浮点数 (floating point numbers)——也就是说所有数字都可以带有小数点。与 C 风格语言不同，整数没有单独的类型。所有数字都存储在 `Number` 类型中。你可以如下所示存储数字：`var x = 12; var y = 2.66; var z = 312e-2;` 最后一个例子是指数计数法的用。在这种情况下，`z` 等于 3.12。在很多情况下，如果你有一个字符串中的数字，JS 会尝试将其转换为数字以进行数值计算。例如 `var num = "1234";` 如果你尝试在数值运算中使用 `num`，它会被视为 1234。然而，在加法期间有一个非常重要的特殊情况，我们很快就会看到。

算术运算首先，让我们看看如何执行基础算术运算。这些包括加法、减法、乘法和除法。执行方式如下：`var x = 12 + 24;` `x` 现在将存储值 36。

```javascript
var x = 24 / 2; // x 现在将存储值 12.
var x = 3 - 2; // x 将存储值 1.
var x = 4 * 9; // x 将存储值 36.
```

注意，除了加法运算符 `+` 之外，所有这些操作使用字符串作为数字也可以工作。让我们来看几个语句：`var x = 24 / "2"; var y = "3" * "4"; var z = "12" + 3; var n = 36 / "Mike";` 第一个将如预期的得到 12，下一个也是如此。但 `z` 将持有值 `"123"` 而不是 15。这是因为 `+` 运算符执行的是拼接 (concatenation)——它正在将字符串连接。在这种情况下，JS 将 3 转换为 `"3"` 然后将两个字符串相加得到 `"123"`。每当你添加任何可能是字符串的内容时，都必须记住这一点！

最后一个也很有趣。这个问题没有明显的答案—— 36 不能除以 Mike。JS 用 `NaN` 的值填充 `n`——它是 Not a Number（不是数字）的缩写。每当你执行一个无法产生数字的数值计算时，你都会得到 `NaN` 作为结果。如果你想检查一个变量是否为 `NaN`，你可以这样做：`isNaN(n);` 这将返回 `true`！你也可以自己给变量填充 `NaN`。同样，当你执行一个导致无穷大的计算时，JS 将返回值 `Infinity`。

`var p = 12 / 0;` 变量 `p` 将具有值 `Infinity`。`Infinity` 不是字符串 `"Infinity"`，而是一个值。

### 使用内置函数

对于简单的事情，例如将数字保留到特定的小位数，或将其转换为字符串，JS 有内置函数。这些函数大部分通过语法 `object.method(arguments);` 使用。要将数字转换为字符串，你可以使用 `toString()` 方法：`var x = 25; var x_in_string = x.toString();` `x_in_string` 将等于 `"25"`。`toExponential(n)` 方法以科学计数法写出数字，小数点后有 `n` 位数字。参数 `n` 是可选的，你可以用任何数字替换它。

`var x = 25.3221; var x_in_exponents = x.toExponential(3);` `x_in_exponents` 将是 `"25.321e0"`。注意输出是一个字符串。如果你不带参数调用 `toExponential`，它将完全不对其进行舍入。`toFixed(n)` 方法的作用是输出带有特定小数位的数字。

`var x = 25.1168; var x_to_2 = x.toFixed(2);` `x_to_2` 将是 `"25.12"`。注意它对数字进行了舍入。通常你需要将字符串转换为数字。这在我们上面看到的尝试将字符串和数字相加的情况下特别有用。为了防止拼接，你应该使用 `Number()` 函数。该函数的使用方式不同：`var x = "25.12"; var y = Number(x);` 现在 `y` 将拥有值 25。你还可以使用另外两个函数：`parseInt()` 和 `parseFloat()`。这两个函数获取字符串中的第一个数字并分别返回舍入后的结果。

`var x = "10.2 20 30"; var y = parseInt(x); var z = parseFloat(x);` `y` 将是 10，而 `z` 将是 10.2。如果无法转换数字，这些函数都将返回 `NaN`。

### Math 函数

算术运算符并不能涵盖你对数字的所有操作。要执行如求平方根或数字的绝对值等操作，你必须使用 Math 函数。这些函数的通用语法为 `Math.method(argument)`。

第一组函数是 `Math.round()`、`Math.ceil()` 和 `Math.floor()`。`Math.round()` 函数将数字四舍五入为整数。如果小数点后的第一位数字大于或等于 5，则向上舍入到下一个整数；如果小于 5，则向下舍入到上一个整数。`ceil` 函数与之相似，但总是将数字向上取整到下一个整数，而 `floor` 函数总是将其向下取整到上一个整数。

```
var x = 25.52;
var y = 25.19;

var xRound = Math.round(x); var yRound = Math.round(y); var xCeil = Math.ceil(x); var yCeil = Math.ceil(y); var xFloor = Math.floor(x); var yFloor = Math.floor(y); xRound 将为 26，yRound 将为 25。xCeil 和 yCeil 都将为 26，xFloor 和 yFloor 将为 25。Math.pow() 函数可用于计算一个数字的另一个数字的幂。例如：var x = Math.pow(2,10); x 将为 1024。求平方根（即 ½ 次幂）是一个非常常见的操作，你可以使用 Math.sqrt(x) 来执行它：var x = Math.sqrt(9); 此时 x 将为 3。Math.abs() 函数返回传递给它的数字的绝对值。
```

`var x = Math.abs(-2);` `x` 将为 2。`Math.min()` 和 `Math.max()` 函数可以用于找到给定的数字列表的最小值和最大值。它们可以接受任意数量的参数。

```
var maximum = Math.max(10,12,14,3,7,1,3); var minimum = Math.min(10,12,14,3,7,1,3); maximum 将取值 14，minimum 将取值 1。math 库还包含三角函数的内置函数 sin、cos 和 tan 以及它们的反函数。这些函数分别是 Math.sin()、Math.cos()、Math.tan()、Math.asin()、Math.acos()、Math.atan()。所有这些函数都以弧度运行，因此你应该将任何角度的角度转换为弧度后再使用。
```

`var sinpi = Math.sin(Math.PI);` `sinpi` 将取值 0。最后，`Math.log()` 函数允许你找到数字的自然对数。

```
var logten = Math.log(10);
```

`logten` 将取值 2.302。JS 在 Math 库中也有几个数学常数，例如 Pi 和 E。

### 随机数

对于加密和视频游戏等情况，随机数非常重要。要生成随机数，你可以使用 `Math.random()` 函数。`Math.random()` 函数返回 0 到 1 之间的随机数，包含 0 但不包含 1。

```
var n = Math.random(); n 每次都会取一个不同的值。在需要两个数字 a 和 b 之间的随机数的情况下，可以使用以下代码：randn = a + (Math.random() * (a-b)); 这将始终给你一个 a 和 b 之间的数字。要获取 a 和 b 之间的整数，可以使用我们上面看到的 floor、ceil 或 round 函数。
```

## 第 13 章 在 JavaScript 中处理字符串

字符串是一组字符。它存储了一系列字符。如前面的章节所述，我们使用单引号或双引号来存储字符串。例如：`var name="Amit";` //双引号 或者，

```
var name= 'Amit'; //单引号
```

如果字符串本身包含单引号或双引号怎么办？例如：`desc= "He is referred as the "Don" among his colleagues';` //错误 或者

```javascript
var desc = 'It's alright'; //错误
```

在这些情况下，我们利用转义字符（ `\` ）来以正确的方式界定我们的字符串。转义字符告诉编译器后面跟着特殊字符。让我们通过一个例子来更好地理解这一点。

```
var desc= "He is referred to as the \"Don\" among his colleagues";
```

或者，

```javascript
var desc = 'It\'s alright';
```

有时我们也可以使用简单的方法。如果字符串包含双引号，则用单引号包裹整个字符串；如果字符串包含单引号，则用双引号包裹整个字符串。例如：`var answer = "It's alright"; var desc= 'He is referred to the "Don" among his colleagues';` 转义字符也可以用于其他特殊字符，如反斜杠 (`\`)、退格符 (`\b`)、回车 (`\r`) 等。

每个字符串都有一个名为 `length` 的内置属性，可以用于知道字符串的长度。例如：`var textRand = "INDIA"; var len=textRand.length;` //`len` 将存储 5

有时字符串可能会比通常长。在这些情况下，字符串可能无法单行显示。这通常会导致混乱。为了防止这产生混乱并引起问题，我们将字符串分为两部分，然后使用它进行连接。

有许多与字符串相关的方法和各种属性，使得字符串的操作变得简单。让我们逐一查看。

### 1. Length 属性

每个字符串都有一个相关的 `length` 属性。它返回字符串字符的数量。

例如：`var randText="ABC DEF GHI"; var len=randText.length;` //`len` 将包含 11

### 2. indexOf 方法

该方法返回指定文本在字符串中第一次出现的位置（索引）。如果未找到指定的字符串，则返回 -1。索引从 0 开始。

例如：`var text = "My name is Amit"; var ind = text.indexOf("Amit");` //将返回 11，因为 Amit 存在于位置 11

### 3. lastIndexOf 方法

该方法返回给定文本在字符串中最后一次出现的位置（索引）。如果未找到指定的字符串，则返回 -1。

```
var text = "Our own planet earth is a great planet"; var n = str.lastIndexOf("planet"); //这将返回 31，因为 planet 的最后一次出现是在 31
```

注意：上述两种方法也接受第二个参数，该参数是搜索开始的位置。

```javascript
var text = "My name is Amit"; var ind = text.indexOf("Amit",2); // 在这种情况下，搜索从索引 2 开始
```

### 4. search 方法

`search` 方法的行为与 `indexOf()` 方法完全相同。然而，它不接受任何第二个参数。因此，在这种情况下，搜索在所有情况下都从索引 0 开始。这用于使用正则表达式搜索字符串模式。

### 5. slice 方法

`slice()` 方法接受两个参数——start（开始）和 end（结束）。正如名称所示，`slice` 返回从开始索引到结束索引的字符串。

例如：`var country = "India, Bahama, Fiji";`

```javascript
var res = country.slice(7, 13); //这将返回 Bahama // 如果省略第二个参数，字符串的剩余部分将被切掉。
```

```javascript
// 如果索引为负数，则从末尾计数
```

### 6. substring() 方法

`substring()` 方法与 `slice()` 相似，不同之处 `substring()` 不接受负索引。

```javascript
var country = "India, Bahama, Fiji"; var res = country.substring(7, 13);
```

```javascript
// 这将返回 Bahama
```

```javascript
// 如果省略第二个参数，字符串的剩余部分将被截断。
```

### 7. substr() 方法

该方法再次与 `slice()` 相似，不同之处该方法接受的两个参数是起始索引和提取部分的长度。例如：

```javascript
var country = "India, Bahama, Fiji";
var res = country.substr(7, 13);
```

```javascript
// 这将返回 Bahama
```

```javascript
// 如果省略第二个参数，字符串的剩余部分将被截断。
```

### 8. replace() 方法

该方法的工作方式与“查找并替换”完全相同。它将字符串中的给定值替换为另一个值，这两个值都必须作为参数传递。

```javascript
name = "My name is Amit";
var n = name.replace("Amit", "Amitabh");
```

然而，需要注意的是，原始字符串不受影响。返回的是一个新的字符串。默认情况下，它只替换字符串中的第一个匹配项。

为了替换字符串中的所有匹配项，我们使用带有 `/g` 标志的正则表达式，这意味着替换所有全局匹配项。

```javascript
name = "My name is Amit and Amit";
```

```javascript
var n = name.replace("/Amit/g", "Amitabh");
```

`replace` 函数默认对大小写敏感。要使其不区分大小写，我们使用 `/i`。例如：

```javascript
name = "My name is Amit and Amit";
var n = name.replace("/Amit/i", "Amitabh");
```

### 9. toUpperCase() 方法

不需要猜！此函数将字符串转换为大写。例如：

```javascript
var text1 = "Amit"; var text2 = text1.toUpperCase(); // 返回 AMIT
```

### 10. toLowerCase() 方法

不需要猜！此函数将字符串转换为小写。例如：

```javascript
var text1 = "Amit"; var text2 = text1.toLowerCase(); // 返回 amit
```

### 11. concat() 方法

该方法用于连接两个字符串。

例如：`var text1 = "Name is"; var text2 = "Amit"; var text3 = text1.concat(" ", text2);` //结果将为 `"Name is Amit"`

### 12. charAt() 方法

该方法用于从指定位置提取一个字符。例如：`var name="Amitabh"; name.charAt(1);` // 这将返回 `"m"`

### 13. charCodeAt() 方法

该方法用于确定指定位置字符的 Unicode 编码。例如：`var name = "Himalaya"; name.charCodeAt(0);` // 返回 72

坦率地说，在 JavaScript 中我们处理得最多就是字符串。因此，有必要从核心上理解它。大多数时候你都会遇到字符串，因此要理解它的实际用途。与字符串相关的方法可以被视为应该根据需要使用的“武器”。JavaScript 字符串还有许多其他方法，你可以在网上搜索它们。

## 第 14 章 在 JavaScript 中处理日期和时间

日期和时间操作是 JavaScript 的重要部分，作为一名开发者，你将面临日期和时间起至关作用的情况。

### 'Date' 对象

在 JavaScript 中，我们使用内置的 `Date` 对象来处理日期和时间；它提供了许多实用的函数用于高效的日期和时间操作。

### 初始化 'Date' 对象

你可以借助 JavaScript 中的 `new` 操作符来初始化一个新的日期对象。你可以用四种格式来初始化日期对象，列如下：

- `new Date()`
  当不带任何参数初始化时，日期对象指向当前的日期和时间。

  示例：`var example = new Date(); console.log( example );` // 显示当前日期和时间。生成的日期和时间相对于运行代码的系统本地时区。

- `new Date(milliseconds)`
  当使用单个参数（整数）初始化时，该整数被视为毫秒（1 秒等于 10³ 毫秒），由此形成的日期对象指向在 1970 年 1 月 1 日 UTC+0 加上指定的毫秒数后的日期和时间。自 1970 年 1 月 1 日 UTC+0 经过的毫秒被称为时间戳。

  示例：`var example = new Date (24 * 3600 * 1000);` // 加上一天 `console.log( example );` // Fri Jan 02 1970 ...

- `new Date(datestring)`
  如果使用单个参数（字符串）初始化日期对象，它被视为日期字符串（你将在本章稍后部分学习有效日期字符串），由此创建的日期对象指向日期字符串中指定的日期和时间。

  示例：`var date = new Date("2017-01-26"); alert(date);` // Thu Jan 26

- `new Date(year, month [,date, hours, minutes, seconds])`
  如果使用多个参数初始化日期对象，则它们分别被视为年、月、日、小时、分钟和秒。其中年、月是必需的，其余参数是可选的。

  示例：`var date = new Date(2017, 0, 26); alert(date);` // Thu Jan 26

### 有效日期字符串

日期字符串有特定的格式，以下是日期字符串的有效格式：

- `YYYY-MM-DD`
  这是 ISO 格式，表示日期
  示例：`"2017-07-17"`

- `YYYY-MM`
  这是 ISO 格式，表示月份
  示例：`"2017-07"`

- `YYYY`
  这是 ISO 格式，表示年份
  示例：`"2017"`

- `MM-DD-YYYY`
  这是 ISO 格式，表示日期
  示例：`"07-17-2017"`

- `MM-YYYY`
  这是 ISO 格式，表示月份
  示例：`"07-2017"`

- `DD-YYYY`
  这是 ISO 格式，表示年份
  示例：`"17-2017"`

- `MM/DD/YYYY`
  这是 ISO 格式，表示日期
  示例：`"07/17/2017"`

- `MM/YYYY`
  这是 ISO 格式，表示月份
  示例：`"07/2017"`

- `DD/YYYY`
  这是 ISO 格式，表示年份
  示例：`"17/2017"`

- `YYYY/MM/DD`
  这是 ISO 格式，表示日期
  示例：`"2017/07/17"`

- `YYYY/MM`
  这是 ISO 格式，表示月份
  示例：`"2017/07"`

- `YYYY/DD`
  这是 ISO 格式，表示日期
  示例：`"2017/17"`

### 从日期对象获取组件

你可以使用日期对象提供的方法来访问特定组件（年、日等）。

- `getFullYear()`
  该方法返回四位年份。
  示例：`var date = new Date("2017-07-17");` // 2017

- `getDate()`
  该方法返回月份数字。可能值范围为 1–31。
  示例：`var date = new Date("2017-07-17");` // 17

- `getMonth()`
  该方法返回月份。请注意，此方法返回 0–11 而不是 1–12，其中 0 代表第一个月。
  示例：`var date = new Date("2017-07-17");` // 6

- `getDay()`
  该方法返回星期几的整数。
  示例：`var date = new Date("2017-07-17");` // 1 代表周一

- `getHours()`
  该方法返回一天的小时整数，可能值范围为 0–23。
  示例：`var date = new Date("2017-07-17T10:21:35Z");` // 10

- `getMinutes()`
  该方法返回小时的分钟整数，可能值范围为 0–59。
  示例：`var date = new Date("2017-07-17T10:21:35Z");` // 21

- `getSeconds()`
  该方法返回分钟的秒整数，可能值范围为 0–59。
  示例：`var date = new Date("2017-07-17T10:21:35Z");` // 35

- `getTime()`
  该方法返回自 1970 年 1 月 1 日起过的毫秒数表示日期和时间。
  示例：`var date = new Date("2017-07-17T10:21:35Z");` // 1500169295000

```javascript
console.log( myDate.getTime() ); // 1500286895000
```

注意，上述方法返回的是相对于本地时区的日期分量。如果你想获取相对于 UTC（世界标准时间）的数据，只需在上述方法的“get”部分之后添加“UTC” 单词即可，例如，将 `getHours()` 变为 `getUTCHours()`。

### 设置 Date 对象的分量

`Date` 对象也为我们提供了设置日期分量的功能！通常，这些方法的名称以“set” 开头。以下是这些方法：

- `setFullYear(year [, month, date])`
  此方法用于将日期设置为特定日期，该方法中的第一个参数是强制性的。

  示例：`var myDate = new Date(); myDate.setFullYear(2017, 6, 17);`

- `setMonth(month [, date])`
  此方法用于将日期设置为年份中的某个月份；我们也可以设置月份中的日期，这是可选的。整数 0 代表第一个月份（即 1 月），11 代表最后一个月份。
  示例：`var myDate = new Date(); myDate.setMonth(6);` // 将月份设置为 7 月

- `setDate(date)`
  此方法用于设置月份中的日期，其中 1 代表月份的第一天。
  示例：`var myDate = new Date(); myDate.setDate(17);`

- `setHours(hour [, min, ms])`
  此方法用于设置日期对象的时间，该方法中的第一个参数是强制性的。
  示例：`var myDate = new Date(); myDate.setHours(11);`

- `setMinutes(min [, sec, ms])`
  此方法用于设置小时的分钟，你也可以通过此方法设置秒和毫秒，但它们是可选的。
  示例：`var myDate = new Date(); myDate.setMinutes(20);`

- `setSeconds(sec [, ms])`
  此方法用于设置分钟的秒，你也可以通过此方法设置毫秒，但它是可选的。
  示例：`var myDate = new Date(); myDate.setSeconds(58);`

- `setMilliseconds(ms)`
  此方法用于设置秒的毫秒。
  示例：`var myDate = new Date(); myDate.setMilliseconds(123);`

- `setTime(milliseconds)`
  此方法用于将日期和时间设置为时间戳格式，即自 1970 年 1 月 1 日以来的毫秒数。
  示例：`var myDate = new Date(); myDate.setTime(1500286895000);` // 2017-07-17T10:21:35Z

请注意，上述方法设置的是相对于本地时区的分量。如果你想获取相对于 UTC 的，只需在上述方法的“set”部分之后添加“UTC” 单词，例如 `setMinutes()` 变为 `setUTCMinutes()`。

### Date.now() 方法

如果你想获取自 1970 年 1 月 1 日以来经过的毫秒数作为当前时间，你不需要创建一个新的日期对象并在其上使用 `getTime()` 方法。你可以通过 `Date.now()` 方法来实现。
示例：`console.log( Date.now() );` // 输出自 1970 年 1 月 1 日以来经过的毫秒当前时间

### Date.parse() 方法

此方法解析作为参数传递的日期字符串，并将其返回为自 1970 年 1 月 1 日以来经过的毫秒数，即时间戳。日期字符串必须是有效格式。日期字符串的有效格式在本章之前已经解释过。
示例：`var example = Date.parse("2017-07-17T10:21:35Z");` // 1500286895000

## 鼠标事件

当系统检测到指针设备在绑定了监听器的元素之上的位置/状态发生变化时，就会触发鼠标事件。

- 1) `mouseenter` - 当鼠标移动到任何绑定了监听器的元素上时，会触发此事件。它的工作方式类似于 CSS 中的 `:hover` 伪类。
  例如：`<a href="#" onmouseover=someFunc()> 元素 </a>`
- 2) `mouseover` - 当指针设备移动到绑定了监听器的元素或其任何一个子元素时，会触发此事件。
- 3) `mouseup`/`mousedown` - 当鼠标在元素上按下时触发 `mousedown` 事件，当鼠标在元素上释放时触发 `mouseup` 事件。
- 4) `click` - 当鼠标按钮（右键或左键）在元素上按下并释放时，会触发此事件。
- 5) `dblclick` - 当在元素上点击两次鼠标按钮（任意）时，会触发此事件。
- 6) `wheel` - 当鼠标滚轮按钮向任何方向旋转时，会触发此事件。
- 7) `mouseleave` - 当鼠标离开绑定了监听器的元素时，会触发此事件。

## 键盘事件

这些事件是在系统检测到键盘按键状态变化时触发的。

- 1) `keydown` - 当按下键盘上的任何按键时，会触发此事件。
- 2) `keypress` - 当按下键盘上的除 Fn 等特殊键以外的任何按键时，会触发此事件。
- 3) `keyup` - 当释放键盘上的任何按键时，会触发此事件。

## 浏览器事件

这些事件是在系统检测到浏览器相关页面状态变化时触发的。

- 1) `error` - 当资源加载失败时，会触发此事件。
- 2) `abort` - 当资源加载被取消时，会触发此事件。
- 3) `load` - 当资源加载完成时，会触发此事件。
- 4) `complete` - 当整个页面（及其所有资源）加载完成时，会触发此事件。
- 5) `beforeunload` - 在页面准备卸载之前，会触发此事件。
- 6) `unload` - 当页面被卸载时，会触发此事件。

## 表单事件

这些事件是与表单操作相关的。

- 1) `reset` - 当表单被重置时，会触发此事件。
- 2) `submit` - 当表单被提交时，会触发此事件。
- 3) `change` - 当表单元素的值发生改变并失去焦点时，会触发此事件。
- 4) `blur` - 当元素失去焦点时，会触发此事件。
- 5) `focus` - 当元素获得焦点时，会触发此事件。
- 6) `input` - 当元素的内容值发生变化时，会触发此事件。

## 媒体事件

这些事件是与媒体（如音视频）相关的。

- 1) `play` - 当媒体播放开始时，会触发此事件。
- 2) `pause` - 当媒体播放暂停时，会触发此事件。
- 3) `loadedmetadata` - 当媒体元数据加载完成时，会触发此事件。

## 动画事件

这些事件是与 CSS 动画相关的。

- 1) `animationstart` - 当动画开始时，会触发此事件。
- 2) `animationend` - 当动画结束时，会触发此事件。
- 3) `animationiteration` - 当动画每循环一次时，会触发此事件。

## 过渡事件

这些事件是与 CSS 过渡相关的。

- 1) `transitionstart` - 当过渡开始时，会触发此事件。
- 2) `transitioncancel` - 当过渡被取消时，会触发此事件。
- 3) `transitionend` - 当过渡完成时，会触发此事件。

