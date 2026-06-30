# Android Web 应用开发入门指南：使用 HTML5、CSS3 和 JavaScript 为 Android 进行开发






为方便读者，Apress 将部分前言材料置于索引之后。请使用"书签"和"目录概览"链接访问这些内容。

Apress®

www.allitebooks.com


## 引言

第一位作者（Jon）的父母都是艺术家。他们每个人都能画出酷似现实生活的奇妙图画，并且惊讶地发现自己的儿子几乎连一个火柴人都画不好。如果你一直觉得，你内心的艺术家气质最好通过借助计算机和互联网所能构建的东西来表达，那么本书可以指导你手中的"虚拟画笔"。最终成果是什么？一个面向 Android 设备的移动网页应用，它可以进而激发数百万潜在用户的创造力和生产力。我们希望这本书能为你提供所需的一切，让你迅速上手并开始创作你的杰作。

### 本书适合谁

本书是为初学者编写的。在写作过程中，我们基本假设读者没有任何基础，内容涵盖了从什么是 HTML 到如何应用 CSS，再到查询数据库和使用 JavaScript 显示内容等所有方面。对于一些人来说，这意味着他们可能希望略过某些入门材料（并且肯定会错过很多蹩脚的笑话）。然而，即使是高级用户，也很可能从我们卷起袖子揭示的技巧中有所收获。

### 本书结构

我们将本书内容分为若干章节，并划分为三个“非正式”部分。

在**第一部分**，我们向你（第 1 章）介绍网络的基本语言：HTML、CSS、JavaScript 等。然后我们迅速进入两个应用（第 2-3 章），让你初窥门径，接着再退回来讨论设计自己的应用时可能需要解决的规划问题（第 4-6 章）。

在**第二部分**，我们开始增添一些亮点。我们深入讲解如何构建令人印象深刻的用户界面（第 7 章）以及处理视觉内容（第 8 章）。然后我们再向你展示另外两个应用（第 9-10 章），它们体现了移动应用的独特性：使用位置信息来引导你的应用（和用户），以及利用云服务获取信息和数据。

最后，**在最后一部分**，我们讨论为应用添加的下一级交互性。我们介绍了添加音频和视频（第 11 章），在用户不知情的情况下执行操作以提供强大功能（第 12 章），以及将所有这些整合起来，上传到网络或为原本局限于浏览器的创意构建一个完整的应用（第 13 章）。

虽然我们已将章节按逻辑顺序编排，但在第 1 章之后，你可以自由探索其余内容。虽然许多主题是相互关联的，但先阅读你感兴趣的内容可能有助于你更好地理解早期章节中你绝对想要深入了解的概念。同时，每一章都包含独立存在的信息精华，特别是关于设计、心理学和用户体验的讨论！希望你享受这段旅程！

## 下载代码

本书中示例的代码可在 GitHub 上获取，地址为：https://github.com/jonwestfall/Beginning-Android-Web-Apps-Development。

## 联系作者

我们总是很乐意收到读者的来信，如果你对本书（或一般生活）有任何问题、评论或想法，你可以通过我们的个人网站或社交媒体联系我们。

-   Jon Westfall：http://jonwestfall.com
    Rocco Augusto：http://nerdofsteel.com/
    Grant Allen：http://www.artifexdigital.com
-   Twitter：@jonwestfall
    Twitter：@therocco
    Twitter：@fuzzytwtr

# 第 1 章：利用移动 Web 的力量

欢迎阅读本书的第一章。在本章中，我们不仅要告诉你本书的内容，还将它与之前的情况进行比较。你看，很简单，尽管"网络"以某种形式在手机上存在了 10 年，但直到现在，移动网页应用和移动优化网站的真正力量才被认识到。

在我们展示为本书规划的精彩内容之前，最好先确保大家在术语上达成共识。因此，我们将从网页设计的基本术语开始谈起。在第二节中，我们将讨论当今移动 Web 的前身。最后，在最后一节中，我们将讨论指导本书的概念，并让你先睹为快我们即将开发的一些应用！

## 网页设计基础

有些概念最好先讨论一下。如果这些你以前都听过，请见谅。然而，如果你完全是网页设计的新手（即，你从未编写过一个网页或博客），那么这应该是一个很好的起点。而且，如果我们从头开始，那么我们应该从网络的通用语言开始：HTML。

### 入门：超文本标记语言（HTML）

在 20 世纪 80 年代末，我们今天称为 HTML 的计算机语言诞生了。HTML 本身不是一种真正的编程语言，因为它不被编译。相反，HTML 由一种称为**网络浏览器**的特殊软件进行解释。像台式机上的 Microsoft Internet Explorer、Mozilla Firefox 和 Google Chrome，以及 Android 设备上的 Dolphin HD、Opera Mini 和 Skyfire 这样的浏览器，会从**网络服务器**下载 HTML 文件，解释它们并显示它们。整个过程相当简单。网络服务器可以是任何类型的计算机，它通过一种称为超文本传输协议（HTTP，即网络地址开头的 http://，网络地址也称为 **URL**）的方式，将文件列表提供给网络上的其他计算机。浏览器通过 HTTP 下载这些 HTML 文件并读取它们，寻找称为**标签**的特殊元素。这些标签的功能与旧文字处理程序中的标签相同——指定文本和页面的其他元素在查看器中显示时应该是什么样子。看看图 1-1 中的网页。

这是普通文本。但是让我们变得花哨一些，让**这个加粗**（*这个是斜体*）。
左边的标签刚刚使这成为一个新行。

这里的左边标签刚刚使这成为一个新段落。

**图 1–1。** *一个名为 hello.html 的示例网页*

让我们看看构成清单 1-1 所示页面的 HTML 代码：

**清单 1–1。** *hello.html*

```html
<html>
<head>
<title>这是出现在浏览器标题栏中的文本！</title>
</head>
<body>
这是普通文本。但是让我们变得花哨一些，让<strong>这个加粗</strong>（<em>这个是斜体</em>）。
<br /> 左边的标签刚刚使这成为一个新行。
<p> 这里的左边标签刚刚使这成为一个新段落。</p>
</body>
</html>
```

代码可能看起来有点奇怪，但让我们逐行分析一下。第一行只是 <html>，让浏览器知道它正在读取一个 HTML 文档。你会注意到文档的最后一行 </html> 是类似的。这一行“结束”了 HTML 对象——关闭标签并告诉浏览器页面结束。通过拥有这样成对的标签，浏览器知道要应用哪些格式以及何时停止应用它。

代码的第二到第四行被称为页面头。这是程序员存储浏览器正确格式化页面所需的重要信息的地方。在这种情况下，我在头中放置的唯一标签是一个标题标签，它指定应该在用户网络浏览器的标题栏中显示什么。头通常是我们最常找到某些文档的地方，例如层叠样式表（CSS）、用于搜索引擎优化的 JavaScript 和 META 信息、针对不同浏览器的特殊指令、收藏夹图标（即浏览器中书签条目旁边出现的小图标），以及其他与文档内容无关的页面重要信息，这引出了第 5 行——body 标签。

body 标签告诉浏览器，即将提供要显示给用户的内容。从这里开始，我们看到纯文本——与图 1-1 所示渲染页面中的文本相同。但是，你会注意到我们添加了一些特殊的标签。第一个是 <strong>，它告诉浏览器，它与其结束标签 </strong> 之间的文本应该以粗体显示，以使其突出。



## 第一章：驾驭移动网络的力量

HTML 标签 `<strong>` 用于创建粗体文本，以增强视觉冲击力。第二个标签 `<em>` 通过强调内容或使内容变为斜体来实现相同效果。¹ 第三个标签 `<br />` 用于开始一个新行（br 代表换行！）。`<br />` 标签与大多数 HTML 标签略有不同。由于该标签不像 `<strong>` 和 `<em>` 标签那样需要包含页面上的内容，因此它自行闭合。最后，`<p>` 标签开始一个新段落。

从本质上讲，所有网页都是某种形式的 HTML，尽管我们将在本书中讨论的大多数网页要复杂得多。幸运的是，我们将引导你逐步了解，这样你就不会感到不知所措！

如果这是你第一次涉足 HTML 和网络应用的世界，那么在深入本书之前，最好先熟悉一下 HTML 的基础知识。互联网上学习 HTML 和浏览基本代码示例的最佳资源之一是 W3Schools (http://www.w3schools.com/)。一旦你对 HTML 有了一点了解，或者即使你已经非常熟悉，接下来也该学习本书中将要使用的一些更中级的网络应用设计和技术了。

### 获取样式：层叠样式表（CSS）

想象一下，你正在编写一个简单的网页来辅助你的家庭管理——一份家庭 chores 清单。它可能看起来像图 1–2 中的列表。

### 家庭 chores 清单

- **Tommy**：倒垃圾
- **Beth**：清理冰箱。
- **Mittens**：抓老鼠。

**图 1–2.** *家庭 chores 清单*

仅仅瞥一眼成品，似乎并没有太多内容。我们有一份标准的、乏味的黑白文档，完全缺乏任何风格或个性。让我们来看一看图 1-2 中展示的幕后代码（清单 1–2）。

**清单 1–2.** *chores.html*

```html
<html>
<head>
<title> Family Chore List </title>
</head>
<body>
<h1>Family Chore List</h1>
<ul>
<li><strong>Tommy</strong>: Take out the trash</li>
<li><strong>Beth</strong>: Clean out the fridge. </li>
<li><strong>Mittens</strong>: catch mice. </li>
</ul>
</body>
</html>
```

> ¹ 值得注意的是，你可能熟悉的 `<b>` 和 `<i>` 标签在 HTML 4 中用于与 `<strong>` 和 `<em>` 相同的目的。在 HTML5 中，它们已被弃用，转而使用上述标签。

让我们分解一下 body 元素中微小的代码片段。这里，页面上的无序列表是使用 `ul` 标签创建的。无序列表非常适合用于创建带项目符号的列表。如果你的列表需要更多的顺序，你可以选择使用 `ol`（或有序列表）HTML 标签。

虽然页面相当简洁，但你可能想让它更吸引人。也许在圣诞节期间，你想为你的家庭 chores 页面增添一些色彩，让最不情愿的精灵也会开心地微笑（见图 1-3）。

![圣诞节 chores 清单，绿色和红色增添了节日氛围](img/8b0ff5e51ddb912cd941bb18cf27206a_8_0.png)

图 1-3. 圣诞节 chores 清单，绿色和红色增添了节日氛围

在七月四日，你可能想让你的家人充满爱国热情（见图 1-4）。

![爱国 chores 清单，红、白、蓝三色](img/8b0ff5e51ddb912cd941bb18cf27206a_8_1.png)

图 1-4. 爱国 chores 清单，红、白、蓝三色

每次我们改变颜色，都是通过添加适当的标签来修改 HTML 源代码。看看清单 1-3 中 patriotic 版本的 chores.html。

**清单 1-3. patriotic chores.html**

```html
<html>
<head>
<title> Family Chore List </title>
</head>
<body bgcolor=blue>
<font color=red><h1>Family Chore List</h1></font>
<font color=white>
<ul>
<li><strong>Tommy</strong>: Take out the trash</li>
<li><strong>Beth</strong>: Clean out the fridge. </li>
<li><strong>Mittens</strong>: catch mice. </li>
</ul>
</font>
</body>
</html>
```

直接修改 HTML 对于小页面来说是可以的。然而，想象一下，如果有 12 个孩子和无数宠物需要协调，添加那些 font 标签会花费多少时间。或者，也许你有多个页面，每个孩子一个，你不想让他们因为兄弟姐妹有漂亮的颜色组合而他们没有，感到被冷落。别担心——我们可以使用一种叫做层叠样式表（CSS）的东西来保持一切有序。基本上，CSS 文件是一个由一组样式组成的小文档，这些样式应用于 HTML 文档，可以随时更改，影响连接到它的每个页面，而无需编辑原始 HTML 文档。清单 1–4 提供了一个 CSS 文件示例。

**清单 1–4.** patriotic.css

```css
body {background-color: blue}
h1 {color: white}
li {color: red}
```

请注意文件的格式只是你想要编辑的 HTML 标签（例如 H1）和你想赋予它的属性。在这种情况下，我们希望 h1 中的文本颜色为白色。我们可以简化 chores.html 以包含对此 CSS 文件的链接，如清单 1–5 中的代码所示。

**清单 1–5.** 引用 CSS 的 chores.html

```html
<html>
<head>
<title> Family Chore List </title>
<link rel="stylesheet" type="text/css" href="patriotic.css" />
</head>
<body>
<h1>Family Chore List</h1>
<ul>
<li><strong>Tommy</strong>: Take out the trash</li>
<li><strong>Beth</strong>: Clean out the fridge. </li>
<li><strong>Mittens</strong>: catch mice. </li>
</ul>
</body>
</html>
```

我们将得到与图 1–4 完全相同的输出。现在，想象一下当我们扩大规模时这是如何工作的。首先，父母不再需要直接编辑 HTML 标签来改变样式。根据节日的不同，他们可以简单地链接多个 CSS 文件（只需更改清单 1–5 代码中的第四行）。其次，他们可以进一步扩展 CSS，以指定间距、字体（Mittens 讨厌衬线字体）等。最后，如果他们有多个页面，他们只需在每个页面的顶部链接 CSS 样式表到当前“主题”，所有页面就会看起来一样。虽然上面的例子非常简单，但它们说明了 CSS 的强大功能。随着本书的继续，我们将更详细地研究 CSS！

### 获取交互：JavaScript

有时，优秀的设计不足以表达你的观点。有时你想做一些更炫酷的、独特的或非常实用的东西。最简单的方法之一就是使用 JavaScript。JavaScript 是一种在观众的网络浏览器中运行的脚本语言。例如，也许你以前访问过一个网站，并得到了如图 1–5 所示的弹出消息。

![JavaScript 警告](img/8b0ff5e51ddb912cd941bb18cf27206a_10_0.png)

**图 1–5. *JavaScript 警告***

通常，你会在填写表单页面或在线购物车时看到这些消息，告诉你你的商品缺货或类似烦人的信息。虽然你可能习惯在电脑的网页上看到这些消息，但它们也可以在移动网络浏览器中显示（见图 1-6）。

![Android 手机上的 JavaScript 警告](img/8b0ff5e51ddb912cd941bb18cf27206a_10_1.png)

**图 1–6. *Android 手机上的 JavaScript 警告***

创建这些消息的代码非常简单。清单 1–6 将代码集成到了我们在上面的 CSS 示例中看到的 chores.html 页面中。

**清单 1–6.** 引用 JavaScript 的 chores.html

```html
<html>
<head>
<title> Family Chore List </title>
<link rel="stylesheet" type="text/css" href="patriotic.css" />
<script type="text/javascript">
function ShowWarning() {
alert("Mittens - your mousing numbers are down this week - NO CATNIP FOR YOU");
}
</script>
</head>
<body onload=ShowWarning();>
<h1>Family Chore List</h1>
<ul>
<li><strong>Tommy</strong>: Take out the trash</li>
<li><strong>Beth</strong>: Clean out the fridge. </li>
<li><strong>Mittens</strong>: catch mice. </li>
</ul>
</body>
</html>
```

让我们从讨论 CSS 链接正下方、`head` 部分内的新代码段开始，它带有 `script` 标签。`script` 标签告诉浏览器，一段脚本代码（在这种情况下，类型为 `text/javascript`）即将被提供。然后浏览器解释代码。由于它在 `head` 部分，浏览器只是存储这段代码以备后用。这段代码被称为一个函数，你可以把它想象成一个包装在“快捷方式”中的命令列表。这里的命令是另一个名为 `alert` 的函数。如你所见，JavaScript 函数可能变得相当复杂，包括其他函数并与用户输入交互。

一旦函数被加载到浏览器的菜单中，我们需要告诉浏览器我们希望何时执行它。在这种情况下，我已经修改了 `body` 标签以包含 `onload=ShowWarning();` 行。这告诉浏览器，当页面加载时，我希望它运行 `ShowWarning` 函数。括号表示我可以包含传递给函数的信息的位置。这对于创建计算器或检查表单中的输入很有用。例如，我可以编写类似清单 1–7 的内容。

**清单 1–7.** 传递变量的引用 JavaScript 的 chores.html

```html
<html>
<head>
<title> Family Chore List </title>
<link rel="stylesheet" type="text/css" href="patriotic.css" />
<script type="text/javascript">
function ShowWarning(catname) {
alert(catname + " - your mousing numbers are down this week - NO CATNIP FOR YOU");
}
</script>
</head>
<body onload=ShowWarning("Mittens");>
<h1>Family Chore List</h1>
<ul>
<li><strong>Tommy</strong>: Take out the trash</li>
<li><strong>Beth</strong>: Clean out the fridge. </li>
<li><strong>Mittens</strong>: catch mice. </li>
</ul>
</body>
</html>
```



### 获取信息：可扩展标记语言（XML）

清单1–7中的代码将产生与清单1–6中的代码完全相同的消息。然而，在清单1–7中，我将猫的名字作为变量传递。函数ShowWarning现在期望我传递一个名为`catname`的变量，并且它可以在其代码中使用该信息。当我在body标签中调用ShowWarning()时，我只需添加猫的姓名以传递给函数。如果需要，我可以传递不止一个参数。如前所述，这可能会变得相当复杂，取决于我想要如何严厉地训斥可怜的小Mittens。

如您所见，将JavaScript与HTML和CSS结合使用可以生成外观良好、易于更新且能与用户交互的页面。但有时您可能需要生成一份不提供样式信息——仅提供一般信息——的文档。下一节给出了一个典型的例子，我们将开始进入奇妙的XML世界！

如果您花时间在网络上浏览，您可能会注意到某些页面上有一个奇怪的小图标，看起来像下面这样。

![RSS图标](img/8b0ff5e51ddb912cd941bb18cf27206a_12_0.png)

**图1–7.** *RSS图标*

这个小橙色图标向读者告知当前网站提供的RSS订阅源。RSS订阅源对用户来说看起来相当乏味且难以理解（请看图1–8中RSS订阅源的开头部分）。然而，其他网页和脚本可以利用它们从一个来源获取大量信息，并以不同的方式展示给用户。

```xml
<?xml version="1.0" encoding="UTF-8"?>
<?xml-stylesheet type="text/xsl" media="screen" href="~/d/styles/rss2full.xsl"?>
<channel>
<title>JonWestfall.Com</title>
<link>http://jonwestfall.com</link>
<description>More Than You Want To Know!</description>
<lastBuildDate>Thu, 16 Jun 2011 13:21:06 +0000</lastBuildDate>
<docs>http://backend.userland.com/rss092</docs>
<language>en</language>
<!--[generator="WordPress/3.1.3"]-->

<atom10:link xmlns:atom10="http://www.w3.org/2005/Atom" rel="self" type="application/xml" href="..."/>
<title>Keep your Android Tablet Up To Date Daily With Increased Battery Life!</title>
<description>Recently I found that I had a problem with my Samsung Galaxy Tab (Although you &lt;p&gt;&lt;a href="http://feeds.g.doubleclick.net/~a/EFFCCCh7JV-yrNNULTsPwYhvAs_A/0/da"&gt;&lt;img src="..."/></description>
<link>http://feedproxy.google.com/~r/jonwestfall/~3/FFCZ10Xe7kc</link>
</item>
```

#### 图1–8. 博客RSS订阅源的开头部分，显示了新条目

例如，图1–9是我个人博客RSS订阅源的开头部分。每个元素包含各种数据，看起来并不美观，但提供了所有可能希望使用称为RSS阅读器的特殊软件来查看我博客的信息。虽然某些应用程序（如Microsoft Outlook）内置了RSS阅读器，但许多人更喜欢使用专用的阅读器客户端。一个流行的RSS阅读器是Google Reader，它可以获取我的RSS订阅源链接，并生成我博客的精美视图，使Google Reader用户能够快速看到我最近发布的文章。

![Google Reader中的RSS订阅源](img/8b0ff5e51ddb912cd941bb18cf27206a_13_0.png)

#### 图1–9. 我的个人博客，在Google Reader中显示

现在，您可能会问为什么要让人们在其通常的网址之外的地方查看我的网站。简单的答案是，对于我的用户来说，在单个软件中查看他们阅读的所有博客（我的和其他人的）可能更为方便。诸如Google Reader之类的软件可以跟踪数百个RSS订阅源，从新闻来源、博客，甚至到像我的Twitter动态这样的简单状态更新。所有这些信息片段都由Google Reader以称为可扩展标记语言（XML）的格式获取。XML不是您希望人类观众看到的格式，但如果您在网页之间或Web服务之间共享信息，它是您会想要使用的格式。

虽然上面的例子展示了XML作为输出，但我的博客的Web应用程序（WordPress）生成XML以便其他网站（如Google Reader）可以使用它。XML也可以用作输入。例如，我可能想要获取数据（如体育比分）并显示在我的网页上。这些体育比分很可能以XML格式提供，我的网页可以打开并**解析**它。解析只是一个花哨的术语，意思是"读取、解释和显示"。我的网页将读取比分，必要时进行解释（即，计算某些内容、聚合某些内容），然后以某种有意义的方式向用户展示。

因此，总结一下，我们现在已经看到了如何构建基本网页，如何使它看起来漂亮（轻松地），以及如何使其与用户交互。最后，我们讨论了网页和程序如何通过使用XML在彼此之间获取数据。随着我们在本书中的深入，我们将详细讨论这些领域中的每一个，并为您提供大量如何使用它们的示例。事实上，在即将到来的第2章中，我们将讨论如何从非常流行的Web服务获取数据，并将其显示在我们要创建的第一个完整应用程序中！

### JSON：人类可读的数据交换

如果您有一个出色的移动Web应用程序创意，它依赖于其他服务（如Twitter或Foursquare）的应用程序编程接口（API），那么您很可能会很快接触到JSON（JavaScript对象表示法），这是我最喜欢的技术之一。

JSON是一种人类可读的、超轻量级的数据交换技术，基于JavaScript。基本上，它是一个JavaScript对象，可用于传输简单的数据结构和信息数组。在处理Web应用程序中的外部数据时，我已爱上JSON，因为它在与XML等其他技术相比时非常易用。不过，和所有技术一样，您的体验可能会有所不同。图1–10展示了JSON文档的外观示例。

![JSON格式示例](img/8b0ff5e51ddb912cd941bb18cf27206a_15_0.png)

**图1–10.** *Rocco Augusto在nerdofsteel.com上的JSON格式作品集*

### 移动Web的昨日与今日

我们许多人首次开始使用互联网是在20世纪90年代末，或者，如果您当时还未出生，也许您一生都在使用它！虽然我们对桌面上的互联网非常熟悉，但将它放到可以放入口袋的小屏幕上可能看起来有些奇怪，尤其是当涉及到Web时常听到的不同行话和营销话术。我们将从讨论数据到达手机的速度开始，然后讨论可以发送哪些类型的数据。

### 了解速度（或者"3G到底是什么？"）

通常，在最新智能手机的广告中，您会听到诸如"4G"或"比3G更快"之类的数字。"G"代表技术的代际。您很少听到2G，即第二代，这是有充分理由的。智能手机上数据的涌入恰好与第三代蜂窝网络数据标准的出现同时发生。然而，1G和2G确实存在，如果您拥有第一代iPhone（2007年发布），您只有2G速度，使用包括GPRS、EDGE和1X在内的协议。通过2G传输给您的数据大约只有拨号调制解调器的两倍速度，约115Kbps。因此，虽然电子邮件和基于文本的网页加载速度相当可以，但任何包含太多图像或多媒体的内容都需要大约 eternity² 的时间。

大约在2001年，我们认为的3G（或第三代）数据网络的初步设计被起草，理论上可以达到超过7Mbps的速度。这些网络包括UMTS、WCDMA和EV-DO等协议，可以比其2G对应物更快地传输数据。首次，这使得流媒体电影和音乐直接传输到手机成为可能。显示复杂网页的限制因素不再是数据连接的速度，而是手机的速度。到2007年，大多数电信运营商已经采用 cover 并"推出"了3G网络，移动宽带卡等设备也变得常见。

在过去的几年中（2008-2010年），当前3G技术的改进版本已经问世。虽然我们之前了解的3G技术与这种被称为"4G"的基于3G的新技术之间的确切差异存在相当大的争议，但显然，HSPA、HSPA+、WiMAX和LTE等新协议比其3 ancestor 更快。不幸的是，虽然所有主要运营商都在逐步推进其提高数据传输速度和网络容量的计划，但这些更新和变化不会立即对最终用户显现，直到他们购买具有合适内部硬件的手机以利用这些众多变化为止。

许多针对移动设备的Web开发者早期可能会陷入的一个常见陷阱是，速度是开发移动应用时唯一需要考虑的因素。如果我知道我的用户需要3G网络才能使用我正在开发的功能，我可能会忍不住跳过优化应用程序其他领域的工作，因为我知道我将拥有更快的数据连接。然而，如上所述，速度并不是唯一需要考虑的因素。设备的实际处理和软件能力（即其Web浏览器的功能）也可能减慢应用程序的速度。如果您想要证据，请使用您自己的智能手机或平板电脑连接Wi-Fi而非蜂窝数据，并观察某些网站和应用程序在连接到互联网时仍然会滞后，尽管连接通常比3G或4G更快。随着我们继续阅读本书，我们将讨论如何避免编写臃肿无响应的应用程序。

### 语言与协议的昨日与今日

现在我们知道了自己的速度，我们应该谈谈过去10年中网页是如何展示给手持设备用户的，以及移动世界的当前状态。

起初，手持设备（如最早的现代个人数字助理PDA）没有直接的互联网连接。这意味着任何内容

> ² 至少感觉上是那样的。



用户想要阅读的网络内容需要先下载，然后存储在设备上或进行缓存。其中一个非常流行的服务是AvantGo，它运营了大约十多年，最终在2009年关闭。虽然这些服务有些烦人（因为你需要定期将PDA与电脑进行物理同步以获取所需内容），但它们通常以一种非常基础且易于阅读的方式呈现内容。讽刺的是，这种呈现方式在当下又经历了一次复兴，因为用户在网上或忙于其他事务时（例如在工作中）发现内容并希望保存下来以便稍后阅读。一个流行的服务"稍后阅读"（http://readitlaterlist.com/）甚至有一个移动客户端，它以类似于1990年代末流行的旧式"离线缓存"系统的格式来显示这些保存的网页！图1-11展示了"稍后阅读"上的一篇缓存文章。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_17_0.png)

**图 1-11。** *安卓平台上的"稍后阅读"显示了一篇雅虎体育文章的缓存版本*

随着配备内置Wi-Fi无线电和智能手机的出现，用户可以直接连接到网页并查看其内容。然而，在直接访问互联网之前，许多电信公司提供的手机都配备了WAP浏览器。WAP，即无线应用协议，是一种极其简单的数据服务，允许用户通过简单的菜单导航来获取他们想要的信息。这些菜单通常是纯文本的，可能偶尔有一两张图片，设计上旨在快速提供基于网络的电子邮件、电影放映时间或天气信息等服务。带有WAP浏览器的手机实际上并没有连接到互联网，因为它们只能查看服务提供商放在菜单上的内容，但至少它们可以在有手机信号覆盖的任何地方查看内容，而不像下载内容离线阅读那样受限。

与WAP类似的概念是Java平台微型版，通常缩写为j2me。j2me允许用户在手机上加载小型Java小程序，这些小程序可以像WAP一样连接到特定服务，提供类似的体验。虽然j2me（Java平台微型版）在2-3年前就在手机上可用，与同样受欢迎的高通公司为功能手机设计的Brew MP操作系统并存，但它受到手机上可能存在的奇怪安全设置和预防措施的限制。奇怪的是，它在已经有可用网络浏览器的手机上也能使用，而这些浏览器可以访问任何网站。这不禁让人疑惑：既然可以直接访问移动版Gmail，为什么还要加载一个特殊的Gmail j2me小程序呢？

最终，大约到2005年，市场上大多数智能手机都包含了一个相当不错的网络浏览器，用户可以打开它，输入URL，并查看实际的网页。这些网页通常属于以下两种类型之一：被压缩到小屏幕上的普通网页（见图1-12），或专门为网站创建的移动版本（见图1-13）。两者各有优缺点。普通页面在小屏幕上通常看起来很糟糕，信息溢出屏幕，无法阅读，或者用技术术语来说，无法渲染（渲染是网页在浏览器中显示的过程）。虽然信息通常显示得很糟糕，但如果有足够的耐心和技巧，用户通常能找到他们需要的信息。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_18_0.png)

**图 1–12。** *我的个人博客，桌面视图，在移动浏览器中显示*

另一方面，移动版本通常更容易导航，因为它们是专为小屏幕设计的，使用HTML语言的变体，如XHTML或CHTML。这些页面看起来不错且非常易用，但通常缺乏特定内容。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_19_0.png)

**图 1–13。** *我的个人博客，在移动浏览器中以移动视图显示*

本书的目标是帮助你创建网站的移动优化版本，这些版本包含与桌面版本大致相同的内容，同时仍然保持可用性。正如你所料，那些发现你的页面易于使用的用户，会更有可能忽略一些缺失的部分。然而，那些需要20分钟（或者正如我们一位编辑指出的，20秒！）才能找到最新比赛比分或天气报告的用户，很可能会转向其他网站。

### 我们喜欢的概念——以及接下来的内容！

在我们结束本章时，我们想花点时间讨论一些我们喜欢牢记在心的指导原则，并希望你也能记住，不仅在阅读本书时，而且在开始编写自己的Web应用程序时也是如此。

### 概念一：像用户一样思考

思考一个你拥有的网站，一个你参与贡献的网站，或者仅仅是你经常访问的网站，然后问自己：当人们访问这个网站时，他们通常会做什么？答案可能很快就会出现。然而，更深入地思考这个答案有多"普遍"可能更有价值。

例如，我的一个朋友最近在《赫芬顿邮报》上发表了几个博客帖子，该网站以评论发布速度快且直言不讳而闻名。当他发给我他文章的链接时，我打开并通读了一遍。读完后，我关闭了浏览器，继续做我的事情。那周晚些时候，我的朋友问我是否看了那篇文章，在我回答看了之后，他问"你觉得那些评论怎么样？"答案很简单。我根本没怎么想那些评论，当然也没有花时间去读。然而，在他看来，因为评论是对他自己作品的反馈，所以评论本身比文章更有趣（毕竟，对作者来说，他们自己的作品似乎相当熟悉且不那么有趣）。现在想象一下，如果我的朋友设计了发布他作品的网站，当你看到用户评论被突出显示，甚至可能显示在文章旁边或其他地方而不是底部的小字体时，你可能不会感到惊讶。对我的朋友来说，"平均"用户会对评论比对文章更感兴趣，而事实上，情况很可能恰恰相反。

值得庆幸的是，我的朋友不是程序员。但作为程序员，我们必须密切关注用户如何使用我们的网站或应用。如果我们把所有注意力都放在用户认为微不足道的功能上，而忽略用户认为必要的核心功能更新或增强，我们可能会大量失去这些用户。

### 概念二：不要惹恼用户

我能给出的关于概念二的最好例子来自于"盈利"这个邪恶的词汇，或者简单地说就是"嘿，我做了很多工作，我想以法定货币的形式获得某种形式的回报！"盈利通常来自销售广告；这是用户理解的生活现实。如果你想要免费的东西，你可能会接受偶尔会看到广告以保持其免费。大多数人认为这比付费获取内容更可取，事实上，许多出版商报告称通过广告赚取的收入超过了销售付费产品的收入！

然而，仅仅因为你向人们做广告，并不意味着你需要把广告塞到他们脸上！你需要使用有品位的广告，激发用户兴趣的广告，以及不会惹恼用户的广告。在每段文字或每页的顶部、侧面和底部都放置广告很少有效果。

同样，不必要的内容或特效也可能惹恼用户。例如，最近我遇到一个页面，它使用了一个特殊的登录按钮，按钮有漂亮的凸起边缘，在我的桌面浏览器上看起来不错。然而，在我的安卓智能手机上，浏览器感到困惑：这是一个按钮还是一张图片？当我点击它时，没有任何反应。最后，通过一个非常奇怪的点击、轻微按住并移动手指的动作，我才成功登录。如果页面作者做了以下任何一件事，这个问题本可以得到解决：

-   用移动浏览器测试页面
-   使用标准的网页表单按钮

在这个例子中，形式优先于功能。别误会，只要不影响可用性，花哨的设计是可以的。

### 概念三：重测信度

在我（乔恩）的日常工作（兼职）中，我研究个体如何做决策以及这些决策的影响。在我的研究生涯中，"重测信度"这个概念意味着，对一个给定任务进行一次测试的结果应该与第二次（以及随后的）测试结果相同。我将从研究方法论中借用这个概念来讨论关于测试你内容的一个观点。

与概念一类似，用户都是不同的。他们的设置大多与你在设计网页或应用时所使用的略有不同。例如，现在我使用的是一个27英寸的显示器，作为设计师我觉得这非常有用，但我不指望大多数人都拥有。因此，如果我设计一个网页，我可能不应该假设人们的浏览器窗口像我现在这样是1565像素宽、912像素高。在处理较小的屏幕时，这一点变得尤为重要。一些安卓手机和平板电脑屏幕相对较大，而另一些则较小。在各种设备上（或许在朋友的帮助下）测试你的应用或网页，可以确保你的用户每次访问网站时都能获得最佳和最优化的体验。还必须小心重复访问，因为浏览器可能会缓存应该更新的内容。另一方面，我们将在后续章节中重点介绍的一些技术会利用模板或框架，使浏览器缓存成为你的朋友。这些技术会重用用户已经下载的内容！

### 概念四：保持简单，愚蠢！

如今，走在街上，你总会看到一些父母把智能手机塞到蹒跚学步的孩子面前，以让他们在长途汽车旅行或在商店里有事可做。在这个基于神奇触摸、支持互联网的手机和平板电脑时代之前，在这个（我，罗科）也喜欢称之为"时间之前的时间"的宽带互联网时代之前，能够参加一个基础的计算机课程被认为是一种巨大的特权。这是小学里期望学生做的事情之一，如果他们高中毕业时想从事任何与电子表格相关的成功工作的话。

我每周都和父亲一起虔诚地看《星际迷航》，你可以想象当我上六年级终于能够参加第一堂正式的计算机课时，我是多么欣喜若狂。我是说，拜托！你怎么可能不想像斯科蒂那样，在电脑上几秒钟就调制出透明铝的配方呢？而就在一秒钟前，你还在对着鼠标说话，试图给它语音指令



## 第一章：驾驭移动网络的力量

    命令？！这就是为什么在开学前的那个整个夏天，我都泡在图书馆里，查阅所有能找到的计算机书籍，为即将到来的计算机入门课做准备。然而，当我了解到计算机世界并不像《星际迷航》和所有带有电脑黑客的电影所描绘的那样光鲜亮丽、激动人心时，那份兴奋很快变成了失望。那门课我学到的最多不过是如何复制《比佛利山警探》主题曲并存到软盘上，以及如何打开一个 HyperCard 应用程序（尽管奇怪的是，我们从未学过如何编写一个 HyperCard 应用程序。）

    尽管第一年令人失望，但它成为了我执着/痴迷于计算机的催化剂，促使我在七年级时再次报名参加了一门计算机课。我未曾想到，这门计算机课，这每天仅占我生活一小时的微小片段，最终引领我踏上了一生的痴迷之路。要知道，那一年，AOL 开始在美国真正流行起来。最重要的是，HTML 2.0 在那一年诞生了。当时的老师预见到了这项技术的走向，并拥抱了一个信息自由交换的未来愿景。每天在课堂上，他都会反复强调，总有一天，“创建互联网页面的人”（这是在 Web Developer 这个术语出现之前）的收入会像医生和律师一样高，价值和重要性也将不相上下。当然，我们都认为他是个疯老头，但他对所预见未来的热情足以让我着迷，最终我也开始相信并宣扬它。他对此愿景深信不疑，以至于我们全年唯一的作业就是创建整个学校网站。

    在从那门课学到的所有东西中，最重要的规则是 KISS 原则，即“Keep it Simple Stupid”（保持简单，笨蛋）的首字母缩写。尽管我很爱这位老师给予我的知识，但不可否认他是个脾气暴躁的老混蛋。每次我们为学校网站提出绝妙的点子，比如添加动画 GIF 火焰和 Beavis and Butthead 的小精灵图时，他总会说“保持简单，笨蛋！”。虽然小时候不断被泼冷水、几乎每天都被说成白痴很烦人，但这对培养我耐心和克制的艺术却大有裨益。它让我意识到，尽管功能 X、Y 和 Z 在任何我正在做的项目上都会很棒，但更重要的是先把它们放在次要位置，以便我能集中精力编码和交付功能 A、B 和 C。现在，当我做一个项目时，我会坐下来，仔细规划出启动项目所需的一切。我会把那些非必需的、很酷的额外功能想法先搁置一旁，以便在手头任务不会让我分心时再处理它们。

    无论你是谁，无论你设计或开发了多长时间，有一件事始终是真理。任何项目最难的部分就是启动它。你项目中那些并非必需但因为很酷而最终添加的特性越多（例如，给改装车添加火焰让它跑得更快），你就越难决定从哪里开始你的项目以启动它。所以请记住，无论你刚刚想到的主意有多不可思议，如果它对于启动你的项目并吸引兴趣并非绝对必要，那么在现阶段把它加入项目之前，请三思。把这个想法记在脑子里或纸上，稍后再来处理。Twitter 就是一个完美的例子。几年前 Twitter 发布时，它是一个非常简陋的程序，基于一个非常简单的想法：“你现在在做什么？”随着时间的推移，更多新的、令人兴奋的功能根据需要被添加进来。Twitter 已经从一个告诉你午餐吃了什么的小网站，发展成了一个备受关注的网络应用程序，它曾报道了迈克尔·杰克逊去世这样的重大新闻事件，甚至在内战期间将信息从缺乏互联网的国家中传出，发挥了至关重要的作用。

    请记住，罗马不是一天建成的。它是一个不断演变的帝国，每天都在自身基础上发展壮大，你应该以同样的方式看待你的下一个网络项目。从小处着手，在力所能及的范围内逐步添加，同时避免让自己不堪重负。本质上——*保持简单，笨蛋！*

## 下一步内容

    既然我们已经讨论了网页设计的要素、缩写、奇闻轶事和概念，让我们稍微谈谈你在本书中将会发现的内容。

    从下一章开始（就在几页之后！），我们将利用当今网络上最受欢迎的服务之一——Twitter，来开发一个简单的应用程序。Twitter 是一个很棒的网络现象，所以我们将在第三章继续用它构建另一个小型应用程序。然后我们会退一步，从更宏观的角度来看待问题——比如你如何从头开始开发一个应用（第四章），以及如何处理不同的屏幕分辨率和浏览器平台（第五和第六章）。在第七章，我们将展示 jQuery Mobile——重要的是，向你展示如何用它让你的应用看起来专业且“漂亮”。第八章将继续这个主题，展示一些在用户界面设计中可以使用的优秀资源。解决这些之后，我们将尝试基于位置和基于云的应用程序，最后以讨论使用音频和视频、Ajax，以及准备让你的产品“发布”来结束本书。有很多内容要涵盖，但我们知道你能应付这次旅程！另外，如果你还没注意到，我们的模式是先通过示例给你大量信息，然后再回到更像教科书式的叙述中。这样，希望你能在阅读这本令人心跳加速的计算机书时保持投入！（好吧，这有点讽刺，但我们真心希望这种方法能让阅读变得“有趣”。）

    那么，事不宜迟，让我们从我们的第一个应用开始吧！

## 第二章：Twitter 应用程序：那是谁发的推文？

    既然我们已经介绍了本书中将要学习的内容，现在是时候动手实践，创建我们的第一个移动网络应用程序了。这两个应用程序都非常简单，它们与 Twitter API 交互。API，即应用程序编程接口，是一个根据用户提供的一组规则或参数，用于与特定应用程序交互的接口。通常，人们会使用 API 来从应用程序的基础设施中收集和解析数据，而无需直接连接到应用程序的数据库来获取该信息。

    我们将构建的第一个应用程序是“那是谁发的推文？”，它将解析一个小型的预定义认证 Twitter 用户列表，并在页面上显示一条随机推文，以及一个包含四位可能发布该推文的候选人的列表。

    我们将构建的第二个小型网络应用程序叫做“我爱火腿”，它同样将借用 Twitter 的数据洪流，为移动用户创造一种快速有趣的娱乐形式。“我爱火腿”将专注于非常基础的游戏机制。系统会向用户呈现两个预定义的押韵 Twitter 搜索供选择。如果他们选择的 Twitter 搜索返回的结果最多，那么他们就是赢家。这两个移动网络游戏都将严重依赖 HTML5、JavaScript，以及一项名为 JSONP 的出色技术。

    在本章中，我们将在你自己的个人电脑上搭建并运行开发环境（可以把它想象成你自己的迷你互联网，它会连接到真正的互联网上的 Twitter，但大部分时间只在你的电脑上运行），并讨论“那是谁发的推文？”应用程序。在下一章，我们将继续讨论“我爱火腿”应用程序。让我们开始吧！



## 第2章 Twitter 应用：这条推文是谁发的？

## JSONP

你可能还记得我们在第一章中讨论过 JSON。JSON 是一项出色的技术，如果你在过去几年中从事过 Web 开发领域的工作，那么你可能已经遇到过它一两次。如果你在过去一天内浏览过网页，你可能也遇到过使用它的网站！如果你曾经使用过 Flickr、Twitter 或 Gowalla 的 API，那么很可能你对 JSON 也非常熟悉。对于那些完全跳过第一章的人来说，JSON 是一种人类可读的轻量级数据交换技术，也是一个开放标准。作为一项技术，JSON 相当年轻，其使用最早可追溯到世纪之交后不久，JSON.org（http://www.json.org）网站于 2002 年上线。

如果你熟悉 JavaScript 的使用和对象的创建，那么 JSON 对你来说应该相对熟悉。然而，JSON 不应与 JavaScript 对象混淆，因为它们并不相同。尽管我非常喜爱 JSON，但有一个小小的、烦人的问题，大多数开发者在花费数小时 prematurely 地抓耳挠腮、让自己变秃之前都不会意识到，那就是一个非常讨厌的、微小的、棘手的东西，叫做跨域脚本。

要理解什么是跨域脚本以及为什么浏览器中有硬性规则阻止你执行它，你首先必须了解什么是跨站脚本攻击（XSS）。XSS 是网站和应用程序中的一种漏洞类型，允许攻击者或入侵者将他们自己的脚本和内容注入到网站或系统中。入侵者可能利用 XSS 漏洞向你的服务器上传一个脚本，使他们能够在你自己的浏览器中模拟 Bash shell（一种常见的 UNIX shell 或命令行界面），或者更糟糕的是，可能利用该漏洞从你的数据库中窃取数千个用户名和密码。

由于这些顾虑，在大多数情况下，你的浏览器不会从你网站服务器之外的域加载 JSON 数据。为了获取和使用该数据，必须在页面加载之前在后端服务器端获取，然后提供给用户。这似乎不是什么大问题，直到你开始构建拥有成千上万用户的应用程序。那时，解析外部数据最终会影响服务器的性能。为了解决这个性能问题并将部分外部数据解析需求委托给最终用户，我们将使用 JSONP 或"带填充的 JSON"，它将允许我们的应用程序请求我们需要的 JSON 数据，因为它将被包装（或填充）在 JavaScript 对象中。

## 设置你的开发环境

在开始编码之前，我们需要设置一个开发环境。为了简单起见，我假设我们使用的是基于 Windows 的操作系统，因此我将只介绍设置基本 WAMP（Windows、Apache、MySQL 和 PHP）服务器以测试我们代码的步骤。我知道不是每个人都使用基于 Windows 的系统，但如果你使用的是 Linux 或 OS X，那么你可能已经熟悉如何设置 *AMP 环境进行测试。

对于我们的测试环境，我们将使用名为 Uniform Server（http://www.uniformserver.com/）的开源免费 WAMP 服务器。你可以从其网站下载该 WAMP 服务器。我使用的版本，以及本章截图中显示的版本，将是"7.1.2–Orion"。

设置测试环境相当简单。只需找到你从网站下载的文件，运行自解压 EXE 文件。完成后，打开文件夹。在运行服务器之前，我想介绍一下 Uniform Server 团队包含的几个有用的程序，以使我们的生活更轻松。第一个应用程序叫做 Pre-Check（Run_pre_check.exe）。<sup>1</sup> 让我们运行这个应用程序，并查看图 2–1 中的结果。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_26_0.png)

**图 2–1。** *Uniform Server 的 Pre-Check 应用程序显示端口 80 和 443 当前正在使用中*

正如你所看到的，如果我现在尝试运行服务器，它会失败。我目前打开了 Skype，它正在运行经典的 HTTP 端口（端口 80 和 443），而我需要这些端口来运行服务器。网络中有一个程序对应一个端口的规则，所以我们需要做一些简单的调整。虽然你可以编辑一些配置文件来更改将要使用的端口，但为了简单起见，我将直接关闭 Skype，以便我们可以在默认设置下运行。

现在我们已经释放了端口，我们可以运行"Start.exe"应用程序，该程序将打开并在系统托盘中放置一个图标。右键单击系统托盘中的 Uniform Server 图标。它看起来像一个带有数字 1 的蓝色方块，如下面的图 2–2 所示。选择菜单顶部的"Install and Run All Services"选项。现在，如果你打开 Web 浏览器并指向 http://localhost/，你应该会看到默认的 Uniform Server 起始页面（localhost 只是你当前正在使用的计算机的另一个名称，IP 地址 127.0.0.1 也是如此）。

> <sup>1</sup> 在 Windows 中，你可能需要以管理员身份运行此命令和其他命令。为此，右键单击该命令并选择"以管理员身份运行"。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_27_0.png)

现在我们的服务器已经启动并运行，我们*几乎*可以开始编写一些代码了。最后一件事是熟悉服务器的默认 WWW 根文件夹。如果你打开提取 Uniform Server 的文件夹，你会看到一个名为 www 的文件夹（见图 2–3）。你放置在此文件夹中的任何内容都将对通过浏览器查看你网站的任何用户可见。由于我们将使用自己的项目文件，你可以随意删除此文件夹中的所有内容以重新开始。稍后，你在设置生产服务器时可能会用到这些文件。然而，出于开发目的，它们并不需要。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_28_0.png)

**图 2-3。** *将容纳你应用程序项目文件的默认 WWW 文件夹视图*

现在你已经成功设置了用于本地开发的 Web 服务器并清理了根文件夹，是时候开始编码了！如果你需要任何关于 Uniform Server 的帮助，或者只是想更深入地探索一下你可以用这个服务器做什么，你可以运行 Uniform Server 目录中的"help.bat"批处理文件，这将为你提供一些非常详尽的文档（见图 2-4）。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_28_1.png)

**图 2-4。** *Uniform Server 快速帮助文档*

## 你的第一个移动 Web 应用程序

给自己倒杯咖啡，做一点伸展运动，因为现在是时候开始编码了。我们构建的第一个应用程序"Who's That Tweet?"将是一个小巧简单的游戏，它收集了一批经过验证的 Twitter 用户和名人，并随机显示他们的一条推文。然后，用户将看到一个包含四个可能创建了那条 Twitter 帖子的 Twitter 用户的列表。如果最终用户选择了与那条帖子匹配的正确 Twitter 用户，那么他们将获得 100 分加到他们的分数中，并进入下一条随机帖子。如果没有，他们将看到一个视觉提示，表明他们的猜测能力不足，并将进入下一条随机的 Twitter 帖子。

我们要做的第一件事是为我们的游戏创建一个非常基本的 HTML 布局，或者说基础。之后，我们将使用一些 CSS3 为那个平淡的骨架布局添加样式，一旦它看起来漂亮了，我们最终会编写 JavaScript，这将在我们的第一个移动 Web 应用程序中将一切联系在一起。

### HTML

清单 2–1 包含了我们游戏的基本 HTML。

**清单 2–1。** *Who's That Tweet? 的基本 HTML*

```
<!DOCTYPE HTML>
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content=" initial-scale=1.0; maximum-scale=1.0; minimum-scale=1.0; user-scalable=0;" />
<title>Who's That Tweet?</title>
<link href='http://fonts.googleapis.com/css?family=Droid+Sans&v1' rel='stylesheet' type='text/css'>
<link rel="stylesheet" type="text/css" href="css/style.css">
<script type="text/javascript" src="js/jquery-1.6.1.min.js"></script>
<script type="text/javascript" src="js/main.js"></script>
</head>
<body>
    <header>
        <div class="score"><strong>Score:</strong> <span>0</span></div>
        <h2>Player 1</h2>
    </header>
    <section>
        <div id="tweet">
            <div class="avatar"></div>
            <div class="content"></div>
        </div>
        <ul></ul>
    </section>
</body>
</html>
```

页面的 HTML 标记非常平淡和基础。从 head 元素开始，你可能会注意到与标准基于桌面的 Web 开发略有不同的是 viewport 元标签的包含。viewport 元标签是移动 Web 开发的关键要素，它允许你控制移动浏览器视口的大小和缩放。

Web 开发中使用带有 `name="viewport"` 的 meta 元素。此元素在移动设计与开发中至关重要，我们将在第 10 章详细探讨。通过它，你可以控制用户是否能缩放页面内容，甚至能限制缩放程度。此处我们将视口缩放设为默认值，并禁用了用户手动缩放的选项，从而避免用户因误触屏幕导致页面意外缩放而影响体验。

进入 `body` 元素后，你可能会注意到我们使用了多个“新式”HTML5 元素，例如 `header` 和 `section`。`header` 作为语义化标签，专门用于标识页面或网络文章的头部区域。在我们的页面头部中，它被用来容纳玩家当前分数（我们将通过 JavaScript 在每轮游戏后更新）和玩家名称。为保持演示简洁性，我们将玩家名默认设为“玩家 1”。

接下来是 `section` 元素，它用于承载示例的主要内容。与 `header` 类似，`section` 是 HTML5 引入的语义化标签，专为标记文档或页面的区块而设计。在旧式 xHTML 时代，我们通常需要堆砌大量 `div` 标签来划分页面区块，这会让搜索引擎和视障人士使用的屏幕阅读器感到困惑。现在通过合理运用 `section` 标签，搜索引擎和屏幕阅读器能更轻松地判断页面中哪些信息需要被朗读或索引。

在页面主要内容区域内，我们放置了一个 ID 为 `tweet` 的 `div` 容器，用于显示从认证用户数组中随机抽取的推文，同时还有一个空的 `ul`（无序列表）元素，将容纳四个随机展示的认证 Twitter 用户信息。

在 `#tweets` 容器内部，我们看到两个 `div` 容器：`.avatar` 和 `.content`。对于不熟悉 CSS 的读者，本书中当涉及代码时出现井号（#）表示引用元素的 ID；而通过 class 属性引用标签时会使用点号（.）前缀，例如上方的 `.avatar`。

基础结构已搭建完成，现在进入我最喜欢的环节之一——用 CSS 为页面添加样式！

### CSS 部分

上一章我们讨论了 CSS，本章将通过实践深入学习。如果暂时无法完全理解，请不要气馁，我们将在后续章节逐步展开讲解。

这里的 CSS 不会使用过于复杂的技巧，但我们会充分利用 Android 的 Webkit 渲染引擎，运用近几年流行的 CSS3 新特性。首先进行基础的样式重置和全局布局设置，然后逐段解析 CSS 文件。在代码清单 2-2 中，我们将梳理页面的基础 HTML 元素，重置它们的外边距（margin）和内边距（padding）——即页面元素间的间距，同时重置全文档的字体尺寸和字体类型。

#### 代码清单 2-2. Who's That Tweet? CSS 文件 – 第一部分

```css
/*** 重置样式 ***/
html, body, header, section, div, p, ul, li, h2 {
    margin:0;    padding:0;
}
ul, li {
    list-style:none;
}

/*** 全局样式 ***/
html, body {
    width:100%;
    overflow-x:hidden;
}
body {
    font-size:14px;
    font-family: 'Droid Sans', Arial, Helvetica, sans-serif;
    background:#06c;
}
h2 {
    font-size:14px;
}
```

如果你有过 CSS 编写经验，这段基础样式代码应该非常熟悉。我们首先将多个页面元素的内外边距重置为零，确保无论在何种 Android 设备上，页面样式都能精确定位。考虑到 Android 平台的快速迭代（每年发布两次以上新版本），这点尤为重要。

接下来我们移除了无序列表（ul）和列表项（li）可能自带的项目符号，并设置页面默认字体、字号以及应用背景颜色。

最后我们要使用“Droid Sans”网络字体。近年来随着 Web 技术的发展，设计师和开发者一直在呼吁寻找更简便的方式来使用那些在印刷广告中屡见不鲜的精美字体。毕竟，谁愿意整天盯着 Arial 或 Times New Roman 呢？CSS3 的一项革命性特性就是支持 True Type 字体。从此你不再需要依赖压缩质量低劣的图片或侵入性极强的 Flash 方案来实现优美的排版效果。

Google 甚至贴心地为我们创建了一个免费开放的网络字体库。你可以访问 Google Web Fonts 网站：http://www.google.com/webfonts。找到心仪字体后，Google 会提供 HTML 代码片段，将其添加到页面布局中即可加载字体，然后在 CSS 文件中调用——就像我们在这里将“Droid Sans”设为页面默认字体一样（参见图 2-5）。

![图 2-5. 在 Google Web Fonts 网站查看 Droid Sans 字体](img/8b0ff5e51ddb912cd941bb18cf27206a_32_0.png)

#### 代码清单 2-3. Who's That Tweet? CSS 文件，第二部分

```css
/*** 头部区域 ***/
header {
	width:100%;
	font-weight:bold;
	text-transform:uppercase;
	text-shadow: 1px 1px 1px rgba(255,255,255,0.5);
	line-height:40px;
	background-image: -webkit-gradient(
		linear,
		left bottom,
		left top,
		color-stop(0, rgb(135,135,135)),
		color-stop(0.8, rgb(201,201,201))
	);
	-webkit-box-shadow:0 0 15px rgba(0,0,0,0.5);
	box-shadow:0 0 15px rgba(0,0,0,0.5);
}
header h2 {
	margin-left:10px;
}
.score {
    float:right;
    margin-right:10px;
}
```

CSS 的 HEADER 部分让我们有机会体验 CSS3 的魔力。在 CSS3 普及之前，若要创建渐变背景区域，必须依赖图形设计软件制作图片并拼接。而现在如同魔法般，只需几行看似复杂的 CSS 代码，就能实现与 Photoshop 相同的渐变效果。在这些新潮渐变之上，我们只需一行 CSS 代码就能为头部添加阴影效果。简直像魔法！

代码清单 2-4 可以说是 CSS 文件的核心部分，包含了让页面焕发生机的主要样式属性。

#### 代码清单 2–4. Who's That Tweet? CSS 文件，第三部分

```css
/*** 内容区块 ***/
section {
    margin:20px 10px;
    padding:10px;
    border-radius:7px;
    background:#aaa;
    -webkit-box-shadow:0 0 20px rgba(0,0,0,0.5);
    box-shadow:0 0 20px rgba(0,0,0,0.5);
}

section.fail {
    background:#990000;
    color:#fff;
}
section.win {
    background:#009900;
    color:#fff;
}
section.fail li, section.win li {
    border-bottom:1px solid #fff;
}
section.fail li:first-child, section.win li:first-child {
    border-top: 2px groove #fff;
}
section #tweet {
    width:100%;
    margin-bottom:10px;
    padding-bottom:10px;
}
section .avatar {
    float:left;
    width:48px;
    height:48px;
}
section .content {
    margin-left:58px;
    min-height:48px;
}
```

## 清单 2–4. 这是谁的推文？CSS 文件，第二部分

```
section .person {
    margin-left:42px;
}
section ul {
    width:100%;
    clear:both;
}
section li {
    margin:0;
    padding:5px 5px 5px;
    height:32px;
    line-height:32px;
    border-bottom:1px solid #666;
}
section li .avatar {
    width:32px;
    height:32px;
}
section li .avatar img {
    width:32px;
    height:32px;
}
section li:first-child {
    border-top: 2px groove #666;
}
```

CSS的`section`部分，就像之前的HTML文档一样，是大部分魔法发生的地方。你应该首先注意到的是CSS3的另一个由权能者创造的新颖特性，旨在让我们的生活更轻松——`border-radius`。现在，我们不再需要花费数小时试图正确拼接图像以在文档中获得圆角，或者更糟的是，依赖臃肿的JavaScript库来满足我们的圆角需求，我们可以将这项工作交给浏览器的渲染引擎，然后就完成了。

这里我们利用`border-radius` CSS属性为我们的`section`容器赋予一个漂亮的现代智能手机外观，然后再用一个漂亮的阴影效果来点缀它。之后，我们为`.win`和`.fail`类定义了两组样式，我们将在每一轮通过JavaScript调用它们，作为用户选择是否正确的视觉指示。

图2–6、2–7和2–8分别显示了我们的游戏视图、选择错误后的视图和选择正确后的视图。现在，让我们了解一下产生用户反馈视图所需的JavaScript。

# 第2章：Twitter应用：这是谁的推文？

![](img/8b0ff5e51ddb912cd941bb18cf27206a_35_0.png)

图2–6. 这是谁的推文？在Android 2.3网页浏览器中运行

![](img/8b0ff5e51ddb912cd941bb18cf27206a_35_1.png)

图2–7. 这是谁的推文？在未能选择推文的正确所有者后的显示

图2–8. 这是谁的推文？在选择了正确的推文发布者后的显示

## JavaScript

现在我们已经完成了页面的布局和样式，是时候用一些JavaScript让它动起来了。本书中所有的应用演示都将使用jQuery JavaScript框架。如果你不熟悉jQuery，它是一个出色的JavaScript库，在全球范围内被广泛使用，与过去Internet Explorer 6占主导地位的时代相比，它使得跨平台JavaScript开发变得轻而易举。

这里有一点JavaScript，所以我会像之前处理CSS那样将其分解开，一次解释一部分的内容。在编写这个演示时，我添加了一堆有用的注释，这应该能进一步帮助我们中新的开发者理解正在发生什么。

清单2–5将带领我们了解一组将在应用程序中使用的默认变量，以及一个包含一些Twitter最受欢迎的经过验证的用户的非常充实的数组。

### 清单 2–5. 这是谁的推文？Javascript 文件，第一部分

```
/**
 * Who's That Tweet
 * @author: Rocco Augusto
 * @file: js/main.js
**/

/* 此数组包含一个经过验证的
Twitter账户列表，我们将使用它来为每一轮拉取随机推文 */
```

```
var defaultIcon = 'https://sio.twimg.com/sticky/default_profile_images/default_profile_3_normal.png';
var currentRound = [];
var correct = '';
var tweets = [
    'jimmyjohns',
    'sugarsammyk',
    'wilw',
    'JeriLRyan',
    'pattonoswalt',
    'trutriciahelfer',
    'AndrewWK',
    'ChristianKane01',
    'charliesheen',
    'levarburton',
    'edwardjolmos',
    'Rosie',
    'kevinrose',
    'jason',
    'leolaporte',
    'aplusk',
    'StacyKeibler',
    'LilianGarcia',
    'nicolerichie',
    'rainnwilson',
    'ericschmidt',
    'pennjillette',
    'nerdist',
    'Scobleizer'
];
```

这里我们定义了几个将在整个应用程序中使用的全局变量。第一个是`defaultIcon`变量，它包含我们在整个脚本中使用的默认用户Twitter头像图片的长URL。我们本可以不使用这个变量，只在需要时将代码添加到脚本中，但在编码时，将尽可能多的代码缓存以供重用始终是一个好的实践。现在，当我们想在脚本的任何地方添加`defaultIcon`时，我们不必记住一个又长又复杂的URL，在大多数情况下，这会在视觉上使我们的代码变得混乱。

接下来，我们创建一个名为`currentRound`的空数组，它将包含我们从Twitter为当前轮次拉取的所有数据。我们创建了一个预先定义的经过验证的用户数组，以便随机选择。对于这个列表，我只是在Google上搜索了经过验证的Twitter用户，并复制了我在Google搜索结果第一页上找到的所有用户的名称。

如果这是一个基于Twitter API的真实游戏，而不是演示，我们可能希望利用一个在线服务器和所有经过验证的Twitter账户的列表，但是，由于我们是从零开始，一个数组现在就能很好地工作。

清单2–6显示了这是谁的推文的主JavaScript文件的第二部分。

### 清单 2–6. 这是谁的推文？Javascript 文件，第二部分

```
// 此函数将从tweets数组中获取一个随机用户。
function getRandom() {
    var l = tweets.length;          // 获取tweets数组的长度
    var ran = Math.floor(Math.random()*l);    // 获取随机用户

    // 检查随机选择的用户是否已在列表中
    if(currentRound.indexOf(tweets[ran]) == -1) {
        if(currentRound.length == 0)
            correct = tweets[ran];  // 将第一个随机用户设为正确用户

        // 将随机用户推入currentRound数组
        currentRound.push(tweets[ran]);

        // 再获取三个额外的随机用户
        if(currentRound.length < 4)
            getRandom();
    }
    else {
        // 如果随机用户已在列表中，则重新开始
        getRandom();
    }
}
```

在清单2–7中，我们的下一个函数将遍历并从我们的`tweets`数组中选择一个随机用户，然后获取另外三个随机用户供用户选择，如`getRandom()`函数所示。在这个函数中，我们使用JavaScript的`Math`对象来完成选择随机用户的繁重工作。

### 清单 2–7. 这是谁的推文？Javascript 文件，第三部分

```
// 获取currentRound数组中用户的头像
function buildQuiz() {
    var l = currentRound.length;
    for(i=0;i<l;i++) {
        $.getJSON('https://twitter.com/status/user_timeline/' + currentRound[i] + '.json?count=10&callback=?', function(data) {
            var img = data[0].user.profile_image_url;
            var name = data[0].user.screen_name
            var h = '';

            // 创建将注入到游戏屏幕中的HTML
            h += '<li rel="' + name + '">';
            h += '   <div class="avatar"><img src="' + img + '" alt="" /></div>';
            h += '   <div class="person">' + name + '</div>';
            h += '</li>';

            // 将用户和图像添加到页面
            $('section ul').append(h);
        });
    }
}

function init() {
    // 重置正确答案和currentRound数组
    correct = '';
    currentRound = [];
    $('ul, section').removeClass();
    $('ul').empty();

    getRandom();

    // 显示默认的Twitter账户图标
    $('#tweet .avatar').html('<img src="' + defaultIcon + '" alt="" />');

    // 从正确用户获取一条随机推文
    $.getJSON('https://twitter.com/status/user_timeline/' + correct + '.json?count=10&callback=?', function(data) {
        var ran = Math.floor(Math.random()*data.length);

        console.log(data.length);
        console.log(ran);

        $('#tweet .content').html(data[ran].text);

        // 打乱currentRound数组，使正确用户不总是第一个
        currentRound.sort(function() {return 0.5 - Math.random()});

        // 获取头像并显示用户名
        buildQuiz();
    });
}
```

在接下来的两个函数中，我们将通过调用`init()`函数来启动应用程序。此函数重置所有变量以开始一个全新的游戏，解析JSONP Twitter API源以获取随机选择的经过验证的Twitter账户，然后将所有内容传递给`buildQuiz()`函数，以构建并显示给用户。

一旦文档加载到浏览器中，并且DOM（文档对象模型 - HTML文档中所有对象的跨平台表示）准备好被操作，下面的代码（清单2–8）就会运行。在jQuery中，你可以通过使用下面的简写形式`$(function() { ... 代码放这里 });`，在文档准备好时运行你的代码——这是JavaScript领域中的`ondocumentready`事件。

一旦文档准备好，我们将调用`init()`函数，该函数将重置页面上的所有内容，获取一个随机用户，并像我们之前经历过的那样构建测验。我们还将为将被写入页面的所有列表项分配点击事件，使它们最终像按钮一样工作。一旦用户点击列表项，应用程序将用发布推文的正确用户的头像替换`defaultIcon`，如果用户选择正确则更新分数，并为游戏分配`gameover`类，如果屏幕再次被点击，这将告诉应用程序开始新一轮。

### 清单 2–8. 这是谁的推文？Javascript 文件，第四部分

```
$(function(){
    // 运行init()函数并启动应用程序
    init();

    // 在用户选择时检查正确用户
    $('ul li').live('click', function() {
        var name = $(this).attr('rel');
```



```javascript
var img = $('li[rel="' + correct + '"] img').attr('src');
var score = $('.score span');

// 如果游戏结束，重启游戏
if($('ul').hasClass('gameover')) {
    init();
}
else {
    // 将默认头像替换为正确的头像
    $('#tweet .avatar img').attr('src', img);

    if(name == correct) {
        score.text(parseInt(score.text())+100);
        $('section').addClass('win');
    }
    else {
        $('section').addClass('fail');
    }

    // 为页面添加 gameover 类
    $('ul').addClass('gameover');
}
```
就是这样！对于那些正在跟随代码编写的读者，恭喜你们，你们正式完成了第一个移动 Web 应用程序。现在你可以启动你信任的 Android 设备了（如果你还没有这样做的话），连接到与你电脑相同的网络，并在设备上查看你的新应用程序。要这样做，只需将设备的浏览器指向你电脑的 IP 地址。你可以通过打开命令提示符（Windows）并运行 `ipconfig` 命令（见图 2–9），或者打开终端（OS X/Linux）并运行 `ifconfig` 命令来查找你的 IP 地址。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_40_0.png)

**图 2–9。** *Windows 7 上的命令提示符，显示我们的服务器 IP 地址*

就这样——你的第一个应用程序。

## 总结

我们在本章涵盖了很多“应用”层面的内容，例如设置开发服务器、编写 CSS 和 JavaScript 文件，以及测试你的新应用程序。我们将在下一章使用另一个示例继续这种“应用”式写作，然后再停下来更多地讨论 Web 设计的核心概念。现在让我们聊聊第三章的火腿吧！

# 第三章

## Twitter 应用程序：我爱火腿

既然我们已经掌握了一个移动 Web 应用程序，我想让我们探索使用 Twitter API 做一些不同于层出不穷的经典的“显示 Twitter 消息应用程序”的事情。正如我们在第二章中讨论的那样，使用 Twitter API 可以访问始终丰富的“火水管”数据，这些数据可用于各种应用程序和游戏——基本上你可以想到的任何东西。

我一直非常喜欢使用 Twitter 的一个想法来自几年前的一系列老式网络节目。虽然这个游戏的名称因节目而异，但其背后的主要原则始终相同：用户会被呈现两个押韵的不同搜索词，并必须猜测哪个词产生的推文数量更多。虽然规则很简单，但这小小的游戏，我们将称之为“我爱火腿”，可以带来数小时的乐趣。所以，让我们不再废话，启动我们的本地开发环境并开始编写代码吧！

### HTML

下面列出的代码清单 3–1 设置了将成为我们应用程序基础的基本 HTML 文档。

*清单 3–1。我爱火腿的 HTML*

```html
<!DOCTYPE HTML>
<html>
<head>
<meta charset="utf-8">
<title>我爱火腿</title>
<link href='http://fonts.googleapis.com/css?family=Droid+Sans&v1' rel='stylesheet' type='text/css'>
<link rel="stylesheet" type="text/css" href="css/style.css">
<script type="text/javascript" src="js/jquery-1.6.1.min.js"></script>
<script type="text/javascript" src="js/main.js"></script>
<meta name="viewport" content="width=320, height=device-height,user-scalable=no, initial-scale=1.0,maximum-scale=1.0,minimum-scale=1.0" />
</head>
<body>            <section></body>

<h2>这些精彩的推文中哪一个的搜索结果更多？！</h2>
</ul></section>

<body>
</section></body>

</body>
</html>


```

我们在本应用程序中使用的 HTML 标记将比我们之前构建的“这是那条推吗？”应用程序中的标记更稀疏，而且看起来也非常相似！为了简单起见，我保留了文件夹树布局的命名约定基本不变（见图 3-1）：

![](img/8b0ff5e51ddb912cd941bb18cf27206a_43_0.png)


**图 3-1。** *一个干净且易于阅读的文件结构，正如在 Adobe Dreamweaver CS 中看到的，这将为你节省大量的时间和烦恼！*

在创建文件和组织项目的文件夹结构时，我发现坚持使用人类可读、一目了然且在整个项目中保持一致的命名方案通常很有用。如果你给文件命名为“supercooldocument12-667.html”，那么最终用户将更难找到这些文档，而且当你将来回来更新和修改应用程序时，这也可能会引起问题。（相信我：你会完全忘记这些文件的作用。）另一个建议是，给文件命名时使用当前日期，或者使用版本控制系统来保持条理。所以请记住，在命名文件时，要保持简单和/或有意义！

### CSS

我们的 CSS 也将与我们之前构建的应用程序看起来相似。这里有一些细微的差别，以及一些我们在本应用程序中展示的有趣的 CSS 属性，例如 text-shadow CSS 属性，它允许你在客户端的浏览器中实时为你的文本应用一些非常出色的阴影效果。这不需要像我们几年前那样（“几年前”意味着几年前！）依赖设计师来制作一张包含新时尚文本的过度压缩图像，然后将其注入页面，或者将它们分配为 CSS 类的背景图像，以便在需要时分配给我们的文本块容器。虽然这样做并不难，但这需要编写更多的代码，并且在设备上加载更多的图形资源。如果用户所在的地区数据连接较慢，这可能会导致明显的停顿，或者使用户在情感上与你的应用程序脱节！

清单 3–2 涵盖了基本重置应用程序中将使用的常见元素的间距和字体大小。

**清单 3–2。** *我爱火腿的 CSS -第 1 部分*

```css
/*** 重置 ***/
html, body, header, section, div, p, ul, li, h2 {
margin:0;
padding:0;
}

ul, li {
list-style:none;
}

/*** 全局 CSS ***/
html, body {
width:100%;
height:600px;
overflow-x:hidden;
}

body {
font-size:14px;
font-family: 'Droid Sans', Arial, Helvetica, sans-serif;
background:#993366;
}

h2 {
font-size:18px;
color:#fff;
text-shadow:1px 1px 5px rgba(0,0,0,0.9);
}
```

我们的 h2 标签将幸运地成为 text-shadow 的受益者。如果你查看此应用程序的 HTML 标记，你可以看到这个 h2 标签包含一段将呈现给用户的文本。根据当前游戏状态的不同，文本将更改多达四次，并将由应用程序的 JavaScript 进行更新。如前所述，如果我们用旧方法做这件事，我们将不得不创建四个包含所需文本的单独图像，并在需要时手动将这些图像注入页面，或者将它们分配为 CSS 类的背景图像，以便在需要时分配给我们的文本块容器。虽然这样做并不难，但这需要编写更多的代码，并且在设备上加载更多的图形资源。如果用户所在的地区数据连接较慢，这可能会导致明显的停顿，或者使用户在情感上与你的应用程序脱节！

在清单 3–3 中，我们将设置列表项：

**清单 3–3。** *我爱火腿的 CSS –第 2 部分*

```css
/*** 区域 ***/
section {
    margin:20px 10px;
    padding:10px;
}

sectionul {
    width:100%;
    margin:25px 0;
}

section li {
    margin:10px 0;
    padding:10px 5px 10px;
    min-height:22px;
    line-height:32px;
    border-radius:7px;
    background:-webkit-gradient(linear, 0% 0%, 0% 100%, from(#a1a1a1), to(#A1A1A1), color-stop(.6,#8A8A8A));
    -webkit- box-shadow:0 0 20px rgba(0,0,0,0.5);
    box-shadow:2px 2px 10px rgba(0,0,0,0.8);
}
```

你也会注意到我们在 CSS 中对列表项做了一些不同的处理。在这里，我们向按钮添加了漂亮的渐变背景，使它们更具活力。与我们在第一个应用程序中创建的渐变背景不同，这个使用了三色渐变系统，使其更具倒角效果。同样，就像我们的文本阴影一样，使用 CSS 有助于减少浪费客户端资源，例如加载我们不使用的图像。我知道我反复强调这一点，但那是因为这是一条真正重要的规则！切勿浪费你的客户端资源，尤其是在当今世界，数据上限荒谬或数据连接缓慢的时代。最后但并非最不重要的是，在我们的 CSS 文件（参见清单 3–4）中，我将向你介绍两个非常实用的 CSS 选择器，以便你熟悉它们——:before 和 :after 选择器。
```



#### 清单 3–4. CSS for I Love Ham– 第 3 部分

```css
sectionli.fail {
background:#990000;
color:#fff;
}

sectionli.win {
background:#009900;
color:#fff;
}

sectionli.fail, section li.win {
border-bottom:1px solid #fff;
}

sectionblockquote {
margin:0;
padding:0;
}
sectionblockquote:before {
content: "\201c\2005";
font-size:26px;
float:left;
margin-right:5px;
padding-left:5px;
}

sectionblockquote:after {
content: "\201d\2005";
font-size:26px;
margin-left:5px;
padding-left:5px;
}
```

现在，这些选择器非常简洁，因为它们允许你在附加它们的元素前后添加内容。在这里，我将它们附加到引用块元素上，这是一个较旧的 HTML 元素，用于在语义上标记该内容应区别于页面的其余部分，以示突出。

现在，如果你查看 content 属性，你可能会感到有些困惑。在大多数情况下，人们通常在这个字段中添加一些有意义的东西，例如在无序列表的圆点处添加一个" > "，或在关联回某篇文章的一串串内容之后添加省略号。然而，很多人并不知道，你也可以在这个属性中包含十六进制代码，以显示键盘上不常见的字符，例如下面我所希望在我引用块内容的开头和结尾添加的引号！

### JavaScript 部分

既然我们已经对一切是如何布局有了良好的理解，现在该动手弄清楚所有的齿轮、滑轮和链节是如何组装在一起并使该应用程序运行起来的！首先，正如我们之前的应用程序一样，我们在此处声明将在整个应用程序中使用的全局变量。在 JavaScript 中，理解全局变量与局部变量之间的区别非常重要。

简而言之，我想花点时间强调这是一个最基本的解释：局部变量是一个可以在函数内部使用的变量，但不可在不同的函数内使用或作为脚本的一部分。函数基本上是可重复使用的“捷径”。例如，我可能会创建一个对给定输入（称为“函数参数”，即在函数调用后放在 () 内的信息）进行一些数学运算的函数，并在整个代码中重用该函数。局部变量仅在函数块内使用，在外不可访问。可以说，就这些变量而言，函数内部就像是你代码其余部分的一个独立小世界！

另一方面，如你现在可能已经猜到的，全局变量可以在全局范围内访问，因此你可以在 JavaScript 文件中的任何函数或对象中调用它。尽管有些人会对使用全局变量嗤之以鼻，因为它们*可能*在后续引发问题。例如，全局变量可能由多种函数更新，导致在调试过程中对变量如何变化感到困惑。然而，为了学习方便，既然这是一本面向初学者的书，我们将在示例中使用它们。

清单 3–5 设置了一组将在我们的 JavaScript 文件中使用的环球变量，以及一个充满押韵演示选项的数组，以让我们的用户娱乐数小时……或几分钟。

#### 清单 3–5. Javascript for I Love Ham - 第 1 部分

```javascript
/**
 * I Love Ham
 * @author: Rocco Augusto
 * @file: js/main.js
**/

var correct = '';
var choice = '';
var resultLength = 0;
var tweets = [
 ['I love ham','Earthquake in Japan'],
 ['Android is awesome', 'I just hit an opossum'],
 ['Ice cream sandwich','I fell out of my hammock'],
];
```

与我们之前的游戏不同，我们将为用户展示一个更小的选项数组。虽然我非常喜欢添加 50 到 100 个不同的押韵示例，但不幸的是，我仅能以只有三种即兴押句的能力。暂时来说，我认为三种就足够了，但如果你在家跟着学，请尽可能多地添加你能想到的选项！我相信你们中许多人比我更有幽默感！

清单 3–6 引导我们查看应用程序的 init() 函数，并从 API 获取我们的 Twitter JSON 馈送。

#### 清单 3–6. Javascript for I Love Ham - 第 2 部分

```javascript
function init() {
    window.scrollTo(0, 1);

    //reset the correct answer and currentRound array
    correct = '';
    choice = getRandom();
    $('ul, section').removeClass();
    $('ul').empty();

    //find out which item has more search results
    for(i=0; i<choice.length; i++){
        var position = i;
        $.getJSON('http://search.twitter.com/search.json?rpp=100&q=' + choice[i].replace(/\s/g,'%20') + '&callback=?', function(data) {
            //check the length of results for each search
            //then set them to the "correct" variable
            correct.push(data.results.length);
        });
    }

    // generate the buttons for this round
    buildQuiz();
}
```

这里是我们的 init() 函数，它将在应用程序稍后加载 DOM（文档对象模型）后被调用并运行。当使用 Twitter API 时，你可以发送几个参数进行搜索。让我们快速过一遍！

- Rpp 告诉 API 我们希望每页返回多少结果。在这种情况下，我们每次搜索拉取最多 100 条结果。
- Q 是用于存放我们搜索查询的参数。
- Callback 被触发以确保 API 以 JSONP 格式返回数据，这样我们就不会遇到任何跨域安全问题！

你还会注意到上面搜索查询中的 i，其中我们正在调用当时要搜索的词。在那一部分，我使用 replace() 方法来搜索字符串中的所有空格并将其替换为 %20，这是空格在 URL 中的编码版本。这允许搜索通过普通的 HTTP 请求发送，而不会扰乱网页在网络上的实际指向位置。为了更好地理解为何这是必要的，想象一下——有人给你发送一个 http://someawesomesite.com/some awesome page 的链接。由于 URL 被破碎了，如果你发给那个人，他点击后，他最有可能被导航到 http://someawesomesite.com/some 的页面，而 URL 的其余部分将被忽略，但点击一个看起来像 http://someawesomesites.com/some%20awesome%20page 的 URL 会将用户精确地带到他们想去的地方。始终确保你创建的 URL 中没有间断（参见图 3–2）！

[content]www.androidthoughts.com/news/show/112817/amazon-cloud-player-unlimited-music-storage-as-long-as-you-pay.html


## 摘要

嘿，要是照我这么说，这还算不错！我们成功地将一小段代码和一个疯狂的想法结合起来，很快将其转变为一个外观不错的原型供人把玩。我们展示了另一个通过 JavaScript 接入 Twitter API 的例子，并为将其扩展到其他方面奠定了基础——不仅仅是搜索推文，还包括使用热门话题和提及。只需再多花一点时间和努力，我们就可以在此基础上开发这个非常基础的 Twitter 应用，将其转变为一个完整的游戏，让用户耗费数小时在我们的应用中！

# 第四章

## 应用程序的基本规划和结构构建

到目前为止，我们一直让你们直接开始编写几个应用程序，提供了一些关于屏幕分辨率、JavaScript 和 CSS 的背景信息，并且我们给了你们一大袋免费（且便宜）的“东西”，形式为各种资源，你可以在开发时使用它们。有了这些信息，你完全可以狂热地编写各种有趣的东西并发布到网上供世人观看和使用。唯一的问题是，如果你没有真正考虑你正在构建什么，世界可能不会太热衷于使用你所构建的东西。没有什么比花费几个小时在只有你自己（或许还有几个朋友）才会看到的项目上更让人感到沮丧的了。

在本章中，我们将以两种不同的方式讨论应用程序开发：规划你的应用程序（这涉及理解你正在构建什么以及如何确保你不会遗漏关键部分）；以及构建代码结构，这是一个更简单的概念，但对于即将讨论的理由同样重要。这是“将秩序带入混乱”的章节，我们希望你听取我们的警告和建议！

### 了解你的受众

如果你对创造某事有任何激情，那么你以前可能有过这样的想法：“我希望有一个工具可以完成[在此插入一个机智的想法]……我知道，我就来建吧！”到了这一步，你很可能为了自己的使用而将一些东西拼凑起来（hack），然后意识到其他人也可能感兴趣使用它。每当我创建新的 Web 或移动应用程序时，我知道我总是这样做，为自己或有与我相同需求的人构建它们。这些人也许就是你的受众。

#### 满足人们的需求

开始研究你的下一个应用程序，有几种方法。有时需求会显现出来，或者你看到了一个明显的机会。其他时候你可能会觉得某事会很受欢迎，但并不确定它是否真的能成功。虽然你可以关注 Twitter 和 Facebook 上能补救的抱怨，或者使用某种调查来了解你的受众想要什么，但我们将在此展示一种非常简单的方法，体现了一个普适的规则：知道人们在寻找什么。以下方法应该能提供一些线索，说明人们如何在线上花费时间，从而让你知道哪里可能存在机会。

我们从网络上一个流行的广告系统开始，即 Google 的 Adwords。注册是免费的，即使你从未放置过任何广告，Adwords 提供的其中一个非常实用的工具就是外部关键词工具：https://adwords.google.com/select/KeywordToolExternal。该工具告诉你有多少人正在搜索特定关键词。查看人们对你想构建的东西是否真正感兴趣，这是种很棒的方法。

例如，一个我考虑了很久（并且实际上在某种程度上已经建立起来）的项目是一个面向有抱负的作家的网站，用于磨练他们的技能。我设想一个网站，用户可以获取主题来撰写散文、短篇小说、文章、诗歌等形式，并让其他人对作品进行投票。获胜者会获得一些积分，或许还能赢得真正的奖品。

我如何了解这是否有市场？嗯，我可以使用关键词工具进行一些简单的搜索，就像图 4-1 中针对“写作比赛”和“写作帮助”这些关键词的搜索一样。要记住，关键词搜索是专为广告商设计的，因此稍加破解那种不友好的语言混乱（即“市场营销 SEO 术语”）是很重要的。首先，我知道“写作比赛”的流量（以 Google 月度搜索量计算）比“写作帮助”多约 2.5 倍。这些信息很有用，因为它表明寻找比赛和认可的人比寻求建设性写作评论的人更多。如果我的网站或应用将包含这两种元素，那么利用比赛角度似乎更好。然而，如果我还不完全确定我的应用或网站是什么，我可能会发现关键词创意列表（图 4-2）特别有帮助：

在这里，“竞争”列可能有助于告诉我去哪里。你看到的“竞争”，根据 Google Adwords 是指有多少其他广告商在人们搜索所列关键词时试图让他们的广告出现。对于“比赛写作”（或列表更后面的另一项，“免费帮助撰写商业计划书”），我会遇到激烈竞争，但对于“文章写作比赛”（或未显示的另一个项目：“有说服力的写作比赛”）竞争很小。

使用 Adwords 中的外部关键词工具，我可以不仅了解人们搜索什么，还可以了解其他公司在广告什么。这可以帮助你更好地理解是否存在针对你产品的受众（通过使用你认为他们会使用的 Google 关键词），以及是否已经有很多替代产品你面临。虽然口碑广告对某些产品效果很好，你不应该低估搜索流量的力量！

### 我的用户是谁？

如果你已经知道存在针对你产品的受众，现在你必须弄清楚你的用户是谁。最近，在参加一个充满才华横溢的年轻未来持有 MBA 高管的课程时，我发现他们对于“目标定位”或寻找他们的细分用户并进行针对性营销的想法感到恼火。他们对不向“所有人”营销的想法表示反对，而却没意识到：a）“所有人”可能不感兴趣，b）目标用户比外面通用的“普通人”（或“普通女人”）更有动力使用你的产品。

了解你的用户最好的方法是研究你自己的产品（在其早期阶段）或其他已存在的产品或网站。如果你正在构建一个跟踪通勤交通到达和出发时间及延误的应用程序，或许可以看看竞争应用程序或服务针对的是谁。你有很大的机会针对同一群人，因此在产品上花一些时间和精力考虑该群体的需求和愿望是非常值得的。

让我们用一个我早些时候提到的虚构的交通应用程序来探讨这个例子。确定受众可能很困难，你可能需要考虑多于一组人。一个似乎合理的群体是忙碌的通勤者或商务旅客。如果我想针对这个群体，我可能会问并回答一些问题，例如：

- 我的应用或网站中的哪些功能对忙碌的人有吸引力？
- 我的应用中的哪些功能、细微差别或流程会减慢快速移动的人的速度？
- 我的应用有哪些功能实际上对使用公共交通的人有用？
- 我如何轻松地向我的忙碌用户发出信号，表明有什么重要的事情发生（例如，公交车或火车晚点）？
- 我的应用程序将如何使用？它是用来规划行程，还是最后一刻重新规划路线？或是两者都有？

清单可以从那里继续，但你明白了图意。通过开发一个假设的“用户”并设身处地为他们着想，你可以更好地理解需要做些什么来使他们的生活更轻松。使其变得更简单，你就会获得用户或客户！然后简单地对你下一个人口统计群体进行相同的调查，也许这次是“休闲旅客”或“游客”。

并非所有研究都必须在你脑海中完成；存在资源可以用来挖掘你的潜在用户说什么。也许可以看看你潜在竞争对手的评价，看看人们喜爱和讨厌那些应用的什么内容。你还可以查看用户小组和论坛，甚至进行简单的 Twitter 搜索，以掌握某一领域的“问题”。

正如我之前提到的几段文字一样，你可能已经处于能够拥有这些信息的位置。如果你过去开发过网站或应用程序，你可能使用过像 Google Analytics (http://google.com/analytics) 或 Flurry Analytics (http://www.flurry.com) 这样的产品。这些产品可以追踪谁使用了你的应用程序，并提供无价的信息，你以后可以利用这些信息来定义你的“用户”。




For example, in one application that I wrote, I had a Bowen form that people could use to tell me a bit more about themselves. From there, I found out that the average user of my app was between 25 and 34 years old, as seen in Figure 4-3.

![img/8b0ff5e51ddb912cd941bb18cf27206a_56_0.png](img/8b0ff5e51ddb912cd941bb18cf27206a_56_0.png)

**图 4-3.** *某应用的用户年龄分布*

这些信息可以有多种用途。首先，我可能会考虑这个群体认为重要的功能，并在未来的版本中重点实现这些功能。或者，我可能会将有限的广告预算从青少年到二十出头这个市场转移出来，转而更多地关注 25 到 34 岁的人群，以吸引新用户。我对用户了解得越多，就越能理解他们的需求，我的网站或应用也就能更好地为他们服务。

不过有一点需要注意：你可能会注意到，我的应用只有 17% 的用户拥有已知信息。这是因为记录这部分信息的应用功能可能对某些特定人群更有用，这可能会导致我的数据产生偏差。不深究这个特定程序的细节，需要指出的是，你不应该只依赖单一来源，尤其是当你只有少量数据时，或者当你觉得样本可能存在偏差时。

一旦我从各种渠道收集到了关于我的受众和用户的信息，我就可以制定一个计划了。

## 制定计划

作为一名急于玩耍、构建和获利的新开发者，规划可能是最容易被忽视的事情。在本节中，我们将讨论关于构建何种类型的应用、该应用应该是什么样的外观，以及用户应该如何在其中进行操作等问题。通过从一开始就理解所有这些，我们可以保持优先级的有序，在编码时，只需实现我们已经设计好的内容。让我们先来看看我们可以构建的不同类型的移动应用或界面。

## 并非所有移动应用都一样

本书标题中包含"Web 应用（web apps）"一词，这本身就承认了还有其他类型的应用存在。让我们讨论三种类型的移动界面或应用。

### 原生应用（Native Applications）

如果你拥有或使用过 Android 手机（我希望你正在读这本书的话，你已经拥有了一部），你可能已经使用过手机上的一些应用。Web 浏览器是其中一个应用，通讯录应用是另一个，计算器应用则是又一个。这些针对 Android 的应用通常使用 Java 编写，并使用称为 Android 软件开发工具包（Software Development Kit，简称 SDK）的特殊工具进行编译。这些工具可以免费下载和使用，用于创建你可以在 Android 应用市场（Android Marketplace）发布的应用。

这些应用被称为"原生"应用，因为它们直接从手机运行。用户拥有它们的专属图标，点击图标即可打开应用（见图 4-4）。这些应用可以轻松地在手机上存储数据，并且如果用户允许，它们可以相互交互。通常，它们必须通过应用市场或发布者的网站下载和安装，但也可以"侧载"（side-loaded），即通过在手机上直接下载并运行应用的 APK 安装包来进行安装。

![img/8b0ff5e51ddb912cd941bb18cf27206a_58_0.png](img/8b0ff5e51ddb912cd941bb18cf27206a_58_0.png)

Native applications tend to be faster because all pieces of the application live in the phone's memory and they also have deeper access to the hardware of the phone, which the web browser does not have. By the same token,原生应用程序在性能上通常更具优势，因为应用的各个组件都驻留在手机内存中，而且它们能更深入地访问手机硬件——这是 Web 浏览器所不具备的。然而，这同时也给最终用户带来了风险：刚刚安装的应用可能实际上是试图窃取信息的木马；或者开发者为了急于推出更新，没有仔细检查就留下了一个安全漏洞。这与 2011 年 Skype 发生的情况类似，当时有人发现用户名和密码以未加密的纯文本形式保存在用户的手机上，任何人都可以轻易获取。幸运的是，该问题很快就得到了修复。对于开发者来说，开发原生应用可能需要更多时间，学习曲线也可能更陡峭，特别是当开发者已经熟悉 HTML、CSS、JavaScript 和其他 Web 技术时。

### 移动网站（Mobile Web Sites）

移动网站，或针对移动设备优化的网站，通常是用户直接访问，或者访问常规网站后被重定向到移动版本时查看的。这些仍然是网站，通常不会在用户设备上存储数据，也不会与用户设备进行非常密切的交互。从根本上说，它们只是用于展示内容，而不是真正与用户进行深度互动。这通常是一家公司或网站改善移动用户体验的最基本方式。移动网站允许你进行一些基本操作，但不会与你进行过多交互，只是提供几页简单的文字，或许还有一两个表单。

正因为如此，这些网站缺乏其桌面端"大哥"（即完整网站）的"完整功能特性"，也可能没有针对智能手机或平板屏幕进行特别优化（例如，平板电脑可能看到太大的版本，智能手机可能看到太小的版本，这取决于该网站针对的是哪种设备）。虽然开发者可能喜欢这种方式，因为它创建、更新和测试起来相对简单，但最终用户并不认为这些移动网站是应用。如果你的目标是构建一个具有交互性或被视为工具的东西，那么你可能需要避免这种简单的方式，转而选择 Web 应用。

### Web 应用（Web Applications）

最后，我们来讨论前面两种应用类型的结合，也是本书一直在开发的应用类型。Web 应用试图将原生应用的流畅体验与移动网站相对容易编码和更新的特点结合起来。例如，本书前面章节中的应用（见第 2 章和第 3 章）拥有用户可以轻松点击的按钮，就像图 4-4 中展示的原生应用一样，但它们运行在 Web 浏览器内部。如果用户为这个应用创建快捷方式（或者应用本身可以询问用户是否愿意创建），那么它就可以像原生应用一样拥有自己的图标。Web 应用还可以使用一些技术，像原生应用一样集成到操作系统中。

最好的理解方式是：Web 应用，就像常规应用一样，旨在与用户进行互动，而不仅仅是被浏览。

### 那么我应该构建哪种？

现在，你可能会想知道自己真正想走哪个方向。老实说，虽然本书重点介绍 Web 应用的优势（因为它们通常比原生应用更容易编程，比移动网站功能更丰富，而且对初学者程序员更友好），但你可能无法只使用一种解决方案。我们再次回到了解你的用户这一理念。如果你的用户所在地区始终有蜂窝网络服务，那么 Web 应用可能和原生应用一样有用。如果用户使用各种不同的设备（例如 Android、Windows Phone 或 iOS 设备），那么 Web 应用可能是同时覆盖这三个平台的最简单方式。

最终，你必须制定适合用户的移动策略。在本书后面的章节（第 13 章），我们将告诉你如何通过简单地将 Web 应用转换为原生应用，无需做太多工作就能至少拥有一个 Web 应用和一个 Android 原生应用。

一旦你决定了如何构建移动策略，你应该避免急于直接开始编码。一个好的开发者会规划他或她的应用，无论是原生的、基于 Web 的还是移动网站。这一步骤可以归入应用结构化的理念，我们将在接下来讨论。

## 应用的结构设计

在本节中，我们将讨论从零开始设计应用的过程。这包括三个步骤：线框图或原型阶段、图形设计阶段，以及代码结构阶段。让我们从设计开始谈起。

## 线框图 / 原型图

拥有一个想法后，立即开始编码而不考虑最终产品的外观，这可能非常诱人。但出于以下几个原因，这可能是个坏主意：

- 它可能让你陷入一个最终看起来并不理想的的设计（即过于杂乱）。或者你可能会意识到，如果没有急着直接创建按钮和框，你的设计本可以更高效！
- 它可能阻碍你进行创新，因为你"懒得"为了添加新功能而改动东西。
- 它可能让你直到项目最后才征求反馈，而此时修改可能太耗时了。向用户展示设计，看看他们是否觉得直观，然后调整草图，要比给他们看一个应用后再重新编码来改善设计要容易得多。

为了防止这些问题，许多设计师会创建线框图或应用的"原型图"（mockups）。例如，一个类似我们之前讨论过的交通应用，一个非常粗略的原型图可能是这样的（见图 4-5）。




正如我之前提到的，这是一个相当粗糙的模拟原型；实际上，它可能甚至达不到我最终设计版本的千分之一。然而，在构建这个模拟原型的过程中，我确实意识到了一些问题。我为过境时间、警报和偏好设置构建了按钮；为警报预留了空间；甚至在底部预留了一些广告位。但是，我还有另一块标记为“E”的屏幕区域，完全不知道可以用它来做什么。有了模拟原型，我可以简单地擦掉并重绘来完善它。但如果在实际开发中，我可能会在那里留下一片空白，直到版本接近1.0时才真正意识到这个问题。

显然，你可以按照自己喜欢的方式创建模拟原型。图4-5是使用我平板电脑上的一个应用程序创建的，它允许我进行手绘（你可能看得出来）。也可以在网页编辑器中使用实际的图片、按钮等来布局模拟原型（即使按钮实际上无法工作）。另一种选择是使用PowerPoint或Keynote之类的程序，这些程序可以轻松地绘制方框、制作动画并创建许多类似的图形。

### HotGloo及其他原型设计工具

如果你正在寻找一个基于网络的工具来创建模拟原型，那么你可能需要了解一下HotGloo。该产品的主页如图4-6所示（http://www.hotgloo.com/）。这款提供按月订阅服务的工具，可能是我使用过的最好且最易用的线框图工具之一。我使用过的一些线框图工具只提供基本的线框图，但HotGloo允许你同时进行大量的视觉设计和线框图绘制，从而节省时间。

你可能还想考虑的其他产品包括LucidChart（http://www.lucidchart.com）和Pencil Project（http://pencil.evolus.vn），它们可以集成到你已有的工具中，比如Microsoft Visio。

## 用户动线：导航或故事板

一旦完成了线框图，接下来就是坐下来，连接各个点，弄清楚你将如何组织网站内容，规划出所有的页面及其所属的部分。这个过程被称为网站规划，如果你花点时间去做，它会变得相当简单和有趣。如果你的应用程序不是特别线性（例如，可能是一个游戏），你也可以将其视为故事板。简而言之，就是以有组织、合乎逻辑的方式布局内容。

在创建你的规划图时，最好尝试将内容相似的部分放在相似的区段或分组中。这将使你在构建应用时更加轻松，因为你可以一目了然地看到应用程序中哪些页面需要相互关联。对于游戏来说，可以将其理解为以逻辑的方式呈现你的信息；将所有的“金币”以及用它能购买的东西放在一起，或者将所有的“生命值”以及影响它们的增强效果放在一起，依此类推。

请查看下面的图4-7，以更好地了解传统网站规划图的样子。注意它与我们小时候在语法学校被迫做的那些家谱项目非常相似？嗯，原则基本相同。网站的父级页面（或区段）每个都有关联于该区段或类别的子页面。

对于这个网站规划图，我使用了一个图形设计工具为本书创建了这个模拟原型；但当我为个人项目工作，或者与想要快速看到某些东西的客户坐下来时，我会在餐巾纸或笔记本纸上画出网站规划图和线框图。

使用你手头可用的任何工具来创建你的网站规划图。无论它是如何创建的，重要的是你要坐下来，思考你的页面是如何组织的，这样可以让你在构建和开发时更加轻松。

任何开发人员最不想做的事情，就是在完成80%的项目后，却因为缺乏适当规划而不得不回头重做某些事情！

现在我们知道了应用程序的外观以及内容的组织方式，我们可以开始编码了。让我们用本章最后几页来讨论如何最好地构建我们的开发环境，以实现最大的生产力。

## 构建你的开发环境

在掌握了高层信息之后，你还需要考虑一些良好的实践开发规则，这些规则可以在编写应用程序时让你保持条理和高效。接下来，我们将讨论一些关于如何构建代码及其存放目录的想法。

### 代码结构

现在你的线框图已经完成，你对页面上所有元素的布局也有了一个大致的概念，是时候开始思考如何构建代码了，这样在构建应用程序时，你就不会做多余的工作。

你现在可能正在挠头想：“这能有多难？我只是在页面上写文字而已。”你说得对。但是，假设你的应用程序中有十个不同的页面。你向Web应用程序推送了一个更新，然后发现你的页脚部分有问题。

如果没有做好适当的准备，我们那位不幸的开发人员可能已经将相同的页脚复制粘贴到了构成应用程序的十个不同的HTML页面中。现在是时候更新代码了，我们的虚构开发人员必须在十个不同的HTML文件中更新新的页脚信息。

正确构建代码的一个更简单的方法是，将整个站点中相同的页脚信息提取出来，为它创建一个单独的文件。然后在你的代码中，你可以将这个文件包含到你的页面模板中，并像之前一样在每个页面上显示它。如果将来你需要更改该代码，使用这种方法，你只需在一个文件中更改代码，就能让你的生活轻松很多。

让我们看看下面的示例。在清单4-1中，我们有一个非常简洁的页面，它使用PHP引入了我们希望在每个页面上显示的额外页面代码。

#### 清单 4–1. 使用PHP包含语句，我们将引入要包含在页面中的额外代码

```html
<!DOCTYPE HTML>
<html>
<head>
<meta charset="utf-8">
<title>Super Cool Web Application</title>
</head>
<body>
<header>Super Awesome Header</header>
<article>
<header>Article Header</header>
<p>Fusce luctus accumsan odio. Cras vel sodales mi. Suspendisse et arcu quis magna feugiat ultrices sit amet non erat. Etiam malesuada dui venenatis eros gravida aliquet. Aliquam erat volutpat. Nullam dapibus cursus ultricies. Suspendisse congue accumsan purus non scelerisque. Phasellus ut sapien libero, vel luctus velit.</p>
</article>

<!-- 这就是我们使用PHP将另一个文件包含到文档中的地方 -->
<?php include('footer.php'); ?>

</body>
</html>
```

如果你查看该清单的底部，会注意到我引入了页面footer.php（见清单4–2）。我通过将包含函数包裹在`<?php ?>`标签中来实现这一点。这告诉你的页面，如果服务器支持PHP，就执行PHP代码，在此代码中，它会查找与前面列出的文档位于相同相对路径的footer文档。如果你使用的是我们之前在书中讨论过的Uniform Server本地开发服务器，那么这应该能完美运行。否则，我们可能需要指定一个相对路径；例如，如果我将所有“包含”文件放入一个名为“includes”的目录中，我的代码可能读作：`include('includes/footer.php')`。我们稍后会讨论目录结构，所以当你完成这里的内容时，你就知道相对路径对你的文件来说是什么样子了。

现在我们知道如何在文档中使用PHP包含文件，我们将看看那个PHP文件的内部是什么样子，这样你就能看到以简单、可重用的方式构建代码是多么容易。

#### 清单 4–2. 查看 footer.php 文件内部

```html
<footer>
<ul>
<li><a href="#">Home</a></li>
<li><a href="#">About</a></li>
<li><a href="#">Contact</a></li>
<li><a href="#">Privacy Policy</a></li>
<li><a href="#">Terms and Conditions</a></li>
</ul>
<p>&copy; 2011 Super Awesome Site, Inc. All rights reserved.</p>
</footer>
```

如你所见，此文档中的代码非常基础。我们有一个无序列表，它被浮动到文档的右侧，还有一些版权文本，它将浮动到列表的左侧。我们只需想象，在远处某个地方，已经为这个文档创建了一个样式表，让一切都变得美观。



## 使用 CSS 3 处理多种屏幕分辨率

PHP 的妙处在于它是在服务器端运行的，而不是在客户端。这意味着你在 HTML 文档中包含的任何 PHP 代码（无论是将其他文档包含到你的模板中，还是自定义创建的类、函数等）对客户端都是不可见的。当客户端加载页面并查看源代码时，他们看到的只是一个无缝的 HTML 文档（参见清单 4–3）。

清单 4–3。在浏览器中查看我们的仿真实文章会显示一个完整的 HTML 文档，其中没有服务器端 PHP 代码

```
<!DOCTYPE HTML>
<html>
<head>
<meta charset="utf-8">
<title>Super Cool Web Application</title>
</head>
<body>
<header>Super Awesome Header</header>
<article>
<header>Article Header</header>
<p>Fusce luctus accumsan odio. Cras vel sodales mi. Suspendisse et arcu quis magna
feugiat ultrices sit amet non erat. Etiam malesuada dui venenatis eros gravida aliquet.
Aliquam erat volutpat. Nullam dapibus cursus ultricies. Suspendisse congue accumsan
purus non scelerisque. Phasellus ut sapien libero, vel luctus velit.</p>
</article>

<!-- This is where we use PHP to include another file into our document -->
<footer>
<ul>
<li><a href="#">Home</a></li>
<li><a href="#">About</a></li>
<li><a href="#">Contact</a></li>
<li><a href="#">Privacy Policy</a></li>
<li><a href="#">Terms and Conditions</a></li>
</ul>
<p>&copy; 2011 Super Awesome Site, Inc. All rights reserved.</p>
</footer>

</body>
</html>
```

## 文件夹结构

在上一个例子中，我们讨论了将文件分割成更小的结构以使其更易于管理。随着文件增多，你可能还希望创建目录来按功能分组存储特定文件。

在图 4–8 中，我为一个虚构的应用程序创建了一个模拟文件夹结构。就像在文档中分隔代码一样，以一种整洁的方式安排你的文件夹结构也是一个好习惯，这样你就可以在应用程序的整个开发生命周期中轻松找到所需的文件。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_66_0.png)

**图 4–8。** 在 Adobe Dreamweaver CS5.5 的文件浏览器中看到的一个组织有序的模拟文件夹结构

这里我们坚持使用一个非常基础的结构，其中所有的资源目录（例如我们的 css、img 和 js 文件夹）都位于站点的文档根文件夹中，并且有一个模板文件夹，其中将包含我们 Web 应用程序不同页面的模板代码。

在模板文件夹内部，有一个 includes 文件夹，我们将用来存放应用程序中使用的文档，例如页眉或页脚的标记代码，甚至可能是一些随机的内容块。参考我们之前关于相对路径部分的示例，图 4–8 中 index.php 文件中的 include 行将把页脚文件引用为 include('template/includes/footer.php')。这不仅保持了事物的分离，而且在逻辑上也有意义。页脚是模板的一部分，并且几乎在所有地方都会被包含，因此它位于模板目录内的 includes 目录中。

现在，当需要开发我们的应用程序或在未来进行更新时，我们就不必试图记住所有代码的位置，因为我们可以轻松而有逻辑地一目了然地找到它。

如果我们想编辑联系页面上的信息，我们只需编辑位于 /template/contact.php 的模板文件。如果我们发现页眉文件有问题，我们可以轻松地进入 /template/includes/header.php 并随心所欲地进行任何需要的更改，然后让这些更改反映在整个应用程序中。

## 总结

希望现在你已经读到了又一章的结尾，你对在实际编码开始之前，创建 Web 应用程序甚至网站所需的思考过程和工作有了更好的了解。如果你在代理公司、工作室或其他以开发者为中心的企业工作，那么你可能会在一个团队中工作，每个人负责自己的任务，并在转交给作为开发者的你之前处理规划的不同部分。（你可能还会有更多的测试团队、开发里程碑、构建等。）然而，如果你是为自己工作，你现在知道该做些什么来让你的生活稍微容易承受一些，让你的工作量稍微整洁一些。

# 第 5 章：使用 CSS 3 处理多种屏幕分辨率

设计网站时最难处理的事情之一是你可能遇到的无数种不同的用户配置。现代 Web 浏览器和操作系统是高度可配置的，不同的选项会影响你的 Web 应用程序的显示方式。在本章中，我们将专门讨论屏幕分辨率——或屏幕上的像素数量——以及如何使用 CSS 3 来适应不同的分辨率设置。

## 疲劳眼睛与分辨率进化的历史

如果你曾在深夜使用计算机，也许是在漫长的一天工作之后，你可能发现了一个有用的技巧：你可以更改屏幕上对象的大小，以便让眼睛更容易阅读。这通常涉及更改计算机的显示分辨率。分辨率就是屏幕显示的像素数量，由两个数字给出——第一个是像素宽度，第二个是像素高度。通过更改分辨率，通常是从高分辨率（如 2560 x 1600——顺便说一句，我晚上 7 点打这一页时用的就是这个）降低到较低的分辨率（也许是 1600 x 1200——一个不错的晚上 11 点的分辨率），你正在移除单个像素，这意味着你屏幕上的项目将显得更大。

在 1990 年代末，随着人们开始大量上网，标准分辨率被称为 VGA（视频图形阵列），通常设置为 640 x 480。随着时间的推移，显示器变得更大、更便宜、更高效，大多数用户采用了 SVGA（S 代表 Super——老实说！），分辨率为 800 x 600。这又被 XGA（扩展图形阵列——谢天谢地不是 Xtreme）所取代，分辨率为 1024 x 768 或更大。今天，我的显示器显示的是 WQHD（宽四倍高清），分辨率为前面提到的 2560 x 1600。

可以想象，网页设计师多年来一直在与屏幕分辨率作斗争，自从 640 x 480 不再流行以来。他们最终分化为两个阵营——支持为一种分辨率设计（“固定宽度”）的人，以及为多种分辨率设计（“弹性宽度”）的人。固定宽度派认为最好的网页设计是你绝对确定所有用户都能看到你的网站尽可能接近你设计的方式。这意味着选择一个分辨率，例如 1024 x 768，并设计你的页面以利用那个空间（参见图 5–1）。如果用户设置了更大的分辨率，你的页面两侧将只是有额外的空间，但表格和布局将保持在你想要的位置，在你的 1024 像素宽度内（参见图 5–2）。如果用户——可怕地——设置了更小的分辨率，那么你的内容将占据比他们可用的更多的屏幕空间，他们将被迫为你页面使用绝对可怕的水平滚动条。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_69_0.png)

**图 5–1。** *固定宽度网页在 1024 x 600 分辨率下的示例*

![](img/8b0ff5e51ddb912cd941bb18cf27206a_70_0.png)

**图 5–2。** *固定宽度网页在 1920 x 1080 分辨率下的示例*

相比之下，弹性宽度布局将尝试适应所有大小的分辨率（参见图 5–3 和 5–4）。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_70_1.png)

**图 5–3。** *弹性宽度网页在 1024 x 600 分辨率下的示例*

![](img/8b0ff5e51ddb912cd941bb18cf27206a_71_0.png)

**图 5–4。** *同一页面在 2048 x 1536 分辨率下的示例*

到目前为止，你可能已经开始看你的智能手机或平板电脑，并想：“嗯……不知道这东西的分辨率是多少？”你知道吗？大多数移动网页设计师也在想同样的事情。目前，Android 每天的激活量徘徊在 35 万台左右，设计师和开发者 alike 都意识到他们需要对他们开发 Web 应用程序的方法做出重大改变，以便在使用我们日常使用的各种设备浏览网络时保持相关性。如果你倾向于固定宽度的方法，这是一场艰难的游戏：我该为哪个分辨率构建我的移动应用程序？有一些简单的答案（“嗯，大多数人有 iPhone，我就只针对那个构建”），但它们也有缺点（“什么？！？他们做了一个更大的 iPhone 叫 iPad……呃哦……”）。通过针对特定设备，你也会惹恼除目标设备之外的任何设备的用户。

在本章中，我们将为你提供一点“屏幕分辨率”。也就是说，我们将尝试通过讨论你的移动 Web 应用程序如何能够智能地理解你用户使用的设备的分辨率，甚至方向，并自动适应它来解决这个问题。这就像你正在编写一个小的大脑，它会说：“嗯，这个设备宽度很大；让我们尽可能多地显示一切”或者“哦，不；这是一个小屏幕。我们不能并排显示这些信息！”作为设计师，我们可以通过让它向不同设备显示相同内容的不同方式——进而向不同用户显示——来利用这个小大脑并使其更加智能。让我们从一个例子开始。



## 每日机器人报

假设你决定为安卓用户创办一份日报，并想出了一个很棒的名字：每日机器人报。唯一的问题是，你的部分用户使用的是摩托罗拉 Xoom，分辨率为 2048 x 1536；部分用户使用的是三星 Galaxy Tab（分辨率为 1024 x 600）；还有一些用户使用的是 Roccwest XTreme，不知为何其分辨率为 1280 x 800。如果你只针对其中一种设备进行优化，那么固定宽度的页面在其他两种设备上的显示效果就不会太理想。幸运的是，我们可以编写一个页面，使其在三种设备上都能完美显示——参见图 5-5 至图 5-7：

![](img/8b0ff5e51ddb912cd941bb18cf27206a_72_0.png)

图 5-5. 分辨率为 1024 x 600 时的每日机器人报

![](img/8b0ff5e51ddb912cd941bb18cf27206a_73_0.png)

![](img/8b0ff5e51ddb912cd941bb18cf27206a_73_1.png)

将这几张图并排比较可能会令人非常惊讶——内容完全相同，但布局却发生了显著变化。更神奇的是，这是同一个页面——我们的开发人员只需创建一次，就能让它智能地适应这三种不同的分辨率^1。

那么，对于那些没有平板电脑的朋友们呢？好吧，只需稍加调整，我们同样可以为他们提供《每日机器人报 智能手机版》，如图 5-8（竖屏模式）和图 5-9（横屏模式）所示。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_74_0.png)

^1 在本例中，开发人员（Rocco）完全不知道负责撰写说明文字的人员（Jon）会选择哪些分辨率，但页面效果依然很棒。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_75_0.png)

让我们来研究一下《每日机器人报》背后的代码，以了解该页面的构建方式，以及我们如何判断它应该显示“智能手机版”还是“平板电脑版”。我们将在下一节介绍 HTML，然后在随后的节中介绍 CSS。阅读以下代码时，你应该能根据注释了解每个部分的功能。

### 每日机器人报的基础 HTML 代码

我们将其 HTML 分解为几个部分，以便你能够逐步理解。第一部分如清单 5-1 所示，我们创建了初始的 HTML 布局并指定了两个不同的页眉。

清单 5-1. 每日机器人报的 HTML 代码 第一部分

.Features Overview
| Feature | Description | Status |
| --- | --- | --- |
| ID | SPEC-001 | Active |
| priority | High | - |
| owner | team-alpha | - |

```
<!DOCTYPE HTML>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<meta charset="utf-8">
<title>The Daily Droid</title>
<meta name="description" content="An Android Responsive Web Design Demonstration.">
<meta name="author" content="Rocco Augusto">

<!-- Here we set the viewport so the device knows that this page is not one that can scale/zoom -->
<meta name="viewport" content="width=device-width; initial-scale=1.0; maximum-scale=1.0; user-scalable=0;" />
<link href="style.css" rel="stylesheet" type="text/css" >

<!-- Here we pull in two fonts from the Google Font API database -->
<link href="http://fonts.googleapis.com/css?family=UnifrakturCook:bold" rel="stylesheet" type="text/css">
<link href='http://fonts.googleapis.com/css?family=Bevan' rel='stylesheet' type='text/css'>
```

```
</head>

<!--
    HEADER
    We are adding two different sub headings (h6) to this page.
    One heading will be for the "Smartphone Edition" of the
    page and the second will be for the "Tablet Edition"
    of the page. Both pages are the same but depending on
    the screen size the pages CSS will tell the browser which
    subheading to display.
-->
<header id="mast">
    <hgroup>
        <h1>The Daily Droid</h1>
        <h6>Smartphone Edition</h6>
        <h6>Tablet Edition</h6>
    </hgroup>
    <time datetime="2011-05-29">May 29th, 2011</time>
</header><!-- /HEADER -->
```

如清单 5-1 中的代码所示，智能手机版和平板电脑版文本都出现在 HTML 中。CSS（将在本节后续的“每日机器人报 CSS”中讨论）将选择正确的一个进行显示。在 HTML 的第二部分，如清单 5-2 所示，我们将布局内容区域和文章空间，然后完成 HTML 结构。

#### 清单 5-2. 每日机器人报的 HTML 代码，第二部分

```
<section id="content">
    <!--
        SECTION: FEATURED ARTICLES
        The featured article would be the main article on the page
        that will be featured. Think of it in this sense as the
        front page story on a newspaper - which makes sense since
        this demo's completed code would be a mock vintage newspaper
        layout.

        The article contains several sections. You have the header
        section which contains the title of the article as well as
        a "figure" or image that would be displayed with the article
        and any caption text that would go along with it.
    -->
    <section id="featured">
        <article>
            <header>
                <h1>Title goes here...</h1>
                <figure>
                    <img src="ww1647-05.jpg" width="100%" alt="" />
                    <figcaption>Figure caption...</figcaption>
                </figure>
            </header>
            <div class="entry">
                <p>Article content goes here...</p>
            </div>
        </article><!-- /ARTICLE -->
    </section><!-- /SECTION: FEATURED ARTICLES -->

    <!--
        SECTION: REGULAR ARTICLES
```

本页面的常规文章将放置在此部分。此部分的标记与特色文章部分完全相同。唯一的区别将取决于它们被分配的样式所决定的显示方式。

```
    -->
    <section id="regular">
        <article>
            <header>
                <h2>Title...</h2>
            </header>
            <div class="entry">
                <p>Body Content...</p>
            </div>
        </article><!-- /ARTICLE-->
    </section><!-- /SECTION: REGULAR ARTICLES -->

</section><!-- /SECTION: CONTENT -->
<body>
</body>
</html>
```

现在让我们转向 CSS 以及《每日机器人报》的视觉呈现。

### 每日机器人报的半神奇 CSS 代码

以下是用于设置《每日机器人报》整体外观的 CSS 样式表。正如你所记得的，CSS 会获取在上一节中解释的纯 HTML 结构，并按照我们的指定为标签应用各种样式。我们将 CSS 分解为几个部分，以帮助解释其功能。第一部分如清单 5-3 所示，设置正文文本和部分标题的样式。

**清单 5-3.** *每日机器人报的 CSS 代码，第一部分*

```
/*
    CSS reset code only for the elements that will be
    used in our code. We could use a more robust CSS reset
    solution, but I am a firm believer that you should not
    riddle your stylesheet with code that you have no
    intention of using in your markup.
*/
html, body, h1, h2, h6, p, article, figure, figcaption header, hgroup, section {
    padding:0;
    margin:0;
}
/*
    General global styles to be used throughout the demo
*/
html, body {
    width:100%;
    overflow-x:hidden;
}
body {
    font-size:14px;
    font-family:"Times New Roman", Times, serif;
    line-height:20px;
```

```
background:url(bg.png);
-webkit-box-shadow: inset 0 -5px 300px rgba(153,99,38,1); /* This inset box-shadow
adds gives the page a nice vintage feel to it */
box-shadow: inset 0 -5px 300px rgba(153,99,38,1);
}
h1, h2 {
    font-weight:normal;
}
h1 {
    font-size:36px;
    line-height:42px;
}
h2 {
    font-size:20px;
}
h6 {
    font-size:16px;
    text-transform:uppercase;
}
p {
    margin:10px 0;
}
/*
    Header/Mast CSS code
*/
#mast {
    padding:20px 0 0 0;
    text-align:center;
    letter-spacing:1px;
}
#mast h1 {
    font-family:'UnifrakturCook', Georgia, "Times New Roman", Times, serif;
    font-size:62px;
    line-height:48px;
}
```

现在我们已经设置好了一些 CSS，是时候查看在“平板电脑版”和“智能手机版”之间切换的代码了。默认情况下，我们希望显示平板电脑版，因此代码如清单 5-4 所示：

#### 清单 5-4. 每日机器人报的 CSS 代码，第二部分

```
#mast h6 {
    display:none; /* hiding both of the pages subheaders */
}
#mast h6:nth-child(3) {
    display:block; /* displaying the "Tablet Edition" subheader by default */
}
#mast time {
    display:block;
    margin:10px 0;
    border-top:double 6px #000;
    border-bottom:double 6px #000;
    text-transform:uppercase;
    font-size:16px;
    line-height:24px;
}
```



文章/内容样式。
本节将主要依赖 CSS3 的两大新特性：弹性盒模型和多列布局。

弹性盒模型可能是我最喜爱的 CSS3 新特性之一。简而言之，它允许开发者使用灵活的盒子网格来控制页面布局，从而基本消除了在代码中通过不当使用浮动来拼凑布局的需求。

CSS3 多列布局是另一个节省时间的新特性，它允许设计师/开发者将一段代码块自动转换为基于列的布局，非常适合报纸式的展示。

```
#content {
    padding:0 10px;
    display:-webkit-box; /* here we are using the -webkit-box argument instead of
        plain old "box," so our code will work across newer and
        older Android browsers */
    -webkit-box-orient: horizontal; /* setting the box orientation to horizontal
        displays the content in this container from
        left to right instead displaying the content
        in the traditional way of top to bottom */
}
#featured {
    max-width:50%; /* our featured article will take up half the width of the display */
    height:100%; /* our featured article will take up all of the available height of the
    display */
    box-flex:1; /* tell our child elements to be evenly sized and take up one "box"
    space */
    -webkit-box-flex:1;
}
#featured .entry {
    -webkit-column-count: 2; /* this will display our featured content article text in 2
    columns */
    -webkit-column-gap: 20px; /* here we add a hearty 20px gap/spacing between our
    columns */
    -webkit-column-rule: 1px solid rgba(91,58,21,0.5); /* here we are adding a border to
    our columns */
}
#regular {
    margin-left:5px;
    padding-left:10px;
    max-width:49%;
    box-flex:1;
    -webkit-box-flex:1;
    -webkit-column-count: ublisher: 3;
    -webkit-column-gap: 20px;
    -webkit-column-rule: 1px solid rgba(91,58,21,0.5);
    border-left: 1px solid rgba(91,58,21,0.5);    /* here we are adding a border to the
    #regular container to match the rest of the columns' borders */
}
#regular article {
    display:inline; /* displaying our articles inline prevents our articles from
stacking on top of each other */
}
article h1, article h2 {
    margin-bottom:10px;
    font-family:Bevan, "Times New Roman", Times, serif;
}
article .entry {
    text-align:justify; /* to give the page a more realistic feel we will justify the
column text */
}
article figure {
    width:90%;
    padding:0;
    margin:10px auto 20px auto;
}
article figcaption {
    font-style:italic;
    text-align:right;
}
```

现在，我们将设置智能手机代码（如代码清单 5–5 所示），并相应地调整布局。

**代码清单 5–5. The Daily Droid 的 CSS 代码，第 3 部分**

```
/*
    Android Smartphone Devices
    Here we will use CSS3 media queries to determine
    the resolution of our screen and present the user with
    a completely different layout if their viewing
    does not meet certain requirements.

    Here we are targeting smartphone devices that will,
    on average, have a width of 320px (portrait) and up
    to 569px (landscape).

    This layout will display the content in a more
    commonly used smartphone style layout, presenting the
    user with a list of articles that they can scroll up
    and down to view.
*/
@media screen and (min-width: 320px) and (max-width: 569px) {
    body {
        -webkit-box-shadow: inset 0 -5px 50px rgba(153,99,38,1); /* lessen the shadow on
the page to adjust to the screen's new dimensions */
        box-shadow: inset 0 -5px 50px rgba(153,99,38,1);
    }
    h1 {
        font-size:20px;  /* lower the size of the header font to accommodate the smaller
screen resolution */
        line-height:24px;
    }
    h6 {
        font-size:12px; /* same as the h1 above it */
    }
    #mast h1 {
        font-family:'UnifrakturCook', Georgia, "Times New Roman", Times, serif;
        font-size:42px;
        line-height:42px;
    }
    #mast h6:nth-child(2) {
        display:block; /* since we are dealing with a smaller screen we will show the "Smartphone Edition" subheader */
    }
    #mast h6:nth-child(3) {
        display:none; /* and hide the "Tablet Edition" subheader */
    }
    #mast time {
        font-size:12px;
        line-height:24px;
    }
    section#content {
        -webkit-box-orient: vertical; /* here we are telling this content to display vertically instead of horizontally */
        padding-bottom:15px;
    }
    #featured {
        max-width:100%; /* take up the entire width of the screen instead of half of it */
    }
    #featured .entry {
        -webkit-column-count: 1; /* only display our text in a single column, which is more appropriate for our screen real estate */
        -webkit-column-gap: 0; /* remove the 20px padding around columns */
        -webkit-column-rule: none; /* remove the border off our columns */
    }
    #regular {
        margin-left:0px;
        padding-left:0px;
        max-width:100%; /* like our featured article we will now take up the entire width of the page */
        -webkit-column-count: 1; /* like our featured article we will display a single column of text */
        -webkit-column-gap: 0;
        -webkit-column-rule: none;
        border-left: none;
    }
    #regular article {
        display:block; /* display our articles as blocks so they appear vertical */
    }
    article .entry p, article figure {
        display:none; /* hide all of our article content so the user is not stuck scrolling into oblivion */
    }
    article .entry p:first-child {
        display:block; /* display only the first paragraph of an article for the user */
    }
    article {
        margin-bottom:10px;
        border-bottom:2px solid rgba(0,0,0,1);
    }
}
```

对于一份简单的报纸来说，这代码量似乎很大；然而，它的美妙之处在于其通用性：一个 HTML 页面和一个 CSS 页面就能掌控所有设备——手机、平板电脑、Android 媒体播放器，以及任何其他运行 Android 的设备！让我们花点时间来讨论一下，这种魔法是如何通过媒体查询实现的。

## 媒体查询

当你查看前面的代码时，你可能首先注意到的是，这个流畅的复古报纸布局程序只由两个相对较小的代码文件构成。五到七年前，在一个网站开发者需要身兼两职的时代——既是网站开发者又是 Internet Explorer 6 的黑客——创建这样一个布局将是极其繁琐的任务，很可能需要创建两个甚至更多完全不同的布局。每个布局都必须拥有自己的一套 HTML 和 CSS 文件，然后由某个后端服务器代码根据查询到的设备用户代理字符串，将这些文件提供给客户端。移动设备将被提供专门为移动设备设计的 HTML 和 CSS 模板。台式计算机则会获得桌面版的等效模板。不同版本的代码之间没有融合或流动性可言。

快进几年到未来——我们正处于 HTML5 和 CSS3 时代的黎明——景象已完全不同。如今，我们生活在一个桌面互联网浏览器开发和发布速度之快，让大多数用户都来不及安装最新更新的时代。在移动领域，进步程度几乎同样显著，智能手机操作系统的新版本，以及随之而来的功能丰富的网络浏览器新版本，正以每六到十二个月甚至更短的时间间隔发布！

对于你，这位移动网站开发者来说，这意味着你不必再受困于过去，为十年甚至更老的浏览器编写网站代码。最多，作为一名专注于 Android 用户体验的开发者，你实际上只需考虑过去一年半内发布的 Android 版本。能够专注于更新的设备，而无需因过分关注过去的技术而担心损害用户体验的能力，赋予了开发者一种我们以前不曾拥有的自由。伴随着这种自由而来的是创新，而创新又带来了更好的技术和功能——比如 CSS3 媒体查询——正是这项技术让我们得以构建之前展示的那个精美的 "The Daily Droid" 演示。

媒体查询自 HTML4 时代起，就以某种形式成为网站开发的一部分。在那段充斥着 `font` 标签和嵌套表格的黑暗时期，媒体类型通过控制与用户查看内容所用媒介相关的样式和样式表而声名鹊起（参见图 5–10 和 5–11）。例如，开发者可能会为“打印”媒体类型指定某些样式，以移除博客文章中的所有广告，这样用户在打印博客内容时就不会不必要地浪费昂贵的墨水（参见代码清单 5–6）。



## 第五章：使用CSS 3处理多种屏幕分辨率

代码清单5–6。媒体查询示例1：基于媒体类型隐藏或显示块

```css
<style type="text/css" media="screen">
    #advertisements {
        display: block;
    }
</style>

<style type="text/css" media="print">
    #advertisements {
        display: none;
    }
</style>
```

![](img/8b0ff5e51ddb912cd941bb18cf27206a_83_0.png)

图5–10。在普通桌面网页浏览器中查看Android Thoughts主页

# Android Thoughts - 关于Android设备的观点、新闻、建议和评测

关注我们的Twitter，获取网站上不常发布的独家内容！

-   - Apple Thoughts
- Laptop Thoughts
- Digital Home Thoughts

-   - 首页
- 论坛
- 新帖
- 注册
- 文章
- 评测
- 商店
- 联系我们
- 关于
- 搜索

![](img/8b0ff5e51ddb912cd941bb18cf27206a_84_0.png)

开发者也可以为“投影”媒体类型分配样式或样式表，以解决在会议室中使用投影仪查看项目时网站页眉颜色变淡的问题（参见代码清单5–7）。

### 代码清单5–7。媒体查询示例2：基于媒体类型更改背景颜色

```css
<style type="text/css" media="screen">
    #header {
        background: #444444;
    }
</style>

<style type="text/css" media="projection">
    #header {
        background: #111111;
    }
</style>
```

然而，有了CSS3，媒体类型的概念已经演变成更美妙、更灵活的东西，这使得级联样式表不仅仅是一个为网页和标记添加样式的“笨”机制。

媒体查询在使用时，会让人感觉它本应从一开始就属于CSS的一部分。我听过一些朋友称媒体查询为“自由”，甚至听过一位我认识的开发者——没错，是在一个漫长的编码之夜后——简单地将媒体查询称为数字时代的新“黑魔法”。实际上，它们都不是。媒体查询是一种工具，一旦掌握，就能让你作为开发者的工作更轻松，最终为你带来一个精美灵活的布局，它能在用户眼前瞬间转换为其观看媒介！

如果你曾使用过JavaScript或任何其他脚本或编程语言，那么媒体查询对你来说可能很容易学习。基本上，所做的就是为你的样式表分配逻辑，让客户端的浏览器在分配正确的模板样式到正确的观看设备方面完成所有繁重的工作。以下是一个使用CSS媒体查询的非常基础的示例：

```html
<link rel="stylesheet" media="screen and (orientation:portrait)" href="portrait.css" />
```

在这个例子中，我们告诉客户端的浏览器，当浏览器从处于垂直位置的移动设备查看应用程序或网站时，加载“portrait.css”样式表。² 你并不限于将媒体查询分配给链接标签。媒体查询也可以直接添加到你设备的CSS文件中，正如我们之前在“The Daily Droid”示例中看到的那样。事实上，甚至可以使用@import规则调用CSS文件时调用媒体查询，以实现正确的显示，如以下示例：

```css
<style type="text/css">
	@import url(landscape.css) screen and (orientation:landscape);
</style>
```

在接下来的示例中，我们将有多个@import规则导入许多不同的CSS文件，用于不同的布局类型（参见代码清单5–8）。

### 代码清单5–8：媒体查询示例3

```css
<style type="text/css">
	<!-- 针对智能手机横屏显示的样式 -->
	@import url(landscape.css) handheld and (orientation:landscape) and (max-width:480px);

	<!-- 针对Honeycomb平板电脑横屏显示的样式 -->
	@import url(landscape.css) handheld and (orientation:landscape) and (max-width:648px);

	<!-- 针对竖屏显示的样式 -->
	@import url(landscape.css) all and (orientation:portrait);
</style>
```

² 具有运动检测传感器的设备通常会告知软件手机是否从横屏切换到竖屏视图，从而允许你的网页根据定义的样式自动重新格式化。

我完全知道你在想什么，“如果我必须为连接到电视或具有16x9显示屏的设备的Google TV Android设备编写我的Web应用程序，该怎么办？！”别担心，因为CSS3媒体查询的灵活性已经为你准备好了，正如以下示例所示：

```html
<link rel="stylesheet" media="all and (device-aspect-ratio: 16/9)" href="television.css" />
```

从这些前面的例子可以看出，在一个迅速被支持HTML5和CSS3的设备和应用程序主导的世界里，媒体查询是任何Web开发者工具库中一个不可思议的工具。要了解更多关于媒体查询威力的信息，请查看W3.org网站这里——www.w3.org/TR/css3-mediaqueries/#media0。

## 总结

在本章中，我们讨论了很多关于你网页的大小以及该大小如何根据查看内容的屏幕而变化。现在我们已经解决了屏幕分辨率的问题，我们将稍微放大一点，讨论处理不同浏览器的最佳方法！

## 处理不同的浏览器平台

到目前为止，我们已经讨论了检测访问你的网页或应用程序的设备类型并进行相应处理的方法。这涉及特殊的CSS文件、格式问题等等。然而，正如任何优秀的面包师会告诉你的，把所有的鸡蛋放在一个篮子里并不总是明智的。这就是为什么，在本章中，我们将退一步讨论你可以用来了解什么设备正在访问你的服务并采取适当行动的方法。

原因很简单：没有一种解决方案能解决所有问题。例如，你可能需要允许移动用户访问一个Web应用程序，并且你可能发现可以格式化在桌面和手机上都看起来很棒的页面。对于极其简单的布局，开发者通常会这样做。然而，对于更复杂的系统，可能需要创建一个完全独立的网站。折中的方法是构建一个HTML文档，使其在桌面、平板电脑或手机上都能看起来不错。在本章中，我们将为你提供必要的工具来确定什么设备正在查看你的页面，并提供一些关于你的页面如何对每种设备做出反应的想法。毕竟，正如没有两个网站是完全相同的一样——尽管相似——没有两个设备的行为会完全相同（但值得庆幸的是，与网站一样，它们之间有相似之处）。

### META标签和视口

我们已经讨论了很多关于HTML对普通用户隐藏的内容——使用的不同标签、不同的部分（如head和body），甚至CSS和JavaScript如何嵌入到HTML文档中。然而，META标签或元素是特殊的，因为虽然它们不向用户显示，但它们通常会影响用户对页面显示或格式的体验。

META标签位于HTML页面的head部分，通常有两个元素：元素的名称和值。例如，以下值指定了与特定网页关联的关键词：

```html
<meta name="keywords" content="android, howto, information" >
```

### META小历史

早在搜索引擎开始索引互联网时，它们就使用关键词和描述META元素来理解给定网页的内容。在1990年代后期，全文搜索引擎（如Google）开始索引并使用给定网页的所有文本来确定页面包含的内容，这些META元素变得不那么重要了。事实上，一个完整的行业已经兴起，声称通过“优化”网页来帮助网页所有者获得更多流量，这通常包括更新搜索引擎使用的META元素。这个“搜索引擎优化”或SEO行业至今仍然存在，事实上是一种非常残酷的业务类型，尽管许多搜索引擎会寻找使用过的旧“把戏”，并且今天可能会因使用它们而惩罚页面。例如，一个使用的把戏被非正式地称为“关键词堆砌”，正如其名称所示——在META关键词元素中塞入许多不同的术语，其中一些可能对搜索引擎得分很高，但关于页面的实际内容并不完全准确。现代的SEO公司必须依赖许多其他技术来提高页面的搜索排名，包括许多我们通常作为设计师不考虑的事情（例如，页面上有哪些链接、页面标题、布局、措辞等）。

META标签的一个有趣之处在于，网络上实际存在的META标签总数远少于“官方”META标签。各种制作网络浏览器的软件公司，如微软，可能会决定构建他们的浏览器来检测“非官方”META标签并对其做出响应。

例如，微软率先使用了MobileOptimized META标签，它告诉其移动互联网浏览器（Pocket Internet Explorer或Internet Explorer Mobile）如何专门渲染使用了此标签的页面。一些非微软生产的浏览器也支持该标签，但无法保证该标签能像帮助Internet Explorer用户那样帮助竞争对手浏览器的用户。同样，我们之前提到的老朋友AvantGo使用了一个名为HandheldFriendly的标签，目的大致相同，但也存在同样的问题。

### Viewport元素

所有这些混乱、竞争和不一致性导致了一个新的META元素Viewport的引入和相当广泛的接受，虽然它仍然是非官方的，但它是当前移动开发者最感兴趣的“特殊”META标签。Viewport可以被看作是网页之上的一个窗口。有时整个网页都适合窗口，而有时我们想根据页面构建方式以不同方式调整窗口大小。Viewport标签更成功的一个原因



## 6.2 Viewport

Viewport 标签可以提供比以前尝试更多的信息量。例如，一个简单的 Viewport 标签可能如下所示：

```html
<meta name="viewport" content="width=320,height=device-height" />
```

这段代码告诉移动浏览器，此页面的内容宽度应为 320 像素，高度与设备屏幕相同。（如果您是为平板电脑设计，您可能会将其调整为 800px 宽。）为了更好地了解此设置如何显示页面，请参阅图 6-1。它展示了我们在第 2 章中使用上述视口设置制作的“Who's That Tweet?”游戏。

![Figure 6-1](img/8b0ff5e51ddb912cd941bb18cf27206a_89_0.png)

**图 6-1.** *这是我们设置了视口的“Who's That Tweet?”游戏*

请注意，页面的布局比手机可用的显示区域大？这是因为虽然我们将高度设置为设备的高度，但我们将宽度设置得过宽——320px——浏览器对初始缩放一无所知，这从页面底部的缩放按钮可以看出。在这种情况下，浏览器放大了页面以显示左上角，并提供了缩放按钮，以便用户可以缩放页面以查看他们选择的任意多或任意少的页面内容（虽然有时可以缩放页面上的内容很好，但如果我们可以在此页面上禁用该功能以保证我们的布局能按预期显示，那就更好了）。换句话说，浏览器对其应如何显示此页面做出了一个合理的猜测，但通过将其拉到左上角，它失败得很彻底。它也可能以缩小的方式显示所有内容，那样 320px 就能全部显示，但文本会非常小。我们将给它更多信息，以便它第一次就能正确显示。

幸运的是，Viewport 标签也可以包含有关页面缩放的信息——包括用户缩放给定页面的能力。下面这个稍微复杂一些的 Viewport 标签指定了所有这些内容：

```html
<meta name="viewport" content="width=没去, height=device-height, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0" />
```

这段代码告诉浏览器两件事。首先，它提供了缩放值，使浏览器知道您认为的最大和最小缩放比例，以及初始缩放设置。在此示例中，我们告诉浏览器，我们编写页面时设计为以 100% 视图显示，并且不应再大或再小。其次，此代码还增加了关闭用户缩放选项的能力，如图 6-2 所示。现在我们不必担心我们的设计不能按我们意图的方式呈现给用户。就个人而言，我总是喜欢在构建移动网站或应用程序时剥夺用户缩放页面的能力。我知道有些人真的喜欢通过捏合和缩放来调整大小，但实际上，移动设备的屏幕空间非常有限，我认为作为设计者或开发者，您的工作是利用有限的屏幕空间来发挥优势，而不是让用户承担额外的负担，让他们通过捏合和缩放来浏览您完成的产品。

![Figure 6-2](img/8b0ff5e51ddb912cd941bb18cf27206a_90_0.png)

**图 6-2.** 第 2 章的“Who's That Tweet?”游戏，用户缩放功能已关闭

但是，如果您希望折中一下，即您的应用应该自动缩放，但也允许用户根据他们的意愿修改缩放呢？对于具有更高像素密度（例如 Google Nexus One，宽 480px）的设备又该如何处理呢？我们可以通过几种方式来解决这个问题。第一种是直接删除 META 标签中的 `user-scalable=no」`行，并调整针对特定屏幕密度的缩放值。这允许 META 标签提供初始值，但不限制用户。为了确定这是否是正确的做法，我们可以进行一些用户测试（例如，调查用户对我们移动界面的看法），或者如果我们真的很好奇，我们可以实现一些 `JavaScript` 代码来查看用户的行为，然后将其写入日志（这超出了本书的范围，尽管存在相关资源，例如此页面上的讨论：http://htmldoodads.appspot.com/zoom-level.html）。我们还可以构建一个根据设备像素密度而显示不同的页面——这必须在底层 CSS 中指定，使用低密度 (`ldpi`)、中等密度 (`mdpi`) 和高密度 (`hdpi`) 的标签，然后为每种情况指定不同的 CSS 格式。

最后，如果我们有仅为一个平台（例如，仅 Android 手机）开发的便利，我们可以研究浏览器的特定功能。在这种情况下，Android WebKit 浏览器会自动缩小文本元素以适应屏幕（去在线报纸上看一篇文章，并放大一段宽文本，就能看到实际效果）。如果这是我们的使用场景，那么我们就不用担心 META 标签了。虽然依赖这一点很诱人，但您应该在 Android 设备上彻底测试您的页面。使用 META 标签作为帮助内置浏览器的额外安全层也没有坏处。

## 6.3 用户代理

有时，仅指定浏览器应如何处理您的页面并不足以满足您的需求。例如，也许您知道某些信息，无论它在移动设备上如何缩放或格式化，对于普通用户来说，在小屏幕上处理都太多了。也许您的页面使用了许多 Flash 小程序，这些程序在 iOS 设备（如 iPhone 或 iPad）上无法工作，您希望将这些用户重定向到其他地方。也许您网站上的某些功能和特性并非在所有应用程序中都可用，需要针对较不先进的浏览器禁用。最后，也许您只想提供一个网址，http://mysite.com，并让它自动将手机和平板电脑引导至特别优化的版本，同时向其他所有人显示完整页面。大多数网站实现这些目标的方式是通过读取由访问者网络浏览器提供的用户代理字符串。让我们先看一个用户代理示例，然后看看如何在我们的应用程序中使用它。

### 6.3.1 Nexus One 用户代理

用户代理字符串的格式由 RFC 1945（HTTP 规范）规定，该规范包含此字符串的定义。该字符串由产品名称和版本，以及一个可选的注释组成。虽然这些是 RFC 1945 要求的字符串部分，但许多供应商会添加其他信息，如操作系统、已加载的扩展和平台详细信息。Google Nexus One 上运行 Android 2.2 (Froyo) 的内置浏览器发送以下用户代理：

```
Mozilla/5.0 (Linux; U; Android 2.2; en-us; Nexus One Build/FRF91) AppleWebKit/533.1 (KHTML, like Gecko) Version/4.0 Mobile Safari/533.1
```

此字符串分解后翻译为：

- Mozilla 5.0 浏览器
- 运行 Linux 操作系统，具体是 Android 2.2
- 使用英语 - 美国 (en-us)
- 在 Nexus One 手机上，运行操作系统的构建版本 FRF91。
- （注释指示）类似于 AppleWebKit 浏览器（版本 533.1）。

我们的网页或应用程序可以获得大量信息（如果您查看 RFC，关于引擎或当前浏览器提供的安全级别可能会有更多信息）。使用这些信息，我们可以将特定手机、浏览器、操作系统和语言的用户引导到我们为他们创建的特别格式化的页面，或显示针对我们所针对的特定浏览器的功能。

然而，使用用户代理检测需要考虑一个警告：用户代理欺骗。许多第三方浏览器，例如 Android 上流行的 Dolphin HD 浏览器，允许用户设置自己的用户代理。这样做的原因有多种，包括：

- 用户希望查看页面的桌面版本，无论其格式看起来有多糟糕。
- 用户希望访问专门为另一个操作系统或浏览器构建的页面（即，也许网页开发者尚未构建优化的 Android 版本，但有一个优化的 iOS 版本）。
- 用户只是想出于某种原因出现在网站日志的桌面系统中！我能想到的一个例子是开发者设置的限制（即，只向桌面用户显示特别优惠），而移动用户希望查看它。

对于用户代理欺骗，我们能做的不多。毕竟，整个系统的设置都围绕着用户代理被准确报告。如果这是您关心的问题，您可能希望除了用户代理检测之外，还使用其他方法来为用户提供正确的页面，无论他们想要什么。这通常会采用脚本的形式，可以测试浏览器的功能——然而，人们需要知道移动浏览器具有哪些微小功能，而哪些只有桌面浏览器才有——这远远超出了我们这里的讨论范围。

现在您已经基本了解了用户代理字符串的用途，让我们看几个检测终端用户用户代理字符串的例子。



## PHP 用户代理检测

清单 6-1 展示了一个 PHP 示例，我们将检测用户代理字符串并将其显示给用户。如果用户使用的是 Android 网络浏览器，那么他们将会看到始终令人愉快的笑脸（参见图 6-3），但如果他们尝试在非 Android 设备上查看脚本，那么他们将会面对永远不受欢迎的皱眉表情（参见图 6-4）。

**清单 6-1.** *PHP 用户检测代码*

```
<?php
$userAgent = strtolower($_SERVER['HTTP_USER_AGENT']);
if(stripos($userAgent,'android') !== false) {
    echo 'You are using an Android web browser! :)';
}
else {
    echo 'You are not using an Android web browser! :('; 
}
?>
```

为了理解这段代码是如何工作的，我们将逐行剖析它。首先，我们定义变量 `$userAgent`，它获取请求页面的浏览器的用户代理字符串。然后我们使用 PHP 的 `stripos` 函数——用于在字符串中查找子字符串的出现位置——来解析用户代理中我们提供的值。如果值（在此例中是 `android`）未在字符串中找到，则会向用户显示一条消息。如果找到了，则会显示另一条消息。

这只是使用 PHP 检测用户代理字符串的一个小例子，但在许多情况下，这种技术可能会让你避免抓狂。例如，在 PHP 中使用检测可以在内容发送之前就将其阻止（通常这是 JavaScript 检测无法做到的）。此外，如果你的应用程序主要部分是用 PHP 编写的，你可能会更习惯用这种方式记录用户代理，而不是通过 JavaScript。

![img/8b0ff5e51ddb912cd941bb18cf27206a_93_0.png](img/8b0ff5e51ddb912cd941bb18cf27206a_93_0.png)

You are using an Android web browser! :)

**图 6-3.** *使用 PHP，我们获取用户代理字符串并用它来决定向最终用户显示哪些内容*

![img/8b0ff5e51ddb912cd941bb18cf27206a_94_0.png](img/8b0ff5e51ddb912cd941bb18cf27206a_94_0.png)

> 图 6-4：糟糕！看起来这个人没使用 Android 浏览器！

## JavaScript 用户代理检测

虽然 PHP 非常适合在服务器端检测用户代理字符串，但有时开发者可能需要在客户端检测用户代理字符串。举个例子，假设你正在开发一个网站或应用程序，它能让你将信息导出为用户电脑上的文本文件或二进制格式文件以供稍后查看。在 Android 设备上，文本没问题，但如果用户选择了二进制格式，当他们无法打开文件时可能会感到困惑。因此，我们可能只想隐藏该选项，只显示其他选项。幸运的是，使用 JavaScript 完成这项任务就像使用 PHP 一样简单。

### JavaScript 代理检测代码介绍

清单 6-2 中显示的 JavaScript 代码让我们快速体验了 JavaScript 检测可以多么简单；它与 PHP 类似。这段代码与之前代码的主要区别在于，我们没有像使用 PHP 那样将消息写入页面，而是选择向用户显示一个弹出警报对话框（参见图 6-5 和图 6-6）。

清单 6-2. JavaScript 用户检测代码

```
<script type="text/javascript">
var ua = navigator.userAgent.toLowerCase();
window.onload = function() {
    if(navigator.userAgent.match(/android/i)) {
        alert('Android Rocks!');
    }
    else {
        alert('Yawn, I guess your boring Desktop browser is okay');
    }
}
</script>
```

![img/8b0ff5e51ddb912cd941bb18cf27206a_95_0.png](img/8b0ff5e51ddb912cd941bb18cf27206a_95_0.png)

图 6-5. Android 2.3 Gingerbread 设备上的警报对话框

![img/8b0ff5e51ddb912cd941bb18cf27206a_95_1.png](img/8b0ff5e51ddb912cd941bb18cf27206a_95_1.png)

图 6-6. Google Chrome 网络浏览器上的无聊警报对话框

## 使用 JavaScript 代理检测向不同平台显示不同内容

单平台开发者（即为 Android、iOS 或仅一个操作系统编写应用的开发者）的一个自然进展是转向不同平台。网络应用程序在这方面非常出色，因为它们基本上可以编码一次，然后轻松“移植”到其他类似架构。然而，为了避免那些可能成为噩梦的衍生版本（即 Android 和 iOS 版本，需要你分别向两个版本添加内容），只拥有一段可以根据运行环境改变的代码可能更容易。在这个例子中，我们将向你展示如何将上一节清单 6-2 中的 JavaScript 代码实现到一个网络应用程序中，该程序将根据其运行环境显示不同的内容。

我们还将让你提前体验一下你将在下一章（jQuery Mobile）中经常看到的东西，将其作为此应用程序的“框架”。如果你喜欢接下来几个屏幕的外观，那么你会喜欢阅读第 7 章！

让我们首先讨论我们的总体目标：显示适当的应用程序下载链接。在 Android 中，我们希望链接指向 Android Market（或者可能是新开放的 Android 应用商店之一，例如亚马逊的应用商店）。在 iOS 中，我们希望链接指向 Apple App Store。我们还想显示相应的图形。让我们从构建一个显示 Android 链接的简单页面开始。我们首先需要获取图形（可在 Android 品牌页面 www.android.com/branding.html 获取，以及 Apple App Store 图形 www.apple.com/itunes/affiliates/resources/documentation/identity-guidelines.html），并将它们都放在与清单 6-3 相同的目录中。

清单 6-3. 下载我们应用的 HTML 页面

```
<!DOCTYPE HTML>
<html>

<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Download our App</title>
<link rel="stylesheet" href="//code.jquery.com/mobile/1.0.1/jquery.mobile-1.0.1.min.css"
/>
<script src="http://code.jquery.com/jquery-1.6.4.min.js"></script>
<script src="//code.jquery.com/mobile/1.0.1/jquery.mobile-1.0.1.min.js"></script>

<script type="text/javascript">

$( '#aboutPage' ).live( 'pageinit',function(event){

    if (navigator.userAgent.match(/android/i)) {
        document.getElementById("androiddiv").style.display = "block";
    }

    if (navigator.userAgent.match(/iPhone/i)) {
        document.getElementById("applediv").style.display = "block";
    }
});

</script>
</head>
<body>
<div data-role="page" id="aboutPage">
<div data-role="header">
<h1>Our App!</h1>
</div><!-- /header -->
<div data-role="content">
<div id="androiddiv" style="display: none">
<p>We have an application you can download in the Android Marketplace!</p>
<p align="center"><img src="45_avail_market_logo1.png"></p>
</div>
<div id="applediv" style="display: none">
<p>We have an application you can download in the Apple App Store!</p>
<p align="center"><img src="app-store.png"></p>
</div>
</div><!-- /content -->
<div data-role="footer">
<h4>bugjr.com</h4>
</div><!-- /footer -->
</div><!-- /page -->
</body>
</html>
```

你会注意到这个页面相当简单。如果你查看页面的内容，你会看到我们有两个内容块：第一个名为 `androiddiv`，显示 Android Marketplace 的文本和图像。第二个 `applediv` 显示 Apple App Store 的文本和图像。两个块在其 `div` 标签中都设置为 `display: none`，这意味着默认情况下都不显示。页面顶部是一个非常简单的 JavaScript 函数，它测试检测到的是哪个用户代理，并通过将 `display` 设置为 `block` 来切换相应文本块的显示。如果我们在 Android 网络浏览器中加载此页面，我们将看到图 6-7：

# 96 第 6 章：处理不同的浏览器平台

![img/8b0ff5e51ddb912cd941bb18cf27206a_98_0.png](img/8b0ff5e51ddb912cd941bb18cf27206a_98_0.png)

**图 6-7.** 在 Android 浏览器中加载下载应用 HTML 页面

然而，如果我们使用 iPhone 上的 Safari 加载此页面，我们将看到图 6-8：

![img/8b0ff5e51ddb912cd941bb18cf27206a_99_0.png](img/8b0ff5e51ddb912cd941bb18cf27206a_99_0.png)

图 6-8. *Safari 中的下载应用 HTML 页面*

现在我们有一个简单的方法将用户路由到正确的下载，而不需要他们点击这个或那个图标！可以想象，我们可以将同样的检测用于其他目的——向不同的用户显示不同的文本，显示不同的广告等等... 最好的部分是这一切都是用 HTML 和 JavaScript 实现的，这意味着如果你选择使用产品将你的 Web 应用转变为原生应用（我们将在第 13 章讨论，使用 PhoneGap 或 Titanium Mobile 等工具），你可以使用这个技巧为用户提供更高程度的自定义！

既然我们已经讨论了在 PHP 和 JavaScript 中检测用户代理，我们将最后讨论如何使用 Apache Web 服务器来为我们进行检测。

## .htaccess 用户代理检测

这些类型的文件是通常与 Apache Web 服务器关联的配置文件。也称为分布式配置文件，`.htaccess` 文件可以为 Web 应用程序设置一系列规则和配置，基于每个目录。`.htaccess` 文件可用于控制将 URL 重写为更干净、更易于人类阅读的形式，如果服务器支持的话，可以使用 `mod_rewrite` 模块。`.htaccess` 文件的另一个有趣用途是用它来检测用户代理字符串，并在需要时将用户定向到不同的站点或子域名。参见清单 6-4。



**图 6-4。*一个示例 .htaccess 文件***

```
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteBase /
RewriteCond %{HTTP_USER_AGENT} ^.*Android.*$
RewriteRule ^(.*)$ http://android.yoursitesurl.com [R=301]
</IfModule>
```

上述代码首先检查您的 Apache 服务器是否支持重写模块，然后启用重写引擎并设置条件和规则。该条件检查用户代理中是否包含“Android”，如果找到，则规则指示 Web 浏览器将请求重定向到 http://android.yoursiteurl.com，而不是您通常的 http://yoursiteurl.com（或用户输入的其他内容）。

这种类型的检测功能非常强大，但也会让一些用户感到烦恼。虽然用户可以通过禁用 JavaScript 来禁用 JavaScript 检测，但 .htaccess 和 PHP 用户代理检测只能通过更改用户代理来“欺骗”，并非所有浏览器都支持此操作。（值得注意的是，免费的海豚 HD 浏览器允许用户轻松在 Android、iOS 和桌面之间切换用户代理，使其在测试和欺骗方面非常有用！）此外，用户可能希望在 Android 浏览器中查看完整的网页，而 PHP 方法允许您通过代码提供一些切换功能（例如，用户点击的链接可以设置 PHP 会话变量，告知代码不要显示移动版网站），但 .htaccess 用户代理检测不允许这样做。然而，在简单情况下，.htaccess 解决方案是最易于配置的。明智地选择您的检测方法！

## 摘要

恭喜！您已经完成了另一个章节，凭借您对视口（Viewports）和用户代理字符串的新知识，您将更有能力处理不时会出现的某些讨厌的用户界面问题。尽管本书主要关注为 Android 设备构建 Web 应用程序，但认为您永远不会遇到需要开发跨平台解决方案的情况是愚蠢的。利用我们讨论的内容，您可以为您的应用程序量身定制高效且优雅的方案！

# 第 7 章

# 使用 jQuery Mobile 构建令人印象深刻的用户体验

信不信由你，我对于艺术才能并不具备太多天赋，毕竟我的母亲曾获得艺术学院的奖学金，而父亲曾在广告行业工作多年。我大部分的编程工作都侧重于功能而非样式……结果好坏参半。一方面，许多人称赞这种极简设计——例如，我的一款名为 *快餐热量查询* 的应用程序，基本上只有两个下拉框和几个按钮。拥有超过 1000 条评论，它在 Android 市场获得了 4.3 分（满分 5 分）的高评分。然而，每有一个人赞叹“如此易于导航，实用信息丰富！”（真实评论），也会有人无法理解为什么它看起来不够美观。

幸运的是，在 Web 应用程序领域，有一些选项可以让像我这样的设计“懒人”看起来像是聘请了价格高昂的设计师制作了精美的界面。实际上，有一些免费工具可以实现这一目标，在本章中我们将深入探讨其中之一：jQuery Mobile（http://jquerymobile.com）。这绝非您拥有的唯一选择。其他可供选择的是：Wink Toolkit（www.winktoolkit.org/）、Sencha Touch（www.sencha.com/products/touch/）、Zepto.js（http://zeptojs.com）、Jo（http://joapp.com/）、xui.js（http://xuijs.com/）以及 JQTouch（www.jqtouch.com/）。然而，就我们的目的而言，jQuery Mobile 在功能和配置简便性方面提供了最大的性价比。那么——让我们开始探索吧！

## 基础

如果您熟悉用于桌面浏览器的 jQuery UI 工具包，那么您将很快掌握 jQuery Mobile！jQuery Mobile 是那些试图将开发移动应用程序时的许多繁琐任务自动化出来的框架之一。

# **图 7-1。** *HTML 中一个无效自定义属性的示例*

```
<div class="post" mood="awesome">
<h1>Today was an awesome day!</h1>
<p>Suspendisse consectetur consequat risus non viverra. Phasellus ligula urna, egestas
porttitor facilisis vel, euismod sit...</p>
</div>
```

# **图 7-2。** *HTML5 中一个有效的自定义属性的示例*

```
<div class="post" data-mood="awesome">
<h1>Today was an awesome day!</h1>
<p>Suspendisse consectetur consequat risus non viverra. Phasellus ligula urna, egestas
porttitor facilisis vel, euismod sit...</p>
</div>
```

在第二个示例（图 7-2）中，我们使用 `data-mood` 属性以通过验证器认可的方式记录情绪，同时仍然允许我们在脚本中根据需要使用这些数据的！只要我们将在想存储的数据字符串前加上前缀“data-”，它就是有效的 HTML5 代码。我们可以将这些用作小型数据容器，如下例所示。

现在，您对数据属性的工作原理及其如何丰富我们的移动应用程序有了了解，让我们来看看一些 jQuery Mobile 代码，并剖析其运作机制。

在图 7-3 中，我们将使用 jQuery Mobile 框架显示一个非常简单的页面。您会注意到它使用了多个 `data-role` 属性。

# **图 7-3。** *默认 jQuery Mobile 模板示例的 HTML 标记*

```
<!DOCTYPE HTML>
<html>
<head>
<title>Our Super Rad Demo Page</title>
<link rel="stylesheet" href="http://code.jquery.com/mobile/1.0a1/jquery.mobile-1.0a1.min.css" />
<script src="http://code.jquery.com/jquery-1.4.3.min.js"></script>
<script src="http://code.jquery.com/mobile/1.0a1/jquery.mobile-1.0a1.min.js"></script>
</head>
<body>
<!-- page -->
<div data-role="page">
<!--header -->
<div data-role="header">
<h1>Well Then, Soldier…</h1>
</div>
<!-- /header -->
<!-- content -->
<div data-role="content">
<p>How goes the day?</p>
</div>
<!-- /content -->
<!-- footer -->
<div data-role="footer">
<h4>&copy; 2011 Dodo Men Pty, Inc.</h4>
</div>
<!-- /footer -->
</div>
<!-- /page -->
</body>
</html>
```

仅凭上述几行代码，您就可以在普通的旧式 Web 浏览器中创建出非常原生的移动应用程序外观和感觉。这个页面非常简单。首先，我们有一个主容器，其 `data-attribute` 值为“page”，它是我们内容的包装器。正如预期的那样，接下来是我们的“header”，通常用于放置页面标题以及您决定放在那里的任何导航元素。经过标题之后，我们开始走向页面的主体，也称为“content”`data-attribute`，紧接着是我们的“footer”。

如前所述，这段标记中并没有太多东西发生。大部分“魔法”发生在幕后，在 jQuery Mobile 应用程序的内部运作中。在接下来的几个示例中，我们将探索可以使用 jQuery Mobile 做什么，从简单到复杂，然后进入自定义主题！让我们启动我们值得信赖的 Web 浏览器，看看这个页面在移动设备上的样子（见图 7-1）！

![](img/8b0ff5e51ddb912cd941bb18cf27206a_104_0.png)

**图 7-1。** *由 jQuery Mobile 创建的具有原生外观的用户界面，显示在 Android 2.3.4 手机上*

您看这多容易？最好的部分是，我们仅仅稍微触及了 jQuery Mobile 能力的表面。花点时间，任何人都可以轻松构建一个功能齐全的移动 Web 应用程序，包括花哨的用户界面元素、模态窗口、对话框、页面过渡、导航工具栏，以及大量其他内容！让我们深入挖掘一下。

## 添加多个页面

通常，应用程序由多个页面组成！在图 7-4 中，我们将创建一个更高级的 jQuery Mobile 文档，其中包含三个页面：主页、关于页和联系页。在此过程中，我们将比平时添加更多注释，以便您看到代码的哪一部分创建了哪个元素（显示在图 7-2、7-3 和 7-4 中）。这样，如果您想自定义某些元素，您就能确切知道需要修改哪些内容。

*图 7-4。页面上的所有 UI 元素均由 jQuery Mobile 应用程序创建*

```
<!DOCTYPEHTML>
<html>
<head>
<title>Our Super Rad Demo Page</title>
<link rel="stylesheet" href="http://code.jquery.com/mobile/1.0a1/jquery.mobile-1.0a1.min.css" />
<script src="http://code.jquery.com/jquery-1.4.3.min.js"></script>
<script src="http://code.jquery.com/mobile/1.0a1/jquery.mobile-1.0a1.min.js"></script>
</head>
<body>
<!-- home -->
<div data-role="page" id="home">
<div data-role="header"><h1>Hello World</h1>
```

在头部，我们将指定希望在页面上部黑色条中显示的内容。如果我希望，我可以包含多于一行的文本，而黑色条将继续增加长度。然而，这可能会让用户感到分心。

**表 7–4 续**。*主页面内容*

```
</div>
<div data-role="content">
<ul data-role="list-view" class="ui-listview">
<li data-theme="b" class="ui-btn ui-btn-icon-right ui-li ui-btn-up-c">
<div class="ui-btn-inner ui-li">
<div class="ui-btn-text">Pellentesque habitant morbi tristique senectud    </div>
</div>
</li>
<li data-theme="b" class="ui-btn ui-btn-icon-right ui-li ui-btn-up-c">
<div class="ui-btn-inner ui-li">
<div class="ui-btn-text">Morbi ultrices dignissim erat id blandit    </div>
</div>
</li>
<li data-theme="b" class="ui-btn ui-btn-icon-right ui-li ui-btn-up-c">
<div class="ui-btn-inner ui-li">
<div class="ui-btn-text">Etiam massa quam, tempus quis    </div>
</div>
</li>
<li data-theme="b" class="ui-btn ui-btn-icon-right ui-li ui-btn-up-c">
<div class="ui-btn-inner ui-li">
<div class="ui-btn-text">Nam laoreet congue aliquet    </div>
</div>
</li>
<li data-theme="b" class="ui-btn ui-btn-icon-right ui-li ui-btn-up-c">
<div class="ui-btn-inner ui-li">
<div class="ui-btn-text">Morbi et ligula vel ligula lobortis pharetra ut eu massa
</div>
</div>
</li>
<li data-theme="b" class="ui-btn ui-btn-icon-right ui-li ui-btn-up-c">
<div class="ui-btn-inner ui-li">
<div class="ui-btn-text">Nam commodo erat orci.    </div>
</div>
</li>
</ul>
</div>
```

如果你在家跟随代码实践，你会发现每个项目都出现在一个类似按钮的列表中。你可能会想是否可以让这些列表更有趣。确实可以——jQuery Mobile 支持多种类型的列表（http://jquerymobile.com/demos/1.0.1/docs/lists/index.html）提供了完整的列表和示例）。这里我们使用的是只读列表，因为我们没有将列表项链接到特定页面或操作。然而，还有其他链接选项可用，例如：

- 嵌套列表（参见图 7–2），其中当点击一个列表项时，它会滑走以揭示几个更多的列表项。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_106_0.png)

**图 7–2. 一个嵌套列表**

- 计数气泡列表（参见图 7–3），其中每个列表项的末端可以显示一个数字，嵌入到项目中。这对于显示新项目的数量、通知、新闻故事等的计数非常有用…

![](img/8b0ff5e51ddb912cd941bb18cf27206a_106_1.png)

**图 7–3. 一个计数气泡列表**

- 缩略图（图 7–4）和图标（图 7–5）列表，这些列表在列表文本的左侧显示缩略图图形或图标。这对于显示小照片和描述项目用途的说明性图标很有用，或者仅作为装饰。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_106_2.png)

**图 7–4：一个缩略图列表**

![](img/8b0ff5e51ddb912cd941bb18cf27206a_106_3.png)

**图 7–5. 一个图标列表。**

- 创建内嵌搜索字段（图 7–6）的几种选项，通常是一个位于顶部的列表项，用于过滤后面的列表项。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_107_0.png)

图 7–6. 列表顶部的搜索过滤器框

- 最后，可以创建一个带有表单的列表（图 7–7），允许你在列表视图内创建排序良好的表单元页面。这对结账页面、设置页面和类似情况非常有用。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_107_1.png)

图 7–7. 列表中的表单元素

就你能用列表实现的内容可以说是没有限制的！现在，回到代码……

**表 7–4 续：**主页面的底部。

```
<div data-role="footer" class="ui-bar">
<a href="#about" data-transition="flip" data-role="button" data-theme="b">About</a>
<a href="#contact" data-transition="pop" data-role="button" data-theme="b">Contact</a>
</div>
</div>
<!-- /home -->
```

你会注意到，在主页面的底部，我们创建了一个底部区域（看起来像另一个黑色条），并且添加了两个按钮。在 jQuery Mobile 中创建按钮非常简单——从根本上说，它只是在任何常规 HTML 链接中添加 `data-role="button"`。

后两个属性——transition 和 theme——指的是页面过渡应该如何发生，以及按钮的颜色和样式。我们将在接下来的章节中详细介绍这两点。我们还可以通过指定图标来为按钮添加更多样式。在合理的情况下，jQuery Mobile 会自动向按钮添加图标（例如，通过向对话框关闭按钮添加一个 X 图标）。但是，如果我们愿意，也可以手动完成此操作。例如，将前面的“Contact”链接改为

```
<a href="#contact" data-transition="pop" data-role="button" data-theme="b" data-icon="plus">Contact</a>
```

这将为按钮添加一个漂亮的加号图标。完整的图标列表可以在 jQuery Mobile 网站找到（http://jquerymobile.com/demos/1.0.1/docs/buttons/buttons-icons.html）。默认情况下，图标出现在按钮的左侧；然而，我们可以使用 data-iconpos="right" 或 "top" or "bottom" 来移动它。我们还可以使用 data-iconpos="notext" 来显示图标且不显示其他内容！

如果你想使用自己的图标怎么办？这也是可能的。你需要添加一些自定义 CSS 来完成，并创建一个格式正确的图标文件（这两者都在之前提供的链接中进行了说明）。

最后，可以通过将一系列按钮围绕在 `<div data-role="controlgroup">` 和 `</div>` 标签周围，将按钮格式化为同一组的一部分。这将让你能够视觉上聚集具有类似含义的按钮（例如，“是”、“否”或“取消”组）。这通常意味着只有顶部和底部按钮的角被圆角化（如果使用默认主题），并且按钮之间几乎没有空间。这对于给用户关于相关分组按钮的微妙提示非常有用。现在，第一页已经完成，从头部到底部，我们将在同一个 HTML 文档中定义另外两个页面！

**表 7–4 续：** *关于和联系页面。*

```
<!-- about -->
<div data-role="page" id="about">
<div data-role="header">
<h1>About Us</h1>
</div>
<div data-role="content">
<p>Vivamus sit amet nulla vitae odio ultricies fringilla quis at felis. Integer sagittis eleifend leo, et tempor elit adipiscing in. Pellentesque commodo condimentum pulvinar. Integer vitae tellus ac sapien molestie euismod. Sed a enim ut leo fermentum lobortis ac eget velit. Mauris commodo porta felis id fermentum. Aenean eleifend justo eu sem consectetur auctor. Quisque convallis ullamcorper elementum. Integer hendrerit vehicula nisi eu congue. Integer aliquet quam a arcu cursus ac consequat est pretium. Nam nec pharetra lorem. Maecenas lacinia facilisis eros quis tempor.</p>
</div>
<div data-role="footer" class="ui-bar">
<a href="#home" data-transition="flip" data-role="button" data-theme="b">Home</a>
<a href="#contact" data-transition="pop" data-role="button" data-theme="b">Contact</a>
</div>
</div>
<!-- /about -->

<!-- contact -->
<div data-role="page" id="contact">
<div data-role="header">
<h1>Send Us Mail!</h1>
</div>
<div data-role="content">
<form action="#" method="get">
<div data-role="fieldcontain">
<label for="name">Name:</label>
<input type="text" name="name" id="name" value="" />
<label for="email">Email:</label>
<input type="email" name="email" id="email" value="" />
</div>
<div data-role="fieldcontain">
<label for="message">Message:</label>
<textarea id="message"></textarea>
</div>
<div class="ui-body ui-body-b">
<fieldset class="ui-grid-a">
<div class="ui-block-a">
<button type="submit" data-theme="d">Cancel</button>
</div>
<div class="ui-block-b">
<button type="submit" data-theme="a">Send</button>
</div>
</fieldset>
</div>
</form>
</div>
</div>
<!-- /contact -->

</body>
</html>
```

现在我们讨论了代码的工作原理，让我们看看主页面在图 7–8 中的样子。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_109_0.png)

**图 7–8.** 我们的 jQuery Mobile 主页正在 Android 2.3.4 移动设备上查看

我们会很快跳过“关于”页面，因为这里没有太多操作。不过有一点点美味的东西我们会覆盖。我确信，看着这个页面，你很可能正在问自己，“嘿，他为什么没有创建某种视觉提示，可以用来导航回到我们之前的页面



我们已经在页面上了？！”（即使你之前没想到这个，现在你也想到了）那么，你完全不用担心这个问题！如果你在浏览器中加载我们刚刚创建的这个页面，并查看“关于我们”页面，你会注意到jQuery Mobile很贴心地为你的页面自动包含了一个返回按钮（参见图7–9），甚至包括了我之前提到过的正确图标！

![](img/8b0ff5e51ddb912cd941bb18cf27206a_110_0.png)

**图7–9.** *我们的jQuery Mobile“关于我们”页面在一台Android 2.3.4移动设备上被查看。注意到jQuery Mobile自动包含在用户界面中的返回按钮了吗？*

最后，在我们的“联系我们”页面，我们才真正开始享受jQuery Mobile提供的一些有趣功能（参见图7–10）。查看我们的代码，你会看到这个页面上有两个`data-role`为`"fieldcontain"`的`div`容器。我相信你现在可能已经猜到了，这些容器用于容纳和分隔那些不必要挤在一起的表单输入字段。基本上，对于我们这些缺乏图形设计感的人来说，这是为了美观。在分隔了表单字段之后，我们还有一个`div`容器用来放置“取消”和“提交”按钮。这些按钮通过为`fieldset`元素分配CSS类`ui-grid-a`（这里的“a”代表将用于样式化网格容器的主题）以网格格式定位在页面上。最后，值得注意的是，我们这里的代码目前将电子邮件表单发送到了空地址（`#`）。在本章的后面部分，我们将看到如何使用JavaScript来处理表单，或者也可以编写一个简单的PHP脚本来接收表单数据并处理它。

如你所见，jQuery Mobile允许你在非常短的时间内创建出非常美观的用户界面！

![](img/8b0ff5e51ddb912cd941bb18cf27206a_111_0.png)

图7-10. 我们的jQuery Mobile“联系我们”页面格式整洁，在一台Android 2.3.4移动设备上被查看

### 那么——关于那些过渡效果

如果你一直在跟着编写代码，你会注意到在前面的例子中，按钮的过渡效果会根据我们想要执行的操作而有所不同。动画是移动设计中的一个关键元素，因为它能让小屏幕给用户带来三维感，这有助于他们理解自己正在做什么。默认情况下，jQuery Mobile框架会实现从右向左的滑动过渡，这给用户一种翻页的感觉。该框架也很贴心，当按下“返回”按钮时，它会反转最初使用的过渡效果，在这种情况下，就是翻回到上一页。在清单7-5中，我创建了一个简单的页面来展示所有过渡类型，从页面一移动到页面二。

**清单7–5.** *过渡效果演示HTML*

```
<!DOCTYPE HTML>
<html>
<head>
<title>This is jQuery's Base Template, Showing off The Transitions</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
```

```
<link rel="stylesheet" href="http://code.jquery.com/mobile/1.0/jquery.mobile-1.0.min.css" />
<script type="text/javascript" src="http://code.jquery.com/jquery-1.6.4.min.js"></script>
<script type="text/javascript" src="http://code.jquery.com/mobile/1.0/jquery.mobile-1.0.min.js"></script>
</head>
<body>

<div data-role="page" id="one" data-title="First Page">

<div data-role="header">
<h1>The Title</h1>
</div><!-- /header -->

<div data-role="content">
<p>This is where we put what we want to talk about on this page, it's going to be great</p>
<a href="#two" data-transition="pop">Pop Page 2</A><br>
<a href="#two" data-transition="slide">Slide Page 2</A><br>
<a href="#two" data-transition="slideup">Slideup Page 2</A><br>
<a href="#two" data-transition="slidedown">Slidedown Page 2</A><br>
<a href="#two" data-transition="fade">Fade Page 2</A><br>
<a href="#two" data-transition="flip">Flip Page 2</A><br>
</div><!-- /content -->

</div><!-- /page -->

<div data-role="page" id="two" data-title="Second Page">

<div data-role="header">
<h1>The Title of Page 2</h1>
</div><!-- /header -->

<div data-role="content">
<p>This is where we put what we want to talk about on this page, it's going to be great</p>
<a href="#" data-rel="back">Back to page 1</A>
</div><!-- /content -->

</div><!-- /page -->

</body>
</html>
```

渲染后，页面看起来像图7-11，其中有几个文本链接会根据需要显示相应的过渡效果。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_113_0.png)

图7–11. *过渡效果演示页面*

点击每个链接查看相应的过渡效果，然后使用页面2上的返回按钮查看反向过渡。我们在清单7–4的HTML `HREF`链接中指定了所需的过渡效果，你可以根据需要随意尝试。但是请记住，在处理过渡效果时，可能应该提前决定每个过渡效果的含义，以免让用户感到困惑。如果将某些内容输入数据库会触发淡入过渡，而向上滑动则表示一条消息或错误，那么随意切换这些可能会让用户对自己所采取的操作产生怀疑。另外请注意，Flip和Pop过渡效果可能无法在某些版本的Android原生浏览器中正确渲染，因此可能要避免使用它们。说到向用户显示消息……

### 让我们来个对话框

对话框在计算机领域已经存在很久了。我们已经在本书前面展示了一些非常简单的对话框；然而，jQuery Mobile有一种非常棒的内置方式来显示这些对话框，我们将使用下面的清单7–6来展示它。

**清单7–6.** *对话框示例*

```
<!DOCTYPE HTML>
<html>
<head>
<title>This is jQuery's Base Template, Showing off The Dialogs</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="http://code.jquery.com/mobile/1.0/jquery.mobile-1.0.min.css" />
<script type="text/javascript" src="http://code.jquery.com/jquery-1.6.4.min.js"></script>
<script type="text/javascript" src="http://code.jquery.com/mobile/1.0/jquery.mobile-1.0.min.js"></script>
```

```
</head>
<body>

<div data-role="page" id="one" data-title="First Page">

<div data-role="header">
<h1>The Title</h1>
</div><!-- /header -->

<div data-role="content">
<p>This is where we put what we want to talk about on this page, it's going to be great</p>
<a href="#two" data-rel="dialog" data-role="button">Open Dialog</A><br>
<a href="#two" data-rel="dialog" data-role="button" data-transition="slidedown">Slide Down Dialog</A><br>
<a href="#two" data-rel="dialog" data-role="button" data-transition="flip">Flip Dialog</A><br>
<a href="#two" data-rel="dialog" data-role="button" data-transition="Pop">Pop Dialog</A><br>
</div><!-- /content -->

</div><!-- /page -->

<div data-role="page" id="two" data-title="Second Page">

<div data-role="header">
<h1>The Title of Page 2</h1>
</div><!-- /header -->

<div data-role="content">
<p>This is a dialog box</p>
<a href="#" data-rel="back">Back to page 1</A>
</div><!-- /content -->

</div><!-- /page -->

</body>
</html>
```

当我们加载清单7–6时，会得到一个包含一系列3个按钮（图7–12）的页面，我们可以点击这些按钮来查看页面二（与我们过渡效果演示中相同的页面）弹出（或滑动，或翻转）。在对话框中，一旦打开，右上角还会出现一个小的黑色X按钮来关闭消息，无需任何额外的编码。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_115_0.png)

图7–12. *对话框演示页面，dialogs.html*

当你需要引起用户注意，并且不想给他们一种正在跳转到新页面的感觉时，对话框非常有用。正确使用它们，会给你的用户带来出色、流畅的体验。

既然你已经通过过渡效果和对话框添加了一些个性化设置，让我们回顾一下我之前提到过的一个话题：自定义主题。

### 使用ThemeRoller打造你自己的主题

让我们面对现实：创建一个主题并非易事。有很多因素需要考虑，尽管苹果公司做了很多工作，为移动页面建立了一种相对标准的外观，但你可能不希望我们的Android应用程序看起来完全像iPhone的复制品，对吧？（实际上，也许你想，但是嘿——有选择总是好的！）值得庆幸的是，jQuery Mobile团队创建了一个他们自己的很棒的Web应用程序，叫做ThemeRoller（图7–13），它让你能够快速、轻松地创建一个主题。



## 第7章：使用 jQuery Mobile 打造令人印象深刻的用户体验

图 7–13. ThemeRoller 的主启动屏幕

ThemeRoller 让你能够微调 jQuery Mobile 主题中的每一个元素。在屏幕右侧，你会看到三个主题（A、B 和 C）——每个主题都可以自定义，如果需要，你甚至可以添加更多主题。创建完成后，我们可以通过使用 `data-theme` 属性来指定在给定页面上使用哪个主题（例如可以在前面的清单中看到，如清单 7–4）。

一旦你关闭“Get Rolling”屏幕，就可以开始展开屏幕左侧的选项，如图 7–14 所示。

**图 7–14.** *自定义 ThemeRoller 屏幕左侧的选项*

我可以进行全局更改，影响所有主题，或者我也可以专门更改主题 A、B 或 C 中的内容。在这种情况下，所有默认设置都提供了一种非常类似 iPhone 的外观。我打算将它们改造成如图 7–15 所示的配置。

你可以看到我已经更改了很多设置，这使得界面大不相同。我还没有更改颜色，虽然我可以非常轻松地做到这一点。实际上，ThemeRoller 甚至会提供一组 Adobe kuler 色板（图 7-16；一组颜色搭配和谐的色板 - (www.adobe.com/products/kuler/)）来帮助我挑选一组能让用户感到愉悦的颜色。

自定义几分钟（或几小时）后，我可以通过输入一些选项来下载我的主题，如图 7-17 所示。这会提供给我一个 ZIP 文件，其中包含一个主题目录、一个正确嵌入我的主题的示例 index.html、所需的图片，以及两个用于我的主题的 CSS 文件，如果我愿意，之后可以手动编辑它们。

图 7–17. 带有说明的下载主题窗口

如果我需要对主题进行更改，我可以使用 ThemeRoller 中的“Import”选项将其重新导入 Web 应用并再次进行调整。然后我可以像第一次一样导出我的新主题。想象一下：你可以创建自定义主题（比如我之前创建的主题，如图 7–18 中的示例索引文件所示），然后为“姊妹”应用程序修改它们——而无需直接接触 CSS！

图 7–18. 应用到 ThemeRoller 提供的示例索引文件上的我的自定义主题

现在我的应用程序已经呈现出我想要的样子，而且我知道如何构建额外的页面、过渡和对话框。我正走在创建不仅功能强大而且外观出色的杀手级应用程序的路上！

## 将所有内容整合在一起：Simple Calc

既然我们已经用 jQuery Mobile 构建了一些示例页面，让我们来构建一些实用的东西：一个简单的计算器。我们将构建一个非常简单的计算器，它接受两个数字并对它们执行某种操作，返回结果。我还将创建一个自定义主题供使用。最终结果如图 7-19 所示：

图 7-19. Simple Calc jQuery Mobile 应用程序

Simple Calc 是一个极其简单的计算器。你将一个数字放入第一个框，将另一个数字放入下方的按钮框，然后点击 + 或 -。一个小型的 JavaScript 警告框会弹出，告诉你答案是什么。它确实很简单，但对于展示如何使用 JavaScript 向 jQuery Mobile 页面添加一些交互性非常有用。让我们看看清单 7-7 中的代码。

清单 7-7. Simple Calc 的代码

```html
<!DOCTYPE HTML>
<html>
<head>
<title>Simple Calc</title>
<link rel="stylesheet" href="http://code.jquery.com/mobile/1.0a1/jquery.mobile-1.0a1.min.css" />
<script src="http://code.jquery.com/jquery-1.4.3.min.js"></script>
<link rel="stylesheet" href="themes/simplecalc.css" />
<script src="http://code.jquery.com/mobile/1.0a1/jquery.mobile-1.0a1.min.js"></script>
<script type="text/javascript">
function addnums() {
var num1 = document.calc.number1.value;
var num2 = document.calc.number2.value;
var num3 = num1 + num2;
alert(num3);
}

function subnums() {
var num1 = document.calc.number1.value;
var num2 = document.calc.number2.value;
var num3 = num1 - num2;
alert(num3);
}
</script>
</head>
<body>
<!-- page -->
<div data-role="page" id="aboutPage">

<!--header -->
<div data-role="header">
<h1>Simple Calc</h1>
</div>
<!-- /header -->

<!-- content -->
<div data-role="content">
<form action="#" name="calc" method="post">
<p>Enter a number in the first box, one in the second, and then press a button in between to get the answer!</p>
<p><input type="number" name="number1" id="number1" placeholder="Number 1">
<p><div data-role="controlgroup"><a href="#" data-role="button" onclick="addnums()">+</a><a href="#" data-role="button" onclick="subnums()">-</a></div>
<p><input type="number" name="number2" id="number2" placeholder="Number 2">
</form>
</div>
<!-- /content -->

<!-- footer -->
<div data-role="footer">
<h4>Neat!</h4>
</div>
<!-- /footer -->
</div>
<!-- /page -->

</body>
</html>
```

让我们逐步解析这段代码。首先，我们开始添加通常的 HTML 标头以及指向 jQuery Mobile 的链接。你会注意到我的自定义主题也包含在第 7 行（simplecalc.css）。我使用我们在上一节讨论过的 ThemeRoller 构建了这个主题！

接下来是一组自定义的 JavaScript 函数：`addnums()` 和 `subnums()`。这些函数访问两个数字框（分别声明为 `num1` 和 `num2`）并执行所需的操作。然后它们会弹出一个标准的 JavaScript 警告框显示结果。如果你想展示你的 JavaScript 能力，可以将这两个函数合并为一个！

再往下一点，我们看到实际的内容布局。我们放入了两个输入框，`number1` 和 `number2`，在它们之间是我们的两个按钮。我们使用了一个 `controlgroup`，这样按钮就组合在一起，而不是分开显示。你会注意到每个按钮都有一个 `onclick=` 引用，指向其对应的 JavaScript 函数。这就是魔法发生的地方——也是为什么我们实际上不需要构建一个表单提交页面——JavaScript 处理了所有的计算。

就是这样——一个简单的计算器！

## 总结

使用 jQuery Mobile，你可以快速将一个简陋的应用程序变得看起来像是专业设计的。你也可以快速制作漂亮“信息展示”应用程序（即作为会议程序或建筑/活动导游的应用程序）。我们已经介绍了 jQuery Mobile 的基础知识，但仍然有一些高级主题和细微之处留待你自己去探索——你的想象力是唯一的限制！

## 第8章：构建视觉丰富的互联网应用程序

现在我们对 JavaScript 和各种面向移动设备的 JavaScript 框架如何增强用户体验有了更好的理解，是时候深入其中，用一些数字涂鸦来大展身手了。构建出色的 Web 应用程序不仅仅关乎编程和逻辑。相当多的网页开发工作都大量借鉴了设计领域。以 CSS 为例。它让开发者抓狂的主要原因之一是 CSS 本质上是一种设计工具，而不是真正的开发工具。当然，我们必须编写代码来让一切看起来漂亮，但实际上我们做的是精心设置边距、内边距、颜色、字体等等。

记住这一点，在本章中，我们将探索那些与设计更相关的有趣开发方面。我们将了解 Creative Commons 图标和图形的资源、Web 字体资源、CSS 框架，甚至还有一个面向网页开发者和网页设计师的优秀位图和矢量图形编辑器，名为 Adobe Fireworks (www.adobe.com/products/fireworks.html)。

## 寻找和使用图标与库存照片

让网站看起来更有吸引力的最简单方法之一是为你的项目添加一些图标或吸引人的库存照片。有很多资源，艺术家们很乐意提供他们创建的图标集或他们拍摄的看起来很壮观的照片，可以免费使用，无需询问。

在本节中，我们将看看一些更受欢迎的网站，这些网站迎合设计师、开发者以及所有其他喜欢有吸引力和有趣视觉效果的人。

### Iconfinder

Iconfinder (www.iconfinder.com/, 见图 8-1) 是我个人最喜欢的一个，它位于 Creative Commons 空间，提供开源图标。这个搜索引擎允许你

筛选超过150,000种不同的图标，它们正等待被用于你的下一个项目中。

从12像素到惊人的512像素的图标和图形，这个搜索引擎几乎保证能让你找到可用于提升任何项目视觉效果的素材。

虽然这个搜索引擎中的图标可以免费使用，但并非所有商业网站（即为营利团体而非非营利组织建立的网站）上的图标都可以免费使用，因此请务必阅读你想要使用的任何图标的许可协议。我们已经多次提到知识共享许可协议（Creative Commons），因此有必要花点时间了解它以及其他许可协议。首先也是最重要的是，你必须记住，任何原创艺术品（无论是图标、照片等……）的设计者都保留该艺术品的版权。人们很容易想"嘿，它在网上呢，一定是免费的。"然而，如果所有者发现，这种思维方式可能会很快让你陷入麻烦。许多不愿意为其内容创建独特许可协议的艺术家和设计师选择使用知识共享许可协议（http://creativecommons.org）。这些许可协议允许艺术家允许他人自由使用其作品，可能带有或不带某些限制。你不能仅仅假设知识共享许可的内容可以免费使用——它可能限制商业用途（NC是知识共享团队使用的简写），或者可能需要在应用中标明归属（将图标或图片归功于所有者，此处使用的简写是BY）。此外，所有者可能会指定其他需要注意的选项。

总而言之，如果你不确定是否可以使用某个图标，不要害怕联系作者询问。最坏的情况也不过是他们拒绝你！

![](img/8b0ff5e51ddb912cd941bb18cf27206a_124_0.png)

**图8–1.** *Iconfinder搜索引擎主页。超过158,184个图标，而且还在增长！*

## 查找图标

查找图标（图8-2）是另一个面向需要为网站增添亮点的开发者和设计师的搜索引擎。其功能和布局与Iconfinder相似，因此如果你熟悉其中一个搜索引擎，可以轻松适应使用另一个。

我发现搜索图标时同时使用两个网站总是有好处的，因为每个网站都有另一个网站上没有的图标集合。你可以在 http://findicons.com/ 浏览查找图标搜索引擎。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_125_0.png)

## 使用图标

假设你已经找到了喜欢的图标，或者使用favicon.ico生成器（www.favicon.cc/）等服务创建了一个，你可以通过将以下HTML代码放入HTML头部来轻松为你的Web应用指定此图标：

```
<link rel="shortcut icon" href="http://yourdomain.com/app.ico" />
```

**deviantART**

deviantART（www.deviantart.com/，见图8-5）似乎一直存在，从技术角度来说确实如此。这个2000年的古老遗迹经受住了互联网的考验，是业余和专业艺术家及平面设计师创造力的光辉支柱。

再加上一些社交媒体功能，允许用户评论或与其他用户分享艺术作品，你就拥有了一种令人上瘾的用户体验，提供了大量优质资源……有时也有一些不那么优质的资源。

一定要去他们的摄影区看看，那里有大量的免费库存照片，可以在你即将开展的项目中进行处理和利用。还要确保查看所提供的库存照片的许可协议。一些艺术家可能有特殊要求，在你利用他们的作品之前必须满足。这些要求可能相当普通（即禁止商业用途），也可能非常具体（即必须用于公益广告或慈善用途）。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_127_0.png)

**图8–5.** 查看deviantART的库存照片区

## iStockphoto

获取Web应用优质库存照片的另一个更专业——也更昂贵的解决方案是iStockphoto（www.istockphoto.com/）。这是我多年来用于为客户项目购买免版税图片的服务。

与deviantART不同，此资源不是免费使用的，但你将购买的图片来自专业人士，质量往往比其他地方找到的业余作品更好。

再加上可以轻松搜索找到所需内容的大量图片档案，你就拥有了一个应该随时备用的资源！你永远不知道什么时候，某一天，某个客户可能会打电话给你说"嘿，我决定我们真的想在网站上添加一个巨大的粉色电话"，即使这听起来疯狂而荒谬，但很可能你能在iStockphoto上找到一张巨大粉色电话的图片。

除了iStockphoto和deviantART，还可以在Shutterstock（www.shutterstock.com）和Flickr（www.flickr.com）找到图片。Flickr特别有一个非常实用的 advanced search function (www.flickr.com/search/advanced/)功能（www.flickr.com/search/advanced/），允许你指定只想要知识共享许可的内容（更进一步，只想要可免费商业使用且可改编的CC许可内容）。这是为你的应用获取非常优质的用户提交照片的简便方法。

在结束讨论照片之前，讨论一下何时应该以及何时不应该选择使用照片可能很有用。在许多不同的地方使用图片来推广你的应用和/或让它出彩可能很诱人；然而，必须把握好分寸。

## Web应用中使用照片的指导

在找到我们在前面章节中讨论的服务后，你可能会很想为应用的每个部分都找一张照片。例如，你的应用主屏幕上可能有大型导航按钮，那些大方块如果放照片而不是文字或简单图标，看起来不是更棒吗？也许吧……但我们建议你先考虑以下几点：

- **每张照片会增加多少加载时间？** 请记住，我们在测试时，应用通常运行在自己的电脑上。这使得加载时间的争论很大程度上变得无关紧要——我们根本无法知道我们的应用在某些情况下会如何加载。考虑到这一点，漂亮的照片有时会导致应用加载缓慢。我们建议使用适当大小的照片（例如，必要时进行 resize；不要仅仅指定高度和宽度使其渲染变小，而实际文件大小并未变小——如果可能，小于10KB），并在各种条件下测试照片版和非照片版的页面（例如，从生产Web服务器提供，到WiFi和蜂窝数据连接上的设备）。

- **我的图片会分散用户注意力吗？** 是的，虽然一图胜千言，但有些图片在用户中引发的争议可能价值更高。在某些情况下，STOP标志的照片可能易于用户理解，但在其他情况下可能造成困惑（例如，在游戏中——STOP标志意味着回合结束？退出游戏？阻止我的小人物行走？）。图片应该只帮助用户更快地找到东西，而不是通过分散注意力、造成困惑或质量低劣来迷惑用户。

- **使用图片会唤起用户刻板印象吗？** 图片可以很有力量，但在某些情况下，它们可能与我们熟知的传统刻板印象相关，也可能与你可能想不到的一些刻板印象相关。例如，使用久经考验的"穿西装的男士"和"使用笔记本电脑的女士"可能对你的应用来说似乎合适；然而，用户通常之前已经看过这些库存图片，可能会假设你的Web应用和用过相同图片的其他应用一样ironically一样缺乏灵感。这就是为什么许多网站现在倾向于极简设计趋势——它比"辛勤工作的企业高管"或"足球妈妈"更不可预测。

假设你已经仔细考虑了前面列表中讨论的问题，使用照片可以是增强应用吸引力的绝佳方式。只是要注意你的使用方式！现在我们将看看一种更微妙的图片处理方式：在Web应用中使用自定义字体。



## 网络字体

你可能还记得，在第2章构建"那是谁的推文？"应用时，我们曾简要接触过网络字体的使用。在过去的一年半里，所有主流的桌面浏览器都已推出更新，现在可以在标记中使用网络字体了。几乎所有安卓移动浏览器也都能使用它们。

将网络字体添加到你的网站或应用中易如反掌，如清单8–1所示。

清单 8–1. *用一点CSS魔法将Droid Sans字体加载到我们的网页浏览器中。*

```
<style type="text/css">
@font-face {
    font-family: 'Droid Sans';
    font-style: normal;
    font-weight: normal;
    src: local('Droid Sans'), local('DroidSans'), url('droidsans.woff') format('woff');
}

body {
    font-family:'Droid Sans', Arial, Helvetica, sans-serif;
}
</style>
```

让我们快速看一下清单8–1中的代码，以便理解我们在这里做什么。我们在@font-face代码中要定义的第一个属性是font-family属性。在这里，我们可以随意命名字体。我们在这里使用的是字体的真实名称Droid Sans，但如果我真的想，也可以叫它"Turtle Wax"。使用自定义名称可能有助于你使用内部命名结构，不过如果你想在两个不同的产品中使用同一种字体，这可能会造成混淆。

接下来，我们要定义新字体的font-style。这很重要，因为我们可以根据font-style的不同加载Droid Sans字体的不同变体。作为开发者，在这个领域你需要小心，确保不要过度加载10种不同的字体变体，而实际上并不需要。这不仅会让你的代码变得杂乱，还会不必要地加载资源，拖累用户体验。在本例中，我们只是想让这种字体使用默认或'normal'样式；也就是说，我们不需要斜体。

在font-style之后，我们有font-weight。它和前面的属性一样，可以用来加载字体的不同版本，比如Droid Sans粗体。

最后但并非最不重要，我们有src，它用于告诉你的计算机在服务器上哪里可以找到我们的字体，以及用户的计算机上字体可能叫什么名称。如果字体在用户机器上，这可能会省去下载我们已经拥有的文件，从而节省一些带宽。虽然本地加载在多数情况下更可取，但你可能会遇到想从其他位置加载字体的情况，比如当你测试多种字体样式以确定最佳搭配时。

### Google网络字体

你可能还记得之前我们在某章中从Google网络字体获取了Droid Sans字体。当时，我们没有详细介绍Google网络字体，也没有说明它对于设计师和开发者来说是多么不可思议的资源。

在你的下一个项目中使用Google网络字体（如图8–6所示）最吸引人的一点是，所有字体都是开源的，任何人都可以使用，无需担心违反许可或欠别人钱。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_130_0.png)

图 8–6. 重新设计的Google网络字体网站着陆页

我听到反对使用网络字体的开发者最大的抱怨之一是，字体往往有点笨重，这确实会增加加载时间。虽然在移动设备上由于带宽有限这可能会令人烦恼，但Google已经考虑到了这一点，并创建了一种简单的方法来缩减加载到用户浏览器中的字体文件大小。

快速看一下清单8–2。这里我们有将Chivo Google网络字体添加到我们的网页应用所需的基本HTML标记。

清单 8–2. 将非优化版本的Chivo字体加载到用户的浏览器中。

```
<link href='http://fonts.googleapis.com/css?family=Chivo' rel='stylesheet' type='text/css'>
```

现在，如果你看一下清单8-3，就可以看到我们是如何通过只加载组成"Hello World"这个词所需的字母来优化字体大小的。如果你需要将一个只使用一次的字体加载到你的网站中，比如用于logo，而且只使用几个字母，这就很完美了。

> **清单 8-3.** 加载优化版本的Chivo字体，只从字体中加载我们需要的字母

<link href='http://fonts.googleapis.com/css?family=Chivo&text=Hello%20World' rel='stylesheet' type='text/css'>

除了允许你优化字体外，Google还会定期向Google网络字体目录中添加新字体。这绝对是我无聊时最喜欢浏览的地方之一，因为你永远不知道什么时候会找到那个神奇的字体，激发你坐下来开始编写新的东西。

### 需要考虑的字号问题

就像使用照片一样，使用不同的字体和文字样式也有一些注意事项需要考虑和计划：

#### 不同样式意味着什么？

我们之前提到，可以为字体指定样式变化，比如将文字设为斜体或粗体，甚至使用字体的不同变体，比如使用块字母样式。虽然这些变体提供了很大的灵活性，但如果应用不一致，也可能会让用户感到困惑。你应该考虑是否希望块文字来表示动作（例如，视频或音频片段的**播放**按钮），或者你更愿意用斜体来表示（尽管如果文字不够大，斜体在移动屏幕上可能难以阅读）。然而，如果动作是斜体，照片下方的说明文字应该如何显示呢？粗体可能在那里显得过于强烈，或者可能暗示文字是链接。看到这会如何变得有点复杂了吗？为你的应用创建一个非正式的"样式指南"可以极大地帮助你产出一致且美观的效果，并有效地使用字体。

#### 样式值得牺牲流畅性吗？

认知心理学研究人员——或者说研究大脑如何解释信息的心理学学者——使用"流畅性"一词来指代信息处理的难易程度。一个粗细适中、线条分明、且没有衬线的字体流畅性很高，意味着读者可以轻松快速地解析并理解你要表达的内容。另一方面，波浪形的"优雅"手写体或非常方正的块字体（字母开始相互重叠）流畅性很低。这意味着用户需要更长的时间来阅读这些部分。在某些情况下，这是件好事——我们可能想吸引用户注意应用中的某个部分，确保他们花足够的时间来考虑它（例如，所有数据即将被擦除的通知可能适合用块字母样式，前提是它不至于太不流畅而导致用户因沮丧而跳过它！）。然而，在其他情况下，我们可能更想注重速度而非风格。

- **颜色可能比字体更有表现力。** 虽然使用不同的字体来在应用内部创造不同的外观很诱人，但应该考虑一下，仅仅改变文字颜色是否就足够了。使用搭配和谐的颜色方案（也许可以参考Color Combos (www.colorcombos.com/)这样的网站）在创造丰富外观方面能做的，比改变字体更多。前面讨论的相同规则也适用于颜色（即，颜色应该始终向读者传达相同的信息——这是警告、动作还是描述？）；然而，与使用字体相比，颜色在加载和配置方面的成本更低。

现在我们已经讨论了如何使用字体、图片和图标来创造你想要的外观，我们将进入更广泛的背景——CSS框架，在这里我们可以获得一整套CSS"皮肤"来包裹我们的应用，产生深远的影响和效果！

## CSS框架

无论你是爱是恨，在过去几年里，CSS网格框架在新手网页设计师和开发者中越来越受欢迎。我把这一切都归咎于Blueprint，一个在2008年左右非常流行的CSS框架。Blueprint的创建是为了减少开发时间，并防止开发者在忘记margin和padding的区别时，因沮丧而扯掉大把头发¹。最后一点可能是我在开玩笑，但事实也不远矣。

正如我们在本章开头所讨论的，像层叠样式表这样的工具被开发者广泛使用，但原本是作为供设计师使用的工具。开发者可能对CSS不太适应——有点像让木匠来给家里布线。他可能懂得够做，但话说回来，他可能会把事情搞得比完全不开始还要糟糕。

虽然这听起来有点荒谬，但我已经多次接手客户项目中那些由开发者或工程师写好的样式代码，很明显他们是把写CSS的方法当作写代码逻辑一样来处理了。把CSS看作是设计标准，而不是用代码规定的规则。

如果你听起来就是那种似乎总是搞不"懂"CSS的人，那么你可能想看看外面的一些框架，它们是为了让你的生活更轻松而创建的。从长远来看，它们会通过快速帮你解决许多开发者在尝试样式设计时遇到的常见问题，从而为你节省时间和金钱。

> ¹ 对Rocco来说，这不是什么问题。对Jon来说，他需要他能留住的每一根头发！




## 第八章：构建视觉丰富的互联网应用

内容填充到网格中。它们也是绝佳的学习工具，可以拆解开来，如饥似渴地学习它们的工作原理。

谁知道呢，在玩转了一段时间的 CSS 框架并了解它们的工作方式后，你可能会对样式表语言产生真正的热情，并最终发现自己手工编写 CSS 的速度比实现一个现成的解决方案还要快！

在下文中，我们重点介绍了三个框架，从最简单的开始，它为你解决了许多桌面端/移动端的 CSS 难题——即 *1140px 网格*。其次是 *Less 框架 4*，它提供了一些支持，但有更大的修改空间。最后，我们讨论 *320 and Up*，它是 Less 框架 4 的一个版本，允许你无需大量调整即可快速上手运行！

### 1140px 网格

1140px 网格是目前互联网上流行的另一个 CSS 框架，拥有相当多的追随者。该框架本身基于知识共享许可协议发布，可以自由使用、复制、分发和随心所欲地修改。

创建这个框架是为了适应屏幕分辨率的近期变化，特别是当前流行的 1280 x 800 电脑屏幕，同时也为较小的显示器提供了流畅的缩放能力。直到不久前，大多数网站都是围绕着普通用户的浏览器宽度约为 1024 像素、高度为 800 像素的想法来设计的。然而，在过去几年中，许多开发者注意到平均用户屏幕分辨率一直在缓慢地提高。

考虑到这一点，1140px 网格旨在利用现在更常见的屏幕分辨率，并按照本书第 5 章讨论的响应式网络设计原则，从该分辨率开始进行流畅的向下缩放。对你作为开发者来说，这意味着如果你正在为桌面用户体验设计和构建一个 Web 应用，你只需为更大的显示器设计一次应用。然后，框架会智能地为你将应用缩放，以适应任何分辨率更低的浏览器。

然而，这并不总是一个一劳永逸的过程，有时确实需要你深入其中，对 CSS 进行一些调整，才能让它看起来完全如你所愿。例如，网格允许你使用多列；但是，如果你希望你的应用在桌面端和小浏览器（类似于我们之前在书中讨论专用移动版本与单一页面服务两者时提到的）上都具有吸引力，你可能希望将自己限制在一个网格内。不过，总而言之，如果你必须先构建大屏版本再构建小屏版本，你可以通过查看 1140px 网格框架来让自己的生活轻松一点，网址是 http://cssgrid.net/

### Less 框架 4

Less 框架（http://lessframework.com/，图 8–7）是另一个流行的 CSS 网格系统。它包含三种不同的排版预设和四种不同的布局类型，比一些其他竞争产品更健壮一些。与 1140px 网格框架不同，这个框架在构建时考虑了平板电脑和智能手机。如果你构建的应用或页面只需要在手机或平板电脑上显示，Less 框架 4 比 1140px 网格是更好的选择。虽然这个框架是为 iPad 和 iPhone 用户开发的，但它在基于 Android Webkit 的浏览器上也表现得非常好。

然而，Less 框架并不像其他一些选项那样是一个为你包办一切的框架。为了最好地利用这个框架，建议你与 HTML 和 CSS 都保持良好的关系。你们三个不必是密友，也不必邀请彼此共进圣诞晚餐，但偶尔在饮水机旁聊聊天，问问孩子们近况，也没什么坏处。

举个例子来说明我们的意思：考虑 Less 框架 4 有两种移动布局：普通布局和宽布局。宽布局是为横屏模式的手机设计的。考虑到你的用户可能会因为各种原因在不同时间切换手机方向，你可能需要在 JavaScript 或 HTML 中采取措施，根据方向重新渲染或重新组织内容。一个在宽布局下看起来不错的应用在普通布局下可能看起来很糟糕——这是你应该确定、测试和调试的。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_135_0.png)

*图 8–7. 在 Google Chrome 桌面浏览器中看到的 Less 框架 4 主页*

### 320 and Up

另一个基于知识共享许可协议的框架，320 and Up（http://stuffandnonsense.co.uk/projects/320andup/）从一开始就考虑到较小的视图端口而创建。正如 320 and Up 网站所说，这个框架是“小屏幕优先”。它由 Andy Clarke 和 Keith Clark 创建，基于 Less 框架 4，这组 CSS 样式包含了预设的排版样式和一些额外的 JavaScript 工具，用于调整图像大小和提高旧版浏览器中站点的整体性能。正如你在图 8–8、8–9 和 8–10 中看到的那样，它能够很好地适应当前 Android 设备上使用的不同常见方向和屏幕。

320 and Up 是一个很好的选择，当你希望避免桌面端和移动端版本应用之间的任何重叠，并且响应性是你的主要目标时。320 and Up 还包含比 Less 框架 4 更多的自定义选项，例如用于调整照片大小和应用适当优化 CSS 的内置 JavaScript 库。如果 Less 框架 4 的自定义让你觉得难以驾驭，你可能想从 320 and Up 开始，看看是否真的需要深入挖掘！

![](img/8b0ff5e51ddb912cd941bb18cf27206a_136_0.png)

图 8–8. 在 Android 2.3.4 姜饼系统手机竖屏模式下查看的 320 and Up 网站

![](img/8b0ff5e51ddb912cd941bb18cf27206a_136_1.png)

图 8–9. 在 Android 2.3.4 姜饼系统手机横屏模式下查看的 320 and Up 网站

![](img/8b0ff5e51ddb912cd941bb18cf27206a_137_0.png)

图 8–10. 在桌面浏览器的 Google Chrome 中查看的 320 and Up 网站。请注意，这幅图和前面的图都显示了相同的标记代码，但页面的外观因用户的浏览器分辨率而异。

### 框架比较：关于乔恩！

选择合适的框架可能很困难，所以在本例中，我们将使用相同的内容，并在所有三个框架中进行渲染。素材来自我个人网站上关于我（乔恩）的简历简介。假设这是我移动应用程序中的一个页面。首先，让我们看看在桌面 Web 浏览器中渲染的原始页面（见图 8–11）——这是我们试图在移动版本中在某种程度上模仿的效果。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_137_1.png)

图 8–11. 在桌面上渲染的乔恩的简历简介。

首先，我们将在 1140px 网格中渲染这个页面。回想一下，这个框架的优点是我们可以得到从桌面到移动设备相似的效果。首先是移动端视图（图 8–12）：

![](img/8b0ff5e51ddb912cd941bb18cf27206a_138_0.png)

图 8–12. 使用 1140px 网格在移动设备上渲染的乔恩的简历简介

现在，让我们看看桌面浏览器中的视图（图 8–13）：

![](img/8b0ff5e51ddb912cd941bb18cf27206a_138_1.png)

图 8–13. 使用 1140px 网格在桌面端渲染的乔恩的简历简介

这并不完全理想——两个单列布局在移动端是堆叠显示的。然而，在桌面端视图中，它们是并排显示的，并且“挤压”得非常厉害。通过调整 HTML 代码，我们可以缓解这个问题，并使桌面端版本看起来更美观（见图 8–14），同时保持移动版本。在这个例子中，问题仅仅在于我们使用了两个“onecol”框，而不是左侧一个 onecol，右侧一个 elevencol（填充屏幕的其余部分）。1140px 网格要求

-   你清楚需要从起始位置开始填充多少列，并使用相应的 `div` 语句。共有 12 列，因此无论你使用哪种组合，总和应为 12（即在本例中，1 列 `onecol` 和 1 列 `elevencol`）。此外，你会注意到最后一列在其 `div` 语句中包含单词 `'last'`（参见清单 8-2），这让 1140px Grid 知道它是该行中的最后一列，因此应填充页面的剩余部分。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_139_0.png)

现在，让我们来看看 Less Framework 4 中的情况。首先，你会注意到 Less Framework 擅自应用了一些基本的字体格式，而 1140px 则允许我们手动操作，或者如果愿意的话根本不做任何设置。如果你想要那种“移动”端的感觉，这可能会帮助你更快地运行起来，如图 8–15 所示。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_140_0.png)

**图 8–15.** *Jon 使用 Less Framework 4 框架编写的个人简介*

代码的实现要简单得多，主要是因为我们要考虑桌面版本。清单 8–3 给出了全部代码，引用了 Less Framework 4 包中提供的 CSS。

**清单 8–3.** *Jon 使用 Less Framework 4 框架编写的个人简介*

```html
<!DOCTYPE HTML>
<html>
	<head>
		<meta charset="utf-8"/>
```

```html
<title></title>
<link rel="stylesheet" href="main-16px.css"/>
<meta name="viewport" content="width=device-width, initial-scale=1"/>
<p><img src=http://jonwestfall.com/wp-content/uploads/2010/03/jon-website.jpg height=220px width=240px></p>
<p>Jonathan E. Westfall, PhD, born 1982, is a researcher and technologist working in New York City at Columbia Business School. His current research focuses on the variables individuals use when making economic and consumer finance decisions, specifically strength of handedness, a variable correlated with a number of decision-making and cognitive psychology tasks and measures. Dr. Westfall also conducts research on consumer financial decision making, and applications to both marketing and public policy. His current appointment is as the Associate Director for Research and Technology at the Center for Decision Sciences, a center within Columbia Business School at Columbia University in New York City. Additionally, he holds an appointment as a Lecturer in the Columbia University Psychology department, periodically teaching a course in Judgment and Decision Making</p>
</head>
<body>
</body>
</html>
```

最后，让我们看看使用 320 and Up 编写的我的个人简介。它应用了进一步的格式设置，包括背景图像和自定义字体，如图 8–16 所示。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_141_0.png)

与 1140px Grid 相比，代码再次变得更加简洁，因为我们不关心桌面渲染。见清单 8–4。

## **清单 8–4.** *Jon 使用 320 and Up 框架编写的个人简介*

```html
<!DOCTYPE HTML>
<head>
<meta charset="utf-8">

<title>320 and Up Version</title>
<!-- http://t.co/dKP3o1e -->
<meta name="HandheldFriendly" content="True">
<meta name="MobileOptimized" content="320">
<meta name="viewport" content="width=device-width, target-densitydpi=160dpi, initial-scale=1.0">

<!-- For all browsers -->
<link rel="stylesheet" href="css/style.css">

</head>

<body class="clearfix">
<div role="main">
    <p><img src=http://jonwestfall.com/wp-content/uploads/2010/03/jon-website.jpg height=220px width=240px></p>
        <p>Jonathan E. Westfall, PhD, born 1982, is a researcher and technologist working in New York City at Columbia Business School. His current research focuses on the variables individuals use when making economic and consumer finance decisions, specifically strength of handedness, a variable correlated with a number of decision-making and cognitive psychology tasks and measures. Dr. Westfall also conducts research on consumer financial decision making, and applications to both marketing and public policy. His current appointment is as the Associate Director for Research and Technology at the Center for Decision Sciences, a center within Columbia Business School at Columbia University in New York City. Additionally, he holds an appointment as a Lecturer in the Columbia University Psychology department, periodically teaching a course in Judgment and Decision Making</p>

<!-- Scripts -->
<script src="js/libs/jquery-1.6.2.min.js"></script>
<script src="js/plugins.js"></script>
<script src="js/script.js"></script>
<script src="js/mylibs/helper.js"></script>
</div>
</body>
</html>
```

正如你所看到的，每个框架的格式略有不同，允许你选择想要使用的一个。虽然 Less Framework 4 和 320 and Up 在外观上看起来非常“移动”，但它们缺乏与桌面版本的跨功能兼容性。另一方面，1140px Grid 在其风格上并不太“移动”，这意味着你需要手动添加这些内容。然而，作为优点，你可以在一个文件中获得桌面和移动版本。

为你自己选择合适的 CSS 框架可能很困难；不过，鉴于我们在这里讨论的框架，它应该能为你选择合适的框架提供一个起点！

## Adobe Fireworks

如图 8–17 所示，Adobe Fireworks 可能是我 Web 开发工具带中第二常用的工具，这是有充分理由的。这个非常容易使用的矢量和位图编辑程序非常适合修饰或压缩图形，以及用于模拟设计和原型制作新的项目。

Adobe Fireworks 最初由 Macromedia 创建并拥有，后于 2009 年被 Adobe 收购。这个对 Web 设计师来说的奇迹应用并没有像 Adobe 的旗舰照片编辑程序 Photoshop 那样受到关注，但这没关系，因为它拥有许多出色的功能，使其成为一个毋庸置疑的必选程序，应包含在你的工具库中。事实上，对于 Web 开发人员和设计师处理的许多任务，Fireworks 是更适合该工作的产品。

就像 Adobe Photoshop 一样，Fireworks 也充满了键盘快捷键，以适应高级用户的需求，同时保持一个稀疏的用户界面，工具、选项和属性易于查找，使得任何 Adobe Fireworks 的新用户都能轻松地找到应用中的方向。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_143_0.png)

**图 8–17.** *在 Windows 7 PC 上运行的 Adobe Fireworks CS5*

Adobe Fireworks 最酷的功能之一是其能够在其特殊格式的 PNG 文件类型中创建 Pages（页面），这将允许设计师非常整洁地创建漂亮的布局，并将其传递给他们的本地开发人员。Pages 的工作方式本质上是在你需要新页面时为你提供一个新的画布。你可以在 Fireworks 中按 F5 键轻松访问你的页面。

当查看你的 Pages 时（如图 8–18 所示），你可以通过简单的鼠标点击选择正在查看和处理的页面。一旦进入新选择的页面，你可以切换到图层标签，查看仅与当前所选页面相关的所有图层，而不必处理单个画布中五个或更多页面的图层。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_144_0.png)

> **图 8–18.** Adobe Fireworks Pages 面板的特写

保持设计整洁将在最终开始编写代码时帮助你。你花在浏览无尽图层的时间越少，试图找到正确的资源以从你的模拟中提取并在网站中使用的时间就越少，那就越好！

此外，当需要向客户展示你的原型时，给他们留下你整洁有序的印象（如图 8–19 和图 8–20 所示）总是一个好主意，表明你会将你在模拟和原型设计中花费的同样的细心和考虑投入到构建他们的网站或应用程序中。




## 小结

嘿，快看！我们又完成了一章，你的脑海里已经积累了更多的知识和有趣的小技巧。现在你对该往哪里走、用什么工具来让你的移动 Web 应用如虎添翼、活力四射有了更清晰的认识。

在这个连时尚设计师都能把流浪汉的行头变得时髦的世界里，在这个你环顾四周都能看到有人在夸赞自己的新 gadget 有多"漂亮"的时代，应用和网站再带着那种"刚出炉的工程味"外观和气息，已经越来越让人无法接受了。就连谷歌也在 Google+ 发布并逐步将全新的 Google+ 主题推广到其众多产品之后，一改往日设计丑陋但功能强大的作风！然而，正如我们迄今为止讨论的所有概念一样，能力越大……责任越大。通过一贯地使用这些工具，你就能打造出视觉效果惊艳且实用的应用！

## 第 9 章

## 基于 HTML5 位置的应用程序

移动开发者最大的机遇之一，源于 Android 手机和平板电脑等设备的本质特性所开启的丰富选择：它们是移动的！虽然传统桌面应用的用户位置可能也有一定价值，但很少有人会整天扛着台式机到处跑。然而移动设备是会移动的，它们的位置（进而也暗指设备用户的位置）可以影响方方面面——从游戏，到产品和信息搜索，再到语言设置和设备行为等多样化的细微差别和选项。

在本章中，我们将探索在 Android 设备上利用 HTML5、CSS 和 JavaScript 实现地理定位。我们将探讨一个简单的支持定位功能的应用，看看如何利用 HTML5 的特性与功能。那么，让我们开始行动吧！

### 地理定位的机制

要将你的地理定位创意变为现实，重要的是要了解所有组成部分的能力（抱歉，这个双关语我们忍不住了）。在任何面向 Android 的地理定位 Web 应用中，有两组能力至关重要。首先，给定 Android 设备向任何基于 Web 的、聚焦位置的应用程序提供了哪些能力？其次，HTML5 的哪些特性（以及较次要的 CSS3 和 JavaScript）提供了定位能力？归根结底，设备能够汇报其位置的多种方式，以及 Web 应用能够利用这些信息做些什么，这两者共同决定了你能实现什么。让我们来看看这两方面的背景知识。

### 了解设备能力

无论你拥有何种设备，它都可以依赖一系列令人惊讶的技术来提供基于位置的数据。即使对于缺乏专用硬件的设备，也存在可选方案 Balls to 当前位置，包括已经经过的 waypoint 以及将要到达的 waypoint。这些对于导航和基于位置的服务非常重要。位置和航向等附加信息也可能被提供，具体取决于设备的能力。这些信息通常用于增强现实（AR）应用或需要精确定位的场景。

在某些实现中，设备可能还提供速度和海拔数据，这对于健身追踪或航空应用特别有用。位置信息的更新频率也可以由应用程序控制，以平衡精度和电池消耗。开发者应该意识到，不同的设备和浏览器组合可能提供不同级别的地理定位服务，因此应该始终设计优雅降级的策略。

### 使用 `watchPosition()` 进行持续监控

除了获取一次性位置快照外，HTML5 地理定位 API 还提供了 `watchPosition()` 方法，用于持续监控用户位置。这个方法会返回一个 watch ID，可以用来稍后清除监控。

**Listing 9–2.** Using `watchPosition()` for continuous location monitoring

```javascript
var watchId = navigator.geolocation.watchPosition(
    successCallback, 
    errorCallback, 
    options
);

// Later, to stop watching
navigator.geolocation.clearWatch(watchId);
```

`watchPosition()` 的参数与 `getCurrentPosition()` 相同，但它会在位置发生变化时多次调用成功回调函数。这对于实时导航或运动跟踪应用至关重要。

### 处理错误和边缘情况

地理位置请求可能因为多种原因失败。作为负责任的开发者，你应该始终准备处理这些情况。

**Listing 9–3.** Error handling in geolocation

```javascript
function errorCallback(error) {
    switch(error.code) {
        case error.PERMISSION_DENIED:
            console.log("User denied the request for Geolocation.");
            break;
        case error.POSITION_UNAVAILABLE:
            console.log("Location information is unavailable.");
            break;
        case error.TIMEOUT:
            console.log("The request to get user location timed out.");
            break;
        case error.UNKNOWN_ERROR:
            console.log("An unknown error occurred.");
            break;
    }
}
```

理解这些错误情况对于创建健壮的地理定位应用至关重要。例如，当用户拒绝权限时，你应该提供备选的输入方式，如手动地址输入。

### 隐私和安全考量

地理位置数据属于敏感个人信息。开发者必须始终将隐私保护放在首位：

- **明确告知用户**：清楚说明为什么需要位置信息以及如何使用
- **最小化数据收集**：只收集应用功能所必需的位置精度
- **安全传输**：始终通过 HTTPS 发送位置数据
- **数据保留策略**：明确位置数据的存储时间和删除机制

不同国家和地区对地理位置数据有不同的法律要求，如欧盟的 GDPR 和加利福尼亚的 CCPA。确保你的应用符合相关法规。

### 优化性能和电池使用

持续使用 GPS 是移动设备上最耗电的操作之一。以下策略可以帮助优化：

| 手脚 | 描述 |
|------|------|
| 降低更新频率 | 使用 `maximumAge` 和 `timeout` 选项控制请求频率 |
| 降低精度需求 | 高纬度时指定 `enableHighAccuracy: false` |
| 及时清理 watcher | 不需要时调用 `clearWatch()` |
| 考虑使用其他信号 | WiFi 或基站定位通常比 GPS 更省电 |

### 实际应用示例

让我们整合所学知识，构建一个完整的地理定位应用示例。该示例展示了如何获取位置、显示地图并处理各种边界情况。

现代 Web 开发中还有更高级的定位技术，如基于蓝牙低功耗（BLE）的信标定位、超宽带（UWB）技术以及结合了多种传感器的惯性导航系统。这些技术在室内定位等 GPS 信号不佳的场景中尤为重要。

随着 5G 网络的普及和边缘计算的发展，地理定位服务的精度和响应速度将进一步提升。未来的应用可能会结合 AR/VR 技术，创造更加沉浸式的基于位置的体验。

开发者在设计位置服务时，还应考虑离线场景、网络延迟和不完整的地理数据等挑战。构建容错能力强、用户体验流畅的地理定位应用需要综合考量技术、设计和用户心理等多方面因素。

## 小结

本章深入探讨了 HTML5 地理定位 API 在移动 Web 开发中的应用。从基础概念到实际代码实现，再到性能优化和隐私保护，我们覆盖了开发健壮地理定位应用所需的核心知识。记住，最佳的位置服务是那些用户几乎注意不到其存在、却能无缝增强应用价值的服务。

下一章我们将探索更多 HTML5 的高级特性，继续扩展你的移动 Web 开发技能树。



## 第 9 章：基于位置的 HTML5 应用程序

关于我们第一段测试地理位置支持的第一段代码，有两点需要注意。首先，确定特定浏览器的支持情况真的如此简单（尽管在本章稍后的“可能会出现哪些问题？”一节中，对于有位置功能但不实际配合的设备进行了一些更为细致的分析）。第二点是，在桌面应用程序中使用 JavaScript alert 函数大多数时候都会让人感到烦恼，而在小屏幕的移动设备上更是令人讨厌得不得了。你们中间经验丰富的通用网页开发者都知道这一点；而对于初学者来说，这也是一个很好的时机，让你们考虑将工作代码封装到一个易于重复调用的函数中，以避免打扰您的好用户。Listing 9-2重构了我们的检测示例以创建一个单独的 geoSupport() 函数，我们可以根据需要重新使用它。

**列示表 9–2。** *修订后的简单地理位置支持检查*

```
<html>
	<head>
		<title>Android Web Application Development-Geolocation example 2</title>
		<script type="text/javascript">
			function supportsGeo () {
				var geosupport = "Sorry, your browser does not support geolocation";
				if (navigator.geolocation) {
					geosupport = "Congratulations, your browser supports geolocation";
				}
				return geosupport;
			}
		</script>
	</head>
	<body>
		<script type="text/javascript">
			document.write(supportsGeo());
		</script>
	</body>
</html>
```

当然，您可以更进一步，将该函数移入单独加载的 JavaScript 源文件中。如果您愿意，请自由这样做并调整本章稍后的代码。

## 探索我们的示例应用程序

是时候介绍我们的样品（测试）应用程序了。除非您一直住在山洞里，您可能已经了解到随着移动设备的爆发式增长而蓬勃发展的各种流行的“签到”风格应用程序的范围。无论是 Foursquare、Latitude、TripIt，还是其他类似的应用程序，所有这些让您向外界宣告您的位置——据推测是为了让您的粉丝和狗仔队能够追踪您的著名活动。许多这些应用程序是作为给定设备本机（本地）应用实现的，但也没有什么能阻止我们在任何设备的浏览器内开发同一风格的应用程序。

我们的应用程序完全自包含于 ch09-example03.html 中，您可以从您选择的 Web 浏览器运行它。让我们先从用户的角度看看它是如何运作的（显然）。将浏览器指向该页面会显示我们新的基于位置的签到风格应用程序非常简单但功能齐全的首页，如图 9-4所示。

目前，它在图形设计方面远非典范之作，但我们稍后会说到这一点。现在让我们来看看当我们点击“地理位置报到！”按钮时会发生什么。图9–5显示了我们的页面已动态更新为看似一组纬度和经度坐标的样子。之所以看起来是这样，因为那正是它所在的确切内容——这些数据确实来自测试运行的非常位置。

## 构建我们基本的地理定位应用程序

到了这一步，您可能想知道要让这个表面上简单的工作程序正常运行需要多少逻辑和代码。让我们看看列示表9–3，在那里我们将看到 ch09-example03.html文件的整套代码。

**列示表 9–3。** *地理位置报到示例*

```
<html>
    <head>
        <title>Android Web Application Development-Geolocation example 3</title>
        <script type="text/javascript">
            function supportsGeo () {
                if (navigator.geolocation) {
                    return true;
                } else {
                    return false;
                }
            }

            function changeDiv (name, data) {
                var div = document.getElementById(name);
                if(div)
                {
                    div.innerHTML = data;
                }
            }

            function checkIn () {
                var geoData = "";
                if (supportsGeo()) {
                    navigator.geolocation.getCurrentPosition(function(position) {
                        geoData = position.coords.latitude + ", " +
                                  position.coords.longitude;
                    });
                    <!-- alert("Confirm geolocation access before clicking OK"); -->
                } else {
                    geoData = "Your browser does not support HTML5 geolocation";
                }
                changeDiv ("myCheckIn",geoData);
            }
        </script>
    </head>
    <body>
        <h1>
            <div id="myCheckIn">
                <!-- This is where your check-in will display -->
                <p>Ready to check in...</p>
            </div>

            <form name="checkInFrm">
                <input type="button" name="checkInBtn" value="Geolocation Check-In!"
                       onClick="checkIn()">
        </h1>
    </body>
</html>
```

让我们将此内容分解为四个部分，以便您可以消化正在发生的事情，同时也可以摆弄和更改代码本身，让我们在前进过程中探索各种可能性。

### 再次测试地理位置支持功能章节开头引入的 supportsGeo()函数已进行了调整以返回布尔值（Boolean value），因此我们可以在其他表达式中使用其行内结果：

```
function supportsGeo () {
    if (navigator.geolocation) {
        return true;
    } else {
        return false;
    }
}
```

这比之前版本提供了更多的实用性，后者返回的只是一个字符串值。

### 为动态页面变化创建工具函数

接下来，我们介绍了一个简单的实用程序（Utility）函数来控制代码中任何位置的 <div>元素上的动态HTML行为。changeDiv()函数接受一个<div>元素的名称以及期望进行的文本更改，并执行必要的操作：

```
function changeDiv (name, data) {
    var div = document.getElementById(name);
    if(div)
    {
        div.innerHTML = data;
    }
}
```

这并不严格与地理位置相关，但我们认为您会同意这样做将使其余的代码示例更清晰一些，因为它将这些更改的机制从主要逻辑中去除。

### 回顾基础 HTML

我们的HTML代码在我们示例中几乎只是无辜的旁观者。它提供了一个命名的<div>元素 myCheckIn，我们要在这个上面运作其地理定位魔法功能的。

```
<h1>
    <div id="myCheckIn">
        <!-- This is where your check-in will display -->
        <p>Ready to check in...</p>
    </div>

    <form name="checkInFrm">
        <input type="button" name="checkInBtn" value="Geolocation Check-In!"
        onClick="checkIn()">
```

表单和输入按钮调用了我们的核心函数checkIn()，该函数将执行实际的地理位置定位工作。

## 深入坐标研究领域

好了，停止在边缘徘徊的舞蹈吧！checkIn()函数在我们这个小示例中执行关键任务。

```
function checkIn(){
	var geoData = "";
	if (supportsGeo()){
		navigator.geolocation.getCurrentPosition(function(position){
			geoData = position.coords.latitude + ", " + position.coords.longitude;
		});
		<!--alert("Confirm geolocation access before clicking OK");-->
	}else{
		geoData = "Your browser does not support HTML5 geolocation";
	}
	changeDiv("myCheckIn",geoData); 
}
```

geoData 变量最终持有了我们所得到的纬度和经度。我们调用 supportsGeo()函数来确保浏览器支持我们的意图。然后我们通过调用 navigator.geolocation.getCurrentPosition()进入正题，这是核心HTML地理位置定位功能之一，在http://dev.w3.org/geo/api/spec-source.html有大量超负荷的定义页面可供参考。

目前您所需要知道的是navigator.geolocation.getCurrentPosition()是一个异步（asynchronous）函数，此处使用的形式向回调函数传递一个一旦浏览器和底层硬件响应对当前位置请求时就会被调用的一次性调用的功能。我们的位置回调将两个数据成员赋值给 geoData 变量：position.coords.latitude和 position.coords.longitude值，这等同于呼叫者的纬度和经度。

剩下的一切是我们只需调用实用程序 changeDiv()函数来更新HTML页面即可，妙极！当然，我们同时也确保不支持地理位置定位的浏览器会被指向适当的信息，表明对我们的位置工作没有任何支持。

> 注意：您可能会看到我们对一个询问用户在继续之前确认访问位置的alert（）调用了注释掉的部分。如果您没有允许网页自由地请求您的位置（而且也没有理由应该这样做），那么在您的浏览器被要求时您将需要确认权限。但即使是速度最快的人类也无法在 navigator.geolocation.getCurrentPosition()调用返回之前执行此操作，尽管它是异步的。此时回调将返回我们的代码当前未捕获的错误（但在本章稍后的“可能出现什么问题？”一节中可以看到该错误处理方法），并且我们的示例将静默失败。取消注释测试中的警报，以便您可以更好地控制navigator.geolocation.getCurrentPosition ()的异步行为。



## 应对 Android 地理定位世界的四大问题

我们的初始示例应用介绍了几乎所有使用地理定位的 Web 应用程序的一些关键构建模块。为了完整地介绍地理定位的世界，我们需要解决四个问题：*我身在何处？*、*我是什么设备？*、*可能出现什么问题？*，以及*我将去向何方？*

### 我身在何处？

我们已经在前面的示例中使用了 `position.coords.latitude` 和 `position.coords.longitude` 数据成员，触及了确定设备位置的基础知识。你可能认为确定位置不过如此，但还有一些额外的数据点值得考虑。

虽然纬度和经度可以告诉你是在夏威夷还是喜马拉雅山脉，但你可能同意，在这两个地方，你都关心另一个维度：海拔高度！HTML5 规范包含一个 `position.coords.altitude` 数据成员，用于提供高于名义海平面的海拔高度。请注意，对这个功能的支持相当不均衡，以至于在许多版本的 Android 开发工具中，即使是 Android 模拟器及其浏览器也不支持它。

除了纬度、经度和海拔高度，你可能还会关心读数的准确程度。我们在本章开头介绍了四种可能的定位机制，每种机制的准确度各不相同。我们可以使用两个额外的数据成员 `position.coords.accuracy` 和 `position.coords.altitudeAccuracy` 来提供任何地理定位数据的误差范围。

有趣的是，没有直接的方法可以确定使用了哪种定位机制来提供你的坐标。你可以通过查询另一个数据值 `position.coords.satellites` 来推断，如果你的浏览器和设备支持，它将返回用于获得 GPS 定位的卫星数量。唯一的问题是，如果你的设备不支持 GPS，或者无法获得 GPS 信号，这两种情况都会返回 NULL。因此，你将处于一种模糊状态，无法确定卫星数量缺失的原因。

### 我是什么设备？

我们已经基本处理了回答*我是什么设备？*这个问题的最佳方法。HTML5 地理定位规范并没有提供详尽的方法来确定设备上存在哪些特定硬件。处理这个问题的最佳方法是使用 `supportsGeo()` 函数，或者我们上一节介绍的类似函数。这将我们的问题转化为：*我是什么设备？是支持地理定位的设备和浏览器组合，还是不支持？*

### 可能出现什么问题？

想象一下，你编写了你的出色签到应用，准备挑战 Foursquare 等应用。你的用户很开心，世界一片美好。不可能出错，对吧？嗯，也许我们说得太早了。

在任何设备上的任何时候，你都可能不得不处理一系列问题，这些问题会阻止你的地理定位代码返回准确的值，甚至根本无法返回任何值。可能是天气原因，太阳和行星的排列（实际上，这比你想象的更严肃），甚至是用户的干预。无论原因是什么，都有明确定义的错误状态需要在代码中处理。

在 HTML5 规范下可能出现的四种主要错误情况是：

- **TIMEOUT**：在允许的时间内，没有定位机制响应并返回位置数据。
- **POSITION_UNAVAILABLE**：你的设备有一个或多个有效的定位机制（如 GPS 或 WiFi），但它们都无法提供有效的位置数据。
- **PERMISSION_DENIED**：由于权限原因，浏览器被阻止访问 HTML5 地理定位 API。要么是用户在提示时拒绝了访问，要么是浏览器被明确配置为阻止访问。
- **UNKNOWN_ERROR**：由于未知原因，位置数据不可用。

了解错误条件是什么固然很好，但如何利用它们呢？你会记得我们说过 `getCurrentPosition()` 函数有大量重载版本。其中很大一部分包含一个常见的模式：第一个参数是用于报告位置的回调函数，第二个参数是用于错误处理的回调函数。看看我们示例应用的下一个迭代版本，文件在 ch09-example03.html。关键的变化在于我们的 `checkIn()` JavaScript 函数，现在看起来像这样。

```
function checkIn() {
    var geoData = "";
    if (supportsGeo()) {
        navigator.geolocation.getCurrentPosition(
            function(position) {
                geoData = position.coords.latitude + ", " + position.coords.longitude;
            },
            function(error) {
                switch(error.code) {
                    case error.TIMEOUT:
                        alert ('Geolocation returned a timeout error');
                        break;
                    case error.POSITION_UNAVAILABLE:
                        alert ('Geolocation returned a position unavailable error');
                        break;
                    case error.PERMISSION_DENIED:
                        alert ('Geolocation returned permission denied (did you deny access?)');
                        break;
                    case error.UNKNOWN_ERROR:
                        alert ('Geolocation encountered an unknown error');
                        break;
                }
            }
        );
        <!-- alert("Confirm geolocation access before clicking OK"); -->
    } else {
        geoData = "Your browser does not support HTML5 geolocation";
    }
    changeDiv ("myCheckIn",geoData);
}
```

在粗体文本中，你会看到我们修改了 `getCurrentPosition()` 函数的方法签名（重载版本），以注册我们的错误回调函数，并在返回任何错误条件时向用户发出警报。我们处于一个有利的位置（好吧，我们有点讽刺），因为 Android 模拟器在响应地理定位请求时以速度慢和喜怒无常而闻名。因此，一个很好的做法是在真实设备和模拟器上都测试你的代码。作者们在第一次尝试时，几乎没有费什么力气就触发了一个 `POSITION_UNAVAILABLE` 错误。你可以在图 9-6 中看到结果。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_159_0.png)

**图 9–6.** *一次地理定位尝试返回了 POSITION_UNAVAILABLE 错误*

就像我们处理 `supportsGeo()` 函数一样，你应该将这种错误检查风格转换为一个工具函数，以便在你的代码中使用，而不是用警报式的错误轰炸用户——尽管，在这种情况下，这可能是合理的。

### 我将去向何方？

为了完整地介绍我们正在探索的能力，我们可以问自己——或者更准确地说是设备——*我将去向何方*？有两种方法值得介绍。首先，我们可靠的地理定位数据成员包括另外两个有用的值：`position.coords.speed` 和 `position.coords.heading`。这些值指示设备的最后已知速度和最后已知方向。这些值听起来非常适合在地图上绘制移动等任务，从理论上讲，这正是它们旨在提供的功能。然而，实际上，相当多的设备要么不报告这些值的数据，要么使用如此简化的 GPS 芯片组，以至于根本不支持收集这些数据。

这就引出了另一种方法。到目前为止，我们一直在展示 `navigator.geolocation` 的 `getCurrentPosition()` 方法。这个方法有一个对等的方法，在确定随时间变化的位置及其相关移动方面，更加复杂和有用。这就是 `watchPosition()` 方法。

`watchPosition()` 方法的各种重载形式与我们的 `getCurrentPosition()` 方法的行为相当相似。它注册一个回调函数用于常规定位，另一个回调函数用于错误处理，但它也接受一系列选项，包括一个定时器选项，用于确定它应该休眠和唤醒自身并*持续调用*你的回调函数的频率。`watchPosition()` 将持续运行，直到通过调用 `clearWatch()` 停止，或者其父进程终止。清单 9-4 展示了我们持续进行的示例应用的下一个迭代版本，来自 ch09-example05.html。

**清单 9-4. 随时间推移（以及移动！）进行地理定位跟踪**

```
<html>
    <head>
        <title>Android Web Application Development-Geolocation example 5</title>
        <script type="text/javascript">
            function supportsGeo () {
                if (navigator.geolocation) {
                    return true;
                } else {
                    return false;
                }
            }

            function changeDiv (name, data) {
                var div = document.get.getElementById(name);
                if(div)
                {
                    div.innerHTML = data;
                }
            }

            function startWatch () {
                var geoData = "";
                var watchOptions = { frequency: 5000 };
                if (supportsGeo()) {
```



geoData = navigator.geolocation.watchPosition(onWatchSuccess,
    onWatchError, watchOptions);
} else {
    geoData = "Your browser does not support HTML5 geolocation";
    changeDiv ("myCheckIn",geoData);
}

function onWatchSuccess(position) {
    var currentLocation = "";
    currentLocation = 'Latitude: ' + position.coords.latitude + ', Longitude: ' +
        position.coords.longitude;
    changeDiv("myLocationWatch",currentLocation);
}

function onWatchError(error) {
    var currentError = "";
    currentError = 'Error code: ' + error.code + ', Error message: ' +
        error.message;
    changeDiv("myLocationWatch",currentError);
}
</script>
</head>
<body>
<h1>
    <div id="myLocationWatch">
        <!-- This is where your check-in will display -->
        <p>Ready to check in...</p>
    </div>
    <form name="watchFrm">
        <input type="button" name="watchBtn" value="Start Watching"
            onClick="startWatch()">
</h1>
</body>
</html>

Our utility functions supportsGeo() and changeDiv() are the same, and the HTML layout is only cosmetically changed. The key is that the button now calls our startWatch() function, which itself ultimately calls watchPosition(). We pass it our regular and error callbacks- onWatchSuccess() and onWatchError()--and an options construct. In this case, our options look like this

```
var watchOptions = { frequency: 5000 };
```

This effectively is used to pass a 5 second refresh frequency to the watchPosition() function. If you run the code yourself, and choose the Start Watching button you see, your browser should update approximately every five seconds with your location. This is a little hard to show in static screen shots, so you'll have to try it for yourself. Don't worry if you aren't actually moving around: you should still see updates to the coordinates, because the accuracy of each reading will be slightly different depending on the number of GPS satellites used for the fix, varying local interference, etc. You should see small changes to the least significant digits even if you are relaxing on your sofa!

## 拓展视野：结合地图应用

想必现在你已经完全同意，我们的示例应用程序还称不上是一件艺术品。那么让我们添加一些亮点，并引入与地理定位几乎形影不离的伙伴：地图！

### 为应用程序添加地图

我们最新的示例来自文件 ch09-example06.html，它使用 Google 地图将我们之前的签到示例提升到了一个新高度。该示例不再仅仅报告数字坐标，而是利用这些坐标配合托管于 http://maps.googleapis.com/ 的 Google 地图 API 来加载地图，并在上面放置标记以突出显示您的位置。清单 9–5 是我们修改后的 JavaScript、CSS 和 HTML5。

清单 9–5. 地理定位与地图协同工作

```
<html>
    <head>
        <title>Android Web Application Development-Geolocation example 6</title>
        <meta name="viewport" content="initial-scale=1.0, user-scalable=no" />
        <style type="text/css">
            html { height: 100% }
            body { height: 100%; margin: 0; padding: 0 }
            #mapContainer { height: 100% }
        </style>
        <script type="text/javascript"
        src="http://maps.googleapis.com/maps/api/js?key=AIzaSyBpoxnQbCGPTIcpIJ8YPO3pTNcJX3zbc4c&sensor=false">
        </script>
        <script type="text/javascript">
            function supportsGeo () {
                if (navigator.geolocation) {
                    return true;
                } else {
                    return false;
                }
            }

            function changeDiv (name, data) {
                var div = document.getElementById(name);
                if(div)
                {
                    div.innerHTML = data;
                }
            }

            function mapMe(thisLat, thisLong) {
                var myLatlong = new google.maps.LatLng(thisLat, thisLong);
                var myOptions = {
                    center: new google.maps.LatLng(thisLat, thisLong),
                    zoom: 12,
                    mapTypeId: google.maps.MapTypeId.ROADMAP
                };
                var map = new google.maps.Map(document.getElementById("mapContainer"),
                                myOptions);
                var marker = new google.maps.Marker({
                    position: myLatlong,
                    map: map,
                    title: "Hello World!"
                });
            }
        </script>
    </head>
<body onload="initialize()">
    <div id="mapContainer" style="width:100%; height:100%">
        <!-- Your map goes here! -->
    </div>
</body>
</html>

function initialize() {
    if (supportsGeo()) {
        myLatitude = "";
        myLongitude = "";
        navigator.geolocation.getCurrentPosition(
            function(position) {
                myLatitude = position.coords.latitude;
                myLongitude = position.coords.longitude;
            },
            function(error) {
                switch(error.code) {
                    case error.TIMEOUT:
                        alert ('Geolocation returned a timeout error');
                        break;
                    case error.POSITION_UNAVAILABLE:
                        alert ('Geolocation returned a position unavailable error');
                        break;
                    case error.PERMISSION_DENIED:
                        alert ('Geolocation returned permission denied (did you deny access?)');
                        break;
                    case error.UNKNOWN_ERROR:
                        alert ('Geolocation encountered an unknown error');
                        break;
                }
            }
        );
        alert("Confirm geolocation access before clicking OK");
    }
    mapMe(myLatitude, myLongitude);
}
```

You'll note that our code starts with some CSS, and ends with very simple HTML that invokes our new initialize() method as soon as the page loads. The CSS is boilerplate stuff from Google to allow a div to act as a container for map objects. Following this, you'll see the JavaScript reference to the Google Maps API (the following line has the formatting massaged to better fit this page):

```
<script type="text/javascript"
  src="http://maps.googleapis.com/maps/api/js?key=AIzaSyBpoxnQbCGTICpIJ8YP03pTNcJX3zbc4c&sensor=false">
</script>
```

This invokes the Maps API with a particular API key. This is Google's technique for uniquely identifying users of its API, and also rate-limiting how many calls to various APIs can be made. You should definitely sign up for your own API key so that you can control your own API access, monitor usage, etc.

> **提示：** 在本书印刷之时，免费的 Google 地图 API 限制为每天 25000 次调用。要获取您自己的地图 API 密钥，请访问 http://developer.google.com/ 并按照说明操作。

Our initialize() function is very similar to our old checkIn() function, so we won't rehash that here. The key differences are it populates two local variables for latitude and longitude, and then calls our new function, mapMe(), to do all the hard mapping work.

```
function mapMe(thisLat, thisLong) {
  var myLatLong = new google.maps.LatLng(thisLat, thisLong);
  var myOptions = {
    center: new google.maps.LatLng(thisLat, thisLong),
    zoom: 12,
    mapTypeId: google.maps.MapTypeId.ROADMAP
  };
  var map = new google.maps.Map(document.getElementById("mapContainer"), myOptions);
  var marker = new google.maps.Marker({
    position: myLatLong,
    map: map,
    title:"Hello World!"
  });
}
```

Within mapMe(), we complete four main actions to present our map and location marker. First, we create a google.maps.LatLng object using the latitude and longitude we received from our HTML5 geolocation calls. Next, we construct an options object named myOptions, which consists of a center object which will be used to choose the center of the map presented in the browser. The zoom value dictates the starting zoom setting in the map—this is very important on mobile devices, as the default zoom is at far too high a scale, leaving the user to zoom in several times with imprecise pinch and zoom techniques.

We then get to the meat of our mapping. We create a new google.maps.Map object, and pass the element that will hold the map ("mapContainer" is the ID of our <div> in our HTML), and the options object we constructed. This actually creates and displays the map in the user's browser. Following its creation, we create a google.maps.Marker object at the same coordinates on our map, and give it a meaningful label. The results in Figure 9–7 speak for themselves.

# 第 9 章：基于 HTML5 位置的应用程序



## 其他基于位置的服务

我们已经了解了一种流行的地图服务，但值得考虑拓宽视野，看看其他提供基础地理定位服务的提供商，以及提供地图瓦片（即实际显示的图形"瓦片"）的提供商。

你可能有以下几个理由考虑分散风险，并至少确保你能够使用其他服务执行等效操作：

-   **免费服务、可扩展性和成本：** 许多服务，如Google、Yahoo、Bing、MapQuest、Nokia/Ovi等，都提供某种程度的免费服务。通常的条款规定，你和你的用户每天可以消费一定数量的地图请求，之后就会被限速，或者被要求付费。
-   **不同的优势和劣势：** 一些服务，如Google，提供有用的东西，比如某些地点的路线指引、公共交通详情等。但在其他地方，像Open Street Map这样的服务提供了更详细的、更新的数据，而对于一些服务如OpenCycleMap，整个地图渲染和数据都专注于专业用途：在这种情况下，是针对自行车手。
-   **职责分离：** 虽然使用单一服务来完成所有事情很方便，但你可能会发现你希望将检索给定位置周围原始地图数据和渲染该位置相关图像（地图瓦片）这两个方面分离开来。抽象化你的地图服务意味着你可以根据需要进行混合和匹配。

抽象化你的地图数据和图像提供商的最重要原因可能是，这个领域正在快速发展和变化，良好的软件工程实践应该引导你将所有其他代码与此类不稳定的依赖项隔离开来（只要可能）。这种不稳定性也可能是提供商自身进行版本升级和更改的结果。

这里有一些有用的数据提供商、地图瓦片提供商、一体化服务，甚至现成的地图抽象JavaScript库，你也可以考虑，除了那些常见的选择之外：

-   Open Street Map (openstreetmap.org)—最初的开放数据提供商之一，现在也在基于众包的地理定位数据之上提供其他服务。
-   CloudMade (cloudmade.com)—一个用于Open Street Map数据的地图瓦片提供商。也是Leaflet的提供者，这是一个开源的瓦片集服务。
-   Mapnik (mapnik.org)—一个地图渲染器，经常在其他工具中找到（包括这里列出的一些其他工具）。
-   CartoDB (cartodb.com)—一个基于云的空间数据库。
-   Mapstraction (mapstraction.com)—一个现成可用的JavaScript库，提供对地图服务和数据提供商的抽象。
-   Wax (mapbox.com/wax)—另一个现成的抽象层。来自同一家公司的TileMill，用于生成瓦片。

这个列表可以写满好几页，但你明白这个意思。更令人兴奋的是，意识到每周都有几十家这样的公司和服务提供商涌现出来。

## 调试你的位置信息

即使你正在开发移动应用，也不要忘记可以使用手头的工具来帮助测试和完善你的地理定位代码。例如，Eclipse中的Android Developer Tools插件中的DDMS为你提供了为模拟器设备设置任意坐标/位置数据的能力。在模拟器中运行项目时，你可以切换到DDMS模式，并打开Emulator Console标签页。你将看到设置原始坐标的能力，或者直接提供GMX或KML数据的能力，如图9-8所示，你的模拟器浏览器随后可以使用这些数据。

如果运行Eclipse不是你首选的开发方式，你也可以使用Android的adb工具来发出`geo fix`命令，提供纬度、经度和高度。最后，如果你正在调试一个未连接到计算机的设备上的应用程序，你可以使用免费应用程序Fake GPS location (`https://market.android.com/details?id=com.lexa.fakegps`)来设置你的位置。

### 调试你的位置信息——为了好玩！

探索Web应用程序地理定位功能的好方法之一就是把它做成一个游戏——字面意思！使用上一节中的简单构建块，你可以构建游戏和活动，包括寻宝游戏、定向越野活动，甚至驾驶、赛车和帆船游戏。你会发现将我们的`startWatch()`示例与我们的Google Maps示例结合起来创建一个“地图轨迹”风格的应用程序非常直接，该应用程序可以在地图上实时绘制你的移动轨迹，并且根据游戏或竞赛的不同，还可以显示其他玩家的移动和位置，甚至显示其他整个游戏进行的位置。

地理定位功能的有趣应用，例如我们在这里展示的，在流行的“geocaching”（地理寻宝）运动中可以找到。用你偏好的搜索引擎做产房搜索以获取更多详情，或者继续到第10章，使用你自己的搜索界面进行搜索！

天空真的是极限（事实上，你的地理定位数据应该也能在你最喜欢的热气球上愉快地工作！）。

## 总结

在本章中，我们探讨了作为移动Web开发人员可以使用的基于位置的功能。我们的示例应用程序演示了如何使用你手头的许多核心地理定位功能，包括你在哪里、你的用户设备可能具有什么功能，以及如何处理持续的位置变化。我们将在第10章进一步探讨地理定位应用程序开发，并涵盖其他在线服务和API。

# 使用云服务：一个交通应用

掌握地理定位的基础知识固然很好，正如我们在第9章所学，我们可以用坐标来获得乐趣。一旦我们知道我们在哪里，以及有哪些其他服务可以将我们的位置信息与其他数据混合使用，大量的可能性就会打开。在本章中，我们将利用我们的地理定位知识，并结合一些本地搜索功能，来构建一个个性化的交通应用。

我们的示例交通应用将找到你的位置，然后搜索你最近的交通选择，无论是公共汽车站、地铁站或火车站，甚至机场。有了这些基础知识，你将能够将我们的交通应用扩展到几乎任何搜索加位置的问题。

作为一名开发人员，在将基于Web或云的服务与自己的应用程序混合时，你有许多选择来决定你想做多少工作。你可以选择使用公开可用的数据馈送构建自己的服务，使用完整服务，或者构建混合型服务。使用完整服务将让我们在本章中没什么可谈的，所以我们选择了混合方法，我们将利用我们的地理定位知识使用标准搜索服务来提供有用的交通信息。

在我们深入代码、示例和解释之前，花一点时间考虑一下你可能已经在使用但可能没有主动思考的各种构建块。在构建任何类型的交通或运输应用程序时，我们希望结合知识和数据，然后向用户提供一些有用的选项。这些可能包括：

-   **我是谁？** 从某种意义上说，思考使用你的应用程序的“谁”是实际用户和他们使用的设备及其功能的组合会很有用。我们将重用第9章介绍的检测代码，以确定设备是否支持地理定位。
-   **我在哪里？** 从第9章中，我们学习了如何根据Android设备及其浏览器的地理定位功能来确定用户的位置。我们将把这个基本的起点作为驱动其他选项的基础。
-   **我想去哪里？** 这总是一个微妙的问题。应用程序用户心中是否有一个目的地，或者一种交通类型，或者实际上对如何在两点之间旅行有任何偏好。这里要记住的两个关键点是：不要过早地限制你在应用程序中提供的选项，而且当你确实限制选项时，要刻意地让用户知道。例如，让他们知道有其他路线或交通方式可用。
-   **在线服务知道关于我和我的位置的什么？** 这是一个很大的领域，涵盖了许多通用服务。给定一个位置和某种期望的旅程或目的地，思考一下作为开发人员你可以获得哪些帮助，这样你就不需要自己做所有的工作。例如，来自Google、Yahoo和Microsoft等公司的通用网络搜索API可以处理许多类型的交通搜索，包括查找交通站点、测量距离和计算交通时间。使用这些，这样你就不用自己做了（除非，当然，你的目标是竞争这个领域）。
-   **专业服务知道关于我的位置的什么？** 这是需要考虑的最大领域，但不要感到畏惧。专业API和服务存在于令人眼花缭乱的各种交通和运输类型中。世界各地大量的公共交通机构提供时刻表和路线数据，我们将在本章后面讨论。然而，许多机构还提供直接的API来回答关于下一班服务、最近服务等的查询。聚合器存在以提供跨提供商的服务。一个例子是Kayak用于航空交通搜索。你可以通过思考（并询问）你的用户为什么要进行特定的旅行，将专业API更进一步。如果是为了去电影院、在餐馆吃饭或参加其他活动，像Yelp、TripAdvisor等服务提供API来搜索特定的场所和活动。作为应用程序开发人员，你可以创建结合所有这些的应用程序，以针对你的用户。
-   **我能用这些知识得出什么有用的结论？** 采用你的应用程序收集的关于用户在哪里、他们想去哪里以及他们到达后想做什么的数据，你开始描绘应用程序的流程和功能。专注于使用前面段落中描述的构建块，而不是重新发明它们，你将构建出引人注目、脱颖而出的应用程序。举个例子，想象一下，如果你知道用户想乘船从曼哈顿去布鲁克林参观一家特定的餐厅。你可以将体验提升到下一个层次，使用OpenTable在线服务检查可用性，并注意到...

## 介绍“移动我”示例应用

我们的示例应用名为“移动我”。我们将用它来探索如何从任何位置查找附近的交通方式。当然，我们将使用第9章介绍的技术来检测我们的位置。具体来说，我们将利用安卓设备的地理定位功能确定我们的纬度和经度，然后利用这些数据驱动搜索服务，找到我们偏好的交通方式。

## 分析代码

代码清单10-1展示了“移动我”应用第一个版本的代码。不要被它的长度吓倒：我们将分解并讲解各个组件，帮助你理解其工作原理，并激发你将此示例进一步扩展，融入自己的想法。

**代码清单10-1.** *“移动我”应用源代码，版本1*

```html
<!--
Licensed under the Apache License, Version 2.0: http://www.apache.org/licenses/LICENSE-2.0
-->
<html>
    <head>
        <title>Move Me! - Transit Search Example
        </title>
        <link href="./ch10-example01.css" rel="stylesheet" type="text/css"/>
        <script
            src="http://www.google.com/jsapi?key=AIzaSyBU-TWQkYc-ynkeVIrd_aPOUdyRieCyRO"
            type="text/javascript">
        </script>
        <script type="text/javascript">
            google.load('maps' , '3', {"other_params":"sensor=false"});
            google.load('search', '1');

            var myLatLong;
            var myTransitMap;
            var myLocalSearch;
            var searchResults = [];

            var resultMarker = new google.maps.MarkerImage(
                "Red_Train_Marker.png",
                new google.maps.Size(20, 34),
                new google.maps.Point(0, 0),
                new google.maps.Point(10, 34));
            var youMarker = new google.maps.MarkerImage(
                "You_Marker.png",
                new google.maps.Size(20, 34),
                new google.maps.Point(0, 0),
                new google.maps.Point(10, 34));

            function supportsGeo () {
                if (navigator.geolocation) {
                    return true;
                } else {
                    return false;
                }
            }

            function changeDiv (name, data) {
                var div = document.getElementById(name);
                if(div)
                {
                    div.innerHTML = data;
                }
            }

            function getLocation() {
                if (supportsGeo()) {
                    myLatitude = "";
                    myLongitude = "";
                    navigator.geolocation.getCurrentPosition(
                    function(position) {
                        myLatitude = position.coords.latitude;
                        myLongitude = position.coords.longitude;
                    },
                    function(error) {
                        switch(error.code) {
                            case error.TIMEOUT:
                                alert ('Geolocation returned a timeout error');
                                break;
                            case error.POSITION_UNAVAILABLE:
                                alert ('Geolocation returned a position unavailable error');
                                break;
                            case error.PERMISSION_DENIED:
                                alert ('Geolocation returned permission denied (did you deny access?)');
                                break;
                            case error.UNKNOWN_ERROR:
                                alert ('Geolocation encountered an unknown error');
                                break;
                        }
                    }
                    );
                    alert("Confirm geolocation access before clicking OK");
                }
                myLatLong = new google.maps.LatLng(myLatitude, myLongitude);
            }

            function prepareMap() {
                // Union Square test
                myLatLong = new google.maps.LatLng(37.788056, -122.4075);
                //getLocation();

                myTransitMap = new google.maps.Map(document.getElementById("map"), {
                    center: myLatLong,
                    zoom: 14,
                    mapTypeId: google.maps.MapTypeId.ROADMAP
                });

                var yourMarker = new google.maps.Marker({
                    position: myLatLong,
                    map: myTransitMap,
                    icon: youMarker,
                    title:"You!"
                });

                myLocalSearch = new GlocalSearch();
                myLocalSearch.setSearchCompleteCallback(null, processLocalSearchResults);
            }

            function execSearch() {
                var searchText = document.getElementById("searchtext").value;
                myLocalSearch.execute(searchText);
            }

            function processLocalSearchResults() {
                for (var i = 0; i < myLocalSearch.results.length; i++) {
                    searchResults.push(new LocalResult(myLocalSearch.results[i]));
                }
            }

            // Google's common example LocalResult object
            function LocalResult(result) {
                var me = this;
                me.result_ = result;
                me.resultNode_ = me.node();
                me.marker_ = me.marker();
                document.getElementById("resultlist").appendChild(me.resultNode_);
            }

            LocalResult.prototype.node = function() {
                if (this.resultNode_) return this.resultNode_;
                return this.html();
            };

            LocalResult.prototype.marker = function() {
                var me = this;
                if (me.marker_) return me.marker_;
                var marker = me.marker_ = new google.maps.Marker({
                    position: new google.maps.LatLng(parseFloat(me.result_.lat), parseFloat(me.result_.lng)),
                    icon: resultMarker,
                    map: myTransitMap});
                return marker;
            };

            LocalResult.prototype.html = function() {
                var me = this;
                var container = document.createElement("div");
                container.className = "unselected";
                container.appendChild(me.result_.html.cloneNode(true));
                return container;
            }

            GSearch.setOnLoadCallback(prepareMap);
        </script>
    </head>
    <body>
        <p>Move Me! Transit Search Example</p>
        <div style="width: 330px;">
            <input type="text" id="searchtext" style="width: 240px;"/>
            <input type="button" value="Find" onclick="execSearch()"/>
            <div style="position: absolute; left: 440px;">
                <div id="resultlist">
                </div>
            </div>
            <div id="map" style="height: 450px;"></div>
        </div>
    </body>
</html>
```

首先，我们来处理一些简单的内容。你应该已经从我们第9章的地理定位介绍中认出了几个JavaScript函数。我们的老朋友 `supportsGeo()` 和 `changeDiv()` 都在，分别执行相同的地理定位支持检测和 `<div>` 内容更改功能。

我们的示例代码对我们调用某些公开可用服务的方式进行了一些微调。在这种情况下，因为我们选择使用谷歌地图API及其搜索API，我们对加载谷歌JavaScript库进行了重构，首先加载基础框架，如下所示：

```html
<script
    src="http://www.google.com/jsapi?key=AIzaSyBU-TWQkYc-ynkeYIrd_aPOUFdyRieCyRo"
    type="text/javascript">
</script>
```

然后，在我们自己的JavaScript代码中，我们使用谷歌的 `google.load()` 函数来额外加载地图API和搜索API。如果你选择其他服务或服务集，如Bing、Yahoo、百度或其他，加载API的方式将相应改变以匹配那些服务的调用方式。对于我们这个示例，代码非常简单：

```javascript
google.load('maps' , '3', {"other_params":"sensor=false"});
google.load('search', '1');
```

> 注意：如果你更熟悉，可以改回使用谷歌地图版本2的API，但你会看到反复出现的警告，指出它已被弃用，尤其是在依赖该版本API的网站上。

## 处理全局状态

接下来，我们设置一些全局状态变量，这些变量能很好地说明我们将如何使我们的交通应用工作。

```javascript
var myLatLong;
var myTransitMap;
var myLocalSearch;
var searchResults = [];
```

变量名应该描述了它们的用途，但万一还有疑问，我们将使用 `myLatLong` 来保存用户的坐标；`myTransitMap` 代表用户位置的地图，最终也将包含附近的交通选项；`myLocalSearch` 是搜索对象，它将包含我们查找相关交通选项的标准；最后，`searchResults` 数组将保存从 `myLocalSearch` 搜索返回的结果。

## 自定义位置标记

如果你曾经使用过任何类型的在线地图服务，你可能熟悉用于标记位置的虚拟“地图图钉”。在我们的示例中，由于我们使用谷歌地图，我们使用 `google.maps.Marker` 对象来表示地图上的特定位置。我们没有使用谷歌地图默认提供的标准红色地图标记图标，而是为我们的“移动我”应用制作了一些自定义标记。我们的自定义 `google.map.MarkerImage` 图形的代码如下：

```javascript
var resultMarker = new google.maps.MarkerImage(
    "Red_Train_Marker.png",
    new google.maps.Size(20, 34),
    new google.maps.Point(0, 0),
    new google.maps.Point(10, 34));
var youMarker = new google.maps.MarkerImage(
    "You_Marker.png",
    new google.maps.Size(20, 34),
    new google.maps.Point(0, 0),
    new google.maps.Point(10, 34));
```

所引用的两个 .png 图像文件包含在本书的源代码中。第一个，`Red_Train_Marker.png`，是基于谷歌地图使用的普通红色图钉设计的，增加了字母T，代表交通或运输。`You_Marker.png` 地图图钉是一个蓝色标记，上面叠加了“You”这个词。我们为地图图钉指定了正常尺寸，以便用户在希望点击标记以查看“信息气泡”获取特定点的更多详细信息时能更方便。这使得图钉在小型手机屏幕上看起来稍大一些，但保持正常尺寸很重要，以减少用户在按屏幕时错过点击图钉的可能性。

你会注意到两个 `MarkerImage` 对象都调用了两次 `google.map.Point()`。第一次设置用作叠加层的图像的原点。在我们之前的示例中，我们没有改变默认值。第二次调用 `google.map.Point()` 设置图像的锚点。默认情况下，当



## 准备我们的地图

完成这些准备工作后，我们深入到用于驱动我们交通应用的主要函数——`prepareMap()`函数。

```
function prepareMap() {
    getLocation();

    myTransitMap = new google.maps.Map(document.getElementById("map"), {
        center: myLatLong,
        zoom: 14,
        mapTypeId: google.maps.MapTypeId.ROADMAP
    });

    var yourMarker = new google.maps.Marker({
        position: myLatLong,
        map: myTransitMap,
        icon: youMarker,
        title:"You!"
    });

    myLocalSearch = new GlocalSearch();
    myLocalSearch.setSearchCompleteCallback(null, processLocalSearchResults);
}
```

`prepareMap()`函数易于理解，可分解为四个主要动作。首先，我们调用`getLocation()`函数，这主要是第9章清单9-5中`initialize()`函数所示代码的重新包装版本。为完整起见，此处再次列出：

```
function getLocation() {
    if (supportsGeo()) {
        myLatitude = "";
        myLongitude = "";
        navigator.geolocation.getCurrentPosition(
            function(position) {
                myLatitude = position.coords.latitude;
                myLongitude = position.coords.longitude;
            },
            function(error) {
                switch(error.code) {
                    case error.TIMEOUT:
                        alert ('Geolocation returned a timeout error');
                        break;
                    case error.POSITION_UNAVAILABLE:
                        alert ('Geolocation returned a position unavailable error');
                        break;
                    case error.PERMISSION_DENIED:
                        alert ('Geolocation returned permission denied (did you deny access?)');
                        break;
                    case error.UNKNOWN_ERROR:
                        alert ('Geolocation encountered an unknown error');
                        break;
                }
            }
        );
    }
    myLatLong = new google.maps.LatLng(myLatitude, myLongitude);
}
```

与前面章节一样，这使用了浏览器的navigator.geolocation对象来确定你的纬度和经度。为节省篇幅，此处将省略重复的近乎相同的代码。

然后我们创建一个新的google.maps.Map对象，名为myTransitMap，并将地图中心设置为检测到的位置。我们将缩放级别设置为14，因为这是人类步行的良好比例尺，尽管你可以将其更改为任何所需的缩放设置。我们还选择标准道路地图样式，而非卫星视图。

> **提示：** 以下是一些在为用户渲染地图时需要牢记的缩放级别设置便捷值。

**缩放级别 12：** 适用于公路级驾驶，显示数十英里或公里范围内的主要路线。

**缩放级别 14：** 适合市区内驾驶，以及当距离超过几十码或米时的总体步行导航。

**缩放级别 15：** 最适合详细的步行导航，显示建筑轮廓，以及显示单行道和其他障碍物的驾驶导航。

在我们的myTransitMap对象上，我们在检测到的手机或设备的相同纬度和经度处放置一个标记。我们使用之前描述的自定义蓝色“你”标记，甚至提供一些悬停文本以强化此标记将你定位在地图上的事实。

最后，我们构造一个新的本地搜索对象myLocalSearch，然后注册回调函数processLocalSearchResults()。当此搜索对象完成搜索执行时，将调用此函数。回调机制将在本章稍后展示。随着prepareMap()函数的完成，我们实际上可以看到当用户最初在他们的设备上运行我们的应用程序时的样子，如图10–1所示。

我们对起始示例做了一些调整，将坐标设置在Android模拟器中的一个相当著名的位置：旧金山的联合广场。这并不像听起来那么刻意。想象一下你是旧金山的一名游客。你已经看过了城市的风景和声音，发现自己在联合广场，想要找到火车、公共汽车或渡轮去你的酒店或其他目的地。这就是我们示例应用程序其余功能发挥作用的地方。

## 执行本地交通搜索

示例中的接下来两个函数执行我们选择的本地搜索任务并处理结果。

```
function execSearch() {
    var searchText = document.getElementById("searchtext").value;
    myLocalSearch.execute(searchText);
}
```

execSearch()函数只是读取我们HTML表单中searchtext字段的内容（在图10-1顶部可见），并用该文本调用myLocalSearch()对象的execute方法。我们已将processLocalSearchResults()方法注册为当myLocalSearch()报告执行完成时的回调函数。

```
function processLocalSearchResults() {
    for (var i = 0; i < myLocalSearch.results.length; i++) {
        searchResults.push(new LocalResult(myLocalSearch.results[i]));
    }
}
```

processLocalSearchResults()函数遍历我们的结果，实例化LocalResult对象，并将它们添加到searchResults数组中。LocalResult对象是Google在其许多API示例中使用的一个常见示例对象，我们在此复制了它。我们主要使用它是因为它便于我们随后访问本地搜索结果的坐标。它执行与我们之前代码类似的工作，因为它在我们的地图上放置一个标记，并且还创建一个文本结果列表。在我们当前的示例中，我们创建了CSS来隐藏文本列表，但我们将很快介绍相关选项。

最后，就我们的JavaScript而言，我们注册prepareMap()函数作为Google搜索API加载完成后调用的回调。

```
GSearch.setOnLoadCallback(prepareMap);
```

剩下的就是实际的HTML代码，它控制我们地图的大小、搜索字段和查找按钮，以及相关的<div>名称和嵌套。我们特意为整体显示及其内部的地图对象选择了明确的像素尺寸，以适应手机上的垂直显示和平板电脑上的水平显示，同时也显示我们将在本章稍后介绍的文本结果。

```
<body>
    <p>Move Me! Transit Search Example</p>
    <div style="width: 330px;">
        <input type="text" id="searchtext" style="width: 240px;"/>
        <input type="button" value="Find" onclick="execSearch()"/>
        <div style="position: absolute; left: 440px;">
            <div id="resultlist">
            </div>
        </div>
        <div id="map" style="height: 450px;">
        </div>
    </div>
</body>
```

我们的HTML显示了你在图10–1中看到的简单表单。

## 运行我们的代码

那么，当我们实际搜索交通选项时会发生什么？在我们目前的示例中，候选用户是一名发现自己在联合广场的游客，正在寻找最近的交通选项。如果你发现自己在旧金山，你可能会想到使用湾区快速交通系统，即BART。所以让我们以此作为标准，来显示当我们调用execSearch()时实际发生的情况。图10–2显示了通过我们本地搜索调用返回的结果，并使用LocalResult对象绘制在我们的地图上。

看哪，我们找到了四个最近的BART车站，从市政中心到内河码头。你也可以看到我们在本章开头描述的自定义交通MarkerImage和Marker对象的最终渲染效果。

也许，作为一名游客，你真正想要的是旧金山湾的壮丽景色，而比寻找最近的渡轮码头去探索世界上伟大水道之一的巡游更好的方式是什么？图10-3显示了我们的应用程序找到最近的渡轮码头。



图 10–3。*使用 Move Me 查找渡轮运输服务* 

再次，我们如愿找到了通勤选项。在这种情况下，你注意到有几个标记重叠在一个位置上。这是谷歌搜索返回在该位置运营的几家不同的渡轮公司和渡轮选项，而不是我们所使用的 HTML 或 JavaScript 中出现了错误。

## 改进"Move Me"示例应用程序

到此为止，你会注意到我们的表单的简单性实际上变得有点繁琐。当然，你的用户可以在当地搜索中输入他们想要的任何内容，但也许你想免去他们在小型软键盘上输入的麻烦。我们示例代码的第二版（在文件 ch10-example02.html 中）对表单代码进行了改进，为常用的交通类型提供了简单的按钮，并调用我们要修改的 `execSearch()` 函数。我们的新表单代码如下所示：

```
<div style="width: 330px;">
    <input type="button" value="Subway" onclick="execSearch('BART station')"/>
    <input type="button" value="Train" onclick="execSearch('train station')"/>
    <input type="button" value="Bus" onclick="execSearch('bus stop')"/>
    <input type="button" value="Ferry" onclick="execSearch('ferry terminal')"/>
<div style="position: absolute; left: 440px;">
```

我们修改后的 execSearch() 函数不再需要从文本字段读取数据，主要是因为我们已经将其删除了！相反，它在我们调用函数时传递的文本（例如 "train station" 或"ferry terminal"）作为参数接收，并调用相关搜索的执行。

```
function execSearch(searchText) {
  myLocalSearch.execute(searchText);
}
```

我们的应用程序现在看起来立即可用了一些，具有适用于 Subway、Train, Bus 等的相应按钮，如图 10–4 所示。在此之后，按下一个按钮就会产生像以前一样的结果，显然是根据为每个按钮编制的条件而量身定制的。

## 处理其他交通可能性

你可以从本例中将其扩展到无数种方式。一个明显的例子是扩展用于交通选项的按钮数量。您可以包含出租车、机场、有轨电车等。也有其他需要考量的细微之处。旧金山的地铁可能指的是 BART 系统，但 Muni 系统的很大一部分也被认为是地铁。在其他城市，地铁有其他名称，例如伦敦的"Underground"或巴黎的"Metro"。代码可以扩展以重用您的位置坐标来确定用户当前位于哪个城市，并相应地本地化搜索文本。

## 对我们方法的局限性

我们以前的示例适用于查找我们自己、当地交通站点或车站的内容。这确实有助于计算从任何给定位置出发可能的通勤选项，但就像一段未完成的旅程一样，它让我们离真正想要到达的地方还差一点点。我们可能知道拐角处有公交车站，或者街对面有火车站，但我们是否知道这些地点运营什么服务以及它们前往何处？我们知道下次服务计划何时到达吗？甚至我们要想知道该车站是否有计划的服务吗？

如果有一种方法可以找到与我们发现的交通站点匹配的公交时刻表数据就好了！

## 介绍公共交通数据资源

迄今为止，我们探索了如何查找我们自己及其周围的可能交通工具选项，并将结果绘制在地图上。但正如任何旅行员可以告诉你的那样，了解*何时*有运输工具可用与其从何处运营同样重要。如果有办法利用公交车程表、火车时刻表和其他交通日程安排来扩大我们的通勤应用程序的可能性，那该有多好！好吧，确实有一种方法！

## 充分利用公交时间和时间表

试图与交通管理部门的数据进行协作的历史漫长而曲折。为了免于让您忍受之前开发人员所遭受的痛苦，我们将故事缩短：我们将聚焦于“过去”和“现在”。1995 年以前，处理各种政府或官僚机构以获取其交通数据是一项代价高昂的受虐练习。未记录的专有格式、阻挠公众利益的官员以及对所有权扭曲的观念模糊了任何使用“公共”交通枢纽数据的尝试。

在 1995 年，波特兰 TriMet 公共交通机构的员工对可用的专有的地图和交通枢纽数据来源感到沮丧。她是美国俄勒冈州的主要城市之一的人。她写信给当时许多主要的制图和地理定位服务提供商，询问他们有何计划将公共交通数据纳入其服务中。只有一家公司作出了回应：Google。

从当时的开发者的角度来看，处理掌管数据的机构的反复无常——甚至有时任性——的态度是极其令人沮丧且复杂的。但 TriMet 的探究性问题打开了这样一个想法：渴望获取数据的沮丧开发人员与同样希望看到数据更好地利用来为社区服务的沮丧的数据保管人和公共官员形成了对应关系。

这激发了通用交通 feeds 格式 (GTFS) 的出现，旨在为交通枢纽数据的格式提供一致的协议。任何这个时代的史学家都会观察到，GTFS 格式几乎正是 TriMet 在波特兰用于其枢纽数据的格式。通常情况就是如此，某个技术领域的先行者实际上是事实上的标准制定者。很快就有更多的政府和交通机构有远见地以该格式发布他们持有的数据，并已成为共享交通枢纽日程、路线和相关信息的标准。

几乎每个人都在一度或另一程度上乘坐过公交车、火车、飞机或渡轮，因此我们可以跳过 GTFS 馈送是什么内容的基础知识。相反，让我们从 Android 开发者的角度来看这份规范。

## 审查 GTFS 组件

GTFS feed 只是一堆以逗号分隔格式表示的文本文据数据，分为几个文本文件，然后打包成单个 zip 文件以便于处理。作为 Web 应用程序或原生 Android 应用程序的开发者，您可以获取 GTFS feed 的 zip 文件并与其协作，将交通枢纽位置、时刻表信息等内容纳入您的代码中。一个典型的GTFS zip档由（需要）以下文本文组成：

- **Agency.txt** 在本GTFS包中提供数据的机构和组织。
- **Calendar.txt**各服务基于周班表的日期。这包括服务的起始和结束日期，以及它们有可用和无可用的时间等细节内容。 
- **Routes.txt**给定服务经过的站点集合及其之间的路径。这对应于大多数人认为的单条公交线路、火车行程等内容。
- **Stops.txt** 供乘客上下车的独立位置，其中也包括终点或端点站。
- **Stop_times.txt**一辆给定车辆到达并离开站点的时间。这也允许计算“停留时间”，即服务停留在车站的时段。
- **Trips.txt**给定路线上的行程，期间该给定的车辆依次停靠站点。

除了前面的强制性文件列表外，给定的GTFS feed 还可以在下述文本文件中包括或部分/全部包含以下可选附加数据：

- **Calendar_dates.txt**列出日历文件中标准调度服务详情的例外情况。
- **Fare_attributes.txt**关于使用给定服务的实际费用详情，由运营该服务的机构收取的费用为准。其中可能涉及学生、老年人和其他群体的优惠票价等规定。 
- **Fare_rules.txt** 应用 fare_ attributes.txt 中规定的价格的规则。这可以包括高峰和低谷时段规则、针对学生和老年人的津贴等内容。
- **Feed_info.txt**关于此 GTFS feed 的附加信息，例如版本号及适用日期。
- **Frequencies.txt**不经常运行到常规频率的服务的时间表信息。 
- **Shapes.txt**帮助绘制路线图形详情的内容（如何表示返回路径和回程点等的差异）。
- **Transfers.txt**关于从一个交通工具换乘至另一个工的交通的规则详情等。

有关各个文件字段、格式要求和其他规则的详细信息，可找到任何众多与GTFS相关的网站上的信息，例如 https://developers.google.com/transit/ 。世界各地的许多交通机构都在利用中央交易所作为 GTFS 数据资源，其位于 www.gtfs-data-exchange.com/ 。该站点不仅充当了 GTFS feed的存储库中心站，并且还包含有关规范的简介和贡献新GTFS数据集等方面的详细信息。

如果这一切听起来令人振奋——近乎乌托邦主义般的理想状态——那么确实还有一点点麻烦始终影响着交通枢纽日程、路线的理想以及通勤者或游客的现实状况发生了什么事会发生？即当服务未能准时或不运行时该怎么办呢？引入 GTFS-Realtime 标准来应对这一情况！ 

## 处理实际的时刻表

GTFS-Realtime是 GTFS核心部分的一个相对较新的增项，由一组利益相关方于2011年8月推出。它旨在解决“理论与实践中相遇”的永恒问题，即提供交通工具服务时刻表的实时更新形式向订阅数据的人士提供的现实时的更新内容方面提供服务支持其运作模式包括以下种类：任何已调度服务的更改路线、时间或取消操作都需实时通知用户；
- **Trip Updates:****乘车更新**：任何针对计划服务的更改路由、时间表或取消情况。  
-**Service Alerts :** 服务警报级别上的变化，例如站点位置移动了被关闭或是整批车辆因电力故障等问题导致停止运营的情况发生等等实例中出现的各种问题都要及时向用户提供预警通知;
- **Vehicle Positions:**在交通系统内车辆的定位信息以及（如果可获得的话）由这些车身本身或者相关的道路交通基础设施所提供当地拥挤状况的相关信息也都将被纳入该系统的实时更新范畴之内供用户随时查询参考.




谷歌是 GTFS-Realtime 演进过程中的关键参与者，这在所选数据格式上显而易见。GTFS-Realtime 并未沿用基础 GTFS 标准的逗号分隔格式，而是采用了谷歌的 Protocol Buffer 格式。这只是另一种以高效、平台无关的序列化和反序列化理念创建的数据格式——本质上是一种简洁的并行 XML 方案。在实践中，这意味着需要参考 Protocol Buffer 定义来确定文本/数据中的字段长度和属性。

## 探索 GTFS 示例

本章篇幅已颇长，即便介绍和探讨一个小型 GTFS 示例，也需涉及数百行 JavaScript、HTML 和 CSS 代码。这并非因为示例困难或复杂，而是因为它们需要处理本章已涉及的所有地理定位和地图渲染样式代码，以及大量用于处理 GTFS 数据来源和处理的文本处理代码与 I/O 代码。

相关内容足以独立成书，因此，为避免让本书陷入如此大的离题内容，我们将转而介绍一些出色的公开可用在线示例，供您下载和尽情探索，以深入了解 GTFS 及其可能性。

在线上一些值得注意且非常有用的 GTFS 开源示例包括：

-   **谷歌交通开发者页面**：作为 GTFS 社区的活跃成员，谷歌提供了丰富的在线示例。请将浏览器指向 https://developers.google.com/transit/gtfs/examples/display-to-users，获取大量示例和背景信息。
-   **One Busway 项目**：最初由普吉特海湾的开发者创立，http://developer.onebusaway.org 是 One Busway 项目的主页，该项目已扩展为面向全球 GTFS 开发者的倡议。
-   **社区项目**：例如 UlmApi.de 的实时地图，这是一个黑客马拉松项目在短短几小时内构建的、功能完备的基于 GTFS 的交通应用。完整项目详情可在 https://github.com/UlmApi/livemap 获取。

在图 10-5 中，您可以看到由 UlmApi.de 的安卓网页应用程序渲染的清晨乌尔姆市完整交通系统。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_187_0.png)

图 10-5. UlmApi.de 的黑客马拉松 GTFS 应用在安卓浏览器中的展示。

本着交通出行应用的真正精神，我们邀请您探索这些及其他 GTFS 网站，看看这段旅程将带您走向何方！

## 总结

在本章中，我们进一步探讨了面向安卓的基于位置的 Web 应用开发。我们的示例涵盖了使用谷歌流行的本地搜索网络服务，演示如何为行动敏捷的游客查找火车、地铁、渡轮及其他交通选择。我们只是初步触及了 GTFS 等交通数据馈送系统的应用潜力，但您现在已掌握足够知识，可以探索众多在线可用选项。我们希望本示例应用已展示了如何轻松地将基于手机的位置功能与基于云的服务相结合，以创建实用的混搭应用和非常易于开发的功能。

# 第 11 章：通过音频和视频突破极限

音频和视频是移动 Web 中最难涵盖的两个主题。虽然每项技术都能在很大程度上提升网站或应用的视觉和听觉吸引力，但移动内容创作者们往往会对这两项技术滥用有加。例如，我注意到移动端一种日益普遍的滥用形式是针对移动浏览器的音频广告。尽管音频和视频技术可能被错误使用或以令人厌烦的常规方式使用，但若运用得当，它们能发挥奇妙作用。

假设我们正在开发一款移动游戏应用，希望添加一些轻松循环的背景音乐来提升用户体验。我们可以利用安卓操作系统内置浏览器的 HTML5 功能，通过 `audio` 标签用几行代码轻松实现。此外，我们甚至可以使用少量 JavaScript 来操控音频元素。例如，我们可以实现按下按钮播放、停止或暂停音频等功能。

通过安卓的浏览器程序，我们还可以利用 HTML5 的 `video` 标签，以 h.264、MPEG-4 和 WebM 格式的视频来增强我们的 Web 应用。无论是 `audio` 标签还是 `video` 标签，只要运用得当，都能为它们所在的应用带来顶级用户体验，使其充满卓越感。

在本章中，我们将逐一探讨这些元素、它们的 API，以及在我们崭露头角的应用中使用这些新 HTML5 标签的优缺点。

## 移动 Web 应用的音频

几年前，如果您作为开发者想在 Web 应用中加入音频，选择几乎为零。几乎所有解决方案都涉及使用 Adobe Flash，并利用 Flash 作为中介将音频传输到用户的音频输入设备。虽然通过 `embed` 和 `object` 标签将音频添加到用户体验中是可能的，但大多数情况下，您得到的是一种相当受限且不可接受的用户体验，让最终用户——以及开发者——都渴望更多。

随着 HTML5 采用率的提升，在安卓中实现 HTML5 `audio` 标签时处理音频（尽管在某些罕见情况下仍有不便）总体上已变得顺畅。移动 Web 应用和游戏利用 `audio` 元素为项目带来背景音乐和音效的例子比比皆是，这有助于为用户创造更具沉浸感的探索场景。

不幸的是，就像 Web 开发领域的大多数事物一样，并非所有音频编解码器都是平等的。在移动端尤其如此。自 2010 年中期 Android 2.0 首次推出以来，谷歌的 Android 操作系统就一直在使用 HTML5 `audio` 标签，但它仅支持两种更流行的音频编解码器选择——MP3 和 AAC 音频格式。

### 使用 HTML5 audio 标签

使用 HTML5 `audio` 标签非常简单。看看清单 11–1 中的示例，我们向用户的页面添加了一个重复播放的音频循环。

清单 11–1. *HTML5 audio 元素的基本用法*

```
<audio autoplay="autoplay" controls="controls">
    <source src="audio/stairwell.ogg" type="audio/ogg" />
    <source src="audio/stairwell.mp3" type="audio/mpeg" />
    "Sorry, your browser does not support the audio element."
</audio>
```

`audio` 标签的基本用法与 HTML 领域的其他标签非常相似。声明 HTML `audio` 元素时，我们可以在文档中调用多个属性。让我们看看下面的一些属性：

-   **autoplay** ——如果调用此属性，音频元素将在其准备就绪并可用时立即播放。
-   **controls** ——确定是否向用户显示此音频元素的控件。
-   **loop** ——如果设置，此属性会告诉音频无限循环播放。就像那首永不结束的歌！
-   **preload** ——这决定音频元素是否会在文档加载时预加载到页面中。
-   **src** ——音频文件的 URL。

查看清单 11–1，我们还可以注意到 `audio` 标签还包含两个 `source` 标签。这些 `source` 标签各自拥有 `src` 属性，指向服务器上文件的 URL。使用多个标签实际上是一种巧妙的方法，可以编写一个适用于多种浏览器的 HTML 文档。您的浏览器（如果支持 HTML5 `audio` 标签）会逐一检查这些源编解码器，直到找到适合您浏览器的那个。如果成功找到合适的文件（即您提供了可在用户系统上播放的文件版本），它就会播放。如果没有，它将什么也不做。如果您因某种原因在较旧的、不显示 `audio` 标签的安卓设备上查看此页面，那么浏览器将完全忽略该元素，并显示预设的错误信息 *Sorry. Your browser does not support the audio element*，如图 11–1 所示。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_190_0.png)

**图 11–1.** *HTML5 audio 元素在设置了 'controls' 属性的安卓 Gingerbread 2.3 设备上。*

### 将音频集成到 "Who's That Tweet?" 中

在本书的第一个应用中，我们让人们猜测哪个 Twitter 账户发布了给定的推文。现在想象一下，我们想加入一些音频来安抚那些玩我们游戏的人的烦躁情绪。我们可以轻松地使用 `Audio` 标签，通过清单 11–2 中的代码来实现。



### 使用音频编解码器

如果你正在为 Android 设备开发应用程序，你会希望坚持使用以下三种在整个平台都可用的编解码器之一：MPEG-2 Audio Layer III (MP3)、*高级音频编码*（AAC）以及开源界备受喜爱的 Ogg。虽然每种编解码器都有其自身的优势，但大多数开发者通常只选择 MP3 和 Ogg，因为有大量免费的开源工具可用于将音频转换为这些格式。

#### MP3

MP3 音频格式被称**有损压缩**音频格式。有损压缩格式在多媒体领域非常流行，如果你以前使用过图形设计程序，如 Adobe Fireworks、Gimp 或 Adobe Photoshop，那么很可能你已经（宽松地）熟悉有损压缩了——这里没有双关的意思。

#### AAC

*高级音频编码*，也称为 AAC，是另一种新兴的音频格式。如果你曾经从 Apple iTunes 购买过音乐，那么你很可能购买的就是这种音频格式的音乐。

这种音频格式之所以受到开发者的欢迎，除了其音质明显优于竞争对手这一显而易见的事实外，还在于分发或流式传输 AAC 编码内容不需要任何许可或专利费用。请注意，这种许可仅适用于实际**编码**——你不能拿走不属于你的受版权保护的材料，将其编码为 AAC，然后在向全世界分发后对着律师哈哈大笑。好吧，我猜你可以笑，但这对你的案子没什么帮助！

#### Ogg

在我们征服 Android 设备上 HTML5 音频的旅程中，另一个后起之秀是我个人最喜欢的编解码器之一：**Ogg**。

这促进了 Ogg 被大多数浏览器采纳为默认的 HTML5 音频编解码器。如果你将音频编码为 Ogg 格式，很有可能它不仅能在 Android 设备上工作，还能在当今市场上的大量其他设备和浏览器上工作。

虽然 Ogg 像 MP3 和 AAC 一样是有损压缩格式，但 Ogg 背后的框架可以在市场上的几种无损音频格式中找到，如 OggPCM 和 FLAC。使用 Ogg，你可以随心所欲：**小巧的文件**或**庞大的无损文件**。一切皆有可能。

### 使用 Audacity 音频编辑器

我最喜欢的开源音频软件之一是 Audacity（http://audacity.sourceforge.net/）。这款免费的跨平台应用程序让你可以轻松导入多种不同格式的音频。使用 Audacity，你可以轻松拼接音频、剪切音频文件、录制现场音频、改变音频文件的音调和速度、为音轨添加噪音、降低音量过高的音轨，以及许多其他非常酷且有用的功能（见图 11–2）。

![img/8b0ff5e51ddb912cd941bb18cf27206a_193_0.png](img/8b0ff5e51ddb912cd941bb18cf27206a_193_0.png)

Figure 11–2. Audacity 1.3 Beta 编辑一个知识共享音频文件

每当我处理来自客户的音频，面对一个 512MB–1024MB 的大型 WAV 音频文件时，Audacity 始终是我的首选，用于修剪掉我不需要的音频部分，或将其转换为更小、更易于管理的格式。

由于本书仅旨在涵盖为 Android 移动设备设计的初学者方面，我不会深入探讨 Audacity 的所有功能。相反，我将介绍一些基础知识，例如将一种音频格式导出为另一种。

如果你想要将文件转换为 MP3 格式，那么你需要下载 LAME MP3 库。你可以通过在 Audacity 中进入首选项来轻松完成此操作。

1.  转到 **Edit** 菜单并选择 **Properties**。
2.  在 **Properties** 窗口的左侧部分选择 **Libraries** 选项，如图 11–3 所示。

![img/8b0ff5e51ddb912cd941bb18cf27206a_194_0.png](img/8b0ff5e51ddb912cd941bb18cf27206a_194_0.png)

Figure 11–3. 查看 Audacity 1.3 Beta 首选项对话框。

3.  在那里，你可以选择将 Audacity 指向你的 LAME 库，如果它已经安装在你的计算机上。如果你尚未安装 LAME 库，请继续执行步骤 4。
4.  单击 **Download** 按钮，这将带你到一个可以下载最新最好版本的 LAME MP3 库的网站，如图 11–4 所示。

![img/8b0ff5e51ddb912cd941bb18cf27206a_195_0.png](img/8b0ff5e51ddb912cd941bb18cf27206a_195_0.png)

5.  一旦下载了库并将其解压到你的硬盘，你就完全可以录制和导出音频为 MP3 格式了。

如果你查看本节前面的图 11-2，你会看到我们正在处理一个名为 stairwell.ogg 的知识共享音频文件。我们要做的是将这个 Ogg 文件快速转换为 MP3 文件。具体操作如下：

1.  单击菜单栏中的 **File**，然后选择 **Export**，如图 11–5 所示。

![img/8b0ff5e51ddb912cd941bb18cf27206a_196_0.png](img/8b0ff5e51ddb912cd941bb18cf27206a_196_0.png)

**Figure 11–5.** *在 Audacity 1.3 Beta 的 File 菜单中选择 Export。*

2.  在下拉框中，确保将文件格式更改为 MP3，而不是音频文件的当前格式。

3.  选择你要保存文件的位置，单击 **Save** 按钮，就完成了！

看吧，我不是承诺过这很简单吗？现在你知道如何快速将音频从一种格式转换为另一种格式了，是时候进入通过非常方便的 HTML5 Audio Data API 操作音频的有趣部分了。

### Audio Data API

使用 Audio Data API，开发者可以以几年前还不可能的方式与音频数据交互。使用 JavaScript 和一些 HTML，你可以轻松创建自己的控件来与音频数据交互，如我们在清单 11–3 中所见。

看看下面的例子，你可以看到我们在清单 11–1 的基础上进行了扩展，并添加了一些新定制的控件来播放和停止音频。

**Listing 11–3.** *HTML5 Audio Data API 更深入的了解*

```html
<audio id="audioDemo">
    <source src="audio/stairwell.ogg" type="audio/ogg" />
    <source src="audio/stairwell.mp3" type="audio/mpeg" />
    "Sorry, your browser does not support the audio element."
</audio>

<button id="play">Play</button>
<button id="pause">Pause</button>

<script type="text/javascript">
    var audio = document.getElementById('audioDemo');
    var playButton = document.getElementById('play');
    var pauseButton = document.getElementById('pause');

    playButton.addEventListener('click', function() {
        audio.play();
    }, false);

    stopButton.addEventListener('click', function() {
        audio.pause();
    }, false);
</script>
```

当你在浏览器中运行此代码时，你可能首先注意到的是页面上完全没有音频控件，除了我们添加的两个按钮，其 ID 分别为 play 和 pause。这些按钮虽然不如图 11–6 中所示的那么美观，但将是我们操作页面上音频的唯一方式。

![img/8b0ff5e51ddb912cd941bb18cf27206a_197_0.png](img/8b0ff5e51ddb912cd941bb18cf27206a_197_0.png)

**Figure 11–6.** *在 Android 2.3.4 Gingerbread 设备上加载我们的 HTML5 音频演示文档*



现在，如果你查看清单 11-3 的底部，在 JavaScript 中，我们可以探究真正的魔法发生在哪里。在这里，我们声明了 audio、playButton 和 pauseButton 的变量。接着，我们为这些按钮分别添加了事件监听器，以便当用户点击这些按钮时，我们触发一些代码来播放或停止音频流。如果我们愿意，还可以添加额外的音量控制按钮，其形式与上面的代码类似，但会调用 audio.volume=X，其中 X 是 0 到 1 之间的数字，表示音量级别的百分比（因此如果你想将音量提高 10%，你的代码应写为 audio.volume = audio.volume + .1）。

你也不仅仅只能随意暂停你的音频文件。使用 HTML5 Audio Data API，你可以轻松控制页面中播放或欣赏音频的许多方面，例如操作音频文件的音量、分析曲目中的每分钟节拍数、结合 canvas 的强大功能与 Audio Data API 创建你自己的可听音调，以及更多。

## 为移动应用程序添加视频

既然我们已经介绍了精彩的音频世界，现在是时候用 HTML5 视频来探索互联网多媒体中视觉上吸引人的一面了。video 标签是未来几年中出现的又一个新 HTML5 元素。它的创建是为了让开发者的工作更轻松，并使我们摆脱对 Adobe Flash 的依赖。不幸的是，没有人能够真正就视频标准达成一致，而且有这么多的障碍、编解码器、许可协议和专利挡在我们的道路上，我们不太可能很快就更接近制定出一种用于浏览器消费的通用视频格式。

好消息是，由于我们只专注于基于 Android 的设备，我们不必处理与桌面计算世界中的 HTML5 视频相关的许多令人沮丧的问题。在这里，这非常简单。有一些视频编解码器可以在 Android 浏览器中工作，只要你坚持其中一种或全部使用它们，你就能够为你的移动用户提供更丰富的多媒体体验。

### 使用 HTML5 video 标签

调用 HTML5 video 标签就像我们之前在本章讨论的 audio 标签一样简单。查看清单 11-3，了解我们如何使用几行代码轻松地向用户显示视频。

清单 11-3. *HTML5 video 元素的基本用法*

```
<video width="320" height="240" controls="controls" poster="video/big_buck_b TCP"><source src="video/big_buck_bunny.mov" type="video/mp4" /><source src="video/big_buck_bunny.ogg" type="video/ogg" /><source src="video/big_buck_bunny.webm" type="video/webm" />
    Sorry! Unfortunately your browser does not support the video tag
</video>
```

在这个例子中，我们只是调用一个视频文件，并将视频容器的宽度设置为 320 像素，高度设置为 240 像素。我们还告诉视频显示其控件，以便用户可以播放、暂停、停止和操作视频的音量。你可以在图 11-7 中看到这在移动设备上的样子。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_199_0.png)

图 11-7. *在 Android 2.3.4 Gingerbread 设备上观看 HTML5 视频*

你还会注意到 video 标签与 audio 标签的不同之处在于具有不同的属性。最突出的一个是 `poster` 属性，它让我们可以添加一个截图（或任何其他我们拥有的图像）来代表即将播放的视频。这对于移动设备来说非常棒，因为当你在 Android 设备上播放视频时，就像在桌面计算机上使用多年后的期望那样，不是让视频在浏览器中播放，Android 设备会将视频流传递给其内置的视频播放器，由它来为你播放视频。

虽然这个功能有趣且方便，但它完全消除了人们使用 Video Data API 的许多原因，因为它在我们的页面之外播放视频——在一个专用的视频应用程序中。这破坏了用户体验，并阻止我们控制用户观看视频时看到的确切内容。

稍后，我们将给出一个类似于我们上面使用音频 API 的视频示例。然而，我们应该注意，虽然你可以用 Video Data API 做一些很酷的事情，但很多东西往往超出了大多数人的需求。以下是基础内容；完整的 API 可以在 www.w3.org/2010/05/video/mediaevents.html 参考。现在让我们看看在开发使用视频的下一个移动 Web 应用程序时可以使用的一些最有用的属性！

- height–控制播放视频的高度
- width–控制播放视频的宽度
- preload—如果设置，将在页面加载时预加载视频
- autoplay—如果设置，将在视频准备好时自动播放
- loop—如果设置，将无限循环播放视频
- controls—如果设置，将向用户显示控制视频的控件
- src—指向视频文件来源的 URL

### 编解码器

就像我们对音频所做的那样，视频必须编码成原生 Android Web 浏览器支持的几种格式之一（稍后提及）。编码视频可能比音频更棘手一些，因为你正在编码两件事——即音频和视频！我们将介绍你可以使用的格式，并讨论如何轻松地在它们之间移动音频和视频。

#### h.264/MPEG-4

多年来，MPEG-4 已成为互联网和我们日常消费者生活中视频编码的首要标准之一，尤其是在高清视频方面。最近，MPEG-4 通过社交视频分享网站（如 YouTube 和 Vimeo）的兴起进入公众意识，这些网站允许用户以这种格式上传视频。MPEG-4 的当前版本正式称为 h.264/MPEG-4 AVC，是高质量视频压缩的标准，例如蓝光光盘上的视频。

#### Ogg Theora

Theora 是由负责维护 Ogg 音频编解码器的同一家基金会 Xiph.Org Foundation 创建的免费开源有损视频压缩格式。虽然 Theora 本身基于专有的视频编解码器



应用程序的右侧是为您呈现诸多精彩功能的地方。在这里，您可以从各种预配置的视频设置中进行选择，因此您只需输入视频源，决定保存视频的位置，选择一项您喜欢的设置，然后开始编码即可。

如果您查看图11-9，您还会注意到视频容器选项旁边有两个小复选框。这两个复选框——“Web优化”和“iPod 5G支持”——是在编码视频时您可能想要尝试的两个选项。在某些情况下，我发现这些设置有助于我创建更高质量的视频文件以供浏览器使用。然而，在其他时候，它们只会给我带来烦恼。这一切都取决于您用作源素材的视频文件。视频可能很棘手，尤其是在将其从一种格式转码为另一种格式时。最终，通常必须“尝试”各种设置才能获得最佳效果。如果您的视频文件很大（因此需要更多时间转码），您可以考虑分割出一小段来进行试验。一旦您找到了设置和选项的正确组合，就可以转换完整版本的视频，从而节省一些时间。

![图11-9. 在Windows 7版Handbrake中设置视频源、目标位置和视频容器设置](img/8b0ff5e51ddb912cd941bb18cf27206a_202_0.png)

![图11-10. 为我们的视频选择iPhone & iPod Touch预设配置设置](img/8b0ff5e51ddb912cd941bb18cf27206a_203_0.png)

最后，Handbrake中可供您使用的选项数量可能有点让人不知所措。如果您正在寻找更简单的东西，您可能需要查看更面向消费者的（即，为非开发人员或高级用户设计的）解决方案，例如DoubleTwist (www.doubletwist.com) 和Videora (www.videora.com)。两者都可以将视频转换为可在移动设备上查看的格式，几乎不需要费力或自定义。

既然我们已经介绍了一些关于创建、显示和使用您自己的音频和视频的基础信息，我们将介绍一些您可以通过与程序员可用的不同API对接来扩展应用程序的领域。

## 自行探索：音乐服务API

许多网络服务通过API（应用程序编程接口）向程序员提供对其平台的访问。在本节中，我们将讨论两个流行的应用程序及其提供的API。您可能会发现，将您的应用程序与这些服务之一集成，不仅可以访问一些很酷的工具——还能为该服务的用户增加对您应用程序的吸引力。

### 将曲目“Scrobble”到Last.fm

Last.fm是一项旨在不仅向您的计算机或手机传输音乐，而且智能地了解您喜好的服务。它实现这一点的一种方式是允许多个设备（即安装了Last.fm客户端的iOS设备和安卓手机）将收听的曲目信息发送给Last.fm，Last.fm将此过程称为“scrobbling”。例如，我使用Google Music通过浏览器收听我的音乐收藏。通过使用一个将我的曲目scrobble到Last.fm的Chrome扩展程序，我可以在之后查看我的收听行为，而Last.fm也知道我喜欢听什么样的音乐（图11-11）。

![图11-11. 我的Last.fm最近收听的曲目](img/8b0ff5e51ddb912cd941bb18cf27206a_204_0.png)

一旦曲目被记录下来，它就会告知Last.fm我的收听习惯。这对于告诉Last.fm向我推荐什么很有用，并且它允许我找到我可能喜欢的新音乐。

假设我们想在我们的新应用MusicDiscovery中向用户展示音乐片段。假设MusicDiscovery播放45秒的歌曲片段给用户听。用户对歌曲的喜欢程度进行评分，如果评分足够高，我们就将其scrobble到Last.fm，以便它可以记录他们的喜好。我们该如何做呢？

首先，我们需要了解Last.fm API。大多数提供API访问的网络服务都会在其网站标有“for developers”或“API access”的部分清晰地说明如何使用它。Last.fm在其主页底部包含一个“API”链接，该链接会带您进入API主页（图11-12）。

![图11-12. Last.fm网络服务页面](img/8b0ff5e51ddb912cd941bb18cf27206a_205_0.png)

查看Last.fm API信息，这似乎是一个两步过程。首先，必须申请成为开发者（这涉及告诉Last.fm您计划如何使用他们的数据，即商业或非商业用途），并填写一些关于您应用程序的基本信息。一旦这些处理完毕，您就可以探索使用他们的API。

API简介页面列出了一些基本信息，包括API根URL。这是我们发送信息的网络地址。这些请求大多数将使用AJAX，这是一项我们将在下一章详细讨论的技术。浏览文档，我们找到了如何向Last.fm发送数据的示例。

正如我们在图11-13中所看到的，我们对Last.fm API的请求采用特殊格式的URL或HTTP POST请求的形式。然后，Last.fm API使用XML返回响应。

#### Last.fm网络服务

API根URL位于 [http://ws.audioscrobbler.com/2.0/](http://ws.audioscrobbler.com/2.0/)

一般来说，您将向根URL发送一个表示为'package.method'的method参数以及特定于方法的参数。所有调用都需要以下参数：

- **api_key**: Last.fm API密钥。
- **method**: 一个表示为 *package.method* 的API方法，对应于last.fm文档中列出的API方法名称。

例如：

```
http://ws.audioscrobbler.com/2.0/?method=artist.getSimilar&api_key=xxx...
```

如果您要访问的是*写入*服务，则需要以HTTP POST请求的形式提交请求。所有POST请求都应发送到根URL：

```
http://ws.audioscrobbler.com/2.0/
```

所有参数（包括'method'）都应在POST请求体中发送。为了执行写入请求，您需要使用API对用户进行身份验证。有关更多信息，请参见[身份验证](http://authentication)。

#### REST响应

响应将包装在一个lfm状态节点中

```
<lfm status="$status">
    ...
</lfm>
```

其中**$status**是**ok**或**failed**。如果状态为failed，您将获得一个错误代码和消息。您可以通过在方法调用中发送一个**raw=true**参数来从响应中去除状态包装器。

**图11-13.** *Last.fm API请求文档*

现在我们大致了解了信息如何在我们的应用程序和Last.fm之间来回传递，我们可以开始探索scrobbling功能。Last.fm的scrobbling文档（www.last.fm/api/scrobbling，图11-14）详细介绍了整个过程，包括使用哪些API调用（或函数），以及在发送scrobble请求时使用哪些标准。

![图11-14. Scrobbling过程](img/8b0ff5e51ddb912cd941bb18cf27206a_207_0.png)

现在我们已经掌握了所有要素，我们需要做的就是编写适当的JavaScript代码，获取用户当前评分的音乐，在Last.fm的目录中查找它，并发送scrobble请求。在这里，您可以展示您的编程能力并解决它。在此过程中，请务必查看Last.fm丰富的查询和记录功能的其余部分。您不仅可以增强Last.fm用户的用户体验，还可以使用Last.fm数据为您自己不使用Last.fm的用户增强体验！

## 利用Amazon产品广告API的力量

Amazon.com大约在15年前以书店起家。现在他们已经发展成为一家庞大的零售巨头，提供从书籍到云计算服务器等各种产品。最近，他们的音乐产品扩展了很多，在应用程序中展示音乐或视频的开发者可能希望通过Amazon提供购买这些资源的链接。

Amazon产品广告API (https://affiliate-program.amazon.com/gp/advertising/api/detail/main.html，图11-15) 是一个庞大的网站，因此我们在这里只能重点介绍其主要功能。您确实可以花费数天时间探索使用Amazon数据所能做的一切，所有目标都是通过您的应用程序提供Amazon产品销售来推动收入。

![图11-15. Amazon产品广告API](img/8b0ff5e51ddb912cd941bb18cf27206a_208_0.png)

Amazon不仅提供其API的文档，还提供开发者论坛，您可以在其中向其他开发者寻求帮助，甚至提供代码示例，这些可以帮助您快速上手。

快速搜索代码数据库会发现一段非常有趣的代码，适用于任何想要构建展示特定艺术家应用程序的人。假设您在一个乐队中，并想为您的乐队构建一个应用程序。您决定构建一个Web应用程序，因为它可以轻松地在每个人的智能手机上运行，并且您将音乐会录音、演示曲目和专辑存储在Amazon的S3云存储中。我们如何向粉丝销售这些？有一个名为iObjects的演示（http://j.mp/iobjects，图11-16）。

# 第11章：突破音频与视频的极限

"mp3" > iObjects 使用亚马逊FPS将您的Amazon S3对象货币化

> **社区贡献软件**
* 亚马逊云服务提供这些软件包的链接，以方便我们的客户，但"@AWS"账号以外的作者所编写的软件未经AWS审核或筛查。
* 请在使用前审查此软件，以确保其满足您的需求。

一段PHP代码示例，用于列出Amazon S3中的对象，并使用亚马逊FPS服务将其货币化。您的Amazon S3对象可以是图片、播客、视频、文档等任何内容

### 详细信息

| 提交者： | Jinesh@AWS |
|---|---|
| 使用的AWS产品： | Amazon FPS, Amazon S3 |
| 语言： | PHP |
| 许可证： | Apache License 2.0 |
| 创建时间： | 2008年2月29日 格林尼治标准时间凌晨3:18 |
| 最后更新： | 2009年2月5日 格林尼治标准时间凌晨3:25 |

### 关于本示例

* 此代码示例简单演示了如何列出您的Amazon S3对象并使用Amazon FPS将其货币化
* 它实现了SingleUse功能，并演示了如何进行Pay调用
* 使用Amazon FPS PHP REST库

### 使用场景

* 您是摄影师，在Amazon S3上存储了大量图片/照片，希望将其出售给朋友
* 您是天生的艺术家，希望在Facebook上向朋友出售您的MP3铃声

*图11-16. iObjects代码示例*

虽然这比我们在上一节中讨论的Last.fm API要复杂得多，但它确实可以展示在应用程序中使用API的强大功能。现在您无需担心材料的支付问题（因为亚马逊灵活支付系统（FPS）可以处理此事），您可以轻松通过亚马逊在您的应用中提供产品，而您的朋友们很可能熟悉并经常使用亚马逊！

正如我们所见，使用亚马逊或Last.fm等服务的API不仅可以为您的应用程序增加交互性，还可以带来新的收入来源和创新方式。您的乐队（或客户的乐队）肯定会在用户能够在音乐会现场下载歌曲时脱颖而出，而您将成为这一切实现的开发英雄！

## 小结

由于需要支持的手机型号和操作系统数量有限，在移动HTML5前端处理音频和视频可能相当轻松。但是，正如本章开头所述，这两种技术都很容易被滥用，如果使用不当，很快就会对您产生不利影响。在本章中，希望我已经为您提供了必要的工具，让您能够利用这些技术为自己带来益处。

在音频和视频转换及处理方面，我们就可用工具而言甚至还没有触及皮毛。市面上优质的音频和视频工具实在太多——我们可能可以写整整一本书来专门讨论它们。您不必使用我在本章中推荐的工具，我鼓励您进行一些研究，找到最适合您的解决方案。

## 用AJAX增强用户体验

我们已经读完了这本书的大部分内容，但还没有明确提到一个让普通用户、尤其是移动用户长期困扰的问题： dreaded刷新！

为什么令人恐惧？因为在移动世界中，正如我们所了解的，速度就是一切。移动用户最不愿意做的事情就是重新加载整个网页。即使页面的"较重"部分（如图片、字体等）已缓存在用户的手机上，手机浏览器仍然需要将它们重新加载到浏览器中。这需要一定的时间、处理能力、电池电量以及用户的耐心。幸好有一系列技术可以帮助我们，这就是AJAX。

### 什么是AJAX？

AJAX代表异步JavaScript和XML。让我们拆解这个名称。第一个词"异步"（Asynchronous）乍一听可能有点令人生畏，但它是AJAX特殊之处的关键所在。

### 异步？

大多数网页的编程方式要求通信遵循发送/接收/显示的顺序。用户按下Web应用上的按钮，页面将所需信息发送到服务器，服务器返回一些响应，应用将新页面显示出来。如此往复，直到用户完成使用该应用。每次用户与应用交互时，页面都会完全刷新。对某些人来说，这就是烦人的定义。

异步传输指的是我们可以将这个链条简化为发送/接收/显示/发送/接收/发送/接收，等等，而不需要在每一轮中包含显示部分。换句话说，我们可以在不加载新页面的情况下发送和接收数据。异步调用就是我们通过这种替代方法向Web服务器发出的请求。要了解这一点，我们只需在手机上的Google搜索引擎中体验一下。我们从空白搜索页面开始，如图12-1所示。

**图12-1.** *Google搜索主页*

假设现在是一大早，我想开始我的一天，听一首配有歌曲所讲述事件图片的精彩歌曲。我可能会开始输入歌曲名称，如图12-2所示，而在我输入的同时，Google正在使用异步调用试图找出我在寻找什么。当我打字时，它在不刷新页面的情况下对照中央数据库检查每个字母。然后它在搜索栏下方显示这些建议。

**图12-2.** *开始我的搜索*

在某个时刻，大约在图12-3时，建议与我正在寻找的完整短语匹配，我可以简单地点击它。

**图12-3.** *当我输入更多内容时，网页会尝试填充可能的查询。有趣的是，Android操作系统也在试图弄清楚我在写什么——就好像它们都在试图读懂我的心思！*

基本上，Google已经能够预测我在寻找什么，并为我提供直接访问这些搜索列表的快捷方式。当我点击符合我想要的建议时，它会将我带到图12-4中显示的搜索结果。

**图12-4.** *啊，我的结果——现在我可以收听我一直在搜索的flash视频了*

在Google在搜索页面上推出这些异步调用之前，用户需要在搜索框中输入完整查询，按下"搜索"，然后等待屏幕重新加载。如果查询中有错误，用户在新页面加载并由Google指出之前是不知道的。这占用了用户的时间（通过不必要的页面加载）和Google的带宽。最近，Google将这只"帮助之手"更进了一步，将整个搜索异步运行——您可以输入查询，逐字逐句地，搜索结果在同一浏览器窗口中更新。

### 那么JavaScript和XML呢？

AJAX在技术上可以与任何客户端编程语言配合使用（客户端语言，如JavaScript，在用户的浏览器中处理。服务器端语言，如PHP，在Web服务器上处理）。然而，JavaScript被主要使用，因为它已成为客户端语言的通用语。XML参与其中是因为它已经变成了移动数据的简单易懂方式。虽然您可以将其他技术混入AJAX的盛宴中，但在我们的示例中，我们将坚持使用JavaScript和XML。

现在我们已经确定了AJAX是什么，让我们谈谈一些巧妙的方式，可以将其融入一些非常简单的应用中。我们将从一个每日一词示例开始，然后转向稍微复杂一些的内容，引用Web服务和我们自己的本地数据库。

### AJAX每日一词

最近有报道称，2011年的"年度词汇"是"pragmatic"（务实的）。这是因为一个提供词典服务的网站发现它是该年度被查找次数最多的词，因此将其加冕为赢家。也许您看到这里会想，"我一直想知道'pragmatic'是什么意思"（或者也许，"什么样的白痴会不知道'pragmatic'是什么意思？！？"），并想知道为什么没有更多的Web应用为我们带来这样的内容。好吧，今天是您的幸运日，因为您即将编写一个这样的应用。

对于每日一词应用，我们将创建一个相当基础的机制来提供上述词汇。在本章后面，我们将讨论如何使用AJAX从数据库或Web服务中提取信息，但现在我们将使用一个好的、老式的纯文本文件。恰如其分地命名为`word.txt`：

**代码清单12-1.** *word.txt*

```
<em>Pragmatic</em>: relating to matters of fact or practical affairs. <i>-<A
HREF=http://www.merriam-webster.com/dictionary/pragmatic>Merriam-Webster.com</A></i>
```

文件`word.txt`中包含一些HTML片段（在这种情况下，我们使用的是简单的样式标签，不过我们也可以使用CSS主题的div语句），如果我们在Web浏览器中加载它（图12-5），我们将看到它以纯文本形式显示：

**图12-5.** *每日一词word.txt文件*

接下来，我要构建一个HTML页面，当用户按下按钮时会加载每日一词。从代码角度来看，它将类似于代码清单12-2。我们将逐步介绍这个示例。

**代码清单12-2.** *word.html，第1部分：加载单词的初始JavaScript函数*

```
<html>
<head>
<meta content="text/html; charset=ISO-8859-1"
http-equiv="content-type">
<title>Word of the Day</title>
<script type="text/javascript">
function loadword(){
```



### 好了，我们已经准备就绪并开始运行

我们首先创建了一个标准HTML页面的顶部结构，然后启动了一个名为`loadword`的新JavaScript函数，这个函数将负责页面的大部分主要工作。在这个函数内部，我们首先需要判断使用的是现代浏览器（比如近五年发布的Firefox、Safari、Opera、Chrome或较新版本的Internet Explorer）还是旧版的Microsoft浏览器（Internet Explorer 5或6）。原因很简单：旧版的Microsoft浏览器不知道`XMLHttpRequest()`对象是什么！对于它们，我们会请求创建一个ActiveX对象，以提供相同的功能。这只是对Microsoft过去编码浏览器方式的一种有趣的妥协。让我们继续看清单12-3中的页面JavaScript代码。

#### 清单12-3：word.html，第二部分：JavaScript的onreadystatechange函数和JavaScript代码块的结尾

现在我们有了请求对象，恰当地命名为“request”，我们可以让它执行一些操作了。这段代码的下一部分写得稍微“颠倒”了一些，因为写在顶部的代码实际上会在写在底部的代码之后执行。这是因为AJAX的核心——XMLHttpRequest对象——有一个名为`onreadystatechange`的特殊函数。任何时候，我们发起并后台处理的请求，无论是按预期执行还是发生意外，都会触发这个函数。本质上，这个函数就是我们放置“如何处理返回数据”代码的地方。你可以把这里的代码想象成“代课老师的指示”。你可能还记得，作为一个敏锐的学生，当你的老师缺席时，他或她会为代课老师留下指示，可能放在一个特殊的文件夹里。你的`onreadystatechange`函数就充当这些指示，告诉计算机（这里指JavaScript引擎）当你不在场但有事情发生时该怎么做。大多数时候，这些指示与我们之前编写的内容相似（这里指“如果请求处理成功，就在屏幕上显示它”）。我们也可以包含针对“最坏情况”的指示，比如当请求无法完成或抛出错误时。

# 第12章：使用AJAX提升用户体验

在这个函数中，我们首先检查请求的`readyState`和`status`。前者可以返回五个不同的数字，对应于请求在处理过程中的不同阶段：

+   - **0** 表示请求尚未开始。这是新请求在发送之前的状态。
+   - **1** 表示与服务器的连接已经初始化。本质上，管道已经打开，数据开始流动。
+   - **2 或 3** 分别表示请求已发送和正在处理。此时，你的代码所能做的就是等待（或者如果你愿意，可以显示一个“加载中”的图形）。
+   - **4** 表示请求已完成并可供代码处理。你现在可以对这些信息做任何你想做的事情。我们只在`readyState`达到4时才更改页面上的文本。

我们也关心`status`，它可以报告200（表示“OK”）或404（表示“未找到”）。因此，清单12-3的第二行代码可以翻译为：“只有在请求准备就绪且处理成功时才执行此操作！”接着，只需一行代码就可以将省略号或文本占位符（见清单12-4）替换为请求返回的文本。

完成清单12-3，我们创建并发送了请求。以`request.open`开头的行调用了一个函数，该函数指定了我们要检索的内容以及执行的速度。*在这个例子中，这是一个非常简单的请求——我们只是获取数据，没有发送任何需要服务器解析的数据。我们将使用“GET”方法而不是“POST”，因为它更快；我们将请求`"word.txt"`，并将异步设置为“true”，因为我们希望响应在后台进行，允许脚本继续运行。关于为什么可能将其设置为false，以及GET与POST方法的更多细节，请参阅本章末尾的“AJAX注意事项”部分。*

最后，我们只需调用`request.send()`来触发我们的请求。一旦收到请求返回，XMLHttpRequest对象就会触发我们的`onreadystatechange`函数并更改网页中的行。

#### 清单12-4：word.html，第三部分：页面的其余部分，包含简单的body部分、文本以及‘theword’ div

```markdown
</head>
<body>
<span style="font-family: Helvetica,Arial,sans-serif;">Get Today's Word Of The Day<br>
<div id="theword">
<h2>...</h2>
</div>
<button type="button" onclick="loadword()">Get The Word!</button>
```

在Android网页浏览器上查看时，页面加载并显示默认状态（见图12-6）。

**图12-6。** *“每日一词”示例的初始页面*  
<img src="img/8b0ff5e51ddb912cd941bb18cf27206a_219_0.png" alt="图12-6" />

现在，当用户点击“获取单词！”按钮时，省略号被替换为从`word.txt`中提取的实际每日单词（见图12-7）。你还会注意到文本似乎缩小了一点——这是因为AJAX请求占据了`theword` `<div>`部分的全部，包括通常会提供更多间距的`<h2>`标签。我这样做是为了指出，在考虑AJAX请求时，标签的嵌套很重要。将`<h2>`放在`<div>`外部可以保留间距。*

**图12-7。** *单词现已放入页面中，无需页面重新加载！*  
<img src="img/8b0ff5e51ddb912cd941bb18cf27206a_219_1.png" alt="图12-7" />

成功！我们通过调用服务器更改了页面内容，而无需实际重新加载页面。更妙的是，如果用户点击浏览器的“刷新”，我们将避免出现类似图12-8中那样的丑陋错误，因为我们实际上没有向服务器发送任何“POST”数据（在传统意义上）。有关POST数据的更多信息，请参阅本章末尾的“AJAX注意事项”部分。

# 第12章：使用AJAX提升用户体验  
<img src="img/8b0ff5e51ddb912cd941bb18cf27206a_220_0.png" alt="图12-8" />  

*图12-8。Android确认重新加载对话框*

现在，“每日一词”的基础知识已经完成，我们可以继续让它变得更漂亮一些（即使用之前提到的漂亮的CSS方案）。不过，就我们的目的而言，你现在应该已经很好地理解了，平面文本文件不仅可以如前面章节所示通过PHP包含，现在还可以通过AJAX包含。*我们的下一站？网络服务、XML和JSON的奇妙世界。*

## 我的新闻！

我们的下一个示例将调用几个网络服务，为我们带来不会存储在我们自己设备上的内容。我们还需要从一种稍微以自我为中心的视角来看待这个世界，但嘿，这是成为程序员所必需的！*让我们想象一下，我们有一些喜欢访问的网站，我们希望我们的应用程序显示来自这些网站的最新新闻。为此，我们需要将这些网站的RSS源汇集在一起，合并它们，然后显示出来。我们希望列表能够在我们的页面上实时更新，无需用户干预。听起来很复杂？**并不真的——只要你懂一些技巧！**

### 首先：创建一个管道

Yahoo! Pipes是我最喜欢的网络服务之一（图12-9，http://pipes.yahoo.com），它并没有被大多数博客或网站大量报道。*但它提供的服务非常棒——它可以将RSS源和其他数据拼接在一起，并以你选择的易于使用的格式提供。

<img src="img/8b0ff5e51ddb912cd941bb18cf27206a_221_0.png" alt="" />  

虽然其他网站允许你将事物连接起来（想到Yahoo!旗下的另一个网站Dapper，网址为http://open.dapper.net/，以及ifttt（If This Then That），网址为http://ifttt.com），但Pipes提供了更可定制的“输出”，因此我们将在这个示例中使用它。要开始使用，点击“Create a pipe”加载管道编辑器，如图12-10所示。*管道编辑器允许你将一系列模块（在左侧）组织成逻辑规则结构。每个管道以一个或多个输入开始，然后使用模块对它们进行操作（即更改数据或合并数据），然后以多种形式输出结果。*



## 第12章：用AJAX提升用户体验

图12-10。*雅虎Pipes编辑器*

左侧你可以找到一系列模块，可以拖拽到Pipes界面中。这些模块可以相互连接以执行你想要的操作。我将使用三个模块——获取站点Feed、联合和截断——来汇集三个网站的Feed，将它们合并，然后在五个项目后截断输出（图12-11）。

-   1. 获取站点Feed接收网站的RSS Feed URL。在这个例子中，我将获取三个不同网站的RSS Feed并将它们链接起来。你会注意到在图12-11中，我有三个“获取站点Feed”模块。

-   2. 联合简单地将最多五个输入合并为一个Feed。这里联合操作合并了我输入的三个Feed。如果需要，我可以使用多个联合，并通过将多个管道“联合”到另一个联合中等方式来处理超过五个的管道。

-   3. 截断告诉Pipes我只想输出五个项目。这有助于加快响应时间，因为Pipes只需要导出少量项目，而不是多个Feed可能提供的数十或数百个项目。在这里，它是我连接到Pipes输出模块之前的最后一个操作。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_223_0.png)

**图12-11。** *完成的管道*

在调试器窗口（图12-12）中，我可以看到整个管道或沿途各个部分的输出结果。以下输出（图12-12）是当我点击“管道输出”时显示的。如果我点击联合操作，我会看到所有的Feed项目，而不仅仅是截断命令之后显示的五个。这种中间级别的调试在调试管道时非常有用，可以查看哪个组件可能导致问题。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_223_1.png)

**图12-12。** *我的管道的完整输出，我们已在五个项目后截断*

完成后，点击“保存”并给你的管道命名。然后点击“运行管道”来查看输出（图12-13）。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_224_0.png)

**图12-13。** *我创建的书籍管道*

### 书籍管道

点击添加描述

管道网址：http://pipes.yahoo.com/pipes/pipe.info?_id=0a1f972788e5ee484b335cb892fc85be (编辑)

编辑源码 | 删除 | 发布 | 克隆

![](img/8b0ff5e51ddb912cd941bb18cf27206a_224_0.png)

你会注意到雅虎Pipes为我提供了如何访问管道的选项。我可以将其作为RSS Feed本身访问，或者我可以获取其JSON结果输出。在“更多选项”下，我还可以配置通过电子邮件或PHP获取结果。对于这个例子，我想要以JSON格式获取结果。你会记得我们在本书前面第2章和第3章的应用程序中使用过JSON。在这里，我们再次使用它来获取管道的输出。点击JSON按钮会给我一个相当难看的满是内容的屏幕，但我真正想要记住的是那个URL。它看起来像http://pipes.yahoo.com/pipes/pipe.run?_id=0a1f972788e5ee484b335cb892fc85be&_render=json，并且可以通过我的AJAX网页调用。

### 第二步：获取输出并显示它！

我们将修改我们的每日一词示例来获取JSON输出并显示它。虽然有更简单的方法可以做到这一点（最著名的是使用getJSON函数和循环列表项），但清单12-5中的代码稍微详细一些，这使得更容易准确地看到我们正在做什么来解析每个项目。稍后，作为你JavaScript技能的展示，如果你愿意，可以使用getJSON重写这段代码。

**清单12-5。** *mynews.html*

```html
<html>
<head>
<meta content="text/html; charset=ISO-8859-1"
http-equiv="content-type">
<title>My News</title>
<script type="text/javascript" src="jquery-1.7.1.min.js"></script>
<script type="text/javascript">
function loadnews() {
    if (window.XMLHttpRequest) {
        // Modern browsers use this type of request
        request = new XMLHttpRequest();
    } else {
        // Old Microsoft Browsers use this type!
        request = new ActiveXObject("Microsoft.XMLHTTP");
    }

    request.onreadystatechange=function() {
        if ( request.readyState == 4 && request.status == 200) {
            var resp = jQuery.parseJSON(request.responseText);
            var lister = "<ul>";
            lister += "<li><A HREF=" + resp.value.items[0].href + ">" +
            resp.value.items[0].title + "</li>";
            lister += "<li><A HREF=" + resp.value.items[1].href + ">" + resp.value.items[1].title +
            "</li>";
                lister += "<li><A HREF=" + resp.value.items[2].href + ">" +
                resp.value.items[2].title + "</li>";
                lister += "<li><A HREF=" + resp.value.items[3].href + ">" +
                resp.value.items[3].title + "</li>";
                lister += "<li><A HREF=" + resp.value.items[4].href + ">" +
                resp.value.items[4].title + "</li>";
                lister += "</ul>";
                document.getElementById("thenews").innerHTML = lister;
            }
    }

    request.open("GET","http://pipes.yahoo.com/pipes/pipe.run?_id=4659b1f4f4bfdb96c3775b61be
8ca3b8&_render=json",true);
            request.send();
}
</script>
</head>
<body>
<span style="font-family: Helvetica,Arial,sans-serif;">Get the News!<br>
<div id="thenews">
<h2>...</h2>
</div>
<button type="button" onclick="loadnews()">Get The News!</button>
</span>
</body>
</html>
```

你会注意到这段代码大部分与我们在每日一词中使用的代码相同。特别是，我们改变了一些东西，在我们的代码中以粗体显示。

-   - 我们将请求从word.txt更改为雅虎Pipes JSON输出的URL。
- 我们现在使用jQuery，这是一个我们之前用过的库，包含一些用于读取和解码JSON输出的有用函数。使用jQuery意味着我们必须在顶部添加对jquery-1.7.1.min.js文件的引用。

-   - 我们现在使用jQuery.parseJSON来解析我们从XMLHttpRequest获取的文本。
- 我们有一个HTML格式的列表，一旦检索到JSON就会显示。

完成的产品在我们的浏览器中看起来像这样（图12-14）：

![](img/8b0ff5e51ddb912cd941bb18cf27206a_226_0.png)

当我们点击“获取新闻！”时，显示以下内容（图12-15）：

![](img/8b0ff5e51ddb912cd941bb18cf27206a_226_1.png)

现在我们已经从服务器加载了数据，也从Web服务加载了数据，我们可以转向最后一部分：网页和数据库之间的来回交互。这类似于Google的即时搜索结果，这是我们之前讨论过的功能。我们将从使用清单12-6中的模式创建数据库开始。这个清单首先创建一个表，然后用几个测试用户名（“hardcore”、“dinosaur”等）填充它。

**清单12-6。** *用户表的SQL模式*

```sql
CREATE TABLE IF NOT EXISTS `users` (
  `name` varchar(25) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

--
-- Dumping data for table `users`
--

INSERT INTO `users` (`name`) VALUES
('hardcore'),
('dinosaur'),
('yelius'),
('tep');
```

使用前面的模式在你的MySQL数据库中创建users表。（MySQL可在http://www.mysql.com/products/community/获取。）注意，你可以随意命名数据库，但在这个例子中它被称为“datab”。现在我们需要一个简单的PHP脚本，它接收一个值并在数据库中检查它。清单12–7将很合适。

**清单12–7。** *check_name.php脚本*

```php
<?php
$name = $_GET['u'];
$user = "root";
$pass = "";
$server = "localhost";
$db = "datab";
mysql_connect($server,$user,$pass) or die("Can not connect");
mysql_select_db($db) or die("No such database");
$query = "SELECT * FROM `users` where `name` = '$name'";
$result = mysql_query($query);
if (mysql_num_rows($result) == 0)
{ echo "<font color=green>Available!</font>"; } else { echo "<font color=red>Not Available :( </font>"; }
?>
```

前面的脚本相当简单。它连接到数据库并执行一个简单的查询，查看该名称被输入了多少行。如果在任何行中都找不到该名称，那么它是可用的；脚本返回“Available”（并且推测会有许多欢呼）。然而，如果它不可用，因为数据库中已经有包含该名称的行，脚本会返回相当悲伤的“Not Available”。你可以通过在Web浏览器中访问check_name.php脚本（包含&u=test和某种测试用户名）来测试这一点。例如，在我的测试环境中，http://localhost/~jon/uname/check_name.php?u=dino返回“Available”，而http://localhost/~jon/uname/check_name.php?u=dinosaur返回“Not Available”。如果这对你有效，那么你就可以继续了。

#### 清单 12–8. checkname.html 页面

```html
<html>
<head>
<title>Registration Page</title>
<script type="text/javascript">
function checkusername($name) {
    if (window.XMLHttpRequest) {
        // Modern browsers use this type of request
        request = new XMLHttpRequest();
    } else {
        // Old Microsoft Browsers use this type!
        request = new ActiveXObject("Microsoft.XMLHTTP");
    }

    request.onreadystatechange = function() {
        if (request.readyState == 4 && request.status == 200) {
            document.getElementById("theres").innerHTML = request.response;
        }
    }

    request.open("GET", "check_name.php?u=" + $name, true);
    request.send();
}
</script>
</head>
<body>
<form name="theform">
<span style="font-family: Helvetica,Arial,sans-serif;">Register!<br>
<div id="theres">
<h2>...</h2>
</div>
<input type="text" name="un" onkeyup="checkusername(this.form.un.value)">
</span>
</form>
</body>
</html>
```

你会注意到，和上次一样，我们是基于“每日一词”中使用的相同格式进行构建的。这次我们将函数改为接受一个参数（我们需要检查的名称），并将按钮改为文本字段。这个文本字段在每次按键释放时（`onkeyup` 事件）检查名称，结果会随之更新。加载后，页面看起来类似于图 12–16。

注册！

____________

#### 图 12–16. 检查用户名页面

如果你输入一个可用的名称，比如 “skip”，你会看到一条成功消息，如图 12–17 所示。

注册！
可用！
skip

图 12–17. *甜蜜的胜利*

然而，如果你想要的用户名已被某个厉害的人占用，那么你会看到一条令人难过的消息，如图 12–18 中所示。

注册！
不可用 :(
dinosaur

图 12–18. *“不可用”界面*

在整个网络表单中应用此技术，不仅能让你实时检查用户名，还能验证信息，这样用户就无需在点击“提交”按钮后才发现自己输入了无效的数字、电子邮件地址或用户名了。

在结束之前，关于表单有两个你可能觉得有用的小建议。第一个是考虑你想将 AJAX 检查代码绑定到哪个事件上。在这个例子中，我们将其绑定到我们正在检查的表单字段（用户名）的 `onkeyup` 事件上。然而，这会导致每次按键都触发一次查询操作，这可能会拖慢你的脚本。一个替代方案是将函数代码放在下一个元素（例如，可能是一个密码字段）的 `onfocus` 事件中，而不是 `onkeyup`。这将导致 AJAX 请求在用户移动到表单上的下一个字段后才触发，从而减少负载。第二个考虑涉及表单的验证和自动提交。让表单在最后一个字段完成后自动提交可能很诱人。毕竟，你可能在用户输入信息时就在进行验证，所以为什么要在他们完成最后一个字段后让他们等待呢？但这可能会带来问题，因为有些人可能希望在继续之前检查他们的答案。最好在页面上保留一个“提交”按钮，让用户在准备就绪时继续。

## AJAX 考量

在这个相对较短的章节中，我们使用的例子涵盖了使用 AJAX 时你会交互的三种主要数据类型。我们从服务器获取数据并将其放入页面，而无需刷新；我们查询网络服务以获取 RSS 新闻标题；我们检查用户名以确保其可用。至此，你已经掌握了编写利用 AJAX 强大功能的应用程序所需的基本工具。从这里开始构建时，有几件事需要考虑，接下来我们将重点说明。

### POST 与 GET

你会注意到，在我们的例子中，我们一直在使用 GET 方法而不是 POST 方法，这在清单 12–3 和 12–4 中首次出现。这样做的主要原因是速度。GET 比 POST 快得多，因为它使用的格式更简单。如果你想知道原因，很可能是因为 GET 的最初用途——它仅设计用于“幂等”数据。这仅仅意味着该信息不是为了持久使用（即它应该只是一个查找值，而不是要输入数据库或以任何方式处理的数据）。

然而，有时 POST 会更合适。首先，GET 有大小限制，而 POST 没有，因此如果你要传递大量信息到服务器，就需要使用 POST。其次，当你在更改服务器上的内容（例如数据库更新）时，应该使用 POST，而不是引用静态或缓存的内容。简单来说，如果你传递的数据不会再被需要，就使用 GET。如果你传递的数据需要被处理或输入到数据库、电子邮件或文件中，就使用 POST。

使用 POST 比使用 GET 稍微复杂一些。你需要设置一个请求头，并通过 send 函数发送信息。这是因为 POST 数据编码在消息体中，而 GET 数据只是简单地附加到 URL 上。这就是为什么图 12–8 中的 Android 浏览器会提到重新发送 POSTDATA——它指的是这个特殊编码的消息。如果我们想将我们的用户名示例改为使用 POST，我们可以更改以下几行：

```
request.open("GET","check_name.php?u=" + $name,true);
request.send();
```

更改后将得到清单 12–9 中所示的行。

#### 清单 12–9. 在用户名可用性示例中使用 POST

```
request.open("POST","check_name.php",true);
request.setRequestHeader("Content-type","application/x-www-form-urlencoded");
request.send("u="+$name);
```

我们还必须修改 PHP 脚本（参见清单 12–7），将第一行从 `$name = $_GET['u'];` 改为 `$name = $_POST['u'];`

### 设置 Asynchronous 为 False？

正如你在前面的例子中看到的，我们 XMLHttpRequest 的 open 函数的第三个参数通常设置为 “true”。这样设置是有道理的——毕竟，我们为什么要设置它为 false 呢？嗯，答案是我们很少会这样做！不过，在某些情况下你可能会这么做。例如，如果你正在编写一个脚本，并且你绝对不希望在请求返回并准备好处理之前发生任何事情，那么设置这个值为 false 是可以的。我能想到的一个例子涉及一个用户名检查表单，类似于图 12–16 中的那个，它应该只允许用户在用户名可用的情况下继续填写表单（也许是为了根据用户名定制其他选项）。在这种情况下，人们可能会禁用或隐藏所有后续的表单字段，然后等待请求返回；如果成功，这些字段可以重新启用或显示。但要注意，你的整个脚本都会被挂起，因此用大量数据这样做不是一个好主意。你可以想象整个浏览器“卡住”，这在任何平台上都令人沮丧，但在对速度需求本就更高的移动设备上尤其烦人。

还要注意，如果你决定设置 asynchronous 为 false，你不需要（也不应该使用）`onreadystatechange` 函数。这是因为没有要查找的 ready state——代码将在请求准备好后继续处理。只需将你的其余 JavaScript 代码放在 send 函数之后，它将按顺序处理。

最后，在设置 asynchronous 为 false 之前，你可能需要问问自己，AJAX 是否真的是实现你目标的最佳解决方案。当然，它可能看起来很酷，但如果你需要强制用户等待某件事，也许用不同的方式实现代码会更容易。例如：

-   如果你的用户可能禁用 JavaScript，那么要求使用 JavaScript 来完成表单将使页面对他们无用。使用设置 asynchronous 为 true 的 AJAX 通常可以避免这个问题。
-   一个需要在几个选项之后进行复杂验证（例如数据库查询）的长表单，最好作为一个多页表单来处理，允许用户在第一页创建账户，然后在空闲时返回后续页面。每个页面都可以保存表单的进度，允许用户在需要时跳回，同时提供充分的验证。

考虑到这些想法以及你在测试中的自身经验，你不仅会对最佳的表单提交方法（GET 或 POST）有概念，还会知道在你的脚本中使用不常见的设置 asynchronous 为 false 的方法是否是个好主意。

## 总结

在本章中，我们朝着让用户生活更轻松迈出了重要一步。我们开始在后台处理一些表单或页面上的操作，这样用户就不需要毫无必要地刷新页面、提交表单或重新加载内容。通过将这里概述的想法和概念应用到你的项目中，甚至应用到我们之前的示例中，你将能够很快创建出出色的“增强”设计！



## 第13章：打包你的应用程序

终于到了这一刻：最后一章。在本书中，我们回顾了往昔岁月（也就是20世纪90年代），学习了CSS3、HTML5和JavaScript的奇妙之处。我们尝试了音频和视频。我们体会到了使用JavaScript框架来提高效率，并为用户打造令人惊叹、易于创建的页面布局的乐趣。我们甚至创建了一堆初学者应用程序，其中一个最终让你成为了国际神秘人物，为你未来的明星之路奠定了基础。希望在阅读完本书后，我们已经成功地强调了优化代码以及在开发时考虑到大量移动用户受限的有限带宽的重要性。

然而，如同所有美好的事物一样，我们的时间也即将告终。不过，在我们结束之前，我还将向你介绍更多信息。虽然我们已经学习并构建了一系列有趣的应用程序，但当我们完成这些应用程序的构建后，接下来该做什么，我们还未涉及！在本章的剩余部分，我们将涵盖从打包和压缩你的应用程序，使其准备好上互联网；到选择合适的托管服务来存储你的应用程序；再到将你的文件传输到你使用的任何托管服务；甚至完全跳过整个托管服务解决方案，转而将你可靠的HTML5代码封装在PhoneGap或Appcelerator的Titanium Mobile这样的框架中，这样你的代码就能像原生应用程序一样运行，用户可以从Android Market下载并安装到他们的设备上！

### 压缩你的应用程序

现在你已经完成了代码编写，并在本地开发环境中进行了测试，你可能很兴奋地想要将你的应用程序上传到互联网，并开始告诉你认识的每一个人去看看它。在任何项目中达到这个阶段都是一项成就，但代码完成并不意味着你没有其他工作要做。在本书中，我试图反复强调更智能地编码的重要性；以及诸如使用CSS3创建华丽的渐变效果，和自定义Web字体（得益于Google令人惊叹的Web字体目录）来替代图像或其他“重量级”资源（如Flash动画）的做法。这些方法最终有助于你的代码在用户的设备上快速加载。

当然，我们正处于全国第四代移动互联网对所有需要的人开放的边缘，但实际上，你的运营商的宽带服务有多快并不重要，因为移动网络在延迟方面表现不佳（延迟是指你的手机在数据传输之前与你试图加载的网站或服务进行通信所需的时间）。为了帮助我们的代码更快地到达用户手中，反过来也有助于减轻我们可怜的Web服务器的压力，我们将做一些通常被称为代码最小化的事情。最小化或压缩我们的代码包括将我们的CSS和JavaScript文件通过一个应用程序或服务运行，该程序或服务会移除所有换行符和不需要的空白，使最终产品比之前小得多。

#### 什么是压缩？

让我们再次看看许多Web开发者使用的流行的jQuery框架。正如你在图13-1中看到的，我们有两个版本的jQuery主库。一个版本的脚本是未压缩的，体积庞大，达到231KB；另一个版本已经过压缩和一轮混淆处理，总大小减少到仍然较高但更易管理的90KB。在代码编辑器中打开我们的JavaScript文档，我们可以立即看到两个文件之间的差异。如图13-2所示，jQuery的开发版本格式非常漂亮，中间穿插着许多非常有用的注释；而体积更小、可用于生产环境的jQuery版本看起来几乎像一种奇怪的外星语言，几乎难以理解。请看图13-3，以更好地理解我所指的内容。这就是混淆代码所做的。我们不仅移除了所有换行符和漂亮的格式，而且代码本身被缩小和修改，以混淆代码并使其更难理解。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_234_0.png)

![](img/8b0ff5e51ddb912cd941bb18cf27206a_234_1.png)

![](img/8b0ff5e51ddb912cd941bb18cf27206a_235_0.png)

图13-3。在Adobe Dreamweaver 5.5中查看压缩、混淆且如外星代码般的jQuery代码

有人可能会问，我们为什么要混淆代码——毕竟，难道我们不希望别人看到我们巧妙的技巧吗？嗯，在像本书这样的书中，我们当然希望，但在现实生活中，保持一些东西“藏在手心里”可能非常重要。虽然混淆代码并不能阻止执着的代码阅读者找出你的所有秘密（因此，永远不要依赖混淆的代码来保护诸如密码、信用卡号码、核发射代码等东西），但它会阻止那些知识有限的人窃取你辛苦工作很久才得来的代码，仅仅是为了重用你巧妙的过渡效果或酷炫的布局。

#### 压缩工具和实用程序

互联网上有大量的程序和可靠的老网站可以帮助你使生产就绪的代码变得更小，减轻服务器和用户的资源负担。最受欢迎的之一是雅虎的YUI Compressor（图13-4）。与其他一些压缩解决方案不同，YUI Compressor是一个用Java编写的应用程序，需要在你的开发工作站上运行。运行应用程序并从命令行给出你所需的选项后，该应用程序将获取你的代码，按我们讨论的方式压缩它，甚至将你许多不同的JavaScript或CSS文件合并成一个超级压缩的文档，准备好上传到你的服务器。你可以在 http://developer.yahoo.com/yui/compressor/ 找到YUI Compressor。

```
$ java -jar yuicompressor-x.y.z.jar
Usage: java -jar yuicompressor-x.y.z.jar [options] [input file]

Global Options
-h, --help              Displays this information
--type <js|css>         Specifies the type of the input file
--charset <charset>     Read the input file using <charset>
--line-break <column>   Insert a line break after the specified column number
-v, --verbose           Display informational messages and warnings
-o <file>               Place the output into or a file pattern.
                        Defaults to stdout.

JavaScript Options
--nomunge               Minify only, do not obfuscate
--preserve-semi         Preserve all semicolons
--disable-optimizations  Disable all micro optimizations

GLOBAL OPTIONS

-h, --help
    Prints help on how to use the YUI Compressor

--line-break
    Some source control tools don't like files containing lines longer than,
    say 8000 characters. The linebreak option is used in that case to split
    long lines after a specific column. It can also be used to make the code
    more readable, easier to debug (especially with the MS Script Debugger)
    Specify 0 to get a line break after each semi-colon in JavaScript, and
    after each rule in CSS.

--type js|css
    The type of compressor (JavaScript or CSS) is chosen based on the
    extension of the input file name (.js or .css) This option is required
    if no input file has been specified. Otherwise, this option is only
    required if the input file extension is neither 'js' nor 'css'.

--charset character-set
    If a supported character set is specified, the YUI Compressor will use it
    to read the input file. Otherwise, it will assume that the platform's
    default character set is being used. The output file is encoded using
    the same character set.

-o outfile
    Place output in file outfile. If not specified, the YUI Compressor will
    default to the standard output, which you can redirect to a file.
    Supports a filter syntax for expressing the output pattern when there are
    multiple input files. ex:
    java -jar yuicompressor.jar -o '*.css$:-min.css' *.css
    ... will minify all .css files and save them as -min.css

-v, --verbose
    Display informational messages and warnings.

JAVASCRIPT ONLY OPTIONS

--nomunge
    Minify only. Do not obfuscate local symbols.

--preserve-semi
```

![](img/8b0ff5e51ddb912cd941bb18cf27206a_236_0.png)

使用YUI Compressor可能看起来令人生畏（当查看所有选项时，如图13-4所示），但它实际上相当直接。例如，假设我想压缩我们第2章“Who's That Tweet?”应用程序中的main.js文件。首先，我会从其网站下载YUI Compressor。然后，我会解压文件，打开一个命令行窗口，并切换到包含Java JAR文件的目录（在本例中为yuicompressor-2.4.7.jar；此名称将根据版本而变化）。接下来，我会将我想要压缩的文件复制到当前目录，并运行压缩命令。我将使用的命令是：

```
java -jar yuicompressor-2.4.7.jar main.js -o main.small.js
```



## 第13章：打包你的应用程序

这会告诉 YUI Compressor 将 main.js 压缩成一个名为 main.small.js 的更小文件。在此例中，压缩器将文件大小从 3,763 字节缩减到了 1,946 字节——略多于一半！

还有一些其他压缩应用程序绝对值得一提。我想介绍的第一个是 Dean Edwards 创建的一个便捷小工具，名为 Packer（http://dean.edwards.name/packer/），如图 13-5 所示。这个网络服务允许你将开发中的 JavaScript 代码复制到网站上的一个文本区域，然后只需快速点击一个按钮，就能输出压缩后的 JavaScript 代码，你可以直接将其复制粘贴到一个新的文本文件中，然后就可以使用了。如果你认为 YUI 对你的特定需求来说可能有点大材小用，Packer 可能是一个非常棒且极其简单的替代方案。

然而，需要注意的是，虽然 Packer 是一个很好的代码压缩工具，但通过简单地禁用防止你将代码粘贴到“复制”框中的 JavaScript 并点击“解码”，它也很容易被反向还原！因此，它应该仅被用作压缩工具，而非安全机制。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_237_0.png)

**图 13-5。** *使用 Packer，我们可以轻松地将第2章的“Who's That Tweet?” JavaScript 代码（位于顶部文本区域）压缩成仅占原始文档大小极小一部分的内容（如底部文本区域所示）。*

我想讨论的最后一个很棒的软件是一个由 Paul Irish 创建的代码和应用集合，称为 HTML5 Boilerplate，可以在 `http://html5boilerplate.com/` 找到。虽然它本身不是一个压缩工具，但它是一个非常有用的框架，你可以考虑用于应用开发，并且它包含自己的压缩工具。HTML5 Boilerplate 是一个相当年轻的项目（于 2010 年 8 月 10 日推出），是那些不想因为需要一遍又一遍地编写相同的基础代码而烦恼的开发者的绝佳起点，因为这些基础代码几乎包含在他们创建的每一个项目中。有些人喜欢将 HTML5 Boilerplate 与框架混淆，但实际上它远非一个框架。我更愿意将这个项目视为一种组织结构和工具箱（图 13-6）；它帮助你有序地组织项目文件，并通过提供一种简单的方式来实现开发者经常需要重复做的许多事情（例如指定某些文件、JavaScript 库等），让你避免重复劳动。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_238_0.png)

**图 13-6。** *HTML5 Boilerplate 文件夹结构一瞥。所有神奇的压缩功能都在 "build" 文件夹内进行。*

在 Boilerplate 包中（截至本文写作时为 2.0 版本），可以找到大量有用的项目和功能，例如：已经编写好的 index.html 和 404.html 文件的基础骨架布局；最新版本的 jQuery；一些用于在广袤的互联网浏览器海洋中重置样式的预定义 CSS 样式；用于移动环境的特殊优化；甚至还有一个漂亮的小型代码压缩器，当你准备发布应用程序的生产版本时，它会为你压缩 HTML、CSS 和 JavaScript 文件。

要使用内置工具（包括我们之前讨论过的 YUI Compressor 等压缩器）压缩文件，只需编辑位于 build 目录中的 build.xml 文件（参见图 13-7）。在这里，你会找到一堆你可以指定的选项，随心所欲地压缩你的 Web 应用程序。你可能需要花点时间来熟悉这个文件的配置，但一旦你按照自己的意愿设置好了一切，你只需运行 runbuildscript.bat 文件，你的代码就会被快速压缩和优化。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_239_0.png)

## 寻找托管解决方案

既然我们已经设法从代码中挤掉了每一个不必要的字节，使其尽可能小，现在是时候将这个美丽的“东西”上传到互联网上，让全世界都看到了。找到一个适合你和你的项目的托管解决方案有时可能是一件令人沮丧的事情，特别是当你不确定自己具体需要什么的时候。在这里，我们将讨论三个最大的托管公司，以及我们的印象和它们提供的功能。不过，首先让我们考虑一下选择托管服务提供商的过程。

### 评估托管服务提供商

并非每个提供商都是一样的，对一个开发者来说运作良好的服务可能无法满足另一个开发者的需求。你需要了解提供商的情况，并清楚自己的需求和目标。在评估任何托管服务时，以下问题是一个很好的起点：

1.  **我能得到多少个域名或子域名？** 在许多 Web 开发者刚开始的时候，最大的问题是“我有多少空间？”或“我有多少流量（每月可以发送的数据量而不会产生超额费用——基本上就是你可以有多少访客）？”。
2.  **他们的技术支持响应如何？是否有常见问题解答（FAQ）或知识库？** 在我使用当前 Web 托管的六年，以及使用前一家托管的十年里，我可能因为各种各样的问题（从微小的（“服务器支持...吗？”）到重大的（“我所有的网站都宕机了。”））给技术支持发过大概五到十次电子邮件。每次我都希望立即得到答案，尤其是在后一种情况下，因为任何等待的时间都太长了。更好的是，我当前的 Web 托管提供了非常好的常见问题解答和知识库，涵盖的内容远不止重置密码或创建新电子邮件账户。它讨论了诸如 PHP 版本、服务器软件、Shell 访问权限等问题。关键是：你要确保当遇到问题时，要么信息已经可用以提供帮助，要么帮助能够通过一封快速的电子邮件得到响应。
3.  **有哪些管理工具可用？** 你会希望选择一个在账户管理方面提供足够功能的 Web 托管。有些托管商可能希望你每次需要设置新域名、数据库或任何其他东西时都联系他们。而另一些则可能通过控制面板完全自动化这个过程。我倾向于选择后者，因为前者通常总是可用的。我当前的托管商甚至允许我在网上取消域名或整个账户，如果我将来决定离开，这可以省去一次尴尬的电话沟通。
4.  **如果我的计划不够用了怎么办？** 有可能在几年后，你需要访问更高级的功能或更多的资源。接下来，在我们对 Dreamhost 的讨论中，我们注意到它提供某些功能来“扩展”或“升级”你的套餐。如果你担心未来，你可以调查或询问潜在的托管商，切换计划或升级有多困难。如果他们说你必须重新设置一切，你可能想找一个能为你迁移一切，或者只需简单升级而无需任何更改的托管商。
5.  **我是否有 Shell 和/或 CRON 访问权限？** 最后一点有点技术性，但如果你从事某些类型的开发工作，它可能很重要。Shell 访问，或 Shell 账户，指的是你作为客户能够以交互方式登录到托管商服务器的能力。通常通过一个名为 SSH 的服务，Shell 账户允许你直接在服务器上运行命令，就像你电脑上的命令提示符或终端窗口一样。CRON 是服务器上的一个特殊软件包，允许你安排命令稍后或定期运行。如果你创建的应用程序需要定期检查自身——例如一个向用户发送电子邮件的应用程序——这对你来说可能非常有用。每 20 或 30 分钟，你可能需要自动运行一个脚本来检查是否有任何电子邮件需要发送。CRON 访问权限允许你这样做。然而，CRON 也可能被滥用，这就是为什么一些 Web 托管不允许你使用它，或者根本不允许你交互式登录服务器。

除了前面提到的指导原则，你也可以在决定选择哪家托管商时查阅评论网站。但要小心：这些网站上一些过于正面或过于负面的评论可能并不代表实际的服务质量。归根结底，我们总是更信任那些我们知道真正使用过某项服务的人的推荐，而不是那些可疑的评论，这就是为什么我们会快速花点时间回顾一下我们过去使用或合作过的一些托管服务提供商，为你寻找完美托管商的过程提供一个良好的起点。

请注意，以下部分讨论了许多托管商提供的功能，而我们提到的具体托管商只是我们个人使用过的。虽然我们显然对其服务感到满意，但我们绝不会假设它们适合每个人。请考虑以下段落中读到的内容，权衡你的选择和价格范围，找到适合你的托管商！



## Dreamhost

在过去的六年里，我（Rocco）一直是托管服务商 Dreamhost（http://dreamhost.com/）的忠实粉丝，这是一家由四位雄心勃勃的计算机科学本科生于 1997 年创建的优秀小公司（见图 13–8）。Dreamhost 已经存在了一段时间，虽然在过去经历了一些成长的阵痛，但它们为我提供的服务始终坚如磐石，几乎没有任何波折。它们的价格极具竞争力，通常起价为每月 9 美元，甚至还为客户提供无限带宽和无限存储空间。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_242_0.png)

*图 13–8。自 1997 年以来，Dreamhost 一直在互联网上托管数百万个网站。目前，它们托管着超过 50 万个基于 WordPress 开源内容管理解决方案的网站*

Dreamhost 提供多种托管服务，其中基本的托管形式是共享环境。虽然共享托管对于基本项目来说没问题，但采用这种路线存在一些主要的局限性。首先，您与同一服务器上的其他人共享一个环境，如果某人上传了一个脚本，该脚本以某种方式占用了服务器的大量资源甚至导致服务器崩溃，那么该服务器上的每个人都会受到影响。此外，您在共享服务器上能进行的自定义操作非常有限。您无法安装自定义应用程序或服务以后台运行，也无法对 Web 服务器配置文件进行任何更改。

如果你像我一样是一个控制狂，你可能想看看自己是否可以获得虚拟私有服务器（VPS）或专用服务器。虚拟私有服务器本质上是一台在另一台计算机内部运行的计算机。使用专门的虚拟化软件，人们可以在安全且隔离的软件解决方案中模拟计算机的硬件，允许你在另一个操作系统内安装并运行整个操作系统，就像它是一个独立的计算机一样。当您在 Dreamhost 租用虚拟私有服务器（VPS）时，您仍然与其他人在共享环境中使用它，但您有一个*巨大的*优势，即被沙箱隔离或保护，免受与您共享该物理服务器的其他人的有害操作影响。

您不仅不必担心因为其他人的疏忽而导致您的网站宕机，您的资源也得到了保护。在 Dreamhost 的管理面板中，使用一个极其简单的滑块，您可以随时、实时地为您的服务器分配任意数量的 RAM 和 CPU 处理能力（见图 13–9）。然而，为您的服务添加更多的 RAM 和 CPU 功率会增加您的月费；但如果您有一个应用程序，您知道它需要专用的 1GB RAM 和 CPU 功率以及时地快速服务所有用户，那么知道这些资源会自动为您独家保护是非常美妙的。如果您对在 Dreamhost 上设置 VPS 感兴趣，它提供第一周的免费试用期，您可以将服务器扩展到所需或较低的资源量，以找到适合您网站的最佳资源量。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_243_0.png)

*图 13–9。使用滑块来确定具有选定数量的 RAM 的虚拟私有服务器的成本*

Dreamhost 还让您拥有自己的专用环境。通常，这些机器是相对强大的服务器，拥有两到四个 CPU 核心，甚至高达 12GB 的 RAM。如果您是新手开发者，您可能不需要那么多处理能力，但当您有一天需要时，您现在知道去哪里找。

除了拥有在 Dreamhost 托管您网站的众多选择外，您还可以获得非常响应迅速的技术支持团队。如果您遇到问题，或者服务器在深夜出现混乱情况，在大多数情况下，您可以在几分钟内与技术人员进行文本聊天，并迅速解决问题。在我过去使用过的所有托管公司中，Dreamhost 在我需要帮助时，是我最喜欢的之一。

#### 1and1

作者转换（Jon 在这里），现在是时候听听我过去六年的 Web 托管服务商 1and1 的情况了。1and1 实际上是一家相当大的托管商，在行业内大多获得 lukewarm（不冷不热/褒贬不一）的评价。它不是最好的（尽管谁是最好的存在争议），也不是最差的。Dreamhost 提供的许多功能（Rocco 之前讨论过的）1and1 也有（事实上，许多其他托管服务商也有），所以我认为最好简单地概述一下我发现 1and1 真正有用的方面。这归结为两个类别：文档和可靠性。文档指的是 1and1 的 FAQ（常见问题解答）部分，这让我感到惊讶，因为它的一般问题中包含了我之前提到的详细信息。我当时遇到了一个脚本问题，当 1and1 的 FAQ 网站拥有非常具体的服务器设置、PHP 版本和可用软件信息时，我感到非常惊讶。我能够调试我的问题，而无需写一封冗长复杂的电子邮件。我非常喜欢的第二个 1and1 的特点是服务的可靠性。虽然没有人能吹嘘 100% 的正常运行时间（行业标准术语，指服务器或服务可用），但根据我所见，1and1 非常接近。作为一个按最低清单收费的客户（即，我在基本共享托管套餐上每月支付约 9 美元），如果我的服务时好时坏，我不会感到惊讶。事实上，情况恰恰相反——在我在这里的整个时间里，我的网站几乎没有宕机。

如果您正在考虑其他托管服务商，并想知道其在可靠性方面的表现，您可能会找到一位使用它的朋友或论坛人员，并询问他们的域名是什么。从这里，我建议用 Pingdom（http://www.pingdom.com）等服务设置一个免费账户，这是一个 uptime（正常运行时间）监控服务。Pingdom 允许您免费监控一个网站，所以不妨将其指向您朋友网站。几周或几个月后，您将获得可以 consulted（查阅）的报告，以查看该托管服务商是否可靠地保持在线。

所以就这样，1and1 对我而言是可靠和彻底的。现在回到 Rocco 讨论最后一个托管服务商！

#### Media Temple

我（Rocco）过去使用过的另一家托管公司，也是我将在本章与您讨论的第三家，是行业内最受欢迎的 Media Temple（http://mediatemple.net/）之一。在许多方面，Media Temple 提供的服务对于更技术性的用户来说可以被认为是比 Dreamhost 更好。Media Temple 提供了一系列解决方案，从基本的 Grid Server（网格服务器）套餐开始（见图 13–10），该套餐将您的网站托管在一个拥有数百台其他服务器支撑该集群的集群中。它也提供专用虚拟服务器，就像 Dreamhost 一样，并提供一系列非常强大的专用服务器。

我对 Media Temple 唯一的真正问题是，它往往比其他提供商（如 Dreamhost）贵得多，但它确实有提供更好硬件和像 Dreamhost 那样的技术支持的选项；所以如果您在寻找力量，请务必查看 Media Temple 提供的内容。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_245_0.png)

*图 13–10。Media Temple 的 Grid Service 着陆页*

## 文件传输协议

现在我们已经引导您朝着满足您需求的托管服务商的方向前进，我们必须将我们在本地开发服务器上创建的这些文件上传到我们闪亮的新生产服务器上。这一步通常通过文件传输协议（FTP）应用程序完成。FTP 是一种标准的网络协议，用于在一台计算机和另一台计算机之间传输文件和文档。在您的托管机器上有一个运行的 FTP 服务器，它将允许您使用台式机或工作站上的 FTP 客户端连接到该机器。这里有大量的免费 FTP 程序，但我个人最喜欢的是一款名为 FileZilla（http://filezilla-project.org/）的免费开源软件，如图 13-11 所示。

**图 13–11。*使用 FileZilla 将本书的代码传输到我的一个预发布服务器进行测试***

我喜欢 FileZilla 的一个主要原因是，这个软件一直在不断更新，而且与该项目相关的开发人员非常努力地工作，以确保它成为市面上最快和最稳定的 FTP 程序之一。

使用 FTP 客户端实际上非常简单且直截了当。一旦你注册了一个托管解决方案，你会获得用于插入应用程序的凭证，一旦连接成功，如果你的 FTP 客户端支持该功能，你只需将你想要的文件拖放到服务器上你拥有访问权限的任何文件夹中即可。以下是一些 FTP 凭证可能的示例：

```
url: ftp.myawesomesite.com
user: testuser112
password: pssw0rdz
port: 21
path: /var/www/myawesomesite.com/
```

如果你以前从未这样做过，可能会觉得有点困惑。在下一节中，我们将介绍如何部署应用。

### 使用安全 FTP 部署应用程序

在这个例子中，我们将引导你使用 SFTP 将整个应用程序上传到网络托管服务。我们将在 Windows 机器上使用 FileZilla，但如果你使用 Mac，你可以使用一个名为 Cyberduck 的免费捐赠支持程序。步骤大致相同，尽管屏幕在 Mac 上的显示会有所不同。

首先，你需要收集以下信息：

-   你的网络主机要求的连接方法。一些网络主机不再支持 FTP，而是更倾向于加密版本 SFTP。你需要知道你的 FTP 地址（通常是 ftp.yourdomainname.com，其中 yourdomainname 是你的个人域名，如 jonwestfall.com）、你的 FTP 用户名和 FTP 密码。
-   你需要知道你域名的文件是否位于网络主机上的特定目录下。许多网络主机默认将你的 FTP 信息放在根目录下（即，一旦你登录服务器，你在 "/" 下看到的文件与域名下的文件相同。所以 /test.txt 对应于 http://jonwestfall.com/test.txt）。其他主机可能会将你的文件放在以域名命名的目录中（即 /jonwestfall.com）或名为 /public_html 或 /web 的目录中。
-   你还需要考虑你希望你的文件存放在哪里。在这个例子中，我希望 "Who's That Tweet?" 存放在 http://jonwestfall.com/whosthattweet，所以我需要创建该目录并将我的文件上传到其中。

一旦你拥有了所需的信息，下载并安装 FileZilla 客户端（从 http://filezilla-project.org/download.php 下载）。安装后，你应该能在“开始”菜单中的 FileZilla FTP Client 组下找到它。打开 FileZilla，你应该会看到一个类似于图 13–12 的屏幕。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_248_0.png)

**图 13–12。** *未进行任何配置的 FileZilla 主窗口*

你会注意到它相当空旷，并被分成六个窗格。顶部的窗格显示 FileZilla 发送到服务器的 FTP 命令。左侧的窗格显示你计算机上的文件（以树状格式显示以及列出你正在查看的目录中的文件），右侧的窗格将显示服务器上的文件（在我们连接后，采用相同的排列方式）。底部显示我们当前正在传输的文件，从一侧到另一侧（从我们的计算机到服务器，或反之亦然）。

首先，在顶部的“主机”框中输入你的 FTP 主机名、你的 FTP 用户名和你的 FTP 密码。如果你的主机支持 SFTP（更安全的方式），你需要在“端口”框中输入 SFTP 的端口号，通常是 "22"。但是，如果你只能使用普通 FTP，你将使用 FTP 端口号，通常是 "21"。（注意：如果你的主机更改了这些值，这非常罕见，你应该能在其常见问题解答部分或知识库中找到它们。）输入所有信息后，按“快速连接”以连接到服务器（图 13–13）。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_248_1.png)

**图 13–13。** *FileZilla 的 SFTP 主机连接信息*

如果这是你第一次连接到该服务器，并且你正在使用 SFTP，你可能会看到以下框（图 13–14）要求你验证服务器身份。通常你不知道要验证什么值，但你可能想在第一次记下它，以确保它总是相同的。这是一个安全功能，确保你始终连接到正确的机器。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_249_0.png)

**图 13–14。FileZilla 未知主机密钥提示**

一旦你登录，屏幕右侧的窗格会更改以显示服务器上的文件。单击文件夹直到找到你想要上传文件的位置。在我的例子中，我将转到 /new-jonwestfall.com 目录（jonwestfall.com 的网页文件所在的位置）并创建一个 whosthattweet 目录。我可以通过在右侧窗格中双击 new-jonwestfall.com，然后在空白处右键单击来完成此操作。在出现的菜单中（图 13–15），我选择“创建目录”，在下一个窗口中（图 13–16），我为它命名。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_249_1.png)

**图 13–15。右键单击显示上下文菜单，允许你创建一个目录**

![](img/8b0ff5e51ddb912cd941bb18cf27206a_249_2.png)

**图 13–16。FileZilla “创建目录”对话框**

现在我确保目录设置正确：我想要移动的文件在左侧，目标位置在右侧，如图 13–17 所示。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_250_0.png)

**图 13–17。** *显示源（左侧）和目标（右侧）*

现在，只需在左侧选择文件，右键单击它们，然后选择“上传”（参见图 13–18）。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_250_1.png)

**图 13–18。** *我现在可以单击“上传”选项将文件上传到服务器*

执行此操作后，我应该在两个窗格中看到相同的文件，如图 13–19 所示。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_250_2.png)

**图 13–19。** *我计算机上的文件（左侧）现在在服务器上（右侧）*

现在是大考验。既然文件已经可访问，我应该能够通过访问相应的地址在移动浏览器（或桌面）中查看它们。在这个例子中，地址是 http://jonwestfall.com/whosthattweet/index.html。通过在桌面网络浏览器中访问此地址，我可以看到文件已经在线，如图 13–20 所示。这可能看起来很丑，因为文件本意是在移动网络浏览器上查看的；但是，我们已经验证了文件已经在线并且可以访问！恭喜——你已经将你的项目上传到网络上了！

![](img/8b0ff5e51ddb912cd941bb18cf27206a_251_0.png)

**图 13–20。** *游戏在桌面浏览器上无法正确渲染，但此测试验证了文件已正确上传*

## 版本控制你的软件

FTP 通常适用于由一个开发者参与的小型开发项目，尤其是在项目不太复杂的情况下。但是，例如，假设你正在与一个开发者团队合作开发一个项目，每个团队成员都可以访问 FTP 服务器，并且可以随时上传和更改内容。最终你会遇到这样的情况：一个用户最终对一个文件进行了更改，一分钟后另一个人上传了他们对完全相同文件的更改，完全覆盖了第一个人刚刚上传的工作。

这是一个非常令人沮丧的情况，实际上，这种事情相当普遍，在程序员没有组织性的情况下时有发生。防止这种情况发生的一个简单方法是使用某种形式的软件版本控制，例如 Subversion，它本质上会为你备份文件并进行版本控制。这样，假设 Jon 对我们共享的一个文件做了一些更改，而我不小心签入了该文件的新版本，但没有包含 Jon 添加的代码。我们可以轻松地将文件恢复到其较早的版本，并保存我们以为丢失的代码，而不是像以前那样只能惊慌失措和恐慌。甚至，使用版本控制，你甚至可以将文件的两个先前版本合并在一起，创建一个超级文件。

市面上有大量等待使用的版本控制解决方案，但最受欢迎的两个解决方案是 Apache Subversion (http://subversion.apache.org/) 和 Git (http://git-scm.com/)。Subversion，也称为 SVN，已经存在很长时间了，是一个非常成熟的产品，在我过去使用过的几乎所有托管解决方案中都有广泛的支持。最棒的是，Windows 上有一个非常棒的

一款能够将所有 SVN 选项添加到右键菜单中的应用程序，这对于那些对使用命令行感到畏惧的新手开发者来说简直是妙极了。
尽管我非常喜欢 SVN，但在过去的几年里，我在版本管理需求上逐渐转向更多地使用 Git。Git 是另一个免费且开源的版本控制软件解决方案，与 SVN 相比它快得令人难以置信，也非常容易上手，正如你在图 13–21 中看到的。

| 克隆和创建补丁 | 创建并提交 |
| --- | --- |
| $ git clone git://github.com/git/hello-world.git | $ cd {project-directory} |
| $ cd hello-world | $ git init |
| $ (编辑文件) | $ (添加一些文件) |
| $ git add {files} | $ git add . |
| $ git commit -m '解释我做了哪些更改' | $ git commit -m '初始提交' |
| $ git format-patch origin/master | |

Git 也往往更加用户友好，这得益于 GitHub（https://github.com/）这一广受欢迎的网站。GitHub 将自己宣传为一个社交代码枢纽，利用 Web 2.0“尽可能使一切社会化”的运作模式（参见图 13–22）。通过 GitHub，你可以免费将所有项目存储在其云平台上；随后其他开发者可以 fork（复制）你的仓库，以便他们对它进行他们想要的任何更改，同时保持这些更改与你的工作完全分离。这有点像是噱头，但 Git 本身是一项如此出色的技术，以至于如果你不喜欢这种社交功能，你只需将其忽略即可。

## 第 13 章：打包您的应用程序

![](img/8b0ff5e51ddb912cd941bb18cf27206a_253_0.png)
git GitHub 欢迎页！下一步是什么？（2011年5月20日）
创建存储库
关于我们
浏览有趣的项目
关注 @github 的 Twitter

给那个宝贝起名叫“八爪鱼”。宝宝们喜欢奥克托卡特。
> 隐藏此次广播
查看最新的 13 次广播

你的仓库（0）
书签

**图 13–22**。*使用社交代码枢纽 GitHub*

最好将版本控制视为备份您的代码和应用程序的一种手段。事实上，即使你是项目中唯一的开发者，在你为该应用创建第一个文件夹或文件的那一刻开始对其进行版本管理也是最好的做法。这样，如果途中发生任何意外（例如笔记本电脑爆炸，或者你的小孩子决定“拯救”电脑并把它淹在苹果汁里），你就能找回那些代码并将其拉取到新机器上继续工作。即使你的计算机没有爆炸，一旦你准备好将项目部署到服务器上，你所需要做的就是登录并在提示符中运行一个简单的命令，即可复制版本化程序的內容到你的生产服务器（即你的网络主机）而无需触碰任何 FTP 程序。

如果你的电脑老师像我小时候的老师一样严厉，他们可能也反复强调不断保存工作的重要性的道理。就像在大学时，你绝不想被写大论文的电源突然中断所赶尽杀绝从而丢失一切那样，务必经常保存工作，然后将这些新修订版本推送到你所选择的版控制解决方案中。

## 原生之旅 (Going Native)

现在我们已经构建了一个应用程序，通过压缩其长久的生命力来优化大小度找到了一个可接受的托管方案，并学会了使用 FTP、SVN 或 Git 将文件传输到该服务器——但如果你不想打包你的应用程序以便在互联网上通过数据连接使用怎么办？如果你在开发将在没有任何数据覆盖的区域使用的应用程序时会怎样？如果你知道你的一款应用程序资源消耗很大，包含大量音频文件或图片而不想让它们在设备上加载等待呢？如果你的项目如此出色，以至于你不想免费赠送给用户，而是想出售它们的副本给他们。别担心，我们为你有了解决方案可以将这种惊人的 HTML5 和 JavaScript 应用程序转变为可以在用户手机上运行的完整原生应用程序，而无需打开他们的互联网浏览器。

此外，采用原生化路线还会为你开启许多 previously unavailable avenues（之前不可用的途径），通过为你提供访问设备功能的权限来实现这一点（例如访问设备的联系人列表，或创建一个利用电话或平板加速器的游戏，或在设备的文件系统中创建文件）。这些都是正常浏览标准网页浏览器时无法获准访问的功能！如果有人能够从互联网修改你的计算机、平板或手机的文件系统，那么整个星球都将陷入群众歇斯底里。如果你觉得电脑世界现在在病毒和特洛伊木马方面就已经问题多多了，想想如果你访问 Amazon.com 时被一个愤怒的黑客开发者利用其文件系统访问权限删除了你电脑上的所有文件会怎样？是的，我告诉过你，那是群情激奋！这就是为什么正如我们在创建我们的 Twitter 应用程序“Who's That Tweet?”（那是谁发的推？）和“I Love Ham”时讨论的那样，你的浏览器受到了严格的限制。

然而有时确实需要这样的访问权限，而这时就需要像 PhoneGap (http://www.phonegap.com/) 和 Titanium Mobile (http://www.appcelerator.com/products/titanium-mobile-application-development/) 之类的框架发挥作用了。这两种应用程序框架都让开发者可以将现有的 HTML5 和 JavaScript 代码转换为完整的原生应用程序并上传到你选择的任何移动应用商店中。虽然这两个产品都能让你的应用程序走上原生化之路，但它们各自实现的方法截然不同，我觉得值得提一提。

### PhoneGap

PhoneGap 是一个免费且开源的解决方案，就像许多流行的网络开发解决方案一样，它在很短的时间内取得了长足的进步。由 Nitobi Software（尼托比软件）公司在2009年 iPhone Developer Camp（iPhone开发者夏令营）期间为期48小时的编码狂欢中创建出来的 PhoneGap应运而生，并且一直是希望跳入移动开发生态系统而不愿花费大量时间学习新编程语言的网络开发者的宠儿。

随着 Adobe Dreamweaver CS5.5 的最新发布，Adobe 已将 PhoneGap 框架集成到 Dreamweaver 中，这样开发者只需单击鼠标（参见图 13–23）即可创建原生应用程序并在 Android 模拟器中进行测试。与这样一个庞大的开发巨头合作使得 PhoneGaP 在“编写一次到处运行”的移动应用领域对其竞争对手拥有了巨大的优势。

让我们快速查看列于清单 13-1 中的一些来自PhoneGap示例的代码，以便你了解如何构建HTML5 PhoneGap 应用程序的结构。

# **图 13–23**。*配置 Adobe Dreamweaver CS5.5，使用 PhoneGap 将我们的 HTML5 应用程序构建为原生应用程序*

让我迅速看一下一些代码片段，出自 PhoneGap 示例清单 13-1，以便你了解如何构建HTML5 PhoneGap 应用的结构。

# **列表 13–1**。*PhoneGapExample*

```html
<!DOCTYPE HTML>
<html>
<head>
<meta name="viewport" content="initial-scale=1.0, user-scalable=no, width=device-width">
<title>Training App</title>
<link rel="stylesheet" href="assets/css/master.css" type="text/css" media="screen" />
<script src="phonegap.js" type="text/JavaScript" charset="utf-8"></script>
<script src="assets/js/xui.js" type="text/JavaScript" charset="utf-8"></script>
<script src="assets/js/lawnchair/adaptors/LawnchairAdaptorHelpers.js" type="text/JavaScript" charset="utf-8"></script>
<script src="assets/js/lawnchair/adaptors/DOMStorageAdaptor.js" type="text/JavaScript" charset="utf-8"></script>
<script src="assets/js/lawnchair/adaptors/WebkitSQLiteAdaptor.js" type="text/JavaScript" charset="utf-8"></script>
<script src="assets/js/lawnchair/Lawnchair.js" type="text/JavaScript" charset="utf-8"></script>
<script src="assets/js/dsl.js" type="text/JavaScript" charset="utf-8"></script>
<script src="assets/js/app.js" type="text/JavaScript" charset="utf-8"></script>
</head>
<body>
<div id="title_bar">Phone<strong>Gap</strong> Training App</div>
<div id="welcome" class="view">
<div class="app_button" id="map_button">显示我的位置</div>
<div class="app_button" id="settings_button">设置</div>
</div>
<div id="map" class="view">
<div class="map_image"><img id="static_map" src="assets/img/staticmap.png"></div>
```



<p>这就是你当前的位置</p>
<div class="app_button" id="welcome_button">返回</div>
</div>
<div id="settings" class="view">
<form id="settings_form">
<fieldset>
<legend> 地图类型 </legend>
<input type="radio" name="map" value="roadmap" checked> 道路地图<br/>
<input type="radio" name="map" value="satellite"> 卫星地图<br/>
<input type="radio" name="map" value="terrain"> 地形图<br/>
<input type="radio" name="map" value="hybrid">

正如你从前文的"百宝箱"示例中所见，这里并没有太多与你通常构建页面的方式不同的地方。就所有实际目的而言，这是一个HTML文档，而这正是PhoneGap相比于其竞争对手开始显得不足的地方。你看，在手机上使用PhoneGap应用时，即使这个应用现在是原生应用，并且能够通过权限接入操作系统——这是普通基于互联网托管的Web应用永远无法获得的——你仍然只是在设备上加载一个网页。在大多数情况下这没问题，但在Android设备上，我们必须承认其浏览器并不像iPhone浏览器那样支持硬件加速；所以，如果你的应用中有大量华丽的效果和动画，它仍然会像在浏览器中查看时一样缓慢和迟钝。仅仅因为你将应用封装得可以称之为"原生"，它并非真正意义上的原生。这时，我最喜欢的移动平台就登场了：Titanium Mobile！

### Titanium Mobile

多年来，我一直是Appcelerator团队使用Titanium Mobile所做工作的大力支持者。他们最初采取了与PhoneGap相同的方法，允许用户使用纯HTML和JavaScript创建内容，但很快意识到，为了提升性能和速度，有时最好完全采用原生方式。大约在Titanium Mobile软件成熟到生产就绪的1.0版本时，Appcelerator发布了一套新的API，这些API仍然允许开发者使用HTML5在WebView中创建应用，但新增的功能是，开发者现在可以完全跳过HTML5，直接用纯JavaScript创建应用。

通过这种方式，他们能够在构建时获取这些JavaScript文件，并使用操作系统自身的代码来生成页面布局，从而将它们完全转换为*真正的*原生应用。这意味着，你不必在应用中创建自己的一套按钮或样式，而是可以使用对应平台的原生用户界面元素，让你的应用看起来更像一个真正的原生应用。

为了不被PhoneGap与Adobe Dreamweaver的集成所比下去，Appcelerator的好伙伴们收购了集成开发环境（IDE）公司Aptana，并为自己开发了一个功能齐全的IDE来配合其框架使用。自Titanium Studio于2011年初发布以来，使用Titanium Mobile环境变得轻而易举。

虽然Titanium Mobile是一个开源项目，可以免费使用，但也有一些特殊模块仅向付费客户提供。成为Titanium Mobile的付费客户有其特权，比如可以提前访问更新版本的Titanium Mobile，以及使用能让你接入AdMob（应用内广告）和Paypal（应用内购买）等公司API的模块。成为Titanium Mobile的订阅会员对钱包也很友好，提供免费的基础会员制，付费会员制则从每月$49.99起步。

如果你负担得起，并且想要访问像GameKit和OpenGL游戏模块这样的特定模块，那么选择基础独立计划是毋庸置疑的。如果你只是想摆弄一下这个软件，创建没有花哨模块的应用，那也可以，并且完全免费！通过Titanium Mobile，你将能够使用纯JavaScript或HTML5与JavaScript的组合，在短时间内创建出真正令人惊叹的移动应用。

## 闭幕时刻

既然我们已经经历了进入移动开发领域所需了解的一切，现在是时候说再见、关灯、然后缓缓走开了，同时远处某个地方会响起70年代末期电视剧《不可思议的浩克》的主题曲钢琴演奏。我们非常享受与你分享所有这些知识和信息，并希望你能在不久的将来利用它，将自己转变为一个10级的网络萨满，击败任何挡在路上的棘手开发状况。我们确信你现在正咧嘴笑着，准备跳上电脑开始编写你的下一个项目，而我们也咧嘴笑着，因为我们为你感到兴奋；但在今天离开你之前，我们要再次提醒你一条近二十年前给过Rocco的友好建议——保持简单，笨蛋！

感谢你花时间阅读这本书，如果你碰巧认识任何能从这本关于移动Web开发的著作中受益的新兴开发者，那么请随意将你的副本借给他们，将这份知识和信息传递给其他人。保重，编程愉快！

— Jon, Rocco, 和 Grant

# 索引

## A, B

- Adobe Dreamweaver CS5.5
  - 压缩
    - 压缩、混淆且难以理解的jQuery代码, 236
    - 未压缩的jQuery脚本, 235
  - HTML5 Boilerplate, 240
  - PhoneGap, 256

- Adobe Fireworks
  - 设计稿, 143, 144
  - 在Windows 7平台上, 141
  - 页面面板, 142

高级音频编码 (AAC), 191

Android 2.3网页浏览器, 32

- Android的地理位置世界, 155
  - checkIn()函数, 156
  - 地理位置跟踪, 158
  - PERMISSION_DENIED错误, 156
  - position.coords.accuracy, 155
  - position.coords.altitude, 155
  - position.coords.heading, 158
  - position.coords.latitude, 155
  - position.coords.longitude, 155
  - position.coords.satellites, 155
  - position.coords.speed, 速度
  - POSITION_UNAVAILABLE错误, 156, 157
  - supportsGeo()函数, 155
  - TIMEOUT错误, 156
  - UNKNOWN_ERROR, 156
  - watchPosition()方法, 158

API. 参见 应用程序编程接口 (API)

### 应用程序打包

- 压缩
  - 压缩、混淆且难以理解的jQuery代码, 236
  - 描述, 233–234
  - jQuery 1.6.2. 文件大小检查, 235
  - 工具和实用程序, 236–240
  - 未压缩的jQuery脚本, 235

特性, 254–255

- FTP应用程序
  - 部署应用程序, 248–252
  - 描述, 246
  - FileZilla, 247

Git, 253–254

- 主机解决方案
  - 1and1, 245
  - Dreamhost, 243–245
  - 评估, 241–242
  - Media Temple, 245–246

PhoneGap, 255–257

软件版本控制, 252–254

Titanium Mobile, 258–259

### 应用程序编程接口 (API)

- 音频数据, 196
  - Android 2.3.4姜饼设备, 196
  - 描述, 196
  - HTML5, 196

定义, 21

- 音乐服务
  - Amazon的产品广告API, 207–208

- 描述, 202

Last.fm, 203–206

异步JavaScript和XML (AJAX)

异步传输
- Android操作系统, 214
- 开始我的搜索, 213
- 描述, 211
- false设置, 230–231
- 闪存视频, 215
- Google搜索主页, 212

描述, 211

JavaScript和XML, 215–216

POST与GET, 230

RSS订阅源, 220
- JSON输出并显示它, 224–226
- Pipes创建, 221–224

用户名可用性
- 检查用户名页面, 228
- check_name.php脚本, 227–228
- 检查代码, 229
- checkname.html页面, 228
- 描述, 226
- 不可用屏幕, 229
- 用户表, 227
- 验证和表单
  - 自动提交, 229

每日一词应用程序
- Android网页浏览器, 219–220
- onreadystateJavaScript函数, 217
- readyState和status, 218
- request.send()函数, 218
- word.txt文件, 216–217

Audacity音频编辑器
- 编辑, 192
- 导出选项, 195
- LAME MP3库下载页面, 194
- 首选项对话框, 193

音频，移动Web应用
- audacity音频编辑器
  - 编辑, 192
  - 导出选项, 195
  - LAME MP3库下载页面, 194
  - 首选项对话框, 193
- 音频编解码器
  - AAC, 191
  - MP3, 190–191
  - Ogg, 191

音频数据API
- Android 2.3.4姜饼设备, 196
- 描述, 196
- HTML5, 196

描述, 187

HTML5音频标签
- Android姜饼2.3设备, 189
- 属性, 188
- 元素, 188
- 集成, 189–190

音乐服务API
- Amazon的产品广告API, 207–208
  - 描述, 202
- Last.fm, 203–206

## C

- CartoDB, 164

层叠样式表 (CSS)
- 家庭杂务清单, 3
- 框架, 130–131
  - 320 and Up, 133–135
  - 生物素描，框架比较, 135–140
  - Less Framework 4, 132–133
  - 1140px Grid, 131
- HTML标签, 5
- 爱国杂务清单, 4

基站三角定位, 146

ChangeDiv()函数, 154

CheckIn()函数, 154, 156

CloudMade, 164

编解码器
- 音频
  - AAC, 191
  - MP3, 190–191
  - Ogg, 191



### 描述，190

MP3，190–191

Ogg，191

视频

h.264/MPEG4，199

Ogg Theora，199

WebM，199–200

### 压缩

- 经过压缩、混淆且难以理解的jQuery代码，236

#### 描述，233–234

#### jQuery 1.6.2 文件大小检查，235

### 工具和实用程序

- 应用程序，238
- HTML5 Boilerplate，239–240
- YUI 压缩工具，236–237
- 未压缩的 jQuery 脚本，235

## deviantART，124–125

## 文档对象模型（DOM），36，147

## Dreamhost

- 描述，243
- VPS，244–245

## Droid Sans 字体，29，127

## 可扩展标记语言（XML）

- 交互，10
- 我的个人博客，9–10
- RSS 订阅源，8–9
- RSS 图标，8

## FAILboard Pro，54–55

## 文件传输协议（FTP）应用程序

Cyberduck，248

部署应用程序，248–252

描述，246

## FileZilla

- 描述，247
- 创建目录，250–252
- 主机连接信息，249
- 未知主机密钥提示，250
- 无需配置，249

SFTP，248–252

## FileZilla

- 描述，247
- 创建目录，250–252
- 主机连接信息，249
- 未知主机密钥提示，250
- 无需配置，249

Find Icons 搜索引擎，123

字体问题，129–130

## 地理位置

- 应用，151–152
- changeDiv() 函数，154
- checkIn() 函数，154
- HTML 复习，153
- navigator.geolocation.getCurrentPosition()，154
- supportsGeo() 函数 Redux，153
- 工具函数，153
- 信号塔三角测量，146
- 桌面浏览器地理位置支持测试，149
- 文档对象模型（DOM），147
- 全球定位系统（GPS），146
- IP 地址分配，146
- 移动浏览器地理位置支持测试，149
- 设置，147
- 简单地理位置支持，148，150
- 追踪，158
- WiFi 三角测量，146

## 地理位置

- Google 地图，160–163
- 基于位置的服务，163
  - CartoDB，164
  - CloudMade，164
  - Mapnik，164
  - Mapstraction，164
  - Open Street Map，164
  - 优缺点，163–164
  - Wax，164
- Google Nexus One，89–90
- Google 网页字体，128–129
- GPS。请参阅 *全球定位系统（GPS）*

## H

- .htaccess 用户代理检测，97–98
- h.264，199
- 主机解决方案
  - 1and1，245
  - 评估，241–242
  - Media Temple，245–246
- HotGloo，58–59
- HTML。请参阅 *超文本标记语言（HTML）*
- HTML5
  - 音频标签
    - Android 2.3 姜饼设备，189
    - 属性，188
    - 元素，188
  - 视频标签
    - Android 2.3.4 姜饼设备，198
    - 属性，198
    - 元素，197
    - 功能，198
- HTML5 Boilerplate
  - 配置，240
  - 描述，239
  - 结构，239
- HTML5 基于位置的应用程序
  - Android 的地理位置世界
    - checkIn() 函数，156
    - 地理位置追踪，158
    - PERMISSION_DENIED 错误，156
    - position.coords.accuracy，155
    - position.coords.altitude，155
    - position.coords.heading，158
    - position.coords.latitude，155
    - position.coords.longitude，155
    - position.coords.satellites，155
    - position.coords.speed，158
    - POSITION_UNAVAILABLE 错误，156，157
    - supportsGeo() 函数，155
    - TIMEOUT 错误，156
    - UNKNOWN_ERROR，156
    - watchPosition() 方法，158
- 地理位置，145
  - 信号塔三角测量，146
  - 桌面浏览器地理位置支持测试，149
  - 文档对象模型（DOM），147
  - 全球定位系统（GPS），146
  - IP 地址分配，146
  - 移动浏览器地理位置支持测试，149
  - 设置，147
  - 简单地理位置支持，148，150
  - WiFi 三角测量，146
- 地理位置应用程序，151–152
  - changeDiv() 函数，154
  - checkIn() 函数，154
  - HTML 复习，153
  - navigator.geolocation.getCurrentPosition()，154
  - supportsGeo() 函数 Redux，153
  - 工具函数，153
- Google 地图，160–163
  - 基于位置的服务，163–164
- 位置游戏，164–166
- 人类可读数据交换，10–11
- 超文本标记语言（HTML）
  - body 标签，2
  - 代码，2
  - 描述，1
  - 页面页头，2
  - 复习，153

## I Love Ham

- CSS，41–43
- HTML 标记，39–41
- JavaScript，43–48
- Web 应用程序，21

## Iconfinder，121–122

## 图标

- Find Icons 搜索引擎，123
- Iconfinder，121–122

## Init() 函数，36

## 互联网应用程序

- Adobe Fireworks，141
  - 设计稿，143，144
  - 在 Windows 7 平台上，141
  - 页面面板，142
- CSS 框架，130–131
  - 1140px Grid，131
  - 320 and Up，133–135
  - 框架比较，135–140
  - Less Framework 4，132–133
- 图标
  - Find Icons 搜索引擎，123
  - 图标用途，收藏夹图标，123–124
  - Iconfinder，121–122
- 素材照片
  - deviantART，124–125
  - iStockphoto，125–126
  - 照片使用规则，126
- 网页字体
  - Droid Sans 字体，127
  - Google，128–129
  - 问题，129–130

## IP 地址分配，146

## iStockphoto，125–126

## JavaScript，网页设计，6–8

## JavaScript 对象表示法（JSON），10–11

带填充，22

## JavaScript 用户代理检测

- 检测代码，92–93
- 单平台开发者，94
- Android 浏览器，96
- 应用 HTML 页面，94–95
- Safari，97

## jQuery JavaScript 框架，33

## jQuery Mobile

- 动画，109
- Avery 原生外观用户界面，102
- 内容 data-attribute，101
- 对话框，111–113
- 功能，100
- HTML 标记，101
- 无效的自定义 mood 属性，100
- 多页，102
  - 关于和联系页面，106–107
  - 关于页面，108
  - 联系页面，109
  - 内容，103
  - 计数气泡列表，104
  - 页脚，105
  - 表单元素，105
  - 首页，107
  - 嵌入式搜索字段，104
  - 嵌套列表，104
  - 搜索过滤框，105
  - 缩略图和图标列表，104
  - 过渡和主题属性，105
- UI 元素，102

### Simple Calc，118–120

### ThemeRoller，113

- Adobe kuler 色板，116
- 配置，116
- 自定义选项，115
- 下载主题窗口，117
- 我的自定义主题，117
- 启动屏幕，114
- 过渡页面，109–111
- 有效的 data-mood 属性，100

JSON。请参阅 *JavaScript 对象表示法（JSON）*

## Less Framework 4，132–133

## 位置游戏，164–166

## 基于位置的服务

- CartoDB，164
- CloudMade，164
- Mapnik，164
- Mapstraction，164
- Open Street Map，164
- 优缺点，163–164
- Wax，164

## M

- MapMe() 函数，162
- Mapnik，164
- Mapstraction，164
- META 标签
  - 描述，85
  - 历史，86
  - 视口元素，86
    - Android Webkit 浏览器，89
    - 代码添加，88
    - 描述，86
    - 设备像素密度，89
    - 缩放值，88
    - 关闭 user-scalable，88–89
    - Who's That Tweet 游戏，87
- 移动界面
  - 移动策略，56
  - 原生应用程序，54–55
  - Web 应用程序，56
  - 网站，55–56
- 移动 Web 应用程序
  - 3G 技术，11–12
  - 音频
    - audacity 音频编辑器，192–195
    - 音频编解码器，190–192
    - Audio Data API，196–197
    - HTML5 音频标签，188–189
    - 集成，189–190
    - 音乐服务 API，202–208
  - 概念，15
    - 保持简单，愚蠢（KISS），17–19
    - 盈利，16

## N

- 重测信度，17
- 像用户一样思考，16
- 外部关键词工具，50，51
- Google 关键词搜索，51
- KISS 原则，18
- 语言和协议，12
  - 桌面视图，我的博客，14
  - 移动视图，我的博客，15
  - 掌上电脑，12–14
  - WAP，14
- 部分关键词创意列表，51
- 规划
  - 描述，53
  - FAILboard Pro，54–55
  - 移动策略，56
  - 移动网站，55–56
  - 原生应用程序，54–55
  - Web 应用程序，56
- 结构化
  - 代码结构，60–62
  - 粗略模型，58
  - 描述，57
  - 文件夹结构，62–63
  - HotGloo，58–59
  - 线框图/模型，57–58
- Twitter，19
- 用户移动，59–60
- 用户，51
  - 年龄分布，53
  - 描述，52
  - 虚构的交通应用程序，52
- 视频
  - 描述，197
  - Handbrake，200–202
  - HTML5 视频标签，197–198
  - 视频编解码器，199–200
- 网页设计
  - CSS，3–5
  - HTML，1–3
  - JavaScript，6–8
  - JSON，10–11
  - XML，8–10
- Move Me 应用程序
  - 全局状态变量，173
  - 限制，181
  - 本地交通搜索，176–177



# 索引

## 267

- 位置标记自定义，173–174
- 地图准备，174–176
- 运行代码，177–179
- 源代码，169–172
- 交通可能性，180
- 使用专用交通按钮，180

MP3, 190–191
MPEG-4, 199

## 音乐服务 API

- 亚马逊产品广告 API
    - 描述，207
    - iObjects 代码示例，208
- Last.fm
    - API 请求文档，205
    - 描述，203
    - 播放记录流程，206
    - 网络服务页面，204

## O

- Ogg
    - 音频编解码器，191
    - 视频编解码器，199
- Open Street Map，164

## P, Q

Packer，238
个人数字助理（PDA），12–14
PhoneGap，255–257
Web 应用的照片使用规则，126
PHP 用户代理检测，91–92
1140px 网格，131

## R

- RSS 订阅源，220
    - JSON 输出及显示，224–226
    - Pipes 创建，221
        - 完成的 Pipe，223–224
        - 编辑器，222
        - Fetch Site，222
        - 主页，221
        - 模块，222
        - Truncate，222
        - Union，222

## S

- 屏幕分辨率，CSS 3, 65
- Daily Droid 报纸
    - CSS 代码，74–79
    - HTML 代码，72–74
- 480 x 859 分辨率，71
- 859 x 480 分辨率，72
- 1024 x 600 分辨率，69
- 1280 x 800 分辨率，70
- 2048 x 1536 分辨率，70
- 1024 x 600 分辨率下的固定宽度网页，66
- 2048 x 1536 分辨率下的固定宽度网页，66, 67
- 1024 x 600 分辨率下的弹性宽度网页，67
- 2048 x 1536 分辨率下的弹性宽度网页，68
- 媒体查询，79–83
- 视频图形阵列（VGA），65

Simple Calc，118–120
软件版本控制，252–254
- 素材照片
    - deviantART，124–125
    - iStockphoto，125–126
    - 照片使用规则，126

- 构建移动 Web 应用
    - 代码结构，60
    - footer.php 文件，61
    - HTML 文档，62
    - PHP Include 语句，61
    - 初步草图，58
    - 描述，57
    - 文件夹结构，62–63
    - HotGloo，58–59
    - 线框图/模型，57–58

SupportsGeo() 函数，Redux，153

## T

- ThemeRoller，113
    - Adobe kuler 色板，116

## U

- Uniform Server 开发环境，22
    - 默认 WWW 文件夹视图，25
    - 菜单，24
    - Pre-Check 应用程序，23
    - 快速帮助文档，25

## 用户代理，浏览器平台

- 描述，89
- JavaScript，92
    - 检测代码，92–93
    - 单平台开发者，94–97
- PHP，91–92
- 欺骗，90

实用函数，动态页面更改，153

## V

视频图形阵列（VGA），65

- 视频，移动 Web 应用
    - 编解码器
        - h.264/MPEG-4, 199
        - Ogg Theora, 199
        - WebM, 199–200
    - 描述，187, 197
    - Handbrake
        - 描述，200
        - 在 Windows 7 操作系统中，200
        - iPhone 和 iPod Touch 预设配置设置，202
        - 设置，201
    - HTML5 视频标签
        - Android 2.3.4 Gingerbread 设备，198
        - 属性，198
        - 元素，197
        - 特性，198

- Viewport 元素
    - Android Webkit 浏览器，89
    - 代码添加，88
    - 描述，86
    - 设备像素密度，89
    - 缩放值，88
    - 用户可缩放关闭，88–89
    - Who’s That Tweet 游戏，87

虚拟专用服务器（VPS），244–245

- Patriotic Chore 列表，4
    - HTML
        - body 标签，2
        - 代码，2
        - 描述，1
        - 页面标题，2
    - JavaScript，6–8
    - JSON，10–11
    - XML
        - 交互，10
        - 我的个人博客，9–10
        - RSS 订阅源，8–9
        - RSS 图标，8

- Web 字体
    - Droid Sans 字体，127
    - Google，128–129
    - 问题，129–130
- Webkit，28
- WebM，199–200

- Who’s That Tweet?
    - CSS 文件，27–33
    - HTML 标记，26–27
    - JavaScript，33–37
    - 带填充的 JSON，22
    - Uniform Server 开发环境，22
        - 默认 WWW 文件夹视图，25
        - 菜单，24
        - Pre-Check 应用程序，23
        - 快速帮助文档，25

WiFi 三角定位，146
线框图/模型，57–58

## W

- WatchPosition() 方法，158
- Wax，164
- Web 浏览器平台
    - META 标签
        - 描述，85
        - 历史，86
        - viewport 元素，86–89
    - 用户代理
        - .htaccess，97–98
        - 描述，89
        - Google Nexus One，89–90
        - JavaScript，92–97
        - PHP，91–92
        - 欺骗，90

- Web 设计
    - CSS
        - Family Chore 列表，3
        - HTML 标签，5

## X, Y, Z

XML。参见可扩展标记语言（XML）
XSS。参见跨站脚本（XSS）

# Android Web 应用开发入门

使用 HTML5、CSS3 和 JavaScript 为 Android 进行开发

Jon Westfall
Rocco Augusto
Grant Allen

Apress

# Android Web 应用开发入门：使用 HTML5、CSS3 和 JavaScript 为 Android 进行开发

版权所有 © 2012 Jon Westfall, Rocco Augusto, Grant Allen

本作品受版权保护。无论材料的全部还是部分，所有权利均由出版商保留，特别是翻译权、转载权、插图重用权、朗诵权、广播权、微缩胶片或其他任何物理方式的复制权，以及以信息存储和检索、电子改编、计算机软件或类似或不同的方法（无论是现在已知或将来开发）进行传输的权利。与此法律保留相关的是用于评论或学术分析的简短摘录，或专门为在计算机系统上输入和执行而提供的材料，仅供作品购买者独家使用。仅在出版商所在地版权法现行版本的规定下，才允许复制本出版物或其部分内容，并且必须始终获得 Springer 的许可。可通过版权结算中心的 RightsLink 获得使用许可。违反者将根据相应的版权法受到起诉。

ISBN-13 (pbk): 978-1-4302-3957-4
ISBN-13 (electronic): 978-1-4302-3958-1

本书中可能出现商标名称、标志和图像。我们不会在每次出现受商标保护的名称、标志或图像时都使用商标符号，而是仅以编辑方式并为商标所有者的利益使用这些名称、标志和图像，无意侵犯商标。

本出版物中使用商品名称、商标、服务标志和类似术语，即使未明确标识，也不应被视为表达了关于其是否受专有权约束的观点。

虽然本书中的建议和信息在出版之日被认为是真实和准确的，但作者、编辑和出版商均不对可能犯下的任何错误或遗漏承担任何法律责任。出版商对本文包含的材料不作任何明示或暗示的保证。

> 献给我的妻子 Karey，以及我的父母 Alan 和 Dianne
> ——Jon Westfall

> 我将此书献给我的女儿 Rose……以及 Perry White，他是一位如此优秀的记者，不可能不知道 Clark Kent 就是超人。Perry，你是一块真正的瑰宝。
> ——Rocco Augusto

# 目录

- **速览目录** iv
- **关于作者** ix
- **关于技术审校者** x
- **致谢** xi
- **简介** xii

## 第 1 章：驾驭移动 Web 的力量 1

- Web 设计基础
    - 入门：超文本标记语言（HTML）
    - 添加样式：层叠样式表（CSS）
    - 实现交互：JavaScript
    - 获取信息：可扩展标记语言（XML）
    - JSON：人类可读的数据交换
- 移动 Web，过去与现在
    - 了解速度（或者“3G 到底是什么？”）
    - 语言和协议，过去与现在
- 我们喜欢的概念——以及未来展望！
    - 概念 1：像用户一样思考
    - 概念 2：不要惹恼用户
    - 概念 3：测试-重测可靠性
    - 概念 4：保持简单，笨！（Keep it Simple, Stupid!）
- 即将到来

## 第 2 章：Twitter 应用：Who's That Tweet？ 21

- JSONP
- 搭建你的开发环境
- 你的第一个移动 Web 应用
- 总结

## 第 3 章：Twitter 应用：I Love Ham 39

- HTML
- CSS
- JavaScript
- 总结



■ 目录

## ■ 第4章：应用程序的基础规划与架构

-   了解你的受众
-   给人们想要的
-   谁是我的用户？
-   制定计划
-   并非所有移动设备都相同
-   构建你的应用程序结构
-   用户移动：导航或故事板
-   构建你的开发结构
-   代码结构
-   文件夹结构
-   总结

## ■ 第5章：使用 CSS 3 处理多种屏幕分辨率

-   疲劳眼睛的历史与分辨率演进
-   The Daily Droid 应用
-   The Daily Droid 的基础 HTML 代码
-   The Daily Droid 的半魔法 CSS 代码
-   媒体查询
-   总结

## ■ 第6章：处理不同的浏览器平台

-   META 标签与视口
-   一点 META 历史
-   视口元素
-   用户代理
-   Nexus One 的用户代理
-   PHP 用户代理检测
-   JavaScript 用户代理检测
-   JavaScript 代理检测代码介绍
-   .htaccess 用户代理检测
-   总结

## ■ 第7章：使用 jQuery Mobile 构建令人印象深刻的用户体验

-   基础知识
-   添加多个页面
-   那么——关于那些过渡效果
-   来创建一个对话框
-   使用 ThemeRoller 创造你自己的主题
-   整合一切：简单计算器
-   总结

## ■ 第8章：构建视觉丰富的互联网应用

-   寻找并使用图标和库存图片
-   Iconfinder 网站
-   查找图标
-   使用图标
-   deviantART 社区
-   iStockphoto 图库
-   Web 应用中使用照片的指南

vi

网页字体
-   Google 网页字体
-   需要考虑的字体问题

CSS 框架
-   1140px 网格
-   Less Framework 4
-   320 and Up
-   框架比较：关于 Jon！！

Adobe Fireworks

总结

## 第9章：HTML5 基于位置的应用

地理定位的原理
-   理解设备能力
-   理解 HTML5 能力
-   检测浏览器的地理定位支持

探索我们的示例应用
-   构建我们的基础地理定位应用
-   处理 Android 地理定位世界的四大难题

使用地图扩展你的视野
-   为我们的应用添加地图

玩转你的位置
-   玩转你的位置——为了乐趣！

总结

## 第10章：使用云服务：一个交通应用

介绍“Move Me”示例应用
-   检查代码
-   处理全局状态
-   自定义位置标记
-   准备我们的地图
-   执行本地交通搜索
-   运行我们的代码

改进“Move Me”示例应用
-   处理其他交通可能性
-   我们方法的局限性

介绍交通数据资源
-   利用交通时刻表和时间表
-   探索 GTFS 示例

总结

## 第11章：挑战音频与视频的极限

移动 Web 应用的音频
-   利用 HTML5 audio 标签
-   将音频集成到“这是谁的推文？”应用中
-   处理音频编解码器
-   使用 Audacity 音频编辑器
-   音频数据 API

为移动应用添加视频
-   使用 HTML5 video 标签



# 目录

编解码器 ........................................................................................................... 199
使用 Handbrake 转码视频 ................................................................... 200
自主探索：音乐服务 API .............................................................. 202
    将曲目“Scrobble”到 Last.fm ............................................................................. 203
    利用亚马逊产品广告 API 的强大功能！.................................... 207
总结 ............................................................................................................... 209

## 第 12 章：通过 AJAX 增强用户体验 ......................... 211

-   什么是 AJAX？ .................................................................................................. 211
    异步？ ................................................................................................. 211
    那么 JavaScript 和 XML 呢？ .............................................................. 215
每日 AJAX ................................................................................................ 216
我的新闻！ ............................................................................................................ 220
    首先：创建一个管道 ........................................................................................... 221
    其次：获取输出并显示它！.................................................................. 224
用户名可用性检查 ........................................................................................... 226
AJAX 考量 ........................................................................................... 229
    POST 与 GET 对比 ................................................................................................... 230
    将异步设置为 False？............................................................................ 230
总结 ............................................................................................................... 231

## 第 13 章：打包你的应用 ...................................................... 233

-   压缩你的应用 .............................................................................. 233
    什么是压缩？ ......................................................................................... 234
    压缩工具和实用程序 ............................................................................ 236
寻找托管解决方案 ................................................................................... 241
    评估托管服务商 ............................................................................... 241
    1and1 ............................................................................................................... 245
文件传输协议 ........................................................................................... 246
    使用安全 FTP 部署应用 ............................................................. 248
软件版本控制 ..................................................................................... 252
走向原生 ........................................................................................................ 254
    PhoneGap ........................................................................................................ 255
    Titanium Mobile .................................................................................................. 258
闭幕时刻 ........................................................................................................ 259

## 索引 .............................................................................................................. 261

## 关于作者

![](img/8b0ff5e51ddb912cd941bb18cf27206a_275_0.png)

**Jon Westfall** 是一位在纽约市哥伦比亚商学院工作的研究员和技术专家。他目前的职位是哥伦比亚商学院决策科学中心的研究与技术副主任，该中心隶属于纽约市哥伦比亚大学。此外，他还被任命为哥伦比亚大学心理学系的讲师，定期教授判断与决策课程。除了研究工作，他的职业生涯还与信息技术紧密相连，自1997年以来一直担任顾问，并创立了自己的公司 Bug Jr. Systems。作为一名顾问，他开发了定制的软件解决方案（包括原生 Windows 32 应用程序、Windows .NET 应用程序、Windows Phone 7 和 Android 移动应用程序，以及 ASP、ASP.NET 和 PHP Web 应用程序）。他还曾担任高级网络和系统架构师及管理员（负责 Windows 和 Unix 网络及其混合环境），并曾被评为微软最有价值专家（MVP）2008 – 2012。在业余时间，他喜欢撰写技术书籍和小说。他的小说《Mandate》以及其他作品可通过他的网站 http://jonwestfall.com 获取。你可以通过他的网站联系他，并在 Twitter 上关注他（@jonwestfall）。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_275_1.png)

**Rocco Augusto** 是一位总部位于“玫瑰之城”——俄勒冈州波特兰市的网络开发者。Rocco 在中学时首次接触网页设计与开发的艺术，编程的“虫子”咬了他，从此拒绝松口。当不在捣鼓新的标记或设计创意时，你通常可以发现 Rocco 正在享受与他美丽的妻子、女儿们以及他们不听话的小狗们共度的时光。

![](img/8b0ff5e51ddb912cd941bb18cf27206a_275_2.png)

**Grant Allen** 在 IT 领域工作超过 20 年，曾担任 CTO、企业架构师和数据库管理员。Grant 的角色涵盖私营企业、学术界和全球政府部门，专注于全球规模系统的设计、开发和性能。他是行业和学术会议的常客，演讲主题涵盖从数据挖掘到合规性，以及数据库（DB2、Oracle、SQL Server、MySQL）、内容管理、协作、颠覆性创新和 Android 等移动生态系统等技术。他的第一个 Android 应用程序是一个任务列表，用来提醒他完成所有其他未完成的 Android 项目。Grant 就职于 Google，业余时间正在完成关于构建创新高科技环境的博士学位。Grant 是《Beginning DB2》的作者，也是《Beginning Android 4》、《Oracle SQL Recipes》和《The Definitive Guide to SQLite》的首席作者。

## 关于技术审阅者

![](img/8b0ff5e51ddb912cd941bb18cf27206a_276_0.png)

**Steven Hughes** 在过去十年一直是微软 Windows Phone MVP，他对移动社区充满热情和奉献精神。Steven 从90年代初就开始接触掌上电脑，包括参与多款硬件和软件设计的 beta 测试和原型设计。他对移动技术和移动行业的热情与知识为许多人提供了建议和咨询，并因此获得了“fyiguy”的昵称。Steven 热衷于分享信息和帮助他人；你可能会在多个与移动技术相关的网站、出版物、播客和其他制作中看到他的贡献和文章。Steven 还是 BostonPocketPC.com 的首席新闻和评论编辑，撰写了几篇关于移动技术各个方面的详细评论和文章。Steven 是微软答案论坛的版主，并共同管理新英格兰 Windows Phone 用户组。Steven 受雇于 VA 新英格兰医疗保健系统，担任生物医学工程师。空闲时间，他通常与家人在一起，或在户外踢足球、滑雪、弹吉他、在他的自建家庭影院看电影，或骑山地自行车沿着小径骑行。

## 致谢

我要感谢 Apress 的编辑们（Mark Beckner, Adam Heath, Chris Nelson, & Jonathan Gennick），以及我的合著者 Rocco 和 Grant，还有技术编辑 Steven，感谢他们在这个项目中的辛勤工作。就个人而言，我的妻子 Karey、父母 Alan 和 Dianne，以及我的大家庭（特别是 Dan, Sue, Greg, Scott, & Mark）给予我的支持怎么强调都不为过。我也感谢我的导师 Eric Johnson 和 Elke Weber，我的同事 Cindy Kim, Margaret Lee, Ye Li, Christoph Ungemach, Soo Baik, Galen Treuer, 和 Min Bang，以及我过去和现在的实习生 Katherine Chang, Meaghan Gartner, Mary Reiser, Yechao Liu, Soo Jung Lee, & Nina Rouhani 的支持。最后，我要感谢我的朋友们，他们直接或间接地鼓励我变得像现在这样“极客”。这包括 Steve Jocke, Tony Rylow, Ashley Newman, Maria Gaglio, Marie Batteiger, JD Jasper, Jason Dunn, Don Sorcinelli, Eric Hicks, Darius Wey, Jack Cook, Johan van Mierlo, Annie Ma, Holly Feiler, Dot Bertram, & Cathy Bischoff。

—Jon Westfall
