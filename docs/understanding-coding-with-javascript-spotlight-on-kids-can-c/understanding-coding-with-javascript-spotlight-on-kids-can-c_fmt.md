
# JavaScript 编程入门指南（儿童编程系列）

你是否曾在网络浏览器中玩过游戏或查看过在线幻灯片？如果是这样，你很可能访问过使用 JavaScript 的网页。JavaScript 是一种流行的编程语言，它能让网页活起来。从游戏到文字处理器、电子表格等整个业务应用程序，很难想象没有它的万维网。

在 20 世纪 90 年代中期，程序员 Brendan Eich 写了 Mocha，这是 JavaScript 的早期版本。在互联网早期，网页大多是基础文本文件，是静态的或不变的。早期的网页先驱希望找到一种让网页更具动态性和交互的方法。这需要一种专门为网页设计的新编程语言。结果就是 JavaScript。今天，JavaScript 被用于创建各种通过浏览器运行的在线程序。

让网页活起来的编程语言。

JavaScript 是一种流行的编程语言，它能让网页活起来。从游戏到文字处理器、电子表格等整个业务应用程序，很难想象没有它的万维网。

在 20 世纪 90 年代中期，程序员 Brendan Eich 写了 Mocha，这是 JavaScript 的早期版本。在互联网早期，网页大多是基础文本文件，是静态的或不变的。早期的网页先驱希望找到一种让网页更具动态性和交互的方法。这需要一种专门为网页设计的新编程语言。结果就是 JavaScript。今天，JavaScript 被用于创建各种通过浏览器运行的在线程序。

JavaScript 是一种流行的编程语言，它能让网页活起来。从游戏到文字处理器、电子表格等整个业务应用程序，很难想象没有它的万维网。

在 20 世纪 90 年代中期，程序员 Brendan Eich 写了 Mocha，这是 JavaScript 的早期版本。在互联网早期，网页大多是基础文本文件，是静态的或不变的。早期的网页先驱希望找到一种让网页更具动态性和交互的方法。这需要一种专门为网页设计的新编程语言。结果就是 JavaScript。今天，JavaScript 被用于创建各种通过浏览器运行的在线程序。

JavaScript 是一种流行的编程语言，它能让网页活起来。从游戏到文字处理器、电子表格等整个业务应用程序，很难想象没有它的万维网。

在 20 世纪 90 年代中期，程序员 Brendan Eich 写了 Mocha，这是 JavaScript 的早期版本。在互联网早期，网页大多是基础文本文件，是静态的或不变的。早期的网页先驱希望找到一种让网页更具动态性和交互的方法。这需要一种专门为网页设计的新编程语言。结果就是 JavaScript。今天，JavaScript 被用于创建各种通过浏览器运行的在线程序。

## 需要了解的术语

编程不仅仅是计算机专家的专利。任何人都可以做到！在我们运行几个示例之前，这里有一份你将需要的有用术语列表。你很快就能用 JavaScript 编写代码了！

> 你不需要成为专家——甚至不需要成年人就可以学习编程。查看一下你的学校或当地图书馆是否提供编程课程，从今天就开始吧！

- **alert**：一个内置的 JavaScript 函数，会在弹出窗口中向用户显示消息。
- **code library（代码库）**：预写的代码，用于执行常用任务以便在创建程序时节省时间。
- **function（函数）**：可重用的代码，执行特定任务并在程序中重复使用。
- **HTML event（HTML 事件）**：用户或浏览器的操作，会导致代码执行。
- **HTML tag（HTML 标签）**：网页的单个构建模块。
- **pop-up window（弹出窗口）**：较大的浏览器窗口内部的较小窗口，通常用于向用户显示消息。
- **write（写入）**：一个内置的 JavaScript 函数，在网页浏览器屏幕上写入文本。

```javascript
function getValues(array) {
  var matValue = 0;
  for (var index = 0; index < array.length; index++) {
    var element = array[index];
  }
}
```

开始编写 JavaScript 并不困难。你只需要一个简单的文本编辑器和一个网页浏览器。大多数计算机已经安装了这些程序，或者已经设置好可以使用。文本编辑器是你编写代码并将其保存为 `.html` 扩展名的地方。`.html` 扩展名告诉浏览器它是在网页浏览器中打开的。

HTML 标签 `<script>` 和 `</script>` 指令网页浏览器将它们之间的文本视为 JavaScript 代码。在这个示例中，`document.write("Hello, World!");` 就是被执行的 JavaScript 代码。

```html
<!doctype html>
<html>
<head>
  <title>My Webpage</title>
  <script>
    document.write("Hello, World!");
  </script>
</head>
<body>
</body>
</html>
```

`<body>` 标签包含你在浏览器中显示的代码。一旦文件加载完成，你就可以点击浏览器的刷新按钮再次执行代码。

上一个示例使用了名为 `write` 的 JavaScript 函数。函数是许多编程语言共同的，也是大多数应用程序中重要的构建模块。它们执行某些操作，并可以在页面上命名为任何名称。

在编写代码时，拼写和大小写非常重要。如果不一致，你的代码将无法正常工作。

```html
<!doctype html>
<html>
<head>
  <title>My Webpage</title>
  <script>
    alert("Hello, World!");
  </script>
</head>
<body>
</body>
</html>
```

- 函数可以接受参数。参数是函数内部代码可以使用的一些信息。在这个示例中，我们将文本 `"Hello, World!"` 作为参数传递给 `alert` 函数。`alert` 函数的任务是在弹出窗口中显示其参数。

在这里，我们使用 HTML `button` 标签来创建一个按钮。在这个标签内，有一个特殊的属性叫做 `onclick`。它指令浏览器调用我们的自定义函数。

```javascript
function say() {
  alert("Hello, World!");
}
```

```html
<!doctype html>
<html>
<head>
  <title>My Webpage</title>
  <script>
    function say() {
      alert("Hello, World!");
    }
  </script>
</head>
<body>
  <button onclick="say()">Say</button>
</body>
</html>
```

`onclick` 属性是多个事件中的一个。事件是用户或浏览器的操作。`onclick` 命令告诉函数执行。简单来说，点击按钮将触发对我们 `say` 函数的调用，然后执行其内部的 `alert`。

为你创建的函数使用描述性名称是一个良好的习惯。这会让你的代码更容易于理解。

```html
<!doctype html>
<html>
<head>
  <title>My Webpage</title>
  <script>
    function say() {
      alert("Cheese!");
    }
  </script>
</head>
<body>
  <button onclick="say()">Say</button>
</body>
</html>
```

## 计划

当你准备好创建自己的 JavaScript 程序时，请遵循以下步骤：

1. 为你的程序编写一个简单的计划。
2. 打开你的文本编辑器并创建一个带有 `.html` 扩展的文件。
3. 在文件中输入以下 HTML 代码：

```html
<!doctype html>
<html>
<head>
  <title>My Webpage</title>
  <script>
  </script>
</head>
<body>
</body>
</html>
```

4. 在 `<script>` 和 `</script>` HTML 标签之间输入你的 JavaScript 代码。
5. 保存文件。
6. 在网页浏览器中打开文件以运行你的代码！

如果你对代码进行了任何更改，请确保在浏览器中运行之前再次保存文件。如果不先保存文件，你的任何更改都不会显示在浏览器中。

有很多在线资源可以帮助你学习更多编码知识。有些网站甚至提供了分步操作说明，并让你直接在他们的页面上进行编码练习。

JavaScript 的语法与更复杂、强大的编程语言（如 C++ 和 Java）相似。如果你熟悉 JavaScript，你可能会发现学习其他编程语言会变得更容易。今天，有许多 JavaScript 代码库可以下载，可以让构建程序变得更快、更简单。你可以从网上免费下载许多 JavaScript 框架。框架是预先编写的代码，为你提供了一种创建程序的条理方法。这些示例只是你用 JavaScript 能做事情的开始。只要有一个计划、一个文本编辑器和一个浏览器，就能轻松开始使用 JavaScript 进行编码！

- **环境**：计算机硬件和软件的结合，允许用户执行各种任务。
- **扩展名**：文件名的最后一部分，用于说明文件类型，例如 `.docx`。
- **输入**：输入到计算机中的信息。
- **逻辑**：思考或理解某事的正确或合理的方法。
- **语法**：单词排列以形成句子的方式。
- **版本**：事物与之前的形式不同的形式。
- **网页浏览器**：允许用户搜索互联网的计算机程序。
- **网页服务器**：托管并提供网站服务的计算机。

由于互联网链接的变动性，Powerkids Press 开发了一个与本书主题相关的在线网站列表。该网站定期更新。请使用此链接访问列表：`www.powerkidslinks.com/skcc/ucjs__`。

**儿童编程**

- 通过 Apple Swift 理解编码
- 通过 Python 理解编码
- 通过 JavaScript 理解编码
- 什么是集成电路？
- 什么是程序和应用程序？
- 什么是 HTML 代码？
- 什么是用户体验设计？
- 什么是用户界面设计？
- 为什么有这么多？
