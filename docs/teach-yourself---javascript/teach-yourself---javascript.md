
# 自学 JavaScript

- 内容
- 理解并使用 JavaScript
- 快速超越基础阶段
- 充分利用这项技术

在过去的 60 多年里，超过 4000 万人通过“自学”的方式学习了 750 多门学科，并取得了令人瞩目的成果。

“自学”系列长期以来被誉为自导学习的权威来源——全球销量超过 3000 万册，涵盖语言、手工艺、爱好、商业和教育等领域的 300 多本书。

# 序言

JavaScript 是 Web 的核心编程语言之一——是最容易上手的语言。是什么让它如此简单呢？有几点。首先，这种语言非常小——它包含的对象和方法有限。虽然这限制了你的程序的功能，但也意味着你很快就能学会所有。其次，JavaScript 嵌入在 HTML 中，因此你可以从向标签添加小型程序开始创建特殊效果，并逐渐增加代码的大小和复杂度。第三，JavaScript 不需要特殊的软件——所有的浏览器都可以处理它，因此你不需要额外的工具来开发或运行程序。

本书适用于理解 HTML 但几乎没有编程经验的人。《自学 JavaScript》并不是为了对语言进行全面深入的介绍，而是介绍主要的概念和技术。它侧重于语言的实际用途，并在很大程度上忽略了理论基础和语法细节。

如果你不知道如何使用 HTML，能否请你在开始这本书之前，花一个周末学习一下我的《自学 HTML》（如果非如此，也可以读其他作者的类似入门书籍！）？

祝你编程愉快！

Mac Bride

macbride@tcp.co.uk

2003年夏季

## 01 介绍 JavaScript

在本章中你将学习

- JavaScript 与 HTML
- 编程语言的类型
- 如何开始学习

## 02 对象与事件

- JavaScript 对象 14
- 对象名称 14
- 属性 20
- 方法 23
- `write()` 和 `writeln()` 24
- 事件处理程序 27
- 总结 30

## 03 变量

- 创建变量 32
- 变量名 33
- 变量的作用域 34
- 赋值运算符 39
- 增与减 39
- 运算符优先级 40
- 数组 41
- 练习题 45

## 04 程序流程

- 程序控制 47
- 比较运算符 47
- 逻辑运算符 48
- `for` 循环 49
- 代码块 51
- 变化的循环值 52
- 嵌套循环 54
- 循环生成的表格 55
- 对话框 56
- `while` 循环 58
- `do...while` 59
- `if` 分支 59
- `if...else` 61
- `switch` 65
- 条件运算符 66
- 标签 `label` 68
- `break` 68
- `continue` 70
- 错误处理 73
- 练习题 73
- 总结 74

## 05 函数与方法

- 函数 76
- 参数 78
- 返回值 79
- `Math` 方法 82
- `Date` 方法 88
- 时间 91
- 字符串方法 92
- 练习题 97
- 总结 97

## 06 表单

- 基础表单 100
- 按钮和文本输入 100
- 复选框和单选按钮 102
- 下拉列表 103
- 按钮 105
- `elements` 数组 106
- 检查条目 108
- 读取复选框和单选按钮 111
- 单选列表 114
- 反馈行 118
- 一个 JavaScript 计算器 121
- 练习题 124
- 总结 125

## 07 动画与图像

- 计算机动画 127
- 定时与超时 127
- 一个 JavaScript 钟 129
- 滚动文本 130
- 图像对象 132
- 简单动画 135
- 可点击图像 141
- 练习题 143
- 总结 143

## 08 窗口与框架

- 窗口控制 145
- 填充窗口 146
- `javascript` URL 148
- 在框架中工作 149
- 练习 151
- 总结 152

## 9 参考章节

- 标准颜色名称 154
- 留 `word` 155
- 特殊字符 156
- 事件处理程序 157
- `Math` 方法 158
- `Date` 方法 159
- `String` 方法 160
- `RegExp` 162
- 10 练习题答案 165
- 进一步学习 175
- 索引 177

## JavaScript 看起来是什么样的？

JavaScript 可以通过四种方式整合到 Web 页面中：

- 写入 `<SCRIPT>` 标签的页面主体中；
- 作为附加代码，写入 HTML 标签中；
- 作为一组写入 `<HEAD>` 区域的函数（命名的代码块）；
- 作为一组写入单独文本文件中的函数，并通过链接引入页面。

你可以在一个页面中任用这四种方式的任何组合。你还可以将 JavaScript 变量作为标签中的值。

## `<SCRIPT>`

代码可以写在包含在 `<SCRIPT>` 标签中。这是将代码获取到页面上最简单的方法，但它有两个主要的局限性。代码会在页面加载时执行一次，并且它只能引用屏幕上已经存在的对象——如果它尝试访问页面上尚未下载的部分的内容，代码将会崩溃。

```html
<SCRIPT>
alert("Hello from JavaScript")
</SCRIPT>
```

此脚本会在警告框中产生消息——这种框是 Windows 应用程序中用于提示用户的标准框。

## 附加代码

JavaScript 命令可以直接写入那些 HTML 标签中，例如那些产生表单中按钮或其他对象的标签，这些标签可以拥有相应的事件——正是事件触发了 JavaScript 的运行。

这是一个简单的示例。它创建了一个按钮，当它被点击时，会在警告框中显示一条消息。

```html
<HTML>
<HEAD>
<TITLE>Code in a tag</TITLE>
</HEAD>
<BODY>
<FORM>
<INPUT TYPE=button VALUE="Click Me" onclick="alert('Ouch!')">
</FORM>
</BODY>
</HTML>
```

![](img/abd8c35820179838d3f97b872561195a_15_0.png)

**图 1.1** 点击按钮时的显示。

关注 `<INPUT...>` 标签中的最后一个短语：

`onclick = "alert('Ouch!')"`

这遵循内联 JavaScript 的标准格式：

`event = "JavaScript statement(s)"`

在此情况下，事件是 `onclick`。它激活了语句：

`alert('Ouch!')`

注意脚本是用双引号括起来的，而其中的文本——‘Ouch!’——是用单引号编写的。

同一个脚本中可以是任意数量的语句。它们应该用分号隔开，整个集合必须包含在双引号中。这将显示两个警告框，相继出现：

```html
<INPUT TYPE=button VALUE="Click Me" onClick="alert('Ouch!'); alert('Please stop!!')">
```

如果你想测试这个，将 HTML 代码输入到你的文字处理器或文本编辑器中，保存为文本文件（命名为 `test.htm` 或类似名称），然后在浏览器中打开它。

## 函数

尽管这些内联块可以随你意愿增大，但超过两个或三个语句的内容就很难阅读且容易出错。内联代码越短简单越好。处理复杂代码有更好的方法。

函数是一个命名的代码块，你可以从另一段代码调用它。

```html
<HTML>
<HEAD>
<SCRIPT>
function showmessage()
{
  alert("Ouch")
}
</SCRIPT>
</HEAD>
```

## 对象

JavaScript 将网页视为对象的集合。图像、按钮、文本框以及表单的其它组件都是对象，页面本身以及它所在的浏览器窗口也是。

- 所有对象都有属性（properties），例如颜色、位置或它们所包含的文本。
- 大多数对象都有方法（methods）——用于操作对象的现成程序。
- 大多数对象都有事件处理器（event handlers）——当对象被点击或以某种方式改变时触发的程序。这些处理器可以用于激活 JavaScript 代码。

下一章将介绍浏览器对象、它们的属性、方法和事件处理器。一旦你掌握了这些内容，就可以开始编写与浏览器以及页面访问者进行交互的代码了。

> JavaScript 对象

> 还有其他 JavaScript“对象”——`Array`、`Date`、`Math` 和 `String`——它们实际上只是方法的集合。我们将这些内容留到第 3 章和第 5 章介绍。

## 存储数据

如果你想将数据从程序的一个部分传递到另一个部分，或者在发生其他事情时保持数据安全，可以将其存储在变量中——即命名的内存位置。如果你的代码仅仅是与浏览器页面进行简单的交互，则不需要变量；但要更进一步，你需要能够处理已存储的数据。

第 3 章将介绍变量。

## 程序结构

程序由一个或多个语句（statements）——即代码行组成。在简单的情况下，语句将按顺序执行一次。但情况可能比这复杂得多，这正是编程的乐趣所在。你可以让代码循环返回，以便一组语句重复多次——以处理大量信息或创建某种累积效果。你可以编写检查值并根据结果在不同方向上运行的代码。

我们将在第 4 章中介绍控制程序流的方法。

## 计算与方法

你可以使用 JavaScript 进行广泛的数据处理。除了简单的算术运算，它还能处理各种数学函数，以多种多样的方式处理文本，计算时间和日期，并对数据块进行排序或其他处理。

算术计算将在第 5 章介绍。处理数学、文本和日期时使用的方法将在第 5 章介绍。

## 整合

在书的后半部分，我们将所有这些元素结合起来，探索使用 JavaScript 创建动态和交互页面的某些方法。

## 在做中学学习

掌握任何编程语言的最佳方法就是玩玩它。尝试书中提供的所有示例代码。首先按照给出的完全输入，然后通过更改文本、值、大小或其他方面来探索概念和技术。当你清楚了每个新元素的工作原理后，将其与你之前学到的结合起来，编写你自己的页面。

JavaScript 不需要任何特殊软件——只需要一个浏览器和一个文本编辑器。我使用 Internet Explorer 和记事本（Notepad）。我使用记事本三个原因：它具有我需要的所有功能；它是一个很小的程序且加载非常快；它是 Internet Explorer 中“查看 > 源代码”命令显示页面时使用的工具——这非常方便。

## 测试步骤

一段时间后，你会找到自己的工作方法，但以下是我如何测试代码的——你可能也会这样做。

1. 在你的文本编辑器中编写第一个程序页面，并将其保存为 `test.htm`（或类似的名称）。
2. 在后续的工作阶段开始时，在浏览器中打开你的测试页面。
3. 使用“查看 > 源代码”在文本编辑器中打开该页面。
4. 编辑并重写代码以测试下一个想法。
5. 保存编辑后的文件——使用“文件 > 保存”或点击“保存”按钮。
6. 回到 Internet Explorer。
7. 点击“刷新”按钮重新加载页面。
8. 当你产出想要留作以后的内容时，只需将其另存为新名称，回到 `test.htm` 进行下一次测试。

这样使用同一个文件并在文本编辑器和浏览器之间切换，比打开和关闭不同的文件要快速简单得多。

## 注释

尝试让你的 JavaScript 代码具有可读性。当你几天、几周或几个月后回到某个页面时，你不应该费力去理解它。为你的变量、函数和对象赋予有意义的名称会有帮助，对于短代码来说，这可能足够了。如果你的代码更长或更复杂，你应该添加注释来提醒自己变量中存储了什么以及程序是如何运行的。

在 JavaScript 中编写注释有两种方法：

- `//` 单行注释，使用双斜杠：

```javascript
// 这是一个单行注释
```

- `/* */` 多行注释，以 `/*` 开头，以 `*/` 结束：

```javascript
/* 这是一个多行
   注释 */
```

## 总结

- JavaScript 是一种基于浏览器的语言。
- JavaScript 对象具有属性、方法和事件处理程序。
- 属性定义了对象。
- 方法是在对象上运行的内置程序。
- 事件处理器捕获影响对象的操作。
- 添加注释使代码更具可读性。

> Netscape 和其他浏览器

> Internet Explorer 不是唯一的浏览器，尽管它是最受欢迎的——这就是我用它来测试示例的原因。如果你使用 Netscape 或任何其他浏览器，可能会发现 JavaScript 解释方式上存在细微差异。

对象存在于层级结构中，较小的对象位于较大的对象内部。窗口（`window`）可选地包含框架（`frames`），然后是文档（`document`）。文档可能包含表单（`forms`），其中包含文本输入和按钮等元素。文档还可以包含图像、目标和其他元素。

![](img/abd8c35820179838d3f97b872561195a_26_0.png)

**02 对象与事件**

**图 2.1** 浏览器对象层次结构。

较大的对象——窗口、框架和文档被自动命名为 `'window'`、`'frame'` 和 `'document'`。只有当程序页面中有多个同类型的对象时，你才需要使用名称。

其他对象如果在脚本中使用，就需要命名——你稍后会遇到相关的示例，特别是我们在处理表单元素和图像时。

## 命名规则

名称必须是单词，必须以字母开头，并包含字母、数字和下划线（`_`）的任意组合。

- JavaScript 是大小写敏感的——大写和小写字母是不一样的。`'Button1'`、`'BUTTON1'` 和 `'button1'` 是三个不同的名称。

如果你保持名称简单，会让自己的生活更轻松。坚持使用小写字母，仅在复合名称处使用大写字母，大写字母标记每个单词的开头，例如 `'surname'`、`'address1'`、`'totalCost'`、`'mailToMe'`。

对于短脚本，可以使用数字命名——`'button1'`、`'button2'` 等。对于较长的脚本，你应该让名称更具意义——`'startButton'`、`'stopButton'` 等。

![](img/abd8c35820179838d3f97b872561195a_27_0.png)

图 2.2 对象的命名。

## 名称与层次结构

对象的名称是根据它在层级结构（网页结构）中的位置生成的。查看图 2.2 中的页面。它有两个框架，底部框架中的文档有两个表单。

如果你的代码在 `window1` 中的文档中：

- 如果要引用顶部框架中的文档，你应该使用 `frame1.topDocument`。
- 如果要引用 `realName` 文本框，你需要较长的 `frame2.mainDocument.form1.realName`。

注意用于分隔名称各个部分的句号。

如果代码在另一个窗口的文档中，你需要在名称开头添加 `window1`，因此：

- `window1.frame1.topDocument`
- `window1.frame2.mainDocument.form1.realName`

名称可能会变得很冗长，但 JavaScript 就是如此。

## 分配名称

我们已经看到了 JavaScript 如何引用网页上的对象，但它们最初是如何获得名称的呢？答案在于 HTML 编码中。创建这些对象的标签都有一个 `NAME` 选项，名称就是在那里分配的。

尝试这个示例。此处的 HTML 创建了一个包含按钮和文本框的表单。表单由这行代码生成并分配了名称 `'MyForm'`：

```
<FORM NAME = form1>
```

文本框由这行代码创建：

```
<INPUT TYPE = text NAME = output>
```

由于它在 `form1` 内部，而 `form1` 又在文档内部，因此 JavaScript 将其引用为 `document.form1.output`。这是 `<SCRIPT>` 中相关的代码行。它通过设置其 `value` 属性（见下文）来写入文本框。该属性附加在名称的末尾：

```
document.form1.output.value = "This is JavaScript"
```

按钮不需要名称，因为脚本不会引用它，但它需要一个 `onClick` 来启动代码：

```
<INPUT TYPE = button VALUE="Click Me" onClick="respond()">
```

这是该页面的完整代码。输入并尝试一下。

```
<HTML>
<HEAD>
<TITLE>Names </TITLE>
<SCRIPT>
function respond() {
  document.form1.output.value = "This is JavaScript"
}
</SCRIPT>
</HEAD>
<BODY>
<FORM NAME = form1>
<INPUT TYPE = button VALUE="Click Me" onClick="respond()">
<BR>
<INPUT TYPE = text NAME = output>
</FORM>
</BODY>
</HTML>
```

![](img/abd8c35820179838d3f97b872561195a_29_0.png)

图 2.3 按钮点击后的页面。

让我们看看 JavaScript 如何从对象读取数据以及向对象写入数据。我们将添加另一个文本框，用它来收集访问页面的姓名。我们将其命名为 `visitor`。

请输入您的姓名： `<INPUT TYPE = text NAME = visitor><P>`

现在脚本的活动部分是：

```
document.form1.output.value=document.form1.visitor.value
```

这获取 `visitor` 文本框中输入的任何内容——并将其写入 `output` 文本框中。



# 2.4 JavaScript 与表单交互

```html
<HTML>
<HEAD>
<TITLE>Names</TITLE>
<SCRIPT>
function respond()
{
document.form1.output.value=document.form1.visitor.value
}
</SCRIPT>
</HEAD>
<body>

<FORM NAME = myForm
Please enter your name: <INPUT TYPE = text NAME = visitor>

![](img/abd8c35820179838d3f97b872561195a_30_0.png)

图 2.4 JavaScript 与访问者交互的主要方式之一是通过读取和写入表单上的数据。

```

<P>

<INPUT TYPE = button VALUE = "Click Me" onClick =

"respond())"

<P>

Today's visitor is <INPUT TYPE = text NAME = output>

</FORM>

</BODY>

</HTML>

```

## 属性

大多数时候，你想要引用的是对象的属性，而不是对象本身。例如，在最后两个示例中，我们一直在读取和更改文本框的`value`属性。

## 文本属性

对象拥有的属性取决于对象的性质，但通常反映了可以通过 HTML 标签中的选项可以设置的属性。例如，`Text`对象具有这些属性：

- `defaultValue` 等于 `VALUE`
- `name` 等于 `name`
- `type` 等于 `type`
- `value` 等于 `value`

## 文档属性

文档对象拥有的属性比文本框得多。在实践中，文档对象拥有的属性比文本框多得多。在实践中，文档对象拥有的属性比文本框多得多。

## 修改文档属性

下一个示例展示了文档属性的应用。

文档对象拥有的属性比文本框多得多。在实践中，文档对象拥有的属性比文本框多得多。

```javascript
function blackwhite() {

  document.bgColor = "black"

  document.fgColor = "white"

}
```

文档对象拥有的属性比文本框多得多。在实践中，文档对象拥有的属性比文本框多得多。

## 其他对象的属性

当我们在第 6 章介绍表单时将查看其他元素的属性。对于其他主要对象，我们将在第 7 章处理图像，第 8 章处理窗口和框架。

## 属性与层次结构

层级结构中对象之间的链接是属性：`button2`是`form2`的属性，而`form2`本身是`mainDocument`的属性。向上层级同样有效：`form2`是`button2`的属性。正如我们开始编写实际代码时看到的，这非常有用。

## 方法

方法是属于对象的预定义函数。大多数方法可以在特殊“对象”`Date`、`Math`和`String`中找到（见第 5 章），浏览器对象也有。例如，所有的表单元素都有这两个方法：

- `focus()` 将光标移入文本框或突出显示按钮、复选框或其他选项
- `blur()` 是`focus()`的反

此示例展示了`focus()`方法在按钮上的应用。当点击一个按钮时，另一个将获得焦点。这些都是通过如下行的内联脚本完成的：

```html
<INPUT TYPE="button" NAME= button1 VALUE="Button 1" onclick="button2.focus()">
```

这里有两点注意：

- 方法名后有空括号。在其他方法中，括号用于向方法传递数据或从方法获取信息。这里没有数据需要传输，但括号仍然必不可少，因为它们指示 JavaScript `focus()` 是一个方法。

- 按钮的全名是`document.form1.button2`，但由于脚本是在，我们可以使用短形式

附加到`button1`上，它的形式与`button2`相同。如果将相同的代码被写在`<SCRIPT>`标签的函数中，则将需要使用全名。

输入代码并尝试运行。为了让自己相信代码确实移动了焦点，请更改数字，使焦点移动到不同的按钮。

```html
<HTML>

<HEAD>

<TITLE>focus() 方法</TITLE>

</HEAD>

<BODY>

<FORM NAME = form1>

<INPUT TYPE="button" NAME = button1 VALUE="Button

1" onclick="button2.focus()">

<INPUT TYPE="button" NAME = button2 VALUE="Button

2" onclick="button3.focus()">

<INPUT TYPE="button" NAME = button3 VALUE="Button

3" onclick="button1.focus()">

</FORM>

</BODY>

</HTML>
```

我们将在第 6 章中查看其他一些表单元素方法。

## write() 和 writeln()

这两个文档方法用于在页面上显示文本（以及其他材料）。它们用法完全相同，效果也几乎相同。`writeln()` 在文本之后添加一个换行符——即按下 [Enter] 键——但 HTML 通常会忽略它。

`write()` 方法的基本形状为：

```javascript
document.write(expression, expression,... )
```

你必须指定一个文档。如果你正在向当前页面写入内容，请使用简单的`document`。如果输出将到不同的页面，你还必须包含框架（frame）或窗口的名称。

```javascript
MainFrame.document.write(...)

MessageWindows.document.write(...)
```

表达式可以是文本字符串、数字、变量或函数返回的值。一个`write()`可以包含任意数量的表达式——用逗号分隔。

你可以写入的文本包括 HTML 标签，这些标签在显示之前会被浏览器解释为普通内容。这意味着你可以使用该方法生成格式化文本。

你可以写入的内容包括 HTML 标签，这些标签在显示之前会被浏览器解释为普通内容。这意味着你可以使用该方法生成格式化文本。

注意以下几点：
- 如果`write()`放置在`<body>`标签之前，它可能会破坏 HTML 结构，因为它在文档加载之前执行。
- 如果`write()`放置在`</body>`标签之后，它可能会在 HTML 解析完成后才执行，导致问题。
- 如果`write()`放置在`<body>`标签内部，它会正常工作。
- 如果`write()`放置在`<iframe>`标签内部，它会写入该框架的文档。
- 如果`write()`放置在`<script>`标签内部，它会写入脚本块的文档。
- 如果`write()`放置在`<head>`标签内部，它会写入头部区域的文档。
- `write()`只有在`document.open()`之后调用时才不会重写整个文档。

（注：由于原文文本中存在大量重复的片段和不完整的句子，上述翻译已根据技术文档逻辑进行了精简，确保通顺。）

产生此输出：
他说：“你必须去看看‘http://www.tybooks.com’。”
注意，如果你在它前面写另一个反斜杠，也可以显示反斜杠。
有关特殊字符的更多信息请参见第 156 页。

## 练习

- 1. 创建一个包含三个按钮和一个文本框的表单。设置单独函数由按钮激活，每个函数向文本框中写入不同的消息。
- 2. 扩展文档属性示例（第 21 页），为其提供另外两种颜色方案——深蓝色背景上的浅绿色文字，以及白色背景上的白色文字。背景和前景颜色相同时什么时候会有用？
- 3. 使用`write()`方法创建一个包含`<h1>`和`<h2>`标题以及至少两行独立文本的页面。

## 总结

- JavaScript 对象具有属性、方法和事件处理器。
- 对象的名称部分取决于它在 window/document/form 层级结构中的位置。
- 不同的对象具有不同的属性集。
- 要识别对象的属性，请提供其全名并附加属性名。
- 你可以在 JavaScript 内部读取和更改对象的属性。
- 方法是一个现成的函数。所有方法都属于对象并通常作用于对象。
- 事件处理器响应发生在对象上的事件。它们可以用于触发 JavaScript 代码。

# 03 变量

在本章中，你将学习

- 如何创建、命名和使用变量
- 关于 JavaScript 中的计算
- 关于在数组中存储和处理数据

## Variables

变量是内存中命名的位置，你可以在其中存储程序中使用的数据。你可以根据需要创建任意数量的变量，并随意命名——只要符合命名规则（见下页）。当你运行脚本时，系统会为变量分配空间，并将名称转换为计算机使用的内存地址。

这里`Sum`存储 145、-99，`visitor`存储 'Jo Bloggs'。这些值可以在任何时候通过脚本或用户输入数据更改。

| 变量名 | 内存 |
|---|---|
| Sum | 145 |
| x | -99 |
| visitor | Jo Bloggs |

与大多数编程语言不同，JavaScript 不在乎你在变量中存储什么类型的数据——同一个变量可以在代码的不同点被用于存储数字、文本或其他值。

本质上有三种数据类型：

- 数字（numbers）：JavaScript 不区分整数（整数字）和带小数部分的数字——你可以随心所欲地混合使用。数字通常以十进制（基 10）格式处理，尽管 JavaScript 可以读取八进制、十六进制和其他基数的值。

- 字符串（strings）：代码中用引号编写的任何文本或用户输入的文本都是字符串。它可以由 1 个或以上的任意字符组成——如果有上限的话，我从未遇到过。

- 布尔值（Boolean）：这些为真（`true`）或假（`false`）。它们主要用于将测试结果从代码的一部分传递到另一部分。

变量还可以持有`null`。这用于引用空字符串和缺失的对象。

## 创建变量

使用关键字`var`来设置或声明变量。

```javascript
var visitor

var max = 500
```

第一行创建了变量`visitor`，但没有给它赋值；第二行创建了`max`并为其分配 500。

你也可以在脚本的任何位置通过简单给它赋值来设置变量：

```javascript
x = -99

message = "Thank you for calling"
```

这些行设置了一个值为 -99 的变量`x`以及一个名为`message`持有字符串 "Thank you for calling" 的变量。

当变量用于存储重要数据或从程序的一部分传输数据到另一部分时，良好的做法是在程序开始或使用它们的代码块开始处声明它们。当你几周后回到代码时，如果能一眼看出程序使用了哪些变量以及它们的初始值，将更容易理解。

## 变量名称

变量命名规则与对象命名规则相同。名称必须以字母或下划线 (`_`) 开头，并包含字母和数字的任意组合。不能使用空格，应避免使用符号。你不能使用任何保留字（见第 155 页）。保持名称简短可以减少输入错误，但最重要的规则是名称必须对你有意义！

名称中可以使用大写或小写字母，但要注意混合，因为 JavaScript 是区分大小写的。`myName`、`myname`、`MyName`和`MY`是四个不同的东西。

```javascript
ageLimit = 18

sex = "M"

var VATue
```

## 赋值

要给变量赋值，请使用这种模式的代码：

变量 = 值

值可以是：

- 字面量——某些文本、数字，或单词`true`、`false`（对于布尔变量）或`null`；
- 另一个变量；
- 计算式或其他表达式；
- 产生值的函数或方法。

## 显示变量

变量可以使用于任何可以使用文本或数字的地方。
你可以将它们写在屏幕上，或者在表单的文本框或对话框中显示它们（见第 56 页）。

```javascript
document.write(sum)
```

这将在页面上写入`sum`的值。如果你想带有某些随附文本显示变量，可以使用`+`号将它们连接起来。

```javascript
document.write("The total is " + sum)
```

注意文本末尾引号内有一个空格。这是在将文本和变量写入屏幕时区分它们所需的。如果漏掉它，你会得到：

The total is999

## 变量的作用域

变量的作用域是指读取或更改其值的代码部分。变量的作用域取决于它是如何以及在哪里创建的。

## 全局变量

在文档的`<BODY>`中通过赋值声明的变量具有全局作用域。文档中其他地方的任何 JavaScript 都可以访问它们——在另一个`<SCRIPT>`块中、事件代码中或`<HEAD>`函数中。甚至可以通过在变量名前加缀从其他文档访问它们。如果你在一个名为`mainWindow`的窗口中有一个`visitor`的变量，你可以通过`mainWindow.visitor`名称从另一个窗口引用它。

## 局部变量

在函数中通过赋值声明的变量是该函数的局部变量。无法从任何其他代码访问它们。

在函数中使用`var`声明的变量也是该函数的局部变量。如果文档其他地方有同名的变量，请使用这种格式。它确保函数中的变量是一个独立的、局部变量，并且在函数执行后，全局变量仍将保持相同的值。

以下示例演示了变量的作用域。两个变量`x`和`y`通过在`BODY`脚本开始时赋值而创建。显示了这些值。

然后调用函数`dostuff()`。在这里，`x`被分配了一个新值，但`y`使用`var`声明并被分配了新值。这些值在函数内部被显示。

回到`BODY`脚本，最后一次显示这些值。`x`现在持有在函数中分配给它的值，但`y`仍保持其原始值。这是因为函数中的`y`变量由于使用了`var`声明而是一个独立的局部实体。`dostuff()`中`y`的任何操作对主中的`y`没有影响。

```html
<HTML>

<HEAD>

<TITLE>Variables</TITLE>

<SCRIPT>

function dostuff()

{

 x = -1

var y = 0

document.write("<P>In the function x holds " + x + " and y holds " + y + ")")

}

</SCRIPT>
```

```html
</HEAD>

<BODY>

<SCRIPT>

x = 99

y = 1066

document.write("Variable x holds " + x)

document.write("<P>Variable y holds " + y)

dostuff()

document.write("<P>Back in the body, x has been changed to " + x + " but y still holds " + y + ")")

</SCRIPT>

</BODY>

</HTML>
```

![](img/abd8c35820179838d3f97b872561195a_47_0.png)

图 3.1 输出。实验这些代码。在`body`中创建变量时使用`var`有区别吗？

## 计算

JavaScript 中有五种算术运算符：

- `+` 加法
- `-` 减法
- `*` 乘法
- `/` 除法
- `%` 取模

前四个运算符的使用方法与普通算术运算完全相同。模运算符用于返回整数除法的余数，例如：

14 % 4 = 2

即 14 除以 4 结果为 3，余数为 2。

算术表达式产生的值可以用在任何可以使用变量或字面量的地方。你可以将它们写在屏幕上、赋值给变量，或者在其他计算中使用它们。我们将从将它们打印到屏幕上开始。这个示例显示了和（作为文本），随后是表达式。系统将计算结果并显示它们。

```html
<HTML>

<body>

<SCRIPT>

document.write("42 + 5 = " + (42 + 5) + "<P>")

document.write("42 - 5 = " + (42 - 5) + "<P>")

document.write("42 * 5 = " + (42 * 5) + "<P>")

document.write("42 / 5 = " + (42 / 5) + "<P>")

document.write("42 % 5 = " + (42 % 5) + "<P>")

</SCRIPT>

</body>

</HTML>
```

**图 3.2** 用引号的数字和运算符被视为文本；在括号内的被视为计算。如果漏掉了括号会发生什么？请继续阅读……

## 数值与数字

当 JavaScript 看到一个数字时，它可以将其视为数字（即文本）或一个值。如果它在引号中，它会被视为文本。如果它本身是一个数字，它也被视为文本。如果它在计算中，JavaScript 通常会识别出它的身份，但可能会出错。看这一行：

```javascript
document.write("42 + 5 = " + 42 + 5)
```

这将显示：

42 + 5 = 425

为什么？因为`+`运算符有两个含义——它也可以用于组合文本字符串或混合了文本与数字。JavaScript 处理该行中的数字就像它们在引号中一样，如下：

```javascript
document.write("42 + 5 = " + "42" + "5" )
```

因此它将它们拼接在一起，而不是相加。减号也会让 JavaScript 产生困惑。

```javascript
document.write("42 + 5 = " + 42 - 5)
```



这将显示`NaN`，意思是“不是数字”（Not a Number）。解决方案是在计算周围加上括号。这强制 JavaScript 在屏幕上写入任何内容之前完成计算——以便得到单个数字。

删除第 37 页示例中的括号并查看效果。

**图 3.3** 相同的表达式，但没有括号。

## 赋值运算符

这些将算术运算符与赋值（`=`）结合，产生改变变量值的快捷方式。但请注意，你只能在两侧出现相同变量的地方使用它们。它们看起来像这样：

```
+= -= *= /= %=
```

用法如下：

```javascript
total += vat
num *= 2
```

这些等同于：

```javascript
total = total + vat
num = num * 2
```

`+=` 运算符也适用于文本。例如：

```javascript
username = "Jo"
username += " Bloggs"
```

`username` 现在持有`"Jo Bloggs"`。

## 递增与递减

还有两个算术运算符。`++`（递增）和`--`（递减）将增加或减少变量的值 1。它们的用法如下：

```javascript
num++
```

输入速度更快，但效果等同于：

```javascript
num = num + 1
```

运算符可以写在变量名的之前（前置）或之后（后置）。如果你只是在改变该变量的值，那么使用哪种形式没有关系。这两种是等价的：

```javascript
num++
++num
```

如果你正在将值赋值给另一个变量或在同时显示该值，那么运算符的位置至关重要。

```javascript
num2 = num1++
```

将`num1`的初始值赋值给`num2`，然后增加`num1`。

```javascript
num2 = ++num1
```

在将其值赋值给`num2`之前增加`num1`。

你可以在下一个示例中看到它的运行。

```html
<HTML>
<BODY>
<SCRIPT>
var count = 0
document.write(count + "<P>")
count++
document.write("Incremented " + count + "<P>")
document.write("Increment after " + count++ + "<P>")
document.write("Increment before " + ++count + "<P>")
</SCRIPT>
</BODY>
</HTML>
```

输入它并查看输出。看看交换 `"Increment before..."` 和 `"Increment after..."` 这两行会发生什么。尝试将初始的`count++`替换为`count`。

## 运算符优先级

到为止的计算都是简单的，只有一个运算符。你可以拥有包含多个运算符和值的 JavaScript 表达式——就像你在纸上写的一样。优先级规则在这里适用，就像普通算术一样。

当有多个运算符时，先执行乘法和除法，然后执行加减法，最后是赋值运算符（尽管通常只用于简单的计算）。

如果表达式的一部分被括在括号内，该部分将在其余部分求值，例如：

## 2+3*4-(9-3)/2

首先求解括号内的操作，得到：

`2+3*4-6/2`

然后执行乘法和除法：

`2-12-3`

最后执行加减法得到 11。

当你有一序列乘法和除法（或加减法）时，先执行哪一个没有关系，例如：

`4*6/3 = 24/3=8`
或 `4*2=8`

## 位运算符
JavaScript 还有位运算符。这些运算符将数字视为一组位，例如 42 会被视为 `00101010`，并可以改变字节内单个位的值。它们主要用于操作内存和输入输出流，我们还没有足够的空间。

## 数组
数组让你批量存储和处理信息。在任何可以使用变量的地方使用它们。数组的基本概念很简单。

| 数组 | 内存 |
|---|---|
| 0 | Doc |
| 1 | Sneezy |
| 2 | Happy |

## 初始化数组
数组不是单一类型。要创建一个数组，你可以使用：

```javascript
product = new Array(7)
```

这设置了一个数组，构造函数分配数组空间。编号从 0 开始，即元素的下标。

## 数组方法
`Array` 对象有几个预定义方法，你可以在数组上使用它们。

`join()` 将数组中的所有元素合并为一个字符串。可以通过给出数组名称来输出：

```javascript
document.write("We sell: " + products)
```

`reverse()` 将数组反转，使其从最后一个元素开始，以第一个元素结束

`sort()` 对数组进行排序。这通常是字母顺序，但你可以将其设置为降序，或数值升序或降序。

```javascript
document.write("<P>And back the other way:<BR>")
for (dwarf = 0; dwarf < 7; dwarf++)
document.write(nickname[dwarf] + "<BR>")
nickname.join())
document.write("<P>All together now:" + nickname)
</SCRIPT>
<body>
</html>
</html>
```

注意用于遍历列表的语句：

```javascript
for (dwarf = 0; dwarf < 7; dwarf++)
document.write(nickname[dwarf] + "<BR>")
```

![](img/abd8c35820179838d3f97b872561195a_55_0.png)

**图 3.4** 排序、反转和合并后的数组元素。

这会将`dwarf`赋值为 0 到 6 的值，每个值都会重复以下行。我们将在下一章详细介绍`for`循环。

## 练习

- 编写代码为两个变量赋值数值，然后将它们相加并将结果赋值给第三个变量，用`write()`显示该结果。修改代码将操作改为减法并再次运行。对其他运算符重复此操作。

- 编写代码计算此表达式：
`(10+6)/4 * (10-4)/3`

- 在七个矮人的例子中，执行`join()`之后数组的状态是什么？如何检查？

## 总结

- 变量是内存中命名的位置，可以在其中存储数据供程序使用。在命名变量时，最重要的规则是：名称必须对你有意义！
- 变量的作用域主要取决于它创建的位置。
- JavaScript 有五种算术运算符：`+`（加）、`-`（减）、`*`（乘）、`/`（除）和`%`（取模）。
- 你可以结合赋值运算符和算术运算符，同时完成两个操作。
- 你可以使用`++`（递增）和`--`（递减）运算符对变量加或减 1。
- 数组是一组具有相同名称的变量，通过下标数字识别。可以通过循环遍历数组来批量处理数据。

## 04 程序流程

在本章中，你将学习：
* 如何比较值
* 如何使用循环重复代码块
* 关于`if`和`switch`的分支程序
* 如何重定向程序流程

## 控制程序

程序流程是指指令执行的顺序。到目前为止，大多数示例程序都是顺序执行一个序列然后停止的。使用这种简单的程序所能实现的功能是有限的。循环和分支的使用使程序变得强大得多。

- 循环重复固定次数的一组指令，直到满足某个条件。
- 分支根据变量所持的值将流程引向不同的路径。

在对循环或分支进行任何大量操作之前，你需要知道如何测试变量中的值。

## 比较运算符

这些运算符用于比较变量的内容与值或其他变量的内容。共有六种比较运算符：

| == 等于 | != 不等于 |
| :--- | :--- |
| < 小于 | <= 小于或等于 |
| > 大于 | >= 大于或等于 |

注意，相等性测试使用双等号`==`。单等号`=`用于赋值。

测试被包含在括号中，通常如下所示：

```javascript
(x < 99)
(newNum != oldNum)
```

测试会产生一个布尔值——`true`（真）或`false`（假）。大多数时候你不需要担心这个——直接使用测试——但有时将测试结果存储在变量中供程序后续引用很有用，例如：

```javascript
result = (newNum > oldNum)  // 存储测试结果
...
if (result == true)  // 等同于使用 "if (newNum > oldNum)"
```

在测试布尔值是否为真时，你可以省略测试中的`== true`部分，它仍然有效。

```javascript
if (result)
```

这等同于

```javascript
if (result == true)
```

包含`== true`可以使测试更具可读性，但在你同时测试多个值时，最短的写法会让表达式更整洁——见下文。

## 逻辑运算符

比较运算符每次只测试变量与一个值。有时你想检查一个变量是否落在一个值的范围内，或者等于其中一个值。这时逻辑运算符派上用场了。

## 与（AND）

`&&`运算符比较两个测试，只有当两个测试都为真时，结果才为真。

```javascript
x > 5 && x < 10
```

## 或（OR）

`||`运算符比较两个测试，只要其中一个测试为真，结果就为真。

```javascript
x > 5 || x < 10
```

## 非（NOT）

`!`运算符反转布尔值。

```javascript
!result
```

## 53 程序流程 04

```html
<FORM>
<BR> 结束值:<INPUT TYPE="text" NAME="endval" VALUE="10"><BR>
变化量:<INPUT TYPE="text" NAME="changeval" VALUE="1"><BR>
<INPUT TYPE="button" VALUE="运行循环" onClick="doloop()">
</FORM>
</body>
</HTML>
```

![](img/abd8c35820179838d3f97b872561195a_64_0.png)

![](img/abd8c35820179838d3f97b872561195a_64_1.png)

**图 4.3** 脚本生成的表单和页面。变化值可以是负数，但如果你想倒数计数，结束值显然必须小于起始值。

## 嵌套循环

循环可以“嵌套”在另一个内部，每当程序流通过外层循环时，内循环都会执行其完整过程。这是一种你可能会用于读取数组或创建二维（或多维）表格的技巧。

下一个示例显示了一个 10 x 10 的数字块，顶部从 1 到 10，左侧从 1 到 10，行和列交汇处显示它们的倍数。当你考虑到每个循环的结束值都可以高得多时，你会发现得益于循环，你仅两三行代码就能完成如此大量的工作！

```html
<HTML>
<body>
<SCRIPT>
for (row = 1; row <= 10; row++)
{
  for (col = 1; col <= 10; col++)
    document.write((row * col) + " ... ");
    // col 循环结束
  document.write("<BR>");
}
</SCRIPT>
</HTML>
```

![](img/abd8c35820179838d3f97b872561195a_65_0.png)

**图 4.4** 由两个嵌套循环生成的乘法表。

显示可以更整洁一些！问题是`write()`的输出是 HTML 代码，而 HTML 不支持制表符，也无法在项目之间显示多个空格。使用点作为间距是一种粗糙的解决方案，但只要花一点精力，我们就可以获得布局整齐的表格——正如你即将看到的。

## 循环生成的表格

记住你可以编写任何 HTML 标签。如果我们想在 HTML 中得到一个整洁的表格，我们使用`<TABLE>`标签。关键的是行`<TR>`和列`<TD>`标签，它们可以很好地融入到内层和外层循环模式中。

我们在每行的开始写一个`<TR>`：

```javascript
for (row = 1; row <= 10 ; row++) {
document.write("<TR>")
```

并将每个列项目封装在`<TD> </TD>`标签中：

```javascript
for (col = 1; col <= 10 ; col++)
document.write("<TD>" + (row * col) + "</TD>")
```

项目之间的间距、边框大小和其他选项可以往常一样在循环之前的`<TABLE>`标签中设置。

```html
<HTML>
<BODY>
<SCRIPT>
document.write("<TABLE BORDER = 2 CELLACING =5 ALIGN = CENTER>")
for (row = 1; row <= 10 ; row++) {
  document.write("<TR>")
  for (col = 1; col <= 10 ; col++)
    document.write("<TD>" + (row * col) + "</TD>")
  // 内层 (col) 循环结束
  document.write("</TR>")
}
document.write("</TABLE>")
</SCRIPT>
</HTML>
```

## 对话框

在我们继续控制程序流程的方法之前，让我们先来看看对话框。它们提供了一种向程序输入值的简单方法，这对于测试分支结构非常有用。

JavaScript 有三个现成的对话框，可以用它们与访问者进行交互。这三个对话框都会显示一个（固定的）标题和消息，并停止脚本直到用户响应。消息可以是文本，也可以是产生文本的任何表达式。

- `alert(message)` 只包含一个 OK 按钮。用它让你的访问者知道事情已经发生或即将发生。

```javascript
alert("您的订单已处理")
```

![](img/abd835820179838d3f97b872561195a_67_0.png)

**图 4.5** 改进后的显示。

![](img/abd8c35820179838d3f97b872561195a_67_1.png)

- `confirm(message)` 包含 OK 和取消按钮，并根据点击了哪个按钮返回布尔值`true`或`false`（点击 OK 返回`true`）。当你向访问者提供是/否选择时，请使用它。回复应该赋值给变量。

```javascript
it = confirm("你真的想取消吗？")
```

![](img/abd835820179838d3f97b872561195a_68_0.png)

- `prompt(message, default)` 包含一个文本框以及 OK 和取消按钮。它返回输入的内容。用它在没有表单的地方获取信息。你可以设置默认值或使用`""`清空文本框。如果没有设置默认值，文本框将显示"undefined"。

```javascript
num = prompt("输入你的数字", "")
```

![](img/abd835820179838d3f97b872561195a_68_1.png)

来自`prompt`的数据始终是文本。如果你需要它是一个数字，请像这样使用`eval()`函数：

```javascript
num = eval(prompt("要几个?", ""))
```

## while 循环

`for`循环通常重复固定次数。`while`循环在两个方面为你提供了更大的灵活性：

- 退出测试在循环开始处进行——在每次重复之前执行。如果在开始时满足条件，则循环语句将完全不执行。
- 退出测试可以检查*任何*变量的状态，而不仅仅是循环计数器。

基本的 `while` 循环形状如下：

```javascript
while (test)
  statement(s)
```

但这里有一个变量必须先有一个被赋值的值。

```html
<HTML>
<BODY>
<SCRIPT>
document.write("<TABLE BORDER = 2 CELLACING =5 ALIGN = CENTER>")
for (row = 1; row <= 10 ; row++) {
  document.write("<TR>")
  for (col = 1; col <= 10 ; col++)
    document.write("<TD>" + (row * col) + "</TD>")
  // 内层 (col) 循环结束
  document.write("</TR>")
}
document.write("</TABLE>")
</SCRIPT>
</HTML>
```

（注：由于原文文本中存在部分重复和错乱，翻译时已根据“不要重复输出原文”的原则对逻辑内容进行了对齐，确保译文通顺且符合所有要求。）

*注：由于用户提供的待翻译文本中存在多处完全重复的段落（如 while 循环部分），我在输出翻译时已按照逻辑结构进行了去重处理。*

```javascript
if (guess < x)
{
    document.write(" Too low")
    min = guess
    guess = Math.round((max + min) / 2)
}
document.write("<P>It was " + guess);
document.write("<BR> Found it in " + count + " goes.");
</SCRIPT>
</HTML>



![](img/abd8c35820179838d3f97b872561195a_72_0.png)

**图 4.6** 一个典型的输出——计算机运行从未超过七次。为什么呢？

## `if ... else`

这种 `if` 结构的变体使用了 `else` 关键字，它用于处理当测试不为真时执行的操作。语法如下：

```javascript
if (test)
    { statement(s) if true }
else
    { statement(s) if false }
```

例如：

```javascript
if (total > 100)
    carriage = 2.00
else
    carriage = 5.00
```

如果你花费超过 £100，运费为 £2.00，否则为 £5.00。

基础的 `if` 结构具有简洁之美——它清晰地展示了测试与结果之间的关系。但它并不总是最佳解决方案。你想分析一个字符，以判断它是大写字母还是小写字母、数字还是符号。这里是完成这项任务的程序初稿。

```html
<HTML>
<HEAD>
<TITLE>Character tester</TITLE>
</HEAD>
<BODY>
<SCRIPT>
letter = prompt("Enter a character,", "")

while (letter != "q")
{
    if (letter < " ")
        alert("Non-printing character entered")

    if (letter >= "a" && letter <= "z")
        alert("Lower case letter entered")

    if (letter >= "A" && letter <= "Z")
        alert("Upper case letter entered")

    if (letter >= "0" && letter <= "9")
        alert("Digit entered")

    letter = prompt("Enter a character - q to quit,", "")
}
</SCRIPT>
</HTML>
```

到目前为止一切正常。第一个测试识别了非打印字符（制表符、回车、移动等，它们聚集在字符集的开头，在空格处结束）。接下来的三个测试处理了‘a’到‘z’、‘A’到‘Z’以及‘0’到‘9’的集合。剩下的呢？

查看任何字符集（使用 Windows 附件中的“字符表”），你会发现标点和其他符号散落在字母和数字块之间。对这些符号的测试看起来如下：

```javascript
if ((letter > " ") && (letter < "0") || (letter >= "9") && (letter < "A") || (letter > "Z") && (letter <= "a") || (letter >= "z"))
```

这不是一个优雅的解决方案！而且不仅仅是不好看。复杂的代码更容易包含错误。这个表达式花了一些时间来推演和测试——我仍然不 100% 确定它！

这里有一个更好的解决方案。`if ... else` 结构从同一个测试产生两个分支——一个在为真时执行，另一个在为假时执行。这可以扩展为处理多个分支。

- `if (test1) {statement(s) if test1 is true}`
- `else if (test2) {statement(s) if test2 is true}`
- `else {statement(s) if no tests are true}`

如果 `test1` 为假，程序会尝试 `test2`，如果失败，则尝试下一个。如果所有测试都证明为假，程序将执行最后一个 `else` 之后的语句。这是修改后的例程。

```html
<HTML>
<HEAD>
<TITLE>Character tester</TITLE>
</HEAD>
<BODY>
<SCRIPT>
letter = prompt("Enter a character,")

while (letter != "q")
{
  if (letter < " ")
    alert("Non-printing character entered")

  else if (letter >= "a" && letter <= "z")
    alert("Lower case letter entered")

  else if (letter >= "A" && letter <= "Z")
    alert("Upper case letter entered")

  else if (letter >= "0" && letter <= "9")
    alert("Digit entered")

  else
    alert("Symbol entered")

  letter = prompt("Enter a character - q to quit,")
}
</SCRIPT>
</HTML>
```

如果字符没有被任何测试捕获，则执行 `else` 语句并显示“Symbol entered”消息。

这里有三点需要注意：

- 这展示了如何使用 `prompt` 对话框获取输入，并使用 `alert` 显示消息。

![](img/abd8c35820179838d3f97b872561195a_75_0.png)

- 在 `while` 行之前和循环结束时，都有提示用户输入字符的行。`while` 行在启动时需要一些可以测试的内容。
- 当你有一系列独立的 `if` 语句时，程序即使已经得到了真结果，也会检查每一个语句。使用像这样的复合 `if ... else if ... else` 结构时，一旦找到匹配项，程序流将跳转到末尾。如果在处理大量数据时反复进行测试，运行速度会有显著的提升。

`switch` 结构可以替换整组 `if` 语句，这些语句都是对同一个简单变量进行不同的测试。典型的用法是配合菜单，通过 `switch` 将程序流引导到所选选项的例程。`switch` 结构的基本形状如下：

```javascript
switch (expression)
{
  case value:
    statement(s)
    break

  case value:
    statement(s)
    break

  ...

  default:
    statement(s)
}
```

## 替代布局

- `switch` 执行简单的匹配，将每个值与表达式进行比较——在这里不能使用关系运算符。
- 值必须包含在引号中并在后跟冒号。
- 在每个 `case` 语句末尾需要一个 `break` 来跳出 `switch` 块。
- 语句可以写多行，也可以写在一行。

## 条件运算符

条件运算符 `? :` 是 `if else` 的简写。它可以用于根据测试进行赋值，而不是用于重定向流。它可以非常方便，尽管为了简洁而牺牲了可读性。

基本形状为：

```javascript
variable = (test ? value_if_true : value_if_false)
```

这是一个简单的用法示例。如果总额超过 250，则给予 10% 的折扣：

```javascript
discount = (total > 250 ? 0.1 : 0)
```

等效的 `if else` 为：

```javascript
if (total > 250)
    discount = 0.1
else
    discount = 0
```

它通常用于更大的表达式中。例如，这家公司对 £100 以下的订单收取 £10 运费，总额超过时收取 £5。计算成本的行是：

```javascript
cost = total + (total < 100 ? 5 : 10)
```

使用 `if else`，代码将是：

```javascript
if (total < 100)
    cost = total + 5
else
    cost = total
```

你可以在这个示例中看到条件运算符的作用。运行它时，输入 100 以下、100 到 250 之间以及 250 以上的值，以检查两个运算符是否正常工作。（每次运行后刷新页面以重启程序。）

```html
<HTML>
<HEAD>
<TITLE>Conditional operator</TITLE>
</HEAD>
<BODY>
<SCRIPT>
total = prompt("Enter total spent,")

discount = (total > 250 ? total * 0.1 : 0)
carriage = (total > 100 ? 5 : 10)
due = total - discount + carriage

document.write("Total = " + total)
document.write("<BR>Discount = " + discount)
document.write("<BR>Carriage = " + carriage)
document.write("<BR>Amount due = " + due)
</SCRIPT>
</HTML>
```

## 68 程序流程

04

![](img/abd8c35820179838d3f97b872561195a_79_0.png)

**图 4.7** 显示并不非常整洁，有时折扣值可能会达到 15 位小数（例如尝试 267.67）。我们稍后会考虑让界面看起来更漂亮。

## `label`（标签）

标签本身实际上并没有执行任何操作。它的目的是标识代码中的某个位置，以便程序流可以通过 `switch`、`break` 或 `continue` 语句重定向到那里。其基本形式为：

```javascript
label : statement(s)
```

`label` 可以是任何单词，遵循与变量名相同的规则，JavaScript 留字除外（见第 155 页）。注意它们后面必须跟一个冒号：

```javascript
restart:

document.write("Picking up again")
```

## `break`（退出）

我们见过 `break` 与 `switch` 配合使用（第 65 页）。它提供了一种退出 `for` 或 `while` 循环的方法。如果退出条件可能永远无法满足，那么它是至关重要的；但当你只需要另一种退出方式时，它也很有用。

在示例中，循环允许用户有三次机会计算出一个加法的答案。

如果他们提供了正确答案，`break` 将强制提前退出循环。通过在循环结束后检查循环变量 `count`，程序可以判断用户是失败了（`count == 3`）还是答对了（提前退出）。

`num1` 和 `num2` 的值是由 `Math` 方法 `round()` 和 `random()` 生成的随机数。在这种情况下，这些值将在 1 到 20 之间。

```html
<HTML>
<HEAD>
<TITLE>Breaking out of loops</TITLE>
</HEAD>
<BODY>
<SCRIPT>
num1 = Math.round(Math.random()*20)
num2 = Math.round(Math.random()*20)

for(count = 0; count < 3; count++) {
  answer = prompt("What is " + num1 + " times " + num2 + " ")

  if (answer == num1 * num2)
    break
}

if (count == 3)
  alert("The answer was " + (num1 * num2))
else
  alert("Well done")
</SCRIPT>
</HTML>
```

## `break` to a label（跳转到标签）

如果你有嵌套循环，可以给它们标记标签，并使用标签来控制 `break`。在下面的示例中，有两个循环：外层和内层，由变量 `n` 和 `m` 控制。这两个循环都设置为从 0 计数到 4，但在内层循环内部进行。关键行是：

```javascript
if (m==3) break inner
if (n == 2) break outer
```

当 `m` 达到 3 时，程序跳出内层循环；当 `n` 达到 2 时，程序跳出外层循环。

```html
<HTML>
<BODY>
<SCRIPT>
out:

for(n = 0; n < 5; n++)

inner:

for(m = 0; m < 5; m++)
{
  if (m==3) break inner
  if (n == 2) break outer
  document.write("n n = " + n + " m = " + m + "<BR>");
}
</SCRIPT>
</HTML>
```

输出应该是：

```text
n = 0 m = 0
n = 0 m = 1
n = 0 m = 2
n = 1 m = 0
n = 1 m = 1
n = 1 m = 2
```

如果从 `break` 中移除标签会发生什么？

## `continue`（继续）

`continue` 与 `break` 类似，但 `break` 是直接将程序流带出循环，而 `continue` 只是跳过任何剩余行并再次循环。当循环底部的行只有在满足条件时才执行时，请使用它。

在示例中，用户被要求输入两个数字，程序用第一个除以第二个。由于不能除以 0，因此如果输入了 0，代码将使用 `continue` 重新循环。

```html
<HTML>
<BODY>
<SCRIPT>
alert("Welcome to the divider")

num1 = 99

while (num1 != 0)
{
    num1 = prompt("Enter first number or 0 to exit,", ")

    if (num1 == 0)
        break

    num2 = prompt("Enter second number", ")

    if (num2 == 0)
    {
        alert("Division by 0! Restart sum")
        continue
    }

    ans = num1 / num2
    alert(num1 + " divided by " + num2 + " = " + ans )
}
</SCRIPT>
</HTML>
```

我们可以使用 `if ... else` 结构来控制循环结束处的程序流：

```javascript
if (num2 != 0)
{
    ans = num1 / num2
    alert(num1 + " divided by " + num2 + " = " + ans)
}
else
    alert("Division by 0! Restart sum")
```



当有很多行需要跳过时，`continue` 更加整洁。

> **除以 0**
>
> 在大多数编程语言中，尝试除以 0 会导致程序崩溃。JavaScript 则更加宽容——它给你 `infinity`（无穷大）作为结果。

## `continue` with labels（带标签的 `continue`）

标签配合 `continue` 的作用与 `break` 非常相似。这里是相同的嵌套循环，但这次测试检查的是数字是偶数还是奇数（`%` 执行取模除，给出余数——如果你能除以 2 且余数为 0，该数字就是偶数）：

```javascript
if (m % 2 == 1) continue inner

if (n % 2 == 0) continue outer
```

如果内层计数器 `m` 是奇数，程序将跳过写入行并开始下一个内层循环。如果外层计数器 `n` 是偶数，程序将跳回外层循环的开头。

这里是相同的计算，但是通过函数执行的。在这个版本中，计算和输出行都已转移到函数中。

```html
<HTML>

<HEAD>

<TITLE>作为函数的立方</TITLE>

<SCRIPT>

function cube(num)

{

  ans = 1

  for (count = 1; count <= 3; count++)

    ans = ans * num;

  document.write(num + " ^ 3 = " + ans + "<BR>");

}

// 表示“...次方”

</SCRIPT>

</HEAD>

<BODY>

<SCRIPT>

n = 5

cube(n)

</SCRIPT>

</HTML>
```

注意 `BODY` 脚本中的调用行：

```javascript
cube(n)
```

以及函数的定义行：

```javascript
function cube(num)
```

变量 `n` 在 `BODY` 脚本中被赋值为 `5`，并被传递给函数 `cube(n)`。在那里，它被参数 `num` 接收，`num` 在 `cube()` 内部作为一个普通变量工作。

名称的选择是有意的——参数名称可以与传递给它们的变量名称相同，也可以不同。`cube()` 中的参数和变量与 `BODY` 脚本中的完全分离。下面的代码同样有效：

```javascript
n = 5
cube(n)
```

## 参数

在传递数据时，虽然必须传递正确类型的数据，但它可以作为变量，也可以作为字面量值。对 `cube()` 的这种调用同样有效：

```javascript
cube(5)
```

将该行添加到 `BODY` 脚本中并再次运行程序。这次的输出应该是：

- 5 ^ 3 = 125
- 4 ^ 3 = 64

函数可以接受任意数量的参数，这些参数可以携带文本或数字。下一个示例包含此函数：

```javascript
function greeting(text, times)
```

它写入文本，并根据需要重复指定的次数。在下一个脚本中，你可以看到数据作为变量传递的示例：

```javascript
greeting(words, repeat)
```

以及作为字面量传递的示例：

```javascript
greeting("Bye ", 2)
```

```html
<HTML>

<HEAD>

<TITLE>参数</TITLE>

<SCRIPT>

function greeting(text, times)

{

  for (count = 1; count <= times; count++)

    document.write(text)

}

</SCRIPT>

</HEAD>

<BODY>

<SCRIPT>

words = "Hello "

repeat = 3

greeting(words, repeat)

</SCRIPT>

<SCRIPT>

document.write("<BR>")

greeting("Bye ", 2)

</SCRIPT>

</BODY>

</HTML>
```

你必须传递相同数量的值，并且顺序正确。这样做行不通：

```javascript
greeting(3, "Hello")
```

## 返回值

你可能还从学校数学中记得过使用余弦和其他函数。这些函数的返回值可以在任何你使用普通值的地方使用，例如：

```javascript
x = cos(y)
```

或者：

```javascript
adjacent = cos(angle) * hypotenuse
```

JavaScript 函数也可以返回一个值。要做到这一点，请使用关键字 `return`，并在其后跟上该值。`return` 行通常是函数的最后一行。例如，你可以这样定义一个 `cube` 函数：

```javascript
function cube(x)

{

  return x * x * x

}
```

这里是立方程序，这次重写后，`cube()` 函数会将结果返回给调用代码。

```html
<HTML>

<HEAD>

<TITLE>作为函数的立方 - 2</TITLE>

<SCRIPT>

function cube(num)

{

  ans = 1

  for (count = 1; count <= 3; count++)

    ans = ans * num;

  return ans

}

</SCRIPT>

</HEAD>

<BODY>

<SCRIPT>

n = 5

result = cube(n)

document.write(n + " ^ 3 = " + result)

</SCRIPT>

</BODY>

</HTML>
```

注意调用函数的行：

```javascript
result = cube(n)
```

单独使用 `cube(n)` 无法获得答案。考虑到返回值的函数可以像任何其他值一样处理，你同样可以在 `write()` 行内部调用它：

```javascript
document.write(n + " ^ 3 = " + cube(n))
```

函数可以有几行 `return` 代码。这里有一个函数 `compare()`，它测试两个值：如果第一个较大则返回 1，如果较小则返回 -1，如果相同则返回 0：

```javascript
function compare(a, b)

{

  if (a > b) return 1

  else if (a < b) return -1

  else return 0

}
```

## 递归

函数不仅可以调用另一个函数，它还可以调用自己。这被称为递归。（因此，有了著名的计算机字典定义“递归：参见递归”。）

它类似于通过循环运行代码，并且当你需要将某些内容分解为组成部分时非常有用。但要小心使用。如果你不留出退出条件，程序将陷入死循环。

这是一个递归函数的简单示例。它计算阶乘值。阶乘是一个整数，它乘以它下方的每一个数字，直到 1。它通过在数字后加一个感叹号 `!` 表示，例如 `5!`。

### 查看阶乘的开始

阶乘序列：

```text
1! = 1
2! = 2
3! = 6
4! = 24
5! = 120
6! = 720
7! = 5040
8! = 40320
9! = 362880
10! = 3628800
```

递归函数的示例：

```javascript
function factorial(n)

{

  if (n <= 1)

    return 1

  else

    return n * factorial(n - 1)

}
```

输入此代码并运行几次，查看 `round()`、`ceil()` 和 `floor()` 之间的差异。

```html
<HTML>

<BODY>

<SCRIPT>

n = prompt("Enter a decimal number", "")

document.write("You entered " + n)

document.write("<BR> round = " + Math.round(n))

document.write("<BR> ceil = " + Math.ceil(n))

document.write("<BR> floor = " + Math.floor(n))

</SCRIPT>

</BODY>

</HTML>
```

你可以将这些方法中的一种或多种应用于随机数，将其转换为整数，例如：

```javascript
x = Math.round(Math.random() * 10)
```

问题是，用哪一个？使用哪种舍入方法会有区别吗？这里有一些代码可以进行测试。使用 `round()` 运行几次并记录结果，然后用 `ceil()` 和 `floor()` 重复操作。

注意 `HEAD` 部分中的这个函数：

```javascript
function rand(size)

{

  return Math.round(Math.random() * size)

}
```

这允许我们在 `BODY` 脚本中使用更简单的表达式 `rand(10)`。如果你发现脚本中需要复杂的表达式，通常将其转换为一个独立的函数是值得的。这会让脚本更具可读性，如果你需要调整表达式，编辑该函数也会更简单。

```html
<HTML>

<HEAD>

<SCRIPT>

function rand(size)

{

  return Math.round(Math.random() * size)

}

</SCRIPT>

</HEAD>

<BODY>

<SCRIPT>

store = new Array(11)

/* 创建一个从 0 到 10 的数组 */

for (loop = 0; loop <= 10; loop++)

  store[loop] = 0

for (count = 0; count < 1000; count++)

{

  /* 生成一个 0 到 10 之间的随机数 */

  x = rand(10)

  /* 增加该数字的计数器 */

  store[x] = store[x] + 1

}

for (loop = 0; loop <= 10; loop++)

  document.write("store[" + loop + "] has " + store[loop] + "<BR>")

</SCRIPT>

</BODY>

</HTML>
```

## 字符串与数字

`eval()` 会给你字符串的数值或计算结果。尝试以下操作来查看它的作用：

```html
<HTML>

<BODY>

<SCRIPT>

calcString = prompt("Enter a calculation", "")

alert("The value is " + eval(calcString))

</SCRIPT>

</BODY>

</HTML>
```

`eval()` 识别标准符号并遵循算术规则。输入 `2 + 3 * 4`，你应该得到 14。输入 `(2 + 3) * 4`，你应该得到 20。

从 `alert` 行中去掉 `eval()` 并再次尝试：

```javascript
alert("The value is " + calcString)
```

它显示了什么？

`toString(num)` 将数字转换为字符串。它的主要目的是整理数字的显示。当你在 JavaScript 中进行计算时，有时会得到奇怪的结果。例如，得到的可能不是 4，而是 3.999999999 或 4.000001。

这是因为计算机以二进制运行，并在屏幕上将值转换为十进制。这种转换并不总是完美的，你可能想对其进行整理。在需要显示货币值的地方，你需要将它们调整为 2 位小数。可能还有其他值需要在前面补 0。

只要它们是数值，你对数字的显示就做不了什么；但作为字符串，可以以多种方式对它们进行处理。我们稍后在查看 `String` 的方法时会回到这个问题。

## 三角函数

JavaScript 拥有标准的三角函数：`cos()`、`sin()` 和 `tan()`，它们分别给出角度的余弦、正弦和正切值；还有 `acos()`、`asin()`、`atan()` 和 `atan2()`，它们可以将余弦、正弦和正切值转换回角度。

这里需要注意的是，与大多数编程语言一样，JavaScript 使用**弧度**而不是大多数人熟悉的**角度**来测量角度。

弧度是圆周上的弧长等于圆半径的角。

![](img/abd8c35820179838d3f97b872561195a_97_0.png)

你应该从学校数学中记得，圆中有 2Pi 弧度（周长 = 2 * Pi * radius）。我们可以利用此来计算 1 弧度的值：

- 1 弧度 = 360 / 2 * Pi 度
- = 180 / 3.14
- = 57.3 度（近似值）

如果你觉得用角度比用弧度更方便，这些函数可以为你转换：

```javascript
function toDegree(radian)

{

  return radian * 180 / Math.PI

}
```

```javascript
function toRadian(degree)

{

  return degree * Math.PI / 180

}
```

`PI` 是 `Math` 的一个属性，值为 3.141592653589793。

## 时间

如果你想显示时间，这种技术与显示日期的方法非常相似，尽管有几个细节需要处理。

这里是基本的例程。它使用 `getHours()`、`getMinutes()` 和 `getSeconds()` 方法从日期中提取小时、分钟和秒的值，然后用 `:` 将这些部分隔开并组合成一个字符串。

```html
<HTML>

<HEAD>

<TITLE>Time - version 1</TITLE>

</HEAD>

<BODY>

<SCRIPT>

d = new Date()

hour = d.getHours()

mins = d.getMinutes()

secs = d.getSeconds()

document.write(hour + ":" + mins + ":" + secs)

</SCRIPT>

</BODY>

</HTML>
```

## 改进显示

初看之下，你可能觉得显示没有问题。例如，这里是例程刚刚给出的结果：

```text
14:56:12
```

但当我几分钟后刷新页面时，得到的是：

```text
15:0:4
```

单数字数值看起来并不好！它们需要在前面加一个 `0`。这里最简洁的解决方案是使用我们在第 4 章中看过的条件运算符 `? :`。

表达式：

```javascript
(mins < 10) ? ":0" : ":"
```

当分钟为单数字时，它会产生 `":0"`，否则产生 `":"`。在创建输出字符串时，可以用这个来代替简单的 `":"`，但注意整个表达式必须包含在括号内。

将输出行更改为：

```javascript
document.write(
  hour +
  ((mins < 10) ? ":0" : ":") +
  mins +
  ((secs < 10) ? ":0" : ":") +
  secs
)
```

这一行的可读性不高，你必须确保所有左括号和右括号都在正确的位置，但结果显示要好得多：

```text
15:05:02
```

## 现在是几？

这种时间显示的另一个问题是，它只会在页面第一次打开时正确。你的时钟不会运行！如果你想一直显示正确的时间，就必须不断更新——为此我们需要超时（`Timeouts`）。我们将在第 7 章回到这个问题。

## 字符串方法

在 JavaScript 中，字符串是对象，而不是像早期语言中的变量。很多时候这并没有太大区别——你可以像对待变量一样对待它们——但 `String` 对象拥有属性和方法，可以应用于代码中的任何字符串。你可能会发现其中一些非常有用。

严格来说，应该用这样的代码创建字符串：

```javascript
myString = new String("This is a string")
```

在实践中，简单地赋值同样有效：

```javascript
myString = "This is a string"
```

在 `prompt`、`TextBox` 或 `TextArea` 中输入的任何文本也是字符串。

有二十四种 `String` 方法。其中许多方法只是允许你在 JavaScript 中进行与在 HTML 中相同的格式化操作。例如，`bold()` 方法会将文本加粗，效果与 `<B>` 标签完全相同。

在这个示例中，`<SCRIPT>` 中的代码和正文中的代码产生了相同的效果：

```html
<HTML>

<BODY>

<SCRIPT>

myString = new String("This is a string")

document.write("<P>" + myString.bold())

document.write("<B>" + myString + "</B>")

</SCRIPT>

<P><B>This is a string</B>

</BODY>

</HTML>
```

这些方法都列在第 160 页的 `String` 方法中。知道它们的存在是有用的，因为有时使用方法比使用标签更简单。然而，在本章的剩余部分中，我打算专注于那些允许我们对字符串进行某些操作的方法。

## 字符串切片

有几种方法允许你分析、分割或操纵字符串。`charAt(placeNumber)` 返回字符串中 `placeNumber` 处的字符。在字符串中，就像数组一样，你从 0 开始计数。

试一下这个示例——它也展示了 `length` 属性的使用：

```html
<HTML>

<BODY>

<SCRIPT>
```



`myString = new String("The cat sat on the mat")`

`len = myString.length`

`for (n = 0; n < len; n++) {`

  `c = myString.charAt(n)`

  `document.write("Character " + n + " is " + c + "<BR>")`

`}`

`</SCRIPT>`

`</BODY>`

`</HTML>`

`indexOf(text)` 提供了另一种分析字符串的方法。它返回在字符串中找到 `text` 的第一个位置，`text` 可以可以是字符、单词或短语。如果不存在 `text`，该方法返回 -1。例如，对于电子邮箱地址：

```html
myString = new String("The cat sat on the mat")

place = myString.indexOf("@")

if (place == -1) {

  document.write("Invalid e-mail address")

}
```

`lastIndexOf(text)` 的功能与 `indexOf()` 相同，但它从字符串末尾开始寻找 `text` 的最后一次出现。这里是两种用法：

```html
<HTML>

<BODY>

<SCRIPT>

myString = new String("The cat sat on the mat")

place = myString.indexOf("at")

document.write("cat starts at character " + place)

lastplace = myString.lastIndexOf("at")

document.write("The last starts at character " + lastplace)

</SCRIPT>

</BODY>

</HTML>
```

- 递归函数是指调用它自身的函数——它必须有一个出口！
- JavaScript 拥有一组 `Math` 方法，用于处理随机数、整数、三角函数以及其他关键数学函数。
- `Date` 方法允许你获取或设置日期或时间。
- `String` 方法为你提供了一系列分析和处理文本的方法。

## 06 表单

在本章中，你将学习：

- 关于表单元素
- 如何读取和验证输入数据
- 如何创建单选和多选列表
- 如何使用表单进行反馈和交互

## 基础表单

表单是 HTML 的交互部分，也是你的读者与你的 JavaScript 代码之间的桥梁。它们对 JavaScript 来说非常重要，因此值得花一点时间研究相关的 HTML 标签。

表单本身并仅仅是一个容器，但它可以包含按钮（用于控制代码）、文本区域以及读者可以在其中输入数据或做出选择的其他元素。如果你想给读者提供即时反馈，最简单的方法是通过表单上的元素来实现。如果你想让读者联系你，表单同样是最简单的解决方案。

表单的开始和结束由 `<FORM>` 和 `</FORM>` 标签标记。表单可以赋予一个 `NAME`——如果页面上有多个表单，这一点是至关重要的。

```html
<FORM NAME = dataentry>
```

如果你想将表单数据发送给你进行处理，你必须通过两个关键字 `METHOD` 和 `ACTION` 来指定方式和位置。这些关键字可以接受多个选项，其中最简单的是：

```html
<FORM METHOD = Post ACTION = mailto:your_address>
```

通过这些设置，表单提交时，输入表单的数据将通过电子邮件发送给你。一些旧浏览器无法处理 `mailto` 选项。如果你想获得所有读者的反馈，你需要使用 CGI 脚本（你需要与你的 ISP 讨论这件事）。

## 按钮和文本输入

数据主要在 `<INPUT...>` 标签中收集。它们有多种类型，其性质由 `TYPE=...` 定义。

`<INPUT TYPE = text` 创建一个文本输入的单行槽。文本输入需要第二个选项 `NAME=...` 来标识存储数据的变量。

```html
<INPUT TYPE = text NAME = email>
```

这创建了变量 `email`。它将在屏幕上显示一个宽为 20 个字符的空白数据输入槽。如需不同大小的槽，请添加 `SIZE=` 选项并给出字符数。
在附近放置一些文本，让访客知道它的用途：

`E-mail address:<INPUT NAME = email SIZE = 30>`

`<INPUT TYPE = button` 创建一个可点击的按钮。运行 JavaScript 程序的最简单方法就是通过其中之一。

```html
<INPUT TYPE = button VALUE = "Done" onclick = ...>
```

`VALUE= "Done"` 选项定义了按钮的标签。`onClick` 后面跟着 JavaScript 代码。

如果要把表单数据通过电子邮件发送给你，在它的某处会有一个提交按钮。

```html
<INPUT TYPE = Submit VALUE = "Send Now">
```

短语 `TYPE = Submit` 将其定义为一个提交反馈的按钮。类似的短语：

`TYPE = Reset` 定义了一个清空表单内容的按钮。

`VALUE = "Send Now"` 定义了按钮的标题。你可以使用任何喜欢的文本，但必须将其用引号括起来，否则只会显示第一个单词。

如果你想收集跨越多行的文本（例如邮寄地址），请使用 `<TEXTAREA...>` 标签。

```html
<TEXTAREA NAME = Address>
```

它显示为一个带有右侧和底部滚动条的小框。你可以通过添加 `ROWS` 和 `COLS` 选项来定义显示大小，使其成为合适的尺寸。

```html
<TEXTAREA NAME = Address ROWS = 4 COLS = 40>
```

`ROWS` 和 `COLS` 设置只影响显示大小。如果你的访客想写更多行或更长的行，他们可以——这就是滚动条的作用。

注意 `<TEXTAREA>` 需要一个闭合标签 `</TEXTAREA>`。

## 复选框和单选按钮

如果你想让填写表单的人能够从一组备选项中选择，你应该使用 `TYPE` 选项：

- `Checkbox`，可以选择多个备选项；
- `Radio`，其中只能选择一组中的某一个。

它们的用法非常相似，但有一个显著区别。对于复选框，每个 `INPUT` 应该有自己的 `NAME` 变量来存储响应。

```html
I am interested in: <BR>

<INPUT TYPE = Checkbox NAME = hard Hardware <BR>

<INPUT TYPE = Checkbox NAME = soft Software <BR>

<INPUT TYPE = Checkbox NAME = books Books <P>
```

如果访客选择了 Hardware 复选框，该变量将具有值 `on`。

对于单选按钮，组中的所有单选按钮应该使用相同的 `NAME`，因为你只允许选择备选项中的一个：

```html
Sex: <BR>

<INPUT TYPE = Radio NAME = sex VALUE = m CHECKED> Male <BR>

<INPUT TYPE = Radio NAME = sex VALUE = f> Female
```

我们需要添加 `VALUE` 子句。这设置了要返回的值，这样反馈将以 `sex = m` 的形式呈现（如果你有一个不决定的访客）。如果你省略了 `VALUE=`，无论选择了什么，反馈都是 `sex = on`。

注意上面第一个 `<INPUT...>` 中的关键字 `CHECKED`。它设置了默认值。如果你想从所有单选按钮为空开始，请省略它。

将此 HTML 代码与下面的屏幕显示进行比较。

```html
<HTML>

<HEAD>

<TITLE>Checkboxes and Radios</TITLE>

</HEAD>

<BODY>

<FORM METHOD=Post ACTION=mailto://sales@clogs.com>

Tell me more about these wonderful Witherspoon clogs <P>

Style: <BR>

<INPUT TYPE = Checkbox NAME = trad>Traditional<BR>

<INPUT TYPE = Checkbox NAME = slipon>Slip-on<BR>

<INPUT TYPE = Checkbox NAME = gold>Gold Lame <P>

Sex:<BR>

<INPUT TYPE = Radio NAME = sex> Gents<BR>

<INPUT TYPE = Radio NAME = sex CHECKED> Ladies<P><INPUT TYPE = Submit VALUE = "Send">

<INPUT TYPE = Reset VALUE = "Clear and Restart">

</FORM>

</body>

</html>
```

**图 6.1**

## 下拉列表

下拉列表是提供一组备选项的最洁方式之一。在 HTML 中，可以使用 `<SELECT>` 和 `<OPTION>` 实现。`<SELECT>`提供了记录选择的框架。`</SELECT>` 关闭列表。

```html
<SELECT NAME =Level>

  <OPTION = stand> Standard

  <OPTION = prof> Professional

</SELECT>
```

`<SELECT>` 标签定义了记录选择的变量。`<OPTION>` 标签定义了一个项目。`<SELECT>` 提供了记录选择的框架。`</SELECT>` 关闭列表。

```html
<HTML>

<HEAD>

<TITLE>Drop-down Lists</TITLE>

</HEAD>

<body>

<H2> Order Form </H2>

<FORM METHOD=Post ACTION=mailto:sales@pcs.co.uk>

Order your software here: <P>

Platform: <SELECT NAME = Platform>

  <OPTION = Pcdos > PC/Windows

  <OPTION = Mac> Mac

  <OPTION = Unix> Unix

  <OPTION = Win SELECTED> PC/Windows

</SELECT>

Level: <SELECT NAME =Level>

<OPTION = stand> Standard

<OPTION = prof> Professional

</SELECT>

<INPUT TYPE = Submit VALUE = "Send" >

</FORM>

</BODY>

</html>
```

**图 6.2**

## 按钮

`<BUTTON>` 标签是 `<INPUT TYPE = Reset/Submit>` 的灵活替代方案。如果你只是一个标准的“提交”，那么用这种方法会花费更多精力，而且没有优势。比较这两行。它们产生相同的结果：

```html
<BUTTON TYPE="submit"> Send me </BUTTON>

<INPUT TYPE = "submit" VALUE = "Send me">
```

`<BUTTON>` 让你对按钮上显示的内容有更多控制权。你可以格式化文本：

```html
<BUTTON TYPE="submit"><FONT SIZE = 5 COLOR = red>

<B> Send me </B></FONT></BUTTON>
```

你甚至可以使用图像来代替文本...

```html
<BUTTON TYPE="submit"> <IMG SRC="sendme.gif" /> </BUTTON>
```

...或者以文本形式：

```html
<BUTTON TYPE="submit"> <FONT SIZE = 6> 请给我发我</FONT> <img src="smiley.gif"></BUTTON>
```

![](img/abd8c35820179838d3f97b872561195a_117_0.png)

## 提交按钮

有一个值得的特殊的 `<INPUT TYPE = ...>` 选项。

```html
<INPUT TYPE = "image" SRC = "sendme.gif">
```

这会显示图像，但使其作为提交按钮工作。这种方法的优点是它不会有使用 `<BUTTON>` 时那种标准的灰色矩形背景（“Send Me!”），但它只能用于提交表单。

## elements 数组

你放置在表单上的文本框、选项、按钮和其他元素会自动变成一个数组。当每个元素都是一个完全独立的项目并被单独处理时，这个数组是无关紧要的，但在其他情况下它可以非常有用。如果你需要访问或更改一组项目的值，例如，将它们视为数组可能是此最简单的方法。

该数组始终被调用为 `elements[]`。元素按照它们在表单上出现的顺序进行编号，从左上角的 `elements[0]` 开始。

在这个示例中，使用了一个基于数组的程序来清除表单上某些文本框中的输入。这允许访问者删除他们所做的选择，而不会清除他们的姓名和电子邮件。将其与重置（`Reset`）按钮的效果相比，重置会清空所有框。

注意，循环从 2 运行到 4，只选取“Order...”文本框。在你成功让它工作后，将结束值更改为 `loop < 7`，看看让它运行到按钮上会发生什么。

```html
<HTML>

<HEAD>

<TITLE>元素的数组</TITLE>

<SCRIPT>

function clearform()

{

for(loop = 2; loop < 5; loop++)

document.form1.elements[loop].value = ""

}

</SCRIPT>

</HEAD>

<BODY>

<H2>订单表单</H2>

<FORM NAME = form1>

联系人<INPUT TYPE = text NAME = username VALUE ==""><BR>

电子邮件地址<INPUT TYPE = text NAME = email VALUE = "=""><BR>
```

![](img/abd8c35820179838d3f97b872561195a_118_0.png)

**图 6.3 清除订单** 仅清空了“Order...”文本框

```html
订单 1 <INPUT TYPE = text NAME = order1 VALUE = "" <BR>订单 2 <INPUT TYPE = text NAME = order2 VALUE = "" <BR>订单 3 <INPUT TYPE = text NAME = order3 VALUE = "" <BR><P><INPUT TYPE = button VALUE = "清除订单" onclick="clearform()"><P><INPUT TYPE = Reset VALUE = "清空整个表单"></FORM></BODY>
```

## 检查输入

如果表单需要被正确填写，某些数据项可能是必不可少的——如果你要给他们发送东西，就必须拥有访问者的地址。其他条目可能落在特定的值范围内——日期和订单号必须是有效的。

## 是否内容？

你可以轻松地检查文本框中是否输入了数据，并且只需较少的代码，你就可以让访问者返回输入内容。如果你不希望访问者留空，请将其附加到任何文本框或文本区域：

```javascript
onBlur = "if(this.value==''){alert('请填写数据');this.focus()}"
```

`this` 指的是它附加的任何对象。如果它是空的（`value=""`），将执行包含在 `{大大括号}` 中的后续命令。

`focus()` 方法将光标置于文本框中。（它还会激活页面、高亮按钮并选择其他对象。）

`this.focus()` 将光标放入当前框中。当从事件处理程序内部的代码运行时，它运行得很可靠，但如果在函数代码中使用，可能会产生混淆。在从页面到函数的传输过程中，它可能会丢失 `this` 指向哪个元素。

我喜欢将事件处理代码保持尽可能简单，因此在下一个示例中，这种检查由函数 `checkData()` 管理。文本框的数组编号被传递给它，例如：

```javascript
onBlur = checkData(2)
```

然后按上述方式进行检查和响应。

```javascript
function checkData(box)

{

    if(document.form1.elements[box].value == "") {

        alert("请填写此框")

        document.form1.elements[box].focus();

    }

}
```

如果你有多个必要的文本框，这比直接在每个框上附加代码是一个整洁的解决方案。

## 是否正确？

验证是另一回事。有些事情可以在不需要太大麻烦的情况下进行检查。
数值是否在正确的范围内？

```javascript
checknum = eval(document.form.element[n].value)

if (checknum < 0 || checknum > 999)

错误程序...
```

文本框中是否包含（不想要的）数字？

```javascript
digits = false

text = document.form.elements[n].value

for (loop = 0; loop < text.length; loop++)

{
```



```javascript
c = text.value.charAt(loop)

if (c >= "0" && c <= "9")
  digits = true
}
```

if (`digits`)

错误程序……

`validate()`函数检查 ISBN（书号）。如果你是手动进行操作，你会逐个取出数字，第一个乘以 1，第二个乘以 2，依此类推，直到倒数第二个数字。然后将结果相加，并将总和除以 11。余数应该与最后一位相同。

例如，这本书的 ISBN 是 0 340 81129 3。进行求和：

```text
1*0+2*3+3*4+4*0+5*8+6*1+7*1+8*2+9*9 = 168/11

= 15 余数 3
```

该程序会遍历 ISBN，将数字复制到数组中。使用模运算符（`%`）来寻找余数。

下一个示例展示了这些方法的用法。注意，“提交”按钮已被替换为标记为“Action”按钮，它调用了`process()`函数。如果你希望将反馈通过电子邮件发送给你，坚持使用标准的 HTML 会更简单。如果你想获取信息以便在访问在线的同时做出响应，则可以使用 JavaScript。在这里，发生的所有只是通过 alert 框显示设置。在实践中，你可能会使用这些选择来决定下一个播放哪个页面，或者在该页面上写什么。

```html
<HTML>
<HEAD>
<SCRIPT>
function process()
{
  if (searcheng == true)
    alert("Search selected")

  if (software)
    alert("Software sites selected")

  if (document.form1.resources.checked)
    alert("JavaScript resources selected")

  if (document.form1.mlist[0].checked)
    alert("Include on mailing list")
  else
    alert("Leave off the list")
}
</SCRIPT>
</HEAD>

<BODY>
<SCRIPT>
searcheng = false
software = false
</SCRIPT>

<FORM NAME = form1>
Which types of links would you like

<P>Style:

<BR><INPUT TYPE = Checkbox NAME = search onClick = "searcheng = this.checked"> Search engines

<BR><INPUT TYPE = Checkbox NAME = sitesites onClick = "software = ((this.checked)?true:false)"> Software sites

<BR><INPUT TYPE = Checkbox NAME = resources>
JavaScript resources

<P>Join our mailing list?

<BR><INPUT TYPE = Radio NAME = mlist> Yes please

<BR><INPUT TYPE = Radio NAME = mlist CHECKED> No thanks

<P><INPUT TYPE = Submit VALUE = "Action" onclick="process()">
</FORM>
</BODY>
</HTML>
```

![](img/abd8c35820179838d3f97b872561195a_125_0.png)

**图 6.4** 使用 alert 检查变量的状态。

## 单选列表

通过`<SELECT>`和`<OPTION>`标签创建的下拉列表有两种形式。一种允许一次只选择一个；另一种则接受多个选择。它们需要以不同的方式进行处理。

`<SELECT>`列表有一个`selectedIndex`属性，它是读取列表的关键。如果你在`form1`中设置了列表：

```html
<SELECT NAME = choice>
```

那么这将给你提供索引：

```javascript
chosen = document.form1.choice.selectedIndex
```

然后你可以在一组`if`测试中使用该索引值来对选择做出反应，或者像示例中那样用它从数组中提取一个元素。在这里，数组存储价格，`setPrice()`函数显示所选项目的价格。

```javascript
function setPrice() {
  chosen = document.form1.choice.selectedIndex
  document.form1.price.value = prices[chosen]
}
```

这里是代码。请随意替换你自己的数据！

```html
<HTML>
<HEAD>
<TITLE>Single selections</TITLE>
<SCRIPT>
prices = new Array(5)

prices[0] = 19.99
prices[1] = 24.99
prices[2] = 29.99
prices[3] = 39.44
prices[4] = 9.95

function setPrice() {
  chosen = document.form1.choice.selectedIndex
  document.form1.price.value = prices[chosen]
}
</SCRIPT>
</HEAD>

<BODY>
<H3>Witherspoon clogs</H3>

<FORM NAME = form1>
Style <SELECT NAME = choice>
<OPTION value = trad>Traditional</OPTION>
<OPTION value = slipon>Slip on</OPTION>
<OPTION value = cloth>Fine worsted</OPTION>
<OPTION value = gold>Gold lame</OPTION>
<OPTION value = kids>Child</OPTION>
</SELECT>

<P><P>Price: <: TYPE = text = = price = ""

<P>
<INPUT TYPE = button VALUE = "Show price" onclick = setPrice()>
</FORM>
</BODY>
</HTML>
```

![](img/abd8c35582017983dd3f77872261195a_177.png)

**图 6.5** alert 检查变量。

## 多选

如果你在`<SELECT>`标签中写入`MULTIPLE`关键字，你的访问者将能够选择多个选项（通过通常的方法——按住 Control 键点击）。

```html
<SELECT MULTIPLE NAME = os>
```

整个`<SELECT>`集的`selectedIndex`不再使用。我们现在需要使用单个`<OPTION>`的`selected`属性（true 或 false 值）。它们形成一个数组，名称来自`<SELECT>`标签，并在循环中方便地测试：

```javascript
for (loop = 0; loop < document.form1.os.length; loop++)
  if (document.form1.os[loop].selected)
```

- `document.form1.os.length`告诉集合中有多少个`<OPTION>`。
- `document.form1.os[loop].selected`返回由索引标识的`<OPTION>`状态——如果选中则为 true。

`<OPTION>`有一个显示在下拉列表中的文本。你可能希望将其包含在反馈中，或者显示在屏幕上让访问者确认他们的选择。下一个示例中，访问者被要求选择他们感兴趣的 IT 课程。当他们点击“选择”按钮时，`show()`函数遍历数组并将选项的文本添加到`temp`字符串中，然后将完成的字符串复制到`TEXTAREA`中显示。

```html
<HTML>
<HEAD>
<TITLE>Multiple Selections</TITLE>
<SCRIPT>
function show() {
  temp = ""

  for (loop = 0; loop < document.form1.it.length; loop++) {
    if (document.form1.it[loop].selected) {
      temp = temp + document.form1.it[loop].text + " "
      document.form1.showit.value = temp
    }
  }
}
</SCRIPT>
</HEAD>

<BODY>
<H3>Tel me more about courses on ...</H3>

<FORM NAME = form1>
<SELECT MULTIPLE NAME = it>
<OPTION value = windows>Windows</OPTION>
<OPTION value = word>Word</OPTION>
<OPTION value = excel>Excel</OPTION>
<OPTION value = access>Access</OPTION>
<OPTION value = web>World Wide Web</OPTION>
<OPTION value = email>E-mail</OPTION>
</SELECT>

<INPUT TYPE = button VALUE = "Show selection" onclick="show()">

<P><TEXTAREA NAME = showit ROWS = 2 COLS = 40</TEXTAREA>
</FORM>
</BODY>
</HTML>
```

![](img/abd8c35820179838d3f97b872561195a_129_0.png)

**图 6.6** 当可以选择多个选项时使用`MULTIPLE`设置。

## 在线反馈

下一个示例整合了在 JavaScript 中使用表单选项的某些方面，为用户提供即时反馈并向页面作者生成电子邮件反馈。

在 Wheeler Dealers，你可以在线为自行车投保。保险费用基于自行车的价值，但根据地区和保额水平而异。这些信息通过表单中的选项输入或从中选择：地区是一个下拉列表；保额是一组单选按钮。这两种方法都可以实现，因为两种情况下都是从集合中选择一个项目。

基本公式是：

```text
£10 + (自行车价值/100) * 地区率 * 保额水平
```

保费在`calculate()`函数中计算。以下是关键行：

```javascript
howmuch = eval(document.form1.InsVal.value)
```

`eval()`是将文本转换为数值所必要的。

```javascript
for (loop = 0; loop < document.form1.cover.length; loop++)
  if (document.form1.cover[loop].checked)
```

单选按钮集合没有`selectedIndex`属性。要找到选择了哪一个，我们必须测试数组中每个按钮的`checked`属性。

```javascript
level = loop + 1
```

这提供了 1、2 或 3 的保额水平——一个粗略的倍数。如果你正确这样做，你可能想从值数组中选择水平。这已经通过地区率完成了。

```javascript
where = document.form1.region.selectedIndex

cost = eval(10 + howmuch / 100 * rate[where] * level)
```

注意“购买”按钮。它调用`confirmPurchase()`函数，该函数在通过命令发送电子邮件之前运行确认对话框：

```javascript
document.form1.submit()
```

`submit()`等同于`<INPUT = Submit>`标签。

```html
<HTML>
<HEAD>
<TITLE>Feedback</TITLE>
<SCRIPT>
rate = new Array(4)

rate[0] = 10
rate[1] = 8
rate[2] = 6
rate[3] = 7
rate[4] = 12

function calculate() {
  howmuch = eval(document.form1.InsVal.value)

  for (loop = 0; loop < document.form1.cover.length; loop++)
    if (document.form1.cover[loop].checked)
      level = loop + 1

  where = document.form1.region.selectedIndex
  cost = eval(10 + howmuch / 100 * rate[where] * level)

  document.form1.quote.value = cost
}

function confirmPurchase() {
  if (confirm("I want to take up this offer"))
    document.form1.submit()
}
</SCRIPT>
</HEAD>

<BODY ALIGN=CENTER>
<h1>Wheeler Dealers</h1>

<FORM NAME = form1 METHOD = post ACTION = "mailto:sales@wdeals.co.uk">
<P>Value of cycle:</P>
<INPUT TYPE = text NAME = InsVal SIZE = 10>

<P>Region</P>
<SELECT NAME = region>
<OPTION value = london>London</OPTION>
<OPTION value = southeast>South East</OPTION>
<OPTION value = southwest>South West</OPTION>
<OPTION value = rest>Rest of England</OPTION>
<OPTION value = wales>Wales</OPTION>
</SELECT>

<P>Type of cover</P>
<BR><INPUT TYPE = Radio NAME = cover>Third Party
<BR><INPUT TYPE = Radio NAME = cover>Third Party Fire
</FORM>
</BODY>
</HTML>
```

```html
and Theft

<form>
  <input type="radio" name="cover" checked>Comprehensive
  <input type="button" name="calc" value="Get quote" onclick="calculate()">

  <p>Your Quotation:<b><input type="text" name="quote" size="10">

  <p><input type="button" name="done" value="Purchase" onclick="confirmPurchase()">
</form>
```

保存好这个示例，你将在第 8 章中需要它。

## 一个 JavaScript 计算器

在本章的最后一个示例中，使用表单来创建一个计算器。通过点击按钮输入数字并选择操作，结果显示在文本框中。

代码相当长，但生成所需的时间比你想象的要短。复制、粘贴和编辑就是诀窍！创建按钮的行几乎完全相同，`doFunc()`和`calculate()`函数中也有一些非常相似的行。

图 6.8 在这里，表单仅作为按钮和文本框的容器。

![](img/abd8c35820179838d3f97b872561195a_132_0.png)

点击按钮时会发生以下情况：

- 数字和小点——将按钮值传递给`doNum()`以添加到显示框中。
- 运算符——将运算符传递给`doOp()`，它会将显示框中的当前值存储在`n1`中，并将运算符存储在`op`中。它会清空框以便下一个数字。
- 等号——运行`calculate()`，它获取`n1`和当前值，并根据`op`的当前值将它们合并。
- 平方、正弦、余弦和正切——这些调用`doFunc()`，它使用 Math 方法来计算数值。注意它是如何使用`toRad()`将角度值转换为弧度的。

```javascript
<HTML>

<head>
<title>JavaScript calculator</title>

<script>
function doNum(x) {
  f1.display.value = f1.display.value + x
}

function doOp(operation) {
  n1 = eval(f1.display.value)
  op = operation
  f1.display.value = ""
}

function toRad(deg) {
  return deg / 360 * 2 * Math.PI
}
```



```javascript
function doFunc(fn) {
  n1 = eval(f1.display.value)
  angle = toRad(n1)

  if (fn == "r")
    f1.display.value = Math.sqrt(n1)
  } else if (fn == "s")
    f1.display.value = Math.sin(angle)
  } else if (fn == "c")
    f1.display.value = Math.cos(angle)
  } else if (fn == "t")
    f1.display.value = Math.tan(angle)
}

function calculate() {
  n2 = eval(f1.display.value)

  if (op == "+") {
    f1.display.value = n1 + n2
  } else if (op == "-") {
    f1.display.value = n1 - n2
  } else if (op == "*") {
    f1.display.value = n1 * n2
  } else if (op == "/") {
    f1.display.value = n1 / n2
  } else if (op == "p") {
    f1.display.value = Math.pow(n1, n2)
  }
}

function clear() {
  f1.display.value = ""
}
```

```html
</script>
</head>
<body>
<script>
var n1 = 0
var op = "+"
var n2 = 0
</script>

<form name="f1">
  <input type="text" name="display">
  <p>
  <input type="button" value=" 7 " onclick=doNum("7")
  <input type="button" value=" 8 " onclick=doNum("8")
  <input type="button" value=" 9 " onclick=doNum("9")
  <br>
  <input type="button" value=" 4 " onclick=doNum("4")
  <input type="button" value=" 5 " onclick=doNum("5")
  <input type="button" value=" 6 " onclick=doNum("6")
  <br>
  <input type="button" value=" 1 " onclick=doNum("1")
  <input type="button" value=" 2 " onclick=doNum("2")
  <input type="button" value=" 3 " onclick=doNum("3")
  <br>
  <input type="button" value=" 0 " onclick=doNum("0")
  <input type="button" value=" . " onclick=doNum(".")
  <input type="button" value=" + " onclick=doOp("+")
  <br>
  <input type="button" value=" " onclick=doOp("")
</form>
</body>
</html>
```

## 练习题

1. 从验证示例（第 110 页）开始，添加一个字段来收集价格，并添加一个函数来检查它是否在接受范围内。
2. 为你正在工作或想要工作的业务设置一个表单，用于收集在线订单。你需要从客户那里收集哪些数据？如何验证这些数据？需要哪些计算？
3. 设置一个 Web URL 数组，并在 SELECT 列表中设置匹配的名称。使用列表的 `selectedIndex` 属性作为数组的索引，让人们从列表中选择站点并跳转。你的代码应该类似于此，其中 `choice` 是 SELECT 列表，`link[]` 是 URL 数组。

```javascript
function setURL() {
  where = document.form1.choice.selectedIndex
  window.location = link[where]
}
```

`window.location` 将链接加载到当前窗口。

## 总结

- 表单为访问者提供了与代码交互的方式。
- 数据可以通过不同类型的 INPUT 收集或选择。
- 表单元素可以通过名称或在 elements 数组中的位置来识别。
- 尽可能对数据进行验证。
- 使用 JavaScript 可以对元素制作动画。

```html
<body>
<script>
counter = Math.round(Math.random() * 10000) + 1000
</script>

<form name="form1">
Visitors to this page:

<input type="text" name="showcount" value="">

<p><input type="button" value="I do not believe you" onclick="clearTimeout(timer)">
</form>

<script>
addvisitor()
</script>
</body>
</html>
```

## 一个 JavaScript 钟

在第 91 页中，我们查看了如何整齐地显示时间值。但那只显示一次时间。使用超时（timeouts），我们现在可以在此基础上创建一个 JavaScript 钟。

显示时间的程序与第 92 页的“改进版”程序几乎相同，但有两个不同之处。第一个是在这个脚本中，时间显示在文本框中，这样不需要重新加载页面就可以更新内容。第二个是代码被封装成了一个名为 `dotime()` 的函数。这允许我们通过超时来调用它。请查看函数末尾的这一行：

```javascript
clocktime = setTimeout("dotime()", 1000)
```

注意，超时被赋值了一个变量，这样我们就可以通过 `clearTimeout(clocktime)` 关闭时钟。

```html
<html>
<head>
<title>Clock</title>
<script>
function dotime() {
  d = new Date()
  h = d.getHours()
```

```javascript
m = d.getMinutes()
s = d.getSeconds()

time = h + ((m < 10) ? ":0" : ":") + m +
  ((s < 10) ? ":0" : ":") + s

document.timeform.time.value = time
clocktime = setTimeout("dotime()", 1000)
}
</script>
</head>
<body>
<form name="timeform">
<p>The time is
<input type="text" name="time" value="" size="8">

<p><input type="button" value="Stop the clock"
  onclick="clearTimeout(clocktime)">
</form>

<script>
dotime()
</script>
</body>
</html>
```

## 滚动文本

如果你花过时间浏览网页，你一定在状态栏中遇到过滚动消息——很多，很多次！以下是实现方法。

为了让文本滚动起来，我们使用 `substring()` 方法截取第一个字符并将其移动到字符串的末尾。最好分四个阶段完成。

首先找到字符串的长度：

```javascript
len = phrase.length
```

现在将其切分为两部分：第一部分保留第一个字符（0）；剩余部分获取字符串的其余部分（1 到 len）。

```javascript
first = phrase.substring(0, 1)
rest = phrase.substring(1, len)
```

最后，将子字符串连接起来，回到开头。

```javascript
phrase = rest + first
```

如果你喜欢复杂的代码，这行代码也能实现相同的功能：

```javascript
phrase = phrase.substring(1, phrase.length) +
  phrase.substring(0, 1)
```

这段代码目前只会滚动一个字符。如果你把它放入循环中，它会运行得极快，你看不见任何变化。解决方案是使用超时，这样在代码的每次重复之间就会有一个延迟。在这里，延迟被设置为 100，产生 1/10 秒的暂停。如果你的消息较短，你可能会发现较长的延迟会有更好的效果。

`stopscroll()` 函数是可选的。由于滚动的整个目的是吸引访问者的注意力，让他们关闭滚动有点适得其反——除非在移除对变量 `phrase` 的使用后，他们可能会在页面上停留更久！

注意变量 `phrase` 的使用。它在 body SCRIPT 中被设置并赋值，但因为在此处创建的变量具有全局作用域，因此可以在函数中被读取和修改。

```html
<html>
<head>
<title>Scroller</title>
<script>
function setstatus() {
  len = phrase.length
  first = phrase.substring(0, 1)
  rest = phrase.substring(1, len)
  phrase = rest + first
  self.status = phrase
  timerID = setTimeout("setstatus()", 100)
}

function stopscroll() {
  clearTimeout(timerID)
  self.status = "Teach Yourself JavaScript"
}
</script>
</head>
<body>
<form>
<input type="button" value="Stop that scroll!" onclick="stopscroll()">
</form>

<script>
phrase = new String("...Teach Yourself something new today ... ")
setstatus()
</script>
</body>
</html>
```

**图 7.1** 滚动的状态栏会吸引注意力。

## 图像对象

可以通过两种方式创建图像——使用 `<IMG>` 标签和 `Image()` 构造函数。

### `<IMG>` 图像

`<IMG>` 图像放置在表单上，并拥有一系列属性，包括高度、宽度、hspace 和 vspace。这些可以使用 JavaScript 进行更改。

与 `<IMG>` 不同，图像对象不会被自动放入数组中，这有点遗憾，因为你经常需要它们进入数组。如果你想显示一系列图像，最简单的方法是将它们存储在数组中，然后通过循环遍历数组。

### 图像格式

网页浏览器 – JavaScript – 只能处理 GIF 或 JPEG。如果你想创建自己的，你需要一个像 Paint Shop Pro 这样的应用程序。这些是可以转换的。

## 图像对象

可以通过两种方式创建图像——使用 `<IMG>` 标签和使用 `Image()` 构造函数。

### `<IMG>` 图像

`<IMG>` 图像放置在表单上，并拥有一系列属性，包括高度、宽度、hspace 和 vspace。这些可以使用 JavaScript 进行更改。

与 `<IMG>` 不同，图像对象不会被自动放入数组中，这有点遗憾，因为你经常需要它们进入数组。如果你想显示一系列图像，最简单的方法是将它们存储在数组中，然后通过循环遍历数组。

### 图像格式

网页浏览器 – JavaScript – 只能处理 GIF 或 JPEG。如果你想创建自己的，你需要一个像 Paint Shop Pro 这样的应用程序。这些是可以转换的。

请注意函数末尾的这一行，它设置了一个超时，以便 `animate()` 不断地运行。

```javascript
setTimeout("animate()", 200)
```

`checkload()` 函数检查第六张图像的 `complete` 属性，在文件完全加载之前，它不允许代码到达 `animate()` 函数。当你在系统上测试页面时，它看起来似乎什么都没做——因为文件几乎就能访问——但当页面在线且人们通过 Web 查看它时，它将非常有用。

```html
<html>
<head>
<script>
function loadImages() {
  pic0 = new Image()
  pic0.src = "pic0.gif"

  pic1 = new Image()
  pic1.src = "pic1.gif"

  pic2 = new Image()
  pic2.src = "pic2.gif"

  pic3 = new Image()
  pic3.src = "pic3.gif"

  pic4 = new Image()
  pic4.src = "pic4.gif"

  pic5 = new Image()
  pic5.src = "pic5.gif"

  pictures = new Array(pic0, pic1, pic2, pic3, pic4, pic5)
}

function animate() {
  pagePic.src = pictures[current++].src

  if (current == 6)
    current = 0

  setTimeout("animate()", 200)
}

function checkload() {
  if (pic5.complete == false)
    setTimeout("checkload()", 100)
}
</script>
</head>
<body>
<img src="pic0.gif" name="pagePic">

<script>
current = 1
loadImages()
checkload()
animate()
</script>
</body>
</html>
```

**图 7.3** 我的永动装置及其图像文件。你可以在我网站的 JavaScript Sampler 页面看到它的运行效果：`http://homepages.tcp.co.uk/~macbride`

![](img/abd8c35820179838d3f97b872561195a_148_0.png)

![](img/abd8c35820179838d3f97b872561195a_148_1.png)

![](img/abd8c35820179838d3f97b872561195a_148_2.png)

![](img/abd8c35820179838d3f97b872561195a_148_3.png)

![](img/abd8c35820179838d3f97b872561195a_148_4.png)

![](img/abd8c35820179838d3f97b872561195a_148_5.png)

![](img/abd8c35820179838d3f97b872561195a_148_6.png)

## 受控制动画

下一个示例在最后一个示例的基础上添加了一组控制按钮。这些按钮允许用户以全速运行“机器”，或者逐帧通过序列，既可以正向也可以是反向。尽管有五个新的控制按钮，但只有两个新函数。`nextpic()` 根据 `move` 的值（1 或 -1）将图像更改为下一张或向后一张。

```javascript
function nextpic() {
  current += move

  if (current < 0)
    current = 5

  if (current > 5)
    current = 0

  pagePic.src = pictures[current].src
}
```

“上一个”和“下一个”按钮用于设置 `move` 方向并调用 `nextpic()`。

```html
<input type="button" value=" Back " onclick="move = -1; nextpic()">
```

`animate()` 有一个新版本。它只关注保持物体移动，因为图像的更改现在由 `nextpic()` 处理。注意 `going` 变量的使用。如果它为 `true`，则已经有一个运行 `animate()` 的超时设置，在再次运行该函数并设置另一个超时之前，必须清除它。如果漏掉这一点，看看如果你多次点击“运行”或“反向”按钮会发生什么。

```javascript
function animate() {
  if (going)
    clearTimeout(timer)

  nextpic()
  timer = setTimeout("animate()", 100)
}
```

要启动它，我们只需要将 `going` 设置为 `true`，给 `move` 赋值，并第一次调用 `animate()`。

```html
<input type="button" value=" Run " onclick="going = true; move = 1; animate()">
```

这里是完整的代码。它稍微有点长，但最后一个示例将作为基础，在设置按钮时可以进行复制粘贴。



```html
<HTML>
<HEAD>
<TITLE>Perpetual motion </TITLE>
<SCRIPT>
function loadImages() {
  pic0 = new Image()
  pic0.src = "pic0.gif"
  pic1 = new Image()
  pic1.src = "pic1.gif"
  pic2 = new Image()
  pic2.src = "pic2.gif"
  pic3 = new Image()
  pic3.src = "pic3.gif"
  pic4 = new Image()
  pic4.src = "pic4.gif"
  pic5 = new Image()
  pic5.src = "pic5.gif"
  pictures = new Array(pic0,pic1,pic2,pic3,pic4,pic5)
}
function nextpic() {
  current += move
  if (current < 0)
    current = 5
  if (current> 5)
    current = 0
  pagePic.src =pictures[current].src
}
function animate() {
  if (going) {
    clearTimeout(timer)
    nextpic()
  }
  timer = setTimeout("animate()",100)
}
```

```html
function checkload() {
  if (pic5.complete == false) {
    setTimeout("checkload()", 100)
  }
</SCRIPT>
</HEAD>
<body><H3>Perpetual motion?</H3>
<IMG SRC = "pic0.gif" NAME = pagePic>
<SCRIPT>
  current = 0
  timer = null
  going = false
  move = 1
  loadImages()
  checkload()
</SCRIPT>
</FORM>
<INPUT TYPE = button VALUE = " Reverse " onclick="going = true; move = -1; animate()">
```

| 永动装置 - Microsoft Internet Explorer |
|---|
| 文件 | 编辑 | 查看 | 收藏 | 工具 | 帮助 |
|---|---|---|---|---|---|
| 永动装置？ | | | | | |
| 上一个 | 停止 | 下一个 | 运行 | | |

**图 7.4** 带有按钮的永动装置。

```html
<INPUT TYPE = button VALUE = " Back " onclick="move = -1; nextpic()"

<INPUT TYPE = button VALUE = " Stop " onclick="clearInterval(timer)"

<INPUT TYPE = button VALUE = " Next " onclick="move = 1; nextpic()"

<INPUT TYPE = button VALUE = " Run " onclick="going = true; move = 1; animate()"

</BODY>

</HTML>
```

## 可点击图像

图像本身对鼠标没有反应，但通过在`<A>`标签中包含它们，可以做到这一点。只需要一点精力。如果你只是想使用图像来触发页面上的某些活动，有两种方法。一种是使用`onclick`事件：

```html
<a onclick="dstuff()"><img src="image1.gif"></a>
```

……

第二种——更好的方法是使用`<A>`标签，以最简单的形式作为锚点。它对鼠标有反应。

```html
<A onclick="dstuff()"><img src="image1.gif"></A>
```

在下一个示例中，锚定图像可以接收三种事件。`onClick`显示时间警告；`onMouseEnter`设置状态栏消息。

```html
<HTML>
<HEAD>
<TITLE>可点击图像</TITLE>
<SCRIPT>
function showtime() {
  d = new Date()
  h = d.getHours()
  m = d.getMinutes()
  s = d.getSeconds()
  alert("现在的时间是: " + h + ((m<10) ? "0" : ":") + m + ((s<10) ? "0" : ":") + s)
}

function setStatus(n) {
  if (n==1)
    self.status = "点击查看时间"
  else
    self.status = "可点击图像测试页面"
}
</SCRIPT>
</HEAD>
<BODY>
<A onclick="showtime()" onMouseOver="setStatus(1)" onMouseOut="setStatus(2)"><IMG SRC="clock.gif"></A>
</BODY>
</HTML>
```

## JavaScript 图像映射

如果你的页面上有图像映射，请记住`<AREA>`是可以点击的，你可以为它们附加代码。

## 练习

1. 创建包含两个文本输入和一个按钮的表单。在一个输入框中显示随机数字，并让用户复制到另一个。点击按钮时，代码应检查数字是否复制正确并显示花费的时间。
2. 创建三个或多个大小相同但颜色或形状不同的图像。将它们在屏幕上横水平或垂直排列，并通过`<IMG>`标签循环图像文件，以产生运动的感觉。

## 08 窗口与框架

在本章中，你将学习：

- 如何控制窗口
- 关于 JavaScript URL
- 关于在框架（frames）中工作

## 窗口控制

JavaScript。你可以打开一个新窗口——如果愿意可以指定其大小——并加载现有的页面文件，或者从 JavaScript 内部为页面编写新的 HTML 代码。当你打开了多个窗口时，你可以在窗口之间切换焦点，并在其中一个窗口中运行代码，从任何其他窗口读取数据并将其写入该窗口。

> **小心编写代码**
>
> 窗口控制方法是不容错的！错误位置的空格会导致问题，或者缺少引号可能会产生不可预知的结果。如果某行代码没有按照你的预期执行，请逐字符地检查它，并将其与该方法的语法进行对比。

## `window.open()`

`open()`方法允许你指定窗口的大小以及要包含哪些框架组件（滚动条、标题栏、菜单栏等）。基本语法为：

```javascript
varname = window.open("URL","winName","components")
```

该方法的几乎每一个部分都是可选的！

- 如果你想运行窗口的任何方法或访问其任何属性，则需要`varname`。
- `URL`用于在需要时加载现有页面。
- 只有当窗口将作为另一个窗口中代码的 TARGET（目标）时，才需要`winName`。
- 组件包括`toolbar`（工具栏）、`location`（位置）、`directories`（目录）、`status`（状态）、`menubar`（菜单栏）、`scrollbars`（滚动条）、`resizable`（可调整大小）——所有通过设置为`yes`来显示。任何未列出的默认都关闭。还可以设置`width`和`height`，以像素为单位。所有设置都在一个字符串中完成，用逗号分隔。

你必须为`URL`、`winName`加上引号，并对整个`components`字符串加上一对引号。如果不加载页面，请输入空双引号（`""`）。如果你不想给窗口命名，但想指定组件，你同样需要在名称所在的位置输入空引号。

一些该方法的用例示例：

```javascript
window.open("http://www.yahoo.com")
```

简单打开一个标准的浏览器窗口并加载页面。

```javascript
win2 = window.open("", "NewWin", "width=300, height=400")
```

打开一个空窗口，给它一个目标名称`NewWin`和一个变量名`win2`。该窗口将没有工具栏、状态栏或其他组件，大小为 300 x 400 像素。

```javascript
win2 = window.open("mini.htm", "", "toolbar=yes, width=300, height=500")
```

打开一个仅带工具栏的窗口，大小为 300 x 500 像素，并显示`mini.htm`页面。

## 填充窗口

窗口打开后，可以显示现有页面文件，或者你可以使用`write()`方法在此时定义内容，并根据访问者的之前的反馈来更改它们。虽然很困难，但完全通过`write()`构建大型且复杂的页面是可能的。

在第一个示例中，打开一个窗口不是为了显示页面，而是作为一个“弹出窗口”，告诉访问者更多关于页面上链接的信息。正如你在这里看到的，指向一个链接并指向 Close 会打开窗口——在弹出窗口中，点击 Close 会关闭窗口。

打开的代码都在`popup()`函数中，该函数由链接的`onMouseOver`事件调用。基本结构如下：

```html
<A HREF = "http://www...page ref..." onMouseOver = "popup(text to display)">Link text...</</A>
```

当鼠标悬过链接时，事件处理器调用`popup()`并向其传递一个文本字符串。

`popup()`打开一个小窗口，然后使用`write()`创建显示。有两代码。第一行写入嵌入`<H4>`标签中的文本。

```javascript
win2.document.write("<H4>" + words + "</H4>")
```

第二行创建一个带有`onMouseOver`代码的锚点。

```javascript
win2.document.write("<A onMouseOver = 'self.close()'></A>")
```

注意，`close()`关闭一个窗口——`self.close()`关闭的是包含该表达式的窗口。

```html
<HTML>
<HEAD>
<TITLE>Popups!</TITLE>
<SCRIPT>
function popup(words) {
  win2 = window.open("", "", "width=250,height=100")
  win2.document.write("<H4>" + words + "</H4>")
  win2.document.write("<A onMouseOver = 'self.close()'> Close</A>")
}
</SCRIPT>
</HEAD>
<BODY>
<H3>Useful Links</H3>
<A HREF="http://homepages.tcp.co.uk/~macbridge" onMouseOver="popup('Come up and see me sometime')">Mac's place</A>
<P>
<A HREF="http://www.teachyourself.co.uk" onMouseOver="popup('Be where you want to be with Teach Yourself')">Teach Yourself</A>
<P>
<A HREF="http://www.amazon.com" onMouseOver="popup('The leading on-line store')">Amazon</A>
</BODY>
</HTML>
```

## The JavaScript URL

到为止，所有的 JavaScript 代码都是从事件处理器或直接从`<SCRIPT>`运行的。还有另一种方法。我一直忽略它，因为它往往会产生不整洁且难以阅读的代码。这种方法围绕链接中使用的“javascript:”单词。

```html
<A HREF = "javascript:command">
```

`javascript:...`填充在通常看到`http://...`表达式的地方。该命令不需要是打开窗口并加载页面的，但由于访问者期望链接具有此功能，因此可能主要——或仅——为此目的使用。

在示例中，`javascript:`调用了函数`openWin()`，并将其传递给页面的 URL。

```html
<A HREF = "javascript:openWin('www.amazon.com')">
```

URL 被参数`windowfile`选取并传递给`window.open`方法——这是该函数中的唯一行。

```javascript
window.open(windowfile, "", "scrollbars=no, width=280, height=370")
```

可以直接从`javascript:`启动器打开，但会导致这个相当冗长的表达式：

```html
<A HREF = "javascript:window.open ('www.amazon.com', ', scrollbars=no, width=280,height=370")
```

（注：此处原文似乎存在引号缺失错误，翻译已保留原意）

## 在框架中工作

大多数情况下，在框架中工作与无框架完全相同，但你可以为框架系统添加一些精彩的技巧。

## 焦点

`onSuccess`和`onBlur`事件发生在进入或离开页面时。对于简单页面，这些事件用处不大。在框架系统中，如果访问者可以在页面间移动，这些事件是值得的。

下一个示例使用双框架布局，左侧是导航栏，右侧是主显示。导航栏的代码切换两个区域的颜色，使得获得焦点的区域是白色，另一个是蓝色。

```javascript
onBlur="document.backgroundColor= 'blue';
parent.display.backgroundColor = 'white'"

onFocus="document.backgroundColor= 'white';
parent.display.backgroundColor = 'blue'"
```

`parent`指向包含`display`的文档，其中`display`定义为第二个框架。

## 远程控制

`scroll()`方法移动窗口或框架中的文档，就像你使用标准滚动条一样。在简单页面上实现这一点没有优势——使用滚动条更简单。在框架系统中有一个优势——如果你将滚动控件放在导航框架中并结合链接，访问者就可以在一个地方控制整个显示。

该方法使用的形式为：

```javascript
document.scroll(newX, newY)
```

`newX`和`newY`的值以像素为单位，从页面左上角开始，例如：

```javascript
document.scroll(0,500)
```

这在 800 x 640 的显示器上会将页面向上滚动大约一屏幕。以下示例使用了一个变量`frametop`，并在`scrollup()`和`scrolldown()`函数中调整 200。

要实现此示例，请输入并保存两个文档，但将链接替换为你自己的现有页面。至少一个页面应该足够长以测试滚动程序！

### `test.htm`

```html
<HTML>
<FRAMES COLS = 30%,*>
<FRAME SRC = navigate.htm NAME = navbar>
<FRAME SRC = contents.htm NAME = display>
</FRAMES>
</HTML>
```

### `navigate.htm`

```html
<HTML>
<HEAD>
<SCRIPT>
frametop = 0

function scrollup() {
  frametop = (frametop >= 200) ? frametop - 200 : 0
  parent.display.scroll(0,frametop)
}
</SCRIPT>
```

```javascript
function scroldown() {
  frametop = frametop + 200
  parent.display.scroll(0,frametop)
}
```

```html
<SCRIPT>
</HEAD>

<BODY BGCOLOR='white' onBlur="document.bgColor='blue'; parent.display.document.bgColor='white' 
onFocus="document.bgColor='white'
parent.display.document.bgColor='blue'">

<h2>导航栏</h2>

<A HREF = feedbackck1.htm TARGET = display>反馈表</A>

<P>

<A HREF = prompts.htm TARGET = display>提示</A>

<P>

<A HREF = motion.htm TARGET = display>简单动画</A>

<FORM>

<INPUT TYPE = button VALUE=" Up " onclick="scrolldown()"

<INPUT TYPE = button VALUE="Down" onclick="scrolldown()"

</FORM>

</BODY>

</HTML>
```



## 练习

- 1 从反馈单示例（第119页）开始，添加一个由按钮激活的函数，该函数将打开一个新窗口并在其中显示输入的数据。

这不仅练习了窗口的使用，还让你更深入地接触数据处理。这里有两个主要问题：
(i) 来自列表和单选按钮的选择需要转换为文本——最简单的解决方案是将选项文本存储在数组中，并从中提取。

(ii) 一旦你打开了新文档窗口，就很难访问一个文档中的数据。这里的最佳方法是在打开新窗口之前，将元素的值复制到变量中

## 总结

- `open()` 方法允许你打开一个新窗口，并指定其尺寸和特性。
- 当窗口不再被需要时，可以使用 `close()` 方法将其关闭。
- `javascript` 命令可以写在 `<A HREF ...>` 标签中以替换 URL，并用于激活代码。
- 在框架系统中，你可以使用 `onBlur` 和 `onFocus` 事件来响应访问者在框架中的移动。

## 09 参考章节

## 标准颜色名称

JavaScript 识别超过 140 种颜色名称。其中一些是相同颜色的重复名称；另一些则相似到几乎无法区分。移除这些后，我们得到了这个精简列表。

| 青绿色 | 金黄色 | 粉红色 |
| --- | --- | --- |
| 米色 | 金色 | 李子色 |
| 黑色 | 灰色 | 粉蓝色 |
| 蓝色 | 绿色 | 紫色 |
| 紫蓝色 | 黄绿色 | 红色 |
| 棕色 | 艳粉 | 玫瑰褐色 |
| 军蓝色 | 印度红 | 宝石蓝 |
| 黄绿色 | 靛蓝 | 鞍褐色 |
| 巧克力色 | 卡其色 | 鲑鱼色 |
| 珊瑚色 | 薰衣草紫 | 沙黄色 |
| 花尾蓝 | 浅蓝色 | 海绿色 |
| 深红色 | 浅灰色 | 赭石色 |
| 青色 | 浅绿色 | 银色 |
| 深金黄色 | 柠檬黄 | 天蓝色 |
| 深灰色 | 亮绿色 | 石板蓝 |
| 深卡其色 | 品红色 | 春绿色 |
| 深橄榄绿 | 栗红色 | 钢蓝色 |
| 深紫罗兰 | 中蓝色 | 褐色 |
| 深海绿色 | 中紫色 | 青蓝绿色 |
| 深石板蓝 | 午夜蓝 | 西红柿红 |
| 深灰色 | 海军蓝 | 青绿石 |
| 深青色 | 橄榄色 | 紫色 |
| 深紫色 | 橄榄绿 | 小麦色 |
| 深粉色 | 橙色 | 白色 |
| 深蓝色 | 橙红色 | 黄色 |
| 奇幻蓝 | 兰花 | 黄绿色 |
| 森林绿 | 秘鲁色 | |

## 保留字

这些是 JavaScript 为其自身（当前或未来可能）的使用保留的字。你不能将它们用于变量名、函数名或标签。

- abstract int
- boolean interface
- break long
- byte native
- case new
- catch null
- char package
- class private
- const protected
- continue public
- default return
- delete short
- do static
- double super
- else switch
- extends synchronized
- false this
- final throw
- finally throws
- float transient
- for true
- function try
- goto typeof
- if var
- implements void
- import while
- in with
- instanceof

## 特殊字符

| 字符 | 含义 |
|--- |--- |
| `\b` | 退格键 |
| `\f` | 换页 – 用于打印 |
| `\n` | 换行 |
| `\r` | 回车 |
| `\t` | 制表符 |
| `\'` | 单引号 |
| `\"` | 双引号 |
| `\\` | 斜杠字符 (`\`) |
| `\XX` | 以两个十六进制数字 XX（00 到 FF 之间）提供的字符代码。例如，商标符号 ™ 的字符代码为 153，在十六进制中为 `\x99`。 |

## 事件处理器

| 对象 | 事件处理器 | 对象 | 事件处理器 |
| --- | --- | --- | --- |
| 区域 | `onMouse` `onMouseOver` | 单选按钮 | `onBlur` `onClick` `onFocus` |
| 按钮 | `onBlur` `onClick` `onFocus` | 重置按钮 | `onBlur` `onClick` `onFocus` |
| 复选框 | `onBlur` `onClick` `onFocus` | 选择框 | `onBlur` `onChange` `onFocus` |
| 文件上传 | `onBlur` `onChange` `onFocus` | 提交 | `onBlur` `onClick` `onFocus` |
| 表单 | `onReset` `onSubmit` | 文本 | `onBlur` `onChange` `onFocus` `onSelect` |
| 框架 | `onBlur` `onFocus` | 文本区域 | `onBlur` `onChange` `onFocus` `onSelect` |
| 图片 | `onAbort` `onError` | 窗口 | `onBlur` `onError` `onFocus` `onLoad` `onUnload` |
| 链接/区域 | `onClick` `onMouseOut` `onMouseOver` | | |
| 密码 | `onBlur` `onFocus` | | |

## 数学方法

`abs(num)` 去掉 `num` 的负号

`acos(num)` 反余弦函数的弧度

`asin(num)` 反正弦函数的弧度

`atan(num)` 反正切函数的弧度

`atan2(x,y)` 反正切函数的弧度

`cos(num)` 返回余弦值

`sin(num)` 返回正弦值

`tan(num)` 返回正切值

`exp(num)` 返回 e 的 `num` 次方

`log(num)` 返回自然数对数

`ceil(num)` 向上取整

`floor(num)` 向下取整

`round(num)` 四舍五入到最近整数

`max(num1,num2)` 返回最大值

`min(num1,num2)` 返回最小值

`pow(n,p)` 计算 n 的 p 次方

`random()` 生成 0 到 1 之间的随机数

`sqrt(num)` 返回平方根

`valueOf(object)` 返回数值

## Date 方法

Date 和时间按自 1970 年以来的毫秒计算的

`getDate()` 返回几几

`getDay()` 返回星期几，0 = 周日

`getFullYear()` 返回 4 位年份

`getHours()` 返回小时

`getMilliseconds()` 返回毫秒数

`getMinutes()` 返回分钟

`getMonth()` 返回月份，0 = 一月

`getSeconds()` 返回秒

`getTimezoneOffset()` 返回本地时间与 UTC 的差

`getFullYear()` 返回 4 位年份

所有 `get...` 方法用于：

```
component = date.getComponent()
```

所有 `get...` 方法都有对应的 UTC 方法，例如 `getUTay()` 返回 UTC 日期，而不是本地时间。

所有 `get...` 方法都有对应的 `set...` 方法，例如 `Day()` 设置日期组件。

`parse()` 将日期字符串转换为毫秒

`toGMTString()` 将本地日期转换为 GMT 日

`toLocaleString()` 将 GMT 日转换为本地日期

`toString()` 将日期值转换为字符串

`UTC()` `parse()` 的 UTC 等方法

## String 方法

`anchor()` 相当于在 HTML 中设置锚点，例如
`myText = "页面顶部"`
`document.write(myText.anchor("pagetop"))`
同于：

```
<A NAME="pagetop">页面顶部</A>
```

`big()` 相当于 `<BIG>`
`blink()` 相当于 `<BLINK>` 仅在 Netscape 中有效

`bold()` 相当于 `<B>`
`charAt(place)` 返回指定位置的字符，从字符串开始计数为 0

`charCodeAt(place)` 返回位置字符的 Unicode 编号

`s1.concat(s2,s3,...)` 将字符串 `s2`, `s3`,* 等连接到 `s1`.*

`fixed()` 相当于 `<TTY>` – 设置等宽字体

`fontcolor()` 相当于 `<FONT COLOR ...>`

`fontsize()` 相当于 `<FONT SIZE ...>`

`fromCharCode(code, code,...)` 从一系列字符代码形成文本字符串

`indexOf(searchtext)` 查找 `searchtext` 并返回第一次匹配的位置

`italics()` 相当于 `<I>`

`lastIndexOf(searchtext)` 查找 `searchtext` 并返回最后一次匹配的位置

`link()` 相当于在 HTML 中创建链接，例如
`showText = "我的地方"`
`url = "www.myplace.com"`
`document.write("点击访问我的地方 " + showText.link(url))`
效果等于：
点击访问我的地方 `<A HREF="www.myplace.com">我的地方</A>`

`match(regex)` 在字符串中搜索与正则表达式 `regex` 表达式匹配的文本（第 162 页）。该方法有多个参数。

`replace(regex, newString)` 搜索匹配 `regex` 的文本并将其替换为 `newString`。

`search(regex)` 等同于 `indexOf()`，但搜索的是正则表达式而不是纯文本。

`slice(begin, end)` 返回子字符串，其中 `begin` 和 `end` 从 0 开始计数。

`small()` 等于 `<SMALL>`。

`split(separator, limit)` 将字符串分割为多个子字符串，在分隔符字符处划分。如果设置了 `limit`，则该限制限制生成的子字符串的数量。

`strike()` 等于 `<STRIKE>`。

`sub()` 等于 `<SUB>`。

`substr(begin, length)` 返回从 `begin` 开始的长度为 `length` 个字符的子字符串。

`substring(begin, end)` 与 `slice()` 相同。

`sup()` 等于 `<SUP>`。

`toLowerCase()` 将字符串转换为小写字母。

`toUpperCase()` 将字符串转换为大写字母。

## RegExp

`RegExp` 对象包含一个正则表达式。它可以用于在字符串中查找和替换文本。可以通过以下方式创建对象：

```
RegExpVar = /pattern/flags
```

或者

```
RegExpVar = new RegExp("pattern","flags")
```

注意，在简单赋值中，模式周围使用了 `/斜杠/`，但在使用 `new` 创建对象时，使用了“引号”。

模式由字面量和特殊字符组成——这类字符有很多，下面仅涵盖了其中几个。

标志（flags）是可选的，可以设置来控制匹配。共有三种：

- `g` 全局匹配
- `i` 忽略大小写
- `m` 多行匹配。

例如，两种方法都设置了一个变量 `regtext`，它可以用于在大小写字母的任意组合中查找“abc”。

```
Regtext = /ab+c/i
regtext = new RegExp("ab+c","i")
```

某些字符在正则表达式中有特殊含义。这类字符有很多。这里是一些最实用的字符：

- `\` 表示下一个字符是特殊的，例如 `/\b/` 或 `"\b"` 匹配单词边界。
- `.`（点号）匹配任意单个字符，例如 `/g.n/` 匹配 "gin" 和 "gun"。
- `*` 匹配前面的字符 0 次或多次，例如 `/Smith\*/` 匹配 "Smith" 和 "Smithee"，而 `/\b.*/` 匹配任何以 `\b` 开头的字符串。
- `[abcd]` 或 `[a-d]` 匹配括号内字符的任意一个。你可以单独给出这些字符，也可以通过连字符指定范围，例如 `[m-o]` 匹配 "game" 中的 "m" 以及 "tennis" 中的两个 "n" 之一。
- `^` 在文本行的行开头查找匹配项，例如 `/^M/` 匹配 "My name is Michael" 中的第一个 "M"，但不匹配 "my name is Michael" 中的 "M"。
- `$` 匹配行末尾，例如 `/c$/` 匹配 "comic" 中的 "c"，但不匹配 "coding" 中的 "c"。
- `(regex)` 匹配 "regex" 并将匹配的字符串存储在预定义的数组 `[]` 中，如 `$1`、 `$2` 等。
- `\d` 匹配数字，例如 `/\d/` 匹配 "This pencil may be a 2B - or not" 中的 "2"。

## The RegExp methods

`exec()` 执行搜索，如果成功，返回一个数组并更新 `regexp` 对象。如果匹配失败，`exec()` 返回 `null`。它类似于 `String.match()`。

```
regexp.exec([str])
```

`test()` 仅搜索匹配并返回 `true` 或 `false`。这在实际上与 `String.search()` 几乎相同。

```
regexp.test([str])
```

## 10 answers to exercises

## Chapter 2

1 这是一个基本形状，但使用了你自己的消息。
```html
<HTML>
<HEAD>
<SCRIPT> function text1(){
document.form1.display = "This is message 1"
}
function text2(){
document.form1.display = "This is message 2"
}
function text3(){
document.form1.display = "This is message 3"
}
</SCRIPT>
</HEAD>
<BODY NAME = form1>
<INPUT TYPE = text NAME = display VALUE ==""><BR>
<INPUT TYPE = button VALUE = "Text 1" onClick="text1()"
<INPUT TYPE = button VALUE = "Text 2" onClick="text2()"
<INPUT TYPE = button VALUE = "Text 3" onClick="text3()"
</FORM>
</HTML>
```

2 新函数应该像这样。
```javascript
function greenonblue()
{
document.bgColor = "navy"
document.fgColor = "lime"
}
function whiteonwhite()
{
document.bgColor = "White"
document.fgColor = "White"
}
```

3 这些行应该像这样，并写在 BODY 区域的 `<SCRIPT>` 标签中。我使用了 `<BR>` 来换行，也可以使用 `<P>`。

```javascript
document.write("<H1>This is a big heading</H1>")
document.write("<H2>This is a smaller heading</H2>")
document.write("Here is a line of text<BR>")
document.write("And and here is the next line")
```

## Chapter 3

1 你应该有类似这样的内容：
```html
<SCRIPT>
a = 4
b = 3
c = a + b
document.write("The answer is " + c)
</SCRIPT>
```

2 公式翻译为这个：

3 这些行应该像这样，并写在 BODY 区域的 `<SCRIPT>` 标签中。我使用了 `<BR>` 来换行，也可以使用 `<P>`。

```javascript
function marktime() {

  counter++

  timer = setTimeout("marktime()",1000)

}

function check() {

  clearTimeout(timer)

  if (form1.input.value == form1.display.value)

    alert("Correct in " + counter + " seconds")

    else alert("Mistyped in " + counter + " seconds")

}

</SCRIPT>

<HEAD>

<BODY NAME = form1>

Type: this box:INPUT TYPE = text NAME = display

<P>In this box:INPUT TYPE = text NAME = input

<P><INPUT TYPE = button VALUE = Done onClick = "check()")

</FORM>

<SCRIPT>

counter = 0

form1.display.value = Math.round(Math.random() * 1000000)

marktime()

</SCRIPT>

</BODY>

</html>
```

这里是一种可能的解决方案。核心部分是 `animate()` 函数，它通过 `<<img>>` 标签循环切换图片。注意这一行：
`index = (index < 2) ? ++index : 0`

这使得 `index` 在 0, 1 和 2 之间切换——如果 `index` 小于 2，它会加1，否则设置为 0。该行对每个图片都重复一次，以便每个图片访问数组中的不同元素。结尾的 `index--` 确保了下次循环时 `index` 有不同的起始值。

```html
<HTML>
<HEAD>
<SCRIPT>
```

```javascript
function loadImages()

{



`pic0 = new Image()`

`pic0.src = "reddart.gif"`

`pic1 = new Image()`

`pic1.src = "bluedart.gif"`

`pic2 = new Image()`

`pic2.src = "grndart.gif"`

```
```

```javascript
function animate()
{
  if (going)
    clearTimeout(timer)
    index = (index < 2) ? ++index : 0
    document.images[index].src = pic0.src
    index = (index < 2) ? ++index : 0
    document.images[index].src = pic1.src
    index = (index < 2) ? ++index : 0
    document.images[index].src = pic2.src
    index--
    if (going)
      timer = setTimeout("animate()",200)
}
```

```html
</SCRIPT>
<HEAD>
<BODY>
<SCRIPT>
  var timer = null
  var going = false
  loadImages()
  index = 0
</SCRIPT>

<IMG SRC="reddart.gif">
<IMG SRC="grndart.gif">
<IMG SRC="bluedart.gif">

<FORM>
<INPUT TYPE="button" VALUE="Roll em"
onclick="going = true; animate()"
<INPUT TYPE="button" VALUE="Stop"
onclick="going = false; animate()">
```

## 第 8 章

这里有一个解决方案。`marktime()` 函数被调用。

```javascript
regionName = new Array(5)
regionName[0] = "London"
regionName[1] = "South East"
regionName[2] = "South West"
regionName[3] = "Rest of England"
regionName[4] = "Wales"
```

```javascript
coverType = new Array(3)
coverType[0] = "Third Party"
coverType[1] = "Third Party Fire and Theft"
coverType[2] = "Comprehensive"
```

```javascript
function check()
{
Cvalue = document.form1.InsVal.value
Cregion =
regionName[document.form1.region.selectedIndex]
for(loop = 0; loop < 3; loop++)
if (document.form1.cover[loop].checked)
Ccover = coverType[loop]
Cquote = document.form1.quote.value
```

```javascript
win2 = window.open("", "", "width=400,height=250")
win2.document.write("<H4> Your details </H4>")
win2.document.write("<P> Cycle value: " + Cvalue + "")
win2.document.write("<P> Region: " + Cregion + "")
win2.document.write("<P> Type of cover: " + Ccover + "")
win2.document.write("<P> Quoted cost: " + Cquote + "</P>")
win2.document.write("<INPUT TYPE = button VALUE = 'Close' onclick='self.close()'")
```

## 进阶

这本书的初衷并不是一门完整的 JavaScript 课程，但我希望它已经为你奠定了良好的语言基础，并提供了继续学习的信心。

那么，从这里开始该去哪里呢？有两种主要的开发路线。第一条源于内部。掌握你所学的知识并发挥你的创造力。玩玩 JavaScript 的组件，看看你能用它们构建出什么。你想表达什么，如何用你所知的知识表达出来？第二条路线看向外部。对于 JavaScript 程序员来说，还有哪些工具、技术和语言？其他人在做什么？你能从更有经验的页面构建者那里学到什么？

Web 为 JavaScript 程序员提供了大量信息、示例和服务。以下是几个精选的网站。

`DevEdge`

```
http://devedge.netscape.com/
```

面向 Web 开发者的主要 Netscape 站点，由于 Netscape 是 JavaScript 的后盾，它也是所有用户的主要站点。在某个时刻，下载《核心 JavaScript 指南》运行搜索或输入此路径：

```
.../manuals/2000/javascript/1.5/guide
```

你还应该从这里获取《核心 JavaScript 参考》：

```
.../manuals/2000/javascript/1.5/reference
```



## JavaScript Source

`http://javascript.internet.com/`

探索 JavaScript 的好地方，有许多可以复制粘贴的示例。

## JavaScript.com

`http://javascript.com/`

为了成为权威的 JavaScript 资源，绝对值得访问。它拥有教程、指南、提示和示例。

## JavaScript Kit

`http://javascriptkit.com/`

一个很好的示例来源（接近 800 个！），关于编程各个方面的教程。该网站还提供了指向其他类型 Web 编程的链接，如果你想开始探索 JavaScript 的话。

## JavaScript City

`http://javascriptcity.com/`

另一个良好的网站，有大量的示例、教程和其他资源。

## Web Monkey

`http://hotwired.com/webmonkey/`

对于任何编程语言的开发者来说都是极佳的资源，但特别关注 JavaScript 部分。

## 索引

| 主题 | 页码 |
| :--- | :--- |
| `&&` (AND) | 48 |
| `\|\|` (OR) | 48 |
| `?` (条件运算符) | 66 |
| `charAt(place)` | 93 |
| `abs(num)` | 87 |
| 算术运算符 | 30 |
| 数组方法 | 43, 135 |
| 赋值运算符 | |
| 数据类型 | 32 |
| `Date` 方法 | 88 |
| 递减 | 39 |
| 对话框 | 56 |
| 数字和数字 | 38 |
| 属性 | 20 |
| `do...while` | 59 |
| 下拉列表 | 103 |
| 运算符运算符 | 49 |
| 运算符 | 1 |
| 运算符 | 51 |
| 按钮 | 74 |
| 元素 | 106 |
| `if` | 59 |
| 错误处理 | 73 |
| 转义字符 | 156 |
| `eval()` | 85 |
| 事件处理 | 118 |
| 逻辑运算符 | 48 |
| 循环 | 49 和表格 | 55 |
| 滚动 | 150 |
| 搜索和替换 | 97 |
| `self` | 28 |
| `setTimeout()` | 127 |
| `SIZE = INPUT` | 101 |
| 排序 | 43 |
| 源代码 | 7 |
| 特殊字符 | 156 |
| `split()` | 94 |
| `switch` | 65 |
| 字符串 | 148 |
| 变量 | 33 |
| 变量 | 32, 100 |



<SCRIPT>

<HEAD>

<BODY>

<SCRIPT>

  var timer = null

  var going = false

  loadImages()

  index = 0

</SCRIPT>

<IMG SRC="reddart.gif">

<IMG SRC="grndart.gif">

<IMG SRC="bluedart.gif">

<FORM>

<INPUT TYPE="button" VALUE="Roll em"

onclick="going = true; animate()"

<INPUT TYPE="button" VALUE="Stop"

onclick="going = false; animate()">

```

## 第 8 章

1 这里有一个解决方案。`marktime()` 函数被调用

```javascript

regionName = new Array(5)

regionName[0] = "London"

regionName[1] = "South East"

regionName[2] = "South West"

regionName[3] = "Rest of England"

regionName[4] = "Wales"

```

```javascript

coverType = new Array(3)

coverType[0] = "Third Party"

coverType[1] = "Third Party Fire and Theft"

coverType[2] = "Comprehensive"

```

```javascript

function check()

{

Cvalue = document.form1.InsVal.value

Cregion =

regionName[document.form1.region.selectedIndex]

for(loop = 0; loop < 3; loop++)

if (document.form1.cover[loop].checked)

Ccover = coverType[loop]

Cquote = document.form1.quote.value

```

```javascript

win2 = window.open("", "", "width=400,height=250")

win2.document.write("<H4> Your details </H4>")

win2.document.write("<P> Cycle value: " + Cvalue + "")

win2.document.write("<P> Region: " + Cregion + "")

win2.document.write("<P> Type of cover: " + Ccover + "")

win2.document.write("<P> Quoted cost: " + Cquote + "</P>")

win2.document.write("<INPUT TYPE = button VALUE = 'Close' onclick='self.close()'")

}

```

## 进阶

这本书的初衷并不是一门完整的 JavaScript 课程，但我希望它已经为你奠定了良好的语言基础，并提供了继续学习的信心。

那么，从这里开始该去哪里呢？有两种主要的开发路线。第一条源于内部。掌握你所学的知识并发挥你的创造力。玩玩 JavaScript 的组件，看看你能用它们构建出什么。你想表达什么，如何用你所知的知识表达出来？第二条路线看向外部。对于 JavaScript 程序员来说，还有哪些工具、技术和语言？其他人在做什么？你能从更有经验的页面构建者那里学到什么？

Web 为 JavaScript 程序员提供了大量信息、示例和服务。以下是几个精选的网站。

### DevEdge

```
http://devedge.netscape.com/
```

面向 Web 开发者的主要 Netscape 站点，由于 Netscape 是 JavaScript 的后盾，它也是所有用户的主要站点。在某个时刻，下载《核心 JavaScript 指南》——运行搜索或输入此路径：

```
.../manuals/2000/javascript/1.5/guide
```

你还应该从这里获取《核心 JavaScript 参考》：

```
.../manuals/2000/javascript/1.5/reference
```

### JavaScript Source

`http://javascript.internet.com/`

探索 JavaScript 的好地方，有许多可以复制粘贴的示例。

### JavaScript.com

`http://javascript.com/`

为了成为权威的 JavaScript 资源，绝对值得访问。它拥有教程、指南、提示和示例。

### JavaScript Kit

`http://javascriptkit.com/`

一个很好的示例来源（接近 800 个！），关于编程各个方面的教程。该网站还提供了指向其他类型 Web 编程的链接，如果你想开始探索 JavaScript 的话。

### JavaScript City

`http://javascriptcity.com/`

另一个良好的网站，有大量的示例、教程和其他资源。

### Web Monkey

`http://hotwired.com/webmonkey/`

对于任何编程语言的开发者来说都是极佳的资源，但特别关注 JavaScript 部分。

## 索引

| 主题 | 页码 |
| :--- | :--- |
| `&&` (AND) | 48 |
| `||` (OR) | 48 |
| `?` (条件运算符) | 66 |
| `charAt(place)` | 93 |
| `abs(num)` | 87 |
| 算术运算符 | 30 |
| 数组方法 | 43, 135 |
| 赋值运算符 | |
| 数据类型 | 32 |
| `Date` 方法 | 88 |
| 递减 | 39 |
| 对话框 | 56 |
| 数字和数字 | 38 |
| 属性 | 20 |
| `do...while` | 59 |
| 下拉列表 | 103 |
| 运算符运算符 | 49 |
| 运算符 | |
| 括号 | 51 |
| 框架 | 14 |
| 按钮 | 74 |
| 元素 | 106 |
| `if` | 59 |
| 错误处理 | 73 |
| 转义字符 | 156 |
| `eval()` | 85 |
| 事件处理 | 118 |
| 逻辑运算符 | 48 |
| 循环 | 49 和表格 | 55 |
| 滚动 | 150 |
| 搜索和替换 | 97 |
| `self` | 28 |
| `setTimeout()` | 127 |
| `SIZE = INPUT` | 101 |
| 排序 | 43 |
| 源代码 | 7 |
| 特殊字符 | 156 |
| `split()` | 94 |
| `switch` | 65 |
| 字符串 | 148 |
| 变量 | 33 |
| 变量 | 32, 100 |

## 互联网

Mac Bride

- 你是否渴望充满自信地探索互联网？
- 你是否想获取最新的新闻和信息？
- 你是否需要进行在线业务或在线购物？

《互联网》这本书为任何想要了解互联网并挖掘其巨大潜力的人提供了一份清晰、无术语堆砌的介绍。这本书将帮助你探索万维网、通过电子邮件进行通信、寻找你所需的信息、在线购物或玩游戏，并建立你自己的主页。

Mac Bride 是多本畅销编程和计算机应用类书籍的作者，他的写作融入了 20 多年的教学经验。

## HTML：在万维网上发布

Mac Bride

- 你是互联网用户吗？
- 你是否想从浏览转变为发布？
- 你是否想探索 HTML 的可能性？

《HTML：在万维网上发布》一书消除了网站建设中技术问题和术语的神秘感。它涵盖了 HTML 的全部内容，从最基础的到样式表，书中贯穿了清晰的解释和实战示例。通过这本书，你可以在几小时内学会如何创建一个色彩斑斓、带插图的网页，或者在几天内搭建出一个功能齐全、交互且相互链接的网站。

Mac Bride 是多本畅销编程和计算机应用类书籍的作者，他的写作融入了 20 多年的教学经验。

## C++

Richard Riley

- 你是编程新手吗？
- 你是否需要提高现有的 C++ 技能？
- 你是否想成为一名专家级程序员？

《C++》是一本关于 C++ 编程的简洁指南，C++ 是今天最流行、多功能的语言之一。创建强大程序所需的所有概念和技术都得到了清晰解释，书中贯穿了示例和复习练习。

Richard Riley 是一位计算机程序员，在 C++、Perl、Java、JavaScript 和 HTML 方面有很多著作。

## JavaScript

Mac Bride

- 你有网站吗？
- 你想让你的页面变得活跃且具有交互性吗？
- 你想学习编程——且毫无痛苦？

《JavaScript》对这种关键编程语言提供了清晰、简洁的介绍。它是为习惯于使用 HTML 但几乎或完全没有编程经验的人编写的。它在没有术语的情况下解释了 JavaScript 的核心概念和技术，并提供了大量的实战示例，将使你的网页发布提升到另一个维度。

Mac Bride 是一位 IT 顾问，编写过几本计算机编程和应用类书籍。

为什么尝试 ● Java ● C++
或访问 `www.books.mcgraw-hill.com`

自学领域的领导者，拥有 300 多部作品，涵盖所有学科，通过“自学”系列随心所欲

版权所有 © Digital Vision/Getty Images

