# 初学者Web编码与开发指南 (5合1书籍)：学习 HTML, CSS, BOOTSTRAP, JAVASCRIPT 和 JQUERY














# 第一章

### HTML

### 导言

在本章中，将讨论用于设计网页的各种 HTML 组件。

HTML 页面的基本结构如下所示。

- 位于 `/<.../>` 内部的条目被称为标签（tags）。大多数标签都有开始标签和结束标签，例如 `<head>`（开始 head 标签）和 `</head>`（结束 head 标签）。某些标签没有结束标签，例如 `<!DOCTYPE ...` 和 `/>`。
- 注释写在 `<!--` 和 `-->` 之间。
- 这里第 1 行向网络浏览器提供了“HTML 版本”的详细信息。`html` 告诉它是版本 5。`head` 标签（html 的开始）以及指向 CSS 文件的链接等。
- `body` 标签（7-11 行）包含了在网络浏览器上显示的实际 HTML 代码。我们在结束的 body 标签（`</body>`）之前添加所有与 JavaScript 相关的代码。

```
<!DOCTYPE html> <!-- 告诉浏览器上面的 html 版本 -->
<html>
<head>
<!--头部相关标签，例如 title, links 等 -->
</head>
<body>
<!-- 此处是实际 HTML 文档 -->
<!-- 此处添加 JavaScript 文件 -->
</body>
</html>
```

### 第一段代码

在下面的代码中，消息“Hello World”显示在 HTML 页面上。图 1.1 是生成的 HTML。

- 标题（第 4 行）出现在浏览器的顶部。
- `<h1>` 标签被称为“标题”（header）标签，它的字体比普通文本大（参见“Hello World!”的尺寸）。
- `<p>` 标签被称为“段落”（paragraph）标签，可用于编写段落。

```
<!DOCTYPE html>
<html>
<head>
<title>HTML Tutorial</title>
</head>
<body>
<h1>Hello World!</h1>
<p>This is the first HTML code</p>
</body>
</html>
```

![](img/f70659d57873500d1a13fffa6bbe945a_5_0.png)

图 1.1：第一段代码

### 基础标签

- 表格 1.1 显示了编写基础“HTML” 代码所需的标签列表，即不带任何样式（例如加粗、斜体和编号等）的代码。

表格 1.1：基础标签列表

| 标签 | 说明 | 示例 |
|---|---|---|
| h1, ... h6 | 标题标签 h1 到 h6 | <h2> Hi </h2> |
| p | 段落（末尾的行） | <p> Hi </p> |
| span | span 之后不换行 | <span>Hi</span><span> Bye.</span> |
| div | 在内容之间进行划分 | <div> ... </div> |
| hyperlink | 将内容移动到居中 | 参见第 1.9 节 |
| center | | <center> Hi </center> |
| br | 换行（无结束标签） | <br /> 或 <br> |
| hr | 水平线（无结束标签） | <hr> 或 <hr> |
| pre | 保留格式 | <pre> ...... </pre> |
| table | 插入表格 | 参见第 1.5 节 |

- 让我们看看这些标签的每个示例，

> 注意：所有新代码都添加在 `body` 标签中之前的代码之后。因此，教程中只显示了新添加的代码。

```
<h2> Heading 2</h2>
<h6> He heading 6</h6>
```

### 1.3. 基础标签（接上页）

```
<p> This is paragraph </p>
<span> This is span.</span>
<span> The 'br' tag is used after span to break the line </span>
<br/>
<div style="color:blue">
'div' 标签可以使用 'style' 和 'classes' 等一次性对对其内部的标签进行格式化
<p> This paragraph is inside the 'div' tag </p>
<span> This span is inside the 'div' tag </span>
<br/>
</div>
<center>
<h3> Heading 3 is centered</h3>
<p><span> Centered span inside the paragraph. </span></p>
</center>
使用两个 'hr' 标签画出了两条水平线。
<hr/>
<hr/>
<pre>'pre' 标签保留了格式（非常适合写代码） # Python 代码
x=2
y=3
print(x+y)
</pre>
```

- 图 1.2 是上述代码的输出。阅读文本以理解每个标签。

### Heading 2

Heading 6

This is paragraph
The 'br' tag is used after span to break the line
The 'div' tag can be used for formatting the tags inside it at once using 'style' and 'classes' etc.
nThis paragraph is inside the 'div' tag
This span is inside the 'div' tag

### Heading 3 is centered

Centered span inside the paragraph.

使用两个 'hr' 标签画出了两条水平线。

```
'pre' 标签保留了格式（非常适合写代码）
### Python 代码
x=2
y=3
print(x+y)
```

![](img/f70659d57873500d1a13fffa6bbe945a_6_0.png)

### 属性

在图 1.2 中，我们看到了属性示例（例如 style），它将 `div` 标签内部所有元素的颜色更改为“蓝色”。

### 属性 'name' 和 'value'

- 属性定义在“标签”的起始部分。例如，在下面的代码中，属性 'style' 定义在 `div` 标签内部。

```
<div style="color:blue;">
</div>
```

- 属性包含两个部分，即 'name' 和 'value'。例如，在上面的代码中，属性的 name 和 value 分 'style' 和 'blue'。

### 核心属性

以下是网页设计中常用的三个属性。

- id: 'id' 是可以赋给任何标签的唯一名称。这在区分元素与其他元素时非常有用。
<p id="id">
- <p class="class">
- <span class="class">

（注：原文中此处存在大量重复的 id 描述，译文已按要求保持结构并针对性翻译）

...（此处重复内容略）...

### 表格

在本节中，我们将学习如何结合表 1.2 节讨论的某些属性绘制表格。

### 表格 1.3：创建表格的标签和属性

| 标签 | 说明 |
|---|---|
| table | 表格的开始和结束 |
| tr | 表格行 |
| th | 表头单元格
| td | 数据单元格 |
| 属性 | |
| rowspan | 合并行数 |
| colspan | 合并列数 |
| border | 边框宽度 |
| cellpadding | 单元间的空白宽度 |
| cellspacing | 边框内的空白宽度 |
| bgcolor | 背景颜色 |
| bordercolor | 边框颜色 |
| width | 表格宽度（数字或 %） |
| height | 表格高度（数字） |
| caption | 表格标题 |

- 表格 1.3 的某些属性在下面的示例中使用，

### 列表 1.1：带有边框和颜色

```
<!-- border - 颜色，宽度和高度 -->
<table border="1" bgcolor="black" width="450" height="100">
<caption>Table 1 : Various格的标签</caption>
<tr bgcolor="red">
  <th>Column 1</th>
  <th>Column 2</th>
  <th>Column 3</th>
</tr>
<tr bgcolor="yellow">
  <td>Data 1</td>
  <td>Data 2</td>
  <td>Data 3</td>
</tr>
<tr bgcolor="cyan">
  <td colspan="2">New Data 1</td>
  <td>New Data 2</td>
</tr>
</table>
```



```html
<tr bgcolor="cyan" <!-- row -->
  <td>Data 1</td><!-- data -->
  <td>Data 2</td>
  <td>Data 3</td>
</tr>
</table
```

- 图 1.3 是上述代码的输出，

| 列 1 | 列 2 | 列 3 |
| --- | --- | --- |
| Data 1 | Data 2 | Data 3 |
| New Data 1 | | New Data 2 |

表 1: 表格的各种标签

| 列 1 | 列 2 | 列 3 |
| --- | --- | --- |
| Data 1 | Data 2 | Data 3 |

表 2 : 宽度为 80%

图 1.3：由表 1.3 生成的表格

#### 文本格式

在本节中，我们将看到一些文本格式选项（参见表 1.4），例如**粗体**、*斜体*、下标和删除线等。

表 1.4：文本格式

| 标签 |  |
| --- | --- |
| b | 粗体 |
| i | 斜体 |
| u, ins | 下划线 |
| strike, del | 删除线 |
| sup | 上标 |
| sub | 下标 |
| big | 大号字体 |
| small | 小号字体 |

- 下面是一些文本格式的示例，其结果如图 1.4 所示，

```html
<!-- Text formatting -->
<p>This is <b>bold</b></b> text</p>
<p>This is <strike>striked</strike> text</p>
<p>This is <sub>subscript</sub> text</p>
```

#### 图像

图像有两个重要的属性，即 'src' 和 'alt'，如下所示，

- src 告诉“图像”文件的位置，例如在第 2 行中，图像 'logo.jpg' 将 'img' 文件夹内搜索。

#### 这是粗体文本

#### 这是带删除线的文本

#### 这是下标

图 1.4：文本格式

- alt 是“替代文本”，当未找到图像时显示。例如，在第 6 行中，图像名称写写了，即 'logo'（而不是 'logo'），因此 'alt' 的值即 'Missing Logo.jpg' 将如图 1.5 所示显示。

```html
<!-- Images -->
<img src="img/logo.jpg" alt="Logo.jpg" width="200"/>
<br/> <br>
<img src="img/logoa.jpg" alt="Missing Logo.jpg" width="200"/>
```

![](img/f70659d57873500d1a13fffa6bbe45a_10.png)

图 1.5：图像

**注意：** 还可以使用其他属性，例如 'height'、'align' 和 'border'。

### 列表

HTML 有三种列表：

- 无序列表：使用项目符号（参见第 2 和 9 行）
- 有序列表：使用数字（参见第 15、22 和 28 行）
- 定义列表：用于在 HTML 中编写定义（参见第 35 行）

```html
<!-- Lists -->
<!-- unordered list -->
<ul>
  <li>Pencil</li>
  <li>Pencil</li>
  <li>Eraser</li>
</ul>

<ul type="circle"> 符号符号：'square'、'circle' 或 'disc'
  <li>Pencil</li>
  <li>Pencil</li>
  <li>Eraser</li>
</ul>

<!-- ordered list -->
<ol>
  <li>Pencil</li>
  <li>Pencil</li>
  <li>Eraser</li>
</ol>

<ol type="i"> 样式：'i'、'I'、'1' 或 'A'
  <li>Pencil</li>
  <li>Pencil</li>
  <li>Eraser</li>
</ol>

<ol type="l" start="5"> 从 'v' 开始
  <li>Pencil</li>
  <li>Pencil</li>
  <li>Eraser</li>
</ol>

<!-- Definition list -->
<dl>
  <dt>HTML</dt>
  <dd>HTML is easy</dd>
  <dd>HTML is good</dd>
</dl>
```

### 链接

```html
<!-- links -->
<p><a href="#para1" id="para1">Link</a></p>
<a href="http://dsp.io/"> PythonDSP </a> 在当前窗口中打开。</p>
<p><a href="js.html" target="_blank"> JavaScript Tutorial </a> 在新窗口中打开。</p>

（下页继续）

#### 无序列表

- Pen
- Pencil
- Eraser

项目符号：'square'、'circle' 或 'disc'
- Pen
- Pencil
- Eraser

#### 有序列表

- 1. Pen
2. Pencil
3. Eraser

样式：'i'、'I'、'1' 或 'A'
i. Pen
ii. Pencil
iii. Eraser

从 'v' 开始
v. Pen
vi. Pencil
vii. Eraser

#### HTML 定义列表

HTML is easy
HTML is good

<p><a href="http://python.readthedocs.io/pdf">Download PDF, DOC or Zip Files</a></p>

<p><a href="mailto:thondyspl@gmail.com">Email me</a></p><p><a href="mailto:thondyspl@gmail.com?subject=Feedback">Feedback</a></p>

#### 跳转到到 id='paral' 的段落

### PythonDSP

在当前窗口中打开 JavaScript。

### 在窗口中打开 JavaScript。

### 下载 PDF、DOC 或 Zip 文件

### 联系我们

### 反馈邮件

注意：可以通过在'body标签'中定义这些属性来更改链接（alink，激活链接）、'link'和'vlink（访问过的链接））的颜色，如下所示，

```html
<body alink="green" link="blue" vlink="red">
```

### 表单

表单有几个属性：

| 控件 | 属性 | 值 |
| --- | --- | --- |
| text | 描述 | 单行输入 |
| password | 描述 | 掩码输入 |
| radio | 描述 | 组内单选 |
| checkbox | 描述 | 多选 |
| select | 描述 | 下拉列表 |
| file | 描述 | 文件选择 |
| button | 描述 | 可点击按钮 |
| hidden | 描述 | 用户对不可见 |
| textarea | 描述 | 多行文本 |
| image | 描述 | 嵌入图像 |

### 1.5. 列表

有几种类型的列表：

| 类型 | 描述 | 示例 |
| --- | --- | --- |
| 无序列表 | 使用项目符号 | <ul> |
| 有序列表 | 使用数字 | <ol> |
| 定义列表 | 使用键值对 | <dl> |

### HTML

HTML 是用于创建网页结构的语言。它由一系列标签组成，告诉浏览器如何显示内容。

常用标签包括：

*   `<html>`：HTML 页面的根元素
*   `<head>`：包含关于文档的元数据
*   `<body>`：包含可见页面内容
*   `<p>`：定义段落
*   `<a>`：定义超链接
*   `<img>`：定义图像
*   `<ul>`：定义无序列表

### 列表

列表用于分组相关项目。有三种列表：

- 无序列表：使用项目符号（圆圈、方形等）
- 有序列表：使用数字或字母
- 定义列表：用于术语及其定义

### 链接

链接用于连接一个页面到另一个页面。`<a>` 标签使用 `href` 属性来指定 URL。

```html
<a href="https://www.google.com">访问 Google</a>
```

### JavaScript

JavaScript 是一种用于让网页交互性的脚本语言。它允许你创建动态内容、动画等。

JavaScript 警窗示例：

```javascript
alert("Hello World!");
```

### 结论

HTML、CSS 和 JavaScript 是 Web 的构建块。通过掌握这三项技术，你可以创建精美且实用的网站。





### 文本输入

名称：例如 meher21

密码： 

单选按钮：名称应相同

- 男 ☐ 女 ☆ 婴儿 ☐

复选框：名称应不同

- ☑ 男 ☐ 女 婴儿 ☐

选择框：下拉列表

![](img/f70659d57873500d1a13fffa6bbe945a_16_0.png)

选择框：滚动

![](img/f70659d57873500d1a13fffa6bbe945a_16_1.png)

文本区域

```
Initial Text
x = 2
y = 3
```

> 图 1.7：用于创建表单的各种控制输入

### 按钮与隐藏

名称：Meher
密码：
你好
跳转到 jQuery 重置

图 1.8：表单中的各种按钮和隐藏输入

# 第二2 章

# 级联样式表 (CSS)

## 简介

CSS 用于增强网页。在第 1.4.2 节中，我们看到了用于更改文本颜色的属性 'style'。让我们按照下一节所示重写 'style' 示例。

### 内联 CSS

- 下面代码是“内联 CSS”的示例，其中样式定义在单个标签内部。

```
<!-- css.html -->
<!DOCTYPE html>
<html>
<head>
  <title>CSS Tutorial</title>
</head>
<body>
  <h3 style="color:blue"> 标题 1</h3>
  <h3 style="color:blue"> 标题 2</h3>
  <h3 style="color:blue"> 标题 3</h3>
</body>
</html>
```

在上面的代码中，我们有三个字体颜色为蓝色（blue）的“标题”。假设我们想将颜色改为红色，那么我们必须进入每一个 'h3' 标签并更改颜色。在这种情况下，这是很容易的，但如果我们有 5 个不同的 'html' 文件和 100 个标题，那么这个过程就不太方便了。在这样的情况下，正如下一节所示，CSS 可以非常有用。

### 嵌入式 CSS

在代码中，样式被嵌入在 'style' 标签内，如第 8-17 行所示。在这里，我们定义了两个类 i.h3_blue（第 21-23 行）和 .h3_red（第 26-28 行）。然后，第 9 行和第 13 行的选择器目标是类 .h3_blue 和 .h3_red，并将颜色分别改为蓝色和红色。在本章中，我们将详细讨论选择器（例如 #h3_blue）。

### 注意：

- 在 CSS 中，注释写在 /* 和 */ 之间。

### 2.1 简介

- CSS 包含三个部分。
- 选择器，例如 p,h3.h3_blue
- 属性，例如 color
- 属性值，例如 red（红色）

```
<!-- css.html -->
<!DOCTYPE html>
<html>
<head>
<title>CSS Tutorial</title>
<style type="text/css">
h3.h3_blue{
    /* 将颜色改为蓝色 */
    color: blue;
}

h3.h3_red{
    /* 将颜色改为红色 */
    color:red;
}
</style>
</head>
<body>
<h3 class="h3_blue"> 标题 1 </h3>
<h3 class="h3_blue"> 标题 2 </h3>
<h3 class="h3_blue"> 标题 3 </h3>
</body>
</html>
```

```
<h3 class="h3_red"> 标题 1 </h3>
<h3 class="h3_red"> 标题 2 </h3>
<h3 class="h3_red"> 标题 3 </h3>
```

5 下面是代码的输出，

### 外部 CSS

我们可以在不同的文件中编写 'CSS' 代码并将文件导入 'html' 文档，如本节所示。这样，我们可以轻松地管理文件。

- 'CSS' 代码保存在 'my_css.css' 文件中，该文件保存在 'asset/css' 文件夹内。

```
/* asset/css/my_css.css */
h3.h3_blue{
    color: blue;
}
h3.h3_red{
    color:red;
}
```

- 接下来，我们需要将 CSS 文件导入 'html' 文件中，如第 7 行所示。

```
<!-- css.html -->
（续见下一页）
```

### 标题 1
### 标题 3
### 标题 3
### 标题 1
### 标题 3
### 标题 3

![](img/f70659d57873500d1a13fffa6bbe945a_20_0.png)

```
<!DOCTYPE html>
<html>
<head>
  <title>CSS Tutorial</title>
  <link rel="stylesheet" type="text/css" href="asset/my_css.css">
</head>
<body>
  <h3 class="h3_blue"> 标题 1</h3>
  <h3 class="h3_blue"> 标题 3</h3>
  <h3 class="h3_blue"> 标题 3</h3>
  <h3 class="h3_red"> 标题 1</h3>
  <h3 class="h3_red"> 标题 3</h3>
  <h3 class="h3_red"> 标题 3</h3>
</body>
</html>
```

### 基础 CSS 选择器

CSS 有三种选择器：

- 元素：使用其名称选择，例如 'p'、'div' 和 'h1'。
- 类：使用 '.className' 选择。
- ID：使用 '#idName' 选择，例如 '#my_para'。

我们将使用以下 HTML 来理解选择器：

```
<!-- css.html -->
<!DOCTYPE html>
<html>
<head>
  <title>CSS Selectors</title>
  <link rel="stylesheet" type="text/css" href="my_css.css">
</head>
<body>
  <h3 class="h3_blue"> CSS Selectors </h3>
  <p class="c_head">带有类 c_head 的段</p>
  <p id="i_head">带有 id i_head 的段</p>
</body>
</html>
```

下面的代码显示了不同选择器的示例，输出如图 2.2 所示：

```
/* my_css.css */
/* 元素选择 */
h3 {
  color: blue;
}
/* 类选择 */
.c_head {
  font-family: cursive;
  color: orange;
}
/* id 选择 */
#i_head {
  font-variant: small;
  color: red;
}
```

### CSS 选择器

带有类 c_head 的段，带有 ID I_HEAD 的段

# 第 2 章 级联样式表 (CSS)

**重要：** 以下是优先级：

- ID（优先级最高）
- 类
- 元素

如果 CSS 具有相同优先级，则应用最后一个 CSS 规则。以下是带有标签的 HTML：

- 'p' 标签
- 带有类 c_head 的 'p' 标签
- 带有类 c_head 和 id i_head 的 'p' 标签

```
<!-- css.html -->
<!DOCTYPE html>
<html>
<head>
  <title>CSS Selectors</title>
  <link rel="stylesheet" type="text/css" href="asset/my_css.css">
</head>
<body>
  <p>段</p>
  <p class="c_head">带有类 c_head 的段</p>
  <p class="c_head" id="i_head">带有类 c_head 和 id i_head 的段</p>
</body>
</html>
```

以下是 CSS 代码。让我们理解所有 'p' 标签的格式。第 13 行的 HTML：由于 'id' 优先级最高，对#i_head (第 12 行) 会被第 24 行覆盖；因此颜色为红色。第 13 行有 'p' 标签，因此 'font-variant' 由第 17 行应用。此外，此标签具有类 c_head，因此 'font' 将设置为 'cursive'。第 12 行的 HTML：同样，标签的优先级比 '元素' 高，因此此行的颜色为橙色。第 10 行的 HTML：第 18 行定义的颜色将被第 24 行覆盖；因此颜色将为蓝色。图 2.3。

```
/* asset/my_css.css */
/* 选择 */
.c_head {
  font-family: cursive;
  /* 覆盖蓝色 */
}
/* id 选择 */
#i_head {
  color: red;
}
/*元素选择 */
p {
  font-variant: small-caps;
  color: blue;
}
```

（续见下一页）

```
/* 元素选择 */
p {
  color: green;
}
```

### 带有类 C_HEAD 的段
### 带有类 C_HEAD 和 ID I_HEAD 的段
### 带有类 C_HEAD 和 ID I_HEAD 的段

图 2.3：CSS 规则的优先级

### 更多选择器

表 2.1 显示了用于 HTML 各种元素的选择器组合。本节还显示了“属性选择器”的某些示例。

表 2.1：选择器列表

| 选择器 | 描述 |
| --- | --- |
| h1, p, span 等. | 元素选择器 |
| .className | 类选择器 |
| #idName | id 选择器 |
| * | 通用选择器（选择一切） |
| h1.className | 选择带有类 className 的 h1 |
| h1#idName | 选择带有 id idName 的 h1 |
| p span | 后代选择器（p 内部的 span） |
| p > span | 子选择器（作为 p 的直接后代的 span） |
| h1, h2, p | 组选择器（选择 h1, h2 和 p） |
| span[my id] | 选择带有属性 my_id 的 span |
| span[my id=m_span] | 选择带有属性 my_id=m_span 的 span |

### 属性选择器

- 在 html 文件末尾添加块代码。在这些行中添加了“自定义属性”（例如 my_id）。

```
<!-- css.html -->
<span with attribute 'my_id' value 'm_span'> </span>
<span[my_id] { 选择带有属性 my_id 的 span }
<span class='priority-2'> 带有属性 my_id 为 m_span2 的 span </span>
font-weight: bold;
```

- 这些自定义属性可以如下所示被选择，





## 第 2 章 级联样式表 (CSS)

（接上页）

```css
}
span[my_id=m_span] { /* 选择属性为 'my_id = _span' 的 'span' */
color: red;
}
```

#### 更多属性

表 2.2 显示了一些可以在 CSS 中使用的其他重要属性，

表 2.2：CSS 属性

| 属性 | 语法 | 描述/可能值 |
| --- | --- | --- |
| size | 20% | size = 20px |
| | 20px | 20 像素 |
| | 2em | 2 倍字体大小 |
| | 2mm, 2cm, 2in | 2 mm, cm 和英寸 |
| color | 颜色 | 例如 red, blue, green |
| | 十进制代码 (#RRGGBB 或 #RGB) | #FFF000 或 #FFF |
| | rgb(num, num, num) | rgb(0, 0, 255) 或 rgb(20, 10%, 70%) |
| link | a:link | a:link [color: red] |
| | a:hover | |
| | a:visited | |
| | a:active | |
| Font | font-family | serif, cursive |
| | font-style | normal, italic, oblique |
| | font-variant | normal, small-caps |
| | font-weight | normal, bold, lighter, 100-900 |
| | font-size | 10px, small, medium, large 等 |
| Text | color | red, #FFF |
| | letter-spacing | 10px |
| | word-spacing | 10 px |
| | text-align | right, left, center |
| | text-decoration | underline, outline, line-through, none |
| | text-transform | capitalize, uppercase, lowercase, none |
| | white-space | pre, normal, nowrap |
| | text-shadow | text-shadow:5px 5px 5px red; |
| Image | border | '1px', 或 '1px solid blue' |
| | height, width | 100px, 20% |
| Border | border | solid, dashed, double, none 等. |
| | border-top-style | |
| | border-bottom-style | |
| | border-left-style | |
| | border-right-style | |
| | border-width | 4px, 4pt |
| | border-bottom-width | 同样使用 'top', 'left', 'right' |
| border (快捷方式) | 1px solid blue |
| Margin | margin, margin-left 等. | |
| Padding | padding (top, bottom, left, right) | '10px 20px 2px' 或 '10px 2px' |
| | padding-right, padding-left 等. | |

## 第 3 章

## Bootstrap

## 引言

基础 HTML 设计的问题之一是网页在不同的浏览器或设备（例如手机、平板电脑和笔记本）上看起来可能不同。因此，我们可能需要根据浏览器或设备修改代码。使用 Bootstrap 可以轻松解决这个问题。

Bootstrap.js 是一个使用 HTML、CSS 和 JavaScript 进行 Web 设计的框架。它支持所有主流浏览器，例如 Firefox、Opera 和 Chrome 等。此外，Bootstrap 包含了几个预定义的类用于方便布局，例如下拉菜单、导航栏和警报等。最后，它本质上是响应式的，即布局随设备（如手机或笔记本电脑等）自动更改。

### 安装

Bootstrap 运行至少需要 3 个文件，可以从 Bootstrap 网站下载。

- bootstrap.css (第 7 行) ：此文件包含 bootstrap 的各种 CSS。
- bootstrap.js (第 16 行) ：此文件包含各种 JavaScript 功能，例如下拉菜单和警报等。
- jQuery.js (第 17 行) ：此文件是 jQuery 库，可以从 'jQuery' 网站下载。它是 'bootstrap' 正常运行所需的。

### 下载并引入文件

这些文件被下载并保存在 'asset' 文件夹中。接下来，我们需要如下将这些文件包含在 HTML 文档中。

```html
<!DOCTYPE html>
<html>
<head>
<title>Bootstrap 教程</title>
<!-- CSS -->
<link href="asset/bootstrap.css" rel="stylesheet">
<!-- 在下方添加自定义 CSS -->
</head>
<body>
<!-- Javascript -->
<!-- 在 bootstrap.min.js 之前放置 jquery；然后添加自定义 jquery -->
<script src="asset/js/jquery-3.3.min.js"></script>
<script src="asset/js/bootstrap.min.js"></script>
</body>
</html>
```

## 第 3 章 Bootstrap

### 添加 CDN

另一种通过 CDN 引入文件的方法。在这种方法中，我们不需要下载文件，只需像下方的第 8、17 和 19 行那样提供这些文件的链接。注意，在这种情况下，代码无法在离线模式下工作。

```html
<!DOCTYPE html>
<html>
<head>
<title>Bootstrap 教程</title>
<!-- CSS -->
<!-- 版本的编译后的 CSS -->
<link rel="stylesheet" href="https://cdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BWWY8iKIdgnmKyuhAHr32Omucw7nRYdg4v+PmTSsz/K8vbdE_j4hu4" crossorigin="anonymous">
<!-- 在下方添加自定义 CSS -->
</head>
<body>
<!-- JavaScript -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js" integrity="sha384-TCqib027aqviSMFHOM">
```
注意：在这种情况下，我们使用了第一种方法下载文件并包含在 html 文档中。

### 检查设置

让我们编写第一段代码来检查 Bootstrap 的设置是否正确。注意：我们不需要记忆 'dropdown' 按钮的代码。所有模板在 Bootstrap 网站上都可用。从那里复制并粘贴代码，并根据本教程的需要修改代码。

```html
<!DOCTYPE html>
<html>
<head>
<title>Bootstrap 教程</title>
<!-- CSS -->
<link href="asset/bootstrap.css" rel="stylesheet">
</head>
<body>
[/content] (注：原文此处似乎有截断或逻辑跳转，根据后续内容翻译)

*(注：由于原文文本在 `Check setup` 之后出现了逻辑重复和格式错乱，我将根据您提供的文本片段进行了最符合逻辑的翻译处理。)*

[content]
```html
<!DOCTYPE html>
<html>
<head>
<title>Bootstrap 教程</title>
<!-- CSS -->
<link href="asset/bootstrap.css" rel="stylesheet">
</head>
<body>
<!-- 示例 -->
<div class="dropdown">
  <button class="btn btn-default dropdown-toggle" type="button" data-toggle="dropdown" aria-expanded="false">
    下拉菜单
  </button>
  <ul class="dropdown-menu">
    <li><a href="#">Action</a></li>
    <li>
    < class class=""></a></li>
    <li class="dropdown-header">标题</li>
    <li><a href="#">Action</a></li>
    <li><a href="#"></a></li>
  </ul>
</div>
</body>
</html>
```




图 3.3：“极小”和“小”屏幕具有相同的网格大小（即 4）

### 嵌套列

我们可以通过在“列”（第 29 行）内部定义一个“行”（第 30 行），将一列划分为若干小列，如第 29-34 行所示。

```html
<!DOCTYPE html>
<html>
<head>
<title>Bootstrap Tutorial</title>
<!-- CSS --><link href="asset/bootstrap.min.css" rel="stylesheet">
<!-- 在下方添加自定义 CSS -->
<style type="text/css">
  .col-xs-1 .col-xs-2 .col-xs-3 .col-xs-4 .col-xs-5 .col-xs-6 .col-xs-7 .col-xs-8,
  .col-sm-1 .col-sm-2 .col-sm-3 .col-sm-4 .col-sm-5 .col-sm-6 .col-sm-7 .col-sm-8,
  .col-md-1 .col-md-2 .col-md-3 .col-md-4 .col-md-5 .col-md-6 .col-md-7 .col-md-8,
  .col-lg-1 .col-lg-2 .col-lg-3 .col-lg-4 .col-lg-5 .col-lg-6 .col-lg-7 .col-lg-8 {
  background-color: green;
  color: white;
  border: 1px solid red;
  height: 3em;/*框的高度*/
  text-align: center;/*文字垂直居中*/
}
</style>
</head>
<body>
<div class="row">
  <div class="col-md-4">
  <div class="row col-xs-4">
    <div class="row">
      <div class="col-xs-6">col-xs-6</div>
      <div class="col-xs-6">col-xs-6</div>
    </div>
  </div>
</div>
</div>
</div>
<!-- Javascript -->
<!-- 在 bootstrap.min.js 之前引入 jQuery；然后添加自定义 jquery -->
<script src="asset/js/jquery-3.1.min.js"></script>
<script src="asset/bootstrap.min.js"></script>
</body>
</html>
```

- 我们可以使用 'offset' 来偏移列，如第 27 行所示；相应的 HTML 页面如图 3.4 所示，

## 第 3 章. Bootstrap 

```html
<!DOCTYPE html>
<html>
<head>
<title>Bootstrap Tutorial</title>
<!-- CSS -->
<link href="asset/bootstrap.min.css" rel="stylesheet">
<!-- 在下方添加自定义 CSS -->
<style type="text/css">
.col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8,
.col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8,
.col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8,
.col-lg-9 { background-color: green;
color: white;
font-weight: bold;
border: 1px solid red;
height: 3cm;/*框的高度*/
text-align: center;/*文字垂直居中*/
</style>
</head>
<body>
<div class="row">
<div class="col-md-offset-2 col-md-2">
<div class="col-md-8">col-md-8</div>
</div>
</div>

![](img/f70659d57873500d13fabbe945a_30.png)

```html
<!-- 在 $(document).ready(function(){... }); 处引入 jQuery -->
<script src="asset/js/jquery-3.1.min.js"></script>
<!-- 图 14: 偏移 (Offset) -->
```

## 组件

理解了 'html'、'css' 和 'Bootstrap 网格' 后，Bootstrap 组件的使用非常简单。只需从 Bootstrap 网站复制代码并根据需要修改。

在本节中，我们将使用以下模板。

（下一页）

```html
<!DOCTYPE html>
<html>
<head>
<title>Bootstrap Tutorial</title>
<!-- CSS -->
<link href="asset/bootstrap.min.css" rel="stylesheet">
<!-- 在下方添加自定义 CSS -->
</head>
```

### 3.4. 组件
（接上页）

```html
<body>
<!-- 在 bootstrap.min.js 之前引入 jQuery；然后添加自定义 jquery -->
<script src="asset/js/jquery-3.1.min.js"></script>
<script src="asset/js/bootstrap.min.js"></script>
</body>
</html>
```

### 标签 (Labels)

- 'label' 用于创建标签（第 11 行）。
- 'label-info' 类将标签设置为蓝色（第 11 行）。
- 'labels' 的大小可以使用 'span' 标签进行更改（例如第 11 行）。

注意：Bootstrap 提供了 6 种颜色：
- danger
- info
- primary
- success

```html
<!DOCTYPE html>
<html>
<head>
<title>Bootstrap Tutorial</title>
<!-- CSS -->
<link href="asset/bootstrap.min.css" rel="stylesheet">
<!-- 在下方添加自定义 CSS -->
</head>
<body>
<h3>Example heading <span class="label label-info">New</span></h3>
<!-- 在 bootstrap.min.js 之前引入 jQuery；然后添加自定义 jquery -->
<script src="asset/js/jquery-3.1.min.js"></script>
<script src="asset/js/bootstrap.min.js"></script>
</body>
</html>
```

图 3.5 是上述代码的输出，

![](img/f70659d57873500d13fabbe945a_31.png)

图 3.5：标签 (Label)

## 第 3 章. Bootstrap

注意：所有代码将位于 `body` 标签，新代码将插入到之前的代码下方。'button' 元素可以如下文所示在 Bootstrap 中创建按钮。注意：我们可以使用 'lg'、'md' 和 'xs' 等设置按钮的大小。在第 3 行，Bootstrap 网页应用中添加了 glyphicon。

```html
<h3>Buttons</h3>
<button class="btn btn-primary">Sign<span></span></button>
<button class="btn btn-danger">Delete <span></span></button>
<button class="btn btn-lg-success">Submit</button>
<button class="btn btn-md-success">Submit</button>
```

图 3.6 是上述代码的输出，

![](img/f70659d57873500d13fabbe945a_32.png)

图 3.6：按钮 (Buttons)

### 表单 (Forms)

在本节中，添加 4 种表单，

### 3.4.3 表单

下方代码的输出如图 3.7 所示（下一页）

```html
<h2>Basic form</h2>
<div class="row">
<div class="col-sm-5" style="background: pink;">
<div class="panel-body">
<form class="form">
<div class="form-group">
<label for="exampleInput">Email address</label>
<input class="form-control" id="exampleInput" placeholder="Enter email">
</div>
<div class="form-group">
<label for="exampleInput">Password</label>
<input class="form-control" id="exampleInput" placeholder="Password" type="password">
</div>
</form>
</div>
</div>
</div>
```

```html
<div class="form-group">
  <label for="exampleInput">File input</label>
  <input id="exampleInput" type="file">
  <p class="help-block">Example block-level text here.</p>
  <div class="checkbox">
    <label>
      <input type="checkbox"> Check me
    </label>
  </div>
  <button type="submit" class="btn btn-info">Submit</button>
</form>
</div>
</div>
```

3.4. 组件
（接上页）

![](img/f70659d57873500d13fabbe945a_33.png)

### 水平表单 (Horizontal form)

下方代码的输出如图 3.8 所示，

```html
<h3>Horizontal form</h3>
<div class="row">
<div class="col-sm-5" style="background: pink;">
<div class="panel-body">
<form class="form-horizontal" role="form">
<div class="form-group">
<label class="col-lg-2 col-sm-2" for="exampleInput">Email</label>
<div class="col-lg-10">
  <input class="form-control" id="exampleInput" placeholder="Email" type="email">
</div>
</div>
<div class="form-group">
<label class="col-lg-2 col-sm-2" for="inputPassword">Password</label>
<div class="col-lg-10">
  <input class="form-control" id="inputPassword" placeholder="Password" type="password"
</div>
</div>
<div class="form-group">
<div class="col-lg-2 col-sm-2">
<div class="checkbox">
    <label>
      <input type="checkbox"> Remember me
    </label>
  </div>
</div>
<div class="col-lg-10 offset-offset-2">
  <button type="submit" class="btn-danger">Sign in</button>
</div>
</div>
</div>
</form>
</div>
</div>
</div>
```

### 内联表单 (Inline form)

下方代码的输出如图 3.9 所示。

```html
<h2>Inline form</h2>
<div class="row">
<div class="col-sm-5" style="background: pink;">
<div class="panel-body">
<form class="form-inline" role="form">
<div class="form-group">
<label class="sr-only" for="exampleInput2">Email address</label>
<input class="form-control" id="exampleInput2" placeholder="Enter email" type="email">
</div>
<div class="form-group">
<label class="sr-only" for="examplePassword2">Password</label>
<input class="form-control" id="examplePassword2" placeholder="Password" type="password"
</div>
</form>
<div class="checkbox">
  <label>
    <input type="checkbox"> Remember me
    </label>
  </div>
  <button type="submit" class="btn btn-info">Submit</button>
</form>
</div>
</div>
</div>
```





![](img/f70659d57873500d1a13fffa6bbe945a_35_0.png)

<div>
</div>
<div>
<br><br>
</div>

### 内联表单

![](img/f70659d57873500d1a13fffa6bbe945a_35_1.png)

### 模态表单

模态形式出现在弹出窗口中。下方代码的输出如图图 3.10 所示，

```html
<!-- model form -->
<h3>模态表单</h3>

<div class="row">
<div class="col-sm-5" style="background: pink">
<div class="panel-body">
  <!-- 用于生成模态表单的按钮 -->
  <a href="#myModal" data-toggle="modal" class="btn btn-xs btn-success" data-body>模态中的表单
</>

  <!-- 模态表单设置 -->
  <div aria-hidden="true" aria-labelledby="myLabel" role="dialog" tabindex="-1" id="myModal" class="modal fade">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <button aria-hidden="true" data-dismiss="modal" class="close"
                  type="button">&times;</button>
          <h4 class="modal-title">表单标题</h4>
        </div>
        <div class="modal-body">
          <!-- 实际表单 -->
          <form>
            <div class="form-group">
              <label for="exampleInputEmail">邮箱地址</label>
              <input class="form-control" id="exampleInputEmail"
                     placeholder="输入邮箱">
            </div>
            <div class="form-group">
              <label for="exampleInputPassword1">密码</label>
              <input class="form-control" id="exampleInputPassword1"
                     placeholder="密码">
            </div>
            <div class="form-group">
              <label for="exampleFileInput3">文件输入</label>
              <input id="exampleFileInput3" type="file">
              <p class="help-block">此处为示例帮助性文本。</p>
            </div>
            <div class="checkbox">
              <label>
                <input type="checkbox"> 选中我
              </label>
            </div>
            <button type="submit" class="btn btn-default">提交</button>
          </form>
          <!-- 实际结束 -->
        </div>
      </div>
    </div>
  </div>
</div>
</div>
</div>
<hr>
```

### 表单元素

下方代码的输出如图图 3.11 所示，

### 水平表单

![](img/f70659d57873500d1a13fffa6bbe945a_37_0.png)

### 内联表单

![](img/f70659d57873500d1a13fffa6bbe945a_37_1.png)

### 模态表单

![](img/f70659d57873500d1a13fffa6bbe945a_37_2.png)

图 3.10：模态表单

```html
<!-- 表单元素 -->
<h3>表单元素</h3>
<div class="row">
<div class="col-sm-5" style="background: pink">
<div class="panel-body">
  <form class="form-horizontal tasi-form" method="get">
    <div class="form-group">
      <label class="col-sm-2 col-sm-2 label-label">默认</label>
      <div class="col-sm-10">
        <input class="form-control" type="text">
      </div>
    </div>
    <div class="form-group">
      <label class="col-sm-2 col-sm-2 label-label">帮助文本</label>
      <div class="col-sm-10">
        <input class="form-control" type="text">
        <span class="help-block">一段会换行并可能的帮助文本。</span>
      </div>
    </div>
    <div class="form-group">
      <label class="col-sm-2 col-sm-2 label-label">圆角</label>
      <div class="col-sm-10">
        <input class="form-control round-input" type="text">
      </div>
    </div>
  </form>
</div>
</div>
</div>
<div class="form-group">
  <label class="col-sm-2 col-sm-2 label-label">输入焦点</label>
</div>
<div class="col-sm-10" id="focusedInput">
  <input class="form-control" value="这里已聚焦.."
       type="text">
</div>
<div class="form-group">
  <label class="col-sm-2 col-sm-2 control-label" for="disabled">禁用</label>
  <div class="col-sm-10">
    <input class="form-control" id="disabled"
           disabled type="text">
  </div>
</div>
<div class="form-group">
  <label class="col-sm-2 col-sm-2 control-label">占位符</label>
  <div class="col-sm-10">
    <input class="form-control" placeholder type="text">
  </div>
</div>
<div class="form-group">
  <label class="col-sm-2 col-sm-2 control-label">密码</label>
  <div class="col-sm-10">
    <input class="form-control" placeholder type="password">
  </div>
</div>
<div class="form-group">
  <label class="col-sm-2 col-sm-2 control-label">静态</label>
  <div class="col-sm-10">
    <p>example.com</p>
  </div>
</div>
```

### 控件大小

下方代码的输出如图图 3.12 所示，

```html
<!-- 控件大小 -->
<h3>控件大小</h3>
<div class="row">
<div class="col-sm-5" style="background: pink">
<div class="panel-body">
  <form class="form-horizontal tasi-form" method="get">
    <div class="form-group">
      <label class="col-sm-2 col-sm-2 label-label">默认</label>
      <div class="col-sm-10">
        <input class="form-control" type="text">
      </div>
    </div>
    <div class="form-group">
      <label class="col-sm-2 col-sm-2 label-label">帮助文本</label>
      <div class="col-sm-10">
        <input class="form-control" type="text">
        <span class="help-block">一段会换行并可能的帮助文本。</span>
      </div>
    </div>
    <div class="form-group">
      <label class="col-sm-2 col-sm-2 label-label">圆角</label>
      <div class="col-sm-10">
        <input class="form-control round-input" type="text">
      </div>
    </div>
    <div class="form-group">
      <label class="col-lg-2 col-sm-2 control-label">静态</label>
      <div class="col-sm-10">
        <p>example.com</p>
      </div>
    </div>
  </form>
</div>
</div>
</div>
```





# 第3章 Bootstrap

```
<div>
</div>
</div>
</div>
```

![](img/f70659d57873500d1a13fffa6bbe945a_42_0.png)

### 3.4. 组件

```html
<div class="form-group">
  <label class="col-sm-2 control-label col-lg-2" for="inputSuccess">列大小调整/
</label>
  <div class="col-lg-10">
    <div class="row">
      <div class="col-lg-2">
        <input class="form-control" placeholder="col-lg-2" type="text">
      </div>
      <div class="col-lg-3">
        <input class="form-control" placeholder="col-lg-3" type="text">
      </div>
      <div class="col-lg-4">
        <input class="form-control" placeholder="col-lg-4" type="text">
      </div>
    </div>
  </div>
</form>
```

### 按钮

- 复选框和单选框
- 选项一是这个和那个，一定要包含它为什么很棒
- 选项一是这个和那个，一定要包含它为什么很棒的选项
- 选项一是这个和那个，一定要包含它为什么很棒
- 选项二可以是其他的，选择它会取消选项一

行内复选框

- 1
2
3
4
5

选择框

| | | | | |
|---|---|---|---|
| 列大小调整 | col-lg-2 | col-lg-3 | col-lg-4 |

![](img/f70659d57873500d1a13fffa6bbe945a_43_0.png)

### 输入组

下方代码的输出如图 3.14 所示，

```html
<!-- Input groups -->
<h3>输入组</h3>
<div class="row">
  <div class="col-sm-2" style="background: pink;">
    <div class="panel-body">
      <form class="form-horizontal-form" method="get">
        <div class="form-group">
          <label class="col-sm-2 control-label col-lg-2">基础示例</label>
          <div class="col-lg-10">
            <div class="input-group">
              <span class="input-group-addon">@</span>
              <input class="form-control" placeholder="Username" type="text">
            </div>
          </div>
        </div>
      </form>
    </div>
  </div>
</div>
```

第3章. Bootstrap

```html
<div class="input-group m-bot-15">
  <input class="form-control input-addon" type="text">
  <span class="input-group-addon">.00</span>
</div>
<div class="input-group m-bot-15">
  <span class="input-group-addon">$</span>
  <input class="form-control" type="text">
  <span class="input-group-addon">.00</span>
</div>
<div class="form-group">
  <label class="col-sm-2 control-label col-lg-2">尺寸调整</label>
  <div class="col-lg-10">
    <div class="input-group input-group-addon m-bot-15">
      <span class="input-group-addon">@</span>
      <input class="form-control input-lg" placeholder="Username" type="text">
    </div>
    <div class="input-group m-bot-15">
      <span class="input-group-addon">@</span>
      <input class="form-control" placeholder="Username" type="text">
    </div>
    <div class="input-group input-group-sm m-bot-15">
      <span class="input-group-addon">@</span>
      <input class="form-control" placeholder="Username" type="text">
    </div>
  </div>
</div>
<div class="form-group">
  <label class="col-sm-2 control-label col-lg-2">复选框</label>
  <div class="col-lg-10">
    <div class="input-group m-bot-15">
      <span class="input-group-addon">
        <input type="checkbox">
      </span>
      <input class="form-control" type="text">
    </div>
    <div class="input-group m-bot-15">
      <span class="input-group-addon">
        <input type="radio">
      </span>
      <input class="form-control" type="text">
    </div>
  </div>
</div>
<div class="form-group">
  <label class="col-sm-2 control-label col-lg-2">按钮</label>
  <div class="col-lg-10">
    <div class="input-group m-bot-15">
      <span class="btn-white">
        <button type="button">Go</button>
      </span>
      <input class="form-control" type="text">
    </div>
  </div>
</div>

```html
<div class="input-group m-bot-5">
  <input class="form-control" type="text">
  <span class="input-group-btn">
    <button class="btn-white" type="button">Go!</button>
  </span>
</div>
<div class="input-group m-bot-5">
  <input class="form-control" type="text">
  <div class="input-group-btn">
    <button class="btn-white dropdown-toggle" data-toggle="dropdown">
      <span class="caret"></span>
    </button>
    <ul class="dropdown-menu">
      <li><a href="#">操作</a></li>
      <li><a href="#">另一个操作</a></li>
      <li><a href="#">此处其他内容</a></li>
      <li></li>
      <li><a href="#">分离链接</a></li>
    </ul>
  </div>
  <input class="form-control" type="text">
</div>
<div class="input-group m-bot-5">
  <input class="form-control" type="text">
  <div class="input-group-btn">
    <button class="btn-white dropdown-toggle" data-toggle="dropdown">
      <span class="caret"></span>
    </button>
    <ul class="dropdown-menu pull-right">
      <li><a href="#">操作</a></li>
      <li><a href="#">另一个操作</a></li>
      <li><a href="#">此处其他内容</a></li>
      <li></li>
      <li><a href="#">分离链接</a></li>
    </ul>
  </div>
</div>
<div class="form-group">
  <label class="col-sm-2 control-label col-lg-2">分段按钮</label>
  <div class="col-sm-10">
    <div class="input-group m-bot-5">
      <div class="input-group-btn">
        <button class="btn-white" type="button">操作</button>
        <button class="btn-white dropdown-toggle" data-toggle="dropdown">
          <span class="caret"></span>
        </button>
        <ul class="dropdown-menu">
          <li><a href="#">操作</a></li>
          <li><a href="#">另一个操作</a></li>
          <li><a href="#">此处其他内容</a></li>
          <li></li>
          <li><a href="#">分离链接</a></li>
        </ul>
      </div>
      <input class="form-control" type="text">
    </div>
  </div>
</div>
```

```html
<div class="input-group m-bot">
  <input class="form-control" type="text">
  <div class="input-group-btn">
    <button class="btn-white" type="button" aria-expanded="false">操作</button>
    <button class="btn-white dropdown-toggle" data-toggle="button">
      <span class="caret"></span>
      <ul role="menu" class="dropdown-menu pull-right">
        <li><a href="#">操作</a></li>
        <li><a href="#">另一个操作</a></li>
        <li><a href="#">此处其他内容</a></li>
        <li></li>
        <li><a href="#">分离链接</a></li>
      </ul>
    </button>
  </div>
</div>
</div>
```

![](img/f70659d57873500d1a13fffa6bbe945a_47_0.png)

| | |
|---|---|
| 基础示例 | 用户名 |
| | $ |
| 字符串 | 用户名 |
| | 用户名 |
| 复选框和单选框 | |
| 按钮选项 | |
| 分段按钮 | 操作 |

### 图 14: 输入组

### 导航栏 (navbar)

对于导航栏，在第 8 行添加了另一个 'css' 文件。此 CSS 将为 'navbar' 创建顶部顶部空间，使其不会与 HTML 页的内容重叠。此外，链接 13-44 为导航栏添加了各种链接。最后，我们可以在第 46 行下方添加 HTML 标题。

下方代码的输出如图 3.15 所示。

```html
<!DOCTYPE html>
<html>
<head>
<title>Bootstrap 教程</title>
<!-- CSS -->
<link href="asset/bootstrap.min.css" rel="stylesheet">
<!-- 在下方添加自定义 CSS -->
<link href="asset/css/theme.css" rel="stylesheet"> <!-- 为导航栏顶部留出空间 -->
</head>

<body>
  <div class="navbar navbar-inverse navbar-fixed-top">
    <div class="container">
      <div class="navbar-header">
        <button type="button" class="navbar-toggle" data-toggle="collapse" data-target="navbar-collapse">
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </button>
        <a class="navbar-brand hidden-sm" href="http://pythondsp.readthedocs.io/">PythonDSP</a>
      </div>
      <div class="row">
        <div class="navbar-collapse collapse">
          <ul class="nav navbar-nav">
            <li><a href="basic.html">HTML</a></li>
            <li><a href="css.html">CSS</a></li>
          </ul>
          <li class="dropdown">
            <a href="#" class="dropdown-toggle" data-toggle="dropdown">更多<span class="caret"></span></a>
            <ul class="dropdown-menu">
              <li><a href="bootstrap.html">Bootstrap</a></li>
              <li><a href="js.html">JavaScript</a></li>
              <li><a href="jquery.html">jQuery</a></li>
            </ul>
          </li>
        </div>
      </div>
    </div>
  </div>
<!-- /nav - collapse -->

<!-- 其他代码 -->
<!-- Javascript 之前 -->
<!-- 在 bootstrap.min.js 之前放入 jQuery; 并添加自定义 jquery -->
  <script src="asset/jquery-3.3.1.min.js"></script>
  <script src="asset/bootstrap.min.js"></script>
</body>
</html>
```





![](img/f70659d57873500d1a13fffa6bbe945a_49_0.png)

图 3.15: 导航栏 (navbar)

# 第 4 章

### JavaScript

## 引言

- JavaScript 是一种动态语言，用于设计客户端网页页面。
- 它是一种区分大小写的语言。
- 它是一门无类型语言，即变量可以持有任何类型的值。
- // 用于编写注释。
- ; 用于行结束。
- JavaScript 代码应该添加在末尾，即紧跟在 `</body>` 标签之前。
- 最好将 JavaScript 代码写在单独的文件中，如下一节所示。

### 第一段代码

JavaScript 代码可以写在‘html’ 文件中，也可以像本节所示，写在单独的‘JavaScript 文件 (.js)’中，

### 在 HTML 文件中使用 JavaScript

在 HTML 文件中，JavaScript 代码可以写在‘script’ 标签内部，如下所示代码的第 11-13 行所示。该代码将在网页上打印“Hello World from JavaScript!”。在浏览器中打开‘js.html’即可查看该消息。

```
<!-- js.html -->
<!DOCTYPE html>
<html
<head>
<title>JavaScript</title>
</head>
<body>
<script type="text/javascript">
document.write("Hello World from JavaScript!<br>");
</script>
</body>
</html>
```

以下是 HTML 页面上的输出。

### 4.3. 关键字、数据类型、变量和运算符

### 在单独文件中使用 JavaScript

- JavaScript 代码保存在文件 'my_javascript.js' 中，该文件位于文件夹 'asset/js' 内。注意，这里没有使用‘script 标签’。

```
// asset/my/javascript.js
document.write('Hello World from JavaScript!<br>');
// 接下来我们需要如下所示在 HTML 文件中导入 .js 文件，
<!-- js.html -->
<!DOCTYPE html>
<html>
<head>
 <title>JavaScript</title>
</head>
<body>
 <!-- 在此处导入 JavaScript 文件 -->
 <script src="asset/my/javascript.js"></script>
</body>
</html>
```

**注意：** 我们将在本教程中使用第二种方法。

### 关键字、数据类型、变量和运算符

### 关键字

- 下面是 JavaScript 中的保留关键字，它们不能作为‘变量’和‘函数’名称等。

### 表 4.1; 关键字列表

| abstract | boolean | break | byte |
| --- | --- | --- | --- |
| case | catch | char | class |
| const | continue | debugger | default |
| delete | | double | else |
| enum | export | extends | false |
| final | float | for | function |
| goto | | implements | import |
| in | int | interface | long |
| native | | null | package |
| private | protected | public | return |
| short | static | super | switch |
| this | throw | throws | transient |
| true | try | typeof | var |
| void | volatile | while | with |

### 数据类型

JavaScript 有三种数据类型：

- 数字 (Numbers)：123, 32, 32
- 字符串 (Strings):"Meher", "Krishna Patel", "123"
- 布尔值 (Boolean)：true, false

注意：所有数字都被视为‘浮点数’。

### 变量

可以使用关键字 'var' 定义变量。此外，JavaScript 是一门无类型语言，即变量可以持有任何类型的值。

- 在下方的 HTML 中，id 为 'p_name' 的 'p' 标签定义在第 10 行。这将用于使用 JavaScript 写入一些文本，

```
<!-- js.html -->
<!DOCTYPE html>
<html>
<head>
<title>JavaScript</title>
</head>
<body>
<p id='p_name'></p>
<!-- 在此处导入 JavaScript 文件 -- -->
<script src="asset/js/my_javascript.js"></script>
</body>
</html>
```

在第 9-10 行分别定义了两个类型为 'string' 和 'float' 的变量。然后使用 'getElementById' 定位 id 为 'p_name' 的标签，并如第 11 行所示插入文本。最后，使用 '+' 号如第 11 行所示对值进行拼接。

```
// asset/js/my_javascript

// 在网页上打印消息
document.write("Hello World from JavaScript!<br>");

// 变量示例
var var_name = "Meher";
var age = 20;
document.getElementById('p_name').innerHTML = "Hello " + var_name + "<br>Age : " + age;
// 以下是上述代码的输出。注意消息 'Hello world from JavaScript' 被添加到了
// 因为 'JavaScript' 文件是在末尾导入的。
```

### 4.3. 关键字、数据类型、变量和运算符

警告：如果在‘结束的 head 标签’和‘开始 body 标签’之间导入‘JavaScript’文件，那么“Hello Meher...” 消息将不会显示，因为 'JavaScript' 将在页面加载之前执行；且 JavaScript 找不到 'p_name'。

注意：所有的 JavaScript 代码都将添加到以下代码之后，因此可以使用 'prompt' 从用户处读取值。

```
//prompt
var x = prompt("enter a number");
document.write("2*" + x + " = " + x + "<br>");
```

Hello
Meher
Age : 20
Hello World from JavaScript!

注意：'+' 可以如上面的示例所示组合输出。其中一些运算符的用法将在第 4.4 节显示。

### 运算符

### 算术运算符

- +
- *
- /
- % 取模，即余数
- ++ (递增)
- - (递减)

### 赋值运算符

- +=
- -=
- *=
- /=

### 比较运算符

- == (仅比较值)
- === (同时比较值和类型)
- !=
- >
- >=
- <=

### 条件运算符

- ?: (a > b) ? a : b

### 逻辑运算符

- && (逻辑与)
- || (逻辑或)
- ! (逻辑非)

### 位运算符运算符

- & (位与)
- | (位或)
- ^ (位异或)
- ~ (位反)

### 字符串转数字

'Number' 用于将字符串转换为数字。

```
// 字符串转数字
document.write(Number("3.4")); // 字符串转数字
2 + Number("3.4")
5.4
```

以下是上述代码的输出，字符串或浮点值可以使用 'parseInt' 转换为整数。

### 转换为整数

```
// 整数转换
document.write(parseInt("3.4")); // 整数转换
2 + parseInt("3.4") // 字符串到 int
5
```

代码：
'parseFloat' 或 'Number' 可用于转换浮点值。

### Math

'Math' 库包含如下所示的函数：

```
// math
document.write("Math.PI = =", Math.PI, "<br>");
document.write("Math.floor(3.14) = =", Math.floor(3.14), "<br>"); // 向取
document.write("Math.ceil(3.14) = =", Math.ceil(3.14), "<br>"); // 向上取
document.write("Math.random() = =", Math.floor(Math.random()*20), "<br>"); // 随机数：16
```

以下是一些'字符串样式':

### 字符串

```
// 字符串
document.write("meher".toUpperCase() + "<br>"); // 大写
w = "Krishna"
document.write(w.toLowerCase(), "<br>"); // 小写(w)
document.write(w.small(), "<br>"); // 小字体
document.write(w.strike(), "<br>"); // 粗体
document.write(w.fontsize("5em"), "<br>"); // 划线
document.write(w.link("http://javascript.info"), "<br>"); // 链接
document.write(w.fontcolor("red").fontsize("12em"), "<br>"); // 多重
```

输出见图4.1。

### 数组

在 JavaScript 中，数组可以如下所示存储不同类型的值

```
// 数组
arr = [15, 30, "Meher"]
for(a in arr) {
  document.write(arr[a], " ");
  document.write("<br>");
}
document.write(arr.pop(), "<br>"); // 移除最后一个元素
arr.push("Krishna"); // 将元素添加到末尾
document.write(arr.pop());
document.write("<br>");
document.write("length of array: ", arr.length, "<br>");
```

以下是上述代码的输出，

| 15 30 |
| Meher |
| Meher |
| Krishna |
| Length of array: 2 |

### 控制结构、循环和函数

### If-else

在下面的代码中，对变量 'age' 检查了三个条件；并打印相应的消息。（（继续见下一页）

```
// asset/js/my_javascript
if-else {
  age = 10;
  if (age > 3 && age < 6) {
    document.write("Age: " + age + "<br> go to kindergarten</br>");
  } else if (age >= 6 && age < 8) {
    document.write("Age: " + age + "<br> go to school</br>");
  } else {
    document.write("Age: " + age + "<br> go to college</br>");
  }
}
```





### 4.4. 控制结构、循环与函数
（接上页内容）

```javascript
}
document.write("<br>");
```

- 由于 age 等于 10，满足了 else if 语句，我们将得到下面的输出：

Age : 10 go to school

### Switch-case-default

下面是 Switch-case-default 语句的示例：

```javascript
//asset/js/my_javascript
// Grade_A: Very good grade!
var grade = 'A';
document.write("Grade " + grade + ": ");
switch(grade) {
    case 'A':
        document.write("Very good grade!");
        break;
    case 'B':
        document.write("Good grade!");
        break;
    default: // 如果 grade 既不是 'A' 也不是 'B'
        document.write("Enter correct grade");
}
document.write("<br>");
```

- 下是上述代码的输出：

### For 循环

以下代码打印从 5-0 的值：

```javascript
// For loop
for (i=5;i>0;i--) {
    document.write(i + " \ ");
}
```

```javascript
document.write("<br>");
```

- 下是输出：

### While 循环

以下代码打印从 0-4 的值：

```javascript
// While loop
x=0;
while (x < 5) {
    document.write(x + " \ ");
    x++;
}
document.write("<br>");
```

## 第 4 章 JavaScript do-while 循环

以下代码打印从 0-2 的值：

```javascript
// do-while
x=0;
do {
  document.write(x + " ");
  x++;
} while(x < 3);
document.write('<br>');
```

下面是输出：

### For-in 循环

'for-in' 循环可以用于遍历数组，如下所示：

```javascript
// for-in loop
arr = [10, 12, 31]; // array
for (a in arr) {
  document.write(arr[a] + " ");
}
document.write('<br>');
```

### Continue 和 break

Continue 和 break 语句用于 'loop' 语句内部。

- 如果满足条件，continue 语句将跳过当前循环并进入下一次迭代。在下面的代码中，输出中将不会打印 3。

```javascript
// continue
for (i=5; i>=0; i--) {
  if (i==3) { // 跳过 3
    continue;
  }
  document.write(i + " ");
}
document.write('<br>');
```

下面是输出，其中 3 没有被打印出来。

> 如果满足条件，'Break' 语句将退出循环。在下面的代码中，循环将在 'i=3' 时终止，因此只会打印 5 和 4：

```javascript
// break
for (i=5; i>=0; i--) {
  if (i==3) { // 当 i=3 时退出循环
    break;
  }
  document.write(i + " ");
}
document.write('<br>');
```

下面是上述代码的输出：

### 4.5. 事件处理

### 函数

在下面的代码中，定义了函数 'add2Num'，它可以两个两个相加并返回结果。

```javascript
// function
function add2Num(num1, num2) { // 函数定义
  return num1 + num2;
}
sum = add2Num(2, 3); // 调用函数
document.write("2 + 3 = " + sum);
document.write("<br>");
```

下面是输出：

### 事件处理

JavaScript 'event handling' 的主要用途之一。“鼠标点击”和“在键盘上按键”都是“事件”的示例。通过 JavaScript 的帮助，我们可以在事件发生时执行某些操作，如下所示。

- 'alert' 用于在“弹出”窗口中显示消息。

```javascript
function alertMessage(message) {
  alert(message);
}
```

- 在第 13 行中，触发 'onclick' 事件时，弹出窗口中显示 "Hello"。注意这里使用了 "JavaScript:void(0)"，它不会刷新页面。
- 第 15 行与第 13 行不同，没有使用 "JavaScript:void(0)"，因此页面将刷新。
- 第 17 行调用函数 'alertMessage' 来显示消息，该函数在上面的代码中定义。
- 第 19-25 行使用了不同的事件，即 'onmouseover''onmouseleave''onmouseup' 和 'onmousedown'文本字符串的颜色会根据这些操作而改变。

```html
<!-- js.html -->
<!DOCTYPE html>
<html>
<head>
  <a href="javascript:void(0)" onclick="alert('Hello')">点击这里 <!-- (第 13 行) -->
  <a href="index.html" onclick="alert('Hello')">点击这里 <!-- (第 15 行，刷新页面) -->
  <button onclick="alertMessage('Hello')">点击这里</button> <!-- (第 17 行) -->
  <p onmouseover="this.style.color='red'" onmouseleave="this.style.color='black'">鼠标悬入/离开改变颜色</p>
  <p onmouseup="this.style.color='blue'" onmousedown="this.style.color='green'">鼠标按下/松开改变颜色</p>
</body>
</html>
```
*(注：由于原文提供的 HTML 代码不完整，此处根据描述还原了逻辑结构)*





## 第 5 章 jQuery

```html
<span class="label label-primary" id="l_primary">主要</span>

<span class="label label-success" id="l_success">成功</span>

<span class="label label-info" id="l_info">信息</span>

<span class="label label-warning" id="l_warning">警告</span>

<span class="label label-danger" id="l_danger">危险</span>

<!-- Javascript -->
<!-- 引入 jquery.js/jquery-3.1.min.js，然后添加自定义 jquery -->
<script src="asset/js/bootstrap.min.js"></script>


<script type="text/javascript">
$(function() {
  $("#l_default").hide(1000); // 使用 # 操作符在 3000 ms 后隐藏 id = 'l_default'
});
</script>

</body>
</html>
```

![](img/f70659d57873500d1a13fffa6bbe945a_64_0.png)

注意："#" 用于选择 'id'；而 "." 用于选择 'class'。

- 在下方的代码中，移除了“Danger（危险）”标签；并为其余标签设置了 "opacity=0.5"。在这里，'.label' 选择了所有包含 'label' 名称的类。由于所有条目都具有名为 'label' 的类，因此它们都被选中并淡出到 'opacity=0.5$，如图 5.3 所示。

```html
<!-- jQuery -->
<!DOCTYPE html>
<html>
<head>
  <title>jQuery</title>
  <!-- CSS -->
  <link href="asset/css/bootstrap.min.css" rel="stylesheet">
  <!-- 在下方添加自定义样式 -->
</head>
<body>
  <div class="umbotron">
    <div class="col-md-offset-4 container">
      <h1>jQuery</h1>
    </div>
  </div>

<span class="label label-default" id="l_default">默认</span>
<span class="label label-primary" id="l_primary">主要</span>
<span class="label label-success" id="l_success">成功</span>
```

## 5.2 jQuery 示例
（接上页）

```html
<span class="label label-info" id="l_info">信息</span>
<span class="label label-warning" id="l_warning">警告</span>
<span class="label label-danger" id="l_danger">危险</span>
```

```html
<!-- Javascript -->
<!-- 将 jquery.js 放在 bootstrap.min.js 之前；然后添加自定义 query -->
<script src="asset/js/jquery-3.1.min.js"></script>
<script src="asset/js/bootstrap.min.js"></script>
```

```javascript
<script type="text/javascript">
$(function() {
  $("#l_default").hide(1000); // 使用 # 操作符在 3000 ms 后隐藏 id = 'l_default'
  $(".label-danger").hide(); // 使用 . 操作符隐藏类 = 'label-danger'
  $(".label").css({"opacity": 0.5}); // 为所有名为 'label' 的类添加透明度
});
</script>
</body>

</html>
```

![](img/f70659d57873500d1a13fffa6bbe945a_65_0.png)

图 5: 淡出的标签

### 在独立文件中编写 jQuery

将 jQuery 写在独立文件中会更好，这样代码更易于管理。

- 为此，将第一个代码写在独立文件 'my_jquery.js' 中，如下所示，

注意：'html' 用于如下方列表第 5 行所示，更改 'id' 的内容（见图 5.4）

```javascript
// asset/js/my_jquery.js
$(function() {
  $("#l_default").hide(); // 使用 # 操作符隐藏 id = 'l_default'
  $(".label-danger").html("Shark is dangerous"); // 使用 "html" 修改内容
});
```

- 接下来，将此文件导入到 'html' 中，如代码第 35 行所示，

```html
<!-- jquery.jquery.html -->
<!DOCTYPE html>
<html>
<head>
<title>jQuery</title>
<!-- CSS -- -->
<link href="asset/css/bootstrap.min.css" rel="stylesheet">
<!-- 在下方添加自定义样式 ---- -->
```

```html
</head>
<body>
<div class="jumbotron">
<div class="col-md-offset-4 container">
<h1><b>>jquery</b></h1>
</div>
</div>
<span class="label label-lg label-default" id="l_default">默认</span>
<span class="label label-lg label-primary" id="l_primary">主要</span>
<span class="label label-lg label-success" id="l_success">成功</span>
<span class="label label-lg label-info" id="l_info">信息</span>
<span class="label label-lg label-warning" id="l_warning">警告</span>
<span class="label label-lg label-danger" id="l_danger">危险</span>

<!-- jQuery 放在 bootstrap.min.js 之前，然后添加自定义 -->
<script src="asset/js/jquery-3.1.min.js"></script>
<script src="asset/js/bootstrap.min.js"></script>
<script src="asset/js/my_jquery.js"></script>
</body>
</html>
```

![](img/f70659d57873500d1a13fffa6bbe945a_66_0.png)

图 5.4: 使用 ‘html’ 修改后的代码

### 获取用户输入

以下是我们在本节将使用的完整 html 代码，

列表 5.1: 完整代码

```html
<!-- jQuery.html -->
<!DOCTYPE html>
<html>
<head>
<title>jquery</title>
<!-- CSS -- -->
<link href="asset/css/bootstrap.min.css" rel="stylesheet">
<!-- 添加自定义样式 -->
</head>
<body>
<div class="jumbotron">
<div class="col-md-offset-4 container">
<h1><b>>jquery</b></h1>
</div>
</div>
</body>
</html>
```

### 5.2 jQuery 示例（接上页）

```html
<span class="label label-default" id="l_default">默认</span>
<span class="label label-primary" id="l_primary">主要</span>
<span class="label label-success" id="l_success">成功</span>
<span class="label label-info" id="l_info">信息</span>
<span class="label label-warning" id="l_warning">警告</span>
<span class="label label-danger" id="l_danger">危险</span>

```



```javascript
$('#' + labelId).toggle(); // 切换存储在 'label_id' 中的 id 标签
);
);
```

### 选择器

在本节中，我们将使用以下内容来理解 HTML 的各种选择器组合，这些组合被总结在表 5.1 中。

```html
<!DOCTYPE html>
<head>
<title>查询选择器</title>
</head>
<body>
<p>查询选择器</p>
<p class="foo">带有类的段落。</p>
<p><span>带有 span 的段落。<span></</span></span></p>
<p id="bar">带有 ID 的段落。<span class="foo">带有类且在带有 id 的段落内的 span。<span></</span></span></p>
<div>
<p id="my_para">div 内部（带有自定义 id）的段落</p>
<p id="my_para_2"><span>div 内部（带有自定义 id）的段落内部的 span</span></p>
</div>

<!-- Javascript -->
<script src="...asset/js/jquery-3.3.1.min.js"></script>
```

注意：

- 按 'ctrl+shift+k'（或转到 工具->开发者->Web 控制台）在 Firefox 中打开 Web 控制台，点击 'console' 那里输入 "jQuery" 命令。
- 在 'Chrome' 中按 'ctrl-shift+J'（或转到 工具->Javascript 控制台），在那里输入 jQuery 命令。
- 在本教程中，显示的是 "Firefox" 的输出。

### 选择元素

选择元素

HTML 元素，例如 div, p, span 和 table 等，可以通过如下面的代码所示用引号编写它们来选择。

- 在这里，('$') 是命令，其下方的行是输出结果。
- 输出显示了“选中的元素”以及所选中元素的总数，即 ‘length: 6’。
- 如果我们把光标置于其中一个输出上，它将高亮 html 中对应的元素，如图 5.8 所示。

## 第 5 章. jQuery

```javascript
$('p')
[..]
0: <p>
1: <p class="foo">
2: <p>
3: <p id="bar">
4: <p my-id="my_para">
5: <p my-id="my_para_2">
6: { length: 6 }
```

![](img/f70659d57873500d1a13fffa6bbe945a_70_0.png)

- 同样，我们可以选择 'div' 元素

```javascript
$('div')
[..]
0: <div>
length: 1
```

### 选择类

可以使用 '. ' 操作符选择类。在下方的代码中，选了 'foo'。

```javascript
$('.foo')
[..]
0: <p class="foo">
1: <span class="foo"></span>
length: 2
```

### 选择 ID

可以使用 '#bar' 操作符选择 ID。在下方的代码中，选择了 'bar'。

```javascript
$('#bar')
[..]
0: <p id="bar">
length: 1
```

### 组合选择器

我们可以使用 '. ' 操作符选择具有特定类名的元素，如下方的代码所示。在这里，选择了类为 'foo' 的元素 'span'。

### 5.3. 选择器

```javascript
$('span.foo')
[]
0: <span class="foo"></span>
length: 1
```

### 多重选择器

使用 '*' 选择不同类型的元素。在下方的代码中，选择了“带有 id 'bar' 的段落”和“带有类 'foo' 的元素”。

```javascript
$('*bar .foo')
[]
0: <span class="foo"></span>
1: <span id="bar"></span>
2: <span class="foo"></span>
length: 3
```

### 选择后代元素

选择 'p' 内部的 'span'（在 'span' 和 'p' 之间使用空格）。

```javascript
$('p span')
[]
0: <span>
1: <span class="foo"></span>
2: <span></span>
length: 3
```

### 选择子元素

'>' 用于选择元素的子元素。

```javascript
$('div span')
[]
length: 0
```

> 注意：'div' 内部有一个元素，但它的路径是 'div->span'，因此 'span' 是 'p' 的子元素（而不是 'div' 的子元素）。但 'span' 是 'div' 的后代元素，因此可以使用空格访问，

```javascript
$('div span')
[]
0: <span></span>
length: 1
```

### 属性选择器

可以如下所示选择自定义属性（继续见下一页）

```javascript
$('[my-id = my_para]')
[]
0: <p my-id="my_para"></>
length: 1
```

## 第 5 章. jQuery

```javascript
$('p[my-id != my_para]') // 选择 my-id != my_para 的 p
[...]
<p>
0:
1: <p class="foo">
2: <p>
3: <p id="bar">
4: <p my-id="my_para_2">
   length: 5

$('p[class = 'foo'])
[...]
0: <p class="foo">
length: 1
```

### 过滤器

各种过滤器选项（例如 first, last 等）可以使用 ':' 如下所示：

```javascript
(':first') // 选择第一个元素
[...]
0: <p>

(':last') // 选择最后一个元素
[...]
0: <p my-id="my_para_2">
   length: 1

(':not('foo)') // 选择不具有类 'foo' 的 p
[...]
0: <p>
1: <p>
2: <p id="bar">
3: <p my-id="my_para_2">
   length: 5

(':has(span)') // 选择内部包含 'span' 的 p
[...]
0: <p>
1
length: 3

(':hidden') // 隐藏的 'p'
[...]
length: 0

(':visible') // 可见的的 'p'
[...]
0: <p>
1: <p class="foo">
2: <p>
3: <p id="bar">
4: <p my-id="my_para">
5: <p my-id="my_para_2">
   length: 6

(':contains(class)') // 选择包含该类的段落
```

```javascript
<p class="foo">
0: <span id="bar"></span>
length: 2
$('').filter(
```

表 5.1: 选择器

| 命令 | 说明 | 示例 |
| --- | --- | --- |
| ${(elementName) | 选择标签 (p, body, table) | $('p'), $('body') |
| $('.className') | 选择带有类的元素 | $(".foo") |
| ${(elementName.className) | 选择带有类的元素 | $("span.foo") |
| $(selector1,selector2) | 选择 selector1 和 selector2 | $('pbar, foo') |
| $(selector1 selector2) | 选择 selector1 内部的 selector2 | $('p span') |
| $(selector1>selector2) | 选择作为 selector1 子元素的 selector2 | $(div>span) |
| ${(attribute = someName) | 选择带有属性 someName | \$(['my-id = my_para']) |
| \$(attr(attribute = someName)) | 选择带有属性 someName 的 p | $('my-id = my_para']) |

表 5.2: 操作

| | | | |
|---|---|---|---|
| hide() | hide(speed) | fadeIn(speed) | fadeOut(speed) |
| show() | show(speed) | slideDown(speed) | slideToggle(speed) |
| slideUp(speed) | toggle() | toggle(speed) | toggle(switch) |

表 5.3: 事件处理

| 事件 | | | |
|---|---|---|---|
| click | keydown | keypress | key |
| mousedown | mouseover | | |

