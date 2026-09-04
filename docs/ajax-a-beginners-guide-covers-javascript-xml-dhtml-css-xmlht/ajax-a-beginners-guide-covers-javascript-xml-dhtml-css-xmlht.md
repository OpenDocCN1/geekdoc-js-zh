
# Ajax 初学者指南

涵盖内容：

JavaScript • XML • DHTML • CSS • XMLHttpRequest 对象 • PHP

---

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_1_0.png)

# 关于作者

史蒂文·霍兹纳是一位屡获殊荣的计算机图书作者和网络创业者，已出版超过 100 本著作，涵盖 18 种语言，销量超过 300 万册。他广泛撰写了关于 Ajax 的文章，并在自己的网站上日常使用 Ajax。他曾在康奈尔大学和麻省理工学院任教。

# 关于技术编辑

吉姆·基奥于 1982 年在《大众电子杂志》专栏中首次向全国推广 PC 编程。他所在的团队曾为华尔街公司构建了首批 Windows 应用程序之一，并在 1986 年受到比尔·盖茨的赞誉。他花费了近二十年时间为所罗门公司和贝尔斯登公司等华尔街公司开发计算机系统。

基奥目前在纽约大学任教，并且是《J2EE：完整参考手册》和《J2ME：完整参考手册》的作者，这两本书均由麦格劳-希尔出版。此外，他还撰写了超过 55 部其他著作。

---

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_4_0.png)

# 献给南希

# 简介

本书致力于让网络应用在外观和行为上，都像运行在你电脑上的桌面应用一样。随着我们步入互联网时代，桌面应用与互联网应用之间的区别将不断缩小。迄今为止，桌面应用与基于浏览器的应用之间存在一个主要差异：在浏览器中，你通常需要等待整个页面刷新后才能看到任何结果。

想在线购买一本书？点击那本书——**唰**——购物车页面就出现了。想结账？点击结账按钮——**唰**——那个页面就出现了。接着又是——**唰**——信用卡信息页面。

所有这些“唰”的闪烁，让在线应用的感觉与电脑上的应用截然不同。Ajax 背后的理念，就是消除困扰在线体验的页面闪烁刷新。通过 Ajax，你可以在后台连接到网络服务器，下载数据，然后在浏览器当前页面中显示这些数据，而无需刷新页面。

这就是网络开发的未来——创造一种与使用自己电脑上的程序无异的浏览体验。Ajax 使你能够创造这种体验。

本书将为你提供 Ajax 的全面介绍——你需要知道的一切都在这里。我们将从概述 Ajax 的功能以及当今的应用开始。然后，你会接触到 JavaScript 的介绍，它是 Ajax 在浏览器端的基础（稍后，你会了解网络服务器端）。掌握了 JavaScript 之后，我们将深入 Ajax 本身，向你展示如何创建支持 Ajax 的应用。我们还将探讨一些特殊问题，例如，如何确保发往服务器的两个 Ajax 请求不会相互混淆。

如果你完全排斥编程，还有一种简单的方法来创建 Ajax 应用，那就是使用一套预先写好的代码，称为“AJAX 框架”，来为你完成编程工作。你将看到如何使用一些流行且免费的 Ajax 框架，让一切变得非常容易组装。

通常，你通过 Ajax 从服务器读取的数据是 XML 格式的（它不必如此——也可以是简单文本），因此我们将花一些时间在浏览器中处理 XML，了解如何解码从服务器下载的 XML。

Ajax 的另一个重要部分涉及使用从后台下载的数据，以不引人注目的方式更新网页。我们将看看如何使用动态 HTML 和级联样式表（CSS）来实现这一点。

此外，我们将探讨如何在网络服务器上支持 Ajax。你可以使用 Ajax 下载静态数据文件，但这并不令人兴奋。Ajax 通常涉及服务器端的一些编程，而 PHP 脚本语言是与 Ajax 一起在服务器端最常用的语言，因此你将被介绍 PHP。你可以使用 Ajax 向服务器发送命令和数据，并通过服务器端的 PHP，定制你发送回浏览器的数据。

当你开始完整的 Ajax 世界之旅时，本书将涵盖以上所有内容，甚至更多。

# 本书中使用的惯例

本书使用了一些惯例。例如，当首次引入一个术语时，它会以斜体显示。当引入一段新代码时，它会以粗体显示，比如这个 `<div>` HTML 元素。

你还会发现“动手试试”部分，邀请你自己尝试这些应用，以及“专家问答”部分，为你提供更深入的 Ajax 技术见解。

```html
<body>
    <h1>使用 DOM 和 Ajax 追加元素</h1>
    <form>
        <input type="button" value="下载消息"
               onclick="getData()">
    </form>
    <div id="targetDiv" width="100" height="100">
        <p id="text"></p>
    </div>
</body>
```

# 你需要准备什么

阅读本书，你应该具备良好的 HTML 知识。你不必是 HTML 高手，但你应该知道如何组装一个基本网页。如果本书中默认的 HTML 水平让你感到困惑，请在继续之前先阅读一本好的 HTML 入门书。

就软件方面而言，你需要一个能运行 JavaScript 的浏览器，比如 Internet Explorer 或 Firefox。Ajax 围绕浏览器展开，因此你需要使用互联网浏览器才能有效利用本书并跟随示例学习。

本书中的服务器端编程并非完全必要，因此你不需要理解本书介绍的 PHP。然而，我确实建议你使用一个允许你在线支持 PHP 脚本的互联网服务提供商（ISP）。如果你不进行任何服务器端编程，你的 Ajax 体验将非常有限，只能让你从服务器下载已有的文件。

当你在服务器上使用 PHP 时，你可以从浏览器向服务器发送数据（例如，潜在买家正在搜索的邮政编码），并使用这些数据来定制你发送回浏览器显示的回复。

这就是你需要的一切。现在进入第 1 章，它将让你很好地概览 Ajax 能提供什么。

# 第 1 章：基础 Ajax

## 关键技能与概念

- Ajax 简介
- 实时搜索
- 自动完成
- 拖放
- Ajax 聊天程序

打开你的网络浏览器，访问 Google，网址是 `www.google.com`，在搜索文本框中输入“Ajax”，如图 1-1 所示，然后点击 Google 搜索按钮。

那么会发生什么？浏览器闪烁了一下，显示刷新了，你看到了与搜索词匹配的结果（根据 Google 的说法，在撰写本文时，有高达 66,700,000 条匹配结果），如图 1-2 所示。

![图 1-1 在 Google 中搜索“Ajax”](img/2cd265cf0a64e9b4b91ab611753cd5d5_21_0.png)

很明显，你是在浏览器中工作——当浏览器从互联网下载数据并向你显示这些数据时，显示会闪烁。事实上，整个浏览器窗口在更新时都闪烁了，因为浏览器需要从 Google 网站下载数据。

如果把整个 Google 放在你的家用电脑上，让你在数据下载时避免闪烁，会是什么感觉？换句话说，如果 Google 是一个桌面应用而不是互联网应用，会是什么样子？

你可以通过查看 Google Suggest 来了解其工作原理，网址是 `www.google.com/webhp?complete=1&hl=en`，如图 1-3 所示。

现在在搜索文本框中输入“Ajax”。如图 1-4 所示，Google Suggest 会在屏幕上弹出一个下拉列表，实时显示与你的搜索词匹配的内容。

没有闪烁，没有屏幕抖动。Google Suggest 只是显示了与你输入的词匹配的结果。正如你在图 1-4 中看到的，Google Suggest 不仅显示与你输入内容匹配的词条——它还指示了每个搜索词条的匹配数量。没有闪烁，没有抖动，没有屏幕更新。很酷。

当你从下拉列表中选择一个词条时，浏览器会导航到 Google 并为你查找该词条，显示所有找到的匹配结果。请注意，这次浏览器中有一个页面刷新，显示闪烁了，因为当浏览器导航到 Google 时没有使用 Ajax。

![图 1-3 Google Suggest](img/2cd265cf0a64e9b4b91ab611753cd5d5_23_0.png)

![图 1-4 Google Suggest 为你提供搜索匹配结果。](img/2cd265cf0a64e9b4b91ab611753cd5d5_23_1.png)

如你所见，Google Suggest 让 Google 有了桌面应用的感觉——至少是部分如此：当浏览器导航到 Google 查找你在下拉列表中点击的词条时，屏幕仍然会闪烁（你将在本书后面看到如何将自己的网站连接到 Google Suggest）。

这就是 Ajax 背后的核心思想：将互联网上的交互变得仿佛本地化，就好像应用程序就在你的电脑上一样。

让互联网应用感觉像本地应用，这就是所谓的 Web 2.0 的基础。这是软件设计的下一步：尽管你使用的程序实际上在旧金山，但它感觉就像在纽约市的你自己的电脑上，就像你的文字处理程序或电子表格程序一样。

在本章中，你将熟悉 Ajax 是什么以及它能提供什么。目前有成千上万个支持 Ajax 的网络应用，你将在本章中看到其中的一些良好示例。我们将从确定 Ajax 到底是什么——以及它代表什么——来开始这次调查。

## 什么是 Ajax？

Ajax，全称为异步 JavaScript 和 XML，是一系列用于创建高度交互性网站和网络应用的技术。其理念是通过提供丰富的用户体验，提供通常只在桌面应用中出现的功能，让网络上的内容看起来像是本地的。

Ajax 应用的重点是使用从互联网获取的数据更新网页，而不刷新浏览器中的网页。你在 Google Suggest 中看到了一个例子，浏览器中出现了一个下拉列表，而无需页面刷新。

“Ajax”这个术语由 Adaptive Path 公司总裁 Jesse James Garrett 在 2005 年 2 月 18 日的一篇文章中创造，该文章将已经存在的、构成 Ajax 的技术汇集在一个总称之下。那篇名为《Ajax：Web 应用的新方法》的文章是 Ajax 历史上最重要的一篇，发表在 `www.adaptivepath.com/ideas/essays/archives/000385.php`。

Jesse Garrett 在文章开头这样写道：

> 如果说当前的交互设计中有什么可以称之为“魅力四射”的，那就是创建 Web 应用。毕竟，你上一次听到有人对一个非 Web 产品的交互设计赞不绝口是什么时候？（好吧，除了 iPod。）所有酷炫的、创新的新项目都在网上。
>
> 尽管如此，Web 交互设计师们还是忍不住有点羡慕那些创建桌面软件的同行。桌面应用具有 Web 上似乎无法企及的丰富性和响应性。正是使 Web 得以迅速普及的简洁性，也在我们能提供的体验和用户从桌面应用中能获得的体验之间造成了鸿沟。
>
> 这个鸿沟正在缩小。

他继续写道：

> 这个名字是“异步 JavaScript + XML”的缩写，它代表了网络可能性的一次根本性转变。

Ajax 并非一项技术，而是多项技术的集合，每项技术都自成体系，却以强大的新方式协同工作。Ajax 融合了：

- 基于 XHTML 和 CSS 的标准化呈现；
- 利用文档对象模型实现动态显示与交互；
- 基于 XML 和 XSLT 的数据交换与操作；
- 借助 `XMLHttpRequest` 实现异步数据检索；
- 以及通过 JavaScript 将一切整合在一起。

换言之，Ajax 是一个总称，涵盖了你用于让 Web 应用程序看起来像桌面应用程序的各种技术。其工作原理如下：在浏览器中，用脚本语言（最常见的是 JavaScript，这也是第 2 章的内容）编写的代码会监控用户需要的信息，例如他们在 Google Suggest 中搜索的关键词。当用户需要这些信息时（甚至在此之前），JavaScript 代码就会在后台与 Web 服务器通信，获取信息，而不会导致浏览器页面刷新。

也就是说，Ajax 从服务器获取数据的方式对用户是不可见的。JavaScript 代码使用浏览器内置的一个特殊对象——`XMLHttpRequest` 对象——与服务器建立连接并下载数据。这些数据通常是 XML 格式（Ajax 中的 x 代表 XML），但正如你将看到的，也可以是纯文本。

当用户需要的数据在后台下载完成后，JavaScript 代码会利用这些数据更新浏览器中的显示内容。例如，在前面的 Google Suggest 例子中，JavaScript 负责在后台获取 Google 的建议词，然后在下载完成后将它们显示在下拉列表框中。

使用 Ajax 并不局限于下拉列表框。你可以使用 JavaScript 对下载的数据进行几乎任何形式的显示或报告，因为浏览器支持动态 HTML，这意味着你在页面上所做的更改会立即在浏览器中更新，无需刷新页面。

例如，你可以更新网页上的文本，或者改变其大小或颜色以吸引用户对新文本的注意。你可以与朋友聊天，他们的评论可以实时显示在网页上。你甚至可以使用 Ajax 与动态 HTML 一起，下载并显示与用户所需信息对应的图片。

例如，你可以在服务器上绘制商业股票表现图表，然后使用 Ajax 和动态 HTML 下载并显示它们——所有操作都无需页面刷新。想象一下那有多酷：用户可以选择他们想要图表化的股票，页面上的图表就会相应改变，整体体验就像是桌面应用，而非网络应用。

Ajax 由多个组件构成——JavaScript、`XMLHttpRequest` 对象、动态 HTML 等——这些技术自 1998 年以来就已存在。在 Ajax 被正式提出之前，它就已经被一些应用程序（例如微软的 Outlook Web Access）使用了。但 Ajax 真正爆发是在 2005 年，随着 Google Suggest 等新应用的推出，以及杰西·加勒特那篇著名的文章将这些部分整合成一个术语“Ajax”。

自那以后，Ajax 迅速普及。如果你不知道如何使用 Ajax，你就无法成为一名 Web 开发者。幸运的是，Ajax 并不难掌握，正如你将在本书中看到的那样。

让我们继续 Ajax 功能之旅。在着手编写自己的 Ajax 应用程序时，了解 Ajax 能做什么至关重要。

我们将从一个有趣的例子开始：汤姆·里德尔日记。

## 示例：由 Ajax 驱动的汤姆·里德尔日记

如果你访问 `http://pandorabots.com/pandora/talk?botid=c96f911b3e35f9e1`，如图 1-5 所示，你会看到一个在线版的汤姆·里德尔日记（汤姆是《哈利·波特》系列中的一个角色）。

![图 1-5 汤姆·里德尔日记](img/2cd265cf0a64e9b4b91ab611753cd5d5_26_0.png)

这本日记实际上是一个支持 Ajax 的 Web 应用程序。如果你在里面输入内容，它会通过 Ajax 连接到服务器，并输入回复。例如，如果你输入“Hello”，如图 1-6 所示，日记会回复“Hi there!”，如图 1-7 所示。

![图 1-6 向汤姆·里德尔日记问好](img/2cd265cf0a64e9b4b91ab611753cd5d5_27_0.png)

在后台，该网页连接到其服务器，将你输入的内容发送给该服务器，并获得一个响应，然后将其显示出来。很酷。

## 试试这个：汤姆·里德尔日记

打开你的浏览器，导航到 `http://pandorabots.com/pandora/talk?botid=c96f911b3e35f9e1` 以打开汤姆·里德尔日记。

在日记中输入一些内容，例如问题“What's your name?”。你会得到一个答案（“What's your name?”的答案是：“My name is Tom Marvolo Riddle, also known as Lord Vol…eh, forget that last thing will you.”）。

你可以问一些详细的问题——这本日记的设定显得相当智能。试试“Where are you?”、“How old are you?”和“What is the meaning of life?”。

![图 1-7 从汤姆·里德尔日记获得响应](img/2cd265cf0a64e9b4b91ab611753cd5d5_28_0.png)

## 使用 Ajax 更新网页文本

Ajax 经常在后台用于从 Web 服务器获取文本并在网页上显示，而无需刷新页面。你可以在 `http://demos.openrico.org/complex_ajax` 找到一个很好的例子，如图 1-8 所示。

此页面由 Rico 公司提供，该公司销售用于富互联网应用程序的 JavaScript 框架。这是一个 Ajax 演示，允许你创建格式信函——点击左侧的人名，他们的名字和信息就会出现在信件正文中，如你所见，无需刷新页面。

像这样的 Ajax 应用程序从服务器获取的文本可以是 XML 或纯文本格式——值得了解的是 Ajax 也适用于纯文本，而不仅仅是 XML（当然，“纯文本”会让这个缩写变成 Ajapt，听起来远不如 Ajax 好听）。

![图 1-8 Rico Ajax 演示](img/2cd265cf0a64e9b4b91ab611753cd5d5_29_0.png)

## 使用 Ajax 进行实时聊天

许许多多的互联网应用程序会受益于看起来像桌面应用程序，其中一些就是聊天应用程序，允许你与互联网上的其他用户进行交互式打字。

Ajax 聊天会话通过在后台下载他人输入的内容并上传你输入的内容来运作——页面在浏览器中更新时没有任何闪烁。一个 Ajax 聊天应用程序出现在 `www.plasticshore.com/projects/chat/`，如图 1-9 所示。

要开始使用，你只需在标记为“your message”的文本字段中输入文本，然后单击提交按钮。你的消息将无缝添加到聊天显示中；你可以在图 1-9 中看到几个人在来回聊天。

![图 1-9 使用 Ajax 聊天](img/2cd265cf0a64e9b4b91ab611753cd5d5_30_0.png)

## 使用 Ajax 进行拖放操作

随着时间的推移，Web 应用程序看起来会越来越像桌面应用程序，这意味着所有类型的桌面技术都将在网络上可用。例如，许多桌面应用程序使用拖放技术——你可以用鼠标拖动图标或对象并放下它们。

现在，得益于 Ajax，你也可以在网络上进行拖放操作，Ajax 在后台用于通知服务器你将拖动的内容放置在了哪里。



图 1-10 展示了一个支持 Ajax 的拖放互联网应用程序，名为 `Mosaic`。其理念是你和其他人可以通过拖放图块来创建共享的艺术作品。你可以在 `www.thebroth.com/mosaic` 找到 `Mosaic`。

如你所见，通过在后台与服务器来回发送文本和 XML，你可以用 Ajax 做很多事情。只可惜你只能处理文本和 XML——如果能在后台下载图片岂不更好？事实上，你确实可以。

## 12 Ajax：初学者指南

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_31_0.png)

图 1-10 Ajax 的拖放操作

### 使用 Ajax（以及动态 HTML）下载图像

在后台，Ajax 使用文本（包括 XML，它也是文本）与服务器通信。因此，表面上看，Ajax 似乎并不适合下载二进制数据，比如图像。但是，在如今浏览器内置的动态 HTML 的少许帮助下，你也可以下载图像。

借助 JavaScript，你可以使用 Ajax 下载图像。当你更改 HTML `<img>` 标签中当前显示的图像名称时，浏览器会自动下载新图像。这意味着你只需使用 Ajax 下载新图像的文件名，然后依靠 JavaScript 来完成剩下的工作。

你将在本书后面为这个示例创建代码；该示例如图 1-11 所示。只需点击两个按钮中的一个，即可完全在后台下载一个新图像——并显示它，如图 1-11 所示。非常酷。

而且，通过调整此技术，你也可以使用 Ajax 下载和使用其他二进制数据。

还有成千上万的其他 Ajax 应用程序。例如，看看 Netflix 的百佳视频列表，网址为 `www.netflix.com/Top100`，如图 1-12 所示。你在弹出窗口中看到的有关电影的信息就是使用 Ajax 下载的。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_32_0.png)

图 1-11 使用 Ajax 下载图像

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_32_1.png)

图 1-12 Netflix 百佳榜

## 14 Ajax：初学者指南

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_33_0.png)

图 1-13 Ajax 国际象棋

来局国际象棋怎么样？看看这个支持 Ajax 的国际象棋网站 `www.JesperOlsen.Net/PChess/`，如图 1-13 所示。只需点击一个棋子，然后点击你想移动到的方格即可。

有成千上万的 Ajax 应用程序可用，现在你已经看到了其中的一些潜力。例如，想象一个在线购物网站，你不需要经历四五个闪烁的屏幕才能将物品添加到购物车——你只需将物品拖动到购物车图标，而在后台，Ajax 会通知服务器你的购买行为。

所有这些以及更多内容都将在本书中介绍。现在请翻到第 2 章，在那里你将掌握 Ajax 的基础——JavaScript。

## 第 2 章：认识 JavaScript

## 16 Ajax：初学者指南

## 关键技能与概念

- JavaScript 属性和方法

- 将数据存储在变量和数组中

- 使用 `if` 语句做出决策

- 使用 `for` 和 `while` 循环

- 将 JavaScript 连接到 HTML 按钮

我们将通过一个 Ajax 示例立即开始本章。查看图 2-1，了解此示例 `ajax.html` 的运行情况。

如图 2-1 所示，`ajax.html` 显示一个按钮，标题为“获取消息”。当你点击该按钮时，名为 `data.txt` 的文件中的文本将从服务器获取；以下是 `data.txt` 的内容（注意这是简单的文本，这表明 Ajax 除了可以下载 XML 外，还可以下载简单的文本）：

```
Welcome to Ajax!
```

此文本将使用 Ajax 从服务器获取，并显示在 `ajax.html` 页面中。当你点击 `ajax.html` 中的按钮时，所有这些都会发生，如图 2-2 所示。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_35_0.png)

图 2-1 Ajax.html

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_36_0.png)

### 测试 ajax.html

这是你第一个从头编写的 Ajax 脚本的真实示例。要让你自己让此示例工作，请下载本书的代码并解压缩，然后从 `chapter2` 目录复制 `ajax.html` 和 `data.txt`。将这些文件复制到 Web 服务器中的目录中——例如，如果你已经在那里托管网页，你可能使用你的 ISP 的 Web 服务器。如果你没有 ISP，那么此时你需要注册一个——最好是支持 PHP 的 ISP，我们将在本书后面使用 PHP 进行编程。询问你的 ISP 工作人员如何将文件上传到 Web 服务器。将 `ajax.html` 和 `data.txt` 复制到 Web 服务器上的同一位置（即，它们应该在同一个目录中）。然后打开浏览器并使用类似 `www.your_isp/your_name/ajax.html` 的 URL 导航到 `ajax.html`。当 `ajax.html` 出现在浏览器中时，点击按钮以获得如图 2-2 所示的结果。如果你有 Windows XP Pro 或 Windows Vista Business 或 Ultimate，你的计算机上可能已经有一个功能正常的 Web 服务器 Microsoft Internet Information Server (IIS)——如果你有一个名为 `c:\inetpub` 的目录，那么你就拥有 IIS。打开目录 `c:\inetpub\wwwroot`，并创建一个新目录，例如 `c:\inetpub\wwwroot\chapter2`，并将 `ajax.html` 和 `data.txt` 存储在该目录中。然后导航到 `http://localhost/chapter2/ajax.html` 以查看 `ajax.html` 的工作情况。

那么 `ajax.html` 实际上是什么样子的呢？它是本书中我们将要开发的那种代码的一个示例，如下所示：

```html
<html>
  <head>
    <title>An Ajax example</title>
    <script language = "javascript">
      var XMLHttpRequestObject = false;
      if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
        ActiveXObject("Microsoft.XMLHTTP");
      }

      function getData(dataSource, divID)
      {
        if(XMLHttpRequestObject) {
          var obj = document.getElementById(divID);
          XMLHttpRequestObject.open("GET", dataSource);

          XMLHttpRequestObject.onreadystatechange = function()
          {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                obj.innerHTML = XMLHttpRequestObject.responseText;
            }
          }

          XMLHttpRequestObject.send(null);
        }
      }
    </script>
  </head>

  <body>
    <H1>An Ajax example</H1>

    <form>
      <input type = "button" value = "Fetch the message"
      onclick = "getData('data.txt', 'targetDiv')">
    </form>

    <div id="targetDiv">
      <p>The fetched message will appear here.</p>
    </div>

  </body>
</html>
```

上面代码中加粗的部分是 JavaScript，是 Ajax 的核心。要编写 Ajax 应用程序，你需要了解 JavaScript——而这正是本章的重点。

### JavaScript 简介

JavaScript 于 1995 年首次由 Netscape Communications Corporation 的一位名叫 Brendan Eich 的开发者创建并向世界推出。他将他的编程语言命名为 LiveScript，但 Netscape 的当权者将其重命名为 JavaScript。当时 Java 编程语言非常流行，尽管 JavaScript 与 Java 无关，但这个名字还是保留了下来。（事实上，Java 语言的创建者 Sun Microsystems 已经注册了 Java 这个商标，因此“JavaScript”这个名字成为了 Sun Microsystems 的商标。）

JavaScript 大受欢迎。它有趣、强大——总而言之，它很酷。程序员喜欢用它在网页上能做的事情。你可以更改网页中的文本、响应鼠标、更改配色方案等等。网页编写者对此趋之若鹜。

JavaScript 不可避免地引起了微软的注意。当时，两个主流浏览器是 Netscape Navigator 和 Microsoft Internet Explorer。微软不想在 JavaScript 战争中落后，但它又不想简单地从 Netscape 授权 JavaScript——因此它创建了自己的版本，JScript。

JScript 于 1996 年首次出现在 Internet Explorer 3.0 中，多年来，JavaScript 和 JScript 变得越来越相似。然而，存在一些差异，我们将在 Ajax 的导览中遇到（例如，创建 `XMLHttpRequest` 对象——Ajax 的基本编程结构——的方式在 JavaScript 和 JScript 中有所不同），但这不会是我们无法处理的问题。

作为有趣的历史注释，Netscape 和 Microsoft 都求助于第三方，标准机构欧洲计算机制造商协会（Ecma International，`www.ecma-international.org`），以标准化 JavaScript，使其可以在两种浏览器中使用。事实上发生的是，诞生了第三种语言 ECMAScript。如今，大多数浏览器版本的 JavaScript 都正与 ECMAScript 保持一致。

#### 专家答疑

> **问：** 有没有关于 JavaScript、JScript 和 ECMAScript 的在线参考资料？
>
> **答：** 当然有。你可以在 `http://developer.mozilla.org/en/docs/Core_JavaScript_1.5_Reference` 找到 JavaScript 的参考资料，JScript 的参考资料在 `http://msdn2.microsoft.com/en-us/library/hbxc2t98(vs.71).aspx`。
>
> 网上也有大量关于 ECMAScript 的信息：
> - ECMAScript 语言规范，第 3 版，在 `www.ecma-international.org/publications/standards/Ecma-262.htm`。
> - ECMAScript 组件规范在 `www.ecma-international.org/publications/standards/Ecma-290.htm`。
> - ECMAScript 第 3 版紧凑型规范在 `www.ecma-international.org/publications/standards/Ecma-327.htm`。

现在让我们开始深入研究 JavaScript 并看看它是如何工作的。

### JavaScript 入门

我们将通过一个新示例 `javascript.html` 来立即了解 JavaScript 编程。该示例如图 2-3 所示。

在这个第一个示例中，我们将使用 JavaScript 代码来编写图 2-3 中所示的标题“欢迎来到 JavaScript！”；这样做将是我们学习 JavaScript 的起点。

你需要将 JavaScript 嵌入到网页中。假设，例如，`javascript.html` 开头如下——纯 HTML：

```
<html>
  <head>
    <title>This is a first JavaScript example</title>
  </head>

  <body>
    This is a first JavaScript example.
  </body>
</html>
```

现在我们要开始添加 JavaScript 了。你需要将 JavaScript 代码放入一个 HTML `<script>` 元素中，该元素位于页面的 `<head>` 元素内部，如下所示：

```
<html>
  <head>
    <title>This is a first JavaScript example</title>

    <script language="javascript">
      .
      .
      .
    </script>
  </head>

  <body>
    This is a first JavaScript example.
  </body>
</html>
```

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_39_0.png)

## 第 2 章：认识 JavaScript

请注意，`<script>` 元素与其他任何 HTML 元素一样。它的目的是告知浏览器存在 JavaScript 代码，并且浏览器应运行该代码。同时注意 `<script>` 元素的 `language` 属性，这里被设置为值“javascript”，表示 `<script>` 元素内使用的脚本语言是 JavaScript（还有其他脚本语言，例如 VBScript，它在 Internet Explorer 中运行）。

现在我们的任务是将标题“欢迎来到 JavaScript！”（见图 2-3）写入网页。在 JavaScript 中，你通过使用内置*对象*与浏览器进行交互；这些对象已经存在，并且可以通过名称从你的 JavaScript 代码中访问。以下是最常用的四个对象：

- **document** 代表网页本身

- **history** 代表浏览器已访问过的 URL 列表

- **window** 代表浏览器本身

- **XMLHttpRequest** 这是在 Ajax 中用于与服务器通信的对象

在 JavaScript 中，对象有方法和属性。*方法*是内置在对象中的一段代码，用于执行某些操作——例如，你使用 `document` 对象的 `write` 方法（通过 `document.write` 访问）来写入文档（即当前网页）。以下是一些代表性的方法及其在 JavaScript 中的作用：

- **document.write** 允许你向当前网页写入文本

- **history.go** 将浏览器移动到历史记录中的某个页面

- **window.open** 打开一个新的浏览器窗口

另一方面，*属性*只是你可以放置数据的设置。例如，`document.bgcolor` 允许你访问 HTML `<body>` 元素的 `bgcolor` 值——即背景颜色。（JavaScript 属性通常从 HTML 元素的属性中获取其名称，例如 `<body>` 元素的 `bgcolor` 属性。）以下是可用的一些有用属性：

- **document.bgcolor** 保存当前页面的背景颜色

- **document.fgcolor** 保存当前页面的前景颜色

- **document.lastmodified** 保存页面最后修改的日期

- **document.title** 保存页面的标题

- **location.hostname** 保存页面主机的名称

- **navigator.appName** 保存浏览器的类型

## 22 Ajax：初学者指南

我们将在 `javascript.html` 示例中使用 `document.write` 方法向当前网页写入内容。你可以通过将要写入的文本放在括号内来将其发送到网页，这会将文本传递给 `document.write` 方法，如下所示：

```
<html>
  <head>
    <title>This is a first JavaScript example</title>
    
    <script language="javascript">
      document.write("<h1>Welcome to JavaScript!</h1>");
    </script>
  </head>

  <body>
    This is a first JavaScript example.
  </body>
</html>
```

这样的代码行在 JavaScript 中被称为*语句*，如你所见，它们以分号结尾。请注意，我们实际上是将 HTML 传递给 `document.write` 方法——也就是说，我们在当前网页中显示的文本是 `<h1>Welcome to JavaScript!</h1>`，它在 `<h1>` 标题内显示“欢迎来到 JavaScript！”文本，就像你自己将此 HTML 添加到网页中一样：

<h1>Welcome to JavaScript!</h1>



你可以在图 2-3 中看到结果，新的标题出现了。效果不错。

注意图 2-3 中文本的位置。我们用 JavaScript 编写的标题出现在 `<body>` 元素中文本的上方。为什么？因为当浏览器读取 `javascript.html` 时，它会一边读取一边处理页面，并且它首先读取 `<head>` 部分（我们的 JavaScript 就在那里）。因此，在浏览器看到 `<body>` 元素中的文本之前，JavaScript 代码就被执行了，从而产生了你在图 2-3 中看到的结果。通常，`<script>` 元素中的代码在加载后就会执行，但这并不总是你想要的：例如，你可能希望等到用户点击按钮后再执行你的 JavaScript。在本章后面，你将看到如何确保 JavaScript 代码只在你想要执行的时候执行——而不是在页面加载时自动执行。

### 动手试试：让 `javascript.html` 运行起来

你需要某种文本编辑器来输入 `javascript.html` 并在浏览器中运行它。（你可以直接从本书可下载代码的 `chapter2` 文件夹中获取 `javascript.html`，但为了跟上本书的学习，你必须知道如何创建自己的文件。）

例如，在 Windows 中，Windows 写字板就可以很好地工作。打开写字板并输入 `javascript.html` 的文本。要保存 `javascript.html`，选择“文件” | “另存为”以打开“另存为”对话框。将文件命名为 `javascript.html`，并且——这一点很重要——在“保存类型”下拉列表框中，选择“文本文档”，而不是默认的“富文本文档 (RTF)”。如果你以 RTF 格式保存网页，浏览器将无法读取它们。

关于写字板还有一点需要注意：如果你保存的文件的文件名扩展名是写字板不熟悉的，它会在你的文件名后附加后缀“.txt”。对于 HTML 文件来说这不是问题，因为它们具有 `.html` 扩展名，写字板是理解的。但当涉及到本书末尾我们将用于在 Web 服务器上执行编程的 PHP 文件（从第 9 章开始，你将看到 PHP 是一种在 Web 服务器上使用的编程语言）时，这将成为一个问题。例如，如果你尝试使用写字板将文件另存为 `ajax.php`，写字板会将文件保存为 `ajax.php.txt`，这在服务器上将无法工作。相反，你必须在“另存为”对话框的“文件名”框中将文件名用引号括起来，如下所示："ajax.php"。这样做告诉写字板你不想更改你保存的文件名，因此它不会附加 `.txt` 扩展名。

你可以将 `javascript.html` 保存到 Web 服务器，或者，如果你愿意，也可以简单地保存到你的硬盘——由于 `javascript.html` 完全依赖 JavaScript，不需要与服务器交互，因此可以直接从磁盘在浏览器中打开。保存 `javascript.html` 后，在浏览器中打开它，并通过与图 2-3 中看到的进行比较来确认结果。你可以通过输入在 Web 服务器上访问它的 URL 来导航到 `javascript.html`，或者直接从磁盘打开（在 Internet Explorer 中，选择“文件” | “打开”并浏览到 `javascript.html`；在 Firefox 中，选择“文件” | “打开文件”）。

另外请注意，有些用户可能在他们的浏览器中关闭了 JavaScript 支持，在这种情况下，他们无法运行 `javascript.html`，也无法运行 Ajax。（你可以考虑在网页中添加一条说明，如果用户没有看到预期的效果，请确保浏览器中的 JavaScript 支持已开启。）

### 为你的代码添加注释

既然我们已经运行了一些 JavaScript，值得注意的是你可以用注释来为你的代码添加说明，注释是供人阅读的文本，计算机则会忽略它们。使用注释可以让你的 JavaScript 代码更具可读性，并用通俗的语言解释你的程序做了什么。

JavaScript 中有两种形式的注释：单行和多行。单行注释以 `//`（两个正斜杠）开头，如下所示：

```html
<html>
  <head>
    <title>This is a first JavaScript example</title>

    <script language="javascript">
      //Write to the web page
      document.write("<h1>Welcome to JavaScript!</h1>");
    </script>
  </head>
```

### Ajax：入门指南

```html
<body>
This is a first JavaScript example.
</body>
</html>
```

在一行中，`//` 之后的所有内容都会被浏览器忽略。你也可以在代码行的末尾放置单行注释，就像这样：

```html
<html>
<head>
<title>This is a first JavaScript example</title>
<script language="javascript">
document.write("<h1>Welcome to JavaScript!</h1>"); //Write to the page
</script>
</head>
<body>
This is a first JavaScript example.
</body>
</html>
```

多行注释用 `/*` 和 `*/` 包围。当你使用 `/*` 时，浏览器会忽略之后的所有内容，直到看到 `*/` 才结束注释。这里是一个多行注释的例子：

```html
<html>
<head>
<title>This is a first JavaScript example</title>
<script language="javascript">
/*
Write
to
the
web page.
*/
document.write("<h1>Welcome to JavaScript!</h1>");
</script>
</head>
<body>
This is a first JavaScript example.
</body>
</html>
```

### 使用外部 JavaScript 文件

你经常会看到启用了 Ajax 的网页使用这种语法，而网页本身内部没有 JavaScript（`external.html`）：

```html
<html>
    <head>
        <title>Using external JavaScript</title>
        <script language="javascript" src="script.js"></script>
    </head>
    <body>
        <h1>Using external JavaScript</h1>
    </body>
</html>
```

这里发生了什么？在这种情况下，JavaScript 代码被外部存储在一个名为 `script.js` 的文件中。那么 `script.js` 里到底是什么？就是你想执行的 JavaScript 代码行，仅此而已。例如，在这个例子中，那就是：

```javascript
document.write("<h1>Welcome to JavaScript!</h1>");
```

这个新例子的工作方式与你已经看到的 `javascript.html` 示例非常相似，只是 JavaScript 位于网页外部。你在 Ajax 中会经常看到这种情况——你可以找到大型的预编写代码的 JavaScript 库，这些库可能有几十页之多。其中一些代码是为了支持 Ajax 而编写的，这样你只需要编写最少的代码，在这种情况下，这些库被称为 Ajax 框架（参见第 5 章）。当你使用这样一个框架时，如果必须将它的全部代码——几十页的内容——都包含在你自己的网页中，那会很尴尬。解决方案是 Ajax 框架将其 JavaScript 打包在外部文件中，你只需像这里看到的那样，使用 `<script>` 元素的 `src` 属性来引用该代码。问题解决了。

好的，到目前为止，你看到的 JavaScript 代码都是在包含该 JavaScript 的页面加载后由浏览器立即执行的。但如果你想运行你的 JavaScript——例如，显示新文本——只有在页面加载完毕并且用户点击按钮之后才运行呢？接下来我们就会讲到。

### 在浏览器中处理事件

到目前为止，你的 JavaScript 都是在页面加载后立即运行的：

```html
<html>
    <head>
        <title>This is a first JavaScript example</title>
        <script language="javascript">
            document.write("<h1>Welcome to JavaScript!</h1>");
        </script>
    </head>
    <body>
        This is a first JavaScript example.
    </body>
</html>
```

但你可能只想在特定事情发生时才执行一些代码，比如鼠标点击或输入字符。在这种情况下，你可以设置你的 JavaScript 代码来响应浏览器*事件*（如鼠标点击或按键）。

事件就像它的名字一样——发生了某事；例如，用户点击了一个按钮。有哪些可用的事件？以下是你在 Ajax 应用程序中可能常见的一些事件：

| 事件 | 发生在…… |
|---|---|
| `onabort` | 一个操作被中止时。 |
| `onblur` | 一个元素失去输入焦点时。 |
| `onchange` | 控件（如文本字段）中的数据发生变化时。 |
| `onclick` | 一个元素被点击时。 |
| `ondblclick` | 一个元素被双击时。 |
| `ondragdrop` | 进行拖放操作时。 |
| `onerror` | 发生 JavaScript 错误时。 |
| `onfocus` | 一个元素获得焦点时。 |
| `onkeydown` | 一个键被按下时。 |
| `onkeypress` | 一个键被按下并且按键代码可用时。 |
| `onkeyup` | 一个键被释放时。 |
| `onload` | 页面加载完成时。 |
| `onmousedown` | 鼠标按钮被按下时。 |
| `onmousemove` | 鼠标移动时。 |
| `onmouseout` | 鼠标离开一个元素时。 |
| `onmouseover` | 鼠标移动到一个元素上方时。 |
| `onmouseup` | 鼠标按钮被释放时。 |
| `onreset` | 用户点击重置按钮时。 |
| `onresize` | 元素或页面被调整大小时。 |
| `onsubmit` | 用户点击提交按钮时。 |
| `onunload` | 页面被卸载时。 |

要处理这些事件，你需要在 HTML 标签中使用同名属性。让我们来看一个简单的例子 `click.html`，它能让这一点更清楚。在这个例子中，我们将使页面在你点击它时做出响应，使用*内联* JavaScript——即，将 JavaScript 代码分配给 HTML 标签中的事件属性，像这样（`click.html`）：

```html
<html>
    <head>
        <title>
            Using browser events
        </title>
    </head>
    <body onmousedown="alert('You clicked the page.')">
      <h1>
        Click this page!
      </h1>
      Go ahead...
    </body>
</html>
```

这里发生的是，我们使用 `<body>` 元素（代表整个网页）的 `onmousedown` 事件来响应鼠标按下事件（即，鼠标按钮被按下）。当用户在页面中按下鼠标按钮时，`onmousedown` 事件会“触发”（这是技术术语），并且分配给该事件的 JavaScript 会被执行。

在这个例子中，JavaScript 就是语句 `alert('You clicked the page.')`，它会显示一个 JavaScript 警告框（即，一个对话框），其中包含文本“You clicked the page.”。

### 专家问答

> **问：** 为什么你在语句 `alert('You clicked the page.')` 中使用单引号？难道不应该是 `alert("You clicked the page.")` 吗？
>
> **答：** 你使用单引号是为了避免混淆浏览器。请注意，内联 JavaScript 必须完全包含在引号中，像这样：
>
> ```html
> <body onmousedown="alert('You clicked the page.')">
> ```
>
> 如果我们不交替使用双引号和单引号，浏览器将不知道要显示的文本从哪里开始、到哪里结束。

你可以在图 2-4 中看到实际操作，其中显示了 `click.html`。

![图 2-4 `click.html`](img/2cd265cf0a64e9b4b91ab611753cd5d5_46_0.png)

**图 2-4** `click.html`

28 Ajax：入门指南

![图 2-5 `click.html` 运行效果](img/2cd265cf0a64e9b4b91ab611753cd5d5_47_0.png)

**图 2-5** `click.html` 运行效果

当你点击页面时，一个对话框会出现，表明点击已被注意到，如你在图 2-5 中所见。很酷吧。现在你已经响应了一个浏览器事件。

### 动手试试：让 `click.html` 工作

使用你的文本编辑器将 `click.html` 的代码输入到一个文件中（或者，如果你想走捷径，直接从本书可下载代码的 `chapter2` 文件夹中复制 `click.html`），并将该文件存储在浏览器可以访问的 Web 服务器上，或者直接存储在磁盘上。现在打开你的浏览器，导航到 `click.html`——然后点击页面。你应该会看到图 2-5 中所示的对话框。干得好！

好，这是一种响应浏览器事件的方法——使用内联 JavaScript 代码。但随着你的 JavaScript 代码变得越来越大，它将无法以内联方式存储。那么你能做什么呢？你可以使用 JavaScript 函数，接下来就会讲到。

### 使用 JavaScript 函数

你已经知道，你可以在 `<script>` 元素中编写代码，该代码将在页面加载时自动执行：

```html
<html>
    <head>
        <title>This is a first JavaScript example</title>
        <script language="javascript">
            document.write("<h1>Welcome to JavaScript!</h1>");
        </script>
    </head>
    <body>
        This is a first JavaScript example.
    </body>
</html>
```

第 2 章：了解 JavaScript

29

要在你想执行代码时执行它，你需要将该代码放在一个 JavaScript *函数*中（函数就像方法，只是方法包含在 JavaScript 对象内部，而函数是独立的）。例如，以下是你如何创建一个名为 `display` 的函数：

```html
<html>
<head>
    <title>Using JavaScript functions</title>
    <script language="javascript">
        function display()
        {
            .
            .
            .
        }
    </script>
</head>
<body>
    <h1>Using JavaScript functions</h1>
</body>
</html>
```

注意这里的语法——你使用关键字 `function`，后跟新函数的名称，以及一对圆括号。后面是函数的代码，包含在花括号 `{` 和 `}` 中，代码将放在那里。

要运行函数中的代码，你必须*调用*那个函数，我们将当用户点击按钮时调用它，所以现在使用 HTML `<input>` 标签添加该按钮，像这样：

```html
<html>
<head>
    <title>Using JavaScript functions</title>
    <script language="javascript">
        function display()
        {
            .
            .
            .
        }
    </script>
</head>
<body>
    <h1>Using JavaScript functions</h1>
</body>
</html>
```

## 30 Ajax：初学者指南

```html
<form>
    <input type="button" value="Click Here">
</form>
</body>
</html>
```

请注意，在 HTML 中，你必须将控件（如按钮、列表框、复选框等）包裹在 HTML `<form>` 元素中。这里的 `<input>` 元素创建了一个标题为“Click Here”的按钮。

那么，当用户点击按钮时，我们实际上如何调用显示函数呢？你可以使用一小段内联代码来实现。只需给出函数名，后跟括号，即可调用该函数。因此，我们可以通过将函数调用赋值给按钮的 `onclick` 事件，在用户点击按钮时调用函数：



```html
<html>
    <head>
        <title>Using JavaScript functions</title>
        <script language="javascript">
            function display()
            {
                .
                .
                .
            }
        </script>
    </head>
    <body>
        <h1>Using JavaScript functions</h1>
        <form>
            <input type="button" onclick="display()"
                   value="Click Here">
        </form>
    </body>
</html>
```

现在，当用户点击按钮时，`display`函数就会被调用。在`display`函数中，我们可以向网页写入一条消息——比如，“You clicked the button.”。那么，我们可以用下面的代码来实现吗？

```html
<html>
    <head>
        <title>Using JavaScript functions</title>
        <script language="javascript">
function display()
{
    document.write("You clicked the button.");
}
</script>
    </head>
    <body>
        <h1>Using JavaScript functions</h1>
        <form>
            <input type="button" onclick="display()"
                   value="Click Here">
        </form>
    </body>
</html>
```

不幸的是，不行。`display`函数确实会在页面主体加载完成后——当用户点击按钮时——被调用，这没问题。但这里有个陷阱。当页面主体加载完毕后，你就不能再使用`document.write`方法了，因为此时文档被视为已关闭。再次打开它来写入内容会清除其中的所有文本，所以这里不适用——你只会看到“You clicked the button.”消息，因为“Using JavaScript functions”标题会被覆盖。

在网页加载后显示新文本的方法是写入一个现有的 HTML 元素，比如`<div>`元素。例如，你可以添加一个`<div>`元素并给它一个 ID `targetDiv`：

```html
<html>
    <head>
        <title>Using JavaScript functions</title>
        <script language="javascript">
            function display()
            {
                .
                .
                .
            }
        </script>
    </head>
    <body>
        <h1>Using JavaScript functions</h1>
        <form>
            <input type="button" onclick="display()"
                   value="Click Here">
        </form>
        <div id="targetDiv">
        </div>
    </body>
</html>
```

那么，如何在 JavaScript 代码中通过`display`函数访问`targetDiv`元素呢？你必须告诉 JavaScript 你想要将文本放置到哪个 HTML 元素中以显示该文本。要在网页中查找 HTML 元素，你可以使用 JavaScript 方法`document.getElementById`。

你传递给这个方法的是你想查找的元素的 ID；要将数据传递给方法或函数，你需要将该数据括在括号中（就像你用`document.write`一样：`document.write("Here is the text")`）。所以，要找到`targetDiv` HTML 元素，你可以调用`document.getElementById('targetDiv')`。此方法调用返回一个对应于`targetDiv` `<div>`元素的对象——当方法或函数返回数据时，你就可以访问这些数据。例如，对应于`targetDiv` `<div>`元素的对象支持它自己的各种方法和属性，其中一个属性`innerHTML`包含元素中当前的文本。这意味着你可以通过将新文本赋值给表达式`document.getElementById('targetDiv').innerHTML`，在元素中存储新文本。

下面是你可以在`targetDiv` `<div>`元素中存储文本“You clicked the button.”的方法：

```html
<html>
    <head>
        <title>Using JavaScript functions</title>
        <script language="javascript">
            function display()
            {
                document.getElementById('targetDiv').innerHTML =
                "You clicked the button.";
            }
        </script>
    </head>
    <body>
        <h1>Using JavaScript functions</h1>
        <form>
            <input type="button" onclick="display()" value="Click Here">
        </form>
        <div id="targetDiv">
        </div>
    </body>
</html>
```

很好，我们准备就绪：在浏览器中打开`functions.html`，然后点击按钮。当你这样做时，你会看到文本“You clicked the button.”被显示出来，如图 2-6 所示。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_52_0.png)

### 向函数传递数据

就像你可以向 JavaScript 内置的方法传递数据一样，你也可以向你创建的函数传递数据。例如，假设你想通过将消息传递给`display`函数来指定要显示的消息。你可以像之前调用方法那样，通过在调用`display`时将其放在括号内，将消息传递给`display`函数，就像我们在新网页`message.html`中看到的：

```html
<html>
    <head>
        <title>Passing data to functions</title>
        <script language="javascript">
            function display()
            {
                .
                .
                .
            }
        </script>
    </head>
    <body>
        <h1>Passing data to functions</h1>
        <form>
            <input type="button" onclick=
            "display('You are seeing this thanks to JavaScript')" value=
            "Click Here">
        </form>
    </body>
</html>
```

那么，在代码中如何读取传递给`display`函数的消息呢？很简单——你只需在创建`display`函数时，在括号中列出传递给`display`函数的数据的名称：

```html
<html>
    <head>
        <title>Passing data to functions</title>
        <script language="javascript">
            function display(message)
            {
                .
                .
                .
            }
        </script>
    </head>
    <body>
        <h1>Passing data to functions</h1>
        <form>
            <input type="button" onclick="display('You are seeing this thanks to JavaScript')" value="Click Here">
        </form>
        <div id="targetDiv"></div>
    </body>
</html>
```

现在，你可以在函数体内使用你赋予该数据的名称——`message`——来引用传递给`display`函数的数据。所以，例如，要在网页中显示该消息，你可以这样做（`message.html`）：

```html
<html>
    <head>
        <title>Passing data to functions</title>
        <script language="javascript">
            function display(message)
            {
                document.getElementById("targetDiv").innerHTML = message;
            }
        </script>
    </head>
    <body>
        <h1>Passing data to functions</h1>
        <form>
            <input type="button" onclick=
            "display('You are seeing this thanks to JavaScript')" value=
            "Click Here">
        </form>
        <div id="targetDiv">
        </div>
    </body>
</html>
```

你可以在图 2-7 中看到其效果。点击 Click Here 按钮，你的消息将被传递给`display`函数，该函数获取该消息并将其显示在网页中，如你在图 2-7 中所见。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_54_0.png)

图 2-7 向 JavaScript 函数传递数据

## 36 Ajax：初学者指南

### 尝试一下：向函数传递数据

在文本编辑器中将`message.html`的代码输入到一个文件中，并将该文件存储在可访问你浏览器的 Web 服务器上，或者只是存储在磁盘上。将传递给`display`函数的消息从‘You are seeing this thanks to JavaScript’更改为‘Hey, this works!’。

现在打开你的浏览器，导航到`message.html`，然后点击按钮。你应该会看到你的消息被显示出来。太棒了！

如果你想向函数传递多个数据项怎么办？你只需在函数名后的括号中用逗号分隔传递这些项即可。例如，假设你在页面中有两个`<div>`元素，`targetDiv`和`targetDiv2`：

```html
<html>
    <head>
        <title>Passing data to functions</title>
        <script language="javascript">
            function display(message)
            {
                document.getElementById("targetDiv").innerHTML = message;
            }
        </script>
    </head>
    <body>
        <h1>Passing data to functions</h1>
        <input type="button" onclick=
        "display('You are seeing this thanks to JavaScript')" value=
        "Click Here">
        <div id="targetDiv">
        </div>
        <div id="targetDiv2">
        </div>
    </body>
</html>
```

如何指定要在哪个`<div>`元素中显示你的消息呢？你可以将该`<div>`元素的 ID 传递给`display`函数，它的工作方式如下：

```html
<html>
    <head>
        <title>Passing data to functions</title>
```

### 将数据传递给函数

```html
<script language="javascript">
    function display(message)
    {
        document.getElementById("targetDiv").innerHTML = message;
    }
</script>
</head>

<body>

<h1>将数据传递给函数</h1>

<input type="button" onclick=
"display('You are seeing this thanks to JavaScript', 'targetDiv')"
value="Click Here">

<div id="targetDiv">
</div>
<div id="targetDiv2">
</div>

</body>
</html>
```

接下来，在`display`函数中，你可以将传入的第二个数据项命名为类似`elementID`的名字，函数可以这样编写：

```javascript
function display(message, elementID)
{
    .
    .
    .
}
```

现在你就可以在代码中自由使用`elementID`这个数据项，将消息放置到对应的`<div>`元素中，如下所示：

```html
<html>
<head>
    <title>将数据传递给函数</title>

    <script language="javascript">
        function display(message, elementID)
        {
            document.getElementById(elementID).innerHTML = message;
        }
    </script>
</head>

<body>
    <h1>将数据传递给函数</h1>
    <input type="button" onclick=
    "display('You are seeing this thanks to JavaScript', 'targetDiv')"
    value="Click Here">
    <div id="targetDiv"></div>
</body>
</html>
```

就是这样简单。

### 从函数返回数据

你也可以从函数中返回数据。换句话说，一个函数可以完成它的工作，并将某种结果传回给你。例如，假设你有一个巧妙的名为`adder`的函数，并且你传递两个数字给它相加——它如何能从`adder`函数中将答案发送回来呢？

假设`adder`看起来像这样：

```javascript
function adder(operand1, operand2)
{
    .
    .
    .
}
```

你可以使用`return`语句从函数返回一个值，在`adder`的例子中如下所示：

```javascript
function adder(operand1, operand2)
{
    return operand1 + operand2;
}
```

也就是说，我们正在将传递给`adder`的两个数据项`operand1`和`operand2`相加，并返回它们的和。这样，当你调用，比如`adder(6, 6)`时，JavaScript 将在运行时用`adder`函数返回的值替换该调用。所有这些都意味着，以下是你如何从另一个函数`display`中调用`adder`的方法（这是`adder.html`）：

```html
<html>
<head>
    <title>从函数返回数据</title>
    <script language="javascript">
        function display()
        {
            document.getElementById("targetDiv").innerHTML =
            "6 + 6 = " + adder(6, 6);
        }

        function adder(operand1, operand2)
        {
            return operand1 + operand2;
        }
    </script>
</head>
<body>
    <h1>从函数返回数据</h1>
    <input type="button" onclick="display()" value="Click to add 6 + 6">

    <div id="targetDiv">
    </div>
</body>
</html>
```

查看图 2-8 中的`adder.html`。当你点击按钮时，瞧，6 加上 6 的结果就显示出来了。这里发生的事情是，6 和 6 被传递给`adder`函数，该函数将它们相加并返回和值 12。很好。

### 动手试试：从函数返回数据



尝试创建你自己版本的`adder`示例，但不是将两个数字相加，而是将它们相乘！编写并使用一个名为`multiplier`的函数来代替`adder`，并将两个值传递给`multiplier`——然后显示结果乘积。在 JavaScript 代码中，你使用`*`符号进行乘法运算；例如，`6 * 6 = 36`。

![img/2cd265cf0a64e9b4b91ab611753cd5d5_58_0.png](img/2cd265cf0a64e9b4b91ab611753cd5d5_58_0.png)

图 2-8 从 JavaScript 函数返回数据

### 使用变量

JavaScript 允许你将数据存储在*变量*中，这些变量是内存中的占位符，设置用于保存数据。当你将数据存储在变量中时，该数据会保留下来，供你随时使用。你可以使用 JavaScript 的`var`语句创建变量；这里有一个例子，它创建了一个名为`message`的变量，并将文本 "This text was stored in a variable." 存入其中（在`variable.html`中）：

```html
<html>
  <head>
    <title>使用变量</title>

    <script language="javascript">

      var message = "This text was stored in a variable.";

      function display()
      {
        .
        .
        .
      }
    </script>
  </head>

  <body onload="showMessage()">
    <h1>使用变量</h1>

    <input type="button" onclick="display()" value="Click Here">

    <div id="targetDiv">
    </div>

  </body>
</html>
```

现在你可以在代码中引用`message`变量，就像这里一样，我们正在将`message`的文本显示在一个`<div>`元素中（`variable.html`）：

```html
<html>
  <head>
    <title>使用变量</title>

    <script language="javascript">

      var message = "This text was stored in a variable.";

      function display()
      {
        document.getElementById('targetDiv').innerHTML = message
      }
    </script>
  </head>

  <body onload="showMessage()">
    <h1>使用变量</h1>

    <input type="button" onclick="display()" value="Click Here">

    <div id="targetDiv">
    </div>

  </body>
</html>
```

你可以在图 2-9 中看到`variable.html`的实际效果。只需点击按钮，消息就会从`message`变量中获取并显示在网页上。

![img/2cd265cf0a64e9b4b91ab611753cd5d5_60_0.png](img/2cd265cf0a64e9b4b91ab611753cd5d5_60_0.png)

图 2-9 在变量中存储数据

除了在变量中存储文本，你还可以存储数字，比如在这个例子中，我们修改了`adder`函数，将计算出的和存储在一个名为`sum`的变量中，然后返回该和：

```html
<html>
    <head>
        <title>从函数返回数据</title>

        <script language="javascript">
            function display()
            {
                document.getElementById("targetDiv").innerHTML =
                    "6 + 6 = " + adder(6, 6);
            }

            function adder(operand1, operand2)
            {
              var sum = operand1 + operand2;
              return sum;
            }
        </script>
    </head>

    <body>
      <h1>从函数返回数据</h1>
      <input type="button" onclick="display()" value="Click to add 6 + 6">

      <div id="targetDiv">
      </div>

    </body>
</html>
```

你应该知道这两个例子之间有一个区别。当你在任何函数外部创建一个变量时，就像这样：

```javascript
<script language="javascript">

  var message = "This text was stored in a variable.";

  function display()
  {
    document.getElementById('targetDiv').innerHTML = message
  }
</script>
```

那么这个变量就被称为*全局*变量，可以在代码中的任何地方使用，无论是在函数内部还是外部。然而，如果你在函数内部创建一个变量，就像这样：

```javascript
function adder(operand1, operand2)
{
  var sum = operand1 + operand2;
  return sum;
}
```

那么这个变量就被称为*局部*变量，它只能在同一个函数内部使用和访问。

### 用运算符将一切组合起来

你已经知道可以使用`+`号来相加值：

```javascript
function adder(operand1, operand2)
{
  var sum = operand1 + operand2;
  return sum;
}
```

加号`+`是 JavaScript 的加法运算符。你也可以使用减法运算符`−`来相减值：

```javascript
var value = operand1 + operand2;
```

或者使用`*`运算符来相乘值：

```javascript
var value = operand1 * operand2;
```

或者使用除法运算符`/`来相除值：

```javascript
var value = operand1 / operand2;
```

JavaScript 中已经内置了许多这样的运算符。完整列表见表 2-1。

| 运算符 | 描述 |
|---|---|
| **算术运算符** | |
| `+` | 将两个数字相加。 |
| `++` | 将变量中的值增加一。 |
| `–` | 从另一个数字中减去一个数字。也可以像这样改变其操作数的符号：`–variableName`。 |
| `--` | 将变量中的值减去一。 |
| `*` | 将两个数字相乘。 |
| `/` | 将两个数字相除。 |
| `%` | 计算两个数字进行整数除法后的余数。 |
| **字符串运算符** | |
| `+` | 连接（拼接）两个字符串。 |
| `+=` | 连接（拼接）两个字符串，并将连接后的字符串赋值给第一个操作数。 |
| **逻辑运算符** | |
| `&&` | 如果两个操作数都为 true，则求值为 true；否则，求值为 false。 |
| `\|\|` | 如果任一操作数为 true，则求值为 true。但是，如果两个操作数都为 false，则求值为 false。 |
| `!` | 如果其操作数为 true，则求值为 false；如果其操作数为 false，则求值为 true。 |
| **位运算符** | |
| `&` | 在两个操作数的位都为 1 的每个位位置上设置一个 1。 |
| `^` | 在其中一个操作数的位为 1，但两个操作数不都为 1 的位位置上设置一个 1。 |
| `\|` | 如果任一操作数在该位置为 1，则在该位设置一个 1。 |

表 2-1 JavaScript 运算符（续）

Ajax：初学者指南

| 运算符 | 描述 |
| :--- | :--- |
| `~` | 按位取反。 |
| `<<` | 将第一个操作数的位向左移动由第二个操作数指定的位数。 |
| `>>` | 将第一个操作数的位向右移动由第二个操作数指定的位数。 |
| `>>>` | 将第一个操作数的位向右移动由第二个操作数指定的位数，并在左侧移入零。 |

## 赋值运算符

| 运算符 | 描述 |
| :--- | :--- |
| `=` | 将第二个操作数的值赋给第一个操作数。 |
| `+=` | 将两个操作数相加，并将结果赋给第一个操作数。 |
| `-=` | 将两个操作数相减，并将结果赋给第一个操作数。 |
| `*=` | 将两个操作数相乘，并将结果赋给第一个操作数。 |
| `/=` | 将两个操作数相除，并将结果赋给第一个操作数。 |
| `%=` | 计算两个操作数的模，并将结果赋给第一个操作数。 |
| `&=` | 对两个操作数执行按位与操作，并将结果赋给第一个操作数。 |
| `^=` | 对两个操作数执行按位异或操作，并将结果赋给第一个操作数。 |
| `\|=` | 对两个操作数执行按位或操作，并将结果赋给第一个操作数。 |
| `<<=` | 对两个操作数执行左移操作，并将结果赋给第一个操作数。 |
| `>>=` | 对两个操作数执行符号传播右移操作，并将结果赋给第一个操作数。 |
| `>>>=` | 对两个操作数执行零填充右移操作，并将结果赋给第一个操作数。 |

## 比较运算符

| 运算符 | 描述 |
| :--- | :--- |
| `==` | 如果两个操作数相等，则计算结果为 true。 |
| `!=` | 如果两个操作数不相等，则计算结果为 true。 |
| `===` | 如果两个操作数相等且类型相同，则计算结果为 true。 |
| `!==` | 如果两个操作数不相等或类型不同，则计算结果为 true。 |
| `>` | 如果第一个操作数的值大于第二个操作数的值，则计算结果为 true。 |
| `>=` | 如果第一个操作数的值大于或等于第二个操作数的值，则计算结果为 true。 |

## 第 2 章：认识 JavaScript

| 运算符 | 描述 |
| :--- | :--- |
| `<` | 如果第一个操作数的值小于第二个操作数的值，则计算结果为 true。 |
| `<=` | 如果第一个操作数的值小于或等于第二个操作数的值，则计算结果为 true。 |

## 特殊运算符

| 运算符 | 描述 |
| :--- | :--- |
| `?:` | 执行“if...else”测试。 |
| `,` | 计算两个表达式并返回第二个表达式的结果。 |
| `delete` | 删除一个对象并从内存中移除它，或删除一个对象的属性，或删除数组中的一个元素。 |
| `function` | 创建一个匿名函数。 |
| `in` | 如果你测试的属性被特定对象支持，则计算结果为 true。 |
| `instanceof` | 如果给定对象是指定类型的实例，则计算结果为 true。 |
| `new` | 从指定对象类型创建一个新对象。 |
| `typeof` | 计算结果为操作数类型的名称。 |
| `void` | 允许在不返回任何值的情况下计算表达式。 |

表 2-1 JavaScript 运算符（续）

下面是一个例子。假设你有五个苹果和三个橙子：

```javascript
var apples = 5;
var oranges = 3;
```

如果你想把你的苹果和橙子加起来，你可以这样进行加法运算：

```javascript
var apples = 5;
var oranges = 3;
var fruit = apples + oranges;
```

现在名为`fruit`的变量的值是 8；`=`号被称为赋值运算符，你用它来为变量赋值。事实上，JavaScript 通过复合赋值运算符`+=`给了你一个捷径，它既能将两个值相加，又能将结果赋给一个变量。例如，如果你想将一个名为`temperature`的变量中存储的值增加 3，你可以这样做：

```javascript
var temperature = 72;
temperature = temperature + 3;
```

或者，你可以使用`+=`捷径，像这样：

```javascript
var temperature = 72;
temperature += 3;
```

### Ajax：初学者指南

除了`+=`，还有`*=`、`-=`和其他复合赋值运算符，如表 2-1 所示。

注意表 2-1 中的运算符，如`==`、`<`和`>`。它们是做什么的？它们是比较运算符，它们允许你通过`if`语句（稍后介绍）在代码中做出决定（温度是否低于 72？是吗？是时候去野餐了！）。

## 使用 if 语句

这个`if`语句是我们将看到的第一个允许你根据某个条件（你设置的）是否为真来执行代码的语句。`if`语句的形式如下所示（方括号中的部分是可选的，你需要用你自己的 JavaScript 替换斜体部分）：

```javascript
if (condition) {
    statements1
}
[else {
    statements2
}]
```

让我们看一个例子来说明这一点。你的银行账户里有超过 100 万美元吗？如果有，下一个例子将显示消息“是时候去度假了！”（这是`if.html`）：

```html
<html>
  <head>
    <title>使用 if 语句</title>

    <script language="javascript">

      function display()
      {
        var account = 2000000;
        if(account > 1000000) {
            document.getElementById('targetDiv').innerHTML =
                "是时候去度假了！";
        }
      }
    </script>

  </head>

  <body>

    <h1>使用 if 语句</h1>

    <input type="button" onclick="display()" value="点击这里">

  </body>
</html>
```

```html
<div id="targetDiv"></div>
</body>
</html>
```

你可以在图 2-10 中看到结果，是时候去度假了。这段代码是如何工作的？你首先将两百万这个数字放入一个名为`account`的变量中：

```javascript
var account = 2000000;
```

然后你使用`>`（大于）比较运算符检查`account`是否存储了超过 100 万美元：

```javascript
var account = 2000000;
if(account > 1000000) {
.
.
.
}
```

如果`account`大于一百万（它确实是），JavaScript 会执行花括号中的代码，显示文本“是时候去度假了！”：

```javascript
var account = 2000000;
if(account > 1000000) {
    document.getElementById('targetDiv').innerHTML = 
        "是时候去度假了！";
}
```

这就是`if`语句让你在代码中做出决定的方式，根据条件是否为真来执行代码或不执行。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_66_0.png)

## 动手试试：测试 if 语句

尝试你自己的`if.html`示例版本，创建一个名为`temperature.html`的文件。在你的版本中，创建一个名为`temperature`的变量并为其赋值。然后测试该值是否超过 65，如果是，则显示消息“是时候去野餐了！”

## 使用 else 语句

如果你没有超过 100 万美元在银行里怎么办？换句话说，如果你检查的条件（`account > 1000000`）为假怎么办？如果你想在`if`语句的条件为假时执行代码，你可以添加一个`else`语句。例如，如果你银行里没有 100 万美元，你可能想显示（相当严厉的）消息“回去工作！”你可以通过将要在`if`语句条件为假时运行的代码放在`else`语句（必须跟在`if`语句之后）的花括号中来实现，像这样（这是`else.html`）：



```html
<html>
  <head>
    <title>使用 else 语句</title>
    <script language="javascript">
      function display()
      {
        var account = 500000;
        if(account > 1000000) {
            document.getElementById('targetDiv').innerHTML =
                "是时候去度假了！";
        } else {
            document.getElementById('targetDiv').innerHTML =
                "回去工作！";
        }
      }
    </script>
  </head>
  <body>
    <h1>使用 else 语句</h1>
    <input type="button" onclick="display()" value="点击这里">
    <div id="targetDiv">
    </div>
  </body>
</html>
```

请注意，（很遗憾）我们已将账户变量中的金额更改为 500,000，因此当你运行此代码时，会得到图 2-11 所示的结果。唉。

### 试一试：测试 else 语句

尝试修改你的`temperature.html`文件，使其能够处理温度低于 65 度的情况。在这种情况下，让你的代码显示消息“Turn up the heat!”（调高暖气！）。

## 使用逻辑运算符

在本书中，你还将看到 JavaScript 逻辑运算符的使用。这些运算符——你将在本书中看到`&&`（与）和`||`（或）运算符——将两个或多个条件连接在一起。

例如，如果你想表达：如果你银行存款超过 100 万美元，并且债务少于 50 万美元，那么就该去度假了，你可以用与运算符`&&`将两个条件（`account > 1000000`和`debt < 500000`）组合起来，就像这样（这是`and.html`文件）：

```html
<html>
  <head>
    <title>Using logical operators</title>

    <script language="javascript">

      function display()
      {
        var account = 2000000;
        var debt = 100000;
        if(account > 1000000 && debt < 500000) {
          document.getElementById('targetDiv').innerHTML =
          "Time for a vacation!";
        } else {
          document.getElementById('targetDiv').innerHTML =
          "Get back to work!";
        }
      }
    </script>
  </head>
  <body>
    <h1>Using logical operators</h1>
    <input type="button" onclick="display()" value="Click Here">
    <div id="targetDiv">
    </div>
  </body>
</html>
```

你可以在图 2-12 中看到结果，显示是时候去度假了。

### 试一试：测试“或”运算符

“或”运算符`||`（两个竖线）允许你检查多个条件中是否至少有一个为真。例如，表达式`a || b || c`在`a`、`b`或`c`中任意一个为真时即为真。

使用“或”运算符检查温度是否低于 65 度或高于 85 度，如果是，则显示消息“Please adjust the temperature.”（请调节温度。）

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_69_0.png)

现在我们开始用 JavaScript 真正“烹饪”了；让我们继续看看一些循环结构，从`for`循环开始。

## 使用 for 循环反复执行任务

计算机非常擅长一遍又一遍地执行任务（这是它们的魅力之一——它们可以做苦力活）。JavaScript 让你反复执行任务的方式之一是使用`for`循环，你可以用它多次执行代码（例如，为 25 岁的人显示 25 次“Happy Birthday!”）。

`for`循环的正式语法如下（与之前一样，方括号中的部分是可选的，你需要将斜体部分替换为你自己的 JavaScript 代码）：

```javascript
for ([initial-expression]; [condition]; [increment-expression]) {
    statements
}
```

你通常将`for`循环与一个循环索引（也称为循环计数器）一起使用。循环索引是一个变量，用于跟踪循环已执行的次数。在`initial-expression`部分，你通常将循环索引设置为一个起始值；在`condition`部分，你测试该值以确定是否仍要继续循环；而`increment-expression`部分则让你递增循环计数器。

这是一个例子，`for.html`。这个例子将从 1 加到 100——你可能会很高兴让计算机来做这件事，而不是自己去把所有数字加起来。在这种情况下，你希望计算机循环 100 次，你可以用一个`for`循环和一个循环索引变量像这样实现：

```javascript
var loopIndex;

for(loopIndex = 1; loopIndex <= 100; loopIndex++) {
    .
    .
    .
}
```

在这个循环中，变量`loopIndex`从 1 开始，在每次循环结束时，通过表达式`loopIndex++`给`loopIndex`加 1，因为 JavaScript 的`++`运算符会将其作用的变量递增 1（`--`运算符则会递减 1）。上面的循环在`loopIndex`的值大于 100 时停止（也就是说，只要`loopIndex <= 100`，循环就会继续）。

因此，要计算从 1 到 100 的和，你只需添加这段代码：

```javascript
var loopIndex;
var total = 0;

for(loopIndex = 1; loopIndex <= 100; loopIndex++) {
    total += loopIndex;
}
```

### Ajax：初学者指南

这是在网页中的样子，`for.html`：

```html
<html>
<head>
    <title>Using the for loop</title>
    <script language="javascript">
        function display() {
            var loopIndex;
            var total = 0;
            for(loopIndex = 1; loopIndex <= 100; loopIndex++) {
                total += loopIndex;
            }
            document.getElementById('targetDiv').innerHTML = "The total of 1 to 100 is " + total;
        }
    </script>
</head>
<body>
    <h1>Using the for loop</h1>
    <input type="button" onclick="display()" value="Click Here">
    <div id="targetDiv">
    </div>
</body>
</html>
```

你可以在图 2-13 中看到结果，我们了解到从 1 到 100 的数字之和是 5050。

### 试一试：测试 for 循环

`for`循环是一个很棒的循环，也是所有循环中最基本、必须掌握的一个。试试这个练习：设置一个名为`age`的变量为某人的年龄，然后让你的代码显示“Happy Birthday!”（生日快乐！），显示的次数等于该人的年龄。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_72_0.png)

图 2-13 `for.html`

## 使用 while 循环持续循环

`while`循环在很多方面与`for`循环相似，但它被设计为在条件为真时持续循环：

```javascript
while (condition) {
    statements
}
```

换句话说，这个循环会在条件为真时，持续执行循环体内的语句。

这是一个例子。在这个例子中，我们将使用一个`while`循环和一个学生数组来定位特定的学生。数组就像一个变量集合，你可以用数字索引来索引它，它是存储多个数据元素的便捷结构。事实上，由于你可以用数字索引来访问数组中的元素，因此数组非常适合与循环一起使用，因为你可以用循环来递增数字索引。

让我们看看代码是如何工作的。在这个例子中，我们将存储八名学生的名字，所以我们需要创建一个包含八个元素的数组，你可以这样做：

```javascript
var students = new Array(8);
```

现在你可以自由地为数组中的每个元素分配名称。要访问数组中的特定元素，你可以通过给出数组的名称（`students`），后跟方括号中你想要访问的元素的数字索引（例如`students[5]`）来实现。数组的数字索引从 0 开始，所以你可以像这样为数组中的所有元素分配名称：

```javascript
var students = new Array(8);

students[0] = "George";
students[1] = "Ed";
students[2] = "Stella";
students[3] = "Ted";
students[4] = "Liz";
students[5] = "Cary";
students[6] = "Nancy";
students[7] = "Zack";
```

### Ajax：初学者指南

好的，现在假设你想查看 Nancy 在`students`数组中的位置。你可以用一个`while`循环像这样来做到这一点，我们持续循环直到找到 Nancy：

```javascript
var loopIndex = 0;

while(students[loopIndex] != "Nancy" && loopIndex <
  students.length - 1){
  loopIndex++;
}
```

表达式`students.length`返回数组中元素的总数，因此这样设置`while`循环，它会持续循环，直到`loopIndex`递增到`students.length - 1`（即 7），除非 Nancy 在更早的索引处被找到。

如果在这个`while`循环结束时，变量`loopIndex`小于或等于数组中最后一个元素的索引（即`students.length - 1`），那么我们就找到了 Nancy，我们可以用这种方式报告这一事实（在`while.html`中）：

```html
<html>
  <head>
    <title>Using the while loop</title>

    <script language="javascript">

      function display()
      {
        var loopIndex = 0, students = new Array(6);

        students[0] = "George";
        students[1] = "Ed";
        students[2] = "Stella";
        students[3] = "Ted";
        students[4] = "Liz";
        students[5] = "Cary";
        students[6] = "Nancy";
        students[7] = "Zack";

        while(students[loopIndex] != "Nancy" && loopIndex <
          students.length - 1){
          loopIndex++;
        }
```

### 注意

此处使用了一个快捷方式来设置两个变量：`loopIndex`和`students`数组，它们在一行中声明如下：`var loopIndex = 0, students = new Array(6);`。

你可以在图 2-14 中看到结果，其中我们在`students`数组的索引 6 处找到了 Nancy。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_74_0.png)

### 用户使用的是哪种浏览器？

对于 Ajax 程序员来说，知道用户使用的是哪种浏览器可能非常重要，因为浏览器是你与用户通信的方式，而不同的浏览器具有不同的能力（例如，Internet Explorer 有一个 Firefox 没有的滚动`<marquee>`元素）。

你可以在支持 Ajax 的网页中使用 JavaScript 来确定用户使用的浏览器。为此，你需要检查内置`navigator`对象的`userAgent`属性中的文本字符串（在 JavaScript 中通过`navigator.userAgent`访问）。

在 JavaScript 中，文本字符串实际上是具有自身属性和方法的对象。要搜索文本字符串，你可以使用字符串的`indexOf`方法，该方法返回你要搜索的子字符串在主字符串中的索引（即子字符串在主字符串中的起始位置，其中第一个字符是字符 0）。如果在主字符串中未找到子字符串，`indexOf`将返回一个负值。

因此，例如，要查看`navigator.userAgent`中保存的浏览器标识字符串是否包含文本 "Firefox"，你可以检查表达式`navigator.userAgent.indexOf("Firefox")`的返回值——如果它非负，则字符串`navigator.userAgent`包含单词 "Firefox"。

除了`navigator.userAgent`字符串外，本页（`browser.html`）还使用了另一个字符串`navigator.appName`。`navigator.appName`字符串使`browser.html`能够对浏览器类型做出初步判断——如果它包含 "Netscape"，你使用的是 Firefox（或 Netscape Navigator），如果它包含 "MSIE"，你使用的是 Microsoft Internet Explorer。

以下是`browser.html`的内容（`browser.html`）：

```html
<html>
  <head>
    <title>
      What browser do you have?
    </title>

    <script language="javascript">

    var begin, end

    function display()
    {
      if(navigator.appName == "Netscape") {
        if(navigator.userAgent.indexOf("Firefox") > 0) {
          begin = navigator.userAgent.indexOf("Firefox") +
            "Firefox".length + 1;
          end = navigator.userAgent.length;
          document.getElementById("targetDiv").innerHTML =
            "You are using Firefox " +
            navigator.userAgent.substring(begin, end);
        }
      }
      if (navigator.appName == "Microsoft Internet Explorer") {
          begin = navigator.userAgent.indexOf("MSIE ") +
                  "MSIE ".length;
          if(navigator.userAgent.indexOf(";", begin) > 0) {
              end = navigator.userAgent.indexOf(";", begin);
          } else {
              end = navigator.userAgent.indexOf(")", begin)
                    + 2;
          }
          document.getElementById("targetDiv").innerHTML =
              "You are using Internet Explorer " +
              navigator.userAgent.substring(begin, end);
      }
    }
    </script>
  </head>

  <body>
    <h1>Determining browser type and version</h1>

    <input type="button" onclick="display()" value="Click Here">

    <div ID="targetDiv"></div>
  </body>
</html>
```



你可以在图 2-15 中看到结果，其中`browser.html`正确识别了 Internet Explorer。在图 2-16 中，它识别的是 Firefox。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_76_0.png)

图 2-15 确定浏览器类型：Internet Explorer

## Ajax 入门指南

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_77_0.png)

图 2-16 确定浏览器类型：Firefox

### 试一试：使用 browser.html

确保你理解 JavaScript 文件`browser.html`的工作原理。如果你理解了，那么你在一章 JavaScript 的学习中就已经取得了很大进步！在你自己的浏览器中让`browser.html`工作起来。

# 第 3 章：创建 Ajax 应用程序

## 关键技能与概念

- 创建`XMLHttpRequest`对象
- 配置`XMLHttpRequest`对象
- 使用匿名函数处理从服务器下载的数据
- 从服务器获取文本数据
- 使用 Ajax 以及 GET 和 PUT HTTP 方法将数据传递给服务器
- 从服务器获取 XML 数据并解码该数据
- 通过将数据传递给服务器来获取 XML 数据

现在是开始讨论 Ajax 的时候了，我们将通过逐一剖析一个可工作的 Ajax 应用程序来做到这一点。你在第 2 章中已经简要瞥见了我们在本章将要研究的程序——`ajax.html`。你可以在图 3-1 中看到它的工作情况。当你点击标有“获取消息”的按钮时，`ajax.html`将从服务器获取一个名为`data.txt`的文件的内容（内容如下所示）：

```text
Welcome to Ajax!
```

并将该文本显示在网页中，如图 3-2 所示。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_79_0.png)

图 3-1 `ajax.html`示例

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_80_0.png)

这个示例是一个真正的 Ajax 示例——它使用 Ajax 在后台从服务器获取数据，并在浏览器中更新其网页，而不会导致页面刷新。以下是`ajax.html`的内容——我们将在本章中逐步分解这个支持 Ajax 的网页：

```html
<html>
  <head>
    <title>An Ajax example</title>
    <script language="javascript">
      var XMLHttpRequestObject = false;

      if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
          ActiveXObject("Microsoft.XMLHTTP");
      }

      function getData(dataSource, divID)
      {
        if(XMLHttpRequestObject) {
          var obj = document.getElementById(divID);
          XMLHttpRequestObject.open("GET", dataSource);

          XMLHttpRequestObject.onreadystatechange = function()
          {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
              obj.innerHTML = XMLHttpRequestObject.responseText;
            }
          }
          XMLHttpRequestObject.send(null);
        }
      }
    </script>
  </head>
  <body>
    <h1>An Ajax example</h1>
    <form>
      <input type="button" value="Fetch the message"
             onclick="getData('data.txt', 'targetDiv')">
    </form>
    <div id="targetDiv">
      <p>The fetched message will appear here.</p>
    </div>
  </body>
</html>
```

### 让`ajax.html`工作起来

为了在本章取得进展，你必须能让`ajax.html`运行起来。正如第 2 章提到的，你必须将`ajax.html`和`data.txt`放在一个可以通过浏览器访问的 Web 服务器上。仅仅将这些文件放到你的硬盘上，然后用浏览器打开它们是行不通的，因为 Ajax 必须与真正的 Web 服务器交互，一个能够根据请求在后台发送数据的服务器。

所以，现在请确保你能让`ajax.html`运行起来。从本书的可下载代码的`chapter3`目录中复制`ajax.html`和`data.txt`。将这两个文件放入 Web 服务器上的一个目录中——例如，如果你已经在那里托管网页，可以使用你的 ISP 的 Web 服务器。或者你甚至可以在自己的计算机上设置一个 Web 服务器。无论哪种情况，请确保你能获得如图 3-2 所示的结果。

### 拆解`ajax.html`

现在来看看`ajax.html`是如何工作的。通过移除 Ajax 部分，你可以在`ajax.html`中识别出基本网页的框架，这给你提供了一个包含`<head>`和`<body>`部分的基本页面，并且在`<body>`中有一个`<div>`元素用于显示从服务器获取的数据：

```html
<html>
  <head>
    <title>An Ajax example</title>
           .
           .
           .
  </head>

  <body>

    <H1>An Ajax example</H1>
           .
           .
           .

    <div id="targetDiv">
      <p>The fetched message will appear here.</p>
    </div>

  </body>
</html>
```

`ajax.html`中还有一个按钮，当用户点击该按钮时，浏览器会调用 JavaScript 函数`getData`来启动页面的 Ajax 部分：

```html
<html>
  <head>
    <title>An Ajax example</title>
           .
           .
           .
  </head>

  <body>

    <H1>An Ajax example</H1>

    <form>
      <input type = "button" value = "Fetch the message"
             onclick = "getData('data.txt', 'targetDiv')">
    </form>

<div id="targetDiv">
    <p>The fetched message will appear here.</p>
</div>
</body>
</html>
```

### 创建 JavaScript

有两个数据项被传递给 JavaScript`getData`函数：服务器上要读取的文件名（`data.txt`），以及用于显示从服务器获取的文本的`<div>`元素的 ID（`targetDiv`）。我们可以在`<script>`元素中创建`getData`函数，像这样读取这两个数据项：

```html
<html>
  <head>
    <title>An Ajax example</title>
    <script language = "javascript">
      function getData(dataSource, divID)
      {
        .
        .
        .
      }
    </script>
  </head>
  <body>
    .
    .
    .
  </body>
</html>
```

JavaScript`getData`函数的首要任务是检查我们是否已成功创建了`XMLHttpRequest`对象，该对象是`ajax.html`将用于与服务器通信的基础。我们将要创建的`XMLHttpRequest`对象是 Ajax 的核心——它允许 JavaScript 代码与服务器通信并从服务器下载数据。此对象将存储在一个名为`XMLHttpRequestObject`的全局变量中：

```html
<html>
  <head>
    <title>An Ajax example</title>
    <script language = "javascript">
      var XMLHttpRequestObject = false;
        .
        .
        .
    </script>
  </head>
  <body>
    .
    .
    .
  </body>
</html>
```

在`getData`函数中，我们使用一个`if`语句来检查是否已成功创建`XMLHttpRequest`对象——如果没有，`if`语句将失败，这意味着我们不会尝试使用 Ajax 来联系服务器（注意变量`XMLHttpRequestObject`被初始化为`false`，这意味着除非我们成功创建了`XMLHttpRequest`对象，否则`if`语句将失败）：

```html
<html>
  <head>
    <title>An Ajax example</title>

    <script language = "javascript">
      var XMLHttpRequestObject = false;
          .
          .
          .
      function getData(dataSource, divID)
      {
        if(XMLHttpRequestObject) {
            .
            .
            .
        }
      }
    </script>
  </head>

  <body>
    .
    .
    .
  </body>
</html>
```

那么，我们如何创建`XMLHttpRequest`对象呢？

### 创建`XMLHttpRequest`对象

我们将在`ajax.html`中添加代码，以便在浏览器加载`ajax.html`后立即创建我们将用于与服务器通信的`XMLHttpRequest`对象。这意味着将该代码放在`getData`函数外部，因为该函数仅在用户点击按钮时才会被调用。

那么，如何创建一个`XMLHttpRequest`对象呢？该对象内置于浏览器中，但根据`ajax.html`运行的浏览器不同，你访问它的方式也不同。Netscape Navigator（7.0 版及更高版本）、Apple Safari（1.2 版及更高版本）和 Firefox 允许你直接使用如下代码创建`XMLHttpRequest`对象：

```javascript
XMLHttpRequestObject = new XMLHttpRequest();
```

在这些浏览器中，`XMLHttpRequest`对象可以通过浏览器的`window`对象来访问，你可以通过检查`window.XMLHttpRequest`是否存在来判断`window`对象是否可以这样使用。如果存在，说明你正在使用 Netscape Navigator、Firefox 或 Apple Safari，可以像这样创建`XMLHttpRequest`对象并将其存储在变量`XMLHttpRequestObject`中：

```html
<html>
	<head>
		<title>An Ajax example</title>
		<script language = "javascript">
			var XMLHttpRequestObject = false;
			if (window.XMLHttpRequest) {
				XMLHttpRequestObject = new XMLHttpRequest();
			}
			.
			.
			.
			function getData(dataSource, divID)
			{
				if(XMLHttpRequestObject) {
				.
				.
				.
			}
			}
		</script>
	</head>
	<body>
		.
		.
		.
	</body>
</html>
```

但如果你使用的是 Internet Explorer 呢？在这种情况下，你可以使用以下 JavaScript 来创建`XMLHttpRequest`对象：

```javascript
XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
```

那么`ajax.html`如何确定它正在与 Internet Explorer 交互呢？在这种情况下，`window.XMLHttpRequest`不存在——但`window.ActiveXObject`存在，这意味着你可以使用此代码在 Internet Explorer 中创建`XMLHttpRequest`对象：

```html
<html>
  <head>
    <title>An Ajax example</title>

    <script language = "javascript">
      var XMLHttpRequestObject = false;

      if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
          ActiveXObject("Microsoft.XMLHTTP");
      }

      function getData(dataSource, divID)
      {
        if(XMLHttpRequestObject) {
          .
          .
          .
        }
      }
    </script>
  </head>

  <body>
    .
    .
    .
  </body>
</html>
```

好的，这就创建了我们将用于在幕后与服务器通信的`XMLHttpRequest`对象。尽管不同浏览器支持的`XMLHttpRequest`对象有所不同，但对于几乎所有 Ajax 工作，你都使用该对象相同的基本属性和方法——而且幸运的是，这些基本属性和方法在不同的浏览器中是相同的。

你可以在表 3-1 中看到 Internet Explorer`XMLHttpRequest`对象的属性，在表 3-2 中看到其方法。此对象在 Mozilla、Netscape Navigator 和 Firefox 中的属性出现在表 3-3 中，方法出现在表 3-4 中。Apple 尚未发布其`XMLHttpRequest`对象的完整属性和方法版本，但它已发布了一组常用属性（出现在表 3-5 中）和常用方法（出现在表 3-6 中）。

68 Ajax: A Beginner's Guide

**表 3-1 Internet Explorer 的`XMLHttpRequest`对象属性**

| 属性 | 描述 |
| --- | --- |
| `onreadystatechange` | 包含当`readyState`属性值更改时应调用的事件处理程序的名称。可读/写。 |
| `readyState` | 包含请求的状态。只读。 |
| `responseBody` | 包含响应体，这是 HTTP 响应可以返回的一种方式。只读。 |
| `responseStream` | 包含响应流，即到服务器的二进制流。只读。 |
| `responseText` | 包含作为字符串的响应体。只读。 |
| `responseXML` | 包含作为 XML 的响应体。只读。 |
| `status` | 包含请求返回的 HTTP 状态码。只读。 |
| `statusText` | 包含 HTTP 响应状态文本。只读。 |

**表 3-2 Internet Explorer 的`XMLHttpRequest`对象方法**

| 方法 | 描述 |
| --- | --- |
| `abort` | 中止 HTTP 请求。 |
| `getAllResponseHeaders` | 返回所有 HTTP 头。 |
| `getResponseHeader` | 返回一个 HTTP 头的值。 |
| `open` | 打开对服务器的请求。 |



| `send` | 向服务器发送 HTTP 请求。 |
|---|---|
| `setRequestHeader` | 设置 HTTP 头的名称和值。 |

**表 3-3 Mozilla、Firefox 和 Netscape Navigator 的 `XMLHttpRequest` 对象属性**

| 属性 | 描述 |
|---|---|
| `channel` | 包含用于执行请求的通道。只读。 |
| `readyState` | 包含请求的状态。只读。 |
| `responseText` | 包含作为字符串的响应体。只读。 |
| `responseXML` | 包含作为 XML 的响应体。只读。 |
| `status` | 包含请求返回的 HTTP 状态码。只读。 |
| `statusText` | 包含 HTTP 响应状态文本。只读。 |

### `XMLHttpRequest` 对象方法

| 方法 | 描述 |
|---|---|
| `abort` | 中止 HTTP 请求。 |
| `getAllResponseHeaders` | 返回所有 HTTP 头。 |
| `getResponseHeader` | 返回一个 HTTP 头的值。 |
| `openRequest` | 原生（非脚本）打开请求的方法。 |
| `overrideMimeType` | 覆盖服务器返回的 MIME 类型。 |

**表 3-4** Mozilla、Firefox 和 Netscape Navigator 的 `XMLHttpRequest` 对象方法

### `XMLHttpRequest` 对象属性

| 属性 | 描述 |
|---|---|
| `onreadystatechange` | 包含当 `readyState` 属性值改变时应调用的事件处理函数的名称。可读/可写。 |
| `readyState` | 包含请求的状态。只读。 |
| `responseText` | 包含作为字符串的响应体。只读。 |
| `responseXML` | 包含作为 XML 的响应体。只读。 |
| `status` | 包含请求返回的 HTTP 状态码。只读。 |
| `statusText` | 包含 HTTP 响应状态文本。只读。 |

**表 3-5** Apple Safari 的 `XMLHttpRequest` 对象属性

### Apple Safari 的 `XMLHttpRequest` 对象方法

| 方法 | 描述 |
|---|---|
| `abort` | 中止 HTTP 请求。 |
| `getAllResponseHeaders` | 返回所有 HTTP 头。 |
| `getResponseHeader` | 返回一个 HTTP 头的值。 |
| `open` | 向服务器打开一个请求。 |
| `send` | 向服务器发送一个 HTTP 请求。 |
| `setRequestHeader` | 设置一个 HTTP 头的名称和值。 |

**表 3-6** Apple Safari 的 `XMLHttpRequest` 对象方法

### 打开 `XMLHttpRequest` 对象

现在我们有了一个 `XMLHttpRequest` 对象，该如何使用它呢？你可以从打开它开始，这允许你配置它，为连接服务器和下载数据做准备。

当 `ajax.html` 在浏览器中首次加载时，它会尝试创建一个 `XMLHttpRequest` 对象。当用户点击按钮使用 Ajax 从服务器获取数据时，会调用 `getData` 函数，该函数做的第一件事就是检查 `XMLHttpRequest` 对象是否成功创建：

```html
<script language="javascript">
var XMLHttpRequestObject = false;

if (window.XMLHttpRequest) {
  XMLHttpRequestObject = new XMLHttpRequest();
} else if (window.ActiveXObject) {
  XMLHttpRequestObject = new
    ActiveXObject("Microsoft.XMLHTTP");
}

function getData(dataSource, divID)
{
  if(XMLHttpRequestObject) {
    .
    .
    .
  }
}
</script>
```

万一 `XMLHttpRequest` 对象无法创建，你可以添加代码向用户解释他们的浏览器不支持 Ajax，如下所示：

```javascript
function getData(dataSource, divID)
{
  if(XMLHttpRequestObject) {
    .
    .
    .
  }
  else {
    var obj = document.getElementById(divID);
    obj.innerHTML = "抱歉，您的浏览器不支持 Ajax。";
  }
}
```

# 第 3 章：创建 Ajax 应用程序

是时候打开 `XMLHttpRequest` 对象了。这样做允许你配置 `XMLHttpRequest` 对象，例如，设置它连接服务器时要联系的 URL。下面是你通常如何使用 `XMLHttpRequest` 对象的 `open` 方法（一如既往，方括号中的项是可选项，斜体项是你需要自己填写的占位符）：

```javascript
open("method", "URL"[, asyncFlag[, "userName"[, "password"]]])
```

下表解释了各个参数的含义：

| `method` | 用于打开连接的 HTTP 方法，例如 GET、POST、PUT、HEAD 或 PROPFIND。 |
|---|---|
| `URL` | 请求的 URL。 |
| `asyncFlag` | 一个布尔值，指示调用是否异步。默认为 true。 |
| `userName` | 你的账户的用户名。 |
| `password` | 用于连接你账户的密码。 |

下面的代码展示了 `ajax.html` 如何使用 `XMLHttpRequest` 对象的 `open` 方法。在本例中，它使用 HTTP GET 方法联系服务器（这是联系服务器的正常方式——我们将在本章后面讨论另一个选项 POST 方法时看到更多相关内容），并传递它正在查找的文件的 URL，该 URL 作为 `dataSource` 参数传递给 `getData` 函数。

```javascript
function getData(dataSource, divID)
{
    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", dataSource);
        .
        .
        .
    }
}
```

像这样使用 `open` 方法配置 `XMLHttpRequest` 对象——它*不会*连接或打开任何到服务器的连接。实际的连接过程将在几页后介绍。

请注意，`XMLHttpRequest` 对象被配置为访问的 URL 只是一个文件名，`data.txt`，正如你在按钮点击时调用 `getData` 时看到的：

```html
<body>

<H1>一个 Ajax 示例</H1>

<form>
    <input type="button" value="获取消息"
        onclick="getData('data.txt', 'targetDiv')">
</form>

<div id="targetDiv">
  <p>获取的消息将显示在这里。</p>
</div>
</body>
```

以这种方式引用文件只有在该文件（`data.txt`）与网页（`ajax.html`）位于同一目录中时才有效。换句话说，如果你只给出一个文件名，浏览器将假定该文件位于当前显示的网页所在的同一目录中。

现在假设 `data.txt` 文件位于包含 `ajax.html` 的目录的子目录 `data` 中。在这种情况下，你可以使用相对路径 `data/data.txt` 来引用它（在 Web 服务器上使用正斜杠 `/`，而不是 Windows 中用于表示子目录的反斜杠）：

```html
<body>
  <H1>一个 Ajax 示例</H1>
  <form>
    <input type="button" value="获取消息"
      onclick="getData('data/data.txt', 'targetDiv')">
  </form>
  <div id="targetDiv">
    <p>获取的消息将显示在这里。</p>
  </div>
</body>
```

你也可以为要获取的数据提供一个完整的 URL，像这样：

```html
<body>
  <H1>一个 Ajax 示例</H1>
  <form>
    <input type="button" value="获取消息"
      onclick="getData('http://www.starpowder.com/data.txt',
      'targetDiv')">
  </form>
  <div id="targetDiv">
    <p>获取的消息将显示在这里。</p>
  </div>
</body>
```

并且该 URL 不必是一个文件的 URL——它也可以是任何 Web 资源，例如一个 PHP 脚本（正如你很快将在本书中看到的，PHP 是一种在 Web 服务器上运行的编程语言，它允许你控制发送回浏览器的 HTML 和数据）：

```html
<body>

    <H1>一个 Ajax 示例</H1>

    <form>
        <input type="button" value="获取消息"
            onclick="getData('http://www.starpowder.com/data.php',
            'targetDiv')">
    </form>

    <div id="targetDiv">
        <p>获取的消息将显示在这里。</p>
    </div>

</body>
```

然而，这里有一点需要注意：如果你连接的 URL，例如 `http://www.starpowder.com/data.php`，和试图下载该 URL 的启用 Ajax 的页面（此处为 `ajax.html`）位于不同的服务器上，你将会遇到安全问题。如果你的启用 Ajax 的页面试图从不同服务器后台下载数据，你的浏览器会怀疑有不良操作，并会通过对话框向用户请求许可后才会继续。

然而，让用户响应一个对话框，并不符合 Ajax 在后台、不唐突地执行操作的理念。我们将在第 4 章中看到如何绕过这个限制。

为简单起见，本书中的示例大多从启用 Ajax 的 HTML 页面所在的同一 Web 服务器目录下载数据。

现在你已经配置了 `XMLHttpRequest` 对象。下一步是为数据下载做好准备。

### 为数据下载做准备

Ajax 中的 **A** 代表 *asynchronous*（异步），这意味着你不需要坐着等待 Ajax 下载发生。在下载进行期间，浏览器可以做其他事情——例如，与用户交互。这意味着 Ajax 需要在数据已下载并准备好使用时通知浏览器，这通过一个 *回调* 函数发生。这个函数是 Ajax 在你的数据正在下载或已完全下载时调用的。你如何告诉 Ajax 你想调用哪个函数？

你告诉 `XMLHttpRequest` 对象。该对象有一个名为 `onreadystatechange` 的属性，你将回调函数赋值给它。作为它可能如何工作的一个例子，假设你有

### Ajax：初学者指南

一个回调函数简单命名为 `callback`。你可以通过将函数赋值给 `onreadystatechange` 属性，来让 `XMLHttpRequest` 对象调用该函数，方式如下：

```javascript
function getData(dataSource, divID)
{
    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", dataSource);
        XMLHttpRequestObject.onreadystatechange = callback()
    }
}
function callback()
{
.
.
.
}
```

现在，当你所下载数据的状态发生变化时，例如下载完成，回调函数就会被调用。

这方法可行，但在 Ajax 中，通常采用一种快捷方式——使用*匿名*函数，即没有任何名称的函数。你可以仅用 `function` 关键字创建匿名函数，后跟括号括起来的传给该函数的参数（此处没有参数），然后是用花括号括起来的函数体。以下是 `ajax.html` 中的示例：

```javascript
function getData(dataSource, divID)
{
    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", dataSource);
        XMLHttpRequestObject.onreadystatechange = function()
        {
.
.
.
        }
    }
}
```

因此，这里发生的情况是：当 `XMLHttpRequest` 对象正在下载的数据状态发生变化时，匿名函数将被调用，这意味着 `function` 关键字之后花括号内的代码将被执行。

在匿名函数内部，我们需要检查已下载的数据：

下载是否完成？我们是否可以使用这些数据？你可以通过 `XMLHttpRequest` 对象的两个属性来确定：`readyState` 和 `status`。

`readyState` 属性告诉你数据下载的进展。以下是该属性可能的取值——你希望看到的值是 4，因为这表示数据已完全下载：

| 0 | 未初始化 |
|---|---|
| 1 | 加载中 |
| 2 | 已加载 |
| 3 | 交互中 |
| 4 | 完成 |

`status` 属性是包含下载实际状态的属性。这实际上就是你尝试下载网页时获得的正常 HTTP 状态码。例如，如果你要查找的数据未找到，你将在 `status` 属性中得到值 404。以下是一些可能的取值——请注意，你希望看到的值是 200，这意味着下载正常完成：

| 状态码 | 描述 |
|---|---|
| 200 | OK |
| 201 | Created |
| 204 | No Content |
| 205 | Reset Content |
| 206 | Partial Content |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 405 | Method Not Allowed |
| 406 | Not Acceptable |
| 407 | Proxy Authentication Required |
| 408 | Request Timeout |
| 411 | Length Required |
| 413 | Requested Entity Too Large |
| 414 | Requested URL Too Long |
| 415 | Unsupported Media Type |
| 500 | Internal Server Error |
| 501 | Not Implemented |
| 502 | Bad Gateway |
| 503 | Service Unavailable |
| 504 | Gateway Timeout |
| 505 | HTTP Version Not Supported |

我们将通过检查 `readyState` 属性来开始处理下载的数据。

### 使用 `readyState` 属性

`readyState` 属性让你了解下载的状态，我们希望等待该属性的值等于 4，这意味着下载完成。以下是在匿名函数中的写法：

```javascript
function getData(dataSource, divID)
{
    if (XMLHttpRequestObject) {

        XMLHttpRequestObject.open("GET", dataSource);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4
                .
                .
                .
            }
        }

    }
}
```

好的，如果我们正在执行此 `if` 语句内的代码，我们就知道数据下载已完成。但它是成功完成，还是出现了错误？要检查这一点，你必须检查 `status` 属性。

### 使用 `status` 属性

`status` 属性包含与数据传输状态对应的 HTTP 代码。我们希望看到值 200，这表示数据传输正常。以下是我们如何确保 `XMLHttpRequest` 对象的 `status` 属性包含值 200：



```javascript
function getData(dataSource, divID)
{
    if (XMLHttpRequestObject) {
        
        XMLHttpRequestObject.open("GET", dataSource);
        
        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                .
                .
                .
            }
        }
        
    }
}
```

现在我们已经验证了使用 Ajax 从服务器获取的数据已成功完成。我们如何显示获取的数据？

### 显示获取的数据

我们希望在其中显示下载数据的 `<div>` 元素的 HTML ID 被传递给`getData`函数，并命名为`divID`：

```javascript
function getData(dataSource, divID)
{
    .
    .
    .
}
```

我们可以通过以下方式创建一个对应于该 `<div>` 元素的名为`obj`的对象：

```javascript
function getData(dataSource, divID)
{
    if (XMLHttpRequestObject) {
        var obj = document.getElementById(divID);
        XMLHttpRequestObject.open("GET", dataSource);
```

```javascript
XMLHttpRequestObject.onreadystatechange = function()
{
    if (XMLHttpRequestObject.readyState == 4 &&
        XMLHttpRequestObject.status == 200) {
        ...
    }
}
```

现在我们已成功下载要显示的数据，如何从`XMLHttpRequest`对象中获取该数据并将其显示在 `<div>` 元素中？你可以从`XMLHttpRequest`对象的`responseText`属性中获取下载的文本。该属性是`XMLHttpRequest`对象存储下载的纯文本的地方（如果你下载的是 XML，正如我们稍后将在本章中看到的，你读取该 XML 的属性名为`responseXML`）。

因此，以下是我们如何在 `<div>` 元素中显示下载的文本：

```javascript
function getData(dataSource, divID)
{
    if (XMLHttpRequestObject) {
        var obj = document.getElementById(divID);
        XMLHttpRequestObject.open("GET", dataSource);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                obj.innerHTML = XMLHttpRequestObject.responseText;
            }
        }
        XMLHttpRequestObject.send(null);
    }
}
```

太好了——现在我们已准备好处理从服务器下载数据。为什么只是“准备好”处理数据下载？因为我们实际上还没有启动下载，这就是原因。我们如何实际连接到服务器以开始实际的下载过程？

### 连接到服务器

事实证明，到目前为止我们所做的只是为使用 Ajax 连接到服务器做好准备。我们创建了`XMLHttpRequest`对象，使用其`open`方法对其进行了配置，并设置了一个回调函数来检查下载并显示下载的文本。但我们实际上还没有连接到服务器并启动整个下载过程。

你如何连接到服务器？这取决于你用于连接的 HTTP 方法。在本例中，我们使用的是 GET 方法，因此你要调用`XMLHttpRequest`对象的`send`方法，并传入值`null`，这是 JavaScript 中表示空值的占位符（当使用 POST HTTP 方法连接到服务器时，你传入不同的参数）。在`ajax.html`中如下所示：

```javascript
function getData(dataSource, divID)
{
    if(XMLHttpRequestObject) {
        var obj = document.getElementById(divID);
        XMLHttpRequestObject.open("GET", dataSource);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                obj.innerHTML = XMLHttpRequestObject.responseText;
            }
        }

        XMLHttpRequestObject.send(null);
    }
}
```

看——你完成了！现在你已经完成了`ajax.html`，当你在浏览器中加载它并点击按钮时，页面使用 Ajax 与服务器通信并下载文本数据。很酷。

我们已经能够从一个名为`data.txt`的文件下载文本并显示它。另一方面，总是下载同一个文件可能会有点无聊。为什么不有一些可以在服务器上变化的数据呢？这就是服务器端编程的用武之地。

### 添加一些服务器端编程

为了在服务器上进行一些编程，我们将使用 PHP，一种服务器端语言（即运行在 Web 服务器上，而不是用户机器上的语言），它已成为 Ajax 开发人员最受欢迎的选择。使用 PHP（在第 9 章正式介绍），我们将让服务器发回变化的数据，而不是总是只获取同一个文件`data.txt`的内容。

`data.txt`的 PHP 等效物是`data.php`，一个 PHP 脚本，它将向浏览器发回一条消息。要在此处操作，你需要一个支持 PHP 的服务器，如第 9 章深入讨论的那样。我们以以下标记开始`data.php`，它向服务器表明这是一个 PHP 脚本，并应作为脚本执行：

```php
<?php
    .
    .
    .
?>
```

Ajax: 初学者指南

图 3-3 `data.php`

要将文本实际发送回浏览器，我们可以使用 PHP 的`echo`语句：

```php
<?php
    echo 'This text comes to you thanks to PHP.';
?>
```

就这样——很简单。你可以在浏览器中查看`data.php`的效果（此时还未使用 Ajax），如图 3-3 所示。

现在，让我们获取`data.php`发送回浏览器的文本——这次使用 Ajax 技术。为此，你只需将访问的 URL 从`data.txt`改为`data.php`，如下所示（这是`ajax2.html`）：

```html
<html>
  <head>
    <title>An Ajax example using PHP</title>

    <script language = "javascript">
      var XMLHttpRequestObject = false;

      if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
          ActiveXObject("Microsoft.XMLHTTP");
      }

      function getData(dataSource, divID)
      {
        if(XMLHttpRequestObject) {
          var obj = document.getElementById(divID);
          XMLHttpRequestObject.open("GET", dataSource);

          XMLHttpRequestObject.onreadystatechange = function()
          {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
              obj.innerHTML = XMLHttpRequestObject.responseText;
            }
          }
          XMLHttpRequestObject.send(null);
        }
      }
    </script>
  </head>
  <body>
    <H1>An Ajax example using PHP</H1>
    <form>
      <input type = "button" value = "Fetch the message"
      onclick = "getData('data.php', 'targetDiv')">
    </form>
    <div id="targetDiv">
      <p>The fetched message will appear here.</p>
    </div>
  </body>
</html>
```

就是这样？是的，就是这样。现在你正在使用 Ajax 访问`data.php`，而不是访问`data.txt`。你可以在图 3-4 中看到`ajax2.html`。

现在当你点击按钮时，Ajax 在后台被用来获取`data.php`返回的数据，如图 3-5 所示。

### 让`ajax2.html`工作起来

有一个可以运行 PHP 的服务器吗？互联网上有很多，如果你想的话，也可以将 PHP 下载到自己的计算机上，如第 9 章所述。如果你能在服务器上执行 PHP，可以尝试一下`ajax2.html`。

为此，请将`ajax2.html`和`data.php`放入同一目录（如果需要，可更改`data.php`的权限以便在你的服务器上执行），然后在浏览器中导航到`ajax2.html`。希望你能看到如图 3-4 和图 3-5 所示的页面。

在深入讨论 PHP 之前，我们将一直使用第 9 章。但如果你要使用 Ajax，能够进行服务器端编程很重要——最常见的组合是 Ajax 和 PHP。

好了，现在我们已经成功从`data.php`读取了文本，这很有趣——但时间久了，它会变得无聊，因为那段文本从不改变。通过向服务器发送数据来与其进行交互怎么样？在接下来的两节中，我们将研究两种与服务器通信的方法：HTTP GET 方法和 HTTP POST 方法，先从前者开始。

### 使用 GET 向服务器发送数据

与服务器通信是 Ajax 功能的核心，为了使服务器对你发送的内容做出响应，你需要能够在服务器上使用某种形式的编程。在本节中，我们将创建一个名为`dataresponder.php`的 PHP 脚本，你可以向它发送数据。

# 第 3 章：创建 Ajax 应用程序

如果你向`dataresponder.php`发送一个值 1，它将返回文本“The server got a value of 1”，如果你发送一个值 2，该脚本将返回文本“The server got a value of 2”。

## 使用 URL 编码发送数据

GET 方法允许你通过将文本附加到用于访问服务器的 URL 末尾来向服务器发送文本数据。例如，如果你想向服务器发送名称 Steve，你可以将“Steve”作为参数的值传递，就像使用 JavaScript 函数一样。我们可以将该参数命名为“name”，以下是你将“Steve”分配给参数“name”并使用 HTTP GET 方法将所有内容发送到服务器的方法（注意，你使用问号将你的数据与 URL 的导航部分分开）：

```text
http://www.server.com/script.php?name=Steve
```

在服务器上，你的 PHP 脚本可以请求获取与“name”参数对应的值，它将接收到值“Steve”。

如果你想向服务器传递两个或多个数据项怎么办？你要将要传递的数据分成参数/值对（即“参数=值”），并用与符号`&`分隔这些对。这里有一个例子：

```text
http://www.server.com/script.php?firstname=Steve&lastname=Holzner
```

如果你想发送的数据包含空格怎么办？你不能在 URL 中包含空格。相反，你应该用加号`+`替换空格。这里有一个例子：

```text
http://www.server.com/script.php?name=Steve+Holzner
```

像这样向 URL 添加数据称为 URL 编码，它允许你将数据发送到服务器（只要该数据是文本）。但是，请注意，你发送的文本是你正在访问的（非常公开的）URL 的一部分，因此使用 GET 方法没有任何隐私可言。POST 方法将你要发送的数据编码在发送给服务器的请求的 HTTP 头中，在保持隐私方面做得更好（如本章后面“使用 POST 向服务器发送数据”中所讨论的）。

因此，这意味着我们可以像这样向`dataresponder.php`脚本发送一个值 1，这里我们命名发送到服务器的参数为`data`，并将`data`赋值为 1：

```text
http://www.server.com/dataresponder.php?data=1
```

要向服务器发送一个值 2，你可以这样做：

```text
http://www.server.com/dataresponder.php?data=2
```

现在我们需要编写我们的 PHP 脚本`dataresponder.php`来读取名为“data”的参数，并通过向浏览器发送正确的文本做出响应：“The server got a value of 1”或“The server got a value of 2”。

### 编写 PHP 代码

我们以常用的 PHP 标记开始`dataresponder.php`，表明这是一个期望由服务器执行的 PHP 脚本：

```php
<?php
...
?>
```

现在我们需要访问通过 GET 方法发送给我们的“data”参数。PHP 包含一个名为`$_GET`的特殊数组，允许你恢复通过 GET 方法发送给你的 PHP 脚本的数据。你要做的就是使用你想要的值的参数的名称作为`$_GET`数组的索引。换句话说，要恢复发送给`dataresponder.php`的名为“data”的参数的值，你只需使用`$_GET["data"]`。

好了，现在我们有了从网页发送给我们的数据，需要检查该数据是 1 还是 2。PHP 的语法在很多方面类似于 JavaScript，因此我们可以使用 PHP 的`if`语句来检查“data”是否包含 1 或 2（注意，`==`是 PHP 中的相等比较运算符，就像在 JavaScript 中一样）：

```php
<?php
if ($_GET["data"] == "1") {
...
}
?>
```

此时，我们知道自己被传递了一个值 1，因此我们可以用 PHP 的`echo`语句向浏览器发回确认消息“The server got a value of 1”：

```php
<?php
if ($_GET["data"] == "1") {
    echo 'The server got a value of 1';
}
...
?>
```

相反，如果我们被发送了一个值 2，

```php
<?php
if ($_GET["data"] == "1") {
    echo 'The server got a value of 1';
}
if ($_GET["data"] == "2") {
```

那么我们可以向浏览器发回消息“The server got a value of 2”：

```php
<?php
if ($_GET["data"] == "1") {
    echo 'The server got a value of 1';
}
if ($_GET["data"] == "2") {
    echo 'The server got a value of 2';
}
?>
```

你可以使用类似这样的 URL 在浏览器中测试`dataresponder.php`，向其发送一个值 1：

`http://www.server.com/dataresponder.php?data=1`

你可以在图 3-6 中看到结果，其中`dataresponder.php`正确识别了发送给它的值。

太好了，`dataresponder.php`准备就绪。现在我们必须编写支持 Ajax 的页面来与之交互。

### 与`dataresponder.php`交互



让我们编写支持 Ajax 的页面 `ajax3.html` 来与 `dataresponder.php` 交互。我们需要在这里放置两个按钮：一个用于向 `dataresponder.php` 发送值 1，另一个用于发送值 2。第一个按钮——用于向 `dataresponder.php` 发送值 1 的按钮——在 HTML 中是这样的：

```html
<form>
    <input type="button" value="Fetch message 1"
    .
    .
    .
</form>
```

图 3-6 测试 `dataresponder.php`

## Ajax：入门指南

我们可以使用这个按钮来调用我们之前在 `ajax.html` 中见过的 `getData()` 函数。你需要向 `getData()` 传递两个参数——要下载数据的 URL，以及要显示结果的 `<div>` 元素的 ID，因此我们可以将这行代码添加到按钮中：

```html
<form>
    <input type="button" value="Fetch message 1"
           onclick="getData('dataresponder.php', 'targetDiv')">
    .
    .
    .
</form>
```

不过，这还不完整——我们需要向 `dataresponder.php` 传递一个值为 1 的参数，我们可以通过 URL 编码来实现这一点，将 URL 更改为 `dataresponder.php?data=1`：

```html
<form>
    <input type="button" value="Fetch message 1"
           onclick="getData('dataresponder.php?data=1', 'targetDiv')">
    .
    .
    .
</form>
```

这就处理好了第一个按钮。第二个按钮类似，只是标签和它调用的 URL 不同，URL 是 `dataresponder.php?data=2`（这是 `ajax3.html`）：

```html
<html>
    <head>
        <title>Sending Data to the Server</title>

        <script language="javascript">
            var XMLHttpRequestObject = false;

            if (window.XMLHttpRequest) {
                XMLHttpRequestObject = new XMLHttpRequest();
            } else if (window.ActiveXObject) {
                XMLHttpRequestObject = new
                        ActiveXObject("Microsoft.XMLHTTP");
            }

            function getData(dataSource, divID)
            {
                if(XMLHttpRequestObject) {
                    var obj = document.getElementById(divID);
                    XMLHttpRequestObject.open("GET", dataSource);

                    XMLHttpRequestObject.onreadystatechange = function()
                    {
                        if (XMLHttpRequestObject.readyState == 4 &&
XMLHttpRequestObject.status == 200) {
    obj.innerHTML = XMLHttpRequestObject.responseText;
}
}
XMLHttpRequestObject.send(null);
}
</script>
</head>
<body>
<h1>Sending Data to the Server</h1>
<form>
  <input type="button" value="Fetch message 1"
         onclick="getData('dataresponder.php?data=1', 'targetDiv')">
  <input type="button" value="Fetch message 2"
         onclick="getData('dataresponder.php?data=2', 'targetDiv')">
</form>
<div id="targetDiv">
  <p>The fetched message will appear here.</p>
</div>
</body>
</html>
```

你可以在图 3-7 中看到 `ajax3.html` 的运行效果，用户点击了第一个按钮，服务器正确地做出了响应。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_106_0.png)

**图 3-7** `ajax3.html` 向服务器发送 1

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_107_0.png)

**图 3-8** `ajax3.html` 向服务器发送 2

如果用户点击第二个按钮，一个值为 2 的数据会被发送到服务器，相应的消息就会返回，如图 3-8 所示。酷。

## 使用 POST 向服务器发送数据

GET 方法只是向服务器发送数据的一种方式——还有其他方法，包括我们现在要探讨的 POST 方法。POST 方法提供了更多的安全性，因为你发送给服务器的数据不会被 URL 编码，从而不会暴露给所有人看。

### 编写 PHP

既然我们已经创建了 PHP 脚本 `dataresponder.php`，那么创建一个可以接收 POST 请求的 PHP 脚本就很容易了。你所要做的就是在 `dataresponder.php` 中将 `$_GET` 数组

```php
<?php
if ($_GET["data"] == "1") {
    echo 'You sent the server a value of 1';
}
if ($_GET["data"] == "2") {
    echo 'You sent the server a value of 2';
}
?>
```

更改为新 PHP 脚本 `dataresponderpost.php` 中的 `$_POST` 数组：

```php
<?php
if ($_POST["data"] == "1") {
    echo 'You sent the server a value of 1';
}
if ($_POST["data"] == "2") {
    echo 'You sent the server a value of 2';
}
?>
```

你可能已经猜到了，`$_POST` 数组允许你读取使用 POST 方法而不是 GET 方法发送到你的 PHP 脚本的数据。让我们看看启用 Ajax 的页面 `ajax4.html`，它与服务器上的 `dataresponderpost.php` 进行交互。从本章中我们已经创建的启用 Ajax 的网页开始，你该如何设置以通过 POST 向服务器发送数据呢？

### 与 `dataresponderpost.php` 交互

第一步似乎很清楚——你必须更改 `getData()` 函数中的这一行：

```javascript
function getData(dataSource, divID)
{
    if(XMLHttpRequestObject) {
        var obj = document.getElementById(divID);
        XMLHttpRequestObject.open("GET", dataSource);
        .
        .
        .
    }
}
```

改为这样，这里我们使用 POST 方法：

```javascript
function getData(dataSource, divID)
{
    if(XMLHttpRequestObject) {
        var obj = document.getElementById(divID);
        XMLHttpRequestObject.open("POST", dataSource);
        .
        .
        .
    }
}
```

接下来，为了通过 POST 发送数据，你还必须设置一个 HTTP 请求头 `Content-Type` 为 `"application/x-www-form-urlencoded"`。即使你不知道这是什么意思，也请确保包含这段代码：

```javascript
function getData(dataSource, divID)
{
    if(XMLHttpRequestObject) {
        var obj = document.getElementById(divID);
        XMLHttpRequestObject.open("POST", dataSource);
        XMLHttpRequestObject.setRequestHeader('Content-Type', 'application/x-www-form-urlencoded');
        .
        .
        .
    }
}
```

到目前为止一切顺利。现在我们可以处理要发送给 `dataresponderpost.php` 的数据了。当我们使用 GET 方法时，我们只是在调用 `getData()` 时像这样对数据进行 URL 编码：

```html
<body>
    <h1>Sending Data to the Server</h1>
    <form>
        <input type="button" value="Fetch message 1"
            onclick="getData('dataresponder.php?data=1', 'targetDiv')">
        <input type="button" value="Fetch message 2"
            onclick="getData('dataresponder.php?data=2', 'targetDiv')">
    </form>
    <div id="targetDiv">
        <p>The fetched message will appear here.</p>
    </div>
</body>
```

使用 POST 方法时，你不能直接像这样进行 URL 编码。但我们仍然需要向 `getData()` 函数传递一个 1 或 2，所以让我们在 `getData()` 调用中添加第三个参数——一个名为 `data` 的参数。在 `getData()` 函数中，`data` 参数将包含 1 或 2，具体取决于点击了哪个按钮：

```html
<script language="javascript">
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    function getData(dataSource, divID, data)
    {
        if(XMLHttpRequestObject) {
            var obj = document.getElementById(divID);
            XMLHttpRequestObject.open("POST", dataSource);
            XMLHttpRequestObject.setRequestHeader('Content-Type',
                'application/x-www-form-urlencoded');
            .
            .
            .
        }
    }
</script>
</head>
```

```html
<body>

<h1>Sending Data to the Server With POST</h1>

<form>
  <input type="button" value="Fetch message 1"
         onclick="getData('dataresponderpost.php', 'targetDiv', 1)">
  <input type="button" value="Fetch message 2"
         onclick="getData('dataresponderpost.php', 'targetDiv', 2)">
</form>

<div id="targetDiv">
  <p>The fetched message will appear here.</p>
</div>

</body>
```

现在我们必须在 `getData()` 函数中使用 POST 发送数据。我们首先添加标准的回调函数，以便正确处理从服务器下载的数据：

```javascript
function getData(dataSource, divID, data)
{
  if(XMLHttpRequestObject) {
    var obj = document.getElementById(divID);
    XMLHttpRequestObject.open("POST", dataSource);
    XMLHttpRequestObject.setRequestHeader('Content-Type',
        'application/x-www-form-urlencoded');

    XMLHttpRequestObject.onreadystatechange = function()
    {
      if (XMLHttpRequestObject.readyState == 4 &&
          XMLHttpRequestObject.status == 200) {
           obj.innerHTML = XMLHttpRequestObject.responseText;
      }
    }
    .
    .
    .
  }
}
```

我们已经准备好通过 POST 方法发送数据了。为此，你需要使用 `XMLHttpRequest` 对象的 `send()` 方法。在本章中使用 GET 方法的其他 Ajax 网页中，这行代码是我们使用 `send()` 方法连接到服务器的方式：

```javascript
function getData(dataSource, divID)
{
  if(XMLHttpRequestObject) {
    var obj = document.getElementById(divID);
    XMLHttpRequestObject.open("GET", dataSource);
```

## Ajax：初学者指南

```javascript
XMLHttpRequestObject.onreadystatechange = function()
{
    if (XMLHttpRequestObject.readyState == 4 &&
        XMLHttpRequestObject.status == 200) {
        obj.innerHTML = XMLHttpRequestObject.responseText;
    }
}
XMLHttpRequestObject.send(null);
}
```

然而现在，我们不再发送 `null` 值，而是将要通过 POST 发送的数据，以 URL 编码字符串的形式发送。在这种情况下，该字符串是 `"data=1"` 或 `"data=2"`，具体取决于 `getData()` 函数的 `data` 参数持有的值。因此，我们可以使用 `XMLHttpRequest` 对象的 `send()` 方法，以这种方式将数据发送到服务器：



```javascript
function getData(dataSource, divID, data)
{
    if(XMLHttpRequestObject) {
        var obj = document.getElementById(divID);
        XMLHttpRequestObject.open("POST", dataSource);
        XMLHttpRequestObject.setRequestHeader('Content-Type',
            'application/x-www-form-urlencoded');
        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                obj.innerHTML = XMLHttpRequestObject.responseText;
            }
        }
        XMLHttpRequestObject.send("data=" + data);
    }
}
```

以下是`ajax4.html`的完整内容供参考：

```html
<html>
  <head>
    <title>Sending Data to the Server With POST</title>
    <script language = "javascript">
      var XMLHttpRequestObject = false;
      if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
      }

      function getData(dataSource, divID, data)
      {
        if(XMLHttpRequestObject) {
          var obj = document.getElementById(divID);
          XMLHttpRequestObject.open("POST", dataSource);
          XMLHttpRequestObject.setRequestHeader('Content-Type',
            'application/x-www-form-urlencoded');

          XMLHttpRequestObject.onreadystatechange = function()
          {
            if (XMLHttpRequestObject.readyState == 4 &&
              XMLHttpRequestObject.status == 200) {
                obj.innerHTML = XMLHttpRequestObject.responseText;
            }
          }

          XMLHttpRequestObject.send("data=" + data);
        }
      }
    </script>
  </head>

  <body>

  <H1>Sending Data to the Server With POST</H1>

  <form>
    <input type = "button" value = "Fetch message 1"
      onclick = "getData('dataresponderpost.php', 'targetDiv', 1)">
    <input type = "button" value = "Fetch message 2"
      onclick = "getData('dataresponderpost.php', 'targetDiv', 2)">
  </form>

  <div id="targetDiv">
    <p>The fetched message will appear here.</p>
  </div>

  </body>
</html>
```

你可以在图 3-9 和图 3-10 中看到`ajax4.html`的实际运行效果，它能够通过 POST 与服务器进行通信。

## 94 Ajax：初学者指南

![img/2cd265cf0a64e9b4b91ab611753cd5d5_113_0.png](img/2cd265cf0a64e9b4b91ab611753cd5d5_113_0.png)

**图 3-9** `ajax4.html`向服务器发送 1

![img/2cd265cf0a64e9b4b91ab611753cd5d5_113_1.png](img/2cd265cf0a64e9b4b91ab611753cd5d5_113_1.png)

**图 3-10** `ajax4.html`向服务器发送 2

现在我们已经了解了如何处理 Ajax 中的异步下载，即 Ajax 中的“A”。到目前为止，我们只处理了从服务器发送的纯文本，但 Ajax 也可以处理 XML，即 Ajax 中的“X”。事实证明，在 JavaScript 中处理 XML 需要多做一些工作（这是第 6 章的主题），但现在我们可以先做一个入门介绍。

## 将 Ajax 与 XML 结合使用

假设你有一个非常重要的 XML 文档`colors.xml`（其中列出了红色、绿色和蓝色），你想要下载它。与任何 XML 文档一样，`colors.xml`以 XML 声明开头（第 6 章将详细介绍）：

```xml
<?xml version = "1.0" ?>
```

第 3 章：创建 Ajax 应用程序   95

所有 XML 文档都需要一个*文档元素*——即一个包含文档中所有其他元素的单一元素。在这种情况下，我们称文档元素为`<colors>`：

```xml
<?xml version = "1.0" ?>
<colors>
    .
    .
    .
</colors>
```

`<colors>`元素将包含三个`<color>`元素，每个元素包含一种颜色：红色、绿色和蓝色：

```xml
<?xml version = "1.0" ?>
<colors>
    <color>red</color>
    <color>green</color>
    <color>blue</color>
</colors>
```

这就是我们想在新示例`colors.html`中使用 Ajax 获取并解码的 XML 文档`colors.xml`，该示例如图 3-11 所示。当你点击`colors.html`中的“获取颜色”按钮时，`colors.xml`会被下载、解码，并显示颜色——红色、绿色和蓝色。

`colors.html`文档的开头与你在本章中看到的其他 Ajax 示例非常相似，有一个调用名为`getData`的 JavaScript 函数的按钮，以及一个用于显示结果的`<div>`元素：

```html
<body>
    <h1>Using Ajax with XML</h1>

    <form>
      <input type = "button" value = "Fetch the Colors"
             onclick = "getData('colors.xml', 'targetDiv')">
    </form>
    <div id="targetDiv" width =100 height=100>
    The list of colors will appear here.</div>
</body>
```

![img/2cd265cf0a64e9b4b91ab611753cd5d5_114_0.png](img/2cd265cf0a64e9b4b91ab611753cd5d5_114_0.png)

**图 3-11** `colors.html`

## 96 Ajax：初学者指南

在`<script>`元素中，我们首先创建将要使用的 XMLHttpRequest 对象：

```javascript
<script language = "javascript">

var colors;

var XMLHttpRequestObject = false;

if (window.XMLHttpRequest) {
    XMLHttpRequestObject = new XMLHttpRequest();
} else if (window.ActiveXObject) {
    XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
}
.
.
.
</script>
```

在 Firefox/Mozilla 系列浏览器中，你还需要指定要下载的是 XML，而不是纯文本。为此，你可以使用这行代码，它将下载的 MIME 类型设置为`text/xml`（每种主要数据格式都有对应的 MIME 类型）：

```javascript
<script language = "javascript">

var colors;

var XMLHttpRequestObject = false;

if (window.XMLHttpRequest) {
    XMLHttpRequestObject = new XMLHttpRequest();
    XMLHttpRequestObject.overrideMimeType("text/xml");
} else if (window.ActiveXObject) {
    XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
}
.
.
.
</script>
```

现在我们可以编写`getData`函数了。在这个函数中，我们检查 XMLHttpRequest 对象是否已创建，如果已创建，则打开它：

```javascript
function getData(dataSource, divID)
{
    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", dataSource);
        .
        .
        .
    }
}
```

接下来，我们可以添加匿名回调函数，并检查下载的状态和`readyState`属性：

```javascript
function getData(dataSource, divID)
{
    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", dataSource);
        var obj = document.getElementById(divID);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                .
                .
                .
            }
        }

    }
}
```

如果我们在执行这个`if`语句内的代码，说明下载成功了。那么，我们如何获取 XML 数据呢？我们是否使用 XMLHttpRequest 对象的`responseText`属性？不——我们使用的是 XMLHttpRequest 对象的`responseXML`属性，它包含一个 JavaScript XML 文档对象（这是第 6 章的主题）：

```javascript
function getData(dataSource, divID)
{
    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", dataSource);

        XMLHttpRequestObject.onreadystatechange = function()
        {
          if (XMLHttpRequestObject.readyState == 4 &&
            XMLHttpRequestObject.status == 200) {
            var xmlDocument = XMLHttpRequestObject.responseXML;
            .
            .
            .
          }
        }
    }
}
```

你将在第 6 章了解更多关于处理 XML 文档对象的内容，但我们可以用一点代码来剖析这里传递给我们的对象。首先，你可以使用文档的`getElementsByTagName`方法从 XML 文档中获取`<color>`元素数组。我们将这样创建一个名为`colors`的数组：

```javascript
function getData(dataSource, divID)
{
  if(XMLHttpRequestObject) {
    XMLHttpRequestObject.open("GET", dataSource);

    XMLHttpRequestObject.onreadystatechange = function()
    {
      if (XMLHttpRequestObject.readyState == 4 &&
        XMLHttpRequestObject.status == 200) {
        var xmlDocument = XMLHttpRequestObject.responseXML;
        colors = xmlDocument.getElementsByTagName("color");
        .
        .
        .
      }
    }
  }
}
```

现在我们可以准备列出获取的颜色，方法是在目标`<div>`元素中显示一条消息“以下是获取到的颜色：”；我们还将使用`<ul>` HTML 标签开始一个无序列表，这样颜色会以项目符号列表的形式出现：

```javascript
function getData(dataSource, divID)
{
  if(XMLHttpRequestObject) {
    XMLHttpRequestObject.open("GET", dataSource);
    var obj = document.getElementById(divID);

    XMLHttpRequestObject.onreadystatechange = function()
    {
```

以下是获取到的颜色列表：

* 红色
* 绿色
* 蓝色

在这个循环中，我们可以将当前的`<color>`元素引用为`colors[loopIndex]`。这是否意味着我们每次循环只需简单地显示`colors[loopIndex]`就能显示当前颜色呢？不，我们需要从`<color>`元素中专门提取颜色文本。`<color>`元素的结构如下所示：

```xml
<?xml version = "1.0" ?>
<colors>
  <color>red</color>
  <color>green</color>
  <color>blue</color>
</colors>
```

在 XML 中，每个`<color>`元素内的文本被视为*文本节点*。我们可以通过`colors[loopIndex].firstChild`来访问该文本节点，因为文本节点是每个`<color>`元素的第一个子节点。

很好，这是否意味着我们可以将每种颜色显示为`colors[loopIndex].firstChild`呢？不，因为在 JavaScript 中，文本节点是一个对象，而不仅仅是纯文本。要实际从文本节点中提取文本，必须使用文本节点的`data`属性，如下所示：`colors[loopIndex].firstChild.data`。因此，我们可以使用列表项 HTML 标签`<li>`将每种颜色添加到带项目符号的列表中，然后用`</ul>`结束该列表，如下所示：



```javascript
function getData(dataSource, divID)
{
    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", dataSource);
        var obj = document.getElementById(divID);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                var xmlDocument = XMLHttpRequestObject.responseXML;
                colors = xmlDocument.getElementsByTagName("color");
                obj.innerHTML = "Here are the fetched colors:<ul>";
                for (loopIndex = 0; loopIndex < colors.length; loopIndex++)
                {
                    obj.innerHTML += "<li>" +
                        colors[loopIndex].firstChild.data + "</li>";
                }
                obj.innerHTML += "</ul>";
            }
        }
    }
}
```

我们终于可以准备使用`XMLHttpRequest`对象的`send`方法连接服务器了。由于我们使用的是`GET`方法，只需向该方法传递`null`值即可：

```javascript
function getData(dataSource, divID)
{
    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", dataSource);
        var obj = document.getElementById(divID);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                var xmlDocument = XMLHttpRequestObject.responseXML;
                colors = xmlDocument.getElementsByTagName("color");
                obj.innerHTML = "Here are the fetched colors:<ul>";
                for (loopIndex = 0; loopIndex < colors.length; loopIndex++)
                {
                    obj.innerHTML += "<li>" +
                        colors[loopIndex].firstChild.data + "</li>";
                }
                obj.innerHTML += "</ul>";
            }
        }
    }
}

XMLHttpRequestObject.send(null);
}
}
```

至此，`colors.html`文件已全部完成，您可以参考下面的完整代码：

```html
<html>
<head>
    <title>Using Ajax with XML</title>

    <script language = "javascript">
        var colors;

        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
            XMLHttpRequestObject.overrideMimeType("text/xml");
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }

        function getData(dataSource, divID)
        {
            if(XMLHttpRequestObject) {
                XMLHttpRequestObject.open("GET", dataSource);
                var obj = document.getElementById(divID);

                XMLHttpRequestObject.onreadystatechange = function()
                {
                    if (XMLHttpRequestObject.readyState == 4 &&
                        XMLHttpRequestObject.status == 200) {
                        var xmlDocument = XMLHttpRequestObject.responseXML;
                        colors = xmlDocument.getElementsByTagName("color");
                        obj.innerHTML = "Here are the fetched colors:<ul>";
                        for (loopIndex = 0; loopIndex < colors.length; loopIndex++)
                        {
                            obj.innerHTML += "<li>" + 
                                colors[loopIndex].firstChild.data + "</li>";
                        }
                        obj.innerHTML += "</ul>";
                    }
                }
            }
        }

        XMLHttpRequestObject.send(null);
    </script>
</head>

<body>

    <h1>Using Ajax with XML</h1>

    <form>
        <input type = "button" value = "Fetch the Colors"
            onclick = "getData('colors.xml', 'targetDiv')">
    </form>

    <div id="targetDiv" width =100 height=100>
        The list of colors will appear here.</div>

</body>

</html>
```

您可以在图3-12中看到结果，它显示了点击按钮后如何获取`colors.xml`文档中的 XML 数据、对其进行解码，并将颜色以带项目符号的列表形式显示出来。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_121_0.png)

### 图3-12 使用 Ajax 下载 XML

# 第四章：全力冲刺 Ajax

## 关键技能与概念

- 处理多个`XMLHttpRequest`请求
- 使用两个`XMLHttpRequest`请求
- 使用`XMLHttpRequest`请求数组
- 使用内部函数和多个`XMLHttpRequest`请求
- 处理服务器发送的 JavaScript
- 克服浏览器缓存

本章将带您深入了解一些高级 Ajax 技术。第3章为我们开启了 Ajax 的大门，本章将在此基础上深入探讨这一主题。本章将要研究的主要议题之一是如何在同一个页面中处理多个`XMLHttpRequest`请求——也就是说，如果您有多个按钮使用 Ajax 连接服务器，如果一个请求尚未完成用户就点击了另一个按钮会发生什么？当 Ajax 返回时，是哪个请求在返回数据？我们将在这里探讨如何在同一个页面中处理多个`XMLHttpRequest`请求。

我们还将看到，除了下载纯文本和 XML，您还可以下载其他基于字符的数据，例如 JavaScript，这实际上是使用 Ajax 下载的常见数据类型。例如，自行通过代码连接一些 Google 应用程序，如 Google Suggest（见第1章），就涉及下载 JavaScript。

本章还将介绍更多 Ajax 内容——如何克服浏览器缓存、处理可通过 Ajax 下载的 HTTP 头信息等。我们将首先探讨在同一页面中拥有多个`XMLHttpRequest`对象可能导致混乱的情况。

## 在同一页面中处理多个`XMLHttpRequest`对象

您可能还记得第3章中的示例，我们在该示例中与服务器上的 PHP 脚本`dataresponder.php`进行了通信。当您点击按钮1时，一个值为1的数据被发送到服务器，服务器将该值返回，如图4-1所示。

当您点击按钮2时，一个值为2的数据被发送到服务器，服务器将该值返回。到目前为止一切正常。

但现在假设用户变得不耐烦，随意点击按钮。问题在于应用程序只使用了一个`XMLHttpRequest`对象，而现在这个对象正在被要求向服务器发送多个请求。根据服务器的响应速度，响应可能会被打乱——用户甚至可能点击按钮1，然后点击按钮2，但如果服务器响应顺序错误，用户看到的可能是点击按钮1的响应。

这种乱序的可能性是因为应用程序只使用一个`XMLHttpRequest`对象，即使用户可能发出多个请求。你可以在代码中看到这个问题，它只使用一个`XMLHttpRequest`对象（这是`single.html`，已从上一章重命名为`ajax3.html`）：

```html
<html>
  <head>
    <title>Sending Data to the Server</title>

    <script language="javascript">
      var XMLHttpRequestObject = false;

      if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
          ActiveXObject("Microsoft.XMLHTTP");
      }

      function getData(dataSource, divID) {
        if (XMLHttpRequestObject) {
          var obj = document.getElementById(divID);
          XMLHttpRequestObject.open("GET", dataSource);
          XMLHttpRequestObject.onreadystatechange = function() {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
              obj.innerHTML = XMLHttpRequestObject.responseText;
            }
          }
          XMLHttpRequestObject.send(null);
        }
      }
    </script>
  </head>
  <body>
    <h1>Sending Data to the Server</h1>

    <form>
      <input type="button" value="Fetch message 1"
        onclick="getData('dataresponder.php?data=1', 'targetDiv')">
      <input type="button" value="Fetch message 2"
        onclick="getData('dataresponder.php?data=2', 'targetDiv')">
    </form>

    <div id="targetDiv">
      <p>The fetched message will appear here.</p>
    </div>
  </body>
</html>
```

这是服务器端代码`dataresponder.php`：

```php
<?php
if ($_GET["data"] == "1") {
    echo 'The server got a value of 1';
}
if ($_GET["data"] == "2") {
    echo 'The server got a value of 2';
}
?>
```

那么，问题就变成了：如何同时处理多个`XMLHttpRequest`请求？我们的第一个解决方案是显而易见的——使用两个`XMLHttpRequest`对象。

### 使用两个`XMLHttpRequest`对象

`single.html`中有两个按钮，但只有一个`XMLHttpRequest`对象，这可能导致响应混淆。如果我们创建两个`XMLHttpRequest`对象，每个按钮对应一个，会怎么样呢？

这正是我们将在新示例`double.html`中做的。首先，我们创建一个`XMLHttpRequest`对象`XMLHttpRequest1`：

```html
<html>
  <head>
    <title>Using Two XMLHttpRequest Objects</title>

    <script language="javascript">
      var XMLHttpRequestObject1 = false;

      if (window.XMLHttpRequest) {
        XMLHttpRequestObject1 = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
        XMLHttpRequestObject1 = new
          ActiveXObject("Microsoft.XMLHTTP");
      }
    </script>
  </head>
</html>
```

接下来，我们创建一个使用此`XMLHttpRequest`对象的`getData`函数的新版本`getData1`：



然后，我们创建第二个新的`XMLHttpRequest`对象`XMLHttpRequest2`：

```html
<html>
  <head>
    <title>Using Two XMLHttpRequest Objects</title>

    <script language="javascript">
      var XMLHttpRequestObject1 = false;

      if (window.XMLHttpRequest) {
        XMLHttpRequestObject1 = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
        XMLHttpRequestObject1 = new
          ActiveXObject("Microsoft.XMLHTTP");
      }

      var XMLHttpRequestObject2 = false;

      if (window.XMLHttpRequest) {
        XMLHttpRequestObject2 = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
        XMLHttpRequestObject2 = new
          ActiveXObject("Microsoft.XMLHTTP");
      }

      function getData1(dataSource, divID) {
        if (XMLHttpRequestObject1) {
          var obj = document.getElementById(divID);
          XMLHttpRequestObject1.open("GET", dataSource);

          XMLHttpRequestObject1.onreadystatechange = function() {
            if (XMLHttpRequestObject1.readyState == 4 &&
                XMLHttpRequestObject1.status == 200) {
              obj.innerHTML = XMLHttpRequestObject1.responseText;
            }
          }
          XMLHttpRequestObject1.send(null);
        }
      }
    </script>
  </head>
</html>
```

接着，我们添加另一个版本的`getData`函数`getData2`，它使用`XMLHttpRequest2`：

```html
<html>
  <head>
    <title>Using Two XMLHttpRequest Objects</title>

    <script language="javascript">
      var XMLHttpRequestObject1 = false;

      if (window.XMLHttpRequest) {
        XMLHttpRequestObject1 = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
        XMLHttpRequestObject1 = new
          ActiveXObject("Microsoft.XMLHTTP");
      }

      var XMLHttpRequestObject2 = false;

      if (window.XMLHttpRequest) {
        XMLHttpRequestObject2 = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
        XMLHttpRequestObject2 = new
          ActiveXObject("Microsoft.XMLHTTP");
      }

      function getData1(dataSource, divID) {
        if (XMLHttpRequestObject1) {
          var obj = document.getElementById(divID);
          XMLHttpRequestObject1.open("GET", dataSource);

          XMLHttpRequestObject1.onreadystatechange = function() {
            if (XMLHttpRequestObject1.readyState == 4 &&
                XMLHttpRequestObject1.status == 200) {
              obj.innerHTML = XMLHttpRequestObject1.responseText;
            }
          }
          XMLHttpRequestObject1.send(null);
        }
      }

      function getData2(dataSource, divID) {
        if (XMLHttpRequestObject2) {
          var obj = document.getElementById(divID);
          XMLHttpRequestObject2.open("GET", dataSource);

          XMLHttpRequestObject2.onreadystatechange = function() {
            if (XMLHttpRequestObject2.readyState == 4 &&
                XMLHttpRequestObject2.status == 200) {
              obj.innerHTML = XMLHttpRequestObject2.responseText;
            }
          }
          XMLHttpRequestObject2.send(null);
        }
      }
    </script>
  </head>
  <body>
    <h1>Using Two XMLHttpRequest Objects</h1>

    <form>
      <input type="button" value="Fetch message 1"
        onclick="getData1('dataresponder.php?data=1', 'targetDiv')">
      <input type="button" value="Fetch message 2"
        onclick="getData2('dataresponder.php?data=2', 'targetDiv')">
    </form>

    <div id="targetDiv">
      <p>The fetched message will appear here.</p>
    </div>
  </body>
</html>
```

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_130_0.png)

图4-2 `double.html`

大功告成。你可以测试`double.html`。点击任一按钮都会下载正确的消息，如图4-2所示。

## 动手试试：让`double.html`工作起来

现在创建`double.html`，或者从本书的可下载代码中获取它，并使其运行起来。这个应用程序是我们第一次尝试使用多个`XMLHttpRequest`对象，所以请确保你理解它的工作原理和功能。

好的，使用两个`XMLHttpRequest`对象解决了问题。但如果应用程序中有三个按钮呢？你需要编写三个`XMLHttpRequest`对象的代码吗？如果有一百个按钮呢？如果用户点击了这两个按钮十几次呢？显然，我们需要一个更好的解决方案。

## 使用`XMLHttpRequest`对象数组

一个更好的解决方案是使用一个`XMLHttpRequest`对象数组。我们可以为每个新请求创建一个新的`XMLHttpRequest`，并使用数组轻松地将它们分开管理。

以下是在新示例`array.html`中实现这一点的方法。我们可以先使用JavaScript的`Array`函数为`XMLHttpRequest`对象创建一个名为`XMLHttpRequestObjects`的新数组：

```html
<html>
<head>
<title>Using an Array of XMLHttpRequest Objects</title>
```

## 112 Ajax：入门指南

```javascript
<script language="javascript">
    var XMLHttpRequestObjects = new Array();
    .
    .
    .
</script>
```

在 JavaScript 中，向数组末尾添加项目的便捷方法是使用`push`函数。我们可以用`push`函数将新的`XMLHttpRequest`对象存储到`XMLHttpRequestObjects`数组中，就像在`getData1`（连接到按钮 1 的函数）中这样：

```html
<html>
    <head>
        <title>使用 XMLHttpRequest 对象数组</title>

        <script language="javascript">

            var XMLHttpRequestObjects = new Array();

            function getData1(dataSource, divID)
            {
                if (window.XMLHttpRequest) {
                    XMLHttpRequestObjects.push(new XMLHttpRequest());
                } else if (window.ActiveXObject) {
                    XMLHttpRequestObjects.push(new ActiveXObject("Microsoft.XMLHTTP"));
                }
            }
        </script>
    </head>
    <body>
        <!-- 内容 -->
    </body>
</html>
```

最新`XMLHttpRequest`对象在数组中的索引是`XMLHttpRequestObjects.length -1`，我们将该值赋给一个名为`index`的变量，以便跟踪最新的`XMLHttpRequest`对象：

```html
<html>
    <head>
        <title>使用 XMLHttpRequest 对象数组</title>

        <script language="javascript">
            var index = 0;

            var XMLHttpRequestObjects = new Array();

            function getData1(dataSource, divID)
            {
                if (window.XMLHttpRequest) {
                    XMLHttpRequestObjects.push(new XMLHttpRequest());
                } else if (window.ActiveXObject) {
                    XMLHttpRequestObjects.push(new ActiveXObject("Microsoft.XMLHTTP"));
                }
            }
        </script>
    </head>
    <body>
        <!-- 内容 -->
    </body>
</html>
```

```javascript
index = XMLHttpRequestObjects.length - 1;
.
.
.
```

现在，我们可以在`getData1`的剩余部分中这样引用最新的`XMLHttpRequest`对象：`XMLHttpRequestObjects[index]`：

```html
<html>
  <head>
    <title>使用 XMLHttpRequest 对象数组</title>

    <script language="javascript">
      var index = 0;

      var XMLHttpRequestObjects = new Array();

      function getData1(dataSource, divID)
      {
        if (window.XMLHttpRequest) {
          XMLHttpRequestObjects.push(new XMLHttpRequest());
        } else if (window.ActiveXObject) {
          XMLHttpRequestObjects.push(new ActiveXObject("Microsoft.XMLHTTP"));
        }

        index = XMLHttpRequestObjects.length - 1;

        if(XMLHttpRequestObjects[index]) {
          XMLHttpRequestObjects[index].open("GET", dataSource);
          var obj = document.getElementById(divID);

          XMLHttpRequestObjects[index].onreadystatechange = function()
          {
            if (XMLHttpRequestObjects[index].readyState == 4 &&
                XMLHttpRequestObjects[index].status == 200) {
              obj.innerHTML = XMLHttpRequestObjects[index].responseText;
            }
          }

          XMLHttpRequestObjects[index].send(null);
        }
      }
```

而`getData2`（绑定到按钮 2 的函数）的工作方式类似：



```javascript
function getData2(dataSource, divID)
{
  if (window.XMLHttpRequest) {
    XMLHttpRequestObjects.push(new XMLHttpRequest());
  } else if (window.ActiveXObject) {
    XMLHttpRequestObjects.push(new ActiveXObject("Microsoft.XMLHTTP"));
  }

  index = XMLHttpRequestObjects.length - 1;

  if (XMLHttpRequestObjects[index]) {
    XMLHttpRequestObjects[index].open("GET", dataSource);
    var obj = document.getElementById(divID);

    XMLHttpRequestObjects[index].onreadystatechange = function()
    {
        if (XMLHttpRequestObjects[index].readyState == 4 &&
            XMLHttpRequestObjects[index].status == 200) {
            obj.innerHTML = XMLHttpRequestObjects[index].responseText;
        }
    }

    XMLHttpRequestObjects[index].send(null);
  }
}
```

最后，我们将`getData1`和`getData2`绑定到两个按钮上：

```html
<html>
<head>
<title>使用 XMLHttpRequest 对象数组</title>

<script language="javascript">
var index = 0;

var XMLHttpRequestObjects = new Array();

function getData1(dataSource, divID)
{
    if (window.XMLHttpRequest) {
        XMLHttpRequestObjects.push(new XMLHttpRequest());
    } else if (window.ActiveXObject) {
        XMLHttpRequestObjects.push(new ActiveXObject("Microsoft.XMLHTTP"));
    }

    index = XMLHttpRequestObjects.length - 1;

    if (XMLHttpRequestObjects[index]) {
        XMLHttpRequestObjects[index].open("GET", dataSource);
        var obj = document.getElementById(divID);

        XMLHttpRequestObjects[index].onreadystatechange = function()
        {
            if (XMLHttpRequestObjects[index].readyState == 4 &&
                XMLHttpRequestObjects[index].status == 200) {
                obj.innerHTML = XMLHttpRequestObjects[index].responseText;
            }
        }

        XMLHttpRequestObjects[index].send(null);
    }
}

function getData2(dataSource, divID)
{
  if (window.XMLHttpRequest) {
    XMLHttpRequestObjects.push(new XMLHttpRequest());
  } else if (window.ActiveXObject) {
    XMLHttpRequestObjects.push(new ActiveXObject("Microsoft.XMLHTTP"));
  }

  index = XMLHttpRequestObjects.length - 1;

  if(XMLHttpRequestObjects[index]) {
    XMLHttpRequestObjects[index].open("GET", dataSource);
    var obj = document.getElementById(divID);

    XMLHttpRequestObjects[index].onreadystatechange = function()
    {
      if (XMLHttpRequestObjects[index].readyState == 4 &&
          XMLHttpRequestObjects[index].status == 200) {
            obj.innerHTML = XMLHttpRequestObjects[index].responseText;
      }
    }

    XMLHttpRequestObjects[index].send(null);
  }
}
</script>
</head>

<body>

<h1>使用 XMLHttpRequest 对象数组</h1>

<form>
  <input type="button" value="获取消息 1"
         onclick="getData1('dataresponder.php?data=1', 'targetDiv')">
  <input type="button" value="获取消息 2"
         onclick="getData2('dataresponder.php?data=2', 'targetDiv')">
</form>

<div id="targetDiv">
  <p>获取的消息将显示在此处。</p>
</div>

</body>
</html>
```

您可以看到这个新应用程序`array.html`在图 4-3 中的运行效果。很酷。点击任一按钮都会下载正确的消息，如图 4-3 所示。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_135_0.png)

图 4-3  `array.html`

## 动手试试：让`array.html`运行起来

现在创建`array.html`，或者从本书的可下载代码中获取它，并使其运行起来。这个应用程序是处理多个`XMLHttpRequest`请求的更好选择，因此请确保您理解它的工作原理。

那么`array.html`的工作方式是为每个 Ajax 请求创建一个新的`XMLHttpRequest`对象。但这是否有点浪费？毕竟，所有那些旧的`XMLHttpRequest`对象即使在其请求完成后，仍然留在数组中。这会占用内存。更糟糕的是，如果用户点击按钮数百次或数千次，例如在支持 Ajax 的游戏中，它可能会使您的应用程序停止运行。

难道没有简单的方法来删除不再需要的`XMLHttpRequest`对象吗？

## 使用内部函数

事实证明，在 Ajax 中处理多个`XMLHttpRequest`请求的常用方法是使用*内部函数*，而不是`XMLHttpRequest`对象的数组。

什么是内部函数？这些是包含在另一个函数内部的函数，像这样：

```javascript
function outer(value)
{
    var item1 = value;

    function inner(item2)
    {
        return (item1 + item2)
    }
}
```

如您所见，内部函数包含在外部函数内部。这有什么特别之处？如果用一个用于设置变量`item1`的值来调用外部函数，那么当调用内部函数时，`item1`会保留其值。因此，例如，如果调用`outer`并传递值 1，然后调用`inner`并传递值 2，`inner`将返回 1 + 2。然后如果用值 4 调用`inner`，它将返回 1 + 4。

假设然后用新值 2 调用`outer`，再用值 3 调用`inner`。在这种情况下，`item1`是 2，`item2`是 3，所以`inner`返回 3 + 2 = 5。

这给你带来了什么？关键在于：每次调用`outer`时，都会创建一个外部函数的新副本，其中包含内部函数的新副本。将思考方式从`item1`转换为`XMLHttpRequest`对象，您就能明白要点了：您可以这样设计，即每次调用`getData`函数时，都会创建一个新的`XMLHttpRequest`对象，而使用它的匿名函数——即内部函数——将始终拥有一个全新的`XMLHttpRequest`对象可供使用。

以下是我们代码目前的大致样子——请注意`XMLHttpRequest`对象的创建是在`getData`函数外部：

```javascript
var XMLHttpRequestObject = false;

if (window.XMLHttpRequest) {
  XMLHttpRequestObject = new XMLHttpRequest();
} else if (window.ActiveXObject) {
  XMLHttpRequestObject = new
    ActiveXObject("Microsoft.XMLHTTP");
}

function getData(dataSource, divID)
{
  if (XMLHttpRequestObject) {
    var obj = document.getElementById(divID);
    XMLHttpRequestObject.open("GET", dataSource);

    XMLHttpRequestObject.onreadystatechange = function()
    {
      if (XMLHttpRequestObject.readyState == 4 &&
        XMLHttpRequestObject.status == 200) {
          obj.innerHTML = XMLHttpRequestObject.responseText;
      }
    }

    XMLHttpRequestObject.send(null);
  }
}
```

为了确保每个 Ajax 请求都有一个全新的`XMLHttpRequest`对象，您只需将`XMLHttpRequest`对象的创建代码移动到`getData`函数内部。这使得`getData`将`XMLHttpRequest`对象创建代码移入封装了内部匿名函数的外部函数中。每次调用`getData`时，都会创建该函数的一个新副本，这进而又会创建一个新的`XMLHttpRequest`对象，该对象将在 Ajax 请求从服务器返回时供内部函数使用。

代码示例如下：

```javascript
function getData(dataSource, divID)
{
  var XMLHttpRequestObject = false;

  if (window.XMLHttpRequest) {
    XMLHttpRequestObject = new XMLHttpRequest();
  } else if (window.ActiveXObject) {
    XMLHttpRequestObject = new
      ActiveXObject("Microsoft.XMLHTTP");
  }

  if(XMLHttpRequestObject) {
    var obj = document.getElementById(divID);
    XMLHttpRequestObject.open("GET", dataSource);

    XMLHttpRequestObject.onreadystatechange = function()
    {
      if (XMLHttpRequestObject.readyState == 4 &&
        XMLHttpRequestObject.status == 200) {
          obj.innerHTML = XMLHttpRequestObject.responseText;
      }
    }

    XMLHttpRequestObject.send(null);
  }
}
```

因此，无需像下面这样创建多个`XMLHttpRequest`对象和两个函数`getData1`与`getData2`：

```javascript
var XMLHttpRequestObject1 = false;

if (window.XMLHttpRequest) {
  XMLHttpRequestObject1 = new XMLHttpRequest();
} else if (window.ActiveXObject) {
  XMLHttpRequestObject1 = new
    ActiveXObject("Microsoft.XMLHTTP");
}

var XMLHttpRequestObject2 = false;

if (window.XMLHttpRequest) {
  XMLHttpRequestObject2 = new XMLHttpRequest();
} else if (window.ActiveXObject) {
  XMLHttpRequestObject2 = new
  ActiveXObject("Microsoft.XMLHTTP");
}
```

```javascript
function getData1(dataSource, divID)
{
  if(XMLHttpRequestObject1) {
    var obj = document.getElementById(divID);
    XMLHttpRequestObject1.open("GET", dataSource);

    XMLHttpRequestObject1.onreadystatechange = function()
    {
      if (XMLHttpRequestObject1.readyState == 4 &&
          XMLHttpRequestObject1.status == 200) {
            obj.innerHTML = XMLHttpRequestObject1.responseText;
      }
    }

    XMLHttpRequestObject1.send(null);
  }
}
```

```javascript
function getData2(dataSource, divID)
{
  if(XMLHttpRequestObject2) {
    var obj = document.getElementById(divID);
    XMLHttpRequestObject2.open("GET", dataSource);

    XMLHttpRequestObject2.onreadystatechange = function()
    {
      if (XMLHttpRequestObject2.readyState == 4 &&
          XMLHttpRequestObject2.status == 200) {
            obj.innerHTML = XMLHttpRequestObject2.responseText;
      }
    }

    XMLHttpRequestObject2.send(null);
  }
}
```

……

## 第4章：全力冲刺 Ajax

你只需要一个`getData`函数，并且可以简单地将`XMLHttpRequest`对象创建代码移入该函数中，就像在`inner.html`中这样：



```html
<html>
  <head>
    <title>使用内部函数和多个 XMLHttpRequest 对象</title>

    <script language="javascript">
      function getData(dataSource, divID)
      {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
          XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
          XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
        }

        if (XMLHttpRequestObject) {
          var obj = document.getElementById(divID);
          XMLHttpRequestObject.open("GET", dataSource);

          XMLHttpRequestObject.onreadystatechange = function()
          {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                  obj.innerHTML = XMLHttpRequestObject.responseText;
            }
          }

          XMLHttpRequestObject.send(null);
        }
      }
    </script>
  </head>

  <body>
    <h1>使用内部函数和多个 XMLHttpRequest 对象</h1>

    <form>
      <input type="button" value="获取消息 1"
        onclick="getData('dataresponder.php?data=1', 'targetDiv')">
      <input type="button" value="获取消息 2"
        onclick="getData('dataresponder.php?data=2', 'targetDiv')">
    </form>

    <div id="targetDiv">
      <p>获取的消息将显示在这里。</p>
    </div>
  </body>
</html>
```

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_140_0.png)

你可以在图 4-4 中看到 `inner.html` 的实际效果。尽管点击按钮，Ajax 请求之间不会发生任何冲突。

`inner.html` 示例展示了如何避免 Ajax 请求之间潜在的冲突——只需将 XMLHttpRequest 创建代码放在 `getData` 函数（或你在自己代码中对该函数的任何称呼）内部。

就是这样。现在你可以轻松处理多个 XMLHttpRequest 请求了。

## 动手试试：让内部函数工作起来

通过检查下面这段代码，确认内部函数确实如所述那样工作：

```javascript
function outer(value)
{
    var item1 = value;

    function inner(item2)
    {
        return (item1 + item2)
    }
}
```

将其放入一个页面，并调用 `outer(1)`，然后调用 `inner(2)`。你得到的结果是 3 吗？然后再试试调用 `outer(2)` 和 `inner(2)`。你得到的是 4 吗？

## 下载 JavaScript

有时，Ajax 用于下载不仅是纯文本或 XML，还包括其他基于字符的数据。一个流行的选择是——信不信由你——JavaScript。这个选择是有道理的，例如，如果你的网站有十几个 JavaScript 函数和代码来确定现在应该调用哪个函数；比如，一个餐厅网站可能会根据一天中的时间显示不同的菜单。或者，你可以读取调用特定数据函数的 JavaScript。

事实上，这正是我们稍后在本章中连接到 Google Suggest 以下载其为用户输入的搜索词找到的匹配项的方式。你从 Google 实际下载的是 JavaScript 文本，而该 JavaScript 是一个函数调用。例如，如果你输入字母 "a"，你将能够从 Google Suggest 下载这段 JavaScript：

```javascript
window.google.ac.Suggest_apply(frameElement, "a", new Array(2,
"amazon", "855,000,000 results", "argos", "12,500,000 results",
"aol", "278,000,000 results", "autotrader", "5,820,000 results",
"apple", "436,000,000 results", "amazon.com", "461,000,000 results",
"aol.com", "87,200,000 results", "american airlines",
"14,600,000 results", "australian open", "12,300,000 results",
"ask.com", "39,600,000 results"), new Array(""));
```

这是一段调用名为 `window.google.ac.Suggest_apply` 函数的 JavaScript（这个名字很奇怪，因为它是一个完全非法的 JavaScript 函数名——浏览器的 `window` 对象没有名为 `google.ac.Suggest_apply` 的内置方法），你可以在这个函数调用中看到 Google Suggest 为字符 "a" 找到的匹配项，我们将在本章稍后对其进行解码。

我们将从查看一个下载 JavaScript 的示例 `javascript.html` 开始。这个 Ajax 应用程序将从 PHP 脚本 `javascript.php` 读取文本，而该文本只是一个名为 `show` 的函数调用（请记住，你将在第 9 章全面了解 PHP）：

```php
<?php
    echo 'show()';
?>
```

当我们从 `javascript.php` 下载文本时，我们可以将该文本作为 JavaScript 执行，这将导致浏览器查找我们编写的名为 `show` 的 JavaScript 函数并调用该函数。

以下是 `javascript.html` 的开始部分——注意我们在 HTML 中创建了一个按钮，并将其连接到一个名为 `getData` 的 JavaScript 函数：

```html
<html>
    <head>
        <title>使用 Ajax 下载 JavaScript</title>
        <script language="javascript">
            var XMLHttpRequestObject = false;

            if (window.XMLHttpRequest) {
              XMLHttpRequestObject = new XMLHttpRequest();
            } else if (window.ActiveXObject) {
              XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
            }

            function getData(dataSource)
            {
              if (XMLHttpRequestObject) {

                XMLHttpRequestObject.open("GET", dataSource);

                XMLHttpRequestObject.onreadystatechange = function()
                {
                  if (XMLHttpRequestObject.readyState == 4 &&
                    XMLHttpRequestObject.status == 200) {

                      .
                      .
                      .
                  }
                }

                XMLHttpRequestObject.send(null);
              }
            }
        </script>
    </head>

    <body>
      <H1>使用 Ajax 下载 JavaScript</H1>

      <form>
        <input type="button" value="获取 JavaScript"
          onclick="getData('javascript.php')">
      </form>

      <div id="targetDiv">
        <p>数据将放在这里。</p>
      </div>
    </body>
</html>
```

当你从 `javascript.php` 下载文本（内容为 “show()”）时，你可以使用 JavaScript 的 `eval` 函数执行该文本。这就是 `eval` 函数的作用——你向它传递文本，它将该文本作为 JavaScript 执行。

# 124 Ajax：初学者指南

下载的文本将位于 `XMLHttpRequestObject.responseText` 中，你可以在 `getData` 中以如下方式将该文本作为 JavaScript 执行：

```javascript
function getData(dataSource)
{
    if (XMLHttpRequestObject) {

        XMLHttpRequestObject.open("GET", dataSource);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {

                eval(XMLHttpRequestObject.responseText);
            }
        }

        XMLHttpRequestObject.send(null);
    }
}
```

当然，这意味着我们需要一个名为 `show` 的 JavaScript 函数。在该函数中，我们可能只是在网页上显示文本 "Yep, it worked!"。以下是 `javascript.html` 最终版本中的完整代码：

```html
<html>
  <head>
    <title>Downloading JavaScript with Ajax</title>

    <script language="javascript">
      var XMLHttpRequestObject = false;

      if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
      }

      function getData(dataSource)
      {
        if (XMLHttpRequestObject) {

          XMLHttpRequestObject.open("GET", dataSource);

          XMLHttpRequestObject.onreadystatechange = function()
          {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {

                eval(XMLHttpRequestObject.responseText);
            }
          }

          XMLHttpRequestObject.send(null);
        }
      }

      function show()
      {
        var targetDiv = document.getElementById("targetDiv");

        targetDiv.innerHTML = "Yep, it worked!";
      }
    </script>
  </head>

  <body>
    <H1>Downloading JavaScript with Ajax</H1>

    <form>
        <input type="button" value="Get the JavaScript"
               onclick="getData('javascript.php')">
    </form>

    <div id="targetDiv">
        <p>The data will go here.</p>
    </div>
  </body>
</html>
```

因此，当用户点击按钮时，应用程序会读取 `javascript.php` 返回的文本，并将该文本作为 JavaScript 执行，调用 `show` 函数，该函数会显示你在图 4-5 中看到的消息。

这个例子演示了你可以几乎像下载文本一样轻松地下载和执行 JavaScript。这为你接下来学习使用 Google Suggest 做了准备。

## 尝试下载 JavaScript

尝试创建一个新的支持 Ajax 的网页，其中包含一个名为 `adder` 的 JavaScript 函数，该函数将两个值相加并返回它们的和：

```javascript
function adder(value1, value2)
{
    return (value1 + value2)
}
```

然后从服务器下载文本 `adder(2, 3)`，执行它，并确认你得到的答案是 5。

现在我们已经了解了如何使用 Ajax 下载和执行 JavaScript，我们可以进入本章的主要示例——连接到 Google Suggest。

## 连接到 Google Suggest

看看图 4-6 中的 Google Suggest。当你开始输入搜索词时，Google Suggest 会在一个下拉列表中建议与你输入内容匹配的项。然后你可以从该列表中选择一个术语，这样你就无需输入整个搜索词了。

你可以自己使用 Ajax 连接到 Google Suggest，我们现在就来看看如何做到这一点。除此之外，这个例子将让你学习如何使用 Ajax 响应用户的单个按键输入。

现在让我们开始创建我们自己版本的 Google Suggest 页面。

## 创建搜索词输入框

我们将使用 Ajax 自己连接到 Google Suggest。首先，我们需要一个文本框让用户输入搜索词，这在页面的正文中可能看起来像这样：

```html
<body>
    <H1>Handling Google Suggest</H1>

    Search for <input id="textField" type="text">
    .
    .
    .
</body>
```

你可以在图 4-7 中看到这个网页目前的样子。

我们需要在每次用户按键时检查他们输入的内容，并显示与他们输入内容匹配的结果。我们可以通过使用文本框的 `onkeyup` 事件来响应按键，该事件在用户释放按键时触发。我们可以通过调用一个名为 `askGoogleSuggest` 的函数来处理该事件：

```html
<body>
    <H1>Handling Google Suggest</H1>

    Search for <input id="textField" type="text" name="textField" onkeyup="askGoogleSuggest()">
    ...
</body>
```

**图 4-7** 我们版本的 Google Suggest

这完成了网页的正文部分。接下来让我们转向 JavaScript，真正的操作就在这里。

## 编写 JavaScript

现在让我们创建 `askGoogleSuggest` 函数：

```javascript
<script language="javascript">
    function askGoogleSuggest()
    {
        .
        .
        .
    }
</script>
```

当用户按下按键时，会调用此函数，我们可以使用文本框的 `value` 属性读取该按键。首先，我们获取一个对应于文本框的对象（文本框的 ID 是 `textField`）：



```html
<script language="javascript">
    function askGoogleSuggest()
    {
        var input = document.getElementById("textField");
        .
        .
        .
    }
</script>
```

如果文本框中有部分搜索词，我们可以将其发送到 Google Suggest 以获取其建议；以下是检查是否已有部分搜索词输入的方法：

```html
<script language="javascript">
    function askGoogleSuggest()
    {
        var input = document.getElementById("textField");

        if (input.value) {
            .
            .
            .
        }
    }
</script>
```

如果有搜索词在等待，我们可以将其发送到 Google Suggest。我们将通过一个名为`google.php`的 PHP 脚本使用 GET 方法来完成此操作，这意味着我们需要对我们的数据进行 URL 编码。我们将使用参数名`qu`（query 的缩写）将部分搜索词发送到`google.php`（该脚本会将该词转发给 Google Suggest）。以下是我们如何通过调用一个名为`getData`的函数将部分搜索词发送到`google.php`：

```html
<script language="javascript">
    function askGoogleSuggest()
    {
        var input = document.getElementById("textField");

        if (input.value) {
            getData("google.php?qu=" + input.value);
        }
    }
</script>
```

为什么我们通过 PHP 脚本与 Google Suggest 通信？为什么我们不能直接从这个网页联系 Google Suggest？这些都是重要的问题。答案是这是一个安全问题。如果 Web 浏览器检测到你的 Ajax 脚本试图联系的服务器不是你网页所在的同一台服务器，它就会产生怀疑。这里的情况就是这样——Google Suggest 所在的服务器与我们的服务器不同。

在这种情况下，浏览器会弹出一个（烦人的）对话框，询问用户是否应该继续。这种事情破坏了 Ajax 的实用性，因为 Ajax 应该在幕后无缝运行。为了解决这个问题，你可以在自己的服务器上使用服务器端编程来连接到外部服务器。这就是我们在这里所做的——我们通过`google.php`连接到 Google Suggest 以避免安全问题（我们稍后会编写`google.php`）。

好的，我们几乎完成了`askGoogleSuggest`函数。最后一步是，如果用户清除了搜索文本框中的文本，则清除下拉列表框，我们这样做：

```html
<script language="javascript">
    function askGoogleSuggest()
    {
        var input = document.getElementById("textField");

        if (input.value) {
            getData("google.php?qu=" + input.value);
        }
        else {
            var targetDiv = document.getElementById("targetDiv");

            targetDiv.innerHTML = "<div></div>";
        }
    }
</script>
```

这个示例中的`getData`函数只接受一个名为`dataSource`的 URL 参数：

```html
<script language="javascript">
    function getData(dataSource)
    {
        .
        .
        .
    }
</script>
```

`dataSource`参数将包含`google.php`的 URL 以及用户输入的经 URL 编码的搜索词。我们将在`getData`函数中使用 Ajax 连接到`google.php`，我们将从创建一个`XMLHttpRequest`对象开始：

# 第四章：全力以赴的 Ajax

```javascript
<script language="javascript">
function getData(dataSource)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }
    .
    .
    .
}
</script>
```

现在我们可以用通常的方式——使用匿名函数——来连接到`google.php`：

```javascript
<script language="javascript">
function getData(dataSource)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", dataSource);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                .
                .
                .
            }
        }

    }
}
</script>
```

我们从 Google Suggest 会得到什么样的返回文本呢？例如，如果你的搜索词是“a”，这就是你通过 Ajax 从 Google Suggest 返回的文本：

```javascript
window.google.ac.Suggest_apply(frameElement, "a", new Array(2,
"amazon", "855,000,000 results", "argos", "12,500,000 results",
"aol", "278,000,000 results", "autotrader", "5,820,000 results",
"apple", "436,000,000 results", "amazon.com", "461,000,000 results", "aol.com", "87,200,000 results", "american airlines", "14,600,000 results", "australian open", "12,300,000 results", "ask.com", "39,600,000 results"), new Array(""));
```

这是 JavaScript：Google Suggest 返回的是一个 JavaScript 函数调用（当然是以文本形式），这样构建是为了让你能在你的 Ajax 应用程序中调用同名函数。但这引入了一个问题：如果你试图创建一个名为`window.google.ac.Suggest_apply`的函数，Firefox 和 Internet Explorer 都会报错，并告诉你它们的内置`window`对象不包含 "google" 属性或方法。如何解决这个问题呢？你可以将 Google Suggest 返回的 JavaScript 中的函数重命名为一个合法的名称，比如 "callback"：

```javascript
callback(frameElement, "a", new Array(2, "amazon", "855,000,000 results", "argos", "12,500,000 results", "aol", "278,000,000 results", "autotrader", "5,820,000 results", "apple", "436,000,000 results", "amazon.com", "461,000,000 results", "aol.com", "87,200,000 results", "american airlines", "14,600,000 results", "australian open", "12,300,000 results", "ask.com", "39,600,000 results"), new Array(""));
```

如何将从 Google Suggest 获取的文本中的 "window.google.ac.Suggest_apply" 重命名为 "callback" 呢？你可以使用方便的 JavaScript`replace`函数，它正是为此设计的——替换字符串中的文本。我们从 Google Suggest（通过`google.php`）获取的文本可以在`XMLHttpRequest`对象的`responseText`属性中访问，我们可以如下使用`replace`方法，将调用 "window.google.ac.Suggest_apply" 转换为 "callback"，并将结果编辑后的文本存储在名为`text`的变量中：

```html
<script language="javascript">
function getData(dataSource)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", dataSource);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 && XMLHttpRequestObject.status == 200) {
                var text =
                XMLHttpRequestObject.responseText.replace(
                    "window.google.ac.Suggest_apply", "callback");
                .
                .
                .
            }
        }

    }
}
</script>
```

太好了；现在存储在`text`变量中的 JavaScript 可以被视为可工作的 JavaScript（一旦我们创建了名为`callback`的函数）。下面是如何用`eval`函数执行那段 JavaScript——注意我们同时也用`XMLHttpRequest`对象的`send`方法连接到服务器：

```html
<script language="javascript">
    function getData(dataSource)
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {
            XMLHttpRequestObject.open("GET", dataSource);

            XMLHttpRequestObject.onreadystatechange = function()
            {
                if (XMLHttpRequestObject.readyState == 4 &&
                    XMLHttpRequestObject.status == 200) {
                    var text =
                        XMLHttpRequestObject.responseText.replace(
                            "window.google.ac.Suggest_apply", "callback");
                    eval(text);
                }
            }

            XMLHttpRequestObject.send(null);
        }
    }
</script>
```

这就完成了`getData`函数，它调用了从 Google Suggest 下载的 JavaScript。我们已经编辑了那段 JavaScript，使其调用一个名为`callback`的函数，现在我们必须编写`callback`函数。

## 显示匹配结果

以下是被`getData`函数下载、编辑并执行的 JavaScript：

```javascript
callback(frameElement, "a", new Array(2, "amazon", "855,000,000 results",
"argos", "12,500,000 results", "aol", "278,000,000 results", "autotrader",
"5,820,000 results", "apple", "436,000,000 results", "amazon.com",
"461,000,000 results", "aol.com", "87,200,000 results",
"american airlines", "14,600,000 results", "australian open",
"12,300,000 results", "ask.com", "39,600,000 results"), new Array(""));
```

我们的`callback`函数应该接受这些参数，所以创建该函数的方法如下：

```html
<script language="javascript">
    function callback(unusedVariable, searchTerm, arrayTerm,
        unusedArray)
    {
        .
        .
        .
    }
</script>
```

我们将把建议的下拉列表显示为一个 HTML 表格，并将该 HTML 存储在一个名为`data`的变量中。以下是我们如何创建`data`变量并设置循环来添加从 Google Suggest 获取的所有建议：



```javascript
<script language = "javascript">
    function callback(unusedVariable, searchTerm, arrayTerm,
        unusedArray)
    {
        var data = "<table>";
        var loopIndex;

        for (loopIndex = 1; loopIndex < arrayTerm.length;
            loopIndex++) {
            .
            .
            .
        }

        data += "</table>";
    }
</script>
```

下面是实际的循环，遍历从 Google Suggest 获取的建议——注意我们将搜索词变成了超链接（指向 Google），就像真实的 Google Suggest 页面一样：

```javascript
<script language = "javascript">
    function callback(unusedVariable, searchTerm, arrayTerm,
        unusedArray)
    {
        var data = "<table>";
        var loopIndex;

        for (loopIndex = 1; loopIndex < arrayTerm.length;
             loopIndex++) {
            data += "<tr><td>" +
            "<a href='http://www.google.com/search?q=" +
            arrayTerm[loopIndex] + "'>" + arrayTerm[loopIndex] +
            "</a></td><td>" + arrayTerm[++loopIndex] + "</td></tr>";
        }

        data += "</table>";
    }
</script>
```

### 专家问答

**问：** 在上面的代码中，`++loopIndex` 这个术语是做什么的？它和 `loopIndex++` 有什么不同？

**答：** 将 JavaScript 自增运算符（在第 2 章介绍过）放在变量名前面（`++loopIndex`）会在执行其余 JavaScript 语句之前将变量的值加 1，而将运算符放在变量名末尾（`loopIndex++`）则意味着在执行完其余语句之后才会将变量的值加 1。通常选择哪一个并不重要，但在这里它很重要，因为我们需要在使用 `loopIndex` 获取建议数组中的下一个建议之前对其递增。

在 `callback` 函数的代码末尾，`data` 变量保存了我们将用于显示从 Google Suggest 获取的建议的 HTML 表格，我们通过将 `data` 赋值给将显示下拉列表的 `<div>` 元素的 `innerHTML` 属性来显示该表格：

```javascript
<script language = "javascript">
    function callback(unusedVariable, searchTerm, arrayTerm,
                       unusedArray)
    {
        var data = "<table>";
        var loopIndex;

        for (loopIndex = 1; loopIndex < arrayTerm.length;
             loopIndex++) {
```

# 136 Ajax：初学者指南

```javascript
data += "<tr><td>" +
    "<a href='http://www.google.com/search?q=" +
    arrayTerm[loopIndex] + "'>" + arrayTerm[loopIndex] +
    "</a></td><td>" + arrayTerm[++loopIndex] + "</td></tr>";
}

data += "</table>";

var targetDiv = document.getElementById("targetDiv");

targetDiv.innerHTML = data;
}
</script>
```

这是最后一个步骤。我们可以为显示 Google Suggest 建议的 `<div>` 元素设置样式，使其具有下拉列表的外观。下面是在 google.html 应用程序中使用 `<style>` 元素为 `<div>` 元素中出现的 HTML 设置浅粉色背景的方法：

```html
<html>
    <head>
        <title>处理 Google Suggest</title>

        <style>
        #targetDiv {
            background-color: #FFAAAA;
            width: 40%;
        }
        </style>

        <script language = "javascript">
            function getData(dataSource)
            .
            .
            .
```

至此，google.html 就完成了——这是它的完整形态：

```html
<html>
    <head>
        <title>处理 Google Suggest</title>

        <style>
        #targetDiv {
            background-color: #FFAAAA;
            width: 40%;
        }
        </style>
```

```html
</style>

<script language = "javascript">
function getData(dataSource)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", dataSource);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                    var text = XMLHttpRequestObject.responseText.replace(
                        "window.google.ac.Suggest_apply", "callback");
                    eval(text);
            }
        }

        XMLHttpRequestObject.send(null);
    }
}

function askGoogleSuggest()
{
    var input = document.getElementById("textField");

    if (input.value) {
        getData("google.php?qu=" + input.value);
    }
    else {
        var targetDiv = document.getElementById("targetDiv");

        targetDiv.innerHTML = "<div></div>";
    }
}

function callback(unusedVariable, searchTerm, arrayTerm,
    unusedArray)
{
    var data = "<table>";
    var loopIndex;
```

```javascript
for (loopIndex = 1; loopIndex < arrayTerm.length; loopIndex++) {
    data += "<tr><td>" +
        "<a href='http://www.google.com/search?q=" +
        arrayTerm[loopIndex] + "'>" +
        arrayTerm[loopIndex] +
        "</a></td><td>" + arrayTerm[++loopIndex] + "</td></tr>";
}

data += "</table>";

var targetDiv = document.getElementById("targetDiv");

targetDiv.innerHTML = data;
}
</script>
</head>
<body>
<H1>处理 Google Suggest</H1>
搜索 <input id = "textField" type = "text"
    name = "textField" onkeyup = "askGoogleSuggest()">
<div id = "targetDiv"><div></div></div>
</body>
</html>
```

很好，google.html 到这里就完成了。最后一步是创建与之通信的 PHP 脚本，google.php。

## 创建 google.php

如你所知，google.html 依赖于一个 PHP 脚本 google.php 来连接 Google Suggest。google.html 应用程序通过这种方式连接 Google Suggest，以避免当使用 Ajax 连接到与页面所在服务器不同的服务器时可能引发的安全问题。

因此，我们将使用 google.php 来连接 Google Suggest。Google Suggest 的 URL 是 `"http://www.google.com/complete/search?hl=en&js=true&qu="`，你需要在 URL 末尾添加用户输入的部分搜索词——例如，如果搜索词是 `"ajax"`，那么你访问的 URL 就是 `"http://www.google.com/complete/search?hl=en&js=true&qu=ajax"`。

如何使用 PHP 脚本访问这样的 URL 呢？你将在本书后面更详细地了解 PHP，但事实上，在 PHP 中你可以像处理文件名一样处理 URL，并且可以使用 `fopen`（文件打开）函数来“打开”一个 URL，该函数返回一个*文件句柄*，你将其存储在一个变量中（本书不会过多使用文件句柄或 PHP 文件处理，但此示例会用到）。然后你可以使用该文件句柄来引用该 URL，包括从该 URL 读取数据。下面是如何使用传递给 google.php 的部分搜索字符串来“打开” Google Suggest（你从 `$_GET` 数组中获取部分搜索词，然后使用 PHP 字符串连接运算符（即点号 `.`）将该词添加到 URL 中）：

```php
<?php
$filehandle =
    fopen("http://www.google.com/complete/search?hl=en&js=true&qu=" .
    $_GET["qu"], "r");
    .
    .
    .
?>
```

这里的 `"r"` 表示我们要以读取方式打开 Google Suggest URL（而不是尝试写入）。

现在你准备好读取 Google Suggest 将传回给你的建议了。你可以在 PHP 的 `while` 循环中完成此操作，其工作方式与 JavaScript 中的 `while` 循环一样。在这个 `while` 循环中，我们将从文件句柄读取数据，并可以使用 PHP 的 `feof`（文件结束）函数来判断何时到达“文件”末尾（此时 `while` 循环应终止）：

```php
<?php
$filehandle =
    fopen("http://www.google.com/complete/search?hl=en&js=true&qu=" .
    $_GET["qu"], "r");
while (!feof($filehandle)){
    .
    .
    .
}
?>
```

注意这里的 `while` 循环条件——`!feof($filehandle)`。`!` 是什么？它是一个运算符（在 PHP 和 JavaScript 中都如此；参见表 2-1），用于反转表达式的逻辑意义。因此，当到达文件末尾时，`feof($filehandle)` 为 true，而 `!feof($filehandle)` 在我们*未*到达文件末尾时为 true——这正是我们想要的，以确保 `while` 循环持续循环直到到达文件末尾。

现在 google.php 从 Google Suggest 读取单行文本，并使用 PHP 的 `fgets`（文件获取字符串）和 `echo` 函数将其回显给 google.html：

```php
<?php
$filehandle =
    fopen("http://www.google.com/complete/search?hl=en&js=true&qu=" .
    $_GET["qu"], "r");
while (!feof($filehandle)){
```

```php
$download = fgets($filehandle);
echo $download;
}
?>
```

我们快完成了。在 google.php 末尾只剩下关闭我们一直在读取的 URL，我们可以使用 PHP 的 `fclose`（文件关闭）函数来完成：

```php
<?php
$filehandle = 
    fopen("http://www.google.com/complete/search?hl=en&js=true&qu=" .
    $_GET["qu"], "r");
while (!feof($filehandle)){
    $download = fgets($filehandle);
    echo $download;
}
fclose($filehandle);
?>
```

呼。全部完成。这个示例——google.html 和 google.php——已经准备就绪。这个示例在用户输入时读取他们输入的内容，通过 google.php 将其转发给 Google Suggest，下载 Google Suggest 的建议，然后显示它们。

你可以在图 4-8 中看到这个示例的实际效果，其中用户输入了 `"a"`，应用程序已经下载了 Google Suggest 提出的建议并正在显示它们。非常酷。

这样就完成了 google.html。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_159_0.png)

## 使用 Ajax 从其他域下载

正如你在构建 google.html 时看到的，使用 Ajax 访问不同于网页托管服务器的服务器有点棘手。假设你的 Ajax 页面位于 `www.myserver.com/hamster_fan.html`，但你想要下载位于 `www.theirserver.com/hamster_data.html` 的页面——即位于不同的服务器上。你可以从当前页面直接通过 Ajax 访问该页面，但浏览器会向用户显示一个警告对话框，请求他们继续的许可。

这不是最酷的事情。

常见的解决方案是通过服务器端代码与另一台服务器（`www.theirserver.com`）通信，你在 google.php 中看到了一个例子。通过 google.php，我们能够将我们的请求转发给 Google Suggest，然后下载 Google Suggest 的响应。

下面是一个通用的 PHP 脚本，让你可以以这种方式重定向 Ajax 请求——将*URL*替换为你想要访问的 Web 资源的 URL：

```php
<?php
$filehandle = 
   fopen(URL, "r");
while (!feof($filehandle)){
   $download = fgets($filehandle);
   echo $download;
}
fclose($filehandle);
?>
```

### 动手试试：使用 Ajax 联系另一台服务器

在你让 google.html 和 google.php 正常工作后，尝试对另一台服务器使用相同的技术。例如，你可以下载并显示*今日美国*网站（`www.usatoday.com`）的 HTML。在 PHP 脚本中这样操作：



```php
<?php
$filehandle = 
   fopen("www.usatoday.com", "r");
while (!feof($filehandle)){
   $download = fgets($filehandle);
   echo $download;
}
fclose($filehandle);
?>
```

如果你愿意，甚至可以修改`google.php`以从`www.usatoday.com`下载，并直接使用现有的`google.html`来连接和显示*今日美国*网站的 HTML。

现在是时候转向另一个主题了——使用 Ajax 请求 HTML 头信息。

## 获取更多信息：HTML 头信息请求与 Ajax

你不仅可以使用 Ajax 下载文件内容，还能获取关于这些文件的信息。为此，你可以使用`XMLHttpRequest`对象的`getAllResponseHeaders`方法，它能返回服务器返回的所有 HTML 头信息对应的文本。

HTTP 头信息有诸如`Server`、`Date`等名称，并被赋予关于你正在访问资源的文本描述。你甚至可以在尝试下载网络资源之前，使用这类信息来了解该资源的大小、类型、最后修改日期等，从而更好地为下载做准备。而且，如果用户请求你下载一个不存在的资源，你可以在所需数据未显示时告知他们，而不会让你的应用程序因数据缺失而报错。

让我们来尝试一下，看看能为`google.html`文件下载到什么样的 HTTP 头信息。这是`head.html`文件，它仅仅使用`XMLHttpRequest`对象的`getAllResponseHeaders`方法，来获取服务器关于`google.html`的所有可用 HTTP 头信息。我们在调用`open`函数时使用`"HEAD"`方法，而不是`"GET"`或`"POST"`：

```html
<html>
  <head>
    <title>Getting head data</title>

    <script language = "javascript">
      function getData(dataSource, divID)
      {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
          XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
          XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {
          var obj = document.getElementById(divID);
          XMLHttpRequestObject.open("HEAD", dataSource);
          .
          .
          .
```

然后我们使用`getAllResponseHeaders`来读取所有 HTTP 头信息：

```html
<html>
  <head>
    <title>Getting head data</title>

    <script language = "javascript">
      function getData(dataSource, divID)
      {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
          XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
          XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }

        if (XMLHttpRequestObject) {
          var obj = document.getElementById(divID);
          XMLHttpRequestObject.open("HEAD", dataSource);

          XMLHttpRequestObject.onreadystatechange = function()
          {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                obj.innerHTML =
                    XMLHttpRequestObject.getAllResponseHeaders();
            }
          }

          XMLHttpRequestObject.send(null);
        }
      }
    </script>
  </head>

  <body>
    <H1>Getting header data</H1>

    <form>
        <input type = "button" value = "Get info on google.html"
            onclick = "getData('google.html', 'targetDiv')">
    </form>

    <div id="targetDiv">
        <p>The fetched data will go here.</p>
    </div>
  </body>
</html>
```

你可以在图4-9中看到`head.html`的工作效果，用户已点击按钮，应用程序获取了关于`google.html`的信息。

以下是应用程序获得的数据：

```
Server: Microsoft-IIS/5.1 Date: Fri, 22 Feb 2008 17:15:09 GMT
Content-Type: text/html Accept-Ranges: bytes Last-Modified:
Thu, 21 Feb 2008 18:26:23 GMT ETag: "82283a43b774c81:a57"
Content-Length: 2304
```

144 Ajax：入门指南

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_163_0.png)

你可以在这里看到各个 HTTP 头信息：例如，`Server: Microsoft-IIS/5.1`告诉你服务器运行的软件。`Content-Length: 2304`告诉你`google.html`的长度。`Content-Type: text/html`告诉你它是一个 HTML 文件，等等。

## 获取特定的 HTML 头信息

如果你使用`getResponseHeader`，也可以一次只请求一个特定的 HTTP 头信息。尝试这种获取`google.html`的`"Last-Modified"`头信息的技术：

```javascript
function getData(dataSource, divID)
{
    if(XMLHttpRequestObject) {
        var obj = document.getElementById(divID);
        XMLHttpRequestObject.open("HEAD", dataSource);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                obj.innerHTML =
                    "The file google.html was last modified on " +
                    XMLHttpRequestObject.getResponseHeader(
                        "Last-Modified");
            }
        }

        XMLHttpRequestObject.send(null);
    }
}
```

## 突破缓存

开发 Ajax 应用程序时一个令人沮丧的方面是浏览器缓存，尤其是在 Internet Explorer 中。当浏览器访问一个 URL 时，缓存就会发生——它会存储服务器响应的副本，并且即使你要求它直接访问该 URL，它实际上也不会再次访问。

如果你正在修改一个网络资源——比如开发应用程序时——或者网络资源在不同时间给你不同的数据，这就是个问题。例如，假设你正在调试`important_data.php`，并且当用户点击按钮时，你像这样从该 PHP 文件下载文本：

```html
<body>
    <H1>Reading JavaScript with Ajax</H1>

    <form>
        <input type = "button" value = "Get the JavaScript"
            onclick = "getData('important_data.php')">
    </form>

    <div id="targetDiv">
        <p>The data will go here.</p>
    </div>
</body>
```

当你对`important_data.php`进行更改时，你希望浏览器使用它返回的新数据，但当浏览器缓存了该数据时，你只会一直看到旧数据。为了绕过缓存，你可以通过添加一点 URL 编码（这会被`important_data.php`忽略）来稍微改变你访问的 URL。当浏览器看到你正在访问一个不同的、没有缓存的 URL 时，它就会从该 URL 下载一份新的数据副本。下面是一个示例——注意 URL 末尾添加的虚拟`"?a=5"` URL 编码：

```html
<body>
    <H1>Reading JavaScript with Ajax</H1>

    <form>
        <input type = "button" value = "Get the JavaScript"
            onclick = "getData('important_data.php?a=5')">
    </form>

    <div id="targetDiv">
        <p>The data will go here.</p>
    </div>
</body>
```

这种技术的问题是，一旦你使用了新 URL `important_data.php?a=5`，浏览器也会缓存那个 URL，你就不能再使用它了。一个更好的解决方案是在 URL 编码的文本中使用一些总是会变化的东西，比如当前时间。下面是使用 JavaScript 的`getTime`函数来实现的方法：

```html
<body>
    <H1>Reading JavaScript with Ajax</H1>

    <form>
        <input type = "button" value = "Get the JavaScript"
            onclick = "getData('important_data.php?a=' + 
                new Date().getTime())">
    </form>

    <div id="targetDiv">
        <p>The data will go here.</p>
    </div>
</body>
```

这段代码将克服浏览器中的缓存问题。

# 第5章：使用 Ajax 框架

## 关键技能与概念

- 构建 Ajax 框架库
- 创建`downloadText`函数
- 创建`downloadXml`函数
- 创建`postDataDownloadText`函数
- 创建`postDataDownloadXml`函数
- 使用`libXmlRequest` Ajax 框架
- 使用`AJAXLib` Ajax 框架

正如你在前几章所看到的，编写 Ajax 程序可能有点棘手。因此，你会在网上遇到几十个 Ajax 框架。Ajax 框架是预先编写的代码（通常是 JavaScript），它使得使用 Ajax 变得轻而易举。所有的 Ajax 编程都为你完成了——例如，要使用 Ajax 从服务器下载文本，你只需调用一个名为`downloadText`（比如）的函数即可。你不必关心细节。

在本章中，我们将构建自己的 Ajax 框架`ajaxframework.js`（可在本书的可下载代码中免费获取），随时供你插入并使用。这里开发的 Ajax 框架将使用良好的编码技术，并支持多个`XMLHttpRequest`请求。我们还将在本章中看一看一些已有的 Ajax 框架。

让我们从创建`ajaxframework.js`开始。

## 创建`ajaxframework.js`

从`.js`扩展名可以看出，`ajaxframework.js`是一个 JavaScript 函数库。它包含四个函数，支持四种 Ajax 操作——使用 GET 下载文本、使用 GET 下载 XML、使用 POST 下载文本和使用 POST 下载 XML。以下是我们 Ajax 框架中可以调用的四个函数的概述：

- `downloadText(url, callbackFunction)`：使用 GET 方法从服务器获取文本。
- `downloadXml(url, callbackFunction)`：使用 GET 方法从服务器获取 XML。
- `postDataDownloadText(url, dataToSend, callbackFunction)`：使用 POST 方法将`dataToSend`发送到服务器，并获取文本返回。你以参数/值对的形式传递要发送的数据，例如：`"value=100"`。
- `postDataDownloadXml(url, dataToSend, callbackFunction)`：使用 POST 方法将`dataToSend`发送到服务器，并获取 XML 响应。你需要以参数/值对的形式传递要发送的数据，例如：`"value=100"`。

请注意，对于每个函数，你都需要传递一个要调用的 URL——即你想要下载的数据对应的 URL。你还需要传递一个回调函数，我们的 Ajax 框架会使用下载的数据来调用该函数。如果你打算使用 POST 方法，你还可以向服务器发送数据。

让我们从了解如何创建`downloadText`函数开始本章。

## 使用`downloadText`函数下载文本

我们将在 Ajax 框架中构建的第一个函数是`downloadText`函数，它使用 GET 方法从服务器下载文本。你需要向此函数传递用于通过 Ajax 获取数据的 URL，以及一个应该用下载的数据进行回调的回调函数：

```javascript
function downloadText(url, callbackFunction)
{
    .
    .
    .
}
```

首要任务是创建一个`XMLHttpRequest`对象，用于在后台与服务器通信——注意我们是在`downloadText`函数内部创建它的，因此即将出现的匿名函数将是一个内部函数。以下是如何为 Firefox 类型的浏览器（如 Firefox、Netscape 和 Safari）创建`XMLHttpRequest`对象：

```javascript
function downloadText(url, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    }
    .
    .
    .
}
```

以下是如何为 Internet Explorer 创建`XMLHttpRequest`对象：

```javascript
function downloadText(url, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }
    .
    .
    .
}
```

接下来，我们检查是否成功创建了所需的`XMLHttpRequest`对象：



如果`XMLHttpRequest`对象存在，我们可以打开它来配置该对象，如下所示，向`open`方法传递HTTP方法（`"GET"`）和要访问的URL（该URL是通过`downloadText`函数的`url`参数传入的）：

```
function downloadText(url, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", url);
        .
        .
        .
    }
}
```

接下来，我们可以设置将要处理下载文本的匿名函数：

```
function downloadText(url, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
        ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", url);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            .
            .
            .
        }
    }
}
```

然后我们检查下载是否成功：

```
function downloadText(url, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
        ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", url);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                .
                .
                .
            }
        }
    }
}
```

此时，我们已知道数据已安全下载。我们如何处理这些数据呢？我们必须将该数据发送给传递给`downloadText`函数的回调函数（作为`callbackFunction`参数）。以下是我们如何将下载的文本传递给回调函数：

```
function downloadText(url, callbackFunction)
{
  var XMLHttpRequestObject = false;

  if (window.XMLHttpRequest) {
    XMLHttpRequestObject = new XMLHttpRequest();
  } else if (window.ActiveXObject) {
    XMLHttpRequestObject = new
      ActiveXObject("Microsoft.XMLHTTP");
  }

  if(XMLHttpRequestObject) {
    XMLHttpRequestObject.open("GET", url);

    XMLHttpRequestObject.onreadystatechange = function()
    {
      if (XMLHttpRequestObject.readyState == 4 &&
          XMLHttpRequestObject.status == 200) {
          callbackFunction(XMLHttpRequestObject.responseText);
          .
          .
          .
      }
    }

  }
}
```

现在我们处理完了`XMLHttpRequest`对象，如果我们愿意，可以显式地删除它。如下所示，我们删除该对象并将变量`XMLHttpRequestObject`设置为`null`：

```
function downloadText(url, callbackFunction)
{
  var XMLHttpRequestObject = false;

  if (window.XMLHttpRequest) {
    XMLHttpRequestObject = new XMLHttpRequest();
  } else if (window.ActiveXObject) {
    XMLHttpRequestObject = new
      ActiveXObject("Microsoft.XMLHTTP");
  }

  if(XMLHttpRequestObject) {
    XMLHttpRequestObject.open("GET", url);

    XMLHttpRequestObject.onreadystatechange = function()
    {
      if (XMLHttpRequestObject.readyState == 4 &&
          XMLHttpRequestObject.status == 200) {
          callbackFunction(XMLHttpRequestObject.responseText);
          delete XMLHttpRequestObject;
          XMLHttpRequestObject = null;
      }
    }

    XMLHttpRequestObject.send(null);
  }
}
```

最后，剩下的就是通过`XMLHttpRequest`对象的`send`方法连接到服务器：

```
function downloadText(url, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }

    if (XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", url);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                callbackFunction(XMLHttpRequestObject.responseText);
                delete XMLHttpRequestObject;
                XMLHttpRequestObject = null;
            }
        }

        XMLHttpRequestObject.send(null);
    }
}
```

现在，让我们通过创建一个使用它的Ajax页面来测试`downloadText`函数。这个页面将有两个按钮，其中一个将下载`data.txt`的内容：

```
This text was downloaded with Ajax.
```

另一个按钮将下载`data2.txt`的内容：

```
This text was also downloaded with Ajax.
```

我们将这个用于测试`downloadText`函数的页面命名为`downloadText.html`。我们首先包含`ajaxframework.js`，这使得`downloadText`函数对我们的JavaScript可用：

```
<html>
  <head>
    <title>Downloading Text With the Ajax Framework Library Pack</title>
    <script type = "text/javascript" src = "ajaxframework.js"></script>
    .
    .
    .
```

现在我们可以将两个按钮添加到测试网页中：

```
<form>
  <input type = "button" value = "Get message 1"
         onclick = "downloadText('data.txt', callbackMessage1)">
  <input type = "button" value = "Get message 2"
         onclick = "downloadText('data2.txt', callbackMessage2)">
</form>
```

注意我们在这里做什么：我们向`downloadText`函数传递要获取的数据的URL（就是`"data.txt"`或`"data2.txt"`——我们假设`data.txt`和`data2.txt`与`ajaxframework.js`和`downloadText.html`位于同一目录和同一服务器上，因此这里可以使用相对URL）以及回调函数。

按钮1的回调函数命名为`callbackMessage1`，按钮2的回调函数命名为`callbackMessage2`。在这些回调函数中，我们只想在ID为`"targetDiv"`的`<div>`元素中显示下载的文本：

```
<body>
  <H1>Downloading Text With the Ajax Framework Library Pack</H1>
  <form>
    <input type = "button" value = "Get message 1"
           onclick = "downloadText('data.txt', callbackMessage1)">
  </form>
```

## 第5章：使用Ajax框架

```
<input type = "button" value = "获取消息 2"
       onclick = "downloadText('data2.txt', callbackMessage2)">
</form>

<div id="targetDiv">
  <p>获取的数据将显示在此处。</p>
</div>

</body>
```

回调函数`callbackMessage1`的代码如下所示：

```
<script language = "javascript">
  function callbackMessage1(text)
  {
    document.getElementById("targetDiv").innerHTML = text;
  }
  .
  .
  .
</script>
```

回调函数`callbackMessage2`的代码如下所示：

```
<script language = "javascript">
  function callbackMessage1(text)
  {
    document.getElementById("targetDiv").innerHTML = text;
  }

  function callbackMessage2(text)
  {
    document.getElementById("targetDiv").innerHTML = text;
  }
</script>
```

很好，代码完成了。下面是测试`downloadText`函数的完整页面`downloadText.html`：

```
<html>
  <head>
    <title>使用Ajax框架库包下载文本</title>

    <script type = "text/javascript" src = "ajaxframework.js"></script>

    <script language = "javascript">
      function callbackMessage1(text)
      {
        document.getElementById("targetDiv").innerHTML = text;
      }

      function callbackMessage2(text)
      {
        document.getElementById("targetDiv").innerHTML = text;
      }
    </script>

  </head>

  <body>

    <H1>使用Ajax框架库包下载文本</H1>

    <form>
        <input type = "button" value = "获取消息 1"
               onclick = "downloadText('data.txt', callbackMessage1)">
        <input type = "button" value = "获取消息 2"
               onclick = "downloadText('data2.txt', callbackMessage2)">
    </form>

    <div id="targetDiv">
        <p>获取的数据将显示在此处。</p>
    </div>

  </body>
</html>
```

你可以在图5-1中看到此页面的实际运行效果。

当你点击按钮1时，确实会下载并显示正确的数据。我们成功了——目前为止一切顺利。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_175_0.png)

图5-1  downloadText.html 的运行效果

### 试试看：让 downloadText.html 工作起来

请注意，如果你想通过HTTP GET方法向服务器发送数据，你必须对数据进行URL编码。这同样适用于`downloadText`函数。下面是一种测试方法，用于验证你是否能访问支持PHP的服务器，这里使用了第3章开发的`dataresponder.php`脚本：

```
<?php
if ($_GET["data"] == "1") {
    echo '服务器收到了值为1的数据';
}
if ($_GET["data"] == "2") {
    echo '服务器收到了值为2的数据';
}
?>
```

通过URL编码连接到此PHP脚本并发送数据，代码大致如下：



```html
<form>
    <input type = "button" value = "获取消息 1"
           onclick = "downloadText('dataresponder.php?data=1',
                                  callbackMessage1)">
    <input type = "button" value = "获取消息 2"
           onclick = "downloadText('dataresponder.php?data=2',
                                  callbackMessage2)">
</form>
```

当你点击第一个按钮时，你应该会看到“服务器收到了值为1的数据”，而当你点击第二个按钮时，你应该会看到“服务器收到了值为2的数据。”

### 使用`downloadXml`函数下载XML

你也可以使用GET方法来下载XML，这需要使用`ajaxframework.js`中的`downloadXml`函数（请记住，你将在第6章详细学习如何创建XML）。你向该函数传递服务器上XML文件的URL，以及一个回调函数，该回调函数将接收一个JavaScript XML文档对象：

```javascript
function downloadXml(url, callbackFunction)
{
    .
    .
    .
}
```

正如你所料，我们开始`downloadXml`函数时，首先创建一个`XMLHttpRequest`对象——请注意，我们为Firefox类型的浏览器设置了MIME类型为`text/xml`：

```javascript
function downloadXml(url, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
        XMLHttpRequestObject.overrideMimeType("text/xml");
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }
    .
    .
    .
}
```

然后，我们让这个`XMLHttpRequest`对象开始工作，从传递给`downloadXml`函数的URL下载请求的XML：

```javascript
function downloadXml(url, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
        XMLHttpRequestObject.overrideMimeType("text/xml");
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", url);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                .
                .
                .
            }
        }
    }
}
```

下载完成后，我们希望将下载的XML数据——以JavaScript XML文档对象的形式（由`XMLHttpRequest`对象的`responseXML`属性提供）——传递给回调函数。以下是具体的实现方式——请注意，我们同样使用`XMLHttpRequest`对象的`send`方法连接到服务器：

```javascript
function downloadXml(url, callbackFunction)
{
  var XMLHttpRequestObject = false;

  if (window.XMLHttpRequest) {
    XMLHttpRequestObject = new XMLHttpRequest();
    XMLHttpRequestObject.overrideMimeType("text/xml");
  } else if (window.ActiveXObject) {
    XMLHttpRequestObject = new
      ActiveXObject("Microsoft.XMLHTTP");
  }

  if(XMLHttpRequestObject) {
    XMLHttpRequestObject.open("GET", url);

    XMLHttpRequestObject.onreadystatechange = function()
    {
      if (XMLHttpRequestObject.readyState == 4 &&
          XMLHttpRequestObject.status == 200) {
          callbackFunction(XMLHttpRequestObject.responseXML);
          delete XMLHttpRequestObject;
          XMLHttpRequestObject = null;
      }
    }

    XMLHttpRequestObject.send(null);
  }
}
```

好的，`downloadXml`函数完成了。让我们用一个新的网页`downloadXml.html`来测试它，该页面将使用`downloadXml`函数下载并显示第3章中`colors.xml`的数据：

```xml
<?xml version = "1.0" ?>
<colors>
  <color>red</color>
  <color>green</color>
  <color>blue</color>
</colors>
```

我们将在`downloadXml.html`的开头引入Ajax框架`ajaxframework.js`：

```html
<html>
  <head>
    <title>使用Ajax框架库包下载XML</title>
    <script type = "text/javascript" src = "ajaxframework.js"></script>
```

接下来，我们将在`downloadXml.html`中提供一个按钮，允许用户下载`colors.xml`：

```html
    <form>
      <input type = "button" value = "获取颜色"
        onclick = "downloadXml('colors.xml', callback)">
    </form>
  </head>

  <body>
    <h1>使用Ajax框架库包下载XML</h1>

    <form>
      <input type = "button" value = "获取颜色"
        onclick = "downloadXml('colors.xml', callback)">
    </form>

    <div id="targetDiv">颜色将显示在此处。</div>

  </body>
</html>
```

请注意，此按钮调用`downloadXml`函数，传递要下载的XML文件的URL，以及一个简单的名为`callback`的回调函数。当用户点击此按钮时，我们将下载`colors.xml`，解析它，并在ID为`targetDiv`的`<div>`元素中显示颜色。

回调函数将由`ajaxframework.js`中的代码调用，并传入一个JavaScript XML文档对象：

```html
<script language = "javascript">

  function callback(xmlDocument)
  {
    .
    .
    .
  }

</script>
```

现在我们有了一个可供操作的JavaScript XML文档对象，我们需要提取`<color>`元素。我们首先使用`getElementsByTagName`方法获取这些元素的数组，我们将其命名为`colors`：

```html
<script language = "javascript">
function callback(xmlDocument)
{
    colors = xmlDocument.getElementsByTagName("color");
    .
    .
    .
}
</script>
```

现在我们可以设置文本并开始创建用于在`<div>`元素中显示颜色的项目符号列表：

```html
<script language = "javascript">
function callback(xmlDocument)
{
    var obj = document.getElementById('targetDiv');
    colors = xmlDocument.getElementsByTagName("color");
    obj.innerHTML = "以下是获取到的颜色：<ul>";
    .
    .
    .
}
</script>
```

然后我们可以遍历每个单独的颜色并显示它：

```html
<script language = "javascript">
function callback(xmlDocument)
{
    var obj = document.getElementById('targetDiv');
    colors = xmlDocument.getElementsByTagName("color");
    obj.innerHTML = "以下是获取到的颜色：<ul>";
    for (loopIndex = 0; loopIndex < colors.length; loopIndex++ )
    {
    .
    .
    .
    }
}
</script>
```

# 162 Ajax：初学者指南

要获取单个颜色，你需要在循环中将`<color>`元素访问为`colors[loopIndex]`。然后，你可以访问实际包含颜色文本的文本节点：

```xml
<?xml version = "1.0" ?>
<colors>
  <color>red</color>
  <color>green</color>
  <color>blue</color>
</colors>
```

这些文本节点可以被访问为`colors[loopIndex].firstChild`，而文本节点中的实际数据（即颜色本身的文本）可以被访问为`colors[loopIndex].firstChild.data`。那么，以下是如何提取并逐一显示颜色：

```javascript
<script language = "javascript">

function callback(xmlDocument)
{
    var obj = document.getElementById('targetDiv');

    colors = xmlDocument.getElementsByTagName("color");
    obj.innerHTML = "Here are the fetched colors:<ul>";
    for (loopIndex = 0; loopIndex < colors.length; loopIndex++ )
    {
        obj.innerHTML += "<li>" +
            colors[loopIndex].firstChild.data + "</li>";
    }
    obj.innerHTML += "</ul>";
}

</script>
```

以下是完整的`downloadXml.html`文件：

```html
<html>
  <head>

    <title>Downloading XML With the Ajax Framework Library Pack</title>

    <script type = "text/javascript" src = "ajaxframework.js"></script>

    <script language = "javascript">

    function callback(xmlDocument)
    {
        var obj = document.getElementById('targetDiv');

        colors = xmlDocument.getElementsByTagName("color");
        obj.innerHTML = "Here are the fetched colors:<ul>";
        for (loopIndex = 0; loopIndex < colors.length; loopIndex++ )
        {
            obj.innerHTML += "<li>" +
                colors[loopIndex].firstChild.data + "</li>";
        }
        obj.innerHTML += "</ul>";
    }

    </script>
  </head>

  <body>

    <h1>Downloading XML With the Ajax Framework Library Pack</h1>

    <form>
        <input type = "button" value = "Get the colors"
            onclick = "downloadXml('colors.xml', callback)">
    </form>

    <div id="targetDiv">The colors will appear here.</div>

  </body>

</html>
```

你可以在图5-2中看到这个页面的实际运行效果。当你点击按钮时，`colors.xml`文件会被下载并显示。很酷吧。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_182_0.png)

图5-2 运行中的`downloadXml.html`

**164 Ajax：初学者指南**

## 动手试试：让`downloadXml.html`工作起来

尝试在`downloadXml.html`中添加URL编码，这样你就可以为名为`data`的参数赋值为1或2，从而让服务器返回不同的颜色列表。你需要一个新的PHP脚本来实现这个功能——这就是它，`colors.php`：

```php
<?php
header("Content-type: text/xml");
if ($_GET["data"] == "1")
    $colors = array('red', 'green', 'blue');
if ($_GET["data"] == "2")
    $colors = array('orange', 'navy', 'viridian');
echo '<?xml version="1.0" ?>';
echo '<colors>';
foreach ($colors as $value)
{
    echo '<color>';
    echo $value;
    echo '</color>';
}
echo '</colors>';
?>
```

当你向这个脚本发送URL编码的数据时，它会响应你所请求的颜色集合，而`downloadXml.html`中的其余代码会正确地显示它。

## 使用`postDataDownloadText`函数发布数据并下载文本

你也可以使用我们Ajax框架的`postDataDownloadText`函数向服务器发布数据（使用POST方法）并下载文本。你需要向此函数传递URL、要发送的数据以及回调函数：

```javascript
function postDataDownloadText(url, dataToSend, callbackFunction)
{
    // ...
}
```

在`postDataDownloadText`函数中，我们首先创建一个`XMLHttpRequest`对象：



```javascript
function postDataDownloadText(url, dataToSend, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }
    // ...
}
```

然后我们检查是否成功创建了该对象：

```javascript
function postDataDownloadText(url, dataToSend, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        // ...
    }
}
```

如果`XMLHttpRequest`对象存在，我们就打开它，配置要访问的`URL`，并告诉它使用`POST`方法：

```javascript
function postDataDownloadText(url, dataToSend, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("POST", url);
        // ...
    }
}
```

# Ajax：初学者指南

正如第3章所讨论的，当你使用`POST`方法时，我们还将`Content-Type` HTTP头设置为`application/x-www-form-urlencoded`：

```javascript
function postDataDownloadText(url, dataToSend, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("POST", url);
        XMLHttpRequestObject.setRequestHeader('Content-Type',
            'application/x-www-form-urlencoded');
        // ...
    }
}
```

接下来，我们将一个匿名函数连接到`XMLHttpRequest`对象的`onreadystatechange`属性：

```javascript
function postDataDownloadText(url, dataToSend, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("POST", url);
        XMLHttpRequestObject.setRequestHeader('Content-Type',
            'application/x-www-form-urlencoded');

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                // ...
            }
        }
    }
}
```

当我们从服务器收到文本后，我们可以将其传递给用户希望我们使用的回调函数：

```javascript
function postDataDownloadText(url, dataToSend, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("POST", url);
        XMLHttpRequestObject.setRequestHeader('Content-Type',
            'application/x-www-form-urlencoded');

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                callbackFunction(XMLHttpRequestObject.responseText);
                delete XMLHttpRequestObject;
                XMLHttpRequestObject = null;
            }
        }
    }
}
```

这差不多就完成了——剩下的就是使用`XMLHttpRequest`对象的`send`方法将数据发布到服务器：

```javascript
function postDataDownloadText(url, dataToSend, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("POST", url);
        XMLHttpRequestObject.setRequestHeader('Content-Type',
            'application/x-www-form-urlencoded');
        // ...
    }
}
```

# Ajax：入门指南

```javascript
XMLHttpRequestObject.onreadystatechange = function()
{
    if (XMLHttpRequestObject.readyState == 4 &&
        XMLHttpRequestObject.status == 200) {
        callbackFunction(XMLHttpRequestObject.responseText);
        delete XMLHttpRequestObject;
        XMLHttpRequestObject = null;
    }
}
XMLHttpRequestObject.send(dataToSend);
}
```

好的，`postDataDownloadText`函数完成了；让我们在一个新页面`postDataDownloadText.html`中试用一下。在该页面中，我们首先引入`ajaxframework.js`，即包含`postDataDownloadText`函数的库：

```html
<head>
<title>使用 Ajax 框架库包发送数据和下载文本</title>
<script type="text/javascript" src="ajaxframework.js"></script>
.
```

我们将显示一个按钮来调用`postDataDownloadText`函数：

```html
<form>
<input type="button" value="获取文本"
onclick="postDataDownloadText('repeater.php', 'message=Hello there.', display)">
</form>
```

注意这里发生了什么：我们使用 URL`repeater.php`、一个数据字符串和一个回调函数`display`的名称来调用`postDataDownloadText`函数。这一切意味着什么？

让我们从`repeater.php`开始。这个 PHP 脚本只是发回你向它 POST 的任何文本；以下是 PHP 代码：

```php
<?php
echo ($_POST["message"]);
?>
```

那么我们传递给`postDataDownloadText`函数的数据字符串呢？它是这样的：`'message=Hello there.'`。我们传递这个字符串是因为这是使用`POST`方法时必须使用的那种数据类型（更多信息请参见第 3 章）。这个数据字符串将文本`"Hello there."`与参数`message`关联起来，这意味着`repeater.php`将能够读取该文本并将其返回。

`display`函数是我们的回调函数——即当文本从服务器下载完成时将被调用的函数。在`display`函数中，我们可以在一个`<div>`元素`targetDiv`中显示接收到的文本：

```html
<script language="javascript">
    function display(text)
    {
        document.getElementById('targetDiv').innerHTML = text;
    }
</script>
```

以下是整个页面`postDataDownloadText.html`的样子：

```html
<html>
  <head>
    <title>使用 Ajax 框架库包发送数据和下载文本</title>
    <script type="text/javascript" src="ajaxframework.js"></script>
    <script language="javascript">
      function display(text)
      {
        document.getElementById('targetDiv').innerHTML = text;
      }
    </script>
  </head>
  <body>
    <h1>使用 Ajax 框架库包发送数据和下载文本</h1>
    <form>
      <input type="button" value="获取文本"
      onclick=
      "postDataDownloadText('repeater.php', 'message=Hello there.', display)">
    </form>
    <div id="targetDiv">获取的文本将显示在这里。</div>
  </body>
</html>
```

你可以在图 5-3 中看到这个页面的实际运行效果，用户已点击按钮并使用`POST`方法下载了文本。效果不错。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_189_0.png)

## 使用 postDataDownloadXml 函数发送数据和下载 XML

我们已经使用`GET`下载了文本和 XML，也使用`POST`下载了文本，所以`ajaxframework.js`还剩一个主题——使用`POST`下载 XML。这由`ajaxframework.js`中一个名为`postDataDownloadXml`的函数处理，我们现在来看看如何创建这个函数。

使用`POST`，我们可以向服务器发送数据，我们将使用一个名为`colors.xml`的 PHP 脚本以 XML 形式返回两种配色方案之一：如果我们以名为`data`的参数发布一个值为`1`的参数，则返回其中一种；如果我们向此脚本发布一个值为`2`的参数，则返回另一种。向服务器发送数据并获取 XML 将使我们能够测试`postDataDownloadXml`函数。以下是`colors.php`的样子——我们首先告诉浏览器我们正在向其发送 XML：

```php
<?php
header("Content-type: text/xml");
?>
```

然后我们可以读取名为`data`的参数的值——如果它是`1`，我们将使用红色、绿色和蓝色作为返回给浏览器的颜色，方法是将它们存储在一个名为`$colors`的 PHP 数组中（在 PHP 中，变量以`$`开头）：

```php
<?php
header("Content-type: text/xml");
if ($_POST["data"] == "1")
$colors = array('red', 'green', 'blue');
.
.
.
?>
```

而配色方案 2 将是橙色、海军蓝和翠绿色：

```php
<?php
header("Content-type: text/xml");
if ($_POST["data"] == "1")
    $colors = array('red', 'green', 'blue');
if ($_POST["data"] == "2")
    $colors = array('orange', 'navy', 'viridian');
.
.
.
?>
```

将要使用的颜色存储在名为`$colors`的数组中后，我们可以构建返回给用户的 XML，配色方案 1 的 XML 如下所示：

```xml
<?xml version="1.0" ?>
<colors>
    <color>red</color>
    <color>green</color>
    <color>blue</color>
</colors>
```

配色方案 2 的 XML 如下所示：

```xml
<?xml version="1.0" ?>
<colors>
    <color>orange</color>
    <color>navy</color>
    <color>viridian</color>
</colors>
```

要将该 XML 发送回浏览器，我们从开始 XML 文档的 XML 声明（`<?xml version="1.0" ?>`）开始：



```php
<?php
header("Content-type: text/xml");
if ($_POST["data"] == "1")
    $colors = array('red', 'green', 'blue');
if ($_POST["data"] == "2")
    $colors = array('orange', 'navy', 'viridian');
echo '<?xml version="1.0" ?>';
.
.
.
?>
```

然后我们可以输出文档元素`<colors>`：

```php
<?php
header("Content-type: text/xml");
if ($_POST["data"] == "1")
    $colors = array('red', 'green', 'blue');
if ($_POST["data"] == "2")
    $colors = array('orange', 'navy', 'viridian');
echo '<?xml version="1.0" ?>';
echo '<colors>';
    .
    .
    .
echo '</colors>';
?>
```

然后我们可以使用 PHP `foreach`循环（见第 9 章）遍历`$colors`数组，并将每种颜色放入一个`<color>`元素中：

```php
<?php
header("Content-type: text/xml");
if ($_POST["data"] == "1")
    $colors = array('red', 'green', 'blue');
if ($_POST["data"] == "2")
    $colors = array('orange', 'navy', 'viridian');
echo '<?xml version="1.0" ?>';
echo '<colors>';
foreach ($colors as $value)
{
    echo '<color>';
    echo $value;
    echo '</color>';
}
echo '</colors>';
?>
```

很好，`colors.php`完成了。我们只需向此脚本发布一个名为`data`的参数，设置为 1 或 2，它就会返回配色方案 1 或 2。

现在我们知道了`postDataDownloadXml`函数将与之交互的脚本类型是什么样子，让我们来组合该函数。我们将要从中下载 XML 的 URL、要发送的数据以及回调函数传递给此函数：

```javascript
function postDataDownloadXml(url, dataToSend, callbackFunction)
{
    .
    .
    .
}
```

像往常一样，我们首先创建一个`XMLHttpRequest`对象，并检查是否成功创建了它：

```javascript
function postDataDownloadXml(url, dataToSend, callbackFunction)
{
    var XMLHttpRequestObject = false;
    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
        XMLHttpRequestObject.overrideMimeType("text/xml");
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
        ActiveXObject("Microsoft.XMLHTTP");
    }
    if(XMLHttpRequestObject) {
        .
        .
        .
    }
}
```

然后我们可以打开`XMLHttpRequest`对象，配置它要访问的 URL，并指定 POST 方法：

```javascript
function postDataDownloadXml(url, dataToSend, callbackFunction)
{
    var XMLHttpRequestObject = false;
    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
        XMLHttpRequestObject.overrideMimeType("text/xml");
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
        ActiveXObject("Microsoft.XMLHTTP");
    }
    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("POST", url);
        XMLHttpRequestObject.setRequestHeader('Content-Type',
            'application/x-www-form-urlencoded');
            .
            .
            .
    }
}
```

接下来我们可以设置匿名函数，该函数将被服务器返回的 XML 调用，我们将其传递给用户指定的回调函数，最后发送用户希望我们发送到服务器的数据字符串：

```javascript
function postDataDownloadXml(url, dataToSend, callbackFunction)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
        XMLHttpRequestObject.overrideMimeType("text/xml");
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("POST", url);
        XMLHttpRequestObject.setRequestHeader('Content-Type',
            'application/x-www-form-urlencoded');

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                    callbackFunction(XMLHttpRequestObject.responseXML);
                    delete XMLHttpRequestObject;
                    XMLHttpRequestObject = null;
            }
        }

        XMLHttpRequestObject.send(dataToSend);
    }
}
```

这样就完成了`ajaxframework.js`中的`postDataDownloadXml`函数。现在剩下的就是测试它，我们将使用名为`postDataDownloadXml.html`的文档进行测试。这个 HTML 文档将让用户点击两个按钮之一来下载两种配色方案：

```html
<form>
    <input type = "button" value = "Get color scheme 1"
        onclick = "postDataDownloadXml('colors.php', 'data=1', callback)">
    <input type = "button" value = "Get color scheme 2"
        onclick = "postDataDownloadXml('colors.php', 'data=2', callback)">
</form>
```

请注意，我们调用`postDataDownloadXml`函数来下载 XML 格式的配色方案——两种方案都来自`colors.php`脚本，但对于方案 1，我们发送值 1，对于方案 2，我们发送值 2。以下是整个`postDataDownloadXml.html`的样子：

```html
<html>
  <head>
    <title>Posting Data and Downloading Text With the Ajax Framework Library Pack</title>
    <script type = "text/javascript" src = "ajaxframework.js"></script>
    <script language = "javascript">
      function callback(xmlDocument)
      {
          var obj = document.getElementById('targetDiv');
          colors = xmlDocument.getElementsByTagName("color");
          obj.innerHTML = "Here are the fetched colors:<ul>";
          for (loopIndex = 0; loopIndex < colors.length; loopIndex++ )
          {
              obj.innerHTML += "<li>" + colors[loopIndex].firstChild.data + "</li>";
          }
          obj.innerHTML += "</ul>";
      }
    </script>
  </head>
  <body>
    <h1>Posting Data and Downloading Text With the Ajax Framework Library Pack</h1>
    <form>
      <input type = "button" value = "Get color scheme 1"
        onclick = "postDataDownloadXml('colors.php', 'data=1', callback)">
      <input type = "button" value = "Get color scheme 2"
        onclick = "postDataDownloadXml('colors.php', 'data=2', callback)">
    </form>
    <div id="targetDiv">Your color scheme will appear here.</div>
  </body>
</html>
```

你可以在图 5-4 中看到这个 HTML 文档`postDataDownloadXml.html`的实际运行效果——只需点击按钮，应用程序就会使用`postDataDownloadXml`函数下载匹配的配色方案。效果很棒。

这样就完成了`ajaxframework.js`库，这是一个方便的 JavaScript 库，包含以下函数：

- `downloadText(url, callbackFunction)`
- `downloadXml(url, callbackFunction)`
- `postDataDownloadText(url, dataToSend, callbackFunction)`
- `postDataDownloadXml(url, dataToSend, callbackFunction)`

使用`ajaxframework.js`意味着如果你不想自己编写 Ajax 代码，就不必编写——只需在你的页面中包含`ajaxframework.js`，然后调用相应的函数即可。

目前已经有许多 Ajax 框架，接下来我们将看看其中几个。

## 使用 libXmlRequest JavaScript Ajax 框架

在众多可用的 Ajax 框架中，有 libXmlRequest JavaScript Ajax 框架，你可以在`www.whitefrost.com/reference/2008/04/27/libXmlRequest.html`免费获取。该 JavaScript 库本身是`libXmlRequest.js`，当你在`<script>`元素中包含该文件时，就可以让你的代码访问`libXmlRequest`中的函数。

libXmlRequest 框架以两个 Ajax 函数为中心——`getXml`和`postXml`。请注意，这个库是基于 XML 的，并包含许多处理 XML 的函数。以下是 libXmlRequest 库中 Ajax 函数的概述：

- `getXml(url)`：一个同步 GET 请求，返回`null`或一个 XML 文档对象。
- `getXml(url, callback, 1)`：一个异步 GET 请求，如果请求成功则返回 1，并在 XML 下载完成时调用回调函数处理器。
- `postXml(url, data)`：一个同步 POST 请求，返回`null`或一个 XML 文档对象。
- `postXml(url, data, callback, 1)`：一个异步 POST 请求，如果请求成功则返回 1，并在 XML 下载完成时调用回调函数处理器。

回调函数被调用时带有两个参数，我们感兴趣的是第二个参数，因为它包含下载的 XML——特别是，该参数的`xdom`属性是包含我们请求的 XML 数据的 XML 对象。

让我们使用 libXmlRequest 下载并读取一个名为`hello.xml`的 XML 文档中的数据，该文档只包含文本“Hello from libXmlRequest.”：

```xml
<?xml version = "1.0" ?>
<text>
Hello from libXmlRequest.
</text>
```

我们将在一个名为`libxmlrequest.html`的 HTML 文档中测试 libXmlRequest。首先，我们包含`libXmlRequest.js`：

```html
<html>
  <head>
    <title>Using the libXmlRequest Ajax framework</title>
    <script src = "libXmlRequest.js"></script>
    .
    .
    .
</html>
```

然后我们添加一个按钮，该按钮调用 libXmlRequest 函数来获取 XML，`org.cote.js.xml.getXml`：

```html
<html>
  <head>
    <title>Using the libXmlRequest Ajax framework</title>
    <script src = "libXmlRequest.js"></script>
    .
    .
    .
<body>

    <h1>Using the libXmlRequest Ajax framework</h1>

    <form>
        <input type = "button" value = "Get the message"
               onclick = "org.cote.js.xml.getXml('hello.xml', callback, 1)">
    </form>
</body>
</html>
```

这个对`org.cote.js.xml.getXml`的调用将回调函数的名称简单地提供为“callback”，所以我们现在将添加该函数。我们只是想从下载的 XML 中提取`<text>`元素中的文本，我们可以通过使用`getElementsByTagName`方法提取`<text>`元素，使用`firstChild`属性从`<text>`元素中提取文本节点，然后使用文本节点的`data`属性最终到达文本来实现：



```html
<html>
<head>
    <title>Using the libXmlRequest Ajax framework</title>

    <script src = "libXmlRequest.js"></script>

    <script language = "javascript">

        function callback(a, b)
        {
            var textElement = b.xdom.getElementsByTagName("text");

            var div = document.getElementById('targetDiv');

            div.innerHTML = textElement[0].firstChild.data;

        }
    </script>
</head>

<body>

    <H1>Using the libXmlRequest Ajax framework</H1>

    <form>
      <input type = "button" value = "Get the message"
        onclick = "org.cote.js.xml.getXml('hello.xml', callback, 1)">
    </form>

    <div id="targetDiv">
      <p>The fetched data will go here.</p>
    </div>

</body>
</html>
```

就这样——这就完成了我们使用`libXmlRequest`库的示例。你可以在图5-5中看到这个网页的实际运行情况，它正确地下载了`hello.xml`文档。

现在让我们看看另一个 Ajax 框架——`AJAXLib`。

## 使用 AJAXLib JavaScript Ajax 框架

`AJAXLib`是一个免费的 Ajax 框架，你可以在`http://karaszewski.com/tools/ajaxlib/`获取。该框架的实际 JavaScript 库名为`ajaxlib.js`。

这个框架使用简单。你只需将此库的`loadXMLDoc`函数传递 XML 源的 URL、回调函数（用于调用下载的 XML）和一个布尔参数，该参数允许你删除下载 XML 中的空白字符（如果你传递值`true`，`AJAXLib`将删除 XML 中的缩进空白字符）。XML 下载完成后，它将可以通过名为`resultXML`的 JavaScript 变量在你的 JavaScript 代码中访问。

## 180 Ajax：入门指南

让我们在一个名为`ajaxlib.html`的示例中使用这个框架，通过`AJAXLib`从名为`hello2.xml`的文档中下载并提取文本“Hello from AJAXLib.”：

```xml
<?xml version = "1.0" ?>
<text>
Hello from AJAXLib.
</text>
```

`ajaxlib.html`网页以一个用于下载`hello2.xml`的按钮开始，并指定回调函数名为`callback`：

```html
<form>
  <input type = "button" value = "Get the message"
    onclick = "loadXMLDoc('hello2.xml', callback, false)">
</form>
```

在回调函数中，我们可以利用将存储在`resultXML`变量中的 JavaScript XML 文档对象来提取`hello2.xml`中的文本。以下是它在`ajaxlib.html`中的样子：

```html
<html>
  <head>
    <title>Using the AJAXLib Ajax framework</title>
    <script src = "ajaxlib.js"></script>
    <script language = "javascript">
      function callback()
      {
        var xmlData = resultXML.getElementsByTagName("text");
        var div = document.getElementById('targetDiv');
        div.innerHTML = xmlData[0].firstChild.data;
      }
    </script>
  </head>
  <body>
    <H1>Using the AJAXLib Ajax framework</H1>
    <form>
      <input type = "button" value = "Get the message"
        onclick = "loadXMLDoc('hello2.xml', callback, false)">
    </form>
  </body>
</html>
```

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_200_0.png)

图 5-6  运行中的 AJAXLib.html

```html
<div id="targetDiv">
    <p>The fetched data will go here.</p>
</div>
```

你可以在图 5-6 中看到结果——当用户点击按钮时，新消息确实被`AJAXLib`下载并显示出来了。很酷吧。

# 第六章：在 Ajax 中处理 XML

Ajax：入门指南

## 关键技能与概念

- 在 JavaScript 中处理 XML
- 遍历 XML 文档
- 检索 XML 元素数据
- 检索 XML 元素属性数据

Ajax 中的`x`代表 XML，本章将全部围绕在 Ajax 应用程序中处理 XML 展开。本章的大部分内容都与在 JavaScript 中使用 XML 有关，因为正如你已经看到的，这样做绝非易事。但你将在本章中获得在 JavaScript 中处理 XML 的宝贵经验。

我们将从讨论 XML 的工作原理开始（本书假设你了解 HTML，但对 XML 不做同样的假设）。

## 构建一些 XML

编写你自己的 XML 很像编写你自己的 HTML——你使用标签、元素和属性，就像在 HTML 中一样。关键的区别在于，在 XML 中，你可以自己创造元素名称。例如，以下是使用 HTML 4.01 预定义元素名称的 HTML 文档可能的样子：

```html
<html>
  <head>
    <title>The Report</title>
  </head>
  <body>
    <h1>The Report</h1>
    All Quiet on the Western Front.
  </body>
</html>
```

这在它本身的范围内是没问题的，但如果你想存储你自己的私有数据呢？例如，假设你想创建一个让你可以追踪朋友信息的文档？HTML 中没有`<friend>`元素，也没有`<first_name>`或`<last_name>`元素。但你可以在 XML 中创造并使用这些元素——没问题。

以下是这样一个文档在 XML 中可能的样子——注意，你在这里存储了三位朋友的信息：

```xml
<?xml version="1.0"?>
<friends>
    <friend>
        <first_name>Cary</first_name>
        <last_name>Grant</last_name>
    </friend>
    <friend>
        <first_name>Myrna</first_name>
        <last_name>Loy</last_name>
    </friend>
    <friend>
        <first_name>James</first_name>
        <last_name>Stewart</last_name>
    </friend>
</friends>
```

你可以在 XML 中自由使用你自己的元素名称，只要它们在语法上是合法的元素名称。这枚硬币有两面：虽然可以通过编程让浏览器理解 HTML 元素并相应地显示你的 HTML 文档，但对于 XML，你必须采取额外的步骤。也就是说，XML 文档完全是关于存储数据，而不是像 HTML 那样将数据可视化呈现，这意味着你必须提供一种方法来提取数据并自己处理它。这就是本章中 JavaScript 将要发挥作用的地方——你将在本章中看到如何使用 JavaScript 来读取和遍历 XML 文档。通过你自己的编程（对于 HTML 来说这一步是不必要的），你可以从 XML 文档中提取数据并使用这些数据。

这里有一些你应该了解的 XML 规则，我们现在就来看一下。我们将从零开始构建一个 XML 文档，记录派对上的出席人员——在这个例子中，是一个因学校取消课程（雪天）而举办的派对。

首先，所有 XML 文档都必须以*XML 声明*开头，它看起来像这样：

```xml
<?xml version="1.0" ?>
```

这是一个 XML 声明，而不是 XML 元素，它必须是 XML 文档的第一行。`version`属性是必需的，你可以将其设置为`"1.0"`（最常见的版本，也是我们将使用的版本）或`"1.1"`。除了`version`属性，你还可以包含`standalone`属性（如果此文档包含其他 XML 文档，则设置为`"no"`，否则设置为`"yes"`）和`encoding`属性（设置为你所使用的字符编码——例如，你可以指定你使用的是日文字符或俄文字符）。默认的编码是 UTF-8 字符集，这是 WordPad 和其他标准编辑器使用的编码（实际上，它们使用的是 UTF-8 的子集）：

```xml
<?xml version="1.0" standalone="yes" encoding="UTF-8" ?>
.
.
.
```

接下来，XML 文档中是包含文档数据的元素。你在 XML 中可以自己创造标签名称，但关于什么是合法的标签名称有一些规则。标签名称不能以数字开头，不能包含空格，也不能包含一些其他非法字符，例如引号或空格。以下是一些非法的标签名称：

```xml
<12steps>
<big dog>
"ok">
```

文档中的第一个元素是*文档元素*。在 XML 文档中，一个元素包裹所有其他元素，这个元素被称为文档元素。在我们这个雪天派对的例子中，我们可以将文档元素命名为`<parties>`，这样我们就可以记录多个派对：

```xml
<?xml version="1.0"?>
<parties>
.
.
.
</parties>
```

XML 文档中的每个其他元素都必须包含在这个文档元素内，因此，例如，如果你想记录三个不同派对的参加者，你可以在`<parties>`元素内包含三个`<party>`元素：

```xml
<?xml version="1.0"?>
<parties>
  <party>
    .
    .
    .
  </party>
  <party>
    .
    .
    .
  </party>
  <party>
    .
    .
    .
  </party>
</parties>
```

所以你看，就像 HTML 一样，XML 元素可以包含其他 XML 元素。事实上，你也可以有*空元素*，就像在 HTML 中一样（HTML 中的`<img>`元素就是一个空元素的例子）。空元素没有内容：没有嵌套的元素，没有嵌套的文本。在 XML 中，你使用标记`/>`来结束一个空元素，因此，例如，如果你有名为`<afternoon />`和`<evening />`的空元素，你可以使用这些元素来表示派对举行的时间：

```xml
<?xml version="1.0"?>
<parties>
    <party>
        <afternoon />
        .
        .
        .
    </party>
    <party>
        <evening />
        .
        .
        .
    </party>
    <party>
        <afternoon />
        .
        .
        .
    </party>
</parties>
```

XML 元素也可以包含*属性*，就像 HTML 元素一样。属性可以出现在元素的开始标签中，或者空元素内部，它们是名称/值对。例如，假设你想给`<party>`元素添加一个`type`属性，表示这是一个冬季派对；你可以这样做：

```xml
<?xml version="1.0"?>
<parties>
    <party type="winter">
        .
        .
        .
    </party>
</parties>
```

在 XML 中（不同于 HTML），你总是必须为属性赋值——在这个例子中，`type`是属性名称，而`"winter"`是属性值。属性值*必须始终*在引号内。

188 Ajax：入门指南

除了其他元素，你还可以将文本包含在 XML 元素中。以下是在我们完整的派对示例（即`party.xml`）中的可能形式：

```xml
<?xml version="1.0"?>
<parties>
    <party type="winter">
        <party_title>Snow Day</party_title>
        <party_number>63</party_number>
        <subject>No school today!</subject>
        <date>2/2/2009</date>
        <people>
            <person attendance="present">
                <first_name>Ralph</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="absent">
                <first_name>Alice</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="present">
                <first_name>Ed</first_name>
                <last_name>Norton</last_name>
            </person>
        </people>
    </party>
</parties>
```

现在你开始明白了吧。构建 XML 其实相当简单，但也有陷阱。我们构建的这个 XML 文档是所谓的*格式良好*的 XML 文档的一个例子。然而，很容易出错，导致你的 XML 文档格式不良好——而像浏览器这样的 XML 感知软件，如果你的 XML 格式不良好，就会报错。未能正确嵌套 XML 元素是主要的格式不良错误。例如，这个版本的示例 XML 文档，其中一个`<person>`元素在另一个开始前没有结束，就会因为嵌套错误而不被浏览器读取：

```xml
<?xml version="1.0"?>
<parties>
    <party type="winter">
        <party_title>Snow Day</party_title>
        <party_number>63</party_number>
        <subject>No school today!</subject>
        <date>2/2/2009</date>
        <people>
            <person attendance="present">
                <first_name>Ralph</first_name>
                <last_name>Kramden</last_name>
            <person attendance="absent">
                </person>
                <first_name>Alice</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="present">
                <first_name>Ed</first_name>
                <last_name>Norton</last_name>
            </person>
        </people>
    </party>
</parties>
```

这种错误很明显，但那些更细微的错误呢？你能发现我们文档以下版本中的错误吗？



```xml
<?xml version="1.0"?>
<parties>
  <party type="winter">
    <party_title>Snow Day</party_title>
    <party_number>63</party_number>
    <subject>No school today!</subject>
    <date>2/2/2009</date>
    <people>
      <person attendance="present">
        <first_name>Ralph</first_name>
        <last_name>Kramden</last_name>
      <person attendance="absent">
      </person>
        <first_name>Alice</first_name>
        <last_name>Kramden</last_name>
      </person>
      <person attendance="present">
        <first_name>Ed</first_name>
        <last_name>Norton</last_name>
      </person>
    </people>
  </party>
</parties>
```

错误在于第一个 `<person>` 元素中的 `attendance` 属性被拼写成了 `attendence`。文档格式是良好的，但它是不正确的。因此，除了格式良好性，XML 文档还可以进行有效性检查。要检查 XML 文档是否有效，你必须指定文档的合法语法。例如，一个 `<friend>` 元素可以包含一个 `<people>` 元素吗？一个 `<party>` 元素具有哪些属性？等等。

有两种方法来检查 XML 文档的有效性：XML 文档类型定义（DTD）和 XML Schema。两者都允许你指定 XML 文档的语法规则，在这两者中，XML Schema 是最新且最强大的。

不幸的是，你使用的浏览器可能不支持 XML Schema（Internet Explorer 的支持有问题），因此如果你想确保文档经过有效性检查，可能需要坚持使用较旧的方法来指定 XML 文档语法，即 DTD（我们将在本章末尾看到一个例子——请注意，在 Ajax 中使用 XML 并不强制要求进行有效性检查）。以下是我们示例 XML 文档的 DTD 格式：

```xml
<?xml version="1.0"?>
<!DOCTYPE parties [
<!ELEMENT parties (party*)>
<!ELEMENT party (party_title, party_number, subject, date, people*)>
<!ELEMENT party_title (#PCDATA)>
<!ELEMENT party_number (#PCDATA)>
<!ELEMENT subject (#PCDATA)>
<!ELEMENT date (#PCDATA)>
<!ELEMENT first_name (#PCDATA)>
<!ELEMENT last_name (#PCDATA)>
<!ELEMENT people (person*)>
<!ELEMENT person (first_name,last_name)>
<!ATTLIST party
    type CDATA #IMPLIED>
<!ATTLIST person
    attendance CDATA #IMPLIED>
]>
<parties>
    <party type="winter">
        <party_title>Snow Day</party_title>
        <party_number>63</party_number>
        <subject>No school today!</subject>
        <date>2/2/2009</date>
        <people>
            <person attendance="present">
                <first_name>Ralph</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="absent">
                <first_name>Alice</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="present">
                <first_name>Ed</first_name>
                <last_name>Norton</last_name>
            </person>
        </people>
    </party>
</parties>
```

如果你有兴趣确保 XML 文档的有效性，请查阅涵盖 DTD 和 XML Schema 的 XML 书籍。

好了，这为你奠定了良好的 XML 基础。让我们开始学习如何在 JavaScript 中处理 XML，这是你在 Ajax 应用程序中很可能要做的事情。

## 在 JavaScript 中使用 XML

要了解如何在 JavaScript 中使用 XML，你必须理解 JavaScript 如何看待 XML。JavaScript 从`节点`的角度看待 XML。以这个 XML 文档为例：

```xml
<?xml version="1.0" ?>
<document>
    <greeting>
        Welcome to XML
    </greeting>
    <text>
        Hello there!
    </text>
</document>
```

在这个例子中，`<document>` 节点有两个子节点，即 `<greeting>` 和 `<text>` 节点。这些节点是彼此的兄弟节点。`<greeting>` 和 `<text>` 元素本身各有一个子节点——一个包含字符数据的文本节点。作为节点树查看，这个文档的结构如下：

```text
                    <document>
                          |
-----------------------------------
            |                       |
     <greeting>               <text>
            |                       |
     Welcome to XML           Hello there!
```

对 JavaScript 来说，XML 文档是由节点构成的——而且不仅仅是元素节点。还有文本节点、属性节点等等。表 6-1 显示了节点类型（数字是 JavaScript 分配给每种节点类型的编号）。

JavaScript 有内置属性可用于处理 XML 文档中的节点（例如 `XMLHttpRequest` 对象的 `responseXML` 属性返回的 `document` 对象），如表 6-2 所示。

特别注意 `nodeType` 属性保存着节点的类型。你将在本章中看到如何在 JavaScript 中使用这些属性。

现在是写点代码的时候了，我们将从我们的示例 XML 文档 `party.xml` 中提取文档元素开始。

192 Ajax：入门指南

| 编号 | 节点类型 |
| --- | --- |
| 1 | 元素节点 |
| 2 | 属性节点 |
| 3 | 文本节点 |
| 4 | CDATA（XML 字符数据）节节点 |
| 5 | XML 实体引用节点 |
| 6 | XML 实体节点 |
| 7 | XML 处理指令节点 |
| 8 | XML 注释节点 |
| 9 | XML 文档节点 |
| 10 | XML DTD 节点 |
| 11 | XML 文档片段节点 |
| 12 | XML 记法节点 |

表 6-1 节点类型

| 属性 | 含义 |
| --- | --- |
| `attributes` | 该节点的属性 |
| `childNodes` | 子节点数组 |
| `documentElement` | 文档元素 |
| `firstChild` | 第一个子节点 |
| `lastChild` | 最后一个子节点 |
| `localName` | 节点的本地名称 |
| `name` | 节点的名称 |
| `nextSibling` | 下一个兄弟节点 |
| `nodeName` | 节点的名称 |
| `nodeType` | 节点类型 |
| `nodeValue` | 节点的值 |
| `previousSibling` | 前一个兄弟节点 |

表 6-2 可用于处理节点的 JavaScript 属性

## 6：在 Ajax 中处理 XML

### 获取文档元素

获取文档元素——即 XML 文档中包含所有其他元素的元素——通常是处理 XML 文档的第一步。我们现在来看一个名为 `documentElement.html` 的示例，了解如何提取文档元素。

`documentElement.html` 示例将读取我们的 `party.xml` 文档，并显示文档元素，即 `\boxed{<parties>}`。我们以一个按钮开始这个应用程序：

```html
<body>
    <h1>Getting the Document Element</h1>
    <form>
        <input type = "button" value = "Get the document element"
            onclick = "getDocumentElement()">
    </form>
</body>
```

当用户点击此按钮时，浏览器会调用一个名为 `getDocumentElement` 的 JavaScript 函数：

```html
<script language = "javascript">
    function getDocumentElement()
    {
        .
        .
        .
    }
</script>
```

好的，我们想在这里使用 Ajax 技术读取 `party.xml` 文档。我们首先创建一个新的 `XMLHttpRequest` 对象：

```html
<script language = "javascript">
    function getDocumentElement()
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new
                ActiveXObject("Microsoft.XMLHTTP");
        }
    }
</script>
```

如果创建该对象成功，我们配置 `XMLHttpRequestObject` 以使用 HTTP GET 方法访问 `party.xml` 文档：

```html
<script language = "javascript">

   function getDocumentElement()
   {
      var XMLHttpRequestObject = false;

      if (window.XMLHttpRequest) {
         XMLHttpRequestObject = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
         XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
      }

      if(XMLHttpRequestObject) {
         XMLHttpRequestObject.open("GET", "party.xml", true);
         .
         .
         .
      }
   }
</script>
```

然后我们添加匿名函数来下载 `party.xml`：

```html
<script language = "javascript">

   function getDocumentElement()
   {
      var XMLHttpRequestObject = false;

      if (window.XMLHttpRequest) {
         XMLHttpRequestObject = new XMLHttpRequest();
      } else if (window.ActiveXObject) {
         XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
      }

      if(XMLHttpRequestObject) {
         XMLHttpRequestObject.open("GET", "party.xml", true);

         XMLHttpRequestObject.onreadystatechange = function()
         {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                .
                .
                .
            }
         }
      }
   }
</script>
```

下载完成后，我们可以从 `XMLHttpRequest` 对象的 `responseXML` 属性获取 XML 作为 JavaScript XML 对象。然后我们可以使用该对象的 `documentElement` 属性来获取文档元素：

```html
<script language = "javascript">

function getDocumentElement()
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", "party.xml", true);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                var xmlDocument = XMLHttpRequestObject.responseXML;
                var documentElement = xmlDocument.documentElement;
                .
                .
                .
            }
        }
    }
}
</script>
```

现在我们有了文档元素，它存储为一个 JavaScript 元素对象。这一个对象包含了文档中的所有其他元素。我们如何确认我们得到的是文档元素 `<parties>` 呢？我们可以像这样打印它，使用 `documentElement` 对象的 `nodeName` 属性（注意我们将 `<` 写为 `&lt;`，这是你希望浏览器直接显示标记，而不是将其作为 HTML 处理的方式）：



```html
<script language = "javascript">

    function getDocumentElement()
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new
                ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {
            XMLHttpRequestObject.open("GET", "party.xml", true);

            XMLHttpRequestObject.onreadystatechange = function()
            {
                if (XMLHttpRequestObject.readyState == 4 &&
                    XMLHttpRequestObject.status == 200) {
                    var xmlDocument = XMLHttpRequestObject.responseXML;
                    var documentElement = xmlDocument.documentElement;
                    if(documentElement){
                        document.getElementById("targetDiv").innerHTML =
                            "The document element is &lt;" +
                            documentElement.nodeName + ">.";
                    }
                }
            }

            XMLHttpRequestObject.send(null);
        }
    }
</script>
```

就是这样——这是整个网页`documentElement.html`：

```html
<html>
    <head>
        <title>Getting the Document Element</title>

        <script language = "javascript">

            function getDocumentElement()
            {
                var XMLHttpRequestObject = false;

                if (window.XMLHttpRequest) {
                    XMLHttpRequestObject = new XMLHttpRequest();
                } else if (window.ActiveXObject) {
                    XMLHttpRequestObject = new
                        ActiveXObject("Microsoft.XMLHTTP");
                }

                if (XMLHttpRequestObject) {
                    XMLHttpRequestObject.open("GET", "party.xml", true);

                    XMLHttpRequestObject.onreadystatechange = function()
                    {
                        if (XMLHttpRequestObject.readyState == 4 &&
                            XMLHttpRequestObject.status == 200) {
                            var xmlDocument = XMLHttpRequestObject.responseXML;
                            var documentElement = xmlDocument.documentElement;
                            if (documentElement) {
                                document.getElementById("targetDiv").innerHTML =
                                    "The document element is &lt;" +
                                    documentElement.nodeName + ">.";
                            }
                        }
                    }

                    XMLHttpRequestObject.send(null);
                }
            }
        </script>

    </head>

    <body>

        <h1>Getting the Document Element</h1>

        <form>
            <input type = "button" value = "Get the document element"
                onclick = "getDocumentElement()">
        </form>

        <div id="targetDiv" width =100 height=100>
            The result will appear here.
        </div>

    </body>

</html>
```

你可以在图6-1中看到结果，应用程序已正确检索到`party.xml`的文档元素。

我们正在取得进展——我们已经提取并读取了 XML 文档的文档元素。那么如何访问 XML 文档中的任何元素呢？

### 动手试试：获取文档元素的子元素数量

想了解文档元素有多少个子元素吗？现在就修改`documentElement.html`来实现这一点。你可以使用`documentElement`对象的`childNodes`属性来完成。该属性包含一个数组，其中存储了文档元素的所有子节点，你可以通过数组的`length`属性来确定该数组的长度——从而得出文档节点的子节点数量：

```javascript
"The document element has " + documentElement.childNodes.length + " children.";
```

请注意，在我们的`party.xml`示例中，文档元素`<parties>`只有一个直接的子节点`<party>`，当你运行修改后的`documentElement.html`时，你应该会看到这一点。

## 访问任意 XML 元素

在通过 Ajax 下载`party.xml`之后，我们已经能够在 JavaScript 中访问`party.xml`的文档元素。但是，如果我们想访问`party.xml`中的其他元素呢？例如，如果我们想访问派对上的第三位客人，并获取他们的名（Ed）和姓（Norton）呢？

```xml
<?xml version="1.0"?>
<parties>
    <party type="winter">
        <party_title>Snow Day</party_title>
        <party_number>63</party_number>
        <subject>No school today!</subject>
        <date>2/2/2009</date>
        <people>
            <person attendance="present">
                <first_name>Ralph</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="absent">
                <first_name>Alice</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="present">
                <first_name>Ed</first_name>
                <last_name>Norton</last_name>
            </person>
        </people>
    </party>
</parties>
```

你能用 JavaScript 访问第三位客人吗？当然可以，我们将在一个新示例`party.html`中看看这是如何工作的。这个应用程序从一个按钮开始，当点击时，会调用一个名为`getData()`的函数：

```html
<body>
    <h1>Retrieving the Third Guest From party.xml</h1>
    <form>
        <input type="button" value="Get the third guest" onclick="getData()">
    </form>
    <div id="targetDiv" width=100 height=100>
        Who was the third guest?
    </div>
</body>
```

在`getData()`函数中，我们可以创建一个`XMLHttpRequest`对象：

```javascript
<script language = "javascript">
    function getData()
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
            XMLHttpRequestObject.overrideMimeType("text/xml");
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new
                ActiveXObject("Microsoft.XMLHTTP");
        }
    .
    .
    .
    }
</script>
```

然后我们可以使用该`XMLHttpRequest`对象通过 Ajax 下载`party.xml`，从`XMLHttpRequest`对象的`responseXML`属性获取 JavaScript XML 对象形式的`party.xml`，并将该 XML 对象传递给另一个名为`displayGuest()`的函数：

```javascript
<script language = "javascript">

    function getData()
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
            XMLHttpRequestObject.overrideMimeType("text/xml");
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new
                ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {
            XMLHttpRequestObject.open("GET", "party.xml", true);

            XMLHttpRequestObject.onreadystatechange = function()
            {
                if (XMLHttpRequestObject.readyState == 4 &&
                    XMLHttpRequestObject.status == 200) {
                    var xmlDocument = XMLHttpRequestObject.responseXML;
                    displayGuest(xmlDocument);
                }
            }
            XMLHttpRequestObject.send(null);
        }
    }
</script>
```

好的，现在我们将包含我们要处理的 XML 数据的 XML 对象传递给了一个名为`displayGuest()`的函数：

```javascript
<script language = "javascript">
function displayGuest (xmldoc)
{
.
.
}

</script>
```

我们通过获取`party.xml`的文档元素开始遍历 XML 文档以到达第三位客人：

```javascript
<script language = "javascript">
function displayGuest (xmldoc)
{
var partiesNode;

partiesNode = xmldoc.documentElement;
.
.
}

</script>
```

好了，现在我们已经获得了文档元素，我们如何导航到第三位客人呢？我们使用像这样的导航属性，这些属性被所有元素节点对象（包括文档元素节点）支持：

| 属性 | 描述 |
| :--- | :--- |
| `childNodes` | 子节点数组 |
| `firstChild` | 第一个子节点 |
| `lastChild` | 最后一个子节点 |
| `nextSibling` | 下一个兄弟节点 |
| `previousSibling` | 上一个兄弟节点 |

例如，`<party>`元素节点是`<parties>`节点的第一个（也是唯一的）子节点：

```xml
<?xml version="1.0"?>
<parties>
    <party type="winter">
        <party_title>Snow Day</party_title>
        <party_number>63</party_number>
        <subject>No school today!</subject>
        <date>2/2/2009</date>
        <people>
            <person attendance="present">
                <first_name>Ralph</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="absent">
                <first_name>Alice</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="present">
                <first_name>Ed</first_name>
                <last_name>Norton</last_name>
            </person>
        </people>
    </party>
</parties>
```

由于我们已经有了一个对应于`<parties>`文档元素节点的对象（`partiesNode`），我们可以在`displayGuest()`函数中这样访问`<party>`子节点：



```javascript
<script language = "javascript">
    function displayGuest (xmldoc)
    {
        var partiesNode, partyNode;

        partiesNode = xmldoc.documentElement;
        partyNode = partiesNode.firstChild;
        .
        .
        .
    }
</script>
```

第三位客人存储在 `<people>` 元素内，而 `<people>` 元素是 `<party>` 元素的最后一个子元素，因此我们可以使用 `<party>` 元素的 `lastChild` 属性来访问它：

```javascript
<script language = "javascript">
    function displayGuest (xmldoc)
    {
        var partiesNode, partyNode, peopleNode;
        var firstNameNode, lastNameNode, displayText;

        partiesNode = xmldoc.documentElement;
        partyNode = partiesNode.firstChild;
        peopleNode = partyNode.lastChild;
        .
        .
        .
    }
</script>
```

现在我们已经到达了 `<people>` 元素。我们感兴趣的 `<person>` 元素是 `<people>` 元素的最后一个子元素，因此我们可以这样访问第三个 `<person>` 节点：

```javascript
<script language = "javascript">
    function displayGuest (xmldoc)
    {
        var partiesNode, partyNode, peopleNode;
        var firstNameNode, lastNameNode, displayText;

        partiesNode = xmldoc.documentElement;
        partyNode = partiesNode.firstChild;
        peopleNode = partyNode.lastChild;
        personNode = peopleNode.lastChild;
        .
        .
        .
    }
</script>
```

快完成了。现在我们必须访问 `<person>` 元素内部的 `<first_name>` 和 `<last_name>` 元素。`<first_name>` 元素是 `<person>` 元素的第一个子元素，所以我们这样获取它：

```javascript
<script language = "javascript">
    function displayGuest (xmldoc)
    {
        var partiesNode, partyNode, peopleNode;
        var firstNameNode, lastNameNode, displayText;

        partiesNode = xmldoc.documentElement;
        partyNode = partiesNode.firstChild;
        peopleNode = partyNode.lastChild;
        personNode = peopleNode.lastChild;
        firstNameNode = personNode.firstChild;
        .
        .
        .
    }
</script>
```

`<last_name>` 元素是 `<person>` 元素的最后一个子元素，所以我们可以使用 `personNode` 对象的 `lastChild` 属性来访问它，但为了多样性，注意到 `<last_name>` 元素是 `<first_name>` 节点的兄弟节点（即，同一级别的元素），我们也可以使用 `<first_name>` 元素的 `nextSibling` 属性来访问 `<last_name>` 元素：

```javascript
<script language = "javascript">
    function displayGuest (xmldoc)
    {
        var partiesNode, partyNode, peopleNode;
        var firstNameNode, lastNameNode, displayText;

        partiesNode = xmldoc.documentElement;
        partyNode = partiesNode.firstChild;
        peopleNode = partyNode.lastChild;
        personNode = peopleNode.lastChild;
        firstNameNode = personNode.firstChild;
        lastNameNode = firstNameNode.nextSibling;
        .
        .
        .
    }
</script>
```

呼。现在我们有了两个对应于 `<first_name>` 和 `<last_name>` 元素的对象——`firstNameNode` 和 `lastNameNode`。虽然费了些劲才到达这里，但我们拿到了这些对象。

那么，你如何从 `<first_name>` 和 `<last_name>` 元素中提取客人的实际姓名呢？名和姓作为文本节点存储在这些元素内：

```xml
<person attendance="present">
    <first_name>Ed</first_name>
    <last_name>Norton</last_name>
</person>
```

你可以访问这些文本节点，因为它们是 `<first_name>` 和 `<last_name>` 元素的第一个子节点。因此，包含名和姓的文本节点分别是 `firstNameNode.firstChild` 和 `lastNameNode.firstChild`。

我们完成了吗？没有。文本节点本身只是对象——你不能在网页上显示它们。要实际访问文本节点中的文本，你必须使用文本节点的 `nodeValue` 属性。所以，最终，你可以通过 `firstNameNode.firstChild.nodeValue` 访问第三位客人的名，通过 `lastNameNode.firstChild.nodeValue` 访问他们的姓。代码如下所示：

```javascript
<script language = "javascript">

    function displayGuest (xmldoc)
    {
        var partiesNode, partyNode, peopleNode;
        var firstNameNode, lastNameNode, displayText;

        partiesNode = xmldoc.documentElement;
        partyNode = partiesNode.firstChild;
        peopleNode = partyNode.lastChild;
        personNode = peopleNode.lastChild;
        firstNameNode = personNode.firstChild;
        lastNameNode = firstNameNode.nextSibling;
        displayText = firstNameNode.firstChild.nodeValue + " " +
            lastNameNode.firstChild.nodeValue;
    }
</script>
```

## 第6章：在 Ajax 中处理 XML

### 205 Ajax：初学者指南

```javascript
partiesNode = xmlDoc.documentElement;
partyNode = partiesNode.firstChild;
peopleNode = partyNode.lastChild;
personNode = peopleNode.lastChild;
firstNameNode = personNode.firstChild;
lastNameNode = firstNameNode.nextSibling;

displayText = "The third guest was " +
    firstNameNode.firstChild.nodeValue + ' ' +
    lastNameNode.firstChild.nodeValue;

var target = document.getElementById("targetDiv");
target.innerHTML=displayText;
}
```

这是完整的应用程序 `party.html`：

```html
<html>
  <head>
    <title>从 party.xml 中检索第三位客人</title>
    <script language = "javascript">
      function getData()
      {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
          XMLHttpRequestObject = new XMLHttpRequest();
          XMLHttpRequestObject.overrideMimeType("text/xml");
        } else if (window.ActiveXObject) {
          XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {
          XMLHttpRequestObject.open("GET", "party.xml", true);

          XMLHttpRequestObject.onreadystatechange = function()
          {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
              var xmlDocument = XMLHttpRequestObject.responseXML;
              displayGuest(xmlDocument);
            }
          }

          XMLHttpRequestObject.send(null);
        }
      }

      function displayGuest(xmlDocument) {
        var partiesNode = xmlDocument.documentElement;
        var partyNode = partiesNode.firstChild;
        var peopleNode = partyNode.lastChild;
        var personNode = peopleNode.lastChild;
        var firstNameNode = personNode.firstChild;
        var lastNameNode = firstNameNode.nextSibling;

        var displayText = "The third guest was " +
            firstNameNode.firstChild.nodeValue + ' ' +
            lastNameNode.firstChild.nodeValue;

        var targetDiv = document.getElementById("targetDiv");
        targetDiv.innerHTML = displayText;
      }
    </script>
  </head>
  <body onload="getData()">
    <div id="targetDiv">Here's the third guest from party.xml:</div>
  </body>
</html>
```

### 206 Ajax：初学者指南

```javascript
XMLHttpRequestObject.send(null);
}
```

```javascript
function displayGuest (xmldoc) {
    var partiesNode, partyNode, peopleNode;
    var firstNameNode, lastNameNode, displayText;

    partiesNode = xmldoc.documentElement;
    partyNode = partiesNode.firstChild;
    peopleNode = partyNode.lastChild;
    personNode = peopleNode.lastChild;
    firstNameNode = personNode.firstChild;
    lastNameNode = firstNameNode.nextSibling;

    displayText = "The third guest was " +
        firstNameNode.firstChild.nodeValue + ' ' +
        lastNameNode.firstChild.nodeValue;

    var target = document.getElementById("targetDiv");
    target.innerHTML=displayText;
}
```

```html
<script>
```

```html
<head>
```

```html
<body>
```

# 从 party.xml 中检索第三位客人

```html
<form>
    <input type = "button" value = "Get the third guest"
           onclick = "getData()">
</form>
```

```html
<div id="targetDiv" width =100 height=100>
    Who was the third guest?
</div>
```

```html
</body>
```

```html
</html>
```

你可以在图6-2中看到这个应用程序运行，它正确地将埃德·诺顿识别为第三位客人。就是这样。

到目前为止一切顺利——除了有一个问题。如上所述的这个示例在 Internet Explorer 中可以工作，但在 Firefox 中不行。哪里出错了？

## 第6章：在 Ajax 中处理 XML

![图6-2 运行中的 party.html](img/2cd265cf0a64e9b4b91ab611753cd5d5_226_0.png)

### 查找第二位客人

想找到第二位客人的名字吗？你需要做的就是导航到该人员的 `<person>` 元素。你可以通过从最后一个 `<person>` 元素向前导航一个兄弟节点来实现，如下所示：

```javascript
function displayGuest (xmldoc)
{
  var partiesNode, partyNode, peopleNode;
  var firstNameNode, lastNameNode, displayText;

  partiesNode = xmldoc.documentElement;
  partyNode = partiesNode.firstChild;
  peopleNode = partyNode.lastChild;
  personNode = peopleNode.lastChild;
  personNode = personNode.previousSibling;
  firstNameNode = personNode.firstChild;
  lastNameNode = firstNameNode.nextSibling;

  displayText = "The second guest was " + 
    firstNameNode.firstChild.nodeValue + ' ' + 
    lastNameNode.firstChild.nodeValue;

  var target = document.getElementById("targetDiv");
  target.innerHTML=displayText;
}
```



尝试一下，并确认你确实得到了第二位客人的名字。然后尝试获取第一个人的名字。

### 在 Firefox 中处理空白符

说到空白符，Firefox 默认的行为与 Internet Explorer 不同。在 Firefox 中，用于缩进 XML 中元素的空白符会被视为文本节点。因此，在默认情况下，在 Firefox 中导航时，我们必须考虑所有的空白节点。例如，假设我们有一个对应于 `<parties>` 元素的对象，比如`partiesNode`：

```xml
<?xml version="1.0"?>
<parties>
    <party type="winter">
        <party_title>Snow Day</party_title>
        <party_number>63</party_number>
        <subject>No school today!</subject>
        <date>2/2/2009</date>
        <people>
            <person attendance="present">
                <first_name>Ralph</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="absent">
                <first_name>Alice</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="present">
                <first_name>Ed</first_name>
                <last_name>Norton</last_name>
            </person>
        </people>
    </party>
</parties>
```

如果我们想导航到 `<party>` 元素呢？你可能认为`partiesNode.firstChild`就能搞定，但在这里不行。表达式`partiesNode.firstChild`会将你带到`<parties>`元素节点的第一个子节点，而在 Firefox 中，那是用于缩进`<party>`元素的文本节点：

```xml
<?xml version="1.0"?>
<parties>
xxxx<party type="winter">
        <party_title>Snow Day</party_title>
        <party_number>63</party_number>
        .
        .
        .
```

所以，要到达`<party>`元素，你实际上需要到达文本节点的下一个兄弟节点。这意味着正确的 JavaScript 代码是`partyNode = partiesNode.firstChild.nextSibling`：

```xml
<?xml version="1.0"?>
<parties>
xxxx<party type="winter">
        <party_title>Snow Day</party_title>
        <party_number>63</party_number>
        .
        .
        .
```

同样，要到达`<party_title>`元素节点，你需要使用`partyNode.firstChild.nextSibling`来跳过缩进空白文本节点：

```xml
<?xml version="1.0"?>
<parties>
    <party type="winter">
        <party_title>Snow Day</party_title>
        <party_number>63</party_number>
        .
        .
        .
```

因此，你可以使用`nextSibling`和`previousSibling`属性来导航空白文本节点，但这很麻烦。以下是在考虑 Firefox 默认空白处理后，`displayGuest`函数变成的样子：

```javascript
function displayGuest(xmldoc)
{
    var partiesNode, partyNode, peopleNode;
    var personNode, firstNameNode, lastNameNode, displayText;

    partiesNode = xmlDoc.documentElement;
    partyNode = partiesNode.firstChild.nextSibling;
    peopleNode = partyNode.lastChild.previousSibling;
    personNode = peopleNode.firstChild.nextSibling
                  .nextSibling.nextSibling.nextSibling.nextSibling;
    firstNameNode = personNode.firstChild.nextSibling;
    lastNameNode = firstNameNode.nextSibling.nextSibling;

    displayText = "The third guest is: " +
                  firstNameNode.firstChild.nodeValue + ' ' +
                  + lastNameNode.firstChild.nodeValue;

    var target = document.getElementById("targetDiv");
    target.innerHTML=displayText;
}
```

这看起来一团糟——不得不从一个元素导航到另一个元素已经够糟糕了，但现在我们还得处理文本节点？难道没有更好的方法吗？

## 处理跨浏览器空白问题

确实有更好的方法——例如，你可以在 Firefox 处理它之前，先去除缩进空白。为此，我们可以编写一个名为`removeWhitespace`的 JavaScript 函数，它接收一个 JavaScript XML 文档对象作为参数：

```javascript
function removeWhitespace(xml)
{
    .
    .
    .
}
```

我们可以通过遍历所有子节点，为 XML 文档对象中的所有节点设置一个循环：

```javascript
function removeWhitespace(xml)
{
    var loopIndex;

    for (loopIndex = 0; loopIndex < xml.childNodes.length; loopIndex++) {
        .
        .
        .
    }
}
```

然后，我们通过`childNodes`属性获取循环中的当前节点，该属性保存着一个子节点数组：

```javascript
function removeWhitespace(xml)
{
    var loopIndex;

    for (loopIndex = 0; loopIndex < xml.childNodes.length; loopIndex++) {
        var currentNode = xml.childNodes[loopIndex];
        .
        .
        .
    }
}
```

如果当前节点是一个元素节点（我们可以通过检查其`nodeType`属性是否等于 1 来确认，参见表 6-1），它可能包含子节点——我们也必须去除这些子节点中的空白，因此我们再次将当前节点传递给`removeWhitespace`函数：

```javascript
function removeWhitespace(xml)
{
    var loopIndex;

    for (loopIndex = 0; loopIndex < xml.childNodes.length; loopIndex++) {

        var currentNode = xml.childNodes[loopIndex];

        if (currentNode.nodeType == 1) {
            removeWhitespace(currentNode);
        }
        .
        .
        .
    }
}
```

> **专家问答**
>
> **Q：** 在函数内部调用`removeWhitespace`函数是一种不寻常的做法吗？
>
> **A：** 在函数内部调用函数被称为递归，JavaScript 支持递归。这是一种合法的技术，而且，正如你所见，它也很强大。

在这个例子中，我们使用递归来遍历 XML 文档中的所有节点，无论该文档的结构如何。十五层嵌套的元素？没问题——`removeWhitespace`会通过在每个层级上操作并调用自身来处理当前节点的子节点，从而解决这个问题。

现在我们已经排除了元素节点，我们有了想要移除的缩进空白节点候选。我们如何检查它是否是可移除的空白？我们可以移除任何纯空白的文本节点——即只包含空格。那么我们如何检查当前节点是否是一个只包含空格的文本节点呢？

文本节点的`nodeType`属性值设置为 3，所以我们需要确认这一点。我们还可以使用正则表达式来检查文本节点是否包含全部空格。正则表达式允许你测试文本字符串的内容，JavaScript 通过字符串的`test`方法支持正则表达式。我们将测试的正则表达式是`^\s+$`。

翻译过来就是，要匹配成功，文本节点必须包含一个或多个空格（这是`\s+`部分）——并且从开头（这是`^`字符）到结尾（这是`$`字符）没有其他内容。

以下是测试纯空白节点的方法：

```javascript
function removeWhitespace(xml)
{
    var loopIndex;

    for (loopIndex = 0; loopIndex < xml.childNodes.length; loopIndex++) {

        var currentNode = xml.childNodes[loopIndex];

        if (currentNode.nodeType == 1) {
            removeWhitespace(currentNode);
        }

        if (((/^\s+$/.test(currentNode.nodeValue))) &&
            (currentNode.nodeType == 3)) {
            .
            .
            .
        }
    }
}
```

如果`if`语句的条件满足，你就知道你得到了一个纯空白的文本节点，它应该被移除。那么，到底该如何从 JavaScript 的 XML 文档中移除一个节点呢？你需要使用 XML 文档对象的`removeChild`方法。你只需要将想要移除的节点对象传递给该方法即可。这意味着你可以这样移除一个空白节点：

```javascript
function removeWhitespace(xml)
{
    var loopIndex;
```

## 正则表达式

正则表达式让你头晕目眩吗？你不需要为了学习本书、JavaScript 或 XML 而学习它们，但它们很有用。它们有自己独特的语法，掌握起来并不特别容易。你可以在`http://perldoc.perl.org/perlre.html`了解关于正则表达式以及如何用它们测试字符串的所有信息（你可以测试文本是否是电话号码、社会安全号码的格式，是否全部大写，或者成千上万种其他格式）。

## 第 6 章：在 Ajax 中处理 XML

```javascript
for (loopIndex = 0; loopIndex < xml.childNodes.length; loopIndex++) {

    var currentNode = xml.childNodes[loopIndex];

    if (currentNode.nodeType == 1) {
        removeWhitespace(currentNode);
    }

    if (((/^\s+$/.test(currentNode.nodeValue))) &&
        (currentNode.nodeType == 3)) {
        xml.removeChild(xml.childNodes[loopIndex--]);
    }
}
}
```

搞定，我们完成了。剩下的就是确保如果在 Firefox 中操作，就调用`removeWhitespace`，我们可以通过一个名为`firefoxFlag`的变量来检查。如果`firefoxFlag`设置为`true`，那么我们就是在 Firefox 中操作，这种情况下就调用`removeWhitespace`。以下是完成了这个功能的`party.html`的最终版本：

```html
<html>
  <head>
    <title>从party.xml中检索第三位客人</title>
    <script language = "javascript">
      function getData()
      {
        var firefoxFlag = false;
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
            XMLHttpRequestObject.overrideMimeType("text/xml");
            firefoxFlag = true;
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {
            XMLHttpRequestObject.open("GET", "party.xml", true);

            XMLHttpRequestObject.onreadystatechange = function()
            {
                if (XMLHttpRequestObject.readyState == 4 &&
XMLHttpRequestObject.status == 200) {
    var xmlDocument = XMLHttpRequestObject.responseXML;
    if(firefoxFlag){
        removeWhitespace(xmlDocument);
    }
    displayGuest(xmlDocument);
}
}

XMLHttpRequestObject.send(null);
}
}
```

```javascript
function displayGuest (xmldoc)
{
    var partiesNode, partyNode, peopleNode;
    var firstNameNode, lastNameNode, displayText;

    partiesNode = xmldoc.documentElement;
    partyNode = partiesNode.firstChild;
    peopleNode = partyNode.lastChild;
    personNode = peopleNode.lastChild;
    firstNameNode = personNode.firstChild;
    lastNameNode = firstNameNode.nextSibling;

    displayText = "第三位客人是 " +
        firstNameNode.firstChild.nodeValue + ' ' +
        lastNameNode.firstChild.nodeValue;

    var target = document.getElementById("targetDiv");
    target.innerHTML=displayText;
}
```



```javascript
function removeWhitespace(xml)
{
    var loopIndex;

    for (loopIndex = 0; loopIndex < xml.childNodes.length;
        loopIndex++) {

        var currentNode = xml.childNodes[loopIndex];

        if (currentNode.nodeType == 1) {
            removeWhitespace(currentNode);
        }

        if (((/^\s+$/.test(currentNode.nodeValue))) &&
            (currentNode.nodeType == 3)) {
xml.removeChild(xml.childNodes[loopIndex--]);
}
}
</script>
</head>
<body>
<h1>从party.xml中检索第三位客人</h1>
<form>
<input type = "button" value = "获取第三位客人"
onclick = "getData()">
</form>
<div id="targetDiv" width =100 height=100>
第三位客人是谁？
</div>
</body>
</html>
```

结果如图6-3所示（在Firefox中显示）——现在 `party.html` 既能在Firefox中工作，也能在Internet Explorer中工作。酷。

如你所见，使用像 `firstChild` 和 `lastChild` 这样的方法从一个元素导航到另一个元素是可行的，但这种方式很笨拙，并且你必须确切知道XML文档的结构。你的XML文档的结构稍有偏差，整个应用程序就会失败。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_234_0.png)

## 直接访问 XML 数据

您实际上可以通过使用 XML 文档对象的 `getElementsByTagName` 方法，在 XML 文档中仅搜索您需要的数据，该方法会返回一个 XML 元素节点的数组。

例如，要查找第三位宾客的名字和姓氏，您只需搜索所有的 `<first_name>` 和 `<last_name>` 元素，并从每个的第三个元素中提取必要的文本：

```xml
<?xml version="1.0"?>
<parties>
    <party type="winter">
        <party_title>Snow Day</party_title>
        <party_number>63</party_number>
        <subject>No school today!</subject>
        <date>2/2/2009</date>
        <people>
            <person attendance="present">
                <first_name>Ralph</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="absent">
                <first_name>Alice</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="present">
                <first_name>Ed</first_name>
                <last_name>Norton</last_name>
            </person>
        </people>
    </party>
</parties>
```

我们可以在一个基于先前示例 `party.html` 的新 Ajax 应用程序 `party2.html` 中执行此搜索。不过在这里，我们只需简单修改 `displayGuest` 函数来搜索 `<first_name>` 和 `<last_name>` 元素：

```javascript
function displayGuest (xmldoc)
{
    firstnamenodes = xmldoc.getElementsByTagName("first_name");
    lastnamenodes = xmldoc.getElementsByTagName("last_name");
    .
    .
    .
}
```

## 第 6 章：在 Ajax 中处理 XML 217

我们得到 `<first_name>` 和 `<last_name>` 元素的数组后，可以使用每个数组中的第三个元素（数组索引为 2，因为数组索引从 0 开始）来定位我们要查找的名字。它看起来是这样的（在 `party2.html` 中）：

```html
<html>
  <head>
    <title>Accessing XML Data Directly</title>

    <script language = "javascript">
      function getData()
      {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
          XMLHttpRequestObject = new XMLHttpRequest();
          XMLHttpRequestObject.overrideMimeType("text/xml");
        } else if (window.ActiveXObject) {
          XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {
          XMLHttpRequestObject.open("GET", "party.xml", true);

          XMLHttpRequestObject.onreadystatechange = function()
          {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
              var xmlDocument = XMLHttpRequestObject.responseXML;
              displayGuest(xmlDocument);
            }
          }

          XMLHttpRequestObject.send(null);
        }
      }

      function displayGuest (xmldoc)
      {
        firstnamenodes = xmldoc.getElementsByTagName("first_name");
        lastnamenodes = xmldoc.getElementsByTagName("last_name");

        var displayText = "The third guest was: " +
          firstnamenodes[2].firstChild.nodeValue + ' '
          + lastnamenodes[2].firstChild.nodeValue;

        var target = document.getElementById("targetDiv");
        target.innerHTML=displayText;
      }

    </script>

  </head>

  <body>

    <h1>Accessing XML Data Directly</h1>

    <form>
      <input type = "button" value = "Get the third guest"
             onclick = "getData()">
    </form>

    <div id="targetDiv" width =100 height=100>
      Who was the third guest?
    </div>

  </body>

</html>
```

您可以在图 6-4 中看到结果，其中 `party2.html` 已正确识别出第三位宾客。这很简单——毫不费力。

好的，我们已经能够从 XML 元素中提取数据，那么 XML 属性呢？例如，如果您想读取派对上第三位宾客的 `attendance` 属性值，以查看他们是出席还是缺席，该怎么办？

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_237_0.png)

```xml
<?xml version="1.0"?>
<parties>
    <party type="winter">
        <party_title>Snow Day</party_title>
        <party_number>63</party_number>
        <subject>No school today!</subject>
        <date>2/2/2009</date>
        <people>
            <person attendance="present">
                <first_name>Ralph</first_name>
                <last_name>Kramden</last_name>
                <person attendance="absent">
                </person>
                <first_name>Alice</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="present">
                <first_name>Ed</first_name>
                <last_name>Norton</last_name>
            </person>
        </people>
    </party>
</parties>
```

您可以通过元素节点的 `attributes` 属性获取一个元素属性的数组，这在新的示例 `attributes.html` 中看起来像这样：

```javascript
function displayGuest (xmldoc)
{
    var partiesNode, partyNode, peopleNode;
    var firstNameNode, lastNameNode, displayText;

    partiesNode = xmldoc.documentElement;
    partyNode = partiesNode.firstChild;
    peopleNode = partyNode.lastChild;
    personNode = peopleNode.lastChild;
    firstNameNode = personNode.firstChild;
    lastNameNode = firstNameNode.nextSibling;
    attributes = personNode.attributes
    .
    .
    .
}
```

实际上，`attributes` 变量并不保存一个数组——严格来说，它是一个命名节点映射。这很有用，因为命名节点映射对象支持一个名为 `getNamedItem` 的方法，您可以将要获取的属性的名称传递给它。`getNamedItem` 方法将返回对应于该属性的对象，您可以通过该对象的 `nodeValue` 属性恢复属性的值。

## 220 Ajax：初学者指南

换句话说，读取属性很容易；以下是我们读取第三位宾客的 `attendance` 属性的方法（在 `attributes.html` 中）：

```html
<html>
  <head>
    <title>Accessing Data in XML Attributes</title>
    <script language = "javascript">
      function getData()
      {
        var mozillaFlag = false;
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
          XMLHttpRequestObject = new XMLHttpRequest();
          XMLHttpRequestObject.overrideMimeType("text/xml");
          mozillaFlag = true;
        } else if (window.ActiveXObject) {
          XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {
          XMLHttpRequestObject.open("GET", "party.xml", true);

          XMLHttpRequestObject.onreadystatechange = function()
          {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
              var xmlDocument = XMLHttpRequestObject.responseXML;
              if(mozillaFlag){
                removeWhitespace(xmlDocument);
              }
              displayGuest (xmlDocument);
            }
          }

          XMLHttpRequestObject.send(null);
        }
      }
    </script>
  </head>
  <body>
    <script>getData();</script>
  </body>
</html>
```

## 第 6 章：在 Ajax 中处理 XML 221



```javascript
firstNameNode = personNode.firstChild;
lastNameNode = firstNameNode.nextSibling;
attributes = personNode.attributes
attendancePerson = attributes.getNamedItem("attendance");

var displayText = firstNameNode.firstChild.nodeValue
+ ' ' + lastNameNode.firstChild.nodeValue
+ " was " + attendancePerson.nodeValue;

var target = document.getElementById("targetDiv");
target.innerHTML=displayText;
}

function removeWhitespace(xml)
{
var loopIndex;

for (loopIndex = 0; loopIndex < xml.childNodes.length;
loopIndex++) {

var currentNode = xml.childNodes[loopIndex];

if (currentNode.nodeType == 1) {
removeWhitespace(currentNode);
}

if (((/^\s+$/.test(currentNode.nodeValue)) &&
(currentNode.nodeType == 3))) {
xml.removeChild(xml.childNodes[loopIndex--]);
}
}
}
</script>

</head>

<body>

<h1>Accessing Data in XML Attributes</h1>

<form>
<input type = "button" value = "Get the third guest's attendance"
onclick = "getData()">
</form>

<div id="targetDiv" width =100 height=100>
Was the third guest present?
</div>

</body>

</html>
```

## Ajax：入门指南

![图 6-5 读取XML属性值](img/2cd265cf0a64e9b4b91ab611753cd5d5_241_0.png)

图 6-5 读取XML属性值

你可以在图 6-5 中看到`attributes.html`的运行效果，它报告了第三位客人，Ed Norton，到场了。非常好。

## 验证你的XML

本章最后一个XML主题是如何验证你的XML。如本章前面所述，你可以指定XML文档的语法并测试它是否遵守你的规则。指定XML文档语法有两种方法：使用XML Schema和DTD。不幸的是，浏览器对Schema的支持摇摇欲坠，甚至可以说是不存在的——即使Internet Explorer对Schema的支持也非常不稳定。因此，在这个例子中，我们将坚持使用较老的指定XML语法的方式，即DTD。

我们之前已经在本章中看过了`party.xml`的DTD是什么样子，我们将包含`party.xml`的DTD的文档称为`partydtd.xml`：

```xml
<?xml version="1.0"?>
<!DOCTYPE parties [
<!ELEMENT parties (party*)>
<!ELEMENT party (party_title, party_number, subject, date, people*)>
<!ELEMENT party_title (#PCDATA)>
<!ELEMENT party_number (#PCDATA)>
<!ELEMENT subject (#PCDATA)>
<!ELEMENT date (#PCDATA)>
<!ELEMENT first_name (#PCDATA)>
<!ELEMENT last_name (#PCDATA)>
<!ELEMENT people (person*)>
<!ELEMENT person (first_name,last_name)>
<!ATTLIST party
    type CDATA #IMPLIED>
<!ATTLIST person
    attendance CDATA #IMPLIED>
]>
```

```xml
<parties>
    <party type="winter">
        <party_title>Snow Day</party_title>
        <party_number>63</party_number>
        <subject>No school today!</subject>
        <data>2/2/2009</data>
        <people>
            <person attendance="present">
                <first_name>Ralph</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="absent">
                <first_name>Alice</first_name>
                <last_name>Kramden</last_name>
            </person>
            <person attendance="present">
                <first_name>Ed</first_name>
                <last_name>Norton</last_name>
            </person>
        </people>
    </party>
</parties>
```

请注意这里有一个错误——该文档使用了一个`<data>`元素，而不是`<date>`元素，你可以在Internet Explorer等浏览器中捕捉到这个错误。要检查文档的有效性，你可以在Internet Explorer中创建一个MSXML2.DOMDocument类型的XML解析器对象，我们是在`getData`函数中这样做的：

```javascript
function getData()
{
    var XMLHTTPRequestObject = false;

    XMLHTTPRequestObject = new
        ActiveXObject("Microsoft.XMLHTTP");

    if (XMLHTTPRequestObject) {
        XMLHTTPRequestObject.open("GET", "partydtd.xml?b=5", true);

        XMLHTTPRequestObject.onreadystatechange = function()
        {
            if (XMLHTTPRequestObject.readyState == 4 &&
                XMLHTTPRequestObject.status == 200) {
                var xmlDocument = XMLHTTPRequestObject.responseXML;

                var parser = new ActiveXObject("MSXML2.DOMDocument");
                parser.validateOnParse = true;
                .
                .
                .
            }
        }
    }
```

请注意，你还必须将解析器对象的`validateOnParse`属性设置为`true`，以使其实际解析XML。现在你可以使用解析器的`load`方法，像这样将下载的XML传递给它：

```javascript
function getData()
{
    var XMLHttpRequestObject = false;

    XMLHttpRequestObject = new
        ActiveXObject("Microsoft.XMLHTTP");

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", "partydtd.xml?b=5", true);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                var xmlDocument = XMLHttpRequestObject.responseXML;

                var parser = new ActiveXObject("MSXML2.DOMDocument");
                parser.validateOnParse = true;
                parser.load(XMLHttpRequestObject.responseXML);
                .
                .
                .
        }
    }
```

如果解析器发现错误，`parser.parseError.errorCode`属性将为非零值，你可以在一个新示例（`validation.html`）中像这样报告错误：

```html
<html>
    <head>

        <title>Validating an XML Document</title>

        <script language = "javascript">

            function getData()
            {
                var XMLHttpRequestObject = false;

                XMLHttpRequestObject = new
                    ActiveXObject("Microsoft.XMLHTTP");

                if(XMLHttpRequestObject) {
                    XMLHttpRequestObject.open("GET", "partydtd.xml?b=5", true);

                    XMLHttpRequestObject.onreadystatechange = function()
                    {
                        if (XMLHttpRequestObject.readyState == 4 &&
                            XMLHttpRequestObject.status == 200) {
                            var xmlDocument = XMLHttpRequestObject.responseXML;
```

```javascript
var parser = new ActiveXObject("MSXML2.DOMDocument");
parser.validateOnParse = true;
parser.load(XMLHttpRequestObject.responseXML);
var target = document.getElementById("targetDiv");

if (parser.parseError.errorCode != 0) {
    target.innerText = "Error in " +
        parser.parseError.url +
        " line " + parser.parseError.line +
        " position " + parser.parseError.linepos +
        ".\nError source: " + parser.parseError.srcText +
        "\n" + parser.parseError.reason +
        "\n" + "Error: " +
        parser.parseError.errorCode;
}
else {
    displayGuest(xmlDocument);
    }
}
}

XMLHttpRequestObject.send(null);
}
}

function displayGuest(xmldoc)
{
    var partiesNode, partyNode, peopleNode;
    var firstNameNode, lastNameNode, displayText;

    partiesNode = xmldoc.documentElement;
    partyNode = partiesNode.firstChild;
    peopleNode = partyNode.lastChild;
    personNode = peopleNode.lastChild;
    firstNameNode = personNode.firstChild;
    lastNameNode = firstNameNode.nextSibling;

    displayText = "The third guest was " +
        firstNameNode.firstChild.nodeValue + ' ' +
        lastNameNode.firstChild.nodeValue;

    var target = document.getElementById("targetDiv");
    target.innerHTML=displayText;
}

</script>

</head>

<body>
```

```html
<h1>Validating an XML Document</h1>

<form>
    <input type="button" value="Get the third guest" onclick="getData()">
</form>

<div id="targetDiv" width=100 height=100>
    Your data will appear here.
</div>

</body>

</html>
```

你可以看到`partydtd.xml`未能通过验证过程，因为解析器在期望一个`<date>`元素时找到了一个`<data>`元素，如图 6-6 所示。

你现在在Ajax中使用XML方面有了一个良好的基础。

![图 6-6 验证XML文档](img/2cd265cf0a64e9b4b91ab611753cd5d5_245_0.png)

图 6-6 验证XML文档

# 第7章：在Ajax中使用层叠样式表

## 核心技能与概念

- 使用CSS让文本引人注目
- 使用CSS设置字体样式
- 使用CSS设置颜色样式
- 使用CSS设置绝对定位
- 创建一个功能完整的Ajax启用CSS驱动的菜单系统

正如你在前面章节中已经看到的，使用Ajax的主要原因是它允许网页在不需要刷新页面的情况下进行更新，这使得页面更新对用户来说相当无缝。使用这项技术时，一个重要的考虑因素是你如何呈现从服务器下载的数据。到目前为止，你只是通过覆盖一个`<div>`元素来呈现下载的数据。正如本章将解释的，你在呈现这些新数据时拥有更多的选择，使你能够吸引读者的注意力到变化上。

因为呈现下载数据的方式是Ajax应用程序的重要组成部分，这就是本章的主题。例如，在专业Ajax开发者中，一个经常被问到的问题是，当下载内容出现在页面中时，用户会注意到吗？在呈现数据表的页面中，当你只更新一两个项目时，这可能成为一个问题。正如你将看到的，处理这个问题的一种方法是以颜色闪烁的方式显示下载的文本。

你还将看到，你不必在简单的`<div>`元素中显示下载的文本。你可以将此类数据显示在页面的任何位置，正如你将在创建弹出菜单系统时看到的，该菜单系统使用通过Ajax交互下载的文本，允许菜单项实时更新。

在本章中，使用Ajax下载的数据更新页面将通过使用层叠样式表（CSS）来实现。熟悉CSS对于Ajax开发者至关重要，你将在本章中获得对该主题的良好介绍。CSS是最重要的Ajax主题之一，因为在Ajax中更新网页如此重要。

CSS是用于安排和设置网页中项目的样式的正式规范。你可以使用CSS设置数据的字体、颜色、外观、可见性和位置。你将在本章中获得良好的CSS基础，但关于CSS的完整、详细的细节，请参阅`www.w3.org/TR/CSS21/`上的CSS规范。

## 吸引用户注意下载的文本

Ajax应用程序的主要问题之一也是它的主要优势——下载数据时没有页面刷新。这很棒，但也可能意味着用户会错过数据更新，尤其是在内容很多的页面中。

## 第7章：在Ajax中使用层叠样式表 231



解决这个问题有多种方法，但最简单的解决方案就是让新显示的数据以某种方式脱颖而出。例如，你可以放大新显示的文本，或者暂时改变其颜色。本节将展示一个示例`attentionGetter.html`，它在数据下载后将文本显示为红色半秒钟。之后，新下载的文本将恢复为黑色。在 Ajax 应用程序中，让新下载的数据以这种方式闪烁是吸引用户注意的好方法。

我们可以通过结合使用 CSS 和 JavaScript 来创建这个示例。我们从`attentionGetter.html`开始，其中包含一个按钮，点击后会调用一个名为`getData`的函数，该函数会下载一个名为`message.txt`的文件，并将其内容显示在 ID 为`targetDiv`的`<div>`元素中：

```html
<body>

<H1>获取用户注意力</H1>

<form>
    <input type = "button" value = "获取文本"
           onclick = "getData('message.txt', 'targetDiv')">
</form>

<div id="targetDiv">
    <p>获取的数据将显示在这里。</p>
</div>

</body>
```

在`getData`函数中，我们创建一个`XMLHttpRequest`对象：

```javascript
<script language = "javascript">
    function getData(dataSource, divID)
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new
                ActiveXObject("Microsoft.XMLHTTP");
        }
        .
        .
        .
    }
```

如果我们成功创建了`XMLHttpRequest`对象，我们打开它，并将其配置为使用 GET 方法：

```javascript
<script language = "javascript">
  function getData(dataSource, divID)
  {
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
      XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
      XMLHttpRequestObject = new
        ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
      XMLHttpRequestObject.open("GET", dataSource);
      .
      .
      .
    }
  }
```

然后我们设置一个匿名 JavaScript 函数来处理下载，如下所示：

```javascript
<script language = "javascript">
  function getData(dataSource, divID)
  {
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
      XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
      XMLHttpRequestObject = new
        ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
      XMLHttpRequestObject.open("GET", dataSource);

      XMLHttpRequestObject.onreadystatechange = function()
      {
        if (XMLHttpRequestObject.readyState == 4 &&
          XMLHttpRequestObject.status == 200) {
          .
          .
          .
        }
      }
    }
  }
```

当文本下载完成后，我们希望最初将其显示为红色。你可以通过使用`<div>`元素内置`style`对象的`color`属性来设置`<div>`元素的样式，使其文本显示为红色。`style`对象允许你通过 JavaScript 访问可见元素的 CSS 样式。

你在 CSS 中通过设置 CSS 属性来设置项目样式。以下是与颜色相关的属性：

- `color`设置前景色。你将其设置为 HTML 颜色值（如`#FFFFFF`）。
- `background-color`设置背景色。同样，你将其设置为 HTML 颜色值。

你使用 HTML 颜色值来设置颜色——就像在网页中一样——格式为`rrggbb`，其中`rr`是红色分量的十六进制值（从 00 到 FF），`gg`是绿色分量，`bb`是蓝色分量。（这是必须了解的基本 HTML 知识。如果你不熟悉如何在 HTML 中设置颜色，请在线搜索“HTML color values”。）

因此，例如，要将 ID 为`targetDiv`的`<div>`元素的文本颜色设置为红色（在 HTML 中表示为`"#FF0000"`），你可以在我们的示例`attentionGetter.html`中这样做：

```javascript
<script language = "javascript">
    function getData(dataSource, divID)
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new
                ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {
            var obj = document.getElementById("targetDiv");
            XMLHttpRequestObject.open("GET", dataSource);

            XMLHttpRequestObject.onreadystatechange = function()
            {
                if (XMLHttpRequestObject.readyState == 4 &&
                    XMLHttpRequestObject.status == 200) {
                    obj.style.color = "#FF0000";
                    .
                    .
                    .
                }
            }
        }
    }
}
```

# 232 Ajax：入门指南

这就是你如何在网页中访问可见元素的 CSS 样式属性的方法——例如`obj.style.color`。如果 CSS 样式属性名称中带有连字符，比如`background-color`，该怎么办呢？JavaScript 变量名中不允许使用连字符，因此约定是将连字符后的字母大写，然后移除连字符。所以，例如，如果你想将`<div>`元素的背景色设置为红色，该怎么做呢？你可以这样做：`obj.style.backgroundColor = "#FF0000"`。

很好，这让你能够使用 JavaScript 通过 CSS 设置 HTML 元素的前景色和背景色。以下是我们如何完成`getData`函数，将下载的文本显示为红色：

```javascript
<script language = "javascript">
  function getData(dataSource, divID)
  {
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
      XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
      XMLHttpRequestObject = new
        ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
      var obj = document.getElementById("targetDiv");
      XMLHttpRequestObject.open("GET", dataSource);

      XMLHttpRequestObject.onreadystatechange = function()
      {
        if (XMLHttpRequestObject.readyState == 4 &&
          XMLHttpRequestObject.status == 200) {
            obj.style.color = "#FF0000";
            obj.innerHTML = XMLHttpRequestObject.responseText;
        }
      }

      XMLHttpRequestObject.send(null);
    }
  }
```

这会将下载的文本显示为红色，但我们只希望下载的文本闪烁红色半秒钟，然后恢复为黑色。那么，我们到底该怎么做呢？

这就是 JavaScript 派上用场的地方。我们可以使用 JavaScript 的`setTimeout`函数，将另一个函数的名称和我们希望 JavaScript 在调用该函数前经过的时间量（以毫秒为单位——即千分之一秒）传递给 JavaScript。因此，我们可以设置 JavaScript 调用另一个名为`attentionGetter`的函数，该函数会在半秒钟（即 500 毫秒）后将文本颜色改回黑色，如下所示：

## 第 7 章：在 Ajax 中使用层叠样式表 233

```javascript
<script language = "javascript">
function getData(dataSource, divID)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        var obj = document.getElementById("targetDiv");
        XMLHttpRequestObject.open("GET", dataSource);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                obj.style.color = "#FF0000";
                obj.innerHTML = XMLHttpRequestObject.responseText;
                setTimeout(attentionGetter, 500);
            }
        }

        XMLHttpRequestObject.send(null);
    }
}
</script>
```

在`attentionGetter`函数中，我们只需将文本颜色设置回黑色（HTML 颜色值`"#000000"`）：

```javascript
<script language = "javascript">
function getData(dataSource, divID)
{
    .
    .
    .
}

function attentionGetter()
{
    var target = document.getElementById("targetDiv");
    target.style.color = "#000000";
}
</script>
```

## 使用 CSS 设置文本样式

除了让新下载的文本在网页中以彩色闪烁显示外，您还可以选择其他 CSS 效果来吸引用户对该文本的注意力。例如，您可以临时将其放大、加粗显示、添加下划线或使用其他文本样式。

### Ajax：初学者指南

| 属性 | 描述 |
| :--- | :--- |
| `font-family` | 指定实际的字体，如 Arial 或 Helvetica。如果您想在目标计算机缺少首选字体的情况下列出备选字体，请将它们指定为逗号分隔的列表，例如`{font-family: Arial, Helvetica}`。 |
| `font-style` | 指定文本的渲染方式。可设置为`normal`、`italic`或`oblique`。 |
| `font-weight` | 指用于渲染文本的字形相对于同一字体族中其他字体的粗细或轻重。可设置为`normal`、`bold`、`bolder`、`lighter`、`100`、`200`、`300`、`400`、`500`、`600`、`700`、`800`或`900`。 |
| `line-height` | 表示赋予每一行的高度。 |
| `font-size` | 指字体的大小。 |
| `text-decoration` | 为文本添加下划线。可设置为`none`、`underline`、`overline`、`line-through`或`blink`。 |
| `text-align` | 居中文本。可设置为`left`、`right`或`center`。 |

## 表 7-1 CSS 样式属性

CSS 有许多不同的文本样式，可用于使新下载的文本脱颖而出。表 7-1 列出并描述了最受欢迎的样式属性。下面是一个示例`textStyles.html`，展示了如何运用这些文本属性。此示例为网页的`<body>`元素设置了样式（您已经见过如何在 JavaScript 中通过 ID 为单个元素（如`<div>`元素）设置样式）。除了 JavaScript，您还可以在`<style>`元素中设置样式，该元素通常放在网页的`<head>`元素中：

```html
<html>
    <head>
        <title>
            Styling text with CSS
        </title>

        <style type="text/css">
            .
            .
            .
        </style>
    </head>
    .
    .
    .
</html>
```

## 第 7 章：在 Ajax 中使用层叠样式表 237

您通过样式规则在此处为网页元素设置样式，样式规则是由分号分隔的样式属性和样式值对的集合。例如，下面是为`<body>`元素设置样式规则的方式，设置各种样式属性：

```html
<html>
    <head>
        <title>
            Styling text with CSS
        </title>
        <style type="text/css">
            body {font-style: italic; font-weight: bold;
            font-size: 16pt; line-height: 12pt; font-family: arial,
            helvetica; text-align: center}
        </style>
    </head>
    .
    .
    .
</html>
```

这将`<body>`元素的`font-style`属性设置为`italic`，`font-weight`样式属性设置为`bold`，以此类推。现在我们可以向`<body>`元素添加一些文本：



```html
<html>
    <head>
        <title>
            Styling text with CSS
        </title>
        <style type="text/css">
            body {font-style: italic; font-weight:
            bold; font-size: 16pt; line-height: 12pt; font-family:
            arial, helvetica; text-align: center}
        </style>
    </head>

    <body>
        <br>
        <h1>Styling text with CSS</h1>
        <br>
        This page displays text styled with CSS.
        .
        .
        .
    </body>
</html>
```

### Ajax：初学者指南

**图 7-2** 设置 `<body>` 元素的样式

您可以在图 7-2 中看到结果。现在让我们添加一个按钮，当点击时，它将为文本添加下划线。要为文本添加下划线，您需要使用 `text-decoration` 样式属性，并将其设置为 `"underline"`。在 JavaScript 中，该属性变为 `textDecoration` 属性，因此我们可以让按钮这样执行操作（在 `textStyles.html` 中）：

```html
<html>
    <head>
        <title>
            Styling text with CSS
        </title>
        <style type="text/css">
            body {font-style: italic; font-weight: bold; font-size:
                16pt; line-height: 12pt; font-family: arial, helvetica;
                text-align: center}
        </style>
    </head>

    <body>
        <br>
        <h1>Styling text with CSS</h1>
        <br>
        This page displays text styled with CSS.

        <form>
            <input type = "button" value = "Underline the text"
                onclick = "body.style.textDecoration = 'underline'">
        </form>

    </body>
</html>
```

## 第 7 章：在 Ajax 中使用层叠样式表

图 7-3 为 `<body>` 元素中的文本添加下划线。

您可以在图 7-3 中看到这个新按钮的效果。以下是此示例中的 CSS 样式属性及其值：

- `font-style`: `italic`
- `font-weight`: `bold`
- `font-size`: `16pt`
- `line-height`: `12pt`
- `text-decoration`: `underline`
- `font-family`: `arial, helvetica`
- `text-align`: `center`

如果您有多个相同类型的 HTML 元素（例如 `<div>` 或 `<p>` 元素），并且想为它们设置不同的样式，该怎么办？在这种情况下，您可以为它们分配不同的 ID 值，并使用以井号（`#`）开头的 ID 值为每个元素创建样式规则。例如，如果有一个 ID 为 `targetDiv` 的 `<div>` 元素，您可以这样设置其样式，使其在 `textStyles.html` 的 `<style>` 元素中使用 36 点字体：

```html
<html>
    <head>
        <title>
            Styling text with CSS
        </title>
        <style type="text/css">
            body {font-style: italic; font-weight: bold; font-size: 16pt; line-height: 12pt; font-family: arial, helvetica; text-align: center}
            #targetDiv {font-size: 36pt}
        </style>
```

图 7-4 设置 `<div>` 元素的样式。

```html
</style>
</head>

<body>
    <br>
    <h1>Styling text with CSS</h1>
    <br>
    This page displays text styled with CSS.

    <form>
        <input type = "button" value = "Underline the text"
        onclick = "body.style.textDecoration = 'underline'">
    </form>

    <div id="targetDiv">Here is more text</div>
</body>
</html>
```

您可以在图 7-4 中看到这个页面新版本的效果。

## 动手试一试：更改文本大小

尝试在用户点击按钮时，将 `textStyles.html` 页面中的文本大小更改为 48 点字体。下面是操作方法：

```html
<html>
    <head>
        <title>
            Styling text with CSS
```

除了为文本设置样式，你还可以在支持 Ajax 的页面中为颜色和背景设置样式。

## 使用 CSS 设置颜色和背景样式

有多个 CSS 属性可用于设置颜色和背景。表 7-2 列出并描述了最常用的颜色和背景属性。

| 属性 | 描述 |
|---|---|
| `color` | 设置前景色。设置为 HTML 颜色值（如 `#FFFFFF`）。 |
| `background-color` | 设置背景色。设置为 HTML 颜色值。 |
| `background-image` | 设置背景图像。设置为一个 URL。 |
| `background-repeat` | 指定背景图像是否平铺。可设置为 `repeat`、`repeat-x`、`repeat-y` 或 `no-repeat`。 |
| `background-attachment` | 指定背景是否随文档其余部分一起滚动。可设置为 `scroll` 或 `fixed`。 |
| `background-position` | 设置背景的初始位置。可设置为 `top`、`center`、`bottom`、`left` 或 `right`。 |

表 7-2 CSS 颜色和背景属性。

下面是一个名为 `letter.html` 的示例，它设置了商务信函的颜色和背景色：

```html
<html>
    <head>
        <title>
            Styling Foregrounds and Backgrounds
        </title>
    </head>

    <body style="background-color: #EEDDDD">

        <div align="left">
            Chief Web Designer
            <br>
            Pretty Pleasing Web Designs, Inc.
            <br>
            Los Angeles
        </div>

        <p>
            Dear you:
            <br>
            <br>
            <div align="center"
                 style="color: #FF0000; background-color: #55FF55;
                         font-weight: bold; font-size: 16pt">
                <br>
                What do you think of this style?
                <br>
                <br>
            </div>

            <div align="right">
                <br>
                <p>
                    Chief Stylist
                    <br>
                    Dynamo CSS Stylers, Inc.
                    <br>
                    London
                </p>
            </div>

    </body>
</html>
```

## 第 7 章：在 Ajax 中使用层叠样式表

你还可以添加一个按钮，点击该按钮可以改变信函中间 `<div>` 元素的背景色。你已经知道可以像 `body.style.backgroundColor` 这样引用像 `<body>` 元素这样的元素——但如何引用一个特定的 `<div>` 元素呢？你可以使用 `getElementById` 方法获取与该 `<div>` 元素对应的对象，就像我们在本章开头所做的那样，但还有另一种方法。

你可以为 `<div>` 元素赋予一个 ID 值，然后在 JavaScript 中只需使用该 ID 值就能引用该元素——无需调用 `getElementById` 方法。例如，如果你给 `<div>` 元素赋予 ID `div1`，你就可以像这样引用它的背景色：`div1.style.backgroundColor`。

下面是我们如何在用户点击按钮时将 `<div>` 元素的背景色更改为白色：

```html
<html>
    <head>
        <title>
            Styling Foregrounds and Backgrounds
        </title>
    </head>

    <body style="background-color: #EEDDDD">

        <div align="left">
            Chief Web Designer
            <br>
            <br>
            Pretty Pleasing Web Designs, Inc.
            <br>
            Los Angeles
        </div>

        <p>
            Dear you:
            <br>
            <br>
            <div align="center" id="div1"
                style="color: #FF0000; background-color: #55FF55;
                font-weight: bold; font-size: 16pt">
                <br>
                    What do you think of this style?
                <br>
                <br>
            </div>

            <div align="right">
                <br>
                <p>
                    Chief Stylist
                    <br>
                    Dynamo CSS Stylers, Inc.
                    <br>
                    London
                </div>
                <center>
                  <form>
                    <input type = "button" value = "Change background color"
                           onclick = "div1.style.backgroundColor = '#FFFFFF'">
                  </form>
                </center>
    </body>
</html>
```

这在 Ajax 应用中非常有用，当仅仅让文本闪烁还不够时——你想通过改变元素的背景色来突出你在网页上所做的更改（在处理 HTML 表格中的单元格时尤其有用）。

你可以在图 7-5 中看到这个示例的实际效果，点击按钮将中间的 `<div>` 元素颜色更改为白色。效果很好。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_263_0.png)

## 尝试：使用预定义颜色

除了允许你使用颜色值（如 `#FFCCEE`）来设置颜色外，现代浏览器还支持数十种预定义的颜色名称，如 `"green"`、`"red"`、`"ivory"`、`"sand"`、`"viridian"` 等。

尝试将 `letter.html` 中中间 `<div>` 元素的背景色更改为珊瑚色（`coral`）而不是白色。以下是代码：

```html
<center>
  <form>
    <input type = "button" value = "Change background color"
           onclick = "div1.style.backgroundColor = 'coral'">
  </form>
</center>
```

## 在网页中设置元素位置

CSS 在 Ajax 中的一个主要用途是设置网页中元素的绝对位置，例如当你创建弹出菜单、对话框、下拉自动完成列表框等时。表 7-3 列出并描述了设置绝对位置时使用的 CSS 属性。

> **注意**
>
> 默认情况下，`top`、`bottom`、`left` 和 `right` 的度量单位被认为是像素。你可以在这些值的末尾添加 `px`，以确保浏览器将度量值解释为像素，例如 `50px`。

| 属性 | 描述 |
| :--- | :--- |
| `position` | 设置为 `absolute` 以进行绝对定位。 |
| `top` | 元素顶部在屏幕上的偏移量。 |
| `bottom` | 元素底部在浏览器客户区域中的偏移量。 |
| `left` | 元素左边缘在浏览器客户区域中的偏移量。 |
| `right` | 元素右边缘在浏览器客户区域中的偏移量。 |
| `z-order` | 设置项目相对于其他元素的堆叠顺序。 |

**表 7-3** CSS 绝对定位属性。

下面是一个名为 `location.html` 的示例，它在网页中定位图像。每张图像将存储在一个 `<div>` 元素中，我们将设置该 `<div>` 元素的位置。我们将首先使用 HTML `style` 属性定位图像 1（`image01.jpg`）：

```html
<html>
<head>
<title>
Using Absolute Positioning
</title>
</head>
<body>
<h1 align="center">
Using Absolute Positioning
</h1>
<div style="position:absolute; left:40; top:60;" id="image01">
<img src="image01.jpg" width="200" height="100">
<br>
Image 1
</div>
.
.
.
</body>
</html>
```

请注意，我们在 `<div>` 元素中同时显示了图像和说明文字（“Image 1”），并给该元素赋予了 ID “image01”。还要注意，为了定位图像，我们将 `position` 样式属性设置为“absolute”，然后用 `top` 和 `left` 样式属性设置图像左上角的位置——默认情况下，这些位置以像素为单位。我们也可以添加其他两张图像：



```html
<html>
<head>
<title>
Using Absolute Positioning
</title>
</head>
<body>
<h1 align="center">
Using Absolute Positioning
</h1>
<div style="position:absolute; left:40; top:60;" id="image01">
    <img src="image01.jpg" width="200" height="100">
    <br>
    Image 1
</div>
<div style="position:absolute; left:195; top:90;" id="image02">
    <img src="image02.jpg" width="200" height="100">
    <br>
    Image 2
</div>
<div style="position:absolute; left:350; top:120;" id="image03">
    <img src="image03.jpg" width="200" height="100">
    <br>
    Image 3
</div>
...
</body>
</html>
```

然后，为了好玩，让我们添加一个按钮，让用户可以移动包含图像的其中一个`<div>`元素——比如`image01`——像这样：

```html
<html>
    <head>
        <title>
            Using Absolute Positioning
        </title>
    </head>
    <body>
        <h1 align="center">
            Using Absolute Positioning
        </h1>
        <div style="position:absolute; left:40; top:60;" id="image01">
            <img src="image01.jpg" width="200" height="100">
            <br>
            Image 1
        </div>
        <div style="position:absolute; left:195; top:90;" id="image02">
            <img src="image02.jpg" width="200" height="100">
            <br>
            Image 2
        </div>
```

# 248 Ajax：初学者指南

```html
<div style="position:absolute; left:350; top:120;" id="image03">
    <img src="image03.jpg" width="200" height="100">
    <br>
    Image 3
</div>
```

```html
<center>
    <form>
        <input type = "button" value = "Change location"
            style="position:absolute; left:220; top:260;"
            onclick = "image02.style.top = '150'">
    </form>
</center>

</body>

</html>
```

请注意，我们通过其 ID 访问第二个`div`的顶部位置：`image02.style.top`。同时也要注意，我们定位按钮的方式与定位图像的方式相同，都使用绝对定位。

你可以在图 7-6 中看到结果，正如你所见，图像已经正确定位。

当你点击按钮时，第二张图片会移动，这正如你所料，如图 7-7 所示。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_267_0.png)

## 第 7 章：使用 Ajax 处理层叠样式表 249

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_268_0.png)

图 7-7 动态定位图像

绝对定位在 Ajax 应用程序中非常有用，因为你可以将新数据放置在页面的任何位置；无需刷新。

## 动手试一试：添加一个额外的按钮

尝试添加一个额外的按钮来移动第三张图片。以下是一种实现方式：

```html
<html>
    <head>
        <title>
            Using Absolute Positioning
        </title>
    </head>

    <body>
        <h1 align="center">
            Using Absolute Positioning
        </h1>

        <div style="position:absolute; left:40; top:60;" id="image01">
            <img src="image01.jpg" width="200" height="100">
            <br>
            Image 1
```

（接下页）

```html
</div>

<div style="position:absolute; left:195; top:90;" id="image02">
    <img src="image02.jpg" width="200" height="100">
    <br>
    Image 2
</div>

<div style="position:absolute; left:350; top:120;" id="image03">
    <img src="image03.jpg" width="200" height="100">
    <br>
    Image 3
</div>

<center>
    <form>
        <input type = "button" value = "Change location of image 2"
            style="position:absolute; left:220; top:260;"
            onclick = "image02.style.top = '150'">
        <input type = "button" value = "Change location of image 3"
            style="position:absolute; left:220; top:290;"
            onclick = "image03.style.left = '400'">
    </form>
</center>

</body>

</html>
```

## 设置网页元素的层叠顺序

你也可以利用网页元素的层叠顺序来定位它们，这在 Ajax 应用程序中进行拖放操作时尤其重要，可以确保被拖动的元素滑过页面上的其他元素。具有较高层叠顺序的元素——通过样式属性`z-index`设置——会显示在层叠顺序较低的元素之上。

这是一个快速示例`stacker.html`，它显示了前一个示例中的三个堆叠图像：

```html
<html>

<head>
    <title>
        Using Stacking Order
    </title>
</head>

<body>
```

## 第 7 章：使用 Ajax 处理层叠样式表 251

```html
<h1 align="center">
	Using Stacking Order
</h1>

<div style="position:absolute; left:40; top:60;" id="image01">
	<img src="image01.jpg" width="200" height="100">
	<br>
	Image 1
</div>

<div style="position:absolute; left:195; top:90;" id="image02">
	<img src="image02.jpg" width="200" height="100">
	<br>
	Image 2
</div>

<div style="position:absolute; left:350; top:120;" id="image03">
	<img src="image03.jpg" width="200" height="100">
	<br>
	Image 3
</div>
.
.
.
</body>

</html>
```

现在，我们添加一个按钮，通过为`image01`分配`z-index`值 300，为`image02`分配 200，为`image03`分配 100，来反转层叠顺序：

```html
<html>
<head>
	<title>
		Using Stacking Order
	</title>
</head>
<body>
	<h1 align="center">
		Using Stacking Order
	</h1>
	<div style="position:absolute; left:40; top:60;" id="image01">
		<img src="image01.jpg" width="200" height="100">
		<br>
		Image 1
	</div>
```

### Ajax：初学者指南

```html
<div style="position:absolute; left:195; top:90;" id="image02">
    <img src="image02.jpg" width="200" height="100">
    <br>
    Image 2
</div>

<div style="position:absolute; left:350; top:120;" id="image03">
    <img src="image03.jpg" width="200" height="100">
    <br>
    Image 3
</div>

<center>
    <form>
        <input type = "button" value = "Flip stacking order"
               style="position:absolute; left:200; top:260;"
               onclick = "image01.style.zIndex = '300';
                          image02.style.zIndex = '200'; image03.style.zIndex = '100';">
    </form>
</center>

</body>

</html>
```

你可以在图 7-8 中看到原始的层叠顺序。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_271_0.png)

**图 7-8 堆叠的图像**

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_272_0.png)

图 7-9 设置层叠顺序

当你点击按钮时，层叠顺序会反转，如图 7-9 所示。效果不错。

## 一个完整的 Ajax CSS 示例：`menus.html`

作为本章最后一个侧重于 CSS 的示例，我们将研究一个支持 Ajax 的 CSS 驱动菜单系统。这个真实世界的示例`menus.html`从服务器下载菜单项，并使用 CSS 显示其菜单。因为菜单项是实时下载的，所以你可以更新和更改应用程序显示的菜单项。例如，如果你的菜单是为一家供应冰淇淋和三明治的餐厅准备的，而餐厅的甘草冰淇淋售罄了，你可以在下载菜单项之前从菜单中移除该项目。

你可以在图 7-10 中看到`menus.html`的运行效果，用户正在从一个弹出菜单中选择巧克力冰淇淋，该菜单项是刚刚在后台使用 Ajax 下载的。

当用户做出选择时，应用程序会报告该选择，如你所见图 7-11。

这是一个完整的 Ajax 应用程序，代码很长，所以不必觉得需要掌握所有细节。这个示例的目的是展示如何使用 CSS 以独特的方式显示 Ajax 下载的数据——在响应鼠标点击的下拉菜单中。在此过程中，你将学到一些 CSS 和 JavaScript 技能。

## 254 Ajax：初学者指南

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_273_0.png)

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_273_1.png)

对鼠标的响应构成了这个示例的很大一部分。当用户将鼠标移到某个图像（"Ice Cream" 或 "Sandwiches"）上时，相应的菜单需要弹出打开。如果用户将鼠标移开菜单，菜单需要关闭。如果用户点击菜单中的某个项目进行选择，应用程序必须做出相应的响应。最重要的是，应用程序必须同时在 Internet Explorer 和 Firefox 类型的浏览器中响应鼠标，而这些浏览器处理鼠标的方式完全不同。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_273_2.png)

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_273_3.png)

## 第 7 章：使用 Ajax 处理层叠样式表

首先，在应用程序的`<body>`中，我们将设置用户可以移动鼠标以打开菜单的图像（"Ice Cream" 和 "Sandwiches"），并创建用于容纳菜单的`<div>`元素：

```html
<body onclick = "hideMenu()" onmousemove = "checkMenu(event)">

    <H1>Creating an Ajax-enabled Menu System</H1>

    <img id = "image1" src="image1.jpg"
      style="left:30; top:50; width:200; height:40;">
    <div id = "menu1Div" style="position: absolute; left:30; top:100;
      width:100; height: 70; visibility:hidden;"><div></div></div>
    <img id = "image2" style="left:270; top:50; width:200;
      height:40;" src="image2.jpg">
    <div id = "menu2Div" style="position: absolute; left:270; top:100;
      width:100; height: 70; visibility:hidden;"><div></div></div>
    <br>
    <br>
    <div id = "targetDiv"></div>
</body>
```

请注意，在此处我们将`<body>`元素的`onmousemove`事件连接到 JavaScript 函数`checkMenu`（参见上面的`<body>`标签）。这个函数将响应鼠标移动，根据需要打开和关闭菜单。

在`checkMenu`函数中，我们首先使用另一个函数`mouseEventCreator`创建一个新的鼠标事件对象：

```javascript
function checkMenu(evt)
{
    var e = new mouseEventCreator(evt);
    .
    .
    .
}
```

我们创建自己的鼠标事件对象的原因是，Internet Explorer 和 Firefox 处理鼠标的方式完全不同，我们需要将这两种方式合并到一个对象中，以使我们的代码更简单。我们将创建的鼠标事件将具有以下属性：

- `e`包含实际浏览器的事件对象（其中包含有关事件的信息，例如鼠标是否被点击、拖动或只是移动）。
- `x`和`y`包含事件发生的（x，y）位置，以像素为单位。
- `target`包含一个与作为鼠标事件目标的 HTML 元素相对应的对象。例如，如果事件是鼠标单击，此属性将包含一个与被单击的 HTML 元素相对应的对象。

这是我们刚才用来创建统一鼠标事件对象的`mouseEventCreator`，它考虑了 Internet Explorer 和 Firefox 在处理鼠标事件时的不同方式：

```javascript
function mouseEventCreator(e)
{
    if(e) {
        this.e = e;
    } else {
        this.e = window.event;
    }

    if(e.pageX) {
        this.x = e.pageX;
    } else {
        this.x = e.clientX;
    }

    if(e.pageY) {
        this.y = e.pageY;
    } else {
        this.y = e.clientY;
    }

    if(e.target) {
        this.target = e.target;
    } else {
        this.target = e.srcElement;
    }
}
```



现在，回到`checkMenu`函数，我们得到了一个统一的鼠标事件对象，它具有`e`、`x`、`y`和`target`属性。在`checkMenu`中，我们将检查鼠标是否移动到了任一图像上方。如果是这种情况，我们就需要下载菜单项并显示相应的菜单。

我们通过检查鼠标事件的`target`属性来实现这一点。如果`target`持有一个与某个图像匹配的对象，我们就为对应的菜单（即菜单1或2）下载菜单项。我们将使用一个名为`getData`的函数来下载菜单项——调用`getData(1)`将下载第一个菜单（冰淇淋菜单）的项，调用`getData(2)`将下载第二个菜单（三明治菜单）的项。以下是`checkMenu`中的代码：

```javascript
function checkMenu(evt)
{
    var e = new mouseEventCreator(evt);
    var imgObject;

    imgObject = document.getElementById("image1");

    if(e.target == imgObject){
        getData(1);
    }

    imgObject = document.getElementById("image2");

    if(e.target == imgObject){
        getData(2);
    }
    // ... 其他代码 ...
}
```

`getData`函数的全部工作就是下载菜单项并调用一个函数`showMenu`，该函数将显示请求的菜单。

第一个菜单的菜单项存储在文档`items1.txt`中：

草莓、香草、巧克力

第二个菜单的菜单项存储在文档`items2.txt`中：

火鸡、牛肉、沙丁鱼

以下是`getData`函数的代码——请注意，它只是使用 Ajax 下载存储在`items1.txt`或`items2.txt`中的文本，并将该文本传递给`showMenu`函数：

```javascript
function getData(menuNumber)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new
            ActiveXObject("Microsoft.XMLHTTP");
    }

    var itemsSource;

    if(menuNumber== 1){
        itemsSource = "items1.txt";
    } else {
        itemsSource = "items2.txt";
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", itemsSource);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                showMenu(menuNumber, XMLHttpRequestObject.responseText);
            }
        }

        XMLHttpRequestObject.send(null);
    }
}
```

`getData`函数调用`showMenu`函数，向其传递要显示的菜单编号（1或2），以及从服务器下载的、包含菜单项的文本（“草莓、香草、巧克力”或“火鸡、牛肉、沙丁鱼”）。`showMenu`函数使用这些菜单项显示正确的菜单。

该函数首先使用便捷的 JavaScript`split`函数将下载的文本分割成一个名为`menuItems`的全局项数组。`split`函数会将一个文本字符串分割成一个字符串数组，前提是向该函数传递要分割字符串的字符或字符序列（这里是一个逗号）。以下是我们如何创建`menuItems`（我们想要显示的菜单项数组）：

```html
<html>
  <head>
    <script language="javascript">
      var menuItems;
      // ...
      function showMenu(menuNumber, itemsString)
      {
        menuItems = itemsString.split(", ");
        // ...
      }
    </script>
  </head>
</html>
```

每个菜单实际上将是一个包含菜单项的 HTML 表格，我们将通过一个循环来构建这个表格。该循环遍历`menuItems`数组中的菜单项，其代码如下所示：

```javascript
function showMenu(menuNumber, itemsString)
{
  var loopIndex;

  menuItems = itemsString.split(", ");

  var menuText = "<table width = '100%'>";

  if (menuItems.length != 0) {
    for (var loopIndex = 0; loopIndex < menuItems.length;
         loopIndex++) {
      var text = "displaySelection(" + loopIndex + ")";
      menuText += "<tr><td "
        + "onclick='" + text + "'>" +
        menuItems[loopIndex] +
        "</td></tr>";
    }
  }

  menuText += "</table>";
  // ...
}
```

您可能会注意到，菜单 HTML 表格中每个单元格的`onclick`事件都连接到一个名为`displaySelection`的函数。当用户点击 HTML 表格中的一个单元格（即我们显示的菜单中的一项）时，浏览器将调用`displaySelection`函数，这就是我们处理菜单项点击的方式。

既然我们已经组装好了菜单的 HTML，我们就可以显示该菜单了。我们可以通过 CSS 属性`visibility`来控制 HTML 元素的可见性，可以将其设置为`"visible"`或`"hidden"`。以下是我们如何将菜单的 HTML 加载到正确的`<div>`元素中，然后使该菜单可见：

```javascript
function showMenu(menuNumber, itemsString)
{
  var loopIndex;
  var menuObject;

  menuItems = itemsString.split(", ");

  var menuText = "<table width = '100%'>";

  if (menuItems.length != 0) {
    for (var loopIndex = 0; loopIndex < menuItems.length;
         loopIndex++) {
      var text = "displaySelection(" + loopIndex + ")";
      menuText += "<tr><td "
        + "onclick='" + text + "'>" +
        menuItems[loopIndex] +
        "</td></tr>";
    }
  }

  menuText += "</table>";

  if(menuNumber == "1"){
    menuObject = document.getElementById("menu1Div");
  }

  if(menuNumber == "2"){
    menuObject = document.getElementById("menu2Div");
  }

  if(menuObject.style.visibility == "hidden"){
    menuObject.innerHTML = menuText;
    menuObject.style.visibility = "visible";
  }
}
```

呼。这会在鼠标移动到匹配的图像上时（即，如果鼠标移动事件的`target`是图像）显示一个菜单。

但是，如果用户将鼠标移开图像呢？在这种情况下，我们应该隐藏任何可见的菜单。我们已经在`checkMenu`函数中检查了鼠标是否移动到图像上并显示了相应的菜单；现在我们必须在`checkMenu`中添加代码，以便在用户将鼠标从图像上移开时隐藏菜单。以下是`checkMenu`中的代码——我们将调用一个名为`hideMenu`的函数来隐藏菜单：

```javascript
function checkMenu(evt)
{
    var e = new mouseEventCreator(evt);
    var menuObject = null;
    var imgObject;

    imgObject = document.getElementById("image1");

    if(e.target == imgObject){
        getData(1);
    }

    imgObject = document.getElementById("image2");

    if(e.target == imgObject){
        getData(2);
    }

    menuObject = document.getElementById("menu1Div");

    imgObject = document.getElementById("image1");

    if (menuObject.style.visibility == "visible"){
        if(e.x < parseInt(menuObject.style.left) || e.y < parseInt(imgObject.style.top) ||
           e.x > (parseInt(imgObject.style.left) + parseInt(imgObject.style.width)) ||
           e.y > (parseInt(menuObject.style.top) + parseInt(menuObject.style.height))){
            hideMenu();
        }
    }

    menuObject = document.getElementById("menu2Div");
    imgObject = document.getElementById("image2");

    if (menuObject.style.visibility == "visible"){
        if(e.x < parseInt(menuObject.style.left) || e.y < parseInt(imgObject.style.top) ||
           e.x > (parseInt(imgObject.style.left) + parseInt(imgObject.style.width)) ||
           e.y > (parseInt(menuObject.style.top) + parseInt(menuObject.style.height))){
            hideMenu();
        }
    }
}
```

## 专家解答

> **问：** 这段代码中的 JavaScript`parseInt`函数是什么？
>
> **答：** 该代码正在检查鼠标是否在图像的边界之外。它使用诸如`menuObject.style.top`或`menuObject.style.left`之类的样式属性获取这些边界——而这些属性是以文本形式存储的。为了将它们从文本转换为数字，以便将鼠标位置与之进行比较，您可以使用 JavaScript`parseInt`函数。该函数将文本转换为整数。

为了在用户将鼠标移出图像外部时隐藏菜单，前面的代码调用了`hideMenu`函数。该函数只是将菜单的`visibility`属性设置为`"hidden"`来隐藏菜单。以下是该代码：

```javascript
function hideMenu()
{
    var menu1Div = document.getElementById("menu1Div");

    if(menu1Div.style.visibility == "visible"){
        menu1Div.innerHTML = "<div></div>";
        menu1Div.style.visibility = "hidden";
    }

    var menu2Div = document.getElementById("menu2Div");

    if(menu2Div.style.visibility == "visible"){
        menu2Div.innerHTML = "<div></div>";
        menu2Div.style.visibility = "hidden";
    }
}
```

## 262 Ajax：初学者指南

哇，这里涉及很多 JavaScript 代码。但我们即将完成这个示例。

最后一个函数是`displaySelection`函数，当用户点击菜单项时，浏览器会调用它。`displaySelection`函数接收被点击的菜单项编号（例如，在第一个菜单中，“Strawberry”是第0项，“Vanilla”是第1项，“Chocolate”是第2项），该函数的任务是在网页上显示用户的选择。

`displaySelection`函数通过将该编号作为我们之前创建的菜单项名称数组`menuItems`的索引，将编号（0、1或2）转换为英文项目名称（“Strawberry”、“Vanilla”或“Chocolate”）。所以，终于，这就是我们显示用户菜单选择的方式：

```javascript
function displaySelection(index)
{
    var targetDiv = document.getElementById("targetDiv");
    targetDiv.innerHTML = "You chose " + menuItems[index] + ".";
}
```

至此，这个示例就完成了。这是该应用程序的完整代码——请注意，我们还在一个`<style>`元素中设置了菜单和显示`<div>`元素的样式（`menus.html`）：



```html
<html>
  <head>
    <title>Creating an Ajax-enabled Menu System</title>
    <style>
      #targetDiv {
        color: #00BBBB;
        font-size: 24pt;
        font-weight: bold;
        font-family: arial;
      }
      #menu1Div {
        color: #222222;
        background-color: #FFCCFF;
        font-weight: bold;
        font-family: arial;
        visibility: hidden;
        cursor: hand;
      }
      #menu2Div {
        color: #222222;
        background-color: #FFCCFF;
        font-weight: bold;
        font-family: arial;
        visibility: hidden;
        cursor: hand;
      }
    </style>

    <script language = "javascript">
      var menuItems;

      function checkMenu(evt)
      {
        var e = new mouseEventCreator(evt);
        var menuObject = null;
        var imgObject;

        imgObject = document.getElementById("image1");

        if(e.target == imgObject){
          getData(1);
        }

        imgObject = document.getElementById("image2");

        if(e.target == imgObject){
          getData(2);
        }

        menuObject = document.getElementById("menu1Div");

        imgObject = document.getElementById("image1");

        if (menuObject.style.visibility == "visible"){
          if(e.x < parseInt(menuObject.style.left) || e.y <
             parseInt(imgObject.style.top) ||
             e.x > (parseInt(imgObject.style.left) +
                    parseInt(imgObject.style.width))
             || e.y > (parseInt(menuObject.style.top) +
                       parseInt(menuObject.style.height))){
            hideMenu();
          }
        }

        menuObject = document.getElementById("menu2Div");

        imgObject = document.getElementById("image2");

        if (menuObject.style.visibility == "visible"){
          if(e.x < parseInt(menuObject.style.left) || e.y <
             parseInt(imgObject.style.top) ||
             e.x > (parseInt(imgObject.style.left) +
                    parseInt(imgObject.style.width))
             || e.y > (parseInt(menuObject.style.top) +
                       parseInt(menuObject.style.height))){
            hideMenu();
          }
        }
      }

      function mouseEventCreator(e)
      {
        if(e) {
          this.e = e;
        } else {
          this.e = window.event;
        }

        if(e.pageX) {
          this.x = e.pageX;
        } else {
          this.x = e.clientX;
        }

        if(e.pageY) {
          this.y = e.pageY;
        } else {
          this.y = e.clientY;
        }

        if(e.target) {
          this.target = e.target;
        } else {
          this.target = e.srcElement;
        }
      }

      function getData(menuNumber)
      {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
          XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
          XMLHttpRequestObject = new
              ActiveXObject("Microsoft.XMLHTTP");
        }

        var itemsSource;

        if(menuNumber== 1){
          itemsSource = "items1.txt";
        } else {
          itemsSource = "items2.txt";
        }

        if(XMLHttpRequestObject) {
          XMLHttpRequestObject.open("GET", itemsSource);

          XMLHttpRequestObject.onreadystatechange = function()
          {
            if (XMLHttpRequestObject.readyState == 4 && XMLHttpRequestObject.status == 200) {
              showMenu(menuNumber, XMLHttpRequestObject.responseText);
            }
          }

          XMLHttpRequestObject.send(null);
        }
      }

      function showMenu(menuNumber, itemsString) {
        var loopIndex;
        var menuObject;

        menuItems = itemsString.split(", ");

        var menuText = "<table width = '100%'>";

        if (menuItems.length != 0) {
          for (var loopIndex = 0; loopIndex < menuItems.length; loopIndex++) {
            var text = "displaySelection(" + loopIndex + ")";
            menuText += "<tr><td " + "onclick='" + text + "'>" + menuItems[loopIndex] + "</td></tr>";
          }
        }

        menuText += "</table>";

        if(menuNumber == "1"){
          menuObject = document.getElementById("menu1Div");
        }

        if(menuNumber == "2"){
          menuObject = document.getElementById("menu2Div");
        }

        if(menuObject.style.visibility == "hidden"){
          menuObject.innerHTML = menuText;
          menuObject.style.visibility = "visible";
        }
      }

      function hideMenu() {
        var menu1Div = document.getElementById("menu1Div");

        if(menu1Div.style.visibility == "visible"){
          menu1Div.innerHTML = "<div></div>";
          menu1Div.style.visibility = "hidden";
        }

        var menu2Div = document.getElementById("menu2Div");
        if(menu2Div.style.visibility == "visible"){
          menu2Div.innerHTML = "<div></div>";
          menu2Div.style.visibility = "hidden";
        }
      }

      function displaySelection(index)
      {
        var targetDiv = document.getElementById("targetDiv");
        targetDiv.innerHTML = "You chose " + menuItems[index] + ".";
      }
    </script>
  </head>
  <body onclick = "hideMenu()" onmousemove = "checkMenu(event)">
    <H1>Creating an Ajax-enabled Menu System</H1>
    <img id = "image1" src="image1.jpg"
         style="left:30; top:50; width:200; height:40;">
    <div id = "menu1Div" style="position: absolute; left:30; top:100;
         width:100; height: 70; visibility:hidden;"><div></div></div>
    <img id = "image2" style="left:270; top:50; width:200;
         height:40;" src="image2.jpg">
    <div id = "menu2Div" style="position: absolute; left:270; top:100;
         width:100; height: 70; visibility:hidden;"><div></div></div>
    <br>
    <br>
    <div id = "targetDiv"></div>
  </body>
</html>
```

以上就是`menus.html`，我们第一个完整的Ajax深度示例。这里涉及大量的CSS和JavaScript——而这正是关键所在。在大多数Ajax应用中，通常都会有大量的CSS和JavaScript在运行。

你现在对如何在Ajax应用中处理CSS（更不用说鼠标事件）有了实用的知识，并且你可以让使用Ajax下载的数据出现在页面上任何你想要的位置，无需刷新页面。这很酷。

## 第8章：使用Ajax处理动态HTML

### 核心技能与概念

- 使用动态HTML方法更新页面
- 使用动态HTML属性更新页面
- 动态创建元素
- 使用数据更新表格
- 向浏览器写入文档

正如第7章所述，使用Ajax的主要原因是它使你能够在浏览器中无需刷新页面的情况下更新网页。你已经看到如何使用CSS来实现这一点；在本章中，你将看到如何将Ajax与动态HTML结合使用。

与CSS类似，动态HTML也提供了更新和管理网页的方式。在许多方面，动态HTML比CSS更强大，因为通过使用动态HTML，你可以修改页面中的HTML。我们将首先探讨这究竟是如何工作的。

### 使用动态HTML方法更新页面

使用动态HTML修改网页中的HTML主要有两种方式：方法或属性。我们已经在本书中使用了`innerHTML`这个动态HTML属性将下载的数据插入网页：

```javascript
if(XMLHttpRequestObject) {
  var obj = document.getElementById("targetDiv");
  XMLHttpRequestObject.open("GET", dataSource);

  XMLHttpRequestObject.onreadystatechange = function()
  {
    if (XMLHttpRequestObject.readyState == 4 &&
        XMLHttpRequestObject.status == 200) {
          obj.innerHTML = XMLHttpRequestObject.responseText;
    }
  }
}
```

还有其他可用的动态HTML属性，正如你将在本章中看到的。但是，使用动态HTML方法是怎么回事？你可以用来修改网页中HTML的主要方法如下：

- `insertAdjacentHTML` 允许你在已存在的元素旁边插入HTML
- `insertAdjacentText` 允许你在已存在的元素旁边插入文本

通过向`insertAdjacentHTML`和`insertAdjacentText`方法传递常量`"BeforeBegin"`、`"AfterBegin"`、`"BeforeEnd"`或`"AfterEnd"`，你可以指定新的文本或HTML相对于现有元素的位置。

在下面的示例`insertAdjacent.html`中，我们将在用户点击按钮时使用`insertAdjacent`方法插入一些文本和一个文本框。我们从一个名为`targetDiv`的`<div>`元素内的按钮开始：

```html
<body>
    <center>
        <h1>
            Updating a Page With insertAdjacentHTML
        </h1>
    </center>

    <div id="targetDiv">
        <center>
            <form>
                <input type=button value="Click here"
                       onclick="addHTML()">
            </form>
        </center>
    </div>
</body>
```

该按钮连接到一个名为`addHTML`的JavaScript函数，该函数将添加新文本和文本框所需的HTML：

```javascript
<script language="JavaScript">
    function addHTML()
    {
        .
        .
        .
    }
</script>
```

在`addHTML`函数中，我们可以使用`insertAdjacentHTML`方法在`targetDiv` `<div>`元素之后添加我们想要的HTML。要在`targetDiv` `<div>`元素的末尾之后添加该HTML，我们可以将常量`"AfterEnd"`传递给`insertAdjacentHTML`方法，如下所示：



```javascript
<script language="JavaScript">
    function addHTML()
    {
        targetDiv.insertAdjacentHTML("AfterEnd",
        .
        .
        .
        }
    </script>
```

并且我们必须指定要插入的HTML，我们可以通过以下方式创建一个文本框和一些新文本来实现：

```javascript
<script language="JavaScript">

  function addHTML()
  {
    targetDiv.insertAdjacentHTML("AfterEnd",
    "<p><input type=text value='Hello there.'> See? A new text field.</p>");
  }

</script>
```

以下是完整示例，`insertAdjacent.html`：

```html
<html>
  <head>
    <title>
      Updating a Page With insertAdjacentHTML
    </title>

    <script language="JavaScript">
      function addHTML()
      {
        targetDiv.insertAdjacentHTML("AfterEnd",
        "<p><input type=text value='Hello there.'> See? A new text field.</p>");
      }
    </script>
  </head>

  <body>

    <center>
      <h1>
        Updating a Page With insertAdjacentHTML
      </h1>
    </center>

    <div id="targetDiv">
        <center>
            <form>
                <input type=button value="Click here"
                       onclick="addHTML()">
            </form>
        </center>
    </div>

</body>
</html>
```

你可以在图8-1中看到这个页面的实际效果。当你点击按钮时，一个新的文本框（其中包含文本）和一些额外的文本会出现，如图8-2所示。很酷吧。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_290_1.png)

**图8-3** 向`insertAdjacent.html`添加更多HTML

如果你再次点击按钮，新的HTML会再次被添加到页面中，如图8-3所示。

如果你希望使用Ajax重新配置你的网页（例如，根据下载的数据向页面添加或移除表格），这是一个很好的方法。

另一方面，这里有一个问题。`insertAdjacentHTML` 和 `insertAdjacentText` 方法在Firefox类型的浏览器中不起作用。如果你想保持跨浏览器兼容性，可以使用接下来要介绍的动态HTML属性。

## 使用动态HTML属性更新页面

无论你是在Internet Explorer还是Firefox中，网页中的每个项目都支持以下动态HTML属性：

- `innerText` 允许你更改元素开始和结束标签之间的文本（Mozilla/Netscape/Firefox不支持）。
- `outerText` 允许你更改元素的所有文本，包括开始和结束标签（Mozilla/Netscape/Firefox不支持）。
- `innerHTML` 更改元素开始和结束标签之间的内容；可以包含HTML。
- `outerHTML` 更改元素的内容，包括开始和结束标签；将文本视为HTML。

如前所述，你已经在本书中多次看到`innerHTML`属性：

```javascript
if (XMLHttpRequestObject) {
    var obj = document.getElementById("targetDiv");
    XMLHttpRequestObject.open("GET", dataSource);

    XMLHttpRequestObject.onreadystatechange = function()
    {
        if (XMLHttpRequestObject.readyState == 4 &&
            XMLHttpRequestObject.status == 200) {
            obj.innerHTML = XMLHttpRequestObject.responseText;
        }
    }
}
```

下面是一个使用`innerText`属性的示例`innerText.html`。这个示例让你点击一个HTML `<h1>`标题——当你点击时，它会更改该标题中的文本。我们从标题本身开始，并将一个名为`changeHeader`的函数连接到标题的`onclick`事件：

```html
<body>
    <center>
        <h1 id = "header"
            onclick = "changeHeader()">
            Changing Text With the innerText Property
        </h1>
        Click the above header to make it change.
    </center>
</body>
```

现在，当用户点击标题时，将调用`changeHeader`函数：

```html
<head>
    <title>
        Changing Text With the innerText Property
    </title>

    <script language = "JavaScript">
        function changeHeader()
        {
            .
            .
            .
        }
    </script>
</head>
```

在`changeHeader`函数中，你可以使用`innerText`属性在`<h1>`标题内放置新文本：

```javascript
<script language = "JavaScript">
    function changeHeader()
    {
        var header = document.getElementById("header");
        header.innerText = "Here is the new header.";
    }
</script>
```

以下是完整示例`innerText.html`的样子：

```html
<html>
    <head>
        <title>
            Changing Text With the innerText Property
        </title>
        <script language = "JavaScript">
            function changeHeader()
            {
                var header = document.getElementById("header");
                header.innerText = "Here is the new header.";
            }
        </script>
    </head>
    <body>
        <center>
            <h1 id = "header"
                onclick = "changeHeader()">
                Changing Text With the innerText Property
            </h1>
            Click the above header to make it change.
        </center>
    </body>
</html>
```

你可以在图8-4中看到这个页面的实际效果。当你点击标题时，该标题中的文本会发生变化，如图8-5所示。很好。你使用`innerText`属性来设置元素的内部文本，而不是完全重写它。请注意，如果你想要将HTML插入到标题中，可以改用`innerHTML`属性。以下是一个将`<marquee>`元素插入标题并显示滚动字幕的示例——请注意，此元素仅在Internet Explorer中有效（`innerHTML.html`）：

```html
<html>
    <head>
        <title>
            Changing HTML With the innerHTML Property
        </title>

        <script language = "JavaScript">

            function changeHeader()
            {
                var header = document.getElementById("header");
                header.innerHTML = "<marquee>Here is the new header.</marquee>";
            }

        </script>

    </head>

    <body>

        <center>
            <h1 id = "header"
                onclick = "changeHeader()">
                Changing HTML With the innerHTML Property
            </h1>

            Click the above header to make it change.
        </center>

    </body>

</html>
```

你可以在图8-6中看到`innerHTML`的实际效果。当你点击标题时，会出现一个新的滚动字幕（至少在Internet Explorer中是这样）。`<h1>`标题内的HTML已被替换，新的字幕显示为一个滚动的`<h1>`标题。

如果你想要将`<h1>`标题本身更改为，比如说，一个`<h3>`标题呢？你可以使用`outerHTML`属性而不是`innerHTML`。`outerHTML`属性允许你重写包含你正在处理的元素的HTML。换句话说，使用`innerHTML`属性可以让你编辑当前元素内部的HTML，而`outerHTML`属性可以让你更改当前元素的所有HTML。

# 第8章：使用Ajax处理动态HTML

![图8-6 更改标题中的HTML](img/2cd265cf0a64e9b4b91ab611753cd5d5_296_0.png)

图8-6 更改标题中的HTML

这在一个新示例`outerHTML.html`中是如何工作的。在此示例中，当您点击`<h1>`标题时，`changeHeader`函数将使用`outerHTML`属性将其更改为`<h3>`标题：

```javascript
function changeHeader()
{
    var header = document.getElementById("header");
    header.innerHTML =
    "<h3>Here is the new, smaller header</h3>"
}
```

整个示例`outerHTML.html`如下所示：

```html
<html>
    <head>
        <title>
            Changing HTML With the outerHTML Property
        </title>

        <script language = "JavaScript">
            function changeHeader()
            {
                var header = document.getElementById("header");
                header.innerHTML =
                "<h3>Here is the new, smaller header</h3>"
            }
        </script>
    </head>
    <body>
        <center>
            <h1 id = header
                onclick = "changeHeader()">
                Changing HTML With the outerHTML Property
            </h1>

            Click the above header to make it change.
        </center>
    </body>
</html>
```

![图8-7 `outerHTML.html`运行效果](img/2cd265cf0a64e9b4b91ab611753cd5d5_297_0.png)

图8-7 `outerHTML.html`运行效果

您可以在图8-7中看到`outerHTML.html`的实际运行情况。当用户在图8-7中点击`<h1>`标题时，`changeHeader`函数使用`outerHTML`属性将其更改为图8-8中您所看到的`<h3>`标题。效果不错。

![图8-8 将`<h1>`标题更改为`<h3>`标题](img/2cd265cf0a64e9b4b91ab611753cd5d5_297_1.png)

图8-8 将`<h1>`标题更改为`<h3>`标题

说到动态HTML，您会发现Internet Explorer具有比任何其他浏览器更多的功能——对于本章目前讨论的主题也是如此：在我们讨论的动态HTML属性中，只有`innerHTML`在Firefox中受支持；所有其他属性（`innerText`、`outerText`和`outerHTML`）仅在Internet Explorer中受支持。

事实上，Internet Explorer中内置了更多动态HTML功能，可以让您像在启用Ajax的应用程序中那样更改网页内容。除了我们在本章讨论的方法和属性外，您还可以使用文本范围。

## 在Internet Explorer中使用文本范围

在Internet Explorer中，您可以定位文本部分并使用文本范围来处理它们。文本范围内置了各种方法，但我们在本章只看一个简单的示例，因为文本范围仅在Internet Explorer中可用。

这是一个示例`textRanges.html`，它将文本放入文本范围，然后在该范围上粘贴HTML以进行替换。此示例以一个按钮开始，当点击时，调用名为`changeText`的函数：

```html
<body>
    <center>
        <h1>
            Replacing Text With Text Ranges
        </h1>
    </center>

    <input type="button" value="Click here"
        onclick="changeText()">

    <br>
    <br>

    <div id="div1">
        Click the button to change this text.
    </div>

</body>
```

在`changeText`函数中，我们为文档创建一个新的文本范围：

```javascript
function changeText()
{
    var range = document.body.createTextRange();
    .
    .
    .
}
```

然后我们创建一个对应于我们要覆盖的`<div>`元素的对象：

```javascript
function changeText()
{
    var range = document.body.createTextRange();
    var div = document.getElementById("div1");
    .
    .
    .
}
```

接下来，我们移动文本范围，使其包含`<div>`元素：

```javascript
function changeText()
{
    var range = document.body.createTextRange();
    var div = document.getElementById("div1");
    range.moveToElementText(div);
    .
    .
    .
}
```

最后，我们可以使用新文本范围的`pasteHTML`方法粘贴一些文本，替换`<div>`中当前的文本（"Click the button to change this text."）为新文本（"You have successfully clicked the button."）：



```javascript
function changeText()
{
    var range = document.body.createTextRange();
    var div = document.getElementById("div1");
    range.moveToElementText(div);
    range.pasteHTML("You have successfully clicked the button.");
}
```

这是整个示例`textRanges.html`：

```html
<html>
  <head>
    <title>
      Replacing Text With Text Ranges
    </title>

    <script language="JavaScript">
      function changeText()
      {
        var range = document.body.createTextRange();
        var div = document.getElementById("div1");
        range.moveToElementText(div);
        range.pasteHTML("You have successfully clicked the button.");
      }
    </script>
  </head>

  <body>
    <center>
      <h1>
        Replacing Text With Text Ranges
      </h1>
    </center>

    <input type="button" value="Click here"
      onclick="changeText()">

    <br>
    <br>

    <div id="div1">
      Click the button to change this text.
    </div>
  </body>
</html>
```

您可以在图8-9中看到此示例。当您在此示例中点击按钮时，代码将新文本粘贴到包含`<div>`元素的文本范围上，您可以在图8-10中看到结果。文本范围是强大的工具，但除非您确定只处理Internet Explorer，否则在Ajax应用程序中可能应该避免使用它们；否则，您将不得不为其他浏览器在代码中复制相同的操作。

![图8-9 textRanges.html运行效果](img/2cd265cf0a64e9b4b91ab611753cd5d5_301_0.png)

如您所知，您可以使用通过Ajax下载的数据来配置页面。您甚至可以编写新的HTML来根据需要向页面添加控件——例如，您可能正在从房地产网站下载房屋列表，并需要创建按钮以便用户可以电子邮件联系列表代理。在Ajax中创建新HTML是一件非常常见的事情，正如您所看到的，您只需将其写入页面即可创建该新HTML。另一方面，如果您有很多HTML要写，可能会变得混乱。

有一种特殊的动态HTML方法`createElement`，可用于创建新HTML元素，如果您必须创建大量新元素，可以节省您的时间。`createElement`还有一个额外的好处，它可以在Internet Explorer和Firefox类型的浏览器中工作。

![图8-10 替换文本范围中的文本](img/2cd265cf0a64e9b4b91ab611753cd5d5_301_1.png)

## 使用createElement创建新HTML元素

Ajax应用程序经常需要创建新HTML元素。例如，如果您下载类似Rolodex的电话目录数据，您将必须为Rolodex中使用的控件创建HTML。或者，如果您编写一个Ajax电子邮件应用程序，在用户请求之前下载电子邮件文本以避免延迟，您将必须创建按钮和文本字段以使用户能够回复电子邮件。或者，如果您正在与在线数据库交互，您将必须动态创建HTML表格以在其中显示数据。

所有这些任务都可以用`createElement`方法来执行，我们现在将在一个新示例`createElement.html`中查看该方法。当您在此示例中点击按钮时，示例会创建一个包含文本的文本框、一个可用的按钮（点击它会显示一个JavaScript警报对话框）和一些文本。我们如何只创建文本？事实证明，我们可以使用名为`createTextNode`的方法创建文本节点，这正是我们将要做的，将我们想要显示的文本添加到该文本节点中。

我们从`createElement.html`示例开始，包含用户点击以创建新元素的按钮：

```html
<body>
    <center>
        <h1>
            Creating New Elements
        </h1>
    </center>

    <form>
        <input type="button" value="Click here"
            onclick="createNewElements()">
    </form>

</body>
```

当按钮被点击时，调用名为`createNewElements`的函数：

```javascript
function createNewElements()
{
    .
    .
    .
}
```

我们将把在此示例中创建的新元素（一个文本框、一个按钮和一个文本节点）添加到一个`<div>`元素中，并现在开始创建该`<div>`元素：

```javascript
function createNewElements()
```

284 Ajax：入门指南

```javascript
{
    var newDiv;

    newDiv = document.createElement("div");
    .
    .
    .
}
```

注意这里使用了 `createElement` 方法，它用于创建新的 `<div>` 元素。我们可以将新创建元素的属性作为元素对象的属性来访问。例如，要设置新 `<div>` 元素的 ID 属性，我们只需使用 `<div>` 对象的 `id` 属性：

```javascript
<script language="JavaScript">
function createNewElements()
{
    var newDiv;

    newDiv = document.createElement("div");
    newDiv.id = "NewDIV";
    .
    .
    .
}
</script>
```

现在，我们将创建要添加到 `<div>` 元素中的新 HTML 元素，首先从新的文本字段开始。文本字段是 `<input>` 元素，所以我们这样创建它们：

```javascript
<script language="JavaScript">
function createNewElements()
{
    var newDiv, newTextfield, newText, newButton;

    newDiv = document.createElement("div");
    newDiv.id = "NewDIV";

    newTextfield = document.createElement("input");
    .
    .
    .
}
</script>
```

这创建了一个通用的 `<input>` 元素。我们如何将其变成文本字段？我们必须将 `type` 属性设置为 "text"，我们可以这样做：

```javascript
<script language="JavaScript">
function createNewElements()
{
    var newDiv, newTextField, newText, newButton;

    newDiv = document.createElement("div");
    newDiv.id = "NewDIV";

    newTextField = document.createElement("input");
    newTextField.type = "text";
    .
    .
    .
}
</script>
```

我们还可以通过设置其 `value` 属性来向新文本字段添加文本，如下所示，我们在这里将文本 "Hello!" 存储在新的文本字段中：

```javascript
<script language="JavaScript">
function createNewElements()
{
    var newDiv, newTextField, newText, newButton;

    newDiv = document.createElement("div");
    newDiv.id = "NewDIV";

    newTextField = document.createElement("input");
    newTextField.type = "text";
    newTextField.value = "Hello!";
    .
    .
    .
}
</script>
```

好了，这创建了新的文本字段，现在存储在 `newTextField` 对象中。接下来，让我们创建新的按钮，它也将是一个 `<input>` 控件：

```javascript
<script language="JavaScript">
function createNewElements()
{
    var newDiv, newTextField, newText, newButton;

    newDiv = document.createElement("div");
    newDiv.id = "NewDIV";

    newTextField = document.createElement("input");
    newTextField.type = "text";
    newTextField.value = "Hello!";

    newButton = document.createElement("input");
    .
    .
    .
}
</script>
```

我们将通过将其 `type` 属性设置为 "button" 并将其标题设置为 "New Button" 来使其成为一个按钮：

```javascript
<script language="JavaScript">
function createNewElements()
{
    var newDiv, newTextField, newText, newButton;

    newDiv = document.createElement("div");
    newDiv.id = "NewDIV";

    newTextField = document.createElement("input");
    newTextField.type = "text";
    newTextField.value = "Hello!";

    newButton = document.createElement("input");
    newButton.type = "button";
    newButton.value = "New Button";
    .
    .
    .
}
</script>
```

现在我们可以创建一些代码——一个名为 `sayHello` 的函数，当按钮被点击时将调用该函数。这个新函数将调用 JavaScript 的 `alert` 函数来显示一个提示对话框，上面写着 "Hello!"：

```javascript
<script language="JavaScript">
function createNewElements()
{
    var newDiv, newTextField, newText, newButton;

    newDiv = document.createElement("div");
    newDiv.id = "NewDIV";

    newTextField = document.createElement("input");
    newTextField.type = "text";
    newTextField.value = "Hello!";

    newButton = document.createElement("input");
    newButton.type = "button";
    newButton.value = "New Button";
    .
    .
    .
}

function sayHello()
{
    alert("Hello!");
}
</script>
```

我们可以通过将 `sayHello` 函数赋值给按钮的 `onclick` 属性，将 `sayHello` 函数连接到新按钮，方式如下：

```javascript
<script language="JavaScript">
function createNewElements()
{
    var newDiv, newTextField, newText, newButton;

    newDiv = document.createElement("div");
    newDiv.id = "NewDIV";

    newTextField = document.createElement("input");
    newTextField.type = "text";
    newTextField.value = "Hello!";

    newButton = document.createElement("input");
    newButton.type = "button";
    newButton.value = "New Button";
    newButton.onclick = sayHello;
    .
    .
    .
}

function sayHello()
{
    alert("Hello!");
}
</script>
```

## 第8章：使用 Ajax 处理动态 HTML

现在是时候创建文本节点了，我们可以使用 `createTextNode` 方法来完成：

```javascript
<script language="JavaScript">
function createNewElements()
{
    var newDiv, newTextfield, newText, newButton;

    newDiv = document.createElement("div");
    newDiv.id = "NewDIV";

    newTextfield = document.createElement("input");
    newTextfield.type = "text";
    newTextfield.value = "Hello!";

    newButton = document.createElement("input");
    newButton.type = "button";
    newButton.value = "New Button";
    newButton.onclick = sayHello;

    newText = document.createTextNode("Here is the new text.");
    .
    .
    .
}
</script>
```

太好了，我们已经创建了一个文本字段、一个按钮和一个文本节点。下一步是将所有这些项目安装到我们创建的 `<div>` 元素 `newDiv` 中，我们将使用动态 HTML 的 `insertBefore` 方法。使用此方法可以将新元素插入到网页中，传递要插入的新元素对象以及要在其之前插入新元素的当前元素对象。在这种情况下，我们将把新对象插入到我们创建的 `<div>` 元素中——并且由于 `<div>` 元素中没有现有对象可以放在新对象之前，我们将为该参数传递 `null` 值。以下是我们如何将新按钮、文本字段和文本节点插入到我们创建的 `<div>` 元素中：

```javascript
<script language="JavaScript">
function createNewElements()
{
    var newDiv, newTextfield, newText, newButton;

    newDiv = document.createElement("div");
    newDiv.id = "NewDIV";

    newTextfield = document.createElement("input");
    newTextfield.type = "text";
    newTextfield.value = "Hello!";

    newButton = document.createElement("input");
    newButton.type = "button";
    newButton.value = "New Button";
    newButton.onclick = sayHello;

    newText = document.createTextNode("Here is the new text.");

    newDiv.insertBefore(newButton, null);
    newDiv.insertBefore(newTextfield, null);
    newDiv.insertBefore(newText, null);
    .
    .
    .
}
</script>
```



接下来，我们将包含新文本字段、按钮和文本节点的`<div>`元素插入到网页中。我们可以通过将`<body>`元素引用为`document.body`，将该`<div>`元素插入到页面的`<body>`元素中，方式如下：

```javascript
<script language="JavaScript">
function createNewElements()
{
    var newDiv, newTextfield, newText, newButton;

    newDiv = document.createElement("div");
    newDiv.id = "NewDIV";

    newTextfield = document.createElement("input");
    newTextfield.type = "text";
    newTextfield.value = "Hello!";

    newButton = document.createElement("input");
    newButton.type = "button";
    newButton.value = "New Button";
    newButton.onclick = sayHello;

    newText = document.createTextNode("Here is the new text.");

    newDiv.insertBefore(newButton, null);
    newDiv.insertBefore(newTextfield, null);
    newDiv.insertBefore(newText, null);

    document.body.insertBefore(newDiv, null);
}
</script>
```

290 Ajax：入门指南

![img/2cd265cf0a64e9b4b91ab611753cd5d5_309_0.png](img/2cd265cf0a64e9b4b91ab611753cd5d5_309_0.png)

图8-11 动态创建新元素

![img/2cd265cf0a64e9b4b91ab611753cd5d5_309_1.png](img/2cd265cf0a64e9b4b91ab611753cd5d5_309_1.png)

图8-12 点击按钮会显示一个提示对话框。

就是这样——我们已经创建了三个新对象，将它们插入到一个`<div>`元素中，并将该`<div>`元素插入到网页中。你可以在图8-11中看到结果；当用户点击按钮时，会添加一个新的按钮、文本字段和文本节点。

这个按钮也是功能性的——点击它会显示图8-12中你看到的提示对话框。非常好。

这让你对创建新的 HTML 元素并将其添加到网页有了一个概览。Ajax 开发者发现自己经常需要从头创建的项目之一是 HTML 表格，例如当他们从数据库下载数据并需要显示它时。事实上，创建和编辑表格是如此常见的事情，以至于在 Internet Explorer 和 Firefox 类型浏览器都支持的动态 HTML 中，有专门的支持。

### 动态编辑表格

在动态 HTML 中，表格对象（即对应于`<table>`元素的对象）具有以下可用于编辑其内容的属性和方法：

- `tableObject.rows(index)`返回表格中行的集合（数组）。
- `tableObject.insertRow(index)`插入一个新行。返回插入的`<tr>`元素（将是空的），或者失败时返回`null`。如果未提供`index`，则`<tr>`元素将被插入到末尾。
- `tableObject.deleteRow(index)`删除一行。索引值表示要删除的行的索引。

以下是表格行对象（即对应于`<tr>`元素的对象）的属性和方法：

- `tableObject.cells(index)`返回该行中单元格的集合（数组）。
- `tableObject.row(index)`返回该行的行索引。对于插入和删除行很有用。
- `tableObject.insertCell(index)`插入一个新单元格并返回插入的`<td>`元素（该元素将为空），如果失败则返回`null`。如果未提供索引，则`<td>`元素将插入到行的末尾。
- `tableObject.deleteCell(index)`删除一个单元格。索引值表示要删除的单元格集合中的位置。

让我们通过一个示例`editTable.html`来实践即时编辑表格。这个示例将通过单击按钮来添加新行以编辑表格（它将在 Internet Explorer 和 Firefox 中工作）。我们首先显示一个 HTML 表格：

```html
<body>
    <center>
        <h1>
            Editing HTML Tables
        </h1>

        <table id="table1" border="2">
            <tr>
                <td>Fe</td>
                <td>Fi</td>
                <td>Fo</td>
                <td>Fum</td>
            </tr>
            <tr>
                <td>Fe</td>
                <td>Fi</td>
                <td>Fo</td>
                <td>Fum</td>
            </tr>
            <tr>
                <td>Fe</td>
                <td>Fi</td>
                <td>Fo</td>
                <td>Fum</td>
            </tr>
        </table>
        .
        .
        .
    </center>
</body>
```

292 Ajax：初学者指南

注意，我们已经给表格分配了一个 ID“table1”，这将允许我们在 JavaScript 中访问该表格。让我们添加一个标题为“添加新行”的按钮，该按钮连接到一个名为`createRow`的 JavaScript 函数：

```html
<body>
<center>
    <h1>
        Editing HTML Tables
    </h1>
    <table id="table1" border="2">
        <tr>
            <td>Fe</td>
            <td>Fi</td>
            <td>Fo</td>
            <td>Fum</td>
        </tr>
        <tr>
            <td>Fe</td>
            <td>Fi</td>
            <td>Fo</td>
            <td>Fum</td>
        </tr>
        <tr>
            <td>Fe</td>
            <td>Fi</td>
            <td>Fo</td>
            <td>Fum</td>
        </tr>
    </table>
    <br>
    <input type="button" value="Add a new row"
           onclick="createRow()">
</center>
</body>
```

在`createRow`函数中，我们可以获取与`table1`对应的对象：

```javascript
<script language="javascript">
    function createRow()
    {
        var table1 = document.getElementById("table1");
        .
        .
        .
    }
</script>
```

## 第8章：使用Ajax处理动态HTML

然后我们调用表格对象的`insertRow`方法向表格中插入一个新行——该方法返回新行对象，以便我们可以对它进行操作，向该行添加单元格：

```javascript
<script language="javascript">
    function createRow()
    {
        var table1 = document.getElementById("table1");
        var newRow = table1.insertRow(3);
        .
        .
        .
    }
</script>
```

注意，我们在这里插入的是第3行，因为表格已经有了三行——即第0行、第1行和第2行。现在我们有了一个新行对象可供操作，我们将使用行对象的`insertCell`方法向其添加单元格。

表格中的每一行都有四个单元格：单元格0、1、2和3。你可以用以下方式向新创建的行添加单元格0：

```javascript
<script language="javascript">
    function createRow()
    {
        var table1 = document.getElementById("table1");
        var newRow = table1.insertRow(3);

        var newCell = newRow.insertCell(0);
        .
        .
        .
    }
</script>
```

`insertCell`方法返回新的单元格对象。我们如何向这个新单元格添加数据？我们可以使用它的`innerHTML`属性，就像我们之前经常对`<div>`元素所做的那样：

```javascript
<script language="javascript">
    function createRow()
    {
        var table1 = document.getElementById("table1");
        var newRow = table1.insertRow(3);

        var newCell = newRow.insertCell(0);
        newCell.innerHTML = "Fe";
        .
        .
        .
    }
</script>
```

很好——我们已经能够向刚刚插入新行的单元格中插入文本数据了。我们也可以创建该行中的其他三个单元格并同样向它们添加数据：

```javascript
<script language="javascript">
	function createRow()
	{
		var table1 = document.getElementById("table1");
		var newRow = table1.insertRow(3);

		var newCell = newRow.insertCell(0);
		newCell.innerHTML = "Fe";

		newCell = newRow.insertCell(1);
		newCell.innerHTML = "Fi";

		newCell = newRow.insertCell(2);
		newCell.innerHTML = "Fo";

		newCell = newRow.insertCell(3);
		newCell.innerHTML = "Fum";
	}
</script>
```

很好——以下是完整的示例`editTable.html`：

```html
<html>
	<head>
		<title>
			Editing HTML Tables
		</title>

		<script language="javascript">
			function createRow()
			{
				var table1 = document.getElementById("table1");
				var newRow = table1.insertRow(3);

				var newCell = newRow.insertCell(0);
				newCell.innerHTML = "Fe";

				newCell = newRow.insertCell(1);
				newCell.innerHTML = "Fi";

				newCell = newRow.insertCell(2);
				newCell.innerHTML = "Fo";

				newCell = newRow.insertCell(3);
				newCell.innerHTML = "Fum";
			}
		</script>
	</head>

	<body>
		<center>
			<h1>
				Editing HTML Tables
			</h1>

			<table id="table1" border="2">
				<tr>
					<td>Fe</td>
					<td>Fi</td>
					<td>Fo</td>
					<td>Fum</td>
				</tr>
				<tr>
					<td>Fe</td>
					<td>Fi</td>
					<td>Fo</td>
					<td>Fum</td>
				</tr>
				<tr>
					<td>Fe</td>
					<td>Fi</td>
					<td>Fo</td>
					<td>Fum</td>
				</tr>
			</table>

			<br>

			<input type="button" value="Add a new row"
			       onclick="createRow()">

		</center>
	</body>
</html>
```

你可以在图8-13中看到这个示例的效果，其中表格以原始状态显示。

296 Ajax：初学者指南

![图8-13：editTable.html中的原始表格](img/2cd265cf0a64e9b4b91ab611753cd5d5_315_0.png)

**图8-13** `editTable.html`中的原始表格

当你单击按钮时，一个新行会出现在表格的底部，如图8-14所示。

酷，现在你知道如何即时编辑表格了。这对于 Ajax 应用程序来说是一项非常有用的技能，因为你可以更新表格——甚至用新数据重写它——而无需刷新页面。

![图8-14：在editTable.html中添加新行](img/2cd265cf0a64e9b4b91ab611753cd5d5_315_1.png)

**图8-14** 在`editTable.html`中添加新行

## 第8章：使用Ajax处理动态HTML

### 动手实践：即时删除表格行

要真正做到能够即时编辑 HTML 表格，你需要知道如何删除行以及添加行。尝试使用`deleteRow`方法，让用户在添加新行后能够删除一行。代码如下所示：

```html
<html>
	<head>
		<title>
			Editing HTML Tables
		</title>
		<script language="javascript">
			function createRow()
			{
				var table1 = document.getElementById("table1");
				var newRow = table1.insertRow(3);

				var newCell = newRow.insertCell(0);
				newCell.innerHTML = "Fe";

				newCell = newRow.insertCell(1);
				newCell.innerHTML = "Fi";

				newCell = newRow.insertCell(2);
				newCell.innerHTML = "Fo";

				newCell = newRow.insertCell(3);
				newCell.innerHTML = "Fum";
			}

			function removeRow()
			{
				var table1 = document.getElementById("table1");
				table1.deleteRow(3);
			}
		</script>
	</head>

	<body>
		<center>
			<h1>
				Editing HTML Tables
			</h1>
			<table id="table1" border="2">
				<tr>
					<td>Fe</td>
```

## 使用`document.write`将文档写入浏览器

你应该了解的另一个动态 HTML 方法是`document.write`方法，它允许你从 JavaScript 向网页写入内容。与你在本章前面看到的技术不同，`document.write`旨在一次性写入整个页面，而不仅仅是更新页面的某些部分。在 Ajax 应用程序中使用`document.write`，你可以在写入网页之前从服务器下载并检查数据，并根据该数据写入不同的网页。



这是一个名为`restaurant.html`的示例，展示了`document.write`如何响应当前条件。在这个例子中，我们将为一家餐厅创建一个网页，根据一天中的不同时间显示不同的菜单——早餐、午餐或晚餐。这个网页将完全由 JavaScript 写入，因此它的`<body>`元素是空的：

```html
<body>
</body>
```

在`<script>`元素中，我们首先通过创建一个 JavaScript`Date`对象并使用其`getHours`方法来确定当前的小时数：

```javascript
<script language="JavaScript">
    var currentDate = new Date();
    var currentHour = currentDate.getHours();
    .
    .
    .
</script>
```

接下来，我们可以使用`document.write`写入一个欢迎人们来到餐厅的标题（“欢迎光临我们的餐厅”）：

```javascript
<script language="JavaScript">
    var currentDate = new Date();
    var currentHour = currentDate.getHours();
    document.write( "<center>");
    document.write( "<h1>");
    document.write("Welcome to Our Restaurant");
    document.write( "</h1>");
    document.write( "</center>");
    .
    .
    .
</script>
```

这就是它的工作方式——你使用`document.write`向网页写入内容。你可以检查当前的小时数，并据此写入相应的网页。例如，如果餐厅当前已关门，你可以写入反映这一点的网页：

```javascript
<script language="JavaScript">
    var currentDate = new Date();
    var currentHour = currentDate.getHours();
    document.write( "<center>");
    document.write( "<h1>");
    document.write("Welcome to Our Restaurant");
    document.write( "</h1>");
    document.write( "</center>");

    if (currentHour < 5 || currentHour > 23){
        document.write( "<center>");
        document.write( "<h1>");
        document.write( "Sorry, we are currently closed." );
        document.write( "</h1>");
        document.write( "</center>");
    }
    .
    .
    .
</script>
```

或者，如果是早餐时间，你可以在，比如说，一个 HTML 表格中显示早餐菜单：

```javascript
<script language="JavaScript">
    var currentDate = new Date();
    var currentHour = currentDate.getHours();
    document.write( "<center>");
    document.write( "<h1>");
    document.write("Welcome to Our Restaurant");
    document.write( "</h1>");
    document.write( "</center>");

    if (currentHour < 5 || currentHour > 23){
        document.write( "<center>");
        document.write( "<h1>");
        document.write( "Sorry, we are currently closed." );
        document.write( "</h1>");
        document.write( "</center>");
    }

    if (currentHour > 6 && currentHour < 12 ) {
        document.write( "<center>");
        document.write( "<h2><i>We're now serving breakfast!</i></h2>");
        document.write( "<table border bgcolor='aqua'>");
        document.write( "<tr><th colspan = 2>Our Breakfast Menu</th></tr>");
        document.write( "<tr><td>Fried Eggs</td><td>$3.50</td></tr>");
        document.write( "<tr><td>Boiled eggs</td><td>$3.00</td></tr>");
        document.write( "<tr><td>Waffles</td><td>$2.00</td></tr>");
        document.write("<tr><td>Gruel</td><td>$2.50</td></tr>");
        document.write( "<tr><td>Spinach</td><td>$2.50</td></tr>");
        document.write( "</table>");
        document.write( "</center>");
    }
    .
    .
    .
</script>
```

## 第 8 章：使用 Ajax 处理动态 HTML

这是完整的`document.write`示例，`restaurant.html`：

```html
<html>
    <head>
        <script language="JavaScript">
            var currentDate = new Date();
            var currentHour = currentDate.getHours();
            document.write( "<center>");
            document.write( "<h1>");
            document.write("Welcome to Our Restaurant");
            document.write( "</h1>");
            document.write( "</center>");

            if (currentHour < 5 || currentHour > 23){
                document.write( "<center>");
                document.write( "<h1>");
                document.write( "Sorry, we are currently closed." );
                document.write( "</h1>");
                document.write( "</center>");
            }

            if (currentHour > 6 && currentHour < 12 ) {
                document.write( "<center>");
                document.write(
                    "<h2><i>We're now serving breakfast!</i></h2>");
                document.write( "<table border bgcolor='aqua'>");
                document.write(
                    "<tr><th colspan = 2>Our Breakfast Menu</th></tr>");
                document.write(
                    "<tr><td>Fried Eggs</td><td>$3.50</td></tr>");
                document.write(
                    "<tr><td>Boiled eggs</td><td>$3.00</td></tr>");
                document.write(
                    "<tr><td>Waffles</td><td>$2.00</td></tr>");
                document.write("<tr><td>Gruel</td><td>$2.50</td></tr>");
                document.write(
                    "<tr><td>Spinach</td><td>$2.50</td></tr>");
                document.write( "</table>");
                document.write( "</center>");
            }

            if ( currentHour >= 12 && currentHour < 17 ) {
                document.write( "<center>");
                document.write(
                    "<h2><i>We're now serving lunch!</i></h2>");
                document.write( "<table border bgcolor='aqua'>");
                document.write(
                    "<tr><th colspan = 2>Our Lunch Menu</th></tr>");
                document.write(
                    "<tr><td>Ham Sandwich</td><td>$4.50</td></tr>");
                document.write(
                    "<tr><td>Pickle Sandwich</td><td>$4.50</td></tr>");
                document.write(
                    "<tr><td>Peacock Sandwich</td><td>$4.00</td></tr>");
                document.write(
                    "<tr><td>Alligator Nuggets</td><td>$6.00</td></tr>");
                document.write(
                    "<tr><td>Python Salad</td><td>$5.50</td></tr>");
                document.write(
                    "<tr><td>Rattler Soup</td><td>$2.50</td></tr>");
                document.write("</table>");
                document.write("</center>");
            }

            if ( currentHour >= 17 && currentHour < 22 ) {
                document.write("<center>");
                document.write(
                    "<h2><i>We're now serving dinner!</i></h2>");
                document.write(
                    "<table border bgcolor='aqua'>");
                document.write(
                    "<tr><th colspan = 2>Our Dinner Menu</th></tr>");
                document.write(
                    "<tr><td>Filet Mignon</td><td>$9.00</td></tr>");
                document.write(
                    "<tr><td>Lobster Thermador</td><td>$8.50</td></tr>");
                document.write(
                    "<tr><td>Strip Steak</td><td>$8.00</td></tr>");
                document.write(
                    "<tr><td>Tube Steak</td><td>$4.50</td></tr>");
                document.write(
                    "<tr><td>Baked Potato</td><td>$3.50</td></tr>");
                document.write(
                    "<tr><td>Broiled Potato</td><td>$2.50</td></tr>");
                document.write(
                    "<tr><td>Eggplant Drops</td><td>$2.50</td></tr>");
                document.write("</table>");
                document.write("</center>");
            }
        </script>
    </head>
    <body>
    </body>
</html>
```

## 第 8 章：使用 Ajax 处理动态 HTML

303

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_322_0.png)

图 8-15 一份取决于时间的餐厅菜单

你可以在图 8-15 中看到`restaurant.html`的运行效果，它正在显示午餐菜单。关于`document.write`的关键点在于：它真的只能用于一次性写入整个页面；无法只写入页面的特定部分。当你使用`document.write`时，它会为写入“打开”一个网页，而当该网页显示后，就“关闭”了写入。如果你尝试在已关闭的网页上使用`document.write`，该页面会再次被“打开”——这意味着它被擦除并变为空白。如果你想重写整个页面，这没问题，但如果你只想更新该页面特定部分的数据，这就不好了。

## 第 9 章

### 用 Ajax 介绍 PHP

## 关键技能与概念

- 将 PHP 与 HTML 混合使用
- 向浏览器输出文本
- 使用变量
- 使用数组
- 使用`if`语句
- 使用`for`循环
- 使用`while`循环
- 使用`foreach`循环

当然，你可以使用 Ajax 从服务器下载静态文本和 XML 文件，但这样做并没有太大优势。如果你的数据不变化，为什么不直接将其存储在你的网页中呢？Ajax 的真正威力在于你的网页与服务器交互，并且服务器可以发送变化的数据。这就是为什么 Ajax 通常与某种在服务器上运行的编程语言一起使用——而当今与 Ajax 一起使用的最常见的服务器端语言就是 PHP。

因此，本章及接下来的两章将集中介绍与 Ajax 相关的 PHP。你将在这些章节中获得良好的 PHP 工作知识，为你想要进行的几乎所有 Ajax 工作打下坚实的基础。

### PHP 入门

要运行 PHP，你必须拥有一个支持它的服务器。你可以寻找一个托管 PHP 的互联网服务提供商（ISP），或者你可以从`www.php.net/`自行安装。要运行 PHP 代码，你必须在服务器上将你的文件扩展名设置为`.php`（请记住，如果你使用的是 WordPad，保存时应将文件名用引号括起来，这样 WordPad 就不会为你的文件添加`.txt`扩展名）。

在文件内部，你可以在标记`<?php`和`?>`之间包含 PHP 代码：

```
<?php
.
.
.
.
[将你的 PHP 代码放在这里]
.
.
.
?>
```



然后，当你通过 Web 浏览器访问服务器上的文件时，服务器会看到文件扩展名为`.php`，并检查其中是否有任何 PHP 代码。如果服务器找到 PHP 代码，它就会运行该代码，该代码可以将结果发送回浏览器。

这是一个运行 PHP 内置函数`phpinfo`的示例，它显示一个关于服务器运行的 PHP 版本的 HTML 数据表。此示例将被命名为`phpinfo.php`。

我们也可以在 PHP 文件中包含 HTML，在`phpinfo.php`中，我们希望向浏览器发送一个网页，所以让我们从一些 HTML 开始：

```
<html>
    <head>
        <title>
            运行 phpinfo
        </title>
    </head>

    <body>
        <h1>
            运行 phpinfo
        </h1>
        .
        .
        .
    </body>
</html>
```

现在我们可以添加 PHP 标记，告诉服务器有 PHP 代码需要运行：

```
<html>
    <head>
        <title>
            运行 phpinfo
        </title>
    </head>

    <body>
        <h1>
            运行 phpinfo
        </h1>
        <?php
            .
            .
            .
        ?>
    </body>
</html>
```

308 Ajax：入门指南

在这种情况下，我们将运行的唯一 PHP 是`phpinfo`函数，它将显示一个 HTML 表格：

```
<html>
    <head>
        <title>
            运行 phpinfo
        </title>
    </head>

    <body>
        <h1>
            运行 phpinfo
        </h1>
        <?php
            phpinfo();
        ?>
    </body>
</html>
```

正如你在图 9-1 中看到的，`phpinfo`函数确实运行了，结果显示在图中。不错——我们本章的第一个 PHP 示例已成功运行。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_327_0.png)

图 9-1 运行 phpinfo 函数

### 将文本返回给浏览器

当然，除非你能将数据发送回浏览器，否则在服务器上运行 PHP 脚本用处不大，你的 Ajax 应用程序可以在 JavaScript 中使用这些数据。在 PHP 中，将数据发送回浏览器的主要函数是`echo`函数。

这是一个示例`echo.php`，它应用了这个函数。我们将用一些 HTML 来开始`echo.php`：

```
<html>
    <head>
        <title>
            输出文本
        </title>
    </head>

    <body>
        <h1>
            输出文本
        </h1>
        .
        .
        .
    </body>
</html>
```

接下来，我们将在一个 PHP 块中添加对`echo`函数的调用——我们只需将要发送回浏览器的文本传递给`echo`函数（`echo.php`）：

```
<html>
    <head>
        <title>
            输出文本
        </title>
    </head>

    <body>
        <h1>
            输出文本
        </h1>
        <?php
            echo("来自 PHP 的问候。");
        ?>
    </body>
</html>
```

你可以在图 9-2 中看到结果，我们发送回浏览器的文本确实出现在浏览器中。很好。

Ajax：入门指南

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_329_0.png)

图 9-2 使用 echo 函数

### 动手试试：向浏览器发送 HTML

除了简单文本，你还可以使用`echo`函数将 HTML 发送回浏览器。试试这个：使`echo.php`中的消息在浏览器中以粗体、斜体字体显示，使用 HTML 标签`<b>`和`<i>`。

代码将是这样的：

```
<html>
    <head>
        <title>
            输出文本
        </title>
    </head>

    <body>
        <h1>
            输出文本
        </h1>
        <?php
            echo("<b><i>来自 PHP 的问候。</i></b>");
        ?>
    </body>
</html>
```

那么，如何将 XML 发送回浏览器呢？

### 将 XML 返回给浏览器

发送简单文本回浏览器更容易，但毕竟 Ajax 中的 *x* 代表 XML。让我们通过一个新的示例`xml.php`来看看如何从 PHP 脚本将 XML 发送回浏览器。

假设我们想将此 XML 文档发送给浏览器：

```
<?xml version="1.0" ?>
<document>
  <item>Raspberry</item>
  <item>Strawberry</item>
  <item>Blueberry</item>
  <item>Tomato</item>
</document>
```

因为这是 XML，我们不能发送任何 HTML 回浏览器，所以这个示例将全是 PHP，没有 HTML：

```
<?php
.
.
.
?>
```

我们首先设置服务器发送到浏览器的头部为`Content-Type`头部，设置为 "text/xml"，这告诉浏览器此文档是 XML（如果你不设置此头部，默认为 HTML）：

```
<?php
header('Content-Type: text/xml');
.
.
.
?>
```

每个（合法的）XML 文档都以 XML 声明开头：

```
<?xml version="1.0" ?>
<document>
  <item>Raspberry</item>
  <item>Strawberry</item>
```

### 专家问答

**问：** 为什么我们将`Content-Type`头部设置为 "text/xml"？

**答：** 要将 XML 发送回浏览器，你需要通过将`Content-Type`头部设置为 MIME（多用途互联网邮件扩展）类型 "text/xml" 来告诉浏览器数据的格式。

**问：** 谁设定数据格式的 MIME 类型，还有哪些其他类型可用？

**答：** 数据格式由互联网号码分配机构 (IANA) 命名并赋予 MIME 类型。你可以在 www.iana.org/assignments/media-types/ 找到所有可用的 MIME 类型。示例包括用于 Rich Text Format 文本的 "text/rtf"，以及用于 HTML 的 "text/html"，后者是 Web 服务器的默认类型。

```
<item>Blueberry</item>

<item>Tomato</item>

</document>
```

我们可以像这样将这样的声明输出到浏览器：

```
<?php
    header('Content-Type: text/xml');
    echo '<?xml version="1.0" ?>';
    .
    .
    .
?>
```

接下来，我们将文档元素的起始标签（名为`<document>`）发送回浏览器：

```
<?xml version="1.0" ?>
<document>

    <item>Raspberry</item>

    <item>Strawberry</item>

    <item>Blueberry</item>

    <item>Tomato</item>

</document>
```

# 第 9 章：通过 Ajax 介绍 PHP 313

以下是 xml.php 中的代码示例：

```
<?php
    header('Content-Type: text/xml');
    echo '<?xml version="1.0" ?>';

    echo '<document>';
        .
        .
        .
?>
```

接下来是实际的 XML`<item>`元素：

```
<?xml version="1.0" ?>
<document>
    <item>Raspberry</item>

    <item>Strawberry</item>

    <item>Blueberry</item>

    <item>Tomato</item>
</document>
```

这些 XML`<item>`元素在 xml.php 中的呈现方式如下：

```
<?php
    header('Content-Type: text/xml');
    echo '<?xml version="1.0" ?>';

    echo '<document>';

    echo '<item>';
    echo 'Raspberry';
    echo '</item>';

    echo '<item>';
    echo 'Strawberry';
    echo '</item>';

    echo '<item>';
    echo 'Blueberry';
    echo '</item>';

    echo '<item>';
    echo 'Tomato';
    echo '</item>';
        .
        .
        .
?>
```

最后，我们关闭`<document>`元素：

```
<?php
header('Content-Type: text/xml');
echo '<?xml version="1.0" ?>';

echo '<document>';

echo '<item>';
echo 'Raspberry';
echo '</item>';

echo '<item>';
echo 'Strawberry';
echo '</item>';

echo '<item>';
echo 'Blueberry';
echo '</item>';

echo '<item>';
echo 'Tomato';
echo '</item>';

echo '</document>';
?>
```

很好——现在我们已经通过 PHP 脚本创建并返回了 XML（参见图 9-3）。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_333_0.png)

**图 9-3** 查看从 xml.php 发送的 XML

# 为 PHP 代码添加注释

注释是你在程序中添加的说明性文字，用于增强代码的可读性。服务器会忽略注释内容，但它们能帮助你向他人（或未来的自己）解释程序的功能。

PHP 中有三种注释类型。第一种是**单行注释**，以`//`开头，表示 PHP 不读取该行剩余内容。示例如下：

```
<?php
header('Content-Type: text/xml');
echo '<?xml version="1.0" ?>';

//Print the document element
echo '<document>';

//Print the elements
echo '<item>';
echo 'Raspberry';
echo '</item>';

echo '<item>';
echo 'Strawberry'; //Strawberries are good!
echo '</item>';

echo '<item>';
echo 'Blueberry';
echo '</item>';

echo '<item>';
echo 'Tomato';
echo '</item>';

echo '</document>';
?>
```

请注意，每个注释不一定独占一行；你可以在行尾添加注释，就像上面关于草莓的注释一样。第二种 PHP 注释同样是单行注释，但使用井号符号（`#`）而非`//`开头：

```
<?php
header('Content-Type: text/xml');
echo '<?xml version="1.0" ?>';

#Print the document element
echo '<document>';
```

```
#Print the elements
echo '<item>';
echo 'Raspberry';
echo '</item>';

echo '<item>';
echo 'Strawberry';  #Strawberries are good!
echo '</item>';

echo '<item>';
echo 'Blueberry';
echo '</item>';

echo '<item>';
echo 'Tomato';
echo '</item>';

echo '</document>';
?>
```

除了这两种单行注释，PHP 还支持**多行注释**，使用`/*`（开始注释）和`*/`（结束注释）标记。PHP 会忽略`/*`和`*/`之间的所有文本。以下是将单行注释转换为多行注释的示例：

```
<?php
header('Content-Type: text/xml');
echo '<?xml version="1.0" ?>';

/* Print the
document
element */
echo '<document>';

/* Print
the
elements */
echo '<item>';
echo 'Raspberry';
echo '</item>';

echo '<item>';
/* Strawberries are good! */
echo 'Strawberry';
echo '</item>';

echo '<item>';
echo 'Blueberry';
echo '</item>';

echo '<item>';
echo 'Tomato';
echo '</item>';

echo '</document>';
?>
```

# 在变量中存储数据

如你所知，变量是内存中数据的占位符。在 PHP 中使用变量与 JavaScript 中一样简单。PHP 变量名以美元符号开头，例如：`$numberOfBooks`或`$moneyOwedToMe`。与 JavaScript 类似，你可以使用 PHP 变量存储数字或文本字符串。

# 在变量中存储数字

以下是变量示例`variables.html`，展示如何存储数字。本例将跟踪苹果数量，首先将两个苹果存储到变量`$apples`中：

```
<html>
    <head>
        <title>
            Storing numbers in variables
        </title>
    </head>
    <body>
        <h1>
            Storing numbers in variables
        </h1>

        <?php
            echo "I'm setting the number of apples to 2...<br>";

            $apples = 2;
            .
            .
            .
        ?>

    </body>
</html>
```

现在`$apples`的值为 2，你可以通过`echo`语句在浏览器中显示其内容进行验证：

```
<html>
    <head>
        <title>
            Storing numbers in variables
        </title>
    </head>

    <body>
        <h1>
            Storing numbers in variables
        </h1>

        <?php
            echo "I'm setting the number of apples to 2...<br>";

            $apples = 2;

            echo "The current number of apples is ", $apples, ".<br>";
            .
            .
            .
        ?>

    </body>
</html>
```

请注意其工作原理：如果用逗号分隔多个项目，你可以将它们全部输出到浏览器。现在，你可以增加三个苹果，并输出新的总数（`variables.php`）：



```html
<html>
    <head>
        <title>
            Storing numbers in variables
        </title>
    </head>

    <body>
        <h1>
            Storing numbers in variables
        </h1>

        <?php
            echo "I'm setting the number of apples to 2...<br>";

            $apples = 2;

            echo "The current number of apples is ", $apples, ".<br>";

            echo "Now I'm adding three more apples...<br>";

            $apples = $apples + 3;

            echo "The number of apples I have now is ", $apples, "<br>";
        ?>

    </body>
</html>
```

这就是全部操作——你可以在图 9-4 中查看结果。

# 在变量中存储文本字符串

除了数字，你还可以在 PHP 变量中存储字符串，如下例所示：

```php
$name = "Eythmoid Studge, Jr.";
```

在 JavaScript 中，你可以使用 `+` 运算符连接（即拼接）字符串，但在 PHP 中，你需要使用点（`.`）运算符：

```php
$name = "Eythmoid" . " Studge," . " Jr.";
```

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_338_0.png)

你也可以使用 PHP 中许多内置的字符串函数来处理字符串。例如，`strtoupper` 函数将文本转换为大写字母。语句

```php
$name = strtoupper("Eythmoid Studge, Jr.");
```

会将 `"EYTHMOID STUDGE, JR."` 存入 `$name`。下一个示例 `string.php` 使用以下常用的字符串函数，帮助你开始学习 PHP 字符串操作：

- `trim` 删除字符串开头和结尾的空格
- `substr` 从字符串中提取子字符串
- `strlen` 返回字符串的长度
- `substr_replace` 替换字符串中的文本
- `strtoupper` 将整个字符串转换为大写字母

我们将从带有前导空格的字符串 `" Good old PHP!"` 开始，并使用 `trim` 函数删除这些空格——这是一个非常实用的函数，因为用户常常会输入多余的前导或尾随空格：

```php
<html>
    <head>
        <title>
            Working with PHP strings
        </title>
    </head>

    <body>
        <h1>
            Working With PHP strings
        </h1>

        <?php
            echo trim("    Good old PHP!"), "<br>";
            .
            .
            .
        ?>

    </body>

</html>
```

接下来，我们将使用 `substr` 函数从字符串中提取子字符串。你需要向该函数传递原始字符串、子字符串的起始位置（基于 0）以及子字符串的长度。例如，要从 `"Good old PHP!"` 中提取 `"PHP"`，可以这样做：

```php
<?php
    echo trim("     Good old PHP!"), "<br>";

    echo substr("Good old PHP!", 9, 3), "<br>";

?>
```

你可以使用 `strlen` 函数检查字符串的长度，该函数返回传入字符串的字符数：

```php
<?php
    echo trim("     Good old PHP!"), "<br>";

    echo substr("Good old PHP!", 9, 3), "<br>";

    echo "'PHP' starts at position ", strpos("Good old PHP!",
        "PHP"), "<br>";

    echo "'Good old PHP!' is ", strlen("Good old PHP!"), "
        characters long.<br>";

?>
```

你还可以使用 `substr_replace` 函数将字符串中的子字符串替换为另一个子字符串。你需要向该函数传递要编辑的字符串、要插入的新字符串、插入位置以及要替换的字符数。以下是如何使用 `substr_replace` 将 `"Good old PHP!"` 转换为 `"Great old PHP!"` 的示例：

```php
<?php
    echo trim("     Good old PHP!"), "<br>";

    echo substr("Good old PHP!", 9, 3), "<br>";

    echo "'PHP' starts at position ", strpos("Good old PHP!",
        "PHP"), "<br>";

    echo "'Good old PHP!' is ", strlen("Good old PHP!"), "
        characters long.<br>";

?>
```

## 322 Ajax：初学者指南

```php
echo substr_replace("Good old PHP!", "Great", 0, 4), "<br>";
.
.
.
?>
```

最后，我们使用 `strtoupper` 函数将 `"Good old PHP!"` 转换为全大写字母：

```php
<?php
	echo trim("    Good old PHP!"), "<br>";

	echo substr("Good old PHP!", 9, 3), "<br>";

	echo "'PHP' starts at position ", strpos("Good old PHP!",
		"PHP"), "<br>";

	echo "'Good old PHP!' is ", strlen("Good old PHP!"), "
		characters long.<br>";

	echo substr_replace("Good old PHP!", "Great", 0, 4), "<br>";

	echo strtoupper("Good old PHP!"), "<br>";
?>
```

你可以在图 9-5 中看到这个名为 `string.php` 的示例在运行。PHP 中提供了许多字符串函数，你可以在表 9-1 中找到一个示例。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_341_0.png)

**图 9-5** 在 `string.php` 中使用字符串函数

第 9 章：用 Ajax 介绍 PHP 323

| 函数 | 描述 |
| :--- | :--- |
| `addslashes` | 用反斜杠引用字符串 |
| `bin2hex` | 将二进制数据转换为十六进制表示 |
| `chop` | `rtrim` 函数的别名 |
| `chr` | 根据给定的 ASCII 码返回特定字符 |
| `chunk_split` | 将字符串分割成更小的块 |
| `convert_cyr_string` | 从一种西里尔字符集转换到另一种 |
| `count_chars` | 返回关于字符串中字符的信息 |
| `crc32` | 计算字符串的 crc32 多项式 |
| `crypt` | 支持单向字符串加密（哈希） |
| `echo` | 显示一个或多个字符串 |
| `explode` | 在子字符串上分割字符串 |
| `fprintf` | 将格式化字符串写入流 |
| `get_html_translation_table` | 返回翻译表 |
| `hebrev` | 将希伯来语文本转换为视觉文本 |
| `hebrevc` | 将逻辑希伯来语文本转换为视觉文本 |
| `html_entity_decode` | 将所有 HTML 实体转换为它们对应的字符 |
| `htmlentities` | 将所有适用字符转换为 HTML 实体 |
| `htmlspecialchars` | 将特殊字符转换为 HTML 实体 |
| `implode` | 用字符串连接数组元素 |
| `join` | `implode` 函数的别名 |
| `levenshtein` | 计算两个字符串之间的莱文斯坦距离 |
| `localeconv` | 获取数字格式化信息 |
| `ltrim` | 去除字符串开头的空白字符 |
| `md5` | 计算字符串的 MD5 哈希值 |
| `md5_file` | 计算给定文件名的 MD5 哈希值 |
| `metaphone` | 计算字符串的语音键 |
| `money_format` | 将数字格式化为货币字符串 |
| `nl_langinfo` | 查询语言和区域信息 |
| `nl2br` | 在字符串中的所有换行符前插入 HTML 换行符 |
| `number_format` | 使用千位分隔符格式化数字 |

表 9-1 字符串函数（续）

324 Ajax：初学者指南

| 函数 | 描述 |
|---|---|
| `ord` | 返回字符的 ASCII 值 |
| `parse_str` | 将字符串解析为变量 |
| `print` | 显示字符串 |
| `printf` | 显示格式化字符串 |
| `quoted_printable_decode` | 将 quoted-printable 字符串转换为 8 位字符串 |
| `quotemeta` | 引用元字符 |
| `rtrim` | 去除字符串末尾的空白字符 |
| `setlocale` | 设置区域信息 |
| `sha1` | 计算字符串的 SHA1 哈希值 |
| `sha1_file` | 计算文件的 SHA1 哈希值 |
| `similar_text` | 计算两个字符串之间的相似度 |
| `soundex` | 计算字符串的 soundex 键 |
| `sprintf` | 返回格式化字符串 |
| `sscanf` | 根据格式从字符串解析输入 |
| `str_ireplace` | `str_replace` 函数的不区分大小写版本 |
| `str_pad` | 用另一个字符串填充字符串 |
| `str_repeat` | 重复字符串 |
| `str_replace` | 将搜索字符串的所有出现替换为替换字符串 |
| `str_rot13` | 对字符串执行 rot13 转换 |
| `str_shuffle` | 随机打乱字符串 |
| `str_split` | 将字符串转换为数组 |
| `str_word_count` | 返回关于字符串中使用单词的信息 |
| `strcasecmp` | 执行二进制不区分大小写的字符串比较 |
| `strchr` | `strstr` 函数的别名 |
| `strcmp` | 执行二进制安全的字符串比较 |
| `strcoll` | 执行基于区域设置的字符串比较 |
| `strcspn` | 找到与掩码不匹配的初始段的长度 |
| `strip_tags` | 从字符串中去除 HTML 和 PHP 标签 |
| `stripcslashes` | 取消引用用 `addcslashes()` 引用的字符串 |
| `stripos` | 找到不区分大小写的字符串第一次出现的位置 |
| `stripslashes` | 取消引用用 `addslashes()` 引用的字符串 |

表 9-1 字符串函数（续）

第 9 章：用 Ajax 介绍 PHP 325

| 函数 | 描述 |
| --- | --- |
| `stristr` | `strstr` 函数的不区分大小写版本 |
| `strlen` | 获取字符串的长度 |
| `strnatcasecmp` | 执行不区分大小写的字符串比较 |
| `strnatcmp` | 使用“自然顺序”算法执行字符串比较 |
| `strncasecmp` | 执行前 *n* 个字符的二进制不区分大小写的比较 |
| `strncmp` | 执行前 *n* 个字符的二进制安全比较 |
| `strpos` | 找到字符串第一次出现的位置 |
| `strrchr` | 找到字符在字符串中最后一次出现的位置 |
| `strrev` | 反转字符串 |
| `strripos` | 找到不区分大小写的字符串最后一次出现的位置 |
| `strrpos` | 找到字符在字符串中最后一次出现的位置 |
| `strspn` | 找到与掩码匹配的初始段的长度 |
| `strstr` | 找到字符串第一次出现的位置 |
| `strtok` | 将字符串标记化 |
| `strtolower` | 将字符串转换为小写 |
| `strtoupper` | 将字符串转换为大写 |
| `strtr` | 翻译某些字符 |
| `substr` | 返回字符串的一部分 |
| `substr_compare` | 从偏移量开始执行两个字符串的二进制安全（可选不区分大小写）比较 |
| `substr_count` | 计算子字符串出现的次数 |
| `substr_replace` | 替换字符串中部分文本 |
| `trim` | 去除字符串开头和末尾的空白字符 |
| `ucfirst` | 使字符串的第一个字符大写 |
| `ucwords` | 使字符串中每个单词的第一个字符大写 |
| `vprintf` | 输出格式化字符串 |
| `vsprintf` | 返回格式化字符串 |
| `wordwrap` | 将字符串换行到给定的字符数 |

表 9-1 字符串函数（续）

接下来讨论，你还可以对 PHP 中的变量做的另一件事是将它们插值到字符串中。

## 将变量插值到文本字符串中

将变量插值到文本字符串中意味着让 PHP 将变量的值代入文本字符串中的变量名。例如，如果你有一个名为 `$apples` 的变量，里面有 2 个苹果，你可以用 `echo` 语句像这样显示这个事实：

```php
$apples = 2;
echo "I have " . $apples . " apples.";
```

但 PHP 也允许你使用以下快捷方式，你可以简单地将变量放在文本字符串中，变量名将被替换为变量的值：

```php
$apples = 2;
echo "I have $apples apples.";
```

当你使用双引号（不是单引号！）包围文本字符串时，就会发生变量插值。在这样的字符串中，每个变量的名称将被其值替换。例如，这是我们的早期示例 `variables.php`，如果你使用插值代替（这是 `interpolation.php`）：

```php
<head>
	<title>
		Interpolating variables in strings
	</title>
</head>
<body>
	<h1>
		Interpolating variables in strings
	</h1>
	<?php
		echo "I'm setting the number of apples to 2...<br>";

		$apples = 2;

		echo "The current number of apples is $apples.<br>";

		echo "Now I'm adding three more apples...<br>";

		$apples = $apples + 3;

		echo "The number of apples I have now is $apples.<br>";
	?>
</body>
</html>
```

你可以在图 9-6 中看到 `interpolation.php` 在运行。很酷。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_346_0.png)

但是这里有一个问题：你能将变量名放入其他文本中吗？例如，如果你想显示“I have a hotdog.”怎么办？你可以首先将“hotdog”中的“hot”存储在一个名为 `$data` 的变量中：

```php
<?
    $data = "hot";
    .
    .
    .
?>
```

然后，你能使用 `$data` 组合成“hotdog”这个单词吗？会像这样吗？

```php
<?
    $data = "hot";
    echo "I have a $datadog.<br>";
?>
```

事实证明这行不通——PHP 会想知道这个名为 `$datadog` 的新变量是什么。相反，你可以用花括号包围变量名（但不包括前导 `$`），在这种情况下使插值生效：

```php
<?
    $data = "hot";
    echo "I have a ${data}dog. <br>";
?>
```

以上就是如何在文本字符串中处理变量与其他非空白字符相邻时的插值方法。如果你不希望变量被插值，可以在变量前加上反斜杠（`\`）：

```php
echo "I have \$apples.";
```

这将显示 “I have $apples.”

## 在 PHP 数组中处理数据

处理数据的下一步是从变量进阶到数组，PHP 中的数组工作方式与 JavaScript 中的数组非常相似。



这里有一个`arrays.php`，它向你展示数组操作的基础知识。在PHP中，你可以通过直接引用数组名来创建它。以下是如何创建一个名为`$fruit`的数组（与其他变量一样，PHP中的数组名也以`$`开头）并为`$fruit[0]`赋值字符串“apples”（与JavaScript一样，PHP中的数组索引从0开始）：

```php
<?php
    $fruit[0] = "apples";
    .
    .
    .
}
?>
```

我们也可以向数组中添加其他元素：

```php
<?php
    $fruit[0] = "apples";
    $fruit[1] = "oranges";
    $fruit[2] = "pomegranates";
    .
    .
    .
}
?>
```

我们可以通过为数组元素重新赋值来覆盖其内容，就像这样，我们覆盖了`$fruit[2]`：

```php
<?php
    $fruit[0] = "apples";
    $fruit[1] = "oranges";
    $fruit[2] = "pomegranates";
    
    $fruit[2] = "watermelons";
    .
    .
    .
?>
```

事实上，PHP中有一个快捷方式可以向数组末尾添加新元素——你可以省略方括号`[`和`]`中的索引。例如，以下是我们如何创建`$fruit[3]`并将其设置为“kumquats”：

```php
<?php
    $fruit[0] = "apples";
    $fruit[1] = "oranges";
    $fruit[2] = "pomegranates";

    $fruit[2] = "watermelons";

    $fruit[] = "kumquats";

...
?>
```

好的，让我们在`for`循环中打印出数组元素，这与JavaScript中的`for`循环工作方式相同。在PHP中，我们可以通过将数组传递给PHP的`count`函数来确定数组中的元素数量，该函数返回数组中的元素总数；因此，我们可以这样遍历所有元素：

```php
<?php
    $fruit[0] = "apples";
    $fruit[1] = "oranges";
    $fruit[2] = "pomegranates";

    $fruit[2] = "watermelons";

    $fruit[] = "kumquats";

    for ($loopIndex = 0; $loopIndex < count($fruit);
         $loopIndex++){
        ...
    }
?>
```

以下是我们如何在浏览器中显示`arrays.php`中数组的每个元素：

```php
<html>
    <head>
        <title>
            Creating PHP Arrays
        </title>
    </head>

    <body>
        <h1>
            Creating PHP Arrays
        </h1>

<?php
    $fruit[0] = "apples";
    $fruit[1] = "oranges";
    $fruit[2] = "pomegranates";

    $fruit[2] = "watermelons";

    $fruit[] = "kumquats";

    for ($loopIndex = 0; $loopIndex < count($fruit);
        $loopIndex++){
        echo "\$fruit[$loopIndex] = $fruit[$loopIndex] <br>";
    }
?>
</body>
</html>
```

你可以在图9-7中看到此示例的实际运行效果。在PHP中，你也可以使用单词作为数组索引，像这样：

```php
$array["fruit"] = "apples";
```

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_349_0.png)

图9-7 使用数组

## 使用运算符处理数据

与JavaScript一样，PHP有一系列内置运算符，以下是按优先级顺序排列的（即，在同一语句中组合使用时，列表中靠上的运算符会先于靠下的运算符执行）：

1. `new`
2. `[`
3. `! ~ ++ --`
4. `* / %`
5. `+ - .`
6. `== !=`
7. `&`
8. `|`
9. `&&`
10. `||`
11. `?:`
12. `= += -= *= /= .= %= &= |= ^= <<= >>=`

这是一个示例`operators.php`，展示了一些PHP运算符的使用——具体是`+`、`-`、`*`和`/`：

```php
<html>
    <head>
        <title>
            Using PHP Operators
        </title>
    </head>

    <body>
        <h1>
            Using PHP Operators
        </h1>
        <?php
            echo "12 + 3 = ", 12 + 3, "<br>";

            echo "12 - 3 = ", 12 - 3, "<br>";

            echo "12 * 3 = ", 12 * 3, "<br>";

            echo "12 / 3 = ", 12 / 3, "<br>";

        ?>
    </body>
</html>
```

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_351_0.png)

图9-8 使用PHP运算符

结果显示在图9-8中，与你基于JavaScript知识所预期的结果相同。

## 使用`if`语句进行分支

PHP的`if`语句看起来与JavaScript中的版本非常相似，只是增加了可选的`elseif`子句。在PHP中，`if`语句的正式形式如下（注意，`statement`可以是由多行代码组成的复合语句，包含在花括号`{`和`}`中）：

```text
if (condition)
    statement
[elseif (condition)
    statement]
.
.
.
[elseif (condition)
    statement]
else
    statement
```

你已经从JavaScript知识中了解了`if`和`else`关键字的工作方式。PHP中的`elseif`关键字允许你测试额外的条件，并在条件为真时执行相应的代码。这是一个示例`elseif.php`，展示了如何将变量与多个条件进行比较，并执行第一个计算结果为真的条件所对应的代码：

```php
<html>
<head>
<title>
Using elseif in PHP
</title>
</head>
<body>
<h1>
Using elseif in PHP
</h1>
<?
$temperature = 87;
if ($temperature < 80){
echo "Temperature is OK.";
}
elseif ($temperature < 85) {
echo "Pretty warm.";
}
elseif ($temperature < 90) {
echo "Pretty hot.";
}
else {
echo "Too hot!";
}
?>
</body>
</html>
```

你可以在图9-9中看到结果——相当热！

与JavaScript一样，你可以使用比较运算符（如`<`和`>`）以及逻辑运算符（如`&&`与运算符）在代码中表达条件。例如，这个`if`语句检查温度是否在65到85之间（包含65和85）：

```php
<?
$temperature = 70;
if (($temperature >= 65) && ($temperature <= 85)){
echo "In the comfort zone.";
}
?>
```

PHP比较运算符总结在表9-2中，逻辑运算符总结在表9-3中。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_353_0.png)

图9-9 使用`elseif`关键字

| 运算符 | 操作 | 示例 | 结果 |
| --- | --- | --- | --- |
| `==` | 等于 | `$a == $b` | 如果`$a`等于`$b`则为真 |
| `===` | 恒等 | `$a === $b` | 如果`$a`等于`$b`且类型相同则为真 |
| `!=` | 不等于 | `$a != $b` | 如果`$a`不等于`$b`则为真 |
| `<>` | 不等于 | `$a <> $b` | 如果`$a`不等于`$b`则为真 |
| `!==` | 不恒等 | `$a !== $b` | 如果`$a`不等于`$b`，或类型不同则为真 |
| `<` | 小于 | `$a < $b` | 如果`$a`小于`$b`则为真 |
| `>` | 大于 | `$a > $b` | 如果`$a`大于`$b`则为真 |
| `<=` | 小于或等于 | `$a <= $b` | 如果`$a`小于或等于`$b`则为真 |
| `>=` | 大于或等于 | `$a >= $b` | 如果`$a`大于或等于`$b`则为真 |

表9-2 比较运算符

| 运算符 | 操作 | 示例 | 结果 |
| --- | --- | --- | --- |
| `and` | 与 | `$a and $b` | 如果`$a`和`$b`都为真则结果为真 |
| `or` | 或 | `$a or $b` | 如果`$a`或`$b`为真则结果为真 |
| `xor` | 异或 | `$a xor $b` | 如果`$a`或`$b`为真但两者不同时为真则结果为真 |
| `!` | 非 | `! $a` | 如果`$a`不为真则结果为真 |
| `&&` | 与 | `$a && $b` | 如果`$a`和`$b`都为真则结果为真 |
| `||` | 或 | `$a || $b` | 如果`$a`或`$b`为真则结果为真 |

表9-3 逻辑运算符

## 在PHP中使用`for`循环

`for`循环重复执行一条语句，在PHP中其形式如下：

```text
for (expression1; expression2; expression3)
    statement
```

这里，与JavaScript一样，`expression1`用于初始化循环，通常是初始化一个循环计数器（也称为循环索引），用于跟踪循环已执行的次数。下一个表达式`expression2`是测试表达式——当该表达式保持为真时，循环将继续。最后一个表达式`expression3`在每次循环执行`statement`之后执行。你通常在该表达式中递增循环计数器变量。每次循环，`statement`（可以是一个由包含在花括号中的多条简单语句组成的复合语句）都会被执行。

这是一个`for`循环的示例，在`for.php`中，它将“I'm going to print this ten times.”打印十次：

```php
<html>
    <head>
        <title>
            Using the PHP for Loop
        </title>
    </head>

    <body>
        <h1>
            Using the PHP for Loop
        </h1>

        <?php
            for ($loopIndex = 0; $loopIndex < 10; $loopIndex++){
                echo "I'm going to print this ten times.<br>";
            }
        ?>
    </body>
</html>
```

你可以在图9-10中看到结果。很好。

## 使用`while`循环进行循环

`while`循环在其条件保持为真时持续执行其代码。此循环的正式形式如下：

```text
while (condition)
    statement
```

# 336 Ajax：初学者指南

![img/2cd265cf0a64e9b4b91ab611753cd5d5_355_0.png](img/2cd265cf0a64e9b4b91ab611753cd5d5_355_0.png)

图9-10 使用`for`循环

此循环会持续执行`statement`（当然，这可以是用花括号括起来的复合语句），直到`condition`变为假。

下面是一个示例`while.php`，它持续显示消息“I'm going to print this ELEVEN times.”。首先，我们设置`while`循环和一个变量来跟踪循环执行的次数：

```php
<html>
    <head>
        <title>
            Using a PHP while Loop
        </title>
    </head>

    <body>
        <h1>
            Using a PHP while Loop
        </h1>
        <?php
            $variable = 0;

            while ($variable < 11){
```

...}

?>

</body>

</html>

现在我们可以在`while`循环中添加内容——即向浏览器输出消息并递增变量的部分：

```php
<html>
    <head>
        <title>
            Using a PHP while Loop
        </title>
    </head>

    <body>
        <h1>
            Using a PHP while Loop
        </h1>
        <?php
            $variable = 0;

            while ($variable < 11){
                echo "I'm going to print this ELEVEN times.<br>";
                $variable++;
            }
        ?>
    </body>
</html>
```

你可以在图9-11中看到结果——这个示例确实打印了十一次消息。很好。

## 动手试试：多次显示消息

创建一个PHP示例，让消息持续打印十分之一秒。你可以使用`gettimeofday`函数获取当前时间；该函数返回一个数组，预定义的常量`sec`是该数组中秒数值的索引。因此，要让消息持续打印十分之一秒，你可以这样做：

```php
<html>
    <head>
        <title>
```

（续）

![img/2cd265cf0a64e9b4b91ab611753cd5d5_357_0.png](img/2cd265cf0a64e9b4b91ab611753cd5d5_357_0.png)

图9-11 使用`while`循环

```php
Using a PHP while Loop
</title>
</head>

<body>
    <h1>
        Using a PHP while Loop
    </h1>
    <?php
        $time = gettimeofday();
        $start = $time[sec];

        $time = gettimeofday();
        $timeNow = $time[sec];

        while ($timeNow < ($start + 0.1)){
            $time = gettimeofday();
            $timeNow = $time[sec];
            echo "I'm going to keep going for a tenth of a second!<br>";
        }
    ?>
</body>
</html>
```

## 使用`do...while`循环

还有另一种版本的`while`循环——`do...while`循环。这种循环在循环末尾检查其条件，而不是在开始处，这意味着循环的语句总是至少执行一次（如果该语句设置了你想测试的条件，以判断循环是否应继续，那么这就很有用）。这个循环的正式形式如下：

```text
do
    statement
while (condition)
```

你可能已经注意到，在之前的“动手试试”示例中，你必须在开始`while`循环之前设置`$timeNow`变量——然后在循环内部每次循环时再次设置。使用`do...while`循环，我们不必在开始循环之前设置`$timeNow`变量，因为循环的条件是在循环末尾检查的：



```html
<html>
    <head>
        <title>
            Using a PHP while Loop
        </title>
    </head>

    <body>
        <h1>
            Using a PHP while Loop
        </h1>
        <?php
            $time = gettimeofday();
            $start = $time[sec];

            do {
                $time = gettimeofday();
                $timeNow = $time[sec];
                echo "I'm going to keep going for a tenth of a second!<br>";
            } while ($timeNow < ($start + 0.1))
        ?>
    </body>
</html>
```

请记住，`do...while` 循环的主体总是至少执行一次。

## 使用 `foreach` 循环

PHP 还有一个特殊的循环，用于遍历数据集合（如数组）的所有成员——`foreach` 循环。它的形式如下：

```php
foreach (array as $value)
    statement
```

`foreach` 循环是一个方便的循环，因为每次循环时，它会将数组的下一个元素放入一个变量中，你可以在循环体内使用该变量。这是一个示例 `foreach.php`。我们首先创建一个水果数组：

```html
<html>
    <head>
        <title>Using the PHP foreach Loop</title>
    </head>

    <body>
        <h1>Using the PHP foreach Loop</h1>
        <?php
        $array = array("apples", "oranges", "bananas", "cherries");
        .
        .
        .
        ?>
    </body>
</html>
```

然后我们设置一个 `foreach` 循环，遍历该数组，每次循环时将当前元素填充到我们命名为 `$fruit` 的变量中：

```html
<html>
    <head>
        <title>Using the PHP foreach Loop</title>
    </head>

    <body>
        <h1>Using the PHP foreach Loop</h1>
        <?php
        $array = array("apples", "oranges", "bananas", "cherries");

            foreach ($array as $fruit) {
            .
            .
            .
            }
        ?>
    </body>
</html>
```

现在我们可以在循环体中自由使用 `$fruit` 变量，我们通过打印它来实现：

```html
<html>
    <head>
        <title>Using the PHP foreach Loop</title>
    </head>

    <body>
        <h1>Using the PHP foreach Loop</h1>
        <?php
        $array = array("apples", "oranges", "bananas", "cherries");

        foreach ($array as $fruit) {
            echo "The current fruit: $fruit <br>";
        }
        ?>
    </body>
</html>
```

很好——你可以在图 9-12 中看到结果。请注意，`foreach` 循环是遍历数组时极其有用的循环。使用其他循环时，你必须设置一个数组索引来遍历数组（如果数组使用单词作为索引值，这很难），并且设置循环时总有可能将数组索引搞错一位。`foreach` 循环通过自动遍历数组的所有元素来避免此问题，不需要数组索引。

![img/2cd265cf0a64e9b4b91ab611753cd5d5_360_0.png](img/2cd265cf0a64e9b4b91ab611753cd5d5_360_0.png)

图 9-12 使用 `foreach` 循环

# 第 10 章：深入 PHP

Ajax：初学者指南

## 关键技能与概念

- 创建函数
- 向函数传递数据
- 创建默认参数
- 从函数返回数据
- 处理文本字段、复选框和单选按钮
- 处理多选 HTML 控件
- 使用图像映射

前一章介绍了 PHP 的基础知识。在本章中，你将获得该主题的实际工作知识。这里，你将学习如何在 JavaScript 中编写函数，以及如何在 HTML 控件（如文本字段、单选按钮、复选框等）中处理用户输入。

让我们从 PHP 函数开始，这在你学习 JavaScript 函数时应该已经有所了解。

## PHP 函数介绍

我们将通过直接进入示例来开始 PHP 函数的学习。假设你有一个像这样的网页：

```html
<html>
  <head>
    <title>Using PHP Functions</title>
  </head>

  <body>
    <h1>Using PHP Functions</h1>

    <?php
      echo "<h3>Welcome to my Web page!</h3>";
      echo "<br>";
      echo "Do you like it?";
      echo "<br>";
      echo "<br>";
```

# 第 10 章：深入 PHP

```php
?>
</body>
</html>
```

这看起来不错，但假设你不想让任何人从你漂亮的新页面上偷走任何东西，因此决定添加版权声明。为此，你计划调用一个名为 `print_copyright_notice` 的函数，你可以这样调用它，就像在 JavaScript 中一样：

```html
<html>
  <head>
    <title>Using PHP Functions</title>
  </head>

  <body>
    <h1>Using PHP Functions</h1>

    <?php
      echo "<h3>Welcome to my Web page!</h3>";
      echo "<br>";
      echo "Do you like it?";
      echo "<br>";
      echo "<br>";

      print_copyright_notice();

      .
      .
      .
    ?>
  </body>
</html>
```

你可以像在 JavaScript 中一样创建 `print_copyright_notice` 函数，使用关键字 `function`、函数名和一对括号：

```html
<html>
  <head>
    <title>Using PHP Functions</title>
  </head>

  <body>
    <h1>Using PHP Functions</h1>

    <?php
      echo "<h3>Welcome to my Web page!</h3>";
      echo "<br>";
```

## 346 Ajax：初学者指南

```php
echo "Do you like it?";
echo "<br>";
echo "<br>";

print_copyright_notice();

function print_copyright_notice()
{
    .
    .
    .
}
?>
</body>
</html>
```

然后，将要在函数被调用时执行的代码放在函数体内部。在这种情况下，你可以像这样显示版权通知（在此示例中，文件名为 `functions.php`）：

```php
</html>
<html>
<head>
    <title>使用 PHP 函数</title>
</head>

<body>
    <h1>使用 PHP 函数</h1>

    <?php
    echo "<h3>欢迎访问我的网页！</h3>";
    echo "<br>";
    echo "你喜欢它吗？";
    echo "<br>";
    echo "<br>";

    print_copyright_notice();

    function print_copyright_notice()
    {
        echo "<hr>";
        echo "<center>";
        echo "&copy; 2008 PHP 超级奇才公司";
        echo "</center>";
    }
    ?>
</body>
</html>
```

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_366_0.png)

**图 10-1** 通过调用函数显示版权通知

你可以在图 10-1 中看到结果，函数确实被调用并显示了版权通知。

很好——但函数的功能远不止于此。如何向它们传递数据呢？

## 在 PHP 中向函数传递数据

你也可以在 PHP 中向函数传递数据，就像在 JavaScript 中一样——而且语法也相同。例如，假设你想在一个新的示例 `passfunctions.php` 中，将要显示的版权文本传递给 `print_copyright_notice` 函数。你可以这样传递该文本：

```php
<html>
    <head>
        <title>向 PHP 函数传递数据</title>
    </head>

    <body>
        <h1>向 PHP 函数传递数据</h1>

        <?php
            echo "<h3>欢迎访问我的网页！</h3>";
            echo "<br>";
            echo "你喜欢它吗？";
            echo "<br>";
            echo "<br>";

            print_copyright_notice(
                "&copy; 2008 PHP 超级奇才公司");
.
.
.
?>
</body>
</html>
```

并且，就像在 JavaScript 中一样，你在函数的参数列表中为传递的数据指定一个名称（这里是 `$text`），然后你就可以在函数体内使用该名称来引用这些数据：

```php
<html>
    <head>
        <title>向 PHP 函数传递数据</title>
    </head>

    <body>
        <h1>向 PHP 函数传递数据</h1>

        <?php
            echo "<h3>欢迎访问我的网页！</h3>";
            echo "<br>";
            echo "你喜欢它吗？";
            echo "<br>";
            echo "<br>";

            print_copyright_notice(
                "&copy; 2008 PHP 超级奇才公司");

            function print_copyright_notice($text)
            {
                echo "<hr>";
                echo "<center>";
                echo $text;
                echo "</center>";
            }
        ?>
    </body>
</html>
```

结果如图 10-2 所示——如你所见，数据已传递给函数，并且函数正确地使用了这些数据。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_368_0.png)

**图 10-2** 向函数传递数据

### 试一试：向函数传递多个项

想向函数传递多个项吗？这也和 JavaScript 中的工作方式完全一样。你在参数列表中用逗号分隔这些项。试试这个——将两个数字传递给一个名为 `adder` 的函数，让它们相加并显示结果。代码如下所示：

```php
<html>
    <head>
        <title>向 PHP 函数传递数据</title>
    </head>

    <body>
        <h1>向 PHP 函数传递数据</h1>

        <?php
            echo "<h3>欢迎访问我的数学页面！</h3>";
            echo "<br>";
            echo "5 + 3 等于多少？";
            echo "<br>";

            adder(5, 3);

            function adder($operand1, $operand2)
            {
                echo "总和是 ";
                echo $operand1 + $operand2;
            }
        ?>
    </body>
</html>
```

（续）

### 在函数中创建默认参数

在 PHP 中，你还可以在函数中设置*默认*参数。这些默认值用于当你没有为某个参数提供值的情况。下面是一个示例 `default.php`，它设置了一些用于版权通知的默认文本。你可以通过为 `$text` 参数提供一个默认值来实现，方法是在函数声明中使用等号：

```php
function print_copyright_notice($text = "&copy; 2008")
{
    echo "<hr>";
    echo "<center>";
    echo $text;
    echo "</center>";
}
```

现在，如果你调用 `print_copyright_notice` 并且不向函数传递任何数据，`$text` 将默认设置为 `"&copy; 2008"`。让我们在一个新的示例 `default.php` 中进行测试，调用该函数但不传递任何数据：

```php
<html>
  <head>
    <title>使用带默认参数的 PHP 函数</title>
  </head>

  <body>
    <h1>使用带默认参数的 PHP 函数</h1>

    <?php
      echo "<h3>欢迎访问我的网页！</h3>";
      echo "<br>";
      echo "你喜欢它吗？";
      echo "<br>";
      echo "<br>";

      print_copyright_notice();

      function print_copyright_notice($text = "&copy; 2008")
      {
        echo "<hr>";
        echo "<center>";
        echo $text;
        echo "</center>";
      }
    ?>
</body>
</html>
```

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_370_0.png)

**图 10-3** 在函数中使用默认参数

你可以在图 10-3 中看到结果——版权通知确实使用了默认值。

### 从函数返回数据

因为你已经知道 JavaScript 的工作原理，所以你大致也了解如何从 PHP 函数返回数据。例如，如果你想构建一个名为 `adder` 的函数，它将两个数字相加并返回它们的和，你可以在一个新的示例 `returnfunctions.php` 中这样开始：

```php
<html>
  <head>
    <title>从 PHP 函数返回数据</title>
  </head>

  <body>
    <h1>从 PHP 函数返回数据</h1>

    <?php
        echo "<h3>欢迎访问我的数学页面！</h3>";
        echo "<br>";
        echo "5 + 3 等于多少？";
        echo "<br>";

        function adder($operand1, $operand2)
        {
            return $operand1 + $operand2;
        }
    ?>
</body>
</html>
```

现在你可以调用 `adder` 函数，并且，就像在 JavaScript 中一样，函数的名称将被该函数返回的值所替换：



```php
<html>
    <head>
        <title>从 PHP 函数返回数据</title>
    </head>

    <body>
        <h1>从 PHP 函数返回数据</h1>

        <?php
            echo "<h3>欢迎访问我的数学页面！</h3>";
            echo "<br>";
            echo "5 + 3 等于多少？";
            echo "<br>";

            echo "总和是 " . adder(5, 3);

            function adder($operand1, $operand2)
            {
                return $operand1 + $operand2;
            }
        ?>
    </body>
</html>
```

你可以在图 10-4 中看到效果。正如你所预料的那样。

你还可以设置 PHP 函数同时返回多个项。通过返回一个数组来实现，PHP 使得在代码中操作数组变得很容易——这里有一个示例 `multipereturnfunctions.php`。

### 专家问答

**问：** 如果我有多个参数需要分配默认值怎么办？例如，如果我修改 `adder` 函数以接受三个参数，并且想给第二个参数 `$operand2` 一个默认值？

```php
function adder($operand1, $operand2, $operand3)
{
    echo "总和是 ";
    echo $operand1 + $operand2 + $operand3;
}
```

**答：** 如果你给一个参数指定了默认值，你必须给它右边的所有参数也指定默认值。因此，如果你想给 `$operand2` 一个默认值，你也必须给 `$operand3` 分配一个默认值：

```php
function adder($operand1, $operand2 = 1, $operand3 = 3)
{
    echo "总和是 ";
    echo $operand1 + $operand2 + $operand3;
}
```

你可以使用 `return` 语句以这种方式返回两个数字的和：

```php
<html>
    <head>
        <title>从 PHP 函数返回数据</title>
    </head>

    <body>
        <h1>从 PHP 函数返回数据</h1>

        <?php
            echo "<h3>欢迎访问我的数学页面！</h3>";
            echo "<br>";
            echo "5 + 3 等于多少？";
            echo "<br>";

            function adder($operand1, $operand2)
            {
                return $operand1 + $operand2;
            }
        ?>
    </body>
</html>
```

## 在 PHP 中使用 HTML 控件

PHP 的很多功能都与读取用户输入到 HTML 控件（如文本字段、单选按钮、列表框等）的信息有关，本节将介绍如何在 PHP 中解码这些信息。

首先，你需要在网页中设置一个 `<form>` 元素，用于放置你的 HTML 控件。以下是 `<form>` 元素的重要属性：

- **ACTION**：指定将处理表单数据的 URL。请注意，你可以省略此属性，此时默认值为当前文档的 URL。
- **METHOD**：指定向目标操作 URL 发送数据的方法或协议。如果设置为 GET（默认值），此方法会将所有表单名/值对信息放在一个类似如下的 URL 中发送：

  `URL?name=value&name=value&name=value`

  如果使用 POST 方法，表单内容的编码方式与 GET 方法相同，但会通过隐藏的环境变量发送。
- **TARGET**：指示浏览器在哪个命名框架中显示表单结果。

这是一个使用 `<form>` 元素的示例。此示例使用 POST 方法将其数据发送到服务器，特别是发送到名为 `responder.php` 的 PHP 文件：

```html
<html>
    <head>
        <title>
            Using HTML forms
        </title>
    </head>

    <body>
        <h1>
            Using HTML forms
        </h1>
        <form method="post" action="responder.php">
            .
            .
            .
        </form>
    </body>
</html>
```

好了，这设置了 `<form>` 元素。要实际发送你放在 `<form>` 元素中的任何 HTML 控件内的数据，你可以使用提交按钮，该按钮通过 `<input type="submit">` 元素创建：

```html
<html>
    <head>
        <title>
            Using HTML forms
        </title>
    </head>

    <body>
        <h1>
            Using HTML forms
        </h1>
        <form method="post" action="responder.php">
            .
            .
            .
            <input type="submit" value="Submit">
        </form>
    </body>
</html>
```

你也可以通过一个重置按钮，让用户有机会将表单中所有 HTML 控件的内容恢复为默认值，该按钮通过 `<input type = "reset">` 元素创建：

```html
<html>
    <head>
        <title>
            Using HTML forms
        </title>
    </head>

    <body>
        <h1>
            Using HTML forms
        </h1>
        <form method="post" action="responder.php">
            .
            .
            .
            <input type="submit" value="Submit">
            <input type="reset" value="Reset">
        </form>
    </body>
</html>
```

既然我们已经设置了 `<form>` 元素，让我们在表单中放置一些 HTML 控件，首先是文本字段，然后是复选框、单选按钮、列表框和图像映射。

## 使用文本字段

文本字段允许用户在网页中输入文本，你可以使用 PHP 在服务器上读取该文本。下面是一个名为 `textfield.html` 的示例，展示了如何读取并显示用户的名字。我们将从示例的 HTML 部分开始，然后编写 PHP。

### 创建 HTML

我们需要在 `textfield.html` 中创建一个 HTML 表单，用于放置我们的新文本字段，并且需要将表单中的数据发送到 `textfield.php`：

```html
<html>
    <head>
        <title>
            Using Text Fields
        </title>
    </head>
    <body>
        <center>
            <h1>
                Using Text Fields
            </h1>
            <form method="post" action="textfield.php">
                .
                .
                .
            </form>
        </center>
    </body>
</html>
```

接下来，我们可以添加一个提示，让用户输入他们的名字（你可以在 `<form>` 元素内部使用 HTML）：

```html
<html>
    <head>
        <title>
            Using Text Fields
        </title>
    </head>
```

现在我们将添加文本字段本身，它是一个 `<input type="text">` 元素，给它命名为 `"name"`（因为它应该包含这个人的名字）：

```html
<html>
    <head>
        <title>
            Using Text Fields
        </title>
    </head>

    <body>
        <center>

            <h1>
                Using Text Fields
            </h1>

            <form method="post" action="textfield.php">
                Please enter your name:

                <input name="name" type="text">
                .
                .
                .
            </form>

        </center>
    </body>
</html>
```

最后，我们可以添加所需的提交按钮：

```html
<html>
    <head>
        <title>
            Using Text Fields
        </title>
    </head>

    <body>
        <center>

            <h1>
                Using Text Fields
            </h1>

            <form method="post" action="textfield.php">
                Please enter your name:

                <input name="name" type="text">

                <br>
                <br>

                <input type="submit" value="Submit">
            </form>

        </center>
    </body>
</html>
```

你可以在图 10-6 中看到 `textfield.html` 的样子，其中用户已输入他们的名字并正在点击提交按钮。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_380_0.png)

那么当用户点击提交按钮时会发生什么？文本字段中的文本会被发送到 PHP 脚本 `textfield.php`，但首先我们需要编写该脚本。

### 创建 PHP

现在我们将编写 `textfield.php`。我们可以在 PHP 页面中放置 HTML，所以我们将从一条消息开始，告诉用户我们已读取他们的名字：

```html
<html>
    <head>
        <title>
            Reading text from text fields
        </title>
    </head>

    <body>
        <center>

            <h1>
                Reading text from text fields
            </h1>
            Your name is
            .
            .
            .

        </center>
    </body>
</html>
```

我们将这样创建脚本的 PHP 部分：

```php
<html>
    <head>
        <title>
            Reading text from text fields
        </title>
    </head>

    <body>
        <center>

            <h1>
                Reading text from text fields
            </h1>
            Your name is
            <?php
            .
            .
            .
            ?>

        </center>
    </body>
</html>
```

从一个名为 `$fruits` 的函数开始，它返回一个水果数组，你可以使用内置的 PHP 数组函数创建该数组：

```php
<html>
    <head>
        <title>
            Returning Multiple Values From PHP Functions
        </title>
    </head>

    <body>
        <h1>
            Returning Multiple Values From PHP Functions
        </h1>

        <?php
            .
            .
            .

            function fruits()
            {
                $array = array("Apples", "Oranges", "Plums", "Cherries",
                                "Strawberries", "Bananas");

                return $array;
            }
        ?>
    </body>
</html>
```

你可以使用 PHP 内置的 `list` 函数来处理返回数组的函数。该函数允许你将数组中的每个元素分配给一个新变量。以下是其工作原理，其中你将返回数组的第一个元素分配给名为 `$first` 的变量，第二个元素分配给名为 `$second` 的变量，依此类推：

```php
<html>
<head>
    <title>
        Returning Multiple Values From PHP Functions
    </title>
</head>
<body>
    <h1>
        Returning Multiple Values From PHP Functions
    </h1>
    <?php
        list($first, $second, $third, $fourth, $fifth, $sixth) = fruits();
        .
        .
        .
        function fruits()
        {
            $array = array("Apples", "Oranges", "Plums", "Cherries",
                "Strawberries", "Bananas");

            return $array;
        }
    ?>
</body>
</html>
```

最后，你可以显示新变量及其值：

```php
<html>
<head>
    <title>
        Returning Multiple Values From PHP Functions
    </title>
</head>
<body>
    <h1>
        Returning Multiple Values From PHP Functions
    </h1>
</body>
</html>
```

356 Ajax: A Beginner's Guide

```php
<?php

list($first, $second, $third, $fourth, $fifth, $sixth) = fruits();

echo "\$first: $first<br>";
echo "\$second: $second<br>";
echo "\$third: $third<br>";
echo "\$fourth: $fourth<br>";
echo "\$fifth: $fifth<br>";
echo "\$sixth: $sixth<br>";

function fruits()
{
    $array = array("Apples", "Oranges", "Plums", "Cherries", "Strawberries", "Bananas");

    return $array;
}
?>
</body>
</html>
```

此示例的结果出现在图 10-5 中；如你所见，`fruits` 函数能够返回多个值。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_375_0.png)

图 10-5 从函数返回多个数据值

## 使用复选框



另一个常用的 HTML 控件是复选框。与处理文本框的方式略有不同，我们将在新示例中进行说明。

### 创建 HTML

这个名为`checkbox.html`的示例将询问用户是否希望中彩票，允许他们通过勾选复选框来回答“是”或“否”。我们首先创建一个表单，将数据发送到名为`checkbox.php`的 PHP 脚本：

```html
<html>
    <head>
        <title>Using Checkboxes</title>
    </head>
    <body>
        <center>
            <h1>Using Checkboxes</h1>
            <form method=post action="checkbox.php">
                .
                .
                .
            </form>
        </center>
    </body>
</html>
```

接下来，我们向用户添加提示和“是”复选框，这是一个`<input type="checkbox">`元素——注意我们给这个控件起的名称是`"check1"`：

```html
<html>
    <head>
        <title>Using Checkboxes</title>
    </head>
    <body>
        <center>
            <h1>Using Checkboxes</h1>
            <form method=post action="checkbox.php">
                Would you like to win the lottery?
                <input name="check1" type="checkbox" value="Yes">
                Yes
                .
                .
                .
            </form>
        </center>
    </body>
</html>
```

接下来我们添加第二个复选框，即“否”复选框，将其命名为`"check2"`，并添加提交按钮：

```html
<html>
    <head>
        <title>Using Checkboxes</title>
    </head>

    <body>
        <center>
        <h1>Using Checkboxes</h1>
        <form method=post action="checkbox.php">
            Would you like to win the lottery?
            <input name="check1" type="checkbox" value="Yes">
            Yes
            <input name="check2" Type="checkbox" value="No">
            No
            <br>
            <br>
            <input type="submit" value="Submit">
        </form>
        </center>
    </body>
</html>
```

很好——你可以在图 10-8 中看到这个新页面，上面有复选框。当用户点击提交按钮时，复选框中的数据会被发送到`checkbox.php`，接下来我们将介绍这个 PHP 脚本。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_384_0.png)

**图 10-8** 一个带有复选框的网页

### 创建 PHP

我们将第一个复选框命名为`"check1"`，那么我们是否可以这样检查`check1`的设置并报告它呢？

```html
<html>
    <head>
        <title>
            Reading data from checkboxes
        </title>
    </head>
    <body>
        <center>
            <h1>Reading data from checkboxes</h1>
            You checked
            <?php
                echo $_REQUEST["check1"], "<br>";
            .
            .
            .
            ?>
        </center>
    </body>
</html>
```

不，我们不能这样做。如果`check1`未被勾选，尝试引用`$_REQUEST["check1"]`将会导致错误（因为`check1`在`$_REQUEST`数组中没有值）。因此，我们首先必须确定`check1`是否已被勾选。我们可以使用`isset`函数来完成，该函数判断数组元素是否已被设置，如果已设置则返回 true（否则返回 false）：

```html
<html>
    <head>
        <title>
            Reading data from checkboxes
        </title>
    </head>
    <body>
        <center>
            <h1>Reading data from checkboxes</h1>
            You checked
            <?php
                if (isset($_REQUEST["check1"]))
                    echo $_REQUEST["check1"], "<br>";
            .
            .
            .
            ?>
        </center>
    </body>
</html>
```

`$_REQUEST["check1"]`的值就是我们在`checkbox.html`网页中为`check1`设置的值，也就是`"Yes"`。同样，我们可以这样处理“否”复选框`check2`：

```html
<html>
    <head>
        <title>
            Reading data from checkboxes
        </title>
    </head>

    <body>
        <center>
            <h1>Reading data from checkboxes</h1>

            You checked
            <?php
                if (isset($_REQUEST["check1"]))
                    echo $_REQUEST["check1"], "<br>";
                if (isset($_REQUEST["check2"]))
                    echo $_REQUEST["check2"], "<br>";
            ?>
        </center>
    </body>
</html>
```

你可以在图 10-9 中看到结果，`checkbox.php`正确识别了被勾选的复选框。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_386_0.png)

另一方面，请注意，在这个示例中用户完全有可能同时点击**两个**复选框，这将给我们带来混乱的结果`"You checked Yes No."`。由于这里只可能有一个答案——是**或**否——我们需要设置两个控件，以便用户一次只能选择其中一个。这就需要用到单选按钮了。

## 使用单选按钮

正如每个网络用户所知，单选按钮是那些圆形的控件，点击（选中）时会出现圆点。单选按钮协同工作，意味着一组单选按钮中一次只能选中一个。

为了理解单选按钮如何与 PHP 配合使用，我们将看一个示例，`radiobutton.html`。

### 创建 HTML

`radiobutton.html`示例以一个表单元素开始，该表单会将其数据发送到`radiobutton.php`：

```html
<html>
<head>
<title>Using radio buttons</title>
</head>
<body>
<center>
<h1>Using radio buttons</h1>
<form method=post action="radiobutton.php">
.
.
.
</form>
</center>
</body>
</html>
```

接下来我们添加一个名称为`"radio1"`，值为**Yes**的单选按钮：

```html
<html>
<head>
<title>Using radio buttons</title>
</head>
<body>
<center>
<h1>Using radio buttons</h1>
<form method=post action="radiobutton.php">
Would you like to win the lottery?
<input name="radio1" type="radio" value="Yes">
Yes
```

对于第二个单选按钮，你可能认为我们会将其命名为`"radio2"`，但为了让它与`radio1`协同工作，我们必须给它相同的名称`radio1`（我们同时添加一个提交按钮）：

```html
<html>
	<head>
		<title>Using radio buttons</title>
	</head>

	<body>
		<center>
		<h1>Using radio buttons</h1>
		<form method=post action="radiobutton.php">
			Would you like to win the lottery?
			<input name="radio1" type="radio" value="Yes">
			Yes
			<input name="radio1" Type="radio" value="No">
			No
			<br>
			<br>
			<input type="submit" value="Submit">
		</form>
		</center>
	</body>
</html>
```

你可以在图 10-10 中看到`radiobutton.html`。

接下来，让我们创建`radiobutton.php`。

### 创建 PHP

在`radiobutton.php`中，我们首先是一些 HTML：

```html
<html>
	<head>
		<title>
			Reading data from radio buttons
		</title>
	</head>
```

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_389_0.png)

图 10-10 在`radiobutton.html`中使用单选按钮

```html
<body>
    <center>
        <h1>Reading data from radio buttons</h1>

        You selected
        .
        .
        .
    </center>
</body>
</html>
```

接下来，我们可以使用`isset`函数检查是否有任何等待处理的数据，其名称为`radio1`：

```html
<html>
    <head>
        <title>
            Reading data from radio buttons
        </title>
    </head>

    <body>
        <center>
            <h1>Reading data from radio buttons</h1>

            .
            You selected
            <?php
                if (isset($_REQUEST["radio1"]))
```

如果有一个名为`"radio1"`的数据等待我们接收，那么该数据将是第一个单选按钮（"是"）或第二个单选按钮（"否"）的值。要显示单选按钮的数据，我们只需按如下方式回显`$_REQUEST["radio1"]`：

```html
<html>
    <head>
        <title>
            从单选按钮读取数据
        </title>
    </head>

    <body>
        <center>
            <h1>从单选按钮读取数据</h1>

            你选择了
            <?php
                if (isset($_REQUEST["radio1"]))
                    echo $_REQUEST["radio1"], "<br>";
            ?>
        </center>
    </body>
</html>
```

你可以在图 10-11 中看到结果——`radiobutton.php`正确地识别了用户选择的单选按钮。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_390_0.png)

## 使用列表框

我们调查中的下一个 HTML 控件是 HTML 列表框，它允许用户从项目列表中进行选择。有两种类型的列表框：

- **单选列表框**：用户只能选择一个项目。这个控件的工作方式与我们已经审查过的控件非常相似。你在网页中为控件命名，并通过`$_REQUEST`（或`$_GET`或`$_POST`）数组获取用户所做的选择。
- **多选列表框**：用户可以从多个项目中选择。你可以在 HTML 中通过`multiple`属性创建这些列表框。你处理这些列表框的方式不同于处理其他控件。

本节的重点是多选列表框。

## 创建 HTML

这个示例`listbox.html`将显示一个包含多种水果选择的列表框。用户可以从列表中进行多项选择，然后由`listbox.php`显示这些选择。在`listbox.html`中，我们从一个表单开始，指明`listbox.php`将接收来自列表框的数据：

```html
<html>
    <head>
        <title>使用列表</title>
    </head>

    <body>
        <center>
            <h1>
                使用列表
            </h1>

            <form method="get" action="listbox.php">
            .
            .
            .
            </form>
        </center>
    </body>
</html>
```

接下来，我们用`<select>`元素创建一个新的多选列表框，添加`multiple`属性使其成为多选列表框，并添加所需的提交按钮：

```html
<html>
    <head>
        <title>使用列表</title>
    </head>

    <body>
        <center>
            <h1>
                使用列表
            </h1>

            <form method="get" action="listbox.php">

                选择你最喜欢的水果：
                <br>
                <br>
                <select name="fruit" multiple>
                    .
                    .
                    .
                </select>
                <br>
                <br>
                <input type="submit" value="提交">
            </form>
        </center>
    </body>
</html>
```

接下来，我们可以用`<option>`元素为列表框填充水果：



```html
<html>
    <head>
        <title>使用列表</title>
    </head>

    <body>
        <center>
            <h1>
                使用列表
            </h1>

            <form method="get" action="listbox.php">
                选择你最喜欢的水果：
                <br>
                <br>
                <select name="fruit" multiple>
                    <option>草莓</option>
                    <option>樱桃</option>
                    <option>苹果</option>
                    <option>西瓜</option>
                </select>
                <br>
                <br>
                <input type="submit" value="提交">
            </form>
        </center>
    </body>
</html>
```

这里是关键：由于这是一个多选列表框，用户在其中做出的选择不会像本章前面的 HTML 示例那样作为单个项目发送到服务器。相反，用户的选择将作为数组发送到服务器。

如何告诉 PHP 为水果列表框期望一个数组？在使用 PHP 时，你需要将控件的名称从单个单词（例如`fruit`）更改为一个数组`fruit[]`。在 HTML 中是这样的：

```html
<html>
    <head>
        <title>使用列表</title>
    </head>

    <body>
        <center>
            <h1>
                使用列表
            </h1>

            <form method="get" action="listbox.php">
                选择你最喜欢的水果：
                <br>
                <br>
                <select name="fruit[]" multiple>
                    <option>草莓</option>
                    <option>樱桃</option>
                    <option>苹果</option>
                    <option>西瓜</option>
                </select>
                <br>
                <br>
                <input type="submit" value="提交">
            </form>
        </center>
    </body>
</html>
```

很好——你可以在图 10-12 中看到这个页面，其中显示了水果，并且用户已经选择了两个（你可以在多选列表框中使用 SHIFT 和 CTRL 键进行多项选择）。

现在是时候创建`listbox.php`了。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_394_0.png)

图 10-12 一个多选列表框

## 创建 PHP

我们以一些 HTML 开始`listbox.php`，这个脚本处理用户在`listbox.html`中做出的选择，用来设置舞台：

```html
<html>
    <head>
        <title>从列表读取选择</title>
    </head>

    <body>
        <center>
            <h1>从列表读取选择</h1>
            你选择了：
            <br>
            .
            .
            .
        </center>
    </body>
</html>
```

我们将使用 HTML 无序列表（使用`<ul>`标签）来显示用户的选择：

```html
<html>
    <head>
        <title>从列表读取选择</title>
    </head>

    <body>
        <center>
            <h1>从列表读取选择</h1>
            你选择了：
            <br>
            <ul>
            .
            .
            .
            </ul>
        </center>
    </body>
</html>
```

要列出所选的水果，我们可以使用 PHP 的`foreach`循环遍历`fruit[]`数组，我们可以通过`$_REQUEST["fruit"]`访问它：

```php
<html>
    <head>
        <title>从列表读取选择</title>
    </head>

    <body>
        <center>
            <h1>从列表读取选择</h1>
            你选择了：
            <br>
            <ul>
            <?php
            foreach($_REQUEST["fruit"] as $fruit){
            .
            .
            .
            }
            ?>
            </ul>
        </center>
    </body>
</html>
```

最后，我们用`<li>`标签将每个选中的水果变成列表中的一个项目：

```php
<html>
    <head>
        <title>从列表读取选择</title>
    </head>

    <body>
        <center>
            <h1>从列表读取选择</h1>
            你选择了：<br>
            <ul>
            <?php
            foreach($_REQUEST["fruit"] as $fruit){
                echo "<li> $fruit </li><br>";
            }
            ?>
            </ul>
        </center>
    </body>
</html>
```

你可以在图 10-13 中看到结果。很酷！

好了，现在让我们看看本章涵盖的最后一个 HTML 控件：图像映射。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_396_0.png)

图 10-13 从多选列表框读取数据

## 使用图像映射

图像是可点击的，包含“热点”，应用程序在你点击它们时会做出响应。你处理图像映射的方式不同于任何其他控件，因为图像映射会发送给你两段数据——用户在图像映射中点击鼠标时的 x 和 y 位置——这意味着你不能只通过一个名称来访问它们的数据。

## 创建 HTML

在这个示例`map.html`中，我们从一些设置场景的 HTML 开始：

```html
<html>
    <head>
        <title>
            使用图像映射
        </title>
    </head>

    <body>
        <center>
            <h1>
                使用图像映射
            </h1>
            .
            .
            .
        </center>
    </body>
</html>
```

我们可以添加一个表单，将图像映射中的点击位置发送到一个名为`map.php`的 PHP 文件：

```html
<html>
    <head>
        <title>
            使用图像映射
        </title>
    </head>

    <body>
        <center>
            <h1>
                使用图像映射
            </h1>
```

图像映射本身是通过一个`<input type="image">`元素创建的，我们将把它命名为 "map"，并使用名为`map.jpg`的图像文件作为显示的图像：

```html
<html>
<head>
<title>
Using Image Maps
</title>
</head>
<body>
<center>
<h1>
Using Image Maps
</h1>
<form method="post" action="map.php">
Click anywhere in the image map.
<br>
<br>
<input name="map" type="image" src="map.jpg">
</form>
</center>
</body>
</html>
```

你可以在图 10-14 中看到结果，其中图像映射即将被用户点击。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_399_0.png)

图 10-14 一个图像映射

现在让我们创建 PHP 文件`map.php`，该文件用于读取并报告图像映射被点击的位置。

## 创建 PHP

在`map.php`中，我们同样以一些 HTML 开始：

```php
<html>
<head>
<title>Reading Image Map Data</title>
</head>
<body>
    <center>
        <h1>Reading Image Map Data</h1>
        <br>
        You clicked the image at (
        .
        .
        .
    </center>
</body>
</html>
```

现在我们需要显示鼠标点击的 x 和 y 位置。包含映射的 HTML 控件的名称就是 "map"，PHP 将自动创建`map_x`来保存 x 坐标，创建`map_y`来保存 y 坐标。这意味着我们可以使用`$_REQUEST`数组来显示用户点击图像映射的位置，如下所示：

```php
<html>
    <head>
        <title>Reading Image Map Data</title>
    </head>

    <body>
        <center>
            <h1>Reading Image Map Data</h1>
            <br>
            You clicked the image at (
            <?php
                echo $_REQUEST["map_x"], ", ", $_REQUEST["map_y"];
            ?>
            ).
        </center>
    </body>
</html>
```

你可以在图 10-15 中看到结果，它显示了用户点击映射的位置（像素坐标），请注意在图像映射中 (0, 0) 位于左上角。

382 Ajax: A Beginner's Guide

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_401_0.png)

图 10-15 从图像映射读取数据

了解鼠标点击的位置对于在网页中激活“热点”非常重要。既然你有了鼠标位置，你就知道点击了哪个热点，并可以在你的 PHP 脚本中采取相应的操作。

# 第 11 章 使用 Ajax 和 PHP 验证用户输入

## 关键技能与概念

- 显示表单中的所有数据
- 使用 PHP 服务器变量
- 以数组形式发送表单数据
- 创建单页 PHP 应用程序
- 验证数字
- 验证文本

前两章让你开始了解用于 Ajax 的 PHP 基础知识，本章将让你对目前用于 Ajax 应用程序的 PHP 有一个良好的实践知识。在本章中，你将学习在 PHP 中所需的技能，包括显示发送到服务器的所有表单数据（这对调试非常有用）；以数组形式处理表单数据（如果数据量很大，这样做很好）；以及创建单页 PHP 应用程序。

到目前为止，我们创建的 PHP 应用程序都由一个 HTML 页面和一个 PHP 页面组成，但大多数 PHP 应用程序将它们全部组合成一个 PHP 页面，你也将在此了解如何做到这一点。

本章还讨论了验证用户输入——即确保用户填写了必填字段并以正确的格式提供数据。你在互联网上见过这样的页面：如果你省略了必填数据，页面会以红色显示错误信息，我们将在本章中了解如何在自己的应用程序中实现这一点。

以下是 PHP 中验证用户输入的框架：你有一个函数，比如命名为`check_data`，用于检查用户的输入（检查操作在 PHP 中完成，是在服务器端执行的）。`check_data`函数将其发现的任何错误存储在一个名为`$errors`的数组中，如果该数组最终包含任何错误条目，你可以显示错误消息（红色），然后再次显示“欢迎”页面，要求用户重新输入数据。另一方面，如果用户的数据没问题，你可以调用第二个函数，比如命名为`process_data`，来处理这些数据。它的结构如下：

```php
check_data();

if(count($errors) != 0){
    display_errors();
    display_welcome();
}
else {
    process_data();
}
```

你将在本章末尾看到这个骨架代码变得具体化。让我们从一个基本的 PHP 技能开始：查看你的 HTML 表单实际发送到服务器的是什么数据。

## 显示 HTML 表单中的所有数据

当你在创建 Ajax 应用程序时，了解你的网页正在向服务器上的 PHP 发送什么数据可能很重要，这是出于调试目的。你的 PHP 脚本实际获取的数据是什么样子的？让我们看一个例子`datadumper.html`，它转储表单发送给它的所有数据。

### 创建 HTML

我们可以从一个将数据发送到`datadumper.php`的表单开始编写`datadumper.html`：

```html
<html>
  <head>
    <title>Displaying All Form Data</title>
  </head>

  <body>
    <center>
      <h1>Displaying All Form Data</h1>

      <form method="post" action="datadumper.php">
        .
        .
        .
      </form>
    </center>
  </body>
</html>
```

我们可以添加一些控件，以便数据确实会被发送到`datadumper.php`，从一个文本字段开始：

```html
<html>
  <head>
    <title>Displaying All Form Data</title>
  </head>

  <body>
    <center>
      <h1>Displaying All Form Data</h1>

      <form method="post" action="datadumper.php">
        Please enter your name:
        <input name="name" type="text">
        <br>
        <br>
        .
        .
        .
      </form>
    </center>
  </body>
</html>
```

我们可能还会发送一些将作为数组发送的数据——比如`fruit[]`——使用列表框，并添加提交按钮：

```html
<html>
  <head>
    <title>Displaying All Form Data</title>
  </head>

  <body>
    <center>
      <h1>Displaying All Form Data</h1>

      <form method="post" action="datadumper.php">
        Please enter your name:
        <input name="name" type="text">
        <br>
        <br>
        Select your favorite fruit:
        <br>
        <br>
        <select name="fruit[]" multiple>
          <option>Bananas</option>
          <option>Strawberries</option>
          <option>Apples</option>
          <option>Watermelons</option>
        </select>
        <br>
        <br>
        <input type="submit" value="Submit">
      </form>
    </center>
  </body>
</html>
```



这就完成了`datadumper.html`，你可以在图 11-1 中看到它。现在是时候编写`datadumper.php`了，这是一个通用的 PHP 脚本，将显示发送给它的所有数据，这对于调试非常方便。

### 创建 PHP

我们在`datadumper.php`中的目标是创建一个通用的 PHP 脚本，无论哪个页面发送表单数据，它都能显示发送给它的表单数据。这意味着我们需要从`$_REQUEST`数组中恢复表单数据，该数组可以处理通过 GET 或 POST 发送的数据，而不仅仅是`$_GET`或`$_POST`数组。让我们从一些设置场景的 HTML 和一个 PHP 部分开始：

```php
<html>
  <head>
    <title>
      Displaying All Form Data
    </title>
  </head>

  <body>
    <center>
      <h1>Displaying All Form Data</h1>
      Here is the form's data I got:
      <br>
      <?php
          // Loop over all data in the $_REQUEST array
          foreach ($_REQUEST as $name => $value) {
              // Display each data item's name and value
              echo "$name: $value<br>\n";
          }
      ?>
    </center>
  </body>
</html>
```

以下是`datadumper.php`的内容，它显示从表单提交的数据：

```php
<html>
<head>
<title>
显示所有表单数据
</title>
</head>
<body>
<center>
<h1>显示所有表单数据</h1>
这是我获取到的表单数据：
<br>
<?php
foreach($_REQUEST as $index => $value){
    .
    .
    .
}
?>
</center>
</body>
</html>
```

循环的第一次迭代中，`$index`将保存文本字段的名称，即`"name"`，而`$value`将保存用户输入到文本字段中的名称。循环的第二次迭代中，`$index`将保存列表框数据数组的名称`"fruit"`，而`$value`将保存实际的`$fruit`数组。

换句话说，我们需要在`datadumper.php`中处理单个项目数据和数组数据。要检查`$value`是否是一个数组，我们可以使用 PHP 函数`is_array`：

```php
<html>
<head>
<title>
显示所有表单数据
</title>
</head>
<body>
<center>
<h1>显示所有表单数据</h1>
这是我获取到的表单数据：
<br>
<?php
foreach($_REQUEST as $index => $value){
    if(is_array($value)){
        .
        .
        .
    }
}
?>
</center>
</body>
</html>
```

如果`$value`是一个数组，我们可以用另一个`foreach`循环来遍历它：

```php
<html>
<head>
<title>
显示所有表单数据
</title>
</head>
<body>
<center>
<h1>显示所有表单数据</h1>
这是我获取到的表单数据：
<br>
<?php
foreach($_REQUEST as $index => $value) {
    if(is_array($value)){
        foreach($value as $number => $item){
            .
            .
            .
        }
    }
}
?>
</center>
</body>
</html>
```

在这个新循环中，我们遍历`$value`变量中的数组；`$number`将保存数组中项目的索引号，`$item`将保存项目本身的名称。这意味着我们可以这样回显数组名称、当前项目的索引以及项目名称本身：

```php
<html>
<head>
<title>
显示所有表单数据
</title>
</head>
<body>
<center>
<h1>显示所有表单数据</h1>
这是我获取到的表单数据：
<br>
<?php
foreach($_REQUEST as $index => $value){
    if(is_array($value)){
        foreach($value as $number => $item){
            echo "${index}[${number}] => $item <br>";
        }
    }
}
?>
</center>
</body>
</html>
```

呼。好的，但如果`$value`不是数组——它只是一个单个项目数据呢？在这种情况下，我们只需要显示该项目的名称及其值：

```php
<html>
<head>
<title>
显示所有表单数据
</title>
</head>
<body>
<center>
<h1>显示所有表单数据</h1>
这是我获取到的表单数据：
<br>
<?php
foreach($_REQUEST as $index => $value){
    if(is_array($value)){
        foreach($value as $number => $item){
            echo "${index}[${number}] => $item <br>";
        }
    }
    else {
        echo $index, " => ", $value, "<br>";
    }
}
?>
</center>
</body>
</html>
```

很好，这完成了`datadumper.php`。在图 11-2 中，你可以看到用户在`datadumper.html`中输入一些数据并点击提交按钮后的实际运行情况。请注意，`datadumper.php`确实正确识别了发送给它的数据——无论是单个项目还是数组。还不错。

## 第 11 章：使用 Ajax 和 PHP 验证用户输入

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_411_0.png)

图 11-2 显示发送到`datadumper.php`的表单数据

### 使用 PHP 服务器变量

PHP 还有许多有用的内置变量，你可以在 PHP 代码中访问它们，称为服务器变量。你可以在表 11-1 中找到 PHP 服务器变量的列表。

| 服务器变量 | 描述 |
| :--- | :--- |
| `AUTH_TYPE` | 在 Apache Web 服务器下运行并进行 HTTP 身份验证时，保存身份验证类型（例如密码身份验证）。 |
| `DOCUMENT_ROOT` | 包含脚本所在的文档根目录。 |
| `GATEWAY_INTERFACE` | 包含服务器使用的 CGI（通用网关接口——服务器与浏览器通信的方式）规范版本。 |
| `HTTP_ACCEPT` | 包含当前请求中`Accept:`头中的文本。 |
| `HTTP_ACCEPT_CHARSET` | 包含当前请求中`Accept-Charset:`头中的文本。 |
| `HTTP_ACCEPT_ENCODING` | 包含当前请求中`Accept-Encoding:`头中的文本。 |
| `HTTP_ACCEPT_LANGUAGE` | 包含当前请求中`Accept-Language:`头中的文本。 |
| `HTTP_CONNECTION` | 包含当前请求中`Connection:`头中的文本。 |
| `HTTP_HOST` | 包含当前请求中`Host:`头中的文本。 |
| `HTTP_REFERER` | 包含将用户代理引导至当前页面的页面地址（如果有的话）。由浏览器设置。 |
| `HTTP_USER_AGENT` | 包含当前请求中`User-Agent:`头中的文本。 |
| `PATH_TRANSLATED` | 指定基于文件系统的脚本路径。 |
| `PHP_AUTH_PW` | 在 Apache Web 服务器下运行并进行 HTTP 身份验证时，保存用户提供的密码。 |
| `PHP_AUTH_USER` | 在 Apache Web 服务器下运行并进行 HTTP 身份验证时，保存用户提供的用户名。 |
| `PHP_SELF` | 包含当前执行脚本的文件名，相对于文档根目录。 |
| `QUERY_STRING` | 包含查询字符串（如果有的话）。 |
| `REMOTE_ADDR` | 包含用户查看当前页面的 IP 地址。 |
| `REMOTE_HOST` | 包含用户查看当前页面的主机名。 |
| `REMOTE_PORT` | 包含用户机器上用于与 Web 服务器通信的端口。 |
| `REQUEST_METHOD` | 指定用于访问页面的请求方法，例如`'GET'`、`'HEAD'`、`'POST'`、`'PUT'`。 |
| `REQUEST_URI` | 指定用于访问此页面的 URI，例如`'/index.html'`。 |
| `SCRIPT_FILENAME` | 指定当前执行脚本的绝对路径名。 |
| `SCRIPT_NAME` | 包含当前脚本的路径。这对于需要指向自身的页面很有用。 |
| `SERVER_ADMIN` | 包含 Web 服务器配置文件中`SERVER_ADMIN`指令给出的值。 |
| `SERVER_NAME` | 包含脚本在其下执行的服务器主机名。 |
| `SERVER_PORT` | 包含服务器机器上用于 Web 服务器通信的端口。 |
| `SERVER_PROTOCOL` | 包含用于请求页面的信息协议的名称和版本。 |
| `SERVER_SIGNATURE` | 包含服务器版本和虚拟主机名。 |
| `SERVER_SOFTWARE` | 包含服务器标识字符串。 |

表 11-1 PHP 服务器变量

PHP 服务器变量对你作为 Ajax 程序员来说可能非常有用。例如，`HTTP_USER_AGENT`保存用户使用的浏览器名称。由于你完全通过浏览器与用户交互，了解他们使用哪个浏览器是很有好处的，因为不同的浏览器具有不同的功能。例如，假设你想在一个`<marquee>`元素中显示用户的姓名，该元素会滚动显示——但仅在 Internet Explorer 中可用。你可以使用`HTTP_USER_AGENT`服务器变量来确定用户是否使用 Internet Explorer。让我们在新示例`servervariables.html`中看看实际操作。

### 创建 HTML

这个 HTML 页面会将数据发送到`servervariables.php`，后者将在一个`<marquee>`元素中显示用户的姓名——如果用户使用 Internet Explorer 的话。这是`servervariables.html`，它以一个将数据发送到`servervariables.php`的表单开始：

```php
<html>
<head>
<title>
使用服务器变量
</title>
</head>
<body>
<center>
<h1>使用服务器变量</h1>
<form method="post" action="servervariables.php">
.
.
.
</form>
</center>
</body>
</html>
```

以下是此示例中的文本字段和提交按钮：

```php
<html>
<head>
<title>
使用服务器变量
</title>
</head>
<body>
<center>
```

第11章：使用Ajax和PHP验证用户输入

## 使用服务器变量

```html
<h1>使用服务器变量</h1>

<form method="post" action="servervariables.php">
    请输入您的姓名：
    <input type="text" name="name">
    <br>
    <br>
    <input type="submit" value="提交">

</form>

</center>
</body>
</html>
```

这就是我们需要的全部内容——你可以看到图11-3中的结果。

## 创建PHP文件

在`servervariables.php`中，我们首先必须确定用户是否使用 Internet Explorer；如果是，我们在一个`<marquee>`元素中显示他们的姓名；如果不是，则显示为普通文本。我们以一些HTML开始`servervariables.php`：

```html
<html>
    <head>
        <title>使用服务器变量</title>
    </head>

    <body>
        <center>
            <h1>使用服务器变量</h1>
```

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_414_0.png)

### Ajax：入门指南

```html
<br>
<?php
.
.
.
?>
</center>
</body>
</html>
```

然后我们检查`HTTP_USER_AGENT`服务器变量，看看它是否包含文本`"MSIE"`——如果用户的浏览器是 Internet Explorer，它就会包含。我们通过PHP的`$_SERVER`数组访问`HTTP_USER_AGENT`服务器变量，并且可以使用`strpos` PHP字符串函数来查找`"MSIE"`——如果字符串中没有`"MSIE"`，`strpos`将返回`false`：

```html
<html>
  <head>
    <title>使用服务器变量</title>
  </head>
  <body>
    <center>
      <h1>使用服务器变量</h1>
      <br>
      <?php
        if(strpos($_SERVER["HTTP_USER_AGENT"], "MSIE")){
          .
          .
          .
        }
      ?>
    </center>
  </body>
</html>
```

如果我们确实在处理 Internet Explorer，我们可以恢复用户的名字并将其显示在一个`<marquee>`元素中，如下所示：

```html
<html>
  <head>
    <title>使用服务器变量</title>
  </head>
  <body>
    <center>
      <h1>使用服务器变量</h1>
```

另一方面，如果我们在处理的不是 Internet Explorer，我们可以在一个简单的`<h1>`标题中显示用户的名字：

```php
<br>
<?php

$name = $_REQUEST["name"];

if(strpos($_SERVER["HTTP_USER_AGENT"], "MSIE")){
    echo("<marquee><h1>欢迎来到我的页面, ${name}!</h1></marquee>");
}
.
.
.
?>

</center>
</body>
</html>
```

```html
<html>
    <head>
        <title>使用服务器变量</title>
    </head>

    <body>
        <center>
            <h1>使用服务器变量</h1>

            <br>
            <?php

            $name = $_REQUEST["name"];

            if(strpos($_SERVER["HTTP_USER_AGENT"], "MSIE")){
                echo("<marquee><h1>欢迎来到我的页面, ${name}!</h1></marquee>");
            }
            else {
                echo("<h1>欢迎来到我的页面, ${name}!</h1>");
            }
            ?>

        </center>
    </body>
</html>
```

结果如图11-4所示，在 Internet Explorer 中，第二行是一个`<marquee>`元素，它在屏幕上滚动显示。很酷。

另一方面，在 Firefox 中，相同的文本显示为一个静态的`<h1>`标题，如图11-5所示。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_417_0.png)

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_417_1.png)

## 以数组格式获取数据

PHP支持一种便捷的方式来组织从HTML表单发送给它的数据。你可以将这些数据存储在数组中，这对于发送大量数据特别有用，尤其是当你的HTML页面包含多个表单时。将你的表单数据组织成数组意味着这些数据项彼此干扰的可能性更小。

## 创建HTML

使用表单数组很简单。只需使用数组和索引名称作为你想存储数据的变量名。例如，这就是在`formarrays.html`中将用户名存储在名为`$data`的数组中，索引为`"name"`的样子：



```html
<html>
<head>
    <title>
        发送表单数组数据
    </title>
</head>

<body>
    <center>
        <h1>
            发送表单数组数据
        </h1>

        <form method="post" action="formarrays.php">

            输入您的姓名：
            <input name="data[name]" type="text">
            .
            .
            .
        </form>

    </center>
</body>
</html>
```

将文本字段的名称设为`data[name]`意味着你可以在PHP脚本中通过`$data["name"]`访问用户名（注意，在HTML页面中命名变量时，你需要省略引号）。以下是我们如何询问用户的身高（英寸）并将其存储为`$data["height"]`的示例：

```html
<html>
    <head>
        <title>
            发送表单数组数据
        </title>
    </head>
```

```html
<body>
    <center>
        <h1>
            发送表单数组数据
        </h1>

        <form method="post" action="formarrays.php">

            输入您的姓名：
            <input name="data[name]" type="text">

            <br>
            <br>
            输入您的身高（英寸）：
            <input name="data[height]" type="text">

            <br>
            <br>
            <input type="submit" value="提交">
        </form>

    </center>
</body>
</html>
```

你可以在图11-6中看到这个页面`formarrays.html`的样子，其中用户输入了一些信息，正准备点击“提交”按钮。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_419_0.png)

图11-6 准备将表单数据以数组形式发送给PHP

## 创建PHP文件

在PHP脚本`formarrays.php`中，你可以恢复包含表单数据的数组并将其命名为`$data`：

```html
<html>
<head>
<title>接收表单数组数据</title>
</head>
<body>
<center>
<h1>接收表单数组数据</h1>
您的姓名是
<?php
$data = $_REQUEST['data'];
.
.
.
</center>
</body>
</html>
```

并且你可以通过引用`$data['name']`来获取用户名：

```html
<html>
<head>
<title>接收表单数组数据</title>
</head>
<body>
<center>
<h1>接收表单数组数据</h1>
您的姓名是
<?php
```

## 402 Ajax：入门指南

```php
$data = $_REQUEST['data'];
echo $data['name'], "<br>";
?>
.
.
.
</center>
</body>
</html>
```

你也可以像这样显示用户的身高（英寸）：

```html
<html>
<head>
<title>
接收表单数组数据
</title>
</head>

<body>
<center>
<h1>
接收表单数组数据
</h1>

您的姓名是
<?php
$data = $_REQUEST['data'];
echo $data['name'], "<br>";
?>

您的身高（英寸）是
<?php
$data = $_REQUEST['data'];
echo $data['height'], "<br>";
?>
</center>
</body>
</html>
```

你可以在图11-7中看到结果。很好。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_422_0.png)

图11-7 显示表单数组数据

## 将应用程序封装到单个PHP页面

你看到的大多数PHP应用程序并不像我们之前那样，从一个HTML页面开始，然后跳转到一个PHP页面。在大多数PHP应用程序中，所有内容都被封装在一个PHP页面中，而在PHP页面中显示所有内容意味着至少要向浏览器返回两个不同的页面：一个欢迎页面，要求用户输入数据；以及一个结果页面，处理他们发送的数据并将结果返回给他们。

那么，这样的应用程序是如何做到这一点的呢？它们如何知道该返回哪个页面？通常的做法是检查是否有数据等待处理——如果没有，应用程序显示欢迎页面；如果有，应用程序处理数据并返回结果页面。

下面是在一个新的单页示例`singlepage.php`中的样子。在欢迎页面中，我们将要求用户提供他们的名字，并在结果页面中显示该名字。那么，我们如何知道是否有数据（即用户名）要处理呢？我们可以检查`$_REQUEST`数组中是否有"name"数据：

```html
<html>
  <head>
    <title>
      单页PHP应用程序
    </title>
  </head>

  <body>
    <center>
      <h1>单页PHP应用程序</h1>
      <?php
        if(isset($_REQUEST["name"])){
      ?>
        .
        .
        .
    </center>
  </body>
</html>
```

## 第11章：使用Ajax和PHP验证用户输入

### 验证用户输入

作为本章的最后一个主题，我们将探讨如何验证用户在网页中输入的数据。他们是否输入了姓名？输入的年龄是数字吗？这些就是我们现在要讨论的问题。

以下是本章开头你首先看到的PHP代码概览，它说明了我们如何检查错误并按需显示：

```php
check_data();

if (count ($errors) != 0){
  display_errors();
  display_welcome();
}
else {
  process_data();
}
```

让我们来构建这个名为`checkdata.php`的示例。在这个例子中，用户将被要求输入姓名。如果他们没有输入姓名而是点击了提交按钮，这将被视为一个错误，并在服务器端由PHP处理。这意味着，如果欢迎页面已经显示，我们不需要再检查文本字段是否包含数据，因为如果文本字段没有数据，欢迎页面本就不会被显示。

相反，我们将使用一个名为`welcome_already_displayed`的`<input type=hidden>`控件来跟踪欢迎页面是否已经显示。这种技术可能比检查文本字段是否有数据更好，因为在某些情况下，你可能希望允许用户将文本字段留空。

以下是我们如何在`checkdata.php`中检查欢迎页面是否已经显示：

```html
<html>
  <head>
    <title>
      验证用户数据
    </title>
  </head>

  <body>
    <center>

      <h1>验证用户数据</h1>
      <?php

        if(isset($_REQUEST["welcome_already_displayed"])){
          .
          .
          .
      ?>

    </center>
  </body>
</html>
```

如果有数据等待我们处理，我们可以在一个新函数`check_data`中检查这些数据，该函数会将发现的任何错误填充到一个名为`$errors`的数组中：

```html
<html>
  <head>
    <title>
      验证用户数据
    </title>
  </head>

  <body>
    <center>

      <h1>验证用户数据</h1>
      <?php
        $errors = array();

        if(isset($_REQUEST["welcome_already_displayed"])){

          check_data();
          .
          .
          .
      ?>

    </center>
  </body>
</html>
```

在`check_data`函数中，我们首先声明`$errors`数组是一个全局数组，不受限于`check_data`函数内部：

```html
<html>
  <head>
    <title>
      验证用户数据
    </title>
  </head>

  <body>
    <center>

      <h1>验证用户数据</h1>
      <?php
        $errors = array();

        if(isset($_REQUEST["welcome_already_displayed"])){
          check_data();
          .
          .
          .
        }

        function check_data()
        {
          global $errors;
          .
          .
          .
        }
      ?>
    </center>
  </body>
</html>
```

现在我们可以自由地检查用户是否在文本字段中输入了任何文本——如果没有，我们将一条错误消息（“请输入您的姓名”）存储到`$errors`数组中：

```html
<html>
  <head>
    <title>
      验证用户数据
    </title>
  </head>

  <body>
    <center>
      <h1>验证用户数据</h1>
      <?php
        $errors = array();

        if(isset($_REQUEST["welcome_already_displayed"])){
          check_data();
          .
          .
          .
        }

        function check_data()
        {
          global $errors;

          if($_REQUEST["name"] == "") {
            $errors[] = "<font color='red'>请输入您的姓名</font>";
          }
        }
      ?>
    </center>
  </body>
</html>
```

回到主代码部分，就在调用`check_data`之后，我们检查`$errors`数组中是否存储了任何错误。如果有，我们使用一个名为`display_errors`的函数显示错误信息，然后使用一个名为`display_welcome`的函数显示欢迎页面的其余部分——以便用户可以再次尝试：

```html
<html>
<head>
<title>
验证用户数据
</title>
</head>
<body>
<center>
<h1>验证用户数据</h1>
<?php
$errors = array();
if(isset($_REQUEST["welcome_already_displayed"])){
  check_data();
  if(count($errors) != 0){
    display_errors();
    display_welcome();
  }
  .
  .
  .
}
?>
</center>
</body>
</html>
```

在`display_errors`函数中，我们将当前的错误信息发送回浏览器：

```html
<html>
<head>
<title>
    验证用户数据
</title>
</head>

<body>
    <center>

        <h1>验证用户数据</h1>
        <?php
        $errors = array();

        if(isset($_REQUEST["welcome_already_displayed"])){

            check_data();

            if(count($errors) != 0){
                display_errors();
                display_welcome();
            }
            .
            .
            .
        }

        function display_errors()
        {
            global $errors;

            foreach ($errors as $error){
                echo $error, "<br>";
            }
        }
        ?>

    </center>
</body>
</html>
```

接下来，在`display_welcome`函数中，我们显示页面的欢迎部分，其中包括文本字段和提示用户输入姓名的提示。请注意，`display_welcome`函数还创建了名为`welcome_already_displayed`的隐藏控件（这样我们就能在服务器端知道欢迎页面已经显示过了）。

```html
<html>
<head>
<title>
    验证用户数据
</title>
</head>

<body>
    <center>
        <h1>验证用户数据</h1>
        <?php
        $errors = array();

        if(isset($_REQUEST["welcome_already_displayed"])){

            check_data();

            if(count($errors) != 0){
                display_errors();
                display_welcome();
            }
            .
            .
            .
        }

        function display_welcome()
        {
            echo '<form method="post" action="checkdata.php">';
            echo '<input type="hidden" name="welcome_already_displayed">';
            echo '请输入您的姓名：';
            echo '<input name="name" type="text">';
            echo '<br><br>';
            echo '<input type="submit" value="提交">';
            echo '</form>';
        }
        ?>

    </center>
</body>
</html>
```

现在，让我们在浏览器中看看我们的成果。你可以在图11-8中看到欢迎页面，用户已经输入了他们的姓名，正准备点击提交按钮。

![图11-8 显示表单数组数据：欢迎页面](img/2cd265cf0a64e9b4b91ab611753cd5d5_425_0.png)

结果页面显示了用户的姓名，如图11-9所示。非常酷。

![图11-9 显示表单数组数据：结果页面](img/2cd265cf0a64e9b4b91ab611753cd5d5_425_1.png)

将PHP应用程序的所有代码放在单个页面中是一项新的、强大的技能。

接下来，你将看到另一种测试欢迎页面是否已经显示的方法——通过在网页中设置一个隐藏控件。

### 单页PHP应用程序

如果姓名数据等待我们处理，我们可以将其回显到浏览器：

```html
<html>
    <head>
        <title>
            单页PHP应用程序
        </title>
    </head>

    <body>
        <center>
            <h1>单页PHP应用程序</h1>
            <?php
                if(isset($_REQUEST["name"])){
            ?>
                您的姓名是
            <?php
                echo $_REQUEST["name"];
                }
                .
                .
                .
            ?>
        </center>
    </body>
</html>
```



另一方面，如果没有姓名数据等待我们处理，我们可以显示欢迎页面，该页面通过使用一个新表单中的文本字段来询问用户的姓名，该表单将把其数据发送回同一页面`singlepage.php`：

```html
<html>
    <head>
        <title>
            单页PHP应用程序
        </title>
    </head>

    <body>
        <center>
            <h1>单页PHP应用程序</h1>
            <?php
                if(isset($_REQUEST["name"])){
            ?>
                您的姓名是
            <?php
                echo $_REQUEST["name"];
                }
                .
                .
                .
            ?>
        else {
        ?>
        <form method="post" action="singlepage.php">
            请输入您的姓名：
            <input name="name" type="text">
            <br>
            <br>
            <input type="submit" value="提交">
        </form>
        <?php
        }
        ?>
        </center>
    </body>
</html>
```

请注意，在单页PHP应用程序中，你可以省略`<form>`元素中的`action`属性，因为默认操作是将表单数据发送回同一页面。这意味着你也可以这样编写`singlepage.php`：

```html
<html>
<head>
    <title>
        单页PHP应用程序
    </title>
</head>
<body>
    <center>
        <h1>单页PHP应用程序</h1>
        <?php
        if(isset($_REQUEST["name"])){
        ?>
        您的姓名是
        <?php
        echo $_REQUEST["name"];
        }
        else {
        ?>
        <form method="post">
            请输入您的姓名：
            <input name="name" type="text">
            <br>
            <br>
            <input type="submit" value="提交">
        </form>
        <?php
        }
        ?>
    </center>
</body>
</html>
```

# 第11章：使用Ajax和PHP验证用户输入

## Ajax：入门指南

```html
<body>
<center>
<h1>验证用户数据</h1>
<?php
$errors = array();

if(isset($_REQUEST["welcome_already_displayed"])){
    check_data();
    if(count($errors) != 0){
        display_errors();
        display_welcome();
    }
}

function display_errors(){
    global $errors;
    foreach ($errors as $error){
        echo $error, "<br>";
    }
}

function display_welcome(){
    echo "<form method='post' action='checkdata.php'>";
    echo "请输入您的姓名";
    echo "<br>";
    echo "<input name='name' type='text'>";
    echo "<br>";
    echo "<br>";
    echo "<input type='submit' value='提交'>";
    echo "<input type='hidden'
        name='welcome_already_displayed' value='data'>";
    echo "</form>";
}
?>

</center>
</body>
</html>
```

另一方面，如果没有错误，我们将调用一个名为`process_data`的函数来处理用户输入的数据：

```html
<html>
  <head>
    <title>
      验证用户数据
    </title>
  </head>

  <body>
    <center>

      <h1>验证用户数据</h1>
      <?php
        $errors = array();

        if(isset($_REQUEST["welcome_already_displayed"])){

          check_data();

          if(count($errors) != 0){
            display_errors();
            display_welcome();
          }
          else {
            process_data();
          }
        }
        .
        .
        .
      ?>

    </center>
  </body>
</html>
```

在本例的`process_data`函数中，我们只是获取用户输入的姓名并显示它：

```php
function process_data()
{
    echo "谢谢。您的姓名是 ";
    echo $_REQUEST["name"];
}
```

## Ajax：入门指南

```php
if(isset($_REQUEST["welcome_already_displayed"])){

    check_data();

    if(count($errors) != 0){
        display_errors();
        display_welcome();
    }
    else {
        process_data();
    }
}
else {
    display_welcome();
}
.
.
.
?>
```

至此代码完成——以下是完整的代码供您参考，文件名为`checkdata.php`：

```html
<html>
    <head>
        <title>
            验证用户数据
        </title>
    </head>

    <body>
        <center>

            <h1>验证用户数据</h1>
            <?php
                $errors = array();

                if(isset($_REQUEST["welcome_already_displayed"])){

                    check_data();

                    if(count($errors) != 0){
                        display_errors();
                        display_welcome();
                    }
                    else {
                        process_data();
                    }
                }
                else {
                    display_welcome();
                }

                function check_data()
                {
                    global $errors;

                    if($_REQUEST["name"] == "") {
                        $errors[] = "<font color='red'>请输入您的姓名</font>";
                    }
                }

                function display_errors()
                {
                    global $errors;

                    foreach ($errors as $error){
                        echo $error, "<br>";
                    }
                }

                function process_data()
                {
                    echo "谢谢。您的姓名是 ";
                    echo $_REQUEST["name"];
                }

                function display_welcome()
                {
                    echo "<form method='post' action='checkdata.php'>";
                    echo "请输入您的姓名";
                    echo "<br>";
                    echo "<input name='name' type='text'>";
                    echo "<br>";
                    echo "<br>";
                    echo "<input type='submit' value='提交'>";
                    echo "<input type='hidden' name='welcome_already_displayed' value='data'>";
                    echo "</form>";
                }
            ?>
        </center>
    </body>
</html>
```

好了，但它能工作吗？请查看图11-10中的`checkdata.php`。

如果用户在点击提交前未输入姓名，他们将看到图11-11所示的结果，其中有一条错误消息要求他们输入姓名。

如果现在输入姓名，例如“史蒂夫”，然后点击提交，该姓名将出现在结果页面中，如图11-12所示。效果不错。

417

![图11-10 显示欢迎页面](img/2cd265cf0a64e9b4b91ab611753cd5d5_436_0.png)

![图11-11 显示错误](img/2cd265cf0a64e9b4b91ab611753cd5d5_436_1.png)

![图11-12 显示结果页面](img/2cd265cf0a64e9b4b91ab611753cd5d5_436_2.png)

## 验证整数

如果你想验证输入数据的实际格式怎么办？例如，如果你坚持要求一个数字必须是整数怎么办？

这里有一个新的例子，`checkdatainteger.php`，它要求用户输入年龄，并在输入的不是整数时提出异议。它如何检查输入的数据是否为整数？代码使用 PHP 的`intval`函数将输入的文本转换为整数，然后使用 PHP 的`strval`函数将其转换回字符串。如果结果与最初输入的值相同，则输入的数据是整数。如果不是，则数据不是整数形式，我们必须将错误消息添加到`$errors`数组中：

```php
if(strcmp($_REQUEST["number"],
    strval(intval($_REQUEST["number"])))) {
    $errors[] = "<font color='red'>请输入一个整数</font>";
}
```

以下是`checkdatainteger.php`的完整代码，其中与`checkdata.php`不同的部分已高亮显示：

```php
<?php
$errors = array();

if(isset($_REQUEST["welcome_already_displayed"])){

    check_data();

    if(count($errors) != 0){
        display_errors();
        display_welcome();
    }
    else {
        process_data();
    }
}
else {
    display_welcome();
}

function check_data()
{
    global $errors;

    if($_REQUEST["number"] == "") {
        $errors[] = "<font color='red'>请输入您的年龄</font>";
    }
    if(strcmp($_REQUEST["number"],
              strval(intval($_REQUEST["number"])))) {
        $errors[] = "<font color='red'>请输入一个整数</font>";
    }
}

function display_errors()
{
    global $errors;

    foreach ($errors as $error){
        echo $error, "<br>";
    }
}

function process_data()
{
    echo "谢谢。您的年龄是 ";
    echo $_REQUEST["number"];
}

function display_welcome()
{
    echo "<form method='post' action='checkdatainteger.php'>";
    echo "请输入您的年龄";
    echo "<br>";
    echo "<input name='number' type='text'>";
    echo "<br>";
    echo "<br>";
    echo "<input type='submit' value='提交'>";
    echo "<input type='hidden'
            name='welcome_already_displayed' value='data'>";
    echo "</form>";
}
?>
```

如您所见，代码与`checkdata.php`的代码基本相同，这表明您可以轻松修改我们的 PHP 验证技术来检查您想要的各类错误。`checkdatainteger.php`应用程序如图11-13所示。

如果您输入的数据不是整数，您将得到一个错误，如图11-14所示。

效果很好。

# 验证文本

你甚至可以使用 PHP 的正则表达式检查来确保文本条目符合正确的格式。正则表达式允许你检查文本的格式，以确保其匹配你提供的模板——详情请参阅`http://perldoc.perl.org/perlre.html`。

## 第11章：使用Ajax和PHP验证用户输入

例如，假设你要确保用户输入的社会安全号码（数字形式为`xxx-xx-xxxx`）格式正确。你可以使用 PHP 的`preg_match`函数来实现这一点，该函数利用正则表达式中数字由`\d`表示的特性，使你的`validate_data`函数如下所示：

```php
function validate_data()
{
    global $errors;

    if(!preg_match('/^\d\d\d-\d\d-\d\d\d\d$/', $_REQUEST["data"])){
        $errors[] =
        "<font color='red'>Please enter a social security number</font>";
    }
}
```

# 第12章

## 使用 HTML DOM 和 Ajax

### 关键技能与概念

- 介绍 DOM
- 使用 DOM 追加元素
- 使用 DOM 替换元素
- 处理 Ajax 超时

网页可以被视为使用 HTML DOM（文档对象模型）的对象集合，这使你能够访问页面中的所有内容。在 Ajax 中，了解如何用新下载的数据更新网页至关重要。你已经看到基本模型是使用`<div>`或`<span>`元素，并简单地用新数据替换该元素的内容：



```javascript
function getData(dataSource, divID)
{
    if (XMLHttpRequestObject) {
        var obj = document.getElementById(divID);
        XMLHttpRequestObject.open("GET", dataSource);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                obj.innerHTML = XMLHttpRequestObject.responseText;
            }
        }
    }
```

除了基本模型，另一个选择是使用动态 HTML，正如你在第 8 章中看到的那样。在那里，你发现了将新数据插入网页的新方法，例如使用`insertAdjacentHTML`方法：

```html
<html>
    <head>
        <title>
            Updating a Page With insertAdjacentHTML
        </title>
    </head>
    <script language="JavaScript">
        function addHTML()
        {
            targetDiv.insertAdjacentHTML("AfterEnd",
                "<p><input type=text value='Hello there.'> See? A new text field.</p>");
        }
    </script>
</script>
</head>
.
```

事实上，还有额外的技术可以用来修改网页而无需刷新该页面，这些技术被整合在 HTML DOM 中。DOM 提供了一种将网页内容视为对象集合的方式，这些对象带有内置的方法和属性，所有这些都可在你的 Ajax 应用程序中使用。

### 认识 DOM

如前所述，DOM 将网页视为对象的集合。解释这一点最简单的方法是通过一个例子，所以我们从一个看起来像 HTML 网页的例子开始：

```html
<html>
  <head>
    <title>
      The Report
    </title>
  </head>

  <body>
    <h1>
      All quiet on the Western front.
    </h1>
  </body>
<html>
```

这只是一个普通的网页，有一个会出现在浏览器标题栏中的标题，以及一些会出现在`<h1>`标题中的文本。但从 DOM 的角度来看，这个简单网页的元素构成了一个对象集合，排列成树状结构。以下是此网页在 DOM 术语中的样子，即一个节点树：

```
<html>
|
-------------------------------------------------------------
|                                                             |
|                                                             |
<head>                                                  <body>
|                                                             |
<title>                                                   <h1>
|                                                             |
The Report                                    All quiet on the Western front.
```

## 426 Ajax：初学者指南

JavaScript 具有以下内置属性，你可以使用它们来处理像这样的网页文档中的 DOM 节点：

| 属性 | 描述 |
| --- | --- |
| `attributes` | 此节点的属性 |
| `childNodes` | 子节点数组 |
| `documentElement` | 文档元素 |
| `firstChild` | 第一个子节点 |
| `lastChild` | 最后一个子节点 |
| `localName` | 节点的本地名称 |
| `name` | 节点的名称 |
| `nextSibling` | 下一个兄弟节点 |
| `nodeName` | 节点的名称 |
| `nodeType` | 节点类型 |
| `nodeValue` | 节点的值 |
| `previousSibling` | 上一个兄弟节点 |

这些 JavaScript 属性将在本章中出现。请注意`nodeType`属性，在 HTML 中它可以具有以下值（在 XML 中，还有九个可能的值）：

1. Element（元素）
2. Attribute（属性）
3. Text node（文本节点）

就 DOM 节点类型而言，我们的页面如下所示：

```
         <html> [Element node]
              |
     -------------------------
     |                         |
     |                         |
     |                         |
     <head> [Element node]     <body> [Element node]
     |                         |
     |                         |
     <title> [Element node]    <h1> [Element node]
     |                         |
     |                         |
     The Report [Text node]    All quiet on the Western front. [Text node]
```

除了上表中列出的属性外，节点在 JavaScript 中还支持以下方法：

| 方法 | 描述 |
|---|---|
| `replaceNode(a, b)` | 用节点 a 替换节点 b |
| `insertBefore(a, b)` | 在节点 b 之前插入节点 a |
| `appendChild(a)` | 将子节点 a 追加到你调用此方法的节点上 |

好的，这就是概述。现在是时候让 DOM 发挥作用了。

### 使用 DOM 和 Ajax 向网页追加新元素

我们将使用 DOM 的第一个用途是向网页的节点树追加新的元素节点。换句话说，我们将使用 Ajax 下载数据，并通过实际创建一个新元素并将其追加到构成网页的 DOM 节点树来显示这些数据。

此页面以一个按钮开始，用户可以点击该按钮使用 Ajax 下载数据：

```html
<body>
  <h1>Appending Elements With the DOM and Ajax</h1>
  <form>
    <input type = "button" value = "Download the message"
           onclick = "getData()">
  </form>
  .
  .
  .
  .
</body>
```

我们还添加了一个`<div>`元素，我们将把下载的数据插入其中：

```html
<body>
  <h1>Appending Elements With the DOM and Ajax</h1>
  <form>
    <input type = "button" value = "Download the message"
           onclick = "getData()">
  </form>
<div id="targetDiv" width =100 height=100>
  <p id="text"></p>
</div>
</body>
```

当按钮被点击时，我们应该下载并显示一个名为`data1.txt`的文件，其内容如下：

> This text was appended using the DOM.

此下载和显示将在一个名为`getData`的函数中进行：

```html
<html>
  <head>
    <title>Appending Elements With the DOM and Ajax</title>
    <script language = "javascript">
      function getData()
      {
        .
        .
        .
      }
    </script>
  </head>
  .
  .
  .
</html>
```

在`getData`函数中，我们首先创建一个 XMLHttpRequest 对象：

```javascript
<script language = "javascript">
  function getData()
  {
    var XMLHttpRequestObject = false;
    if (window.XMLHttpRequest) {
      XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
      XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }
    .
    .
    .
  }
</script>
```

## 第12章：使用HTML DOM和Ajax

接着我们检查该`XMLHttpRequest`对象是否确实被创建了：

```javascript
<script language = "javascript">

function getData()
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        .
        .
        .
    }
}

</script>
```

如果`XMLHttpRequest`对象存在，我们可以通过打开它来配置其下载`data1.txt`：

```javascript
<script language = "javascript">

function getData()
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {

        XMLHttpRequestObject.open("GET", "data1.txt");
        .
        .
        .
    }
}

</script>
```

我们可以将一个匿名函数附加到对象的`onreadystatechange`属性上，以监控数据的下载：

```javascript
<script language = "javascript">

function getData()
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {

        XMLHttpRequestObject.open("GET", "data1.txt");

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                .
                .
                .
            }
        }
    }
}

</script>
```

从文件`data1.txt`下载数据后，我们将创建一个新的`<p>`元素来容纳该数据，并将这个`<p>`元素追加到我们网页中已有的`<div>`元素（位于按钮下方）。下面是我们如何使用`createElement`方法创建一个新的`<p>`元素：

```javascript
<script language = "javascript">

function getData()
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {

        XMLHttpRequestObject.open("GET", "data1.txt");

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                var newPElement = document.createElement("p");
                .
                .
                .
            }
        }

    }
}
```

你不能直接将文本插入到`<p>`元素或任何其他 HTML 元素中——你必须首先将文本插入到一个文本节点中。因此，我们首先创建一个新的文本节点来插入文本（注意我们将下载的数据`XMLHttpRequestObject.responseText`放入了文本节点）：



```javascript
<script language = "javascript">

function getData()
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {

        XMLHttpRequestObject.open("GET", "data1.txt");

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                var newPElement = document.createElement("p");
                var newText =
                    document.createTextNode(XMLHttpRequestObject.responseText);
                .
                .
                .
            }
        }

    }
}

XMLHttpRequestObject.send(null);
}
}
</script>
```

现在我们必须将新的文本节点放入 `<p>` 元素中，我们可以使用 `appendChild` 方法来完成：

```javascript
<script language = "javascript">
function getData()
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", "data1.txt");

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                var newPElement = document.createElement("p");
                var newText =
                    document.createTextNode(XMLHttpRequestObject.responseText);
                newPElement.appendChild(newText);
                .
                .
                .
            }
        }

        XMLHttpRequestObject.send(null);
    }
}
</script>
```

很好，这样就将下载的数据放入了 `<p>` 元素。最后一步是使用 DOM 方法将 `<p>` 元素插入到网页中。我们可以通过获取对应目标 `<div>` 元素的对象，并使用 `appendChild` 方法将 `<p>` 元素插入到网页中来完成：

```javascript
<script language = "javascript">

  function getData()
  {
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
      XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
      XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {

      XMLHttpRequestObject.open("GET", "data1.txt");

      XMLHttpRequestObject.onreadystatechange = function()
      {
        if (XMLHttpRequestObject.readyState == 4 &&
            XMLHttpRequestObject.status == 200) {
          var newPElement = document.createElement("p");
          var newText =
            document.createTextNode(XMLHttpRequestObject.responseText);
          newPElement.appendChild(newText);
          var divElement = document.getElementById("targetDiv");
          divElement.appendChild(newPElement);
        }
      }

      XMLHttpRequestObject.send(null);
    }
  }
</script>
```

这是整个页面 `appender.html`：

```html
<html>
  <head>
    <title>使用 DOM 和 Ajax 追加元素</title>

    <script language = "javascript">

      function getData()
      {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
          XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {
            XMLHttpRequestObject.open("GET", "data1.txt");

            XMLHttpRequestObject.onreadystatechange = function()
            {
                if (XMLHttpRequestObject.readyState == 4 &&
                    XMLHttpRequestObject.status == 200) {
                    var newPElement = document.createElement("p");
                    var newText = 
                        document.createTextNode(XMLHttpRequestObject.responseText);
                    newPElement.appendChild(newText);
                    var divElement = document.getElementById("targetDiv");
                    divElement.appendChild(newPElement);
                }
            }

            XMLHttpRequestObject.send(null);
        }
      }
</script>
</head>
<body>
<h1>使用 DOM 和 Ajax 追加元素</h1>
<form>
    <input type = "button" value = "下载消息"
        onclick = "getData()">
</form>
<div id="targetDiv" width =100 height=100>
    <p id="text"></p>
</div>
</body>
</html>
```

你可以在图 12-1 中看到这是如何工作的：用户点击了下载按钮，数据被下载并插入到一个新的 `<p>` 元素中，随后该 `<p>` 元素使用 DOM 方法插入到了页面中。非常好。

除了使用 DOM 追加元素，你还可以替换它们。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_454_0.png)

图 12-1 使用 DOM 追加新元素

## 使用 DOM 替换元素

正如你在上一节所看到的，你可以使用 `appendChild` 方法使用 DOM 追加子节点。你也可以使用 `replaceChild` 方法完全替换子节点，我们将在一个新示例 `replacer.html` 中看看它是如何工作的。这个示例将有一个 ID 为 `"targetDiv"` 的 `<div>` 元素：

```html
<body>
    <h1>使用 DOM 替换元素</h1>
    .
    .
    <div id="targetDiv" width=100 height=100>
    .
    .
    </div>
</body>
```

这就是我们将要替换其子节点的 `<div>` 元素。为了实现这一点，我们必须先给它一个子节点，因此让我们像这样在 `<div>` 元素中包含一个 ID 为 `"text"` 的 `<p>` 元素：

```html
<body>
    <h1>使用 DOM 替换元素</h1>
    .
    .
    .
```

## 436 Ajax：入门指南

```html
<div id="targetDiv" width=100 height=100>
  <p id="text">获取的消息将显示在此处。</p>
</div>

</body>
```

因此，这就是我们要操作替换的元素——ID 为 `"text"` 的 `<p>` 元素。我们还需要一个按钮，当点击时，将使用 Ajax 下载新的文本并替换该 `<p>` 元素。新文本将位于名为 `replace1.txt` 的文件中，下面是下载此文件的按钮：

```html
<body>
  <h1>使用 DOM 替换元素</h1>
  <form>
    <input type="button" value="下载消息 1"
           onclick="getData('1')">
    .
    .
    .
  </form>

  <div id="targetDiv" width=100 height=100>
    <p id="text">获取的消息将显示在此处。</p>
  </div>

</body>
```

也就是说，要下载 `replace1.txt` 文件，你只需将 `"1"` 传递给 JavaScript 函数 `getData`。让我们添加第二个按钮来下载另一个文件 `replace2.txt`。当你下载 `replace2.txt` 时，该文件中的文本将替换 `<p>` 元素。第二个按钮的样子如下：

```html
<body>
  <h1>使用 DOM 替换元素</h1>
  <form>
    <input type="button" value="下载消息 1"
           onclick="getData('1')">
    <input type="button" value="下载消息 2"
           onclick="getData('2')">
  </form>

  <div id="targetDiv" width=100 height=100>
    <p id="text">获取的消息将显示在此处。</p>
  </div>

</body>
```

## 第 12 章：使用 HTML DOM 和 Ajax

好了，我们准备编写 JavaScript 来下载 `replace1.txt` 和 `replace2.txt`。以下是 `replace1.txt` 中的文本：

此文本使用 DOM 替换了之前的文本。

以下是 `replace2.txt` 中的文本：

此文本也使用 DOM 替换了之前的文本。

现在是时候编写 `getData` 函数了，它将执行实际的下载和替换操作：

```javascript
<script language="javascript">
    function getData(number)
    {
        .
        .
        .
    }
</script>
```

首先，我们将创建一个新的 `XMLHttpRequest` 对象：

```javascript
<script language="javascript">
    function getData(number)
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }
        .
        .
        .
    }
</script>
```

然后我们检查 `XMLHttpRequest` 对象是否确实已创建：

```javascript
<script language="javascript">
    function getData(number)
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }
    }
</script>
```

438 Ajax：入门指南

```javascript
if (XMLHttpRequestObject) {
.
.
}
}
```

```html
</script>
```

如果 `XMLHttpRequest` 对象确实已创建，我们可以配置它来下载 `replace1.txt` 或 `replace2.txt`，这取决于传递给 `getData` 函数的是 `"1"` 还是 `"2"`：

```javascript
<script language="javascript">

function getData(number)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {

        XMLHttpRequestObject.open("GET", "replace" + number + ".txt");
        .
        .
        .
    }
}
```

```html
</script>
```

接下来，我们将一个匿名内部函数附加到 `onreadystatechange` 属性：



```javascript
<script language="javascript">

function getData(number)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }
}
```

## 第 12 章：使用 HTML DOM 和 Ajax

```javascript
if(XMLHttpRequestObject) {

    XMLHttpRequestObject.open("GET", "replace" + number + ".txt");

    XMLHttpRequestObject.onreadystatechange = function()
    {
    .
    .
    .
    }

}
}
</script>
```

我们可以通过`status`和`readyState`属性来检查下载何时完成：

```javascript
<script language="javascript">

function getData(number)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {

        XMLHttpRequestObject.open("GET", "replace" + number + ".txt");

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                .
                .
                .
            }
        }

    }
}
</script>
```

### Ajax：入门指南

现在我们已经下载了新文本，是时候创建我们新的`<p>`元素了，我们将用它来替换现有的`<p>`元素。以下是我们如何使用`createElement`方法创建新的`<p>`元素：

```javascript
<script language="javascript">

    function getData(number)
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {

            XMLHttpRequestObject.open("GET", "replace" + number + ".txt");

            XMLHttpRequestObject.onreadystatechange = function()
            {
                if (XMLHttpRequestObject.readyState == 4 &&
                    XMLHttpRequestObject.status == 200) {
                    var newPElement = document.createElement("p");
                    .
                    .
                    .
                }
            }

        }
    }

</script>
```

请注意，当前的`<p>`元素——即将被替换的那个——的 ID 是`"text"`。我们也将给新的`<p>`元素相同的 ID，以便它可以被后续的按钮点击所替换：

```javascript
<script language="javascript">

    function getData(number)
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
```

## 第 12 章：使用 HTML DOM 和 Ajax

```javascript
XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
}

if(XMLHttpRequestObject) {

    XMLHttpRequestObject.open("GET", "replace" + number + ".txt");

    XMLHttpRequestObject.onreadystatechange = function()
    {
        if (XMLHttpRequestObject.readyState == 4 &&
            XMLHttpRequestObject.status == 200) {
            var newPElement = document.createElement("p");
            newPElement.setAttribute("id", "text");
            .
            .
            .
        }
    }
}

</script>
```

在将新下载的文本`XMLHttpRequestObject.responseText`放入`<p>`元素之前，我们需要先将其放入自己的文本节点中，我们按如下方式创建新的文本节点：

```javascript
<script language="javascript">

    function getData(number)
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {

            XMLHttpRequestObject.open("GET", "replace" + number + ".txt");

            XMLHttpRequestObject.onreadystatechange = function()
            {
                if (XMLHttpRequestObject.readyState == 4 &&
                    XMLHttpRequestObject.status == 200) {
                    var newPElement = document.createElement("p");
                    newPElement.setAttribute("id", "text");
```

### Ajax：入门指南

```javascript
var newText = document.createTextNode(XMLHttpRequestObject
    .responseText);
.
.
.
}
}

}
}

</script>
```

我们将新的文本节点追加到新的`<p>`元素中，方法如下：

```javascript
<script language = "javascript">

function getData(number)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {

        XMLHttpRequestObject.open("GET", "replace" + number + ".txt");

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                var newPElement = document.createElement("p");
                newPElement.setAttribute("id", "text");
                var newText = document.createTextNode(XMLHttpRequestObject
                    .responseText);
                newPElement.appendChild(newText);
                .
                .
                .
            }
        }

    }
}

</script>
```

接下来，我们获取一个对应于`<div>`元素的对象：

```javascript
<script language = "javascript">

    function getData(number)
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {

            XMLHttpRequestObject.open("GET", "replace" + number +  ".txt");

            XMLHttpRequestObject.onreadystatechange = function()
            {
                if (XMLHttpRequestObject.readyState == 4 &&
                    XMLHttpRequestObject.status == 200) {
                    var newPElement = document.createElement("p");
                    newPElement.setAttribute("id", "text");
                    var newText = document.createTextNode(XMLHttpRequestObject
                        .responseText);
                    newPElement.appendChild(newText);
                    var divElement = document.getElementById("targetDiv");
                    .
                    .
                    .
                }
            }

        }
    }

</script>
```

我们还要获取一个对应于我们希望替换的`<p>`元素的对象：

```javascript
<script language = "javascript">

    function getData(number)
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {

            XMLHttpRequestObject.open("GET", "replace" + number +  ".txt");

            XMLHttpRequestObject.onreadystatechange = function()
            {
              if (XMLHttpRequestObject.readyState == 4 &&
                  XMLHttpRequestObject.status == 200) {
                var newPElement = document.createElement("p");
                newPElement.setAttribute("id", "text");
                var newText = document.createTextNode(XMLHttpRequestObject
                    .responseText);
                newPElement.appendChild(newText);
                var divElement = document.getElementById("targetDiv");
                var oldPElement = document.getElementById("text");
                .
                .
                .
              }
            }

            XMLHttpRequestObject.send(null);
          }
        }

</script>
```

现在，我们准备好使用`replaceChild`方法将旧的`<p>`元素替换为新的`<p>`元素了。我们按照顺序将新元素和旧元素传递给`replaceChild`，方式如下：



```javascript
<script language = "javascript">

function getData(number)
{
  var XMLHttpRequestObject = false;

  if (window.XMLHttpRequest) {
    XMLHttpRequestObject = new XMLHttpRequest();
  } else if (window.ActiveXObject) {
    XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
  }

  if(XMLHttpRequestObject) {

    XMLHttpRequestObject.open("GET", "replace" + number +  ".txt");

    XMLHttpRequestObject.onreadystatechange = function()
    {
      if (XMLHttpRequestObject.readyState == 4 &&
          XMLHttpRequestObject.status == 200) {
        var newPElement = document.createElement("p");
        newPElement.setAttribute("id", "text");
        var newText = document.createTextNode(XMLHttpRequestObject.responseText);
        newPElement.appendChild(newText);
        var divElement = document.getElementById("targetDiv");
        var oldPElement = document.getElementById("text");
        divElement.replaceChild(newPElement, oldPElement);
      }
    }

    XMLHttpRequestObject.send(null);
  }
}

</script>
```

这样就完成了替换。剩下的就是使用 `send` 方法连接到服务器：

```javascript
<script language = "javascript">

function getData(number)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {

        XMLHttpRequestObject.open("GET", "replace" + number +  ".txt");

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                var newPElement = document.createElement("p");
                newPElement.setAttribute("id", "text");
                var newText = document.createTextNode(XMLHttpRequestObject.responseText);
                newPElement.appendChild(newText);
                var divElement = document.getElementById("targetDiv");
                var oldPElement = document.getElementById("text");
                divElement.replaceChild(newPElement, oldPElement);
            }
        }

        XMLHttpRequestObject.send(null);
    }
}

</script>
```

很好——这是供参考的完整 `replacer.html` 文件：

```html
<html>
  <head>
    <title>Replacing Elements With the DOM</title>
    <script language = "javascript">
      function getData(number)
      {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
          XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
          XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {

          XMLHttpRequestObject.open("GET", "replace" + number + ".txt");

          XMLHttpRequestObject.onreadystatechange = function()
          {
            if (XMLHttpRequestObject.readyState == 4 &&
              XMLHttpRequestObject.status == 200) {
              var newPElement = document.createElement("p");
              newPElement.setAttribute("id", "text");
              var newText = document.createTextNode(XMLHttpRequestObject
                .responseText);
              newPElement.appendChild(newText);
              var divElement = document.getElementById("targetDiv");
              var oldPElement = document.getElementById("text");
              divElement.replaceChild(newPElement, oldPElement);
            }
          }

          XMLHttpRequestObject.send(null);
        }
      }
    </script>
  </head>
  <body>
    <h1>Replacing Elements With the DOM</h1>
    <form>
      <input type = "button" value = "Download message 1"
        onclick = "getData('1')">
      <input type = "button" value = "Download message 2"
        onclick = "getData('2')">
    </form>
    <div id="targetDiv" width =100 height=100>
      <p id="text">The fetched message will appear here.</p>
    </div>
  </body>
</html>
```

您可以在图 12-2 中看到结果——当用户点击按钮 1 时，第一条消息被下载并显示。而且，如图 12-3 所示，当用户点击按钮 2 时，第二条消息被下载并显示。

## 处理 Ajax 中的超时

假设你已准备好在 Ajax 中为用户下载请求的文件或数据项，但却找不到它。你该怎么办？在等待一段时间后若下载仍未发生，你应该通知用户操作已超时。否则，你的 Ajax 应用程序将一直等待一个不存在的资源或已断开的连接。

以下是一个示例 `timeout.html`，它展示了如何在 Ajax 操作在一定时间后未成功时进行超时处理。在这个例子中，我们将尝试下载一个不存在的文件 `data.txt`，然后当操作失败时，我们将超时并显示一个消息框给用户。我们以 `timeout.html` 开始，其中包含一个按钮，用户可以点击该按钮在名为 `getData` 的函数中尝试下载 `data.txt`：

```html
<body>
	<H1>处理 Ajax 超时</H1>
	<form>
		<input type = "button" value = "下载消息"
			onclick = "getData('data.txt', 'targetDiv')">
	</form>
</body>
```

我们将添加一个 `<div>` 元素来显示结果：

```html
<body>
	<H1>处理 Ajax 超时</H1>
	<form>
		<input type = "button" value = "下载消息"
			onclick = "getData('data.txt', 'targetDiv')">
	</form>
	<div id="targetDiv">
		<p>获取的数据将显示在这里。</p>
	</div>
</body>
```

接下来，我们将创建 `getData` 函数：

```javascript
<script language = "javascript">
	function getData(dataSource, divID)
	{
		...
	}
</script>
```

我们需要一个 `XMLHttpRequest` 对象：

```javascript
<script language = "javascript">
function getData(dataSource, divID)
{
    var XMLHttpRequestObject = false;
    
    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }
    .
    .
    .
}
</script>
```

我们将使用 JavaScript 的 `setTimeout` 函数来设置超时。其思路是，如果数据在一秒（1000 毫秒）内未下载完成，我们将停止下载尝试，并在消息框中显示错误消息。我们通过配置 `XMLHttpRequest` 对象来开始这个过程：

```javascript
<script language = "javascript">
function getData(dataSource, divID)
{
    var XMLHttpRequestObject = false;
    
    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }
    
    if(XMLHttpRequestObject) {
        
        XMLHttpRequestObject.open("GET", dataSource);
        .
        .
        .
    }
}
</script>
```

现在，我们将附加一个匿名函数来监控下载过程：

```javascript
<script language = "javascript">
function getData(dataSource, divID)
{
    var XMLHttpRequestObject = false;
    
    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }
    
    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", dataSource);
    
        XMLHttpRequestObject.onreadystatechange = function()
        {
        .
        .
        .
        }
    }
}
</script>
```

当下载开始时，`readyState` 属性的值将为 1，我们希望在此时启动我们的超时计时器。我们不希望在超时已被设置的情况下再次设置（这会将其重置为 0），因此我们将引入一个名为 `timeoutIsSet` 的变量，并以如下方式检查超时是否已被设置：

```javascript
<script language = "javascript">
function getData(dataSource, divID)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", dataSource);

        var timeoutIsSet = false;

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 1) {
                if(!timeoutIsSet){
                .
                .
                .
                }
            }
        }
    }
}
</script>
```

要设置超时，我们将使用 `setTimeout` 函数在 1000 毫秒后调用另一个匿名函数：



```javascript
<script language = "javascript">
  function getData(dataSource, divID)
  {
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
      XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
      XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
      var obj = document.getElementById(divID);
      XMLHttpRequestObject.open("GET", dataSource);

      var timeoutIsSet = false;
      var downloadWentOK = false;

      XMLHttpRequestObject.onreadystatechange = function()
      {
        if (XMLHttpRequestObject.readyState == 1) {
          if(!timeoutIsSet){
            window.setTimeout(function(){
            .
            .
            .
            },
            1000);
            timeoutIsSet = true;
          }
        }
      }
    }
  }
</script>
```

在这个匿名函数中，我们将通过检查一个名为`downloadWentOK`的变量值来判断下载是否成功：

```javascript
<script language = "javascript">
  function getData(dataSource, divID)
  {
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
      XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if (XMLHttpRequestObject) {
        var obj = document.getElementById(divID);
        XMLHttpRequestObject.open("GET", dataSource);

        var timeoutIsSet = false;
        var downloadWentOK = false;

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 1) {
                if (!timeoutIsSet) {
                    window.setTimeout(function() {
                        if (!downloadWentOK) {
                            .
                            .
                            .
                        }
                    }, 1000);
                    timeoutIsSet = true;
                }
            }
        }
    }
}
</script>
```

如果在操作超时之前数据尚未下载完成，我们可以显示错误信息并使用`XMLHttpRequest`对象的`abort`方法中止 Ajax 操作：

```javascript
<script language = "javascript">
    function getData(dataSource, divID)
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }

        if (XMLHttpRequestObject) {
            var obj = document.getElementById(divID);
            XMLHttpRequestObject.open("GET", dataSource);

            var timeoutIsSet = false;
            var downloadWentOK = false;

            XMLHttpRequestObject.onreadystatechange = function()
            {
                if (XMLHttpRequestObject.readyState == 1) {
                    if(!timeoutIsSet){
                        window.setTimeout(function(){
                            if(!downloadWentOK){
                                alert("抱歉，操作已超时。");
                                XMLHttpRequestObject.abort();
                            }
                        },
                        1000);
                        timeoutIsSet = true;
                    }
                }
            }
        }
    }
</script>
```

另一方面，如果下载操作确实成功了，我们可以显示数据并将`downloadWentOK`变量设置为`true`：

```javascript
<script language = "javascript">
function getData(dataSource, divID)
{
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        var obj = document.getElementById(divID);
        XMLHttpRequestObject.open("GET", dataSource);

        var timeoutIsSet = false;
        var downloadWentOK = false;

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 1) {
                if(!timeoutIsSet){
                    window.setTimeout(function(){
                        if(!downloadWentOK){
                            alert("抱歉，操作已超时。");
                            XMLHttpRequestObject.abort();
                        }
                    },
```

## 第12章：使用 HTML DOM 和 Ajax

### Ajax：入门指南

```javascript
        1000);
        timeoutIsSet = true;
      }
    }

    if (XMLHttpRequestObject.readyState == 4 &&
        XMLHttpRequestObject.status == 200) {
      downloadWentOK = true;
      obj.innerHTML = XMLHttpRequestObject.responseText;
    }
  }

  XMLHttpRequestObject.send(null);
}
}
</script>
```

请注意，在前面代码的末尾，我们使用了`XMLHttpRequest`对象的`send`方法来尝试下载数据。下面是完整的示例，`timeout.html`：

```html
<html>
  <head>
    <title>处理 Ajax 超时</title>

    <script language = "javascript">
      function getData(dataSource, divID)
      {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
          XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
          XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {
          var obj = document.getElementById(divID);
          XMLHttpRequestObject.open("GET", dataSource);

          var timeoutIsSet = false;
          var downloadWentOK = false;

          XMLHttpRequestObject.onreadystatechange = function()
          {
            if (XMLHttpRequestObject.readyState == 1) {
              if(!timeoutIsSet){
                window.setTimeout(function(){
                  if(!downloadWentOK){
                    alert("Sorry, but I timed out.");
                    XMLHttpRequestObject.abort();
                  }
                },
                1000);
                timeoutIsSet = true;
              }
            }

            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
              downloadWentOK = true;
              obj.innerHTML = XMLHttpRequestObject.responseText;
            }
          }

          XMLHttpRequestObject.send(null);
        }
      }
    </script>
  </head>

  <body>
    <H1>处理 Ajax 超时</H1>

    <form>
        <input type = "button" value = "下载消息"
               onclick = "getData('data.txt', 'targetDiv')">
    </form>

    <div id="targetDiv">
        <p>获取的数据将显示在这里。</p>
    </div>
  </body>
</html>
```

因为此示例尝试下载的文件`data.txt`不存在，所以在此情况下 Ajax 操作超时，如图 12-4 中的消息框所示。很酷。

![img](img/2cd265cf0a64e9b4b91ab611753cd5d5_474_0.png)

## 使用 Ajax 下载图像

我们将查看本章的最后一个示例，展示如何使用 Ajax 下载图像。“那是什么？”你问。“下载图像？Ajax 不能只下载基于文本的数据吗？”

没错，你只能下载文本。但该文本可以是你要下载的图像文件的名称，如果你使用该图像的文件名创建一个 HTML `<img>`元素，那么浏览器——通过动态 HTML 的魔力——会立即下载图像，无需刷新页面。

下面是一个示例`images.html`，展示了这一操作。首先，我们可以在页面上添加两个按钮，让用户下载两张图像中的一张（图像 1 或图像 2），以及一个`<div>`元素来显示新图像：

```html
<body>
  <H1>使用 Ajax 下载图像</H1>

  <form>
    <input type = "button" value = "显示图像 1"
      onclick = 
        "getData('imageName1.txt', callback)">
    <input type = "button" value = "显示图像 2"
      onclick = 
        "getData('imageName2.txt', callback)">
  </form>

  <div id="targetDiv">
    <p>获取的图像将显示在这里。</p>
  </div>
</body>
```

请注意，`getData`函数被要求下载`imageName1.txt`或`imageName2.txt`，这些是包含要使用动态 HTML 下载的图像名称的文件。`imageName1.txt`的内容如下：

```
Image1.jpg
```

`imageName2.txt`的内容如下：

```
Image2.jpg
```

因此，我们实际上使用 Ajax 下载的是图像文件的名称。下载该名称后，我们可以将其传递给一个新函数（比如命名为`callback`）来创建新的`<img>`元素：



```javascript
<script language = "javascript">

  function getData(imageName, callback)
  {
    var XMLHttpRequestObject = false;

    if (window.XMLHttpRequest) {
        XMLHttpRequestObject = new XMLHttpRequest();
    } else if (window.ActiveXObject) {
        XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
    }

    if(XMLHttpRequestObject) {
        XMLHttpRequestObject.open("GET", imageName);

        XMLHttpRequestObject.onreadystatechange = function()
        {
            if (XMLHttpRequestObject.readyState == 4 &&
                XMLHttpRequestObject.status == 200) {
                    callback(XMLHttpRequestObject.responseText);
                    delete XMLHttpRequestObject;
                    XMLHttpRequestObject = null;
            }
        }

        XMLHttpRequestObject.send(null);
    }
  }
  .
  .
  .
</script>
```

在`callback`函数中，我们使用图像名称创建一个新的`<img>`元素，将其放入目标`<div>`元素，如下所示：

```javascript
<script language = "javascript">

    function getData(imageName, callback)
    {
        var XMLHttpRequestObject = false;

        if (window.XMLHttpRequest) {
            XMLHttpRequestObject = new XMLHttpRequest();
        } else if (window.ActiveXObject) {
            XMLHttpRequestObject = new ActiveXObject("Microsoft.XMLHTTP");
        }

        if(XMLHttpRequestObject) {
            XMLHttpRequestObject.open("GET", imageName);

            XMLHttpRequestObject.onreadystatechange = function()
            {
                if (XMLHttpRequestObject.readyState == 4 &&
                    XMLHttpRequestObject.status == 200) {
                    callback(XMLHttpRequestObject.responseText);
                    delete XMLHttpRequestObject;
                    XMLHttpRequestObject = null;
                }
            }
            XMLHttpRequestObject.send(null);
        }
    }

    function callback(imageName)
    {
        document.getElementById("targetDiv").innerHTML =
        "<img border='1' src= " + imageName + ">";
    }
</script>
```

就是这样——现在我们已经下载了用户想要看到的图像名称，并显示了该图像。以下是整个应用程序，`images.html`：

```html
<html>
<head>
    <title>使用 Ajax 下载图像</title>
    <script language = "javascript">
        function getData(imageName, callback)
        {
            var XMLHttpRequestObject = false;
            if (window.XMLHttpRequest) {
                XMLHttpRequestObject = new XMLHttpRequest();
            } else if (window.ActiveXObject) {
                XMLHttpRequestObject = new
                ActiveXObject("Microsoft.XMLHTTP");
            }
            if(XMLHttpRequestObject) {
                XMLHttpRequestObject.open("GET", imageName);
                XMLHttpRequestObject.onreadystatechange = function()
                {
                    if (XMLHttpRequestObject.readyState == 4 &&
                        XMLHttpRequestObject.status == 200) {
                        callback(XMLHttpRequestObject.responseText);
                        delete XMLHttpRequestObject;
                        XMLHttpRequestObject = null;
                    }
                }
                XMLHttpRequestObject.send(null);
            }
        }

        function callback(imageName)
        {
            document.getElementById("targetDiv").innerHTML =
                "<img border='1' src= " + imageName + ">";
        }
    </script>
</head>

<body>
    <H1>使用 Ajax 下载图像</H1>

    <form>
        <input type = "button" value = "显示图像 1"
            onclick =
                "getData('imageName1.txt', callback)">
        <input type = "button" value = "显示图像 2"
            onclick =
                "getData('imageName2.txt', callback)">
    </form>

    <div id="targetDiv">
        <p>获取的图像将显示在这里。</p>
    </div>
</body>
</html>
```

你可以在图 12-5 中看到结果，其中用户点击了按钮 1 并下载了图像 1——无需刷新浏览器窗口。在图 12-6 中，你可以看到用户如何通过点击按钮 2 来下载图像 2。很酷。当然，这只是一个示例——当从服务器发送的图像根据发送到服务器的数据而变化时，该技术的真正威力才会显现。

Ajax：入门指南

![img](img/2cd265cf0a64e9b4b91ab611753cd5d5_479_0.png)

图 12-5 下载图像 1

![img](img/2cd265cf0a64e9b4b91ab611753cd5d5_479_1.png)

图 12-6 下载图像 2

## 索引

### 符号

- `,`（逗号），349
- `.`（点操作符），319
- `;`（分号），22, 237
- `&&`（与操作符），49–50, 333
- `&`（和号），83
- `\`（反斜杠），328
- `$`（美元符号），170–171, 327
- `!`（感叹号），139
- `/`（正斜杠），331, 332
- `//`（双正斜杠），23, 315
- `-`（连字符），232
- `-`（减号），331, 332
- `||`（或操作符），49, 50–51
- `+`（加号），42–43, 83, 331, 332
- `"`（双引号），23, 27, 187, 326
- `'`（单引号），27
- `#`（井号），239, 315–316
- `[ ]`（方括号），53, 71, 329, 333
- `{ }`（花括号），29, 327, 332, 336
- `*/`字符，23, 316
- `/*`字符，23, 316
- `*`操作符，39, 331, 332
- `++`操作符，51
- `--`操作符，51
- `=>`操作符，388

### A

- 绝对定位，245–250
- `action`属性，357
- `ActiveXObject`，67
- Adaptive Path，5
- `adder`函数，126, 351–356
- 加法运算符，43
- `AfterBegin`常量，269
- `AfterEnd`常量，269
- Ajax（异步 JavaScript 和 XML）
  - 基础，1–14
  - 示例，7–9
  - 概述，5–7
  - 超时处理，448–455
  - 与 XML 结合使用，94–102
- Ajax 应用程序。参见 Web 应用程序
- Ajax 框架，147–181
  - AJAXLib 框架，179–181
  - 构建库，148–149
  - 描述，148
  - `downloadText`函数，148, 149–157
  - `downloadXml`函数，148, 157–164
  - `libXmlRequest`，176–179
  - `postDataDownloadText`函数，148, 164–170
  - `postDataDownloadXml`函数，149, 170–176
- `ajax2.html`文档，80–82
- `ajax3.html`文档，85–88, 105
- `ajax4.html`文档，89–94
- `ajaxframework.js`脚本，148–181
- `ajax.html`文档，60–79
  - 分析，63–64
  - 连接到服务器，78–79
  - 为其创建 JavaScript，64–65
  - 创建`XMLHttpRequest`对象，66–70
  - 数据下载，73–77
  - 显示获取的数据，77–78
  - 打开`XMLHttpRequest`对象，70–73
  - 概述，16–17, 60–62
  - 服务器端编程，79–82
  - 测试，17–18
- AJAXLib 框架，179–181
- `alert`对话框，286–287, 290
- `alert`函数，286–287, 290
- 和号（`&`），83
- 与操作符（`&&`），49–50, 333
- `and.html`文档，49–50
- 注释。参见 comments
- 匿名回调函数，97
- 匿名函数，74–75
- `appendChild`方法，427, 432–433, 435
- `appender.html`文档，433–435
- 应用程序。参见 Web 应用程序
- 参数
  - `asyncFlag`作为参数，71
  - 默认参数，350–351
  - 方法作为参数，71
  - 密码作为参数，71
  - PHP 中的参数。350–351
  - URL 作为参数，71
  - `userName`作为参数，71
- 算术运算符，43–46
- 数组索引，330, 341
- `array.html`文档，115–116

### 数组

- 描述，53
- `$errors`，408–415, 418–419
- 表单，399–403
- 处理数据，328–330
- 迭代，341
- JavaScript 数组，53–55, 111–116
- 循环遍历，387–390
- 数组元素命名，53
- PHP 数组，328–330
- `$_POST`数组，89
- `$_REQUEST`数组。参见`$_REQUEST`数组
- 作为数组发送数据，374, 386
- 发送到服务器，374, 386
- `$_SERVER`数组，396
- 在数组中存储数据，399–403
- 使用数组，53–55
- `XMLHttpRequest`对象数组，111–116
- `arrays.php`脚本，328–330
- `askGoogleSuggest`函数，127, 128–133
- 赋值运算符，44, 45
- 星号（`*`），39, 331, 332
- `asyncFlag`参数，71
- 异步 JavaScript 和 XML。参见 AJAX
- 异步操作，73
- `attentionGetter.html`文档，229–235
- 属性。另见特定属性
  - HTML 控件属性，357
  - HTML 元素属性，187
  - 名称属性，187
  - XML 元素属性，187, 218–222
- `attributes`属性，426
- `AUTH_TYPE`服务器变量，392

### B

- 背景图像，241
- `background-attachment`属性，241
- `background-color`属性，231, 241
- `background-image`属性，241
- `background-position`属性，241
- `background-repeat`属性，241
- 背景
  - 颜色，231–232, 241–245
  - 图像，241
  - 使用 CSS 设置样式，241–245
- 反斜杠（`\`），328
- `BeforeBegin`常量，269
- `BeforeEnd`常量，269
- 位运算符，43–44
- `bottom`属性，245
- 花括号`{ }`，29, 327, 332, 336
- 方括号`[ ]`，53, 71, 329, 333
- 浏览器缓存，145–146
- `browser.html`文档，56–58
- 浏览器。参见 Web 浏览器
- 内置列表，355–356
- 带项目符号的列表，100–102, 161

### 按钮

- `+ -`使用添加行，292–296
- 使用调用`getData`函数，63, 86–87, 90–94
- 使用更改背景颜色，243–244
- 点击此处，35–38
- 用户点击，29–38
- 使用`createElement`创建，283, 285–287
- HTML 按钮，29–38
- 确定按钮，29–33
- 使用定位图像，247–250
- 单选按钮，368–371
- 重置按钮，358
- 使用发送值，85–87
- 使用设置堆叠顺序，251–253
- 提交按钮，358, 361–362, 372–373

### C

- 缓存，Web 浏览器缓存，145–146

### 回调函数

- 匿名回调函数，97
- 下载颜色，160
- 下载数据，73–74
- 下载图像，457–458
- 下载文本，152–157, 167, 169
- 下载 XML，159, 172–174
- `getXml`函数，177
- Google Suggest，133–138
- `libXmlRequest`框架，177–179
- 层叠样式表。参见 CSS
- 单元格，表格单元格，291, 293–294
- 聊天会话，10–11
- `chckdata.php`脚本，407–417
- 复选框，364–368
- `checkbox.html`文档，364–365
- `checkbox.php`脚本，366–368
- `check_data`函数，408–417
- `checkdatainteger.php`脚本，418–420
- 国际象棋游戏，14
- 子元素，198, 201–206
- 子节点，211, 435–447
- `childNodes`属性，198, 201, 426
- `click.html`文档，27–28

### 颜色

- `+ -`背景颜色，231–232, 241–245
- 使用 XML 获取颜色，94–102, 159–164
- 前景色，232, 241
- 预定义颜色，245
- 使用 CSS 设置颜色，241–245



- 文本颜色，229–235
- `color`属性，231, 241
- 配色方案，170–176
- `colors.php`脚本，170–172
- `colors.xml`脚本，94–102, 159–160
- 逗号（`,`），349

## 注释
- + - JavaScript 注释，23–24
- PHP 注释，315–317

## 比较运算符
- + - JavaScript 比较运算符，44–45, 46
- PHP 比较运算符，333, 334
- 版权声明，显示，345–349
- `createElement`方法，282, 283–290, 430–431
- `createElement.html`文档，283–290
- `createRow`函数，292
- `createTextNode`方法，283

## CSS（层叠样式表），227–266
- + - 绝对定位，245–250
- 吸引对文本的注意，228–235
- 概述，228
- 真实示例，253–266
- 设置颜色，241–245
- 设置元素位置，245–250
- 设置元素堆叠顺序，250–253
- 设置背景样式，241–245
- 设置文本样式，235–241
- CSS 属性，231–232, 259
- CSS 规范，228
- 花括号`{ }`，29, 327, 332, 336

## D
- 数据
    - 显示获取的数据，77–78
    - 显示表单数组数据，399–403
    - 在 HTML 表单中显示，385–392
    - 下载。参见 下载项目
    - 从 XML 元素中提取数据，216–218
    - 从服务器获取数据，16–18
    - 在 PHP 数组中处理数据，328–330
    - 使用 PHP 运算符处理数据，331–332
    - 插入到网页中，268–272, 424–425
    - 传递给 JavaScript 函数，33–38
    - 传递给 JavaScript 方法，32
    - 传递给 PHP 函数，347–350
    - 使用`postDataDownloadText`发送数据，148, 164–170
    - 使用`postDataDownloadXml`发送数据，149, 170–176
    - 从复选框读取数据，364–368
    - 从 JavaScript 函数返回数据，38–39
    - 从 PHP 函数返回数据，351–356
    - 作为数组发送数据，374, 386
    - 通过 GET 发送数据到服务器，82–88
    - 通过 POST 发送数据到服务器，88–94
    - 使用 URL 编码发送数据，83
    - 存储在数组中，399–403
    - 存储在变量中（JavaScript），40–42
    - 存储在变量中（PHP），317–325
- `datadumper.html`文档，385–387, 391
- `datadumper.php`脚本，385, 387–392
- `data.php`脚本，79–82
- `dataresponder.php`脚本，82–94, 157
- `data.txt`文件，72
- 调试，384, 385, 387
- `default.php`脚本，350–351
- `deleteRow`方法，297–298
- 桌面应用程序，3–6
- 汤姆·里德尔的日记，7–9
- `display_welcome`函数，411–415
- `<div>`元素，31–32
- 文档元素，95, 186, 193–198
- `document`对象，21
- 文档对象模型。参见 DOM
- 文档类型定义（DTD），189–191, 222, 226
- `document.bgcolor`属性，21
- `documentElement`属性，426
- `documentElement.html`文档，193–198
- `document.fgcolor`属性，21
- `document.getElementById`方法，32
- `document.lastmodified`属性，21
- `DOCUMENT_ROOT`服务器变量，392
- 文档
    - 已关闭的文档，31
    - HTML 文档，184–185
    - 文本文档，22–23
    - 写入 Web 浏览器，298–303
    - XML 文档。参见 XML 文档
- `document.title`属性，21
- `document.write`方法，21, 22, 298–303
- 美元符号（`$`），170–171, 327

## DOM（文档对象模型）
- 向页面追加新元素，427–435
- 基本网页，425–427
- 简介，424–427
- 通过 DOM 替换元素，435–447
- 与 JavaScript 结合使用，426–427
- DOM 节点树，425, 427
- DOM 节点，425–427
- 点操作符（`.`），319
- `double.html`文档，107, 110–111
- `do...while`循环，339

## 下载项目
- 中止下载，452–453
- 使用 Ajax，73–77, 427–428
- 匿名函数与下载，74–75
- 显示错误消息，452–453, 455
- 下载状态，76
- 下载状态，75, 77
- 使用动态 HTML，12–14, 456–460
- 处理超时，448–455
- 图像，12–14, 456–460
- JavaScript 下载，122–126
- 从其他域下载，141
- 成功操作消息，453–454
- 文本。参见 下载文本
- XML 下载，94–102, 148, 157–164
- 下载文本
    - 回调函数，152–157, 167, 169
    - 显示下载的文本，78
    - `downloadText`函数，148, 149–157
    - 吸引用户注意，228–235
    - `postDataDownloadText`，148, 164–170
    - 使用 CSS 设置样式，235–241

## 索引 465
- `downloadText`函数，148，149–157
- `downloadText.html`文档，149–157
- `downloadXml`函数，148，157–164
- `downloadXml.html`文档，157–164
- 拖放操作，11–12，250
- 下拉列表，135–136
- DTD（文档类型定义），189–191，222–226
- 动态 HTML，267–303
  - 浏览器支持，6，279
  - `createElement`方法，282，283–290
  - 概述，268
  - `document.write`方法，298–303
  - 使用其下载项目，12–14，456–460
  - 动态编辑表格，290–298
  - 使用其修改 HTML，272，275–279
  - 使用其修改文本，272–279
  - 删除表格行，297–298
  - 文本范围，279–282
  - 使用方法更新页面，268–272
  - 使用属性更新页面，272–279
  - 将文档写入浏览器，298–303

## E
- `e`属性，255
- `echo`函数，139–140，309–310
- `echo.php`脚本，308
- ECMA（欧洲计算机制造商协会），19
- ECMAScript，19
- `editTable.html`文档，291–298
- Eich, Brendan，19
- 元素节点，211，427–435
- 元素。另见特定元素
  - 子元素，198，201–206
  - HTML。见 HTML 元素
  - 在数组中命名，53
  - 通过 DOM 替换，435–447
  - 网页。见网页元素
  - XML。见 XML 元素
- `else`语句，48–49
- `else.html`文档，48–49
- `elseif`关键字，332–334
- `elseif.php`脚本，332–334
- `encoding`属性，185，186
- 错误
  - 检查，407，419
  - 显示，407–411，416，417，419–420
  - 报告，224–225
  - 下载时出现，452–453
  - XML 文档，188–189
- `$errors`数组，408–415，418–419
- 欧洲计算机制造商协会。见 ECMAScript
- `eval`函数，123，133
- 事件，25–28
- 感叹号（`!`），139
- 表达式检查，420–421
- 正则表达式，211，212，420–421
- 可扩展标记语言。见 XML
- 扩展名，23，148，307

## F
- `fclose`（文件关闭）函数，140
- `feof`（文件结束）函数，139
- `fgets`（文件获取字符串）函数，139
- 文件关闭 (`fclose`) 函数，140
- 文件结束 (`feof`) 函数，139
- 文件获取字符串 (`fgets`) 函数，139
- 文件句柄，138–139
- 文件处理，138–139
- 文件打开 (`fopen`) 函数，138–139
- 查找项目。见搜索
- Firefox 浏览器。另见网络浏览器
  - 浏览器标识，56，58
  - 显示文本，397，398
  - 下载 XML，96
  - 处理空白符，208–210
  - `insertAdjacentHTML`与，272
  - `insertAdjacentText`与，272
  - `XMLHttpRequest`对象与，66–69
- `firstChild`属性，201，426
- `font-family`属性，236
- 字体，236–241
- `font-size`属性，236
- `font-style`属性，236，237
- `font-weight`属性，236，237
- `fopen`（文件打开）函数，138–139
- `for`循环，51–53，329，335
- `foreach`循环，339–341，388–390
- `foreach.php`脚本，340–341
- 前景色，232，241
- `for.html`文档，51–53
- 表单数组，399–403
- `<form>`元素，30，357–359
- 表单信函演示，9–10
- `formarrays.html`文档，399–400
- `formarrays.php`脚本，401–403
- 表单。*见* HTML 表单
- `for.php`脚本，335
- 正斜杠（`/`），331，332
- 正斜杠（`//`），23，315
- 框架。*见* Ajax 框架
- 函数。*另见* 特定函数
  - 匿名，74–75
  - 从函数内部调用，211
  - 内部函数，116–121
  - JavaScript。*见* JavaScript 函数
  - 数学函数，38–46
  - 外部函数，117–118
  - PHP。*见* PHP 函数
  - 字符串函数，323–325
- `functions.php`脚本，346–347

## G
- 游戏，14
- Garrett, Jesse James，5–6，7
- `GATEWAY_INTERFACE`服务器变量，392
- `$_GET`数组，84–85，88，363
- GET 方法
  - 使用其下载文本，148，149–157
  - 使用其下载 XML，148，157–164
  - `getData`函数与，86–87
  - 隐私性与，83
  - 向服务器发送数据，82–88
  - 向 Google Suggest 发送部分搜索词，129–130
- `getAllResponseHeaders`方法，142
- `getData`函数
  - 通过按钮调用，63，86–87，90–94
  - 下载数据，428–433
  - 下载图像，456–457
  - GET 方法与，86–87
  - POST 方法与，89–93
  - 读取数据项，64–65
  - `XMLHttpRequest`对象，70，107–111
- `getElementsByTagName`方法，160–161，216
- `getHours`方法，299
- `getNamedItem`方法，219
- `getTime`函数，146
- `getXml`函数，177
- 全局变量，42
- Google 搜索，2–5
- Google Suggest
  - 通过 PHP 脚本与其通信，130
  - 连接到，126–138
  - 概述，3，126
  - 作为桌面应用程序，3–5
  - 从中下载 JavaScript，122
  - 循环建议，134–135
- `google.html`文档，136–138
- `google.php`脚本，129–132，138–140

## H
- `<head>`元素，20
- HEAD 方法，142
- `history`对象，21
- `history.go`方法，21
- 热点，378
- 小时，确定当前小时，299–303
- HTML
  - 动态。*见* 动态 HTML
  - 在 PHP 文件中包含，307–308
  - 插入到现有元素旁边，268，269–272，424–425
  - JavaScript 与，20–23
  - 在头部修改，275–278
  - 使用动态 HTML 修改，272，275–279
  - 通过 PHP 发送到 Web 浏览器，310
- HTML 按钮，29–38
- HTML 控件 (PHP)，357–382
  - 属性，357
  - 复选框，364–368
  - 图像映射，378–382
  - 列表框，372–377
  - 单选按钮，368–371
  - 恢复默认值，358
  - 发送数据，357–358
  - 文本字段，359–363
- HTML 文档，184–185。*另见* 特定文档
- HTML DOM。*见* DOM（文档对象模型）
- HTML 元素
  - 属性，187
  - 使用`createElement`方法创建，283–290
  - 空元素，187
  - 在其旁边插入 HTML，268，269–272
  - 在其旁边插入文本，268，272
  - 预定义，184
- `.html`扩展名，23
- HTML 表单
  - 复选框，364–368
  - 显示数据，385–392
  - 图像映射，378–382
  - 列表框，372–377
  - 单选按钮，368–371
  - 设置，357–359
  - 在数组中存储数据，399–403
  - 文本字段，127–128，359–363
- HTML 头部请求，142–144
- HTML 头部，142–144，273–278
- HTML 表格，290–298，300，308
- HTTP GET 方法。*见* GET 方法
- HTTP 头部，142–144
- HTTP POST 方法。*见* POST 方法
- `HTTP_ACCEPT`服务器变量，392
- `HTTP_ACCEPT_CHARSET`服务器变量，392
- `HTTP_ACCEPT_ENCODING`服务器变量，392
- `HTTP_ACCEPT_LANGUAGE`服务器变量，392
- `HTTP_CONNECTION`服务器变量，392
- `HTTP_HOST`服务器变量，392
- `HTTP_REFERER`服务器变量，393
- `HTTP_USER_AGENT`服务器变量，393，394，396–397
- 连字符（`-`），232

## I
- IANA（互联网号码分配机构），312
- ID 属性，284
- ID 值，239，243
- `if`语句
  - 使用其进行分支，332–334
  - JavaScript，46–48
  - PHP，332–334
- `if.html`文档，46–48
- IIS（互联网信息服务器），16–18
- 图像映射，378–382
- 图像
  - 背景，241
  - 下载，12–14，456–460
  - 在网页中定位，246–247
  - 堆叠，250–253
- `images.html`文档，456–460
- 递增运算符，135
- 内部函数，116–121
- `inner.html`文档，116–121
- `innerHTML`属性，116–121，268，272，275–277
- `innerHTML.html`文档，276
- `innerText`属性，272，273–275
- `innerText.html`文档，273–275
- `<input>`标签，29–30
- `insertAdjacent.html`文档，269–272
- `insertAdjacentHTML`方法，268，269–272，424–425
- `insertAdjacentText`方法，268，272
- `insertBefore`方法，288–289，427
- `insertCell`方法，293–294
- `insertRow`方法，293，294
- 整数验证，418–420
- 互联网应用程序。*见* Web 应用程序
- 互联网号码分配机构 (IANA)，312
- Internet Explorer 浏览器。*另见* 网络浏览器
  - 浏览器缓存与，145
  - 浏览器标识，56，57
  - 显示文本，394–397，398
  - 动态 HTML 与，279
  - JavaScript 与，19



- 文本范围，279–282
- `XMLHttpRequest` 对象与，67，68
- 互联网信息服务器（`IIS`），16–18
- `interpolation.php` 脚本，326–328
- `is_array` 函数，389–391
- `isset` 函数，366–367，370–371
- `Java` 语言，19
- `JavaScript`，15–58
  - 添加注释，23–24
  - 数组，53–55，111–116
  - 浏览器支持，23
  - 为 `ajax.html` 示例创建，64–65
  - 下载，122–126
  - 从 `Google Suggest` 下载，122–126
  - 作为文本执行，122–126
  - 执行，22
  - 通过其获取数据，6
  - 函数。*见* `JavaScript` 函数
  - 入门，20–23
  - `HTML` 与，20–23
  - 递增运算符，135
  - 循环，51–56
  - 方法，21，22，32，427
  - 对象，21
  - 在线参考资料，19
  - 运算符，42–46，49–50
  - 概述，19
  - 属性，21，191，192，426
  - `RTF` 文档与，23
  - 语句，22，46–49
  - 文本字符串，56
  - 使用 `XML`，185，191–192
  - 变量，40–42
  - `Web` 浏览器类型/版本，56–58
  - 向网页写入内容，298–303
- `JavaScript` 文件，22–25
- `JavaScript` 函数，28–39
  - `adder`，126
  - `alert`，286–287，290
  - 调用，29–30
  - `eval`，123，133
  - `getTime`，146
  - 向其传递数据，33–38
  - `replace`，132–133
  - 从其返回数据，38–39
  - `setTimeout`，449
  - 使用，28–33
- `javascript.html` 文档，20–23，122–126
- `javascript.php` 脚本，122，123，125
- `.js` 扩展名，148
- `JScript`，19

## K

- `karaszewski.com`，179
- 按键，26
- 按键响应，127–129

## L

- `lastChild` 属性，201，202，204，426
- `left` 属性，245
- `letter.html` 文档，242–245
- `libXmlRequest` 框架，176–179
- `libXmlRequest.html` 文档，176–179
- `line-height` 属性，236
- 列表框，372–377
- `listbox.html` 文档，372–375
- `listbox.php` 脚本，375–377
- 列表
  - 内置，355–356
  - 项目符号，100–102，161
  - 下拉，135–136
- 实时搜索，2–5
- `LiveScript`，19
- `loadXMLDoc` 函数，179
- 局部变量，42
- `localName` 属性，426
- `location.hostname` 属性，21
- `location.html` 文档，246–250
- 逻辑运算符
  - `JavaScript`，43，49–50
  - `PHP`，334
- 循环计数器，51，335
- 循环索引，51，335
- `++loopIndex` 项，135
- `loopIndex` 值，135
- 循环
  - `for`，51–53，329，335
  - `do...while`，339
  - `foreach`，339–341，388–390
  - `Google Suggest`，134–135
  - `JavaScript`，51–56
  - 遍历数组，388–390
  - `PHP`。*见* `PHP` 循环
  - `while`。*见* `while` 循环

## M

- `map.html` 文档，378–380
- `map.php` 脚本，380–382
- 滚动字幕，275–276，277
- `<marquee>` 元素，394–398
- 数学函数，38–46

## 索引 469

- 菜单项，253–266
- 菜单系统，253–266
- 菜单
  - 显示，257–260
  - 隐藏，260–261
- `menus.html` 文档，253–266
- 消息
  - 显示，33–38, 337–338
  - 错误，409–411, 416, 417
  - 存储在变量中的文本，40–42
- `method` 属性，357
- 方法
  - 作为参数，71
  - 描述，71
  - 动态 `HTML`，268–272
  - `JavaScript`，21, 22, 32, 427
  - 使用方法更新页面，268–272
- 微软，19
- 微软 `Internet Explorer`。*参见* `Internet Explorer`
- 微软 Internet 信息服务器（`IIS`），16–18
- `MIME`（多用途互联网邮件扩展），312
- `MIME` 类型，312
- 减号（`-`），331, 332
- 鼠标点击，26
- 鼠标事件，255–257
- `Mozilla` 浏览器。*另见* 网络浏览器
  - 下载 `XML`，96
  - `XMLHttpRequest` 对象及其，67, 68, 69
- `multiplereturnfunctions.php` 脚本，353–356
- 多用途互联网邮件扩展（`MIME`），312
- 节点，201–206
  - 子节点。*参见* 子节点
  - `DOM`，425–427
  - 元素，211, 427–435
  - 文本，100, 204–206, 283, 288
  - 在 `XML` 文档中，191–192
- `nodeType` 属性，191, 426
- `nodeValue` 属性，426
- 井号（`#`），239, 315–316
- 数字
  - 在 `PHP` 中相加，351–353, 354
  - 数学函数，38–46
  - 存储在变量中，41–42, 317–319
- `onabort` 事件，26
- `onblur` 事件，26
- `onchange` 事件，26
- `onclick` 事件，26
- `ondblclick` 事件，26
- `ondragdrop` 事件，26
- `onerror` 事件，26
- `onfocus` 事件，26
- `onkeydown` 事件，26
- `onkeypress` 事件，26
- `onkeyup` 事件，26, 127–128
- `onload` 事件，26
- `onmousedown` 事件，26, 27
- `onmouseout` 事件，26
- `onmouseover` 事件，26
- `onmouseup` 事件，26
- `onreadystatechange` 属性，166, 430, 438
- `onreset` 事件，26
- `onresize` 事件，26
- `onsubmit` 事件，26
- `onunload` 事件，26
- 运算符。*另见* 特定运算符
  - 加法，43
  - 算术，43–46
  - 赋值，44, 45
  - 位运算，43–44
  - 比较。*参见* 比较运算符
  - `JavaScript`，42–46, 49–50
  - 逻辑，43, 49–50, 334
  - `PHP`，331–334

## N

- `name` 属性，426
- 命名节点映射，219
- `navigator.appName` 属性，21
- 嵌套项目，188–189
- `Netflix` 前 100 视频列表，12, 13
- `Netscape`，19
- `Netscape` 通信公司，19
- `Netscape Navigator`，19, 56, 66–69。*另见* 网络浏览器
- `nextSibling` 属性，201, 204, 209, 426
- 节点类型，191, 192
- `nodeName` 属性，196, 426

### Ajax：入门指南

- 运算符（续）
  - 特殊，45
  - 字符串，43
- `operators.php` 脚本，331–332
- `Or` 运算符（`||`），49, 50–51
- 外部函数，117–118
- `outerHTML` 属性，272
- `outerHTML.html` 文档，277–278
- `outerText` 属性，272
- 运行代码，306–308
- 向浏览器发送 `HTML`，310
- 运行服务器，79–82
- 单页应用程序，403–406
- 文本扩展及其，23
- 文本字段，362–363
- 验证整数，418–420
- 验证文本，420–421
- 验证用户输入，384, 407–417
- 变量。*参见* `PHP` 变量
- 将应用程序包装为单页，403–406
- 页面刷新，5, 228
- （`()`）圆括号，29
- 圆括号（`()`），29
- `parseInt` 函数，261
- 解析器，224–225
- `party2.html` 文档，216–222
- `partydtd.xml` 文档，222–226
- `party.html` 文档，199–207
- `party.xml` 文档，199
- 密码，作为参数，71
- `PATH_TRANSLATED` 服务器变量，393
- `PHP` 应用程序，403–406
- `PHP` 数组，328–330
- `.php` 扩展名，307
- `PHP` 函数
  - 基础，344–347
  - 内置列表，355–356
  - `count`，329
  - 创建默认参数，350–351
  - `fclose`，140
  - `feof`，139
  - `fgets`，139
  - 向函数传递数据，347–350
  - `phpinfo`，307–308
  - 从函数返回数据，351–356
- `PHP`
  - 添加注释，315–317
  - 数字相加，351–356
  - 高级技术，343–382
  - 为参数分配默认值，352
  - 基础，305–341
  - 复选框，366–368
  - `dataresponder.php` 脚本，82–94, 157
  - 在 `HTML` 表单中显示数据，385–392
  - 显示消息，337–338
  - 函数。*参见* `PHP` 函数
  - 入门，306–309
  - `HTML` 控件。*参见* `HTML` 控件（`PHP`）
  - `if` 语句，332–334
  - 图像映射，380–382
  - 安装，306
  - 列表框，375–377
  - 单选按钮，369–371
  - 要求，17
  - 返回多个项目，353–356
  - 向浏览器返回文本，309–314
  - 返回变量数据，79–82
  - 向浏览器返回 `XML`，311–314
- `PHP` 循环，335–341
  - `do...while`，339
  - `for`，329, 335
  - `foreach`，339–341, 388–390
  - `while`，53–56, 139
- `PHP` 运算符，331–334
- `PHP` 脚本。*另见* 特定脚本
  - 使用脚本访问 `URL`，138–139
  - 通过脚本与 `Google Suggest` 通信，130
  - 在脚本中包含 `HTML`，307–308
  - 通过 `GET` 将数据发送到服务器，84–85
  - 通过 `POST` 将数据发送到服务器，88–94
- `PHP` 变量
  - 插值到文本字符串中，326–328
  - 服务器变量，392–398
  - 在变量中存储数据，317–325
  - 在变量中存储数字，317–319
  - 在变量中存储文本字符串，319–325
- `PHP_AUTH_PW` 服务器变量，393
- `phpinfo` 函数，307–308

## 索引 471

- `phpinfo.php` 脚本，307–308
- 加号（`+`），42–43, 83, 331, 332
- `position` 属性，245
- `$_POST` 数组，89
- `POST` 方法
  - 使用 `POST` 下载文本，148, 164–170
  - 使用 `POST` 下载 `XML`，149, 170–176
  - `getData` 函数，89–93
  - 隐私及其，83
  - 向服务器发送数据，88–94
  - `postDataDownloadText` 函数，148, 164–170
  - `postDataDownloadText.html` 文档，164–170
  - `postDataDownloadXml` 函数，149, 170–176
  - `postDataDownloadXml.html` 文档，170–176
- 发布数据
  - 使用 `postDataDownloadText`，148, 164–170
  - 使用 `postDataDownloadXml`，149, 170–176
- 发布 `XML`，177
- `postXml` 函数，177
- 井号（`#`），239, 315–316
- `preg_match` 函数，421
- `previousSibling` 属性，201, 209, 426
- 隐私，83
- `process_data` 函数，413–416
- 属性。*另见* 特定属性
  - `CSS`，231–232
  - 动态 `HTML`，272–279
  - `JavaScript`，21, 191, 192, 426
- `push` 函数，112
- `REMOTE_ADDR` 服务器变量，393
- `REMOTE_HOST` 服务器变量，393
- `REMOTE_PORT` 服务器变量，393
- `removeChild` 方法，212
- `removeWhitespace` 函数，210–211
- `replace` 函数，132–133
- `replaceChild` 方法，435, 444–445
- `replaceNode` 方法，427
- `replacer.html` 文档，435–447
- `$_REQUEST` 数组
  - 检查其中的数据，403–404
  - 显示单选按钮数据，371
  - 循环遍历，387–390
  - 从文本字段读取数据，363
  - 引用数据，366–367
- `REQUEST_METHOD` 服务器变量，393
- `REQUEST_URI` 服务器变量，393
- 重置按钮，358
- `responder.php` 脚本，357–358
- `restaurant.html` 文档，298–303
- `return` 语句，352–353
- `returnfunctions.php` 脚本，351–353, 354
- 富文本格式（`RTF`），23, 312
- `Rico Ajax` 演示，9–10
- `Rico` 公司，9
- `Riddle, Tom`（日记），7–9
- `right` 属性，245
- 行索引，291
- 行，表格，290, 292–298
- `RTF`（富文本格式），23, 312

## Q

- `QUERY_STRING` 服务器变量，393
- 引号（`"`），23, 27, 187, 326
- 引号（`'`），27

## R

- 单选按钮，368–371
- `radiobutton.html` 文档，368–369
- `radiobutton.php` 脚本，369–371
- `readyState` 属性，75, 76, 439, 450
- 递归，211
- 正则表达式，211, 212, 420–421

## S

- `Safari` 网络浏览器，66, 67, 69。另见网络浏览器
- `<script>` 元素，20, 21, 28
- `SCRIPT_FILENAME` 服务器变量，393
- `SCRIPT_NAME` 服务器变量，393
- 脚本。*另见* 特定脚本/`HTML` 文档
  - 使用脚本访问 `URL`，138–139
  - `PHP`。*参见* `PHP` 脚本
  - 测试，17–18, 85
  - 滚动字幕，275–276, 277
- 搜索引擎，2–5
- 搜索词字段，127–128
- 搜索词，127, 129

## 索引 472 Ajax：入门指南

- 搜索
  - `Google Suggest`，129–130
  - 实时，2–5
  - `XML` 数据，216–222
  - `XML` 文档，216–222
- 分号（`;`），22, 237
- `send` 方法，445
- `$_SERVER` 数组，396
- 服务器变量，392–398
  - `SERVER_ADMIN` 服务器变量，393
  - `SERVER_NAME` 服务器变量，393
  - `SERVER_PORT` 服务器变量，393
  - `SERVER_PROTOCOL` 服务器变量，393
- 服务器
  - 访问，141
  - 支持 `Ajax` 的页面在其上，73
  - 匿名函数及其，74–75
  - 连接到，78–79, 445
  - 通过 `Ajax` 联系，141
  - 从服务器获取数据，16–18
  - 从服务器获取文本，73–77
  - `Internet` 信息服务器，16–18



- 在服务器上运行 PHP，79–82
- 向服务器发送数组，374，386
- 通过 GET 向服务器发送数据，82–88
- 通过 POST 向服务器发送数据，88–94
- 向服务器发送多个请求，104–106
- 服务器上的 URL，73

- 服务器端编程，79–82，130
- `SERVER_SIGNATURE` 服务器变量，393
- `SERVER_SOFTWARE` 服务器变量，393
- `servervariables.html` 文档，394–395
- `servervariables.php` 脚本，394，395–398
- `setTimeout` 函数，232，451
- 井号（`#`），239，315–316
- `show` 函数，122–125
- `single.html` 文档，104–105
- `singlepage.php` 脚本，403–406
- 空格，URL 及其，83
- 特殊运算符，45
- 方括号（`[` `]`），53，71，329，333
- 堆叠顺序，250–253
- `standalone` 属性，185，186
- 语句。*另见* 特定语句
  - JavaScript，22，46–49
  - PHP，332–334
- `status` 属性，75，77
- 字符串函数，323–325
- 字符串运算符，43
- `string.php` 脚本，320–322
- 字符串。参见文本字符串
- `strlen` 函数，320，321
- `strtoupper` 函数，320，322
- `strval` 函数，418–419
- 样式规则，237
- 样式表。参见 CSS（层叠样式表）
- 样式，文本，235–241
- 提交按钮，358，361–362，372–373
- `substr` 函数，320，321
- `substr_replace` 函数，320，321–322
- Sun Microsystems，19

## T

- `tableObject.cells(index)`，291
- `tableObject.deleteCell(index)`，291
- `tableObject.deleteRow(index)`，291
- `tableObject.insertCell(index)`，291
- `tableObject.insertRow(index)`，290
- `tableObject.row(index)`，291
- `tableObject.rows(index)`，290
- 表格，290–298，300，308
- 标签。参见元素
- `target` 属性，357
- `target` 属性，255
- `temperature.html` 文档，48，49
- 测试脚本，17–18，85
- 文本。*另见* 文本字段
  - 居中，236
  - 颜色，229–235
  - 为下载显示，78
  - 在浏览器中显示，394–398
  - 已下载的。参见下载文本
  - 封装在 XML 元素中，188
  - 在网页中输入，285，359–363
  - 作为 JavaScript 执行，122–126
  - 从服务器获取，73–77
  - 闪烁，232–235
  - 字体，236–241
  - 在现有元素旁插入，268，272
  - 使用动态 HTML 修改，272–279
  - 纯文本，9
  - 通过 DOM 替换，435–447
- 索引 473
- 使用文本范围替换，279–282
- 返回至浏览器（PHP），309–314
- RTF，312
- 大小，236，240–241
- 存储在变量中，40–42
- 使用 CSS 设置样式，235–241
- 下划线，236，238–239
- 在网页中更新，9–10
- 验证，420–421
- XML，9
- 文本文档，22–23
- 文本编辑器，22–23
- 文本扩展名，23
- 文本字段
  - 为其创建 HTML，127–128，359–362
  - 为其创建 PHP，362–363
  - 使用 `createElement` 创建，283，284–290
  - 向其中输入文本，285，361–362
  - 用于搜索词，127–128
  - 使用，359–363
- 文本节点，100，204–206，283，288
- 文本范围，279–282
- 文本字符串
  - 将 PHP 变量插入其中，326–328
  - JavaScript，56
  - 存储在 PHP 变量中，319–325
- `text-align` 属性，236
- `text-decoration` 属性，236，238
- `textfield.html` 文档，359–362
- `textfield.php` 脚本，362–363
- `textRanges.html` 文档，279–282
- `textStyles.html` 文档，236–241
- 时间，确定当前时间，299–303
- `timeout.html` 文档，448–455
- 超时，448–455
- 汤姆·里德尔的日记，7–9
- `top` 属性，245
- `trim` 函数，320
- `.txt` 扩展名，23

## U

- URL 编码，83，164
- URL
  - 使用 PHP 脚本访问，138–139
  - 作为参数，71
  - 浏览器缓存与，145–146
  - 在不同服务器上，73
  - 获取，72–73
  - 通过其导航到 JavaScript 文件，23
  - 空格与，83
  - 使用其测试脚本，85
- 用户输入验证，384，407–417
- `userAgent` 属性，56
- `userName`，作为参数，71
- UTF-8 字符集，185–186

## V

- `validateOnParse` 属性，224
- 验证
  - 整数，418–420
  - 文本，420–421
  - 用户输入，384，407–417
  - XML，189–191，222–226
- `validation.html` 文档，224–226
- `var` 语句，40–42
- `variable.html` 文档，40–42
- 变量。*另见* 特定变量
  - 描述，40，317
  - 全局，42
  - JavaScript，40–42
  - 局部，42
  - PHP。*见* PHP 变量
- `variables.html` 文档，317–318
- `variables.php` 脚本，318–319
- `version` 属性，185

## W

- Web 2.0，5
- Web 应用程序，59–102
  - 聊天，10–11
  - 国际象棋游戏，14
  - 拖放，11–12
  - 表格信函演示，9–10
  - Netflix 前 100 视频列表，12，13
  - 单页，403–406
  - 汤姆·里德尔的日记，7–9
  - 用作桌面应用程序，3–6
  - 封装到单个 PHP 页面中，403–406
- Web 浏览器
  - 缓存与，145–146
  - 直接创建 `XMLHttpRequest` 对象，66–70
  - 确定类型/版本，56–58
  - 显示文本，394–398
  - 动态 HTML 支持，6，279
  - Firefox。*见* Firefox 浏览器
  - 处理事件，25–28
  - Internet Explorer。*见* Internet Explorer 浏览器
  - JavaScript 与，23，56–58
  - 实时搜索，2–5
  - Mozilla，67，68，69，96
  - Netscape，19，56，66
  - 打开 `XMLHttpRequest` 对象，70–73
  - 返回文本至，309–314
  - 返回 XML 至，311–314
  - Safari，66，67，69
  - 发送 HTML 至，310
  - 文本范围与，279，281
  - 欢迎页面，403–417，420
  - 空白问题，210–216
  - 写入文档至，298–303
  - XML Schema 与，190，222
  - `XMLHttpRequest` 对象与，66–73
- Web 交互，5
- Web 交互设计师，5
- 网页元素
  - 追加到网页，427–435
  - 更改背景颜色，241–245
  - 定位，245–253
  - 替换，435–447
  - 堆叠顺序，250–253
  - 样式，237–241
- 网页
  - 基础，63–64
  - 元素。*见* 网页元素
  - 输入文本，359–363
  - 插入新数据，268–272，424–425
  - 页面上的多个 `XMLHttpRequest` 对象，104–106
  - 页面刷新，5，228
  - 定位图像，246–247
  - 设置元素位置，245–250
  - 更新文本，9–10
  - 使用动态 HTML 更新，268–279
  - 验证用户输入，384，407–417
  - 欢迎页面，403–417，420
  - 将应用程序封装为单页，403–406
  - 写入，298–303
- Web 资源，修改，145–146
- Web 服务器。*见* 服务器
- 欢迎页面，403–417，420
- `while` 循环
  - JavaScript，53–56
  - PHP，53–56，139，335–338
- `while.html` 文档，53–55
- `while.php` 脚本，336–338
- whitefrost.com，176
- 空白字符
  - 跨浏览器问题，210–216
  - 在 Firefox 中处理，208–210
  - 从 XML 中移除，179–181
- `window` 对象，21
- `window.open` 方法，21
- WordPad，22–23

## X

- x 坐标，381
- x 位置，378，381–382
- `x` 属性，255
- XML（可扩展标记语言）
  - 直接访问数据，216–222
  - 使用 AJAX 下载，94–102
  - 使用 `downloadXml` 下载，148，157–164
  - 使用 `postDataDownloadXml` 下载，149，170–176
  - 概述，184–191
  - 从其移除空白，179–181
  - 使用 PHP 返回至浏览器，311–314
  - 规则/指南，184–188
  - 与 Ajax 一起使用，94–102
  - 与 JavaScript 一起使用，185，191–192
  - 验证，189–191，222–226
- XML 声明，94，185–186，311
- XML 文档类型定义（DTD），189–191，222–226
- XML 文档，94–102
  - 直接访问数据，216–222
  - 从零开始创建，185–190
  - 声明，94，185–186
  - 文档元素，95，186，193–198
  - DTD，189–191，222–226
  - 元素。*见* XML 元素
  - `encoding` 属性，185，186
  - 错误，188–189
  - 示例，185
  - 获取颜色，94–102，159–164
  - 节点，191–192
  - 搜索，216–222
  - `standalone` 属性，185，186
  - 语法规则，189–191
  - 有效性，189–191
  - `version` 属性，185
  - 与 HTML 文档相比，184–185
  - 格式良好，188
  - XML Schema，189–191，222
- XML 元素
  - 访问，193–207
  - 属性，187，218–222
  - 文档元素，95，186，193–198
  - 空元素，187
  - 包围文本，188
  - 提取数据，216–218
  - 名称，185，186
  - 嵌套，188–189
  - 检索属性数据，218–222
- XML 解析器对象，223–224
- XML Schema，189–191，222
- `XMLHttpRequest` 对象
  - 数组，111–116
  - 配置，71–73
  - 创建，64，65，66–70
  - 为数据下载创建，428–434
  - 为单个按钮创建，107–111
  - 从 Web 浏览器创建，66–70
  - 描述，21
  - `downloadText` 函数，149–153
  - `downloadXML` 函数，158–159
  - 同一页面中的多个对象，104–106
  - 打开，70–73
  - `postDataDownloadText` 函数，164–168
  - `xml.php` 脚本，311–314

## Y

- y 坐标，381
- y 位置，378，381–382
- `y` 属性，255

## Z

- `z-index` 属性，250
- `z-order` 属性，245

---

# 必备技能——轻松掌握！

学习如何使用 Ajax（异步 JavaScript 和 XML）来创建可与桌面应用程序丰富功能相媲美的 Web 应用程序。通过简单易懂的示例，《Ajax 入门指南》将让你迅速上手使用这一前沿技术集合。创建 `XMLHttpRequest` 对象，并使用 JavaScript、XML、DHTML、CSS、PHP 等构建下一代 Web 应用程序。你还会了解到多种可立即使用的免费预编写 Ajax 框架。

# 专为轻松学习而设计

- **关键技能与概念**—章节涵盖的特定技能列表
- **专家问答**—包含补充信息和实用技巧的 Q&A 部分
- **动手实践**—展示如何应用技能的实践练习
- **注释语法**—带有注释的示例代码，描述所阐释的编程技术

可在 www.mhprofessional.com 获取即用型代码。

Steven Holzner 是超过 100 本计算机书籍的获奖作者，包括《PHP 完全参考手册》。他曾担任《PC Magazine》特约编辑，在财富 500 强公司教授编程课程，并曾在康奈尔大学和麻省理工学院任教。

![](img/2cd265cf0a64e9b4b91ab611753cd5d5_499_0.png)
