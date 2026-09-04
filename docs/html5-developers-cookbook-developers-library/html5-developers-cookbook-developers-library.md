
# HTML5 开发者秘籍（开发者图书馆）

## 引言

超文本标记语言（HTML）是创建和构建网页的核心语言。二十多年来，开发人员一直在编写 HTML，在最初的几年里，该语言经历了根本性的变化，但在 20 世纪 90 年代后期，事情放缓了一点。直到现在。

## HTML 简史

1991 年，蒂姆·伯纳斯-李爵士撰写了一篇名为“HTML 标签”的文档，其中描述了 20 个用于编写网页文档的元素。到 1993 年中期，互联网工程任务组（IETF）发布了第一个 HTML 规范的提案。该提案草案到期，直到 1995 年 11 月，第一个规范才发布：不是 HTML 1.0，而是 HTML 2.0。

HTML 3.2 于 1997 年发布，随后是 1998 年发布的 HTML 4。HTML 4 有三种变体：严格型、过渡型和框架集型。在此期间，浏览器供应商（如微软和网景）开始以略微不同的方式实现 HTML，我们经历了第一轮的浏览器战争（http://en.wikipedia.org/wiki/Browser_wars）。

## XHTML

HTML 4 发布后，万维网联盟（W3C）决定停止 HTML 的演进和发展，并着手研究可扩展超文本标记语言（XHTML）1.0，一种基于 XML 的语言，被认为是互联网的未来。XHTML 中没有新元素——事实上，该规范与 HTML 4 相同——但开发人员必须遵循新的语法规则：标签必须闭合，或自闭合，属性必须加引号。这要求更严格、更规范的编码标准，并确保开发人员将使用单一的书写风格。大约在 2001 年左右，层叠样式表（CSS）开始变得更加突出和流行，随着博客的兴起，对网络标准的认识显著提高。

从 2002 年开始，W3C 发布了 XHTML 1.1 的草案。虽然 XHTML 1 本质上是带有 XML 色彩的 HTML，但 XHTML 1.1 本质上是 XML。尽管它本应更具前瞻性，但它不向后兼容，因此如果将其用于网站开发，该网站在当前和旧版浏览器中将无法工作。

这引发了网络社区、浏览器厂商甚至 W3C 内部的担忧。并非所有人都确信 XML 是网络的未来标记语言。

## Web Forms、Web Apps 与 WHATWG

2004 年，来自苹果、Mozilla 和 Opera 的个人开始着手制定他们自己的规范，旨在创建向后兼容的代码，用于构建 Web 应用程序。W3C 拒绝了这项提议，这导致了一个自称 Web 超文本应用技术工作组（WHATWG）的团体的成立。

WHATWG 开始着手 Web Forms 2.0 和 Web Applications 1.0 的工作。规范的编辑是 Ian “Hixie” Hickson，议题和想法通过公共邮件列表提出。尽管最初的工作涉及两个规范——Web Forms 2.0 和 Web Applications 1.0，但它们现已合并为一个名为 HTML5 的规范。

## XHTML 2 对决 HTML5

因此，在 WHATWG 开发 HTML5 的同时，W3C 的 XHTML 2 规范却举步维艰。2006 年，W3C 决定其在前几年放弃 HTML 的做法是错误的，虽然仍会继续开发 XHTML 2，但将再次审视 HTML 的发展。W3C 决定使用 WHATWG 迄今为止完成的工作作为新版本 HTML 的起点。

尽管这是个好消息，但也导致了一种令人困惑的局面，因为目前有三种不同的标记语言正在开发中：W3C 的 HTML 5 和 XHTML 2；以及 WHATWG 的 HTML5（注意与 W3C 的“HTML 5”相比没有空格）。因此，HTML5/HTML 5 这个规范由两个团体同时开发。

WHATWG 的运作方式与 W3C 截然不同，其步伐要快得多。由于 WHATWG 的公共邮件列表，想法得以定期提出，Web 开发者能够质疑一些做出的决定。规范团队——过去和现在——都能够基于社区反馈快速地采纳好想法、拒绝坏想法，并更改或删除规范中的项目。HTML5 在 WHATWG 的发展速度远快于在 W3C 的速度。

这样经过几年后，在 2009 年，W3C 宣布停止 XHTML 2 的工作。HTML5“赢了”。

那么，规范现在处于什么状态？嗯，它主要仍由 WHATWG 开发，然后由 W3C 进行审查。

这个过程并不完美，但带来了令人兴奋的成果。

## 我应该参考哪个规范？

W3C（http://dev.w3.org/html5/spec/spec.html）和 WHATWG（http://whatwg.org/specs/web-apps/current-work/multipage/）各有一个版本的规范。两者都是庞大、厚重的文档。2011 年 3 月，Ben Schwarz 推出了“面向 Web 开发者的 WHATWG HTML5 规范”（http://developers.whatwg.org），我们建议使用它。如果您对日常讨论感兴趣，也可以通过邮件列表随时了解规范动态：http://lists.whatwg.org/htdig.cgi/whatwg-whatwg.org。

基础 HTML5 规范仅仅是一个基础。为了匹配技术发展的速度，已经发生了重大转变。WHATWG 和 W3C 的团队一直在不断开发新的附加规范，这些规范包含诸如网络连接信息和设备摄像头信息之类的功能。浏览器厂商正在共同努力，帮助定义这些功能并加快其在浏览器中的实现。未来几年将会非常激动人心。

## HTML5 的原则

HTML5 的创建方式支持现有内容，换句话说，是向后兼容的。对 XHTML2 规范提议的主要担忧是它将破坏大多数网站。HTML5 建立在 HTML 4 的基础上，因此浏览器可以继续支持 HTML，不仅是新的 HTML5 元素，还包括 HTML 4 中的所有内容。现在能在 HTML 4 或 XHTML 中正常工作的网站，预计在 HTML5 中也能正常工作。

使用 HTML5 意味着您可以继续使用以前的编码风格。我们将在第 1 章中更详细地介绍这一点，但 HTML5 是为开发者着想而编写的，因此您可以继续使用 HTML 语法或 XHTML 语法，浏览器会知道如何处理。

HTML5 还告诉浏览器如何处理由不正确的标记实现引起的错误。以前，浏览器会自行解释这些错误，因此每个浏览器都有自己的怪癖。HTML5 是为我们这样的开发者和浏览器厂商编写的，以便在不久的将来，我们都遵循相同的标准。

或许 HTML5 真正强大的地方在于它如何满足 Web 应用程序开发者的需求。因为浏览器如此强大，我们可以创建非常像应用程序的网站：它们可以提供照片共享、绘图、文件编辑和其他功能。以前，这些功能需要多层 JavaScript 和插件（如 Java 或 Flash）。但这意味着可访问性问题，并依赖于第三方软件的稳定性。HTML5 为我们创建 Web 应用程序提供了新标准，提供了强大的 API，用于诸如 `canvas` 绘图、拖放、离线存储和浏览器原生视频等功能。有了明确的标准，浏览器将正确且稳定地处理这些事情。网络社区将帮助发展和完善这些标准，持续推动和改进它们，而开发者则不必创建 hack 来让这些功能工作。

## HTML5 到底是什么？

HTML5 不仅仅是一项技术。它更像是一个总称，涵盖了新的和增强的 HTML 元素、CSS 样式以及 JavaScript API 和事件。这些技术的结合提供了广泛的新增功能，以增强用户体验，使网站更像原生应用程序，并与设备集成。以下只是部分新增或增强的功能：

- 改进的语义
- 表单
- Canvas 绘图
- 拖放
- 本地存储
- 页面间通信
- 桌面通知
- 视频和音频
- Web Sockets
- 地理定位
- 历史记录
- 微数据

尽管地理定位并非 HTML5 规范严格的一部分，但它是一项同时开发的很酷的新技术，因此常与 HTML5 相提并论。是的，我们在这本书中也会讨论地理定位。

并非网络开发中所有新事物都是 HTML5。CSS3 *不是* HTML5，但因为它很新且非常酷，所以常被归入与 HTML5 同一类。CSS 是一种完全不同于 HTML 的语言和技术。CSS 是表现；HTML 是结构。您可以使用 CSS3 做一些非常棒的事情，但开发者和社区应该意识到它们之间的区别。

虽然我们不想陷入 HTML5 是否是 Flash 杀手（它不是）的辩论，但 HTML5 的底线是，现在浏览器内置了难以置信的丰富功能，而且这一切都是标准化的。

## HTML5 有标志吗？

是的，HTML5 当然有标志。过去几年，网络开发者和网站所有者会在他们的网站上放置图标，表明他们遵守各种 W3C 准则，例如 (X)HTML、CSS 或无障碍性。这一趋势最近有所降温，但在 2011 年初，W3C 发布了一系列标志，这最初在网络社区引起了相当大的轰动，因为它将许多网络技术（包括 CSS3）归入了 HTML5 的范畴之下。如前所述，CSS3 并不是 HTML5，但 W3C 似乎默认了这种说法，网络社区提出了他们的担忧。

值得庆幸的是，W3C 改变了其标志的目标和定义，因此主标志（图 1.1）“代表 HTML5，现代网络应用的基石”，而较小的标志（图 1.2）“代表现代网络应用和网站的方面——样式、语义、图形等等”。

因此，这些标志是为那些想要表示对核心网络标准的支持的开发者准备的。使用这些图标或标志不是必须的，但如果您愿意使用它们来展示对各种功能的采用，它们是可用的。标志可从 http://w3.org/html/logo 获取，并且有一个标志构建器，您可以从中选择不同的图标和样式。

## 食谱风格

本书旨在成为一本通过示例进行展示的文本，遵循食谱风格，提供主题解释以及支持该主题的具体方法（食谱）。在大多数情况下，这些食谱尝试展示技术如何应用于真实的编码问题，而不是展示一个没有实际目的的例子。就像厨房里使用的食谱一样，我们希望您会发现这些食谱是您自己编程解决方案的宝贵起点。

![](img/de30ea99ecac39b49e690a84c48f43b9_23_0.png)

![](img/de30ea99ecac39b49e690a84c48f43b9_23_1.png)

## 引言

总的来说，本书的结构是从较简单的主题开始，在前期主题的基础上逐步深入到更复杂的主题。我们在早期章节中介绍了 HTML5 元素和 CSS3 的新增内容，后期章节则过渡到各种 JavaScript API 和事件。我们知道，对于其中任何一个主题，都可以写一整本书来探讨其所有复杂性。尤其是在 CSS3 这类主题上，市面上已有很多优秀的书籍可供参考。

对于章节中涉及的每个主题，我们都包含了一个表格，展示了该功能在主流浏览器中的支持情况。我们还提供了一个或多个示例，演示如何应用该技术。在大多数情况下，示例包含一系列说明、代码清单以及对该示例的详细讲解。每个示例也已发布在本书网站上：www.HTML5DevelopersCookbook.com。

> **注意：** 构成 HTML5 的各个组件，如 JavaScript API，仍在通过规范进行定义，并被整合到各种浏览器平台中。我们专注于那些规范明确且得到一个或多个主流浏览器支持的元素。但需要理解的是，HTML5 正通过新的功能和特性不断发展。在第 15 章中，我们将介绍一些围绕设备集成的即将推出的功能和特性。

示例分为三个类别：初级、中级和高级。这些分类旨在让你对所涵盖主题的难度有所了解，同时尝试让你了解完成该示例可能需要投入的精力和时间。这些是粗略的分类，我们深知所需的时间和精力因读者而异。

## 第三方库

如果你参与过一段时间的 Web 开发，那么你首先会注意到本书中的一个特点是，很少有示例利用 jQuery 等众多可用的 JavaScript 第三方库。只有少数几个例外情况，我们特别介绍了第三方库的支持或集成，以解决这些库可能克服的障碍。但总的来说，我们试图专注于核心 HTML5 技术，因为每位读者都有自己偏爱的库，而每个库对 HTML5 特性的支持和集成方式也各不相同。

我们坚信库在日常网站和应用的设计与开发中扮演着重要角色。我们自己也有偏爱的库。在许多情况下，已经集成了许多 HTML5 特性的库，其集成方式与规范定义的方式相似。因此，了解如何在原生 JavaScript 中使用该组件，将使你更容易在所选的库中利用它。

本书网站 www.HTML5DevelopersCookbook.com 正是为此目的而设立，它不仅提供示例的电子版本以及可供执行和下载的支持文件，还提供额外的资源。

## HTML5 何时可以投入使用？

开发者普遍担心不能或现在不应该开始使用 HTML5，但事实并非如此。

### 我必须等到 2022 年吗？

不，你不必等到 2022 年！在 2008 年的一次采访中，HTML5 编辑 Ian Hickson 给出了一个时间表，称 HTML5 要到 2022 年才会准备就绪。这在媒体和网络社区中被过分夸大了。我们认为 Hickson 的本意是最终的建议性推荐要到 2022 年左右才会发布，但这并不意味着你不能使用所有已经定义并纳入的功能。你可能从 HTML 历史的讨论中了解到，规范需要付出难以置信的努力和时间，并且在完成之前需要经过许多阶段。

一个常见的论点涉及 CSS 2.1 的状态。CSS 2.1 已经开发了 10 多年，直到 2011 年夏天才最终定稿。但在它开发的那些年里，我们不都还在使用 CSS 吗？我们现在到了 CSS3，谁知道它什么时候才算“准备好”。这是网络社区推动技术发展超越规范的一个典型例子。

### 那么，我现在可以使用 HTML5 吗？

是的，你现在就可以使用 HTML5！不存在一个必须停止使用 HTML4 而开始使用 HTML5 的时刻。谁知道 W3C 何时会宣布 HTML5 正式就绪；到那时我们可能都在使用 HTML6 的特性了。但浏览器制造商正在全心全意地拥抱 HTML5 特性，并不断整合新功能。

由于规范和补充规范中包含如此多不同的部分和技术，你可以选择性地整合 HTML5 中你想要的部分；这不是全有或全无的情况。并非所有浏览器都能 100% 完美运行，但在第 3 章《HTML5 中的浏览器处理》中，我们解释了一些浏览器处理方法。最新版本的 Firefox、Safari、Opera、Chrome 和 Internet Explorer 都广泛支持（尽管支持的 HTML5 特性集略有不同）HTML5 特性。然而，日复一日，甚至在本书撰写过程中，我们已经看到浏览器有了显著的改进，并且随着浏览器之间的竞争，这种情况只会持续下去。所以，找一个文本或 HTML 编辑器，准备几个浏览器，开始接触 HTML5 吧。

## 致谢

### Chuck Hudson 的致谢

每当承担像本书这样具有挑战性的项目时，都会有多人参与确保项目的成功。我很幸运能与我的合著者 Tom Leadbolt 共同着手本书的编写，他是一位极具才华的设计师和开发者。谢谢你，Tom，感谢你分享你的知识，测试我的想法，并成为我许多疯狂想法的绝佳共鸣板。

感谢我的家人：妈妈，谢谢你的支持；爸爸，谢谢你开创了创业之路；还有我的祖父母，谢谢你们的爱。给我亲爱的小女儿 Sierra，你总能用你无尽的“为什么”问题让我脸上露出笑容。永远不要停止好奇。特别要感谢 Michele，感谢你对我痴迷前沿技术和无尽“项目”的无尽支持。你在我为一行代码而痛苦挣扎多次时的理解，对我意义重大。

Tom S.，谢谢这些年来的许多欢笑。我期待着看到我们前方有什么冒险。

最后，感谢所有的朋友和家人，让我有时间完成这个项目；你们都教会了我，只要有激情和毅力，一切皆有可能。

### Tom Leadbolt 的致谢

首先，我要感谢我的合著者 Chuck Hudson，他在整个写作过程中帮助了我，并在最需要的时候提供了宝贵的反馈，更不用说他还编写了一些精彩的代码片段！

感谢 HTML5 Doctors 团队——Rich Clark、Bruce Lawson、Remy Sharp、Jack Osborne、Mike Robinson、Oli Studholme、Brandan Lennox——感谢他们在 HTML5Doctor.com 网站上付出的时间、技能和奉献精神，该网站始终为网络社区提供美妙的知识和讨论。

最后，感谢我的妻子 Lucy：非常感谢你在我挣扎时的支持，感谢在我许多个夜晚和周末消失不见时的耐心。我已尽最大努力完成本书，你一路都在帮助我。

### 共同致谢

感谢 Trina MacDonald 和 Pearson 对我们的信任，并在我们不断改进书稿的过程中持续的耐心。感谢各位编辑。

## 致谢

感谢 Michael Thurston、Evan Burchard、Tim Wright、Siddharth Ram 和 Kim Wimpsett 提供的建议、详细而深刻的反馈，以及发现我们可能永远不会注意到的许多问题。许多次，你们帮助我们透过树木看到了森林，最终成果因此变得更好。感谢你们付出的所有时间和精力。我们知道这需要牺牲，也带来了很好的挑战。

最后，我们要感谢整个 HTML5 社区分享你们的知识，也感谢读者你们，在这个真正令人兴奋的时代成为开拓者。我们希望你们通过本书能像我们创作时一样，享受这些技术带来的乐趣。

## 关于作者

**Chuck Hudson** 自 20 世纪 90 年代以来一直从事网络和移动领域的开发。作为一位成功的企业家，他热衷于利用技术解决商业问题，这促使他为多家公司提供各种网络技术的咨询，并在会议上发表演讲。哈德森也是一位终身学习的技术爱好者，他还是认证的 PHP 程序员、PayPal 开发者，并在波士顿和亚特兰大地区教授网络编程、移动技术和创业课程。2008 年，他因开发首个 iOS 移动网页和原生应用而获得 eBay Star Developer 奖。

**Tom Leadbetter** 是一位来自英国利物浦的网络设计师和开发者。自 2005 年起，他一直在网络行业工作，为各种组织和客户服务，并从 2009 年初开始研究 HTML5。他在 HTML5Doctor.com 上撰写相关博客。

## 1 HTML5 中的新结构元素

**HTML5** 不仅仅是关于使用 JavaScript API 进行交互式巫术和视频酷炫。你可以使用超过 20 种新元素来构建你的网页，添加语义化以提供更易于访问、可重用的内容。

在后续章节中，你将学习新的 HTML5 表单控件和多媒体元素。在本章中，你将学习新的结构元素：`header`、`hgroup`、`nav`、`footer`、`article`、`section` 和 `aside`，重点关注如何、为什么以及何时使用这些新元素，无论是单独使用还是组合使用。本质上，你将使用这些新元素构建一个基本的网站模板，如图 1.1 所示。

![](img/de30ea99ecac39b49e690a84c48f43b9_31_0.png)



# 初学者食谱：构建一个 HTML5 启动文档

你即将开始使用 HTML5，所以让我们从 HTML 文档的顶部开始。虽然本节中的内容不包含新元素，但有一种新的编写方式，因此最好在深入主体之前了解它。

## doctype

这看起来熟悉吗？

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
```

doctype 应该是 HTML 文档的第一行。它被称为文档类型定义（DTD），是网络标准的要求，它告诉浏览器如何处理文档，这就是为什么它必须是 HTML 文档中的第一个元素。如果你不使用 doctype，或者在 doctype 之前放置了任何其他代码，那么浏览器将进入怪异模式，你编写的代码可能无法在某些浏览器中正常工作。

你不太可能想记住前面的 doctype。为什么要记呢？它既难看又笨重。在 HTML5 中，你现在有了一个简单易记的 doctype：

```
<!DOCTYPE html>
```

老实说，它就是这么简单。这就是你需要告诉浏览器你正在使用标准模式的全部内容。如果浏览器不支持 HTML5，页面仍然会正常工作。如果你使用`<!doctype html5>`，它也会触发怪异模式。选择这个 doctype 是为了确保它在任何浏览器中都能工作，无论语言的最新版本是什么。

> 注意
>
> 如果你参考 http://infomesh.net/html/history/early/，你可以看到最早的 HTML 文档，来自1990年11月13日。它的标记非常简单，这种简洁性让我们想起了 HTML5 的 doctype。事实上，如果你将新的 doctype 添加到那个页面，它将通过验证！

### 字符编码

你需要在 head 中的第一行是 charset 声明，它告诉浏览器应如何解释该文件；在这种情况下，你希望它接收一个 HTML 文档。

在 HTML 4 中，它看起来像这样：

```
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
```

但像`doctype`一样，在 HTML5 中它现在简单多了：

```
<meta charset="utf-8" />
```

很简单！记住，你的页面需要这个和`doctype`。

### JavaScript 和 CSS 链接

我们也可以快速浏览这个小节。HTML5 帮助你减少页面中的大量标记，你可以简化对 JavaScript（和其他客户端脚本文件）和 CSS 的调用。在 HTML4 中，script 和 link 元素需要一个`type`属性，如下所示：

```
<script type="text/javascript" src="my-javascript-file.js"></script>
<link rel="stylesheet" type="text/css" href="my-css-file.css" />
```

但在 HTML5 中，这些行现在看起来像这样：

```
<script src="my-javascript-file.js"></script>
<link rel="stylesheet" href="my-css-file.css" />
```

你可能想知道为什么你现在可以这样做。嗯，HTML5 的目标之一是让你在编码时更加合理。所以，如果你链接到一个脚本，浏览器会假设它是一个 JavaScript 文件，如果你使用`rel=stylesheet`，它只能意味着你链接到一个 CSS 文件。别担心，不使用`type`属性在旧浏览器中不会引起任何问题。

### 语法编写风格

在 HTML5 中，使用前面的代码示例，你可以用略有不同的方式编写页面代码。

你可以用大写字母编写：

```
<SCRIPT SRC="MY-JAVASCRIPT-FILE"></SCRIPT>
```

你可以不使用引号编写：

```
<script src=my-javascript-file></script>
```

你可以省略结束斜杠：

```
<link rel="stylesheet" type=text/css href=my-css-file.css >
```

或者你可以使用组合！

```
<LINk rel="stylesheet" tYPE="text/css" href=my-css-file.css />
```

所有这些都可以使用；但是，强烈建议你选择一种风格并坚持使用。这不仅对你自己有用，对其他可能在某些时候必须使用你的代码的开发者也有用。语法风格将保持一致。我们来自 XHTML 背景，所以我们将关闭所有标签，使用小写字母，并在属性周围使用引号。

将所有前面的内容组合在一起，给你 HTML5 的起始页面，如清单 1.1 所示。

**清单 1.1 一个简单的 HTML5 起始页面**

```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<title>page title</title>
<script src="my-javascript-file.js"></script>
<link rel="stylesheet" href="my-css-file.css" />
</head>
<body>
<!-- new HTML5 elements are going to go here :) -->
</body>
```

就是这样！将页面保存为 .htm（或 .html）文件，现在你可以开始用精彩的内容填充页面了。

**提示**

验证是检查为什么东西可能出故障的一个非常有用的工具，它是你开发过程中一个很好的步骤。然而，随着 HTML5 仍在发展中，目前还没有官方的验证器服务。W3C 验证器 http://validator.w3.org 会检查 HTML5 的一致性，但会警告这是一个实验性功能。另一个可以用来测试你页面的验证器是 http://html5.validator.nu。值得在这两个验证器中测试你的页面。

### 所有新元素从哪里来？

新的结构元素旨在告诉浏览器页面的结构，并赋予内容语义意义，但它们的名字从何而来？

2005年，Google 分析了超过 10 亿个网页，以找出开发者和网页作者正在使用哪些类名（http://code.google.com/web-stats）。这使得 HTML5 规范的主要编辑 Ian Hickson（“Hixie”）开始思考这些新元素。尽管这已经是五年前的事情了，在互联网时代算是相当久远了，但它识别出了网站上哪些内容是重要且被重用的。

以下是当时最流行的 20 个类名：

| | | |
|---|---|---|
| footer | menu | Title |
| Small | Text | Content |
| Header | Nav | Copyright |
| Button | Main | Search |
| Msonormal | Date | Smalltext |
| Body | Style1 | Top |
| White | link | |

尽管其中一些元素是表现性的（例如，`white`、`style1`、`msnormal`），但其他元素构成了 HTML5 规范中包含的元素（`footer`、`nav`、`header`）。

那么，为什么要使用这些新元素呢？嗯，HTML5 允许你赋予你的内容以语义意义，所以，例如，如果你的页面上有导航，你可以使用`nav`元素，因为该元素为其内容提供了意义。

# 初学者指南：使用 header 元素创建网站页眉

让我们从一个“典型”网页的顶部开始。

`header`元素通常是网页上的第一个东西，它通常包含诸如标志、网站名称或主要站点导航之类的内容。它可以在页面上使用不止一次，并且如将会讨论的，它可以用于特定部分的导航，而不仅仅是整个页面。诸如搜索表单或目录之类的内容可以包含在`header`元素中。以下是一个基本示例：

```html
<header>
    <img alt="HTML5 Cookbook logo" src="logo.png" />
    <h1><a href="#">HTML5 Cookbook</a></h1>
</header>
```

正如 HTML5 规范所说，`header`元素可以包含导航辅助工具，因此图 1.2 中的元素可以用一个包含标志、主要导航链接和搜索表单的`header`来标记。但根据网站的设计，这可能意味着你必须将`nav`标记在`header`之外，这是可以的。

以下是`header`元素的可能内容，其中几个在图 1.2 中显示：

- 标志
- 网站名称/标题
- 网站副标题
- 搜索表单
- 主导航

![](img/de30ea99ecac39b49e690a84c48f43b9_35_0.png)

你并不限于每个页面只有一个`header`元素，并且它也不必在页面顶部。正如我们稍后将详细解释的，如果你的页面上有多个标题，你可能会考虑将它们放在一个`header`元素中。你也可以在一个页面上使用多个`h1`标签，所以你可能会有类似清单 1.2 的内容（你将在本章稍后学习`article`元素）。

### 清单 1.2：在一页上使用多个页眉

```html
<article>
  <header>
    <h1><a href="#">Chapter 1</a></h1>
    <p>11.11.2011</p>
  </header>
  <p> Pellentesque habitant morbi tristique senectus et netus et malesuada fames
ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget,
tempor sit amet, ante...</p>
</article>
<article>
  <header>
    <h1><a href="#">Chapter 2</a></h1>
    <p>11.12.2011</p>
  </header>
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames
ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget,
tempor sit amet, ante.</p>
</article>
<article>
  <header>
    <h1><a href="#">Chapter 3</a></h1>
    <p>11.13.2011</p>
  </header>
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac
turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget,
tempor sit amet, ante.</p>
</article>
```

清单 1.2 中的代码将产生图 1.3 所示的显示。你也可以在`header`元素中放入作者和日期。然而，HTML5 规范建议作者信息更适合放在`footer`元素中。

如果你的`header`元素中只有一个标题（`h1`-`6`），那么就没有必要使用`header`；单独的`h1`-`6`就足够了。

# 第 1 章

11.11.2011

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo. Quisque sit amet est et sapien ullamcorper pharetra. Vestibulum erat wisi, condimentum sed, commodo vitae, ornare sit amet, wisi. Aenean fermentum, elit eget tincidunt condimentum, eros ipsum rutrum orci, sagittis tempus lacus enim ac dui. Donec non enim in turpis pulvinar facilisis. Ut felis. Praesent dapibus, neque id cursus faucibus, tortor neque egestas augue, eu vulputate magna eros eu erat. Aliquam erat volutpat. Nam dui mi, tincidunt quis, accumsan porttitor, facilisis luctus, metus

# 第 2 章

11.12.2011

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante.

# 第 3 章

11.13.2011

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante.

![](img/de30ea99ecac39b49e690a84c48f43b9_37_0.png)

## 初学者指南：使用 hgroup 元素组合标题

使用另一个新的 HTML5 元素`hgroup`，你可以为`header`元素添加更多信息。

此元素用于组合多个相关的`h1`-`6`标题。因此，如果你的网站有副标题，你可以使用清单 1.3 中所示的元素，它会生成图 1.4 中的布局。虽然这是一个有用的分组选项，但`hgroup`主要旨在告诉文档大纲（我们稍后将讨论）哪个标题是最重要的。在清单 1.3 中，文档大纲将排除除最高级标题（在本例中为`h1`）之外的所有标题。

### 清单 1.3：排除除 h1 之外的所有标题

```html
<header>
    <hgroup>
        <h1><a href="#">HTML5 Cookbook</a></h1>
        <h2>Delicious HTML5 recipes</h2>
    </hgroup>
</header>
```

8 第 1 章 HTML5 中的新结构元素

![](img/de30ea99ecac39b49e690a84c48f43b9_38_0.png)

图 1.4 带有主标志和副标题的网站。这些会包含在一个`hgroup`元素内。

在清单 1.3 中，`h2`与`h1`的内容相关，因此在这种情况下你可以使用`hgroup`。如果你只有一个`h1`-`6`标题，则不需要使用`hgroup`。

## 初学者指南：使用 nav 元素创建导航

`nav`元素，顾名思义，用于导航内容。它用于链接到网站内的其他页面或页面的其他部分（例如目录）。

`nav`最常见的用途是用于网站的主导航。通常的做法是使用无序列表来编写导航，如清单 1.4 所示。

### 清单 1.4：传统的导航标记方式

```html
<ul id="nav">
  <li><a href="#">Home</a></li>
  <li><a href="#">About</a></li>
  <li><a href="#">Meet the team</a></li>
  <li><a href="#">News</a></li>
  <li><a href="#">Contact</a></li>
</ul>
```

在 HTML5 中创建`nav`元素时，此代码变化不大。图 1.5 的代码将类似于清单 1.5 所示的内容。

### 清单 1.5：HTML5 中的导航标记

```html
<nav>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Meet the team</a></li>
    <li><a href="#">News</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

www.it-ebooks.info

图 1.5 会包含在`nav`元素内的全站导航

你也可以将`nav`放在`header`中，如清单 1.6 所示，因为`header`允许包含介绍性和导航性内容。然而，它不一定必须在`header`中，有时它的位置可能取决于样式问题。在页面的页脚中看到导航菜单也很常见，有时会复制主导航。

### 清单 1.6：header 元素内的 nav 元素



```html
<header>
  <h1>My super HTML5 site</h1>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">News</a></li>
      <li><a href="#">Contact us</a></li>
    </ul>
  </nav>
</header>
```

没有必要将页面上的所有链接都放在一个`nav`元素中。HTML5规范警告说，只有“主要导航”块才被认为适合`nav`元素。

在新闻或博客网站上，通常会看到一个包含指向文章和其他页面链接的侧边栏。清单1.7中的标记用于生成图1.6中所示的元素。

### 清单1.7：单个nav元素中的多个导航组

```html
<nav>
  <h2>Shared</h2>
  <ul>
    <li><a href="#">Pellentesque habitant</a></li>
    <li><a href="#">Morbi tristique senectus</a></li>
  </ul>
</nav>
```

## 第1章 HTML5中的新结构元素

```html
<li><a href="#">Aenean ultricies mi vitae est</a></li>
</ul>
<h2>Read</h2>
<ul>
  <li><a href="#">Pellentesque habitant</a></li>
  <li><a href="#">Morbi tristique senectus</a></li>
  <li><a href="#">Aenean ultricies mi vitae est</a></li>
</ul>
<h2>Watched/Listened</h2>
<ul>
  <li><a href="#">Pellentesque habitant</a></li>
  <li><a href="#">Morbi tristique senectus</a></li>
  <li><a href="#">Aenean ultricies mi vitae est</a></li>
</ul>
</nav>
```

请注意，导航栏中使用了一个`h2`来分隔链接组。在图1.6中，这些`h2`标签可以作为选项卡标题，因此当用户选择一个标题时，内容会切换（此效果可以通过JavaScript实现）。标题元素并非总是必需的，但在可能的情况下，应使用它来分隔和组织导航组。出于样式原因，您可能需要将前面的示例分成两个`nav`结构，这也是可以的。

使用`nav`元素可以带来巨大的无障碍访问收益。辅助技术，如屏幕阅读器，将能够搜索并立即使用导航组，而不是等待它们出现在屏幕上。传统上，开发者在HTML文档中使用“跳过”或“跳转”链接作为第一个元素，这些链接通常指向主导航或主要内容。然而，使用`nav`元素意味着您很快就能摆脱此类“跳过”菜单。唯一的问题是目前辅助技术对HTML5元素的支持有限。然而，它们很快就会跟上。

![](img/de30ea99ecac39b49e690a84c48f43b9_40_0.png)

## 中级技巧：使用新的article元素

`article`元素和`section`元素（将在下一节讨论）可以说是两个最重要的HTML5新结构元素，但它们也是最容易让人困惑的两个。

`article`元素是一个独立的内容块；它可以独立存在并且可以重复使用。想想你在RSS订阅源中看到的内容；这些内容几乎都是单独的文章。你可以将它们从订阅源中取出，它们本身就有意义。

HTML5规范建议了一些如何使用`article`元素的例子，例如论坛帖子、杂志或报纸文章、博客条目或用户提交的评论。

清单1.8使用`article`元素标记一个新闻项目，如图1.7所示。

```html
<article>
  <header>
    <h1>HTML5拯救数百万人！</h1>
    <p>2010年10月32日</p>
  </header>
  <p><strong>Pellentesque habitant morbi tristique</strong> senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget...</p>
  <h2>另一个标题</h2>
  <ol>
    <li>Lorem ipsum dolor sit amet, consectetuer adipiscing elit.</li>
    <li>Aliquam tincidunt mauris eu risus.</li>
  </ol>
  <blockquote><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus magna. Cras in mi at felis aliquet congue. Ut a est eget ligula molestie gravida. ...</p></blockquote>
  <h3>以及另一个标题</h3>
  <ul>
    <li>Lorem ipsum dolor sit amet, consectetuer adipiscing elit.</li>
    <li>Aliquam tincidunt mauris eu risus.</li>
  </ul>
  <p>本文发表于2010年10月32日星期日的《HTML5时报》，作者为Tom Leadbetter</p>
</article>
```

## 第1章 HTML5中的新结构元素

## HTML5拯救数百万人！

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. *Aenean ultricies mi vitae est.* Mauris placerat eleifend leo. Quisque sit amet est et sapien ullamcorper pharetra. Vestibulum erat wisi, condimentum sed, *commodo vitae*, ornare sit amet, wisi. Aenean fermentum, elit eget tincidunt condimentum, eros ipsum rutrum orci, sagittis tempus lacus enim ac dui. [Donec non enim] in turpis pulvinar facilisis. Ut felis.

## 二级标题

1. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

2. Aliquam tincidunt mauris eu risus.

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Vivamus magna. Cras in mi at felis aliquet congue. Ut a est eget ligula molestie gravida. Curabitur massa. Donec eleifend, libero at sagittis mollis, tellus est malesuada tellus, at luctus turpis elit sit amet quam. Vivamus pretium ornare est.

## 三级标题

- Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

- Aliquam tincidunt mauris eu risus.

本文发表于2010年10月32日星期日的《HTML5时报》，作者为Tom Leadbetter。

![](img/de30ea99ecac39b49e690a84c48f43b9_42_0.png)

这篇博客/新闻条目是一个`article`，因为它是一个独立的内容。它会出现在联合供稿（即RSS订阅源）中吗？会的！它本身有意义吗？有！那么它就是一个`article`。

正如你将在后面的章节中发现的，你可以在`article`中嵌套`section`，也可以在`section`中嵌套`article`。

HTML5规范指出，`article`是一个“独立的内容项”，它甚至说博客评论也可以是`article`。

## 中级技巧：使用section元素对内容进行分组

`section`元素是一个内容区域或页面区域，几乎总是需要一个标题。它可用于对一整个部分的内容进行分组，并且如果需要，可以进一步细分为更小的部分。它不是用于通用包装样式的元素。一个`section`可以包含`article`元素，而`article`元素也可以将其内容分割成多个`section`。因此，正如你在`article`元素中看到的那样，你需要思考何时使用`article`或`section`。清单1.9是一个使用`section`的示例，如图1.8所示。

## 大量新闻

### 体育新闻

我们将在此放置体育新闻。

### 娱乐新闻

娱乐新闻将放在这里。

### 极客新闻

极客的新闻将放在此页面的此部分。

图1.8 高亮显示了分区的基本新闻页面（未应用样式）

### 清单1.9 为不同类型的新闻创建带有分区的基本新闻页面

```html
<h1>大量新闻</h1>
<section>
  <h1>体育新闻</h1>
  <p>我们将在此放置体育新闻。</p>
</section>
<section>
  <h1>娱乐新闻</h1>
  <p>娱乐新闻将放在这里。</p>
</section>
<section>
  <h1>极客新闻</h1>
  <p>极客的新闻将放在此页面的此部分。</p>
</section>
```

在图1.8中，每个`section`都有自己的标题，并且每个`section`与其他`section`完全分离。如果页面上还有其他内容，你可以将它们全部包装在一个`section`中，并给它一个“我们涵盖的新闻类型”的标题：

```html
<section>
  <h1>我们涵盖的新闻类型</h1>
  <section>
    <h1>娱乐新闻</h1>
    <p>娱乐新闻将放在这里。</p>
  </section>
  ....
</section>
```

此外，你还可以将“极客新闻”部分进一步细分为更小的部分：

```html
<section>
  <h1>我们涵盖的新闻类型</h1>
  <section>
    <h1>极客新闻</h1>
    <p>极客的新闻将放在此页面的此部分。</p>
    <section>
      <h2>游戏新闻</h2>
      ...
    </section>
    <section>
      <h2>gadget新闻</h2>
      ...
    </section>
  </section>
  ....
</section>
```

www.it-ebooks.info

## 你应该使用哪个：`article`还是`section`？

`section`元素的用法类似于你现在使用的`div`标签。但与`div`不同，`section`具有语义意义；它是对相关内容的分组。

一个`section`中可以包含`article`。想象一个新闻页面；它可能有一个新闻部分，然后在该部分内，有不同的新闻类别。

你可能有一个“新闻”的标题，然后是所有不同类型的新闻，就像一份报纸。在HTML4中，你会用`div`包装它，但现在你可以用`section`包装所有这些。每种类型的新闻将放在自己的`section`中，并有自己的标题。

如果你认为内容本身就有意义，那么它就是一个`article`。HTML5流程图是一个方便的工具，可以帮助你决定使用哪个元素：http://html5doctor.com/happy-1st-birthday-us。

> **提示**

正如我们稍后讨论HTML5大纲生成器时将看到的，检查你是否使用了正确的标记非常重要。

早期采用HTML5时的一个常见错误是使用`section`来包装整个站点，例如`<section class="container">`或`<section class="wrap">`。这不是正确使用`section`的方式。

正如HTML5规范所说：

"强烈建议作者将`div`元素视为最后的手段，仅在其他元素都不合适时才使用。使用`div`元素代替更合适的元素会导致读者访问性差和作者可维护性差。"

`div`元素“完全没有特殊含义”，因此你使用它来对不属于任何新HTML5元素之一的内容进行分组。通常，当CSS无法通过其他方式针对内容进行样式设置时，需要使用`div`来设置样式。如果你使用

## 第1章 HTML5中的新结构元素

`section`元素会被添加到文档大纲中，因为它被认为对文档很重要，而`div`则不会。因此，如果只是为了样式化目的使用`section`，你应该改用`div`。

## 初学者指南：使用`aside`元素创建侧边栏

`aside`元素用于放置与周围内容“tangentially（tangentially）”相关的内容组，例如最受欢迎的文章列表、博客分类或近期评论。这类内容与页面主体内容相关，但又自成一体。

在当前的网页开发中，页面上出现“侧边栏”是很常见的。这不一定意味着它在页面的物理侧面，但它通常包含相关链接或分类列表等内容。`aside`的正确使用取决于你将其放置的位置：如果它在`article`内部，则`aside`内容应与`article`内容tangentially相关，例如一个术语表。或者，如果`aside`位于`article`或`section`外部，则其内容必须与整个页面相关，例如相关链接、网站所有者的Twitter动态或与网站相关的广告。清单1.10展示了如何创建一个“相关链接”部分，如图1.9所示。

### 关于HTML5的10件事

### 相关链接

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. *Aenean ultricies mi vitae est.* Mauris placerat eleifend leo. Quisque sit amet est et sapien ullamcorper pharetra. Vestibulum erat wisi, condimentum sed, `commodo` vitae, ornare sit amet, wisi. Aenean fermentum, elit eget tincidunt condimentum, eros ipsum rutrum orci, sagittis tempus lacus enim ac dui. [Donec non enim](http://www.it-ebooks.info) in turpis pulvinar facilisis. Ut felis.

- [关于HTML 4的10件事](http://www.it-ebooks.info)

- [关于CSS3的10件事](http://www.it-ebooks.info)

- [关于JavaScript的10件事](http://www.it-ebooks.info)

### 标题级别2

1. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

2. Aliquam tincidunt mauris eu risus.

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Vivamus magna. Cras in mi at felis aliquet congue. Ut a est eget ligula molestie gravida. Curabitur massa. Donec eleifend, libero at sagittis mollis, tellus est malesuada tellus, at luctus turpis elit sit amet quam. Vivamus pretium ornare est.

### 标题级别3

- Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

- Aliquam tincidunt mauris eu risus.

本文发表于2010年10月32日星期日的《HTML5时报》，作者为Tom Leadbetter

图1.9 带有“侧边栏”的页面基本布局

### 清单1.10 使用aside标记“相关链接”部分



## 使用 `aside` 元素

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>This has a nice outline</title>
<style>
article, aside, nav {display: block;}
article, aside {float: left;}
article {width: 500px;}
nav {width: 250px;}
</style>
</head>
<body>
<article>
<header>
<h1>10 things about HTML5</h1>
</header>
<p><strong>Pellentesque habitant morbi tristique</strong> ...</p>
...
</article>
<aside>
<h2>Related links</h2>
<nav>
<ul>
<li><a href="#">10 things about HTML4</a></li>
<li><a href="#">10 things about CSS3</a></li>
<li><a href="#">10 things about JavaScript</a></li>
</ul>
</nav>
</aside>
</body>
</html>
```

你也可以将`aside`嵌套在其他元素内，包括`article`元素。扩展前面的例子，你可以为用户提供一个术语表，涵盖主要内容中用户可能不熟悉的短语或内容：

```html
<article>
<header>
<h1>10 things about HTML5</h1>
<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>
....
</header>
<aside>
  <h2>Glossary</h2>
  <p>We have probably used lots of acronyms and abbreviations on this page, so here is the glossary</p>
  ....
</aside>
</article>
```

## 初学者指南：使用 `footer` 元素

`footer`元素，顾名思义，通常位于页面底部。然而，情况并非总是如此，尽管`footer`经常位于某个部分或页面的底部。`footer`元素用于放置其所属部分的内容信息，包括作者或网站所有者信息、版权声明以及网站条款和条件。如果它位于`article`或`section`内部，则可以包含文章的发布日期、标签、分类和其他元数据。

HTML5规范为一种非常常见的网页元素提供了解决方案：页面上的版权声明：

```html
<footer>
<small>&copy; Copyright HTML5 Cookbook 2011</small>
</footer>
```

前面的例子很可能放在`</body>`标签之前。（也请注意版权声明是放在`small`标签中的。我们将在下一章讨论这个。）

就像`header`元素一样，你可以在一个页面上多次使用`footer`。你可以将`footer`放在`article`内部。清单1.11详细展示了一个带有全站页脚的页面，以及`article`内使用嵌套`footer`元素的情况，如图1.10所示。

### 清单1.11 带有全站页脚和 `article > footer` 组合的页面

```html
<article>

  <h1>10 things about HTML5</h1>

  <footer>
    <p>This news article was published on <time>1st April 2011</time> by <a href="#">Tom Leadbetter</a></p>
  </footer>
  <p><strong>Pellentesque habitant morbi tristique</strong>...</p>
  <!-- general content -->

  <footer>
    <p>This news article was published on <time>1st April 2011</time> by <a href="#">Tom Leadbetter</a></p>
    <a href="#">Read Tom's next article</a>
  </footer>
</article>
<footer>
    <small>&copy; Copyright HTML5 Cookbook 2011</small>
</footer>
```

这个例子展示了`article`内的两个`footer`元素。在新闻文章或博客文章的顶部和底部显示作者或日期是很常见的，你可以根据需要多次使用`footer`。

在前面的例子中，我们引入了`time`元素，我们将在下一章讨论它。

你可以在`footer`中包含其他内容，例如导航（是的，使用`nav`元素）、合作伙伴标志和许可协议，你经常会看到类似“本站由<cms name>提供支持”的文本。

### 关于HTML5的10件事

本文发表于2011年4月1日，作者为Tom Leadbetter

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo. Quisque sit amet est et sapien ullamcorper pharetra. Vestibulum erat wisi, condimentum sed, `commodo` vitae, ornare sit amet, wisi. Aenean fermentum, elit eget tincidunt condimentum, eros ipsum rutrum orci, sagittis tempus lacus enim ac dui. Donec non enim in turpis pulvinar facilisis. Ut felis.

### 标题级别2

1. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

2. Aliquam tincidunt mauris eu risus.

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Vivamus magna. Cras in mi at felis aliquet congue. Ut a est eget ligula molestie gravida. Curabitur massa. Donec eleifend, libero at sagittis mollis, tellus est malesuada tellus, at luctus turpis elit sit amet quam. Vivamus pretium ornare est.

### 标题级别3

- Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

- Aliquam tincidunt mauris eu risus.

本文发表于2010年10月32日星期日的《HTML5时报》，作者为Tom Leadbetter

本文发表于2011年4月1日，作者为Tom Leadbetter

阅读Tom的下一篇文章

©版权所有HTML5 Cookbook 2011

图1.10带有多个`footer`元素的页面布局（未应用样式）

HTML5规范指出，`footer`元素可以包含指向相关文档的链接。虽然之前你可能使用`aside`和`nav`的组合来实现这一功能，但如果该内容位于`article`内部，你也可以使用`footer`元素来承载。它还可以包含其他链接，例如指向上一篇和下一篇文章的链接，其结构大致如下：

```
<article>
... 本文章的所有内容...
<footer>
<a href="#">上一篇文章</a> | <a href="#">下一篇文章</a>
</footer>
</article>
```

## 中级技巧：使用HTML5大纲工具确保正确的文档结构

借助这些新元素，你有机会使内容以逻辑的方式流动，并允许人们使用层级结构（例如使用屏幕阅读器）来浏览内容，其作用非常类似于目录。通过大纲进行测试，可以帮助你检查是否正确使用了标题和节。你可以使用各种浏览器扩展和网站，这里我们将使用一个Google Chrome扩展程序：`http://code.google.com/p/h5o/`。

下载Chrome扩展程序并安装后，你会在地址栏看到一个图标，如图1.11所示。

选择此工具时，你会看到类似目录的显示数据，内容通常会缩进显示。

如果你的内容组织得当，你应该得到一个结构清晰、逻辑合理的目录。你需要避免出现“无标题节/文章”的情况。如果显示此消息，很可能你使用了错误的标记，因此需要重新检查你的标记。但请注意，`nav`和`aside`允许有“无标题节”。

![](img/de30ea99ecac39b49e690a84c48f43b9_49_0.png)

第20页 第1章 HTML5中的新结构化元素

一个正确的大纲可能如下所示：

+ 1. 网站名称
  a. 博客
     i. 文章标题
     ii. 文章标题
  b. 关于我
     i. 我的姓名
     ii. 我的喜好
     iii. 我的厌恶
  c. 联系我

图1.12展示了一个文档大纲示例。缩进正确，除了`nav`之外没有无标题节，这是可以接受的。

你将在本技巧中创建的大纲如下：

+ 1. 海量新闻
  a. 为您带来各类新闻！
  b. 无标题导航
  c. 体育新闻
  d. 娱乐新闻！
  e. 极客新闻

![](img/de30ea99ecac39b49e690a84c48f43b9_50_0.png)

代码清单1.12展示了此页面的源代码。

### 代码清单1.12 创建基本文档大纲

```
<header>
  <hgroup>
    <h1><a href="#">海量新闻</a></h1>
    <h2>为您带来各类新闻</h2>
  </hgroup>
</header>

<nav>
  <ul>
    <li><a href="#">首页</a></li>
    <li><a href="#">关于</a></li>
    <li><a href="#">联系</a></li>
    <li><a href="#">首页</a></li>
  </ul>
</nav>
<section>
  <h1>体育新闻</h1>
</section>
<section>
  <h1>娱乐新闻</h1>
</section>
<section>
  <h1>极客新闻</h1>
</section>
```

此页面顶部有一个`header`，它在大纲中作为第一个节点（而非页面标题），随后是带有标题的节。`header`元素中使用了一个`hgroup`元素，其中包含文本“为您带来各类新闻！”，但在大纲中你看不到`h2`，因为大纲会读取元素中的第一个标题（`h1`、`h2`、`h3`、`h4`、`h5`或`h6`）。

`section`、`article`、`nav`和`aside`元素在大纲中开始了缩进（节）。这些节都有一个`h1`，并在大纲中显示。如果你想，也可以使用`h2`或`h3`；这并不重要。如果有一个节包含内容但没有标题，大纲会显示“无标题节”，而你需要避免这种情况。

## 高级技巧：使用所有新元素构建新闻页面

图1.13和代码清单1.13展示了如何使用所有新的HTML5元素来构建新闻页面的布局。它包含一些用于定位元素的基础CSS，但目前不会做任何过于花哨的事情；我们将把所有这些留到后面的章节。

### 代码清单1.13 创建新闻主页



```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>海量新闻 - 有史以来最好的新闻网站</title>
<style>
header, nav, section, article, footer {display: block;}
header, nav {border-bottom: 1px dotted #000; clear: both; width: 100%;}
nav li {display: inline;}
section#headline {clear: both; border: 5px solid #000; padding: 1%; width: 97%;}
section#sports, section#entertainment, section#nerdy {float: left; margin: 0 5px; padding: 1%; width: 30%;}aside, footer {clear: both;}
aside img {border: 1px solid #ccc; margin: 0 10px 0 0;}
</style>
</head>
<body>
<header>
  <hgroup>
    <h1>海量新闻</h1>
    <h2>为您带来各类新闻！</h2>
  </hgroup>
</header>
<nav>
  <ul>
    <li><a href="#">首页</a></li>
    <li><a href="#">体育新闻</a></li>
    <li><a href="#">娱乐新闻</a></li>
    <li><a href="#">极客新闻</a></li>
    <li><a href="#">关于</a></li>
    <li><a href="#">联系</a></li>
  </ul>
</nav>
<section id="headline">
  <h1>头条文章</h1>
  <article>
    <header>
      <h2><a href="#">这是我们最重要的文章</a></h2>
      <p>2010年11月10日</p>
    </header>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>
    </article>
  </section>
  <section id="sports">
    <h1>体育新闻</h1>
    <article> <!-- (x3) -->
      <header>
        <h2><a href="#">体育头条1</a></h2>
        <p>2010年11月10日</p>
      </header>
      <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>
    </article>
  </section>
  <section id="entertainment">
    <h1>娱乐新闻</h1>
    <article> <!-- (x3) -->
      <header>
        <h2><a href="#">娱乐头条1</a></h2>
        <p>2010年11月10日</p>
      </header>
      <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>
    </article>
  </section>
  <section id="nerdy">
    <h1>极客新闻</h1>
    <article><!-- (x3) -->
      <header>
        <h2><a href="#">极客头条1</a></h2>
        <p>2010年11月10日</p>
      </header>
      <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>
    </article>
  </section>
  <aside>
    <ul>
      <li><a href="#"><img alt="时尚广告" src="snazzy-advert.gif" height="128" width="128" /></a></li><!-- (x4) -->
    </ul>
  </aside>
  <footer>
    <ul>
      <li>本站由<a href="#">无名CMS</a>提供支持</li>
      <li>本站由<a href="#">无名主机</a>托管</li>
      <li>本站照片均归摄影师所有</li>
    </ul>  <small>&copy; 版权所有 无名氏 2011</small>
```

第24页 第1章 HTML5中的新结构化元素

## 图1.13 使用新HTML5元素构建的新闻页面布局

# 海量新闻

为您带来各类新闻！

- [首页](#)
- [体育新闻](#)
- [娱乐新闻](#)
- [极客新闻](#)
- [关于](#)
- [联系](#)

## 头条文章

[这是我们最重要的文章](#)

2010年11月10日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

### 体育新闻

### [体育头条1](#)

2010年11月10日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

### [体育头条2](#)

2010年11月9日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

### [体育头条3](#)

2010年11月8日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

### 娱乐新闻

### [娱乐头条1](#)

2010年11月10日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

### [娱乐头条2](#)

2010年11月9日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

### [娱乐头条3](#)

2010年11月8日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

### 极客新闻

### [极客头条1](#)

2010年11月10日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

### [极客头条2](#)

2010年11月9日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

### [极客头条3](#)

2010年11月8日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

| 时尚广告 | 时尚广告 | 时尚广告 | 时尚广告 |

本站由[无名CMS](#)提供支持

本站由[无名主机](#)托管

本站照片均归摄影师所有

© 版权所有 无名氏 2011

## 2 分组、文本级与重定义语义

在前一章中，你已经了解了几个新的HTML5元素。这些元素使你能够创建页面的主体结构。在本章中，你将学习更多新的HTML5元素（即`figure`、`time`、`details`和`mark`），以及一些被重新定义的元素（`address`、`s`、`cite`、`ol`、`dl`、`small`、`b`、`strong`、`i`、`em`、`abbr`和`hr`）。你还将了解新的块级链接和WAI-ARIA。这些元素被称为*分组*或*文本级*元素，用于处理页面内容。

## 初学者指南：使用 `figure` 和 `figcaption` 元素标记图形与说明文字

`figure`元素允许你包裹一个图像并为其添加描述。以前，你可能不得不使用`div`或类似元素，然后将文本添加到页面，这样做意味着图像和说明文字之间没有关联。但现在，借助`figure`，你可以使用`figcaption`将图像与说明文字关联起来。

此外，`figure`并不总是必须包含图像；它可以是代码片段、表格数据、音频或视频。不过，通常情况下，`figure`会用于图像；图2.1展示了一个示例。创建图2.1所使用的代码在代码清单2.1中给出。

### 代码清单 2.1 带说明文字的图像

```
<figure>
  <img alt="Bar chart" src="analytics.gif" />
  <figcaption>
    Website analytics for October 2010
  </figcaption>
</figure>
```

## 访客数量先升后降，再回升

2010年11月1日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo. Ut felis. Praesent dapibus, neque id cursus faucibus, tortor neque egestas augue, eu vulputate magna eros eu erat. Aliquam erat volutpat. Nam dui mi, tincidunt quis, accumsan porttitor, facilisis luctus, metus.

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo. Quisque sit amet est et sapien ullamcorper pharetra. Vestibulum erat wisi, condimentum sed, commodo vitae, ornare sit amet, wisi. Aenean fermentum, elit eget tincidunt condimentum, eros ipsum rutrum orci, sagittis tempus lacus enim ac dui. Donec non enim in turpis pulvinar facilisis. Ut felis. Praesent dapibus, neque id cursus faucibus, tortor neque egestas augue, eu vulputate magna eros eu erat. Aliquam erat volutpat. Nam dui mi, tincidunt quis, accumsan porttitor, facilisis luctus, metus.

![图2.1](img/de30ea99ecac39b49e690a84c48f43b9_62_0.png)

*Website analytics for October 2010*

图 2.1 用于显示图表和说明文字的 figure 元素

关于在`figure`元素中是否仍需要`alt`文本（为不支持图形的浏览器提供的文本替代方案），一直存在困惑。在`figure`之外，`img`总是需要`alt`。如果图像纯粹是装饰性的，并且不需要被辅助技术识别，那么可以使用空的`alt`属性。对于`figure`，如果说明文字是一个合适的描述，那么就不需要`alt`。然而，由于浏览器和辅助技术支持不足，这目前阻碍了无障碍访问。

我们建议此处采取谨慎的做法，无论如何都提供`alt`。在代码清单2.1中，说明文字非常直接，但对于使用屏幕阅读器的人来说，图表将如何呈现是未知的，因此`alt`文本提供了这一信息。

此外，即使示例使用的是图表图像，也没有理由不能使用通过Canvas或SVG创建的图表。

> **注意**
>
> 最初，规范要求使用（已有的）`legend`元素而不是新元素（`figcaption`），但由于跨浏览器样式问题，`legend`被弃用，转而支持`figcaption`。

# 2010年冬季访客数量

2011年1月1日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo. Quisque sit amet est et sapien ullamcorper pharetra. Vestibulum erat wisi, condimentum sed, commodo vitae, ornare sit amet, wisi.

> 图 2.2 用于显示共享一个图注的三张图片的 figure 元素

如图 2.2 所示，使用`figure`时并不局限于只显示一张图片；你可以使用`figure`元素来显示多张图片。图 2.2 的代码在代码清单 2.2 中。

## 代码清单 2.2 在 figure 中包含多张图片

```
<figure>
  <img alt="October 2010 data in bar chart format"
       src="analytics-october.jpg" />
  <img alt="November 2010 data in bar chart format"
       src="analytics-november.jpg" />
  <img alt="December 2010 data in bar chart format"
       src="analytics-december.jpg" />
  <figcaption>
    Comparative website analytics for Winter 2010
    (October, November, December)
  </figcaption>
</figure>
```

在显示此类内容时，是否总是应该使用`figcaption`？如果图像（或图表、表格等）纯粹是用于展示性目的，那么只需使用普通的`img`标签即可。但是，如果它包含附加信息并且对内容有益，那么很可能需要一个描述来配合它，因此在这种情况下，应使用`figure`和`figcaption`。最后，一个`figure`只能有一个`figcaption`。

## 初学者食谱：使用 time 元素标记日期和时间



## `time` 元素

`time`元素允许你编码机器可读但以用户友好方式显示的日期和时间。因此，你可以用它来为发布日期或事件添加时间戳，这些时间戳可以供其他技术使用（日历是最明显的例子）。`time`元素有两个可选属性：

- `datetime`：最终用户将看到`time`标签内的内容，但机器能够读取`datetime`的值：`datetime="2011-04-01T16:00Z"`。此值中的时间部分（`T16:00`）是可选的。你还可以添加时区偏移量：`T16:00+04:00`。`Z`代表协调世界时（UTC），相当于时区偏移量为`+00:00`。
- `pubdate`：`pubdate`是一个布尔属性。它指示其最近的父级`article`元素的发布日期和可能的发布时间。如果没有父级`article`元素，则`pubdate`指整个文档。每个`article`元素必须只有一个带有`pubdate`的`time`元素。

`time`元素旨在显示精确的日期，例如“2011年1月22日”，而不是模糊的日期，例如“2011年的某个时候”。`datetime`属性必须采用公历格式：`YYYY-MM-DD`，时间编码为`T00:00`。以下是一些示例：

```
<article>....
  <footer>
    <p>This news article was published on <time pubdate datetime="2011-04-01T16:00">1st April 2011 at 4pm</time> by <a href="#">Tom Leadbetter</a></p>
  </footer>
</article>

<article>
  <h1>Christmas day family photo</h1>
  <p>It was lovely to have the family here for <time pubdate datetime="2010-12-25">Christmas Day 2010</time></p>
  <figure>
    <img alt="" src="000001.jpg" />
    <figcaption>The Leadbetter family on Christmas morning</figcaption>
  </figure>
</article>
```

```
<p>HTML6 release date is due on <time datetime="2040-01-04">April 1<sup>st</sup></time> 2040</time></p>
```

## 初学者食谱：使用 `details` 元素制作原生切换部件

在撰写本文时，只有 Chrome 13+ 支持新的`details`元素。我们希望其他浏览器能尽快支持它。

`details`元素创建了一个交互式的开/关切换效果，无需 JavaScript 和/或 CSS。`summary`元素可在`details`内部使用，以表示内容的摘要。

`details`有一个可选属性：`open`。如果此属性为 true，它将默认显示`details`元素为打开状态；否则，`details`元素将关闭，并显示`summary`。`summary`是可点击的部分，用于打开/关闭`details`。

图 2.3 显示了一个简短的作者简介，顶部的默认是打开的。代码清单 2.3 展示了代码。

- ▼ Tom Leadbetter
  - Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
  - Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
  - Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
- ▶ Chuck Hudson

图 2.3 在 Chrome 中查看的`details`元素，其中一部分默认打开

第36页 第2章 分组、文本级别和重新定义的语义

### 代码清单 2.3 `details` 元素示例

```
<details open>
  <summary>Tom Leadbetter</summary>
  <figure>
    <img alt="" src="images/tom-and-luce.jpg" />
    <figcaption>Tom and Lucy Leadbetter</figcaption>
  </figure>
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>
</details>

<details>
  <summary>Chuck Hudson</summary>
  <figure>
    <img alt="" src="chuck.jpg" />
    <figcaption>Chuck Hudson</figcaption>
  </figure>
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>
</details>
```

另一个例子是使用`details`元素来显示/隐藏目录。根据页面的样式和内容量，将目录始终放在顶部角落可能很有用，用户可以点击展开它并导航到页面的不同部分。代码清单 2.4 包含了这段代码，其中`details`元素默认是关闭的。

### 代码清单 2.4 创建可折叠的目录

```
<article>
  <h1>A massive document with lots of juicy content</h1>
  <details>
    <summary>Table of contents</summary>
    <nav>
      <ul>
        <li><a href=#chapter1>Chapter 1</a></li>
        <li><a href=#chapter2>Chapter 2</a></li>
      </ul>
    </nav>
  </details>
  <section>
    <h1 id="chapter1">Chapter 1</h1>
  </section>
  <section>
    <h1 id="chapter2">Chapter 2</h1>
  </section>
  ....
</article>
```

## 初学者食谱：使用 `address` 元素提供联系信息

规范将`address`元素定义为一个“分段”元素，类似于`nav`或`article`。然而，我们将其放在本章中，因为我们认为它作为“文本级别”语义更合适，因为它的使用涉及文本内容，而非布局。

多年来，`address`元素一直被 Web 开发者错误使用。它不应该被用作通用的邮政地址（通常在“联系我们”页面上）。因此，以下代码是不正确的：

```
<address>
Tom Leadbetter
1 My Street
United Kingdom
</address>
```

HTML5 试图通过将`address`元素用于其最近的`article`或`body`元素的联系信息来澄清这种混淆。

那么，这意味着什么呢？它意味着你应该使用`address`元素来提供当前文章或整个网页作者的联系信息。因为你可以在`article`内部使用`address`，这意味着`address`可以在一个站点上多次使用。`address`元素的内容可以是电子邮件地址、网站、电话号码、邮政地址或任何其他类型的联系信息。

由于它是用于联系信息，在`footer`内部使用`address`很常见。代码清单 2.5 两次使用了`address`元素：一次用于主页内容的作者，另一次用于整个站点的作者。

### 代码清单 2.5 `address` 元素的多次使用

```
<article>
  <header>
    <h1><a href="#">My amazing blog entry</a></h1>
    <p>12.12.2011</p>
  </header>
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas....</p>
```

## 初学者配方：使用 `mark` 元素高亮文本

`mark`元素为文档作者提供了一种高亮或引起文档中某些文本注意的机会。

如果用户搜索网站并被带到单独的页面，他们搜索的术语可能会被高亮以供参考。这里我们会使用`mark`，而不是`strong`或`em`，因为我们不是要赋予该术语任何重要性或强调，仅仅是为了用户而高亮它。图2.4展示了如何使用它。清单2.6展示了HTML和CSS代码。

```
清单 2.6  附加了CSS的 mark 元素
<style>
mark {background-color: #0F0; font-weight:bold;}
</style>
<article> <header>
  <h1>Something in Latin</h1>
</header>
<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. <mark>Vestibulum tortor quam</mark>, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>
</article>
```

# Something in Latin

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.

图 2.4  用于为用户高亮文本的 `mark` 元素

## 初学者配方：使用 `s` 元素表示不准确或不相关的内容

以前`s`元素专门用于删除线文本。在HTML5中，它已被重新定义，现在用于表示不再正确或相关的内容。

这到底是什么意思？你可以使用`s`元素来表示产品的原始零售价，而该产品现在有了不同的价格，如图2.5所示。根据上下文，显示过时的信息可能并非总是正确。然而，在这种情况下，它对用户可能派上用场。清单2.7展示了在哪里使用该元素。

```
清单 2.7 s 元素

<h1>Tom Leadbetter's Autobiography</h1>
<p><s>Recommended retail price: £45.99</s></p>
<p><strong>Now selling for just £5.99!</strong></p>
```

在HTML 4中，`s`元素定义了删除线文本，因此浏览器默认会为`s`元素添加删除线样式。

如果文档文本已被编辑或删除，请不要使用`s`元素；应改用`del`元素。

## 对现有元素的更改

在第一章中，你了解了可用于创建页面布局和添加内容的新元素。在本章的前面部分，你看到了更多新的HTML5元素，但它们与内容本身有关，例如图像。仅仅因为关注点集中在新元素上，并不意味着现有元素被忽视了。事实上，有几个元素的角色已经改变。

### `cite` 元素

`cite`元素在HTML5中已作调整。在HTML4中，`cite`允许内容开发者标记引用中说话者/作者的姓名：

```
<cite>Julies Caesar</cite> once said, <q>I came, I saw, I conquered.</q>
```

![图 2.5 用于显示旧价格的 s 元素](img/de30ea99ecac39b49e690a84c48f43b9_69_0.png)

图 2.5 用于显示旧价格的 `s` 元素

它也用于`blockquote`内部，这在HTML4中技术上是不正确的，但尽管如此仍被普遍使用：

```
<blockquote>
<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget,
tempor sit amet, ante.</p>
<cite>A Person who spoke Latin</cite>
</blockquote>
```

然而，在HTML5中，`cite`代表作品的标题，例如一本书或一首歌曲。HTML5规范明确指出，人的名字不是作品的标题。所以，你可以使用类似以下的内容：

```
<p>One of my favourite books is <cite>The Day of the Jackal</cite> by <b>Frederick Forsyth</b></p>
```

（HTML5规范建议对作者姓名使用`b`元素。）

HTML5中不允许`cite`用于姓名这一更改引起了一些争议。Jeremy Keith 的文章 http://24ways.org/2009/incite-a-riot 值得一读；它深入探讨了这个问题。总结一下，HTML5中的`cite`元素不再向后兼容，相反，HTML5规范建议对姓名使用`b`元素，尽管这个标签本身没有语义意义，即使其内容是有意义的。

因此，你需要做出选择：是按照规范执行，还是像许多人继续做的那样，使用`cite`来表示姓名。值得关注`cite`元素，看看其定义是否会改变。

> **注意**

2011年7月，有讨论可能允许在`blockquote`中使用`footer`，这将为添加关于引用的信息（如作者）提供绝佳机会。因此，请关注这一发展。

### `ol` 元素

用于创建有序列表的`ol`元素已被重新定义，因此它现在有三个可接受的属性：

- `start`
- `reversed`
- `type`

在清单2.8中使用的`reversed`属性是HTML5新增的，当至少有一个浏览器选择实现它时，将使你能够反转一个从大到小计数的列表。

#### 清单 2.8  反向有序列表

```
<h1>My favorite colors</h1>
<ol reversed>
  <li>Red</li>
  <li>Green</li>
  <li>Blue</li>
</ol>
```

目前，没有浏览器支持此功能，但如果支持，它将呈现为：

**我最喜欢的颜色**

1. 蓝色
2. 绿色
3. 红色

`start`属性在HTML4中已被弃用，因此如果使用`start`，页面将无法通过验证。这被证明是一个麻烦，但值得庆幸的是，它现在回归了，并且在HTML5中完全可接受。因此，如果你需要从第二项开始一个有序列表，请使用以下方式：

```
<ol start="2">
  <li>here we go</li>
  ....
</ol>
```

同样从“死亡”中回归的是`type`属性。以前，如果你想更改列表类型的显示，例如罗马数字（例如 I, IV, X），你必须使用CSS。但在HTML5中，你又可以这样做了。清单2.9的标记展示了一个示例。

#### 清单 2.9  嵌套有序列表



## 有序列表

```html
<ol>
  <li>Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    <ol>
      <li>Lorem ipsum dolor sit amet, consectetuer adipiscing elit.</li>
      <li>Aliquam tincidunt mauris eu risus.</li>
      <li>Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        <ol>
          <li>Aliquam tincidunt mauris eu risus.</li>
          <li>Vestibulum auctor dapibus neque.</li>
        </ol>
      </li>
      <li>Vestibulum auctor dapibus neque.</li>
    </ol>
  </li>
  <li>Aliquam tincidunt mauris eu risus.</li>
  <li>Vestibulum auctor dapibus neque.</li>
</ol>
```

前面的代码将创建：

1. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    1. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    2. Aliquam tincidunt mauris eu risus.
    3. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        1. Aliquam tincidunt mauris eu risus.
        2. Vestibulum auctor dapibus neque.
    4. Vestibulum auctor dapibus neque.
2. Aliquam tincidunt mauris eu risus.
3. Vestibulum auctor dapibus neque.

使用`type`属性，你可以更改列表上的编号类型，而无需使用CSS。你可以选择五种类型：

```
type="1" = 1, 2, 3, 4, 5
type="a" = a, b, c, d, e
type="A" = A, B, C, D, E
type="i" = i, ii, iii, iv, v
type="I" = I, II, III, IV, V
```

如果你将`ol`类型更改为其中任何一种，那么项目符号将呈现如下：

1. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    a. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    b. Aliquam tincidunt mauris eu risus.
    c. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        i. Aliquam tincidunt mauris eu risus.
        ii. Vestibulum auctor dapibus neque.
    d. Vestibulum auctor dapibus neque.
2. Aliquam tincidunt mauris eu risus.
3. Vestibulum auctor dapibus neque.

使用不同的类型，在内容中你可以引用项目 1.b.ii，而不是 1.3.2。浏览器将正确实现`type`属性，但在撰写本文时，它会导致验证错误。

### `dl`元素

在HTML4中，`dl`是一个定义列表，它应该包含一个术语，然后是一个定义，但其自身的定义和用法从来不是很清楚，因此要么被误用，要么被舍弃而转用另一个元素。

在HTML5中，它被重新定义为描述性列表或关联列表。通过一些示例可以更好地理解这个元素。清单2.10使用`dl`创建了一个术语表。我们将术语表放在`aside`中，因为可以假设它位于一篇关于网络开发的文章内部。

#### 清单2.10 创建术语表

```html
<aside>
<h2>术语表</h2>
<dl>
<dt>HTML</dt>
<dd>HTML，即超文本标记语言，是网页的主要标记语言。</dd>
<dt>PHP</dt>
<dd>PHP：超文本预处理器是一种广泛使用的通用脚本语言，最初专为网页开发而设计，用于生成动态网页。</dd>
</dl>
</aside>
```

清单2.11使用`dl`来标记电影演职员表。

#### 清单2.11 添加电影演职员表

```html
<h1>肖申克的救赎</h1>
<dl>
<dt>导演：</dt>
<dd>弗兰克·德拉邦特</dd>
<dt>编剧：</dt>
<dd>斯蒂芬·金</dd>
<dd>弗兰克·德拉邦特</dd>
<dt>演员表</dt>
<dd>蒂姆·罗宾斯</dd>
<dd>摩根·弗里曼</dd>
<dd>鲍勃·冈顿</dd>
...
</dl>
```

上述代码为一个键（`dt`）使用了多个值（`dd`）。可以说，演职员表的每个部分（导演、编剧等）都可以放在各自的区块中，如下面所示：

```html
<article>
<header>
<h1>肖申克的救赎</h1>
<time>1994</time>
</header>
<section>
<h1>导演</h1>
<h2>弗兰克·德拉邦特</h2>
<p>（简介）</p>
</section>
<section>
<h1>编剧</h1>
<h2>斯蒂芬·金</h2>
<p>（简介）</p>
<h2>弗兰克·德拉邦特</h2>
<p>（简介）</p>
</section>
</article>
```

这实际上取决于你的内容以及你希望如何组织你的内容。

**提示**

过去，`dl`元素曾被用来标记对话，但规范现在指出使用`dl`是不恰当的。最初，在HTML5中有一个`dialog`元素，但它在2009年底被废弃了。取而代之，你应该使用`p`元素来满足此需求，如果你想设置说话者姓名的样式，应该使用`span`或`b`。下面是一个示例：

```html
<p><b>约翰</b>：你现在能使用HTML5了吗？</p>
<p><b>简</b>：是的，你当然可以！</p>
```

### `small`元素

在HTML4中，`small`元素用于减小文本大小。然而，这过去是、现在也仍是一个表现形式的问题，因此应使用CSS来实现此目的。现在，在HTML5中，`small`元素用于显示小字体文本，例如版权信息、条款和条件或许可/法律信息：

```html
<p><small>本站采用<a href="http://creativecommons.org/licenses/by-nc/2.0/uk/">知识共享署名-非商业性使用2.0</a>许可协议。欢迎修改、复用、改编和扩展。</small></p>
```

由于`small`是内联内容，如有必要，你可以将其嵌入其他元素中，例如`strong`，这将强调此小字体文本的重要性：

```html
<p><strong><small>此内容归我所有！请勿窃取，否则会有严重、严重的后果。</small></strong></p>
```

### `b`和`strong`元素

在HTML4中，`b`元素用于加粗文本，但这一点已经改变。现在它纯粹是表现形式；应用于样式化一段文本，而不传递任何特定的重要性。

你经常会看到博客文章的第一段样式不同，通常是加粗文本：

```html
<h2>简单方法揭示暗能量与平坦宇宙</h2>
<p><b class="lead">研究人员开发了一种简单的技术，为宇宙是平坦的理论增添了证据。</b></p>
<p>此外，这种方法——通过重访一个30年前的想法而开发——证实了“暗能量”占据了宇宙近四分之三的比重。</p>
```

你不会使用`strong`元素，因为你并不想给第一段增加重要性；你只是想给它设置不同的样式。然而，你也可以使用一些CSS（`p:first-of-type`或`h2+p`）来替代`b`实现样式化。清单2.12使用`b`为部分文本添加了颜色样式。

#### 清单2.12 `b`元素

```html
<style>
b.red {color: red;}
b.green {color: green;}
b.blue {color: blue;}
</style>
<h1>我最爱的颜色</h1>
<ol reversed>
  <li><b class="red">红色</b></li>
  <li><b class="green">绿色</b></li>
  <li><b class="blue">蓝色</b></li>
</ol>
```

`strong`元素表示具有强烈重要性的文本，所以你通常用它来生成加粗效果，并且你可以嵌套`strong`以增加内容的重要性：

```html
<p><strong>不要吃我的饼干</strong>并且<strong><strong>不要喝我的牛奶</strong></strong></p>
```

### `i`和`em`元素

在HTML4中，`i`元素用于样式化斜体文本。但现在，它代表以另一种语气或情感表达的文本。HTML5规范给出了一些使用示例，包括梦境、技术术语、思考或船名：

```html
<p>我今晚要吃鱼<i>（然后我想我要吃点饼干，我好久没吃饼干了）</i>。</p>
```

相比之下，`em`元素表示改变句子含义的强调。根据需要强调的单词（或多个单词），将其包裹在`em`元素中，但移动`em`元素会导致句子改变其含义：

```html
<p>我以为我晚上8点和朋友见面，但我妻子说是<em>晚上9点</em></p>
<p><em>我</em>以为我晚上8点和朋友见面，但我的<em>妻子</em>说是<em>晚上9点</em></p>
```

### `abbr`元素

`abbr`元素在HTML5中并非新元素，它也没有被重新定义。那么，为什么还要提到它呢？因为`abbr`已经与`acronym`合并了。现在，`abbr`元素代表一个缩写或首字母缩略词。你可以使用`title`属性来展开缩写，这通常意味着对用户显示工具提示：

```html
<p><abbr title="HyperText Markup Language">HTML</abbr>是自切片网页以来最棒的东西</p>
```

缩写和首字母缩略词是不同的；NATO是首字母缩略词，而BBC是缩写。在HTML4中，两个标签都可用，但由于内容作者对使用哪个感到困惑，`acronym`已被废弃，所以现在对两者都使用`abbr`。

### `hr`元素

`hr`元素过去用于在文档中创建一条水平线。它的定义已被微调，现在它表示一个段落之后的分隔，例如书中场景的转换。通常，它会被样式化为在章节之间显示一条线或一个花哨的图形。如今它不常用了，因为CSS可用于在必要章节（如`p`、`div`、`article`或`section`）的底部或顶部添加空隙/图形/线/装饰。

## 不复存在的元素

HTML5已经移除了几个元素，所以请向以下元素说再见：

- acronym（使用`abbr`；见上文）
- applet（使用`object`）
- basefont（使用CSS进行表现）
- big（使用CSS进行表现）
- center（使用CSS进行表现）
- frame（尽管`iframe`仍然存在）
- frameset
- noframes
- font（使用CSS进行表现）
- strike（根据内容，使用`s`或`del`）
- tt（使用CSS进行表现）
- u（使用CSS进行表现）

就这些了，真的。我们不会哀悼这些元素，如果你现在还在使用它们，请立即停止！

## 入门技巧：将链接包裹在元素周围

HTML5一个方便的新特性是能够将多个元素组合成一个链接。这为你提供了更大的点击区域，过去你可能需要使用JavaScript或标签组合来完成这项任务。

在HTML4中，如果你正在标记一个新闻或博客主页，其中有多篇文章需要链接，你可能之前使用了类似清单2.13中的代码，使每个项目都可点击。

#### 清单2.13 在HTML4中包裹链接

```html
<div class="article">
  <h2><a href="article.htm"><img alt="article thumbnail" src="thumb.jpg"
    height="100" width="100" /> 我的文章标题</a></h2>
  <p><a href="article.htm">Pellentesque habitant morbi tristique senectus et
    netus et malesuada fames ac turpis egestas.</a></p>
</div>
```

清单2.14表明，在HTML5中，你可以将所有这些包裹在一个`a`元素中。

#### 清单2.14 使用HTML5包裹链接

```html
<article>
  <a href="article.htm">
    <h2><img alt="article thumbnail" src="thumb.jpg" height="100" width="100" />
      我的文章标题</h2>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames
      ac turpis egestas.</p>
  </a>
</article>
```

你也可以将`article`包裹在`a`元素中；然而，已知这会导致一些浏览器问题，因此我们建议不要采用这种方法。

## 中级技巧：使用微数据添加语义信息

微数据规范允许作者为内容片段添加标签，使其可被机器读取。使用微数据格式理论上有助于“机器”（如谷歌）返回关于网页更准确的信息。

# 第2章 分组、文本级别与重定义语义

你可以将微数据视为自定义元素，因此可以用它来标记诸如商家、人物、产品或事件等事物。由于不存在`<book>`元素，你可以将微数据属性应用于现有元素。

微数据有五个属性：`itemid`、`itemprop`、`itemref`、`itemscope`和`itemtype`。清单2.15展示了一个基本示例，描述了一个人。

### 清单2.15 微数据示例

```html
<article itemscope itemtype="http://data-vocabulary.org/Person">
  <h1 itemprop="name">Tom Leadbetter</h1>
  <p><span itemprop="address" itemscope itemtype="http://data-vocabulary.org/Address">
    I live in <span itemprop="region">Liverpool</span>,
    <span itemprop="country-name">UK</span>.
  </span></p>
  <p>I am a <span itemprop="title">Space Cowboy</span> at
    <span itemprop="affiliation">Space Cowboy Inc.</span>. I also have a website:
    <a href="http://www.tomleadbetter.co.uk"
       itemprop="url">tomleadbetter.co.uk</a></p>
</article>
```

清单2.15表明，这里有一个人，他的名字叫Tom Leadbetter，居住在英国，是一名受雇于Space Cowboy Inc.的太空牛仔。

当`itemscope`用于一个元素时，该元素就成为一个微数据项。`itemprop`是这个微数据项的一个属性，它描述内容是什么。示例中有两个`itemscope`属性：一个用于整体内容（Person），另一个用于其中的地址`itemtype`。

示例中的`itemprop`值来自http://data-vocabulary.org，该网站为各种数据类型（事件、产品等）建议了名称。你可以自定义值，但为了获得一致的结果，你应该使用标准的、公认的名字。Google在http://google.com/support/webmasters/bin/answer.py?answer=99170上也提供了示例和建议。使用Google网站管理员富媒体摘要测试工具，你可以检查你的微数据，看看Google可能会如何在搜索结果页中呈现它，如图2.6所示。

图2.7展示了Google现在关于该内容掌握的其他信息。

这只是一个微数据的小例子，但它有很多有用的选项。请查看前面提到的Google页面，以获取更多可创建内容的示例。除了Google，还有一些工具可能在你创建微数据时有所帮助：http://foolip.org/microdatajs/live 和 http://microdata.freebaseapps.com。

![Google搜索预览](img/de30ea99ecac39b49e690a84c48f43b9_78_0.png)

**图2.6** Google搜索预览



```
Item
    Type: http://data-vocabulary.org/person
    name = Tom Leadbetter
    address = /Item( 1 )
    title = Space Cowboy
    affiliation = Space Cowboy Inc.
    url = http://www.tomleadbetter.co.uk/

Item 1
    Type: http://data-vocabulary.org/address
    region = Liverpool
    country-name = UK
```

**图2.7** Google掌握的其他信息

2011年6月，`http://schema.org`上线，这是由Bing、Google和Yahoo!共同协作推出的共享词汇表。`Schema.org`提供了多个示例和大量的示例数据。在清单2.15中，我们链接到`http://data-vocabulary.org`，因为这目前在富媒体摘要测试工具中受支持，但不久后你就可以在微数据中使用`http://schema.org`，它很可能会成为开发者学习应使用何种标记的目标网站。

> **注意**
>
> 微格式（Microformats）和RDFa是扩展HTML以描述特定信息的另外两种方式。这些选项存在一些我们不会深入讨论的政治因素，但两者都有其优缺点。实际上，你可以将微数据与微格式结合使用，尽管微数据是新兴标准，但微格式目前更为流行。

## 中级技巧：在HTML5中使用WAI-ARIA

Web无障碍倡议-可访问富互联网应用（WAI-ARIA），也常被称为ARIA，是一项草案规范（`http://w3.org/TR/wai-aria`），旨在提高Web应用和网页的无障碍性。ARIA使开发者和内容作者能够开发丰富的互联网应用和内容，这些内容可以被辅助技术识别和使用。通常情况下，辅助技术不知道小部件是什么，并且很少有小部件可以通过键盘访问。还要考虑到当内容通过Ajax调用更新时，辅助技术不知道内容已更新，因此无法通知用户。虽然我们不会讨论ARIA提供的所有可能解决方案，但我们将涵盖ARIA的**地标角色（Landmark Roles）**部分，以及如何将这些新角色添加到你的HTML5文档中。

地标角色是页面中用作导航地标的区域。规范（`http://w3.org/TR/wai-aria/roles#landmark_roles`）中列出了超过50个角色，但这里列出的是更常用的地标角色：

- `role="article"`
- `role="banner"`
- `role="complementary"`
- `role="contentinfo"`
- `role="form"`
- `role="heading"`
- `role="main"`
- `role="navigation"`
- `role="search"`

你可以像这样轻松地将它们添加到你的标记中：

```html
<form role="search">
  ....
</form>
```

这表示这个特定的表单（页面上可能有多个表单）是用于搜索的。

查看前面的列表，你可以看到一些角色与新的HTML5元素有明显的对应关系，当你将它们添加到上一章的主要页面结构中时，你会得到一个类似于图2.8的布局。

因为你使用了这种逻辑结构加上ARIA角色，终有一天辅助技术将能够轻松导航到页面内容的特定区域。然而，目前，屏幕阅读器不仅对HTML5的支持有限，对ARIA元素的支持也有限。

鼓励你在文档顶部使用跳转链接（skip links），这些链接通常用CSS隐藏，允许使用屏幕阅读器、键盘或其他辅助技术导航的人快速“跳过”或“跳转”到重要区域，通常是主导航或主要内容。代码类似于：

```html
<ul>
    <li><a href="#menu">Skip to navigation</a></li>
    <li><a href="#content">Skip to content</a></li>
</ul>
```

但是有了ARIA，地标将会高亮显示给用户，这样他们就可以循环浏览选项。

HTML5验证接受ARIA角色，你也可以在HTML 4中使用ARIA角色。它们会导致验证错误。

这些角色还为你提供了一个巧妙的CSS挂钩，扩展了你的选择器工具库。你可能在一个页面上有多个页眉或页脚，但你想为页面的主要页眉和页脚设置不同的样式，你可以在CSS中像这样定位它们：

```css
/* to style all headers */
header {background: red; border: 5px dotted black;}

/* to style our main header, which likely has the site logo */
header[role=banner] {background: black; border: 5px solid red;}

/* to style all footers */
footer {background: blue; border: 5px dotted green;}

/* to style our site footer, which likely has copyright info */
footer[role=contentinfo] {background: green; border: 5px solid blue;}
```

你不一定非要以这种方式使用CSS，但这确实是一个不错的选择。

关于WAI-ARIA规范和HTML5无障碍性还有更多内容，因此我们鼓励你在以下网站进行进一步阅读：

- `http://w3.org/TR/wai-aria`
- `http://html5accessibility.com`
- `http://paciellogroup.com/blog`

## 高级技巧：为带评论的文章页面进行标记

清单2.16展示了创建带评论的文章页面（图2.9）所需的代码。

它使用了本章涵盖的几项新技术。

### Tom的博客

### 我的文章标题

2010年12月12日，星期日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.

### 评论

1. **13/12/2010 11:15**

   评论者：[Tom Leadbetter](#)

   多么精彩的文章啊！

2. **16/12/2010 11:15**

   评论者：匿名

   那真是垃圾。

**图2.9** 带评论的网站文章

### 清单2.16 带评论的文章

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Blog comments</title>
  <style>
    [role=banner] h1 {background: #333; color: #fff; padding: 5px;}
    [role=main] h1 {border-bottom: 2px dotted #333; color: #333;}
    b {float: left; font-family:"Palatino Linotype", Palatino, serif; font-size: 
    2.5em; font-style: italic; font-weight: bold; line-height: 1; margin: 0 
    5px 5px 0;}
  </style>
</head>
<body>
  <h1 role="banner">Tom's blog</h1><article role="main">
    <header>
      <h1>Title of my article</h1>
      <time pubdate datetime="2010-12-12">Sunday, 12th December 2010</time>
```

## 高级指南：使用注释标记文章页面

```html
<p><b>P</b>ellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor ...</p>
</header>
<section>
    <h2>评论</h2>
    <ol reversed>
        <li>
            <article>
                <h3><time datetime="2010-12-13T11:15Z">2010年12月13日 11:15</time></h3>
                <footer>由 <address><a href="http://tomleadbetter.co.uk">Tom Leadbetter</a></address> 发表的评论</footer>
                <p>多么精彩的文章！</p>
            </article>
        </li>
        <li>
            <article>
                <h3><time datetime="2010-12-16T11:15Z">2010年12月16日 11:15</time></h3>
                <footer>由匿名用户发表的评论</footer>
                <p>这简直是垃圾。</p>
            </article>
        </li>
    </ol>
</section>
</article>
</body>
</html>
```

代码清单2.15使用了一些ARIA地标角色，我们利用这些角色来辅助`h1`标签的样式设计。同时，我们还使用`b`元素来样式化文章的首字母，使其看起来更别致一些。在为`h1`和`b`元素设置样式时，不一定非要使用前面提到的CSS，因为还有其他方法可以定位这些元素，但提供多种选项总是好的。

新的`time`元素被多次使用：一次用于主文章（带有`pubdate`属性），另一次用于每条评论中。在上一章中，我们提到用户评论本身就是一个`article`，因此我们在这里采用了这种结构。在这个例子中，我们使用日期和时间作为评论的标题。我们本可以使用评论者的作者名，但我们不希望在页面大纲中出现重复的标题，而使用日期和时间则为其提供了唯一标识符。这仅仅是个人偏好；没有任何规则禁止你使用，比如，评论作者作为标题。

我们还使用了一个有序列表，这样每条评论都有一个序号。这不仅定义了评论的顺序，也提供了一种样式化的选择。我们在`ol`上使用了`reversed`属性，因为在这个案例中，我们希望最新的评论出现在最上方。这样，我们未来或许可以添加一个“按日期排序”的开关，并通过JavaScript来添加或移除`reversed`属性。同样，你不必完全照搬，有很多替代方案，而且评论区的设计可能意味着你需要考虑其他选择。

# 第2章 分组、文本级与重新定义的语义

## 总结

在本章中，你学习了HTML5中一系列全新的元素以及一些经过微调的元素。像`figure`和`details`这样的新元素，无疑将使开发者的工作在未来变得更加轻松。结合新的ARIA角色，你可以构建出语义更丰富、可访问性更强的文档。此外，你还可以使用微数据向HTML添加更多信息，从而使搜索引擎能够提供更丰富、更精确的数据。

## 3 浏览器中的HTML5处理

尽管HTML5及其相关规范尚未完全定稿，细节也处于不断变化之中，但你现在就可以使用其中的许多功能。HTML5是一门不断发展的语言，并集成了不断增长的JavaScript API。浏览器厂商们正努力跟上这些新规范的快速发展。面对这些不断变化的新功能和浏览器版本，我们开发者常常会遇到浏览器支持问题。在本章中，你将学习如何处理浏览器之间的差异，以及如何运用现有的技巧、窍门和脚本来弥补这些差距。

## 入门指南：处理 Internet Explorer

如果你一直在Internet Explorer（IE）7、8或甚至6（我们真心希望你没有被迫支持IE6）中测试前面章节的代码，那么你可能已经注意到一个小小的问题——你在指南中创建的页面可能无法正常显示。这是因为我们目前提供的代码只能在以下主流浏览器中原生运行：Firefox、Chrome、Safari、Opera和Internet Explorer 9（IE9）。这并不是说IE7和IE8完全不支持HTML5；它们确实支持一些HTML5 API，例如拖放功能和`ContentEditable`。

### 使用 JavaScript 实现 HTML5 兼容性

默认情况下，IE6、7和8无法识别新的HTML5元素，比如`article`或`section`，因此也不会对这些标签应用任何样式。如果你不采取任何措施，页面效果很可能与你预期的不同。为了让IE识别这些元素，你可以通过JavaScript在DOM中以编程方式创建它们，然后相应地设置样式，如下例所示：

第56页 第3章 浏览器中的HTML5处理

```html
<script>
document.createElement('article');
document.createElement('section');
//以及诸如此类的操作
</script>
```

当然，为每一个新的HTML5元素都这样做会有点繁琐，而且你很可能会遗漏某些元素。幸运的是，你可以使用一个叫做HTML5Shiv（`http://code.google.com/p/html5shiv`）的工具，它由Remy Sharp编写，包含了所有新元素。还有一个叫做IE Print Protector（`http://iecss.com/print-protector`）的JavaScript小脚本，可以帮助IE正确显示HTML5元素。这个“shiv”旨在让IE9之前的版本能够识别HTML5元素，并允许通过CSS对它们进行样式化。

尽管这个脚本内部包含条件代码，使其只在IE中运行，但你最好还是自己用一个条件注释将其包裹起来，这样只有IE 8及更早版本会下载并运行此代码。这个脚本必须放在`head`标签内，并且要在样式表调用之前，如代码清单3.1所示。你可以自行决定是选择本地托管html5shiv文件，还是直接链接到`http://googlecode.com`上的文件。将文件放在本地可以避免任何远程访问问题导致的“资源未找到”错误，以及因JavaScript文件未来修改而可能引起的中断。

代码清单3.1 使用HTML5 Shiv

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<!--[if lt IE 9]>
<script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
<![endif]-->
<!-- 在 shiv 之后放置 CSS -->
</head>
```

### 使 CSS 兼容

现在你已经让IE支持了新的HTML5元素，接下来需要让它与CSS良好协作。大多数现代浏览器默认知道如何处理这些新元素，即使没有任何样式也是如此；然而，为了确保IE能正常工作，你需要将新元素的显示属性设置为`block`，如代码清单3.2所示。

代码清单3.2 在CSS中设置新元素

```css
article, aside, details, figcaption, figure, footer, header, hgroup, nav, section
{
display: block;
}
```

如果你使用CSS重置（CSS reset），可以将代码清单3.2中的代码包含进去，或者也可以使用当前各种已包含HTML5修复的CSS重置方案：

- `http://meyerweb.com/eric/thoughts/2011/01/03/reset-revisited`
- Modernizr（我们将在本章稍后介绍）
- `http://html5doctor.com/html-5-reset-stylesheet`

### 样板代码



无论你是 web 开发领域的新手还是老手，你可能都积累了一些最佳实践和代码片段，并在几乎每个项目中重复使用。根据你投入多少时间来组织这些组件，你可能已经有了自己的样板代码，这是一系列文件夹和文件，能让你快速启动项目。目前在 web 社区中正在推广几个流行的样板代码：`http://html5boilerplate.com` 和 `http://html5reset.org`。此外，这些样板代码已经可以通过像 `http://initializr.com` 这样的网站扩展，用于生成针对你特定网站或应用程序的模板，该网站就使用了 HTML5 Boilerplate。

这些网站，尤其是 HTML5 Boilerplate，提供了大量文档、说明以及针对你 web 项目的技巧和窍门，涵盖标记、脚本、CSS 和优化技术。

样板代码的意义不在于直接拿来就用，而在于理解其中的内容，并根据你的需要或偏好增删一些你认为不需要或不认同的部分，这完全没问题。样板代码只是为你提供一个起点，让你受益于众多智慧的结晶，以获得 HTML5 跨浏览器支持和性能结构。你甚至可能最终根据你认为重要的特性，形成自己定制的样板代码。

> **提示**

HTML5 Boilerplate 在项目启动阶段提供了大量可利用的功能和优势。该样板代码包含浏览器兼容性模型、针对旧版浏览器的 HTML5 支持选项、移动设备设计处理，甚至还有一个优化构建脚本。我们建议你查阅 `http://html5boilerplate.com` 上的完整功能列表。如果你需要一个更完善的模板作为起点，可以查看 `http://initializr.com`，它利用 HTML5 Boilerplate 为你创建模板。

## 入门指南：检测 HTML5 功能

在前面，你学习了如何让浏览器识别新的 HTML5 元素，以及如何使用 CSS 让它们正常显示。但并非所有浏览器都支持所有新的 HTML5 功能，比如 `canvas` 或 `geolocation`。虽然你仍然有时……

## HTML5中的浏览器处理

由于需要让浏览器以特定方式运行，你可能不得不进行一些“浏览器嗅探”，但这并不是一个推荐的方法。随着HTML5的广泛采用和浏览器的快速迭代，你可以转而使用特性检测方法。特性检测需要JavaScript，因此你需要确保你的标记足够好，可以“优雅降级”，以便使用旧版浏览器或关闭JavaScript的用户仍然可以使用该网站。

通常，HTML5的特性（如属于HTML5元素和JavaScript API的`canvas`和地理定位），可以通过JavaScript检查它们的存在与否来确定。在清单3.3中，你将对浏览器进行一个简单的检查，以确定其是否支持地理定位API。

```
清单3.3 测试HTML5地理定位支持
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>地理定位检查</title>
<script>
if (navigator.geolocation) {
    alert('Geolocation is supported.');
} else {
    alert('Geolocation is not supported.');
}
</script>
</head>
<body>
</body>
</html>
```

对于JavaScript API，检查其是否存在相当容易，我们将在本书中多次展示。然而，如果你试图检查HTML5元素（如`canvas`元素）的可用性，过程会稍微复杂一些。检查元素是否支持的标准方法是创建该元素，然后尝试检索其默认方法或属性。如果返回的值是`null`或`undefined`，则浏览器不支持该元素。清单3.4展示了一个如何用`canvas`元素进行此检查的例子。

```
清单3.4 检查canvas支持
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>Canvas检查</title>
<script>
if (document.createElement('canvas').getContext) {
    alert('Canvas is supported.');
} else {
    alert('Canvas is not supported.');
}
</script>
</head>
<body>
</body>
</html>
```

你首先创建了一个`canvas`类型的新元素，然后立即检查该元素是否提供了`getContext`方法。你将在本书后面看到`canvas`的各种方法，但目前只需知道`getContext`方法是任何`canvas`对象必需且默认的方法。因此，如果这个元素上不存在`getContext`方法，那么该元素本身也不存在，此浏览器不支持`canvas`。

## 中级技巧：利用jQuery替换日历控件

在第5章中，你将学习所有HTML5中可用的新表单特性，但现在我们将简要介绍其中的一个新特性：日期输入类型。日期输入类型会向用户显示一个日历小部件，如图3.1所示。目前这仅在Opera浏览器中有效，并且虽然在其他浏览器中它会优雅降级，只显示一个用户可以输入日期的普通输入框，但这里你希望在所有浏览器中都出现一个日历小部件。

![图3.1 Opera中的日期输入控件](img/de30ea99ecac39b49e690a84c48f43b9_89_0.png)

![图3.2 Internet Explorer中使用jQuery回退方案的日历](img/de30ea99ecac39b49e690a84c48f43b9_90_0.png)

*图3.2 Internet Explorer中使用jQuery回退方案的日历*

以下是你需要使该输入在Opera中工作的HTML代码：

```
<form>
    <label for="date">What date do you leave?</label>
    <input required type="date" id="date" name="date" />
    <input type="submit" value="Submit" />
</form>
```

使用JavaScript，你将在DOM中创建一个元素，为其添加`type`属性为`date`，然后测试浏览器是否支持它。如果浏览器支持，那么无需做任何事。如果浏览器不支持，那么你将提供一个日历小部件。图3.2显示了Internet Explorer中的日历。清单3.5展示了实现此功能的代码。在这个例子中，我们使用了jQuery来提供日历功能，因此为了方便，我们直接链接了必要的jQuery文件。

### 清单3.5 使用jQuery日历作为回退方案

```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>检测日期输入类型</title>
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.4.4/jquery.min.js"></script>
<script src="http://ajax.googleapis.com/ajax/libs/jqueryui/1.8.7/jquery-ui.min.js"></script>
<link rel="stylesheet" href="http://ajax.googleapis.com/ajax/libs/jqueryui/1.8.7/themes/base/jquery-ui.css" media="screen" />
<script>
$(function(){
  function inputSupport() {
    var input = document.createElement("input");
    input.setAttribute("type", "date");
    var val = (input.type !== "text");
    delete input;
    return val;
  }

  if (!inputSupport() || ($.browser.webkit)) {
    //alert("the date input type is not supported");
    $('input[type=date]').datepicker({
      dateFormat: 'yy-mm-dd' // this format is the same format as in the HTML5 Specification
    });
  }
});
</script>
</head>
<body>
<form>
<label for="date">What date do you leave?</label> <input required type="date" id="date" name="date" />
<input type="submit" value="Submit" />
</form>
</body>
</html>
```

眼尖的你可能已经注意到了下面这段JavaScript代码：`($.browser.webkit)`。我们在清单3.5中包含了它，因为令人沮丧的是，WebKit浏览器确实能检测到`<input type="date">`，但目前它们对此并无任何实际处理。`email`、`number`、`tel`和`url`这些输入类型也是如此。因此，这段小小的JavaScript代码确保了jQuery日历小部件能在Safari和Chrome中工作。我们希望这些基于WebKit的浏览器很快就能默认对这些输入类型做一些了不起的事情，这样我们就可以摆脱浏览器检测代码了。

清单3.5中的JavaScript代码仅处理检测日期类型的支持情况。如果你想检测其他类型，你可能需要调整前面的代码，以便测试多种输入类型。例如，参见清单3.6。

### 清单3.6 检测不同的输入类型

```
$(function(){
  function inputSupport(inputType) {
    var input = document.createElement("input");
    input.setAttribute("type", inputType);
    var val = (input.type !== "text");
    delete input;
    return val;
}
    if (!inputSupport("date")) {
      alert("the date input type is not supported");
      //do something else instead
    }
    if (!inputSupport("email")) {
      alert("the email input type is not supported");
      //do something else instead
    }
});
```

如果你有一个小型网站，可能只有几个新的HTML5元素需要在所有浏览器中可用，那么前面的方法可能适用，因为它是一个相当快速的修复方法。然而，如果你执行大量的功能支持检测，这可能会变得乏味，因此你可能考虑使用像Modernizr这样的JavaScript库。

## 中级技巧：使用Modernizr检测特性

Modernizr是一个JavaScript库（可在 `http://modernizr.com` 找到），它能检测浏览器支持哪些HTML5和CSS3特性，并让开发者能够轻松地针对不支持某些新技术的浏览器进行测试和编码。在前面的例子中，我们使用标准JavaScript来测试特性，但使用Modernizr则非常容易。

尽管Modernizr为你完成了检测部分，但它不会为你填补空白或添加缺失的功能。尽管如此，它是一个极其强大的脚本片段，开发者应该了解并随时准备使用。目前是第2版的Modernizr库专注于CSS3检测、HTML5标签支持和JavaScript API支持。对于这些领域中的每一个，Modernizr库都有特定的属性，可以在初始化后访问，并用于动态更改源内容，从而支持多种体验和浏览器。部分属性标志包括：

- 地理定位API

- `localStorage`

- `sessionStorage`

- 拖放

- 历史管理

- `applicationCache`

- `Canvas`

- Web Sockets

- Web Workers

- Web SQL 数据库

- 输入类型

- 输入属性

Modernizr库，或按其术语称为微库，使用简单，已集成到全球各大网站中。在浏览器统一支持HTML5、CSS3和JavaScript API的所有功能之前，仍需要像Modernizr这样的工具。

那么，如何使用它呢？要生成你的文件，你需要选择想要测试的功能。只选择少量功能很有用，因为这能保持文件大小较小，并让你更具体地思考网站将具备的功能。因此，首先，你需要从该网站生成一个文件，如清单3.7所示，在`head`标签中包含该链接，并在`html`标签上添加`no-js`类。

### 清单3.7 使用Modernizr进行设置

```
<!DOCTYPE html>
<html class="no-js" lang="en">
<head>
    <meta charset="utf-8">
    <title>Let's go Modernizr</title>
    <script src="modernizr.js"></script>
</head>
<body>
</body>
</html>
```

Modernizr脚本在被包含后将自动运行，并会替换添加到`html`元素的`no-js`类属性。该脚本会动态附加CSS类，以显示浏览器支持哪些功能，以及浏览器不支持哪些功能。以下代码显示了Modernizr脚本运行并替换类属性后，在Chrome 8版本中的`html`标签。如你所见，Chrome 8浏览器支持许多CSS3和HTML5的优秀特性，但不支持例如WebGL，因此它添加了一个`no-webgl`类。

```
<html lang="en" class=" js flexbox canvas canvastext no-webgl no-touch geolocation postmessage websqldatabase no-indexeddb hashchange history draganddrop websockets rgba hsla multiplebgs backgroundsize borderimage borderradius boxshadow textshadow opacity cssanimations csscolumns cssgradients cssreflections csstransforms no-csstransforms3d csstransitions fontface video audio localstorage sessionstorage webworkers applicationcache svg inlinesvg smil svgclippaths">
```

清单3.8展示了一个简单的用法，说明Modernizr如何通过检查Session Storage API支持，在CSS标签中暴露不同的功能支持。如果会话存储可用，则将使用`.sessionstorage`类样式；如果会话存储不支持，则将使用`.no-sessionstorage`类样式。

### 清单3.8 使用Modernizr的CSS选项

```
<!DOCTYPE html>
<html class="no-js" lang="en">
<head>
    <meta charset="UTF-8" />
    <title>3 Modernizr CSS</title>
    <style>
        div.storageNo, div.storageYes { display: none }
        .no-sessionstorage div.storageNo { display: block }
        .sessionstorage div.storageYes { display: block }
    </style>
    <script src="modernizr.js" type="text/javascript"></script>
</head>
<body>
    <div class="storageNo">SessionStorage is not supported.</div>
    <div class="storageYes">SessionStorage is supported.</div>
</body>
</html>
```

因此，在前面的示例中，相应的`div`将根据支持情况进行显示。但你可以将其用于任何JavaScript API的使用。所有在Modernizr对象上暴露的属性列表可以在 `http://modernizr.com` 网站的文档部分找到。

尽管这对于CSS开发很有用，但Modernizr拥有丰富的JavaScript属性，可用于功能检测。在清单3.9中，你根据Modernizr对象的一个属性，以编程方式向用户提示会话存储是否可用。

### 清单3.9 使用Modernizr和JavaScript进行功能检测



```html
<!DOCTYPE html>
<html class="no-js">
<head>
    <meta charset="UTF-8" />
    <title>3 Modernizr JS</title>
    <script src="modernizr.js" type="text/javascript"></script>
    <script>
        if (Modernizr.sessionstorage) {
            alert('SessionStorage is supported.');
        } else {
            alert('SessionStorage is not supported.');
        }
    </script>
</head>
<body>
</body>
</html>
```

你还可以将Modernizr与jQuery和其他库结合使用。清单3.5使用了一个JavaScript解决方案，为不支持HTML5日期输入类型的浏览器提供一个日历小部件。在清单3.10中，我们使用Modernizr作为检测工具重新创建了这个示例。

## 清单3.10 使用Modernizr的jQuery日历后备方案

```html
<!DOCTYPE html>
<html class="no-js" lang="en">
<head>
    <meta charset="utf-8">
    <title>Let's go Modernizr</title>
    <script src="modernizr2.js"></script>
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.4.4/jquery.min.js"></script>
    <script src="http://ajax.googleapis.com/ajax/libs/jqueryui/1.8.7/jquery-ui.min.js"></script>
    <link rel="stylesheet"
          href="http://ajax.googleapis.com/ajax/libs/jqueryui/1.8.7/themes/base/jquery-ui.css" media="screen" />
    <script>
        $(function(){
            //check to see browser does not support input type
            if (!Modernizr.inputtypes.date){
                $('input[type=date]').datepicker({
                    dateFormat: 'yy-mm-dd' // same format as in the HTML5 specification
                });
            }
        });
    </script>
</head>
<body>
    <form>
        <label for="date">What date do you leave?</label>
        <input required type="date" id="date" name="date" />
        <input type="submit" value="Submit" />
    </form>
</body>
</html>
```

你通常不需要像我们在清单3.10中那样使用JavaScript的开头部分`$(function(){})`，但在这个示例中，我们使用了一个jQuery日历，所以需要它。这就是全部内容。这真的很容易，Modernizr文档 http://modernizr.com/docs 中有数十个选项，包括使用新测试扩展库的灵活性。

## Polyfilling（填充）

能够检测HTML5支持了哪些功能，无论是使用自己的代码还是使用Modernizr，都只是成功了一半。最终目标是在用户访问你创建的Web应用程序和网站时，能够在他们使用的各种浏览器和浏览器版本中支持HTML5功能。为了允许不支持特定HTML5功能的浏览器使用，你需要使用一个第三方库，该库包含为各种浏览器提供相同功能的代码。允许功能在浏览器上得到支持的代码或代码库被称为*polyfill*（填充）或*polyfiller*（填充器）。填充器的一个例子可以是一个为Internet Explorer提供canvas支持的库，因为Internet Explorer不直接支持canvas元素，但有其自身的绘图功能，如Silverlight。你希望能够使用新的API进行开发，同时仍然为不支持这些API的浏览器提供相同的体验。我们已经看到使用jQuery这样的JavaScript库来填补一些空白的示例，但没有一个库能解决所有问题。

不仅仅是旧浏览器在HTML5功能上存在缺陷；新浏览器也尚未普遍涵盖HTML5。因此，无论是使用自己的检测代码还是使用Modernizr，你都需要加载一个适当的填充库，以在多个浏览器中提供对HTML5功能同等水平的支持。事实上，Modernizr提供了一个通过其`Modernizr.load`方法直接加载脚本的实用程序，该方法基于对特定功能的测试，其结果可以动态加载一个填充器，如这里所示：

```javascript
Modernizr.load({
    test: Modernizr.canvas,
    yep: 'myCanvas.js',
    nope: 'myCanvasPolyfiller.js'
});
```

> **提示**

> `Modernizr.load`方法实际上是一个别名命令，指向一个包含的第三方JavaScript库，名为yepnope.js，你可以在 http://yepnopejs.com 找到它。该库致力于成为一个快速的条件资源加载器，且占用空间小。该库可以单独使用，也可以通过Modernizr load别名方法使用。yepnope JavaScript库通过测试从字符串到数组的各种类型的数据对象，对于有条件地加载CSS或JavaScript非常有益。

目前已经为各种浏览器中的多种组件开发了广泛的填充器；你可以在 http://github.com/Modernizr/Modernizr/ 找到一份广泛的列表。

wiki/HTML5跨浏览器Polyfills。这份有用的列表由Modernizr的首席开发者Paul Irish维护，包含了各种功能的回退方案，如canvas、视频、地理定位、表单等。

> **注意**

> 拥有各种polyfill、shim和库来支持当前可能未在一个或多个浏览器中实现的HTML5功能，是为用户提供跨浏览器统一体验的强有力方式。然而，如果需要加载多个polyfill，可能会对性能产生负面影响。需要在开发中平衡负面的加载时间与获得的功能和支持。

# 实用的HTML5验证网站

我们已经介绍了各种技术和脚本，以了解如何处理不同的浏览器行为，所以这里有一个快速网站列表，可以告诉你哪些浏览器支持哪些功能。随着浏览器更新，或者如果你不确定某个特定功能，可以尝试访问以下网站之一：

- http://findmebyIP.com：提供你启动页面的浏览器的详细信息，包括CSS3、HTML5、Forms 2.0、CSS3选择器测试、脚本支持和IP详情。实际上，它使用Modernizr提供大部分信息。

- http://caniuse.com：提供HTML5、JS API和CSS3与各种浏览器的兼容性表格，并可按需筛选。

- http://html5test.com：测试一组各种HTML5功能，并根据支持情况为你的浏览器评分。这可以比较一个浏览器与其他浏览器。

- http://html5readiness.com：可视化各种浏览器在HTML5功能方面的状态。

## 总结

在本章中，你学习了处理旧版浏览器以及浏览器版本在HTML5方面的缺陷的一些方法。HTML5的情况是，组成HTML5的各种CSS、HTML和JavaScript的附加功能得到了广泛支持，但它仍在不断成熟。你还学习了CSS重置和模板，它们包含了现代、最新的Web开发工具、技巧和技术。

你学习了Modernizr的使用，这是一个强大的脚本，用于功能检测，使你能够为尚不支持某些新HTML5功能的浏览器提供回退方案。我们不会在本书中展示如何使用Modernizr，因为你可能会也可能不会选择在你的网站中使用它，并且我们试图展示执行功能的基础方法。然而，我们推荐并完全期望，使用Modernizr或本章中提到的其他工具将在你的HTML5编码中为你提供益处。

*此页有意留白*

# 使用CSS3的新布局和样式技术

CSS第3级（CSS3）是CSS规范的最新迭代。在先前版本的基础上，CSS3带来了新功能，你可以在最新的浏览器中实现，以改进网页的外观、可用性、可访问性和性能。CSS*不是*HTML5，我们知道这一点，你也需要知道这一点，但我们包含这一章是因为它们通常携手并进，并且我们向你展示的是CSS3可用的一些可能性，以便你能够让你的新HTML5网站看起来非常出色。在本章中，你将学习使用媒体查询进行响应式Web设计、自定义字体、渐变、过渡、变换，最后是动画。我们不会涵盖CSS3的所有新功能；我们只是浅尝了可用功能的表面。

## 中级技巧：使用CSS3媒体查询创建响应式设计

移动浏览一直在增长，有人估计它将在五年内取代桌面浏览。CSS3媒体查询使你能够针对特定的屏幕宽度、高度甚至方向，因此你可以针对像iPhone或Android手机这样的智能手机，以及像iPad这样的新平板设备，全部使用CSS。表4.1显示了支持CSS3媒体查询的每个浏览器的版本。

过去，你可能使用JavaScript来检测移动设备并提供单独的样式表或重定向用户到特定的移动站点。或者你可能使用JavaScript来检测浏览器何时被调整大小，然后改变一些样式以适应布局。我们一直拥有媒体查询的基础，因为我们一直能够针对屏幕或打印：

70  第4章  使用CSS3的新布局和样式技术

**表4.1  CSS3媒体查询设备和浏览器支持**

| 浏览器 | 版本 |
| :--- | :--- |
| Android | 2.3+ |
| Chrome | 13.0+ |
| Firefox | 4.0+ |
| Internet Explorer | 9.0+ |
| iOS Safari | 4.0+ |
| Opera | 11.0+ |
| Safari | 5.0+ |

```html
<link rel="stylesheet" href="screen.css" media="screen" />
<link rel="stylesheet" href="print.css" media="print" />
```

但现在你可以使用CSS3媒体查询更精确地控制。代码清单4.1展示了一个快速示例。

**代码清单4.1  简单的媒体查询示例**

```html
<link rel="stylesheet" media="screen and
(max-device-width: 480px)" href="smartphone.css" />
<link rel="stylesheet" media="screen and
(min-width: 480px)" href="screen.css" />
```

代码清单4.1询问设备其水平分辨率是否为480像素宽或更小。如果是，那么这里假设它是智能手机并加载`smartphone.css`。然后询问分辨率是否至少为480像素宽；如果是，那么可以使用不同的样式表。你可能会尝试针对所有不同类型的设备、分辨率和屏幕方向，拥有几个不同的媒体查询。你可能会为智能手机、横向的智能手机、Android屏幕尺寸、iPad、纵向的iPad、宽度小于800像素的浏览器或宽屏分辨率的浏览器准备样式表。你真的可以非常精确，没有限制。

所以，你需要一个好的方法来组织所有单独的查询。记住，你已经拥有了所有的主样式表。使用代码清单4.1中的方法意味着在`head`标签中会有很多HTTP请求。

或者，你可以在CSS文件中包含媒体查询，如代码清单4.2所示，使用`@media`。

www.it-ebooks.info

**代码清单4.2  在CSS文件中的媒体查询**

```css
body {background: black; color: #fff; font: normal 62.5%/1.5 tahoma, verdana, sans-serif;}
h1 {font-size: 2em;}
p {font-size: 1.4em;}

/* 针对智能手机和非常小屏幕分辨率的样式 */
@media only screen and (min-width: 320px) and (max-width: 400px)
{
body {background: blue;}
}

/* 针对大于智能手机但小于或等于1024px屏幕分辨率的样式 */
@media only screen and (min-width: 401px) and (max-width: 1024px)
{
body {background: red;}
}

/* 针对非常宽的屏幕分辨率的样式 */
@media only screen and (min-width: 2000px)
{
body {background: green;}
}
```

在代码清单4.2中，我们根据屏幕分辨率更改了背景颜色。所有媒体查询都是同一个CSS文档的一部分，因此确保CSS文档组织良好非常重要；你的默认设计可能会有数百行代码，然后为媒体查询添加额外的CSS。根据你的网站设置，在CSS文件中编辑媒体查询类型（例如将`min-width: 2000px`调整为`min-width: 2500px`）可能比在所有页面的HTML中编辑更容易。

使用`and`语法，你可以组合不同的查询。你可以针对多个功能：宽度、高度、设备宽度、设备高度、方向、宽高比、设备宽高比、颜色、颜色索引、单色、分辨率、扫描和网格。结合公认的媒体类型：`all`、`braille`、`embossed`、`handheld`、`print`、`projection`、`screen`和`speech`，你可以组合它们以同时针对多种不同类型的设备和尺寸。值得注意的是，`max-device-width`是设备的屏幕尺寸（如iPhone），而`max-width`仅是视口区域的宽度（如浏览器窗口）；参见以下代码中的区别：

```css
/* 设备小于480px；移动设备、iPhone和普通屏幕 */
@media handheld and (max-width: 480px), screen and (max-device-width: 480px), screen and (max-width: 480px) {
```

www.it-ebooks.info

# 第四章 使用CSS3实现新的布局与样式技术

```css
/* styles go here */
}

/* 布局适用于横屏模式下的iPad */
@media only screen and (min-device-width: 768px) and (max-device-width: 1024px) and (orientation: landscape) {
    /* styles go here */
}
```

> **提示**

> 在接下来的代码示例中，我们使用了不同类型的CSS选择器。第一种是属性选择器，应用于`header[role=banner]`，第二种是伪类选择器，即`nth-xx()`，在多种场景下使用，例如`section:nth-of-type(1)`。属性选择器并非CSS3的新特性，但结合新的ARIA-Roles，它们让你在CSS中拥有了更灵活的选择器运用方式。CSS3引入了许多新选择器，包括`nth-child()`和`nth-of-type()`。使用这些新选择器意味着你可以不必在许多元素上使用类（class）。例如，使用`nth-of-type()`，你可以选中每个奇数位的表格行或列表项。关于这一点的更多信息，我们推荐阅读 http://quirksmode.org/css/nthchild.html。

> 许多新选择器在旧版本的Internet Explorer中无法正常工作，因此我们推荐使用Selectivizr (http://selectivizr.com)，这是一个易于使用的JavaScript工具，能让Internet Explorer理解新的CSS选择器。

图4.1展示了来自第2章的新闻网站示例HTML标记。清单4.3提供了精简后的HTML。清单4.4中的CSS代码用于默认布局，如图4.1所示。

## 清单4.3 新闻网站的精简HTML

```html
<body>

<header role="banner">
  <hgroup></hgroup>
</header>

<nav></nav>

<section> <!-- 此section重复三次 -->
  <article>
    <header></header>
    <img alt="thumbnail" src="box-100x100.gif" />
    <p></p>
  </article>
</section>

<aside></aside>

</body>
```

图4.1 应用默认CSS的新闻网站

## 清单4.4 默认屏幕布局的CSS



```css
<style>
* {margin: 0; padding: 0;}
body {background: #fff; color: #000; font: normal 62.5%/1.5 "Palatino Linotype", "Book Antiqua", Palatino, serif; margin: 0 auto; width: 1260px}
header, nav, section, article, footer, aside {display: block;}
header[role=banner] {margin: 10px 0 20px; text-align: center;}
header[role=banner] h1 {background: url(logo.gif) top center no-repeat;font-size: 5em; padding: 100px 0 0; text-transform: uppercase;}
header[role=banner] h2 {font-style: italic;}
header, nav {clear: both; width: 100%;}
nav {border-bottom: 1px dotted #ccc; padding-bottom: 20px; text-align: center;}
nav li {display: inline;}
nav li a {font-size: 1.4em; padding: .5em;}
section {float: left; margin: 0 0 0 10px; padding: 10px; width: 345px;}
section h1 {margin: 0 0 10px;}
section article {margin: 0 0 10px;}
section article header p {font-size: 1em; font-weight: bold; margin: 0 0 10px;}
section article img {float: left; margin: 0 5px 5px 0;}
section:nth-of-type(1) {clear: both; margin: 0 0 10px; min-height: 200px; padding: 1% 1% 1% 30%; position: relative; width: 69%;}
section:nth-of-type(1) article {margin: 0;}
section:nth-of-type(1) article img  {float: none; height: 200px; left: 0; position: absolute; top: 10px; width: 360px}
section:nth-of-type(2) {margin-left: 0;}
aside {float: right; margin-left: 10px; width: 130px;}
aside img {border: 1px solid #ccc; display: block; margin: 0 auto 10px;}
footer {clear: both;}
h1 {font-size: 2em;}
p {font-size: 1.4em;}
</style>
```

图4.2显示了在较小屏幕尺寸上的布局，使用了清单4.5中的媒体查询。

![新闻网站布局示例](img/de30ea99ecac39b49e690a84c48f43b9_104_0.png)

首页 | 体育新闻 | 娱乐新闻 | 极客新闻 | 关于 | 联系方式

### 今日最热文章

### 体育新闻

文章标题

2010年11月20日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo. Quisque sit amet est et sapien ullamcorper pharetra. Vestibulum erat wisi, condimentum sed, commodo vitae, ornare sit amet, wisi. Aenean fermentum, elit eget tincidunt condimentum, eros ipsum rutrum orci, sagittis tempus lacus enim ac dui. Donec non erat in turpis pulvinar facilisis. Ut felis. Praesent dapibus, neque id cursus faucibus, tortor neque egestas augue, eu vulputate magna eros eu erat.

体育标题.1

2010年11月19日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis.

体育标题.2

2010年11月16日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

体育标题.3

2010年11月16日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

### 娱乐新闻

### 极客新闻

娱乐标题.1

2010年11月20日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis.

极客标题 1

2010年11月20日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis.

娱乐标题.2

2010年11月9日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

极客标题 2

2010年11月16日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

娱乐标题.3

2010年11月16日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

极客标题 3

2010年11月16日

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

炫酷广告

炫酷广告

图4.2 缩小屏幕尺寸后的新闻网站

## 清单4.5 适用于较小屏幕尺寸的CSS

```css
/* 适用于屏幕分辨率大于智能手机但小于等于1280px的样式 */
@media only screen and (min-width: 481px) and (max-width: 1259px)
{
    body {width: 800px;}
    section {margin: 0 0 0 10px;}
    section:nth-of-type(1), section {clear: none; float: left; padding: 10px; width: 375px;}
    section:nth-of-type(1) article img {float: left; height: auto; position: relative; width: auto;}
    section:nth-of-type(2) {margin-left: 10px;}
    section:nth-of-type(3) {clear: both; margin-left: 0;}
    aside {clear: both; float: left; width: 100%;}
    aside img {float: left; margin: 0 10px 0 0;}
}
```

最后，清单4.6包含了在智能手机上显示或浏览器窗口被极度缩小时所需的CSS媒体查询，如图4.3所示。本质上，我们仅用几行额外的CSS，就在小尺寸屏幕上隐藏并调整了几个元素的大小。

![智能手机上的新闻网站](img/de30ea99ecac39b49e690a84c48f43b9_105_0.png)

图4.3 智能手机上的新闻网站

## 清单4.6 适用于智能手机的CSS

```css
/* 适用于智能手机和非常小的屏幕分辨率的样式 */
@media only screen and (max-width: 480px), only screen and (max-device-width: 480px) {
    body {width: 100%;}
    header[role=banner] h1 {background-image: url(logo-small.gif); font-size: 3em; padding: 50px 0 0;}
    section:nth-of-type(1), section {margin: 0 0 10px; min-height: inherit; padding: 0 1%; width: 98%;}
    header[role=banner] h2, img, section article p, aside {display: none;}
    section h2 a {border-bottom: 1px dotted #999; display: block; text-decoration: none;}
    nav, section article:last-of-type h2 a {border: none;}
}
```

## 合理使用

虽然你可以为不同的设备和屏幕尺寸创建独立的样式，但问题是，是否应该总是使用媒体查询？它们在台式电脑和笔记本电脑上无疑很有用，但移动领域的格局已经变化了一段时间。像iPhone和Android设备这样的现代智能手机，其内置的浏览器与桌面浏览器几乎无异，因此它们能处理大多数事务，并且设备的交互性允许用户通过捏合和缩放相对轻松地浏览网站。

使用媒体查询通常意味着你根据屏幕大小来显示/隐藏内容。许多网站，如`http://youtube.com`、`http://facebook.com`、`http://cnn.com`和`http://nfl.com`，都会检测用户是否在使用手持设备，并将其重定向到网站的移动版。他们这样做的原因是他们的网站内容繁重，包含大量数据、图片、视频、广告、Flash以及各种内容。如果这些网站在智能手机上仅使用媒体查询，那么即使用户看不到这些数据，智能手机仍然需要下载所有这些数据。因此，你究竟需要全新的样式还是完全独立的移动站点，取决于你的内容。但如果你只需要更改布局并添加一些小改进，那么你或许应该使用CSS3媒体查询。关于CSS3媒体查询的一些优秀用例，请查看`http://mediaqueri.es`。

## 针对iPhone和Android设备

如果你曾使用媒体查询来针对iPhone或Android设备，你可能会注意到它们并未识别用于小屏幕的CSS更改。这是因为现代智能手机浏览器功能强大，默认情况下，它们显示网页的方式与桌面浏览器相同。然后浏览器会缩小网站以适应小屏幕，这常常导致文本和图片变得很小，用户不得不放大才能阅读和浏览。你可以强制浏览器使用设备的宽度作为视图区域的宽度，也称为视口（view-port）。以下代码应放在`head`标签中：

```html
<meta name="viewport" content="width=device-width; initial-scale=1.0; " />
```

## 初学者食谱：使用 @font-face 自定义字体

尽管`@font-face`并非CSS3的新特性，但在CSS3旗帜下它重新焕发生机，如今网页设计师和开发者在选择网站字体和实现方面有了大量选择。表4.2展示了各浏览器支持`@font-face`的版本。

表4.2 `@font-face`设备与浏览器支持情况

| 浏览器         | 版本   |
|-----------------|---------|
| Android         | 2.3+    |
| Chrome          | 13.0+   |
| Firefox         | 4.0+    |
| Internet Explorer | 6.0+   |
| iOS Safari      | 4.0+    |
| Opera           | 11.0+   |
| Safari          | 5.0+    |

> **注意**
>
> `@font-face`在1998年的CSS2规范中就被纳入；然而，由于浏览器实现不佳、字体文件类型混淆，以及对使用字体的合法性和许可问题的担忧，它当时几乎未被使用。Internet Explorer 4甚至支持自定义字体，尽管仅限于EOT格式。

通过`@font-face`，你只需几行CSS即可嵌入自己的字体。图4.4中的`h1`标题使用的是一种名为Anagram的字体（稍后会介绍字体获取途径），但该字体可用于任何元素。

![](img/de30ea99ecac39b49e690a84c48f43b9_107_0.png)

代码清单4.7展示了图4.4所需的代码，并提供了`@font-face`最简单用法的示例。你在`font-family`中将字体命名为Anagram（你也可以随心所欲地命名，稍后会再次引用它），请参阅`h1`的字体值。在`@font-face`声明中，字体的`src`与HTML页面位于同一目录；如果你想的话，也可以将其放在不同的目录。

### 代码清单4.7 最简形式的`@font-face`

```html
<style>
@font-face {
    font-family: Anagram;
    src: url('anagram.ttf');
}
h1 {
    font-family: Anagram, Tahoma, Verdana, sans-serif;
    font-size: 9em;
}
</style>
<header role="banner">
    <hgroup>
        <h1>Loads of News</h1>
        <h2>Bringing you all kinds of news!</h2>
    </hgroup>
</header>
```

## 文件格式与跨浏览器修复

代码清单4.7仅使用了`.ttf`（TrueType/OpenType）字体文件。不出所料，这会产生跨浏览器实现问题。存在几种不同的字体文件格式：

- 嵌入式OpenType（`.eot`）
- OpenType PS（`.otf`）
- TrueType/OpenType（`.ttf`）
- SVG（`.svg`）
- WOFF（`.woff`）

WOFF是字体的新网络标准。Internet Explorer 8及更早版本需要`.eot`字体，但Internet Explorer 9将支持新的WOFF格式。尽管Safari很早以前就支持`.ttf`，但iPhone和iPad直到最近才开始支持`.ttf`格式；此前，它们需要`.svg`字体。因此，你需要做的是以不同格式提供相同的字体。为此，你需要自行转换字体，或使用像Font Squirrel（`http://fontsquirrel.com`）这样的工具。`@font-face`生成器允许你上传字体并将其转换为不同格式。它还会生成必要的CSS代码，使字体能够在不同浏览器中工作，如代码清单4.8所示。

### 代码清单4.8 跨浏览器的@font-face



```css
@font-face {
    font-family: 'AnagramRegular';
    src: url('type/Anagram-webfont.eot');
    src: url('type/Anagram-webfont.eot?#iefix') format('embedded-opentype'),
         url('type/Anagram-webfont.woff') format('woff'),
         url('type/Anagram-webfont.ttf') format('truetype'),
         url('type/Anagram-webfont.svg#webfontCiW7vqzS') format('svg');
}
```

在代码清单 4.8 中，你引用了同一字体的四种不同格式。将字体组织在一个单独的文件夹中可能值得，就像你处理图片一样。前面的代码顺序是为了让 Internet Explorer 正常工作，并修复了 Android 中的一个错误。前面的代码已经历了多次迭代，但随着浏览器的发展，发现了更多问题。目前，当你生成字体包时，Font Squirrel 提供的就是前面的代码，但当然，未来它可能会有变化。

## 字体服务

找到合适的字体可能很困难。找到一种可以合法在网页上使用的字体则更难。Font Squirrel 允许你将字体转换为各种必要的格式。为此，你必须勾选一个方框，上面写着“是的，我上传的字体在法律上有资格用于网页嵌入”。如果你勾选此项但并非完全确定，那么你可能会面临一些法律问题。

如果你需要免费字体，我们建议浏览 Font Squirrel 上的字体库，因为该网站不仅提供字体生成器，其主要重点是提供完全免费供商业使用的字体。而且，他们不会随便放任何免费字体；他们确保字体是高质量的。Font Squirrel 并非获取免费网络字体的唯一途径，但在其他地方搜索时，请注意合法性问题。

另一个免费字体的选择是 Google 字体目录 (http://code.google.com/webfonts)。使用可用的 API，使用它们提供的字体非常容易。由于字体由 Google 托管，加载时间将非常短。使用 Google 字体时，你只需找到一种字体并选择“使用此字体”。它会为你提供所需的 HTML 和 CSS，如果字体有额外的字重，还会提供选择。放入 `<head>` 标签的 HTML 代码类似于：

```html
<link href='http://fonts.googleapis.com/css?family=Yanone+Kaffeesatz' rel='stylesheet' >
```

Google 会为你提供放入 CSS 字体栈的字体名称：

```css
h1 {font-family: 'Yanone Kaffeesatz', arial, serif;}
```

就是这么简单。

# 第 4 章 CSS3 新的布局与样式技术

> **提示**
>
> 你可能在前面的示例中注意到，在声明自定义字体后，我们列出了一些网页安全字体，例如 `font-family: 'Yanone Kaffeesatz', arial, serif`。我们提供后备字体以防自定义字体检索出错。服务器可能有问题，浏览器可能无法检索到我们想要的自定义字体，因此使用字体栈，我们可以提供一个已知可用的字体作为后备。在使用 CSS `font-family` 时，应始终提供字体栈。

如果 Font Squirrel 或 Google 字体目录无法提供你正在寻找的字体，那么还有其他服务可用。由于许可问题多年来一直存在，许多主要字体铸造厂已经开始要么创建自己的框架，允许你合法安全地使用他们的字体，要么与第三方合作来帮助提供这些字体。

像 FontDeck 和 TypeKit 这样的服务使你能够注册并从一系列字体中选择，所有这些字体都经过调整以在屏幕上提高可读性。FontDeck 和 TypeKit 提供字体的方式略有不同，但在两个服务上设置、选择和激活字体都非常轻松。两个服务都有带某些限制的免费账户，并提供各种定价套餐。

## 中级食谱：使用 CSS 渐变和多重背景制作按钮

你可以使用 CSS3 渐变来制作精美的细微渐变或一些古怪、丑陋的渐变。你无需创建图像，而且渐变是可伸缩的，因此一旦掌握，它比创建、编辑和重新创建图像要省事得多，因为你可以全部通过代码完成。表 4.3 展示了各浏览器支持 CSS3 渐变的版本。

表 4.3 渐变设备与浏览器支持情况

| 浏览器         | 版本   |
|-----------------|---------|
| Android         | 2.3+    |
| Chrome          | 13.0+   |
| Firefox         | 4.0+    |
| Internet Explorer | -       |
| iOS Safari      | 4.0+    |
| Opera           | 11.0+   |
| Safari          | 5.0+    |

图 4.5 一个简单的 CSS3 线性渐变

代码清单 4.9 包含了一个从白色到黑色的基本渐变代码，如图 4.5 所示。

### 代码清单 4.9 简单的 CSS 线性渐变

```css
div {
    height: 200px;
    width: 200px;
    background: url(gradient.gif); /* for browsers that can't do gradients */
    background: -moz-linear-gradient(white, black);
    background: -webkit-linear-gradient(white, black);
    background: linear-gradient(white, black);
}
```

首先，设置渐变类型（线性或径向），然后是包含渐变起始和结束颜色的括号。你会注意到代码有四个不同的声明。第一个是浏览器不支持 CSS3 渐变时的后备颜色；`-moz-linear-gradient` 用于 Mozilla（Firefox）浏览器；`-webkit-gradient` 用于 WebKit（Safari 和 Chrome）浏览器；最后一个 `background` 声明是官方的 CSS3 渐变语法，但目前没有浏览器支持它。

> **注意**
>
> 2008 年，WebKit 是第一个开始使用渐变的引擎，并使用了自己的语法风格。随着 CSS 渐变变得更受欢迎，Mozilla 实现了与官方规范非常接近的语法。然而，在 2011 年 1 月，有消息称 WebKit 将更改其渐变语法，并开始使用与 Mozilla 和官方规范相同的风格，这对每个人来说都是好消息，因为原始的 WebKit 语法更复杂且不是基于标准的。本书使用的是新的 WebKit 语法。

代码清单 4.10 使用了输入按钮，并结合了属性选择器、盒子阴影、圆角边框、多重背景和 CSS 渐变来实现图 4.6 中的效果。在 `background` 属性中，你用逗号分隔多个背景样式。因此，首先是你想要使用的图像，然后设置渐变样式。如果先使用渐变样式，它会覆盖图像。

# 第4章 CSS3 新布局与样式技术

![](img/de30ea99ecac39b49e690a84c48f43b9_112_0.png)

图 4.6 CSS3 按钮渐变效果

## 清单 4.10 按钮的渐变效果

```css
input {
  border: none;
  -webkit-box-shadow: 0 1px 5px rgba(0, 0, 0, .4);
  box-shadow: 0 1px 5px rgba(0, 0, 0, .4);
  -webkit-border-radius: 10px;
  border-radius: 10px;
  cursor: pointer;
  color: #fff;
  font: bold 1.2em Arial, Helvetica, sans-serif;
  margin: 0 10px 0 0;
  padding: 10px 10px 10px 30px;
  text-shadow: 0 2px 2px rgba(0, 0, 0, 0.25);
}

input[type="submit"] {
  background: url(accept.png) 8px 55% no-repeat #91BD09;
  background: url(accept.png) 8px 55% no-repeat, -webkit-linear-gradient(#91BD09, #578730);
  background: url(accept.png) 8px 55% no-repeat, -moz-linear-gradient(#91BD09, #578730);
  background: url(accept.png) 8px 55% no-repeat, linear-gradient(#91BD09, #578730);
}

input[value="Cancel"] {
  background: url(cross.png) 8px 55% no-repeat #b53109;
  background: url(cross.png) 8px 55% no-repeat, -webkit-linear-gradient(#b53109, #540303);
  background: url(cross.png) 8px 55% no-repeat, -moz-linear-gradient(#b53109, #540303);
  background: url(cross.png) 8px 55% no-repeat, linear-gradient(#b53109, #540303);
}

input[type="reset"] {
  background: url(error.png) 8px 55% no-repeat #f0bb18;
  background: url(error.png) 8px 55% no-repeat, -webkit-linear-gradient(#f0bb18, #a46b07);
  background: url(error.png) 8px 55% no-repeat, -moz-linear-gradient(#f0bb18, #a46b07);
  background: url(error.png) 8px 55% no-repeat, linear-gradient(#f0bb18, #a46b07);
}
```

您可以实现的效果远不止两种颜色之间的简单淡入淡出。通过使用色标，您可以向渐变中添加多种颜色，如图 4.7 所示。色标在每个逗号后添加，并且可以指定其起始位置，如清单 4.11 所示。

清单 4.11 展示了用于制作图 4.7 左侧图像的代码。渐变变得更为复杂，但本质上，每个逗号都开始一个新的渐变部分，并为它传递颜色值以及起始的百分比位置。

您可以通过更改诸如 `left` 和 `left top` 这样的声明来倾斜渐变，如清单 4.11 所示，这给出了图 4.7 的右侧图像。

```css
清单 4.11 带有多个色标的渐变
div {
    height: 200px;
    width: 200px;
    background-color: #000;
    background: -moz-linear-gradient(45deg, #000000 0%, #FFFFFF 25%, #000000 50%,
    #FFFFFF 75%, #000000 100%);
    background: -webkit-linear-gradient(45deg, #000000 0%, #FFFFFF 25%, #000000 50%,
    #FFFFFF 75%, #000000 100%);
    background: linear-gradient(45deg, #000000 0%, #FFFFFF 25%, #000000 50%, #FFFFFF
    75%, #000000 100%);
}
```

CSS3 渐变提供了大量选项，包括创建径向渐变，因此我们推荐尝试一些渐变生成器来激发您的创意：

- http://colorzilla.com/gradient-editor
- http://westciv.com/tools/radialgradients/index-moz.html
- http://display-inline.fr/projects/css-gradient/

![](img/de30ea99ecac39b49e690a84c48f43b9_113_0.png)

## 中级技巧：使用变形与过渡增强网站

以前，Web 开发人员需要使用 JavaScript 或 Flash 等插件来在网页上实现效果和动画。但现在，您可以仅使用 CSS 就能旋转和调整 HTML 元素的大小。由于目前还没有浏览器采用官方的 CSS 语法，因此您需要为每个浏览器厂商添加 CSS。这意味着您将拥有重复的 CSS，但目前必须这样做，而且这实际上并不算额外的太多工作。表 4.4 显示了支持变形和过渡的各浏览器版本。

### 表 4.4 CSS 变形和过渡的设备与浏览器支持

| 浏览器 | 版本 |
| :--- | :--- |
| Android | 2.3+ |
| Chrome | 13.0+ |
| Firefox | 4.0+ |
| Internet Explorer | 9.0+ |
| iOS Safari | 4.0+ |
| Opera | 11.0+ |
| Safari | 5.0+ |

图 4.8 显示了应用于图形元素的旋转变形。

要创建图 4.8 中的效果，您需要将 `transform` 属性的 `rotate` 值应用于 `figure` 和 `h1`。如清单 4.12 所示，您必须使用多个浏览器特定的 CSS 前缀才能使该效果在 WebKit、Mozilla 和 Opera 中工作。这里有一个 `-ms-` 前缀，尽管目前 IE9 测试版不支持 `transform` 效果；我们希望当您阅读本书时，它已经支持了。

## 清单 4.12 CSS 变形

```css
* {
margin: 0;
padding: 0;
}
body {
font: normal .9em Arial, Helvetica, sans-serif;
position: relative;
padding: 30px 10px 10px 75px;
width: 600px;
}
h1 {
left: -100px;
position: absolute;
top: 160px;
text-align: left;
-webkit-transform: rotate(270deg);
-moz-transform: rotate(270deg);
-o-transform: rotate(270deg);
-ms-transform: rotate(270deg);
transform: rotate(270deg);
}
figure {
background: #fff;
border: 1px solid #BFBFBF;
-webkit-box-shadow: 2px 2px 4px rgba(0,0, 0, 0.3);
-moz-box-shadow: 2px 2px 4px rgba(0,0, 0, 0.3);
box-shadow: 2px 2px 4px rgba(0,0, 0, 0.3);
display: block;
float: right;
margin: 20px 20px 50px 50px;
padding: 5px;
text-align: center;
-webkit-transform: rotate(10deg);
-moz-transform: rotate(10deg);
-o-transform: rotate(10deg);
-ms-transform: rotate(10deg);
transform: rotate(10deg);
}
figcaption {
clear: both;
display: block;
font-weight: bold;
padding: .5em 0;
}
p {
margin: 0 0 1em;
}
```

```html
<h1>This is the page title</h1>
<p>Pellentesque habitant morbi tristique sen.....</p>
<figure>
<img alt="Sandy beach" src="beach.jpg" />
<figcaption>
The view from our hotel room
</figcaption>
</figure>
<p>Pellentesque habitant morbi tristique sen.....</p>
```

![](img/de30ea99ecac39b49e690a84c48f43b9_116_0.png)

图 4.8 使用 CSS 旋转的图像和文本

图 4.8 使用了 CSS `transform` 属性的 `rotate` 函数，但您还可以使用其他几个函数：`translate`、`scale` 和 `skew`。清单 4.13 展示了实现这些效果所需的示例代码（不要忘记添加浏览器特定的前缀）。代码展示了变形效果应用于文本，但它们可以应用于任何元素，包括 `body`。

## 清单 4.13 更多 CSS 变形选项



```css
h1 {transform: translate(100px, 200px)}
h1 {transform: skew(40deg);}
h1 {transform: scale(2);}
/* 您还可以在单个声明中将它们链接在一起： */
h1{transform: translate(100px, 200px) skew(40deg) skew(2) rotate(40deg);}
```

您还可以进行过渡和动画。CSS 过渡和 CSS 动画之间存在差异。过渡是由鼠标悬停（`:hover`）或鼠标点击（`:active`）触发的两个状态之间的过渡。CSS 动画是时间线动画，可以自行运行。

WebKit 很久以前就支持过渡了，Mozilla 和 Opera 现在也实现了 CSS 过渡；遗憾的是，目前 IE 还不支持。过渡使用前面展示的`transform`属性，并可以应用于`:hover`或`:active`。您无需在悬停时立即更改元素的值，而是可以使用 CSS`transition`属性来动画化到这些新值。图 4.9 显示了一个普通文本链接的基本示例。

![](img/de30ea99ecac39b49e690a84c48f43b9_117_0.png)

图 4.9 带有悬停效果的文本链接

图 4.10 显示了鼠标悬停时链接背景渐变为空白、文本渐变为白色的过渡中间效果和最终效果。在黑白印刷的书籍中很难呈现这种效果，因此我们强烈建议您在浏览器中尝试一下。

清单 4.14 展示了此鼠标悬停效果的代码。您希望动画化到的颜色更改位于`:hover`上。没有任何过渡时，颜色会在`:hover`时立即改变，但要获得淡入淡出效果，您可以使用`transition`属性（以及 WebKit、Mozilla 和 Opera 的浏览器特定前缀）。这是您需要的 CSS 关键部分：`transition: all 1s ease-in;`。这里您是在告诉浏览器动画化所有属性（背景和颜色），使用`ease-in`时间函数，并且过渡的总持续时间为一秒（`1s`）。您可以选择包含一个延迟值，例如`transition: all 1s ease-in 1s;`，它会延迟过渡的开始，并延迟元素恢复到其默认状态。

## 清单 4.14 鼠标悬停时的颜色动画变化

```css
a {
  background: #fff;
  border-radius: 5px;
  display: block;
  float: left;
  padding: 5px;
  text-align: center;
  width: 125px;
  -webkit-transition: all 1s ease-in;
  -moz-transition: all 1s ease-in;
  -o-transition: all 1s ease-in;
  transition: all 1s ease-in;
}

a:hover {
  background: #000;
  color: #fff;
}
```

![](img/de30ea99ecac39b49e690a84c48f43b9_117_1.png)

图 4.10 过渡效果

# 第四章 使用CSS3的新布局与样式技术

![](img/de30ea99ecac39b49e690a84c48f43b9_118_0.png)

图4.11 转换效果前的照片画廊

![](img/de30ea99ecac39b49e690a84c48f43b9_118_1.png)

图4.12 鼠标悬停时的照片画廊图片

因此，你可以使用过渡来实现微妙的小效果，也可以用它们来增强页面的用户体验。以图4.11中的缩略图照片画廊为例。使用清单4.15中的代码，通过结合`rotate`和`scale`，你可以创建一个美观的悬停效果，以全尺寸显示图片，无需JavaScript，如图4.12所示。

## 清单4.15 鼠标悬停时的动画图像缩放

```
img {
background: #fff;
border: 1px solid #BFBFBF;
display: block;
float: left;
height: 125px;
margin: 0 10px 0 0;
padding: 5px;
width: 125px;
-webkit-box-shadow: 2px 2px 4px rgba(0,0,0,0.3);
-moz-box-shadow: 2px 2px 4px rgba(0,0,0,0.3);
box-shadow: 2px 2px 4px rgba(0,0,0,0.3);
-webkit-transition: all 1s ease-in-out;
-moz-transition: all 1s ease-in-out;
-o-transition: all 1s ease-in-out;
}

img:hover {
-webkit-transform: rotate(10deg) scale(2);
-moz-transform: rotate(10deg) scale(2);
-o-transform: rotate(10deg) scale(2);
-ms-transform: rotate(10deg) scale(2);
transform: rotate(10deg) scale(2);
}
```

使用更多CSS，结合`:after`伪元素和CSS`content`属性，你可以在图片放大时显示其`alt`标签。代码在清单4.16中，并扩展了清单4.15的代码。这段CSS在`:hover`时显示`img`的`alt`属性，为照片画廊添加更多信息。你可以用JavaScript在其他浏览器中实现此效果，尽管我们已经简要提到了`:after`伪元素，但我们鼓励你了解更多关于它的内容（以及`:before`伪元素），它可以在网页开发中以多种创造性的方式使用。目前，此效果仅适用于Opera浏览器中的图片，所以如果你有Opera浏览器，可以试试这段代码。

## 清单4.16 图片悬停时显示alt文本

```
img {
position: relative;
}

img:hover {
z-index: 2;
}

img:hover:after {
content: attr(alt);
display: block;
position: absolute;
bottom: -45px;
left: 0;
z-index: 2;
text-align: center;
}
```

## 高级技巧：使用CSS创建动画

与过渡不同，动画不需要通过鼠标悬停或点击效果来触发。目前，动画仅在WebKit浏览器和最新版本的Firefox中可用，但通过使用各种JavaScript技术，你可以在其他浏览器中实现动画。表4.5列出了支持CSS动画的各浏览器版本。

### 表4.5 CSS动画设备与浏览器支持

| 浏览器 | 版本 |
| :--- | :--- |
| Android | 2.3+ |
| Chrome | 13.0+ |
| Firefox | 5.0+ |
| Internet Explorer | - |
| iOS Safari | 4.0+ |
| Opera | - |
| Safari | 5.0+ |

对于一个基本的例子，你将把图像从屏幕左侧移动到右侧，并在移动过程中使其旋转。展示这个效果的截图意义不大，所以请打开Chrome、Firefox或Safari浏览器，尝试清单4.17中的代码。

### 清单4.17 CSS动画

```
/* CSS */

div {
  float: left;
  height: 100%;
  position: relative;
  width: 100%;
}
img {
  position: absolute;
  -webkit-animation-name: moveIt;
  -webkit-animation-duration: 5s;
  -webkit-animation-iteration-count: infinite;
  -webkit-animation-timing-function: linear;
  -moz-animation-name: moveIt;
  -moz-animation-duration: 5s;
  -moz-animation-iteration-count: infinite;
  -moz-animation-timing-function: linear;
  animation-name: moveIt;
  animation-duration: 5s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}

@-webkit-keyframes moveIt {
from {
left: 0;
-webkit-transform:rotate(0deg);
}
to {
left: 100%;
-webkit-transform:rotate(360deg);
}
}

@-moz-keyframes moveIt {
from {
left: 0;
-moz-transform:rotate(0deg);
}
to {
left: 100%;
-moz-transform:rotate(360deg);
}
}

@keyframes moveIt {
from {
left: 0;
transform:rotate(0deg);
}
to {
left: 100%;
transform:rotate(360deg);
}
}

/* HTML */
<div>
<img src="beach.jpg" width="250" height="188" alt="Beach">
</div>
```

在`img`选择器上，有四个动画CSS属性。它们被重复定义，因为必须显式地针对`-webkit-`、`-moz-`前缀。最后，你包含了非浏览器特定的属性名，以备所有浏览器都支持CSS动画的那一天：

- `-webkit/moz-animation-name`：你想要使用的动画名称
- `-webkit/moz-animation-duration`：动画将持续多长时间
- `-webkit/moz-animation-iteration-count`：动画重复的次数
- `-webkit/moz-animation-timing-function`：动画类型；可从`ease`、`linear`、`ease-in`、`ease-out`、`ease-in-out`以及自定义的`cubic-bezier`中选择

![](img/de30ea99ecac39b49e690a84c48f43b9_122_0.png)

图4.13 正在动画化的背景颜色

接下来，你定义动画`@-webkit/moz-keyframes moveIt`。这是一个简单的动画，所以你以`from`属性开始，以`to`值结束。在这些属性中，你使用普通的CSS来移动图像并对其进行旋转。你可以在这些动画中更改几乎所有的CSS属性，因此这里有巨大的潜力。

你不仅仅可以使用`from`和`to`属性；你还可以使用百分比来设置关键帧，这为你提供了更大的灵活性。图4.13显示了一个位于页面右上角的横幅。使用清单4.18中的代码，背景颜色在颜色之间平滑地淡入淡出，关键帧设置在动画时间线的每25%处。

### 清单4.18 动画横幅

```
p {
  background: #000;
  color: #fff;
  font: bold 20px Tahoma, Geneva, sans-serif;
  padding: 10px;
  position: absolute;
  right: -65px;
  text-align: center;
  top: 75px;
  width: 300px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -o-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
  -webkit-animation-name: glow;
  -webkit-animation-duration: 5s;
  -webkit-animation-iteration-count: infinite;
  -webkit-animation-timing-function: ease-in;
  -webkit-backface-visibility: hidden;
  -moz-animation-name: glow;
  -moz-animation-duration: 5s;
  -moz-animation-iteration-count: infinite;
  -moz-animation-timing-function: ease-in;
  animation-name: glow;
  animation-duration: 5s;
  animation-iteration-count: infinite;
  animation-timing-function: ease-in;
}

@-webkit-keyframes glow {
0% {
background: #F00;
}
25% {
background: #06C;
}
50% {
background: #000;
}
75% {
background: #06C;
}
100% {
background: #F00;
}
}

@-moz-keyframes glow {
0% {
background: #F00;
}
25% {
background: #06C;
}
50% {
background: #000;
}
75% {
background: #06C;
}
100% {
background: #F00;
}
}

@keyframes glow {
0% {
background: #F00;
}
25% {
background: #06C;
}
50% {
background: #000;
}
75% {
background: #06C;
}
100% {
background: #F00;
}
}
```

> **提示**
>
> 过渡和动画有多种用途。它们不仅为网页添加了美观的效果，也帮助了设计师和开发者，他们可以快速地创建和调整这些效果。本章我们只展示了基本示例以激发你的兴趣，因此如何发挥创意取决于你自己。然而，能力越大，责任越大，所以请不要过度使用所有这些不同的效果，因为它们可能迅速将一个优秀的网站变得俗气。过多的过渡和动画也可能影响浏览器的性能。我们建议花时间在网上搜索示例，并研究其他设计师和开发者如何使用CSS3改进网站。

## 总结

在本章中，你了解了一些CSS的新特性：媒体查询、字体、渐变、变换、过渡和动画。除了我们描述的这些特性之外，还有更多的特性；我们只是浅尝辄止。利用这些新特性，你可以实现的可能性是无穷无尽的。如果你对CSS感兴趣，那么我们建议你进行进一步的研究和学习，因为在使用其中一些新特性时，还有许多其他的技术和最佳实践。去探索吧，尽情玩转CSS吧。

# 5 HTML5 网页表单

在本章中，你将学习关于 HTML5 网页表单的内容，以及现在可供网页开发者使用的全新功能。当然，并非所有这些新功能都得到所有浏览器的完全支持，但正如你将在本章各处的示例中看到的那样，新功能能够优雅地降级。有超过十种新的输入类型和若干新属性可供选择，以及一些你可以用来创建表单的新 CSS 技巧。

## 验证

尽管有几种新的输入类型，但毫无疑问，最大的新功能是 HTML5 提供的内置表单验证。以前，你必须使用像 PHP 或 C# 这样的服务器端代码来检查提交的表单内容，然后返回页面并向用户显示错误。或者你必须使用一些复杂的 JavaScript 来即时检查输入的数据内容，并告诉用户是否存在任何错误。

有了 HTML5，表单验证变得轻而易举；你可以在用户尝试提交表单时提供内联验证和反馈，这使得表单更易于填写，并增加了提交正确信息的机会。当然，你仍然需要一些服务器端代码来实际处理表单并将其发送到目的地。

在本章各处的示例中，我们在大多数表单元素上添加了一个`required`属性；这是为了让你在测试它们时，可以看到浏览器显示了哪些验证消息（如果有的话）。此属性告诉浏览器，如果该元素未完成，就无法发送表单。

## HTML 4 输入类型

我们将非常简要地提及那些在网页开发中使用了多年的表单元素。它们仍然是基础且完全有效的表单元素，并未被取代。它们仍将在 HTML5 和表单开发中被广泛使用。

96 第 5 章 HTML5 网页表单

![](img/de30ea99ecac39b49e690a84c48f43b9_126_0.png)

图 5.1 HTML5 之前的表单控件

本质上，你拥有 form 元素、一个 fieldset（fieldset 是一个用于在表单中对相关字段进行分组的元素），以及常见的表单元素，它们为你提供了图 5.1 所示的表单控件。

清单 5.1 提供了图 5.1 的 HTML 代码。请注意，使用了无序列表（`ul`）和列表项（`li`）来格式化此表单。这不是组织表单的唯一方式，但它意味着你不必在代码中使用不必要的`<br/>`。

### 清单 5.1 包含不同表单元素的页面



```
<form>
  <fieldset>
    <legend>Fieldset legend - a caption/title for this set of fields</legend>
    <ul>
      <li><label for="normal">Normal input box</label> <input id="normal"
        type="text" value="a 'normal' input box" /></li>
      <li><input id="checkbox" type="checkbox" /> <label for="checkbox">I'm a
        checkbox</label></li>
      <li><input id="radio" type="radio" /> <label for="radio">I'm a radio
        button</label></li>
      <li><label for="file">Upload</label> <input id="file" type="file" /></li>
      <li><label for="password">Password</label> <input id="password"
        type="password" value="mypassword" /></li>
      <li><label for="textarea">Textarea</label> <textarea id="textarea" rows="5"
        cols="40">This is a textarea</textarea></li>
      <li><label for="select">Select</label>
        <select id="select">
          <option>Option 1</option>
          <option>Option 2</option>
          <option>Option 3</option>
          <option>Option 4</option>
        </select></li>
      <li><input type="submit" value="Submit" /></li>
      <li><input type="reset" value="Reset" /></li>
    </ul>
  </fieldset>
</form>
```

HTML5 中有几种新的输入类型，对于创建表单或更新旧表单非常有用。它们将使你作为开发者的任务更轻松，同时也能帮助用户输入正确的数据。

## 初学者示例：创建一个收集联系信息的表单

清单 5.2 使用了三种新的输入类型来收集用户的联系信息：`email`、`tel` 和 `url`。查看代码；输入类型以粗体突出显示，并在后续章节中进一步讨论。

### 清单 5.2 使用新 HTML5 表单元素的联系表单

```
<form>
  <fieldset>
    <legend>Contact information</legend>
    <ul>
      <li>
        <label for="email">Email</label>
        <input required type="email" id="email" name="email" />
      </li>
      <li>
        <label for="tel">Telephone number</label>
        <input required type="tel" id="tel" name="tel" />
      </li>
      <li>
        <label for="url">Website</label>
        <input required type="url" id="url" name="url" />
      </li>
    </ul>
    <input type="submit" value="Submit this" />
  </fieldset>
</form>
```

## `input type="email"`

`email` 输入类型告诉浏览器，此字段的内容应该看起来像一个电子邮件地址。在清单 5.3 中，我们在 `email` 输入上放置了一个 `required` 属性。这将指示兼容的浏览器在提交表单前检查此字段的内容。它不会检查电子邮件地址是否实际存在。

### 清单 5.3 email 输入类型

```
<form>
  <label for="email">Email</label>
  <input required type="email" id="email" name="email" />
  <input type="submit" />
</form>
```

**表 5.1 `email` 输入类型的设备和浏览器支持**

| 浏览器 | 版本 |
| :--- | :--- |
| Android | 2.3+* |
| Chrome | 10.0+ |
| Firefox | 4.0+ |
| Internet Explorer | 9.0+* |
| iOS Safari | 4.0+* |
| Opera | 10.0+ |
| Safari | 5.0+* |

\* 无验证

随着浏览器发展越来越快，试图保持领先并相互超越，它们处理验证的方式存在差异。表 5.2 中的测试突出显示了浏览器处理表单、表单验证和反馈方面的差异。早些时候，验证消息与测试中显示的不同。还要注意，`test@test` 在 Firefox 中是有效的，但在 Opera 中不是，这是两个浏览器之间最显著的差异。

在撰写本文时，在 Chrome 或 Safari 中使用前面的示例时，没有浏览器验证。

> 注意：你可能想知道是否可以为表单反馈设置样式。嗯，答案是，某种程度上可以。我们将在本章后面讨论 CSS。

**表 5.2 `email` 输入类型验证测试**

| 提交的数据 | Firefox 4 响应 | Firefox 4：表单是否提交？ | Opera 11 响应 | Opera 11：表单是否提交？ |
|---|---|---|---|---|
| 未输入数据 | “请填写此字段” | 否 | “此为必填字段” | 否 |
| test | “请输入电子邮件地址” | 否 | “请输入有效的电子邮件地址” | 否 |
| test@test.com | 无错误 | 是 | 无错误 | 是 |
| test@test | “请输入电子邮件地址” | 否 | 无错误 | 是 |

## `input type="tel"`

与新的 `search` 输入类型类似，`tel` 输入类型呈现为一个普通的文本字段（见图 5.2）。它接受此字段中的任何字符，而不仅仅是数字，因为电话号码可以包含非数字字符，如 `+` 或 `(`。如果你想强制字段仅接受数字，那么可以使用 `pattern`，这将在本章后面描述。

**表 5.3 `tel` 输入类型的设备和浏览器支持**

| 浏览器 | 版本 |
|---|---|
| Android | 2.3+* |
| Chrome | 10.0+ |
| Firefox | 4.0+ |
| Internet Explorer | 9.0+* |
| iOS Safari | 4.0+* |
| Opera | 10.0+ |
| Safari | 5.0+* |

\* 无验证

图 5.2 Opera 中的 `input type="tel"` 元素。它看起来像一个普通的输入文本字段。

## `input type="url"`

网页表单上的一个常见需求，比如博客上的评论表单，是要求用户提供他们自己网站的 URL。在 HTML5 中，现在请求 URL 变得非常简单，如清单 5.4 所示。

### 清单 5.4 url 输入类型

```
<label for="url">Website</label><input required type="url" id="url" name="url" />
```

**表 5.4 `url` 输入类型的设备和浏览器支持**

| 浏览器/设备 | 版本 |
|---|---|
| Android | 2.3+* |
| Chrome | 10.0+ |
| Firefox | 4.0+ |
| Internet Explorer | 9.0+* |
| iOS Safari | 4.0+* |
| Opera | 10.0+ |
| Safari | 5.0+* |

\* 无验证

此输入类型期望内容是有效的 URL。同样，与 `email` 类型一样，它不会检查该 URL 是否实际存在（你可以用一些额外的脚本来做到这一点）。传统的 URL 是一个网址，例如 `http://mysite.com`。Firefox 4.0b7 不允许 `mysite.com` 或 `www.mysite.com`；它要求地址包含 `http://`。然而，Opera 11 会自动将 `mysite.com` 转换为 `http://mysite.com`，这是有效的，并允许表单提交。

大多数时候，此字段的内容将是 `http://mysite.com`；但是，它也接受其他类型的 URL：

- `ftp://user:password@server`
- `javascript:window.alert`（小心这个；你可能想编写自己的验证以不允许提交任何 JavaScript）
- `file://server/path`
- `tel:12345`

由于这些额外的 URL 类型，目前表单将以 `hello:world` 验证通过。这是因为大多数浏览器都有自己 URL 类型，比如 Firefox 有 `about:config`。所以，目前，任何包含冒号的 URL 将被验证。随着浏览器完善其验证方法，这在将来可能会发生变化。

## 初学者教程：使用 `input type="search"` 创建搜索表单

`input type="search"` 期望一个搜索词。它看起来像一个普通的文本字段，因为本质上它就是一个普通的文本字段。它并没有什么特别之处，但它有助于浏览器识别这是一个搜索字段。清单 5.5 展示了如何在搜索控件中使用它。

**清单 5.5 search 输入类型**

```
<form role="search">
  <label for="search">搜索词</label>
  <input required type="search" id="search" name="search" />
  <input type="submit" value="搜索" />
</form>
```

**表 5.5 `search` 输入类型设备与浏览器支持**

| Android | 2.3+ |
| :--- | :--- |
| Chrome | 10.0+ |
| Firefox | 4.0+ |
| Internet Explorer | 9.0+ |
| iOS Safari | 4.0+ |
| Opera | 10.0+ |
| Safari | 5.0+ |

WebKit 浏览器（如 Safari 和 Chrome）的一个有趣补充是，你可以添加 `results` 属性，它提供了一些额外功能：

```
<label for="search">搜索词</label>
<input required type="search" results="5" id="search" name="search" />
```

这段代码生成了如图 5.3 所示的搜索项。请注意，`input` 上添加了一个放大镜图标，如果有搜索历史，它会显示以前的搜索词。遗憾的是，目前你还无法使用 CSS 或 JavaScript 来设置这些结果的样式。

第 5 章 HTML5 Web 表单

![](img/de30ea99ecac39b49e690a84c48f43b9_132_0.png)

**图 5.3 带有 WebKit 浏览器特定细节和信息的 `input type="search"` 元素**

Safari 目前会接管搜索输入的设计，但你可以在 CSS 中使用 `-webkit-appearance: none` 来覆盖它。

## 初学者教程：创建日历和时间控件

Web 开发人员需要处理的一个常见问题是如何创建日历小部件，让用户从日历中选择日期，而无需手动输入日期。创建这样一个小部件以前总是需要 JavaScript，但这种情况即将改变。在本教程中，你将了解用于创建不同日历控件的各种新输入类型。对于不提供日历小部件的浏览器，请参考第 3 章，我们在那里提供了一些备用解决方案。

**表 5.6 `datetime` 输入类型设备与浏览器支持**

| Android | * |
| :--- | :--- |
| Chrome | * |
| Firefox | * |
| Internet Explorer | * |
| iOS Safari | 5.0+ |
| Opera | 10.0+ |
| Safari | * |

\* 无日历小部件，但提供文本输入备用方案

```
input type="datetime"
```

肯定会受到用户喜爱的是新的 `datetime` 输入类型。一些主要浏览器厂商将如何处理这种输入类型还有待观察，但 Opera 原生生成了一个出色的日历/日期选择器小部件，如图 5.4 所示。

以前，你需要使用 JavaScript 来提供如此复杂的控件。因为现在浏览器可以处理这个，所以它可以与其他服务集成，例如连接到你的 Facebook 活动日历或 Outlook 日历。

![](img/de30ea99ecac39b49e690a84c48f43b9_133_0.png)

**图 5.4 Opera 11 中的 `input type="datetime"` 元素为用户提供了一个日历日期选择器。**

此外，因为是浏览器处理日历，如果你的系统设置为其他语言，它将显示该语言（例如，意大利语中的 Novembre），不像，例如，jQuery datepicker (`http://docs.jquery.com/UI/Datepicker`)。

```
input type="datetime-local"
```

与之前的 `datetime` 输入几乎相同，`datetime-local` 生成的日历有一个细微差别：右侧没有 "UTC" 标签，因此没有附带时区（参见图 5.5）。

```
input type="date"
```

图 5.6 显示 `date` 输入类型类似于图 5.4 中显示的 `datetime` 输入类型，但这里的控件不显示时间选项。

![](img/de30ea99ecac39b49e690a84c48f43b9_133_1.png)

**图 5.5 Opera 11 中显示的 `input type="time"` 元素**

![](img/de30ea99ecac39b49e690a84c48f43b9_133_2.png)

**图 5.6 Opera 10.63 中显示的 `input type="date"` 元素**

104 第 5 章 HTML5 Web 表单

![](img/de30ea99ecac39b49e690a84c48f43b9_134_0.png)

**图 5.7 Opera 10.63 中显示的 `input type="time"` 元素**

```
input type="time"
```

`time` 输入类型允许用户以 24 小时格式输入时间。目前，只有 Opera 支持此元素。图 5.7 显示了此输入在 Opera 中的外观。在此输入中，用户可以自行键入数字，如 `22:11`，也可以使用 Opera 提供的按钮来滚动选择时间。

```
input type="month"
```

`month` 输入类型显示如图 5.4 所示的日历，但只允许选择月份。输入的值为 `YYYY-MM`。在图 5.8 中，可以选中十二月。你也可以选择上个月或下个月。

```
input type="week"
```

与 `date` 和 `month` 输入类型非常相似，`week` 允许用户选择一年中的某一周。输入的值为 `YYYY-W00`。在图 5.9 中，可以选择该周，并在左列提供周数。

### 对日期和时间进行限制

有两个新属性 `min` 和 `max`，我们将在本章后面再次提到；它们可用于控制和限制小部件的日期或时间。对于日期，如果你想确保用户不能选择过去的日期，可以添加一个 `min` 属性值，格式如下：`YYYY-MM-DD`。`max` 属性值格式相同，用于阻止用户选择过于遥远的未来日期。对于 `time` 输入类型，格式为 `HH:MM`。

![](img/de30ea99ecac39b49e690a84c48f43b9_134_1.png)

**图 5.8 Opera 10.63 中显示的 `input type="month"` 元素**

初学者教程：创建数字选择器

![](img/de30ea99ecac39b49e690a84c48f43b9_135_0.png)

**图 5.9 Opera 10.63 中显示的 `input type="week"` 元素**

## 初学者教程：创建数字选择器

`number` 输入类型用于输入数字。它只接受数字；否则，它将返回验证错误。它允许 `min`、`max` 和 `step` 属性，因此你可以根据需要限制数字范围。`step` 属性允许你指定可输入的增量值。

**表 5.7 数字选择器设备与浏览器支持**

| Android | * |
| :--- | :--- |
| Chrome | 11.0+ |
| Firefox | * |
| Internet Explorer | * |
| iOS Safari | * |
| Opera | 10.0+ |
| Safari | 5.1 |

\* 无数字选择器，但提供文本输入备用方案



使用清单 5.6 中的代码，Opera 创建了一个允许用户循环浏览数字的控件（参见图 5.10）。数字可以是负数，除非你指定了最小值或最大值，否则数字可以无限大。使用`step`属性，你可以更精确地控制数字。图 5.10 允许用户以 0.5 为步长，在 0 到 10（`min`和`max`）之间选择数字。因此，他们可以选择 0、0.5、1、1.5，依此类推。用户可以使用提供的控件，也可以直接键入数字。

www.it-ebooks.info

# 第 5 章 HTML5 Web 表单

![](img/de30ea99ecac39b49e690a84c48f43b9_136_0.png)

**图 5.10 Opera 11 中显示的`input type="number"`元素**

![](img/de30ea99ecac39b49e690a84c48f43b9_136_1.png)

**图 5.11 带有无效数字的`input type="number"`元素（在此示例中只允许 0.5 或整数）**

**清单 5.6 带有步长的`number`输入类型**

```
<input min="0" max="10" step="0.5" required type="number" id="number" name="number" />
```

因为你指定了`step`范围，超出此范围的任何输入都将导致验证错误。因此，在图 5.11 中输入 9.99 是不允许的。

## 初学者教程：创建滑块（无需 JavaScript）

`range`输入类型生成一个滑块控件。它没有可供用户输入的文本区域，并且像`number`输入类型一样，它可以使用`min`、`max`和`step`属性。

**表 5.8 滑块设备与浏览器支持**

| 设备 / 浏览器 | 支持情况 |
| :--- | :---: |
| Android | * |
| Chrome | 10+ |
| Firefox | * |
| Internet Explorer | * |
| iOS Safari | 5.0+ |
| Opera | 10.0+ |
| Safari | 5.0+ |

\* 无滑块，但提供文本输入备用方案

`range`输入类型的一些可能用途可以是页面或表单上的“评价我的*某物*”部分，或者可以用来控制视频或音频播放器的音量。

www.it-ebooks.info

## 5.7 范围输入类型

在清单 5.7 中，我们将看到创建一个基本*范围*输入所需的 HTML，尽管在后续章节中你将学习如何使其成为功能性的音量控制。

**清单 5.7 范围输入类型**

```
<label for="range">音量</label>
<input min="0" max="10" step="0.5" required type="range" id="range" name="range" />
```

我们对滑块外观的控制有限，因为目前控件是特定于浏览器的。但是，你可以为范围控件指定高度和宽度。如果指定的高度大于宽度，音量控件将垂直渲染，而不是其默认的水平布局。

在撰写本文时，Opera、Chrome 和 Safari 支持此输入类型，如图 5.12 所示。主要区别在于 Opera 默认显示增量。

## 新手指南：创建颜色选择器

如图 5.13 所示，`<input type="color">`为用户提供了一些基本颜色的选择，并允许输入十六进制值（#12ff00）或使用颜色选择器，类似于许多软件包中使用的。目前唯一支持此有用输入类型的桌面浏览器是 Opera 11（尽管新的 BlackBerry 浏览器也支持颜色选择器）。

### 表 5.9 颜色选择器设备和浏览器支持

| 设备/浏览器 | 支持情况 |
| :--- | :--- |
| Android | * |
| Chrome | * |
| Firefox | * |
| Internet Explorer | * |
| iOS Safari | * |
| Opera | 10.0+ |
| Safari | * |

\* 不提供颜色选择器，但提供文本输入回退方案

## 新手指南：使用`output`元素显示结果

`output`元素使用 JavaScript 来显示结果，通常来自计算或脚本。它可以用作计算器，或者使用清单 5.6 中的代码，为页面添加一些额外功能，例如显示用户的名。如果不需要在其中显示任何额外内容，它可以是一个自结束标签，因此你可以选择`<output/>`或`<output></output>`。

### 表 5.10 `output`元素设备和浏览器支持

| Android | - |
| --- | --- |
| Chrome | 10.0 |
| Firefox | 4.0 |
| Internet Explorer | - |
| iOS Safari | 4.0 |
| Opera | 10.0+ |
| Safari | 5.0 |

例如，如图 5.14 所示，可以在拖动滑块时显示范围输入类型的值。默认值为空，但当用户移动滑块时，输出值会更改并实时显示给用户。清单 5.8 包含此功能的代码。

### 清单 5.8 `output`元素

```
<label for="range">音量</label><input min="0" max="10" step="0.5" value="2" required type="range" id="range" name="range" />
<output onforminput="value=range.value"></output>
```

## 新手指南：使用表单占位符文本

如前所述，有许多新的输入类型供你尝试，但你也可以在新输入类型旁边使用许多新属性来改进表单。

占位符文本是表单加载时显示在文本字段内的文本。当用户点击或切换到该字段时，它会消失。通常，它提供有关在字段中输入什么的提示，或建议应输入的格式类型。例如，一个搜索表单显示“搜索此站点”，或者如你所见的 url 输入类型，提示用户以 http:// 开头输入 URL。图 5.15 显示了一个示例。

以前，这需要 JavaScript 来实现此效果，但现在你可以坐下来让浏览器为你完成。

`placeholder`文本存在可访问性问题，因为目前文本颜色默认为浅灰色，与默认背景颜色的对比度不足。你可以在 Mozilla 和 WebKit 浏览器中使用以下 CSS 覆盖文本颜色：

```
input::-webkit-input-placeholder {color: red;}
input:-moz-placeholder {color: red;}
```

### 表 5.11 `placeholder`属性设备和浏览器支持

| Android | 2.2 |
| Chrome | 9.0+ |
| Firefox | 4.0+ |
| Internet Explorer | - |
| iOS Safari | 4.0+ |
| Opera | 10.0+ |
| Safari | 4.0+ |

## 新手指南：使用`list`和`datalist`创建自动完成功能

`datalist`是 HTML5 中的新元素。与`list`属性结合使用，它用于提供预定义的选项列表（参见图 5.16），使创建列表的过程看起来像自动完成表单。用户不必从预定义选项中选择；如果他们愿意，可以输入自己的答案。

### 表 5.12 `datalist`元素设备和浏览器支持

| Android | * |
| Chrome | * |
| Firefox | 4.0+ |
| Internet Explorer | * |
| iOS Safari | * |
| Opera | 10.0+ |
| Safari | * |

\* 不提供下拉列表，但提供文本输入回退方案

`datalist`的代码（显示在清单 5.9 中）类似于`select`元素。但是，对于`select`元素，用户如果需要输入自己的选项则无法做到。`datalist`不存在此问题。使用`list`属性，你可以关联一个普通输入（也可以是 url、email、search 或 tel 类型）。

### 清单 5.9 datalist 示例

```
<label for="sport">你最喜欢的运动是什么？</label>
<input list="sportlist" type="text" id="sport" name="sport" />
<datalist id="sportlist">
  <option label="棒球" value="棒球" />
  <option label="足球（英式）" value="足球" />
  <option label="橄榄球" value="橄榄球" />
  <option label="冰球" value="冰球" />
</datalist>
```

在上一个示例中，有四个自动完成选项。目前只有 Firefox 和 Opera 显示自动完成选项，而且它们的做法略有不同：Firefox 仅显示与已输入内容相似的选项，而 Opera 在字段处于活动状态时显示整个列表。

`datalist`可以从数据库或 Ajax 调用生成（类似于 Google 搜索引擎的自动完成功能），为用户提供，比如说，该问题的前 10 个常见答案。这个新元素和属性的妙处在于，如果用户使用的是不渲染此 HTML5 元素的浏览器，没有 JavaScript，或者存在 Ajax 连接问题，表单控件将像普通文本框一样渲染，用户可以正常输入。

## 新手指南：使用`progress`元素跟踪任务进度

新的进度元素用于跟踪任务的状态和完成情况。它可以用于显示下载的进度，例如下载文件或从 Ajax 调用加载数据。

进度元素有两个可选属性：

- **value**：`value`属性表示任务（以百分比计）已完成的量。
- **max**：`max`属性表示完成任务所需的总量。`value`和`max`内容都应显示在进度元素内，以便用户获得完成状态的反馈。

在 Chrome 中，以下代码会给你如图 5.17 所示的进度元素。进度条还会发光，这是一个很好的点缀。

```
<p>您正在下载一个非常重要的文件，请稍候。</p>
<progress value="45" max="100"><span>45</span>% 完成</progress>
```

在不支持`progress`元素的浏览器中，你会得到如图 5.18 所示的结果（来自 Firefox 3.6 的截图）。其背后的思路是，绿色（或蓝色，取决于操作系统和浏览器版本）的条形，或文本视觉效果，会实时更新，以便用户知道已过去多少时间以及还剩多少时间。

### 表 5.13 `progress`元素设备和浏览器支持

| Android | * |
| Chrome | 13+ |
| Firefox | * |
| Internet Explorer | * |
| iOS Safari | * |
| Opera | 11.0+ |
| Safari | * |

\* 不提供样式化的条形，但提供文本回退方案

## 新手指南：使用`meter`元素进行测量

`meter`元素用于显示测量值，例如温度，或显示分数值。

它具有六种可能的属性：

- `min`：允许的最小值。如果没有`min`属性，则值默认为零。你可以根据需要使用负数。
- `max`：允许的最大值。
- `value`：这是实际值，使用`meter`时必须存在。
- `low`：这是值的低部分。
- `high`：这是值范围的高部分。
- `optimum`：这是最佳值。其值必须介于`min`和`max`之间。然而，其`value`可以大于`high`属性的值。

以下是一些基本示例：

```
<p>Your score is: <meter value="2">2 out of 10</meter></p>
<p>Your score is: <meter value="91" min="0" max="100" low="40" high="90"
    optimum="100">A+</meter></p>
```

`meter`元素（如图 5.19 所示）可用于描述硬盘空间的当前状态：

```
<meter min="0" value="512" max="1024">You are using exactly 50% of your hard drive
    space</meter>
```

### 表 5.14 `meter`元素设备与浏览器支持情况

| Android | * |
| Chrome | 13+ |
| Firefox | * |
| Internet Explorer | * |
| iOS Safari | * |
| Opera | 11.0+ |
| Safari | * |

\* 无样式化进度条，但提供文本回退

![](img/de30ea99ecac39b49e690a84c48f43b9_143_0.png)

**图 5.19 Chrome 中的`meter`元素**

# 第 5 章 HTML5 Web 表单

## 入门技巧：页面加载时跳转到表单元素

`autofocus`属性让你有机会在页面加载时聚焦一个表单控件。如果聚焦在一个`input`或`textarea`上，用户就可以在页面加载后立即开始输入。如果你自动聚焦的字段有占位符文本，那么它将被清空，因为文本光标在该字段内。以前，你必须使用 JavaScript 来执行自动聚焦任务。`autofocus`布尔属性，所以它要么开启，要么关闭。图 5.20 展示了一个示例。

### 表 5.15 `autofocus`属性设备与浏览器支持情况

| Android | - |
| Chrome | 9.0+ |
| Firefox | 4.0+ |
| Internet Explorer | - |
| iOS Safari | - |
| Opera | 10.0+ |
| Safari | 5.0+ |

`autofocus`属性应谨慎使用。自动让页面跳转/滚动到内容区域并非最佳的用户体验实践，因为使用移动设备、屏幕阅读器或低分辨率屏幕的用户可能会错过其上方可能相关的内容。建议仅在`form`元素是主要内容的页面上使用`autofocus`，例如联系页面或如图 5.17 所示的搜索站点（如 Google.com 上的表单，它实际上通过 JavaScript 实现了自动聚焦）。代码清单 5.10 展示了用于生成图 5.17 的代码。

**清单 5.10 搜索输入类型上的 autofocus**

```
<label for="autofocus">Search the site</label>
<input autofocus required type="search" id="autofocus" name="autofocus" />
```

![](img/de30ea99ecac39b49e690a84c48f43b9_144_0.png)

> **注意**

`autofocus`在每个页面上应仅使用一次。有趣的是，如果你在页面上有多个字段都设置了`autofocus`，Opera、Chrome 和 Safari 会将自动聚焦放在最后一个字段，而 Firefox 则使用第一个。

## 入门技巧：允许多个条目

`multiple`属性允许用户在特定字段中输入多个值。它可以用于任何 input 类型，因此可以用来创建“发送给朋友”表单或电子邮件应用程序，允许用户在收件人、抄送和密送字段中输入多个电子邮件地址。

### 表 5.16 `multiple`属性设备与浏览器支持情况

| Android | - |
| Chrome | 10.0+ |
| Firefox | 4.0+ |
| Internet Explorer | - |
| iOS Safari | - |
| Opera | 11.0+ |
| Safari | 5.0+ |

上传多个文件是另一个例子。以前，这需要 JavaScript 或服务器端代码来检测何时选择了文件，然后显示另一个上传选项。但现在使用代码清单 5.11 中的代码，你可以在 HTML5 中完成。

**清单 5.11 允许多个文件上传**

```
<label for="upload">Upload some files</label>
<input multiple type="file" id="upload" name="upload" />
```

目前，只有 Firefox 4、Safari 和 Chrome 支持这个新属性。Safari 和 Chrome 会显示所选文件的数量。在图 5.21 所示的示例中，选择了三个文件。Firefox 4 不会自动显示已选择的文件数量；相反，它会在一个文本框内列出完整的文件路径，用逗号分隔，类似“C:\fileone.doc, C:\filetwo.pdf.”

# 第 5 章 HTML5 Web 表单

![](img/de30ea99ecac39b49e690a84c48f43b9_146_0.png)

**图 5.21 Safari 中在文件输入上使用`multiple`属性**

## 入门技巧：使用`required`属性进行基本验证

`required`属性在本章的许多示例中都已使用过。如果使用了该属性，浏览器在必填字段为空时将不会尝试提交表单。在支持此属性的浏览器中，如果必填字段为空，将显示错误，如图 5.22 所示。

### 表 5.17 `required`属性设备与浏览器支持情况

| Android | - |
| Chrome | 10.0+ |
| Firefox | 4.0+ |
| Internet Explorer | - |
| iOS Safari | - |
| Opera | 11.0+ |
| Safari | 5.0+ |

> **提示**



除了`required`属性外，你还可以添加`aria-required="true"`，如下所示，这将提高表单元素的可访问性。你可能会有兴趣知道，WordPress 默认为其评论表单使用了这个属性。

```
<input aria-required="true" required type="text" id="name" name="name" />
```

![](img/de30ea99ecac39b49e690a84c48f43b9_146_1.png)

图 5.22 Opera 11 中不完整必填字段的错误消息

www.it-ebooks.info

## 中级技巧：编写你自己的验证规则

尽管 HTML5 具有内置验证，你仍可以使用`pattern`属性和正则表达式设置自己的规则。

表 5.18 `pattern`属性设备与浏览器支持情况

| 浏览器 | 支持情况 |
| --- | --- |
| Android | - |
| Chrome | 10.0+ |
| Firefox | 4.0+ |
| Internet Explorer | - |
| iOS Safari | - |
| Opera | 11.0+ |
| Safari | - |

例如，你已经看到`url`输入类型接受各种类型的 URL。你可能想阻止这种情况，并强制用户以`http://`开头。你可以使用自定义正则表达式来做到这一点。

代码清单 5.12 中使用的正则表达式仅验证以`http://`或`https://`开头的 URL。它还接受子域名和查询字符串，因此`http://you.site.com/search.aspx?=test`是有效内容，但`mailto:`地址则无效。

```
Listing 5.12 pattern Attribute with Regular Expression
<input required pattern="(http|https)://([\w-]+\.)+[\w-]+(/[\w-./?%&=]*)?"
 type="text" id="url" name="url" />
```

正则表达式可能很棘手，并且会迅速变得复杂，因此根据你的自信程度，最好尽可能保持简单。如果你遇到困难，互联网上有无数的答案。

## 入门技巧：限制用户输入

HTML5 中的表单条目现在可以通过各种属性进行限制（如果适用）。

### `step`

`step`属性可用于`number`、`range`和`time`输入类型。它指定了`input`可取数值的增量步长。请参阅本章前面的代码清单 5.10（带有`number`输入类型）作为示例。

表 5.19 `step`属性设备与浏览器支持情况

| 设备/浏览器 | 支持情况 |
| --- | --- |
| Android | - |
| Chrome | 10.0+ |
| Firefox | - |
| Internet Explorer | - |
| iOS Safari | - |
| Opera | 11.0+ |
| Safari | 5.1 |

### `min`、`max`

如`meter`元素以及`number`和`range`输入类型上所示，`min`和`max`属性设置了元素上允许的值范围。这些不是必需属性，你可以只使用`min`或`max`，或者两者都用。这些设置了验证规则，如果`min`或`max`值不在范围内，表单将不会提交。这些可用于`date`和`time`输入类型，以限制用户选择某个值，例如在活动日历上或在日期之间搜索时。

表 5.20 `min`、`max`属性设备与浏览器支持情况

| 设备/浏览器 | 支持情况 |
| --- | --- |
| Android | - |
| Chrome | 10.0+ |
| Firefox | - |
| Internet Explorer | - |
| iOS Safari | - |
| Opera | 11.0+ |
| Safari | 5.1 |

## `formnovalidate`、`novalidate`

如果你有一个表单，但不想使用浏览器验证，那么可以使用`formnovalidate`或`novalidate`属性。如果你希望保存表单的当前状态而不是提交，例如，如果网站有一个大型表单，或者在流程的当前阶段，因为用户在最终提交前还有其他阶段要完成，你并不关心数据验证，那么使用其中一个属性可能会特别有用。

表 5.21 `formnovalidate`、`novalidate`属性设备与浏览器支持

| 设备/浏览器 | 支持情况 |
| :--- | :--- |
| Android | - |
| Chrome | 10.0+ |
| Firefox | 5.0+ |
| Internet Explorer | - |
| iOS Safari | - |
| Opera | 11.0+ |
| Safari | - |

你可以在`form`元素上放置`novalidate`，这样当表单被提交时，表单将忽略任何格式不正确或为空的字段：

```
<form novalidate>
```

你也可以在任何单独的表单元素上放置`formnovalidate`属性。例如，你可以将其放在`url`输入类型上，浏览器将忽略对此元素的验证（尽管费这么大劲使用`url`输入类型然后又忽略验证，这一点很值得商榷）。

## 中级技巧：自定义和设置表单样式

设计师们最先问的问题之一是，“我能为新元素设置样式吗？” 嗯，算是可以吧。虽然你不能改变日期选择器的外观，因为它是由浏览器生成的（这在未来*可能*会改变），但你可以设置`input`框的外观样式，例如边框、字体和背景颜色，因为你可以利用 CSS3 技巧来设置 HTML5 字段不同状态的样式。

清单 5.13 中的代码生成了你在图 5.23 中看到的内容；请注意不同的字段状态。这些字段最初是橙色的，并带有一个星号图像，因为它们是必填的。

![](img/de30ea99ecac39b49e690a84c48f43b9_150_0.png)

图 5.23 使用 CSS3 针对表单字段的不同状态

当字段处于活动状态但为空或包含无效内容时，方框会变红并显示错误图像。如果内容有效，则字段会变为绿色并显示对勾图像。所有这一切都不需要 JavaScript！

清单 5.13 用于表单元素的新 CSS3 选项

```
<style>
* {margin: 0; font: 13px tahoma, verdana, sans-serif; padding: 0;}
form {padding-top: 10px; width: 310px;}
li {clear: both; list-style-type: none; margin: 0 0 10px;}
label {display: block; float: left; margin: 0 10px 0 0; padding: 5px; text-align: right; width: 100px}
input {background-position: 3px 5px; background-repeat: no-repeat; border-radius: 5px; padding: 5px 5px 5px 25px; width: 155px;}
input:focus {outline: none;}
input:invalid:required {background-image: url(asterisk.png); box-shadow: 0px 0px 5px #f0bb18; border: 2px solid #f0bb18;}
input:focus:invalid {background-image: url(invalid.png); box-shadow: 0px 0px 5px #b01212; border: 2px solid #b01212;}
input:valid {background-image: url(accept.png); border: 2px solid #7ab526;}
input[type=submit] {background: #7ab526; border: none; box-shadow: 0px 0px 5px #7ab526; color: #fff; cursor: pointer; float: right; font-weight: bold; padding-left: 5px; width: auto;}
</style>
<ol>
    <li><label for="tel">电话：</label><input placeholder="例如: 012345" required type="tel" id="tel" name="tel" /></li>
    <li><label for="website">网站：</label><input required type="url" id="website" name="website" /></li>
    <li><label for="email">邮箱：</label><input required type="email" id="email" name="email" /></li>
    <li><input type="submit" value="提交表单" /></li>
</ol>
```

我们将不会涵盖所有新的 CSS 选项，但在图 5.20 中，我们使用了 CSS3 基本用户界面模块 (www.w3.org/TR/css3-ui) 中的以下伪类：

- `:valid`：当表单元素的内容根据元素类型和验证规则有效时，该元素会接收此伪类。
- `:invalid`：如果表单元素的内容不正确，则会应用`:invalid`伪类。
- `:required`：任何具有`required`属性的表单元素都会被分配`:required`伪类。

### 错误消息

我们希望你一直在跟踪前面的示例，并注意到错误消息在 Opera 和 Firefox 中的显示方式不同。Opera 显示一个摇晃的红色错误消息，而 Firefox 显示一个更平静的黄色错误消息。目前，你无法更改这些错误的显示方式，因为它们是由浏览器生成的。这在未来可能会改变，因为目前正在讨论是否可以通过 CSS 使其可编辑。所以，尽管你可能会抱怨错误消息看起来很丑陋或不符合你可爱的品牌准则，但这些错误消息在同一个浏览器内是一致的，因此可以说在可用性上是成功的，因为用户会期望在使用他们选择的浏览器时看到这些错误样式。

虽然你目前还不能改变错误的样式，但你可以使用 JavaScript 和`setCustomValidity()`方法来更改错误消息文本。清单 5.14 提供了一个示例，当添加了不正确的内容时，它会覆盖默认的错误消息。

清单 5.14 一个 HTML5 注册表单

```
<form>
<label for="email">邮箱</label><input oninput="check()" type="email" id="email"
name="email" />
<input type="submit"/>
</form>
<script>
function check() {
    var emailInput = document.getElementById("email");
    emailInput.setCustomValidity("这不是一个有效的邮箱地址。请修正它。");
}
</script>
```

## 高级技巧：将一切整合起来制作一个注册表单

既然你已经了解了所有新的 HTML5 表单功能，让我们将其中几个与一些 CSS 结合起来，看看这些新功能如何创建一个注册表单。清单 5.15 中的 HTML 和 CSS 提供了图 5.24 中的结果。

# 注册使用我们神奇的产品。它真的很神奇。

![](img/de30ea99ecac39b49e690a84c48f43b9_152_0.png)

**个性化你的个人资料**

选择页面颜色

![](img/de30ea99ecac39b49e690a84c48f43b9_152_1.png)

最后，从 1 到 10，你对 HTML5 表单有多兴奋？

![](img/de30ea99ecac39b49e690a84c48f43b9_152_2.png)

5.5 / 10

![](img/de30ea99ecac39b49e690a84c48f43b9_152_3.png)

图 5.24 在 Opera 11 中使用一些 HTML 4 元素、新的 HTML5 表单元素和 CSS 创建的注册表单

因此，在图 5.24 中，我们使用了`tel`、`date`、`url`、`number`、`text`、`email`、`color`和`range`输入类型。在几个地方还使用了`datalist`元素，虽然我们本可以使用`select`，但在这个表单中，我们希望人们输入他们的职位或国家/地区。在表单的末尾，使用了`range`输入类型以及与之配套的`output`元素。所有包含我们需要捕获数据的元素都具有`required`属性，这将触发浏览器内置的验证。为了使其看起来更漂亮，我们添加了一些新的 CSS3 选择器来针对元素的`:required`、`:valid`和`:invalid`状态。

## 清单 5.15 一个功能完备的注册表单



```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>大型注册表单</title>
<style>
* {margin: 0; padding: 0;}
body {background: #fff; color: #000; font: normal 62.5%/1.5 tahoma, verdana, sans-serif;}
h1 {font-size: 2.9em; font-weight: bold; margin: 1em 0 1em 10px;}
form {padding: 0 10px; width: 700px;}
legend {left: -9999px; position: absolute;}
fieldset {border: 1px solid #ccc; border-radius: 5px; float: left; padding: 10px; width: 320px;}
fieldset:nth-of-type(1) {margin-right: 10px;}
li {clear: both; list-style-type: none; margin: 0 0 10px;}
label, input {font-size: 1.3em;}
label {display: block; padding: 0 0 5px; width: 200px}
input {background-position: 295px 5px; background-repeat: no-repeat; border: 2px solid #ccc; border-radius: 5px;  padding: 5px 25px 5px 5px; width: 285px;}
input:focus {outline: none;}
input:invalid:required {background-image: url(asterisk.png); box-shadow: none;}
input:focus:invalid {background-image: url(invalid.png); box-shadow: 0px 0px 5px #b01212; border: 2px solid #b01212;}
input:valid:required {background-image: url(accept.png); border: 2px solid #7ab526;}
input[type=date], input[type=number] {background-position: 275px 5px; text-align: left;}
input[type=color], input[type=range] {padding-right: 5px;}
input[type=range]:before{content: "1";}
input[type=range]:after{content: "10";}
div#range label {font-weight: bold;}
output {font-size: 1.3em; font-weight: bold; display: block; text-align: center;}
div {clear: both; float: left; margin: 10px 0; text-align: center; width: 100%;}
div label {width: 100%;}
input[type=submit] {background: #7ab526; border: none; box-shadow: 0px 0px 5px #7ab526; color: #fff; cursor: pointer; font-size: 3em; font-weight: bold; margin: 20px auto; padding: 15px; width: auto;}
input[type=submit]:hover {box-shadow: 0px 0px 25px #7ab526; }
</style>
</head>
<body>
<h1>注册使用我们神奇的产品。它真的很神奇。</h1>
<form>
  <fieldset>
    <legend>个人信息</legend>
    <ol>
      <li><label for="name">姓名</label><input autofocus required type="tel" id="name" name="name" /></li>
      <li><label for="birthday">生日</label><input required type="date" id="birthday" name="birthday" /></li>
```

# 第五章 HTML5 网页表单

```html
<li><label for="website">网站</label><input
    placeholder="http://mysite.com" pattern="(http|https)://([\w-]+\.)+[\w-]+(/[\w- ./?%&=]*)?" type="url" id="website" name="website" /></li>
<li><label for="job">职业</label><input list="joblist" required type="text"
    id="job" name="job" />
    <datalist id="joblist">
        <option label="Space Cowboy" value="Space Cowboy">
        <option label="International Playboy" value="International Playboy">
        <option label="Web developer" value="Web developer">
        <option label="Web designer" value="Web designer">
        <option label="Jack of all trades" value="Jack of all trades">
    </datalist>
</li>
<li><label for="salary">年薪（约）</label><input
    placeholder="&#36;" required min="0" step="1000" type="number"
    id="salary" name="salary" /></li>
</ol>
</fieldset>
<fieldset>
<legend>联系信息</legend>
<ol>
    <li><label for="address1">地址行 1</label><input required
        type="text" id="address1" name="address1" /></li>
    <li><label for="address2">地址行 2</label><input required type="text"
        id="address2" name="address2" /></li>
    <li><label for="country">国家</label><input list="countrylist" required
        type="text" id="country" name="country" />
        <datalist id="countrylist">
            <option label="Canada" value="Canada">
            <option label="United Kingdom" value="United Kingdom" >
            <option label="USA" value="USA">
        </datalist>
    </li>
    <li><label for="tel">电话</label><input placeholder="例如：012345" type="tel"
        id="tel" name="tel" /></li>
    <li><label for="email">电子邮件</label><input required type="email" id="email"
        name="email" /></li>
</ol>
</fieldset>
<div id="personalise">
    <h2>个性化您的个人资料</h2>
    <label for="color">选择页面颜色</label>
    <input type="color" id="color" name="color" />
</div>
<div id="range">
    <label for="excited">最后，从1到10分，您对HTML5表单
        有多兴奋？</label>
    <input min="1" max="10" step="0.5" type="range" id="excited" name="excited" />
    <output onforminput="value=excited.value + ' / 10'"></output>
    <input type="submit" value="注册" />
</div>
</form>
</body>
</html>
```

## 总结

本章中，您了解了所有新的输入类型，以及如果它们被完全支持，它们在浏览器中的工作方式。这些新的输入类型，连同新的内置原生验证功能以及优秀浏览器中的新CSS功能，使得创建表单和向用户提供反馈变得容易得多。尽管在所有浏览器都赶上之前还有很长的路要走，但总有一天——理想情况下很快——您将不必依赖JavaScript来创建诸如日期选择器、滑块和验证等有用功能。所有新的输入类型，如`email`、`tel`和`date`，在浏览器中都“能工作”，至少会显示一个文本字段，因此没有理由不开始使用它们。

## 第六章 使用 Canvas 绘图

2004年，苹果公司为 Mac OS X Dashboard 开发了一个名为`canvas`的基于像素的绘图元素，后来被应用于 Safari 浏览器。HTML5 规范采纳了这个元素及其相关的一套API，以提供基本的绘图功能。在`canvas`元素出现之前，浏览器需要第三方插件来渲染这些基本图形。由于这是一种基于像素的绘图机制，而不是基于矢量和图层的系统，因此底层功能较为基础；然而，正如您将在本章学到的，它仍然可以提供一种提供丰富显示的方式。

## Canvas 概览

实现canvas的核心是两个部分：HTML中的`canvas`元素和用于在canvas上执行操作的JavaScript。就像画家一样，canvas在画家使用画笔、工具和介质创作出最终的艺术品之前是一片空白。同样地，您将使用canvas形状工具、效果和变换的运动编程到您的JavaScript中。然后这些被绘制到canvas上，形成更新后的新像素视图。

`canvas`元素为您提供了一个空白表面（因此得名`canvas`），您可以使用它来动态渲染图形、图像和文本。canvas的功能非常强大，因此我们将介绍一些基础知识，如绘制形状，然后介绍一些更复杂的效果和变换。然而，如果您喜欢这类东西，我们鼓励您进行进一步研究，因为我们在这里只是触及了皮毛。在深入探讨canvas的大量用法之前，我们将快速过一遍基础知识。

表 6.1 显示了支持`canvas`元素的每个浏览器的版本。

> **注意**

对于 Internet Explorer 8 及更早版本，您需要一些第三方帮助，这就是 explorercanvas (http://code.google.com/p/explorercanvas) 的用武之地。因为您只需要在 IE8 中使用它，所以可以将其放在条件语句中：

```
<!--[if lte IE 8]><script src="excanvas.js"></script><![endif]-->
```

表 6.1 Canvas 浏览器支持情况

| 浏览器 | 版本 |
| --- | --- |
| Android | 2.1+ |
| Chrome | 10.0+ |
| Firefox | 3.6+ |
| Internet Explorer | 9.0+ |
| iOS Safari | 3.2+ |
| Opera | 10.6+ |
| Safari | 3.2+ |

### 入门

清单 6.1 包含了开始使用`canvas`元素所需的代码。如果您在浏览器中尝试此代码，将看不到任何内容，因为没有添加任何JavaScript来实际在canvas上绘制。验证canvas是否已被浏览器渲染的一种快速方法是使用CSS为元素添加边框。

清单 6.1 设置`canvas`元素

```html
<!DOCTYPE html>
<html>
<head>
<style>
canvas {
    border: 1px solid #000;
}
</style>
</head>
<body>
<canvas id="myCanvas" width="640" height="480"></canvas>
</body>
</html>
```

`canvas`元素具有HTML元素的标准属性。至少，您需要`id`、`width`和`height`属性，以便能够从JavaScript中引用canvas并设置其大小。此外，`canvas`元素可以像任何其他元素一样通过CSS进行样式设置。在清单 6.1 中，应用了一个边框，以便您可以快速验证canvas已放置在页面上并且尺寸正确。您也可以添加背景颜色或其他样式。这些样式默认会在canvas中显示，因为canvas默认是透明的，它会渲染`canvas`元素下方的所有内容。这对于将canvas叠加在其他HTML元素上非常有用，这样您就可以在其上绘制了。

您会注意到在清单 6.1 中，我们在HTML中包含了结束标签`</canvas>`。包含结束标签的原因是为了提供一个后备容器，并完全符合Mozilla的规范，因为该浏览器期望有后备内容。通过拥有一个后备容器，如果浏览器不支持canvas元素，则可以显示标签之间的内容。与其他元素一样，您可以提供 alt 属性来显示文本内容，但如果canvas标签不受支持，则开始和结束元素标签内的任何内容都将被显示。这可以方便地显示从文本到图像的任何内容，因为canvas绘图将不会被显示。

要使用JavaScript在canvas上绘制，您首先必须获取要绘制的canvas的上下文。为此，您的脚本将通过id获取canvas元素，然后使用`getContext`来获取canvas元素二维上下文的引用。此上下文引用提供了更改canvas中像素的链接，如下所示：

```html
<canvas id="mycanvas" width="640" height="480"></canvas>
<script>
  var canvas = document.getElementById('mycanvas').getContext('2d');
</script>
```

`getContext`方法也可用于验证您的JavaScript并确定当前浏览器是否支持canvas绘图。使用canvas元素进行一个简单的检查，如果支持则返回true值，如果不支持则返回false值：

```javascript
var canvas = document.getElementById('mycanvas');
if (mycanvas.getContext) {
  // canvas is supported
  ...
}
```

然后JavaScript可以根据浏览器是否支持canvas功能采取适当的编程路径。

### X 和 Y 坐标

在深入探讨基本canvas绘图工具之前，我们需要讨论的最后一个领域是用于在canvas上绘图的坐标系统。由于canvas是基于像素的，因此使用 (X,Y) 坐标系来确定正在更新的特定位置或像素。这些坐标也与各种工具一起用于引用起点、终点和其他位置。如果您使用过 Adobe Photoshop 等工具，那么使用基于坐标的绘图系统对您来说不会是新鲜事。坐标系统的关键是 (0,0) 点默认位于canvas的左上角，X值向右移动时增加，Y值向下移动时增加。作为对一些绘图工具和canvas网格系统的介绍，本章的第一个配方将为您在canvas上展示此网格。

## 初学者教程：在画布上绘制网格

所有基于canvas元素的绘图基础都是网格系统。然而，就实际应用而言，这个网格系统本身是不可见的。canvas元素利用网格系统来支持基本图形绘制工具、效果和变换。在本教程中，你将使用两种基本图形绘制方法——直线和弧形——在画布上创建网格，并在水平线与垂直线的交汇处绘制小点。通过这个实践，你将理解网格系统在使用这些基础绘图画笔时的重要性。

画布将被定义为宽600像素、高400像素。每隔100像素，我们将绘制一条垂直线和一条水平线，从而形成网格。为了显示交汇点的坐标，本教程将使用canvas的`fillText`效果，该效果允许JavaScript在canvas元素上绘制文本。最终，你应该能得到如图6.1所示的效果。

现在，让我们按照以下步骤，参照代码清单6.2，让这个网格变得可见：

1.  创建一个空白的HTML页面，包含如代码清单6.2所示的`<html>`和`<body>`标签，其中应包括`<canvas>`的开始和结束标签，以及其间的替换文本。

2.  添加包含`canvas` ID样式的`<style>`部分。

3.  添加`window.addEventListener`，以便在页面加载时启动`showGrid`函数，并声明canvas和上下文变量。



### 添加`showGrid`函数

添加`showGrid`函数，以便在画布上绘制线条、点和文本。

**代码清单6.2 绘制画布网格**

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>6.2 Canvas Grid System</title>
<style>
#canvas {
    border: 1px solid #03F;
    background: #CFC;
}
</style>
<script>

// Declare our canvas and context reference variables
var canvas;
var context;

// Lay the grid on to the canvas
function showGrid() {

    // Get references to the canvas and then the drawing context
    canvas = document.getElementById('canvas');
    context = canvas.getContext('2d');

    // Set line width and color for the grid lines
    context.lineWidth = 1;
    context.strokeStyle = '#999';

    // Set the line spacing for the grid lines
    lineSpacing = 100;

    // Initialize the x and y positions
    var xPos = 0;
    var yPos = 0;

    // determine the number of horizontal and vertical lines on the grid
    var numHorizontalLines = parseInt(canvas.height/lineSpacing);
    var numVerticalLines = parseInt(canvas.width/lineSpacing);

    // Draw the horizontal lines
    for (var i=1; i<=numHorizontalLines;i++) {
        yPos = i*lineSpacing;
        context.moveTo(0,yPos);
        context.lineTo(canvas.width,yPos);
        context.stroke();
    }

    // Draw the vertical lines
    for (var i=1; i<=numVerticalLines;i++) {
        xPos = i*lineSpacing;
        context.moveTo(xPos,0);
        context.lineTo(xPos,canvas.height);
        context.stroke();
    }

    // Add circles and coordinates to the grid intersections
    for (var y=0; y<=numHorizontalLines; y++) {
        for (var x=0; x<=numVerticalLines; x++) {

            // calculate the x and y position
            xPos = x*lineSpacing;
            yPos = y*lineSpacing;

            // if at (0,0) then change color
            if (x==0 && y==0) {
                context.fillStyle='#f00';
            } else {
                context.fillStyle='#000';
            }

            // draw circle at point
            context.beginPath();
            // Draws a circle of radius 5 at the x and y position
            context.arc(xPos,yPos,5,0,Math.PI*2,true);
            context.closePath();
            context.fill();

            // Display the text for the coordinate
            // Check if on last vertical and place text on left
            if (x==numVerticalLines) {
                context.textAlign = 'right';
                xPos -= 5;
            } else {
                context.textAlign = 'left';
                xPos += 5;
            }
            // Check if on bottom horizontal and place text above
            if (y==numHorizontalLines) {
                yPos -= 8;
            } else {
                yPos += 12;
            }
            // Add the text to the canvas
            context.fillText('('+x*lineSpacing+','+y*lineSpacing+')',xPos,yPos);
        }
    }
}

// on page load initialize the bar chart
window.addEventListener('load',showGrid,false);

</script>
</head>
<body>
<h1>Canvas Grid System</h1>
<canvas id="canvas" width="600" height="400">
    The Canvas HTML5 element is not supported by your browser.
    Please run this page in a different browser.
</canvas>
</body>
</html>
```

在这里，我们不会过多深入讲解具体的直线、点或文本绘制细节，因为这些图形绘制方法和效果将在本章后面详细描述。关键在于理解当你想在画布上绘图时所发生的处理过程。在本教程中，你已经在HTML中创建了一个宽600像素、高400像素的`canvas`元素。此外，该`canvas`元素被设置了边框和背景色样式。当代码在浏览器中运行时，你会看到这个边框和背景色。由于`canvas`默认是透明的，而代码仅在`canvas`上绘制线条、点和文本，因此背景样式颜色会显现出来。

当页面加载时，`showGrid`函数将被触发。在本教程中，你需要做的第一件事是获取对`canvas`元素的引用，然后获取`canvas`的绘图上下文。一旦你有了上下文，就可以设置一些基本设置，例如使用`context.lineWidth`设置线宽，以及使用`context.strokeStyle`设置要使用的颜色。然后，你将网格线的间距设置为100，设置初始起始坐标为(0,0)，并确定需要绘制的水平线和垂直线的数量。利用这些信息，代码通过每100像素向下移动位置并绘制一条横跨画布的线来绘制所有水平线。在完成水平线后，代码从左到右绘制垂直线，每条线从画布顶部绘制到底部。请记住，对于y轴方向，顶部是0，向下则数值增加。

# 第6章 使用Canvas绘图

网格线绘制完成后，接下来需要添加交汇点及其坐标。要绘制这些点，你将使用弧形工具在每个点绘制一个圆，我们将在本章后面更详细地介绍这个工具。在每个点上，你还需要使用`fillText`方法显示其坐标文本。默认情况下，文本是左对齐和顶部对齐的，这对网格上的大多数点都适用，除了最右侧的列和最底部的行。如果你不改变文本对齐方式就显示这些点，那么文本将不可见，因为它会绘制在上下文中但却在画布可视区域之外。因此，代码会判断该点是否位于最后一列或最后一行，并相应地修改该位置的文本对齐方式。

> 注意

由于`canvas`是基于像素操作的，在二维世界中，你在画布上绘制的顺序非常重要。Canvas API中没有图层的概念，因此你构建绘图的顺序将决定最终成品。例如，如果你在为路牌绘制实心背景之前就将文本添加到画布上，那么你的文本就会被覆盖掉。相反，你应该先绘制路牌背景，然后再在上面绘制文本。

你刚刚完成了你的第一幅`canvas`绘图，同时也学会了网格系统如何与`canvas`上下文配合工作。现在，让我们来看看`canvas`功能的基本绘图形状或方法，以及一些可用的效果。

## Canvas工具

Canvas提供了一套基本工具（如下所示），你可以使用它们在画布上创建各种简单和复杂的图形。在本教程中，你将简要了解这些工具中的每一个，并查看一些快速示例。

- 矩形：在特定位置绘制一个具有特定宽度和高度的矩形
- 线：从点A创建一条线到点B
- 路径：使用一条或多条线或曲线创建一条路径
- 弧形：根据给定尺寸创建一个弧形，也可用于创建圆形
- 曲线：创建两种曲线类型之一：贝塞尔曲线或二次曲线

## 初学者教程：制作简单图形和线条

在本教程中，你将绘制简单的图形，如正方形和三角形，并学习如何绘制线条和路径。

### 绘制和样式化矩形或正方形

使用`fillRect(pos-x, pos-y, width, height)`，你可以绘制矩形或正方形：

```
canvas.fillRect(0, 0, 100, 100);
```

这将创建一个100像素乘以100像素的正方形，并将其放置在画布的左上角（0,0），如图6.2所示。默认情况下，正方形将是黑色的，这相当乏味，所以我们来尝试添加一些颜色。

除了`canvas`提供的基本工具集外，还有一些效果可以与这些工具结合使用：

- 填充：控制形状的填充参数
- 描边：控制形状中使用的线条描边
- 渐变：允许在形状中使用线性或径向填充图案
- 透明度：定义画布上所有形状的不透明度级别，或者通过填充RGBa值为特定形状设置透明度
- 阴影：为单个形状提供易于使用的阴影
- 合成：遮罩或裁剪画布区域，并控制画布上形状构建的整体顺序

你在本章中已经简要看到过其中一些效果的方法。以下是一些可用于形状的更常见效果方法：

- `strokeStyle`：指定形状周围线条的颜色或样式
- `fillStyle`：指定形状内部使用的颜色或样式
- `shadowOffsetX`/`shadowOffsetY`：指定阴影的距离
- `shadowBlur`：指定模糊效果的级别
- `shadowColor`：指定阴影的颜色
- `createLinearGradient`：在形状内创建线性渐变
- `createRadialGradient`：在形状内创建径向渐变

![](img/de30ea99ecac39b49e690a84c48f43b9_165_0.png)

因此，如果你对之前用`fillRect`绘制的正方形使用多种可用效果，你可以得到一个相当迷人的带紫色阴影的紫色正方形（见清单6.3）。对于任何使用颜色的效果，如`strokeStyle`、`fillStyle`和`shadowColor`，你不必使用RGBA格式，也可以使用十六进制值或HSLA。但需要注意的是，所有样式和效果都必须在调用`fillRect`方法之前完成，因为`fillRect`方法会告知`canvas`上下文渲染形状，一旦渲染完成，形状就固定了。由于形状是通过单个像素显示在画布上的，绘制后无法更改形状。相反，你需要重新绘制形状来修改它，正如你将在本章后面学到的。

### 清单6.3 为正方形添加样式

```
<canvas id="canvas" width="640" height="480"></canvas>
<script>
    var canvas = document.getElementById('canvas').getContext('2d');
    canvas.shadowOffsetX = 10;
    canvas.shadowOffsetY = 10;
    canvas.shadowBlur = 10;
    canvas.shadowColor = 'rgba(200, 0, 200, .3)';
    canvas.fillStyle = 'rgba(200, 0, 200, 1)';
    canvas.fillRect(0, 0, 100, 100);
</script>
```

使用可用的颜色代码选项，颜色可以包含不透明度设置，这对于创建分层图像效果非常方便。清单6.3使用了半透明的阴影RGBA值来获得最理想的阴影效果。

绘制矩形还有另外两个方法：`clearRect(pos-x, pos-y, width, height)`和`strokeRect(pos-x, pos-y, width, height)`。`clearRect`方法将清除给定矩形区域内的像素。这将移除该区域内的任何像素更改，将区域恢复到默认的透明状态。正如你将在本章后面学到的，使用`clearRect`方法在动画中非常有用，你可以使用画布的宽度和高度来清除整个画布，或者只清除特定区域。`strokeRect`与`lineWidth`结合使用，将在你设置的坐标、宽度和高度处绘制描边。结合使用这些形状和效果，如清单6.4所示，将创建出更独特的图像。

### 清单6.4 更多样式选项

```
var canvas = document.getElementById('canvas').getContext('2d');
canvas.shadowOffsetX = 10;
canvas.shadowOffsetY = 10;
canvas.shadowBlur = 10;
canvas.shadowColor = 'rgba(200, 0, 200, .3)';
canvas.fillStyle = 'rgba(200, 0, 200, 1)';
canvas.strokeStyle = '#09c';
canvas.lineWidth = 5;
canvas.fillRect(0, 0, 100, 100);
canvas.clearRect(25, 25, 50, 50);
canvas.strokeRect(25, 25, 50, 50);
```

### 为形状应用渐变

你可以与`canvas`形状一起使用的另一个效果是渐变。画布中的渐变填充可以通过线性（`createLinearGradient`）或径向（`createRadialGradient`）渐变创建。要向渐变添加颜色，请使用`addColorStop`属性。清单6.5使用两种渐变类型创建了两个矩形。

### 清单6.5 创建渐变

```
<canvas id="canvas" width="640" height="480"></canvas>
<script>
var canvas = document.getElementById('canvas').getContext('2d');
var grd = canvas.createLinearGradient(0, 200, 200, 0);
grd.addColorStop(0, '#000');
grd.addColorStop(.5, '#ccc');
grd.addColorStop(1, '#000');
canvas.fillStyle = grd;
canvas.strokeStyle = '#09c';
canvas.lineWidth = 5;
canvas.fillRect(0, 0, 200, 200);
canvas.closePath();

var grd = canvas.createRadialGradient(300, 250, 2, 200, 200, 250);
grd.addColorStop(0, '#000'); // 浅蓝色
grd.addColorStop(1, '#ccc'); // 深蓝色
canvas.fillStyle = grd;
canvas.fillRect(200, 200, 200, 200);
canvas.closePath();
</script>
```

清单6.5创建了一个左上角带有线性渐变的矩形和一个右下角带有径向渐变的矩形。两种渐变方法使用不同的参数来控制渐变的行为，如下所示：

```
createLinearGradient(startX, startY, endX, endY)
createRadialGradient(startX, startY, startRadius, endX, endY, endRadius)
```

径向渐变方法可能有点复杂，因此值得尝试一下；尝试添加各种`addColorStop`来看看会发生什么。

# 第6章 使用Canvas绘图

## 绘制线条和路径

要使用`canvas`绘制线条，有三个方法构成了这个过程：

- `moveTo(x,y)`：将画布网格上的当前位置移动到线条的起点；线条将从这里开始绘制。
- `lineTo(x,y)`：告诉`canvas`线条的终点位置。
- `stroke()`：调用以让`canvas`绘制线条。如果尚未使用`strokeStyle`方法设置描边样式，则线条的默认颜色将是黑色。



在清单6.6中，你从左上角10像素处开始线条，并使用`lineTo`将线条终点设置在画布右下角10像素处，如图6.3所示。

### 清单6.6 绘制一条线

```
<canvas id="canvas" width="640" height="480"></canvas>
<script>
  var canvas = document.getElementById('canvas').getContext('2d');
  canvas.moveTo(10,10);
  canvas.lineTo(630, 470);
  canvas.stroke();
</script>
```

请记住，线条的选项（如宽度和颜色）必须在调用`stroke`方法之前设置，以便样式能够正确渲染。

你可以多次使用`lineTo`来绘制各种形状，通过创建线条所走的“路径”来实现。让我们看看在清单6.7中绘制一个三角形，它使用了三次`lineTo`来绘制三角形的三条边。

![](img/de30ea99ecac39b49e690a84c48f43b9_168_0.png)

### 清单6.7 绘制一个三角形

```
<canvas id="canvas" width="640" height="480"></canvas>
<script>
    var canvas = document.getElementById('canvas').getContext('2d');

    canvas.beginPath();
    canvas.moveTo(10,10);
    canvas.lineTo(630, 470); // 对角线
    canvas.lineTo(10, 470); // 底边
    canvas.lineTo(10, 10); // 左边
    canvas.closePath();

    canvas.strokeStyle = '#000';
    canvas.lineWidth = 3;

    canvas.fillStyle = '#ccc';
    canvas.fill();

    canvas.stroke();
</script>
```

要让线条形成一个路径，你需要使用两个新方法：`beginPath`和`closePath`。`beginPath`告诉canvas，之后的线条或曲线属于一个路径对象，当调用`closePath`方法时该路径被“闭合”。线条或曲线的路径随后可以作为一个对象来处理，类似于矩形，然后可以类似地进行样式化。

使用清单6.7中的代码预览形状，你会注意到线条结束的地方（左上角）有点粗糙，因为线条没有平滑地衔接。嗯，有一个方法可以解决这个问题，`lineCap`，它接受`butt`、`round`或`square`值。这将封闭线条的末端，但三角形的其他顶点呢？你可以使用`lineJoin`方法，它接受`bevel`、`miter`或`round`值：

```
canvas.lineCap = 'round';
canvas.lineJoin = 'round';
```

路径可以包含不仅由线条创建的段，还可以由曲线创建，正如你将在后面看到的。

## 中级技巧：使用路径绘制多边形

在这个技巧中，你将使用Canvas API的线条绘制和路径功能，根据用户提供的边数和半径来绘制一个正多边形。因为多边形是通过使用路径特性创建的，所以你可以然后填充

# 第6章 使用Canvas绘图

### 使用路径绘制多边形

要创建多边形，JavaScript将根据数学公式计算顶点坐标，并在多边形的每个顶点之间绘制一条线。可以按照以下步骤并使用清单6.8中的代码来实现此效果：

1. 使用`style`和`body`标签为画布创建清单6.8中的页面。

2. 添加用于输入边数和半径的输入框，以及触发多边形绘制的按钮。

3. 添加`init`函数、全局变量和加载事件处理器，以设置对画布和上下文的全局引用。

4. 添加`drawPolygon`函数，这是绘制实际正多边形的工作函数。

**清单6.8 使用路径绘制多边形**

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>6.8 使用路径绘制多边形</title>
<style>
#canvas {
  border:1px solid #03F;
}
</style>
<script>
// 画布和上下文的全局变量
var canvas;
var context;

// 页面加载时的初始化函数
function init() {

  // 设置按钮处理器
  var btnDrawPolygon = document.getElementById('drawPolygon');
  btnDrawPolygon.addEventListener('click',drawPolygon,false);

  // 设置对画布和上下文的引用
  canvas = document.getElementById('canvas');
  context = canvas.getContext('2d');
}

// 在画布上绘制多边形的函数
function drawPolygon() {

  // 获取用户输入的多边形参数
  var numSides = document.getElementById('numSides').value;
  var radius = document.getElementById('radius').value;

  // 获取画布中心点以将多边形居中
  var xCenter = parseInt(canvas.width/2);
  var yCenter = parseInt(canvas.height/2);

  // 清除画布
  canvas.clearRect(0,0,canvas.width,canvas.height);

  // 开始我们的路径
  context.beginPath();

  // 映射第一个顶点作为起点
  var xPos = xCenter + radius * Math.cos(2 * Math.PI * 0 / numSides);
  var yPos = yCenter + radius * Math.sin(2 * Math.PI * 0 / numSides);
  context.moveTo(xPos,yPos);

  // 循环遍历所有顶点并映射线段
  for (i = 1; i <= numSides; i++) {

      // 确定下一个顶点的坐标
      xPos = xCenter + radius * Math.cos(2 * Math.PI * i / numSides);
      yPos = yCenter + radius * Math.sin(2 * Math.PI * i / numSides);

      // 将线段连接到下一个顶点
      context.lineTo(xPos,yPos);
  }

  // 关闭线段路径
  context.closePath();

  // 设置线段属性并绘制线段
  context.lineWidth = 30;
  context.lineJoin = 'round';
  context.stroke();

  // 填充新创建的多边形
  context.fillStyle = '#00F';
  context.fill();
}

// 在页面加载时调用init函数
window.addEventListener('load',init,false);

</script>
</head>
<body>
    <h1>Canvas路径用法：</h1>
    <canvas id="canvas" width="400" height="400"></canvas>
    您的浏览器不支持canvas元素。
    </canvas>
    <br>
    边数：<input type="number" id="numSides" min="3" step="1" value="7" /><br>
    半径：<input type="number" id="radius" min="10" step="1" value="150" /><br>
    <button id="drawPolygon">绘制多边形</button>
</body>
</html>
```

点击“创建多边形”按钮后，将调用`drawPolygon`函数。首先，该函数获取用户输入的多边形边数和半径。接着，函数找到画布的中心点，以便将多边形放置在画布中央。然后，使用`clearRect`函数清除画布，这样每次用户创建新多边形时都能从空白画布开始。

画布设置完成后，使用`beginPath`方法开始路径绘制。然后，通过一些巧妙的算法，计算起始的X、Y坐标，并使用`lineTo`循环遍历每个顶点以创建线段。当所有线段构建完成后，使用`closePath`方法关闭路径。`closePath`方法将所有线段连接成一个路径，然后使用该路径设置多边形的边线和填充色，最终结果如图6.4所示，多边形被绘制在画布上。

图6.4 通过路径功能创建的五边形，半径为150

### 绘制弧线和圆形

使用Canvas不仅可以绘制直线，还可以添加曲线。从`arc`方法开始，该方法接受以下值：

```
canvas.arc(x, y, radius, startAngle, endAngle, antiClockwise(Boolean));
```

让我们看一下清单6.9中的示例，其结果如图6.5所示。

**清单6.9 绘制弧线**

```html
<canvas id="canvas" width="640" height="480"></canvas>
<script>
  var canvas = document.getElementById('canvas').getContext('2d');
  canvas.arc(100, 100, 40, 5, 1, true);
  canvas.strokeStyle = '#000';
  canvas.lineWidth = 5;
  canvas.stroke();
</script>
```

在清单6.9中，你将`antiClockwise`的值设置为`true`。尝试将其设置为`false`，看看会绘制出什么。

要绘制圆形，请使用`arc()`方法，起始角度为0，结束角度为`2 * Math.PI`：

```
canvas.arc(100, 150, 60, 0, 2 * Math.PI, false);
canvas.fillStyle = '#000';
canvas.fill();
canvas.strokeStyle = '#000';
canvas.lineWidth = 2;
```

### 绘制曲线

Canvas中提供了两种曲线类型：`quadraticCurveTo`和`bezierCurveTo`。两者的区别在于，`quadraticCurveTo`有一个控制点，而`bezierCurveTo`有两个控制点。控制点使你能够在直线中添加曲线，从而创建更复杂的形状：

```
canvas.quadraticCurveTo(cX, cY, endX, endY);
canvas.bezierCurveTo(c1X, c1Y, c2X, c2Y, endX, endY);
```

### 添加文本

Canvas API提供了两种向画布添加文本的方法：`fillText`和`strokeText`。`fillText`接受一个要显示的字符串以及显示文本的X、Y坐标，并将文本字符串创建为填充字母；而`strokeText`方法接受相同的参数，但创建的是文本字符的轮廓：

```
fillText(text, x, y);
```

在这两种情况下，都可以通过`font`属性修改字体类型、粗细和大小，并且可以通过画布的`fillStyle`和`strokeStyle`属性控制填充和描边样式，如清单6.10所示。

**清单6.10 向Canvas添加文本**

```html
<script>
    var canvas = document.getElementById('canvas').getContext('2d');
    canvas.font = 'bold 80px Tahoma';
    canvas.fillStyle = '#000';
    canvas.fillText('HTML5 Canvas', 10, 100);

    canvas.strokeStyle = '#000';
    canvas.lineWidth = 3;
    canvas.fillStyle = '#ccc';
    canvas.textAlign = 'center';
    canvas.fillText('HTML5 Canvas', 320, 200);
    canvas.strokeText('HTML5 Canvas', 320, 200);
</script>
```

清单6.10的结果如图6.6所示。注意，在`fillText`和`strokeText`中，字符串值之后是文本将要绘制的X和Y坐标。另外，在第二个示例中，文本是居中对齐的，并且同时使用了`fillText`和`strokeText`，所以如果你只想要文本轮廓，可以移除`fillText`。

图6.6 在Canvas上绘制的文本

### 绘制图像

Canvas API中一个更有趣的领域是图像的引入。通过`drawImage`方法，你可以包含自己选择的图像，并以多种方式操作图像。清单6.11中的简单示例加载了一个PNG图像文件，显示效果如图6.7所示。

**清单6.11 绘制图像**

```html
<canvas id="canvas" width="640" height="480"></canvas>
<script>
  var canvas = document.getElementById('canvas').getContext('2d');
  var canvasImage = new Image();

  function drawCanvasImage(){
    canvas.drawImage(canvasImage, 155, 0);
  };

  canvasImage.addEventListener('load',drawCanvasImage,false);

  canvasImage.src = 'images/html5-logo.png';
</script>
```

`drawImage`函数有三种不同的格式：

- `drawImage(image, dx, dy)`：在位置x和y处显示提供的image URL中的图像。

- `drawImage(image, dx, dy, dw, dh)`：根据显示宽度（dw）和显示高度（dh）对图像进行缩放。

- `drawImage(image, sx, sy, sw, sh, dx, dy, dw, dh)`：根据提供的（sx、sy、sw和sh）的X、Y坐标和宽高裁剪图像的某个区域。

图6.7 绘制到画布上的图像（HTML5标志归属W3C，www.w3.org）

## 第六章 使用 Canvas 绘图

基础的`drawImage`方法接受图像的URL，然后是显示图像的x和y坐标。图像不会以任何方式缩放或裁剪。在清单6.11中，使用了`load`事件来验证图像在尝试显示到画布之前已经加载完毕。如果你直接将图像URL传入变量，那么将不会显示任何内容，因为图像尚未加载到页面中。因此，为了确认图像在要求画布显示之前已加载，你需要监听图像加载事件。

在图6.4中，你可以看到图像刚好能放入我们的画布框架内；你可以通过使用带有缩放宽度和高度选项的`drawImage`方法来调整图像大小：

```
drawImage(image, x, y, width, height);
```

通过这种方式，脚本传入了额外的宽度和高度值，例如`canvas.drawImage(canvasImage, 50, 50, 150, 211);`，这将把图像调整为150像素宽、211像素高，并将其定位在距离顶部和左侧各50像素的位置。

## 中级技巧：裁剪图像

你也可以使用包含裁剪属性的第三种方法签名来裁剪图像。裁剪属性包括图像中的起始X和Y位置，以及裁剪框的宽度和高度。这有点复杂，所以清单6.12在每个值旁边都有注释。

### 清单6.12 裁剪图像

```
function cropImage() {
    canvas.drawImage(canvasImage,
        0, // 裁剪框内的位置 X
        0, // 裁剪框内的位置 Y
        168, // 源图像宽度
        236, // 源图像高度
        110, // 裁剪位置 X
        110, // 裁剪位置 Y
        250, // 裁剪宽度
        250 // 裁剪高度
    );
}

canvasImage.addEventListener('load', cropImage, false);
```

除了简单地将图像绘制到画布上，API还提供了一种使用图像来填充给定形状的方法。使用`createPattern`方法，你可以用图像来填充形状的背景。首先，传入你想要显示的图像；然后使用该图像创建一个pattern变量。接着，使用坐标和大小绘制一个形状。然后，将形状的填充样式设置为已创建的pattern，如下所示：



```
var canvasImage = new Image();
function createImagePattern(){
  var pattern = canvas.createPattern(canvasImage, 'repeat');
  canvas.rect(0, 0, 640, 480);
  canvas.fillStyle = pattern;

  canvas.fill();
}

canvasImage.addEventListener('load',createImagePattern,false);

canvasImage.src = 'images/html5-logo.png';
```

`repeat`参数可以具有以下值：

- `repeat`：在水平和垂直方向上重复图案
- `repeat-x`：在水平方向上重复图案
- `repeat-y`：在垂直方向上重复图案
- `no-repeat`：不重复图案

## 中级技巧：制作精灵图动画

由于`drawImage`方法可用于裁剪源图像并将生成的子图像绘制到画布上，你可以利用相同的效果，通过循环播放精灵图像的帧来制作精灵图动画。在设定的时间间隔内，`drawImage`方法被调用以每次渲染源图像的一个新帧，从而创建动画。在这个技巧中，你将使用一个包含三帧的简单精灵图来制作一个回收图标的动画。每次调用`drawImage`时，帧移动到下一帧。到达最后一帧后，帧移回源图像的第一帧。要创建此示例，请使用以下步骤和清单 6.13：

1. 使用清单 6.13 中用于画布的`style`和`body`标签创建页面，并包含启动和停止动画的按钮。
2. 添加全局变量定义、`init`函数和`window.addEventHandler`事件处理器。
3. 添加`animateSprite`函数，用于绘制裁剪后的图像。
4. 添加`startAnimation`和`stopAnimation`函数，它们分别与开始和停止动画按钮关联。

### 清单 6.13 使用图像裁剪与精灵图

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>6.13 精灵图切片动画</title>
<style>
#canvas {
  /* 为画布添加边框 */
  border:1px solid #03F;
}
</style>
<script>
// 用于绘制的画布和上下文变量
var canvas;
var context;

// 动画图像载体
var spriteRecycle = new Image();

// 精灵图像帧变量
var sliceX = 0;
var sliceY = 0;
var sliceWidth = 100;
var sliceHeight = 100;

// 动画变量
var intervalRef;

// 初始化画布
function init() {
  // 设置按钮处理器
  var btnStart = document.getElementById('start');
  var btnStop = document.getElementById('stop');
  btnStart.addEventListener('click',startAnimation,false);
  btnStop.addEventListener('click',stopAnimation,false);

  // 获取画布和上下文的引用
  canvas = document.getElementById('canvas');
  context = canvas.getContext('2d');

  // 分配图像源
  spriteRecycle.src = 'recycle_sprite.png';
}

// 基于切片制作图像动画
function animateSprite() {
  // 根据当前精灵切片绘制图像
  context.drawImage(spriteRecycle, sliceX, sliceY, sliceWidth, sliceHeight, 0, 0,
100, 100);

  // 增加精灵的切片位置
  sliceX+=100;
  // 如果需要，将切片重置为第一帧
  if (sliceX>=spriteRecycle.width) {
      sliceX = 0;
  }
}

// 通过设置间隔来启动动画
function startAnimation() {
    intervalRef = setInterval('animateSprite()',100);
}

// 通过清除已设置的间隔来停止动画
function stopAnimation() {
    clearInterval(intervalRef);
    // 使用 clearRect 擦除画布
    context.clearRect(0,0,100,100);
}

// 在页面加载时调用 init 函数
window.addEventListener('load',init,false);
</script>
</head>
<body>
<h1>使用 Canvas 制作精灵图动画</h1>
<canvas id="canvas" width="100" height="100">
    此浏览器不支持 Canvas 元素。
</canvas>
<br>
<button id="start">开始</button>
<button id="stop">停止</button>
</body>
</html>
```

在用户点击开始按钮后，`startAnimation`函数被调用，该函数设置一个 100 毫秒的间隔来启动`animateSprite`函数。这是动画计时的核心。每隔 100 毫秒，`animateSprite`函数将被调用，直到`stopAnimation`函数被调用并清除该间隔。每次运行`animateSprite`函数时，都会显示回收图像的一个切片。回收图像宽 300 像素，包含三个 100x100 像素的切片。每次绘制切片后，切片的水平位置向右移动 100 像素，如图 6.8 所示。如果切片已经在最后 100 像素处，则将切片移回 0。

![图 6.8](img/de30ea99ecac39b49e690a84c48f43b9_180_0.png)

图 6.8 精灵图像的切片帧在每次循环中显示

请注意，你无需在每次`drawImage`调用前清除画布，因为精灵图像具有不透明背景，并且你每次都在整个 100x100 像素的画布上绘制。

> **注意**

尽管`canvas`元素本身不支持图层，但你可以模仿图层的功能。由于画布是页面上一个可以设置样式的元素，默认具有透明背景，因此没有任何理由阻止开发者定义多个相互层叠的`canvas`元素。要控制页面上的图层位置，可以使用元素上的`z-index`样式属性。想象一个游戏，它有一个背景画布，而角色精灵被加载在一个位于另一个画布之上较小的画布中，这并非牵强附会。如果你实现了多画布页面，请注意性能问题，因为必须保持对各个`canvas`元素的引用才能使用它们。

## 画布变换

除了可用的画布工具和效果外，还有一些变换工具可用。以下是可用的三种变换工具：

- `rotate(angle)`：旋转画布的底层上下文网格，使得任何添加到旋转上下文的内容对用户来说都呈现旋转状态。角度以弧度为单位，顺时针测量。
- `scale(x, y)`：允许开发者控制 x 和 y 单位的比例。该方法接受 x 单位比例和 y 单位比例作为参数。
- `transform`：此转换允许开发者直接访问变换矩阵。

与 canvas 相关联的有三种方法，用于协助执行变换。`translate(x, y)` canvas 方法允许您将 canvas 的原点移动到新位置。因此，如果您调用`translate(100,100)`，新的原点将向下移动 100 像素，向右移动 100 像素，并成为您的新原点。这对于旋转等变换极为重要，因为原点是执行旋转的中心点。有两种方法可以将原点返回到原始位置。第一种是简单地再次使用`translate`方法，以相反方向返回位置。第二种也是首选方法是使用`save`和`restore` canvas 方法。

`save`和`restore`方法允许您在任何变换之前保存当前上下文，然后在稍后将上下文恢复到保存的版本。我们将在各种示例中结合使用这种模式与`rotate`方法，来演示使用 canvas 进行变换。`rotate`方法接受以弧度为单位的数值来旋转 canvas 方向。要将角度度数转换为弧度，请使用以下公式：

弧度数 = 角度度数 * Pi / 180

通过使用诸如`rotate`和`scale`方法之类的变换，您可以使用 canvas 创建有趣的动画，如下一个示例所示。

> **注意**

与任何可基于基本组件进行扩展和重复功能（如绘制正方形、圆形等）的 API 基础调用集一样，各种开发者已经创建了扩展的调用库。反过来，其中许多库已经产品化，并可以为用更简单的调用封装 canvas 功能提供基础。此外，这些库通常扩展了功能，使更复杂的特性更容易使用。您可能想要查看的一些库包括 netron、canvas toolkit、EaselJS、jCanvassScript 和 gury。随着 HTML5 canvas 的日益普及，我们确信库的数量和广度将继续增长。

## 高级示例：为图像添加动画

在本示例中，您将使用两个步骤来使一个齿轮图像从左到右在 canvas 上“滚动”。第一步是通过每隔一定间隔向右重绘图像来移动图像。第二步是在每次移动图像时将其旋转一定角度。如前所述，旋转效果用于旋转绘图的上下文。在本例中，您将保存默认的 canvas 上下文，然后旋转上下文，绘制图像，最后恢复上下文。通过这种方式并结合这些方法，清单 6.14 中的代码将创造出齿轮图像在屏幕上滚动的错觉。

1. 使用`style`和`body`标签创建清单 6.14 中的页面。
2. 添加全局变量定义、`init`函数和`window.addEventListener`事件处理器。
3. 添加`moveGear`函数，该函数负责旋转、移动和绘制齿轮图像。

### 清单 6.14 移动和旋转图像

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>6.14 移动齿轮</title>
<style>
#canvas {
    /* 为 canvas 应用一个简单的边框 */
    border:1px solid #03F;
}
</style>
<script>

// 用于绘图的 canvas 和 context 引用变量
var canvas;
var context;

// 齿轮图像引用
var gear = new Image();

// 图像的当前 x 位置
var xpos;

// 动画变量
var stepCounter;  // 当前步骤计数器
var stepDegrees;  // 每步旋转多少度
var stepDistance;  // 每步移动图像的距离
var stepSpeed;    // 旋转和移动图像的速度
var stepsFullRevolution;  // 完成完整旋转需要多少步

// 初始化画布宽度和高度
function init() {
    canvas = document.getElementById('canvas');
    context = canvas.getContext('2d');

    // 初始化旋转的步数计数器
    stepCounter = 0;
    stepDegrees = 2;
    stepDistance = 2;
    stepSpeed = 5;
    stepsFullRevolution = parseInt(360 / stepDegrees);

    // 添加图像加载事件监听器
    gear.addEventListener('load',initGear,false);

    // 设置齿轮源图像
    gear.src = 'gear.png';
}

// 图像加载后开始动画
function initGear(){
    // 设置初始 X 位置，刚好在 canvas 左侧外部
    xpos = -(gear.width/2);
    // 调用动画函数
    moveGear();
};

// 移除旧齿轮图像并绘制新图像的函数
function moveGear() {

    // 清除 canvas 上的旧齿轮
    context.clearRect(0, 0, canvas.width, canvas.height);

    // 保存当前的 canvas 上下文以便恢复
    context.save();

    // 增加位置
    xpos += stepDistance;

    // 将我们的 0,0 点移动到齿轮的新位置
    context.translate(xpos,canvas.height-(gear.width/2));

    // 旋转上下文，从而旋转我们的齿轮
    context.rotate(Math.PI * stepDegrees * stepCounter / 180);

    // 绘制新旋转后的图像
    context.drawImage(gear, -(gear.width/2), -(gear.height/2), gear.width,
gear.height);

    // 将上下文恢复到原始方向
    context.restore();

    // 检查齿轮是否已从右侧离开 canvas
    if ((xpos-(gear.width/2)) < canvas.width) {
        // 增加步数计数器，并检查是否已完成完整旋转
        stepCounter++;
        if (stepCounter>=(stepsFullRevolution-1)) {
            stepCounter=0;
        }

        // 齿轮仍在显示 - 继续移动
        setTimeout('moveGear()',stepSpeed);
    }
}

// 在页面加载时调用 init 函数
window.addEventListener('load',init,false);

</script>
</head>
<body>
<h1>滚动的齿轮</h1>
<canvas id="canvas" width="600" height="100">
  此浏览器不支持 Canvas 元素。
</canvas>
</body>
</html>
```

当图像加载后调用`moveGear`函数时，代码执行的第一个操作是通过调用`clearRect`清除 canvas。您需要这样做，否则先前绘制的图像“残影”将留在 canvas 上。接下来，脚本保存当前上下文，增加水平位置，然后使用`translate`函数将原点定位到新位置。然后，脚本根据新原点，使用之前通过`rotate`方法设置的`stepDegrees`来旋转图像。接着绘制图像，之后恢复上下文方向以便进行下一次绘图操作。

在将齿轮图像绘制到新位置和角度后，您通过比较水平位置和 canvas 宽度来检查图像是否已移动到 canvas 的右边缘之外。如果已移出边缘，则停止动画。但是，如果图像仍在 canvas 可视区域内，则脚本会增加步数计数器，并设置下一个超时时间以再次启动`moveGear`函数。

可以通过更改脚本顶部的动画变量来调整任何动画设置。图 6.9 显示了图像在 canvas 中的不同阶段。

![img/de30ea99ecac39b49e690a84c48f43b9_185_0.png](img/de30ea99ecac39b49e690a84c48f43b9_185_0.png)

图 6.9 精灵图像在每次循环中显示时的切片帧

> **注意**

您可以通过捕获`mouseover`和`click`等鼠标事件与 canvas 进行交互，无论是玩游戏还是移动形状。事件提供的坐标可以通过偏移 X 和 Y 坐标映射到页面上 canvas 的位置。例如，如果鼠标单击事件的 X,Y 为 150,200，而 canvas 的偏移量 x 为 100，y 为 100，那么鼠标单击在 canvas 内的坐标为 50,100。知道了这个 canvas 网格中的坐标，您就可以确定该点击是否发生在绘制在 canvas 上的特定形状上。

## 高级示例：为垂直柱状图添加动画

在本章的最后一个示例中，您将使用 canvas 工具以及一些效果和变换，从一组示例 JSON 数据创建一个垂直柱状图。当图表加载时，垂直柱条将根据一些预设的动画设置（如每列增长的速度和距离）增长到其定义值。图 6.10 显示了柱条动画完成后，使用示例数据输出的结果。要创建此示例，请按照以下步骤和清单 6.15 中的代码操作：

1. 创建清单 6.15 中的页面，其中`style`和`body`标签用于 canvas，其`id`为`graph`。
2. 添加全局变量定义，包括`chartData` JSON 对象、`initGraph`函数和`window.addEventListener`事件处理器。
3. 添加`initSettings`函数，该函数设置图表的所有属性，包括柱条的数量和尺寸。
4. 添加`drawAxis`函数，该函数将添加 x 轴和 y 轴线、轴上的数据标记和标题。
5. 添加`growBars`函数，该函数用于将垂直柱条的增长动画到其正确的高度。
6. 添加`drawBar`辅助函数，该函数执行在 canvas 上绘制柱条的实际操作。

# 第6章 使用Canvas绘图



![](img/de30ea99ecac39b49e690a84c48f43b9_186_0.png)

图6.10 使用示例数据完成的垂直条形图

## 清单6.16 创建动画垂直条形图

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>6.16 Growing Bar Chart</title>
<style>
#graph {
  /* outline our canvas */
  border:1px solid #03F;
}
</style>
<script>

// Canvas and drawing context variables
var canvas;
var context;

// Chart settings
var chartMargin;
var chartAxisSpace;
var chartWidth;
var chartHeight;

// bar variables
var numBars = 0;       // total number of bars
var barMargin = 20;    // margin between bars
var barWidth = 0;     // bar width
var maxValue = 0;     // maximum data value for the bars

// number of y-axis labels
var numYLabels;

// bar animation variables
var idxStep;
var numSteps;
var growSpeed;

// Chart JSON sample data
var chartData = {'bars':[
  {'title':'Year 1','value':'7'},
  {'title':'Year 2','value':'12'},
  {'title':'Year 3','value':'20'},
  {'title':'Year 4','value':'33'},
  {'title':'Year 5','value':'55'},
  {'title':'Year 6','value':'93'},
  {'title':'Year 7','value':'156'}
]}

// initialize the board width and height
function initGraph() {

  // get reference to canvas and drawing context
  canvas = document.getElementById('graph');
  context = canvas.getContext('2d');

  initSettings(); // initialize the chart settings
  drawAxis(); // draw the chart axis and labels
  growBars(); // animate the bars into the chart
}

function initSettings() {

  // set our chart settings
  chartMargin = 20; // margin around entire canvas
  chartAxisSpace = 50; // area for the x- and y-axes
  // set the chart drawing area
  chartHeight = canvas.height-chartAxisSpace-2*chartMargin;
  chartWidth = canvas.width-chartAxisSpace-2*chartMargin;

  // set the number of labels to use for the y-axis
  numYLabels = 8;

  // set the number of bars based on the chartData
  numBars = chartData.bars.length;

  // find our max data value to scale the graph
  for (var i=0; i < numBars; i++) {
      if (chartData.bars[i].value > maxValue) {
          maxValue = parseInt(chartData.bars[i].value);
      }
  }

  // determine the width of each bar
  barWidth = (chartWidth / numBars)-barMargin;

  // initialize animation variables
  idxStep = 0;
  numSteps = 100;
  growSpeed = 6;
}

function drawAxis() {
    // Set line width for the axis lines
    context.lineWidth = 2;

    // draw y-axis - from lower left to upper left
    context.moveTo(chartMargin+chartAxisSpace,chartHeight+chartMargin);
    context.lineTo(chartMargin+chartAxisSpace, chartMargin);
    context.stroke();

    // draw X axis - from lower left to lower right
    context.moveTo(chartMargin+chartAxisSpace, chartMargin+chartHeight);
    context.lineTo(chartMargin+chartAxisSpace+chartWidth, chartMargin+chartHeight);
    context.stroke();

    // Set the line width back to 1 pixel
    context.lineWidth = 1;

    // Add data marks to the y-axis
    var markerAmount = parseInt(maxValue / numYLabels);
    context.textAlign = 'right';
    context.fillStyle = '#000';
    // Loop through and add the markers to the y-axis
    for (var i=0; i <= numYLabels; i++) {
        // Determine the label and X and Y points
        markerLabel = i*markerAmount;
        markerXPos = chartMargin + chartAxisSpace - 5;
        markerYPos = chartMargin + (chartHeight - 
            ((i*markerAmount*chartHeight)/maxValue));
        
        // Add the text marker at the positions determined
        context.fillText(markerLabel, markerXPos, markerYPos, chartAxisSpace);
    }
}

// Add labels for each bar based on the chart data
context.textAlign = 'center';
// loop through each bar and add the title
for (var i=0; i<numBars; i++) {
    // determine the X and Y positions for the marker
    markerXPos = chartMargin+chartAxisSpace + barMargin + (i * (barWidth+barMargin)) + (.5*barWidth);
    markerYPos = chartMargin+chartHeight + 10;

    // Add the text under the bottom of the bar
    context.fillText(chartData.bars[i].title, markerXPos, markerYPos, barWidth);
}

// Add y-axis title
// Save the present context
context.save();
// Move the 0,0 point to the y-axis title point
context.translate(chartMargin+10,chartHeight/2);
// Rotate the current drawing context counter-clockwise 90 degrees
context.rotate(Math.PI*-90 / 180);
// Add our text title
context.fillText('Sales (in 000s)',0,0);
// Restore the context drawing orientation
context.restore();

// Add X Axis Title
context.fillText('Year Out',chartMargin+chartAxisSpace+(chartWidth/2),chartMargin+chartHeight+40);
}

// Animation function to grow the bars vertically
// Called on a timeout based on number of steps
function growBars() {

    // Declare our bar x,y, and h
    // barWidth is predetermined above
    var barStartX = 0;
    var barStartY = 0;
    var barHeight = 0;

    // bar value variable from the data set
    var barValue = 0;

    // Loop through the bars and draw each based on step
    for (var i=0; i < numBars; i++) {
        // get the bar value
        barValue = parseInt(chartData.bars[i].value);

        // calculate the bar height, starting x and y points
        barHeight = (barValue * chartHeight / maxValue) / numSteps * idxStep;
        barStartX = chartMargin + chartAxisSpace + (i * (barWidth + barMargin)) + barMargin;
        barStartY = chartMargin + (chartHeight-barHeight);

        // call the helper function to draw the bar
        drawBar(barStartX, barStartY, barWidth, barHeight);
    }

    // Grow the bars more if they have not finished growing
    if (idxStep<numSteps) {
      idxStep++;
      setTimeout('growBars()',growSpeed);
    }
}

// helper function to draw a bar based on dimensions passed
//could pass in context along with other params to customize
function drawBar(barX, barY, barW, barH) {
  // Create rectangle with fill
  context.fillStyle = '#00c';
  context.fillRect(barX, barY, barW, barH);

  // Add shadow to bar
  context.shadowOffsetX = 3;
  context.shadowOffsetY = -3;
  context.shadowBlur = 3;
  context.shadowColor = 'rgba(200, 200, 200, .3)';

  // Add line border on the bar
  context.strokeStyle = '#000';
  context.lineWidth = 1;
  context.strokeRect(barX, barY, barW, barH);
}

// on page load initialize the bar chart
window.addEventListener('load',initGraph,false);

</script>
</head>
<body>
  <h1>Growing Bar Chart</h1>
  <canvas id="graph" width="600" height="400">
  This browser does not support the canvas element.
  </canvas>
</body>
</html>
```

当页面加载时，`initGraph`函数将被调用，它接着会调用`initSettings`函数，该函数将设置图表的所有设置。接下来，`initGraph`将调用`drawAxis`方法。`drawAxis`函数将为x轴和y轴绘制两条线。然后，该函数将根据你在初始化中设置的刻度数量，在y轴上添加数据标记。对于x轴，你使用JSON图表数据中每个条形的`title`属性。注意，你将每个条形的文本对齐到条形的中心。最后，该函数添加y轴标题（逆时针旋转90度）和x轴标题。

接下来，`initGraph`函数调用`growBars`函数。`growBars`函数是这个简单动画的核心，它递增动画步骤，以确定基于`chartData`中最终条形值的百分比级别来增长每个条形。通过这种方式，每次执行`growBars`函数时，该函数都按比例增长每个条形。在计算每个条形的新尺寸后，`growBars`函数将使用条形尺寸调用辅助函数`drawBar`，以在画布上实际绘制条形。一旦`growBars`函数遍历了图表的所有条形，该函数就会检查此步骤是否是动画的最后一步。如果还有更多步骤，则在递增步骤索引后，该函数设置一个超时来再次调用`growBars`函数。图6.11展示了条形图如何通过此动画增长。

要改变条形的速度或增长率，你只需在`initSettings`函数中更改`numSteps`和`growSpeed`变量。

> **提示**

> 使用HTML5 canvas创建动画甚至交互式图表非常简单，正如你在最后一个示例中看到的那样。如果你想看到使用HTML5 canvas创建图表的无尽可能性——从基本的折线图到复杂的玫瑰图——你将想查看RGraph JavaScript和HTML5 canvas图表库www.rgraph.net。该库的开发人员已经完成了繁重的工作，只要你遵循许可协议，你就可以根据需要将其合并到你自己的项目中。无论哪种方式，该库都展示了将canvas与JavaScript结合使用的潜力。

![](img/de30ea99ecac39b49e690a84c48f43b9_191_0.png)

## 总结

在本章中，你学习了 Canvas API。Canvas API 提供了远超已描述内容的强大绘图功能。然而，有了这些基础知识，你现在就有工具去探索 Canvas API 的更多高级方法和主题。我们鼓励你突破其极限，让你的艺术创造力尽情流淌。

## 7. 使用 HTML5 嵌入视频

除非你过去五年左右都与世隔绝，否则我们确信你肯定用过像 YouTube 和 Vimeo 这样的网站，换句话说，就是那些在页面上嵌入了视频的网站。尽管这些网站是主要的视频分享平台，但在过去近十年里，我们一直在以各种方式将视频放到网上。问题在于视频呈现没有统一标准，因此我们不得不使用 Flash 等插件，或者使用 object 元素来播放 QuickTime 文件。

你可能觉得这没什么问题，因为大多数情况下这些方法都有效。问题在于你不应该依赖第三方插件来播放视频。在 HTML5 中，你现在有了新的标准方式来在网页中原生渲染视频。你可以使用 video 元素。

在本章中，你将学习 video 元素的基础知识，然后了解一些编解码器，以及通常会遇到的跨浏览器问题。你还将学习如何通过字幕和说明文字来改善视频的无障碍访问，最后你将使用新的 HTML5 媒体 API 创建你自己的视频播放器和控件。

## 初级技巧：使用 video 元素包含视频

关于如何使用新的 video 元素在页面上放置视频，一个非常基础的示例请参阅代码清单 7.1。

### 代码清单 7.1 video 元素的基础使用



```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>7_1 Basic Use of the Video Element</title>
</head>
<body>
  <video src="mymovie.mp4"></video>
  <!--
    video is a self-closing element so can also be used as:
    <video src="mymovie.mp4" />
  -->
</body>
</html>
```

很简单，不是吗？在基础层面上，这就是让`video`元素在 HTML5 中工作所需的全部。然而，遗憾的是，实际情况并不完全如此简单。但既然已经引起了你的兴趣，在你开始使用视频之前，还有一些问题需要了解。

## 浏览器和设备支持

表 7.1 列出了`video`元素的浏览器兼容性。它假设的是撰写时的浏览器最新版本以及此后发布的所有版本。

**表 7.1 `video`元素的支持情况**

| 浏览器/设备 | 支持版本 |
|---|---|
| Android | 2.1+ |
| Chrome | 10.0+ |
| Firefox | 3.6+ |
| Internet Explorer | 9.0+ |
| iOS Safari | 3.2+ |
| Opera | 10.6+ |
| Safari | 4.0+ |

所以，一方面，当前浏览器对`video`元素的支持非常好；但另一方面，Internet Explorer 6、7 和 8 版本并不原生支持`video`元素，而它们的市场份额加起来非常大。本章稍后将展示如何为那些尚不支持`video`元素的浏览器和设备提供回退内容。但在我们深入探讨之前，你需要先理解不同的视频类型和编解码器。

## HTML5 与视频编解码器

HTML5 视频取得了巨大成功，特别是像 YouTube 和 Vimeo 这样的大型视频网站已经开始创建 HTML5 视频内容。然而，HTML5 视频面临着一个重大挑战：编解码器问题。

如果你曾经将视频上传到 YouTube，你可能没有留意上传的文件格式，因为 YouTube 几乎接受任何视频文件格式并为你转换视频。但在 HTML5 中，目前你需要考虑三种主要的编解码器和视频格式（见表 7.2）。

在 HTML5 规范的早期，原本计划所有浏览器都应支持 Ogg Theora 编解码器（Ogg Theora 是视频编解码器；Ogg Vorbis 是音频编解码器）。然而，苹果和诺基亚对此有异议，因此这些编解码器被从规范中移除，再也没有恢复，也没有提出其他编解码器建议。

目前，Chrome 和 Firefox 浏览器原生支持 Ogg Theora。Safari 目前仅原生支持 H.264 编解码器。H.264 编解码器也得到 Chrome、iPhone、iPad 和 Android (2.3) 设备的支持。

2010 年 5 月，谷歌宣布开发另一种多媒体格式——webM（也称为 VP8）项目。这是一个开源编解码器，并迅速获得了 Chrome、Firefox 和 Opera 浏览器的支持。

Internet Explorer 9 原生支持 H.264 编解码器，但只有通过单独安装的编解码器才能支持 webM，这并不理想。

### 为什么你应该关心编解码器问题？

编解码器问题将在未来一段时间内持续存在。最大的问题是 H.264 编解码器。H.264，也称为 MPEG-4，要求其产品的供应商和用户（如果你在你的网站上托管它，你就是用户）支付专利许可费。2010 年 8 月，有消息称用户使用 H.264 视频将*不会*被收费，但这一点存在争议，并且可以说在涉及此编解码器的许可时，情况并不完全明朗。

然而，Ogg 和 webM 都是免版税的开源编解码器，被认为是“开放网络”的格式。在 2011 年 1 月之前，Chrome 确实支持 H.264，但在 2011 年 1 月，谷歌提升了视频竞争层次，宣布将放弃对 H.264 编解码器的支持，转而支持 webM 视频编解码器。本书不会深入探讨这一决定的所有细节，但关于谷歌为何做出此决定有各种理论。值得一提的是，YouTube（谷歌所有）将继续将视频转换为 H.264 格式，但它可能会将所有视频转换为 webM，而目前尚不清楚 Android（也是谷歌所有）设备在 H.264 格式方面会如何处理。移动视频规模庞大且只增不减，因此我们强烈建议密切关注此话题。

正如你所看到的，面对如此多的浏览器和设备以及背后的诸多博弈，编解码器是一个巨大的挑战。谷歌决定的影响可能很深远，但我们目前尚不清楚究竟有多深远。我们也不知道 Internet Explorer 9 将如何处理这一切，因此有很多东西需要你思考和及时更新。

不过，不要让这些编解码器问题阻止你，因为你仍然可以使用 HTML5 视频做很多事情。

> **提示：** 好的，你已经了解了不同的格式，但如何创建它们呢？目前流行的视频软件包通常不导出 Ogg 或 webM 格式，而是导出 H.264 文件。iPhone 导出 .mov 文件，大多数数码相机将导出为 .mov 或 .avi 文件。有各种软件可用于转换你的视频，包括 Firefogg（一个编码 Ogg 视频的 Firefox 扩展）或 Handbrake（用于编码 H.264 视频）。但我们建议使用 MiroVideoConverter (http://mirovideoconverter.com)，这是一款易于使用且*免费*的软件，可以转换为几种不同的视频类型。

## 中级技巧：为所有浏览器启用视频

正如本章第一个技巧中提到的，`video`元素最简单的用法是使用以下标记：

```html
<video src="mymovie.mp4"></video>
```

由于浏览器和编解码器问题，你必须在同一个`video`元素中提供不同格式的视频，这通过使用多个`source`元素来实现。为了让视频在关键浏览器的最新版本中工作，你需要指定一个 .mp4 格式和一个 .webm 或 .ogv 格式的文件，这正是你在代码清单 7.2 中所做的。

### 代码清单 7.2 使用 Source 元素显示不同视频格式

```html
<video width="640" height="480" controls>
    <source src="video.mp4" type="video/mp4" />
    <source src="video.webm" type="video/webm" />
    <source src="video.ogv" type="video/ogg" />
</video>
```

> **注意**

在理想情况下，浏览器和设备会自动选择它们能播放的第一个文件。虽然这在主流桌面和笔记本电脑浏览器上通常可行，但 iPad 浏览器存在一个 bug，导致它只能加载第一个源视频文件。因此，必须将 .mp4 文件放在首位，如清单 7.2 所示。

`video`元素有`height`和`width`值，尽管你可以使用 CSS 来设置高度和宽度。该元素还有一个`controls`属性，用于显示默认的视频控件。在清单 7.2 中，`video`元素内有三个`source`元素，每个`source`元素都链接到一个单独的视频。每个`source`都有一个`type`属性，因为此属性告诉浏览器所提供的文件类型。如果浏览器不识别该类型，它将不会下载该文件，这一点很重要，因为它可以节省带宽并加快页面加载速度。浏览器会选择它能播放的第一个文件。

清单 7.2 提供的视频可以在 Chrome、Firefox、Internet Explorer 9 和 Safari 上播放，并适用于 iPad、iPhone 和最新的 Android (2.3) 设备，所有这些都无需第三方组件，这非常棒。但是，对于使用 Internet Explorer 6、7 和 8 的用户，这些浏览器当时不支持`video`标签，你能提供什么呢？

### 为旧版浏览器添加后备内容

在`source`元素之后，你可以放入一些内容，当用户的浏览器无法处理`video`元素时向他们发出提示。将该内容放在`video`元素内部，你有多种选择来决定提供什么信息。你可以提供一些简单的消息，如下所示：

```
<p>抱歉，您的浏览器版本太旧了。请升级。</p>
```

或者，你可以提供更实用的帮助，直接提供视频的下载链接：

```
<a href="video.mp4">下载我们的 MP4 格式电影</a>
<a href="video.webm">下载我们的 WebM 格式电影</a>
<a href="video.ogv">下载我们的 Ogg 格式电影</a>
```

提供直接下载选项总是一个好主意，而且你应该将其提供给所有用户，无论他们使用什么设备，因此我们将在最终的代码解决方案中加入这段代码。主要来说，我们将这些后备内容针对那些使用旧版 Internet Explorer 浏览的用户。由于 Flash 拥有巨大的市场份额，并且安装在非常高比例的机器上，因此你可以相对安全地将 Flash 内容作为后备。对此有几个可能的选择：你可以将视频上传到 YouTube，或者你可以使用自己的 Flash 播放器。选择 YouTube 选项会让事情变得非常简单，同时它还能解决托管问题。YouTube 还会为你提供所需的 HTML 代码，以便将电影嵌入你的页面，如清单 7.3 所示。

### 清单 7.3 YouTube 视频嵌入代码

```
<object width="480" height="385">
    <param name="movie" value="http://www.youtube.com/v/VIDEO_ID"></param>
    <param name="allowFullScreen" value="true"></param>
    <param name="allowscriptaccess" value="always"></param>
    <embed src="http://www.youtube.com/v/VIDEO_ID" type="application/x-shockwave-flash" allowscriptaccess="always" allowfullscreen="true" width="480" height="385">
    </embed>
</object>
```

因此，将所有这些整合起来就得到了清单 7.4 中的代码，它通过原生的`video`元素或使用 Flash 后备方案，在所有当前主流浏览器中提供视频。

### 清单 7.4 包含后备方案的跨浏览器视频

```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>7_4 包含后备方案的跨浏览器视频</title>
</head>
<body>
<video width="640" height="480" controls>
    <!-- 适用于 Safari 和 IE9 的视频。iPad 必须首先使用 MP4 -->
    <source src="cablecar.mp4" type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"' />
    <!-- 适用于 Chrome、Firefox 和 Opera 的视频 -->
    <source src="cablecar.webm" type="video/webm" />
    <source src="cablecar.ogv" type="video/ogg; codecs="theora, vorbis"' />

    <!-- 为较旧、功能较弱的浏览器提供的后备方案 -->
    <object width="480" height="385">
        <param name="movie" value="http://www.youtube.com/v/ZR-H-FQDenw"></param>
        <param name="allowFullScreen" value="true"></param>
        <param name="allowscriptaccess" value="always"></param>
        <embed src="http://www.youtube.com/v/ZR-H-FQDenw" type="application/x-shockwave-flash" allowscriptaccess="always" allowfullscreen="true" width="480" height="385">
        </embed>
    </object>
</video>
</body>
</html>
```

你不必选择 YouTube 作为视频托管方；你可以自己托管文件并使用自己的 Flash 电影来播放视频。你可以自己制作一个，或者使用互联网上众多可用的播放器之一，例如流行且可定制的 JW Player，如清单 7.5 所示。

### 清单 7.5 非 YouTube 后备视频

```
<video width="640" height="480" controls>  <!-- 适用于 Safari 和 IE9 的视频。iPad 必须首先使用 MP4 -->
    <source src="video.mp4" type="video/mp4" />

    <!-- 适用于 Chrome、Firefox 和 Opera 的视频 -->
    <source src="video.webm" type="video/webm" />
    <source src="video.ogv" type="video/ogg" />

    <!-- 为较旧、功能较弱的浏览器提供的 JW Player 后备方案 -->
    <script type='text/javascript' src='swfobject.js'></script>
    <div id='mediaplayer'></div>
    <script type="text/javascript">
      var so = new SWFObject('player.swf','playerID','480','270','9');
      so.addParam('allowfullscreen','true');
      so.addParam('allowscriptaccess','always');
      so.addVariable('file', 'video.mp4');
      so.write('mediaplayer');
    </script>
</video>
```

> **提示**

在 HTML5 视频开发中，可能会遇到的一个问题是 MIME 类型问题。在为本书开发示例时，我们遇到一个问题：当 .ogv 和 .webm 文件上传到 Web 服务器后，在 Firefox 中无法播放。这些视频在我们的本地机器上播放正常，当放到 Web 服务器（Apache）上时，在 Opera 和 Chrome 中也能正常运行；然而，.ogv 和 .webm 文件在 Firefox 中却无法播放。这是因为 Firefox 需要知道服务器支持特定的 MIME 类型。并非所有服务器都支持这些新的视频类型，为了支持它们，你必须进行适当的配置更改，例如根据你的服务器平台，在 .htaccess 或 httpd.conf 文件中添加以下几行：

```
AddType video/mp4 .mp4
AddType video/ogg .ogv
AddType video/webm .webm
```

所以，现在你拥有了为所有主流浏览器和设备提供视频的完整代码，但还有一些额外的新属性可用。

## 新的视频属性

`video`元素有几个新的可用属性。在前面的示例中，你使用了`width`和`height`属性，这些属性不是必需的，但我们建议设置这些值，因为这有助于加载时间。设置这些值不会拉伸或扭曲你的视频，因为`video`元素会将视频放在框的中间，所以如果你将高度和宽度设置为 200 x 1000，浏览器会相应地缩小视频，同时保持其比例。

### `src`属性

本章开头的清单 7.1 展示了一个非常基础的`video`元素示例，它包含一个`src`属性。但使用`src`意味着你只能限于一个视频文件，并且由于编解码器和浏览器的问题，这使得它在目前几乎没有用处。与其使用`src`，不如考虑在`video`内部使用`source`元素，如清单 7.4 所示，这样你就可以使视频在各种浏览器中工作。

### `poster`属性

`poster`属性用于在视频下载期间或等待开始播放时，显示一张图片代替视频。`poster`图片旨在让观众对视频的内容或主题有一个概念。该图片可以是 .gif、.jpg 或 .png 文件（尽管透明的 PNG 不会叠加在视频上）。如果没有`poster`，浏览器只会显示视频的第一帧，这可能适合你的需要。如果不适合，下面是设置`poster`图片的方法，图 7.1 展示了它在页面加载时的样子：

```
<video width="640" height="480" poster="poster.gif">
```

![在 Google Chrome 中显示的`poster`图片](img/de30ea99ecac39b49e690a84c48f43b9_200_0.png)

图 7.1 在 Google Chrome 中显示的`poster`图片

### `preload`属性

如果页面上有一个相对较大的视频，或者你确信用户会想观看你嵌入的视频（例如 YouTube 页面），那么你可以让浏览器在页面加载时开始下载该视频。`preload`属性有三个可能的值：

```
preload="auto"
```



`auto`，或者你只需写`preload`，这会告诉浏览器在页面加载时下载视频。

```
preload="none"
```

`preload="none"`告诉浏览器不要下载视频。只有当用户开始播放视频时，它才会开始下载。不过目前，似乎只有 Firefox 4 支持这一项。

```
preload="metadata"
```

`metadata`属性会检索关于视频的信息（元数据），包括视频时长、第一帧、视频尺寸和音轨列表。浏览器在用户开始播放视频本身之前，不应该下载视频。

### `audio`属性（目前不支持）

虽然浏览器目前不支持，但`audio`属性的存在是为了让你可以控制视频的默认音量。目前，它只有一个指定的值：`muted`。使用时，它看起来像这样：

```
<video height="300" width="300" audio="muted">
...
</video>
```

其思路是，如果使用了这个属性，那么视频默认将是静音的，用户需要手动调高音量。将来有可能可以填入其他值，例如`audio="2"`或`audio="low"`，以控制默认音频音量。在后面的章节中，你将看到如何通过 JavaScript 更改音量。

#### `loop`属性

如果`video`具有`loop`属性，那么当视频播放结束时，它将循环回到开头并再次播放。这是一个布尔属性，所以它要么开启，要么关闭。除了奇怪的 Firefox 4 当前测试版外，所有主流浏览器都支持此属性。

### `autoplay`属性

`autoplay`是一个布尔属性，它将强制浏览器在页面加载时开始下载并播放视频。例如，YouTube 就是这样做的，视频广告也经常自动开始播放。关于视频自动播放，存在可访问性和可用性方面的担忧，更不用说这可能会很烦人。但规范中之所以包含它，是因为你现在有了一个标准的方式来实现这一点（如果你*真的*需要的话）。你不必借助各种 JavaScript 技巧来达到这个效果。请注意，已经有各种浏览器扩展可以下载，用于禁用自动播放。

> **注意**

在 iOS 中，`autoplay`和`preload`属性已被故意禁用。这是出于对用户潜在成本和加载速度问题的考虑。在用户手动选择开始播放视频之前，不会下载任何数据。有一些技术，嗯，可以说是变通方法，可以绕过这个限制。但由于它们是非官方方法，不应该被使用，本书也不会涉及。

### `controls`属性

`controls`属性为你的视频添加了默认的浏览器特定控件，包括播放/暂停按钮、进度条、时长/已播放时间信息和音量控制。

该属性是一个布尔属性，所以你要么包含它，要么不包含。以下是一个示例：

```
<video height="300" width="300" controls>
...
</video>
```

如果未包含，则会显示视频的第一帧或`poster`图片。用户必须右键点击视频并从选项列表中选择。因此，最好使用`controls`属性提供控件。如果你想，可以使用自定义控件，我们将在本章后面讨论这一点。图 7.2 显示了各大浏览器中的默认控件。

> **注意**

奇怪的是，在 Firefox 中，如果你没有启用 JavaScript，那么控件不会出现。其他浏览器则正确地在没有 JavaScript 的情况下显示控件。

![](img/de30ea99ecac39b49e690a84c48f43b9_203_0.png)

图 7.2 Chrome（顶部）、Firefox、Internet Explorer 9、Opera 和 Safari 中的默认控件

## 中级技巧：创建带字幕和说明的视频

你可以做一些事情来提高视频的可访问性。例如，你可以启用字幕、隐藏式字幕和描述，以帮助耳聋或听力障碍者。

有一个`track`元素可用，你可以用它来使用不同类型的文件。以下是其基本用法：

```
<track src="subtitles.vtt" kind="subtitles" srclang="en" label="English">
```

对于`kind`属性，你可以使用不同的值：

- `subtitles`：对话的转录或翻译

- `captions`：类似于字幕，但也包括音效和其他音频信息

- `descriptions`：旨在成为单独的音频文件，描述视频内容

- `chapters`：旨在帮助用户导航视频

- `metadata`：关于视频的信息和内容，不打算显示给观众

`track`元素是 HTML5 规范中非常近期的新增内容，字幕/隐藏式字幕的标准最初是 WebSRT，但现在是 Web Video Text Track (WebVTT)。由于这项技术很新，而且工作量巨大，目前还没有可用的示例或浏览器实现。不过，你可以使用 JavaScript 和 WebVTT (`.vtt`) 文件来显示字幕。清单 7.6 是一个基本示例，包含来自 WebVTT 文件的一些示例数据（基于当前规范）。你可以使用像 Notepad 这样的基本文本编辑器创建和编辑`.vtt`文件。`.vtt`文件包含一个步骤编号，然后是它要显示的时段，接着是要显示的内容。

清单 7.6  示例`.vtt`文件内容

```
0
00:00:0,000 --> 00:00:2,000
This is the first bit of the subtitles

1
00:00:3,000 --> 00:00:5,000
This is the second bit

2
00:00:7,000 --> 00:00:15,000
And as you might have guessed, this is the third bit of the subtitles
```

由于目前还没有浏览器原生支持`track`元素，你需要一个 JavaScript 插件来完成这项工作。在清单 7.7 中，你使用的是一个名为 VideoSub 的 jQuery 插件，可从 http://github.com/icelab/jquery-videosub 获取，它基于 Thomas Sturm 的原始 MooTools 脚本 (http://storiesinflight.com/js_videosub)。该插件将视频包装在一个`div`中，然后添加一个包含字幕的额外`div`。在这个例子中，你默认隐藏字幕，并添加一个链接来切换字幕显示。图 7.3 显示了字幕显示效果的示例。完整代码在清单 7.7 中。

![](img/de30ea99ecac39b49e690a84c48f43b9_204_0.png)

图 7.3    视频上显示的字幕

清单 7.7    视频字幕

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>7_7 Video Subtitles</title>
<script
    src="http://ajax.googleapis.com/ajax/libs/jquery/1.4.4/jquery.min.js"></script>
<script src="jquery.videosub.js"></script>
<script>
$(function(){
  $('video').videoSub({
    containerClass : 'videosub-container',
    barClass : 'videosub-bar',
    useBarDefaultStyle : false
  });

  $('.videosub-container').append('<a title="show/hide video subtitles"
    id="subtitlestoggle" href="#">Show subtitles</a>');

  $('.videosub-bar').hide();

  $('#subtitlestoggle').click(function() {
    $(this).text($(this).text() == 'Show subtitles' ? 'Hide subtitles' : 'Show subtitles');
    $('.videosub-bar').toggle();
  });
});
</script>
<style>
body {
  font-family: arial, Arial, Helvetica, sans-serif;
}
.videosub-container {
  width: 640px;
}
.videosub-bar {
  background: black;
  bottom: 40px;
  color: yellow;
  font-size: 1.3em;
  font-weight: bold;
  padding: 10px 20px;
  position: absolute;
  text-align: center;
  width: 560px;
}
a#subtitlestoggle {
  background: black;
  color: yellow;
  display: block;
  font-weight: bold;
  padding: 10px;
  position: absolute;
  right: 0;
  text-decoration: none;
  top: 0;
}
a#subtitlestoggle:hover {
  text-decoration: underline;
}
</style>
```

一个值得留意的可能发展是，是否应该为`poster`图片提供`alt`文本。目前尚未最终确定，但存在一些可访问性问题，因此`poster`属性未来可能会有所改变。

## 第7章 使用HTML5嵌入视频

```
</head>
<body>
<video width="640" height="480" controls>
  <!-- 用于Safari和IE9的视频格式。MP4必须放在第一位以支持iPad -->
  <source src="video.mp4" type="video/mp4" />

  <!-- 用于Chrome、Firefox和Opera的视频格式 -->
  <source src="video.webm" type="video/webm" />
  <source src="video.ogv" type="video/ogg" />
  <track src="subtitles.vtt" kind="subtitles" srclang="en" label="English">

  <!-- 为兼容性较差的浏览器（如YouTube等）提供的后备方案 -->
</video>

<p>下载视频：<a href="video.mp4">MP4文件，3MB</a>；<a href="video.webm">WebM文件，3MB</a>；<a href="video.ogv">Ogg文件，3MB</a></p>
<p>下载字幕：<a href="subtitles.vtt">VTT文件，1 KB</a>；<a href="subtitles.txt">纯文本文件，1 KB</a></p>

</body>
</html>
```

### 其他字幕样式选项

清单7.6和7.7展示了WebVTT、jQuery插件以及一些用于显示和设置字幕样式的基础CSS的基本示例。有一些替代方案在未来可能会得到浏览器支持。首先，你可以使用内联的`<b>`、`<i>`和`<u>`标签为字幕添加粗体、斜体或下划线样式：

```
1
00:00:0,000 --> 00:00:2,000
<b>This is</b> the <i>first bit</i> of the <u>subtitles</u>
```

如果你想实现粗体、斜体或下划线之外的效果，也可以应用一个CSS类。例如，你可以使用自定义字体。为此，你需要添加一个带有CSS类的内联`<c>`标签：

```
1
00:00:0,000 --> 00:00:2,000
<c.myclassname>This is</c> the first bit of the subtitles
```

还有更多选项，例如文本位置和文本大小。关于这个发展中的标准的更多信息，请查阅 http://delphiki.com/webvtt。

## 媒体API

HTML5为多媒体提供了庞大且令人兴奋的API。使用该API和JavaScript，你可以操控网页中的视频。以下是可用的API事件列表：

- `abort`

- `canplay`

- `canplaythrough`

- `canshowcurrentframe`

- `dataunavailable`

- `durationchange`

- `emptied`

- `empty`

- `ended`

- `error`

- `loadeddata`

- `loadedmetadata`

- `loadstart`

- `pause`

- `play`

- `playing`

- `progress`

- `ratechange`

- `seeked`

- `seeking`

- `suspend`

- `timeupdate`

- `volumechange`

- `waiting`

还有许多可用的媒体属性：

- `audioTracks`

- `autoplay`

- `buffered`

- `controls`

- `controller`

- `currentSrc`

- `currentTime`

- `defaultMuted`

- `defaultPlaybackRate`

- `duration`

- `ended`

- `error`

- `initialTime`

- `loop`

- `muted`

- `networkState`

- `paused`

- `preload`

- `played`

- `playbackRate`

- `readyState`

- `seekable`

- `seeking`

- `startOffsetTime`

- `src`

- `textTracks`

- `videoTracks`

- `volume`

并非所有这些事件和属性都已可供使用，但大多数都可以使用，包括那些允许你创建自己的视频播放器控件的重要选项。我们不会解释所有的API选项，只讲解创建你自己的播放器所需的部分。但如果你有兴趣了解更多关于API的信息，我们推荐参考 http://w3.org/2010/05/video/mediaevents.html 上的API演示和 http://w3.org/TR/html5/video.html#mediaevents 上非常详细的规范。

## 高级技巧：制作你自己的自定义控件

HTML5为`<video>`和`<audio>`元素提供了JavaScript媒体API。如上一节所示，有许多方法和事件可供你使用，以便创建自己的视频播放器和自定义控件。

本技巧以清单7.4中的视频代码为基础，添加了一个播放/暂停按钮、一个进度条、音量控件、时间显示以及快进和快退按钮。正如我们稍后将要解释的，浏览器存在一些怪癖，因此本技巧中创建的示例最好在Opera或Chrome中查看，如图7.4所示。

你自己创建控件所需的基本功能是播放按钮，但借助JavaScript和媒体API，你可以创建远比这更多的功能，正如使用清单7.8中的代码所示。

1.  用一个`<div id="video-wrapper">`包裹`<video>`元素，并添加一个包含按钮、滑块和其他控件显示所需元素的`<div id="controls">`。为了便于阅读，我们在本技巧的开始就包含了这个HTML，但实际上，你应该避免在主标记中包含这样的控件，而应该使用JavaScript动态创建它们，这样只有启用了JavaScript的用户才能获得这些控件。

2.  将`<video>`元素声明为一个对象，以便可以引用它，然后通过删除为非JavaScript用户指定的`controls`属性来移除默认的浏览器控件。在视频准备好播放之前，播放按钮是禁用的。

3.  为了更好的性能和跨浏览器兼容性，你需要等待视频准备就绪，然后才能收集其持续时间等信息。当视频准备好播放时，播放按钮将被启用。

4.  为按钮、其他控件和显示添加`functions`（函数）和`listeners`（监听器）。

![](img/de30ea99ecac39b49e690a84c48f43b9_208_0.png)

图7.4 在Opera 11中查看带有自定义控件的视频

### 清单7.8 自定义视频控件



```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>7_8 Custom Video Controls</title>
<style>
body {
    font: bold .8em Arial, Helvetica, sans-serif;
}

video {
    display: block;
}

#video-wrapper {
    -moz-box-shadow: 0 0 20px rgba(0, 0, 0, .8);
    -webkit-box-shadow: 0 0 20px rgba(0, 0, 0, .8);
    box-shadow: 0 0 20px rgba(0, 0, 0, .8);
    display: block;
    margin: 20px auto;
    overflow: hidden;
    position: relative;
    width: 568px;
}

#controls {
    background: rgba(0, 0, 0, .3);
    bottom: 0;
    height: 30px;
    left: 0;
    padding: 35px 10px 10px;
    position: absolute;
    width: 548px;
    z-index: 1;
}

button {
    background: rgba(255, 255, 255, .7);
    border: none; -moz-border-radius: 15px;
    -webkit-border-radius: 15px;
    border-radius: 15px;
    cursor: pointer;
    padding: 5px
}

#play {
    width: 70px;
}

#time, #duration {
    color: #fff;
    position: absolute;
    top: 0;
}
#time {
  left: 10px;
}
#duration {
  right: 10px;
  text-align: right
}
input[type="range"] {
  position: absolute;
}
#seekbar {
  top: 8px;
  width: 465px;
  left: 50px;
}
#volume {
  width: 50px;
}
#mute {
  float: right;
  width: 60px;
}
label[for="volume"] {
  color: #fff;
  float: right;
  margin: 5px 55px 0 15px;
}
button.speed {
  font-size: .8em
}
</style>
<script>
var video   = null;
var seekbar = null;
var playBtn = null;

// 初始化页面
function init() {

  // 获取视频容器
  video   = document.getElementsByTagName('video')[0];

  // 引用范围输入控件
  seekbar = document.getElementById('seekbar');
  volume = document.getElementById('volume');

// 设置进度条范围变化处理程序
seekbar.addEventListener('change',seek,false);
volume.addEventListener('change',changeVolume,false);

// 引用按钮
playBtn = document.getElementById('play');
muteBtn = document.getElementById('mute');
rewindBtn = document.getElementById('rewind');
ffBtn = document.getElementById('ff');
fullscreenBtn = document.getElementById('fullscreen');

// 设置按钮点击处理程序
playBtn.addEventListener('click',playPause,false);
muteBtn.addEventListener('click',mute,false);
rewindBtn.addEventListener('click',rewind,false);
ffBtn.addEventListener('click',fastforward,false);
fullscreenBtn.addEventListener('click',fullscreen,false);

// 移除默认的浏览器控件
video.removeAttribute('controls');

// 初始化视频播放器信息
if (video.readyState > 0) {
  var durationText = document.getElementById('duration');
  durationText.innerHTML = (formatTime(video.duration));

  var durationRounded = Math.round(video.duration);
  seekbar.setAttribute('max', durationRounded);

  playBtn.disabled = false;
  seekbar.value = 0;
}

// 视频播放时的监听事件
video.addEventListener('timeupdate', function() {
  var currentTime = document.getElementById('time');
  currentTime.innerHTML = formatTime(video.currentTime);
  seekbar.value = video.currentTime;
}, false);

video.addEventListener('ratechange', function() {
  //你也可以选择显示当前播放速度
  //console.log(video.playbackRate);
}, false);

video.addEventListener('play', function() {
  playBtn.innerHTML = 'Pause';
}, false);
```

## 第7章 使用HTML5嵌入视频

```javascript
video.addEventListener('pause', function() {
  playBtn.innerHTML = 'Play';
}, false);

//检测视频何时结束
video.addEventListener('ended', function(){
  playBtn.innerHTML = 'Play again';
}, false);
}

function playPause() {
  if (ifPlaying()) {
    video.pause();
    playBtn.innerHTML = 'Play';
  } else {
    video.play();
    playBtn.innerHTML = 'Pause';
  }
};

//切换视频的静音状态
function mute(){
  var muteBtn = document.getElementById('mute');
  if (!video.muted){
    video.muted = true;
    muteBtn.innerHTML = 'Un-mute';
  }
  else {
    video.muted = false;
    muteBtn.innerHTML = 'Mute';
  }
}

//更改音量
function changeVolume() {
  video.volume = volume.value;
}

//进度条控制
function seek(){
  video.currentTime = seekbar.value;
}

//快进视频
function fastforward() {
  video.playbackRate = video.playbackRate + 2;
}

//快退视频
function rewind() {
  video.playbackRate = video.playbackRate - 2;
}

//进入全屏模式（仅webkit内核浏览器）
function fullscreen() {
  video.webkitEnterFullscreen()
}

//检查视频是否正在播放
function ifPlaying() {
  if(video.paused || video.ended) {
    return false;
  } else {
    return true;
  }
};

//将时间格式化为易读的形式
function formatTime(seconds) {
  seconds = Math.round(seconds);
  minutes = Math.floor(seconds / 60);
  minutes = (minutes >= 10) ? minutes : '0' + minutes;
  seconds = Math.floor(seconds % 60);
  seconds = (seconds >= 10) ? seconds : '0' + seconds;
  return minutes + ':' + seconds;
}

//页面加载后初始化
window.addEventListener('load',init,false);
```

### 进阶食谱：创建自定义控件

```html
</script>
</head>
<body>
<div id="video-wrapper">
  <div id="controls">
    <button id="play">Play</button>
    <p id="time">0:00</p>
    <p id="duration">0:00</p>
    <label for="volume"> Vol:<input id="volume" name="volume" type="range" min="0" max="1" step="0.1" required /></label>
    <button id="mute">Mute</button>
    <input id="seekbar" name="seekbar" type="range" min="0" max="1" step="0.1" required />
    <button id="rewind" class="speed">Rewind</button>
    <button id="ff" class="speed">Fast-forward</button>
    <button id="fullscreen">Fullscreen</button>
  </div>

  <video width="568" height="320" controls>
    <!-- Safari和IE9的视频。MP4格式必须放在iPad的首位 -->
    <source src="cablecar.mp4" type="video/mp4" />
    <!-- Chrome、Firefox和Opera的视频 -->
    <source src="cablecar.webm" type="video/webm" />
    <source src="cablecar.ogv" type="video/ogg" />
  </video>
</div>
</body>
</html>
```

代码开头是一些用于基本样式和按钮定位的CSS。我们在这里没有使用过多的CSS，但结合CSS和JavaScript API，你几乎可以创建任何你想要的视频播放器布局。

现在来看JavaScript部分。首先，你需要将一些元素关联到变量：视频本身、进度条和播放按钮。对于不使用JavaScript的用户，我们在视频上添加了`controls`属性，所以你需要用JavaScript移除它，因为你不想显示默认控件。

接下来是一个重要的检测。你需要等待浏览器获取到关于视频的足够信息，然后才能开始播放。如果你试图获取视频时长，某些浏览器会失败，因为它们仍在下载视频的部分内容。所以，如果你有一个很大的视频文件，那么你可能需要等待一段时间，浏览器才能准备好播放。在这个食谱中，你检测的是`readyState`的值。`readyState`有五个可能的值：

- `have_nothing` (0)
- `have_metadata` (1)
- `have_current_data` (2)
- `have_future_data` (3)
- `have_enough_data` (4)

`have_nothing`的值表示浏览器没有关于视频的任何信息，而其他值表示浏览器拥有关于视频的各种信息，包括时长、高度和宽度、当前位置以及下一帧。因此，在这个食谱中，你寻找的是`readyState`值大于0的时候，当它大于0时，你检测时长并更新屏幕上的时长值。你还启用了播放按钮，这样用户就可以开始播放视频。在这个食谱中，当视频准备好时，你只做了一些事情，但这可能是在视频上创建控件、显示/隐藏加载图形，或者甚至显示视频本身的时刻。

或者，你可以使用`loadeddata`事件监听器，当浏览器拥有足够的信息以允许播放开始时，它将触发：

`video.addEventListener("loadeddata", function(){//执行操作}, false);`

现在你知道了时长，所以使用`video.duration`，你获得视频片段的总长度，然后可以将其分配给`input[type="range"]`进度条，这样它就有了一个终点。然后你将滑块的起点设置到开始位置（零秒）。

你使用一些`addEventListener`事件来检测视频播放时间何时更新（`timeupdate`），当它更新时，你更新播放显示和进度条。

尽管你已经移除了默认的视频控件，并且拥有了自己的控制按钮（包括播放和静音），但如果用户右键单击视频，根据浏览器的不同，他们可能会在那里看到播放/暂停、显示控件、静音、保存视频等选项。你无法移除或更改这些浏览器默认设置，但你也可以挂钩到这些事件。在这个食谱中，你有代码监听播放或暂停事件，当这些事件发生时，按钮文本会改变。

你还想知道视频何时结束，以便可以更改播放按钮的文本。这个事件很有用，因为当视频结束时，你可以做几件事，例如从播放列表中启动另一个视频。你通过使用事件监听器检测`ended`事件来检测视频结束：

`video.addEventListener("ended", function(){//执行操作}, false);`

在`addEventListener`之后，你有用于其他视频功能的各种函数，例如检查视频是否正在播放；设置音量（`video.volume = volume.value`）；使视频以全屏模式播放（`video.webkitEnterFullscreen()`），这仅在WebKit浏览器中有效；以及检查播放速率（`playbackRate`）。你还添加了播放功能，以便用户可以控制视频的位置和方向：有一个进度条，用户可以跳转到时间线上的某个位置（`video.currentTime = seekbar.value`），以及快进和快退按钮。

正如你已经发现的，浏览器在处理自定义控件时存在各种怪癖：

- 目前，使视频全屏的唯一方法是使用`webkitEnterFullscreen`函数，这目前仅在Safari中有效。从名称可以看出，这不是使视频全屏的标准方式；事实上，规范中可能永远不会有标准方法。但是，浏览器厂商知道这是用户想要的东西，因此未来很可能会有非标准的、特定于浏览器的方法来实现这一点。还有其他方法可以通过结合JavaScript和CSS使视频全屏。然而，几个浏览器在视频本身上右键单击时都有全屏模式。

![图7.5 在Firefox 4中查看带有自定义jQuery控件的视频](img/de30ea99ecac39b49e690a84c48f43b9_216_0.png)

图7.5 在Firefox 4中查看带有自定义jQuery控件的视频

- 目前只有Safari、Chrome和Opera支持`<input type="range">`，并且只有Opera允许此元素拥有透明背景，因此在Chrome中看起来有点丑，而在Safari中它根本不可见。Firefox和IE9默认显示一个文本框，其中显示更新的时间。

- 快进按钮在Firefox中不起作用，在IE9中非常卡顿。快退按钮在任何浏览器中都尚未起作用。

由于浏览器在控件显示以及它们如何与API交互方面存在这种不一致性，你可能需要考虑使用其他控件。例如，在图7.5中，视频控件是使用jQuery滑块创建的。还有其他几个视频播放器可供下载，例如来自http://sublime-video.net和http://videojs.com的播放器。

## 总结

在本章中，你了解了`video`元素的各种问题，例如浏览器支持，但最大的问题是编解码器支持，因此值得密切关注编解码器之争的发展。

但除了编解码器之外，你学习了在所有当前主要浏览器中原生播放视频的方法，而无需像Flash这样的第三方插件。对于不支持`video`元素的旧版浏览器，你可以回退到链接或嵌入的Flash文件。你还使用最新的WebVTT文件标准创建了一个带字幕的视频播放器，尽管这是一个新兴标准，因此请务必关注任何变化和实践。



最后，我们介绍了媒体API的几个组件，可用于创建自定义控件，你可以用CSS来设置它们的样式。

# 使用HTML5嵌入音频

与新的视频元素类似，新的音频元素允许你将音频文件嵌入到页面中，而无需依赖像Flash这样的额外插件。音频现在无需依赖这些第三方插件，即可在现代网络浏览器中播放，包括许多移动设备上的浏览器。

本章，你将学习`audio`元素的基础知识，然后探讨解决跨浏览器兼容性问题的方法。接着，你将了解可用的API，学习如何创建自己的音频播放器。

## 初级配方：使用`audio`元素添加音频

要查看如何使用新的`audio`元素在页面上放置音频的基本示例，请看清单8.1中的代码。代码中添加了`controls`属性；否则，用户界面上将不会显示任何控件。

```
清单 8.1 `audio` 元素基本示例

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>8_1 Basic Audio Example</title>
</head>
<body>
<audio src="music.mp3" controls />
</body>
</html>
```

### 表 8.1 文件类型与浏览器支持

| 编解码器 | Android | Chrome | Firefox | Internet Explorer | iPhone | Opera | Safari |
|---|---|---|---|---|---|---|---|
| Ogg Vorbis | - | 13+ | 4+ | - | - | 11+ | - |
| MP3 | 2.3 | 13+ | - | 9+ | 4+ | - | 5+ |
| WAV | - | - | - | - | - | - | - |

代码本身非常直接，但和视频元素一样，音频元素也存在一些问题。如果你尝试清单8.1中的代码并使用`.mp3`文件，但音频没有播放，这可能是因为你遇到了一些编解码器问题。

我们在第7章更详细地讨论了编解码器困境，虽然那里的信息主要针对视频文件类型，但音频文件类型也面临类似情况。

主要有两种音频编解码器：Ogg Vorbis (`.ogg`) 和 MP3 (`.mp3`)。你也可以考虑WAV (`.wav`)，但我们将主要关注Ogg Vorbis和MP3，因为WAV文件通常很大，不适合在网络上加载；WAV文件也不支持元数据，如艺术家和标题。虽然MP3格式几乎可以被视为标准文件类型，但MP3是MPEG4/H.2.64组的一部分，因此是一种封闭的、需要支付版税的文件类型。另一方面，Ogg被认为是“自由”和“开放”的。毫无疑问，关于哪种文件类型能提供更高质量的音频会有很多争论，但主要问题在于浏览器的支持情况是分裂的。简而言之，表8.1展示了当前的浏览器播放兼容性。

## 中级配方：为所有浏览器启用音频

就像你在第7章为视频所做的那样，你需要在所有现代浏览器中实现音频播放和支持。你可以使用嵌套在`audio`元素中的`source`元素来堆叠不同的音频文件，浏览器会选择它能播放的那一个。清单8.2提供了所需的代码，为现代浏览器提供它们能播放的音频文件。

```
清单 8.2 音频文件堆叠

<audio controls>
  <source src="music.mp3" type="audio/mp3" />
  <source src="music.ogg" type="audio/ogg" />
</audio>
```

音频元素不需要`height`或`width`属性，因为默认情况下每个浏览器都有自己的音频播放器，但你可以使用CSS来应用高度和宽度：

```
audio {display: block; width: 90px; height: 28px;}
```

### 为旧版浏览器添加后备内容

在`source`元素之后，你可以为不能原生播放音频的浏览器编写额外的代码；我们主要谈论的是Internet Explorer 6、7和8。像视频一样，有几个选项。你可以将音频文件托管在类似`http://soundcloud.com`这样的网站上，并使用其嵌入代码来提供音频，或者你可以使用Flash Player将音频内容传递给功能较弱的浏览器。在清单8.3中，我们使用了JW Player，一个非常流行且可定制的多媒体播放器，但还有更多可供选择，或者你可以自己制作一个。

```
清单 8.3 使用 JW Player

<script type="text/javascript" src="swfobject.js"></script>
<div id="mediaplayer"></div>
<script>
  var so = new SWFObject('player.swf','playerID','480','24','9');
  so.addParam('allowfullscreen','true');
  so.addParam('allowscriptaccess','always');
  so.addVariable('file', 'music.mp3');
  so.write('mediaplayer');
</script>
```

只有旧版浏览器会下载`swfobject.swf`和`player.swf`文件，并在Flash Player中播放音频文件。

清单8.4将所有内容整合在一起。这段代码在所有主流浏览器中提供音频，要么使用原生音频元素，要么在必要时使用Flash Player后备方案。

```
清单 8.4 跨浏览器音频

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>8_4 Cross-Browser Audio</title>
</head>
<body>
<audio controls>
  <source src="music.mp3" type="audio/mp3" />
  <source src="music.ogg" type="audio/ogg" />
  <script type="text/javascript" src="swfobject.js"></script>
  <div id="mediaplayer"></div>
  <script>
    var so = new SWFObject('player.swf','playerID','480','24','9');
    so.addParam('allowfullscreen','true');
    so.addParam('allowscriptaccess','always');
    so.addVariable('file', 'music.mp3');
    so.write('mediaplayer');
  </script>
</audio>
<p>下载音频文件: <a href="music.mp3">MP3文件, 3MB</a>; <a href="music.ogg">Ogg文件, 3MB</a></p>
</body>
</html>
```

### 新的音频属性

`audio`元素有几个新的属性，你现在将了解它们。

#### `src`属性

本章开头的清单8.1展示了`audio`元素的基本示例，它包含一个`src`属性。但使用`src`意味着你只能局限于一个音频文件，而且由于编解码器和浏览器问题，它目前几乎没什么用。但理想情况下，有一天它会是你所需要的全部。考虑使用`audio`内的`source`元素，如清单8.4所示，而不是使用`src`，这样你就能让音频跨浏览器工作。

#### `preload`属性

如果页面上有一个相对较大的音频文件，或者你确信用户会想听你嵌入的音频，那么你可以让浏览器在页面加载时就开始下载该文件。`preload`属性有三个可能的值：

```
preload="auto"
    auto，或者你也可以只写 `preload`，告诉浏览器在页面加载时下载音频文件。
preload="none"
    preload="none"告诉浏览器不要下载音频。只有当用户开始播放音频时，它才会开始下载。不过，目前似乎只有Firefox 4支持这一点。
preload="metadata"
    `metadata`属性获取音频轨道的信息（元数据），包括音频时长、第一帧和轨道列表。它不应该在用户启动音频之前下载音频本身。
```

#### `loop`属性

如果`audio`有`loop`属性，那么当音频播放完毕时，它会循环回到开头再次播放。它是一个布尔属性，所以要么开，要么关。所有主流浏览器都支持这个属性，但奇怪的是，Firefox 4除外。

#### `autoplay`属性

一个布尔属性，`autoplay`会强制浏览器在页面加载时开始下载和播放音频。广告经常自动开始播放。关于音频自动播放存在可访问性和可用性方面的担忧，更不用说它可能有多烦人了，但这个属性被包含在规范中是因为，如果你*真的*需要，现在有了一种标准方式来实现它，你不必借助各种JavaScript技巧来达到效果。已经有各种浏览器扩展可供下载来禁用`autoplay`。

> **注意**
>
> `autoplay`和`preload`属性在iOS上已被刻意禁用。这是考虑到对用户可能产生的费用和加载速度问题。在用户启动音频之前，不会下载任何数据。有一些技术，嗯，可以说是“黑科技”，可以绕过这一点。但因为是黑科技，我们并不想在本书中教给你这样的坏习惯。

#### `controls`属性

`controls`属性为你的音频文件添加浏览器特定的控件，包括播放/暂停按钮、搜索栏、时长/已播放时间信息和音量控制。以下是示例：

```
<audio controls>
  . . .
</audio>
```

它是一个布尔属性，所以你要么包含它，要么不包含。但是，如果你不包含`controls`，那么不会显示任何控件，显然用户也就无法控制音频。所以，我们得强调，不使用`autoplay`而同时不使用`controls`是多么重要。

如果你想使用自己的控件，可以通过API来创建停止和开始控件，我们将在本章稍后介绍。图8.1展示了主要浏览器中的默认控件。

> **注意**
>
> 奇怪的是，在Firefox中，如果你没有启用JavaScript，控件就不会出现。其他浏览器则正确地在无JavaScript的情况下显示了控件。

![](img/de30ea99ecac39b49e690a84c48f43b9_221_0.png)

### 用于测试的免费音频文件

出于测试目的，你可能需要一些免费音频文件。有很多选择，但我们可以使用一些来自以下网站的文件：`http://beatstorm.com`、`http://free-soundtrackmusic.com`、`http://vocaldownloads.com` 和 `http://freesound.org`。

这些文件有各种格式，正如你已读到的，你将需要转换它们才能在不同的浏览器中播放。我们建议尝试以下工具：`http://media.io` 或 Free MP3/WMA/OGG Converter，可从 `http://download.cnet.com/Free-MP3-WMA-OGG-Converter/3000-2140_4-10793572.html` 获取。

## 媒体API

HTML5为多媒体提供了一个庞大且令人兴奋的API。使用该API和JavaScript，你可以在网页中操作音频文件。以下是可用的API事件：

| | |
|---|---|
| `abort` | `loadstart` |
| `canplay` | `pause` |
| `canplaythrough` | `play` |
| `canshowcurrentframe` | `playing` |
| `dataunavailable` | `progress` |
| `durationchange` | `ratechange` |
| `emptied` | `seeked` |
| `empty` | `seeking` |
| `ended` | `suspend` |
| `error` | `timeupdate` |
| `loadeddata` | `volumechange` |
| `loadedmetadata` | `waiting` |

以下是可用的媒体属性：

| | |
|---|---|
| `audioTracks` | `muted` |
| `autoplay` | `networkState` |
| `buffered` | `paused` |
| `controls` | `preload` |
| `controller` | `played` |
| `currentSrc` | `playbackRate` |
| `currentTime` | `readyState` |
| `defaultMuted` | `seekable` |
| `defaultPlaybackRate` | `seeking` |
| `duration` | `startOffsetTime` |
| `ended` | `src` |
| `error` | `textTracks` |
| `initialTime` | `videoTracks` |
| `loop` | `volume` |
| `mediaGroup` | |

并非所有这些事件和属性都可供使用，但其中大部分都可用，包括那些允许你创建自己的音频播放器控件的重要API。我们不会解释所有API选项，只会解释创建以下食谱所需的内容。如果你有兴趣了解更多关于API的信息，我们推荐 `http://w3.org/2010/05/video/mediaevents.html` 上的API演示；虽然它是视频演示，但API同样适用于音频。还有非常详细的API规范在 `http://w3.org/TR/html5/video.html#mediaevents`。

## 中级食谱：创建混音器

到目前为止，你已经知道如何在现代浏览器中让音频原生播放。在这个食谱中，你将创建一个混音器，以便测试浏览器如何处理同时播放的多个音频元素。存在一些浏览器怪异行为，因此我们建议为此食谱使用Chrome和Opera。

这个食谱在Safari和Internet Explorer中使用`.mp3`文件，在Chrome、Firefox和Opera中使用`.ogg`文件。我们不关心这个食谱中旧版本的Internet Explorer。这是一个开始使用音频和API的简单食谱。

你将从列表中的六个音频元素开始，尽管理论上你可以动态加载音频文件。使用了一些CSS进行基本布局和样式设置，并且有一个`class`用于音频未播放的情况。对于每个音频元素，都有一个`onclick`事件来切换文件的播放状态。你可以在图8.2中看到该页面，代码在清单8.5中。

![](img/de30ea99ecac39b49e690a84c48f43b9_223_0.png)

图8.2 运行中的混音器，在Firefox中查看

### 清单8.5 创建混音器



```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>8_5 Beat Mixer</title>
<script
src="http://ajax.googleapis.com/ajax/libs/jquery/1.6.1/jquery.min.js">
</script>
<script>
  $(function(){
    $('audio').each(function(index){
      $(this).removeAttr("controls");
      $(this).addClass('stopped');
      var currentTime = $(this).next('div');
      currentTime.html("")
      $(this).click(function() {
        if (this.paused == false) {
          this.pause();
          $(this).addClass('stopped');
          this.currentTime = 0;
        } else {
          this.play();
          $(this).removeClass('stopped');
        }
      });

      this.addEventListener('timeupdate', function() {
        currentTime.html(formatTime(this.currentTime));
      }, false);
    });
  });

  function formatTime(seconds) {
    seconds = Math.round(seconds);
    minutes = Math.floor(seconds / 60);
    minutes = (minutes >= 10) ? minutes : '0' + minutes;
    seconds = Math.floor(seconds % 60);
    seconds = (seconds >= 10) ? seconds : '0' + seconds;
    return minutes + ':' + seconds;
  }
</script>
<style>
* {
  padding: 0;
  margin: 0;
}

ul {
  list-style-type: none;
  margin: 50px auto;
  width: 205px;
}

li {
  float: left;
  margin: 0 0 5px 5px;
}

li:nth-child(odd) {
  clear: both;
  margin-left: 0;
}

p {
  clear: both;
}

audio {
  background: url(images/stop.png) center center no-repeat #ccc;
  -webkit-border-radius: 50px;
  -moz-border-radius: 50px;
  border-radius: 50px;
  -moz-box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.5);
  -webkit-box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.5);
  box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.5);
  cursor: pointer;
  display: block;
  height: 100px;
  margin: 0 0 5px;
  width: 100px;
}

audio.stopped {
  background: url(images/play.png) center center no-repeat #fff;
}

li div {
  clear: both;
  text-align: center;
}
</style>
</head>
<body>

<ul>
  <li>
    <audio controls loop>
      <source src="guitar.mp3" type="audio/mp3" />
      <source src="guitar.ogg" type="audio/ogg" />
    </audio>
    <div></div>
  </li>

  <li>
    <audio controls loop>
      <source src="beat.mp3" type="audio/mp3" />
      <source src="beat.ogg" type="audio/ogg" />
    </audio>
    <div></div>
  </li>

  <li>
    <audio controls loop>
      <source src="turntable.mp3" type="audio/mp3" />
      <source src="turntable.ogg" type="audio/ogg" />
    </audio>
    <div></div>
  </li>

  <li>
    <audio controls loop>
      <source src="clap.mp3" type="audio/mp3" />
      <source src="clap.ogg" type="audio/ogg" />
    </audio>
    <div></div>
  </li>

  <li>
    <audio controls loop>
      <source src="boxingball.mp3" type="audio/mp3" />
      <source src="boxingball.ogg" type="audio/ogg" />
    </audio>
    <div></div>
  </li>

  <li>
    <audio controls loop>
      <source src="synth6.mp3" type="audio/mp3" />
      <source src="synth6.ogg" type="audio/ogg" />
    </audio>
    <div></div>
  </li>
</ul>

<p>音频来自 <a href="http://beatstorm.com">beatstorm.com</a>; <a
href="http://www.vocaldownloads.com">vocaldownloads.com</a>; <a
href="http://www.freesound.org">freesound.org</a></p>
</body>
</html>
```

首先，你隐藏默认控件并使用CSS显示播放按钮。当用户点击一个`audio`元素时，你会检查文件是否已暂停。如果没有暂停，则使用`play`方法开始播放音频。如果文件正在播放，则使用`pause`方法暂停文件。在播放或暂停时，你会切换一个类以显示不同的按钮操作。当你暂停音频时，实际上是通过将其`currentTime`设置回0来停止它。而当音轨播放时，你使用`timeupdate`监听器事件来显示音轨已播放多长时间。

> **混音器的浏览器怪异行为**

这个食谱有一些浏览器怪异行为。首先，Firefox 4不支持`loop`属性，因此音轨不会自动重复，尽管你可以通过JavaScript检测音轨`ended`并再次`play`它来实现这一点。其次，虽然JavaScript在IE9和Safari中可以工作，但这个食谱在这些浏览器中将无法工作，因为这些浏览器尚不支持`audio`元素的样式设置。如果你移除隐藏`controls`属性的代码行，那么它在这些浏览器中就可以正常工作。或者，你可以为`li`设置样式以包含播放/停止图标。

## 高级食谱：添加流媒体广播

到目前为止，在本章中，你已经了解了如何播放“物理”文件（.mp3和.ogg），但流媒体内容呢？传统上，我们总是需要Flash来流式传输音频，但现在你可以原生地实现了。在这个食谱中，你将使用一个公开可用的广播流的JSON列表。使用API事件，包括`onerror`、`play`和`volume`，用户可以从下拉列表中选择一个流，它将开始播放。这有多酷？这是在浏览器中的网络广播，无需任何插件。你可以在图8.3中看到播放器的预览，此食谱的代码在清单8.6中。

这些流采用OGG或MP3格式，OGG流将在Firefox、Opera和Chrome中工作。MP3流将在Chrome、IE9和Safari中工作。如果浏览器不支持该格式，则会显示错误消息。

1. 使用HTML和CSS创建播放器的布局和控件。

2. 创建一个基于JSON的广播电台及其URL列表。

3. 如果有错误，则使用API检测错误类型。

4. 将每个电台作为选项添加到电台列表中。

5. 当选择一个电台时，触发函数`setStation`，该函数更改音频元素的`src`并立即开始播放。

# 第8章 使用HTML5嵌入音频

![HTML5音频流播放器，在Chrome浏览器中查看](img/de30ea99ecac39b49e690a84c48f43b9_228_0.png)

图8.3 HTML5音频流播放器，在Chrome浏览器中查看

### 清单8.6 流媒体电台播放器



```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>8.6 Streaming Radio Player</title>
<script>
// local variables for elements
var radioPlayer;
var radioStatus;
var radioControls;
var volumeControl;
var buttonPlayPause;

// Define our JSON list of stations
var stations = { "entries":[
    {"name":"Absolute Radio Classic Rock",
    "url":"http://ogg2.as34763.net/vc160.ogg",
    "type":"ogg"},
    {"name":"Absolute Radio DAB",
    "url":"http://ogg2.as34763.net/vr160.ogg",
    "type":"ogg"},
    {"name":"Absolute Radio 80s",
    "url":"http://ogg2.as34763.net/a8160.ogg",
    "type":"ogg"},
    {"name":"Absolute Radio 90s",
    "url":"http://ogg2.as34763.net/a9160.ogg",
    "type":"ogg"},
    {"name":"BBC World Service",
    "url":"http://vprbbc.streamguys.net:80/vprbbc24.mp3",
    "type":"mp3"},
    {"name":"Classic FM London",
    "url":"http://media-ice.musicradio.com:80/ClassicFMMP3",
    "type":"mp3"},
    {"name":"Rainwave",
    "url":"http://stream.gameowls.com:8000/rainwave.ogg",
    "type":"ogg"},
    {"name":"SomaFM",
    "url":"http://streamer-ntc-aa06.somafm.com:80/stream/1018",
    "type":"mp3"},
    {"name":"VoxNoctem",
    "url":"http://voxnoctem.de:9113/high.ogg",
    "type":"ogg"},
    {"name":"WBUR-Boston",
    "url":"http://wbur-ogg.streamguys.com:80/wburlive.ogg",
    "type":"ogg"},
    {"name":"WCLV",
    "url":"http://auggie.wclv.com:80/hi.ogg",
    "type":"ogg"},
    {"name":"WCPE-Classical",
    "url":"http://audio-ogg.ibiblio.org:8000/wcpe.ogg",
    "type":"ogg"}
  ]})

// Initialization function
function init() {

  // set reference to the audio element
  radioPlayer = document.getElementById('audioPlayer');

  // set error handler
  radioPlayer.onerror = function(evt) {
    switch (radioPlayer.error.code) {
      case radioPlayer.error.MEDIA_ERR_ABORTED:
        alert('Play has been aborted.');
        break;
      case radioPlayer.error.MEDIA_ERR_NETWORK:
        alert('Network error occurred.');
        break;
      case radioPlayer.error.MEDIA_ERR_DECODE:
        alert('Error occurred while decoding stream.');
        break;
      case radioPlayer.error.MEDIA_ERR_SRC_NOT_SUPPORTED:
        alert('Media resource provided is not suitable.');
        break;
      default:
        alert('Unknown error occurred: '+radioPlayer.error.code+'.');
        break;
    }
  }

  // set listener for durationchange event
  radioPlayer.addEventListener('durationchange', streamPlaying, false);

  // set references to elements
  radioStatus = document.getElementById('radioStatus');
  radioControls = document.getElementById('radioControls');
  volumeControl = document.getElementById('volumeControl');
  buttonPlayPause = document.getElementById('buttonPlayPause');

  // set the default volume
  setVolume(0.7);

  // load the station list
  loadStations();
}

// Load the stations from JSON variable
function loadStations() {

  // reference the station list select element
  var stationList = document.getElementById('stationList');

  // loop through JSON stations and create list
  for(i=0;i<stations.entries.length;i++) {
    // create option with text and value
    var newOption = document.createElement('option');
    newOption.text = stations.entries[i].name + ' ('+stations.entries[i].type+')';
    newOption.value = i;

    // add the new option to the list
    try {
      stationList.add(newOption, null);
    } catch(ex) {
      // IE only
      stationList.add(newOption);
    }
  }
}

// Set the station selected
function setStation() {

  // update status
  radioStatus.innerHTML = 'Buffering...';

  // set the source and type for the audio element
  var selStationList = document.getElementById('stationList');
  radioPlayer.src = stations.entries[selStationList.selectedIndex].url;
  radioPlayer.type = 'audio/' + stations.entries[selStationList.selectedIndex].type;

  // display selected to user
  var currentStation = document.getElementById('currentStation');
  currentStation.innerHTML = stations.entries[selStationList.selectedIndex].name;

  // tell audio element to play
  radioPlayer.play();
}

// Stream now playing
function streamPlaying() {

  // update display and show player controls
  radioStatus.innerHTML = 'Now playing...';
  buttonPlayPause.innerHTML = 'Pause';
  radioControls.style.visibility = 'visible';
}

// play / pause functions
// play / pause button click handler
function playPauseClicked() {
  // check if playing or paused
  if (radioPlayer.ended || radioPlayer.paused) {
    // player is paused, now play
    playerPlay();
  } else {
    // player is playing, now pause
    playerPause();
  }
}

// restart play of player
function playerPlay() {

  // update status
  buttonPlayPause.innerHTML = 'Pause';
  radioStatus.innerHTML = 'Now playing...';

  // restart play of player
  radioPlayer.play();
}

// pause player
function playerPause() {

  // update status
  buttonPlayPause.innerHTML = 'Play';
  radioStatus.innerHTML = 'Paused';

  // pause player
  radioPlayer.pause();
}

// volume control functions
// set the volume
function setVolume(newVolume)
{
  // set the volume
  radioPlayer.volume = newVolume;

  // update volume bar size
  wrapper = document.getElementById('volume_background');
  wrapper_width = wrapper.offsetWidth;
  newWidth = wrapper_width*newVolume;

  volume_bar = document.getElementById('volume_bar');
  volume_bar.innerHTML = parseInt(newVolume*100) + '%';
  volume_bar.style.width=newWidth+'px';
}

// handler for clicking of volume bar
function volumeChangeClicked(event)
{
  //get the position of the event
  var clientX = event.clientX;
  var offset = clientX - event.currentTarget.offsetLeft;
  var newVolume = offset/event.currentTarget.offsetWidth;
  setVolume(newVolume);
}

// initialize on load
window.addEventListener('load',init,false);

</script>
<style>
* {
  color: #000;
  font-family: "Lucida Sans Unicode", "Lucida Grande", sans-serif;
  margin: 0;
  padding: 0;
}

#radioContainer {
  background-color: #ccc;
  border: 15px solid rgba(0,0,0,.5);
  -moz-border-radius: 25px;
  -webkit-border-radius: 25px;
  border-radius: 25px;
  -moz-box-shadow: 0px 0px 4px #000;
  -webkit-box-shadow: 0px 0px 4px #000;
  box-shadow: 0px 0 35px rgba(1, 1, 1, 0.7), inset 0px 0 35px rgba(1, 1, 1, 0.7);
  padding: 20px;
  margin: 40px auto;
  overflow: hidden;
  width: 420px;
}

h1 {
  font-size: 1.8em;
  margin: 0 0 10px;
  text-align: center;
}

h2 {
  margin: 10px 0 5px;
}

label {
  left: -9999px;
  position: absolute;
}

#stationList {
  background-color:#fff;
  border: 1px solid #000;
  -moz-border-radius: 5px;
  -webkit-border-radius: 5px;
  border-radius: 5px;
  color:#333;
  cursor: pointer;
  padding: 5px;
  text-align: center;
  width: 100%;
}

#radioPlayer {
  float: left;
  width: 100%;
}

#currentStation {
  color:#333;
  text-shadow:#999;
}

#radioControls {
  text-align:left;
  visibility:hidden;
  margin-top:10px;
}

#radioControls * {
  float: left;
}

#volumeControl {
  border: 1px solid #fff;
  cursor: pointer;
  float:left;
  height: 25px;
  margin: 0 5px;
  position:relative;
  width:60px;
}

#volume_background {
  background-color:#ccc;
  height:25px;
  width:60px;
}

#volume_bar {
  background:#fff;
  color:#333;
  height:25px;
  position:absolute;
  text-align:center;
  width:0px;
}

button {
  background: #fff;
  border: none;
}
</style>
```

## HTML5 音频流播放器

页面加载时，`init()`函数会运行。该函数通过设置音频播放器以便后续引用和操控来启动整个流程，同时也会设置播放和音量控制等其他控件。随后，它使用`loadStations()`函数加载电台。该函数遍历电台的 JSON 列表，并生成供用户选择的列表。`select`元素的`onChange`事件绑定了`setStation()`函数，该函数会获取选中的电台，将其 URL 设为音频的`src`，并修改音频的`type`属性（设为 MP3 或 OGG），以确保其正确播放。如果浏览器无法播放该音频类型（例如，由于 MP3 格式限制，BBC World Service 在 Firefox 或 Opera 中无法播放），则会弹出错误提示，错误文本取决于具体的错误类型。

即使设置了播放器的源地址，除非明确调用`radioPlayer.play()`，否则音频不会播放。当流媒体正在播放时，会触发一个名为`durationchange`的监听事件。当此事件发生时，会启动一个名为`streamPlaying()`的函数，该函数更新屏幕上正在播放的电台文本；将播放按钮切换为暂停按钮；并显示其余的控件。



最后的控件涉及播放/暂停按钮和音量控制。点击播放/暂停按钮时，会运行一个函数来检查当前状态：如果音频处于暂停或结束状态，则触发`.play()`；否则触发`.pause()`。在上一章关于视频的内容中，你使用了新的 HTML5 `range` 输入元素作为音量控件。在这里，你创建了一个跨浏览器兼容的版本，它能检测音量条被点击的位置，并通过`.volume`来更新音频的音量。

## 总结

在本章中，你学习了如何在浏览器中播放音频文件，而无需依赖第三方插件（通常是 Flash）。当然，由于这是一个新的浏览器特性，在不同浏览器中存在各种兼容性问题。与`video`元素一样，你需要处理编解码器问题，但你可以为旧版浏览器提供备用选项。

你还了解了新 API 的各种元素，这些元素允许你操控音频文件在浏览器中的行为，包括控制播放和暂停、控制音量以及更改播放的文件。

# 9 更改浏览器历史记录

本章讨论 HTML5 中历史记录接口的更新，特别是 History API 中的两个新方法（`pushState`和`replaceState`），并包含若干将它们融入会话导航的实用方案。此外，你将了解`state`事件、使用 History API 存储超出页面导航范围的信息，以及诸如安全性和扩展库等高级主题。

## History 基础

History API 是一个 JavaScript API，自 JavaScript 1.0 起就已在网站中使用，但在 HTML5 之前并未进行重大更新。随着 Ajax 和无页面导航的兴起，使用`history`对象进行前进、后退或跳转到特定会话条目变得存在问题。事实上，包括 YUI 在内的几个框架都引入了自己的浏览器会话管理技术。

以前，要在不实际更改页面的情况下向浏览器历史记录添加页面，你需要通过在 URL 后添加`#`符号和哈希值来更改 URL。使用`history.pushState`和`history.replaceState`方法，你现在可以分别添加和修改历史记录，并且当它们与`window popstate`事件结合使用时，可以为用户提供改进的导航体验。通过公开向网站添加和修改页面历史记录的能力，History API 为使用 Ajax 技术的富应用程序提供了更好的后退按钮支持。你现在只需将一个虚拟页面或上下文推入历史记录，即可更改应用程序的“视图状态”。

你可以将浏览器会话历史记录，即用户在你网站中浏览过的页面，视为一个栈。当页面被查看时，它们被推入栈顶。当用户点击或点击浏览器的后退按钮时，页面会逐一从栈中“弹出”。仅使用 JavaScript，你可以使用以下命令前进、后退或前进/后退特定数量的页面：

- `window.history.forward`
- `window.history.back`
- `window.history.go([delta])`

这些方法在 History API 中仍然可用，但除此之外，你现在可以动态添加历史记录、捕获导航事件，甚至通过 HTML5 History API 控制页面的上下文。

### 浏览器兼容性

History API 扩展目前在表 9.1 所列的浏览器平台上受支持。

### 表 9.1 History API 浏览器兼容性

| 浏览器 | 版本 |
| :--- | :--- |
| Android | 2.2+ |
| Chrome | 5.0+ |
| Firefox | 4.0+ |
| Internet Explorer | - |
| iOS Safari | 3.0+ |
| Opera | 11.0+ |
| Safari | 5.0+ |

## 初学者指南：使用 pushState 添加历史记录

你可以使用 History API 的`pushState`方法，通过当前浏览器页面向浏览器会话栈添加一个新条目。该方法接受两个参数：`data`和`title`，以及一个可选的第三个参数`url`：

`history.pushState(data, title [,url])`

`pushState`方法的参数如下：

- `data`：传递的一个字符串或对象，用于表示页面的状态。
- `title`：显示在浏览器标题栏中的页面标题字符串。
- `url`：（可选）要添加到历史记录栈的新 URL。

`data`参数表示页面的状态，并自动与新条目关联。稍后你将看到，可以通过窗口的`popstate`事件来检索它。这里的*状态*，我们指的是页面显示的当前上下文。例如，这可以是用户当前通过 Ajax 等方式从数据库调用查看的菜谱。

某些浏览器对`data`参数的大小施加限制，因为状态对象由浏览器本地存储在用户的磁盘上。在 Firefox 中，此限制是状态对象序列化表示的 640,000 个字符。如果你计划达到或可能达到此限制，你应该改用`sessionStorage`或`localStorage`（参见第 11 章，客户端存储）。

> 注意
>
> 某些浏览器，如 Firefox，会忽略`title`参数，并且不会在用户的会话历史列表中显示该值。这是浏览器特定的，我们希望在未来的更新中能得到修正。

如果提供了`url`参数，这将替换浏览器地址栏中的 URL，但不会导致浏览器从网站请求该页面。这允许用户将 URL 加入书签并在以后返回。当然，你需要在服务器端页面上设置逻辑，以处理那些不代表真实页面的书签地址。传递的 URL 可以是相对路径或绝对路径；但是，路径必须与当前 URL 在同一域中。如果使用相对路径，则路径将基于当前文档的位置。如果不包含`url`参数或仅提供查询字符串（例如`"?page=5"`），则默认路径是文档的当前 URL。

`pushState`方法类似于使用哈希值来控制页面上下文，这在基于 Ajax 的动态应用中很常见：

`window.location = "#foo";`

然而，`pushState`方法比哈希访问提供了更大的灵活性：

- `pushState`允许你保持在同一页面或更改 URL。使用哈希方法时，浏览器保持在同一 URL。
- `pushState`允许你在历史记录的状态中保留上下文信息。正如你稍后将在本章中看到的，这非常有用。

最后一点需要强调，因为它是对 URL 添加哈希方法的重大改进。历史记录中的每个条目，`pushState`允许你存储一个数据对象，该对象可以保存关于页面状态的上下文信息。数据可以简单如字符串值，也可以复杂如序列化的 JSON 对象。例如，假设你有一个展示演示文稿幻灯片的页面。每张幻灯片可能有关于如何显示的详细信息，例如副标题、边框、致谢等。状态对象可以保存这些信息，从而轻松根据你所在的幻灯片更改页面样式。你将在本章后面看到一个利用此状态对象的方案。

让我们使用历史记录的`pushState`方法向历史会话添加一个新条目。页面在加载时通过调用`typeof`检查`history.pushState`方法来检测浏览器中 History API 的可用性。如果该方法返回`"undefined"`，则浏览器不支持 History API。你可以使用此

## 9.1 修改浏览器历史记录

我们需要根据用户当前使用的浏览器，采用不同的方法来实现历史记录或限制功能：

1. 创建一个空白的HTML页面，其中包含一个用于显示当前展品的`div`。
2. 添加一个按钮，点击该按钮将启动JavaScript函数`nextExhibit`。
3. 插入`nextExhibit`函数来执行`pushState`方法。
4. 添加`pushState`方法调用，将狐獴展品的上下文添加到历史记录中：

   `history.pushState('Meerkat','Meerkat Exhibit','meerkats.html');`

5. 更新展品`div`，告知用户当前处于狐獴展区：

   `document.getElementById("exhibit").innerHTML = "At the Meerkats.";`

清单9.1包含了整个页面的代码。

### 清单9.1：使用 pushState 将页面添加到历史记录

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>9_1 At the Zoo</title>
</head>
<body>
<script>
// initialize the button handler
function init() {
  // attach the click button handler
  var btnNextExhibit = document.getElementById('btnNextExhibit');
  btnNextExhibit.addEventListener('click',nextExhibit,false);
}

function nextExhibit() {
  // Check to see if the history pushState API is available

  if (typeof history.pushState !== "undefined") {
    // Execute the pushState method

    history.pushState('Meerkat','Meerkat Exhibit','meerkats.html');

    document.getElementById("exhibit").innerHTML = "At the Meerkats.";

  } else {

    // the History API is not available
    alert('The History API is not available in this browser.');

  }
}
</script>

// Add the listener to initialize the page
window.addEventListener('load',init,false);

</script>
Welcome to the zoo.
<div id="exhibit">You are at the Zoo entrance.</div>
<button id="btnNextExhibit">Visit the Meerkats</button>
</body>
</html>
```

当你在浏览器中加载此页面时，根据页面标题和显示的消息，你会看到你位于动物园入口。如果点击“参观狐獴”按钮，页面会将当前页面推入历史记录，然后更改浏览器窗口的标题和URL，而无需实际导航到新页面。JavaScript会更改消息，告知用户狐獴展区的信息。从所有目的来看，用户会感觉是从服务器加载了一个新页面。然而，这仅仅是通过`pushState`添加到历史记录中的一个新上下文。

> **提示**
>
> 在某些情况下，如果在`pushState`中提供的`url`参数值指向一个无效页面，可能会在某些浏览器（如 Firefox）中导致安全异常。要解决此问题，请提供一个有效的 URL 或使用可选的`state`参数，这样可以避免异常。

如果你查看浏览器的历史记录列表，你会看到“在动物园”页面是最后一个页面，如果点击返回按钮，你将返回到该页面。页面上的消息不会变回“在动物园入口”，但你稍后将了解如何修复此问题。请记住，URL是可选的，但对于回访用户来说可能非常有用。当然，你需要在服务器上设置逻辑来处理那些在服务器上没有真实页面的书签条目。

## 初级配方：创建图片查看器

在前一个配方中，你完成了第一个`pushState`调用，将一个简单条目推入了历史会话。此配方将更进一步，为用户提供多个选择选项，并将每个选择存储到不断增长的历史会话中。有许多网站允许用户通过提供缩略图链接并动态替换所选内容来浏览一系列照片、视频或其他内容。在此配方中，你将向用户展示一系列图片缩略图，允许他们选择一张图片进行查看，并添加一个新的历史记录条目来跟踪已查看的内容，并允许用户返回到这些图片。清单9.2显示了使用历史记录条目创建图片查看器的完整页面代码。代码清单中引用的图片和其他资源可从本书网站获取。请将图片放入`images`文件夹中，以便在代码的`showImage`函数中正确引用。

### 清单9.2：图片查看器：创建多个历史记录条目

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>Image 1</title>
<style>
div.imgView { height: 300px; }
div.imgView img { height: 300px; }
div.imgRow img { height: 100px; }
a { cursor: pointer }
</style>
</head>
<body>
<script>
// variable to keep track of the current image
var currentImg = 1;

// navigate to the next slide
function showImage(imgNum) {

  // check if the History API is available
  if ( typeof history.pushState !== "undefined" ) {

    // verify the image selected is not the current one
    if (currentImg != imgNum) {

      // set the image title
      var imgTitle = 'Image ' + imgNum;

      // set next slide in history entries with state object and defaults
      history.pushState( imgNum, imgTitle, '?img=' + imgNum );
      document.getElementById('imgSlide').src = 'images/slide' + imgNum + '.jpg';
      document.getElementById('imageInfo').innerHTML = imgTitle;

      // set the current page title
      document.title = 'Image ' + imgNum;
      var stateInfo = document.getElementById('stateInfo')
      stateInfo.innerHTML = imgTitle + "<br>" + stateInfo.innerHTML;

      // set the current image to the image selected
      currentImg = imgNum;
    }
  } else {
    // History API is not available
    alert('The History API is not available in this browser.');
  }
}
</script>

<!-- image view and title - set to first image -->
<div id='imgView' class='imgView'><img id='imgSlide' src="images/slide1.jpg"
style='height:300px'></div>
<div id='imageInfo'>Image 1</div>

<!-- thumbnail image row -->
<div id='imgRow' class='imgRow'></div>
<script>
// create row of img links
var newImg;
var imgRow = document.getElementById('imgRow');
for (var i=1; i<=5; i++ ) {
  newImg = '<a onclick="showImage('+i+');"><img class="thumbnail"
src="images/slide'+i+'.jpg"></a>';
  imgRow.innerHTML += newImg;
}
</script>

<!-- history state display area - set to first image (page when loaded)-->
<div id='stateInfo'>Image 1</div>
</body>
</html>
```

如果你运行前一个配方并选择缩略图进行查看，你会看到条目被推入浏览器的历史记录，就好像浏览器加载了单独的页面一样。在图9.1中，我们选择了图片3、5、4和2。左侧图表显示了浏览器后退按钮的下拉菜单；右侧显示了选择图片后页面上为用户选择的图片显示的内容。请注意“Image 1”位于列表底部，因为这是HTML页面的原始标题。从第一张图片开始，你动态创建的标题被添加到历史记录列表中。最后选择并当前显示的图片（Image 2）未在历史记录中列出，因为这是当前上下文。

![图9.1](img/de30ea99ecac39b49e690a84c48f43b9_244_0.png)

*图9.1：后退按钮下拉列表中的历史记录与我们的选择匹配。*

> **注意**
>
> 在前面的清单中，我们使用内联脚本在页面加载时创建缩略图按钮。通常，这会通过像 jQuery 这样的框架中的`domReady`事件来处理。为了节省空间并保持代码无关性，我们使用了内联脚本。

当你运行此配方时，你会注意到，如果你在浏览器中点击后退按钮，`pageInfo` div中的页面列表保持不变。如果你能在用户点击后退按钮时捕获一个事件来更新显示的页面，那不是很好吗？HTML5正好为此提供了`popstate`事件，这将在下一个配方中介绍。

## 中级配方：在图片查看器中弹出状态



为了与 History API 的新方法配合工作，HTML5 定义了一个新的窗口事件，称为`popstate`。当浏览器窗口的活动历史记录会话条目发生更改时，将触发此事件。历史记录条目可能由于用户点击浏览器的前进或后退按钮，或者调用 JavaScript history 对象的`back`和`go`等方法而发生更改。在任何一种情况下，你都可以基于事件处理程序执行逻辑来捕获此事件。事件处理程序的语法在 JavaScript 中采用以下格式：

```javascript
window.addEventListener('popstate',funcRef,false);
```

`popstate`事件通过`popstate`事件在 JavaScript window 对象上触发，并与一个处理函数相关联，在上一行中引用为`funcRef`。因此，当用户使用后退按钮浏览历史记录时，你可以执行任何必要的逻辑，以便在页面 HTML 中加载正确的上下文。你会记得在`pushState`调用中，对于推送的每个条目，你可以存储该条目的数据或状态。`popstate`事件将你存储的状态传递给事件处理程序，并允许脚本访问状态对象。你可以通过访问事件的只读属性`event.state`来使用此状态数据。

## 图像查看器：捕获弹出状态事件

在清单 9.2 中，你创建了一个简单的图像查看器，允许用户选择缩略图。选中后，图像会加载到查看区域，并将一个新的页面条目推入历史记录。然而，除非你能在用户使用浏览器后退按钮导航或脚本调用`history.back`或`history.go`时显示正确的图像，否则历史记录中的页面并无益处。在这个配方中，你将添加弹出状态事件处理器来捕获导航事件，并加载正确的图像和详情。

将清单 9.3 中的高亮代码部分添加到清单 9.2 的现有脚本行之间，如下所示。

```
...

<script>

// 设置弹出状态页面处理器
window.addEventListener('popstate', popPage, false);

// 用于跟踪当前图像的变量
var currentImg = 1;

// 历史记录弹出状态事件处理函数
function popPage(event) {

    // 从历史记录中获取状态
    currentImg = event.state;

    // 设置图像和标题
    var imgTitle = 'Image ' + currentImg;
    document.getElementById('imgSlide').src = 'images/slide' + currentImg + '.jpg';
    document.getElementById('imageInfo').innerHTML = imgTitle;
    document.title = imgTitle;

    // 显示我们弹出了一个历史事件以及弹出的状态
    var stateInfo = document.getElementById('stateInfo')
    stateInfo.innerHTML = 'History popped : ' + imgTitle + ' : state: ' + JSON.stringify(event.state) + "<br>" + stateInfo.innerHTML;

}

// 导航到下一张幻灯片
function showImage(imgNum) {
...
```

![图 9.2 历史记录状态的推入和弹出](img/de30ea99ecac39b49e690a84c48f43b9_246_0.png)

**图 9.2 历史记录状态的推入和弹出**

在代码中加入清单 9.3 的事件处理函数后，运行代码。当页面加载时，选择第二个缩略图，然后选择第三个缩略图。这会对每个选择执行`pushState`，将它们添加到历史记录条目列表中。通过添加之前的弹出状态事件处理器，每当用户在浏览器中点击后退或前进按钮时，你都可以捕获该事件，然后根据事件上存储的状态为用户加载正确的图像。

现在点击浏览器的后退按钮。`popstate`事件处理器将被调用。你首先会通过将事件状态分配给当前图像来检索状态，然后用它来显示正确的图像并设置标题。为了验证，你随后会更新`stateInfo` div，以便你可以看到历史记录中弹出了什么（参见图 9.2）。

请注意，即使从浏览器的历史记录下拉菜单中选择其中一个条目，也会触发该事件。尝试使用代码，看看`pushState`和`popstate`事件如何处理历史记录遍历。

> **提示**

> 用户可以通过历史记录菜单或脚本中的 history API 命令（如`go`和`back`）在浏览器历史记录中向后导航任意步数。最好将历史记录条目的数据元素与一个能让你确切知道条目上下文的键关联起来。例如，这可以是项目的唯一编号、幻灯片编号或其他唯一索引。这样，当处理`popstate`事件时，代码将确切知道要处理哪个元素，而不仅仅是最后访问的那个。

## 初级配方：使用 replaceState 更改历史记录

History API 的`replaceState`方法用于用新条目替换浏览器历史记录中的当前条目。参数与`pushState`相同：data、title 和一个可选的 URL 字段。`replaceState`方法在更新历史记录条目的状态（随着上下文变化）或设置页面的初始状态时很有用。`replaceState`方法采用以下形式：

```
history.replaceState(data, title [, url])
```

当页面在浏览器中全新加载时，标题和 URL 会存储在历史记录条目中。但是，没有上下文数据与这些信息一起存储。要将数据与标题和 URL 一起存储，你可以在页面加载时调用`replaceState`，使用相同的标题、URL 以及你的额外状态数据存储在历史记录条目中。这本质上将用相同的页面信息和你的额外数据覆盖当前条目。页面加载后，用户可以改进搜索结果，例如，在每次改进之后，你可以使用`replaceState`方法替换存储的设置。

这个配方使用`replaceState`来演示页面如何不重新加载，而是改变当前历史记录条目的状态。页面加载后，用户可以点击一个按钮，该按钮用更新的计数器替换当前状态（键为 "page"，值为 idxCounter）。每次替换状态时，计数器只是递增。要构建清单 9.4 中的页面，请按照以下步骤操作：

1. 创建一个空白 HTML 页面，包含一个空的`stateInfo` div。这将用于查看你每次设置的内容。

2. 添加一个按钮，当点击时，启动一个名为`nextState`的 JavaScript 函数。

3. 插入包含`history.replaceState`的`nextState`函数：

   `history.replaceState({page: idxCounter}, "page "+idxCounter, "?page="+idxCounter);`

4. 在`nextState`中更新`stateInfo` div，显示`replaceState`已执行，并递增`idxCounter`计数。

```
清单 9.4 替换当前状态

<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>Page</title>
<script>
var idxCounter = 1; // 用于跟踪页面状态的计数器

// 初始化按钮处理器
function init() {
 // 附加点击按钮处理器
 var btnNextState = document.getElementById('btnNextState');
 btnNextState.addEventListener('click', nextState, false);
}

// 我们的 replaceState 包装函数
function nextState() {

 // 用下一个替换当前页面
 history.replaceState({page: idxCounter}, 'page '+idxCounter, '?page=' + idxCounter);

 // 更新我们的页面状态 div
 var strStateInfo = document.getElementById('stateInfo').innerHTML;
 document.getElementById('stateInfo').innerHTML = strStateInfo +
  '<br>Replaced state ' + idxCounter;

 // 递增我们的计数器
 idxCounter++;
}

// 添加监听器以初始化页面
window.addEventListener('load', init, false);

</script>
</head>
<body>
<button id="btnNextState">Replace State</button>
<div id="stateInfo"></div>
</body>
</html>
```

每次点击 "Replace State" 按钮时，你会注意到可以验证状态正在被替换，因为 URL 会显示你添加的查询字符串：`page=<idxCounter>`。如果你查看浏览器后退按钮的历史记录下拉菜单，你还会注意到每次调用`replaceState`时，都不会向堆栈添加新的历史记录条目。请注意，你在`replaceState`中为状态使用了不同样式的数据。你使用了一个 JSON 风格的序列化对象，键为`page`，值为`idxCounter`。对于 push 或 replace 的 data 元素，你不仅限于字符串，还可以存储复杂的对象。

## 中级配方：更改页面历史记录

下一个配方在页面加载时对浏览器历史记录执行多个操作，采用`pushState`、`replaceState`以及`back`和`forward`方法。`popstate`事件用于显示当使用历史记录方法时事件何时被触发。清单 9.5 显示了该配方的代码。

**清单 9.5 推入和弹出**

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>Page</title>
<script>
// popstate 事件处理函数
function popPage(event) {
  var strState = 'POP - location: ' + document.location + ', state: ' +
JSON.stringify(event.state);
  document.getElementById('stateInfo').innerHTML += strState + '<br>';
};

function loadPages() {

  logAction('pushing page 1');
  history.pushState({page: 1}, 'page 1', '?page=1');

  logAction('pushing page 2');
  history.pushState({page: 2}, 'page 2', '?page=2');

  logAction('replacing page 2 with page 3');
  history.replaceState({page: 3}, 'page 3', '?page=3');

  logAction('taking one step back');
  history.back();

  logAction('taking one step back again');
  history.back();

  logAction('taking two steps forward');
  history.go(2);

}

function logAction(strAction) {
  document.getElementById('stateInfo').innerHTML += strAction + '<br>';
  alert(strAction);
}

// 添加我们的窗口事件监听器
window.addEventListener('popstate', popPage, false);
window.addEventListener('load', loadPages, false);

</script>
</head>
<body>
<div id="stateInfo"></div>
</body>
</html>
```

加载时，脚本调用`loadPages`函数，该函数推入两个后续页面，执行一次`replaceState`，执行两次 history back 命令，并

## 第9章 更改浏览器历史记录

然后在历史记录中前进两步。以下是该方法在 Firefox 浏览器窗口中的输出结果：

```
pushing page 1
pushing page 2
replacing page 2 with page 3
taking one step back
POP - location: 9_4_page_flow.html?page=1, state: {"page":1}
taking one step back again
POP - location: 9_4_page_flow.html, state: null
taking two steps forward
POP - location: 9_4_page_flow.html?page=3, state: {"page":3}
```

在推入页面 1 和页面 2 之后调用了`replaceState`，因此浏览器历史记录中只剩下页面 1 和页面 3，其中页面 3 是当前状态。现在历史记录堆栈中已有一些条目，你可以通过调用`history.back`来回退。调用`history.back`会触发 popstate 事件，使你返回到页面 1。再次调用`History.back`，会带你回到没有状态的原始页面。请注意，状态为 null，因为该页面是通过浏览器加载的，而非通过 pushState 或 replaceState。

最后，你执行了`history.go`，在浏览器堆栈中向前移动了两个页面。这通过从原始页面跳转到页面 1，然后再到页面 3（因为页面 2 之前已被页面 3 替换），将你带回到了页面 3。这可能会让人感到困惑，你可能会发现在弹出警告框时，在纸上画出这个过程会更容易理解。我们发现最简单的方法是绘制一个由块组成的塔，每个块代表一个推入的条目。替换一个条目就是替换一个块，而在历史记录中导航则只是将当前指针移动到堆栈中的某个块（参见图 9.3）。

需要注意的是，`popstate`事件在窗口的`onload`事件触发之后才会触发。如果在窗口的`onload`事件之前调用了通常会触发`popstate`事件的方法，那么通常只有最后一个`popstate`事件会在浏览器中被触发。

> **提示**

> 本方法演示了在`pushState`执行后，`replaceState`方法如何替换页面的状态。如你所见，原始页面的状态为 null，因为原始页面是通过浏览器加载的，而非通过`pushState`。如果你需要为原始页面关联一个状态，请在页面加载时执行`replaceState`来关联你的状态数据。

![](img/de30ea99ecac39b49e690a84c48f43b9_250_0.png)

## 高级方法：使用高级状态数据对象在页面间传递信息

根据`pushState`和`replaceState`方法的语法，第一个参数可以接受字符串或对象作为表示页面状态的数据。到目前为止，你只为数据参数传递了字符串或一个小型键值对象。在许多情况下，页面上下文的更多详细信息最好能与历史记录条目一起保存，这样当用户返回该页面时，你可以直接渲染内容，而无需在浏览器外部调用获取信息。

可以通过 JSON 表示法将对象传递给这些方法，如以下示例所示，其中包含一个 JSON 格式的变量：

```
var stateObj = { page: 1 };
history.pushState(stateObj, 'Title 1', 'page1.html');
```

以下代码展示了如何传递更复杂的对象：

```
var stateObj = { page: 1, title: "My Slide #1", author: "Savel"};
history.pushState(stateObj, 'Slide 1', 'slide1.html');
```

状态数据对象是存储用户在页面上执行的选项、操作或偏好设置的好方法，这些数据随后会与历史记录条目一起被存入。不过请注意，如果用户清除了浏览器历史记录，这些状态数据对象会丢失，并且每个浏览器可能对数据的长度有限制，但对于大多数用例来说，这应该不是问题。

在本方法中，你将学习如何以 JSON 格式将数据与历史记录条目一起存储，然后通过`window.onpopstate`事件将数据取回。清单 9.6 使用幻灯片图像和用户偏好设置创建了一个简单的幻灯片放映。用户偏好设置与每个历史记录条目一起存储，这样当用户使用后退按钮导航到之前的幻灯片时，偏好设置会被恢复。偏好的恢复发生在 popstate 事件处理程序中。

### 清单 9.6 幻灯片演示：推入带数据的页面



# 幻灯片演示与浏览器历史记录控制

## HTML 页面结构

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>Slide 1</title>
</head>
<body>
<script>
// set first and last slide numbers
var minSlide     = 1;
var maxSlide     = 5;

// initialize fields used
var currentSlide   = 1;
var currentTitle   = "My Slide 1";
var borderOn       = 0;  // 0 is off, 1 is on
var slideNote      = "";

// initialize our first slide state by replacing current state
var stateObj = { slide: currentSlide, border: borderOn, note: slideNote };
history.replaceState(stateObj, currentTitle, '?slide=' + currentSlide);

// history pop state handler
window.onpopstate = function(event) {

  // show the location URL and string display of the event.state
  document.getElementById('stateInfo').innerHTML = "location: " +
  document.location + "<br>state: " + JSON.stringify(event.state);

  // retrieve state object data
  currentSlide   = event.state.slide;
  borderOn       = event.state.border;
  slideNote      = event.state.note;

  // show the current slide
  showSlide();
}

// navigate to the next slide
function nextSlide() {

  // check if the History API is available
  if ( typeof history.pushState !== "undefined" ) {

    // validate that we are not at the end of the presentation
    if ( currentSlide < maxSlide ) {

      // retrieve any notes that have been entered
      slideNote = document.getElementById('txtNote').value;

      // set the state object with the current options
      var currentStateObj = { slide: currentSlide, border: borderOn, note:
slideNote };

      // replace the current slide properties in the current history entry
      history.replaceState( currentStateObj, 'Slide ' + currentSlide + ' ' +
slideNote, "?slide=" + currentSlide);

      // increment the current slide index
      currentSlide++;

      // set global variables to next slide and reset to defaults
      borderOn = 0;
      slideNote = "";
      document.getElementById('stateInfo').innerHTML = "";

      // set next slide in history entries with state object and defaults
      var nextStateObj = { slide: currentSlide, border: borderOn, note: slideNote };
      history.pushState( nextStateObj, 'Slide ' + currentSlide, "?slide=" + currentSlide );

      // show the now current slide
      showSlide();
    }
  } else {
    // History API is not available
    alert('The History API is not available in this browser.');
  }
}

// navigate to previous slide
function prevSlide() {

  // validate that we are not at the beginning already
  if (currentSlide>minSlide) {

    // move back one step in history
    history.back();
  }
}

// show the current slide, title, and options
function showSlide() {

  // set the current slide and title
  document.getElementById('imgSlide').src = "images/slide" + currentSlide + ".jpg";
  document.getElementById('slideInfo').innerHTML = "Slide " + currentSlide;

  // set the current page title
  document.title = "Slide " + currentSlide;

  // set the current slide options
  if (borderOn == 1) {
    document.getElementById('imgSlide').style.border = "5px solid #000000";
    document.getElementById('chkBorder').checked = 1;
  } else {
    document.getElementById('imgSlide').style.border = "";
    document.getElementById('chkBorder').checked = 0;
  }
  document.getElementById('txtNote').value = slideNote;
}

// handle the change of the image border option
function setImgBorder() {

  // set border based on checkbox and global property
  if (document.getElementById('chkBorder').checked == 1) {
    document.getElementById('imgSlide').style.border = "5px solid #000000";
    borderOn = 1;
  } else {
    document.getElementById('imgSlide').style.border = "";
    borderOn = 0;
  }
}
</script>

<!-- slide image and title -->
<div id='slide' style='height:100px;'><img id='imgSlide'
    src="images/slide1.jpg"></div>
<div id='slideInfo'>Slide 1</div>

<!-- slide options -->
<input type="checkbox" id="chkBorder" onChange="setImgBorder();">Border<br>
    Note: <input type="text" id="txtNote" value=""><br>

<!-- slide navigation buttons -->
<input type="button" onclick="prevSlide();" value="Previous Slide" />
<input type="button" onclick="nextSlide();" value="Next Slide" />

<!-- history state display area -->
<div id='stateInfo'></div>
</body>
</html>
```

此代码允许用户为每张幻灯片设置图片边框和备注。你可以提供任意数量的选项。一个名为`stateInfo`的调试`div`会显示历史记录条目被弹出时数据的上下文。你可以使用`JSON.stringify`方法来显示JSON状态对象。要引用每个已存储的状态对象值，只需通过键名进行引用。例如，要获取边框状态值，可以调用`event.state.border`。当用户点击下一张幻灯片时，你创建一个包含当前设置和幻灯片编号的对象。然后将其传递给`replaceState`调用，以便在推入下一张幻灯片之前存储状态。接着你重置设置并推入下一张幻灯片。

## 第9章 更改浏览器历史记录

用于显示的幻灯片。当然，这并未考虑在当前幻灯片之后出现的已查看幻灯片，因为每个后续幻灯片都会作为新的历史记录条目被压入历史栈。为了解决这个问题，你可以使用HTML5的一些新的客户端存储技术，这些技术将在第11章"客户端存储"中介绍。

## 中级技巧：测试历史记录安全性

每当你能够修改浏览器历史记录、页面标题和URL地址时，都需要考虑安全问题。更改URL地址历来是常见的钓鱼方法之一，也被称为*网站伪造*。新的History API首次为开发者提供了一种无需实际加载页面即可更改URL内容的方法。然而，HTML5规范包含了各种浏览器需要遵循的保障措施，以防止History API的滥用：

- 脚本不能在`pushState`和`replaceState`的URL中设置与当前域名不同的域名。
- `popstate`事件只能引用由相同域名源的页面存储在历史记录中的状态对象，以维护跨站点隐私。
- 限制页面通过`pushState`方法添加到浏览器历史记录栈中的条目数量，以防止"泛滥"用户的浏览器历史记录。

通过这些浏览器策略，History API可能被恶意使用的风险应被最小化。让我们通过尝试将URL更改为不同的域名来验证其中一项策略。

> **注意**
>
> 浏览器可能会实施限制并修剪历史记录栈，以防止潜在的"泛滥"攻击造成的过载。条目数量由每个浏览器决定，但移除顺序遵循先进先出（FIFO）原则。

关于允许JavaScript控制浏览器的URL显示，而无需实际更改页面或导致加载新页面，已经有很多争论。主要关注点是，诸如`pushState`或`replaceState`之类的方法可能被用于钓鱼以获取个人和机密信息，通过使用户看起来位于不同的位置。你可以想象，如果能够将地址更改为任何你想要的内容会造成多么大的混乱。然而，History API的规范要求浏览器验证`url`参数中使用的地址。如果使用绝对路径，则该地址必须与原始页面具有相同的源。让我们通过尝试将不同域名的页面压入历史记录来验证浏览器是否能防止这种可能的滥用。清单9.7提供了一个非常简单的页面用于压入新状态。请尝试它，并按照以下步骤创建清单9.7的副本，在你的浏览器中验证其是否有效：

1. 创建一个空白HTML页面，其中包含一个按钮，单击时启动`pushPage`函数。
2. 添加`pushPage`函数，该函数检查`history.pushState`方法的可用性，然后压入`page.html`的新上下文。

### 清单9.7 同一源中的简单压入

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>9.7 Push across domains</title>
</head>
<body>
<script>
// initialize the button handler
function init() {
  // attach the click button handler
  var btnPushPage = document.getElementById('btnPushPage');
  btnPushPage.addEventListener('click',pushPage,false);
}

// push the new state into history
function pushPage() {

  // we check to see if the History API is available
  if (typeof history.pushState !== "undefined") {

    // push the new state
    history.pushState(null, 'Good Page', 'page.html');
  } else {

    // the History API is not available
    alert('History API not available in this browser');
  }
}

// Add the listener to initialize the page
window.addEventListener('load',init,false);

</script>
<button id="btnPushPage">Try Push</button>
</body>
</html>
```

现在让我们对前面的清单进行微小的修改，看看如果有人试图使用`pushState`伪造域名URL会发生什么。如清单9.8所示，将`pushState`方法的`url`参数更改为与你当前运行的域名不同的域名的绝对路径。我们仅以`www.asite.com`为例。

### 清单9.8 设置不同的源

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>9.8 Setting a Different Origin</title>
</head>
<body>
<script>
// initialize the button handler
function init() {
  // attach the click button handler
  var btnPushPage = document.getElementById('btnPushPage');
  btnPushPage.addEventListener('click',pushPage,false);
}

// push the new state into history
function pushPage() {

  // we check to see if the History API is available
  if (typeof history.pushState !== "undefined") {

    // push the new state
    history.pushState(null, 'Bad Page', 'http://www.asite.com/fish.html');
  } else {

    // the History API is not available
    alert('History API not available in this browser');
  }
}

// Add the listener to initialize the page
window.addEventListener('load',init,false);

</script>
<button id="btnPushPage">Try Push</button>
</body>
</html>
```

当使用`pushState`方法将新状态压入历史记录时，浏览器将验证传递的URL。如果URL是完整路径且域名与正在"压入"的域名不同，调用将失败、抛出异常，或者根据浏览器的不同可能不做任何操作。`replaceState`方法同样如此。

## 实用库

作为Web开发者，我们不仅需要关注History API的安全方面，还需要关注该API在浏览器之间以及同一浏览器不同版本之间的支持情况。对于HTML5的几个新API，不同浏览器的实现程度差异很大，向后兼容性在可预见的未来将是一个问题，至少在大多数用户迁移到新版本之前是这样。对于History API，这意味着你需要继续支持哈希地址方法和`hashChange`事件，以保持页面状态的向后兼容性：

```javascript
window.onhashchange = function() {
    alert("hash changed!");
};
window.location.hash = Math.random();
```



然而，这并不意味着你必须放弃新的HTML5历史记录功能的好处。与大多数浏览器兼容性问题一样，其他开发者已经认识到这个缺点，并创建了库来处理不仅在浏览器之间，而且在浏览器版本之间的差异。对于History API，目前领先的库是`history.js`。

你仍然可以自己编写逻辑，但`history.js`库可在GitHub上获取（https://github.com/balupton/History.js），并提供了一个易于使用的包装JavaScript库，该库尝试使用HTML5历史记录方法（如果支持），但在需要时会自动回退到哈希码方法。总体而言，其语法与你在本章中看到的History API方法、事件和属性相似。遗憾的是，我们在这里没有篇幅来详细探讨该库，但该库提供了以下功能：

- 多浏览器支持
- 框架支持，包括jQuery、MooTools和Prototype
- 通过使用哈希标签实现对旧浏览器的向后兼容性

## 总结

JavaScript中可用的History API功能非常强大，为Web开发者提供了在不更改实际页面的情况下更改用户站点历史记录的机会。GitHub和Flickr等网站已经充分利用了History API，提供了更用户友好的功能。

在本章中，你研究了`pushState`和`replaceState`方法以及`popstate`事件如何与历史记录条目列表协同工作（参见图9.4）。

以下是HTML5现在为历史记录添加的主要技术特性：

- 将新条目压入浏览器历史记录条目中
- 替换当前历史记录条目状态数据
- 管理导航事件处理和检索状态

你现在应该对如何在你自己的网站或应用中使用这些功能有了些想法。

## 10 使用地理位置 API 实现位置感知

多年来，网站一直使用位置信息来提供增强的用户体验，例如显示最近的商店位置或您所在地区的活动。位置数据的收集方式包括利用浏览器的 IP 地址在数据库中进行匹配，或直接询问用户的位置。随着智能手机和内置 GPS 的普及，支持位置感知的应用程序大幅增加。借助 HTML5 和地理位置 API，网站和 Web 应用程序可以轻松且相对可靠地获取浏览器的位置信息。在本章中，您将通过一系列实践方案，了解地理位置 API 的对象和方法，以获取浏览器设备的位置信息并在您的应用中使用。

## 地理位置概述

识别浏览器（无论是笔记本电脑还是移动端）位置信息的能力，提供了可用于多种功能的关键信息，包括以下方面：

- 在地图上显示浏览器的位置
- 显示特定位置的信息或兴趣点
- 将位置数据添加到用户贡献中，例如地点评论或照片

通过关联浏览器的 IP 地址来访问用户的位置可能会有问题，因为 IP 地址和位置的数据库必须广泛且维护良好。位置信息也可能比较模糊，仅能提供大致区域的信息。使用位置数据的网站通常会要求用户提供其邮政编码或完整地址，以克服 IP 地址定位的挑战，这并不少见。然而，这些信息与用户当时所在的位置相关，而不是他们未来可能所在的位置。HTML5 地理位置 API 提供了内置方法，可以提供相当精细的信息。

通过地理位置 API，浏览器现在能够通过纬度和经度值告诉您其在世界上的位置，并附带一定的精确度。精确度取决于多个因素，开发者可以影响精确度。现在您可能想知道，如果您不知道街角咖啡馆的纬度和经度坐标，那么纬度和经度有什么用呢？为了让地理位置发挥作用，传达位置的通用方式必须处于“最低公分母”水平，而纬度和经度坐标系统提供了这一点。正如您将在本章后面看到的，有许多来自不同供应商的服务可以接收纬度和经度坐标并提供额外信息。并且，要进行反向地理编码（参见下文侧栏），给定像 Google 这样拥有大型地理数据库的供应商，一组坐标是相当容易获取的。

> ### 反向地理编码
>
> 反向地理编码是地理编码（将地址转换为一组纬度和经度坐标）的相反过程，它是将一组纬度和经度坐标转换为物理地址的做法。各种服务都可以提供此信息。最常用的是 Google 地图 JavaScript API V3 服务 (http://code.google.com/apis/maps/documentation/javascript/services.html#ReverseGeocoding)。

### 浏览器兼容性

地理位置 API 仍然很年轻，但考虑到它所具有的价值，其 API 定义正在被各种浏览器迅速采用。表 10.1 列出了当前浏览器对地理位置 API 的支持情况。

表 10.1 地理位置 API 浏览器支持情况

| 浏览器 | 版本 |
| :--- | :--- |
| Android | 2.1+ |
| Chrome | 9.0+ |
| Firefox | 3.5+ |
| Internet Explorer | 9.0+ |
| iOS Safari | 3.2+ |
| Opera | 10.6+ |
| Safari | 5.0+ |

### 初学者实践：使用简单的 getCurrentPosition 确定您的位置

### 世界在何处：getCurrentPosition

地理位置 API 的基本功能是查找浏览器在世界上的当前位置。`getCurrentPosition`方法通过 JavaScript 异步调用向您提供此信息。需要注意的是，在 JavaScript 中确定位置的调用本质上是异步的。大多数 JavaScript 是同步执行或在主程序流中执行的。通过异步方法调用，JavaScript 在后台执行调用，然后在过程完成后将结果返回给函数。通过将 API 调用设为异步调用，可以向用户显示查询结果，而不会阻塞页面其余部分的处理。

`getCurrentPosition`方法检索浏览器的当前位置，并接受一个必需参数（成功回调函数名称）和两个可选参数（错误回调函数和位置选项对象）：

`getCurrentPosition(successCallback [, errorCallback] [, positionOptions])`

`getCurrentPosition`的参数包括以下内容：

- `successCallback`：要执行并传递坐标的函数
- `errorCallback`：（可选）处理任何发生错误的函数
- `options`：（可选）用于处理如何检索位置的选项对象

由于对`getCurrentPosition`的调用是异步的，因此需要告诉该方法在方法完成后将执行哪些成功和潜在失败的函数。让我们立即开始，通过一个实践方案来找到您的位置。

### 初学者实践：使用简单的 getCurrentPosition 确定您的位置

在此实践中，页面将使用带有成功回调函数的`getCurrentPosition`方法来确定您的当前位置，并显示返回的位置对象的属性。请使用以下步骤和代码清单 10.1 来创建此实践：

1. 创建一个空白的 HTML 页面，其中包含一个`div`（称为`btnFindMe`）和一个“Find Me”按钮，该按钮在被点击时将调用`findMe`函数。

2. 在一组`script`标签中添加`findMe`函数，使用以下代码来检查地理位置 API，然后调用`getCurrentPosition`方法：

```javascript
if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(geoSuccess);
} else {
    document.getElementById('myLocation').innerHTML = "Geolocation API Not Supported";
}
```

3. 添加`geoSuccess`函数，该函数将处理来自`getCurrentPosition`请求的成功回调。

4. 在 HTML 中添加第二个`div`（称为`myLocation`），您将在其中显示从`getCurrentPosition`返回的位置信息。

**代码清单 10.1 使用 getCurrentPosition 查找浏览器位置**

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>10.1 Find Me</title>
<script>

// Initialize the page with other event listeners
function init() {
  var btnFindMe = document.getElementById('findMe');
  btnFindMe.addEventListener('click',findMe,false);
}

// success callback function for getCurrentPosition
function geoSuccess(position) {

  // grab the position DOMTimeStamp for display
  var dateDisplay = new Date(position.timestamp);

  // get reference to result div
  var myLocationDiv = document.getElementById('myLocation');

  // display the coords and timestamp object fields
  myLocationDiv.innerHTML = 'Lat: ' + position.coords.latitude + '<br>' +
    'Lng: ' + position.coords.longitude + '<br>' +
    'Accuracy: ' + position.coords.accuracy + '<br>' +
    'Alt. Accuracy (opt): ' + position.coords.altitudeAccuracy + '<br>' +
    'Heading (opt): ' + position.coords.heading + '<br>' +
    'Speed (opt): ' + position.coords.speed + '<br>' +
    'Position DOMTimeStamp: ' + position.timestamp + '<br>' +
    'Time Date Stamp: ' + dateDisplay.toLocaleString();
}

// function called from button click to find position
function findMe() {
  var myLocationDiv = document.getElementById('myLocation');
  // check for geolocation support
  if (navigator.geolocation) {
    // make asynchronous getCurrentPosition call
    navigator.geolocation.getCurrentPosition(geoSuccess);
    myLocationDiv.innerHTML = 'Retrieving your location.';
  } else {
    // geolocation not supported
    myLocationDiv.innerHTML = 'Geolocation API Not Supported';
  }
}

// Initialize the page on load
window.addEventListener('load',init,false);
</script>
</head>
<body>
<div id='btnFindMe'>
  <button id="findMe">Find Me</button>
</div>
<div id="myLocation"></div>
</body>
</html>
```

当您点击“Find Me”按钮时，`findMe()`函数将被调用。此函数的第一步是检查您使用的浏览器是否支持地理位置 API。此检查通过使用以下代码完成：

`if (navigator.geolocation) {`

如果`navigator.geolocation`对象可用，那么您就可以执行`getCurrentPosition`；否则，您可以通过显示 API 不支持的相应消息来处理 API 的缺失支持。成功验证 API 的可用性后，将使用回调函数名`geoSuccess`调用`getCurrentPosition`方法。这将是当`getCurrentPosition`完成时要执行的函数。

当调用`getCurrentPosition`方法时，浏览器要执行的第一个操作是验证用户是否已授权浏览器向页面提供此信息，或者提示用户进行授权。根据使用的浏览器，消息和选项可能略有不同。例如，在 Firefox 中，会从浏览器顶部下拉一个授权面板，允许用户选择共享或不共享其位置，并记住该网站的选择。在 Safari 中，将出现一个对话框，向用户确认允许、不允许或允许接下来的 24 小时。

当浏览器被授权检索您的位置时，浏览器将利用 WiFi 和蜂窝网络信息（如果可用）来确定位置。

## 第10章 使用地理定位API实现位置感知

表10.2 位置返回对象

| 对象 | 属性 | 类型 | 用途 |
|---|---|---|---|
| coords | latitude | double | 位置的纬度坐标 |
| | longitude | double | 位置的经度坐标 |
| | accuracy | double | 纬度和经度值的精度，单位为米 |
| | altitude | double | （可选）高度值，如果可用 |
| | altitudeAccuracy | double | （可选）高度值的精度 |
| | heading | double | （可选）从北开始的航向角度，如果可用 |
| | speed | double | （可选）速度，如果可用 |
| timestamp | | DOMTimeStamp | 当前的本地日期和时间 |

信息将作为位置对象传递给成功回调函数。该位置对象包含位置的属性，包括纬度和经度（见表10.2）。

位置对象的数据分为`coords`对象和一个`DOMTimeStamp`格式的时间戳。在`geoSuccess`函数中，你现在可以通过位置根对象来引用`coords`对象的各种属性。例如，要获取位置的纬度，你需要使用`position.coords.latitude`。每个浏览器对可选字段的处理方式会有所不同；图10.1展示了Chrome 14的输出。

![](img/de30ea99ecac39b49e690a84c48f43b9_266_0.png)

## 位置隐私

知晓浏览器的位置，从而知晓查看浏览器者的位置，这可以被视为隐私信息。允许用户共享其私人位置信息的方法是通过一个授权操作，正如你在第一个示例中看到的那样。在用户允许或拒绝访问位置之前，`getCurrentPosition` API调用将处于等待状态。这是该调用通过异步方法执行的一个关键原因，这样页面的其余部分就不会因为等待用户授权或回复而“阻塞”。

你可能会想，如果用户没有提供信息授权或位置信息超时了会怎样。这时`getCurrentPosition`的错误处理参数就派上用场了，这也是你将在下一个示例中看到的内容。

> **提示**
>
> 当你使用地理定位API时，你可能会发现在某些情况下你的页面没有产生结果或返回了超时错误（正如你将在下一个示例中看到的）。这通常是因为你的代码中某个回调函数存在错误。由于位置方法是异步的，这些错误是否会冒泡到你的浏览器窗口取决于你正在使用的浏览器。在回调函数中使用`console.log()`调试来识别问题会很有帮助。

## 中级示例：使用getCurrentPosition绘制位置地图

在这个示例中，你将使用`getCurrentPosition`方法来获取浏览器的位置，并在页面上的谷歌地图中将其绘制出来。你将在示例中包含一个错误处理程序，以防`getCurrentPosition`方法返回错误（一旦你的页面正常工作，你就会让它发生）。

与之前的示例类似，当页面加载时，用户可以点击“Map Me”按钮，这将触发`getCurrentPosition`方法。一旦你收到调用，你将使用经纬度坐标来创建一个带有标记和信息窗口的谷歌地图实例，用于显示坐标、城市和州。城市和州信息来自Mozilla地址对象，在其他浏览器中不可用。如果你想在其他浏览器中显示对应的物理地址，那么你需要使用反向地理编码，这将在本章的另一个示例中看到。

1. 利用之前的示例，将按钮更改为“Map Me”，并将调用的函数更改为`mapMe`。

2. 包含Google Maps JavaScript API V3 Overlay脚本标签（注意，使用V3版的Google Maps套件，你不再需要开发者密钥）：

```html
<script src="http://maps.google.com/maps/api/js?sensor=false">
```

3. 修改`getCurrentPosition`请求以添加错误处理函数：

`navigator.geolocation.getCurrentPosition(geoSuccess, geoErrorHandler);`

4. 添加`geoErrorHandler`函数`geoErrorHandler(error)`，该函数将处理`getCurrentPosition`请求返回的任何错误。

5. 更新HTML主体`div`部分，使其与清单10.2中的内容一致，包含一个包含`mapCanvas`、`mapMe`按钮和`myLocation`的容器。

### 清单10.2 使用getCurrentPosition绘制位置地图



```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>10.2 Map Me With Error Handling</title>
<style>
#container {
    width:500px;
}

#mapCanvas {
    width:500px;
    height:300px;
    border-style:solid;
    border-width:2px;
    margin: 22px 0;
}

#btnMapMe {
    float:left;
}

#myLocation {
    float:right;
}
</style>
<script src="http://maps.google.com/maps/api/js?sensor=false"></script>
<script>

// Initialize the page
function init() {
    // Add the button click listener
    var btnMapMe = document.getElementById('mapMe');
    btnMapMe.addEventListener('click',mapMe,false);
}

// success callback function for getCurrentPosition
function geoSuccess(position) {

    // get reference to result div
    var myLocationDiv = document.getElementById('myLocation');

    // retrieve our lat and long coordinates
    var posLat = position.coords.latitude;
    var posLng = position.coords.longitude;
    var posAccuracy = position.coords.accuracy;

    // display the coords and timestamp object fields
    myLocationDiv.innerHTML = 'Lat: ' + posLat + ', Lng: ' + posLng + '<br>Accuracy: ' + posAccuracy;

    // create a google map latlng out of our coordinates
    var myLatlng = new google.maps.LatLng(posLat, posLng);

    // set our options for our map using our latlng as the center
    var myOptions = {
        zoom: 14,
        center: myLatlng,
        mapTypeId: google.maps.MapTypeId.ROADMAP
    }

    // create our google map instance
    var map = new google.maps.Map(document.getElementById('mapCanvas'), myOptions);

    // add our marker for our location
    var marker = new google.maps.Marker({
        position: myLatlng,
        map: map
    });

    // create our info window text
    var infoText = '';
    infoText = posLat + ', ' + posLng + '<br>Accuracy: ' + posAccuracy;
    if (position.address) {
        infoText += '<br>' + position.address.city + ', ' + position.address.region;
    }

    // create the info window and set the text
    var infowindow = new google.maps.InfoWindow();
    infowindow.setContent(infoText);
    infowindow.open(map, marker);
}

// error handler for getCurrentPosition
function geoErrorHandler(error) {

    // initialize our error message
    var errMessage = 'ERROR: ';

    // based on the error code parameter set the message
    switch(error.code)
    {
        case error.PERMISSION_DENIED:
            errMessage += 'User did not share geolocation data.';
            break;
        case error.POSITION_UNAVAILABLE:
            errMessage += 'Could not detect current position.';
            break;
        case error.TIMEOUT:
            errMessage += 'Retrieving position timed out.';
            break;
        default:
            errMessage += 'Unknown error.';
            break;
    }

    // display the error to the user
    document.getElementById('myLocation').innerHTML = errMessage;
}

// function called from button click to find position
function mapMe() {
    var myLocationDiv = document.getElementById('myLocation');

    // check for geolocation support
    if (navigator.geolocation) {
        // make asynchronous getCurrentPosition call
        navigator.geolocation.getCurrentPosition(geoSuccess, geoErrorHandler);
        myLocationDiv.innerHTML = 'Retrieving your location...';
    } else {
        // geolocation not supported
        myLocationDiv.innerHTML = 'Geolocation API Not Supported';
    }
}

// Initialize the page
window.addEventListener('load',init,false);

</script>
</head>
```

## 进阶示例：使用 `getCurrentPosition` 定位地图

```html
<body>
<div id="container">
  <div id="mapCanvas"></div>
  <div id="btnMapMe">
    <button id="mapMe">Map Me</button>
  </div>
  <div id="myLocation"></div>
</div>
</body>
</html>
```

当你点击 "Map Me" 按钮时，`mapMe` 函数将被调用。与之前一样，你需要检查地理位置 API 是否可用，如果可用，则执行 `getCurrentPosition` 方法。如果 `getCurrentPosition` 成功，则会调用 `geoSuccess` 函数，检索坐标，显示在 `myLocation` div 中，然后用于创建带有标记和信息窗口的谷歌地图实例。结果将类似于图 10.2，但显示的是你的位置。

在 `getCurrentPosition` 方法调用中，你添加了第二个参数，即名为 `geoErrorHandler` 的错误处理程序。以下是位置方法可能返回的错误：

- `PERMISSION_DENIED` (1)：请求失败，因为用户未授权使用位置信息。
- `POSITION_UNAVAILABLE` (2)：浏览器无法确定设备的位置。
- `TIMEOUT` (3)：如果提供了 `timeout` 属性且超时时间已过，则返回此错误。

![](img/de30ea99ecac39b49e690a84c48f43b9_271_0.png)

## 第 242 章 使用地理位置 API 实现位置感知

错误处理程序允许你捕获返回的错误并采取相应的措施。一个常见的错误 `PERMISSION_DENIED` 是由于用户未授予页面上地理位置 API 调用所需的信息访问权限导致的。要查看此错误，请重新加载页面，当浏览器询问是否允许访问位置信息时，选择不共享或拒绝访问你的位置。错误处理程序 `geoErrorHandler` 将被调用，并传入一个位置错误对象。在我们的代码中，该位置错误对象（命名为 `error`）将包含两个属性：`code` 和 `message`。前面显示的代码是一个定义错误类型的数值常量，而 `message` 可能包含一个可选的字符串消息，供你（开发者）更深入地了解错误发生的原因。在这种情况下，由于用户拒绝了位置信息的访问权限，将提供 `PERMISSION_DENIED` 错误代码，你可以显示自己的消息。

> **注意**

Mozilla 添加了第四个可能的错误代码值：`UNKNOWN_ERROR` (0)。当位置检索因未知原因失败且不属于其他错误范围时，会提供此错误。在代码清单 10.2 中，`switch` 的 `default` 分支将捕获任何未知错误，包括 Mozilla 提供的 `UNKNOWN_ERROR`。在这种情况下，错误对象的 `message` 属性对于确定错误原因可能更有帮助。

在示例中，你利用谷歌地图 JavaScript API V3 Overlay 向用户显示其带有标记的位置。与此标记关联的，你还打开了一个包含其经纬度坐标的信息窗口。Mozilla 提供了一个名为 `address` 的附加位置属性，它不在 W3C 规范中。它提供了坐标的物理位置。当然，由于位置的精度可能过大，这个物理地址位置可能不精确，但在可用时，它省去了使用另一个服务对坐标进行逆地理编码的需要。在这个示例中，如果 `address` 对象可用，你可以从中提取 `city` 和 `region` 属性，并将值附加到信息窗口中。以下是当提供 `address` 对象时可用的属性：

- `city`: 包含城市名的 `DOMString`。
- `country`: 包含国家名的 `DOMString`。
- `countryCode`: 包含国家代码的 `DOMString`。
- `county`: 包含县/郡名的 `DOMString`。
- `postalCode`: 包含邮政编码或 ZIP 码的 `DOMString`。
- `premises`: 包含建筑物/场所名称的 `DOMString`。
- `region`: 包含地区/州/省名的 `DOMString`。
- `street`: 包含街道名称的 `DOMString`。
- `streetNumber`: 包含街道门牌号的 `DOMString`。

### 进阶示例：使用 `PositionOptions` 确定距离

如果 `address` 对象不可用，那么你可以使用谷歌提供的逆地理编码服务，这将在下一个示例中看到。在下一个示例中，你将研究 `getCurrentPosition` 接口提供的三个选项，以及它们如何根据你的具体需求发挥作用。

### 进阶示例：使用 `PositionOptions` 确定距离

本示例将首先使用 `getCurrentPosition` 定位你的浏览器位置，然后计算到一组点的距离，对你的位置进行逆地理编码，并将此信息显示给用户。为了更好地控制提供的位置信息，你将使用 `getCurrentPosition` 方法的第三个参数 `PositionOptions`。

`PositionOptions` 是一个作为参数传递给 `getCurrentPosition` 方法的对象，允许你对该方法的行为进行一些控制。根据你正在开发的应用程序类型，这可能是有益的。例如，如果你正在为移动设备开发一个基于位置的餐厅应用程序，那么返回位置的常规精度可能对你的需求来说过于宽泛。你可以在 `getCurrentPosition` 的 `PositionOptions` 中设置三个选项，如表 10.3 所示。

> 注意

对于 `PositionOptions` 参数的 `timeout` 选项，用户在请求面板或对话框弹出期间授权访问位置信息所花费的时间不计算在此时间内。超时毫秒数仅针对实际调用执行的时间进行计算。

### 表 10.3 `PositionOptions` 参数

| 选项 | 默认值 | 描述 |
| :--- | :--- | :--- |
| `enableHighAccuracy` | False，未启用 | （可选）一个布尔值，告诉浏览器如果为 `true`，你希望设备可能提供的最精确的位置。根据所使用的设备，这可能是相同的位置。 |
| `maximumAge` | 0，允许任何年龄 | （可选）返回的位置信息的最大有效期（毫秒），因为浏览器可能会缓存上次的位置以节省电池电量。 |
| `timeout` | 0，无超时 | （可选）允许浏览器返回位置信息的最大时间（毫秒）。 |

## 第 244 章 使用地理位置 API 实现位置感知

页面加载时，`setLocation` 函数将被调用，该函数将使用一组选项触发 `getCurrentPosition` 方法。一旦收到调用，你将使用经纬度坐标创建谷歌地图实例，对坐标进行逆地理编码，并计算到各个城市的距离。

1. 将 `setLocation` 方法调用添加到 `body` 的 `onload` 属性中，并添加 `setLocation` 函数，确保包含位置选项对象。
2. 更新谷歌地图 JavaScript API V3 Overlay 脚本标签以加载用于距离计算的 geometry 库：

   `<script src="http://maps.google.com/maps/api/js?sensor=false&libraries=geometry"></script>`

3. 添加 `reverseGeoCode` 函数，该函数接受你的经纬度点并从谷歌地理编码器检索地址信息。
4. 添加 `calculateDistance` 函数，该函数使用 `computeDistanceBetween` 计算到伦敦、纽约和旧金山的距离。
5. 更新 HTML body `div` 部分以与代码清单 10.3 中的结构一致，包含一个容器，其中包括 `mapCanvas`、位置信息和城市距离 div。

代码清单 10.3 带有位置选项的 `getCurrentPosition`

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>10.3 Points To</title>
<style>
#container {
  width:500px;
}
#mapCanvas {
  width:500px;
  height:300px;
  border-style:solid;
  border-width:2px;
  margin: 22px 0;
}
#location {
  float:right;
  text-align:right;
}
</style>
</head>
<body>
</body>
</html>
```

## 中级示例：使用 `PositionOptions` 确定距离



```html
<style>
#cityDistance tr:nth-child(odd) { background-color:#eee; }
#cityDistance tr:nth-child(even) { background-color:#fff; }

.numDistance {
    text-align:right;
}
</style>
<script src="http://maps.google.com/maps/api/js?sensor=false&libraries=geometry"></script>
<script>
// global reference variable
var map;

// success callback function for getCurrentPosition
function geoSuccess(position) {

    // get our lat and lng coordinates
    var myPosLat = position.coords.latitude;
    var myPosLng = position.coords.longitude;

    // display the coords and timestamp object fields
    document.getElementById('myPosLat').innerHTML = myPosLat;
    document.getElementById('myPosLng').innerHTML = myPosLng;

    // create our latlng object
    var myLatLng = new google.maps.LatLng(myPosLat, myPosLng);

    // set our options for the map and create the map
    var myOptions = {
        zoom: 14,
        center: myLatLng,
        mapTypeId: google.maps.MapTypeId.ROADMAP
    }
    map = new google.maps.Map(document.getElementById('mapCanvas'), myOptions);

    // reverse geocode the lat and lng
    reverseGeoCode(myLatLng);

    // calculate the distance to points of interest
    calculateDistance(myLatLng);

    // update our status
    document.getElementById('geoStatus').innerHTML = '位置已获取';
}

// function to reverse geocode given a lat / lng
function reverseGeoCode(geoLatLng) {

    // create our object instances
    var geocoder = new google.maps.Geocoder();
    var infowindow = new google.maps.InfoWindow();

    // perform our geocoding
    geocoder.geocode({'latLng': geoLatLng}, function(results, status) {
        if (status == google.maps.GeocoderStatus.OK) {
            // check if we received an address
            if (results[0]) {
                // create marker on map
                var marker = new google.maps.Marker({
                    position: geoLatLng,
                    map: map
                });
                // set the content to the address and open the window
                infowindow.setContent(results[0].formatted_address);
                infowindow.open(map, marker);
            }
        } else {
            alert('地理编码失败，原因：' + status);
        }
    });
}

// calculate distance function
function calculateDistance(disLatLng) {

    // set up variables and objects for distance
    var conEarth = 3963.19; // ave. miles circumference
    var gmapsSpherLib = google.maps.geometry.spherical;

    // points of interest
    var NYCLatLng = new google.maps.LatLng(40.7141667, -74.0063889);
    var LDNLatLng = new google.maps.LatLng(51.5001524, -0.1262362);
    var SFOLatLng = new google.maps.LatLng(37.615223, -122.389979);

    // distance calculations
    var distFromLDN =
        gmapsSpherLib.computeDistanceBetween(disLatLng, LDNLatLng, conEarth).
            toFixed(2);
    var distFromNYC =
        gmapsSpherLib.computeDistanceBetween(disLatLng, NYCLatLng, conEarth).
            toFixed(2);
    var distFromSFO =
        gmapsSpherLib.computeDistanceBetween(disLatLng, SFOLatLng, conEarth).
            toFixed(2);

    // set display with values
    document.getElementById('divDistFromLDN').innerHTML = distFromLDN + ' 英里';
    document.getElementById('divDistFromNYC').innerHTML = distFromNYC + ' 英里';
    document.getElementById('divDistFromSFO').innerHTML = distFromSFO + ' 英里';
}

// error handler for getCurrentPosition
function geoErrorHandler(error) {

    // initialize our error message
    var errMessage = '错误：';

    // based on the error code parameter set the message
    switch(error.code)
    {
        case error.PERMISSION_DENIED:
            errMessage += '用户未共享地理位置数据。';
            break;
        case error.POSITION_UNAVAILABLE:
            errMessage += '无法检测当前位置。';
            break;
        case error.TIMEOUT:
            errMessage += '获取位置超时。';
            break;
        default:
            errMessage += '未知错误。';
            break;
    }

    // display the error to the user
    document.getElementById('geoStatus').innerHTML = errMessage;
}

// function to initialize call for position
function setLocation() {

    var divStatus = document.getElementById('geoStatus');

    // check for geolocation support
    if (navigator.geolocation) {

        // oldest allowed is 1 minute and timeout as 30 sec.
        var posOptions = {maximumAge:60000, timeout:30000};

        // make asynchronous getCurrentPosition call
        navigator.geolocation.getCurrentPosition(geoSuccess, geoErrorHandler, posOptions);

        divStatus.innerHTML = '正在获取您的位置。';

    } else {
        // geolocation not supported
        divStatus.innerHTML = '不支持地理定位 API';
    }
}

// Launch the location retrieval
window.addEventListener('load',setLocation,false);

</script>
</head>
<body>
<div id="container">
    <div id="mapCanvas"></div>
    <div id="location">
        <table id="status">
            <tr>
                <td colspan="2"><div id="geoStatus"></div></td>
            </tr>
            <tr>
                <td>纬度：</td>
                <td class="numDistance"><div id="myPosLat"></div></td>
            </tr>
            <tr>
                <td>经度：</td>
                <td class="numDistance"><div id="myPosLng"></div></td>
            </tr>
        </table>
    </div>
    <div id="distance">
        <table id="cityDistance">
            <tr>
                <td>伦敦：</td>
                <td class="numDistance"><div id="divDistFromLDN"></div></td>
            </tr>
            <tr>
                <td>纽约：</td>
                <td class="numDistance"><div id="divDistFromNYC"></div></td>
            </tr>
            <tr>
                <td>旧金山：</td>
                <td class="numDistance"><div id="divDistFromSFO"></div></td>
            </tr>
        </table>
    </div>
</div>
</body>
</html>
```

当页面加载时，你使用`getCurrentPosition`方法来检索经纬度坐标，但传递了一些关键选项。创建了一个名为`posOptions`的对象并传递给`getCurrentPosition`。在`posOptions`中，你将最大有效时间选项设置为`60000`，等于一分钟，超时时间设置为30秒（`30000`）。这告诉`getCurrentPosition`仅在位置信息不超过一分钟时从之前缓存的位置拉取数据。超时时间限制了`getCurrentPosition`检索位置所允许的时间长度：

```javascript
var posOptions = {maximumAge:60000, timeout:30000};
```

一旦你获得了位置信息，你就可以使用Google脚本中方便的`geocoder`对象进行反向地理编码以获取完整地址，然后计算到三个城市的距离。结果将类似于图10.3。

正如你在本示例中所见，你可以通过在`getCurrentPosition`调用中设置`PositionOptions`对象来控制位置获取的行为。这些选项允许你更改精度和性能，将你的应用调整为满足用户所需的体验。到目前为止的示例已经包含了地图、反向地理编码甚至距离计算。你可能已经想过移动端空间以及如何随着用户位置的变化来更改呈现给用户的信息。嗯，地理定位API正好有这个功能，正如你将在下一个示例中看到的那样。

![](img/de30ea99ecac39b49e690a84c48f43b9_279_0.png)

图10.3 计算出的到三个城市的距离

## 高级示例：使用 watchPosition 跟踪移动位置

在许多情况下，你的访客使用的浏览器将是基于移动端的。人们在街上行走、乘坐地铁或以其他方式移动时获取关于周围环境或自身位置的信息，这并不少见。`getCurrentPosition`方法在被调用时提供一次位置对象。然而，随着一个人四处移动，能够“跟踪”位置是很有用的。这就是地理定位API的两个新方法`watchPosition`和`clearWatch`的用武之地。

`watchPosition`方法与`getCurrentPosition`非常相似，接受相同的参数。当调用`watchPosition`方法时，浏览器将创建一个后台任务，并提供一个监视进程的引用ID作为返回值。后台任务将检索当前位置，将位置发送给成功回调，然后设置一个计时器来监视位置。每次计时器触发并检索到新位置时，都会比较该位置是否“显著”不同。如果新位置与上一次位置显著不同，则会使用新位置信息调用成功回调函数。该过程将持续运行，直到使用监视ID作为参数调用`clearWatch`方法，或者浏览器标签页或窗口被关闭（在iPhone等移动平台上，这可能是在浏览器被发送到后台时）。以下是`watchPosition`和`clearWatch`方法的接口：

`long watchPosition (successCallback [, errorCallback] [, positionOptions])`

`watchPosition`方法的参数如下：

- `successCallback`：当浏览器识别到新位置时执行并传递位置对象的函数
- `errorCallback`：（可选）处理任何发生错误的函数
- `options`：（可选）处理如何检索位置的选项对象

`clearWatch (watchId)`

`clearWatch`方法的参数如下：

- `watchId`：要结束的监视进程的long型ID引用

在这个示例中，你将使用`watchPosition`方法来检索浏览器的位置，并在位置与上一个标记物相差超过四分之一英里时，在Google地图上绘制一个新的标记。本示例的视口在`meta`标签中设置为iPhone宽度，并配合CSS样式，以便该示例可以轻松地在iPhone上运行以显示地图上的移动。点之间将连接一条线，以显示过去点的轨迹，并且地图将始终以最后显示的点为中心。当用户点击“清除监控”按钮时，监控进程将结束。

通过检查与上一个点的距离，此方法可以在用户移动设备时保持地图相对干净。但是，如果您正在处理较小的尺度，例如城市内的导航，四分之一英里的差异可能太大；如果您使用的是快速交通工具，四分之一英里可能又不够大。这种距离检查将基于您自己的需求，但本技巧展示了如何在位置变化时使用一些快速的距离计算来过滤位置点。

1. 创建包含“开始监控”和“清除监控”按钮的HTML页面，如清单10.4所示。
2. 引入包含geometry库的Google Maps JavaScript API V3 Overlay脚本，以及用于存储监控ID、地图、折线以及最后纬度和经度坐标的全局变量。



### 3. 在脚本中添加 `initMap` 函数，并将加载事件设置为启动 `initMap` 函数。

### 4. 添加 `startWatch` 和 `clearWatch` 函数。

### 5. 添加 `successCallback` 和 `errorCallback` 函数。

**清单 10.4：使用 `watchPosition` 跟踪您的路径**

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width; initial-scale=1.0; maximum-scale=1.0; user-scalable=0;" />
<title>10.4 Leaving My Mark</title>
<style>
  #container {
    width:300px;
  }

  #mapCanvas {
    width:300px;
    height:200px;
    border-style:solid;
    border-width:2px;
    margin: 22px 0;
  }

  #btnMap {
    float:left;
  }

  #location {
    float:right;
  }

  .numDistance {
    text-align:right;
  }
</style>
<script type="text/javascript"
      src="http://maps.google.com/maps/api/js?sensor=false&libraries=geometry">
</script>
<script>

// 声明我们的变量
var watchId;  // 我们的 watchposition 进程 id
var map;      // 我们的地图
var poly;     // 用于标记我们路径的折线
var lastLatLng;  // 最后的经纬度坐标

// 为 computeDistanceBetween 方法设置英里常量
var conEarthMi = 3963.19;

// 初始化我们的地图
function initMap() {

  // 添加按钮监听器
  var btnStartWatch = document.getElementById('startWatch');
  var btnStopWatch = document.getElementById('stopWatch');
  btnStartWatch.addEventListener('click', startWatch, false);
  btnStopWatch.addEventListener('click', stopWatch, false);

  // 将初始位置设置为纽约并创建地图
  lastLatLng = new google.maps.LatLng(40.7141667, -74.0063889); // 纽约
  var myOptions = {
    zoom: 14,
    center: lastLatLng,
    mapTypeId: google.maps.MapTypeId.ROADMAP
  }
  map = new google.maps.Map(document.getElementById('mapCanvas'), myOptions);

  // 设置用于显示路径的折线
  var polyOptions = {
    strokeColor: '#00FF00',
    strokeOpacity: 1.0,
    strokeWeight: 3
  }
  poly = new google.maps.Polyline(polyOptions);
  poly.setMap(map);
}

// 地理位置监控位置的 success handler
function successCallback(position) {

    // 获取我们的纬度和经度
    var posLat = position.coords.latitude;
    var posLng = position.coords.longitude;

    // 创建一个新的 google maps latlng 对象
    var newLatLng = new google.maps.LatLng(posLat, posLng);

    // 计算与上一个点的距离
    var distFromLast = 
        google.maps.geometry.spherical.computeDistanceBetween(newLatLng, 
                                                            lastLatLng, conEarthMi);

    // 验证距离是否大于四分之一英里
    if (distFromLast > 0.25) {

        // 获取折线路径数组
        var path = poly.getPath();

        // 将新坐标添加到我们的路径数组中
        path.push(newLatLng);

        // 在新坐标处添加一个新的标记
        var marker = new google.maps.Marker({
            position: newLatLng,
            title: '#' + path.getLength(),
            map: map
        });

        // 将地图重新居中于新坐标
        map.setCenter(newLatLng);

        // 更新我们的显示
        document.getElementById('myPosLat').innerHTML = posLat.toFixed(8);
        document.getElementById('myPosLng').innerHTML = posLng.toFixed(8);
        document.getElementById('watchStatus').innerHTML = 'Updated Position (#' + 
            path.getLength() + ')';

        // 将我们的最后坐标设置为新坐标
        lastLatLng = newLatLng;

    }
}

// 地理位置 watchposition 的 error handler
function errorCallback(error) {

  // 初始化我们的错误消息
  var errMessage = 'ERROR: ';
  var divWatchStatus = document.getElementById('watchStatus');

  // 根据 error code 参数设置消息
  switch(error.code)
  {
    case error.PERMISSION_DENIED:
      errMessage += 'User did not share geolocation data.';
      break;
    case error.POSITION_UNAVAILABLE:
      errMessage += 'Could not detect current position.';
      break;
    case error.TIMEOUT:
      errMessage += 'Retrieving position timed out.';
      break;
    default:
      errMessage += 'Unknown error.';
      break;
  }

  // 更新我们的状态
  divWatchStatus.innerHTML = errMessage;
}

// 按钮开始监控处理程序
function startWatch() {

  var divWatchStatus = document.getElementById('watchStatus');

  // 验证地理位置是否可用
  if (navigator.geolocation) {

    // 确保只有一个监控
    if (watchId == null) {

      // 设置我们的位置选项
      // maximum age 40 seconds
      // timeout of 20 seconds
      // enhanced accuracy on for mobile
      var posOptions = {maximumAge:40000,
        timeout:20000,
        enhancedAccuracy:true}

      // 开始我们的监控
      watchId = navigator.geolocation.watchPosition(successCallback,
        errorCallback,
        posOptions);

      // 更新我们的状态
      divWatchStatus.innerHTML = 'Watching Location ('+watchId+')';
    }
  } else {
    // 更新状态，指出地理位置不可用
    divWatchStatus.innerHTML = 'Geolocation Not Supported';
  }
}

// 按钮停止监控处理程序
function stopWatch() {

  // 验证我们当前是否有监控
  if (watchId != null) {
    // 清除我们的监控
    navigator.geolocation.clearWatch(watchId);

    // 将 watchId 标志设置为 null
    watchId = null;

    // 更新我们的状态
    document.getElementById('watchStatus').innerHTML = 'Off';
  }
}

// 初始化页面
window.addEventListener('load', initMap, false);

</script>
</head>
<body>
<div id="container">
  <div id="mapCanvas"></div>
  <div id="btnMap">
    <button id="startWatch">Start Watch</button>
    <br>
    <button id="stopWatch">Stop Watch</button>
  </div>
  <div id="location">
    <table id="status">
      <tr>
        <td>Latitude:</td>
        <td class="numDistance"><div id="myPosLat"></div></td>
      </tr>
      <tr>
        <td>Longitude:</td>
        <td class="numDistance"><div id="myPosLng"></div></td>
      </tr>
      <tr>
        <td colspan="2"><div id="watchStatus"></div></td>
      </tr>
    </table>
  </div>
</div>
</body>
</html>
```

让我们详细看看清单 10.4。当页面加载时，`initMap` 函数被调用并在页面上初始化地图。我们选择了纽约市的坐标，但您也可以轻松地设置不同的起始中心，或者仅在监控开始时加载地图。在 `initMap` 中，您在地图上创建了一个折线图层，这将允许您连接来自监控的坐标并向查看者显示“路径”。地图现已初始化，您可以开始位置监控。

首先，点击或轻触“开始监控”按钮。通常，系统会要求您确认是否要共享位置信息。点击后，`startWatch` 函数将被调用。在 `startWatch` 函数中，您通过检查全局 `watchId` 变量来检查是否已有监控进程运行。这可以防止启动多个监控进程。然后您设置位置选项并调用 `watchPosition` 方法。`watchPosition` 的返回值，即监控 ID，随后存储在 `watchId` 变量中，以便稍后可以使用它通过 `clearWatch` 停止该进程。

当 `watchPosition` 返回一个位置对象时，您提取纬度和经度属性，创建一个经纬度对象，然后使用 Google 的 `computeDistanceBetween` 方法计算与上一个经纬度坐标的距离。在这种情况下，您将新坐标、最后一个坐标和一个常量值传递给该方法，告知函数您希望返回值以英里为单位。然后您检查此距离是否大于四分之一英里，以避免地图被标记淹没。如果下一个点的距离大于该值，则将新坐标推送到折线路径点数组中，并添加一个新标记。将坐标推送到数组会更新地图上的线，因此每个新点都会使路径增长，显示您到过的地方，如图 10.4 所示。

本技巧展示了如何访问浏览器的位置，并在位置变化时收到通知。这些信息可用于广泛的应用程序，包括与基于位置的服务数据库集成，如 Yahoo Query Language 和 Google Places（测试版），以显示附近的兴趣点。

地理定位 API 提供了一个简便的接口，用于为网站和应用程序添加基于位置和位置感知的功能。可以设计的一些解决方案包括：

- 显示特定位置的信息
- 邻近感知
- 根据区域动态调整，例如语言和货币
- 集成地图和路线
- 为数据、图片和其他项目添加地理位置标记信息

在本章中，你学习了 `getCurrentPosition`、`watchPosition` 和 `clearWatch` 方法，以及这些方法的成功和错误回调函数。其可能性是无限的，现在浏览器能提供这个选项令人兴奋。

## 11 客户端存储

访问者浏览器中信息的持久化存储历来仅限于 cookie 中的键和值。Cookie 存储在大小和结构上是有限的，并且 cookie 会随每个请求发送到其对应的网站，造成不必要的开销。如果数据可以存储和本地检索，而不是每次使用时都由 Web 服务器检索，那么某些数据集可以改善用户体验。在 HTML5 中，增加了两种客户端存储设施：Web 存储（包括会话存储和本地存储）以及数据库存储。在本章中，你将了解这些新的客户端存储选项，并通过一些实践来开始在浏览器中本地存储数据。

## 客户端存储概述

在开始讨论新的存储 API 之前，让我们先看看之前浏览器中可用的本地存储信息方式。通常，要在访问者浏览器中存储信息以便稍后检索，你必须创建一个 cookie。存储的信息可能包括用户偏好设置、表单信息、用户密钥等。然而，cookie 的存储限制在大约 4KB，仅包含简单的键/值对，并且由于每个请求都附带 cookie 发送到服务器，增加了开销。

HTML5 提供的会话存储和本地 Web 存储选项与 cookie 类似，其结构是键/值格式，其中字符串值可以分配给基于字符串的键。可以通过在存储对象中请求相应的键来访问会话存储或本地存储中的值。会话存储和本地存储的区别仅在于数据在访问者会话中的作用域。在会话存储中，数据仅存储在与该网站的特定会话期间。一旦会话结束（通过关闭浏览器窗口或标签页），存储就会被移除。当用户返回时，会话存储将为空。相反，如果你希望数据在会话之间可用，无论是在另一个窗口中同时使用还是在以后的新会话中使用，那么你可以使用本地存储，即使关闭当前会话，它也会持久化保存。

键/值对限制了存储更复杂信息（或至少使其变得困难）。因此，增加了第三种类型的存储，以提供类似于服务器端通常使用的数据存储：数据库存储。数据库存储利用 SQLite 数据库或 IndexedDB，允许你存储更复杂的数据对象，正如本章后面将看到的。与本地存储类似，数据库存储在会话之间持久化。在你的网站或应用程序中使用哪种存储机制，取决于你需要存储的信息类型、数据的作用域以及你需要数据保存多长时间。表 11.1 提供了一种快速确定合适存储类型的方法。

### 数据安全

在讨论数据存储时，我们也必须讨论安全性。与在 Web 应用程序的服务器数据库中存储信息类似，客户端数据库存储也应遵循类似的安全指南。这一点尤其重要，因为与你可以控制防火墙、用户、密码和其他安全功能的服务器不同，访问者的浏览器位于直接网络之外。这使得对存储在客户端浏览器中的内容及其存储方式保持警惕变得更加重要。根据你存储的数据，加密可能是一个考虑因素，但如果你考虑对数据进行加密，你可能需要重新考虑是否应该首先存储它。

HTML5 中的存储选项采用“基于源”的安全策略，通过将对会话存储、本地存储和数据库客户端存储的访问限制为来自创建存储的同一域名的页面。这样，来自其他网站或页面的数据就无法被访问。然而，“源”安全实现使用页面的源作为访问会话存储和本地存储键/值对列表的决定因素。因此，存储有可能暴露给嵌入式脚本。这使得了解你在页面中使用的外部文件的行为变得更加重要。

> **注意**
>
> 你使用 `local`、`session` 或 `database` 对象存储的数据仅限于访问者当时使用的特定浏览器。如果用户使用不同的浏览器或不同的计算机返回你的网站或应用程序，那么存储将无法访问。你希望在任何地方都能访问的数据仍然需要存储在你的数据库服务器或云中。

**表 11.1 客户端存储类型和属性**

| 存储 | 格式 | 作用域 | 持久性 |



## 第11章 客户端存储

| 存储类型 | 数据格式 | 数据生命周期 | 作用域 |
|-----------|--------------|-------------------|-------------------|
| 会话存储 | 键/值 | 仅限会话 | 仅限会话 |
| 本地存储 | 键/值 | 跨会话 | 跨会话 |
| 数据库存储 | 结构化 | 跨会话 | 跨会话 |

不同的浏览器平台正在迅速采用客户端存储，Chrome 在这方面的支持是领先的。不同浏览器对于最佳数据库存储机制的实现仍存在争议，但表 11.2 列出了各种浏览器当前对客户端存储对象的支持情况。

**表 11.2 客户端存储浏览器支持情况**

| 浏览器 | 版本 |
| :-------------- | :------ |
| Android | 2.1+ |
| Chrome | 10.0+ |
| Firefox | 10.6+ |
| Internet Explorer | 8.0+ |
| iOS Safari | 3.2+ |
| Opera | 10.6+ |
| Safari | 4.0+ |

### 键和值：sessionStorage 和 localStorage

会话存储对象和本地存储对象在实现上相似，仅在数据的写入作用域和持久性方面有所不同，如表 11.1 所示。浏览器为每种存储类型提供了内置的存储接口：`sessionStorage` 和 `localStorage`，每个都使用键/值对列表来存储数据。你可以将一个值设置给一个键，然后通过请求该键来检索值。这两个存储对象都提供了设置值、获取值、移除键、检索列表中某个位置的键以及清除存储对象中所有键/值对的方法。每种存储对象类型的方法和属性是相同的，因为它们继承自 Web 存储规范中定义的同一个 `Storage` 接口：

- `setItem(key,value)`：设置作为参数传递的键/值对。如果键已存在，则使用传递的值更新。
- `getItem(key)`：返回作为参数传递的键对应的值。
- `removeItem(key)`：移除由传递的键定义的键/值对。
- `key(n)`：返回给定索引的键的名称。
- `clear`：移除所有键/值对。
- `length`：提供存储列表中键/值对的数量。

要设置一个项，你需要调用 `setItem` 并提供一个要设置的键和值：

```
setItem(key, value)
```

以下是参数说明：

- `key`：用于存储字符串值的键名
- `value`：需要与键一同存储的值

该值是字符串类型，因此如果存储的是数字，在存储中将被视为字符串，检索时需要转换回正确的数据类型。键和值随后将按无特定顺序存储在浏览器存储中该页面所属域的键值对列表中。

如果使用已存在的键设置项，则该键的值将更新为提供的新值。因此，`setItem` 方法同时充当创建方法和更新方法。要将值 `"book"` 存储在会话存储的 `"source"` 键下，可以在 JavaScript 中进行如下调用：

```
sessionStorage.setItem('source', 'book');
```

`setItem` 方法没有返回值，因此为防止可能的存储错误，可以将调用封装在 `try-catch` 块中。

要从会话存储或本地存储中检索键的值，请使用你感兴趣的键调用 `getItem`。返回值是字符串，随后可在脚本中使用：

```
string getItem(key)
```

此处 `key` 是用于检索对应值的字符串键。

要检索上一个示例中存储的值，可以通过执行以下调用从会话存储中请求 `"source"` 键：

```
textSource = sessionStorage.getItem('source');
```

由于会话存储和本地存储基于存储对象，也可以使用对象点表示法，通过将键作为属性名来访问存储的值，如下所示：

```
textSource = sessionStorage.source;
```

在简要讨论了会话存储和本地存储的获取与设置方法后，我们将展示一个基本配方的实际应用。我们将从会话对象开始展示配方，然后转向本地存储。

> **提示**
>
> 在 Firefox 等浏览器中，用户可以禁用存储。为验证存储是否可用，你的代码应尝试写入然后检索一个值。如果无法检索到该值，则可能是浏览器中禁用了存储。

### 初学者配方：获取和设置会话存储

在此配方中，HTML 页面将使用 `sessionStorage` 对象的 `getItem` 和 `setItem` 方法，在会话中存储并检索访问者查看页面的次数。每次刷新页面时，此数字会递增并向访问者显示。请执行以下步骤创建清单 11.1 中的页面：

1. 创建一个空白 HTML 页面，其中包含一个标题为 `divVisits` 的 div。
2. 在一组 `script` 标签中添加 `init` 函数，代码来自清单 11.1。
3. 添加 `window.addEventListener` 事件处理程序，以便在页面加载后启动 `init` 函数。

**清单 11.1** 使用会话存储显示页面访问量

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>11.1 会话存储页面访问量</title>
<script>
function init() {
  // 引用用于显示的 div
  var divVisits = document.getElementById('divVisits');

  // 检查浏览器是否支持 sessionStorage
  if (window.sessionStorage) {

    var visits; // 访问此页面的次数

    // 使用点表示法检查我们的变量是否存在
    if (sessionStorage.visits) {

      // 检索键并转换为整数
      visits = parseInt(sessionStorage.getItem('visits'));

      // 递增访问次数
      visits++;

    } else {
      // 默认为首次访问
      visits = 1;
    }

    // 更新我们的 visits 变量
    sessionStorage.setItem('visits',visits);

    // 显示会话访问次数
    divVisits.innerHTML = '会话页面访问次数：' + visits;

} else {
    // sessionStorage 不可用
    divVisits = 'Window sessionStorage 不可用';
}
}

// 在 onload 时启动我们的 init 函数
window.addEventListener('load',init,false);

</script>
</head>
<body>
    <div id="divVisits"></div>
</body>
</html>
```

当你在浏览器中加载清单 11.1 创建的页面时，`init` 函数将被启动。`init` 函数将首先通过检查 `window.sessionStorage` 来查看会话存储对象在窗口中是否可用。如果会话存储对象不可用，则会在页面上的 div 中显示一条消息。

假设会话存储对象可用，JavaScript 代码然后通过点表示法请求值来检查键 `"visits"` 是否存在：`sessionStorage.visits`。如果键 `"visits"` 存在，则会返回该值，并且检查将通过。否则，你就知道这是该会话的第一次，并将 `"visits"` 计数从 1 开始。如果该键在会话存储中，那么为了演示获取值的 `get` 方法，你将通过 `getItem` 方法检索该键的值。检索到值后，你使用 `parseInt` 将 `"visits"` 字符串值转换为整数数据类型。必须进行此转换，因为 Web 存储中的所有值都作为基本字符串存储。如果你的脚本存储并随后检索其他数据类型，你将需要将这些字符串转换为其适当的类型。

检索到访问次数并将其递增 1 或将初始值设置为 1 后，脚本将使用 `setItem` 方法更新会话存储中的 `"visits"` 键。如果该键之前不在会话存储中，则 `setItem` 将添加键/值对，但如果 `"visits"` 键已经在会话存储中，则该值将更新为新的访问次数。

### 用于查看存储的 Chrome 开发者工具

在浏览器中加载清单 11.1 创建的页面后，你可能想知道如何在脚本运行时验证本地会话存储中幕后发生的情况。Google Chrome 浏览器有一套名为开发者工具的工具集，你可能已经熟悉。如果在浏览器窗口中打开这些工具并刷新页面，你将能够在"资源"部分下看到会话存储的键/值对，如图 11.1 所示。

在图 11.1 中，左侧"会话存储"下显示了存储了键的域，右侧是当前存储的键/值对。在此例中，当前的访问次数值为 2，JavaScript 已将其显示给用户。Chrome 的开发者工具对于处理会话存储和本地存储非常有用，因为你不仅可以确认脚本正常工作，还可以通过用户界面添加、更新和删除键/值对。在当前版本的开发者工具中，如果你更改了键/值对，需要使用底部的"刷新"按钮刷新存储键/值视图窗格。

> **提示**
>
> 任何具有内置 `toString` 方法的对象都可以存储在会话存储和本地存储的键/值对的 value 字段中。甚至更复杂的 JSON 结构化对象也可以通过使用 `JSON.stringify(yourObject)` 和 `JSON.parse(itemRetrieved)` 方法转换 JSON 对象为字符串，然后将检索到的字符串转换回你的对象来存储。

![](img/de30ea99ecac39b49e690a84c48f43b9_295_0.png)

图 11.1 在 Chrome 开发者工具中查看会话存储键/值对

此配方执行了会话存储中键/值对的非常简单的设置和获取操作。下一个配方将包含错误处理，并展示会话存储在不同页面间的可用性。

### 初学者配方：来自会话存储的样式

在此配方中，你将为访问页面的访问者提供选择页面背景主题颜色的机会。访问者的选择将存储在会话存储中，并在第二个页面上检索以控制背景颜色。提供了一个主题重置选项，它将从会话存储中移除已存储的背景键/值对。以下是本配方中将使用的 `removeItem` 方法：

```
removeItem(key)
```

此处 `key` 是要移除的键字符串。

与任何数据存储机制一样，会话存储和本地存储有大小限制以保护浏览器和客户端机器。每个浏览器设置自己的大小限制，但与仅限 4KB 的小 Cookie 不同，为会话存储和本地存储分配的大小要大得多。在撰写本书时，例如 Internet Explorer 9 有 10MB 的限制。如果你的脚本尝试为键设置或更新值并达到此上限，将抛出一个错误。为防止你的脚本因该错误而突然终止，应将 `setItem` 方法调用封装在 `try-catch` 块中。在此配方中，我们将向你展示如果发生此错误如何捕获它。以下步骤和清单 11.2 将允许你创建配方的第 1 页：

1. 使用 `style`、`script` 和 `body` 标签创建清单 11.2 中的页面。
2. 添加 `themeContent` 和 `themeSettings` div，如清单 11.2 中的相应 HTML 所示。
3. 将 `initTheme`、`setTheme`、`resetTheme` 和 `applyTheme` 函数添加到你的脚本中。
4. 添加 `window.addEventListener` 语句以触发 `initTheme` 函数。

**清单 11.2** 在会话存储中设置主题

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>11.2 主题选择器 - 第1页</title>
<style>
#themeContent {
  background-color:#FFF;
  border-style:solid;
  border-width:2px;
}
#themeSettings {
  margin:10px;
}
</style>
<script>

var themeDiv; // 用于输出显示的div

// 初始化主题的函数
function initTheme() {

  // 为输出设置div引用
  themeDiv = document.getElementById('theme');

  // 检查浏览器是否支持sessionStorage
  if (window.sessionStorage) {

    // 设置按钮处理程序
    var btnResetTheme = document.getElementById('resetTheme');
    btnResetTheme.addEventListener('click',resetTheme,false);

    // 设置选择列表变化处理程序
    var selThemeColor = document.getElementById('themeColor');
    selThemeColor.addEventListener('change',setTheme,false);

    // 检查是否之前已设置主题颜色
    if (sessionStorage.themeColor) {

      // 设置初始主题颜色
      var themeColor = sessionStorage.getItem('themeColor');
      document.getElementById(themeColor).selected = true;

      applyTheme(themeColor);
    }
  } else {
    themeDiv.innerHTML = '不支持sessionStorage。';
  }
}

// 设置所选主题
function setTheme() {

  // 检索所选的主题颜色
  var themeColor = document.getElementById('themeColor').value;

  // 使用try catch设置主题颜色
  try {
    sessionStorage.setItem('themeColor',themeColor);
    applyTheme(themeColor);
  }
  catch(err){
    // 错误代码22 QUOTA_EXCEEDED_ERR 表示空间不足
    if(err.code == QUOTA_EXCEEDED_ERR){
      themeDiv.innerHTML = 'sessionStorage内存不足。';
      // 在此处执行任何其他所需的处理
    }
  }
}

// 重置主题颜色的函数
function resetTheme() {
  // 从会话存储中移除该项
  sessionStorage.removeItem('themeColor');

  // 重置显示
  document.getElementById('default').selected = true;
  document.body.style.backgroundColor = '';
  themeDiv.innerHTML = '主题已重置。';
}

// 将主题应用于页面
function applyTheme(themeColor) {
  document.body.style.backgroundColor = themeColor;
  themeDiv.innerHTML = '已应用主题 ' + themeColor + '。';
}

// 初始化窗口
window.addEventListener('load',initTheme,false);

</script>
</head>
<body>
<div id="themeContent">
  <div id="themeSettings">
    <h1>第1页</h1>
    选择主题：
    <select id="themeColor">
      <option id="default" value="">选择颜色...</option>
      <option id="blue" value="blue">蓝色</option>
      <option id="red" value="red">红色</option>
      <option id="yellow" value="yellow">黄色</option>
      <option id="green" value="green">绿色</option>
    </select>
    <button id="resetTheme">重置主题</button><br><br>
    <div id="theme"></div><br><br>
    <a href="11_3_theme_page_2.html">转到第2页</a>
  </div>
</div>
</body>
</html>
```

在第1页（即代码清单11.2）设置主题后，你可以通过加载另一个读取存储并使用主题信息来设置正确主题的页面，来验证主题已被存储。请按照以下步骤，使用代码清单11.3创建第二个页面，以显示之前选择的主题颜色：



## 根据代码清单11.3创建页面

1. 根据代码清单11.3创建一个包含相应部分的新页面。
2. 修改两个页面中的`<a>`标签，使其指向你实际页面的名称，以便你可以在页面之间来回导航。

### 代码清单11.3 显示主题 - 第2页

```html
<!DOCTYPE html>
<html><head>
<meta charset="UTF-8" />
<title>11.3 显示主题 - 第2页</title>
<style>
#themeContent {
    background-color:#FFF;
    border-style:solid;
    border-width:2px;
}
#themeSettings {
    margin:10px;
}
</style>
<script>

// 初始化页面
function init() {

    // 检索保存的主题颜色
    var themeColor = sessionStorage.getItem('themeColor');
    applyTheme(themeColor);
}

// 将主题应用于页面
function applyTheme(themeColor) {

    document.body.style.backgroundColor = themeColor;
    var themeDiv = document.getElementById('theme');
    themeDiv.innerHTML = themeColor + ' 主题。';

}

// 初始化页面
window.addEventListener('load',init,false);

</script>
</head>
<body>
<div id="themeContent">
  <div id="themeSettings">
    <h1>第2页</h1>
    <div id="theme"></div>
    <br><br>
    <a href="11_2_theme_page_1.html">转到第1页</a>
  </div>
</div>
</body>
</html>
```

当第1页加载到你的浏览器时，页面首先从会话存储中检索当前存储的主题颜色。页面首次运行时，没有主题，返回值为空，因此主题设置为浏览器的默认值。在页面后续加载时，颜色会被检索出来，设置为背景色，并设置为颜色选择控件中的选中值。

> **注意**
>
> 要运行涉及会话存储的示例，你需要将页面上传到服务器，而不是在“本地模式”下运行。原因是，在本地模式下，某些浏览器会抛出错误，指出不支持该操作。例如，在Firefox中，会抛出一个代码为9的“Operation is not supported”错误。

一旦加载，访问者可以将下拉列表选项更改为另一种颜色，这会更改页面背景色，并将该颜色以`themeColor`为键存储在会话存储中。在脚本中，这个用于存储设置的`setItem`调用已被包装在一个try-catch块中。如果由于大小限制而触发，代码会通知访问者会话存储已满，但你可以在此场景发生时执行任何所需的其他操作。设置主题颜色后，访问者可以点击“转到第2页”，这将加载第二个页面。由于第二个页面与第一个页面在同一个会话中，它也可以访问第1页保存的会话存储键/值对。然后第二个页面检索此项目，并将背景设置为存储的颜色。

在代码清单11.2中，你还添加了让访问者重置主题的选项。在这种情况下，示例使用`removeItem`方法从会话存储中移除键/值对。示例也可以通过使用空字符串值调用`setItem`来更新键。

在本章开头，我们讨论了会话存储如何允许你仅为该会话存储数据。如果你在同一个浏览器中的两个标签页或窗口中加载代码清单11.2中创建的页面，然后选择不同的颜色，每个标签页将有自己的背景色，因为每个标签页或窗口都有不同的会话。要使值在浏览器窗口或标签页之间可用，甚至在浏览器关闭并重新打开后仍然可用，你需要使用本地存储对象。我们将在下一个示例中研究本地存储对象。

## 中级技巧：使用本地存储存储表单

如前面的示例所示，会话存储为你提供了一种在访问者会话期间存储项目的方法，这对于短期存储很有用。然而，有时你会希望将数据存储在访问者的浏览器中，以便他们返回时使用，甚至在当前活动的会话中使用。这就是本地存储的价值所在。本地存储使用相同的键/值对列表，并使用`getItem`、`setItem`和`removeItem`网络存储方法来存储数据。重要的因素是，你存储在本地存储中的数据在会话关闭后仍然会持久化。

本示例展示了一个记住访问者之前填写的表单数据的示例。访问者可以访问你的网站，开始填写表单，然后导航离开或关闭浏览器。通常，当访问者返回网站时，会发现表单是空的。在这个示例中，当访问者填写表单时，JavaScript会捕获更改，并将表单字段和值存储在本地存储中。然后，如果页面关闭并重新加载，页面会检查本地存储是否有存储的表单数据，并自动用该信息填充表单。类似的实现甚至可以处理从多页表单收集表单数据，并将其本地存储，直到整个表单完成。

本示例采用了会话存储和本地存储的两个新概念：`key`和`length`。`key`方法允许你通过向`key`方法提供索引值来检索存储的键的名称：

```
DOMString key(index)
```

这里，`index`是要返回其键字符串的键/值对的索引。

该示例还使用了会话存储和本地存储的`length`属性，它返回会话存储或本地存储中键/值对的数量。要返回键/值对的数量，你可以使用如下调用：

```
var numItems = localStorage.length;
```

在这个示例中，你将同时使用`key`方法和`length`属性来遍历`localStorage`的键/值对。让我们按照以下步骤开始学习清单11.4的内容：

1. 创建一个空白HTML文件，并添加清单11.4中的`body` HTML代码，其中包含了你将要使用的表单和表单字段。为了简化，我们在表单字段上使用了`onchange`内联事件，但你也可以为每个字段替换为事件监听器。
2. 在HTML文件的`head`中添加`<script>`标签，并使用`window.addEventListener`函数，以便在页面加载时启动`checkStorage`函数。
3. 在脚本中添加`checkStorage`函数，如清单11.4所示。
4. 在脚本中添加`changeField`函数，如清单11.4所示，该函数将处理表单字段的更改。
5. 在Chrome浏览器中加载该文件，并打开开发者工具，定位到本地存储区域，然后在字段中输入信息。

### 清单11.4 将表单更改存储到localStorage中

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>11.4 使用本地存储保存表单数据</title>
<script>

// 用于读取存储并初始化表单的函数
function checkStorage() {

    // 检查本地存储是否可用
    if (window.localStorage) {

        var key, value, field;

        // 遍历本地存储
        for (var i = 0; i < localStorage.length; i++) {

            // 获取键
            key = localStorage.key(i);

            // 根据键设置字段
            field = document.getElementById(key);

            // 检查字段并赋值
            if (field) {
                // 获取值
                value = unescape(localStorage.getItem(key));
                // 设置字段值
                field.value = value;
            }
        } // 结束循环
    } // 结束本地存储检查
} // 结束函数

// 将更改的字段保存到 localStorage
function changeField(formField) {

    // 检查本地存储是否可用
    if (window.localStorage) {

        var key, value;

        // 将键设置为表单字段的 id
        key = formField.id;
        // 将值设置为表单字段的值
        value = escape(formField.value);

        // 尝试将项目设置到本地存储中
        try {
            localStorage.setItem(key, value);
        }
        catch (err) {
            if (err.code == QUOTA_EXCEEDED_ERR) {
                alert('localStorage 内存已用尽。');
            }
        }

    } else {
        alert('localStorage 未被支持。');
    }
}

// 从存储中初始化我们的表单
window.addEventListener('load', checkStorage, false);

</script>
</head>
<body>
<h1>我的表单</h1>
<form id='myForm'>
  <table>
    <tr>
      <td>名：</td>
      <td><input type="text" id="firstName" onchange="changeField(this);" /></td>
    </tr>
    <tr>
      <td>姓：</td>
      <td><input type="text" id="lastName" onchange="changeField(this);" /></td>
    </tr>
    <tr>
      <td>电子邮件：</td>
      <td><input type="email" id="email" onchange="changeField(this);" /></td>
    </tr>
    <tr>
      <td>电话：</td>
      <td><input type="tel" id="phone" onchange="changeField(this);" /></td>
    </tr>
  </table>
</form>
</body>
</html>
```

在`firstName`字段中输入你的名字并切换到下一个字段后，`firstName`字段的`onchange`事件将被触发。随后，`changeField`函数将被执行，并将表单字段`firstName`作为参数传入。`changeField`函数随后会将字段数据以键/值对的形式存储在`localStorage`中。该函数使用表单字段的ID作为键，字段值作为键/值对中的值。因此，如果你在执行此操作时在Chrome中打开了开发者工具，你现在应该会看到键`firstName`及其对应的文本输入值。

为了真正体会`localStorage`的强大功能，请关闭你的标签页或浏览器窗口，然后重新打开此表单页面。当你重新打开页面时，`checkStorage`函数将在页面加载时执行。此函数旨在检查你之前是否在本地存储中保存过任何表单信息，并检索这些信息。该函数将通过遍历`localStorage`列表来获取每个键/值对，检查是否存在与键名匹配的表单字段ID，如果匹配，则将字段值设置为检索到的值。

在这个示例中，你使用简单的文本字段来展示`localStorage`的功能，但它也可以用于其他类型的表单输入。`changeField`和`checkStorage`函数需要更新以处理不同字段类型（如选择列表或单选按钮）的不同逻辑，但其值可以像普通文本输入一样存储在本地存储中。

当页面完成存储表单信息并最终将表单提交给服务器后，理想情况下你会想要删除这些字段。除了你之前看到的`removeItem`方法外，存储API还提供了一个用于清除整个会话或本地存储的方法：`clear`。`clear`方法不接受任何参数，也不返回任何结果，它会从列表中“清除”页面域的所有键/值对。以下是调用示例：

```javascript
localStorage.clear();
```

执行这行代码将从本地存储列表中清除所有键/值对，无论它们是由哪个页面添加的，或者是何时添加的。由于这是一种“全有或全无”类型的方法，你应该绝对确定要清除会话存储或本地存储的内容。

到目前为止，在这个系列示例中，你已经学习了在客户端机器上为网站添加、更新和删除存储数据的基础知识。这假设访问者当时在单个页面上与网站交互。如果存储的信息是从浏览器中的另一个页面更改的，你无法自动处理之前打开的页面上的这种更改。客户端存储API为会话存储和本地存储更新提供了事件结构，你可以在打开的页面上捕获并处理这些事件。下一个示例将结合你所学的方法与存储更新事件，以刷新你的页面内容。

## 高级示例：在本地存储中捕获事件

在这个示例中，你将使用本地存储的方法和属性来实现一个笔记侧边栏，允许访问者在浏览网站时做笔记。笔记存储在访问者浏览器的本地存储中，并且笔记的顺序得以维护。访问者可以添加新笔记、更新笔记、删除笔记或删除所有笔记。此外，如果访问者在多个标签页或浏览器实例中查看网站，当一个页面上的笔记发生变化时，所有页面上的笔记都会自动更新。

为了根据访问者在另一个标签页或窗口中对笔记列表的更改，自动更新浏览器标签页或窗口中的笔记列表，你需要采用存储事件机制。与你见过的其他事件一样，当会话存储或本地存储被修改时，会触发存储事件。该事件可能在添加、更新或移除新的键/值对时发生。页面上的处理程序可以监听这些事件，并根据接收到的事件执行操作。`storageEvent`包含有助于确定所需操作的属性（表11.3）。在这个示例中，你将捕获该事件，验证它来自本地存储，向访问者提示更改，然后刷新笔记列表，以便显示当前列表。

### 表11.3 storageEvent属性

| 属性 | 类型 | 目的 |
|---|---|---|
| key | DOMString | 发生更改的键 |
| oldValue | DOMString | 旧值 |
| newValue | DOMString | 新值 |
| url | DOMString | 进行更改的页面的URL |
| storageArea | Storage | 此更新发生的存储区域 |

让我们按照以下步骤开始学习清单11.5：

1. 创建一个空白HTML页面，包含如清单11.5所示的HTML `body`和`style`标签。
2. 添加`<script>`标签和`keyCode`变量声明。此变量保存一个键，你将使用它作为每个存储笔记的前缀。
3. 添加`window.addEventListener`行以及`initNoteBoard`和`updateNoteBoard`函数。
4. 添加笔记函数：`addNote`、`changeNote`、`updateNote`和`removeNote`。`changeNote`函数将笔记加载到更新表单中，而`updateNote`则修改本地存储中的笔记。
5. 添加`clearAllNotes`函数，允许访问者重置笔记板。
6. 添加事件处理函数`onStorageEvent`，它将捕获任何存储事件。

### 清单11.5 在本地存储中存储笔记

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>11.5 在本地存储中存储笔记</title>
<style>
* {margin: 0; padding: 0;}
body {padding: 20px;}
h1 {font-size: 120%; margin: 0 0 .5em;}
section {width: 300px;}
#noteBoard, textarea {
  -moz-border-radius: 10px;
  -webkit-border-radius: 10px;
  border-radius: 10px;
  -moz-box-shadow: 0px 0px 4px rgba(0,0,0,.4);
  -webkit-box-shadow: 0px 0px 4px rgba(0,0,0,.4);
  box-shadow: 0px 0px 4px rgba(0,0,0,.4);}
#noteBoard {
  background: #FCFABA;
  float: right;
  padding: 10px 20px;}
#noteBoard div {
  border-bottom: 1px dashed #CCC;
  margin: 0 0 5px;
  padding: 5px 0;
  width: 100%;}
#noteBoard div.buttons {border: none;}
#addNote, #updateNote {float: left;}
```

## 高级技巧：在本地存储中捕获事件



```
#addNote {
  border-right: 1px dashed #ccc;
  margin: 0 50px 0 0;
  padding: 0 50px 0 0;
}
#updateNote { display: none; }
textarea {
  border: none;
  clear: both;
  height: 150px;
  margin: 0 0 10px;
  padding: 10px;
  width: 280px;
}
input[type="text"] { margin: 0 0 10px; padding: 4px; }
button { padding: 5px; }
</style>

<script>
// 存储条目的便条前缀
var keyCode = 'note';

// 初始化我们的便条板
function initNoteBoard() {
  // 设置存储变更的事件监听器
  window.addEventListener('storage', onStorageEvent, false);

  // 为新建和更新便条设置监听器
  var btnAddNote = document.getElementById('btnAddNote');
  var btnUpdateNote = document.getElementById('btnUpdateNote');
  btnAddNote.addEventListener('click', addNote, false);
  btnUpdateNote.addEventListener('click', updateNote, false);

  // 更新显示
  updateNoteBoard();
}

// 存储事件处理器
function onStorageEvent(eventObj) {
  if (eventObj.storageArea == localStorage) {
    // 提醒访客发生了变更
    alert(eventObj.key + ' 的值已从 "' +
      eventObj.oldValue +
      '" 变更为 "' +
      eventObj.newValue + '"。');

    // 更新显示
    updateNoteBoard();
  }
}

// 添加便条函数
function addNote() {
  // 检索我们当前的便条数量
  var numNotes = parseInt(localStorage.getItem('numNotes'));
  if (isNaN(numNotes)) {
    numNotes = 0;
  }

  // 设置键和值
  var noteKey = keyCode + numNotes;
  var noteValue = document.getElementById('note').value;

  // 设置便条
  localStorage.setItem(noteKey, noteValue);

  // 更新便条数量
  numNotes++;
  localStorage.setItem('numNotes', numNotes);

  // 更新便条板
  updateNoteBoard();

  // 重置便条输入框
  document.getElementById('note').value = '';
}

// 加载待更新便条的函数
function changeNote(noteKey) {
  // 在更新表单中设置键和值
  document.getElementById('oldKey').value = noteKey;
  document.getElementById('oldNote').value = localStorage.getItem(noteKey);

  // 显示更新便条区域
  document.getElementById('updateNote').style.display = 'block';
}

// 更新便条的函数
function updateNote() {
  // 检索便条的新值
  var key = document.getElementById('oldKey').value;
  var note = document.getElementById('oldNote').value;

  // 更新键值对
  localStorage.setItem(key, note);

  // 清空更新区域
  document.getElementById('updateNote').style.display = 'none';
  document.getElementById('oldKey').value = '';
  document.getElementById('oldNote').value = '';

  // 更新显示
  updateNoteBoard();
}

// 移除便条的函数
function removeNote(noteKey) {
  // 检索便条数量
  var numNotes = parseInt(localStorage.getItem('numNotes'));

  // 从便条键中提取索引
  keyIdx = parseInt(noteKey.substr(keyCode.length, noteKey.length));

  // 遍历便条并逐个向下移动
  for (var i = keyIdx; i < numNotes; i++) {
    localStorage.setItem(keyCode + i, localStorage.getItem(keyCode + (i + 1)));
  }

  // 更新便条数量
  numNotes--;
  localStorage.setItem('numNotes', numNotes);

  // 移除现在重复的最后一个便条
  localStorage.removeItem(keyCode + numNotes);

  // 更新显示
  updateNoteBoard();
}

// 移除所有便条的函数
function clearAllNotes() {
  // 检索便条数量
  var numNotes = parseInt(localStorage.getItem('numNotes'));
  if (isNaN(numNotes)) {
    numNotes = 0;
  }

  // 遍历所有便条键值对并移除
  for (var i = 0; i < numNotes; i++) {
    localStorage.removeItem(keyCode + i);
  }

  // 将便条数量更新为0
  localStorage.setItem('numNotes', '0');

  // 更新显示
  updateNoteBoard();
}

// 显示我们的便条
function updateNoteBoard() {
  // 设置显示区域
  var noteBoard = document.getElementById('noteBoard');

  // 检索便条数量
  var numNotes = parseInt(localStorage.getItem('numNotes'));
  // 如果没有便条则默认为0
  if (isNaN(numNotes)) {
    numNotes = 0;
  }

  var notes = '<div>我的便条：</div>';
  var key = '';
  var value = '';

  // 遍历便条
  for (var i = 0; i < numNotes; i++) {
    // 使用前缀创建键
    key = keyCode + i;

    // 检索键值
    value = localStorage.getItem(key);

    // 构建此便条的显示
    notes += '<div><p>' + value + '</p><div class="buttons">' +
             '<button onclick="changeNote(\'' + key + '\');">更改</button>' +
             '<button onclick="removeNote(\'' + key + '\');">移除</button>' +
             '</div>' +
             '</div>';
  }

  // 完成显示内容
  notes += '<div style="float:right;"><button id="clearAllNotes">移除所有便条</button></div>';

  // 设置列表内容到显示区域
  noteBoard.innerHTML = notes;

  // 为移除所有便条按钮设置监听器
  var btnClearAllNotes = document.getElementById('clearAllNotes');
  btnClearAllNotes.addEventListener('click', clearAllNotes, false);
}

// 初始化便条板
window.addEventListener('load', initNoteBoard, false);
</script>
</head>
<body>
<h1>便条板</h1>
<section id="noteBoard"></section>
<section id="addNote">
<h1>在此添加新便条：</h1>
<textarea name="note" id="note"></textarea>
<button id="btnAddNote">添加便条</button>
</section>
<section id="updateNote">
<h1>更新便条</h1>
<input type="text" name="oldKey" id="oldKey" disabled />
<textarea name="oldNote" id="oldNote"></textarea>
<button id="btnUpdateNote">更新便条</button>
</section>
</body>
</html>
```

页面加载时，初始化过程会启动`initNoteBoard`函数。该函数附加事件监听器以捕获任何存储事件，并将触发`storageEvent`处理程序。接下来，`initNoteBoard`通过检查本地存储来更新便条的显示。在`updateNoteBoard`函数中，脚本会首先检索键`numNotes`，该键记录了之前存储的便条数量。然后，使用`numNotes`，脚本将循环遍历并使用前缀`keyCode`（即`"note"`）和从0开始的索引来检索每个键值对。因此，要检索第一条便条，页面会调用`getItem`并使用键`note0`。使用`keyCode`和`numNotes`键有两个原因。首先，使用它们可以确保您不必遍历站点本地存储中可能存储的任何其他键值对；其次，这将使您能够有序地组织便条。请记住，对于会话和本地存储，列表中的键值对没有特定的顺序。浏览器使用`setItem`插入它们时没有特定顺序（参见图 11.2）。

![图 11.2 显示本地存储中多个键值对的示例输出](img/de30ea99ecac39b49e690a84c48f43b9_312_0.png)

图 11.2 显示本地存储中多个键值对的示例输出

这个技巧真正的强大之处在于事件处理。如果您在两个浏览器标签页或窗口中加载该页面，并在其中一个窗口中添加新便条，事件处理程序将被触发。在这种情况下，将调用`onStorageEvent`函数，该函数将执行两个操作。首先，该函数会提醒访客发生了变更，并提供有关更新的一些信息。其次，事件处理程序调用更新显示函数以显示更新后的便条列表。如果您尝试添加、更新和移除便条，您将看到此事件处理的行为方式。

如果您移除一条便条，事件处理程序将向您显示本地存储中发生的多个变更。原因是便条顺序的维护方式。为了维护列表的顺序，脚本使用一种算法，将被移除条目之后的条目依次向下移动，然后移除最后一个条目。请记住，`clear`方法不仅会移除您感兴趣的键值对，还会移除存储中的所有键值对。

> **注意**
>
> 存储事件不会在进行会话或本地存储修改的同一页面上触发。相反，存储事件是传播到其他浏览器窗口或标签页的通知。要在进行更改的页面上捕获变更，您需要在进行更改时直接调用相关逻辑。

在本例中，你使用了一个特定的键`numNotes`来保存已输入笔记的数量。此外，为了保持笔记的有序性，你使用了带有递增数字的键前缀，如`note0`、`note1`和`note2`。如果脚本需要基于不同的标准对列表进行排序，或者需要将你的笔记归类到不同的类别中，该怎么办？你可以使用 JavaScript 和对象自己设计方法，但借助 HTML5 及其定义的 Web SQL Database API，这项任务将变得非常简单，正如你将在本章最后一个示例中看到的那样。

## Web SQL Database API

正如你在本章前面的示例中所看到的，Session 和 Local Storage API 允许在客户端浏览器中存储简单的数据。如果你想存储更复杂的对象、属性和关系，你就需要利用新的 Web SQL Database API 或 IndexedDB API。与其他 API 一样，这些并非 HTML5 核心规范的一部分，而是一套正在被浏览器采纳的附加规范。总的来说，Web SQL Database API 目前得到了多个浏览器的支持，而 IndexedDB API 仍在定义中，支持有限。随着时间的推移，预计 IndexedDB 将获得更广泛的支持，但为了演示方便，本章我们将重点介绍 Web SQL Database API。

如果你有机会在服务器端页面和数据库访问方面工作过，很可能你已经使用过类似的基于 SQL 的数据库。如果没有，那么现在就是你机会，可以在浏览器中获得一个强大的数据管理存储系统。表 11.4 展示了浏览器对 Web SQL Database API 的支持情况。

**表 11.4 Web SQL Database 浏览器支持情况**

| 浏览器 | 版本 |
| --- | --- |
| Android | 2.1+ |
| Chrome | 9.0+ |
| Firefox | - |
| Internet Explorer | - |
| iOS Safari | 3.2+ |
| Opera | 10.6+ |
| Safari | 3.2+ |

Web SQL Database API 规范基于 SQLite，因此如果你已经在移动环境（如 iOS 开发）中使用过 SQLite，那么你会感到很熟悉。同时，如果你使用过像 MySQL 这样的服务器端数据库，基本的命令和结构也会让你觉得眼熟。如果你没有 SQL 经验，那么你可能需要寻找一些关于 SQL 命令的资料，但我们将在下一个示例中介绍基本的创建、读取、更新和删除命令。与 session 和 local storage 类似，出于安全目的，web 数据库仅对创建它的同一源的页面可用；然而，与 session 和 local storage 不同的是，web 数据库可以存储带有关系信息的复杂数据。

> **注意**
>
> 目前，关于 Web SQL Database API 使用的底层数据库格式存在一些争议。SQLite 被列在 W3 Web Database 规范中，并已被多个浏览器实现。然而，在获得普遍接受之前，W3C 的 web 数据库小组已暂停该规范的进一步开发。这导致了 IndexedDB 规范的进一步推进，该规范正获得越来越多的关注。

要与 web 数据库交互，API 提供了三个核心异步命令。这些命令通常是异步的原因，是为了在等待数据库调用返回时，浏览器页面的渲染不会被“阻塞”。根据事务中请求的数据量，页面可能需要等待几秒钟才能返回数据集。这三个核心命令允许你打开（或创建）数据库、创建事务，并在事务中执行 SQL 语句：

- `openDatabase`：打开一个现有的数据库，如果数据库不存在，则根据传递的参数创建一个数据库。
- `Transaction`：包含对数据库的命令，以便你可以在需要时对整个事务执行回滚。还有一个只读版本可用，即`readTransaction`。
- `executeSql`：在打开的数据库上运行实际 SQL 命令的方法。

`openDatabase`方法打开一个已建立的数据库，或者如果数据库不存在，该方法将根据参数中描述的信息自动创建数据库，然后打开数据库，如下所示：

```
WindowDatabase openDatabase(name, version, displayName, estimatedSize [, creationCallBack])
```

`openDatabase`方法的参数如下：

- `name`：数据库的名称
- `version`：你为数据库分配的版本号
- `displayName`：数据库的用户友好显示名称
- `estimatedSize`：数据库的预估大小
- `creationCallBack`：（可选）数据库首次创建时调用的函数

返回一个`WindowDatabase`对象，随后将用于执行事务。当浏览器窗口或标签页关闭时，数据库会自动关闭。

**提示**

`openDatabase`方法的版本号是一个你可以用来跟踪数据库结构和数据版本的值。如果你使用数据库来提供快速的本地数据查找，这会很有帮助。当你的查找数据发生变化，并且用户返回到你的网站时，你可以通过将该值存储在一个主 web 数据库的表中来检查这个版本。如果查找数据库不是最新的，那么可以安装一个新的。或者，你可以使用打开时的错误代码来验证它是否是错误的版本。



要查询数据库，必须执行事务请求。事务方法封装一个或多个`executeSql`命令，为数据库创建一个单一的事务来处理。如果任何 SQL 查询失败，该事务可用于回滚。事务的`callback`参数包含`executeSql`方法的内联函数，如下所示：

```
transaction(callback [, errorCallback] [, successCallback])
```

`transaction`方法的参数如下：

- `callback`：在事务中执行的功能
- `errorCallback`：（可选）处理任何发生错误的函数
- `successCallback`：（可选）如果事务中的所有过程都成功，则调用的成功函数

`executeSql`方法将你的 SQL 查询命令作为第一个参数，并且可以包含一个数组或可选参数、一个成功回调和一个可选的错误回调，如下所示：

```
executeSql(sqlStatement [, arguments] [, callback] [, errorCallback])
```

`executeSql`方法的参数如下：

- `sqlStatement`：要执行的 SQL 语句
- `arguments`：（可选）一个可选参数的数组
- `callback`：（可选）如果 SQL 语句执行成功，则执行的功能
- `errorCallback`：（可选）如果 SQL 语句执行产生错误，则执行的功能

数据库 API 方法的错误处理参数选项用于捕获在与数据库交互时可能发生的任何错误。这可能包括 SQL 错误或访问数据库时出现问题等实例：

- `UNKNOWN_ERR (0)`：发生了未列出的未知错误。
- `DATABASE_ERR (1)`：数据库中发生了不属于任何错误类别的错误。
- `VERSION_ERR (2)`：命令中声明的版本与数据库的版本不匹配。
- `TOO_LARGE_ERR (3)`：数据库返回给请求的结果数据集太大，无法返回。
- `QUOTA_ERR (4)`：没有剩余的存储空间，或者用户拒绝为你的数据库分配更多空间。
- `SYNTAX_ERR (5)`：由于语法错误导致请求失败。
- `CONSTRAINT_ERR (6)`：由于违反数据库结构中的约束导致请求失败。
- `TIMEOUT_ERR (7)`：由于无法及时建立数据库锁导致事务失败。

一个常见的错误是`SYNTAX_ERR`，它表示你的 SQL 命令存在语法问题。传递给错误处理程序的错误对象的消息部分对于提供有关特定错误代码的更多细节至关重要。

至此，你可能想知道所有这些如何协同工作来在数据库中存储和检索信息。下一个示例将把这些核心方法组合在一起，正是实现这一点。

## 进阶示例：使用 Web 数据库构建杂货购物清单

本示例将使用我们刚刚回顾的 web 数据库接口，创建一个完全存储在浏览器数据库资源中的购物清单。访客将能够向列表中添加物品，包括数量和名称，并从下拉菜单中选择该物品所在的杂货部门。每当添加一个物品，杂货清单就会更新并显示。列表将按部门分组，以方便购物。访客可以从列表中移除物品，也可以完全清空列表。如果访客离开后再次返回页面，页面将显示已存储的物品。

本示例创建的数据库将有两个表：一个`groceryitems`表用于保存列表中的物品，一个`departments`表，它是一个包含预定义部门列表的查找表。当页面首次加载时，数据库和表将被创建，`departments`表将填充部门信息。`groceryitems`表将有四个字段，如表 11.5 所定义。

`departments`表将有两个字段，如表 11.6 所定义。

默认情况下，当`departments`表创建时，脚本将在`departments`表中添加四个部门。

### 表 11.5 杂货物品表结构

| 字段 | 类型 | 描述 |
|---|---|---|
| `itemid` | INTEGER | 表中每个物品的唯一主键 |
| `quantity` | INTEGER | 需要获取的该特定物品的数量 |
| `itemname` | TEXT | 物品的名称 |
| `deptid` | INTEGER | 来自部门表的部门 ID |

### 表 11.6 部门表结构

| 字段 | 类型 | 描述 |
|---|---|---|
| `deptid` | INTEGER | 表中每个部门的唯一主键 |
| `deptname` | TEXT | 该特定物品需要获取的数量 |

> **提示**
>
> 与会话存储和本地存储类似，Chrome 开发者工具提供了一种高效的方式来查看 JavaScript 执行过程中的 SQLite 数据库。你可以在开发者工具窗口的“资源”部分下找到“数据库”部分。与会话存储和本地存储项目不同，数据库表和数据无法在开发者工具中编辑，但此功能可能会在将来添加。

出于调试目的，页面上还放置了一个“删除数据库”按钮，以便你可以删除数据库。目前，网络数据库规范不包含删除数据库的方法。为了变通并删除数据库，你必须“删除”已在数据库中创建的表，这样你的数据库就会变为空。在使用网络数据库 API 进行开发时，重新创建数据库对于验证你的 SQL 数据库创建事务很有用。

要创建杂货清单页面，请按照以下步骤操作：

1. 使用 HTML body、`shoppingdb`变量声明、`window.addEventListener` load 事件处理器和`init` JavaScript 函数创建页面的基本结构。
2. 添加从`init`函数调用的 JavaScript 函数：`openShoppingDb`和`dbPresent`。
3. 为了完成数据库的初始化，添加`initShoppingDb`、`onDbError`和`nullHandler`函数。`initShoppingDb`函数创建表并插入部门数据。`onDbError`函数是一个通用函数，用于处理脚本执行事务时可能发生的数据库错误，而`nullHandler`用于捕获成功的事务事件。如果你此时加载页面，你应该能在 Chrome 开发者工具中看到你的脚本正在创建数据库。
4. 你需要通过添加`initPage`、`getDepartments`和`showDepartments`函数，在页面显示时展示杂货物品。“获取并展示”技术将很常见，因为事务请求是异步的，需要回调函数来处理结果。在这种情况下，`getDepartments`执行从部门表获取部门的请求，然后由`showDepartments`函数来显示它们。`showDepartments`将为我们的选择列表创建选项。
5. 为了完成初始化时的显示，你需要展示之前存储在数据库中的任何杂货物品，因此添加清单 11.6 中的`getGroceryItems`和`showGroceryItems`函数。
6. 要添加物品，需要调用`addGroceryItem`函数，该函数将获取输入字段的值并将其插入到`groceryitems`表中。如果成功，页面将显示新的杂货物品列表。要删除物品，添加`deleteItem`方法。
7. 为了完成页面，添加`resetGroceryList`方法以清空杂货清单，以及用于删除数据库表的调试函数`removeDatabase`。

### 清单 11.6 使用客户端数据库创建杂货清单

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>11.6 数据库杂货清单</title>
<style>
  section {
    margin-bottom:20px;
  }
</style>
<script>
var shoppingdb = null; // 我们的数据库引用

// 启动页面初始化的函数
function init() {

  // 检查是否支持数据库
  if (window.openDatabase) {

    // 设置按钮点击处理器
    var btnAddGroceryItem = document.getElementById('addGroceryItem');
    var btnResetGroceryList = document.getElementById('resetGroceryList');
    var btnRemoveDatabase = document.getElementById('removeDatabase');
    btnAddGroceryItem.addEventListener('click',addGroceryItem,false);
    btnResetGroceryList.addEventListener('click',resetGroceryList,false);
    btnRemoveDatabase.addEventListener('click',removeDatabase,false);

    // 打开数据库
    openShoppingDb();

    // 检查我们是否拥有数据库引用
    if (shoppingdb) {

        // 检查数据库是否已初始化
        dbPresent();
    }
  } else {
    alert('此浏览器不支持数据库');
  }
}

// 打开数据库函数
function openShoppingDb() {

    // 尝试打开我们的数据库
    try {
        var dbSize = 5000000; // 5MB 大小
        shoppingdb = openDatabase('shoppingdb', '1.0', '购物清单', dbSize);
    } catch (err) {
        // 打开数据库时发生错误
        shoppingdb = null;
        console.log('打开数据库时出错: ' + err.code + ' - ' + err.message);
        return;
    }
}

// 检查数据库表是否存在的函数
function dbPresent() {
    // 开始我们的事务
    shoppingdb.readTransaction(function(tx) {
        // 执行 SQL 查询第一条记录
        // 如果成功，则初始化页面
        // 如果不成功，则初始化数据库
        tx.executeSql('SELECT 1 FROM departments', [],
            initPage, initShoppingDb);
    });
}

// 初始化页面的函数
function initPage() {
    // 获取部门列表
    getDepartments();
    // 加载存在的杂货物品
    getGroceryItems();
}

// 初始化购物数据库
function initShoppingDb() {
  // 开始我们的数据库事务
  shoppingdb.transaction(function(tx) {
    // 为数据库创建表
    tx.executeSql('CREATE TABLE IF NOT EXISTS ' +
      'groceryitems(itemid INTEGER NOT NULL PRIMARY KEY, quantity INTEGER, ' +
      'itemname TEXT, deptid INTEGER)',
      [], nullHandler, onDbError);
    tx.executeSql('CREATE TABLE IF NOT EXISTS ' +
      'departments(deptid INTEGER NOT NULL PRIMARY KEY, deptname TEXT)',
      [], nullHandler, onDbError);

    // 填充我们的部门表
    tx.executeSql('INSERT INTO departments(deptname) VALUES (?)',
      ['新鲜农产品'], nullHandler, onDbError);
    tx.executeSql('INSERT INTO departments(deptname) VALUES (?)',
      ['熟食'], nullHandler, onDbError);
    tx.executeSql('INSERT INTO departments(deptname) VALUES (?)',
      ['面包房'], nullHandler, onDbError);
    tx.executeSql('INSERT INTO departments(deptname) VALUES (?)',
      ['食品杂货'], initPage, onDbError);
  });
}

// 标准数据库错误函数
function onDbError(tx, err) {
  alert('发生数据库错误: ' + err.code + '|' + err.message );
}

// 我们的成功空处理器
function nullHandler(tx, r) {
  return;
}

// 获取部门列表的函数
function getDepartments() {
  // 开始我们的数据库事务
  shoppingdb.readTransaction(function(tx) {
    // 执行我们的 SQL 以检索部门
    tx.executeSql('SELECT * FROM departments ORDER BY deptname ASC', [],
      showDepartments, onDbError);
  });
}

// 显示检索到的部门的函数
function showDepartments(tx, rs) {
  // 获取部门选择框的引用
  var selectObj = document.getElementById('department');

  // 遍历部门记录集并添加到选择框
  for (var i=0; i < rs.rows.length; i++) {
    row = rs.rows.item(i);
    selectObj.options[selectObj.options.length] =
      new Option(row.deptname, row.deptid, false, false);
  }
}

// 获取杂货物品的函数
function getGroceryItems() {
  // 开始我们的数据库事务
  shoppingdb.readTransaction(function(tx) {
    // 检索物品列表
    tx.executeSql('SELECT * FROM groceryitems, departments WHERE ' +
    'groceryitems.deptid=departments.deptid ORDER BY deptname ASC',
      [], showGroceryItems, onDbError);
  });
}

// 显示杂货物品列表的函数
function showGroceryItems(tx, rs) {
  var myShoppingList = document.getElementById('myShoppingList');
  var tableRow = '<table>';
  var row = null;

  // 设置表格标题
  tableRow +=
    '<tr><td>数量</td><td>物品</td><td>部门</td><td>删除</td>' +
    '</tr>';

  // 遍历返回的记录集
  for (var i=0; i < rs.rows.length; i++) {
    // 检索我们的行
    row = rs.rows.item(i);

    // 构建我们的表格行
    tableRow += '<tr><td>' + row.quantity + '</td>' +
      '<td>' + row.itemname + '</td>' +
      '<td>' + row.deptname + '</td>' +
      '<td><button onclick="deleteItem(' +
    row.itemid + ');">X</button></td></tr>';
  }
  tableRow += '</table>';
```



```javascript
// set our info in the div
myShoppingList.innerHTML = tableRow;
}

// add a grocery item to our database groceryitems table
function addGroceryItem() {
  // open our database transaction async call
  shoppingdb.transaction(function(tx){
    // retrieve our data for the grocery item
    var itemname = document.getElementById('item').value;
    var quantity = parseInt(document.getElementById('quantity').value);
    var deptid = parseInt(document.getElementById('department').value);

    // perform our executeSql insert
    tx.executeSql('INSERT INTO groceryitems(quantity, itemname, deptid) VALUES (?,?,?)',
      [quantity, itemname, deptid], getGroceryItems, onDbError);
  });
}

// function remove an item from the list
function deleteItem(id) {
  // start our transaction
  shoppingdb.transaction(function(tx) {
    // execute sql to delete the item from the database
    tx.executeSql('DELETE FROM groceryitems WHERE itemid=?',
      [id], getGroceryItems, onDbError);
  });
}

// function reset grocery list
function resetGroceryList() {
  // start our transaction
  shoppingdb.transaction(function(tx) {
    // execute our sql to drop the grocery item table
    tx.executeSql('DROP TABLE groceryitems', [], nullHandler, onDbError);
  });
}

// function remove database
function removeDatabase() {
  // start our transaction
  shoppingdb.transaction(function(tx) {
    // drop our tables
    tx.executeSql('DROP TABLE departments', [], nullHandler, onDbError);
    tx.executeSql('DROP TABLE groceryitems', [], nullHandler, onDbError);
  });
}

// call init on load
window.addEventListener('load',init,false);
</script>
</head>
<body>
<section>
    数量：<input type="number" id="quantity" />
    物品：<input type="text" id="item" placeholder="Milk" />
    部门：<select id="department"></select>
    <button id="addGroceryItem">添加物品</button>
</section>
<section id="myShoppingList"></section>
<section>
    <button id="resetGroceryList">重置购物清单</button>
    <button id="removeDatabase">移除数据库</button>
</section>
</body>
</html>
```

当页面在浏览器中加载时，`init`函数将通过验证`window.openDatabase`方法是否可用，来检查Web SQL Database API是否可用。如果可用，则使用数据库参数调用`openDatabase`方法。在此例中，脚本将数据库大小大致设置为5MB，因为浏览器对于此大小或更小的数据库创建似乎不会向用户确认。如果你的数据库在创建时或之后超过此大小，浏览器将向用户确认以分配更多空间。如果这是你第一次运行该代码，那么数据库将被创建并返回句柄；否则，数据库将被打开。

由于本方案使用`departments`表的值来加载部门的下拉列表，你需要确保如果是新的数据库实例，你已用查询信息填充了`departments`表。为检查是否需要创建表，脚本通过执行一个简单的查询（在`dbPresent`方法中尝试从`department`表中选择第一行）来检查数据库表的存在。如果表尚不存在，则脚本将在`initShoppingDb`方法中创建两个表，并将部门值插入`departments`表。数据库加载后，脚本从数据库中将部门加载到下拉列表，并通过调用`getGroceryItems`方法显示任何已存储的购物物品。`getGroceryItems`方法将打开另一个事务，从`groceryitems`表中请求所有物品，如果成功，则将结果行集传递给`showGroceryItems`方法。`show`方法随后将循环遍历购物物品，并在页面的`myShoppingList`部分显示它们。

> **注意**

> `transaction`方法用于需要数据库写权限的SQL命令。由于要求写权限，该事务会对数据库加写锁，防止其他人在该时间写入数据库。如果你只是对数据库执行读命令，应使用`readTransaction`方法。`readTransaction`方法的调用方式与`transaction`方法相同。

一旦页面初始化完成并且数据库和部门填充完毕，访问者就可以输入数量和物品，并为购物清单中的新物品选择部门。然后，`addGroceryItem`将获取这些信息，创建一个数据库事务，并通过执行SQL插入将物品添加到内联函数调用中。如果插入失败，你将调用错误处理器`onDbError`，它将显示我们的错误。如果成功，脚本将调用`getGroceryItems`，随后调用`showGroceryItems`来显示从`groceryitems`表返回的结果行集。图11.3显示了输入若干物品后的输出。

![添加几个购物物品后的示例输出](img/de30ea99ecac39b49e690a84c48f43b9_324_0.png)

图11.3 添加几个购物物品后的示例输出

当调用`getGroceryItems`函数时，脚本将使用内联函数调用`executeSql`来调用`readTransaction`方法。该SQL命令从`groceryitems`表中选择所有记录，按部门分组，并按部门名称的字母顺序排序。此外，SQL命令通过`deptid`连接`groceryitems`表和`departments`表，因此返回集也将包含要显示的部门名称。如果`executeSql`调用成功，脚本将把结果返回给`showGroceryItems`，传递事务引用和结果记录集。为了显示记录集中的结果，脚本会循环遍历记录集的行。每一行代表SQL查询返回的一条记录，你可以通过点表示法引用每个字段。

要删除一个物品，访问者点击X按钮，该按钮调用`deleteItem`方法并传入物品ID。然后页面使用传入的物品ID从`groceryitems`表中删除该物品。如果调用成功，则通过获取和显示购物物品的函数刷新列表。最后，访问者可以重置购物清单，这将从`groceryitems`表中删除所有物品。

本方案是集成客户端Web数据库到你的网站和应用程序中的一个快速示例。该方案涵盖了记录的创建、检索、更新和删除，以及数据库的初始创建。这些功能为实现你自己的数据库存储提供了所需的构建模块。

## 小结

在本章中，你学习了一些在客户端浏览器上存储数据的令人兴奋的新方法。以前，客户端浏览器技术仅限于使用Cookie。随着会话存储、本地存储和Web数据库的加入，现在有了一个强大的平台（尽管还很年轻），你可以在其中选择多种方式来存储简单的键/值对或复杂的数据结构。利用这些存储选项，你可以创建强大的离线应用程序，减少与服务器之间的数据往返传输，并在客户端跨浏览器会话存储健壮的信息。

## 第12章 通信与线程

HTML5 API涵盖了广泛的改进和领域，但其中两个最新的API包括WebSocket和Web Workers API。这两组API填补了网站和Web应用程序开发中的一些关键空白。在这些API出现之前，与服务器建立双向通信通道非常困难。此外，在页面中执行繁重的处理会阻塞用户界面的用户交互。WebSocket API通过套接字连接提供了客户端JavaScript与服务器之间的双向通信，而Web Workers API则为客户端JavaScript开启了基本的线程选项。在本章中，你将学习如何通过一些简单但有效的方案来实现这些API，并以此为基础构建你自己的解决方案。

## WebSocket API概述

WebSocket API提供了一种通过直接套接字消息与服务器通信的新方法。这些消息是双向的，在连接打开期间，可以随时从客户端页面发送到服务器，或从服务器发送到浏览器页面。WebSocket使用一个独立的、服务器定义的协议，没有HTTP请求的开销，因此数据包也具有轻量级的优势。然而，默认情况下，要启用WebSocket连接，你必须在消息发送和接收的服务器上拥有相应的WebSocket服务。这些服务可以用多种语言编写。在HTML5之前，此通信功能只能通过安装专用对象、使用comet持久连接，或客户端频繁轮询服务器来实现。

要创建一个WebSocket连接，脚本会创建一个`WebSocket`接口的实例，并传入Web服务URL，如下所示：

```javascript
var myWS = new WebSocket("ws://some.webservice.com/");
```

当`WebSocket`对象被实例化时，它会尝试与在`WebSocket`对象构造函数中提供的URL上监听的服务建立套接字连接。如果连接成功打开，那么`WebSocket`对象实例将提供发送消息和关闭连接的方法，如下所示：

## 第12章 通信与线程

表12.1 WebSocket `readyState`属性值

| 值 | 常量 | 描述 |
|---|---|---|
| 0 | CONNECTING | 套接字连接正在尝试连接中。 |
| 1 | OPEN | 套接字连接已打开并就绪。 |
| 2 | CLOSING | 套接字连接正在关闭过程中。 |
| 3 | CLOSED | 套接字连接已关闭。 |

- `send(DOMString)`：以字符串形式发送数据。
- `send(ArrayBuffer)`：以`ArrayBuffer`形式发送数据。
- `send(Blob)`：以二进制对象（`Blob`）形式发送数据。
- `close([code][,reason])`：关闭套接字连接，可选参数包括一个无符号长整型代码和一个`DOMString`类型的原因说明。

要确定套接字连接何时准备好发送数据，你可以使用连接的`readyState`属性（该属性可以是表12.1所列的四个值之一），或者使用`onopen`事件。

以下是WebSocket实例上可用的事件：

- `onopen`：套接字连接已打开并就绪。
- `onclose`：套接字连接已关闭。
- `onmessage`：已在套接字连接上接收到一条消息。
- `onerror`：套接字连接发生错误。

表12.2显示了支持WebSocket API的浏览器版本。但请注意，不同浏览器的支持程度不同，在本章的具体示例中会酌情注明。

表12.2 WebSocket API浏览器支持情况

| 浏览器 | 版本 |
|---|---|
| Android | - |
| Chrome | 10.0+ |
| Firefox | 4.0+ |
| Internet Explorer | - |
| iOS Safari | 4.2+ |
| Opera | 11.0+ |
| Safari | 5.0+ |

## 初学者示例：通过WebSocket进行通信

本示例将使用WebSocket接口与服务器建立WebSocket连接，发送用户输入的消息，并接收服务器回送的相同消息回显。本例中，我们将使用在 www.websocket.org 上设置的一个免费测试WebSocket服务。这个免费在线服务通过验证你可以建立连接、发送消息和接收消息，使测试WebSocket脚本变得简单。要创建此连接，请执行以下步骤，最终得到清单12.1：

1. 创建一个空白HTML页面，包含消息输入元素、发送和关闭按钮，以及状态和消息结果显示的`div`元素。
2. 添加用于WebSocket和URL的全局变量。
3. 添加`init`函数和用于页面加载事件的事件监听器。
4. 添加`onOpen`、`onClose`、`onMessage`和`onError`函数，以处理WebSocket连接的事件。
5. 添加`postMessage`、`closeWS`和`updateStatus`函数，以处理发送消息、关闭连接和更新连接状态。

### 清单12.1 通过WebSocket发送和接收数据



```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>12.1 WebSocket通信</title>
<script>
// 设置我们的全局WebSocket引用
var directorWebSocket = null;

// 指定我们的WebSocket监听地址
var wsUri = 'ws://echo.websocket.org/';

// 在页面加载时创建WebSocket连接
function init()
{
    // 添加按钮事件处理程序
    var btnSend = document.getElementById('btnSend');
    var btnClose = document.getElementById('btnClose');

    btnSend.addEventListener('click',postMessage,false);
    btnClose.addEventListener('click',closeWS,false);

    updateStatus('正在初始化WebSocket连接');

    // 使用监听地址创建WebSocket实例
    directorWebSocket = new WebSocket(wsUri);

    // 设置WebSocket事件的处理函数
    directorWebSocket.onopen = function(evt) { onOpen(evt) };
    directorWebSocket.onclose = function(evt) { onClose(evt) };
    directorWebSocket.onmessage = function(evt) { onMessage(evt) };
    directorWebSocket.onerror = function(evt) { onError(evt) };
}

// WebSocket事件处理程序

// WebSocket连接成功打开
function onOpen(evt) {
  console.log('Director连接已打开');
  updateStatus('连接已打开');
};

// 通过WebSocket连接接收到消息
function onMessage(evt) {
  console.log('接收到消息：' + evt.data);
  updateStatus('已接收消息：' + evt.data);
  document.getElementById('messages').innerHTML = evt.data;
};

// 从WebSocket接收到错误
function onError(evt) {
  console.log('Director连接错误：' + evt.data);
  updateStatus('错误：' + evt.data);
};

// WebSocket连接成功关闭
function onClose(evt) {
  console.log('Director连接已关闭。');
  updateStatus('连接已关闭。');
};

// 客户端函数

// 通过WebSocket连接发送消息
function postMessage() {
  // 从输入框获取消息
  msg = document.getElementById('msg').value;
  console.log('正在发送ws消息：' + msg);
  updateStatus('正在发送消息：' + msg);

  // 使用send()发送消息
  directorWebSocket.send(msg);
}

// 通知WebSocket关闭
function closeWS() {
    console.log('正在断开ws连接');
    updateStatus('正在断开连接');
    // 通知WebSocket实例关闭连接
    directorWebSocket.close();
}

// 更新WebSocket状态的辅助函数
function updateStatus(msg) {
    document.getElementById('wsState').innerHTML = msg;
}

// 添加页面加载事件监听器以启动init函数
window.addEventListener('load', init, false);
</script>
</head>
<body>
<div id="btnTryCall">
    <input type="text" id="msg" />
    <button id="btnSend">发送消息</button>
    <button id="btnClose">关闭WebSocket</button>
</div>
<div id="wsState"></div>
<div id="messages"></div>
</body>
</html>
```

当清单12.1的页面加载时，会调用`init`函数。在`init`函数中，脚本添加按钮事件监听器，然后通过创建`WebSocket`接口的一个实例并传入地址来建立WebSocket连接。创建此实例后，本示例注册了`onopen`、`onclose`、`onmessage`和`onerror`事件，并将一个函数链接到每个事件。当WebSocket成功打开连接时，会触发`onopen`事件，并调用`onOpen`函数，更改页面上显示的连接状态。在本示例中，我们保留了控制台日志语句，以便你可以在浏览器的开发者日志中查看WebSocket连接的流程。

页面显示一个输入框，供用户输入消息并通过WebSocket发送给服务器。消息在`postMessage`函数中发送，该函数在WebSocket上调用`send`方法，并将消息作为参数传递。接收到消息后，WebSocket服务会重新打包文本字符串，并将该字符串作为消息发送回页面。`onmessage`事件处理程序捕获传入的消息，相应的`onMessage`函数接收传入的消息，并使用消息的`data`部分更新显示。

如果在WebSocket连接打开、使用或关闭过程中发生任何错误，`onerror`事件处理程序将捕获错误，并向用户显示错误的数据部分。一旦页面与WebSocket服务之间的对话完成，你可以通过调用WebSocket上的`close`方法来关闭WebSocket连接。

> **注意**
>
> 你的WebSocket实例向其发送消息并从中接收消息的服务通常是你自己设计的，并运行在你的Web服务器上。你可以在网上找到多种语言的开源示例，用于设置WebSocket服务器进程。在本书的在线参考列表中，我们包含了几个此类软件包的链接。

在本示例中，你与远程服务器建立了连接，并通过WebSocket连接来回发送消息。这对于双向通信，特别是从服务向已连接的浏览器页面主动发送消息，非常有用。

## 通过Web Worker进行多线程处理

JavaScript在HTML页面中运行的一个普遍问题是，JavaScript在页面上以单线程运行，在执行繁重处理时很容易阻塞界面。通过HTML5 Web Workers API，开发者有了一个新的机会来分离这种处理，让功能在一个后台线程上执行，其优先级低于HTML页面的主线程。这样，主线程可以保持不被阻塞，允许用户与页面交互，几乎不会产生负面影响。

HTML5中Web Workers API的实现提供了两种类型的Web Worker：专用（dedicated）和共享（shared）Web Worker。专用Web Worker特定于启动该Web Worker的页面，不能跨页面使用。相比之下，共享Worker可以在同一浏览器实例中来自同一源的多个页面之间共享。共享Worker有其自己的状态，该状态也跨越页面，正如你将在本章的最后一个示例中看到的那样。

那么，Web Worker究竟是什么呢？Web Worker是一个分离为文件的JavaScript脚本，可以在新线程上运行。在单独线程上运行的脚本甚至可以直接传递给Web Worker，而不是保存在专用的`.js`文件中。Web Worker可以通过在线程之间传递消息，与启动页面和主脚本进行通信，反之亦然。

### 表 12.3 工作线程事件

| 事件名称 | 属性 | 目的 |
|---|---|---|
| `message` | `onmessage` | 当收到消息时触发。将提供一个包含`data`成员的事件对象，其中包含该消息。 |
| `error` | `onerror` | 当工作线程中发生错误时触发。该事件提供一个包含错误信息的`data`成员。 |

> 提示
>
> Web工作者无法操作页面的DOM元素，因为Web工作者运行在与页面本身不同的线程上。只有主页面线程才能修改DOM。

要创建一个Web工作者的实例，你需要创建一个新的`Worker`接口实例，并传入要执行的脚本或文件，如下所示，用于创建一个专用工作者：

`var myWorker = new Worker('worker_script.js');`

上一代码中的专用Web工作者将在创建Web工作者时执行JavaScript。专用Web工作者将保持运行并可用，直到该线程被终止或创建该专用Web工作者的页面被关闭。以下是专用Web工作者可用的方法：

- `postMessage(Message [, MessagePort])`：向Web工作者线程发送消息。工作者线程通过后面将描述的`onmessage`事件“捕获”该消息。
- `terminate()`：终止调用该方法的工作线程。

专用Web工作者上有两个可用事件：`onmessage`和`onerror`。`onmessage`事件允许主页面脚本接收来自Web工作者线程的消息，或让Web工作者从主线程接收消息。

> 注意
>
> 如果你使用过支持多线程的编程语言，那么你可能了解线程安全问题以及在并发运行线程时可能出现的问题。在HTML5 Web Workers API中，通过序列化对象进行的线程间通信在很大程度上可以防止这些问题。为了防止其他并发问题，工作者线程无法访问DOM页面结构或非线程安全的组件。只有主页面线程才能更新页面的DOM元素。

### 表 12.4 Web Workers API 浏览器可用性

| 浏览器 | 版本 |
| :--- | :--- |
| Android | 2.1 |
| Chrome | 10.0+ |
| Firefox | 3.6+ |
| Internet Explorer | 10.0+ |
| iOS Safari | - |
| Opera | 10.6+ |
| Safari | 4.0+ |

请注意，Safari是唯一支持共享工作者（shared workers）的浏览器平台，本章稍后将介绍。在2.1版本之后，Android浏览器移除了对工作者的支持。

## 初学者指南：创建Web工作者

在本指南中，你将创建一个简单的专用Web工作者，使用一种基本的方法在Web工作者线程上在后台计算一系列数字的和。当HTML页面加载时，Web工作者将被启动。随着Web工作者处理数字范围的进程，工作者将向主脚本提供进度百分比消息。一旦Web工作者完成数字求和，工作者将向主脚本发送一条包含最终结果的消息。提供了一个终止按钮，以便用户可以随时终止工作者。

如上所述的Web工作者将在一个不阻塞主页面脚本和处理的线程中执行命令。为了演示，页面包含一个时间戳按钮，用于在页面上记录日期时间戳。随着工作者的进行，尝试点击日期时间戳按钮以验证主页面没有被Web工作者线程的活动阻塞。本指南将包含两个文件：清单12.2中的HTML页面和清单12.3中的Web工作者JavaScript文件。

1. 创建清单12.2中的页面，包含`output`标签、按钮和结果日志部分。
2. 向页面添加脚本部分，包括工作者变量和`startWorkerThread`初始化函数。
3. 添加`terminateWorker`函数以终止Web工作者线程。
4. 添加`getTimeStamp`函数和`window.addEventListener`触发器。

### 清单 12.2 向Web工作者发送消息

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>12.2 Simple Web Worker Communication</title>
<script>
// global reference to our web worker
var worker = null;

// on page load start the web worker
function startWorkerThread() {

  // add button event handlers
  var btnTimeStamp = document.getElementById('btnTimeStamp');
  var btnTerminateWorker = document.getElementById('btnTerminateWorker');

  btnTimeStamp.addEventListener('click',getTimeStamp,false);
  btnTerminateWorker.addEventListener('click',terminateWorker,false);

  // create the web worker instance
  worker = new Worker('12_3_simple_worker.js');

  // assign handler for receiving messages from web worker
  worker.onmessage = function (event) {
    // display the message in our result field
    document.getElementById('result').textContent = event.data;
  };
}

// handle the button to terminate the web worker
function terminateWorker() {

  // tell the web worker to terminate
  worker.terminate();
}

// local thread to time stamp and show how main thread is
// not blocked by calculations going on
function getTimeStamp() {

  // get the current date and time and add to the time log
  var currentDateTime = new Date();
  document.getElementById('timeLog').innerHTML += currentDateTime+ '<br>';
}

// kick off the web worker on page load
window.addEventListener('load',startWorkerThread,false);

</script>
</head>
<body>
  <p>Computing <output id="result"></output></p>
  <button id="btnTimeStamp">Time Stamp</button>
  <button id="btnTerminateWorker">Terminate Worker</button>
  <section id="timeLog"></section>
</body>
</html>
```

306 第12章 通信与线程

当页面创建Web工作者时，你会将要在新线程上执行的JavaScript文件名传递给新实例。在这个例子中，JavaScript文件名为`12_3_simple_worker.js`。清单12.3提供了该文件的代码，该文件遍历数字范围，将它们相加，并将消息发送回主页面脚本。

1. 创建清单12.3中的JavaScript文件，在顶部声明变量。
2. 添加for循环，从1循环到`maxLimit`，对数字求和并发送完成百分比状态。
3. 添加最后的`postMessage`以将总和发送给主页面脚本。

### 清单 12.3 在Web工作者中执行任务



## 第十二章 通信与线程

### 简单 Web Worker 示例

```javascript
// The 12.3 js simple web worker file

// initialize our variables
var sum = 0;
var currentPercentageComplete = 0;
var maxLimit = 100000000;

// loop
for (var j=0; j<=maxLimit; j++) {

  // perform long way of summation
  sum+=j;

  // determine percentage complete
  newPercentageComplete = Math.round((j/maxLimit)*100);

  // minimize messages sent by only sending message
  // when percentage has changed
  if (newPercentageComplete > currentPercentageComplete) {

    // send message back to main page thread
    postMessage(newPercentageComplete + '% complete');

    // update current percentage complete
    currentPercentageComplete = newPercentageComplete;
  }
}

// finally post resulting sum value to main page thread
postMessage('Sum = ' + sum);
```

当主页面在浏览器中加载时，窗口加载事件会调用`startWorkerThread`函数。该函数添加按钮监听器；创建一个新的`Worker`实例，传入 JavaScript 文件名；并将此引用赋值给`worker`变量。创建此实例后，脚本注册`onmessage`事件，并定义一个事件发生时执行的函数，以获取数据并在`result`输出中显示来自工作者线程的消息。当工作者线程通过`postMessage`向主脚本发送消息时，`onmessage`事件处理器将被触发。

当工作者实例被创建时，脚本被加载到线程中并自动执行。在下一个指南中，你将看到如何在创建线程后手动告诉脚本何时开始运行。

随着脚本在工作者线程中执行，通过一次循环一个数字（尽管为了演示目的，这是一种非常长且费力的方式）来计算总和。随着循环的进行，脚本会检查完成百分比是否增加。如果完成百分比发生了变化，则脚本通过`postMessage`命令向主页面发送一条消息，包括新的完成百分比。此发送的消息将触发主页面脚本中的`onmessage`事件处理器。主脚本然后获取此事件并访问包含实际文本的`data`成员。主脚本随后显示完成百分比，如图 12.1 所示。

如果用户确实想在不关闭页面的情况下终止工作者线程，可以使用终止工作者按钮，通过`terminate`方法告诉工作者立即停止。

### 中级食谱：添加双向通信

在上一个食谱中，你学习了主脚本如何创建专用 Web Worker，以及 Worker 如何将消息发回给主脚本。消息的传递被设计为可在不同线程间进行，这包括了创建 Worker 实例的主页面线程。这意味着主脚本和 Worker 线程可以通过`Worker`接口的`postMessage`方法相互发送消息。在本食谱中，主脚本将向 Web Worker 发送消息，而 Web Worker 将反过来向主脚本发送一条消息接收确认。

本食谱还探讨了在两个层面上对 Worker 的错误处理：通过`error`事件，以及通过返回给主脚本的自定义消息。通过`postMessage`方法发送的消息格式为序列化对象。这意味着你可以发送 JSON 格式的字符串来封装多个数据成员。在本食谱中，你将使用这种发送复杂数据的方法来通知主脚本所发送的消息类型以及消息的有效负载。此外，`onerror`事件处理程序被编程用于处理 Worker 脚本处理过程中发生的任何 JavaScript 错误。要开始本食谱，请按照以下步骤操作，最终将得到代码清单 12.4：

1. 创建一个空白 HTML 文件，并添加代码清单 12.4 中的`body` HTML，这包括输入字段、发送消息的按钮以及显示返回消息的部分。
2. 添加包含 Worker 声明和`onmessage`处理程序的脚本部分。
3. 添加`onerror`处理程序以捕获任何 Worker 错误。
4. 添加`postToWorker`函数，通过`postMessage`方法将文本输入发送给 Web Worker。

**代码清单 12.4** 创建客户端页面

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>12.4 Worker Communication</title>
<script>
// create our web worker
var worker = new Worker('12_5_two_way_worker.js');

// create handler for messages from web worker
worker.onmessage = function (event) {
  // retrieve message portion of data
  var msgFromWorker = event.data;

  // check to see our type of message
  switch (msgFromWorker.msgType) {
    case 'MSG':
      // message sent from web worker - display
      var workerResponse = document.getElementById('workerResponse');
      workerResponse.innerHTML = 'Worker sent: ' + msgFromWorker.msg;
      break;
    case 'ERR':
      // error sent from web worker - alert user
      alert('Error from worker: ' + msgFromWorker.msg);
      break;
  }
};

// error handler for web worker
worker.onerror = function (error) {
  // simply alert user with error
  alert('Error from worker: ' + error.message);
};

// post the input to the web worker
function postToWorker() {
  worker.postMessage(document.getElementById('inputForWorker').value);
}

// initialize our handlers
function init() {
  var btnPostToWorker = document.getElementById('btnPostToWorker');
  btnPostToWorker.addEventListener('click',postToWorker,false);
}

window.addEventListener('load',init,false);
</script>
</head>
<body>
  <p>Enter a text message for the worker thread (leave blank to have worker
return a message type of error):</p>
  <input id='inputForWorker' />
  <button id="btnPostToWorker">Send to Worker</button>
  <section id="workerResponse"></section>
</body>
</html>
```

与上一个食谱一样，你将使用一个外部 JavaScript 文件来存放你的 Web Worker 代码。代码清单 12.5 包含了该文件的脚本，并可以通过以下步骤创建。确保文件的名称与你在代码清单 12.4 的主脚本中用于 Worker 实例化的名称相同。

1. 创建一个空白文件，并添加代码清单 12.5 中的`onmessage`事件处理程序。
2. 添加`if`条件以及相应的代码段，以检查输入是否有效，并向主脚本发回错误或确认消息。

**代码清单 12.5** 添加 Web Worker

```javascript
// The 12.5 2 way Web Worker js file

// Catch messages sent to the web worker
onmessage = function(event) {
  // check for empty data and send back an error
  if (event.data === '') {
    // post message to client with error info
    postMessage({msgType:'ERR',msg:'Invalid data entry'});
  } else {
    // post message to client confirming receipt
    newMessage = 'Worker received "' + event.data + '"';
    postMessage({msgType:'MSG',msg:newMessage});
  }
}
```

当 HTML 页面加载时，Web Worker 通过加载 JavaScript Worker 文件来创建，但请注意，与之前的食谱不同，Web Worker 在创建时并未执行任何操作。Web Worker 将等待任何传入的消息触发消息处理程序。在 HTML 页面上，用户会被提示在输入字段中输入一个文本字符串，并点击“Send to Worker”按钮。“Send to Worker”按钮触发一个`postMessage`，将文本字符串发送给 Web Worker。然后 Web Worker 检查该字符串是否为空，如果为空，则使用一个消息类型为“ERR”且包含相应消息的 JSON 字符串，将消息发回给主脚本。如果 Web Worker 收到的消息不为空，则 Worker 将该字符串包装在另一个字符串中以显示接收到的内容，并以相同的 JSON 格式（消息类型为“MSG”）将这个更新后的消息发回。

在错误或消息被发送回主脚本后，主脚本中的`onmessage`事件处理程序会触发，并接收到从 Web Worker 来的消息。该函数会检查发送的消息类型，然后要么向用户发出错误警报，要么使用 Web Worker 发来的消息更新结果字段，如图 12.2 所示，从而完成通信循环。

要触发错误消息，请将输入字段留空，然后点击“Send to Worker”按钮向 Web Worker 发送一个空字符串。

本食谱和上一个食谱都利用了专用 Web Worker，它们仅对创建它们的页面可用。但在某些情况下，你可能需要使用一个在跨页面共享作用域的 Web Worker。在下一个食谱中，我们将解释共享 Web Worker 的结构以及如何实现与 Web Worker 的连接。

### 高级食谱：利用共享 Web Worker

正如你在前面的食谱中所看到的，专用 Web Worker 的作用域仅限于创建了该 Web Worker 的页面。在所有方面，Web Worker 在该环境中被沙箱化以执行线程安全操作。HTML5 Web Workers API 提供了第二个 Worker 接口，称为`SharedWorker`。该接口提供了相同的 Web Worker 功能，但其作用域可在同一浏览器的同一源下跨多个页面共享。共享 Web Worker 中的功能可以像专用 Web Worker 一样对每个请求独立，或者 Web Worker 可以跨页面共享其环境，正如你将在本食谱中看到的。

由于一个共享 Web Worker 实例可以有多个客户端与线程通信，因此其接口与专用 Web Worker 接口略有不同。共享 Web Worker 使用一个端口分配来标识页面到 Web Worker 的连接。这个标识被共享 Web Worker 用来识别消息的来源以及应该将消息发送给谁。以下是`SharedWorker`的创建方式：

```javascript
var sworker = new SharedWorker('mySharedWorker.js');
```

**表 12.5 SharedWorker 事件**

| 事件名称 | 属性 | 用途 |
| :--- | :--- | :--- |
| connect | onconnect | 当接收到消息时触发。会提供一个包含 data 成员的事件对象及消息。 |

共享 Web Worker 有一个事件`connect`，当客户端线程连接到共享 Web Worker 时执行，如表 12.5 所示。如前所述，每个客户端连接都有一个端口标识符来唯一标识该连接。`postMessage`方法和`message`事件被推送到端口，从而在连接级别执行消息传递。

在本示例中，我们将解释如何跨多个页面使用共享 Web Worker，从任何已连接的页面提供的值中计算平均值。当平均值发生变化时，结果将发送到每个页面进行显示。为便于测试，客户端页面使用 iframe 在一个容器页面中显示，而不是在浏览器中单独加载每个页面。因此，需要创建三个文件：主容器页面（用于保存每个客户端页面的 iframe）、接受用户输入并连接到共享 Web Worker 的客户端页面，以及实际的共享 Web Worker JavaScript 文件。让我们从清单 12.6 所示的容器文件开始：

1. 创建一个空白的 HTML 页面，包含 HTML body 和三个 div 标签中的 iframe，如清单所示。
2. 接着添加`style`标签以及 div 和 iframe 标签的样式，使 iframe 以三列等宽形式显示在页面中。至此，容器文件完成。

**清单 12.6** 创建客户端页面容器

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>12.6 SharedWorker Across Pages</title>
<!-- This is purely a container page to show
multiple pages using a shared worker. This would
perform the same if the pages were in separate
tabs or windows in the same browser. -->
<style>
  div{float:left;width:33.3%;height:500px}
  iframe{width:100%;height:100%}
</style>
</head>
<body>
    <div>Client Page 1<iframe src="12_7_sw_client.html"></iframe></div>
    <div>Client Page 2<iframe src="12_7_sw_client.html"></iframe></div>
    <div>Client Page 3<iframe src="12_7_sw_client.html"></iframe></div>
</body>
</html>
```

接下来，你需要按照清单 12.7 中的代码创建客户端页面，该页面将被加载到容器的每个 iframe 中，并显示输入字段供用户输入数字：

1. 创建一个空白的 HTML 页面，包含如清单 12.7 所示的`body`，包括`input`标签、SEND NUMBER 按钮和日志区域。
2. 添加`script`标签和一个名为`sworker`的共享 Worker 实例的全局引用。这将是用于发送和接收消息的`SharedWorker`实例。
3. 添加`window.addEventListener`行和`init`函数，该函数创建共享 Worker 连接并为该客户端在共享 Worker 上的端口注册`onmessage`处理器。
4. 添加`sendNumber`函数，该函数获取输入值并将数字发送到共享 Worker 进行处理。

**清单 12.7** 创建客户端页面



```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>12_7 SharedWorker Client</title>
<script>

// global SharedWorker reference
var sworker = null;

// initialize the page and SharedWorker connection
function init() {

    // reference our log output section
    var logOutput = document.getElementById('log');

    // add the button listener
    var btnSendNumber = document.getElementById('btnSendNumber');
    btnSendNumber.addEventListener('click',sendNumber,false);

    // create our SharedWorker reference
    sworker = new SharedWorker('12_8_shared_worker.js');

// onmessage handler for messages from SharedWorker
sworker.port.onmessage = function(msg) {

    // based on type of message display appropriately
    switch (msg.data.msgType) {
      case 'LOG':
        // received a log message, add to log
        logOutput.innerHTML += msg.data.msgText + '<br>';
        break;

      case 'AVE':
        // received a new average value, update average
        var aveOutput = document.getElementById('average');
        aveOutput.innerHTML = msg.data.aveValue;

        // add log entry
        logOutput.innerHTML += msg.data.msgText + '<br>';
        break;
    }
}

// send the number entered to the SharedWorker
function sendNumber() {

    // retrieve the number
    var numToSend = document.getElementById('numberToSend').value;

    // post message to the SharedWorker (notice port)
    sworker.port.postMessage(numToSend);

    // reset our value input field
    document.getElementById('numberToSend').value = '';
}

// add our event page load initialize call
window.addEventListener("load", init, false);

</script>
</head>
<body>
    Current Average: <output id="average"></output>
    <br><br>
    <input id="numberToSend" />
    <button id="btnSendNumber">Send Number to SharedWorker</button>
    <hr width="100%">
    Messages from SharedWorker:<br>
    <section id="log"></section>
</body>
</html>
```

当清单 12.7 中的客户端页面加载时，你将初始化与从文件`12_4_sworker.js`构建的共享 Worker 的连接。本示例的最后一步是创建共享 Worker JavaScript 文件。共享 Worker JavaScript 文件在清单 12.8 中提供，并通过以下步骤创建：

1. 创建一个 JavaScript 文件，命名为`12_4_sworker.js`（或者你选择的任何名称，只要与客户端 HTML 页面中共享 Worker 文件参数匹配即可）。

2. 在脚本顶部添加全局变量和`onconnect`事件处理器。

3. 将`sendAllConnections`和`updateAverage`函数添加到脚本中。

**清单 12.8 添加共享 Worker .js 文件**

```javascript
// 12.8 SharedWorker js file for averaging numbers across pages

// Initialize the connections array for storing the connection ports
var count = 0;
var connections = new Array();

// Initialize our average formula variables
var average = 0;
var numValues = 0;
var sumValues = 0;

// onconnect event for SharedWorker
onconnect = function(msg) {

    // get the reference for this connection
    var port = msg.ports[0];

    // store this connection reference for future messages
    connections[count] = port;

    // increment the number of connections we have
    count += 1;

    // respond to the client and initialize their average
    port.postMessage({msgType:'LOG',msgText:'[SW] Now connected [' + count + '].'});

    port.postMessage({msgType:'AVE',msgText:'[SW] Average updated: ' + average + '.', aveValue:average});

// create handler for when we receive a message from the client
port.onmessage = function(msg) {
  // set the value passed into the SharedWorker
  var newValue = msg.data;

  // respond that we received the value
  port.postMessage({msgType:'LOG',msgText:'[SW] Received: ' + newValue + '.'});

  // update the Average with the new value
  updateAverage(newValue);
}

// helper function to send a message to all clients
function sendAllConnections(msgTypeVal,msgVal) {

  // loop through the clients and postMessage
  for (var i=0; i<count; i++) {

    // post message to client with our JSON formatted message
    // with message type, text, and current average
    connections[i].postMessage({msgType:msgTypeVal,
      msgText:msgVal,
      aveValue:average});
  }
}

// our simple average update function
function updateAverage(newValue) {

  // adjust average formula variables
  numValues++;
  sumValues += parseFloat(newValue);

  // create new average
  average = Math.round((sumValues / numValues)*100)/100;

  // update all clients with new average
  sendAllConnections('AVE','[SW] Average updated: ' + average + '.');
}
```

要运行本示例，请将容器 HTML 页面加载到你的浏览器中。请注意，在撰写本示例时，只有 Safari 支持 SharedWorker 接口。当容器加载时，它将在三个 iframe HTML 页面中加载客户端页面的实例，如图 12.3 所示。每个客户端页面将创建一个 SharedWorker 接口的实例，该实例创建一个共享的 Web Worker。

线程并连接客户端页面与单个共享 Web Worker。当客户端页面连接时，共享 Web Worker 中的`onconnect`事件处理程序将被触发。该事件处理程序将获取连接所绑定的端口引用，以便后续可以向此客户端连接发送消息，并将此端口存储在`connections`数组中。接下来，共享 Web Worker 在`onconnect`事件处理程序中向刚刚连接的端口发送一条日志消息，说明客户端已连接以及这是第几个客户端连接。此外，共享 Web Worker 向客户端发送当前平均值，以初始化客户端页面上的显示。最后，共享 Web Worker 为此端口注册一个`onmessage`事件处理程序，以便当客户端页面向共享 Web Worker 发送消息时，可以捕获该消息。

当共享 Web Worker 在初始连接时将日志或平均值消息发回客户端页面时，客户端页面中的`onmessage`处理程序将捕获这些消息。客户端页面将根据传递的 JSON 字符串中的字段确定消息类型，并通过添加日志消息和在需要时设置平均值来更新显示。

一旦所有客户端页面都初始化了与共享 Web Worker 的连接，用户就可以在任何客户端页面中输入一个数字，并点击“将数字发送到 SharedWorker”按钮。这将调用客户端 JavaScript 中的`sendNumber`函数，进而向共享 Web Worker 发送一条包含所输入数字的消息。请注意，这里使用的是`sworker`的端口来调用`postmessage`，如下所示，这与向专用 Web Worker 发送消息略有不同：

```
swworker.port.postMessage(numToSend);
```

此 post message 命令将用户输入发送到共享 Web Worker，然后共享 Web Worker 将在已注册的`onmessage`事件中获取此数字，并向客户端端口返回一条已收到该数字的日志消息。发送完收到日志消息后，共享 Web Worker 将更新全局变量中的当前平均值，并将此新平均值发送给所有已连接的客户端。用于向所有客户端发送消息的辅助函数会遍历`connections`并在消息中发送新平均值。图 12.3 展示了此操作的一个示例运行。

`SharedWorker`接口应被视为尚处于早期阶段；它仅在少数浏览器平台中受支持，并且功能有限。该接口还存在一些尚未解决的挑战，例如处理客户端断开连接的问题，但该接口前景广阔，未来将为开发者提供大量功能。

> **提示**

在开发自己的 Web Worker 结构时，最好先在主页面中开发 Worker 功能，以便于调试。一旦核心 Worker 功能正常工作，你就可以将代码封装在单独的 Worker 文件和线程中。

## 总结

在本章中，这些操作示例展示了如何使用 WebSocket API 和 Web Workers API 来实现一些关键的通信模式。WebSocket API 提供了一种易于使用的服务器与客户端页面之间的通信方法，而 Web Workers 提供了一种高效的方式，将繁重处理从网站或应用程序的主线程中卸载。通过在应用程序中利用这些新的 API，你可以增强整体用户体验和功能。本章中的这些操作示例仅触及了使用这些 API 所能实现功能的皮毛，但为你实现自己的解决方案奠定了基础。

# 第 13 章：HTML5 浏览器体验

由于安全原因，浏览器历来与操作系统的其余部分隔离。随着 HTML5 的出现，一些 API 被提出，允许与用户可能使用的设备的操作系统进行更紧密的集成，并提供更接近原生应用程序的典型用户体验。我们将其中三个 API 归入本章关于浏览器体验的内容中。这三个 API 允许以下类型的用户体验：

- 在浏览器外部和页面内部拖放对象

- 应用程序缓存存储，允许离线使用网页

- 桌面通知，提醒用户浏览器窗口中的事件

在本章中，你将了解这些 API，尽管它们比我们已经介绍过的其他 API 更不成熟，并且还有改进的空间。我们将从一个比较完善的 API 开始，并以一个尚未被大多数浏览器支持但前景广阔的 API 结束。那么，让我们从拖放 API 开始深入探讨。

## 拖放 API

拖放 API 已被添加到 HTML5 API 中，允许用户选择一个对象，将该对象拖到页面上的某个区域，然后释放该对象以触发某些操作。拖放功能的基础是四个部分的组合：

- 一个可从浏览器内部或外部拖拽的对象

- 一个用于接收对象的拖放区域

- 允许控制拖放行为的事件

- 一个用于传输对象上下文数据的数据存储

要允许浏览器中的对象被拖拽，有一个名为`draggable`的新属性。`draggable`属性有三个可能的值：`true`、`false`和`auto`。如果`draggable`设置为`true`，则该对象可以被用户拖拽。如果该属性设置为`false`，则该对象不能被拖拽。如果该值设置为`auto`，则浏览器将使用该类型对象的默认可拖拽值，就像未提供`draggable`属性一样。例如，你可能已经注意到你可以抓取页面上的图像并拖动它。当然，当你释放它时，什么也不会发生，因为没有定义拖放区域；但它仍然可以被拖动。要创建一个可拖拽的`div`，代码应如下所示：

```
<div class="divClass" id="myDiv" draggable="true">My Div</div>
```

要创建一个可以释放对象的区域，HTML5 中添加了一个名为`dropzone`的属性。`dropzone`属性可以有三个值之一：`copy`、`move`或`link`。你选择的值取决于你希望在对象释放时执行的操作类型。`dropzone`在 div 上的声明示例如下：

```
<div id="divDropzone" dropzone="copy" ...
```

`dropzone`属性还可以使用过滤器，例如格式列表`f:/image/png`，它表示只有 PNG 类型的图像文件可以拖放到该拖放区域上。

接下来，你必须通过捕获由你指定为`draggable`对象和`dropzone`对象的元素触发的事件，来处理项的实际拖放操作。当用户开始拖动一个对象时，`ondragstart`属性或`dragstart`事件将被触发。通过在此事件上调用一个函数，你将能够存储一些关于正在拖动对象的数据。当该对象随后被释放到`dropzone`上时，`dropzone`将触发一个名为`ondrop`或`drop`事件的属性事件。当此事件被触发时，存储在正在拖动对象上的数据就可以被检索出来，并用于执行脚本选择的任何函数。要传递此信息，你需要使用一个名为`DataTransfer`的新接口。

`DataTransfer`接口有各种属性和方法，但用于传递信息的两个是`setData`和`getData`。以下是`DataTransfer`接口可用的方法：

- `setData(format, data)`：将类型为 format（例如文本）的数据设置到数据存储中。

- `getData(format)`：从数据存储中检索类型为 format 的数据。

- `clearData([format])`：清除数据存储中提供的可选格式的数据。如果未提供格式，则清除整个存储。

- `void setDragImage(image, long x, long y)`：使用在 x,y 坐标处的图像向用户显示。

- `void addElement(element)`：将提供的元素添加到数据存储中。

表 13.1 显示了支持拖放 API 的每个浏览器的版本。

表 13.1 拖放 API 浏览器可用性

| 平台 | 版本 |
|---|---|
| Android | 2.1+ |
| Chrome | 10.0+ |
| Firefox | 3.6+ |
| Internet Explorer | 6.0+ |
| iOS Safari | - |
| Opera | - |
| Safari | 3.2+ |

## 初学者指南：跨`div`拖放



本指南将使用拖放功能，允许用户将便签图片拖拽到软木板投放区。当便签被放下时，所选便签图片的新副本将被添加到软木板，如图 13.1 所示。

本指南将向你展示通过使用`draggable`和`dropzone`属性以及关键事件和`DataTransfer`接口来创建拖放用例的基础知识。代码清单 13.1 展示了此示例的代码，但你可以按照以下步骤创建文件：

1. 创建一个空白 HTML 页面，包含代码清单 13.1 中所示的`style`和`body`部分。在`body`部分，务必为便签图片和看板`div`添加事件处理属性。
2. 在 HTML body 中添加`fileAttributes`部分，用于显示文件属性。

![](img/de30ea99ecac39b49e690a84c48f43b9_351_0.png)

www.it-ebooks.info

## 322 第 13 章 HTML5 浏览器体验

3. 添加`dragStartHandler`和`dropHandler`函数，这两个函数都接收事件触发的目标元素以及事件本身。
4. 添加`getStartPos`和`init`函数，分别用于检索被拖动元素中的拖动起始位置和初始化样式。

```
代码清单 13.1  基本拖放示例
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>13.1 基本拖放</title>
<style>
#notes {
    float:left;
    height:220px;
    width:50px;
    text-align:center;
    border-style:solid;
    border-width:2px;
    border-color:#333;
    background-color:#666;
}
#board {
    float:left;
    width:300px;
    height:220px;
    border-style:solid;
    border-width:2px;
    border-color:#333;
    background-image:url('corkboard.png');
}
</style>
<script>
// 用于保存图片点击偏移量的变量
var imgOffsetX = 0;
var imgOffsetY = 0;

// 处理拖动开始的函数
function dragStartHandler(tgt, evt) {
    evt.dataTransfer.setData("Text", tgt.id);
}

// 处理放置动作的函数
function dropHandler(tgt, evt) {
// 阻止浏览器默认动作发生
// 例如用新标签页打开拖动的项目
if(evt.preventDefault) {
  evt.preventDefault();
}

// 检索被拖动图片的 id
var elImgId = evt.dataTransfer.getData("Text");

// 创建新的图片实例
var oImg = new Image();

// 设置图片的 src
oImg.src = document.getElementById(elImgId).src;

// 设置图片位置
oImg.style.position='absolute';
var newX = evt.x - imgOffsetX;
var newY = evt.y - imgOffsetY;

var divLeft = tgt.x;
var divTop = tgt.y;
var divWidth = parseInt(tgt.style.width);
var divHeight = parseInt(tgt.style.height);

// 确保图片完全在 div 内
var imgWH = 50;
if (newX<tgt.offsetLeft) {
  newX=tgt.offsetLeft
} else if (newX+imgWH>(tgt.offsetLeft + divWidth)) {
  newX = tgt.offsetLeft + divWidth-imgWH;
}
if (newY<tgt.offsetTop) {
  newY=tgt.offsetTop;
} else if (newY+imgWH>(tgt.offsetTop + divHeight)) {
  newY = tgt.offsetTop + divHeight-imgWH;
}

// 定位图片
oImg.style.left = newX+'px';
oImg.style.top = newY+'px';

// 将图片追加到 div 投放区
tgt.appendChild(oImg);

// 用于设置便签图片点击点的辅助函数
function getStartPos(evt) {
    imgOffsetX = evt.offsetX;
    imgOffsetY = evt.offsetY;
}

// 初始化看板宽度和高度
function init() {
    document.getElementById('board').style.width = '300px';
    document.getElementById('board').style.height = '220px';
}

// 页面加载时调用 init 函数
window.addEventListener('load',init,false);

</script>
</head>
<body>
    <h1>将便签拖到软木板上：</h1>
    <div id="notes">
        <img id="note_blue" src="post_blue.png" onmousedown="getStartPos(event);"
             ondragstart="dragStartHandler(this, event);"><br>
        <img id="note_green" src="post_green.png" onmousedown="getStartPos(event);"
             ondragstart="dragStartHandler(this, event);"><br>
        <img id="note_pink" src="post_pink.png" onmousedown="getStartPos(event);"
             ondragstart="dragStartHandler(this, event);"><br>
        <img id="note_yellow" src="post_yellow.png" onmousedown="getStartPos(event);"
             ondragstart="dragStartHandler(this, event);">
    </div>
    <div id="board" dropzone="copy" ondrop="dropHandler(this, event);"
         ondragover="return false;"></div>
</body>
</html>
```

当页面在浏览器中加载时，每个图片都设置了一个`ondragstart`事件处理程序，以调用`dragStartHandler`并传入相应的元素。注意，你不需要添加`draggable`属性，因为图片的默认设置就是`draggable`。在`div`看板那一行，你将该`div`设置为`dropzone`，并设置了`ondrop`和`ondragover`事件处理程序。`ondragover`事件处理程序是必需的，用于覆盖标准浏览器功能，只需在事件触发时返回`false`。如果用户选择一个便签并开始拖动它，那么`dragStartHandler`函数将被调用。此外，`onmousedown`事件将触发一个辅助函数，该函数仅将 x 和 y 坐标存储在变量中，用于计算便签在看板上的定位。在`dragStartHandler`函数中，脚本在`DataTransfer`接口中设置了正在被拖动的元素的 ID。

然后用户将便签放到看板上，`dropHandler`函数将被调用。在放置处理程序中，你做的第一件事是通过调用事件的`preventDefault`来否定浏览器的默认行为。这将允许你控制浏览器中放置动作的行为。脚本随后从数据存储中获取元素 ID，创建一个新图片，设置其源，并进行一些计算以在看板上设置新图片的位置。请注意，由于可用的定位方法，这种定位仅在 Chrome 等某些浏览器中有效，但这对于示例来说并不关键。一旦图片被创建并定位，你就可以将图片追加到看板`div`，从而产生便签图片的一个副本。

这是一个简单的拖放功能示例。在下一个指南中，你将把这些概念与其他拖放事件结合起来，以更全面地控制拖放体验。

## 进阶指南：利用事件和 dataTransfer

在上一个指南中，你仅使用了拖放 API 的基本功能来捕获拖放到某个区域的图像，并在该区域添加一个新图像。除了基本的拖放事件外，拖放 API 接口还提供了其他几个事件，允许你同时控制拖动和放置行为。利用这些事件，你可以控制诸如可以拖动的项目类型以及它们可以被放置到何处等行为。以下是拖放 API 产生的其他事件：

- `dragstart`：拖动操作已在可拖动对象上开始。
- `drag`：对象正在被移动。
- `dragenter`：拖动操作进入一个可用的投放区。
- `dragleave`：拖动操作离开一个可用的投放区。
- `dragover`：对象正在一个可用的投放区上被拖动。
- `drop`：对象被释放到一个可用的投放区上。
- `dragend`：对可拖动对象的拖动操作已结束。

在本指南中，你将运用拖放 API 来创建通常被称为汉诺塔的数学游戏，该游戏由数学家爱德华·卢卡斯于 1883 年发明（你可以在维基百科 http://en.wikipedia.org/wiki/Tower_of_Hanoi 上找到关于该游戏历史的更多信息）。基本规则是：你有三根柱子，最左边的柱子上有一系列从大到小堆叠的圆盘。圆盘的数量在不同的棋盘上可能不同。目标是将整个堆叠移动到最右边的柱子上，一次只能移动一个圆盘，并且只能放在空的柱子上或放有比要移动的圆盘更大的圆盘的柱子上。我们将使用拖放 API 事件和`dataTransfer`对象来创建这个游戏，并确保强制执行游戏规则。

## 326 第13章 HTML5中的浏览器体验

在游戏过程中，如果玩家尝试将圆盘放置在有更小圆盘的堆栈上，代码将不允许圆盘被放下。但是，如果移动是有效的，圆盘将被移动并添加到堆栈中。此外，如果用户尝试移动不是特定堆栈顶部的圆盘，该操作将被禁止。每次将圆盘移动到最右边的堆栈后，你将检查用户是否已成功移动整个堆栈并表示祝贺。让我们开始吧，看看如何使用各种事件来执行游戏规则：

1. 创建如清单13.2所示的页面，包含用于方块和三个放置区域的`style`和`body`标签。注意，在方块上添加`draggable`属性，以确保浏览器理解这些`div`可以被拖动。
2. 添加`script`标签，添加`initTowers`函数，并添加`window.addEventListener`来触发初始化。
3. 为方块添加事件处理程序；`blockHandleDragStart`和`blockHandleDragEnd`函数将只允许堆栈顶部的方块被拖动。这些函数还会在拖动开始和结束时改变样式。
4. 为了配合方块处理程序，你需要放置区域处理程序。添加堆栈放置区域处理程序函数`towerHandleDragOver`、`towerHandleDragLeave`和`towerHandleDragDrop`，以控制将方块移动到其上时堆栈放置区域的样式，并处理方块在堆栈上的放置。
5. 在脚本顶部添加全局变量声明，用于堆栈方块游戏地图（名为`towers`的二维数组）、游戏中的方块数量以及玩家已执行移动次数的计数器。

> **注意**

> 你可以在本书网站上找到此配方的图片（参见引言部分了解位置信息）。

### 清单13.2 为汉诺塔应用拖放功能



```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>13.2 Towers Game</title>
<style>
.towerDropZone {
  float: left;
  height: 200px;
  width: 200px;
  margin: 5px;
  padding: 15px;
  position:relative;
  background-color:#fff;
  background-image:url(tower.png);
  background-repeat:no-repeat;
  background-position:bottom;
}
.towerDropZone.over {
  border-radius: 15px 15px;
  background-color:#EEE;
}
.tower {
  width: 200px;
  position:absolute;
  bottom:1px;
  border:none;
}
.block {
  height: 25px;
  margin:1px auto;
  border: 1px solid #ccc;
  border-radius: 15px 15px;
  background-color:#00F;
  color:#FFF;
  text-align:center;
  font-size:19px;
  font-weight:bold;
}
</style>
<script>
// 声明堆栈地图、方块数量和步数计数器
var towers = [[],[],[]];
var numblocks = 4;
var numMoves = 0;

// 初始化事件处理程序和状态
function initTowers() {

  // 为堆栈放置区域设置事件处理程序
  var towerDropZones = document.querySelectorAll('#towers .towerDropZone');
  [].forEach.call(towerDropZones, function(tdz) {
    tdz.addEventListener('dragover', towerHandleDragOver, false);
    tdz.addEventListener('drop', towerHandleDragDrop, false);
    tdz.addEventListener('dragleave', towerHandleDragLeave, false);
  });

  // 为各个方块设置事件处理程序
  var blocks = document.querySelectorAll('.block');
  [].forEach.call(blocks, function(block) {
    block.addEventListener('dragstart', blockHandleDragStart, false);
    block.addEventListener('dragend', blockHandleDragEnd, false);
  });

  // 设置初始堆栈0上方块状态的地图
  for (var i=numblocks-1;i>=0;i--) {

    // 将方块添加到第一个堆栈（3,2,1,0）的地图上
    towers[0].push(i);

    // 为方块创建不同的宽度
    document.getElementById(i+"block").style.width = (90 + i * 30) + "px";
  }
}

// 处理方块拖动到堆栈放置区域的事件
function towerHandleDragOver(e) {
    // 阻止默认操作以便我们可以放下
    if (e.preventDefault) {
        e.preventDefault();
    }

    // 将效果设置为移动选项
    e.dataTransfer.dropEffect = 'move';

    // 设置堆栈的外观以显示可用
    this.className = "towerDropZone over";

    return false;
}

// 处理方块拖动离开堆栈放置区域的事件
function towerHandleDragLeave(e) {
    // 将堆栈放置区域外观恢复为正常
    this.className = "towerDropZone";
}

// 处理将方块放置在堆栈放置区域上的事件
function towerHandleDragDrop(e) {

    // 阻止默认操作
    if (e.preventDefault) {
        e.preventDefault(); // 必要；允许我们放下
    }

    // 将堆栈放置区域外观恢复为正常
    this.className = "towerDropZone";

    // 获取通过dataTransfer传递的JSON数据
    var blockInfo = JSON.parse(e.dataTransfer.getData("Text"));

    // 设置源/目标堆栈和方块信息
    var blockId = blockInfo.blockId;
    var blockNum = parseInt(blockInfo.blockId);
    var fromTowerId = parseInt(blockInfo.fromTowerId);
    var toTowerId = this.id;

    // 获取堆栈元素
    var tower = document.getElementById("tower"+toTowerId);

    // 确定方块是否可以放置在堆栈上的逻辑
    var towerheight = towers[toTowerId].length;
    if ( towerheight == 0) {
      // 堆栈为空 - 在堆栈中的<p>占位符之前插入方块
      tower.insertBefore(document.getElementById(blockId),document.getElementById("p"+toTowerId));
    } else {
      // 堆栈上有方块 - 获取堆栈顶部的方块值
      var topBlock = towers[toTowerId][towerheight-1];

      // 检查方块是否可以放置在顶部方块上
      if ( topBlock > blockNum) {
        // 将方块插入到顶部方块之前，以便放置在其顶部
        tower.insertBefore(document.getElementById(blockId),document.getElementById(topBlock+"block"));
      } else {
        // 方块不能放置在当前顶部方块上
        // 返回false以终止操作
        return false;
      }
    }

    // 更新此方块的游戏地图位置
    towers[toTowerId].push(blockNum);
    towers[fromTowerId].pop();

    // 递增已执行的移动次数
    numMoves++;
    document.getElementById("numMoves").textContent = numMoves;

    // 检查游戏是否结束 - 所有方块按顺序在第三个堆栈上
    if (towers[2].length==numblocks) {

      // 游戏完成 - 使方块不可拖动
      var blocks = document.querySelectorAll('.block');
      [].forEach.call(blocks, function(block) {
        block.draggable = false;
      });

      // 通知用户
      alert("恭喜 - 你已移动了整个塔。");
    }
}

// 处理方块开始被拖动的事件
function blockHandleDragStart(e) {

  // 获取方块id和源堆栈id
  var blockId = this.id;
  var fromTowerId = this.parentNode.parentNode.id;

  // 获取变量以检查拖动的方块是否是堆栈顶部的方块
  var towerheight = towers[fromTowerId].length;
  var topBlock = towers[fromTowerId][towerheight-1];
  var thisBlock = parseInt(blockId);

  // 检查这是否是堆栈顶部的方块
  if (topBlock == thisBlock) {

    // 方块是顶部方块，所以我们可以移动它
    this.style.opacity = '0.4';

    // 创建用于通过dataTransfer传递信息的JSON包
    var blockinfo = {
      "blockId": blockId,
      "fromTowerId": fromTowerId};

    // 设置dataTransfer的数据
    e.dataTransfer.setData("Text", JSON.stringify(blockinfo));

  } else {

    // 方块不是顶部方块
    this.style.opacity = '1.0';

    // 返回false以防止方块被拖动
    return false;
  }
}

// 处理方块拖动操作结束的事件
function blockHandleDragEnd(e) {
  // 将方块不透明度恢复为正常
  this.style.opacity = '1.0';
}

// 在页面加载时调用我们的初始化函数
window.addEventListener('load',initTowers,false);
</script>
</head>
<body>
    <h1>塔游戏</h1>
    <p>将左侧堆栈上的方块移动到最右侧的塔上。<br>
    方块只能移动到空塔或有更大方块的塔上。</p>
    <div>已执行移动次数：<span id="numMoves">0</span></div>
    <section id="towers">
        <div class="towerDropZone" id="0">
            <div class="tower" id="tower0">
                <div class="block" id="0block" draggable="true">1</div>
                <div class="block" id="1block" draggable="true">2</div>
                <div class="block" id="2block" draggable="true">3</div>
                <div class="block" id="3block" draggable="true">4</div>
                <p id="p0" />
            </div>
        </div>
        <div class="towerDropZone" id="1">
            <div class="tower" id="tower1"><p id="p1" /></div>
        </div>
        <div class="towerDropZone" id="2">
            <div class="tower" id="tower2"><p id="p2" /></div>
        </div>
    </section>
</body>
</html>
```

那么，现在你已经构建好了页面，并且理想情况下通过来回拖动方块玩了几轮，你已经对基于玩家操作如何触发事件有了概念。但是，让我们花几分钟时间来了解一下游戏逻辑如何与拖放功能集成的一些细节。

当页面加载时，该配方声明了游戏地图的全局变量（如果你编写过基于位置的游戏，那么游戏地图对你来说将是第二天性；否则，游戏地图可以简单地理解为游戏棋子在任何特定时间所在位置的表示）、游戏中的方块数量以及玩家移动次数的计数器。这里的游戏地图是一个二维数组，用于跟踪每个三个堆栈上有哪些方块。放置区域或堆栈具有从零开始的基于整数的ID，这些ID直接映射到堆栈。

运行`initTowers()`函数后，页面会为每个汉诺塔塔注册放置区域的事件处理器，以及那些将要移动的方块的事件处理器。接着，脚本通过将方块3、2、1、0添加到塔零（第一个塔）的数组中来设置当前游戏地图。你会注意到添加的顺序是反过来的，这代表了方块3比方块2大，依此类推。此外，你还使用这个顺序通过样式属性动态地调整方块的大小，这完成了游戏棋盘的初始化。

现在让我们看看游戏流程。当用户将一个方块从一个塔拖到另一个塔时，随着事件的触发，会发生几件事。首先，拖动开始事件被触发，`blockHandleDragStart()`函数执行。此函数首先验证所选方块是否是其所在塔的顶部方块。如果不是，则函数返回`false`，从而阻止该方块被拖动。如果是顶部方块，那么该步骤会创建一个包含一些关键信息的JSON字符串：方块ID以及方块被拖动的源塔ID。然后，这些数据被设置到`DataTransfer`接口中，以便当方块被放置到新塔上时，你能够知道被选中的方块以及它来自哪个塔。为了向用户显示你正在拖动特定的方块，你还需要在函数中更改该方块的透明度。

当方块被拖入一个放置区域或塔时，拖动经过事件被触发，`towerHandleDragOver()`函数执行。此函数的目的是让玩家知道他们已经移动到了一个放置区域上。这是通过更改被拖动经过的塔`div`区域的样式来实现的，如图13.2所示。

然而，一个关键点是包含了`preventDefault()`命令。正如你在前面的步骤中所看到的，为了阻止浏览器执行默认操作（这可能会导致游戏流程出现问题），你必须使用此命令。如果方块只是“路过”塔的放置区域，那么拖动离开事件将被触发，`towerHandleDragLeave()`函数将被执行。此函数将离开的塔放置区域的样式更回正常视图。

当方块被放置到塔的放置区域时，大部分的游戏逻辑在`towerHandleDragDrop()`函数中执行。当此函数启动时，你首先调用`preventDefault()`方法，再次阻止浏览器使用其拖放事件的默认逻辑。接下来，该步骤将检索`dataTransfer`信息，以便在游戏逻辑中使用这些数据。逻辑的关键是确定方块是否可以被放置，这通过检查游戏地图来完成，查看方块被放置的塔是空的还是上面已经有一个更大的方块。如果塔上有一个较小的方块，则不能添加该方块，你将返回`false`，这将阻止在塔上发生放置操作。如果可以添加方块，那么你会将方块“插入”到顶部方块之前（为了正确显示方块）或者塔上的占位符（即段落标签`<p id="px">`）之前。一旦方块被添加到HTML中，该步骤会更新游戏地图，增加移动次数计数器，并最后检查玩家是否已完成游戏。

为了检查玩家是否完成了游戏，你执行一个非常简单的检查，看最后一个塔是否拥有全部四个方块。由于游戏逻辑防止较小的方块位于塔上较大方块的下方，因此你不需要验证顺序。如果游戏已解决，那么玩家应该不能再移动方块，因此代码通过程序化地将每个方块的`draggable`属性设置为`false`来使方块不可拖动。这便结束了游戏；要再次游玩，玩家必须重新加载页面。

你可以通过以下功能极大地增强此步骤，例如根据方块是否可以放置在某个区域来更改放置区域的颜色。但现在你已经理解了拖放API的事件流，并且知道如何在事件触发时添加逻辑，如果你想添加这些功能，我们就留给你来完成。

在拖放API的两个示例中，你已经通过`DataTransfer`接口传递了简单的文本字符串。如前所述，`DataTransfer`接口可以处理多种类型的信息传输，包括图像、文件等。这些步骤仅涉及实现拖放解决方案功能的基础知识。拖放API还有许多其他特性，包括不同的行为、可拖动的对象，以及从桌面拖动到浏览器。在第14章“使用本地文件”中，你将学习如何使用`DataTransfer`接口的一些特殊功能来处理将文件从浏览器外部拖放到页面上的放置区域。

> 提示

如果你发现自己在调试拖放程序时遇到困难，因为每次你将对象拖放到放置区域时，浏览器都会启动一个新标签页或窗口，并只显示你正在拖动的对象，那么很可能你在触发的事件上遗漏了`preventDefault()`方法调用。没有此方法，浏览器将根据被拖动对象的类型执行其处理放置操作的默认流程。例如，在Firefox中，如果你正在拖动一个图像并将其放到一个没有执行`preventDefault()`方法的放置区域上，将打开一个新标签页，只显示你正在拖动的图像。

## 应用程序缓存与API

在智能手机和平板设备上，如果你想让一个应用程序始终可用，那么你需要一个原生应用程序。如果你想使用来自网站的应用程序，那么你需要一个互联网连接——也就是说，直到应用程序缓存的出现。应用程序缓存意味着你可以离线运行在线应用程序，不仅在智能手机或平板上，也可以在桌面浏览器上。

表13.2显示了支持应用程序缓存和API的每个浏览器版本。

**表13.2 应用程序缓存浏览器兼容性**

| 浏览器 | 版本 |
| :--- | :--- |



### 浏览器支持情况

| Android | 2.1+ |
| Chrome | 10.0+ |
| Firefox | 3.6+ |
| Internet Explorer | - |
| iOS Safari | 3.2+ |
| Opera | 10.6+ |
| Safari | 4.0+ |

应用程序缓存是一个文件列表，记录在一个清单中，它告诉浏览器下载这些文件并存储它们，以便当用户返回页面时，这些文件可供使用。如果你没有连接，这非常有用，但即使你有连接，这也会加快页面的加载速度，因为这些文件已经被加载过了。

任何引用该清单的页面都会自动被存储，但这并不意味着你想存储，或者确实应该（考虑到文件大小和类型限制）存储所有内容进行离线访问。你想提供给用户的是一个合适的离线体验。如果你有一个应用程序设计，那么使用该应用程序的关键文件应该被离线存储。

### 浏览器缓存安全

由于应用程序缓存在开发人员选择的用户文件系统上存储文件，因此与网站或应用程序相关的安全问题就存在了。一个恶意文件从网络服务器缓存到客户机上并非天方夜谭。考虑到这个安全问题，浏览器会在缓存任何文件之前询问用户是否信任该站点在本地系统上存储数据和文件。图13.3显示了浏览器如何向用户请求许可的示例。

### 引用清单文件

浏览器引用清单文件很简单；只需将`manifest`属性添加到`html`元素中，并指定你的清单文件名（`.appcache`），如下所示：

```
<!DOCTYPE html>
<html manifest="application.appcache">
<head>
</head>
<body>
</body>
</html>
```

> **注意**
>
> 清单文件中引用的任何文件（`.html`、`.php`等）都将被下载并缓存。

你的 Web 服务器可能不知道如何处理`.appcache`文件，因此你可能需要向服务器添加 MIME 类型。你可以通过 IIS 进行此操作，或者如果你使用的是 Apache，请在服务器上使用以下代码：

```
AddType text/cache-manifest .appcache
```

## 初级配方：创建清单文件

你不需要任何特殊软件来创建清单文件；你可以使用任何基本的文本编辑器，如记事本。将文件另存为`xxx.appcache`。在文件的顶部，你必须包含以下内容：

```
CACHE MANIFEST
```

> **注意**
>
> 我们建议在完成你的应用或网站之前不要创建清单文件，因为你不会希望存储未完成的文件，它们可能会干扰开发过程。清除或刷新缓存并不像刷新页面那样简单（我们将在本章后面介绍）。

从这里开始，你可以开始列出想要存储的文件，如下所示：

```
CACHE MANIFEST
css/main.css
js/jquery.js
images/logo.png
```

这应该就是你所需要的全部。如果你创建了一个 HTML 页面并包含了一个列出文件的清单文件，如上所示，那么在线访问该页面后，页面及其支持文件将被缓存。然后，如果你断开互联网连接并刷新页面，页面将正常显示。清单中列出的文件可以是相对地址或绝对地址。

但你还可以做更多。你可以将清单文件分为三个部分：`CACHE`、`FALLBACK`和`NETWORK`：

- `CACHE`：应在客户端浏览器设备上缓存的文件，以便在互联网连接不可用时使用。
- `FALLBACK`：当无法连接到互联网时使用的文件及其替代文件列表。
- `NETWORK`：仅在连接时需要且不应缓存的文件。

### CACHE

`CACHE`部分与前面示例中的基本相同。像前面示例中的那样列出的文件或带有`CACHE`标题的文件是“显式”的，将被下载并缓存在浏览器中。它们可以包含存储在外部的文件，但在缓存文件时不能使用通配符，因此`css/*`将不起作用。

> **警告**
>
> 不要在缓存中缓存清单本身，因为这将几乎不可能通知浏览器新的清单。

### FALLBACK

清单的`FALLBACK`部分非常有用，可以作为检测用户是否在线或离线的一种方式。使用`FALLBACK`，你可以告诉浏览器，如果由于用户离线导致特定文件不可用，该使用哪个文件。例如，如果你有一个离线使用不必要的大型 CSS 文件，那么你可以将其从`CACHE`部分省略，转而使用`FALLBACK`，如下所示：

```
CACHE MANIFEST
FALLBACK:
online.css offline.css
```

因此，在此示例中，如果用户离线但 HTML 页面调用了`online.css`，清单文件会告诉浏览器切换到`offline.css`（注意文件之间用空格分隔），该文件已被缓存。很方便，不是吗？这不仅限于 CSS 文件，还可以用于图像、JavaScript 文件、HTML 页面，甚至视频片段。只需将每个声明放在新的一行。

使用`FALLBACK`，你可以使用通配符技术。因此，如果你想为所有文件设置一个回退，你可以使用以下内容：

```
/ /offline.html
```

因此，如果用户离线，斜杠后的所有文件（如`/page1.html`）将显示`offline.html`。但请记住，一旦打开了一个文件（如`page1.html`）并且它引用了清单文件，那么它将被下载并可供离线使用。

你可以进一步使用`FALLBACK`，为特定目录或仅 HTML 页面提供通用回退：

```
/js/ /offline.js
*.html /offline.html
```

### NETWORK

`NETWORK`部分告诉浏览器哪些文件仅在连接时可用，并阻止这些文件被下载。通常，放在此部分的资源是需要数据库或服务器连接的资源，例如登录页面：

```
CACHE MANIFEST
NETWORK:
login.aspx
```

### 通过清单更新缓存

当浏览器首次看到清单文件时，它会下载列表中的文件，并且不会刷新缓存，除非你强制它。你可以通过 API（稍后介绍）来执行此操作；通过清除浏览器缓存（Firefox 有按站点删除清单的选项；选择 Firefox > 选项 > 高级）；或者通过更新清单文件。更新清单中列出的文件不会强制更新；你必须对清单本身进行更改。一个简单的方法是，与其添加或删除资源，不如保留或更新注释。你可以通过以井号（`#`）开头的行在文件中添加注释，如以下示例所示。注释必须单独占一行。

```
CACHE MANIFEST
# v1.0 - 06.28.2011

CACHE:
magic.js
style.css
```

刷新缓存可以像更新注释一样简单。

## 初级配方：离线使用网页

你已经了解了逻辑，现在你将看到一个示例。在这个 Web 应用程序中，你将创建一个简单的乘法计算，使用两个提供的数字，并允许用户在在线时使用“联系我们”类型的表单。如果用户离线，那么你将回退到一个包含联系信息的静态页面。在此配方中，你将拥有以下内容：

- 三个 HTML 页面
- 一个 JavaScript 文件
- 两个 CSS 文件
- 两个图像

第一个 HTML 页面上有两个输入字段（当然是新的 HTML5 输入类型），按钮将两个数字相乘（本示例中没有验证）。当单击提交按钮时，将显示结果，并提供一个选项，通过联系表单将你的结果发送给一个虚构的公司。但是，联系表单仅在连接时显示，因此你将提供一个`FALLBACK`选项，该选项是一个仅包含电话号码的页面。

此外，在应用程序中你有一个包含一些布局样式的 CSS 文件，以及一个单独的 CSS 文件，用于加载漂亮的字体（例如，它可能来自网络字体服务）。你希望这个漂亮的字体仅在用户在线时显示。

最后，一个图像将简单地告诉你用户是否在线（一个勾号图形）或不在线（一个 X 图形）。

清单 13.3 显示了此应用程序的 HTML，清单 13.4 显示了清单文件。你可以在图 13.4 中查看其实际效果。

**清单 13.3 用于显示计算表单的 HTML**

```
<!DOCTYPE html>
<html manifest="13_3_cookbook.appcache">
<head>
<meta charset="utf-8">
<title>Offline</title>
<script src="13_3_calculation.js"></script>
<link rel="stylesheet" href="13_3_offline_style.css" />
<link rel="stylesheet" href="13_3_offline_style2.css" />
</head>
<body>
    <h1>提交一个计算</h1>
    <label for="first">第一个</label>
    <input required type="number" id="first" name="first" />
    <label for="second">第二个</label>
    <input required type="number" id="second" name="second" />
    <input type="submit" onclick="calculate()" value="计算" />
    <div id="resultHolder">
        <h2>你的结果是 <span id="result"></span></h2>
        <p>现在你得到了结果，可以 <a href="13_1_offline_contact.html">联系我们</a></p>
    </div>
    <img src="connection-tick.gif" width="50" height="50" alt="">
</body>
</html>
```

### 提交一个计算

![](img/de30ea99ecac39b49e690a84c48f43b9_369_0.png)

![](img/de30ea99ecac39b49e690a84c48f43b9_369_1.png)

![](img/de30ea99ecac39b49e690a84c48f43b9_369_2.png)

![](img/de30ea99ecac39b49e690a84c48f43b9_369_3.png)

图 13.4 在线时提交计算的输出

**清单 13.4 计算应用的清单**

```
CACHE MANIFEST
# 版本 1.0

CACHE:
13_3_calculation.js
13_3_offline_style.css

NETWORK:
13_3_offline_style2.css

FALLBACK:
connection-tick.gif connection-cross.gif
13_3_offline_contact.html 13_3_offline_offline.html
```

如果你在联机时尝试此示例，你将看到漂亮的 Comic Sans 字体和勾号图形（见图 13.4），但如果你随后离线并刷新，应用程序将没有分配的字体，并且显示 X 图形（见图 13.5）。如果你完成计算并尝试访问联系表单，你将看到图 13.6 所示的“给我们打电话”页面。

### 提交一个计算

![](img/de30ea99ecac39b49e690a84c48f43b9_369_4.png)

![](img/de30ea99ecac39b49e690a84c48f43b9_369_5.png)

![](img/de30ea99ecac39b49e690a84c48f43b9_369_6.png)

![](img/de30ea99ecac39b49e690a84c48f43b9_369_7.png)

图 13.5 离线时提交计算的输出

### 联系我们

我们的联系表单需要您连接互联网。或者，您也可以拨打 123-456-789 联系我们。

图 13.6 离线时显示的替代联系表单页面

应用缓存为您提供了多种选择。您的应用可能完全在单个页面上，也可能分布在多个页面中，因此您需要考虑存储哪些文件以及哪些文件需要互联网访问。

浏览器之间存在一些差异。IE9 不完全支持离线 Web 应用；然而，它似乎可以很好地缓存初始页面、CSS 和 JavaScript 并在离线状态下工作，但不应依赖此缓存。Chrome、Firefox 和 Safari 按预期工作并显示回退图像和 HTML 页面。Opera 11 显示回退图像，但在连接到表单时，它没有显示回退页面，而是显示一个连接错误页面。

## 应用缓存 API

当浏览器重新加载具有清单的页面时，它首先检查是否有任何更改，然后如果文件有更改，它会在后台进行更新。如果您在 Chrome 中打开一个带有清单的页面，打开开发者控制台，然后刷新页面，您将看到它返回以下内容：

```
Document was loaded from Application Cache with manifest http://website/13_3_cookbook.appcache
Application Cache Checking event
Application Cache NoUpdate event
```

如果您更改清单并再次刷新，您将看到更多的活动：

```
Document was loaded from Application Cache with manifest http://website/13_3_cookbook.appcache
Application Cache Checking event
Application Cache Downloading event
Application Cache Progress event (0 of 5) http://website/13_3_offline_style.css
Application Cache Progress event (1 of 5) http://website/13_3_calculation.js
Application Cache Progress event (2 of 5) http://website/13_3_offline.html
Application Cache Progress event (3 of 5) http://website/13_3_offline_offline.html
Application Cache Progress event (4 of 5) http://website/connection-cross.gif
Application Cache Progress event (5 of 5)
Application Cache UpdateReady event
```

`ApplicationCache`对象中有几个事件，如下所列。浏览器默认提供加载事件，但应用缓存 API 为您提供了更多选择（如果您想使用它们）。

- `checking`：浏览器首次下载清单文件或正在查找文件的更新。
- `noupdate`：清单文件未更改。
- `downloading`：如果浏览器是首次查看清单文件，它将下载资源；否则，它已找到更新并正在下载该更新。
- `progress`：浏览器正在下载列出的资源。
- `cached`：资源现已下载并缓存。
- `updateready`：清单中的资源已下载完毕，浏览器缓存可以更新。然后可以触发`swapCache`函数使浏览器使用最新的清单。请注意，必须调用`swapCache`函数；否则，浏览器仍将使用旧缓存。
- `obsolete`：找不到清单文件。
- `error`：找不到清单文件、引用清单的页面未正确下载，或检查清单时发生致命错误。

这些事件为您提供了选择，例如使用`addEventListener`告知用户更新已准备就绪，然后调用`swapCache`函数：

```
applicationCache.addEventListener('updateready', function() {
    //do something
    alert("There is an update to the cache")
    applicationCache.swapCache();
})
```

## 通知 API

通知 API，也称为 Web 通知 API，是一套较新的 API，允许浏览器页面通过桌面通知来提醒用户。该 API 尚处于早期阶段，目前仅通过 WebKit 规范以及基于 WebKit 的浏览器得到支持。通过 WebKit 通知接口进行的调用与 W3C 草案规范中定义的调用相似，因此当 Web 通知 API 未来被浏览器支持时，更新应该很小。

很多时候，用户会在使用系统上的其他应用程序时将浏览器窗口置于后台。当浏览器页面提醒用户其会话即将过期、某只股票达到卖出价位或某些其他对用户可能很重要的事件时，该警报可能位于桌面其他窗口的后面。使用通知 API，浏览器页面现在可以请求用户的桌面代为显示通知。通知将像其他已安装应用程序的通知一样显示，通常在用户屏幕的某个角落。

WebKit 通知 API 提供了两个接口，分别名为`NotificationCenter`和`Notification`。`NotificationCenter`接口提供了请求用户通知权限、维护权限状态和创建通知的能力。以下是`NotificationCenter`接口上可用的方法：

- `Notification createNotification(in DOMString iconUrl, in DOMString title, in DOMString body)`：基于提供的图标、标题和正文创建一个通知实例。
- `Notification createHTMLNotification(in DOMString url)`：创建一个基于 HTML 页面的通知。
- `Int checkPermission()`：获取当前来源的通知权限级别。
- `void requestPermission([in Function callback])`：请求用户显示通知的权限。



`NotificationCenter`接口在 WebKit 浏览器中通过`window`对象的名为`webkitNotifications`的属性暴露。例如，要使用 JavaScript 创建通知，您可以使用以下代码行：

```
window.webkitNotifications.createNotification('icon.png', 'My Title', 'My Notification');
```

如您所见，该接口有两种不同的创建通知的方法：`createNotification`和`createHTMLNotification`。`createNotification`方法接受传递的参数以显示带有图标、标题和正文的标准桌面通知。除这些值外，使用`createNotification`时无法对通知执行其他自定义操作。使用`createHTMLNotification`时，源页面的 URL 被传递给该方法。然后此 URL 页面可以具有格式等以提供附加功能，例如超链接。无论哪种情况，都会返回一个`Notification`实例。

一旦创建了`Notification`实例，您就可以使用`Notification`接口方法来控制通知的显示。在 WebKit 通知接口中，有两个方法`show`和`cancel`，说明如下：

- `show()`：如果权限已允许，则将通知添加到桌面队列中进行显示。
- `cancel()`：从桌面或队列中移除通知。

`Notification`接口还具有事件处理函数，用于在通知显示、关闭或发生错误时提供通知的详细信息，如下所列：

- `ondisplay`：通知已在桌面上显示。
- `onclose`：通知已通过手动操作或通过`cancel`方法关闭。
- `onerror`：通知发生错误。

您将在本章的最后一个示例中研究如何处理`Notification`接口事件。

## 通知权限

由于通知 API 能够随时在用户的屏幕上显示任何性质的弹出窗口，因此对安全性和不需要的广告内容的担忧是自然的。因此，通知 API 包含一个权限系统，用户必须首先被询问是否希望允许或拒绝特定来源的通知。当向用户请求权限时，特定浏览器将使用下拉栏或类似方法向用户请求权限，如图 13.7 所示。

请注意，只能通过用户的有意操作（例如单击按钮或链接）来显示权限请求。在页面加载时请求权限将不起作用，并且出于安全目的，权限请求不会显示给用户。

同样重要的是要认识到，通知的权限是按来源设置的，而不是按页面设置的。因此，如果用户拒绝了您的某个页面的通知，那么整个域的通知都将被拒绝。如果用户未提供权限而您创建了通知，通知不会失败，但也不会显示。在本章的最后一个示例中，您将了解如何检查用户对域的当前“权限级别”。

## 浏览器兼容性

表 13.3 显示了每个支持通知 API 的浏览器的版本。但请注意，通知 API 是使用 WebKit 实现的，因为通用规范仍在草案阶段。预计最终发布的规范将拥有一个不依赖 WebKit 的通知方法。

**表 13.3 通知 API 浏览器可用性**

| 浏览器 | 版本 |
|---|---|
| Android | - |
| Chrome | 10.0+ |
| Firefox | - |
| Internet Explorer | - |
| iOS Safari | - |
| Opera | - |
| Safari | - |

![](img/de30ea99ecac39b49e690a84c48f43b9_373_0.png)

## 初级教程：显示简单通知

本篇第一个通知教程将使用 WebKit 通知功能，先向用户请求权限，然后在用户点击“发送通知”按钮时创建并显示通知。用户可以按需发送任意数量的通知，每次都会显示一个带有递增唯一编号的新通知。如果桌面已达到可显示通知的数量上限，通知将会排队等待显示。

这是一个简单的教程，但将展示在桌面上显示桌面通知的基础知识。让我们通过查看代码清单 13.5 来发送第一个通知：

1. 创建一个空白 HTML 页面，包含如代码清单 13.5 所示的 HTML body 标签，其中包括“设置权限”和“发送通知”两个按钮。
2. 添加`window.addEventListener`行以监听页面加载事件，并添加`init`函数，该函数为按钮附加点击事件处理程序。
3. 添加全局变量`notificationCount`，为每个通知维护一个唯一 ID。
4. 添加`setPermission`函数，以便在支持`webkitNotifications`接口时请求权限。
5. 添加`fireNotification`函数，该函数创建并显示通知。

### 代码清单 13.5 使用 createNotification 显示事件

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>13.5 Basic Notification</title>
<script>
// counter for notifications
var notificationCount = 0;

// initialize the page
function init() {

    // reference the buttons
    var btnSetPermission = document.getElementById('setPermission');
    var btnFireNotification = document.getElementById('fireNotification');

    // set our button click event handlers
    btnSetPermission.addEventListener('click',setPermission,false);
    btnFireNotification.addEventListener('click',fireNotification,false);
}

// Request the user permission for notifications
function setPermission() {
  // check if the webkitNotifications is supported
  if (webkitNotifications) {
    // request permission from the user
    window.webkitNotifications.requestPermission();
  } else {
    // Let the user know that notifications are not supported
    alert("Notifications are not supported on this browser.");
  }
}

// Function to fire the notification
function fireNotification() {
  // increment our notification counter
  notificationCount++;

  // create the notification passing in icon, title, body
  var notification = webkitNotifications.createNotification(
    'icon_notification.png',
    'Number '+notificationCount,
    'This is notification '+notificationCount);

  // now show the actual notification
  notification.show();
}

// Add our page load listener to initialize
window.addEventListener('load',init,false);
</script>
</head>
<body>
  <h1>Basic Notification Recipe</h1>
  <p>Click set permission to allow notifications, then fire a notification.</p>
  <section>
    <button id="setPermission">Set Permission</button>
    <button id="fireNotification">Fire Notification</button>
  </section>
</body>
</html>
```

当代码清单 13.5 在浏览器中加载时，`init`函数将运行，并为两个按钮“设置权限”和“发送通知”添加点击事件处理程序。你需要首先点击“设置权限”按钮，以便浏览器显示授权提示。（请记住在 Chrome 或其他基于 WebKit 的浏览器中运行此代码。）当权限请求出现时，选择“允许”选项，这将告知浏览器，允许来自该页面源点的任何页面请求桌面显示桌面通知。在`setPermission`函数内部，你首先检查`webkitNotifications`是否可用。如果接口可用，脚本将执行`webkitNotifications`接口的`requestPermission`方法。这将启动向用户请求权限的流程。如果你之前已设置权限允许通知，那么再次调用`requestPermission`将不会有任何效果。你可以重置页面源点的权限以便进行测试，如下面的提示所示。

> ### 提示
>
> 在使用这些教程或你自己的页面测试通知时，你会注意到一旦你允许或拒绝了通知，将无法再使用`requestPermission`方法再次询问用户是否允许或拒绝通知。要重置通知的首选项，你必须进入浏览器的设置并手动重置权限。在 Chrome 中，你可以在“偏好设置” > “高级” > “隐私” - “内容设置...” > “通知” > “管理例外情况...”下找到此选项，如图 13.8 所示。
>
> 要重置你域名的通知权限，请将鼠标悬停在你的条目上，然后点击 X 从主机名模式列表中移除你的条目，如图 13.9 所示。这将重置权限，并允许 JavaScript 代码通过`requestPermission`方法进行询问。

一旦权限设置为允许桌面通知，你就可以点击“发送通知”按钮。这将执行`fireNotification`方法，该方法增加通知计数器，然后通过`createNotification`方法创建一个通知。传递给该方法的参数包括我们创建的图标 URL、包含计数器的标题，以及包含唯一计数器的通知正文文本。创建通知后，你仍然必须调用`show`方法，告诉浏览器要求桌面显示通知。如果权限未被允许或已被拒绝，则通知将不会显示。

每次点击“发送通知”按钮，都会创建并显示一个新的通知。在图 13.10 中，你可以看到多次点击“发送通知”按钮的示例。

> **注意**
>
> 每个桌面环境都会对一次可以向用户显示的通知数量有限制。如果你创建了一个通知，而桌面当前正在显示最大数量的通知，那么该通知将被排队，直到用户移除一个通知或通知被自动移除，桌面才有空间显示。

本教程展示了通过 WebKit 通知创建和显示桌面通知的简单示例。在下一个教程中，你将使用这些方法以及其他事件来创建来自 Twitter 用户的新推文通知。

## 高级教程：创建推文通知页面

在上一个教程中，你已经能够创建桌面通知，你可能对如何使用通知 API 有了一些想法。当用户不在浏览器窗口中时，能够通知他们发生事件是非常有用的。

在这个教程中，你将使用通知 API 在桌面上显示来自特定 Twitter.com 用户的新推文通知。该教程将使用 Twitter API `statuses/user_timeline`来检索用户的新推文，然后将推文作为通知显示在桌面上。该页面将每隔 60 秒向 Twitter.com 发送一次请求来检查用户的新推文。首次发出请求时，页面将默认抓取三条最新的推文进行显示。有关 Twitter API 的更多信息，请参阅 REST API 的文档 http://dev.twitter.com/doc，以及本教程将使用特定 API 方法的文档 http://dev.twitter.com/doc/get/statuses/user_timeline。

> **注意**
>
> Twitter API 能够通过 Twitter REST API 执行回调函数。本教程利用这种回调技术，能够直接对 Twitter API 进行 JavaScript 调用。你必须使用此回调方法以及 JSONP 格式，以解决这些基于客户端的请求中常见的跨域请求安全问题。此外，你也可以使用第三方库（如 jQuery）来执行调用，甚至可以在你自己的域中构建代理服务器。请注意，与大多数在线 API 一样，Twitter API 对其 API 实施速率限制以防止滥用，如果你使用过于频繁，可能会收到“超过速率限制”的错误。

除了你在前一个教程中看到的`createNotification`和`show`方法外，你还将使用`cancel`方法在特定时间段后自动移除通知。该教程将使用`ondisplay`事件处理程序来触发一个计时器，在 15 秒后自动移除显示的通知。然后，脚本将等待一分钟，并向 Twitter 询问是否有新推文。

在前一个示例中，您可能已经注意到，很难知道是否已提供权限或当前的通知权限级别。在本示例中，您将使用`webkitNotifications`接口上的`checkPermission`方法，允许用户随时查看权限。通常，这不是您会在页面中向用户展示的内容，但可以在您的脚本中很有用。`checkPermission`方法返回一个整数值，描述桌面通知的当前权限状态，如表 13.4 所示。

通常，要使用回调函数调用外部 Web 服务，您需要将内联脚本源作为 REST 调用的 URL。本示例展示了一种令人兴奋的替代方法，使用 Web Worker 来检索结果、解析它们，然后将它们发送回主线程。这是通过在 Web Worker 中使用`importScripts`命令来实现的，如第 12 章“通信与线程”中所述。这允许主线程在调用 Twitter 时继续运行而不被阻塞，并允许处理结果。您只需在每次想要检索结果时创建一个新的 Web Worker，并且 Web Worker 在处理完结果后结束。关于这一点的一个注意事项是，通知不能从 Web Worker 启动，因为通知是`window`对象的一部分，而该对象在 Web Worker 中不可用。因此，您只需将信息发送到主线程以显示通知。使用这种 Web Worker 模型，将有两个文件。清单 13.6 是主页面，清单 13.7 是 Web Worker。让我们从主页面开始，如清单 13.6 所示：

1. 创建一个空白的 HTML 页面，包含 HTML body 标签和按钮：设置权限、检查权限级别和获取推文。
2. 添加 script 标签和全局变量`tworker`和`lastTweetId`。
3. 添加 script 标签和`setPermission`函数，用于请求桌面通知的权限。
4. 添加`checkPermissionLevel`函数，用于检索和显示当前的权限级别。
5. 添加`grabTweets`函数，该函数启动 Web Worker，为来自 Web Worker 的消息分配监听器，并处理通知的创建。

### 表 13.4 桌面通知的权限级别

| 权限 | 值 | 说明 |
| :--- | :---: | :--- |
| `PERMISSION_ALLOWED` | 0 | 用户已授予桌面通知的权限。 |
| `PERMISSION_NOT_ALLOWED` | 1 | 用户已允许或拒绝权限。通常，尚未执行权限请求。 |
| `PERMISSION_DENIED` | 2 | 用户已拒绝此来源的桌面通知权限。 |

### 清单 13.6 在主线程中创建通知



```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>13.6 Twitter 通知</title>
<script>

// 设置我们的 web worker 引用
var tworker = null;
// 设置最后阅读的推文 ID
var lastTweetId = 0;

// 初始化处理程序的函数
function init() {
    // 设置处理程序
    var btnSetPermission = document.getElementById('btnSetPermission');
    var btnCheckPermission = document.getElementById('btnCheckPermissionLevel');
    var btnGrabTweets = document.getElementById('btnGrabTweets');

    btnSetPermission.addEventListener('click',setPermission,false);
    btnCheckPermission.addEventListener('click',checkPermissionLevel,false);
    btnGrabTweets.addEventListener('click',grabTweets,false);
}

// 请求用户通知权限的函数
function setPermission() {

    // 检查浏览器是否支持通知
    if (webkitNotifications) {

        // 检查通知尚未被允许
        if (webkitNotifications.checkPermission() == 1) {

            // 请求权限并回调此函数
            webkitNotifications.requestPermission(setPermission);
        } else {
            // 验证权限已被授予
            alert('Permission has been given.');
        }
    } else {
        // 不支持通知
        alert('Notifications are not supported on this browser. ');
    }
}

// 检查通知权限
function checkPermissionLevel() {

  // 验证是否支持通知
  if (webkitNotifications) {

    // 获取当前的权限级别
    var permissionLevel = webkitNotifications.checkPermission();

    // 将权限级别映射到等效值
    switch (permissionLevel) {
      case 0:
        // PERMISSION_ALLOWED
        alert('Current level: PERMISSION_ALLOWED (0)');
        break;
      case 1:
        // PERMISSION_NOT_ALLOWED
        alert('Current level: PERMISSION_NOT_ALLOWED (1)');
        break;
      case 2:
        // PERMISSION_DENIED
        alert('Current level: PERMISSION_DENIED (2)');
        break;
    }
  }
}

// 获取推文并创建通知的函数
function grabTweets() {

  // 在日志中验证我们正在创建 web worker
  console.log('creating worker');

  // 创建用于获取用户推文的 web worker 实例
  tworker = new Worker('13_7_tweetworker.js');

  // 用于接收来自 web worker 消息的 message 事件处理程序
  tworker.addEventListener('message', function(msg) {

    // 确定来自 worker 的消息类型
    switch (msg.data.msgType) {

      // 收到一条推文消息，需要显示通知
      case 'TWEET':

        console.log('creating notification');

        // 从 worker 消息中获取图标、标题和内容
        nIcon = msg.data.icon;
        nTitle = msg.data.title;
        nBody = msg.data.body;

        // 创建通知
        var notification = webkitNotifications.createNotification(nIcon, nTitle,
            nBody);

        // 设置 ondisplay 事件处理程序
        notification.ondisplay = function(event) {

            // 播放通知音频
            var audio = new Audio('13_6_notify.mp3');
            audio.play();

            // 设置一个超时，在 15 秒后移除通知
            setTimeout(function() {event.currentTarget.cancel()}, 15000);
        }

        // 设置 onclose 事件处理程序
        notification.onclose = function() {
            // 记录通知已关闭
            console.log('Notification closed.');
        }

        // 设置 onerror 事件处理程序
        notification.onerror = function() {
            // 记录通知出错
            console.log('Notification Error.');
        }

        // 显示通知
        notification.show();

        break;

      // Web worker 已完成
      case 'END':

        // 如果有最后一条推文 ID，则存储起来用于下次搜索
        if (msg.data.lastTweetId>0) {
            lastTweetId = msg.data.lastTweetId;
        }

        // 设置一个超时，在 1 分钟后再次搜索
        setTimeout('grabTweets()',60000);
        break;
    }
  }, false);

  // 使用最后一条推文 ID 启动 worker 搜索
  tworker.postMessage(lastTweetId);
}

// 窗口加载事件处理程序
window.addEventListener('load',init,false);

</script>
</head>
<body>
<h1>根据新推文创建通知</h1>
首先点击“设置权限”以授权通知。<br>
然后点击“获取推文”开始监听新推文。
<br><br>
<button id="btnSetPermission">设置权限</button>
<button id="btnCheckPermissionLevel">检查权限级别</button>
<button id="btnGrabTweets">获取推文</button>
</body>
</html>
```

现在主页面已完成，您需要创建Web Worker JavaScript文件，该文件将检索推文并解析返回的任何推文，如清单13.7所示：

1. 为Web Worker创建一个`.js`文件，其中包含用于接收来自主页面消息的`onmessage`处理程序。`onmessage`处理程序还将执行从Twitter.com导入REST API脚本的操作。

2. 添加`getResult`函数，它是`importScripts` REST API调用的回调函数。此函数将处理检索到的任何推文的解析，并将它们发送回主线程进行显示。这就是Web Worker的全部内容。

### 清单13.7 利用 Web Worker 关注推文

```javascript
// 13_7_tweetworker.js
// 用于检索推文集的 Web worker 线程

// 解析推文结果的回调函数
function getResult(data) {

// 用于保存推文列表最大 ID 的变量
var maxId = 0;
```

## 354 第13章 HTML5中的浏览器体验



```
// 检查是否有待解析的推文
if (data.length > 0) {

    // 用于通知的变量
    var tIcon = '';
    var tTitle = '';
    var tBody = '';

    // 倒序遍历结果集
    for (var i = (data.length - 1); i >= 0; i--) {

        // 获取用户头像、用户名和推文内容
        tIcon = data[i].user.profile_image_url;
        tTitle = data[i].user.screen_name;
        tBody = data[i].text;

        // 将推文信息返回给主线程进行显示
        postMessage({msgType: 'TWEET', icon: tIcon, title: tTitle, body: tBody});

        // 将id_str存储为最大ID，以避免重复显示
        maxId = data[i].id_str;
    }
}

// 通知主线程当前循环已完成
postMessage({msgType: 'END', lastTweetId: maxId});
}

// 接收主线程的消息
onmessage = function(event) {

    // 获取上一条推文的起始ID
    var lastId = event.data;
    var qString = '';

    // 检查上一个ID是否为有效的推文ID
    if (lastId != 0) {
        // 如果是有效的推文ID，则使用since_id参数
        qString = '&since_id=' + lastId;
    } else {
        // 如果之前没有读取过推文，则最多获取三条
        qString = '&count=3';
    }

    // 使用importScripts作为JSONP方法，而非内联script标签
    // 当前关注的是BreakingNews的屏幕名称，但你可以更改
    // 为你想要关注的任意Twitter用户
importScripts('http://api.twitter.com/1/statuses/user_timeline.json?screen_name=BreakingNews' + qString + '&callback=getResult');
}
```

## 高级技巧：创建推文通知页面

在浏览器中加载主页面后，点击“设置权限”按钮之前，先点击“检查权限级别”按钮。这将调用`checkPermissionLevel`函数。该函数会验证`webkitNotifications`是否可用，然后执行`checkPermission`方法，以整数值的形式获取当前的权限级别。接着，该值会被转换为对应的含义，并以警报形式显示。这将帮助你快速验证该域是否已正确设置显示桌面通知的权限。你可以通过浏览器设置移除权限、拒绝权限以及最终允许权限来观察权限级别的变化，以此进行测试。如果你尚未将权限设置为允许通知，则需要在继续后续操作前完成设置。

加载代码时，会设置一个指向名为`tworker`的Web Worker的全局引用，并设置一个名为`lastTweetId`的全局变量，用于存储你为该用户读取的最后一条推文的“书签”。加载时，该变量被设置为零，以便你知道这是首次加载页面且尚未读取任何推文。当你启动Web Worker以获取推文列表时，`lastTweetId`将被传递给Web Worker，用于确定要显示的推文。你需要将这个变量保存在主页面中，因为一旦Web Worker完成推文的检索和解析，该Worker就会销毁。每次你请求推文时，都会创建一个新的Web Worker。

要开始为用户检索推文并显示通知，请点击“获取推文”按钮。这将执行`grabTweets`方法，该方法首先会在控制台日志中添加一条日志消息，以验证你已开始检索过程。接下来，该函数将从tweet-worker.js文件创建一个新的Web Worker。在进入这个Worker之前，让我们先看看`grabTweets`函数的其余部分做了什么，因为根据设计，Web Worker在收到开始处理的消息之前不会执行任何操作。`grabTweets`函数的下一步是将`onmessage`事件处理程序分配给Web Worker，以便在Web Worker发回消息时能够接收它们。你将使用与第12章“通信与线程”中类似的基于Web Worker的消息通信方式，即Web Worker可以根据带有消息类型和相关参数的JSON格式有效载荷，发回不同类型的消息。

Web Worker发送给主页面的消息将有两种不同类型：TWEET消息和END消息。如果你收到`msgType`为TWEET的消息，意味着Web Worker已找到一条待显示的推文，然后你将使用有效载荷的其余部分来显示一条通知，其中包含用户头像作为图标、用户名作为标题，以及推文内容作为正文。本示例中的代码会创建通知；添加`ondisplay`、`onclose`和`onerror`事件处理程序；最后显示通知。`onclose`和`onerror`事件处理程序将仅在捕获事件时记录控制台日志消息。你将使用`ondisplay`处理程序在通知显示时播放声音，并设置一个超时时间，以便在用户尚未关闭通知时自动从桌面移除该通知。然后，使用`show`方法显示通知。

END消息将通知主页面，Web Worker已完成任何推文的检索和处理。通过让Web Worker告知你线程已完成，你可以确保没有多个Worker（线程）同时运行，并确保在Worker结束和启动新Worker之间等待一段时间。
请求被拒绝，因为它被视为高风险

## 本章总结

在本章中，你学习了一些较小的API扩展。拖放、离线存储和通知API提供了极大改善网站与应用程序用户体验的手段。这些API提供了更高级别的集成能力，正迅速消除浏览器体验与原生应用之间的差异。未来这些API扩展将如何被运用，将十分令人期待。

## 处理本地文件

在HTML5之前，客户端浏览器对文件处理的支持与关注度都较为有限。通常其功能广度仅限于为向Web服务器上传而进行的简单文件选择。借助HTML5以及一套补充API——File API，我们现在拥有更丰富的功能集，更重要的是，获得了一套标准化的功能集，可通过JavaScript获取文件基本属性，并将不同类型的文件读取到客户端浏览器中。在本章中，你将通过一系列实例，学习File API的新功能集，这些实例涵盖基础内容以及一些即将推出的新File API规范。

### File API概览

File API提供了一套标准化方式，用于在客户端浏览器中与用户选择的文件进行交互。File API的接口可分为三个功能领域：

- 在`FileList`接口中选择一个或多个文件
- 通过`File`接口获取文件的属性
- 通过`FileReader`接口读取实际文件内容

`FileList`接口是用户选择的文件列表，可以像数组一样进行遍历。`File`接口提供了所选文件的属性。借助这两个接口，脚本可以遍历所选文件并获取文件的关键属性，如下所示：

- `name`：文件名
- `type`：MIME格式、ASCII编码的文件类型
- `size`：文件大小（以字节为单位）
- `lastModifiedDate`：文件最后修改日期和时间

### File API安全性

File API与客户端设备上浏览器容器之外的信息和数据进行交互。这种与本地文件系统的交互自然引发了安全方面的担忧。HTML5 File API规范通过仅允许JavaScript与用户授权访问的文件进行交互，来处理文件读取访问的安全问题。File API无法自行浏览目录结构或选择文件，必须通过文件选择机制由用户交互触发。

表14.1展示了支持File API的浏览器版本。各浏览器的支持程度有所不同，在本章实例中将会标注适用情况。

**表14.1 File API浏览器支持情况**

| Android | 3.0+ |
| --- | --- |
| Chrome | 9.0+ |
| Firefox | 3.6+ |
| Internet Explorer | 10.0+ |
| iOS Safari | - |
| Opera | 11.1+ |
| Safari | - |

## 入门实例：获取文件属性

本实例将使用`File`接口，获取页面访问者通过标准文件输入元素选择的文件的名称、类型、大小和最后修改日期。在展示如何获取这些信息之前，本实例将先演示如何验证浏览器是否支持`FileList`接口。要显示文件的属性，如清单14.1所示，请执行以下步骤：

1. 创建一个空白HTML页面，包含文件输入元素，并添加`onchange`事件处理程序，以便在选择文件时被调用。
2. 在HTML正文部分添加`fileAttributes`区域，用于显示文件属性。
3. 添加`handleFile`函数，以`fileInput`作为参数。

### 清单14.1 显示文件属性

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8" />
  <title>14.1 获取文件属性</title>
  <script>
    // 处理选定的文件
    function handleFile(fileInput) {
      // 引用用于显示属性的部分
      var fileAttributes = document.getElementById('fileAttributes');
      // 验证浏览器是否支持files接口
      if (fileInput.files) {
        // 使用files接口引用文件
        var file = fileInput.files[0];
        // 创建输出内容
        var output = 'File attributes:<br>';
        output += 'name: ' + file.name + '<br>';
        output += 'type: ' + file.type + '<br>';
        output += 'size: ' + (file.size/1024).toFixed(2) + 'KB<br>';
        output += 'last modified date: ' + file.lastModifiedDate;
        // 将输出内容设置到该部分
        fileAttributes.innerHTML = output;
      } else {
        // 浏览器不支持files接口
        fileAttributes.innerHTML = 'files interface not supported';
      }
    }
  </script>
</head>
<body>
  <h1>Select File Below:</h1>
  <section>
    <input type="file" id="input" onchange="handleFile(this)" />
  </section>
  <br>
  <section id="fileAttributes"></section>
</body>
</html>
```

当清单14.1创建的页面的访问者从文件输入元素的浏览按钮中选择一个文件时，`onchange`事件处理程序将调用`handleFile`函数，并将文件元素作为参数传递。在`handleFile`函数内部，你首先获取显示部分元素的引用，然后检查以验证浏览器是否支持`FileList`接口。如果浏览器不支持`FileList`接口（通过检查`Files`数组是否存在来判断），将在`fileAttributes`部分显示一条消息，但你可以选择继续处理逻辑或请求访问者提供更多信息。

如果支持`FileList`接口，你将从文件数组中获取一个特定实例（`File`对象），即引用`Files`数组中的第一个文件`fileInput.files[0]`。然后你使用该`File`接口实例来获取`name`、`type`、`size`和`lastModifiedDate`属性。对`size`属性执行了转换，因为其度量单位是字节，而文件大小通常以千字节为单位引用更常见。该等式将字节转换为千字节。你可以通过编写一个函数来增强此功能，该函数接收字节数，并根据总字节数以千字节、兆字节或其他单位显示转换结果，就像在常规目录列表中所做的那样。

> 注意
> `File`接口继承自`Blob`，因此它包含`size`和`type`属性。通过`File`接口，添加了`name`和`lastModifiedDate`属性。然而，在多个浏览器平台中，`lastModifiedDate`不可用，当被请求时会返回未定义的值。

在本实例中，你获取了访问者选择的文件并显示了文件属性。这在文件上传到服务器之前进行过滤，或仅向用户显示确认信息时非常方便。下一个实例将扩展此功能，为访问者提供选择多个文件进行处理的接口。

## 入门实例：使用拖放处理多个文件

`FileList`接口提供了处理来自本地文件系统的`File`对象数组的能力。本实例展示如何将拖放区域与`FileList`结合使用，以处理用户选择的多个文件。这有多种不同用途，包括按名称、大小或类型过滤文件，以及让用户确认他们选择的文件。一旦文件被拖放到放置区域，脚本将使用`length`属性遍历`FileList`序列。`length`属性返回`FileList`中的元素数量（即`File`对象数量），可用于“遍历”文件序列。对于每个`File`对象，页面将在表格中显示文件属性，以向查看者确认哪些内容被放置到了页面的放置区域。要创建拖放页面，请按照以下步骤和清单14.2中的代码操作：

1. 创建清单14.2中的页面，包含放置区域和`filesSelected`部分的样式和正文标签。确保`input`元素具有`multiple`属性和`onchange`事件处理程序。
2. 在`init`函数中添加放置区域事件监听器，并添加`handleFileDrop`和`handleDragOver`函数以启用放置区域。

### 清单14.2 使用FileList遍历多个文件

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>14.2 使用 FileList 处理多个文件</title>
<style>
#dropZone {
  width:300px;
  border: 2px dashed #bbb;
  -moz-border-radius: 5px;
  -webkit-border-radius: 5px;
  border-radius: 5px;
  padding: 25px;
  text-align: center;
  font: 20pt bold;
  color: #bbb;
}
#fileTable {
  border: 1px solid #000;
  -moz-border-radius: 5px;
  -webkit-border-radius: 5px;
  border-radius: 5px;
  padding: 5px;
  visibility:hidden;
}
tr:nth-child(odd)  { background-color:#eee; }
tr:nth-child(even) { background-color:#fff; }
</style>
<script>
// 初始化我们的拖放区域
function init() {
    // 设置拖放区域和事件监听器。
    dropZone = document.getElementById('dropZone');
    dropZone.addEventListener('dragover', handleDragOver, false);
    dropZone.addEventListener('drop', handleFileDrop, false);
}
// 处理拖放的文件
function handleFileDrop(evt) {
    // 阻止默认的拖放行为
    evt.stopPropagation();
    evt.preventDefault();
    // 获取文件列表
    var files = evt.dataTransfer.files;
    // 显示选中的文件列表
    displayFiles(files);
}
// 处理拖拽经过事件
function handleDragOver(evt) {
    // 在拖拽经过时阻止默认行为
    evt.stopPropagation();
    evt.preventDefault();
}
// 显示选中的文件
function displayFiles(files) {
    // 清空当前表格
    clearTable();
    // 显示选中的文件数量
    var fileCount = document.getElementById('fileCount');
    fileCount.innerHTML = files.length + ' 个文件被选中';
    // 设置表格生成的字段
    var fileTable = document.getElementById('fileTable');
    if (files.length>0) {
        var row;
        var cell;
        var textNode;
        // 遍历文件列表并创建行
        for (var i=0; i<files.length; i++) {
            // 添加行
            var row = fileTable.insertRow(i);
```



```
// 添加文件名单元格
cell = row.insertCell(0);
textNode = document.createTextNode(files[i].name);
cell.appendChild(textNode);

// 添加文件类型单元格
cell = row.insertCell(1);
textNode = document.createTextNode(files[i].type);
cell.appendChild(textNode);

// 添加文件大小单元格
cell = row.insertCell(2);
textNode = document.createTextNode((files[i].size/1024).toFixed(2)+'KB');
cell.appendChild(textNode);

if (files[i].lastModifiedDate != undefined) {
  // 添加文件最后修改日期单元格
  cell = row.insertCell(3);
  textNode = document.createTextNode(files[i].lastModifiedDate);
  cell.appendChild(textNode);
}
}

fileTable.style.visibility = 'visible';

} else {
fileTable.style.visibility = 'hidden';
}
}

// 清空表格
function clearTable() {
// 获取表格
var fileTable = document.getElementById('fileTable');
// 循环移除现有行
while (fileTable.rows.length>0) {
fileTable.deleteRow(fileTable.rows.length-1);
}
}

// 初始化窗口
window.addEventListener('load',init,false);
</script>
</head>
<body>
<h1>将多个文件拖到下面的拖放区域：</h1>
<section id="fileSelection">
<!--
// 多文件部分也可以通过 multiple 属性来实现
<input type="file" id="input" multiple="true" onchange="displayFiles(this.files)">
-->
<div id="dropZone">将文件拖放到此处</div>
</section>
<section id="filesSelected">
<br>
<div id="fileCount"></div>
<table id="fileTable">
</table>
</section>
</body>
</html>
```

## 第 364 页 第 14 章 处理本地文件

页面在浏览器中加载后，通过窗口`load`事件监听器调用的`init`函数初始化拖放区域。`init`函数将`dropzone`变量设置为拖放区域的`div`，并为`dragover`和`drop`事件注册两个事件监听器。当`dragover`事件被触发时，将调用`handleDragOver`函数；当`drop`事件被触发时，将调用`handleFileDrop`函数。当文件被放置到拖放区域并且`handleFileDrop`被调用时，脚本将检索`FileList`并将其传递给`displayFiles`方法。

`displayFiles`函数调用辅助函数`clearTable`来清除任何先前的结果。`clearTable`从表格中移除行，直到所有行都被移除。接下来，`displayFiles`检查`FileList`的长度，以验证是否有文件被放置到拖放区域。脚本使用索引遍历`FileList`，以获取每个`File`接口。对于每个`File`对象，检索其属性并将它们作为新行中的单元格添加到表格中。最后，脚本通过使表格可见来显示它，如示例执行图 14.1 所示。

通过使用拖放区域和`FileList`序列，HTML5 使得访问者能够轻松地将文件提交到客户端页面。然而，到目前为止，您已经查看了文件的属性，而不是文件中的数据。在本章的其余部分，您将学习如何在客户端 JavaScript 中读取不同类型的文件。

## 将多个文件拖到下面的拖放区域：

![](img/de30ea99ecac39b49e690a84c48f43b9_396_0.png)

**4 个文件被选中**

| 名称 | 类型 | 大小 | 日期 |
| :--- | :--- | :--- | :--- |
| contacts.csv | text/csv | 531.01KB | Thu Feb 26 2009 14:13:16 GMT-0500 (EST) |
| contacts.xls | application/vnd.ms-excel | 767.50KB | Thu Feb 26 2009 14:11:38 GMT-0500 (EST) |
| DSC_4269.JPG | image/jpeg | 3185.01KB | Fri Sep 18 2009 15:02:06 GMT-0400 (EDT) |
| good_code.png | image/png | 38.18KB | Sun Mar 06 2011 14:53:32 GMT-0500 (EST) |

图 14.1 显示拖放文件到页面上多个属性的示例输出

www.it-ebooks.info

> **提示**
> 从`Blob`接口继承的`File`接口的`type`属性返回文件的多用途互联网邮件扩展 (MIME) 类型。MIME 类型是一个全小写、ASCII 编码的`DOMString`。此 MIME 类型字符串可用于根据文件类型（如图像等）进行过滤。如图 14.1 所示，有两种不同类型的图像，但 MIME 类型都以`image`开头，因此您可以轻松验证这两个文件都是图像。MIME 类型提供了一种简单有效的方式来执行文件过滤和验证，正如您将在下一节中看到的。

## FileReader 接口

要将文件读入客户端内存，HTML5 File API 规范提供了一个名为`FileReader`的新接口。此接口提供了允许开发者从客户端 JavaScript 异步读取文件的方法、属性和事件。通过`FileReader`事件，您可以显示或处理文件数据。可以读取多种不同类型的文件，因为`FileReader`接口根据您可能读取的文件类型提供了四种不同的读取方法：

- `readAsArrayBuffer(Blob)`：将文件内容作为`ArrayBuffer`返回。
- `readAsBinaryString(Blob)`：将文件内容作为二进制字符串返回。
- `readAsText(Blob [,encoding])`：将文件内容作为文本`DOMString`返回。
- `readAsDataURL(Blob)`：将文件内容作为表示数据 URL 的`DOMString`返回。

由于`FileReader`接口是异步的，这允许页面的主线程继续处理，同时使用事件来捕获文件读取的关键阶段。表 14.2 显示了定义为`FileReader`接口一部分的事件。

| 事件名称 | 属性 | 目的 |
|---|---|---|
| loadstart | onloadstart | 当开始读取文件时触发 |
| progress | onprogress | 在读取文件期间由浏览器自行决定触发 |
| abort | onabort | 当执行中止操作时触发 |
| error | onerror | 当读取文件时遇到错误时触发 |
| load | onload | 当文件被成功读取时触发 |
| loadend | onloadend | 当文件读取完成（无论成功或失败）时触发 |

## 第14章 处理本地文件

通过使用适当的`FileReader`读取方法并监听`FileReader`事件，您可以利用`FileReader`接口在客户端浏览器中执行通常在文件上传后在服务器端才会进行的工作。在接下来的这个方法中，您将使用`readAsDataURL`方法在用户的浏览器中为选定的图像创建缩略图，并显示它们的相应属性。

> **注意**
> 文件读取可以通过与 Web Worker 一起使用`FileReaderSync`来作为同步接口，因为 Web Workers API 允许这些方法在与主线程不同的线程上执行。`FileReaderSync`接口具有与`FileReader`相同的方法。有关同步文件 API 使用的更多信息，请参阅 W3C 工作草案。

### 中级方法：通过`readAsDataURL`预览图像

`FileReader`接口的`readAsDataURL`方法接受一个提供的`Blob`或`File`引用，并将数据读入一个可以在适当容器中加载的 URL。在这个方法中，您将让访问者选择多个文件，然后从文件集合中过滤出图像，通过`readAsDataURL`读取它们，并将它们加载到图像容器中作为缩略图进行查看。通常，在 HTML5 File API 之前复制此功能，您需要将文件上传到服务器，在服务器上处理它们，然后将它们加载到客户端浏览器页面中。这需要增加文件来回发送和服务器上处理文件的开销。通过使用 HTML5 File API，您可以消除来回发送文件的需要，并利用客户端计算机的处理能力来执行文件的处理。

这个方法将使用`readAsDataURL`方法以及`onload` `FileReader`事件来读取选定的文件。此外，当您将鼠标悬停在缩略图上时，该方法将显示每个文件的属性。要开始使用这个方法，请执行以下步骤以创建清单 14.3：

- 1. 创建一个空白的 HTML 文件并添加清单 14.3 中的`body` HTML，其中包括多文件`input`元素、用于显示缩略图的部分以及用于显示属性的部分。
- 2. 添加`style`部分，其中包括用于处理图像选择和取消选择的三个样式集。
- 3. 如清单 14.3 所示，在脚本中添加`handleFiles`函数，该函数在文件被选择后触发。
- 4. 添加`showFile`函数以显示鼠标悬停文件的属性。
- 5. 添加`clearFile`函数，当焦点不再停留在图像上时，该函数简单地清除属性区域。

### 清单 14.3 使用 readAsDataURL 预览图像

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>14.3 FileReader - imgPanel 本地图像</title>
<style>
.highlight,.unhighlight {
  max-height:100px;
  max-width:100px;
  -moz-border-radius: 5px;
  -webkit-border-radius: 5px;
  border-radius: 5px;
  margin:10px;
}
.highlight {
  border: 5px solid #6f0;
}
.unhighlight {
  border: 5px solid #000;
}
</style>
<script>
// 加载选定的图像文件
function handleFiles(files) {
  // 设置默认值
  var fileLimit = 10;        // 一次最大文件数
  var sizeLimit = 500;        // KB 文件大小限制
  var imageType = /image.*/;  // 图像的 MIME 类型 - 正则表达式

  // 引用图像面板并清空
  var imgPanel = document.getElementById('imgPanel');
  imgPanel.innerHTML = '';

  // 以字节为单位计算文件大小限制
  var sizeLimitBytes = sizeLimit*1024;

  // 检查文件数量是否超过限制
  if (files.length<fileLimit) {
    // 遍历文件列表
    for (var i = 0; i < files.length; i++) {
      // 引用当前文件
      var file = files[i];

      // 验证文件是图像
      if (file.type.match(imageType)) {
        // 验证文件未超过最大大小
        if (file.size<sizeLimitBytes) {
          // 为文件创建一个图像容器
          var img = document.createElement("img");
          img.file = file;
          img.className = 'unhighlight';
          img.addEventListener('mouseover', showFile, false);
          img.addEventListener('mouseout', clearFile, false);
          imgPanel.appendChild(img);

          // 创建读取器来读取文件
          var reader = new FileReader();

          // 设置读取器的 onload 事件
          reader.onload = (function(aImg) { return function(e) { aImg.src = e.target.result; }; })(img);

          // 将文件作为数据 URL 读取以获取图像
          reader.readAsDataURL(file);
        } else {
          // 文件太大
          alert(file.name+' 大于 '+sizeLimit+'KB。');
        }
      } else {
        // 文件不是图像 MIME 类型
        alert(file.name+' 不是图像。');
      }
    }
  } else {
    // 选择了太多文件
    imgPanel.innerHTML = '一次只能选择 '+fileLimit+' 个文件。';
  }
}

// 显示鼠标悬停图像上的信息
function showFile() {
  // 高亮显示当前图像
  this.className = 'highlight';

  // 获取属性面板和文件的引用
  var fileAttributes = document.getElementById('fileAttributes');
  var file = this.file;

  // 创建文件信息
  var fileinfo = '文件信息：<br>';
  fileinfo += file.name + '<br>';
  fileinfo += file.type + '<br>';
  fileinfo += (file.size/1024).toFixed(2) + 'KB<br>';
  fileinfo += file.lastModifiedDate + '<br>';

  // 显示文件信息
  fileAttributes.innerHTML = fileinfo;
}

// 鼠标移出图像后重置
function clearFile() {
  // 清空文件属性面板
  var fileAttributes = document.getElementById('fileAttributes');
  fileAttributes.innerHTML = '';

  // 将图像高亮恢复为正常
  this.className = 'unhighlight';
}
</script>
</head>
<body>
  <h1>选择要预览的图像。</h1>
  <section>
    <input type="file" id="input" multiple="true"
      onchange="handleFiles(this.files)">
  </section>
  <section id="imgPanel"></section>
  <section id="fileAttributes"></section>
</body>
</html>
```



## 使用 `FileReader` 处理本地文件

当清单 14.3 创建的页面加载时，访问者将被提示选择一个文件或一组文件。文件选定后，`input` 元素的 `onchange` 事件被触发，该事件启动 `handleFiles` 函数并传递已选定的文件。`handleFiles` 函数是脚本的核心，并首先设置关键默认值。这些默认值包括允许的最大文件数、每个文件的最大大小，以及一个将用于匹配图像 MIME 类型的正则表达式。限制文件大小和数量是为了防止客户端浏览器的内存过载，因为处理将在客户端机器的内存中执行。在这个方法中，您将循环遍历文件，这将创建同时工作的多个 `FileReader`。脚本可以在处理方面更智能一些，维护一个读取器池，只有在读取器空闲时才处理下一个文件，但这将留给您自己实现。

脚本接下来检查您选择的文件数量是否少于最大值，如果不是，则显示相应的消息。如果您选择的文件数量可控，那么您将循环遍历 `FileList`，并通过匹配 MIME 类型验证每个文件是否为图像，并确保每个文件都小于您设置的最大文件大小。如果每个文件都满足这些要求，那么该方法将创建一个图像容器，其属性包括用于显示属性的 `mouseover` 和 `mouseout` 事件。现在，脚本已准备好通过为每个图像创建一个新的 `FileReader` 来读取文件。脚本将 `onload` 事件设置在 `FileReader` 上，以将 `FileReader` 的结果加载到图像元素的源属性中，从而创建实际的缩略图，如图 14.2 所示。

最后，您告诉 `FileReader` 通过 `readAsDataURL` 方法读取每个文件，该方法将返回用于图像源的数据 URL 结果。函数的其余部分处理各种检查失败的情况，并向用户显示相应的消息。`showFile` 和 `clearFile` 方法显示文件的属性。

这个方法展示了 `FileReader` 接口的基本实现以及可用的读取方法之一。此外，我们希望这个方法已经向您展示了在客户端浏览器中同时运行多个异步读取时必须注意的问题。要实际看到这个限制，请增加文件大小和数量的限制（但要小心操作，因为很容易耗尽浏览器的内存）。在下一个方法中，您将了解 `FileReader` 接口上的一些附加功能，这些功能将允许您中止处理并捕获可能发生的错误。

## 高级技巧：使用 `readAsText` 解析 CSV 文件

至此，你应对 `FileReader` 接口在客户端浏览器处理文件方面提供的前景感到兴奋。这种方法可以将原本需要在服务器端处理的任务转移到客户端。其中一个典型应用就是导入逗号分隔值（CSV）格式的数据文档。通常，文件会被上传到服务器，然后立即或按计划进行解析，最后导入数据库，供网站或应用程序使用。这个过程可能会占用宝贵的服务器资源。

在这个技巧中，我们将展示一种使用 HTML5 的替代方案，即使用 `readAsText` 方法。这个技巧将允许用户选择一个本地 CSV 文件。然后，该文件将在客户端浏览器中被读取和解析，并显示行和字段。但请注意，本技巧中的 CSV 解析逻辑并不处理 CSV 结构的复杂性。你可以在网上找到多个用于健壮解析 CSV 文件的算法。这个技巧更多地是展示使用 `FileReader` 和 `readAsText` 方法的流程。解析后，字段可以放入 JSON 字符串，并通过 Ajax 网络服务调用发送到服务器进行处理。

除了新方法 `readAsText`，本技巧还将使用 `FileReader` 上的 `abort` 函数。此方法允许脚本或用户中止读取过程。当 `abort` 方法被成功调用时，`FileReader` 会抛出一个 `ABORT_ERR` 错误来确认中止已发生。由于读取文件或提供的 Blob 时出现问题，`FileReader` 可能抛出五种可能的错误，如表 14.3 所示。

表 14.3 可能的 `FileReader` 错误

| 错误常量 | 值 | 说明 |
| :--- | :--- | :--- |
| `NOT_FOUND_ERR` | 1 | 当找不到要读取的文件时抛出错误。 |
| `SECURITY_ERR` | 2 | 当文件在读取过程中可能已更改、文件被视为不安全或对文件进行的读取操作过多时抛出错误。 |
| `ABORT_ERR` | 3 | 当调用中止方法时抛出错误。 |
| `NOT_READABLE_ERR` | 4 | 无法读取文件。通常是因为文件权限问题。 |
| `ENCODING_ERR` | 5 | 当 `readAsDataURL` 的结果不是数据 URL 的形式时抛出错误。此错误不涉及将文件作为文本读取时的编码问题。 |

在这个技巧中，你将探索 `FileReader` 提供的最后一个事件处理程序 `onprogress`。`onprogress` 事件处理程序提供读取文件的进度通知，可用于向用户显示状态。`onprogress` 事件处理程序包含三个属性：`lengthComputable`、`loaded` 和 `total`。`lengthComputable` 属性是一个布尔标志，用于标记 `loaded` 和 `total` 属性是否可用。`loaded` 属性是已读取到内存中的字节数，而 `total` 是要读取的总字节数。通过将 `progress.loaded` 除以 `progress.total`，你可以计算出完成百分比并显示给用户。在这个技巧中，当文件读取到内存时，页面将显示一个进度条来指示状态。但请注意，进度事件是由每个浏览器对 `FileReader` 接口的实现自行决定的，因此无法保证事件何时或以多大频率触发。以下步骤将创建清单 14.4 中的代码：

1. 创建一个空白 HTML 页面，包含如清单 14.4 所示的 HTML `body` 和 `style` 标签，包括文件选择、取消按钮、文件信息部分和文件输出 `div`。
2. 添加各种类的样式标签和样式，包括隐藏取消按钮。
3. 添加 `script` 标签和对名为 `textReader` 的 `FileReader` 实例的全局引用。这将是用于读取所选 CSV 文件的 `FileReader` 实例。
4. 添加 `addEventListener load` 行和 `init` 函数，用于为 `textReader` 事件注册相应的函数。
5. 添加相应的事件函数：`onErrorHandler`、`updateProgress`、`onAbortHandler`、`onLoadStartHandler` 和 `onLoadHandler`。
6. 添加 `cancelFileReader` 函数，允许访客中止读取过程。
7. 添加 `handleFile` 函数，该函数通过 `readAsText` 方法启动对所选文件的读取过程。

### 清单 14.4 显示 CSV 文件的内容

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>14.4 Basic File API</title>
<style>
#fileInfo {
    border: 1px solid #000;
    -moz-border-radius: 5px;
    -webkit-border-radius: 5px;
    border-radius: 5px;
padding: 5px;
visibility:hidden;
}
#progHolder {
  float:right;
  width:200px;
  height:30px;
  border:solid;
  border-width:1px;
  background-color:#999;
  text-align:center;
}
#progMeter {
  width:0px;
  height:30px;
  background-color:#9FF;
}
#btnCancel {
  visibility:hidden;
}
</style>
<script>
// set up a filereader
var textReader = new FileReader();

function init() {
  // set up our filereader handlers
  textReader.onerror     = onErrorHandler;
  textReader.onprogress  = updateProgress;
  textReader.onabort     = onAbortHandler;
  textReader.onloadstart = onLoadStartHandler;
  textReader.onload      = onLoadHandler;
}

// handle the selected file
function handleFile(inputFile) {

  // the csv mime type for regular expression
  var csvMimeType = /text\/csv/;

  // reference our selected file
  var file = inputFile.files[0];

  // verify that the file is a csv file
  if (file.type.match(csvMimeType)) {
// make the file info section visible
var fileInfo = document.getElementById("fileInfo");
fileInfo.style.visibility = 'visible';

// kick off the reader to read the csv file
textReader.readAsText(file);

// set our file info - the filereader is asynchronous
// so this will display
var output = 'File attributes:<br>';
output += 'name: ' + file.name + '<br>';
output += 'type: ' + file.type + '<br>';
output += 'size: ' + (file.size/1024).toFixed(2) + 'KB<br>';
output += 'last modified date: ' + file.lastModifiedDate;

// display the file attributes
var fileAttributes = document.getElementById('fileAttributes');
fileAttributes.innerHTML = output;

} else {
  // inform user that the file is not a csv
  alert(file.name + ' is not a CSV file.');
}
}

// cancel filereader function
function cancelFileReader() {

  // tell the filereader to abort
  textReader.abort();
}

// triggered filereader onloadstart handler
function onLoadStartHandler(evt) {

  // get our local element references
  var btnCancel = document.getElementById('btnCancel');
  var progMeter = document.getElementById('progMeter');
  var fileoutput = document.getElementById('fileoutput');

  // reset our cancel button, progress meter, and file output
  btnCancel.style.visibility = 'visible';
  progMeter.style.width = '0%';
  progMeter.innerHTML = 'loading...';
  fileoutput.innerHTML = '';
}
// triggered filereader onload handler
function onLoadHandler(evt) {
  // set our progress meter to 100% and hide the cancel button
  var progMeter = document.getElementById('progMeter');
  var btnCancel = document.getElementById('btnCancel');
  progMeter.style.width = '100%';
  progMeter.innerHTML = 'loaded.';
  btnCancel.style.visibility = 'hidden';

  // split the file into an array for processing
  var fileArr = evt.target.result.split('\n');

  // process each row and set to rows in a table
  // this is a simplistic processing for csv and
  // does not handle differences in csv format
  var strDiv = '<table>';
  for (var i=0; i<fileArr.length; i++) {
    strDiv += '<tr>';
    var fileLine = fileArr[i].split(',');
    for (var j=0; j<fileLine.length; j++) {
      strDiv += '<td>'+fileLine[j].trim()+'</td>';
    }
    strDiv += '</tr>';
  }
  strDiv += '</table>';

  // set our output
  var fileoutput = document.getElementById('fileoutput');
  fileoutput.innerHTML = strDiv;
}

// progress handler for the filereader
function updateProgress(evt) {
  // reference to our progress meter
  var progMeter = document.getElementById('progMeter');

  // compute and display the progress
  if (evt.lengthComputable) {
    var loaded = Math.round((evt.loaded / evt.total)*100);
    if (loaded < 100) {
      progMeter.style.width = loaded + '%';
    } else {
      progMeter.style.width = '100%';
    }
  }
}
```

```javascript
// 处理文件读取器读取过程中的任何中止操作
function onAbortHandler(evt) {
  alert('文件读取已取消');
}

// 处理文件读取器的任何错误
function onErrorHandler(evt) {
  switch(evt.target.error.code) {
    case evt.target.error.NOT_FOUND_ERR:
      alert('文件未找到！');
      break;
    case evt.target.error.SECURITY_ERR:
      alert('文件安全错误。');
      break;
    case evt.target.error.ABORT_ERR:
      break;
    case evt.target.error.NOT_READABLE_ERR:
      alert('文件不可读。');
      break;
    case evt.target.error.ENCODING_ERR:
      alert('文件编码错误。');
      break;
    default:
      alert('读取文件时发生错误。');
  };
}

// 初始化我们的窗口
window.addEventListener('load', init, false);

</script>
</head>
<body>
  <h1>选择一个要处理的CSV文件。</h1>
  <section>
    <input type="file" id="input" onchange="handleFile(this)">
    <button id="btnCancel" onclick="cancelFileReader();">取消处理</button>
  </section>
  <br>
  <section id="fileInfo">
    <div id="progHolder">
      <div id="progMeter"></div>
    </div>
    <div id="fileAttributes"></div>
  </section>
  <br>
  <div id="fileoutput"></div>
</body>
</html>
```



当页面加载到浏览器中时，访问者可以浏览并选择一个CSV文件进行读取。选择文件后，`handleFile`方法会被调用，并将文件作为参数传入。`handleFile`方法首先通过匹配MIME类型的正则表达式来验证是否选择了CSV文件。如果文件与CSV的MIME类型不匹配，则会显示一个提醒，告知用户该文件不是CSV格式的文件。如果文件是CSV格式的，则代码会调用`FileReader`实例的`readAsText`方法，并将文件作为参数传入。这将启动一个异步读取过程，该过程会在读取进度中触发相应的事件。为了验证读取是异步的，你在调用`readAsText`函数之后才放置了文件属性的显示代码。由于读取不会阻塞脚本的主线程，因此在调用`readAsText`后，属性会立即显示。

在脚本的`init`函数中，你注册了`onLoadStartHandler`函数，以便在`onloadstart`事件发生时被调用。当`FileReader`开始读取文件时，`onloadstart`事件将被触发。当此事件发生时，`onLoadStartHandler`会显示取消按钮、进度条和输出区域。

在文件读取过程中，当`FileReader`触发`onprogress`事件时，会调用`updateProgress`方法来更新进度条。`updateProgress`方法通过检查`lengthComputable`属性来验证`loaded`和`total`属性是否可用。该属性如果为真，则基本表明`loaded`和`total`属性是可用的。`updateProgress`将使用`loaded`和`total`来计算完成百分比，并通过进度条显示此值。进度条是通过设置`progHolder` div中`progMeter` div的宽度来构建的。

如果文件被`FileReader`读取完成，则会触发`onload`事件，并调用`onLoadHandler`函数，读取结果将包含在传递给该方法的事件中。在方法内部，你关闭了取消按钮，并将进度标记为100%，以便访问者知道文件已被读取到内存中。由于CSV文件是基于行的，接下来你通过执行以下代码行，将结果按换行符分割成行数组：

```javascript
var fileArr = evt.target.result.split('\n');
```

`result`引用的是内存中的文本文件。在将结果分割成行（或逗号分隔值行）数组后，脚本会遍历每个数组元素，并用逗号字符分割值。当脚本遍历每一行时，值会被添加到一个输出字符串中，所有行处理完毕后，该字符串会显示在文件输出区域中，如图14.3所示。

![](img/de30ea99ecac39b49e690a84c48f43b9_410_0.png)

本示例中用于解析逗号分隔值文件的方法相当简单；它没有处理值中嵌入逗号的情况，也不理解带引号值和不带引号值的区别。你可以在网上找到更全面的解析方法，但为了展示`readAsText`方法的工作原理，本示例使用了一个简单的模型。

本示例通过一个取消按钮包含了中止选项。如果访问者在`FileReader`读取文件期间点击了取消按钮，则会调用`cancelFileReader`方法，该方法继而调用`FileReader`实例（`TextReader`）的`abort`方法。这会指示`FileReader`实例取消读取过程，移除内存中已读取的任何信息，并触发`onabort`事件。反过来，脚本将通过`onaborthandler`方法捕获`onabort`事件，并向访问者显示一条消息，确认读取已取消。

你还会注意到，脚本包含了一个针对`onerror`事件传递的任何错误的错误处理程序。当读取过程中止时，会创建一个名为`ABORT_ERR`的错误事件，并调用`onErrorHandler`方法处理此错误。由于你在其他地方处理了中止操作，脚本会简单地忽略此错误。然而，可能会遇到的其他错误将通过向用户显示适当的消息来处理。

本示例展示了在客户端浏览器中使用`FileReader`接口处理CSV文件的强大功能。CSV文件解析的结果可以被过滤、显示，并打包后传输到Web服务器，而无需服务器端的任何工作。本示例包含了读取文件、中止进程以及处理可能出现的错误的功能。这应该能为你开始处理自己网页中的文件提供一个模板。

### 文件API扩展规范

你可能想知道是否可以浏览系统目录、创建文件并写入它们。基于文件API，有两个新的规范正在制定中，以处理这些确切的用例。第一个是`File API: Directories and System`，第二个是`File API: Writer`规范。这些规范已经历了几个版本并且仍在变动中，因此尚未被许多浏览器实现。事实上，目前唯一支持这些扩展文件API对象和方法的浏览器是Chrome。

> 注意：在Chrome 12及更新版本中，浏览器使用自定义版本的`requestFileSystem`调用，即`webkitRequestFileSystem`。该调用的参数相同，但你需要根据Chrome版本有条件地使用正确的调用。理想情况下，随着规范的完善以及更多浏览器支持文件API规范，这些调用将再次通用并在所有浏览器中保持一致。

在目录和写入器文件API中有几个对象和方法，但其中一些对于本示例以及处理文件系统和文件至关重要。以下是一些更有用的目录和系统接口：

- `FileSystem`：表示正在操作的文件系统
- `Entry`：表示文件系统中的一个通用条目
- `DirectoryEntry`：表示文件系统中的一个目录
- `FileEntry`：表示文件系统中的一个文件

以下是一些更有用的文件写入器接口：

- `BlobBuilder`：用于管理与文件接口一起使用的数据Blob
- `FileSaver`：用于监视写入事件和进度
- `FileWriter`：用于写入、截断和追加文件

`DirectoryEntry`和`FileEntry`接口构建在`Entry`接口之上，后者具有标准的复制、移动和删除方法。目录和写入器API集合具有相应的事件和一组可能的错误。此外，API提供了异步调用（用于嵌入式使用）和同步调用（用于Web Worker）。每个接口都有方法和属性，我们建议你查阅最新的规范以获取当前信息。然而，表14.4描述了本章中你将要使用的一些方法。`FileWriter`接口还具有`length`和`position`属性，可用于定位要追加或写入文件信息的位置。目录和系统相关的多个方法包括复制和移动，并且包含你在普通目录和文件浏览器中常见的文件和目录属性。这些方法和属性将使

## 第14章 使用本地文件

表14.4 关键文件目录与系统，以及编写器方法

| 接口 | 方法 | 目的 |
| :--- | :--- | :--- |
| `FileSystem` | `requestFileSystem` | 请求一个用于存储应用数据的文件系统 |
| `Entry` | `copyTo` | 将目录或文件的条目复制到给定位置 |
| `Entry` | `getMetadata` | 获取此条目的元数据 |
| `Entry` | `getParent` | 获取条目的父级目录条目 |
| `Entry` | `moveTo` | 将条目从当前文件系统位置移动到不同位置 |
| `Entry` | `remove` | 删除该条目，无论是文件还是目录 |
| `Entry` | `toURL` | 返回可用于引用的给定条目的URL |
| `FileEntry` | `createWriter` | 创建一个文件编写器实例，用于写入文件 |
| `FileEntry` | `file` | 返回`FileEntry`指向的文件 |
| `FileWriter` | `seek` | 设置文件中下次执行写入方法的位置 |
| `FileWriter` | `truncate` | 通过缩短或扩展来改变文件的长度 |
| `FileWriter` | `write` | 将提供的数据写入文件的当前位置 |

制作自己的文件和目录浏览器相当容易。不幸的是，我们在此没有篇幅来创建一个这样的食谱，但你可以在目录和系统API规范中找到使用这些方法和属性的所有必要信息。不过需要注意的一点是，这些接口似乎处理的是浏览器为安全目的在源自域的特定沙箱中“生成”的文件系统。在下一个食谱中，你将创建一个本地文件并写入一些数据。

## 高级食谱：创建本地文件

在此食谱中，你将创建一个页面，该页面使用本地文本文件存储用户添加的电子邮件地址列表。该页面将允许用户添加电子邮件地址，该地址将追加到文件中；显示文件中的电子邮件地址列表；并删除文件。

> 由于目前没有允许用户授权浏览器访问本地文件存储的安全权限接口，你必须通过启动带有两个参数的Chrome浏览器来授予该权限：`--unlimited-quota-for-files`和`--allow-file-access-from-files`。要使用这些参数启动Chrome浏览器，你可以在Mac OS中启动终端并使用以下命令：
>
> `open /Applications/Google\ Chrome.app -n --args -unlimited-quota-for-files -allow-file-access-from-files`
>
> 此命令将启动Chrome浏览器，并传递命令行参数，指示浏览器允许文件访问并为文件设置无限配额。如果不以这种方式启动Chrome，你将收到安全或权限错误，阻止你访问文件系统。

此脚本通常会使用`requestFileSystem`方法来获取对本地文件系统的引用；然而，在Chrome 12及更新版本中，浏览器使用了自己的版本方法`webkitRequestFileSystem`，因为规范一直在变动。此外，脚本中使用条件逻辑，根据浏览器版本通过`BlobBuilder`或`WebKitBlobBuilder`创建`Blob`对象。要创建该页面，请执行以下步骤来创建清单14.5：

1. 创建一个空白HTML文件，并添加清单14.5中的`body` HTML，其中包含电子邮件输入元素、多个`button`元素以及用于显示电子邮件地址列表的显示`div`。
2. 添加`fileErrorHandler`函数，该函数将处理异步代码遇到的任何目录或文件错误。
3. 在清单14.3所示的脚本中添加`fileAction`函数，该函数获取文件引用并根据用户请求的操作进行分派。
4. 添加`writeToFile`、`readFromFile`和`removeFile`函数，这些函数处理传入文件引用的具体操作。
5. 添加页面加载的事件监听器，该监听器将启动`fileAction`方法以显示存储文件中存在的任何电子邮件地址。

### 清单14.5 在本地文件中存储电子邮件列表

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>14.5 文件创建/异步写入</title>
<script>
// 文件API错误处理器
function fileErrorHandler(e) {
  var msg = '';

  // 根据代码设置适当的错误消息
  switch (e.code) {
    case FileError.NOT_FOUND_ERR:
      msg = '未找到文件或目录。';
      break;
    case FileError.SECURITY_ERR:
      msg = '发现安全问题。';
      break;
    case FileError.NOT_READABLE_ERR:
      msg = '无法读取文件或目录。';
      break;
    case FileError.ENCODING_ERR:
      msg = '文件或目录的地址格式错误。';
      break;
    case FileError.NO_MODIFICATION_ALLOWED_ERR:
      msg = '无法修改文件或目录。';
      break;
    case FileError.INVALID_STATE_ERR:
      msg = '文件或目录状态错误。';
      break;
    case FileError.SYNTAX_ERR:
      msg = '写入文件时语法错误。';
      break;
    case FileError.INVALID_MODIFICATION_ERR:
      msg = '请求的修改无效。';
      break;
    case FileError.QUOTA_EXCEEDED_ERR:
      msg = '存储配额剩余空间不足。';
      break;
    case FileError.TYPE_MISMATCH_ERR:
      msg = '文件或目录类型错误。';
      break;
    case FileError.PATH_EXISTS_ERR:
      msg = '路径已存在。';
      break;
    default:
      msg = '未知的文件API错误。';
      break;
  };

  console.log('文件API错误: ' + msg);
}

// 获取文件系统并分派操作的函数
function fileAction(actionType) {

  var fileName = 'HTML5FileText.txt';

  // 开始使用文件系统的异步过程
  // 获取fileSystem对象
  window.webkitRequestFileSystem(window.PERSISTENT, 1024 * 1024,
    function(fileSystemObj) {

    // 获取文件的引用，如果不存在则创建文件
    fileSystemObj.root.getFile(fileName, {create:true}, function(fileEntry) {

      // 分派到处理程序函数
      switch (actionType) {
        case 'write':
          writeToFile(fileEntry);
          break;
        case 'read':
          readFromFile(fileEntry);
          break;
        case 'remove':
          removeFile(fileEntry);
          break;
      }
    }, fileErrorHandler);
  }, fileErrorHandler);
}

// 用于将条目追加到文件的异步处理程序
function writeToFile(fileEntry) {

  // 创建文件的编写器
  fileEntry.createWriter(function(fileWriter) {

    // 编写器的onwriteend处理程序
    fileWriter.onwriteend = function(e) {
      console.log('写入文件成功。');
      readFromFile(fileEntry);
    };

    // 编写器的onerror处理程序
    fileWriter.onerror = function(e) {
      console.log('写入文件失败: ' + e.toString());
    };

    // 创建用于添加到文件的blob
    var bb = new (window.BlobBuilder || window.WebKitBlobBuilder)();
    var emailToAdd = document.getElementById('emailAddress').value + "<br/>";
    bb.append(emailToAdd);

    // 定位到文件末尾，然后添加blob
    fileWriter.seek(fileWriter.length);
    fileWriter.write(bb.getBlob('text/plain'));

  }, fileErrorHandler);
}

// 读取文件的异步处理程序
function readFromFile(fileEntry) {

  // 获取文件对象
  fileEntry.file(function(file) {

    // 创建文件读取器
    var reader = new FileReader();

    // 读取器的onloadend处理程序
    reader.onloadend = function(e) {
      // 显示文件结果
      var emailDiv = document.getElementById('emailList');
      emailDiv.innerHTML = this.result;
    };

    // 使用读取器读取文件
    reader.readAsText(file);
  }, fileErrorHandler);
}

// 删除文件的异步处理程序
function removeFile(fileEntry) {

  // 删除文件
  fileEntry.remove(function() {
    console.log('文件已删除。');
  }, fileErrorHandler);
}

// 默认从文件读取
window.addEventListener('load',fileAction('read'),false);

</script>
</head>
```

## 14.5 使用本地文件（清单14.5示例）



```html
<body>
    <input type="email" id="emailAddress" /><button onClick="fileAction('write');">添加邮箱</button>
    <button onClick="fileAction('read');">读取邮箱</button>
    <button onClick="fileAction('remove');">删除文件</button>
    <br/><br/>
    <div id="emailList"></div>
</body>
</html>
```

要启动清单14.5中创建的页面，务必通过命令行启动Chrome浏览器，并传入授权访问本地文件系统的参数。如果Chrome未使用这些参数启动，页面将无法操作本地文件。页面加载时，会指示加载文件中的任何现有邮箱地址并进行显示（前提是文件当前存在）。这是通过调用`fileAction`函数并传入`read`值实现的。在`fileAction`函数中，首先通过`webkitRequestFileSystem`方法获取文件系统的引用，从而启动一系列异步函数调用。你需要向该函数传递文件持续时间标志、文件大小、内联回调函数和错误处理程序。持续时间标志告知浏览器如何处理文件，具体是允许浏览器在必要时删除文件（`TEMPORARY`），还是保留文件不变（`PERSISTENT`）。在此示例中，你为所有目录和文件方法调用创建了一个通用错误处理程序，尽管某些错误代码可能并不适用。不过，File API中的错误代码集合是一致的。当然，根据需要，你也可以为更专业的错误信息和操作设置单独的错误处理程序。

获得文件系统的句柄后，脚本随后在文件系统根对象上执行`getFile`方法，传入文件名、打开参数、成功回调和错误处理程序。在此情况下，当获取文件时，你通过将`create`标志设置为`true`来通知方法：如果文件不存在则创建文件。如果该标志设置为`false`，则方法不会在文件不存在时创建文件，而仅作为打开函数。获取文件条目后，脚本将流程分派到`readFromFile`函数，该函数通过获取文件并通过文件读取器对象实例读取文件来继续异步流程。文件读取器对象完成文件读取后，结果将显示在结果div中，如图14.4所示。

文件创建后，用户可以通过输入邮箱地址并点击“添加邮箱”按钮来添加地址，这将触发`fileAction`。`fileAction`将启动`writeToFile`，在其中你将创建一个`fileWriter`来将文本写入文件。脚本首先为`fileWriter`完成（`onwriteend`）以及如果文本写入因任何原因失败（`onerror`）设置一些处理程序。脚本使用`BlobBuilder`为输入的邮箱地址创建一个`Blob`对象。在此情况下，你根据Chrome版本的不同条件性地选择接口。然后，脚本使用文件写入器的`seek`方法，根据长度属性将位置移动到文件末尾，然后调用`write`命令以文本格式添加Blob。请注意，将地址追加到文件时，你在每个邮箱地址末尾添加了一个HTML换行符`<br/>`。这纯粹是为了在读取文件时，在div中显示多个邮箱地址更方便。你可以按照最适合你信息的布局来格式化文件的数据。将新邮箱地址写入文件后，脚本会触发一次读取操作以更新页面上显示的列表。

最后，脚本提供了文件的删除选项，它调用`FileEntry`上的`remove`方法。这将从文件系统中删除该文件。如果你离开页面后返回而未删除文件，由于你在调用`webkitRequestFileSystem`时请求文件系统持久保存该文件，该文件将会保留。在接下来的几个月里，这些规范预计会有很大进展，并且预计各种浏览器制造商将开始更多地集成File API：目录与系统API以及File API：Writer API。

## 本章小结

本章中的示例展示了如何通过客户端浏览器中的新File API查看文件属性和读取文件。此外，你了解了一些较新的文件规范，这些规范将增加超越仅仅读取文件的功能。通过将原本需要服务器端处理的工作负载转移到客户端浏览器，你可以将处理分布到客户端机器上，从而改善访问者的整体体验。

## 15 集成设备数据

在过去20年里，超文本标记语言（HTML）已经取得了长足的进步，并通过浏览器创建者和W3C工作组等各个团体的工作不断演进。我们所熟知的HTML5是HTML标签和属性、JavaScript API以及CSS样式的集合。在本书中，我们介绍了许多作为HTML5一部分创建的扩展API。然而，为了提升用户的浏览器体验，尤其是随着用户使用越来越多的移动设备，相关的工作努力并未停止，实际上比以往任何时候都更为强劲。在过去几年中，出现了大量新型移动设备，它们与过去的移动电话有一个根本性的不同。设备不再是一部具有众多其他功能的移动电话，而是一部将电话仅作为其中一项功能的移动设备。

在本章中，你将学习浏览器体验中最令人兴奋和新颖的领域之一：与设备功能（如摄像头、麦克风、陀螺仪、加速计）以及设备应用程序（如联系人数据库、日历应用和图片库）的集成。通过这些设备API，预计网页将能够执行广泛的功能，包括视频电话会议、在用户日历中安排约会、从用户图库插入图片、检查电池电量或其他通常仅限于本地设备应用程序或专用插件才能完成的任务。Web开发者很快也将受益于接入这些功能。

## 设备API简史

W3C设备API与策略工作组成立于2009年5月，旨在创建一组客户端API和事件，以便与设备硬件和应用程序交互。该工作组在其原始章程中定义了几个不同的API，这些API范围相当广泛，并与其他几个工作组有重叠。该工作组章程的预期结束日期定于2011年7月。然而，由于各种原因，该工作组于2010年11月进行了重组，聚焦于一组更集中的API。该工作组现在被称为设备API工作组，预计将在2010年11月至新的截止日期2013年6月之间创建几个专注于设备集成的API。

可以想象，对于设备API这样的主题，API覆盖的范围相当广泛。该工作组在为浏览器制造商创建用于使用的API和事件规范方面取得了巨大进展。尽管还处于早期阶段，但一些浏览器已经开始包含这些API。设备API工作组的API集合和事件包括：

- *应用注册API*：提供Web应用注册为系统中应用程序的能力，并允许应用程序通过注册的数据字符串标识符处理调用。
- *电池状态事件*：提供电池状态变化的事件，包括电池电量和充电状态。
- *蜂鸣API*：提供对设备系统蜂鸣声的控制。
- *日历API*：提供对设备上日历事件的读取访问。
- *通讯录API*：提供对设备通讯录存储应用中的联系人及其信息的读取访问。
- *图库API*：提供对设备图库的访问，图库可能包括音频、视频和图像文件。
- *通用传感器API*：提供对设备上各种传感器的集成和支持。
- *HTML媒体捕获*：提供属性和HTML能力，以便在设备上实时捕获媒体，如音频、视频和图像。
- *媒体捕获API*：提供通过设备的摄像头和麦克风捕获媒体的编程接口。
- *菜单API*：提供对应用程序设备菜单的控制。
- *消息API*：允许客户端页面发送基于mms、sms或mailto URI方案的消息。
- *网络信息API*：检索设备的当前网络连接类型。
- *任务API*：提供对设备上管理的个人任务的访问。
- *振动API*：提供对设备振动的控制。

目前，列出的API非常新，任何已在浏览器中实现的API都是例外。事实上，在撰写本书时，只有通讯录API达到了规范草案的最终征求意见阶段。标有星号（*）的规范在www.w3.org网站上发布了某种形式的草案。预计到2011年底，其中许多API将拥有其规范的工作草案版本。在本章中，我们将介绍这些API中的一部分，展示一些发展较完善的API，以及一些示例，其中……

## 第15章 集成设备数据

目前可用的API实现。需要注意的是，鉴于这些API尚处于早期阶段，现在断言哪些浏览器平台将支持哪些功能还为时过早。

## 通讯录API

通讯录API旨在允许与浏览器页面交互的用户，将其本地通讯录应用程序中关于联系人（或多个联系人）的信息与该页面共享。用户可以选择仅与页面共享特定字段。此外，用户可以选择仅提供符合页面请求条件的联系人，例如那些地址州字段值为"CA"的联系人。该API是只读API，因此目前无法添加新条目。通讯录API规范建议使用当前的行业格式（如vCard）来在用户的通讯录存储库中添加或更新联系人。由于该API提供对个人和机密信息的访问，浏览器代理在提供对通讯录API的访问权限之前，必须请求用户许可。

如果获得许可，页面上的JavaScript便可以使用`Contacts`接口开始查找联系人。`Contacts`接口有一个名为`find`的方法，该方法允许脚本查找一个或多个联系人，如下所示的`find`方法签名所示：

```
void find (DOMString[] fields, ContactFindCB successCB, optional ContactErrorCB errorCB, optional ContactFindOptions options);
```

`find`函数的参数在此解释：

- `DOMString[] Fields`：一个`DOMStrings`数组，表示要返回的联系人记录字段
- `successCB`：成功时启动的成功回调函数
- `errorCB`：失败时启动的可选回调函数
- `Options`：用于匹配联系人记录的搜索选项，例如名字

为防止在搜索联系人时阻塞页面，`find`方法在成功或失败时使用回调函数。如果存在匹配的联系人且有待返回的字段，则成功回调函数将启动，其结果变量包含一个结果数组。如果`find`方法执行时没有错误但未返回任何结果，则将向成功回调函数传递一个`null`值，表示未找到匹配的联系人记录。

返回的联系人记录是`Contacts`接口的一个实例，该接口包含多个属性以及其他联系人接口子类型（如`ContactName`、`ContactAddress`等），因为一个联系人实际上可能具有多个子组件（如多个地址）。表15.1显示了`Contacts`接口的属性。我们不会在这里描述所有子接口，但可以在W3C的通讯录API草案（www.w3.org/TR/contacts-api）中轻松查阅。

### 表15.1 通讯录接口属性

| 属性类型 | 属性 | 描述 |
| --- | --- | --- |
| DOMString | id | 联系人的唯一标识符 |
| DOMString | displayName | 联系人的显示名称 |
| ContactName | name | 联系人的全名 |
| DOMString | nickname | 联系人的昵称 |
| ContactField | phoneNumbers | 联系人的一项或多项电话号码（ContactField类型） |
| ContactField | emails | 联系人的一项或多项电子邮件地址（ContactField类型） |
| ContactAddress | addresses | 联系人的一项或多个地址（ContactAddress对象） |
| ContactField | ims | 一项或多项即时消息标识符（ContactField类型） |
| ContactOrganization | organizations | 联系人的一项或多个组织（ContactOrganization对象） |
| Date | birthday | 联系人的出生日期（Date对象） |
| DOMString | note | 联系人记录上的备注字段 |
| ContactField | photos | 联系人的一项或多项照片URL |
| [DOMString] | categories | 表示此联系人类别的DOMStrings数组 |
| ContactField | urls | 此联系人的一项或多个URL（ContactField类型） |

**注意**

目前，尚未知任何浏览器代理支持通讯录API。然而，预计浏览器代理将很快支持此API，甚至可能在本书出版之前。我们提供以下示例作为参考；它可能包含错误或与最终实际实现存在差异。

## 初学者示例：检索所有联系人和手机号码

尽管检索用户的所有联系人可能不被推荐，但有时这可能是适用的。本示例将使用通讯录接口的`find`方法以及成功和错误回调函数来检索所有联系人，检查联系人是否有手机号码，并在页面的`div`中显示联系人的姓名和手机号码。要创建此示例，请执行以下步骤，结果如代码清单15.1所示：

1. 创建一个空白HTML页面，包含一个`button`元素和用于显示结果的`div`。为按钮添加`click`处理程序以启动`findAllContacts`方法。
2. 在页面中添加`script`标签和`findAllContacts`方法，该方法启动通讯录请求。
3. 添加`contactsFindSuccess`回调函数和`contactsError`回调函数，分别处理通讯录请求的成功和失败事件。

### 代码清单15.1 检索和显示所有联系人的手机号码

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>15.1 检索所有联系人</title>
<script>
// 初始化页面功能
function init() {
  // 设置按钮处理程序
  var btnFindAll = document.getElementById('findAll');
  btnFindAll.addEventListener('click',findAllContacts,false);
}

// 查找联系人的成功回调函数
function contactsFindSuccess(contacts) {
  // 获取用于显示结果的div的引用
  var divResults = document.getElementById('divResults');
  // 遍历联系人结果
  for (var i in contacts) {
    // 对于每个联系人，遍历其所有电话号码
    for (var j in contacts[i].phoneNumbers) {
      // 检查电话号码是否为手机号码
      if (contacts[i].phoneNumbers[j].type === 'mobile') {
        // 显示联系人姓名和电话号码
        divResults.innerHTML += contacts[i].displayName + '(' +
            contacts[i].phoneNumbers[j].value + ')';
      }
    }
  }
}

// 查找联系人的错误回调函数
function contactsError(error) {
    // 适当地处理错误，此处仅显示错误码
    alert(error.code);
}

// 查找联系人的函数
function findAllContacts() {

    // 检查通讯录API是否可用
    if (navigator.contacts) {

        // 设置要检索的字段数组
        var arrFields = ['displayName', 'phoneNumbers'];

        // 在通讯录上调用find方法
        navigator.contacts.find(arrFields, contactsFindSuccess, contactsError);

    } else {

        // 告知用户此浏览器尚不支持通讯录API
        alert('此浏览器尚不支持通讯录API...');
    }
}

// 页面加载时初始化页面
window.addEventListener('load',init,false);
</script>
</head>
<body>
    <h1>检索所有具有手机号码的联系人</h1>
    <button id="findAll">查找所有联系人</button>
    <div id="divResults"></div>
</body>
</html>
```

## 初学者示例：检索所有联系人和手机号码

在此示例中，当用户单击“查找所有联系人”按钮时，将调用`findAllContacts`函数对`Contacts`接口发出请求。在`findAllContacts`函数中，代码首先检查`Contacts`接口是否可用。如果接口不可用，则会显示一个警报，但您可以根据解决方案的要求将其替换为其他逻辑。如果`Contacts`接口可用，则代码会创建一个字段数组，您希望通过通讯录`find`方法返回这些字段。然后，代码调用`find`方法，并提供字段数组、成功回调函数和错误回调函数。

通过`Contacts`接口检索到的`phoneNumbers`字段被构造为`ContactField`接口。`ContactField`接口由`type`、`value`和`pref`属性组成，如表15.2所示。

`type`属性是一个`DOMString`，对于`phoneNumbers`类型，`type`属性可以是`home`或`mobile`。`value`属性是实际的号码，`pref`属性是一个布尔值，用于指示该值是否为此联系人的首选值或主要值。当成功回调函数`contactsFindSuccess`被调用时，会传递一个结果集给该函数。这个结果集是一个联系人接口实例的数组，然后您可以对其进行遍历。在本例中，我们将结果变量命名为`contacts`。

在成功回调中，该示例首先在页面上创建对结果`div`的引用，以便您可以显示任何匹配的结果。接下来，函数遍历`contacts`数组。对于每个联系人，该示例遍历该联系人的`phoneNumbers`。对于每个电话号码，代码检查`type`以查看该电话号码是否为手机号码。如果是手机号码，则代码在结果`div`中显示姓名和电话号码。



本示例中使用的通讯录`find`方法请求所有联系人，并提供了成功和错误回调函数。`find`方法可以接受第四个可选参数，其类型为`ContactFindOptions`。根据通讯录API规范，此接口的具体实现由各浏览器代理决定。然而，此接口的基础是创建一个基于请求的联系人字段进行匹配的过滤器。这是一个简单的过滤方法，它将匹配请求字段中的任何一个，并且匹配值中的任何位置。例如，如果提供过滤值"son"并检索了`displayName`和`emails`字段，那么任何其字符串中包含"son"的联系人……（文本在此截断）

### 表15.2 ContactField接口属性

| 属性类型 | 属性 | 描述 |
|---|---|---|
| DOMString | type | 此值的分类 |
| DOMString | value | 字段的实际值 |
| Boolean | pref | 一个标志，表示此字段是主要或首选值 |

## 消息传递 API

消息传递 API 旨在允许页面使用`sms`、`mms`和`mailto` URI 方案向特定地址发送消息。该 API 非常简单，因为它只有一个接口和一个方法：`device`和`sendMessage`。`device`接口预计是`navigator`接口的一部分，因此要检查是否支持消息传递 API，您可以使用以下代码：

```javascript
if (navigator.device.sendMessage) {
    ... your sendMessage code here ...
}
```

如果浏览器代理支持消息传递 API，那么您可以使用`sendMessage`方法向给定的收件人发送消息。`sendMessage`方法的结构如下所示：

```javascript
void sendMessage (DOMString to [,Blob attachments] [, messagingErrorCB]);
```

`to`参数接受一个与`sms`、`mms`或`mailto`方案匹配的 URI 方案，并且可以接受包含`body`元素等的查询字符串。`attachments`字段可以是图片或视频，最后一个参数是可选的错误处理程序。因此，要通过 SMS 发送一条基本消息，您可能会像下面这样调用`sendMessage`：

```javascript
navigator.device.sendMessage('sms:+17705551212?body=Hi%20Tom');
```

如果添加了错误回调函数（这是推荐的，否则您将不知道`sendMessage`失败了），那么一个错误对象将被传递给处理程序，其中包含一个错误代码。表 15.3 提供了可能的错误代码列表。

尽管消息传递 API 是一个简短的规范，但其影响是非同凡响的。现在，客户端页面将能够通过设备上的浏览器直接发送短信、视频和图片，以及通过 MMS 消息和电子邮件发送。

> **注意**
>
> 联系人 API 被纯粹设计为设备上联系人数据的只读服务。要在设备上的数据存储中执行联系人的添加和更新，您需要将联系人信息放入联系人应用程序的标准格式（如基于文本的 vCard），然后通过`href`元素引用此卡文本，以便用户可以将该卡片下载到其联系人应用程序中。

任何一组字段中的匹配项，例如 "sonny@....com" 或 "Chuck Hudson。" 此示例的预期语句如下：

```javascript
{filter: 'son'}
```

在浏览器代理实际实现带有过滤功能的联系人 API 之前，我们只能猜测我们将对过滤器拥有多大的控制权，但似乎该过滤器将至少提供对设备上联系人的一些基本筛选。

**表 15.3 消息传递 API 错误代码值**

| 值 | 常量项 | 描述 |
| :--- | :--- | :--- |
| 0 | `UNKNOWN_ERROR` | 发生未知错误。 |
| 1 | `INVALID_ARGUMENT_ERROR` | `sendMessage`方法传递了无效参数。 |
| 3 | `TIMEOUT_ERROR` | 发送消息的请求超时。 |
| 4 | `PENDING_OPERATION_ERROR` | 浏览器已在等待回调。 |
| 5 | `IO_ERROR` | 发生通信错误。 |
| 6 | `NOT_SUPPORTED_ERROR` | 不支持`sendMessage`方法。 |
| 20 | `PERMISSION_DENIED_ERROR` | 用户或浏览器未授权方法调用。 |
| 30 | `MESSAGE_SIZE_EXCEEDED` | 此消息类型的消息方案限制已超出。 |

> **提示**
>
> 预计浏览器代理中的`sendMessage`方法将实现以支持 URI 功能，以便启用诸如多个收件人等功能。如果情况如此，那么只需用逗号分隔号码，例如 "sms:+17705551212,+18025551212...."，就可以轻松地向多个 SMS 收件人发送消息。

## 网络信息 API

确定浏览器的连接速度对于节流数据和功能以获得更好的用户体验非常重要。网络信息 API 旨在暴露一个简单的`type`属性，该属性将指示设备当前具有的连接类型。基于此值，页面可以改变其行为以适应可用数据管道的大小和速度。连接类型的值可以是以下之一：`unknown`、`ethernet`、`wifi`、`2g`、`3g`、`4g`和`none`。提供了一个名为`Connection`的新接口，它有一个关联的属性：`type`。因此，要检索当前连接类型，您将使用以下代码：

```javascript
var connectionType = navigator.connection.type;
```

了解连接类型后，您可以在完整版本和轻量版本的样式表之间动态切换，或者在连接速度较慢时更改页面上的逻辑以仅检索部分结果。

除了`Connection`接口，还有两个新事件：`online`和`offline`。这些事件与`window`对象相关联，可以在`online`触发时用于检查连接类型的变化，或在设备离线时进行处理。

> **提示**
>
> 当用户更改连接类型时，`online`事件可能会被多次触发。您的代码应尽可能精简，以最小化在此事件上运行的功能，因为该事件可能会由于快速连接类型切换而重复发送。

## 电池状态事件

电池状态事件允许您捕获与设备电池状态相关的事件。在电池状态事件规范中，有两种可能触发事件的状态变化。第一种状态变化在设备插入电源或从电源拔出时触发。第二种事件表示电池电量变化达到 1% 或更多。在任何一种情况下，都会触发电池状态事件。然后该事件将具有可用的属性：`isPlugged`，这是一个布尔值，以及`level`，这是一个浮点数，范围从 0 到 100，其中 100 表示电池已充满电。如果`level`为`null`，则浏览器无法报告电池电量。

要注册处理电池状态事件，可以使用`onbatterystatus`属性和`batterystatus`事件。以下任一示例都是有效的：

```javascript
window.addEventListener('batterystatus', function (event) {
    alert(event.level);
});

window.onbatterystatus = function (event) {
    alert(event.level);
};
```

在任何一种情况下，当前电池电量都将提醒用户。如果您想在插入状态更改时提醒用户，那么您可以使用`event.isPlugged`来检索设备是否已插入电源的布尔值。

> **注意**
>
> 如果浏览器无法确定当前电池电量（在 0 到 100 之间，包括 0 和 100），则`level`属性将被赋予`null`值。

## HTML 媒体捕获

HTML 媒体捕获旨在指示浏览器代理基于文件输入元素的新参数和属性启动媒体捕获工具。通过提供有关文件输入应接受的信息类型以及使用什么来“捕获”输入的建议，浏览器代理可以启动适当的设备捕获机制。捕获可以采取视频、音频或图片的形式，因为它们都是媒体形式，通常在具有摄像头和麦克风的设备（如智能手机、平板电脑和笔记本电脑）上可用。

通常，文件输入元素打开文件浏览窗口以选择要提交的适当文件。HTML 媒体捕获使用文件输入的`accept`属性来推荐合适的文件选择器，例如用于接收图像的摄像头。以下是三种不同的`accept`属性值：

- `image/*`：用于从摄像头或用户的图像库中接收图像
- `audio/*`：用于通过设备麦克风录制来接收音频输入
- `video/*`：用于接收通过设备摄像头和麦克风录制的视频文件

可以添加一个额外的属性来建议浏览器应使用什么方法来捕获输入。`capture`属性可以采用四个值之一：`camera`、`camcorder`、`microphone`或`filesystem`。如果未提供`capture`属性，则默认值为`filesystem`。因此，一个用于从麦克风捕获音频的示例文件输入元素如下：

```html
<input type="file" accept="audio/*" capture="microphone">
```

通过`accept`和`capture`属性，您将能够以一些有趣的方式使用设备麦克风和摄像头。已经有一些团队正在努力使用 HTML 媒体捕获和其他 HTML5 技术（如 WebSocket）来实现设备之间的全双工音频/视频通话流。

## 中级配方：使用文件输入捕获图片

在此配方中，您将使用文件输入元素上的`accept`和`capture`属性来让浏览器启动设备内置的摄像头图片捕获屏幕，让用户拍摄照片，然后将照片返回到页面。照片文件返回到页面后，HTML 媒体捕获将获取该文件并将其加载到一个新的图像元素中，该元素被缩放为缩略图并添加到页面。要创建清单 15.2 中的代码，请按照以下步骤操作：

1. 创建一个空白 HTML 页面，其中包含文件输入元素和缩略图 div。
2. 在页面中添加`script`标签和`handleCapture`函数，该函数处理通过文件输入的`onChange`方法传递的文件。

## 400 第15章 集成设备数据

> **注意**
>
> 在撰写本文时，此示例可在支持 HTML Media Capture 的 Android 3.0 及更新版本的设备上运行。因此，本章的截图来自一台 Android 平板电脑。

### 清单 15.2 捕获摄像头图像

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>15.2 HTML Media Capture</title>
<script>
// Function to handle the HTML media capture of a file
function handleCapture(files) {

    // Set the image matching pattern
    var imageType = /image.*/;

    // We expect only one picture at a time but loop through any files provided
    for (var i = 0; i < files.length; i++) {

        // Retrieve the file from those passed in
        var file = files[i];

        // Check if the file is an image type
        if (file.type.match(imageType)) {

            // Create our new image element
            var newImg = document.createElement("img");
            newImg.classList.add("obj");
            newImg.file = file;
            newImg.style.maxHeight = "100px";
            newImg.style.maxWidth = "100px";

            // Append the new image element to the thumbnails area
            var thumbnails = document.getElementById('thumbnails');
            preview.appendChild(newImg);

            // Load the image element with the contents of the file
            var reader = new FileReader();
            reader.onload = (function(aImg) {
                return function(e) { aImg.src = e.target.result; };
            })(newImg);
            reader.readAsDataURL(file);
        }
    }
}
</script>
</head>
<body>
  <h2>Media Capture - Camera</h2>
  <input type="file" accept="image/*;capture=camera"
    capture="camera"
    onChange="handleCapture(this.files)"></input>
  <div id="thumbnails"></div>
</body>
</html>
```

当页面在浏览器中加载时，会提供常规的“选择文件”提示，如图 15.1 所示。

当用户点击“选择文件”时，浏览器会通过`accept`和`capture`属性被告知启动摄像头选择器，本例中将启动 Android 的拍照界面，如图 15.2 所示。

一旦拍摄了照片，图片文件会发送到页面，并以文件作为参数调用`handleCapture`函数。在`handleCapture`函数中，你首先检查文件以验证其是否为图像类型，然后创建一个新的图像元素，将其添加到页面并使用该文件加载。在图 15.3 中，“选择文件”按钮已被点击数次，所拍摄的图片已作为缩略图添加到 div 中供查看。

![](img/de30ea99ecac39b49e690a84c48f43b9_431_0.png)

## 第15章 集成设备数据

![](img/de30ea99ecac39b49e690a84c48f43b9_432_0.png)

图 15.2 设备调出默认的摄像头屏幕以捕获图像。

![](img/de30ea99ecac39b49e690a84c48f43b9_432_1.png)

图 15.3 拍照后，用户会自动返回到网页应用，并显示缩略图。

## 设备方向和运动事件

设备方向和运动事件最初是设备 API 工作组的一个规范，但后来被移至地理定位工作组，因此在当前的设备 API 工作组列表中看不到它。我们将其保留在本章中，因为它专门聚焦于与用户当前可能正在使用的设备内置陀螺仪的集成。许多手机、平板电脑甚至计算机都内置了这种硬件陀螺仪，而 Chrome 等浏览器代理也已将这些事件实现到其 JavaScript 引擎中。

W3C 组织的设备方向规范指定了三个新事件，如下所列：

- `deviceorientation`：提供以 alpha、beta、gamma 格式表示的方向，显示设备的空间定位
- `compassneedscalibration`：由浏览器代理触发的事件，表明设备的指南针需要校准
- `devicemotion`：提供加速度、包含重力的加速度、旋转速率以及用于设备移动的间隔时间

设备方向中的所有三个事件都在`window`对象上触发，并且像`window`对象上的任何正常事件一样进行注册。`deviceorientation`事件通过传递给你的处理程序的事件数据提供四个可读属性：`alpha`、`beta`、`gamma`和`absolute`。`alpha`、`beta`和`gamma`属性对应于设备的方向，例如设备的倾斜或旋转。`alpha`属性表示旋转，而`beta`和`gamma`对应于向左/右倾斜和向前/向后倾斜。例如，放在桌子上的笔记本电脑的`beta`为 0，`gamma`为 0，而`alpha`将有一个代表其方向的值。对于笔记本电脑，方向是基于键盘的，而不是屏幕，而手机的方向则是手机本身。`absolute`属性表示浏览器是否能够提供方向角的绝对值。如果设备不能绝对地设置该值，则此值将为 false。在我们的大多数测试中，该值确实为 false，尽管`beta`和`gamma`角是绝对的，而`alpha`在页面执行时被任意设置为 0。

`compassneedscalibration`事件是一个简单的事件，它通知窗口设备的内部指南针需要校准。根据规范，该事件可以被网站或应用程序取消，并且默认的设备校准用户界面可以由 Web 应用程序提供的自定义校准所取代。然而，关于此事件的细节仍有待确定。



`devicemotion`事件是一个更复杂的事件，因为它包含用于加速度、旋转和间隔的属性。`acceleration`属性是新接口`DeviceAcceleration`的一个实例，该接口以`double`数据类型格式提供`x`、`y`、`z`加速度属性，以显示X、Y、Z方向的加速度。旋转速率也是一个接口实例，但是`DeviceRotationRate`的实例，它以`alpha`、`beta`、`gamma`的格式提供旋转。`devicemotion`事件的所有属性在规范中都显示为可选属性。表15.4更详细地展示了`devicemotion`事件的属性。

### 表15.4 devicemotion事件属性值

| 属性 | 类型 | 描述 |
| :--- | :--- | :--- |
| `acceleration` | `DeviceAcceleration` | 以X、Y、Z值表示的设备加速度。 |
| `accelerationIncludingGravity` | `DeviceAcceleration` | 包含重力影响的设备加速度，以X、Y、Z值表示。 |
| `rotationRate` | `DeviceRotationRate` | 通过`alpha`、`beta`和`gamma`角显示的设备旋转。 |
| `interval` | `double` | 采集加速度和旋转数据的间隔（以毫秒为单位）。预期这是一个常量。 |

## 中级食谱：创建一个气泡水平仪

如果你有机会参与移动设备编程领域，你很可能会看到大多数移动平台上都可用的气泡水平仪原生应用程序，用于显示设备的方向。`deviceorientation`事件可以通过查看`beta`和`gamma`事件字段，在客户端JavaScript中提供相同类型的功能。（你不需要`alpha`字段，因为气泡水平仪不使用设备的旋转。）在本食谱中，你将使用分层的`canvas`元素来构建一个复合气泡水平仪，并显示`beta`和`gamma`值，如图15.4所示。

你可以改进定位算法以添加诸如将气泡限制在圆形内等功能，但本食谱将展示处理设备方向数据的基础知识。要创建此气泡水平仪，请使用清单15.3并执行以下步骤：

1. 创建一个空白HTML页面，包含构成气泡水平仪的三个`canvas`元素，并添加用于显示`beta`和`gamma`值的`span`。
2. 添加用于设置`canvas`元素样式的`style`部分。

## 第15章 集成设备数据

### 清单15.3 使用Beta和Gamma值创建气泡水平仪

![](img/de30ea99ecac39b49e690a84c48f43b9_435_0.png)

图15.4 在笔记本电脑上倾斜时，显示气泡水平仪画布层和beta/gamma值的示例输出

3. 添加`init`函数，该函数包含在`script`标签内定义的`deviceorientation`事件处理器。
4. 使用`window.addEventListener`添加页面加载时启动`init`函数的代码。

> 注意
>
> 此配方要求你的浏览器支持`canvas`元素，并且你启动此页面的设备需要具有内部陀螺仪以提供`beta`和`gamma`值。

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>15.3 Bubble Level</title>
<style>
#canvas {
    height:100px;
    width:100px;
}
</style>
<script>

// canvas and context reference variables for drawing
var cvsBackground;
var ctxBackground;
var cvsBubble;
var ctxBubble;
var cvsCircle;
var ctxCircle;

// Variable holders for the beta and gamma values
var tempBeta = 0;
var tempGamma = 0;

// The canvas location and center variables
var canvasX;
var canvasY;
var canvasXCenter;
var canvasYCenter;

// Initialize the canvas object references and orientation event handler
function init() {

  // Grab references to the canvas objects and their contexts
  cvsBackground = document.getElementById('background');
  ctxBackground = cvsBackground.getContext('2d');
  cvsBubble = document.getElementById('bubble');
  ctxBubble = cvsBubble.getContext('2d');
  cvsCircle = document.getElementById('circle');
  ctxCircle = cvsCircle.getContext('2d');

  // Set the canvas coordinates and center coordinates
  canvasX = parseInt(cvsBackground.offsetLeft);
  canvasY = parseInt(cvsBackground.offsetTop);
  canvasXCenter = parseInt(cvsBackground.width/2);
  canvasYCenter = parseInt(cvsBackground.height/2);

  // Draw the bubble level background
  ctxBackground.fillStyle='#0c0';
  ctxBackground.beginPath();
  ctxBackground.arc(canvasXCenter,canvasYCenter,50,0,Math.PI*2,true);
  ctxBackground.closePath();
  ctxBackground.fill();

  // Draw the bubble
  ctxBubble.fillStyle='#0FF';
  ctxBubble.beginPath();
  ctxBubble.arc(canvasXCenter,canvasYCenter,10,0,Math.PI*2,true);
  ctxBubble.closePath();
  ctxBubble.fill();

  // Draw the center circle to designate level
  ctxCircle.strokeStyle='#fff';
  ctxCircle.lineWidth='5';
  ctxCircle.beginPath();
  ctxCircle.arc(canvasXCenter,canvasYCenter,20,0,Math.PI*2,true);
  ctxCircle.closePath();
  ctxCircle.stroke();

  // Add the listener for deviceorientation events
  window.addEventListener('deviceorientation', function(event) {

    // Check if the beta or gamma have changed
    if (parseInt(event.beta)!=tempBeta||parseInt(event.gamma)!=tempGamma) {

        // Set our beta and gamma variables
        tempBeta = parseInt(event.beta);
        tempGamma = parseInt(event.gamma);

        // Set the adjustment variables
        var adjX = 0;
        var adjY = 0;
        var adjFactor = 3;   // Scaling factor for bubble movement
        var adjMax = 40;     // Maximum adjustment for bubble

        // Determine the new position of the bubble
        if (tempBeta*adjFactor > adjMax) {
            adjY = -adjMax;
        } else if (tempBeta*adjFactor < -adjMax) {
            adjY = adjMax;
        } else {
            adjY = tempBeta*adjFactor * -1;
        }
        if (tempGamma*adjFactor > adjMax) {
            adjX = -adjMax;
        } else if (tempGamma*adjFactor < -adjMax) {
            adjX = adjMax;
        } else {
            adjX = tempGamma*adjFactor * -1;
        }

        // Move the bubble to the new position
        cvsBubble.style.left = canvasX+adjX+'px';
        cvsBubble.style.top = canvasY+adjY+'px';

        // Set our span values for displaying the beta and gamma
        var spanBeta = document.getElementById('betaValue');
        var spanGamma = document.getElementById('gammaValue');
        spanBeta.innerHTML = tempBeta;
        spanGamma.innerHTML = tempGamma;

    }
}, true);
}

// call the init function on page load
window.addEventListener('load',init,false);
</script>
</head>
<body>
  <h1>Chapter 15 Bubble Level</h1>
  <!-- The canvas elements are layered as defined below -->
  <canvas id="background" style="position:absolute; left:100px; top:150px;">
    The bubble level background.
  </canvas>
  <canvas id="bubble" style="position:absolute; left:100px; top:150px;">
    The bubble which moves to show the level.
  </canvas>
  <canvas id="circle" style="position:absolute; left:100px; top:150px;">
    The overlaid circles to show the center of the level.
  </canvas>
  <br>
  Beta Value: <span id="betaValue"></span><br>
  Gamma Value: <span id="gammaValue"></span>
</body>
</html>
```

当页面在浏览器中加载并调用`init`函数时，脚本将首先创建气泡水平仪的各个组件。气泡水平仪由三个`canvas`元素组成：背景、气泡和前景中心环。将气泡水平仪拆分为这三个组件有两个目的。首先，这使得气泡可以分层显示在背景之上、中心环之下，看起来像一个真实的气泡水平仪。其次，这允许你以编程方式移动气泡，而无需在每次移动时重绘元素。

绘制完气泡水平仪组件后，脚本为`deviceorientation`事件设置事件处理器。事件处理函数的设计是首先检查`beta`和`gamma`值是否发生了任何变化，如果有变化，则将临时保存变量设置为新值。接下来，该函数设置一些位置调整变量，这些变量用于计算气泡画布的位置。`adjFactor`变量用于随着气泡远离中心而“加速”其移动，而`adjMax`变量是气泡可以移动的最大距离。计算出气泡画布的新`top`和`left`坐标后，你移动画布并显示更新后的`beta`和`gamma`角度。请注意，在处理`beta`和`gamma`角度时，你只使用事件提供的双精度值的整数部分。在我们的测试中，提供的角度粒度非常细，因此为了防止在角度发生最微小的变化时就移动画布；我们选择只在整个度数发生变化时才移动画布。

## 总结

在本章中，你了解了一些新的和即将推出的API和事件规范，这些规范正在被创建以提供对所有类型设备信息和功能的访问。这些规范完成、发布并在各种浏览器平台中可用只是时间问题。Web应用程序最终将拥有许多原生设备应用程序提供的集成功能。设备API周围仍有几个规范需要完成，但这些努力显示了HTML5在其功能方面持续增长。

此页有意留白

www.it-ebooks.info

## 配方

### 初级配方

- 构建HTML5入门文档 2
- 使用`header`元素创建网站页眉 5
- 使用`hgroup`元素对标题进行分组 7
- 使用`nav`元素创建导航 8
- 使用`aside`元素创建侧边栏 15
- 使用`footer`元素 17
- 使用`figure`和`figcaption`元素标记图表和标题 31
- 使用`time`元素标记日期和时间 34
- 使用`details`元素制作原生切换小部件 35
- 使用`address`元素提供联系信息 37
- 使用`mark`元素突出显示文本 38
- 使用`s`元素显示不准确或无关的内容 39
- 将链接包裹在元素周围 47
- 处理Internet Explorer 55
- 测试HTML5功能 57
- 使用`@font-face`使用自定义字体 77
- 创建一个表单来收集联系信息 97
- 使用`input type="search"`创建搜索表单 101
- 创建日历和时间控件 102
- 创建数字选择器 105
- 创建滑块（无需JavaScript） 106
- 创建颜色选择器 107
- 使用`output`元素显示结果 108
- 使用表单占位符文本 109

www.it-ebooks.info

# 412 个实用技巧

- 使用`list`和`datalist`创建自动完成功能 110
- 使用`progress`元素跟踪任务完成情况 111
- 使用`meter`元素进行度量 112
- 页面加载时跳转到表单元素 114
- 允许多项输入 115
- 使用`required`属性进行基本验证 116
- 限制用户输入 118
- 在画布上绘制网格 130
- 绘制简单形状和线条 134
- 添加文本 144
- 绘制图像 145
- 使用`video`元素嵌入视频 163
- 使用`audio`元素嵌入音频 187
- 使用`pushState`添加历史记录 208
- 创建图片查看器 211
- 使用`replaceState`修改历史记录 216
- 使用简单的`getCurrentPosition`确定位置 233
- 获取和设置会话存储 263
- 根据会话存储设置样式 266
- 通过Web Sockets进行通信 299
- 创建Web Worker 304
- 跨`div`拖放元素 321
- 创建Manifest文件 335
- 离线使用网页 337
- 显示简单通知 344
- 获取文件属性 360
- 通过拖放处理多个文件 362
- 检索所有联系人和手机号码 393

## 中级技巧

- 使用新的`article`元素 11
- 使用`section`元素对内容进行分组 12
- 使用HTML5大纲工具确保正确的结构 19
- 使用微数据添加语义信息 47
- 在HTML5中使用WAI-ARIA 49
- 利用jQuery替换日历组件 59
- 使用Modernizr检测功能 62
- 使用CSS3媒体查询创建响应式设计 69
- 使用CSS渐变和多重背景制作按钮 80
- 使用变换和过渡增强网站 84
- 编写自定义验证规则 117
- 自定义和美化表单 119
- 使用路径绘制多边形 139
- 绘制圆弧和圆形 143
- 裁剪图像 146
- 制作精灵图动画 147
- 为所有浏览器启用视频 166
- 创建带字幕和说明文字的视频 173
- 为所有浏览器启用音频 188
- 创建节拍混音器 193
- 在图片查看器中弹出状态 214
- 修改页面历史记录 218
- 测试历史记录安全性 225
- 使用`getCurrentPosition`在地图上标记位置 237



# 使用 PositionOptions 确定距离 243

# 使用本地存储保存表单数据 271

# 添加双向通信 308

# 通过 readAsDataURL 预览图像 368

# 使用文件输入捕获图片 399

# 创建气泡水平仪 404

## 高级技巧

- 使用所有新元素构建新闻页面 21
- 使用所有新元素构建搜索结果页面 25
- 使用评论功能标记文章页面 51
- 使用 CSS 创建动画 89
- 综合运用创建注册表单 121
- 制作图像动画 151
- 制作垂直柱状图动画 155
- 创建自定义控件 178
- 添加流式广播电台 197
- 使用高级状态数据对象跨页面传递信息 221
- 使用 `watchPosition` 跟踪移动位置 250
- 捕获本地存储事件 275
- 使用 Web 数据库实现购物清单 286
- 利用共享 Web Worker 311
- 利用事件和 `dataTransfer` 325
- 创建推文通知页面 348
- 使用 `readAsText` 解析 CSV 文件 373
- 创建本地文件 382

# 索引

## A

- `abbr` 元素，46
- `abort` 函数，`FileReader`，373、376、378、380
- `ABORT_ERR`，`FileReader`，373、378
- `accept` 属性，HTML Media Capture，399–402
- 无障碍访问
  - 使用 ARIA 改善，49–51
  - 结合 `nav` 元素进行导航，10
  - 占位符文本，109
  - 为视频添加字幕和说明文字，173–176
- 首字母缩略词，46
- `:active` 状态，CSS3 过渡，86
- `addEventListener` 函数
  - 为设备方向创建气泡水平仪，405、407–408
  - 创建 web worker，304–306
  - 自定义视频控件，181–183、185
  - 数据库存储，287–288、293
  - 显示简单通知，344–345
  - 利用事件和 `dataTransfer`，326–328
  - 利用共享 web worker，313–314
  - 使用 `readAsText` 解析 CSV 文件，374、378
  - 通过拖放处理多个文件，363、365
  - 使用本地存储保存表单，272–273
- `addGroceryItem` 函数，数据库存储，288、292–293
- `addNote` 函数，本地存储，276–278、281
- `address` 元素，联系人，37–38
- Adobe Photoshop，基于坐标的绘图系统，129
- 高级技巧，413–414，xxviii
- 警报。请参阅 Notification API
- 替换文本
  - 鼠标悬停时显示，89
  - 用于标记图形和标题，32
  - 用于海报图像，171
- `and` 语法，CSS3 媒体查询，71
- Android
  - 浏览器支持。*请参阅* 浏览器支持
  - 通过媒体查询进行定向，76
- `animateSprite` 函数，147–149
- 动画
  - CSS3 动画，86、89–94
  - 图像动画，151–155
  - 精灵图动画，147–150
  - 垂直柱状图动画，155–161
- `antiClockwise` 值，圆弧，143
- API 类型
  - 应用缓存，340–341
  - 音频媒体，192–193
  - 联系人，391–396
  - 拖放，319–325
  - 文件。*请参阅* File API
  - 地理定位。*请参阅* Geolocation API
  - Google 地图。*请参阅* Google Maps API V3 服务
  - History，207
  - 设备历史记录，389–391
  - HTML Media Capture，398–402
  - IndexedDB API，260、283–286
  - 消息传递，396–397
  - 网络信息，397–398
  - 通知，341–343
  - 视频媒体，177
  - Web Workers。*请参阅* Web Workers API
  - WebSocket，297–302
- `.appcache` 文件，335
- 应用缓存
  - API，340–341
  - 创建 manifest 文件，335–337
  - 概述，334–335
  - 离线使用网页，337–340
- `arc` 方法
  - 在 canvas 中绘制圆弧和圆形，143
  - 在画布上绘制网格，130–133
- 弧形工具，134
- `aria-required:"true"`，116
- ARIA (Web Accessibility Initiative Accessible Rich Internet Applications)，49–51
- `article` 元素
  - 用于文档大纲，21
  - 使用评论功能标记文章页面，53
  - 用于新闻主页，23–25
  - 在其中放置页脚元素，17–18
  - 用于搜索结果页面，27–29
  - 在 `section` 内使用，12
  - 与 `section` 元素的比较，14–15
  - 使用，11–12
- 带评论的文章页面，51–54
- `aside` 元素
  - 用于文档大纲，21
  - 用于新闻主页，23–25
  - 用于搜索结果页面，28–29
  - 用于侧边栏，15–17
- 关联列表，43–44
- 异步命令，Web SQL Database API，284
- `@font-face`，CSS3，77–78
- 属性选择器，CSS3，72
- 属性
  - 音频，190–192
  - `canvas` 元素，128
  - `ContactField` 接口，395
  - `Contacts` 接口，391–392
  - `DataTransfer` 接口，320
  - `DeviceAcceleration` 接口，404
  - `devicemotion` 事件，403–404
  - `deviceorientation` 事件，403
  - 获取文件属性，360–362
  - HTML Media Capture，399
  - 微数据，48
  - `FileReader` 的 `onprogress` 事件，374
- `audio` 属性，`video` 元素，171
- `audio` 元素
  - 添加流式音频，198–206
  - 创建节拍混音器，193–197
  - 为所有浏览器启用音频，188–190
  - 使用 `audio` 元素嵌入音频，187–188
  - 新属性，190–192
- 音频，使用 HTML5 嵌入
  - 创建节拍混音器，193–197
  - 为所有浏览器启用音频，188–190
  - 测试用的免费音频文件，192
  - 媒体 API，192–193
  - 新属性，190–192
  - 流式广播电台，197–206
  - 使用 `audio` 元素，187–188
- 作者信息
  - `cite` 元素不用于此目的，39–40
  - 在页脚中，6、17
  - 在页头中，6
  - 使用 `b` 元素表示，40
- 授权，位置隐私和，237
- 自动完成，使用 `list` 和 `datalist` 创建，110–111
- `autofocus` 属性，114–115
- `autoplay` 属性
  - `audio` 元素，191
  - `video` 元素，172
- 电池，移动设备，257
- Battery Status 事件，398
- 节拍混音器，193–197
- 初级技巧，411–412，xxviii
- `beginPath` 方法，canvas 线条，139、142
- `bezierCurveTo`，绘制曲线，143
- `BlobBuilder` 接口，381
- 块级处理器，利用事件，326–328、330
- `blockquote` 和 `cite` 元素，40
- 博客条目，11–12
- 模板代码，57
- 边框
  - 添加到 canvas，128
  - 绘制 canvas 网格，131、133
- HTML5 浏览器体验
  - 应用缓存，334–335
  - 应用缓存 API，340–341
  - 创建 manifest 文件，335–337
  - 创建推文通知页面，347–356
  - 显示简单通知，344–347
  - 拖放 API，319–321
  - 跨 `div` 拖放元素，321–325
  - 利用事件和 `dataTransfer`，325–333
  - 通知 API，341–343
  - 概述，319
  - 离线使用网页，337–340
- 浏览器处理
  - 模板代码，57
  - 自定义视频控件，184
  - 处理 Internet Explorer，55–57
  - 使用 Modernizr 检测功能，62–66
  - HTML 历史，xxiii
  - 概述，55

### 浏览器处理（续）

- polyfilling，66–67
- HTML5 的原则，xxv
- 使用 jQuery 替换日历组件，59–62
- 测试 HTML5 特性，57–59
- 实用的 HTML5 验证网站，67

### 浏览器历史

- 使用 `pushState` 添加到历史记录，208–211
- 基础知识，207–208
- 浏览器兼容性，208
- 更改页面历史记录，218–220
- 使用 `replaceState` 创建历史记录，216–218
- 创建图像查看器，211–214
- 有用的库，228
- 在图像查看器中使用 `popstate`，214–216
- 安全性测试，225–228
- 使用高级状态数据对象，221–225

### 浏览器支持

- application cache，334
- audio codecs，188
- `autofocus` attribute，114
- 日历组件，102
- canvas，128
- 客户端存储，261
- 颜色选择器，107
- CSS 动画，90
- CSS 变换与过渡，84
- CSS3 `@font-face`，77
- CSS3 渐变，80
- CSS3 Media Queries，70
- `datalist` 元素，110–111
- 拖放 API，321
- `email` 输入类型，98
- 启用音频，188–190
- 启用视频，166–173
- File API，360
- `formnovalidate`/`novalidate` 属性，119
- Geolocation API，232
- History API，208
- HTML5 和视频编解码器，165
- `meter` 元素，113
- `min` 和 `max` 属性，118
- `multiple` 属性，115
- Notification API，343
- 数字选择器，105
- `output` 元素，108
- `pattern` 属性，117
- `placeholder` 属性，110
- `progress` 元素，112
- beat mixer 中的怪异行为，197
- `required` 属性，116
- `search` 输入类型，101
- 滑块控件，106
- `step` 属性，118
- `tel` 输入类型，99
- `url` 输入类型，100
- `video` 元素，164
- Web SQL Database，283
- Web Workers API，303
- WebSocket API，298

### 创建气泡水平仪，404–408

## C

#### 缓存

- application. *参见* Application cache
- 通过 manifest 文件更新，337

#### CACHE 部分，manifest 文件，336

#### `cached` 事件，application cache API，341

#### `calculateDistance` 函数，`PositionOptions`，244–246

## 日历组件

- 利用 jQuery 进行替换，59–62
- 时间控件，102–105

## 客户端存储

- 回调函数，tweet 通知，348–349，353，356

## 相机，使用 file input 捕获图片，399–402

## `cancel` 方法，notifications，348，352

## canvas

- 添加文本，144
- 动画图像，151–155
- 动画精灵图，147–150
- 动画垂直条形图，155–161
- 为形状应用渐变，137
- 创建气泡水平仪，404–408
- 裁剪图像，146–147
- 绘制和设置矩形或正方形样式，135–137
- 绘制弧线和圆形，143
- 绘制图像，145–146
- 绘制线条和路径，138–139
- 使用路径绘制多边形，139–142
- 在 canvas 上绘制网格，130–134
- canvas 概述，127–128
- 设置 `canvas` 元素，128–129
- 测试浏览器对 HTML5 特性的支持，58–59
- 工具，134
- 变换工具，150–151
- X 和 Y 坐标，129

## 字幕

- 创建视频字幕，173–176
- `figcaption` 关联图像，31–34

## `capture` 属性，HTML Media Capture，399–402

## 层叠样式表. *参见* CSS (Cascading Style Sheets)

## 分类，食谱，xxviii

## `changeField` 函数，本地存储，272–274

## `changeNote` 函数，本地存储，276，278，280

## `chapters` 值，`kind` 属性，173

## 字符编码，2–3

## `charset` 声明，2–3

## `checking` 事件，application cache API，340–341

## `checkPermission` 方法，tweet 通知，349–351，353，355

## `checkPermissionLevel` 函数，tweet 通知，349–353，355

## `checkStorage` 函数，本地存储，272–274

## Chrome

- 浏览器支持. *参见* Browser support
- HTML5 Outliner 扩展程序图标，19–21

## Chrome 开发者工具

- 使用本地存储存储表单，272，274
- 查看 SQLite 数据库，287
- 查看存储，265–266

## 圆形，在 canvas 中绘制，143

## `cite` 元素，更改，39–40

## `clearAllNotes` 函数，本地存储，276，279–281

## `clearFile` 函数，预览图像，368，370–372

## `clearRect` 方法

- 清除 canvas，142，154
- 矩形，136

## `clearTable` 函数，拖放，363–366

## `clearWatch` 函数，`watchPosition`，251，255–256

## 客户端存储

- 在本地存储中捕获事件，275–283
- 使用 Chrome 开发者工具查看，265–266
- 数据安全，260–261
- 在浏览器中禁用，262
- 获取和设置 `sessionStorage`，263–264
- 概述，259–260
- session storage 和 local storage，261–262
- 使用本地存储存储表单，271–275
- 使用 session storage 设置样式，266–271
- 类型，259
- 使用 web database 创建杂货清单，286–295
- Web SQL Database API，283–286

#### 通过 Web Workers API 实现线程处理，302–304

#### WebSocket API 概述，297–298

## `compassneedscalibration` 事件，设备方向，403

## 兼容性. *参见* Browser support

## 合成，canvas 工具，135

## `computeDistanceBetween` 函数

- `PositionOptions`，244
- `watchPosition`，252–253，256

## 并发，303

## `connect` 事件，共享 web worker，312

## `Connection` 接口，Network Information API，397

## 联系信息

- 使用 `address` 元素，37–38
- 创建表单以收集，97–101

## `ContactField` 接口，392，395

## Contacts API

- 开发，390
- 概述，391–392



- 检索所有联系人和手机号码，393–396

## `Contacts`接口，391–392

## `contactsFindSuccess`函数，`Contacts`接口，393

## 内容

- `footer`元素，17–19

- 使用`section`元素分组，12–14

- 可能的`header`，5

## `closePath`方法，canvas线条，139，142

## `closeWS`函数，WebSocket API，299–301

## 编解码器

- `audio`元素问题，188

- HTML5和视频，165

- 为什么应该关注，165–166

## 编码，HTML5的原则，xxv

## 颜色。*另见* 背景颜色

- CSS3过渡，86–89

- 覆盖表单占位符文本，109

- 美化正方形，136

## `color`输入类型

- 颜色选择器，107–108

- 创建注册表单，122–125

## 颜色选择器，107–108

## 逗号分隔值（CSV）文件，使用`readAsText`解析，373–380

## 注释

- 使用注释标记文章页面，51–54

- 在`article`元素中标记注释，11–12

## 通信

- 添加双向通信，308–311

- 创建web worker，304–308

- 利用共享web worker，311–318

- 概述，297

- 通过web sockets进行通信，299–302

## `controls`属性，`audio`元素，191

## `controls`属性，`video`元素，172–173

## 控件，自定义视频控件，178–186

## 食谱风格，HTML5，xxvii–xxviii

## Cookies，存储，259

## 坐标系，canvas

- 绘制网格，130–134

- 概述，129

## `coords`对象，`getCurrentPosition`，236，239

## 版权数据，`footer`元素，17

## Create Polygon按钮，142

## `createHTMLNotification`属性，`NotificationCenter`，342

## `createLinearGradient`方法，形状，135

- 定义，342

## `createNotification`属性，`NotificationCenter`

- 简单通知，344–347

- tweet通知，348，352

## `createPattern`方法，裁剪图像，145–146

## `createRadialGradient`方法，形状，135

## 裁剪图像，145–146

## 跨浏览器修复，`@font-face`，79

## CSS（层叠样式表），188

- beat mixer，193–197

- 构建HTML5入门文档，3

- 创建带字幕和标题的视频，174–176

- 自定义视频控件，179，184

- HTML5与CSS，xxvi

- 使IE兼容HTML5，56–57

- 设置视频高度和宽度，167

- 流式广播播放器，197

- 开发过程中的可用性，xxix

- 用于分隔符，46

- 在线使用网页，338–340

- 与ARIA roles一起使用，51

## CSS3

- 动画，89–94

- 基本用户界面模块，120–121

- 带有渐变和多重背景的按钮，80–83

- 使用`@font-face`的自定义字体，77–78

- 使用Modernizr进行特性检测，62–64

- 文件格式和跨浏览器修复，78–79

- iPhone和Android设备以及CSS3，76

- Media Queries，69–76

- 概述，69

- 合理使用，76

- 设置canvas样式，128

- 设置表单元素样式，119–121

- 变换与过渡，84–89

- 类型服务，79–80

## CSV（逗号分隔值）文件，使用`readAsText`解析，373–380

## 曲线，绘制

- 使用Curve工具，134

- 概述，143–144

## 自定义字体

- 使用CSS3 `@font-face`，77–78

- 文件格式和跨浏览器修复，78–79

- 类型服务，79–80

## 自定义视频控件，178–186

## 自定义Web表单，119–121

## D

### `data`参数，History API

- `pushState`方法，208–209

- `replaceState`方法，216–218

### 数据库存储

- HTML5选项，260

- 客户端安全问题，260–261

- 用于杂货清单，286–295

- Web SQL Database API，283–286

### `datalist`元素

- 创建自动完成功能，110–111

- 创建注册表单，122–125

## `dataTransfer`

- 属性和方法，320

## `dataTransfer`（续）

- 拖放API，321–324

- 利用事件与，325，329–330，332–333

## `date`输入类型

- 日历，103–104

- 创建注册表单，122–125

- 利用jQuery替换日历，59–62

## Date，使用`time`元素标记，34–35

## `datetime`属性，`time`元素，34–35

## `datetime`输入类型，日历，102–103

## `datetime-local`输入类型，日历，103

## `dbPresent`函数，数据库存储，287，289，293

## 调试

- 开发worker功能以简化调试，317

- 拖放编程，333

- 在地理位置API中，237

- 为调试而移除数据库，287–288

## 专用Web Workers

- 添加双向通信，308–311

- 定义，302

- 方法与事件，303

## 定义列表，42–43

## `del`元素，已编辑或删除的文本，39

## `deleteItem`方法，数据库存储，288

## 描述列表，用于此的`dl`元素，43–44

## `descriptions`值，`kind`属性，173

## `details`元素，使用其进行切换，35–37

## 设备API工作组，389–390

## 设备数据，集成

- 电池状态事件，398

- 通讯录API，391–396

- 设备API历史，389–391

- 设备方向与运动事件，403–408

- HTML媒体捕获，398–402

- 消息API，396–397

- 网络信息API，397–398

- 概述，389

## 设备方向与运动事件

- 创建水平仪，404–408

- 概述，403–404

## `DeviceAcceleration`接口，404

## `devicemotion`事件，403–404

## `deviceorientation`事件

- 创建水平仪，404–408

- 定义，403

## `DeviceRotationRate`接口，404

## 直接下载，适用于较旧的浏览器，167

## 目录与系统规范，File API，381–382

## `DirectoryEntry`接口，381

## 显示结果，使用`output`元素，108–109

## `displayFiles`函数，通过拖放处理多个文件，362–366

## `div`元素

- 拖放API，321–325

- 作为最后手段，14–15

## `dl`元素，42–44

## `doctype`

- HTML5入门文档，2

- 新闻主页，23

- 搜索结果页，26

## 文档类型定义（DTD），2

## `downloading`事件，应用程序缓存API，341

## 拖放API

- 跨`div`拖放，321–325

- 利用事件与`dataTransfer`，325–333

- 概述，319–321

- 处理多个文件，362–367

## `draggable`属性，拖放API，319–320，321，324

## `dragstart`属性，拖放API，320

## `dragStartHandler`函数，拖放API，322，324

## `drawAxis`函数，垂直柱状图动画，155，157–158，161

## `drawBar`函数，垂直柱状图动画，155，160–161

## `drawImage`方法，canvas，145–150

## 绘图，使用canvas。*参见* canvas

## `drawPolygon`函数，139–142

## `drop`事件，`dropzone`属性，320

## 放置区域

- 利用事件与`dataTransfer`，326，328，331–333

- 通过拖放处理多个文件，362–366

## `dropHandler`函数，322，324–325

## `dropzone`属性，320–321，324

## DTD（文档类型定义），2

## 时长，自定义视频控件，179–181，183–185

## `durationChange`事件，流媒体广播，200，206

# E

## 效果，用于此的canvas工具，135

## 元素

- 分组或文本级别。*参见* 分组或文本级别元素

- 结构性。*参见* 结构性元素，新的

- 将链接包裹在其周围，47

## 元素，现有元素的更改

- `abbr`，46

- `b`和`strong`，44–45

- `cite`，39–40

- `dl`，42–44

- `hr`，46

- `i`和`em`，45–46

- `ol`，40–42

- 已移除的元素，46–47

- `small`，44

## `em`元素，45–46

## 电子邮件，创建本地文件，382–388

## `email`输入类型

- 创建联系表单，98–99

- 创建注册表单，122–125

## 嵌入式

- 音频。*参见* 音频，使用HTML5嵌入

- 视频。*参见* 视频，使用HTML5嵌入

## 嵌入式OpenType（.eot）字体文件格式，78

## 强调，句子，45–46

## `enableHighAccuracy`，`PositionOptions`，243

## `ENCODING_ERR`，`FileReader`，373，378

## 加密，数据存储，260–261

## END消息，推文通知，355–356

## `Entry`接口，381

## .eot（嵌入式OpenType）字体文件格式，78

## 错误代码值

- `FileReader`，373，378

- 消息API，397

## `error`事件，应用程序缓存API，341

## 错误处理

- 更改Web表单的消息，121

- Web SQL数据库API，285–286

## 错误处理，地理位置API

- 确定距离，247

- 跟随移动位置，254

- 位置隐私，237

- 映射位置，238，240–242

## `errorCallback`参数

- `getCurrentPosition`，233

- `watchPosition`，250，251

## 事件处理

- 与`dataTransfer`，326–328

- 本地存储，276–277，282

- 推文通知，348，351–353

## 事件

- 应用程序缓存，340–341

- 电池状态，398

- 在本地存储中捕获，275–283

- `dataTransfer`与利用，325–333

- 设备方向与运动，403–404

- 拖放API，320，325

- `FileReader`，367–368

- 利用共享web worker，312

- 媒体API，177，192–193，197

- 网络信息API，398

- 使用`readAsText`解析CSV文件，374–376

- Web Workers API，303

- WebSocket API，298

## `executeSql`方法，Web SQL数据库API，284–285

## 可扩展超文本标记语言（XHTML），xxiii–xxiv

## File API

- 扩展规范，381–382

- 概述，359–360

## 文件格式，以及CSS3跨浏览器修复，78–79

## `file`输入元素，捕获图片，399–402

## `File`接口，359–362

## `fileAction`函数，本地文件，383，385–387

## `fileAttributes`部分，360–362

## `FileEntry`接口，381

## `fileErrorHandler`函数，本地文件，383–386

## `FileList`接口

- File API，359

- 获取文件属性，360–362

- 通过拖放处理多个文件，362–367

## `FileReader`接口

- File API，359

- 本地文件，367–368

- 概述，367–368

- 使用`readAsText`解析CSV文件，373–380

- 通过`readAsDataURL`预览图像，368–372

## `FileReaderSync`，368

## `FileSaver`接口，381

## `FileSystem`接口，381

## `FileWriter`接口，381–382，385–387

## 填充效果，canvas工具，135

## `fillRect`方法，矩形或正方形，135–136

## `fillStyle`方法

- 向canvas添加文本，144

- 形状，135–137

## `fillText`方法

- 向canvas添加文本，144

- 绘制canvas网格，130–134

## 过滤器，`dropzone`属性，320

# F

## 回退容器，canvas，129

## 回退内容，在较旧的浏览器中，167–169，189–190

## FALLBACK部分，清单文件，336–337

## 快进按钮，自定义视频控件，186

## 特性检测方法，浏览器

- Modernizr，62–66

- 概述，57–59

## `figcaption`元素，31–34

## `figure`元素

- 和`figcaption`，31–34

- 应用旋转转换，84

## `find`方法，`Contacts`接口，391，393–395

## `findAllContacts`方法，`Contacts`接口，393–395

## `FindMe`函数，`getCurrentPosition`，233–235

## Firefox。*参见* 浏览器支持

## `fireNotification`函数，Notification API，344–345

## Flash Player回退，较旧的浏览器，167–169，189–190

## Font Squirrel，78–80

## 字体栈，使用CSS `font-family`，80

## FontDeck服务，80

# 字体

- 向canvas添加文本，144

- 使用CSS3 `@font-face`自定义，77–78

- 文件格式与跨浏览器修复，78–79

- 字体服务，79–80

# `footer`元素

- 内部的作者信息，6

- 在`blockquote`中，40

- 创建新闻主页，23–25

- 创建搜索结果页，28–29

- 使用，17–19

## `form`元素，页面加载时跳转至，114–115

# 格式

- CSS3跨浏览器修复与文件，78–79

- `drawImage`函数，145

## `formnovalidate`属性，表单条目，119

## 表单。*参见* Web表单

## 论坛帖子，标记，11–12

## 全屏模式，视频，181，183–185

# G

## 地理编码，232

# `geoErrorHandler`函数

- `getCurrentPosition`，238，240–242

- `PositionOptions`，247

# 地理位置API

- 浏览器兼容性，232

- 设备方向规范，403–404

- `getCurrentPosition`，位置感知，233–236

- `getCurrentPosition`，位置隐私，237

- `getCurrentPosition`，映射位置，237–243

- 概述，231–232

- `PositionOptions`，确定距离，243–249

- `watchPosition`，跟随移动位置，250–257

## `geoSuccess`函数，`getCurrentPosition`，234–236，239

## `getContext`方法，在canvas上绘图，129

# `getCurrentPosition`方法，地理位置API

- 确定浏览器位置，233–236

- 使用`PositionOptions`确定距离，243–249

- 位置隐私，237

- 映射位置，237–243

- 概述，233

## `getData`属性，`DataTransfer`，320

## `getDepartments`函数，数据库存储，288

## `getGroceryItems`函数，数据库存储，288，290–292

# `getItem`方法

- `sessionStorage`，263–264

- `sessionStorage`和`localStorage`，262

`getTimeStamp`函数，Web Worker，304–305

GitHub，228

术语表，使用`dl`创建，43

Google

Chrome。参见Chrome



# 字体目录

79–80

# HTML5 与视频编解码器

165–166

# Google Maps API V3 服务

地理位置 API 与，232

`getCurrentPosition`，237–243

`PositionOptions`，244–249

`watchPosition`，250–257

Grab Tweets 按钮，推文通知，355

`grabTweets` 函数，349

# 渐变生成器

83

## 渐变

添加到形状，137–138

具有多重背景和 CSS3 的按钮，80–83

Canvas 工具，135

格里高利历，34–35

## 网格系统，Canvas

130–134

# 杂货清单页面，数据库存储

287–295

## 内容分组

12–14

## 标题分组

7–8

## 导航分组

9–10

## 分组或文本级元素。另见元素，现有元素的变更

使用`address`的联系信息，37–38

使用评论创建文章页面，51–54

使用`time`表示日期和时间，34–35

`figure`和`figcaption`，31–34

使用`mark`高亮文本，38

使用`s`显示不准确/无关内容，39

使用`details`进行切换，35–37

使用微数据，47–49

使用 WAI-ARIA，49–51

将链接包裹在元素周围，47

`growBars`函数，157，159–161

# H

H.264 编解码器（MPEG-4），165–166

`handleCapture`函数，HTML Media Capture，399–401

`handleDragOver`函数，多个文件，362–364，366

## `handleFile`函数

获取文件属性，360–361

解析 CSV 文件，374–375，378–379

`handleFileDrop`函数，多个文件，362–363，366

`handleFiles`函数，图像预览，368–369，371

哈希地址方法，History API，228

`hashChange`事件，History API，228

## `header`元素

创建文档大纲，21

创建新闻主页，23–25

创建搜索结果页，27–28

创建站点页头，5–7

使用`hgroup`分组标题，7–8

内部的`nav`元素，9

## 标题

文档大纲，21

使用`hgroup`分组，7–8

页面上的多个`header`元素，6–7

`height`值，`video`元素，167

## `hgroup`元素

分组标题，7–8

制作文档大纲，21

Hickson, Ian "Hixie"，4，xxiv

`high`属性，`progress`元素，113

高亮文本，38

## 历史记录

更改浏览器历史记录。参见浏览器历史记录

History API，207

HTML 的历史，xxiii–xxv

`history.js`库，228

托管站点，旧版浏览器的音频，189

`:hover`状态，CSS3 过渡，86–89

`hr`元素，46

IE Print Protector，56

IETF（互联网工程任务组），HTML 历史，xxiii

HTML（超文本标记语言），xxiii–xxv

HTML Media Capture，398–402

HTML4，输入类型，95–97

## HTML5

Boilerplate，57

Cookbook 风格，xxvii–xxviii

增强功能和新特性，xxvi

标志，xxvii

原则，xxv–xxvi

可用性就绪，xxix

第三方库，xxviii

Web Forms 2.0 和 Web App 1.0 作为其一部分，xxiv

XHTML 2 与之对比，xxiv

HTML5DevelopersCookbook.com，xxvii

HTML5Shiv，56

## 图像查看器

创建历史记录条目，211–214

其中的`popstate`事件，214–216

## 图像

添加标题，31–34

添加悬停效果，88–89

动画效果，151–155

捕捉摄像头，399–402

裁剪，145–146

在 Canvas 中绘制，145–146

用于在线网页，338–340

使用`readAsDataURL`预览，368–372

`i`元素，45–46

图标，xxvii

`id`样式，Canvas，129–130

## IE（Internet Explorer）。另见浏览器支持

旧版浏览器中的音频，189–190

CSS 兼容性，56–57

支持 HTML5，55

使用 Selectivizr 实现新的 CSS 选择器，72

`img`标签，使用`figure`/`figcaption`元素代替，32

`importScripts`命令，推文通知，349，353，355–356

不准确内容，使用`s`元素显示，39

IndexedDB API，数据库存储，260，283–286

## `init`函数

创建水平仪，404–408

创建数据库存储，287–288

使用 Canvas 绘制多边形，140

用于会话存储，263–264

流式收音机播放器，199，202，205

通过 Web Socket 通话，299

`initGraph`函数，动画化垂直柱状图，155，157，160–161

`initMap`函数，`watchPosition`，251–252，255–256

`initNoteBoard`函数，本地存储，276–277，281

`initPage`函数，数据库存储，288

`initShoppingDb`函数，数据库存储，287，289–290，293

## 输入类型

颜色，107–108

联系表单，97–101

日期，103–104

日期时间，102–103

本地日期时间，103

电子邮件，98–99

HTML4，95–97

利用 jQuery 替换日历，59–62

月份，104

多个条目，115–116

数字，105–106

范围，106–107

搜索，100

搜索表单，101–102

注册表单，122–125

电话，99

时间，104

URL，100

周，104–105

## 接口

File API，359

文件写入器，381

`FileEntry`，381

`FileList`，359–367

`FileReader`。参见`FileReader`接口

`FileSaver`，381

`FileSystem`，381

`FileWriter`，381

`Notification`，341–342

`NotificationCenter`，341–342

`Worker`，303

中级食谱，412–413，xxviii

互联网工程任务组（IETF），HTML 历史，xxiii

Internet Explorer。参见 IE（Internet Explorer）

交点，Canvas 网格，134

`:invalid`类，CSS3，121

`INVALID_ARGUMENT_ERROR`代码，Messaging API，397

`IO_ERROR`代码，Messaging API，397

iOS Safari。参见浏览器支持

IP 地址位置挑战，231

iPhone，76。另见浏览器支持

无关内容，使用`s`元素显示，39

`itemid`属性，微数据，48

`itemprop`属性，微数据，48

`itemref`属性，微数据，48

`itemscope`属性，微数据，48

`itemtype`属性，微数据，48

## 设备数据集成。参见设备数据，集成

## 接口

基础用户界面模块，CSS3，120–121

`BlobBuilder`，381

`Connection`，397

`ContactField`，392，395

`Contacts`，391–395

`DeviceAcceleration`，404

`DeviceRotationRate`，404

目录和系统，381

`DirectoryEntry`，381

`Entry`，381

`File`，359–362

## JavaScript

构建 HTML5 起始文档，3

创建自定义视频控件，184

创建带字幕和隐藏字幕的视频，174–176

从 JavaScript 在 Canvas 上绘图，129

使用 Modernizr 和 JavaScript 进行功能检测，64–65

使用 JavaScript 实现 Canvas，127–128

用于 jQuery 日历小部件，61

使 IE 兼容 HTML5，55–56

使用 JavaScript 为手机设置样式，69

用于在线网页，338–340

## jQuery 日历

用作备用方案，59–62

使用 Modernizr 作为检测工具，65–66

jQuery 插件，带字幕和隐藏字幕的视频，174–176

## JSON

列出电台和 URL，197，205

推送带数据的页面，221–222，224

使用开发者工具查看存储，265

JSONP，Twitter REST API 与，348

JW Player，169，189–190

# K

`key`方法，使用本地存储存储表单，271–275

## 键/值对

使用 Chrome 开发者工具查看，265–266

基于源的安全性和，260

用于会话存储和本地存储，261–262

用于会话存储，263–264

使用本地存储存储表单，271–275

从会话存储设置样式，266–271

用于 Web 存储，259–260

`kind`属性，带字幕和隐藏字幕的视频，173

# L

标签，使用微数据添加，47–49

## 地标角色部分，ARIA

标记带评论的文章页面，51–54

概述，49–51

语言，日历上的日期时间控件，103

`lastModifiedDate`属性，File API，359，362

`lastTweetId`，推文通知，355

## 纬度坐标

地理位置 API，232

`getCurrentPosition`，242

`PositionOptions`，244–249

逆向地理编码，232

`watchPosition`，253，255–256

图层，在 Canvas 中，150

法律问题，字体服务，79–80

`legend`元素，32

`length`属性，表单的本地存储，271–272

`lengthComputable`属性，`onprogress`事件，374，377，379

库，228，xxviii

许可协议，在`footer`内，18

`line`方法，绘制 Canvas 网格，130–133

直线工具，Canvas，134

线性渐变，81，137–138

线条，在 Canvas 中绘制，138–139

## 链接

在`footer`元素内，19

包裹在元素周围，47

`list`属性，`datalist`元素，110–111

`loaded`属性，`onprogress`事件，374

`loadeddata`事件监听器，自定义视频控件，185

`loadPages`函数，页面历史记录，219–220

## 本地文件

创建，335–337

引用，335

使用在线网页，337–340

## 本地文件

创建，382–388

File API 扩展规范，381–382

File API 概述，359–360

`FileReader`接口，367–368

获取文件属性，360–362

解析 CSV 文件，373–380

预览图像，368–372

处理多个文件，362–367

“Map Me”按钮，237–238, 241

映射位置，使用`getCurrentPosition`，237–243

`mark`元素，高亮文本，38

## `max`属性

限制表单条目，118

数字输入类型，105

`progress`元素，111–112, 113

范围输入类型，105–106

限制部件的日期或时间，104–105

## 本地存储

捕获其中的事件，275–283

键/值对，261–262

基于源的安全策略，260

会话存储与之对比，259

使用其存储表单，271–275

网页数据库存储与之对比，284

`max-device-width`，CSS3 媒体查询，71–72

`max-width`，CSS3 媒体查询，71

`maximumAge`，`PositionOptions`，243

测量，使用`meter`元素，112–113

位置感知。参见 Geolocation API

## 标志

在`footer`元素内，18

在`header`元素内，5

HTML5 与之相关，xxvii

## 媒体 API

音频，192–193

视频，177

媒体捕获。参见 HTML Media Capture

## CSS3 媒体查询

浏览器支持，70

组合不同的查询，71–72

为新闻网站精简 HTML，72–73

默认屏幕布局，73–74

示例，70

在 CSS 文件内，70–71

概述，69–70

减小的屏幕尺寸，74–75

选择器，72

合理使用，76

用于智能手机，75–76

定位 iPhone 和 Android 设备，76–77

## 经度坐标

Geolocation API，232

`getCurrentPosition`，242

`PositionOptions`，244–249

反向地理编码中，232

`watchPosition`，253, 255–256

## `loop`属性

`audio`元素，190

`video`元素，172

`low`属性，`progress`元素，113

# M

## 清单文件

应用缓存 API，340–341

其中捕获的应用缓存文件，334

`nextExhibit`函数，将页面添加到历史记录，431

`MESSAGE_SIZE_EXCEEDED`代码，Messaging API，397

多媒体 API，177

Messaging API，396–397

`multiple`属性，网页表单条目，115–116

`metadata`属性，`audio`元素，190

多个条目，网页表单，115–116

`metadata`值，`kind`属性，173

`myLocation`，`getCurrentPosition`，234

`meter`元素，使用其进行测量，112–113

# N

Micro-library，Modernizr，63

微数据，添加语义信息，47–49

`name`属性，File API，359, 362

## `nav`元素

微格式，扩展 HTML，49

创建导航，8–10

MIME 类型，HTML5 视频开发，169

## `min`属性

限制表单条目，118

创建新闻主页，23–25

数字输入类型，105

## 导航

`progress`元素，113

用于导航的`header`元素，5–7

使用`nav`元素。参见`nav`元素

限制部件的日期或时间，104–105

`Navigator`地理定位对象，235

移动浏览，用于其的 CSS3 媒体查询，69–76

## 嵌套元素

`article`元素，11

## Modernizr

检测浏览器功能，62–66

`aside`元素，16–17

加载跨浏览器填充脚本，66–67

`strong`元素，45

Network Information API，397–398

`month`输入类型，日历，104

`NETWORK`部分，清单文件，336–337

`mouseclick`事件，CSS 过渡，86–89

## 新闻项，标记

11–12

`mouseover`事件

## 新闻页面

CSS 过渡，86–89

使用新元素构建，21–25

与画布交互，155

使用`section`创建，13–14

`moveGear`函数，动画图像，152–155

## 新闻网站

为其精简 HTML，72–73

`nextState`函数，更改历史记录，217

注意事项，本地存储事件，275–283

`NOT_FOUND_ERR`，`FileReader`，373, 378

## Notification API

创建推文通知页面，347–356

显示简单通知，344–347

概述，341–343

`Notification`接口，341–342

`NotificationCenter`接口，341–342

`NOT_READABLE_ERR`，`FileReader`，373, 378

`NOT_SUPPORTED_ERROR`，Messaging API，397

`noupdate`事件，应用缓存 API，341

`novalidate`属性，限制表单条目，119

`nth-child`选择器，CSS3，72

`nth-of-type`选择器，CSS3，72

`nullHandler`函数，数据库存储，287

`number`输入类型，105–106, 122–125

数字选择器，105–106

# O

`obsolete`事件，应用缓存 API，341

`offline`事件，Network Information API，398

离线，网页，337–340

`.ogg`文件（Ogg Vorbis），音频编码

- `audio`元素问题，188

- 节拍混音器，193–197

- 流式广播，197–206

Ogg Theora 编解码器，165

## `ol`元素

变更，40–42

标记带评论的文章页面，53

`onbatterystatus`属性，Battery Status 事件，398

## `onchange`事件

通过文件输入捕获图片，399–402

获取文件属性，360–361

处理多个文件，362, 365

流式广播播放器，205

## `onclose`事件

推文通知，352, 355–356

WebSocket API，298–301

`onconnect`事件，共享 Web Worker，317

`onDbError`函数，数据库存储，287, 290–294



`ondisplay`事件，推文通知，348，352，355–356

`ondragstart`属性，拖放 API，320，324

`ondrop`事件，`dropzone`属性，320

### `onerror`事件

推文通知，352，355–356

双向通信，308–309

Web Workers API，303

WebSocket API，298–302

`online`事件，Network Information API，398

`onload FileReader`事件，预览图像，368，370，372

### `onmessage`事件

创建 Web Worker，307

利用共享 Web Worker，317

推文通知，352，355

Web Workers API，303

WebSocket API，298–302

`onmousedown`事件，拖放 API，324

`onopen`事件，WebSocket API，298–301

`onprogress`事件，`FileReader`，374

`onStorageEvent`函数，本地存储，276–277，282

`open`属性，`details`，35–36

`postMessage`函数，433

`openDatabase`方法，Web SQL Database API，284–285

- 简单通知，344–346

- 推文通知，349–351，353，355

`openShoppingDb`函数，287，289

`OpenType PS (.otf)`字体文件格式，78

Opera，59–60。*另见*浏览器支持

`optimum`属性，`progress`元素，113

`PERMISSIONS_DENIED_ERROR`，Messaging API，397

`PERMISSION_UNAVAILABLE`错误

`options`参数，`getCurrentPosition`，233

- `getCurrentPosition`，241

- `PositionOptions`，247

- `watchPosition`，254

`options`参数，`watchPosition`，250

### 有序列表，40–41

### 网络钓鱼攻击，与历史记录安全性，225

### 基于源的安全策略，存储选项，260

### 占位符文本，表单，109–110

`.otf (OpenType PS)`字体文件格式，78

### 大纲，制作文档，19–21

### 播放按钮

- 节拍混音器，194，197

- 自定义视频控件，178

`Outliner`扩展图标，HTML5，19–21

`output`元素，显示结果，108–109

### 播放/暂停按钮，流式广播，198，200–202，205–206

# P

### 播放速率，视频，181–183，185

### 页面元素

### 策略，浏览器，225

内容。*参见*分组或文本级元素

结构性。*参见*结构性元素，新

### 填充脚本，66–67

### 段落分隔，`hr`元素，46

### 多边形，绘制，139–142

### 解析 CSV 文件，使用`readAsText`，373–380

### `popstate`事件

### 路径工具，画布，134

- 为网站添加/修改历史记录，207

- 更改页面历史记录，218–220

- 在图像查看器中，214–216

- 推送带数据的页面，221–225

- 使用其检索新条目的数据参数，208

- 测试历史记录安全性，225

### 路径

- 使用画布绘制多边形，139–142

- 使用画布绘制，138–139

`pattern`属性，验证规则，117

`pause`方法，节拍混音器，194，197

`position`返回对象，浏览器位置，236

`PENDING_OPERATION_ERROR`，Messaging API，397

`PositionOptions`方法，Geolocation API，243–249

`PERMISSION_DENIED`错误

`posOptions`，`getCurrentPosition`，247，249

`poster`属性，`video`元素，170–171

`postToWorker`函数，双向通信，308–310

`preload`属性，`audio`元素，190–191

`preload`属性，`video`元素，171

### `preventDefault`方法

- 调试拖放，333

- 跨`div`拖放，325

- 利用事件和`dataTransfer`，328，332–333

`progress`元素，跟踪任务完成情况，111–112

`progress`事件，应用缓存 API，341

### 属性

- 音频媒体 API，192–193

- 客户端存储类型及其，260

- 使用 Modernizr 检测，62–63

- File API，359

- `sessionStorage`和`localStorage`，261

- 视频媒体 API，177

`pubdate`属性，`time`元素，34

`pushPage`函数，历史记录安全性，225–227

### `pushState`方法

- 添加到历史记录，208–211

- 更改页面历史记录，218–220

- 定义，207

- 在图像查看器中，216

- 推送带数据的页面，221–225

- 测试历史记录安全性，225–228

# Q

`quadraticCurveTo`，绘制曲线，143

引号，语法，3

# R

径向渐变，81–83，137–138

### `range`输入类型

- 创建注册表单，122–125

- 创建滑块，106–107

- 自定义视频控件怪癖，186

`RDFa`，扩展 HTML，49

`readAsDataURL`，预览图像，368–372

`readAsText`方法，解析 CSV 文件，373–380

`readFromFile`函数，本地文件，383，385–387

`readyState`属性值，WebSocket，298

`readyState`值，自定义视频控件，181，184

### 食谱

- 高级，413–414

- 初级，411–412

- 本书使用的食谱风格，xxvii–xxviii

- 中级，412–413

矩形工具，画布，134

矩形，绘制，135–136

正则表达式，编写验证规则，117

移除数据库按钮，287

已移除元素，来自 HTML5，46–47

`removeDatabase`函数，288，292–293

`removeFile`函数，本地文件，383，385

`removeItem`方法，从会话存储设置样式，266，271

`removeNote`函数，本地存储，276，279–280

`repeat`参数，裁剪图像，146

### `replaceState`方法

- 更改历史记录，216–218

- 更改页面历史记录，218–220

- 定义，207

- 推送带数据的页面，221–225

- 测试历史记录安全性，225，228

`requestPermission`方法，Notification API，345–346

`setItem`方法，客户端存储 435

必填属性

- 创建注册表单，122–125

- 电子邮件输入类型，98–99

- 表单验证，95，116

- 内容分组，12–14

- 创建文档大纲，21

- 使用`article`元素对比，14–15

## 安全

- 浏览器缓存，334

- 客户端数据存储问题，260–261

- File API，360

- Notification API 权限，343

- 测试历史记录，225–228

`:required`类，CSS3，121

`resetGroceryList`方法，数据库存储，288，292–293

重置，CSS，57

`SECURITY_ERR`，`FileReader`，373，378

`restore`方法，`canvas`，151

`results`属性，搜索输入类型，101

`select`元素，流媒体广播播放器，200–201，205

反向地理编码，232

`reversed`属性，`ol`元素，40–41，53

Selectivizr，72

选择器，新的 CSS3，72

`reverseGeoCode`函数，`PositionOptions`，244–245

语义信息，通过 Microdata 添加，47–49

倒带按钮，自定义视频控件，186

`rotate`函数，CSS `transform`属性，84–86

`sendAllConnections`函数，共享 Web Worker，315–316

`rotate`方法，`canvas`，150–151，154

`sendMessage`方法，Messaging API，396–397

规则，编写验证，117

## S

`sendNumber`函数，共享 Web Worker，313，317

`s`元素，39

Safari。请参阅浏览器支持

会话历史，207

### 会话存储

- 获取与设置，263–264

- 键/值对，261–262

- 本地存储对比，259

- 基于源的安全机制，260

- 运行示例，270

- 设置样式，266–271

- 使用 Chrome 开发者工具查看，265–266

- Web 数据库存储对比，284

`save`方法，`canvas`，151

`scale`函数，CSS `transform`属性，86

`scale`方法，`canvas`，151

脚本标签，推文通知，348

### 搜索表单

- 使用`input type="search"`创建，101–102

- 使用`header`元素，5

### 会话

- 跨会话数据库存储，260

- 跨会话本地存储，259–260

### `search`输入类型

- 创建搜索表单，101–102

- 使用`autofocus`，114–115

`setData`属性，`DataTransfer`，320

搜索结果页，25–29

`setItem`方法，客户端存储，261–264

`setLocation`函数，`PositionOptions`，244

### `setPermission`函数

- Notification API，344–347

- 推文通知，349

`setStation`函数，流媒体广播，197，201，205

阴影效果，135

`shadowBlur`方法，形状，135–137

`shadowColor`方法，形状，135–137

`shadowOffsetX`方法，形状，135–137

`shadowOffsetY`方法，形状，135–137

形状，135，137–138

共享 Web Worker，302，311–318

`shoppingdb`变量声明，数据库存储，287，289

`showDepartments`函数，数据库存储，288

`showFile`函数，预览图像，368，370，372

`showGrid`函数，在`canvas`上绘制网格，131，133

`showGroceryItems`函数，数据库存储，288，291，293–295

### 侧边栏

- 使用`aside`元素创建，15–17

- 使用`nav`对导航进行分组，9–10

- 本地存储事件，275–283

注册表单，121–125

站点页头，创建，5–7

站点所有者，在页脚内，17

站点条款和条件，在页脚内，17

`size`属性，File API，359，362

`skew`函数，CSS `transform`属性，86

滑块控件，106–107

`small`元素，44

智能手机，75–76

Socket 连接。请参阅 WebSocket API

### `source`元素

- 显示视频格式，166–167

- 为所有浏览器启用音频，188–190

规范，File API 扩展，381–382

精灵图，动画，147–150

### SQLite 数据库

- 存储，260

- 使用 Web 数据库存储购物清单，287

- 基于 SQLite 的 Web SQL Database API，283–284

正方形，绘制，135–136

### `src`属性

- 音频元素，190

- 视频元素，170

### 栈，历史

- 使用`pushState`添加历史记录，207

- 更改页面历史，220

- 定义，207

- 替换当前历史状态，218

`start`属性，`ol`元素，40–41

`startAnimation`函数，精灵图，147–149

`startWatch`函数，`watchPosition`，251，256

`startWorkerThread`函数，Web Worker，304–307

### `stateInfo div`

- 创建图像查看器，212–213

- 在图像查看器中弹出状态，215–216

- 历史状态的推入与弹出，216

- 替换当前历史状态，217–218

### `step`属性

- 限制表单输入项，118

- 数字输入类型，105–106

- 范围输入类型，105–106

`stepDegrees`方法，动画图像，154

`stopAnimation`函数，精灵图，147–149

存储。请参阅客户端存储

`storageEvent`属性，本地存储，275

### 流媒体音频，197–206

`streamPlaying`函数，流媒体广播，200–201，206

### `stringify`方法，JSON

- 更改页面历史，219

- 在图像查看器中弹出状态，215

- 推入带数据的页面，222，224

描边效果，`canvas`工具，135

`stroke`方法，`canvas`线条，138

`strokeRec`方法，矩形，136

`strokeStyle`方法，形状，135–137

`strokeText`方法，`canvas`，144

`strong`元素，44–45

## 结构元素，新的

- `article`，11–12

- `article`对比`section`，14–15

- 构建新闻页面，21–25

- 构建搜索结果页，25–29

- 构建入门文档，2–4

- 使用 HTML5 Outliner 确保正确结构，19–21

- 使用`nav`创建导航，8–10

- 使用`aside`创建侧边栏，15–17

- 使用`header`创建站点页头，5–7

- `footer`，17–19

- 使用`section`对内容分组，12–14

- 使用`hgroup`对标题分组，7–8

- 概述，1

- 新元素的来源，4–5

## 样式化

- 矩形和正方形，135–137

- 从会话存储设置样式，266–271

- 视频字幕，173–176

- Web 表单，119–121

字幕，视频，173–176

### `successCallback`参数

- `getCurrentPosition`，233

- `watchPosition`，250，251

`summary`元素，在`details`元素内，35–36

`.svg (SVG)`字体文件格式，78

`swapCache`函数，应用缓存 API，341

## 语法

- HTML5 编写风格，3

- XHTML 规则，xxiii

`SYNTAX_ERR`，Web SQL Database API，286

# T

目录，显示/隐藏，36–37

标签，HTML4，62–66

任务完成，跟踪，111–112

### `tel`输入类型

- 联系表单，99

- 注册表单，122–125

`terminateWorker`函数，304–306

## 测试

- 浏览器的 HTML5 功能支持，57–59

- 历史记录安全，225–228

- 通知，346

## 文本

- 添加到`canvas`，144

- 表单占位符，109–110

`text`输入类型，96，122–125

文本级元素。请参阅分组或文本级元素

`textReader`，`FileReader`，374–376

## 主题

- 在会话存储中设置，266–270

- 显示，268–270

第三方库，HTML5，xxviii

线程。请参阅 Web Workers API

时间控件，日历，101–105

### `time`元素

- 日期和时间，34–35

- 标记带评论的文章页面，53

`time`输入类型，日历，104

时区，日历，103

### 超时

- 通知，352，356

- `PositionOptions`，243

### `TIMEOUT`错误代码

- `getCurrentPosition`，241

- Messaging API，397

- `PositionOptions`，247

- `watchPosition`，254

超时错误，Geolocation API，237

时间戳，`GetCurrentPosition`，239

### `title`参数



- `pushState`方法，208–209

- `replaceState`方法，216–218

切换，使用`details`元素，35–37

工具，`canvas`，134

`toString`内置方法，查看会话存储，265

`total`属性，`onprogress`事件，374

汉诺塔游戏，325

`track`元素，173–174

`transaction`方法，Web SQL Database API，284–285

## 变换

- 用于变换的`canvas`工具，150–151

- CSS3，84–89

过渡，CSS3，84–89，94

### `translate`函数

- `canvas`，151，154

- CSS `transform`属性，86

透明效果，`canvas`工具，135

`.ttf` (TrueType/OpenType) 字体文件格式，78

TWEET 消息，推文通知，355–356

推文通知页面，348–356

Twitter REST API，348

Twitter，推文通知页面，348–356

`tworker`，通知，349–350，353，355

`type`属性，Network Information API，397

`type`属性，`ol`元素，40–42

`type`属性，File API，359，362

字体服务，CSS3，79–80

TypeKit 服务，80

# U

## `UNKNOWN_ERROR`代码

- `getCurrentPosition`，242

- Messaging API，397

- `PositionOptions`，247

- `watchPosition`，254

无序列表，标记导航，8

`updateAverage`函数，共享 Web Worker，315–316

`updateNote`函数，本地存储，276–281

`updateNoteBoard`函数，本地存储，276–281

`updateready`事件，应用缓存 API，341

### 更新

- 通过清单文件更新缓存，337

- Contact API 中的联系人更新，391

`updateStatus`函数，WebSocket API，299–301

上传，多文件，115

大写，语法编写风格，3

`url` input type

contact form, 100

sign-up form, 122–125

## `url` parameter, `pushState` method, 208–209, 211

## `url` parameter, `replaceState` method, 216–218

## URLs

- 通过`pushState`添加到历史记录, 209–211

- `drawImage` method 与 URLs, 145

- History API 的先前用法, 207

- 测试历史记录安全性, 225–228

## 用户输入，在 Web 表单上进行限制, 118–119

### `:valid` class, CSS3, 121

## 验证, HTML5 表单

- `email` input type, 99

- 概述, 95

- 使用`required`属性进行验证, 116

- 编写自己的验证规则, 117

## 验证器, HTML5, 4

## `value`属性, `progress`元素, 111–113

## vCard, Contact API, 391

## 验证网站, 67

## 版本号, `openDatabase` method, 285

## 垂直条形图，动画效果, 155–161

## `video`元素

- 基本用法, 163–166

- 浏览器兼容性, 164

- 自定义视频控件, 178–186

- 为所有浏览器启用视频, 166–167

- HTML5 与视频编解码器, 165

- 原生渲染视频, 163

- 新属性, 170–173

- 针对旧版浏览器, 167–169

## 使用 HTML5 嵌入视频

- 自定义控件, 178–186

- 为所有浏览器启用, 166–169

- 媒体 API, 177

- 新属性, 170–173

- 概述, 163

- 字幕和说明, 173–176

- 使用`video`元素, 163–166

## 视频播放器，可下载, 186

## 使用开发者工具查看存储, 265–266

## 视口，iPhone 和 Android, 76

## Vimeo, HTML5 与视频编解码器, 165–166

## 音量控制，流媒体广播, 198, 200, 202, 204–206

## 音量控制，视频, 180–183, 185

## VP8 (webM) 多媒体格式, 165–166

## `.vtt`文件 (WebVTT), 173–176

## W3C 验证器, 4

## W3C (万维网联盟)

- 开发 HTML5, xxiv

- 开发 XHTML 1.0, xxiii

- 设备 API 与策略工作组, 389–390

- HTML5 徽标与 W3C, xxvii

## WAI-ARIA (Web 可访问性倡议 - 无障碍富互联网应用), 49–51

## `watchID`参数, `clearWatch`, 250

## `watchPosition`方法, Geolocation API, 250–257

## `.wav`文件 (WAV) 音频编解码器, 188

## Web 可访问性倡议 - 无障碍富互联网应用 (ARIA), 49–51

## Web Applications 1.0, xxiv

## Web 表单

- 允许多次输入, 115–116

- 自动完成特性, 110–111

- 日历和时间控件, 102–105

- 拾色器, 107–108

- 联系信息, 97–101

- 自定义和样式化, 119–121

- 使用`output`元素显示结果, 108–109

- 错误消息, 121

- HTML4 input types, 95–97

- 页面加载时跳转到表单元素, 114–115

- 限制用户输入, 118–119

- 使用`meter`元素进行测量, 112–113

- 数字选择器, 105–106

- 占位符文本, 109–110

- 搜索表单, 101–102

- 注册表单, 121–125

- 滑块, 106–107

- 使用本地存储进行存储, 271–275

- 跟踪任务完成情况, 111–112

- 验证, 95, 116

- 验证规则, 117

#### Web Forms 2.0, HTML 历史, xxiv

#### Web Hypertext Application Technology Working Group (WHATWG), xxiv–xxv

#### Web Notifications API. 请参阅 Notification API

#### 离线网页, 337–340

## Web SQL Database API

- 概述, 283–286

- 用于杂货清单, 286–295

## Web 存储, HTML5 选项, 259–260

## Web worker

- 利用 Web Worker 跟踪推文, 353–356

- 推文通知, 349–353

## Web Workers API

- 创建 web worker, 304–307

- 定义, 297

- 利用共享 web worker, 311–318

- 最小化使用 web workers, 308

- 通过线程进行通信, 302–304

- 双向通信, 308–311

## WebKit 浏览器

- CSS 动画, 89

- 显示简单通知, 344

- 渐变语法, 81

- 输入类型与 WebKit, 61

- 搜索输入类型, 101–102

- 支持 Notification API, 341–343

#### `webkitEnterFullScreen`函数, 183, 185

#### `webkitNotifications`属性, `NotificationCenter`接口, 341

#### `webkitRequestFileSystem`, Chrome 12

- 创建本地文件, 383–388

- 定义, 381

#### webM (VP8) 多媒体格式, 165–166

#### 网站伪造, 225

#### WebSocket API, 297–302

#### `week` input type, 日历, 104–105

#### WHATWG (Web Hypertext Application Technology Working Group), xxiv–xxv

#### `width`值, `video`元素, 167

#### 通配符, manifest 的 `FALLBACK` 部分, 336–337

#### `.woff` (WOFF) 字体文件格式, 78

#### `Worker`接口, 303

#### Writer, File API 规范用于文件写入, 381–382

#### Writer 规范, File API, 381–382

#### `writeToFile`函数, 本地文件, 383, 385, 387

# X

## X 坐标, `canvas`

- 裁剪图像, 145–146

- 绘制`canvas`网格, 130–134

- 与`canvas`交互, 155

- 概述, 129

## XHTML (可扩展超文本标记语言), xxiii–xxiv

- 为旧版浏览器添加后备内容, 167–169

- HTML5 与视频编解码器, 165–166

# Y

## Y 坐标, `canvas`

- 裁剪图像, 145–146

- 绘制`canvas`网格, 130–134

- 与`canvas`交互, 155

- 概述, 129

# Z

## `z-index`样式属性, `canvas`, 150

## YouTube
