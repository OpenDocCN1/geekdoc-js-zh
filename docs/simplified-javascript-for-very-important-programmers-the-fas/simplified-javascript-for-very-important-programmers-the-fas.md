
# 针对重要程序员的简易 JavaScript：快速掌握核心 JavaScript 概念

[content]

创建 `Date` 对象 . . . . . . . . . . . . . . . . . . . . . . . . . . . . 212

获取日期和时间组件 . . . . . . . . . . . . . . . . . . . . . . 214

设置日期和时间组件 . . . . . . . . . . . . . . . . . . . . . . 216

格式化日期和时间 . . . . . . . . . . . . . . . . . . . . . . . . . . . 216

**结语** . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 219

## 前言

《针对重要程序员的简易 JavaScript》是一本为想要掌握 JavaScript 所有核心方面面的初学者提供的令人目一新且实用的指南。在书中，我提供了一种简化的 JavaScript 学习方法，通过贴近生活的实例让这些概念变得易理解，即使对于没有编程经验的人也是如此。

我将本书分为两个部分。第一部分为所有学习 JavaScript 的人设计；第二部分侧重于在 Web 上使用 JavaScript，并在第一部分涵盖的基础概念基础上进行。

我用清晰简洁的语言编写了所有内容，让每个人都能跟随并掌握。无论你是学生、企业家，还是仅仅对编程感兴趣的人，这本书都将引导你从轻松、高效地掌握 JavaScript 的核心概念。

从变量、运算符到循环、函数和对象，我们将涵盖成为一名胜任的 JavaScript 程序员所需要的所有知识。书中的示例和练习旨在强化你的学习效果，并帮助你在现实场景中应用这些知识。

如果你正在寻找一种实用且有趣的方式来学习 JavaScript，那么你读到一本完美的书了。

## 什么是 JavaScript？它是如何工作的？

JavaScript 是一种编程语言，最初开发用于为网站添加动态和交互元素。今天，它是世界上最流行的编程语言之一，广泛用于各种领域，包括 Web 开发、移动应用开发、服务器端脚本、机器学习、游戏开发等。在学习 Web 开发时，理解 JavaScript 是如何工作的以及你如何使用它来构建动态网站并为网页添加交互性至关重要。

JavaScript 是一种动态类型语言，这意味着你可以用它存储不同类型的信息，而无需提前告诉计算机你将在那里放置什么。由于你不需要跟踪这么多规则，因此阅读和编写 JavaScript 通常比 C++、Java 或 Rust 等其他编程语言更容易。然而，这也意味着你可能会犯难以发现的错误，因此在编写 JavaScript 代码时要小心。

JavaScript 经常与 HTML 和 CSS 结合使用以创建交互式和动态网站。它的主要特性之一是能够操作并与网页进行交互；它可以更改网页的内容和布局，响应用户输入，并与服务器通信以检索和更新数据。因此，虽然 HTML 提供了网页的结构和内容，CSS 定义了其样式和布局，但 JavaScript 增加了行为和交互性。

## JavaScript 是如何工作的？

当运行 JavaScript 程序时，计算机会读取代码并按照其指令执行。

在 Web 开发中，JavaScript 通常运行在 Google Chrome 或 Mozilla Firefox 等网络浏览器中。当你打开一个包含 JavaScript 的网页时，你的浏览器会读取 JavaScript 代码并利用它来交互和修改网页的内容、布局和行为。

你也可以在其他场景下使用 JavaScript，例如移动应用开发和服务器端编程，在这种情况下，JavaScript 代码运行在不同类型的设备或平台上，但执行代码的过程是相似的。

需要注意的是，JavaScript 是一种**解释型语言**，意味着它在运行之前不需要编译（翻译成机器码）。相反，计算机在执行时解释代码。这使得编写和调试 JavaScript 程序变得更容易，但也可能让它们的运行速度比用编译语言编写的程序慢。

## JavaScript 的历史

JavaScript 由 Brendan Eich 于 1995 年创建，并随着当时流行的网络浏览器 Netscape Navigator 2.0 发布而首次引入。JavaScript 最初被称为 Mocha，后来更命名为 LiveScript，最后改为 JavaScript，以试图利用 Java 编程语言的热度。

JavaScript 迅速在 Web 开发者之间流行起来，并受到了 Internet Explorer 和 Safari 等其他主流浏览器的支持。1996 年，JavaScript 被欧洲计算机厂商协会（ECMA）标准化为 ECMAScript，这仍然是它今天的官方名称。

## JavaScript 与 HTML/CSS 的区别

JavaScript 经常与 HTML 和 CSS 一起构建网站。然而，这三种语言之间存在一些重要的区别。一个关键区别是 JavaScript 是一种编程语言，而 HTML 是一种标记语言，CSS 是描述网页外观的样式表。因此，你会经常发现 JavaScript 比 HTML 和 CSS 更难学习。

JavaScript 中不具备的一些关键特性包括：

- 根据条件或事件执行代码的能力
- 遍历数据并在多个元素上执行操作的能力
- 创建操作不同类型数据的能力
- 向服务器发送请求并检索数据的能力

虽然 HTML 和 CSS 对于定义网页的内容和外观很重要，但如果没有 JavaScript，很难为网页添加让用户喜欢的交互性。JavaScript 允许开发者构建更复杂、更吸引人的用户体验，它是现代 Web 开发的关键组成部分。

## JavaScript 在多领域的应用

除了 Web 开发，你还可以将 JavaScript 用于广泛的应用，包括：

### 服务器端编程

当你访问网站时，你的浏览器会向网站服务器发送请求，服务器执行负责处理该请求并生成相应响应的代码。`Node.js` 和 `Deno` 等工具使得在服务器上运行 JavaScript 成为可能。这让开发者能够构建可以处理许多并发用户的可扩展、高性能应用程序。

### 移动应用开发

你可以使用 `Cordova`、`React Native` 和 `NativeScript` 等工具使用 JavaScript 构建跨平台移动应用。这些工具允许开发者编写 JavaScript 代码，这些代码会被编译并运行在移动设备而非浏览器中。

### 游戏开发

你还可以使用 `Phaser` 和 `Babylon.js` 等工具构建基于浏览的游戏。这些工具允许你创建可以在网页浏览器中运行 2D 和 3D 游戏。

### 数据可视化

`D3.js` 和 `Highcharts` 等 JavaScript 库可以为网站和应用程序创建交互式数据可视化。

### 机器人

你可以使用 `NodeBots` 和 `Johnny-Five` 等平台使用 JavaScript 控制和编写机器人。

### 物联网 (IoT)

JavaScript 可用于构建交互并控制联网设备（如智能家居和传感器）。

### 机器学习

通过 `TensorFlow.js` 和 `Brain.js` 等 JavaScript 库，你可以构建机器学习模型并将其纳入 Web 应用程序。

## 如何编写和运行 JavaScript 代码

学习 JavaScript 的最好方法是编写。让我们探索编写和运行 JavaScript 代码的不同方式，以便你轻松练习所学的任何内容。

### 使用网络浏览器

编写 JavaScript 代码最简单、最易获取的方法之一是使用网络浏览器。大多数现代浏览器（如 Google Chrome、Mozilla Firefox 和 Safari）都内置了 JavaScript 引擎，允许你直接在浏览器中编写和运行 JavaScript 代码。

要在浏览器中编写 JavaScript 代码，可以使用浏览器的开发者工具。要在 Google Chrome 中打开开发者工具，右键点击任何网页并从上下文菜单中选择“检查”。或者，你可以在 Windows 或 Linux 上按下 `Ctrl + Shift + I`，或在 Mac 上按下 `Command + Option + I`。

打开开发者工具窗口后，导航到“控制台”（Console）选项卡，你可以在那里编写 JavaScript 代码。例如，你可以尝试在控制台中输入以下代码，但将我的名字换成你的：

1. `console.log('My name is Ebenezer Don')`
2. `console.log('JavaScript is awesome!')`

要运行你的 JavaScript 代码，按下键盘上的 Enter 键。这将打印消息“My name is Ebenezer Don”并

## 如何编写和运行 JavaScript 代码

向控制台输出“JavaScript is awesome!”。做得好！稍后我会详细解释你刚刚编写的代码的每一个部分。

### 使用在线代码编辑器

编写和运行 JavaScript 代码的另一种方法是使用在线代码编辑器或在线集成开发环境（IDE）。有很多在线代码编辑器和 IDE 可用，允许你从浏览器中编写并运行 JavaScript 代码。流行的选项包括 `CodePen`、`JSFiddle` 和 `JS Bin`。

使用在线代码编辑器需要连接网络，但它也有许多优点。首先，它允许你在任何地方编写和运行代码。其次，你可以通过链接轻松与他人分享代码。第三，许多在线代码编辑器和 IDE 具有内置功能，可以简化编写代码和检查错误的过程。

### 使用离线代码编辑器

你还可以几种离线代码编辑器和 IDE 来编写和运行 JavaScript 代码。流行的选项包括 `Eclipse`、`NetBeans`、`Visual Studio` 和 `Visual Studio Code`（借助扩展程序）。这些 IDE 需要安装在你的本地计算机上，并且通常比在线代码编辑器具有更多功能和特性。它们通常用于更复杂的项目，即使你一开始不是从它们开始，随着学习的深入，你最终也会需要一个。

最容易开始的是你的浏览器控制台，所以我建议在控制台上编写并运行你的第一段 JavaScript 代码，这样做时，截一张屏幕并保存到你一年后还能访问的地方。我相信你会为自己的进步感到自豪。

## JavaScript 语法和数据类型

JavaScript 语法和数据类型是你学习 JavaScript 时应该理解的基础概念。编程语言的语法包括其编写和结构化代码的规则，而数据类型代表了你在代码中存储和操作的值的分类。

### 语法

这里是编写和结构化 JavaScript 代码的一些基本规则：

- JavaScript 是区分大小大小的，这意味着你使用的字符和关键字的大小很重要。所以，如果你在代码中编写像 'name' 这样的单词，JavaScript 会认为它与'Name' 或'nAme' 不同。这是初学者编写代码时常见的困惑，所以请注意你使用的的大小写。
- 使用空格、制表符和换行符来提高代码的可读性，但要确保保持一致性。这也被称为**缩进**（indentation），我们将在后续学习中看到示例。
- 你可以选择在每个语句末尾写分号（;）。*语句是任何指示计算机执行特定任务的代码行。* 使用分号终止语句过去是 JavaScript 代码正常运行的运行，但现在不再是了。所以你会看到一些带有分号的代码库，另一些没有。

保持代码风格的一致性是非常重要的，因为这有助于提高读性和理解，所以如果你选择使用分号，请在代码的每个语句中都使用分号；如果你选择不使用分号，就完全不要使用。还有一些规则你现在可能不容易理解，我将在后续学习中展示给你看。

### 数据类型

在 JavaScript 中，有几种数据类型用于表示不同类型的信息，如数字、文本或真假值。最基本的数据类型是数字、字符串和布尔值。一组具有相同或不同数据类型的多个值组合被称为数据结构。

JavaScript 是一种动态类型语言，这意味着值的类型是在程序运行时确定的，并可以在程序运行期间更改。这与其他编程语言不同，在其他语言中，你必须在创建时设置值的类型，并且以后无法更改。这些语言被称为“静态类型”。

JavaScript 中有几种基本数据类型，包括：

### 数字 Numbers

JavaScript 中的数字可以是整数或浮点数。整数是像 1、2 或 3 这样的整数，浮点数是带有小数点的数字，如 7.8 或 0.05。

你已经使用 `console.log()` 在浏览器控制台中显示了你的名字。`console.log()` 也是一个**方法**（method），我们稍后会详细解释。现在，你可以通过它们后面的括号 `()` 来识别方法。它们代表了计算机的一组指令。

让我们介绍另一个方法 `typeof()`。我们将用它来查找你在 JavaScript 中创建的任何值的类型。在你的浏览器控制台上，输入以下代码并按回车键应该显示文本“number”：

`typeof(10)`

练习你所学到的所有内容对于便于理解和记忆很重要。尝试使用 `typeof()` 方法来查找 **-10** 的类型。

注意，你仍然得到了响应'number'。这是因为正数和负数之间没有区别。正数是大于零的数字，负数是小于零的。你可以在 JavaScript 中用相同的语法表示正数和负数。

### 字符串 Strings

在 JavaScript 中，字符串是一组用于存储文本的字符。字符串通常用于存储单词和句子。要编写字符串，你必须将其封装在单引号（'This is a string'）或双引号（"This is also a string"）中。两种类型的引号都可以用于编写字符串，只要它们是一致的。所以，如果你用单引号开始写字符串，就必须用单引号结束。

字符串可以是一个单词、句子或多个段落，并且它可以包含字母、数字和空格的任何组合。我们之前使用的 `console.log()` 语句中的文本“My name is Ebenezer Don”也是一个字符串。记住在任何看到“Ebenezer Don”的地方都使用你的名字。

让我们分别使用单引号和双引号向控制台打印字符串“Hello World”：

`console.log('This is really cool!')`

`console.log("This is really cool!")`

现在，尝试使用 `typeof()` 方法来查找“Hello World”的类型。记住要注意关键字的大小写。例如，`typeof()` 方法中没有大写字母。字符串是 JavaScript 中一个重要的数据类型。你可以用它表示基于文本的数据，如名称、消息。

### 布尔值 Booleans

布尔值表示真或假值。它们通常用于进行比较并判断是否应该执行一组指令。当你在浏览器控制台上运行代码 `typeof(true)` 时，你应该得到响应'boolean'。

要在 JavaScript 中进行值比较，你可以使用符号 `>`（大于）、`<`（小于）或 `===`（相等）。现在，让我们看看字符串“Hey”和'hey'在 JavaScript 中是否相同。在控制台中运行以下行代码：

`'hey' === 'HEY'`

运行上面的代码应该返回 **false**，这是因为 JavaScript 中的字符串是区分大小写的。布尔值是 JavaScript 中一个重要的数据类型，因为它们允许你表示逻辑值、进行比较并条件运行代码。

## JavaScript 中的注释

在 JavaScript 中，注释是代码中执行时会被忽略的文本。它们非常用于为你的代码添加注释，或者临时禁用某些代码而无需删除它们。在 JavaScript 中有两种编写注释的方法：单行注释和多行注释。

### 单行注释

单行注释以双斜杠（//）开始，一直持续到行尾。例如：

`// This is a single-line comment`

### 多行注释

多行注释以正斜杠和星号（/*）开始，以星号和正斜杠（*/）结束。它们可以跨多行，并用于禁用代码块或为你的代码添加较长的注释和解释。这里是一个多行注释的示例：

```
/*
This is a
multi-line comment
*/
```

15

### 基础条件语句

### (If-else)

在 JavaScript 中，你可以使用条件语句根据条件是否满足来运行不同的代码块。*代码块是一组包含在花括号中的语句。*

条件语句是编程中至关重要的方面，因为它们允许你控制程序的执行流，并让程序在各种情况下表现出不同的行为。

JavaScript 中有两种主要的条件语句：if 语句和 switch 语句。在本节中，你将学习 if 语句，稍后将学习 switch 语句。

### If 语句

if 语句允许你在特定条件为真（true）时运行代码块。以下是 if 语句的基础语法：

```javascript
1 if (condition) {
2 // 如果条件为真则执行的代码
3 }
```

条件是一个布尔表达式，其结果为真（true）或假（false）。表达式是值和运算符的组合，求值为单个值。例如 `10 > 5` 是一个求值为真的表达式，而 `10 < 5` 是一个求值为假的的表达式。表达式也可以是一个单一值，如数字、字符串或布尔值。

如果条件求值为真，则执行**if 语句**内部的代码块。如果条件求值为假，则跳过该代码块。代码块包含在花括号 {} 中，被称为 **if 体（if body）**。

例如，运行以下代码应返回字符串“7 is greater than 5”：

```javascript
1 if (7 > 5) {
2 console.log('7 is greater than 5')
3 }
```

由于 7 大于 5，花括号中的 `console.log()` 语句将执行。同样，运行以下代码不会在控制台中返回任何内容：

```javascript
1 if (7 < 5) {
2 console.log('7 is less than 5')
3 }
```

注意我们将比较符号从 `>`（大于）改为 `<`（小于）。由于 7 并不小于 5，计算机不会执行 `console.log()` 语句。



你还会发现花括号内部的代码块前面有两个空格。这被称为**缩进（indentation）**，它让代码更容易阅读和理解。我们对代码进行缩进是为了显示它位于块内部。如果我们不对 `if` 语句内部的代码进行缩进，就很难判断它是 `if` 语句的一部分，还是一个完全独立的语句。JavaScript 运行不需要缩进，但对于编写可读性的代码和避免错误是必要的。你可以使用任何数量的空格进行缩进，但通常使用两个空格。你会发现一些开发者使用四个空格或制表符（tabs），但最好与你或你的团队选择的任何风格保持一致。

## Else 子句

你可以为 `if` 语句添加一个 **else 子句（else clause）**，这允许你在条件为假时指定一个要运行的代码块。以下是 `if-else` 语句的基础语法：

```javascript
if (condition) {
// 如果条件为真则执行的代码
} else {
// 如果条件为假则执行的代码
}
```

为我们的条件语句添加一个 `else` 子句：

```javascript
if (7 < 5) {
console.log('7 is less than 5')
} else {
console.log('The condition is false')
}
```

由于 `7` 并不小于 `5`，运行上述代码应返回字符串“The condition is false”。

条件语句是创建能够适应不同情况并根据接收到的数据做出决策程序的本质工具。随着学习的，我们将介绍更复杂的条件语句以及编写它们的其他方式。

## JavaScript 中的变量

### 简介

在不使用变量的情况下编写 JavaScript 代码并不容易。到目前为止，我们一直很好地避开了它们，但现在是时候你学习编程中最重要的概念之一了。

**变量（variable）**是计算机内存中用于存储数据的命名位置。简单来说，它是一个容器，我们可以在其中存储各种数据，如数字、文本、代码段，甚至是其他变量。所以，把变量想象成一个带有标签的盒子。标签是变量名，盒子的内容是变量值。

以下是 JavaScript 变量的示例：

```javascript
let myName = 'Ebenezer Don'
```

在这个示例中，我们创建了一个名为“`myName`”的变量并在其中存储了字符串值“Ebenezer Don”。这被称为**变量声明（variable declaration）**。变量声明由四个部分组成：声明关键字、变量名、赋值符号 (`=`) 和变量值。

### 声明关键字

`let` 关键字是你在 JavaScript 中声明变量的方法之一。还有其他声明变量的方法，但 `let` 是最常用的。随着学习的，你将学习其他的变量声明关键字。*在 JavaScript 中，关键字是具有特定用途的保留字。*

### 变量名

此示例中的变量名是 `myName`。为变量使用描述性名称是一个良好的习惯，因为当变量名代表了它的值时，你的代码会更容易理解。

### 赋值符号 (=)

赋值符号 (`=`) 用于给变量赋值。它也被称为赋值运算符，JavaScript 中还有其他运算符，如加法运算符 (`+`)、减法运算符 (`-`)、乘法运算符 (`*`) 和除法运算符 (`/`)。

### 变量值

在我们的示例中，变量值是字符串“Ebenezer”。变量的值可以是任何类型，包括数字、字符串、布尔值或其他变量。

我们可以使用 `console.log()` 将变量值打印到控制台。

```javascript
console.log(myName)
```

如果我们想通过赋值运算符将变量的值改为“Jane Butters”，可以写这行代码：

```javascript
myName = 'Jane Butters'
```

现在，如果你运行 `console.log` 语句，它会打印出“Jane Butters”。

### 变量声明与赋值

JavaScript 中有多种声明变量的方法，每种都有其用途。

### let 关键字

`let` 关键字是 JavaScript 中声明变量的方法。它用于创建局部变量，即只能在代码块内访问的变量。以下是使用 `let` 关键字创建局部变量的示例：

```javascript
if (true) {
let message = 'JavaScript is awesome!'
}
console.log(message)
```

在这个示例中，`message` 变量是局部的，仅在花括号代码块内访问。如果你在这个块之外尝试访问，将会报错。

**全局变量（Global variables）**是可以在代码中任何地方访问的变量。如果你想用 `let` 关键字创建一个全局变量，可以在代码块之外声明。以下是使用 `let` 关键字创建全局变量的示例：

```javascript
let name = 'Jane'
if (true) {
console.log(name)
}
```

运行这段代码将向控制台返回字符串值“Jane”。这是因为 `name` 变量是全局的，可以在代码的任何地方访问。

### var 关键字

`var` 关键字是 JavaScript 中声明变量的最旧方法，用于创建全局变量。所以，如果我们在第一个示例中使用 `var` 关键字来声明 `message` 变量，我们就不会报错。以下是使用 `var` 关键字创建全局变量的示例：

```javascript
if (true) {
var message = 'JavaScript is awesome!'
}
console.log(message)
```

上述代码不会返回任何错误，因为 `message` 变量是全局的。这意味着它可以在代码的任何地方访问，包括声明它的代码块之外。

在使用全局变量时必须小心。由于它们可以在代码的任何地方访问，全局变量可能会导致问题。例如，如果你在代码中声明了一个与局部变量同名的全局变量，全局变量将覆盖局部变量；这会导致代码中出现意想不到的结果和困惑。

## const 关键字

到为止，我们已经学习了如何创建可以重新赋值的局部和全局变量。但大多数情况下，创建不可重新赋值的变量更安全，这样我们就不会意外改变它们的值。`const` 关键字就用于此目的。

这是一个常量变量的示例：

```javascript
const age = 21
```

如果我们尝试重新给 `age` 变量赋值，将会得到一个错误：

```javascript
age = 22
// Uncaught TypeError: Assignment to constant variable.
```

这是因为 `age` 变量是一个常量变量，不能重新赋值。使用 `const` 关键字是我声明不需要重新赋值的变量的首选方式。

## 变量命名规则和规范

在编程中，**惯例**（convention）是你应该遵循的一系列指南，以确保你的代码以一致的风格编写，并且易于阅读和理解。在命名变量时，遵循 JavaScript 变量命名规范至关重要，这可以确保你的代码正常运行并避免错误。**bug**（bug）是你代码中的错误，会导致程序运行异常或完全不运行。以下是在 JavaScript 中命名变量时通常遵循的规则和规范。我们将从应该避免的事开始，然后介绍在命名变量时应该做什么。

### 避免使用数字作为变量名的第一个字符

变量名不能以数字开头，尽管它们包含数字。例如，变量名 `person1` 是有效的，但如果你将变量命名为 `1person`，就会得到一个错误。

### 避免在变量名中使用特殊字符

在 JavaScript 中，特殊字符是在语言中具有特定含义或用途且不是字母、数字或符号的字符。这些包括：`@` `!` `#` `$` `%` `^` `&` `*` `(` `)` `_` `+` `-` `=` `{` `}` `[` `]` `:` `;` `“` `”` `‘` `’` `<` `>` `,` `.` `?` `/` `\` `|` `~`

变量名不能包含特殊字符，因此如果你尝试将变量命名为 `name-of-person` 或 `#name_of_person`，就会得到一个错误。美元符号 `$` 有时用作变量名前缀，但这并不是要求的，且通常不建议这样做。

### 避免在变量名中使用空格

变量名不能包含空格。因此，将变量命名为 `my country` 或 `my age` 将导致错误。

### 避免在变量名中使用保留字

JavaScript 有一组不能用作变量名的保留字。这些包括如 `var`、`const` 和 `let` 等词。将保留字作为变量名会导致错误。你可以在 Mozilla 开发者网络 (MDN) 文档中查看 JavaScript 保留字的完整列表。（[在这里]）

### 变量名的最大和最小长度

JavaScript 中的变量名没有明确的最大或最小长度限制。然而，某些限制可能会影响变量名的最大长度。

其中一个限制是 JavaScript 中字符串的最大长度，为 $2^{53} - 1$（约 9 万亿个字符）。所以你不能拥有比这更长的变量名，但在实践中，你可能不需要这么长的变量名。

### 使用驼峰命名法命名变量

在命名变量时，一个单词可能不足以描述变量存储的内容。由于你不能在变量名中使用空格，可以使用驼峰命名法（camelCase）来分隔组成变量名的单词。

驼峰命名法是一种命名规范，其中变量名的第一个字母小写，每个后续单词的首字母大写。例如，如果你想命名一个存储学生年龄的变量，可以写成 `studentAge` 或 `ageOfStudent`。

在 JavaScript 中，驼峰命名法是变量最常用的命名规范。因此，在命名变量时，始终从小写字母开头并使用驼峰命名法来分隔单词。

### 使用有意义的变量名

为变量使用描述性且有意义的名字是非常重要的；这会让你的代码更易编写、阅读和理解。例如，如果你正在创建一个变量来存储学生姓名，你应该写类似 `nameOfStudent` 或 `studentName`，而不是 `x` 或 `sname`。你的变量名应该始终代表它们所存储的数据，因为描述性的变量名有助于更好地理解变量的作用和功能。这将帮助你避免 bug，提高代码质量并使其更易维护。

如何命名变量非常重要，通过遵循建议的规范，你将编写出易于阅读、理解和维护的代码。

## 基础 JavaScript 运算符

运算符是可以在值上执行操作的符号。例如，当你在计算器上输入 `2+3` 时，你使用 `+` 运算符来相加两个值。值 `2` 和 `3` 被称为操作数，而加号符号 (`+`) 是运算符。在本章中，我们将探索 JavaScript 中不同类型的运算符，包括：

- 算术运算符

- 字符串运算符

- 赋值运算符

- 比较运算符

- 逻辑运算符

### 算术运算符

我们使用算术运算符执行数学计算，如加法 (`+`)、减法 (`-`)、乘法 (`*`) 和除法 (`/`)。以下是一些你可以在控制台中尝试的示例：

```javascript
console.log(10 + 2) // 输出: 12
console.log(10 - 2) // 输出: 8
console.log(10 * 2) // 输出: 20
console.log(10 / 2) // 输出: 5
```

我们还有递增和递减运算符。递增运算符 (`++`) 将变量的值加 `1`，而递减运算符 (`--`) 将变量的值减 `1`。这些运算符可以放在操作数之前或之后。

当放在操作数之前时，这些运算符被称为前置运算符，这意味着操作在返回值之前应用，从而给我们一个新值。这是一个示例：

```javascript
let firstValue = 3
console.log(++firstValue) // 输出: 4
```

当放在操作数之后时，它们被称为后置运算符；操作在返回当前值后应用到变量。这是一个示例：

```javascript
let secondValue = 5
console.log(secondValue++) // 输出: 5
console.log(secondValue) // 输出: 6
```

注意，我们必须单独记录变量以获取它的新值。这是因为当你使用后置运算符时，值先返回，然后应用操作。

同样重要的是，递增和递减运算符会给变量赋新值，因此你只能对使用 `let` 关键字声明的变量执行此操作。如果你对使用 `const` 关键字声明的变量使用这些运算符，将得到错误。让我们尝试一下。记住始终亲自运行这些示例以查看结果：

```javascript
const thirdValue = 7
console.log(++value) // Uncaught ReferenceError: value is not defined
```

JavaScript 中还有两个你可以使用的算术运算符：**取模运算符** (`%`) 和 **幂运算符** (`**`)。

**取模运算符**当操作数被另一个操作数除时返回剩余的值。因此，如果你在控制台中运行 `5 % 2`，你会得到 `1`，因为 `2` 除 `5` 两次余 `1`。

**幂运算符**将第一个操作数提升为第二个操作数的幂。因此，如果你在控制台中运行 `2 ** 3`，你会得到 `8`，因为 `2` 的三次幂是 `8`（即 `2*2*2`）。

### 拼接运算符

在 JavaScript 中，我们使用拼接运算符来拼接字符串。当一个或多个操作数是字符串时，加号符号 (`+`) 用作拼接运算符。因此，如果你在控制台中运行 `'Hello' + 'World'`，你会得到输出 “HelloWorld”。

此外，如果你在控制台中运行 `'Hello' + 1`，你会得到输出 ‘Hello1’。当你对字符串和数字使用加运算符时，数字将转换为字符串形式然后进行拼接。让我们尝试更多示例：

```javascript
console.log('Hello' + ' ' + 'Everyone') // 输出: Hello Everyone
console.log('James ' + 'Bond ' + 007) // 输出: James Bond 007
console.log(
  10 + 'years from now' + "I'll be a 100 years old"
) // 输出: 10 years from now I'll be a 100 years old
```

注意我们在第一个示例中使用了空格字符 (`' '`) 来分隔单词。如果不使用空格字符，我们将得到输出 ‘HelloEveryone’。在第二个示例中，我们在单词 ‘James’ 的同一个字符串中添加了空格字符。这是在拼接字符串时在单词间添加空格的另一种方法。

在第三个示例中，我们使用双引号（“ ”）来包裹字符串。这是因为字符串（`I'll`）包含一个单引号，如果我们也使用单引号（’ ’）来包裹它，就会导致错误。

### 赋值运算符

我们使用赋值运算符来给变量赋值。你已经见过赋值运算符 (`=`) 的用法了。JavaScript 中还有复合赋值运算符，包括：`+=`, `-=`, `*=`, `/=` 和 `%=`。这些复合运算符会对变量和操作数执行操作，然后将结果赋值给该变量。例如，如果你有一个名为“`age`”且值为 `10` 的变量，想让它增加 `5`，可以这样使用`+=`运算符：

```javascript
let age = 10
age += 5; // 输出: 15
```

使用 `+=` 运算符等同于编写 `age = age + 5`，这会将 `age` 变量重新赋值为 `10 + 5`。让我们用其他复合赋值运算符尝试一些例子：

```javascript
age = 10
age *= 5; // Output: 50
age /= 5; // Output: 10
age -= 5; // Output: 5
age %= 5; // Output: 0
```

复合赋值运算符是减少代码重复的一种极佳方法。

### 比较运算符

我们使用比较运算符来比较两个值，并根据比较结果返回布尔值（`true` 或 `false`）。以下是比较运算符及其含义：

- `==` : 等于

- `!=` : 不等于

- `>` : 大于

- `<` : 小于

- `>=` : 大于等于

- `<=` : 小于等于

- `===` : 严格等于（比较操作数的值和类型）

- `!==` : 严格不等于（比较操作数的值和类型）

让我们尝试一些例子：

```javascript
console.log(10 == 10); // 输出: true
console.log(10 == 5); // 输出: false
console.log(10 != 5); // 输出: true
console.log(10 > 5); // 输出: true
console.log(10 < 5); // 输出: false
console.log(10 >= 10); // 输出: true
console.log(10 >= 11); // false: 10 既不大于等于 11
console.log(10 <= 10); // true: 10 等于 10
console.log(10 <= 9); // false: 10 既不小于等于 9
console.log(10 === 10); // true: 10 等于 10 且它们都是数字
console.log(10 === '10'); // false: 数字 10 不等于字符串 '10'
console.log(10 !== 9); // true: 10 不等于 9
console.log(10 !== '10'); // true: 数字 10 不等于字符串 '10'
```

### 逻辑运算符

在 JavaScript 中，我们使用逻辑运算符来执行逻辑操作，如与 (`&&`)、或 (`||`) 和非 (`!`)。以下是一些示例：



```javascript
console.log(true && true); // 输出: true
console.log(true && false); // 输出: false
console.log(false && true); // 输出: false
console.log(false && false); // 输出: false
console.log(true || true); // 输出: true
console.log(true || false); // 输出: true
console.log(false || true); // 输出: true
console.log(false || false); // 输出: false
console.log(!true); // 输出: false
console.log(!false); // 输出: true
```

当两个操作数都为 `true` 时，与运算符 `&&` 返回 `true`；如果任一操作数为 `false`，它则返回 `false`。所以，如果你在控制台中运行`console.log(10 > 5 && 7 < 10)`，你将得到 `true` 输出，因为 `10` 大于 `5` 且 `7` 小于 `10`。但如果你在控制台中运行`console.log(10 > 5 && 7 > 10)`，你将得到 `false` 输出，因为 `10` 大于 `5`，但 `7` 并不大于 `10`。使用或运算符 `||` 时，如果至少有一个操作数为 `true`，则返回 `true`；如果两个操作数都为 `false` 则返回 `false`。所以，如果你在控制台中运行`console.log(10 > 5 || 7 > 10)`，你将得到 `true` 输出，因为 `10` 大于 `5`。非运算符 `!` 会反转其操作数的布尔值。所以，如果你在控制台中运行`console.log(!(10 > 5))`，你将得到 `false` 输出，因为 `10` 大于 `5`。

## Functions

让我们尝试给函数提供一个非数字的内容：

```javascript
console.log(multiplyByTwo('this is a string'))
// output: Value must be a number
```

### 函数参数 (Parameters) 与 实参 (Arguments)

当我们调用函数时，我们提供的用来替换其参数的值被称为实参（arguments）。

因此在我们的案例中，数字`35`和字符串`“this is a string”`就是我们的函数实参。

- 在函数定义期间，代表我们打算提供给函数的名称称为参数（parameters）。
- 在函数调用期间，我们提供给函数的实际值被称为实参（arguments）。
- 我们可以在函数定义中使用最多 `255` 个参数。

### 关于 return 语句（return statement）的更多信息

如果不使用`return`语句来告诉函数返回什么，它的默认值将是`undefined`。

让我们通过创建一个没有`return`语句的函数并调用它来测试：

```javascript
function multiplyByTwo(value) {
  const result = value * 2;
}
console.log(multiplyByTwo(35))
// output: undefined
```

当我们提供`return`关键字但不提供值时，函数默认也会返回`undefined`。这使得它成为了空返回（empty return）：

```javascript
function multiplyByTwo() {
  const result = value * 2;
}
console.log(multiplyByTwo(35))
// output: undefined
```

### 匿名函数 (Anonymous functions)

你已经见过如何使用函数声明来定义命名函数。你也可以使用函数声明来定义匿名函数（anonymous functions）和立即执行函数表达式（IIFE）。

匿名函数是没有名称的函数；因此被称为“匿名”。由于我们无法通过名称引用上述函数，因此无法在我们的代码库的其他地方调用它。在这种情况下，该函数通常是一个 IIFE（立即执行函数表达式），这意味着它将在声明后后立即被调用。为了实现这一点，我们将函数封装在括号中，并在其声明后紧跟另一一对括号来立即调用它：

```javascript
(function() {
  return "I'm a function, and I'm anonymous!";
})()
```

### 函数表达式 (Function expression)

为了重用匿名函数，我们必须将其赋值给变量（variable）。这样我们就可以通过该名称引用它。实现这一方法是通过函数表达式（Function expression）。让我们将匿名函数赋值给一个变量：

```javascript
const alertUser = function() {
  return "I'm anonymous, but with a name!"
}
```

现在，我们可以像调用`multiplyTwo()`一样调用（或执行）我们的函数。由于我们的函数没有参数（parameter），因此不需要提供实参（argument）。

```javascript
alertUser()
```

### 多行 return 语句 (Multi-line return statements)

在函数中返回表达式时，不要在`return`和值之间换行。你可能忍不住将表达式与`return`语句分开：

```javascript
function multiplyFive(value) {
  return
  value * 5
}
```

调用上面的`multiplyFive`函数将返回`undefined`，这是因为我们的编译器在`return`关键字之后结束了语句，使其成为空返回。如果你想让`return`语句跨多行，你应该在`return`关键字的同一行开始你的表达式，或者在`return`关键字的同一行有一个左括号：

```javascript
function multiplyFive(value) {
  return (value * 5)
}
console.log(multiplyFive(10))
// output: 50
```

### 箭头函数 (Arrow Functions)

JavaScript 箭头函数，也称为“胖箭头（fat arrow）”或“lambda”函数，是在 JavaScript 中编写函数表达式的简写方式。它们是在 ES6（JavaScript 的第六个主要版本）中引入的，并已经在现代 JavaScript 开发中变得流行。

箭头函数使用“胖箭头”语法定义，即一个等号后跟着一个大于号 (`=>`)。例如，让我们使用你已知的函数声明语法来编写一个返回数字平方的函数，即该数字乘以其本身：

```javascript
const squareNumber = function (value) {
  return value * value
}
console.log(squareNumber(5))
// Output: 25
```

等价的箭头函数如下：

```javascript
const squareOfNumber = (value) => value * value
```

看，这比函数声明语法短得多。首先，我们定义了一个名为`squareNumber`的变量，然后将我们的箭头函数作为它的值。箭头函数接受一个名为`value`的参数并返回它的平方。由于函数体是一个单一表达式，我们不需要使用大括号。我们也可以省略`return`关键字，当我们省略它时，函数将返回表达式的值。

如果箭头函数只有一个参数，你可以省略参数列表周围的括号：

```javascript
const squareOfNumber = value => value * value
```

你也可以使用大括号编写箭头函数，但在这种情况下，你必须使用`return`关键字：

```javascript
const squareOfNumber = (value) => {
  return value * value
}
```

使用箭头函数的主要优点之一是它们的简洁性。当你需要编写一个接受另一个函数作为参数的函数时，它们特别有用。当一个函数被作另一个函数的参数时，它被称为回调函数（callback function）。而接受回调函数作为参数的父函数被称为高阶函数（higher order function）。随着学习的进行，我们将学习更多这些概念。

### 函数最佳实践 (Functions best practices)

函数的命名应该是描述性的、直击当的且持久的。

注意我们如何命名第一个函数`multiplyByTwo`。这是因为它的工作是将数字乘以 2。这样做有助于任何人通过名称知道我们的函数在做什么。

函数命名是函数定义中至关重要的部分，忽视这一点会导致你的代码不可读、不可维护，并导致效率降低。

在命名函数时，务必不要使用只有少数人理解的俚语或人们只能在特定时间内相关的趋势。

让你的函数名具有描述性、直击重点且持久性。

---

**注意事项**

- 函数（Function）是一组旨在执行特定任务的语句集合。
- 在函数定义期间，代表我们打算提供给函数的名称称为参数（parameters）。
- 在函数调用期间，我们提供给函数的实际值被称为实参（arguments）。
- 我们可以在函数定义中使用最多 `255` 个参数。
- 匿名函数是不带名称的函数，为了重用匿名函数，我们必须将其赋值给变量。
- IIFE（立即执行函数表达式）是一种在声明后立即被调用的函数。
- 函数应该只有单一职责。
- 函数名应该是描述性的、直击重点且持久的。

## Functions

### toUpperCase()

`toUpperCase()`方法用于将字符串转换为大写。

我们可以在任何字符串上使用此方法，它将返回一个新字符串，其中包含原始字符串的所有大写字符。让我们来看一个例子：

```javascript
let message = 'Hello World'
console.log(message.toUpperCase())
// output: HELLO WORLD
```

`toUpperCase()`方法不会改变原始字符串。相反，它会返回一个新字符串。因此，`message`变量将保持不变：

```javascript
console.log(message)
// output: Hello World
```

### toLowerCase()

`toLowerCase()`方法将字符串转换为小写。与`toUpperCase()`方法一样，它不会改变原始字符串。让我们用上面创建的`message`变量尝试一个例子：

```javascript
console.log(message.toLowerCase())
// output: hello world
```

### trim()

`trim()`方法用于移除字符串开头和结尾的空白字符：

```javascript
let message = ' Hello World '
console.log(message.trim())
// output: Hello World
```

需要理解的一个重要概念是这些方法是可以链调用的，这意味着你可以在同一个字符串上连续调用多个方法，以便在单行代码中执行多个操作。让我们尝试一个演示链式多个内置方法来操作字符串的例子：

```javascript
let message = ' Hello World '
console.log(message.trim().toUpperCase())
// output: HELLO WORLD
```

在上面的示例中，我们首先在`message`变量上调用`trim()`方法来移除字符串开头和结尾的空白。然后，我们在`trim()`方法的结果上调用`toUpperCase()`方法，将字符串转换为大写。

JavaScript 中的内置方法为编写可读且简洁的代码提供了许多功能。随着本书的不断进行，我们还将介绍其他一些实用的字符串方法。良好地理解我们目前所涵盖的方法，以及如何使用它们来编写高效的代码是非常重要的。

### JS Math functions

JavaScript 拥有一个内置的`Math`对象，它包含了用于数学常数和操作的属性和方法。让我们来看一些最常用的方法。

### Math.round()

`Math.round()`方法返回四舍五入到最近整数的数字。让我们来看一个例子：

```javascript
console.log(Math.round(4.7))
// output: 5
```

### Math.ceil()

`Math.ceil()`方法返回向上取整到最近整数的数字值。如果一个数字已经是整数，该方法将返回该数字：

```javascript
console.log(Math.ceil(4.2))
// output: 5
console.log(Math.ceil(5))
// output: 5
```

方法名中的“ceil”代表“ceiling”（天花板），这是向上取整到最近整数的数学术语。

### Math.floor()

`Math.floor()`方法返回向下取整到最近整数的数字值。与`Math.ceil()`方法一样，如果一个数字已经是整数，该方法将返回该数字：

```javascript
console.log(Math.floor(4.7))
// output: 4
console.log(Math.floor(4))
// output: 4
```

方法名中的“floor”是“ceiling”的反面。

### Math.random()

`Math.random()`方法返回一个 `0`（包含）到 `1`（不包含）之间的随机数：

```javascript
console.log(Math.random())
// output: 0.3218232744225875
```

生成的数字每次运行代码时都会不同，并且始终小于 `1`。如果你想生成一个 `0` 到 `10` 之间的随机数，可以将`Math.random()`的结果乘以 `10`：

```javascript
console.log(Math.random() * 10)
// output: 8.688668583064922
```

### Math.max()

`Math.max()`方法返回一组数字中的最大值。该方法期望这些数字作为单独参数传递。让我们来看一个例子：

```javascript
console.log(Math.max(1, 2, 3, 4, 5))
// output: 5
```

不带任何参数调用`Math.max()`将返回`-Infinity`（负无穷）：

```javascript
console.log(Math.max())
// output: -Infinity
```

如果你向`Math.max()`传递非数字参数，它将返回`NaN`（不是数字）：

```javascript
console.log(Math.max(1, 2, 3, 4, 5, 'a'))
// output: NaN
```

### Math.min()

`Math.min()`方法返回一组数字中的最小值：

```javascript
console.log(Math.min(1, 2, 3, 4, 5))
// output: 1
```

`Math`对象中还有其他一些实用的方法，但这些是最常用的。我们可以一起使用这些方法来执行复杂的数学运算。例如，由于`Math.random()`总是返回小数，我们可以将其封装在`Math.floor()`方法中，将其向下取整到最近整数，这样我们生成的数字始终是一个整数：

```javascript
console.log(Math.floor(Math.random() * 10))
// output: 3
```

## Arrays

在 JavaScript 中，我们使用数组在单个变量中存储多个值。这些值可以是任何数据类型，包括数字、字符串，甚至其他数组。你也可以将数组认为是一种存储项目列表的数据结构。数组是许多 JavaScript 程序的基础构建块。它们被用于各种语境，从简单的数据列表到更复杂的数据结构。让我们学习如何在 JavaScript 中创建、访问和操作数组。

### 声明和初始化数组

在 JavaScript 中，我们可以使用数组构造函数或方括号语法来声明和初始化数组。

```javascript
// 声明空数组
let fruits = new Array();
let colors = [];

// 初始化带元素的数组
let fruits = new Array('apple', 'banana', 'orange');
let colors = ['red', 'green', 'blue'];

// 也可以通过赋值初始化
let numbers = new Array();
numbers[0] = 1;
numbers[1] = 2;
```

### 访问和修改数组元素

初始化完成后，我们可以通过索引来访问和修改数组中的元素。数组的索引从 `0` 开始计数。



```javascript
let fruits = ['apple', 'banana', 'orange'];

// 访问第一个元素
console.log(fruits[0]); // output: apple

// 访问第二个元素
console.log(fruits[1]); // output: banana

// 修改第一个元素
fruits[0] = 'strawberry';
console.log(fruits[0]); // output: strawberry
```

## 数组长度

数组的 `length` 属性返回数组中元素的数量。

```javascript
let fruits = ['apple', 'banana', 'orange'];
console.log(fruits.length); // output: 3

// 添加元素后长度会变化
fruits.push('mango');
console.log(fruits.length); // output: 4

// 删除元素后长度会变化
fruits.pop();
console.log(fruits.length); // output: 3
```

## 数组

### 数组方法

数组有多种方法可以用来操作和与存储在其中的数据进行交互。这些方法是每个 JavaScript 数组都可用的内置函数。你可以使用它们在数组中添加、删除、重新排列或搜索元素。

一些常用的数组方法包括：

- `push()` - 向数组末尾添加一个或多个元素
- `pop()` - 从数组中删除最后一个元素
- `shift()` - 从数组中删除第一个元素
- `unshift()` - 向数组开头添加一个或多个元素
- `indexOf()` - 返回元素在数组中首次出现的索引
- `slice()` - 将数组的一部分浅拷贝到一个新数组对象中
- `splice()` - 通过移除或替换现有元素和/或在原有位置添加新元素来更改数组的内容
- `join()` - 将数组中的所有元素连接成一个字符串

让我们来尝试一些示例。

#### `push()`

`push()` 方法向数组末尾添加一个或多个元素，并返回数组的新长度。让我们在 `favoriteFruits` 数组的末尾添加两种新水果：

```javascript
favoriteFruits.push('mango', 'pineapple')
// output: 5
```

上述代码会将 `'mango'` 和 `'pineapple'` 加到 `favoriteFruits` 数组的末尾，并返回它的新长度，即 5。如果你将 `favoriteFruits` 数组打印到控制台，你会看到我们刚刚添加的新元素：

```javascript
console.log(favoriteFruits)
// output: ['strawberry', 'banana', 'orange', 'mango', 'pineapple']
```

#### `pop()`

`pop()` 方法从数组中删除最后一个元素并返回该元素。让我们从 `favoriteFruits` 数组中删除最后一个元素：

```javascript
favoriteFruits.pop()
// output: 'pineapple'
```

如果你将 `favoriteFruits` 数组打印到控制台，你会发现 `'pineapple'` 不再那里了：

```javascript
console.log(favoriteFruits)
// output: ['strawberry', 'banana', 'orange', 'mango']
```

#### `shift()`

该方法从数组中删除第一个元素并返回被删除的元素：

```javascript
favoriteFruits.shift()
// output: 'strawberry'
```

#### `unshift()`

`unshift()` 方法向数组开头添加一个或多个元素并返回其新长度：

```javascript
favoriteFruits.unshift('lemon', 'grape')
// output: 5
```

将 `favoriteFruits` 数组打印到控制台将显示我们刚刚添加的新元素：

```javascript
console.log(favoriteFruits)
// output: ['lemon', 'grape', 'banana', 'orange', 'mango']
```

#### `indexOf()`

你可以使用 `indexOf()` 方法找到元素在数组中首次出现的索引。让我们在 `favoriteFruits` 数组中找到 `'banana'` 的索引：

```javascript
favoriteFruits.indexOf('banana')
// output: 2
```

这将返回 2，因为 `'banana'` 是 `favoriteFruits` 数组中的第三个元素，这意味着它的索引为 2。请记住，在标识数组元素的索引时，我们从 0 开始计数。如果你查找的元素不在数组中，`indexOf()` 方法将返回 -1：

```javascript
favoriteFruits.indexOf('watermelon')
// output: -1
```

#### `slice()`

`slice()` 方法用于提取数组的一部分。该方法接受两个参数：切片的起始索引（包含）和结束索引（不包含）。起始索引处的元素将包含在切片中，但结束索引处的元素将不包含。`slice()` 方法不会修改原始数组。相反，它返回一个包含提取元素的新数组。

让我们从 `favoriteFruits` 数组中提取前三个元素并将它们放入名为 `topThreeFruits` 的新数组中：

```javascript
const topThreeFruits = favoriteFruits.slice(0, 3)
console.log(topThreeFruits)
// output: ['lemon', 'grape', 'banana']
```

如果不指定结束索引，切片将一直到数组末尾：

```javascript
const fruitsInTheBasket = favoriteFruits.slice(2)
console.log(fruitsInTheBasket)
// output: ['banana', 'orange', 'mango']
```

记住 `favoriteFruits` 的值仍然是 `['lemon', 'grape', 'banana', 'orange', 'mango']`。在上面的代码中，我们的切片从索引 2 开始，即 `'banana'`，由于我们没有指定结束索引，切片一直到了数组的末尾，给了我们 `['banana', 'orange', 'mango']`。

`slice()` 方法还可以接受负索引。如果你传递负索引，切片将从数组末尾开始。因此，为了获取 `favoriteFruits` 数组的最后一个元素，我们可以这样写：

```javascript
const lastFruit = favoriteFruits.slice(-1)
console.log(lastFruit)
// output: ['mango']
```

#### `splice()`

`splice()` 方法通过移除或替换现有元素和/或在原有位置添加新元素来更改数组的内容。它可以接受多个参数：第一个是起始索引，第二个是移除元素的数量，剩余的是要添加的元素。与 `slice()` 方法不同，`splice()` 会修改原始数组。我们将 `favoriteFruits` 数组的前两个元素替换为 `'cherry'` 和 `'avocado'`：

```javascript
favoriteFruits.splice(0, 2, 'cherry', 'avocado')
console.log(favoriteFruits)
// output: ['cherry', 'avocado', 'banana', 'orange', 'mango']
```

#### `join()`

`join()` 方法将数组中的所有元素连接成字符串。它接受一个可选参数，作为元素之间的分隔符。如果不指定分隔符，元素将用逗号连接。`join()` 方法不会修改原始数组，所以如果你想连接 `favoriteFruits` 数组并将结果存储在一个新变量中，你可以这样写：

```javascript
const favoriteFruitsString = favoriteFruits.join()
console.log(favoriteFruitsString)
// output: 'banana,orange,mango'
```

你可以传递不同的分隔符作为参数：

```javascript
const newFavoriteFruitsString = favoriteFruits.join(' and ')
console.log(newFavoriteFruitsString)
// output: 'banana and orange and mango'
```

#### `reverse()`

`reverse()` 方法反转数组元素的顺序。让我们反转 `favoriteFruits` 数组的顺序：

```javascript
favoriteFruits.reverse()
console.log(favoriteFruits)
// output: ['mango', 'orange', 'banana']
```

## 高阶函数 (HOFs) 与回调函数

```javascript
const numbers = [1, 2, 3, 4, 5]

const squaredNumbers = numbers.map(
  (number) => number * number
)

console.log(squaredNumbers)
// Output: [1, 4, 9, 16, 25]
```

在这个示例中，匿名函数 `(number) => number * number)` 被作为参数传递给 `map()` 函数。在回调函数中，`number` 参数代表 `numbers` 数组中的每个元素。我们可以我们想要的任何名称，但通常使用数组名称的单数形式。

`map()` 函数将回调函数应用到数组中的每个元素，并返回一个名为 `squaredNumbers` 的新数组，该数组包含原数组中每个元素的平方。

让我们尝试另一个示例，使用 `map()` 函数将字符串数组中的每个元素转换为大写字母：

```javascript
const words = ['this', 'is', 'such', 'a', 'great', 'day']
const capitalizedWords = words.map((word) =>
  word.toUpperCase()
)

console.log(capitalizedWords)
// Output: ['THIS', 'IS', 'SUCH', 'A', 'GREAT', 'DAY']
```

在这个示例中，我们使用 `map()` 函数将 `words` 数组中的每个元素转换为大写。`map()` 函数不会修改原始数组，因此我们必须将其返回值赋值给名为 `capitalizedWords` 的新数组。

## 创建高阶函数

我们可以自己创建高阶函数。我们需要做的只是在调用时添加一个函数参数，或者返回另一个函数。这里有一个接受回调函数作为参数的高阶函数示例：

```javascript
const higherOrderFunction = (callback) => {
  const string = 'HOFs are really cool!'
  callback(string)
}

higherOrderFunction(console.log)
// Output: 'HOFs are really cool!'
```

注意我们的 `higherOrderFunction()` 接收一个回调函数作为参数，然后使用字符串 `'HOFs are really cool!'` 调用该函数。在这种情况下，将 `console.log()` 作为参数传递给 `higherOrderFunction()` 会将字符串打印到控制台。

我们还可以从一个函数中返回另一个函数。这里有一个返回回调函数的高阶函数示例：

```javascript
const callMeTwice = () => console.log

callMeTwice()('Hey, this works!')
// Output: 'Hey, this works!'
```

在这个示例中，`callMeTwice()` 函数返回 `console.log()` 函数。因此，当我们调用 `callMeTwice()` 时，得到的是 `console.log()` 函数。所以，我们需要调用 `callMeTwice()` 的结果来使用 `console.log()` 函数。

这种链式函数调用被称为**柯里 (currying)**。在柯里中，每次函数调用都会返回另一个函数，该函数可以使用不同的参数再次调用。主要目标是通过将过程拆分为一系列函数调用（每个调用接受单个参数），来简化向函数传递参数的过程。

## 内置 HOF 和数组方法

让我们探索其他可以用于操作数组的内置高阶函数。

### `forEach()`

`forEach()` 函数是一个数组方法，它会在数组的每个元素上执行回调函数。与 `map()` 函数不同，`forEach()` 不返回新数组，也不会修改原始数组。相反，它遍历数组的元素并对每个元素执行某种操作。**迭代 (iterate)** 意味着重复执行某个特定操作或一组操作若干次，直到满足某个条件为止。

我们可以使用 `forEach()` 函数将数组中的每个元素打印到控制台，或者对每个元素执行某种操作并将结果推入新数组。让我们使用 `forEach()` 函数将数组中的每个元素打印到控制台：

```javascript
const namesOfPeople = ['oluchi', 'jude', 'kanye', 'tiwa']

namesOfPeople.forEach((name) => console.log(name))
```

这将输出：

1. oluchi
2. jude
3. kanye
4. tiwa

注意我们数组中的名字是以小写字母开头的。以下是将数组中的每个元素转换为首字母大写（title-case）并将结果推入新数组的方法。首字母大写意味着将字符串中每个单词的首字母大写：

```javascript
const titleCasedNames = []

namesOfPeople.forEach((name) => {
  const titleCasedName = name[0].toUpperCase() + name.slice(1)
  titleCasedNames.push(titleCasedName)
})

console.log(titleCasedNames)
// Output: ['Oluchi', 'Jude', 'Kanye', 'Tiwa']
```

在这个示例中，我们使用 `forEach()` 函数遍历 `namesOfPeople` 数组。对于数组中的每个字符串，我们使用方括号符号和 `toUpperCase()` 方法将其首字母大写。*在处理字符串时，我们可以使用方括号符号和字符索引来访问字符串中的每个字符。* `slice()` 方法返回一个新的字符串，包含从我们指定的索引到字符串末尾的字符。然后我们将首字母大写的名字推入 `titleCasedNames` 数组。

### `filter()`

`filter()` 函数是另一个我们可以用来过滤掉符合特定条件的元素的数组方法。例如，如果我们有一个国家数组，可以使用 `filter()` 函数过滤掉以字母 `'N'` 开头的国家：

```javascript
const countries = [
  'Nigeria',
  'UK',
  'Netherlands',
  'Canada',
  'USA',
  'Norway',
]

const countriesThatStartWithN = countries.filter(
  (country) => country.startsWith('N')
)

console.log(countriesThatStartWithN)
// Output: ['Nigeria', 'Netherlands', 'Norway']
```

在 JavaScript 中，每个字符串都有一个 `startsWith()` 方法，如果字符串以我们指定的字符开头，则返回 true。在我们的示例中，`filter` 方法接收一个带有参数 `country` 的回调函数，该参数代表 `countries` 数组中的每个元素。如果国家以字母 `'N'` 开头，回调函数返回 true，`filter()` 返回包含符合条件元素的新数组。

我们使用方括号符号或 `charAt()` 方法来检查字符串是否以某个字符开头。`charAt()` 方法返回字符串中指定索引处的字符：

```javascript
const countriesThatWithU = countries.filter(
  (country) => country.charAt(0) === 'U'
)

console.log(countriesThatWithU)
// Output: ['UK', 'USA']
```

我们可以使用 `filter()` 函数过滤掉不符合条件的元素。让我们过滤掉不以字母 `'N'` 开头的国家：

```javascript
const countriesDontStartWithN = countries.filter(
  (country) => !country.startsWith('N')
)

console.log(countriesDontStartWithN)
// Output: ['UK', 'Canada', 'USA']
```



在这个示例中，我们使用逻辑非运算符（`!`）来反转条件，使得`filter()`函数返回一个包含不符合条件元素的新数组。在使用`filter`方法时，需要重要的是回调函数应该返回一个布尔值。

### sort()

`sort()`方法用于对数组元素进行排序。`sort()`方法会修改原始数组并返回排序后的数组。例如，如果我们想对数字数组排序，可以使用`sort()`方法。默认情况下，`sort()`方法按升序对数组元素排序：

```javascript
const numbers = [7, 4, 3, 1, 5, 2, 8, 6]

numbers.sort()

console.log(numbers)
// Output: [1, 2, 3, 4, 5, 6, 7, 8]
```

我们也可以对字符串数组进行排序：

```javascript
const favoriteColors = [
  'red',
  'blue',
  'green',
  'yellow',
  'orange',
]

favoriteColors.sort()

console.log(favoriteColors)
// Output: ['blue', 'green', 'orange', 'red', 'yellow']
```

看到`blue`排在第一个，是因为它以字母‘b’开头，该字母在`green`的字母‘g’之前，以此类推。如果我们想按降序对数组元素排序，向`sort()`方法传递一个回调函数，该函数接收两个代表数组中两个元素的参数。如果第一个元素应该排在第二个元素之前，回调函数应返回负数；如果第一个元素应该排在第二个元素之后，则返回正数；如果元素的顺序不重要，则返回 0：

## 高阶函数 (HOFs) 与回调函数

```javascript
const famousBirthYears = [
  1990, 2001, 1989, 2023, 2005, 1993, 2020
]

famousBirthYears.sort((a, b) => b - a)

console.log(famousBirthYears)
// 输出: [2023, 2020, 2005, 2001, 1993, 1990, 1989]
```

在这个示例中，我们对`famousBirthYears`数组进行了降序排序。回调函数接受两个参数`a`和`b`，代表数组中的两个元素。由于我们想降序排列数组，因此我们返回`b - a`，使得第二个元素在第一个元素之前（即较大的数字在较小的数字之前）。如果我们想升序排列数组，我们将返回`a - b`，使得第一个元素在第二个元素之前（即较小的数字在较大的数字之前）：

```javascript
famousBirthYears.sort((a, b) => a - b)

console.log(famousBirthYears)
// 输出: [1989, 1990, 1993, 2001, 2005, 2020, 2023]
```

### reverse()

我们可以使用`reverse()`方法来反转数组中元素的顺序。`reverse`方法会修改原始数组。让我们来看一个示例：

```javascript
const agesOfStudents = [13, 10, 15, 12, 11, 14]

agesOfStudents.reverse()

console.log(agesOfStudents)
// 输出: [14, 11, 12, 15, 10, 13]
```

注意，`reverse()`方法并没有对数组元素进行排序。相反，它反转了从最后一个元素到第一个元素的顺序。

### reduce()

`reduce()`方法将数组减少为单个值。它遍历数组，对每个元素执行一个操作，并返回一个单一值。例如，如果我们想累加数字数组中的所有元素，可以使用`reduce()`方法：

```javascript
const participantPoints = [10, 20, 30, 40, 50]

const totalPoints = participantPoints.reduce(
  (a, b) => a + b
)

console.log(totalPoints)
// 输出: 150
```

`reduce()`方法接受一个带有两个参数`a`和`b`的回调函数，这两个参数代表数组中的两个元素。回调函数会从数组的第一个元素开始执行操作。在我们的示例中，我们将第一个元素加上第二个元素，然后将结果加上第三个元素，依此类推，直到我们得到总分。如果我们想减去数组中的元素，我们将返回`a - b`：

```javascript
const minusedPoints = participantPoints.reduce(
  (a, b) => a - b
)

console.log(totalPoints)
// 输出: -130
```

我们上面的示例执行了操作：`10 - 20 - 30 - 40 - 50`。我们可以使用相同的过程来乘以数组中的元素：

```javascript
const multipliedPoints = participantPoints.reduce(
  (a, b) => a * b
)

console.log(multipliedPoints)
// 输出: 12000000
```

这一次，我们将第一个元素乘以第二个元素，然后将结果乘以第三个元素，依此类推。`reduce()`方法不会修改原始数组。

我们还可以使用`reduce()`方法来拼接字符串数组中的元素：

```javascript
const favoriteDishes = ['jollof', 'burger', 'yam', 'meatloaf', 'pizza']

const favoriteDishes = favoriteDishes.reduce(
  (a, b) => a + ', ' + b
)

console.log(favoriteDishes)
// 输出: jollof, burger, yam, meatloaf, pizza
```

## 高阶函数 (HOFs) 和回调函数

两个参数：要执行的函数以及在执行该函数之前等待的毫秒数。让我们在5秒后显示一条消息：

```javascript
const displayMessage = () => {
  console.log('Hello, world!')
}

setTimeout(displayMessage, 5000)
// 输出: 2 (等待，原文写的是 "Output: 2" 和 "Output: Hello world!")
// 输出: Hello world!
```

1 秒是 1000 毫秒，5 秒是 5000 毫秒。`setTimeout()`方法将在等待 5 秒后执行`displayMessage()`函数。`setTimeout()`方法在调用后还会立即返回一个表示定时器 ID 的数字。我们可以使用这个 ID 来取消定时器。

首先，我们将`setTimeout`方法赋值给变量：

```javascript
const displayMessage = () => {
  console.log('Hello, world!')
}

const timerId = setTimeout(displayMessage, 5000)

console.log(timerId)
// 输出: 4 (可以是任意数字)
// 输出: Hello world!
```

这仍然会在 5 秒后显示消息，但现在我们在`timerId`变量中拥有了定时器的 ID。让我们在执行`displayMessage()`函数之前使用它取消定时器。我们将使用`clearTimeout()`方法来实现。`clearTimeout()`方法接收定时器的 ID 作为参数并取消定时器：

```javascript
const displayMessage = () => {
  console.log('Hello, world!')
}

const timerId = setTimeout(displayMessage, 5000)

clearTimeout(timerId)
```

`clearTimeout()`方法将在`displayMessage()`函数执行之前取消定时器。因此，当你运行这段代码时，`displayMessage()`函数将不会执行。

### setInterval()

`setInterval()`方法允许我们按固定间隔调度函数的执行。例如，如果我们想每 5 秒显示一次消息，可以使用`setInterval()`方法。`setInterval()`方法接收两个参数：要执行的函数以及在再次执行该函数之前等待的毫秒数。我们可以直接调用该方法，也可以将其赋值给变量。与`setTimeout()`方法一样，`setInterval()`方法也会返回一个表示定时器 ID 的数字。让我们使用`setInterval()`方法每 1 秒运行一次`displayMessage()`函数：

```javascript
const displayMessage = () => {
  console.log('Hello, world!')
}

const interVal = setInterval(displayMessage, 1000)
```

这将每隔 1 秒显示一次“Hello world!”。我们可以使用`clearInterval()`方法来取消定时器。`clearInterval()`方法接收定时器的 ID 作为参数并取消定时器：

```javascript
clearInterval(interVal)
```

运行`clearInterval()`方法将停止`displayMessage()`函数每秒执行一次。

## JavaScript 对象

假设你有一辆汽车，想要跟踪它的颜色、品牌、型号和里程数。你可以为这些属性各创建一个变量：

```javascript
const carColor = 'red'
const carMake = 'Tesla'
const carModel = 'Cybertruck'
const carMileage = 30
```

但如果你有 10 辆车呢？你必须为每辆车创建 4 个变量，总共 40 个变量。如果你想添加一个新属性呢？比如汽车使用的燃料类型？你必须创建 10 个新变量。随着你不断创建变量，将知道哪些变量是相互相关的或者它们属于哪辆车将变得越来越困难。

通过 JavaScript 对象，你可以将相关数据分组在单个变量中。因此，与其为第一辆车创建四个不同的变量，不如创建一个存储所有四个属性的变量。如果你想添加新属性，可以在不创建新变量的情况下完成。这里使用对象存储汽车数据看起来像是所示：

```javascript
const myCar = {
  color: 'red',
  make: 'Tesla',
  model: 'Cybertruck',
  mileage: 30,
}
```

在上面的示例中，我们创建了一个名为`myCar`的变量并给它赋值了一个对象。你可以通过包裹在周围的大括号来识别对象，后面跟着一个键值对列表。每个键值对都是对象的一个属性。在我们的示例中，第一个属性是汽车的颜色。它的键是`color`，值为 "red"。与变量声明不同，键和值之间用冒号隔开，每个属性之间用逗号分隔。

要访问对象的属性，可以使用点符号法（dot notation）或括号符号法（bracket notation）。点符号法是访问属性的最常用方法；首先，输入对象的名称，后跟一个点，然后是属性的名称。以下是使用点符号法访问`color`属性值的方法：

```javascript
console.log(myCar.color)
// 输出: "red"
```

这里是使用括号符号法的方法：

```javascript
console.log(myCar['color'])
```

当你想要访问一个名称存储在变量中的属性时，括号符号法非常有用。例如，让我们创建一个名为`propertyName`的变量并赋值字符串 "color"：

```javascript
const propertyName = 'color'

console.log(myCar[propertyName])
// 输出: "red"
```

### 创建对象的规则和指南

在创建对象时，有几点需要注意：

- **对象的属性名必须是唯一的**

  多个属性可以具有相同的值，但如果你尝试创建一个与现有属性同名的属性，新属性将覆盖旧属性。此外，如果一个对象有多个同名的属性，则只使用最后一个一个。

```javascript
const myFavoriteBook = {
  title: 'The Hobbit',
  title: 'The Lord of the Rings',
}

console.log(myFavoriteBook.title)
// 输出: "The Lord of the Rings"
```

- **属性名必须是字符串**

  当使用非字符串作为属性名时，它会被转换为字符串。例如，以下代码会创建一个名为 "1" 的属性：

```javascript
const myFavoriteDress = {
  1: "green"
}

console.log(myFavoriteDress.1) // 语法错误
```

尝试使用点符号法访问键 1 将导致语法错误，因为数字 1 不是合法的键。在这种情况下，你可以使用括号符号法访问它：

```javascript
// 1: "green"
```

- **无效的 JavaScript 标识符必须包含在引号中**

对象的键可以是任何字符串，包括空字符串。但是，如果键不是有效的 JavaScript 标识符，则必须包含在引号中。例如，在键中添加空格会导致语法错误：

```javascript
const myFavoriteMeal = {
  plate type: "ceramic"
} // 语法错误
```

但将键包含在引号中使其成为合法的属性名：

```javascript
const myFavoriteMeal = {
  "plate type": "ceramic",
  "": "valid but not recommended"
}

console.log(myFavoriteMeal["plate type"]) // 输出: "ceramic"

console.log(myFavoriteMeal[""]) // 输出: "valid but not recommended"
```

注意到我们使用了括号符号法来访问属性。当键包含空格或其他无效字符时，不能使用点符号法：

```javascript
const myFavoriteCar = {
  'engine*type': 'electric',
}

console.log(myFavoriteCar.engine * type) // 输出: NaN

console.log(myFavoriteCar['engine*type']) // 输出: "electric"
```

- **属性名大小敏感**

记住 JavaScript 是一种大小敏感的语言。这同样适用于属性。例如，以下代码会创建两个属性，一个名为 "title"，另一个名为 "Title"：

```javascript
const myFavoriteMovie = {
  title: 'Titanic',
  Title: 'The Lion King',
}

console.log(myFavoriteMovie.title) // 输出: "Titanic"

console.log(myFavoriteMovie.Title) // 输出: "The Lion King"
```

就像变量一样，在属性名上使用驼峰命名法（camelCase）是一个良好的习惯，可以使你的代码风格保持一致且易于阅读。

## JavaScript 对象

**属性值可以是任何有效的 JavaScript 表达式**

属性的值可以是任何有效的 JavaScript 表达式，包括函数。当函数被用作属性值时，它被称为方法（method），这就是为什么我们在提到像`console.log()`等内置 JavaScript 函数时，一直沿用“方法”这个词。

让我们创建一个带有名为`sayHello`方法的对象：

```javascript
const person = {
  fullName: 'Victor Otedola',
  sayHello: function () {
    console.log('Hello! My name is ' + this.name)
  },
}

person.sayHello()
// 输出: Hello! My name is Victor Otedola
```

在上面的示例中，我们创建了一个名为`person`的对象，它包含一个`fullName`属性和一个名为`sayHello`的方法。`sayHello`方法使用**this 关键字**来访问对象的`name`属性。在方法内部使用`this`关键字时，它指的是调用该方法的对象。在这种情况下，`this`指向`person`对象。

你也可以使用箭头函数作为方法，但`this`关键字的工作方式会有所不同；相反，它的值将由调用方法的上下文决定：

```javascript
const person2 = {
  fullName: 'Linda Chima',
  sayHello: () => {
    console.log('Hello! My name is ' + this.name)
  },
}

person2.sayHello()
// 输出: Hello! My name is undefined
```



`this`关键字的工作方式与第一个示例不同，因为它被用在了箭头函数。在这种情况下，`this`指向全局对象，而全局对象没有`name`属性。这可能会引起困惑，因此最好避免在箭头函数中使用`this`。

## 添加、修改和删除属性

你可以使用点表示法或括号表示法向对象添加新属性。让我们创建一个名为`student`的新对象并添加一个新属性`gender`（性别）：

```javascript
const student = {
  name: 'Kachi',
  age: 17,
}

student.gender = 'Male'
console.log(student)
// 输出: { name: "Kachi", age: 17, gender: "Male" }
```

以下是使用括号表示法添加新属性的方法：

```javascript
student['grade'] = 12
console.log(student)
// 输出: { name: "Kachi", age: 17, gender: "Male", grade: 12 }
```

你也可以使用点表示法和括号表示法来修改现有属性：

```javascript
student.age = 18
student['grade'] = 13
console.log(student.age) // 输出: 18
console.log(student.grade) // 输出: 13
```

JavaScript 有一个`Object.defineProperty()`方法用于向对象添加新属性。`Object.defineProperty()`方法是定义或修改对象上属性的一种。它用于控制属性的行为，并使其变为只读的（不可修改）、不可枚举的（不可遍历）或不可配置的（不可删除或修改）。以下是使用它向对象添加新属性的方法：

```javascript
Object.defineProperty(student, 'school', {
  value: 'University of Lagos',
  writable: false,
  enumerable: true,
  configurable: true,
})

console.log(student)
```

输出：

```json
{
  name: "Kachi",
  age: 18,
  gender: "Male",
  grade: 13,
  school: "University of Lagos"
}
```

第一个参数是要添加属性的对象。第二个参数是属性名。第三个参数是一个包含属性属性的对象。`value`属性是必须，它指定了属性的值。`writable`（可写）、`enumerable`（可枚举）和`configurable`（可配置）属性是可选的。如果不指定，将默认为`false`。注意，我们将`school`属性的`writable`属性设置为`false`，因此更改它的值将无效：

```javascript
student.school = 'Havard University'
console.log(student.school)
// 输出: "University of Lagos"
```

要删除属性，你可以使用`delete`关键字：

```javascript
delete student.school
console.log(student.school)
// 输出: undefined
```

尝试使用`Object.defineProperty()`为`student`对象添加一个无法删除的新属性：

```javascript
Object.defineProperty(student, 'language', {
  value: 'English',
  writable: true,
  enumerable: true,
  configurable: false,
})

console.log(student.language)
// 输出: "English"

delete student.language
console.log(student.language)
// 输出: "English"
```

`configurable`属性被设置为`false`，因此`language`属性无法被删除。

## Object.prototype

在 JavaScript 中，每个对象都有一个原型（prototype）。当你创建一个对象时，它会继承一个原型，原型是一个包含了你可以在主对象上使用的其他内置属性和方法的对象。例如，每个对象都有一个`toString()`方法，可以返回对象的字符串表示，即使你没有手动添加它：

```javascript
const computerInfo = {
  brand: 'Apple',
  model: 'MacBook Pro',
  color: 'Silver',
}

console.log(computerInfo.toString())
// 输出: [object Object]
```

对象的默认字符串表示是`[object Object]`。如果你想获取对象的字符串表示，可以使用`JSON.stringify()`方法：

```javascript
JSON.stringify(computerInfo)
// 输出: {"brand":"Apple","model":"MacBook Pro","color":"Silver"}
```

每个对象的原型都包含了你可以在主对象上使用的其他内置属性和方法。例如，每个对象都有一个`toString()`方法，即使你没有手动添加它：

```javascript
const computerInfo = {
  brand: 'Apple',
  model: 'MacBook Pro',
  color: 'Silver',
}

console.log(computerInfo.toString())
// 输出: [object Object]
```

每个对象的原型都包含了你可以在主对象上使用的其他内置属性和方法。例如，每个对象都有一个`toString()`方法，即使你没有手动添加它：

```javascript
const computerInfo = {
  brand: 'Apple',
  model: 'MacBook Pro',
  color: 'Silver',
}

console.log(computerInfo.toString())
// 输出: [object Object]
```

每个对象的原型都包含了你可以在主对象上使用的其他内置属性和方法。例如，每个对象都有一个`toString()`方法，即使你没有手动添加它：

```javascript
const computerInfo = {
  brand: 'Apple',
  model: 'MacBook Pro',
  color: 'Silver',
}

console.log(computerInfo.toString())
// 输出: [object Object]
```

每个对象的原型都包含了你可以在主对象上使用的其他内置属性和方法。例如，每个对象都有一个`toString()`方法，即使你没有手动添加它：

```javascript
const computerInfo = {
  brand: 'Apple',
  model: 'MacBook Pro',
  color: 'Silver',
}

console.log(computerInfo.toString())
// 输出: [object Object]
```

每个对象的原型都包含了你可以在主对象上使用的其他内置属性和方法。例如，每个对象都有一个`toString()`方法，即使你没有手动添加它：

```javascript
const computerInfo = {
  brand: 'Apple',
  model: 'MacBook Pro',
  color: 'Silver',
}

console.log(computerInfo.toString())
// 输出: [object Object]
```

每个对象的原型都包含了你可以在主对象上使用的其他内置属性和方法。例如，每个对象都有一个`toString()`方法，即使你没有手动添加它：

```javascript
const computerInfo = {
  brand: 'Apple',
  model: 'MacBook Pro',
  color: 'Silver',
}

console.log(computerInfo.toString())
// 输出: [object Object]
```

每个对象的原型都包含了你可以在主对象上使用的其他内置属性和方法。例如，每个对象都有一个`toString()`方法，即使你没有手动添加它：

```javascript
const computerInfo = {
  brand: 'Apple',
  model: 'MacBook Pro',
  color: 'Silver',
}

console.log(computerInfo.toString())
// 输出: [object Object]
```

每个对象的原型都包含了你可以在主对象上使用的其他内置属性和方法。例如，每个对象都有一个`toString()`方法，即使你没有手动添加它：

```javascript
const computerInfo = {
  brand: 'Apple',
  model: 'MacBook Pro',
  color: 'Silver',
}

console.log(computerInfo.toString())
// 输出: [object Object]
```

每个对象的原型都包含了你可以在主对象上使用的其他内置属性和方法。例如，每个对象都有一个`toString()`方法，即使你没有手动添加它：

```javascript
const computerInfo = {
  brand: 'Apple',
  model: 'MacBook Pro',
  color: 'Silver',
}

console.log(computerInfo.toString())
// 输出: [object Object]
```

每个对象的原型都包含了你可以在主对象上使用的其他内置属性和方法。例如，每个对象都有一个`toString()`方法，即使你没有手动添加它：

```javascript
const computerInfo = {
  brand: 'Apple',
  model: 'MacBook Pro',
  color: 'Silver',
}

console.log(computerInfo.toString())
// 输出: [object Object]
```

## Object 方法

Object 对象中有很多常用的方法，但你可以在 MDN 文档中找到更多。

### keys()

`Object.keys()`返回给定对象的可枚举属性名的数组。获取`computerInfo`的键：

```javascript
Object.keys(computerInfo)
// 输出: ["brand", "model", "color"]
```

### values()

`Object.values()`返回给定对象的可枚举值的数组。获取`computerInfo`的值：

```javascript
Object.values(computerInfo)
// 输出: ["Apple", "MacBook Pro", "Silver"]
```

### entries()

`Object.entries()`返回给定对象的可枚举属性 [键，值] 对数组。在返回值中，每个元素都是包含属性名和值的数组。

```javascript
Object.entries(computerInfo)
// 输出: [["brand", "Apple"], ["model", "MacBook Pro"], ["color", "Silver"]]
```

### assign()

`Object.assign()`方法将一个或多个源对象的可枚举属性拷贝到目标对象。它返回修改后的目标对象。让我们创建一个名为`newComputerInfo`的对象并将`computerInfo`的属性复制到它：

```javascript
const newComputerInfo = Object.assign({}, computerInfo)

console.log(newComputerInfo)
// 输出: {brand: "Apple", model: "MacBook Pro", color: "Silver"}
```

### freeze()

`Object.freeze()`冻结对象使其无法修改。让我们冻结`computerInfo`对象并尝试修改它：

```javascript
Object.freeze(computerInfo)

computerInfo.brand = 'Dell'

console.log(computerInfo.brand)
// 输出: "Apple"
```

### seal()

`Object.seal()`方法密封对象，防止添加新属性并将所有现有属性标记为不可配置。让我们密封`computerInfo`对象并尝试向其添加新属性：

```javascript
Object.seal(computerInfo)

computerInfo.price = 200000

console.log(computerInfo.price)
// 输出: undefined
```

掌握这些方法对于精通 JavaScript 对象至关重要。因此，请确保你继续练习，直到对它们感到熟悉为止。

参考文档：https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object

## JavaScript 对象

### 对象解构

对象解构是访问对象属性的另一种方法。通过解构，我们可以从对象中提取值并将它们赋值给与对象属性同名的变量。这是通过在赋值运算符`=`的左侧用大括号`{}`包裹属性来实现的。让我们来看一个例子。首先，我们先创建一个存储会议参与者信息的对象：

```javascript
const attendee = {
  name: 'Peter Okoye',
  age: 30,
  email: 'peterokoye@nonexistentmail.com',
  ticketType: 'VIP',
}
```

现在，让我们使用解构来访问`attendee`对象的属性：

```javascript
const { name, age, email, ticketType } = attendee;

console.log(name)
// 输出: "Peter Okoye"

console.log(age)
// 输出: 30

console.log(email)
// 输出: "peterokoye@nonexistentmail.com"

console.log(ticketType)
// 输出: "VIP"
```

我们不需要一次性解构对象的所有属性。我们可以只解构我们需要的属性：

```javascript
const { name } = attendee;
```

如果对象没有该属性，我们还可以为变量分配默认值：

```javascript
const { name, isPaid = false } = attendee;

console.log(isPaid)
// 输出: false
```

我们可以通过使用冒号`:`在属性名后加上新名称来为变量指定不同的名称。这在我们想要避免命名冲突时非常有用：

```javascript
const { name: attendeeName } = attendee;

console.log(attendeeName)
// 输出: "Peter Okoye"
```

### 数组解构

我们同样可以类似地解构数组。让我们创建一个存储会议参与者姓名的数组：

```javascript
const attendeeNames = [
  'Peter Okoye',
  'Paul Okoye',
  'Lynda Okoye',
  'Rita Okoye',
]
```

要解构数组，我们需要在赋值运算符`=`的左侧用方括号`[]`包裹元素。由于数组元素没有名称，我们只能按照它们在数组中出现的顺序进行解构。因此，数组的第一个元素将赋值给第一个变量，第二个元素赋值给第二个变量，依此类推。让我们解构`attendeeNames`数组：

```javascript
const [
  firstAttendee,
  secondAttendee,
  thirdAttendee,
  fourthAttendee
] = attendeeNames;

console.log(firstAttendee)
// 输出: "Peter Okoye"

console.log(thirdAttendee)
// 输出: "Lynda Okoye"
```

我们也可以通过用逗号`,`跳过不需要的元素来只解构我们需要的元素。让我们跳过数组的第二个元素：

```javascript
const [firstAttendee, , thirdAttendee] = attendeeNames;
```



对象和数组解构可以通过简化从对象和数组中提取值并将其赋值给变量的过程，使代码更加简洁简洁。尽管如此，是否使用对象和数组解构取决于具体的用法和个人偏好。在某些情况下，可能是没必要的，但在大多数你发现反复使用对象属性或将其赋值给变量的情况下，考虑解构是一个好主意。

## 条件语句

我们已经学习了基本的条件语句以及如何使用 `if-else` 语句根据条件执行代码。条件语句用于控制程序的流程，就像我们过日常生活一样。你根据自己的情况做决定并相应执行不同的操作。例如，如果你觉得冷，你可能会穿外套；如果在下雨，你可能会穿雨衣；如果天气晴，你可能会穿T恤。你可以使用基础的`if-else`语句处理第一个条件（如果冷的话），但当你需要检查多个条件时，你需要更复杂的条件语句，如`else if`和`switch`语句。

### JavaScript 中的 else-if 语句

要检查多个条件，可以使用`else if`子句。`else if`子句允许你将多个条件语句链在一起，使得如果第一个条件不满足，就会检查第二个条件，依此类推。这里有一个说明`else if`子句如何工作的简单示例：

```text
如果冷：穿外套
否则如果在下雨：穿雨衣
否则：穿T恤
```

让我们来看一个 JavaScript 示例。我们将使用`console.log()`方法在满足条件时在控制台上输出显示文本：

```javascript
if (weather === 'cold') {
  console.log("wear a jacket");
} else if (weather === 'raining') {
  console.log("wear a raincoat");
} else {
  console.log("wear a t-shirt");
}
```

### 嵌套条件语句

当需要在一个条件内部检查另一个条件时，可以使用嵌套条件语句。下面是一个示例：

```javascript
let laptopWorks = true
let batteryLow = true
let internetUnavailable = true
let batteryIsCharged = false

if (laptopWorks) {
  if (batteryLow) {
    console.log('Charge it')
  } else if (internetUnavailable) {
    console.log('Restart the router')
  } else if (batteryIsCharged) {
    console.log('Use it')
  }
}

//输出: Charge it
```

由于所有条件都取决于电脑是否正常工作，我们只需要写一次。如果电脑正常工作，就会评估嵌套条件。然而，如果电脑无法工作，则任何嵌套条件都不会被评估。让我们将`laptopWorks`的值改为`false`并再次运行代码：

```javascript
laptopWorks = false

if (laptopWorks) {
  if (batteryLow) {
    console.log('Charge it')
  } else if (internetUnavailable) {
    console.log('Restart the router')
  } else if (batteryIsCharged) {
    console.log('Use it')
  }
}

//输出: (nothing)
```

在嵌套时，你应该始终对嵌套条件进行缩进，以使你的代码更易读。如果你想处理电脑无法工作的情况，可以为父条件添加一个`else`子句：

```javascript
if (laptopWorks) {
  if (batteryLow) {
    console.log('Charge it')
  } else if (internetUnavailable) {
    console.log('Restart the router')
  } else if (batteryIsCharged) {
    console.log('Use it')
  }
} else {
  console.log('The laptop is broken. It needs fixing')
}

//输出: The laptop is broken. It needs fixing
```

在编写条件语句时，如果条件内部只有一个语句，可以省略大括号：

```javascript
if (laptopWorks) {
  if (batteryLow) console.log('Charge it')
  else if (internetUnavailable)
    console.log('Restart the router')
  else if (batteryIsCharged) console.log('Use it')
} else {
  console.log('The laptop is broken. It needs fixing')
}
```

我们也可以不带大括号地写`else`子句，但在这种情况下使用大括号更易读。在编写代码时，将可读性优先于简洁是非常重要的。

### switch 语句

`switch`语句是一种简化编写多个`if-else`语句过程的方法。它是条件语句的一种，允许你将值与多个情况进行比较。`switch`语句将表达式与可能值的列表进行比较，如果表达式匹配其中一个值，将执行对应`case`内部的代码。其语法如下：

```javascript
switch (expression) {
  case value1:
    // 如果表达式匹配 value1 则执行的代码
    break
  case value2:
    // 如果表达式匹配 value2 则执行的代码
    break
  default:
    // 如果表达式不匹配任何情况则执行的代码
    // 任何情况
}
```

在上述语法中：

- 表达式（`expression`）是将与情况进行比较的值。
- `value1`和`value2`是表达式可能匹配的值。
- `break`关键字用于在执行完`case`内的代码后停止`switch`语句的执行。如果`case`中没有`break`关键字，`switch`语句将继续运行直到遇到`break`关键字或结束。
- 如果表达式不匹配任何`case`，则执行`default`情况。

为了说明`switch`语句的工作原理，让我们来看一个例子。假设我们有一个名为`day`的变量，存储星期，我们想根据星期向控制台打印不同的消息。我们可以使用`if-else`语句来实现这一点：

```javascript
const day = 'Monday'

if (day === 'Monday') {
  console.log('Today is Monday!')
} else if (day === 'Tuesday') {
  console.log('Today is Tuesday!')
} else if (day === 'Wednesday') {
  console.log('Today is Wednesday!')
} else if (day === 'Thursday') {
  console.log('Today is Thursday!')
} else if (day === 'Friday') {
  console.log('Today is Friday!')
} else if (day === 'Saturday') {
  console.log('Today is Saturday!')
} else if (day === 'Sunday') {
  console.log('Today is Sunday!')
} else {
  console.log('That is not a day of the week!')
}

//输出: Today is Monday!
```

这段代码可以工作，但我们可以通过使用`switch`语句来简化它：

```javascript
const day = 'Monday'

switch (day) {
  case 'Monday':
    console.log('Today is Monday!')
    break
  case 'Tuesday':
    console.log('Today is Tuesday!')
    break
  case 'Wednesday':
    console.log('Today is Wednesday!')
    break
  case 'Thursday':
    console.log('Today is Thursday!')
    break
  case 'Friday':
    console.log('Today is Friday!')
    break
  case 'Saturday':
    console.log('Today is Saturday!')
    break
  case 'Sunday':
    console.log('Today is Sunday!')
    break
  default:
    console.log('That is not a day of the week!')
}

//输出: Today is Monday!
```

### 嵌套 switch 语句

在检查值的多个情况时，`switch`语句通常比`if-else`语句更高效，因为它需要的代码更少且更易读。但并非总是如此。如果你处理多个条件，`switch`语句可能会变得难以管理。例如，如果你想使用变量`day`和`month`来检查是否为一月份的一个工作日，你可以这样编写嵌套的`switch`语句：

```javascript
const day = 'Monday'
const month = 'January'

switch (day) {
  case 'Monday':
    switch (month) {
      case 'January':
        console.log('Today is a weekday in January!')
        break
      default:
        console.log('Today is a weekday!')
    }
    break
  default:
    console.log('That is not a day of the week!')
}

//输出: Today is a weekday in January!
```

在上面的示例中：
第一个`case`检查`day`是否为'Monday'；如果是，它进入内部`switch`语句检查变量`month`。内部`switch`语句检查`month`是否为'January'，如果是，它向控制台打印"Today is a weekday in January!"并使用`break`语句退出`switch`语句。如果`month`不是'January'，它向控制台打印"Today is a weekday!"。

虽然这段代码可以工作，但它不可读。嵌套的`switch`语句难以理解，编写时很容易出错。这就是为什么在这种情况下使用`if-else`语句更好：

```javascript
const day = 'Monday'
const month = 'January'

if (day === 'Monday' && month === 'January') {
  console.log('Today is a weekday in January!')
} else {
  console.log('That is not a day of the week!')
}

//输出: Today is a weekday in January!
```

当你需要嵌套`switch`语句时，最好考虑改用`if-else`语句。编写复杂的`switch`语句很容易导致代码出现错误。

需要注意的是，`switch`语句并不限于检查相等性。你也可以用它检查其他条件。例如，你可以使用`switch`语句检查数字是否大于或小于某个值：

```javascript
const num = 5

switch (num) {
  case num > 5:
    console.log('num is greater than 5')
    break
  case num < 5:
    console.log('num is less than 5')
    break
  default:
    console.log('num is equal to 5')
}

// output: num is equal to 5
```

这种方法较少用，但在某些情况下非常有用。如果你觉得`switch`语句很困惑，使用`if-else`语句也是可以的。

记住始终在每个`case`之后包含一个`break`关键字。否则，即使找到了第一个匹配项，`switch`语句也会继续执行剩余`case`的代码块：

```javascript
const day = 'Monday'

switch (day) {
  case 'Monday':
    console.log('Today is Monday!')
  case 'Tuesday':
    console.log('Today is Tuesday!')
  case 'Wednesday':
    console.log('Today is Wednesday!')
  case 'Thursday':
    console.log('Today is Thursday!')
  case 'Friday':
    console.log('Today is Friday!')
  case 'Saturday':
    console.log('Today is Saturday!')
  case 'Sunday':
    console.log('Today is Sunday!')
  default:
    console.log('That is not a day of the week!')
}

// output: Today is Monday!
// output: Today is Tuesday!
// output: Today is Wednesday!
// output: Today is Thursday!
// output: Today is Friday!
// output: Today is Saturday!
// output: Today is Sunday!
// output: That is not a day of the week!
```

当`case`简单且定义明确时，`switch`语句通常更有结构化且易于阅读。然而，`switch`语句还是`if-else`语句更高效取决于具体的用例。

### 三元运算符

三元运算符是编写`if-else`语句的简写方式。它是一个条件运算符，接受三个操作数：一个条件、一个条件为真时执行的表达式，以及一个条件为假时执行的表达式。语法如下：

```javascript
condition ? expression1 : expression2
```

要使用三元运算符，你首先写一个条件，后面跟着一个问号（`?`）。然后，写一个在条件为真时执行的表达式。最后，你写一个冒号（`:`）和一个在条件为假时执行的表达式。冒号代表`else`子句，在三元运算符中是必需的。

让我们看一个使用存储年龄变量的示例。我们想根据人的年龄在控制台打印一个字符串。如果此人18岁或以上，我们将打印"You can vote"；如果小于18岁，我们将打印"You can't vote"。首先，我们使用`if-else`语句来实现：

```javascript
let age = 18

if (age >= 18) {
  console.log('You can vote')
} else {
  console.log("You can't vote")
}

// output: You can vote
```

这是我们使用三元运算符实现：

```javascript
let age = 18

age >= 18
  ? console.log('You can vote')
  : console.log("You can't vote")

// output: You can vote
```

三元运算符比`if-else`语句短得多，但在这种情况下可能难以阅读。它主要用于根据条件为变量赋值：

```javascript
let age = 18

let canVote = age >= 18 ? true : false

console.log(canVote)

// output: true
```

看到这里三元运算符在这里要易读得多。在处理简单条件时，它是简化代码的极佳方法。

你还可以嵌套三元运算符：

```javascript
let score = 80

let grade = score >= 90 ? 'A' : score >= 80 ? 'B' : 'C'

console.log(grade)
```



*// output: B*

在上面的例子中，三元运算符显然更易读。但是，嵌套三元运算符会使代码变得难以维护。如果你发现自己正在这样做，请考虑使用嵌套的 `if-else` 语句：

（注：原文提供的示例代码似乎不完整，根据逻辑补充如下）

```javascript
let score = 80
let grade = score >= 90 ? 'A' : score >= 80 ? 'B' : 'C'
console.log(grade)
```

*// output: B*

## 循环

`if` 语句检查 `i` 的当前值是否等于 5。如果是，则执行 `continue` 语句，它会跳过循环中的剩余代码并继续下一次迭代。

### break 关键字

`break` 关键字用于退出循环。因此，如果我们想在 `i` 等于 5 时停止循环，可以使用 `break` 关键字：

```javascript
for (let i = 1; i <= 10; i++) {
  if (i === 5) {
    break
  }
  console.log(i)
}
```

输出：

```
1
2
3
4
```

由于 `break` 语句在 `i` 等于 5 时结束了循环，因此在该迭代中不会执行 `console.log()` 语句。所以我们只在控制台中打印了从 1 到 4 的数字。

### for...in 循环

`for...in` 循环用于遍历对象的可枚举属性。如果我们有一个包含属性列表的对象，并且想要访问每个属性，可以使用 `for` 循环来遍历对象的属性，如下所示：

```javascript
let person = {
  name: 'Jane',
  age: 27,
  city: 'Kigali',
}

for (let i = 0; i < Object.keys(person).length; i++) {
  console.log(
    `${Object.keys(person)[i]}: ${person[Object.keys(person)[i]]}`
  )
}
```

虽然这种方法可行，但并不易读。我们可以使用 `for...in` 循环用更简洁的方式编写相同的代码。通过 `for...in` 循环，我们可以直接访问对象的键，而不需要使用 `Object.keys()` 方法：

```javascript
let person = {
  name: 'Jane',
  age: 27,
  city: 'Kigali',
}

for (let key in person) {
  console.log(`${key}: ${person[key]}`)
}
```

输出：

```
name: Jane
age: 27
city: Kigali
```

在上面的示例中，我们声明了一个名为 `key` 的变量，并使用 `in` 运算符将其赋值为 `person` 对象中每个属性的值。然后我们使用 `key` 变量来访问 `person` 对象中每个属性的值。JavaScript 中的 `in` 运算符用于检查指定的属性是否存在于对象中。我们也可以在循环外部使用它：

```javascript
let person = {
  name: 'Jane',
  age: 27,
  city: 'Kigali',
}

if ('name' in person) {
  console.log('The person object has a name property.')
}

// 输出: The person object has a name property.
```

我们也可以用它来检查元素是否存在于数组：

```javascript
let fruits = ['apple', 'banana', 'orange']

if ('apple' in fruits) {
  console.log(
    'The apple element exists in the fruits array.'
  )
}

// 输出: The apple element exists in the fruits array.
```

由于我们可以在数组上使用 `in` 运算符，也可以使用 `for...in` 循环来遍历数组的元素：

```javascript
let names = ['Jane', 'John', 'Ada']

for (let index in names) {
  console.log(names[index])
}
```

输出：

```
Jane
John
Ada
```

当使用 `for...in` 循环遍历数组时，赋值给 `in` 运算符的变量将是数组每个元素的索引。遍历数组元素的更简单方法是使用 `for...of` 循环。

### for...of 循环

`for...of` 循环与 `for...in` 循环类似，但它遍历数组的值而不是索引。让我们使用 `for...of` 循环重写 `names` 循环示例：

```javascript
let names = ['Jane', 'John', 'Ada']

for (let name of names) {
  console.log(name)
}
```

输出：

```
Jane
John
Ada
```

在使用 `for...of` 循环访问数组元素时，赋值给 `of` 运算符的变量将是数组每个元素的值。我们还可以使用 `for...of` 循环来遍历字符串的字符：

```javascript
let name = 'Jane'

for (let character of name) {
  console.log(character)
}
```

输出：

```
J
a
n
e
```

在处理数组时，`for...of` 循环比 `for...in` 循环更易读和理解。然而，我们不能像使用 `for...in` 循环那样用 `for...of` 循环直接访问对象的属性。

### while 循环

`while` 循环类似于 `for` 循环，但没有没有表达式。它用于我们不知道循环将运行多少次。例如，如果我们有一个骰子游戏，不断掷骰子直到出现 6。我们可能在第一次就掷出 6，也可能需要 10 次。由于我们不知道运行多少次，所以不能使用 `for` 循环。使用 `while` 循环，只要值不是 6，就可以一直掷骰子。用通白的话说，`while` 循环写法如下：

当骰子的值不为 6 时，一直掷骰子。让我们看看如何编写 `while` 循环。当骰子的值不为 6 时，掷骰子。使用 `Math.ceil()` 方法将数字四舍五入到整数。首先创建一个变量 `dieRoll`，然后使用 `while` 循环来更新它的值，直到得到 6：

```javascript
let dieRoll = 0

while (dieRoll !== 6) {
  dieRoll = Math.ceil(Math.random() * 6)
  console.log(`You rolled a ${dieRoll}`)
}
```

取决于得到 6 需要多少次，代码应该返回如下（但数字是随机的）：

```
You rolled a 2
You rolled a 4
You rolled a 3
```

如果第一次就是 6，循环运行一次。如果需要 10 次，循环就会运行 10 次。`while` 循环只要条件成立就会继续运行。在这种情况下，条件是 `dieRoll` 不等于 6。在 `while` 循环中，在运行之前检查条件。如果在声明时给 `dieRoll` 赋值为 6，循环将不会运行，因为条件从开始就是假的：

```javascript
let dieRoll = 6

while (dieRoll !== 6) {
  dieRoll = Math.ceil(Math.random() * 6)
  console.log(`You rolled a ${dieRoll}`)
}
```

在 `while` 循环中，我们必须确保条件最终会被满足。否则，循环将无限运行。看到我们在每次迭代中是如何更新 `dieRoll` 的。如果不这样做，第一个示例中的 `dieRoll` 将始终为 0，条件 `dieRoll !== 6` 将始终为真，导致循环无限运行。循环无限运行时，被称为死循环。

让我们尝试移除更新 `dieRoll` 的行。运行这样的死循环会导致浏览器冻结，请将光标靠近 X 按钮（关闭标签页）以便防止浏览器崩溃：

```javascript
let dieRoll = 0

while (dieRoll !== 6) {
  console.log(`You rolled a ${dieRoll}`)
}
```

### do...while 循环

`do...while` 循环类似于 `while` 循环，但与 `while` 循环不同，它是在运行之后检查条件。这意味着循环至少运行一次。因此，在我们骰子游戏的第二个示例中，即使声明时给 `dieRoll` 赋值为 6，`do...while` 循环也会运行一次：

```javascript
let dieRoll = 6

do {
  dieRoll = Math.ceil(Math.random() * 6)
  console.log(`You rolled a ${dieRoll}`)
} while (dieRoll !== 6)
```

### 数字猜数字游戏

`do...while` 循环在我们希望至少运行一次循环，无论条件如何时非常有用。让我们创建一个猜数字游戏，让用户猜 1 到 10 之间的数字。我们将使用 `Math` 方法生成一个 1 到 10 之间的随机数，然后让用户猜数字。如果他们猜对了，游戏就会结束，我们会祝贺他们。如果他们猜错

循环

120

如果猜错了，我们会让他们再次猜一次。我们可以使用 `prompt()` 方法获取用户的输入，这是一个内置的浏览器函数，会显示一个带有文本输入字段的对话框。我们将使用 `do...while` 循环来让用户不断猜数字，直到他们猜对为止：

```javascript
let correctNumber = Math.ceil(Math.random() * 10)
let guess = 0

do {
  guess = prompt('Guess a number between 1 and 10')
  if (guess == correctNumber) {
    alert('You guessed the correct number!')
  } else {
    alert('Sorry, that was incorrect. Try again.')
  }
} while (guess != correctNumber)
```

在这个示例中，我们首先生成一个 1 到 10 之间的随机数，并将其赋值给 `correctNumber` 变量。然后，我们声明一个变量来存储用户的猜测，并将其赋值为 0。我们使用 `do...while` 循环来让用户不断猜数字，直到他们猜对为止。

在循环内部，我们使用 `prompt()` 方法让用户猜数字。将 `prompt()` 方法的结果赋值给 `guess` 变量，会将用户的输入存储在该变量中。

然后，我们检查用户的猜测是否等于正确数字。如果是，我们就祝贺他们并结束循环。如果不是，我们就告诉他们猜错了，并让他们再次猜一次。`alert()` 方法是另一个内置的浏览器函数，会显示一个带有消息的简单对话框。`do...while` 循环确保循环体代码在检查条件之前至少执行一次。因此，即使我们使用 `correctNumber` 变量作为 `guess` 的值，用户仍然会被要求再次猜数字：

```javascript
let correctNumber = Math.ceil(Math.random() * 10)
let guess = correctNumber

do {
  guess = prompt('Guess a number between 1 and 10')
  if (guess == correctNumber) {
    alert('You guessed the correct number!')
  } else {
    alert('Sorry, that was incorrect. Try again.')
  }
} while (guess != correctNumber)
```

另一方面，如果如果我们使用 `while` 循环，用户永远不会被要求猜数字，因为条件从开始就是虚假的：

```javascript
let correctNumber = Math.ceil(Math.random() * 10)
let guess = correctNumber

while (guess != correctNumber) {
  guess = prompt('Guess a number between 1 and 10')
  if (guess == correctNumber) {
    alert('You guessed the correct number!')
  } else {
    alert('Sorry, that was incorrect. Try again.')
  }
}
```

我们可以通过将 `guess` 变量初始化为 0 来修复这个问题。然而，如果 `correctNumber` 变量声明中的表达式最初返回的是 0，那么 `while` 循环仍然不会运行。

请注意，我们使用了普通相等运算符 (`==`) 来检查用户的猜测是否等于正确数字，而不是使用严格相等运算符 (`===`)。这是因为 `prompt()` 方法返回的是一个字符串，而 `correctNumber` 变量是一个数字。由于严格相等运算符会检查类型和值是否相同，如果我们使用它，条件将始终为虚假。

值得注意的是，`alert()` 和 `prompt()` 方法被认为是阻塞性方法，这意味着代码执行将停止，直到对话框关闭。在对话框打开期间，我们无法与网页进行交互或使用浏览器控制台。我们将在后面的章节中讨论其他获取用户输入和显示消息的非阻塞方法。

在进入下一节之前，尝试自己重写每个示例，以更深入地理解循环的工作原理。此外，你还可以尝试使用循环以及 `prompt()` 和 `alert()` 方法创建另一个交互游戏来挑战自己。这不仅能帮助你更熟悉循环，还能提高你的 JavaScript 技能。

## 文档对象模型 (DOM)

文档对象模型 (DOM) 是网页的面向对象的表示，页面上的每个元素（如按钮、图像或文本）都表示为一个对象，该对象拥有自己的一组属性和方法。DOM 是 HTML 和 XML 文档的编程接口，允许我们使用 JavaScript 来访问和更新网页的内容、结构和样式。

通过 DOM，我们可以监听事件（例如点击按钮）并对其做出响应。我们还可以创建新的元素和属性，更改现有元素的内容，或从页面中删除元素。

DOM 将文档表示为节点树。“节点”一词指的是数据结构中的单个点，在 DOM 的情况下，它代表网页上的一个元素或一段文本。每个节点都是一个代表文档一部分的对象。DOM 的树形结构由节点之间的父子关系形成，每个元素包含其他元素，这些元素可以被视为子节点。

例如，在 HTML 文档中，一个节点代表一个元素，例如段落 `<p>Hello World</p>`，而文本“Hello World”是段落节点的子节点。节点提供了一种以逻辑和分级方式（从页面顶部到底部）表示网页的方法，使得导航和理解文档结构变得简单。

让我们一个简单的 HTML 文档：

| | |
|---|---|
| 1 | `<!DOCTYPE html>` |
| 2 | `<html>` |
| 3 | `<head>` |
| 4 | `<title>My Simple Web Page</title>` |
| 5 | `</head>` |
| 6 | `<body>` |
| 7 | `<h1>This is awesome!</h1>` |
| 8 | `</body>` |
| 9 | `</html>` |

上述文档的 DOM 树看起来如下：

| | |
|---|---|
| 1 | Document |
| 2 | html |
| 3 | head |
| 4 | title |
| 5 | /head |
| 6 | body |
| 7 | h1 |
| 8 | /body |
| 9 | /html |
| 10 | doctype |
| 11 | html |
| 12 | head |
| 13 | title |
| 14 | body |
| 15 | h1 |

## 访问 DOM

浏览器提供了一个名为 `document` 的全局对象来表示 DOM，我们可以用它来访问网页的所有元素。例如，访问访问元素，可以使用 `title` 属性。在浏览器控制台中输入以下代码：

`document.title`

这将返回文本“My Web Page”。文档对象的 `title` 属性是标题元素的引用。我们还可以通过 `head` 和 `body` 属性来访问头部和主体元素：

| | |
|---|---|
| 1 | `document.head` |
| 2 | *// Output: `<head>...</head>`* |
| 3 | |
| 4 | `document.body` |
| 5 | *// Output: `<body>...</body>`* |

### getElementsByTagName 方法

`document` 对象有一个 `getElementsByTagName` 方法，可以通过标签名来访问元素。该方法接受一个字符串参数，即标签名称。要访问 `h1` 元素，在控制台中输入以下代码：



`document.getElementsByTagName('h1')`

这将返回一个包含`h1`元素引用的`HTMLCollection`。`HTMLCollection`是一个包含网页元素引用的数组对象。当我们使用`getElementsByTagName`方法时，它会返回一个按层次顺序包含所有指定标签元素的`HTMLCollection`。由于我们的文档中只有一个`h1`元素，`HTMLCollection`只包含一个元素。控制台输出如下：

```
HTMLCollection[h1]
```

如果我们有两个`h1`元素，`HTMLCollection`将包含两个元素：

```
HTMLCollection[(h1, h1)]
```

要访问`HTMLCollection`中的`h1`元素，我们可以使用括号表示法，就像处理数组一样：

```
document.getElementsByTagName('h1')[0]
```

这将返回`h1`元素：

```
<h1>Using JavaScript to access the DOM</h1>
```

我们也可以通过使用`HTMLCollection`的`item`方法来访问`h1`元素，该方法接受索引作为参数：

```
document.getElementsByTagName('h1').item(0)
// 输出: <h1>Using JavaScript to access the DOM</h1>
```

现在我们已经可以访问`h1`元素，可以使用`textContent`或`innerText`属性来获取`h1`元素的文本内容：

```
document.getElementsByTagName('h1')[0].textContent
// 输出: "Using JavaScript to access the DOM"

document.getElementsByTagName('h1')[0].innerText
// 输出: "Using JavaScript to access the DOM"
```

`textContent`和`innerText`属性用于获取或设置HTML元素的文本内容。`innerText`属性会考虑应用到文本上的样式（例如可见性），如果文本被CSS隐藏，则不会返回该文本；而`textContent`属性无论应用了什么样式，都会返回文本。

由于DOM属性依赖于浏览器，某些浏览器在特定情况下可能会返回不同的结果，或者对这些属性的支持程度不同。但总的来说，这些属性在不同浏览器中的行为是相似的。

让我们使用`textContent`属性来更改`h1`元素的文本。在控制台中输入以下代码：

```
document.getElementsByTagName('h1')[0].textContent = 'DOM Manipulation'
// 输出: DOM Manipulation
```

这将`h1`元素的文本更改为“DOM Manipulation”。

我们将`h1`元素赋值给变量，这样每次访问它时就不需要重复输入`document.getElementsByTagName('h1')[0]`：

```
const pageHeading = document.getElementsByTagName('h1')[0]

console.log(pageHeading.textContent)
// 输出: DOM Manipulation
```

现在，我们可以使用`pageHeading`变量访问`h1`元素并更改它的文本。这次使用`innerText`属性：

```
pageHeading.innerText = 'Learning the DOM with JavaScript'
// 输出: Learning the DOM with JavaScript
```

运行这将`h1`元素的文本更改为“Learning the DOM with JavaScript”。

我们可以以相同的方式访问任何其他标签。这里是`p`元素的示例：

```
document.getElementsByTagName('p')[0].textContent
// 输出: DOM stands for Object Model
```

## 使用`getElementById`和`getElementsByClassName`更具体地访问元素

到目前为止，你已经看到了如何使用`getElementsByTagName`方法访问特定标签。然而，通常你需要更具体地访问元素。例如，如果页面上有多个代表不同内容的`p`元素，使用`getElementsByTagName`方法来识别你想要的`p`元素将非常困难。相反，可以使用`id`或`class`属性更具体地访问元素。

### `getElementById`方法

文档对象的`getElementById`方法通过其`id`属性访问元素。由于HTML的`id`属性是唯一的，我们可以用它来直接标识网页上的特定元素。让我们在网页上再添加一个`p`元素，并给两个`p`元素都赋予一个`id`属性。修改你的`index.html`文件如下所示：

```html
<!DOCTYPE html>
<html>
<head>
<title>Learning the DOM</title>
</head>
<body>
<h1>Using JavaScript to access the DOM</h1>
<p id="dom-definition">
DOM stands for Document Object Model
</p>
<p id="dom-example">
We can use the DOM to manipulate the content of a page
</p>
</body>
</html>
```

现在，我们可以使用文档对象的`getElementById`方法访问`p`元素。该方法接受一个字符串参数，即我们想要访问的元素的`id`属性值。要访问`id`为“dom-definition”的`p`元素，在浏览器控制台中输入以下代码：

```
document.getElementById('dom-definition')
// 输出: <p id="dom-definition">DOM stands for Object Model</p>
```

可以看到这直接返回了`id`为“dom-definition”的`p`元素。我们也可以使用`textContent`属性访问它的文本内容：

```
document.getElementById('dom-definition').textContent
// 输出: DOM stands for Document Object Model
```

让我们获取`id`为“dom-example”的`p`元素的文本内容：

```
document.getElementById('dom-example').textContent
// 输出: We can use the DOM to manipulate the content of a web page
```

通过`id`属性和`getElementById`方法访问网页上的特定元素很容易。然而，如果你有多个具有相同`id`属性的元素，`getElementById`方法只会返回它找到的元素。要识别同一类别的多个元素，你可以改用`class`属性配合`getElementsByClassName`方法。

### `getElementsByClassName`方法

文档对象的`getElementsByClassName`方法通过其`class`属性访问元素。`class`属性不是唯一的，因此该方法返回一个具有相同`class`属性的元素的`HTMLCollection`。让我们为`index.html`文件中的`p`元素赋予名为“paragraph”的`class`属性：

```html
<p id="dom-definition" class="paragraph">
DOM stands for Document Object Model
</p>
<p id="dom-example" class="paragraph">
We can use the DOM to manipulate the content of a page
</p>
```

现在，我们可以使用`getElementsByClassName`方法访问所有`class`属性为“paragraph”的元素。该方法接受一个字符串参数，即我们要访问的元素的`class`属性值。在你的浏览器控制台中运行以下代码：

```
document.getElementsByClassName('paragraph')
// 输出: HTMLCollection(2) [p#dom-definition.paragraph, p#dom-example.paragraph]
```

在输出`p#dom-definition.paragraph`中，`p`代表标签名，`#`代表`id`属性，`.`代表`class`属性。因此，`#dom-definition`表示元素的`id`属性为“dom-definition”，而`.paragraph`表示元素的`class`属性为“paragraph”。

## 使用`querySelector`和`querySelectorAll`方法访问元素

`querySelector`和`querySelectorAll`方法与`getElementById`和`getElementsByClassName`方法类似，但允许我们更灵活地访问元素。通过这些方法，我们可以使用`id`、`class`或任何属性来访问元素。我们也可以通过标签名或标签名与属性的组合来访问元素。让我们看看这些方法是如何工作的。

文档对象的`querySelector`方法用于访问匹配指定选择器的第一个元素。选择器是指定要选择元素的字符串。例如，选择器`p`将选择网页上所有的`p`元素。`querySelector`方法接受选择器作为参数并返回匹配它的第一个元素。让我们使用`querySelector`方法选择网页上的第一个`p`元素：

```javascript
document.querySelector('p')
// 输出: <p id="dom-definition" class="paragraph">DOM stands for Document Object Model</p>
```

另一方面，`querySelectorAll`方法返回所有匹配指定选择器的`NodeList`。`NodeList`与`HTMLCollection`相似，但它是更通用的列表，可以包含不同类型的节点，包括文本节点、注释节点和文档节点。`NodeList`和`HTMLCollection`都是数组对象，因此我们可以通过索引访问它们的元素。

让我们使用`querySelectorAll`方法来选择网页上所有的`p`元素：

```javascript
document.querySelectorAll('p')
// 输出: NodeList(2) [p#dom-definition.paragraph, p#dom-example.paragraph]
```

我们还可以使用`querySelector`和`querySelectorAll`方法通过`id`或`class`属性来选择元素。例如，选择器`#dom-definition`将选择`id`属性为“dom-definition”的元素，选择器`.paragraph`将选择所有`class`属性为“paragraph”的元素。让我们使用`querySelector`方法选择`id`属性为“dom-definition”的元素：

```javascript
document.querySelector('#dom-definition')
// 输出: <p id="dom-definition" class="paragraph">DOM stands for Document Object Model</p>
```

让我们使用`querySelectorAll`方法选择所有`class`属性为“paragraph”的元素：

```javascript
document.querySelectorAll('.paragraph')
// 输出: NodeList(2) [p#dom-definition.paragraph, p#dom-example.paragraph]
```

为了更具体地访问元素，我们可以结合标签名和属性。例如，选择器`p#dom-definition`将选择`id`属性为“dom-definition”的`p`元素，而选择器`p.paragraph`将选择所有`class`属性为“paragraph”的`p`元素。因此，如果存在相同`class`或`id`的另一个元素，`querySelector`方法只会返回同时匹配标签名和属性的元素。让我们在`index.html`文件中添加一个`class`属性与`p`元素相同的`div`元素：

```html
<body>
  <h1>Using JavaScript to access the DOM</h1>
  <p id="dom-definition" class="paragraph">
    DOM stands for Document Object Model
  </p>
  <p id="dom-example" class="paragraph">
    We can use the DOM to manipulate the content of a web page
  </p>
  <div class="paragraph">
    This div element has the same class attribute as the p elements
  </div>
</body>
```

现在，让我们使用`querySelector`方法选择`class`属性为“paragraph”的`div`元素。在你的浏览器控制台中运行以下代码：

```javascript
document.querySelector('div.paragraph')
// 输出: <div class="paragraph">This div element has the same class attribute as the p elements</div>
```

`querySelector`方法只返回同时匹配标签名和属性的元素。让我们使用`querySelectorAll`方法获取所有`class`属性为“paragraph”的`p`元素：

```javascript
document.querySelectorAll('p.paragraph')
// 输出: NodeList(2) [p#dom-definition.paragraph, p#dom-example.paragraph]
```

这是一个使用`id`属性的示例。我们将使用选择器`p#dom-definition`来获取`id`为“dom-definition”的`p`元素：

```javascript
document.querySelector('p#dom-definition')
// 输出: <p id="dom-definition" class="paragraph">DOM stands for Document Object Model</p>
```

在使用`querySelector`和`querySelectorAll`方法通过`id`或`class`属性访问元素时，必须在属性值之前包含`#`或`.`符号。`#`代表`id`属性，`.`代表`class`属性。如果你在属性值之前没有包含它们，这些方法将假设你正尝试通过标签名访问元素。因此，如果我们不使用“#dom-definition”而是使用“dom-definition”，`querySelector`方法将搜索标签名为“dom-definition”的元素并返回`null`：

```javascript
document.querySelector('dom-definition')
// 输出: null
```

## 访问元素的属性和属性

### `attributes`属性和`getAttribute`方法

我们可以使用`getAttribute`方法和`attributes`属性来访问元素的属性。`getAttribute`方法接受属性名作为参数并返回属性值。`attributes`属性返回一个包含元素所有属性的类数组对象。让我们使用`getAttribute`方法获取`id`为“dom-definition”的`p`元素的`id`属性值：

```javascript
document.querySelector('#dom-definition').getAttribute('id')
// 输出: "dom-definition"
```

让我们使用`attributes`属性获取`id`为“dom-definition”的`p`元素的所有属性：

```javascript
document.querySelector('#dom-definition').attributes
// 输出: NamedNodeMap(2) [id, class]
```



`attributes`属性返回一个包含元素所有属性的`NamedNodeMap`对象。`NamedNodeMap`代表一个可以通过名称访问的节点集合。我们可以使用方括号符号和属性索引，或者使用点符号和属性名，来访问`NamedNodeMap`对象的属性。让我们使用方括号符号获取`id`为“dom-definition”的`p`元素的`id`属性：

```javascript
document.querySelector('#dom-definition').attributes[0]
// Output: id
```

这里是使用点符号的相同示例：

```javascript
document.querySelector('#dom-definition').attributes.id
// Output: id
```

要访问属性的值，我们可以使用它的`value`属性：

```javascript
document.querySelector('#dom-definition').attributes[0].value
// Output: "dom-definition"

document.querySelector('#dom-definition').attributes.id.value
// Output: "dom-definition"
```

## style属性

`style`属性返回一个包含元素所有样式属性的对象。让我们获取`dom-definition`元素的`style`属性：

```javascript
document.querySelector('#dom-definition').style
// output: CSSStyleDeclaration {accentColor: '', backgroundColor: '', fontSize: '', ...}
```

注意`style`属性返回一个`CSSStyleDeclaration`对象。`CSSStyleDeclaration`对象代表一个CSS声明块。在JavaScript对象中，每个样式属性都用驼峰法（camelCase）表示。因此，在CSS中是`background-color`，`style`属性是`backgroundColor`。由于我们没有对元素设置样式，每个样式属性的值都是一个空字符串。

要直接访问样式属性的值，我们可以使用点符号或方括号符号：

```javascript
document.querySelector('#dom-definition').style.backgroundColor
// Output: ""

document.querySelector('#dom-definition').style['backgroundColor']
// Output: ""
```

我们还可以使用`getPropertyValue`方法获取样式属性的值：

```javascript
document.querySelector('#dom-definition').style.getPropertyValue('background-color')
// Output: ""
```

## 修改DOM元素

在DOM中修改元素与修改JavaScript对象中的元素相同。我们可以重新赋值DOM元素属性的值，并添加或删除属性。例如，我们可以通过重新赋值`id`属性的值来更改元素的`id`属性值。让我们将`id`为“dom-definition”的`p`元素的`id`属性改为“new-dom-definition”：

```javascript
document.querySelector('#dom-definition').id = 'new-dom-definition'
document.querySelector('#new-dom-definition').getAttribute('id')
// Output: "new-dom-definition"
```

DOM元素还有一个`setAttribute`方法，我们可以用它修改属性值。`setAttribute`方法接受两个参数：属性名和属性值。让我们使用`setAttribute`方法将`id`属性改回“dom-definition”：

```javascript
document.querySelector('#new-dom-definition').setAttribute('id', 'dom-definition')
document.querySelector('#dom-definition').getAttribute('id')
// Output: "dom-definition"
```

元素样式也可以通过重新赋值样式属性的值来修改。让我们将`dom-definition`元素的背景颜色改为红色：

```javascript
document.querySelector('#dom-definition').style.backgroundColor = 'red'
// 输出: "red"
```

这也应该改变浏览器中元素的背景颜色。就像`setAttribute`方法一样，`style`属性也有一个`setProperty`方法，我们可以用它来修改元素的样式。让我们将`dom-definition`元素的字体大小改为3em：

```javascript
document.querySelector('#dom-definition').style.setProperty('font-size', '3em')
document.querySelector('#dom-definition').style.fontSize
// 输出: "3em"
```

你可以看到，每当我们修改DOM时，浏览器都会更新页面。这是因为DOM是页面的实时表示，对DOM进行的任何更改都会立即反映在浏览器中。

## innerHTML属性

`innerHTML`属性以字符串形式返回元素的HTML内容。例如，在你的浏览器控制台中运行`document.body.innerHTML`将返回`body`元素的HTML内容：

```javascript
document.body.innerHTML
// 输出: '<h1>...</h1> <p>...</p>..."
```

我们也可以使用`innerHTML`属性来修改元素的HTML内容。让我们为`body`元素添加一个带有“The DOM is awesome!”文本的`p`元素：

```javascript
document.body.innerHTML += '<p>The DOM is awesome!</p>'
```

注意，我们使用的是`+=`运算符追加新的HTML内容，而不是重新给`innerHTML`属性赋值。如果我们使用`=`运算符，新的HTML内容将替换现有的HTML内容。记住，我们的HTML文档有一个类名为“paragraph”且文本为“This div element has the same class attribute as the p elements”的`div`元素。让我们使用`innerHTML`属性将其内容替换为一个按钮：

```javascript
document.querySelector('div.paragraph').innerHTML = '<button>Click me!</button>'
```

现在你应该会在`div`中看到一个按钮，而不是文本“This div element has the same class attribute as the p elements”。

## 创建DOM元素

`document`对象有一个`createElement`方法，我们可以用它创建新元素。该方法接受一个参数，即要创建的元素的标签名，例如`p`或`div`。让我们创建一个新的`p`元素作为示例：

```javascript
document.createElement('p')
// 输出: <p></p>
```

`createElement`方法返回一个具有规范指定标签名的新元素，但并不会将其添加到DOM中。我们可以使用`appendChild`方法将元素添加到DOM中。`appendChild`方法接受一个元素作为参数，并将其作为调用方法的元素的子元素添加。新元素将作为父元素的最后一个元素添加。

在将`p`元素添加到DOM之前，让我们先给它添加一些文本。我们可以使用`textContent`或`innerText`属性向元素添加文本。我们需要将新元素赋值给变量，以便方便地更新其属性：

```javascript
let newParagraph = document.createElement('p')
newParagraph.textContent = 'JavaScript is a versatile language.'
```

我们还可以给新元素添加任何我们想要的属性。让我们给它添加一个值为“about-javascript”的`id`属性：

```javascript
newParagraph.setAttribute('id', 'about-javascript')
```

现在，我们可以使用`appendChild`方法将新元素添加到DOM中：

```javascript
document.body.appendChild(newParagraph)
```

你应该看到新段落被添加到页面底部。

创建并向DOM添加新元素的其他方法还包括：

### insertBefore

`insertBefore`方法在指定的元素之前插入一个新元素。该方法接受两个参数：要添加的元素以及新元素要插入之前的元素。例如，让我们在`id`为“dom-example”的`p`元素之前添加一个新的`h2`元素：

```javascript
let newHeading = document.createElement('h2')
newHeading.textContent = 'Working with the DOM'
document.body.insertBefore(newHeading, document.querySelector('#dom-example'))
```

### replaceChild

`replaceChild`方法用新元素替换旧元素。该方法接受两个参数：要添加的元素和要替换的元素。让我们用一个新的`div`元素替换`#dom-example`元素。我们还会在`div`内部创建一个新的`p`元素：

```javascript
let newDiv = document.createElement('div')
let newParagraph = document.createElement('p')
newParagraph.setAttribute('id', 'dom-example')
newParagraph.textContent = 'Working with the DOM is fun!'
newDiv.appendChild(newParagraph)
document.body.replaceChild(newDiv, document.querySelector('#dom-example'))
```

这应该会将`#dom-example`元素替换为一个新的`div`元素。我们的新`div`也包含一个`p`元素。

### insertAdjacentHTML

`insertAdjacentHTML`方法在调用方法的元素的指定位置插入HTML内容。该方法接受两个参数：位置和HTML内容。位置可以是以下之一：

- `beforebegin`: 元素本身之前。
- `afterbegin`: 元素内部，在其第一个子元素之前。
- `beforeend`: 元素内部，在其最后一个子元素之后。
- `afterend`: 元素本身之后。

让我们将带有文本“The DOM is awesome!”的新的`p`元素添加到`#dom-example`元素之前：

```javascript
document.querySelector('#dom-example').insertAdjacentHTML('beforebegin', '<p>The DOM is awesome!</p>')
```

这会将新的`p`元素添加到`#dom-example`之前。

### insertAdjacentElement

`insertAdjacentElement`方法与`insertAdjacentHTML`方法相似。区别在于`insertAdjacentElement`方法接受元素作为第二个参数，而不是HTML内容。让我们将带有文本“The DOM is really cool!”的新`p`元素添加到`#dom-example`元素之后：

```javascript
let newParagraph = document.createElement('p')
newParagraph.textContent = 'The DOM is really cool!'
document.querySelector('#dom-example').insertAdjacentElement('afterend', newParagraph)
```

这会将新的`p`元素添加到`#dom-example`之后。

### insertAdjacentText

与其他`insertAdjacent`方法一样，`insertAdjacentText`方法相对于调用元素的指定位置插入文本。该方法接受两个参数：位置和要插入的文本。让我们将带有文本“JavaScript is for everyone!”的文本节点添加到`body`元素的最后一个子元素：

```javascript
document.body.insertAdjacentText('beforeend', 'JavaScript is for everyone!')
```

这会将新的文本节点作为`body`元素的最后一个元素。

### cloneNode

`cloneNode`方法返回调用方法的副本。它接受一个布尔参数，决定拷贝是否包含元素的子元素。让我们创建一个`#dom-definition`元素的拷贝：

```javascript
document.querySelector('#dom-definition').cloneNode(true)
// 输出: <p id="dom-definition">DOM stands for Document Object Model</p>
```

`cloneNode`方法创建元素的复制，但不会将其添加到DOM中。如果元素有子元素，只有当布尔参数为`true`时`cloneNode`方法才会复制它们。在上面的示例中，`#dom-definition`元素的文本节点也被复制了。让我们再次创建一个`#dom-definition`元素的拷贝，这次不包含它的子元素：

```javascript
document.querySelector('#dom-definition').cloneNode(false)
// 输出: <p id="dom-definition"></p>
```

### createTextNode

`createTextNode`方法创建一个文本节点。它接受一个参数，即要添加到文本节点中的文本。让我们创建一个带有“Learning the DOM requires practice”文本的文本节点。我们将把它追加到`#dom-example`元素：

```javascript
let textNode = document.createTextNode(
  ' Learning the DOM requires practice'
)
document.querySelector('#dom-example')
  .appendChild(textNode)
```

你应该能看到新文本被添加到`#dom-example`元素中。我们在文本之前添加了一个空格，以便将其与`#dom-example`元素中的现有文本隔离开来。

## 从DOM中移除元素

我们可以使用`removeChild`方法从DOM中移除一个元素。`removeChild`方法接受一个参数，即要删除的元素。让我们移除`#dom-definition`元素：

```javascript
document.body.removeChild(
  document.querySelector('#dom-definition')
)
```

我们还可以使用`innerHTML`属性将元素的值设置为空字符串。这将移除该元素的所有子节点。让我们移除`#dom-example`元素：

```javascript
document.querySelector('#dom-example').innerHTML = ''
```

请记住，DOM是网页的实时表示，因此你对其进行的任何更改都会反映在浏览器中。然而，当你刷新页面时，DOM将重置为初始状态。

## 遍历DOM

遍历DOM意味着在DOM树的元素之间移动。让我们对`index.html`文件做一些更改，以便我们有更多元素可以操作。用以下代码替换你的文件内容，然后在浏览器中刷新页面：

```html
<!DOCTYPE html>
<html>
<head>
  <title>Learning the DOM</title>
</head>
<body>
  <h1>Using JavaScript to access the DOM</h1>
```



DOM 代表文档对象模型。

我们可以使用 DOM 来操作网页的内容。

```
<div id="dom-intro">

  <p id="dom-definition">

    DOM stands for Document Object Model

  </p>

  <p id="dom-example">

    We can use the DOM to manipulate the content of a

    web page

  </p>

</div>
```

在新的 HTML 代码中，我们将 `<p>` 元素包裹在一个`id`为“dom-intro”的`<div>`元素中。让我们看看如何利用元素之间相互的关系来访问 DOM 元素。

### parentNode 属性

`parentNode` 属性返回调用它的元素的父节点。让我们使用`#dom-definition`元素的`parentNode`属性来访问其父节点：

```javascript
document.querySelector('#dom-definition').parentNode
// 输出: <div id="dom-intro">...</div>
```

我们还可以通过链式使用`parentNode`属性来访问元素的祖父节点：

```javascript
document.querySelector('#dom-definition').parentNode
  .parentNode
// 输出: <body>...</body>
```

### childNodes 属性

`childNodes` 属性返回一个元素所有子节点的`NodeList`，包括元素节点和像文本节点这样的非元素节点。

这里是一个使用`#dom-intro`元素的`childNodes`属性来访问其子节点的示例：

```javascript
document.querySelector('#dom-intro').childNodes
// 输出: NodeList(5) [text, p#dom-definition, text, p#dom-example, text]
```

子节点包括：
- 一个值为`"\n "`的文本节点（代表页面上元素之间的换行符。）
- 一个`id`为“dom-definition”的`<p>`元素节点
- 一个值为`"\n "`的文本节点
- 一个`id`为“dom-example”的`<p>`元素节点
- 一个值为`"\n "`的文本节点

### children 属性

`children` 属性与`childNodes`属性类似，但它返回的是一个仅包含子元素节点的`HTMLCollection`：

```javascript
document.querySelector('#dom-intro').children
// 输出: HTMLCollection(2) [p#dom-definition, p#dom-example]
```

### firstChild 和 lastChild 属性

`firstChild` 属性返回元素的第一个子节点，包括非元素节点。`lastChild`属性返回元素的最后一个子节点，也包括非元素节点。让我们使用`#dom-intro`元素的`firstChild`和`lastChild`属性来访问它的首两个子节点：

```javascript
document.querySelector('#dom-intro').firstChild
// 输出: #text

document.querySelector('#dom-intro').lastChild
// 输出: #text
```

### firstElementChild 和 lastElementChild 属性

`firstElementChild` 和`lastElementChild`属性分别返回元素的第一个和最后一个元素节点。与`firstChild`和`lastChild`属性不同，它们只返回元素节点：

```javascript
document.querySelector('#dom-intro').firstElementChild
// 输出: <p id="dom-definition">DOM stands for Document Object Model</p>

document.querySelector('#dom-intro').lastElementChild
// 输出: <p id="dom-example">We can use the DOM to manipulate the content of a web page</p>
```

### nextSibling 和 previousSibling 属性

`nextSibling` 属性返回元素的下一个兄弟节点，包括非元素节点。`previousSibling`属性返回元素的上一个兄弟节点，也包括非元素节点。让我们使用`#dom-definition`元素的`nextSibling`和`previousSibling`属性来访问它的下一个和上一个兄弟节点：

```javascript
document.querySelector('#dom-definition').nextSibling
// 输出: #text

document.querySelector('#dom-definition').previousSibling
// 输出: #text
```

### nextElementSibling 和 previousElementSibling 属性

与`nextSibling`和`previousSibling`属性不同，`nextElementSibling`和`previousElementSibling`属性只返回元素节点：

```javascript
document.querySelector('#dom-definition')
  .nextElementSibling
// 输出: <p id="dom-example">We can use the DOM to manipulate the content of a web page</p>

document.querySelector('#dom-definition')
  .previousElementSibling
// 输出: null
```

## 结论

文档对象模型是一个强大的工具，允许我们让网页具有动态性和交互性。它是 Web 开发中不可或缺的一部分，理解它的工作原理至关重要。创建更多的 HTML 文件并使用它们练习用 JavaScript 访问和修改 DOM。你也可以访问喜爱的网站，并使用浏览器的开发者工具来探索 DOM。

## 如何在 HTML 文件中引入 JavaScript

到目前为止，我们通过在控制台中运行 JavaScript 来练习它。但当我们开始处理网页和 DOM 时，我们需要在的 HTML 文件中包含 JavaScript。我们可以通过使用`<script>`标签在 HTML 文件中直接编写代码，或者通过创建一个`.js`扩展名的独立 JavaScript 文件并在 HTML 中引用它。让我们来看这两种方法。

### 在 HTML 文件中编写 JavaScript

（内联 JavaScript）

在 HTML 文件中包含 JavaScript 最简单的方法是使用`<script>`标签将代码直接添加到 HTML 中。这通常内联 JavaScript。我们可以在文档的`<head>`或`<body>`部分包含 JavaScript 代码，但最好将其放在`<body>`部分，这样在执行 JavaScript 之前加载 HTML 内容。让我们来看一个示例。创建一个名为`js-in-html.html`的新 HTML 文件并添加以下代码：

```html
<!DOCTYPE html>
<html>
<head>
  <title>JS in HTML</title>
</head>
<body>
  <h1>JS in HTML</h1>
  <script>
    alert('Hey everyone!')
  </script>
</body>
</html>
```

在上面的示例中，我们在 HTML 文件中添加了一个`alert()`方法。页面加载时，浏览器将运行 JavaScript 代码并显示带有“大家好！”消息的提示框。你可以通过在浏览器中打开 HTML 文件来查看效果。

虽然内联 JavaScript 可以作为小型项目或添加简单功能的解决方案，但它并不是大型项目的最佳选择。如果在 HTML 中包含大量的 JavaScript 代码，可能会变得难以阅读和维护。它也不高效，因为浏览器每次加载页面时都需要解析 JavaScript 代码。由于这些原因，通常最好创建一个独立的 JavaScript 文件并在 HTML 中引用它。

### 创建独立的 JavaScript 文件

（外部 JavaScript）

在 HTML 文件中引入 JavaScript 最常见的方法是创建一个扩展名为`.js`的独立 JavaScript 文件，并在 HTML 文件中引用它。让我们来看一个示例。

## 如何在 HTML 文件引入 JavaScript

在`js-in-html.html`文件相同的文件夹中，创建一个名为`js-in-html.js`的新 JavaScript 文件，并为其添加 alert 方法调用：

```javascript
alert('Hey everyone!')
```

现在，打开`js-in-html.html`文件，移除现有的`<script>`元素并添加一个新的链接到`js-in-html.js`文件的`<script>`元素：

```html
<!DOCTYPE html>
<html>
<head>
  <title>JS in HTML</title>
</head>
<body>
  <h1>JS in HTML</h1>
  <script src="./js-in-html.js"></script>
</body>
</html>
```

在我们新的示例中，我们添加了一个`<script>`元素，通过其`src`属性和路径链接到`js-in-html.js`文件，而不是使用最初包含 JavaScript 代码的那个`<script>`元素。当页面加载时，浏览器将运行`js-in-html.js`文件中的 JavaScript 代码，并显示带有消息“Hey everyone!”的 alert 框。

将 JavaScript 链接到单独的文件中可以保持 HTML 和 JavaScript 代码分离，这使其更易阅读和维护。它也使得在多个 HTML 文件中复用 JavaScript 代码变得更容易。例如，如果我们想在另一个 HTML 文件中添加相同的 alert，只需简单链接到同一个`js-in-html.js`文件即可。

`<script>`标签还有其他属性可以被我们用来控制 JavaScript 代码的加载和执行。让我们来看其中几个。

### async 属性

`async`属性告诉浏览器异步加载 JavaScript 文件，这意味着浏览器在加载 JavaScript 文件时可以继续加载 HTML 文件。这对于加载耗时较长的大型 JavaScript 文件非常有用。但是，如果 JavaScript 代码依赖于先加载 HTML 内容，它也可能会导致问题，因为一旦 JavaScript 文件加载，即使 HTML 内容尚未加载完成，浏览器也会执行 JavaScript 代码。以下是我们在`<script>`元素中使用`async`属性的方式：

```html
<script src="./js-in-html.js" async></script>
```

### defer 属性

`defer`属性告诉浏览器异步加载 JavaScript 文件，但在 HTML 文件加载后执行 JavaScript 代码。与`async`属性不同，`defer`属性确保在 HTML 内容加载后执行 JavaScript 代码，从而避免 JavaScript 代码依赖于先加载 HTML 内容时可能出现的任何问题。以下是我们使用`defer`属性的方式：

```html
<script src="./js-in-html.js" defer></script>
```

需要注意的是，`async`和`defer`属性并不是所有浏览器都支持，特别是旧版本的浏览器。然而，它们是控制你的 JavaScript 代码加载和执行的好选择。

## 结论

我们已经了在 HTML 文件中引入 JavaScript 代码的不同方法。每种方法都有其优缺点，选择使用哪种取决于多种因素，如项目的规模和复杂性、对不同浏览器的兼容性要求以及优化的需求。

无论你使用哪种方法，保持代码的组织有序和可维护都是至关重要的，这样你就可以创建提供良好用户体验的可靠 Web 应用。

## 浏览器事件

浏览器事件是浏览器中发生的动作。这些动作通常由用户触发，例如点击按钮、滚动网页或提交表单。通过使用 JavaScript，我们可以响应这些事件并创建动态、交互式的网页。

当用户点击你网页上的按钮时，你可能想通过显示显示消息或导航到新页面来响应该操作。浏览器提供了一种监听这些事件并对其响应的方法。通过 DOM，我们可以为 HTML 页面中的元素添加事件监听器，这样当用户执行特定操作时，浏览器将执行一个 JavaScript 函数来作为响应。这个函数被称为事件处理器（event handler）。事件处理器通常被称为事件监听器（event listeners），但更具体地说，事件监听器是负责监听事件的，而事件处理器是事件发生时执行的函数。

DOM 元素拥有`addEventListener()`方法，允许我们为它们添加事件监听器。该方法接受两个参数：事件的名称和事件处理器函数。例如，如果我们想为按钮添加点击事件监听器，我们将调用它的`addEventListener()`方法并将事件名称和事件处理器函数作为参数传递：

```javascript
const button = document.querySelector('button')
button.addEventListener('click', () => {
  console.log('You clicked me!')
})
```

除了`addEventListener()`方法外，元素还有几个事件属性，我们可以将它们设置为事件处理器函数。这些属性以它们监听的事件命名，例如用于点击事件的`onclick`或用于滚动事件的`onscroll`。例如，我们也可以通过将按钮的`onclick`属性设置为事件处理器函数来添加点击事件监听器：

```javascript
button.onclick = () => {
  console.log('You clicked me!')
}
```

当执行事件处理器函数时，浏览器会将一个事件对象作为参数传递给该函数。该对象包含有关发生事件的信息。例如，传递到点击事件函数中的事件对象包含了被点击元素的信息。我们可以通过使用事件对象的`target`属性来访问这些信息。例如，如果我们想记录被点击的元素，可以这样做：

```javascript
button.onclick = (event) => {
  console.log(event.target)
}
```

让我们在另一个 HTML 文件上工作，以便你可以看到事件监听器是如何工作的。创建一个名为`browserEvents.html`的新文件并添加以下代码：

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8"
  <title>Browser Events</title>
</head>
<body>
  <h1>Working with Browser Events</h1>
  <p>点击下面的按钮触发浏览器事件。</p>
  <button id="click-me-btn">Click Me!</button>
</body>
</html>
```

在同一目录下创建一个名为`browserEvents.js`的新文件，并添加以下 JavaScript 代码。我们将首先选择元素并为其添加事件监听器：

```javascript
const button = document.querySelector('#click-me-btn')
button.addEventListener('click', () => {
  alert('You clicked me!')
})
```

在我们的 JavaScript 文件中，我们使用`querySelector()`方法选择元素并将其存储在变量`button`中。然后，通过调用`addEventListener()`方法并将事件名称和事件处理器函数作为参数，为按钮添加点击事件监听器。事件处理器是一个显示消息框的匿名箭头函数。让我们将 JavaScript 文件包含在 HTML 代码中，以便浏览器可以执行它。在`browserEvents.html`文件中添加以下代码：

```html
<script src="browserEvents.js"></script>
```



现在你可以在浏览器中打开 HTML 文件并点击按钮。

如果我们想获取有关发生事件或被点击元素的更多信息，我们可以向事件处理器函数传递一个事件参数。该参数将代表浏览器在执行时传递给函数的事件对象，它包含了发生事件的信息。事件对象的一些常用属性和方法包括：

## target

`target` 属性返回事件发生的元素。例如，如果我们想将被点击的元素记录到控制台，可以将 `browserEvents.js` 文件中的点击事件处理器函数修改为：

```javascript
button.addEventListener('click', (event) => {
  console.log(event.target)
})
```

刷新页面并点击按钮，控制台应该会出按钮元素 `<button id="click-me-btn">Click Me!</button>`。

## 浏览器事件

### type

`type` 属性返回发生事件的类型，例如 `click`（点击）或 `submit`（提交）：

```javascript
button.addEventListener('click', (event) => {
  console.log(event.type)
})
```

### currentTarget 和事件冒泡

`currentTarget` 属性返回绑定事件监听器的元素，而不一定是事件发生的元素。`target` 和 `currentTarget` 之间的区别在于：`target` 返回被点击的元素，而 `currentTarget` 返回事件监听器所绑定的元素。例如，如果我们从按钮上移除点击事件监听器，并将其添加到 `body` 元素上，那么即使我们点击了按钮，`currentTarget` 属性也会返回 `body` 元素。这被称为**事件冒泡**。事件冒泡允许事件向其父元素传播或“冒泡”向的机制。由于 `body` 元素是按钮元素的父元素，因此点击事件将冒泡到绑定了事件监听器的 `body` 元素。将你 `browserEvents.js` 文件中的代码替换为以下内容：

```javascript
document.body.addEventListener('click', (event) => {
  console.log(event.currentTarget)
})
```

### stopPropagation()

`stopPropagation()` 方法阻止事件冒泡到父元素。例如，如果我们想在点击按钮时防止点击事件冒泡到 `body` 元素，我们可以在按钮上添加一个事件监听器，并在事件处理函数中调用事件对象的 `stopPropagation()` 方法。同上一个示例中的 `body` 事件监听器一起，将以下代码添加到你的 `browserEvents.js` 文件中并刷新页面：

```javascript
const button = document.querySelector('#click-me-btn')

button.addEventListener('click', (event) => {
  event.stopPropagation()
})
```

现在，当你点击按钮时，点击事件将不再冒泡到 `body` 元素，`body` 事件监听器也不会被执行。你也可以在按钮的事件处理函数中添加代码，这些代码会在按钮被点击时运行：

```javascript
button.addEventListener('click', (event) => {
  event.stopPropagation()
  alert('You clicked me!')
})
```

如果没有 `stopPropagation()` 方法，点击按钮时，`body` 事件监听器和按钮的监听器都将被执行。

### key

`key` 属性返回发生键盘事件时按下或释放的按键值。例如，如果我们想将按下按键的值打印到控制台，可以修改 `browserEvents.js` 文件中的 `body` 事件处理函数为如下内容：

```javascript
document.body.addEventListener('keydown', (event) => {
  console.log(event.key)
})
```

刷新页面并按下键盘上的任意键，应该会将该按键的值打印到控制台。

### preventDefault()

`preventDefault()` 方法阻止事件的默认行为被执行。例如，表单提交按钮的默认行为是在点击时重新加载页面。如果我们想阻止这种行为，可以在提交事件处理函数中对事件对象调用 `preventDefault()` 方法。让我们在 `browserEvents.html` 文件中添加一个表单。在元素下方添加以下代码：

```html
<form id="name-form">
  <label for="name">Name:</label>
  <input type="text" id="name">
  <input type="submit" value="Submit">
</form>
```

当你点击浏览器中的提交按钮时，注意看页面刷新了。让我们为表单的提交按钮添加事件监听器来防止这种行为。将你 `browserEvents.js` 文件中的代码替换为以下内容：

```javascript
const form = document.querySelector('#name-form')

form.addEventListener('submit', (event) => {
  event.preventDefault()
})
```

现在，点击提交按钮不应再刷新页面。我们也可以在事件处理函数中添加代码，将输入字段的值打印到控制台：

```javascript
form.addEventListener('submit', (event) => {
  event.preventDefault()
  console.log(event.target.name.value)
})
```

刷新页面并提交表单，应该会将输入字段的值打印到控制台。`event.target` 属性返回表单元素，`name` 属性返回输入元素，而 `value` 属性返回输入字段的值。

### 浏览器事件类型和监听器

让我们探索不同的浏览器事件类型，以及我们如何使用监听器来响应它们。

#### 鼠标事件

鼠标事件是用户与鼠标交互时发生的动作，例如移动鼠标或点击元素。以下是一些最常见的鼠标事件：

- `click` - 当用户点击元素时发生
- `dblclick` - 当用户双击元素时发生
- `mousedown` - 当用户在元素上按下鼠标键时发生
- `mouseup` - 当用户在元素上释放鼠标键时发生
- `mouseover` - 当用户鼠标悬过元素时发生
- `mouseout` - 当用户移出元素时发生
- `mousemove` - 当用户移动鼠标时发生
- `wheel` - 当用户在元素上滚动滚轮时发生

#### 键盘事件

键盘事件由键盘执行的操作触发，如打字和按键。一些常见事件包括：

- `keydown` - 当按键按下时发生
- `keyup` - 当按键释放时发生
- `keypress` - 当按键按下时发生

#### 表单事件

表单事件在用户与表单交互时触发，例如提交表单。一些常见事件包括：

- `submit` - 当表单提交时发生
- `reset` - 当表单重置时发生

#### 窗口事件

窗口事件在用户与浏览器窗口交互时触发，例如调整大小或滚动页面。一些常见事件包括：

- `load` - 当页面加载时发生
- `unload` - 当页面卸载时发生
- `resize` - 当浏览器窗口大小发生变化时发生
- `scroll` - 当用户滚动页面时发生

## 浏览器存储

在构建 Web 应用时，你通常需要向浏览器中存储数据，用于各种目的，例如缓存（在本地存储数据以提高性能）、存储用户偏好或存储用户数据以便于检索。由于这些原因，现代浏览器提供了几种客户端存储机制，包括 Cookies、LocalStorage 和 SessionStorage。

### Cookies

Cookies 是由 Web浏览器存储在用户计算机上的小段数据。它们被设计为一种可靠的机制，让网站能够记住状态信息（例如在线商店中添加到购物车的物品），或记录用户的浏览活动并存储少量数据，以便在页面请求之间持久化信息。

Cookies 通常以键值对的形式存储，并且每个 Cookie 都与特定的域关联。因此，一个网站只能访问它设置的 Cookies。Cookies 的大小也受到限制，最多只能存储 4KB 的数据。它们可以被设置为在特定时间过期，到期后由浏览器删除。如果 Cookie 没有设置过期日期，它将被视为会话 Cookie（session cookie），并在用户关闭浏览器时被删除。然而，并非所有浏览器都会在关闭时自动删除会话 Cookie，可能还有其他影响浏览器中 Cookie 行为的因素，例如用户设置或扩展程序。

由于 Cookies 与特定域关联，你必须在服务器上运行你的网页来设置和检索 Cookies。如果你正在使用 VS Code 或其他强大的代码编辑器，可以安装 **Live Server** 扩展或类似的插件来运行你的网页。例如，在 VS Code 中，安装扩展后，右键点击任何 HTML 文件并选择 **Open with Live Server**（用 Live Server 打开）。如果没有，你可以使用任何其他本地服务器，例如 Node.js 的 `http-server` 软件包。

### 在 Cookies 中存储数据

当你的网页在服务器上运行时，让我们通过实践来学习如何操作 Cookies。我们可以使用 `document.cookie` 属性来设置 Cookie。该属性是一个包含当前域所有 Cookies 的字符串。让我们设置一个在 2035 年 11 月 23 日期过期的 Cookie：

```javascript
document.cookie = 'name=Ada Lovelace; expires=Fri, 23 Nov 2035 12:00:00 UTC; path=/';
```

在这个示例中，键值对 `name=Ada Lovelace` 是存储在 Cookie 中的实际数据，而 `expires` 和 `path` 属性是可选参数，用于控制 Cookie 的生存时间和访问范围。`expires` 属性指定 Cookie 的过期日期，`path` 属性指定 Cookie 有效的路径。如果没有指定 `path` 属性，则 Cookie 对整个域有效。

要添加新 Cookie，我们可以再次设置 `document.cookie` 属性。这将新 Cookie 追加到现有的 Cookie 字符串中。让我们添加一个键值对为 `favorite_language=JavaScript` 的 Cookie：

```javascript
document.cookie = 'favorite_language=JavaScript';

console.log(document.cookie)
// "name=Ada Lovelace; favorite_language=JavaScript"
```

### 从 Cookies 中检索数据

我们可以通过 `document.cookie` 属性检索 Cookie 的值。然而，该属性返回的是当前域所有 Cookies 的字符串，因此我们需要使用 `split()` 方法将字符串拆分为单个 Cookie 的数组。`split()` 方法是一个字符串方法，接受一个分隔符作为参数并返回子字符串数组。分隔符用于确定每个子字符串的开始和结束。由于 Cookie 是用分号和空格分隔的，我们将使用 `"; "` 作为分隔符：

```javascript
const cookies = document.cookie.split('; ');

console.log(cookies)
// ["name=Ada Lovelace", "favorite_language=JavaScript"]
```

让我们检索 `name` Cookie 的值。我们无法总是确定 Cookie 存储的顺序，因此需要遍历 Cookie 数组并检查每个项，看它是否以字符串 `name` 开头。如果是，我们就返回该 Cookie。我们可以使用 `find()` 方法来完成操作：

```javascript
const nameCookie = cookies.find((cookie) =>
  cookie.startsWith('name')
)

console.log(nameCookie)
// output: "name=Ada Lovelace"
```

记住 Cookies 的大小限制为 4KB，因此它们不适合存储大量数据。Cookies 还会随每次请求发送到服务器，因此如果 Cookie 太多，可能会减慢你 Web 应用的性能。所以，在处理 Cookies 时，最好只存储应用程序运行必需的少量数据。如果你需要存储更多数据，可以考虑使用 LocalStorage 或 SessionStorage。

### LocalStorage 和 SessionStorage

LocalStorage 和 SessionStorage 是浏览器存储选项中较新添加的内容，与 Cookies 相比它们具有几个优势。像 Cookies 一样，它们允许 Web 应用在客户端存储数据，但它们具有更大的存储容量（通常约为 5MB），并且不会像 Cookies 那样随每个请求将数据发送到服务器。

LocalStorage 和 SessionStorage 的相似之处在于它们都在客户端存储数据，但不同之处在于数据存储的时间。LocalStorage 存储的数据没有过期日期，因此在关闭浏览器窗口后数据将依然存在。相反，SessionStorage 仅为单个会话存储数据。这意味着当用户关闭浏览器窗口或标签页时，数据会被删除。

让我们看看如何使用 LocalStorage 和 SessionStorage 存储数据。我们将从 LocalStorage 开始，然后是 SessionStorage。

### LocalStorage

LocalStorage 是 `window` 对象的一个属性，我们可以通过 `window.localStorage` 访问它。`localStorage` 是一个包含 `setItem()` 方法（设置数据）和 `getItem()` 方法（检索数据）的对象。让我们在 LocalStorage 中存储用户名 `ada_loelace`：

```javascript
localStorage.setItem('username', 'Ada Lovelace')
```

要检索 `username` 键的值，我们可以使用 `localStorage.getItem()` 方法。该方法接受一个键作为参数并返回与该键关联的值。让我们检索 `username` 的值：

```javascript
const username = localStorage.getItem('username')

console.log(username)
// output: "Ada Lovelace"
```

我们也可以打印 `localStorage` 对象来查看在 LocalStorage 中的所有键：

```javascript
console.log(localStorage)
// output: Storage {username: "Ada Lovelace"}
```

### 存储和检索数组与对象

数组在存储到 LocalStorage 时会自动转换为字符串，因此我们可以存储一个用户名数组：

```javascript
const allUsernames = [
  'ada_loelace',
  'grace_hopper',
  'alan_turing',
]

localStorage.setItem('allUsernames', allUsernames)

const storedUsernames = localStorage.getItem('allUsernames')

console.log(storedUsernames)
// output: "ada_loelace,grace_hopper,alan_turing"
```

要将字符串转换数组，可以使用 `split()` 方法：

```javascript
const usernamesArray = storedUsernames.split(',')

console.log(usernamesArray)
// ["ada_loelace", "grace_hopper", "alan_turing"]
```

而对象在存储到 LocalStorage 之前需要先转换为字符串。如果你尝试直接存储一个对象，它会被自动转换为字符串 `[object Object]`，而不是实际的对象数据。这是因为 JavaScript 默认的 `toString()` 方法在对象上调用时会返回字符串 `[object Object]`。

要将对象转换为字符串，可以使用 `JSON.stringify()` 方法。该方法接受一个对象作为参数并返回该对象的字符串表示。

## SessionStorage

SessionStorage 与 LocalStorage 非常相似，但它仅在页面会话中有效。这意味着当用户关闭标签页或浏览器时，SessionStorage 中的数据会被清除。

我们可以以相同的方式操作数据：

```javascript
const user = {
  name: 'Ada',
  role: 'Developer'
};

sessionStorage.setItem('user', JSON.stringify(user));

const retrievedUserString = sessionStorage.getItem('user');
```



`const retrievedUser = JSON.parse(retrievedUserString);`

`console.log(retrievedUser.name);` // // output: "Ada"

## 浏览器存储

`const user = {`

  `username: 'ada_lovelace',`

  `favoriteLanguage: 'JavaScript',`

`}`

`localStorage.setItem('user', JSON.stringify(user))`

要从 LocalStorage 中检索对象，我们可以使用`localStorage.getItem()`方法。然而，该方法返回的是一个字符串，因此我们需要使用`JSON.parse()`方法将其转换回对象。该方法接受字符串作为参数，并返回该字符串所代表的对象：

`const storedUser = localStorage.getItem('user')`

`console.log(storedUser)`

// output: "{\"username\":\"ada_lovelace\","

// "\"favoriteLanguage\":\"JavaScript\"}"

`const userObject = JSON.parse(storedUser)`

`console.log(userObject)`

// output: {username: "ada_lovelace", favoriteLanguage: "JavaScript"}

## 从 LocalStorage 中移除项

要从 LocalStorage 中移除一个项，我们可以使用`localStorage.removeItem()`方法。该方法接受键作为参数，并从 LocalStorage 中移除该键值对：

`localStorage.removeItem('username')`

`console.log(localStorage.getItem('username'))`

// output: null

## 清空 LocalStorage

要清除 LocalStorage 中的所有项，我们可以使用`localStorage.clear()`方法：

`localStorage.clear()`

`console.log(localStorage)`

// output: Storage {}

在使用 LocalStorage 时，请记住数据是存储在客户端的，任何能够访问客户端的任何人或脚本都可以访问。因此，你应该避免在 LocalStorage 中存储敏感数据，例如密码或信用卡信息。LocalStorage 还在所有浏览器标签页和窗口之间共享。这意味着，如果你在一个标签页的 localStorage 中存储了数据，它将在所有其他共享相同源（相同的域名、协议和端口）的标签页和窗口可用。这对于在多个标签页或窗口之间维护数据非常有用，但如果不小心，也可能导致冲突或不一致的状态。

## SessionStorage

SessionStorage 的语法与 LocalStorage 类似。我们可以通过`window.sessionStorage`属性访问它。该属性是一个对象，包含用于设置数据的`setItem()`方法和用于检索数据的`getItem()`方法。让我们使用与之前相同的示例在 SessionStorage 中存储用户名`ada_lovelace`：

`sessionStorage.setItem('username', 'ada_lovelace')`

要检索用户名 键的值，我们可以使用`sessionStorage.getItem()`方法：

`const username = sessionStorage.getItem('username')`

`console.log(username)`

// output: "ada_lovelace"

像 LocalStorage 一样，我们可以使用`removeItem()`方法从 SessionStorage 中移除项：

`sessionStorage.removeItem('username')`

`console.log(sessionStorage.getItem('username'))`

// output: null

我们还可以使用它的`clear()`方法清除 SessionStorage 中的所有项：

`sessionStorage.clear()`

`console.log(sessionStorage)`

// output: Storage {}

记住 SessionStorage 仅对当前会话有效。因此，如果你关闭浏览器窗口或标签页，数据将被删除。与 LocalStorage 不同，SessionStorage 特定于单个浏览器标签页；当你在一个标签页的 SessionStorage 中存储数据时，它在其他标签页或窗口中无效，并在标签页关闭时被删除。

## 使用 JavaScript 构建待事项列表应用

让我们利用 JavaScript 和 DOM 的知识来构建一个简单的待事项列表应用程序。在我们的应用中，我们将能够向列表中添加任务、将它们标记为已完成、从列表中删除它们，并将它们存储在浏览器的 LocalStorage 中。这是一个 Web 存储 API，允许我们在浏览器中持久化数据，以便在刷新页面或关闭浏览器后，我们的任务仍然可用。

### 使用 HTML 构建我们的应用结构

我们将开始创建一个名为`todoApp.html`的 HTML 文件并添加以下代码：

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Todo App</title>
</head>
<body>
  <h1>Todo App</h1>
  <form id="addTaskForm">
    <input type="text" id="taskInput" required />
    <button type="submit">Add Task</button>
  </form>
  <ul id="taskList"></ul>
  <script src="./todoApp.js"></script>
</body>
</html>
```

该 HTML 代码创建了一个带有文本输入和按钮的简单表单。我们为表单分配了`addTaskForm`的 id，为输入框分配了`taskInput`的 id 以便访问它。我们还有一个 id 为`taskList`的无序列表。

### 使用 JavaScript 为我们的应用添加功能

让我们创建`todoApp.js`。我们将首先使用`document.querySelector()`方法获取元素的引用：

（正文继续下文...）

注意，我们直接将 HTML 代码作为字符串返回。我们本可以使用`document.createElement()`方法来创建元素并将它们添加到列表项中，但这种方法更直观且易于阅读。由于我们返回的是多行字符串，我们使用了反引号（`` ` ``）而不是单引号（`'`）来包裹字符串。我们还将将任务输入的值作为复选框的值和标签，这将允许我们在想要从列表中删除任务时，轻松地获取该任务值。

### 将已保存的任务渲染到浏览器

当用户加载页面时，我们想要渲染存储在浏览器 LocalStorage 中的任何任务。我们将首先创建一个名为`storedTasks`的变量，它将存储我们从 LocalStorage 中获取的任务。由于任务是以 JSON 字符串形式存储的，我们将使用`JSON.parse()`方法将其转换为 JavaScript 对象。如果 LocalStorage 中没有任务，我们将`storedTasks`变量设置为空数组：

`const storedTasks = JSON.parse(localStorage.getItem('tasks')) || []`

在向列表中添加任务时，我们还将其将其添加到`storedTasks`数组中，然后使用`JSON.stringify()`方法将数组转换回 JSON 字符串，然后使用键`tasks`将其存储在 LocalStorage 中。这是必要的，因为 LocalStorage 只支持存储字符串。OR 运算符（`||`）如果第一个操作数为真值，则返回第一个操作数的值，否则将返回第二个操作数的值。在这种情况下，如果`localStorage.getItem('tasks')`的值为`null`，OR 运算符将返回一个空数组。

接下来，让我们创建一个名为`renderTasks()`的函数，将我们在 LocalStorage 中的任务渲染到浏览器。我们将使用`forEach()`方法遍历`storedTasks`数组，并为每个任务调用`createTaskItem()`函数。然后我们将使用`insertAdjacentHTML()`方法将返回的 HTML 代码添加到无序列表中：

## 使用 JavaScript 构建一个 Todo 列表应用

```javascript
const renderTasks = () => {
  storedTasks.forEach((task) => {
    taskList.insertAdjacentHTML(
      'beforeend',
      createTaskItem(task)
    )
  })
}
```

`insertAdjacentHTML()`方法接受两个参数：我们想要插入 HTML 代码的位置，以及 HTML 代码本身。在这种情况下，我们使用`beforeend`位置，它将把 HTML 代码添加到无序列表的末尾。接下来，我们将在页面加载时调用`renderTasks()`函数。每当页面加载时，它都会将我们在 LocalStorage 中存储的任务渲染到浏览器中：

```javascript
window.onload = renderTasks
```

我们的`todoApp.js`文件现在看起来应该是这样：

```javascript
const taskInput = document.querySelector('#taskInput')
const taskList = document.querySelector('#taskList')
const addTaskForm = document.querySelector('#addTaskForm')

taskList.style = `
  list-style: none;
  margin-top: 1rem;
  font-size: 1.5rem;
`

const createTaskItem = (task) => `
  <li>
    <input type="checkbox" name="task" value="${task}">
    <label for="task">${task}</label>
    <button type="button">X</button>
  </li>
`

const storedTasks = JSON.parse(localStorage.getItem('tasks')) || []

const renderTasks = () => {
  storedTasks.forEach((task) => {
    taskList.insertAdjacentHTML(
      'beforeend',
      createTaskItem(task)
    )
  })

window.onload = renderTasks
```

### 将任务添加到列表

现在，让我们创建一个点击提交按钮时将任务添加到列表的。我们将使用`addEventListener()`方法监听表单的提交事件。当事件触发时，我们将阻止表单的默认行为（即刷新页面）。然后我们将获取输入字段的值，使用`createTaskItem()`函数创建一个列表项，并将其添加到页面`ul`元素中。我们还将任务添加到`storedTasks`数组中，并将其存储在 LocalStorage 的`tasks`键中，最后通过`reset()`方法清除输入字段：

```javascript
const addTask = (event) => {
  event.preventDefault()
  const task = taskInput.value
  const taskItem = createTaskItem(task)
  taskList.insertAdjacentHTML('beforeend', taskItem)
  storedTasks.push(task)
  localStorage.setItem('tasks', JSON.stringify(storedTasks))
  addTaskForm.reset()
}
```

接下来，我们将为表单添加事件监听器，在表单提交时调用`addTask()`函数：

```javascript
addTaskForm.addEventListener('submit', addTask)
```

我们也可以在`todoApp.html`文件的表单元素上使用`onsubmit`属性添加事件监听器：

```html
<form id="addTaskForm" onsubmit="addTask(event)">
```

这将实现`addEventListener()`方法，以便将所有的 JavaScript 代码保留在`todoApp.js`文件中。

为了测试目前的进展，请在浏览器中打开`todoApp.html`文件。你应该看到表单和无序列表。在输入字段中输入任务并点击提交按钮。你应该看到任务已添加到列表中。即使刷新页面，任务仍然在那里。

### 标记任务为完成

现在，让我们添加标记任务为完成的功能。当用户勾选任务的复选框时，我们将使用`textDecoration`样式将其划线；如果他们取消勾选复选框，我们将取消划线。首先创建一个名为`toggleTaskCompletion()`的函数。我们的函数接受事件对象作为参数，使用事件对象的`target`属性获取被点击的复选框。然后我们使用`parentElement`属性获取包含复选框的列表项。接下来，我们将使用`querySelector()`方法获取列表项内部的 label 元素。如果复选框被选中，我们将`textDecoration`样式设置为`line-through`，否则设置为`none`：

```javascript
const toggleTaskCompletion = (event) => {
  const taskItem = event.target.parentElement
  const label = taskItem.querySelector('label')
  if (event.target.checked) {
    label.style.textDecoration = 'line-through'
  } else {
    label.style.textDecoration = 'none'
  }
}
```

接下来，我们将在`createTaskItem()`函数中为复选框添加事件监听器。将你的函数更新为：

```javascript
const createTaskItem = (task) => `
  <li>
    <input type="checkbox" name="task" value="${task}" onchange="toggleTaskCompletion(event)">
    <label for="task">${task}</label>
    <button type="button">X</button>
  </li>
`
```

### 移除任务

接下来，我们将添加从列表中移除任务的功能。当用户点击 X 按钮时，我们将从页面、从`storedTasks`数组中移除任务，并更新 LocalStorage，这样刷新页面时任务就不会回来了。我们首先创建一个名为`removeTask()`的函数：

```javascript
const removeTask = (event) => {
  const taskItem = event.target.parentElement
  const task = taskItem.querySelector('label').innerText
  const index = storedTasks.indexOf(task)
  storedTasks.splice(index, 1)
  localStorage.setItem('tasks', JSON.stringify(storedTasks))
  taskItem.remove()
}
```

最后，我们将在`createTaskItem()`函数的按钮上添加一个`onClick`事件监听器。将你的函数更新为：

```javascript
const createTaskItem = (task) => `
  <li>
    <input type="checkbox" name="task" value="${task}" onchange="toggleTaskCompletion(event)">
    <label for="task">${task}</label>
```



## 使用 JavaScript 构建待办事项应用

现在你可以通过点击 `X` 按钮从列表中移除任务了。

```html
<button type="button" onclick="removeTask(event)">X</button>
```

```javascript
const storedTasks = JSON.parse(localStorage.getItem('tasks')) || [];

const renderTasks = () => {
  storedTasks.forEach((task) => {
    const taskItem = createTaskItem(task)
    taskList.insertAdjacentHTML('beforeend', taskItem)
  })
}

window.onload = renderTasks;

const addTask = (event) => {
  event.preventDefault();
  const task = taskInput.value;
  const taskItem = createTaskItem(task);
  taskList.insertAdjacentHTML('beforeend', taskItem);
  storedTasks.push(task);
  localStorage.setItem(
    'tasks',
    JSON.stringify(storedTasks)
  );
  addTaskForm.reset();
}

addTaskForm.addEventListener('submit', addTask);

const toggleTaskCompletion = (event) => {
  const taskItem = event.target.parentElement;
  const task = taskItem.querySelector('label');
  if (event.target.checked) {
    task.style.textDecoration = 'line-through';
  } else {
    task.style.textDecoration = 'none';
  }
}

const removeTask = (event) => {
  const taskItem = event.target.parentElement;
  const task = taskItem.querySelector('label').innerText;
  const indexOfTask = storedTasks.indexOf(task);
  storedTasks.splice(indexOfTask, 1);
  localStorage.setItem(
    'tasks',
    JSON.stringify(storedTasks)
  );
  taskItem.remove();
}
```

## 结论

现在，你已经学会了如何使用 HTML、CSS 和 JavaScript 创建一个简单的待办事项应用。你已经从获取用户输入、在 DOM 中添加和删除元素、在 `localStorage` 中存储数据以及使用事件监听器响应用户操作方面获得了实战经验。这为构建更复杂的 Web 应用奠定了良好的基础。为了测试你的知识，请尝试再次构建这个应用，但这次要靠自己独立完成。你还可以为应用添加更多功能，例如清除所有任务的按钮，或者将所有任务标记为已完成的按钮。如果你遇到困难，可以随时查阅这本指南。

## 异步 JavaScript

### 什么是异步 JavaScript？

异步 JavaScript 是现代 Web 开发中的一个核心概念。在传统的 JavaScript 中，代码是同步方式执行的，这意味着每行代码都按顺序线性执行（从上到下）。这对于简单的程序来说没有问题，但在处理耗时任务（如发送网络请求、执行复杂计算或访问数据库或文件系统）时就会出现问题。如果你同步执行这些任务，负责渲染用户界面和处理用户交互的主线程将被阻塞，在任务完成之前无法进行任何其他操作，导致程序看起来像死机或对用户无响应。

这就是异步 JavaScript 的用场，它允许你在不阻塞主 UI（用户界面）线程的情况下执行耗时任务，这样你的应用程序就可以继续运行并响应用户输入。“异步”一词指的是一种允许同时执行多个任务互不阻塞的编程模式。这对于现代 Web 应用是必要的，因为它们通常需要同时执行多个任务，例如发送网络请求、在后台加载数据以及播放音频或视频。

### Promises（承诺）

在 JavaScript 中管理异步代码的一种方法是使用 `Promise`。`Promise` 是代表异步操作最终完成或失败的对象。你可以将其想象成未来某个可用值的占位符。`Promise` 处于三种可能的状态之一：

- **pending**（等待中）：`Promise` 的初始状态，表示值尚不可用。
- **fulfilled**（已履行）：`Promise` 的表示操作成功的状态，意味着值已变为可用。
- **rejected**（已拒绝）：`Promise` 的表示操作失败的状态，意味着发生了错误。

`Promise` 是使用 `Promise` 构造函数创建的，该构造函数接受一个函数作为参数。这个函数被称为 **executor function**（执行器函数），负责启动异步操作。执行器函数接收两个函数作为参数：`resolve` 和 `reject`。当异步操作成功时调用 `resolve` 函数，当操作失败时调用 `reject` 函数。`resolve` 和 `reject` 函数用于改变 `Promise` 的状态，并可以带有一个值传递给注册到该 `Promise` 的处理器。这是一个在延迟 5 秒后解析字符串值“Data retrieved successfully”的 `Promise` 示例：

```javascript
let myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Data retrieved successfully')
  }, 5000)
})
```

当你运行这段代码时，`myPromise` 变量将被赋值一个 `pending` 状态的 `Promise` 对象。在执行器函数调用 `resolve` 函数之前，`Promise` 将一直保持 `pending` 状态，该调用将把 `Promise` 的状态改为 `fulfilled`，并将字符串值传递给注册到该 `Promise` 的任何处理器。在这种情况下，`Promise` 将在 5 秒后变为履行。如果你在 `Promise` 履行之前向控制台打印 `myPromise` 变量，你会发现它仍然处于 `pending` 状态：

```javascript
console.log(myPromise)
// 输出: Promise { <pending> }
```

如果你想处理 `Promise` 的结果，可以使用它的 `then` 方法注册处理器。`then` 方法接受一个函数作为参数，该函数在 `Promise` 履行时被调用。该函数将可以访问传递给 `resolve` 函数的值。以下是如何为 `Promise` 注册处理器的示例：

```javascript
myPromise.then((value) => {
  console.log(value)
})
```

这应该在 5 秒后向控制台输出字符串值“Data retrieved successfully”。注意，`Promise` 在 `pending` 状态下不会停止其他任务的执行。所以如果我们在创建 `Promise` 后向控制台打印其他内容，它将立即打印，而无需等待 `Promise` 履行；当 `Promise` 履行后，它的值将打印到控制台。要尝试这一点，请运行以下代码：

```javascript
let myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Data retrieved successfully')
  }, 5000)
})

myPromise.then((value) => {
  console.log(value)
})

console.log('Hey there!')
```

输出结果：
```
Hey there!
Data retrieved successfully
```

如果在 `Promise` 中不是调用 `resolve` 函数而是调用 `reject` 函数，那么 `Promise` 将被拒绝，注册到 `Promise` 的任何错误处理器将接收错误值。我们可以使用 `catch` 方法注册错误处理器。`catch` 方法接受一个函数作为参数，该函数在 `Promise` 被拒绝时被调用。该函数将可以访问传递给 `reject` 函数的值。处理 `Promise` 时，同时处理履行和拒绝状态是非常重要的，这样当发生错误时你可以做出恰当响应。这是一个在 5 秒后被拒绝的 `Promise` 示例，以及一个将错误记录到控制台的错误处理器：

```javascript
let myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    reject('An error occurred')
  }, 5000)
})

myPromise
  .then((value) => {
    console.log(value)
  })
  .catch((error) => {
    console.log(error)
  })
```

我们也可以将 `Promise` 写在函数体内，这样它就可以在稍后运行或重用：

```javascript
const doSomeMath = (a, b) => {
  return new Promise((resolve, reject) => {
    const result = a + b
    if (result > 10) {
      resolve(result)
    } else {
      reject('The result is too small')
    }
  })
}
```

在我们的示例中，`doSomeMath` 函数接收两个数字作为参数并返回一个 `Promise`。如果两个数字之和大于 10，该 `Promise` 将变为完成（`fulfilled`）；如果小于 10，则将变为拒绝（`rejected`）。我们可以这样调用 `doSomeMath` 函数：

```javascript
doSomeMath(5, 20)
  .then((value) => {
    console.log(value)
  })
  .catch((error) => {
    console.log(error)
  })

// 输出: 25
```

让我们再次调用它，但这次传入两个会导致 `Promise` 被拒绝的数字：

```javascript
doSomeMath(5, 2)
  .then((value) => {
    console.log(value)
  })
  .catch((error) => {
    console.log(error)
  })

// 输出: The result is too small
```

**Promise 方法**

我们还可以使用其他几种配合 `Promise` 的方法。这些方法包括：`Promise.all`, `Promise.race`, `Promise.resolve`, `Promise.reject` 以及 `finally`。我们将从 `Promise.all` 开始。

### Promise.all

`Promise.all` 方法接收一个 `Promise` 数组作为参数并返回一个单一的 `Promise`。返回的单个 `Promise` 在参数数组中的所有 `Promise` 都变为完成后才会变为完成。如果参数数组中的任何一个 `Promise` 被拒绝，返回的单个 `Promise` 也会被拒绝。这里是使用 `Promise.all` 的示例：

```javascript
let promise1 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise 1 resolved')
  }, 5000)
})

let promise2 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise 2 resolved')
  }, 3000)
})

let promise3 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise 3 resolved')
  }, 1000)
})

Promise.all([promise1, promise2, promise3]).then(
  (values) => {
    console.log(values)
  }
)

// 输出: ["Promise 3 resolved", "Promise 2 resolved", "Promise 1 resolved"]
```

如果我们拒绝了数组中的其中一个 `Promise`，返回的单个 `Promise` 就会被拒绝。让我们重写 `promise2`，使其变为拒绝而不是完成：

```javascript
let promise2 = new Promise((resolve, reject) => {
  setTimeout(() => {
    reject('Promise 2 rejected')
  }, 3000)
})

Promise.all([promise1, promise2, promise3])
  .then((values) => {
    console.log(values)
  })
  .catch((error) => {
    console.log(error)
  })

// 输出: Promise 2 rejected
```

### Promise.race

`Promise.race` 方法接收一个 `Promise` 数组作为参数并返回一个单一的 `Promise`。只要参数数组中的任何一个 `Promise` 变为完成或拒绝，返回的单个 `Promise` 就会变为完成或拒绝。把它想象成比赛，第一个完成的 `Promise` 获胜。让我们尝试一个示例：

```javascript
let promise1 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise 1 resolved')
  }, 5000)
})

let promise2 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise 2 resolved')
  }, 3000)
})

let promise3 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise 3 resolved')
  }, 1000)
})

Promise.race([promise1, promise2, promise3]).then(
  (values) => {
    console.log(values)
  }
)

// 在我们的示例中，promise1 将 5 秒后解析，promise2 将 3 秒后解析，promise3 将 1 秒后解析。由于 promise3 是第一个完成的，返回的单个 Promise 将以该值完成。
```

`Promise.resolve` 方法接收一个值作为参数并返回一个 `Promise`。返回的单个 `Promise` 以该值完成。这在你需要将一个值转换为 `Promise` 时非常有用。这里有一个示例：

```javascript
let myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Promise resolved')
  }, 5000)
})

myPromise
  .then((value) => {
    console.log(value)
  })
  .catch((error) => {
    console.log(error)
  })

// 输出: Promise resolved
```

`Promise.reject` 方法接收一个值作为参数并返回一个以该值拒绝的 `Promise`。这在你需要将一个值拒绝为 `Promise` 时非常有用。这里有一个示例：

```javascript
let myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    reject('Promise rejected')
  }, 3000)
})

myPromise
  .then((value) => {
    console.log(value)
  })
  .catch((error) => {
    console.log(error)
  })

// 输出: Promise rejected
```

`Promise.finally` 方法接收一个函数作为参数并返回一个 `Promise`。传递的函数会在 `Promise` 变为完成或拒绝时执行。这里是一个示例：



`let myPromise = new Promise((resolve, reject) => {`

```
  setTimeout(() => {

    resolve('Promise resolved')

  }, 5000)

})
```

`myPromise`

```
  .then((value) => {

    console.log(value)

  })

  .catch((error) => {

    console.log(error)

  })

  .finally(() => {

    console.log('finally')

  })
```

`// 输出: Promise resolved`

## 使用 Promises 和 Fetch API 发起 HTTP 请求

### 简介

向服务器发送 HTTP 请求以获取数据是 Web 开发的重要组成部分。随着 Promises 和 Fetch API 等 JavaScript 特性的引入，发送 HTTP 请求变得更加简单和高效。`Fetch API` 是一个 JavaScript API，提供了一种简单方便的方法来发送 HTTP 请求，并被所有现代浏览器支持。API（应用程序编程接口）是访问特定服务或数据源的一组编程指令和标准。我们可以使用 `Fetch API` 发起 GET（获取数据）、POST（创建数据）、PUT（更新数据）和 DELETE（删除数据）请求。当使用 `Fetch API` 发起请求时，它会返回一个解析 `Response` 对象的 `Promise`，该对象包含了从服务器获取的数据。

为了说明如何使用 `Fetch API` 发起 HTTP 请求，我们将创建一个包含我们想要获取的数据 JSON 文件。

在真实世界的应用中，我们会使用 API URL 从服务器像这样获取数据。然而，对于此示例，我们将使用本地 JSON 文件，这样我们就不需要担心在发送请求时服务器是否可用。JSON 代表 JavaScript 对象表示，是一种用于存储和传输数据的轻量格式。当数据从服务器发送到网页时，通常使用 JSON，其数据结构类似于 JavaScript 对象。让我们创建一个名为 `data.json` 的 JSON 文件，其中包含一个对象数组。JSON 文件以 `.json` 扩展。在我们的 JSON 数据中，每个对象将代表一个用户并具有 `name` 和 `age` 属性：

```json
[

  {

    "name": "John",

    "age": 30

  },

  {

    "name": "Sara",

    "age": 22

  },

  {

    "name": "Bill",

    "age": 40

  }

]
```

与典型的 JavaScript 对象不同，JSON 对象中的键必须包含在双引号中。现在我们有了 JSON 数据，

## 异步 JavaScript

异步地，我们可以使用 `Fetch API` 发起 GET 请求，从 JSON 文件中检索数据。在与 `data.json` 文件相同的目录中，创建一个名为 `fetchExample.html` 的 HTML 文件，并向其中添加以下代码：

```html
<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8" />

  <title>Fetch API</title>

</head>

<body>

  <script src="./fetchExample.js"></script>

</body>

</html>
```

接下来，在同一级目录下创建一个名为 `fetchExample.js` 的 JavaScript 文件。在我们的 JavaScript 文件中，我们将使用 `fetch()` 方法对 `data.json` 文件发送 GET 请求。`fetch()` 方法接受 URL 作为第一个参数，并返回一个解析为 `Response` 对象的 `Promise`：

```javascript
let fetchRequest = fetch('./data.json')

console.log(fetchRequest)
```

当你在浏览器中打开 `fetchExample.html` 文件时，会在控制台中看到 CORS 错误。CORS 代表跨源资源共享（Cross-Origin Resource Sharing），它是一种允许网页上的受限资源从提供第一个资源的域之外的其他域进行请求的机制。为了避免此错误，我们需要运行一个本地服务器。如果你正在使用 VS Code，可以安装 Live Server 扩展。一旦安装了扩展，右键点击 `fetchExample.html` 文件并选择“Open with Live Server”。否则，你可以使用任何其他本地服务器，例如 Node.js 的 `http-server` 包。

一旦启动了本地服务器，你会发现 `fetchRequest` 变量包含一个状态为“pending”的 `Promise` 对象：

```javascript
Promise {<pending>}
```

当请求完成后，返回的 `Promise` 将解析为 `Response` 对象。让我们使用 `then()` 方法在 `Promise` 解析时处理它。我们将 `Response` 对象打印到控制台：

```javascript
fetchRequest.then((response) => {

  console.log(response)

})
```

解析后的响应看起来应该是这样：

```javascript
Response {body: ReadableStream, status: 200, type: "cors",...}
```

`Response` 对象包含了关于响应的信息，包括状态码、响应类型和响应正文。`body` 属性包含一个 `ReadableStream` 对象，我们可以用它来读取从服务器返回的数据。我们可以使用 `json()` 方法将响应数据转换为 JavaScript 对象。`json()` 方法返回一个解析为 JavaScript 对象的 `Promise`，因此我们将链式另一个 `then()` 方法来在 `Promise` 解析时处理它：

```javascript
fetchRequest

  .then((response) => {

    return response.json()

  })

  .then((data) => {

    console.log(data)

  })
```

`data` 变量将包含从服务器返回的 JavaScript 对象：

```javascript
(3) [{...}, {...}, {...}]

0: {name: "John", age: 30}

1: {name: "Sara", age: 22}

2: {name: "Bill", age: 40}

length: 3

__proto__: Array(0)
```

让我们使用 `data` 变量在页面上显示用户数据。我们将创建一个 `ul` 元素并为每个用户添加一个 `li` 元素。更新 `fetchExample.js` 文件如下：

```javascript
let fetchRequest = fetch('./data.json')

fetchRequest

  .then((response) => {

    return response.json()

  })

  .then((data) => {

    let ul = document.createElement('ul')

    data.forEach((user) => {

      let li = document.createElement('li')

      li.textContent = `${user.name} is ${user.age}`

      ul.appendChild(li)

    })

    document.body.appendChild(ul)

  })
```

当你刷新页面时，你应该能看到页面上显示的用户数据：

- John is 30
- Sara is 22
- Bill is 40

## Async/Await

`async` 和 `await` 关键字在 ES2017 中引入，使得处理 `Promise` 变得简单。例如，我们可以使用 `async` 和 `await` 关键字简化 `fetchExample.js` 文件中的 Fetch 请求：

```javascript
let fetchUsers = async () => {

  let response = await fetch('./data.json')

  console.log(response)

}

fetchUsers()

// Response {body: ReadableStream, status: 200, type: "cors",...}
```

`async` 关键字用于定义异步函数，而 `await` 关键字用于等待 `Promise` 解析，且只能在 `async` 函数内部使用。在我们的示例中，我们首先定义了一个名为 `fetchUsers()` 的异步箭头函数。我们也可以在普通的函数声明中使用 `async` 关键字：

```javascript
async function fetchUsers() {

  // ...

}
```

在 `fetchUsers()` 函数内部，我们使用 `await` 关键字等待 `fetch()` 方法解析。当我们在变量声明中使用 `await` 关键字时，该变量将被赋值 `Promise` 的解析值。在我们的示例中，`response` 变量将被赋值 `fetch()` `Promise` 的解析值。然后我们可以使用 `await` 关键字等待 `json()` 方法解析。我们将创建一个名为 `data` 的新变量，并将其赋值 `json()` `Promise` 的解析值。在 `fetchUsers()` 函数内部，我们将 `data` 变量打印到控制台：

```javascript
let response = await fetch('./data.json')

let data = await response.json()

console.log(data)
```

当你刷新页面时，你会看到之前示例中的相同数据：

```javascript
(3) [{...}, {...}, {...}]

0: {name: "John", age: 30}

1: {name: "Sara", age: 22}

2: {name: "Bill", age: 40}

length: 3

__proto__: Array(0)
```

现在我们可以使用 `data` 变量在页面上显示用户数据：

```javascript
let fetchUsers = async () => {

  let response = await fetch('./data.json')

  let data = await response.json()

  let ul = document.createElement('ul')

  data.forEach((user) => {

    let li = document.createElement('li')

    li.textContent = `${user.name} is ${user.age}`

    ul.appendChild(li)

  })

  document.body.appendChild(ul)

}
```

当你刷新页面时，你应该看到页面上显示了用户数据：

- John is 30
- Sara is 22
- Bill is 40

我们可以使用 `try` 和 `catch` 关键字来处理异步函数中的错误。让我们更新 `fetchUsers()` 函数使用 `try` 和 `catch` 关键字：

```javascript
let fetchUsers = async () => {

  try {

    let response = await fetch('./data.json')

    let data = await response.json()

  } catch (error) {

    // 处理错误

    console.log(error)

  }

}
```

这将捕获 `try` 块中发生的任何错误，包括 `fetch()` 方法和 `json()` 方法中发生的错误。`async` 和 `await` 关键字帮助我们编写看起来更像同步代码的异步代码，避免了链式调用 `.then()` 方法。然而，`async` 和 `await` 只是 `Promise` 的语法糖（为了使代码更易读而添加的语法），它们并没有改变 `Promise` 工作的底层机制。

我们已经成功地使用 `Fetch API` 从 `data.json` 文件检索了数据。我们也可以以相同的方式向服务器发送 HTTP 请求。让我们更新 `fetchUsers()` 函数向 GitHub API 发起 HTTP 请求。我们可以通过用户名获取任何用户的数据。我们将用我的用户名进行一个示例：

```javascript
let fetchUsers = async () => {

  try {

    let response = await fetch(

      'https://api.github.com/users/ebenezerdon'

    )

    let data = await response.json()

  } catch (error) {

    // 处理错误

    console.log(error)

  }

}
```

当你刷新页面时，你将看到用户名为 `ebenezerdon` 的 GitHub 用户数据。如果你有 GitHub 账号，可以使用你的用户名代替我的用户名来查看你的数据。在 `fetch()` 方法中将 `ebenezerdon` 替换为你的用户名，你就能看到关于你的账户的信息。

现在你已经知道如何使用 Promises 和 Fetch API 了。通过构建一个从服务器获取并显示数据的简单应用，来练习你学到的一切内容。你可以在 Google 上搜索“public APIs”来寻找另一个你可以使用的 API。记住，掌握 JavaScript 是一个过程，你需要大量的练习才能精通。

## 处理日期和时间

JavaScript 提供了几种处理日期和时间的方法，允许我们创建、操作和格式化它们。内置的 `Date` 构造函数是实现这一点的最常用方法。它提供了创建日期对象、获取和设置日期时间组件以及将日期时间格式化为字符串的方法。

### 创建日期对象

我们可以通过调用不带参数的 `Date` 构造函数来创建一个新的 `Date` 对象：

```javascript
let currentDate = new Date()

console.log(currentDate)

// output: Sat May 19 2025 08:59:03 GMT+0100
```

要创建一个带有特定日期时间的 `Date` 对象，我们可以向 `Date` 构造函数传递一个字符串：

```javascript
let christmas = new Date('December 25, 2025')

console.log(christmas)

// output: Thu Dec 25 2025 00:00:00 GMT+0100
```

`Date` 构造函数接受日期时间字符串的多种格式，包括：

- December 25, 2025
- December 25 2025
- Dec 25 2025
- 12/25/2025
- 12-25-2025
- 2025-12-25
- 2025/12/25
- 2025.12.25
- 2025 12 25
- 2025 Dec 25
- 2025 December 25

我们也可以在字符串中指定时间：

```javascript
let christmas = new Date('December 25, 2025 23:15:30')

console.log(christmas)

// output: Thu Dec 25 2025 23:15:30 GMT+0100
```

如果未指定时间，它将默认为午夜。时间格式为“时:分:秒”，小时使用 24 小时制。我们还可以向字符串添加时区：

```javascript
let christmas = new Date('December 25, 2025 23:15:30 GMT-0500')

console.log(christmas)

// output: Fri Dec 26 2025 05:15:30 GMT+0100 (West Africa Standard Time)
```

`Date` 构造函数还可以接受多个参数，分别代表年、月、日、时、分、秒和毫秒：

```javascript
let christmas = new Date(2025, 11, 25)

console.log(christmas)

// output: Thu Dec 25 2025 00:00:00 GMT+0100
```



月份用数字指定，其中`0`代表一月，`1`代表二月，以此类推。日期用数字指定，其中`1`是该月的第一天。小时、分、秒和毫秒用数字指定，其中`0`是当天的第一个小时、分、秒或毫秒。

## 获取日期和时间组件

一旦我们有了`Date`对象，就可以使用它的属性和方法提取日期和时间的多个组件。`Date`对象具有以下属性：

- `getFullYear()` - 返回四位数字的年份
- `getMonth()` - 返回数字形式的月份
- `getDate()` - 返回数字形式的每月几号
- `getDay()` - 返回数字形式的星期几
- `getHours()` - 返回数字形式的小时
- `getMinutes()` - 返回数字形式的分钟
- `getSeconds()` - 返回数字形式的秒
- `getMilliseconds()` - 返回数字形式的毫秒
- `getTime()` - 返回自 1970 年 1 月 1 日以来的毫秒数。1970 年 1 月 1 日被用作 JavaScript `Date`对象的参考点，因为它是 Unix 纪元（Unix epoch）的起点，Unix 是计算机系统中表示日期和时间的标准系统。

让我们用创建的`Date`对象尝试一个例子：

```javascript
let christmas = new Date('December 25, 2025 23:15:30 GMT-0500')
console.log(christmas.getFullYear()) // output: 2025
console.log(christmas.getMonth()) // output: 11
console.log(christmas.getDate()) // output: 25
console.log(christmas.getDay()) // output: 5
console.log(christmas.getHours()) // output: 5
```

`getMonth()`方法返回`0-11`范围内的月份，`0`代表一月，`11`代表十二月。同样，`getDay()`方法返回`0-6`范围内的星期，`0`代表星期日，`6`代表星期六。我们还可以使用`toString()`方法将`Date`对象转换为字符串：

```javascript
let christmas = new Date('December 25, 2025 23:15:30 GMT-0500')
console.log(christmas.toString()) // output: 'Fri Dec 26 2025 05:15:30 GMT+0100'
```

## 设置日期和时间组件

一旦我们从`Date`对象中提取了日期时间组件，就可以操作这些组件来创建一个表示不同日期时间的新`Date`对象。其中一种方法是使用`Date`对象的方法和属性设置日期和时间的各个组件。`Date`对象具有以下设置日期时间组件的方法：

- `setFullYear(year)` - 设置年份
- `setMonth(month)` - 设置月份
- `setDate(date)` - 设置每月几号
- `setHours(hours)` - 设置小时
- `setMinutes(minutes)` - 设置分钟
- `setSeconds(seconds)` - 设置秒
- `setMilliseconds(milliseconds)` - 设置毫秒

让我们用`Date`对象尝试一个例子：

```javascript
let christmas = new Date('December 25, 2025 23:15:30 GMT-0500')
christmas.setFullYear(2026)
console.log(christmas) // output: Sat Dec 26 2026 05:15:30 GMT+0100
```

## 格式化日期和时间

`Date`对象有几个方法可以将日期时间格式化为字符串，包括：

- `toDateString()` - 返回字符串格式的`Date`对象日期部分
- `toTimeString()` - 返回字符串格式的`Date`对象时间部分
- `toLocaleString()` - 返回根据本地语言格式格式化的`Date`对象日期部分字符串
- `toLocaleTimeString()` - 返回根据本地语言格式格式化的`Date`对象时间部分字符串
- `toUTCString()` - 返回根据 UTC 时区格式化的对象日期和时间部分字符串

让我们用`Date`对象再尝试另一个例子：

```javascript
let christmas = new Date('December 25, 2025 23:15:30 GMT-0500')
console.log(christmas.toDateString()) // output: Fri Dec 26 2025
console.log(christmas.toTimeString()) // output: 05:15:30 GMT+0100
console.log(christmas.toLocaleDateString()) // output: 26/12/2025
console.log(christmas.toLocaleTimeString()) // output: 5:15:30
console.log(christmas.toUTCString()) // output: Fri, 26 Dec 2025 04:15:30 GMT
```

`Date`对象还有其他可转换为字符串的方法，包括`toISOString()`、`toJSON()`和`toGMTString()`。你可以在 MDN 文档中找到关于这些方法的更多信息。理解创建`Date`对象、操作它们以及处理时区对于创建准确且友好的 Web 应用程序非常重要。例如，你可能需要在网页上显示当前日期和时间，或者显示待办列表中特定条目的日期。处理`Date`对象可能会有点棘手，但通过练习，你将游刃有余。

`https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date`

## 结语

恭喜你！你已经读完了《面向重要程序员的极简版 JavaScript》。

当我决定撰写这本书时，我希望创建一个易于获取且易理解的资源，即使对于那些没有编程经验的人也是如此。我相信我已经实现了这个目标，并希望书中的解释和示例能够帮助你巩固学习成果，并建立起作为 JavaScript 程序员的信心。

请记住，练习是掌握任何编程语言的关键，因此我鼓励你继续运用你的知识并迎接新的挑战。

动手构建项目，当你感到困惑或需要刷新某个概念的知识时，随时回到这里。你可以通过在 YouTube 上搜索“Ebenezer Don”或访问`www.youtube.com/ebenezerdon`来找到基于项目的 JavaScript 教程。

作为程序员，你需要培养的一项重要技能是与他人协作并保持负责的能力。`NewDev`（`www.newdev.io`）是我的学习平台和开发者社区，旨在帮助你学习编程并与其他开发者建立联系。考虑在社区中分享你的每日进度，这将帮助你保持动力并坚持下去。

你还应该检查 MDN 文档以获取最新的 JavaScript 更新和功能。

- `https://www.youtube.com/c/ebenezerdon`
- `https://www.newdev.io`
- `https://developer.mozilla.org/en-US/docs/Web/JavaScript`

如果你喜欢这本书，请在 Amazon 或你购买它的任何其他平台上留下评价。我也非常期待在 Twitter 和 LinkedIn 上听到你的消息，所以请随时联系我并打个招呼。

我所有的社交媒体链接可以在我的 NewDev 个人页面上找到：`www.newdev.io/ebenezer`。

感谢阅读，我期待在社交媒体或通过邮件（`ebenezeron@newdev.io`）听到你所有的成就。

编码愉快！

- `https://www.newdev.io/ebenezer`
