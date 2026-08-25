
# CSS：快速启动指南——高效网页设计（CSS、HTML、JavaScript、编程）

## 引言

CSS，即层叠样式表（Cascading Style Sheets）的缩写，是所有设计语言中最简单的一种，也是实现最高效网页设计所必需的语言。CSS 将处理网页的外观和感觉；你可以设置文本颜色、字体样式、段落间距、网页列的布局和大小、背景所需的颜色和图像，以及所有其他布局和设计变化，以使你的网站在不同屏幕尺寸和设备上正常工作。

CSS 非常容易理解和学习，它让你能够强有力地控制 HTML 文档的呈现方式。它通常与两种更流行的标记语言（HTML 或 XHTML）结合使用，为你提供制作设计精良网站所需的所有工具。

本书将带你了解 CSS 可以控制的网页设计的所有主要方面，并附有示例代码。我希望，在阅读完本书后，你能对 CSS 的易用性以及它能产生的惊人效果有所了解。

## 第 1 章：使用 CSS 的优势

CSS 相比其他类似程序有许多优势，包括：

- **节省时间**——使用 CSS，你可以编写一次样式表，然后在多个不同的 HTML 页面中使用完全相同的样式表。每个 HTML 元素都可以拥有自己独立的样式，并可应用于多个网页。
- **更快的页面加载速度**——使用 CSS 时，无需每次都编写 HTML 标签属性。相反，你可以为某个标签编写一条规则，然后将其应用于该标签的每次出现。更少的代码意味着更快的加载速度。
- **易于维护**——当你想要进行全局更改时，只需更改样式；所有使用该样式的网页中与该样式相关的每个元素都将被更改。
- **在样式上优于 HTML**——CSS 提供了比 HTML 更广泛的属性访问范围，因此你的 HTML 页面看起来会比使用 HTML 属性更好。
- **兼容多种设备**——你的样式表允许内容针对多种设备类型进行优化。例如，使用相同的 HTML 文档，你可以为打印、PDA 或移动设备生成不同的网站版本。
- **全球网络标准**——越来越多地推荐使用 CSS 而非 HTML，所以现在是开始学习并将其应用于所有 HTML 页面的好时机。这样，它们将与未来的浏览器兼容。
- **离线浏览**——CSS 能够通过离线缓存本地存储应用程序。这意味着你将更容易查看离线网站，并且由于缓存，它们加载速度更快，网站性能更好。

如你所见，CSS 相比 HTML 提供了大量优势，尤其是它现在已成为公认的标准。随着 CSS 越来越流行，现在正是开始学习的最佳时机。

闲话少说，让我们深入探讨用于网页设计的 CSS 元素。

在进一步讲解之前，我必须说明，本书中使用的一些示例代码归功于 `www.tutorialspoint.com`。

## 第 2 章：CSS 模块

CSS 模块采用了现有的 CSS 规范以及一些扩展功能，包括：

- 选择器
- 盒模型
- 图像值
- 背景和边框
- 替换内容
- 文本效果
- 2D 和 3D 变换
- 动画
- 多列布局
- 用户界面

CSS 由一系列样式规则组成，这些规则由浏览器解释后应用于文档的正确元素。样式规则分为三部分：

- **选择器**——这是应用样式的 HTML 标签。这些标签的示例有 `<h1>` 或 `<table>`。
- **属性**——属性是 HTML 标签属性的类型。简单来说，所有 HTML 属性都转换为 CSS 属性，例如 `color`、`border` 等。
- **值**——每个属性被赋予一个或多个值。例如，颜色属性的值可以是红色或 `#F2F2F2` 等。

CSS 样式规则的语法为：

```css
selector { property: value }
```

例如，你可以为表格定义边框：

```css
table{ border :1px solid #C00; }
```

在这个例子中，`table` 是一个选择器，`border` 是一个属性。它被赋予了 `1px solid #C00` 的值。

选择器可以通过多种方式定义，下面我们逐一介绍。

### 类型选择器

上面你已经看到了类型选择器的例子，但让我们再看一个——为所有一级标题添加颜色的方法：

```css
h1 {
    color: #36CFFF;
}
```

### 通用选择器

这个选择器不是选择与特定类型相关的元素，而是直接匹配元素类型的名称。例如：

```css
* {
    color: #000000;
}
```

在这个例子中，所有元素的内容都变成了黑色。

### 后代选择器

假设你想给某个特定元素设置样式，但仅当它位于另一个特定元素内部时。在下面的例子中，我们将样式规则应用于 `<em>` 元素，但仅当它位于 `<ul>` 标签之外时：

```css
ul em {
    color: #000000;
}
```

### 类选择器

类选择器允许你使用元素的 `class` 属性来定义样式规则。所有属于该特定类的元素都会按照定义的规则进行格式化：

```css
.black {
    color: #000000;
}
```

在这个例子中，规则将所有 `class` 属性为 `black` 的元素内容变为黑色。如果你愿意，还可以更进一步：

```css
h1.black {
    color: #000000;
}
```

现在你指定了只有 `<h1>` 元素中 `class` 属性为 `black` 的内容才会变为黑色。

不过，一个元素并不限于只能使用一个类选择器。请看这个例子：

```html
<p class="center bold">
该段落的样式由 Bold 和 Center 这两个类定义。
</p>
```

### ID 选择器

样式规则可以定义在元素的 `id` 属性上，一旦定义了规则，它将格式化所有具有指定 `id` 属性的元素：

```css
#black {
    color: #000000;
}
```

这条规则会将所有 `id` 属性为 `black` 的元素内容变为黑色。如果你愿意，可以更具体一些，例如：

```css
h1#black {
    color: #000000;
}
```

这条规则仅当 `<h1>` 元素的 `id` 属性设置为 `black` 时，才将其内容变为黑色。

ID 选择器的真正威力在于它们作为后代选择器的基础时体现出来，例如：

```css
#black h2 {
    color: #000000;
}
```

这里可以看到，所有二级标题只有在位于 `id` 属性设置为 `black` 的标签内部时，才会变为黑色。

### 子选择器

子选择器与后代选择器类似，但功能不同。请看这个例子：

```css
body > p {
    color: #000000;
}
```

这将使段落变为黑色，但仅当它们是 `<body>` 元素的直接子元素时。其他位于其他元素（如 `<td>` 或 `<div>`）内部的段落不会改变。

### 属性选择器

样式也可以应用于具有特定属性的 HTML 元素。请看下面的例子；你可以看到样式规则将匹配所有 `type` 属性值为 `text` 的 `input` 元素：

```css
input[type="text"] {
    color: #000000;
}
```

使用这种方法的优点是 `<input type="submit" />` 不会受到影响，颜色变化仅应用于特定的文本字段。

以下是属性选择器的规则：

- `p[lang]` - 选择所有具有 `lang` 属性的段落元素
- `p[lang="fr"]` – 选择所有 `lang` 属性精确值为 `"fr"` 的段落元素
- `p[lang~="fr"]` – 选择所有 `lang` 属性包含 `"fr"` 的段落元素
- `p[lang|="en"]` – 选择所有 `lang` 属性精确值为 `"en"` 或以 `"en-"` 开头的段落元素

### 多重样式规则

可以为单个元素定义多条样式规则，这些规则应组合成一个块，包含多个属性及其对应的值，如下例所示：

```css
h1 {
    color: #36C;
    font-weight: normal;
    letter-spacing: .4em;
    margin-bottom: 1em;
    text-transform: lowercase;
}
```

在这个例子中，你可以看到每对属性和值之间用分号（`;`）分隔。它们可以放在一行，也可以分散在多行，但为了便于阅读，我们将其放在单独的行上。

### 分组选择器

样式可以应用于多个选择器。你只需记住用逗号分隔每个选择器，如下例所示：

```css
h1, h2, h3 {
    color: #36C;
    font-weight: normal;
    letter-spacing: .4em;
    margin-bottom: 1em;
    text-transform: lowercase;
}
```

这条样式规则将应用于所有 `h1`、`h2` 和 `h3` 元素。列表中的顺序无关紧要，因为选择器中的所有元素都将应用这些声明。从下面的例子可以看出，可以组合多个类选择器：

```css
#content, #footer, #supplement {
    position: absolute;
    left: 510px;
    width: 200px;
}
```

## 第 3 章：包含方式

你有四种方法将样式与 HTML 文档关联起来，其中最常用的是内联 CSS 和外部 CSS 方法。

### 嵌入式 CSS

CSS 规则可以通过使用 `<style>` 元素放入 HTML 文档中。该标签位于 `<head>…</head>` 标签内，使用此语法定义的规则适用于所有可用元素。下面的例子展示了一个嵌入式 CSS 样式元素：

```html
<!DOCTYPE html>
<html>
   <head>
      <style type="text/css" media="all">
         body {
            background-color: linen;
         }
         h1 {
            color: maroon;
            margin-left: 40px;
         }
      </style>
   </head>   
   <body>
      <h1>这是一个标题</h1>
      <p>这是一个段落。</p>
   </body>
</html>
```

#### 属性

与 `<style>` 元素相关的常见属性如下表所示：

| 属性 | 值 | 描述 |
| --- | --- | --- |
| `type` | `text/css` | 该属性将样式表的语言指定为 MIME 内容类型，是必需属性 |
| `media` | `screen` `tty` `tv` `projection` `handheld` `print` `braille` `aural` `all` | 指定文档将在哪种设备上显示。默认值为 `all`，属于可选属性 |

### 内联 CSS

你也可以使用任何 HTML 元素的 `style` 属性来定义规则。这些特定规则仅应用于该特定元素。通用语法为：

```html
<element style="...样式规则....">
```

#### 属性

`style` 属性的值由不同的样式声明混合而成，每个声明之间用分号分隔。以下示例基于通用语法：

```html
<html>
   <head>
   </head>
   <body>
      <h1 style="color:#36C;"> 这是内联 CSS </h1>
   </body>
</html>
```

### 外部 CSS——`<link>` 元素

你可以使用 `<link>` 元素将外部样式表包含到 HTML 文档中。外部样式表是独立的文本文件，扩展名为 `.css`。你将在该文件中定义所有样式规则，然后可以通过 `<link>` 元素将其添加到任何 HTML 文档中。通用语法为：

```html
<head>
   <link type="text/css" href="..." media="..." />
</head>
```

#### 属性

与 `<style>` 元素相关的属性如下：

| 属性 | 值 | 描述 |
| --- | --- | --- |
| `type` | `text/css` | 将样式表的语言指定为 MIME 内容类型，是必需属性 |
| `href` | `URL` | 指定样式表包含样式规则，也是必需属性 |
| `media` | `screen` `tty` `tv` `projection` `handheld` `print` `braille` `aural` `all` | 指定文档可以在哪些设备上显示，是可选属性。默认值为 `all` |

例如，考虑一个名为 `mystyle.css` 的样式表，其中包含以下规则：

```css
h1, h2, h3 {
   color: #36C;
   font-weight: normal;
   letter-spacing: .4em;
   margin-bottom: 1em;
   text-transform: lowercase;
}
```

现在，使用以下代码，你可以将这个文件添加到任何 HTML 文档中：

```html
<head>
   <link type = "text/css" href = "mystyle.css" media = " all" />
</head>
```

### 导入 CSS——`@import` 规则

`@import` 规则用于导入外部样式表，其方式与 `<link>` 元素类似。通用语法如下：

```html
<head>
   <@import "URL";
</head>
```

在此语法中，`URL` 用作包含样式规则的特定样式表的 URL。另一种写法是：

```html
<head>
   <@import url("URL");
</head>
```

以下示例展示了如何将样式表导入 HTML 文档：

```html
<head>
   @import "mystyle.css";
</head>
```

### 覆盖 CSS 规则

到目前为止，我们已经了解了在 HTML 文档中包含样式表的四种不同方式。现在我们来看看如何覆盖任何样式表规则：

- 内联样式表拥有最高优先级，包括覆盖外部样式表或 `<style> … </style>` 标签中定义的任何规则。
- 任何 `<style> … </style>` 标签都会覆盖外部样式表文件。
- 外部样式表规则的优先级最低，仅当内联样式或 `<style> … </style>` 标签未应用时才会生效。

### 如何处理旧版浏览器

有不少较旧的浏览器不支持 CSS，因此当你在 HTML 文档中编写嵌入式 CSS 时，请务必小心。以下示例展示了如何使用注释标签来对旧版浏览器隐藏 CSS：

```html
<style type="text/css">
   <!--
      body, td {
         color: blue;
      }
   -->
</style>
```

### CSS 注释

有时你需要在样式表块中添加额外的注释，但注释样式表的任何部分都非常容易。你只需将注释放在 `/*…. 这是样式表中的注释 …. */` 中即可。

你也可以使用 `/*…. */` 来注释多行块，就像在 C 或 C++ 语言中那样。

例如：

```html
<!DOCTYPE html>
<html>
   <head>
      <style>
         p {
            color: red;
            /* 单行注释 */
            text-align: center;
         }
         /* 多行注释 */
      </style>
   </head>
   <body>
      <p>Hello World!</p>
   </body>
</html>
```

这将在屏幕上显示“Hello, World!”。

## 第 4 章：度量单位

CSS 支持多种不同的度量单位，包括相对度量（如百分比）和绝对单位（如厘米、英寸、点等）。当你在样式规则中指定度量值时，需要使用这些值，例如 `border = “1px solid red”`。

下表列出了 CSS 度量单位及其示例：

| 单位 | 描述 | 示例 |
| --- | --- | --- |
| `%` | 将度量定义为相对于其他值的百分比。典型情况是相对于包含元素。 | `p {font-size: 16pt; line-height: 125%;}` |
| `cm` | 以厘米为单位定义度量 | `div {margin-bottom: 2cm;}` |
| `em` | 以 em 空格为单位的字体高度相对度量。一个 em 单位相当于任何给定字体的大小，因此如果你为字体分配 12 pt，每个 em 单位就是 12 pt。这意味着 2em 等于 24 pt。 | `p {letter-spacing: 7em;}` |
| `ex` | 定义相对于字体 x 高度的度量。x 高度由指定字体中小写字母 x 的高度决定。 | `p {font-size: 24pt; line-height: 3ex;}` |
| `in` | 以英寸为单位定义度量 | `p {word-spacing: .15in;}` |
| `mm` | 以毫米为单位定义度量 | `p {word-spacing: 15mm;}` |
| `pc` | 以派卡为单位定义度量，1 派卡等于 12 点。这意味着 1 英寸等于 6 派卡。 | `p {font-size: 20pc;}` |
| `pt` | 以点为单位定义度量，1 点定义为 1/72 英寸 | `body {font-size: 18pt;}` |
| `px` | 以屏幕像素为单位定义度量 | `p {padding: 25px;}` |
| `vh` | 视口高度的 1% | `h2 { font-size: 3.0vh; }` |
| `vw` | 视口宽度的 1% | `h1 { font-size: 5.9vw; }` |



| `vmin` | `1vw` 或 `1vh` 中的较小值 | `p { font-size: 2vmin;}` |

# 第 5 章：颜色

在 CSS 中，我们使用值来指定颜色。通常，这些值用于设置元素文本的颜色（即前景色）或元素的背景色。我们也可以使用它们来改变装饰效果（如边框）的颜色。

颜色值可以用几种不同的格式指定，如下表所示：

| 格式 | 语法 | 示例 |
| --- | --- | --- |
| 十六进制代码 | `#RRGGBB` | `p{color:#FF0000;}` |
| 短十六进制代码 | `#RGB` | `p{color:#6A7;}` |
| RGB 百分比 | `rgb(rrr%,ggg%,bbb%)` | `p{color:rgb(50%,50%,50%);}` |
| RGB 绝对值 | `rgb(rrr,ggg,bbb)` | `p{color:rgb(0,0,255);}` |
| 关键字 | `aqua`, `black`, 等 | `p{color:teal;}` |

让我们更详细地了解这些格式：

## 十六进制代码

十六进制是 6 位颜色表示。第一位 `RR` 表示红色值，`GG` 表示绿色值，`BB` 表示蓝色值。

这些值可以从图形软件（如 JASC Paintshop Pro、Adobe Photoshop、Advanced Paintbrush 等）中获取。每个十六进制代码前面都有一个 `#` 或 `£` 符号，以下是十六进制表示法的示例：

| 颜色 | 颜色十六进制 |
| --- | --- |
|  | `#000000` |
|  | `#FF0000` |
|  | `#00FF00` |
|  | `#0000FF` |
|  | `#FFFF00` |
|  | `#00FFFF` |
|  | `#FF00FF` |
|  | `#C0C0C0` |
|  | `#FFFFFF` |

## 短十六进制代码

这只是十六进制代码的较短版本，每个数字会被复制，从而得到等效的 6 位值。这些值也可以从图形软件中获取，并且前面也有 `#` 或 `£` 符号：

| 颜色 | 颜色十六进制 |
| --- | --- |
|  | `#000` |
|  | `#F00` |
|  | `#0F0` |
|  | `#0FF` |
|  | `#FF0` |
|  | `#0FF` |
|  | `#F0F` |
|  | `#FFF` |

## RGB 值

我们使用 `rgb()` 属性来指定此值，该属性接受三个值——红色、绿色和蓝色。值可以是百分比或 0 到 255 之间的整数。请注意，并非所有浏览器都支持 `rgb()`，因此尽量少用。

| 颜色 | 颜色 RGB |
| --- | --- |
|  | `rgb(0,0,0)` |
|  | `rgb(255,0,0)` |
|  | `rgb(0,255,0)` |
|  | `rgb(0,0,255)` |
|  | `rgb(255,255,0)` |
|  | `rgb(0,255,255)` |
|  | `rgb(255,0,255)` |
|  | `rgb(192,192,192)` |
|  | `rgb(255,255,255)` |

## 构建颜色代码

如果你使用 CSS 颜色代码生成器，你可以构建数百万种不同的颜色代码，但你需要一个支持 Java 的浏览器才能做到这一点。

## 浏览器安全颜色

下表显示了 216 种被认为是安全且与计算机无关的颜色。它们从十六进制代码 `000000` 到 `FFFFFF`，之所以安全，是因为所有计算机都能在 256 色调色板上正确显示这些颜色：

| | | | | | |
|---|---|---|---|---|---|
| `000000` | `000033` | `000066` | `000099` | `0000CC` | `0000FF` |
| `003300` | `003333` | `003366` | `003399` | `0033CC` | `0033FF` |
| `006600` | `006633` | `006666` | `006699` | `0066CC` | `0066FF` |
| `009900` | `009933` | `009966` | `009999` | `0099CC` | `0099FF` |
| `00CC00` | `00CC33` | `00CC66` | `00CC99` | `00CCCC` | `00CCFF` |
| `00FF00` | `00FF33` | `00FF66` | `00FF99` | `00FFCC` | `00FFFF` |
| `330000` | `330033` | `330066` | `330099` | `3300CC` | `3300FF` |
| `333300` | `333333` | `333366` | `333399` | `3333CC` | `3333FF` |
| `336600` | `336633` | `336666` | `336699` | `3366CC` | `3366FF` |
| `339900` | `339933` | `339966` | `339999` | `3399CC` | `3399FF` |
| `33CC00` | `33CC33` | `33CC66` | `33CC99` | `33CCCC` | `33CCFF` |
| `33FF00` | `33FF33` | `33FF66` | `33FF99` | `33FFCC` | `33FFFF` |
| `660000` | `660033` | `660066` | `660099` | `6600CC` | `6600FF` |
| `663300` | `663333` | `663366` | `663399` | `6633CC` | `6633FF` |
| `666600` | `666633` | `666666` | `666699` | `6666CC` | `6666FF` |
| `669900` | `669933` | `669966` | `669999` | `6699CC` | `6699FF` |
| `66CC00` | `66CC33` | `66CC66` | `66CC99` | `66CCCC` | `66CCFF` |
| `66FF00` | `66FF33` | `66FF66` | `66FF99` | `66FFCC` | `66FFFF` |
| `990000` | `990033` | `990066` | `990099` | `9900CC` | `9900FF` |
| `993300` | `993333` | `993366` | `993399` | `9933CC` | `9933FF` |
| `996600` | `996633` | `996666` | `996699` | `9966CC` | `9966FF` |
| `999900` | `999933` | `999966` | `999999` | `9999CC` | `9999FF` |
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

# 第 6 章：背景

在本章中，我们将学习如何为不同的 HTML 元素设置背景。可以设置以下属性：

*   `background-color` - 设置元素的背景颜色
*   `background-image` - 设置元素的背景图像
*   `background-repeat` – 控制背景图像的重复方式
*   `background-position` – 控制背景图像的位置
*   `background-attachment` – 控制背景图像如何随页面滚动
*   `background` – 作为简写属性，用于同时指定多个背景属性

## 设置背景颜色

以下示例展示了如何为元素设置背景颜色：

```html
<html>
   <head>
   <body>
      <p style = "background-color:yellow;">
      This text has a yellow background color.</p>
   </body>
   </head>
<html>
```

你将在屏幕上看到以下内容：

这段文本具有黄色背景。

## 如何设置背景图像

以下示例展示了如何调用本地存储的图像来设置背景：

```html
<html>
   <head>
      <style>
         body  {
            background-image: url("/css/images/css.jpg");
            background-color: #cccccc;
         }
      </style>
      <body>
         <h1>Hello World!</h1>
      </body>
   </head>
<html>
```

现在你将在指定的背景上看到“Hello, World!”。

## 如何重复背景图像

以下是一个重复小背景图像的示例。如果图像不希望重复，而只显示一次，则可以将 `background-repeat` 属性的值设为 `no-repeat`。默认情况下，`background-repeat` 的值为 `repeat`：

```html
<html>
   <head>
      <style>
         body {
            background-image: url("/css/images/css.jpg");
            background-repeat: repeat;
         }
      </style>
   </head>
   <body>
      <p>Tutorials point</p>
   </body>
</html>
```

上一个示例中使用的背景现在将重复显示。在下面的示例中，我们将看到如何垂直重复图像：

```html
<html>
   <head>
      <style>
         body {
            background-image: url("/css/images/css.jpg");
            background-repeat: repeat-y;
         }
      </style>
   </head>
   <body>
      <p>Tutorials point</>
   </body>
</html>
```

选定的背景图像将垂直重复。

下一个示例中，我们来看水平重复：

```html
<html>
   <head>
      <style>
         body {
            background-image: url("/css/images/css.jpg");
            background-repeat: repeat-x;
         }
 </style>
   </head>
   <body>
      <p>Tutorials point</>
   </body>
</html>
```

选定的背景图像将水平重复。

## 如何设置背景图像的位置

以下示例展示了如何将图像放置在距离左侧 100 像素的位置：

```html
<html>
   <head>
      <style>
         body {
            background-image: url("/css/images/css.jpg");
            background-position:100px;
         }
      </style>
   </head>
   <body>
      <p>Tutorials point</>
   </body>
</html>
```

背景图像将被放置在指定位置。

现在我们来看如何将图像放置在距离左侧 100 像素、距离顶部 200 像素的位置：

```html
<html>
   <head>
      <style>
         body {
            background-image: url("/css/images/css.jpg");
            background-position:100px 200px;
         }
 </style>
   </head>
   <body>
      <p>Tutorials point</>
   </body>
</html>
```

背景图像将被放置在指定位置。

## 如何设置背景附着

这决定了图像是固定不动，还是随页面滚动。首先，我们来看固定图像：

```html
<!DOCTYPE html>
<html>
   <head>
      <style>
         body  {
            background-image: url('/css/images/css.jpg');
            background-repeat: no-repeat;
            background-attachment: fixed;
         }
      </style>
   </head>
   <body>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
   </body>
</html>
```

你将看到这行文字在代码中重复出现多次：

背景图像是固定的。尝试向下滚动页面。

接着是：

如果你没有看到滚动条，请尝试调整浏览器窗口大小。

接下来，我们来看设置滚动背景：



```html
<!DOCTYPE html>
<html>
   <head>
      <style>
         body  {
            background-image: url('/css/images/css.jpg');
            background-repeat: no-repeat;
            background-attachment: fixed;
            background-attachment:scroll;
         }.
      </style>
   </head>
   <body>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
      <p>The background-image is fixed. Try scrolling down the page.</p>
   </body>
</html>
```

同样，你将在滚动背景上看到这条重复的消息：

背景图像是固定的。尝试向下滚动页面。

接着是：

如果你没有看到滚动条，请尝试调整浏览器窗口大小。

## 如何使用简写属性

最后一个示例展示了如何通过简写`background`属性同时设置所有背景属性：

```html
<p style="background:url(/images/pattern1.gif) repeat fixed;">
   This paragraph has a fixed background image that will be repeated.
</p>
```

# 第 7 章：字体

现在我们将学习如何设置字体。以下是你可以为元素设置的字体属性：

*   `font-family` - 用于更改字体系列
*   `font-style` - 用于将字体设置为斜体或倾斜
*   `font-weight` – 用于增加或减少字体的粗细或亮度
*   `font-variant` – 用于使字体呈现小型大写字母效果
*   `font-size` – 用于放大或缩小字体

## `font` – 用于指定各种字体属性的简写属性

### 如何设置字体系列

以下示例展示了如何设置特定元素的字体系列。该值可以是任何字体系列名称：

```html
<html>
   <head>
   </head>
   <body>
      <p style="font-family:georgia,garamond,serif;">
      This text will be rendered in georgia, garamond, or the default serif font
      depending on which ones are in your system.
      </p>
   </body>
</html>
```

它将产生以下结果——

此文本将根据您系统中存在的字体，以`georgia`、`garamond`或默认衬线字体呈现。

### 如何设置字体样式

以下示例展示了如何设置元素的样式。值可以是`italic`、`normal`、`oblique`等。

```html
<html>
   <head>
   </head>
   <body>
      <p style="font-style:italic;">
      This text is rendered in italic style
      </p>
   </body>
</html>
```

您将得到以下结果：

此文本以斜体样式呈现。

### 如何设置字体变体

此示例展示了如何设置字体变体，可能的值有`small-caps`、`normal`等。

```html
<html>
   <head>
   </head>
   <body>
      <p style="font-variant:small-caps;">
      The text is going to be rendered as small caps
      </p>
   </body>
</html>
```

您将得到以下结果：

THE TEXT IS GOING TO BE RENDERED AS SMALL CAPS

### 如何设置字体粗细

下一个示例展示了如何设置元素的字体粗细。此属性将指定字体的粗体级别，可能的值包括 – `normal`、`lighter`、`bold`、`bolder`、`100`、`200`、`300`、`400`、`500`、`600`、`700`、`800`、`900`等。

```html
<html>
   <head>
   </head>
   <body>
      <p style="font-weight:bold;">The font is bold.</p>
      <p style="font-weight:bolder;">The font is bolder.</p>
      <p style="font-weight:500;">The font is 500 weight.</p>
   </body>
</html>
```

您将得到以下结果：

The font is bold.

The font is bolder.

The font is 500 weight.

### 如何设置字体大小

此示例展示了如何设置元素的字体大小。这用于控制字体大小，可能的值有 – `small`、`x-small`、`xx-small`、`xx-large`、`x-large`、`large`、`smaller`、`larger`、`%`或像素大小：

```html
<html>
   <head>
   </head>
   <body>
      <p style="font-size:20px;">The font size is 20 pixels</p>
      <p style="font-size:small;">The font size is small</p>
      <p style="font-size:large;">The font size is large</p>
   </body>
</html>
```

您将得到以下结果：

The font size is 20 pixels

The font size is small

The font size is large

### 如何设置字体大小调整

此示例将演示如何设置字体大小调整，它允许您更改 x 高度以使字体更易读。可能的值可以是任何数字：

```html
<html>
   <head>
   </head>
   <body>
      <p style="font-size-adjust:0.61;">
         The text uses a font-size-adjust value.
      </p>
   </body>
</html>
```

您将得到以下结果——

THE TEXT USES A FONT-SIZE-ADJUST VALUE.

### 如何设置字体拉伸

下一个示例展示了如何设置字体拉伸，它依赖于您的计算机是否拥有特定字体的紧缩或扩展版本。值可能为 – `wider`、`normal`、`narrower`、`extra-condensed`、`ultra-condensed`、`condensed`、`semi-condensed`、`expanded`、`semi-expanded`、`extra-expanded`、`ultra-expanded`：

```html
<html>
   <head>
   </head>
   <body>
      <p style="font-stretch:ultra-expanded;">
         If this doesn't look like it works, most likely your computer does not have a condensed or expanded version of the font
      </p>
   </body>
</html>
```

它将产生以下结果——

If this doesn't look like it works, most likely your computer does not have a condensed or expanded version of the font

### 如何设置简写属性

最后一个示例展示了如何使用`font`属性同时设置所有字体属性：

```html
<html>
   <head>
   </head>
   <body>
      <p style="font:italic small-caps bold 15px georgia;">
      This will apply all of the properties on the text at the same time.
      </p>
   </body>
</html>
```

它将产生以下结果——

THIS WILL APPLY ALL OF THE PROPERTIES ON THE TEXT AT THE SAME TIME.

# 第 8 章：文本

本章将介绍如何通过使用一些 CSS 属性来操作文本。以下文本属性可用于元素：

* `color` – 用于设置文本的颜色
* `direction` – 用于设置文本的方向
* `letter-spacing` – 用于在单词的字母之间添加或删除空格
* `text-indent` – 用于缩进文本段落的第一行
* `text-align` – 用于对齐整个文档中的文本
* `text-decoration` – 用于为文本添加装饰，例如`underline`、`overline`和`strikethrough`
* `text-transform` – 用于将文本大写或在大小写字母之间转换
* `white-space` – 用于控制文本流和格式
* `text-shadow` – 用于在文本周围设置阴影

## 如何设置文本颜色

此示例展示了如何设置文本的颜色，使用任何有效格式的任何颜色名称作为值。

```html
<html>
   <head>
   </head>
   <body>
      <p style="color:red;">
      This text is shown in red.
      </p>
   </body>
</html>
```

您将看到以下结果——

This text is shown in red.

## 如何设置文本方向

下一个示例展示了如何设置文本方向，使用`ltr`或`rtl`作为值。

```html
<html>
   <head>
   </head>
   <body>
      <p style="direction:rtl;">
      This text is going to be rendered from right to left
      </p>
   </body>
</html>
```

您将看到此结果——

This text is going to be rendered from right to left

## 如何设置字符间距

此示例展示了如何设置字符之间的间距，使用`normal`或指定间距的数字作为值。

```html
<html>
   <head>
   </head>
   <body>
      <p style="letter-spacing:5px;">
      This text will have spaces between letters.
      </p>
   </body>
</html>
```

您将看到此结果——

This text will have spaces between letters.

## 如何设置单词间距

下一个示例展示了如何设置单词之间的间距，使用`normal`或指定间距的数字作为值。

```html
<html>
   <head>
   </head>
   <body>
      <p style="word-spacing:5px;">
      This text has spaces between words.
      </p>
   </body>
</html>
```

您将看到以下结果——

This text has spaces between words.

## 如何设置文本缩进

下一个示例展示了如何缩进新段落的第一行，使用指定缩进空间的数字或`%`作为值。

```html
<html>
   <head>
   </head>
   <body>
      <p style="text-indent:1cm;">
      The text has the first line indented by 1cm and it will remain at
      this position. This is done using the CSS text-indent property.
      </p>
   </body>
</html>
```

您将看到此结果——

The text has the first line indented by 1cm and it will remain at this position. This is done using the CSS text-indent property

## 如何设置文本对齐

此示例展示了如何对齐文本，使用`justify`、`left`、`right`和`center`作为值。

```html
<html>
   <head>
   </head>
   <body>
      <p style="text-align:right;">
      The text will be right aligned.
      </p>
      <p style="text-align:center;">
      The text will be center aligned.
      </p>
      <p style="text-align:left;">
      The text will be left aligned.
      </p>
   </body>
</html>
```

您将看到以下结果——

The text will be right aligned.

The text will be center aligned.

The text will be left aligned.

## 如何装饰文本

现在我们来看一个示例，展示如何装饰文本，使用`none`、`overline`、`underline`、`blink`和`strikethrough`作为值。

```html
<html>
   <head>
   </head>
   <body>
      <p style="text-decoration:underline;">
```

# 第 9 章：使用图像

图像是网站的重要组成部分，虽然不应使用过多，但使用的图像应质量良好且位置恰当。CSS 通过允许设置以下属性来控制这些图像的显示：

*   `Border` – 用于设置图像边框的宽度
*   `Height` – 用于设置图像的高度
*   `Width` – 用于设置图像的宽度
*   `-moz-opacity` – 用于确定图像的不透明度

## 图像边框

该属性用于设置图像边框的宽度，可以使用长度值或`%`。例如：

```
<html>
   <head>
   </head>
   <body>
      <img style="border:0px;" src="/css/images/logo.png" />
      <br />
      <img style="border:3px dashed red;" src="/css/images/logo.png" />
   </body>
</html>
```

结果将是一个无边框的徽标，然后是一个带有红色虚线边框的徽标。

## 图像高度

该属性用于设置图像的高度，可以使用长度值或`%`。当使用`%`时，该值应用于图像所在的盒子：



```html
<html>
   <head>
   </head>
   <body>
      <img style="border:1px solid red; height:100px;" src="/css/images/logo.png" />
      <br />
      <img style="border:1px solid red; height:50%;" src="/css/images/logo.png" />
   </body>
</html>
```

结果将是两个完全相同的徽标，但一个比另一个高。

## 图像宽度

该属性用于使用`%`或长度值设置图像的宽度。与高度类似，使用百分比时应用于图像所在的盒子：

```html
<html>
   <head>
   </head>
   <body>
      <img style="border:1px solid red; width:150px;" src="/css/images/logo.png" />
      <br />
      <img style="border:1px solid red; width:100%;" src="/css/images/logo.png" />
   </body>
</html>
```

结果将是两个相同的徽标，但尺寸不同。

## `-moz-opacity`

最后一个属性用于设置图像的不透明度，适用于 Mozilla Firefox。对于 Internet Explorer，我们使用`filter:alpha(opacity=x)`来实现透明图像。

在 Mozilla Firefox 中，属性`-moz-opacity:x`中的`x`可以取`0.0`到`1.0`之间的任意值。值越低，图像越透明。同样，在 Internet Explorer 中，`filter:alpha(opacity=x)`的`x`值可以在`0`到`100`之间。同样，值越低，图像越透明。

```html
<html>
   <head>
   </head>
   <body>
      <img style="border:1px solid red;-moz-opacity:0.4;filter:alpha(opacity=40);" src="/css/images/logo.png" />
   </body>
</html>
```

结果将是一个带有红色实线边框的徽标。

# 第 10 章：链接

在本章中，我们将了解如何使用 CSS 设置超链接的属性。可以设置以下属性：

- `:link` 用于表示未访问的超链接。
- `:visited` 用于表示已访问的超链接。
- `:hover` 用于表示鼠标指针悬停在其上的元素。
- `:active` 用于表示当前正在被点击的元素。

通常，这些属性存储在 HTML 文档的头部。请记住以下有效使用的规则：

- 在 CSS 定义中，`a:hover` 位于 `a:link` 和 `a:visited` 之后。
- `a:active` 位于 `a:hover` 之后，如下例所示：

```html
<style type="text/css">
   a:link {color: #000000}
   a:visited {color: #006600}
   a:hover {color: #FFCC00}
   a:active {color: #FF00CC}
</style>
```

接下来，我们将了解这些属性如何用于实现超链接的不同效果。

## 设置颜色

此示例展示了如何使用任何有效格式的颜色名称值来设置链接的颜色：

```html
<html>
   <head>
      <style type="text/css">
         a:link {color:#000000}
      </style>
   </head>
   <body>
      <a href="">Link</a>
   </body>
</html>
```

结果将是一个黑色链接。请注意，这些链接均不可点击，仅用于演示目的。

链接

## 已访问链接的颜色

此示例展示了如何设置已访问链接的颜色，同样使用任何有效格式的颜色名称值：

```html
<html>
   <head>
      <style type="text/css">
         a:visited {color: #006600}
      </style>
   </head>
   <body>
      <a href=""> link</a>
   </body>
</html>
```

结果将是以下链接：初始为黑色，点击后变为绿色。

链接

## 鼠标悬停时链接的颜色

此示例展示了当鼠标指针悬停在链接上时如何改变其颜色：

```html
<html>
   <head>
      <style type="text/css">
         a:hover {color: #FFCC00}
      </style>
   </head>
   <body>
      <a href="">Link</a>
   </body>
</html>
```

结果将是一个黑色链接，当鼠标悬停在其上时变为黄色。

链接

## 活动链接的颜色

此示例展示了如何改变活动链接的颜色：

```html
<html>
   <head>
      <style type="text/css">
         a:active {color: #FF00CC}
      </style>
   </head>
   <body>
      <a href="">Link</a>
   </body>
</html>
```

结果将是一个黑色链接，点击时变为粉色。

链接

# 第 11 章：表格

在本章中，我们将了解可以为 HTML 表格设置的属性。可以设置以下属性：

- `Border-collapse` – 指定表格的单元格是保持各自的外观，还是由浏览器控制相邻的边框。
- `Border-spacing` – 指定表格单元格之间的间距宽度。
- `Caption-side` 标题 – 这些标题位于`<caption>`元素中，默认情况下渲染在表格上方。它们可用于设置表格标题的位置。
- `Empty-cells` – 指定是否应在空单元格上显示边框。
- `Table-layout` – 允许浏览器通过使用它为列找到的第一个宽度属性来加速表格布局，而无需加载表格后再渲染。

接下来我们通过示例来了解这些属性。

## `Border-Collapse`

该属性可以有两个值 – `collapse`和`separate`。以下示例同时使用了这两个值：

```html
<html>
   <head>
      <style type="text/css">
         table.one {border-collapse:collapse;}
         table.two {border-collapse:separate;}
         td.a {
            border-style:dotted;
            border-width:3px;
            border-color:#000000;
            padding: 10px;
         }
         td.b {
            border-style:solid;
            border-width:3px;
            border-color:#333333;
            padding:10px;
         }
      </style>
   </head>
   <body>
      <table class="one">
         <caption>折叠边框示例</caption>
         <tr><td class="a1 Cell 1 Collapse Example</td></tr>
         <tr><td class="2"> Cell 2 Collapse Example</td></tr>
      </table>
      <br />
      <table class="two">
         <caption>分离边框示例</caption>
         <tr><td class="1"> Cell 1 Separate Example</td></tr>
         <tr><td class="2"> Cell 2 Separate Example</td></tr>
      </table>
   </body>
</html>
```

这将产生以下结果：

| 折叠边框： |
|---|
| 单元格 1 折叠示例 |
| 单元格 2 折叠示例 |
| 分离边框： |
| 单元格 1 分离示例 |
| 单元格 2 分离示例 |

## `Border-Spacing`

该属性指定两个相邻单元格边框之间的距离。它可以接受两个值中的任意一个，每个值都应为长度单位。一个值适用于水平和垂直边框，而使用两个值则分别表示垂直和水平间距。

```css
<style type="text/css">
   /* 如果提供一个值 */
   table.example {border-spacing:10px;}
   /* 这是提供两个值的方法 */
   table.example {border-spacing:10px; 15px;}
</style>
```

下一个示例修改了第一个示例：

```html
<html>
   <head>
      <style type="text/css">
         table.one {
            border-collapse:separate;
            width:400px;
            border-spacing:10px;
         }
         table.two {
            border-collapse:separate;
            width:400px;
            border-spacing:10px 50px;
         }
      </style>
   </head>
   <body>
      <table class="one" border="1">
         <caption>带边框间距的分离边框示例</caption>
         <tr><td> 单元格 A 折叠示例</td></tr>
         <tr><td> 单元格 B 折叠示例</td></tr>
      </table>
      <br />
      <table class="two" border="1">
         <caption>带边框间距的分离边框示例</caption>
         <tr><td> 单元格 A 分离示例</td></tr>
         <tr><td> 单元格 B 分离示例</td></tr>
      </table>
   </body>
</html>
```

## `Caption-Side` 属性

该属性允许你指定`<caption>`元素内容相对于表格的位置。它可以接受以下四个值 – `top`、`left`、`bottom`、`right`。以下示例使用了所有四个值：

```html
<html>
   <head>
      <style type="text/css">
         caption.top {caption-side:top}
         caption.bottom {caption-side:bottom}
         caption.left {caption-side:left}
         caption.right {caption-side:right}
      </style>
   </head>
   <body>
      <table style="width:400px; border:1px solid black;">
         <caption class="top">
         此标题将显示在顶部
         </caption>
         <tr><td > 单元格 A</td></tr>
         <tr><td > 单元格 B</td></tr>
      </table>
      <br />
      <table style="width:400px; border:1px solid black;">
         <caption class="bottom">
         标题显示在底部
         </caption>
         <tr><td > 单元格 A</td></tr>
         <tr><td > 单元格 B</td></tr>
      </table>
      <br />
      <table style="width:400px; border:1px solid black;">
         <caption class="left">
         标题显示在左侧
         </caption>
         <tr><td > 单元格 A</td></tr>
         <tr><td > 单元格 B</td></tr>
      </table>
      <br />
      <table style="width:400px; border:1px solid black;">
         <caption class="right">
         标题显示在右侧
         </caption>
         <tr><td > 单元格 A</td></tr>
         <tr><td > 单元格 B</td></tr>
      </table>
   </body>
</html>
```

## `Empty-Cells`

该属性用于指示空单元格是否应显示边框。它可以取以下三个值之一 – `hide`、`show`、`inherit`。以下示例展示了如何使用该属性隐藏`<table>`元素中空单元格的边框：

```html
<html>
   <head>
      <style type="text/css">
         table.empty{
            width:350px;
            border-collapse:separate;
            empty-cells:hide;
         }
         td.empty{
            padding:5px;
            border-style:solid;
            border-width:1px;
            border-color:#999999;
         }
      </style>
   </head>
   <body>
      <table class="empty">
      <tr>
         <th></th>
         <th>标题一</th>
         <th>标题二</th>
      </tr>
      <tr>
         <th>行标题</th>
         <td class="empty">值</td>
         <td class="empty">值</td>
      </tr>
      <tr>
         <th>行标题</th>
         <td class="empty">值</td>
         <td class="empty"></td>
      </tr>
      </table>
   </body>
</html>
```

## `Table-Layout`

该属性旨在帮助你控制浏览器如何布局或渲染表格。它可以取以下三个值之一 – `inherit`、`auto`或`fixed`。下一个示例展示了：

```html
<html>
   <head>
      <style type="text/css">
         table.auto {
            table-layout: auto
         }
         table.fixed{
            table-layout: fixed
         }
      </style>
   </head>
   <body>
      <table class="auto" border="1" width="100%">
      <tr>
         <td width="20%">1000000000000000000000000000</td>
         <td width="40%">10000000</td>
         <td width="40%">100</td>
      </tr>
      </table>
      <br />
      <table class="fixed" border="1" width="100%">
      <tr>
         <td width="20%">1000000000000000000000000000</td>
         <td width="40%">10000000</td>
         <td width="40%">100</td>
      </tr>
      </table>
   </body>
</html>
```

# 第 12 章：边框

边框属性允许你指定元素框的边框外观。以下是你可以控制的三个属性：



`Border-color` – 允许你指定边框的颜色

`Border-style` – 允许你从一系列值中选择样式，包括实线、虚线、双线等

`Border-width` – 允许你指定边框的宽度

## `Border-Color`

该属性允许你更改元素周围边框的颜色。你可以使用以下属性单独更改边框的每一侧：

- `Border-bottom-color`
- `Border-top-color`
- `Border-left-color`
- `Border-right-color`

以下示例展示了所有四个属性的使用：

```html
<html>
   <head>
      <style type="text/css">
         p.example1{
            border:1px solid;
            border-bottom-color:#009900; /* 绿色 */
            border-top-color:#FF0000;    /* 红色 */
            border-left-color:#330000;   /* 黑色 */
            border-right-color:#0000CC;  /* 蓝色 */
         }
         p.example2{
            border:1px solid;
            border-color:#009900;        /* 绿色 */
         }
      </style>
   </head>
   <body>
      <p class="example1">
      此示例展示了所有边框以不同颜色显示。
      </p>
      <p class="example2">
      此示例展示了所有边框仅以绿色显示。
      </p>
   </body>
</html>
```

结果将是：

此示例展示了所有边框以不同颜色显示。

此示例展示了所有边框仅以绿色显示。

## 边框样式（`Border-style`）

此属性允许你选择以下样式之一：

- `None`（无） – 完全没有边框
- `Solid`（实线） – 边框为实线
- `Dotted`（点线） – 边框由点组成
- `Dashed`（虚线） – 边框由短线段组成
- `Double`（双线） – 两条实线
- `Groove`（凹槽） – 使边框看起来像刻入页面
- `Ridge`（脊状） – 与凹槽效果相反
- `Inset`（内嵌） – 盒子看起来嵌入页面
- `Outset`（外凸） – 盒子看起来从页面凸出
- `Hidden`（隐藏） – 与 `None` 完全相同，但针对表格元素的边框冲突解决有例外

与颜色一样，你可以使用以下属性单独更改边框每一侧的样式：

- `Border-bottom-style`
- `Border-top-style`
- `Border-left-style`
- `Border-right-style`

此示例使用了所有这四种样式：

```html
<html>
   <head>
   </head>
   <body>
      <p style="border-width:4px; border-style:none;">
      This is a border with a width of none.
      </p>
      <p style="border-width:4px; border-style:solid;">
      This is a solid border.
      </p>
      <p style="border-width:4px; border-style:dashed;">
      This is a dashed border.
      </p>
      <p style="border-width:4px; border-style:double;">
      This is a double border.
      </p>
      <p style="border-width:4px; border-style:groove;">
      This is a groove border.
      </p>
      <p style="border-width:4px; border-style:ridge">
      This is a ridge border.
      </p>
      <p style="border-width:4px; border-style:inset;">
      This is an inset border.
      </p>
      <p style="border-width:4px; border-style:outset;">
      This is an outset border.
      </p>
      <p style="border-width:4px; border-style:hidden;">
      This is a hidden border.
      </p>
      <p style="border-width:4px;border-top-style:solid;
      border-bottom-style:dashed; border-left-style:groove; border-right-style:double;">
      This is a border with four different styles.
      </p>
   </body>
</html>
```

结果将是：

这是一个宽度为 `none` 的边框。

这是一个实线边框。

这是一个虚线边框。

这是一个双线边框。

这是一个凹槽边框。

这是一个脊状边框。

这是一个内嵌边框。

这是一个外凸边框。

这是一个隐藏边框。

这是一个具有四种不同样式的边框。

## 边框宽度（`Border-Width`）

这允许你设置边框的宽度，使用 `pt`、`px` 或 `cm` 的长度值，或者你可以将其设置为 `thick`（粗）、`medium`（中）或 `thin`（细）。你可以使用以下属性单独更改边框的每一侧：

- `border-bottom-width`
- `border-top-width`
- `border-left-width`
- `border-right-width`

此示例使用了所有这些属性：

```html
<html>
   <head>
   </head>
   <body>
      <p style="border-width:4px; border-style:solid;">
      This is a solid border with a width of 4px.
      </p>
      <p style="border-width:4pt; border-style:solid;">
      This is a solid border whose width is 4pt.
      </p>
      <p style="border-width:thin; border-style:solid;">
      This is a solid border whose width is thin.
      </p>
      <p style="border-width:medium; border-style:solid;">
      This is a solid border whose width is medium;
      </p>
      <p style="border-width:thick; border-style:solid;">
      This is a solid border whose width is thick.
      </p>
      <p style="border-bottom-width:4px;border-top-width:10px;
      border-left-width: 2px;border-right-width:15px;border-style:solid;">
      This is a border with four different widths.
      </p>
   </body>
</html>
```

结果将是：

这是一个宽度为 `4px` 的实线边框。

这是一个宽度为 `4pt` 的实线边框。

这是一个宽度为 `thin`（细）的实线边框。

这是一个宽度为 `medium`（中）的实线边框；

这是一个宽度为 `thick`（粗）的实线边框。

这是一个具有四种不同宽度的边框。

## 边框简写属性（Shorthand Border Properties）

使用简写边框属性，你可以仅用一个属性而不是三个来指定线条的样式、颜色和宽度。以下示例使用 `border` 属性将三者合并，你会发现这是为元素设置边框最常用的方法：

```html
<html>
   <head>
   </head>
   <body>
      <p style="border:4px solid red;">
      Another example:
      </p>
   </body>
</html>
```

# 第 13 章：边距（Margins）

最后一章讨论 `margin` 属性，即 HTML 元素周围的空间。`Margin` 属性值不会被子元素继承，并且你也可以使用负值来重叠内容。

请记住——相邻的垂直边距（即上边距和下边距）会相互折叠，因此每个块之间的距离**不是**边距之和；而是取较大的边距，如果两者大小相同，则等于其中一个边距。

可以使用以下属性：

- `Margin` – 指定在一个声明中设置所有边距属性的简写
- `Margin-bottom` – 指定下边距
- `Margin-top` – 指定上边距
- `Margin-left` – 指定左边距
- `Margin-right` – 指定右边距

现在我们将看看这些属性是如何使用的。

## 边距属性（`Margin` Property）

这是一个简写属性，允许你通过单个声明设置所有四个边距的属性。以下示例展示了如何为段落设置边距：

```html
<html>
   <head>
   </head>
   <body>
      <p style="margin: 15px; border:1px solid black;">
      all four margins will be 15px
      </p>
      <p style="margin:10px 2%; border:1px solid black;">
      top and bottom margin will be 10px, left and right margin will be 2% of the total width of the document.
      </p>
      <p style="margin: 10px 2% -10px; border:1px solid black;">
      top margin will be 10px, left and right margin will be 2% of the total width of the document, bottom margin will be -10px
      </p>
      <p style="margin: 10px 2% -10px auto; border:1px solid black;">
      top margin will be 10px, right margin will be 2% of the total width of the document, bottom margin will be -10px, left margin will be set by the browser
      </p>
   </body>
</html>
```

你将看到以下结果：

所有四个边距均为 `15px`

上边距和下边距为 `10px`，左边距和右边距为文档总宽度的 `2%`。

上边距为 `10px`，左边距和右边距为文档总宽度的 `2%`，下边距为 `-10px`

上边距为 `10px`，右边距为文档总宽度的 `2%`，下边距为 `-10px`，左边距由浏览器设置

## 下边距（`Margin-Bottom`）

这允许你使用 `auto`、长度或百分比值设置下边距：

```html
<html>
   <head>
   </head>
   <body>
      <p style="margin-bottom: 15px; border:1px solid black;">
      This is a paragraph with a specified bottom margin.
      </p>
      <p style="margin-bottom: 5%; border:1px solid black;">
      This is another paragraph with a specified bottom margin in percent
      </p>
   </body>
</html>
```

结果将是：

这是一个指定了下边距的段落。

这是另一个以百分比指定了下边距的段落。

## 上边距（`Margin-Top`）

这允许你指定上边距，并使用 `auto`、长度或百分比值：

```html
<html>
   <head>
   </head>
   <body>
      <p style="margin-top: 15px; border:1px solid black;">
      This is a paragraph with a specified top margin
      </p>
      <p style="margin-top: 5%; border:1px solid black;">
      This is another paragraph with a specified top margin in percent
      </p>
   </body>
</html>
```

结果如下：

这是一个指定了上边距的段落。

这是另一个段落，指定了百分比形式的上外边距。

## `Margin-Left`

该属性允许你设置左外边距，可以使用 `%`、`auto` 或 `length` 作为值。

```html
<html>
   <head>
   </head>
   <body>
      <p style="margin-left: 15px; border:1px solid black;">
      This is a paragraph with a specified left margin
      </p>
      <p style="margin-left: 5%; border:1px solid black;">
      This is another paragraph with a specified top margin in percent
      </p>
   </body>
</html>
```

结果如下所示：

这是一个指定了左外边距的段落

这是另一个指定了百分比形式的上外边距的段落

## `Margin-Right`

该属性允许你指定右外边距，可以使用 `auto`、`length` 或 `%` 作为值。

```html
<html>
   <head>
   </head>
   <body>
      <p style="margin-right: 15px; border:1px solid black;">
      This is a paragraph with a specified right margin
      </p>
      <p style="margin-right: 5%; border:1px solid black;">
      This is another paragraph with a specified right margin in percent
      </p>
   </body>
</html>
```

结果将如下所示：

这是一个指定了右外边距的段落

这是另一个指定了百分比形式的右外边距的段落

# 结语

感谢您购买我的书，希望它对您有所帮助。正如您所见，对于任何想要进入网页设计世界的人来说，CSS 都是一个真正令人惊叹的工具。尽管它是最容易理解和学习的语言之一，但我不能保证您能在一夜之间学会它。与任何计算机语言一样，它需要时间和耐心。

您需要全身心投入学习，一旦掌握了它，就必须准备好跟上所有最新的发展。CSS 不是那种您可以学会、忘记、几个月后再重新捡起来的程序。虽然您脑海中仍会保留基础知识，但在那几个月里，可能已经发生了很多变化，许多改动也可能已经出现。至关重要的是，您要跟上这些变化，并每天使用 CSS，以确保不会丢失任何新掌握的技能。

CSS 是一种您需要学习、理解并融入日常生活的程序。请允许我向您提一个小请求——您能在 Amazon.com 上为我写一篇评论吗？这不仅对我有帮助，对可能决定购买我书的其他人也有帮助。

如前所述，在此重申，我在本书中使用的一些示例代码归功于 www.tutorialspoint.com。
