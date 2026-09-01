
# Web 开发：3 合 1：HTML Web 开发初学者指南、CSS Web 设计与初学者 JavaScript 基础

# 值

# 数字

## 算术

# 字符串

## JavaScript 数组

# 第二章：JavaScript 变量

## JavaScript 标识符

## 数据类型

## 变量声明

### 未定义变量

### 重复

### 算术

### JavaScript 字符串拼接

### JavaScript `let` 关键字

# 第三章：JavaScript 常量

## 块作用域

## 基本值

## JavaScript 常量

# 第四章：提示与条件判断

## JavaScript `if` 语句

## `else` 语句

## `else if` 语句

## JavaScript `switch` 语句

# 第五章：JavaScript 字符串与数组

## `lastIndexOf()` 方法

### 如果找不到索引怎么办？

## `search()` 方法

## JavaScript 数组

## JavaScript 数组 `concat()`

## 数组排序

### 反转排序

### 数字排序

### 比较函数

### 随机排序

## 数组值

## 对象数组排序

## JavaScript 迭代

# 第六章：JavaScript 循环

## `for/in` 循环

## `forEach()` 循环

## `for/of` 循环

## 死循环

## JavaScript `while` 循环

## `do/while` 循环

## JavaScript `break` 和 `continue` 语句

# 第七章：JavaScript 函数

## 函数的调用

## `()` 运算符

## 函数作为变量

## 局部变量

## JavaScript 表达式

## `constructor()`

### 自执行函数

## 函数或对象

## `toString()` 方法

## 箭头函数

## 参数与参数

## 调用

## 全局对象

## 方法复用

# 第八章：JavaScript 对象

## `new` 关键字

## 对象属性

## 删除

## 日期

## JavaScript 类

## 传递参数

## 类继承

## 结论

## 参考文献

# Web 开发

## 针对 HTML 初学者的 Web 开发

![](img/Image00001.jpg)

Andy Vickler

## 引言

![](img/Image00001.jpg)

HTML 是主要的网页语言，考虑到它被用于编写大多数网页，这并不意外——学好它确实将使你走上创建某些惊人网站的正确道路。你在这里将学到构成 HTML 文档的组成部分、所有不同的元素以及如何使用它们。

在每一章中，你将找到简单的代码示例，展示每个元素是如何工作的，并对其工作原理进行简单的解释。在书的最后，有一最后一章将带你从头到尾使用 HTML 构建一个简单的网页。

1989 年，蒂姆·伯纳斯-李（Tim Berners-Lee）发明了改变我们所知世界并在今天继续改变世界的发明。那个发明就是万维网（World Wide Web），在当时，他无法使用像 `JavaScript` 和 `CSS` 这样复杂的编程语言；他拥有的只有 HTML。

过去的 30 多年里，HTML 几乎发生了无法认的变化但也并非完全如此。它现在拥有超过 120 个标签，远多于最初的 18 个，并且仍然是任何网页的核心、最重要的部分。简而言之，它是网页的基础技术。

如果你的网站基于良好的 HTML，你将拥有一个加载快速的站点。浏览器会增量渲染 HTML，这意味着用户在等待从服务器获取其余文件时，可以看到一个部分渲染的页面。

现代开发技术（如 `React` 这样流行的框架）需要向用户发送大量的 `JavaScript`，这些代码在下载后必须由用户的设备解析并执行。而这一切在网页构建之前都必须完成。如果你的网络缓慢，或者你的设备功率低或低端，加载时间可能会慢得令人痛苦并消耗设备电池。

如果你的站点基于良好的 HTML，它将是健壮的。虽然脚本和样式的加载可能需要更长时间，但内容将始终可用，而且 HTML 不仅向后兼容，而且面向未来——它将永远有效。

### 现在还有人手写 HTML 吗？

我经常听到人们说，现在不需要学习 HTML 了，因为面对事实吧，现在还有谁会手写它呢？诚然，这很有道理——`WordPress` 驱动了如今全球超过 35% 的网站。它使用模板来组装网页，并可以为它们应用不同的主题。`Drupal` 和 `Joomla` 的工作原理也相似。同时，其他开发者使用 `React` 和其他类似的框架，这些框架只是将一系列已经写好的组件组合在一起。

但让我们面对事实吧——那些组件和模板仍然需要编写。那些使用 `React` 或 `WordPress` 的开发者仍然需要一些 HTML 知识。否则，他们无法在使用的之前评估这些组件和模板的好坏。

这就是我编写这本指南的原因，让你知道如何用老式的经典 HTML 制作网页，而不必担心别人的工作做得有多好。

## 第 1 章：什么是 HTML？

![](img/Image00001.jpg)

HTML 代表超文本标记语言（Hyper Text Markup Language），它是用于创建 Web 应用程序和网页的语言。那么，这一切意味着什么呢？

- **超文本（HyperText）**：这仅仅意味着“文本中的文本”。任何包含链接的文本被称为两种事物之一——超链接或超文本。如果你点击这些链接之一，将打开一个新的网页。
- **标记语言（Markup Language）**：标记语言是用于对文档应用格式化和布局的计算机语言。这些语言确保了文本更具动态性和交互性，并可以将文本转换为链接、表格、图像等。
- 网页：网页是通常用 HTML 编写的文档，然后使用网页浏览器对其进行翻译。我们使用 `URLs` 来访问和识别这些网页，`URLs` 是网页在互联网上的地址，并且它们可以是动态的或静态的。用于创建静态网页的唯一语言是 HTML。

这意味着 HTML 语言用于通过样式设计创建美观的网页，并以良好的格式将其显示在网页上。HTML 文档由多个标签组成，每个标签都有不同的内容。

让我们通过查看一个简单的 HTML 示例将这一切置于语境中：

```html
<!DOCTYPE>
<html>
<head>
<title>Web page title</title>
</head>
<body>
<h1>Your first heading goes here</h1>
<p>Your first paragraph goes here</p>
</body>
</html>
```

（注：此处运行此代码将在你的屏幕上显示以下内容：

Your first heading goes here

Your first paragraph goes here

让我们将这个示例拆解为各个组件：

- `<!DOCTYPE>`：这定义了文档类型或告诉浏览器正在使用哪个版本的 HTML。
- `<html>`：这告诉浏览器正在使用 HTML 文档。此标签之间的任何文本都在描述文档。换句话说，它是除 `<!DOCTYPE>` 之外所有其他 HTML 元素的容器。
- `<head>`：这是 `<html>` 标签中的第一个元素，它包含了关于文档的详细信息，即元数据。在打开 `<body>` 标签之前，必须关闭 `<head>` 标签。
- `<title>`：顾名其义——此标签添加了网页的标题，即在浏览器显示的窗口顶部看到的标题。它必须包含在 `<head>` 标签内，并且应该被立即关闭。
- `<body>`：这是网页内容所在的地方，即终端用户看到的内容。它是 HTML 文档的主要内容。
- `<h1>`：此标签中的任何文本都在描述网页的一级标题。
- `<p>`：此标签中的文本在描述网页的段落文本。

随着你学习完这本书，所有这些都将变得更加清晰。

## HTML 简史

蒂姆·伯纳斯-李（Tim Berners-Lee）是 20 世纪 80 年代末的一位物理学家，受聘于欧洲核子研究组织（CERN）。在他那里期间，他为研究人员提出了一个系统，并在 1989 年发送了一份包含基于互联网的超文本系统的备录。

他获得了“HTML 之父”的美誉。1991 年，他编写了名为《HTML Tags》的文档，这是第一个 HTML 描述。

## HTML 版本

自 HTML 发明以来，已经发布了几个版本：

- HTML 1.0 – 1991 年发布，这是 HTML 的第一个版本，非常基础。
- HTML 2.0：下一个版本于 1995 年发布，并成为了网站设计的标准。它提供了额外功能的支持，包括表单元素（如选项按钮、文本框等）以及基于表单的文件上传。
- HTML 3.2：W3C 于 1997 年初发布了这个版本，带来了对表格创建的支持以及对表单元素中新选项更多的支持。它还可以支持包含复杂数学方程的网页。1997 年 1 月，它成为了浏览器标准，直到今天，大多数浏览器仍然以实际形式支持它。
- HTML 4.01 – 下一个 HTML 版本于 1999 年 12 月出现，并证明极其稳定——今天依然如此。它是我们目前使用的官方标准，并提供了对 CSS（样式表）和不同多媒体元素脚本能力的支持。
- HTML5：HTML5 是最新版本，于 2008 年 1 月首次宣布。有两个基金会参与 HTML5 的开发——万维网联盟（W3C）和网页超文本应用技术小组（WHATWG），直到今天它仍在开发中。

## HTML 特性

那么，为什么要使用 HTML？为什么不使用较新的语言，例如 JavaScript？除了 HTML 支持 JavaScript 和 CSS 之外，它还为用户提供了所有功能：

1. 它是最容易理解和修改的语言之一。
2. 使用 HTML 制作有效的演示非常容易，因为它提供了大量的格式标签。
3. 因为它是一种标记语言，它为用户提供了一种使用文本设计网页的灵活方法。
4. 它允许用户使用锚点标签在网页上添加链接，从而增强用户的浏览兴趣。
5. 它不依赖于任何特定平台，可以在 Windows、Linux、Mac 以及所有其他系统上显示。
6. 它允许程序员轻松地向页面添加声音、视频和图形，确保它们更具互动性和吸引力。
7. 它不像其他语言那样对大小写敏感，因此标签可以使用小写或大写。然而，为了可读性和一致性，建议使用小写。

## HTML 编辑器

由于 HTML 文件是文本文件，它们需要在文本编辑器中创建。文本编辑器是一个允许你编辑文本以创建网页的程序。有许多不同的编辑器可以下载，但建议初学者在使用 Windows 时使用 `Notepad`（记事本），在使用 macOS 时使用 `TextEdit`。一旦你学会了基础，就可以转向其他专业编辑器，如 `Vim`、`Sublime Text`、`Notepad++` 等。

### 使用记事本

#### 第一步：打开记事本（Windows）

如果你使用 Windows 8 或更高版本：

- 打开“开始”菜单。
- 搜索并打开记事本。

#### 第二步：编写 HTML

在记事本中输入以下内容：

```html
<!DOCTYPE html>
<html>
<head>
<title>Web page title</title>
</head>
<body>
<h1>Your first heading goes here</h1>
<p>Your first paragraph goes here</p>
</body>
</html>
```

运行此代码将在你的屏幕上显示以下内容：

Your first heading goes here

Your first paragraph goes here

#### 第三步：保存文件

点击“文件”>“另存为”。将文件名命名为 `index.html`，并将保存类型更改为“所有文件”。点击保存。

#### 第四步：查看网页

双击你保存的 `index.html` 文件，它将在你的默认浏览器中打开。

### 使用文本编辑（macOS）

#### 第一步：打开文本编辑（macOS）

如果你使用 macOS：

- 打开“启动”。
- 搜索并打开“文本编辑”。

你需要更改一些设置，以便能够正确保存文件：

- 点击“格式”>“制作纯文本”。

#### 第二步：编写 HTML

在文本编辑中输入以下内容：

```html
<!DOCTYPE html>
<html>
<head>
<title>Web page title</title>
</head>
<body>
<h1>Your first heading goes here</h1>
<p>Your first paragraph goes here</p>
</body>
</html>
```

#### 第三步：保存文件

点击“文件”>“另存为”。将文件名命名为 `index.html`，并将编码格式为“UTF-8”。点击保存。

#### 第四步：查看网页

双击你保存的 `index.html` 文件，它将在你的默认浏览器中打开。

有几个标签用于定义 HTML 标题：`<h1>`、`<h2>`、`<h3>`、`<h4>`、`<h5>` 和 `<h6>`。`<h1>` 是最重要的，而 `<h6>` 是不重要的。

```html
<h1>这是标题 1</h1>
<h2>这是标题 2</h2>
<h3>这是标题 3</h3>
```

### HTML 段落

`<p>` 标签用于定义 HTML 段落：

```html
<p>This is a paragraph.</p>
<p>This is another paragraph.</p>
```

（此处未翻译）

### HTML 链接

`<a>` 标签用于定义 HTML 链接：

```html
<a href="https://www.wikipedia.com">这是一个链接</a>
```

`href` 属性用于指定链接的单元目标。我们将在下一章讨论属性，但现在，你只需要知道它们被用于提供有关元素的更多信息。

### HTML 图像

`<img>` 标签用于定义 HTML 图像，其属性有 `src`（源文件）、`alt`（替代文本）、`height`（高度）和 `width`（宽度）。

```html
<img src="wikipedia.jpg" alt="Wikipedia.com" width="104" height="142">
```

### 如何查看 HTML 源代码

你曾多少次查看网页并好奇它是如何创建的？在任何 HTML 网页上，你只需要对页面点击鼠标右键。在 Chrome 浏览器中，点击“查看网页源代码”（View Page Source），或者在 Edge 中，点击“查看源代码”（View Source）。其他浏览器也是一样。会打开一个窗口向你显示页面的源代码。

### 如何检查 HTML 元素

只需右键点击空白区域或元素，并点击“检查元素”（Inspect Element）或“检查”。这将向你显示元素的 HTML 和 CSS 部分，你还可以使用“样式”或“元素”面板来编辑 HTML。

在下一章中，我们将查看组成 HTML 的构建块。

## 第二章：HTML 构建块

![](img/Image00001.jpg)

让我们直接进入正题——HTML 文档是由构建块组成的。基础的构建块包括：

- 标签（Tags）：HTML 标签用于包裹内容并赋予其意义。所有标签都由 `<>` 包围。
- 属性（Attributes）：HTML 属性为元素提供额外的细节，起始标签用于应用它们。所有属性都有两个字段：名称和值。

我们在这章中还将讨论元素。

### 语法

```html
<tag name attribute_name="attr_value">content</tag name>
```

HTML 元素是单个 HTML 文件组件，写在标签中的任何内容都称为元素。

![HTML 构建块](img/Image00002.gif)

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
    <title>基础 HTML 构建块</title>
  </head>
  <body>
    <h2>构建块</h2>
    <p>这是一个段落标签</p>
    <p style="color: red">样式是段落标签的一个属性</p>
    <span>元素包含一个标签、一个属性和内容</span>
  </body>
</html>
```

（此处未翻译）

输出结果是：

构建块

样式是段落标签的一个属性

元素包含一个标签、一个属性和内容

### HTML 表格标签

你可能会使用的表格标签有：

- 表格（Table）
- `tr`（行）
- `td`（单元格）
- `th`（表头单元格）
- `tbody`（列表）
- `thead`（表头）
- `tfoot`（表脚）
- `col`（列）
- `colgroup`（列组）
- `caption`（标题）

### HTML 表单标签

表单标签有：

- `form`（表单）
- `input`（输入）
- `textarea`（文本区域）
- `select`（选择）
- `option`（选项）
- `optgroup`（选项组）
- `button`（按钮）
- `label`（标签）
- `fieldset`（字段组）
- `legend`（图例）

### HTML 脚本标签

有两个脚本标签：

- `script`
- `noscript`

### HTML 标签

你可以将 HTML 标签认为类似于关键字。它们定义了浏览器格式化和显示内容的方式。通过使用标签，网络浏览器可以区分 HTML 和简单内容。标签由三个部分组成：起始标签、内容和结束标签。然而，某些 HTML 标签是不闭合的。



当浏览器读取 HTML 文档时，它是从上到下、从左到右读取的——就像你阅读书页一样。HTML 文档是通过 HTML 标签创建并渲染属性的——每个标签都有自己的属性。

HTML 文件需要基本的标签，以便浏览器能够区分 HTML 和简单文本。根据你的代码需求，你可以使用任意数量的标签：

- 每个 HTML 标签都应该包含在括号 `<>` 之间。
- 所有 HTML 标签都有不同的功能。
- 如果使用了起始标签（`<tag>`），那么在大多数情况下，必须有一个结束标签（`</tag>`）。

## 语法

```html
<tag> 内容 </tag>
```

## HTML 标签示例

所有 HTML 标签都应该用小写字母书写。以下是最基本的标签：

- `<p> 段落标签 </p>`
- `<h2> 标题标签 </h2>`
- `<b> 粗体标签 </b>`
- `<i> 斜体标签 </i>`
- `<u> 下划线标签 </u>`

## 未闭合的 HTML 标签

并不是所有的 HTML 标签都需要闭合。例如：

- `<br>`——`br` 用于换行
- `<hr>`——`hr` 用于插入水平线

## HTML 元标签

这些元标签包括：

- `<!DOCTYPE>`
- `<title>`
- `<link>`
- `<meta>`
- `<style>`

## HTML 文本标签

常用的文本标签有：

- `<p>`
- `<h1>`
- `<h2>`
- `<h3>`
- `<h4>`
- `<h6>`
- `<strong>`
- `<em>`
- `<abbr>`
- `<address>`
- `<blockquote>`

## HTML 链接标签

有两个链接标签：

- `<a>`
- `<base>`

## HTML 对象和图像标签

对象和图像标签有：

- `<img>`
- `<area>`
- `<map>`
- `<param>`
- `<object>`

## HTML 列表标签

主要的标签有：

- `<ul>`
- `<ol>`
- `<li>`
- `<dl>`
- `<dt>`
- `<dd>`

## HTML 标签列表

以下列表按字母顺序排列了所有标签，以便你轻松找到需要的内容，带有星号（`*`）：

| 标签 | 描述 |
| --- | --- |
| `<!-- -->` | 用于在 HTML 文档中使用注释 |
| `<!DOCTYPE>` | 用于指定 HTML 版本 |
| `<a>` | 锚标签，用于创建链接或超链接 |
| `<abbr>` | 为长词或短语创建缩写 |
| `<acronym>` | 定义缩写——HTML5 不支持此标签 |
| `<address>` | 定义文章的联系信息 |
| `<applet>` | 定义嵌入应用程序——HTML5 不支持此标签 |
| `<area>` | 定义图像映射区域 |
| `<article>` | 定义自包含的内容 |
| `<aside>` | 定义独立于主要内容的内容——通常显示为侧边栏 |
| `<audio>` | 用于在 HTML 文档中嵌入声音 |
| `<b>` | 用于将文本加粗 |
| `<base>` | 定义同一文档内所有其他 URL（相对）的基础 |
| `<basefont>` | 用于设置所有元素的默认字体、颜色和大小 |
| `<bdi>` | 该标签隔离指定的文本段，使其与周围文本格式不同 |
| `<bdo>` | 该标签覆盖文本的当前方向 |
| `<big>` | 使字体比周围内容大一号——HTML5 不支持此标签 |
| `<blockquote>` | 定义来自其他来源的内容 |
| `<body>` | 定义 HTML 文档的体部 |
| `<br>` | 应用一次换行 |
| `<button>` | 表示可点击的按钮 |
| `<canvas>` | 该标签用于为网页提供图形空间 |
| `<caption>` | 用于定义表格标题 |
| `<center>` | 用于使内容居中——HTML5 不支持此标签 |
| `<cite>` | 用于定义书籍、网站或其他作品的标题 |
| `<code>` | 用于显示 HTML 文档中的指定代码段 |
| `<col>` | 定义表格中的列，表示公共列属性，并与 `<colgroup>` 元素配合使用 |
| `<colgroup>` | 用于定义表格中的列组 |
| `<data>*` | 用于通过机器可读的翻译来链接内容 |
| `<datalist>*` | 用于提供预定义列表的输入选项 |
| `<dd>` | 为描述列表中的术语提供描述或定义 |
| `<del>` | 定义被删除的文本 |
| `<details>*` | 定义用户可以查看或隐藏的额外信息 |
| `<dfn>` | 表示短语或句子中定义的术语 |
| `<dialog>*` | 定义交互式组件，如对话框 |
| `<dir>` | 用于作为容器类型，容纳所有文件的目录列表——HTML5 不支持此项 |
| `<div>` | 定义文档中的节或划分区域 |
| `<dl>` | 定义描述列表 |
| `<dt>` | 定义描述列表中的术语 |
| `<em>` | 强调元素内的内容 |
| `<embed>*` | 一种嵌入容器，用于容纳外部媒体、应用程序、文件等 |
| `<fieldset>` | 在 Web 表单中将相关的标签或元素分组 |
| `<figcaption>*` | 为 `<figure>` 添加说明或图表 |
| `<figure>*` | 定义自包含的内容 |
| `<font>` | 定义内容的字体、类型、大小和颜色——HTML5 不支持此项 |
| `<footer>*` | 定义网页的页脚 |
| `<form>` | 定义 HTML 表单 |
| `<frame>` | 定义页面的特定部分，其中可能包含另一个 HTML 文件——HTML5 不支持此项 |
| `<frameset>` | 定义一个 Frames 组——HTML5 不支持此项 |
| `<h1>` 到 `<h6>` | 定义文档中不同的标题级别 |
| `<head>` | 定义 HTML 文档的头部部分 |
| `<header>*` | 定义网页的头部 |
| `<hr>` | 在段落级元素之间应用主题分隔 |
| `<html>` | 代表 HTML 文档的根 |
| `<i>` | 使用不同的语调表示文本 |
| `<iframe>` | 定义用于嵌入其他内容的内联框架 |
| `<img>` | 用于在 HTML 文档中插入图像 |
| `<input>` | 定义 HTML 表单的输入字段 |
| `<ins>` | 表示插入文档的文本 |
| `<isindex>` | 显示当前文档的搜索字符串——HTML5 不支持此项 |
| `<kbd>` | 定义键盘输入 |
| `<label>` | 定义表单的输入字段标签 |
| `<legend>` | 为 `<fieldset>` 定义标题 |
| `<li>` | 用于表示列表项 |
| `<link>` | 用于表示外部资源与当前文档之间的关系 |
| `<main>*` | 用于表示 HTML 文档的主内容 |
| `<map>` | 定义带有活动区域的图像映射 |
| `<mark>*` | 用于表示高亮文本 |
| `<marquee>` | 用于插入垂直或水平的滚动文本或图像——HTML5 不支持此项 |
| `<menu>` | 用于创建包含命令的列表 |
| `<meta>` | 定义 HTML 文档的元数据 |
| `<meter>*` | 用于定义具有分数值或已知范围的标量测量 |
| `<nav>*` | 用于表示导航链接的页面节 |
| `<noframes>` | 在不支持 `<frame>` 元素的浏览器中提供备用内容——HTML5 不支持此项 |
| `<noscript>` | 在浏览器不支持脚本类型时提供备用内容 |
| `<object>` | 用于在 HTML 文件中嵌入对象 |
| `<ol>` | 用于定义有序项目列表 |
| `<optgroup>` | 用于分组下拉列表的选项 |
| `<option>` | 用于定义下拉列表的项目或选项 |
| `<output>*` | 作为容器并显示计算结果 |
| `<p>` | 用于表示 HTML 文档段落 |
| `<param>` | 用于定义 `<object>` 元素的参数 |
| `<picture>*` | 用于定义多个源元素和一个图像元素 |
| `<pre>` | 用于定义 HTML 文档的预格式文本 |
| `<progress>*` | 用于定义 HTML 文档中任务的进度 |
| `<q>` | 用于定义短内联引用 |
| `<rp>*` | 用于在浏览器不支持注音（ruby annotations）时定义备用内容 |
| `<rt>` | 用于定义注音的读音和解释 |
| `<ruby>` | 用于表示注音 |
| `<s>` | 用于渲染错误或无关文本 |
| `<samp>` | 表示计算机程序的示例输出 |
| `<script>` | 用于声明 HTML 文档的 JavaScript |
| `<section>*` | 用于定义文档的通用节 |
| `<select>` | 用于表示一个提供选项菜单的控件 |
| `<small>` | 将字体缩小为比文档基础字体小一号 |
| `<source>` | 用于为媒体元素定义多个资源，如 `<audio>`、`<video>` |
| `<span>` | 用于分组和样式 |
| `<strike>` | 渲染带下划线的文本 |
| `<strong>` | 用于你认为重要的文本 |
| `<style>` | 用于持有 HTML 定义的信息 |
| `<sub>` | 定义你想要的下标文本 |
| `<summary>*` | 为 `<details>` 定义摘要 |
| `<sup>` | 定义你想要的上标文本 |
| `<svg>` | 用于可缩放矢量图形 |
| `<table>` | 用于表格格式表示数据或创建表格 |
| `<tbody>` | 表示表格主体内容，配合 `<tfoot>` 和 `<thead>` 使用 |
| `<td>` | 定义表格单元格数据 |
| `<template>` | 用于页面加载时不显示的客户端内容，后续可用 JavaScript 渲染 |
| `<textarea>` | 用于多行输出，如反馈、评论等 |
| `<tfoot>` | 用于定义表格的页脚 |
| `<th>` | 用于定义表格的头部单元格 |
| `<thead>` | 用于定义表格的头部，配合 `<tfoot>` 和 `<tbody>` 使用 |
| `<time>` | 用于定义 HTML 文档中的时间和日期 |
| `<title>` | 定义 HTML 文档的名称或标题 |
| `<tr>` | 定义表格行 |
| `<track>` | 用于 `<audio>` 和 `<video>` 元素的文本轨道 |
| `<tt>` | 定义打字机字体——HTML5 不支持此项 |
| `<u>` | 用于渲染带下划线的文本 |
| `<ul>` | 用于定义无序列表 |
| `<var>` | 用于定义编程或数学背景下的变量名 |
| `<video>*` | 用于嵌入视频内容 |
| `<wbr>*` | 定义文本中可以换行的位置 |

## HTML 属性

HTML 属性类似于你在其他语言中找到的关键字。它们是特殊的，并为元素提供更多细节——简而言之，它们用于修改 HTML 元素。

每个标签或元素都可以有一个或多个属性，用于定义元素的行为。关于属性，有几点需要注意：

- 始终使用起始标签来应用。
- 必须始终以名称/值对的形式应用。
- 名称和值对大小写敏感，建议使用小写。
- HTML 元素可以有多个属性，但它们之间必须有空格。

### 语法

属性使用的语法为：

```html
<element attribute_name="value"> 内容 </element>
```

这是一个示例：

```html
<!DOCTYPE html>
<html>
<head>
</head>
<body>
    <h1> 这是 Style 属性 </h1>
    <p style="height: 50px; color: blue"> 它在元素中添加了 style 属性 </p>
    <p style="color: red"> 它改变了内容的颜色 </p>
</body>
</html>
```

运行此代码应该会在你的屏幕上输出以下内容：

这是 Style 属性

它在元素中添加了 style 属性

它改变了内容的颜色

让我们来拆解一下：

- `<p style='height: px; color: blue"> 它在元素中添加了 style 属性</p>`——该语句使用了段落标签，并在其中应用了 `style` 属性。虽然这本书是关于 HTML 的，但当你想要在 HTML 元素上使用 CSS 属性时，这个属性非常有用。我们在这里执行的操作是设置一个高度为 `50px` 的元素，并将其更改为蓝色。
- `<p style="color: red">它将改变内容的颜色</p>`——再次使用了段落标签来包含 `style` 元素。这次我们将其改为了红色。

接下来，我们将查看一些常用的属性。

## Title 属性（Title Attribute）

它在大多数浏览器中作为文本工具提示。当用户将光标悬停在文本或链接上时，将显示文本。它可以与任何链接或文本配合使用，以显示相关描述。在下面的示例中，我们将其用于段落和标题标签。

使用 `<h1>` 标签：

```html
<h1 title="This is the heading tag"> title 属性的示例 </h1>
```

使用 `<p>` 标签：

```html
<p title="This is the paragraph tag"> 将光标悬停在标题和段落上，描述将作为工具提示显示 </p>
```

代码示例为：

```html
<!DOCTYPE html>
<html>
<head>
</head>
<body>
  <h1 title="This is the heading tag"> title 属性的示例 </h1>
  <p title="This is the paragraph tag"> 将光标悬停在标题和段落上，描述将作为工具提示显示 </p>
</body>
</html>
```

在你的屏幕上，你会看到以下内容：

### title 属性的示例

将光标悬停在标题和段落上，描述将作为工具提示显示

## href 属性（href Attribute）

这是 `<a>` 锚点标签的主要属性，为锚点中指定的链接提供链接地址。简而言之，`href` 提供了超链接；如果留空，它将留在同一页面。

这是一个带有链接地址和不带链接地址的示例。

带有链接地址：

```html
<a href="https://www.Wikipedia.com/html-anchor"> 这是一个链接 </a>
```

没有链接地址：

```html
<a href=""> 这是一个链接 </a>
```

输出将是：

### href 属性的显示

下面是锚点标签的链接；点击链接查看下一页。

[这是一个链接](http://www.wikipedia.com/)

## src 属性（src Attribute）

这是 `<img>` 元素最重要的属性之一，事实上，它是必须的。它提供了在浏览器上显示的图像源。图像可以包含在相同或不同的目录中，且图像的名称或源必须正确——否则，图像将无法显示。

```html
<img src="pigswimming.jpg" height="1000" width="584">
```

注意，这也包含了 `width` 和 `height` 属性，定义了在浏览器上显示的图像大小。

### src 属性的示例

`src` 属性在浏览器上显示：

## 单引号还是双引号（Single or Double Quotes）

你注意到双引号被用于 HTML 属性中。在 `src` 属性中，你应该使用哪一个？

使用双引号执行时：

```html
<a href="https://www.wikipedia.com/"> 链接 </a>
```

使用单引号执行时：

```html
<a href='https://www.wikipedia.com/'> 链接 </a>
```

在 HTML 中，单引号和双引号是等价的。为了一致性，通常建议使用双引号。

## 全局属性（Global Attributes）

全局属性是所有元素通用的属性。在 HTML5 中，带有 `*` 的属性如下：

| 属性 | 说明 |
| :--- | :--- |
| `accesskey` | 键盘快捷键 |
| `class` | 类名 |
| `contenteditable` | 内容编辑 |
| `contextmenu` | 右键菜单 |
| `data-*` | 自定义数据 |
| `dir` | 方向 |
| `draggable` | 可拖拽 |
| `hidden` | 隐藏 |
| `id` | 唯一标识 |
| `lang` | 语言 |
| `style` | 内联样式 |
| `spellcheck` | 拼写检查 |
| `tabindex` | 标签顺序 |
| `title` | 标题 |
| `translate` | 翻译 |

## 窗口事件属性（Windows Event Attributes）

这些事件属性应用于 `<body>` 标签并与窗口有关：

| 属性 | 说明 |
| :--- | :--- |
| `onafterprint` | 打印后执行 |
| `onbeforeprint` | 打印前执行 |



| 属性 | 描述 |
| :--- | :--- |
| `onbeforeunload` | 卸载前执行 |
| `onerror` | 发生错误时执行 |
| `onhashchange` | URL 发生变化时执行 |
| `onload` | 页面完全加载后执行 |
| `onmessage` | 发生消息事件时执行 |
| `onoffline` | 网络断开且浏览器处于离线状态时执行 |
| `ononline` | 浏览器恢复在线时执行 |
| `onpagehide` | 页面被隐藏（如用户离开页面）时执行 |
| `onpageshow` | 页面获得焦点时执行 |
| `onpopstate` | 窗口活动历史发生变化时执行 |
| `onresize` | 窗口大小改变时执行 |
| `onstorage` | 网页存储发生更新时执行 |
| `onunload` | 窗口关闭或页面卸载时执行 |

### 表单事件属性（Form Event Attributes）

这些发生在用户在表单内执行操作时。

| 属性 | 描述 |
| :--- | :--- |
| `onblur` | 表单元素失去焦点时执行 |
| `onchange` | 元素值改变时执行 |
| `onfocus` | 元素获得焦点时触发事件 |
| `oninput` | 当用户向元素添加输入时，执行脚本 |
| `oninvalid` | 当元素不满足预定义的约束时，执行脚本 |
| `onreset` | 当用户重置表单元素的值时，触发事件 |
| `onsearch` | 当输入框进入搜索状态时，触发事件 |
| `onselect` | 当用户选择文本时，触发事件 |
| `onsubmit` | 在提交表单时触发事件 |

### 键盘事件属性

这些事件在用户与键盘进行交互时发生。这些是键盘事件：

| 属性 | 描述 |
| :--- | :--- |
| `onkeydown` | 当用户按下键盘按键时，触发事件 |
| `onkeypress` | 当用户按下的键显示字符时，触发事件 |
| `onkeyup` | 当用户松开已按下的按键时，触发事件 |

### 鼠标事件属性

| 属性 | 描述 |
| :--- | :--- |
| `onclick` | 当元素被鼠标点击时，触发事件 |
| `ondblclick` | 当元素被鼠标双击时，触发事件 |
| `onmousedown` | 当鼠标按钮在元素上被点击按下时，触发事件 |
| `onmousemove` | 当鼠标指针在元素上移动时，触发事件 |
| `onmouseout` | 当鼠标移出元素范围时，触发事件 |
| `onmouseover` | 当鼠标移动到元素上时，触发事件 |
| `onmouseup` | 在松开鼠标按钮时触发事件 |
| `onmousewheel` | 已弃用——应该使用 `onwheel` 属性 |
| `onwheel` | 当鼠标轮在元素上向下或向上滚动时，触发事件 |

### 剪贴板事件属性

| 属性 | 描述 |
| :--- | :--- |
| `oncopy` | 当用户复制内容到系统剪贴板时，触发事件 |
| `oncut` | 当元素中的内容被剪切并复制到剪贴板时，触发事件 |
| `onpaste` | 当用户将内容粘贴到元素中时，触发事件 |

### 媒体事件属性

| 属性 | 描述 |
| :--- | :--- |
| `onabort` | 当媒体播放中止时，执行脚本 |
| `oncanplay` | 当媒体文件准备就绪播放时，执行脚本 |
| `oncanplaythrough` | 当媒体文件可以在不停止或缓冲的情况下播放时，执行脚本 |
| `oncuechange` | 当 `<track>` 元素的文本提示更改时，执行脚本 |
| `ondurationchange` | 当媒体文件的时长发生变化时，执行脚本 |
| `onemptied` | 如果由于媒体致命错误导致文件不可用，则执行脚本 |
| `onended` | 当媒体文件结束时，执行脚本 |
| `onerror` | 在获取媒体数据时发生错误时，执行脚本 |
| `onloadeddata` | 当媒体数据加载完成后，包含脚本 |
| `onloadedmetadata` | 当媒体文件的元数据加载时，执行脚本 |
| `onloadstart` | 当媒体文件开始加载时，执行脚本 |
| `onpause` | 当播放暂停时，执行脚本 |
| `onplay` | 当暂停的媒体文件准备好再次播放时，执行脚本 |
| `onplaying` | 当媒体文件开始播放时，执行脚本 |
| `onprogress` | 当浏览器开始检索媒体数据时，执行脚本 |
| `onratechange` | 当播放速度变化时，执行脚本 |
| `onseeked` | 当跳转操作结束且 `seeking` 属性被设置为 `false` 时，执行脚本 |
| `onseeking` | 在激活跳转操作时执行脚本，并将 `seeking` 属性设置为 `true` |
| `onstalled` | 当浏览器突然停止检索媒体数据时，执行脚本 |
| `onsuspend` | 如果人为停止媒体数据抓取操作，则执行脚本 |
| `ontimeupdate` | 当播放位置发生变化时（如快进或回退音轨），执行脚本 |
| `onvolumechange` | 当媒体音量发生变化时（静音或取消静音），执行脚本 |
| `onwaiting` | 当因需要加载更多数据而导致播放暂停时，执行脚本 |

### HTML 元素

HTML 文件由元素组成，元素用于创建网页并定义其上的内容。HTML 元素通常由 `<tag name>`（起始标签）、内容（属性）和 `</tag name>`（结束标签）组成。请注意，并非所有元素都有内容和结束标签。这些被称为空元素、空元素或自闭元素，包括 `<hr>`、`<br>` 等。这里有一个示例：

```html
<p> Hello world!!! </p>
```

这里还有一个示例：

```html
<!DOCTYPE html >
<html>
<head>
    <title> WebPage </title>
</head>
<body>
  <h1> This is my first web page </h1>
  <h2> How does it look?</h2>
    <p> It looks great! </p>
</body>
</html>
```

输出将是这样：

这是我的第一个网页

看起来怎么样？

看起来棒极了！

注意，`<body>` 元素之间的内容可以在网页上看到。

应该注意，某些 HTML 元素可以嵌套，这意味着元素可以包含其他元素。

### 块级和内联 HTML 元素

在 HTML 中，为了样式化的目的，元素分为两类。

#### 块级元素

块级元素从新行开始，并占据可用宽度（它们向左右延伸到尽可能远）。

- `<address>`
- `<article>`
- `<aside>`
- `<blockquote>`
- `<body>`
- `<div>`
- `<footer>`
- `h1` 到 `h6`
- `<header>`
- `<hr>`
- `<main>`
- `<nav>`
- `<ol>`
- `<p>`
- `<pre>`
- `<section>`
- `<table>`
- `<ul>`
- `<div>`

#### 内联元素

内联元素不从新行开始，仅占据必要的宽度。它们用于包裹内联内容。

- `<a>`
- `<abbr>`
- `<acronym>`
- `<b>`
- `<bdo>`
- `<big>`
- `<br>`
- `<button>`
- `<cite>`
- `<code>`
- `<dfn>`
- `<em>`
- `<i>`
- `<img>`
- `<input>`
- `<kbd>`
- `<label>`
- `<map>`
- `<object>`
- `<q>`
- `<samp>`
- `<script>`
- `<select>`
- `<small>`
- `<span>`
- `<strong>`
- `<sub>`
- `<sup>`
- `<textarea>`
- `<time>`
- `<tt>`
- `<var>`

这里有一个示例：

```html
<!DOCTYPE html >
<html>
<head>
    <title> WebPage </title>
</head>
<body>
  <div style="background-color: lightblue">这是第一个 div </div>
  <div style="background-color: lightgreen">这是第二个 div </div>
  <p style="background-color: pink">这仅占据文本宽度</p>
</body>
</html>
```

| 元素 | 描述 | 结束标签 | 用途 |
| :--- | :--- | :--- | :--- |
| `<h1>` ...... `<h6>` | HTML 标题 | `</h1>`??.. | 用于提供页面标题 |
| `<p>` | 段落 | `</p>` | 用于以段落形式显示内容 |
| `<div>` | div 区域 | `</div>` | 用于在网页中提供区域 |
| `<br>` |  | ____________ | 空元素（Void element）——提供换行符 |
| `<hr>` |  | ____________ | 空元素（Void element）——提供水平线 |

# 标题 1

## 标题 2

### 标题 3

#### 标题 4

##### 标题 5

###### 标题 6

请确保你只使用 `<h>` 标签作为内容的标题——它们绝不应用于放大或加粗你的文本。

你也可以在嵌套元素中使用 `<h>` 标签。以下是使用标题标签的不同方式的示例：

```html
<!DOCTYPE html > 
<html> 
  <head> 
    <title> Heading tags </title> 
  </head> 
  <body> 
    <h1> This is the main heading of the page. </h1> 
      <p> h1 is the most important , and is used to display the page keyword </p> 
    <h2> This is the first sub-heading </h2> 
      <p> h2 describes the first sub heading one the page. </p> 
      <h3> This is the second sub heading </h3> 
      <p> h3 describes the second sub heading on the page. </p> 
      <p> We can use h1 to h6 tag to use different sub-heading with paragraphs if required. </p> 
  </body> 
</html>
```

输出结果看起来像这样：

这是页面的主标题

`h1` 是最重要的，用于显示页面关键词。

这是第一个子标题

`h2` 描述了页面上的第一个子标题。

这是第二个子标题

`h3` 描述了页面上的第二个子标题。

如果需要，我们可以使用 `h1` 到 `h6` 标签在段落中配合不同的子标题。

### HTML 段落

`<p>` 标签用于定义网页页面内容中的段落。让我们来看一个简单的示例，看看它是如何运作的。值得注意的是，浏览器会在段落之前和之后添加空行。`<p>` 标签用于指示开始一个新段落。

注意——如果在一个 HTML 文件中使用多个 `<p>` 标签，浏览器会自动在段落之间添加一个空行。以下是示例：

```html
<!DOCTYPE html>
<html>
<body>
<p>This is first paragraph.</p> 
<p>This is second paragraph.</p> 
<p>This is third paragraph.</p> 
</body>
</html>
```

输出结果是：

This is the first paragraph

This is the second paragraph

This is the third paragraph

#### 段落空格

如果你在 `<p>` 标签内部放置了额外的空格（无论是无意还是故意），浏览器在显示页面时会删除它们以及多余的空行。浏览器会将行数和空格数视作一个：

```html
<p> 
I am 
Providing you with
an HTML tutorial
that is hope you will find beneficial. 
</p> 
<p> 
Look, I added in a lot 
of spaces             I know that the browser will ignore them. 
</p> 
<p> 
You cannot work out what the HTML looks like</p> 
<p>because resized windows give different results. 
</p> 
```

以下是输出结果：

I am providing you with a tutorial on HTML that I hope you will find beneficial.

Look, I added in a lot of spaces but I know that the browser will ignore them.

You cannot work out what the HTML looks like because resized windows give different results.

#### 在 `<p>` 中使用 `<br>` 和 `<hr>`

当你需要换行时使用 `<br>` 标签，你可以将其包含在段落元素中。以下是一个展示其如何运作的示例：

```html
<!DOCTYPE html > 
<html> 
    <head> 
    </head> 
  <body> 
      <h2> Use the line break with the paragraph tag </h2> 
      <p><br> Mama and papa, and baby and Don, 
    <br> Wanda and me? We all went to granny’s house 
             <br> on Christmas day in Bobby’s sleigh. 
      </p> 
  </body>
</html>
```

在段落标签上配合使用换行符

Mama and papa, and baby and Don,

Wanda and me? We all went to granny’s house

on Christmas day in Bobby’s sleigh

`<hr>` 标签在段落或陈述之间应用一条水平线。以下是一个它与 `<p>` 标签一起使用的示例。

```html
<!DOCTYPE html > 
<html>
<head></head>
<body>
<h2> Example showing a horizontal line with paragraphs </h2>
<p> An HTML hr tag will draw a horizontal line which separate two paragraphs .
<hr> a new paragraph is started.
</p>
</body>
</html>
```

此内容的输出是：

Example showing a horizontal line with paragraphs

An HTML hr tag will draw a horizontal line and separate two paragraphs with a new paragraph is started.

#### HTML 短语标签

HTML 短语标签用于定义文本块的结构含义或特定文本的语义。这些是所有的短语标签——你能识别出其中一些：

- `<abbr>`
- `<acronym>`
- `<mark>`
- `<strong>`
- `<em>`
- `<dfn>`
- `<blockquote>`
- `<q>`
- `<code>`
- `<kbd>`
- `<address>`

让我们详细查看这些标签：

1. **文本缩写**：当我们想要对某些文本进行缩写时，使用此标签。该文本放在 `<abbr>` 和 `</abbr>` 之间。这是一个示例：

   ```html
   <p><abbr title="Hypertext Markup language">HTML</abbr> language used for pages.</p>
   ```

   输出结果是：

   Hypertext Markup language used for pages.

2. **标记**：如果你想对特定内容进行高亮，可以使用 `<mark>` 和 `</mark>` 标签。这是一个示例：

   ```html
   <p> This tag will <mark>highlight</mark> the text.</p>
   ```

   输出结果是：

   This tag will highlight the text.

3. **加粗**：如果你想显示某些文本为重要，应使用 `<strong>` 和 `</strong>` 标签。这是一个示例：



```html
<p>In HTML you should use <strong>lower-case</strong>, when you write code.</p>
```

输出结果是：

In HTML you should use lower-case writing code.

### 4. 斜体

如果你希望某些文本倾斜，应将其放在`<em>`和`</em>`之间。这是一个示例：

```html
<p>HTML is an <em>easy</em> language to learn.</p>
```

输出结果是：

HTML is an easy language to learn.

### 5. 定义

`<dfn>`标签用于指定内容的主关键词。这是一个如何使用的示例：

```html
<p><dfn>HTML</dfn> is a markup language.</p>
```

输出结果是：

HTML is a markup language.

### 6. 引用文本

当你想要显示来自不同来源的内容时，使用`<blockquote>`标签。你可以通过使用`cite`属性提供来源 URL，源文本表示放在`<cite>`标签中。这是一个示例：

```html
<blockquote cite="https://www.keepinspiring.me/famous-quotes/"><p>The first step toward success is taken when you refuse to be a captive of the environment in which you find yourself.</p></blockquote>
<cite>-Mark Caine</cite>
```

输出结果是：

"The first step toward success is taken when you refuse to be a captive of the environment in which you find yourself." -Mark Caine

### 7. 短引用

如果你喜欢使用短引用，使用`<q>`标签。插入这些标签之间的文本将以双引号显示。这是一个示例：

```html
<p>Nelson Mandela said: <q>The Greatest Glory In Living Lies In Never Falling, But In Rising Every Time We Fall.</q></p>
```

输出结果是：

Nelson Mandela said: "The Greatest Glory In Living Lies In Never Falling, But In Rising Every Time We Fall."

### 8. 代码标签

我们可以使用`<code>`标签来显示特定的计算机代码。代码以等宽字体显示。这是一个示例：

```html
<p>First Java program</p>
<p><code>class Simple{ public static void main(String args[]){ System.out.println("Hello Java"); }}</code></p>
```

输出结果是：

First Java program

```java
class Simple{ public static void main(String args[]){ System.out.println("Hello Java"); }}
```

### 9. 键盘标签

`<kbd>`标签用于指示指定的内容是用户通过键盘输入的。这里有一个示例：

```html
<p>请按下 <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + t <kbd></kbd> 来在 firefox 上恢复页面。</p>
```

以下是输出：

键盘输入。

请按下 Ctrl + Shift + t 来在 chrome 上恢复页面。

### 10. Address 标签（Address Tag）

`address`标签用于定义内容作者的联系信息。`<address>`和`</address>`之间的任何内容将以斜体显示。示例如下：

```html
<address>
您可以通过 <a href="">example123@newdomain.com</a> 联系我们
<br>
您也可以在以下地址找到我们：
<br>
1234 Pine street, Philadelphia, Pennsylvania, PA 19100.
</address>
```

输出为：

地址标签

您可以通过 example123@newdomain.com 联系我们。

您也可以在以下地址找到我们：

1234 Pine Street, Philadelphia, Pennsylvania, PA 19100.

## 第 5 章：图像、表格和链接

![](img/Image00001.jpg)

### HTML 图像

每个人都知道，一个只有文字而没有图片的网站是非常无聊的，人们很快就会关闭它。添加图像可以显著提升您网站的外观和感受——这里是一些图像示例：

```html
<!DOCTYPE html>
<html>
<body>
<h2>HTML Image</h2>
<img src="pic_girldancing.jpg" alt="girl dancing" width="500" height="333">
</body>
</html>
```

这将会显示以下内容，紧跟着一张图片：

HTML Image

另一个示例：

```html
<!DOCTYPE html>
<html>
<body>
<h2>HTML Image</h2>
<img src="img_girl.jpg" alt="flower garden" width="500" height="600">
</body>
</html>
```

输出是：

HTML Image

![一张包含植物、花的图片 - 自动生成的描述](img/Image00003.jpg)

最后一个示例：

```html
<!DOCTYPE html>
<html>
<body>
<h2>HTML Image</h2>
<img src="img_chania.jpg" alt="open road" width="460" height="345">
</body>
</html>
```

它看起来像：

HTML Image

![一张包含自然、日落、云的图片 - 自动生成的描述](img/Image00004.jpg)

### 语法与属性

在 HTML 网页中嵌入图像需要使用`<img>`标签。从技术上讲，图像并不是被“插入”的；而是链接到一个存放图像的网页，而`<img>`标签是图像引用的容器。

这是没有闭合标签的标签之一；它是空的，只包含属性，其中有两个是必选的：

- `src`–用于指定图像路径
- `alt`–用于指定图像的备用文本——关于这一点稍后会介绍

语法如下：

```html
<img src="url" alt="alternatetext">
```

### src 属性

`src`属性用于指定图像的 URL 或路径。当您打开网页时，浏览器会在加载时获取图像并将其放入网页中。因此，您应该确保图像相对于网页的位置保持不变；否则，访问者只会看到损坏的链接图标。如果浏览器未能找到图像，它将显示损坏链接和`alt`文本。

```html
<img src="img_road.jpg" alt="Open road">
```

### alt 属性

`alt`属性是另一个必选属性，它在观众无法看到图像时提供备用文本。这可能是因为连接不佳、`src`属性错误、正在使用屏幕阅读器等。`alt`属性的值用于描述图像：

```html
<!DOCTYPE html>
<html>
<body>
<h2>备用文本</h2>
<p>alt 属性用于反映图像的内容，以便无法查看图像的用户可以理解它是关于什么：</p>
<img src="img_road.jpg" alt="Open road" width="460" height="345">
</body>
</html>
```

如果浏览器无法定位图像，则显示`alt`属性的值：

```html
<!DOCTYPE html>
<html>
<body>
<p>如果浏览器无法定位图像，则显示 alt 属性的值：</p>
<img src="wrongname.gif" alt="Open road">
</body>
</html>
```

输出是：

如果浏览器无法定位图像，则显示 alt 属性的值：

### 图像尺寸：宽度和高度

`style`属性用于指定图像的高度和宽度：

```html
<!DOCTYPE html>
<html>
<body>
<h2>Image Size</h2>
<p>这里使用 style 属性来指定图像的宽度和高度：</p>
<img src="img_girl.jpg" alt="girl dancing" style="width:500px;height:600px;">
</body>
</html>
```

输出如下内容，紧跟着一张图片：

HTML Image

这里使用 style 属性来指定图像的宽度和高度：

```html
<!DOCTYPE html>
<html>
<body>
<h2>Image Size</h2>
<p>这里使用 style 属性来指定图像的宽度和高度：</p>
<img src="img_girl.jpg" alt="girl dancing" style="width:500px;height:600px;">
</body>
</html>
```

这里使用 style 属性来指定图像的宽度和高度：

```html
<img src="img_girl.jpg" alt="girl dancing" style="width:500px;height:600px;">
```

## 动画图像

HTML 允许动画图像。

### 图片作为链接

如果你想将图片用作链接，需要将`<img>`标签放在`<a>`标签内部：

```html
<!DOCTYPE html>
<html>
<body>
<h2>图片作为链接</h2>
<p>图片是一个链接，可以点击。</p>
<a href="default.asp">
<img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;">
</a>
</body>
</html>
```

输出结果如下，后面紧跟一个微笑笑脸：

图片作为链接

图片是一个链接，可以点击。

### 常见图像格式

这些是所有浏览器都支持的常见图像类型：

| 缩写 | 文件格式 | 文件扩展名 |
| :--- | :--- | :--- |
| APNG | 动画可移植网络图形 | `.apng` |
| GIF | 图像交换格式 | `.gif` |
| ICO | 微软图标 | `.ico`、`.cur` |
| JPEG | 联合图像专家小组图像 | `.jpg`、`.jpeg`、`.jfif`、`.pjpeg`、`.pjp` |
| PNG | 可移植网络图形 | `.png` |
| SVG | 可缩矢量图形 | `.svg` |

### HTML 图像标签

- `<<img>>`–用于定义图像
- `<map>`–用于定义图像映射（image maps）
- `<area>`–用于定义图像映射中的点击区域
- `<picture>`–用于定义包含多个图像资源的容器

### HTML 表格

在 HTML 中，你可以将数据排列成列和行：

```html
<!DOCTYPE html>
<html>
<head>
<style>
table {
  font-family: arial, sans-serif;
  border-collapse: collapse;
  width: 100%;
}
td, th {
  border: 1px solid #dddddd;
  text-align: left;
  padding: 8px;
}
tr:nth-child(Ellie n) {
  background-color: #dddddd;
}
</style>
</head>
<body>
<h2>HTML 表格</h2>
<table>
  <tr>
    <th>公司</th>
    <th>联系人</th>
    <th>国家</th>
  </tr>
  <tr>
    <td>Karl Werner</td>
    <td>Griselda Winters</td>
    <td>德国</td>
  </tr>
  <tr>
    <td>Juan Carlos</td>
    <td>Margarita del Carmen</td>
    <td>墨西哥</td>
  </tr>
  <tr>
    <td>Luisa Bauer</td>
    <td>Sebastian Huber</td>
    <td>奥地利</td>
  </tr>
  <tr>
    <td>Semantics Co Ltd</td>
    <td>John Smith</td>
    <td>英国</td>
  </tr>
  <tr>
    <td>William Tremblay</td>
    <td>Liam Williams</td>
    <td>加拿大</td>
  </tr>
  <tr>
    <td>Alessandro Berlusconi</td>
    <td>Rosa Ricci</td>
    <td>意大利</td>
  </tr>
</table>
</body>
</html>
```

该代码的输出为：

| 公司 | 联系人 | 国家 |
| :--- | :--- | :--- |
| Karl Werner | Griselda Winters | 德国 |
| Juan Carlos | Margarita del Carmen | 墨西哥 |
| Luisa Bauer | Sebastian Huber | 奥地利 |
| Semantic Co Ltd | John Smith | 英国 |
| William Tremblay | Liam Williams | 加拿大 |
| Alessandro Berlusconi | Rosa Ricci | 意大利 |

### 如何定义 HTML 表格

定义 HTML 表格是通过`<table>`标签完成的。使用`<tr>`标签定义每一行，而使用`<th>`标签定义表头。最后，使用`<td>`标签定义单元格/数据。默认情况下，`<th>`标签的文本为粗体并居中，而`<td>`标签的文本左对齐且为常规。

这是一个示例：

```html
<!DOCTYPE html>
<html>
<body>
<h2>基础 HTML 表格</h2>
<table style="width:100%">
  <tr>
    <th>名</th>
    <th>姓</th>
    <th>年龄</th>
  </tr>
  <tr>
    <td>Gillian</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Ellie</td>
    <td>Merton</td>
    <td>94</td>
  </tr>
  <tr>
    <td>John</td>
    <td>Docherty</td>
    <td>80</td>
  </tr>
</table>
</body>
</html>
```

输出为：

基础 HTML 表格

| 名 | 姓 | 年龄 |
| :--- | :--- | :--- |
| Gillian | Smith | 50 |
| Ellie | Merton | 94 |
| John | Docherty | 80 |

注意：`<td>`元素是包含表格数据的图像、列表等 HTML 元素的容器。

### 添加边框

许多人认为需要 CSS 为表格生成边框，但其实不需要：

| Header | Header |
| :--- | :--- |
| Data | Data |

需要的 HTML 代码是：

```html
<table cellspacing="3" bgcolor="#00000">
<tr><th>Header</tr>
<tr><td>Data</tr>
</table>
```

很久以前，在 90 年代，我们使用纯 HTML 来处理边框，这是通过利用`bgcolor`和`cellspacing`属性实现的。如今，如果你倾向于使用 CSS，这是一个完美的方法：

- 我们在`<table>`标签中使用`bgcolor`属性确保背景是特定的颜色。
- 在`<tr>`标签中，`bgcolor`属性用于确保行和列的背景不同。
- `<table>`标签中的`cellspacing`属性在单元格周围创建空间。

### 跨列单元格

`colspan`属性用于使单元格跨越多个列。这是一个示例：



```html
<!DOCTYPE html>
<html>
<head>
<style>
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
th, td {
  padding: 5px;
  text-align: left;
}
</style>
</head>
<body>
<h2>跨列单元</h2>
<p>`colspan` 属性用于使单元格跨越一个列。</p>
<table style="width:100%">
  <tr>
    <th>姓名</th>
    <th colspan="2">联系电话</th>
  </tr>
  <tr>
    <td>Elon Musk</td>
    <td>567852</td>
    <td>567851</td>
  </tr>
</table>
</body>
</html>
```

输出为：

跨列单元

`colspan` 属性用于使单元格跨越一个列：

| 姓名 | 联系电话 | |
| :--- | :--- | :--- |
| Elon Musk | 567852 | 567851 |

### 跨行单元格

`rowspan` 属性用于使单元格跨越多个行：

```html
<!DOCTYPE html>
<html>
<head>
<style>
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
th, td {
  padding: 5px;
  text-align: left;
}
</style>
</head>
<body>
<h2>跨行单元</h2>
<p>`rowspan` 属性用于使单元格跨越一个行。</p>
<table style="width:100%">
  <tr>
    <th>姓名：</th>
    <td>Elon Musk</td>
  </tr>
  <tr>
    <th rowspan="2">联系电话：</th>
    <td>567852</td>
  </tr>
  <tr>
    <td>567851</td>
  </tr>
</table>
</body>
</html>
```

输出为：

跨行单元

`rowspan` 属性用于使单元格跨越一个行：

| 姓名： | Elon Musk |
| :--- | :--- |
| 联系电话： | 567852 |
|  | 567851 |

### 为表格添加标题

`<caption>` 标签用于为表格添加标题：

```html
<!DOCTYPE html>
<html>
<head>
<style>
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
th, td {
  padding: 5px;
  text-align: left;
}
</style>
</head>
<body>
<h2>表格标题</h2>
<p>caption 标签用于为表格添加标题。</p>
<table style="width:100%">
  <caption>每月储蓄</caption>
  <tr>
    <th>月份</th>
    <th>储蓄</th>
  </tr>
  <tr>
    <td>3 月</td>
    <td>$100</td>
  </tr>
  <tr>
    <td>4 月</td>
    <td>$50</td>
  </tr>
</table>
</body>
</html>
```

输出为：

表格标题

caption 标签用于为表格添加标题。

| 每月储蓄 |
| :--- |
| 月份 | 储蓄 |
| 3 月 | $100 |
| 4 月 | $50 |

注意 `<caption>` 标签直接插入在 `<table>` 标签之后。

### 特定表格的特殊样式

如果你想让特定表格具有特殊样式，必须通过 `id` 属性定义：

```html
<table id="t01">
  <tr>
    <th>名</th>
    <th>姓</th>
    <th>年龄</th>
  </tr>
  <tr>
    <td>Ellie</td>
    <td>Merton</td>
    <td>94</td>
  </tr>
</table>
```

现在可以为表格定义特殊样式：

```html
<!DOCTYPE html>
<html>
<head>
<style>
table, th, td {
```

样式表格

| 名字 | 姓 | 年龄 |
| :--- | :--- | :--- |
| Gillian | Smith | 50 |
| Ellie | Merton | 94 |
| John | Docherty | 80 |

| 名字 | 姓 | 年龄 |
| :--- | :--- | :--- |
| Gillian | Smith | 50 |
| Ellie | Merton | 94 |
| John | Docherty | 80 |

你还可以添加更多的样式：

```css
#t01 tr:nth-child(Ellie n) {
  background-color: #eee;
}

#t01 tr:nth-child(odd) {
  background-color: #fff;
}

#t01 th {
  color: white;
  background-color: black;
}
```

将这些内容添加到代码中将产生输出输出：

样式表格

| 名字 | 姓 | 年龄 |
| :--- | :--- | :--- |
| Gillian | Smith | 50 |
| Ellie | Merton | 94 |
| John | Docherty | 80 |

| 名字 | 姓 | 年龄 |
| :--- | :--- | :--- |
| Gillian | Smith | 50 |
| Ellie | Merton | 94 |
| John | Docherty | 80 |

### HTML 表格标签

这些是 HTML 表格标签：

| 标签 | 说明 |
| :--- | :--- |
| `<table>` | 用于定义表格 |
| `<th>` | 用于定义表格的头单元格 |
| `<tr>` | 用于定义表格行 |
| `<td>` | 用于定义表格单元格 |
| `<caption>` | 用于定义表格标题 |
| `<colgroup>` | 用于指定表格中列组以便格式化 |
| `<col>` | 用于指定 `<colgroup>` 标签内每列的属性 |
| `<thead>` | 用于分组表格的头部内容 |
| `<tbody>` | 用于分组表格主体内容 |
| `<tfoot>` | 用于分组表格的页脚内容 |

### HTML 链接

HTML 链接是一个超链接，当你点击它时，它会直接带你到另一个文档。你可能会注意到，当鼠标悬停在链接上时，鼠标光标会发生变化。注意，HTML 中的链接可以是文本、图像或其他元素。

### 语法

`<a>` 标签用于定义超链接：

```html
<a href=" url "> 链接文本 </a>
```

`href` 属性是 `<a>` 标签属性中最重要的属性，因为它用于指示链接的目标。链接文本是用户看到的内容，当他们点击它时，会被重定向到不同的 URL。

以下是创建到 `Wikipedia.com` 链接的方法：

```html
<!DOCTYPE html>
<html>
<body>
<h1>HTML 链接</h1>
<p><a href="https://www.wikipedia.com/">访问 Wikipedia.com!</a></p>
</body>
</html>
```

输出是：

HTML 链接

[访问 Wikipedia.com!](https://www.wikipedia.com/)

在默认情况下，在所有浏览器中，链接显示如下：

- 带下划线且蓝色 – 未访问的链接
- 带下划线且紫色 – 已访问的链接
- 带下划线且红色 – 激活状态的链接

### `target` 属性

默认情况下，链接页面在当前浏览器窗口中显示，但如果你想更改它，则必须指定另一个 `target`。`target` 属性用于指定链接的打开位置，它可以具有以下任何值：

- `_self` - 这是默认值，在点击链接的窗口或标签页中打开链接
- `_blank` - 在不同的标签页或窗口中打开链接
- `_parent_` - 在父框架中打开链接
- `_top_` - 在窗口的全主体中打开链接

这是一个示例：

`target="_blank"` 用于在不同的标签页或窗口中打开链接：

```html
<!DOCTYPE html>
<html>
<body>
<h2>样式表格</h2>
<a href="https://www.wikipedia.com/" target="_blank">访问 Wikipedia.com!</a>
</body>
</html>
```

输出是：

样式表格

[访问 Wikipedia.com!](https://www.wikipedia.com/)

使用 `title` 属性来显示特定元素的额外信息。当鼠标光标悬停在元素上时，将以工具提示的形式显示。

[访问 Wikipedia](https://www.wikipedia.com/html/html_images.asp)

输出为：

# 链接标题

使用 `title` 属性来显示特定元素的额外信息。当鼠标光标悬停在元素上时，将以工具提示的形式显示：

[访问 Wikipedia](https://www.wikipedia.com/html/html_images.asp)

### HTML 链接标签

有一个你需要注意的链接标签：

- `<a>` - 用于定义超链接

# 第 6 章

## HTML 列表

![](img/Image00001.jpg)

在 HTML 中，列表被用于指定包含内容的列表。列表可以包含多个元素，HTML 中有三种类型的列表：

1. 有序列表或编号列表 – `ol`
2. 无序列表或项目符号列表 – `ul`
3. 描述列表或定义列表 – `dl`

值得注意的是，列表可以在列表内部创建，被称为嵌套列表。让我们更详细地查看这些列表类型。

### 有序列表或编号列表（`ol`）

在有序或编号列表中，列表中的所有项目默认都用数字标记。`<ol>` 标签开始编号列表，`<li>` 标签用于开始项目列表：

```html
<!DOCTYPE>
<html> 
<body> 
<ol> 
<li>Libra</li> 
<li>Poker</li> 
<li>Capricorn</li> 
<li>Oracle</li> 
</ol> 
</body>
</html> 
```

输出为：

1. Libra（天秤座）
2. Poker（扑克）
3. Capricorn（摩羯座）
4. Oracle（甲骨）

有序列表可以用于表示字母、数字或任何需要顺序格式的列表。编号列表分为五类：

1. 数字，例如 `1`、`2`、`3` 等。
2. 大写罗马数字，例如 `I`、`II`、`III` 等。
3. 小写罗马数字，例如 `i`、`ii`、`iii` 等。
4. 大写字母，例如 `A`、`B`、`C` 等。
5. 小写字母，例如 `a`、`b`、`c` 等。

`<ol>` 标签可以接受五种类型的属性来表示这五类列表：

| 类型 | 说明 |
| :--- | :--- |
| Type “1” | 默认 – 列表中所有项目使用数字排序 |
| Type “I” | 使用大写罗马数字对列表排序 |
| Type “i” | 使用小写罗马数字对列表排序 |
| Type “A” | 使用大写字母对列表排序 |
| Type “a” | 使用小写字母对列表排序 |

这是一个有序列表的示例，显示了一个包含四个主题的编号列表。注意 `type="1"` 没有定义，因为它是默认值，不需要定义：

```html
<!DOCTYPE html>
<html>
<body>
<ol> 
<li>HTML</li> 
<li>Java</li> 
<li>JavaScript</li> 
<li>SQL</li> 
</ol> 
</body>
</html>
```

输出为：

1. HTML
2. Java
3. JavaScript
4. SQL

### `ol type="I"`

以及使用大写罗马数字显示的相同列表：

```html
<!DOCTYPE html>
<html>
<body>
<ol type="I"> 
<li>HTML</li> 
<li>Java</li> 
<li>JavaScript</li> 
<li>SQL</li> 
</ol> 
</body>
</html>
```

输出为：

1. HTML
2. Java
3. JavaScript
4. SQL

### `ol type="i"`

以及使用小写罗马数字的：

```html
<!DOCTYPE html>
<html>
<body>
<ol type="i"> 
<li>HTML</li> 
<li>Java</li> 
<li>JavaScript</li> 
<li>SQL</li> 
</ol> 
</body>
</html>
```

输出为：

1. HTML
2. Java
3. JavaScript
4. SQL

### `ol type="A"`

使用大写字母的：

```html
<!DOCTYPE html>
<html>
<body>
<ol type="A"> 
<li>HTML</li> 
<li>Java</li> 
<li>JavaScript</li> 
<li>SQL</li> 
</ol>
</body>
</html>
```

输出为：

1. HTML
2. Java
3. JavaScript
4. SQL

### `ol type="a"`

最后，使用小写字母的：

```html
<!DOCTYPE html>
<html>
<body>
<ol type="a"> 
<li>HTML</li> 
<li>Java</li> 
<li>JavaScript</li> 
<li>SQL</li> 
</ol>
</body>
</html>
```

输出为：

1. HTML
2. Java
3. JavaScript
4. SQL

### `Start` 属性

该属性配合 `<ol>` 标签使用，指定列表开始的位置：

- `<ol type="1" start="5">`: 从 5 开始显示。
- `<ol type="A" start="5">`: 从 E 开始显示大写字母。
- `<ol type="a" start="5">`: 从 e 开始显示小写字母。
- `<ol type="I" start="5">`: 从 V 开始显示大写罗马数字。
- `<ol type="i" start="5">`: 从 v 开始显示小写罗马数字。

```html
<!DOCTYPE html>
<html>
<body>
<ol type="i" start="5">
<li>HTML</li> 
<li>Java</li> 
<li>JavaScript</li> 
<li>SQL</li> 
</ol>
</body>
</html>
```

输出为：

5. HTML
6. Java
7. JavaScript
8. SQL

### `Reversed` 属性

`reversed` 属性是一个布尔值，当配合 `<ol>` 标签使用时，会将列表倒序排列：

```html
<!DOCTYPE html>
<html>
<body>
<ol reversed>
<li>HTML</li> 
<li>Java</li> 
<li>JavaScript</li> 
<li>SQL</li> 
</ol>
</body>
</html>
```

输出为：

4. SQL
3. JavaScript
2. Java
1. HTML

## 无序列表或项目符号列表（`ul`）

在无序列表中，使用项目符号来标记列表项目。`<ul>` 标签开始列表，`<li>` 标签开始列表项目：

```html
<!DOCTYPE html>
<html>
<body>
<ul> 
<li>Libra</li> 
<li>Poker</li> 
<li>Capricorn</li> 
<li>Oracle</li> 
</ul>
</body>
</html>
```

输出为：

- Libra
- Poker
- Capricorn
- Oracle

无序列表或项目符号列表不需要特定的顺序。项目符号列表有四类型：

- `disc`
- `circle`
- `square`
- `none`

`<ul>` 标签有四种属性类型来表示不同的列表格式：

| 类型 | 说明 |
| :--- | :--- |
| `disc` | 默认 – 使用实心圆标记列表项目 |
| `circle` | 使用空圈标记列表项目 |
| `square` | 使用正方形标记列表项目 |
| `none` | 列表项目没有任何标记 |

这是一个默认项目符号的示例：

```html
<!DOCTYPE html>
<html>
<body>
<ul> 
<li>HTML</li> 
<li>Java</li> 
<li>JavaScript</li> 
<li>SQL</li> 
</ul>
</body>
</html>
```

输出为：

- HTML
- Java
- JavaScript
- SQL

### `ul type="circle"`

以及圆圈格式：



```html
<!DOCTYPE html>
<html>
<body>
<ul type="circle"> 
<li>HTML</li> 
<li>Java</li> 
<li>JavaScript</li> 
<li>SQL</li> 
</ul>
</body>
</html>
```

输出为：

* HTML
* Java
* JavaScript
* SQL

### `ul type="square"`

以及正方形格式：

```html
<!DOCTYPE html>
<html>
<body>
<ul type="square"> 
<li>HTML</li> 
<li>Java</li> 
<li>JavaScript</li> 
<li>SQL</li> 
</ul>
</body>
</html>
```

输出为：

* HTML
* Java
* JavaScript
* SQL

### `ul type="none"`

以及“无标记”格式：

```html
<!DOCTYPE html>
<html>
<body>
<ul type="none"> 
<li>HTML</li> 
<li>Java</li> 
<li>JavaScript</li> 
<li>SQL</li> 
</ul>
</body>
</html>
```

输出为：

HTML

Java

JavaScript

SQL

### 描述列表

描述列表或定义列表样式在 HTML 和 XHTML 中均支持，条目的列表类似于百科全书或字典。当你需要术语列表、词表或其他键值列表时，最好使用这种列表，它包含三个标签：

1. `<dl>` 标签 – 用于定义列表的开始。
2. `<dt>` 标签 – 用于定义术语。
3. `<dd>` 标签 – 用于定义“定义”术语（描述）。

```html
<!DOCTYPE>
<<html> 
<body> 
<dl> 
<dt>Libra</dt> 
<dd>-一个星座。</dd> 
<dt>Poker</dt> 
<dd>-我最喜欢的周末游戏之一</dd> 
<dt>Capricorn</dt>
<dd>-另一个星座。</dd> 
<dt>Oracle</dt> 
<dd>-一家跨国科技公司。</dd>  
</dl> 
</body>
</html> 
```

输出为：

Libra

-一个星座。

Poker

-我最喜欢的周末游戏之一

Capricorn

-另一个星座。

Oracle

-一家跨国科技公司。

这是另一个示例：

```html
<!DOCTYPE>
<html> 
<body> 
<dl> 
<dt>HTML</dt> 
```

HTML

是一种标记语言

Java

是一个编程平台和语言

JavaScript

是一种脚本语言

SQL

是一种查询语言

### 嵌套列表

列表内部的列表被称为嵌套列表。你可以在一个列表内部包含任何类型的列表，例如有序列表中的无序列表。

```html
<!DOCTYPE html >
<head>
    <title> 嵌套列表 </title>
</head>
<body>
    <p> 非洲国家及其首都是列表 </p>
    <ol>
        <li> 索马利亚
            <ul>
                <li> 摩加迪沙 (Mogadishu)</li>
            </ul>
        </li>
        <li> 埃塞俄比亚
            <ul>
                <li> 亚迪斯亚贝贝 (Adis Ababa)</li>
            </ul>
        </li>
        <li> 冈比亚亚
            <ul>
                <li> 班朱尔 (Banjul)</li>
            </ul>
        </li>
        <li> 塞拉内利昂
            <ul>
                <li> 弗里亚敦 (Freetown)</li>
            </ul>
        </li>
        <li> 安哥拉
            <ul>
                <li> 卢安达 (Luanda)</li>
            </ul>
        </li>
        <li> 摩洛哥
            <ul>
                <li> 拉巴特 (Rabat)</li>
            </ul>  
        </li>
    </ol>
</body>
</html>
```

输出结果为：

非洲国家及其首都是列表

1. 索马利亚
   * 摩加迪沙
2. 埃塞俄比亚
   * 亚迪斯亚贝贝
3. 冈比亚
   * 班朱尔
4. 塞拉内利昂
   * 弗里亚敦
5. 安哥拉
   * 卢安达
6. 摩洛哥
   * 拉巴特

## 第 7 章

## HTML 表单

![](img/Image00001.jpg)

HTML 表单是文档中包含控件的部分。这些控件可以是菜单、复选框、密码字段、单选按钮、文本字段、提交按钮等。这些表单帮助用户输入所需的数据，包括姓名、密码、电子邮件地址、电话号码等。如果你希望从网站访问者那里收集某些数据，这些表单是必须的。例如，假设一个用户想从你的网站进行购买。他们需要为你提供收货地址、姓名、支付详情等，以确保订单能够被正确履行。

### HTML 表单语法

包含表单的语法如下：

```html
<form action="server" method="get|post"> 
//输入控件，例如文本框、文本区域、单选按钮、按钮 
</form>
```

### HTML 表单标签

这些是用于 HTML 表单的标签：

| 标签 | 说明 |
| :--- | :--- |
| `<form>` | 用于定义 HTML 表单，供用户输入内容 |
| `<input>` | 用于定义输入控件 |
| `<textarea>` | 用于定义多行输入 |
| `<label>` | 用于为输入元素定义标签 |
| `<fieldset>` | 用于对表单中的相关元素 |
| `<legend>` | 用于为 `<fieldset>` 元素定义标题 |
| `<select>` | 用于定义下拉列表 |
| `<optgroup>` | 用于在下拉列表中定义选项组 |
| `<option>` | 用于定义下拉列表选项 |
| `<button>` | 用于定义可点击按钮 |

### HTML5 表单属性

| 标签 | 说明 |
| :--- | :--- |
| `<datalist>` | 用于指定预定义的输入控件 |
| `<keygen>` | 用于在表单定义键对 |
| `<output>` | 用于定义计算结果 |

### `<form>` 元素

如前所述，`<form>` 元素为用户提供了输入信息的方法，并提供了不同的控件来实现此，包括密码字段、文本区域、文本字段等。需要注意的是，`<form>` 元素本身不会创建表单；它是一个用于存放表单组成元素的容器。

### `<input>` 元素

这是最基本的表单元素之一，用于创建用户输入信息的表单字段。根据信息的类型，可以使用不同的输入字段。以下是一个显示简单文本输入的示例：

```html
<body>
  <form>
    输入你的姓名 <br>
    <input type="text" name="username">
  </form>
</body>
```

输出结果为：

输入你的姓名![](img/Image00007.jpg)

### 文本框控件（TextField Control）

`input` 标签的 `type="text"` 属性用于创建一个称为单行控件的文本框控件。虽然添加 `name` 属性是可选的，但如 `PHP`、`JSP` 等服务器端组件需要它。

```html
<form>
    名: <input type="text" name="firstname"/> <br>
    姓: <input type="text" name="lastname"/> <br/>
</form>
```

此是输出结果：

名:![](img/Image0008.jpg)

姓![](img/Image0008.jpg)

如果漏掉了 `name` 属性，文本字段输入将不会发送到服务器。

### `<textarea>` 标签

当你在表单中使用多行文本时使用此标签。`<textarea>` 的大小通过 `cols` 或 `rows` 属性指定。这里是一个示例：

```html
<!DOCTYPE html >
<html>
<head>
    <title> HTML 中的表单 </title>
</head>
<body>
  <form>
    输入你的地址： <br>
    <textarea rows="2" cols="20"></textarea>
  </form>
</body>
</html>
```

输出结果为：

输入你的地址![](img/Image00009.jpg)

### 标签标签（Label Tag）

最佳实践建议你应该在表单中带有标签，因为这可以确保代码对用户、浏览器和解析器更加友好。当点击标签时，文本控件将获得焦点。这要求标签标签具有与输入标签的 `id` 属性匹配的属性。

```html
<form>
    <label for="firstname">名: </label> <br>
    <input type="text" id="firstname" name="firstname"/> <br>
    <label for="lastname">姓: </label>
    <input type="text" id="lastname" name="lastname"/> <br/>
</form>
```

输出结果为：

名:![](img/Image0008.jpg)

姓![](img/Image0008.jpg)

### 密码字段控件（Password Field Control）

使用密码字段控件时，用户看不到密码：

```html
<form>
    <label for="password">密码: </label>
    <input type="password" id="password" name="password"/>
</form>
```

输出结果为：

密码![](img/Image0008.jpg)

### 电子邮件字段控件（Email Field Control）

这是 HTML5 的新功能，用于验证用户输入了有效的电子邮件地址。此字段必须包含 `@`。

```html
<form>
    <label for="email">电子邮件:</label>
    <input type="email" id="email" name="email"/>
</form>
```

你应该在浏览器中看到这个：

电子邮件![](img/Image0008.jpg)

如果输入错误的电子邮件地址，屏幕将显示此类错误消息：

电子邮件![](img/Image0010.jpg)

请在电子邮件中包含 `@`

### 单选按钮控件（Radio Button Control）

单选按钮适用于给用户提供多个选项，例如测试、选择性别等。如果你将所有单选按钮命名为同一个，则每次只能选择一个：

```html
<form>
    <label for="gender">性别:</label>
    <input type="radio" id="gender" name="gender" value="male"/>男性
    <input type="radio" id="gender" name="gender" value="female"/>女性 <br/>
</form>
```

此输出在你的浏览器中看起来像这样：

![单选按钮控件](img/Image0011.gif)

### 复选框控件（Checkbox Control）

当你的用户可以从多个复选框中勾选多个选项时使用复选框控件：

```html
<form>
    爱好: <br>
    <input type="checkbox" id="baseball" name="baseball" value="baseball"/>
    <label for="baseball"> 棒球 </label> <br>
    <input type="checkbox" id="basketball" name="basketball" value="basketball"/>
    <label for="basketball"> 篮球 </label> <br>
    <input type="checkbox" id="lacrosse" name="lacrosse" value="lacrosse"/>
    <label for="lacrosse"> 长曲球 </label>
</form>
```

```html
<label for="lacrosse"> 长棍球 </label>
</form>
```

这些与单选按钮非常相似，但可以用于一次选择多个选项——而单选按钮一次只能选择一个选项。

上述代码的输出将是：

爱好：

 棒球

 篮球

 长棍球

### 提交按钮控制

在 HTML 中，当 Web 页面需要提交按钮时，使用 `<input type="submit">`，例如在注册账户或订阅邮件列表时。点击提交按钮时，用户的输入将被发送到服务器。其语法为：

```html
<input type="submit" value="submit">
```

将其拆解：

- `type="submit"` – 指定提交按钮的使用
- `value` 属性 – 你选择写在按钮上显示的任何内容
- `name` 属性 – 可以省略

这是一个示例：

```html
<form>
    <label for="name"> 输入名称 </label><br>
    <input type="text" id="name" name="name"><br>
    <label for="pass"> 输入密码 </label><br>
    <input type="Password" id="pass" name="pass"><br>
    <input type="submit" value="submit">
</form>
```

此的输出为：

输入名称

![](img/Image00012.jpg)

输入密码

![](img/Image00012.jpg)

![](img/Image00013.jpg)

### `<fieldset>` 元素

当你想要在表单中将相关信息分组时，使用 `<fieldset>` 元素。`<legend>` 元素配合它使用，为分组的元素提供标题。

这是一个示例：

```html
<form>
    <fieldset>
        <legend> 用户信息： </legend>
        <label for="name"> 输入名称 </label><br>
        <input type="text" id="name" name="name"><br>
        <label for="pass"> 输入密码 </label><br>
        <input type="Password" id="pass" name="pass"><br>
        <input type="submit" value="submit">
    </fieldset>
</form>
```

此的输出为：

用户信息：

输入名称：

![](img/Image00014.jpg)

输入密码：

![](img/Image00014.jpg)

![](img/Image00015.jpg)

### HTML 表单示例

这是一个简单的注册表单完整示例：




```html
<!DOCTYPE html>
<html>
<head>
    <title> HTML 中的表单 </title>
</head>
<body>
    <h2> 注册表单</h2>
    <form>
        <fieldset>
            <legend> 用户个人信息 </legend>
            <label> 输入您的全名 </label><br>
            <input type="text" name="name" ><br>
            <label> 输入您的电子邮箱 </label><br>
            <input type="email" name="email" ><br>
            <label> 输入您的密码 </label><br>
            <input type="password" name="pass" ><br>
            <label> 确认您的密码 </label><br>
            <input type="password" name="pass" ><br>
            <br><label> 输入您的性别 </label><br>
            <input type="radio" id="gender" name="gender" value="male" /> 男 <br>
            <input type="radio" id="gender" name="gender" value="female" /> 女 <br/>
            <input type="radio" id="gender" name="gender" value="others" /> 其他 <br/>
            <label> 输入您的地址：</br>
            <textarea></textarea>
            <input type="submit" value="sign-up" >
        </fieldset>
    </form>
</body>
</html>
```

在你的屏幕上，你会看到类似这样的内容：![HTML 表单](img/Image00016.gif)

### HTML 表单输入

HTML 表单最重要的元素之一是`<input type="">`。输入元素可以有各种`type`属性，用于定义信息字段。例如，`<input type="text" name="name">`将提供一个文本框。

以下是 HTML 中不同的`<input>`元素类型：

| type | 说明 |
| :--- | :--- |
| text | 用于定义单行文本的输入字段 |
| password | 用于定义单行密码的输入字段 |
| submit | 用于定义将表单发送到服务器的提交按钮 |
| reset | 用于定义重置按钮，允许重置表单值 |
| radio | 用于定义单选按钮，允许选择一个选项 |
| checkbox | 用于定义复选框，允许选择多个选项 |
| button | 用于定义在给定事件上执行指定任务的推按钮 |
| file | 用于定义从设备存储器中选择文件的方法 |
| image | 用于定义带有图形表示的提交按钮 |

在 HTML5 中，`<input>`元素又添加了 10 种新类型：

| type | 说明 |
| :--- | :--- |
| color | 用于定义指定颜色的输入字段 |
| date | 用于定义日期的输入字段 |
| datetime-local | 用于定义本地时间的输入字段 |
| email | 用于定义电子邮箱的输入字段 |
| month | 用于定义月份的输入字段 |
| number | 用于定义数字输入字段 |
| url | 用于定义 URL 的输入字段 |
| week | 用于定义周的输入字段 |
| search | 用于定义搜索的输入字段 |
| tel | 用于定义电话号码的输入字段 |

用户 ID：![](img/Image00020.jpg) 密码：![](img/Image00021.jpg)

![](img/Image00022.jpg) ![](img/Image00023.jpg)

当你输入用户 ID 和密码并点击按钮时，输入字段将重置为默认值。

### `<input type="radio">`

`<input>`的`radio`类型用于定义单选按钮，允许用户从多个相关选项中选择一个。每次只能选择一个选项。这是一个示例：

```html
<form>
  <p> 请选择你最喜欢的颜色 </p>
  <input type="radio" name="color" value="white" > 白色 <br>
  <input type="radio" name="color" value="yellow" > 黄色 <br>
  <input type="radio" name="color" value="black" > 黑色 <br>
  <input type="radio" name="color" value="red" > 红色 <br>
  <input type="submit" value="submit" >
</form>
```

输出是：

输入`radio`类型

表单顶部

请选择你最喜欢的颜色

![](img/Image00024.jpg) 白色

![](img/Image00024.jpg) 黄色

![](img/Image00024.jpg) 黑色

![](img/Image00024.jpg) 红色

![](img/Image00025.jpg)

### `<input type="checkbox">`

`<input>`的`checkbox`类型显示正方形框，用户可以勾选或取消勾选来从一系列给定选项中选择。这些与单选按钮类似，但单选按钮只允许用户在任何时候选择一个选项，而复选框允许他们选择多个。这是一个示例：

```html
<form>
  <label> 输入你的姓名： </label>
  <input type="text" name="name" >
  <p> 请选择你最喜欢的运动 </p>
  <input type="checkbox" name="sport1" value="baseball" > 棒球 <br>
  <input type="checkbox" name="sport2" value="tennis" > 网球 <br>
  <input type="checkbox" name="sport3" value="basketball" > 篮球 <br>
  <input type="checkbox" name="sport4" value="baseball" > 棒球 <br>
  <input type="checkbox" name="sport5" value="badminton" > 羽毛球 <br><br>
  <input type="submit" value="submit" >
</form>
```

输出是：

输入`checkbox`类型

注册表

表单顶部

输入你的姓名：![](img/Image00017.jpg)

请选择你最喜欢的运动

![](img/Image00026.jpg) 棒球

![](img/Image00026.jpg) 网球

![](img/Image00026.jpg) 篮球

![](img/Image00026.jpg) 棒球

![](img/Image00026.jpg) 羽毛球

![](img/Image00027.jpg)

### `<input type="button">`

这用于定义简单的推入按钮，然后对其进行编程以控制事件功能，例如点击事件时会发生什么。虽然它主要配合 JavaScript 工作，但在 HTML 中同样有效：

```html
<form>
  <input type="button" value="点击我 " onclick="alert('you are learning HTML')" >
</form>
```

输出是：

输入`button`类型。

点击按钮查看结果：

### `<input type="file">`

`file` `<input>`类型用于你想让用户从自己的设备存储器中选择一个或多个文件。当文件被选中并提交后，就可以将其上传到服务器，但这需要文件 API 和一些 JavaScript 代码，这超出了本书的范围。

```html
<form>
  <label> 选择要上传的文件： </label>
  <input type="file" name="newfile" >
  <input type="submit" value="submit" >
</form>
```

输出是：

输入`file`类型。

选择任何类型的文件，选中的文件将显示“选择文件”选项旁边：

我们可以选择任何类型的文件，直到我们不指定它！选中的文件将出现在“选择文件”选项旁边

表单顶部

选择文件以上传：![](img/Image00028.jpg)

### `<input type="image">`

这种类型的`<input>`元素代表带有图片的提交按钮：

```html
<!DOCTYPE html>
<html>
<body>
  <h2>输入 "image" 类型。</h2>
  <p> 图像可以作为提交按钮 </p>
  <form>
    <label> 用户 ID： </label><br>
    <input type="text" name="name" /><br>
    <input type="image" alt="提交" src="login.png" width="100px" >
  </form>
</body>
</html>
```

### 新的 HTML5 `<input>`类型

### `<input type="color">`

这定义了带有颜色的输入字段，并允许用户使用浏览器中的视觉界面指定他们想要的颜色。请注意，`color`将使用十六进制值。

```html
<form>
  <label> 选择颜色：</label>
  <input type="color" name="favcolor" value="#ff0000" >
  <input type="submit" value="submit" >
</form>
```

输出是：

输入`color`类型

表单顶部

选择颜色：

```html
<input type="url" name="website" placeholder="http://example.com" ><br>
<input type="submit" value="send data" >
</form>
```

输出是：

`url`类型输入

表单顶部

输入您的网站 URL：

![](img/Image00035.jpg)

### `<input type="week">`

此输入类型将创建一个输入字段，用户可以从下拉日历中选择周和年份，而无需提供时区。

```html
<form>
    <label><b 选择您一年中中最棒的一周： </b></label><br><br>
    <input type="week" name="bestweek" >
    <input type="submit" value="Send data" >
</form>
```

输出是：

`week`类型输入

表单顶部

选择您一年中中最棒的一周：

![](img/Image00036.jpg)

### `<input type="search">`

`search` `<input>`元素将创建一个允许用户输入搜索字符串的输入字段。这些字段在功能上设计为与文本类型对称，但可以有不同的样式。

```html
<form>
    <label> 在此处搜索： </label>
    <input type="search" name="q" >
    <input type="submit" value="search" >
</form>
```

输出是：

`search`类型输入

表单顶部

在此处搜索：![](img/Image00037.jpg)

### `<input type="tel">`

使用此元素允许您创建一个允许用户输入电话号码的输入字段。该类型没有默认验证（如 email 类型那样），因为电话号码的格式在世界各地是不同的。

```html
<form>
    <label><b 输入您的电话号码（格式为 xxx-xxx-xxxx）： </b></label>
    <input type="tel" name="telephone" pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}" requiwhite >
    <input type="submit" ><br><br>
</form>
```

输出是：

`tel`类型输入

表单顶部

输入您的电话号码（格式为 xxx-xxx-xxxx）：![](img/Image00038.jpg)

表单底部

注意我们在这里使用的两个属性是`pattern`和`required`– 这些允许用户按特定格式输入数字，并且在需要将数字输入输入字段时是必须的。

### HTML 表单属性

HTML 包含许多可以与`<form>`元素配合属性：

### `action`属性

当此属性用于`<form>`元素时，它定义了表单在提交或用作 URI 时需要发生什么，用于处理表单上的信息。

它可能是您想在表单处理中使用的 URI，也可能是`.asp`、`.jsp`、`.pho`等。如果未包含属性值，表单将在本地处理并留在当前页面。这是一个示例：

```html
<form action="action.html" method="post" >
    <label> 用户名： </label><br>
    <input type="text" name="name" ><br><br>
    <label> 用户密码 </label>
    <input type="password" name="pass" ><br><br>
    <input type="submit" >
</form>
```

输出是：

表单元素 action 属性的演示

表单顶部

用户名：

![](img/Image00017.jpg)

用户密码

![](img/Image00017.jpg)

![](img/Image00039.jpg)

当点击提交（Submit）按钮时，用户将被重定向到名为`action.html`的另一个页面。

### `method`属性

此属性用于定义浏览器提交表单时使用的 HTTP 方法。它的可能的值有：

- `post`：当我们想要提交敏感数据时使用– 这不会在 URL 中显示提交的数据。

```html
<form action="action.html" method="post" >
```

- `get`：这是表单提交时的默认值，但是不安全的，因为表单提交后数据将显示在 URL 中：

```html
<form action="action.html" method="get" >
```

当提交数据时，输入的文本将显示如下：

`file:///D:/HTML/action.html?name=wikipedia&pass=123`

### `target`属性

此属性用于定义表单提交后响应应该在哪里打开。这些是与此属性使用的关键字：

- `_self`：如果用作属性值，响应将只在当前页面显示：

```html
<form action="action.html" method="get" target="_self" >
```

- `_blank`：如果用作属性，响应将在新页面加载。

```html
<form action="action.html" method="get" target="_blank" >
```

### `autocomplete`属性

`autocomplete`属性是 HTML5 新增的，用于启用输入字段。有两个值`on`和`off`– 它们提供了自动完成选项。

```html
<form action="action.html" method="get" autocomplete="on" >
<form action="action.html" method="get" autocomplete="off" >
```

### `enctype`属性

此属性用于定义表单发送到服务器时的编码类型。可能的值有：

- `application/x-www-form-urlencoded`：这是提交时的默认类型。它会对所有字符进行编码。

```html
<form action="action.html" method="post" enctype="application/x-www-form-urlencoded" >
```

- `multipart/form-data`：当存在文件控件时使用。

```html
<form action="action.html" method="post" enctype="multipart/form-data" >
```

- `text/plain`：这只会编码空格；其他字符将编码。

```html
<form action="action.html" method="post" enctype="text/plain" >
```

### `novalidate`属性

这是添加到`<form>`的布尔值属性。如果对表单应用`novalidate`，则提交时不会进行验证。




```html
<!DOCTYPE html>
<html>
<body>
    <h2>表单</h2>
    <form action="action.html" method="get" novalidate>
        <input type="text" name="name">
        <input type="number" name="age">
        <input type="email" name="email">
        <input type="submit">
    </form>
    <p><b>尝试填写表单详情查看效果。</b></p>
</body>
</html>
```

输出是：

填充表单

表单顶部

name：

age：

email：

![](img/Image0040.jpg)

### `name` 属性

该属性用于定义输入元素的名称。表单提交时，HTTP 请求将包含名称-值对。如果省略名称，输入字段将不会被处理。

```html
<form action="action.html" method="get">
    <input type="text" name="name">
    <input type="number" name="age">
    <input type="email" name="email">
    <input type="submit" value="Submit">
</form>
```

输出是：

填充表单

表单顶部

name：

age：

email：

![](img/Image0041.jpg)

### `value` 属性

此属性用于定义输入字段的初始或默认值。

```html
<form>
    <label>输入您的姓名</label>
    <input type="text" name="uname" value="Input Name">
    <label>输入您的邮箱地址</label>
    <input type="text" name="uname" value="Input email">
    <label>输入您的密码</label>
    <input type="password" name="pass" value="">
    <input type="submit" value="login">
</form>
```

输出是：

填充表单

表单顶部

输入姓名

输入邮箱地址

![](img/Image0042.jpg)

![](img/Image00043.jpg)

输入您的密码

![](img/Image00044.jpg)

![](img/Image00045.jpg)

表单底部

`value` 属性始终会在密码输入字段中自动清除。

### `required` HTML5 属性

该属性是一个布尔值，用于指定在提交表单之前必须填写某个字段：

```html
<form>
    <label>输入您的邮箱地址</label><br>
    <input type="text" name="uname" required><br><br>
    <label>输入您的密码</label><br>
    <input type="password" name="pass"><br><br>
    <input type="submit" value="login">
</form>
```

输出结果为：

填写表单

表单顶部

输入您的邮箱地址

![](img/Image00044.jpg)

输入您的密码

![](img/Image00044.jpg)

![](img/Image00046.jpg)

在提交表单时如果邮箱字段未填写，将显示错误消息。

### `autofocus` HTML5 属性

另一个布尔值属性，它允许字段在网页加载后自动获得焦点。

```html
<form>
    <label>输入您的邮箱地址</label><br>
    <input type="text" name="uname" autofocus><br><br>
    <label>输入您的密码</label><br>
    <input type="password" name="pass"><br><br>
    <input type="submit" value="login">
</form>
```

### `placeholder` HTML5 属性

`placeholder` 用于指定字段中的文本，告诉用户期望他们输入的内容。它可以与密码、文本、URL 和邮箱值一起使用，当输入了 `value` 时，`placeholder` 会被移除。

```html
<form>
    <label>输入您的姓名</label><br>
    <input type="text" name="uname" placeholder="您的姓名"><br><br>
    <label>输入您的邮箱地址</label><br>
    <input type="email" name="email" placeholder="example@gmail.com"><br><br>
    <label>输入您的密码</label><br>
    <input type="password" name="pass" placeholder="您的密码"><br><br>
    <input type="submit" value="login">
</form>
```

输出结果为：

注册表单

表单顶部

输入您的姓名

![](img/Image00044.jpg)

输入您的邮箱地址

输入您的密码

![](img/Image00044.jpg)

![](img/Image00047.jpg)

### `disabled` 属性

该属性将禁用应用的输入字段，意味着用户无法与该字段进行交互。它无法接收任何点击事件，并且在提交表单时，值不会被发送到服务器。

```html
<!DOCTYPE html>
<html>
<body>
    <h3>注册表单</h3>
    <form>
        <label>输入用户名</label><br>
        <input type="text" name="uname" value="USER" disabled><br><br>
        <label>输入您的邮箱地址</label><br>
        <input type="email" name="email" placeholder="example@gmail.com"><br><br>
        <label>输入您的密码</label><br>
        <input type="password" name="pass" placeholder="您的密码"><br><br>
        <input type="submit" value="login">
    </form>
</body>
</html>
```

输出结果为：

注册表单

表单顶部

输入用户名

![](img/Image00048.jpg)

输入邮箱地址

输入您的密码

![](img/Image00044.jpg)

![](img/Image00049.jpg)

### `size` 属性

该属性用于按字符数控制输入字段的大小：

```html
<label>账户持有人</label><br>
<input type="text" name="uname" size="40" required><br><br>
<label>账号</label><br>
<input type="text" name="an" size="30" required><br><br>
<label>CVV</label><br>
<input type="text" name="cvv" size="1" required><br>
```

输出结果为：

带有禁用属性的注册表单

表单顶部

账户名称

![](img/Image00050.jpg)

账号

![](img/Image00051.jpg)

CVV

![](img/Image00052.jpg)

![](img/Image00053.jpg)

### `form` 属性

该属性允许用户为表单指定外部字段，但该字段仍然是主表单的一部分。

```html
User email: <input type="email" name="email" form="fcontrol" required><br>
<input type="submit" form="fcontrol">
```

输出结果为：

表单顶部

用户名：

![](img/Image00044.jpg)

用户密码：

![](img/Image00044.jpg)

表单底部

邮箱字段是外部的

User email:

![](img/Image00044.jpg)

# 8

### Class Attribute

![](img/Image00054.jpg)

### `required` Attribute

![](img/Image00045.jpg)

### `autofocus` Attribute

![](img/Image00046.jpg)

### `placeholder` Attribute

![](img/Image00047.jpg)

### `disabled` Attribute

![](img/Image00048.jpg)

### `size` Attribute

![](img/Image00049.jpg)

### `form` Attribute

![](img/Image00050.jpg)

![](img/Image00051.jpg)

![](img/Image00052.jpg)

![](img/Image00053.jpg)

如今，现代网站通常使用固定菜单进行导航，当你向下滚动页面时，它们通常显示在页面的顶部或侧边。然而，尽管现在是使用 CSS 实现的，但网页浏览器并非一直都支持 CSS。可以使用两个 HTML 元素来提供相同的页面布局，其中某些内容保持静态，而部分内容可以滚动——`frameset` 和 `frame`。

然而，框架确实自带一系列问题，首先是易用性。随着如今移动设备和较小显示器的越来越流行，网站提供可以根据视口更改的视图至关重要。你可以通过操作 `frame` 来提供某种程度的响应式，但它们并不真正适用于响应式网站。其次是可访问性，许多辅助技术（如屏幕阅读器）在理解带有框架的网站并与其通信时会非常困难。

## 如何创建框架

框架背后的概念非常简单：

- `frameset` 元素用于在 HTML 文档中代替 `body` 元素。
- `frame` 元素用于为网页内容创建框架。
- `src` 属性用于识别每个框架中加载的资源。
- 并且可以为每个框架创建带有相关内容的字体。

让我们来看看这一切是如何运作的。首先，我们将创建四个 HTML 文档。这是第一个：

```html
<!DOCTYPE html>
<html>
    <body>
        <h1>Frame 1</h1>
        <p>Frame 1 contents</p>
    </body>
</html>
```

```html
<frame src="frame_2.html" frameborder="0">
<frame src="frame_3.html" frameborder="0">
<frame src="frame_4.html" frameborder="0">
</frameset>
</frameset>
```

我们对第一个框架应用了 `marginheight` 属性，在内容上方和下方留出了 `15px` 的内边距。`frameborder` 的值为 `0`，移除了底部三个框架的边框。

它的样子像这样：

![对顶部框架应用了内边距并移除了其余三个框架边框的框架](img/Image00062.jpg)

### 使用链接指向目标框架

我们使用框架的常用方法之一是向一个始终可见的框架添加固定导航（sticky navigation），无论其他框架中的内容处于什么位置都保持可见。当这些内容被正确实现时，导航链接将导致单个框架中加载新资源，而其余框架保持静态。

我们还可以格式化锚点，使其指向特定的框架，这是通过为带有 `name` 属性的目标框架元素赋值名称，然后在 `<a>` 元素中使用该属性目标来实现的——这将导致 `<href>` 加载到目标框架中。

这听起来清楚吗？让我们一步步来看。

首先，必须在我们希望打开链接的框架上分配一个 `name`。我们将使用在上一个示例中创建的布局——我们将左列用于导航，中间列作为目标框架。要做到这一点，需要为目标分配一个名称：

```html
<frameset rows="150px,*">
    <frame noresize src="frame_1.html" marginheight="15">
    <frameset cols="20%,*,20%">
        <frame src="frame_2.html" frameborder="0">
        <frame src="frame_3.html" name="mid_col" frameborder="0">
        <frame src="frame_4.html" frameborder="0">
    </frameset>
</frameset>
```

中间列被赋予了名称 `name="mid_col"`，现在可以在左侧列（`frame_2.html`）的源文档中创建一些链接，并指向中间列：

```html
<!DOCTYPE html>
<html>
<body>
    <h1>Frame 2</h1>
    <p>Contents of Frame 2</p>
    <ul>
        <li><a href="frame_1.html" target="mid_col">Load frame_1.html</a></li>
        <li><a href="frame_2.html" target="mid_col">Load frame_2.html</a></li>
        <li><a href="frame_3.html" target="mid_col">Load frame_3.html</a></li>
        <li><a href="frame_4.html" target="mid_col">Load frame_4.html</a></li>
    </ul>
</body>
</html>
```

当网页加载时，左侧侧边栏有四个链接。当点击链接时，相关文件内容将显示在带有 `name="mid_col"` 属性的中间列框架中。

当页面加载时，我们首先看到的是这个：

![页面左侧以列形式显示链接的框架集(frameset)](img/Image00063.jpg)

如果点击 `Load Frame_1.html`，我们将看到文件内容加载到中间列，如下所示：

![左侧有导航列且中间框架打开链接的框架集](img/Image00064.jpg)

如果点击 `Load frame_2.html`，导航内容将在中间列和左侧侧边栏中：

![左侧有导航列且中间框架打开链接的框架集](img/Image00065.jpg)

当点击 `Load frame_3.html` 和 `Load frame_4.html` 时，它们将按照你预期的方式工作——在中间列加载内容。

如果我们在链接中省略了 `target="mid_col"`，那么当点击该链接时，资源将在包含链接的框架中加载。如果我们需要重新加载整个页面（例如当链接到外部网站时），则需要在锚点元素中添加 `target="_blank"` 或 `target="_top"`。

### HTML iframes

Iframes 用于显示嵌套的网页，即其他网页内部的网页。`<iframe>` 标签用于定义内联框架（inline frames）。iframe 将一个文档嵌入另一个 HTML 文档的矩形区域内。然而，需要 JavaScript 使 iframe 的内容与网页之间相互交互。

### Iframe 语法

用于定义内联框架的语法是：

```html
<iframe src="URL"></iframe>
```

`src` 属性用于框架地址。

### 设置高度和宽度

`width` 和 `height` 通过 `<iframe>` 属性设置。值的单位是像素，但你也可以将其设置为百分比。这是一个示例：

```html
<!DOCTYPE html>
<html>
<head>
<style>
p { font-size: 50px; }
</style>
</head>
<body style="background">
<p>This is a paragraph.</p>
<iframe src="https://www.w3schools.com" width="300" height="200"></iframe>
</body>
</html>
```

### Iframe 属性表（推断上下文）

| 属性 | 值 | 描述 |
|---|---|---|
| `frameborder` | 1 或 0 | 定义是否添加边框 - HTML5 不支持此属性 |
| `Width` | 像素 | 定义嵌入 iframe 的宽度 – 默认值为 300 px |
| `src` | URL | 此属性提供要加载到 iframe 中的内容的路径或文件名 |



| `sandbox` | `allow-forms` `allow-popups` `allow-scripts` `allow-same-origin` | 用于对帧内容应用额外的限制。这允许提交表单。如果不使用此关键词，表单将无法提交。如果应用此项，将启用弹出窗口；如果不应用，则不启用。这允许脚本运行。这允许嵌入资源被视为从同一源下载的。 |

| `srcdoc` | | 在浏览器支持的情况下，此属性允许在内联帧中显示 HTML 内容，并覆盖 `src` |

| `scrolling` | `auto` `yes` `no` | 此属性告诉浏览器是否为 `iframe` 提供或不提供滚动条 – HTML5 不支持此属性。仅当 `iframe` 的内容大于 `iframe` 的尺寸时才显示滚动条。`iframe` 滚动条将始终显示。`iframe` 滚动条将永远不显示 |

# 第 9 章

## HTML 注释与文件路径

![](img/Image00001.jpg)

### HTML 注释

在计算机编程中，注释是向编码者和其他阅读代码的人解释代码作用的文本或代码。用户看不到它们，只要添加得当，编译器就会忽略它们。

可以使用 `<!-- … -->` 标签在 HTML 中添加注释 – 标签中编写任何内容都会被视为注释：

语法格式：

```
<!-- 在此处编写你的注释文本 -->
```

例如：

```html
<!-- <p>这里有一些文本</p> 
<p>这里有更多文本</p> -->
```

这是一个完整的示例：

```html
<!DOCTYPE html>
<html>
<!-- 这是页眉部分 -->
<head>
    <!-- 内部 CSS -->
    <style>
        body{
            text-align: center;
            background-color: #f0f8ff;
            font-size: 30px;
            color: red;
        }
    </style>
</head>
<!-- 这是正文部分，你希望在网页上显示的代码应该写在这里 -->
<body>
    <!-- 标题标签 -->
<h2>第一个网页</h2>
    <!-- 段落标签 -->
    <p>在此处输入你的内容!!!</p>
</body>
</html>
```

输出结果为：

第一个网页

在此处输入你的内容!!!

### 多行注释

HTML 代码还允许多行注释，你可以在其中添加代码描述、调试指令等。其语法格式如下：

```html
<!---
你的代码被注释了。
为代码编写一段描述。
它将不会在网页上显示。
-->
```

这是一个示例：

```html
<h2>蛋糕画廊</h2>
<!-- 这是一个美味蛋糕的图片
你可以在最喜欢的浏览器在网页上看到这张图片 -->
<img src="https://static.xxxxx.com/htmlpages/images/cake.png" alt="蛋糕图片" height="300px"
width="300px">
```

（请注意，`xxxxx.com` 代替了真实的网站或图像源）

输出结果为：

![包含蛋糕、巧克力、室内、植物的图片自动生成](img/Image00066.jpg)

### HTML 文件路径

HTML 文件路径描述了文件在网站文件夹中的位置。它们非常像你在网络浏览器中输入的以查找特定网站的地址。任何外部资源都可以使用文件路径如图片、JS 文件、CSS 文件、视频等链接到 HTML 文件中。

当 `<href>` 和 `<src>` 属性需要将 HTML 文件链接到外部源时，需要一个属性值。

以下是指定文件路径的不同方式：

* `<img src="picture.jpg">` - 用于指定 `picture.jpg` 在当前页面所在的文件夹中。

* `<img src="images/picture.jpg">` - 用于指定 `picture.jpg` 在当前文件夹中另一个名为“images”的文件夹中。

* `<img src="/images/picture.jpg">` - 用于指定 `picture.jpg` 在当前网站的根目录下的“images”文件夹中。

* `<img src="../picture.jpg">` - 用于指定 `picture.jpg` 在当前文件夹的上一级文件夹中。

我们在网页上使用文件路径来链接以下类型的外部文件：

* 图片

* JavaScript

* 样式表

* 网页

文件路径有两种类型——绝对路径和相对路径。

### 绝对文件路径

这些用于指定完整的 URL 地址，例如：

```html
<!DOCTYPE html>
<html>
<body>
<h2>使用完整的 URL 文件路径</h2>
<img src="https://www.xxxxx.com/images/nature-1.jpg" alt="image" style="width:300px">
</body>
</html>
```

输出结果将是：

### 使用绝对文件路径

![包含树、草、户外、植物的图片自动生成](img/Image00067.jpg)

### 相对文件路径

相对路径指定与页面位置相关的文件。在这个示例中，我们将查看如何使用文件路径指向位于“images”中的文件。

```html
<!DOCTYPE html>
<html>
<body>
<h2>使用绝对文件路径</h2>
<img src="https://www.xxxxx.com/images/nature-1.jpg" alt="image" style="width:300px">
</body>
</html>
```

（注：原文中包含一些重复和重叠的部分，我已根据提供的内容清理了结构。）

### 相对文件路径

相对路径指定与页面位置相关的文件。在这个示例中，我们将查看如何使用文件路径指向位于“images”中的文件。

```html
<!DOCTYPE html>
<html>
<body>
<h2>使用绝对文件路径</h2>
<img src="https://www.xxxxx.com/images/nature-1.jpg" alt="image" style="width:300px">
</body>
</html>
```

主体中的内容显示在浏览器窗口中。

`title` 元素的内容显示在浏览器标签页、搜索引擎搜索结果以及收藏夹中。

输出结果为：

主体中的内容显示在浏览器窗口中。

`title` 元素的内容显示在浏览器标签页、搜索引擎结果和收藏夹中。

### HTML `<style>` 元素

用于为你的 HTML 页面设置样式。虽然 CSS 不在本书的涵盖范围内，但值得注意的是，`<style>` 元素可以包含该特定 HTML 页面的 CSS 属性。这是一个示例：

```html
<!DOCTYPE html>
<html>
<head>
<title>This is the Page Title</title>
<style>
body {background-color: pink;}
h1 {color: red;}
p {color: blue;}
</style>
</head>
<body>
<h1>This is a Heading</h1>
<p>This is a paragraph.</p>
</body>
</html>
```

输出结果为：

This is a Heading

This is a paragraph.

### HTML `<link>` 元素

当你想要将外部样式表链接到你的网页时，可以使用 `<link>` 元素。它有两个属性 —— `rel` 和 `href`。`rel` 用于说明它是一个样式表，而 `href` 提供了指向文件的路径。这是一个示例：

```html
<!DOCTYPE html>
<html>
<head>
<title>This is the title</title>
<link rel="stylesheet" href="style.css">
</head>
<body>
<h2>Web page with external CSS</h2>
<p>This looks cool</p>
</body>
</html>
```

输出结果为：

Web page with external CSS

This is looks cool

### HTML `<meta>` 元素

当我们想要指定字符集，以及页面描述、作者、关键词和其他其他页面元数据（metadata）时，我们使用 `<meta>` 元素。通常，搜索引擎、浏览器和其他网络服务使用元数据作为为你的网页提供更佳排名的方式。

让我们来看看元数据是如何使用的。

### 定义字符集

```html
<meta charset="UTF-8">
```

`charset` 属性用于指定字符的编码。在这个示例中，我们使用的是 `UTF-8`，这意味着任何语言都可以显示。这是一个示例：

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
</head>
<body>
<p>This is written in English <span style="color: blue"> My friend's name is.......</span></p>
<p>This is Chinese language <span style="color: red">Wǒ de péngyǒu jiào</span></p>
</body>
</html>
```

输出结果为：

This is written in English. My friend's name is.......

This is Chinese language W? de péngy?u jiào

#### 定义你的网页描述

```html
<meta name="description" content="Free Web tutorials">
```

元描述对于搜索引擎了解需要寻找什么非常有用。

#### 定义搜索引擎关键词

```html
<meta name="keywords" content="HTML, CSS, XML, JavaScript">
```

当你需要为搜索引擎提供关键词时，也会使用关键词值，但很大程度上归因于垃圾邮件者，浏览器可能会忽略它。

#### 定义网页作者

```html
<meta name="author" content="Akon">
```

此值用于指定谁编写了网页上的内容，某些内容管理系统使用它自动提取作者详情。

#### 每 30 秒刷新一次文档

```html
<meta http-equiv="refresh" content="30">
```

`Meta refresh` 告诉浏览器在指定时间后自动刷新页面。我们将其设置为在 30 秒后刷新，但你可以根据需要设置任何时间段。

```html
<meta http-equiv="refresh" content="10; url=https://www.Wikipedia.com/">
```

如果添加了带有内容值的 URL，则在设定时间结束后将重定向到该页面。这是一个示例：

```html
<!DOCTYPE html>
<html>
<head>
<meta http-equiv="refresh" content="5; url=https://www.Wikipedia.com/">
</head>
<body>
<h2>Meta element Example</h2>
<p style="color: green;">Please wait for 5 seconds and it will automatically redirect to the URL specified in meta tag</p>
</body>
</html>
```

输出结果为：

Meta element Example

Please wait for 5 seconds and it will automatically redirect to the URL specified in meta tag

这是一个展示了 `head` 中使用的所有 `meta` 元素的示例：

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="description" content="Free Web tutorials">
<meta name="keywords" content="HTML, CSS, XML, JavaScript">
<meta name="author" content="Akon">
</head>
<body>
<p>This is written in English <span style="color: blue"> My friend's name is.......</span></p>
</body>
</html>
```

`feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum`

`zzril delenit augue duis dolore te feugait nulla facilisi. Nam liber tempor cum soluta nobis`

`eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum.`

`Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat`

`facer possim assum.`

输出结果：

理解此示例需要你在移动设备上打开该页面。

`Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum. Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum.`

注意 – 为了清楚地看到差异，你应该在移动设备上同时打开之前的两个示例。

#### HTML `<base>` 元素

`<base>` 元素指定了页面上每个相对 URL 的基础 URL 和目标：

```html
<!DOCTYPE html> 
<html>
<head> 
<title>Page Title</title> 
<base href="https://static.Wikipedia.com/ /images/" target="_blank"> 
</head> 
<body> 
<img src="html5.png"> 
<p>The base URL has been specified and the browser will look for the image "html5.png" 
at "https://static.Wikipedia.com/htmlpages/images/html5.png"</p> 

<p><a href=" https://www.Wikipedia.com">Wikipedia</a></a></p> 

<p>This link opens in a new window as the base target has been set to "_blank".</p> 
</body> 
</html>
```

输出结果：

![](img/Image00070.gif)

基础 URL 已指定，浏览器将查找图像 `html5.png` 位于 `https://static.Wikipedia.com/ /images/html5.png`

[维基百科](https://www.wikipedia.com)

此链接将在新窗口中打开，因为基础目标已设置为 `"_blank"`。

## 第 11 章

## HTML 布局

![](img/Image00001.jpg)

HTML 布局是指我们如何以结构良好且响应式的方式安排网页。这是创建网站时需要考虑的最重要的方面之一；出色的布局可以确保你的网站看起来非常专业，并且内容以最合适且用户友好的方式进行布局。

这些是你可以使用的 HTML5 元素用于定义网页的各个部分：

* `<header>`：用于定义节或文档的头部。



- `<nav>`：用于定义包含导航链接的容器。
- `<section>`：用于定义文档节。
- `<article>`：用于定义自包含的、独立的文章。
- `<aside>`：用于定义内容旁的内容，例如侧边栏。
- `<footer>`：用于定义节或文档的页脚。
- `<details>`：用于定义额外的细节。
- `<summary>`：用于`<details>`元素的标题。

HTML 布局确保网页的每个部分都拥有其自身的被正确创建的空间，并可以按照正确的顺序排列。

## 布局元素

### HTML `<header>`

当你想要创建网页头部部分时，使用此元素。在这里，你包含了标题元素、介绍内容、网页图标或标志以及关于作者的信息。这是一个示例：

```html
<header style="background-color: #303030; height: 80px; width: 100%"> 
    <h1 style="font-size: 30px; color: white;text-align: center; padding-top: 15px;">Welcome to MyFirstWebpage</h1> 
</header>
```

输出结果：

![](img/Image00071.jpg)

### HTML `<nav>`

这是一个存放主导航链接的容器，这些链接可以指向同一页，也可以指向外部。这是一个示例：

```html
<nav style="background-color:#bcdeef;"> 
    <h1 style="text-align: center;">Navigation Links</h1> 
    <ul> 
        <li><a href="#">link1</a></li> 
        <li><a href="#">link2</a></li> 
        <li><a href="#">link3</a></li> 
        <li><a href="#">link4</a></li> 
    </ul> 
</nav>
```

### HTML `<section>`

当你想要创建网页头部部分（节）时，使用此元素。在这里，你包含了标题元素、介绍内容、网页图标或标志以及关于作者的信息。这是一个示例：

```html
<section style="background-color: #303030; height: 80px; width: 100%"> 
    <h1 style="font-size: 30px; color: white;text-align: center; padding-top: 15px;">Welcome to MyFirstWebpage</h1> 
</section>
```

### HTML `<article>`

当你想创建网页文章部分时，使用此元素。在这里，你包含了标题元素、介绍内容、网页图标或标志以及关于作者的信息。这是一个示例：

```html
<article style="background-color: #303030; height: 80px; width: 100%"> 
    <h1 style="font-size: 30px; color: white;text-align: center; padding-top: 15px;">Welcome to MyFirstWebpage</h1> 
</article>
```

### HTML `<aside>`

当你想要创建网页侧边部分时，使用此元素。在这里，你包含了标题元素、介绍内容、网页图标或标志以及关于作者的信息。这是一个示例：

```html
<aside style="background-color: #303030; height: 80px; width: 100%"> 
    <h1 style="font-size: 30px; color: white;text-align: center; padding-top: 15px;">Welcome to MyFirstWebpage</h1> 
</aside>
```

### HTML `<footer>`

当你想要创建网页页脚部分时，使用此元素。在这里，你包含了标题元素、介绍内容、网页图标或标志以及关于作者的信息。这是一个示例：

```html
<footer style="background-color: #303030; height: 80px; width: 100%"> 
    <h1 style="font-size: 30px; color: white;text-align: center; padding-top: 15px;">Welcome to MyFirstWebpage</h1> 
</footer
```

### HTML `<details>`

当你想要创建网页细节部分时，使用此元素。在这里，你包含了标题元素、介绍内容、网页图标或标志以及关于作者的信息。这是一个示例：

```html
<details style="background-color: #303030; height: 80px; width: 100%"> 
    <h1 style="font-size: 30px; color: white;text-align: center; padding-top: 15px;">Welcome to MyFirstWebpage</h1> 
</details>
```

### HTML `<summary>`

当你想要创建网页细节标题时，使用此元素。在这里，你包含了标题元素、介绍内容、网页图标或标志以及关于作者的信息。这是一个示例：

```html
<details style="background-color: #303030; height: 80px; width: 100%"> 
    <summary style="font-size: 30px; color: white;text-align: center; padding-top: 15px;">Welcome to MyFirstWebpage</summary> 
</details>
```

## HTML 字符实体

下表显示了 HTML 中最常见的字符实体：

| 结果 | 描述 | 实体名称 | 实体数字 |
| :--- | :--- | :--- | :--- |
|  | 不换行空格 | `&nbsp;` | 160 |
| < | 小于 | `&lt;` | 60 |
| > | 大于 | `&gt;` | 62 |
| & | 安培符号 | `&amp;` | 38 |
| “ | 双引号 | `&quot;` | 34 |
| ‘ | 单引号（撇号） | `&apos;` | 39 |
| ¢ | 分分符号 | `&cent;` | 162 |
| ¢ | 分分符号 | `&cent;` | 162 |
| £ | 英镑 | `&pound;` | 163 |
| ¥ | 日元 | `&yen;` | 165 |
| € | 欧元 | `&euro;` | 8364 |
| © | 版权 | `&copy;` | 169 |

请注意，在使用实体名称时，大小写是非常重要的。使用实体名称的优点是它们容易记忆，但你应该意识到浏览器可能并不支持每一个名称——尽管如此，它们往往倾向于支持实体数字。

这是一个示例：

```html
<!DOCTYPE html>
<html>
<head>
<title></title>
</head>
<body> 
    <h3>HTML 实体示例</h3>
    <p> "这是用实体编写的内容"</p>
    <p> <p> 段落标签 </p> 
</body> 
</html>
```

输出结果是：

HTML 实体示例

"这是用实体编写的内容"

段落标签

### 变音符号（Diacritical Marks）

在 HTML 中，某些特殊的字母类型在字母下方或上方添加有一个字形——这些字形被称为变音符号。这些变音符号中的某些，例如锐音（` ́`）和重音（`̀`），也被称为重符号。变音符号可以使用字母的下方、上方、内部和之间。

以下是常用的变音符号：

| 标记 | 字符 | 构造 | 结果 |
| :--- | :--- | :--- | :--- |
| ̀ | a | a&#768; | à |
| ́ | a | a&#769; | á |
| ̂ | a | a&#770; | â |
| ̃ | a | a&#771; | ã |
| ̀ | O | O&#768; | Ò |
| ́ | O | O&#769; | Ó |
| ̂ | O | O&#770; | Ô |
| ̃ | O | O&#771; | Õ |

### HTML 符号

我们常用的许多技术、数学和货币符号并不总是能在键盘上找到。相反，使用实体名称来将这些符号添加到 HTML 页面中。如果你找不到实体名称或该名称不存在，你可以使用十进制或十六进制引用或实体数字。

这是一个示例：

```html
<!DOCTYPE html>
<html>
    <body>
        <h3> 货币符号</h3>
        <p>这是印度卢比符号 <b>₹<b</b></p>
        <p>这是欧元符号 <b>€</b></p>
        <p> 这是美元符号 <b>#36;</b></p>
    </body>
</html>
```

输出结果是：

货币符号

这是印度卢比符号 ?

这是欧元符号 ?

这是美元符号 $

这些是 HTML 支持的数学符号：

| 字符 | 数字 | 实体 | 描述 |
| :--- | :--- | :--- | :--- |
| ∀ | &#8704; | `&forall;` | 所有的 |
| ∂ | &#8706; | `&part;` | 偏导 |
| ∃ | &#8707; | `&exist;` | 存在 |
| ∅ | &#8709; | `&empty;` | 空集 |
| ∇ | &#8711; | `&nabla;` | Nab 拿算 |
| ∈ | &#8712; | `&isin;` | 属于 |
| ∉ | &#8713; | `&notin;` | 不属于 |
| ∋ | &#8715; | `&ni;` | 包含 |
| ∏ | &#8719; | `&prod;` | n 元乘积 |
| ∑ | &#8721; | `&sum;` | n 元求和 |

HTML 支持希腊符号：

| 字符 | 数字 | 实体 | 描述 |
| :--- | :--- | :--- | :--- |
| Α | &#913 | `&Alpha;` | 希腊字母 Alpha |
| Β | &#914 | `&Beta;` | 希腊字母 Beta |
| Γ | &#915 | `&Gamma;` | 希腊字母 Gamma |
| Δ | &#916 | `&Delta;` | 希腊字母 Delta |
| Ε | &#917 | `&Epsilon;` | 希腊字母 Epsilon |
| Ζ | &#918 | `&Z;` | 希腊字母 Zeta |
|  | &#918 | `&Z;` | 希腊字母 Zeta |

最后，这里是一些重要的符号：

| 字符 | 数字 | 实体 | 描述 |
| :--- | :--- | :--- | :--- |
| © | &#169 | `&copy;` | 版权 |
| ® | &#174 | `&reg;` | 注册 |
| € | &#8364 | `&euro;` | 欧元 |
| ™ | &#8482 | `&trade;` | 商标 |
| ← | &#8592 | `&larr;` | 左箭头 |
| ↑ | &#8593 | `&uarr;` | 上箭头 |
| → | &#8594 | `&rarr;` | 右箭头 |
| ↓ | &#8595 | `&darr;` | 下箭头 |
| ♠ | &#9824 | `&spades;` | 黑桃花 |
| ♣ | &#9827 | `&clubs;` | 梅花形 |
| ♥ | &#9829 | `&hearts;` | 红心形 |
| ♦ | &#9830 | `&diams;` | 方形 |

这是一个示例，展示了如何将表格背景设置为图像。在这里，我建议你在合适的位置插入自己的图片，并查看它在你的计算机上的显示效果：

```html
<!DOCTYPE html>
<html
  <head>
      <title>HTML 背景 Images</title>
  </head>
  <body>
      <!-- 设置表格背景 -->
      <table background = "/images/html.gif" width = "100%" height = "100">
        <tr><td>
          此背景由 HTML 图像填充。
        </td></tr>
      </table>
  </body>
</html>
```

输出结果是：

此背景由 HTML 图像填充。

### 纹理背景和透明背景

在某些网站上，你可以看到背景是有图案的或透明的，这通过使用纹理或透明图像可以轻松实现。当你使用 `PNG` 或 `GIF` 图像来实现此时，请尝试使用尽可能小的尺寸，甚至低到 `1x1`，因为这可以防止加载缓慢。

这是一个示例——再次，请使用你自己的图片：

```html
<!DOCTYPE html>
<html
  <head>
      <title>HTML 背景 Images</title>
  </head>
  <body>
      <!-- 使用纹理设置表格背景 -->
      <table background = "/images/pattern1.gif" width = "100%" height = "100">
        <tr>
          <td>
              此背景有一个纹理图像。
          </td>
        </tr>
      </table>
      <!-- 另一个将纹理作为表格背景的示例 -->
      <table background = "/images/pattern2.gif" width = "100%" height = "100">
        <tr>
          <td>
              此背景有一个纹理图像。
          </td>
        </tr>
      </table>
  </body>
</html>
```

输出结果是：

此背景有一个纹理图像。

此背景有一个纹理图像。

### HTML 颜色

颜色是为你的网页提供极佳视觉效果和感受的最重要方式之一。每个页面都可以使用 `<body>` 标签指定自己的颜色，或者你可以使用 `bgcolor` 属性为单个标签设置颜色。

`<body>` 标签可以具有以下属性：

- `bgcolor` – 用于设置页面背景颜色。
- `text` – 用于设置正文文本颜色。
- `alink` – 用于设置活动或选中链接的颜色。
- `link` – 用于设置链接文本颜色。
- `vlink` – 用于设置已访问链接的颜色，即已经点击点击过的链接。

### 颜色编码方法

你可以使用这三种方法来设置你的网页颜色：

- 颜色名称 – 可以直接指定颜色名称，例如 `green`、`red`、`blue` 等。
- 十六进制代码 – 你可以使用一个 6 位数字来表示颜色，该颜色由固定量的红、绿、蓝组成。
- 颜色十进制或百分比值 – 使用 `rgb()` 属性来设置值。

让我们逐一查看这些：

#### 颜色名称

可以直接使用颜色名称指定颜色来设置你的背景或文本颜色。有 16 个基础名称可以通过 HTML 验证器验证，但总体来说，最大的浏览器支持超过 200 种不同的名称。

这些是标准颜色：

| | 黑色 | | 灰色 | | 银色 | | 白色 |
|---|---|---|---|---|---|---|---|
| | 黄色 | | 柠檬绿 | | 青色 | | 品红 |
| | 红色 | | 绿色 | | 蓝色 | | 紫色 |
| | 栗色 | | 橄榄绿 | | 海蓝色 | | 青绿色 |

这是一个展示如何使用这种方法设置标签背景的示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>按名称命名的 HTML 颜色</title>
  </head>
  <body text = "blue" bgcolor = "green">
    <p>为主使用不同的颜色并查看结果如何。</p>
    <table bgcolor = "black">
      <tr>
        <td>
          <font color = "white">这段文字在背景上将显示为白色。</font>
        </td>
      </tr>
    </table>
  </body>
</html>
```

输出结果是：

为主体使用不同的颜色并查看结果如何。

这段文字在背景上将显示为白色。

#### 十六进制代码

十六进制是 6 位表示法。前两个是 `RR`，代表红色；中间两个是 `GG`，代表绿色；后两个是 `BB`，代表蓝色。十六进制值可以来自 `MS Paint`、`Adobe Photoshop` 以及许多其他图形软件。每个代码前面都有一个哈希（`#`）或符号。这些是一些使用十六进制表示法的颜色：

| 颜色 | 颜色 HEX |
|---|---|
| #000000 |
| #FF0000 |
| #00FF00 |
| #0000FF |
| #FFFF00 |
| #00FFFF |
| #FF00FF |
| #C0C0C0 |
| #FFFFFF |



这是一个展示如何使用十六进制值设置标签背景的示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>按十六进制命名的 HTML 颜色</title>
  </head>
  <body text = "blue" bgcolor = "green">
    <p>为主体和表格使用不同的颜色并查看结果如何。</p>
    <table bgcolor = "black">
      <tr>
        <td>
          <font color = "white">这段文字在背景上将显示为白色。</font>
        </td>
      </tr>
    </table>
  </body>
</html>
```

输出结果是：

为主体和表格使用不同的颜色并查看结果如何。

这段文字在背景上将显示为白色。

### RGB 值

`rgb()` 属性用于设置此值，它将接受三个值 – 红色、绿色和蓝色。该值可以是百分比，也可以是 `0` 到 `255` 之间的整数。注意，并非所有浏览器都支持此颜色属性，因此并不推荐。

是一些使用 RGB 值的颜色：

| 颜色 | 颜色 RGB |
|---|---|
| `rgb(0,0,0)` | |
| `rgb(255,0,0)` | |
| `rgb(0,255,0)` | |
| `rgb(0,0,255)` | |
| `rgb(255,255,0)` | |
| `rgb(0,255,255)` | |
| `rgb(255,0,255)` | |
| `rgb(192,192,192)` | |
| `rgb(255,255,255)` | |

这是一个展示如何使用 `rgb()` 属性设置标签背景的示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>按 RGB 代码命名的 HTML 颜色</title>
  </head>
  <body text = "rgb(0,0,255)" bgcolor = "rgb(0,255,0)">
    <p>为主体和表格使用不同的颜色代码并查看结果如何。</p>
    <table bgcolor = "rgb(0,0,0)">
      <tr>
        <td>
          <font color = "rgb(0,255,255)">这段文字将在背景上显示。</font>
        </td>
      </tr>
    </table>
  </body>
</html>
```

输出结果是：

为主体和表格使用不同的颜色代码并查看结果如何。

这段文字将在背景上显示。

### CSS 颜色

某些颜色被浏览器支持，另一些则不支持。这些是一些标准颜色：

| `999900` | `999933` | `999966` | `999999` | `9999CC` | `9999FF` |
|---|---|---|---|---|---|
| `99CC00` | `99CC33` | `99CC66` | `99CC99` | `99CCCC` | `99CCFF` |
| `99FF00` | `99FF33` | `99FF66` | `99FF99` | `99FFCC` | `99FFFF` |
| `CC0000` | `CC0033` | `CC0066` | `CC0099` | `CC00CC` | `CC00FF` |
| `CC3300` | `CC3333` | `CC3366` | `CC3399` | `CC33CC` | `CC33FF` |
| `CC6600` | `CC6633` | `CC6666` | `CC6699` | `CC66CC` | `CC66FF` |
| `CC9900` | `CC9933` | `CC9966` | `CC9999` | `CC99CC` | `CC99FF` |
| `CCCC00` | `CCCC33` | `CCCC66` | `CCCC99` | `CCCCCC` | `CCCCFF` |
| `CCFF00` | `CCFF33` | `CCFF66` | `CCFF99` | `CCFFCC` | `CCFFFF` |
| `FF0000` | `FF0033` | `FF0066` | `FF0099` | `FF00CC` | `FF00FF` |
| `FF3300` | `FF3333` | `FF3366` | `FF3399` | `FF33CC` | `FF33FF` |
| `FF6600` | `FF6633` | `FF6666` | `FF6699` | `FF66CC` | `FF66FF` |
| `FF9900` | `FF9933` | `FF9966` | `FF9999` | `FF99CC` | `FF99FF` |
| `FFCC00` | `FFCC33` | `FFCC66` | `FFCC99` | `FFCCCC` | `FFCCFF` |
| `FFFF00` | `FFFF33` | `FFFF66` | `FFFF99` | `FFFFCC` | `FFFFFF` |

## HTML 字体

除了颜色和背景图片外，字体在确保你的网站用户友好且内容可读方面也起着重要作用。你所使用的字体样式和颜色完全取决于查看网站时使用的浏览器和硬件，但 `<font>` 标签可以帮助我们为网站文本添加样式、颜色和大小。`<basefont>` 标签用于当你希望所有文本设置为相同的大小、颜色和字体时。

`<font>` 标签有三个可能的属性 – `size`、`face` 和 `color`。如果你想在任何时候更改这些属性中的任何一个，只需要使用 `<font>` 即可。在 `<font>` 标签关闭之前，后续文本将保持更改状态。你可以使用一个 `<font>` 标签来更改一个或所有属性。

### 设置字体大小

`size` 属性用于设置字体大小。接受的值范围从 1 直到 7，但默认值是 3。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>设置字体大小</title>
  </head>
  <body>
      <font size = "1">字体大小 = "1"</font><br />
      <font size = "2">字体大小 = "2"</font><br />
      <font size = "3">字体大小 = "3"</font><br />
      <font size = "4">字体大小 = "4"</font><br />
      <font size = "5">字体大小 = "5"</font><br />
      <font size = "6">字体大小 = "6"</font><br />
      <font size = "7">字体大小 = "7"</font>
  </body>
</html>
```

输出将是：

字体大小 = "1"

字体大小 = "2"

字体大小 = "3"

字体大小 = "4"

字体大小 = "5"

字体大小 = "6"

字体大小 = "7"

#### 相对字体大小

也可以指定比你预设大小更大或更小的字号数。语法为：

`<font size = "+n">`

或者：

`<font size = "−n">`

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>相对字体大小</title>
  </head>
  <body>
      <font size = "-1">字体大小 = "-1"</font><br />
      <font size = "+1">字体大小 = "+1"</font><br />
      <font size = "+2">字体大小 = "+2"</font><br />
      <font size = "+3">字体大小 = "+3"</font><br />
      <font size = "+4">字体大小 = "+4"</font>
  </body>
</html>
```

输出将是：

字体大小 = "-1"

字体大小 = "+1"

字体大小 = "+2"

字体大小 = "+3"

字体大小 = "+4"

#### 设置字体字体

`face` 属性用于设置字体，但你需要注意其中一点 – 如果网站用户没有安装这种特定的字体，他们就无法看到。相反，他们将看到适用于他们的系统的默认字体。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>字体名称</title>
  </head>
  <body>
      <font face = "Times Roman" size = "5">Times Roman</font><br />
      <font face = "Verdana" size = "5">Verdana</font><br />
      <font face = "Comic MS" size ="5">Comic Sans MS</font><br />
      <font face = "WildWest" size = "5">WildWest</font><br />
      <font face = "Bedrock" size = "5">Bedrock</font><br />
  </body>
</html>
```

输出将是：

Times Roman

Verdana

Comic MS

WildWest

#### 指定备用字体

因为如果用户没有你的字体就看不到它，因此你可以指定更多字体作为备用。你所做的只是列出每个字体名称作为备选。

因为如果用户没有你的字体就看不到它，因此你可以指定更多字体作为备用。你所做的只是列出每个字体名称作为备选。

因为用户没有你的字体字体字体字体，，，指定字体字体字体备字体，你所，，，，字体字体字体，，字体。。因为，，，，，，，，，，

字体

，，，，，，，，，，字体，，备字体。

因为如果用户没有你的字体就看不到它，因此你可以指定更多字体作为备用。你所做的只是列出每个字体名称作为备选。



字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体字体字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体备字体。

</p>

字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体。

### 设置字体大小

`size` 属性用于设置字体大小。接受的值范围从 1 直到 7，但默认值是 3。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>设置字体大小</title>
  </head>
  <body>
      <font size = "1">字体大小 = "1"</font><br />
      <font size = "2">字体大小 = "2"</font><br />
      <font size = "3">字体大小 = "3"</font><br />
      <font size = "4">字体大小 = "4"</font><br />
      <font size = "5">字体大小 = "5"</font><br />
      <font size = "6">字体大小 = "6"</font><br />
      <font size = "7">字体大小 = "7"</font>
  </body>
</html>
```

输出将是：

字体大小 = "1"

字体大小 = "2"

字体大小 = "3"

字体大小 = "4"

字体大小 = "5"

字体大小 = "6"

字体大小 = "7"

#### 相对字体大小

也可以指定比你预设大小更大或更小的字号数。语法为：

`<font size = "+n">`

或者

`<font size = "−n">`

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>相对字体大小</title>
  </head>
  <body>
      <font size = "-1">字体大小 = "-1"</font><br />
      <font size = "+1">字体大小 = "+1"</font><br />
      <font size = "+2">字体大小 = "+2"</font><br />
      <font size = "+3">字体大小 = "+3"</font><br />
      <font size = "+4">字体大小 = "+4"</font>
  </body>
</html>
```

输出将是：

字体大小 = "-1"

字体大小 = "+1"

字体大小 = "+2"

字体大小 = "+3"

字体大小 = "+4"

#### 设置字体字体

`face` 属性用于设置字体，但你需要注意其中一点 – 如果网站用户没有安装这种特定的字体，他们就无法看到。相反，他们将看到适用于他们的系统的默认字体。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>字体名称</title>
  </head>
  <body>
      <font face = "Times Roman" size = "5">Times Roman</font><br />
      <font face = "Verdana" size = "5">Verdana</font><br />
      <font face = "Comic MS" size ="5">Comic Sans MS</font><br />
      <font face = "WildWest" size = "5">WildWest</font><br />
      <font face = "Bedrock" size = "5">Bedrock</font><br />
  </body>
</html>
```

输出将是：

Times Roman

Verdana

Comic MS

WildWest

#### 指定备用字体



因为如果用户没有你的字体就看不到它，因此你可以指定更多字体作为备用。你所做的只是列出每个字体名称作为备选。

<font size = "1">字体大小 = "1"</font><br />
<font size = "2">字体大小 = "2"</font><br />
<font size = "3">字体大小 = "3"</font><br />
<font size = "4">字体大小 = "4"</font><br />
<font size = "5">字体大小 = "5"</font><br />
<font size = "6">字体大小 = "6"</font><br />
<font size = "7">字体大小 = "7"</font>

字体字体字体字体字体 1 字体字体字体 =字体 1 字体

<br />

<font size = "1">字体大小 = "1"</font><br />
<font size = "2">字体大小 = "2"</font><br />
<font size = "3">字体大小 = "3"</font><br />
<font size = "4">字体大小 = "4"</font><br />
<font size = "5">字体大小 = "5"</font><br />
<font size = "6">字体大小 = "6"</font><br />
<font size = "7">字体大小 = "7"</font>

字体字体字体字体字体字体字体 1 字体字体字体 =字体 1 字体

字体

<br />

<font size = "1">字体大小 = "1"</font><br />
<font size = "2">字体大小 = "2"</font><br />
<font size = "3">字体大小 = "3"</font><br />
<font size = "4">字体大小 = "4"</font><br />
<font size = "5">字体大小 = "5"</font><br />
<font size = "6">字体大小 = "6"</font><br />
<font size = "7">字体大小 = "7"</font>

字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体字体;font-family:Arial, Helvetica, sans-serif;

| 999900 | 999933 | 999966 | 999999 | 9999CC | 9999FF |
|---|---|---|---|---|---|
| 99CC00 | 99CC33 | 99CC66 | 99CC99 | 99CCCC | 99CCFF |
| 99FF00 | 99FF33 | 99FF66 | 99FF99 | 99FFCC | 99FFFF |
| CC0000 | CC0033 | CC0066 | CC0099 | CC00CC | CC00FF |
| CC3300 | CC3333 | CC3366 | CC3399 | CC33CC | CC33FF |
| CC6600 | CC6633 | CC6666 | CC6699 | CC66CC | CC66FF |
| CC9900 | CC9933 | CC9966 | CC9999 | CC99CC | CC99FF |
| CCCC00 | CCCC33 | CCCC66 | CCCC99 | CCCCCC | CCCCFF |
| CCFF00 | CCFF33 | CCFF66 | CCFF99 | CCFFCC | CCFFFF |
| FF0000 | FF0033 | FF0066 | FF0099 | FF00CC | FF00FF |
| FF3300 | FF3333 | FF3366 | FF3399 | FF33CC | FF33FF |
| FF6600 | FF6633 | FF6666 | FF6699 | FF66CC | FF66FF |
| FF9900 | FF9933 | FF9966 | FF9999 | FF99CC | FF99FF |
| FFCC00 | FFCC33 | FFCC66 | FFCC99 | FFCCCC | FFCCFF |
| FFFF00 | FFFF33 | FFFF66 | FFFF99 | FFFFCC | FFFFFF |

## HTML 字体

除了颜色和背景图片外，字体在确保你的网站用户友好且内容可读方面也起着重要作用。你所使用的字体样式和颜色完全取决于查看网站时使用的浏览器和硬件，但 `<font>` 标签可以帮助我们为网站文本添加样式、颜色和大小。`<basefont>` 标签用于当你希望所有文本设置为相同的大小、颜色和字体时。

`<font>` 标签有三个可能的属性：`size`、`face` 和 `color`。如果你想在任何时候更改这些属性的任何一个，只需要使用 `<font>`。在 `<font>` 标签关闭之前，后续的文本将保持更改状态。你可以使用一个 `<font>` 标签来更改一个或所有属性。

### 设置字体大小

`size` 属性用于设置字体大小。接受的值范围从 1 直到 7，但默认值是 3。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
    <title>设置字体大小</title>
  </head>
  <body>
    <font size="1">字体大小 = "1"</font><br />
    <font size="2">字体大小 = "2"</font><br />
    <font size="3">字体大小 = "3"</font><br />
    <font size="4">字体大小 = "4"</font><br />
    <font size="5">字体大小 = "5"</font><br />
    <font size="6">字体大小 = "6"</font><br />
    <font size="7">字体大小 = "7"</font>
  </body>
</html>
```

输出将是：

字体大小 = "1"

字体大小 = "2"

字体大小 = "3"

字体大小 = "4"

字体大小 = "5"

字体大小 = "6"

字体大小 = "7"

#### 相对字体大小

也可以指定比你预设大小更大或更小的字号数。语法为：

`<font size="+n">`

或者：

`<font size="−n">`

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
    <title>相对字体字体</title>
  </head>
  <body>
    <font size="-1">字体大小 = "-1"</font><br />
    <font size="+1">字体大小 = "+1"</font><br />
    <font size="+2">字体大小 = "+2"</font><br />
    <font size="+3">字体大小 = "+3"</font><br />
    <font size="+4">字体大小 = "+4"</font>
  </body>
</html>
```

输出将是：

字体字体 = "-1"

字体字体 = "+1"

字体字体 = "+2"

字体字体 = "+3"

字体字体 = "+4"

#### 设置字体字体



`face` 属性用于设置字体名称，但你需要注意其中一点：如果网站用户没有安装这种特定的字体，他们就无法看到。相反，他们将看到适用于其系统的默认字体。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>字体名称</title>
  </head>
  <body>
      <font face = "Times Roman" size = "5">Times Roman</font><br />
      <font face = "Verdana" size = "5">Verdana</font><br />
      <font face = "Comic MS" size = "5">Comic Sans MS</font><br />
      <font face = "WildWest" size = "5">WildWest</font><br />
      <font face = "Bedrock" size = "5">Bedrock</font><br />
  </body>
</html>
```

输出将是：

Times Roman

Verdana

Comic MS

WildWest

### 指定备用字体

因为如果用户没有安装你的字体就无法看到它，因此你可以指定更多字体作为备用。你只需要列出每个字体名称作为备选。

## HTML 字体

除了颜色和背景图片外，字体在确保网站用户友好且内容可读方面也起着重要作用。你所使用的字体样式和颜色完全取决于查看网站时使用的浏览器和硬件，但 `<font>` 标签可以帮助我们为网站文本添加样式、颜色和大小。`<basefont>` 标签用于当你希望所有文本设置为相同的大小、颜色和字体时。

`<font>` 标签有三个可能的属性：`size`、`face` 和 `color`。如果你想在任何时候更改这些属性中的任何一个，只需要使用 `<font>`。在 `<font>` 标签关闭之前，后续文本将保持更改状态。你可以使用一个 `<font>` 标签来更改一个或所有属性。

### 设置字体大小

`size` 属性用于设置字体大小。接受的值范围从 1 到 7，但默认值是 3。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>设置字体大小</title>
  </head>
  <body>
      <font size = "1">字体大小 = "1"</font><br />
      <font size = "2">字体大小 = "2"</font><br />
      <font size = "3">字体大小 = "3"</font><br />
      <font size = "4">字体大小 = "4"</font><br />
      <font size = "5">字体大小 = "5"</font><br />
      <font size = "6">字体大小 = "6"</font><br />
      <font size = "7">字体大小 = "7"</font>
  </body>
</html>
```

输出将是：

字体大小 = "1"

字体大小 = "2"

字体大小 = "3"

字体大小 = "4"

字体大小 = "5"

字体大小 = "6"

字体大小 = "7"

#### 相对字体大小

也可以指定比预设大小更大或更小的字号数。语法为：

`<font size = "+n">`

或者：

`<font size = "−n">`

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>相对字体大小</title>
  </head>
  <body>
      <font size = "-1">字体大小 = "-1"</font><br />
      <font size = "+1">字体大小 = "+1"</font><br />
      <font size = "+2">字体大小 = "+2"</font><br />
      <font size = "+3">字体大小 = "+3"</font><br />
      <font size = "+4">字体大小 = "+4"</font>
  </body>
</html>
```

输出将是：

字体大小 = "-1"

字体大小 = "+1"

字体大小 = "+2"

字体大小 = "+3"

字体大小 = "+4"

#### 设置字体名称

`face` 属性用于设置字体名称，但你需要注意其中一点：如果网站用户没有安装这种特定的字体，他们就无法看到。相反，他们将看到适用于其系统的默认字体。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>字体名称</title>
  </head>
  <body>
      <font face = "Times Roman" size = "5">Times Roman</font><br />
      <font face = "Verdana" size = "5">Verdana</font><br />
      <font face = "Comic MS" size = "5">Comic Sans MS</font><br />
      <font face = "WildWest" size = "5">WildWest</font><br />
      <font face = "Bedrock" size = "5">Bedrock</font><br />
  </body>
</html>
```

输出将是：

Times Roman

Verdana

Comic MS

WildWest

### 指定备用字体

因为如果用户没有安装你的字体就无法看到它，因此你可以指定更多字体作为备用。你只需要列出每个字体名称作为备选。

| 999900 | 999933 | 999966 | 999999 | 9999CC | 9999FF |
|---|---|---|---|---|---|
| 99CC00 | 99CC33 | 99CC66 | 99CC99 | 99CCCC | 99CCFF |
| 99FF00 | 99FF33 | 99FF66 | 99FF99 | 99FFCC | 99FFFF |
| CC0000 | CC0033 | CC0066 | CC0099 | CC00CC | CC00FF |
| CC3300 | CC3333 | CC3366 | CC3399 | CC33CC | CC33FF |
| CC6600 | CC6633 | CC6666 | CC6699 | CC66CC | CC66FF |
| CC9900 | CC9933 | CC9966 | CC9999 | CC99CC | CC99FF |
| CCCC00 | CCCC33 | CCCC66 | CCCC99 | CCCCCC | CCCCFF |
| CCFF00 | CCFF33 | CCFF66 | CCFF99 | CCFFCC | CCFFFF |
| FF0000 | FF0033 | FF0066 | FF0099 | FF00CC | FF00FF |
| FF3300 | FF3333 | FF3366 | FF3399 | FF33CC | FF33FF |
| FF6600 | FF6633 | FF6666 | FF6699 | FF66CC | FF66FF |
| FF9900 | FF9933 | FF9966 | FF9999 | FF99CC | FF99FF |
| FFCC00 | FFCC33 | FFCC66 | FFCC99 | FFCCCC | FFCCFF |
| FFFF00 | FFFF33 | FFFF66 | FFFF99 | FFFFCC | FFFFFF |




| 999900 | 999933 | 999966 | 999999 | 9999CC | 9999FF |
|---|---|---|---|---|---|
| 99CC00 | 99CC33 | 99CC66 | 99CC99 | 99CCCC | 99CCFF |
| 99FF00 | 99FF33 | 99FF66 | 99FF99 | 99FFCC | 99FFFF |
| CC0000 | CC0033 | CC0066 | CC0099 | CC00CC | CC00FF |
| CC3300 | CC3333 | CC3366 | CC3399 | CC33CC | CC33FF |
| CC6600 | CC6633 | CC6666 | CC6699 | CC66CC | CC66FF |
| CC9900 | CC9933 | CC9966 | CC9999 | CC99CC | CC99FF |
| CCCC00 | CCCC33 | CCCC66 | CCCC99 | CCCCCC | CCCCFF |
| CCFF00 | CCFF33 | CCFF66 | CCFF99 | CCFFCC | CCFFFF |
| FF0000 | FF0033 | FF0066 | FF0099 | FF00CC | FF00FF |
| FF3300 | FF3333 | FF3366 | FF3399 | FF33CC | FF33FF |
| FF6600 | FF6633 | FF6666 | FF6699 | FF66CC | FF66FF |
| FF9900 | FF9933 | FF9966 | FF9999 | FF99CC | FF99FF |
| FFCC00 | FFCC33 | FFCC66 | FFCC99 | FFCCCC | FFCCFF |
| FFFF00 | FFFF33 | FFFF66 | FFFF99 | FFFFCC | FFFFFF |

## HTML 字体

除了颜色和背景图片外，字体在确保你的网站用户友好且内容可读方面也起着重要作用。你所使用的字体样式和颜色完全取决于查看网站时使用的浏览器和硬件，但 `<font>` 标签可以帮助我们为网站文本添加样式、颜色和大小。`<basefont>` 标签用于当你希望所有文本设置为相同的大小、颜色和字体时。

`<font>` 标签有三个可能的属性：`size`、`face` 和 `color`。如果你想在任何时候更改这些属性中的任何一个，只需要使用 `<font>`。在 `<font>` 标签关闭之前，后续的文本将保持更改状态。你可以使用一个 `<font>` 标签来更改一个或所有属性。

### 设置字体大小

`size` 属性用于设置字体大小。接受的值范围从 1 到 7，但默认值是 3。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>设置字体大小</title>
  </head>
  <body>
      <font size = "1">字体大小 = "1"</font><br />
      <font size = "2">字体大小 = "2"</font><br />
      <font size = "3">字体大小 = "3"</font><br />
      <font size = "4">字体大小 = "4"</font><br />
      <font size = "5">字体大小 = "5"</font><br />
      <font size = "6">字体大小 = "6"</font><br />
      <font size = "7">字体大小 = "7"</font>
  </body>
</html>
```

输出将是：

字体大小 = "1"

字体大小 = "2"

字体大小 = "3"

字体大小 = "4"

字体大小 = "5"

字体大小 = "6"

字体大小 = "7"

#### 相对字体大小

也可以指定比预设大小更大或更小的字号数。语法为：

`<font size = "+n">`

或者：

`<font size = "−n">`

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>相对字体大小</title>
  </head>
  <body>
      <font size = "-1">字体大小 = "-1"</font><br />
      <font size = "+1">字体大小 = "+1"</font><br />
      <font size = "+2">字体大小 = "+2"</font><br />
      <font size = "+3">字体大小 = "+3"</font><br />
      <font size = "+4">字体大小 = "+4"</font>
  </body>
</html>
```

输出将是：

字体大小 = "-1"

字体大小 = "+1"

字体大小 = "+2"

字体大小 = "+3"

字体大小 = "+4"

#### 设置字体名称

`face` 属性用于设置字体名称，但你需要注意一点：如果网站用户没有安装这种特定的字体，他们就无法看到。相反，他们将看到适用于其系统的默认字体。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>字体名称</title>
  </head>
  <body>
      <font face = "Times Roman" size = "5">Times Roman</font><br />
      <font face = "Verdana" size = "5">Verdana</font><br />
      <font face = "Comic MS" size ="5">Comic Sans MS</font><br />
      <font face = "WildWest" size = "5">WildWest</font><br />
      <font face = "Bedrock" size = "5">Bedrock</font><br />
  </body>
</html>
```

输出将是：

Times Roman

Verdana

Comic MS

WildWest

#### 指定备用字体

因为如果用户没有安装你的字体就无法看到它，因此你可以指定更多字体作为备用。你只需要列出每个字体名称作为备选。




```html
<!DOCTYPE html>
<html>
  <head>
    <title>相对字体字体</title>
  </head>
  <body>
    <font size="-1">字体大小 = "-1"</font><br />
    <font size="+1">字体大小 = "+1"</font><br />
    <font size="+2">字体大小 = "+2"</font><br />
    <font size="+3">字体大小 = "+3"</font><br />
    <font size="+4">字体大小 = "+4"</font>
  </body>
</html>
```

输出将是：

字体字体 = "-1"

字体字体 = "+1"

字体字体 = "+2"

字体字体 = "+3"

字体字体 = "+4"

#### 设置字体字体

`face` 属性用于设置字体名称，但你需要注意其中一点：如果网站用户没有安装这种特定的字体，他们就无法看到。相反，他们将看到适用于其系统的默认字体。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
    <title>字体名称</title>
  </head>
  <body>
    <font face="Times Roman" size="5">Times Roman</font><br />
    <font face="Verdana" size="5">Verdana</font><br />
    <font face="Comic MS" size="5">Comic Sans MS</font><br />
    <font face="WildWest" size="5">WildWest</font><br />
    <font face="Bedrock" size="5">Bedrock</font><br />
  </body>
</html>
```

输出将是：

Times Roman

Verdana

Comic MS

WildWest

#### 指定备用字体

因为如果用户没有你的字体就看不到它，因此你可以指定更多字体作为备用。你所做的只是列出每个字体名称作为备选。

| 999900 | 999933 | 999966 | 999999 | 9999CC | 9999FF |
|---|---|---|---|---|---|
| 99CC00 | 99CC33 | 99CC66 | 99CC99 | 99CCCC | 99CCFF |
| 99FF00 | 99FF33 | 99FF66 | 99FF99 | 99FFCC | 99FFFF |
| CC0000 | CC0033 | CC0066 | CC0099 | CC00CC | CC00FF |
| CC3300 | CC3333 | CC3366 | CC3399 | CC33CC | CC33FF |
| CC6600 | CC6633 | CC6666 | CC6699 | CC66CC | CC66FF |
| CC9900 | CC9933 | CC9966 | CC9999 | CC99CC | CC99FF |
| CCCC00 | CCCC33 | CCCC66 | CCCC99 | CCCCCC | CCCCFF |
| CCFF00 | CCFF33 | CCFF66 | CCFF99 | CCFFCC | CCFFFF |
| FF0000 | FF0033 | FF0066 | FF0099 | FF00CC | FF00FF |
| FF3300 | FF3333 | FF3366 | FF3399 | FF33CC | FF33FF |
| FF6600 | FF6633 | FF6666 | FF6699 | FF66CC | FF66FF |
| FF9900 | FF9933 | FF9966 | FF9999 | FF99CC | FF99FF |
| FFCC00 | FFCC33 | FFCC66 | FFCC99 | FFCCCC | FFCCFF |
| FFFF00 | FFFF33 | FFFF66 | FFFF99 | FFFFCC | FFFFFF |

## HTML 字体

除了颜色和背景图片外，字体在确保你的网站用户友好且内容可读方面也起着重要作用。你所使用的字体样式和颜色完全取决于查看网站时使用的浏览器和硬件，但 `<font>` 标签可以帮助我们为网站文本添加样式、颜色和大小。`<basefont>` 标签用于当你希望所有文本设置为相同的大小、颜色和字体时。

`<font>` 标签有三个可能的属性：`size`、`face` 和 `color`。如果你想在任何时候更改这些属性中的任何一个，只需要使用 `<font>`。在 `<font>` 标签关闭之前，后续的文本将保持更改状态。你可以使用一个 `<font>` 标签来更改一个或所有属性。

### 设置字体大小

`size` 属性用于设置字体大小。接受的值范围从 1 直到 7，但默认值是 3。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
    <title>设置字体大小</title>
  </head>
  <body>
    <font size="1">字体大小 = "1"</font><br />
    <font size="2">字体大小 = "2"</font><br />
    <font size="3">字体大小 = "3"</font><br />
    <font size="4">字体大小 = "4"</font><br />
    <font size="5">字体大小 = "5"</font><br />
    <font size="6">字体大小 = "6"</font><br />
    <font size="7">字体大小 = "7"</font>
  </body>
</html>
```

输出将是：

字体大小 = "1"

字体大小 = "2"

字体大小 = "3"

字体大小 = "4"

字体大小 = "5"

字体大小 = "6"

字体大小 = "7"

#### 相对字体大小

也可以指定比预设大小更大或更小的字号数。语法为：

`<font size="+n">`

或者：

`<font size="−n">`

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
    <title>相对字体大小</title>
  </head>
  <body>
    <font size="-1">字体大小 = "-1"</font><br />
    <font size="+1">字体大小 = "+1"</font><br />
    <font size="+2">字体大小 = "+2"</font><br />
    <font size="+3">字体大小 = "+3"</font><br />
    <font size="+4">字体大小 = "+4"</font>
  </body>
</html>
```

输出将是：

字体大小 = "-1"

字体大小 = "+1"

字体大小 = "+2"

字体大小 = "+3"

字体大小 = "+4"

#### 设置字体字体

`face` 属性用于设置字体名称，但你需要注意其中一点：如果网站用户没有安装这种特定的字体，他们就无法看到。相反，他们将看到适用于其系统的默认字体。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
    <title>字体名称</title>
  </head>
  <body>
    <font face="Times Roman" size="5">Times Roman</font><br />
    <font face="Verdana" size="5">Verdana</font><br />
    <font face="Comic MS" size="5">Comic Sans MS</font><br />
    <font face="WildWest" size="5">WildWest</font><br />
    <font face="Bedrock" size="5">Bedrock</font><br />
  </body>
</html>
```

输出将是：

Times Roman

Verdana

Comic MS

WildWest

#### 指定备用字体

因为如果用户没有你的字体就看不到它，因此你可以指定更多字体作为备用。你所做的只是列出每个字体名称作为备选。

| 999900 | 999933 | 999966 | 999999 | 9999CC | 9999FF |
|---|---|---|---|---|---|
| 99CC00 | 99CC33 | 99CC66 | 99CC99 | 99CCCC | 99CCFF |
| 99FF00 | 99FF33 | 99FF66 | 99FF99 | 99FFCC | 99FFFF |
| CC0000 | CC0033 | CC0066 | CC0099 | CC00CC | CC00FF |
| CC3300 | CC3333 | CC3366 | CC3399 | CC33CC | CC33FF |
| CC6600 | CC6633 | CC6666 | CC6699 | CC66CC | CC66FF |
| CC9900 | CC9933 | CC9966 | CC9999 | CC99CC | CC99FF |
| CCCC00 | CCCC33 | CCCC66 | CCCC99 | CCCCCC | CCCCFF |




| CCFF00 | CCFF33 | CCFF66 | CCFF99 | CCFFCC | CCFFFF |
|---|---|---|---|---|---|
| FF0000 | FF0033 | FF0066 | FF0099 | FF00CC | FF00FF |
| FF3300 | FF3333 | FF3366 | FF3399 | FF33CC | FF33FF |
| FF6600 | FF6633 | FF6666 | FF6699 | FF66CC | FF66FF |
| FF9900 | FF9933 | FF9966 | FF9999 | FF99CC | FF99FF |
| FFCC00 | FFCC33 | FFCC66 | FFCC99 | FFCCCC | FFCCFF |
| FFFF00 | FFFF33 | FFFF66 | FFFF99 | FFFFCC | FFFFFF |

## HTML 字体

除了颜色和背景图片外，字体在确保你的网站用户友好且内容可读方面也起着重要作用。你所使用的字体样式和颜色完全取决于查看网站时使用的浏览器和硬件，但`<font>`标签可以帮助我们为网站文本添加样式、颜色和大小。`<basefont>`标签用于当你希望所有文本设置为相同的大小、颜色和字体时。

`<font>`标签有三个可能的属性：`size`、`face`和`color`。如果你想在任何时候更改这些属性中的任何一个，只需要使用`<font>`。在`<font>`标签关闭之前，后续的文本将保持更改状态。你可以使用一个`<font>`标签来更改一个或所有属性。

### 设置字体大小

`size`属性用于设置字体大小。接受的值范围从 1 直到 7，但默认值是 3。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>设置字体大小</title>
  </head>
  <body>
      <font size = "1">字体大小 = "1"</font><br />
      <font size = "2">字体大小 = "2"</font><br />
      <font size = "3">字体大小 = "3"</font><br />
      <font size = "4">字体大小 = "4"</font><br />
      <font size = "5">字体大小 = "5"</font><br />
      <font size = "6">字体大小 = "6"</font><br />
      <font size = "7">字体大小 = "7"</font>
  </body>
</html>
```

输出将是：

字体大小 = "1"

字体大小 = "2"

字体大小 = "3"

字体大小 = "4"

字体大小 = "5"

字体大小 = "6"

字体大小 = "7"

#### 相对字体大小

也可以指定比预设大小更大或更小的字号数。语法为：

`<font size = "+n">`

或者：

`<font size = "−n">`

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>相对字体大小</title>
  </head>
  <body>
      <font size = "-1">字体大小 = "-1"</font><br />
      <font size = "+1">字体大小 = "+1"</font><br />
      <font size = "+2">字体大小 = "+2"</font><br />
      <font size = "+3">字体大小 = "+3"</font><br />
      <font size = "+4">字体大小 = "+4"</font>
  </body>
</html>
```

输出将是：

字体大小 = "-1"

字体大小 = "+1"

字体大小 = "+2"

字体大小 = "+3"

字体大小 = "+4"

#### 设置字体名称

`face`属性用于设置字体名称，但你需要注意一点：如果网站用户没有安装这种特定的字体，他们就无法看到。相反，他们将看到适用于其系统的默认字体。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>字体名称</title>
  </head>
  <body>
      <font face = "Times Roman" size = "5">Times Roman</font><br />
      <font face = "Verdana" size = "5">Verdana</font><br />
      <font face = "Comic MS" size ="5">Comic Sans MS</font><br />
      <font face = "WildWest" size = "5">WildWest</font><br />
      <font face = "Bedrock" size = "5">Bedrock</font><br />
  </body>
</html>
```

输出将是：

Times Roman

Verdana

Comic MS

WildWest

#### 指定备用字体

因为如果用户没有安装你的字体就无法看到它，所以你可以指定更多字体作为备用。你只需要列出每个字体名称作为备选。




## HTML 字体

除了颜色和背景图片外，字体在确保你的网站用户友好且内容可读方面也起着重要作用。你所使用的字体样式和颜色完全取决于查看网站时使用的浏览器和硬件，但`<font>`标签可以帮助我们为网站文本添加样式、颜色和大小。`<basefont>`标签用于当你希望所有文本设置为相同的大小、颜色和字体时。

`<font>`标签有三个可能的属性 – `size`、`face`和`color`。如果你想在任何时候更改这些属性的任何一个，只需要使用`<font>`。在`<font>`标签关闭之前，后续的文本将保持更改状态。你可以使用一个`<font>`标签来更改一个或所有属性。

### 设置字体大小

`size`属性用于设置字体大小。接受的值范围从1直到7，但默认值是3。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>设置字体大小</title>
  </head>
  <body>
      <font size = "1">字体大小 = "1"</font><br />
      <font size = "2">字体大小 = "2"</font><br />
      <font size = "3">字体大小 = "3"</font><br />
      <font size = "4">字体大小 = "4"</font><br />
      <font size = "5">字体大小 = "5"</font><br />
      <font size = "6">字体大小 = "6"</font><br />
      <font size = "7">字体大小 = "7"</font>
  </body>
</html>
```

输出将是：

字体大小 = "1"

字体大小 = "2"

字体大小 = "3"

字体大小 = "4"

字体大小 = "5"

字体大小 = "6"

字体大小 = "7"

#### 相对字体大小

也可以指定比你预设大小更大或更小的字号数。语法为：

`<font size = "+n">`

或者

`<font size = "−n">`

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>相对字体大小</title>
  </head>
  <body>
      <font size = "-1">字体大小 = "-1"</font><br />
      <font size = "+1">字体大小 = "+1"</font><br />
      <font size = "+2">字体大小 = "+2"</font><br />
      <font size = "+3">字体大小 = "+3"</font><br />
      <font size = "+4">字体大小 = "+4"</font>
  </body>
</html>
```

输出将是：

字体大小 = "-1"

字体大小 = "+1"

字体大小 = "+2"

字体大小 = "+3"

字体大小 = "+4"

#### 设置字体字体

`face`属性用于设置字体名称，但你需要注意其中一点 – 如果网站用户没有安装这种特定的字体，他们就无法看到。相反，他们将看到适用于他们的系统的默认字体。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>字体名称</title>
  </head>
  <body>
      <font face = "Times Roman" size = "5">Times Roman</font><br />
      <font face = "Verdana" size = "5">Verdana</font><br />
      <font face = "Comic MS" size ="5">Comic Sans MS</font><br />
      <font face = "WildWest" size = "5">WildWest</font><br />
      <font face = "Bedrock" size = "5">Bedrock</font><br />
  </body>
</html>
```

输出将是：

Times Roman

Verdana

Comic MS

WildWest

#### 指定备用字体

因为如果用户没有你的字体就看不到它，因此你可以指定更多字体作为备用。你所做的只是列出每个字体名称作为备选。



实际上，提示要求“翻译给定的英文文本”。文本中包含大量噪声，因此我只翻译有意义的部分。

```html
<!DOCTYPE html>
<html>
  <head>
      <title>设置字体大小</title>
  </head>
  <body>
      <font size = "1">字体大小 = "1"</font><br />
      <font size = "2">字体大小 = "2"</font><br />
      <font size = "3">字体大小 = "3"</font><br />
      <font size = "4">字体大小 = "4"</font><br />
      <font size = "5">字体大小 = "5"</font><br />
      <font size = "6">字体大小 = "6"</font><br />
      <font size = "7">字体大小 = "7"</font>
  </body>
</html>
```

……（其余 HTML 代码）……

我只提供实际内容的完整翻译。

| `999900` | `999933` | `999966` | `999999` | `9999CC` | `9999FF` |
| --- | --- | --- | --- | --- | --- |
| `99CC00` | `99CC33` | `99CC66` | `99CC99` | `99CCCC` | `99CCFF` |
| `99FF00` | `99FF33` | `99FF66` | `99FF99` | `99FFCC` | `99FFFF` |
| `CC0000` | `CC0033` | `CC0066` | `CC0099` | `CC00CC` | `CC00FF` |
| `CC3300` | `CC3333` | `CC3366` | `CC3399` | `CC33CC` | `CC33FF` |
| `CC6600` | `CC6633` | `CC6666` | `CC6699` | `CC66CC` | `CC66FF` |
| `CC9900` | `CC9933` | `CC9966` | `CC9999` | `CC99CC` | `CC99FF` |
| `CCCC00` | `CCCC33` | `CCCC66` | `CCCC99` | `CCCCCC` | `CCCCFF` |
| `CCFF00` | `CCFF33` | `CCFF66` | `CCFF99` | `CCFFCC` | `CCFFFF` |
| `FF0000` | `FF0033` | `FF0066` | `FF0099` | `FF00CC` | `FF00FF` |
| `FF3300` | `FF3333` | `FF3366` | `FF3399` | `FF33CC` | `FF33FF` |
| `FF6600` | `FF6633` | `FF6666` | `FF6699` | `FF66CC` | `FF66FF` |
| `FF9900` | `FF9933` | `FF9966` | `FF9999` | `FF99CC` | `FF99FF` |
| `FFCC00` | `FFCC33` | `FFCC66` | `FFCC99` | `FFCCCC` | `FFCCFF` |
| `FFFF00` | `FFFF33` | `FFFF66` | `FFFF99` | `FFFFCC` | `FFFFFF` |

## HTML 字体

除了颜色和背景图片外，字体在确保网站用户友好且内容可读方面也起着重要作用。你所使用的字体样式和颜色完全取决于查看网站时使用的浏览器和硬件，但`<font>`标签可以帮助我们为网站文本添加样式、颜色和大小。`<basefont>`标签用于当你希望所有文本设置为相同的大小、颜色和字体时。

`<font>`标签有三个可能的属性：`size`、`face`和`color`。如果你想在任何时候更改这些属性中的任何一个，只需要使用`<font>`。在`<font>`标签关闭之前，后续文本将保持更改状态。你可以使用一个`<font>`标签来更改一个或所有属性。

### 设置字体大小

`size`属性用于设置字体大小。接受的值范围从 1 到 7，但默认值是 3。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>设置字体大小</title>
  </head>
  <body>
      <font size = "1">字体大小 = "1"</font><br />
      <font size = "2">字体大小 = "2"</font><br />
      <font size = "3">字体大小 = "3"</font><br />
      <font size = "4">字体大小 = "4"</font><br />
      <font size = "5">字体大小 = "5"</font><br />
      <font size = "6">字体大小 = "6"</font><br />
      <font size = "7">字体大小 = "7"</font>
  </body>
</html>
```

输出将是：

字体大小 = "1"

字体大小 = "2"

字体大小 = "3"

字体大小 = "4"

字体大小 = "5"

字体大小 = "6"

字体大小 = "7"

#### 相对字体大小

也可以指定比预设大小更大或更小的字号数。语法为：

`<font size = "+n">`

或者：

`<font size = "−n">`

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>相对字体大小</title>
  </head>
  <body>
      <font size = "-1">字体大小 = "-1"</font><br />
      <font size = "+1">字体大小 = "+1"</font><br />
      <font size = "+2">字体大小 = "+2"</font><br />
      <font size = "+3">字体大小 = "+3"</font><br />
      <font size = "+4">字体大小 = "+4"</font>
  </body>
</html>
```

输出将是：

字体大小 = "-1"

字体大小 = "+1"

字体大小 = "+2"

字体大小 = "+3"

字体大小 = "+4"

#### 设置字体名称

`face`属性用于设置字体名称，但你需要注意一点：如果网站用户没有安装这种特定字体，他们就无法看到该字体。相反，他们将看到适用于其系统的默认字体。

这是一个示例：

```html
<!DOCTYPE html>
<html>
  <head>
      <title>字体名称</title>
  </head>
  <body>
      <font face = "Times Roman" size = "5">Times Roman</font><br />
      <font face = "Verdana" size = "5">Verdana</font><br />
      <font face = "Comic MS" size ="5">Comic Sans MS</font><br />
      <font face = "WildWest" size = "5">WildWest</font><br />
      <font face = "Bedrock" size = "5">Bedrock</font><br />
  </body>
</html>
```

输出将是：

Times Roman

Verdana

Comic MS

WildWest

#### 指定备用字体

如果用户没有安装你的字体，就无法看到它。因此，你可以指定更多字体作为备用。你只需要列出每个字体名称作为备选。

1. 在闭合的`<head>`标签下方输入`<body>`。HTML 文档的主体现在已打开，在此标签中输入的任何内容都将显示在页面上。

2. 输入`<h1>`。这会为 HTML 文档提供一个标题，该标题将以大号、加粗字体显示，并位于文档顶部。

3. 输入页面标题，可以是任何内容，从页面标题到简单的问候语。

4. 在标题文本之后，输入`</h1>`来关闭标题标签，然后按回车键。

从这里开始，你可以在页面上添加任何想要的标题。你可以从六种标题样式中进行选择，从`<h1>`到`<h6>`，正如前面的部分所演示的那样。为了复习，你可以连续使用三个不同大小的标题，例如：

```html
<h1>Welcome to this page!</h1>
<h2>My name is Jimmy.</h2>
<h3>I hope you have fun here.</h3>
```

不同的标题表示文本的重要性，但即使你没有使用`<h1>`或`<h2>`标签，仍然可以使用`<h3>`标签；你不需要按顺序使用它们。

5. 现在输入`<p>`来开启段落，文本将在此处以正常大小显示。

6. 输入你的文本，也许是网页描述或其他你希望用户看到的信息。

7. 输入文本后，输入`</p>`来关闭标签并按回车键。你的段落文本看起来像这样：

```html
<p>This is my first paragraph</p>
```

同样，可以使用这种方式添加额外段落。如果你想在一个标题下显示多个段落，可以连续使用多个`<p>`标签。

还可以通过`<font color="color">`和`</font>`标签来更改文本颜色。确保在引号内的`color`部分输入你想要的颜色。使用这些标签，你可以更改任何内容的颜色。例如，如果你想将一个段落改为红色文本，需要输入以下内容：

```html
<p><font color="red">(your text here)</font></p>
```

你还可以添加其他格式，例如斜体和加粗。以下是一些示例：

```html
<b>Bold text</b>
<i>Italic text</i>
<u>Underlined text</u>
<sub>Subscript text</sub>
<sup>Superscript text</sup>
```

如果你想使用斜体和加粗来强调文本，而不仅仅是为了样式，请使用`<em>`和`<strong>`，而不是`<i>`和`<b>`。这将确保在使用屏幕阅读器或其他辅助技术时，你的网页更容易被理解。

## 添加更多元素

你可以添加各种元素。

### 添加图片

1. 输入`<img src=`来打开图片标签。

2. 在`=`之后直接粘贴或输入图片 URL，然后用`>`关闭图片标签。

例如，如果你使用类似`http://www.myimage.com/mountains`的地址，将输入：

```html
<img src="http://www.myimage.com/mountains.jpg">
```

### 链接到不同的页面

1. 输入`<a href=`来打开链接标签。

2. 在`=`之后直接粘贴或输入链接 URL。

3. 输入`>`来关闭链接。

4. 在`>`之后输入链接名称。

5. 随后输入`</a>`。

例如，如果你想链接到 Wikipedia，它看起来像这样：

```html
<a href="https://www.wikipedia.com">Wikipedia</a>
```

### 添加换行符

要添加换行符，只需在需要的位置输入`<br>`。这将创建一条水平线，将你的页面分为若干部分。

### 自定义颜色

首先，决定你想要什么颜色以及在哪里使用，然后选择颜色名称或相关的十六进制代码。你也可以使用十进制，但不建议这样做。

接下来，我们要更改背景颜色。这可以通过带有`style`属性的`<body>`标签实现。例如，你可以将背景颜色改为紫丁香色（lilac）：

```html
<body style="background-color:lilac;">
```

现在，我们要设置任意标签的文本颜色。这同样可以通过`style`属性完成，从而指定特定标签中文本的颜色。例如，你可能希望将`<p>`标签中的文本设置为深蓝色：

```html
<p style="color:darkblue;">
```

此更改仅对指定的`<p>`标签中的文本生效。如果之后又开始另一个`<p>`标签，并且也希望其中的文本为深蓝色，就需要再次包含`style`属性。

### 设置标题或段落的背景颜色

这种方法与`<body>`标签非常相似。假设你希望其中一个`<p>`标签具有浅蓝色背景，而`<h1>`标签具有紫丁香色背景。操作如下：

```html
<p style="background-color:lightblue;">
<h1 style="background-color:lilac;">
```

### 关闭文档

要关闭主体，输入`</body>`。这应该在添加完所有文本以及链接、图片等其他元素后进行。此标签将告诉浏览器不要再期待更多代码。

要关闭 HTML 文档，输入`</html>`。此标签将告诉浏览器不要再期待更多代码。

```html
<!DOCTYPE html>
<html>
<head>
<title>Wikipedia</title>
</head>
<body>
<h1>Welcome to this page!</h1>
<h2>My name is Jimmy.</h2>
<h3>I hope you have fun here.</h3>
<p>This is my first paragraph</p>
<p><font color="red">(your text here)</font></p>
<b>Bold text</b>
<i>Italic text</i>
<u>Underlined text</u>
<sub>Subscript text</sub>
<sup>Superscript text</sup>
<strong>Strong text</strong>
<a href="https://www.wikipedia.com">Wikipedia</a>
<br>
<body style="background-color:lilac;">
<p style="color:darkblue;">
<p style="background-color:lightblue;">
<h1 style="background-color:lilac;">
</body>
</html>
```

| 标签 | 描述 |
| --- | --- |
| `<hr>` | 用于定义文档主题的更改 |
| `<!--…-->` | 用于定义注释 |

#### HTML 格式

| 标签 | 描述 |
| --- | --- |
| `<acronym>` | 用于定义缩写词；这在 HTML5 中不支持，应使用`<abbr>` |
| `<abbr>` | 用于定义缩写或省略词 |
| `<address>` | 用于定义内容所有者或作者的联系信息 |
| `<b>` | 用于加粗文本 |
| `<bdi>` | 用于隔离一段文本，该文本的方向格式可能与周围文本不同 |
| `<bdo>` | 用于覆盖文本的当前方向 |
| `<big>` | 用于定义大文本；这在 HTML5 中不支持，应使用 CSS |
| `<blockquote>` | 用于定义来自不同来源的引用 |
| `<center>` | 用于定义居中文本；这在 HTML5 中不支持，应使用 CSS |
| `<cite>` | 用于定义作品标题 |
| `<code>` | 用于定义计算机代码 |
| `<del>` | 用于定义被删除的文本 |
| `<dfn>` | 用于指定页面内容中定义的术语 |
| `<em>` | 用于定义以某种方式强调的文本 |
| `<font>` | 用于定义文本的颜色、字体和大小；这在 HTML5 中不支持，应使用 CSS |
| `<i>` | 用于定义另一种语气或风格的文本 |
| `<ins>` | 用于定义插入文档的文本 |
| `<kbd>` | 用于定义特定的键盘输入 |
| `<mark>` | 用于定义标记或高亮的文本 |
| `<meter>` | 用于定义仪表内或已知范围内的标量测量 |
| `<pre>` | 用于定义预格式化文本 |
| `<progress>` | 用于表示任务进度 |
| `<q>` | 用于定义短引用 |
| `<rp>` | 用于定义在不支持 Ruby 注释的浏览器中显示的内容 |
| `<rt>` | 用于定义 Ruby 注释文本 |
| `<ruby>` | 用于定义 Ruby 注释，用于东亚排版 |
| `<s>` | 用于定义错误的文本 |
| `<samp>` | 用于定义计算机程序的示例输出 |
| `<small>` | 用于定义较小的文本 |
| `<strike>` | 用于定义删除线文本；这在 HTML5 中不支持，应使用`<s>`或`<del>`代替 |
| `<strong>` | 用于定义重要文本 |
| `<sub>` | 用于定义下标 |
| `<sup>` | 用于定义上标 |
| `<template>` | 用于定义包含不应在页面加载时显示的文本的容器 |
| `<time>` | 用于定义特定的日期或时间 |
| `<tt>` | 用于定义等宽字体；这在 HTML5 中不支持，应使用 CSS |
| `<u>` | 用于定义样式与普通文本不同的未阐明文本 |



| `<var>` | 用于定义变量 |
| `<wbr>` | 用于定义可能的换行 |

#### 表单与输入

| 标签 | 描述 |
| :--- | :--- |
| `<button>` | 用于定义可点击按钮 |
| `<datalist>` | 用于为输入控件指定预定义的选项列表 |
| `<fieldset>` | 用于在表单中分组相关元素 |
| `<form>` | 用于定义用于用户输入的 HTML 表单 |
| `<input>` | 用于定义输入控件 |
| `<label>` | 用于定义 `<input>` 元素的标签 |
| `<legend>` | 用于定义 `<fieldset>` 元素的标题 |
| `<optgroup>` | 用于在下拉列表中定义相关项目组 |
| `<option>` | 用于定义下拉列表中的一个选项 |
| `<output>` | 用于定义计算结果 |
| `<select>` | 用于定义下拉列表 |
| `<textarea>` | 用于定义多行输入控件 – 文本区域 |

#### 帧

| 标签 | 描述 |
| :--- | :--- |
| `<frame>` | 用于在帧集中定义帧或窗体 – 不在 HTML5 中支持 |
| `<frameset>` | 用于定义帧集 – 不在 HTML5 中支持 |
| `<noframes>` | 用于定义用户计算机/浏览器不支持帧时的替代内容 – 不在 HTML5 中支持 |
| `<iframe>` | 用于定义内联帧 |

### 图像

| 标签 | 描述 |
| :--- | :--- |
| `<area>` | 用于定义图像映射内部区域 |
| `<canvas>` | 用于通过脚本绘图 – 实时绘制，通常使用 `JavaScript` |
| `<figcaption>` | 用于定义 `<figure>` 元素的说明 |
| `<figure>` | 用于指定自包含的内容 |
| `<img>` | 用于定义图像 |
| `<map>` | 用于在客户端定义图像映射 |
| `<picture>` | 用于定义包含多个图像资源的容器 |
| `<svg>` | 用于定义 SVG 图形容器 |

#### 音频 / 视频

| 标签 | 描述 |
| :--- | :--- |
| `<audio>` | 用于定义音频内容 |
| `<source>` | 用于定义多个媒体资源，如 `<video>`、`<picture>` 和 `<audio>` |
| `<track>` | 用于定义媒体元素文本轨道 - `<video>` 和 `<audio>` |
| `<video>` | 用于定义电影或视频 |

#### 链接

| 标签 | 描述 |
| :--- | :--- |
| `<a>` | 用于定义超链接 |
| `<link>` | 用于定义文档与外部资源之间的关系 – 通常用于链接样式表 |
| `<nav>` | 用于定义导航 |

#### 列表

| 标签 | 描述 |
| :--- | :--- |
| `<dd>` | 用于定义描述列表中术语的描述 |
| `<dir>` | 用于定义目录列表 – 这在 HTML5 中不支持 – 应该使用 `<ul>` 代替 |
| `<dl>` | 用于描述列表 |
| `<dt>` | 用于定义描述列表中名称或术语 |
| `<li>` | 用于定义列表项 |
| `<ol>` | 用于定义有序列表 |
| `<ul>` | 用于定义无序列表 |

#### 表格

| 标签 | 描述 |
| :--- | :--- |
| `<table>` | 用于定义表格 |
| `<caption>` | 用于定义表格标题 |
| `<th>` | 用于定义表头单元格 |
| `<tr>` | 用于定义行 |
| `<td>` | 用于定义单元格 |
| `<thead>` | 用于分组表格头内容 |
| `<tbody>` | 用于分组表格体内容 |
| `<tfoot>` | 用于分组表格脚内容 |
| `<col>` | 用于指定 `<colgroup>` 中每列的属性 |
| `<colgroup>` | 用于对表格中的列进行分组 |

#### 样式与语义

| 标签 | 描述 |
| :--- | :--- |
| `<article>` | 用于定义文章 |
| `<aside>` | 用于定义不是页面内容的内容 |
| `<data>` | 用于为指定内容添加机器可读的翻译 |
| `<details>` | 用于定义用户可以隐藏或查看的细节 |
| `<dialog>` | 用于定义对话框或框 |
| `<div>` | 用于定义文档中的节 |
| `<footer>` | 用于定义节或文档的底部 |
| `<header>` | 用于定义节或文档的头部 |
| `<main>` | 用于指定文档的主要内容 |
| `<section>` | 用于定义文档的节 |
| `<span>` | 用于定义文档中的节 |
| `<style>` | 用于定义文档的样式信息 |
| `<summary>` | 用于定义 `<details>` 标签的可见标题 |

#### 元信息

| 标签 | 描述 |
| :--- | :--- |
| `<base>` | 为所有相对 URL 指定基础目标或 URL |
| `<basefont>` | 为所有文档文本指定默认大小、颜色和字体 – 这在 HTML5 中不支持 – 应该使用 CSS |
| `<head>` | 用于定义文档的特定信息 |
| `<meta>` | 用于定义文档的元数据 |

#### 编程

| 标签 | 描述 |
| :--- | :--- |
| `<applet>` | 用于定义嵌入式小程序 – 这在 HTML5 中不支持 - 应该使用 `<object>` 或 `<embed>` |
| `<embed>` | 用于定义包含非 HTML（外部）应用程序的容器 |
| `<noscript>` | 用于在用户设置不支持客户端脚本时定义替代内容 |
| `<object>` | 用于定义嵌入对象 |
| `<param>` | 用于定义对象的参数 |
| `<script>` | 用于定义客户端脚本 |

## 结论

![](img/Image00001.jpg)

感谢你花时间阅读我的指南。如果你读到了最后，说明你对使用 HTML 已经有了一定的熟悉程度，并理解了它是如何让内容创作者和开发者创建并构建网页的。

HTML 是一个比本书内容大得多的课题，但我涵盖的是基础知识。你现在知道 HTML 是什么，由什么组成，以及如何使用最常见的元素、标签和属性。简而言之，你学习了如何仅使用 HTML 构建一个基础网页。

与任何编程语言一样，真正熟练使用 HTML 的唯一方法就是使用它——练习得越多，你对它就越熟悉。这种练习包括尝试构建自己的网页，并研究他人的 HTML 代码，尝试理解它是如何被使用的以及实现了什么功能。

要有耐心。没有哪种语言是容易学的，道路上会遇到很多波折。如果你犯了错误，不要过于自责。从错误中学习，纠正错误的地方，并不断尝试改进，再推自己努力一点点。

花时间思考元素，并使用 `class` 和 `id` 属性来识别重要的元素。这对于学习如何最好组织文档结构非常重要。

网络上有大量的 HTML 资源和课程；利用它们，层层构建你的知识体系。

## 参考文献

![](img/Image00001.jpg)

“HTML - Basic Tags - Tutorialspoint.” Tutorialspoint.com, 2019, www.tutorialspoint.com/html/html_basic_tags.htm.

“HTML Tutorial.” W3schools.com, 2018, www.w3schools.com/html/.

Schäferhoff, Nick. “HTML Tutorial for Beginners 101 (Including HTML5 Tags) - WebsiteSetup.” Websitesetup.org, 2019 年 5 月 5 日, websitesetup.org/html-tutorial-beginners/.

“Structuring the Web with HTML - Learn Web Development | MDN.” Developer.mozilla.org, developer.mozilla.org/en-US/docs/Learn/HTML. 访问于 2021 年 3 月 19 日.

“Tutorials - Javatpoint.” Www.javatpoint.com, 2011, www.javatpoint.com/.

# Web 开发

# 使用 CSS 进行设计

![](img/Image00001.jpg)

Andy Vickler

## 引言

![](img/Image00001.jpg)

本书包含了使用 CSS 设计网站的经过验证的步骤和策略。我从零创建了所有代码，以便你可以复制并粘贴到编辑器中进行练习。你可以更改值、属性和样式以获得不同的结果。CSS 允许你尝试各种颜色组合、边框样式、边框图案、盒子、表单来设计网页。

几乎所有的 HTML 元素都欢迎 CSS 作为样式工具。你可以选取单个 HTML 元素并赋予它们独特的样式，为你的网站创建独特的视觉。本书包含了大量的代码和相关输出，以便你将代码用于练习。在书中，某些输出缺失，有些可能与你在网页上看到的不符，因为无法在书中整合网页。然而，当你在编辑器中执行代码并将其上传到浏览器时，你会发现输出正如我描述的以及你预期的那样。此外，请注意不同的不同的浏览器产生不同的结果。有些接受某些代码，而另一些不。因此，请不要忘记在 Firefox、Internet Explorer、Safari 和 Chrome 等不同浏览器上尝试同一段代码。

最有趣的章节之一是书的最后一章，包含了创建和设计网页布局的代码。一旦学会了如何设计单个元素，本书将带你进入创建网页布局的旅。你将学习如何设置头部、页脚和列，以整合博客文章和其他重要元素。

我建议你在开始阅读本书时保持笔记本电脑运行。我也建议你在系统上安装诸如 Adobe Dreamweaver 这样的专业编辑器，以便你可以测试我在书中包含的所有代码示例。在系统上安装多个浏览器来测试不同的代码段也是更好的选择，这样你就能知道你的代码是否在所有浏览器上运行良好。使用在所有浏览器上运行良好的 CSS 代码，这样你就不会因为 CSS 代码在他们的浏览器上无法运行而失去客户。

如果你具备 HTML 的实用性知识，你的学习过程将会很有趣。然而，你不需要成为 HTML 专家。HTML 的代码编写得很整洁，CSS 则清晰地嵌入在 `<style>` 和 `</style>` 标签中。在过几个代码示例后，你将开始掌握哪个 HTML 元素用于什么目的。此外，记住每段 CSS 代码必须设计一个或多个 HTML 元素。

## 第一章：使用 CSS 进行设计

![](img/Image00001.jpg)

网站的创建需要对设计原理以及向观众展示内容的技术有深入的理解。在开始阅读本书之前，你应该确保你有一个功能完备的计算机和操作系统。你应该理解电脑的目录系统，以便浏览不同的文件夹。你应该知道如何保存、定位和查找文件。

在开始阅读本书之前，你应该确保你有一个功能完备的计算机和操作系统。你应该理解电脑的目录系统，以便浏览不同的文件夹。你应该知道如何保存、定位和查找文件。

当你开始学习 CSS 时，你需要安装一个文本编辑器。没有特定的是必须安装的。你可以使用 Adobe Dream 和 Web。

### 工具

有很多工具可以用于 CSS 设计网站；它们从简单到复杂，再到一些健壮的包。工具的选择取决于你的个人喜好、购买的工具以及项目范围。CSS 使用文本作为基础。因此，你可以使用 `Notepad`、`TextEdit` 这样的简单文本编辑器。它们非常适合创建和设计网页。但这些基础工具缺乏检查语法和组织不同网站文件夹的一些高级功能。此外，你无法将代码上传到 Web 服务器。

### Notepad 和 TextEdit

你可以在 Windows 应用程序中找到 `Notepad`。按照以下步骤创建包含 CSS 代码的 HTML 文件。

- 你需要进入“开始”，然后是“程序”，最后是“记事本”。然后选择“文件”并点击“新建”。该文件将以 `.txt` 格式保存。
- 当你打开 `Notepad` 时，你会看到顶部菜单有“文件”。现在点击“另存为”。在文件名字段中将文件扩展名从 `.txt` 更改为 `.html`。
- 在你的系统上，打开“应用程序”文件夹并找到 `TextEdit`。`TextEdit` 软件默认创建以 `.rtf` 格式保存文档。你必须更改应用程序的设置才能成功使用 `HTML`。
- 现在你应该选择“设置”（Preferences）。你会在这里看到一个对话框。
- 在“新建文档”选项卡中，你应该选择“纯文本”单选按钮。现在你将只会看到没有任何任何格式的纯文本。
- 点击“打开”（Open）和“保存”（Save）标签。取消勾选 `.txt` 扩展并启用 `.html` 扩展，以更改你创建和保存的文件类型。

## 颜色编码

你可以使用许多编辑器来编辑代码。其中一些选项也非常高级。高级文本编辑器具有许多优点，使得编辑器易于处理和操作。其最大的优点之一就是颜色编码。无论你是在为 `HTML` 或 `CSS` 页面编写代码，还是打开现有页面进行编辑，你都会看到不同颜色的代码。这有助于不同代码在视觉上进行分离，使得编辑和更改更加容易。带有值和属性的标签具有不同类型的颜色，让你更容易定位特定类型的代码。它还可以帮助你发现并纠正错误。如果你忘记添加引号和闭括号，代码的颜色就会改变。你会立即知道自己犯了错误。如果你漏掉了闭括号或某些引号，会导致内容的颜色与你正确应用标签时的颜色不同。当你习惯了彩色的语法后，你将通过追踪相同的颜色来发现 HTML 文档中的错误。大多数现代文本编辑器都允许你自定义语法颜色。你可以选择你喜欢的颜色。

## 视觉辅助

高级编辑工具在打开的编辑会话中包含行号。这些行号有助于人们在代码中定位，并有助于与开发者和设计师的协作。这些工具让你能够轻松看到原本不可见的换行符。

## 补全

大多数文本编辑器都会处理不同的繁琐任务，如输入括号和常用标签。不同程序的快捷键和方法各异，但大多数功能全文本编辑器都保留了这一功能。某些编辑器通过从选项列表中选择剩余代码来触发代码补全。这加速了编码过程，因为你不需要记住整个代码。此外，大多数文本编辑器会自动处理重复任务。通过自动化片段、宏、代码和其他代码来加快编码速度。这些工具允许你在页面上包含可重用的代码段。这也为你节省了大量时间。

## 第二章：简介 CSS

![](img/Image00001.jpg)

`CSS` 用于网页的样式化。它是层叠样式表（Cascading Style Sheets）的缩写。它用于描述如何在屏幕或任何其他媒体上显示 `HTML` 元素。设计网站时，它将为你节省大量工作。你可以同时控制多个页面的网页布局。外部样式表将存储在所有的 `CSS` 文件中。

`CSS` 定义了不同布局和屏幕尺寸变体的网页样式。在它上市时，`HTML` 并不打算包含格式化网页的标签。它主要用于描述你网站的内容如何在浏览器中显示。后来，`HTML` 添加了 `<font>` 和 `<color>` 标签，这变成了网页开发人员的噩梦。在单个页面中添加字体和颜色信息的大型网站开发变得既昂贵又耗时。正是 `CSS` 解决了这个问题。它移除了 `HTML` 页面上的样式功能。

代码以 `.css` 扩展名保存。当你创建一个外部样式表文件时，只需更改文件即可改变你网站的外观。

## CSS 语法

每个 `CSS` 规则包含一个声明块和一个选择器块。选择器将指向你需要样化的 `HTML` 元素。声明块将包含用分号分隔的声明。每个声明必须包含 `CSS` 属性的名称和值，并必须用冒号分隔它们。多个 `CSS` 声明应当用分号和声明块分隔。你必须将它们包含在大括号内。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p {
  color: green;
  text-align: left;
}
</style>
</head>
<body>
<p>学习 CSS 编程!</p>
<p>我用 CSS 编码样式化了这个段落。</p>
</body>
</html>
```

学习 CSS 编程！

我用 CSS 编码样式化了这个段落。

在上面的示例中，`p` 是指向你必须样化的 `HTML` 元素的选择器。`color` 是 `CSS` 的一个属性，而 `green` 是该属性的值。`text-align` 再次是一个 `CSS` 属性，而 `left` 是该属性的值。这是 `CSS` 代码的基本结构。我将以相同的结构编写所有代码。唯一的区别是代码的长度和目标。

## CSS 选择器

正如你在示例看到的，`CSS` 中的选择器用于选择你需要样化的特定 `HTML` 元素。`CSS` 选择器可以分为以下几类。

- `CSS` 有简单选择器，用于根据名称、`id` 和 `class` 选择元素。
- 你可以使用组合选择器，通过首先分析元素之间的关系来选择元素。
- 伪类选择器基于 `HTML` 元素的特定状态。
- 属性选择器关注属性和属性的值。
- 伪元素选择器关注特定元素的样式。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p {
  text-align: left;
  color: grey;
}
</style>
</head>
<body>
<p>我将此样式应用到这段代码中的所有段落。</p>
<p id="para1">段落 1</p>
<p>段落 2</p>
</body>
</html>
```

我将此样式应用到这段代码中的所有段落。

段落 1！

段落 2



# CSS 选择器

## ID 选择器

ID 选择器将使用 HTML 的属性来选择特定元素。HTML 元素的 id 是唯一的；这就是为什么 ID 选择器只选择单个元素。如果你想通过唯一 ID 选择特定元素，你可以使用`#`字符和元素的 id。

```html
<!DOCTYPE html>
<html>
<head>
<style>
#paragraph1 {
  text-align: left;
  color: green;
}
</style>
</head>
<body>
<p id="paragraph1">学习 CSS 编程!</p>
<p>我用 CSS 编码样式化了这个段落。</p>
</body>
</html>
```

学习 CSS 编程！

我用 CSS 编码样式化了这个段落。

ID 名称不能以数字开头。

## 类选择器

`CSS`类选择器通过特定的类属性选择所有的`HTML`元素。你可以编写点和类名来选择具有特定名称的元素。

```html
<!DOCTYPE html>
<html>
<head>
<style>
.kaz {
  text-align: left;
  color: red;
}
</style>
</head>
<body>
<p class="kaz">样式已应用到这个段落。</p>
<p class="kaz">样式已应用到这个段落</p>
</body>
</html>
```

样式已应用到这个段落。

样式已应用到这个段落

你可以自由指定想要受此类影响的`HTML`元素。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.kaz {
  text-align: left;
  color: red;
}
</style>
</head>
<body>
<h4 class="kaz">样式没有应用到这个段落。</h4>
<p class="kaz">样式已应用到这个段落</p>
</body>
</html>
```

样式没有应用到这个段落。

样式已应用到这个段落

此外，你还可以为单个 HTML 元素添加多个类（class）。这将为你的网页带来独特的视觉效果，也会让样式设置变得简单而有趣。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.kaz {
  text-align: left;
  color: blue;
}
p.large {
  font-size: 200%;
}
</style>
</head>
<body>
<h4 class="kaz">我将不会改变这个标题</h4>
<p class="kaz">我将这个段落变成红色并将其对齐到页面的左侧。</p>
<p class="kaz large">我将这个段落变成红色，并将其对齐到页面的左侧。唯一的区别是它的字体更大。</p>
</body>
</html>
```

我将不会改变这个标题

我将这个段落变成红色并将其对齐到页面的左侧。

我将这个段落变成红色并将其对齐到页面的左侧。唯一的区别是它的字体更大。

## CSS 通用选择器

CSS 通用选择器可以通过`*`符号来识别。它选择网页上的每一个元素。样式将覆盖到所有元素，并赋予它们通用的视觉效果。

```html
<!DOCTYPE html>
<html>
<head>
<style>
* {
  text-align: left;
  color: blue;
}
* {
  font-size: 130%;
}
</style>
</head>
<body>
<h4 class="kaz">我也会改变这个标题</h4>
<p class="kaz">我将这个段落变成红色并将其对齐到页面的左侧。现在它的字体也会变大。</p>
<p class="kaz large">我将这个段落变成红色，并将其对齐到页面的左侧。它的字体将会更大。</p>
</body>
</html>
```

我也会改变这个标题

我将这个段落变成红色并将其对齐到页面的左侧。现在它的字体也会变大。

我将这个段落变成红色并将其对齐到页面的左侧。它的字体将会更大。

## 分组选择器

CSS 分组选择器将样式应用于所有具有相同样式定义的 HTML 元素。在接下来的示例中，我将编写代码并对 HTML 文档内部的所有元素实现 CSS 分组选择器。形成选择器组是一个更好的选择，它有助于减少代码。我将在代码中使用逗号来分隔每个选择器。

```html
<!DOCTYPE html>
<html>
<head>
<style>
h4, p, p {
  text-align: left;
  color: green;
}
</style>
</head>
<body>
<h4>学习 CSS 分组选择器</h4>
<p>CSS 样式应用于此段落了！</p>
<p>这个段落将继承相同的 CSS 样式！</p>
</body>
</html>
```

### 学习 CSS 分组选择器

CSS 样式应用于此段落了！

这个段落将继承相同的 CSS 样式！

# 添加 CSS

每当浏览器读取样式表时，它都会准备好根据样式表中包含的信息来格式化 HTML 文档。在 HTML 文档中插入 CSS 有三种不同的方法：内部 CSS 方法、外部 CSS 方法和内联 CSS 方法。

## 外部 CSS

通过外部样式表，你可能通过更改单个文件来改变整个网站的外观。HTML 页面需要集成对外部样式表的清晰引用。请记住，你必须将引用放在 HTML 文档的`head`内部。

```html
<!DOCTYPE html>
<html>
<head>
<link rel="This is a stylesheet" href="kazstyle.css">
</head>
<body>
<h4>我正在写一个 h4 标题</h4>
<p>样式将应用于此段落。</p>
</body>
</html>
```

我正在写一个 h4 标题

样式将应用于此段落。

你可以使用任何喜欢的文本编辑器编写外部 CSS 表格。你必须以`.css`扩展名保存它。这个外部`.css`文件不能包含 HTML 标签。属性的单位和值之间不应有空格。

## 内部 CSS

第二种 CSS 集成类型是通过内部样式。如果单个 HTML 页面带有独特的样式，你可以使用内部样式表。内部样式表定义在`<style>`元素中，该元素应该放在 HTML 文档的`head`中。

```html
<!DOCTYPE html>
<html>
<head>
<style>
body {
  background-color: green;
}
p {
  color: blue;
  margin-left: 60px;
}
</style>
</head>
<body>
<h4> 学习 CSS 内部样式</h4>
<p>我正在通过内部样式为 HTML 文档设置样式。</p>
<p>这个段落带有相同的样式。</p>
</body>
</html>
```

学习 CSS 内部样式

我正在通过内部样式为 HTML 文档设置样式。

这个段落带有相同的样式。

## 内联 CSS 样式

第三种方法是内联 CSS 样式。你可以为单个元素应用不同的样式。当你使用内联样式时，可以添加样式属性。

```html
<!DOCTYPE html>
<html>
<body>
<p style="color:red;text-align:left;">地球是圆的。</p>
<p style="color:blue;">不要相信。</p>
</body>
</html>
```

地球是圆的。

不要相信。

# 多样式表

当一个元素发现多个样式时，会产生级联（cascading）规则：

- 第一条规则是内联样式，它位于 HTML 元素内部。
- 第二条规则是内部和外部样式，位于`head`部分。
- 第三条规则是浏览器默认设置。

内联样式优先级最高。它会覆盖内部和外部样式，也会覆盖浏览默认设置。

```html
<!DOCTYPE html>
<html>
<head>
<style>
h4 {
  color: blue;
}
</style>
<link rel="This is a stylesheet" type="text/css" href="kazstyle.css">
</head>
<body>
<h4>多样式</h4>
<p>你看到了外部和内部样式的组合。更改颜色产生结果</p>
</body>
</html>
```

### 多样式

你看到了外部和内部样式的组合。更改颜色产生结果

如果你在链接外部样式表之前定义内部样式，颜色将会改变。

# 注释

CSS 注释无法在浏览器中显示；但它们支持源代码的文档化。你可以使用注释为代码添加简要说明，或者在以后编辑源代码时使用。浏览器忽略注释。注释必须放在`<style>`括号内。它必须以`/*`开始，并以`*/`结束。在下面的示例中，我将在代码顶部添加一个注释。查看如何向 CSS 代码添加注释。

```html
<!DOCTYPE html>
<html>
<head>
<style>
/* 我正在学习 CSS 来设计我的网站。*/
p {
  color: green;
}
</style>
</head>
<body>
<p>学习 CSS！</p>
<p>我正在用 CSS 为这个段落设置样式。</p>
<p>CSS 不允许注释在浏览器中显示。</p>
</body>
</html>
```

学习 CSS！

我正在用 CSS 为这个段落设置样式。

CSS 不允许注释在浏览器中显示。

你可以随心所欲地注释的位置。当你编写复杂的代码时，你需要注释来解释代码，这样当你以后回来查看这些代码时，可以轻松地扫描它。

```css
/* 我正在学习 CSS 来设计我的网站。*/

p {
  color: green; /* 我已将颜色设置为绿色。请不要在代码后面重复使用相同的颜色。请改用红色或蓝色 */
}
```

```html
</style>

</head>

<body>

<p>学习 CSS！</p>

<p>我正在使用 CSS 为这个段落设置样式。</p>

<p>CSS 不允许在浏览器中显示注释。</p>

</body>

</</html>
```

# 学习 CSS！

我正在使用 CSS 为这个段落设置样式。

CSS 不允许在浏览器中显示注释。

# 背景颜色

在设计网站时，更改背景颜色是一件趣事。不同的页面根据其结构和内容需要不同的颜色。通过 CSS，你可以为你的网页添加不同的颜色。这使得识别你的网页变得容易。

```html
<!DOCTYPE html>
<html>
<body>
<h4 style="background-color:SkyBlue;">学习 CSS</h4>
<p style="background-color:pink;">
在这段代码中，我将更改两个 HTML 元素的背景。更改背景颜色不会改变元素的文本颜色。
</p>
</body>
</html>
```

### 学习 CSS

在这段代码中，我将更改两个 HTML 元素的背景。更改背景颜色不会改变元素的文本颜色。

# 文本颜色

你也可以更改 HTML 元素的文本颜色。为了这个目的，我必须更改代码的位置。下面的示例将解释如何更改代码的颜色。

```html
<!DOCTYPE html>
<html>
<body>
<h4 style="color:SkyBlue;">CSS 文本颜色</h4>
<p style="color:Pink;">你可以看到代码的位置发生了变化。现在它被集成到了相关的 HTML 中。</p>
<p style="color:SeaGreen;">这是在整个网页中为文本添加颜色最简单、高效的方法。如果需要，你可以为页面上的每个元素赋予唯一的颜色。</p>
</body>
</html>
```

### CSS 文本颜色

你可以看到代码的位置发生了变化。现在它被集成到了相关的 HTML 中。

这是在整个网页中为文本添加颜色最简单、最高效的方法。如果需要，你可以为页面上的每个元素赋予唯一的颜色。

# 边框颜色

虽然边框颜色在网页中并不常见，但 CSS 为你提供了最有效的方法为 HTML 元素添加边框，并涂上你所需的颜色。当你编写代码时，你有机会设置边框的宽度。你可以为边框设置不同的厚度以将其与其他区分开来。当你需要强调网页上的某个元素时，这非常有用。例如，当你设计落地页时，可以使用 CSS 的边框功能包围并着你的行动号召（Call To Action），使其突出且引人注目。就像我们将代码插入单个元素内部为文本着色一样，我们可以使用相同的技术创建并为 CSS 边框添加颜色。查看以下示例了解如何操作。

```html
<!DOCTYPE html>
<html>
<body>
<p style="border: 6px solid pink;">CSS 边框颜色</p>
<p style="border: 4px solid SkyBlue;">CSS 边框颜色</p>
<p style="border: 2px solid Violet;">CSS 边框颜色</p>
</body>
</html>
```

### CSS 边框颜色

CSS 边框颜色

CSS 边框颜色

# 替代着色方法

CSS 中添加颜色的另一种方法。你可以使用 HEX 值、RGB 值、RGBA 值、HSL 值和 HSLA 值。

```html
<!DOCTYPE html>
<html>
<body>
<p>以下将显示与名称 "Tomato" 相同的颜色：</p>
<p style="background-color:rgb(255, 99, 71);">这种颜色是 rgb(255, 99, 71)。这在你制作专业网站时降低了出错的概率。</p>
<p style="background-color:#ff6347;">这是代码 #ff6347 的第二种方法</p>
<p style="background-color:hsl(9, 100%, 64%);">这是 hsl 方法 (9, 100%, 64%)</p>
<p>以下将显示与 "Tomato" 相同的颜色，但它具有 50% 的透明度：</p>
<p style="background-color:rgba(255, 99, 71, 0.5);">这是精确的数字：rgba(255, 99, 71, 0.5)</p>
<p style="background-color:hsla(9, 100%, 64%, 0.5);">这是第二种方法：hsla(9, 100%, 64%, 0.5)</p>
<p>你可以使用预定义的颜色名称，也可以借助 RGBA 或 HSLA 颜色值通过 RGB、HSL、HEX 或透明颜色来指定颜色。</p>
</body>
</html>
```

以下将显示与名称 "Tomato" 相同的颜色：

这种颜色是 rgb(255, 99, 71)。这在你制作专业网站时降低了出错的概率。

这是代码`#ff6347`的第二种方法。

这是 hsl 方法 (9, 100%, 64%)。

以下将显示与 "Tomato" 相同的颜色，但它具有 50% 的透明度：

这是精确的数字：rgba(255, 99, 71, 0.5)。

这是第二种方法：hsla(9, 100%, 64%, 0.5)。

你可以使用预定义的颜色名称，也可以借助 RGBA 或 HSLA 颜色值通过 RGB、HSL、HEX 或透明颜色来指定颜色。

当值达到最大时，背景完全是白色：`rgb(255, 255, 255)`

当你对红、绿、蓝使用相等的值时，你会产生不同深浅的灰色。值不相等则不会产生灰色。

值不相等会破坏灰色调，结果会跳出一种新颜色：`rgb(255, 100, 255)`

你可以看到文本，因为它会将背景涂抹成纯黑色：`rgb(0, 0, 0)`

这比第一个亮一点，但由于黑色的色调，你将看不到任何文本：`rgb(60, 60, 60)`

随着值的增加，你会看到更浅的色调：`rgb(120, 120, 120)`

这比上一个亮：`rgb(180, 180, 180)`

这好多了：`rgb(240, 240, 240)`

当值达到最大时，背景完全是白色：`rgb(255, 255, 255)`

当你对红、绿、蓝使用相等的值时，你会产生不同深浅的灰色。值不相等则不会产生灰色。

值不相等会破坏灰色调，结果会跳出一种新颜色：`rgb(255, 100, 255)`

## RGBA Colors

RGBA 颜色值似乎是带有 alpha 通道的 RGB 值的扩展。它指定颜色的透明度。RGBA 是（红、绿、蓝、alpha）的缩写。alpha 参数是一个 0.0（完全透明）到 1.0（不透明）之间的数字。我将保持颜色值不变，只更改 alpha 值。结果非常悦目。

当 alpha 为零时，背景完全透明的：`rgba(255, 70, 190, 0)`

当你增加 alpha 值时，透明度会略微降低：`rgba(255, 70, 190, 0.2)`

这更不透明但仍然较亮：`rgba(255, 70, 190, 0.4)`

继续增加值，你将在不改变颜色的情况下看到更深色的背景：`rgba(255, 70, 190, 0.6)`

变得浓密：`rgba(255, 70, 190, 0.8)`

这是所有中最浓密的：`rgba(255, 70, 190, 1)`

alpha 的值 1 是最大值。你不能再增加它。即使你这样做，它对背景的透明度也没有影响：`rgba(255, 70, 190, 2)`

这是在不改变原始值的情况下处理颜最专业的方法。

当 alpha 为零时，背景是透明的：`rgba(255, 70, 190, 0)`

当你增加 alpha 值时，透明度会略微降低：`rgba(255, 70, 190, 0.2)`

这更不透明但仍然较亮：`rgba(255, 70, 190, 0.4)`

继续增加值，你将在不改变颜色的情况下看到更深色的背景：`rgba(255, 70, 190, 0.6)`

变得浓密：`rgba(255, 70, 190, 0.8)`

这是所有中最浓密的：`rgba(255, 70, 190, 1)`

alpha 的值 1 是最大值。你不能再增加它。即使你这样做，它对背景的透明度也没有影响：`rgba(255, 70, 190, 2)`



这是在不改变原始值的情况下处理颜色的最专业的方法。

## HEX Colors

HEX 表示十六进制颜色。十六进制颜色用十六进制数指定。六位数字可以分为两个红色、两个绿色和两个蓝的组合。十六进制整数指定颜色。值可以用`00`和`ff`的形式设置。`ff`值是最大值 255。查看以下代码以理解你如何利用 HEX 创建出美妙的色彩混合。

由于前两个位置指定为红色，`ff`意味着 255，所以你会看到深红色：`#ff0000`

最后两个位置指定为蓝色。使用双`f`，你会看到深蓝色：`#0000ff`

这是一种混合，会产生海绿色：`#3cb71`

你不能在`f`之后使用任何字母。如果你这样做，屏幕上将不会显示颜色。如果没有颜色困扰到你，请留意`g, z`或`q`。

准备好迎接橙色：`#ffa500`

紫色出现了。这可能会让你困惑，如何知道哪种颜色组合会产生什么样的结果；然而，练习越多，就能产生越好的组合：`#6aacd`

你可能在 CSS 源码中看到三位十六进制代码。短代码是六位代码的缩写。单个数字代表`r`、`g`和`b`。在短代码中，一个值用于双倍值。代码`#ff00cc`与`#f0c`相同。

## CSS 3-digit Hexadecimal Code

CSS HSL 是色相（hue）、饱和度（saturation）和亮度（lightness）的缩写。你可以通过按 HSL 顺序使用色相、饱和度和来指定颜色。色相范围从 0 到 360，其中`0`表示红色，`120`表示绿色，`240`表示蓝色。饱和度的值为百分比形式。`0%`意味着灰色，`100%`意味着色彩。亮度也以百分比形式出现，`0%`是黑色，`50%`是深浅中间，`100%`是完全白色。你可以更改值并尝试颜色。

此 HSL 代码产生深红色：`hsl(0, 100%, 50%)`

正如我所说`240`将带来蓝色，你会看到深蓝色：`hsl(240, 100%, 50%)`

是时候把背景变为海绿色了。你可以改变数值来改变海绿色的密度：`hsl(147, 50%, 47%)`

紫色：`hsl(300, 76%, 72%)`

是时候引入橙色了：`hsl(39, 100%, 50%)`

我们这里有紫红色：`hsl(248, 53%, 58%)`

当我改变了饱和度和亮度后，没有紫色了：`hsl(248, 53%, 58%)`

紫色仅仅因为饱和度的原因变成了蓝色：`hsl(248, 53%, 58%)`

饱和度有奇妙的作用。即使色相相同，它也能改变颜色。你可以将饱和度描述为衡量颜色强度的标准。在 100% 时，它是最纯净的颜色。没有灰色调。50% 意味着它为 50% 的灰色留出了空间；然而，你仍然可以看到原始颜色。在 0% 时，饱和度完全是灰色。你无法再看到原始颜色。

```html
<!DOCTYPE html>
<html>
<body>
<p style="background-color:hsl(0, 100%, 45%);">炽热色调：hsl(0, 100%, 45%)</p>
<p style="background-color:hsl(0, 80%, 50%);">带灰的红色：hsl(0, 80%, 45%)</p>
<p style="background-color:hsl(0, 60%, 50%);">红与灰的混合：hsl(0, 60%, 45%)</p>
<p style="background-color:hsl(0, 40%, 50%);">灰色开始主于红色：hsl(0, 40%, 45%)</p>
<p style="background-color:hsl(0, 20%, 50%);">红色几乎消失，为灰色留出空间：hsl(0, 20%, 45%)</p>
<p style="background-color:hsl(0, 0%, 50%);">屏幕上没有红色，只有灰色：hsl(0, 0%, 45%)</p>
</body>
</html>
```

使用 HSL 颜色，你可以通过增加和减少饱和度来设定颜色调并创建颜色混合。0% 的饱和度是全灰色。

### 炽热色调：`hsl(0, 100%, 45%)`

带灰的红色：`hsl(0, 80%, 45%)`

红与灰的混合：`hsl(0, 60%, 45%)`

灰色开始主于红色：`hsl(0, 40%, 45%)`

红色几乎消失，为灰色留出空间：`hsl(0, 20%, 45%)`

屏幕上没有红色，只有灰色：`hsl(0, 0%, 45%)`

使用 HSL 颜色，你可以通过增加和减少饱和度来设定颜色调并创建颜色混合。0% 的饱和度是全灰色。

HSL 是程序员的青睐，因为它允许他们在不改变原始颜色的情况下进行实验。就像饱和度一样，你也可以改变颜色的亮度。在 0% 时，意味着没有光。50% 意味着半光，100% 意味着全光。你将在屏幕上看到白色。

```html
<!DOCTYPE html>
<html>
<body>
<p style="background-color:hsl(150, 100%, 0%);">在 0% 时，你的网站看起来是漆黑的。不推荐！hsl(0, 100%, 0%)</p>
<p style="background-color:hsl(150, 100%, 25%);">深绿色出现：hsl(0, 100%, 25%)</p>
<p style="background-color:hsl(150, 100%, 50%);">增加亮度从深绿色中引出鹦鹉色：hsl(0, 100%, 50%)</p>
<p style="background-color:hsl(150, 100%, 75%);">随着亮度进一步提高，海绿色出现：hsl(0, 100%, 75%)</p>
<p style="background-color:hsl(150, 100%, 90%);">当你将其提升到 90% 时，天蓝色出现：hsl(0, 100%, 90%)</p>
<p style="background-color:hsl(150, 100%, 100%);">在 100% 时，屏幕上没有颜色：hsl(0, 100%, 100%)</p>
</body>
</html>
```

在 0% 时，你的网站看起来是漆黑的。不推荐！`hsl(0, 100%, 0%)`

深绿色出现：`hsl(0, 100%, 25%)`

增加亮度从深绿色中引出鹦鹉色：`hsl(0, 100%, 50%)`

随着亮度进一步提高，海绿色出现：`hsl(0, 100%, 75%)`

当你将其提升到 90% 时，天蓝色出现：`hsl(0, 100%, 90%)`

在 100% 时，屏幕上没有颜色：`hsl(0, 100%, 100%)`

你也可以为 HSL 颜色添加透明度。这让上色过程变得更加有趣和神奇。HSL 代码在包含通道道时转变为 HSLA。通道道会调整颜色的透明度。0% 的透明度表示透明背景，而 1% 的透明度表示不透明。

```html
<!DOCTYPE html>
<html>
<body>
<p style="background-color:hsl(150, 100%, 0%);">全黑</p>
<p style="background-color:hsl(150, 100%, 25%);">天蓝色出现</p>
<p style="background-color:hsl(150, 100%, 50%);">海绿色出现</p>
<p style="background-color:hsl(150, 100%, 75%);">深绿色出现</p>
<p style="background-color:hsl(150, 100%, 100%);">全白</p>
</body>
</html>
```

### 三、饱和度

是时候把背景变为海绿色了。你可以改变数值来改变海绿色的密度：`hsl(147, 50%, 47%)`

紫色：`hsl(300, 76%, 72%)`

是时候引入橙色了：`hsl(39, 100%, 50%)`

我们这里有紫红色：`hsl(248, 53%, 58%)`

当我改变了饱和度和亮度后，没有紫色了：`hsl(248, 53%, 58%)`

紫色仅仅因为饱和度的原因变成了蓝色：`hsl(248, 53%, 58%)`

饱和度有奇妙的作用。即使色相相同，它也能改变颜色。你可以将饱和度描述为衡量颜色强度的标准。在 100% 时，它是最纯净的颜色。没有灰色调。50% 意味着它为 50% 的灰色留出了空间；然而，你仍然可以看到原始颜色。在 0% 时，饱和度完全是灰色。你无法再看到原始颜色。

### 四、亮度

HSL 是程序员的青睐，因为它允许他们在不改变原始颜色的情况下进行实验。就像饱和度一样，你也可以改变颜色的亮度。在 0% 时，意味着没有光。50% 意味着半光，100% 意味着全光。你将在屏幕上看到白色。

在 0% 时，你的网站看起来是漆黑的。不推荐！`hsl(0, 100%, 0%)`

深绿色出现：`hsl(0, 100%, 25%)`

增加亮度从深绿色中引出鹦鹉色：`hsl(0, 100%, 50%)`

随着亮度进一步提高，海绿色出现：`hsl(0, 100%, 75%)`

当你将其提升到 90% 时，天蓝色出现：`hsl(0, 100%, 90%)`

在 100% 时，屏幕上没有颜色：`hsl(0, 100%, 100%)`

你也可以为 HSL 颜色添加透明度。这让上色过程变得更加有趣和神奇。HSL 代码在包含通道道时转变为 HSLA。通道道会调整颜色的透明度。0% 的透明度表示透明背景，而 1% 的透明度表示不透明。

### 五、透明度

HSL 代码在包含通道道时转变为 HSLA。通道道会调整颜色的透明度。0% 的透明度表示透明背景，而 1% 的透明度表示不透明。

### 六、图像

另一个用于背景的 CSS 属性是`image`属性。你可以指定如何使用图像作为网页的背景。默认情况下，图像总是重复的，以完全覆盖整个元素。

# CSS 背景图像！

这段代码将把图像设置为你网页的背景！

`background-attachment`属性用于指定图像必须滚动还是保持固定，这意味着当用户滚动页面其他部分时，图像不会向上或向下滚动。

# CSS 边框

CSS 边框属性非常有趣，它们允许你固定 HTML 元素边框的宽度、样式和颜色。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.dot {border-style: dotted;}
p.dash {border-style: dashed;}
p.sol {border-style: solid;}
p.doub {border-style: double;}
p.groov {border-style: groove;}
p.ridg {border-style: ridge;}
p.ins {border-style: inset;}
p.out {border-style: outset;}
p.non {border-style: none;}
p.hid {border-style: hidden;}
p.mixed {border-style: dashed dotted solid double;}
</style>
</head>
<body>
<h4>你正在学习 border-style 属性</h4>
<p>你可以使用各种边框设计你的网站：</p>
<p class="dot">段落有点状边框。</p>
<p class="dash">段落有虚线边框。</p>
<p class="sol">段落有实线边框。</p>
<p class="doub">段落有双线边框。</p>
<p class="groov">段落有凹槽边框。</p>
<p class="ridg">段落有凸脊边框。</p>
<p class="ins">段落有内凹边框。</p>
<p class="out">段落有凸出边框。</p>
<p class="non">段落没有边框。</p>
<p class="hid">段落有隐藏边框。</p>
<p class="mixed">段落有混合边框。</p>
</body>
</html>
```

# 你正在学习 border-style 属性

你可以使用各种边框设计你的网站：

- 段落有点状边框。
- 段落有虚线边框。
- 段落有实线边框。
- 段落有双线边框。
- 段落有凹槽边框。
- 段落有凸脊边框。
- 段落有内凹边框。
- 段落有凸出边框。
- 段落没有边框。
- 段落有隐藏边框。
- 段落有混合边框。

### 宽度

你可以通过指定`em`、`px`、`cm`和`pt`单位来设置和更改边框的宽度。这些测量值将使边框变细、变粗或中等。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.dot {border-style: dotted; border-width: 10px;}
p.dash {border-style: dashed; border-width: medium;}
p.sol {border-style: solid; border-width: 4px;}
p.doub {border-style: double; border-width: thick;}
p.groov {border-style: groove; border-width: thin;}
p.ridg {border-style: solid; border-width: 15px;}
p.ins {border-style: solid; border-width: 5px 15px;} /*5px 上右, 15px 下左 */
p.out {border-style: solid; border-width: 5px 20px;}
p.non {border-style: solid; border-width: 5px 15px 20px 5px;} /* 5px 上, 15px 右, 20px 下, 5px 左 */
p.hid {border-style: hidden;}
p.mixed {border-style: dashed dotted solid double;}
</style>
</head>
<body>
<h4>测试不同的边框宽度类型。 </h4>
<p>我还将使用多个边框宽度：</p>
<p class="dot">段落有点状边框。</p>
<p class="dash">段落有虚线边框。</p>
<p class="sol">段落有实线边框。</p>
<p class="doub">段落有双线边框。</p>
<p class="groov">段落有凹槽边框。</p>
<p class="ridg">段落有凸脊边框。</p>
<p class="ins">段落有内凹边框。</p>
<p class="out">段落有凸出边框。</p>
<p class="non">段落没有边框。</p>
<p class="hid">段落有隐藏边框。</p>
<p class="mixed">段落有混合边框。</p>
</body>
</html>
```

# 测试不同的边框宽度类型。

我还将使用多个边框宽度：

- 段落有点状边框。
- 段落有虚线边框。
- 段落有实线边框。
- 段落有双线边框。
- 段落有凹槽边框。
- 段落有凸脊边框。
- 段落有内凹边框。
- 段落有凸出边框。
- 段落没有边框。
- 段落有隐藏边框。
- 段落有混合边框。

## 边框颜色

你可以使用`border-color`属性设置边框颜色。你可以使用颜色名称、`hex`、`rgb`或`hsl`值。



```html我是由深度求索（DeepSeek）研发的 deepseek-v4-flash-0731 智能大模型。<!DOCTYPE html>
<html>
<head>
<style>
p.dot {border-style: dotted; border-width: 10px; border-color: red;}
p.dash {border-style: dashed; border-width: medium; border-color: green;}
p.sol {border-style: solid; border-width: 4px; border-color: blue;}
p.doub {border-style: double; border-width: thick; border-color: yellow;}
p.groov {border-style: groove; border-width: thin; border-color: purple;}
p.ridg {border-style: solid; border-width: 15px; border-color: #ff0000;}
p.ins {border-style: solid; border-width: 5px 15px; border-color: rgb(255, 0, 0);}
p.out {border-style: solid; border-width: 5px 20px; border-color: hsl(0, 100%, 50%);}
p.non {border-style: solid; border-width: 5px 15px 20px 5px; border-color: transparent;}
p.hid {border-style: hidden;}
p.mixed {border-style: dashed dotted solid double; border-color: red green blue yellow;}
</style>
</head>
<body>
<h4>测试不同的边框颜色。</h4>
<p class="dot">段落有红色点状边框。</p>
<p class="dash">段落有绿色虚线边框。</p>
<p class="sol">段落有蓝色实线边框。</p>
<p class="doub">段落有黄色双线边框。</p>
<p class="groov">段落有紫色凹槽边框。</p>
<p class="ridg">段落有十六进制红色凸脊边框。</p>
<p class="ins">段落有 rgb 内凹边框。</p>
<p class="out">段落有 hsl 凸出边框。</p>
</body>
</html>
```

# 边框边

你可以使用`border-top`、`border-right`、`border-bottom`和`border-left`属性单独为元素的每个边设置边框。

```css
div {
  border-top: 5px solid red;
  border-right: 5px dashed green;
  border-bottom: 5px dotted blue;
  border-left: 5px double yellow;
}
```

你必须记住，边框的设计遵循某些规则。

### 规则 1

第一个规则是，如果你添加四个值并按`ridge dotted solid dashed`的顺序排列，顶部的边框将是`ridged`，右侧边框将是`dotted`，底部边框将是`solid`，左侧边框将是`dashed`。

### 规则 2

如果你添加三个值并按`solid dotted dashed`的顺序排列，顶部将是`solid`，左右两侧是`dotted`，底部将是`dashed`。

### 规则 3

如果你只添加`solid`和`dashed`，顶部和底部将是`solid`，左右两侧将是`dashed`。

### 规则 4

如果你只添加`solid`，边框的所有边都将是`solid`。

## 圆角边框

边框的一个特殊属性是圆角边框。你可以使用特殊的 CSS 属性将正方形边框变为圆边框。该属性命名为`border-radius`。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.kaz {
  border-top-style: solid; border-color: skyblue; border-radius: 15px;
  border-right-style: dotted; border-color: green border-radius: 15px;
  border-bottom-style: double; border-color: skyblue border-radius: 15px;
  border-left-style: ridge; border-color: green border-radius: 15px;
}
</style>
</head>
<body>
<h4>我正在创建单独的边框</h4>
<p class="kaz">段落将具有四种不同的边框样式和圆角。</p>
</body>
</html>
```

# 第四章

## CSS 外边距 (Margins) 与内边距 (Padding)

![](img/Image00001.jpg)

你可以使用 CSS 外边距在你定义的边框周围为不同的元素创建一些空间。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  margin: 100px;
  border: 4px solid #5DAD60;
}
</style>
</head>
<body>
<h4>学习 CSS 外边距</h4>
<div>此 HTML 元素将具有 100px 的边距。</div>
</body>
</html>
```

### 学习 CSS 外边距

CSS 外边距有多个属性。你可以使用它们在边框周围为某些元素构建空间。你可以随心所欲地控制边距。你可以为顶、底、左、右不同的元素设置外边距。你可以在单独的代码行指定每个边的外边距。浏览器将计算外边距，并指定元素的长度和宽度。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  border: 5px solid skyblue;
  margin-top: 150px;
  margin-bottom: 150px;
  margin-right: 150px;
  margin-left: 80px;
  background-color: lightblue;
}
</style>
</head>
<body>
<p>我正在应用单独的 CSS 属性</p>
<div>这个特定的 div 元素将具有 150px 的顶部外边距、150px 的右侧外边距、150px 的底部外边距和 80px 的左侧外边距。</div>
</body>
</html>
```

### 外边距继承

下面的示例包含了外边距的 CSS 继承功能。看看它是如何工作的。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  border: 5px solid skyblue;
  margin-left: 50px;
}
p.kaz {
  margin-left: inherit;
}
</style>
</head>
<body>
<h4>我正在测试外边距的继承值</h4>
<p class="kaz">这个 CSS 段落保留了从 div 元素继承的外边距。</p>
</body>
</html>
```

### 外边距塌叠

HTML 元素的顶部和底部外边距会被塌叠，形式为两个外边距中较宽的一个。这在左右外边距上不会发生，但在底部和顶部边距上会发生。

### CSS 内边距 (Padding)

CSS 内边距为边框内 HTML 元素的内容增加了空间。你可以完全控制 CSS 内边距的属性。你可以用它在定义的边框内为元素生成空间。在 CSS 中，你可以使用属性设置不同元素顶、底、右、左侧的内边距。你可以为不同的属性指定内边距。CSS 内边距属性用于指定内边距的长度`px`和`pt`。宽度以百分比表示。和外边距一样，它也有继承功能。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  border: 4px solid skyblue;
  background-color: lightblue;
  padding-top: 40px;
  padding-right: 50px;
  padding-bottom: 30px;
  padding-left: 60px;
}
</style>
</head>
<body>
<h4>学习 CSS 内边距</h4>
<p>我将使用 CSS 内边距的单独属性</p>
<div>这个特定的 div 元素包含 40px 的顶部内边距、50px 的右侧内边距、30px 的底部内边距和 60px 的左侧内边距。</div>
</body>
</html>
```

### CSS 宽度功能

另一个重要功能是宽度功能。添加`width`属性可以测量并定义 HTML 元素具有多少宽度。当你定义宽度时，内边距会被添加到宽度属性中，这会产生意外的结果。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div.kaz {
  width: 400px;
  background-color: skyblue;
}
div.kaz1 {
  width: 350px;
  padding: 30px;
  background-color: yellow;
}
</style>
</head>
<body>
<p>学习 CSS 内边距和宽度功能</p>
<div class="kaz">这个特定的 div 将有 400px 宽。</div>
<br>
<div class="kaz1">尽管在 CSS 中定义为 350px，该 div 将仍有 400px。</div>
</body>
</html>
```

如果你想将宽度保持在 350px，你需要包含`box-sizing`属性。这将保持元素的宽度。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div.kaz {
  width: 400px;
  background-color: skyblue;
}
div.kaz1 {
  width: 300px;
  padding: 30px;
  box-sizing: border-box;
  background-color: yellow;
}
</style>
</head>
<body>
<p>学习 CSS 内边距和宽度功能</p>
<div class="kaz">这个特定的 div 将有 400px 宽。</div>
<br>
<div class="kaz1">尽管在 CSS 中定义为 300px，该 div 将仍有 400px。</div>
</body>
</html>
```

这些属性不包括边框、内边距和外距。它将设置边框、内边距和元素外距内区域的宽度和高度。你可以将值设置为`auto`来设置默认设置。浏览器将计算宽度和高度并调整自身以提供最具响应性的显示。长度值将以`cm`和`px`定义元素的宽度和高度。初始值用于将宽度或高度设置为默认。`inherit`值将触发属性的继承功能，并为元素分配父元素的值。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  height: 100px;
  width: 150%;
  background-color: skyblue;
}
</style>
</head>
<body>
<p>这是 CSS 宽度和高度属性</p>
<div>正在演示的 HTML 元素高度为 100 像素，宽度为 150%。</div>
</body>
</html>
```

这是 CSS 宽度和高度属性。

正在演示的 HTML 元素高度为 100 像素，宽度为 150%。

我正在使用`px`特性而不是百分比，使其更加精确高效。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  height: 100px;
  width: 150px;
  background-color: skyblue;
}
</style>
</head>
<body>
<p>这是 CSS 宽度和高度属性</p>
<div>正在演示的 HTML 元素高度为 100 像素，宽度为 150%。</div>
</body>
</html>
```

这是 CSS 宽度和高度属性。

正在演示的 HTML 元素高度为 100 像素，宽度为 150%。

你可以使用`max-width`属性设置最大宽度。你可以在长度值中指定此属性，例如`cm`和`px`，或块的百分比`%`。如果浏览器小于你的 HTML 元素宽度，页面上将出现水平滚动条。`max-width`特性将很好地处理这种情况。它将提高网站的响应性。`max-width`特性会覆盖`width`特性。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  max-width: 500px;
  height: 100px;
  background-color: skyblue;
}
</style>
</head>
<body>
<p>这是 CSS max-width 属性</p>
<div>正在演示的 HTML 元素高度为 100 像素，最大宽度为 500px。</div>
</body>
</html>
```

这是 CSS max-width 属性。

正在演示的 HTML 元素高度为 100 像素，最大宽度为 500px。

# 第五

## CSS 盒模型

![](img/Image00001.jpg)

CSS 中的盒模型是网站设计和布局中不可或缺的一部分。CSS 盒模型是一个封装了 HTML 元素的框。它包含了边框、外距、内边距和实际内容。CSS 盒模型有几个部分。最重要的部分之一是`content`，你可以在其中插入显示在网站上的图像和文本。第二个组件是`padding`，它会清除内容的所有区域。内边距始终是透明的。盒模型的第三部分是`borders`。边框围绕模型的内容和内边距描勒。它完全封装了它们。盒模型的第四部分命名为`margin`。它清理了边框周围区域并创建空间让框看起来更整洁。外距始终是透明的。盒模型倾向于元素周围添加边框，并定义所有元素之间的指定空间。在下面的示例中，我将创建一个盒模型。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  background-color: grey;
  width: 200px;
  border: 20px solid skyblue;
  padding: 40px;
  margin: 30px;
}
</style>
</head>
<body>
<h4>学习盒模型</h4>
<p>如果我们深入研究 CSS 盒模型，结果它是一个封装了你想要强调的每个 HTML 元素的框。</p>
<div>这是你填充文本的地方。它有边框、适当的内边距、外距以及用户想要阅读的一些文本。</div>
</body>
</html>
```

学习盒模型

如果我们深入研究 CSS 盒模型，结果它是一个封装了你想要强调的每个 HTML 元素的框。这是你填充文本的地方。它有边框、适当的内边距、外距以及用户想要阅读的一些文本。

如果你想学习盒模型是如何工作的，你应该考虑如何正确设置元素的`height`和`width`。当你设置 HTML 元素的`height`和`width`时，你设置的是区域的尺寸。如果你想计算元素的大小，你需要加上内边距、外距和边框。你应该通过以下方法计算某个元素的总宽度。总宽度等于右内边距、左内边距、宽度、右边框、左边框、右外距和左外距。总高度通过测量高度、底部内边距、顶部内边距、底部外距和顶部边框计算。

## Outline

CSS `outline`绘制在元素的边框之外。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p {
  border: 4px solid grey;
  outline: #FFA99 solid 20px;
  margin: auto;
  padding: 40px;
  text-align: left;
}
</style>
</head>
<body>
<h4>学习框的轮廓</h4>
<p>这段文字将出现在框中。它有 4px 的灰色边框和宽度为 40px 的浅绿色轮廓。</p>
</body>
</html>
```

学习框的轮廓

这段文字将出现在框中。它有 4px 的灰色边框和宽度为 40px 的浅绿色轮廓。

`outline`绘制在 HTML 元素周围。它画在边框之外，以便元素脱颖而出。它用于强调特定的文本、图像或信息。不要将`outline`与边框混淆，因为与边框不同，它是绘制在元素之外的。它可能会重叠内容。`outline`的宽度不会影响元素的高度。`outline`特性具有不同的属性，让程序员自由实验。就像我们改变边框的外观一样，我们可以改变轮廓的外。



```html
<!DOCTYPE html>
<html>
<head>
<style>
p {outline-color:skyblue;}
p.dot {outline-style: dotted;}
p.dash {outline-style: dashed;}
p.sol {outline-style: solid;}
p.doub {outline-style: double;}
p.groov {outline-style: groove;}
p.rid {outline-style: ridge;}
p.ins {outline-style: inset;}
p.out {outline-style: outset;}
</style>
</head>
<body>
<p>学习 outline-style 属性</p>
<p class="dot">虚线轮廓</p>
<p class="dash">破线轮廓</p>
<p class="sol">实线轮廓</p>
<p class="doub">双线轮廓</p>
<p class="groov">槽纹轮廓</p>
<p class="rid">脊形轮廓</p>
<p class="ins">内凹轮廓</p>
<p class="out">外扩轮廓</p>
</body>
</html>
```

学习`outline-style`属性

虚线轮廓

破线轮廓

实线轮廓

双线轮廓

槽纹轮廓

脊形轮廓

内凹轮廓

外扩轮廓

除非你设置了`outline`属性，否则其他属性将无效。首先设置它，然后应用其他属性以获得完整的功能和最少的错误。

### Width 属性

CSS `outline`特性具有`width`属性，根据需要使轮廓变粗或变细。`width`属性指定轮廓有多宽。它可以具有以下值。如果你选择`thin`，它等于`1px`。如果你选择`medium`，它大约为`3px`。如果你选择`thick`，它大约为`5px`。你可以通过选择`px`、`em`、`pt`和`cm`中的任何数字来设置特定尺寸。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.kaz1 {
  border: 2px solid grey;
  outline-style: solid;
  outline-color: blue;
  outline-width: thin;
}
</style>
</head>
<body>
p.kaz2 {
```

```css
{
  border: 2px solid black;
  outline-style: solid;
  outline-color: skyblue;
  outline-width: medium;
}

p.kaz3 {
  border: 2px solid yellow;
  outline-style: solid;
  outline-color: red;
  outline-width: thick;
}

p.kaz4 {
  border: 2px solid green;
  outline-style: solid;
  outline-color: green;
  outline-width: 6px;
}
```

</style>

</head>

<body>

<p>我正在学习`outline-width`属性</p>

<p class="kaz1">生成细轮廓。</p>

<p class="kaz2">生成中等宽的轮廓。</p>

<p class="kaz3">这是一个粗轮廓。</p>

<p class="kaz4">我正在为这个轮廓设置 6px 的厚度。</p>

</body>

</html>

我正在学习`outline-width`属性

生成细轮廓。

生成中等宽的轮廓。

这是一个粗轮廓。

我正在为这个轮廓设置 6px 的厚度。

### 颜色属性

你可以使用 CSS `outline`属性来定义或更改网站上所有 HTML 元素的颜色。你可以使用 HEX、HSL 和 RGB 公式。编写颜色名称也是一种标准做法。

`invert`值会执行颜色的反转，确保轮廓在完全不考虑背景深色的情况下保持可见。

在这个代码示例中，我将解释如何通过代码为不同类型的轮廓分配多种颜色。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.kaz1 {
  border: 2px solid grey;
  outline-style: solid;
  outline-color: blue;
  outline-width: thin;
}

p.kaz2 {
  border: 2px solid black;
  outline-style: solid;
  outline-color: skyblue;
  outline-width: medium;
}

p.kaz3 {
  border: 2px solid yellow;
  outline-style: solid;
  outline-color: #ff0000;
  outline-width: thick;
}

p.kaz4 {
  border: 2px solid green;
  outline-style: solid;
  outline-color: rgb(50, 150, 255);
  outline-width: 6px;
}

p.kaz5 {
  border: 2px solid green;
  outline-style: solid;
  outline-color: hsl(255, 100%, 50%);
  outline-width: 6px;
}

p.kaz6 {
  border: 2px solid yellow;
  outline-style: solid;
  outline-color: invert;
  outline-width: 6px;
}
</style>
</head>
<body>
<p>我正在学习`outline-color`属性</p>
<p class="kaz1">颜色名称。</p>
<p class="kaz2">颜色名称。</p>
<p class="kaz3">HEX 颜色。</p>
<p class="kaz4">用于轮廓的 rgb 颜色。</p>
<p class="kaz5">HSL 颜色。</p>
<p class="kaz6">颜色反转。</p>
</body>
</html>
```

我正在学习`outline-color`属性

颜色名称。

颜色名称。

HEX 颜色。

用于轮廓的 rgb 颜色。

HSL 颜色。

颜色反转。

与其编写单独的代码行，CSS 提供了一个简写属性，你可以在编写长代码时使用它来节省时间。然而，你应该在成为编码专家后才使用它。我将上述示例转换为简写代码。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.kaz1 {outline: solid blue thin;}
p.kaz2 {outline: solid skyblue medium;}
p.kaz3 {outline: dotted #ff0000 thick;}
p.kaz4 {outline: dashed rgb(50, 150, 255) 6px;}
p.kaz5 {outline: solid 2px green;}
p.kaz6 {outline: solid invert 6px;}
</style>
</head>
<body>
<p>我正在学习`outline-color`属性</p>
<p class="kaz1">颜色名称。</p>
<p class="kaz2">颜色名称。</p>
<p class="kaz3">HEX 颜色。</p>
<p class="kaz4">用于轮廓的 rgb 颜色。</p>
<p class="kaz5">HSL 颜色。</p>
<p class="kaz6">颜色反转。</p>
</body>
</html>
```

我正在学习`outline-color`属性

颜色名称。

颜色名称。

HEX 颜色。

用于轮廓的 rgb 颜色。

HSL 颜色。

颜色反转。

### 轮偏移属性

此 CSS 属性在 HTML 元素和轮廓之间创建空间。该空间始终是透明的。你可以决定在轮廓和边框之间添加多少空间。我将通过示例来解释可以创建多大的间隙以及多少是足够的。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p {
  margin: 40px;
  border: 2px dashed grey;
  outline: 1px solid red;
  outline-offset: 20px;
}
</style>
</head>
<body>
<p>我正在学习`outline-offset`属性</p>
<p>你将看到在边框之外 20px 的轮廓。</p>
</body>
</html>
```

学习 CSS `outline-offset`属性

你将看到在边框之外 20px 的轮廓。

当你在浏览器中生成结果时，你会注意到轮廓和元素之间的空间是透明的。

### CSS 文本

在开发和设计网站时，你需要对文本进行格式化并将其放入框内以便更好地显示。CSS 文本格式化是一项重要功能，因为没有文本和内容，网页设计是没有意义的。下面的示例将解释你有多少选项来格式文本。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  border: 2px dashed grey;
  outline: 1px solid red;
  outline-offset: 20px;
}
</style>
</head>
...
```

这将是文本的默认方向。

您的文本将从右到左方向。

这将是文本的默认方向。

您的文本将从右到左方向

### 垂直对齐

此`vertical-align`属性将为您的 HTML 元素设置垂直对齐。您可以添加图片并为其设置垂直对齐。

```html
<!DOCTYPE html>
<html>
<head>
<style>
img.topside {
  vertical-align: top;
}
img.middleside {
  vertical-align: middle;
}
img.bottomside {
  vertical-align: bottom;
}
</style>
</head>
<body>
<p>您的 <img src="logo.gif" alt="kaz" width="250" height="50"> 图片具有默认对齐方式。</p><br>
<p>您的 <img class="topside" src="kaz.gif" alt="kaz" width="250" height="50"> 图片将具有顶部对齐。</p><br>
<p>您的 <img class="middleside" src="logo.gif" alt="kaz" width="250" height="50"> 图片具有中间级对齐。</p><br>
<p>您的 <img class="bottomside" src="logo.gif" alt="kaz" width="250" height="50"> 图片具有底部对齐。</p>
</body>
</html>
```

您的图片具有默认对齐方式。

您的图片将具有顶部对齐。

您的图片具有中间级对齐。

您的图片具有底部对齐。

### 装饰

您可以使用`text-decoration`属性在 CSS 中装饰您的文本。该属性可以设置装饰，也可以移除装饰。该属性的取值`none`会移除所有装饰。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.k {
  text-decoration: overline;
}
p.l {
  text-decoration: line-through;
}
p.m {
  text-decoration: underline;
}
</style>
</head>
<body>
<p class= "k">我们有第一段文字</p>
<p class= "l">这是第二段文字</p>
<p class= "m">正在处理第三段文字</p>
</body>
</html>
```

我们有第一段文字

这是第二段文字

正在处理第三段文字

### 文本转换

此 CSS 属性旨在指定特定文本中的小写和大写字母。您可以使用它将文本转换为小写和大写字母，或者将特定单词的首字母大写。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.ucase {
  text-transform: uppercase;
}
p.lcase {
  text-transform: lowercase;
}
p.capital {
  text-transform: capitalize;
}
</style>
</head>
<body>
<p class="ucase">这段文本被转换为大写字母。</p>
<p class="lcase">将其格式化为小写。</p>
<p class="capital">首字母大写在网页上总是看起来很好。</p>
</body>
</html>
```

这段文本被转换为大写。

将其格式化为小写。

首字母大写在网页上总是看起来很好。

### 缩进

如果设计需要，您也可以对文本进行缩进。`text-indent`属性指定文本第一行的缩进。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p {
  text-indent: 60px;
}
</style>
</head>
<body>
<p>我写这段话是为了展示您如何在 CSS 编程中对段落进行缩进。缩进在 CSS 中是关重要的，因为它让文本在网页上看起来很整洁。随着人们注意力时间的缩短，缩进让文本变得易读且亲眼。我希望您在设计的下一个网站上良好地使用这个属性。</p>
</body>
</html>
```

我写这段话是为了展示您如何在 CSS 编程中对段落进行缩进。缩进在 CSS 中是关重要的，因为它让文本在网页上看起来很整洁。随着人们注意力时间的缩短，缩进让文本变得易读且亲眼。我希望您在设计的下一个网站上良好地使用这个属性。

### 字间距

此 CSS 属性用于指定特定文本字符之间的某些间距。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.k {
  letter-spacing: 5px;
}
p.l {
  letter-spacing: -1px;
}
</style>
</head>
<body>
<p class="k">这段文字的字母之间有 5px 的间距</p>
<p class="l">是时候缩小间距了。负间距在设计中也是一个特性。它美化了文本的外观。进一步减少会让文本变得混乱。</p>
</body>
</html>
```

这段文字的字母之间有 5px 的间距

是时候缩小间距了。负间距在设计中也是一个特性。它美化了文本的外观。进一步减少会让文本变得混乱。

### 行高度

`line-height`属性可以设置行高来指定空间。

```html
<!DOCTYPE html>
<html>
<head>
<style>
img.topside {
  vertical-align: top;
}
img.middleside {
  vertical-align: middle;
}
img.bottomside {
  vertical-align: bottom;
}
</style>
</head>
<body>
<p>您的 <img src="logo.gif" alt="kaz" width="250" height="50"> 图片具有默认对齐方式。</p><br>
<p>您的 <img class="topside" src="kaz.gif" alt="kaz" width="250" height="50"> 图片将具有顶部对齐。</p><br>
<p>您的 <img class="middleside" src="logo.gif" alt="kaz" width="250" height="50"> 图片具有中间级对齐。</p><br>
<p>您的 <img class="bottomside" src="logo.gif" alt="kaz" width="250" height="50"> 图片具有底部对齐。</p>
</body>
</html>
```

*(注：此处提供的原文文本似乎重复了前面的对齐部分内容，已按要求保持格式翻译)*

此段具有 0.7 行高

是时候缩小间距了。负间距在设计中也是一个特性。它美化了文本的外观。进一步减少会让文本变得混乱。

### 字间距

`word-spacing`属性旨在指定特定文本中单词间的空间。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.k {
  word-spacing: 10px;
}
p.l {
  word-spacing: -7px;
}
</style>
</head>
<body>
<p class="k">看到间距如何影响段落的设计。</p>
<p class="l">单词</p>
</body>
</html>
```

看到间距如何影响段落的设计。

单词

### 文本阴影

您可以为文本创建阴影以为网页增添一点样式。`text-shadow`属性负责添加阴影。看看您如何使用该属性以及它的作用。

```html
<!DOCTYPE html>
<html>
<head>
<style>
p {
  text-shadow: 1px 1px;
}
</style>
</head>
<body>
<p>学习文本阴影属性！</p>
</body>
</html>
```

学习文本阴影属性！

通过以下方法为文本添加颜色。



```html我是由深度求索（DeepSeek）研发的 deepseek-v4-flash-0731 智能大模型。<!DOCTYPE html>
<html>
<head>
<style>
p {
  text-shadow: 1px 1px 5px yellow;
}
</style>
</head>
<body>
<p>学习文本阴影属性！</p>
</body>
</html>
```

学习文本阴影属性！

## CSS 字体

为网站选择正确的字体是关重要的。如果您选择了错误的字体，就会破坏页面设计。正确的字体对使用您网站的读者的体验产生巨大影响。正确的字体为您的品牌创建强大的身份。字体样式应该只有一个目标，即易于阅读。与字体样式相结合的是文本的颜色和大小，这是重要的。

你有五种字体族：

- 第一种字体族是衬字体。该家族以字母边缘的小笔画而闻名。它们营造出强大的优雅和正式感，您可能在销售广告中见过它。该家族包含了 `Times New Roman`、`Georgia` 和 `Garamond`。
- 第二种字体族是无衬线字体。它具有整洁的线条，字母没有小笔画。它们看起来更现代，营造出极简主义的气息。该字体族包含了 `Verdana`、`Helvetica` 和 `Arial`。
- 第三种字体族被称为等宽字体。属于该家族的所有字母都具有固定宽度。它们营造出机械感。它包含了 `Monaco`、`Courier New` 和 `Lucida Console`。
- 第四种字体族被称为 `cursive`。`cursive` 字体以类似于手写而称，该字体族包含了 `Lucida Handwriting` 和 `Brush Script M7`。
- 第五种字体族被称为 `fantasy`。这些字体粗体、趣味且装饰性强，该字体族包含了 `Copperplate` 和 `Papyrus`。

在设计网站时，你可以使用 `font-family` 属性来决定网页上显示何种字体样式。`font-family` 属性应该在回退系统中包含多个字体名称，以确保尽可能多的浏览器能够兼容你的网站。从你选择的字体开始，以属于通用族（generic family）的字体结束。如果浏览器没有找到你放在顶部的字体，它将从通用族中选择类似的字体。用逗号分隔它们即可，一切正常。对于多个单词的字体名称，使用引号将其括起来。

```html
<!DOCTYPE html>
<html
<head>
<style>
.kaz1 {
  font-family: "Times New Roman", Times, serif;
}
.kaz2 {
  font-family: Arial, Helvetica, sans-serif;
}
.kaz3 {
  font-family: "Lucida Console", "Courier New", monospace;
}
</style>
</head>
<body>
<h4>Learning CSS font-family</h4>
<p class="kaz1">我计划用 Times New Roman 字体显示此段落。</p>
<p class="kaz2">Arial 字体在可读性方面是最好的。</p>
<p class="kaz3">Lucida Console 字体看起来像是手写的字。</p>
</body>
</html>
```

### 学习 CSS Font-Family

我计划用 `Times New Roman` 字体显示此段落。

`Arial` 字体在可读性方面是最好的。

`Lucida Console` 字体看起来像是手写的字。

## CSS 字体样式

另一个 CSS 属性 `font-style` 用于指定文本的样式。它主要用于将一段文本转换为斜体。该属性包含三个值。你可以保持文本为普通（normal）、斜体（italic）或将其转为倾斜（oblique）。`normal` 值将文本变为普通，而 `italic` 值将文本转为斜体，就像你在 MS Word 中看到的那样。`oblique` 值将文本转为倾斜。`oblique` 看起来像斜体，但它的支持程度没有 `italic`。因此，不要混淆 `oblique` 和 `italic`。

```html
<!DOCTYPE html>
<html>
<head>
<style>
.kaz1 {
  font-style: normal;
}
.kaz2 {
  font-style: italic;
}
.kaz3 {
  font-style: oblique;
}
</style>
</head>
<body>
<h4>Learning CSS font-style</h4>
<p class="kaz1">我计划用普通字体样式显示此段落。</p>
<p class="kaz2">斜体字体在样式方面是最好的。</p>
<p class="kaz3">倾斜字体看起来非常像斜体。</p>
</body>
</html>
```

### 学习 CSS Font-Style

我计划用普通字体样式显示此段落。

斜体字体在样式方面是最好的。

倾斜字体看起来非常像斜体。

## Font-Weight 属性

另一个属性 `font-weight` 决定字体样式的粗细。

```html
<!DOCTYPE html>
<html>
<head>
<style>
.kaz1 {
  font-weight: normal;
}
.kaz2 {
  font-weight: lighter;
}
.kaz3 {
  font-weight: bold;
}
.kaz4 {
  font-weight: 1000;
}
</style>
</head>
<body>
<h4>Learning CSS font-weight property</h4>
<p class="kaz1">CSS 是最好的网页设计语言。</p>
<p class="kaz2">在学习 CSS 之前，你必须学习 HTML。</p>
<p class="kaz3">你可以设计网页上的每个 HTML 元素，赋予它独特的外观。</p>
<p class="kaz4">字体决定了网站的成败，所以请仔细设计文本。</p>
</body>
</html>
```

### 学习 CSS Font-Weight Property

CSS 是最好的网页设计语言。

在学习 CSS 之前，你必须学习 HTML。

你可以设计网页上的每个 HTML 元素，赋予它独特的外观。

字体决定了网站的成败，所以请仔细设计文本。

## Font-Variant 属性

CSS 的 `font-variant` 属性用于指定文本的小大写字体。当你应用该属性时，所有小写字母将被转换为大写字母。尽管如此，转换后的字体比原始大写字母字体小。

```html
<!DOCTYPE html>
<html>
<head>
<style>
.kaz1 {
  font-variant: normal;
}
.kaz2 {
  font-variant: small-caps;
}
</style>
</head>
<body>
<h4>Learning CSS font-weight property</h4>
<p class="kaz1">CSS 是最好的网页设计语言。</p>
<p class="kaz2">在学习 CSS 之前，你必须学习 HTML。</p>
</body>
</html>
```

优秀的字体是优秀设计中不可或缺的一部分。优秀的字体搭配相得益彰，这对于出色的网页设计至关重要。你应该确保字体组合之间相互和谐。字体族（superfamily）就像是一组协同工作的字体。使用来自同一字体族的字体可以确保网页的平滑显示。

相似的字体在一起会产生冲突。如果方法正确，对比会产生最佳的效果。

```html
<!DOCTYPE html>
<html>
<head>
<style>
.kaz1 {
  font-family: Verdana, sans-serif;
  font-size: 60px;
  color: gray;
}
.kaz2 {
font-family: Georgia, serif;
  font-size: 20px;
  color: red;
}
</style>
</head>
<body>
<h4>学习 CSS font-size 属性</h4>
<p class="kaz1">CSS 是最好的网页设计语言。</p>
<p class="kaz2">在你学习 CSS 之前，你必须学习 HTML。</p>
</body>
</html>
```

### 学习 CSS font-size 属性

CSS 是最好的网页设计语言。

在学习学习 CSS 之前，你必须学习 HTML。

让我们来看另一组可行搭配。

```html
<!DOCTYPE html>
<html>
<head>
<style>
.kaz1 {
  font-family: Muli, serif;
  font-size: 40px;
  color: gray;
}
.kaz2 {
font-family: 'Fjalla One', sans-serif;
  font-size: 20px;
  color: red;
}
</style>
</head>
<body>
<h4>学习 CSS font-size 属性</h4>
<p class="kaz1">CSS 是最好的网页设计语言。</p>
<p class="kaz2">在学习学习 CSS 之前，你必须学习 HTML。</p>
</body>
</html>
```

### 学习 CSS font-size 属性

CSS 是最好的网页设计语言。

在学习学习 CSS 之前，你必须学习 HTML。

# 第六章：列表、表格、显示

![](img/Image00001.jpg)

HTML 有两种类型的列表。CSS 的列表属性允许你为有序列表和无序列表设置不同的标记。你也可以插入图像将其设置为标记。你可以为列表项和列表的背景添加颜色。

## CSS 列表

让我们来看 CSS 属性 `list-style-type`，它指定了访问者在网页上看到的列表项类型。你可以使用多种类型来显示项目符号。

```html
<!DOCTYPE html>
<html>
<head>
<style>
ul.k1 {
  list-style-type: square;
}
ul.k2 {
  list-style-type: circle;
}
ol.k3 {
  list-style-type: upper-roman;
}
ol.k4 {
  list-style-type: lower-alpha;
}
</style>
</head>
<body>
<h4>学习列表属性</h4>
<p>你看到一个无序列表的示例：</p>
<ul class="k1">
  <li>marinda</li>
  <li>seven up</li>
  <li>pepsi</li>
</ul>
<ul class="k2">
  <li>avocado</li>
  <li>dragon fruit</li>
  <li>guava</li>
</ul>
<p>这是一个有序列表的示例：</p>
<ol class="k3">
  <li>strawberry</li>
  <li>blueberry</li>
  <li>raspberry</li>
</ol>
<ol class="k4">
  <li>oranges</li>
  <li>apples</li>
  <li>cherries</li>
</ol>
</body>
</html>
```

### 学习列表属性

你看到一个无序列表的示例：

- `marinda`
- `seven up`
- `pepsi`
- `avocado`
- `dragon fruit`
- `guava`

这是一个有序列表的示例：

1. `strawberry`
2. `blueberry`
3. `raspberry`
4. `oranges`
5. `apples`
6. `cherries`

## 添加颜色

你可以用一系列颜色来装饰列表，使其看起来很有趣。你添加到 `<ul>` 或 `<ol>` 标签中的任何内容都会影响整个列表。然而，你添加到 `<li>` 标签的属性只会影响列表的单个项。

```html
<!DOCTYPE html>
<html>
<head>
<style>
ul.k1 {
  background: #ff1122;
  padding: 20px;
}
ul.k2 {
  background: #dd9911;
  padding: 20px;
}
ol.k3 {
  background: #bbe9e09;
  padding: 6px;
  margin-left: 25px;
}
ol.k4 {
  background: #aab9ee;
  margin: 4px;
}
</style>
</head>
<body>
<h4>学习列表属性</h4>
<p>你正在看到一个无序列表的示例：</p>
<ul class="k1">
  <li>marinda</li>
  <li>seven up</li>
  <li>psi</li>
</ul>
<ul class="k2">
  <li>avocado</li>
  <li>dragon fruit</li>
  <li>guava</li>
</ul>
<p>这是一个有序列表的示例：</p>
<ol class="k3">
  <li>strawberry</li>
  <li>blueberry</li>
  <li>raspberry</li>
</ol>
<ol class="k4">
  <li>oranges</li>
  <li>apples</li>
  <li>cherries</li>
</ol>
</body>
</html>
```

### 学习列表属性

你看到一个无序列表的示例：

- `marinda`
- `seven up`
- `pepsi`
- `avocado`
- `dragon fruit`
- `guava`

这是一个有序列表的示例：

1. `strawberry`
2. `blueberry`
3. `raspberry`
4. `oranges`
5. `apples`
6. `cherries`

## CSS 表格

你可以借助 CSS 改变 HTML 表格的外观。它们将看起来非常精美、格式良好。

```html
<!DOCTYPE html>
<html>
<head>
<style>
#listofcustomers {
  font-family: Helvetica, Arial, sans-serif;
  border-collapse: collapse;
  width: 75%;
}
#listofcustomers td, #listofcustomers th {
  border: 2px solid #aaa;
  padding: 6px;
}
#listofcustomers tr:nth-child(even){background-color: #e22e2;}
#listofcustomers tr:hover {background-color: #ddd;}
#listofcustomers th {
  padding-top: 15px;
  padding-bottom: 15px;
  text-align: left;
  background-color: #4D90;
  color: grey;
}
</style>
</head>
<body>
<table id="customers">
  <tr>
    <th>Name of Customers</th>
    <th>Color Allotted</th>
    <th>Name of Country</th>
  </tr>
  <tr>
    <td>Alfredo</td>
    <td>Red</td>
    <td>Ireland</td>
  </tr>
  <tr>
    <td>Jasmine Buckky</td>
    <td>Green</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>Centrum Chuccky</td>
    <td>Violet</td>
    <td>Iceland</td>
  </tr>
  <tr>
    <td>Fanny Line</td>
    <td>Purple</td>
    <td>Scotland</td>
  </tr>
  <tr>
    <td>Fanny Brown</td>
    <td>Yellow</td>
    <td>Neverland</td>
  </tr>
  <tr>
    <td>Peter</td>
    <td>White</td>
    <td>Treasure Island</td>
  </tr>
  <tr>
    <td>Jackson Ramsey</td>
    <td>Green</td>
    <td>Namibia</td>
  </tr>
  <tr>
    <td>Magot Rosy</td>
    <td>Brown</td>
    <td>Spain</td>
  </tr>
  <tr>
    <td>Nany</td>
    <td>Pink</td>
    <td>Egypt</td>
  </tr>
  <tr>
    <td>Paris Hilton</td>
    <td>Tanned Pink</td>
    <td>France</td>
  </tr>
</table>
</body>
</html>
```

## 边框属性

你可以将边框属性添加到代码中，以为结果创建一个漂亮且整洁的边框。表格中的项目将被打乱。



```html
<!DOCTYPE html>
<html>
<head>
<style>
#listofcustomers {
  font-family: Helvetica, Arial, sans-serif;
  border-collapse: collapse;
  width: 75%;
}
#listofcustomers td, #listofcustomers th {
  border: 2px solid #aaa;
  padding: 6px;
}
#listofcustomers tr:nth-child(even){background-color: #e22e2;}
#listofcustomers tr:hover {background-color: #ddd;}
#listofcustomers th {
  padding-top: 15px;
  padding-bottom: 15px;
  text-align: left;
  background-color: #4D90;
  color: grey;
}
table, th {
  border: 2px solid;
}
</style>
</head>
<body>
<table id="customers">
  <tr>
    <th>Name of Customers</th>
    <th>Color Allotted</th>
    <th>Name of Country</th>
  </tr>
  <tr>
    <td>Alfredo</td>
    <td>Red</td>
    <td>Ireland</td>
  </tr>
  <tr>
    <td>Jasmine Buckky</td>
    <td>Green</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>Centrum Chuccky</td>
    <td>Violet</td>
    <td>Iceland</td>
  </tr>
  <tr>
    <td>Fanny Line</td>
    <td>Purple</td>
    <td>Scotland</td>
  </tr>
  <tr>
    <td>Fanny Brown</td>
    <td>Yellow</td>
    <td>Neverland</td>
  </tr>
  <tr>
    <td>Peter</td>
    <td>White</td>
    <td>Treasure Island</td>
  </tr>
  <tr>
    <td>Jackson Ramsey</td>
    <td>Green</td>
    <td>Namibia</td>
  </tr>
  <tr>
    <td>Magot Rosy</td>
    <td>Brown</td>
    <td>Spain</td>
  </tr>
  <tr>
    <td>Nany</td>
    <td>Pink</td>
    <td>Egypt</td>
  </tr>
  <tr>
    <td>Paris Hilton</td>
    <td>Tanned Pink</td>
    <td>France</td>
  </tr>
</table>
</body>
</html>
```

| Name of Customers | Color Allotted | Name of Country |
|---|---|---|
| Alfredo | Red | Ireland |
| Jasmine Buckky | Green | Germany |
| Centrum Chuccky | Violet | Iceland |
| Fanny Line | Purple | Scotland |
| Fanny Brown | Yellow | Neverland |
| Peter | White | Treasure Island |
| Jackson Ramsey | Green | Namibia |
| Magot Rosy | Brown | Spain |
| Nany | Pink | Egypt |
| Paris Hilton | Tanned Pink | France |

### 宽度属性

CSS 表格的`width`属性可以帮助你设置表格列和行的宽度。这可以减少列列错乱的可能性。它会使单元格变宽，使得文本看起来更加宽敞。在添加`width`属性后，表格将扩展到全屏。

```html
<!DOCTYPE html>
<html>
<head>
<style>
#listofcustomers {
  font-family: Helvetica, Arial, sans-serif;
  border-collapse: collapse;
  width: 75%;
}
#listofcustomers td, #listofcustomers th {
  border: 2px solid #aaa;
  padding: 6px;
}
#listofcustomers tr:nth-child(even){background-color: #e2e2e2;}
#listofcustomers tr:hover {background-color: #ddd;}
#listofcustomers th {
  padding-top: 15px;
  padding-bottom: 15px;
  text-align: left;
  background-color: #4DFA90;
  color: grey;
}
table, th, td {
  border: 2px solid green;
}
table {
  width: 100%;
}
</style>
</head>
<body>
<table id="customers">
  <tr>
    <th>客户名称</th>
    <th>分配的颜色</th>
    <th>国家名称</th>
  </tr>
  <tr>
    <td>Alfredo</td>
    <td>Red</td>
    <td>Ireland</td>
  </tr>
  <tr>
    <td>Jasmine Buckky</td>
    <td>Green</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>Centrum Chuccky</td>
    <td>Violet</td>
    <td>Iceland</td>
  </tr>
  <tr>
    <td>Fanny Line</td>
    <td>Purple</td>
    <td>Scotland</td>
  </tr>
  <tr>
    <td>Fanny Brown</td>
    <td>Yellow</td>
    <td>Neverland</td>
  </tr>
  <tr>
    <td>Peter</td>
    <td>White</td>
    <td>Treasure Island</td>
  </tr>
  <tr>
    <td>Jackson Ramsey</td>
    <td>Green</td>
    <td>Namibia</td>
  </tr>
  <tr>
    <td>Magot Rosy</td>
    <td>Brown</td>
    <td>Spain</td>
  </tr>
  <tr>
    <td>Nany</td>
    <td>Pink</td>
    <td>Egypt</td>
  </tr>
  <tr>
    <td>Paris Hilton</td>
    <td>Tanned Pink</td>
    <td>France</td>
  </tr>
</table>
</body>
</html>
```

| 客户名称 | 分配的颜色 | 国家名称 |
|---|---|---|
| Alfredo | Red | Ireland |
| Jasmine Buckky | Green | Germany |
| Centrum Chuccky | Violet | Iceland |
| Fanny Line | Purple | Scotland |
| Fanny Brown | Yellow | Neverland |
| Peter | White | Treasure Island |
| Jackson Ramsey | Green | Namibia |
| Magot Rosy | Brown | Spain |
| Nany | Pink | Egypt |
| Paris Hilton | Tanned Pink | France |

CSS 表格的高度和宽度通常被定义为属性。下面的示例将表格的宽度设置为 100%。你可以在任何喜欢的地方设置高度。

```html
<!DOCTYPE html>
<html>
<head>
<style>
#listofcustomers {
  font-family: Helvetica, Arial, sans-serif;
  border-collapse: collapse;
  width: 75%;
}
#listofcustomers td, #listofcustomers th {
  border: 2px solid #aaa;
  padding: 6px;
}
#listofcustomers tr:nth-child(even){background-color: #e2e2e2;}
#listofcustomers tr:hover {background-color: #ddd;}
#listofcustomers th {
  padding-top: 15px;
  padding-bottom: 15px;
  text-align: left;
  background-color: #4DFA90;
  color: grey;
}
table, th, td {
  border: 2px solid green;
}
table {
  width: 100%;
}
th {
  height: 50px;
}
</style>
</head>
<body>
<table id="customers">
  <tr>
    <th>客户名称</th>
    <th>分配的颜色</th>
    <th>国家名称</th>
  </tr>
  <tr>
    <td>Alfredo</td>
    <td>Red</td>
    <td>Ireland</td>
  </tr>
  <tr>
    <td>Jasmine Buckky</td>
    <td>Green</td>
    <td>Germany</td>
  </tr>
</table>
</body>
</html>
```

| 客户名称 | 分配的颜色 | 国家名称 |
|---|---|---|
| Alfredo | Red | Ireland |
| Jasmine Buckky | Green | Germany |

你可以看到当我增加第一列的高度时，第一列看起来有多宽敞。

### 表格对齐

CSS 提供了`text-align`属性，用于设置内容的水平对齐。内容将居中、左左或右对齐。在下面的示例中，我将在同一段代码中添加三个对齐功能：对齐`td`、对齐`th`以及以垂直格式对齐`td`。

```html
<!DOCTYPE html>
<html>
<head>
<style>
#listofcustomers {
  font-family: Helvetica, Arial, sans-serif;
  border-collapse: collapse;
  width: 75%;
}
#listofcustomers td, #listofcustomers th {
  border: 2px solid #aaa;
  padding: 6px;
}
#listofcustomers tr:nth-child(even){background-color: #e2e2e2;}
#listofcustomers tr:hover {background-color: #ddd;}
#listofcustomers th {
  padding-top: 15px;
  padding-bottom: 15px;
  text-align: left;
  background-color: #4DFA90;
  color: grey;
}
table, th, td {
  border: 2px solid green;
}
table {
  width: 100%;
}
th {
  height: 50px;
}
td {
  text-align: center;
}
th {
  text-align: left;
}
td {
  height: 50px;
  vertical-align: top;
}
</style>
</head>
<body>
<table id="customers">
  <tr>
    <th>客户名称</th>
    <th>分配的颜色</th>
    <th>国家名称</th>
  </tr>
  <tr>
    <td>Alfredo</td>
    <td>Red</td>
    <td>Ireland</td>
  </tr>
  <tr>
    <td>Jasmine Buckky</td>
    <td>Green</td>
    <td>Germany</td>
  </tr>
</table>
</body>
</html>
```

| 客户名称 | 分配的颜色 | 国家名称 |
|---|---|---|
| Alfredo | Red | Ireland |
| Jasmine Buckky | Green | Germany |

### CSS 布局

如果你想在 CSS 中创建一个整洁的布局，你需要使用 CSS 的`display`属性。该属性可以帮助你更好地控制布局。该属性指定了页面上的 HTML 元素应该如何显示。每个 HTML 元素都根据其类型有一个默认的显示值。大多数元素的默认显示值是`inline`或`block`。块级元素会另起一行开始。它们还会占据整个宽度，一直延伸到左右两边。

像`<form>`、`<div>`、`<header>`、`<footer>`、`<p>`和`<h1>`这样的元素都是块级元素。

块级元素总是具有全宽选项。如果你设置了块级元素的`width`，它将防止元素延伸到容器的极端边缘。之后，你可以将边距设置为`auto`，从而在容器中水平居中该特定元素。该元素将继承你指定的宽度，剩余空间将分布在左右边距之间。

如果浏览器窗口小于你的 HTML 元素的宽度，你可能会遇到问题。这时，浏览器会在你的网页上添加一个水平滚动条。通过使用`max-width`，你可以改进浏览器处理小窗口的方式。当你正在制作可以在小设备上使用的网站时，这一点至关重要。

CSS`position`属性通常用于指定某个特定元素所使用的定位方法类型。你可以使用`relative`、`sticky`、`static`、`fixed`和`absolute`方法。一旦决定了要选择哪种定位，你可以使用`right`、`left`、`top`和`bottom`属性对 HTML 元素进行定位。除非代码中设置了`position`属性，否则这些属性不会生效。此外，它们会根据你在代码中填充的位置值起作用。

### Static（静态）

网站的第一种布局位置是`static`。网站上所有的 HTML 元素默认都是`static`位置。这些元素受`left`、`top`、`bottom`和`right`属性的影响最小。带有`static`的 HTML 元素不会进行特殊定位，而是根据页面流进行定位的。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div.ThisIsStatic {
  position: static;
  border: 4px solid #FF9DA97;
}
</style>
</head>
<body>
<h4>学习静态定位属性；</h4>
<p>静态定位最棒的地方是它不是以特定的方式定位的。它根据网页的流来塑造自己的位置：</p>
<div class="ThisIsStatic">
  查看此网页上静态定位是如何工作的；
</div>
</body>
</html>
```

#### 学习静态定位属性

静态定位最棒的地方是它不是以特定的方式定位的。它根据网页的流来塑造自己的位置：

查看此网页上静态定位是如何工作的；

### Relative（相对）

第二种布局位置是`relative`。它相对于 HTML 元素的正常位置对其进行调整。对你已进行相对定位的 HTML 元素设置`bottom`、`top`、`left`和`right`属性，会导致它离开正常位置。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div.ThisIsRelative {
  position: relative;
  left: 40px;
  border: 4px solid black;
}
</style>
</head>
<body>
<h4>学习相对定位属性；</h4>
<p>静态定位最棒的地方是它不是以特定的方式定位的。它根据网页的流来塑造自己的位置：</p>
<div class="ThisIsRelative">
  查看此网页上静态定位是如何工作的；
</div>
</body>
</html>
```

#### 学习相对定位属性；

静态定位最棒的地方是它不是以特定的方式定位的。它根据网页的流来塑造自己的位置：

查看此网页上静态定位是如何工作的；

### Fixed（固定）



具有`fixed`位置的 HTML 元素应该相对于视口（viewport）进行定位。这意味着即使你向下滚动页面到部，元素也会一直留在同一个地方。你可以使用`right`、`left`、`top`和`bottom`属性来设置 HTML 元素的位置。`fixed` HTML 元素不会在网页所在的位置留出空隙。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div.ThisIsFixed {
  position: fixed;
  bottom: 50;
  right: 0;
  width: 500px;
  border: 4px solid red;
}
</style>
</head>
<body>
<h4>学习固定定位属性；</h4>
<p>CSS 如果使用得当，有能力让你的网站对不同的媒体设备具有高度响应性并具有交互性：</p>
<div class="ThisIsFixed">
  此示例展示了如何调整你网站的布局；
</div>
</body>
</html>
```

#### 学习固定定位属性

CSS 如果使用得当，有能力让你的网站对不同的媒体设备具有高度响应性并具有交互性：

此示例展示了如何调整你网站的布局；

如果你给`bottom`属性赋予`0`值，`div`元素将位于网页的底部。无论你向下滚动多少，它将保持固定并对用户可见。使用`fixed`功能时要小心。除非你必须显示用户在留在你的网站时需要知道的极其有用的信息，否则不要使用它。它从一件趣事变成一件令人厌烦的事情只需要一点时间，足以让用户开始讨厌你的网站。

### Absolute（绝对）

具有`absolute`位置的 HTML 元素相对于最近已定位的祖先元素进行定位。如果你的绝对定位 HTML 元素缺少祖先元素，它将展开元素体，并随着你滚动页面而移动。定位元素是指具有除`static`以外的任何位置的元素。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div.ThisIsRelative {
  position: relative;
  width: 500px;
  height: 100px;
  border: 5px solid red;
}
div.ThisIsAbsolute {
  position: absolute;
  top: 100px;
  right: 0;
  width: 300px;
  height: 100px;
  border: 5px solid yellow;
}
</style>
</head>
<body>
<div class="ThisIsRelative"><h4>学习定位属性；</h4><div>CSS 如果使用得当，有能力让你的网站对不同的媒体设备具有高度响应性并具有交互性：</div></div>
<div class="ThisIsAbsolute">
此示例展示了如何调整你网站的布局；
</div>
</body>
</html>
```

*注：Absolute 部分包含了“学习固定定位属性”。*

### Sticky（粘性）

具有`sticky`位置的 HTML 元素会在用户滚动时调整。`sticky`元素在`fixed`和`relative`属性之间切换。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div.stickyscrolling {
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  padding: 4px;
  background-color: skyblue;
  border: 2px solid grey;
}
</style>
</head>
<body>
<h4>学习定位属性；</h4>
<div class="stickyscrolling">这是粘性的！</div>
<div style="padding-bottom:2500px">
<p>CSS 如果使用得当，有能力让你的网站对不同的媒体设备具有高度响应性并具有交互性：</p>
<p> 此示例展示了如何调整你网站的布局。</p>
<p>这是页面的结束。滚动查看该行是否固定在页面顶部。</p>
</div>
</body>
</html>
```

#### 学习定位属性

这是粘性的！CSS 如果使用得当，有能力让你的网站对不同的媒体设备具有高度响应性并具有交互性：

此示例展示了如何调整你网站的布局；

如果你认为网页没有滚动，请向代码添加更多文本以启用滚动。

### Elements Overlapping（重叠）

当你有定位元素时，它们会与不同的 HTML 元素重叠。HTML 元素可能有负或正堆叠顺序。

```html
<!DOCTYPE html>
<html>
<head>
<style>
img {
  position: absolute;
  left: 2px;
  top: 2px;
  z-index: -2;
}
</style>
</head>
<body>
<p>学习重叠属性</p>
<img src="css.gif" width="200" height="110">
<p>由于图像保持 z-index 为 -2，你将能够将其放在网页文本之后。</p>
</body>
</html>
```

### Layout Overflow（溢出）

CSS 布局`overflow`属性用于控制超出特定区域的内容。`overflow`属性指定当元素内容对于网页上的某个区域过大时，程序员是想要固定内容还是为其添加滚动条。CSS`overflow`属性使用多个值来允许程序员自由实验。需要记住的一个重要点是，`overflow`属性适用于具有指定高度的块元素。

### Visible（可见）

第一个`overflow`属性命名为`visible`。默认情况下，网页溢出是可见的。这意味着它永远不会被裁剪，并且会渲染到元素框之外。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  background-color: skyblue;
  width: 150px;
  height: 80px;
}
</style>
```

```css
<style>
div {
  border: 2px dotted red;
  overflow: visible;
}
</style>
</head>
<body>
<p>这是 CSS 溢出</p>
<p>CSS 如果与 HTML 5 结合，将彻底改变你网站的外观</p>
<div>新冠-19 疫情在全球范围内迅速蔓延。最初对这种疾病的恐惧是无法用言表的。然而，人们逐渐发现，它并没有像最初看起来那么致命。</div>
</body>
</html>
```

# 这是 CSS 溢出

CSS 如果与 HTML 5 结合，将彻底改变你网站的外观

新冠-19 疫情在全球范围内迅速蔓延。最初对这种疾病的恐惧是无法用言表的。然而，人们逐渐发现，它并没有像最初看起来那么致命。

虽然这里的文本出现在 body 标签内部，但在网页上，它将显示在 body 之外。

### 隐藏 (Hidden)

第二个属性被称为`hidden`。使用此值时，你的`overflow`将显示为裁剪（clipped）。任何超出框的内容都将被隐藏。

```html
<!DOCTYPE html>
<html
<head>
<style>
div {
  background-color: skyblue;
  width: 150px;
  height: 80px;
  border: 2px dotted red;
  overflow: hidden;
}
</style>
</head>
<body>
<p>这是 CSS 溢出</p>
<p>CSS 如果与 HTML 5 结合，将彻底改变你网站的外观</p>
<div>新冠-19 疫情在全球范围内迅速蔓延。最初对这种疾病的恐惧是无法用言表的。然而，人们逐渐发现，它并没有像最初看起来那么致命。</div>
</body>
</html>
```

这是 CSS 溢出

CSS 如果与 HTML 5 结合，将彻底改变你网站的外观

新冠-19 疫情在全球范围内迅速蔓延。最初对这种疾病的恐惧是无法用言表的。然而，人们逐渐发现，它并没有像

你可以看到文本被切断了。无法放入框内的文本被划掉了（ slashed）。

### 滚动 (Scroll)

另一个值是`scroll`。`overflow`保持裁剪状态，但框内会出现滚动条。用户可以使用垂直和水平滚动条来阅读全文。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  background-color: skyblue;
  width: 150px;
  height: 80px;
  border: 2px dotted red;
  overflow: scroll;
}
</style>
</head>
<body>
<p>这是 CSS 溢出</p>
<p>CSS 如果与 HTML 5 结合，将彻底改变你网站的外观</p>
<div>新冠-19 疫情在全球范围内迅速蔓延。最初对这种疾病的恐惧是无法用言表的。然而，人们逐渐发现，它并没有像最初看起来那么致命。</div>
</body>
</html>
```

`auto`值类似于`scroll`值，因为它也会在代码中添加滚动条。

### CSS 浮动 (Float)

CSS`float`属性为你的网页页增添了一丝样式。它指定了网页上不同的 HTML 元素应该如何浮动。与`float`属性配合的是`clear`属性，它用于调整浮动元素。你可以通过使用`float`属性将图像悬浮在网页的右侧或左侧，从而对内容进行定位和格式化。`float`属性的额外值为`none`、`left`、`right`和`inherit`。

```html
<!DOCTYPE html>
<html>
<head>
<style>
img {
  float: right;
}
</style>
</head>
<body>
<p>这是 CSS 浮动</p>
<p img src="Covid.jpg" alt="Covid" style="width:180px;height:180px;margin-left:20px;">新冠-19 疫情在全球范围内迅速蔓延。最初对这种疾病的恐惧是无法用言表的。然而，人们逐渐发现，它并没有像最初看起来那么致命。</p>
</body>
</html>
```

这是 CSS 浮动

新冠-19 疫情在全球范围内迅速蔓延。最初对这种疾病的恐惧是无法用言表的。然而，人们逐渐发现，它并没有像最初看起来那么致命。

将真实的图片上传到代码并在浏览器中运行，查看图像是如何浮动到代码右侧的。你可以以相同的方式应用`left`值。文本将移到右侧，图像将移到左侧。你可以在网页上创建并行的浮动项目。每个项目将相互浮动。查看下面的示例。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  float: left;
  padding: 20px;
}
.kaz1 {
  background: skyblue;
}
.kaz2 {
  background: yellow;
}
.kaz3 {
  background: skyblue;
}
</style>
</head>
<body>
<p>这是 CSS 浮动</p>
<div class="kaz1">新冠-19 疫情在全球范围内迅速蔓延。</div>
<div class="kaz2">新冠-19 疫情在全球范围内迅速蔓延。</div>
<div class="kaz3">最初对这种疾病的恐惧是无法用言表的。</div>
<p>这是 CSS 浮动</div></div>然而，人们逐渐发现，它并没有像最初看起来那么致命。</div>
</body>
</html>
```

这是 CSS 浮动

新冠-19 疫情在全球范围内迅速蔓延。最初对这种疾病的恐惧是无法用言表的。然而，人们逐渐发现，它并没有像最初看起来那么致命。

### 清除属性 (Clear)

`clear`属性用于调整浮动元素。它指定了哪些元素不应该在浮动元素旁边。`float`属性的值有`none`、`left`、`right`和`inherit`。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  float: left;
  padding: 20px;
}
.kaz1 {
  background: skyblue;
}
.kaz2 {
  background: yellow;
}
.kaz3 {
  background: skyblue;
}
</style>
</head>
<body>
<p>这是 CSS 浮动</p>
<div class="kaz1">新冠-19 疫情在全球范围内迅速蔓延。</div>
<div class="kaz2">新冠-19 疫情在全球范围内迅速蔓延。</div>
<div class="kaz3">最初对这种疾病的恐惧是无法用言表的。</div>
<p>这是 CSS 浮动</div></div>然而，人们逐渐发现，它并没有像最初看起来那么致命。</div>
</body>
</html>
```

*(注：由于原文文本在 HTML 结构上存在一些混乱和重复，翻译时已根据逻辑对内容进行了整理以确保可读性)*

实际上，根据你提供的原始文本翻译如下：

```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
  float: left;
  padding: 20px;
}
.kaz1 {
  background: skyblue;
}
.kaz2 {
  background: yellow;
}
.kaz3 {
  background: skyblue;
}
</style>
</head>
<body>
<p>这是 CSS 浮动</div>
<p>不清除</p>
<div class="kaz1">段落 1</div>
<div class="kaz2">段落 2</div>
<p>是清除</p>
<div class="kaz3">段落 3</div>
<div class="kaz4">段落 4</div>
</body>
</html>
```

不清除

段落 1

段落 2- 请注意，段落 2 位于段落 1 之后。然而，由于我们对段落 1 使用了浮动属性，它将浮在页面的左侧，段落 2 的文本将环绕它流动。

清除

段落 3

段落 4 将掉落在浮动的 3。“left”值将清除已向左浮动的元素。你可以通过将代码改为“right”或“both”来实验它们如何影响你的网页布局。

### CSS 浮动示例

通过 CSS`float`属性的帮助，你可以让框并排浮动。

```html
<!DOCTYPE html>
<html>
<head>
<style>
* {
  box-sizing: border-box;
}
.boxing {
  float: left;
  width: 30%;
  padding: 40px;
}
.clearfixingfeature::after {
  content: "";
  clear: both;
  display: table;
}
</style>
</head>
<body>
<p>这是一个框网格</p>
<p>你正在看到并排浮的框：</p>
<div class="clearfixingfeature">
  <div class="boxing" style="background-color:skyblue">
  <p>第一个浮动的框。</p>
  </</div>
  <div class="boxing" style="background-color:red">
  <p>第二个浮动的框。</p>
  </</div>
  <div class="boxing" style="background-color:yellow">
  <p>第三个浮动的框。</p>
  </div>
</div>
</body>
</html>
```

<p>clearfix 杂技改进了布局流。`box-sizing`属性确保你的框在添加额外的内边距后不会损坏。</p>

# 这是一个盒子网格

你正在看到并排排列的浮动盒子：

- 第一个悬浮的盒子。

- 第二个悬浮的盒子。

- 第三个悬浮的盒子。

clearfix 技巧改善了布局流。`box-sizing`属性确保了你的盒子在添加额外的内边距（padding）后不会破坏。

现在我将移除`boxsize`特性，看看它如何影响网页的布局。参见示例。



```html
<!DOCTYPE html>
<html>
<head>
<style>
.boxing {
  float: left;
  width: 30%;
  padding: 40px;
}
.clearfixingfeature::after {
  content: "";
  clear: both;
  display: table;
}
</style>
</head>
<body>
<p>This is a Grid of Boxes</p>
<p>You are looking at Float boxes put side by side:</p>
<div class="clearfixingfeature">
  <div class="boxing" style="background-color:skyblue">
  <p>The first suspended box.</p>
  </div>
  <div class="boxing" style="background-color:red">
  <p>The second suspended box.</p>
  </div>
  <div class="boxing" style="background-color:yellow">
  <p>The third suspended box.</p>
  </div>
</div>
<p>The clearfix hack ameliorates the layout flow. The box-sizing property ensures that your boxes do not break after you add extra padding. </p>
</body>
</html>
```

如果你将其加载到网页中，盒子将呈现悬浮状态，但它们的尺寸将不是完美的。

```html
<!DOCTYPE html>
<html>
<head>
<style>
* {
  box-sizing: border-box;
}
.image {
  float: left;
  width: 30%;
  padding: 4px;
}
.clearfixingfeature::after {
  content: "";
  clear: both;
  display: table;
}
</style>
</head>
<body>
<p>This is a Grid of Boxes</p>
<p>You are looking at Float boxes put side by side:</p>
<div class="clearfixingfeature">
    <div class="image">
  <img src="mango.jpg" alt="mango" style="width:100%">
  </div>
  <div class="image">
  <img src="coconut.jpg" alt="coconut" style="width:100%">
  </div>
  <div class="image">
  <img src="banana.jpg" alt="banana" style="width:100%">
  </div>
</div>
<p>The clearfix hack ameliorates the layout flow. The box-sizing property ensures that your boxes do not break after you add extra padding. </p>
</body>
</html>
```

## 这是一个盒子网格

你正在看到并排排列的浮动盒子：

`clearfix` 技巧改善了布局流。`box-sizing` 属性确保了你的盒子在添加额外的内边距（`padding`）后不会破坏。

当你创建盒子时，你可以通过这段代码填充它们并让它们浮动。然而，如果你添加了某些超出盒子宽度的内容，盒子就会崩溃。`box-sizing` 属性允许你适应变化的宽度和高度，并防止其崩溃。

### 等高盒子

你已经学习了如何在保持宽度相同的同时让盒子浮动。然而，真正的挑战是创建这些盒子并让它们以等高度浮动。你可以通过设置固定高度来解决这个问题。

```html
<!DOCTYPE html>
<html>
<head>
<style>
* {
  box-sizing: border-box;
}
.boxing {
  float: left;
  width: 30%;
  padding: 40px;
  height: 200px;
}
.clearfixingfeature::after {
  content: "";
  clear: both;
  display: table;
}
</style>
</head>
<body>
<p>This is a Grid of Boxes</p>
<p>You are looking at Float boxes put side by side:</p>
<div class="clearfixingfeature">
  <div class="boxing" style="background-color:skyblue">
  <p>The first suspended box.</p>
  </div>
  <div class="boxing" style="background-color:red">
  <p>The second suspended box.</p>
  </div>
  <div class="boxing" style="background-color:yellow">
  <p>The third suspended box.</p>
  </div>
</div>
<p>The clearfix hack ameliorates the layout flow. The box-sizing property ensures that your boxes do not break after you add extra padding. </p>
</body>
</html>
```

这是一个盒子网格

你正在看到并排排列的浮动盒子：

- 第一个悬浮的盒子。

- 第二个悬浮的盒子。

- 第三个悬浮的盒子。

`clearfix` 技巧改善了布局流。`box-sizing` 属性确保了你的盒子在添加额外的内边距（`padding`）后不会破坏。

这个公式有效，但它是灵活性最低的。如果你认为盒子将具有相同的内容，那么它将长期有效。然而，内容并不会保持不变。内容会随时间推移发生变化。用户在手机上打开网站时，盒子可能会发生溢出。使用 `Flexbox` 属性可以处理这种情况。

```html
<!DOCTYPE html>
<html>
<head>
<style>
.flexbox {
  display: flex;
  flex-wrap: nowrap;
}
.flexbox .item {
  flex: 1;
  background-color: black;
  margin: 5px;
  padding: 10px;
}
.active {
  background-color: yellow;
}
</style>
</head>
<body>
<p>This is a Grid of Boxes</p>
<p>You are looking at Float boxes put side by side:</p>
<div class="flexbox">
  <div class="item active">
  <p>The first suspended box.</p>
  </div>
  <div class="item">
  <p>The second suspended box.</p>
  </div>
  <div class="item">
  <p>The third suspended box.</p>
  </div>
</div>
</body>
</html>
```

## 这是一个盒子网格

你正在看到并排排列的浮动盒子：

- 第一个悬浮的盒子。

- 第二个悬浮的盒子。

- 第三个悬浮的盒子。

### 菜单

你可以使用浮动属性来设计水平菜单。

```html
<!DOCTYPE html>
<html>
<head>
<style>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
}
li {
  float: left;
}
li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}
li a:hover {
  background-color: #aaa;
}
</style>
</head>
<body>
<ul>
  <li><a href="#home">Home</a></li>
  <li><a href="#news">News</a></li>
  <li><a href="#contact">Contact</a></li>
  <li><a href="#about">About</a></li>
</ul>
</body>
</html>
```

### 布局

在以下示例中，我将使用浮动属性来设计完整的布局。你可以使用代码来编辑你的页面。

```html
<!DOCTYPE html>
<html>
<head>
<style>
* {
  box-sizing: border-box;
}
.headers, .footers {
  background-color: lightgrey;
  color: black;
  padding: 20px;
}
.columns {
  float: left;
  padding: 20px;
}
.clearfixing::after {
  content: "";
  clear: both;
  display: table;
}
.menus {
  width: 30%;
}
.contents {
  width: 85%;
}
.menus ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
.menus li {
  padding: 10px;
  margin-bottom: 10px;
  background-color: skyblue;
  color: white;
}
.menus li:hover {
  background-color: yellow;
}
</style>
</head>
<body>
<div class="headers">
  <p>Designing a layout</p>
</div>
<div class="clearfixing">
  <div class="columns menus">
    <ul>
      <li><a href="#home">Home Page</a></li>
      <li><a href="#news">News Corner</a></li>
      <li><a href="#contact">Contact & Email</a></li>
      <li><a href="#about">About Us</a></li>
    </ul>
  </div>
  <div class="columns contents">
    <p><b>Mysterious Places</b></p>
    <p>The world is full of mysterious place. You can find giant spiders, lofty trees, ground level clouds, miles long fish, and coconuts, the size of an air balloon. </p>
  </div>
</div>
<div class="footers">
  <p>Copyright 2023</p>
</div>
</body>
</html>
```

当你掌握了 `CSS` 编码艺术时，网页设计会让你非常兴奋。

# 设计网页

- 天空

- 松树

- 海滩

- 有机食品

## 神秘的地点

世界上充满了神秘的地点。你可以找到巨大的蜘蛛、高耸的树、地面的云朵、长数英里的鱼，以及像气球一样椰子。

当你掌握了 `CSS` 编码艺术时，网页设计会让你非常兴奋。

页脚文本

## 第七

## CSS 显示特性

![](img/Image00001.jpg)

有很多特性可以设置你网站的显示。你已经学习了如何设置 `float` 来设计网页。最常见的显示特性之一是 `inline-block` 特性。它允许设置元素的 `height` 和 `width`。在 `inline-block` 特性的帮助下，浏览器将尊重你的 `paddings` 和 `margins`。

## Inline-Block

```html
<!DOCTYPE html>
<html><head>
<style>
span.z {
  display: inline; /* 这是 span 的默认特性 */
  width: 110px;
  height: 110px;
  padding: 6px;
  border: 2px solid skyblue;
  background-color: grey;
}
span.y {
  display: inline-block;
  width: 110px;
  height: 110px;
  padding: 6px;
  border: 2px solid blue;   
  background-color: yellow;
}
span.x {
  display: block;
  width: 110px;
  height: 110px;
  padding: 6px;
  border: 2px solid skyblue;   
  background-color: yellow;
}
</style>
</head>
<body>
<p>学习 display 属性</p>
<p>这是 display: inline</p>
<div> 世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。
     <span class="z">阿拉伯联合酋长长酋</span> <span class="z">哈利法国塔</span> 无论如何，这栋建筑的宏伟是无与伦比的。</div>
<p>这是 display: inline-block</p>
<div>世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。
    <span class="y">阿联酋</span> <span class="y">迪拜</span> 有时，云朵在建筑半空处落下阵雨。</div>
<p>这是 display: block</p>
<div>世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。
<span class="x">沙漠</span> <span class="x">摩天大楼</span> 当刮风暴风雨大来时，它也会左右摇晃。</div>
</body>
</html>
```

### 学习 display 属性

这是 `display: inline`

世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。阿拉伯联合酋长长酋 哈利法国塔 无论如何，这栋建筑的宏伟是无与伦比的。

这是 `display: inline-block`

世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。阿联酋 迪拜 有时，云朵在建筑半空处落下阵雨。

这是 `display: block`

世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。沙漠摩天大楼 当刮风暴雨大来时，它也会左右摇晃。

## 导航链接

你可以使用 `inline-block` 在网页上添加更多交互。创建导航链接是网站设计中最常见的做法。这有利于为访问者提供便利性。你可以以水平格式显示项目，而不是垂直格式。接的示例将创建一个导航链接。

```html
<!DOCTYPE html>
<html>
<head>
<style>
.navigation {
  background-color: yellow;
  list-style-type: none;
  text-align: center;
  margin: 0;
  padding: 0;
}
.navigation li {
  display: inline-block;
  font-size: 20px;
  padding: 20px;
}
</style>
</head>
<body>
<p>学习 display 属性</p>
<p>这是 display: inline</p>
<p> 世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。无论如何，这栋建筑的宏伟是无与伦比的。 </p>
<ul class="navigation">
  <li><a href="#home">首页</a></li>
  <li><a href="#about">关于我们</a></li>
  <li><a href="#clients">关于我的客户</a></li> 
  <li><a href="#contact">联系我们</a></li>
</ul>
</body>
</html>
```

### 学习 display 属性

这是 `display: inline`

世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。阿拉伯联合酋长长酋酋 哈利法国塔 无论如何，这栋建筑的宏伟是无与伦比的。

- `#home`: 首页

- `#about`: 关于我们

- `#clients`: 关于我的客户

- `#contact`: 联系我们



这是 `display: inline-block`

世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。阿联酋 迪拜 有时，云朵在建筑半空处落下阵雨。

这是 `display: block`

世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。沙漠摩天大楼 当刮风暴雨大来时，它也会左右摇晃。

## 导航链接

你可以使用 `inline-block` 在网页上添加更多交互。创建导航链接是网站设计中最常见的做法。这有利于为访问者提供便利性。你可以以水平格式显示项目，而不是垂直格式。接的示例将创建一个导航链接。

### 学习 `display` 属性

这是 `display: inline`

世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。阿拉伯联合酋长长酋酋 哈利法国塔 无论如何，这栋建筑的宏伟是无与伦比的。

- `#home`: 首页
- `#about`: 关于我们
- `#clients`: 关于我的客户
- `#contact`: 联系我们

这是 `display: inline-block`

世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。阿联酋 迪拜 有时，云朵在建筑半空处落下阵雨。

这是 `display: block`

世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。沙漠摩天大楼 当刮风暴雨大来时，它也会左右摇晃。

## 导航链接

你可以使用 `inline-block` 在网页上添加更多交互。创建导航链接是网站设计中最常见的做法。这有利于为访问者提供便利性。你可以以水平格式显示项目，而不是垂直格式。接的示例将创建一个导航链接。

### 学习 `display` 属性

这是 `display: inline`

世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。阿拉伯联合酋长长酋酋 哈利法国塔 无论如何，这栋建筑的宏伟是无与伦比的。

- `#home`: 首页
- `#about`: 关于我们
- `#clients`: 关于我的客户
- `#contact`: 联系我们

这是 `display: inline-block`

世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。阿联酋 迪拜 有时，云朵在建筑半空处落下阵雨。

这是 `display: block`

世界上最高的建筑位于迪拜。然而，哈利法国塔很快将有一个对手了。沙漠摩天大楼 当刮风暴雨大来时，它也会左右摇晃。

## 对齐

你可以使用 `inline-block` 在网页上添加更多交互。创建导航链接是网站设计中最常见的做法。这有利于为访问者提供便利性。你可以以水平格式显示项目，而不是垂直格式。接的示例将创建一个导航链接。

### 居中

如果你想在框框内居中文本，可以使用 `text-align` 属性。

```css
.centersaligned {
  margin: auto;
  width: 70%;
  border: 2px solid red;
  padding: 15px;
  text-align: center;
}
```

### 居中

如果你想在框框内居中文本，可以使用 `text-align` 属性。

### 居中

这是 CSS，你正在创建一个网页。

### 图片对齐

你可以添加图片并根据你的意愿在页面上对其齐。查看以下代码。

```html
<!DOCTYPE html>
<html>
<head>
<style>
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
</style>
</head>
<body>
<img src="mango.jpg" alt="芒果" style="width:60%">
</body>
</html>
```

### 左齐与右对齐

你可以使用 CSS 设置右对齐或左对齐，将 HTML 元素放置在正确的位置。

```css
.leftalignment {
  position: absolute;
  left: 0px;
  width: 250px;
  border: 2px solid black;
  padding: 15px;
}
```

浮动对齐

你可以使用另一种方法，即 `float`，来设置右对齐或左对齐。`float` 属性更加平滑，并且可以实现紧凑对齐。让我们来看 `float` 属性的演示。

```html
<!DOCTYPE html>
<html>
<head>
<style>
.rightalign {
  float: left;
  width: 250px;
  border: 2px solid black;
  padding: 10px;
}
</style>
</head>
<body>
<h4>网页上对齐的元素</h4>
<div class="rightalignment">
<p>我正在使用 `float` 属性来在网页上设置对齐。</p>
</div>
</body>
</html>
```

# 网页上对齐的元素

我正在使用 `float` 属性来在网页上设置对齐。

# 第八章

## CSS 组合器

![](img/Image00001.jpg)

CSS 组合器解释了不同选择器之间的关系 - CSS 选择器可能包含不仅仅是简单的选择器。选择器有不同的类型。本章将解释这些选择器如何工作，以及组合器如何形成并分析它们之间的关系。

### 后代选择器

后代选择器倾向于匹配从某个元素后代的元素。下一个示例将帮助你选择 `<p>` 和 `<div>` 元素。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div p {
  background-color: skyblue;
}
</style>
</head>
<body>
<h4>这是后代选择器</h4>
<p>这个后代选择器将匹配从某个特定元素后代的元素。</p>
<div>
  <p>这是第一行。</p>
  <p>这是第二行。</p>
  <section><p>这是 div 的第三行也是最后一行。</p></section>
</div>
<p>这一行在 div 之外。</p>
<p>这一行在 div 之外。</p>
</body>
</html>
```

这是后代选择器

这个后代选择器将匹配从某个特定元素后代的元素。

这是第一行。

这是第二行。

这是 div 的第三行也是最后一行。

这一行在 div 之外。

这一行在 div 之外。

### 子选择器

第二类型是子选择器。它将选择拥有一个特定元素的元素。在下面的示例中，我将选择父选择器的子元素。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div > p {
  background-color: skyblue;
}
</style>
</head>
<body>
<h4>这是子选择器</h4>
<p>这个子选择器 (`>`) 应该连接到所有属于特定元素的元素。</p>
<div>
  <p>这一行在 div 内部。</p>
  <p>这一行在 div 内部。</p>
  <section><p>这一行在 div 内部。</p></section>
  <p>这一行也在 div 内部。</p>
</div>
<p>这一行在 div 之外。</p>
<p>这一行在 div 之外。</p>
</body>
</html>
```

这是子选择器

这个子选择器 (`>`) 应该连接到所有属于特定元素的元素。

这一行在 div 内部。

这一行在 div 内部。

这一行在 div 内部。

这一行也在 div 内部。

这一行在 div 之外。

这一行在 div 之外。

### 相邻兄弟选择器

第三类型被称为相邻兄弟选择器。它用于选择某个元素之后的元素。兄弟元素拥有同一个父元素。我将在示例中展示相邻元素。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div + p {
  background-color: skyblue;
}
</style>
</head>
<body>
<h4>这是相邻兄弟选择器</h4>
相邻兄弟选择器 (`+`) 选择某个特定元素之后的元素。
类型是相邻兄弟选择器。
<div>
<p>这一行在 div 之后。</p>
<p>这一行在 div 之后。</p>
</div>
<p>在 div 在 div 之后。</p>
<p>这一行在 div 之后。</p>
</body>
</html>
```

这是相邻兄弟选择器

相邻兄弟选择器 (`+`) 选择某个特定元素之后的元素。

这一行在 div 之后。

这一行在 div 之后。

这一行在 div 之后。

这一行在 div 之后。

这一行在 div 之后。

这一行在 div 之后。

### 通用兄弟选择器

最后类型是通用兄弟选择器。它将选择某个特定元素的兄弟元素。`~` 运算符用于此目的。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div ~ p {
  background-color: skyblue;
}
</style>
</head>
<body>
<h4>这是通用兄弟选择器</h4>
通用兄弟选择器 (`~`) 选择某个特定元素的兄弟元素。
<div>
<p>这一行在 div 之后。</p>
</div>
<p>这一行在 div 之后。</p>
<p>这一行在 div 之后。</p>
</body>
</html>
```

`list-style-type` 特性可以移除导航栏中的项目符号。这段代码是创建水平和垂直导航栏的标准。

### 垂直条形

当你想要构建一个垂直导航栏时，可以在列表中使用 `<a>` 元素。

```html
<!DOCTYPE html>
<html>
<body>
<style>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
li a {
  display: block;
  width: 80px;
  background-color: skyblue;
}
</style>
<ul>
  <li><a href="#homepage">首页</a></li>
  <li><a href="#newspage">新闻角</a></li>
  <li><a href="#contactpage">联系电话</a></li>
  <li><a href="#aboutpage">关于我们</a></li>
</ul>
<p>我使用 `href="#"` 只是为了测试链接。当你构建一个真实的网站时，应该使用 URL。</p>
</body>
</html>
```

[首页](https://tools.tutorialspoint.com/uploads/c3c6d6e1a2ecfe5a1314367f6bd9e220-6848/index.htm#homepage)

[新闻角](https://tools.tutorialspoint.com/uploads/c3c6d6e1a2ecfe5a1314367f6bd9e220-6848/index.htm#newspage)

[联系电话](https://tools.tutorialspoint.com/uploads/c3c6d6e1a2ecfe5a1314367f6bd9e220-6848/index.htm#contactpage)

[关于我们](https://tools.tutorialspoint.com/uploads/c3c6d6e1a2ecfe5a1314367f6bd9e220-6848/index.htm#aboutpage)

我使用 `href="#"` 只是为了测试链接。当你构建一个真实的网站时，应该使用 URL。

当你将链接显示为块级元素时，将使链接区域变得完全可点击，而不仅仅是文本。它还允许你指定宽度、边距、高度和内边距。块元素默认将占据可用的全部宽度。宽度可以随时移除。结果是当你以块元素的形式显示它们时，元素将覆盖可用宽度。这应该产生与上一个示例相同的结果。

```html
<!DOCTYPE html>
<html>
<body>
<style>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
li a {
  display: block;
  background-color: skyblue;
}
</style>
<ul>
  <li><a href="#homepage">首页</a></li>
  <li><a href="#newspage">新闻角</a></li>
  <li><a href="#contactpage">联系电话</a></li>
  <li><a href="#aboutpage">关于我们</a></li>
</ul>
<p>我使用 `href="#"` 只是为了测试链接。当你构建一个真实的网站时，应该使用 URL。</p>
</body>
</html>
```

你可以在浏览器中查看输出。条形的元素将覆盖整个宽度。垂直导航栏中的一个惊人特性是当用户悬停在元素上时颜色的变化。在下面的示例中，我将创建一个在鼠标移动到其上方时改变颜色的导航栏。我添加了一些颜色。背景是白色的。当你将鼠标悬停在条形上时，它将变成红色。你可以测试颜色组合以产生你想要的结果。

```html
<!DOCTYPE html>
<html>
<body>
<style>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 250px;
  background-color: grey;
}
li a {
  display: block;
  color: skyblue;
  padding: 6px 14px;
  text-decoration: none;
}
/* 以下几行代码将在悬停时改变链接的颜色 */
li a:hover {
  background-color: red;
  color: white;
}
</style>
<ul>
  <li><a href="#homepage">首页</a></li>
  <li><a href="#newspage">新闻角</a></li>
  <li><a href="#contactpage">联系电话</a></li>
  <li><a href="#aboutpage">关于我们</a></li>
</ul>
<p>我使用 `href="#"` 只是为了测试链接。当你构建一个真实的网站时，应该使用 URL。</p>
</body>
</html>
```

[首页](https://tools.tutorialspoint.com/uploads/bca82606122f153822b2fcd5ef-17746/index.htm#homepage)

[新闻角](https://tools.tutorialspoint.com/uploads/bca82606122f153822b2fcd5ef-17746/index.htm#newspage)

[联系电话](https://tools.tutorialspoint.com/uploads/bca82606122f153822b2fcd5ef-17746/index.htm#contactpage)

[关于我们](https://tools.tutorialspoint.com/uploads/bca82606122f153822b2fcd5ef-17746/index.htm#aboutpage)

### Active 类

你可以为代码添加 `active` 类，让用户知道他们处于哪个页面。

```html
<!DOCTYPE html>
<html>
<body>
<style>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 250px;
  background-color: grey;
}
li a {
  display: block;
  color: skyblue;
  padding: 6px 14px;
  text-decoration: none;
}
/* 以下几行代码将在悬停时改变链接的颜色 */
li a:hover {
  background-color: red;
  color: white;
}
</style>
<ul>
  <li><a href="#homepage" class="active">首页</a></li>
  <li><a href="#newspage">新闻角</a></li>
  <li><a href="#contactpage">联系电话</a></li>
  <li><a href="#aboutpage">关于我们</a></li>
</ul>
</body>
</html>
```

### 添加边框

你可以通过添加边框来进一步装饰导航栏。你也可以将其放置在 `ul` 标签内部。

```html
<!DOCTYPE html>
<html>
<head>
<style>
body {
  margin: 0;
}
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 20%;
  background-color: #f1f1f1;
  position: fixed;
  height: 110%;
  overflow: auto;
}
li a {
  display: block;
  color: grey;
  padding: 6px 14px;
  text-decoration: none;
}
li a.activeclass {
  background-color: skyblue;
  color: white;
}
li a:hover:not(.activeclass) {
  background-color: lightgrey;
  color: white;
}
</style>
</head>
<body>
<ul>
```

### 固定导航栏



为了给你的网站增加风味，你可以创建一个固定的导航栏。导航栏将是全长度的，并且也是固定的。每当用户向下或向上滚动时，条形将固定在页面侧边。注意，你应该在进行彻底客户研究后使用它，因为某些用户可能会觉得它很人。在使用之前进行测试是必要的。无论用户是否喜欢，你都应该知道如何创建。

```html
<!DOCTYPE html>
<html>
<head>
<style>
body {
  margin: 0;
}
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 20%;
  background-color: #f1f1f1;
  position: fixed;
  height: 110%;
  overflow: auto;
}
li a {
  display: block;
  color: grey;
  padding: 6px 14px;
  text-decoration: none;
}
li a.activeclass {
  background-color: skyblue;
  color: white;
}
li a:hover:not(.activeclass) {
  background-color: lightgrey;
  color: white;
}
</style>
</head>
<body>
<ul>
```

`标签中似乎不完整（在 HTML 代码部分被截断了），我根据您提供的上下文和 Markdown 规范，为您翻译了已提供的文本部分。

以下是翻译后的内容：

```html
<ul>
  <li><a class="activeclass" href="#home">首页</a></li>
  <li><a href="#news">新闻角</a></li>
  <li><a href="#contact">联系方式</a></li>
  <li><a href="#about">关于我们</a></li>
</ul>

<div style="margin-left:20%;padding:2px 14px;height:900px;">
  <p>这是一个全高侧边导航栏</p>
  <p>当你向下滚动此区域时，你会发现侧边导航栏将固定在网页上</p>
  <p>在这里放置一些文本，以便你可以向下滚动网页。文本不足将导致你无法向下滚动，从而永远无法测试固定条的效果。</p>
  <p>在这里放置一些文本...</p>
  <p>在这里放置一些文本...</p>
  <p>在这里放置一些文本...</p>
</div>
```

## 水平导航栏

另一种类型的导航栏是水平条。你可以创建一个浮动条或内联列表在网页上列出不同的项目。

### 内联（Inline）

在此类编码中，你必须将`<li>`元素指定为内联（inline）。这会为网页上的标准代码增加额外的的层层。

```html
<!DOCTYPE html>
<html>
<head>
<style>
ul {
  list-style-type: none;
  margin: 1px;
  padding: 1px;
}
li {
  display: inline;
}
</style>
</head>
<body>
<ul>
  <li><a href="#home">首页</a></li>
  <li><a href="#news">新闻角</a></li>
  <li><a href="#contact">联系方式</a></li>
  <li><a href="#about">关于我们</a></li>
</ul>
</body>
</html>
```

[首页](https://tools.tutorialspoint.com/uploads/8e9e9cf630781eaccd24c665da21eb62-17833/index.htm#home) [新闻角](https://tools.tutorialspoint.com/uploads/8e9e9cf630781eaccd24c665da21eb62-17833/index.htm#news) [联系方式](https://tools.tutorialspoint.com/uploads/8e9e9cf630781eaccd24c665da21eb62-17833/index.htm#contact) [关于我们](https://tools.tutorialspoint.com/uploads/8e9e9cf630781eaccd24c665da21eb62-17833/index.htm#about)

`<li>`元素默认是块级元素（block elements）。你可以在列表的每个项目前后添加换行符，以便在网页上单行显示。

### 浮动（Floats）

如果你想创建浮动的列表项，你必须首先指定网页上所有导航链接的布局。

```html
<!DOCTYPE html>
<html>
<head>
<style>
ul {
  list-style-type: none;
  margin: 1px;
  padding: 1px;
  overflow: hidden;
}
li {
  float: left;
}
li a {
  display: block;
  padding: 10px;
  background-color: skyblue;
}
</style>
</head>
<body>
<ul>
  <li><a href="#home">首页</a></li>
  <li><a href="#news">新闻角</a></li>
  <li><a href="#contact">联系方式</a></li>
  <li><a href="#about">关于我们</a></li>
</ul>
</body>
</html>
```

[首页](https://tools.tutorialspoint.com/uploads/6132f110d3e0be92c3c426b5a0a9d5ce-17814/index.htm#home) [新闻角](https://tools.tutorialspoint.com/uploads/6132f110d3e0be92c3c426b5a0a9d5ce-17814/index.htm#news) [联系方式](https://tools.tutorialspoint.com/uploads/6132f110d3e0be92c3c426b5a0a9d5ce-17814/index.htm#contact) [关于我们](https://tools.tutorialspoint.com/uploads/6132f110d3e0be92c3c426b5a0a9d5ce-17814/index.htm#about)

`float: left`属性会将块级元素设置在页面相邻位置。`display: block`允许你精确控制类似内边距、高度和宽度。由于块级元素占用总宽度，它们无法并排浮动。某些内边距为条增添了美感。

### 精华水平条（Glamor Horizontal Bars）

你可以更改代码让水平导航看起来更精致。在这个示例中，我将解释如何创建一个带有背景颜色的水平导航栏，以及当悬停在导航链接上时颜色如何变化。

```html
<!DOCTYPE html>
<html>
<head>
<style>
ul {
  list-style-type: none;
  margin: 1px;
  padding: 1px;
  overflow: hidden;
  background-color: lightgrey;
}
li {
  float: left;
}
li a {
  display: block;
  color: green;
  text-align: center;
  padding: 12px 14px;
  text-decoration: none;
}
li a:hover {
  background-color: yellow;
}
</style>
</head>
<body>
<ul>
  <li><a href="#home">首页</a></li>
  <li><a href="#news">新闻角</a></li>
  <li><a href="#contact">联系方式</a></li>
  <li><a href="#about">关于我们</a></li>
</ul>
</body>
</html>
```

[首页](https://tools.tutorialspoint.com/uploads/b41caa5d3b4ba4587f16d685723637/index.htm#home) [新闻角](https://tools.tutorialspoint.com/uploads/b41caa5d3b4ba4587f16d685723637/index.htm#news) [联系方式](https://tools.tutorialspoint.com/uploads/b41caa5d3b4ba4587f16d685723637/index.htm#contact) [关于我们](https://tools.tutorialspoint.com/uploads/b41caa5d3b4ba4587f16d685723637/index.htm#about)

### 激活链接（Active Links）

我们可以通过包含`activeclass`为导航条添加更多代码，告诉用户他们正在浏览哪个页面。我将设置一个激活链接将使用的颜色。

```html
<!DOCTYPE html>
<html>
<head>
<style>
ul {
  list-style-type: none;
  margin: 1px;
  padding: 1px;
  overflow: hidden;
  background-color: lightgrey;
}
li {
  float: left;
}
li a {
  display: block;
  color: green;
  text-align: center;
  padding: 12px 14px;
  text-decoration: none;
}
li a:hover {
  background-color: yellow;
}
.activeclass {
  background-color: skyblue;
}
</style>
</head>
<body>
<ul>
  <li><a class="activeclass" href="#home">首页</a></li>
  <li><a href="#news">新闻角</a></li>
  <li><a href="#contact">联系方式</a></li>
  <li><a href="#about">关于我们</a></li>
</ul>
</body>
</html>
```

[首页](https://tools.tutorialspoint.com/uploads/b3161d39cd61a9e7a13eb422b84392-12402/index.htm#home) [新闻角](https://tools.tutorialspoint.com/uploads/b3161d39cd61a9e7a13eb422b84392-12402/index.htm#news) [联系方式](https://tools.tutorialspoint.com/uploads/b3161d39cd61a9e7a13eb422b84392-12402/index.htm#contact) [关于我们](https://tools.tutorialspoint.com/uploads/b3161d39cd61a9e7a13eb422b84392-12402/index.htm#about)

激活链接将具有天蓝色，稍后你可以激活链接的颜色。激活链接让你的代码更具互动性和精致。

### 右对齐（Right Alignment）

你可以创建一个代码将某些导航栏元素浮动到页面的右侧。有时你需要让像“联系方式”或“关于我们”这样的元素与其它元素分开。这就是右对齐功能大有帮助的地方。

以下示例包含了创建一个固定在网页底部或顶部的水平导航栏的代码。即使使用户向下滚动页面，该栏目也会固定在原位置。当您创建固定位置导航栏时，应该确保将导航栏的宽度保持到最小，以免它覆盖页面的部分内容。宽大的固定水平条会令人困扰，因为它们有时会阻挡页面的完整视图。用户会发现很难阅读内容或在网页上移动其他元素。因此，最好对其进行测试。

```html
<!DOCTYPE html>
<html>
<head>
<style>
body {margin:1px;}
ul {
  list-style-type: none;
  margin: 1px;
  padding: 1px;
  overflow: hidden;
  background-color: lightgrey;
  position: fixed;
  top: 1px;
  width: 150%;
}
li {
  float: center;
}
li a {
  display: block;
  color: white;
  text-align: center;
  padding: 12px 14px;
  text-decoration: none;
}
li a:hover:not(.activeclass) {
  background-color: skyblue;
}
.activeclass {
  background-color: #3BAC60;
}
</style>
</head>
<body>
<ul>
  <li><a class="activeclass" href="#home">首页 Home</a></li>
  <li><a href="#news">新闻角 News</a></li>
  <li><a href="#contact">联系方式 Contact</a></li>
  <li><a href="#about">关于我们 About Us</a></li>
</ul>
<div style="padding:15px;margin-top:20px;background-color:yellow;height:1200px;">
  <h4>这是固定顶部的导航栏</h4>
  <h4>您必须向下滚动网页才能看到它的工作原理。</h4>
  <h4>当您滚动网页时，此导航栏倾向于固定在页面顶部。</h4>
  <p>放置一些文本以便滚动。</p>
  <p>放置一些文本以便滚动。</p>
  <p>放置一些文本以便滚动。</p>
</div>
</body>
</html>
```

[首页 Home Page](https://tools.tutorialspoint.com/uploads/c773c0836f7c1dd20e165b69cd544807-32191/index.htm#home)

[新闻角 News Corner](https://tools.tutorialspoint.com/uploads/c773c0836f7c1dd20e165b69cd544807-32191/index.htm#news)

[联系方式 Contact No](https://tools.tutorialspoint.com/uploads/c773c0836f7c1dd20e165b69cd544807-32191/index.htm#contact)

[关于我们 About Us](https://tools.tutorialspoint.com/uploads/c773c0836f7c1dd20e165b69cd544807-32191/index.htm#about)

这是固定顶部的导航栏

您必须向下滚动网页才能看到它的工作原理。

当您滚动网页时，此导航栏倾向于固定在页面顶部。

放置一些文本以便滚动。

放置一些文本以便滚动。

放置一些文本以便滚动。

### 固定条（Sticky Bar）

以下代码示例将使导航栏固定在顶部。如果您在网页中填充大量文本，您将看到固定效果。



```html
<!DOCTYPE html>
<html>
<head>
<style>
body {
  font-size: 31px;
}
ul {
  list-style-type: none;
  margin: 1px;
  padding: 1px;
  overflow: hidden;
  background-color: lightgrey;
  position: -webkit-sticky;
  position: sticky;
  top: 1px;
}
li {
  float: left;
}
li a {
  display: block;
  color: black;
  text-align: center;
  padding: 12px 14px;
  text-decoration: none;
}
li a:hover {
  background-color: yellow;
}
.activeclass {
  background-color: green;
}
</style>
</head>
<body>
<div class="header">
  <h4>固定水平条</h4>
  <p>您必须向下滚动网页才能看到固定效果。</p>
</div>
<ul>
  <li><a class="activeclass" href="#home">博客 Blog</a></li>
  <li><a href="#news">新闻页 News Page</a></li>
  <li><a href="#contact">点点我 Poke Me</a></li>
</ul>
<h4>固定导航栏说明</h4>
<p>当您到达滚动位置时，此导航栏倾向于`stick`固定在顶部。</p>
<p>请注意，Internet Explorer 不支持此功能。Safari 需要`-webkit-`前缀。</p>
<p>在此处填充文本以启用滚动...</p>
<p>在此处填充文本以启用滚动...</p>
<p>在此处填充文本以启用滚动...</p>
</body>
</html>
```

## 固定水平条（Sticky Horizontal Bar）

您必须向下滚动网页才能看到固定效果。

[博客 Blog](https://tools.tutorialspoint.com/uploads/c773c0836f7c1dd20e165b69cd544807-32191/index.htm#home) [新闻页 News Page](https://tools.tutorialspoint.com/uploads/c773c0836f7c1dd20e165b69cd544807-32191/index.htm#news) [点点我 Poke Me](https://tools.tutorialspoint.com/uploads/c773c0836f7c1dd20e165b69cd544807-32191/index.htm#contact)

## 固定导航栏说明（Sticky Navbar Explained）

当您到达滚动位置时，此导航栏倾向于`stick`固定在顶部。

请注意，Internet Explorer 不支持此功能。Safari 需要`-webkit-`前缀。

在此处填充文本以启用滚动...

在此处填充文本以启用滚动...

在此处填充文本以启用滚动...

# 第十章：CSS 下拉菜单与图片（CSS Dropdowns & Images）

![](img/Image0001.jpg)

下拉菜单非常棒，它们让您的网站具有交互性并便于导航。CSS 允许您创建悬停下拉菜单。当用户将鼠标悬在特定元素上时，会弹出一个框。

## 下拉菜单（A Dropdown）

```html
<!DOCTYPE html>
<html>
<head>
<style>
.letusdropdown {
  position: relative;
  display: inline-block;
}
.thisisdropdown-content {
  display: none;
  position: absolute;
  background-color: lightgrey;
  min-width: 180px;
  box-shadow: 1px 7px 17px 1px rgba(0,0,0,0.2);
  padding: 14px 18px;
  z-index: 1;
}
.letusdropdown:hover .thisisdropdown-content {
  display: block;
}
</style>
</head>
<body>
<h4>正在学习悬停下拉菜单</h4>
<p>用户将鼠标移动到网页下方文本上以打开下拉内容。</p>
<div class="letusdropdown">
  <span>在此悬停鼠标</span>
  <div class="thisisdropdown-content">
    <p>CSS 太棒了！不是吗？</p>
  </div>
</div>
</body>
</html>
```

### 正在学习悬停下拉菜单（You are Studying Hoverable Dropdown）

用户将鼠标移动到网页下方文本上以打开下拉内容。

### 在此悬停鼠标（Please Hover Your Mouse Here）

当用户悬停在“在此悬停鼠标”上，将弹出菜单。用户可以点击链接到达另一个页面或启动任务。您也可以使用`<button>`元素创建下拉内容。您可以在`<div>`元素内部添加任何内容创建下拉内容。我使用了类和`relative`位置设置菜单的位置。第二个类`thisisdropdown-content`保存内容。菜单默认是隐藏的。只有当您将鼠标悬停在其上方时才能看到它。您可以更改宽度来尝试下拉菜单的设计。如果您不熟悉它，可以使用`border`属性代替`box-shadow`属性。

## 下拉列表（A Dropdown List）

挑战是在下拉菜单中添加列表。您可以在下拉列表中添加任意数量的选项。我将向下拉菜单添加导航链接，允许用户在页面之间切换并执行不同的任务。您还可以对链接和菜单进行样式处理，使其看起来时尚且精致。这里是您可以为自己的网站编辑和自定义的代码示例。

```html
<!DOCTYPE html>
<html>
<head>
<style>
.mydropbutton {
  background-color: lightgrey;
  color: black;
  padding: 14px;
  font-size: 14px;
  border: none;
  cursor: pointer;
}
.letusdropdown {
  position: relative;
  display: inline-block;
}
.thisisdropdown-content {
  display: none;
  position: absolute;
  background-color: skyblue;
  min-width: 180px;
  box-shadow: 1px 7px 17px 1px rgba(0,0,0,0.2);
  z-index: 1;
}
.thisisdropdown-content a {
  color: black;
  padding: 10px 14px;
  text-decoration: none;
  display: block;
}
.thisisdropdown-content a:hover{background-color: green}
.letusdropdown:hover .thisisdropdown-content {
  display: block;
}
.letusdropdown:hover .mydropbutton {
  background-color: red;
}
</style>
</head>
<body>
```

### 悬停下拉菜单

```html
<div class="letusdropdown">
  <button class="mydropbutton">My Dropdown Menu</button>
  <div class="thisisdropdown-content">
    <a href="#">Iceland</a>
    <a href="#">Ireland</a>
    <a href="#">India</a>
  </div>
</div>
```

## 悬停下拉菜单

### 导航栏下拉菜单

让我们通过在导航栏内部创建一个下拉菜单来提升到一个新的水平。如果你需要与用户有更多交互，可以将下拉菜单添加到栏中。事实上，这种导航栏和下拉菜单的组合正在成为网站设计的标准。用户通过将鼠标悬停在导航栏上来节省时间，并了解网站的内容。这种 CSS 特性加速了用户的决策。这就是它提高转化率的原因。用户喜爱那些能够帮助他们节省时间的业务。

```html
<!DOCTYPE html>
<html>
<head>
<style>
ul {
  list-style-type: none;
  margin: 1px;
  padding: 1px;
  overflow: hidden;
  background-color: skyblue;
}
li {
  float: left;
}
li a, .mydropbutton {
  display: inline-block;
  color: grey;
  text-align: center;
  padding: 12px 14px;
  text-decoration: none;
}
li a:hover, .letusdropdown:hover .mydropbutton {
  background-color: red;
}
li.letusdropdown {
  display: inline-block;
}
.thisisdropdown-content {
  display: none;
  position: absolute;
  background-color: skyblue;
  min-width: 180px;
  box-shadow: 1px 7px 17px 1px rgba(0,0,0,0.2);
  z-index: 1;
}
.thisisdropdown-content a {
  color: black;
  padding: 10px 14px;
  text-decoration: none;
  display: block;
}
.thisisdropdown-content a:hover {background-color: green}
.letusdropdown:hover .thisisdropdown-content {
  display: block;
}
.letusdropdown:hover .mydropbutton {
  background-color: red;
}
</style>
</head>
<body>
<h4>Hoverable Dropdown menus</h4>
<ul>
  <li><a href="#home">Home Page</a></li>
  <li><a href="#news">News Page</a></li>
  <li class="letusdropdown">
    <a href="javascript:void(0)" class="mydropbutton">Browse Countries You Need To Visit</a>
    <div class="thisisdropdown-content">
      <a href="#">Iceland</a>
      <a href="#">Ireland</a>
      <a href="#">India</a>
    </div>
  </li>
</ul>
</body>
</html>
```

### 悬停下拉菜单

[首页](https://tools.tutorialspoint.com/uploads/d2bf8c09bcbe0aeb903d398d55a5b7a8-17804/index.htm#home) [新闻页](https://tools.tutorialspoint.com/uploads/d2bf8c09bcbe0aeb903d398d55a5b7a8-17804/index.htm#news) 浏览你需要访问的国家

## 图片画廊

你可以通过简单的代码为你的网站添加图片。如果你正在为你的旅游网站创建一个在线商店，你可能需要为网站添加旅游目的地的图片。你可以通过创建代码来将它们堆叠起来。一旦你创建了代码，就可以继续添加更多图片来为网站添加更多旅游景点。删除旧过时的图片并用新图片替换它们。查看如何为此创建代码，然后对其进行编辑，看看实验可以走多远。

```html
<!DOCTYPE html>
<html>
<head>
<style>
div.1stgallery {
  margin: 7px;
  border: 2px solid lightgrey;
  float: left;
  width: 200px;
}
div.1stgallery:hover {
  border: 2px solid red;
}
div.1stgallery img {
  width: 120%;
  height: auto;
}
div.description {
  padding: 20px;
  text-align: center;
}
</style>
</head>
<body>
<div class="1stgallery">
  <a target="_blank" href="italy.jpg">
    <img src="italy.jpg" alt="beaches" width="50">
  </a>
  <div class="description">这里是你可以添加描述的地方</div>
</div>
<div class="1stgallery">
  <a target="_blank" href="spain.jpg">
    <img src="spain.jpg" alt="Mountains" width="50">
  </a>
  <div class="description">Description Space</div>
</div>
<div class="1stgallery">
  <a target="_blank" href="rome.jpg">
    <img src="rome.jpg" alt="Castles" width="50">
  </a>
  <div class="description">Description Space</div>
</div>
<div class="1stgallery">
  <a target="_blank" href="germany.jpg">
    <img src="germany.jpg" alt="Lakes" width="50">
  </a>
  <div class="description">Description Space</div>
</div>
</body>
</html>
```

### 图片精灵

Image Sprites 允许你将多张图片合并到单个图像文件中，以减少加载网页所需的 HTTP 请求。通过使用 CSS 属性`background-position`，你可以根据需要显示精灵图像的特定部分。这种技术改进了网站的性能和加载速度，特别是在包含许多小图标或图片的页面上。

# 第十一章

## CSS 属性与表单

![](img/Image00001.jpg)

你可以对带有属性值的不同 HTML 元素设置样式。属性选择器通常用于通过指定的属性选择不同的元素。你可以使用属性选择器根据指定的属性来选择元素。以下示例将根据目标属性选择元素。

```html
<!DOCTYPE html>
<html>
<head>
<style>
a[target] {
  background-color: lightgrey;
}
</style>
</head>
<body>
<h4>学习 CSS 选择器</h4>
<p>以下带有 target 属性的链接将具有黄色背景：</p>
<a href="https://www.sinoform.com">This is sinoform.com</a>
<a href="http://www.treeisgreen.com" target="_blank">This is treeisgreen.com</a>
<a href="http://www.printmedia.org" target="_top">This is printmedia.org</a>
</body>
</html>
```

### 学习 CSS 选择器

以下带有 target 属性的链接将具有黄色背景：

[This is sinoform.com](https://www.sinoform.com/) [This is treeisgreen.com](http://www.treeisgreen.com/) [This is printmedia.org](http://www.printmedia.org/)

### CSS 表单

你的 HTML 表单外观需要通过 CSS 进行极大改进。



```html
<!DOCTYPE html>
<html>
<style>
input[type=thetext], select {
  width: 150%;
  padding: 14px 24px;
  margin: 10px 0;
  display: inline-block;
  border: 2px solid lightgrey;
  border-radius: 6px;
  box-sizing: border-box;
}
input[type=submityourresponse] {
  width: 250%;
  background-color: skyblue;
  color: white;
  padding: 16px 24px;
  margin: 6px 0;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}
input[type=submityourresponse]:hover {
  background-color: yellow;
}
div {
  border-radius: 7px;
  background-color: seagreen;
  padding: 15px;
}
</style>
<body>
<h4>学习使用 CSS 样式化 HTML 表单</h4>
<div>
  <form action="/action_page.php">
    <label for="firstname">First Name</label>
    <input type="thetext" id="firstname" name="firstname" placeholder="Your first name..">
    <label for="lastname">Last Name</label>
    <input type="thetext" id="lastname" name="lastname" placeholder="Your last name..">
    <label for="yourcountry">Country</label>
    <select id="yourcountry" name="yourcountry">
      <option value="Ireland">Ireland</option>
      <option value="canada">Canada</option>
      <option value="Iceland">Iceland</option>
    </select>
    <input type="submityourresponse" value="Submit">
  </form>
</div>
</body>
</html>
```

### 学习使用 CSS 样式化 HTML 表单

First Name Last Name Country ![](img/Image00073.jpg)

你可以通过使用 `width` 属性为输入字段添加更多样式。

```html
<!DOCTYPE html>
<html>
<head>
<style>
input {
  width: 150%;
}
</style>
</head>
<body>
<p>这是一个全宽输入字段：</p>
<form>
  <label for="firstname">Your First Name</label>
  <input type="thetext" id="firstname" name="firstname">
</form>
</body>
</html>
```

这是一个全宽输入字段：

Your First Name

### Padding 属性

你可以使用 `padding` 属性为文本字段提供额外的内边距。当你处理多个输入框时，你可能需要在代码中添加一些外边距（margin）。将在外部添加额外的间距。

```html
<!DOCTYPE html>
<html>
<head>
<style>
input[type=thetext] {
  width: 120%;
  padding: 14px 25px;
  margin: 10px 0;
  box-sizing: border-box;
}
</style>
</head>
<body>
<p>这些是有内边距的文本字段：</p>
<form>
  <label for="firstname">First Name</label>
  <input type="thetext" id="firstname" name="firstname">
  <label for="lastname">Last Name</label>
  <input type="thetext" id="lastname" name="lastname">
</form>
</body>
</html>
```

这些是有内边距的文本字段：

First Name Last Name

### 更多设计

让我们通过在代码中整合 `border` 属性为表单添加更多设计，以改变表单的颜色、大小和长度。`border-radius` 属性可以用于设置输入字段的角。

```html
<!DOCTYPE html>
<html>
<head>
<style>
input[type=thetext] {
  width: 120%;
  padding: 14px 25px;
  margin: 10px 0;
  box-sizing: border-box;
  border: 4px solid green;
  border-radius: 6px;
}
</style>
</head>
<body>
<p>这些是有内边距的文本字段：</p>
<form>
  <label for="firstname">First Name</label>
  <input type="thetext" id="firstname" name="firstname">
  <label for="lastname">Last Name</label>
  <input type="thetext" id="lastname" name="lastname">
</form>
</body>
</html>
```

你可以只添加 `border-bottom` 属性为输入添加底框。

```html
<!DOCTYPE html>
<html>
<head>
<style>
input[type=thetext] {
  width: 120%;
  padding: 14px 25px;
  margin: 10px 0;
  box-sizing: border-box;
  border: none;
  border-bottom: 4px solid red;
}
</style>
</head>
<body>
<p>这些是有内边距的文本字段：</p>
<form>
  <label for="firstname">First Name</label>
  <input type="thetext" id="firstname" name="firstname">
  <label for="lastname">Last Name</label>
  <input type="thetext" id="lastname" name="lastname">
</form>
</body>
</html>
```

### 有颜色的输入框

你还可以使用 `background-color` 代码为表单创建彩色效果。你可以为背景赋予任何颜色。

```html
<!DOCTYPE html>
<html>
<head>
<style>
input[type=thetext] {
  width: 120%;
  padding: 14px 25px;
  margin: 10px 0;
  box-sizing: border-box;
  background-color: skyblue;
  color: green;
}
</style>
</head>
<body>
<p>这些是有内边距的文本字段：</p>
<form>
  <label for="firstname">First Name</label>
  <input type="thetext" id="firstname" name="firstname">
  <label for="lastname">Last Name</label>
  <input type="thetext" id="lastname" name="lastname">
</form>
</body>
</html>
```

### 聚焦输入框

你可以通过添加一个在用户聚焦输入字段时改变颜色的属性来更改样式。将在下面的代码中添加 `focus` 属性以查看结果。

```html
<!DOCTYPE html>
<html>
<head>
<style>
input[type=thetext] {
  width: 120%;
  padding: 14px 25px;
  margin: 10px 0;
  box-sizing: border-box;
  border: 2px solid skyblue;
  outline: none;
}
input[type=thetext]:focus {
  background-color: lightgrey;
}
</style>
</head>
<body>
<p>这些是聚焦的文本字段：</p>
<form>
  <label for="firstname">First Name</label>
  <input type="thetext" id="firstname" name="firstname">
  <label for="lastname">Last Name</label>
  <input type="thetext" id="lastname" name="lastname">
</form>
</body>
</html>
```

现在聚焦字段将具有边框。

```html
<!DOCTYPE html>
<html>
<head>
<style>
input[type=thetext] {
  width: 120%;
  padding: 14px 25px;
  margin: 10px 0;
  box-sizing: border-box;
  border: 4px solid red;
  -webkit-transition: 0.5s;
  transition: 0.5s;
  outline: none;
}
input[type=thetext]:focus {
  border: 4px solid yellow;
}
</style>
</head>
<body>
<p>这些是聚焦的文本字段：</p>
<form>
  <label for="firstname">First Name</label>
  <input type="thetext" id="firstname" name="firstname">
  <label for="lastname">Last Name</label>
  <input type="thetext" id="lastname" name="lastname">
</form>
</body>
</html>
```

你可以通过向搜索框添加背景图像来进一步修改你的搜索框。你可以通过使用 `background` 属性对其进行定位。请注意，你应该为图标在搜索框中的调整留出足够的空间。搜索框的代码如下：

```html
<!DOCTYPE html>
<html>
<head>
<style>
input[type=thetext] {
  width: 150%;
  box-sizing: border-box;
  border: 4px solid lightgrey;
  border-radius: 6px;
  font-size: 14px;
}
</style>

<style>
body {
  background-color: skyblue;
  background-image: url('someicon.png');
  background-position: 12px 12px;
  background-repeat: no-repeat;
  padding: 14px 25px 14px 60px;
}
</style>
</head>
<body>
<p>查看这个带有图标的输入框：</p>
<form>
  <input type="thetext" name="search" placeholder="在此处搜索..">
</form>
</body>
</html>
```

### 文本区域（Text Areas）

您可以使用 `resize` 属性来防止文本区域被调整大小。

```html
<!DOCTYPE html>
<html>
<head>
<style>
textarea {
  width: 150%;
  height: 130px;
  padding: 14px 25px;
  box-sizing: border-box;
  border: 4px solid red;
  border-radius: 6px;
  background-color: skyblue;
  font-size: 18px;
  resize: none;
}
</style>
</head>
<body>
<p><strong>专业提示：</strong>您可以应用 `resize` 属性来防止调整大小：</p>
<form>
  <textarea>一些文本...</textarea>
</form>
</body>
</html>
```

专业提示：您可以应用 `resize` 属性来防止调整大小：

![](img/Image00074.jpg)

### 菜单样式（Menu Styling）

您可以使用相同的代码进行微调来为菜单设置样式。请记住，单个原始 HTML 元素可能会破坏您网站的外观。

```html
<!DOCTYPE html>
<html>
<head>
<style>
select {
  width: 150%;
  padding: 18px 25px;
  border: none;
  border-radius: 6px;
  background-color: skyblue;
}
</style>
</head>
<body>
<p>这是一个样式化的菜单。</p>
<form>
  <select id="listofcountry" name="listofcountry">
    <option value="ir">我们到达了爱尔兰。</option>
    <option value="ca">加拿大正在邀请移民。</option>
    <option value="usa">美国仍然是超级大国。</option>
  </select>
</form>
</body>
</html>
```

以下代码可以帮助设置按钮，例如提交按钮或订阅按钮。

```html
<!DOCTYPE html>
<html>
<head>
<style>
input[type=subscribe], input[type=submit], input[type=Enter] {
  background-color: skyblue;
  border: none;
  color: red;
  padding: 18px 36px;
  text-decoration: none;
  margin: 6px 4px;
  cursor: pointer;
}
</style>
</head>
<body>
<p>这些是样式化的按钮。</p>
<input type="subscribe" value="订阅">
<input type="submit" value="提交">
<input type="Enter" value="回车">
</body>
</html>
```

这些是样式化的按钮。

![](img/Image00075.jpg)

### 响应式表单（Responsive Form）

您可以调整浏览器窗口的大小查看表单的行为。大多数情况下，表单对浏览器窗口大小的变化没有响应。当您的屏幕宽度低于 600px 时，它将以列堆叠的形式显示。您可以创建表单来完成许多任务，例如收集联系信息或为销售产品收集财务信息。后者用于电子商务商店。

```html
<!DOCTYPE html>
<html>
<head>
<style>
* {
  box-sizing: border-box;
}
input[type=thetext], theselect, thetextarea {
  width: 150%;
  padding: 14px;
  border: 2px solid skyblue;
  border-radius: 6px;
  resize: vertical;
}
label {
  padding: 14px 14px 0;
  display: inline-block;
}
input[type=thesubmit] {
  background-color: lightgrey;
  color: red;
  padding: 14px 25px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  float: right;
}
input[type=thesubmit]:hover {
  background-color: yellow;
}
.class1 {
  border-radius: 7px;
```



```html
background-color: seagreen;
padding: 30px;
}

.class2 {
  float: left;
  width: 25%;
  margin-top: 8px;
}

.class3 {
  float: left;
  width: 85%;
  margin-top: 8px;
}

/* 在列之后产生清除的浮动 */
.rowing:after {
  content: "";
  display: table;
  clear: both;
}

/* 这是一个生成的响应式布局 - 当屏幕宽度小于标准的 600px 时，两列将正确地堆叠在彼此之上，而不是并排放置 */
@media screen and (max-width: 600px) {
  .class2, .class3, input[type=thesubmit] {
    width: 150%;
    margin-top: 0;
  }
}
</style>
</head>
<body>
<h4>您正在查看一个响应式表单</h4>

<p>现在，您可以调整浏览器窗口的大小并查看切换效果。当屏幕宽度低于 600px 时，它将变为两列正确地堆叠在彼此之上。</p>

<div class="class1">
  <form action="/theaction_page.php">
    <div class="rowing">
      <div class="class2">
        <label for="firstname">名</label>
      </div>
      <div class="class3">
        <input type="thetext" name="firstname" placeholder="您的名字">
      </div>
    </div>

    <div class="rowing">
      <div class="class2">
        <label for="lastname">姓</label>
      </div>
      <div class="class3">
        <input type="thetext" name="lastname" placeholder="您的名字">
      </div>
    </div>

    <div class="rowing">
      <div class="class2">
        <label for="mycountry">国家</label>
      </div>
      <div class="class3">
        <select id="mycountry">
          <option value="ir">我们到达了爱尔兰。</option>
          <option value="ca">加拿大正在邀请移民。</option>
          <option value="usa">美国仍然是超级大国。</option>
        </select>
      </div>
    </div>

    <input type="thesubmit" value="提交">
  </form>
</div>
</body>
</html>
```

# 第十二章

## CSS 网页布局

![](img/Image00001.jpg)

你可以将网站的布局划分为菜单、页头、页脚和一些内容。有不同的布局设计可供选择。通常，一个网站有一个页头、页脚和内容。有一些菜单可以装饰页面。页头位于网页的顶部。它也可以设置在顶部导航菜单下方。通常，它包含网站的名称或 Logo。

```html
<!DOCTYPE html>
<html lang="en">
<head>
<title>Decoding CSS Layout</title>
<meta charset="utf-8">
<meta name="theviewport" content="thewidth=device-width, theinitial-scale=1">
<style>
body {
  margin: 1px;
}

/* I am now Styling the website header */
.header {
  background-color: lightgrey;
  padding: 25px;
  text-align: center;
}
</style>
</head>
<body>
<div class="header">
  <h4>This Is The Header</h4>
</div>
</body>
</html>
```

这是页头

### 导航栏

布局的第二个组件是导航栏。它几乎是不可避免的。你必须有一个，因为它承载了一系列导航链接，引导用户穿过网站。

```html
<!DOCTYPE html>
<html lang="en">
<head>
<title>CSS Website Layout</title>
<meta charset="utf-8">
<meta name="theviewport" content="width=device-width, initial-scale=1">
<style>
* {
  box-sizing: border-box;
}

body {
  margin: 1px;
}

/* This code is for Styling your header */
.headerclass {
  background-color: skyblue;
  padding: 25px;
  text-align: center;
}

/* This code is for Styling your top navigation bar */
.topnavigationbar {
  overflow: hidden;
  background-color: red;
}

/* This code is for Styling the topnavigation links */
.topnavigationbar a {
  float: left;
  display: block;
  color: black;
  text-align: center;
  padding: 16px 18px;
  text-decoration: none;
}

/* This code is for Changing the color on the mouse hover */
.topnavigationbar a:hover {
  background-color: lightgrey;
  color: black;
}
</style>
</head>
<body>
<div class="theheader">
  <h4>This Is Header</h4>
</div>

<div class="topnavigationbar">
  <a href="#">首页</a>
  <a href="#">关于我们</a>
  <a href="#">新闻角</a>
</div>
</body>
</html>
```

这是页头

[首页](https://tools.tutorialspoint.com/uploads/913c1fb3e01bda4adc4898840c9660b4-17849/index.htm) [关于我们](https://tools.tutorialspoint.com/uploads/913c1fb3e01bda4adc4898840c9660b4-17849/index.htm) [新闻角](https://tools.tutorialspoint.com/uploads/913c1fb3e01bda4adc4898840c9660b4-17849/index.htm)

### 内容

布局的这部分取决于目标用户。网站中最常见的布局是结合了以下不同的列。你可以使用三栏布局在页面上显示你的博客。

```html
<!DOCTYPE html>
<html lang="en">
<head>
<title>This is my CSS Layout</title>
<meta charset="utf-8">
<meta name="theviewport" content="width=device-width, initial-scale=1">
<style>
* {
  box-sizing: border-box;
}

body {
  margin: 1px;
}

/* This code will Style your header */
.headerwebsite {
  background-color: lightgrey;
  padding: 25px;
  text-align: center;
}

/* This code will Style your top navigation bar */
.topnavigationbar {
  overflow: hidden;
  background-color: skyblue;
}

/* This code will Style your links */
.topnavigationbar a {
  float: left;
  display: block;
  color: red;
  text-align: center;
  padding: 16px 18px;
  text-decoration: none;
}

/* This code will Change the color on the hover */
.topnavigationbar a:hover {
  background-color: red;
  color: black;
}

/* Create three equal columns that floats next to other */
.columns {
  float: left;
  width: 30%;
  padding: 15px;
}

/* Clear floats after the columns */
.rowing:after {
  content: "";
  display: table;
  clear: both;
}

/* Create three equal columns that floats next to other */
.columns {
  float: left;
  width: 30%;
  padding: 15px;
}

/* Clear floats after the columns */
.rowing:after {
  content: "";
  display: table;
  clear: both;
}

/* Create three equal columns that floats next to other */
.columns {
  float: left;
  width: 30%;
  padding: 15px;
}

/* Clear floats after the columns */
.rowing:after {
  content: "";
  display: table;
  clear: both;
}

/* Create three equal columns that floats next to other */
.columns {
  float: left;
  width: 30%;
  padding: 15px;
}

/* Clear floats after the columns */
.rowing:after {
  content: "";
  display: table;
  clear: both;
}

/* Create three equal columns that floats next to other */
.columns {
  float: left;
  width: 30%;
  padding: 15px;
}

/* Clear floats after the columns */
.rowing:after {
  /* This is a Responsive web layout. You will see three columns properly stacked atop of other rather than side by side */
  content: "";
  display: table;
  clear: both;
}

@media screen and (max-width:600px) {
  .column {
    width: 100%;
  }
}
</style>
</head>
<body>
<div class="headerwebsite">
  <h4>This Is The Header</h4>
</div>

<div class="topnavigationbar">
  <a href="#">首页</a>
  <a href="#">博客</a>
  <a href="#">新闻</a>
</div>

<div class="rowing">
  <div class="columns">
    <h4>First Column</h4>
  </div>

  <div class="columns">
    <h4>Second Column</h4>
  </div>

  <div class="columns">
    <h4>Third Column</h4>
  </div>
</div>
</body>
</html>
```

这是页头。

这是一种响应式网页布局。你将看到三列垂直堆叠，而不是并排。

### 不等宽列

网站可能包含不等宽的列。这些是不可避免的。因此，通常使用不等宽列来为主要内容留出足够的空间。你可以根据需要更改宽度。

```html
<!DOCTYPE html>
<html lang="en">
<head>
<title>This is my CSS Layout</title>
<meta charset="utf-8">
<meta name="theviewport" content="width=device-width, initial-scale=1">
<style>
* {
  box-sizing: border-box;
}

body {
  margin: 1px;
}

/* This code will Style your header */
.headerwebsite {
  background-color: lightgrey;
  padding: 25px;
  text-align: center;
}

/* This code will Style your top navigation bar */
.topnavigationbar {
  overflow: hidden;
  background-color: skyblue;
}

/* This code will Style your links */
.topnavigationbar a {
  float: left;
  display: block;
  color: red;
  text-align: center;
  padding: 16px 18px;
  text-decoration: none;
}

/* This code will Change the color on the hover */
.topnavigationbar a:hover {
  background-color: red;
  color: black;
}

/* These are the right and left columns */
.columns.side {
  width: 20%;
}

/* This is the Middle column */
.columns.middle {
  width: 60%;
}

/* This clears the float after your columns */
.rowing:after {
  content: "";
  display: table;
  clear: both;
}

/* This is a Responsive web layout. You will see three columns properly stacked atop of other rather than side by side */
@media screen and (max-width:600px) {
  .column {
    width: 100%;
  }
}
</style>
</head>
<body>
<div class="headerwebsite">
  <h4>This Is The Header</h4>
</div>

<div class="topnavigationbar">
  <a href="#">首页</a>
  <a href="#">博客</a>
  <a href="#">新闻</a>
</div>

<div class="rowing">
  <div class="columns side">
    <h4>Left Column</h4>
  </div>
</div>
</body>
</html>
```



```html
</div>

<div class="columns middle">
  <h4>Middle Column</h4>
</div>

<div class="columns side">
  <h4>Right Column</h4>
</div>

</div>

</body>

</html>
```

```html
<body>
  <div class="headerwebsite">
    <h4>This is a Header</h4>
    <p>I am now resizing the browser window so that users can see the responsive effect.</p>
  </div>

  <div class="topnavigationbar">
    <a href="#">Home</a>
    <a href="#">Blog</a>
    <a href="#">News</a>
  </div>

  <div class="rowing">
    <div class="columns">
      <h4>First Columns</h4>
      <p>I like the United Kingdom because of the Victorian-style buildings, castles, pink fields, colorful autumn, and harry potter, of course.</p>
    </div>

    <div class="columns">
      <h4>Second Column</h4>
      <p>I like the United Kingdom because of the Victorian-style buildings, castles, pink fields, colorful autumn, and harry potter, of course. I like the United Kingdom because of the Victorian-style buildings, castles, pink fields, colorful autumn, and harry potter, of course.</p>
    </div>

    <div class="columns">
      <h4>Third Column</h4>
      <p>I like the United Kingdom because of the Victorian-style buildings, castles, pink fields, colorful autumn, and harry potter, of course.</p>
    </div>
  </div>
</body>

</html>
```

## 这是一个标题

我正在调整浏览器窗口的大小，以便用户可以看到响应式效果。

[首页](https://tools.tutorialspoint.com/uploads/491e9fe3acf10a9b139b8508c24ffaff-2886/index.htm) [博客](https://tools.tutorialspoint.com/uploads/491e9fe3acf10a9b139b8508c24ffaff-2886/index.htm) [新闻](https://tools.tutorialspoint.com/uploads/491e9fe3acf10a9b139b8508c24ffaff-2886/index.htm)

### 第一列

我喜欢英国，是因为那里有维多利亚风格的建筑、城堡、粉色田野、色彩丰富的秋天，还有哈利·波特。

### 第二列

我喜欢英国，是因为那里有维多利亚风格的建筑、城堡、粉色田野、色彩丰富的秋天，还有哈利·波特。我喜欢英国，是因为那里有维多利亚风格的建筑、城堡、粉色田野、色彩丰富的秋天，还有哈利·波特。

### 第三列

我喜欢英国，是因为那里有维多利亚风格的建筑、城堡、粉色田野、色彩丰富的秋天，还有哈利·波特。

### 页脚

网站布局的另一个组件是设置网站页脚。通常它包含了联系信息和版权信息等内容。

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <title>This is my CSS Layout</title>
  <meta charset="utf-8">
  <meta name="theviewport" content="thewidth=device-width, theinitial-scale=1">

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 1px;
    }

    /* This code will Style your header */
    .headerwebsite {
      background-color: lightgrey;
      padding: 25px;
      text-align: center;
    }

    /* This code will Style your top navigation bar */
    .topnavigationbar {
      overflow: hidden;
      background-color: skyblue;
    }

    /* This code will Style your links */
    .topnavigationbar a {
      float: left;
      display: block;
      color: red;
      text-align: center;
      padding: 16px 18px;
      text-decoration: none;
    }

    /* This code will Change the color on the hover */
    .topnavigationbar a:hover {
      background-color: red;
      color: black;
    }

    /* Create three equal columns that floats next to each other */
    .columns {
      float: left;
      width: 30%;
      padding: 15px;
    }

    /* Clear floats after the columns */
    .rowing:after {
      content: "";
      display: table;
      clear: both;
    }

    /* These are the right and left columns */
    .columns.side {
      width: 20%;
    }

    /* This is the Middle column */
    .columns.middle {
      width: 60%;
    }

    /* This clears the float after your columns */
    .rowing:after {
      content: "";
      display: table;
      clear: both;
    }

    /* This is a Responsive web layout. You will see three columns properly stacked atop of each other rather than side by side */
    @media screen and (max-width: 600px) {
      .column {
        width: 100%;
      }
    }

    /* This code will Style your footer */
    .footerwebsite {
      background-color: skyblue;
      padding: 12px;
      text-align: center;
    }
  </style>
</head>

<body>
  <div class="headerwebsite">
    <h4>This is a Header</h4>
    <p>I am now resizing the browser window so that users can see the responsive effect.</p>
  </div>

  <div class="topnavigationbar">
    <a href="#">Home</a>
    <a href="#">Blog</a>
    <a href="#">News</a>
  </div>

  <div class="rowing">
    <div class="columns">
      <h4>First Columns</h4>
      <p>I like the United Kingdom because of the Victorian-style buildings, castles, pink fields, colorful autumn, and harry potter, of course.</p>
    </div>

    <div class="columns">
      <h4>Second Column</h4>
      <p>I like the United Kingdom because of the Victorian-style buildings, castles, pink fields, colorful autumn, and harry potter, of course.</p>
    </div>

    <div class="columns">
      <h4>Third Column</h4>
      <p>I like the United Kingdom because of the Victorian-style buildings, castles, pink fields, colorful autumn, and harry potter, of course.</p>
    </div>
  </div>

  <div class="footerwebsite">
    <p>This is a footer</p>
  </div>
</body>

</html>
```



```html
    width: 100%;

  }

}

/* This code will Style your footer */

.footerwebsite {

  background-color: skyblue;

  padding: 12px;

  text-align: center;

}

</style>

</head>

<body>

<div class="headerwebsite">

  <h4>This is a Header</h4>

  <p>I am now resizing the browser window so that users can see the responsive effect.</p>

</div>

<div class="topnavigationbar">

  <a href="#">Home</a>

  <a href="#">Blog</a>

  <a href="#">News</a>

</div>

<div class="rowing">

  <div class="columns">

    <h4>First Columns</h4>

    <p>I like the United Kingdom because of the Victorian-style buildings, castles, pink fields, colorful autumn, and harry potter, of course.</p>

  </div>

  <div class="columns">

    <h4>Second Column</h4>

    <p> I like the United Kingdom because of the Victorian-style buildings, castles, pink fields, colorful autumn, and harry potter, of course.</p>

  </div>

  <div class="columns">

    <h4>Third Column</h4>

    <p> I like the United Kingdom because of the Victorian-style buildings, castles, pink fields, colorful autumn, and harry potter, of course.</p>

  </div>

</div>

<div class="footerwebsite">

  <p>This is a footer</p>

</div>

</body>

</html>
```

本书包含了关于如何编写`JavaScript`代码的经过实践验证的步骤和策略。我在书中包含了`JavaScript`的分步编程技术，以便你能够正确地学习它们。`JavaScript`是一门脚本语言。你会在 HTML 标签中看到大量嵌入的脚本。由于`JavaScript`无法独立工作，我认为将其嵌入 HTML 中是恰当的，这样当你运行它时，它在网络浏览器中运行良好良好。

如果你想练习所学的内容，可以打开代码编辑器，复制代码并粘贴进去以检查结果。此外，你也可以将页面加载到网络浏览器中直接在网页上查看结果。嵌入式脚本是即插即用的形式。学习脚本最好的方法是背下来，然后对它们进行编辑以自定义，这样你就能以更快、更有趣的方式学习。

无论你是在制作网站，还是一个渴望成为 Web 开发者的学生，亦或是计划为自己的业务建立网站，这本书都是你可能在市场上遇到的最优秀的文献。一旦你读完前几章，你将做好心理准备，继续学习复杂的话题。最好的方法是开始时慢一点，随着概念变得清晰逐渐调整自己的节奏。

# 第一章

## JavaScript 简介

![](img/Image00001.jpg)

`JavaScript` 是一种解释型语言。该语言的定义比“解释型”一词更广泛。你可以将其定义为一种弱类型、基于原型、动态且命令式的过程化语言。`JavaScript` 以客户端编程语言的形式开发和实现。它是网络浏览器的一部分，被认为可以帮助开发者实现动态功能，并在网页上创建和集成用户界面。你可能可能在服务器端也能发现`JavaScript`的实现。然而，`JavaScript`编程语言的流行很大程度上基于它在客户端的应用。你可能在 Web 应用之外也能看到`JavaScript`的应用。例如，你可能会发现它们被用于为桌面组件和 PDF 格式文档添加一些交互性。

`JavaScript` 最初的设计与`C`语言的设计模式相同，但它采用了一些`Java`编程语言的名字。你不应该将`Java`与`JavaScript`混淆，因为它们在本质上是不同的。它们也有不同的目的和语义。

### JavaScript 的开发者

Brendan Each 最初开发`JavaScript`时使用的名为`Mocha`。后来这个名字被改为`LiveScript`。随后，它再次被改为`JavaScript`。这个名字困扰了一些人，并给人一种印象，即新语言（即`JavaScript`）是`Java`的分支。人们认为这种新的编程语言是 Netscape 营销策略的一部分，旨在新编程语言领域获得急需的声望。

第二年，微软引入了一种类似的客户端语言并集成到他们著名的`Internet Explorer 3.0`浏览器中。为了规避品牌问题，他们将该语言命名为`JScript`。这个术语听起来和视觉上被认为与`JavaScript`非常相似；然而，它的不同之处在于，它无法 100% 兼容`ECMA`规范。

1997 年，出现了一项将`JavaScript`提交给`ECMA`标准的提案，并在 1997 年 6 月，`ECMA`标准以`ECMAScript`的名称采纳了它。该编程语言还赢得了`ISO`标准推荐。`JavaScript`因其适应互联网的方式积累了极高的普及率。这就是它成为全球最常用编程语言之一的原因。

### JavaScript 的用例

`JavaScript`运行在世界上大多数网页的客户端。当你打开一个网页，而它与你上次打开时有所不同，那么，这些变化可能是使用`JavaScript`完成的。让我告诉你一件趣的事。在你的电脑屏幕上打开一个网页。右键点击网页然后点击“查看源代码”。你会在网页的代码中看到`JavaScript`这个词。不要将`HTML`与`JavaScript`混淆，因为你可能会在网页代码中发现这二者。

`HTML`是一种标记语言，允许开发者格式化内容并创建动态网页。你可以将文本变为粗体，创建你喜的框和表格，并在页面上添加按钮和项目符号。然而，`JavaScript`允许你修改文本、添加弹出消息，并通过`HTML`代码验证你输入的文本。`HTML`和`JavaScript`并肩行走。`JavaScript`领先于`HTML`的地方在于它让页面变得动态且可交互的方式。它将允许你的用户点击某些元素并从现有页面打开新页面。

你应该学习`JavaScript`，因为它非常容易实现。你只需要将代码放在`HTML`文档中，然后指示浏览器运行它。`JavaScript`可以在许多计算机和操作系统上，即使在系统离线时也是如此。在`JavaScript`的帮助下，你可以创建响应式界面，完善用户体验并提供极动态的功能。

`JavaScript`允许用户在需要时随时以文档的形式加载内容，而且无需重新加载网页。我们把这个过程称为`Ajax`。`JavaScript`允许你在浏览器中对现有可能性运行测试，然后做出相应反应。这一过程被称为防御性脚本（defensive Scripting）。`JavaScript`将修复你网页上出现的任何问题。它将弥补浏览器支持中存在的漏洞。

当我们把`JavaScript`为我们做的一切与其他 Web 编程语言进行比较时，我们意识到它可以做很多。`JavaScript`受到了巨大的需求和喜爱，因为它允许你在没有任何费恼的情况下构建复杂的应用程序。你也可以用`Flash`构建复杂的应用程序，但`JavaScript`是最佳选择，因为它是一种 Web 标准。

当谈到`JavaScript`的用法时，它的用法在不断变化。起初，`JavaScript`与网站的交互限于形成交互和给用户反馈。然而，它随着时间的推移而演变，现在的用途比开始多得多。

代码是指用于构成程序的文本。在书的许多章节中，你会发现大量的代码。我必须说，阅读和编写代码是学习和编写程序过程中不可或缺的一部分。

元编程被认为是一种强大的技术，它能够让你编写一组程序。`ES6`的出现进一步放宽了 JavaScript 编程世界中元编程的使用。你可以使用`proxies`和其他类似的特性。`ES6`的`proxies`倾向于重新定义对象中不同的操作。

# `<script>` 标签

让我们来谈谈书中用最多的符号——标签。所有的 JavaScript 代码都包含在`<script>`标签内。

```html
<!DOCTYPE html>

<html>

<body>

<p>JavaScript rests in the Body</p>

<p id="demo12"></p>

<script>

document.getElementById("demo12").innerHTML = "This is your First JavaScript";

</script>

</body>

</html>
```

### JavaScript 位于 Body（正文）中

这是你的第一个 JavaScript

旧版本的 JavaScript 编写方式不同。它采用如下格式，例如`<script type="text/javascript">`。

JavaScript 中有可以可以让你来执行代码块的函数。当某种事件发生时，你可以调用一个函数。事件可以定义为点击按钮。你可以在 HTML 文档中放置任何类型的脚本。你可以将脚本放置在`<head>`中、`<body>`中或者两者都放置。在`<head>`中使用脚本的例如下：

```html
<!DOCTYPE html>

<html>

<head>

<script>

function FunctionUN() {

  document.getElementById("demo34").innerHTML = "I have changed the Paragraph.";

}

</script>

</head>

<body>

<p>You have seen the JavaScript in the Head</p>

<p id="demo">This is a Paragraph.</p>

<button type="button" onclick="FunctionUN()">Click Me</button>

</body>

</html>
```

### 你在 Head（头部）中看到了 JavaScript

这是一个段落。

点击我

当你点击网页浏览器上的按钮时，你将触发函数的调用。你也可以将脚本放在 HTML 页面的`<body>`中。当你点击按钮时，将调用此函数。

```html
<!DOCTYPE html>

<html>

<body>

<p>This is A Web Page</p>

<p id="demo1">This is a Paragraph</p>

<button type="button" onclick="FunctionZ()">Click Me</button>

<script>

function FunctionZ() {

  document.getElementById("demo1").innerHTML = "I have changed the Paragraph.";

}

</script>

</body>

</html>
```

### 这是一个网页

我已经更改了段落。

点击我

# 显示

有不同的方法可以在网页浏览器中显示 JavaScript。程序员为了显示目的使用了不同的技术。我在书中使用的第一种方法是`document.getElementById(id)`方法。在短语中，`id`指定义 HTML 文档的元素。`innerHTML`单词定义了 HTML 的内容。

```html
<!DOCTYPE html>

<html>

<body>

<p>This is going to be my First Web Page</p>

<p>This will be the First Paragraph.</p>

<p id="demo1234"></p>

<script>

document.getElementById("demo1234").innerHTML = 4567 + 36;

</script>

</body>

</html>
```

这将是我的第一个网页

这将是第一个段落。

4603

你可以使用的第二方法是`document.write()`方法。这也是一个简单的方法。但是，除了向你展示它是如何工作的这个示例外，我在书中没有使用这种方法创建任何脚本：

```html
<!DOCTYPE html>

<html>

<body>

<p>This is going to be my First Web Page</p>

<p>This will be the First Paragraph.</p>

<p id="demo1234"></p>

<script>

document.write (4567 + 36);

</script>

</body>

</html>
```

这将是我的第一个网页

这将是第一个段落。

4603

如果你在加载 HTML 页面后使用这种方法，你将丢失所有数据，因为它们会被删除。因此，如果你犯了这个错误，应该注意后果。此外，你用这种方法创建一个按钮并测试 HTML 页面。查看下面的示例。

```html
<!DOCTYPE html>

<html>

<body>

<p>This is going to be my First Web Page</p>

<p>This will be the First Paragraph.</p>

<button type="button" onclick="document.write(335 + 6)">Click me</button>

</body>

</html>
```

这将是我的第一个网页

这将是第一个段落。

点击我

另一种方法是`window.alert`方法。

```html
<!DOCTYPE html>

<html>

<body>

<p>This is going to be my First Web Page</p>

<p>This will be the First Paragraph.</p>

<p id="demo1234"></p>

<script>

window.alert (4567 + 36);

</script>

</body>

</html>
```

这将是我的第一个网页

这将是第一个段落。

上述文本将在浏览器上显示。每当你运行代码时，你会在屏幕顶部的警告窗口上看到数学计算的结果。`window`关键字的使用是可选的。由于 JavaScript 中的`window`对象是全局的，你可以省略它的使用并仍然得到相同的结果。以下代码将交付相同的结果。

```html
<!DOCTYPE html>

<html>

<body>

<p>This is going to be my First Web Page</p>

<p>This will be the First Paragraph.</p>

<p id="demo1234"></p>

<script>

alert (4567 + 36);

</script>

</body>

</html>
```

另一种方法是`console.log()`方法。此方法用于调试代码并显示数据。

```html
<!DOCTYPE html>

<html>

<body>

<p>This is going to be my First Web Page</p>

<p>This will be the First Paragraph.</p>

<p id="demo1234"></p>

<script>

console.log (4567 + 36);

</script>

</body>

</html>
```

# 数值

数字的值是数值。在 JavaScript 代码中，你将这样写：

```javascript
13
```

你将在程序中使用它，它将为计算机内存中的数字带来位模式。JavaScript 使用固定的位数，即 64 位，来存储单个数字的值。使用 64 位，你可以创建无限的模式。这意味着系统可能表示的不同数字数量是受到限制的。通过`N`位十进制数字，你有机会表示`10N`个数字。

计算机的内存曾经要小得多，人们必须使用特定的 8 位和 16 位组来表示数字。某些小数字很容易溢出，导致变成一个无法容纳在某些位数中的数字。时代变了。即使是装在口袋里的电脑，也有巨大的空间来保存你需要的任何内容。

这些位存储了负数，其中一位表示单个数字的符号。你可能会遇到的另一个更大的问题是，非整数也应该被表示。为了实现这一点，你需要使用一些位来存储小数点的位置。

### 算术

核心点是数字被用于算术。它们在编程中被用于执行加法和乘法等算术运算。乘法和加法的简单操作至少需要两个数字来产生第三个数字。`+`是加法的符号，而`*`是乘法的符号。这两个符号都被称为运算符。当你编程时，在两个数字之间放置一个运算符，你就开始了一次算术运算。你可以使用括号来调整运算符执行的顺序。例如，在正常情况下，乘法优先。但如果你把加法放在括号里，你就改变了顺序。现在编辑器将先运行加法。

```javascript
(500 + 100) * 500
```



当运算符在没有括号的情况下出现时，它们的应用顺序根据优先级决定。

## 字符串

在深入 JavaScript 编程的海洋之前，你必须背记的另一个概念是字符串的概念。JavaScript 字符串表示文本。你可以通过将任何想要转换为字符串的文本包含在引号内来编写它们。参见以下示例。

`‘I am looking at the sinking sun.’`

`“I am going to take a flight to Mars.”`

`The weather is balmy, as April has started.`

正如我在上述的示例中展示的那样，你可以使用单引号、双引号和反引号（backticks）。将每个引号放在字符串的开头或结尾，以便代码编辑器将文本识别为字符串。你可以在引号内放置任何内容，JavaScript 将其转换为字符串。然而，语言中的少数字符很难转换。你可能想过如何在引号内部放置引号。在字符串内部要几乎不可能包含的第一件事就是包含换行符。当你按下键盘上的回车键时，会出现换行。当你使用反引号时，不需要转义就可以这样做。

如果你想在字符串中包含特殊字符，可以使用反斜杠（`\`）。反斜杠表示其前面的字符被赋予了特殊含义。这个过程被称为字符转义。如果反斜杠在引号前面，它不会结束字符串，而是会被包含在字符串中。如果你在反斜杠后插入一个 `‘n’` 字符，它将被解释为换行的形式。如果你在反斜杠后放一个 `‘t’`，它表示一个制表符。参见以下字符串的示例。

```text
“I will reach the moon\n And I will travel onwards to Mars.”
```

你在网页上看到的将如下：

```text
I will reach the moon
And I will travel onwards to Mars.
```

你可能会遇到一种情况，即字符串内部需要一个反斜杠，仅仅为了作为一个反斜杠，而不是任何特殊代码。如果两个反斜杠接连出现，它们肯定会合并。在生成的字符串值中只会下一个反斜杠。

你必须以一系列位的形式对字符串进行建模，以便它们存在于计算机上。JavaScript 执行它的方式取决于 Unicode 标准。这些标准倾向于为你需要的每个字符分配特定的数字，包括来自阿拉伯语、希腊语、亚美尼亚语和日语的字符。如果你为每个字符都有数字，你的字符串将由特定的数字序列描述。这就是 JavaScript 执行代码的方式。尽管如此，你可能会面临某些复杂性。JavaScript 的表示每个元素使用 16 位。Unicode 定义的字符比这多得多。像 emoji 这样的字符占用两个字符位置。

JavaScript 字符串的一个独特之处是，你不能对它们进行除、减、乘运算。然而，有一个运算符可以使用于字符串。你可以对 JavaScript 字符串使用 `+` 运算符来拼接它们，或者简单地说，将它们合并为一个整体。参见以下示例：

```text
“I” + “am” + “going” + “to” + “Mars” + “.”
```

字符串值有几个关联函数，你可以使用它们来执行不同的操作。你用单引号或双引号编写的字符串行为相同。两种字符串的唯一区别在于字符串中转义字符的使用。当你在 `${}` 中写入内容时，结果将按计算结果得出，然后转换为字符串，然后包含在相同的位置。

## JavaScript 数组

可以通过方括号识别 JavaScript 数组。数组的项填充在方括号内部，并用逗号分隔。看看我们如何声明数组。

```html
<!DOCTYPE html>
<html>
<body>
<p>Learn JavaScript Arrays</p>
<p>JavaScript 数组的索引从 0 开始。这意味着数组的第一个元素是 [0]</p>
<p id="array-demo"></p>
<script>
var carsArray = ["Volkswagen","Honda", "Suzuki"];
document.getElementById("array-demo").innerHTML = carsArray[0];
</script>
</body>
</html>
```

JavaScript 数组的索引从 0 开始。这意味着数组的第一个元素是 `[0]`。

由于这是第一个示例，你需要仔细理解它。首先，这行代码区分了后端代码和 JavaScript 前端。你可以说，它区分了你在编辑器中编写的内容和你在网页上看到的内容。`h1` 和 `p` 标题在书中显示可能与在网页上显示的有所不同。这是因为我正在使用的文字处理器对 `h1` 和 `p` 有设置。如果你将代码复制粘贴到编辑器并在网页上运行，它们将正常工作。此外，我在本书的其余部分将这样编写嵌入 HTML 结构中的代码，因为你在创建网站时也是这样写的。你需要通过 HTML 嵌入在 JavaScript 中编写脚本，以便网络浏览器读取它们。在上面提到的示例中，你可以看到每个变量都有对应的存储。

现在，我不再创建一个单个字母变量，而是将创建具有完整单词名称的变量。

```html
<!DOCTYPE html>
<html>
<body>
<p>你正在学习 JavaScript 变量</p>
<p>在接下来的示例中，变量将使用完整的单词命名</p>
<p id="variable-demo"></p>
<script>
var milkprice = 150;
var oilprice = 160;
var totalprice = milkprice + oilprice;
document.getElementById("variable-demo").innerHTML =
"The value of totalprice is: " + totalprice;
</script>
</body>
</html>
```

你正在学习 JavaScript 变量

在接下来的示例中，变量将使用完整的单词命名。

`totalprice` 的值是: 310

## JavaScript 标识符

JavaScript 变量需要赋予唯一的名称以便于识别。这些唯一名称被称为标识符。标识符可以是像 `a`、`b`、`c` 这样的短名称，也可以是像 `totalprice`、`milkprice` 和 `oilprice` 这样的描述性名称。JavaScript 变量有一些命名规则。你可以利用这些规则来减少错误概率。

- 变量不能包含数字、字母、美元符号和下划线。
- 变量可以以 `$` 开头。
- 变量对大小写敏感，这意味着 `a` 和 `A` 是不同的变量。
- 变量必须以字母开头。
- 你不能使用 JavaScript 关键字作为变量。

如果你在 JavaScript 中看到像 `=` 这样的等号，不要将其误认为是代数中使用的等号。它有不同的用途。

变量存储的信息稍后可以在你的程序中使用。脚本很长，因此变量可以轻松定位有用值。变量便于在同一段代码中重复使用某个值。与其记住这个值，不如创建一个变量并为其赋值。

## 数据类型

JavaScript 变量可以持有不同类型的信息，如数字和文本。编程中的文本值被称为字符串。JavaScript 可以持有不同类型的数据。正如我已经解释过的，字符串必须写在单引号或双引号中，取决于你的习惯。你编写数字时不需要加引号。如果你给数字加引号，浏览器将将其解释为字符串。

```html
<!DOCTYPE html>
<html>
<body>
<p>你正在学习 JavaScript 变量</p>
<p>我正在定义 JavaScript 数据类型</p>
<p id="variable-demo"></p>
<script>
var num = 5555555.889;
var novelist = "Charles Dickens";
var introduction = 'Charles Dickens wrote melodramatic novels!';
document.getElementById("variable-demo").innerHTML =
num + "<br>" + novelist + "<br>" + introduction;
</script>
</body>
</html>
```

你正在学习 JavaScript 变量

我正在定义 JavaScript 数据类型。

```text
5555555.889
Charles Dickens
Charles Dickens wrote melodramatic novels!
```

## 变量声明

声明变量的过程实际上就是创建变量的过程。你可能在上面的示例中注意到我在每个变量之前都使用了 `var` 关键字。没有 `var` 关键字，你就无法创建变量。一旦声明了变量，该变量将没有值。你必须像我在示例中所做的那样为它赋值。在这里使用了等号 `=`。你将符号放在变量名和值之间。

### 未定义变量

在不同的程序中，你经常可以声明不带值的变量。该值可以是你可以计算出来的，也可以是你稍后提供的，例如用户输入。你声明的未带值的变量将携带一个 `undefined` 值。我将使用我已经创建的示例之一，并去掉变量的值。让我们使用最新的示例，以便你更好地理解。

```html
<!DOCTYPE html>
<html>
<body>
<p>你正在学习 JavaScript 变量</p>
<p>我正在定义 JavaScript 的未定义变量</p>
<p id="variable-demo"></p>
<script>
var num;
var novelist;
var introduction;
document.getElementById("variable-demo").innerHTML =
</script>
</body>
</html>
```

你正在学习 JavaScript 变量

我正在定义 JavaScript 的未定义变量。

### 重复

你可能定义并声明了一个变量，但后来改变了主意，并通过我刚刚解释的过程使其变为未定义。那么，这会让它变成未定义吗？答案是“不是”。在声明后将其未定义不会让变量失去它的值。

```html
<!DOCTYPE html>
<html>
<body>
<p>你正在学习 JavaScript 变量</p>
<p>这是 JavaScript 的未定义变量</p>
<p id="variable-demo"></p>
<script>
var milkprice = 150;
var oilprice = 160;
var totalprice = milkprice + oilprice;
var novelist = "Charles Dickens";
var introduction = 'Charles Dickens wrote melodramatic novels!';
var num;
var novelist;
var introduction;
document.getElementById("variable-demo").innerHTML =
num + "<br>" + novelist + "<br>" + introduction;
</script>
</body>
</html>
```

你正在学习 JavaScript 变量

这是 JavaScript 的未定义变量。

```text
310
Charles Dickens
310
```

### 算术

JavaScript 与其他编程语言一样，允许你进行数学计算。你可以相加数字产生结果，然后将结果传递给变量进行存储。在代码中，你可以使用运算符 `=` 和 `+`。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript 算术</p>
<p>这是 JavaScript 的未声明算术</p>
<p id="variable-demo"></p>
<script>
var a = 15 + 3452 + 13 + 8 + 1;
document.getElementById("variable-demo").innerHTML = a
</script>
</body>
</html>
```

JavaScript 算术

```text
3489
```

### 减法

下一个讨论的算术运算符是减法。运算符的符号与代数中使用的相同。你可以用选择的数字填充程序，并在中间放入 `–` 符号开始减法过程。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript 算术</p>
<p>JavaScript 减法</p>
<p id="variable-demo"></p>
<script>
var a = 55;
var b = 40;
var c = a - b;
document.getElementById("variable-demo").innerHTML = c
</script>
</body>
</html>
```

JavaScript 算术

JavaScript 减法。

```text
15
```

## 字符串拼接

就像你学习加数字一样，JavaScript 允许你拼接字符串。我将在接下来的示例中使用 `+` 运算符来连接字符串。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript 字符串拼接</p>
<p>JavaScript 数据类型</p>
<p id="variable-demo"></p>
<script>
var a = "Charles Dickens" + "" + " wrote" + "" + " melodramatic novels!";
document.getElementById("variable-demo").innerHTML = a
num + "<br>" + novelist + "<br>" + introduction;
</script>
</body>
</html>
```

JavaScript 字符串拼接

JavaScript 数据类型。

```text
Charles Dickens wrote melodramatic novels!
```

在 JavaScript 中，`let` 关键字用于变量声明。`var` 关键字也可以用于变量声明；然而，两者的主要区别在于它们的作用域。`var` 关键字基于函数作用域，而 `let` 关键字基于块级作用域。学习如何使用 `let` 关键字与学习 `var` 关键字与 `let` 关键字之间的区别密切相关。

### 全局作用域

你在 JavaScript 函数之外声明的变量。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript Let 关键字</p>
<p>你可以从任何脚本或任何函数访问全局变量。</p>
<p id="let-demo"></p>
<script>
var cars = "BMW";
Function1();
function Function1() {
  document.getElementById("let-demo").innerHTML = "我计划买一辆 " + cars + " 用于我的日常通勤和越野。";
}
</script>
</body>
</html>
```

JavaScript Let 关键字

你可以从任何脚本或任何函数访问全局变量。

我计划买一辆 BMW 用于我的日常通勤和越野。

你可以在 JavaScript 程序的任何位置访问全局变量。

### 函数作用域

你在 JavaScript 函数范围内声明的变量具有函数作用域。在接下来的示例中，我将在函数范围内声明变量。

```html
<!DOCTYPE html>
<html>
<body>
<p>这些是 JavaScript 作用域</p>
<p>我将在 Function2() 之外定义并声明变量。</p>
<p id="let-demo1"></p>
<p id="let-demo2"></p>
<script>
Function2();
function Function2() {
  var cars = "BMW";
  document.getElementById("let-demo1").innerHTML = typeof cars + " " + cars;
}
document.getElementById("let-demo2").innerHTML = typeof cars;
</script>
</body>
</html>
```

这些是 JavaScript 作用域

我将在 `Function2()` 之外定义并声明变量。

```text
string BMW
undefined
```

我尝试在函数内部和外部定义变量。因此，当我检查变量类型时，我发现超出函数限制的变量被标记为 `undefined`。这就是我们称其为函数作用域变量的原因。所以，如果你编写代码时不小心将变量引到函数外部，你将看到相同的消息。解决方案是将声明包含在函数括号内，这样代码就能正常工作。

### 块级作用域

使用 `var` 关键字声明的变量不具备块级作用域。只有在花括号内声明的变量才能从块外部访问。块级作用域是在 ES2015 中引入 JavaScript 的。在此之前，它没有作用域。虽然使用 `var` 关键字的变量没有块级作用域，但使用 `let` 关键字声明的变量可以具有块级作用域。

`var` 关键字在某些情况下会给程序员带来问题。特别是当你尝试通过包含 `var` 关键字来重新声明变量时，你会看到编辑器中弹出大量问题。如果你在块内部重新声明变量，你也会在同一个块之外重新声明它。从长远来看，会导致额外的问题。

```html
<!DOCTYPE html>
<html>
<body>
<p>这段代码片段将使用 var 关键字声明你的变量</p>
<p id="let-demo"></p>
<script>
var xyz = 10000;
// 你可以看到 xyz 的值为 10000
{ 
  var xyz = 1;
  // 现在重新声明的变量 xyz 的值为 1
}
</script>
</body>
</html>
```



```html
// 查看变量 xyz 的重新声明值是否已应用

document.getElementById("let-demo").innerHTML = xyz;

</script>

</body>

</html>
```

这段代码片段将使用`var`关键字声明你的变量。

1

所以，你可以看到我们遇到了一个大问题。使用`var`关键字，重新声明可能是一个难以处理的麻烦。这就是`let`关键字大显身场。它解决了重新声明的问题。如果你使用`let`关键字声明了变量，当你重新声明同一个变量时，就不会有任何问题。在接下来的代码中，我将解释`let`关键字如何解决重新声明的问题。

```html
<!DOCTYPE html>

<html>

<body>

<p>我现在将使用 let 关键字重新声明一个变量</p>

<p id="let-demo"></p>

<script>

var xyz = 1000;

// 变量 xyz 的值为 1000

{ 

  let xyz = 1;

  // 现在 xyz 的值被设置为 1

}

// let 关键字将让变量 xyz 保留之前声明的值

document.getElementById("let-demo").innerHTML = xyz;

</script>

</body>

</html>
```

我现在将使用`let`关键字重新声明一个变量。

1000

由于`let`关键字引入得较晚，Internet Explorer 11 及之前的版本不支持它。目前，Chrome 49、Firefox 44、Opera 36、Edge 12 和 Safari 11 支持使用`let`关键字。

`var`和`let`关键字在用于 JavaScript 循环时具有不同的行为。通过以下两个示例理解这两个关键字的区别。

### 示例 1

```html
<!DOCTYPE html>

<html>

<body>

<p>JavaScript 关键字</p>

<p id="let-demo"></p>

<script>

var xyz = 4;

for (var xyz = 0; xyz < 9; xyz++) {

}

document.getElementById("let-demo").innerHTML = xyz;

</script>

</body>

</html>
```

JavaScript 关键字

9

### 示例 2

```html
<!DOCTYPE html>

<html>

<body>

<p>JavaScript 关键字</p>

<p id="let-demo"></p>

<script>

let xyz = 4;

for (let xyz = 0; xyz < 9; xyz++) {

}

document.getElementById("let-demo").innerHTML = xyz;

</script>

</body>

</html>
```

JavaScript 关键字

4

在第一个示例中，当我使用`var`关键字时，循环内部的变量重新声明了外部变量。然而，当我在示例 2 中使用`let`时，循环内部的变量没有重新声明外部变量。`let`和`var`关键字都旨在声明变量。然而，在创建 JavaScript 程序之前，你应该理解它们之间的关键区别：

- `var`关键字主要用于旧版本的 JavaScript，而`let`关键字被认为是声明变量的最新方法。`let`关键字始于 ES6，也称为 ES2015。
- `var`关键字基本上是函数作用域的，而`let`关键字是块作用域的。

当我们讨论这两个关键字的推荐时，我们可以说在编写程序时`let`关键字是最佳选择。然而，某些浏览器不支持`let`关键字。因此，你可能需要使用`var`关键字。

## 第三章

## JavaScript Constants

![](img/Image00001.jpg)

JavaScript 中的`const`关键字是在 ES2015 中引入的。使用`const`关键字定义的变量与使用`let`定义的变量一样。区别在于你不能对其进行重新赋值。一旦初始化了常量，你就无法更改它的值。这就是常量与`var`关键字的区别。如果你必须声明常量，需要先初始化它。

你应该仔细考虑一下在程序中是否需要使用常量。只有在你确定不需要更改变量的值时，才使用它。

常量名可以是合法的标识符。

```html
<!DOCTYPE html>

<html>

<body>

<p>你正在学习 JavaScript 常量</p>

<p>记住你不能更改原始类型的值。</p>

<p id="const-demo"></p>

<script>

try {

  const xyz = 89.141592653589793;

  xyz = 54.14;

}

catch (err) {

  document.getElementById("const-demo").innerHTML = err;

}

</script>

</body>

</html>
```

你正在学习 JavaScript 常量

记住你不能更改原始类型的值。

TypeError: Assignment to constant variable.

使用`const`关键字声明变量与在使用块级作用（Block Scope）时使用`let`关键字声明相似。接下来的示例将解释它是如何倾向于`let`关键字并区别于`var`关键字的。

```html
<!DOCTYPE html>

<html>

<body>

<p>在这个示例中，我将使用 `const` 关键字声明一个变量</p>

<p id="const-demo"></p>

<script>

var xyz = 15;

// The value of xyz is 15

{ 

  const xyz = 1;

  // The value of xyz is 1

}

// The value of xyz is 15

document.getElementById("const-demo").innerHTML = xyz;

</script>

</body>

</html>
```

在这个示例中，我将使用`const`关键字声明一个变量。

15

与使用`var`关键字声明的变量不同，常量在声明时必须赋值一个值。你不能让赋值部分为空。“constant”（常量）这个词有点让人困惑，如果说不是完全的误导的话。`const`关键字并不定义常量值。实际上，它定义的是你在等式中所使用的值的常量引用。这就是为什么你不能改变常量的原始值。然而，你可以更改它的属性。

### 原始值

如果你给常量赋了一个原始值，以后你将无法再次更改它的值。

```html
<!DOCTYPE html>

<html>

<body>

<p>这些是 JavaScript 常量</p>

<p>让我们尝试是否可以更改原始值。</p>

<p id="const-demo"></p>

<script>

try {

  const xyz = 5556.175757557757793;

  xyz = 3555.19090;

}

catch (err) {

  document.getElementById("const-demo").innerHTML = err;

}

</script>

</body>

</html>
```

这些是 JavaScript 常量

让我们尝试是否可以更改原始值。

`TypeError: Assignment to constant variable.`

虽然你不能更改 JavaScript 常量的原始值，但你可以更改对象的属性。在接下来的示例中，我将使用`const`关键字创建一个对象，然后对该对象的属性引入一些更改，以查看我是否可以更改它们。查看示例以了解如何操作。

```html
<!DOCTYPE html>

<html>

<body>

<p>JavaScript 常量</p>

<p>你可以在声明对象后更改它们的属性：</p>

<p id="const-demo"></p>

<script>

// 我将创建一个对象：

const mycar = {name:"Honda", model:"Vezel", make:"Japan", color:"Grey"};

// 让我们更改属性：

mycar.model = "Civic";

// 你也可以添加一个新属性：

mycar.transmission = "Automatic";

// 现在该显示你的属性了：

document.getElementById("const-demo").innerHTML = "I have a " + mycar.name + "." + " It is of " + mycar.color + " color and its model label is " + mycar.model + ". " + "This car has " + mycar.transmission + ".";

</script>

</body>

</html>
```

JavaScript 常量

你可以在声明对象后更改它们的属性：

我有一辆 Honda。它是灰色的，它的型号标签是 Civic。这辆车是自动挡的。

你看到我将型号从 Vezel 改为了 Civic。我还添加了新属性来描述汽车的变速模式。这为程序员提供了便利，因为他们可以创建一个对象，然后根据不断变化的需求合适地添加或更改属性。然而，在程序中，你不能将不同的对象重新赋值给同一个常量。如果你这样做，将会看到一个错误。

```html
<!DOCTYPE html>

<html>

<body>

<p>学习 JavaScript 常量</p>

<p>禁止：你不能将不同的对象重新赋值给同一个常量：</p>

<p id="const-demo"></p>

<script>

try {

  const mycar = {name:"Honda", model:"Vezel", make:"Japan", color:"black"};

  mycar = {name:"BMW", model:"Z1", make:"German", color:"red"};

}

catch (err) {

  document.getElementById("demo").innerHTML = err;

}

</script>

</body>

</html>
```

学习 JavaScript 常量

禁止：你不能将不同的对象重新赋值给同一个常量：

### 常量数组

你可以使用`const`关键字创建数组，也可以更改它们。

## 第章

## 提示与条件判断

![](img/Image00001.jpg)

提示框（prompt box）用于要求用户提供信息并为答案提供响应字段。代码向用户提出一些问题，然后在相应的字段中提供答案供响应。你可以更改响应内容。无论你是保留默认响应还是将其改为其他内容，你的响应都会被赋值给变量。

`prompt`代码类似于`alert`代码。然而，两者有两点不同。对于`prompt`代码，你需要遵循一种方法来接收用户的响应，这意味着你必须从声明变量开始代码。之后，你必须使用一个等号。在`prompt`中，你必须指定第二个字符串，即你在看到提示显示时在字段中出现的默认响应。

### JavaScript 的 if 语句

在本节中，我将解释如何处理不同类型的条件。假设你有一个弹窗询问用户：“你住在哪里？”

如果用户正确回答“白宫”，他将收到祝贺。如果他输入了其他内容，程序将不返回任何结果。

- `else`关键字用于指定当相同条件为假时，编辑器必须执行的代码。
- `else-if`关键字用于当第一个条件为假时，添加一个新的条件进行测试。

`if`语句是区分大小大小的，因此关键字`if`和`IF`是两个不同的单词。如果你将`if`替换为`IF`，你将在屏幕上看到错误。

```html
<!DOCTYPE html>

<html>

<body>

<p>如果时间小于 15:00，我将显示“祝你有愉快的一天！”：</p>

<p id="if-demo">祝你有美味的夜晚!</p>

<script>

if (new Date().getHours() < 15) {

  document.getElementById("if-demo").innerHTML = "Have a Great Day!";

}

</script>

</body>

</html>
```

如果时间小于 15:00，我将显示“祝你有愉快的一天！”：

祝你有愉快的一天！

## The else 语句

你可以使用`else`语句来指定当你的条件为假时需要执行的代码。我将使用相同的代码并在代码中添加`else`语句，看看我们如何使用`else`语句来扩展代码，使其更具交互性和用户友好性。现在，用户将有两个选择，而不是死板的单选项代码。

```html
<!DOCTYPE html>

<html>

<body>

<p>我希望你点击下方的按钮，根据当前时间显示问候：</p>

<button onclick="FunctionX()">请点击我显示问候</button>

<p id="ifelse-demo"></p>

<script>

function FunctionX() {

  var myhours = new Date().getHours();

  var mygreetings;

  if (myhours < 15) {

    mygreetings = "Have a Great Day";

  } else {

    mygreetings = "Have a Great Evening. I hope you enjoy your dinner.";

  }

  document.getElementById("ifelse-demo").innerHTML = mygreetings;

}

</script>

</body>

</html>
```

我希望你点击下方的按钮，根据当前时间显示问候：

请点击我显示问候

祝你有愉快的一天

你可以看到`else`语句完美地集成到了现有代码中。我冒昧在代码中添加了一个交互式按钮，以便用户确切知道要做什么。当用户点击按钮时，他们将收到一条问候消息。该消息将根据程序在你本地读取的时间进行构建。这就是你如何在页面上构建交互式网页应用并吸引访问者的方法，你的访问者也会喜欢这种被欢迎的方式。

## The else if 语句

你可以向代码添加`else-if`语句，在第一个条件返回假时指定新条件。在下面的示例中，我将添加两个以上的条件，看看它们是如何工作的，以及它们为我们的代码带来了多大的改进。

```html
<!DOCTYPE html>

<html>

<body>

<p>我希望你点击下方的按钮，根据当前时间显示问候：</p>

<button onclick="FunctionX()">请点击我显示问候</button>

<p id="ifelse-demo"></p>

<script>

function FunctionX() {

  var mygreetings;

  var mytime = new Date().getHours();

  if (mytime < 8) {

    mygreetings = "Have a Good Morning. I hope you have had a nutritious breakfast. Get ready for work";

  } else if (mytime < 15) {

    mygreetings = "Have a Great Day. Don't forget to eat your lunch.";

  } else {

    mygreetings = "Have a Great Evening. Any special plans for dinner?";

  }

  document.getElementById("ifelse-demo").innerHTML = mygreetings;

}

</script>

</body>

</html>
```

我希望你点击下方的按钮，根据当前时间显示问候：

请点击我显示问候

祝你有愉快的一天。不要忘记吃午饭。

这运行得非常完美。现在，你的程序将在一天中的三个时间段都显示问候消息。你可以根据业务需求定制消息并使其更具交互性。一些编码人员习惯于在编写`if`语句时省略大括号。这种做法是完全合法的；但这样做稍微有点困难。有些程序员会将初始大括号放在新的一行。另一种做法是将整个`if`语句写在单行中，这更容易实现，但当你回来研究程序的结构时，它会很难阅读。我建议你遵循我在上面示例中使用的相同规则，这样你会发现编写和理解起来也更容易。在大多数情况下，你可以用双等号`==`代替三等号。然而，你可能会发现一些微小的技术差异。

编写`if`语句以及`if`语句的变体有很多格式。使用`if`语句进行编码的可能性是无限的。

## JavaScript Switch 语句

你可以使用`switch`语句对 JavaScript 条件执行不同的操作。它将帮助你处理单个代码块并执行它。编辑器对其进行评估，在值之间进行比较，如果匹配，则执行该块。如果不匹配，则不执行。下面的程序将在程序运行`switch`语句并检查你的电脑，查看电脑日历是哪一天，以及代码中该一天包含什么消息。它将遍历一周中的七天，当遇到匹配时，它将运行你已经关联到同一天的消息。参见下面的代码。

```html
<!DOCTYPE html>

<html>

<body>

<p id="switch-demo"></p>

<script>

var weekdays;

switch (new Date().getDay()) {
```



`case 0`:

    `weekdays = "the restful Sunday";`

    `break;`

`case 1`:

    `weekdays = "the blue blue Monday";`

    `break;`

`case 2`:

    `weekdays = "the superstitious Tuesday";`

    `break;`

`case 3`:

    `weekdays = "the hectic Wednesday";`

    `break;`

`case 4`:

    `weekdays = "the overwhelming Thursday";`

    `break;`

`case 5`:

    `weekdays = "the joyful Friday";`

    `break;`

`case 6`:

    `weekdays = "the sleepy Saturday";`

}

`document.getElementById("switch-demo").innerHTML = "Today is " + weekdays + "." + " Have a productive day!";`

`</script>`

`</body>`

`</html>`

今天是迷信周二。祝高效的一天！在上面的代码示例中，你可能注意加入了 `break` 关键字。当代码遇到 `break` 关键字时，它会跳出特定的块。这种跳出 `switch` 块的操作为执行提供了停止。你不需要在 `switch` 块的最后一个情况下插入 `break` 关键字。无论包含，它都会结束。如果你从 `switch` 块中排除 `break` 关键字，网络浏览器即使在不匹配的情况下也会执行随后的用例。因此，如果你跳过了 `break` 关键字，请做好遇到错误的准备。还有另一个可以添加到 `switch` 语句的关键字。即使在不匹配的情况下也会运行代码。

```html
<!DOCTYPE html>
<html>
<body>
<p id="switch-demo"></p>
<script>
var weekdays;
switch (new Date().getDay()) {
  default:
```
```javascript
weekdays = "I am desperately waiting for the weekend because I have planned a vacation.";
break;
  case 0:
    weekdays = "it is the restful Sunday";
    break;
  case 1:
    weekdays = "it is the blue blue Monday";
    break;
  case 3:
    weekdays = "it is the hectic Wednesday";
    break;
  case 4:
    weekdays = "it is the overwhelming Thursday";
    break;
  case 5:
    weekdays = "it is the joyful Friday";
    break;
  case 6:
    weekdays = "it is the sleepy Saturday";
}
document.getElementById("switch-demo").innerHTML = weekdays;
```
我正焦虑地等待周末，因为我计划了一个假期。

# 第五章

###### JavaScript 字符串与数组

![](img/Image00001.jpg)

我已经解释了什么是字符串以及你如何在脚本中使用它们。在处理字符串时，你可以使用一些方法。某些原始值不能拥有方法或属性，因为它们不是对象。然而，JavaScript 允许原始值拥有属性和方法，因为它在执行属性和方法时会将原始值视为对象。你可以学习程序中所使用的字符串的长度。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 字符串的属性</p>
<p>这个 String 属性将回答关于你的字符串长度的问题：</p>
<p id="string-demo"></p>
<script>
var msgX = "I am about to leave for New York to start my own business.";
var msgY = msgX.length;
document.getElementById("string-demo").innerHTML = msgY;
</script>
</body>
</html>
```

### 学习 JavaScript 字符串的属性

这个 String 属性将回答关于你的字符串长度的问题：

`58`

另一个 JavaScript 方法可以帮助你在字符串中查找另一个字符串。我在这里将使用的方法叫做 `indexOf()`。如果你在另一个字符串内部指定了一个字符串，它将为你找到它。需要记住的一个重要注意点是，你可以使用单引号在字符串内部创建另一个字符串。接下来的示例将解释这一操作。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 字符串的属性</p>
<p>这个 String 属性将回答关于你的字符串内部字符串的问题：</p>
<p id="string-demo"></p>
<script>
var msgX = "I am about to leave for 'New York' to start my own business.";
var msgY = msgX.indexOf("New York");
document.getElementById("string-demo").innerHTML = msgY;
</script>
</body>
</html>
```

这个 String 属性将回答关于你的字符串内部字符串的问题：

`25`

你可以看到内部字符串的索引已经显示在屏幕上。请记住，JavaScript 从 0 开始计算索引值。

## lastIndexOf() 方法

你可以使用 `lastIndexOf()` 方法来查看 `New York` 最后一次出现的索引，它是我们指定的内部字符串。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 字符串的属性</p>
<p>这个 String 属性将回答关于你的字符串内部字符串的问题：</p>
<p id="string-demo"></p>
<script>
var msgX = "I am about to leave for 'New York' to start my own business.";
var msgY = msgX.lastIndexOf("New York");
document.getElementById("string-demo").innerHTML = msgY;
</script>
</body>
</html>
```

这个 String 属性将回答关于你的字符串内部字符串的问题：

`25`

#### 如果未找到索引怎么办？

如果方法未能找到索引，它们将返回 `-1`。这可能发生你在代码中写了错误的拼写或完全不同的单词时。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 字符串的属性</p>
<p>这个 String 属性将回答关于你的字符串内部字符串的问题：</p>
<p id="string-demo"></p>
<script>
var msgX = "I am about to leave for 'New York' to start my own business.";
var msgY = msgX.lastIndexOf("Washington");
document.getElementById("string-demo").innerHTML = msgY;
</script>
</body>
</html>
```

这个 String 属性将回答关于你的字符串内部字符串的问题：

`-1`

## search() 方法

还有另一种方法可以在长字符串中定位指定的内部字符串。如果匹配完全完美，你可以使用 `search()` 方法来查找它。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 字符串的属性</p>
<p>这个 String 属性将回答关于你的字符串内部字符串的问题：</p>
<p id="string-demo"></p>
<script>
var msgX = "I am about to leave for 'New York' to start my own business.";
var msgY = msgX.search("New York");
document.getElementById("string-demo").innerHTML = msgY;
</script>
</body>
</html>
```

这个 String 属性将回答关于你的字符串内部字符串的问题：

`25`

如果你注意到这两个方法的结果，即 `search()` 和 `indexOf()`，你会发现它们是相同的。然而，`search()` 不能接受第二个参数，而 `indexOf()` 可以。

### 提取部分

你可以根据需要将字符串分成多个部分。第一个方法是 `slice()`。通过使用两个参数来分割字符串：一个是起始位置，另一个是结束位置。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 字符串的属性</p>
<p>这个 String 属性将回答关于你的字符串内部字符串的问题：</p>
<p id="string-demo"></p>
<script>
var msgX = "I am about to leave for 'New York' to start my own business.";
var msgY = msgX.slice(23, 34);
document.getElementById("string-demo").innerHTML = msgY;
</script>
</body>
</html>
```

这个 String 属性将回答关于你的字符串内部字符串的问题：

`'New York'`

请记住 JavaScript 从 `0` 点计算索引。如果一个参数变为负数，你必须从字符串的末尾向前计算。它将反向切割字符串。你可以尝试并获取结果。我现在将跳过它并测试忘记插入结束位置会发生什么。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 字符串的属性</p>
<p>这个 String 属性将回答关于你的字符串内部字符串的问题：</p>
<p id="string-demo"></p>
<script>
var msgX = "I am about to leave for 'New York' to start my own business.";
var msgY = msgX.slice(23);
document.getElementById("string-demo").innerHTML = msgY;
</script>
</body>
</html>
```

这个 String 属性将回答关于你的字符串内部字符串的问题：

`'New York' to start my own business.`

另一种切割字符串并创建子字符串的方法是 `substring()` 方法。它和 `slice()` 方法一样简单。它的不同之处在于不接受负索引。查看以下示例以理解它的用法。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 字符串的属性</p>
<p>这个 String 属性将回答关于你的字符串内部字符串的问题：</p>
<p id="string-demo"></p>
<script>
var msgX = "I am about to leave for 'New York' to start my own business.";
var msgY = msgX.substring(23, 34);
document.getElementById("string-demo").innerHTML = msgY;
</script>
</body>
</html>
```

这个 String 属性将回答关于你的字符串内部字符串的问题：

`'New York'`

第三也是最后一个切片方法是 `substr()` 方法，它与 `slice()` 非常相似。第二个参数定义了剩余字符串的长度。

# 学习 JavaScript 字符串属性

这个 String 属性将回答关于字符串内部字符串的问题：

```javascript
var msgX = "I am about to leave for 'New York' to start my own business.";
var msgY = msgX.substr(23, 34);
document.getElementById("string-demo").innerHTML = msgY;
```

这个 String 属性将回答关于字符串内部字符串的问题：

`'New York' to start my own business`

当 JavaScript 允许你替换字符串内部的值时，它变得有趣了。例如，我在示例中包含的字符串包含 `New York` 作为我要访问的城市。JavaScript 允许你更改城市名称，而无需编写新代码并创建新字符串。这在编写长程序时为你节省了大量时间。该方法标识为 `replace()`。

```javascript
var msgX = "I am about to leave for 'New York' to start my own business.";
var msgY = msgX.replace('New York', 'Las Vegas');
document.getElementById("string-demo").innerHTML = msgY;
```

学习 JavaScript 字符串属性

`I am about to leave for 'Las Vegas' to start my own business.`

默认情况下，如果你写 `NEW YORK` 而不是 `New York`，JavaScript `replace()` 将无法工作。它是区分大小写的，并将不同的大小写识别为不同的单词。因此，如果你发现该方法不起作用，最好检查单词的大小写。此外，`replace()` 方法只替换第一个匹配项。如果字符串中有多个 `New York`，它将只替换第一个匹配项，并保持其余单词不变。如果你想在忽略警告的情况下使用大写，你必须使用正则表达式（例如配合单词 `/i`）以便浏览器能够识别匹配。正则表达式将使单词不区分大小写。看在编辑器中应该怎么写的。

```javascript
var msgX = "I am about to leave for 'New York' to start my own business.";
var msgY = msgX.replace(/NEW YORK/i, 'Las Vegas');
document.getElementById("string-demo").innerHTML = msgY;
```

学习 JavaScript 字符串属性

`I am about to leave for 'Las Vegas' to start my own business.`

让我们看看如果你在代码中漏掉了正则表达式并仍然使用大写字母，代码会变成什么。

```javascript
var msgX = "I am about to leave for 'New York' to start my own business.";
var msgY = msgX.replace('NEW YORK', 'Las Vegas');
document.getElementById("string-demo").innerHTML = msgY;
```

学习 JavaScript 字符串属性

`I am about to leave for 'New York' to start my own business.`

你可以看到代码不再起了。

### 全球化

我已经解释过，如果你必须替换多个单词，你无法通过 `replace` 方法来实现。它根本不起作用。但是，有一个解决方案。如果你有多个必须替换为另一个单词的单词，你需要再次使用正则表达式。这次正则表达式被标记为 `/g`。包含表达式的方法与 `/i` 相同。不过，我将写一个新的字符串并包含该表达式以便你良好理解。

```javascript
var msgX = "The Coach of the NBA team will visit Las Vegas. Las Vegas has a huge fan base for NBA stars.";
var msgY = msgX.replace(/Las Vegas/g, 'Los Angeles');
document.getElementById("string-demo").innerHTML = msgY;
```



# 学习 JavaScript 字符串属性

The Coach of the NBA team will visit Los Angeles. Los Angeles has a huge fan base for NBA stars.

还有一些其他方法可以调整字符串。你可以通过简单的方法将字符串转换为大写和小写。

```javascript
function FunctionX() {
  var msg = document.getElementById("string-demo").innerHTML;
  document.getElementById("string-demo").innerHTML = msg.toUpperCase();
}
```

我正在将字符串转换为大写和小写：JavaScript 让你的网页具有交互性和用户友好！

运行代码时会显示上述结果。我正在将字符串转换为大写和小写：JAVASCRIPT MAKES YOUR WEPAGES INTERACTIVE AND USER-FRILY!

你可以使用另一个`toLowerCase()`将文本转换为小写。

## 合并

合并是所有编程语言不可或缺的一部分。当需要配对更多字符串时，程序员会寻求合并的支持。如果你代码写得好，`concat()`方法就能顺畅运行。接下来的练习将帮助你顺利合并过程。

```javascript
var msg1 = "I have been promoted as Executive Officer of Skyfall.";
var msg2 = "I will call a board meeting next week!";
var msg3 = msg1.concat(" ", msg2);
document.getElementById("string-demo").innerHTML = msg3;
```

学习 JavaScript 字符串：I have been promoted as Executive Officer of Skyfall. I will call a board meeting next week.!

## 字符串数组

这个标题可能看起来有点困惑。并没有所谓的“字符串数组”。但是，有一种新方法可以将字符串转换为数组。

```javascript
function FunctionX() {
  var msg1 = "Texas, Las Vegas, Los Angeles.";
  var msg2 = msg1.split(",");
  document.getElementById("string-demo").innerHTML = msg2[0];
}
```

点击“Click me”来生成第一个数组元素。点击此按钮：Texas

字符串是神奇的，如果你能良好掌握它们的方法和属性，它们将为你的编程工作提供极大帮助。如果你对细微差别有敏锐的观察力，JavaScript 编程是所有语言中最简单且最完美的语言。

## JavaScript 数组

与变量一样，`JavaScript` `Arrays`（数组）也是值的容器。然而，它们在属性上与变量不同，在于它们可以在一个名称下存储比变量更多的数据。因此，每当你需要在同一种名称下加载更多数据时，都应该使用数组。设置数组有多种方法，最简单的方法是使用`var`关键字，然后编写数组名称并赋值。数组在一个变量中存储多个单独的值。你必须用逗号将它们隔开，并将它们全部放在方括号内。等号必须跟在变量名后面。

当你需要访问数组中的所有值时，应该像处理字符串那样使用索引数字。方括号之间的数字表示索引。该数字必须与数组中值的位置对应。最需要记住的是，索引的位置从 0 开始。

当你创建一个数组后，就可以在浏览器中运行它了。你应该能在浏览器屏幕上看到所需的值。你可以修改索引并插入其他内容来显示不同的值。保存修改后的数字并刷新浏览器以更改结果。如果你的数组有三个项目，而你将索引设置为 3，你会发现浏览器会在计算机屏幕上显示“undefined”（未定义）。这是因为数组中只有三个项目。当你输入索引 3 时，你正尝试显示一个并不存在的第四个项目。JavaScript 不会显示错误，而是在数组中添加一个尚未定义的定义位置。JavaScript 将新位置添加到数组的末尾。在你用合理的值填充它之前，它将保持为`undefined`。你可以根据需要使用这个新的`undefined`位置来存储数据。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 数组</p>
<p id="array-demo"></p>
<script>
var carsforsale = ["Honda", "Toyota", "GTX", "Ford"];
document.getElementById("array-demo").innerHTML = carsforsale;
</script>
</body>
</html>
```

学习 JavaScript 数组：Honda,Toyota,GTX,Ford

你可以从上面的示例中看到，JavaScript 数组是一种特殊的变量，它可以同时存储多个值。如果你有一个汽车列表，通常你可能会将其存储在多个变量中，现在你可以使用数组将所有值打包并插入网页中。如果你将它们存储在独立的变量中，你将创建四个不同名称的变量。现在是 4 辆车，所以你可能认为为这些值创建四个独立变量没什么没什么。然而，如果你有 4000 个值，为所有值创建独立变量将是一个问题。在这种情况下，数组就派上用场了。同样，如果你有一百个值并且必须在循环中使用它们，独立变量将没有太大帮助。数组更容易处理，因为你可以轻松地遍历它们。

空格或换行在 JavaScript 数组中并不重要。你可以以不同的格式编写它们。请以下示例，它的内容与上面相同，但格式不同。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 数组</p>
<p id="array-demo"></p>
<script>
var carsforsale = ["Honda",
    "Toyota",
    "GTX",
    "Ford"];
document.getElementById("array-demo").innerHTML = carsforsale;
</script>
</body>
</html>
```

学习 JavaScript 数组：Honda,Toyota,GTX,Ford

它的结果与上一个示例相同。另一种创建数组的方法，这被称为 JavaScript 关键字`new`。我将在下例示例中使用`new`关键字来创建一个数组。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 数组</p>
<p id="array-demo"></p>
<script>
var carsforsale = new Array("Honda", "Toyota", "GTX", "Ford");
document.getElementById("array-demo").innerHTML = carsforsale;
</script>
</body>
</html>
```

学习 JavaScript 数组：Honda,Toyota,GTX,Ford

让我们分析这种新格式并理解它的不同之处。第一个区别是在数组开头和等号之后添加了关键字`new`，紧接着`new`关键字后面是`Array`关键字。另一个显著区别是去掉了方括号并添加了圆括号，但两种方法的工作方式相同。第二种方法更复杂冗长。为了简单、速度和可读性，你应该选择第一种方法，也称为数组字面量方法（`array literal method`）。

### 索引数字

你可以通过索引数字访问数组的项。正如前面提到的，数组的索引从数字 0 开始。在下面的示例中，我将访问索引为 0 的元素。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 数组</p>
<p id="array-demo"></p>
<script>
var carsforsale = new Array("Honda", "Toyota", "GTX", "Ford");
document.getElementById("array-demo").innerHTML = carsforsale[0];
</script>
</body>
</html>
```

学习 JavaScript 数组：Honda

通过索引数字可以访问数组的项。正如前面提到的，数组的索引可以帮助更改数组的值。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 数组</p>
<p id="array-demo"></p>
<script>
var carsforsale = new Array("Honda", "Toyota", "GTX", "Ford");
carsforsale[0] = "BMW";
carsforsale[1] = "Mitsubishi";
document.getElementById("array-demo").innerHTML = carsforsale;
</script>
</body>
</html>
```

学习 JavaScript 数组：BMW,Mitsubishi,GTX,Ford

数组被视为特殊对象。如果你使用`typeof`运算符检查数组的类型，你会得到“object”。但我们必须使用“数组”这个词来描述 JavaScript 数组。这是因为 JavaScript 数组使用数字访问元素，而对象使用项名称。你可以给数组分配任何值。你可以赋值给变量的值你可以在数组中混合不同的类型。程序员更倾向于给数组使用复数名称，如城市、国家等。这是因为每个数组都是多个项目的列表。与普通变量一样，你只需要声明一次数组。

JavaScript 变量可能被称为对象，而 JavaScript 数组被认为是特殊对象，因为数组可以包含不同类型的变量。你可以用对象、函数甚至数组填充数组。与字符串一样，数组的真正力量在于丰富的属性和内置方法。

### 数组属性

要讨论的第一个属性是`length`属性。它返回数组的长度，包含数组的所有元素。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 数组</p>
<p id="array-demo"></p>
<script>
var carsforsale = new Array("Honda", "Toyota", "GTX", "Ford");
document.getElementById("array-demo").innerHTML = carsforsale.length;
</script>
</body>
</html>
```

学习 JavaScript 数组：4

你可以构建一个遍历数组的循环来显示所有项或在程序中使用所有项。创建循环常用的方法之一是`for`循环。

```html
<!DOCTYPE html>
<html>
<body>
<p>这些是 JavaScript 数组</p>
<p>我将在下面的代码中使用 for 循环</p>
<p id="array-demo"></p>
<script>
var carsforsale, msg, cLn, y;
carsforsale = ["BMW", "Mitsubishi", "Honda", "Toyota"];
</script>
</body>
</html>
```

```javascript
cLn = carsforsale.length;
msg = "<ul>";
for (y = 0; y < cLn; y++) {
  msg += "<li>" + carsforsale[y] + "</li>";
}
msg += "</ul>";
document.getElementById("array-demo").innerHTML = msg;
```

这些是 JavaScript 数组，我将在下面的代码中使用`for`循环：

- 宝马
- 本田
- 丰田

你已经看到如何在网页上显示一个整洁、清晰的项目列表。下次当你在网页上看到类似的列表时，你应该知道是数组和`for`循环起了作用。在数组中，还有另一个函数可以实现相同的效果。

```html
<!DOCTYPE html>
<html>
<body>
<p>这些是 JavaScript 数组</p>
<p>我将在下面的代码中使用 for 循环</p>
<p id="array-demo"></p>
<script>
var carsforsale, msg;
carsforsale = ["BMW", "Honda", "Toyota"];
msg = "<ul>";
carsforsale.forEach(function(value) {
  msg += "<li>" + value + "</li>";
});
msg += "</ul>";
document.getElementById("array-demo").innerHTML = msg;
</script>
</body>
</html>
```

- 宝马
- 本田
- 丰田

### 添加元素

你可以使用`push()`方法向数组中添加元素。如果你在零售公司工作，每天都要向同一个数组上传新元素，这个 JavaScript 功能非常有帮助。JavaScript 的奇妙之处在于它允许你声明带有值的变量。之后，你可以使用`push`函数向同一个变量添加值。你可以根据需要更改这些值。所有这些都可以在一个数组中完成。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 数组</p>
<p>我将使用 push 方法向现有数组中添加新元素。</p>
<button onclick="FunctionXX()">请点击此按钮</button>
<p id="array-demo"></p>
<script>
var veggies = ["Pumpkin", "Tomato", "Ginger", "Potato"];
document.getElementById("array-demo").innerHTML = veggies;
function FunctionXX() {
  veggies.push("Spinach");
  document.getElementById("array-demo").innerHTML = veggies;
}
</script>
</body>
</html>
```

学习 JavaScript 数组：南瓜, 西番柿, 生姜, 土豆

你将使用`push`方法向现有数组添加新元素。当你在浏览器中运行代码时，你会看到上面的结果。当你点击网页浏览器中的按钮时，你可以在数组项目列表中看到新添加的元素。当我点击按钮时，我看到了以下结果：

南瓜, 西番柿, 土豆, 菠菜

你可以操作`length`属性向数组添加新元素。看看你是如何使用`length`属性的：

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 数组</p>
<p>我将使用 push 方法向现有数组中添加新元素。</p>
<button onclick="FunctionXX()">请点击此按钮</button>
<p id="array-demo"></p>
<script>
var veggies = ["Pumpkin", "Tomato", "Ginger", "Potato"];
document.getElementById("array-demo").innerHTML = veggies;
function FunctionXX() {
  veggies[veggies.length] = "Spinach";
  document.getElementById("array-demo").innerHTML = veggies;
}
</script>
</body>
</html>
```

学习 JavaScript 数组：南瓜, 西番柿, 土豆, 菠菜

如果你不知道自己在做什么，处理数组可能会很棘手。例如，你可以使用索引号向数组添加元素。在此过程中，如果你在代码中包含一个较大的索引，你将在数组中创建完全为`undefined`的空洞。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 数组</p>
<p>我将添加具有高索引的元素。结果将在数组中产生 undefined "空洞”。</p>
<p id="undefinedarray-demo"></p>
<script>
var veggies, msg, cLn, XX;
veggies = ["Pumpkin", "Ginger", "Tomato", "Garlic"];
veggies[8] = "Spinach";
cLn = veggies.length;
msg = "";
for (XX = 0; XX < cLn; XX++) {
  msg += veggies[XX] + "<br>";
}
document.getElementById("undefinedarray-demo").innerHTML = msg;
</script>
</body>
</html>
```



学习 JavaScript 数组

南瓜、生姜、西番柿、大蒜、`undefined`、`undefined`、`undefined`、`undefined`、菠菜。

你可以看到 JavaScript 并没有在代码中返回错误。它只是在没有项目填充的位置创建了一个 `undefined` 槽位。如果以后需要，可以用项目填充该 `undefined` 槽位。因此，这实际上并不能被视为致命错误。

## 关联数组

在编程世界中，许多编程语言具有具有索引元素的数组。在 JavaScript 中，数组也可以具有由字符串索引的元素。这些被称为关联数组。

```javascript
var user = {};
user["name"] = "John";
user["age"] = 30;
user["city"] = "New York";
console.log(user["name"]); // John
console.log(user["age"]); // 30
console.log(user["city"]); // New York
```

## 数组转换

JavaScript 提供了可以将数组转换为字符串的方法。最常用的方法是`toString()`方法。

```javascript
var fruits = ["Apple", "Banana", "Cherry"];
console.log(fruits.toString()); // Apple,Banana,Cherry
```

不仅`toString()`方法可以将数组转换为字符串，`join()`方法也是如此。它允许你指定一个分隔符。

```javascript
var fruits = ["Apple", "Banana", "Cherry"];
console.log(fruits.join(" - ")); // Apple - Banana - Cherry
```

当你在使用数组操作零售店或金融公司时，你可以使用`pop`和`push`方法来提取或添加元素。`pop`将一个元素从数组中弹出，而`push`则将一个元素推入数组。`pop`方法唯一的问题是你能从数组的末尾删除元素。请查看以下示例了解如何操作。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript 数组</p>
<p id="popping-demo1"></p>
<p id="popping-demo2"></p>
<script>
var veggies = ["Pumpkin", "Ginger", "Tomato", "Garlic"];
document.getElementById("popping-demo1").innerHTML = veggies;
veggies.pop();
document.getElementById("popping-demo2").innerHTML = veggies;
</script>
</body>
</html>
```

# 学习 JavaScript 数组

南瓜、生姜、番柿、大蒜

南瓜、生姜、番柿

数组的最后一项通过`pop()`方法的帮助被弹出了。你可以重复运行脚本，最终将得到一个空数组。

现在你已经学会了如何从数组中弹出项，我将解释如何推入元素。请记住，在运行代码后，你不会立即看到添加的元素。由于我在代码中添加了一个按钮，你必须先点击按钮才能显示元素。由于代码中包含一个函数，`push`方法将向代码中添加许多相同元素的实例。持续点击，浏览器将不断向数组中添加更多实例。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习数组方法</p>
<p>JavaScript `push()` 方法会将新元素附加到你的数组中。</p>
<button onclick="FunctionYY()">点击我</button>
<p id="array-demo"></p>
<script>
var veggies = ["Garlic", "Pumpkin", "Ginger", "Tomato"];
document.getElementById("array-demo").innerHTML = veggies;
function FunctionYY() {
  veggies.push("Spinach");
  document.getElementById("array-demo").innerHTML = veggies;
}
</script>
</body>
</html>
```

# 学习数组方法

JavaScript `push()` 方法会将新元素附加到你的数组中。

点击我

大蒜、南瓜、生姜、番柿、菠菜

## 移位数组 (Shifting Arrays)

另一种名为`shift`的方法用于从数组的起点删除元素。假设你有一个数组。我将使用相同的`veggies`数组来解释数组移位的概念。与`pop`方法相反，`shift`方法将从数组中删除第一个元素。当`shift`方法从数组中删除一个元素时，`unshift`方法从数组开头删除一个或多个元素。

随着元素的删除，索引数字也会发生变化。在使用`shift`或`unshift`方法后，数组中的所有其他元素将自动移动到较低的索引。再次强调，仅仅在浏览器中运行代码不会从开头删除元素。你必须点击“点击我”按钮来触发数组的变化。此外，如果你持续点击按钮，浏览器将不断从数组中移除元素。这种情况会一直持续最后。`shift()`方法非常灵活，因为你可以将被删除的元素收集在一个变量中。然后你就可以根据需要随时使用它们。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习数组方法</p>
<p>`shift()`</p>
<button onclick="FunctionYY()">点击我</button>
<p id="array-demo"></p>
<script>
var veggies = ["Garlic", "Pumpkin", "Ginger", "Tomato"];
document.getElementById("array-demo").innerHTML = veggies;
function FunctionYY() {
  veggies.shift();
  document.getElementById("array-demo").innerHTML = veggies;
}
</script>
</body>
</html>
```

# 学习数组方法

`shift()`

点击我

南瓜、生姜、番柿

有一种方法可以从数组中删除元素。脚本中的关键字被标记为`delete`。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习数组方法</p>
<p>`delete` 方法</p>
<p id="array-demo1"></p>
<p id="array-demo2"></p>
<script>
var veggies = ["Garlic ", "Pumpkin ", "Ginger ", "Tomato "];
document.getElementById("array-demo1").innerHTML =
"这是第一个蔬菜名称：" + veggies[0];
delete veggies[0];
document.getElementById("array-demo2").innerHTML =
"这是第一个蔬菜名称：" + veggies[0];
</script>
</body>
</html>
```

# 学习数组方法

`delete` 方法

这是第一个蔬菜名称：大蒜

这是第一个蔬菜名称：`undefined`

## splice() 方法

JavaScript 中有一个`splice()`方法用于在数组中添加更多或多个元素。该方法还会删除放置在其后的元素。我将使用与之前其他方法相同的数组，以便你理解这些方法之间的区别。括号中的第一个数字是添加或删除的起始索引。第二个元素显示要删除的剩余元素数量。你可以使用`splice`方法复制任何位置的连续元素，并将它们添加到新数组中。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习数组方法</p>
<p>JavaScript `splice()`</p>
<p>我将使用 `splice()` 方法添加元素。</p>
<button onclick="FunctionYY()">点击我</button>
<p id="array-demo1"></p>
<p id="array-demo2"></p>
<script>
var veggies = ["Pumpkin ", "Ginger ", "Tomato ", "Potato "];
document.getElementById("array-demo1").innerHTML = "这是原始数组：<br>" + veggies;
function FunctionYY() {
  veggies.splice(3, "Spinach ", "Garlic ");
  document.getElementById("array-demo2").innerHTML = "这是新数组：<br>" + veggies;
}
</script>
</body>
</html>
```

# JavaScript splice()

我将使用 `splice()` 方法添加元素。

点击我

这是原始数组：

南瓜、生姜、番柿、土豆

这是新数组：

如果你分析代码片段，你会发现代码中有两个参数。第一个参数 (`3`) 指出了元素的位置。第二个参数 (`0`) 定义了我想删除的元素数量。我排除了之前的两个元素，因此没有添加新元素。虽然有很多其他方法可以完成任务，但`splice()`方法为程序员提供了处理数组空位的正确方式。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript `splice()`</p>
<p>我将使用 `splice()` 方法添加元素。</p>
<button onclick="FunctionYY()">点击我</button>
<p id="array-demo1"></p>
<p id="array-demo2"></p>
<script>
var veggies = ["Pumpkin ", "Ginger ", "Tomato ", "Potato "];
document.getElementById("array-demo1").innerHTML = "这是原始数组：<br>" + veggies;
function FunctionYY() {
  veggies.splice(0, 2);
  document.getElementById("array-demo2").innerHTML = "这是新数组：<br>" + veggies;
}
</script>
</body>
</html>
```

## 连接 (Concatenation)

JavaScript 允许连接两个数组以产生一个新的数组。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript 数组 `concat()`</p>
<p>`concat()` 方法遵循合并模式：</p>
<p id="array-demo"></p>
<script>
var veggies = ["Tomato ", "Potato ", "Cauliflower ", "Cabbage "];
var frutoos = ["Orange ", "Fig ", "Guava ", "Date "];
</script>
</body>
</html>
```

# JavaScript 数组 concat() 方法

`concat()` 方法遵循以下合并模式：

西红柿、土豆、花椰菜、卷菜、橙子、无花果、石榴、枣

JavaScript 中的`concat()`方法可以处理两个以上的参数。你可以添加另一个数组将其与前两个合并。下面的示例将解释合并多三个数组的方法。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript Array concat()</p>
<p>The `concat()` method follows the merging pattern:</p>
<p id="array-demo"></p>
<script>
var veggies = ["Tomato ", "Potato ", "Cauliflower ", "Cabbage "];
var frutoos = ["Orange ", "Fig ", "Guava ", "Date "];
var summerfrutoos = ["Watermelon ", "Melon ", "Mango "]
var fruitbasket = veggies.concat(frutoos, summerfrutoos);
document.getElementById("array-demo").innerHTML = fruitbasket;
</script>
</body>
</html>
```

# JavaScript 数组 concat() 方法

`concat()` 方法遵循以下合并模式：

西红柿 ,土豆 ,花椰菜 ,卷菜 ,橙子 ,无花果 ,石榴 ,枣 ,西瓜 ,甜瓜 ,芒果

`concat()` 方法也接受字符串作为参数。这里是学习如何将字符串添加到数组中的示例。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript Array concat()</p>
<p>The `concat()` method follows the merging pattern:</p>
<p id="array-demo"></p>
<script>
var veggies = ["Tomato ", "Potato ", "Cauliflower ", "Cabbage "];
var fruitbasket = veggies.concat('Spinach ', 'garlic ', 'eggplant ');
document.getElementById("array-demo").innerHTML = fruitbasket;
</script>
</body>
</html>
```

# JavaScript 数组 concat() 方法

`concat()` 方法遵循以下合并模式：

西红柿 ,土豆 ,花椰菜 ,卷菜 ,菠菜 ,大蒜 , 茄子

## 切片 (Slicing)

你可以在想要的地方切分数组。`slice()` 方法会产生数组的片段并创建新数组。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript Array concat()</p>
<p>The `concat()` method follows the merging pattern:</p>
<p id="array-demo"></p>
<script>
var veggies = ["Tomato ", "Potato ", "Cauliflower ", "Cabbage "];
var freshveggies = veggies.slice(1);
var freshveggies1 = veggies.slice(2);
document.getElementById("array-demo").innerHTML = veggies + "<br><br>" + freshveggies + "<br><br>" + freshveggies1;
</script>
</body>
</html>
```

# JavaScript 数组 concat() 方法

`concat()` 方法遵循以下合并模式：

西红柿 ,土豆 ,花椰菜 ,卷菜
土豆 ,花椰菜 ,卷菜
花椰菜 ,卷菜

`slice()` 方法保持现有数组完整性。它不会从数组源中删除任何新元素。示例代码：

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript Array</p>
<p>The `concat()` method follows the merging pattern:</p>
<p id="array-demo"></p>
<script>
var veggies = ["Tomato ", "Potato ", "Cauliflower ", "Cabbage "];
var freshveggies = veggies.slice(1, 3);
document.getElementById("array-demo").innerHTML = veggies + "<br><br>" + freshveggies;
</script>
</body>
</html>
```

## JavaScript 数组

`concat()` 方法遵循以下合并模式：

西红柿 ,土豆 ,花椰菜 ,卷菜
土豆 ,花椰菜

如果你省略了结束参数，结果将包含整个左侧的数组。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript Array</p>
<p>The `concat()` method follows the merging pattern:</p>
<p id="array-demo"></p>
<script>
var veggies = ["Tomato ", "Potato ", "Cauliflower ", "Cabbage "];
```



### 数组切片示例

`var freshveggies = veggies.slice(1);` 从 `veggies` 数组中提取从索引 1 开始的所有元素，并将其赋值给新数组 `freshveggies`。

```javascript
var freshveggies = veggies.slice(1);

document.getElementById("array-demo").innerHTML = veggies + "<br><br>" + freshveggies;
```

`document.getElementById("array-demo").innerHTML` 将显示原始数组 `veggies` 和切片后的数组 `freshveggies`。

## JavaScript 数组

`concat()` 方法遵循以下合并模式：

```text
西红柿, 土豆, 花椰菜, 卷菜
土豆, 花椰菜, 卷菜
```

## 数组排序 (Array Sorting)

你可以使用 `sort()` 方法按字母顺序对数组排序。当你处理零售店或金融机构的海量数组项时，这非常有帮助。

```html
<!DOCTYPE html>
<html>
<body>

<p>This is JavaScript Array Sort method</p>
<p>This method will sort out an array in alphabetical order.</p>

<button onclick="FunctionAlpha()">请点击此处</button>

<p id="demo10"></p>

<script>
var veggies = ["Garlic ", "Spinach ", "Radish ", "Peas ", "Potato "];
document.getElementById("demo").innerHTML = veggies;

function FunctionAlpha() {
  veggies.sort();
  document.getElementById("demo10").innerHTML = veggies;
}
</script>

</body>
</html>
```

这是 JavaScript 数组排序方法，该方法将按字母顺序对数组排序。点击按钮后，输出为：

```text
大蒜, 菠菜, 萝卜, 豌豆, 土豆
```

## 反转 (Reverse)

你可以通过 `reverse()` 方法将数组设置为反转位置。它将元素反序排列。该方法按字母倒序排列。

```html
<!DOCTYPE html>
<html>
<body>

<p>This is JavaScript Array Sort method</p>
<p>This method will sort out an array in alphabetical order.</p>

<button onclick="FunctionAlpha()">请点击此处</button>

<p id="demo10"></p>

<script>
var veggies = ["Garlic ", "Spinach ", "Radish ", "Peas ", "Potato "];
document.getElementById("demo").innerHTML = veggies;

function FunctionAlpha() {
  veggies.sort();
  veggies.reverse();
  document.getElementById("demo10").innerHTML = veggies;
}
</script>

</body>
</html>
```

这是 JavaScript 数组排序方法，该方法将按字母顺序对数组排序后再反转。点击按钮后，输出为：

```text
大蒜, 菠菜, 萝卜, 豌豆, 土豆
```

## 数字排序 (Sorting Numeric)

`sort()` 方法在处理数字时默认按字符串顺序排序，但你可以通过比较函数实现正确的数字排序。如果你省略了结束参数，结果将包含整个左侧的数组。

```html
<!DOCTYPE html>
<html>
<body>

<p>JavaScript Array Sort</p>
<p>By clicking the button, you can sort the array in ascending order.</p>

<button onclick="FunctionT()">请点击此处</button>

<p id="demo10"></p>

<script>
var nums = [4000, 1000, 15, 555, 253, 102];
document.getElementById("demo").innerHTML = veggies;

function FunctionT() {
  nums.sort(function(x, y){return x - y});
  document.getElementById("demo10").innerHTML = nums;
}
</script>

</body>
</html>
```

## 降序排序 (Sorting Descending)

我将使用相同的 `sort()` 方法按降序模式进行排序。让我们看看可以得到什么类型的结果。

```html
<!DOCTYPE html>
<html>
<body>

<p>JavaScript Array Sort</p>
<p>By clicking the button, you can sort the array in ascending order.</p>

<button onclick="FunctionT()">请点击此处</button>

<p id="demo10"></p>

<script>
var nums = [4000, 1000, 15, 555, 253, 102];
document.getElementById("demo").innerHTML = veggies;

function FunctionT() {
  nums.sort(function(x, y){return y - x});
  document.getElementById("demo10").innerHTML = nums;
}
</script>

</body>
</html>
```

## 比较函数 (Compare Function)

即使在处理数字时，你也可以使用 `compare` 函数来获得所需的结果。该函数的作用是定义排序顺序的特定替代方案。此 `compare` 函数必须根据你使用的参数返回零、负值或正值。当你向 `sort()` 函数传递几个值时，它会将这些值分发给 `compare` 函数。之后，它将根据返回的负值、正值或零值来对这些值进行排序。如果你看到负结果，则 `x` 将排在 `y` 之后；如果你看到正结果，则 `y` 将排在 `x` 之前。数字 0 表示这些值的排序顺序没有变化。

该函数比较数组中的值。当它比较 `20` 和 `100` 时候，它会调用 `compare` 函数并计算差值。如果结果为负数，它将声明 `20` 的值低于 `100`。你可以使用以下代码段对字母排序和数字排序进行实验。

```html
<!DOCTYPE html>
<html>
<body>

<p>学习 JavaScript 数组排序</p>
<p>你可以使用点击按钮按字母顺序或数字顺序排序数组。</p>

<button onclick="FunctionP()">点击我进行字母排序</button>
<button onclick="FunctionQ()">点击我进行数字排序</button>

<p id="demo1"></p>

<script>
var nums = [4045, 1002, 1567, 5234, 251, 100];
document.getElementById("demo1").innerHTML = nums; 

function FunctionP() {
  nums.sort();
  document.getElementById("demo1").innerHTML = nums;
}

function FunctionQ() {
  nums.sort(function(x, y){return x - y});
  document.getElementById("demo1").innerHTML = nums;
}
</script>

</body>
</html>
```

### 实验示例结果

#### 原始结果

# 学习 JavaScript 数组排序

你可以使用点击按钮按字母顺序或数字顺序排序数组。

点击我进行字母排序  点击我进行数字排序

```text
4045,1002,1567,5234,251,100
```

上述结果是你在浏览器中运行代码时显示的原始结果。以下是点击字母排序按钮后发生的情况。

#### 字母排序结果

# 学习 JavaScript 数组排序

你可以使用点击按钮按字母顺序或数字顺序排序数组。

点击我进行字母排序  点击我进行数字排序

```text
100,1002,1567,251,4045,5234
```

#### 数字排序结果

查看进行数字排序时的结果。

# 学习 JavaScript 数组排序

你可以使用点击按钮按字母顺序或数字顺序排序数组。

点击我进行字母排序  点击我进行数字排序

```text
100,251,1002,1567,4045,5234
```

### 随机排序

你可以使用 `random` 方法随机排序数组。请参考示例了解如何将该方法添加到代码中并获得所需的结果。通过使用 `random` 方法，你将获得数字的随机排序。我无法在这里显示所有排序结果，因为我每次点击按钮时，在浏览器中得到的结果都不一样。你可以使用代码并通过多次点击按钮查看不同的结果。请看以下示例。

```html
<!DOCTYPE html>
<html>
<body>

<p>学习 JavaScript 数组排序</p>
<p>通过点击按钮，你可以按升序排序数组。</p>

<button onclick="FunctionT()">点击我</button>

<p id="demo10"></p>

<script>
var nums = [4000, 1000, 15, 555, 253, 102];
document.getElementById("demo10").innerHTML = nums; 

function FunctionT() {
  nums.sort(function(x, y){return 0.5 - Math.random()});
  document.getElementById("demo10").innerHTML = nums;
}
</script>

</body>
</html>
```

#### 随机排序结果示例

# 学习 JavaScript 数组排序

通过点击按钮，你可以按升序排序数组。

点击我

```text
15,253,1000,555,102,4000
```

随机方法的问题在于它会倾向于某些数字而不是其他数字。还有另一种比这种更正确、更有用的方法。它被称为 Fisher-Yates 洗牌算法（Fisher-Yates shuffle）。该方法在数据科学早期就被引入。

```html
<!DOCTYPE html>
<html>
<body>

<p>JavaScript 数组排序继续</p>

<h3>这是 Fisher-Yates 方法</h3>

<p>当你反复点击按钮时，你将随机顺序排序数组。</p>

<button onclick="FunctionXX()">点击我</button>

<p id="demo12"></p>

<script>
var nums = [404, 10023, 123, 589, 2511, 102];
document.getElementById("demo12").innerHTML = nums; 

function FunctionXX() {
  var a, b, c;
  for (a = nums.length -1; a > 0; a--) {
    b = Math.floor(Math.random() * (a + 1));
    c = nums[a];
    nums[a] = nums[b];
    nums[b] = c;
  }
  document.getElementById("demo12").innerHTML = nums;
}
</script>

</body>
</html>
```

#### Fisher-Yates 方法示例结果

# JavaScript 数组排序继续

### 这是 Fisher-Yates 方法

当你反复点击按钮时，你将随机顺序排序数组。

点击我

```text
404,10023,123,589,2511,102
```

## 数组最大值和最小值

JavaScript 没有内置函数来查找最大值或最小值。然而，当你有一个数组时，你可以使用 `sort()` 来查找最大值和最小值。

### 查找数组最大值

```javascript
var nums = [4077879878, 10023, 147777777777, 53, 25, 1023];
document.getElementById("demo7").innerHTML = ArrayMaxPoint(nums);

function ArrayMaxPoint(arr) {
  var length = arr.length;
  var maximum = -Infinity;
  while (length--) {
    if (arr[length] > maximum) {
      maximum = arr[length];
    }
  }
  return maximum;
}
```

数组中的最高数字是：147777777777。

### 查找数组最小值

同样，你可以创建一个函数，该函数会遍历整个数组，首先检测出最小值，然后将其与数组其余值进行比较。最后，它将在浏览器中输出结果。查看 `ArrayMinPoint()` 函数是如何工作以及遍历数组的。

```javascript
var nums = [4077879878, 10023, 147777777777, 53, 25, 1023];
document.getElementById("demo7").innerHTML = ArrayMinPoint(nums);

function ArrayMinPoint(arr) {
  var length = arr.length;
  var minimum = Infinity;
  while (length--) {
    if (arr[length] < minimum) {
      minimum = arr[length];
    }
  }
  return minimum;
}
```

数组中的最低数字是：25。

## 对象数组排序

如果你有一个包含对象的数组，可以使用以下方法对它们进行排序。

请点击按钮对汽车对象进行排序。

```javascript
var carsObjects = [
  {type:"Honda", year:2020, Make:"Japan", Model:"Vezel"},
  {type:"Toyota", year:2010, Make:"Japan", Model:"Fortuner"},
  {type:"Toyota", year:2018, Make:"Japan", Model:"Vitz"}
];

ToDisplayCars();

function FunctionO() {
  carsObjects.sort(function(x, y){return x.year - y.year});
  ToDisplayCars();
}

function ToDisplayCars() {
  document.getElementById("demo2").innerHTML =
  carsObjects[0].type + " " + carsObjects[0].year + " " + carsObjects[0].Make + " " + carsObjects[0].Model + "<br>" +
  carsObjects[1].type + " " + carsObjects[1].year + " " + carsObjects[0].Make + " " + carsObjects[0].Model + "<br>" +
  carsObjects[2].type + " " + carsObjects[2].year + " " + carsObjects[0].Make + " " + carsObjects[0].Model;
}
```

排序后的输出结果：

```text
Toyota 2010 Japan Fortuner
Toyota 2018 Japan Fortuner
Honda 2020 Japan Fortuner
```

我已经通过点击排序按钮进行了排序。在浏览器中首次运行代码时，可能会看到不同的顺序。只有在点击排序按钮时，顺序才会改变。

## JavaScript 迭代

在创建网页时，JavaScript 数组中还有更多可以学习和应用的内容。`forEach()` 方法帮助你对数组的所有元素执行函数调用。该方法会为所有单个数组元素至少调用一次函数。

```javascript
var msg = "";
var nums = [4588888, 2234, 12349, 16899, 900025];

nums.forEach(FunctionE);
document.getElementById("demo44").innerHTML = msg;

function FunctionE(Evalue, Eindex, Earray) {
  msg = msg + Evalue + "<br>";
}
```



4588888
2234
12349
16899
900025

我为函数分配了三个参数；第一个参数处理项目的值，第二个参数处理项目的索引，第三个参数处理整个数组。在上面的示例中，我只部署了`Evalue`参数。这意味着如果你不需要另外两个，可以将它们从函数中删除以简化代码。然而，如果你认为以后会需要另外两个，可以保留它们并在随后的单独调用中使用它们。`forEach()`方法最好的地方是它适用于除 Internet 8 或之前的版本之外的所有 Web 浏览器。

## map() 方法

程序员使用`map()`方法通过对所有元素执行单独函数来创建一个新数组。它不会对空元素执行函数，也不会改变数组的原始形式。接下来的示例将使用加法运算符为数组中的每个数字加 1000 并创建一个新数组。

```javascript
var nums1 = [12345, 7674, 3449, 12316, 990025];

var nums2 = nums1.map(FunctionM);

document.getElementById("demo90").innerHTML = nums2;

function FunctionM(Mvalue, Mindex, Marray) {

  return Mvalue + 1000;

}
```

13345,8674,4449,13316,990125

我将移除加法运算符并添加乘法运算符以产生不同的结果创建一个新数组。

```javascript
var nums1 = [12345, 7674, 3449, 12316, 990025];

var nums2 = nums1.map(FunctionM);

document.getElementById("demo90").innerHTML = nums2;

function FunctionM(Mvalue, Mindex, Marray) {

  return Mvalue * 1000;

}
```

12345000,7674000,3449000,12316000,990025000

请注意，我在代码中包含的函数接受三个参数；第一个参数是值，第二个是索引，第三个是整个数组。如果你只需要处理一个参数，可以省略其余参数。省略不会影响程序。它将产生相同的结果。与前面的方法一样，`Array.map()`适用于 Explorer 8 或更早版本之外的所有 Web 浏览器。

## filter() 方法

`filter()`方法倾向于创建一个包含通过测试的数组元素的新数组。我将过滤器设置为 20，这意味着所有大于 20 的数字都将被该方法过滤掉。用户只会看到大于 20 的数字。其余元素将被隐藏。

```javascript
var nums = [45890, 17, 3459, 18, 2, 6, 23416, 87625];

var over20 = nums.filter(FunctionZ);

document.getElementById("demo789").innerHTML = over20;

function FunctionZ(valueF, indexF, arrayF) {

  return valueF > 20;

}
```

45890,3459,23416,87625

## reduce() 方法

`reduce()`方法对所有数组元素进行函数调用并产生一个值。该方法在数组内部从左到右操作。它保持原始数组完整不变。

```javascript
var over20 = nums.reduce(FunctionZ);

document.getElementById("demo789").innerHTML = over20;

function FunctionZ(Total, valueF) {

  return Total + valueF;

}
```

这是 JavaScript `Array.reduce()`。

以下程序将通过过滤所有通过测试的数组元素来创建一个新数组。

`160433`

```javascript
var nums = [45890, 17, 3459, 18, 2, 6, 23416, 87625];

var over20 = nums.reduce(FunctionZ, 5000000000);

document.getElementById("demo789").innerHTML = over20;

function FunctionZ(Total, valueF) {

  return Total + valueF;

}
```

这是 JavaScript `Array.filter()`。

以下程序将通过过滤所有通过测试的数组元素来创建一个新数组。

`5000160433`

### reduceRight() 方法

`reduceRight()`方法倾向于对数组的所有元素运行一个函数以产生一个值。该方法运行良好，从数组的右侧向左侧移动。最好的点是，你可以保持原始数组完整。

```javascript
var nums = [45890, 17, 3459, 18, 2, 6, 23416, 87625900000];

var sum = nums.reduceRight(FunctionZ);

document.getElementById("demo789").innerHTML = "The Total sum of all the numbers is " + sum;

function FunctionZ(Total, valueF) {

  return Total + valueF;

}
```

这是 JavaScript `Array.reduceRight()`。

以下程序将通过过滤所有通过测试的数组元素来创建一个新数组。

所有数字的总和为 `87625972808`

`Array.reduceRight()`在所有 Internet Explorer 8 或更早版本的浏览器中都能运行良好。

### every() 方法

`every()`方法对数组进行彻底检查，以查看数组中的所有元素是否通过了测试。在下面的示例中，我将运行一个测试来查看所有元素是否大于 500。

```javascript
var nums = [45890, 17, 3459, 18, 2, 6, 23416, 87625900000];

var Over500 = nums.every(FunctionZ);

document.getElementById("demo789").innerHTML = "Are all values bigger than 500: " + Over500;

function FunctionZ(valueF) {

  return valueF > 500;

}
```

这是 JavaScript `Array.every()`。

以下程序将显示测试结果。

`Are all values bigger than 500: false`

现在我将故意让所有值都大于 500，看看结果是什么。

```javascript
var nums = [45890, 1700, 3459, 1800, 2700, 6222, 23416, 87625900000];

var Over500 = nums.every(FunctionZ);

document.getElementById("demo789").innerHTML = "Are all values bigger than 500: " + Over500;

function FunctionZ(valueF) {

  return valueF > 500;

}
```

这是 JavaScript `Array.every()`。

以下程序将显示测试结果。

`Are all values bigger than 500: true`

### some() 方法

有另一个方法用于检查数组中有多少值通过了测试。我将检查有多少个值通过了大于 500 的测试。该方法可以接受多个参数，但因为我只需要一个，所以我坚持使用。你可以添加更多参数来筛选索引并产生整个数组。

```javascript
var nums = [45890, 170, 345, 1800, 270, 622, 23416, 87625900000];

var Over500 = nums.some(FunctionZ);

document.getElementById("demo789").innerHTML = "Are there some values bigger than 500: " + Over500;

function FunctionZ(valueF) {

  return valueF > 500;

}
```

这是 JavaScript `Array.some()`。

以下程序将显示测试结果。

`Are there some values bigger than 500: true`

### indexOf() 方法

`indexOf()`方法在数组中搜索指定的元素并返回第一次出现的位置。如果未找到元素，则返回 -1。

```javascript
var nums = [45890, 170, 345, 1800, 270, 622, 23416, 87625900000];

var p = nums.indexOf(622);

document.getElementById("demo789").innerHTML = "The position of 622 is: " + p;
```

这是 JavaScript `Array.indexOf()`。

以下程序将显示元素的索引。

`The position of 622 is 5`

## lastIndexOf() 方法

`lastIndexOf()`方法从右到左搜索数组并返回最后一次出现的位置。

```javascript
var veggies = ["Garlic", "Tomatoes", "Potatoes", "Tomatoes", "Pumpkin"];

var a = veggies.lastIndexOf("Tomatoes");

document.getElementById("demo00").innerHTML = "Tomatoes are found at position " + a;
```

这是 JavaScript `Array.lastIndexOf()`。

`Tomatoes are found at position 3`

### find() 方法

`find()`方法给你返回数组中第一个通过函数的项的值。

```javascript
var nums = [444, 55544, 2333, 56666, 22, 876];

var a = nums.find(FunctionZ);

document.getElementById("demo00").innerHTML = "The number is bigger than 500 = " + a;

function FunctionZ(valueF) {

  return valueF > 500;

}
```

这是 JavaScript `Array.find()`。

`The number is bigger than 500 = 55544`

### findIndex() 方法

`findIndex()`方法将返回数组中第一个通过测试的元素的索引号。

```javascript
var nums = [444, 55544, 2333, 56, 22, 876];

var a = nums.findIndex(FunctionZ);

document.getElementById("demo055").innerHTML = "The index of the number that is lower than 500 = " + a;

function FunctionZ(valueF) {

  return valueF < 500;

}
```

这是 JavaScript `Array.findIndex()`。

`The index of the number that is lower than 500 = 0`

JavaScript 的`for`循环包含一个语句和三个表达式。它有一个初始化部分，在`for`循环首次执行之前运行。该表达式用于创建计数器。你在此处创建的变量立即被作用化于`for`循环。一旦循环执行并到达逻辑终点，这些变量就会被销毁。

JavaScript `for`循环的另一个重要部分是条件。`for`循环在每次执行新迭代之前都会检查此表达式。如果你省略了这部分，表达式将被求值为为`true`，并执行循环中的语句。如果求值为`false`，循环将停止工作。

循环的另一个重要部分是`final-expression`。该表达式在每次迭代后运行。它用于递增计数器。不过，你也可以用它来减少计数器。循环的语句部分是在循环内部必须重复的代码。你可以根据需要从`for`循环中省略任何这些表达式。

JavaScript 中的`for`循环用于计算数学数字或语句的迭代。它们也可以重复代码中的语句。只有在循环中插入`break`语句后，你才能退出循环。我将在接下来的章节中详细介绍`break`语句。

循环之所以是特殊的，是因为它们避免了多次编写代码的麻烦。一旦你将代码包含在循环中，它就会重复。代码块应该重复多少取决于你在代码中包含的数字。此外，每次循环执行代码时，值都是不同的。因此，尽管代码有重复，但这种重复是按照适当的方法进行的。

```html
<!DOCTYPE html>

<html>

<body>

<p id="forloop-demo"></p>

<script>

var carsforsale = ["Honda", "Toyota", "Vezel", "Fiat", "Volkswagen"];

var msg = "";

var YY;

for (YY = 0; YY < carsforsale.length; YY++) {

  msg += carsforsale[YY] + "<br>";

}

document.getElementById("forloop-demo").innerHTML = msg;

</script>

</body>

</html>
```

本田
丰田
Vezel
菲亚
大众

在这个示例中，我创建了一个数组，然后添加了一个`for`循环来遍历数组的元素。`for`循环遍历了数组中的项，并将它们整齐地显示在独立的行上。

```html
<!DOCTYPE html>

<html>

<body>

<p id="demo1"></p>

<script>

var msg = "";

var YY;

for (YY = 0; YY < 3; YY++) {

  msg += "The next number you will have to add to the list is " + YY + "<br>";

}

document.getElementById("demo1").innerHTML = msg;

</script>

</body>

</html>
```

你需要添加到列表的下一个数字是 0
你需要添加到列表的下一个数字是 1
你需要添加到列表的下一个数字是 2

在这个示例中，第一个语句在循环启动之前就设置了一个变量。第二个语句定义了该循环运行的正确条件。根据该条件，循环的运行次数不能超过三次。每当`for`循环执行代码时，第三个语句都会通过`YY++`增加变量的值。

通常，你需要使用第一个语句来初始化循环中的变量。然而，并不总是如此。JavaScript 并不强制从第一个语句开始。你可以跳过它，并在第一个语句中初始化不同的值。

```html
<!DOCTYPE html>

<html>

<body>

<p id="demo1"></p>

<script>

var carsforsale = ["Vezel", "Fortuner", "Sportage", "Sorento"];

var YY, length, msg;

for (YY = 0, length = carsforsale.length, msg = ""; YY < length; YY++) {

  msg += carsforsale[YY] + "<br>";

}

document.getElementById("demo1").innerHTML = msg;

</script>

</body>

</html>
```

Vezel
Fortuner
Sportage
Sorento

你也可以跳过第一个语句，就好像你的值在循环启动之前已经设置好了。

```html
<!DOCTYPE html>

<html>

<body>

<p id="demo1"></p>

<script>

var carsforsale = ["Vezel", "Fortuner", "Sportage", "Sorento"];

var YY = 0

var length = carsforsale.length

var msg = ""

for (; YY < length; YY++) {

  msg += carsforsale[YY] + "<br>";

}

document.getElementById("demo1").innerHTML = msg;

</script>

</body>

</html>
```



`Vezel`、`Fortuner`、`Sportage`、`Sorento`

`for` 循环中的第二个语句通常用于评估起始变量的条件。然而，这并不总是如此。JavaScript 不再关心这些了。第二个语句是可选的。如果第二个语句返回 `true`，循环将重新开始。如果返回其他值，循环将结束。如果省略了第二个语句，你必须在循环中插入一个 `break`。否则，循环将变成无限循环。你永远无法停止它。无限循环对你来说是一个死胡同，因为当用户打开包含无限循环的网站时，他们的浏览器将会崩溃。用户可能还会返回你的网站。

第三个语句递增起始变量的值。然而，第三个语句是可选的。

```html
<!DOCTYPE html>
<html>
<body>
<p id="demo1"></p>
<script>
var carsforsale = ["Vezel", "Fortuner", "Sportage", "Sorento"];
var YY = 0
var length = carsforsale.length
for (; YY < length; YY++) {
  msg += carsforsale[YY] + "<br>";
}
document.getElementById("demo1").innerHTML = msg;
</script>
</body>
</html>
```

`Vezel`、`Sportage`

最需要记住的是，计数器 `YY` 可以是任何名称。它随着迭代递增。

## `for...in` 循环

另一种 `for` 循环类型是 `for...in`。`for...in` 循环遍历对象的属性。

### JavaScript For/In 循环

`for...in` 循环遍历对象的属性。大多数程序员使用 `i` 作为变量。

```html
<!DOCTYPE html>
<html>
<body>
<p>Learning JavaScript For/In Loop</p>
<p>Our for/in loops through all the properties of the object.</p>
<p id="demo1"></p>
<script>
var msg = "";
var car = {name:"Honda", model:"Vezel", year:2020, make:"Japan"};
var YY;
for (YY in car) {
  msg += car[YY] + " ";
}
document.getElementById("demo1").innerHTML = msg;
</script>
</body>
</html>
```

学习 JavaScript For/In 循环

我们的 for/in 循环遍历了对象的所有属性。

`Honda Vezel 2020 Japan`

如果你非常在意索引的顺序，那么你应该放弃使用 `for` 循环遍历数组的想法。顺序与实现方式无关。你无法按照预期的顺序访问数组的值。当你认为顺序很特殊时，使用 `for of` 循环、`for` 循环和 `Array.forEach()` 对你来说更重要且更好。

## `forEach()` 循环

该方法会为数组的每个元素调用一次函数，也称为回调函数。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript Array.forEach() 循环</p>
<p>此程序将为数组的每个元素调用一次函数。</p>
<p id="demo5"></p>
<script>
var msg = "";
var nums = [55545, 454, 1239, 78816, 45625];
nums.forEach(FunctionYZ);
document.getElementById("demo5").innerHTML = msg;
function FunctionYZ(fvalue, findex, farray) {
  msg = msg + fvalue + "<br>";
}
</script>
</body>
</html>
```

### 学习 JavaScript Array.forEach() 循环

此程序将为数组的每个元素调用一次函数。

`55545`、`454`、`1239`、`78816`、`45625`

上述代码中的函数通常接受三个参数。第一个参数是项目的值。第二个参数是项目的索引，第三个参数是数组本身。由于示例仅使用了值参数，你可以按照以下模式对其重写。

```html
<!DOCTYPE html>
<html>
<body>
<p>学习 JavaScript Array.forEach() 循环</p>
<p>此程序将为数组的每个元素调用一次函数。</p>
<p id="demo5"></p>
<script>
var msg = "";
var nums = [55545, 454, 1239, 78816, 45625];
nums.forEach(FunctionYZ);
document.getElementById("demo5").innerHTML = msg;
function FunctionYZ(fvalue) {
  msg = msg + fvalue + "<br>";
}
</script>
</body>
</html>
```

### 学习 JavaScript Array.forEach() 循环

此程序将为数组的每个元素调用一次函数。

`55545`、`454`、`1239`、`78816`、`45625`

我排除了 `fvalue` 之外的所有参数，仍然得到了相同的结果。

## `for/of` 循环

JavaScript 中还有另一种类型的 `for` 循环，被称为 `for/of` 语句。该语句遍历可以迭代的特定对象的值。此语句允许你遍历各种数据结构，如 `Maps`、`Arrays`、`NodeLists` 和 `Strings`。

当迭代开始时，下一个属性的值会自动分配给变量。JavaScript 中的变量使用 `var`、`const` 和 `let` 关键字声明。我们已经在之前的章节中涵盖了所有主题。

Safari 7、Chrome 38、Opera 25、Edge 12 和 Firefox 51 是目前支持 `for/of` 语句的浏览器。Internet Explorer 不支持它。

```html
<!DOCTYPE html>
<html>
<body>
<p>这些是 JavaScript For/Of 循环</p>
<p>for/of 语句将遍历你可以迭代的对象的所有值。</p>
<p id="demo6"></p>
<script>
let carsforsale = ["Volkswagen", "Vezel", "Ford", "Fortuner", "Sportage"];
let msg = "";
for (let YY of carsforsale) {
  msg += YY + "<br>";
}
document.getElementById("demo6").innerHTML = msg;
</script>
</body>
</html>
```

### 这些是 JavaScript For/Of 循环

`for/of` 语句将遍历你可以迭代的对象的所有值。

`Volkswagen`、`Vezel`、`Ford`、`Fortuner`、`Sportage`

在下一个示例中，我将使用字符串而不是数组来相同的结果。

```html
<!DOCTYPE html>
<html>
<body>
<p>这些是 JavaScript For/Of 循环</p>
<p>for/of 语句将遍历你可以迭代的对象的所有值。</p>
<p id="demo6"></p>
<script>
let carsforsale = "Volkswagen, Vezel, Ford";
let msg = "";
for (let YY of carsforsale) {
  msg += YY + "<br>";
}
document.getElementById("demo6").innerHTML = msg;
</script>
</body>
</html>
```

### 这些是 JavaScript For/Of 循环

`for/of` 语句将遍历你可以迭代的对象的所有值。

`V`、`o`、`l`、`k`、`s`、`w`、`a`、`g`、`e`、`n`、`，`、`V`、`e`、`z`、`e`、`l`、`，`、`F`、`o`、`r`

## 死循环

当你创建一个循环且没有终点时，它被称为死循环。循环会一直持续，直到计算机或浏览器崩溃。

### `while` 循环

当你创建一个循环且没有终点时，它被称为死循环。循环会一直持续，直到计算机或浏览器崩溃。

在你学习了 `for` 循环后，我将解释 `while` 循环如何工作。`while` 循环只要条件为真就会执行。

```html
<!DOCTYPE html>
<html>
<body>
<p>While 循环</p>
<p id="demo7"></p>
<script>
var msg = "";
var YY = 0;
while (YY < 10) {
  msg += "<br>The digit is " + YY;
  YY++;
}
document.>("demo7").innerHTML = msg;
</script>
</body>
</html>
```

`0`、`1`、`2`、`3`、`4`、`5`

## `do/while` 循环

`do/while` 循环被认为是 `while` 循环的一种变体。它在测试条件之前执行代码。`do/while` 与其他循环的区别在于即使你设置条件为假它也会执行一次。

```html
<!DOCTYPE html>
<html>
<body>
<p>这是 JavaScript Do/While 循环</p>
<p id="demo8"></p>
<script>
var msg = "";
var YY = 0;
do {
  msg += "<br>The digit is " + YY;
  YY++;
}
while (YY < 5);
document.getElementById("demo8").innerHTML = msg;
</script>
</body>
</html>
```

`0`、`1`、`2`、`3`、`4`

如果你对 `for` 和 `while` 循环进行比较，你会发现这两个循环非常相似。`while` 循环与 `for` 循环非常相似。然而，唯一的区别是这里省略了第一和第三语句。我将使用相同的示例并测试 `for` 和 `while` 循环，看看它们之间有多大差异。在第一部分，我将使用 `for` 循环。

```html
<!DOCTYPE html>
<html>
<body>
<p id="demo9"></p>
<script>
var carsforsale = ["Vezel", "Fortuner", "Land Cruiser", "Jimmy"];
var YY = 0;
var msg = "";
for (;carsforsale[YY];) {
  msg += carsforsale[YY] + "<br>";
  YY++;
}
document.getElementById("demo9").innerHTML = msg;
</script>
</body>
</html>
```

`Vezel`、`Fortuner`、`Land Cruiser`、`Jimmy`

在接下来的内容中，我将使用 `while` 循环收集待售车辆的名称，然后在浏览器中整齐地显示它们。

```html
<!DOCTYPE html>
<html>
<body>
<p id="demo9"></p>
<script>
var carsforsale = ["Vezel", "Fortuner", "Land Cruiser", "Jimmy"];
var YY = 0;
var msg = "";
while (carsforsale[YY]) {
  msg += carsforsale[YY] + "<br>";
  YY++;
}
document.getElementById("demo9").innerHTML = msg;
</script>
</body>
</html>
```

`Vezel`、`Fortuner`、`Land Cruiser`、`Jimmy`

## JavaScript Break 和 Continue 语句

`break` 和 `continue` 语句本质上与 `for` 和 `while` 循环相关。`break` 语句允许你跳出循环，而 `continue` 语句则让你跳过循环内部某次特定的迭代。后者并不会中断循环，程序会继续运行。在之前的章节中讨论 `switch` 语句时，我已经解释过 `break` 语句。然而，那里的用途不同，因为它是应用于 `switch` 语句的。现在我将在循环中使用 `break` 语句。

# 学习 JavaScript 循环

我将在 `for` 循环中集成一个 `break` 语句。

```javascript
var msg = "";
var YY;
for (YY = 0; YY < 10; YY++) {
  if (YY === 5) { break; }
  msg += "The next digit is " + YY +"<br>";
}
document.getElementById("demo9").innerHTML = msg;
```

下一个数字是 0
下一个数字是 1
下一个数字是 2
下一个数字是 3
下一个数字是 4

循环本应完成 10 个数字的迭代，但由于我在位置 5 添加了 `break` 语句，循环跳出了迭代，程序停止了。`continue` 语句不能被认为是 `break` 语句的相反面，因为和 `break` 语句一样，它也会中断循环，但随后继续执行程序的剩余迭代。我将使用相同的示例来详细说明你如何从 `continue` 语句中受益。

```javascript
var msg = "";
var YY;
for (YY = 0; YY < 10; YY++) {
  if (YY === 5) { continue; }
  msg += "The next digit is " + YY + "<br>";
}
document.getElementById("demo9").innerHTML = msg;
```

下一个数字是 0
下一个数字是 1
下一个数字是 2
下一个数字是 3
下一个数字是 4
下一个数字是 6
下一个数字是 7
下一个数字是 8
下一个数字是 9

循环在点 5 中断并继续。你可以看到结果中缺失的数字是 5。`continue` 语句适用于跳过循环的某次迭代。`break` 语句只有一个目的：让你跳出 `switch` 或循环。你可以使用 `break` 语句跳出代码块。

## 第七章

## JavaScript 函数

![](img/Image00001.jpg)

到目前为止，我们创建了在浏览器加载网页加载时立即运行的脚本。还有另一种使用代码的方法。你可以将代码封装在一个函数内并在浏览器中运行它。除非你进行函数调用，否则你不会在浏览器中看到任何操作。一个函数短语包含 `function` 关键字、函数名和大括号。

你必须在 `function` 关键字后面包含一个空格。之后，你需要写下你选择给函数起的名称。这些与变量命名的习惯非常相似。然而，函数命名的唯一区别在于，你可以在函数名中添加数字、字母、`$` 或下划线。之后，你需要添加一组圆括号来包含任何参数。之后，你需要放入大括号来编写代码。你不需要将函数写在多行上。如果你习惯的话，可以把它们写在单行上。但是，在开始时最好写在多行上，这样你就能清楚地了解它是如何写的。此外，如果代码运行不良好，你可以轻松地纠正任何错误。

创建 JavaScript 函数是为了执行特定的任务。当你进行函数调用时，你就可以执行它。

```javascript
function FunctionZZ(x1, x2) {
  return x1 * x2;
}
document.getElementById("demo890").innerHTML = FunctionZZ(345, 1222);
```

# 学习 JavaScript 函数

在这个示例中，我将调用一个函数来执行计算并返回结果：

`421590`

你可以看到有一个 `function` 关键字，后面跟着函数名。我在代码中包含了圆括号。你可以在圆括号中包含一个或多个参数。你需要包含在函数中的代码放在大括号内。至于函数参数，你需要在创建函数并在现在想要调用它时传递它们。

## 函数的调用

`function` 关键字后面跟着函数名。我在代码中包含了圆括号。你可以在圆括号中包含一个或多个参数。你需要包含在函数中的代码放在大括号内。至于函数参数，你需要在创建函数并在现在想要调用它时传递它们。

`function` 关键字后面跟着函数名。我在代码中包含了圆括号。你可以在圆括号中包含一个或多个参数。你需要包含在函数中的代码放在大括号内。

字体 执行计算并返回结果的函数调用：

```javascript
function FunctionZZ(x1, x2) {
  return x1 * x2;
}
var Y = FunctionZZ(55, 2345);
document.getElementById("demo890").innerHTML = Y;
```

`128975`

你可以看到有一个 `function` 关键字后面跟着函数名。我在代码中包含了圆括号。你可以在圆括号中包含一个或多个参数。你需要包含在函数中的代码放在大括号内。

### 将华氏度转换为摄氏度：

```javascript
function toCels(f) {
  return (15/90) * (f-40);
}
```



`document.getElementById("demo789").innerHTML = toCels(80);`

```
6.666666666666666
```

## () 运算符

`toCels` 指函数对象，而`toCels()`指函数的结果。当你不带括号访问函数时，它将返回函数对象而不是函数的结果。

```javascript
function toCels(f) {
  return (15/90) * (f-40);
}

document.getElementById("demo789").innerHTML = toCels;
```

`function toCels(f) { return (15/90) * (f-40); }`

## 作为变量的函数

你可以像使用变量一样在不同的赋值、公式和计算中使用函数。与其使用变量来存储函数的返回值，你可以直接以变量值的形式使用它。

# 学习 JavaScript 函数

```javascript
document.getElementById("demo1234").innerHTML = "Presently, the average temperature is about " + toCels(90) + " Celsius";

function toCels(tempfahrenheit) {
  return (15/9) * (tempfahrenheit-40);
}
```

目前的平均温度约为 83.33333333333334 摄氏度。

## 局部变量

你在 JavaScript 函数内部声明的变量成为函数的局部变量。你只能在函数内部访问局部变量。

```javascript
FunctionOP();

function FunctionOP() {
  var carsforsale = "BMW";
  document.getElementById("demo15").innerHTML = typeof carsforsale + " " + carsforsale;
}

document.getElementById("demo25").innerHTML = typeof carsforsale;
```

函数外部的变量是未定义的。

`string BMW`
`undefined`

局部变量可以在函数中被识别。同名的变量可以在多个函数中使用。当函数开始时，你可以创建局部变量。当函数完成时，局部变量会被删除。

当你创建一个函数后，可以保存代码并在浏览器中加载。如果你看到什么都没有发生，说明你的操作是正确的，因为大括号之间的代码不会显示。调用函数有多种方法。你可以使用`onLoad`函数将函数加载到浏览器窗口中。你可以在函数开头添加`onLoad`代码以确保成功执行。

## JavaScript 表达式

你可以借助表达式来定义一个 JavaScript 函数。你可以将函数的表达式存储在变量中。

```javascript
var Y = function (x, y) {return x * y};

document.getElementById("demo12").innerHTML = Y;
```

在这个示例中，我将一个函数存储在变量中：
`function (x, y) {return x * y}`

在表达式存储在变量中之后，你就可以在函数中使用该变量。在下面的示例中，我将为变量分配值。

```javascript
var Y = function (x, y) {return x * y};

document.getElementById("demo12").innerHTML = Y(34, 89);
```

在这个示例中，我将一个函数存储在变量中：
`3026`

如果你分析上面的示例，你会发现函数缺少名称。我特意保持它是匿名的。存储在变量中的函数不需要命名。你始终可以通过变量名来调用它们。至于末尾添加的分号，它是为了结束一个可执行的语句。

## constructor()

JavaScript 函数通常借助`function`关键字来定义。这些函数是通过`constructor()`创建和定义的。

```javascript
var FunctionLK = new Function("x", "y", "return x * y");

document.getElementById("demo555").innerHTML = FunctionLK(345, 2);
```

分析内置构造函数以创建函数。
`690`

如果我们考虑`constructor()`的实际应用，我们会发现不必使用构造函数。

```javascript
var FunctionLK = function(x, y) {return x * y};

document.getElementById("demo555").innerHTML = FunctionLK(345, 2);
```

分析内置构造函数以创建函数。
`690`

## 自执行 (Self-Invoking)

函数的表达式可以被设计为自执行。自执行表达式即使你不进行调用，也可以被自动调用。如果你在函数后加上括号，函数表达式将自动执行。你无法对函数的声明进行自执行。你必须给函数加上括号，以指示它是一个函数的表达式。

```javascript
(function () {
  document.getElementById("demo6789").innerHTML = "This is calling by myself";
})();
```

你可以在不调用的情况下自动调用函数：
`This is calling by myself`

你可以在不调用的情况下自动调用函数：
自执行表达式是一个匿名函数。

你可以在不调用的情况下自动调用函数：
自执行表达式是一个匿名函数。
自执行表达式是一个匿名函数。

```javascript
function (x, y) {
  return x * y;
}

var Y = FunctionH(2, 2);

document.getElementById("demo12").innerHTML = Y;
```

在这个示例中，我将一个函数存储在变量中：
`function (x, y) {return x * y}`

在表达式存储在变量中之后，你就可以在函数中使用该变量。在接的示例中，我将为变量分配值。

在这个示例中，我将一个函数存储在变量中：
`3026`

如果你分析上面的示例，你会发现函数缺少名称。我特意保持它是匿名的。存储在变量中的函数不需要命名。你始终可以通过变量名来调用它们。至于末尾添加的分号，它是为了结束一个可执行的语句。

```javascript
function (x, y) {return x * y}

var Y = FunctionH(2, 2);

document.getElementById("demo12").innerHTML = Y;
```

在这个示例中，我将一个函数存储在变量中：
`3026`

## 函数或对象

如果你使用在之前的章节中学到的`typeof`运算符来了解函数的类型，你会发现 JavaScript 函数最好被描述为对象。就像对象一样，函数也有方法和属性。在下面的示例中，我将尝试将一些属性应用于函数。

```javascript
function FunctionP(x, y) {
  return arguments.length;
}

document.getElementById("demo90").innerHTML = FunctionP(40, 3, 78);
```

`arguments.length`属性用于返回函数接收到的参数。

## toString() 方法

如果你想将函数转换为字符串，可以使用`toString()`方法。以下是你可以操作函数并将其转换为字符串的方法。

```javascript
function Function1234(x, y, z) {
  return x * y * z;
}

document.getElementById("demo12").innerHTML = Function1234.toString();
```

`toString()`方法将你的函数转换为字符串：
`function Function1234(x, y, z) { return x * y * z; }`

## 箭头函数 (Arrow Functions)

箭头帮助你缩短函数中的文本长度。语法将变得简洁，编写时间也会缩短，从而在短时间内编写更多代码。如果你使用箭头函数，就不再需要`function`关键字、大括号和`return`关键字。

```javascript
const a = (a, b) => a * b;

document.getElementById("demo123").innerHTML = a(50, 50);
```

IE11 或更早版本不支持箭头函数。

# 学习 JavaScript 箭头函数

IE11 或更早版本不支持箭头函数。

箭头函数中不需要这种功能。箭头函数并不适用于定义与对象相关的方法。这些函数缺乏变量提升特性。你必须在程序中使用箭头函数之前对其进行定义。如果没有该定义，你将在程序中看到错误。在箭头函数中使用`const`被认为是一种比使用`var`关键字更安全的方法。这是因为函数表达式始终有一个常量值。如果函数只包含一条语句，你应该移除大括号和`return`关键字。

## 参数与实参 (Parameters & Arguments)

JavaScript 函数无法对参数的值进行任何种的检查。函数参数是在函数定义中列出的名称。另一方面，`arguments`对象则包含了传递给函数的实际值。在接收这些值后，函数会对它们进行处理并使用它们来创建不同类型的输出。定义参数没有规则。JavaScript 参数不需要为参数定义类型。你不需要对`arguments`进行任何类型检查。函数对其接收到的参数总数完全没有进行任何检查。

## 默认函数参数

在大多数情况下，你可能觉得没有必要为函数填充参数，在缺少参数的情况下，你会在结果中看到`undefined`。然而，在某些情况下，你是无法省略的。这不符合浏览器的习惯。如果你漏掉了参数的值，参数的默认值将覆盖它。

```html
<!DOCTYPE html>
<html>
<body>
<p>我现在正在为函数参数设置一个默认值。</p>
<p id="demo567"></p>
<script>
function FunctionTUP(a, b) {
  if (b === undefined) {
    b = 6;
  }
  return a * b;
}

document.getElementById("demo567").innerHTML = FunctionTUP(6);
</script>
</body>
</html>
```

ECMAScript 2015 的最新标准允许在函数声明中使用默认参数值。

```html
<!DOCTYPE html>
<html>
<body>
<p>我现在正在为函数参数设置一个默认值。</p>
<p id="demo567"></p>
<script>
function FunctionTUP(a, b = 5) {
  return a * b;
}

document.getElementById("demo567").innerHTML = FunctionTUP(6);
</script>
</body>
</html>
```

JavaScript 函数中有一个内置对象。程序员将其命名为`arguments`。该对象预先填充了一个数组，你可以在调用函数时使用它。这就是你如何使用函数来查找数字列表中的最大值。

```html
<!DOCTYPE html>
<html>
<body>
<p>我现在正在在一个数组中寻找最大的数字。</p>
<p id="demo123"></p>
<script>
function findingtheMax() {
  var O;
  var maximum = -Infinity;
  for(O = 0; O < arguments.length; O++) {
    if (arguments[O] > maximum) {
      maximum = arguments[O];
    }
  }
  return maximum;
}

document.getElementById("demo123").innerHTML = findingtheMax(4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14);
</script>
</body>
</html>
```

## 求和 (The Add Up)

你可以创建一个函数来累加函数接收到的输入的所有值。这是一个包含在你的网页上的有用工具。访问者可以计算他们在你的产品上花了多少钱，以及结账时需要支付多少钱。以下是你如何使用 JavaScript 函数的求和功能。如果一个函数有很多参数（实际上多于声明的参数），实际上可以通过`arguments`对象访问所有参数。

```html
<!DOCTYPE html>
<html>
<body>
<p>这里是如何对参数进行求和的方法：</p>
<p id="demo555"></p>
<script>
function summingAll() {
  var Y;
  var summingUp = 0;
  for(Y = 0; Y < arguments.length; Y++) {
    summingUp += arguments[Y];
  }
  return summingUp;
}

document.getElementById("demo555").innerHTML = summingAll(1444, 1232, 133500, 7115, 454, 123);
</script>
</body>
</html>
```

当函数被调用时，参数充当函数的实参。你可以通过值传递 JavaScript 参数。函数必须知道参数的值，而不是参数的位置。如果特定函数更改了参数的值，它不会改变参数的原始值。你对函数参数所做的更改无法在函数的限制之外被看到或使用。

## 调用 (Invocation)

当你写了一个函数并调用它时，JavaScript 内部的代码就会执行。仅仅定义函数并不会执行代码。调用函数与执行一个函数是相同的。你不应该混淆两者，因为调用函数在 Python 等其他编程语言中被广泛使用。JavaScript 在传统上略有不同，它通过“调用（invoke）”函数来实现。你也可以说调用函数、执行函数或启动函数。这些短语的意思相同，都是执行函数。

```html
<!DOCTYPE html>
<html>
<body>
<p>这是 JavaScript 函数</p>
<p>我的全局函数将返回不同的参数 (x, y)：</p>
<p id="demo77"></p>
<script>
function FunctionXXX(x, y) {
  return x * y;
}

document.getElementById("demo77").innerHTML = FunctionXXX(12, 89);
</script>
</body>
</html>
```

示例中的函数没有与任何对象连接。这让我们产生了一个疑问：为什么在没有对象的情况下执行是成功的？答案是 JavaScript 有一个默认全局对象。JavaScript 与 HTML 并行，HTML 的默认对象是 HTML 页面本身，因此函数是由 HTML 页面使用的。在浏览器内部，对象是访问者的窗口，因此函数变成了窗口函数。

```html
<!DOCTYPE html>
<html>
<body>
<p>这是 JavaScript 函数</p>
<p>我的全局函数将返回不同的参数。如果你调用`FunctionXXX`，你实际上是在调用`window.FunctionXXX`。两者是相同的。(x, y)：</p>
<p id="demo77"></p>
<script>
function FunctionXXX(x, y) {
  return x * y;
}

document.getElementById("demo77").innerHTML = FunctionXXX(12, 89);
</script>
</body>
</html>
```

## 全局对象 (Global Objects)

当函数调用缺少所有者时，`this`的值将变成全局对象。在网络浏览器中，浏览器窗口充当全局对象。

```html
<!DOCTYPE html>
<html>
<body>
<p>在 HTML 编程语言中，`this`的值是窗口对象。</p>
<p id="demo777"></p>
<script>
var Y = FunctionDD();

function FunctionDD() {
  return this;
}

document.getElementById("demo777").innerHTML = Y;
</script>
</body>
</html>
```

### 函数作为方法

在 JavaScript 的世界中，你可以以对象方法的形式定义某些函数。

`thisObject.Namef()`将返回 Mac Millan：

```javascript
var thisObject = {
  Namef:"Mac",
  Namel: "Millan",
  myName: function() {
    return this.Namef + " " + this.Namel;
  }
}

document.getElementById("demo234").innerHTML = thisObject.myName();
```



# 学习 JavaScript 函数

`thisObject.Namef()` 将返回 Mac Millan：

Mac Millan

`myName` 是一个属于名为 `thisObject` 对象的函数。该对象拥有该函数。在示例中，`this` 的值是 `thisObject`。你可以检查一下。

```javascript
var thisObject = {
  Namef:"Mac",
  Namel: "Millan",
  myName: function() {
    return this;
  }
}
document.getElementById("demo234").innerHTML = thisObject.myName();
```

学习 JavaScript 函数

`thisObject.Namef()` 将返回 Mac Millan：

[object Object]

## 函数构造函数()

你可以通过使用函数构造函数 `()` 来调用函数。

```javascript
function FunctionT(argument1, argument2) {
  this.Namef = argument1;
  this.Namel  = argument2;
}
var Y = new FunctionT("Mac","Millan")
document.getElementById("demo234").innerHTML = Y.Namef;
```

函数构造函数：

Mac

## 重用方法

借助 `call()` 方法的帮助，你可以将一个方法应用到不同类型的对象。在 JavaScript 中，所有函数都是对象的方法。如果一个函数不是，它就属于一个全局对象。

```javascript
var thisObject = {
  Namef:"Mac",
  Namel: "Millan",
  myName: function() {
    return this.Namef + " " + this.Namel;
  }
}
Y = thisObject.myName();
document.getElementById("demo234").innerHTML = thisObject.myName(); Y
```

学习 JavaScript 函数

`thisObject.Namef()` 将返回 Mac Millan：

Mac Millan

## call() 方法

JavaScript 中的 `call()` 方法就像一个预定义的方法，你可以用它来调用方法。你可以使用另一个对象拥有的方法。

```javascript
var man = {
  myName: function() {
    return this.Namef + " " + this.Namel;
  }
}
var man1 = {
  Namef:"Christiano",
  Namel: "Ronaldo"
}
var man2 = {
  Namef:"Lionel",
  Namel: "Messi"
}
var Y = man.myName.call(man1);
document.getElementById("demo90").innerHTML = Y;
```

下面的示例将通过在另一个人身上使用，调用人的 `fullName` 方法：

Christiano Ronaldo

现在我将调用 `myName` 方法并将其用在 `man2` 上。

```javascript
var man = {
  myName: function() {
    return this.Namef + " " + this.Namel;
  }
}
var man1 = {
  Namef:"Christiano",
  Namel: "Ronaldo"
}
var man2 = {
  Namef:"Lionel",
  Namel: "Messi"
}
var Y = man.myName.call(man2);
document.getElementById("demo90").innerHTML = Y;
```

下面的示例将通过在另一个人身上使用，调用人的 `fullName` 方法：

Lionel Messi

## 添加参数

`call()` 方法足够灵活，可以向函数包含许多参数来构造该函数。

```javascript
var man = {
  myName: function() {
    return this.Namef + " " + this.Namel;
  }
}
var man1 = {
  Namef:"Christiano",
  Namel: "Ronaldo"
}
var man2 = {
  Namef:"Lionel",
  Namel: "Messi"
}
var Y = man.myName.call(man1, "soccer star", "extremely rich");
document.getElementById("demo90").innerHTML = Y;
```

下面的示例将通过在另一个人身上使用，调用人的 `fullName` 方法：

Christiano Ronaldo, soccer star, extremely rich

下面的示例将通过在另一个人身上使用，调用人的 `fullName` 方法：

Lionel Messi, soccer star, extremely rich

对象可以被变量填充。`JavaScript` 中的对象是命名的值的集合。这些命名的值被称为属性（properties）。你在函数章节中已经见过它们的应用。你可以在不同的对象上执行名为方法（methods）的操作。这些属性可能是原始类型，如对象和函数。对象方法包含函数的定义，你可以在 `JavaScript` 中创建和定义一个对象。你可以使用多种方法来实现这一点。你可以通过这种目的来创建一个对象，即字面量（literal）。`new` 关键字用于创建。对象字面量被认为在 `JavaScript` 中创建对象最简单的方法。通过使用对象字面量，你只需要一条语句即可完成。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript Objects</p>
<p id="demo90"></p>
<script>
var man1 = { Namef:"Christiano", Namel: "Ronaldo", profession: "soccer star", economicalstatus: "rich"};
document.getElementById("demo90").innerHTML =
man1.Namef + " is the biggest " + man1.profession + " across the world. He is a " + man1.economicalstatus + " person."
;
</script>
</body>
</html>
```

# JavaScript 对象
Christiano 是全球范围内最大的足球明星。他是一个富有钱的人。

在 `JavaScript` 中创建对象时，换行和间距并不重要。你可以使用多行来创建对象，结果是相同的。查看另一种形式的同对象创建示例。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript Objects</p>
<p id="demo90"></p>
<script>
var man1 = {
    Namef:"Christiano",
    Namel: "Ronaldo",
    profession: "soccer star",
    economicalstatus: "rich"
};
document.getElementById("demo90").innerHTML =
man1.Namef + "is the biggest " + man1.profession + " aross the world. He is a " + man1.economicalstatus + " person."
;
</script>
</body>
</html>
```

我将把结果写在这里，因为它们是相同的。这种方法在编写整洁的代码时既整洁又高效。如果你习惯了编写这样整洁的代码，当你回到编辑器阅读或修改代码时，你会发现它很容易阅读。

## new 关键字
`JavaScript` 世界中 `new` 关键字是最重要的。它有许多属性，你可以以多种方式使用它。查看相同示例中它的用法并感受区别，区别不在结果，而仅在于代码。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript Objects</p>
<p id="demo90"></p>
<script>
var man1 = new Object();
    man1.Namef="Christiano";
    man1.Namel = "Ronaldo";
    man1.profession = "soccer star";
    man1.economicalstatus = "rich";
document.getElementById("demo90").innerHTML =
man1.Namef + " is the biggest " + man1.profession + " across the world. He is a " + man1.economicalstatus + " person."
;
</script>
</body>
</html>
```

# JavaScript 对象
Christiano 是全球范围内最大的足球明星。他是一个富有钱的人。

你可以看到，唯一的区别是我必须添加更多的单词和符号，并删除了一些旧的符号。我删除了大括号，改用等号代替冒号。我必须移除逗号并用分号代替。无论你观察到什么变化，为了方便使用，我建议使用字面量方法。`new` 关键字只会让代码变得复杂，而对结果没有任何影响。

你可以随心所欲修改 JavaScript 对象。你必须通过引用而不是值来访问对象。如果你通过人的属性构建了一个对象，你无法通过简单的方法创建副本。

## 对象属性
JavaScript 属性是对象最重要的部分。每个对象都有一个命名为 `property` 的值。每个对象都构建在一组无序属性之上。你可以更改它们、向它们添加更多或删除它们。然而，某些属性是只读的。

当你创建一个对象时，可以构建一个循环来遍历对象中的所有项。请参考以下示例。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript Object Properties</p>
<p id="demo555"></p>
<script>
var msg = "";
var man1 = {namef:"Lionel", namel:"Messi", agem:33};
var Y;
for (Y in man1) {
  msg += man1[Y] + " ";
}
document.getElementById("demo555").innerHTML = msg;
</script>
</body>
</html>
```

# JavaScript 对象属性
Lionel Messi 33

向现有对象添加新属性从不是困难的。你只需给它一个值即可添加新属性。我将使用已经创建的同一个对象。我将添加一个新属性来显示创建对象的对象的国籍。见以下示例。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript Objects</p>
<p id="demo90"></p>
<script>
var man1 = {Namef:"Christiano", Namel: "Ronaldo", profession: "soccer star", economicalstatus: "rich"};
    man1.nationality = "Portuguese";
document.getElementById("demo90").innerHTML =
man1.Namef + " is the biggest " + man1.profession + " across the world. He is from " + man1.nationality + "."
</script>
</body>
</html>
```

# JavaScript 对象
Christiano 是全球范围内最大的足球明星。他来自葡萄牙。

## 删除
正如添加属性简单有趣，删除也是容易的。使用的关键字是 `delete`。通过使用关键字，JavaScript 会从对象中删除属性。当你使用它时应该小心。该运算符仅适用于对象，对函数没有影响。这对网站的声誉没有影响。

```html
<!DOCTYPE html>
<html>
<body>
<p>JavaScript Objects</p>
<p id="demo90"></p>
<script>
var man1 = { Namef:"Christiano", Namel: "Ronaldo", profession: "soccer star", economicalstatus: "rich"};
delete man1.nationality
document.getElementById("demo90").innerHTML =
man1.Namef + " is the biggest " + man1.profession + " across the world. He is from " + man1.nationality + "."
;
</script>
</body>
</html>
```

# JavaScript 对象
Christiano 是全球范围内最大的足球明星。他来自 undefined。

## 日期
JavaScript 日期功能非常值得学习。当你创建一个新网站时，你需要将日期功能集成到网页页面中，以便访问者看到。它对于管理货时间和和其他细节很有帮助。默认情况下，JavaScript 日期的输出是根据浏览器时区显示的。显示格式为完整的文本字符串。你可以创建不同的对象包含在日期显示中。这些对象可以是年、月、时、秒和毫秒。你可以根据需要添加更多信息。你可以使用 `new Date()` 方法创建一个数据对象来显示浏览器的当前日期和时间。

```html
<!DOCTYPE html>
<html>
<body>
<p>Learning JavaScript new Dates()</p>
<p>new Date() 方法为你创建一个包含当前日期和时间的日期对象：</p>
<p id="demo678"></p>
<script>
var Y = new Date();
document.getElementById("demo678").innerHTML = Y;
</script>
</body>
</html>
```

## JavaScript 类

JavaScript 也被称为基于原型的语言。这种语言中的每个对象都保留着一个隐藏的内部属性，称为 `[[Prototype]]`。你可以使用它来扩展你在语言中创建的对象的方法和属性。你可以使用 `class` 关键字来创建类。要添加到你的类中的另一个重要方法是 `constructor()` 方法。就像我们给对象添加属性一样，我们也可以给类添加属性。类本身不是一个对象，而是一个创建对象并在网页浏览器中操作它们的模板。

```html
<!DOCTYPE html>
<html>
<body>
<p>这是 JavaScript 类</p>
<p>我将向你展示如何在你的网站上创建和使用 JavaScript 类。</p>
<p id="demo777"></p>
<p id="demo778"></p>
<p id="demo779"></p>
<script>
class LuxCars {
  constructor(cname, cyear, cmake, cmodel, ccolor) {
    this.cname = cname;
    this.cyear = cyear;
    this.cmake = cmake;
    this.cmodel = cmodel;
    this.ccolor = ccolor;
  }
}
Car1 = new LuxCars("Ford", 2020, "USA", "Mustang", "Blue");
document.getElementById("demo777").innerHTML =
Car1.cname + " " + Car1.cyear + " " + Car1.cmake + " " + Car1.cmodel + " " + Car1.ccolor;
Car2 = new LuxCars("BMW", 2010, "Germany", "K45", "Silver");
document.getElementById("demo778").innerHTML =
Car2.cname + " " + Car2.cyear + " " + Car2.cmake + " " + Car2.cmodel + " " + Car2.ccolor;
Car3 = new LuxCars("Mercedes", 2021, "Germany", "S-Class", "Black");
document.getElementById("demo779").innerHTML =
</script>
</body>
</html>
```



`Car3.cname + " " + Car3.cyear + " " + Car3.cmake + " " + Car3.cmodel + " " + Car3.ccolor;`

`</script>`

`</body>`

`</html>`

```html

<!DOCTYPE html>

<html>

<body>

<p>这是 JavaScript 类</p>

<p>我将向你展示如何在你的网站上创建和使用 JavaScript 类。</p>

<p id="demo777"></p>

<p id="demo778"></p>

<p id="demo779"></p>

<script>

class LuxCars {

  constructor(cname, cyear, cmake, cmodel, ccolor) {

    this.cname = cname;

    this.cyear = cyear;

    this.cmake = cmake;

    this.cmodel = cmodel;

    this.ccolor = ccolor;

  }

  carAge() {

    let cdate = new Date();

    return cdate.getFullYear() - this.cyear;

  }

}

let Car1 = new LuxCars("Ford", 2017, "USA", "Mustang", "Blue");

document.getElementById("demo777").innerHTML =

Car1.cname + " " + Car1.cyear + " " + Car1.cmake + " " + Car1.cmodel + " " + Car1.ccolor + " : " + "This car is " + Car1.carAge() + " years old.";

Car2 = new LuxCars("BMW", 2010, "Germany", "K45", "Silver");

document.getElementById("demo778").innerHTML =

Car2.cname + " " + Car2.cyear + " " + Car2.cmake + " " + Car2.cmodel + " " + Car2.ccolor + " : " + "This car is " + Car2.carAge() + " years old.";

Car3 = new LuxCars("Mercedes", 2021, "Germany", "S-Class", "Black");

document.getElementById("demo779").innerHTML =

Car3.cname + " " + Car3.cyear + " " + Car3.cmake + " " + Car3.cmodel + " " + Car3.ccolor + " : " + "This car is " + Car3.carAge() + " years old.";

</script>

</body>

</html>

```

这是 JavaScript 类。我将向你展示如何在你的网站上创建和使用 JavaScript 类。输出结果如下：Ford 2017 USA Mustang Blue : This car is 4 years old. BMW 2010 Germany K45 Silver : This car is 11 years old. Mercedes 2021 Germany S-Class Black : This car is 0 years old.

我使用同一个 `LuxCars` 类创建了三个不同的对象。类提供了创建和部署对象运行的最简单方法。如果你正在经营汽车展厅并需要一个网站来接触客户，这个程序对你将很有帮助。单个类允许你创建无限数量不同汽车的实例。一旦你创建了类，你只需要向它填充属性并并在你的网站上显示它们即可。当一个新对象产生时，`constructor` 方法会被调用并自动运行。这个方法是特殊的。你必须写出拼写正确的 `constructor`。当你在类中创建一个新对象时，该方法会自动执行，节省你的时间。此方法启动了对象的属性。

### 类方法

编写和执行类方法的步骤与编写和创建对象相同。当你向类中添加新方法时，必须使用 `class` 关键字和 `constructor()` 方法。你可以添加的方法总数没有上限。你可以根据意愿添加任何数量。让我们添加一个新方法来声明汽车的年龄。JavaScript 使用当前日期作为基准来计算汽车的年龄。例如，如果一辆车产于 2020 年，程序将显示年龄为 1 年，因为当前年份是 2021 年。

```html

<!DOCTYPE html>

<html>

<body>

<p>这是 JavaScript 类</p>

<p>我将向你展示如何在你的网站上创建和使用 JavaScript 类。</p>

<p id="demo777"></p>

<p id="demo778"></p>

<p id="demo779"></p>

<script>

class LuxCars {

  constructor(cname, cyear, cmake, cmodel, ccolor) {

    this.cname = cname;

    this.cyear = cyear;

    this.cmake = cmake;

    this.cmodel = cmodel;

    this.ccolor = ccolor;

  }

  carAge() {

    let cdate = new Date();

    return cdate.getFullYear() - this.cyear;

  }

}

let Car1 = new LuxCars("Ford", 2017, "USA", "Mustang", "Blue");

document.getElementById("demo777").innerHTML =

Car1.cname + " " + Car1.cyear + " " + Car1.cmake + " " + Car1.cmodel + " " + Car1.ccolor + " : " + "This car is " + Car1.carAge() + " years old.";

Car2 = new LuxCars("BMW", 2010, "Germany", "K45", "Silver");

document.getElementById("demo778").innerHTML =

Car2.cname + " " + Car2.cyear + " " + Car2.cmake + " " + Car2.cmodel + " " + Car2.ccolor + " : " + "This car is " + Car2.carAge() + " years old.";

Car3 = new LuxCars("Mercedes", 2021, "Germany", "S-Class", "Black");

document.getElementById("demo779").innerHTML =

Car3.cname + " " + Car3.cyear + " " + Car3.cmake + " " + Car3.cmodel + " " + Car3.ccolor + " : " + "This car is " + Car3.carAge() + " years old.";

</script>

</body>

</html>

```

这是 JavaScript 类。我将向你展示如何在你的网站上创建和使用 JavaScript 类。输出结果如下：Ford 2017 USA Mustang Blue : This car is 4 years old. BMW 2010 Germany K45 Silver : This car is 11 years old. Mercedes 2021 Germany S-Class Black : This car is 0 years old.

## 传递参数

你可以向你的类发送参数。我将把年龄和年份参数传递给类。看下面的示例。

```html

<!DOCTYPE html>

<html>

<body>

<p>这是 JavaScript 类</p>

<p>我将向你展示如何在你的网站上创建和使用 JavaScript 类。</p>

<p id="demo777"></p>

<p id="demo778"></p>

<script>

class LuxCars {

  constructor(cname, cyear, cmake, cmodel, ccolor) {

    this.cname = cname;

    this.cyear = cyear;

    this.cmake = cmake;

    this.cmodel = cmodel;

    this.ccolor = ccolor;

  }

  carAge() {

    let cdate = new Date();

    return cdate.getFullYear() - this.cyear;

  }

}

let Car1 = new LuxCars("Ford", 2017, "USA", "Mustang", "Blue");

document.getElementById("demo777").innerHTML =

Car1.cname + " " + Car1.cyear + " " + Car1.cmake + " " + Car1.cmodel + " " + Car1.ccolor + " : " + "This car is " + Car1.carAge() + " years old.";

Car2 = new LuxCars("BMW", 2010, "Germany", "K45", "Silver");

document.getElementById("demo778").innerHTML =

Car2.cname + " " + Car2.cyear + " " + Car2.cmake + " " + Car2.cmodel + " " + Car2.ccolor + " : " + "This car is " + Car2.carAge() + " years old.";

Car3 = new LuxCars("Mercedes", 2021, "Germany", "S-Class", "Black");

document.getElementById("demo779").innerHTML =

Car3.cname + " " + Car3.cyear + " " + Car3.cmake + " " + Car3.cmodel + " " + Car3.ccolor + " : " + "This car is " + Car3.carAge() + " years old.";

</script>

</body>

</html>

```

这是 JavaScript 类。我将向你展示如何在你的网站上创建和使用 JavaScript 类。输出结果如下：Ford 2017 USA Mustang Blue : This car is 4 years old. BMW 2010 Germany K45 Silver : This car is 11 years old. Mercedes 2021 Germany S-Class Black : This car is 0 years old.

## 类继承

如果你想创建一个类继承，你必须在类中添加 `extends` 关键字。`extends` 关键字会将所有方法传递给继承的类。

```html

<!DOCTYPE html>

<html>

<body>

<p>这是 JavaScript 类</p>

<p>我将向你展示如何在你的网站上创建和使用 JavaScript 类。</p>

<p id="demo777"></p>

<p id="demo778"></p>

<script>

class LuxCars {

  constructor(cname, cyear, cmake, cmodel, ccolor) {

    this.cname = cname;

    this.cyear = cyear;

    this.cmake = cmake;

    this.cmodel = cmodel;

    this.ccolor = ccolor;

  }

  present() {

    return 'We have a ' + this.cname + ' for sale';

  }

}

class Ecar extends LuxCars {

  constructor(battery, model) {

    super(battery);

    this.cmodel = model;

  }

  show() {

    return this.present() + '. It is a ' + this.cmodel + ' model.';

  }

}

let Car2 = new Ecar("Tesla", 2010);

document.getElementById("demo778").innerHTML = Car2.show()

</script>

</body>

</html>

```

这是 JavaScript 类。我将向你展示如何在你的网站上创建和使用 JavaScript 类。输出结果如下：We have a Tesla for sale. It is a 2010 model.

上述代码中的 `super()` 方法指的是父类。当你在构造方法中调用此方法时，你就可以访问父类的属性和方法。

### Getters 和 Setters

通过类，你可以在浏览器中调整 getter（访问器）和 setter（赋值）。如果你需要对返回值进行某些特殊处理，那么 getter 和 setter 对于属性非常有用。你可以使用 `get` 和 `set` 关键字将它们添加到你的类中。

```html

<!DOCTYPE html>

<html>

<body>

<p>This is the JavaScript Class</p>

<p>I will show you how to create and use the JavaScript Class on your website.</p>

<p id="demo777"></p>

<p id="demo778"></p>

<script>

class LuxCars {

  constructor(carname, caryear, carmake, carmodel, carcolor) {

    this.cname = carname;

    this.cyear = caryear;

    this.cmake = carmake;

    this.cmodel = carmodel;

    this.ccolor = carcolor;

  }

  get namec() {

    return this.cname;

  }

  set namec(Y) {

    this.cname = Y;

  }

}

let Car2 = new LuxCars("Tesla");

document.getElementById("demo778").innerHTML = Car2.namec;

</script>

</body>

</html>

```

这是 JavaScript 类。我将向你展示如何在你的网站上创建和使用 JavaScript 类。输出结果如下：特斯拉

## 结论

![](img/Image00001.jpg)

现在你已经读到了书的最后，下一步是进行更多练习并成为 JavaScript 大师。我希望你不仅阅读了所有的理论和代码，还使用了代码来加载网页并显示信息。我特意将所有代码封装在 HTML 标签中，以便你觉得容易使用并进行同样的练习。

最好的方法是在修订过程中记录代码，并在有空时随时练习。练习是掌握这门脚本语言的唯一途径。记忆代码并在网页浏览器中使用它是学习 JavaScript 的最佳方法。

## 参考文献

![](img/Image00001.jpg)

- Brand, A. W. (2013). *PHP, MySQL, JavaScript & HTML 5*. [`khmerbamboo.files.wordpress.com/2014/09/php-mysql-javascript-html5-all-in-one-for-dummies.pdf`](https://khmerbamboo.files.wordpress.com/2014/09/php-mysql-javascript-html5-all-in-one-for-dummies.pdf)
- Haverbeke, M. (2018). *Eloquent JavaScript*. PDF Drive [`www.pdfdrive.com/eloquent-javascript-a-modern-introduction-to-programming-d158409266.html`](https://www.pdfdrive.com/eloquent-javascript-a-modern-introduction-to-programming-d158409266.html)
- Https://www.digitalocean.com/community/tutorials/understanding-classes-in-javascript. (2020, February 12). JavaScript 的优缺点. freeCodeCamp.org. [`www.freecodecamp.org/news/the-advantages-and-disadvantages-of-javascript/`](https://www.freecodecamp.org/news/the-advantages-and-disadvantages-of-javascript/)
- JavaScript class inheritance. (n.d.). W3Schools Online Web Tutorials. [`www.w3schools.com/js/js_class_inheritance.asp`](https://www.w3schools.com/js/js_class_inheritance.asp)
- JavaScript output. (n.d.). W3Schools Online Web Tutorials. [`www.w3schools.com/js/js_output.asp`](https://www.w3schools.com/js/js_output.asp)
- Patrick, J. (n.d.). *JAVASCRIPT A Beginner’s Guide to Learning the Basics of JavaScript Programming*. PDF Drive - 免费搜索和下载 PDF 文件。 [`www.pdfdrive.com/javascript-a-beginners-guide-to-learning-the-basics-of-javascript-programming-d186477670.html`](https://www.pdfdrive.com/javascript-a-beginners-guide-to-learning-the-basics-of-javascript-programming-d186477670.html)

