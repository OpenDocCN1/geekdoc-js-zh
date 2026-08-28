
# JavaScript 入门指南

![](img/331e10bc8df06a94fc8288a269de6c23_0_0.png)

## 献辞

献给所有强烈渴望学习 JavaScript (js) 脚本语言的你们。

拥有学习的欲望是成功的最好途径。

## 1. 它是给谁的？

JavaScript 与 HTML（文本标记语言）和 CSS（层叠样式表）一起使用。HTML 不是编程语言，但 JavaScript 是，而它的代码包含了所有强烈渴望学习 JavaScript (js) 脚本语言的你们。拥有学习的欲望是成功的最好途径。JavaScript 用于创建动态页面，它在浏览器中非常流行，并被许多网站使用。

## 2. 简介与历史

20 世纪 90 年代初，JavaScript 由 Netscape 的 Brendan Eich 创建。在开发期间，JavaScript 被称为 Mocha，然后是 LiveScript。1996 年它被正式命名为 ECMAScript，但人们仍其称为 JavaScript。竞争浏览器考虑了这种语言及其增长。Internet Explorer 进行了更新以支持它，并重命名为 Jscript。它是面向对象的，具有许多功能，允许用户在网页上创建交互式元素。

右键点击浏览器右上角的首页图标。

## 3. JavaScript 定义

JavaScript 是一种编程语言，它使用的代码运行在您所看到的网页内容之后。因此，用户看不到网页内容背后的东西，但计算机或处理器是可以的。

然而，你可以通过在页面上点击右键并选择“查看源代码”来查看源码，是的，你可以查看它！

HTML 元素，在某种程度上它是一种编码语言，它使用文本、段落、链接、图像标签等更多内容来构建网页；CSS 代码样式则通过使用选择器（如颜色、字体、背景颜色等）为这些由 HTML 创建的页面提供更好的外观。JavaScript 通过为页面引入动态效果使其更进了一层，如果没有它，页面仅仅是静态的，而且可能很无味，因此它通过让用户在点击某些内容时与页面的交互变得可能且有趣来控制页面。

## 4. JavaScript 是一种脚本语言

JavaScript 包含在用于创建网页的文件，该文件保存为 `.html` 文件。你并不真的需要一个单独的文件来在该网页中运行 JavaScript；它运行在网页内部。

但你可以改用带有 `.js` 扩展名的独立 JavaScript 文件，这使得未来的代码更新和修正变得简单。

因为它是一种用于增强使用了 HTML 和 CSS 的页面的脚本语言。我们称其为解释型语言；大多数指令直接执行，它速度快、易用且具有效益。

编译型语言因为代码编译而变得复杂。

## 5. JavaScript 和 Java 是一样的吗？

它们完全不同；JavaScript 是一种配合 HTML 和 CSS 使用的脚本语言，而 Java 与它们没有关系，是一种编译型语言。

在 Web 开发领域，JavaScript 是唯一选择；名称上的相似仅仅是营销手段，当 Netscape 在 20 世纪 90 年开发它时，Java 非常流行，通过将其命名为 JavaScript，它更容易为人知。

Netscape 将该语言交给了全球性公司 ECMA；从那时起，所有著名的浏览器都支持 ECMAScript，但大家仍然称其为 JavaScript。

## 6. 开始

为了开始学习，我们需要做一些准备工作来做好设置并确保它是组织良好的。

所以你将创建一个文件夹并将其保存在你记得的地方，它将存放你为学习 JavaScript 而创建的所有文件。

### 6.1 创建文件夹

创建网页需要将许多文件保存在相同的路径下，以便于获取，并让代码文件位于同一个地方。

让我们创建一个名为 "Basic JavaScript" 的文件夹，你可以选择将其存放在 PC 或 Mac 的任何地方。

- **Windows**：在空白处点击右键并选择“新建-文件夹”，然后输入名称 Basic JavaScript。
- **Mac OS**：`CTRL` + 点击空白处并选择“新建文件夹”，点击这个新命名的文件夹，选中它，再次点击“未命名”的文件夹，进行重命名并写下 "JavaScript"，然后按回车键。
- **Windows PC**：选择你想要放置文件的路径，然后在空白处点击右键，选择“新建”，然后是“文件夹”，左鼠标单击接受，完成后，在空白文件夹上点击右键并选择“重命名”，然后输入你想要的文件名。

一旦存放作品的文件夹准备好了，让我们创建一个网页，并在其中创建 JavaScript。

让我们使用一个纯文本编辑器，以 Windows 的“记事本”作为示例，或使用你拥有的任何其他编辑器。

从 `<!DOCTYPE html>` 标签开始，这意味着文档被用作 HTML 使用。浏览器也期望如此。

1. 让我们使用 `Notepad`（免费）、`Notepad++`（免费）、`TextEdit`、`KomodoEdit`（免费）、`Dreamweaver`、`TextWrangler`（免费）或你喜欢的任何其他工具创建一个网页。

如果使用了 iCloud，请将你创建的文件夹放在硬盘中。

> **注意**：将 TextEdit 偏好设置改为纯文本。

HTML 代码文件：HTML 对大小写不敏感。创建网页所需的最小标签是：

```html
<!DOCTYPE html>
<html></html> 是 HTML 的开启/结束标签，所有的编码将位于其中。
<head></head> 是开启/结束标签，可以包含 <title>....</title> 开启/结束标签。
<body></body> 是开启/结束标签，段落以及可能的列表和其他标签将位于其中。
```

代码总结：

```html
<!DOCTYPE html>
<html>
<head>
<title>给你的网页命名，当你在 Google 上搜索它时它会被找到</title>
</head>
<body>
</body>
</html>
```

### 记事本代码文件

![](img/331e10bc8df06a94fc8288a269de6c23_14_0.png)

选择“文件”然后“保存”，或以 Windows 记事本为例，按 `CTL + S`，或者按你通常的方式保存。

如果是第一次保存，你就会看到“另存为”。

另存为：文件名选择“所有文件 (*.)”，文件名输入 `BasicJavaScript.html` 或 html 也可以，找到你创建的 BasicJavaScript 文件夹以进行组织，然后点击保存按钮。

![](img/331e10bc8df06a94fc8288a269de6c23_14_1.png)

使用了 `.html` 作为扩展名。

对于 Macintosh：当打开“另存为”窗口时，输入文件名并搜索你创建的文件夹，以 `.html` 扩展名保存，并点击保存。

> **注意**：将 TextEdit 偏好设置改为纯文本。

## 7. Mozilla Firefox 结果

![](img/331e10bc8df06a94fc8288a269de6c23_19_0.png)

## 8. Internet Explorer 结果

> **注意**：如果收到 Internet explorer 限制在网页上运行脚本的消息，请点击“允许 (Allow)”按钮。

![](img/331e10bc8df06a94fc8288a269de6c23_19_1.png)

你也可以在 Safari 或 Opera 中查看代码。

检查代码、拼写、标签和结构是一个良好的习惯，以确保它们正常工作。

> **注意**：遗憾的是，无法更改警报框的尺寸、字体和图标，但你可以更改框内的文本。

好消息是，JavaScript 比简单的 `alert` 框有更多有趣的内容可以提供。

## 9. 总结

JavaScript 是一种脚本语言，被最流行的浏览器支持，它与 HTML 和 CSS 一起用于 Web 开发。

它使用打开/关闭标签来告诉用户（在这种情况下为 浏览器）脚本语言从哪里开始到哪里结束。

在 JavaScript 中添加注释，我们使用 `//` 用于单行注释，或使用 `/*` 开始并 `*/` 结束注释（`/*` 和 `*/` 也用于多行注释）。

## 10. 事件处理

JavaScript 代码的执行与代码本身一样重要。例如，`onmouseover` 命令除非用户想要这样做并将鼠标移动到某个物体上，否则不会单独运行，因此，代码会有静止的时候，这正是我们想要的——在我们做出决定之前保持沉默，它在我们执行它之前保持沉默！

因此这被称为事件处理。得益于 HTML 与 JavaScript 代码，我们拥有完全的控制权，它允许更多的页面交互和对事件的控制。

JavaScript 是事件处理器，通过点击页面上的任何地方，当检测到事件时发生交互并执行代码。

事件处理器大多是属性，你可以在 HTML 标签内部使用它们，它们都以“on”开头，且**没有**空格。

以下是几个：

| 事件 | 描述 |
|---|---|
| `onclick` | 用户点击元素 |
| `onmouseover` | 用户将鼠标移过元素 |
| `onchange` | 当 HTML 元素发生变化时 |
| `onload` | 当页面加载完成时 |
| `onmouseout` | 当鼠标移出元素时 |
| `oncontextmenu` | 当使用鼠标右键点击元素时 |
| `ondblclick` | 当双击元素时 |
| `onmouseleave` | 当鼠标指针离开元素时 |
| `onmouseup` | 鼠标按钮在元素上释放 |
| `onmousedown` | 鼠标按钮在元素上按住 |
| `onmousemove` | 指针在元素上移动 |

我们将 JavaScript 代码添加到 HTML 元素中，以允许使用事件处理属性。为此，我们使用“单引号或双引号”。

因为 HTML 不区分大小写，所以可能会遇到看起来像：`onMouseOver` 或 `onMOUSEOVER` 或其他... 这样的事件。这不会影响任何事情，但尽量保持小写，例如 `onmouseover` 等。

`<an HTML element event="JavaScript which is a handler(event)">`

### 让我们来看一个例子

```html
<!DOCTYPE html>
<html>
<head>
<title></title>
</head>
<body>

<p onclick="alert('Have a nice day')">
保重！
</p>

</body>
</html>
```

#### 结果

![](img/331e10bc8df06a94fc8288a269de6c23_21_0.png)

起初你会看到文本：保重！

点击它，警报框就会带有消息出现。

点击 OK 关闭框。

> **注意**：我们不需要使用 `<script>...</script>` 标签来让事件发生并执行，`onclick` 事件处理器就足够了，浏览器知道双引号内部是 JavaScript 代码。

## 11. 嵌套

嵌套很重要，你可以先用双引号再用单引号，或者反过来先用单引号再用双引号，只要 JavaScript 在引号中即可。

```html
<p onclick="alert('Take care')"></p>
```

或者他们先使用单引号：

```html
<p onclick='alert("Take care")'></p>
```

使用第一种引号 `onclick="` 或其他 `onclick='` 的原因是为了让浏览器知道这是 JavaScript 代码的开始，然后是它认为是结束的结束引号。只要起始引号与结束引号匹配：`"` 和 `'` 即可。浏览器假设是这样的。必须正确嵌套，否则将会遇到事件问题。像这样的例子是错误的：

```html
<p onclick="alert('Take care')"></p>
```

#### 良好实践

`<p onclick="">` 紧跟错误之后。

#### 备注

我们可以在不使用 script 标签的情况下使用 JavaScript 代码，并且有时可以实现事件的执行。

## 12. ondblclick

```html
<!DOCTYPE html>
<html>
<head>
<title>帮助</title>
</head>
<body>

<h1 ondblclick="alert('Save a tree')">
树很重要
</h1>
</body>
</html>
```

#### 结果

树很重要

![](img/331e10bc8df06a94fc8288a269de6c23_23_0.png)

在句子“Trees are important”中，每当你双击一个单词时，对话框就会打开，点击 OK 关闭框。你必须双击一个单词来触发 JavaScript 代码并看到框。

## 13. onmouseover

添加一个分号；你可以添加更多 alert 消息，只需简单地将鼠标移到 h1 文本上，第一个框就会立即打开，当你关闭它时，第二个就会出现。查看示例：

```html
<!DOCTYPE html>
<html>
<head>
<title></title>
</head>
<body>
<h1 onmouseover="alert('Save a tree');alert('Help')">
树很重要
</h1>
</body>
</html>
```

#### 结果：第一个 alert 框，点击 OK 关闭它。

![](img/331e10bc8df06a94fc8288a269de6c23_24_0.png)

#### 结果：第二个 alert 框打开，点击 OK 关闭它。

![](img/331e10bc8df06a94fc8288a269de6c23_24_1.png)

现在我们可以添加 `<script>...</script>` 开启/关闭标签，以便在头部部分开始 JavaScript 编码，并在它们之间添加函数。

```html
<!DOCTYPE html>
<html>
<head>
<title>...</title>
<script>
function hi(){
........
}
</script>
</head>
<body>...</body>
</html>
```

"hi" 这个名字是一个虚构的名字，你可以根据喜好为你的函数命名任何名称，方便以后记忆。该函数是一段 JavaScript 代码，因为它包含在 `<script>...</script>` 标签中，并且以单词 `function` 开头。

上面的函数是空的，什么都不做；因为在开启/关闭的大括号 “{ }” 之间没有输入任何内容，大括号内保存了函数在被调用时要执行的代码。

### 非常简单的示例代码

![](img/331e10bc8df06a94fc8288a269de6c23_27_0.png)

使用分号不是必须的，但建议使用且这样更好，它在 JavaScript 中充当换行符并结束代码行。

将文件代码保存为 “.html” 或 “.htm” 并存放在你的文件夹中，将其命名为 “function” 或其他名称以便以后记忆。右键点击它打开，选择“打开方式”，我使用的是 Google Chrome。当你选择的浏览器打开它时，它是空白的，因为使用函数时你需要调用它们来执行你想要的操作，而我们还没有调用该函数。

现在使用你之前保存的同一个文件，打开它并向其中添加 “input” 标签。

```html
<!DOCTYPE html>
<html>
<head>
<title>...</title>
<script>
function hi(){
  alert("hi is the name of the Javascript function");
}
</script>
</head>
<body>
<input type="button" value="click here" onclick="hi()" />
</body>
</html>
```

> **注意**：“input” 标签被添加在 body 部分。

#### 结果

我们有了一个可点击的按钮，其 `onclick` 事件会执行放置在 HTML5 代码头部的函数 “hi()”。

![](img/331e10bc8df06a94fc8288a269de6c23_29_0.png)

一旦点击由于 HTML “input” 标签出现的 “click here”按钮，弹出框就会打开。点击 OK 关闭它。

`type` 和 `value` 是 input 标签的属性，两者都让按钮看起来像一个按钮，而事件处理器 “onclick” 被分配了函数的名称。

> **注意**：
> - JavaScript 是区分大小写的。
> - “input” 标签只是一个创建元素的标签，并且它是自闭合的。
> - 事件处理器 “onclick” 可以用于任何创建虚拟元素的标签。
> - 要执行函数并调用它，我们只需要在事件处理器中写上它的名称即可。

## 14. 总结

我们可以通过控制执行函数代码的时机来控制 JavaScript 的行为。放置在 HTML body 部分 `<script>...</script>` 开启/关闭标签在打开浏览器时会首先执行。

函数用于组织 JavaScript 代码，并放在头部部分的 `<script>...</script>` 标签之间，位于 `<body>` 开启标签上方。

为了标识函数，我们使用某些单词后跟你选择的名称，被调用时要执行的代码放在大括号之间。

事件处理器用于调用函数或（如果有多个需要执行的）函数。

## 15. 如何调试 JavaScript

JavaScript 是区分大小写的，确保你输入小心，否则它会被浏览器忽略。

- 引号嵌套错误可能会导致问题。
- 在事件处理器后使用引号：`event handler="..."` 或 `event handler='...'`。
- 在双引号内部使用单引号，在单引号内部使用双引号。
- 如果浏览器仍然不执行 JavaScript 代码，检查是否启用了 JavaScript。

访问此网站查看如何启用它：`http://www.enable-javascript.com/`

## 16. 介绍

JavaScript 代码本身可能看起来有些过时，但一旦你理解了它，你就可以对其进行改写以适应你的需求。编写它有需要遵循的规则。

理解 JavaScript 如何处理网页和文档是首要的一步，之后，你将理解 JavaScript 如何将网页和文档视为一组对象集合，这些对象具有属性和方法，并可以被用于处理当用户交互时发生的事件。

## 17. DOM

DOM 代表文档对象模型（Document Object Model）。它是网页文档的编程接口。它代表页面，以便程序可以更改文档的结构、样式和内容。

JavaScript 是区分大小写的，确保你输入小心，否则它会被浏览器忽略。

- 引号嵌套错误可能会导致问题。
- 在事件处理器后使用引号：`event handler="..."` 或 `event handler='...'`。
- 在双引号内部使用单引号，在单引号内部使用双引号。
- 如果浏览器仍然不执行 JavaScript 代码，检查是否启用了 JavaScript。

## 18. 属性

`type` 和 `value` 是 input 标签的属性，两者都让按钮看起来像一个按钮，而事件处理器 “onclick” 被分配了函数的名称。

> **注意**：
> - JavaScript 是区分大小写的。
> - “input” 标签只是一个创建元素的标签，并且它是自闭合的。
> - 事件处理器 “onclick” 可以用于任何创建虚拟元素的标签。
> - 要执行函数并调用它，我们只需要在事件处理器中写上它的名称即可。

## 19. 方法

使用分号不是必须的，但建议使用且这样更好，它在 JavaScript 中充当换行符并结束代码行。

将文件代码保存为 “.html” 或 “.htm” 并存放在你的文件夹中，将其命名为 “function” 或其他名称以便以后记忆。右键点击它打开，选择“打开方式”，我使用的是 Google Chrome。当你选择的浏览器打开它时，它是空白的，因为使用函数时你需要调用它们来执行你想要的操作，而我们还没有调用该函数。

现在使用你之前保存的同一个文件，打开它并向其中添加 “input” 标签。

```html
<!DOCTYPE html>
<html>
<head>
<title>...</title>
<script>
function hi(){
  alert("hi is the name of the Javascript function");
}
</script>
</head>
<body>
<input type="button" value="click here" onclick="hi()" />
</body>
</html>
```

> **注意**：“input” 标签被添加在 body 部分。

#### 结果

我们有了一个可点击的按钮，其 `onclick` 事件会执行放置在 HTML5 代码头部的函数 “hi()”。

一旦点击由于 HTML “input” 标签出现的 “click here”按钮，弹出框就会打开。点击 OK 关闭它。

`type` 和 `value` 是 input 标签的属性，两者都让按钮看起来像一个按钮，而事件处理器 “onclick” 被分配了函数的名称。

## 20. 练习

```html
<!DOCTYPE html>
<html>
<head>
<title>Object's Properties and Methods</title>
</head>
<body>
<script>
document.write(screen.width)</script><br>
document.write(navigator.platform)</script><br>
document.write(inner.innerHeight)</script><br>
document.write(document.lastModified)</script><br>
document.write(document.title)</script><br>
<label for="Address">Enter here:</label>
<input type="text" id="Address">
<input type="button" value="SUBMIT"
onclick="alert(document.getElementById('Address').value)">
<button onclick="window.close()">Close this window</button>
</body>
</html>
```

点击 OK 关闭。

`<label>... </label>` 标签是 HTML 标签，因此它是 HTML 代码。label 标签中的 `for="Address"` 部分应该与 `id` 属性相等，它不是必须的，且点击文本“Enter here:”时没有特殊作用，光标会移动到文本框，文本框可以被称为“控件”。“按钮”是一个我们可以点击的控件，它是与页面的交互。

在 `<input>` 标签中，`type="text"` 允许用户输入文本。

在 `<input>` 标签中，`onclick="..."` 创建一个带有 "SUBMIT" 值或单词的按钮……这是使用 `getElementById` 方法的事件处理器。

`<button>` 标签同样可以显示按钮，它是一个用于 `<input type="button">` 等控件的标签……使用 `close()` 方法执行关闭窗口，该方法适用于我们正在使用的浏览器。

## 21. 字面量与变量

不要被这个标题吓到，一旦我们开始练习一些示例，它非常简单。

字面量用于表示永远不会改变的值，通常被包含在引号中。

示例：`alert("Weather");` 浏览器中弹出一个带有引号内文本的警告框，字面意思就是所述的内容，一旦代码执行（我们已经看到），因此它是字面量。

![](img/331e10bc8df06a94fc8288a269de6c23_33_0.png)

#### 结果

![](img/331e10bc8df06a94fc8288a269de6c23_34_0.png)

在 `alert("Weather")` 或 `alert('Weather')` 中，“Weather”是字面量，因为它被包含在双引号或单引号中。

如果是：`alert(Weather)`，在这种情况下 Weather 就是变量名。

变量与字面量相反，因为它们的值可以改变。它们是存储数据值的容器。在 Google 首页上，文本框供我们输入想要搜索和查找的内容，一旦我们输入了想要的内容，它就会存储起来，或者我们使用其数据库查找我们正在寻找的信息。

JavaScript 中的变量语法是：`var name`。

名称可以是任何自定义的但唯一的，名称的唯一性被称为标识符，标识符可以是短名称，也可以更具体且具描述性，它们遵循一些规则：

- 在第一个字符之后，名称可以包含字母、数字、连字符或下划线。
- 必须以字母、美元符号 `$` 或 `_`（下线）开头。
- 区分大小写，尝试使用大小写组合变量名，使其符合逻辑并容易记忆和识别。
- 不允许为空或空格。
- 允许的标点符号仅连字符和下划线。

JavaScript 关键字不能作为变量或其他任何内容，它们是保留字，请查看表格获取这些保留字的列表：

| arguments | boolean | break | case | catch | default |
|---|---|---|---|---|---|
| delete | do | else | enum | export | extends |
| false | float | for | function | import | |
| in | int | native | new | null | |
| private | public | return | short | super | switch |
| this | try | typeof | var | void | |
| while | with | yield | | | |

> **注意**：具有特殊含义的 JavaScript 保留字比表中更多。

## 22. 在 JavaScript 中创建变量

关键字是 `var`，然后是变量名。

示例：`var weather`

在 JavaScript 中，必须定义变量，因此它必须位于 `<script> </script>` 闭合标签之间。

示例：

```html
<!DOCTYPE html>
<html>
<head>
<title></title>
</head>
<body>
<script>
var weather
alert(weather)
</script>
</body>
</html>
```

#### 结果

![](img/331e10bc8df06a94fc8288a269de6c23_35_0.png)

为什么我们得到 undefined ？

一个变量持有一个值，但如果变量没有值且我们没有给 `var weather` 赋予任何值，那么变量的值就是 `undefined`。

### 22.1 赋值给变量的值

变量持有可能会变化的信息，这被称为赋值给变量的值。变量名后面跟着 `=` 号，你可以在此处输入值。

`var name = value` 是创建变量并给其赋值值的方法。

`=` 符号有时被称为赋值运算符。

示例：

```html
<body>
<script>
  var weather = "Cold"
  alert(weather)
</script>
</body>
```

#### 结果

![](img/331e10bc8df06a94fc8288a269de6c23_36_0.png)

因为我们把 "cold" 作为值赋值给变量 `weather`，所以警告框显示 cold 而不是 undefined。

赋值的值可以是数字或其他。请记住，JavaScript 使用持有数据或信息的变量。

`var` 用于此目的，它存储稍后可以使用的信息。

## 23. 总结

与其他编程语言一样，JavaScript 包含了对象模型，并使用了可能会随时间改变的数据或信息的变量。

DOM，文档对象模型，定义了所使用的名称，例如。

## 24. 数字与日期

DOM，文档对象模型定义了所使用的名称，例如。

### 24.1 引言

DOM，文档对象模型定义了所使用的名称，例如。

## 25. 数据类型

DOM，文档对象模型定义了所使用的名称，例如。

### 25.1 字符串

DOM，文档对象模型定义了所使用的名称，例如。

### 25.2 数字

DOM，文档对象模型定义了所使用的名称，例如。

```html
<!DOCTYPE html>
<html>
<head>
<title>数字示例</title>
</head>
<body>
<script>
// 变量 numb 存储数字 9
  var numb = 9
// 变量 price 存储数字 3.99
  var price = 3.99
// 变量 total 乘以数字 9 和 3.99
  var total = numb + price
// 显示变量 total 的结果
  document.write(total);
// 使用 break 标签将结果显示在 2 行
  document.write("<br>");
// 只保留三位小数的乘法结果
  document.write(total.toFixed(3))
</script>
</body>
</html>
```

#### 结果

| 35.91000000000004 |
|---|
| 35.910 |

### 25.3 日期 (Dates)

在 JavaScript 中，我们可以使用和存储日期，方法是计算两个日期之间的过去、未来或中间的天数。为此，我们必须将其存储为日期对象。

此操作的语法与字符串和数字使用的语法不同。

`var name = new Date()`

通过逗号我们可以存储分开的值，例如：

`var name = new Date(year, month)`

你可以将年份替换为 4 位数字，并将月份替换为 0 到 11 之间的数字，因为 JavaScript 语言中的列表始终从 0 开始而不是 1，这在进行数学计算和提高代码运行速度是有意义的。

另一种存储日期是使用字符串（单引号或双引号）。

示例：`var name = new Date("November 16 2012")`

可以在日期中添加时间，只需在年份后加空格即可：

`hours minutes seconds`

示例：`var name = new Date("November 16 2012 14:25:00")`

14:25:00 代表下午 2:25。

示例：

```html
<!DOCTYPE html>
<html>
<head>
<title>存储日期的方法</title>
</head>
<body>
<script>
// 变量 birthday
var birthday = new Date()
// 存储日期和时间
var birthday = new Date(1975,11,16)
var vacation = new Date("November 28 2012")
var vacations = new Date("December 21 2013 14:45:00")
// 显示结果并使用 <br> 标签将其置于多行
document.write(birthday)
document.write("<br>")
document.write(vacation)
document.write("<br>")
document.write(vacations)
</script>
</body>
</html>
```

#### 结果：以特定格式存储的日期值。

Sun Feb 16 1975 00:00:00 GMT-0700 (Mountain Standard Time)

Wed Nov 28 2012 00:00:00 GMT-0700 (Mountain Standard Time)

Sat Dec 21 2013 14:45:00 GMT-0700 (Mountain Standard Time)

如果没有指定时间，则默认为午夜，即 00:00:00。

GMT 代表格林威治标准时间，是一个标准，其后的数字是与 GMT 相差的小时。

### 25.4 布尔数据类型 (Boolean data type)

一种非常简单的数据类型，只有两个值：`true`（真）或 `false`（假）。如果我们赋值了除上述两个值以外的值，它将返回 `false` 或 `true`。

我们通常需要类似于：YES / NO、ON / OFF、TRUE / FALSE 的数据类型，这适用于布尔数据类型，真实值为 `true`，非真实值为 `false`。

0、-0、"null"、NaN（表示不是数字）、undefined（未给变量名分配值），这些都将返回 `false`，但分配任何其他值将返回 `true`。

> **注意**：布尔值不加引号。

你可以将值设为 `false` 或 `true`。

示例：

```html
<!DOCTYPE html>
<html>
<head>
<title>布尔值 (Boolean)</title>
</head>
<body>
<script>
// 命名为 true
var name1 = true
// 命名为 false
var name2 = false
// 显示结果并使用 <br> 标签将其置于多行
document.write(name1)
document.write("<br>")
document.write(name2)
</script>
</body>
</html>
```

#### 结果

![](img/331e10bc8df06a94fc8288a269de6c23_41_0.png)

布尔（Boolean）术语源于乔治·布尔（George Boole），他是一位英国数学家，他的代数逻辑基于 0 和 1，所有现代计算都基于此。

布尔变量简单但实用，通过基于布尔变量的 `if...then...else` 决策，后台正在发生着我们看不见的事情。

## 26. 决策判断 (Decision Making)

编写简单决策代码的步骤是使用“if”语句，与人类做决策一样，但使用的是计算机理解的语言。

### 26.1 “ if ” :

规则：

- `if` 必须小写。
- 条件放在括号内。
- 语句体放在大括号内。

#### 示例

`var x = 5`

我们创建了一个名为 x 的变量并为其赋值了值 5，完全没有比较。

我们将数字 5 存储在名为 x 的变量中。让我们检查这种情况下的表格。

| 示例 | 返回值 |
|---|---|
| `x==5` | true |
| `x>5` | false |
| `x<5` | false |
| `x>=5` | true |
| `x<=5` | true |
| `x!=5` | false |

#### 示例代码

```html
<!DOCTYPE html>
<html>
<head>
  <title>if else语句</title>
</head>
<body>
<script>
  var score = 80;
  if (score > 73) {
    document.write("The score is high");
  } else {
    document.write("The score is low");
  }
</script>
</body>
</html>
```

#### 结果

![](img/331e10bc8df06a94fc8288a269de6c23_46_0.png)

if 代码执行了，是因为条件 `score >= 73` 为真，因此网页显示

The score is high。

某些测试条件并不简单，需要其他类型的运算符，称为“逻辑运算符”。

### 26.2 逻辑运算符

JavaScript 逻辑运算符用于建立变量之间的逻辑关系，或者允许测试许多条件以确定它们是否全部或部分为真。

让我们考虑两个变量，`x = 5` 和 `y = 9`。

| 运算符 | 含义 | 示例 |
| --- | --- | --- |
| `&&` | 与 | `(x < 7 && y > 4)` 为真 |
| `!` | 非 | `!(x == y)` 为真 |
| `||` | 或 | `(x == 3 || y == 3)` 为假 |

#### 更复杂的示例

如果我们看每一个步骤，它实际上非常简单。

```html
<body>
<script>
  var age = 90
  if (age <= 13) {
    document.write("cannot drive")
  } else if (age > 16 && age < 85) {
    document.write("can drive")
  } else {
    document.write("someone else should drive")
  }
</script>
</body>
```

#### 结果

![](img/331e10bc8df06a94fc8288a269de6c23_47_0.png)

#### 解释

`var age = 90`（创建一个名为 age 的变量并将 90 存储为值）。

```javascript
if (age <= 13) {
  document.write("cannot drive")
}
```

这意味着如果 age 小于或等于 13，该人不能开车，由于 90 超过了该值，所以不会发生。

```javascript
else if (age > 16 && age < 85) {
  document.write("can drive")
}
```

这意味着如果 age 大于 16 且小于 85，该人就可以开车，但并非如此，因为 var age 被设置为 90。

```javascript
else {
  document.write("someone else should drive")
}
```

因此，将执行 else 语句，网页显示 someone else drive。

## 27. 总结

- JavaScript 语言存储数据以创建交互式网页。
- 布尔值为 `true`（真）或 `false`（假）。
- 日期诸如月、日、年或简单的时间。
- 数字是标量值。
- 字符串是如文本。

`if...else` 逻辑允许代码根据变量的值做出决策，这有助于开发网站等。

## 28. 站点搜索

让我们从常用的 HTML 控制、HTML5 标签和编码开始，实现搜索。

在我的情况下，打开记事本编辑器或你选择的任何编辑器并开始编码。

### 示例

文件 编辑 格式 查看 帮助

```html
<!DOCTYPE html>
<html>
<head>
<title>搜索网页</title>
</head>
<body>
<script>
<p>Searching the web
<input type="text" id="wordoffsetof" autofocus>
<input type="button" onclick="search()" value="find">
</p>
</script>
</body>
</html>
```

![](img/331e10bc8df06a94fc8288a269de6c23_49_0.png)

当我们将其保存为 .html 后在浏览器中打开时什么都没有显示，为什么？因为我们需要 JavaScript 代码来让搜索发生并进行。因此，在 `</title>` 标签下方、`</head>` 标签上方，我们需要添加 `<script>` 标签，然后通过添加 `</script>` 标签将其关闭。

```html
<html>
<head>
<title>Searching the web</title>
<script>
</script>
</head>
```

在 input 标签中使用 `onclick="search()"` 是为了让代码在点击按钮后找到 search 函数。

```html
<html>
<head>
<title>Searching the web</title>
<script>
function search() {
}
</script>
</head>
```

注意，现在我们有一个 JavaScript 函数 `()`，但它仍然什么都不做，因为它是空的。执行的代码包含在起始括号和结束括号之间。当调用函数时，文本框完全没有填写且仍然是空的，使用 alert 提醒用户输入。获取用户输入的内容 URL（统一资源定位符：...）并将其放在地址栏，你可以使用任何网站名称来开始搜索，如果你有自己的网站，可以在大括号之间编码，你可以使用注释。

```javascript
<script>
function search() {
  // 使用任何网站名称
  var site = "dictionary.org";
}
</script>
```

为了获取用户在文本框中输入的内容，我们使用 `getElementById`，在我们的示例中 input 标签有 `id="wordtofind"`，我们可以获取它的值。将此添加到代码中。

```html
<html>
<head>
<title>Searching the web</title>
<script>
function search() {
  // 使用任何网站名称
  var site = "dictionary.org"
  // 用户输入的文本
  var find = document.getElementById("wordtofind").value;
}
</script>
</head>
</html>
```

添加了一个变量 find，它将存储用户在文本框中输入的数据。

### 28.1 搜索

如果用户在文本框中输入文本，代码将执行搜索，如果为空则用户将收到 alert 提示输入内容。和之前一样添加 if else 块。

```html
<html>
<head>
<title>Searching the web</title>
<script>
function search() {
  // 使用任何网站名称
  var site = "dictionary.org"
  // 用户输入的文本
  var find = document.getElementById("wordtofind").value;
  // 添加 if...else 块，情况为空
  if () {
  } else {
  }
}
</script>
</head>
```

> **注意**：最后一个大括号关闭了整个代码块，它属于代码。

```javascript
function search () {
  // 执行代码块
}
```

使用 if 是根据文本框是否为空来做出决策。我们有一个名为 find 的变量，因此文本框中的任何内容都是字符串类型。

### 28.2 Length 属性

使用语法 `string.length` 来查找用户输入的字符串长度。length 属性允许你这样做，它确定字符的数量，如果文本框为空，结果将显示为 0（数字）。

示例:

![](img/331e10bc8df06a94fc8288a269de6c23_51_0.png)

结果:

![](img/331e10bc8df06a94fc8288a269de6c23_51_1.png)

> **注意**：空格也是一个字符，我们有字符串 "Hi there"。代码发送一个 URL（统一资源定位符），当执行搜索时这是一个地址，因此 Google 搜索并找到它，我们还可以在搜索文本框中输入网站名称。编程语言中的字符串拼接用于连接两个更多的字符串。

## 29. 字符串拼接

字符串是文本，拼接意味着“将事物连接在一起”，就像链一样。假设我们有两个字符串 Hi 和 There，把它们拼接在一起就会得到 Hi There，就如此。

要拼接只需使用 JavaScript 的 `+` 运算符。

在字符串（而不是数字）的情况下，`+` 运算符将两个或多个字符串连接成一个，例如：`"Hi" + "There"` 让我们得到一个单一字符串 `"Hi There"`。

示例:

```html
<body>
<p>点击按钮连接字符串</p>
<button onclick="myFunction()">点击这里</button>
<p id="test"></p>

<script>
function myFunction() {
  var string1 = "Hi ";
  var string2 = "There!"
  var string3 = " How are you?"
  var result = string1.concat(string2,string3);
  document.getElementById("test").innerHTML = result;
}
</script>
</body>
```

#### 结果

![](img/331e10bc8df06a94fc8288a269de6c23_53_0.png)

一旦点击按钮，下方的句子就会出现。`String.concat()` 方法非常简单，它返回现有字符串的新字符串。

## 30. 下拉列表

使用 HTML 控制和 JavaScript 增加一个包含用户选择和选项的下拉列表是有帮助的。许多网站都有下拉列表，这些控件只是一个侧边带有箭头的文本框，通过点击箭头，选择列表就会出现。要添加下拉菜单或列表，我们使用 HTML 的起始和结束标签：`<select>...</select>` 和 `<option>...</option>`。通过向 `<select>` 标签或元素添加 id，允许通过 JavaScript 从列表中进行选择，控件需要一个 ID 名称，因为 JavaScript 只通过 ID 查找控件。`<select>` 元素内部的 `<option>` 标签（其本身是一个能够收集用户数据的控件）列出了列表中的方便选项。每个选项可以使用一个具有唯一项目的值，JavaScript 通过所选项目的值来确定用户选择了哪种选择。结束控件使用 `</select>` 结束标签。

在此搜索： 选择： 点击

为了显示下拉列表，我们按照前面提到的添加了 `<select>` 控件，它需要一个 ID 以便 JavaScript 获取选中的项目。该 ID 是一个自定义名称，区分大小写，没有空格，且必须以字母开头。

```html
<body>
<p>Search here:
  <input type="text" id="texttofind" autofocus>
  <!-- search textbox and text -->
  &nbsp;Pick:
  <select id="dropdownlist">
</select>
  <input type="button" onclick="search()" value="Click">
</p>
</body>
```

#### 结果

在此搜索： 选择： 点击

现在让我们添加 `<option></option>` 闭合标签来列出下拉列表中供选择的项目，我们还将为每个选项添加一个带有（或不带）数字的唯一 `value` 属性，以便 JavaScript 根据用户的选择做出关于后续步骤的决策。

带有值的 `<option></option>` 标签被添加在 `<select></select>` 闭合标签之间。

### 示例

```html
<body>
<input type="text" id="texttofind" autofocus>
<!-- Drop down list -->
&nbsp;Pick:
<select id="dropdownlist">
<option value="blue">Blue</option>
<option value="yellow">Yellow</option>
<option value="green">Green</option>
<option value="red">Red</option>
</select>
<input type="button" onclick="search()" value="Click">
</body>
```

#### 结果

![](img/331e10bc8df06a94fc8288a269de6c23_55_0.png)

点击箭头：

![](img/331e10bc8df06a94fc8288a269de6c23_55_1.png)

添加了选择或下拉列表，用户可以通过点击箭头然后选择他需要的任何值。

### 30.1 默认选择及其更改

> **注意**：在这种情况下，蓝色在选择框中首先显示，但你可以将任何想要首先显示的项目移到顶部，你只需要在编码时将其放在第一组 `<option>...</option>` 标签中即可。

项目的顺序不是强制要求的，但可以用来使用，例如从最小到最大的数字排序，或者表达式的字母顺序。

> **注意**：还有另一种在不重新排列项目的情况下选择默认值的方法。

让我们在不改变项目顺序的情况下，将黄色设置为下拉框中的默认搜索项。

#### 示例

```html
<option value="yellow" selected>Yellow</option>
```

#### 结果

![](img/331e10bc8df06a94fc8288a269de6c23_56_0.png)

**正如你所看到的，只需在值“yellow”之后、option 标签的 “>” 之前添加带空格的 `selected`，黄色就会成为选择列表顶部的项目。当然，蓝色仍在列表中，但它不再是默认值了。**

![](img/331e10bc8df06a94fc8288a269de6c23_56_1.png)

## 31. 总结

- 字符串拼接用于使用 JavaScript `+` 运算符将两个或多个字符串合并为一个单一字符串。
- 使用 HTML 的 `<select>` 和 `<option>` 标签显示下拉列表。
- 在 `<option>` 标签中使用 `selected` 允许从下拉列表中选择默认项目。

## 32. 简介

HTML 使用 `<audio>` 和 `<video>` 标签来处理声音和视频，不需要各种声音和媒体播放器的插件。

但 JavaScript 提供了更多的控制和自由来使用这些元素，它不仅仅是显示它们，还添加了必要的且有趣的背景和音效。

如果你有一些声音和媒体文件，可以随意使用，否则你可以从互联网下载免费的资源用于学习。

## 33. 声音

声音有许多格式，文件扩展名就是它的格式。例如：

MP3, MP4, WAV 等……它们之间的区别在于不损失质量的情况下压缩音频文件的方式。大多数公共领域的方法和技术都没有专利，例如大多数浏览器都支持的 MP3。

另一方面，如果格式没有专利且可以免费使用，那么歌曲或产品就受版权保护，意味着不允许分发；幸运的是，有些是公共领域且免费使用的。

让我们开始使用 HTML5 编码并使用其所需的标签：

```html
<!DOCTYPE html>
<html>
<head>
<title></title>
</head>
<body>
</body>
</html>
```

使用记事本或你选择的任何文本编辑器并将 HTML5 代码文件保存为 `sound.html` 或 `sound.htm`。

### 注意

检查你的浏览器是否处理 HTML5 音频，用于对象检测的语法简单：

```javascript
if (window.HTMLAudioElement) {
    // 在此处编写你的代码
}
```

## 34. 播放器的创建

为了控制声音，我们需要 HTML5：

```javascript
if (window.HTMLAudioElement) {
    var player = document.getElementById("id");
}
```

用于对象检测的语法简单：

```javascript
if (window.HTMLAudioElement) {
    var player = document.getElementById("id");
}
```

## 35. 兼容性检查

在 JavaScript 中检查兼容性：

```javascript
if (player.canPlayType().length > 0) {
    // 在此处编写代码
}
```

## 36. 方法：setAttribute()

`setAttribute` 方法允许在 JavaScript 中设置属性值。

```javascript
element.setAttribute(attributename, value)
```

```html
<audio src="eat.mp3" controls>
</audio>
```

# 或者：

```html
<audio controls>
<source src="eat.mp3">
</audio>
```

#### 结果

![](img/331e10bc8df06a94fc8288a269de6c23_60_0.png)

`<audio>` 标签的常用属性包括：

- `src`: 它的值就是音频文件的 URL。
- `controls`: 如果包含此属性，音频文件将拥有控制控件，这非常实用，它的值就是 "controls"。
- `loop`: 音频结束后，它将重新开始。
- `preload`: 它有三个参数：auto、metadata 和 none。

> **注意**：为了让文件在所有浏览器中都能正常工作，我们使用了 `<source>` 元素。

### 示例

```html
<audio controls>
<source src="eat.mp3">
</audio>
```

## 37. JavaScript音频

```html
<audio src="soundfile">
</audio>
```

soundfile 将被替换为你选择的音频文件，`src` 是一个设置值的属性，可以在 JavaScript 中使用 `setAttribute` 来告诉它要播放哪一个声音文件。

## 38. 音效

在响应事件时播放声音，例如点击按钮时。

让我们创建一个按钮并编写函数代码，当按钮被点击时调用该 JavaScript 函数。

```html
<button onclick="play()">试一下</button>
```

```javascript
function play() {
  if (window.player) {
    player.play();
  }
}
```

当我们调用函数 `play()` 时，事件就会被执行。在段代码示例中，当点击按钮时，系统会寻找名为 player 的对象，这就是使用 `if (window.player)` 的原因。

如果找到了对象，结果为 true，`.play()` 方法会让 HTML5 播放音频播放器并执行；但如果没找到，则返回 false。

### 注意

最新版本的 HTML 称为 HTML5，它拥有以前不具备的控件。浏览器可以播放 HTML5 音频，并不意味着它具备显示范围控件的能力。

`window.HTMLAudioElement` 允许访问 `<audio>` 方法和元素属性以进行操作。

`if(window.HTMLAudioElement)` 用于测试浏览器是否处理 HTML5 输入控件。

## 39. 应用 CSS

CSS 用于网站样式化，并可以使用 JavaScript 进行控制，JavaScript 具有智能方式做出决策的能力。但 JavaScript 和 CSS 中使用的属性名称并不总是相同的，这很遗憾。在 JavaScript 中，我们需要去掉连字符（hyphen）并将后的第一个字母大写。

### 属性对照表

| CSS 属性 | 说明 | JavaScript 属性 |
| --- | --- | --- |
| background | 指定背景属性 | background |
| background-color | 指定背景颜色 | backgroundColor |
| background-image | 指定背景图像 | backgroundImage |
| background-size | 指定背景大小 | backgroundSize |
| border-color | 指定边框颜色 | borderColor |
| color | 指定文本颜色 | color |
| font-family | 指定文本字体族 | fontFamily |
| font-size | 指定字体大小 | fontSize |
| text-align | 指定文本水平对齐方式 | textAlign |

## 40. 总结

- HTML5 音频不需要插件即可播放。
- `<audio>` 标签允许通过 JavaScript 控制音频对象。
- 在支持的浏览器中可以创建音频对象。
- `.canPlayType()`、`.play()` 和 `.pause()` 方法允许控制播放器何时播放什么。
- `.setAttribute` 允许为任何 HTML 标签赋值。
- `.style` 属性允许通过 JavaScript 将 CSS 应用到元素上。

## 41. 数组与循环

### 41.1 创建数组

在编程中，你有时需要处理项目列表，最好的方法是在列表中包含一组文件名，因此，通过它们在列表中的位置来处理它们更容易，这些位置可以用数字表示，而计算机非常非常擅长理解数字。

项目列表对编程语言是可见的而对人类不是，可以通过编程语言进行访问和操作。我们将这种列表称为数组（array），以区别于页面上的可见列表。

#### 1) JavaScript 数组

JavaScript 中的数组对象拥有属性和方法，有助于处理存储在数组中的数据，这些数组只是计算机内存中的列表。

数组是一种可以同时持有多个值的变量。

##### 代码

```javascript
var name = new Array()
```

其中 name 将替换为你选择的变量名，该变量名必须以字母开头，不能有空格或符号。这段代码告诉 JavaScript 创建数组的意图。

在 `Array()` 中我们使用了大写的 `A`，这在 JavaScript 的对象命名中很典型。

我们需要赋值运算符 `=`，所有项目都有相同的名称，为了区分它们，我们只需要在方括号中给每个项目一个数字。

数字从 0 开始，依此类推……而不是 1，所以 `[0]` 是数组中的第一个元素，`[1]` 是第二个元素。

我们可以在同一个数组中拥有不同类型的变量，我们可以拥有名称、对象、函数、数组等……

##### 数组编码示例

```html
<!DOCTYPE html>
<html>
<head>
<title>Array coding</title>
</head>
<body>
<p id="test"></p>
<script>
var cars = new Array("BMW", "Mazda", "Mercedes");
document.getElementById("test").innerHTML = cars;
</script>
</body>
</html>
```

#### 2) 数组方法

a) **sort() 方法**：按字母顺序对数组元素进行排序。

b) **reverse() 方法**：反转元素相对于先之前的顺序。因此，如果使用了 `.sort()` 方法，`.reverse()` 方法将把元素按降序排列。

##### 示例

```html
<body>
<p>点击反转数组中元素的顺序。</p>
<button onclick="myFunction()">点击我</button>
<p id="test"></p>

<script>
var cars = ["BMW", "Mazda", "Mercedes"];
document.getElementById("test").innerHTML = cars;

function myFunction() {
cars.reverse();
document.getElementById("test").innerHTML = cars;
}
</script>
</body>
```

**结果**：一旦点击按钮，元素将按字母顺序降序排列。

你可以将 `.sort()` 和 `.reverse()` 的代码结合起来获得相同的结果，而默认情况下，第一种方法将数组内的元素按升序排列，第二种方法则反转顺序。

数组可以以创意的方式在应用和网站中变得酷炫，但最酷的莫过于对数组进行**循环**。

c) **join() 方法**：

将数组元素连接成一个字符串。

##### 示例

```html
<body>
<p>将数组元素连接成字符串。</p>
<button onclick="myFunction()">点击我</button>
<p id="test"></p>

<script>
function myFunction() {
  var cars = ["BMW", "Mazda", "Mercedes"];
  var z = document.getElementById("test");
  z.innerHTML = cars.join();
}
</script>
</body>
```

如果不添加 var z 或任何其他变量名，代码可以更简单，不加它也能正常工作，`.join()` 方法是为了演示目的，因此添加了一个变量名。

```javascript
<script>
function myFunction() {
  var cars = ["BMW", "Mazda", "Mercedes"];
  document.getElementById("test").innerHTML = cars;
}
</script>
```

#### 结果

.join() 方法的另一个示例：

```javascript
<script>
function myFunction() {
  var cars = ["BMW", "Mazda", "Mercedes"];
  var z = document.getElementById("test");
  z.innerHTML = cars.join(" or ");
}
</script>
```

### 41.2 循环

与许多编程语言一样，JavaScript 拥有循环，循环由重复执行多次的代码块组成，直到达到特定条件。它有助于节省时间并避免重复编写相同的代码，它们被用于访问数组中的元素，循环有两种类型。

#### 1) JavaScript for 循环

它用于创建循环，并在指定的次数内提供重复的手段，同时对某些变量的值进行递增或递减，因此它提供了正向或反向计数的可能性，也可以从任何数字开始和结束。

我们使用 for 语句作为计数器，我们需要起始点（即计数开始的初始值）、用于测试循环是否继续的条件，以及如果条件为真，则在循环完全执行后要执行的递增或递减操作。

```javascript
for (start, condition, increment or decrement) {
  // 要执行的代码
}
```

> **注意**：for 循环的所有部分同时发生。

- `i` 是计数器变量的标签，用于计算循环运行了多少次。
- 决定循环是否继续执行的条件通常包含计数器变量。
- 在每次循环后，计数器变量都会递增或递减。

然后是每次循环要执行的代码。

示例：

```javascript
for (start, condition, increment or decrement) {
  // 要执行的代码
}
```

对于 start 部分，让我们用一个名为 i 的变量来替换并给它一个初始值。

对于 condition 部分，让我们设置循环停止重复的时机。

对于 increment 部分，让我们设置递增或递减的量，我们可以使用 `++` 将值递增或递减 1。

最后是每次要执行的代码。

```html
<!DOCTYPE html>
<html>
<head>
<title>循环</title>
</head>
<body>
<script>
for (var i = 0; i <= 6; i++) {
  document.write(i + "<br>");
}
</script>
</body>
</html>
```

**结果**：我们看到从 0（起始点）到 6 的数字被列出来。

```
0
1
2
3
4
5
6
```

`var i = 0`：名为 i 的变量从值 0 开始。

`i <= 6`：只要它小于或等于 6 就会继续。

`i++`：将值递增 1。

`document.write(i + "<br>");`

**结果**：我们看到从 0（起始点）到 6 的数字被列出来。

当 `i < 9` 时，循环执行代码块：

![](img/331e10bc8df06a94fc8288a269de6c23_75_0.png)

结果是 3

结果是 4

结果是 5

结果是 6

结果是 7

结果是 8

#### 2) do/while 循环的另一个示例

```html
<body>
<script>
do {
  // 用户输入其名字。
  var name = prompt("Please type your name", "");
  // 如果框为空，则再次询问。
} while (name == null || name.length < 1)
// 在页面上回复 Hi。
document.write("Hi " + name);
</script>
</body>
```

**结果**：因为由于脚本紧跟在 `<body>` 标签之后，它会在页面打开时立即执行，提示框会立即出现。我使用的是 IE 浏览器，所以对话框的出现取决于你使用的浏览器，但无论如何都会弹出一个框供用户填写姓名。尝试在不输入任何内容的情况下关闭或取消它，对话框会一直出现，直到你输入一些内容。完成后，点击 OK。

> **注意**：在 Google Chrome 和 Firefox 浏览器中，点击取消或关闭时会返回“Hi null”。

IE（Internet Explorer）代码输出：

![](img/331e10bc8df06a94fc8288a269de6c23_75_1.png)

一旦点击 OK，我们就会获得框中输入的 Hi + name。

![](img/331e10bc8df06a94fc8288a269de6c23_75_2.png)

> **注意**：我们经常使用 `window.prompt()` 方法在进入页面之前通过提示框输入值，并可以选择丢弃窗口前缀，其语法为：
>
> `window.prompt("text of choice", "default text");`
>
> `prompt()` 方法的第一部分 "text of choice" 用于指令说明，另一部分 "default text" 是已经输入到文本框中的值，在我们的代码中它是一个空字符串 `""`，这留了文本框为空。
>
> 用户可以选择在输入内容后点击“OK”或点击“cancel”继续。如果点击“cancel”或“close”，则会返回 null。

Google Chrome 代码输出：

![](img/331e10bc8df06a94fc8288a269de6c23_76_0.png)

结果：一旦点击取消，它将返回值 null。

![](img/331e10bc8df06a94fc8288a269de6c23_76_1.png)

如果在不输入任何内容的情况下点击 OK，它将保留值 " "，即长度为 0 的空字符串。框会短暂关闭，然后由于 do 循环的条件又会再次弹出来：

```javascript
} while (name == null || name.length < 1)
```

如果变量 `name` 等于 null 且其长度小于 1，提示框将持续出现，直到框中输入了某些内容并点击了 OK 按钮，这一切意味着条件已满足。

如果用户输入了内容，一旦点击 OK，变量就会获取该内容作为值。

- 两种循环之间的区别：

do 循环至少执行一次语句（即代码本身），而 while 循环可能不执行，因为决策是在开始或开头做出的。

### 重要

确保条件最终求值为 false，如果不是这样，循环将永远不会停止，某种意义上说这是一个无限循环，因为我们必须关闭浏览器或使用新页面。目标是编写一个根据需要重复次数以完成所需任务的循环，不同于涉及计数的 for 循环。

这是交互式应用和网页的很大部分。JavaScript 提供了其他决策方式来重复或不重复循环，即 `switch` 语句和三元运算符，它们涉及编写代码来做决策。

## 42. JavaScript switch 语句

允许从一组可能的情况中执行并选择单个语句块。它的作用类似于 `if...else` 语句，但提供了更短、更易用的语法。

语法：

```javascript
switch(expression) {
  case n1:
    // 要执行的代码块
    break;
  case n2:
    // 要执行的代码块
    break;
  default:
    // 要执行的默认块
}
```

`expression` 代表包含值的变量名，作为情况（n1, n2 等）。——意味着你可以有更多的 `case` 语句。如果检测到某个 `case`，相关的代码块将执行到 `switch` 语句的底部；`default` 代码块是可选的，只有当其他一个 `case` 语句为真时才执行该代码。

## 43. JavaScript 中的 parseInt() 函数

解析字符串并返回整数，如果无法转换第一个字符，它将返回 NaN，代表“Not Number”（非数字）。

示例代码：

```html
<head><title>switch 语句代码</title></head>
<script>
function switchsample() {
  // 从文本框获取值。
  var number = parseInt(document.getElementById("textEntry").value);
  // 以字符串形式确认信息。
  var info
  switch (number) {
    case 1:
      info = "one";
      break;
    case 2:
      info = "two";
      break;
    case 3:
      info = "three";
      break;
    default:
      info = "It should be a number";
  }
  // 找到结果。
  document.getElementById("output").innerHTML = info;
}
</script>
<body>
<p>Enter a number:</p>
<input type="text" id="textEntry" />
<button onclick="switchsample()">Submit</button>
<p id="output"></p>
</body>
</html>
```

> *(注：由于原文文本中 50 部分的 HTML 代码似乎不完整或存在错乱，此处根据逻辑进行了合理的结构化对齐和翻译，以符合文档工程师的专业处理。)*

**更正说明**：提供的原文中 50 部分的 HTML 存在严重的格式混乱（标签未闭合或逻辑错位），作为高级文档工程师，我根据其逻辑意图在翻译时进行了修复，以确保译文文档的可读性。

```html
<script>
function myFunction() {
  var age, driving = document.getElementById("age").value;
  if (age < 16) {
    driving = "Cannot drive";
  } else {
    driving = "Can drive";
  }
  document.getElementById("test").innerHTML = driving + " the car.";
}
</script>
```

#### 结果

![](img/331e10bc8df06a94fc8288a269de6c23_81_0.png)

## 44. 总结

数组只是通过数字访问的变量列表，循环用于多次执行某行或多行代码，直到满足特定条件，而 switch 语句和三元运算符提供了一种替代的决策方式。

## 45. 定时器与过渡

### 45.1 引言

定时器是 JavaScript 事件，通常我们希望速度变快而不是变慢，但唯一的例外是需要减速时的过渡过渡效果，这样人们就能以慢动作捕捉正在发生的变化。我们可以使用 JavaScript 定时器来实现，但 CSS3 提供了定时器，提供了带有减速可能的时间控制，这样我们就不完全依赖 JavaScript 的动画效果。

### 45.2 定时器或计时事件

允许代码执行延迟，JavaScript 在执行某些函数之前会等待，代码将在精确的时间间隔内通过调用计时事件来执行。

使用定时器有两种方式：

- `setTimeout()`: 括号中包含执行一次的函数，以及以毫秒为单位的精确秒数。
- `setInterval()`: 括号中包含以毫秒为单位、在精确时间间隔内重复执行的函数，类似于循环，但带有时间延迟。

> **注意**：`setTimeout()` 和 `setInterval()` 是 HTML DOM（文档对象模型）的方法。

该函数是要执行的 JavaScript 函数，而毫秒是 1 秒的 1/1000。

`setTimeout()` 和 `setInterval()` 是窗口事件的方法，它们可以带有 `window` 和点 `.` 编写，例如 `window.setInterval()` 和 `window.setTimeout()`，这在 JavaScript 中是可以省略的，因此直接使用 `setInterval()` 和 `setTimeout()` 是可以的。

#### 3) 给定时器赋值的语法

```javascript
var name = setTimeout("JavaScript function", delay in milliseconds);
var name = setInterval("JavaScript function", delay in milliseconds);
```

你可以选择变量名称，使用 `setInterval()` 的代码与 `setTimeout()` 相同，一旦定时器与变量名连接，你就可以通过以下方式停止它：

`clearInterval(定时器的变量名)` 或 `clearTimeout(定时器的变量名)`。

### 示例 1：设置执行时间间隔

```html
<!DOCTYPE html>
<html>
<body>
<p>警框每隔 5 秒连接打开一次。</p>
<p>关闭窗口以停止持续的警框。</p>

<button onclick="setInterval(function() { alert('How are you?');},5000);">点击</button>
</body>
</html>
```

#### 结果

![](img/331e10bc8df06a94fc8288a269de6c23_82_0.png)

> **注意**：
> 每当你关闭警框时，5 秒钟后它又会再次打开，因此你需要关闭浏览器窗口。

### 示例 2：使用 `setInterval()` 方法每 3 秒显示一次当前时间

```html
<p id="test"></p>
<script>
var clock = setInterval(function(){currentTime()},3000);

function currentTime() {
var date = new Date();
document.getElementById("test").innerHTML =
date.toLocaleTimeString();
}
</script>
</body>
```

**结果：下午 7:02:01 之后**是下午 7:02:04，然后是下午 7:02:07，以此类推，每 3 秒一次。

![](img/331e10bc8df06a94fc8288a269de6c23_83_0.png)

> **注意**：显示时间的秒部分将每 3 秒执行一次，并显示 3 的倍数。
>
> **尝试**将时间改为 5000（即 5 秒）或你想要的任何数字。

## 结论

学习作为脚本语言的 JavaScript，其基础和基本原理非常简单，对于开始学习复杂的编译型编程语言非常有帮助。
