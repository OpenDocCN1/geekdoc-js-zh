# Angular 开发之旅：通过实践示例学习 Angular 基础、TypeScript、Webpack、路由、指令、组件、表单和模块（英文版）

# 献词

*致我挚爱的父母：纳格什·马拉和肖巴·马拉，
我的妻子：迪帕尔·马拉，
我的导师和祝福者：希夫普拉萨德·科伊拉腊*

*以及*

*我的 Just Compile 团队*

# 关于作者

我是**苏克什·马拉**，和你一样是一名开发者。让我快速简短地介绍一下我写这本书的历程。

**程序员**

我的职业生涯始于 2008 年，在一家名为 Pi Techniques 的公司担任 .net 开发人员。这是一个极好的开端——优秀的团队和优秀的公司。我的程序员生涯持续了大约 5.5 年。

那是我生命中最美好的时光之一。当一个人的爱好变成他的工作时，那简直就像在天堂一样。

在此期间，我开始从事在线技术写作，并加入了孟买的几个技术用户组。

**早期奖项与成就**

我对编程感到满意，但我一直知道缺少些什么。

我想做更大的事情。

*   我和希夫先生（我的导师）创办了一份名为《程序员》的报纸。
*   我积极参与了许多社区网络研讨会和研讨会，担任演讲者。
*   我参与了一些开源项目。

这些贡献使我多次获奖，包括来自 CSharp corner、CodeProject 和微软的 MVP 奖项。

**培训师与企业家**

最终，我冒险的头脑让我辞去了工作，并把我带入了企业培训和咨询的世界。我将我的公司命名为 Just Compile。

想知道为什么叫“Just Compile”吗？

老实说，这完全是随机的，没有什么特定的理论或原因。

我做了很多关于各种主题的培训——Asp.net、WCF、MSBI、jQuery、HTML 5、Angular JS、Angular、ReactJS、设计模式、Coded UI……等等。

（你注意到前面列表中 Angular 出现了两次吗？你困惑吗？别担心，等第一章就知道了。）

在那段时间里，我甚至完成了我的第一本书——《7 天学会 MVC》。

生活比以前好多了。现在我 100% 地投入到我的爱好中，并享受着每一刻。

**开发公司**

当我是一名培训师时，我想到招募一些新人并免费培训他们。我的想法是，如果有什么好的项目机会，那么它将打开一片机遇之地，因为那时我已经有了团队；否则，这将是社会公益。无论哪种情况，对我来说都是双赢。

于是，我雇佣了我的第一位员工和我亲爱的朋友图沙尔·洛内；随后是姆鲁纳利·萨旺特和迪佩什·辛德。

你猜怎么着？我甚至没有意识到，一个人的公司变成了 18 个人的公司。

我公司的成功故事是坚实的，这要归功于我的员工。

他们都说是我激励了他们，但事实是他们所有人都激励了我。

公司的业务和人才以火箭般的速度增长，而我却慢慢远离了写作。我甚至没有意识到这一点。

**从零到一百学习 Angular**

然后有一天，在与希夫先生交谈时，我意识到我偏离了自己真正擅长的事情。我本是一个通过写作与世界分享经验的作家。幸运的是，他总是在那里让我意识到自己的错误。

我从一开始就以培训师和程序员的身份接触 Angular 框架。我想开始写一本关于 Angular 的书，这就是你现在手中的这本书。

这本书的名字是——《从零到一百学习 Angular》。

**书名不同吗？**

嗯，说来话长。我对这本书有一个愿景。这个愿景最终改变了，书名也随之改变。那个完整的愿景需要不止一本书。也许很快，你会发现我写的一本或多本关于 Angular 的书。这将是本书的续集。你担心这本书不完整吗？完全不用担心。它是 100% 完整的。我计划写的另一本书将作为本书的增强包。

# 关于审阅者

**希夫普拉萨德·科伊拉腊**是微软和 JavaScript 技术领域著名的作者和培训师。他拥有约 20 年的跨国公司工作经验。他还曾连续 5 年担任微软 MVP，并撰写了畅销技术书籍，如《.NET 面试问题》。他大部分时间都在他的 YouTube 频道 Questpond 上讨论技术。他最近对频道突破 10 万订阅者感到非常兴奋。

# 致谢

我想感谢一些人，是他们成就了今天的我。首先，我要感谢我的父母。我仍然记得他们的辛勤工作和牺牲。我永远记得我的父母是如何仅凭每月 4000 印度卢比的工资供我上学和上大学的。

我生命中的每一次成就和成功，都源于我的导师和祝福者希夫普拉萨德·科伊拉腊的祝福。他总是相信我、鼓励我，并在遇到困难或痛苦时站在我身边。

人生中最大的幸运莫过于与最好的朋友结婚，对我来说，她就是迪帕尔·马拉。她持续的支持和信任让我意识到自己有多强大，以及我能做什么。

我还要感谢我的 Just Compile 团队。每家公司都能招到员工，而我却得到了一个新的家庭。他们给我的生活和目标赋予了特殊的意义。

我一直相信天赋。我认为每一种技能都值得赞扬。我希望我的学生能参与我的写作。我希望他们意识到自己有多么特别。因此，我请了几位学生为本书绘制插图。

本书所有图片的功劳归于姆鲁纳利·萨旺特、什拉达·瓦朗和迪拉杰·普贾里。

此外，特别感谢迪帕尔·马拉，她帮助我完成了本书的编辑工作。

# 前言

如果你正在阅读这本书，并且正在阅读这篇引言，这意味着你非常认真地想要学习 Angular。请保持这份专注。

**两个品质（坚持和努力）+ 这本书 = Angular 开发者**

这本书将与你迄今为止见过的所有其他书截然不同。我不会说它比其他书更好。我会说——它与大多数书不同。





想象一下，你即将开始一段火车之旅。你已经收拾好行李，正在站台等待列车进站。这趟列车将带你驶入 Angular 开发的世界。

![](img/Chapter-0-01.jpg)
**图 0.1：** 旅程开始

当你开始阅读第 1 章 – 打好基础的那一刻，你的旅程就开始了；当你完成第 1 章 – 打好基础时，你将抵达第 1 站。

每当你到达一个新站点，你都会发现自己在 Angular 技能方面焕然一新。你的最终目的地将是第 20 站。

## 路线图

正如我之前所说，这将是一段漫长的旅程。总共有 20 站，到最后，当你到达第 20 站时，你将足够强大，可以启动你的 Angular 项目，并称自己为一名 Angular 开发者。

![](img/Chapter-0-02.jpg)
**图 0.2：** 路线图

为了让这段旅程更有序、更高效，我将其划分为以下六个部分：

- **第 1 部分** – 本部分包含一章，让你只到达一个站点——**第 1 站**。在这一部分，我们将进行纯理论学习。我们将初步了解一些你在 Angular 学习过程中经常听到的术语。快速浏览这一部分即可。最多 1 到 1.5 小时就足够了。不要强求在这一章中掌握所有内容。之后，当你完成更多章节时，事情会变得容易得多，那时你可以回来复习。我建议你不要跳过这一部分和这一章。
- **第 2 部分** – 在这一部分，我们将讨论 `ES6` 并探索一些 `ES6` 特性。本部分共包含 4 章，带你从**第 1 站**到达**第 2 站**。如果你对 `ES6` 有一定了解，那么我强烈建议你跳过这一部分，直接开始下一部分。之后，如果你觉得直接跳到第 3 部分是个糟糕的主意，可以再回来复习这一部分。
- **第 3 部分** – 本部分包含两章，带你从**第 2 站**到达**第 4 站**。我们将在这部分讨论 `Webpack` 和 `TypeScript`。如果你愿意，可以跳过这两章。如果你觉得自己已经掌握了这些概念，或者认为已经掌握了基础知识并且足够用了，那就毫不犹豫地跳过吧。（你随时可以回来复习。）
- **第 4 部分** – 真正的旅程从这一部分开始，因为它包含四章，带你从**第 4 站**到达**第 8 站**。这将是 Angular 的起点。本部分将讨论如何创建一个 Angular 项目，包括引入第三方 CSS 库和身份验证。
- **第 5 部分** – 这一部分是所有部分中最大、最复杂、最具挑战性的部分之一。它只带你从**第 8 站**到达**第 10 站**，但总共包含 10 章。这一部分纯粹针对 Angular 服务。我建议你多次尝试本部分中的示例，并熟练掌握。
- **第 6 部分** – 最后一部分将带你从**第 10 站**到达**第 20 站**，共 10 章。本部分将涵盖 Angular 概念，最终让你成为一名 Angular 开发者。

## 本书的特色

写这本书对我来说是一次奇妙的经历，我保证你会享受其中的每一刻。只需保持耐心，专心致志地完成它。

本书的特色在于它不仅仅是概念性的。它更是一种**经验**。

我在 IT 行业已经工作了 12 年以上。我经历过许多技术上的起起落落。我从 Angular 的最初阶段就开始关注它。我第一次使用它时，它还处于测试版。到目前为止，我已经培训了许多 Angular 开发者，并且对许多复杂应用程序有丰富的实践经验。

考虑到所有这些，我在这些年积累的经验值得分享，而这正是我通过本书要做的事情。

## 本书将涵盖哪些内容？

通过本书，你一定会学会 Angular，但最棒的是，你将成为一名 Angular 开发者。

尽管这两句话看起来相同，但它们并不一样。你掌握了概念，但这并不意味着你能**开发一个项目**，也不意味着你能按照**行业最佳实践**来完成。正如我所说，在这本书中，我将分享我的经验。

## 如何最大化利用本书？

（截取这段说明，并在 Angular 学习过程中多次阅读。）

作为一名独立顾问，我经常需要处理各种技术。我不能花几个月或几年的时间去学习任何一门技术。它必须快速且完美。这让我明白了什么是真正的学习。遵循以下基本规则，相信我，你在学习 Angular 的道路上会快乐得多。

- 任何学习的首要黄金原则是：你不可能一次性学会所有东西。它需要多次迭代。因此，如果有必要，请多次阅读本书中的某些内容。
- 养成时不时复习前面章节的习惯。
- 一开始不要太担心理论概念。尽量理解你能理解的部分，然后转向实践。
- 如果有些东西不理解，不要过于担心。继续前进，将来再重新阅读。

试着回想你的学生时代。当你上七年级时，有些主题你一定觉得很难。但几年后，当你再看到那些七年级的主题时，你会觉得它们如此简单。

你有没有想过为什么？因为你的大脑现在已经适应了。你的思维已经习惯了处理更高级的事情；因此，过去的概念变得更容易、更轻松。

同样的原则适用于所有学习。一开始你可能会觉得某些主题很难。给自己一些时间继续前进。几天/几个月后，或者仅仅几个小时后，计划重新审视它，你会觉得它比以前容易理解得多。有些主题最终可能对你来说是个难题。完全没问题。继续前进。你会在项目中遇到一个情境，那时你就会明白那个主题到底是怎么回事。

因此，从本书中获益的最佳方式是——相信自己，时常复习，并诚实且反复地练习所有实验。不止一次地阅读解释。

其次，必要时走捷径。你的时间非常宝贵。正如我之前所说，明智地选择你的部分。如果需要，可以随意跳过第二和第三部分。

## 下载代码

请点击以下链接下载本书的 `代码包` 和 `彩色图片`：

[`rebrand.ly/w6r3u57`](https://rebrand.ly/w6r3u57)

## 勘误

我们在 BPB Publications 对自己的工作感到无比自豪，并遵循最佳实践确保内容的准确性，为读者提供沉浸式的阅读体验。我们的读者是我们的镜子，我们利用他们的反馈来反思和改进可能存在的任何人为错误（例如在出版过程中发生的错误）。为了让我们保持质量，并帮助那些可能因任何意外错误而遇到困难的读者，请写信至：

`errata@bpbonline.com`

BPB Publications 大家庭非常感谢您的支持、建议和反馈。




您是否知道 BPB 提供每本已出版图书的电子书版本，包含 PDF 和 ePub 文件？您可以升级到电子书版本，网址为 [www.bpbonline.com](http://www.bpbonline.com)。作为纸质书客户，您有权享受电子书折扣。如需了解更多详情，请通过 business@bpbonline.com 与我们联系。

在 [www.bpbonline.com](http://www.bpbonline.com) 上，您还可以阅读一系列免费技术文章，订阅多种免费新闻通讯，并享受 BPB 图书和电子书的独家折扣和优惠。

## BPB 正在寻找像您一样的作者

如果您有兴趣成为 BPB 的作者，请访问 [www.bpbonline.com](http://www.bpbonline.com/) 并立即申请。我们已与成千上万的开发者和技术专业人士合作，帮助他们与全球技术社区分享见解。您可以进行一般申请，申请我们正在招募作者的特定热门主题，或提交您自己的想法。

本书的代码包也托管在 GitHub 上，地址为 [`github.com/bpbpublications/A-Journey-to-Angular-Development`](https://github.com/bpbpublications/A-Journey-to-Angular-Development)。如果代码有更新，将在现有的 GitHub 仓库中更新。

我们还有来自丰富图书和视频目录的其他代码包，可在 [`github.com/bpbpublications`](https://github.com/bpbpublications) 获取。欢迎查看！

## 盗版问题

如果您在互联网上发现任何形式的非法复制我们作品的情况，我们将不胜感激，请提供位置地址或网站名称。请通过 business@bpbonline.com 联系我们，并附上相关材料的链接。

## 如果您有兴趣成为作者

如果您有擅长的主题，并且有兴趣撰写或参与一本书，请访问 [www.bpbonline.com](http://www.bpbonline.com/)。

## 评论

请留下评论。当您阅读并使用本书后，何不在您购买本书的网站上留下评论？这样潜在读者可以看到并利用您公正的意见做出购买决定，我们 BPB 可以了解您对我们产品的看法，我们的作者也能看到您对他们书籍的反馈。谢谢！

有关 BPB 的更多信息，请访问 [www.bpbonline.com](http://www.bpbonline.com/)。

# Angular 开发之旅
![](img/Image40710.jpg)

# 第 1 部分

## 第 1 章：夯实基础

## 引言

终于，漫长的等待结束了。火车刚刚抵达站台。请上车。它将带您前往第一站，让您的基础更加扎实。

计划如下：
1. 了解本系列课程的内容。
2. 学习与 Angular 学习相关的术语。
3. 理解 `Node.js` 在 Angular 应用开发中的作用。

![](img/Image40795.jpg)
**图 1.1**

这一站全是理论。不要急于一次性学完本章的所有内容。您可以在将来重新回顾并复习。放松心情，享受学习过程。

### 理解本系列课程的内容

在学习本系列课程的过程中，如果有人问您在学什么，请不要回答 `AngularJS`，因为本系列与 `AngularJS` 无关。这将是一个 Angular 系列课程。

![](img/Image40830.jpg)
**图 1.2**

### AngularJS 和 Angular？

首先，我们必须理解 Angular 和 `AngularJS` 是否相同。

如您所知，*电话* 和 *手机* 是两种不同的东西。

![](img/Image40838.jpg)
**图 1.3**

*电话* 很久以前就被引入世界，其目的是连接人们。它很好地完成了这项工作。

多年后，一种新设备问世，具有相同的核心目的，但更加便捷，并拥有许多出色的功能。它就是 *手机*。

*电话和手机是一样的吗？答案是否定的。*

对于 Angular 和 `AngularJS`，也可以考虑类似的答案。

`AngularJS` 是由 Google 团队创建的 *客户端框架*，用于 *单页应用开发*。

一段时间后，该框架的改进版本被推出。这个新版本强制执行了现代 UI 开发方法论（组件导向架构）。它在 *性能* 方面更好，代码也更加 *有组织且易于管理*。

它以一种全新的方法被引入。它被命名为 Angular，其第一个版本是 2.0。

**它们之间有任何相似之处吗？**

`AngularJS` 和 Angular 确实共享一些标准词汇/功能。在这两种技术中，您都会看到 `Directives`、`Pipes`、`Services` 以及许多其他标准功能。两者都共享 **单页应用** 的核心理念。这两种技术中的概念具有相似的想法，但语法完全不同。

**是否有从 AngularJS 应用迁移到 Angular 应用的路径？**

是的，有，它被称为 *重新创建*。😊

许多人可能会争辩说 `AngularJS` 应用可以迁移到 Angular 应用，但这实际上是一个神话。只有在试用或演示应用中才有可能。对于实时应用，这只是一个梦想。它们的编程风格和语法截然不同。

### 与 Angular 学习相关的术语

如果您以前尝试过学习 Angular，您一定遇到过一些令人兴奋的词汇，例如 `Node`、`TypeScript` 和 `ES6`。让我们讨论其中几个术语。

![](img/Image40875.jpg)
**图 1.4**

请注意，如果您觉得初始理论有点难以消化，请不要担心，放松并继续。一旦您开始进行实践实验，这些理论就会变得简单。

### JavaScript

可能很多人已经知道 JavaScript 是什么。它是一种编程语言，多年来一直被开发者用于 Web 应用中的客户端脚本。其主要目的是 DOM 操作。JavaScript 由浏览器在客户端执行，并操作客户端 DOM。

![](img/Image40917.jpg)
**图 1.5**

**与其他编程语言相比，JavaScript 有何不同？**

与大多数编程语言一样，JavaScript 不是编译型语言。它是一种动态的解释型语言。运行时环境（由浏览器提供）逐行执行代码，并在运行时出现任何问题时抛出错误。

让我们做一个演示来理解这一点。创建一个包含以下内容的 HTML 文件：

```html
<html>
<head></head>
<body>
     <script>
         console.log('A'); console.log('B');
         console.log('C'); console.log(ABCD);
         console.log('D'); console.log('E');
     </script>
</body>
</html>
```

现在，执行该 HTML 文件。（只需双击文件，在浏览器中打开。）

如您所见，尽管第四个 `console.log` 语句中存在错误，但前三行已成功执行。

如果是 `C#` 或 `Java`，我们会看到完全不同的输出。我们会遇到编译时错误。这就是 JavaScript。

![](img/Image40958.jpg)
**图 1.6**

### ES6

`ES6`、`ES2015` 和 `ECMA 2015` 都是相同的。最初，它被提议为 `ES6`，最终 `ES2015` 成为官方名称。通常，大多数人称其为 `ES6`，因此在本系列中我们将称其为 `ES6`。





这是一个新的 JavaScript 标准。该版本新增了许多功能和特性，旨在让 JavaScript 开发者的工作更轻松。在本系列中，我们将探讨其中的一些特性。

### 什么是单页应用？为什么需要它？

Gmail 和 Facebook 是这类应用中最著名的例子。让我们将传统 Web 应用与单页应用（SPA）进行比较。

![](img/Image41033.jpg)
**图 1.7**

![](img/Image41041.jpg)
**图 1.8**

对于 SPA 而言，性能会好得多。最终用户一开始会获得一个页面，并且这个页面会一直存在。用户后续执行的所有操作看起来都像是简单的 DOM 操作。某些内容动态显示，某些内容隐藏，一些新项目被创建，一些现有项目被移除，但整个 UI 永远不会刷新。这给人一种整个应用都在一个页面上开发的感觉。因此，它被称为 `单页应用`。

#### 它真的只包含一个页面吗？

但问题是，它内部真的只包含一个页面吗？我的意思是，你认为开发者实际上将整个应用开发成一个页面吗？答案是否定的。这是不可能的。

实际上，对于开发者来说，它是一个多页应用。他/她会在内部创建多个页面。然后，利用 `Ajax`、`CSS` 和 `JavaScript` 等概念，他/她营造出单页应用的外观，从而提升应用的整体用户体验。对于最终用户来说，它就是一个单页应用。

#### 创建 SPA 的挑战是什么？

使用 `原生 JavaScript` 进行 DOM 操作并不容易。这是社区给纯核心 JavaScript 语法（无第三方库）编写的代码起的名字。

用纯 `原生 JavaScript` 创建实时 Web 应用将充满挑战，因为我们必须编写大量 JavaScript 才能实现。其次，我们还需要关注浏览器兼容性。

像 `jQuery` 这样的库让 DOM 操作变得非常容易。

#### 仅靠 jQuery 或其他 DOM 操作库就足以创建 SPA 吗？

试想一下，为了创建一个 SPA，我们需要编写多少 JavaScript——所有 DOM 操作都将在客户端完成。服务器端代码将仅限于业务逻辑和数据。

如果我们为此使用 `原生 JavaScript` 或像 `jQuery` 这样的库，代码将变得难以管理，因为代码中没有强制性的关注点分离。随着应用规模的增长，JavaScript 代码会越来越庞大，越来越难以管理。

我并不是说我们不能使用 `jQuery` 或其他 DOM 操作库来创建 SPA。我们可以，但过多的 JavaScript 代码会使代码变得不可管理。我们需要某种标准且结构化的 UI 开发方式。

你一定听说过服务器端技术中的架构模式，如 `MVC` 或 `MVVM`，它们为应用的不同逻辑区域提供了清晰的分离。它们明确回答了“什么该放在哪里？”以及“什么与什么通信”。当应用采用此类架构开发时，代码更易于管理。

使用 `jQuery`，我们只能获得一些让 DOM 操作更轻松的方法，但代码管理和架构呢？你不觉得我们在客户端也需要一种更结构化的方法吗？尤其是当我们知道最终会编写大量 JavaScript 代码时。

所以，当前问题的答案是：不。`jQuery` 不足以构建 SPA。我们需要更多。我们需要某种框架，它能在 UI 世界中强制采用结构化的编码方式。

## 什么是 Angular？

Angular 是由 Google 创建的客户端框架。请注意，它不是 JavaScript 的替代品。它是一个 JavaScript 框架。

**注意：它不是库，而是框架。**
**框架是一个比库更宏大的概念。**

![](img/Image41079.jpg)
**图 1.9**

它提供了开发所需的全面平台。该平台可能包含一些可重用的库以简化工作，但它还可能提供许多其他东西，例如编译器、执行环境。它甚至可能强制你在编码时遵循某种固定的结构。

Angular 框架就像 `jQuery` 一样，让 DOM 操作变得非常容易，但它还为你提供了 UI、UI 逻辑、表示逻辑和应用逻辑之间的清晰分离。

Angular 还强制我们以可重用且可组合的 Web 组件的形式来开发整个 UI 应用。这被称为组件导向架构。这是 `HTML 5` 推荐的 UI 开发标准方式。

简而言之，Angular 是一个用于创建 SPA 的客户端框架。

### 什么是 Node.js？

当我第一次学习 Angular 时，我感到相当困惑。我想知道 `Node.js` 在这里做什么，我相信很多人也有类似的困惑。

在深入探讨“`Node.js` 在 Angular 应用开发中扮演什么角色？”这个问题之前，我们先来理解一下 `Node.js` 是什么。

它是执行 JavaScript 代码的运行时。这意味着，我们现在可以编写在浏览器之外运行的 JavaScript 代码。借助 `Node.js`，我们可以使用 JavaScript 语言创建其他类型的应用，例如桌面应用，甚至是可以响应 `HTTP` 请求的服务器等。

### 安装

你可以从以下链接下载最新版本的 `Node.js`：
[`Node.js.org/en/download/`](http://Node.js.org/en/download/)

### 确认安装成功

要确认安装是否成功，请打开命令提示符，并依次执行以下两个命令：

1. `node` 命令
你应该会看到以下输出：
![](img/Image41086.jpg)
**图 1.10**

2. `npm` 命令
![](img/Image41156.jpg)
**图 1.11**

按 `Ctrl` + `C` 两次退出 `node` 命令，然后执行 `npm` 命令：

通常，Node 安装过程也会更新系统中的环境变量。有时，由于某些系统安全问题，它可能无法更新环境变量。如果更新失败，你可能会看到以下错误：

* `node` 未被识别为内部或外部命令。
* `npm` 未被识别为内部或外部命令。

在这种情况下，请确保手动更新。打开 `控制面板 >> 系统和安全 >> 系统`，然后参考以下两幅图：

**更新路径**：
![](img/Image41218.jpg)
**图 1.12**

**更新系统路径**：
![](img/Image41225.jpg)
**图 1.13**

#### Node 控制台应用的快速演示

打开你喜欢的文本编辑器，编写以下代码：

```javascript
var a=10;
var b=20;
console.log(a+b);
```

将文件保存为 `firstnode.js`。

现在，打开命令提示符。导航到保存文件的文件夹，并执行以下命令：

```bash
node firstnode.js
```

你将看到以下输出：
![](img/Image41308.jpg)
**图 1.14**

如你所见，JavaScript 代码在没有浏览器的情况下执行了。

这是一个简单的 `Node.js 应用` 演示。

Node 运行时能理解所有 JavaScript 关键字（除了 UI 特定的关键字，如 `alert` 或 `document`），并知道如何执行它们。`Node.js` 甚至能理解新的 `ES6` 特性，以及在一定程度上理解 `ES7`（将在 `ES6` 之后引入的版本）。

（这是一个快速演示，展示使用 `Node.js` 可以在没有浏览器的情况下执行 JavaScript。）

### 什么是 npm？

当我们谈论应用时，我们会有依赖项。




例如，假设我们正在开发一个名为 `App1` 的应用程序，并且想要使用一个名为 `dep1` 的第三方模块。`dep1` 依赖于另外两个第三方模块 `dep2` 和 `dep3`。而 `dep3` 又依赖于 `dep4`。

现在，这里的挑战是，作为 `App1` 的开发者，我们有责任下载 `dep1` 以及 `dep2`、`dep3` 和 `dep4`。

简而言之，我们需要对整个依赖层级有完整的了解。我们还需要确保下载正确的版本。例如，`dep2` 的最新版本是 3.5，而 `dep1` 需要 `dep2` 的 `2.3` 版本。

这工作量是不是太大了？一个简单的解决方案就是包管理器。它是一种软件工具，可以简化依赖项的管理。你会发现几乎所有技术中都有包管理器的概念。在 Java 中，我们有 Maven；在 .net 中，我们有 Nuget；在 Python 中，我们有 Pep。Node 也有自己的包管理器，那就是 `npm`。

使用 `npm`，我们可以从 `npm` 注册表（称为 node modules）下载各种 JavaScript 包。

npm 注册表是一个在线数据库，其中保存着 node modules。

这些 node modules 既包括可重用的库，也包括实用工具。库可以用于某些应用程序，而实用工具则可以执行一些自动化任务。

### 使用 npm 下载 JavaScript 库

为了演示这一点，让我们使用 `npm` 下载 `jquery`。为此，打开命令提示符，并执行以下命令：

1. `npm install jquery`

现在，打开你执行上述命令的文件夹。你会发现在其中创建了 `node_modules` 文件夹。在 `node_modules` 文件夹内，你会找到 jQuery。

如你所见，使用 npm 工具，我们可以从 npm 注册表下载可重用的库。就像 jQuery 一样，我们可以使用 npm 轻松下载 Angular、ReactJS 等其他库。

### 使用 npm 下载实用工具

JavaScript 包（也称为 node modules）并不仅限于第三方库。它们也可以是某些可执行应用程序。

例如，我们有一个名为 `webpack` 的 node module，它可以让我们将所有 JS 文件打包成一个单独的 `js` 文件。什么是 *打包*，什么是 *webpack* 等等……现在不必担心这些问题。我们很快就会讨论。

现在，让我们演示一下下载一个可执行应用程序的 node module。

只需执行以下命令：

1. `npm install -g @just-compile/jc_calc`

你可能会注意到 `npm install` 中添加了一个属性 `-g`。这意味着我们正在全局安装我们的 node modules。（我们稍后会讨论全局安装和本地安装的区别。）

（在 Windows 机器上，你可以在 `C:\Users\{username}\AppData\Roaming\npm` 找到安装位置。）

一旦上述命令执行完毕，我们将获得一个新的 CLI 命令 `add_jc_calc`。让我们使用它。

1. `add_jc_calc 8 9`

你将得到以下输出：

1. `17`

## 什么是 package.json？

它是一个简单的文本文件，包含关于 `Node.js` 应用程序的元数据信息。

它位于应用程序的根目录中。

使用它有以下三个优点：

1. 提供关于我们的包或应用程序的元数据信息。
2. 跟踪应用程序的依赖项。
3. 创建 npm 脚本。

### package.json 如何保存关于我们的包或应用程序的元数据信息？

让我们从创建 `package.json` 开始。可以使用任何文本编辑器或 npm 工具手动创建它。

打开命令提示符，导航到某个文件夹，并执行以下命令：

1. `npm init`

它会询问一些输入。

请参考下图：

![](img/Image41366.jpg)

**图 1.15**

在最后的提示中，输入 `yes`，然后按 *Enter* 键。在文件资源管理器中打开该文件夹，你会注意到 `package.json` 已在该文件夹中创建，内容如下：

```
{
   “name”: “myapp”,
   “version”: “1.5.1”,
   “description”: “trying package.json for learning”,
   “main”: “index.js”,
   “scripts”: {
     “test”: “echo \”Error: no test specified\” && exit 1”
   },
   “author”: “sukesh marla”,
   “license”: “ISC”
}
```

如你所见，`package.json` 包含关于我们应用程序的大量信息，这就是第一个优点——保存应用程序的元数据。

### package.json 如何用于跟踪应用程序的依赖项，以及它的好处是什么？

首先，让我们回答为什么要跟踪应用程序的依赖项，然后再回答如何跟踪。

假设一个系统依赖于三个外部库——`jquery`、`systemjs` 和 `core-js`。

每个库都可以使用以下 `npm install` 命令下载：

1. `npm install jquery`
2. `npm install systemjs`
3. `npm install corejs`

现在，说到应用程序，会有多个开发者。每个开发者都需要一份源代码副本。因此，建议将整个源代码保存在某种源代码控制仓库中，例如 GitHub、Bitbucket 等。

按照最佳实践，库文件不会包含在源代码控制仓库中；因此，每个开发者都需要使用 `npm` 单独下载它们。

![](img/Image41420.jpg)

**图 1.16**

这种方法的问题是，每个开发者都需要下载每个文件。在上面的例子中，只有三个库，但在某些情况下，可能有 100 个。在这种情况下，他/她很有可能会忘记下载某些库。

解决上述问题的方法是 `package.json`。请按照以下步骤操作：

1. 按照上一节所述的方式创建 `package.json`（即 `npm init`）。
2. 依次执行以下命令：
   a. `npm install jquery --save`
   b. `npm install systemjs --save`
   c. `npm install corejs --save`

请注意每个安装命令中添加的额外 `--save` 标志；它会在 `package.json` 中创建一个名为 dependencies 的新部分，如下所示：

```
{
   “name”: “myapp”,
   “version”: “1.5.1”,
   “description”: “trying package.json for learning”,
   “main”: “index.js”,
   “scripts”: {
     “test”: “echo \”Error: no test specified\” && exit 1”
   },
   “author”: “sukesh marla”,
   “license”: “ISC”,
   “dependencies”: {
     “corejs”: “¹.0.0”,
     “jquery”: “³.4.1”,
     “systemjs”: “⁶.2.5”
   }
}
```

现在，删除 `node_modules` 文件夹，然后执行 `npm install` 命令（在 `package.json` 文件所在的文件夹中）。你会注意到所有依赖项将一次性下载完成。

1. `npm install`

就是这样。`package.json` 会保存所有依赖项的列表，每个开发者只需执行该命令，就能获得所有库。通过这种方式，我们实现了两个要求：

1. 库不作为源代码控制的一部分保存。
2. 没有人需要记住系统中需要哪些库。

![](img/Image41427.jpg)

**图 1.17**

### 如何创建 npm 脚本以及它的目的是什么？

我们已经演示了如何使用 `npm install` 安装第三方 `node_modules`。





### 全局与本地 Node 模块

我们之前已经演示了可执行 Node 模块的用法，但还没有讨论 `npm install` 命令中使用的 `-g` 标志。使用 `-g` 标志安装 Node 模块会将其安装为全局 Node 模块，这样所有应用程序都可以使用它；而如果不使用 `-g` 标志，则会安装为本地（特定于应用程序的）Node 模块。这些本地模块无法直接在命令提示符中执行，我们需要使用 npm 脚本来实现。

下面我们做一个演示。

**步骤 1：** 使用 `npm init` 创建 `package.json`。

**步骤 2：** 为了演示，我们将使用相同的 `@just-compile/jc_calc` 包。

首先，使用以下命令卸载全局模块：
`npm uninstall -g @just-compile/jc_calc`

请确保在上述命令中不要遗漏 `-g` 标志。

现在，将其本地安装如下：
`npm install @just-compile/jc_calc`

**步骤 3：** 现在执行以下命令：
`add_jc_calc 8 9`

你将看到以下错误：
`‘add_jc_calc’ 不是内部或外部命令，也不是可运行的程序或批处理文件。`

由于该包未全局安装，你无法在命令提示符中直接使用 `add_jc_calc` CLI。我们需要一个 npm 脚本来执行本地模块。

**步骤 4：** 打开 `package.json`，并按如下方式添加/修改脚本部分：

```json
{
  "name": "myapp",
  "version": "1.5.1",
  "description": "尝试使用 package.json 进行学习",
  "main": "index.js",
  "scripts": {
    "add": "add_jc_calc"
  },
  "author": "sukesh marla",
  "license": "ISC"
}
```

**步骤 5：** 现在，在命令提示符中，使用以下命令立即执行 npm 脚本：
`npm run add 8 9`

你将看到以下输出：
```
C:\SukeshRND\node\package>npm run add 9 9
> package@1.0.0 add C:\SukeshRND\node\package
> add_jc_calc “9” “9”
18
```

执行本地 Node 模块并不是 npm 脚本的唯一用途。有时，我们可能会遇到一些复杂且需要多次使用的命令。与其多次重复编写这些复杂命令，不如创建指向这些复杂命令的 npm 脚本。

## Webpack

你能想象一个只有一个 JavaScript 文件的实时 Web 应用程序吗？我认为你无法想象。实际项目总是会有大量的 JavaScript 文件。你能想象手动引入所有这些 JavaScript 文件吗（尤其是在单页应用的情况下）？那将是巨大的开销。

### 模块加载器

一种解决方案是使用模块加载器。模块加载器是一种在运行时动态加载 JavaScript 文件的库。此类模块加载器的一个例子是 `systemjs`。

模块加载器可以通过 `npm` 直接下载。例如，要下载 `systemjs`，请使用以下命令：
`npm install systemjs`

![](img/Image41487.jpg)
**图 1.18**

模块加载器的问题在于性能。在运行时加载 JavaScript 文件会影响性能。在未来的某篇文章中，我们将看到模块加载器的一个很好的演示。所以现在，只需尝试理解模块加载器的概念即可。

## 模块打包器

模块打包器是一种 Node 模块，它接收一个 JavaScript 文件作为输入，然后识别该输入文件所依赖（直接或间接）的所有其他 JavaScript 文件，最后将所有文件合并并生成一个单一的 JavaScript 文件。它以不影响这些 JavaScript 文件内部逻辑的方式将它们合并在一起。

生成的这个打包文件将被包含在 HTML 文件中。

![](img/Image41543.jpg)
**图 1.19**

**模块打包器和模块加载器如何理解依赖关系？**
现在不必担心这个问题。当我们计划使用模块打包器或模块加载器时，我们会按照某些标准编写代码。目前，只需相信在每个 JavaScript 文件中，我们都会以某种方式指定与其他 JavaScript 文件的依赖关系。

**只有一个 JavaScript 文件不会影响性能吗？**
它反而会提升性能，因为它将多个请求调用替换为单个请求。如果打包文件太大，我们可以配置模块打包器创建多个按功能划分的打包文件。

**Webpack 是模块打包器吗？**
是的，`webpack` 是一个模块打包器，但它并不是唯一的打包器。还有其他的，比如 `Browserify`。我们将在后续的一篇文章中演示 webpack。

**模块打包器只打包 JavaScript 文件吗？**
不，它也可以打包 CSS 文件。

## 什么是 TypeScript？为什么使用它？

让我们通过回答几个更具体的问题来理解这一点。

*   **什么是 TypeScript？**
    它是一种编程语言。
*   **它有什么作用？**
    与大多数编程语言一样，TypeScript 是一种带有编译器的语言。TypeScript 编译器是一个可以通过 `npm` 下载的 Node 模块。编译后，它会生成 JavaScript 代码。
    ![](img/Image41583.jpg)
    **图 1.20**
*   **在哪里可以使用 TypeScript？**
    TypeScript 可以用于任何可以使用 JavaScript 的地方。你可以编写 TypeScript 代码，编译它，然后使用生成的 JavaScript 代码，而不是直接编写 JavaScript。
*   **为什么我应该用 TypeScript 而不是 JavaScript 编写代码？**
    使用 TypeScript 而不是 JavaScript 编写代码会让你的工作更轻松。它会为我们提供一个类型安全的环境来编写代码（这在 JavaScript 中是不可能的），此外，它还具备一些让程序员生活更轻松的特性。
*   **学习一门新语言不是一种负担吗？**
    对于任何 JavaScript 开发者来说，学习 TypeScript 语言都非常容易。TypeScript 语言的语法继承自 JavaScript。
    *   在 TypeScript 中声明变量和函数、赋值以及许多其他操作的语法与 JavaScript 相同。
    *   在 JavaScript 中能实现的所有功能，在 TypeScript 中同样可以实现。
    *   JavaScript 中的每个函数在 TypeScript 中都有对应的版本。例如，`alert`、`document.getElementById`、`console.log` 等函数在 TypeScript 中同样可以使用。
    任何 JavaScript 代码都可以直接从 JavaScript 文件中复制并粘贴到 TypeScript 文件中，并且会被视为 TypeScript 代码。
*   **TypeScript 中的 ES6 特性呢？**
    我们很快就会介绍 ES6 特性。如果你正在使用 TypeScript，那么好消息是 TypeScript 具有类似的特性。
    ![](img/Image41643.jpg)
    **图 1.21**
    事实上，TypeScript 还拥有额外的特性（例如：装饰器、泛型）。
*   **TypeScript 编译后会生成什么样的 JavaScript 代码？**
    这取决于我们使用的 TypeScript 特性以及我们期望的输出目标版本。TypeScript 编译器提供了指定期望输出的 JavaScript 目标版本的选项。如果 TypeScript 特性在 JavaScript 目标版本中可用，则会生成完全相同的代码。如果 TypeScript 特性在目标 JavaScript 版本中不可用，TypeScript 编译器将生成相应的逻辑。
*   **TypeScript 在 Angular 学习中扮演什么角色？**
    正如我之前所说，Angular 是一个 JavaScript 框架。要使用 Angular 创建应用程序，我们需要编写大量的 JavaScript 代码。我们知道，使用 TypeScript 语言而不是 JavaScript 语言编写代码会让我们的工作更轻松。因此，建议使用 TypeScript 语言创建 Angular 应用程序。




这只是对 TypeScript 的快速概述。我们有一篇专门针对 TypeScript 的详细文章。

### Node.js 在 Angular 应用开发中的作用

许多刚开始学习 Angular 的人会对 Node.js 感到困惑。他们误以为需要掌握 Node.js 才能学习 Angular。

让我们澄清这个困惑。你不需要成为 Node 专家就能学习 Angular。

我们不会在 Angular 应用中编写任何一行 Node.js 代码。

**那么，我可以在对 Node.js 了解不多的情况下创建 Angular 应用吗？**

是的，完全可以。

但这并不意味着我们完全不需要 Node.js。

*   我们会安装 Node.js。
*   使用 `npm`，我们将下载一个第三方 node 模块，并用它来创建 Angular 应用（我们将在后续文章中详细讨论）。
*   我们可能会根据需要，使用 `npm` 下载一些额外的 node 模块。
*   我们可能会使用一些 `npm scripts` 来简化开发、构建和部署。

作为 Angular 开发者，你应该了解 `npm`、`package.json`、`npm scripts` 以及 node 模块的概念。这些就足够了。

#### 总结

好了，我们已经到达了第一站。稍作休息，放松一下。

到目前为止，更多的是理论学习。我保证，接下来会更有趣，也更具挑战性。

让我们列出本章学到的内容：

*   我们探讨了学习 Angular 时每天都会听到的各种术语：
    *   Angular JS
    *   Angular
    *   ES5
    *   ES6
    *   ES2015
    *   SPA
    *   Node.js
    *   `npm`
    *   `package.json`
    *   模块打包器
    *   模块加载器
    *   Webpack
    *   TypeScript
*   我们了解到 Angular 和 Angular JS 并不相同。它们是两种不同的技术，并且没有迁移路径。
*   我们快速回顾了 JavaScript，作为一种编程语言，它多年来一直被用于 Web 应用的客户端脚本。其主要目的是 DOM 操作。JavaScript 由浏览器在客户端执行，并操作客户端 DOM。
*   我们还了解到 JavaScript 不是编译型语言，而是解释型语言。
*   我们介绍了 ES6（又称 ES2015、ECMA 2015），这是一个新的 JavaScript 标准。（当你阅读本书时，可能已经推出了更新的版本。）
*   我们学习了 SPA，并了解了它如何改善用户体验。我们还了解到 SPA 并不是只有一个页面的应用。
*   我们了解到 Angular 是 Google 的一个框架，旨在以组件化风格创建 SPA。我们了解到它并不是 JavaScript 的替代品，而是一个 JavaScript 框架。
*   我们讨论了 Node，并了解到它为 JavaScript 应用提供了执行环境。
    *   现在我们可以在没有浏览器的情况下执行 JavaScript 代码。
    *   我们澄清了一个事实：深入学习 Angular 并不需要 Node.js 知识。
    *   作为 Angular 开发者，你应该了解 `npm`、`package.json`、`npm scripts` 以及 `node_modules` 的概念。这些就足够了。
*   我们学习了 `npm`，它是一个 Node 包管理器。
    *   使用它，我们可以将第三方 node 模块安装到我们的应用中。
    *   它还能帮助我们执行 node 脚本。
*   我们学习了 `package.json`，它是 `npm` 命令的配置文件。
    *   使用它，我们可以定义包或应用的元数据信息。
    *   使用它，我们可以跟踪应用的依赖关系。
    *   使用它，我们可以创建 `npm scripts`。
*   我们讨论了模块加载器和模块打包器。
*   我们了解到 Webpack 是 Angular 内部使用的模块打包器。
*   我们讨论了 TypeScript，并了解了它是什么以及为什么使用它。

# 第二部分

## 第 2 章：ES6 特性 – 第一部分

## 引言

希望你喜欢第一站的旅程。通过那段旅程，我们讨论了与 Angular 学习相关的各种术语，例如 Node.js、`npm`、TypeScript 等。

现在，我们身处第一站。我说，吃完你的早餐/午餐/晚餐，然后再次登上火车，因为我们将开始前往第二站的旅程。确保你已经准备好编码工具。这次，我们将进行大量的编码。

这次，全部是关于 ES6 的内容。我们将其拆分成多篇文章，这样就不会有人被一篇冗长的文章吓到。

### 规划执行环境

我们将学习 ES6，这意味着我们在学习更多的 JavaScript——因此我们需要一个执行环境。

让我们试着回忆一下 JavaScript 有哪些运行时环境。我们有浏览器，还有 Node.js。我们会根据情况随机使用它们，看哪种最合适。

事不宜迟，让我们开始探索 ES6 的特性。

## 变量声明

到目前为止，我们一直使用 `var` 关键字在 JavaScript 中声明变量。现在有了 ES6，我们有了两种新的方式：`let` 和 `const`。让我们做一些演示来理解传统方式中的问题。

#### 传统方式

**演示 1**

创建一个 JavaScript 文件 `Variable_Declaration.js`，包含以下代码块：

```javascript
//Demo 1
console.log(a);
```

现在，花点时间思考一下，如果执行上述代码，输出会是什么。

打开命令提示符，导航到上述文件所在的文件夹，并使用 `node` 命令执行它。由于变量未定义，我们将得到运行时错误。

![](img/Image41758.jpg)
**图 2.1**

**演示 2**

现在将代码替换为以下代码，并尝试输出：

```javascript
var a;
console.log(a);
```

![](img/Image41766.jpg)
**图 2.2**

同样，这是非常预期的输出。在 JavaScript 中，如果变量被声明但从未赋值，默认值为 `undefined`。

**演示 3**

```javascript
//Demo 3
console.log(a);
var a;
```

![](img/Image41766.jpg)
**图 2.3**

现在预期输出是什么？逻辑上，我们应该得到“未定义错误”，因为我们在变量声明之前使用了它。让我们看看会得到什么。

![](img/Image41840.jpg)
**图 2.4**

为什么我们得到了 `undefined`？

在 JavaScript 中，使用 `var` 关键字声明的变量会被提升。这个概念称为“提升”。无论你在哪里声明变量，它总是被视为顶级变量。简单来说，所有变量声明都会被提升到顶部。

**演示 4**

```javascript
//Demo 4
console.log(a);
var a=8;
```

输出仍然是 `undefined`，因为我说的是变量声明被提升，而不是赋值。你可以将上述代码视为三步代码：

```javascript
//Demo 4
console.log(a);
var a;
a=8
```

只有第二行（即 `var a;`）被提升。

**演示 5**

接下来，尝试以下代码：

```javascript
//Demo 5
console.log(a);
if(false) {
   var a;
}
```

![](img/Image41766.jpg)
**图 2.5**

这次我们不应该得到运行时错误吗？如果不是 JavaScript，我们可能会说“是”，因为变量是在 `if` 块内部声明的。

JavaScript 不支持块级变量（至少在使用 `var` 关键字声明时），因此所有在条件或迭代块内部声明的变量都会获得外部作用域。由于变量被提升，我们得到 `undefined` 作为输出。

**演示 6**




你必须清楚，使用 `var` 关键字声明的变量会提升（hoisting），并且不会被视作块级变量。让我展示一个因这种行为导致的实际问题。

假设我们有以下现有代码：

```javascript
//Demo 6
var a=10;
console.log(a);
if(true) {
    //Some logic
}
console.log(a);
```

两个 `console.log` 的输出都是 10。

现在，想象一下应用程序的一个新变更要求在 if 块内添加更多代码。新开发者对现有代码不太了解。

假设他做了修改，最终得到以下代码：

```javascript
//Demo 6
var a=10; // 旧代码 - 未受影响
console.log(a); // 旧代码 - 未受影响 - 期望输出 10
if(true){
    //Some logic
    var a=9; // 新代码
    console.log(a); // 新代码 - 未受影响 - 期望输出 9
}
console.log(a); // 旧代码 - 未受影响 - 期望输出 10
```

![](img/Image41924.jpg)
**图 2.6**

使用 `node` 执行它并检查结果。

新代码也影响了现有代码。

![](img/Image41963.jpg)
**图 2.7**

我知道你感到沮丧，因为这有点令人困惑且出乎意料。别担心。这就是为什么 ES6 引入了一种新的变量声明方式。

### 使用 var 关键字创建私有变量

为此，我们需要创建函数。函数有自己的作用域。

```javascript
//Demo 7
console.log(a);
myFunction();
function myFunction(){
    var a;
}
```

![](img/Image42000.jpg)
**图 2.8**

如你所见，变量 `a` 在函数外部不可访问。这是在 JavaScript 中使变量私有的一种合理方式。

### 新方式

ES6 的 `let` 关键字将解决 `var` 关键字带来的所有问题。

创建另一个文件 `Variable_Declaration2.js`，包含以下代码：

# 演示 1
```javascript
//Demo 1
console.log(a);
let a;
```

![](img/Image42042.jpg)
**图 2.9**

现在它强制我们在使用变量之前先声明。简而言之，现在没有提升。

# 演示 2
```javascript
//Demo 2
if(true){
   let a;
}
console.log(a);
```

![](img/Image42086.jpg)
**图 2.10**

如你所见，现在变量被视为块级变量。

#### 演示 3
```javascript
//Demo 3
let a=10; // 旧代码 - 未受影响
console.log(a); // 旧代码 - 未受影响 - 期望输出 10
if(true){
    //Some logic
    let a=9; // 新代码
    console.log(a); // 新代码 - 未受影响 - 期望输出 9
}
console.log(a); // 旧代码 - 未受影响 - 期望输出 10
```

![](img/Image42130.jpg)
**图 2.11**

当变量使用 `let` 关键字声明时，生活就简单了。

### 常量变量

ES6 也支持常量变量。

创建一个 JavaScript 文件 `Constant_Declaration.js`，包含以下代码块：

```javascript
const c=10;
c=20
console.log(c);
```

使用 `node` 命令执行它。

![](img/Image42170.jpg)
**图 2.12**

如你所见，当我们试图改变变量的值时，得到了一个错误。

（它与 `let` 关键字有相似的行为，即没有提升，变量被视为块级变量，但不允许改变值。）

### 面向对象编程

有了 ES6，JavaScript 世界支持类。

在 ES6 之前，JavaScript 中的面向对象编程并不直接。我们使用诸如 IIFE、闭包和构造函数等逻辑概念来实现面向对象风格的编码。ES6 引入了 `class` 关键字来创建类，就像其他编程语言一样。

# 演示 1
创建一个新的 JavaScript 文件，命名为 `oops.js`，内容如下：

```javascript
class Customer{
   Save(){
       console.log(“Customer Saved: “+this.CustomerName+”(“+this.Designation+”-”+this.CompanyName+”)”);
   }
}

let c=new Customer();
c.CustomerName= ‘Sukesh Marla’;
c.Designation= ‘Director’;
c.CompanyName= ‘Just Compile’;
c.Save();
```

让我们分析代码：
- 使用 `class` 关键字创建类。
- 使用 `new` 关键字创建类的实例。
- 使用点（`.`）运算符访问类成员。
- 在类内部，使用 `this` 关键字访问成员。

对于任何面向对象程序员来说，这都是简单的代码。

由于 JavaScript 是一种动态语言，无需在类内部显式声明 `CustomerName` 和其他成员变量。当执行语句 `c.CustomerName = ‘SukeshMarla’` 时，类成员在运行时被创建。

让我们使用 `node` 命令执行代码：

![](img/Image42246.jpg)
**图 2.13**

# 演示 2
在演示 2 中，我们将学习如何创建构造函数。

在 JavaScript 中，构造函数语法非常不同。这里，我们不遵循“类名和构造函数名应匹配”的规则；相反，创建构造函数时使用 `constructor` 关键字。

```javascript
//Demo2
class Customer{
   constructor(CustomerName,CompanyName,Designation){
       this.CustomerName=CustomerName;
       this.CompanyName=CompanyName;
       this.Designation=Designation;
   }
   Save(){
       console.log(“Customer Saved: “+this.CustomerName+”(“+this.Designation+”-”+this.CompanyName+”)”);
   }
}

let c=new Customer(“Dipesh Shinde”,”CEO”,”Just Compile”);
c.Save();
```

![](img/Image42253.jpg)
**图 2.14**

#### 演示 3
接下来，让我们做一个简单的继承示例。

```javascript
//Demo 3.1
class Customer{
   constructor(CustomerName,CompanyName,Designation){
       this.CustomerName=CustomerName;
       this.CompanyName=CompanyName;
       this.Designation=Designation;
   }
   Save(){
       console.log(“Customer Saved: “+this.CustomerName+”(“+this.Designation+”-”+this.CompanyName+”)”);
   }
}
class GoldCustomer extends Customer{
}

let c=new GoldCustomer(“Parvez”,”Siddiqui”,”Technical Architect”);
c.Save();
```

我们在 JavaScript 中使用 `extends` 关键字进行继承。

你注意到了吗？`GoldCustomer` 类中没有定义任何构造函数，但我们在创建实例时传递了三个参数。

嗯，这对于像 C++ 或 C# 这样的静态语言程序员来说是一种新行为。

执行后，你将得到以下输出：

**你在想发生了什么吗？**

![](img/Image42295.jpg)
**图 2.15**

基类构造函数被调用了。

现在，让我们在派生类中创建一个空构造函数，并检查行为。

```javascript
//Demo3.2
class Customer{
   constructor(CustomerName,CompanyName,Designation){
       this.CustomerName=CustomerName;
       this.CompanyName=CompanyName;
       this.Designation=Designation;
   }
   Save(){
       console.log(“Customer Saved: “+this.CustomerName+”(“+this.Designation+”-”+this.CompanyName+”)”);
   }
}
class GoldCustomer extends Customer{
   constructor(){}
}
let c=new GoldCustomer(“Parvez”,”Siddiqui”,”Technical Architect”);
c.Save();
```

![](img/Image42340.jpg)
**图 2.16**

输出将是一个错误。

规则说，在继承中，如果派生类有构造函数，“派生类构造函数必须显式调用基类构造函数。”

让我们来做。

```javascript
//Demo3.3
class Customer{
```





```
   constructor(CustomerName,CompanyName,Designation){
       this.CustomerName=CustomerName;
       this.CompanyName=CompanyName;
       this.Designation=Designation;
   }
   Save(){
       console.log(“Customer Saved: “+this.CustomerName+”(“+this.Designation+”-”+this.CompanyName+”)”);
   }
}
class GoldCustomer extends Customer{
   constructor(){
       super();
   }
}

let c=new GoldCustomer(“Parvez”,”Siddiqui”,”Technical Architect”);
c.Save();
```

让我们检查输出。

![](img/Image42416.jpg)

**图 2.17**

**对输出感到疑惑？我们来理解一下。**

*   `GoldCustomer` 类的构造函数没有任何参数。因此，传递给构造函数的所有参数都被忽略了。
*   父类（基类）的构造函数在未传递任何参数的情况下被调用。所以，`CustomerName`、`CompanyName` 和 `Designation` 这三个变量都将获得 `undefined` 作为值。
*   因此，我们得到了上述输出。

将代码重写如下：

```
//Demo3.4
class Customer{
   constructor(CustomerName,CompanyName,Designation){
       this.CustomerName=CustomerName;
       this.CompanyName=CompanyName;
       this.Designation=Designation;
   }
   Save(){
       console.log(“Customer Saved: “+this.CustomerName+”(“+this.Designation+”-”+this.CompanyName+”)”);
   }
}
class GoldCustomer extends Customer{
   constructor(CustomerName,CompanyName,Designation){
       super(CustomerName,CompanyName,Designation);
   }
}
let c=new GoldCustomer(“Parvez”,”Siddiqui”,”Technical Architect”);
c.Save();
```

像之前一样执行它。

![](img/Image42423.jpg)

**图 2.18**

*   这一次，`GoldCustomer` 类有一个包含三个参数的构造函数。
*   在 `GoldCustomer` 的构造函数中，我们调用了 `Customer` 类的构造函数，并将这三个值作为参数传递。

### 字符串插值

这是 ES6 中一个虽小但令人兴奋且实用的特性。请看下面的演示：

```
//Demo 1
let myName=”Sukesh Marla”;
let myCompany=”Just Compile”;
console.log(“My Name is “+myName+” and my company is “+myCompany)
```

![](img/Image42467.jpg)

**图 2.19**

输出如下：

这种编码方式的唯一问题在于拼接的困难。

我们最终会用到大量的 `+`，这使得代码难以阅读且充满挑战。

例如，请看下面的代码：

```
//Demo 2
let myName=”Sukesh Marla”;
let myCompany=”Just Compile”;
console.log(“My Name is “+myName+” and my company is”+myCompany)
```

你能看出 `Demo 1` 和 `Demo 2` 之间的区别吗？

如果看不出来，请检查上述代码的输出。

![](img/Image42511.jpg)

**图 2.20**

区别在于 `is` 和 `Just Compile` 之间少了一个空格。

在 ES6 中，借助字符串插值，拼接变得更加方便。

为此，我们将使用反引号（`）符号代替双引号（“”）和单引号（‘’）。为了表示动态值，我们将写 `$` 后跟花括号（{}），并在花括号内放入变量。请检查以下代码：

```
//Demo 3
let myName=”Sukesh Marla”;
let myCompany=”Just Compile”;
console.log(`My Name is ${myName} and my company is ${myCompany}`)
```

执行后，你将得到相同的输出（但语法更简单）。

![](img/Image42467.jpg)

**图 2.21**

### 增强的对象字面量

让我们通过一个演示来理解。

```
let CustomerName=”Ramlal”;
let Address=”Ramgarh”;
let Customer={CustomerName:CustomerName, Address:Address};
console.log(Customer);
```

![](img/Image42627.jpg)

**图 2.22**

上述代码直观且简单。我们只是创建了一个新的 JavaScript 对象 `Customer`，其键为 `CustomerName` 和 `Address`。

让我们检查输出。

![](img/Image42634.jpg)

**图 2.23**

你是否注意到，customer 对象的属性名与变量名相同？（`CustomerName` 和 `Address`）。

在 ES6 中，当左侧和右侧的变量名相同时，代码可以重写如下：

```
let CustomerName=”Ramlal”;
let Address=”Ramgarh”;
let Customer={CustomerName,Address};
console.log(Customer);
```

### 展开运算符

顾名思义，它是一个用于展开某些东西的运算符。

它展开什么？它展开对象和集合。

让我们做几个演示来更好地理解。

**演示 1：合并两个数组**

假设我们有两个数组如下：

```
let a=[1,2,3];
let b=[6,7];
```

我们的目标是创建一个新数组，包含另外两个数组的元素。

你认为下面的代码能实现吗？

```
let c=[a,b];
console.log(c);
```

上述代码将创建一个只有两个元素的新数组，而这两个元素本身又都是数组。请检查以下输出：

![](img/Image42712.jpg)

**图 2.24**

现在，使用展开运算符将相同的代码重写如下：

```
let a = [1,2,3];
let b = [6,7];

let c = […a,…b];
console.log(c);
```

你注意到上面代码中的三个点（...）了吗？这就是展开运算符的写法。它简单地将数组中的值解包并放置在那里。现在我们将得到期望的输出。

![](img/Image42756.jpg)

**图 2.25**

**演示 2：克隆数组**

假设我们有一个像下面这样的数组：

```
let a = [1,2];
```

我们的目标是创建一个新数组，包含与上述数组相同的元素。

我们可以想到以下三种方式：

```
//let b=a;
//let b=[a];
//let b=[…a];
```

根据你的判断，上述哪种方式是正确的？

1.  第一种方式会导致引用复制。

    ```
    let b=a;
    console.log(b);
    ```

    让我们检查输出。

    看起来输出符合预期，但实际上并非如此。

    ![](img/Image42764.jpg)

    **图 2.26**

    让我来证明。只需向第一个数组添加一个元素。

    ```
    let a=[1,2];
    let b=a;
    console.log(“b”,b);
    a.push(3);
    console.log(“a”,a);
    console.log(“b”,b);
    ```

    ![](img/Image42803.jpg)

    **图 2.27**

    你会注意到第二个数组也发生了变化。

    所以，可以肯定第一种方式不可行。

2.  第二种方式会得到一个只有一个元素的新数组，该元素是一个数组。

    让我们试试。

    ```
    let a=[1,2];
    let b=[a];
    console.log(“b”,b);
    ```

    ![](img/Image42869.jpg)

    **图 2.28**

    输出如下：

3.  第三种方式使用展开运算符，将是我们的解决方案。

    ![](img/Image42876.jpg)

    **图 2.29**

    ```
    let a=[1,2];
    let b=[…a];
    console.log(“b”,b);
    ```

**演示 3：合并两个 JavaScript 对象**

展开运算符也可以用于 JavaScript 对象。

假设我们有以下 JavaScript 对象，目标是创建一个合并了这两个对象的新 JavaScript 对象：

```
var a={Name:”Sukesh Marla”, CompanyName:”Just Compile”};
var b={Technology:”JavaScript”};
```

1.  让我们尝试以下代码：

    ```
    var c={a,b};
    console.log(c);
    ```

    它将创建一个包含两个键 `a` 和 `b` 的新 JavaScript 对象。

    这不是我们期望的输出。

    ![](img/Image42919.jpg)

    **图 2.30**

2.  让我们使用展开运算符尝试同样的操作。

    ```
    var a={Name:”Sukesh Marla”, CompanyName:”Just Compile”};
    var b={Technology:”JavaScript”};
    var c={…a,…b};
    console.log(c);
    ```

    ![](img/Image43002.jpg)





**图 2.31**

展开运算符在这里完成了工作。

### 强大的 for-of 循环

我坚信你一定已经使用 JavaScript 的 `for` 和 `for…in` 循环编写了大量代码。

现在，有一个新的 `for…of` 循环。它让我们能够以更好的方式遍历集合。

假设我们有如下数组：

```javascript
let a=[“A”,”B”,”C”,”D”];
```

我们的目标是在控制台中显示数组的每个元素。

使用 ES5，我们可能会采用以下方式之一：

```javascript
for(let index=0;index<a.length;index++){
   console.log(a[index]);
}
```

或者

```javascript
for(let index in a){
   console.log(a[index]);
}
```

`for…in` 只是 for 循环的语法糖。

现在，使用 ES6，有一种更简洁的方式，那就是 `for…of`。

```javascript
for(let element of a){
   console.log(element);
}
```

### REST 参数

你知道 JavaScript 中的 `arguments` 关键字吗？如果知道，那很好。如果不知道，那么我们先来学习一下。

请看下面的代码：

```javascript
function Add(){
   var result=0;
   for(let i of arguments)
   {
       result+=i;
   }
   console.log(result);
}
Add(1,2,3,4,5);
```

如你所见，`Add` 函数没有显式声明任何参数，但在调用时，我们传入了五个值作为参数。这是怎么做到的？很可能是因为 JavaScript 是动态的，所以它就是这样工作的。

在 JavaScript 中，有一个名为 `arguments` 的关键字，我们可以在函数内部使用它，它让我们能够访问传递给函数的参数。

现在，同样的代码可以用更简洁的方式编写，如下所示：

```javascript
function Add(…numbers){
   var result=0;
   for(let i of numbers)
   {
       result+=i;
   }
   console.log(result);
}
Add(1,2,3,4,5);
```

上述两段代码都会输出相同的结果。

![](img/Image43062.jpg)
**图 2.32**

#### 总结

我们现在已经完成了四部分系列的第一部分。在进入下一章之前，先稍作休息。我们在本章中学习了以下 ES6 特性：

*   我们了解到学习 ES6 与学习 JS 并没有太大区别。它们是同一种语言。我们只是学习新特性。
*   我们讨论了新的 `let` 和 `const` 关键字，它们允许我们在 JavaScript 中声明块级变量，这些变量永远不会被提升。
*   我们看到了 JavaScript 中面向对象编程支持的演示。
*   我们学习了**字符串插值**如何在字符串拼接时让生活更轻松。
*   我们看到了增强的对象字面量语法，当对象的属性名与变量名匹配时，它使对象创建变得简单。
*   我们讨论了**展开运算符**，它允许我们展开对象和数组。
*   我们探索了新的强大 `for…of` 循环。
*   我们以 REST 参数的演示结束了本章，它可以作为之前 JavaScript 版本中 `arguments` 的替代方案。

## 第 3 章：ES6 特性 – 第二部分

## 引言

我们正处于从站点 1 到站点 2 的旅程中途。

在本章中，我们将探索更多 ES6 特性。

### 默认参数

检查以下代码：

```javascript
//Demo 1
function GetDiscount(amount,discount) {
   return amount - discount;
}
```

现在，让我们在不传递第二个参数的情况下调用上述函数。

```javascript
let finalAmount = GetDiscount(100);
console.log(finalAmount);
```

输出如下所示。我们的要求是，如果省略第二个参数，默认折扣应为 10。

![](img/Image43076.jpg)
**图 3.1**

在 ES6 之前，可以通过以下代码实现：

```javascript
//Demo 2
function GetDiscount(amount,discount) {
   if(discount===undefined){
      discount=10;  
   }
   return amount - discount;
}
let finalAmount = GetDiscount(100);
console.log(finalAmount);
```

这将得到预期的输出：

![](img/Image43156.jpg)
**图 3.2**

使用 ES6，可以更简单地实现：

```javascript
function GetDiscount(amount,discount=10) {
   return amount - discount;
}
let finalAmount = GetDiscount(100);
console.log(finalAmount);
```

代码更简洁，但输出相同：

![](img/Image43204.jpg)
**图 3.3**

### 箭头函数

箭头函数，也称为**胖箭头**函数，是编写函数表达式的语法紧凑替代方案。

让我通过一个示例向你展示箭头函数的两个实际好处。

#### 优势 1：紧凑且可读的函数表达式

看下面这个简单的函数表达式：

```javascript
let Add=function (number1, number2) {
   return number1+number2;
}
console.log(Add(1,2));
```

使用箭头函数重写上述代码如下：

```javascript
let Add=(number1, number2)=>{
   return number1+number2;
}
console.log(Add(1,2));
```

对上述代码不满意？为什么应该满意呢，因为差别不大。`function` 关键字消失了，引入了 `=>`。

那下面这个呢？

```javascript
let Add=(number1, number2)=>number1+number2;
console.log(Add(1,2));
```

现在是不是很酷？当内部只有一行逻辑时，箭头函数使代码更简单。

让我们做一个实际场景。假设我们有一个数字的 JavaScript 数组，我们想从中提取出偶数并创建另一个数组。

最直接的方式如下：

```javascript
let numbers=[1,2,3,4,5,6,7,8,9,10];
let evenNumbers=numbers.filter(function(number){
     if(number%2==0){
         return true;
     }
     else{
         return false;
     }
});
console.log(evenNumbers);
```

执行后，我们将得到完美的输出，如下所示：

![](img/Image43256.jpg)
**图 3.4**

让我们让代码更紧凑，如下所示：

```javascript
let numbers=[1,2,3,4,5,6,7,8,9,10];
let evenNumbers=numbers.filter(function(number){
     return number%2==0;
});
console.log(evenNumbers);
```

使用 ES6 箭头函数，上述代码可以写成：

```javascript
let numbers=[1,2,3,4,5,6,7,8,9,10];
let evenNumbers=numbers.filter(number => {
     return number%2==0;
});
console.log(evenNumbers);
```

它还可以进一步压缩为以下代码：

```javascript
let numbers=[1,2,3,4,5,6,7,8,9,10];
let evenNumbers=numbers.filter(number=>number%2==0);
console.log(evenNumbers);
```

因此，箭头函数相对于传统方法的第一个优势是代码紧凑且可读。

#### 优势 2：不绑定 `this`

通常，你可能将 `this` 称为当前类的对象。在 JavaScript 中，当 `this` 关键字在函数内部使用时，它会根据上下文绑定到不同的值。

让我们做一个演示来理解这一点。考虑以下代码块：

```javascript
let company={
   Name:”Just Compile”,
   Services:[“Consultancy”,”Application Development”,”Training”],
   DisplayServices:function() {
       console.log(this.Name)
   }
}
company.DisplayServices();
```

上述代码引用了 `company` 对象，因此输出如下：

![](img/Image43305.jpg)
**图 3.5**

现在，让我们稍微修改一下代码：

```javascript
let company={
   Name:”Just Compile”,
   Services:[“Consultancy”,”Application Development”,”Training”],
   DisplayServices:function() {
       this.Services.forEach(function(service){
```





```javascript
6. console.log(`${this.Name} does ${service}`)
7. });
8. }
9. }
10. company.DisplayServices();
```

思考片刻，尝试预测输出结果。输出结果如下：

![](img/Image43346.jpg)
**图 3.6**

你是否注意到输出中的 `undefined`？这是因为传递给 `forEach` 函数的回调函数导致的。该回调函数内部的 `this` 不再指向 `company` 对象。（在 Node.js 中，它会指向全局对象；在浏览器中，则指向 `window` 对象。）

那么，该如何解决呢？在 ES6 之前，我们通常借助一种称为“this is that”的逻辑方案来实现。

请查看以下代码：

```javascript
1. let company={
2.    Name:”Just Compile”,
3.    Services:[“Consultancy”,”Application Development”,”Training”],
4.    DisplayServices:function() {
5.        let that=this;
6.        this.Services.forEach(function(service){
7.            console.log(`${that.Name} does ${service}`)
8.        });
9.    }
10. }
11. company.DisplayServices();
```

现在，我们将得到正确的输出。

![](img/Image43354.jpg)
**图 3.7**

有了 ES6 之后，我们不再需要编写自定义逻辑来实现相同的功能。

```javascript
1. //Demo 11
2. let company={
3.    Name:”Just Compile”,
4.    Services:[“Consultancy”,”Application Development”,”Training”],
5.    DisplayServices:function() {
6.        this.Services.forEach(service=>{
7.            console.log(`${this.Name} does ${service}`)
8.        });
9.    }
10. }
11. company.DisplayServices();
```

使用箭头函数，我们有了更标准的解决方案。

![](img/Image43395.jpg)
**图 3.8**

### 对象解构

这是 ES6 的一个特性，它允许我们将数组和 JavaScript 对象的值提取到单独的变量中。

让我们通过示例来理解。

#### 示例 1
假设我们有一个如下数组：

```javascript
let a=[1,2,3,4,5,6];
```

我们的目标是将上述数组的每个值提取到单独的变量中。其中一种方法如下：

```javascript
let a1=a[0];
let a2=a[1];
let a3=a[2];
```

#### 示例 2
同样的代码可以用 ES6 的对象解构编写如下：

```javascript
let [a1,a2,a3]=a;
```

上述两种代码都会产生相同的输出。

![](img/Image43439.jpg)
**图 3.9**

#### 示例 3
对象解构可以与 REST 参数结合使用。

请查看以下代码：

```javascript
let a=[1,2,3,4,5,6];
let [a1,a2,…a3]=a;
console.log(a1);
console.log(a2);
console.log(a3);
```

它会将剩余的元素放入 `a3` 中。

![](img/Image43485.jpg)
**图 3.10**

#### 示例 4：如果提供的变量数量更多会怎样？
更准确的问题是，如果左侧提供的变量数量多于对象包含的元素数量会怎样？例如，查看以下代码：

```javascript
let a=[1,2,3,4,5,6];
let [a1,a2,a3,a4,a5,a6,a7]=a;
```

额外的变量会被声明，但不会被赋值。没有值意味着 `undefined`。

因此，在上述代码中，`a7` 将得到 `undefined` 作为输出。

#### 示例 5
假设我们有两个变量，想要交换它们的值。使用对象解构，这将变得非常轻松。

```javascript
let a1=6;
let a2=7;
[a2,a1]=[a1,a2];
console.log(a1);
console.log(a2);
```

![](img/Image43532.jpg)
**图 3.11**

#### 示例 6
对象解构也可以作为函数签名的一部分使用。

```javascript
function myFunction(otherParameters1,[a1,a2],otherParameters2) {
   console.log(otherParameters1);
   console.log(a1);
   console.log(a2);
   console.log(otherParameters2);
}
myFunction(77,[1,2,3,4,5],99);
```

我们将得到以下输出：

![](img/Image43579.jpg)
**图 3.12**

#### 示例 7
对象解构也可以与 JavaScript 对象一起使用。

```javascript
let Customer={EmployeeName:”Sukesh Marla”,CompanyName:”Just Compile”};
let {CompanyName, EmployeeName}=Customer;
console.log(EmployeeName);
console.log(CompanyName);
```

它将生成如下输出：

![](img/Image43648.jpg)
**图 3.13**

请注意，在对对象使用对象解构时，变量的名称非常重要。这里顺序无关紧要，而在数组中顺序是重要的。

例如，以下代码将生成与上一个代码相同的输出：

```javascript
let {EmployeeName, CompanyName}=Customer;
console.log(EmployeeName);
console.log(CompanyName);
```

#### 示例 8
让我们尝试最后一个关于函数中对象解构的示例。

```javascript
function myFunction(otherParameters1,{CompanyName,EmployeeName}, otherParameters2) {
   console.log(otherParameters1);
   console.log(CompanyName);
   console.log(EmployeeName);
   console.log(otherParameters2);
}
myFunction(77,{EmployeeName:”Sukesh Marla”,CompanyName:”Just Compile”},99);
```

![](img/Image43695.jpg)
**图 3.14**

#### 总结

在本章中，我们介绍了以下 ES6 特性：

* 我们学习了 TypeScript 中的默认参数，它允许我们为函数参数提供默认值。
* 我们讨论了箭头函数，它允许我们在 TypeScript 中创建无状态函数。
* 我们介绍了对象解构，它允许我们将数组或 JavaScript 对象的值提取到单独的变量中。

我们离 Angular 越来越近了。希望你的兴奋感已经达到顶峰。我们第三部分见。

## 第 4 章：ES6 特性 – 第三部分

## 引言

在第二站的第三部分中，我们将探讨 ES6 中的 Promise。

### Promise

要正确理解 `promise`，首先需要理解**同步**和**异步**编程。让我们通过一些代码来理解。

首先，让我们准备示例所需的所有材料。对于所有示例，我们需要一个运行缓慢的函数。为此，我创建了一个 `SlowFunction` 函数，如下所示：

```javascript
function SlowFunction() {
   let ms = 3000;
   let start = new Date().getTime();
   let end = start;
   while (end < start + ms) {
      end = new Date().getTime();
   }
}
```

不必过于担心上述代码。如果你不理解逻辑，可以忽略它，直接复制即可。只需记住它很慢。

现在假设我们有如下代码：

```javascript
function MyFunction(){
     SlowFunction();
     return 100;
}
//some logic 1
//some logic 2
let returnValue=MyFunction(); //some logic 3
//some logic 4
//some logic 5
console.log(returnValue); //some logic 6
console.log(returnValue+100); //some logic 7
```

在上述代码中，你可以假设每个逻辑都是应用程序中需要的独立逻辑。

为了演示，我们使用 `console.log` 代替注释。

```javascript
function MyFunction(){
     SlowFunction();
     return 100;
}
console.log(“Logic 1”); //some logic 1
console.log(“Logic 2”); //some logic 2
let returnValue=MyFunction(); //some logic 3
console.log(“Logic 4”); //some logic 4
console.log(“Logic 5”); //some logic 5
console.log(returnValue); //some logic 6
console.log(returnValue+100); //some logic 7
```

输出将相对直接。

![](img/Image43702.jpg)
**图 4.1**

执行后，你会发现逻辑 2 之后会有 3 秒的延迟，然后逻辑 4 才会显示。

我们已经准备好了所有样板代码。让我们开始第一个示例。

#### 示例 1：回调的必要性




如果你仔细检查代码，很容易得出结论：`logic 6` 和 `logic 7` 依赖于 `logic 3`，而 `logic 4` 和 `logic 5` 则完全独立于 `logic 3`。

![](img/Image43754.jpg)
**图 4.2**

那么问题来了：我们是否应该在 `logic 2` 之后等待 3 秒，才能得到 `logic 4` 和 `logic 5` 的结果？

答案是否定的。我们不应该等待。

这可以通过让 `MyFunction` 内部的代码异步执行来实现，为此我们将使用 JavaScript 的 `setTimeout` 函数。`setTimeout` 会将代码排队，等待当前调用栈执行完毕后运行。它只是打破了正常的同步流程。

```javascript
function MyFunction(){
    setTimeout(() => {
        SlowFunction();
    }, 1);
}
```

现在的问题是：如何从 `MyFunction` 函数返回值？

这可以通过使用 `callback` 函数来实现。回调函数是一种古老且经过验证的处理异步编程的方法。

以下是最终的代码。

```javascript
//Demo - Callback into action
function MyFunction(callbackFn){
    setTimeout(() => {
        SlowFunction();
        callbackFn(100);    
    }, 1);
}
console.log(“Logic 1”); //some logic 1
console.log(“Logic 2”); //some logic 2
MyFunction(returnValue=>{
    console.log(returnValue); //some logic 6
    console.log(returnValue+100); //some logic 7
}); //some logic 3
console.log(“Logic 4”); //some logic 4
console.log(“Logic 5”); //some logic 5
```

让我们理解一下流程：

* `logic 1` 运行，消息显示在屏幕上。
* `logic 2` 运行，消息显示在屏幕上。
* `logic 3` 运行，它将调用 `MyFunction`。
* 在 `MyFunction` 中，使用了 `setTimeout`，它会将内部代码排队，只有在当前调用栈执行完毕后才会运行。简而言之，在这种情况下，`MyFunction` 执行并迅速完成。
* `logic 4` 运行，消息显示在屏幕上。
* `logic 5` 运行，消息显示在屏幕上。
* 这使得调用栈为空。当前调用栈中的所有指令都已执行。因此，现在排队的代码开始运行。这意味着在等待 3 秒后，回调函数被调用。
* `logic 6` 运行，消息显示在屏幕上。
* `logic 7` 运行，消息显示在屏幕上。

如你所见，现在无需等待 3 秒就能得到 `logic 4` 和 `logic 5`。这就是我们需要回调函数的原因。

![](img/Image43792.jpg)
**图 4.3**

### 演示 2：异常

现在，假设 `MyFunction` 期望一个偶数作为输入参数。奇数将被视为无效输入。让我们实现这些更改：

```javascript
function MyFunction(inputValue,callbackFn){
    if(inputValue%2==0){
        setTimeout(() => {
            SlowFunction();
            callbackFn(100);
        }, 1);
    }    
    else{
        return “Invalid Input”;
    }
}
let fnReturnValue=MyFunction(100,returnValue=>{
    console.log(returnValue);//some logic 6
    console.log(returnValue+100);//some logic 7
});
if(fnReturnValue!=undefined){
    console.log(fnReturnValue);
}
```

与静态语言不同，在 JavaScript 中，并不强制要求从函数的每个部分返回值。`MyFunction` 有一个简单的 `if…else` 块，在 `if` 块中我们没有返回任何内容，因此函数 `ReturnValue` 的值将为 `undefined`，而在 `else` 块中，我们返回了一个字符串值。

虽然这样可行，但这不是一种干净的编码方式。还有另一种方法，即使用两个回调函数——一个用于成功，一个用于失败。

```javascript
function MyFunction(inputValue,callbackFn,errorCallbackFn){
    if(inputValue%2==0){
        setTimeout(() => {
            SlowFunction();
            callbackFn(100);
        }, 1);
    }    
    else{
        errorCallbackFn(“Invalid Input”);
    }
}
MyFunction(100,returnValue=>{
    console.log(returnValue);//some logic 6
    console.log(returnValue+100);//some logic 7
},error=>{
    console.log(fnReturnValue);
});
```

如你所见，我们向 `MyFunction` 传递了两个函数作为参数。第一个代表成功，第二个代表失败。这比之前的方法要清晰得多。

#### 前述方法的缺点

* 没有标准的行业实践来定义哪个函数是成功、哪个是失败。例如，在我们的例子中，成功回调预期在失败回调之前。你在其他地方可能会发现不同的顺序。
* 假设创建 `MyFunction` 的开发人员犯了逻辑错误。他们在回调函数之后立即调用了 `errorCallback` 函数。

```javascript
setTimeout(() => {
    SlowFunction();
    callbackFn(100);
    errorCallbackFn(“Invalid Input”);
}, 1);
```

会发生什么？两者都会执行，没有其他结果。这合理吗？答案是否定的。

我们还可以有其他类似的场景，例如在 `errorCallback` 函数之后调用回调函数，或者多次调用 `errorCallback` 函数，或者多次调用回调函数。

当我们谈论成功和失败时，以上四点最终都没有意义。从逻辑上讲，成功和失败不可能同时发生，其次，成功和失败都只应发生一次。即使我们多次调用其中任何一个，它也只应执行一次。

### 演示 3：回调地狱

假设我们想要一个接一个地调用多个异步方法。我的意思是，调用一个，等它结束后再调用另一个。为了演示，我们只尝试三个方法。

```javascript
function MyFunction(inputValue,callbackFn){
    //some code
    callbackFn(100);
}
function MyFunction2(inputValue,callbackFn){
    //some code
    callbackFn(100);
}
function MyFunction3(inputValue,callbackFn){
    //some code
    callbackFn(100);
}
MyFunction(100,returnValue=>{
    //Some Logic
    //Some Logic
    MyFunction2(200,returnValue2=>{
        //Some Logic
        //Some Logic
        MyFunction2(200,returnValue2=>{
            //Some Logic
            //Some Logic
        });
    })
});
```

上述现象被称为“回调地狱”。随着越来越多的异步方法被调用，代码变得越来越复杂且难以阅读。

![](img/Image43848.jpg)
**图 4.4**

### 演示 4：Promise

在演示 1 中，我们理解了 `callback` 的重要性。我们意识到它是多么必要。然后，在演示 2 和演示 3 中，我们讨论了它的局限性。

让我们回顾一下这些局限性：
1. 没有标准的方法来识别成功和失败。
2. 当异步方法数量较多时，回调会导致“回调地狱”。

`promise` 是这些问题的解决方案。它为我们提供了处理异步方法的标准接口。

让我们进行演示并理解这一点。

```javascript
Function MyFunction(inputValue){
    return new Promise((resolve,reject)=>{
        if(inputValue%2==0){
            setTimeout(() => {
                SlowFunction();
```





```javascript
6.  resolve(100); //success
7.  }, 1);
8.  }
9.  else{
10. reject(“Invalid Input”); //fail
11. }
12. });
13. }
```

在前面的代码中，我们创建了一个 Promise 实例，传入了一个带有两个参数的回调函数。第一个参数表示成功，第二个表示失败。`resolve` 和 `reject` 只是参数名，可以任意命名。最重要的是，第一个是成功，第二个是失败。

让我们看看调用代码：

```javascript
1.  MyFunction(12).then(result=>{
2.      console.log(“Result is”,result);
3.  },result=>{
4.      console.log(“Error is”,result);
5.  });
```

如你所知，`MyFunction` 返回了一个 `Promise` 对象。`Promise` 对象提供了一个名为 `then` 的方法，该方法期望两个回调函数。第一个回调用于成功，第二个用于失败。

![](img/Image43905.jpg)
**图 4.5**

使用 `node` 执行它来检查输出。

![](img/Image43947.jpg)
**图 4.6**

我们再来测试一下错误情况。

```javascript
1.  MyFunction(11).then(result=>{
2.      console.log(“Result is”,result);
3.  },result=>{
4.      console.log(“Error is”,result);
5.  });
```

输出如下：

![](img/Image43985.jpg)
**图 4.7**

### 成功与失败

现在我们有了表示成功和失败的标准方式。第一个回调是成功，第二个是失败。

#### 真的是成功与失败吗？

将 `MyFunction` 修改如下：

```javascript
1.  function MyFunction(inputValue){
2.      return new Promise((resolve,reject)=>{
3.          if(inputValue%2==0){
4.              setTimeout(() => {
5.                      SlowFunction();
6.                      resolve(100);
7.                      reject(“Invalid Input”);
8.                }, 1);
9.          }
10.          else{
11.              reject(“Invalid Input”);
12.          }
13.      });
14. }
```

现在，测试代码：

```javascript
1.  MyFunction(12).then(result=>{
2.      console.log(“Result is”,result);
3.  },result=>{
4.      console.log(“Error is”,result);
5.  });
```

执行并检查输出。

![](img/Image44030.jpg)
**图 4.8**

如你所见，`reject` 被忽略了，因为 `resolve` 在此之前被调用。这意味着一旦成功，就不会有失败。

*   我还建议你尝试在 `reject` 之后调用 `resolve`。这将证明成功之后不会有失败。
*   尝试多次调用 `resolve`，这将确认一旦成功就无法再次成功。
*   最后，尝试多次 `reject`。每次你只会看到一次执行，这将证明一旦失败就无法再次失败。

因此，使用 Promise，我们确实有了真正的成功和失败。

#### 回调地狱怎么办？

`Promise` 也解决了这个问题。查看以下代码：

```javascript
1.  function MyFunction(input){
2.      return new Promise((resolve,reject)=>{
3.      //some logic
4.          resolve(input+1);
5.      });
6.  }
7.  function MyFunction2(input){
8.      return new Promise((resolve,reject)=>{
9.      //some logic
10.          resolve(input+2);
11.      });
12. }
13. function MyFunction3(input){
14.      return new Promise((resolve,reject)=>{
15.      //some logic
16.          resolve(input+3);
17.      });
18. }
20. MyFunction(100).then(result=>{
21.      //some logic
22.      return MyFunction2(result);
23. }).then(result=>{
24.      return MyFunction3(result);
25. }).then(result=>{
26.      console.log(result);
27. });
```

代码现在更简单、更易读。

![](img/Image44077.jpg)
**图 4.9**

#### 总结

在本章中，我们学习了 Promise：

*   我们了解了为什么 Promise 被认为是回调的更好替代方案。
*   我们了解到 ES6 的 Promise 提供了表示成功和失败的标准方式。
*   我们了解到一个 Promise 可以被 resolve 或 reject，且只能一次。
*   我们了解到 `Promise` 也解决了回调地狱的问题。

下一章也是 ES6 部分的最后一章，它将带你到达第二站。我们下一章见。

## 第 5 章：ES6 特性 – 第 4 部分

## 引言

到本章结束时，你将到达第二站，你对 ES6 特性的学习之旅也将随之结束。本章全部关于 ES6 中的模块。

### JavaScript 模块

#### 什么是模块？

几乎每种技术都以某种方式支持模块。什么是模块？我会说，模块代表整个应用程序的一小部分。

#### 为什么需要模块？

现在，我们先不担心如何创建模块。首先，让我们关注模块化开发的重要性。

以下是模块的优点：

*   模块化开发
*   隔离编码
*   依赖管理

![](img/Image44118.jpg)
**图 5.1**

##### 1：模块化开发
将应用程序拆分为多个模块使其更易于管理和阅读。

##### 2：隔离编码
我们编写的每一段代码都属于某个模块，并且不会受到属于其他模块的其他代码的影响。每个模块内部编写的代码默认对该模块是私有的。外部（其他模块）无法访问。如果我们想让某些内容可用，必须显式地这样做。

![](img/Image44166.jpg)
**图 5.2**

因此，一个模块的开发人员不必担心另一个模块中编写的代码。他/她不必担心自己会替换/覆盖别人的功能，或者别人会替换/覆盖他/她的功能。

##### 3：依赖管理
假设我们正在开发一个应用程序，我们的应用需要一个可复用的模块（`module1`）用于某些目的。现在，假设 `module1` 依赖于另外两个模块（`module2` 和 `module3`）。最后，`module2` 依赖于 `module4`。

（在这种情况下，单词“模块”仅用于解释目的。它仅仅意味着某个库。）

**常规库**
假设 `module1`、`module2`、`module3` 和 `module4` 是常规库。我的意思是，它们不是以模块化方式创建的。为了使 `module1` 正常工作，我们必须确保所有其他依赖模块，即 `module2`、`module3` 和 `module4` 也包含在应用程序中。简而言之，我们需要了解整个依赖层次结构。这还不是唯一的挑战。我们还需要确保模块以正确的顺序包含。在这种情况下，我们应该先有 `module4`，然后是 `module2` 和 `module3`，最后是 `module1`。

![](img/Image44200.jpg)
**图 5.3**

**模块化库**
现在，好消息是，对于常规库来说情况确实如此。如果所有这些模块都是以模块化方式开发的，那么我们将采用不同的方法。

在我们的应用程序中，我们只会引用 `module1`，其他所有内容都将被间接引用。

这就是使用模块的第二个优点。

#### 如何在 JavaScript 中创建模块？

接下来，让我们学习如何在 JavaScript 中创建模块。这取决于你的运行时环境：

1.  使用 Node 运行时。
2.  使用浏览器运行时和 ES6 模块。
3.  使用浏览器运行时但不使用 ES6 模块。

让我们逐一了解这三种情况。

##### 使用 Node 运行时

如果你使用 Node.js 运行时执行 JavaScript，那么每个文件都成为一个模块。默认情况下，一个文件中声明的每个函数和变量都对另一个文件隐藏。我们必须显式地让外部世界可见。

让我们做一个演示。创建 JavaScript 文件 `lib1.js` 和 `lib2.js`，内容如下：

```javascript
//lib1.js
function getString(){
    return getString2();
}
function getString2(){
```





```javascript
return “Just Compile”;
}
```

它会自动为我们创建一个名为 `lib1` 的 Node.js 模块。`lib1` 模块中的两个方法都是私有的，外部无法访问。

```javascript
//lib2.js
function getString(){
    return getString2();
}

function getString2(){
    return “Train IT”;
}
```

它会自动为我们创建一个名为 `lib2` 的 Node.js 模块。`lib2` 模块中的两个方法都是私有的，外部无法访问。

如你所见，这两个文件都包含同名函数 `getString` 和 `getString2`。

接下来，再创建一个 JavaScript 文件 `test.js`，内容如下：

```javascript
//test.js
console.log(getString());
```

它会创建一个名为 `test` 的新模块。

使用 `node` 命令执行 `test.js`。

![](img/Image44245.jpg)
**图 5.4**

如你所见，我们遇到了运行时错误，因为 `test` 模块不知道 `getString` 方法。

要解决这个错误，我们必须显式地将这些方法暴露给外部世界。这可以通过 `exports` 关键字来实现。

只需在 `lib1.js` 和 `lib2.js` 的末尾添加以下代码行：

```javascript
//lib2.js 和 lib1.js
exports.myFunction=getString;
```

通过上述代码，我们将 `getString` 方法设为公有，现在外部可以访问它了。

在 `test.js` 中，要访问其他模块导出的内容，我们需要先导入它，为此我们使用 `require` 关键字。

将 `test.js` 的内容修改如下：

```javascript
let lib1=require(‘./lib1’);
let lib2=require(‘./lib2’);
console.log(lib1.myFunction());
console.log(lib2.myFunction());
```

如你所见，我们分别导入了 `lib1` 和 `lib2` 模块，局部变量 `lib1` 和 `lib2` 将允许我们访问各自模块中暴露的函数。

再次使用 `node` 命令执行。

![](img/Image44298.jpg)
**图 5.5**

从上述演示中，我们可以总结出以下几点：

1. 模块将应用程序拆分为多个更小的块，每个块封装特定的功能，从而实现抽象。
2. 模块允许我们进行隔离编码。

让我们再做一次演示。

再创建三个 JavaScript 文件，分别命名为 `lib3.js`、`lib4.js` 和 `test.js`。在其中放入以下内容：

```javascript
//lib3
let lib4=require(“./lib4”);
function getString(){
    return lib4.getString();
}
exports.getString=getString;
```

```javascript
//lib4
function getString(){
    return “Sukesh Marla”;
}
exports.getString=getString;
```

```javascript
let lib3=require(‘./lib3’);
console.log(lib3.getString());
```

如你所见，`test2.js` 只引用了 `lib3.js`，它完全不知道 `lib4.js` 的存在。

使用 `node` 命令执行 `test2.js`，得到以下输出：

第二次演示证明，使用模块时，我们不需要记住整个依赖树。模块系统会自动处理它。

![](img/Image44346.jpg)
**图 5.6**

上述两个演示共同证明了模块的三个优点：模块化开发、隔离编码和依赖管理。

### 在浏览器运行时中（不使用 ES5 模块）

通过之前的实验，我们学会了在 Node.js 环境中创建模块。接下来，让我们学习如何在浏览器运行时中实现。

不幸的是，浏览器运行时不支持内置的 JavaScript 模块。（至少在 ES6 引入之前不支持。我们将在下一节讨论 ES6 模块。）

我知道你内心的开发者不会接受这一点，除非通过演示来证明。让我们来做一下。

创建三个 JavaScript 文件 `lib1.js`、`lib2.js`、`test.js` 和一个 `index.html`，内容如下：

```javascript
// lib1.js
function getLib1Message(){
    return getMessage();
}
function getMessage(){
    return “Just Compile”;
}
```

```javascript
// lib2.js
function getLib2Message(){
    return getLib1Message() +” & “+ getMessage();
}
function getMessage(){
    return “Train IT”;
}
```

```javascript
//test.js
alert(getLib2Message());
```

```html
<html>
<head>
    <title>
        JavaScript 模块演示
    </title>
    <script src=lib1.js></script>
    <script src=”lib2.js”></script>
    <script src=”test.js”></script>
</head>
</html>
```

我们需要一个开发服务器来托管上述 HTML 和 JavaScript 文件。

为此，我们将使用 `lite-server`。打开命令提示符，执行以下命令：

```bash
npm install lite-server -g
```

之后，在保存上述文件的文件夹中执行 `lite-server` 命令。

![](img/Image44433.jpg)
**图 5.7**

它会自动打开浏览器，请求 `http://localhost:3000` 文件。

有时浏览器可能不会自动启动。在这种情况下，请手动启动。

![](img/Image44481.jpg)
**图 5.8**

你期望的输出是不是“Just Compile & Train IT”？

在上述情况中，`lib2.js` 替换了 `lib1.js` 中的 `getMessage` 方法。

`lib1.js` 和 `lib2.js` 不是模块，因此当它们被包含在 HTML 文件中时，会相互影响。

JavaScript（在 ES6 之前）没有默认的模块支持，但我们可以通过模块加载器和模块格式化器来实现。

***注意：*** **本系列教程全部关于 Angular。我们讨论并涵盖所有这些术语，是为了让你的基础更扎实。模块加载器和模块格式化器本身就是一个庞大的主题。目前请不要深入探究。**

### 模块格式化器

它是编写代码的标准方式。`AMD`、`CommonJS`、`UMD` 是模块格式化器的一些例子。在我们的演示中，我们将使用 `AMD` 格式。

因此，第一步，让我们将三个 JavaScript 文件全部重写为 `AMD` 格式。

从 `lib1.js` 开始。

当使用 `AMD` 格式编写代码时，我们必须调用 `define` 函数。

它接受两个参数：第一个是数组类型，第二个是一个函数。

```javascript
//lib1.js
define([], function() {
});
```

我坚信，首先引起你好奇的一定是 `define` 函数。你一定会问自己：“这个 `define` 函数是什么？我以前在 JavaScript 中从未见过。”

暂时把这个想法放在一边，专注于演示。你最终会理解的。

接下来，把你所有的代码都写在这个匿名函数内部。

```javascript
//lib1.js
define([], function() {
    function getLib1Message(){
        return getMessage();
    }
    function getMessage(){
        return “Just Compile”;
    }
});
```

通过上述代码，我们创建了一个名为 `lib1` 的 JavaScript 模块。

其次，由于 `getLib1Message` 和 `getMessage` 都定义在另一个函数内部，它们成为该函数的私有成员，无法被其他代码覆盖，也不会覆盖其他代码。

但如果你还记得之前的演示，`getLib1Message` 被另一个模块 `lib2` 调用。这意味着我们必须将 `getLib1Message` 设为公有。

为此，我们将使用 `exports` 模块。在你的 `lib1` 模块中，你可以访问 `exports` 模块。这就是 `define` 函数中第一个参数的作用。请看以下代码：

```javascript
//lib1.js
define([‘exports’],
function(e) {
    function getLib1Message(){
        return getMessage();
    }
    function getMessage(){
        return “Just Compile”;
    }
```





```javascript
10. e.getMessage=getLib1Message;
11. });
```

“之前定义，现在导出，这是怎么回事。”

别担心。放松一下，继续看演示。

我们来分析前面的代码。

*   那个数组指定了你的模块所依赖的其他模块。
*   在前面的代码中，`exports` 是一个模块名。将其放在数组中表示我们的模块依赖于它。函数中的参数 `e` 持有对 `exports` 模块的引用。
*   前面的代码表明 `getLib1Message` 将以 `getMessage` 的形式提供给其他模块。

现在我们已经完成了 `lib1.js`，接下来继续看 `lib2.js`。

```javascript
1. // lib2.js
2. define([‘exports’,”./lib1.js”],
3. function(e,lib1) {
4.     function getLib2Message(){
5.         return lib1.getMessage() +” & “+ getMessage();
6.     }
7.     function getMessage(){
8.         return “Train IT”;
9.     }
10.     e.getMessage=getLib2Message;
11. });
```

如你所见，这次我们不仅在数组中指定了 `exports`，还指定了 `./lib1.js`。通过 `exports`，我们使 `getLib2Message` 在另一个模块中可用；通过 `lib1`，我们可以访问 `lib1.js` 的 `getMessage` 方法。

接下来，修改 `test.js`。

```javascript
1. define([
2.     ‘./lib2.js’,
3. ], function(lib2) {
4.     alert(lib2.getMessage());
5. });
```

在 `test.js` 中，我们只依赖 `./lib2.js`。

### 模块加载器

模块加载器是第三方库，它们让浏览器理解模块。`requireJS` 和 `systemJS` 是模块加载器的一些例子。

简单来说，下载模块加载器，将其包含在应用程序中，之后浏览器才会开始识别 `define` 和 `exports` 关键字。

那么，让我们使用 `npm` 下载模块加载器。

```bash
npm install requirejs
```

在上面的命令中，下载 `requireJS` 模块加载器，并将其放在 `node_modules` 文件夹中。

现在一切就绪，我们来做最后的修改。修改 `index.html`。

```html
1. <html>
2. <head>
3.     <title>
4.         JavaScript 模块演示
5.     </title>
6.     <script data-main = “test.js” src = “\node_modules\requirejs\require.js”></script>
7. </head>
8. </html>
```

如你所见，我们只在 HTML 文件中包含了 `require.js`，并为 script 标签添加了一个特殊属性 `data-main`，其值设置为 `test.js`。这就是在 `require.js` 中指定启动文件的方式。

现在，如你所知，`test.js` 依赖于 `lib1.js`，而 `lib1.js` 又依赖于 `lib2.js`。因此，这两个文件都会被模块加载器动态加载到 HTML 文件中。

在存放上述所有文件的文件夹中执行 `lite-server` 命令，启动服务器。

这次我们将得到正确的输出。

![](img/Image44490.jpg)
**图 5.9**

![](img/Image44587.jpg)
**图 5.10**

这是一个使用 AMD 作为模块格式化器、`requireJS` 作为模块加载器的演示。你也可以尝试其他组合。这个演示的目的是认识 JavaScript 模块的重要性和基本原理。

### 使用浏览器运行时和 ES6 模块

到目前为止，我们已经了解到 Node.js 运行时默认支持模块，而浏览器运行时则不支持。

好消息是，与 ES5 不同，ES6 支持 JavaScript 模块。

因此，如果你的浏览器兼容 ES6 JavaScript 模块，你就可以摆脱模块格式化器和模块加载器的复杂性。你可以遵循 ES6 模块的标准语法。

现代浏览器已经开始支持 ES6 JavaScript 模块。

在我们的演示中，我们将使用完全支持它的 Google Chrome。

那么，不要浪费时间，让我们像之前一样开始创建 `lib1.js`、`lib2.js` 和 `test.js`。

```javascript
1. //lib1.js
2. export function getLib1Message(){
3.     return getMessage();
4. }
5. function getMessage(){
6.     return “Just Compile”;
7. }
```

你注意到 `getLib1Message` 方法上的 `export` 关键字了吗？这意味着 `lib1.js` 是一个包含两个方法的 JavaScript 模块，其中 `getLib1Message` 将是公开的，而 `getMessage` 将是私有的。

```javascript
1. // lib2.js
2. import {getLib1Message} from “./lib1.js”
3. export function getLib2Message(){
4.     return getLib1Message() +” & “+ getMessage();
5. }
6. function getMessage(){
7.     return “Train IT”;
8. }
```

看看 `import` 语句。我相信它不言自明。

在本次演示之后，我们将更深入地探讨 `export` 和 `import`。现在，先让我们得到最初的输出。

```javascript
1. //test.js
2. import {getLib2Message} from “./lib2.js”
3.     alert(getLib2Message());
```

代码更加简洁易读。

最后一件事，创建 `index.html` 文件。

```html
1. <html>
2. <head>
3.     <title>
4.         JavaScript 模块演示
5.     </title>
6.     <script type=”module” src = “test.js”></script>
7. </head>
8. </html>
```

你注意到没有涉及模块加载器吗？我们不需要它。这是 ES6，是标准语法。另外，你可以看到 `type` 属性有一个特殊的值 `module`。这使 JavaScript 理解 `test.js` 是一个 JavaScript 模块。

现在是执行的时候了。在存放上述文件的文件夹中执行 `lite-server` 命令，启动服务器。输出如下：

![](img/Image44600.jpg)
**图 5.11**

是不是很酷？毫无疑问。

在结束本章之前，让我们再学习一些关于 ES6 模块的知识。

### 关于 ES6 模块的更多内容

**我们可以在 Node.js 中使用 ES6 模块吗？**

使用 Node.js 13 或更高版本，我们可以毫无问题地使用 ES6 模块语法。

**我们可以从一个 ES6 模块中导出多个东西吗？**

是的，使用相同的语法，我们可以做到。

```javascript
1. //module1.js
2. export function a(){
3.     …
4. }
5. export function b(){
6.     …
7. }
8. function c(){
9.     …
10. }
11. //module2.js
12. import {a,b} from “./module1.js”
```

**我们可以导出变量吗？**

可以，查看以下语法：

```javascript
1. //module1.js
2. export const ABCD=10;
3. //module2.js
4. import {ABCD} from “./module1.js”
```

**如果导入的功能已经存在怎么办？**

我们可以在导入时设置别名。查看以下语法：

```javascript
1. //module1.js
2. export function a(){
3.     …
4. }
5. //module2.js
6. import {a as mya} from “./module1.js”
7. function a(){
8.     mya();
9. }
```

**如果我们想导入模块导出的所有内容，但不想为每个导出的东西显式指定 import 语句，该怎么办？**

你可以使用 `*`，如下所示：

```javascript
1. //module1.js
2. export function a(){
3.     …
4. }
5. export function b(){
6.     …
7. }
8. function c(){
9.     …
10. }
12. //module2.js
13. import * as lib2 from “./lib2.js”
14. console.log(lib2.a());
15. console.log(lib2.b());
```

**还有其他导出方式吗？**

前面演示中使用的导出语法称为命名导出。

还有一种叫做默认导出。查看以下代码：

```javascript
1. //module1.js
2. export default function a(){
3.     …
4. }
5. export function b(){
6.     …
7. }
9. // module2.js
10. import xyz,{b} from “./module1.js”
11. function m1(){
12.     return xyz();
13. }
14. function m2(){
15.     return b();
16. }
```

在前面的代码中，`module1` 同时具有命名导出（`function b`）和默认导出（`function a`）。





*   命名导出必须在`{and}`内部指定，而默认导出则不需要。
*   每个模块只能有一个默认导出。
*   我们可以为默认导出使用别名。在上述代码中，该函数作为函数`xyz`被导入。

#### 总结

终于，我们完成了第二站的旅程，并探索了 ES6 的特性。如果有什么令人困惑或复杂的地方，不用担心。一旦我们开始学习 Angular，你会再次看到它们中的大部分在实际中的应用，那时一切都会变得简单得多。让我们回顾一下本章所学的内容：

*   我们讨论了模块的优势——模块化开发、隔离编码和依赖管理。
*   模块化开发意味着将应用程序拆分成多个更小的模块，从而提高代码的可维护性和可读性。
*   隔离编码意味着每个开发者独立编写代码，不受其他开发者编写内容的影响。在一个模块内编写的代码对该模块来说是私有的，除非显式地公开。因此，不会出现一个开发者覆盖另一个开发者所写功能的情况。
*   依赖管理意味着应用程序的依赖关系可以轻松管理。我们不需要了解整个依赖关系图。
*   我们学习了为`Node.js`运行时创建 JavaScript 模块。
*   我们学习了在不使用 ES6 的情况下为浏览器运行时创建 JavaScript 模块。
*   我们学习了使用 ES6 为浏览器运行时创建 JavaScript 模块。
*   我们还讨论了 ES6 模块中的默认导出和命名导出。

## 第 2 节总结

第 2 节全部关于 ES6。ES6 是 JavaScript 的新标准。学习 ES6 使基础更加扎实，TypeScript 也变得更简单。

它总共包含四章，从第 2 章：ES6 特性（第一部分）开始，到第 5 章：ES6 特性（第四部分）结束。在这一旅程中，我们探索了 ES6 的各种特性。

### 第 2 章
*   我们了解到学习 ES6 与学习 JS 并没有太大区别。它们是同一种语言。我们只是学习新特性。
*   我们讨论了新的`let`和`const`关键字，它们允许我们在 JavaScript 中声明块级变量，这些变量永远不会被提升。
*   我们看到了 JavaScript 中面向对象编程支持的演示。
*   我们学习了字符串插值如何使字符串拼接变得简单。
*   我们看到了 JavaScript 中增强的对象字面量语法，当对象的属性名与变量名匹配时，它使对象创建变得容易。
*   我们讨论了展开运算符，它允许我们展开对象和数组。
*   我们探索了强大的新`for…of`循环。
*   我们以 REST 参数的演示结束了本章，REST 参数可以作为之前 JavaScript 版本中`arguments`的替代方案。

### 第 3 章
*   我们学习了 TypeScript 中的默认参数，它允许我们为函数参数提供默认值。
*   我们讨论了箭头函数，它允许我们在 TypeScript 中创建无状态函数。
*   我们讨论了对象解构，它允许我们将数组或 JavaScript 对象的值提取到单独的变量中。

### 第 4 章
*   我们了解到 ES6 的 Promise 提供了一种表示成功和失败的标准方式。
*   我们了解到一个 Promise 可以被解决或拒绝，并且只能发生一次。
*   我们了解到`Promise`也解决了回调地狱的问题。

### 第 5 章
*   我们讨论了模块的优势——模块化开发、隔离编码和依赖管理。
*   模块化开发意味着将应用程序拆分成多个更小的模块，从而提高代码的可维护性和可读性。
*   隔离编码意味着每个开发者独立编写代码，不受其他开发者编写内容的影响。在一个模块内编写的代码对该模块来说是私有的，除非显式地公开。因此，不会出现一个开发者覆盖另一个开发者所写功能的情况。
*   依赖管理意味着应用程序的依赖关系可以轻松管理。我们不需要了解整个依赖关系图。
*   我们学习了为`Node.js`运行时创建 JavaScript 模块。
*   我们学习了在不使用 ES6 的情况下为浏览器运行时创建 JavaScript 模块。
*   我们学习了使用 ES6 为浏览器运行时创建 JavaScript 模块。
*   我们还讨论了 ES6 模块中的默认导出和命名导出。

# 第 3 节：Webpack

## 引言

亲爱的 Angular 爱好者们，我相信到目前为止你们已经享受了前往第二站的旅程。

我 100% 保证，现在你已经对`Node.js`、`npm`有了基本的了解，并且对 ES2015（也称为 ES6）有了很好的概念。

在本章中，我们将讨论`webpack`的基础知识。本文将从第二站带你到第三站，当你到达那里时，我保证你对`webpack`的理解将得到提升。

## 模块打包器

在上一章中，我们讨论了模块加载器。模块加载器在运行时按需动态加载模块。

这种按需特性有其自身的问题。想象一个场景，我们的应用程序包含数百个模块，并且它们被动态加载。这将影响应用程序的性能。

模块加载器是传统应用程序的正确解决方案。对于 SPA（单页应用），其中大量 JavaScript 代码将跨多个文件编写，我们需要一个更好的解决方案，那就是模块打包器。

模块打包器是一个节点模块，它接收一个 JavaScript 文件作为输入，然后识别该输入文件所依赖（直接或间接）的所有其他 JavaScript 文件，最后合并所有文件并生成一个单一的 JavaScript 文件。它以不影响这些 JavaScript 文件内部逻辑的方式将它们连接起来；生成的这个打包文件将被包含在 HTML 文件中。

![](img/Image44714.jpg)
**图 6.1**

## Webpack

社区中有很多打包器。`webpack`是市场上最著名的打包器之一。它也是 Angular 应用程序中包含的默认模块打包器。

因此，在进入 Angular 之前，了解并学习`webpack`的基础知识至关重要。

我们将在这里进行三个演示：
1. 使用`Node.js`作为运行时。
2. 使用浏览器作为运行时，配合 AMD 模块。
3. 使用浏览器作为运行时，配合 ES6 模块。

在开始第一个演示之前，让我们先完成安装。

要开始我们的打包过程，我们需要两个节点模块：`webpack`和`webpack-cli`，它们都是节点模块，可以通过`npm`下载。

1. `npm install webpack -g`
2. `npm install webpack-cli -g`

如你所见，这两个节点模块都使用`-g`标志安装在全局级别。如果你遗漏了`-g`标志，它们将被安装在本地，然后你需要使用`npm`脚本来使用它们。

现在我们已经完成了安装，让我们开始演示。

## 使用 Node.js 作为运行时

创建三个 JavaScript 文件：`lib1.js`、`lib2.js`和`test.js`，代码如下：

**lib1.js**
```javascript
function getLib1Message(){
     return getMessage();
}
function getMessage(){
     return “Just Compile”;
}
exports.getMessage=getLib1Message;
```

**lib2.js**
```javascript
let lib1=require(“./lib1”);
function getLib2Message(){
     return lib1.getMessage() +” & “+ getMessage();
}
```





```javascript
function getMessage(){
     return "Train IT";
}
exports.getMessage=getLib2Message;
//test.js
let lib2=require('./lib2');
console.log(lib2.getMessage());
```

在这三个文件中，`test.js` 将是我们的主文件。它依赖于 `lib2.js`，而 `lib2.js` 又依赖于 `lib1.js`。

另外请注意，`lib1.js` 和 `lib2.js` 包含一个同名的方法 `getMessage`。

为了打包，请在前述三个文件所在的文件夹中执行以下命令：

```
webpack test.js
```

如你所见，我们将 `test.js` 作为输入参数提供给了 `webpack` 命令。

![](img/Image44767.jpg)

**图 6.2**

执行上述命令后，你会在根文件夹中发现一个名为 `dist` 的新文件夹，其中包含一个文件 `main.js`。这是由 `webpack` 创建的打包文件。它将每个文件中的所有内容合并到一个文件中，且没有任何内容被替换。

![](img/Image44813.jpg)

**图 6.3**

让我们通过使用 node 命令执行 `main.js` 来测试输出，如下所示：

![](img/Image44849.jpg)

**图 6.4**

如你所见，生成了预期的输出。

我希望你现在知道了什么是打包，以及如何使用 webpack 进行打包。

## 使用浏览器作为 AMD 模块的运行时

创建三个 JavaScript 文件 `lib1.js`、`lib2.js` 和 `test.js`，代码如下：

```javascript
//lib1.js
define(['exports'],
function(e) {
     function getLib1Message(){
         return getMessage();
    }
     function getMessage(){
         return "Just Compile";
    }
     e.getMessage=getLib1Message;
});
// lib2.js
define(['exports',"./lib1.js"],
function(e,lib1) {
     function getLib2Message(){
         return lib1.getMessage() +" & "+ getMessage();
    }
     function getMessage(){
         return "Train IT";
    }
     e.getMessage=getLib2Message;
});
//test.js
define([
     './lib2.js',
], function(lib2) {
     alert(lib2.getMessage());
});
```

除了这次代码是用 AMD 格式编写的之外，其他都与之前的演示相同。

![](img/Image44888.jpg)

**图 6.5**

让我们使用与之前演示相同的过程进行打包。

然后创建用于测试的 HTML 文件，如下所示：

```html
<html>
<head>
     <title>
         JavaScript module Demo
     </title>
     <script  src = "./dist/main.js"></script>
</head>
</html>
```

如你所见，与之前使用模块加载器的演示不同，这次我们没有在 HTML 文件中包含任何模块加载器，而是将 `main.js` 作为一个普通的 JavaScript 文件包含进来。

现在，使用 `lite-server` 命令在根文件夹中启动 web 服务器。

（`lite-server` 是我们正在使用的开发用 web 服务器。它是在*第 5 章：ES6 特性第 4 部分*中下载并安装的。如果你还没有安装，请立即安装。）

![](img/Image44933.jpg)

**图 6.6**

在浏览器中检查输出：

![](img/Image44971.jpg)

**图 6.7**

## 使用浏览器作为 ES6 模块的运行时

完全重复之前的演示。唯一的区别是，这次使用 ES6 模块语法，而不是 AMD。

```javascript
//lib1.js
export function getLib1Message(){
     return getMessage();
}
function getMessage(){
     return "Just Compile";
}
// lib2.js
import {getLib1Message} from "./lib1.js"
export function getLib2Message(){
     return getLib1Message() +" & "+ getMessage();
}
function getMessage(){
     return "Train IT";
}
//test.js
import {getLib2Message} from "./lib2.js"
     alert(getLib2Message());
```

重复与之前演示相同的打包和执行过程，你将得到相同的输出。

## Webpack 配置文件

到目前为止，在我们的演示中，我们将主 JavaScript 文件的名称作为参数传递给 `webpack` 命令，结果得到了一个名为 `main.js` 的打包文件。

在实际项目中，你可能期望输出文件名不同。

`webpack` 对此有相应的规定。我们必须按如下方式执行 `webpack` 命令：

```
webpack --entry ./test.js --output-filename ./dist/main.js
```

但你知道吗，webpack 的能力远不止打包 JavaScript 文件。它也可以打包 CSS 文件，为此我们需要 webpack 插件。

通过命令行提供所有这些配置并不是一个优雅的解决方案。我们需要一种更简洁的方式，这就是 webpack 配置文件发挥作用的地方。

让我们通过一个快速演示来了解它。

让我们复用前面演示中的 BrowserModule 示例。在根文件夹中创建一个名为 `webpack.config.js` 的新文件，内容如下：

```javascript
const path = require('path');

module.exports = {
     entry: {
         main: "./test.js"
    },
     output: {
         path: path.resolve(__dirname, 'dist'),
         filename: "[name].js"
    }
};
```

上述代码是 Node.js 代码。

1. `__direname` 是 Node.js 中的一个全局变量，其值为当前文件夹的路径。假设当前文件夹是 `C://SourceCode`。
2. `path` 是 Node.js 运行时提供给我们的本地 node 模块。它有助于拼接路径。例如，`path.resolve(__direname, 'dist')` 将返回 `C://SourceCode/dist`。
3. 我们导出了一个具有两个属性——entry 和 output——的 JavaScript 对象，一个用于表示输入文件名，另一个用于指定输出文件名。
4. 在 entry 部分，main 不是关键字。它可以是任何内容。它决定了打包文件的名称，在我们的例子中，由于我们将键指定为 main，因此打包文件将是 `main.js`。

***注意：** 如果你在理解上述代码时遇到困难，请不要担心。*

**只需尝试感受 webpack。更多地关注 Angular。所有这些初始实验都是为了巩固你的基础。如果你愿意，甚至可以跳过。**

现在，打开命令提示符，并执行以下命令：

```
webpack
```

如你所见，没有向 `webpack` 命令提供任何参数。它将根据 `webpack.config.js` 中的设置生成打包文件。

你会注意到 `main.js` 文件在 `dist` 文件夹内生成。

## Webpack 用于 CSS 打包

我说过 Webpack 也可以打包 CSS 文件吗？这次让我们看看它的实际应用。

首先，让我们创建项目。

创建两个 CSS 文件和 HTML 文件，如下所示：

```css
/* file2.css */
header span{
     color: red;
}
```

```css
/* file.css */
@import url("file2.css");
div{
     color: green;
}
```

```html
<html>
<head>
     <title>CSS bundle demo</title>
</head>
<header>
     <span>Hello from header span</span>
</header>
<div>
     Hello from Div
</div>
</html>
```

如你所见，我们在 `file.css` 中导入了 `file2.css`。

接下来，让我们创建 `webpack.config.js`，如下所示：

```javascript
const path = require('path');

module.exports = {
     entry: {
         style: "./file.css"
    },
     output: {
         path: path.resolve(__dirname, 'dist'),
         filename: "[name].css"
    },
}
```

现在，让我们执行神奇的 `webpack` 命令：

![](img/Image45075.jpg)

**图 6.8**





不幸的是，`webpack` 期望每个文件都是有效的 JavaScript 模块，而 `file.css` 并不是 JavaScript 模块。要使其正常工作，首先需要将 CSS 模块转换为 JavaScript 模块，这时就需要用到名为 `css-loaders` 的 `webpack` 插件。

使用 `npm install css-loader` 命令下载它，然后按如下方式配置 `webpack` 以使用它：

```
const path = require(‘path’);
module.exports = {
     entry: {
         style: “./file.css”
    },
     output: {
         path: path.resolve(__dirname, ‘dist’),
         filename: “[name].css”
    },
     module: {
         rules: [
             {
                 test: /\.css$/,
                 use: [‘css-loader’]
            }
        ]
    }
}
```

现在，重新运行 `webpack` 命令。

它生效了吗？

让我们检查一下打包后的 `style.css` 文件。

![](img/Image45084.jpg)

**图 6.9**

![](img/Image45128.jpg)

**图 6.10**

它看起来像 CSS 文件吗？

`webpack` 是一个 JavaScript 打包工具。它将所有 CSS 文件打包并创建了一个打包后的 JavaScript 文件。

由于它生成的是 JavaScript 文件，而不是 CSS，因此将扩展名设置为 CSS 是没有意义的。

打开 webpack 配置文件，将打包文件的扩展名设置为 `js` 而不是 `css`。

```
……
    },
     output: {
         path: path.resolve(__dirname, ‘dist’),
         filename: “[name].js”
    },
     module: {
……
```

重新运行 `webpack` 命令。它将生成 `style.js` 而不是 `style.css`，然后将其包含在 HTML 文件中。

```
……
    <title>CSS bundle demo</title>
     <script src=”dist/style.js”></script>
</head>
<header>
     <span>Hello from header span</span>
</header>
……
```

运行该文件。我认为这不是预期的输出。

问题在于，我们将打包后的 JavaScript 文件包含在了 HTML 中。

![](img/Image45172.jpg)

**图 6.11**

我们必须以某种方式将 CSS 样式注入到 DOM 中。

`css-loader` 帮助 webpack 将 CSS 模块转换为 JavaScript 模块，以便它可以被打包。我们还需要一个名为 `style-bundle` 的插件，它会在打包文件中添加特殊代码，从生成的 JavaScript 包中提取 CSS 并将其注入到 DOM 中。

使用 `npm install style-loader` 命令安装 `style-loader`。

然后，在 webpack 配置文件的 loader 集合中添加 `style-loader`。

```
……
     module: {
         rules: [
             {
                 test: /\.css$/,
                 use: [‘style-loader’,’css-loader’]
            }
        ]
    }
……
```

完成后，重新运行 `webpack` 命令，然后执行 HTML 文件。

使用 Chrome 开发者工具检查 HTML。你会注意到 CSS 已被注入到 DOM 中。

![](img/Image45252.jpg)

**图 6.12**

## 模块加载器与模块打包器

我相信现在你已经对模块打包器有了清晰的认识，并且了解了它们与模块加载器的区别。

模块加载器是一个必须显式包含在 HTML 文件中的库。它在运行时按需动态加载模块。

模块打包器是一个仅在开发机器上需要的 node 模块。它类似于一个应用程序，将所有模块打包成一个文件，而不会影响彼此内部的代码。

模块打包器是更优的选择。它消除了模块加载器的复杂性，并且在此基础上提供了更好的性能。

## webpack-dev-server

你不觉得在开发过程中使用 `webpack` 会增加一些额外开销吗？每次我们在任何 JavaScript 文件中更改内容时，都必须重新创建打包文件。

![](img/Image45213.jpg)

**图 6.13**

这个问题的解决方案是 `webpack-dev-server`。就像 `lite-server` 一样，它是一个用于开发目的的 web 服务器，但它还提供了内存打包功能。让我们通过一个演示来理解它。

从上一节中选取一个浏览器示例。你可以选择两个演示中的任意一个——AMD 或 ES6 模块。显式删除其中的 `dist` 文件夹，并保持其他所有内容不变，包括如下所示的 `Index.html` 文件：

```
<html>
<head>
     <title>
         JavaScript module Demo
     </title>
     <script src = “./dist/main.js”></script>
</head>
</html>
```

首先，使用 `npm` 安装 `webpack-dev-server`：

```
npm install webpack-dev-server -g
```

现在，在根文件夹中执行以下命令：

```
webpack-dev-server --entry ./test.js --output-filename ./dist/main.js
```

![](img/Image45291.jpg)

**图 6.14**

如你所见，在执行 `webpack-dev-server` 命令时，我们使用了 `--entry` 标志，其值为 `test.js`，以及 `--output-filename` 标志，其值为 `./dist/main.js`。

`--entry` 标志用于指定输入文件名，`--output-filename` 标志用于指定打包文件名。

![](img/Image45329.jpg)

**图 6.15**

让我们理解上述命令的作用：

*   它会创建一个打包文件，但不会保存在磁盘上，而是保存在内存中。

它会启动一个用于开发目的的 web 服务器，就像 `lite-server` 一样。

现在，在浏览器中检查输出。

你是否在疑惑，如果 `main.js` 在磁盘上不存在，演示是如何工作的？

嗯，这就是 `webpack-dev-server` 的强大之处。

现在，让 `webpack-dev-server` 在后台运行，并按如下方式修改 `lib1.js`：

```
………
function getMessage(){
         return “Just Compile123”;
}
………
```

你会注意到，打包文件会自动重新创建，浏览器会刷新，并显示更新后的输出。

我希望这解决了你在开发时的打包问题。

![](img/Image45365.jpg)

**图 6.16**

#### 总结

我们在本章中探索了 `webpack`，对于 Angular 学习者来说，这些知识已经足够了。一旦你开始使用 Angular，你甚至不会在任何地方看到 `webpack`。所有打包和其他复杂操作都将对你抽象隐藏，你的注意力将完全集中在构建应用程序上。

在内部，`angular-cli` 会根据情况（构建或开发）使用 `webpack` 或 `webpack-dev-server`，以及 `css-loader` 和 `style-loader`。它还使用一个名为 `html-webpack-plugin` 的 webpack 插件，该插件在打包后会自动将打包后的 JavaScript 文件注入到 HTML 文件中。

了解你所学习技术的内部原理总是很好的。因此，了解所有这些内容将使你的 Angular 开发之旅更加有趣和顺利。

让我们快速回顾一下本章所学的内容：

*   我们发现了模块打包器如何通过将多个 JavaScript 文件合并为一个来提高性能，从而减少请求数量。

*   我们了解了 `Webpack`，它是 Angular 内部使用的模块打包器。

*   我们讨论了 `Webpack CLI`，这是一个用于处理打包的命令行界面。

*   我们做了一个 `Webpack` 的演示。

*   我们看到了 `Webpack` 配置文件的演示。

*   我们学习了如何使用 `Webpack` 打包 CSS 文件。

*   最后，我们探索了 `Webpack Dev Server`，并学习了如何在开发环境中处理 `Webpack`。

至此，第三站的旅程结束了。你的第四站旅程将带你了解 TypeScript。

## 第 7 章

## TypeScript





## 引言

我们已经完成了前往第三站的旅程，掌握了 Angular 学习的所有基础知识。

随着我们前往第四站，我们将迈出 Angular 开发的第一步。在开发 Angular 应用程序时，我们将使用 TypeScript 语言编写代码。

在本章结束时，你将到达第四站，届时你将更清晰地了解 JavaScript、ES6 和 TypeScript 之间的区别。

## 什么是 TypeScript？为什么使用它？

我们在第一章中已经快速讨论过这个问题。让我们再来一次。

*   它是一种带有编译器的编程语言。编译后，会生成相应的 JavaScript 代码。
*   更准确的术语应该是转译器（Transpiler），而不是编译器（Compiler），因为它是从一种语言创建另一种语言。在本系列中，我们将同时使用这两个词，因为“编译”是社区中最流行的词，而“转译”是实际术语。对于 TypeScript 而言，两者含义相同。
*   我们可以考虑用 TypeScript 编写代码，而不是 JavaScript，因为 TypeScript 让开发者的生活变得非常轻松。怎么做到的？这正是我们将在本章中学习的内容。

## 类型安全与编译环境

这是 TypeScript 相对于 JavaScript 的最大优势之一。*它为我们提供了一个编译环境。* 让我们通过几个演示来理解这一点。

首先，在命令提示符中执行以下命令来安装 TypeScript：

1.  `npm install typescript -g`

### 演示 1：类型安全

创建一个新的 TypeScript 文件 `comp_env.ts`，并放入以下内容：

```
var myName="Sukesh";
myName=2.0; //无效代码 – 会抛出编译错误。
```

使用 `tsc` 命令编译（转译）：

![](img/Image45407.jpg)

**图 7.1**

如你所见，编译后我们得到了一个错误。

变量 `myName` 是字符串类型，但我们试图给它赋一个数字，这是不允许的。

如果你在想 `myName` 为什么是字符串类型，那是因为类型推断。类型推断意味着数据类型将根据第一次赋值来确定。

在我们的例子中，第一次赋的值是 Sukesh，因此它变成了字符串类型。

如果你愿意，也可以显式地指定数据类型。

```
//演示 1.2
var myName:string="Sukesh";
myName=2.0; //无效代码 – 会抛出编译错误。
```

我们不会逐一讨论 TypeScript 中的每种数据类型。一旦我们开始使用 Angular，这些知识会自动掌握。

但有一种数据类型值得讨论，那就是 `any`。用 `any` 数据类型声明变量会使其成为动态类型变量，并且它可以接受所有类型的值。

```
//演示 1.3
var myName:any="Sukesh";
myName=2.0; //有效代码 – 不会抛出任何编译错误。
```

虽然不推荐使用，但它存在是为了支持向后兼容。那些没有类型安全性的旧 JavaScript 代码，可以通过将变量类型设置为 `any` 来进行迁移。

### 演示 2：函数

让我们创建一个新函数，如下所示：

```
function myFunction(x:number,y:number):string{
     var result=x+y;
}
```

上面代码中的函数期望两个 number 类型的参数，并且返回类型为 string，但我们没有返回任何内容。让我们看看编译时会发生什么。

![](img/Image45460.jpg)

**图 7.2**

让我们将函数改为如下形式：

```
function myFunction(x:number,y:number):string{
     return (x+y).toString();
}
```

接下来，让我们调用该函数，并传入错误类型的参数。

```
myFunction("a",123);
```

让我们编译并检查输出。

![](img/Image45504.jpg)

**图 7.3**

这两个演示足以证明 TypeScript 中的编译环境。

这一特性将使那些拥有丰富静态语言经验、现在开始大量涉足 JavaScript 世界的开发者的生活变得异常轻松。

在结束这个编译世界的解释之前，还有一件事值得讨论。那就是，当编译失败时会发生什么？

首先，让我们尝试一段正确的代码：

![](img/Image45541.jpg)

**图 7.4**

如你所见，编译成功后，生成了一个 JavaScript 文件。

现在，让我们尝试一段无效代码。

![](img/Image45578.jpg)

**图 7.5**

是不是很惊讶？当编译无效代码时，我们会在控制台中看到错误，但 JavaScript 文件也会被生成。

无论是编译成功还是失败，TypeScript 都会生成 JavaScript 文件。

虽然这看起来有点糟糕，但这是默认行为，可以通过使用 `noEmitOnError` 标志来关闭。

1.  `tsc comp_env.ts --noEmitOnError`

## JavaScript 的最新特性

这是 TypeScript 的第二个特性，使其优于 JavaScript。在 TypeScript 中，我们可以做所有 JavaScript 能做的事情。它支持 JavaScript 中的所有语法和特性，包括最新的 ES 特性，例如 `let`、`const`、展开运算符等。

![](img/Image45619.jpg)

**图 7.6**

TypeScript 还提供了一些 JavaScript 本身无法实现的特性，例如泛型、接口等。

## 我的一位客户的好奇心

我愿意分享我在咨询工作中与一位客户进行的一次精彩对话。

![](img/Image45658.jpg)

**图 7.7**

我的客户问道：“我不想要类型安全和编译环境。我们已经使用 JavaScript 很长时间了。我们非常习惯它的动态行为，并且对此很满意。在这种情况下，我为什么不选择 ES6 而要用 TypeScript 呢？”

以下是我的回答。

*“你问了一个非常合理的问题。请告诉我，你能保证 ES6 特性在你的客户端浏览器中都能正常工作吗？你不能保证。它可能可以，也可能不行。*

*使用 TypeScript，你可以保证所有特性在所有浏览器中都能工作。目前，TypeScript 默认在编译/转译时生成 ES5 代码。它会为你生成相应的逻辑。让我用一个简单的演示来解释。”*

我从笔记本电脑上打开了一个文件，内容如下，并问他这是什么。

```
let a=10;
console.log(a
if(true){
   let a=9;
   console.log(a);
}
console.log(a);
```

![](img/Image45698.jpg)

**图 7.8**

他迅速回答：“*这是使用了 ES6 的 let 关键字的 JavaScript 代码。*” 我微笑着回答：“*这是 TypeScript 代码。检查一下文件的扩展名。*”

我继续说道：“*TypeScript 继承了 JavaScript 的语法。你在 JavaScript 中写的所有内容都可以在 TypeScript 中编写。*”

然后，我编译（转译）了 TypeScript 文件，如下所示：

1.  `tsc Var_Dec.ts`

接着，我打开了生成的 JavaScript 文件，并将其与 TypeScript 代码进行了比较。

![](img/Image45767.jpg)

**图 7.9**

我说：“*它将 let 转换成了 var，因为 let 是 ES6 的关键字，但同时也重命名了 if 块内部的变量。重命名确保了尽管它是 var，但会产生与 let 相同的输出。因此，我获得了两个世界的好处。一是可以使用 let 关键字，二是不需要考虑浏览器兼容性。*”

我继续说道：“*TypeScript 编译器会处理新的 ES6 特性。必要时，它会生成自定义逻辑，确保输出不受影响。*”

他被打动了，但他毕竟是客户。他又提出了另一个问题。他问道：“*这听起来不错，但如果有一天 ES6 在所有浏览器中完全兼容了呢？到那时会是什么情况？*”

他很聪明，但我也不差。

以下是我的回答：





*“使用 TypeScript 而非 JavaScript 还有一个好处：TypeScript 始终领先于 JavaScript 版本。当所有浏览器都兼容 ES6 时，TypeScript 已经开始支持下一版 JavaScript 的特性了。”*

我继续说道，*“此外，额外的好处是，在这里你可以更改要生成的 JavaScript 目标版本。目前，TypeScript 会被转译为 ES5，但只需设置一个标志，我们就可以配置它生成 ES6。因此，当 ES6 完全兼容时，我们会将其设置为 ES6，这样就不需要额外的自定义逻辑了。”*

`tsc Var_Dec.ts --target ES6`

我以这样的话结束了对话：*“为了说服你使用 TypeScript，让我告诉你最后一个优势。TypeScript 会提供一些甚至 ES6 都没有的特性，例如泛型、接口等。我认为这些理由足以让你觉得 TypeScript 比 ES6 更舒适。”*

他被说服了，而我的公司也得到了一份新合同。

## TypeScript 的独特特性

现在，正如我之前所说，每个 JavaScript 特性都是 TypeScript 的特性，包括所有 ES6 特性。因此，我们不会重复所有这些特性。

我们还提到，TypeScript 有一些甚至最新 JavaScript 标准中都没有的特性。让我们来探索其中的几个。

## 接口

与 JavaScript 不同，TypeScript 支持接口。

让我们做一个演示来理解它。

创建一个 TypeScript 文件 `interface.ts`，内容如下：

```
interface MyInterface{
     MyMethod(x:string,y:number):string;
     MyMethod2():number;
}
```

让我们编译上述文件，看看生成的输出是什么。

![](img/Image45809.jpg)

**图 7.10**

它是空的。

如果你有面向对象编程的背景，那么你可能会回忆起接口的定义是 *“每个人都必须遵守的契约”*。

JavaScript 是一种动态语言，因此不需要遵守任何契约。因此，TypeScript 编译器不会为接口生成任何内容。

这个特性是为 TypeScript 程序员准备的。一旦我们开始使用 Angular，你会看到很多接口的实际应用。

让我们在代码中使用它，然后看看 JavaScript 是如何生成的。

创建一个新函数 `myFunction`，如下所示，然后编译它。

```
function myFunction(type1:MyInterface,type2:MyInterface){
     let a=type1.MyMethod(“A”,12);
     let b=type1.MyMethod2();
     let c=type2.MyMethod(“B”,12);
     let d=type2.MyMethod2();
}
```

![](img/Image45816.jpg)

**图 7.11**

**当你使用 TypeScript 时，不必过于担心生成了什么。只需理解它带来的开发时好处即可。**

例如，让我们创建一个类 `Customer`，它不实现 `MyInterface`，然后将它的实例传递给 `myFunction`，最后编译并看看会发生什么。

```
interface MyInterface{
     MyMethod(x:string,y:number):string;
     MyMethod2():number;
}

function myFunction(type1:MyInterface,type2:MyInterface){
     let a=type1.MyMethod(“A”,12);
     let b=type1.MyMethod2();
     let c=type2.MyMethod(“B”,12);
     let d=type2.MyMethod2();
}
class Customer{
}
let c=new Customer();
myFunction(c,c);
```

![](img/Image45857.jpg)

**图 7.12**

如你所见，它强制你传递遵循契约的实例，而契约规定该实例必须包含 `MyMethod` 和 `MyMethod2` 方法的定义。

## 泛型

泛型是一种编程方法论，我们编写的代码可以适用于多种数据类型。在编写代码时，我们不会显式指定数据类型，而是在其他代码中使用该代码时指定数据类型。

让我们做一个演示来理解它。

我相信，作为一名程序员，你知道什么是数组。它是相同类型元素的集合。

但在 JavaScript 中，这个概念略有不同。在 JavaScript 中，一个数组可以包含不同数据类型的元素。

如你所知，TypeScript 是一种类型化语言，这里有一个名为 `Array` 的泛型类。它允许我们创建一个可以容纳相同数据类型元素的集合。

看下面的代码：

```
let myArray:Array<number>=new Array<number>();
```

上述代码将创建一个名为 `myArray` 的数字数组。

让我们尝试向其中添加一些元素。

```
myArray.push(1); // 有效代码
myArray.push(1); // 有效代码
myArray.push(“Sukesh”); // 无效代码 - 编译错误
```

现在，让我们使用同一个 `Array` 类来创建一个字符串数组。

```
let myStrings:Array<string>=new Array<string>();
myStrings.push(“Sukesh”);  // 有效代码
myStrings.push(“Marla”);  // 有效代码
myStrings.push(1); // 无效代码 - 编译错误
```

这就是泛型编程，它给我们带来了以下两个好处：

1. `Array` 类可以用于多种数据类型，不局限于某一种特定类型。
2. 它是类型安全的。它可以处理各种数据类型，但不会因此变得类型不安全。

既然你知道 TypeScript 支持泛型，让我们创建自己的泛型自定义函数。

看下面的代码：

```
function IsEqual(x:number,y:number):boolean{
     if(x==y){
         return true;
    }
     else{
         return false;
    }
}
```

上述函数只适用于数字。我们不能将其用于字符串。那么如何让它适用于多种类型呢？

**解决方案 1：无参数类型解决方案**

将上述代码改为以下内容：

```
function IsEqual(x,y):boolean{
     if(x==y){
         return true;
    }
     else{
         return false;
    }
}
console.log(IsEqual(1,2));
console.log(IsEqual(“A”,”B”));
```

使用 `tsc` 命令编译它。

![](img/Image45908.jpg)

**图 7.13**

看起来它起作用了。但真的起作用了吗？让我们用另一种可能性测试代码。

```
function IsEqual(x,y):boolean{
     if(x==y){
         return true;
    }
     else{
         return false;
    }
}
console.log(IsEqual(1,2));
console.log(IsEqual(“A”,”B”));
console.log(IsEqual(“A”,2));
```

我们什么都没改，只是增加了一个函数调用，但这次传入了一个字符串和一个数字。看看它是否能正确编译：

![](img/Image45996.jpg)

**图 7.14**

是的，它编译通过了。这是预期的输出吗？答案是否定的。

通过从函数参数签名中移除数据类型，我们简单地将其变成了 `any` 类型，因此现在它可以接受所有类型的值。

我们期望的是一个函数，其中两个参数必须是相同的数据类型。

这可以通过将其变成泛型代码来实现。

```
function IsEqual<T>(x:T,y:T):boolean{
     if(x==y){
         return true;
    }
     else{
         return false;
    }
}
console.log(IsEqual<number>(1,2)); // 有效代码
console.log(IsEqual<string>(“A”,”B”)); // 有效代码
console.log(IsEqual<number>(“A”,”B”)); // 无效代码 - 编译错误
console.log(IsEqual<number>(1,”B”)); // 无效代码 - 编译错误
```

编译它，你会看到现在它按预期工作了。

我相信，通过这个例子，泛型编程的优势应该已经清楚了。

## 枚举

枚举是命名常量。

在编程中，我们经常会遇到需要声明常量的情况。例如，看下面的代码：





```
//Constants - May be declared in some different file
const AddMode:string="Add";
const EditMode:string="Edit";
let currentMode=GetCurrenMode();
if(currentMode==AddMode){
//Do Save operation
}
else if(currentMode==EditMode){
//Do Update Operatopm
}
```

现在，让我们定义 `GetCurrentMode` 函数：

```
function GetCurrenMode():string{
//Some logic
     return "Veg Burger";
}
```

现在，如果你编译上述 TypeScript 代码，它将顺利编译，不会报错。

我想你已经足够聪明，能意识到上述代码中的问题。值 "Veg Burger" 对于模式来说是无效的，但在编译时却无法识别。

这个问题可以使用 `enums` 来解决。

让我们用 `enums` 重写相同的代码：

```
const enum Mode{
     AddMode="Add",
     EditMode="Edit"
}
let currentMode:Mode=GetCurrenMode();
if(currentMode==Mode.AddMode){
//Do Save operation
}
else if(currentMode==Mode.EditMode){
//Do Update Operatopm
}
function GetCurrenMode():Mode{
     return Mode.VegBurger;
}
```

现在，让我们编译它。

![](img/Image46006.jpg)

**图 7.15**

枚举使得常量的使用更加方便，同时也让代码更具可读性。

## 模块

如果你熟悉 ES6 模块，那么使用模块会非常容易。

我们已经在*第 6 章：Webpack*中详细讨论过。

这里我们快速演示一下。

创建一个独立的文件夹（避免混淆），命名为 `Module-demo`，并创建两个 TypeScript 文件 `simple.ts` 和 `reusable.ts`，内容如下：

```
//reusable.ts
export function getString():string{
     return getString2();
}
function getString2():string{
     return "Just Compile";
}
//simple.ts
import {getString as myFunction} from "./reusable";
console.log(myFunction());
```

现在，使用 `tsc` 命令编译 `simple.ts`。

![](img/Image46103.jpg)

**图 7.16**

请注意，我们没有显式编译 `reusable.ts`。但由于 `simple.ts` 导入了它，它也被编译了。

![](img/Image46117.jpg)

**图 7.17**

让我们查看生成的代码——打开 `simple.ts`。

```
"use strict";
exports.__esModule = true;
//simple.ts
var reusable_1 = require("./reusable");
console.log(reusable_1.getString());
```

你在上述代码中看到的是 `CommonJS` 格式。如果你还记得，在我们讨论模块格式化器时，我们说过有很多模块格式化器，并且我们用 AMD 做了演示。

TypeScript 默认生成 `CommonJS` 格式。

我们可以使用 `--module` 标志指示 TypeScript 编译器生成 AMD 格式的代码。

![](img/Image46187.jpg)

**图 7.18**

让我们检查编译后生成的代码：

```
define(["require", "exports", "./reusable"],
function (require, exports, reusable_1) {
     "use strict";
     exports.__esModule = true;
     console.log(reusable_1.getString());
});
```

这段代码看起来熟悉吗？这是 AMD 代码。

## 在 TypeScript 中使用现有的 JavaScript 文件

在我多年的经验中，我从未见过一个不使用外部 JavaScript 文件的 Web 项目。

如果我们计划用 TypeScript 编写代码，那么外部 JavaScript 文件（不是从 TypeScript 编译而来的）该怎么办？我们如何使用它们？

我们以 jQuery 为例进行演示。

创建一个 TypeScript 文件 `simple.ts`，内容如下：

```
$(document).ready(function() {
         $('#myElement').text("Just Compile");
    }
);
```

上述代码是 jQuery 代码，它会获取 ID 为 `myElement` 的元素，并更改其内部文本。（现在不必担心 jQuery，只需知道 `$`、`text` 和 `ready` 是 jQuery 库提供的函数即可。）

让我们使用 `tsc` 命令编译代码：

![](img/Image46195.jpg)

**图 7.19**

不幸的是，`$` 不是 TypeScript 的已知关键字，因此编译失败。

解决方案是类型定义文件。

**类型定义文件**

类型定义文件是扩展名为 `d.ts` 的 TypeScript 文件。它只包含 JavaScript 库中所有构件的声明。例如，jQuery 的类型定义文件将包含 jQuery 中所有可用函数的声明。

一旦我们有了类型定义文件，就可以从这些类型定义文件中导入。

让我们看一个演示。

（如果你愿意，可以跳过这个演示，直接进入下一节，因为它在 Angular 学习中并不十分重要。由你决定。）

好消息是，几乎所有主要的可重用社区库都有类型定义文件，可以通过 `npm` 命令下载。

那么，让我们下载 jQuery 的类型定义文件。

```
npm install @types/jquery
```

执行上述命令后，你会注意到 `node_modules` 文件夹中创建了 `@types` 文件夹。

现在，将你的 TypeScript 代码修改为以下内容：

```
import $ from 'jquery';
$(document).ready(function() {
         $('#myElement').text("Just Compile");
    }
);
```

现在，使用 `tsc` 命令编译它。

由于 TypeScript 编译器识别了 `$` 函数，编译将会成功。

![](img/Image46240.jpg)

**图 7.20**

现在，让我们尝试通过将上述文件包含在 HTML 文件中来执行它。我们将使用 `webpack-dev-server` 来实现此目的，这在*第 6 章：Webpack*中讨论过。

创建一个新的 HTML 文件 `index.html`，内容如下：

```
<html>
<head>
     <title>External library demo</title>
     <script src = "dist/main.js"></script>
</head>
<body>
     <h1>Welcome to, <span id="myElement">Train IT Solutions</span></h1>
</body>
</html>
```

让我们使用以下命令执行 `webpack-dev-server`：

```
webpack-dev-server --entry ./simple.js --output-filename ./dist/main.js
```

让我们检查输出。

如果你期望现在就能得到可工作的输出，那可能会有点失望。你会发现 HTML 文本没有变化，而且更糟糕的是，它会抛出一个错误，可以通过开发者工具查看。

![](img/Image46281.jpg)

**图 7.21**

让我们理解这个错误的原因。

我们下载了 jQuery 类型定义文件，但没有下载 jQuery 库文件——`jquery.js`。

类型定义文件只是让 TypeScript 知道 jQuery 的存在，以便能够编译。要使它工作，需要显式下载 jQuery 库并将其包含在 HTML 文件中。

简而言之，类型定义文件确保编译工作，而实际的库确保执行工作。

让 `webpack-dev-server` 在后台保持运行。打开另一个命令提示符，使用 `npm` 下载 jQuery。

现在，将其包含在 HTML 文件中。

```
npm install jquery
```

将 jQuery 包含在 HTML 文件中，如下所示：

```
<html>
<head>
     <title>External library demo</title>
     <script src="./node_modules/jquery/dist/jquery.js"></script>
     <script  src = "dist/main.js"></script>
</head>
<body>
     <h1>Welcome to, <span id="myElement">Train IT Solutions</span></h1>
</body>
</html>
```

让我们检查输出：

![](img/Image46324.jpg)

**图 7.22**

**如果没有类型定义文件怎么办？**

这是完全可能的。并非每个外部 JavaScript 文件都有类型定义文件。




例如，假设我们有一个名为 `myLib.js` 的 JavaScript 文件，其中包含以下代码：

```
function getAuthorName(){
    return "Sukesh Marla";
}
```

假设我们想在 TypeScript 代码中使用前面 JavaScript 文件中的 `getAuthorName`。该怎么做呢？

创建一个 TypeScript 文件 `imple.ts`，并直接在 TypeScript 文件中尝试使用前面的函数。

```
//simple.ts
alert(getAuthorName());
```

现在，我们来编译它。

![](img/Image46370.jpg)

**图 7.23**

我们可以通过一个逻辑方案来解决这个问题。将 `simple.ts` 代码修改如下：

```
//simple.ts
var getAuthorName:any;
alert(getAuthorName());
```

现在你就可以成功编译了。

![](img/Image46406.jpg)

**图 7.24**

让我们在 HTML 文件中测试一下，为此创建一个如下所示的 HTML 文件：

```
<html>
<head>
    <title>外部库演示</title>
    <script src = "dist/main.js"></script>
</head>
<body>
</body>
</html>
```

使用以下命令执行 `webpack-dev-server`：

```
webpack-dev-server --entry ./simple.js --output-filename ./dist/main.js
```

让我们检查输出结果。

和上一个实验一样，我们需要在 HTML 文件中显式地包含 `myLib.js`。

![](img/Image46447.jpg)

**图 7.25**

将 HTML 文件修改为以下内容：

```
<html>
<head>
    <title>外部库演示</title>
    <script src="myLib.js"></script>
    <script src = "dist/main.js"></script>
</head>
<body>
</body>
</html>
```

检查输出结果：

![](img/Image46447.jpg)

**图 7.26**

我们仍然没有得到输出。

要理解原因，请打开生成的 `simple.js` 文件。

```
//simple.ts
var getAuthorName;
alert(getAuthorName());
```

你注意到 `var getAuthorName;` 了吗？它替换了库中的 `getAuthorName` 函数。

我们应该以某种方式指示 TypeScript 编译器在转译时跳过这一行。这可以通过 `declare` 关键字来实现。

将 `simple.ts` 修改为以下内容：

```
//simple.ts
declare var getAuthorName:any;
alert(getAuthorName());
```

现在，重新编译 TypeScript 文件，并检查生成的 JavaScript 文件。它应该如下所示：

```
alert(getAuthorName());
```

如你所见，声明语句被跳过了。

切换到浏览器并检查输出结果。

![](img/Image46534.jpg)

**图 7.27**

## TypeScript 配置

目前我们尚未解决以下两个实际问题：

1.  在实际项目中，我们会有许多 TypeScript 文件，无法逐个编译。我们需要一种快捷方式一次性转译所有文件。

2.  我们希望许多 TypeScript 设置是在项目级别配置的，而不是在文件级别。例如，我们希望将目标设置为 ES6。

这两个问题都可以通过配置文件来解决。

创建一个文件夹并执行 `tsc --init` 命令。

执行命令后，你会发现在文件夹内生成一个新的 JSON 文件，名为 `tsconfig.json`，其中包含一些默认设置。

![](img/Image46610.jpg)

**图 7.28**

接下来，创建两个 TypeScript 文件 `one.ts` 和 `two.ts`，并写入一些随机的 TypeScript 代码。

![](img/Image46617.jpg)

**图 7.29**

现在，打开命令提示符，导航到该文件夹，并执行不带任何参数的 `tsc`。

你能想象发生了什么吗？

![](img/Image46654.jpg)

**图 7.30**

它编译了文件夹中的所有文件。这仅在存在 `tsconfig.json` 文件时才有效。

除此之外，在编译时，它会考虑 `tsconfig.json` 中的设置进行转译。

你可以查看 [`www.typescriptlang.org/docs/handbook/compiler-options.html`](https://www.typescriptlang.org/docs/handbook/compiler-options.html) 并阅读每个设置的说明，如果你感兴趣的话。

## 装饰器

装饰器是 TypeScript 中另一个重要的特性。我们不会对装饰器进行任何演示。一旦我们开始学习 Angular，你就会看到它们的作用，但让我们先快速讨论一下。

装饰器允许我们在不修改现有代码的情况下，为函数、类、属性等添加一些新的行为。

其他技术中也有类似的功能。在 Java 中，我们有注解（Annotation），在 C# 中，有特性（Attributes），在 Python 中，它被称为装饰器（Decorators）。

现在先不用为装饰器担心。我们将在 Angular 中看到它们的作用，我保证你会喜欢它们，并理解它们的好处。

#### 总结

你已经到达了第 4 站，是时候庆祝一下了。下一章，我们将开始向更高层次迈进。我们终于达到了可以开始学习 Angular 的阶段。请保持你的兴奋度，我们下一章见。

让我们回顾一下本章学到的内容：

*   我们了解到 TypeScript 是一种会被转译成 JavaScript 的语言。

*   TypeScript 提供了编译环境，从而帮助我们避免许多运行时错误。

*   我们了解到 TypeScript 让我们能够利用最新的 ES 标准，而无需担心浏览器兼容性。

*   我们探索了泛型、接口和枚举等特性，这些特性甚至在 ES6 中都不存在。

*   我们讨论了类型定义文件，并学习了如何将第三方 JavaScript 库与 TypeScript 一起使用。

*   我们讨论了 `tsconfig.json` 文件，它是 TypeScript 的配置文件。

*   我们快速讨论了装饰器，它可以为函数、类和属性添加额外的行为。

# 第 3 部分

#### 总结

第 3 部分主要介绍了 Webpack 和 TypeScript。一个是模块打包器，另一个是会被编译成 JavaScript 的语言。让我们回顾一下这两个章节。

### 第 6 章：总结

第 6 章通过讨论 Webpack 将我们的旅程带到了第 3 站。Webpack 是一个非常庞大的主题。本章的目的是让你了解后台发生了什么：

*   我们发现了模块打包器如何通过将多个 JavaScript 文件合并为一个来减少请求次数，从而提升性能。

*   我们学习了 Webpack，它是 Angular 内部使用的模块打包器。

*   我们讨论了 Webpack CLI，这是一个用于处理打包的命令行界面。

*   我们做了一个 Webpack 的演示。

*   我们看到了 Webpack 配置文件的演示。

*   我们学习了如何使用 Webpack 打包 CSS 文件。

*   最后，我们探索了 Webpack Dev Server，并学习了如何在开发环境中使用 Webpack。

### 第 7 章：总结

第 7 章将我们的旅程带到了第 4 站，本章我们讨论了 TypeScript：

*   我们了解到 TypeScript 是一种会被转译成 JavaScript 的语言。

*   TypeScript 提供了编译环境，从而帮助我们避免许多运行时错误。

*   我们了解到 TypeScript 让我们能够利用最新的 ES 标准，而无需担心浏览器兼容性。

*   我们探索了泛型、接口和枚举等特性，这些特性甚至在 ES6 中都不存在。

*   我们讨论了类型定义文件，并学习了如何将第三方 JavaScript 库与 TypeScript 一起使用。

*   我们讨论了 `tsconfig.json` 文件，它是 TypeScript 的配置文件。

*   我们快速讨论了装饰器，它可以为函数、类和属性添加额外的行为。

# 第 4 部分

## 第 8 章

## Angular：开始

## 引言





各位 Angular 学习者，大家好！既然我们已经完成了所有必要的准备工作，是时候进入正题了。接下来就是 Angular 的环节。我们已经通过了第 4 站，正在前往第 5 站的路上。到第 5 站结束时，你将更清晰地了解如何创建一个基本的 Angular 应用程序。

## 什么是 Angular？

让我们开始理解 Angular 是什么？

它是一个用于构建 SPA（单页应用）的框架。

## 如何创建 Angular 应用程序？

首先，我会解释步骤，然后创建我们的第一个 Hello World Angular 应用程序。如果你对某个步骤感到困惑，不要紧张。继续下一步。

一直前进，直到你到达下一个模块，在那里我们将创建第一个 Angular 应用程序。

它包含以下三个简单的步骤：

![](img/Image46738.jpg)

**图 8.1**

让我们详细说明每一步。

## 步骤 1：下载和配置

让我们列出在此步骤中需要完成的所有子步骤：

1.  **下载并配置 TypeScript**

    Angular 应用程序推荐使用 TypeScript 开发，因此我们首先要做的是使用 `npm` 命令下载 TypeScript。之后，我们将创建 `tsconfig.json` 文件并进行配置。

2.  **下载 Angular 框架**

    Angular 是一个 JavaScript 框架，如果我们想用它开发应用程序，需要先下载它。

    现在，我们面临的最大挑战是它不是一个单一的库。它是一个由 7 个独立模块组成的框架——compiler、core、common、animation、forms、router、platform-browser 和 platform-browser-dynamic。

    我们必须下载每一个模块。

    因此，创建 `package.json` 并列出这七个模块。最后，使用 `npm install` 命令下载它们。

    有一点可以放心：我们不需要显式下载这些模块的类型定义文件，因为它们会随各自的模块一起下载。

3.  **下载依赖库**

    Angular 内部依赖三个库：`RxJS`、`tslib` 和 `zone.js`。

    `RxJS` 是 JavaScript 的响应式扩展库。

    `zone.js` 为 Angular 提供执行上下文。

    `tslib` 是 TypeScript 的运行时辅助库，包含一些辅助函数。

    放松，现在不用担心这些库。Angular 内部使用它们，同样可以通过 `npm` 命令下载。

4.  **下载并配置 webpack**

    到目前为止，我们还没有编写一行代码，但很快就要写了。我们已经知道模块打包器在复杂 JavaScript 应用程序中的重要性。因此，接下来我们需要下载并配置模块打包器——推荐使用 Webpack。

5.  **下载并配置 Web 服务器**

    这是一个 Web 应用程序，我们需要一个 Web 服务器来运行它。你可以使用任何你喜欢的服务器，甚至可以考虑使用 Webpack 提供的 `webpack-dev-server`。

## 步骤 2：编写启动代码

在 Angular 应用程序中，组件是基本的构建块。

一个 Angular 应用程序由许多 Angular 组件组成，这些组件按逻辑分组到一个或多个 Angular 模块中。

放松，现在不用过多担心组件和模块。我们将在后续章节中详细讨论。现在，先了解个大概。

在这些多个 Angular 模块中，有一个会被视为主模块或根模块；同样，在主模块的所有组件中，有一个会被视为主组件或根组件。

要创建 Angular 项目，首先需要创建一个根模块和一个根组件，这就是“*编写启动代码的全部内容*”。

我们还需要一个 HTML 文件，它将作为我们的启动文件。使用你喜欢的编辑器创建它。你现在可能已经感到头晕了。

为了仅仅显示 Hello World，需要做太多事情了。

![](img/Image46786.jpg)

**图 8.2**

## 步骤 3：创建打包文件

现在，这是一个自然的步骤。使用在步骤 1 中下载的模块打包器，将所有内容打包成一个 JavaScript 文件。

## 步骤 4：使用组件

现在，它包含以下两个步骤：

1.  **使用组件**

    正如我所说，组件将在本书后面详细讨论。

    现在，只需记住一个简单的事情。

    *创建一个新组件 = 创建一个新的 HTML 标签。*

    首先，在启动文件中引入打包后的 JavaScript 文件，然后在 body 标签内使用根组件。

    如果你想知道如何使用它，那么正如我所说，创建一个新组件就是创建一个新的 HTML 标签，我相信你知道如何在 HTML 中使用标签。

2.  **运行服务器**

    启动 Web 服务器并执行启动 HTML 文件。

    创建 Angular 应用程序将是一个简单的 4 步过程。

## 创建第一个 Angular 应用程序

所以，终于到了按照上述步骤创建第一个应用程序的时候了。

或者，我可以教你一种更简单的方法。

前面提到的所有步骤都封装在一个名为 **Angular CLI** 的命令行界面中。

让我们通过一个演示来了解它：

**步骤 1：安装 Angular CLI**

为此，执行以下命令：

1.  `npm install @angular/cli -g`

**步骤 2：创建第一个项目**

安装 Angular CLI 后，会有一个新命令可用——`ng`。

使用它创建一个新项目 `myapp`，如下所示：

1.  `ng new myapp`

过程中会询问一个问题。暂时忽略这个问题。对于所有是/否问题，先输入 N，然后按 *Enter* 键。

![](img/Image46852.jpg)

**图 8.3**

如果是 Angular v.11，你会看到类似下面的特殊提示：

*Do you want to enforce stricter type checking and stricter bundle budgets in the workspace?*

*This setting helps improve the maintainability and catch the bugs ahead of time.*

*For more information, see [`angular.io/strict`](https://angular.io/strict) (y/n)*

暂时也忽略它。输入 `N` 并按 *Enter* 键。

![](img/Image46906.jpg)

**图 8.4**

接下来还会出现另一个提示。请忽略它并继续。

![](img/Image46991.jpg)

**图 8.5**

安装需要一些时间。

安装完成后，你会注意到一个新文件夹 `myapp`，里面包含一些文件。

![](img/Image46999.jpg)

**图 8.6**

你一定在想刚才发生了什么。简单的答案是，我们之前提到的四个步骤中，前两个步骤已经完成：“*下载和配置*”以及“*编写启动代码*”。

![](img/Image47008.jpg)

**图 8.7**

现在，你一定感到轻松和高兴，因为 `ng` 让项目创建变得如此简单。

**步骤 3：执行项目**

导航到 `myapp` 文件夹，然后执行以下命令：

1.  `ng serve --open`

![](img/Image47051.jpg)

**图 8.8**

你会看到类似上图所示的内容，最后浏览器会自动打开并显示以下输出：

![](img/Image47093.jpg)

**图 8.9**

你在想发生了什么吗？步骤 3 和步骤 4 已经完成了。

![](img/Image47127.jpg)

**图 8.10**

有了 Angular CLI，创建第一个 Angular 项目简直是小菜一碟。

## Angular Hello World

如果你像我一样年纪较大，你会怀念 Hello World——每个新编程语言的第一个实验。

我不会让你失望的。在我们开始探索 `ng new` 创建了什么之前，让我们先搞定 Hello World。

## 编码编辑器

等等！！！在继续之前，你有一个合适的编辑器吗？相信我。每个人都需要一个完美的编辑器。拥有一个完美的编辑器就像拥有一个完美的妻子（或丈夫）（在这方面我很幸运）。它能让生活轻松很多。




我更喜欢使用 *Visual Studio Code*，你可以通过以下链接下载：

[`code.visualstudio.com/`](https://code.visualstudio.com/)

### 回到编码

接下来，让我们编写我们的 Hello World。

打开位于 `myapp/src/app` 文件夹中的 `app.component.html` 文件。

![](img/Image47164.jpg)

**图 8.11**

你会注意到里面写了很多内容。删除所有内容，并放入以下 HTML 代码：

1.  `<h1>Hello World</h1>`

保存文件，这样就完成了。

无需重新执行 `ng serve` 命令，甚至无需刷新浏览器，因为它会自动刷新。切换到浏览器，你会看到更新后的输出。

![](img/Image47206.jpg)

**图 8.12**

### 根组件

现在，让我们先看看我们的根组件。

请注意，我们将在本书后面更详细地讨论组件和模块。

目前，让我们探索我们的第一个项目。

在 app 文件夹内，你会找到 `app.component.ts` 和 `app.component.html`。这两个文件共同构成了我们的根组件。让我们打开 TypeScript 文件并研究它。

```
import {Component} from '@angular/core';
@Component({
   selector: 'app-root',
   templateUrl: './app.component.html',
   styleUrls: ['./app.component.css']
})
export class AppComponent {
   title = 'myapp';
}
```

现在，让我们移除 `styleUrls`。我们将在单独的章节中专门讨论它。目前它对输出没有影响。

![](img/Image47243.jpg)

**图 8.13**

以下三点值得讨论：

*   我们有一个名为 `AppComponent` 的 TypeScript 类，它使用从 `@angular/core` 导入的名为 `component` 的装饰器进行装饰。

*   我再次重复关于组件的相同陈述——创建组件 = 创建一个新的 HTML 标签。通过编写上述代码，我们创建了一个名为 `app-root` 的新 HTML 标签。

*   使用 `app-root` 标签，我们将获得 `app.component.html` 的内容作为响应——我们的 Hello World。

接下来，你一定在想这个新生成的组件（HTML 标签）在哪里使用。

在 `src` 文件夹中，你会找到一个包含以下内容的 `index.html` 文件：

```
<html lang="en">
<head>
   <meta charset="utf-8">
   <title>Myapp</title>
   <base href="/">
   <meta name="viewport" content="width=device-width, initial-scale=1">
   <link rel="icon" type="image/x-icon" href="favicon.ico">
</head>
<body>
   <app-root></app-root>
</body>
</html>
```

如你所见，`app-root` 标签被用在 body 标签内。

Angular CLI 内部使用 Webpack 和 `Webpack-dev-server`。它使用在 *第 6 章：Webpack* 中讨论的 `html-webpack-plugin` 动态地将打包的内存文件注入到这个 HTML 文件中。

让我们进行一个小实验。从这个 HTML 文件中移除 `app-root` 标签，并检查输出。

![](img/Image47285.jpg)

**图 8.14**

我们只会得到一个巨大的白屏。但这将是你在浏览器开发者控制台中发现的最奇怪的事情。

*必须在 index.html 中使用 app-root，因为 AppComponent 是根组件。*

你一定很好奇 `AppComponent` 是如何成为根组件的。

现在让我们来了解这一点。

## 根模块

在同一个 `src` 目录中，你会看到一个文件 `app.module.ts`。它将包含 `AppModule` 的定义，这是一个 Angular 模块。

```
import {BrowserModule} from '@angular/platform-browser';
import {NgModule} from '@angular/core';
import {AppComponent} from './app.component';
@NgModule({
   declarations: [
     AppComponent
  ],
   imports: [
     BrowserModule
  ],
   providers: [],
   bootstrap: [AppComponent]
})
export class AppModule {}
```

![](img/Image47369.jpg)

**图 8.15**

以下三点值得讨论：

*   我们有一个名为 `AppModule` 的 TypeScript 类，它使用从 `@angular/core` 导入的名为 `NgModule` 的装饰器进行装饰。

*   你能看到 declarations 部分吗？它是一个数组，里面提到了 `AppComponent`。这意味着 `AppComponent` 是 `AppModule` 的一部分。

*   类似地，还有另一个部分叫做 `bootstrap`。它表示将直接在启动 HTML 文件（即 `index.html`）中使用的组件。简而言之，它表示根组件。

我们将在本书后面讨论 `NgModule` 中的其他内容。

假设一个 Angular 应用程序将由多个组件和模块组成。这是否意味着应用程序中可以有多个模块定义了 bootstrap 部分？

可以，但只有 `AppModule` 中的 bootstrap 部分会被考虑。

你知道为什么吗？因为 `AppModule` 是根模块。

考虑到这一点，接下来我们将学习 AppModule 如何成为根模块。

## 根模块

在 `src` 文件夹中，你会找到 `main.ts` 文件。

```
import {enableProdMode} from '@angular/core';
import {platformBrowserDynamic} from '@angular/platform-browser-dynamic';
import {AppModule} from './app/app.module';
import {environment} from './environments/environment';
if (environment.production) {
   enableProdMode();
}
platformBrowserDynamic().bootstrapModule(AppModule)
   .catch(err => console.error(err));
```

*   这是启动一切的文件。编译和打包都从这个文件开始。

    它包含将逐行开始执行的语句。

*   看最后一行。这就是使 AppModule 成为根模块的原因。

## 部署

这比你想象的要简单得多。执行以下命令：

1.  `ng build --prod`

一旦上述命令执行完成，你会找到一个名为 `dist` 的新文件夹。

在该文件夹内，你会看到 `Index.html` 文件和几个 JavaScript 文件。这就是我们需要部署的内容。

![](img/Image47376.jpg)

**图 8.16**

我们将在后面的章节中探讨 `ng build` 命令生成的文件。

## 项目中的其他文件

其他文件不言自明：

*   `package.json`：管理依赖、元数据和 npm 脚本。

*   `tsconfig.json`：TypeScript 配置文件。你会注意到这些文件的多个版本。

    *   `tsconfig.json`：包含标准的 TypeScript 设置。

    *   `tsconfig.app.json`：扩展 `tsconfig.json` 并为开发模式定义额外设置。

    *   `tsconfig.app.json`：扩展 `tsconfig.json` 并为测试模式定义额外设置。

*   `angular.json`：这是 Angular CLI 的配置文件。根据此文件中定义的设置，你的 `ng` 命令的行为会有所不同。你将在本书中不时看到它的实际应用。

#### 总结

我们已经跨过了 Angular 学习的第一步，到达了第 5 站。在本章中，我们只涵盖了创建 Angular 项目的基础知识：

*   在本章中，我们讨论了创建 Angular 应用程序需要遵循的手动过程。

*   我们看到了 Angular CLI 的实际应用，并学习了如何使用 CLI 轻松创建、执行和构建 Angular 应用程序。

*   我们决定使用 Visual Studio Code 作为 Angular 编码的代码编辑器。

*   我们了解到，默认情况下，AppComponent 将被视为应用程序的根组件，正如 AppModule 的 bootstrap 部分中所提到的。



*   我们还了解到，默认情况下 `AppModule` 是我们应用的根模块，因为它是在 `main.ts` 文件中被引导启动的。
*   我们提到了 `ng build --prod` 命令，该命令用于编译应用并生成优化后的、可部署的文件。

继续深入，我们将进行大量实验，以至于本章会让你感觉像是“*A 代表苹果，B 代表球，C 代表猫……*”

## 第 9 章

## Angular 第一个应用

## 引言

在上一站（Station 5）的旅程中，我们了解了创建 C Angular 应用的基础知识。

相信我，真正的乐趣现在才开始。从本章开始，我们将逐步学习 Angular。这与我们学习 ES6 和 TypeScript 的方式截然不同。

我们不会逐一讲解每个概念来学习 Angular。相反，我们将进行一些实际工作。我们会创建几个实验，每个实验都会引入一些新的 Angular 概念和新的挑战。每完成一个实验，你都会在旅程中前进到下一站。你甚至不会意识到自己已经到达终点，并成为了一名 Angular 开发者。

## 我们将要创建什么？

我们将创建一个基础的 Angular 应用，它会在一个 HTML 表格中显示一组内存中的记录，并提供添加新记录的功能。

![](img/Image47457.jpg)

**图 9.1**

## 实验 1：理解基础的 Angular 应用

**步骤 1：创建 Angular 项目**

使用 `ng` 创建一个新的 Angular 项目 `lab1-ng`，操作如下：

1.  `ng new lab1-ng`

**步骤 2：检查应用**

使用 `ng serve` 命令运行应用。

1.  `ng serve --open`

![](img/Image47466.jpg)

**图 9.2**

## 讨论

上述项目包含 `AppModule`（我们的 Angular 根模块）和 `AppComponent`（我们的 Angular 根组件）。

下面是一些关于组件的要点。

*   组件是 Angular 应用的基本构建块。整个 Angular 应用是由可复用、可组合的 Web 组件组合而成的。
*   第一个组件，作为所有其他未来组件的容器，被称为根组件。按照惯例，它被命名为 `AppComponent`。

    例如，查看以下 Angular 应用中的组合。`AppComponent` 包含 `CustomerComponent`。`CustomerComponent` 由 `CustomerAddComponent`、`HeaderComponent` 和 `FooterComponent` 组成。接着，`CustomerAddComponent` 由 `Section1Component`、`Section2Component` 和 `Section3Component` 组成。最后，`Section3Component` 由 `Widget1Component` 和 `Widget2Component` 组成。

    ![](img/Image47536.jpg)

    **图 9.3**
*   创建组件相当于教会你的浏览器一个新的 HTML 标签。通过构建它，你将创建一个新的 HTML 元素。

在整本书中，我们将创建大量组件。所以请相信我，“*读完这本书，你将掌握组件导向设计。*”

目前不用担心 Angular 模块。

## 实验 – 继续

**步骤 3：创建新组件**

在 `app` 文件夹内，创建一个名为 `customer` 的新文件夹。

然后在该文件夹中，创建一个 TypeScript 文件 `customer.component.ts`，内容如下：

```
import {Component} from ‘@angular/core’;

@Component({
   selector: ‘customer’,
   templateUrl: ‘./customer.component.html’
})

export class CustomerComponent {
}
```

## 讨论 – 继续

上一步中创建的 `CustomerComponent` 类被称为*组件类*或*模板类*。它通过 `templateUrl` 属性与一个模板文件连接。两者共同构成 Angular 组件。

![](img/Image47584.jpg)

**图 9.4**

以下三点值得讨论：

*   你可能会问：“*为什么要建文件夹？*” 我们将组件创建在 Customer 文件夹内。将组件放在独立的文件夹中是行业标准。
*   其次，你一定注意到了类文件名中的 `component.ts` 和模板文件名中的 `component.html`。你可能会问，这是必须的吗？再次强调，这只是行业中的一种实践。`.ts` 和 `.html` 是扩展名，而 `.component` 用于标识该文件包含组件。请注意，这不是硬性规定。你可以随意命名文件。
*   `templateUrl` 并不是将模板附加到组件类的唯一方式。有时你可能会看到 *template* 而不是 *templateUrl*。如果你的 HTML 很简单，你可以使用 *template* 而不是 *templateUrl*，以减少创建另一个 HTML 文件并连接两者的开销。在实际开发中，大多数情况下我们都会使用 *templateUrl*。

## 实验 – 继续

**步骤 4：模板文件**

在 Customer 文件夹内创建一个文件 `customer.component.html`，内容如下：

1.  `<h1>Hello From Customer.</h1>`

**步骤 5：使用组件**

打开 `app.component.html`，并按如下方式使用 `CustomerComponent`：

1.  `<h1>Simple Angular example</h1>`
2.  `<customer></customer>`

**步骤 6：检查输出**

切换回浏览器并查看输出。

我们不是应该得到一些不同的输出吗？

你觉得呢？会发生什么？

![](img/Image47591.jpg)

**图 9.5**

在进入下一步之前，我建议你给自己一些时间思考原因。

![](img/Image47658.jpg)

**图 9.6**

**步骤 7：检查错误**

切换到命令提示符以检查错误。

![](img/Image47665.jpg)

**图 9.7**

## 讨论 – 继续

Angular 中的每个组件都属于某个 Angular 模块。如果一个组件不属于任何 Angular 模块，它将无法使用，并且我们会收到“*不是已知元素错误*”。

要将组件添加到模块中，我们必须在模块的 `declarations` 部分中提及该组件。

![](img/Image47700.jpg)

**图 9.8**

请注意区分 *declarations* 和 *bootstrap*。在 *bootstrap* 部分中，只会提及根级组件，而在 *declarations* 部分中，每个组件都会被声明。

（目前不用担心系统中存在多个 Angular 模块，我们稍后会讨论。）

## 实验 – 继续

**步骤 8：将组件添加到模块**

打开 `app.module.ts`，并在 declarations 部分添加 `CustomerComponent`。

```
……
import {AppComponent} from ‘./app.component’;
import {CustomerComponent} from ‘./Customer/customer.component’;

@NgModule({
   declarations: [
     AppComponent,CustomerComponent
  ],
……
```

**步骤 9：检查输出**

切换到浏览器并查看输出。

现在我们已经有了一个基础组件，让我们将其转换为符合需求的样子。从动态表格开始。

![](img/Image47736.jpg)

**图 9.9**

**步骤 10：创建模型**

在 app 文件夹内创建一个名为 Models 的文件夹，然后创建一个文件 `customer.ts`，内容如下：

```
export class Customer {
   constructor(public FName:string, public LName:string) {
  }
}
```

## 讨论 – 继续

*模型*是我们用来表示视图数据（即模板或 UI 中所需的数据）的标准命名。上一步中我们没有做任何特殊操作，只是一个简单的文件夹和一个简单的类。

**步骤 11：填充模型**

在 `CustomerComponent` 的组件类中，创建一个类型为 `Customer` 数组的变量，并在类构造函数中填充一些虚拟值。

```
import {Customer} from “../Models/customer”
……
export class CustomerComponent {
     Customers:Array<Customer>;
     constructor() {
```





6.  `this.Customers=new Array<Customer>();`
7.  `this.Customers.push(new Customer(“Sukesh”,”Marla”));`
8.  `this.Customers.push(new Customer(“Just”,”Compile”));`
9.  `this.Customers.push(new Customer(“Ram”,”Lakhan”));`
10. `}`
11. `……`

## 讨论 – 续

现在该介绍**插值**了。这是 Angular 的一个特性，用于在模板中显示动态内容。我们需要将表达式放在`{{`和`}}`之间，它会被求值并渲染。我们将在下一步中看到它的实际应用。

## 实验 – 续

### 步骤 12：在模板中显示动态内容

打开 `customer.component.html`，将内容替换为以下内容：

```
1.  <h1>显示单个客户</h1>
2.  <hr>
3.  名字: {{Customers[0].FName}}<br>
4.  姓氏: {{Customers[0].LName}}
```

![](img/Image47781.jpg)

**图 9.10**

### 步骤 13：检查输出

看看浏览器中显示的内容。

我们已经成功动态显示了集合中的第一个客户。这是我们的需求吗？我想不是。

我们需要显示整个客户集合。

## 讨论 – 续

现在该介绍**指令**了。

指令是 Angular 的一个概念，用于扩展我们的 HTML。

有以下三种指令：

1.  **组件指令**

    你已经见过这种了。`AppComponent` 和 `CustomerComponent` 就是组件指令，也称为组件。创建它们就像创建新的 HTML 标签一样。

2.  **属性指令**

    顾名思义，它是一种属性。我们将其附加到其他 HTML 元素或 Angular 组件上，其默认行为会发生变化。

3.  **结构指令**

    它们也是属性，但不会像属性指令那样改变 HTML 元素或 Angular 组件的默认行为。相反，它们会改变该元素的默认结构。

    在本书中，我们将看到所有三种指令的实际应用，包括我们自定义的指令。

现在，让我们看看 `*ngFor`。不要漏掉那个 `*`。

`*` 表示它是一个*结构指令*。我们将其附加到一个元素上，它的结构就会改变。让我们通过演示来理解它。

## 实验 – 续

### 步骤 14：显示数组

将 `customer.component.html` 的内容更改为以下代码：

```
1.  <h1>客户列表</h1>
2.  <table border=”1”>
3.     <tr>
4.       <th>名字</th><th>姓氏</th>
5.     </tr>
6.     <tr *ngFor=”let item of Customers”>
7.       <td>{{item.FName}}</td><td>{{item.LName}}</td>
8.     </tr>
9.  </table>
```

### 步骤 15：检查输出

运行应用程序，确保客户列表显示出来。

![](img/Image47831.jpg)

**图 9.11**

## 讨论 – 续

### `*ngFor`

如你所知，`tr` 代表一个 HTML 行，但由于我们附加了 `*ngFor` 指令，它的结构发生了变化。我们得到了三行，而不是一行，因为集合中有三个元素。

看看赋给 `*ngFor` 的表达式。

即 – `let item of Customers`

`item` 将持有单个 `Customer` 对象，并作为特定行的数据。它的值可以使用插值动态显示。

我建议你在继续阅读之前，再多玩一下这个演示。

### Angular 模块

你已经大致了解了*模块*的基本概念。

*在一个模块内定义的任何内容都对该模块私有，并且无法在其他模块中访问。如果我们想让某些内容可用，必须显式地导入和导出。我们在 ES6 章节中已经看到过。*

*模块几乎无处不在。ES6 有它，TypeScript 有它，甚至 Angular 也有它。它们都遵循相同的原则：对外部世界抽象掉不必要的东西。*

在 Angular 的世界中，Angular 模块是对组件、指令和管道的逻辑封装。

（你还没有见过管道，所以暂时不用担心。）

如果是这样，那么就会引出以下两个问题：

1.  `*ngFor` 指令封装在哪个 Angular 模块中？

2.  为什么我们可以在 `CustomerComponent` 中使用 `*ngFor`？因为 `CustomerComponent` 是作为 `AppModule` 的一部分定义的，而 `*ngFor` 却不是。

答案是，这是可能的，因为 `CustomerComponent` 定义在 `AppModule` 内部，而 `AppModule` 导入了 `BrowserModule`，`BrowserModule` 又导出了 `*ngFor`。

***注意：*** 当我说 `BrowserModule` 导出了 `*ngFor` 时，你可能会认为 `*ngFor` 是作为 `BrowserModule` 的一部分定义的。

令人惊讶的是，事实并非如此，但同时，`BrowserModule` 确实是让 `*ngFor` 在 `CustomerComponent` 中可用的那个模块。

我们很快就会详细讨论这一点。

## 实验 – 续

### 步骤 16：创建表单

我们的最终 UI 已经完成了一半。让我们开始在 UI 中放置表单。保持 `customer.component.html` 中的现有代码不变。只需在末尾添加以下代码：

```
1.  ……
2.  </table>
4.  <div>
5.     <h1>添加新客户</h1>
6.     名字: <input type=”text” name=”FName”><br>
7.     姓氏: <input type=”text” name=”LName”><br><br>
8.     <input type=”button” value=”保存” (click)=”Save()”> &nbsp;
9.     <input type=”button” value=”取消” >
10. </div>
```

## 步骤 17：检查输出

![](img/Image47919.jpg)

**图 9.12**

## 讨论 – 续

现在该让**事件绑定**发挥作用了。

**事件绑定**允许我们将模板中控件的事件绑定到组件类的方法。这被称为**事件绑定**。

事件绑定还引入了一个概念：**输出属性**。

![](img/Image47960.jpg)

**图 9.13**

在上图中，你能看到括号内写的 `click` 吗？

那就是 `input` 的输出属性，它被赋给了 `save()`，这是组件类中定义的一个方法，整个概念被称为**事件绑定**。

## 实验 – 续

### 步骤 18：添加新客户

按如下方式处理 `保存` 按钮的 `click` 事件：

```
1.  ……..
2.     名字: <input type=”text” name=”FName”><br>
3.     姓氏: <input type=”text” name=”LName”><br>
4.     <input type=”button” value=”保存” (click)=”Save()”>&nbsp;
5.     <input type=”button” value=”取消”>
```

现在，让我们在组件类中定义保存函数，如下所示：

```
1.  ……
2.       Save(){
3.         this.Customers.push(new Customer(“Karan”,”Arjun”));
4.      }
5.  }
```

暂时不用担心硬编码的值。稍后我们会让它变成动态的。

## 讨论 – 续

在 Angular 中，所有 DOM 事件（如 `click`、`focus` 等）都在内部被重写了。在这些事件结束时，Angular 会触发*变更检测*，它会根据 UI 的新状态重新渲染组件。

目前，不用太担心*变更检测*。我们有一个专门的章节来讨论它。

## 实验 – 续

### 步骤 19：检查输出

![](img/Image47974.jpg)

**图 9.14**

## 讨论 – 续

让我们列出尚未完成的需求：

1.  两个部分一次只显示一个——要么是数据录入界面，要么是动态表格。

2.  新客户应该根据文本框中的值创建。

3.  文本框的值必须通过一些验证规则进行验证。

为了实现第一个需求，我们将使用一个名为**属性绑定**的 Angular 概念。**属性绑定**允许我们在模板中控件的属性和组件类属性之间创建绑定。

属性绑定还引入了一个概念：**输入属性**。

![](img/Image48059.jpg)

**图 9.15**

在上图中，你能看到方括号内写的 `href` 吗？




`href` 是 `anchor` 元素的输入属性。它被赋值给 `MyURL`，其中 `MyURL` 是在组件类中定义的属性，这个概念称为 `property binding`。

对 `Property binding` 和 `interpolation` 感到困惑吗？

如果是，别担心。我们很快就会讨论。

## 实验 – 继续

### 步骤 20：为动态可见性设置组件类

在 `CustomerComponent` 类中，创建一个新的布尔属性 `IsAddNew`，并在构造函数中将其赋值为 false。

```
1.  ……
2.      Customers:Array<Customer>;
3.      IsAddNew:boolean;
4.      constructor() {
5.        this.IsAddNew=false;
6.        this.Customers=new Array<Customer>();
7.  ……
```

### 步骤 21：在模板中实现属性绑定

在表格周围添加一个 HTML 容器元素 `div`，并为其附加 hidden 属性。

```
1.  <div [hidden]=”IsAddNew”>
2.     <h1>Customer List</h1>
3.     …….
4.  </div>
5.  ……
```

**注意：** `Hidden` 是一个 HTML 属性，用于隐藏元素。

当 `list` div 隐藏时，`data-entry` div 应该可见，反之亦然。

因此，按如下方式将 hidden 属性附加到 `data-entry` div：

```
1.  ……
2.  <div [hidden]=”!IsAddNew”>
3.     First Name: <input type=”text” name=”FName”><br>
4.     Last Name: <input type=”text” name=”LName”><br>
5.  ……
6.  </div>
```

### 步骤 22：检查输出

返回浏览器，检查输出。

![](img/Image48066.jpg)

**图 9.16**

如你所见，`data-entry` div 现在不可见。

### 步骤 23：实现 AddNew 功能

现在，在 `list` div 中添加 `AddNew` 按钮，并按如下方式处理点击事件：

```
1.  <div [hidden]=”IsAddNew”>
2.     <h1>Customer List</h1>
3.     <input type=”button” value=”Add New” (click)=”AddNew()”>
4.     <table border=”1” >
5.  ……
7.  ……
8.       Save(){
9.         this.Customers.push(new Customer(“Karan”,”Arjun”));
10.      }
11.       AddNew(){
12.         this.IsAddNew=true;
13.      }
14.  }
```

### 步骤 24：检查输出

![](img/Image48119.jpg)

**图 9.17**

我希望你自己完成 `Cancel` 按钮的代码。这将是一个作业。

## 讨论 – 继续

`Property binding` 和 `interpolation` 都让我们在 UI 中显示最新值。

### 为什么使用 interpolation？

Interpolation 使绑定更简单。

假设我们在组件类中有一个变量 `CompanyName`，并且我们希望将其与一些硬编码字符串拼接后显示在文本框中。

使用属性绑定，语法如下：

```
1.  <input type=”text” [value]= “’Hello, the company name is’ + CompanyName” />
```

现在，相同的代码可以使用 interpolation 编写如下：

```
1.  <input type=”text” value=”Hello, the company name is {{CompanyName}}” />
```

你可以轻松地说，使用 interpolation 变得更容易。这给我们留下了一个问题：为什么我们需要属性绑定？

### 为什么使用属性绑定？

首先，你应该知道 `interpolation` 在后台会被转换为 `property binding`。

当值是非字符串值时，使用 interpolation 会遇到困难。为了证明这一点，做一件事：在我们的实验中，将 `Property binding` 改为 `interpolation`，然后检查输出。

我确信它不起作用。无论 `IsAddNew` 变量的值是什么，你一定注意到 `data-entry` div 始终不可见。

因此，如果值是非字符串值，则首选输入属性，因为 interpolation 将所有内容解释为字符串。

## 实验 – 继续

### 步骤 25：将组件属性连接到表单控件

首先，在组件类中创建两个属性。

```
1.  ……
2.       FirstName:string;
3.       LastName:string;
4.       constructor() {
5.  …..
```

接下来，按如下方式修改模板文件中的控件。

```
1.  ……
2.    <h1>Add New Customer</h1>
3.    First Name:
4.    <input type=”text” name=”FName” (change)=”ChangeFirstName($event.target.value)”>
5.    <br>
6.    Last Name:
7.    <input type=”text” name=”LName” (change)=”ChangeLastName($event.target.value)”>
8.    <br><br>
9.    <input type=”button” value=”Save” (click)=”Save()”> &nbsp;
10.  ……
```

接下来，在组件类中定义 `ChangeFirstName` 和 `ChangeLastName`，如下所示：

```
1.  ChangeFirstName(value){
2.         this.FirstName=value;
3.      }
4.       ChangeLastName(value){
5.         this.LastName=value;
6.      }
```

在上述代码中，`$event.target` 表示触发事件的控件，即对应的文本框。

现在，在组件类中，FirstName 和 LastName 始终保存着各自控件的最新状态。我们可以称之为反向单向绑定。每次文本框值改变时，变量都会更新。

### 步骤 26：修改 Save 以支持动态值

```
1.  ……
2.       Save(){
3.         this.Customers.push(new Customer(this.FirstName,this.LastName));
4.      }
5.       AddNew(){
6.  ……
```

### 步骤 27：检查输出

![](img/Image48167.jpg)

**图 9.18**

我不认为这是你期望的输出。你可能以为点击保存后，列表会重新显示并包含新行，但遗憾的是并没有。

不要阅读下一步。相反，思考一下，尝试找出原因。

![](img/Image48245.jpg)

**图 9.19**

### 步骤 28：修正问题

你能找出这个 bug 的原因吗？是 `IsAddNew`。最初它是 false，在 `AddNew` 之后，它的值变为 true，而我们在保存后没有将其切换回 false。因此，可见性没有切换回来。

将 save 函数修改为以下内容：

```
1.  ……
2.       Save(){
3.         this.Customers.push(new Customer(this.FirstName,this.LastName));
4.         this.IsAddNew=false;
5.      }
6.       AddNew(){
7.  ……
```

### 步骤 29：检查输出

![](img/Image48252.jpg)

**图 9.20**

## 讨论 – 继续

我相信你已经能够自己完成 `Cancel` 功能。

如果你检查我们到目前为止创建的内容，你会发现一个小 bug。按照以下步骤操作：

*   点击 `Add New`。你会看到控件没有值。
*   在控件中输入一些值。
*   点击 `Save` 或 `Cancel`。
*   再次点击 `Add New`。你会看到控件不是空的。它们应该是空的。

我相信你知道如何实现这一点。思考一下，看看是否能想出解决方案。

![](img/Image48290.jpg)

**图 9.21**

如你所知，在前面的步骤中，我们在变量和控件之间实现了 `反向单向绑定`，并且你已经知道如何使用 `属性绑定` 实现 `单向绑定`。通过同时使用两者，我们可以实现重置功能。

## 实验 – 继续

### 步骤 30：修改模板以实现重置

按如下方式修改模板文件中的内容：

```
1.  <h1>Add New Customer</h1>
2.    First Name: <input type=”text” name=”FName”
3.    [value]=”this.FirstName”
4.    (change)=”ChangeFirstName($event.target.value)”><br>
5.    Last Name: <input type=”text” name=”LName”
6.    [value]=”this.LastName”
7.    (change)=”ChangeLastName($event.target.value)”><br><br>
8.    <input type=”button” value=”Save” (click)=”Save()”> &nbsp;
```

### 步骤 31：修改组件类以实现重置

创建 `Reset` 函数如下，并在 `Save` 和 `Cancel` 方法中调用它。

```
1.  ……
2.       Reset(){
3.         this.FirstName=””;
4.         this.LastName=””
5.      }
6.       Save(){
7.         this.Customers.push(new Customer(this.FirstName,this.LastName));
8.         this.IsAddNew=false;
9.         this.Reset();
10.      }
11.       Cancel(){
```





12. `this.IsAddNew=false;`
13. `this.Reset();`
14. `}`
15. `…..`

**步骤 32：检查输出**

![](img/Image48369.jpg)

**图 9.22**

又一个令人沮丧的输出。发生了什么？我们来讨论一下。

## 讨论 – 继续

我们通过编写上述代码，在模板中的 **FirstName** 文本框和组件类中的 `FirstName` 属性之间创建了一个**属性绑定**（单向绑定）。

因此，`FirstName` 属性的值将显示在 **FirstName** 文本框中。每当 `FirstName` 属性发生变化时，文本框的值也会随之刷新。

`LastName` 属性也是如此。

现在的问题是，这两个变量最初都是*未赋值*的。因此，它们的值是 `undefined`。让我们通过将它们初始化为*空*字符串来填补这个空白。

**步骤 33：用空值初始化控件**

为此，在构造函数中调用相同的 `Reset` 函数。

1. `……`
2. `constructor() {`
3. `  this.IsAddNew=false;`
4. `  this.Reset();`
5. `  this.Customers=new Array<Customer>();`
6. `……`

**步骤 34：检查输出**

![](img/Image48421.jpg)

**图 9.23**

## 讨论 – 继续

在上面的输出中，我们手动实现了表单功能。

但这并不是必需的。Angular 内置了对表单的支持。

Angular 中关于表单有以下两种方法：

1. 模板驱动方法
2. 模型驱动方法，也称为响应式方法

在**模板驱动方法**中，我们将在模板文件中控制整个表单；而在**响应式方法**（即**模型驱动方法**）中，则在组件类中完成。

在本实验中，我们将采用模板驱动方法。稍后，我们将看到模型驱动方法。

**双向绑定**

模板驱动方法为我们提供了 `ngModel`，这是一个用于实现双向绑定的指令。

1. `ngModel` 负责控件与属性之间的绑定。
2. `ngModel` 处理 `undefined` 的情况。

**双向绑定**是一种 UI 和模型双向连接的绑定方法。

模型的值将显示在 UI 中。UI 会随模型的任何变化而更新；如果 UI 发生变化，模型也会随之更新。

`ngModel` 指令定义在名为 *FormsModule* 的 Angular 模块中。因此，要在我们的组件中使用 `ngModel`，我们需要在 `AppModule` 中导入 `FormsModule`。

## 实验 – 继续

**步骤 35：导入 FormsModule**

按如下方式在 `AppModule` 中导入 `FormsModule`：

1. `……`
2. `import {CustomerComponent} from ‘./Customer/customer.component’;`
3. `import {FormsModule} from ‘@angular/forms’;`
4. `@NgModule({`
5. `   declarations: [AppComponent, CustomerComponent],`
6. `   imports: [BrowserModule, FormsModule],`
7. `   providers: [],`
8. `……`

**步骤 36：删除不必要的代码**

从组件类中删除 `ChangeFirstName` 和 `ChangeLastName` 方法。

同时，删除构造函数中对 `Reset` 函数的调用。

1. `constructor() {`
2. `     this.IsAddNew = false;`
3. `     //this.Reset();`
4. `     this.Customers=new Array<Customer>();`
5. `     this.Customers.push(new Customer(“Sukesh”,”Marla”));`
6. `     this.Customers.push(new Customer(“Just”,”Compile”));`
7. `     this.Customers.push(new Customer(“Ram”,”Lakhan”));`
8. `  }`
9. `// ChangeFirstName(value){`
10. `//   this.FirstName=value;`
11. `//}`
12. `// ChangeLastName(value){`
13. `//   this.LastName=value;`
14. `//}`

**步骤 37：实现 ngModel**

将模板中的两个文本框修改为以下内容：

1. `……`
2. `   <h1>添加新客户</h1>`
3. `   名字：<input type=”text” name=”FName” [(ngModel)]=”this.FirstName”><br>`
4. `   姓氏：<input type=”text” name=”LName”`
5. `   [(ngModel)]=”this.LastName”><br><br>`
6. `   <input type=”button” value=”保存” (click)=”Save()”> &nbsp;`
7. `……`

**步骤 38：检查输出**

你将得到与之前相同的输出。

## 讨论 – 继续

接下来，我们将实现验证。我们将分以下两个阶段进行：

**阶段 1**：如果验证失败，在控件周围添加红色边框。

**阶段 2**：显示错误消息。

为了完成阶段 1，我们将使用 CSS，而最棒的是 `ngModel` 会根据条件动态地将 CSS 类应用于控件。我们只需定义这些类即可。

![](img/Image48430.jpg)

**图 9.24**

你可以注意到控件上附加了以下三个 CSS 类：

1. `ng-untouched`：表示控件尚未被触摸。将光标放入文本框然后移出焦点，`ng-untouched` 将变为 `ng-touched`。一旦被触摸，就不能再回到未触摸状态。
2. `ng-pristine`：表示控件的值未被修改。尝试将其更改为任何值，它将变为 `ng-dirty`。一旦变脏，就不能再回到原始状态。
3. `ng-valid`：表示控件包含有效值，当验证失败时会变为 `ng-invalid`。与其他两个不同，这个类会在有效和无效之间切换。

**如何附加验证？**

为此，我们将使用 HTML 属性，例如 *required*、*minlength*、*pattern* 等。

## 实验 – 继续

**步骤 39：定义样式**

打开 `src` 文件夹中的 `style.css`，并放入以下内容：

1. `.ng-invalid.ng-touched.ng-dirty{`
2. `   border: 1px solid red;`
3. `}`

**步骤 40：为控件附加验证**

按如下方式修改模板中的内容：

1. `……`
2. `<div [hidden]=”!IsAddNew”>`
3. `   <h1>添加新客户</h1>`
4. `   名字：<input type=”text” name=”FName”`
5. `   [(ngModel)]=”this.FirstName” required minlength=”3”><br>`
6. `   姓氏：<input type=”text” name=”LName”`
7. `   [(ngModel)]=”this.LastName” required minlength=”3”><br><br>`
8. `   <input type=”button” value=”保存” (click)=”Save()”> &nbsp;`
9. `   <input type=”button” value=”取消” (click)=”Cancel()” >`
10. `</div>`
11. `……`

根据上述代码，两个文本框都不接受空值，并且值必须至少包含 3 个字符。

**步骤 41：检查输出。**

我们还没有完全完成验证。因此，暂时不要点击 `保存` 按钮。

相反，只需检查格式，并尝试以下操作：

1. 确保开始时没有显示边框，因为控件尚未被触摸。
2. 将光标放入任意文本框然后移出焦点。由于控件尚未变脏，不应显示边框。
3. 将光标放入任意文本框，输入超过三个字符的值，然后移出焦点。由于控件有效，不应显示边框。
4. 将光标放入任意文本框，输入少于三个字符的值或留空，然后移出焦点。由于控件已被触摸、变脏且验证失败，应显示边框。

## 讨论 – 继续

现在我们已经完成了验证控件的格式化，接下来该显示错误消息了。

为此，我们可以使用 `ngModel` 指令暴露的属性。

如你所知，`ngModel` 是一个指令，从概念上讲它是一个 `TypeScript` *类*。

每次我们将指令附加到元素上时，都会创建该指令的一个实例，并与该元素关联。我们可以使用“模板引用变量”在模板中获取该实例的引用。

例如，请看以下代码：

![](img/Image48553.jpg)

**图 9.25**

`ngModel` 类实例将为我们提供以下七个表示控件状态的属性：

1. `touched` – 如果控件被触摸则为 true，否则为 false。





2.  `untouched` – 如果控件尚未被触碰，则为 true，否则为 false。

3.  `pristine` – 如果控件的值尚未更改，则为 true，否则为 false。

4.  `dirty` – 如果控件的值从未更改过，则为 true，否则为 false。

5.  `valid` – 如果控件的值有效，则为 true，否则为 false。

6.  `invalid` – 如果控件的值无效，则为 true，否则为 false。

7.  `error` – 如果控件的值有效，则为 null。当控件值无效时，它将是一个包含 `required`、`minlength`、`pattern` 等属性的对象——每个属性都是一个布尔值，指示哪个验证失败。

让我们进行演示并理解它。

## 实验 – 续

### 步骤 42：附加验证消息

将错误消息添加到两个控件中，如下所示：

```
1.  <div [hidden]=”!IsAddNew”>
2.     <h1>添加新客户</h1>
3.     名字：
4.     <input type=”text” name=”FName”
5.     [(ngModel)]=”this.FirstName” required minlength=”3”>
6.     <span>请输入名字</span>
7.     <span>名字至少需要 3 个字符</span>
8.     <br>
9.     姓氏：
10.     <input type=”text” name=”LName”
11.     [(ngModel)]=”this.LastName” required minlength=”3”>
12.     <span>请输入姓氏</span>
13.     <span>姓氏至少需要 3 个字符</span>
14.     <br><br>
15.     <input type=”button” value=”保存” (click)=”Save()”> &nbsp;
16.     <input type=”button” value=”取消” (click)=”Cancel()” >
17.  </div>
```

### 步骤 43：使用 ngModel 实例控制错误消息

如前所述，在模板引用变量中获取 `ngModel` 指令的实例，并控制错误消息的可见性。

```
1.  ……
2.     <input type=”text” name=”FName”
3.     [(ngModel)]=”this.FirstName” required minlength=”3” #F=”ngModel”>
4.     <span [hidden]=”!(F.dirty && F.errors?.required)”>请输入名字</span>
5.     <span [hidden]=”!(F.dirty && F.errors?.minlength)”>名字至少需要 3 个字符</span>
6.  ……
```

`LastName` 的错误消息将作为你的作业。请确保你尝试并完成它。

现在，如果你对 `hidden` 的赋值感到困惑，请阅读接下来的讨论。否则，直接跳到下一步。

## 讨论 – 续

我们来谈谈上述代码中赋给 `hidden` 属性的值：

1.  如果赋值的表达式结果为 *true*，它将隐藏元素。因此，我们需要最终结果为 *false* 才能看到错误消息。

2.  由于整个表达式被取反，我们希望括号内表达式的结果为 *true* 才能看到错误消息。

3.  如果控件值从未更改，括号表达式的结果为 *false*。简而言之，控件不是 dirty 状态。要看到错误消息，它必须是 dirty 状态。

4.  如果值有效，括号表达式的结果为 *false*。如果值无效，`error` 将返回一个对象，其中 `required` 为 *true* 或 `minlength` 为 *true*。

## 实验 – 续

## 步骤 44：检查输出

保存点击验证尚未完成。所以，不要跳到那里。

相反，只需检查错误消息，为此，请尝试以下操作：

1.  确保错误消息在开始时不可见，因为控件不是 dirty 状态。

2.  将光标放在任意文本框中并移出焦点。错误消息应保持不可见，因为控件尚未变为 dirty。

3.  将光标放在任意文本框中并输入一些值。现在它是 dirty 状态。如果任何验证失败，它应该开始显示错误消息。

## 讨论 – 续

接下来，我们必须控制 `Save` 按钮。

为此，我们将使用 `ngForm` 指令。

我们将 `ngModel` 附加到各个控件，而 `ngForm` 将附加到整个容器。

可以使用 *模板引用变量* 获取其引用，它将暴露与 `ngModel` 类似的属性，但它代表整个容器的状态。

例如，一旦任何控件变为 dirty，容器就会变为 dirty。

类似地，只有当所有控件都有效时，容器才有效。

### 步骤 45：控制按钮

将 `ngForm` 指令附加到我们的顶层 div 元素，该元素封装了整个数据录入界面。

接下来，使用模板引用变量获取该指令的引用。

最后，使用 `ngForm` 属性控制 `Save` 按钮，如下所示：

```
1.  <div [hidden]=”!IsAddNew” ngForm #myForm=”ngForm”>
2.     ………
3.     <input type=”button” value=”保存” (click)=”Save()” [disabled]=”myForm.invalid”>   &nbsp;
4.     <input type=”button” value=”取消” (click)=”Cancel()” >
5.  </div>
```

在上述代码中，你可以清楚地看到我们首先附加了 `ngForm` 指令，然后在 `myForm` 变量中获取了它的引用，最后如果任何内容无效，则禁用 `Save` 按钮。

## 步骤 46：检查输出

运行应用程序，你会注意到一个小问题。你还会在验证错误时看到 div 周围出现红色边框。

### 步骤 47：移除表单的红色边框

就像 `ngModel` 一样，`ngForm` 也会根据条件动态附加这六个 CSS 类。因此，红色边框是完全预期的。

将 `style.css` 更改为以下内容：

```
1.  .ng-invalid.ng-touched.ng-dirty:not([ngForm]){
2.     border: 1px solid red;
3.  }
```

## 步骤 48：检查输出

现在你将能够看到预期的输出。你会注意到当任何控件包含无效值时，`Save` 按钮会被禁用。

我用于错误消息的 CSS 组合仅用于演示目的。我强烈建议你尝试不同的组合并正确理解它。

## 讨论 – 续

我相信你们都在认真且专注地跟随并实践每一步。在这种情况下，你一定注意到了我们到目前为止创建的系统中的一个小问题。

*数据录入表单在保存和取消后没有重置状态。*

请按照以下步骤操作：

*   打开应用程序并点击 `AddNew`。
*   输入一些无效值。你会看到文本框周围出现红色边框以及相应的错误消息。
*   现在点击 `Cancel`。
*   再次点击 `AddNew`，你仍然会看到那些红色边框和错误消息。

![](img/Image48566.jpg)

**图 9.26**

可以通过使用 `ngForm` 类中的 `reset` 函数来解决这个问题。

因此，我们需要在组件类中获取 `ngForm` 的实例来调用其 `reset` 方法。

为了在组件类内部获取 `ngForm` 实例，我们可以使用 `ViewChild` 装饰器。

让我们看看演示。

## 实验 – 续

### 步骤 49：重置整个表单状态

获取附加到 `form` 标签的 `ngForm` 指令的访问权限，并重新定义 `Reset` 函数，如下所示：

```
1.  import {Component, ViewChild} from ‘@angular/core’;
2.  ……
3.    LastName: string;
4.     @ViewChild(‘myForm’) CustomerForm: NgForm;
5.     constructor() {
6.       this.IsAddNew = false;
7.  ……
8.     Reset() {
9.   *// this.FirstName = ‘’;
10.  *// this.LastName = ‘’;
11.       this.CustomerForm.reset();
12.    }
13.     Save() {
14.  ……
15.  ……
```

### 步骤 50：检查输出

现在你将看到一切正常工作。

#### 总结

我们已经到达第 6 站。

前往第 6 站的旅程非常漫长。我们涵盖了很多内容，但并不是非常深入。

让我们回顾一下本章学到的所有主题：

*   创建和使用 Angular 组件
*   Angular 插值
*   指令和 `ngFor` 指令简介
*   输入属性和属性绑定简介




*   属性绑定与插值的区别
*   输出属性与事件绑定简介
*   单向绑定
*   双向绑定
*   模板驱动表单简介
*   验证简介
*   模板引用变量
*   ViewChild 简介

## 第 10 章

## 使用 Bootstrap CSS 美化 Angular 界面

#### 简介

在前往站点 7 的下一段旅程中，我们将基于之前的实验进行增强，使其更上一层楼。

如果你还没有这个项目，可以从 GitHub 仓库下载。

（你可以在引言章节找到 GitHub 仓库的链接。）

这是一个简单的 10 步实验，它将基于之前的实验，并使用 Bootstrap 进行美化。

请注意，本实验的目的并非学习 Bootstrap（一种业界流行的 CSS 框架）。本章旨在学习如何在 Angular 应用中引入第三方库。我们还将学习如何在 Angular 中使用 `ngClass` 指令。

### 实验 2：Bootstrap 实战

#### 第 1 步：创建项目副本

最好创建上一个项目的副本，而不是直接修改它，然后将项目从 `lab1-ng` 重命名为 `lab2-ng`。这需要两步：

1.  打开 `package.json` 和 `package.lock.json`。这两个文件都包含一个 `name` 属性，将其设置为 `lab2-ng`。

2.  现在在 `angular.json` 文件中搜索 `lab1-ng`，并将所有出现的地方替换为 `lab2-ng`。

#### 第 2 步：安装 Bootstrap

接下来，使用 `npm install bootstrap --save` 命令安装 Bootstrap CSS。

请确保在 `npm install` 命令中使用 `--save` 标志。否则 `package.json` 中的 `dependencies` 部分不会更新。另外，注意 `npm` 命令和库名都是区分大小写的。

#### 第 3 步：将 Bootstrap 引入项目

打开 `angular.json` 文件，在 `styles` 部分引入 `bootstrap.min.css`，如下所示。

![](img/Image48642.jpg)

**图 10.1**

#### 第 4 步：运行项目

使用 `ng serve --open` 命令运行项目。你会在第一次执行时就注意到 Bootstrap 的效果。你会看到文本字体和表格边框发生了变化。

![](img/Image48650.jpg)

**图 10.2**

#### 第 5 步：移除多余的标题

从 `app.component.html` 中移除“Simple Angular example”标题。

#### 第 6 步：重新设计客户列表

让我们为 `customer-list` 部分应用一些 Bootstrap 类，如下所示：

```
<div class="container-fluid pt-3">
  <div class="card" [hidden]="IsAddNew">
    <h5 class="card-header">Customer List</h5>
    <div class="card-body">
      <div class="card-title">
        <i class="fas fa-user-plus"></i>
        <input type="button" value="+ Add New" class="btn btn-primary fas fa-coffee fa-xs" (click)="AddNew()">
      </div>
      <table class="table table-striped table-bordered">
        <thead class="thead-dark">
          <tr>
            <th scope="col">First Name</th>
            <th scope="col">Last Name</th>
          </tr>
        </thead>
        <tbody>
          <tr *ngFor="let item of Customers">
            <td scope="row">{{item.FName}}</td>
            <td>{{item.LName}}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
  <!-- Data entry form will be added here -->
</div>
```

不必过于担心上一步中使用的 CSS 类。本章的目标不是学习 Bootstrap，而是学习如何使用第三方库。

#### 第 7 步：重新设计数据录入界面

现在，轮到数据录入界面了。

```
<!-- Table was added in the previous step here -->
<div class="card" [hidden]="!IsAddNew" ngForm #myForm="ngForm">
  <h5 class="card-header">Add New Customer</h5>
  <div class="card-body">
    <div class="form-group">
      <label for="FName">First Name: </label>
      <input class="form-control" type="text" name="FName"
        [(ngModel)]="this.FirstName" required minlength="3" #F="ngModel">
      <!-- error -->
      <div class="alert alert-danger" [hidden]="!(F.dirty && F.errors?.required)">
        Enter First Name
      </div>
      <div class="alert alert-danger" [hidden]="!(F.dirty && F.errors?.minlength)">
        Minimum 3 characters needed for First Name
      </div>
    </div>
    <div class="form-group">
      <label for="LName">Last Name:</label>
      <input class="form-control" type="text" name="LName"
        [(ngModel)]="this.LastName" required minlength="3" #L="ngModel">
      <!-- error -->
      <div class="alert alert-danger" [hidden]="!(L.dirty && L.errors?.required)">
        Enter Last Name
      </div>
      <div class="alert alert-danger" [hidden]="!(L.dirty && L.errors?.minlength)">
        Minimum 3 characters needed for Last Name
      </div>
    </div>
    <input type="button" class="btn btn-success" value="Save" (click)="Save()" [disabled]="myForm.invalid"> &nbsp;
    <input type="button" class="btn btn-danger" value="Cancel" (click)="Cancel()">
  </div>
</div>
```

#### 第 8 步：检查输出

让我们看看现在的效果。

![](img/Image48725.jpg)

**图 10.3**

![](img/Image48827.jpg)

**图 10.4**

很漂亮，不是吗？我们还可以让它更好。

## 讨论

Bootstrap 提供了两个有用的类来处理验证：`is-valid` 和 `is-invalid`。

我们可以使用 Angular 中的属性指令 `ngClass` 动态地应用这些类。

## 实验 – 继续

#### 第 9 步：附加 Bootstrap CSS 验证消息

首先，移除 `style.css` 中当前定义的所有 CSS。

然后，为两个文本框添加 `ngClass` 指令，如下所示：

```
<input class="form-control"
       [ngClass]="{'is-valid':F.valid,'is-invalid':F.invalid}" type="text" name="FName"
       [(ngModel)]="this.FirstName" required minlength="3" #F="ngModel">
<!-- 对 Last Name 做同样的操作 -->
```

## 第 10 步：检查输出

重新检查输出：

![](img/Image48834.jpg)

**图 10.5**

![](img/Image48843.jpg)

**图 10.6**

#### 总结

我们已经到达站点 7。在这段旅程中，我们学习了如何在 Angular 中引入第三方库以及如何美化界面。在进入下一章之前，请多加练习。

我们下一章见。

我们有一个关于 Angular 样式的独立章节，将在其中详细讨论 Angular 中的样式问题。

## 第 11 章

## 身份验证

#### 简介

在第 4 部分的上一章中，我们踏上了前往站点 8 的旅程。

在本实验中，我们将为上一个实验中创建的项目添加身份验证功能。

完成本实验后，只有经过身份验证的用户才能访问 `CustomerComponent`。

以下是本实验结束时我们将得到的效果预览。

![](img/Image48910.jpg)

**图 11.1**

### 实验 3 – Angular 身份验证

#### 第 1 步：创建项目副本

创建上一个项目的备份，并将其重命名为 `lab3-ng`。

#### 第 2 步：创建登录组件

在 `app` 文件夹内创建一个新的 `Login` 文件夹，并创建一个新的 Angular 组件 `Login`，如下所示：

```
login.component.ts
import {Component} from '@angular/core';
@Component({
   selector: 'login',
   templateUrl: './login.component.html'
})
```





```
export class LoginComponent {

}
```

```
<!-- login.component.html -->
<div class="container-fluid pt-3">
   <div class="card">
     <h5 class="card-header">Login</h5>
     <div class="card-body">
       <div class="form-group">
         <label for="UserName">User Name: </label>
         <input class="form-control" type="text" name="UserName">
       </div>
       <div class="form-group">
         <label for="Password">Password:</label>
         <input class="form-control" type="text" name="Password">
       </div>
       <input type="button" class="btn btn-success" value="Login">
     </div>
   </div>
</div>
```

### 第 3 步：将组件添加到模块

我想我不需要重复，“每个 Angular 组件都属于一个 Angular 模块。”

让我们将 `LoginComponent` 添加到 `AppModule` 中。

```
……
import {CustomerComponent} from './Customer/customer.component';
import {LoginComponent} from './Login/login.component';
@NgModule({
   declarations: [AppComponent, CustomerComponent,LoginComponent],
   imports: [BrowserModule, FormsModule],
……
```

### 第 4 步：显示登录组件

现在，打开 `app.component.html` 并将 `CustomerComponent` 替换为 `LoginComponent`。

```
<!-- <customer></customer> -->
<login></login>
```

### 第 5 步：检查输出

如果尚未执行，请使用 `ng serve --open` 命令运行应用程序。

![](img/Image48957.jpg)

**图 11.2**

## 讨论

上次我们处理输入控件时，采用的是**模板驱动方法**。

这次我们将采用**模型驱动方法**，也称为**响应式方法**。这是一种更清晰的方法，与**模板驱动**不同，你会注意到验证决策将在组件类中做出。

## 实验 – 继续

## 第 6 步：准备 LoginComponent 类以进行验证

响应式方法中的验证涉及以下两个步骤：

1.  创建一个 FormGroup。

2.  在 FormGroup 内部创建 FormControls。

将 `LoginComponent` 类中的代码更改为以下内容：

```
import {Component} from '@angular/core';
import {FormGroup, FormControl, Validators} from '@angular/forms';
@Component({
   selector: 'login',
   templateUrl: './login.component.html'
})
export class LoginComponent {
   loginForm = new FormGroup({
     UserName: new FormControl('',[Validators.required,Validators.minLength(6)]),
     Password: new FormControl('',[Validators.required,Validators.minLength(6)]),
  });
}
```

***注意：*** 上述代码中的每个 `FormControl` 属性都代表我们 UI（模板）中的一个控件，你会注意到验证是在组件类中指定的，而不是在模板中。

## 讨论 – 继续

在模型驱动方法中，我们将使用诸如 `formGroup` 和 `formControlName` 之类的指令来处理表单控件。这两个指令都声明为 Angular 模块 `ReactiveFormsModule` 的一部分。

因此，为了使这些指令在 `CustomerComponent` 中可访问，我们必须在 `AppModule` 中导入 `ReactiveFormsModule`。

## 实验 – 继续

## 第 7 步：导入 ReactiveFormsModule

通过从 `@angular/Forms` 导入，在 `app.module.ts` 中获取对 `ReactiveFormsModule` 的访问权限。

```
import {NgModule} from '@angular/core';
import {FormsModule, ReactiveFormsModule} from '@angular/forms';
import {BrowserModule} from '@angular/platform-browser';
……
```

接下来，在附加到 `AppModule` 的 `@NgModule` 装饰器的 imports 部分中指定它。

```
……
import {CustomerComponent} from './Customer/customer.component';
import {LoginComponent} from './Login/login.component';
@NgModule({
   declarations: [AppComponent, CustomerComponent,LoginComponent],
   imports: [BrowserModule, FormsModule,ReactiveFormsModule],
   providers: [],
……
```

## 第 8 步：在模板中绑定 FormGroup

现在我们的组件类已经准备好了 `FormGroup` 实例，让我们使用 `formGroup` 和 `formControlName` 指令将其连接到模板。

```
<!-- login.component.html -->
<div class="container-fluid pt-3">
   <div class="card">
     <h5 class="card-header">Login</h5>
     <div class="card-body" [formGroup]="loginForm">
       <div class="form-group">
         <label for="UserName">User Name: </label>
         <input class="form-control" formControlName="UserName" type="text" name="UserName">
       </div>
       <div class="form-group">
         <label for="Password">Password:</label>
         <input class="form-control" formControlName="Password" type="text" type="password"
name="Password">
       </div>
       <input type="button" class="btn btn-success" value="Login" >
     </div>
   </div>
</div>
```

## 第 9 步：设置验证

现在，就像上一个实验一样，让我们使用以下代码设置验证消息：

```
<!-- login.component.html -->
<div class="container-fluid pt-3">
   <div class="card">
     <h5 class="card-header">Login</h5>
     <div class="card-body" [formGroup]="loginForm">
       <div class="form-group">
         <label for="UserName">User Name: </label>
         <input class="form-control"
         [ngClass]="{'is-valid':loginForm.controls.UserName.valid,'is-invalid':loginForm.controls.UserName.invalid}"
         formControlName="UserName" type="text" name="UserName">
         <div class="alert alert-danger"
         [hidden]="!(loginForm.controls.UserName.dirty && loginForm.controls.UserName.errors?.required)">
           请输入用户名
         </div>
         <div class="alert alert-danger" [hidden]="!(loginForm.controls.UserName.dirty && loginForm.controls.UserName.errors?.minlength)">
           用户名至少需要 6 个字符
         </div>
       </div>
       <div class="form-group">
         <label for="Password">Password:</label>
         <input class="form-control"
         [ngClass]="{'is-valid':loginForm.controls.Password.valid,'is-invalid':loginForm.controls.Password.invalid}"
         formControlName="Password" type="password"name="Password">
         <div class="alert alert-danger"
         [hidden]="!(loginForm.controls.Password.dirty && loginForm.controls.Password.errors?.required)">
           请输入密码
         </div>
         <div class="alert alert-danger" [hidden]="!(loginForm.controls.Password.dirty && loginForm.controls.Password.errors?.minlength)">
           密码至少需要 6 个字符
         </div>
       </div>
       <input type="button" class="btn btn-success" value="Login" [disabled]="loginForm.invalid" >
     </div>
   </div>
</div>
```

如你所见，验证是在视图类中指定的。

## 第 10 步：检查输出

运行应用程序，并使用有效和无效的值进行测试。

![](img/Image49024.jpg)

**图 11.3**

![](img/Image49035.jpg)

**图 11.4**

## 第 11 步：配置无效登录

在连接到真实的 REST API 并进行身份验证之前，让我们正确配置“`用户名或密码无效`”消息。

首先，在组件类中定义 `IsAuthenticatiionFailed` 变量，并在构造函数中将其设置为 false。

```
……
   IsAuthenticatiionFailed: boolean;
   constructor() {
```





4.  `     this.IsAuthenticatiionFailed = false;`

5.  `  }`

6.  `……`

按如下方式处理登录事件：

```
……
           Minimum 6 characters needed for Password
         </div>
       </div>
       <input type="button" class="btn btn-success" value="Login" (click)="login()" [disabled]="loginForm.invalid" >
     </div>
   </div>
</div>
```

定义登录方法，并将 `IsAuthenticatiionFailed` 设置为 true。

```
……
   login() {
     this.IsAuthenticatiionFailed = true;
  }
}
```

在登录模板顶部添加错误消息，如下所示：

```
……
   <div class="card">
     <h5 class="card-header">Login</h5>
     <div class="card-body" [formGroup]="loginForm">
       <div class="form-group">
         <div class="alert alert-danger" *ngIf="IsAuthenticatiionFailed" >
           Invalid User Name or Password
         </div>
         <label for="UserName">User Name: </label>
```

## 讨论 – 续

**你是否注意到了上述代码中的** `ngIf` **？**

与 `ngFor` 类似，它是一个结构型属性。

与 `hidden` 不同，它不会隐藏或显示元素。相反，它会从 DOM 本身创建和移除元素。

## 实验 – 续

**步骤 12：检查输出**

如你所见，初始状态下它是可见的。打开开发者工具，在元素部分检查 HTML。

![](img/Image49156.jpg)

**图 11.5**

如你所见，一开始 `IsAuthenticatiionFailed` 为 false，因此该 div 元素甚至没有被渲染。

![](img/Image49226.jpg)

**图 11.6**

![](img/Image49262.jpg)

**图 11.7**

输入一些虚拟值并点击登录。现在你可以看到错误消息。

打开开发者工具，在元素部分检查 HTML。

如你所见，由于值为 true，div 被动态创建。如果 `IsAuthenticatiionFailed` 变为 false，它又会再次被移除。

![](img/Image49269.jpg)

**图 11.8**

## 讨论 – 续

现在我们已经准备好了初始 UI 相关的内容，包括凭据无效时应该发生什么，接下来的问题是：凭据有效时应该发生什么？

明确的答案是——成功登录后，我们应该重定向到 `CustomerComponent`，并维护一些状态来指示用户已通过身份验证。

是时候引入一个新的 Angular 概念了，叫做 `Angular Routing`。

路由是许多技术中常用的术语。其核心思想是根据不同的 URL 在 UI 中显示不同的内容。我们向路由引擎提供一些数据，路由引擎根据这些数据为不同的 URL 显示 UI。

## 实验 – 续

**步骤 13：定义路由**

首先，在 app 文件夹中创建一个名为 `Routes` 的文件夹。然后在该文件夹内创建一个文件 `app.routes.ts`，内容如下：

```
import {Routes} from '@angular/router';
import {LoginComponent} from '../Login/login.component';
import {CustomerComponent} from '../Customer/customer.component';
export const AppRoutes:Routes=[
   {path:'login',component:LoginComponent},
   {path:'customer',component:CustomerComponent}
];
```

这段代码是不是很直观？我们现在有两条简单的路由——当 URL 为 login 时，显示 `LoginComponent`；当 URL 为 customer 时，显示 `CustomerComponent`。

**步骤 14：导入 RouterModule**

现在，要在 Angular 中配置路由，我们需要在 `AppModule` 中导入 `RouterModule`。

```
……
import {RouterModule} from '@angular/router';
import {AppRoutes} from './Routes/app.routes';
@NgModule({
   declarations: [AppComponent, CustomerComponent,LoginComponent],
   imports: [BrowserModule, FormsModule,ReactiveFormsModule
   ,RouterModule.forRoot(AppRoutes)],
   providers: [],
   bootstrap: [AppComponent],
})
export class AppModule {}
```

如你所见，在导入 `RouterModule` 时，我们将 `Routes` 传递给了它。

## 讨论 – 续

如你所见，这次导入有些不同。这次我们没有在 `NgModule` 装饰器的 imports 部分提及类名，而是调用了 `RouterModule` 类的 `forRoot` 方法，并将我们的 `Routes` 对象作为参数传递。这将在应用程序中配置路由。

**这些不同的组件将在哪里显示？**

我们在应用程序中配置了路由，指定了哪个 URL 对应哪个组件，但问题是，这些组件会在 UI 的哪个位置显示呢？

这时，Angular 组件 `RouterOutlet` 就登场了。

`RouterOutlet` 将作为其他组件的占位符。

是不是文字太多，让你感到困惑了？让我们直接进入实验，在那里讨论。

## 实验 – 续

**步骤 15：在 AppComponent 中添加占位符**

在前面的某个步骤中，我们将 `AppComponent` 中的 `CustomerComponent` 替换为了 `LoginComponent`。现在，让我们将 `LoginComponent` 替换为 `RouterOutletComponent`。

```
<!-- <customer></customer> -->
<!-- <login></login> -->
<router-outlet></router-outlet>
```

在上述代码中，`router-outlet` 是 `RouterOutletComponent` 的选择器。

**步骤 16：检查输出**

切换回浏览器，在 URL 后追加 "`/login`"。

你将看到 `LoginComponent`。

![](img/Image49318.jpg)

**图 11.9**

![](img/Image49311.jpg)

**图 11.10**

将 "`/login`" 替换为 "`/customer`"，你将看到 `CustomerComponent`。

## 讨论 – 续

让我们理解整个流程：

![](img/Image49394.jpg)

**图 11.11**

1.  对于 SPA，第一个请求会发送到服务器。服务器会向客户端发送初始的 *HTML* 响应。对于 Angular 应用程序，它是一个包含 `AppComponent` 的 `index.html` 文件。

2.  由于路由是在客户端配置的，路由系统会根据 URL 搜索匹配的路由。

3.  根据路由信息，相应的组件会被加载到 UI 中。对于 Angular 应用程序，组件会被加载到 `RouterOutlet` 中。

## 实验 – 续

**步骤 17：默认路由**

你是否注意到了初始输出？我是说，当 URL 仅为 `http://localhost:[端口号]` 时。

它会显示一个漂亮的空白屏幕。

让我们配置路由，使其在路径为空时返回 `LoginComponent`。为此，向我们的 `RouteCollection` 添加更多路由，如下所示：

```
……
export const AppRoutes:Routes=[
   {path:'login',component:LoginComponent},
   {path:'customer',component:CustomerComponent},
   {path:'',redirectTo:'login',pathMatch:'full'}
];
```

## 讨论 – 续

**什么是 pathMatch？**

你可以跳过这个解释，因为它并不重要。

当 `pathMatch` 设置为 `full` 时，整个 URL 路径必须匹配，并且会被路由匹配算法消耗。

## 实验 – 续

**步骤 18：检查输出**

切换回浏览器，将 URL 改为简单的 `http://localhost:[端口号]`，你应该会看到 `LoginComponent`。

![](img/Image49432.jpg)

**图 11.12**

**步骤 19：用随机字符串测试**

现在，在 URL 中使用随机字符串测试应用程序。

例如，尝试 `http://localhost:[端口号]/asd` 并检查输出。

我们会看到一个空白屏幕。打开开发者工具检查错误。目前，没有配置与指定当前 URL 模式匹配的组件。

![](img/Image49471.jpg)

**图 11.13**

**步骤 20：定义无效路由**




在我们的 `RouteCollection` 中添加一条路由，用于支持无效路径。

```
1.  `……`
2.  `export const AppRoutes:Routes=[`
3.  `   {path:’login’,component:LoginComponent},`
4.  `   {path:’customer’,component:CustomerComponent},`
5.  `   {path:’’,redirectTo:’login’,pathMatch:’full’},`
6.  `   {path:’**’,redirectTo:’customer’,pathMatch:’full’},`
7.  `];`
```

**第 21 步：检查输出**

如果你发现任何不是“`/login`”或“`/customer`”的路径，它都会重定向到 `CustomerComponent`。

## 讨论 – 继续

我们已经完成了设置过程，但还没有学会如何进行导航。这可以通过 `Router` 服务来实现。

我们已经了解了 Angular 中的*组件*、*指令*和*模块*。现在是时候了解*服务*了。

在本书的后续部分，我们将创建自己的自定义服务，届时会更详细地讨论服务。现在，请尽量理解当前内容，然后进入实验的下一步。

那么，让我们从理解什么是*服务*开始。

***服务*** *是 Angular 的一个特性，代表可注入的应用程序逻辑。*

让我们分别解释这两个词。

**应用程序逻辑**

它可以是任何应用程序逻辑。

**示例**：它可以是将消息记录到某处的逻辑，也可以是帮助我们与外部 API 通信的逻辑，还可以是帮助我们在服务器上创建文件的逻辑。

作为 Angular 应用程序的最佳实践，逻辑不应作为组件的一部分编写，而应移至服务中。我们很快会将 `LoginComponent` 中的所有逻辑移到一个独立的服务中。

**可注入的**

请看下图：

病人需要药物。

药物由医生注入病人体内。

在你看来，谁更了解药物，医生还是病人？答案是医生（除非病人也是医生）。

![](img/Image49508.jpg)

**图 11.14**

想象一下，如果病人需要自己注射药物。你能想到什么问题吗？他们可能不知道要注射多少药物。他们可能会忘记更换针头。

将这一责任交给医生，病人的生活就变得轻松了。

在编程世界中，这被称为**依赖注入**——依赖项将从外部注入到应用程序的各个部分。

![](img/Image49587.jpg)

**图 11.15**

需要对象的组件不会初始化该对象，而只会声明它，框架会在运行时初始化并注入该对象。

在这种情况下，执行注入工作的框架就是我们的医生。应用程序中需要依赖的部分是病人，而药物就是病人所需的对象。

Angular 内置了对**依赖注入**（简称 *DI*）的支持，并且 Angular 服务是*可注入的*。

简而言之，我们不会显式创建 Angular 服务的实例。相反，Angular 会负责服务的实例化。这些服务实例会被注入到需要它们的地方。

还是不太清楚？让我们回到实验。

一旦我们开始创建自定义服务，我们会进一步讨论。

## 实验 – 继续

**第 22 步：获取 Router 服务的引用**

按如下方式修改 `LoginComponent` 的构造函数：

```
1.  `……`
2.  `import {Router} from ‘@angular/router’;`
3.  `@Component({`
4.  `   selector: ‘login’,`
5.  `   templateUrl: ‘./login.component.html’,`
6.  `})`
7.  `……`
8.  `   constructor(private router:Router) {`
9.  `     this.IsAuthenticatiionFailed = false;`
10. `……`
```

如上述代码所示，我们没有显式创建 `RouterService` 的实例，而只是将其声明为构造函数参数。

***注意：*** 通过在 `constructor` 参数前添加 `private` 关键字，我们将其变成了一个 `TypeScript 简写属性`。

**第 23 步：处理登录事件**

在 `LoginComponent` 类中，将 login 方法修改为以下内容：

```
1.  `……`
2.  `   login() {`
3.  `     if (`
4.  `       this.loginForm.controls.UserName.value == ‘Admin1’ &&`
5.  `       this.loginForm.controls.Password.value == ‘Admin1’`
6.  `    ) {`
7.  `       this.router.navigate([‘customer’]);`
8.  `    } else {`
9.  `       this.IsAuthenticatiionFailed = true;`
10. `    }`
11. `  }`
12. `……`
```

这是一个简单的代码。我们根据一些静态值来验证凭据。如果凭据有效，则重定向到 `CustomerComponent`，否则显示“*无效的用户名或密码*”消息。

**第 24 步：检查输出**

返回浏览器，向登录路由发送请求。输入任意凭据（用户名不是 Admin1，密码是 Admin1），然后点击 `Login`。你应该会看到“*无效的用户名或密码*”错误消息。

接下来，输入用户名 Admin，密码 Admin，然后尝试。你应该会被重定向到 `CustomerComponent`。

**第 25 步：实现注销和用户问候消息**

在 `CustomerComponent` 模板中添加一个注销链接以及一条问候消息，如下所示：

```
1.  `<nav class=”navbar navbar-dark bg-dark justify-content-end”>`
2.  `   <span class=”navbar-brand mb-0 h1”>Welcome Sukesh,</span><a class=”navbar-brand mb-0 h1 underline “ href=’/login’ ><u>Logout</u></a>`
3.  `</nav>`
4.  `<div class=”container-fluid pt-3”>`
5.  `   <div class=”card” [hidden]=”IsAddNew”>`
6.  `     <h5 class=”card-header”>Customer List</h5>`
7.  `     <div class=”card-body”>`
8.  `……`
```

**第 26 步：使用无效凭据检查输出**

![](img/Image49642.jpg)

**图 11.16**

**第 27 步：使用有效凭据检查输出**

![](img/Image49676.jpg)

**图 11.17**

## 讨论 – 继续

我们已经完成了几乎所有 UI 和导航步骤。现在，让我们启动服务器（REST API），进行实时身份验证。

首先，让我们了解身份验证在 SPA 中是如何工作的：

**1 – 从服务器获取身份验证令牌**

![](img/Image49684.jpg)

**图 11.18**

![](img/Image49720.jpg)

**图 11.19**

**2 – 在客户端保护路由**

![](img/Image49754.jpg)

**图 11.20**

![](img/Image49788.jpg)

**图 11.21**

除非用户拥有有效的令牌，否则不允许访问受保护的路由。

**3 – 保护服务器资源**

到目前为止，我们通过 REST API 调用获取了身份验证令牌。这是我们到目前为止唯一的服务器调用。一个实时应用程序会有更多的 API 调用，例如很快我们将在 `CustomerComponent` 中发起 REST 调用，以将客户列表与动态数据绑定。

很快你也会看到这一点。这些 API 与身份验证 API 的区别在于安全性。

身份验证 API 对所有人开放，而其他 API 仅对经过身份验证的用户开放。因此，在进行 REST 调用时，必须在请求头中将令牌传递给服务器。服务器仅在令牌有效时返回响应，否则返回错误。

![](img/Image49849.jpg)

**图 11.22**

**上一步中的令牌是什么？**

它是一个由服务器应用程序创建并返回给客户端的字符串值。令牌充当客户端的*身份证*。客户端在每次后续请求中将该令牌发送给服务器。

服务器验证令牌，仅当令牌有效且未过期时才返回响应。

**如何确保令牌的安全性？**

首先需要的是 SSL，它确保通过线路交换的所有数据都是加密的。

其次，它取决于我们遵循的令牌标准。最常用的是 JWT，即 JSON Web 令牌。

JWT 的官方定义如下：





“JSON Web Token (JWT) 是一种开放标准（RFC 7519），它定义了一种紧凑且自包含的方式，用于在各方之间以 JSON 对象的形式安全地传输信息。由于该信息经过数字签名，因此可以被验证和信任。JWT 可以使用密钥（通过 HMAC 算法）或使用 RSA 或 ECDSA 的公钥/私钥对进行签名。”

由于它已签名，因此在传输过程中任何人都无法修改。

令牌还具有有效期。服务器在有效期过后会将令牌视为无效。

我们是否要创建一个用于生成令牌的 REST API？

我们不会从头构建 REST API。我们将为您提供一个示例演示用途的 REST API 代码，该代码会根据一些静态值验证用户名和密码，然后在用户有效的情况下返回 JWT 令牌作为响应。

演示服务器代码在哪里？

您将在下一步中了解。

## 实验 – 继续

### 步骤 28：准备服务器

请按照以下步骤启动您的演示服务器：

1. 从本书的 GitHub 仓库的 `station 8/chapter 11` 文件夹中下载服务器代码。
2. 启动命令提示符，导航到服务器文件夹内。
3. 执行 `npm install`。
4. 现在执行 `node server.js` 命令。

   ![](img/Image49927.jpg)

   **图 11.23**

   这将启动服务器。

   让它保持在后台运行。

### 步骤 29：在登录组件中获取 HttpClient 服务的访问权限

借助以下代码，在 `LoginComponent` 中获取 `HttpClient` 服务的引用：

```
……
import {HttpClient} from ‘@angular/common/http’;
@Component({
   selector: ‘login’,
   templateUrl: ‘./login.component.html’,
})
export class LoginComponent {
……
   constructor(private router: Router,private httpClient:HttpClient) {
     this.IsAuthenticatiionFailed = false;
  }
……
}
```

请记住，`HttpClient` 是一个服务。它将在运行时由 Angular 框架自动注入。

### 步骤 30：检查输出

您会注意到应用程序将停止工作。请为此检查 Chrome 开发者工具。

![](img/Image49976.jpg)

**图 11.24**

让我们讨论这个错误。

## 讨论 – 继续

Angular 中的每个组件和指令都属于某个 Angular 模块。

**但是服务呢？**

只有当 `AngularInjectors` 配置了 `providers` 时，服务才能工作。

**什么是注入器和提供者？**

*注入器* 是根据配置的 *提供者* 创建并在需要的地方注入服务实例的对象。

我们将在下一章中进一步讨论 *注入器*。

*提供者* 是向 Angular 框架的 *依赖注入* 系统发出的指令，用于决定如何获取依赖值。

**如何将注入器与提供者一起配置？**

有以下三种方式可以实现：

1. `Component` 装饰器允许我们这样做。
2. `NgModule` 装饰器允许我们这样做。
3. `Injectable` 装饰器允许我们这样做。
4. 创建一个独立的 *Angular 模块*，在其 `NgModule` 装饰器中配置 *注入器*，然后将该 *Angular 模块* *导入* 到我们的 *Angular 模块* 中。

我们将在本书中讨论所有四种方法。这次让我们看看第四种方法。

**自定义 Angular 模块和导入方法**

前三种方法非常简单直接。第四种方法有点奇怪。它要求我们创建一个自定义的 *Angular 模块*，然后使用第三种方法配置 *注入器*，最后将该 *模块* 导入到我们的 *Angular 模块* 中。当我们将一个 *Angular 模块* 导入到另一个模块时，它们的 *providers* 会合并。

这些模块在逻辑上被称为 **服务模块**。

您一定在想为什么要绕这么大一个弯。让我给您一个场景：

1. 假设我们有一个 *ServiceX*，我们的 *ABCDComponent* 依赖于它。要在 *ABCDComponent* 中使用 *ServiceX*，我们必须使用前三种方法之一配置 *注入器*。
2. 现在令人惊讶的是，*ServiceX* 依赖于 *ServiceY* 和 *ServiceZ*。因此，仅为 *ServiceX* 配置 *注入器* 是不够的。我们还需要为 *ServiceY* 和 *ServiceZ* 配置 *注入器*，并且对于 *ServiceY* 和 *ServiceZ* 所依赖的每一个其他依赖项也是如此。

对于服务的消费者（即组件 *ABCDComponent*）来说，这不是工作量太大了吗？

1. 因此，创建 *服务* 的程序员会创建一个 *Angular 模块*。我们称之为 *ServiceModule*。
2. 他会在该 *ServiceModule* 的 `NgModule` 装饰器中为 *ServiceX* 以及层次结构中的所有其他 *服务* 配置 *注入器*。
3. 负责 *ABCDComponent* 的程序员只需将 *ServiceModule* *导入* 到包含 *ABCDComponent* 的 *模块* 中。
4. 在内部，*ServiceModule* 中定义的所有提供者将与 *ABCDComponent’sModule* 合并，从而使开发人员的工作更轻松。

对于可重用库来说，这是一种方便的方法。

通常，每当您考虑使用可重用的第三方服务时，您总会找到一个需要导入到目标 *Angular 模块* 中的 *Angular 模块*。

最重要的是，让我告诉您，这个概念对您来说并不陌生。您已经在 `AppModule` 中导入了 Browser Module，它负责为 DOM 操作服务配置 *注入器*。

同样，对于 *RouterModule*，您也采用了相同的解决方案。它被导入到 *AppModule* 中，以便 *注入器* 能够将 *RouterService* 的实例注入到 Customer Component 中。

**对于 HttpClient，我们是否有类似的 ServiceModule 快捷方式？**

* 在内部，`HttpClient` 服务依赖于其他一些 Angular 服务。
* 因此，仅为 `HttpClient` 注册 *注入器* 是不够的。我们还需要注册所有其他依赖的服务。

因此，Angular 团队通过提供 `HttpClient` 模块简化了我们的工作。只需将其导入到我们的 `AppModule` 中，一切就完成了。

理解上述查询时出现一些困惑是很常见的。在完成下一章后重新阅读它，就会变得清晰。

## 实验 – 继续

### 步骤 31：在 AppModule 中导入 HttpClientModule

向 `AppModule` 添加如下代码：

```
……
import {AppRoutes} from ‘./Routes/app.routes’;
import {HttpClientModule} from ‘@angular/common/http’;
@NgModule({
   declarations: [AppComponent, CustomerComponent,LoginComponent],
   imports: [BrowserModule, FormsModule,ReactiveFormsModule, HttpClientModule
   ,RouterModule.forRoot(AppRoutes)],
   providers: [],
……
```

## 实验 – 继续

### 步骤 32：检查输出

最终，您将看到零错误，但不要期望有任何不同的输出，因为我们除了获取引用之外什么也没做。

## 实验 – 继续

### 步骤 33：调用 API

将 `LoginComponent` 中的 login 方法更改为以下代码：

```
……
   login() {
     this.httpClient.post(“http://localhost:4000/signin”,this.loginForm.value)
     .subscribe((response:{Token:string})=>{
       if(response.Token==undefined){
         this.IsAuthenticatiionFailed = true;
      }
       else{
         this.router.navigate([‘customer’]);
      }
    });
  }
}
```

## 讨论 – 继续

Angular 中的 HTTP 调用返回 *Observables*。

在上述代码中，`this.httpClient.post(……)` 返回 *Observable*。




我猜想，在你的 Web 开发经历中，你一定在 JavaScript 世界进行异步编程时见过回调函数。后来，`Promise` 以更强大的特性登场。（你可以在 ES6 章节中查看这两者的对比。）

Angular 为此使用了 RxJS Observables。

我相信你还记得 RxJS。它是 Angular 框架所依赖的库之一。

不要将 RxJS 与 ReactJS 混淆。ReactJS 是不同的。

其次，RxJS 并不是 Angular 的一部分。它是一个独立的库，也可以用于其他任何基于 JavaScript 的应用程序。

RxJS 是一个庞大的主题。本书无法涵盖全部内容。我强烈建议你将来通过一些在线教程学习 RxJS。这将让你的 Angular 开发体验好得多。了解 RxJS 并非强制要求，但最好还是学习一下。

要获取上述 API 调用的结果，我们需要订阅 observable，这在前面的代码中可以看到。

## 实验 – 续

**步骤 34：检查输出**

用两组值测试应用程序：

1.  尝试一些随机的用户名和密码——你会收到“`Invalid Credentials`”错误。

2.  尝试使用用户名 Admin1 和密码 Admin1，或者用户名 Admin2 和密码 Admin2。这两组都是有效凭据，你会被重定向到 `CustomerComponent`。

但不幸的是，结果并不如预期。无论我们输入什么凭据，始终会收到“`Invalid Credentials`”作为响应。

## 讨论 – 续

要理解上述问题的原因，我们需要调试 Angular 代码。

是时候学习如何调试了。

幸运的是，这里不需要付出太多努力。

Angular CLI 使用的 Webpack 已配置为在编译时导出 source map 文件。

Source map 文件是 JSON 文件，包含将转译后的代码映射回源文件的信息。

**作为开发者，我该怎么做？如何调试？**

你不需要做任何额外的事情。一切都已经配置好了。

要调试，请打开开发者工具。在 Sources 标签页中，你通常能看到 JavaScript 文件的地方，会找到一个以 `webpack` 为树项的树。展开它，然后你会找到一个名为“.”的树项，里面包含你的整个 Angular 应用程序源代码。打开任意 TypeScript 文件，像平常一样设置断点。

![](img/Image50049.jpg)

**图 11.25**

在接下来的步骤中，我们将调试 `LoginComponent` 以找出错误原因。

## 实验 – 续

**步骤 35：故障排查**

在浏览器中打开开发者工具，并在 `LoginComponent` 的 login 方法中设置断点。

接下来，输入正确的凭据，即用户名 Admin1 和密码 Admin1，然后点击 `Login` 按钮，检查断点。

![](img/Image50099.jpg)

**图 11.26**

我想你现在能看到原因了。我们试图从响应对象中读取 `Token` 属性，而实际上它有一个 `token` 属性。（大小写不同。）

**步骤 36：修正 `LoginComponent` 代码**

```
……
// .subscribe((response:{Token:string})=>{
//   if(response.Token==undefined){
       .subscribe((response:{token:string})=>{
         if(response.token==undefined){
         this.IsAuthenticatiionFailed = true;
……
```

**步骤 37：检查输出**

分别用无效和有效的凭据检查应用程序。这次你会得到预期的输出。

## 讨论 – 续

**身份验证完成了吗？**

给自己 5 到 10 分钟，试着找出缺少了什么。（不许作弊。不要读下一行。开始思考。）

**我们真的保护了 Customer Component 免受未授权访问吗？**

虽然我们的 `LoginComponent` 与实时 API 通信，但应用程序实际上并未受到保护。你仍然可以在未登录的情况下访问 `CustomerComponent`。

试试看。运行应用程序。现在，在不完成登录的情况下，尝试访问 `CustomerComponent`。

要使其完全受保护，我们必须将从 API 调用收到的 JWT 令牌持久化到客户端，然后保护 `CustomerComponent` 路由免受未授权访问。

为了持久化 JWT 令牌，我们可以使用客户端的 **local storage**。

为了保护路由，我们将引入一个新的 Angular 概念：**路由守卫**。

我们先完成令牌存储部分。

## 实验 – 续

**步骤 38：存储令牌**

将 `LoginComponent` 中的 login 方法修改为以下代码：

```
……
login() {
     this.httpClient.post("http://localhost:4000/signin",this.loginForm.value)
// .subscribe((response:{Token:string})=>{
//   if(response.Token==undefined){
       .subscribe((response:{token:string})=>{
         if(response.token==undefined){
         this.IsAuthenticatiionFailed = true;
      }
       else{
         localStorage.token=response.token;
         this.router.navigate(['customer']);
      }
    });
  }
}
```

## 讨论 – 续

**什么是路由守卫？**

Angular 的路由守卫是一些接口，它们可以告诉路由器是否允许导航到请求的路由。它们通过检查实现给定守卫接口的类返回的 `true` 或 `false` 值来做出决定。

在我们的应用程序中，我们需要在以下两种情况下保护 `customer` 路由免受直接访问：

1.  当用户未登录时，即令牌不存在。

2.  当用户已登录，但令牌已过期。

我们先从第一点开始。

为此，我们将使用 `CanActivate` 接口。我们通过创建一个实现该接口的类来创建守卫。如果守卫返回 `true`，导航将继续；如果返回 `false`，导航将被取消。让我们看看实际效果。

## 实验 – 续

**步骤 39：创建 `AuthGuard`**

在 app 文件夹中创建一个新文件夹 `Guards`，然后在其内部创建文件 `auth.guard.ts`，内容如下。目前，我们将返回 `true`。稍后我们会添加动态逻辑。

```
import {ActivatedRouteSnapshot, CanActivate, RouterStateSnapshot}
from '@angular/router';
export class AuthGuard implements CanActivate {
   canActivate(route: ActivatedRouteSnapshot, state: RouterStateSnapshot) {
     return true;
  }
}
```

**步骤 40：将守卫附加到路由**

接下来，在 `Route.ts` 文件中将路由守卫附加到 `CustomerComponent`，如下所示：

```
……
import {AuthGuard} from '../Guards/auth.guard';
export const AppRoutes:Routes=[
   {path:'login',component:LoginComponent},
   {path:'customer',component:CustomerComponent,canActivate:[AuthGuard]},
   {path:'',redirectTo:'login',pathMatch:'full'},
……
```

**步骤 41：检查输出**

目前我们还没有编写任何动态逻辑，所以不要期待任何奇迹。

切换回浏览器，在地址栏中输入 `http://localhost:[portnumber]/customer`。

![](img/Image50106.jpg)

**图 11.27**

奇怪的是，你并没有看到 Customer Component，而是得到了一个白屏。

打开开发者工具并检查错误。

## 讨论 – 续

你看到过 `AuthGuard` 对象被显式创建吗？

像 `Services` 一样，`RouteGuards` 是 `可注入的`。Angular 的 DI 系统会在需要时创建并注入实例。

正如我之前所说，“要让 `DI` 生效，我们需要用提供者配置 `Injector`。”

**这次我们如何配置 `injector`？**

如果你还记得，之前我们讨论过四种配置 Injector 的方法。





它们是 `Component`、`NgModule`、`Injectable decorator` 和 `ServiceModule`。

路由守卫实例需要全局可用，并且必须是**单例**。这意味着在整个应用程序中只需创建和维护一个实例。

这可以通过使用 `Injectable` 装饰器或使用 `AppModule` 的 `NgModule` 装饰器来实现。

我们暂时选择 `Injectable` 装饰器。为什么？我们稍后会回答这个问题。

## 实验 – 继续

## 步骤 42：注册路由守卫

如下所示，将 `Injectable` 装饰器附加到 `AuthGuard` 类：

```
.....
import {Injectable} from '@angular/core';
@Injectable({providedIn:'root'})
export class AuthGuard implements CanActivate {
......
```

## 步骤 43：检查输出

你会看到一切恢复正常。另外，通过从 `CanActivate` 方法返回 `false` 来测试应用程序。

## 步骤 44：在 AuthGuard 中添加动态代码

现在是时候阻止用户在没有正确登录的情况下访问 `CustomerComponent` 了。

为此，将 `AuthGuard` 修改为以下内容：

```
import {ActivatedRouteSnapshot, CanActivate, RouterStateSnapshot, Router}
from '@angular/router';
import {Injectable} from '@angular/core';
@Injectable({providedIn:'root'})
export class AuthGuard implements CanActivate {
   constructor(private router:Router){
   }
   canActivate(route: ActivatedRouteSnapshot, state: RouterStateSnapshot) {
     if(!this.isAuthenticated()){
       this.router.navigate(['login']);
       return false;
    }
     return true;
   }
   isAuthenticated(): boolean {
     const token = localStorage.token;
     return token!=null || token!=undefined;
   }
}
```

花点时间尝试分析这段代码。

## 步骤 45：实现注销

在 `CustomerComponent` 中处理注销点击，如下所示：

```
<nav class="navbar navbar-dark bg-dark justify-content-end">
   <span class="navbar-brand mb-0 h1">Welcome Sukesh,</span><a class="navbar-brand mb-0 h1 underline "
     href='/login' (click)="logout()"><u>Logout</u></a>
</nav>
<div class="container-fluid pt-3">
   <div class="card" [hidden]="IsAddNew">
```

然后在 `CustomerComponent` 类中定义 `logout` 方法，如下所示：

```
  logout(){
     localStorage.clear();
  }
```

## 步骤 46：检查输出

![](img/Image50169.jpg)

**图 11.28**

## 讨论 – 继续

尽管应用程序中一切看起来都很准确，但有一个主要问题。

你注意到点击 `logout` 时页面会完全刷新吗？如果你没有注意到，请再试一次。

与 `login button` 不同，`logout link` 没有进行部分页面更新。相反，它刷新了整个页面。

这就是 HTML 中锚标签的行为方式，我相信你知道如何在 Angular 中更改 HTML 元素的默认行为。它将使用指令，而我们有一个完美的指令用于此目的。它就是 `RouterLink` 指令。

## 实验 – 继续

## 步骤 47：更改 LogoutComponent

将 `CustomerComponent` 中的注销链接更改如下：

```
<nav class="navbar navbar-dark bg-dark justify-content-end">
   <span class="navbar-brand mb-0 h1">Welcome Sukesh,</span><a class="navbar-brand mb-0 h1 underline "
     routerLink='/login' (click)="logout()"><u>Logout</u></a>
</nav>
......
```

## 步骤 48：检查输出

现在你将得到输出，其中注销不会刷新整个页面。

## 讨论 – 继续

接下来，让我们关注关于保护路由的第二点——如果令牌过期，我们必须停止导航。

**如何检查 JWT 令牌是否过期？**

我们可以借助一个名为 `@auth0/angular-jwt` 的库来实现。

## 实验 – 继续

## 步骤 49：安装用于检查令牌过期的库

使用 `npm install` 下载 `@auth0/angular-jwt`，如下所示：

```
npm install @auth0/angular-jwt --save
```

## 步骤 50：创建 IsExpired 方法

在 `AuthGuard` 类中创建 `IsTokenExpired` 方法，如下所示：

```
import {JwtHelperService} from "@auth0/angular-jwt";
......
   isTokenExpired():boolean{
     const helper = new JwtHelperService();
     return helper.isTokenExpired(localStorage.token)
   }
```

接下来，更改 `canActivate` 方法，如下所示：

```
......
   canActivate(route: ActivatedRouteSnapshot, state: RouterStateSnapshot) {
     if(!this.isAuthenticated() || this.isTokenExpired()){
       this.router.navigate(['login']);
       return false;
    }
     return true;
   }
......
```

## 步骤 51：检查输出

要测试上述更改，你需要更改服务器代码。

1.  停止服务器。
2.  打开 `server.js` 文件，将 `jwtExpirySeconds` 的值改为一个较小的数字。
3.  启动服务器。
4.  现在检查 Angular 应用程序。完成登录并路由到 `CustomerComponent`，在指定的秒数后刷新页面。由于令牌自动过期，你将被重定向到登录组件。

**注意：** 测试完成后，请务必将过期时间设置为较大的数字（例如 1200）并重新启动服务器。这会让我们的生活更轻松。否则你必须反复登录。

## 步骤 52：动态问候消息

除了问候消息外，我们几乎已经设置好了所有内容。它被硬编码为“`Welcome, Sukesh.`”。让我们使其动态化。

为此，在 `CustomerComponent` 类中创建一个变量 `LoginUserFirstName`，并将其设置为某个虚拟值。

```
......
   @ViewChild('myForm') CustomerForm: NgForm;
   LoginUserFirstName:string="DummyFName";
   constructor() {
```

## 步骤 53：更改模板中的问候消息

接下来，使用插值更改客户模板中的问候消息。

```
.....
<nav class="navbar navbar-dark bg-dark justify-content-end">
   <span class="navbar-brand mb-0 h1">Welcome {{LoginUserFirstName}},</span>
......
```

## 讨论 – 继续

下一个问题是如何获取已登录用户的名字。有多种方法可以实现。

**API 调用**

一种方法是通过执行另一个 API 调用来获取。一旦客户组件初始化，我们将进行一个 API 调用，传递令牌作为输入，API 将在响应中返回“`FirstName`”。

**令牌中的 FirstName**

第二种方法涉及服务器，将 `FirstName` 作为令牌负载的一部分包含在内。令牌将在客户端解码，然后使用。

**IDToken**

这是第三种方法，也是行业中广泛使用的方法之一。

成功验证凭据后，服务器将创建两个令牌——一个是身份验证令牌，用于验证未来的请求。客户端将在每个请求的标头中包含此令牌。第二个是 ID 令牌。ID 令牌将再次是一个 JWT 令牌，它将包含用户的信息，例如 `FirstName`。

对于我们的演示，我们将使用第二种方法。我们的令牌将嵌入 `FirstName`。

下一个问题是如何解码令牌。

为此，我们将使用 `jwt-decode`，这是一个用于解码 JWT 令牌的库。

## 实验 – 继续

## 步骤 54：安装 jwt-decode

使用“`npm install jwt-decode@2.2.0 --save`”命令安装它。

## 步骤 55：解码令牌并检索 FirstName

在 `CustomerComponent` 中导入 `jwt-decode`，然后在构造函数中进行解码，如下所示：

```
.......
import {Customer} from '../Models/customer';
import * as jwt_decode from "jwt-decode";
@Component({
   selector: 'customer',
   templateUrl: './customer.component.html'
})
```





8.  `………`

9.  `   LoginUserFirstName:string=”DummyFName”;`

10.  `   constructor() {`

11.  `     const decodedToken = jwt_decode(localStorage.token);`

12.  `     this.LoginUserFirstName=decodedToken.firstName;`

13.  `     this.IsAddNew = false;`

14.  `………`

**第 56 步：检查输出**

在浏览器中检查输出，欣赏动态问候消息。

#### 总结

我们已经到达第 8 站。在这一旅程中，我们在项目中实现了身份验证。

让我们快速列出本章学到的内容：

*   `*ngIf` 指令
*   `ngIf` 与 hidden 的区别
*   Angular 路由简介
*   Angular 路由守卫
*   Injectable 装饰器
*   依赖注入简介
*   基于令牌的身份验证
*   在 Angular 中使用本地存储
*   Angular 调试
*   REST API 集成与 HTTP 服务
*   讨论了 JWT 令牌
*   响应式表单模块

# 第 4 部分

#### 总结

第 4 部分是我们 Angular 之旅的起点。让我们回顾一下在本部分学到的所有内容。

**第 8 章：Angular 入门**

*   在本章中，我们讨论了创建 Angular 应用程序所需遵循的手动流程。
*   我们看到了 Angular CLI 的实际应用，并学习了如何使用 CLI 轻松创建、执行和构建 Angular 应用程序。
*   我们介绍了 Visual Studio Code，这是一个用于 Angular 编码的代码编辑器。
*   我们了解到，根据 `AppModule` 的 bootstrap 部分所述，`AppComponent` 默认被视为应用程序的根组件。
*   我们还了解到，`AppModule` 默认是应用程序的根模块，因为它是在 `main.ts` 文件中被引导的。
*   我们讨论了 `ng build --prod` 命令，该命令编译应用程序并生成优化后的部署就绪文件。

**第 9 章：Angular 第一个应用**

在进入实验之前，让我们了解这个 Angular 实验教给了我们什么：

*   创建和使用 Angular 组件
*   Angular 插值
*   指令与 `ngFor` 指令简介
*   输入属性与属性绑定简介
*   属性绑定与插值的区别
*   输出属性与事件绑定简介
*   单向绑定
*   双向绑定
*   模板驱动表单简介
*   验证简介
*   模板引用变量
*   `ViewChild` 简介

**第 10 章：使用 Bootstrap CSS 美化 Angular UI**

在第 10 章中，我们学习了如何将第三方 CSS 库引入 Angular 项目。

我们将该库导入到了 `angular.json` 文件中。

**第 11 章：身份验证**

第 11 章将我们带到了第 8 站，内容全部关于 Angular 中的身份验证。我们在这一旅程中讨论了以下主题：

*   `ngIf` 指令
*   `ngIf` 与 hidden 的区别
*   Angular 路由简介
*   Angular 路由守卫
*   Injectable 装饰器
*   依赖注入简介
*   基于令牌的身份验证
*   在 Angular 中使用本地存储
*   Angular 调试
*   REST API 集成与 HTTP 服务
*   讨论了 JWT 令牌
*   响应式表单模块

# 第 5 部分

## 第 12 章

## 身份验证服务

## 引言

在上一章中，我们介绍了一些 Angular 内置服务，如 Router、HTTP 等。

在前往第 9 站的旅程中，我们将探索自定义服务，并回答许多未解之谜。第 9 站的旅程将是所有旅程中最长的，并且跨越多个章节。所以，请保持耐心，继续阅读。

## 什么是依赖？

在整个第 9 站的旅程中，我们将反复遇到“依赖”这个词。

那么，让我们先理解它是什么。

![](img/Image50300.jpg)

**图 12.1**

## 理解紧耦合

理解紧耦合的最佳方式是通过人体。

![](img/Image50338.jpg)

**图 12.2**

你能想象一个人在需要做重活时，把自己的手换成更强壮的手，或者在考试时把自己的大脑换成非凡的大脑吗？

这是不可能的，因为我们的身体与其他身体部位紧密相连，但如果可能的话，那该有多好啊？

同样的原理也适用于编程世界。请看以下代码：

```
1.  class EmailLayer{
2.       sendEmail(){}
3.  }

5.  class LogicLayer{
6.       Save(){
7.           let b:EmailLayer=new EmailLayer();
8.           b.sendEmail();
9.      }
10.  }

12.  //UI Code
13.  let l:LogicLayer=new LogicLayer();
14.  l.Save();
```

在上面的代码中，你可以看到 `LoginLayer` 类直接与 `EmailLayer` 类连接。

现在，尝试回答以下问题：

1.  如果 `EmailLayer` 类出现错误，你还能测试 `LogicLayer` 类的 save 方法吗？
2.  想象另一个 UI，其中相同的 `LogicLayer` 类可以被重用，但希望使用短信通知而不是电子邮件。这可能实现吗？

上述两个问题的答案都是“不能”，因为与人体部位类似，`LoginLayer` 和 `EmailLayer` 是紧耦合的。

## 理解松耦合

想象一辆机动车。

![](img/Image50376.jpg)

**图 12.3**

与人体不同，机动车与其部件的连接更为松散。

轮胎可以更换为其他轮胎，或者根据需求更换发动机。

这是可能的，因为机动车与其部件是松散连接的。

想象一下如果它们是紧密连接的。如果轮胎损坏，我们就必须更换整个机动车。这完全不符合成本效益。

同样的原理也适用于编程世界。

请看以下代码：

```
1.  abstract class NotificationLayer{
2.       abstract Notify():void;
3.  }

5.  class EmailLayer extends NotificationLayer{
6.       Notify() {
7.           //Send email code
8.      }
9.  }

10.  class SMSLayer extends NotificationLayer{
11.       Notify() {
12.           //Send SMS code
13.      }
14.  }

16.  class LogicLayer{
17.       constructor(private notificationLayer:NotificationLayer){
18.      }
19.       Save(){
20.           this.notificationLayer.Notify();
21.      }
22.  }

23.  //UI Code
24.  let l:LogicLayer=new LogicLayer(new EmailLayer());
25.  l.Save();
```

在上面的代码中，`LogicLayer` 与 `NotificationLayer` 是松散连接的。

因此，同一个 `LogicLayer` 既可以与 `EmailLayer` 一起使用，也可以与 `SMSLayer` 一起使用。它将与 `NotificationLayer` 的所有派生类兼容。

## 理解依赖注入

依赖注入（DI）是一种将依赖实例注入系统的模式，由称为 IOC 容器或 DI 框架的外部框架完成。

![](img/Image50453.jpg)

**图 12.4**

如今，大多数现代技术都配备了 DI 框架。我们在第 11 章：身份验证中已经看到了 DI 的演示，其中 `HttpClient` 和 Router 服务的实例由 Angular DI 系统注入到 `LoginComponent` 中，并供我们使用。

DI 使应用程序松散耦合，从而使其可测试且可维护。

在第 9 站的旅程中，你将详细了解 Angular 中的 DI。

## Angular 服务

让我们快速回顾一下上一章中学到的 Angular 服务的定义。




它们是可注入的应用程序逻辑。可以是任何逻辑，Angular 的依赖注入系统负责实例的创建，并在正确的位置为我们注入。

## 实验 4：项目中的 Angular 服务

目前，`LoginComponent` 包含了一些按照最佳实践不应存在的代码。作为最佳实践，组件不应包含任何业务逻辑。应用程序中的所有业务逻辑都应迁移到服务中。让我们也这样做。

**步骤 1：重命名项目**

将 `lab3-ng` 重命名为 `lab4-ng`。

**步骤 2：创建 AuthenticationService**

在 `app` 文件夹中创建一个名为 Services 的新文件夹，然后创建一个新文件 `authentication.service.ts`，内容如下：

```
export class AuthenticationService{
}
```

**步骤 3：将 LoginComponent 连接到 AuthenticationService**

通过在组件类中将 `AuthenticateService` 指定为构造函数参数来获取其引用。

```
……
import {HttpClient} from ‘@angular/common/http’;
import {AuthenticationService} from ‘../Services/authentication.service’;
……
   constructor(private authenticationService:AuthenticationService,
     private router: Router,private httpClient:HttpClient) {
     this.IsAuthenticatiionFailed = false;
  }
   login() {
……
```

**步骤 4：检查输出**

这将导致应用程序崩溃。在开发者工具中检查错误。

![](img/Image50495.jpg)

**图 12.5**

## 讨论

是时候再次回顾上一章的陈述了。

“要使 *DI* 工作，我们必须使用 *provider* 配置 *injector*。”

**注入器**

这是一个理论，所以不必过于纠结。先轻松地过一遍，稍后再复习。

在 Angular 中，*DI 框架*的核心是一个 *注入器*：

*   Angular 注入器负责实例化依赖并将其注入到应用程序的各个部分，例如组件和服务。
*   作为应用程序开发者，我们不会手动创建注入器。我们只使用 provider 对其进行配置。
*   然后注入器使用该 provider 创建服务的实例。
*   Angular 创建两种注入器——**模块注入器**和**元素注入器**。
*   当应用程序启动时，Angular 会创建一个 *模块注入器*，称为 *根注入器*。

    （随着时间的推移，还会创建其他 *子模块注入器*，但暂时不必担心，因为我们还没有看到多个 *Angular 模块* 的实际应用。目前，假设只创建了一个 *模块注入器*，即 *根注入器*。）

*   Angular 还会为每个组件创建一个元素注入器，并维护一个类似于应用程序组件树的树形层次结构。在当前应用程序中，目前我们有一个简单的组件层次结构。我们有一个 `AppComponent`，它有两个子组件——`CustomerComponent` 和 `LoginComponent`。因此，我们将为 `AppComponent` 创建一个元素注入器，它将作为为 `CustomerComponent` 和 `LoginComponent` 创建的元素注入器的父级。
*   当 Angular 应用程序中需要某个依赖时，第一个请求将发送到关联组件的元素注入器。如果无法解析，它将转发到父组件的元素注入器，依此类推，直到依赖被解析。
*   如果即使 `AppComponent` 注入器也无法解析依赖，它将转发到模块注入器。模块注入器也维护一个我们尚未讨论的树。如果模块注入器树也无法解析实例，Angular 将抛出“*no provider…*”错误。

**提供者**

提供者是一个对象，它将 *DI 令牌* 与 *依赖* 关联起来。你将在下一个演示中看到它。

**DI 令牌**

*   令牌用于定位提供者。
*   我们可以创建三种类型的令牌——*类型令牌*、*字符串令牌* 和 *注入令牌*。

    ![](img/Image50540.jpg)

    **图 12.6**

## 实验 – 继续

**步骤 5：为 AuthenticationService 配置注入器**

将 `AuthenticationService` 添加到组件装饰器的 providers 集合中，如下所示：

```
import {AuthenticationService} from ‘../Services/authentication.service’;
@Component({
   selector: ‘login’,
   templateUrl: ‘./login.component.html’,
   providers:[{provide: AuthenticationService, useClass: AuthenticationService}]
})
export class LoginComponent {
```

## 讨论 – 继续

让我们理解一下我们做了什么。

![](img/Image50586.jpg)

**图 12.7**

通过编写上述代码，我们向 `CustomerComponent` 的 *providers* 集合中添加了一个新的提供者对象，该对象将由 *CustomerComponent* 的元素注入器使用。

在代码中，使用的 *DI 令牌* 是 *类型令牌* 类型。

在上面的示例中，`provide` 和 `useClass` 持有相同的值，但如果有需要，两者可以不同。

基于当前配置，当我们期望 `CustomerService`（因为这是 *provide* 中提到的）时，注入器将注入 `CustomerService` 的实例（因为这是 `useClass` 中提到的）。当 `CustomerComponent` 实例被销毁时，创建的实例也将被销毁。

**简写语法**

当两个属性（`provide` 和 `useClass`）共享相同的值时，我们可以使用更简单的语法。

```
……
import {AuthenticationService} from ‘../Services/authentication.service’;
@Component({
   selector: ‘login’,
   templateUrl: ‘./login.component.html’,
   providers[AuthenticationService]
})
export class LoginComponent {
```

我们将在本书后面探讨其他类型的 *DI 令牌*。

## 实验 – 继续

**步骤 6：检查输出**

执行应用程序。这次你会发现一切恢复正常。

**步骤 7：创建用户模型**

在 `Models` 文件夹中创建一个新的 `user.ts` 文件，内容如下：

```
export class User{
   UserName: string;
   Password: string;
}
```

**步骤 8：创建响应模型**

在 `Models` 文件夹中创建一个名为 `HttpResponses` 的新文件夹，然后在该文件夹中创建一个新文件 `authentication.response.ts`，内容如下：

```
export class AuthenticationResponse{
   token: string;
}
```

**步骤 9：定义 Authenticate 方法**

在 `AuthenticationService` 中定义一个用于身份验证的方法，如下所示：

```
import {Observable} from ‘RxJS’;
import {AuthenticationResponse} from ‘../Models/HttpResponses/authentication.response’;
import {User} from ‘../Models/user’;
import {HttpClient} from ‘@angular/common/http’;

export class AuthenticationService{
   constructor(private httpClient:HttpClient) {
  }
   authenticate(user:User):Observable<AuthenticationResponse>{
     return this.httpClient.post<AuthenticationResponse>(“http://localhost:4000/signin”,user);
  }
}
```

这次我们使用了 post 方法的泛型版本，而不是非泛型版本。

非泛型版本返回 `Observable<object>`，而泛型版本返回 `Observable<T>`。使用泛型版本是最佳实践。

## 讨论 – 继续

现在，有些有趣的事情。

*我们也必须为 AuthenticationService 添加 Injectable 装饰器。*

否则，我们会得到如下错误：

![](img/Image50597.jpg)

**图 12.8**

在上一章中，我们提到了配置注入器的三种方式——使用 *Component 装饰器*、*ngModule 装饰器* 和 *Injectable 装饰器*。

在创建 `AuthGuard` 时，我们遵循了 `Injectable` 装饰器的方法。





这次，对于 `AuthenticationService`，我们遵循了 `Component` 装饰器的方法，但它也要求我们添加 `Injectable` 装饰器。

为什么？

因为在 Angular 中，*“每个服务的订阅者都必须用 `Injectable` 装饰器进行装饰。”*

这意味着每个想要使用该服务的人都必须用 `Injectable` 装饰器进行装饰。

可注入装饰器会生成关于构造函数参数的必要元数据，这些元数据 Angular 会用到。因此，对于每个依赖于其他服务的 Angular 服务，都必须添加 `Injectable` 装饰器。

**如果是这样，那为什么 `LoginComponent` 没有用 `Injectable` 装饰器装饰呢？**

这是因为上述规则仅适用于那些本身没有用其他装饰器装饰的订阅者。

**这是否意味着应用程序中的每个自定义服务都要用 `Injectable` 装饰器装饰？**

从技术上讲，*不是*。我们只需要在自定义服务依赖于其他服务时才为其附加 `Injectable` 装饰器。事实上，大多数自定义服务都依赖于其他服务。因此，在实际项目中，你会发现大多数服务都使用了 `Injectable` 装饰器。

**附加了 `Injectable` 装饰器后，我们还需要在 `Component` 装饰器中提供 providers 吗？**

使用 `Component` 装饰器配置 *注入器* 是否让你觉得毫无意义，因为它仍然要求我们为 *服务* 添加 `Injectable` 装饰器？

如果是这样，那么你的理解中有一点混淆。

在为 `AuthGuard` 服务配置注入器时，我们向装饰器传递了一个参数。

1.  `  @Injectable({providedIn:'root'})`

通过这样做，我们配置了**根注入器**。

这次，我们只附加装饰器，但不传递任何参数。

![](img/Image50687.jpg)

**图 12.9**

因此，它不会配置任何注入器。通过在组件级别指定 provider，我们配置了该组件的**元素注入器**。

**这两种配置方法有什么区别？**

当根注入器被配置为提供服务的实例时：

1.  整个应用程序只会创建该服务的一个实例。
2.  无论在哪里需要，都会注入同一个实例。
3.  该实例的生命周期与应用程序相同。只有当应用程序终止时，它才会被销毁。
4.  建议在根注入器级别配置诸如 `Logger`、`Authentication`、`RouteGuards` 等服务。这些服务会在系统中反复使用。因此，最好将其维护为单例（只有一个实例）。

![](img/Image50694.jpg)

**图 12.10**

当元素注入器被配置为提供服务的实例时：

1.  每个组件实例会创建该服务的一个实例，并在所有子组件之间共享。
2.  服务的生命周期取决于组件实例的生命周期。当该组件被销毁时，服务实例也会被终止。
3.  建议以这种方式配置功能级别的服务，例如 `CustomerService`、`ProductServices`，因为它们在特定组件被销毁后就不再需要了。

![](img/Image50732.jpg)

**图 12.11**

**为 `AuthenticationService` 配置根注入器而不是元素注入器不是更合适吗？**

是的，确实如此。`AuthenticationService` 是整个应用程序都需要使用的服务，因此建议在整个应用程序中保持单例实例。通过在组件级别配置注入器，我们犯了一个错误，我们很快就会纠正。

**使用 `NgModule` 装饰器配置注入器有什么独特之处？**

`Injectable` 装饰器和 `NgModule` 装饰器都允许我们配置**模块注入器**。

我们稍后会回答这个问题。现在，继续实验。到目前为止，我们只学习了使用 `Component` 装饰器和 `Injectable` 装饰器配置注入器。

## 实验 – 继续

### 步骤 10：为 `AuthenticationService` 附加 `Injectable` 装饰器

```
……
import {HttpClient} from '@angular/common/http';
import {Injectable} from '@angular/core';
@Injectable()
export class AuthenticationService{
……
}
```

### 步骤 11：修改 `LoginComponent`

按如下方式更改 `LoginComponent` 中的 login 方法：

```
…..
   login() {
     this.authenticationService.authenticate(this.loginForm.value)
       .subscribe((response:{token:string})=>{
         if(response.token==undefined){
         this.IsAuthenticatiionFailed = true;
      }
       else{
         localStorage.token=response.token;
         this.router.navigate(['customer']);
      }
    });
  }
}
```

## 讨论 – 继续

工作的一部分已经完成。接下来，我们需要在凭据无效时通知 `LoginComponent`。

为此，我们将使用 *RxJS* 中的 `Subject` 类。我们将在演示之后更详细地讨论 `Subject`。

我们先做一个演示，然后再进一步讨论。

## 实验 – 继续

### 步骤 12：处理身份验证成功

让我们在服务端处理成功的身份验证。按如下方式更改 `AuthenticateService` 中的 authenticate 方法：

```
@Injectable()
export class AuthenticationService {
// 更改 1 - 注入 Router 服务
   constructor(private router: Router, private httpClient: HttpClient) {}
// 更改 2 - 返回类型为 void
   authenticate(user: User): void {
// 更改 3 - 订阅 Observable
     this.httpClient
       .post<AuthenticationResponse>('http://localhost:4000/signin', user)
       .subscribe((response: {token: string}) => {
         if (response.token !== undefined) {
           localStorage.token = response.token;
           this.router.navigate(['customer']);
        }
      });
  }
}
```

你会注意到以下三个更改：

1.  我们不再返回 observable。
2.  我们在服务本身中订阅 observable。
3.  我们在服务本身中路由到 `CustomerComponent`。

## 讨论 – 继续

工作的一部分已经完成。接下来，我们需要在凭据无效时通知 `LoginComponent`。

为此，我们将使用 *RxJS* 中的 `Subject` 类。我们将在演示之后更详细地讨论 `Subject`。

我们先做一个演示，然后再进一步讨论。

## 实验 – 继续

### 步骤 13：处理无效凭据

按如下方式处理 authenticate 方法中的 else 部分：

```
……
import {Subject} from 'RxJS';
……
export class AuthenticationService {
// 更改 4 - 用于处理无效凭据的 Subject
   isAuthenticationFailedSubject: Subject<boolean>;
// 更改 1 - 注入 Router 服务
   constructor(private router: Router, private httpClient: HttpClient) {
     this.isAuthenticationFailedSubject = new Subject<boolean>();
  }
}
```





12.  *`// Change no 2 - Return type is void`*
13.  `   authenticate(user: User): void {`
14.  *`// Change no 3 - Observable is subscribed`*
15.  `     this.httpClient`
16.  `       .post<AuthenticationResponse>(‘http://localhost:4000/signin’, user)`
17.  `       .subscribe((response: {token: string}) => {`
18.  `         if (response.token !== undefined) {`
19.  `           localStorage.token = response.token;`
20.  `           this.router.navigate([‘customer’]);`
21.  `        }else{`
22.  *`// Change 5 - Notify subscriber that credentials are invalid`*
23.  `           this.isAuthenticationFailedSubject.next(false);`
24.  `        }`
25.  `      });`
26.  `  }`
27.  `}`

在上述代码中，你可以注意到以下三个新变化：

1.  在顶部，我们声明了一个 `Subject` 实例，并传入 `Boolean` 作为参数。
2.  在构造函数中，它已被初始化。
3.  在 else 部分，通过调用 `Subject` 的 `next` 方法通知订阅者。

## 讨论 – 续

为什么 `Subject` 使用 `Boolean`？

嗯，在我们的用例中，`Boolean` 是合理的。它可以是任何数据类型，包括用户自定义对象。

## 实验 – 续

**步骤 14：修改 LoginComponent**

`login` 方法中不再需要逻辑。只需按如下方式调用 `authenticate` 函数：

```
1.  login() {
2.       this.authenticationService.authenticate(this.loginForm.value);
3.    }
```

**步骤 15：处理无效凭据**

在构造函数中订阅 `isAuthenticationFailedSubject`，如下所示：

```
1.  constructor(private authenticationService: AuthenticationService) {
2.       this.IsAuthenticatiionFailed = false;
3.       this.authenticationService.isAuthenticationFailedSubject.subscribe((x) => {
4.         this.IsAuthenticatiionFailed = x;
5.      });
6.    }
```

**步骤 16：检查输出**

执行应用程序并检查更新后的输出。使用无效凭据进行测试。

遗憾的是，你不会得到预期的输出。我不希望你查看下一步。相反，尝试调试 TypeScript 文件，并自己找出问题所在。

**步骤 17：解决错误**

问题在于，在 `AuhenticationService` 中，当凭据无效时，我们向 `next` 方法传递了 false。在我们的情况下，它应该是 true。

```
1.  ……
2.      else{
3.  *`// Change 5 - Notify subscriber that credentials are invalid`*
4.             this.isAuthenticationFailedSubject.next(true);
5.          }
6.  ……
```

**步骤 18：检查输出**

现在你将得到预期的输出。

## 讨论 – 续

让我们理解 `Observable` 和 `Subject` 之间的区别。但首先，让我们探索 *响应式编程* 中 `Observable` 和 `Observer` 的概念。

**Observable 和 Observer**

在 *响应式编程* 世界中，我们有 `Observable` 和 `Observer` 的概念。

想想 Twitter。假设你访问我的 Twitter 账户（`@sukeshmarla`），并点击关注按钮。那么究竟会发生什么？Twitter 将你添加到我的关注者列表。每当我发推文时，所有关注者都会收到通知。在这种情况下，我（你关注的人）是 `Observable`，Twitter 是 `Observer`，而关注者是 *消费者* 或 *订阅者*。

你观察的对象称为 `Observable`。*订阅者* 订阅其变化。

向 observable 提供新数据的对象称为 `Observer`。*订阅者* 获得订阅是因为 *观察者* 向 `Observable` 提供了某些内容。

![](img/Image50855.jpg)

**图 12.12**

*这种编程方法称为响应式编程——需求方不会持续请求数据。他会订阅变化。负责数据的程序会在数据可用时做出反应并发布数据。*

**Rxjs 中的 Subject**

我们在之前的某个实验中介绍了 *Rxjs*。它是一个用于 *响应式编程* 的 *JavaScript 库*。

在 *RxJSJS* 中，有一个名为 `Subject` 的类，它同时代表了响应式编程中的 `Observable` 和 `Observer`。

让我们回顾一下之前的实验：

1.  我们创建了 `Subject`。
2.  我们在 `LoginComponent` 中订阅了它。因此，它是一个 `Observable`。
3.  我们使用 `next` 方法向它提供数据。因此，它是一个 `Observer`。

**Rxjs Subject 与 Rxjs Observable**

在 Rxjs 中，还有一个名为 `Observable` 的类，它代表了响应式编程中的 `Observable`。

RxJS `Observable` 只能被订阅，而 RxJS *Subjects* 既可以订阅，也可以发出新值。

RxJS *Observables* 不会暴露任何向它提供新数据的方法。简单来说，我们有 `Subject.next` 方法，但没有 `Observable.next`。

**从 Subject 中提取 Observable**

在实际项目中，作为最佳实践，我们从不直接将 subjects 暴露给订阅者。

想象一下，多个订阅者订阅了一个 subject，其中一个订阅者调用了 `next` 方法。你能想象会发生什么吗？其他每个订阅者都会收到通知。

因此，建议将 `Subject` 声明为私有，并将其底层的 `Observable` 暴露给 *订阅者* 进行订阅。`Subject` 类有一个 `asObservable()` 方法，可以让我们从中提取底层的 `Observable`。

让我们看看解决方案。

## 实验 – 续

**步骤 19：将 Subject 转换为 Observable**

打开 `AuthenticationService`，将 Subject 标记为私有，并改为暴露 Observable。

```
1.  *`// Change 4 - Subject for dealing with invalid credentials`*
2.     private isAuthenticationFailedSubject: Subject<boolean>;
3.  *`// Change 6 - Declare Observable`*
4.     invalidCredentialsObservable$: Observable<boolean>;
6.  *`// Change no 1 - Router Service injected`*
7.     constructor(private router: Router, private httpClient: HttpClient) {
8.       this.isAuthenticationFailedSubject = new Subject<boolean>();
9.  *`// Change 7 - Get Observable from Subject`*
10.      this.invalidCredentialsObservable$ = this.isAuthenticationFailedSubject.asObservable();
11.    }
```

***注意：** 在 observable 变量后添加“$”是业界遵循的命名约定。*

**步骤 20：订阅 Observable**

现在，在 Login Component 中，不再订阅 Subject，而是订阅 Observable。

```
1.  ……
2.     constructor(private authenticationService: AuthenticationService) {
3.       this.IsAuthenticatiionFailed = false;
4.       this.authenticationService.invalidCredentialsObservable$.subscribe((x) =>
5.       {
6.         this.IsAuthenticatiionFailed = x;
7.      });
8.    }
9.  ……
```

**步骤 21：检查输出**

再次得到令人满意的输出。

以下是应用程序的示意图流程：

![](img/Image51013.jpg)

**图 12.13**

## 讨论 – 续

上述通信方法被称为**观察者模式**，其中许多**订阅者**订阅 `Observable` 的变化。

#### 总结

步骤 21 并不是本实验的最后一步。实验将在下一章继续。我们刚刚完成了一个长实验的一部分。

让我们回顾一下本实验中学到的所有内容：

*   我们再次复习了 DI 概念，并了解到它使代码松散耦合，从而更易于维护和测试。
*   我们讨论了 Angular 的 `Injector`，它负责将服务实例注入到 Angular 应用程序中。
*   我们讨论了两种注入器——**模块注入器**和**元素注入器**。
*   我们了解到这两种注入器都维护着一个层次结构。
*   我们学习了如何使用 `Injectable` 装饰器和 `Component` 装饰器配置服务。
*   我们了解到 `NgModule` 和 `Injectable` 装饰器都可以配置模块注入器，而 `Component` 装饰器则配置元素注入器。





*   我们了解到，无论配置了哪个注入器，每个依赖于其他服务的 Angular 服务都必须添加 `Injectable` 装饰器。
*   我们了解到，根 `Injector` 会创建一个全局单例实例，而元素注入器则会创建特定于组件实例（及其子组件）的实例。
*   我们讨论了当 `provide` 和 `useClass` 值相同时，配置注入器的简短语法。
*   我们学习了响应式编程，以及如何在 Angular 中借助 RxJS 实现它。
*   我们了解到，在响应式编程中，`Observable` 由 `Subscriber` 订阅，而 `Observer` 将数据馈送到 `Observable` 中。
*   我们演示了 RxJS 的 `Subject`，它在响应式编程中同时代表 `Observable` 和 `Observer`。
*   我们了解到，在实际项目中，RxJS 的 `Subject` 会被标记为私有，而底层的 `Observable` 会作为公共成员暴露出来。

## 第 13 章

## 取消订阅

## 引言

在本章中，我们将学习取消订阅 Observable 的重要性和步骤。

## 为什么要取消订阅？

重要的一点是，无论你使用什么技术栈，当涉及观察者模式时，取消订阅与订阅同样至关重要。想象一下，有几个订阅者订阅了我们的 Observable，而其中一些订阅者不再对接收通知感兴趣。

或者更确切地说，假设某些订阅者甚至已经不存在了。在这种情况下，保持活跃的订阅还有意义吗？当然没有。保留所有不必要的订阅可能会导致内存泄漏。

*最佳实践是，一旦不再需要订阅，就应该取消订阅。否则，会导致内存泄漏。*

## 在 Angular 中何时以及如何取消订阅？

**如何取消订阅 RxJS Observable 订阅？**

幸运的是，RxJS 的 `Subscription` 提供了一种取消订阅的方法。我们很快就会看到演示。

**我们应该何时取消订阅？**

下一个问题是，在我们的应用程序中，我们应该何时取消订阅。

在我们的案例中，一旦成功登录，我们会重定向到 `CustomerComponent`，这将销毁 `LoginComponent`。一旦 `LoginComponent` 被销毁，之后就没有必要再保留对 `invalidCredentialsObservable$` 的订阅了。

Angular 提供了各种生命周期事件，其中之一是 `ngOnDestroy`，它会在组件被销毁时执行。这是执行取消订阅的完美位置。

随着我们的深入，我们将探索其他生命周期事件。

## 实验 – 续 – 取消订阅

**第 22 步：实现 ngOnDestroy 方法**

这是一个两步过程。首先，让 `LoginComponent` 类实现 `OnDestroy` 接口，这将强制你定义 `ngOnDestroy` 方法。

```
import {Component, OnDestroy} from '@angular/core';
……
export class LoginComponent implements OnDestroy {
……
ngOnDestroy(): void {
}
……
```

**第 23 步：取消订阅**

同样是一个两步过程。首先，将订阅保存在一个全局变量中，然后在 `ngOnDestroy` 方法中取消订阅。

```
……
import {FormControl, FormGroup, Validators} from '@angular/forms';
import {Subscription} from 'rxjs';
……
export class LoginComponent implements OnDestroy {
invalidCredentialsSubscription: Subscription;
……
constructor(private authenticationService: AuthenticationService) {
this.invalidCredentialsSubscription = this.authenticationService.invalidCredentialsObservable$.subscribe(
(x) => {
this.IsAuthenticatiionFailed = x;
}
);
}
ngOnDestroy(): void {
this.invalidCredentialsSubscription.unsubscribe();
}
……
```

## 讨论 – 续

现在你已经理解了取消订阅的重要性，是时候研究一种更好的方法来实现同样的目的了。这可以通过使用 **async 管道** 来完成。

**什么是 Angular 管道？**

*管道* 是 Angular 的一个概念，用于在组件模板中转换数据。

**什么是 async 管道？**

Async 管道是一个 Angular 管道，它在内部订阅 *observable* 并返回该 **observable** 发出的最新值。当组件被销毁时，最棒的是 async 管道会自动取消订阅，以避免潜在的内存泄漏。

例如，假设我们有一个 observable `ABCD`，它会返回一些值，并且这些值需要在 UI 中显示。已知的方法如下：

```
//在组件类中
this.somesubsctiption = ABCD.subscribe(
(x) => {
this.myValue = x;
}
);
……
ngOnDestroy(): void {
this.invalidCredentialsSubscription.unsubscribe();
}
<!-- 在模板中 -->
<span>{{myValue}}</span>
```

使用 async 管道，则如下所示：

```
<span>{{ABCD | async}}</span>
```

以上两种方法中，你觉得哪一种更简单？

让我们在我们的应用程序中实现更好的那一种。

## 实验 – 续

**第 24 步：实现 Async 管道**

这将是一个三步过程：

*   在第 1 步中，我们将从 `LoginComponent` 中移除不必要的代码。
*   在第 2 步中，我们将在 `LoginComponent` 中创建一个新的全局变量来保存表示无效凭据的 observable。
*   最后，在第 3 步中，我们将在模板中使用 async 管道。

让我们来实现它。

```
export class LoginComponent // implements OnDestroy
/* 阅读：不需要实现 OnDestroy，
因为取消订阅将由 async 管道处理 */
{
/* 阅读：不需要保存订阅，因为 observable
会在组件销毁时自动取消订阅 */

// invalidCredentialsSubscription: Subscription;

loginForm = new FormGroup({
UserName: new FormControl('', [
Validators.required,
Validators.minLength(6),
]),
Password: new FormControl('', [
Validators.required,
Validators.minLength(6),
]),
});

/* 阅读：不需要布尔变量，
而是需要 Observable 布尔值 */
IsAuthenticatiionFailed$: Observable<boolean>;
// IsAuthenticatiionFailed: boolean;

constructor(private authenticationService: AuthenticationService) {

// this.IsAuthenticatiionFailed = false;
this.IsAuthenticatiionFailed$ = this.authenticationService.invalidCredentialsObservable$;

/* 阅读：不需要手动订阅，
async 管道会处理订阅 */

// this.invalidCredentialsSubscription = this.authenticationService.invalidCredentialsObservable$.subscribe(
// (x) => {
// this.IsAuthenticatiionFailed = x;
// }
// );
}
// ngOnDestroy(): void {
// this.invalidCredentialsSubscription.unsubscribe();
// }
login() {
this.authenticationService.authenticate(this.loginForm.value);
}
}
```

最后，让我们在模板中使用 async 管道。

```
<div class="alert alert-danger"
*ngIf="IsAuthenticatiionFailed$|async" >
无效的用户名或密码
</div>
```

**第 25 步：检查输出**

你将得到类似的输出。只是代码变得更加简洁。

#### 总结

这是一个非常简单的章节，讨论了取消订阅。在本章中，我们涵盖了 Angular 中的以下主题：

*   我们了解到取消订阅非常重要，否则会导致内存泄漏。





*   我们学习了如何取消订阅 RxJS 订阅。
*   我们了解了 Angular 组件的 `ngOnDestroy` 生命周期事件。
*   我们简要讨论了 Angular 管道。它用于封装 Angular 中的转换逻辑（有专门的一章介绍）。
*   最后，我们讨论了 async 管道。

## 第 14 章

## 登出与路由守卫清理

## 引言

在本章中，我们将对之前的实验进行一些清理——遵循最佳实践、消除冗余等。

## 实验 – 续 – 登出与路由守卫

**第 26 步：重构登出**

在上一步中，我们重构了身份验证逻辑。接下来，让我们重构登出代码。

在 `AuthenticationService` 中创建一个新的 `logout` 方法，如下所示：

```
……
@Injectable()
export class AuthenticationService {
……
   logout(){
     localStorage.clear();
}
……
```

**第 27 步：修改 CustomerComponent**

接下来，将 `AuthenticationService` 注入到 `CustomerComponent` 中，然后修改 `CustomerComponent` 中的登出方法，如下所示：

```
……
export class CustomerComponent {
……
   constructor(private authenticationService: AuthenticationService) {
     const decodedToken = jwt_decode(localStorage.token);
……
  }
……
   logout() {
    this.authenticationService.logout();
  }
……
```

**第 28 步：检查输出**

运行应用程序。尝试使用正确的凭据登录，但奇怪的是，应用程序不会重定向到 `CustomerComponent`。

打开开发者工具。你会看到“No provider for AuthenticationService”错误。

## 讨论 – 续

目前，我们为 `LoginComponent` 配置了 `AuthenticationService` 的元素注入器。

因此，`LoginComponent` 可以访问 `AuthenticationService`，但这并不会让 `CustomerComponent` 也能访问 `AuthenticationService`。

**如何实现这一点？**

只有在现有应用程序中执行以下操作之一才能实现：

1.  为 `CustomerComponent` 的元素注入器配置 `AuthenticationService` 提供者。
2.  不为 `LoginComponent` 配置元素注入器，而是为 `AppComponent` 配置元素注入器。
3.  使用 `NgModule` 装饰器为根注入器配置 `AuthenticationService` 提供者。
4.  使用带有 `{providedIn: ‘root’}` 参数的 `Injectable` 装饰器为根注入器配置 `AuthenticationService` 提供者。

**方式 1**

如果采用第一种方法，最终会创建两个 `AuthenticationService` 实例——一个用于 `LoginComponent`，一个用于 `CustomerComponent`。

`AuthenticationService` 是一种在应用程序中会反复需要的服务。因此，建议保持一个应用程序范围的实例，而不是多个。因此，不推荐这种方法。

**方式 2、3、4**

假设我们采用前面提到的其他任何一种方式。那么，`LoginComponent` 中就不需要提供者了。这三种方法都会产生一个 `AuthenticationService` 的单例实例，该实例将可供整个应用程序使用。

**方式 2 – 为什么是单例？**

正如我之前所说，从技术上讲，元素注入器使服务实例可用于特定组件及其所有子组件。当组件实例被销毁时，该服务实例也会被销毁。有趣的是，`AppComponent` 是我们的根组件，因此它永远不会被销毁。所以，最终在根组件上注册的服务在逻辑上成为了全局单例实例。

但是，使用元素注入器来实现单例实例并不是行业中的常见做法（尽管你可以这样做）。因此，我们必须选择方式 3 或方式 4。

**方式 3 与方式 4 的比较**

这两种方式都能达到目的。它们会配置根注入器，从而维护单个服务。

最大的问题是，在方式 3 和方式 4 之间应该选择哪一个。

`providedIn: 'root'` 是在 Angular 6 中引入的，并且是推荐的做法。在此之前，配置根注入器的唯一可用选项是使用 `NgModule` 装饰器。

**为什么推荐使用 Injectable 装饰器？**

当使用 `Injectable` 来配置注入器时，如果该服务在应用程序中从未被使用，它就不会被包含在最终构建中。这个概念称为 Tree Shaking。

我们很快就会讨论使用 `NgModule` 配置注入器的重要性。

## 实验 – 续

**第 29 步：从 LoginComponent 中移除提供者**

首先，打开 `LoginComponent` 类并移除 providers。

**第 30 步：注册根注入器**

使用 `Injectable` 装饰器注册根注入器，如下所示：

```
……
@Injectable({providedIn: ‘root’})
export class AuthenticationService {
……
```

**第 31 步：检查输出**

运行应用程序，确认登录和登出都能正常工作。

**第 32 步：重构守卫**

既然我们正在重构所有内容，那么也来重构我们的守卫。

将 `isAuthenticated` 和 `isTokenExpired` 方法从 `AuthGuard` 类移动到 `AuthenticationService` 类。

```
import {JwtHelperService} from “@auth0/angular-jwt”;
@Injectable({providedIn: ‘root’})
export class AuthenticationService {
……
   isAuthenticated(): boolean {
     const token = localStorage.token;
     return token!=null || token!=undefined;
  }
   isTokenExpired(): boolean{
     const helper = new JwtHelperService();
     return helper.isTokenExpired(localStorage.token)
  }
   logout(){
     localStorage.clear();
  }
}
```

之后，使用 `AuthenticationService` 重构 `AuthGuard`，如下所示：

```
@Injectable({providedIn: ‘root’})
export class AuthGuard implements CanActivate {
   constructor(
     private router: Router,
     private authenticationService: AuthenticationService
  ) {}
   canActivate(route: ActivatedRouteSnapshot, state: RouterStateSnapshot) {
     if (!this.authenticationService.isAuthenticated() ||
       this.authenticationService.isTokenExpired()
    ) {
       this.router.navigate([‘login’]);
       return false;
    }
     return true;
  }
}
```

**第 33 步：检查输出**

测试更改总是好的。尝试在没有正确登录的情况下直接导航到 `CustomerComponent`。如果你被重定向到 LoginComponent，那么一切正确。

**第 34 步：自动聚焦**

你是否厌倦了每次页面刷新时都需要手动将光标放入 `UserName` 文本框？

这可以纯粹使用 HTML 解决，不需要 Angular 的功能。

只需将 autofocus 属性附加到任何输入控件上，当页面加载时，焦点就会自动设置到该控件上。

```
  <label for=”UserName”>User Name: </label>
         <input class=”form-control” autofocus
         [ngClass]=”{‘is-valid’:loginForm.
……
```

**第 35 步：检查输出**

现在，每次刷新页面时，焦点都会自动设置在 `UserName` 文本框上。

**第 36 步：按回车提交**

目前应用程序中另一个烦人的地方是 `Login` 点击。每次提交时我们都必须手动点击。最终用户通常更喜欢按回车键。同样，这可以纯粹用 HTML 实现。

这将是一个两步过程：





首先，将登录按钮从标准按钮转换为提交按钮。

```
<input type=”submit” class=”btn btn-success” value=”Login”
       (click)=”login()”  [disabled]=”loginForm.invalid” >
```

接下来，不要使用`div`作为所有表单控件的容器，而是使用`form`标签。

```
    ……
     <h5 class=”card-header”>Login</h5>
     <!-- <div class=”card-body” [formGroup]=”loginForm”> -->
       <form  class=”card-body” [formGroup]=”loginForm”>
       <div class=”form-group”>
         <div class=”alert alert-danger” *ngIf=”IsAuthenticatiionFailed$|async” >
    ……
```

### 第 37 步：检查输出

刷新登录页面。输入一些凭据，然后按键盘上的*Enter*键。如果你正确遵循了每一步，现在应该能看到预期的输出。

（目前不要尝试在`CustomerComponent`中实现相同的解决方案。它不会起作用。我们稍后会做。）

#### 总结

本章主要关于如何让代码变得更好。我们还涉及了一些令人兴奋的内容。让我们再次回顾一下：

*   我们了解了通过将现有代码移到服务中，在服务中编写逻辑的重要性。

*   我们在本章中再次复习了元素注入器和模块注入器。由于元素注入器无法满足我们的需求，我们切换到了模块注入器。

*   我们了解到`AppComponent`的元素注入器会间接创建一个全局单例实例，因为它作为根组件永远不会被销毁。其次，作为根组件，它创建的服务实例对所有子组件都是可访问的。

*   我们了解到，在配置根注入器时，`Injectable`装饰器比`NgModule`装饰器更受青睐，因为`Injectable`装饰器支持摇树优化。摇树优化是 Angular 构建过程中的一个步骤，确保所有未使用的服务从最终打包文件中移除。

*   我们了解到，我们可以通过使用 HTML 的`autofocus`属性、`form`标签和`submit`按钮来利用 Angular 中的 HTML 能力。

## 第 15 章

### 客户服务

#### 简介

在本章中，通过创建`CustomerService`，我们将把项目提升到一个新的水平。

#### 实验 – 续 – CustomerService

##### 第 38 步：使用 CustomerService 清理 CustomerComponent

在`Services`文件夹中创建一个新文件`customer.service.ts`，内容如下：

```
import {Injectable} from ‘@angular/core’;
import {Observable, of} from ‘RxJS’;
import {Customer} from ‘../Models/customer’;
@Injectable()
export class CustomerService {
   private Customers: Array<Customer>;

   IsAddNew$: Observable<boolean>;
   Customers$: Observable<Array<Customer>>;
   constructor() {
     this.IsAddNew$ = of(false);

     this.Customers = new Array<Customer>();
     this.Customers.push(new Customer(‘Sukesh’, ‘Marla’));
     this.Customers.push(new Customer(‘Just’, ‘Compile’));
     this.Customers.push(new Customer(‘Ram’, ‘Lakhan’));

     this.Customers$ = of(this.Customers);
  }
   setAddNew(){
     this.IsAddNew$ = of(true);
  }
   setList(){
     this.IsAddNew$ = of(false);
  }
   Save(customer: Customer) {
     this.Customers.push(customer);
     this.Customers$ = of(this.Customers);
     this.IsAddNew$ = of(false);
  }
}
```

## 讨论 – 续

你可能期望有一些 API 调用。请耐心等待。

我们很快就会用动态 API 调用替换掉虚拟逻辑。

我们已经看到了使用`HttpClient`服务的示例，并了解到它返回可观察对象。订阅者订阅该可观察对象以获取响应。我们设计了带有虚拟逻辑的`CustomerService`，以便以后创建真实逻辑时可以轻松适应。现在不用担心这个。我们稍后会讨论。

#### 代码解释

*   `of`是一个`RxJS`方法，它从值创建一个可观察对象。

*   我们将`IsAddNew`和`Customers`封装在可观察对象中，这些可观察对象将由`CustomerComponent`订阅。

你会发现`CustomerComponent`中几乎所有的逻辑现在都成为了`CustomerService`的一部分。

## 实验 – 续

#### 第 39 步：为 CustomerService 配置注入器

我相信你一定已经想到了最佳方法。

我们不需要`CustomerService`作为全局单例实例可用。因此，最好的方法是为`CustomerService`配置`CustomerComponent`的元素注入器。

```
……
import {CustomerService} from ‘../Services/customer.service’;
@Component({
   selector: ‘customer’,
   templateUrl: ‘./customer.component.html’,
   providers:[CustomerService]
})
export class CustomerComponent {
……
```

#### 第 40 步：在 CustomerComponent 中注入 CustomerService

将`CustomerService`注入到`CustomerComponent`的构造函数中，如下所示：

```
……
export class CustomerComponent {
   Customers: Array<Customer>;
   IsAddNew: boolean;
   FirstName: string;
   LastName: string;
   @ViewChild(‘myForm’) CustomerForm: NgForm;
   LoginUserFirstName: string = ‘DummyFName’;
   constructor(private customerService: CustomerService,
     private authenticationService: AuthenticationService) {
……
```

#### 第 41 步：声明可观察对象

在`CustomerComponent`类中创建两个全局变量，并将它们指向`CustomerService`中相应的可观察对象。

```
export class CustomerComponent {
   IsAddNew$: Observable<boolean>;
   Customers$: Observable<Array<Customer>>;
   FirstName: string;
   LastName: string;
   @ViewChild(‘myForm’) CustomerForm: NgForm;

   LoginUserFirstName: string = ‘DummyFName’;
   constructor(private customerService: CustomerService,
     private authenticationService: AuthenticationService) {
     const decodedToken = jwt_decode(localStorage.token);
     this.LoginUserFirstName=decodedToken.firstName;
     this.IsAddNew$ = this.customerService.IsAddNew$;
     this.Customers$ = this.customerService.Customers$;
  }
}
```

#### 第 42 步：处理其他功能

重新定义`CustomerComponent`中的`Save`、`AddNew`和`Cancel`方法，如下所示：

```
……..
   AddNew() {
     this.customerService.setAddNew();
  }
   Reset() {
     this.CustomerForm.reset();
  }
   Save() {
     this.customerService.Save(new Customer(this.FirstName, this.LastName));  
     this.Reset();
  }
   Cancel() {
     this.customerService.setList();    
     this.Reset();
  }
   logout() {
     this.authenticationService.logout();
  }
}
```

如你所见，现在我们的组件`class`比以前干净多了。

所有操作都简单地移到了 Angular 服务中。

#### 第 43 步 – 在模板中处理可观察对象

接下来，我们需要在`CustomerComponent`模板中处理`IsAddNew$`和`Customers$`可观察对象。

```
……
<div class=”card” [hidden]=”IsAddNew$|async”>
     <h5 class=”card-header”>Customer List</h5>
……
       <table class=”table table-striped table-bordered”>
         <thead class=”thead-dark”>
           <tr>
             <th scope=”col”>First Name</th>
             <th scope=”col”>Last Name</th>
           </tr>
```





## 步骤 44：检查输出

执行应用程序。使用正确的凭据成功登录。一旦显示 `CustomerComponent`，点击 `AddNew`。不幸的是，这不会起作用。

检查开发者工具，看看是否有任何运行时错误。令你惊讶的是，没有任何错误。

## 讨论 – 续

让我们排查前面的代码，并尝试理解其原因。

### 步骤 1

让我们检查 `IsAddNew$` 当前发出的值。

在 `CustomerComponent` 模板中，紧跟在 `nav` 元素之后，添加 `h1` 标签如下：

```
1.  <h1>IsAddNew value is {{IsAddNew$|async}}</h1>
```

现在，检查输出。

![](img/Image51020.jpg)

**图 15.1**

这证明 `IsAddNew$` 可观察对象已被正确订阅，因为发出的值显示在 `h1` 标签中。

### 步骤 2

接下来，在服务中将默认值设置为 `false`，并查看输出。

```
1.   constructor() {
2.      this.IsAddNew$ = of(true);
3.  …….
```

![](img/Image51203.jpg)

**图 15.2**

正如预期，显示 `true`，并且如你所见，可见性现在也切换了——*客户列表* 被切换为 *客户数据录入*。

这证明我们的 `IsAddNew$` 按预期工作。

那么，原因可能是什么？撤销所有排查代码，我们来讨论一下。

我们的排查证明它在开始时工作正常，但在 `AddNew` 点击后就不行了。

让我们分析 `AddNew` 方法中的代码。

```
1.  AddNew() {
2.      this.customerService.setAddNew();
3.   }
```

在 `AddNew` 方法中，我们简单地调用了 `CustomerService` 的 `setAddNew` 方法。

```
1.   setAddNew(){
2.      this.IsAddNew$ = of(true);
3.   }
```

在 `setAddNew` 方法中，我们简单地用一个新的可观察对象重新赋值了 `IsAddNew$`。

**错误原因**

这是一个简单的*面向对象编程*概念。可观察对象是一个*类*，因此它是一个*引用类型*。

我们在 `CustomerService` 中有一个变量 `IsAddNew$`。它指向一个被 `CustomerComponent` 订阅的 `Observable` 对象，并且在开始时发出 `false`。

1.  当点击 `AddNew` 按钮时，`CustomerService` 使用 *of* 方法创建一个***新的*** *Observable*，并将其赋值给 `IsAddNew$` 变量。

2.  从技术上讲，`CustomerComponent` 订阅的是旧的可观察对象。`CustomerComponent` 与这个新对象没有任何连接。

![](img/Image51210.jpg)

**图 15.3**

**解决方案**

解决方案不是创建新的可观察对象，而是从现有的*可观察对象*发出值。

从技术上讲，RxJS 中的 `Observable` 类不会暴露任何用于更新值的方法。

我想你知道解决方案。想一想。

你还记得我们之前关于 *Subject* 的讨论吗？

由于 *Subject* 既是 *Observable* 又是 *Observer*，它可以满足我们的需求。

以下是实现它的步骤：

1.  `CustomerService` 维护一个 *Subject*。

2.  `CustomerComponent` 将订阅由上述 *Subject* 暴露的可观察对象。

3.  `CustomerService` 使用同一个 *Subject* 发出新值。

![](img/Image51255.jpg)

**图 15.4**

现在，让我们在代码中实现这个逻辑。

## 实验 – 续

## 步骤 45：服务中的 Subject

在 `CustomerService` 中创建一个 `Subject` 对象，并实现前面提到的逻辑，如下所示：

```
1.   export class CustomerService {
2.    private Customers: Array<Customer>;
4.    private IsAddNewSubject: Subject<boolean>;
5.    IsAddNew$: Observable<boolean>;
6.    Customers$: Observable<Array<Customer>>;
7.    constructor() {
8.      this.IsAddNewSubject = new Subject<boolean>();
9.      this.IsAddNew$ = this.IsAddNewSubject.asObservable();
11.      this.Customers = new Array<Customer>();
12.    ………
13.   }
15.    setAddNew() {
16.      this.IsAddNewSubject.next(true);
17.   }
19.    setList() {
20.      this.IsAddNewSubject.next(false);
21.   }
23.    Save(customer: Customer) {
24.      this.Customers.push(customer);
25.      this.Customers$ = of(this.Customers);
26.      this.IsAddNewSubject.next(false);
27.   }
```

## 步骤 46：检查输出

完成上一步后，你会发现 `AddNew` 按预期工作。现在，点击 `Cancel`。

**讨论 – 续**

虽然一切看起来完美，但我们的实验中有一个小问题。为了找出它，让我们在代码中做一个快速的临时更改。

在 `CustomerComponent` 模板中，紧跟在 `nav` 标签之后，添加 `h1` 标签如下：

```
1.  <h1>IsAddNew: {{IsAddNew$|async}}</h1>
```

现在，检查输出。

**初始输出**

![](img/Image51299.jpg)

**图 15.5**

如你所见，什么也没有显示。

**点击 Add New**

点击 `Add New` 按钮并检查输出。

![](img/Image51348.jpg)

**图 15.6**

正如预期，显示 `true`。

**点击 Cancel**

接下来，点击 `Cancel` 并检查输出。

![](img/Image51390.jpg)

**图 15.7**

奇怪的是，现在显示 `false`，这也是开始时预期的。然而，在开始时我们什么也没有得到。

**你意识到这种奇怪行为的原因了吗？**

让我们再做一次实验。

将我们的实验代码替换为以下内容：

```
1.  <h1>IsAddNew: {{(IsAddNew$|async).toString()}}</h1>
```

这次，你会看到一切都崩溃了。检查开发者工具。你会发现以下运行时错误：

![](img/Image51461.jpg)

**图 15.8**

`IsAddNew$` 可观察对象只有在使用 `IsAddNewSubject.next` 方法提供数据时才会发出值，而在开始时没有提供任何值，因此它是 `null`。

这就是我们得到上述运行时错误的原因。

**开始时值为空的原因**

如果值为 `null`，Angular 插值会显示为空。

**为什么*列表部分*在开始时不可见，而*数据录入部分*是隐藏的？**

在 `CustomerComponent` 模板中，`list` 部分被配置为当 `IsAddNew$` 发出 `true` 时隐藏。检查以下代码：

```
1.  <div class=”card” [hidden]=”IsAddNew$|async”>
```

开始时，`IsAddNew$` 没有发出任何值，因此 `IsAddNew$|async` 导致 *null* 值，它不是 `true`；因此 *列表部分* 保持可见。

另一方面，*数据录入部分* 被配置为当 `IsAddNew$` 发出 `false` 时可见，借助以下代码：

```
1.   <div class=”card” [hidden]=”!(IsAddNew$|async)” ngForm #myForm=”ngForm”>
```

你知道 JavaScript 中 `!null` 是什么吗？尝试通过在控制台或 alert 中显示来找出答案。

你会发现它是 *true*，因此 *数据录入部分* 在开始时保持隐藏。

至此，你了解了当前应用程序中的这个小问题以及其背后的原因。

**我们需要对此做些什么吗？**

你可以忽略这个小问题，因为我们得到了预期的输出，但作为最佳实践，应该解决它。

这可以通过使用 `BehaviorSubject` 而不是 `Subject` 来实现。

与 `Subject` 不同，`BehaviorSubject` 构造函数接受一个参数。该值会在被订阅时立即发出。

简单来说，使用 `BehaviorSubject`，我们将有机会分配（发出）默认值。

让我们来做同样的事情。

## 实验 – 续

## 步骤 47：更改 Subject




打开 `CustomerService`，将 `Subject` 替换为 `BehaviorSubject`，如下所示：

1.  `……`
2.  `   private Customers: Array<Customer>;`
4.  `   private IsAddNewSubject: BehaviorSubject<boolean>;`
5.  `   IsAddNew$: Observable<boolean>;`
6.  `   Customers$: Observable<Array<Customer>>;`
7.  `   constructor() {`
8.  `     this.IsAddNewSubject = new BehaviorSubject<boolean>(false);`
9.  `     this.IsAddNew$ = this.IsAddNewSubject.asObservable();`
10. `……`

如上述代码所示，我们向 `BehaviorSubject` 构造函数传递了 `false` 作为参数，因为我们希望默认值为 `false`。

### 第 48 步：检查输出

现在，借助前面讨论中使用的临时 header 标签来交叉验证输出。

（测试后不要忘记删除临时代码。）

## 讨论 – 续

我们完成了吗？还是遗漏了什么？

遗憾的是，还有一个容易被忽略但不应被忽视的问题。为了找出这个问题，我想分享一种在 Angular 中进行调试的新方法。

请按以下步骤逐一操作：

### 第 1 步：选择 Customer 组件

打开 Chrome 开发者工具，导航到 `Elements` 选项卡，最后选择 `CustomerComponent`。（你需要点击它进行选择。）

![](img/Image51469.jpg)

**图 15.9**

### 第 2 步：显示选中的组件

现在，进入 `console` 选项卡并输入 `$0`。

![](img/Image51519.jpg)

**图 15.10**

它会返回当前选中的 DOM 元素。

（此操作仅在开发环境中有效。）

### 第 3 步：获取组件

接下来，在控制台中编写以下代码：

![](img/Image51553.jpg)

**图 15.11**

很酷，不是吗？它会显示附加到所选元素上的 `CustomerComponent` 实例。

### 第 4 步：探索 `IsAddNew$`

首先，展开 `CustomerComponent`，然后选择 `IsAddNew$`。

你会找到一个名为 `source` 的属性。

它就是 `BehaviorSubject`。

展开它，你会找到一个名为 `observers` 的属性，它表示订阅了该 `Observable` 的订阅者。

![](img/Image51588.jpg)

**图 15.12**

在我们的例子中，你可以看到两个订阅者。

这意味着我们订阅了 `IsAddNew$` 两次。

**你还记得订阅了两次吗？**

交叉检查你的所有代码。先别管两次。我们甚至一次都没有**手动**订阅过。

上一句中的“手动”被加粗了，因为它确实会被自动订阅。

**你还记得** `async pipe` **以及我们在模板中写的** `{IsAddNew$|async}` **吗？**

这就是自动订阅的原因。

我们在模板中写了两次。

一次用于*显示*，一次用于*隐藏*。每次使用 *async pipe* 时，observable 都会被自动订阅。

作为最佳实践，我们应该避免不必要的订阅。

可以通过手动订阅和取消订阅来实现，而不是使用 *async pipe*。但这会带来太多手动工作。还有另一种方法，那就是 `ngIf` *和* `async` *as 语法*。

### `ngIf` 和 `async as`

为了理解这个解决方案，请看下图：

![](img/Image51625.jpg)

**图 15.13**

首先，让我们理解它是什么，然后讨论可以应用此解决方案的用例：

1.  在这种方法中，我们将 `ngIf` 指令附加到一个元素上，并将其与带有 *async pipe* 的 observable 绑定，后面跟着*一个别名*。在上图中，我们有一个父级 `div` 元素，我们为其附加了 `ngIf` 指令。

2.  当 observable 发出一个值时，该值将被存储在一个变量中，并且该变量只能在该元素内部访问。在我们的例子中，*XYZ* 将保存 observable 发出的最新值。

这种方法的缺点是 observable 必须发出某个值，并且该值不能是 `false`，否则元素将不会渲染：

*   假设上例中的 `X$` observable 返回一个布尔值 `false`。在这种情况下，元素甚至不会被渲染。这就是 `ngIf` 的工作原理。

*   如果 observable 发出布尔值 `true` 或任何非空值，则元素会被渲染，并且可以使用变量 `XYZ` 访问该值。`XYZ` 变量的作用域是附加了 `ngIf` 指令的元素。

考虑到这一点，在当前 `IsAddNew$` 的场景中，这个解决方案并不适用，因为我们的 `IsAddNew$` 一开始就发出了 `false`。因此，整个父元素本身都不会被渲染。

![](img/Image51665.jpg)

**图 15.14**

**你是否在想在使用 `ngIf` 时对值取反？**

嗯，这是不可能的，因为取反操作无法与 `async` `as` 语法一起使用。

`async as` 对你来说可能看起来像是一个无用的特性。

但它并非无用。如果初始值是 `true`，我们就可以毫无问题地使用它。

### 新的解决方案 - `*ngIf` 和 else 方法

在这种方法中，我们将使用带有 `else` 的 `*ngIf`。我们已经有了一个 `*ngIf` 的例子。

嗯，它还有一些扩展。我们可以指定 `else` 部分，如下所示：

1.  `<div class=”card” *ngIf=”!(IsAddNew$|async);else AddNewContainer”…`

你是否在想 `AddNewContainer` 是什么？它引用了一个元素，当 `IsAddNew$` 发出 `false` 值时，该元素需要被显示。在我们的例子中，它将是对 *数据录入 div* 的引用。

简而言之，用 Angular 的术语来说，它是一个*模板引用变量*。

### 将模板引用变量附加到数据录入 div 时的问题

我们已经在该 `div` 元素上使用了一个*模板引用变量*。检查代码：

1.  `<div class=”card” ngForm #myForm=”ngForm”>`

如你所见，*模板引用变量* 持有附加到该元素上的 `ngForm` 指令的引用。

### 可能的解决方案

*   因此，解决方案是在上述 `div` 元素周围再添加一个父元素。这样做可能会破坏 HTML 结构，并且我们的 UI 可能会受到影响。

*   幸运的是，Angular 提供了一种创建虚拟父元素的方法；这种元素不会影响 UI，仅充当父元素。它就是 `ng-template`。我们可以称之为静默父元素。

所以，事不宜迟，让我们来实现它。

## 实验 – 续

### 第 49 步：应用带有 else 的 `*ngIf`

将 `CustomerComponent` 模板修改如下：

1.  `……`
2.  `<div class=”container-fluid pt-3” >`
3.  `   <div class=”card” *ngIf=”!(IsAddNew$|async);else AddNewContainer”>`
4.  `     ……`
5.  `   </div>`
6.  `   <ng-template #AddNewContainer>`
7.  `     <div class=”card” ngForm #myForm=”ngForm”>`
8.  `     ……`
9.  `     </div>`
10. `   </ng-template>`
11. `</div>`

### 第 50 步：检查输出

最后，你会得到 100% 可用的输出。同时，使用前面讨论中的步骤检查发生的订阅数量。

在进入下一步之前，我希望你尝试添加一条新记录。在 `FirstName` 和 `LastName` 文本框中输入一些值，然后保存一个新的 `Employee`。幸运的是，这也会完美运行。

休息一下。在阅读下一条语句之前，去享受一些属于自己的空闲时间吧。

## 讨论 – 续

现在有一个困惑。

**同样的 `IsAddNew$` 理论难道不也适用于 `Customers$` 吗？**

`Customers$` 是 `CustomerService` 中的一个变量，指向一个由 `CustomerComponent` 订阅的 observable 对象。当点击 `Save` 按钮时，会创建一个新的 observable 对象并赋值给 `Customers$` 变量。




简而言之，`CustomerComponent` 订阅的可观察对象与保存后 `Customers$` 指向的可观察对象是不同的。简单来说，它应该表现出与我们之前遇到的 `IsAddNew$` 问题相同的问题。

令人困惑的是，它并不会表现出任何问题。`save` 将毫无问题地工作。

![](img/Image51711.jpg)

**图 15.15**

让我们进一步深入探讨。

我们先从 `IsAddNew$` 开始，了解在引入 `Subject` 或 `BehaviorSubject` 解决方案之前发生了什么：

1.  如前所述，`IsAddNew$` 变量指向两组可观察对象，一组在开始时，另一组在“添加新”操作之后。

2.  这两组可观察对象都发出了 `Boolean` 值。

3.  `CustomerComponent` 订阅了第一个可观察对象，因此它只会获取第一个 `observable` 发出的值，而不会获取第二个的值。

请查看下图中的完整流程：

![](img/Image51768.jpg)

**图 15.16**

`Customers$` 的情况则略有不同。（请查看上图。）

1.  在 `CustomerService` 中，定义了一个类型为 `Array of Customer` 的类级变量。

2.  我们还在 `CustomerService` 中有一个名为 `Customers$` 的 `Observable`，它将发出上述类级变量。

3.  `CustomerComponent` 订阅了前面提到的 `Customers$`，因此它将获取 `CustomerService` 中定义的 `Array of Customer` 的*引用*。

    请注意，`CustomerComponent` 获取的是引用，而不是值，因为 `Array` 是引用类型。

4.  在 `CustomerService` 的 `Save` 方法中，我们向 `Array of Customer` 添加了一个新的 `Customer` 元素。（不要忘记，`CustomerComponent` 和 `CustomerService` 都持有这个 `Array` 的引用。）

5.  然后，用一个新的可观察对象重新初始化 `Customers$` 变量。所以现在有两个可观察对象，而 `CustomerComponent` 订阅的是旧的那个，而不是新的。（在 `IsAddNew$` 的情况下，我们也遇到了类似的情况——希望你能回想起来。我们实施的解决方案是使用 `Subject`，让同一个可观察对象发出新值。）

6.  但你知道吗，前面一点（第 5 点）其实无关紧要。无论我们是重新初始化它，还是使用 `Subject` 让旧的可观察对象发出更新后的数组，都没有关系。

    原因是，对于 `IsAddNew$`，我们有一个布尔值，它是值类型；而这次是一个 `Array`，它是引用类型，并且 `CustomerComponent` 和 `CustomerService` 共享这个引用（参见第 3 点）。因此，如果任何 `Array` 发生变化，`CustomerComponent` 都能看到这个变化。

![](img/Image51845.jpg)

**图 15.17**

这就是为什么一切都能按预期工作，而无需使用 `Subject` 的原因。

#### 总结

在本章中，我们学习了以下内容：

*   我们学习了如何使用 `RxJS of` 操作符创建自定义可观察对象。

*   我们再次演示了如何配置元素注入器。

*   我们复习了 Angular 中的 `RxJSSubject`。

*   我们学习了 Angular 中的 `RxJSBehaviorSubject`。

*   我们学习了一种在开发者工具中使用 Angular 暴露的 `ng` 对象来排查/调试 Angular 应用的新方法。

*   我们看到了 `async as` 的实际应用。

*   我们看到了 `ngIf` 与 `else` 的实际应用。

*   我们讨论了在从服务中发出引用类型时遇到的挑战。

## 第 16 章

## HTTP 服务

## 引言

终于，漫长的等待结束了。在本章中，我们将把 `CustomerService` 连接到一个实时的 REST 服务。

## 实验 – 续 – HTTP 服务

**步骤 51：将 HttpClient 注入到 CustomerService 中**

首先，将 `HttpClient` 服务注入到 `CustomerService` 中，如下所示：

```
………
import {HttpClient} from '@angular/common/http';
@Injectable()
export class CustomerService {
…….
   constructor(private httpClient: HttpClient) {
……
```

**步骤 52：获取最新的服务器代码**

确保从 GitHub 下载*第 16 章，HTTP 服务*的最新服务器代码，并像之前一样使用 `node server.js` 命令运行它。

**步骤 53：从 REST 服务获取客户数据**

将 `CustomerService` 构造函数中的代码修改如下，以获取实时数据：

```
……
   Customers$: Observable<Array<Customer>>;
   constructor(private httpClient: HttpClient) {
     this.IsAddNewSubject = new BehaviorSubject<boolean>(false);
     this.IsAddNew$ = this.IsAddNewSubject.asObservable();
     this.Customers$ = of(this.Customers);
     this.httpClient.get<Array<Customer>>('http://localhost:4000/customers').subscribe(x => {
       this.Customers = x;
    });
  }
…
```

**步骤 54：检查输出**

完成登录并进入 `CustomerComponent`。

不幸的是，我们会得到类似以下截图所示的结果：

![](img/Image51859.jpg)

**图 16.1**

打开开发者工具，查看是否有运行时错误。

![](img/Image51906.jpg)

**图 16.2**

我们的客户 API 是受保护的，只允许经过身份验证的用户发出请求。因此，我们收到了未授权的响应。

## 讨论 – 续

还记得我们在*第 11 章：身份验证*中关于基于令牌的身份验证的讨论吗？

![](img/Image51967.jpg)

**图 16.3**

我们必须确保在调用 API 时传递令牌，因为 API 是受保护的，防止未经授权的访问，否则我们将被视为未授权用户。

![](img/Image52003.jpg)

**图 16.4**

## 实验 – 续

**步骤 55：在请求头中传递令牌**

将 `CustomerService` 构造函数中的代码修改如下：

```
……
       this.Customers$ = of(this.Customers);
       this.httpClient
       .get<Array<Customer>>('http://localhost:4000/customers', {
         headers: {'x-access-token': localStorage.token},
      })
       .subscribe((x) => {
         this.Customers = x;
      });
……
```

如你所见，我们在 HTTP 请求的请求头中传递了一个令牌。这是因为我们的服务器期望在请求头中获取令牌。在其他项目中，它可能期望以 cookie 或其他形式传递。我们必须遵守这一点。

**步骤 56：检查输出**

奇怪的是，即使添加了令牌，你仍然没有得到空列表。

检查你执行 `ng serve` 命令的命令提示符，看看是否有任何错误？没有错误意味着没有编译错误。

接下来，打开 Chrome 的 `开发者工具`，检查是否有错误。没有错误意味着没有运行时错误。

![](img/Image52012.jpg)

**图 16.5**

最后，让我们设置一个断点，确认是否存在逻辑错误。在 `CustomerService` 构造函数内部设置断点，检查服务器返回了什么。

（请确保断点设置在 subscribe 内部。）

看起来 API 已经返回了正确的响应。

## 讨论 – 续

让我们逐步分析当前的代码：

1.  `CustomerComponent` 通过以下代码持有 `CustomerService` 中 `Customer$` 可观察对象的引用：

    ```
    this.Customers$ = this.customerService.Customers$;
    ```

2.  这个可观察对象通过 `async pipe` 订阅，如下所示：

    ```
    ……
    <tr *ngFor="let item of (Customers$|async)">
    ……
    ```

3.  `Customer$` 在 `CustomerService` 的构造函数中初始化。




`this.Customers$ = of(this.Customers);`

执行上述代码时，`Customers` 变量尚未被赋予任何值，更准确的说法是 `Customers` 变量持有 `undefined` 值。

因此，订阅者将收到 `undefined` 作为发出的值。这就是客户 *列表* 显示为空的原因。

接下来，在 `CustomerComponent` 的 *构造函数* 中，我们进行了 *API 调用* 以从服务器获取客户集合。

```
this.httpClient
get<Array<Customer>>('http://localhost:4000/customers', {
  headers: {'x-access-token': localStorage.token},
})
.subscribe(……);
```

之后，`CustomerService` 中的 `Customers` 变量被 API 调用响应重新初始化。

```
subscribe((x) => {
  this.Customers = x;
});
```

重新初始化 `Customers` 变量并不会向 `Customers$` 可观察对象的订阅者发出新值。因此，列表仍然为空。

![](img/Image52104.jpg)

**图 16.6**

我们需要一个解决方案，使得一旦 API 返回响应，该响应就能立即被发送到 `CustomerComponent`。

你知道怎么做吗？请思考一下，因为我相信你知道如何实现。

## 实验 – 继续

### 步骤 57：在 CustomerService 中创建 Subject 和 Observable

从 `CustomerService` 中移除 `Customers` 变量。

然后，创建一个类型为 `Subject` 的变量 `CustomersSubject`，如下所示：

```
……
export class CustomerService {
// private Customers: Array<Customer>;
   private IsAddNewSubject: BehaviorSubject<boolean>;
   IsAddNew$: Observable<boolean>;
   private CustomersSubject: Subject<Array<Customer>>;
   Customers$: Observable<Array<Customer>>;
   constructor(private httpClient: HttpClient) {
……
```

### 步骤 58：初始化 Subject 和 Observable

在 `CustomerService` 的构造函数中初始化 `CustomersSubject` 和 `Customers$`，就像我们初始化 `IsAddNewSubject` 和 `IsAddNew$` 一样。

```
constructor(private httpClient: HttpClient) {
     this.IsAddNewSubject = new BehaviorSubject<boolean>(false);
     this.IsAddNew$ = this.IsAddNewSubject.asObservable();
     this.CustomersSubject = new Subject<Array<Customer>>();
     this.Customers$ = this.CustomersSubject.asObservable();
```

### 步骤 59：发出客户数据

使用 `Subject` 类的 `next` 方法发出从 API 调用中获取的响应，如下所示：

```
     this.httpClient
       .get<Array<Customer>>('http://localhost:4000/customers', {
         headers: {'x-access-token': localStorage.token},
      })
       .subscribe((x) => {
         this.CustomersSubject.next(x);
      });
```

### 步骤 60：注释保存逻辑

由于我们的更改，你可能会在 `CustomerService` 的 `Save` 方法中发现一些语法错误。暂时注释掉 `Save` 方法中的代码。

```
Save(customer: Customer) {
// this.Customers.push(customer);
// this.Customers$ = of(this.Customers);
// this.IsAddNewSubject.next(false);
  }
```

### 步骤 61：检查输出

这次你会得到一个奇怪的输出。

![](img/Image52112.jpg)

**图 16.7**

## 讨论 – 继续

在上面的输出中，你可以看到三行。这意味着 API 返回了一个包含三条记录的列表。这次让我们用一种新的方式来排查问题。

打开 `CustomerComponent` 模板，然后在 `nav` 元素之后创建 `div` 元素，如下所示：

```
……
</nav>
<div>
   {{Customers$|async}}
</div>
<div class="container-fluid pt-3">
……
```

现在检查输出。

![](img/Image52214.jpg)

**图 16.8**

这并没有帮助。它只是证明我们得到了三个对象，但没有提供关于这三个对象的任何细节。

如果我说有一种方法可以显示其 JSON 格式的表示呢？

这可以通过使用 *json 管道* 来实现。

*json 管道将值转换为其 JSON 格式的表示。*

在 `asyncpipe` 之后应用 *json* 管道，如下所示：

```
<div>
   {{Customers$|async|json}}
</div>
```

上述代码表明 `asyncpipe` 将附加到 `Customer$`，而 `jsonpipe` 将附加到 `asyncpipe` 返回的响应。

当多个管道附加时，顺序至关重要。

现在检查输出。

![](img/Image52256.jpg)

**图 16.9**

**你能理解为什么我们得到三个空行吗？**

我们得到了 *firstName* 和 *lastName*，而在 `CustomerComponent` 模板中，我们显示的是 *FName* 和 *LName*。我们的 *模型* 和 API 响应不兼容。在将响应发送给订阅者（即 `CustomerComponent`）之前，我们必须将 API 响应转换为我们自己的 *模型*。为此，我们可以使用 *RxJS* 的 `map` 操作符。

## 实验 – 继续

### 步骤 62：使用 map 操作符

使用 RxJS 的 map 操作符将实际响应转换为所需响应，如下所示：

```
……
import {BehaviorSubject, Observable, Subject} from 'RxJS';
import {map} from 'RxJS/operators';
import {Customer} from '../Models/customer';
……
     this.httpClient
       .get<Array<{firstName: string, lastName: string}>>('http://localhost:4000/customers', {
         headers: {'x-access-token': localStorage.token},
      }).
       pipe(map(customerAPIResponse => {
         return customerAPIResponse.map(customer => new Customer(customer.firstName, customer.lastName));
      }))
       .subscribe((x) => {
         this.CustomersSubject.next(x);
      });
……
```

## 讨论 – 继续

**你是否在想 `Array<{firstName: string, lastName: string}>` 是什么？**

它表示一个 *对象数组*——一个包含两个属性 `firstName` 和 `lastName` 的对象。

请注意，你可以选择创建单独的类来保存 API 响应，这将是最佳实践。

但在应用程序中，很多时候我们会遇到这样的情况：我们不想创建单独的类，但又需要一些动态的东西。在这种情况下，我们可以这样使用。

但对于这个场景，为其创建一个自定义类也是很好的。

## 实验 – 继续

### 步骤 63：创建 CustomerItemResponse 类

在 `Modes/HttpResponses` 文件夹中创建一个新文件 `customer.response.ts`，内容如下：

```
export class CustomerItemResponse{
   constructor(public firstName: string, public lastName: string) {
  }
}
```

### 步骤 64：使用 CustomerItemResponse 类

重写我们的 `CustomerService` API 逻辑，如下所示：

```
……
     this.httpClient
       .get<Array<CustomerItemResponse>>('http://localhost:4000/customers', {
         headers: {'x-access-token': localStorage.token},
      }).
       pipe(map(customerAPIResponse => {
         return customerAPIResponse.map(customer => new Customer(customer.firstName, customer.lastName));
      }))
       .subscribe((x) => {
         this.CustomersSubject.next(x);
      });
……
```

## 讨论 – 继续

**`Observable.pipe` 和 `Observable.subscribe` 的区别**

`pipe` 方法用于链式调用 *Observable 操作符*，而 `subscribe` 用于激活 *Observable* 并监听发出的值。

*   更准确地说，我们订阅 *observable* 以获取发出的值。为此，使用 `subscribe` 方法。





在值到达 `subscribe` 方法之前，发出的值会通过各个操作符进行管道传输，这些操作符可能会改变值甚至阻止进一步发射。为此，使用了 `pipe` 方法。

在前面的例子中，我们配置了发出的记录通过 `map` 操作符进行管道传输。`map` 操作符允许我们将值转换为其他内容。

如你所见，在上面的代码中，我们将 `Array<CustomerItemResponse>` 转换成了 `Array<Customer>`。

## 实验 – 续

### 步骤 65：检查输出

最后，我们得到了期待已久的输出。

![](img/Image52354.jpg)

**图 16.10**

## 讨论 – 续

让我们解决拼图的最后一部分，即通过 API 保存记录。

## 实验 – 续

### 步骤 66：创建请求实体

在 `Models` 文件夹内创建一个新文件夹 `HttpRequests`，然后创建一个新文件 `newcustomer.requests.ts`，内容如下：

```
export class NewCustomer{
   constructor(public firstName: string, public lastName: string) {  }
}
```

你可能会想，为什么我们没有使用现有的某个类。嗯，如果你愿意，也可以使用。

我更喜欢在应用程序中使用以下三组不同的实体：

1. 一组用于表示模板中所需的数据。
2. 一组用于表示 HTTP 响应。
3. 一组用于表示 HTTP 请求。

### 步骤 67：将 Customer 映射到 NewCustomer

在 `CustomerService` 的 `Save` 方法中，使用 `Customer` 类实例创建一个 `NewCustomer` 类的实例。

```
   Save(customer: Customer) {
// this.Customers.push(customer);
// this.Customers$ = of(this.Customers);
// this.IsAddNewSubject.next(false);
     const newCustomer: NewCustomer = new NewCustomer(
       customer.FName,
       customer.LName
    );
  }
```

### 步骤 68：保存 Customer

在 `CustomerService` 的 `Save` 方法中进行 API 调用，如下所示：

```
Save(customer: Customer) {
// this.Customers.push(customer);
// this.Customers$ = of(this.Customers);
// this.IsAddNewSubject.next(false);
     const newCustomer: NewCustomer = new NewCustomer(
       customer.FName,
       customer.LName);
     this.httpClient
       .post('http://localhost:4000/customers', newCustomer)
       .subscribe(() => {
         this.IsAddNewSubject.next(false);
      });
  }
```

如你所见，这次我们必须使用 `HttpClient` 的 `post` 方法而不是 `get` 方法，因为我们要发布数据。

在 subscribe 中，我们从 `IsAddNewSubject` 发出 true 值，这将使我们切换回列表屏幕。

### 步骤 69：检查输出

执行应用程序。完成登录并进入 `CustomerComponent`。通过点击 `Add New` 按钮切换到数据录入屏幕。输入一些虚拟值并点击 `Save`。

它肯定无法工作。

你能猜到原因吗？试着思考一下，找出原因。

如果你找不到原因，那么打开开发者工具。它会告诉你原因——API 受到未授权访问的保护。我们需要传递令牌。

### 步骤 70：传递令牌

像我们在 get 请求中所做的那样，在头部传递令牌。

```
this.httpClient
       .post('http://localhost:4000/customers', newCustomer, {
         headers: {'x-access-token': localStorage.token},
      })
       .subscribe(() => {
         this.IsAddNewSubject.next(false);
      });
```

### 步骤 71 – 检查输出

尝试创建一个新 Customer，名字为 Gabbar，姓氏为 Singh。保存后，你会得到类似下面的奇怪输出：

![](img/Image52365.jpg)

**图 16.11**

发生了什么？我们来讨论一下。

## 讨论 – 续

在继续阅读之前，我建议你在浏览器中执行一次硬刷新（*F5*）。

奇怪的是，你会看到新记录已添加，并因此显示在列表中。

让我们逐步理解这里发生了什么。

首先，让我们看看开始时我们得到了什么：

1. `CustomerComponent` 使用 `async` 管道订阅了 `IsAddNew$`，`*ngIf` 指令将使用发出的值，该值在开始时为 *false*。
2. `*ngIf` 指令仅在值为 `true` 时才让元素被创建。因此，开始时只渲染了列表部分，而*表单部分*甚至不会渲染到 DOM 中。
3. 在服务中，从 API 获取客户列表并通过 `Subject` 发出。
4. 发出的客户列表显示在视图中。

![](img/Image52420.jpg)

**图 16.12**

现在，让我们理解当我们点击 `Add New` 按钮时会发生什么。

![](img/Image52486.jpg)

**图 16.13**

1. `IsAddNew$` 发出 `false`，导致列表部分从 DOM 中移除，*表单部分*被渲染。
2. 现在，没有人订阅 `Customers$`。此时，如果它发出某些内容，将没有人捕获它。

最后，让我们看看 *保存/取消* 后的情况：

1. `IsAddNew$` 再次发出 *true*。
2. 因此，*表单部分*从 DOM 中移除，*列表部分*被重新创建。
3. 现在令人惊讶的是，这个新创建的*列表部分*与原来的不同。

   当点击 `Add New` 按钮时，旧的*列表部分*和相应的订阅已经完全消失。

   新的*列表部分*也订阅了 `Customer$`，但由于它是一个新的订阅，它不会获得之前发出的值。

![](img/Image52497.jpg)

**图 16.14**

解决方案是在*保存*后发起一个新的 API 调用，并再次发出整个列表。

## 实验 – 续

### 步骤 72：创建 LoadCustomers 方法

由于读取新客户的逻辑与之前相同（构造函数中的逻辑），让我们创建一个可复用的函数，并在两个地方使用它。

```
……
     constructor(private httpClient: HttpClient) {
     this.IsAddNewSubject = new BehaviorSubject<boolean>(false);
     this.IsAddNew$ = this.IsAddNewSubject.asObservable();
     this.CustomersSubject = new Subject<Array<Customer>>();
     this.Customers$ = this.CustomersSubject.asObservable();
     this.LoadCustomers();
  }
   private LoadCustomers(): void{
     this.httpClient
     .get<Array<CustomerItemResponse>>('http://localhost:4000/customers', {
       headers: {'x-access-token': localStorage.token},
    }).pipe(
       map((customerAPIResponse) => {
         return customerAPIResponse.map(
           (customer) => new Customer(customer.firstName, customer.lastName)
        );
      })
    ).subscribe((x) => {
       this.CustomersSubject.next(x);
    });
  }
……
```

### 步骤 73：更新 Save 方法

将 `CustomerService` 中的 `Save` 方法更改如下：

```
  Save(customer: Customer) {
     const newCustomer: NewCustomer = new NewCustomer(
       customer.FName,
       customer.LName
    );
     this.httpClient
       .post('http://localhost:4000/customers', newCustomer, {
         headers: {'x-access-token': localStorage.token},
      }).subscribe(() => {
         this.LoadCustomers();
         this.IsAddNewSubject.next(false);
      });
  }
```

### 步骤 74：检查输出





最后，如果你的输出不符合预期，请重新检查前面提到的所有步骤，我们就能回到正轨。取消操作也会遇到类似的问题。把它作为作业完成。

#### 总结

那么，经过这么多思考和编码，我们终于成功实现了 `CustomerService`。让我们列出本章涵盖的所有主题：

*   我们在应用中再次使用了 `HttpClient` 服务。
*   我们使用了 `HttpClient.get` 和 `post` 方法的泛型版本。
*   我们再次演示了 `Subject` 的用法。
*   我们讨论了基于令牌的身份验证，并在应用中实现了它。
*   我们讨论了 json 管道。使用这个管道，我们可以通过插值显示对象的内容。它们仅用于故障排除。
*   我们了解到，当涉及多个管道时，顺序至关重要。
*   我们演示了将匿名对象用作泛型参数。虽然不推荐，但在项目中可能会看到。
*   我们了解到，我们使用 `subscribe` 方法来获取发出的值，并使用 `pipe` 方法将值通过各个操作符进行管道传输，这些操作符可能会改变值甚至停止进一步发射。
*   我们讨论了 RxJS 中的 `map` 操作符。使用它，我们可以将实际的 HTTP 响应转换为所需的响应。

## 第 17 章

### 令牌拦截器

## 引言

我们现在的应用还有改进的空间吗？

在继续之前，请再次通读完整代码作为复习。如果你能找到改进之处，那就太好了。

问题在于添加令牌。继续下去，我们几乎每次 API 调用都要这样做。有没有更好的方法？

有的，那就是 HTTP 拦截器。使用它，我们可以转换每一个发出的请求或接收的响应。

我们将在演示中创建并注册一个拦截器，它会通过在请求头中添加令牌来转换每一个发出的请求。

迫不及待想看看它的效果，让我们开始吧。

#### 实验 – 续 – 令牌拦截器

**步骤 75：创建 TokenInterceptorService**

在 `Services` 文件夹内，创建一个新文件夹 `Interceptors`，然后创建一个新文件 `http.interceptor.ts`，内容如下：

```
import {HttpEvent, HttpHandler, HttpInterceptor, HttpRequest}
                   from '@angular/common/http';
import {Injectable} from '@angular/core';
import {Observable} from 'RxJS';

@Injectable()
export class TokenInterceptorService implements HttpInterceptor {

   constructor() {}
   intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {

      const token = localStorage.token;
      let newHeaders = req.headers;
      if (token) {
// 如果 token 不为 undefined
         newHeaders = newHeaders.append('x-access-token', token);
      }

// HttpRequest 是不可变的，因此无法直接修改
// 因此我们克隆它并添加请求头
      const authReq = req.clone({headers: newHeaders});
      return next.handle(authReq);
  }
}
```

## 讨论 – 续

**它看起来像是一个服务吗？**

应该是的，因为它就是一个服务。下一步，我们将为其配置注入器。

**理解代码**

这是一个简单的代码。

我们有一个实现了 `HttpInterceptor` 接口的类，这迫使我们定义 `intercept` 方法。

在 `intercept` 方法内部，我们*克隆*现有的 *HTTP 请求*，因为我们无法直接修改 HTTP 请求，它们是不可变的（*immutable*）。*不可变*意味着它们不能被更改。

如你所见，我们将自定义请求头传递给了 `clone` 方法。因此，新的请求对象将附带身份验证请求头。

**应该为 TokenInterceptorService 配置哪个注入器？**

正如我所说，我们需要为 `TokenInterceptorService` 配置注入器。否则，Angular 的依赖注入系统将无法注入 `TokenInterceptorService` 实例。问题是，我们应该配置哪个注入器？

让我们回顾一下关于 Angular DI 的知识。

1.  到目前为止，我们创建了几个服务，并配置了模块注入器和元素注入器。
2.  我们使用 `Injectable` 装饰器配置模块注入器，对于元素注入器，我们使用了 `Component` 装饰器。
3.  到目前为止，我们只有一个 *Angular 模块* 在运行，那就是根模块。因此，我们拥有的唯一模块注入器是根注入器，它创建了一个应用范围内的单例实例。
4.  我们配置了 `CustomerComponent` 的元素注入器。它创建了一个作用域为组件生命周期的服务实例。

在未来的章节中，我们将创建更多组件和更多模块，并再次讨论注入器。

根据你对服务的了解，你认为应该为 *拦截器* 选择哪个注入器？

应该是根模块注入器，但这次有一个转折。

我们不能为此目的使用 `Injectable` 装饰器。

你还记得我们最初是如何为 `AuthenticationService` 配置注入器的吗？

`providers:[{provide: AuthenticationService, useClass: AuthenticationService}`

后来我们了解到，当 `provide` 和 `useClass` 的值相同时，可以使用简写语法。

`Providers: [AuthenticationService]`

尽管由于树摇（tree-shaking）的考虑，推荐使用 `Injectable` 装饰器，但我们不能使用它，因为它不允许我们显式指定 DI 令牌。

**为什么需要为令牌拦截器显式指定 DI 令牌？**

正如我们之前讨论过的，拦截器允许我们在中间修改请求-响应。创建拦截器就像钩入 Angular 的默认执行流程。为拦截器配置注入器不会像为普通 Angular 服务那样简单。对于拦截器，我们需要显式指定 DI 令牌（`HTTP_INTERCEPTORS`）。

**如何在不使用 Injectable 装饰器的情况下配置根注入器？**

那么最后，你将看到借助 `NgModule` 装饰器配置模块注入器的方法。

## 实验 – 续

**步骤 76：配置注入器**

在 `AppModule` 中配置根模块注入器，如下所示：

```
import {HttpClientModule, HTTP_INTERCEPTORS} from '@angular/common/http';
……
import {TokenInterceptorService} from './Services/Interceptors/http.interceptor';
@NgModule({
   ……
   providers: [{provide: HTTP_INTERCEPTORS, useClass: TokenInterceptorService}],
   bootstrap: [AppComponent],
})
export class AppModule {}
```

**步骤 77：检查输出**

一切就绪，是时候检查输出了。切换到浏览器并查看输出。

到目前为止，你得到了最好的输出。“*一个白屏*。”

![](img/Image52550.jpg)

**图 17.1**

检查开发者工具。你会发现一种新的错误。

![](img/Image52622.jpg)

**图 17.2**

我们将在下一章讨论多提供者。现在，让我们完成这个实验。

**步骤 78：将常规提供者转换为多提供者**

为此，将 `multi` 属性附加到提供者，并将其值设置为 `true`。

```
……
   providers: [{provide: HTTP_INTERCEPTORS,
               useClass: TokenInterceptorService, multi:true}],
   bootstrap: [AppComponent],
})
export class AppModule {}
```

**步骤 79：清理 CustomerService**




由于 token-interceptor 已经就位，我们无需显式地将令牌注入到请求中。因此，清理 `CustomerService` 的方法如下：

```
……
  private LoadCustomers(): void{
     this.httpClient
     .get<Array<CustomerItemResponse>>(‘http://localhost:4000/customers’).pipe(
       map((customerAPIResponse) => {
         return customerAPIResponse.map(
           (customer) => new Customer(customer.firstName, customer.lastName));
      })
    ).subscribe((x) => {
       this.CustomersSubject.next(x);
    });
  }
……
   Save(customer: Customer) {
     const newCustomer: NewCustomer = new NewCustomer(
       customer.FName,customer.LName);
     this.httpClient
       .post(‘http://localhost:4000/customers’, newCustomer).subscribe(() => {
         this.LoadCustomers();
         this.IsAddNewSubject.next(false);
      });
  }
……
```

**第 80 步：检查输出**

执行并确认客户列表和数据录入屏幕均正常工作。

#### 总结

让我们列出本章涵盖的所有主题：

*   我们学习了如何创建和配置 HTTP 拦截器。

*   我们讨论了 `HttpInterceptor` 接口，创建拦截器时需要实现该接口。

*   我们了解到，由于 HTTP 请求是不可变的，因此无法在拦截器中直接修改它们。因此，我们需要克隆现有请求。我们将标头附加到克隆的请求上，然后将该克隆的请求进一步传递到管道中。

*   我们演示了配置注入器时使用的长语法和短语法。

*   我们了解到，需要显式指定 DI 令牌——`HTTP_INTERCEPTORS`，以便为 HTTP 拦截器配置注入器。

*   我们了解到，尽管由于摇树优化（tree-shaking）的考虑，推荐使用 `Injectable` 装饰器，但我们不能一直用它来配置模块注入器，因为它不允许我们显式指定 DI 令牌。

*   我们还了解了使用 `NgModule` 装饰器配置注入器的好处。与 `Injectable` 装饰器相比，它提供了更多的配置选项。

*   我们了解到，注入器需要为 HTTP 拦截器配置多提供者（multi providers）。

## 第 18 章：多提供者

## 引言

在本章中，我们将讨论多提供者。如果你愿意，可以暂时跳过本章。

### 常规提供者

在查看了第 17 章“令牌拦截器”中的上一个错误后，你一定已经明白 Angular 中存在不止一种提供者。

有常规提供者，还有多提供者。

我们为 `CustomerService`、`AuthenticationService` 和 `AuthGuard` 定义的提供者都属于常规提供者。

这意味着，对于一个 DI 令牌，将定义一个提供者。

### 多提供者

对于一个 DI 令牌，将定义多个提供者。当应用程序中需要注入一个 DI 令牌时，注入器会注入一个数组。

让我们快速做一个研究来理解这一点。

创建一个新的服务 `MultiRndService`，如下所示：

```
@Injectable()
export class MultiRndService{
     m1(){
       console.log(‘MultiService1’);
    }
}
```

现在，再创建一个服务 `MultiRndService2`，如下所示：

```
@Injectable()
export class MultiRndService2{
     m2(){
       console.log(‘MultiService2’);
    }
}
```

现在，使用常规提供者配置根注入器，如下所示：

```
…….
   providers: [{provide: HTTP_INTERCEPTORS,
            useClass: TokenInterceptorService, multi: true},
     {provide:MultiRndService, useClass: MultiRndService},
     {provide:MultiRndService, useClass: MultiRndService2},
  ],
   bootstrap: [AppComponent],
})
export class AppModule {}
```

如你所见，我们对两个提供者使用了相同的 DI 令牌。

接下来，在 `CustomerComponent` 的构造函数中指定一个类型为 `MultiRndService` 的参数。

```
……
constructor(private customerService: CustomerService,
               private authenticationService: AuthenticationService,
               private rndService: MultiRndService
              ) {
     const decodedToken = jwt_decode(localStorage.token);
……
```

现在，在构造函数中设置一个断点，让我们检查注入的是什么。

![](img/Image52720.jpg)

**图 18.1**

你可以看到，注入的是 `MultiRndService2` 类的实例。

在继续之前，我想通过解释不兼容的类型（`MultiRndService2`）是如何被注入的，来让你的生活更轻松。

嗯，请记住注入发生在运行时，而在运行时，一切都是 *JavaScript*，所以无论你期望什么，任何东西都可能被注入。

因此，*provide* 和 *useClass* 中的值不需要彼此兼容。

在真实系统中，我会在这两种类型之上定义一个*基类*或*接口*，并将其用作 DI 令牌。

现在，让我们回到研究。将 `multi` 属性设置为 `true` 添加到两个*提供者*上，并检查输出。

```
providers: [{provide: HTTP_INTERCEPTORS,
  useClass: TokenInterceptorService, multi: true}
     ,{provide:MultiRndService, useClass: MultiRndService, multi: true},
     {provide:MultiRndService, useClass: MultiRndService2, multi: true},
  ],
```

![](img/Image52805.jpg)

**图 18.2**

如你所见，这次两个类的实例以数组的形式被注入。

**如果我们将其中一个指定为多提供者，另一个指定为常规提供者，会发生什么？**

在这种情况下，我们会收到“无法混合多提供者和常规提供者”的错误。

**为什么在配置 `HTTP_INTERCEPTOR` 的注入器时会收到“无法混合...”的错误？**

我们在第 17 章“令牌拦截器”中创建了一个 HTTP 拦截器，然后配置了模块注入器。关键是我们只做了一次。

我们没有为 `HTTP_INTERCEPTOR` 创建多个提供者。

如果是这样，为什么我们在创建常规提供者时会收到“无法混合...”的错误？

如果你还记得，在之前的某个实验中，我们在 `AppModule` 中导入了 `HttpClientModule`。

（检查 `AppModule` 中 `NgModule` 装饰器的 imports 部分。）

当我们将一个 Angular 模块导入到另一个模块时，提供者会被合并。因此，在我们的例子中，`HttpClientModule` 中定义的所有提供者都合并到了 `AppModule` 的提供者中。

Angular 已经在 `HttpClientModule` 的 `NgModule` 装饰器中为 DI 令牌 `HTTP_INTERCEPTOR` 配置了多提供者。

这就是为什么当我们用常规提供者配置注入器时，会收到“无法混合...”的错误。

**你不觉得构造函数的 rndService 参数应该声明为数组吗？**

问题是，我们不应该像下面这样编写 `CustomerComponent` 的构造函数吗：

```
……
   constructor(private customerService: CustomerService,
               private authenticationService: AuthenticationService,
               private rndService: Array<MultiRndService>
              ) {
……
```

如果我们这样做，将会收到以下错误：

![](img/Image52812.jpg)

**图 18.3**

我们需要为 `Array` 定义一个提供者。虽然这对于任何强类型语言的开发者来说似乎合乎逻辑，但这会让我们的生活更加复杂。




在这种情况下，我们使用 `Injection Token` 或 `String Token` 来代替 `Type Token`。

### DI 令牌

还记得我们讨论过的 DI 令牌吗？

我们了解到，注入器在应用程序中注入时，会使用令牌来识别正确的提供者。

我们还指定了三种令牌——`Type Token`、`String Token` 和 `Injection Token`。

到目前为止，我们一直在使用类型令牌。

但有些场景下，我们无法将类型指定为令牌，比如前面提到的那种情况。

因此，在这种情况下，我们使用 `String token` 或 `Injection token`。

### 字符串令牌示例

使用提供者配置注入器，但使用字符串令牌而不是类型令牌。

```
providers: [{provide: HTTP_INTERCEPTORS,
useClass: TokenInterceptorService, multi: true}
     , {provide: "RND_VALUE", useClass: MultiRndService, multi: true},
     {provide: "RND_VALUE", useClass: MultiRndService2, multi: true},
  ],
   bootstrap: [AppComponent],
})
export class AppModule {}
```

接下来，按如下方式修改组件的构造函数：

```
constructor(private customerService: CustomerService,
               private authenticationService: AuthenticationService,
               @Inject("RND_VALUE")x: Array<MultiRndService>
              ) {
```

你会注意到现在构造函数参数上附加了一个专门的装饰器——`Inject`。

`@Inject()` 是一种手动机制，用于让 Angular 知道某个参数必须被注入。

最棒的是参数类型，它是一个 `Array<MultiRndService>`。

像之前一样进行调试，你会注意到两个 `Service` 实例都以数组的形式被注入。

### 注入令牌示例

在编程中，使用魔法字符串通常被认为是一种不良实践。使用 `String token` 也被视为不良实践，因为存在拼写错误的风险，从而导致运行时错误。

因此，推荐的做法是改用 `Injection` 令牌。

为此，首先按如下方式声明一个类型为 `InjectionToken` 的常量变量。（这只是 RND，所以在你创建 `MultiRNDService` 的同一个文件中定义它。）

```
export const RND_TOKEN = new InjectionToken<MultiRndService[]>
('CollectionOfRNDService');
```

接下来，按如下方式修改提供者：

```
import {MultiRndService, MultiRndService2, RND_TOKEN} from './Services/multi-rnd.service';
@NgModule({
   ......
   providers: [{provide: HTTP_INTERCEPTORS,
       useClass: TokenInterceptorService, multi: true}
// ,{provide: "RND_VALUE", useClass: MultiRndService, multi: true},
// {provide: "RND_VALUE", useClass: MultiRndService2, multi: true},
     ,{provide: RND_TOKEN, useClass: MultiRndService, multi: true},
     {provide: RND_TOKEN, useClass: MultiRndService2, multi: true},
  ],
   bootstrap: [AppComponent],
})
export class AppModule {}
```

现在任何地方都没有硬编码的字符串了。如果出现拼写错误，我们会得到一个编译错误。

最后，按如下方式修改组件的构造函数：

```
constructor(private customerService: CustomerService,
               private authenticationService: AuthenticationService,
// @Inject("RND_VALUE")x: Array<MultiRndService>
               @Inject(RND_TOKEN)x: Array<MultiRndService>
              ) {
```

进行同样的调试以检查输出。

### 为什么需要多提供者？

现在你知道了什么是多提供者。

你也知道了如何创建多提供者。

最后一个问题是：为什么需要它？

有时在创建可复用的服务时，我们需要它。

现在，假设服务逻辑的一部分将在库本身中定义，而另一部分将由使用该库的人提供。这时使用多提供者就变得至关重要。

#### 总结

让我们回顾一下本章学到的主题：

*   我们了解到，可以为单个 DI 令牌定义多个提供者。这被称为多提供者。
*   我们了解到，如果为单个 DI 令牌定义了多个常规提供者，则一个提供者会按顺序替换另一个。
*   我们了解到，如果为单个 DI 令牌定义了多个多提供者，则注入器会注入一个服务数组。
*   我们了解到，在定义提供者时，DI 令牌和实际服务不要求兼容。它们可以具有完全不同的结构。
*   我们了解到，不能为单个 DI 令牌同时定义常规提供者和多提供者。对于单个 DI 令牌，要么所有提供者都是常规的，要么所有提供者都是多提供者。
*   我们了解到，建议将字符串或注入令牌与多提供者一起使用，而不是类型令牌。
*   我们了解了 `Inject` 装饰器，它可以让我们手动告诉 Angular 该参数必须被注入。它将在字符串和注入令牌的情况下使用。
*   我们了解到，在创建可复用服务时，多提供者有时非常有用。

## 第 19 章

## 编译时配置

## 引言

如果你有任何应用程序开发经验，你一定已经发现了当前应用程序的缺点。API URL 直接嵌入在应用程序内部，从长远来看，这会给我们带来很多麻烦。

在生产模式下，我们可能有不同的 API URL。当前的代码将非常难以维护，因为我们必须在每个地方进行更改。我们需要在项目中引入一些配置机制，这正是我们将在本章中学习的内容。

## 编译时配置与运行时配置

编译时配置意味着配置将在编译时完成，而运行时配置意味着配置将在部署时完成。

如果你感到困惑，不用担心。让我们通过演示来理解两者。

## 实验 – 续 – 编译时配置

**步骤 81：创建第二个服务器**

第一步是创建另一个服务器，以确认配置更改是否生效。

为此，在 `server` 文件夹中快速创建一个新的 JavaScript 文件，并将其命名为 `newServer.js`。

将现有 `server.js` 中的所有内容复制到 `newServer.js` 中。

不用担心其中的代码。只需将端口和默认客户集合更改为其他值。

```
const port = process.env.PORT || 5000;
......
let customers = [
   {customerId: 1, firstName: "A", lastName: "B"},
   {customerId: 2, firstName: "C", lastName: "D"},
   {customerId: 3, firstName: "E", lastName: "F"},
];
```

**步骤 82：运行服务器**

现在打开一个新的命令提示符，导航到 `server` 文件夹，并通过执行以下命令运行这个新服务器：

```
node newServer.js
```

现在，我们有两个服务器在运行——一个使用端口 4000，另一个使用端口 5000；两者都返回不同的数据集。

## 讨论 – 续

Angular 提供了编译时配置的功能。在 `src` 文件夹中，有一个名为 `environments` 的文件夹。它包含两个文件：`environment.ts` 和 `environment.prod.ts`，内容如下：

```
// environment.ts
export const environment = {
   production: false
};
```

```
// environment.ts
export const environment = {
   production: true
};
```

如你所见，它导出了一个名为 `environment` 的常量对象，其中包含一个属性——`production`。

## 实验 – 续

**步骤 83：在环境中创建一个 apiURL 键**





### 步骤 84：在服务中动态获取 API URL

按如下方式修改 `CustomerService` 中的 `LoadCustomers` 方法：

```
private LoadCustomers(): void{
     this.httpClient
     .get<Array<CustomerItemResponse>>(`${environment.apiUrl}/customers`)
     .pipe(
       map((customerAPIResponse) => {
         return customerAPIResponse.map(
           (customer) => new Customer(customer.firstName, customer.lastName)
        );
      })
    ).subscribe((x) => {
       this.CustomersSubject.next(x);
    });
  }
  ……
```

如你所见，现在我们不再使用固定的 API URL，而是从配置中获取动态 URL。

### 步骤 85：构建项目

按下 *ctrl+c* 键停止当前正在执行的 `ng serve` 命令。

接下来，使用 `ng build` 命令构建应用程序。

你还记得吗？在 Angular 入门 *第 8 章* 中，我们曾使用带有 `--prod` 标志的 `ng build` 命令。而这次我们执行时没有加该标志。我们很快就会讨论两者的区别。

它会在根文件夹内创建一个名为 `dist/lab4-ng` 的新文件夹，如下所示：

![](img/Image52928.jpg)

**图 19.1**

### 步骤 86：托管应用程序

打开一个新的命令提示符，如果尚未安装 lite-server，请使用以下命令进行安装：

```
npm install lite-server -g
```

lite-server 是一个简单的开发用途 Web 服务器，可用于测试 Web 应用程序。

接下来，导航到 `dist\lab4-ng` 文件夹。然后运行 lite-server 命令，如下所示：

![](img/Image53012.jpg)

**图 19.2**

### 步骤 87：检查应用程序

打开浏览器并检查 http://localhost:3000。

导航到客户界面并检查输出。

你应该会看到运行在 4000 端口的服务器返回的记录。

### 步骤 88：在生产模式下重新构建应用程序

停止 `lite-server`，导航到应用程序的根文件夹，然后重新构建应用程序。但这次要使用 `--prod` 标志。它将创建一个优化后的、可用于生产环境的应用程序构建。

![](img/Image53051.jpg)

**图 19.3**

这次 `dist\lab4-ng` 文件夹中包含的文件会比之前少。

## 讨论 – 续

*   生产构建与非生产构建的一个区别是，在生产构建中，*源映射文件*（扩展名为 `map.js` 的文件）会缺失。源映射文件包含有关源 TypeScript 文件的信息。正是由于源映射文件，我们才能直接在浏览器中调试 TypeScript 文件。

*   第二个区别是，生产构建中不会生成 `vendor.js` 文件。该文件原本用于包含导入到应用程序中的第三方库。

    主包在生产构建期间会被优化。在生成最终包时，所有未使用的代码都会被移除；因此，对于生产构建，供应商构建会被集成到主包中。

### 步骤 89 – 检查应用程序

再次启动 *lite-server* 并检查输出。这次，你将看到来自运行在 5000 端口的服务器的客户记录。

这证明，被考虑的是 *environment.prod.ts* 而不是 *environment.ts*。

这被称为*编译时配置*。在编译时，应用程序会配置一个 API URL。（同时修改 *Save* 函数并进行测试。）

#### 总结

让我们回顾一下本章学到的主题：

*   我们首先理解了应用程序中配置的必要性。

*   我们学习了编译时配置和运行时配置的区别。编译时配置意味着配置将在编译时完成，而运行时配置意味着它将在部署时完成。

*   我们了解了 *environment.ts* 文件，以及在生产模式下它如何被 *environment.prod.ts* 文件替换。

*   我们分别使用 *ng build* 和 *ng build --prod* 命令生成了 Angular 应用程序的非生产模式和生产模式构建。

*   我们了解到，在非生产构建中，Angular CLI 也会生成源映射文件；因此，我们可以在运行时直接调试 TypeScript 文件。

*   我们了解到，在生产构建中不会得到单独的 *vendor.js* 文件，因为它被集成到了 *main* 包中。

*   我们演示了一个名为 lite-module 的 Angular 模块，它可以用作静态文件的开发用途 Web 服务器。

## 第 20 章

### 运行时配置

## 引言

在上一章中，我们讨论了编译时配置。

但在某些情况下，运行时配置更为合适。在本章中，我们将学习如何实现它。

## 实验 – 续 – 运行时配置

### 步骤 90：创建配置文件

在 `src/assets` 文件夹中创建一个新文件 `config.json`，内容如下：

```
{
   “apiUrl”: “http://localhost:4000”
}
```

## 讨论

**为什么是 *assets* 文件夹？**

你一定在想，为什么我们特意把文件放在 `assets` 文件夹中。

如你所知，在当前实验中，我们计划启用运行时配置。

为此，我们需要 `config.json` 文件原样保留在最终构建中。

`ng build` 命令的一个很棒的特性是，*assets* 文件夹会原样复制到最终构建中。

你是否好奇为什么 assets 文件夹如此特殊？

你可以在 `angular.json` 文件中找到答案。

![](img/Image53136.jpg)

**图 20.1**

你注意到 *build* 部分中的 *assets* 部分了吗？

在其中，我们将 *assets* 文件夹指定为值之一。Angular CLI 会将此部分中定义的所有文件夹和文件原样复制到最终构建中。

### 步骤 91：创建 AppConfigService

接下来，在 `Services` 文件夹中创建一个名为 `app-config.service.ts` 的文件，内容如下：

```
import {HttpClient} from ‘@angular/common/http’;
import {Injectable} from ‘@angular/core’;
import {Subscription} from ‘RxJS’;
@Injectable({
   providedIn: ‘root’
})
export class AppConfigService {
   apiUrl: string;
   constructor(private http: HttpClient) {}
   loadConfig(): Subscription {
     return this.http
       .get<{apiUrl: string}>(‘./assets/config.json’)
       .subscribe(config => {
         this.apiUrl = config.apiUrl;
      });
  }
}
```

### 步骤 92：在服务中动态获取 API URL

将 `AppConfigService` 注入到 `CustomerService` 中，如下所示：

```
……
export class CustomerService {
……
   constructor(private appConfigService: AppConfigService,
               private httpClient: HttpClient) {
……
  }
……
```

### 步骤 93：使用动态 URL 进行 API 调用

接下来，按如下方式修改 `LoadCustomers` 方法：

```
……
   private LoadCustomers(): void{
     this.httpClient
     .get<Array<CustomerItemResponse>>(`${this.appConfigService.apiUrl}
/customers`)
     .pipe(
```





```
       map((customerAPIResponse) => {
         return customerAPIResponse.map(
           (customer) => new Customer(customer.firstName, customer.lastName)
        );
      })
     .subscribe((x) => {
       this.CustomersSubject.next(x);
    });
  }
……
```

如你所见，现在 API URL 不再是硬编码的了。

### 第 94 步：检查输出

在浏览器中检查输出。你看到的是一个空表格吗？当然，你看到了。😊

检查开发者工具。你会看到以下错误：

![](img/Image53143.jpg)

**图 20.2**

## 讨论 – 继续

**为什么会出现这个错误？**

如你所知，`AppConfigService` 的 `LoadConfig` 方法负责设置 `apiURL` 属性的值。令人惊讶的是，到目前为止我们还没有在任何地方调用过该方法。因此，`apiURL` 是 `undefined`。

**你知道我们到底想要什么吗？**

我们希望在进行任何外部 API 调用之前，`apiUrl` 属性能够被 `config.json` 文件中的值更新。

**我们该怎么做？**

我们必须在 Angular 将应用程序标记为已初始化之前调用 `LoadConfig` 方法。这样，我们就能 100% 确保在任何组件加载之前 `apiURL` 属性已经被更新。

简而言之，我们需要一个钩子来接入 Angular 的初始化过程，并编写我们自己的代码。

**这可行吗？**

在 Angular 中，我们有一个钩子可以接入 Angular 的引导过程。

我们可以配置一个函数，该函数会在应用程序启动时被注入，并在应用程序初始化期间执行。如果该函数返回一个 `promise`，那么初始化过程会一直等待，直到该 `promise` 被解决。

**如何将自定义逻辑钩入 Angular 的初始化过程？**

你注意到前面解释中提到的 *注入* 这个词了吗？如果没有注意到，请再读一遍。

Angular 暴露了一个类型为 `InjectionToken` 的 DI 令牌，名为 `APP_INITIALIZER`。

我们将函数提供给这个令牌，它就会自动被钩入 Angular 的初始化过程。

**如何将函数注入到 DI 令牌中？**

我们已经见过使用 `useClass` 创建提供者的例子。那是在我们想要提供 *类型* 作为值的时候。Angular 注入器会创建该类型的一个实例并注入它。

但除了 `useClass` 之外，还有更多方式：

*   `useFactory` – 这允许我们提供一个方法作为值。当我们想要手动控制对象的创建时使用。

    Angular 注入器每次想要进行注入时都会调用工厂方法。工厂方法始终期望返回一个对象。工厂方法返回的任何内容都将被注入到应用程序中。

*   `useValue` – 这允许我们注入一个静态值。值可以是任何标量值或对象。最适合注入常量值。

*   `useExisting` – 这是别名提供者。当我们想要用新的提供者替换旧的提供者时使用。

在我们当前的情况下，`useFactory` 非常合适。让我们看看它的实际应用。

## 实验 – 继续

### 第 95 步：创建 initializeConfig 方法

在 `Services` 文件夹中创建一个新文件 `app-initializer.ts`，并在其中创建一个名为 `initializeConfig` 的函数，如下所示：

```
export function initializeConfig() {
   return () => {
     return new Promise((resolve) => {
       setTimeout(() => {
         console.log('Testing');
         resolve();
      }, 3000);
    });
  };
}
```

请花点时间分析一下这段代码。

这是一个简单的函数，它返回另一个函数，而那个函数又返回一个 `promise`，最后，这个 `promise` 在 3 秒后被解决。

### 第 96 步：配置注入器以注入初始化函数

在 `AppModule` 中，按如下方式配置根注入器：

```
import {HttpClientModule, HTTP_INTERCEPTORS} from '@angular/common/http';
import {APP_INITIALIZER, NgModule} from '@angular/core';
……
import {initializeConfig} from './Services/app-initializer';
……
@NgModule({
   declarations: [AppComponent, CustomerComponent, LoginComponent],
   imports: [……],
   providers: 
     {provide: APP_INITIALIZER, useFactory: initializeConfig,multi:true},
     {provide: HTTP_INTERCEPTORS, useClass: TokenInterceptorService, multi:true}
……
```

### 第 97 步：检查输出

运行应用程序，你会注意到在 `CustomerComponent` 或 `LoginComponent` 显示之前有 3 秒的停顿。如果你还没有完全理解，那么将 3 秒的时间增加到更大的数字。你会发现，只有在 promise 被解决之后，应用程序才会被认为已初始化，也只有在那之后，组件才会被渲染。

### 第 98 步：从 AppConfigService 返回 promise

`AppConfigService` 中的 `loadConfig` 方法返回的是订阅对象，因为 observable 的 subscribe 方法返回的是订阅对象。让我们修改它，使其返回 promise 对象。

```
  loadConfig(): Promise<void> {
     return this.http
       .get<{apiUrl: string}>('./assets/config.json').toPromise()
       .then(config => {
         this.apiUrl = config.apiUrl;
      });
  }
```

### 第 99 步：将 AppConfigService 注入到 initializeConfig 方法中

通过将 `AppConfigService` 作为参数添加到方法中，将其注入到 `InitalizeConfig` 中。然后，在其中调用 `loadConfig` 方法，如下所示：

```
import {AppConfigService} from './app-config.service';
export function initializeConfig(appConfigService: AppConfigService) {
   return () => {
     return appConfigService.loadConfig();
  };
}
```

### 第 100 步：检查输出

再次，我们会得到一个“*白屏死机*”。

在开发者工具中，我们会发现以下错误：

![

**图 20.3**

## 讨论 – 继续

**前面到底发生了什么？**

Angular 按预期在初始化过程中调用了工厂函数，即 `initializeConfig`。

问题出在 `initializeConfig` 函数的参数上。

在前面的情况中，当 DI 系统在 Angular 中调用工厂方法时，没有传递任何参数，因此 `appConfigService` 是 `undefined`，导致了前面的错误。

**该怎么办？**

我们必须以某种方式告诉 Angular，我们的工厂函数依赖于 `AppConfigService`，这样在调用工厂函数之前，它会创建 `AppConfigService` 类的实例并传递给它，然后在调用时将其作为参数传递。简而言之，我们必须告诉 Angular 将 `AppConfigService` 类的实例注入到工厂函数中。

这可以通过使用 `deps` 来实现。

## 实验 – 继续

### 第 101 步：定义依赖

在 `AppModule` 中，定义 `APP_INITIALIZER` 的工厂函数时，设置 `deps` 属性以表明我们的工厂函数依赖于 `AppConfigService`。

```
……
   providers: [
     {provide: APP_INITIALIZER, useFactory: initializeConfig, multi: true, deps:[AppConfigService]},
……
  ],
   bootstrap: [AppComponent],
……
```

### 第 102 步：检查输出

最后，我们会看到表格显示了从服务器动态返回的客户数据。

## 讨论 – 继续

现在我知道，尽管得到了正确的输出，你仍然感觉不太舒服。

你一定在想，为什么在使用 `useFactory` 时必须显式地使用 `deps` 属性来指定依赖关系。而在使用 `useClass` 时，这是自动完成的。




答案是，对于 `useClass` 的情况，如果你还记得，我说过：“服务的每个消费者都必须用 `Injectable` 装饰器进行装饰。”这个 `Injectable` 装饰器为我们完成了自动化工作。它向 Service 类添加了元数据，指定了它所依赖的其他服务。

对于 `useFactory` 的情况，我们没有添加任何此类装饰器。因此，我们必须手动完成，为此，我们使用了 `deps`。

## 实验 – 续

**步骤 103：更改所有其他 API 调用**

通过前面的步骤，可以确认 `AppConfigService` 在 `LoadCustomers` 中按预期工作。接下来，让我们在 `CustomerService` 中实现 `Save` 方法，并在 `AuthenticateService` 中实现 `authenticate` 方法。

1.  `……` `//AuthenticationService`
2.  `authenticate(user: User): void {`
3.  `// 更改编号 3 - 订阅 Observable`
4.  `     this.httpClient`
5.  `       .post<AuthenticationResponse>(`
6.  ``         `${this.appConfigService.apiUrl}/signin`,user).subscribe(……``
7.  `……`
8.  `……` `//CustomerService`
9.  `Save(customer: Customer) {`
10.  `     const newCustomer: NewCustomer = new NewCustomer(`
11.  `       customer.FName,`
12.  `       customer.LName`
13.  `    );`
14.  `     this.httpClient`
15.  ``       .post(`${this.appConfigService.apiUrl}/customers`, newCustomer)``
16.  `       .subscribe(……`
17.  `……`

**步骤 104：检查输出**

执行、测试并确认保存和登录功能均正常工作。

**步骤 105：运行时配置**

我相信经过上述步骤，你对运行时配置已经清楚了，如果还不清楚，那么再演示一次后就会明白。使用 `ng build` 命令并带上 `--prod` 标志构建项目。像往常一样，它会在 dist 文件夹中创建应用程序构建，如下所示：

![](img/Image53300.jpg)

**图 20.4**

**步骤 106：更改配置并检查输出**

你会在 `dist\lab4-ng` 文件夹中找到一个名为 assets 的文件夹。它将是我们源代码中 assets 文件夹的副本。

你会在其中找到 `config.json` 文件。将 apiUrl 的值更改为 `http://localhost:5000`，这是我们的新服务器 URL。

之后，在 `lab4-ng` 文件夹内的命令提示符中执行 `lite-server` 命令，如下所示：

![](img/Image53308.jpg)

**图 20.5**

它将启动一个浏览器请求应用程序。你会看到屏幕上显示来自新服务器的客户数据。这就是运行时配置。任何配置更改都不需要重新编译或重新构建应用程序。

#### 总结

通过这个实验，我们终于到达了第 9 站。我希望你现在对运行时配置以及如何在 Angular 中实现它有了更清晰的认识。

这是所有旅程中最长的一段。好好休息一下，让自己睡个好觉。我们下一章见，届时我们将开始前往下一站的旅程。

在本章中，我们涵盖了以下主题：

*   我们了解到，位于 Angular 应用程序 SRC 文件夹中的 assets 文件夹会被复制到最终构建中。

*   我们了解到，我们可以通过使用 DI 令牌提供者 `APP_INITIALIZER` 配置根注入器，从而挂钩到 Angular 的初始化过程。

*   我们了解到，我们可以使用 `useFactory` 将一个方法作为值提供给 DI 令牌。

*   我们讨论了 observable 类的 `toPromise` 方法，它可以从 observable 创建一个 promise。

*   我们了解到，在创建提供者时，使用 `deps` 属性，我们可以指定当前提供者的依赖项。在使用 `useFactory` 时，必须显式定义依赖项。

*   我们了解到，对于 `useClass` 的情况，我们不需要显式指定依赖服务，因为 `Injectable` 装饰器会为我们完成这项工作。这就是为什么我们必须为每个服务类附加一个 `Injectable` 装饰器，无论为其配置了哪个注入器。

## 第 21 章

## 错误处理

## 引言

在本章中，我们将开始前往第 10 站的旅程，到这一站结束时，你将了解 Angular 中运行时错误处理的所有内容。

在深入实验之前，让我们先了解 Angular 应用程序可能出现的不同类型的运行时异常：

1.  **客户端错误**：客户端逻辑中未处理的运行时错误。

2.  **服务器端错误**：可以进一步分为以下三类：

    *   未处理的运行时错误

    *   来自服务器的未授权错误

    *   服务器未连接错误 – 当尝试进行 HTTP 调用但服务器不可用时

在本章中，我们将学习如何处理所有这四种错误。

## 实验 – Angular 中的错误处理

**步骤 1：重命名应用程序**

开始将应用程序从 lab4-NG 重命名为 lab5-NG。

**步骤 2：获取新服务器**

接下来，从 GitHub 下载 lab5 服务器，并使用 `node server.js` 命令执行它。

这个新服务器暴露了一个用于测试服务器端错误的新端点。

**步骤 3：创建一个用于测试错误的组件**

如果我们要处理错误，那么首先需要错误。因此，让我们在 app 文件夹内创建一个 `ErrorTest` 文件夹，然后在其内部创建一个新的组件 `ErrorTesComponent`，如下所示：

1.  `import {component} from ‘@angular/core’;`
2.  
3.  `@Component({`
4.  `   selector: ‘error-test’,`
5.  `   templateUrl: ‘./error-test.component.html’`
6.  `})`
7.  `export class ErrorTestComponent {`
8.  `}`

1.  `<h1>测试错误</h1>`
2.  `<input type=”button” value=”客户端错误” (click)=”throwClientError()”>`
3.  `<input type=”button” value=”服务器端错误” (click)=”throwServerError()”>`
4.  `<input type=”button” value=”未授权错误”`
5.  `(click)=”throwUnAuthorizedError()”>`

如你所见，我们有三个按钮——每个按钮对应最初讨论的一种错误类型。

**步骤 4：将组件添加到模块**

Angular 中的每个组件都必须属于一个 Angular 模块。让我们将 `ErrorTestComponent` 添加到 `AppModule` 中。

1.  `……`
2.  `import {ErrorTestComponent} from ‘./ErrorTest/error-test.component’;`
3.  `……`
4.  `@NgModule({`
5.  `   declarations: [AppComponent, LoginComponent, CustomerComponent, ErrorTestComponent],`
6.  `   imports: [`
7.  `     BrowserModule,`
8.  `……`
9.  `})`
10.  `export class AppModule {}`

**步骤 5：更新路由**

接下来，打开 `app.routes.ts` 并更新路由以访问上述组件。

1.  `……`
2.  `import {ErrorTestComponent} from ‘../ErrorTest/error-test.component’;`
3.  `……`
4.  `export const AppRoutes: Routes = [`
5.  `   {path: ‘login’, component: LoginComponent},`
6.  `   {path: ‘customer’, component: CustomerComponent, canActivate: [AuthGuard]},`
7.  `   {path: ‘error-test’, component: ErrorTestComponent},`
8.  `……`
9.  `];`

**步骤 6：准备客户端逻辑错误**

接下来，在 `ErrorTestComponent` 中定义 `throwClientError`，如下所示：

1.  `throwClientError() {`
2.  `    throw new Error(‘测试客户端错误 !!!’);`
3.  `}`

**步骤 7：准备服务器端逻辑错误**

接下来，在 `ErrorTestComponent` 中定义 `throwServerError`，如下所示：

1.  `   constructor(private appConfigService: AppConfigService,`
2.  `               private httpClient: HttpClient) {`
3.  `  }`
4.  `……`
5.  `   throwServerError(){`
6.  ``     this.httpClient.get(`${this.appConfigService.apiUrl}/getError`).subscribe();``
7.  `}`

如你在上述代码中所见，我们正在发起一个 API 调用，该调用将在服务器端抛出一个运行时错误。

**步骤 8：准备未授权错误**

在 `ErrorTestComponent` 中定义 `throwUnAuthorizedError`，如下所示：

1.  `   throwUnAuthorizedError(){`




```
this.httpClient.get(`${this.appConfigService.apiUrl}/authTest`).
subscribe();
}
```

从技术上讲，上述代码也在进行 API 调用，但用户必须先通过此 API 的身份验证。

### 第 9 步：检查输出

在进入实际工作之前，最好确认一切操作正确无误。

使用 `ng serve --open` 命令运行 Angular 应用程序，然后在浏览器地址栏中显式输入 `ErrorTestComponent` 的 URL，确认生成了预期的输出。

![](img/Image53412.jpg)

**图 21.1**

然后，点击前两个按钮，确保它们会抛出运行时错误。

![](img/Image53448.jpg)

**图 21.2**

![](img/Image53481.jpg)

**图 21.3**

至此，我们确认了演示已针对客户端运行时错误和服务器端运行时错误设置完毕。

第三个按钮让我们确认演示已针对未授权访问错误设置完毕。为此，首先确保您未登录。要确保这一点，请转到登录页面，完成登录，然后注销。当您回到登录屏幕后，通过显式更改 URL 导航到 `ErrorTestComponent`。然后，点击第三个按钮。

现在，为了测试第四种错误类型，您必须停止 node 服务器。为此，切换到命令提示符（当前正在执行 node 服务器的那一个），然后按 Ctrl+C。

![](img/Image53489.jpg)

**图 21.4**

完成后，点击第二个或第三个按钮中的任意一个，查看错误实际发生的情况。

![](img/Image53607.jpg)

**图 21.5**

## 讨论 – 续

至此，我们已经准备好了组件，它将抛出错误并帮助测试错误处理逻辑。

接下来，让我们决定当系统中遇到意外错误时我们想要做什么：

*   对于意外的运行时错误（客户端和服务器端），最常用的方法包括以下两个步骤：

    1.  将用户重定向到某个自定义页面。

    2.  将错误持久化（记录）到某种存储介质中，以便日后检查以进行故障排除。

*   对于未授权错误，首选方法是重定向到登录屏幕。

*   对于因服务器不可用而产生的故障，首选方法是显示一些自定义消息。

所以，现在我们知道了每种错误应该如何处理。

## 实验 – 续

### 第 10 步：创建自定义错误组件

在 app 文件夹中创建一个名为 *Error* 的新文件夹，然后创建一个名为 `ErrorComponent` 的组件，如下所示：

```
import {Component} from ‘@angular/core’;

@Component({
   selector: ‘app-error’,
   templateUrl: ‘./error.component.html’
})

export class ErrorComponent {
   constructor() {}
}
```

```
<h1>500</h1>
<h2>Unexpected Error <b>:(</b></h2>
<div class=”gears”>
   <div class=”gear one”>
     <div class=”bar”></div>
     <div class=”bar”></div>
     <div class=”bar”></div>
   </div>
   <div class=”gear two”>
     <div class=”bar”></div>
     <div class=”bar”></div>
     <div class=”bar”></div>
   </div>
   <div class=”gear three”>
     <div class=”bar”></div>
     <div class=”bar”></div>
     <div class=”bar”></div>
   </div>
</div>
```

### 第 11 步：将 ErrorComponent 添加到模块

我想你现在已经知道怎么做了。

```
……
import {ErrorComponent} from ‘./Error/error.component’;
……
@NgModule({
   declarations: [AppComponent, LoginComponent,
     CustomerComponent,ErrorTestComponent,ErrorComponent],
………
export class AppModule {}
```

### 第 12 步：创建组件 CSS

像往常一样，我们创建了一个组件类（也称为视图类）和一个模板（也称为视图）。两者共同构成了一个 Angular 组件。

这次我们需要再添加一个内容——组件 CSS。我们可以创建并附加一个 CSS 到组件中，使其成为该组件的一部分。让我们尝试一下。

创建一个 CSS 文件 `error.component.css`，并将其附加到组件中，如下所示：

```
body {
     background: #eaeaea;
  }
   h1 {
     margin: 100px auto 0 auto;
     color: black;
     font-family: ‘Encode Sans Semi Condensed’, Verdana, sans-serif;
     font-size: 10rem; line-height: 10rem;
     font-weight: 200;
     text-align: center;
  }
   h2 {
     margin: 20px auto 30px auto;
     font-family: ‘Encode Sans Semi Condensed’, Verdana, sans-serif;
     font-size: 1.5rem;
     font-weight: 200;
     text-align: center;
  }
   h1, h2 {
-webkit-transition: opacity 0.5s linear, margin-top 0.5s linear; /* Safari */
     transition: opacity 0.5s linear, margin-top 0.5s linear;
  }
   .loading h1, .loading h2 {
     margin-top: 0px;
     opacity: 0;
  }
   .gears {
     position: relative;
     margin: 0 auto;
     width: auto; height: 0;
  }
   .gear {
     position: relative;
     z-index: 0;
     width: 120px; height: 120px;
     margin: 0 auto;
     border-radius: 50%;
     background: black;
  }
   .gear:before{
     position: absolute; left: 5px; top: 5px; right: 5px; bottom: 5px;
     z-index: 2;
     content: “”;
     border-radius: 50%;
     background:#eaeaea;
  }
   .gear:after {
     position: absolute; left: 25px; top: 25px;
     z-index: 3;
     content: “”;
     width: 70px; height: 70px;
     border-radius: 50%;
     border: 5px solid black;
     box-sizing: border-box;
     background: #eaeaea;
  }
   .gear.one {
     left: -130px;
  }
   .gear.two {
     top: -75px;
  }
   .gear.three {
     top: -235px;
     left: 130px;
  }
   .gear .bar {
     position: absolute; left: -15px; top: 50%;
     z-index: 0;
     width: 150px; height: 30px;
     margin-top: -15px;
     border-radius: 5px;
     background: black;
  }
   .gear .bar:before {
     position: absolute; left: 5px; top: 5px; right: 5px; bottom: 5px;
     z-index: 1;
     content: “”;
     border-radius: 2px;
     background: #eaeaea;
  }
   .gear .bar:nth-child(2) {
     transform: rotate(60deg);
     -webkit-transform: rotate(60deg);
  }
   .gear .bar:nth-child(3) {
     transform: rotate(120deg);
     -webkit-transform: rotate(120deg);
  }
   @-webkit-keyframes clockwise {
     0% {-webkit-transform: rotate(0deg);}
     100% {-webkit-transform: rotate(360deg);}
  }
   @-webkit-keyframes anticlockwise {
     0% {-webkit-transform: rotate(360deg);}
     100% {-webkit-transform: rotate(0deg);}
  }
   @-webkit-keyframes clockwiseError {
     0% {-webkit-transform: rotate(0deg);}
     20% {-webkit-transform: rotate(30deg);}
     40% {-webkit-transform: rotate(25deg);}
     60% {-webkit-transform: rotate(30deg);}
     100% {-webkit-transform: rotate(0deg);}
  }
   @-webkit-keyframes anticlockwiseErrorStop {
     0% {-webkit-transform: rotate(0deg);}
     20% {-webkit-transform: rotate(-30deg);}
     60% {-webkit-transform: rotate(-30deg);}
     100% {-webkit-transform: rotate(0deg);}
  }
   @-webkit-keyframes anticlockwiseError {
```





```
112.      0% {-webkit-transform: rotate(0deg);}
113.      20% {-webkit-transform: rotate(-30deg);}
114.      40% {-webkit-transform: rotate(-25deg);}
115.      60% {-webkit-transform: rotate(-30deg);}
116.      100% {-webkit-transform: rotate(0deg);}
117.    }
118.     .gear.one {
119.       -webkit-animation: anticlockwiseErrorStop 2s linear infinite;
120.    }
121.     .gear.two {
122.       -webkit-animation: anticlockwiseError 2s linear infinite;
123.    }
124.     .gear.three {
125.       -webkit-animation: clockwiseError 2s linear infinite;
126.    }
127.     .loading .gear.one, .loading .gear.three {
128.       -webkit-animation: clockwise 3s linear infinite;
129.    }
130.     .loading .gear.two {
131.       -webkit-animation: anticlockwise 3s linear infinite;
132.    }
```

（现在，如果你对前面的 CSS 有任何理解困难，请忽略它。让我们专注于 Angular。）

为了将这个样式表文件附加到组件上，我们将使用 Component 装饰器的 `styleUrls` 属性。

```
1.  @Component({
2.     selector: ‘app-error’,
3.     templateUrl: ‘./error.component.html’,
4.     styleUrls:[‘./error.component.css’]
5.  })
6.  })
7.  export class ErrorComponent {
```

## 讨论 – 继续

你一定在想，将 CSS 文件附加到组件有什么特别之处。

我们有一个单独的第 28 章 – Angular 样式，在那里我们会详细讨论。

**步骤 13：更新路由**

接下来，打开 `app.routes.ts` 并更新路由以访问上述组件。

```
1.  ……
2.  import {ErrorComponent} from ‘../Error/error.component’;
3.  import {ErrorTestComponent} from ‘../ErrorTest/error-test.component’;
4.  ……
6.  export const AppRoutes: Routes = [
7.     {path: ‘login’, component: LoginComponent},
8.     {path: ‘customer’, component: CustomerComponent, canActivate: [AuthGuard]},
9.     {path: ‘error-test’, component: ErrorTestComponent},
10.     {path: ‘error’, component: ErrorComponent},
11.  ……
```

**步骤 14：检查输出**

让我们测试我们的错误组件。执行应用程序，输入 `ErrorComponent` 的 URL，并确认显示以下输出：

![](img/Image53621.jpg)

**图 21.6**

## 讨论 – 继续

现在所有要素都已准备就绪，是时候学习如何处理错误了。

幸运的是，Angular 已经内置了集中式异常处理。默认实现会将错误消息打印到控制台。

可以通过使用自定义 Angular 服务并将其作为新的错误处理器注入到 Angular 管道中来覆盖默认行为。让我们来做同样的事情。

## 实验 – 继续

**步骤 15：创建自定义错误处理器**

在 `Services` 文件夹中创建一个新文件 `app-error-handler.service.ts`，内容如下：

```
1.  import {HttpErrorResponse, HttpResponseBase} from ‘@angular/common/http’;
2.  import {ErrorHandler, Injectable, NgZone} from ‘@angular/core’;
3.  import {Router} from ‘@angular/router’;
5.  @Injectable()
6.  export class AppErrorsHandler implements ErrorHandler {
7.     constructor(
8.       private router: Router,
9.       private zone:NgZone
10.    ) {}
12.     handleError(error: Error | HttpErrorResponse) {
13.       if (error instanceof HttpResponseBase) {
14.  this.HandleServerSideError(error); // 表示这是一个服务器端错误
15.      } else {
16.  this.HandleClientSideError(error); // 表示这是一个客户端错误
17.      }
18.    }
20.     private HandleServerSideError(error: HttpErrorResponse) {
21.       if (error.status === 0) {
22.         alert(‘服务器未运行’);
23.      } else if (error.status === 401) {
24.         this.zone.run(() => this.router.navigate([‘/login’]));
25.      } else {
26.         localStorage.error = error.message;
27.         this.zone.run(() => this.router.navigate([‘/error’]));
28.      }
29.    }
30.     private HandleClientSideError(error: Error) {
31.       localStorage.error = error.message;
32.       this.zone.run(() => this.router.navigate([‘/error’]));
33.    }
34.  }
```

## 讨论 – 继续

让我们理解一下上面的代码。

你首先注意到的肯定是 `ErrorHandler` 接口。要创建自定义错误处理器，我们必须让我们的类实现 `ErrorHandler` 接口，并定义 `handleError` 方法。

`handleError` 方法不言自明。你可以看到 if…else 条件。在讨论的四种错误中，有三种在 if 块中处理，而剩下的一种在 else 块中处理。

**注意**：在当前情况下，我们只将最新的错误存储在本地存储中。在实际场景中，你可能会采用更持久的介质，例如数据库，并保留所有错误。

**zone**

我敢肯定，上面代码中的 `zone.run` 一定引起了你的注意。

我们将 `router.navigate` 封装在了 `zone.run` 调用内部。

为了理解这一点，请看下面的代码：

![](img/Image53790.jpg)

**图 21.7**

上面的代码是 Angular 原始源代码的一部分。当 Angular 应用程序抛出未处理的异常时，会执行 `onHandleError`。

Angular 作为对错误的响应，会调用 `zone.runOutsideAngular` 方法。

**zone.runOutsideAngular**

在 Angular 中，zone 为应用程序提供了执行上下文。

`zone.runOutsideAngular` 使代码在 Angular 的执行上下文之外执行，这样变更检测就不会触发。如果你还记得，我们之前曾讨论过变更检测。我们说过它负责更新 UI，而没有变更检测就意味着没有 UI 更新。

有时，为了控制 Angular 应用程序的性能，我们会有意将某些代码放在 Angular 的执行上下文之外执行。这可以通过 `runOutsideAngular` 方法来实现。

默认情况下，Angular 只关心在控制台中显示异常详情，而不关心 UI 更新。因此，在集中式错误处理器中，它使用 `runOutsideAngular` 方法来执行代码。

**zone.run**

当你处于 Angular 的执行上下文之外时，可以使用 `zone.run` 方法重新进入执行区域。

上面的代码表明错误处理器在 Angular 上下文之外执行。因此，我们使用了 `zone.run` 方法，以便我们的 `router.navigate` 方法在应用程序的原始执行上下文中执行，从而我们看到更新后的 UI。

不必过于纠结于理解上述理论，因为我们在实际中很少使用 `runOutsideAngular`。

我的建议是，不要强行在你的项目中使用 `runOutsideAngular` 方法。

当需要时，你自然会意识到它；其次，一旦你使用了它，你可能需要使用 `run` 方法回到原始世界。

## 实验 – 继续

**步骤 16：配置注入器**

上一步将是用我们的自定义错误处理器配置根注入器。打开 `app.module.ts` 文件，并将代码修改为以下内容：

```
1.  import {HttpClientModule, HTTP_INTERCEPTORS} from ‘@angular/common/http’;
2.  import {APP_INITIALIZER, ErrorHandler, NgModule} from ‘@angular/core’;
3.  import {FormsModule, ReactiveFormsModule} from ‘@angular/forms’;
4.  import {BrowserModule} from ‘@angular/platform-browser’;
5.  import {RouterModule} from ‘@angular/router’;
6.  ……
7.  import {AppErrorsHandler} from ‘./Services/app-error-handler.service’;
8.  ……
9.  @NgModule({
10.  ……
11.     providers: [
12.       {provide: APP_INITIALIZER, useFactory: initializeConfig, multi: true, deps:[AppConfigService]},
13.       {provide: HTTP_INTERCEPTORS, useClass: TokenInterceptorService, multi: true},
```





```
{provide:ErrorHandler, useClass:AppErrorsHandler},
……
})
export class AppModule {}
```

## 讨论 – 续

在上述代码中，你可以看到我们使用 `NgModule` 装饰器而不是 `Injectable` 装饰器来配置根注入器。在这种情况下不能使用 `Injectable` 装饰器，因为它不允许我们显式指定 DI 令牌。为了用自定义错误处理器替换错误处理器，我们需要显式提供一个 DI 令牌（`ErrorHandler`）。

## 步骤 17：检查输出

执行应用程序，确保针对四种错误都生成了期望的输出。

**客户端运行时错误**

![](img/Image53797.jpg)

**图 21.8**

**服务器端运行时错误**

![](img/Image53845.jpg)

**图 21.9**

**用户未授权时的服务器端错误**

![](img/Image53879.jpg)

**图 21.10**

**服务器未运行时的服务器端错误**

![](img/Image53914.jpg)

**图 21.11**

#### 总结

至此，我们已经到达了第 10 站。在这一旅程中，我们涵盖了以下主题：

*   我们了解到可以为组件附加组件特定的样式。为此，我们将使用 `Component` 装饰器的 `styleUrls` 参数。

*   我们了解到 Angular 已经内置了集中式异常处理。默认实现会将错误消息打印到控制台。

*   我们了解到可以通过自定义 Angular 服务并将其作为新的错误处理器注入到 Angular 管道中来覆盖默认行为。为此，我们必须为 DI 令牌 `ErrorHandler` 配置根注入器。

*   我们了解到要实现自定义错误处理器服务，必须实现 `ErrorHandler` 接口。

*   我们了解了 `zone.runOutsideAngular` 方法，它允许我们在 Angular 执行上下文之外执行代码。

*   我们了解了 `zone.run` 方法，它允许我们回到 Angular 执行上下文。

## 第 5 节

#### 总结

在第 5 节中，我们详细探讨了 Angular 服务，并涵盖了第 9 站和第 10 站，这完成了我们旅程的一半。让我们回顾一下本节中的每一章。

#### 第 12 章 – 认证服务

*   我们再次复习了 DI 概念，并了解到它使我们的代码松散耦合，从而更易于维护和测试。

*   我们讨论了 Angular 注入器，它负责将服务实例注入到 Angular 应用程序中。

*   我们讨论了两种注入器：模块注入器和元素注入器。

*   我们了解到这两种注入器都维护着一个层级结构。

*   我们学习了如何使用 `Injectable` 装饰器和 `Component` 装饰器配置服务。

*   我们了解到 `NgModule` 和 `Injectable` 装饰器都可以配置模块注入器，而 `Component` 装饰器则配置元素注入器。

*   我们了解到，对于依赖于其他服务的每个 Angular 服务，无论配置了哪个注入器，都必须添加 `Injectable` 装饰器。

*   我们了解到根注入器会创建一个全局单例实例，而元素注入器则会创建特定于组件实例（及其子组件）的实例。

*   我们讨论了当 `provide` 和 `useClass` 具有相同值时配置注入器的简写语法。

*   我们了解了响应式编程，并借助 RxJS 在 Angular 中实现它。

*   我们了解到在响应式编程中，`Observable` 由 `Subscriber` 订阅，而 `Observer` 将数据馈送到 `Observable` 中。

*   我们演示了 RxJS 的 `Subject`，它在响应式编程中同时代表 `Observable` 和 `Observer`。

*   我们了解到在实际项目中，RxJS 的 subject 会被标记为私有，而底层的 observable 会作为公共成员暴露。

#### 第 13 章 – 取消订阅

*   我们了解到取消订阅非常重要，否则会导致内存泄漏。

*   我们学习了如何取消订阅 RxJS 订阅。

*   我们了解了 Angular 组件的 `ngOnDestroy` 生命周期事件。

*   我们简要讨论了 Angular 管道。它用于封装 Angular 中的转换逻辑（有专门的一章介绍）。

*   最后，我们讨论了 async 管道。

#### 第 14 章 – 登出和路由守卫清理

*   我们了解了通过将现有代码移动到服务中来编写服务逻辑的重要性。

*   在本章中，我们再次复习了元素注入器和模块注入器。由于元素注入器无法满足我们的需求，我们切换到了模块注入器。

*   我们了解到 `AppComponent` 的元素注入器会间接创建一个全局单例实例，因为它作为根组件永远不会被销毁。其次，作为根组件，它创建的服务实例对所有子组件都是可访问的。

*   我们了解到，对于配置根注入器，`Injectable` 装饰器比 `NgModule` 装饰器更受青睐，因为 `Injectable` 装饰器可以实现摇树优化。摇树优化是 Angular 构建过程中的一个步骤，确保所有未使用的服务从最终打包文件中移除。

*   我们了解到可以在 Angular 中利用 HTML 的功能，例如使用 HTML 的 `autofocus` 属性、`form` 标签和提交按钮。

#### 第 15 章 – 客户服务

*   我们学习了如何使用 RxJS 的 `of` 操作符创建自定义 observable。

*   我们再次演示了如何配置元素注入器。

*   我们复习了 Angular 中的 RxJS `Subject`。

*   我们学习了 Angular 中的 RxJS `BehaviorSubject`。

*   我们学习了一种新的故障排除/调试 Angular 应用程序的方法，即在开发者工具中使用 Angular 暴露的 `ng` 对象。

*   我们看到了 `async as` 的实际应用。

*   我们看到了 `*ngIf with else` 的实际应用。

*   我们讨论了从服务中发出引用类型时面临的挑战。

#### 第 16 章 – HTTP 服务

*   我们在应用程序中再次使用了 `HttpClient` 服务。

*   我们使用了 `HttpClient.get` 和 `post` 方法的泛型版本。

*   我们再次演示了 `Subject`。

*   我们讨论了基于令牌的身份验证，并在应用程序中实现了它。

*   我们讨论了 `json` 管道。使用此管道，我们可以通过插值显示对象的内容。它们仅用于故障排除。

*   我们了解到，当涉及多个管道时，顺序至关重要。

*   我们演示了使用匿名对象作为泛型参数。虽然不推荐，但在项目中可能会看到。

*   我们了解到，我们使用 `subscribe` 方法来获取发出的值，并使用 `pipe` 方法将值通过各个操作符进行管道传输，这些操作符可能会改变值甚至停止进一步发出。

*   我们讨论了 RxJS 中的 `map` 操作符。使用它，我们可以将实际的 HTTP 响应转换为所需的响应。

#### 第 17 章 – 令牌拦截器

*   在本章中，我们学习了如何创建和配置 HTTP 拦截器。

*   我们讨论了 `HttpInterceptor` 接口，创建拦截器时需要实现该接口。

*   我们了解到不能在拦截器中直接修改 HTTP 请求，因为它们是不可变的。因此，我们需要克隆现有请求。我们将头部附加到克隆的请求上，然后将该克隆的请求传递到管道中。

*   我们演示了配置注入器时的长语法和短语法。





*   我们了解到，需要显式指定 DI 令牌——`HTTP_INTERCEPTORS`，以便为 HTTP 拦截器配置注入器。
*   我们了解到，尽管由于摇树优化的考虑，推荐使用可注入装饰器，但我们不能一直用它来配置模块注入器，因为它不允许我们显式指定 DI 令牌。
*   我们还了解到使用 `NgModule` 装饰器配置注入器的好处。与可注入装饰器相比，它提供了更多的配置选项。
*   我们了解到，注入器需要为 HTTP 拦截器配置多提供者。

## 第 18 章 – 多提供者

*   在本章中，我们了解到可以为单个 DI 令牌定义多个提供者。这被称为多提供者。
*   我们了解到，如果为单个 DI 令牌定义了多个常规提供者，那么一个提供者将根据顺序替换另一个。
*   我们了解到，如果为单个 DI 令牌定义了多个多提供者，那么注入器将注入一个服务数组。
*   我们了解到，在定义提供者时，DI 令牌和实际服务不要求兼容。它们可以具有完全不同的结构。
*   我们了解到，不能为单个 DI 令牌同时定义常规提供者和多提供者。对于单个 DI 令牌，要么所有提供者都是常规的，要么所有提供者都是多提供者。
*   我们了解到，建议使用字符串或 InjectionToken 与多提供者一起作为 DI 令牌，而不是使用类型令牌。
*   我们了解了 `Inject` 装饰器，它允许我们手动告诉 Angular 该参数必须被注入。它将在使用字符串和 InjectionToken 时使用。
*   我们了解到，在创建可复用服务时，多提供者有时非常有用。

## 第 19 章 – 编译时配置

*   本章开始时，我们理解了应用程序中配置的必要性。
*   我们了解了编译时配置和运行时配置之间的区别。编译时配置意味着配置将在编译时完成，而运行时配置意味着它将在部署时完成。
*   我们了解了 `environment.ts` 文件，以及它如何在生产模式下被 `environment.prod.ts` 文件替换。
*   我们分别使用 `ng build` 和 `ng build --prod` 命令生成了 Angular 应用程序的非生产模式和生产模式构建。
*   我们了解到，在非生产构建中，Angular CLI 还会生成源映射文件；因此，我们可以在运行时直接调试 TypeScript 文件。
*   我们了解到，在生产构建中不会得到单独的 `vendor.js` 文件，因为它已集成到主包中。
*   我们演示了一个名为 `lite-module` 的 Angular 模块，它可以用作静态文件的开发用途 Web 服务器。

## 第 20 章 – 运行时配置

*   我们了解到，位于 Angular 应用程序 SRC 文件夹中的 assets 文件夹将被复制到最终构建中。
*   我们了解到，可以通过使用 DI 令牌提供者 `APP_INITIALIZER` 配置根注入器，来挂钩 Angular 的初始化过程。
*   我们了解到，可以使用 `useFactory` 将一个方法作为值提供给 DI 令牌。
*   我们讨论了 observable 类的 `toPromise` 方法，它可以从 observable 创建一个 promise。
*   我们了解到，在创建提供者时，使用 `deps` 属性可以指定当前提供者的依赖项。在使用 `useFactory` 时，必须显式定义依赖项。
*   我们了解到，在使用 `useClass` 的情况下，不需要显式指定依赖服务，因为可注入装饰器会为我们完成这项工作。这就是为什么我们必须为每个服务类附加一个可注入装饰器，无论为其配置了哪个注入器。

## 第 21 章 – 错误处理

本章是第 5 部分的最后一章，因此让我们到达了第 10 站。

*   我们详细讨论了 Angular 中的错误处理。
*   我们了解到，可以为组件附加组件特定的样式。为此，我们将使用 Component 装饰器的 `styleUrls` 参数。
*   我们了解到 Angular 已经内置了集中式异常处理。默认实现将错误消息打印到控制台。
*   我们了解到，可以使用自定义 Angular 服务并将其作为新的错误处理程序注入到 Angular 管道中，从而覆盖默认行为。为此，我们必须为 DI 令牌 `ErrorHandler` 配置根注入器。
*   我们了解到，要创建自定义错误处理程序服务，必须实现 `ErrorHandler` 接口。
*   我们了解了 `zone.runOutsideAngular` 方法，它允许我们在 Angular 执行上下文之外执行代码。
*   我们了解了 `zone.run` 方法，它允许我们返回到 Angular 的执行上下文。

# 第 6 部分

## 第 22 章

## 组件导向风格实战

## 引言

本章将非常精彩。我们将接手之前的项目，并通过实际遵循组件导向风格来改进它。通过本章，你将完成前往第 11 站的旅程。

### 组件导向风格

**组件导向风格**是一种 UI 设计方法，它允许我们将 UI 创建为可复用和可组合的 Web 组件的集合。

看看下面的 UI。当你看到它时，你会想到什么？

![](img/Image54019.jpg)

**图 22.1**

这难道不正是两个标签、两个文本框和两个按钮的组合吗？

这些标签、文本框和按钮到底是什么？它们是**组件**。

现在，看看下面这个。你看到了什么？

![](img/Image54071.jpg)

**图 22.2**

你可能会说——下拉菜单。

我不否认。它确实是一个下拉菜单。

*   但它也可以被视为一个文本框、一个按钮和一个显示多个项目的动态框的组合。
*   按钮通过一些 CSS 放置，使其看起来像是文本框的一部分。
*   当点击该按钮时，会执行一些代码，使动态框在运行时出现，显示几个列表项。当点击这些列表项时，它们会显示在文本框中。

我的意思是，下拉菜单是一个组件，但它是由其他更小的元素（或者更准确地说是组件）组合而成的。

基于我们到目前为止完成的实验，我相信现在你应该对组件有了清晰的概念。

组件代表整个 UI 的一部分。我们将这些组件组合在一起，形成一个巨大的组件，并持续这样做，直到整个 UI 完成。

到目前为止，在我们的应用程序中，我们已经看到了一些组件的实际应用，例如 `LoginComponent`、`CustomerComponent`、`ErrorComponent` 和 `ErrorTestComponent` 等。

### 组件导向风格与 Angular

你可能会惊讶地发现，Angular 并没有首创组件导向风格。

你可以看到其他 UI 技术（如 Polymer、ReactJS 等）也采用了类似的方法。

这是随着 HTML5 的出现而引入的一种标准方法/实践。

这种方法使我们的代码维护变得容易，并允许多个 UI 开发人员并行工作。

### 当前应用程序中的一个问题

你认为我们在迄今为止开发的当前项目中真正遵循了组件导向风格吗？

嗯，部分是的，部分不是。




我们将应用程序分解为多个组件，每个组件都有其角色——`Login`、`Customer`、`ErrorTest` 和 `Error`。

这些顶层组件将根据项目的功能进行识别。这类组件被称为**功能组件**。

更多的功能会引入更多的组件，这些组件主要通过路由进行访问。

一旦确定了一个功能组件并准备开发，下一步就是确定每个功能组件的设计方式。创建一个庞大的功能组件并不是一个好主意，因为它会使代码变得**不可读**且**难以管理**。我们应该将其分解为多个更小的组件。

在我们的示例中，`CustomerComponent` 应该被分解为多个更小的组件。我们还没有这样做，这就是问题所在。

# 容器-展示模式

在分解功能组件时，容器-展示模式被广泛使用并证明有效。

在这种方法中，我们将功能组件分解为多个组件。其中一个称为容器组件，其他的称为展示组件。

有些人对此有不同的称呼。

**容器组件**被称为**智能**组件。它们将与外部 API 交互以检索和更新数据。它们负责应用程序状态的变化。

**展示组件**被认为是**哑**组件。它们只负责处理一种功能。它们将处理整个功能组件逻辑的一部分。

它们将依赖容器组件与外部世界进行任何交互，例如与外部 API 交互、更新应用程序状态等。

在下一个演示之后，您将很好地理解这一点。

# 实验室 – 升级项目以遵循容器-展示模式

为了实现这一点，我们必须引入两个新的组件——`CustomerList` 和 `CustomerAdd`。

*   一个将处理列表，另一个将处理数据输入部分。
*   这两个组件都将封装在 `CustomerComponent` 内部。
*   `CustomerComponent` 将处理 `CustomerService`。

**步骤 1 – 设置实验室 6**

获取源代码 `lab-5` 并将其重命名为 `lab-6`。

**步骤 2 – 创建 CustomerListComponent**

在 `Customer` 文件夹中创建一个新的 Angular 组件 `CustomerListComponent`，如下所示：

```
import {Component} from '@angular/core';
@Component({
   selector: 'customer-list',
   templateUrl: './customer-list.component.html'
})
export class CustomerListComponent {
}
```

**步骤 3 – 创建 CustomerAddComponent**

接下来，创建 `CustomerAddComponent`，如下所示：

```
import {Component} from '@angular/core';
@Component({
   selector: 'customer-add',
   templateUrl: './customer-add.component.html'
})
export class CustomerAddComponent {}
```

**步骤 4 – 将两个组件添加到 AppModule**

打开 `app.module.ts`，并将这两个组件添加到 `AppModule` 的声明部分。

```
……
import {CustomerAddComponent} from './Customer/customer-add.component';
import {CustomerListComponent} from './Customer/customer-list.component';
……
@NgModule({
   declarations: [AppComponent, LoginComponent,CustomerComponent, ErrorTestComponent, ErrorComponent, CustomerAddComponent,CustomerListComponent],
  ……
)
export class AppModule {}
```

## 讨论 – 继续

所以现在，我们有三个与客户相关的组件——`CustomerComponent`、`CustomerListComponent` 和 `CustomerAddComponent`。

在第一部分中，让我们为新组件准备模板文件。

# 实验室 – 继续

**步骤 5 – 准备 CustomerList 模板**

`CustomerListComponent` 将负责组件的列表部分。

因此，让我们从 `CustomerComponent` 中取出列表部分的 HTML，并将其放入 `CustomerListComponent` 中。（暂时不要对 `CustomerComponent` 做任何更改。我们稍后会处理那部分。现在，只需将内容复制到 `CustomerList` 中。）

```
<div class="card">
   <h5 class="card-header">Customer List</h5>
   <div class="card-body">
     <div class="card-title">
       <i class="fas fa-user-plus"></i>
       <input type="button" value="+ Add New"
       class="btn btn-primary fas fa-coffee fa-xs" (click)="AddNew()">
     </div>
     <table class="table table-striped table-bordered">
       <thead class="thead-dark">
         <tr>
           <th scope="col">First Name</th><th scope="col">Last Name</th>
         </tr>
       </thead>
       <tbody>
         <tr *ngFor="let item of (Customers$|async)">
           <td scope="row">{{item.FName}}</td><td>{{item.LName}}</td>
         </tr>
       </tbody>
     </table>
   </div>
</div>
```

**步骤 6 – 准备 CustomerListComponent 的视图类**

`CustomerListComponent` 需要两样东西——`Customers$` 变量和 `AddNew` 方法。

让我们添加它们。

```
……
export class CustomerListComponent {
   Customers$: Observable<Array<Customer>>;
   AddNew() {
  }
}
```

**步骤 7 – 准备 CustomerAddComponent 模板**

从 `CustomerComponent` 中取出整个数据输入部分，并将其放入 `CustomerAddComponent` 中，如下所示：

```
<div class="card" ngForm #myForm="ngForm">
   <h5 class="card-header">Add New Customer</h5>
   <div class="card-body">
     <div class="form-group">
       <label for="FName">First Name: </label>
       <input class="form-control" [ngClass]="{'is-valid':F.valid,'is-invalid':F.invalid}" type="text" name="FName"
         [(ngModel)]="this.FirstName" required minlength="3" #F="ngModel">
       <!-- error -->
       <div class="alert alert-danger" [hidden]="!(F.dirty && F.errors?.required)">
         Enter First Name
       </div>
       <div class="alert alert-danger" [hidden]="!(F.dirty && F.errors?.minlength)">
         Minimum 3 characters needed for First Name
       </div>
     </div>
     <div class="form-group">
       <label for="LName">Last Name:</label>
       <input class="form-control" [ngClass]="{'is-valid':L.valid,'is-invalid':L.invalid}" type="text" name="LName"
         [(ngModel)]="this.LastName" required minlength="3" #L="ngModel">
       <!-- error -->
       <div class="alert alert-danger" [hidden]="!(L.dirty && L.errors?.required)">
         Enter Last Name
       </div>
       <div class="alert alert-danger" [hidden]="!(L.dirty && L.errors?.minlength)">
         Minimum 3 characters needed for Last Name
       </div>
     </div>
     <input type="button" class="btn btn-success" value="Save" (click)="Save()" [disabled]="myForm.invalid"> &nbsp;
     <input type="button" class="btn btn-danger" value="Cancel" (click)="Cancel()">
   </div>
</div>
```

**步骤 8 – 准备 CustomerAddComponent 视图类**

`CustomerAddComponent` 逻辑上需要以下内容——`FirstName` 和 `LastName` 变量、`CustomerForm` 变量、`Reset`、`Save` 和 `Cancel` 方法。

```
export class CustomerAddComponent {
   FirstName: string;
   LastName: string;
   @ViewChild('myForm') CustomerForm: NgForm;
   Reset() {
     this.CustomerForm.reset();
  }
   Save() {}
   Cancel() {}
}
```

**步骤 9 – 准备 CustomerComponent 模板**



现在，在 `CustomerComponent` 中同时使用上述两个组件，如下所示：

```
<nav class="navbar navbar-dark bg-dark justify-content-end">
   <span class="navbar-brand mb-0 h1"> Welcome {{LoginUserFirstName}},</span>
   <a class="navbar-brand mb-0 h1 underline "
     routerLink='/login' (click)="logout()"><u>Logout</u>
   </a>
</nav>
<div class="container-fluid pt-3">
   <customer-list *ngIf="!(IsAddNew$|async);else AddNewContainer">
   </customer-list>
   <ng-template #AddNewContainer>
    <customer-add></customer-add>
   </ng-template>
</div>
```

**第 10 步 – 检查输出**

如果尚未执行，请使用 `ng serve` 命令运行应用程序。

你应该会看到 `CustomerListComponent`，但数据为空，如下所示：

![](img/Image54078.jpg)

**图 22.3**

## 讨论 – 继续

接下来，我们需要逐步让一切重新工作。先从列表数据开始。如果你还记得，之前我们是从服务中获取数据的。

现在，按照容器-展示模式，展示组件不应处理 Angular 服务。它应该纯粹用于展示目的。与 Angular 服务交互将是容器组件的任务。

**那么 CustomerListComponent 如何获取数据？**

我们将从 CustomerComponent 传递给 CustomerListComponent，为此，我们将使用**输入属性**。

我们已经见识过输入属性的实际应用。现在是时候创建我们自己的自定义输入属性了，这可以通过 `Input` 装饰器实现。

## 实验 – 继续

**第 11 步 – 将 CustomerListComponent 中的常规属性转换为输入属性**

将 Input 装饰器附加到 `CustomerListComponent` 中的 `Customers$` 属性上，使其成为输入属性，如下所示：

```
export class CustomerListComponent {
   @Input()
   Customers$: Observable<Array<Customer>>;
```

**第 12 步 – 为输入属性提供值**

如你所知，我们在 `CustomerComponent` 中有一个名为 `customer$` 的全局变量，它持有 `CustomerService` 中 customer$ 可观察对象的引用。查看以下代码以回忆：

```
export class CustomerComponent {
   ……
   Customers$: Observable<Array<Customer>>;
   ……
   constructor(private customerService: CustomerService,
               private authenticationService: AuthenticationService){
……
     this.Customers$ = this.customerService.Customers$;
  }
```

在上一步中，我们已经将 `CustomerListComponent` 中的 `Customers$` 属性转换为输入属性。因此，可以在 `CustomerComponent` 的模板中访问并为其赋值，如下所示：

```
<nav class="navbar navbar-dark bg-dark justify-content-end">
   <span class="navbar-brand mb-0 h1"> Welcome {{LoginUserFirstName}},</span>
   <a class="navbar-brand mb-0 h1 underline "
     routerLink='/login' (click)="logout()"><u>Logout</u>
    </a>
</nav>
<div class="container-fluid pt-3">
   <customer-list [Customers$]="Customers$"
*ngIf="!(IsAddNew$|async);else AddNewContainer">
   </customer-list>
   <ng-template #AddNewContainer>
    <customer-add></customer-add>
   </ng-template>
</div>
```

## 讨论 – 继续

在上面的代码中，你看到以下代码了吗？

`[Customers$]="Customers$"`

请不要感到困惑，因为等号（`=`）两边都有 `Customers$`。

左边的代表 `CustomerListComponent` 中的输入属性，而右边的代表 `CustomerComponent` 中的常规属性。

## 实验 – 继续

**第 13 步 – 检查输出**

这次，你应该会看到列表已填充。如果没有，请重新检查你的代码，确认没有遗漏任何内容。

（我还建议你从 `Customers$` 属性中移除 Input 装饰器，并检查一次输出。它应该会生成一个错误。我请求你检查那个错误。）

接下来，我们将完成 `AddNew` 代码。

## 讨论 – 继续

**之前我们在 AddNew 上做了什么？**

我们调用了 `CustomerService` 的 `setAddNew` 方法。

**现在我们可以做同样的事情吗？**

是的，可以。将 `CustomerService` 实例注入到 `CustomerListComponent` 中，然后调用该方法。

**我们应该这样做吗？**

不，因为 `CustomerListComponent` 是一个展示组件。展示组件不应处理任何逻辑。它应该向容器组件请求此类事情。

最后的问题是如何在点击展示组件的按钮时调用容器组件的函数。

这可以通过在 `CustomerListComponent` 中创建一个自定义输出属性来实现，为此我们将使用 `output` 装饰器。

让我们进行演示并理解这一点。

## 实验 – 继续

**第 14 步 – 在 CustomerListComponent 中创建自定义输出属性**

在 `CustomerListComponent` 中创建一个类型为 `EventEmitter` 的新属性 `OnAddNew`，并添加 Output 装饰器，如下所示：

```
import {Component, EventEmitter, Input, Output} from '@angular/core';
……
export class CustomerListComponent {
   ……
   @Output()
   OnAddNew:EventEmitter<void> =new EventEmitter<void>();
……
```

**第 15 步 – 触发事件**

接下来，当点击 `AddNew` 按钮时，从 `CustomerListComponent` 触发事件，如下所示：

```
……
  AddNew() {
     this.OnAddNew.emit();
  }
……
```

**第 16 步 – 在 CustomerComponent 中初始化输出属性**

打开 `CustomerComponent` 模板，并为 `CustomerListComponent` 的 `onAddNew` 属性赋值，如下所示：

```
<div class="container-fluid pt-3">
   <customer-list [Customers$]="Customers$" (OnAddNew)="AddNew()"
*ngIf="!(IsAddNew$|async);else AddNewContainer">
   </customer-list>
```

## 讨论 – 继续

让我们分析一下上面的代码。取上面代码的一部分来理解。

`(OnAddNew)="AddNew()"`

在这段代码中，`OnAddNew` 是在 `CustomerListComponent` 中定义的输出属性，而 `AddNew` 是 `CustomerComponent` 中的一个方法。以下是完整流程：

![](img/Image54200.jpg)

**图 22.4**

## 实验 – 继续

**第 17 步 – 检查输出**

经过这些更改后，你应该能够看到 `AddNew` 再次工作。

**第 18 步 – 在 CustomerAddComponent 中为取消声明输出属性**

现在是时候让取消按钮再次生效了。为此，在 `CustomerAddComponent` 中创建一个新属性 `OnCancel`，并为其附加输出装饰器。

```
import {Component, EventEmitter, Output, ViewChild} from '@angular/core';
import {NgForm} from '@angular/forms';
@Component({
   selector: 'customer-add',
   templateUrl: './customer-add.component.html'
})
export class CustomerAddComponent {
……
   @Output()OnCancel:EventEmitter<void>=new EventEmitter<void>();
```

**第 19 步 – 触发事件**

在 `cancel` 方法中触发事件，如下所示：

```
……
export class CustomerAddComponent {
……
   Cancel() {
     this.OnCancel.emit();
     this.Reset();
  }
```

**第 20 步 – 在 CustomerComponent 中初始化 OnCancel**

这有两个步骤。首先，我们需要重构 `CustomerComponent` 中现有的 `Cancel` 方法。

让我们看一下 `CustomerComponent` 的 `Cancel` 方法的现有实现。

```
Cancel() {
     this.customerService.setList();
     this.Reset();
  }
   Reset() {
     this.CustomerForm.reset();
  }
```





`CustomerForm` 不再是 `CustomerComponent` 的一部分，因此它将变为未定义。所以，请从 `CustomerComponent` 中移除 `Reset` 方法，并按如下方式重新定义 `Cancel` 方法：

```
   Cancel() {
     this.customerService.setList();
  }
```

（你还会在 `Save` 函数中发现调用了 `Reset` 方法。请确保也移除该语句，以避免编译错误。）

之后，将 `CustomerComponent` 模板修改如下：

```
……
   <ng-template #AddNewContainer>
    <customer-add (OnCancel)=”Cancel()”></customer-add>
   </ng-template>
</div>
```

在上述代码中，`OnCancel` 是 `CustomerAddComponent` 的输出属性，而 `Cancel` 是 `CustomerComponent` 中定义的方法。

## 第 21 步 – 检查输出

使用上述代码后，取消功能应该可以正常工作。取消后是否得到了一个空网格？

![](img/Image54364.jpg)

**图 22.5**

如果是，那么说明你还没有完成*第 16 章：HTTP 服务*中交给你的任务。要使其正常工作，请打开 `CustomerService`，并在 `SetList` 方法中调用 `LoadCustomer` 方法。

```
……
   setList() {
     this.IsAddNewSubject.next(false);
     this.LoadCustomers();
}
……
```

至此，我们完成了三件事：初始列表、`AddNew` 和 `cancel`。

接下来，让我们完成保存功能。

## 第 22 步 – 在 CustomerAddComponent 中为 Save 声明输出属性

在 `CustomerAddComponent` 中创建一个新属性 `OnSave`，并添加输出装饰器，如下所示：

```
……
import {Customer} from ‘../Models/customer’;
……
   @Output()OnSave: EventEmitter<Customer> = new EventEmitter<Customer>();
……
```

可以看到，`EventEmitter` 的泛型参数不再是 void，而是 `Customer`。

我们需要这样做，因为在触发事件时，我们将把客户数据作为参数传递。

## 第 23 步 – 触发事件

将 `CustomerAddComponent` 中的 `Save` 方法修改如下：

```
……
   Save() {
     this.OnSave.emit(new Customer(this.FirstName,this.LastName));
     this.Reset();
  }
……
```

可以看到，在触发事件时，我们传递了客户对象。

## 第 24 步 – 在 CustomerComponent 中初始化 OnSave

在 `CustomerComponent` 中为 `CustomerAddComponent` 附加 `OnSave` 事件处理程序，如下所示：

```
<ng-template #AddNewContainer>
    <customer-add (OnCancel)=”Cancel()” (OnSave)=”Save($event)”></customer-add>
   </ng-template>
```

你注意到上述代码中的 `$event` 关键字了吗？它代表上一步中发出的值。

## 第 25 步 – CustomerComponent 中的 Save 方法

将 `CustomerComponent` 中的 `Save` 方法修改为以下内容：

```
…..
   Save(c: Customer) {
     this.customerService.Save(c);
  }
……
```

## 第 26 步 – 检查输出

确保经过上述步骤后，保存功能正常工作。

## 讨论 – 续

让我们看看上述代码的完整流程：

![](img/Image54375.jpg)

**图 22.6**

经过最后一步，我们完成了*保存*功能。

## 实验 – 续

## 第 27 步 – 清理 CustomerComponent

从 `CustomerComponent` 中移除所有不必要的代码。最终应如下所示：

```
export class CustomerComponent {
   IsAddNew$: Observable<boolean>;
   Customers$: Observable<Array<Customer>>;

   LoginUserFirstName = ‘DummyFName’;
   constructor(private customerService: CustomerService,
               private authenticationService: AuthenticationService) {
     const decodedToken = jwt_decode(localStorage.token);
     this.LoginUserFirstName = decodedToken.firstName;
     this.IsAddNew$ = this.customerService.IsAddNew$;
     this.Customers$ = this.customerService.Customers$;
  }
   AddNew() {
     this.customerService.setAddNew();
  }
   Save(c: Customer) {
     this.customerService.Save(c);
  }
   Cancel() {
     this.customerService.setList();
  }
   logout() {
     this.authenticationService.logout();
  }
}
```

## 讨论 – 续

**容器-展示模式回顾**

通过上一步，我们完成了容器-展示模式的演示。

让我们快速讨论一下如何决定哪些内容放在哪里。

代码的哪一部分应被视为容器，哪一部分应被视为展示？

所有与展示相关的操作都将属于**展示组件**。

包括排序、分页、字段验证、数据格式化、重置表单等。

所有智能操作，例如决策、路由，以及最重要的与 Angular 服务的协调，都将属于**容器组件**。

**待解决问题**

在本章结束之前，让我们解决实验中的两个待解决问题：第一个控件的自动聚焦和默认回车。先从自动聚焦开始。

如果你考虑使用 HTML 的 autofocus 属性，你会失望的。

HTML 的 autofocus 属性会在页面首次加载时将焦点设置到元素上。

快速尝试一下：

*   在 `firstName` 文本框上设置 `autofocus` 属性并运行应用程序。
*   点击 `AddNew`，你会发现焦点在 `firstName` 文本框上。
*   点击 `Cancel`，然后再次点击 `AddNew`。不幸的是，焦点不会重新设置。

为了解决这个问题，我们将使用 `ViewChild` 装饰器和模板引用变量。通过这两者，我们可以在组件类中获取视图元素的访问权限。

下一个问题是，何时设置焦点？我们需要在组件加载完毕且控件准备好接收焦点时设置焦点。

让我们尝试在构造函数中设置。

## 实验 – 续

## 第 28 步 – 附加模板引用变量

让我们为 firstName 文本框附加一个模板引用变量。

```
   <input #firstName class=”form-control”
[ngClass]=”{‘is-valid’:F.valid,’is-invalid’:F.invalid}”
type=”text” name=”FName”[(ngModel)]=”this.FirstName” required
minlength=”3” #F=”ngModel”>
```

在上述代码中，你可以注意到一个模板引用变量 `firstname` 被附加到了文本框上。

## 第 29 步 – 在组件类中创建对控件的引用

打开 `CustomerAddComponent` 类，创建一个类型为 `ElementRef` 的变量 `FirstNameControl`，如下所示：

```
……
import {Component, ElementRef, EventEmitter, Output, ViewChild}
from ‘@angular/core’;
……
export class CustomerAddComponent{
……
   @ViewChild(“firstName”) FirstNameControl: ElementRef;
……
```

## 第 30 步 – 设置焦点

使用以下代码在构造函数中设置焦点：

```
export class CustomerAddComponent implements AfterViewInit  {
……
   constructor(){
     this.FirstNameControl.nativeElement.focus();
  }
……
```

## 第 31 步 – 检查输出

打开应用程序并点击 `AddNew`。你会进入错误页面。要检查错误，你需要查看本地存储。

![](img/Image54480.jpg)

**图 22.7**

## 讨论 – 续

**错误处理问题**

像这样检查错误是不是很烦人？

每当出现错误时，你都会被重定向到错误页面。然后，你必须在本地存储中查找错误。

在生产环境中，这可能是理想的方式，但在开发环境中，我认为默认方法更有意义，即红色错误会显示在控制台中。




有没有更好的方法？有的。打开你的 `AppErrorHandler`，在 `handleError` 函数的开头添加以下代码块：

```
   if(!environment.production){
       throw error;
    }
```

完整的 `handleError` 函数如下所示：

```
……
import {Router} from ‘@angular/router’;
import {environment} from ‘src/environments/environment’;
@Injectable()
export class AppErrorsHandler implements ErrorHandler {
……
   handleError(error: Error | HttpErrorResponse) {
     if(!environment.production){
alert(‘Run-time error occured.` `Kindly check developer tools’)
       throw error;
    }
     if (error instanceof HttpResponseBase) {
this.HandleServerSideError(error); // Indicates its a server side error
    } else {
this.HandleClientSideError(error); // Indicates its a client side error
    }
  }
……
```

经过这一改动，你的自定义错误处理器仅在当前环境为生产环境时才会生效。

**如何解决焦点问题？**

现在的问题是，如何处理焦点问题？在构造函数内部编写逻辑是行不通的。构造函数在 `CustomerAddComponent` 的实例被创建时调用，而此时文本框甚至还不存在。

一种解决方案是 Angular 的生命周期事件。Angular 通过暴露许多生命周期方法，让我们能够钩入 Angular 的执行过程。我们可以将自定义逻辑放入这些方法中，并执行自定义操作。

其中一个生命周期方法是 `ngOnInit`。它在组件初始化后执行。

让我们试试看。

## 实验 – 继续

**步骤 32 – 实现 `ngOnInit` 并添加焦点逻辑**

为此，让 `CustomerAddComponent` 实现 `OnInit` 接口，这将强制我们定义 `ngOnInit` 方法。在 `ngOnInit` 中，将焦点设置到 `firstName` 文本框上。

```
import {Component, ElementRef, EventEmitter, OnInit, Output, ViewChild}
from ‘@angular/core’;
……
@Component({
   selector: ‘customer-add’,
   templateUrl: ‘./customer-add.component.html’
})
export class CustomerAddComponent implements OnInit  {
   ……
   @ViewChild(“firstName”) FirstNameControl: ElementRef;
   ngOnInit(){
     this.FirstNameControl.nativeElement.focus();
  }
……
```

**步骤 33 – 检查输出**

不幸的是，这仍然不起作用。

## 讨论 – 继续

不幸的是，`ngOnInit` 并没有帮助。它在组件初始化后被调用。此时控件尚未渲染，因此 `this.FirstNameControl` 将是 `undefined`。

***注意：*** 请理解，构造函数阶段组件甚至尚未初始化，而在 `ngOnInit` 期间，组件已初始化但尚未渲染。

对于这种情况，我们有一个完美的生命周期方法——`ngAfterViewInit`。它是需要访问已渲染控件的逻辑的理想候选。

让我们使用它。

## 实验 – 继续

**步骤 34 – 实现 `ngAfterViewInit`**

让 `CustomerAddComponent` 实现 `AfterViewInit` 接口，然后按如下方式定义 `ngAfterViewInit` 方法：

```
import {AfterViewInit, Component, ElementRef, EventEmitter,
Output, ViewChild} from ‘@angular/core’;
……
export class CustomerAddComponent implements AfterViewInit  {
…….
   @ViewChild(“firstName”) FirstNameControl: ElementRef;
```

**步骤 35 – 检查输出**

最后，你会发现它生效了。你会注意到，每次访问 `CustomerAddNewComponent` 时，`firstName` 文本框都会获得焦点。

## 讨论 – 继续

因此，通过前面的步骤，我们成功实现了焦点需求。接下来，让我们解决默认回车问题。

如果你还记得，之前我们通过将整个部分放在一个 *form* 标签内，并将常规 *button* 替换为 *submit* 按钮来实现这一点。

这次我们将采用相同的方法。

## 实验 – 继续

**步骤 36 – 实现默认回车**

将 `CustomerAddComponent` 中的 `containerdiv` 元素替换为 form 标签，并将常规按钮替换为 submit 按钮，如下所示：

```
   <form class=”card” #myForm=”ngForm”>
     <h5 class=”card-header”>Add New Customer</h5>
……
       <input type=”submit” class=”btn btn-success” value=”Save”
       (click)=”Save()” [disabled]=”myForm.invalid”> &nbsp;
……
     </div>
   </form>
```

**步骤 37 – 检查输出**

在两个文本框中输入一些值，然后直接按回车键。它将自动触发 `Save` 函数，这样我们就实现了目标。

## 讨论 – 继续

尽管一切看起来都很棒，但与之前相比还是有些不同。你注意到了吗？

之前，`ngForm` 指令是显式附加到 `div` 标签上的。

你是否注意到，我们没有将 `ngForm` 指令显式附加到我们的 `form` 标签上？那么，为什么一切都能正常工作呢？

嗯，在**模板驱动表单**中，`ngForm` 指令会自动附加到 *form* 元素上——无需显式操作。

这就是为什么当我们将 `div` 改为 *form* 时，我们移除了它的原因。

#### 总结

现在，我们已经完成了第 11 站的旅程。让我们快速回顾一下本章学到的内容：

*   我们讨论了一种现代世界中的新 UI 开发方法——组件化风格。这是一种 UI 设计方法，允许我们将 UI 创建为多个更小、可复用组件的组合。

*   我们了解到 Angular 并不是组件化方法的先驱，它只是遵循了这一方法。其他技术，如 React 和 Polymer，也遵循类似的过程。

*   我们了解到这种方法使我们的代码维护变得容易，并允许多个 UI 开发人员并行工作。

*   我们讨论了代表应用程序主要组件的组件，这些组件通常通过路由访问。

*   我们了解到，有时为了代码的可读性和可管理性，会将一个功能组件拆分为更小的组件。容器-展示模式是业界为此目的常用的模式之一。

*   我们快速讨论了容器组件和展示组件之间的区别。容器组件通常是“智能”的，而展示组件被称为“哑”组件，它们负责 UI 展示。

*   我们创建了自定义输入属性，用于将数据从外部组件传递到内部组件。

*   我们创建了自定义输出属性，用于从内部组件触发事件，这些事件可以在外部组件中处理。

*   我们重新审视了 ViewChild 装饰器和模板引用变量，并学习了如何引用组件类的视图元素。

*   我们在本章中再次学习了如何使用环境。我们让错误处理代码在不同环境（开发和生产）下表现不同。

*   我们重新审视了 `ngOnInit`，并了解了它如何最适合初始化逻辑。

*   我们学习了 `ngAfterViewInit` 生命周期，它是需要访问已渲染控件的逻辑的理想候选。

*   我们了解到，在模板驱动表单中，我们不需要显式地将 `ngForm` 指令分配给 form 标签。

## 第 23 章

## Angular 路由

## 引言

那么，大家都准备好学习 Angular 路由这一章并前往第 12 站了吗？

我们已经在之前的一章中看到了路由的实际应用。

在本章中，我们将深入探讨并了解更多相关内容。

## 实验 7 – Angular 路由





### 步骤 1 – 重命名应用程序

将应用程序从 `lab6-ng` 重命名为 `lab7-ng`。

### 步骤 2 – 为演示创建更多组件

本次演示需要更多组件。在 `app` 文件夹内创建 `Supplier` 和 `Product` 文件夹，然后在其中创建相应的组件。

```
1.  import {Component} from ‘@angular/core’;
3.  @Component({
4.     selector: ‘supplier’,
5.     template: ‘<h1>Welcome to supplier</h1>’
6.  })
8.  export class SupplierComponent {
9.     constructor() {}
10.  }
```

```
1.  import {Component} from ‘@angular/core’;
3.  @Component({
4.     selector: ‘product’,
5.     template: ‘<h1>Welcome to product</h1>’
6.  })
8.  export class ProductComponent {
9.     constructor() {}
10.  }
```

如你所见，这次我们使用了 `template` 而不是 `templateURL`。

使用 `template`，我们可以将组件 HTML 内联指定，而无需将其放在单独的 HTML 文件中。

```
1.  ……
2.  import {ProductComponent} from ‘./Product/product.component’;
3.  ……
4.  import {SupplierComponent} from ‘./Supplier/supplier.component’;
5.  @NgModule({
6.     declarations: [AppComponent, LoginComponent,
7.       CustomerComponent, ErrorTestComponent, ErrorComponent,
8.       CustomerAddComponent, CustomerListComponent,
9.       ProductComponent, SupplierComponent
10.    ],
11.  ……
12.     bootstrap: [AppComponent],
13.  })
14.  export class AppModule {}
```

不要忘记将它们添加到 `AppModule` 中。

### 步骤 3 – 准备路由

接下来，打开 `app.routes.ts` 并按如下方式为上述两个组件配置路由：

```
1.  ……
2.  import {ProductComponent} from ‘../Product/product.component’;
3.  import {SupplierComponent} from ‘../Supplier/supplier.component’;
5.  export const AppRoutes: Routes = [
6.     {path: ‘login’, component: LoginComponent},
7.     {path: ‘customer’, component: CustomerComponent, canActivate: [AuthGuard]},
8.     {path: ‘supplier’, component: SupplierComponent, canActivate: [AuthGuard]},
9.     {path: ‘product’, component: ProductComponent, canActivate: [AuthGuard]},
10.     {path: ‘error-test’, component: ErrorTestComponent},
11.     {path: ‘error’, component: ErrorComponent},
12.     {path: ‘’, redirectTo: ‘login’, pathMatch: ‘full’},
13.     {path: ‘**’, redirectTo: ‘customer’, pathMatch: ‘full’},
14.  ];
```

## 讨论 – 续

现在，我们遇到了一些有趣的问题。需要解决以下三个问题：

1.  我们希望创建一个菜单，用于在上述组件之间导航。

    **问题是，我们将菜单添加到哪个组件中？**

    如果添加到 AppComponent，那么即使在登录屏幕上也会显示该菜单。

    在每个组件中显式添加菜单并不可行，因为这会违反 DRY 原则（不要重复自己——代码一旦编写，就不要重复）。

2.  其次，检查上面的路由配置代码。你是否注意到每个路由上都附加了 AuthGuard？这同样违反了 DRY 原则。这是我们的**第二个问题**。

3.  最后，在之前的一章中，我们在客户组件中添加了已登录用户的姓名和注销链接。作为应用程序，它必须出现在每个页面上。这是**第三个问题**。

所有这三个问题的解决方案是**嵌套路由**。

我们将引入另一个组件——AuthComponent，作为菜单、用户名、注销链接以及所有其他需要授权的组件的父组件。

## 实验 – 续

### 步骤 4 – 创建 AuthComponent

在 app 文件夹中创建一个名为 `Auth` 的新文件夹，然后按如下方式创建一个名为 `AuthComponent` 的新组件：

```
1.  import {Component} from ‘@angular/core’;
2.  import {AuthenticationService} from ‘../Services/authentication.service’;
3.  import * as jwt_decode from ‘jwt-decode’;
4.  @Component({
5.     selector: ‘auth-root’,
6.     templateUrl: ‘./auth.component.html’
7.  })
8.  export class AuthComponent {
9.     LoginUserFirstName = ‘DummyFName’;
11.     constructor(private authenticationService: AuthenticationService) {
12.         const decodedToken = jwt_decode(localStorage.token);
13.         this.LoginUserFirstName = decodedToken.firstName;
14.    }
15.     logout() {
16.       this.authenticationService.logout();
17.    }
18.  }
```

如你所见，`CustomerComponent` 中的用户名和注销代码已移至 `AuthComponent`。

（请确保从 `CustomerComponent` 中删除相应的代码，因为它已不再相关。）

模板文件应如下所示：

```
1.  <nav class=”navbar navbar-expand navbar-dark bg-dark”>
2.     <div class=”collapse navbar-collapse” id=”navbarSupportedContent”>
3.       <ul class=”navbar-nav mr-auto”>
4.         <li class=”nav-item “>
5.           <a class=”nav-link” href=”/customer”>Customer</a>
6.         </li>
7.         <li class=”nav-item “>
8.           <a class=”nav-link” href=”/supplier”>Supplier</a>
9.         </li>
10.         <li class=”nav-item “>
11.           <a class=”nav-link” href=”/product”>Product</a>
12.         </li>
13.       </ul>
14.       <span class=”navbar-brand mb-0 h1”> Welcome {{LoginUserFirstName}},</span>
15.       <a class=”navbar-brand mb-0 h1 underline” routerLink=’/login’ (click)=”logout()”><u>Logout</u></a>
16.     </div>
17.  </nav>
18.  <router-outlet></router-outlet>
```

你是否注意到 `AuthComponent` 中再次出现了 `router-outlet`？它将作为所有需要授权的组件的占位符。

确保也将其添加到 `AppModule` 中，如下所示：

```
1.  ……
2.  @NgModule({
3.     declarations: [……,
4.       ProductComponent, SupplierComponent,AuthComponent
5.    ],
6.  ……
7.  export class AppModule {}
```

### 步骤 5 – 修改路由

按如下方式修改路由代码：

```
1.  export const AppRoutes: Routes = [
2.     {path: ‘login’, component: LoginComponent},
3.     {
4.       path: ‘’,
5.       component: AuthComponent,canActivate:[AuthGuard],
6.       children: [
7.         {
8.           path: ‘customer’,
9.           component: CustomerComponent
10.        },
11.         {
12.           path: ‘supplier’,
13.           component: SupplierComponent
14.        },
15.         {
16.           path: ‘product’,
17.           component: ProductComponent
18.        },
19.      ],
20.    },
21.     {path: ‘error-test’, component: ErrorTestComponent},
22.     {path: ‘error’, component: ErrorComponent},
23.     {path: ‘**’, redirectTo: ‘customer’, pathMatch: ‘full’},
24.  ];
```

## 讨论 – 续

让我们尝试理解这段代码：

*   有两个顶级路由——*login*，负责 `LoginComponent`；以及 *auth* 路由，负责 `AuthComponent`。

*   `AppComponent` 中的 *router-outlet* 成为 `LoginComponent` 和 `AuthComponent` 的占位符，具体取决于路由。

*   `AuthComponent` 中的 *router-outlet* 根据 *auth* 路由的子路由成为其他组件的占位符。

## 实验 – 续

### 步骤 6 – 检查输出

执行应用程序并完成登录，确保所有三个链接按预期工作。

![](img/Image54736.jpg)

**图 23.1**

## 讨论 – 续

我们需要解决以下三个问题：

1.  **页面刷新**

    你是否注意到上述输出中有些奇怪的地方？

    你是否注意到每次点击链接时页面都会刷新？

    如果页面刷新，那就不是 SPA。我们必须在不刷新页面的情况下实现相同的输出，这可以通过使用 `routerLink` 指令来实现。

2.  **高亮当前菜单**





截至目前，当前菜单并未高亮显示。可以使用 `routerLinkActive` 指令来解决这个问题。

3.  **空 URL**

前面提到的问题是，当 URL 为空时，我们会看到一个空白屏幕。（运行应用程序，完成登录后检查你看到的内容——一个空白的白色屏幕。）

让我们逐一解决这些问题。

### 步骤 7 – 将锚点替换为 routerLink

打开 `auth.component.html`，将 `href` 替换为 `routerLink` 指令，如下所示：

```
………
<li class=”nav-item “>
         <a class=”nav-link” routerLink=”/customer”>客户</a>
       </li>
       <li class=”nav-item “>
         <a class=”nav-link” routerLink=”/supplier”>供应商</a>
       </li>
       <li class=”nav-item “>
         <a class=”nav-link” routerLink=”/product”>产品</a>
       </li>
………
```

### 步骤 8 – 检查输出

这将解决我们的第一个问题。这次你会得到相同的输出，但页面不会刷新。

### 步骤 9 – 为活动菜单定义 CSS

在 `style.css` 文件中创建一个新的 CSS 类 `active`，如下所示：

```
.active{
   color: black;
   background-color: gray;
}
```

### 步骤 10 – 附加 routerLinkActive 指令

将 `routerLinkActive` 指令附加到每个菜单项，如下所示：

```
……
     <li class=”nav-item “>
           <a class=”nav-link” routerLinkActive=”active” routerLink=”/customer”>客户</a>
         </li>
         <li class=”nav-item “>
           <a class=”nav-link”  routerLinkActive=”active” routerLink=”/supplier”>供应商</a>
         </li>
         <li class=”nav-item “>
           <a class=”nav-link”  routerLinkActive=”active” routerLink=”/product”>产品</a>
         </li>
……
```

### 步骤 11 – 检查输出

如你所见，`active` 类仅附加到了当前菜单项。其他菜单显示时没有应用任何格式。

![](img/Image54744.jpg)

**图 23.2**

### 步骤 12 – 附加默认路由

根据我们当前的路由配置，当 URL 为空时，将显示 `AuthComponent`。

但该配置仅适用于主路由。我们需要对子路由也做同样的处理。为此，将默认路由添加到子路由集合中，如下所示：

```
……
export const AppRoutes: Routes = [
   {path: ‘login’, component: LoginComponent},
   {
     path: ‘’,
     component: AuthComponent,canActivate:[AuthGuard],
     children: [
       {
         path: ‘customer’,
         component: CustomerComponent
      },
       {
         path: ‘supplier’,
         component: SupplierComponent
      },
       {
         path: ‘product’,
         component: ProductComponent
      },
       {
         path: ‘’,
         redirectTo: ‘customer’, pathMatch: ‘full’
      },
    ],
  },
   {path: ‘error-test’, component: ErrorTestComponent},
   {path: ‘error’, component: ErrorComponent},
   {path: ‘**’, redirectTo: ‘customer’, pathMatch: ‘full’},
];
……
```

### 步骤 13 – 检查输出

现在，使用空 URL 检查输出。你将被重定向到客户路由。

## 讨论 – 续

尽管一切按预期工作，但前面的实验中存在一个大问题，即急切加载。

所有组件从一开始就被加载到项目中。

打开开发者工具并检查源代码选项卡。你会找到 `main.js`。请打开它并上下滚动，查看客户模板内容、供应商模板内容和产品模板内容。所有内容都打包在一个文件中。

![](img/Image54825.jpg)

**图 23.3**

![](img/Image54860.jpg)

**图 23.4**

让我们构建项目，确认生成的包文件是否也存在同样的问题。

在命令提示符中按 `Ctrl + C` 停止当前执行。

然后使用 `ng build` 命令创建项目构建。

![](img/Image54867.jpg)

**图 23.5**

如你所见，只生成了一个与应用相关的包——`main.js`。

现在，在其中搜索 `customer` 关键字。然后搜索 `supplier`，接着搜索 `product`。

你会发现所有内容都在这一个 JavaScript 文件中。

想象一下一个包含数百个此类组件的项目。想象一下包的大小，以及浏览器下载这个巨大包文件的负载。

解决方案是惰性加载。我们将配置路由以惰性加载组件。

为此，首先必须将每个组件封装在独立的 Angular 模块中。

## 实验 – 续

### 步骤 14 – 创建 Angular 模块

在 `Customer` 文件夹中创建一个新的 Angular 模块 `CustomerModule`。然后，将所有与客户相关的组件包含在这个 `CustomerModule` 中。

```
import {NgModule} from ‘@angular/core’;
import {CustomerAddComponent} from ‘./customer-add.component’;
import {CustomerListComponent} from ‘./customer-list.component’;
import {CustomerComponent} from ‘./customer.component’;
@NgModule({
   declarations: [CustomerComponent,CustomerListComponent,CustomerAddComponent]
})
export class CustomerModule {}
```

完成后，确保从 `AppModule` 中移除上述所有组件。

![](img/Image54948.jpg)

**图 23.6**

## 讨论 – 续

如你所见，`CustomerComponent`、`CustomerListComponent` 和 `CustomerAddComponent` 被添加到了 `CustomerModule` 的 `declaration` 部分。

*   但你可能注意到 `NgModule` 装饰器中没有 `bootstrap` 部分。

    `bootstrap` 部分仅在根模块中需要，用于声明根组件。

*   你可能已经注意到 `imports` 部分缺少了 `BrowserModule`。

    这是因为 `BrowserModule` 中注册的服务需要是单例的，因此它只在根模块中导入。

不必过于担心。在下一章中，我们将复习关于 Angular 模块（涉及服务、组件、路由等）的所有知识。

## 实验 – 续

### 步骤 15 – 创建其他 Angular 模块

接下来，创建 `SupplierModule` 和 `ProductModule`，如下所示：

```
import {NgModule} from ‘@angular/core’;
import {SupplierComponent} from ‘../Supplier/supplier.component’;
@NgModule({
   declarations: [SupplierComponent],
})
export class SupplierModule {}
```

```
import {NgModule} from ‘@angular/core’;
import {ProductComponent} from ‘./product.component’;
@NgModule({
   declarations: [ProductComponent],
})
export class ProductModule {}
```

同样，不要忘记从 `AppModule` 中移除相应的组件。

### 步骤 16 – 重新配置路由以实现惰性加载

打开 `app.route.ts` 文件，将路由修改为以下内容：

```
export const AppRoutes: Routes = [
   {path: ‘login’, component: LoginComponent},
   {
     path: ‘’,
     component: AuthComponent,
     canActivate: [AuthGuard],
     children: [
       {
         path: ‘customer’,
         loadChildren: () =>
           import(‘src/app/Customer/customer.module’).then(
             (x) => x.CustomerModule
          ),
      },
       {
         path: ‘supplier’,
         loadChildren: () =>
           import(‘src/app/Supplier/supplier.module’).then(
             (x) => x.SupplierModule
          ),
      },
       {
         path: ‘product’,
         loadChildren: () =>
```





```
           import('src/app/Product/product.module').then(
             (x) => x.ProductModule
          ),
      },
       {
         path: '',
         redirectTo: 'customer',
         pathMatch: 'full',
      },
    ],
  },
   {path: 'error-test', component: ErrorTestComponent},
   {path: 'error', component: ErrorComponent},
   {path: '**', redirectTo: 'customer', pathMatch: 'full'},
];
```

如你所见，我们已经移除了所有组件的引用，现在改为引用模块。

同时，在定义路由时，我们不再使用 `component`，而是使用 `loadChildren`。

### 第 17 步 – 定义子路由

要使懒加载生效，还需要执行最后一步。定义子路由，并在相应的 Angular 模块中按如下方式配置：

```
const childRoute: Routes = [{path: '', component: CustomerComponent}];

@NgModule({
   imports: [RouterModule.forChild(childRoute)],
   declarations: [
     CustomerComponent,
     CustomerListComponent,
     CustomerAddComponent,
  ],
})
export class CustomerModule {}
```

```
const childRoute: Routes = [{path: '', component: SupplierComponent}];

@NgModule({
   imports: [RouterModule.forChild(childRoute)],
   declarations: [
     SupplierComponent
  ],
})
export class SupplierModule {}
```

```
const childRoute: Routes = [{path: '', component: ProductComponent}];

@NgModule({
   imports: [RouterModule.forChild(childRoute)],
   declarations: [
     ProductComponent
  ],
})
export class ProductModule {}
```

### 第 18 步 – 检查控制台

我不确定你是否查看过运行 Angular 应用程序的命令提示符。你会发现 `CustomerAddComponent` 和 `CustomerListComponent` 抛出了一堆错误。

![](img/Image55004.jpg)

**图 23.7**

向下滚动，你会看到 `CustomerListComponent` 抛出的 `*ngFor` 错误、`CustomerComponent` 抛出的 `*ngIf` 错误，以及 `CustomerAddComponent` 抛出的 `ngModel` 错误。

## 讨论 – 续

如你所知，Angular 中的组件属于某个 Angular 模块。

同样的规则也适用于指令和管道。（稍后我们将创建自定义指令和管道，届时你会看到实际效果。）

我们在本书前面已经讨论过模块的概念——在 ES6 学习和 TypeScript 学习中。模块的思想在任何地方都是一样的。

在一个模块中定义的所有内容，默认情况下对该模块是私有的，外部无法访问。如果一个模块想要访问另一个模块中定义的内容，那么第二个模块需要导入第一个模块。

**ngModule**

如果你还记得，在我们之前的代码中，`CustomerAddComponent` 是 `AppModule` 的一部分，并且我们在 `AppModule` 中导入了 `FormsModule`。这就是我们能够在 `CustomerAddComponent` 中使用诸如 `ngModel` 等指令的原因。

在新代码中，`CustomerAddComponent` 被定义为 `CustomerModule` 的一部分。我们从未在 `CustomerModule` 中导入 `FormsModule`。这就是我们收到此类错误的原因。

在 `CustomerModule` 中导入 `FormsModule` 将解决 `CustomerAddComponent` 中抛出的一堆错误。

`*ngFor`、`*ngIf` 和 `ngClass`

但这并不能解决 `CustomerListComponent` 抛出的关于 `*ngFor` 的错误。

`*ngFor`、`*ngIf`、`ngClass` 是在 `CommonModule` 中定义的指令。

要解决这些指令相关的错误，我们需要在相应的模块中导入 `CommonModule`。

现在，我相信有一个大问题困扰着你。**为什么之前能正常工作？**

之前，`CustomerListComponent` 是 `AppModule` 的一部分。我知道你会立刻说：“但我们没有在 `AppModule` 中导入 `CommonModule`。” 确实如此，但你导入了 `BrowserModule`，而它内部导入了 `CommonModule`。（你将在下一章中了解更多关于 Angular 模块的内容。）

**那么为什么我们不在 `CustomerModule` 中导入 `BrowserModule` 呢？**

`BrowserModule` 还会为一些负责 DOM 操作和许多其他浏览器相关服务的服务配置注入器。这些服务预期在应用程序级别是单例的。再次导入它会抛出以下错误：

![](img/Image55012.jpg)

**图 23.8**

## 实验 – 续

### 第 19 步 – 导入 Forms 和 CommonModule

在 `CustomerModule` 中同时导入 `FormsModule` 和 `CommonModule`。

```
@NgModule({
   imports: [RouterModule.forChild(childRoute),CommonModule,FormsModule],
   declarations: [
     CustomerComponent,
     CustomerListComponent,
     CustomerAddComponent,
  ],
})
export class CustomerModule {}
```

### 第 20 步 – 检查输出

确保所有路由都能像之前一样正常工作。然后，打开开发者工具并检查源代码选项卡。

![](img/Image55058.jpg)

**图 23.9**

你会看到 `main.js`，但除此之外，你还会发现另一个与客户相关的 JavaScript 文件。

接下来，点击供应商链接，你会发现与供应商相关的 JavaScript 文件被加载。产品也是如此。

![](img/Image55098.jpg)

**图 23.10**

这就是所谓的懒加载。根据需求，`组件/模块` 被加载。

### 第 21 步 – 构建项目

使用 `ng build` 命令构建项目，并检查生成的文件。你会发现每个懒加载模块都有一个对应的包。

# 懒加载的是什么？——模块还是组件？

当你学习这个概念时，有时会听到模块被懒加载，有时是组件。那么，到底什么被懒加载了？

答案是两者都有。模块被懒加载，它们对应的组件也被懒加载。

# 打包是好是坏？

我相信你现在一定在想一件事。

*之前在学习 JavaScript 时，我们谈到了打包的优势。我们说需要打包，而现在我们却在寻找创建多个包的方法。*

让我澄清一下。打包确实很好，但包不应该太大。如果太大，就把它拆分成多个。

我的大多数客户都遇到过这个问题。我见过包大小超过 30MB 的项目。

# 这是否意味着我们应该对每个模块都进行懒加载？

在我们的例子中，我配置路由的方式是让每个模块都懒加载。因此，每个模块都会生成一个包，但在实际项目中并非如此。

如果你这样做，那么打包就毫无意义了。这就像按需加载所有内容。

# 混合方法

在实际项目中，要明智地做出决定。一部分模块急切加载，一部分模块懒加载。

例如，看下面的示例路由：

```
export const AppRoutes: Routes = [
   {path: 'login', component: LoginComponent},
   {path:'',component:AuthComponent,children:[
     {
       path:'config',
loadChildren:import("src/app/master/maser.module").then(x=>x.MasterModule)
    },
     {
       path:'exec',
loadChildren:import("src/app/transaction/transaction.module").then(x=>x.TransactionModule)
    }
  ]},
];

@NgModule({
   declarations: [LoginComponent,HeaderComponent,AuthComponent],
})
export class InitialModule {}

@NgModule({
   imports:[InitialModule,RouterModule.forRoot(AppRoutes)],
   declarations: [AppComponent],
})
export class AppModule   {}
```





*   在上述代码中，你可以看到四个 Angular 模块的实际应用——`AppModule`、`InitialModule`、`MasterModule` 和 `TransactionModule`。
    *   假设 `LoginComponent`、`HeaderComponent` 和 `AuthComponent` 被声明为 `InitialModule` 的一部分。
    *   假设 `MasterModule` 包含 `CustomerComponent` 和 `ProductComponent`。
    *   假设 `TransactionModule` 包含 `CheckoutComponent` 和 `CheckInComponent`。
*   `AppComponent` 是根组件，`AppModule` 是根模块。因此它会在应用初始化时被加载，并包含在主包中。
*   `InitialModule` 被直接导入到 `AppModule` 中。因此它会被立即加载，并包含在主包中。
*   `MasterModule` 将被懒加载，因此会为该模块创建一个单独的包，其中包含 `CustomerComponent` 和 `ProductComponent`。
*   `TransactionModule` 将被懒加载，因此会为该模块创建一个单独的包，其中包含 `CheckoutComponent` 和 `CheckInComponent`。

让我们分别探讨这两个模块。

```
1.  export const configRoutes: Routes = [
2.     {path: ‘customer’, component: CustomerComponent},
3.     {path: ‘product’, component: ProductComponent},
4.  ];
5.  @NgModule({
6.     imports:[RouterModule.forChild(configRoutes)],
7.     declarations: [CustomerComponent,ProductComponent],
8.  })
9.  export class MasterModule  {}
```

`MasterModule` 为其两个组件配置了路由。

```
1.  export const execRoutes: Routes = [
2.     {path: ‘cout’, component: CheckoutComponent},
3.     {path: ‘cin’, component: CheckInComponent},
4.     {path: ‘bal’, component: BalanceSheetComponent},
5.     {path: ‘pnl’, component: ProfitAndLossComponent},
6.  ];
7.  @NgModule({
8.     declarations: [BalanceSheetComponent,ProfitAndLossComponent],
9.  })
10.  export class ReportModule {}
11.  @NgModule({
12.     imports:[ReportModule],
13.     declarations: [CheckoutComponent,CheckInComponent],
14.  })
15.  export class TransactionModule  {}
```

看看 `TransactionModule`。它不仅为自身的每个组件配置了路由，还为 `ReportsModule` 的组件配置了路由。`TransactionModule` 导入了 `ReportsModule`。因此，当 `TransactionModule` 被加载时，`ReportsModule` 也会被加载。此外，`ReportsModule` 中的所有组件都会成为同一个包的一部分。

简而言之，`ReportModule` 和 `TransactionModule` 将被包含在同一个模块中。

因此，总体来看，上述示例有三个懒加载模块——主模块、master 模块和 transaction 模块。

# 预加载策略

懒加载是一个很好的特性，因为它使包更小并减少了初始加载时间——Angular 会在用户首次请求模块时加载它。

Angular 允许我们通过一种称为预加载的技术进一步优化应用——在用户与应用交互时，在后台异步加载懒加载模块。这有助于提升应用的加载时间。

当我们使用 `forRoot` 方法配置路由时，我们可以传入第二个参数来指定策略。

```
1.  RouterModule.forRoot(AppRoutes, {preloadingStrategy: NoPreloading}))
```

它可以有两个可能的值。

`NoPreloading`：这是默认值。表示你不想预加载，因此配置为懒加载的模块将按需下载。

`PreloadAllModules`：表示你想在后台异步加载所有懒加载模块。

通过预加载懒加载模块，用户无需等待模块下载。所有模块都已在后台下载完毕。

尝试使用这两种策略运行我们的项目。这非常简单。只需运行，然后在开发者工具中查看哪些被加载了，哪些没有。

你是否对立即加载和带有 `PreloadAllModules` 的懒加载感到困惑？

**立即加载**

将模块作为同一个包的一部分，并在开始时加载。

**带有 NoPreloading 的懒加载**

为每个懒加载模块创建一个单独的包，并按需加载。

**带有 PreloadAllModules 的懒加载**

为每个懒加载模块创建一个单独的包，并在后台异步加载所有模块。

# 自定义预加载策略

我们甚至可以创建自定义预加载策略来满足我们的需求。为此，我们必须创建一个继承自 `PreLoadingStrategy` 类的自定义类，然后定义 `preload` 方法。

```
1.  export class CustomPreloadStrategy implements PreloadingStrategy {
2.     preload(route: Route, load: () => Observable<any>): Observable<any> {
3.       if (true){
4.         return load();
5.      }
6.       else{
7.         return of(null);
8.      }
9.    }
10.  }
```

`pre-load` 方法会为应用中配置的每个懒加载路由调用一次。

如你所见，pre-load 方法的第一个参数是当前路由。我们可以用它来提取正在加载的路由的信息。

第二个参数是一个 `Observable` 函数，如果我们想预加载这个模块，就需要返回它。如果我们不想预加载该模块，可以返回 `Observable` 的 null。

#### 总结

至此，我们完成了路由的学习，也完成了前往第 12 站的旅程。让我们回顾一下本章学到的内容：

*   我们学习了当组件 HTML 很简单时，如何使用 template 属性代替 templateUrl。
*   我们重新回顾了 router-outlet 组件，它根据不同的 URL 显示不同的组件。
*   我们讨论了 `routerLink` 指令，它允许我们在路由之间导航而无需刷新整个页面。
*   我们学习了 `routerLinkActive`，它允许我们在特定路由处于活动状态时添加 CSS 类。
*   我们讨论了默认路由，当 URL 为空时会加载这些路由。
*   我们了解到可以在根级别和子级别定义默认路由。
*   我们详细研究了懒加载，并学习了它如何减少初始加载时间。
*   我们讨论了预加载策略，它让我们决定是否异步加载懒加载模块。

## 第 24 章

### Angular 模块

## 引言

前往第 13 站的旅程将是所有旅程中最棒的。通过这一章，你将得到几乎所有之前未解答问题的答案。

我们将讨论 Angular 模块的一切。我们将探讨为什么需要它们？我们将讨论它们如何与组件、服务和路由协同工作。

#### Angular 模块与 Angular 组件

在经历了 23 章并完成第 12 站的旅程后，你一定对 Angular 组件有了清晰的认识。它们是 Angular 应用的基本构建块，代表整个 UI 中自包含的一部分。

组件被封装在 Angular 模块内部。

让我们回答几个与之相关的问题。

##### 问题 1 – 为什么将 Angular 组件分组到 Angular 模块中？

我们现在非常清楚，在真实项目中，我们会创建多个基于功能的组件。

想象一个具有十个功能的应用。

它会有多少个组件？

如果你说十个，那并不是正确答案。它会有更多。

我们可能会开发一些可复用的组件。





我们甚至可以将每个功能组件规划为多个更小的组件，使其更具可读性和可管理性。还记得我们的 `CustomerComponent` 吗？我们将其拆分为 `CustomerList`、`CustomerAdd` 和 `CustomerComponent`。

简而言之，我们最终可能会得到大量组件。

组件都有选择器。如何确保每个组件都有唯一的选择器？实际上，这是不可能的。这就是为什么我们需要 Angular 模块。

让我们快速演示一下。

# 实验 8 – 多个 Angular 模块和组件

### 步骤 1 – 创建新的 Angular 项目

使用 Angular CLI，按如下方式创建一个新的 Angular 项目：

1.  `ng new myapp`

### 步骤 2 – 创建功能组件

对于此演示，我们需要两个组件——`Customer` 和 `Product`。

这次我们不会手动操作，而是使用 Angular CLI 来完成。

确保你位于 `myapp` 文件夹内，然后执行以下命令：

1.  `ng g c Customer`

如你所见，CLI 为我们完成了所有繁重的工作。

它创建了 customer 文件夹。

![](img/Image55153.jpg)

**图 24.1**

它为你创建了组件，并将组件类与其模板和 CSS 连接起来。

1.  它将选择器设置为 `app-customer`。
2.  它还将该组件添加到了 `AppModule` 的 `NgModule` 装饰器中的 `declarations` 部分。

### 步骤 3 – 创建 ProductComponent

使用相同的方法，创建 `ProductComponent`。

![](img/Image55215.jpg)

**图 24.2**

### 步骤 4 – 为 Customer 创建 HeaderComponent

现在，假设 `CustomerComponent` 的开发人员决定将其拆分为更小的组件。他/她得出结论，需要 `HeaderComponent`，因此可以像上图所示那样创建它。

![](img/Image55252.jpg)

**图 24.3**

如你所见，我们指示 CLI 在 `customer` 文件夹内创建一个新组件。

其次，默认情况下，CLI 会为每个组件创建一个新文件夹。通过使用 `--flat` 标志，我们指示 CLI 跳过自定义文件夹的创建。

打开组件并检查选择器。

```
@Component({
   selector: ‘app-header’,
……
```

### 步骤 5 – 为 Product 创建 HeaderComponent

`ProductComponent` 的开发人员也经历了同样的思考过程。他也按如下方式创建了 `HeaderComponent`：

![](img/Image55287.jpg)

**图 24.4**

你是否注意到这个组件有什么有趣的地方？你会发现这次 `AppModule` 没有更新。

CLI 未能将新的 `HeaderComponent` 添加到 `AppModule`，因为其类名与上一步创建的 `HeaderComponent` 冲突。

### 步骤 6 – 将新的 HeaderComponent 添加到模块

让我们使用 TypeScript 别名手动完成，如下所示：

```
……
import {HeaderComponent as ProductHeaderComponent} from
‘./product/header.component’;
import {HeaderComponent  } from ‘./customer/header.component’;
import {ProductComponent} from ‘./product/product.component’;
import {CustomerComponent} from ‘./customer/product.component’;

@NgModule({
   declarations: [
     AppComponent,
     CustomerComponent,
     ProductComponent,
     HeaderComponent,
     ProductHeaderComponent,
  ],
……
```

如果你想知道 Product 的 `HeaderComponent` 如何变成了 `ProductHeaderComponent`，那你可能漏掉了 TypeScript 的 import 语句。检查一下，你会发现我们在导入时指定了一个别名，这样两个 `HeaderComponent` 类型就可以同时使用了。

### 步骤 7 – 修改 header 内容

打开 `customer` 文件夹中的 `header.component.html`，放入以下内容：

1.  `<b>I am Customer Header</b>`

然后，将 product 文件夹中的 `header.component.html` 文件内容修改为：

1.  `<b>I am Product Header</b>`

### 步骤 8 – 使用组件

打开 `customer.component.html`，将内容修改为：

1.  `<p>customer works!</p><br>`
2.  `<app-header></app-header>`

打开 `product.component.html`，将内容修改为：

1.  `<p>product works!</p><br>`
2.  `<app-header></app-header>`

### 步骤 9 – 使用 Customer 和 ProductComponent

打开 `app.component.html`，将其内容替换为：

1.  `<app-customer></app-customer><hr>`
2.  `<app-product></app-product>`

### 步骤 10 – 检查输出

使用 `ng serve` 命令运行应用程序。

你将看到如下运行时错误：

试着想象一个大型企业项目，其中有多个开发人员同时工作。

![](img/Image55334.jpg)

**图 24.5**

如果我们采用单个 Angular 模块的方式，在这样的项目中很可能会出现上述错误。每个开发人员无法时刻关注应用中所有其他组件的选择器。

因此，我们采用为应用中的每个功能创建一个 Angular 模块的做法。我们将与一个功能相关的所有组件分组到一个 Angular 模块中。

### 步骤 11 – 创建 Customer 模块

使用 Angular CLI 创建一个新的 Angular 模块 `CustomerModule`，如下所示：

![](img/Image55378.jpg)

**图 24.6**

它在 `customer` 文件夹内创建了 `CustomerModule`。

![](img/Image55414.jpg)

**图 24.7**

我相信你知道为什么它的 `imports` 部分有 `CommonModule`。

`CommonModule` 是一个 Angular 模块，它封装了诸如 `*ngIf`、`*ngFor`、`ngClass` 等指令。

Angular CLI 足够智能，知道通常每个模块都需要这些指令。因此，导入它是 CLI 设计过程的一部分。如果你愿意，可以移除它，但请记住，之后 `CommonModule` 中定义的通用指令和管道将无法工作。

### 步骤 12 – 将与 Customer 相关的组件移动到 CustomerModule

从 `AppModule` 的 `declarations` 部分移除 `CustomerComponent` 和 `HeaderComponent`。

然后将它们放入 `CustomerModule` 的 `declarations` 部分，如下所示：

![](img/Image55474.jpg)

**图 24.8**

![](img/Image55482.jpg)

**图 24.9**

### 步骤 13 – 创建 ProductModule

接下来，使用 Angular CLI 创建 `ProductModule`。

![](img/Image55519.jpg)

**图 24.10**

### 步骤 14 – 将与 Product 相关的组件移动到 ProductModule

将 `ProductComponent` 和 `HeaderComponent` 都移动到 `ProductModule`。

![](img/Image55608.jpg)

**图 24.11**

![](img/Image55621.jpg)

**图 24.12**

完成此步骤后，`AppModule` 将只剩下一个组件，即 `AppComponent`。

### 步骤 15 – 检查输出

使用 `ng serve` 命令运行应用程序。你会注意到以下错误：

![](img/Image55658.jpg)

**图 24.13**

上述错误是预料之中的。原因如下：

*   此时，`CustomerComponent` 属于 `CustomerModule`。
*   规则规定，默认情况下每个组件对其所属模块是私有的。因此，`CustomerComponent` 默认对 `CustomerModule` 是私有的。
*   因此，它不能在非 `CustomerModule` 的任何组件中使用。
*   `AppComponent` 不属于 `CustomerModule`，它属于 `AppModule`。因此，`CustomerComponent` 不能在 `AppComponent` 中使用。

要使其正常工作，我们必须显式地将 `CustomerComponent` 标记为 `CustomerModule` 中的公共组件。

### 步骤 16 – 使 CustomerComponent 对 AppComponent 可见

这需要两步。首先，将 `CustomerComponent` 添加到 `CustomerModule` 的 `exports` 部分，然后在 `AppModule` 中导入 `CustomerModule`，如下所示：

![](img/Image55720.jpg)

**图 24.14**

![](img/Image55727.jpg)

**图 24.15**





在 Angular 中，当一个 Angular 模块导入另一个 Angular 模块时，前者可以访问后者中导出的所有成员。

![](img/Image55735.jpg)

**图 24.16**

**步骤 17 – 让 `ProductComponent` 对 `AppComponent` 可见**

对 `ProductComponent` 执行上述步骤。

**步骤 18 – 检查输出**

运行应用程序以获取预期输出。

因此，为每个特性创建一个模块是任何 Angular 应用程序中的推荐做法。这回答了我们的第一个问题。

# 问题 2 – 是否必须从 Angular 模块中导出每个组件？

不，你不应该这样做。

只将那些你希望在其他组件的模板中使用的组件放入 `exports` 部分。

通过不在 `exports` 部分声明其他组件，将它们保持为私有。

（请记住——一个模块中的组件彼此之间始终可见。除非标记为公共，否则它们在模块外部不可见。）

# 问题 3 – 路由呢？

即使组件是私有的，也可以通过路由访问它。

# 问题 4 – 当一个 Angular 模块导入另一个模块时会发生什么？

第二个模块中所有导出的组件在第一个模块中变为可见。

# 问题 5 – 指令和管道呢？

你学到的关于组件的所有内容同样适用于指令和管道。

每个指令和管道都将放在 `NgModule` 装饰器的 `declarations` 部分。

之后，同样的公共和私有逻辑将适用。

# 问题 6 – 从未被使用的组件会怎样？

Angular 的构建过程非常出色。

你还记得 `Injectable` 装饰器和 `Tree-shaking` 吗？

我们了解到，使用 `Injectable` 装饰器是配置模块注入器的推荐方式。

`Tree-shaking` 是在 Angular 构建过程中发生的过程。它确保如果应用程序中未使用带有 `Injectable` 装饰器的服务，则将其从最终构建中移除。

同样的 tree-shaking 过程也会处理未使用的组件、指令和管道。如果某个组件从未在任何模板中使用过，它将被从最终构建中移除。

**请注意：** 我说的是“从未在任何模板中使用过”。我从未说过“未在 Angular 模块中声明”。即使组件是 Angular 模块的一部分，只要它未在任何其他组件模板中使用，它也会从打包文件中移除。

由于 tree-shaking，打包文件的整体大小会减小。

作为开发者，你不需要对 tree-shaking 做任何操作。只需创建你的应用程序并构建它。Angular CLI 会为你处理所有繁重的工作。

# 问题 7 – tree-shaking 有什么缺点吗？

是的，有。在某些场景下，你永远不会在任何模板中使用某些组件，但你仍然希望它们成为打包文件的一部分。

**在这种情况下该怎么办？**

我们可以处理这种情况。`NgModule` 部分有一个特殊的部分叫做 `entryComponents`。

只需在该组件上声明 `entryComponents` 部分，就可以了。无论该组件是否在其他模板中使用，它都将成为最终打包文件的一部分。

```
@NgModule({
  declarations: [
    AppComponent,
    ProductComponent,
    ProductHeaderComponent, DontDeleteComponent
  ],
  imports: [BrowserModule,CustomerModule,ProductModule],
  providers: [],
  bootstrap: [AppComponent],
  entryComponents:[DontDeleteComponent]
})
export class AppModule {}
```

**现在你可能想知道，我们为什么要这样做？**

在某些场景下，我们会在代码中动态加载组件，而不是在模板中使用它们。

你能想到一个这样的场景吗？我给你一个提示。你已经做过一个这样的演示了。

那就是路由。我们是否曾在模板中的任何地方使用过那些组件？但它们仍然是打包文件的一部分。为什么？答案是 `entryComponents`。

你可能会争辩说，你从未在 `entryComponents` 部分中添加过任何组件。

我同意你的说法。你从未这样做过，但 Angular 做了。每个配置到路由中的组件都会自动添加到 `entryComponents` 数组中。

# 问题 8 – 是否有任何场景需要我们显式地将组件放入 `entryComponents` 部分？

一个用例是第三方库。有时，你可能会遇到某个第三方 Angular 库，它期望你创建一个组件并将其添加到 `entryComponents` 数组中。

# 问题 9 – 层次化导入呢？

以下两个场景将回答这个问题：

![](img/Image55773.jpg)

**图 24.17**

在这个场景中，除非 Module3 显式导入 Module1，否则 Module3 无法访问 Module1 的成员。

![](img/Image55817.jpg)

**图 24.18**

在这个场景中，Module2 重新导出了 Module1 的成员。因此，Module3 也将能够访问 Module1 的组件。

# 如果 Module1 导出了很多成员，而 Module2 想要重新导出所有这些成员怎么办？

答案是，在这种情况下，我们可以直接导出模块，而不是导出成员。

![](img/Image55876.jpg)

**图 24.19**

这意味着，除了 Module2PublicComponent 之外，Module1 中导出的每个其他成员也会被 Module2 重新导出。

你之前已经体验过一次了。

*   `BrowserModule` 内部导入了 `CommonModule`。
*   `CommonModule` 包含 `*ngFor`、`*ngIf` 和其他常用的指令。
*   `BrowserModule` 重新导出了整个 `CommonModule`。
*   因此，每个导入 `BrowserModule` 的模块也能访问 Common Module 暴露的指令。

# Angular 模块与服务

我们看到了 Angular 模块在组件中的作用。接下来，轮到服务了。

让我们做一些复习。

在关于服务的章节中，我们讨论了 Angular 注入器：

*   作为应用程序开发者，我们从不创建注入器。Angular 为我们创建它们。我们只通过 provider 配置它。
*   注入器使用该 provider 创建服务的实例。
*   Angular 创建两种注入器——元素注入器和模块注入器。
*   Angular 为每个组件创建一个元素注入器，并维护一个类似于应用程序组件树的树形层次结构。在该树中，根组件注入器位于顶部。
*   当 Angular 应用程序中需要依赖时，第一个请求将发送到关联组件的元素注入器。如果无法解析，它将转发到父组件的元素注入器，依此类推，直到依赖被解析。
*   如果所有根元素注入器都无法创建实例，它将转发到模块注入器。

![](img/Image55912.jpg)

**图 24.20**

到目前为止，在本书中，我们详细讨论了元素注入器，但谈到模块注入器时，我们只讨论了根注入器。现在是时候讨论*子模块注入器*了。

# 子模块注入器

当应用程序启动时，Angular 会创建一个*模块注入器*，称为*根注入器*。

之后，当其他 Angular 模块被懒加载时，会创建子模块注入器，从而创建一个新的树形层次结构。

让我们回答一些关于 Angular 模块与服务相关的问题。为此，我们需要一个演示应用程序。所以让我们先创建一个。

# 实验 9 – 层次化模块注入器

**步骤 1 – 创建一个项目**





使用 `ng new` 命令创建一个新项目。

当提示是否配置路由时，选择 `Yes`。

![](img/Image55950.jpg)

**图 24.21**

## 第 2 步 – 创建更多模块

按如下方式创建六个模块：

![](img/Image55988.jpg)

**图 24.22**

## 第 3 步 – 创建组件

创建 `CustomerComponent` 并将其包含到 `CustomerModule` 中，如下所示：

![](img/Image56001.jpg)

**图 24.23**

“`ng g c Customer`” – 我们在上一个演示中已经看到过它的实际应用。

这次略有不同。你注意到那个特殊的 `-m` 标志了吗？它的值是 `customer`。这意味着将新创建的组件添加到 `CustomerModule` 中。

同样地，在相应的模块中创建 `Product`、`Checkout` 和 `CheckinComponent`。

## 讨论 – 续

在实际项目中，为了保持根模块的整洁，通常会为路由创建一个单独的模块，然后将该模块导入到根模块中。

当你创建了一个配置了路由的 Angular 项目时，你会发现生成了一个名为 `app-routing.module.ts` 的文件。其内容如下：

```
import {NgModule} from ‘@angular/core’;
import {RouterModule, Routes} from ‘@angular/router’;

const routes: Routes = [];

@NgModule({
   imports: [RouterModule.forRoot(routes)],
   exports: [RouterModule],
})
export class AppRoutingModule {}
```

如果你查看 `AppModule`，你会在 `imports` 部分找到 `AppRoutingModule`。

当 `AppModule` 导入 `AppRoutingModule` 时，发生了以下两件重要的事情：

1.  `AppRoutingModule` 导出的所有内容在 `AppModule` 中变为可见。

    在当前情况下，导出的是 `RouterModule` – 这使得 `RouterModule` 导出的所有内容对 `AppModule` 的组件可见。例如，`router-outlet` 等组件和 `routerLink` 等指令可以在 `AppComponent` 模板中使用。

2.  `AppRoutingModule` 中定义的服务提供者将与 `AppModule` 中的服务提供者合并。

    你在 `AppRoutingModule` 中看到任何服务提供者了吗？

    没有，但这并不意味着 `AppRoutingModule` 的服务提供者为空。

    `AppRoutingModule` 导入了 `RouterModule`。因此，`RouterModule` 中定义的服务提供者会与 `AppRoutingModule` 的服务提供者合并。`RouterModule` 中定义的一个服务提供者是 `RouterService`，我们在 *第 11 章* 身份验证章节中已经看到过它的实际应用。

    所以最终，我们为 `RouterService` 注册了根注入器。

请在阅读完本章后重新阅读此讨论。

## 实验 – 续

## 第 4 步 – 配置根路由

在 `app-routing.module.ts` 中重新定义 routes 变量，如下所示：

```
const routes: Routes = [
   {
     path: ‘master’,
     loadChildren: () =>
       import(‘src/app/master/master.module’).then((x) => x.MasterModule),
  },
   {
     path: ‘transaction’,
     loadChildren: () =>
       import(‘src/app/transaction/transaction.module’).then((x) => x.TransactionModule),
  },
];
```

这意味着我们将懒加载 `MasterModule` 和 `TransactionModule`。

这意味着将为它们创建新的子模块注入器，并且这些注入器将成为根注入器的子级。

## 第 5 步 – 配置第二级路由

接下来，在 `MasterModule` 和 `TransactionModule` 中配置子路由，如下所示：

```
const routes: Routes = [
   {
     path: ‘customer’,
     loadChildren: () =>
       import(‘src/app/customer/customer.module’).then((x) => x.CustomerModule),
  },
   {
     path: ‘product’,
     loadChildren: () =>
       import(‘src/app/product/product.module’).then((x) => x.ProductModule),
  }
];
@NgModule({
   declarations: [],
   imports: [CommonModule, RouterModule.forChild(routes)],
})
export class MasterModule {}
```

这意味着我们将懒加载 `CustomerModule` 和 `ProductModule`。

这意味着将为它们创建新的子模块注入器，并且这些注入器将成为主模块注入器的子级。

```
import {CommonModule} from ‘@angular/common’;
import {NgModule} from ‘@angular/core’;
import {RouterModule, Routes} from ‘@angular/router’;

const routes: Routes = [
   {
     path: ‘checkin’,
     loadChildren: () =>
       import(‘src/app/checkin/checkin.module’).then((x) => x.CheckinModule),
  },
   {
     path: ‘checkout’,
     loadChildren: () =>
       import(‘src/app/checkout/checkout.module’).then((x) => x.CheckoutModule),
  }
];
@NgModule({
   declarations: [],
   imports: [CommonModule, RouterModule.forChild(routes)],
})
export class TransactionModule {}
```

这意味着我们将懒加载 `CheckinModule` 和 `CheckoutModule`。

这意味着将为它们创建新的子模块注入器，并且这些注入器将成为事务模块注入器的子级。

## 第 5 步 – 配置第三级路由

最后，定义访问所有四个模块中组件的路由，如下所示：

```
import {CommonModule} from ‘@angular/common’;
import {NgModule} from ‘@angular/core’;
import {RouterModule, Routes} from ‘@angular/router’;
import {CustomerComponent} from ‘./customer.component’;

const routes: Routes = [
   {
     path: ‘’,
     component: CustomerComponent,
  }
]
@NgModule({
   declarations: [CustomerComponent],
   imports: [CommonModule, RouterModule.forChild(routes)],
})
export class CustomerModule {}
```

```
import {CommonModule} from ‘@angular/common’;
import {NgModule} from ‘@angular/core’;
import {RouterModule, Routes} from ‘@angular/router’;
import {CheckoutComponent} from ‘../checkout/checkout.component’;

const routes: Routes = [
   {
     path: ‘’,
     component: CheckoutComponent
  }
];
@NgModule({
   declarations: [CheckoutComponent],
   imports: [
     CommonModule, RouterModule.forChild(routes)
  ]
})
export class CheckoutModule {}
```

```
import {CommonModule} from ‘@angular/common’;
import {NgModule} from ‘@angular/core’;
import {RouterModule, Routes} from ‘@angular/router’;
import {CheckinComponent} from ‘../checkin/checkin.component’;

const routes: Routes = [
   {
     path: ‘’,
     component: CheckinComponent
  }
];

@NgModule({
   declarations: [CheckinComponent],
   imports: [
     CommonModule, RouterModule.forChild(routes)
  ]
})
export class CheckinModule {}
```

```
import {CommonModule} from ‘@angular/common’;
import {NgModule} from ‘@angular/core’;
import {RouterModule, Routes} from ‘@angular/router’;
import {ProductComponent} from ‘../product/product.component’;

const routes: Routes = [
   {
     path: ‘’,
     component: ProductComponent
  }
];

@NgModule({
   declarations: [ProductComponent],
   imports: [
     CommonModule, RouterModule.forChild(routes)
  ]
})
export class ProductModule {}
```

**请注意：** 在实际项目中，懒加载需要实际实现。不要试图将所有内容都懒加载。将内容分组后再进行懒加载。我们在 *第 23 章* 路由章节中已经讨论过这一点。




例如，也许对 `Master` 和 `TransactionModule` 进行懒加载是合理的。但如果其他模块直接在这两个模块中导入，可能才是最佳做法——简而言之，就是立即加载。

（目前先别担心这个。专注于练习所有内容。）

## 第 6 步 – 设计 AppComponent

最后，我们需要一个地方来检查输出，为此，打开 `AppComponent` 并添加以下内容：

1.  `<a routerLink=”/master/customer”>Customer </a>`
2.  `<a routerLink=”/master/product”>product </a>`
3.  `<a routerLink=”/transaction/checkout”>checkout </a>`
4.  `<a routerLink=”/transaction/checkin”>checkin </a>`
6.  `<router-outlet></router-outlet>`

## 第 7 步 – 检查输出

确保你得到了预期的输出。

![](img/Image56164.jpg)

**图 24.24**

### 我们得到了什么？

我们有一个应用程序，其中模块注入器的层级结构如下：

![](img/Image56172.jpg)

**图 24.25**

# 问题 1 – 拥有注入器层级结构的真正目的是什么？

*   当 Angular 应用程序中需要某个依赖时，第一个请求会发送到关联组件的元素注入器。如果无法解析，则会转发到父组件的元素注入器，依此类推，直到依赖被解析。
*   最后，如果*根元素注入器*也无法解析该依赖，则会转发到关联模块的模块注入器。如果仍然无法解析，则会转发到父模块注入器，依此类推，直到依赖被解析。最终，如果根模块注入器也无法解析该实例，Angular 将抛出“no provider…”错误。

让我们试一试。

创建一个服务，并在 `CusomerComponent` 中使用它。

要创建服务，可以使用以下命令：

![](img/Image56249.jpg)

**图 24.26**

它将创建如下服务：

```
@Injectable({
   providedIn: ‘root’
})
export class MyTestService {
   constructor() {}
}
```

移除根中的 provider，因为我们打算用 `NgModule` 进行演示。

然后进行以下尝试：

1.  运行应用程序，你应该会收到“no provider…”错误。
2.  然后，将 provider 放入 `CustomerModule`，如下所示：

    ```
    @NgModule({
       declarations: [CustomerComponent],
       imports: [CommonModule, RouterModule.forChild(routes)],
       providers:[MyTestService]
    })
    export class CustomerModule {}
    ```

    检查输出。它应该能正常工作。
3.  然后，从 `CustomerModule` 中移除 provider，并将其放入 `MasterModule`。它应该能正常工作。
4.  然后，从 `MasterModule` 中移除 provider，并将其放入 `AppModule`。它应该能正常工作。
5.  现在，不在 `CustomerComponent` 中使用该服务，而是在 `CheckInComponent` 中使用它。这次也应该能正常工作，因为 `AppModule` 是所有模块的根。
6.  现在，从 `AppModule` 中移除 provider，将 provider 放入 `MasterModule`，并继续在 `CheckInComponent` 中使用该服务。它应该再次报错“no provider…error”。
7.  现在，将 provider 同时放入 `CustomerModule` 和 `ProductModule`。（从其他所有地方移除。）在 `Customer` 和 `ProductComponent` 中都使用该服务。它将正常工作。
8.  现在，继续在 `Customer` 和 `ProductComponent` 中使用该服务，但**仅**将 provider 放入 `MasterModule`。它将正常工作。

请随意尝试更多组合。将每个结果记录下来，以便正确分析。

第 7 次和第 8 次尝试的区别在于服务实例的数量：

*   在第 7 次尝试中，创建了两个服务实例。

    为了确认这一点，在服务的 `constructor` 中设置一个断点。你会看到断点被命中两次。
*   而在第 8 次尝试中，只创建了一个实例。位于层级结构中较高位置的注入器可以创建实例并注入到其下的所有组件中。因此，同一个实例在两个组件之间共享。这次断点只会被命中一次。

由根模块注入器创建的服务实例在整个应用程序中将是单例的。

第二级模块注入器创建的实例将在该模块的所有组件及其子组件中作为单例存在。

所以这个问题的答案是：它可以帮助我们控制 provider 的作用域。

# 问题 2 – 如果模块注入器在多个层级配置了相同的 provider，会发生什么？

让我简化这个问题。

假设在当前示例项目中，你在 `AppModule` 和 `CustomerModule` 中都为 `MyTestService` 配置了 provider。这种情况下会发生什么？

在这种情况下，会创建一个 `MyTestService` 实例，并且该实例在整个应用程序中可用。除了 `CustomerComponent` 之外，其他任何需要的地方都会注入同一个实例。对于 `CustomerModule`，会再创建一个独立的实例，并注入到 `CustomerComponent` 中。

这类似于面向对象编程中的覆盖概念。所有组件都获得同一个实例（因为它是根），但 customer 组件获得自己的实例。

（请务必亲自尝试一下。）

# 问题 3 – 当我们在一个模块中导入另一个模块时，会创建层级结构吗？

请注意，导入模块并不会创建任何层级结构。

Angular 不会为导入的模块创建单独的模块注入器。

子注入器只会在模块被懒加载时创建。

# 问题 4 – 在这种情况下，被导入模块的 provider 会怎样？

我们在本章中已经讨论过这一点——provider 会被合并到父模块的 provider 中。

例如，`AppModule` 导入的所有模块的 provider 都会被合并到 `AppModule` 的 provider 中。

请自行尝试以下演示：

*   再创建一个 Angular 模块。命名为 `ServiceModule`。
*   然后，在该 `ServiceModule` 中，为 `MyTestService` 定义 provider。
*   确保应用程序中其他任何地方都没有 provider。

现在，再次尝试问题 1 和问题 2 中的尝试，但这次不直接指定 provider，而是导入 `ServiceModule`，然后进行测试。

你会看到相同的输出，因为 provider 被合并了。

# 问题 5 – 使用 NgModule 装饰器进行配置与使用 Injectable 装饰器有何不同？

当使用 `Injectable` 装饰器进行配置时，我们可以获得摇树优化的优势，这确保了如果服务在应用程序中任何地方都没有被使用，它将被从最终打包文件中移除，从而减少整体打包文件大小。

# 问题 6 – 是否可以使用 Injectable 装饰器配置其他子模块注入器？

我们在之前的实验中已经看到了 `Injectable` 装饰器的演示，当时我们使用 `providedIn` root 方法配置了根注入器。

同样的 `Injectable` 装饰器也可以用于配置子模块注入器。请查看以下代码：

```
@Injectable({
   providedIn: TransactionModule
})
export class MyTestService {
}
```

上述代码配置了与 `TransactionModule` 关联的模块注入器。这次，服务实例只会被创建，并且在 `TransactionModule` 中作为单例存在。

其他任何模块都无法访问它。

我建议你用这种方法尝试问题 1 和问题 2 中的所有八次尝试。

# 问题 7 – 如果某个特定需求可以通过两种方法（即 NgModule 装饰器和 Injectable 装饰器）实现，那么在这种情况下，推荐使用哪种方法？

答案是 `Injectable` 装饰器，因为它支持摇树优化。

# 问题 8 – 既然如此，配置 NgModule 装饰器似乎毫无用处；为什么我们还要保留它？




这是由于以下两个原因：

1.  可注入装饰器不允许我们显式指定 `DI token`。当有这种需求时，我们必须使用 `NgModule` 装饰器。请回想本书中的 *第 17 章：令牌拦截器* 和 *第 21 章：错误处理器*。

2.  假设你正在创建一个 Angular 库，供其他人下载和使用。

    假设该库包含一个名为 `NotificationService` 的服务，其他人将使用它。`NotificationService` 依赖于 `EmailService`，而 `EmailService` 又依赖于 `ConfigService`。

    在这种情况下，想要使用 `NotificationService` 的人必须下载该库，然后为 `NotificationService`、`EmailService` 和 `ConfigService` 配置注入器。

    对于开发者来说，了解所有依赖项是相当具有挑战性的，尤其是在涉及第三方库时。

    试想一下，当服务的依赖层级更加复杂时。

    更好的做法是：创建服务的开发者同时创建一个 Angular 模块，并为所有三个服务配置提供者。

    想要使用该服务的人只需在自己的模块中导入该模块即可。

    你还记得 `HTTPClientModule` 吗？我们在模块中导入了它，这使得根模块为 `HTTPService` 和所有其他依赖服务完成了配置。

这两个用例无法通过 `Injectable` 装饰器覆盖。

如果你需要一个模块注入器，我的建议是：尽可能使用 `Injectable` 装饰器。

如果你是库开发者，或者想要指定一个 DI Token，那么请显式使用 `NgModule` 装饰器。

#### 总结

至此，*第 24 章* 结束，我们来到了第 13 站。在你能自称 Angular 开发者之前，还有 7 站需要学习。让我们回顾一下本章涵盖的主题：

*   我们学习了如何使用 Angular CLI 创建组件和模块。

*   我们学习了 Angular 模块如何使组件开发更加容易。我们将相关组件分组到模块中，然后只导出其中一部分作为公共组件。我们了解到，Angular 模块中未导出的组件对该模块来说是私有的。

*   我们学习了 Angular 模块也对指令和管道进行分组，除非显式导出，否则它们对该模块是私有的。

*   我们学习了 `ServiceModules`，它们是专门用于为服务和依赖服务配置注入器的 Angular 模块。`HttpClientModule` 就是这样一个 `ServiceModule` 的例子。

*   我们在上一章已经讨论了 Angular 模块的第三个优势——惰性加载。

*   我们了解到，即使是 Angular 模块的私有组件也可以通过路由访问。

*   我们学习了 `BrowserModule` 导入 `CommonModule` 并重新导出它。因此，`CommonModule` 导出的指令在 `AppModule` 内部是可见的。

*   我们学习了 Angular 构建过程中的树摇机制确保所有未使用的组件从最终构建中移除，除非它们通过路由被引用。如果某个组件未在任何其他组件的模板中使用，它将被视为未使用。

*   我们学习了当模块被惰性加载时，Angular 会创建一个子模块注入器。

## 第 25 章

## Angular 管道

## 引言

好吧，在前往第 14 站的旅程中，我们将学习 Angular 管道。

到目前为止，你已经看到了两个内置管道的实际应用——`async` 和 `JSON`。

## 什么是管道？

在 Angular 中，我们使用管道来转换数据。

假设我们有一些数据在显示之前需要转换。这时你就需要 Angular 管道。每当你觉得数据需要转换后再显示在项目中时，就为此创建一个管道。

以下是常用的用于数据格式化的内置管道：

*   `DatePipe`：根据区域规则格式化日期值。

*   `UpperCasePipe`：将文本转换为全大写。

*   `LowerCasePipe`：将文本转换为全小写。

*   `CurrencyPipe`：将数字转换为货币字符串，根据区域规则格式化。

*   `DecimalPipe`：将数字转换为带小数点的字符串，根据区域规则格式化。

*   `PercentPipe`：将数字转换为百分比字符串，根据区域规则格式化。

你已经知道使用管道的语法。

我强烈建议你自己用前面列出的几个管道快速做一个演示——在视图类中声明一个变量并在视图中显示它。

1.  `Name= “Sukesh Marla”;`

2.  `…`

3.  `{{Name | uppercase}}`

如果我们创建一个自定义管道，那会很有趣。那么，让我们开始吧。

## 实验 10 – 自定义管道实战 – 演示 1

在这个演示中，我们将创建一个自定义管道，将字节转换为 KB、MB、GB……

**步骤 1 – 创建项目**

使用 Angular CLI 创建一个新的 Angular 项目。

1.  `ng new lab10-ng`

**步骤 2 – 修改 AppComponent**

在视图类中声明一个带有初始值的数值属性，并使用插值在模板中显示它。

```
export class AppComponent {
   SomeValue: number = 2456;
}
{{SomeValue}}
```

**步骤 3 – 检查输出**

使用 `ng serve` 命令执行应用程序，确保一切正常。

![](img/Image56345.jpg)

**图 25.1**

**步骤 4 – 创建管道**

使用以下命令创建新管道：

![](img/Image56352.jpg)

**图 25.2**

这将生成一个新文件 `file-size.pipe.ts`，内容如下：

```
import {Pipe, PipeTransform} from ‘@angular/core’;

@Pipe({
   name: ‘fileSize’
})
export class FileSizePipe implements PipeTransform {

   transform(value: unknown, …args: unknown[]): unknown {
     return null;
   }
}
```

## 讨论 – 续

**让我们探索执行 CLI 命令后生成的代码。**

该命令创建了一个新文件 `file-size.pipe.ts`，并在 `app.module.ts` 中做了一些更改。让我们探索两者。

`file-size.pipe.ts`

*   我们有一个 TypeScript 类，名为 `FileSizePipe`。

*   该类实现了一个接口 `PipeTransForm`——**创建管道的第一个步骤**。

*   实现该接口迫使我们定义 `transform` 方法。（暂时忽略 `return null`。）

*   该类使用了 `Pipe` 装饰器——**创建管道的第二个步骤**。

*   检查 `Pipe` 装饰器中的 `name` 属性。这就是我们稍后在模板中要使用的名称。

`app.module.ts`

最后，打开 AppModule，你会看到 `FileSizePipe` 被包含在 `NgModule` 装饰器的 `declarations` 部分。

与组件类似，Angular 中的每个管道都被分组在一个 Angular 模块内。如果你在一个模块中创建了一个管道，并希望它在另一个模块中使用，那么第一个模块需要导出它。

**CommonModule**

常用的 Angular 内置管道，如 `uppercase`、`async`、`json`，都是 `CommonModule` 的一部分。

**自定义管道和 AppModule**

在实际项目中，我们不会将自定义管道添加到 AppModule。我们会有一个单独的模块，在需要的地方导入它。这样的模块被称为 SharedModules。

**unknown 数据类型**

我知道你内心的开发者正在为前面代码中的 `unknown` 数据类型而困扰。

TypeScript 中有两种特别的数据类型用于动态编码——`any` 和 `unknown`。

它们之间的相似之处如下：

任何值都可以赋值给它们两者。



```
let a: any = 100;      // 我们可以将任何值赋给 any

let b: unknown =  1000; // 我们可以像 any 一样将任何值赋给 unknown
```

它们之间的区别如下：

`any` 可以赋值给任何类型。`unknown` 不能赋值给任何类型。

`let s1: string = a;`     // any 可以赋值给任何类型

`let s2: string = b;` // 无效，我们不能将 `b` 赋值给任何其他类型（除非显式断言）

## 实验 – 继续

**第 5 步 – 修改管道逻辑**

按如下方式修改 transform 方法：

```
transform(value: number, …args: number []): string {
     return ‘Just Compile’;
}
```

你是否注意到我们将 `unknown` 改为了其他数据类型？始终指定确切的数据类型是最佳实践。

**第 6 步 – 应用管道**

打开 `AppComponent` 模板，并按如下方式应用管道：

```
{{SomeValue |fileSize}}
```

**第 7 步 – 检查输出**

执行应用程序，你应该会得到以下输出：

![](img/Image56437.jpg)

**图 25.3**

无论 `SomeValue` 变量的值是什么，你都会得到上述输出，因为 transform 方法没有返回任何动态内容。

**第 8 步 – 修改管道逻辑**

现在是时候将真正的逻辑放入管道中了——修改 transform 方法。

```
transform(value: number, …args: number[]): string {
     let data = ‘’;
     if (value > (1024 * 1024 * 1024)) {
         data = (value / 1024 / 1024 / 1024).toFixed(2) + ‘ GB’;
    } else if (value > (1024 * 1024)) {
         data = (value / 1024 / 1024).toFixed(2) + ‘ MB’;
    } else if (value > 1024) {
         data = (value / 1024).toFixed(2) + ‘ KB’;
    } else {
         data = value + ‘ B’;
    }
     return data;
}
```

这一次，我们返回的是动态值，而不是固定值。

**第 9 步 – 检查输出**

执行应用程序。

多做几次测试。将值改为更大的数值并检查输出。

![](img/Image56444.jpg)

**图 25.4**

## 实验 11 – 自定义管道实战 – 演示 2

这次我们将创建一个管道，通过将数据与其他值拼接来转换数据。

**第 10 步 – 为演示更新 AppComponent**

在 AppComponent 中创建三个 string 类型的属性，并在模板中按如下方式显示它们：

```
export class AppComponent {
   SomeValue: number = 2456;
   FirstName: string= “Sukesh”;
   MiddleName: string= “Nagesh”;
   LastName: string= “Marla”;
}
```

```
{{SomeValue |fileSize}}<br>
Full name :{{FirstName}} - {{MiddleName}} - {{LastName}}
```

**第 11 步 – 检查输出**

![](img/Image56522.jpg)

**图 25.5**

你可以看到三个值被拼接并显示在 UI 中。目前，转换逻辑或拼接逻辑是作为模板的一部分编写的。这是一种不好的做法。对于这种情况，我们需要一个管道。

**第 12 步 – 创建管道**

按如下方式创建 concat 管道：

![](img/Image56595.jpg)

**图 25.6**

**第 13 步 – 实现 transform 逻辑**

如你所知，transform 方法中的第一个参数代表管道所附加的数据。

我们当前的需求需要多个值，这就是第二个参数发挥作用的地方。

按如下方式重新定义 transform 方法：

```
export class ConcatPipe implements PipeTransform {
   transform(value: string, …args: string[]): string {
     args.forEach((x) => {
       value = value + ‘-’ + x;
    });
     return value;
  }
}
```

**第 14 步 – 应用管道**

将 `AppComponent` 模板修改为以下内容：

```
……
Full name :{{FirstName |concat: MiddleName: LastName  }}
```

如你所见，我们将 concat 管道应用于 `FirstName`，然后将 `MiddleName` 和 `LastName` 作为参数传递。

**第 15 步 – 检查输出**

你将得到相同的输出，但这次拼接逻辑（转换逻辑）是写在管道内部的。

## 我的经验

几乎在我做的每一个咨询项目中，我都会发现一个常见问题。大多数情况下，转换逻辑要么写在组件类中，要么写在模板中。有时，我甚至发现转换逻辑作为服务的一部分编写。这是一种不好的做法。对于任何转换逻辑，请使用管道。

## 非纯管道

关于管道，我们还没有讲完。到目前为止，我们看到的都是纯管道。还有另一种管道——非纯管道。接下来让我们理解它。

*在 Angular 中，变更检测是在数据发生变化时更新 DOM 的过程。我们将在接下来的章节中详细讨论它。当 DOM 事件（如点击、聚焦等）发生时，或者当 HTTP 请求完成时，甚至在某些 API（如 `setTimeout` 和 `setInterval`）执行完成后，变更检测就会执行。*

如果谈到管道，那么管道只会在它所附加的值发生变化时执行**。它不会在每次变更检测时都运行。**

让我们讨论一个场景——我们有数据，并且希望根据本地存储中的某些数据来转换这些数据。假设 UI 中有一个按钮，它会改变本地存储的值。按钮点击后，变更检测会执行，但由于管道所附加的值没有改变，我们的管道不会重新执行。因此，我们不会得到期望的输出。

如果前面这段话不太准确，别担心。让我们通过演示来理解它。

## 实验 12 – 理解非纯管道

**第 16 步 – 创建管道**

使用 CLI 创建一个名为 ImpureTest 的新管道。

![](img/Image56606.jpg)

**图 25.7**

**第 17 步 – 重新定义 transform**

按如下方式重新定义 transform 方法：

```
transform(value: number, …args: number[]): number {
     if (localStorage.myValue) {
       return value + parseInt(localStorage.myValue);
    } else {
       return value;
    }
  }
```

**第 18 步 – 设置 AppComponent**

首先，在 `AppComponent` 类中声明一个简单的变量，如下所示：

```
Counter: number = 20;
```

接下来，在模板中显示该变量，并附加 `impureTest` 管道，如下所示：

```
Counter: {{Counter | impureTest}}
```

然后，在模板中创建一个按钮，如下所示：

```
<input type=”button” value=”Click Me” (click)=”HandleClick()”>
```

最后，按如下方式定义 `HandleClick` 方法：

```
   HandleClick() {
     if (!localStorage.myValue) {
       localStorage.myValue = 1;
    } else {
       localStorage.myValue = parseInt(localStorage.myValue) + 1;
    }
  }
```

请注意，每次点击按钮时，我们都会将本地存储的值增加 1，但我们并没有改变变量 `counter` 的值。

**第 19 步 – 检查输出**

执行应用程序。最初，你会看到基于当前本地存储值的结果。

之后，无论你点击按钮多少次，本地存储的值都会改变，但 UI 永远不会改变。

## 讨论 – 继续

不要以为变更检测没有执行。它确实执行了。

问题在于管道没有执行，因为 `counter` 变量的值没有改变。

这是因为它是一个纯管道。

如果你希望管道在每次变更检测时都执行，你必须将其设置为 `impure`（非纯）。

## 实验 – 继续

**第 20 步 – 将管道设为非纯**

按如下方式将纯管道转换为非纯管道：

```
@Pipe({
   name: ‘impureTest’,
   pure:false
})
export class ImpureTestPipe implements PipeTransform {
```

**第 21 步 – 检查输出**

现在，检查输出。它将正常工作。

以上就是关于管道的全部内容。





#### 总结

通过本章，我们离完成旅程又近了一站。第 15 站——自定义指令之旅将在下一章等待你。

让我们回顾一下本章内容：

*   在本章中，我们学习了管道，它帮助我们封装应用程序中的转换逻辑。
*   我们了解到，创建管道需要创建一个类，实现`PipeTransform`接口，然后附加`Pipe`装饰器。
*   我们了解到，管道也像组件一样被封装在 Angular 模块中。
*   我们了解到，Angular 应用程序中常用的管道（如`json`、`async`、`uppercase`等）定义在`CommonModule`中。
*   我们了解到，自定义 Angular 模块（通常称为`SharedModule`）用于封装所有自定义管道，其他模块在实际项目中会导入这些模块。
*   我们讨论了 TypeScript 中两种数据类型——`any`和`unknown`的区别。我们了解到，`any`类型的变量可以赋值给其他类型，而`unknown`类型的变量只能赋值给`unknown`类型的变量。
*   我们演示了 TypeScript 的 REST 参数。
*   我们了解到，纯管道仅在开始时以及输入值发生变化时执行。
*   我们了解到，非纯管道在每次变更检测后都会执行。

## 第 26 章

## Angular 指令

## 引言

在前往第 15 站的旅程中，我们将再次讨论 Angular 指令。

到目前为止，我们已经探索了 Angular 中许多内置指令。现在是时候创建一些我们自己的指令了。

## 什么是指令？

在 Angular 世界中，指令是一种扩展 HTML 的方式。

在 Angular 中，我们会发现以下三种指令之一：

1.  元素指令
2.  属性指令
3.  结构型指令

**元素指令**在 Angular 中也称为组件。你已经看到许多演示，我们创建了一个 Angular 组件，从而创建了一个自定义 DOM 元素。

![](img/Image56697.jpg)

**图 26.1**

**属性指令**用于增强任何 DOM 元素的现有行为。`NgClass`和`NgStyle`就是最好的例子。

**结构型指令**用于当我们想要塑造或重塑现有 DOM 元素的结构时，通常通过添加、操作或移除元素来实现。`NgFor`和`NgIf`就是最好的例子。

让我们对自定义属性指令和结构型指令都做一个演示。

## 实验 11 – 鼠标悬停指令

在本实验中，我们将创建一个自定义指令，该指令将添加在鼠标悬停时更改元素背景颜色的能力。

**步骤 1 – 创建一个新的 Angular 项目**

按如下方式创建一个新的 Angular 项目：

1.  `ng new lab11-ng`

**步骤 2 – 创建一个新的指令**

按如下方式创建一个新的 Angular 指令：

![](img/Image56747.jpg)

**图 26.2**

这将创建一个包含以下内容的 TypeScript 文件：

```typescript
import {Directive} from '@angular/core';

@Directive({
   selector: '[appMouseOver]'
})
export class MouseOverDirective {
   constructor() {}
}
```

## 讨论 – 继续

上述代码非常直接。有一个用`Directive`装饰器装饰的类。你注意到`selector`中的方括号了吗？这非常重要。我们将在本演示之后进一步讨论。

## 实验 – 继续

**步骤 3 – 添加测试代码**

在指令的构造函数中编写一个简单的`console.log`语句，如下所示：

```typescript
export class MouseOverDirective {
   constructor() {
     console.log('Hello world')
  }
}
```

**步骤 4 – 附加指令**

打开`AppComponent`并创建一个 HTML 元素，然后按如下方式附加上述指令：

![](img/Image56788.jpg)

**图 26.3**

**步骤 5 – 执行应用程序**

执行应用程序并检查输出。

![](img/Image56826.jpg)

**图 26.4**

你能在控制台中找到两次“Hello world”吗？

我们将指令应用于两个控件（一个应用于 span 元素，一个应用于 input 元素），因此创建了两个指令类实例，因此消息显示了两次。

## 讨论 – 继续

接下来，我们需要访问指令所附加的元素，为此，Angular 提供了一个名为`ElementRef`的服务。`ElementRef`提供了对指令所附加的`nativeDOM element`的包装。

一旦获得了元素引用，就可以使用另一个 Angular 服务`Renderer2`来操作它。

## 实验 – 继续

**步骤 6 – 在指令中访问和操作元素**

将这两个服务注入到类中，然后按如下方式修改控件的背景颜色：

```typescript
export class MouseOverDirective {
   constructor(el: ElementRef, renderer: Renderer2) {
     renderer.setStyle(el.nativeElement, 'background', 'red');
  }
}
```

***注意：*** 尽管`ElementRef`允许直接操作相应的元素，但不推荐这样做。对于所有操作，建议使用`Renderer2`服务。

**步骤 7 – 检查输出**

这次你将看到更新了颜色的控件。

![](img/Image56863.jpg)

**图 26.5**

## 讨论 – 继续

让我们理解下一步。

目前，我们在指令中硬编码了颜色。在下一步中，让我们使其动态化，为此我们将使用`inputproperty`。

正如我之前所说，组件也是指令。因此，你会发现它们之间有很多相似的功能，例如输入和输出属性、生命周期事件等。

## 实验 – 继续

**步骤 8 – 创建一个输入属性**

在指令中为颜色创建一个新的输入属性，并使用它代替硬编码的值。

```typescript
import {Directive, ElementRef, Input, Renderer2} from '@angular/core';

@Directive({
   selector: '[appMouseOver]'
})
export class MouseOverDirective {
   @Input() color:string= 'red';
   constructor(el: ElementRef, renderer: Renderer2) {
     renderer.setStyle(el.nativeElement, 'background', this.color);
  }
}
```

**步骤 9 – 为输入属性赋值**

接下来，在`app.component.html`文件中为上述输入属性赋值，如下所示：

```html
<span appMouseOver color="blue">My Span 1</span><br>
<input type="button" value="I am button" appMouseOver color="yellow">
```

## 讨论 – 继续

组件的输入属性在模板中绑定到 DOM 属性。

默认情况下，Angular 认为 DOM 属性名称和输入属性名称相同。

这就是为什么`input`控件的 DOM 属性`color`映射到了`MouseOverDirective`中的输入属性`color`。

## 实验 – 继续

**步骤 10 – 检查输出**

这次你期望元素显示蓝色和黄色吗？如果是，那将会令人失望，因为两者仍然会显示为红色。

## 讨论 – 继续

想知道为什么吗？我们之前曾经提到过。

*构造函数在创建类的实例时执行。*

对于组件和指令来说，`constructor`并不是编写初始化逻辑的理想位置。`constructor`在实例创建后立即执行。此时，输入属性尚未设置为从父组件传递的值。

`ngOnInit`是执行此类逻辑的理想位置。

## 实验 – 继续

**步骤 11 – 实现`ngOnInit`**

接下来，在组件中定义`ngOnInit`方法，如下所示：

```typescript
import {Directive, ElementRef, Input, OnInit, Renderer2}
```





```
from '@angular/core';
……
export class MouseOverDirective implements OnInit {
   @Input() color:string= 'red';
   constructor(private el: ElementRef, private renderer: Renderer2) {
  }
   ngOnInit(): void {
     this.renderer.setStyle(this.el.nativeElement, 'background', this.color);
  }
}
```

**第 12 步 – 运行应用程序。**

这次你将看到带有新颜色的控件。

## 讨论 – 继续

你对目前为输入属性赋值的方式满意吗？

如果我们能实现类似下面的效果呢？

1.  `<span mouse-over-color=”blue”>My Span 1</span><br>`
2.  `<input type=”button” value=”I am button”  mouse-over-color=”yellow”>`

看起来是不是更好？如果是，那么这就是我们接下来要做的。

## 实验 – 继续

**第 13 步 – 重新定义输入属性**

首先，按如下方式向输入装饰器传递参数：

1.  `   @Input(‘mouse-over-color’) color:string= ‘red’;`

执行上述代码后，我们需要将 `AppComponent` 的代码修改为以下内容：

1.  `<span appMouseOver mouse-over-color=”blue”>My Span 1</span><br>`
2.  `<input type=”button” value=”I am button” appMouseOver mouse-over-color=”yellow”>`

## 讨论 – 继续

通过向 `Input` 装饰器传递参数，我们指示 Angular 进行不同的映射。

现在，输入属性 `color` 被映射到 DOM 属性 `mouse-over-color`。我们使用参数化的 `Input` 装饰器，以不同的名称将指令的属性暴露给外部世界。

## 实验 – 继续

**第 14 步 – 检查输出**

重新检查你的更新。它必须与之前相同。

**第 15 步 – 修改选择器**

接下来，将指令选择器重新定义为 `mouse-over-color`，如下所示：

```
……
@Directive({
selector: '[mouse-over-color]' // （确保不要漏掉方括号。）
})
export class MouseOverDirective implements OnInit {
   @Input('mouse-over-color') color:string= 'red';
……
```

## 讨论 – 继续

你注意到我们的选择器和 `Input` 属性现在相同了吗？

如果注意到了，说明你关注到了所有细节；否则，你需要提高注意力。😊

## 实验 – 继续

**第 16 步 – 修改 `AppComponent`**

接下来，将 `AppComponent` 的代码修改为以下内容：

1.  `<span mouse-over-color=”blue”>My Span 1</span><br>`
2.  `<input type=”button” value=”I am button” mouse-over-color=”yellow”>`

**第 17 步 – 检查输出**

重新检查你的更新。它必须与之前相同。

## 讨论 – 继续

接下来呢？输出看起来是否像我们之前的目标？我们不是期望在鼠标悬停时颜色发生变化吗？让我们来画上最后的句号。

在 Angular 中，我们可以使用名为 `HostListener` 的装饰器来处理宿主事件。

这里，宿主指的是使用它的元素。

对于指令而言，宿主就是指令所附加到的元素。

## 实验 – 继续

**第 18 步 – 处理鼠标悬停和鼠标离开事件**

在指令类中定义两个方法，并在它们上面附加 `HostListener` 装饰器，如下所示：

```
ngOnInit(): void {
  }
   @HostListener('mouseover')
   OnMouseOver(){
     this.renderer.setStyle(this.el.nativeElement, 'background', this.color);
  }
   @HostListener('mouseleave')
   OnMouseLeave(){
     this.renderer.setStyle(this.el.nativeElement, 'background', '');
  }
```

使用 `HostListener` 装饰器，我们可以监听指令宿主的事件。

**第 19 步 – 检查输出**

这次你会发现，当光标移到该元素上时，颜色会发生变化。

这是一个简单的演示，展示了如何创建自定义属性指令来增强现有 HTML 元素的现有行为。这被称为**属性指令**。

## 不同类型的指令选择器

我知道你一直在等待关于我们在选择器中使用的那些方括号的答案。

事实上，方括号只是指定选择器的一种方式——还有更多方式。

**属性选择器**

在前面的例子中，我们为指令指定了选择器 `[mouse-over-color]`。

这是一个属性选择器的例子——指令将附加到每个带有 `mouse-over-color` 属性的 DOM 元素上。

**CSS 选择器**

请看以下代码：

```
@Directive({
   selector: '.abc'
})
export class MouseOverDirective
```

这是 CSS 选择器。指令将附加到 DOM 中每个具有 CSS 类 `abc` 的元素上。例如，它将附加到以下元素：

1.  `<input type=”button” value=”I am button” class=”abc”>`

**元素选择器**

请看以下代码：

```
@Directive({
   selector: 'input'
})
export class MouseOverDirective{}
```

这是元素选择器。指令将附加到 DOM 中的每个 `input` 元素上。

例如，它将附加到以下两个元素：

1.  `<input type=”button” value=”I am button”>`
2.  `<input type=”text” value=”I am button”>`

**ID 选择器**

请看以下代码：

```
@Directive({
   selector: #MyId
})export class MouseOverDirective{}
```

这是 ID 选择器。指令将附加到每个具有 id 属性且值为 `MyId` 的元素上。

例如，它将附加到第一个 input 元素，如下所示：

1.  `<input id=”MyId” type=”button” value=”I am button”>`
2.  `<input type=”tex” value=”I am button”>`

## 实验 12 – 创建 OnlyIfUserIsAuthorizedDirective 指令

在实验 12 中，我们将创建一个结构型指令，如果当前登录用户的角色不是授权用户，该指令将用一个自定义的 *HTML div 元素* 替换 *HTML 元素*。

**第 1 步 – 创建新指令**

创建一个新的 Angular 指令 `OnlyIfUserIsAuthorizedDirective`，如下所示：

![](img/Image57103.jpg)

**图 26.6**

**第 2 步 – 运行应用程序**

在 `AppComponent` 中添加一个新的输入按钮，并将上述指令附加到它上面。

1.  `<input type=”button” value=”Add new record” appOnlyIfUserIsAuthorized >`

然后，在指令的构造函数中放入一条“*hello world*”消息，并确认到目前为止一切正常（类似于之前的实验测试）。

**第 3 步 – 注入必要的服务**

正如我们已经讨论过的，需求是当用户未授权时，移除按钮元素并放入一个 HTML span 元素。为此，像之前一样将 `ElementRef` 和 `Renderer2` 服务注入到指令中。

```
export class OnlyIfUserIsAuthorizedDirective implements OnInit {
   constructor(private ele: ElementRef,private renderer: Renderer2) {……}
```

**第 4 步 – 定义授权逻辑**

将以下代码放入 `ngOnInit` 方法中：

```
  ngOnInit(): void {
     const isAuthorized = true;
     if (localStorage.IsAuthorized !== 'true') {
       const pNode = this.renderer.createElement('div');
       const txtNode = this.renderer.createText('Not authorized!!!');
       this.renderer.appendChild(pNode, txtNode);
       this.renderer.appendChild(this.ele.nativeElement.parentElement, pNode);
       this.renderer.removeChild(this.ele.nativeElement.parentElement,this.ele.nativeElement);
    }
  }
```

## 讨论 – 继续

根据代码，如果本地存储包含 *false* 值，一个元素将被替换为一个 *HTML div 元素*。让我们逐步分析代码：

1.  首先，我们创建了一个 *HTML div 元素*。
2.  然后，我们创建了一个简单的文本。
3.  接着，我们将文本追加到 *div 元素* 中。





4.  接下来，我们将 *HTML div* 元素追加到当前元素的父元素上。（当前元素指的是我们附加了指令的那个元素。）

5.  最后，我们移除了当前元素。

（我们假设本地存储中保存了一个值，用于指示用户是否已授权。）

## 实验 – 继续

### 步骤 5 – 执行应用程序

执行应用程序，并确认当本地存储中包含 `false` 值时，按钮元素会自动从 DOM 中移除。

![](img/Image57173.jpg)

**图 26.7**

显式更改本地存储中的值，然后刷新页面以查看不同的输出。

（我们没有任何界面可以将本地存储的值更改为 `true` 或 `false`。请手动使用 Chrome 开发者工具进行操作？为此，打开开发者工具，转到 `Application` 选项卡，然后从左侧部分选择 `Local Storage`。）

## 讨论 – 继续

**你觉得这看起来像一个具有不同逻辑的属性型指令吗？**

如果你的答案是肯定的，那么你是对的。

**我们是否说过在本实验开始时我们将创建一个结构型指令？**

是的，我们说过了。

从逻辑上讲，属性型指令和结构型指令都是作为属性附加到现有元素上的。它们根据用途进行区分：一个添加某些行为，另一个修改结构。通常，你会发现所有结构型指令都使用星号（`*`）符号编写。

我们很快就会探讨星号（`*`）背后的秘密。

## 实验 – 继续

### 步骤 6 – 添加更改授权的按钮

手动更改本地存储的值一定非常烦人。因此，让我们在 `AppComponent` 中为此创建一个输入按钮，如下所示：

```
  <input type=”button” value=”Change Authorization” (click)=”Change()”>
  CurrentValue:{{CurrentAuthorization}}<br>
  <input type=”button” value=”Add new record” appOnlyIfUserIsAuthorized >
  ……
  export class AppComponent {
     title = ‘lab11-ng’;
     CurrentAuthorization = localStorage.IsAuthorized;
     Change(): void {
         localStorage.IsAuthorized =
  localStorage.IsAuthorized === ‘true’ ? false : true;
        this.CurrentAuthorization = localStorage.IsAuthorized;
    }
  }
```

这是一个简单的代码。每次单击按钮时，本地存储中的值都会被反转。

### 步骤 7 – 执行应用程序

你会惊讶地发现，单击按钮后，DOM 中的授权部分不会改变。执行硬刷新，你会看到变化。

![](img/Image57180.jpg)

**图 26.8**

## 讨论 – 继续

**上述情况的确切原因是什么？**

到目前为止，我们已将 DOM 操作逻辑写在 `ngOnInit` 中。

`ngOnInit` 是一个 Angular 生命周期事件，在 Angular 指令初始化时执行。初始化仅在开始时发生一次，这意味着 `ngOnInit` 只执行一次。单击按钮后，该代码不会运行，因此 UI 不会改变。

我们需要其他东西。有一个名为 `ngOnChanges` 的事件。让我们尝试一下。

## 实验 – 继续

### 步骤 8 – 实现 ngOnChanges

不要从 `OnInit` 接口实现，而是从 `OnChanges` 接口实现指令。然后，按如下方式定义 `ngOnChanges` 方法：

```
ngOnChanges(changes: SimpleChanges): void {
     const isAuthorized = true;
     if (localStorage.IsAuthorized !== ‘true’) {
       const pNode = this.renderer.createElement(‘div’);
       const txtNode = this.renderer.createText(‘Not authorized!!!’);
       this.renderer.appendChild(pNode, txtNode);
       this.renderer.appendChild(this.ele.nativeElement.parentElement, pNode);
       this.renderer.removeChild(this.ele.nativeElement.parentElement,this.ele.nativeElement);
    }
  }
```

### 步骤 9 – 检查输出

这同样无法达到目的。经过上述更改后，输出不会改变。

## 讨论 – 继续

**ngOnChanges**

`ngOnChanges` 在 `ngOnInit` 方法之后执行一次，之后当指令的数据绑定属性发生变化时，它会被执行。

目前，我们的指令没有任何数据绑定属性，因此 `ngOnChanges` 仅在开始时执行。

**ngDoCheck 解决方案**

我们确实有一个专门用于此类情况的独特生命周期方法——`ngDoCheck`。

它会在每次变更检测时执行。

现在不必担心变更检测。只需理解变更检测负责更新 DOM，并且在 DOM 事件发生后自动发生。

让我们回顾一下到目前为止我们看到的所有生命周期事件。

*   `Constructor` 和 `ngOnInit` 仅在组件或指令构建时执行一次。

    （请注意，`ngIf` 指令和路由会根据需要销毁和创建组件/指令。这两个方法在每次创建组件/指令时都会执行。）

*   `ngOnChanges` 在 `ngOnInit` 方法之后运行一次，之后当指令的数据绑定属性发生变化时，它会被执行。

*   `ngAfterViewInit` 在视图完全初始化后执行。当你需要访问组件中的 DOM 元素时使用它。（还记得 *第 22 章* 中的焦点示例吗？）

*   `ngDestroy` 在组件/指令被销毁时执行，用于清理操作。（还记得我们销毁订阅的示例吗？）

*   `ngDoCheck` 在每次变更检测时执行。

对于我们的情况，`ngDoCheck` 最合适。

### 步骤 10 – 实现 ngDoCheck

移除 `ngOnChanges` 并添加 `ngDoCheck`，如下所示：

```
export class OnlyIfUserIsAuthorizedDirective implements DoCheck {
   constructor(
     private ele: ElementRef,
     private renderer: Renderer2
  ) {}
   ngDoCheck(): void {
     const isAuthorized = true;
     if (localStorage.IsAuthorized !== ‘true’) {
       const pNode = this.renderer.createElement(‘div’);
       const txtNode = this.renderer.createText(‘Not authorized!!!’);
       this.renderer.appendChild(pNode, txtNode);
       this.renderer.appendChild(this.ele.nativeElement.parentElement, pNode);
       this.renderer.removeChild(this.ele.nativeElement.parentElement,this.ele.nativeElement);
    }
  }
}
```

### 步骤 11 – 检查输出

现在按如下方式测试应用程序：

1.  打开开发者工具，将 `IsAuthorized` 本地存储的值更改为 `true`。

2.  现在刷新浏览器。你应该能够看到授权部分。

3.  现在单击 `Change Authorization` 按钮。它将反转本地存储的值，使授权部分被替换为“`Not authorized!!!`”消息。

4.  现在再次单击 `Change Authorization` 按钮。奇怪的是，你无法恢复授权部分。如果你检查本地存储中的值，会发现它已更新为 `true`。

5.  再次单击 `Change Authorization` 按钮。你会在控制台中发现以下错误：

    ![](img/Image57341.jpg)

    **图 26.9**

## 讨论 – 继续

**这里到底发生了什么？**

当用户未授权时，元素会从 DOM 中**移除**，并插入新元素。

**移除**是一个关键词。由于它被移除了，下次将不再可用，这就是导致之前显示的奇怪输出的原因。

使用指令处理 DOM 操作场景的最佳方法是使用 `ViewContainerRef` 和 `TemplateRef` 服务。

让我们先看看它的实际效果，然后进行详细讨论。





## 实验 – 续

### 步骤 12 – 将新服务注入指令

在指令中注入 `ViewContainerRef` 和 `TemplateRef`，并按如下方式移除 `ngDoCheck` 中的代码：

```
constructor(
     private vc: ViewContainerRef, private tc: TemplateRef<any>) {}
   ngDoCheck(): void {
  }
```

### 步骤 13 – 将授权内容包裹在 ng-template 中

在 `AppComponent` 中，将授权内容包裹在 ng-template 内，如下所示：

```
<ng-template>
   <input type=”button” value=”Add new record” >
</ng-template>
```

暂时不用担心 `appOnlyIfUserIsAuthorized` 指令。我们很快就会让它重新发挥作用。

### 步骤 14 – 检查输出

你会发现，无论用户是否被授权，ng-template 内部的内容都不会渲染到屏幕上。

你可能会认为这些内容默认应该被渲染。

但事实并非如此，我们来讨论一下原因。

## 讨论 – 续

## ng-template、TemplateRef 和 ViewContainerRef

`ng-template` 指令代表一个 Angular 模板。

通常，模板指的是一种 DOM 结构，它本身不会独立存在。它们会在运行时与其他 DOM 元素组合在一起。

### 这个定义难以理解吗？

别担心。只需记住，`ng-template` 内部定义的内容不会自动成为 DOM 的一部分。它会在代码中手动使用，并插入到某个位置。

## TemplateRef 和 ViewContainerRef – 两位英雄

`TemplateRef` 服务会提供对 `ng-template` 内部定义内容的引用。

`ViewContainerRef` 代表一个容器，可以将一个或多个视图附加到组件上。

继续演示；之后事情会变得简单得多。

## 实验 – 续

### 步骤 15 – 附加指令

将 `appOnlyIfUserIsAuthorized` 指令附加到 `ng-template` 上，如下所示：

```
……
<ng-template appOnlyIfUserIsAuthorized >
   <input type=”button” value=”Add new record” >
</ng-template>
```

如果你还记得，之前的 `appOnlyIfUserIsAuthorized` 指令是附加在按钮上的。现在我们把它移到了 ng-template 上。

### 步骤 16 – 定义 ngDoCheck

按如下方式实现 `ngDoCheck`：

```
……
   ngDoCheck(): void {
     const isAuthorized = true;
     if (localStorage.IsAuthorized !== ‘true’) {
       this.vc.clear();
    }
     else{
       this.vc.clear();
       this.vc.createEmbeddedView(this.tc);
    }
  }
```

如你所见，当用户被授权时，模板会被动态嵌入到视图容器中；如果用户未被授权，视图容器会被清空。

`TemplateRef` 服务为我们提供了指令所附加的 `ng-template` 的引用，而 `ViewContainerRef` 则提供了容器的引用，我们可以在其中动态添加更多视图。

### 步骤 17 – 检查输出

只需检查输出，当 `IsAuthorized` 为 true 时，你会看到“*Add new record*”；当 `IsAuthorized` 为 false 时，它会消失。

## 讨论 – 续

输出中存在一个大问题。你注意到了吗？如果你认为这是用户未授权时缺少消息的问题，那并不是我们要讨论的。我们很快就会用更好的方式解决那个问题。这是一个更大的问题，**即 *ngDoCheck* 会在每次变更检测时执行。**

这是问题吗？这不正是我们一直想要的吗？

也许是的，但并非在所有变更检测期间都如此。

这是什么意思？

你注意到我们在 *if* 和 *else* 块中都调用了 *clear* 方法吗？你有没有问过自己为什么这样？

*if* 块是有意义的，因为它代表未授权部分，在这种情况下，我们期望它被清空，但为什么 *else* 块中也有它？

如果不在 *else* 块中调用 *clear* 方法，每次变更检测发生时，都会向容器中插入一个新元素。你可以自己验证一下。

从 *else* 块中移除那个 *clear* 方法调用。

在开发模式下，Angular 在开始时执行两次变更检测。所以，你会在开始时看到两个按钮。（现在不用担心这个。）

假设你的 MouseOverDirective 仍在生效，将光标移到该指令所附加的那个元素上。你会注意到，每次移动光标时，都会多创建一个元素。移出光标时也是如此。

这就是为什么在 *if* 和 *else* 块中都要调用 *clear* 方法的原因。

这是正确的方法吗？

不，每次变更检测时移除元素并重新创建，从性能角度来看非常糟糕。我们需要一种更优雅的方式。

这是一个逻辑问题，可以使用一个简单的 *Boolean* 变量来解决。

## 实验 – 续

### 步骤 18 – 修改 ngDoCheck

声明一个布尔变量 `IsViewCreated`，初始值为 false，并在 `ngDoCheck` 中使用它。

```
   IsViewCreated = false;
   ngDoCheck(): void {
     const isAuthorized = true;
     if (localStorage.IsAuthorized !== ‘true’ && this.IsViewCreated) {
       this.vc.clear();
       this.IsViewCreated = false;
    } else if (localStorage.IsAuthorized !== ‘false’ && !this.IsViewCreated) {
       this.vc.createEmbeddedView(this.tc);
       this.IsViewCreated = true;
    }
  }
```

### 步骤 19 – 检查输出

现在一切应该都能正常工作。

在我的咨询经验中，我经常发现这个问题——不必要的 DOM 操作，这会导致应用程序变慢，有时可以通过简单的逻辑来避免。

## 讨论 – 续

接下来，如果用户未授权，我们需要重新显示那条缺失的消息。

为此，我们首先创建一个自定义组件，然后动态加载它。

是时候学习新东西了——**动态加载组件**。

这可以通过一个名为 *ComponentFactoryResolver* 的 Angular 服务来实现。

让我们开始行动。

## 实验 – 续

### 步骤 20 – 创建 CustomMessageComponent

使用 Angular CLI 创建一个名为 `CustomMessageComponent` 的新 Angular 组件，然后在其中创建一个名为 `Message` 的 `Input` 属性，并在模板中使用它。

```
……
export class CustomMessageComponent implements OnInit {
   @Input() Message: string = ‘Default message’;
……
```

```
<b>{{Message}}</b>
```

### 步骤 21 – 将 ComponentFactoryResolver 注入指令

```
import {
   ComponentFactoryResolver,
   ……
} from ‘@angular/core’;
……
export class OnlyIfUserIsAuthorizedDirective implements DoCheck {
   constructor(
     private vc: ViewContainerRef,
     private tc: TemplateRef<any>,
     private resolver: ComponentFactoryResolver,
  ) {}
……
```

### 步骤 22 – 重新定义 ngDoCheck

是时候施展一些魔法了。

```
ngDoCheck(): void {
     const isAuthorized = true;
     if (localStorage.IsAuthorized !== ‘true’ && this.IsViewCreated) {
       this.vc.clear();
       const MessageComponentFactory = this.resolver.resolveComponentFactory(
         CustomMessageComponent
      );
       const MessageComponent = this.vc.createComponent(MessageComponentFactory);
       MessageComponent.instance.Message = ‘Not Authorized!!!’;
       this.IsViewCreated = false;
    } else if (localStorage.IsAuthorized !== ‘false’ && !this.IsViewCreated) {
       this.vc.createEmbeddedView(this.tc);
       this.IsViewCreated = true;
    }
  }
```

只需查看前面代码中的 `if` 块。它包含了所有的魔法。




仅需两行代码，组件即可动态创建并加载。

你会在 `else` 代码块中再次看到对 clear 方法的调用。这是必需的，因为我们需要移除动态创建的组件。（但我们的布尔变量确保逻辑不会在每次不必要的变更检测时执行。）

**第 23 步 – 检查输出。**

非常棒，不是吗？前面的代码完美运行。你将看到“*未授权！！！*”重新出现在操作中。

## 讨论 – 续

我非常确信，你内心的开发者仍然不满意。他/她仍然渴望更多。他/她还在思考我们在 `*ngIf` 和 `*ngFor` 指令中使用的那个特殊的星号（*）符号。

让我展示给你看，而不是解释。

## 实验 – 续

**第 24 步 – 修改 AppComponent。**

打开 `AppComponent`，并按如下方式修改你的授权部分：

```
<input type=”button” value=”添加新记录” *appOnlyIfUserIsAuthorized >
```

（请注意：这里没有 `ng-template`。）

**第 25 步 – 检查输出。**

什么都不会改变。你仍然会得到相同的输出。

## 讨论 – 续

当我们把星号（*）放在指令前面时，Angular 会自动创建 `*ng-template`，附加指令，并将内容（本例中的输入按钮）放入 `*ng-template` 中。

简而言之，它将前面的代码转换为以下代码：

```
<ng-template appOnlyIfUserIsAuthorized >
   <input type=”button” value=”添加新记录” >
</ng-template>
```

使用星号（*）被称为微语法。它让我们在使用结构型指令时更加轻松。

#### 总结

通过本章，我们完成了 Angular 中的一个重要概念。没有自定义指令，我无法想象任何 Angular 项目。至此，我们结束了第 15 站的旅程。我们离终点已经很近了，只剩下五站。让我们回顾一下本章学到的内容：

*   我们在本章学习了指令。它们扩展了现有的 HTML。
*   我们了解到 Angular 有三种类型的指令。
*   第一种称为元素指令，允许我们创建新的 HTML 标签。元素指令在 Angular 中也可以称为组件。
*   第二种是属性指令，允许我们扩展现有 HTML 元素的行为。`ngClass` 和 `ngStyle` 是这类指令的典型例子。
*   第三种是结构型指令，允许我们改变现有 HTML 元素的结构。结构型指令与属性指令类似，会作为属性附加到 HTML 元素上。
*   我们了解到，通常结构型指令会以 * 前缀附加到 HTML 元素上。例如 – `*ngFor`、`*ngIf`。
*   我们学习了为指令指定选择器的不同方式 – 属性选择器、ID 选择器、CSS 选择器和元素选择器。
*   我们演示了 Angular 中的 `ElementRef` 服务，用于引用指令所附加的 HTML 元素。
*   我们学习了 Angular 中的 `Render2` 服务，它提供了处理 DOM 操作的各种方法。
*   我们再次理解了为什么 `ngOnInit` 方法更适合初始化逻辑。我们了解到，*构造函数* 在创建类的对象时执行，而 `ngOnInit` 在组件/指令初始化后执行。这里，初始化意味着实例已创建，并且所有属性都已用父组件传递的值初始化。
*   我们学习了参数化的 Input 装饰器，它允许我们以不同的名称将组件/指令的属性暴露给外部世界。
*   我们学习了 `HostListner` 装饰器，它允许我们处理指令所附加元素的事件。
*   我们学习了 Angular 的 `ngOnChanges` 生命周期事件，每当组件数据绑定属性的值发生变化时，它就会执行。
*   我们学习了 Angular 的 `ngDoCheck` 生命周期事件，它在每次变更检测时执行。
*   我们讨论了用于创建 Angular 模板的 `ng-template`。Angular 模板不会自动渲染。它们会在运行时根据某些自定义逻辑在其他 DOM 元素内部使用和渲染。
*   我们学习了 `TemplateRef` 服务，它提供了 `ng-template` 内部定义内容的引用。
*   我们看到了 `ViewContainerRef` 服务的实际应用，它提供了一个容器的引用，可以将一个或多个视图附加到该容器上。
*   我们学习了 `ComponentFactoryResolver` 服务，它可以用于在运行时动态加载组件。
*   我们讨论了指令的微语法，它消除了显式创建 `ng-template` 元素的负担。

## 第 27 章：Angular 表单

## 引言

我们前往第 16 站的旅程将是一次自学课程。

在前面的章节中，我们已经介绍了模板驱动表单和响应式表单的基础知识。

在学习任何技术时，我坚信 RND（研究与开发）起着关键作用。

当我们遇到困难时，我们会在互联网上搜索答案：

*   这会让我们找到一些论坛、文章或视频。
*   这会向我们介绍一些新的、未知的、未曾接触过的概念。
*   这会将我们的技能提升到新的水平。

因此，我非常相信 RND 在学习和技术方面扮演着非常重要的角色。

考虑到这一点，我希望你能自己创建类似下面的内容：

![](img/Image57433.jpg)

**图 27.1**

它包含了你在任何项目中通常能看到的所有内容。

用两种方式创建它——一种是模板驱动方式，另一种是响应式方式。

在实际项目中，对于如此复杂的表单，不推荐使用模板驱动方式。模板驱动方式适用于没有太多验证的小型表单。但这并不能保证你永远不会遇到使用模板驱动方式的复杂项目。因此，最好用两种方式完成这个实验。

最后，你可以从 Git 仓库下载相应的示例。

考虑到你已经诚实地完成了所有内容，现在你已经准备好前往第 17 站——Angular 样式。

## 第 28 章：Angular 样式

## 引言

在前往第 17 站的旅程中，我们将学习如何在 Angular 中处理样式表。

### 外部样式表

你一定注意到了 Angular 应用中有一个名为 `angular.json` 的文件。它是 Angular CLI 的配置文件。诸如 `ng serve` 和 `ng build` 等命令都是使用该文件中的设置执行的。

![](img/Image57444.jpg)

**图 28.1**

该文件中定义的一个重要部分是 builds/styles 部分。

默认情况下，你会在该部分找到 `style.css` 的条目。

它充当 Angular 应用的全局 CSS 文件。在其中定义的样式将在整个应用中可用。我们在前面某一章中已经看到过它的实际应用。

#### 可以有多个外部样式表文件吗？

是的，有以下三种方式可以实现：

1.  在 `Index.html` 中使用 link 标签包含它。
2.  使用 CSS @import。
3.  在 `angular.json` 文件中导入。

第一种方式非常简单。使用 `link` 标签将外部 CSS 文件包含在 `index.html` 中。

```
<link rel=”stylesheet” href=”mystyle.css”>
```

让我们看看另外两种方式。

**第 1 步 – 创建一个项目。**




使用 `ng` 命令创建一个新的 Angular 项目 `lab15-ng`。

#### 步骤 2 – 创建一个组件。

创建一个名为 `ExternalCSSTestComponent` 的新组件，然后将其包含在 `AppComponent` 中。（删除 `AppComponent` 的现有内容。）

```
<!-- 外部 CSS 测试组件 -->
<p class=”MyClass1 MyClass2”>Hello World!!!</p>
```

```
<!-- 应用组件 -->
<app-external-csstest-component></app-external-csstest-component>
```

#### 步骤 3 – 创建一个新的 CSS 文件。

在 `src` 文件夹中创建一个名为 `mystyle.css` 的新 CSS 文件，并放入以下内容：

```
.MyClass2{
   font-weight: bold;
}
```

#### 步骤 4 – 更新 style.css

使用 CSS @Import 规则在 `style.css` 中导入 `mystyle.css`，然后创建一个新的 CSS 类，如下所示：

```
@import "mystyle.css";
.MyClass1{
   border:1px solid black;
}
```

#### 步骤 5 – 测试输出

执行应用程序。你将看到一个带有黑色边框的粗体“Hello World!!!”——粗体来自 `mystyle.css`，边框来自 `style.css`。

#### 步骤 6 – 构建应用程序。

使用 `ng build --prod` 命令构建应用程序。

执行命令后，你将找到一个名为 `style.***.css` 的单个 CSS 文件。

打开该文件并检查其内容。

```
.MyClass2{font-weight:700}.MyClass1{border:1px solid #000}
```

如你所见，`style.css` 和 `mystyle.css` 的内容现在被捆绑到一个文件中。

让我们看看如果导入多个 CSS 文件会发生什么。

#### 步骤 7 – 创建一个新的 CSS 文件。

在 `src` 文件夹中创建一个新的 CSS 文件 `color.css`。

```
.MyClass3{
   color: red;
}
```

#### 步骤 8 – 更新 ExternalCSSTestComponent

在 `ExternalCSSTestComponent` 中应用这个新的 CSS 类，如下所示：

```
<!-- 外部 CSS 测试组件 -->
<p class=”MyClass1 MyClass2 MyClass3”>Hello World!!!!</p>
```

#### 步骤 9 – 导入新的 CSS 文件

与之前类似，在 `style.css` 中导入 color.css，如下所示：

```
import "mystyle.css";
@import "color.css";
.MyClass1{
   border:1px solid black;
}
```

#### 步骤 10 – 执行应用程序

执行应用程序。你将得到一个粗体且红色的“Hello World!!!”，它由所有三个 CSS 类装饰。

#### 步骤 11 – 构建应用程序

现在构建应用程序。

Angular CLI 会将所有三个 CSS 文件捆绑到一个文件中。

构建后，你将得到一个 CSS 文件 `style.***.css`，它封装了所有三个文件的内容。

```
.MyClass2{font-weight:700}.MyClass3{color:red}.MyClass1{border:1px solid #000}
```

这就是 CSS @import 的示例。在 ng build 时，Angular CLI 会将 `style.css` 及其所有依赖的样式表捆绑到一个包中。

接下来，让我们看看 `angular.json` 的方式。

#### 步骤 12 – 在 angular.json 中导入 color.css

首先，删除 `style.css` 中 color.css 的导入语句。

```
import "mystyle.css";
.MyClass1{
   border:1px solid black;
}
```

接下来，将 `color.css` 包含在 `angular.json` 文件中，如下所示：

```
"build": {
           ……
             "styles": [
               "src/styles.css",
               "src/color.css"
            ],
             "scripts": []
          },
```

#### 步骤 13 – 执行应用程序

`angular.json` 文件中的任何更改都需要重新执行 `ng serve` 命令。

所以请确保你执行了相同的操作。（为此，按 Ctrl+C 停止现有执行，然后再次执行 ng serve 命令。）

执行后，你将得到与之前相同的输出。你将看到红色、粗体并带有黑色边框的“Hello World!!!”。

#### 步骤 14 – 构建应用程序

使用 `ng build --prod` 命令构建应用程序，令人惊讶的是，你不会发现任何显著的不同。你会找到一个生成的单个 CSS 文件，其中包含来自所有三个 CSS 文件的内容，与之前类似。

```
.MyClass2{font-weight:700}.MyClass1{border:1px solid #000}.MyClass3{color:red}
```

看起来没有任何变化。CSS @import 和 `angular.json` 的行为相同。

## 讨论 – 继续

对于外部样式表，我们可以使用 CSS @import 或 `angular.json` 来包含它们。在实际项目中，你可能会看到其中任何一种方式，或者两者都用。

在前面的案例中，我们两者都用了。

你可能想知道该遵循哪一种。嗯，两者都有优缺点：

* CSS @import 使开发变得容易，因为每次我们想要从应用程序中添加或删除外部样式表时，都不需要重新执行 `ng serve` 命令。
* 另一方面，`angular.json` 允许我们在需要时创建多个包。如果你觉得生成的 CSS 包太大，需要拆分成多个文件，那么 `angular.json` 是最好的方式。让我们看看这个的实际应用。

## 实验 – 继续

### 步骤 15 – 为多个包配置 angular.json

打开 `angular.json` 并将 styles 部分修改如下：

```
"styles": [
               "src/styles.css",
               {
                 "input": "src/color.css",
                 "bundleName": "color"
              }
            ],
```

### 步骤 16 – 执行应用程序

重新运行 `ng serve` 命令。输出不会有任何变化。

### 步骤 17 – 构建应用程序

再次构建应用程序。这次会生成两个 CSS 包——`style.***.css` 和 `color.***.css`。

第一个包含 `styles.css` 和 `mystyle.css` 的内容。

第二个包含 `color.css` 的内容。

## 组件样式

当我们谈论组件时，我们称之为两件事的组合——模板类和模板。但这并不完全正确。有时，它也可以有自己的 CSS 文件。

当你使用 Angular CLI 创建 Angular 组件时，你一定注意到了这样的文件。如果没有，不用担心。我们现在就来研究一下，并理解这个 CSS 文件与 `style.css` 有何不同。

## 实验 – 15 – 理解组件样式

### 步骤 1 – 注释 ExternalCSSTestComponent

在 `AppComponent` 中注释掉 `ExternalCSSTestComponent`，如下所示：

```
<!-- 应用组件 -->
<!-- <app-external-csstest-component></app-external-csstest-component> -->
```

### 步骤 2 – 创建组件

创建四个组件——`Customer`、`CustomerList`、`Product` 和 `ProductDashboard`。

### 步骤 3 – 使用组件

将这些组件相互嵌套使用，如下所示：

```
<!-- 应用组件 -->
<!-- <app-external-csstest-component></app-external-csstest-component> -->
<div class="DivContainer">
   <p>Hello From App Comonent</p>
   <app-customer></app-customer>
   <app-product></app-product>
</div>
```

```
<!-- 客户组件 -->
<div class="DivContainer">
   <p>Hello From Customer</p>
   <app-customer-list></app-customer-list>
</div>
```

```
<!-- 产品组件 -->
<div class="DivContainer">
   <p>Hello From Product</p>
   <app-product-dashboard></app-product-dashboard>
</div>
```

```
<!-- 客户列表组件 -->
<div class="DivContainer">
   <p>Hello From Product-List</p>
</div>
```

```
<!-- 产品仪表板组件 -->
<div class="DivContainer">
   <p>Hello From Product-Dashboard</p>
</div>
```

### 步骤 4 – 定义样式

现在魔法开始了。在 `style.css` 中定义一个新的样式，如下所示：

```
……
.DivContainer {
   border:1px solid black;
   margin: 5px;
}
```

![](img/Image57587.jpg)

**图 28.2**

### 步骤 5 – 检查输出





执行应用程序，你将看到以下输出。

正如预期，相同的 CSS 被应用到了每个组件中。

**第 6 步 – 定义组件样式**

接下来，在 `app.component.css` 文件中定义新样式，如下所示：

```
.DivContainer {
   border:2px black dashed;
}
```

**第 7 步 – 检查输出**

你会发现，`app.component.css` 文件中定义的样式只影响了 `AppComponent` 中的 `div` 元素。其他组件仍然显示由 `style.css` 附加的实心黑色边框。

![](img/Image57699.jpg)

**图 28.3**

你能看到虚线边框吗？这是因为 `app.component.css` 文件附加到了 `AppComponent` 上。

**第 8 步 – 定义组件样式**

接下来，在 `customer-list.component.css` 文件中定义样式，如下所示：

```
.DivContainer {
   border:3px red dotted;
}
```

**第 9 步 – 检查输出**

这次你会注意到，新样式只影响了 `CustomerListComponent` 内部的 `div` 元素。

你在之前的输出中看到红色点状边框了吗？这是因为我们在 `customer-list.component.css` 文件中添加的新样式。

![](img/Image57707.jpg)

**图 28.4**

这就是组件样式的全部内容——样式被封装在组件内部。

**第 10 步 – 构建应用程序**

让我们构建应用程序，并准确理解构建后这些组件样式发生了什么变化。

## 讨论 – 续

你会惊讶地发现，构建后没有为任何组件生成特定的 CSS 文件。

打开 `style.***.css` 和 `color.***.css`，检查组件样式是否被打包在这些文件中。你也不会在这些文件中找到组件样式。

**那么组件样式在哪里？**

组件 CSS 样式被封装到了组件自身的视图中，这就是为什么它不会影响应用程序的其他部分。

Angular CLI 将所有自定义应用程序代码打包到一个名为 `main.***.js` 的包文件中。

打开那个 `main.***.js` 文件，搜索 `3px`。如果你还记得，CustomerList 的 CSS 中有 `3px border`。

你会在文件中找到它。

![](img/Image57784.jpg)

**图 28.5**

在运行时，当相应的组件被加载时，Angular 会动态地将这些样式作为内联样式注入到 DOM 中。你甚至可以在开发者工具中检查它们。

![](img/Image57826.jpg)

**图 28.6**

***注意：*** 如你所知，在惰性加载的情况下，会生成多个这样的包。因此，你会在相应的包中找到组件样式，而不是在主包中。

**`styleUrls` 是创建组件特定样式的唯一方法吗？**

`styleUrls` 允许我们将外部 CSS 文件包含到组件中，但这并不是拥有组件特定样式的唯一方法。我们还有另一种方法——内联样式。可以这样做：

```
@Component({
   selector: ‘app-customer-list’,
   templateUrl: ‘./customer-list.component.html’,
   // styleUrls: [‘./customer-list.component.css’]
   styles: [`.DivContainer {
     border:3px red dotted;
   }`]
})
export class CustomerListComponent implements OnInit {……
```

建议使用 `styleUrls` 而不是 `styles`，但你仍然会在项目中找到一些使用后者的地方。

## 视图封装

我们已经说过好几次了——组件 CSS 样式被封装到了组件自身的视图中。

我们可以通过设置组件装饰器中的封装模式，在每个组件的基础上控制这种封装。

目前有以下三种可能的值：

# 1. 模拟（Emulated）

这是默认模式。在这种模式下，你会发现每个 DOM 元素都附加了一些唯一的属性。

```
@Component({
   selector: ‘app-root’,
   templateUrl: ‘./app.component.html’,
   styleUrls: [‘./app.component.css’],
   encapsulation: ViewEncapsulation.Emulated,
})
export class AppComponent {
```

执行应用程序，打开开发者工具，并打开 **`Elements`** 选项卡。

**你能在上图中看到 `_ngcontent-pij-c15` 吗？**

如你所见，它附加到了 `AppComponent` 中的每个元素上。

**你能找到 `_ngcontent-pij-c12` 吗？**

如你所见，它附加到了 `CustomerComponent` 的每个元素上。

![](img/Image57833.jpg)

**图 28.7**

Angular 为每个组件生成一个唯一的字符串，并将其添加到该组件的每个子元素上。

**你是否好奇 Angular 为什么要这样做？**

通过这样做，Angular 使这些样式成为组件特定的。

![](img/Image57877.jpg)

**图 28.8**

要理解这一点，请检查 head 部分。你会发现多个 style 标签。

Angular 在运行时动态创建了这些 style 标签。

其中两个是全局样式，之后每个 style 标签代表一个组件。

展开第三个 *style* 标签。它代表 AppComponent 的样式。

**你看到什么有趣的东西了吗？**

CSS 选择器也被重命名了。

重命名将确保这些 CSS 设置只附加到具有相应属性的元素上。

![](img/Image57910.jpg)

**图 28.9**

# 2. 无（None）

这个值在实际中没什么用。设置此值表示我们不希望任何视图封装，从而使组件样式成为全局样式。

```
@Component({
   selector: ‘app-root’,
   templateUrl: ‘./app.component.html’,
   styleUrls: [‘./app.component.css’],
   encapsulation: ViewEncapsulation.None,
})
export class AppComponent {
```

你会注意到，将其设置为 None 后，AppComponent 中定义的任何样式都将全局应用。

# 3. ShadowDOM

我之前已经说过一次，Angular 组件是受 HTML5 中引入的 **`Web Components`** 概念启发的。**`WebComponent`** 的核心特性之一就是 ShadowDOM。

**让我向你展示什么是 ShadowDOM？**

创建一个 HTML 文件，并将以下内容放入其中。我们是在演示一个 HTML 概念，所以不需要 Angular 项目。你可以有一个简单的 HTML 文件。

```
<html>
<head>
     <title>日期选择器</title>
</head>
<body><input type=”date”></body>
</html>
```

执行该文件并打开开发者工具。

![](img/Image57951.jpg)

**图 28.10**

**你知道这个 HTML 5 日期元素的特殊之处吗？**

它是一个 Web 组件。就像我们的 Angular 组件一样，它是对某些 HTML（最好称为模板）、格式（CSS）和行为（逻辑代码）的封装。你想看看底层的模板吗？

点击开发者工具中的设置图标。

![](img/Image57991.jpg)

**图 28.11**

这将打开设置面板。在 Elements 子部分中，勾选“*显示用户代理 shadow DOM 选项*”。

然后，关闭设置面板并重新检查 **`Elements`** 部分。这次你将能够展开日期元素。

![](img/Image58031.jpg)

**图 28.12**

**你看到 `#shadow-root` 了吗？**

这就是 ShadowDOM。包含在其中的样式不会泄漏到外部世界，因此外部世界不受影响，但这还不是全部。Web 组件的内容也不会受到外部世界 CSS 的影响。这意味着外部世界附加到 div 元素上的任何 CSS 格式都不会影响日期元素的 div 元素。

![](img/Image58073.jpg)

**图 28.13**

**Angular 中的 ShadowDOM**

在 Angular 中，通过将封装设置为 `ShadowDOM`，我们将获得类似的行为。

# 演示 1

**第 1 步 – 设置封装**

为了演示，将 `AppComponent` 和 `CustomerListComponent` 的封装模式设置为 ShadowDOM。然后，从 `AppComponent` 中移除 `styleUrls`，并从 `CustomerListComponent` 中移除 `styles`。

```
@Component({
```





```
   selector: ‘app-customer-list’,
   templateUrl: ‘./customer-list.component.html’,
// styleUrls: [‘./customer-list.component.css’]
// styles: [`.DivContainer {
//   border:3px red dotted;
//}`],
   encapsulation: ViewEncapsulation.ShadowDom,
})
export class CustomerListComponent implements OnInit {
```

```
@Component({
   selector: ‘app-root’,
   templateUrl: ‘./app.component.html’,
//styleUrls: [‘./app.component.css’],
   encapsulation: ViewEncapsulation.ShadowDom,
})
export class AppComponent {
```

**第 2 步 – 设置封装**

将 `Product`、`ProductDashboard` 和 `CustomerComponent` 的封装模式设置为 `ShadowDOM`。

**第 3 步 – 执行应用程序**

现在执行应用程序。你将看到一个没有任何边框的屏幕。

![](img/Image58111.jpg)

**图 28.14**

这证明外部 CSS 对视图封装设置为 `ShadowDOM` 的组件没有影响。（`style.css` 中的 CSS 没有影响这些组件。）

# 演示 2

**第 1 步 – 定义组件样式**

按如下方式为 `CustomerListComponent` 和 `AppComponent` 添加组件样式：

```
@Component({
   selector: ‘app-root’,
   templateUrl: ‘./app.component.html’,
   styleUrls: [‘./app.component.css’],
   encapsulation: ViewEncapsulation.ShadowDom,
})
export class AppComponent
```

```
@Component({
   selector: ‘app-customer-list’,
   templateUrl: ‘./customer-list.component.html’,
// styleUrls: [‘./customer-list.component.css’]
   styles: [`.DivContainer {
     border:3px red dotted;
  }`],
   encapsulation: ViewEncapsulation.ShadowDom,
})
export class CustomerListComponent implements OnInit {
```

**第 2 步 – 更改封装**

移除除 `AppComponent` 之外所有组件的封装。

（换句话说，将 `AppComponent` 的封装设置为 `Emulated`。）

**第 3 步 – 执行应用程序**

执行应用程序，并使用开发者工具检查输出和 DOM。

![](img/Image58156.jpg)

**图 28.15**

![](img/Image58163.jpg)

**图 28.16**

`AppComponent` 被渲染为 `ShadowDOM`，因此其样式直接渲染在内部。

现在让我们检查输出。

你会看到 `AppComponent` 周围有一个虚线边框。这很明显，因为 `AppComponent` 的样式就是这样写的。

你会看到 `CustomerListComponent` 周围有一个红色点状边框。这也很明显，因为 `CustomerListComponent` 的样式就是这样写的。

**为什么其他组件有虚线边框？**

看到其他组件周围的虚线边框，你是否感到失望？

当封装设置为 `emulated` 时，`AppComponent` 的样式仅限于 `AppComponent`。`CustomerComponent` 没有继承它。

但这次情况不同。这次，`AppComponent` 的样式被所有子组件继承，因此除了 `CustomerList` 组件之外的所有组件都有虚线边框。客户列表组件有红色点状边框，因为它有自己的组件样式。

你可能会说这*违反了 ShadowDOM 的规则*——外部样式不会影响 ShadowDOM 内部的内容，而 ShadowDOM 内部定义的样式也不会影响其他元素。

答案是否定的。它并没有违反。再看一下生成的 DOM。`AppComponent` 被渲染为 `ShadowDOM`，但其他组件呢？它们被渲染为 `AppComponent` 的普通子元素，并且它们的封装仍然设置为 `emulated`（默认值）。因此，它们将遵循相同的旧方法，即使用唯一属性。

这就是为什么它们都有虚线边框的原因。

**第 4 步 – 更改封装**

将所有组件的 `encapsulation` 设置为 `ShadowDOM`。

![](img/Image58230.jpg)

**图 28.17**

完成此操作后，你将得到以下输出。

这次每个组件都被渲染为 `ShadowDOM`。因此，它们都不受外部 CSS 的影响。

在创建可重用的独立组件时，`ShadowDOM` 是最佳选择。

*对于实际应用程序，推荐且最佳的方法是 `emulated`*。使用它，我们可以利用全局样式表，并且在需要组件特定样式时，我们也有相应的支持。

#### 总结

*   我们讨论了在 Angular 应用程序中包含外部样式表的三种方式——使用 `index.html` 文件中的 `link` 标签、使用 *CSS @import* 以及使用 `angular.json` 文件。

*   我们了解到 `angular.json` 文件中有一个名为 *builds/styles* 的部分，用于声明项目中的外部 CSS 文件。默认情况下，Angular 样板项目包含一个 `style.css` 文件的条目。

*   我们演示了 *CSS @import*，并了解到在执行 `ng build` 时，Angular CLI 会将 `style.css` 及其依赖的每个样式表文件打包成一个包。

*   我们演示了使用 `angular.json` 文件导入样式表文件，并了解到 `angular.json` 文件中提到的所有样式表文件在执行 `ng build` 时会被打包成一个文件。

*   我们了解到，使用 `angular.json` 而不是 *CSS @import* 来导入样式表文件被认为是更好的方法。它让我们能够指示 Angular CLI 在需要时生成多个包。

*   我们学习了如何使用 *Component* 装饰器的 `styleURL` 或 `styles` 属性将样式附加到单个组件。我们了解到这些样式在构建后不会被打包到任何 CSS 包中；相反，它们会成为组件视图本身的一部分。

*   我们学习了 *ViewEncapsulation*，它让我们能够控制样式如何封装到组件视图中。

*   我们讨论了 `Emulated` 封装，这是默认模式。此模式为组件的每个 DOM 元素附加一个唯一属性，并重命名每个 CSS 选择器，使样式仅对该组件生效。

*   我们讨论了 `Native` 封装，它遵循 HTML 5 的 *ShadowDOM* 方法。使用此模式，我们确保没有外部 CSS 影响组件的内容，并且组件特定的样式不会影响外部世界。这是可重用组件的最佳方法。

*   我们讨论了 `None` 封装，它使每个组件特定的样式成为全局样式。

## 第 29 章

## Angular 变更检测

#### 简介

你是否曾问过自己，模板是如何始终显示最新数据的？每当组件类中的数据发生变化时，它是如何更新的？变更检测就是答案，在本章中，我们将详细探讨变更检测。

## 什么是变更检测？

变更检测是 Angular 中的一种机制，它遍历绑定、评估表达式、将其与先前的值进行比较，并在必要时更新 DOM。

简而言之，它负责保持 UI 的最新状态。

## 哪些组件会参与变更检测？

正如我们之前多次讨论过的，Angular 维护一个组件的树形层次结构。这棵树在顶部有一个根组件。

在变更检测中，组件层次结构中的每个组件都会被检查，并在需要时重新渲染。

（你很快会在我们的演示中看到它的实际效果。）

## Angular 何时执行变更检测？

Angular 在应用程序生命周期中的以下事件期间执行变更检测。

1.  **应用程序初始化之后**——即在 Angular 应用程序启动并加载引导组件之后。





2.  DOM 事件监听器之后——即在浏览器事件（如 click、focus、blur 等）被处理之后。

3.  HTTP 数据请求之后——即在 Ajax 请求被处理（收到服务器响应）之后——响应可以是错误响应或成功响应。

4.  宏任务（MacroTasks）之后——即在 `setTimeout()` 或 `setInterval()` 等宏任务完成之后。这些宏任务在传递给它们的回调函数执行完毕后即视为完成。

5.  微任务（MicroTasks）之后——即在 Promise 等微任务完成之后——Promise 在 resolve 或 reject 后即视为完成。

6.  其他异步操作之后——即在 `WebSocket.onMessage` 和 `Canvas.toBlob` 等其他异步操作执行完毕之后。

## Angular 如何触发变更检测？

Angular 使用名为 `zone.js` 的库对上述所有 API 进行了*猴子补丁（monkey patched）*。

它用新版本替换了所有这些底层 API。这些新版本增加了一些额外功能——例如，在回调被调用后，它会确保检测到变更并在需要时更新 UI，即进行变更检测。

## 开发模式下的变更检测

你必须理解的一个重要点是：在开发模式下，变更检测会执行两次。为了证明这一点，我们来做一个快速演示。

**步骤 1 - 创建项目**

使用 `ng new` 命令创建一个新的 Angular 项目 `lab16-ng`。

**步骤 2 - 创建新组件**

使用 `ng` 命令创建一个名为 `TwiceDetectionTestComponent` 的新 Angular 组件，然后将以下内容放入其中：

```
<h1>Testing twice change detection call - {{getData()}}</h1>
<input type=”button” value=”Click Me” (click)=”HandleClick()” >
@Component({
   selector: ‘app-twice-detection-test-component’,
   templateUrl: ‘./twice-detection-test-component.component.html’,
   styleUrls: [‘./twice-detection-test-component.component.css’]
})
export class TwiceDetectionTestComponentComponent   {
   getData(): string {
     console.log(“getData invoked”)
     return “Just Compile LLP”
  }
   HandleClick(){
  }
}
```

**步骤 3 – 在根组件中包含该组件**

打开 `app.component.html`，将现有内容替换为以下内容：

```
<!-- app.component.html -->
<app-twice-detection-test-component></app-twice-detection-test-component>
```

**步骤 4 – 运行应用程序**

使用 `ng serve` 命令运行应用程序并检查输出。

![](img/Image58286.jpg)

**图 29.1**

但比起输出，你更应该关注开发者工具的控制台。

![](img/Image58351.jpg)

**图 29.2**

## 讨论

我说过在开发模式下变更检测会执行两次吗？

你觉得这是两次吗？实际上是四次。

我们稍后再讨论这个问题。现在，继续下一步。

## 实验 – 继续

**步骤 5 – 点击按钮**

清空开发者控制台，然后点击组件中的 `Click Me` 按钮。正如我之前所说，按钮点击会触发变更检测。检查变更检测执行了多少次会很有趣。

![](img/Image58410.jpg)

**图 29.3**

清空控制台再试一次。你会注意到每次点击按钮，控制台都会显示两条消息。

## 讨论 – 继续

我相信你仍然对一开始的四次执行感到困惑。别担心。

通过上一步，我们证明了点击按钮时变更检测会执行两次。

你想知道原因吗？我们来讨论一下。

打开开发者工具，在 `getData` 方法中设置断点，并检查调用栈。

在第一次断点处，你会得到以下调用栈。

![](img/Image58418.jpg)

**图 29.4**

第二次，调用栈如下：

![](img/Image58486.jpg)

**图 29.5**

你能找出两者之间的区别吗？

在第一次执行时，Angular 更新了 DOM，这正是 `detectchanges` 方法所做的。

在第二次调用中，Angular 确保在之前的 DOM 重新渲染后没有任何变化，这正是 `checkNoChanges` 方法所做的。如果它发现绑定的值发生了变化或确定 DOM 应该更新，就会抛出异常。我们来证明这一点。

## 实验 – 继续

**步骤 6 – 在第一次调用后更改 DOM**

为此，将 `getData` 方法修改如下：

```
getData(): number {
     const data = Math.random() * 100;
     console.log(data);
     return data;
  }
```

**步骤 7 – 重新检查应用程序**

忽略第一次执行的情况。清空控制台并点击 `Click Me` 按钮。你的开发者控制台应该如下所示：

![](img/Image58535.jpg)

**图 29.6**

我们会得到一个异常——`ExpressionChangedAfterItHasBeenChecked`。

Angular 执行了两次变更检测。在第一次执行期间，生成了某些输出；在第二次执行期间，Angular 发现要渲染的值不同了。因此我们得到了这个错误。

请注意，这种两次执行的情况仅在开发模式下可见。在生产模式下，变更检测只执行一次。

**步骤 8 – 在生产模式下运行**

使用 `ng serve --prod` 命令重新运行应用程序。检查开发者工具。你会发现显示两个输出。（之前，在开发模式下是四次。）

清空控制台并点击按钮。你会发现只显示一个值。（之前，在开发模式下是两次。）

## 为什么初始化时会执行两次？

基于之前的实验，我们得到以下组合：

*   开发模式 + 应用程序初始化时 = 变更检测执行四次。

*   开发模式 + 其他变更检测触发器（如事件处理程序、宏任务等）= 变更检测执行两次。

*   生产模式 + 应用程序初始化时 = 变更检测执行两次。

*   生产模式 + 其他变更检测触发器（如事件处理程序、宏任务等）= 变更检测只执行一次。

我们了解到，在开发模式下，Angular 会执行两次变更检测。第一次运行时，DOM 会以最新的组件状态进行渲染；第二次运行时，它会确认在之前的重新渲染后 DOM 没有发生变化。如果发生了变化，我们会得到一个运行时错误——*`ExpressionChangedAfterItHasBeenChecked`*。

现在的问题是，为什么在应用程序初始化后也会执行两次？

*   在应用程序初始化期间，Angular 默认会调用 tick 方法，这会导致变更检测。（在开发模式下，它会执行两次——一次 `changedetection`，一次 `checkNoChanges`。）

*   一旦完成，由于 `zone.js` 的存在，tick 方法会再次执行。这会导致第二次变更检测循环。（在开发模式下，它会执行两次——一次 `changedetection`，一次 `checkNoChanges`。）

## 将 zone.js 与 Angular 断开连接

之前我们了解到，Angular 使用 `zone.js` 对原生底层 API 进行猴子补丁。这些猴子补丁确保一旦这些底层 API 完成，就会触发变更检测，从而更新 DOM。

**这是否意味着没有 zone.js 就没有变更检测？**

并非如此。

**变更检测**是 Angular 中的一种机制，它遍历绑定、评估表达式、与之前的值进行比较，并在必要时更新 DOM。





通过猴子补丁（monkey patching）底层 API（如 `addEventListener`、`setTimeout` 等），`zone.js` 确保了变更检测能够自动触发。

如果我们移除 `zone.js`，并不会移除 Angular 的变更检测能力，只是移除了自动化机制。

在 Angular 中，有一种方法可以将默认的 zone 与应用程序断开连接。让我们来操作一下。

### 第 1 步 – 创建新项目

变更检测的学习有时会变得非常令人困惑。因此，我总是建议为每个新演示创建一个新项目。

使用 `ng` 命令创建一个新的 Angular 项目 `lab17-ng`。

### 第 2 步 – 修改 AppComponent

将 `AppComponent` 的内容修改如下：

```
export class AppComponent   {
   Counter: number=0;
   Increement(){
     this.Counter++;
   }
}
```

```
<input type=”button” value=”Increement” (click)=”Increement()” /> {{Counter}}
```

### 第 3 步 – 运行应用程序

使用 `ng serve` 命令运行应用程序。确保每次点击按钮后数值都会更新。

当前应用程序默认配置为使用 `zone.js` 运行，每次点击都会触发变更检测。

### 第 4 步 – 断开 zone.js

在 `src` 文件夹中，你会找到一个名为 `polyfill.ts` 的文件。

滚动到底部，你会看到一行导入 zone 库的代码。注释掉该语句或将其删除。

```
//import 'zone.js/dist/zone'; // Included with Angular CLI.
```

#### 第 5 步 – 运行应用程序

运行后，你会看到一个空白页面。打开开发者工具检查以下错误：

![](img/Image58660.jpg)

**图 29.7**

## 讨论 – 继续

由于我们已经移除了 `zone.js`，Angular 应用程序中不再有 zone。zone 是 Angular 应用程序的执行上下文。不必过于担心——只需注意一点：Angular 需要 zone，否则会破坏应用程序，而为了使其正常工作，我们需要提供自定义的 zone 对象。

另一种替代方案是 `NoopNgZone`——Angular 自带了 noop zone，它什么也不做，与 `zone.js` 提供的 zone 对象不同，后者会对底层 API 进行猴子补丁。

## 实验 – 继续

### 第 6 步 – 提供 noop zone

为此，将 `main.ts` 文件中的引导语句修改如下：

```
platformBrowserDynamic().bootstrapModule(AppModule,{ngZone: 'noop'})
   .catch(err => console.error(err));
```

### 第 7 步 – 运行应用程序

运行应用程序。你会发现计数器值显示为“0”。

接下来，点击按钮。你不会看到任何 DOM 变化。这证明 DOM 事件发生后没有进行变更检测。

## 讨论 – 继续

Angular 在应用程序初始化后只执行一次变更检测。这就是计数器初始值正确显示的原因。

但由于 `zone.js` 已断开连接，变更检测的自动触发不再生效。

## 实验 – 继续

### 第 8 步 – 手动检测变更

我们移除了 `zone.js`，因此应用程序中不再有任何自动变更检测，但我们可以通过显式调用 `tick` 方法来手动执行。

在 `AppComponent` 中获取 `ApplicationRef` 服务的引用，然后按如下方式调用 `tick` 方法：

```
export class AppComponent {
   Counter: number = 0;
   constructor(private app: ApplicationRef) {}
   Increement() {
     this.Counter++;
     this.app.tick();
   }
}
```

### 第 9 步 – 检查输出

这次你会看到预期的输出。

采用无 zone 的 Angular 方法可以显著提高性能，因为它限制了变更检测，但可能会增加应用程序的复杂性。因此，请谨慎选择。

## polyfill.ts

我相信在完成实验后，你一定想了解 `polyfill.ts` 文件。

### 什么是 polyfill？

Polyfill 是一些库，它们为现有的 JavaScript 添加额外的功能，从而使不兼容的浏览器变得兼容。

让我们快速演示一个名为 `classlist.js` 的 polyfill。

### 第 1 步 – 创建新的 HTML 文件

创建一个新的 HTML 文件 `index.html`，并放入以下内容：

```
<!DOCTYPE html>
<html>
<head>
     <style>
         .mystyle {
             width: 300px;
             height: 50px;
             border: 1px solid black;
        }
     </style>
</head>
<body>
     <button onclick=”addStyle()”>Add Style</button>
     <div id=”myDIV”>
         I am a DIV element
     </div>
     <script >
         function addStyle() {
             document.getElementById(“myDIV”).classList.add(“mystyle”);
        }
     </script>
</body>
</html>
```

### 第 2 步 – 测试 HTML 文件

在你选择的任意浏览器中打开该 HTML 文件。

（确保如果你使用 IE，版本应为 10 或更高）

点击按钮，你应该会在 DIV 元素周围看到一个黑色边框。

### 第 3 步 – 在 IE9 或更低版本中测试 HTML 文件

现在，在 IE9 或更低版本的 IE 中打开同一个 HTML 文件。

你会发现演示无法工作，因为 IE9 及更低版本不支持 classList。

### 第 4 步 – 下载 polyfill

为了使其工作，我们将使用一个名为 `classlist.js` 的 polyfill。

可以使用 `npm install classlist.js` 命令下载它。

### 第 5 步 – 引入 polyfill

下载完成后，将下载的库文件按如下方式引入到 `index.html` 中：

```
<!DOCTYPE html>
<html>
<head>
     <script  src="./node_modules/classlist.js/classList.js"></script>
     <style>
         .mystyle {
……
```

### 第 6 步 – 在 IE9 或更低版本中重新测试 HTML

这次你会发现它可以正常工作。

## Angular 项目中的 polyfill.ts 是什么？

这是一个文件，我们将在其中包含所有希望在应用程序加载之前加载的 polyfill。

默认情况下，它只有一个条目——`zone.js` 的条目。

Angular 库是基于 Web 平台的最新标准构建的。我们无法保证所有这些标准在所有浏览器上都能正常工作。假设你计划在旧版浏览器中运行 Angular 应用程序。在这种情况下，你肯定需要一些 polyfill 库，按照标准，下载 polyfill 后，必须将其包含在 `polyfill.ts` 文件中。

所有在 `polyfill.ts` 中导入的库在使用 `ng build` 命令构建应用程序时，会被打包并压缩为 `polyfill.***.js`。

## 具有组件层次结构的变更检测

在第四个演示中，我们将学习具有组件层次结构的变更检测。

### 第 1 步 – 创建新项目

创建一个新的 Angular 项目 `lab18-ng`。

### 第 2 步 – 创建组件

使用 `ng` 命令创建 Customer、CustomerList、CustomerAdd 和 Product 组件。

### 第 3 步 – 使用组件

*   在 Customer 组件内部使用 CustomerList 和 CustomerAddComponent。
*   在 AppComponent 内部使用 Product 和 Customer 组件。
*   同时，在所有组件中创建一个按钮并处理其点击事件。
*   在所有组件类中创建一个 `GetMessage` 方法，并在相应模板的插值语法中调用它。

```
export class AppComponent {
   GetMessage(): void {
     console.log('App Component message');
   }
   HandleClick(): void  {}
}
<!-- app.component.html -->
<div>
   {{GetMessage()}}
   <input type=”button” value=”AppButton” (click)=”HandleClick()”>
   <app-customer></app-customer>
   <app-product></app-product>
</div>
```





```
export class CustomerComponent  {
   GetMessage(): void {
     console.log('Customer Component message');
  }
   HandleClick(): void  {}
}
```

```
<!-- customer.component.html -->
<div>
   {{GetMessage()}}
   <input type="button" value="CustomerButton" (click)="HandleClick()">
   <app-customer-list></app-customer-list>
   <app-customer-add></app-customer-add>
</div>
```

```
export class ProductComponent{
   GetMessage(): void {
     console.log('Product Component message');
  }
   HandleClick(): void  {}
}
```

```
<!-- product.component.html -->
<div>
   {{GetMessage()}}
   <input type="button" value="ProductButton" (click)="HandleClick()">
</div>
```

```
export class CustomerAddComponent {
   GetMessage(): void {
     console.log('Customer Add Component message');
  }
   HandleClick(): void  {}
}
```

```
<!-- customer-add.component.html -->
<div>
   {{GetMessage()}}
   <input type="button" value="CustomerAddButton" (click)="HandleClick()">
</div>
```

```
export class CustomerListComponent{
   GetMessage(): void {
     console.log('Customer List Component message');
  }
   HandleClick(): void  {}
}
```

```
<!-- customer-list.component.html -->
<div>
   {{GetMessage()}}
   <input type="button" value="CustomerListButton" (click)="HandleClick()">
</div>
```

#### 第 4 步 – 定义样式

打开 `style.css` 并添加以下内容：

```
div{
   padding: 20px;
   margin-top: 10px;
   border: 1px solid black;
}
```

#### 第 5 步 – 运行应用程序

为了正确学习和理解变更检测，请使用 `ng serve --prod` 命令在生产模式下运行应用程序。

![](img/Image58744.jpg)

**图 29.8**

打开开发者工具。你会看到每个组件都输出了一条消息。由于变更检测在启动时会执行两次，因此你会看到每条消息出现两次。

![](img/Image58779.jpg)

**图 29.9**

#### 第 6 步 – 点击按钮

清空控制台，然后点击任意组件中的按钮。

你会发现，无论点击哪个按钮，每个组件的消息都会显示出来——这意味着每个组件都被重新渲染了。

![](img/Image58821.jpg)

**图 29.10**

#### 第 7 步 – 将应用程序与 zone.js 断开连接

让我们将应用程序与 `zone.js` 断开连接。

为此，从 `polyfills.ts` 文件中移除导入语句，并将 `main.ts` 的内容修改如下：

```
platformBrowserDynamic().bootstrapModule(AppModule,{ngZone:'noop'})
   .catch(err => console.error(err));
```

#### 第 8 步 – 测试输出

运行应用程序。初始消息仍然不受影响。

清空开发者控制台，然后点击按钮。

由于上一步中移除了 `zone.js`，不再有变更检测的自动触发，因此你不会收到任何消息。

#### 第 9 步 – 使用 tick 方法实现手动变更检测

在 `CustomerListComponent` 中注入 `ApplicationRef` 服务，并在 `HandleClick` 方法中执行 `tick` 方法。

```
export class CustomerListComponent{
   constructor(private app: ApplicationRef){

  }
   ……
   HandleClick(): void  {
     this.app.tick();
  }
}
```

#### 第 10 步 – 测试输出

点击 `CustomerListComponent` 中的按钮。

虽然你得到了输出，但这并不是一个令人满意的输出。点击按钮后，每个组件都会被渲染，因为 `ApplicationRef.tick` 方法会触发整个层级中每个组件的变更检测。

如果我们只想触发特定组件的变更检测，而不是整个层级，该怎么办？这可以通过一个名为 `ChangeDetectorRef` 的 Angular 服务来实现。

#### 第 11 步 – 使用 ChangeDetectionRef 服务实现手动变更检测

在 `CustomerAddComponent` 中注入 `ChangeDetectionRef` 服务，并在 `HandleClick` 方法中触发变更检测，如下所示：

```
export class CustomerAddComponent {
   constructor(private cd: ChangeDetectorRef){

  }
……
   HandleClick(): void  {
     this.cd.detectChanges();
  }
```

#### 第 12 步 – 测试应用程序

这一次，点击 `CustomerAddComponent` 内部的按钮。它只会显示 CustomerAddComponent 的消息，这意味着只有 `CustomerAddComponent` 被渲染。

## 从特定组件中分离变更检测

通过使应用程序无 zone，我们影响了整个应用程序。如果我们只想对某个特定组件这样做呢？

这可以通过 `ChangeDetectorRef` 类的 `detach` 方法来实现。

### 第 1 步 – 准备项目

创建一个新项目 lab19-ng，然后像上一个项目一样创建 Customer、CustomerList、CustomerAdd 和 Product 组件。

### 第 2 步 – 分离变更检测

从 `CustomerListComponent` 中分离变更检测，如下所示：

```
export class CustomerListComponent implements OnInit {
   constructor(private cd: ChangeDetectorRef) {}
   ngOnInit(): void {
     this.cd.detach();
  }
……
```

### 第 3 步 – 测试应用程序

在生产模式下运行应用程序。

**初始消息**

分离变更检测器和无 zone 的 Angular 是两件不同的事情。

变更检测器负责检测 Angular 组件中的变化，而无 zone 的 Angular 则是关于禁用变更检测的自动触发。

![](img/Image58830.jpg)

**图 29.11**

这一次我们分离了变更检测器本身。因此，在加载应用程序时，控制台中不会出现 `CustomerListComponent` 的消息。

（我相信你知道为什么消息会显示两次。我们已经多次提到过。）

**点击按钮后的输出**

现在，点击组件内部的按钮。无论点击哪个按钮，输出始终如下：

![](img/Image58877.jpg)

**图 29.12**

你可能对一件事感到有些困惑。

**为什么当点击 CustomerListComponent 内部的按钮时，其他组件也会渲染？**

我们的应用程序仍然有 zone.js，因此每次事件发生后，`ApplicationRef` 服务的 `tick` 方法会自动被调用。这将触发除 `CustomerListComponent` 之外的所有组件的变更检测（因为变更检测器已被分离）。

### 第 4 步 – 手动检测变化

在 `CustomerListComponent` 的 `HandleClick` 方法中手动检测变化，如下所示：

```
   HandleClick(): void {
     this.cd.detectChanges();
  }
```

### 第 5 步 – 测试应用程序

经过上述更改后，`CustomerList` 组件内部的按钮点击事件的行为略有不同。点击后，你会在控制台中看到 `CustomerListComponent` 的消息以及其他组件的消息。

## OnPush 变更检测策略

还有另一种在组件级别控制变更检测的方法。即通过更改变更检测策略。默认策略使变更检测始终运行。

通过将其设置为 `OnPush`，我们将其限制为仅以下特定情况：

*   当组件内触发事件时。
*   当组件的输入属性引用发生变化时。
*   当使用 `async` 管道消费的可观察对象发出新值时。

### 第 1 步 – 将 OnPush 设置为 ChangeDetectionStrategy

打开 `CustomerAddComponent` 并将其变更检测设置为 `OnPush`，如下所示：

```
@Component({
   selector: 'app-customer-add',
   templateUrl: './customer-add.component.html',
   styleUrls: ['./customer-add.component.css'],
```





## 步骤 2 – 执行应用程序

你将看到以下输出：

### 初始执行

![](img/Image58961.jpg)

**图 29.13**

Angular 首次为应用程序触发了变更检测。

在之前的某个步骤中，我们已经将变更检测器从 `CustomerListComponent` 中分离出来。

因此，除了 `CustomerListComponent` 之外，我们从每个组件都收到了消息。

之后，`zone.js` 再次执行变更检测。这次，你还会发现 `CustomerAddComponent` 的消息也缺失了，因为它采用了 `OnPush` 策略。

### 按钮点击 – 除 CustomerAddComponent 之外

点击除 `CustomerAddComponent` 按钮之外的所有按钮。你将看到以下输出：

![](img/Image58996.jpg)

**图 29.14**

如你所见，没有显示 `CustomerList` 和 `CustomerAddComponent`，因为我们已将变更检测器从其中一个组件分离，而另一个组件采用了 `OnPush` 作为默认策略。

### 点击 `CustomerAddComponent` 按钮

你将看到以下输出：

![](img/Image59062.jpg)

**图 29.15**

在 `CustomerAddComponent` 内部事件触发后，我们收到了 `CustomerAddComponent` 的消息。

这证明了 `OnPush` 的第一点：当组件内部触发事件时，该组件的变更检测会被触发。

## 步骤 3 – 创建一个类来保存数据

创建一个简单的类 `CustomerAddData`，如下所示：

```
export class CustomerAddData{
   CustomerName: string;
}
```

## 步骤 4 – 创建输入属性

接下来，在 `CustomerAddComponent` 内部创建一个输入属性，如下所示：

```
export class CustomerAddComponent {
   @Input() cData: CustomerAddData;
   ……
```

## 步骤 5 – 修改 CustomerComponent

然后，在 `CustomerComponent` 中创建一个 `CustomerAddData` 实例，并将其赋值给 `CustomerAddComponent` 的输入属性，如下所示：

```
export class CustomerComponent  {
   CustomerData: CustomerAddData={CustomerName:"Sukesh"};
   ……
```

```
<!-- customer.component.html -->
<div>
   {{GetMessage()}}
   <input type="button" value="CustomerButton" (click)="HandleClick()">
   <app-customer-list></app-customer-list>
   <app-customer-add [cData]="CustomerData"></app-customer-add>
</div>
```

## 步骤 6 – 重新定义 HandleClick 方法

在 `CustomerComponent` 中重新定义 `HandleClick` 方法，如下所示：

```
HandleClick(): void  {
     this.CustomerData.CustomerName="ABCD";
  }
```

## 步骤 7 – 测试应用程序

如果你期望在点击 `CustomerComponent` 中的按钮后看到 `CustomerAddComponent` 重新渲染，那么说明你还没有正确理解变更检测的第二点。该点指出，只有当组件输入属性的引用发生改变时，变更检测才会被触发，而当前代码并没有做到这一点，它只是修改了对象本身。

## 步骤 8 – 改变引用

在 `CustomerComponent` 中重新定义 `HandleClick` 方法，如下所示：

```
   HandleClick(): void  {
     this.CustomerData.CustomerName="ABCD";
  }
```

## 步骤 9 – 测试输出

这次，你会发现点击 `CustomerComponent` 中的按钮后，`CustomerAddComponent` 的消息显示出来了。

## 步骤 10 – 巩固你的技能

证明变更检测的第三点将作为你的练习任务。

到目前为止，我们已经完成了许多实验。我认为，现在你已经足够聪明，可以自己完成这个任务了。

*   创建一个服务。
*   从中暴露一个 `Subject`。
*   在 `CustomerAddComponent` 中使用 `async` 管道订阅该 `Subject`。
*   在其他组件中让该 `Subject` 发出新数据。

#### 总结

在本章中，我们详细讨论了变更检测器。本章的内容并不要求你全部记住。只需记住，让 Angular 应用程序实现 *无 zone* 和 *OnPush*，变更检测可以显著提升应用程序性能。至此，我们结束了第 18 站的旅程。在开始第 19 站的旅程之前，让我们快速回顾一下本章所学的内容：

*   我们讨论了变更检测，它会遍历绑定、计算表达式、与之前的值进行比较，并在必要时更新 DOM。
*   我们了解到，默认情况下，在每个变更检测周期中，层级结构中的每个组件都会被检查是否有变化，并在需要时重新渲染。
*   我们了解到，Angular 在应用程序初始化后首次执行变更检测。之后，每当 DOM 事件被触发、HTTP 请求完成、宏任务（如 `setTimeout` 和 `setInterval`）的回调方法执行完毕，或微任务（如 *Promise*）完成时，变更检测都会被触发。
*   我们了解到，Angular 已经对所有的底层 JavaScript API 进行了猴子补丁（monkey patching），并在这些 API 执行结束时显式地执行变更检测。Angular 使用了 `zone.js` 库来实现猴子补丁。
*   我们了解到，在开发模式下，变更检测默认执行两次。
*   我们了解到，在开发模式下，Angular 会执行两次变更检测。第一次运行时，DOM 会以最新的组件状态进行渲染；第二次运行时，它会确认 DOM 在上一次重新渲染后没有发生变化。如果发生了变化，我们会得到一个运行时错误——`ExpressionChangedAfterItHasBeenChecked`。
*   我们了解到，在应用程序初始化期间，变更检测会执行两次。这会产生以下可能性：
    *   开发模式 + 应用程序初始化时间 = 变更检测将执行四次。
    *   开发模式 + 其他变更检测触发器（如事件处理程序、宏任务等）= 变更检测将执行两次。
    *   生产模式 + 应用程序初始化时间 = 变更检测将执行两次。
    *   生产模式 + 其他变更检测触发器（如事件处理程序、宏任务等）= 变更检测将只执行一次。
*   我们明确了 `zone.js` 与变更检测的执行方式或内部逻辑无关。它的核心目的是对底层 API 进行猴子补丁，以便在需要时自动触发变更检测。
*   我们了解到，我们可以将 `zone.js` 从 Angular 应用程序中断开，之后将不再有自动的变更检测触发。
*   我们了解到，Angular 应用程序必须有一个 zone 来执行应用程序，因此移除 `zone.js` 会导致应用程序崩溃。我们演示了 `NoopNgZone`——这是 Angular 提供的一个 zone 对象，它不会像 `zone.js` 那样对底层 API 进行猴子补丁。
*   我们了解了 `ApplicationRef` 服务，它提供了 `tick` 方法，我们可以使用该方法在应用程序中显式触发变更检测。
*   我们讨论了 polyfills——这些库为现有的 JavaScript 添加了一些额外功能，并使不兼容的浏览器变得兼容。
*   我们讨论了 `polyfill.ts` 文件，我们会在其中导入期望应用程序拥有的 polyfills。默认情况下，创建应用程序时，它只包含一个针对 `zone.js` 的入口语句。
*   我们讨论了 `ChangeDetectorRef` 服务，它允许我们为单个组件触发变更检测。
*   我们了解到，我们可以使用 `ChangeDetectorRef` 类的 `detach` 方法将变更检测器从特定组件中分离。
*   我们研究了 `OnPush` 变更检测策略，该策略将变更检测限制为仅在以下某些情况下触发：




*   当事件在组件内部触发时。
*   当组件输入属性的引用发生变化时。
*   当使用 async 管道订阅的可观察对象发出新值时。

## 第 30 章

### Angular 元素

#### 简介

在前往第 19 站的旅程中，我们将发现一个不那么出名但很有用的特性——Angular 元素。

#### 什么是 Angular 元素？

你是否曾想过在非 Angular 项目中使用你的 Angular 组件？

如果有，那么 Angular 元素就是实现这一目标的方式。Angular 元素是可以打包为自定义元素（即 Web 组件）的 Angular 组件。

有了它，你就可以在任何地方使用你的组件，例如 React、Vue 等。

#### 实验 20 – 创建 Angular 元素

**步骤 1 – 创建一个新的 Angular 项目**

创建一个新的 Angular 项目 `lab20-ng`。

**步骤 2 – 创建一个新组件**

创建一个新的 Angular 组件 `MyReusable`。

```
export class MyReusableComponent {
   Message = ‘Initial Message’;
   constructor() {}

   ChangeMessage(): void {
     this.Message = ‘Changed Message’;
  }
}
```

```
<h2>Message is : {{Message}}</h2>
<input type=”button” value=”Change Message” (click)=”ChangeMessage()”>
```

**步骤 3 – 使用组件**

在 `AppComponent` 中使用上述组件。

```
<!-- app.component.html -->
<app-my-reusable></app-my-reusable>
```

**步骤 4 – 测试应用程序**

使用 `ng serve` 命令运行应用程序，确保一切按预期工作。

**初始输出**

![](img/Image59143.jpg)

**图 30.1**

**点击按钮后**

![](img/Image59180.jpg)

**图 30.2**

**步骤 5 – 为 Angular 元素配置项目**

如你所知，此项目的目标是创建一个 Angular 元素。

为此，我们需要一个名为 `document-register-element` 的库。

可以使用 `npm install` 命令下载它，然后通过在 `polyfill.ts` 文件中导入它来将其包含在应用程序中。

还有另一种更简单的方法。我们可以使用 `ng add @angular/elements` 命令，如下所示：

![](img/Image59223.jpg)

**图 30.3**

`ng add` 命令专门用于处理第三方库。它会下载库并更新 `package.json`，还会执行第三方库所需的应用程序中的其他必要配置。

**步骤 4 – 将 Angular 组件配置为 AngularModule**

为此，在 `AppModule` 中定义一个构造函数，如下所示：

```
import {Injector, NgModule} from ‘@angular/core’;
import {createCustomElement} from ‘@angular/elements’;
import {BrowserModule} from ‘@angular/platform-browser’;
import {AppComponent} from ‘./app.component’;
import {MyReusableComponent} from ‘./my-reusable/my-reusable.component’;

export class AppModule {
   constructor(private injector: Injector) {
     const custom = createCustomElement(MyReusableComponent, {
       injector: this.injector,
    });
     customElements.define(‘my-custom-angular-element’, custom);
  }
}
```

在上述代码中，我们在 `AppModule` 中注入了根模块的注入器实例，然后将 `MyReusableComponent` 配置为 Angular 元素。

**步骤 5 – 构建项目**

像往常一样使用 `ng build` 命令构建项目，但这次要加上一个额外的标志。

![](img/Image59263.jpg)

**图 30.4**

你注意到 `--output-hashing none` 标志的作用了吗？

你还记得构建命令后生成的每个文件名后面都会附加一个哈希值吗？例如 `main.3a82886dd6c280a056fd.js`。

现在这个哈希值不再存在了。

我们没有什么特别的原因要去掉这里的哈希值。这只是为了让名称更简单。

**步骤 6 – 项目的示例 HTML 文件**

为了测试上述 Angular 元素，我们不需要一个 Angular 项目。

![](img/Image59272.jpg)

**图 30.5**

为了确保你正确理解了这个概念，在机器上的某个位置创建一个名为 `Test-Angular-Elements` 的独立文件夹。

然后在该文件夹内创建一个名为 `index.html` 的新 HTML 文件，并将以下内容放入其中：

```
<!doctype html>
<html lang=”en”>
<head>
     <title>Angular Elements Demo</title>
</head>
<body>
     <my-custom-angular-element></my-custom-angular-element>
     <script src=”../lab20-ng/dist/lab20-ng/runtime.js” ></script>
     <script src=”../lab20-ng/dist/lab20-ng/polyfills.js” ></script>
     <script src=”../lab20-ng/dist/lab20-ng/main.js” ></script>
</body>
</html>
```

**步骤 7 – 测试 HTML 文件**

在你选择的任何浏览器中打开上一步创建的 `index.html` 文件。

**点击按钮前**

![](img/Image59356.jpg)

**图 30.6**

**点击按钮后**

![](img/Image59390.jpg)

**图 30.7**

虽然输出结果令人满意，但其中有一个小错误。打开开发者工具检查一下。

![](img/Image59398.jpg)

**图 30.8**

记住，我们在 `AppModule` 中仍然将 `AppComponent` 作为引导组件。

**步骤 8 – 移除引导组件**

我们的目标是创建一个 Angular 组件。这里没有必要保留根/引导组件。因此，按如下方式从 `AppModule` 中移除 `bootstrap` 部分：

```
@NgModule({
   declarations: [AppComponent, MyReusableComponent],
   imports: [BrowserModule],
   providers: [],
})
export class AppModule {
```

**步骤 9 – 重新构建应用程序**

再次像之前一样构建应用程序。

**步骤 10 – 测试 HTML 文件**

重新执行 `index.html` 文件。这次你会在控制台中发现以下错误：

![](img/Image59434.jpg)

**图 30.9**

Angular 期望在根模块中指定一个引导组件，除非在 `AppModule` 中定义了 `ngDoBootstrap` 方法。

**步骤 11 – 定义 ngDoBootstrap 方法**

在 `AppModule` 中定义一个空的 `ngDoBootstrap` 方法，如下所示：

```
   ngDoBootstrap (){}
```

`ngDoBootstrap` 方法主要用于当我们想根据某些条件手动加载引导组件时。现在先不用担心这个。

**步骤 12 – 重新构建应用程序**

再次使用相同的标志重新构建应用程序。

**步骤 13 – 测试 HTML 文件**

最后，你将得到一个没有错误且能正常工作的输出。

#### 总结

至此，我们结束了前往第 19 站的旅程。最后，在下一章中，我们将看到前往最后一站——第 20 站的旅程。在那站中，我们将讨论尚未涉及的主题。在此之前，像往常一样，让我们回顾一下本章所学的内容：

*   在本章中，我们学习了如何创建 Angular 元素，这些元素是打包为自定义元素（即 Web 组件）的 Angular 组件。

*   我们了解到 Angular 元素是在非 Angular 项目中使用 Angular 组件的方式。

*   我们演示了 `ng add` 命令。该命令专门用于处理第三方库。它会下载库并更新 `package.json`，还会执行第三方库所需的应用程序中的其他必要配置。

*   我们介绍了 `--output-hashing none` 标志，它可以与 `ng build` 命令一起使用，以指示 Angular CLI 在命名包时不需要哈希。

*   我们了解到，在用于 Angular 元素的 Angular 项目中，没有必要保留根/引导组件。




*   我们了解到，在每个 Angular 项目中都必须指定一个引导组件。这同样适用于针对 Angular 元素的项目。为了解决这个难题，我们引入了 `ngDoBootstrap` 方法，它允许我们手动引导组件。

## 第 31 章

## 剩余内容

## 引言

通过本章，你将抵达目的地——第 20 站。

你值得热烈的掌声。你对学习的投入和热情令人赞叹。

你完成了整个旅程，这是一项巨大的成功。

在本章中，我们将快速了解本书中尚未涉及的一些主题。

## ViewChildren

你还记得之前某个实验中使用的 `ViewChild` 装饰器吗？它允许我们在组件类中获取模板元素的引用。让我们快速回顾一下。

**第 1 步 – 创建新项目**

使用 `ng` 命令创建一个新的 Angular 项目。

**第 2 步 – 修改 AppComponent 内容**

将 `AppComponent` 内容修改为以下代码：

```typescript
export class AppComponent {
  @ViewChild(“MyTextbox”) element: HTMLInputElement;
  ChangeValue(): void{
    this.element.value=”My Value”;
  }
}
```

```html
<input type=”text” #MyTextbox>
<input type=”button” value=”Change Value” (click)=”ChangeValue()”>
```

**第 3 步 – 运行应用程序**

使用 `ng serve` 命令运行应用程序。你将得到以下输出：

**点击按钮前**

![](img/Image59525.jpg)

**图 31.1**

**点击按钮后**

![](img/Image59534.jpg)

**图 31.2**

**第 4 步 – 修改 AppComponent**

现在，将 `AppComponent` 模板修改为以下代码：

```html
<input type=”text” #MyTextbox><br><br><input type=”text” #MyTextbox><br><br>
<input type=”button” value=”Change Value” (click)=”ChangeValue()”>
```

**第 5 步 – 测试输出**

现在检查输出。结果如下：

但当你点击按钮时，只有第一个文本框被填充了值。

![](img/Image59572.jpg)

**图 31.3**

如果你想获取所有模板元素的引用怎么办？答案是使用 `ViewChildren` 装饰器。

**第 6 步 – 修改 AppComponent 代码**

将 `AppComponent` 代码修改为以下内容：

```typescript
@ViewChildren(‘MyTextbox’) elements: QueryList<ElementRef>;
ChangeValue(): void {
  this.elements.forEach((x) => {
    x.nativeElement.value = ‘My Value’;
  });
}
```

**第 7 步 – 重新检查输出**

这次，你会发现两个文本框都更新了新值。

## 内容投影

内容投影是 Angular 的一个概念，它允许我们将 HTML 内容从父组件投影到子组件。

在子组件中，这些投影内容可以通过一个名为 `ng-content` 的内置 Angular 组件来访问。让我们通过一个演示来理解。

**第 1 步 – 获取项目**

创建一个新项目 `lab22-ng`。

**第 2 步 – 创建新组件**

创建一个名为 `MyBoxedContentComponent` 的新 Angular 组件。

**第 3 步 – 使用组件**

接下来，在 `AppComponent` 中使用 `MyBoxedContentComponent`，如下所示：

```html
<app-my-boxed-content>
  <header>My Header</header>
  <section>My Content<br>My Content again</section>
</app-my-boxed-content>
```

你可以在上述代码中看到一些有趣的东西。你可以在 `MyBoxedContentComponent` 选择器之间找到一些自定义的 HTML 内容。

这被称为内容投影——HTML 内容从父组件投影到子组件。

**第 4 步 – 访问投影组件**

最后，让我们在子组件中访问投影组件。

将 `MyBoxedContentComponent` 模板重新定义为以下内容：

```html
<div style=”border: 1px solid black;padding: 20px;”>
  <ng-content></ng-content>
</div>
```

**第 5 步 – 运行项目**

运行应用程序。你将得到以下输出：

![](img/Image59633.jpg)

**图 31.4**

## 讨论 – 续

这是一个内容投影的简单示例。

但还有更多内容。我们有一种叫做内容投影插槽的东西——它们帮助我们将 HTML 内容投影到子组件中特定的 `ng-content` 标签。

简而言之，我们可以在子组件中拥有多个 `ng-content` 标签，每个标签指向投影内容中的特定内容。

## 实验 – 续

**第 6 步 – 更新 MyBoxedContentComponent**

将 `MyBoxedContentComponent` 中的内容修改为以下代码：

```html
<div style=”border: 1px solid black;padding: 20px;”>
  <h1>
    <ng-content select=”header”></ng-content>
  </h1>
  <div style=”border:1px dotted ;padding: 10px;”>
    <ng-content select=”section”></ng-content>
  </div>
</div>
```

**第 7 步 – 检查输出**

你将得到以下输出：

![](img/Image59716.jpg)

**图 31.5**

如你所见，投影内容被分发到不同的插槽中。

查看开发者工具以获得更清晰的理解。

![](img/Image59769.jpg)

**图 31.6**

## ContentChild

`ContentChild` 是一个装饰器，它允许我们引用投影到组件中的匹配元素。让我们通过一个演示来理解。对于演示，我们将重用之前的项目。

**第 1 步 – 修改 AppComponent**

将 `AppComponent` 内容修改为以下代码：

```html
<app-my-boxed-content>
  <header #MyHeader>My Header</header>
  <section>My Content <br>My Content again</section>
</app-my-boxed-content>
```

**第 2 步 – 修改子组件**

将 `MyBoxedContentComponent` 内容修改为以下代码：

```html
<div style=”border: 1px solid black;padding: 20px;”>
  <h1>
    <ng-content select=”header”></ng-content>
  </h1>
  <div style=”border:1px dotted ;padding: 10px;”>
    <ng-content select=”section”></ng-content>
  </div>
  <input type=”button” value=”ChangeStyle” (click)=”ChangeStyle()”>
</div>
```

唯一的改变是在模板中添加了一个新按钮——ChangeStyle。

**第 3 步 – 在 MyBoxedContentComponent 中使用 ContentChild**

在 `MyBoxedContentComponent` 中声明一个 `ElementRef` 类型的属性，为其附加 `ContentChild` 装饰器，在构造函数中注入 `Renderer2` 服务，最后定义 `ChangeStyle` 方法，如下所示：

```typescript
export class MyBoxedContentComponent implements OnInit {
  @ContentChild(‘MyHeader’) HeaderElement: ElementRef;
  constructor(private renderer: Renderer2) {}
  ChangeStyle(): void {
    this.renderer.setStyle(
      this.HeaderElement.nativeElement,
      ‘font-style’,
      ‘italic’
    );
  }
}
```

**第 4 步 – 测试应用程序**

运行应用程序，然后点击按钮。你会发现 header 元素被添加了斜体样式。

![](img/Image59819.jpg)

**图 31.7**

## ContentChildren

`ContentChild` 和 `ContentChildren` 之间的区别与 `ViewChild` 和 `ViewChildren` 之间的区别相同。一个返回匹配选择器的第一个模板元素的引用，另一个返回 `QueryList`。

## Angular 生命周期

Angular 组件生命周期也可以称为生命周期钩子，开发者可以接入这些钩子并编写一些自定义逻辑。

我们在之前的实验中已经看到了大部分钩子的实际应用。让我们快速回顾一下。

*   **构造函数**（仅调用一次）





这不是一个 Angular 生命周期事件/钩子。它在任何面向对象语言中都能见到，TypeScript 也不例外。一旦类的实例被创建，它就会被调用。

*   `ngOnChanges`

    它会在两种情况下执行：一是在*构造函数*之后开始时执行一次，然后每当组件的数据绑定输入属性发生变化时执行。这将是生命周期中的第一个方法，它允许我们使用组件的数据绑定输入属性。在此之前（即在构造函数中），数据绑定的输入属性是未赋值的。我们在*第 26 章：Angular 指令*中已经看到了它的实际应用。

*   `ngOnInit`（仅调用一次）

    它会在第一次 `ngOnChanges` 之后执行，并且更适合用于初始化逻辑。我们在*第 26 章：Angular 指令*中已经看到了它的实际应用。

*   `ngDoCheck`（多次调用）

    它会在每次 Angular 变更检测运行时执行。我们在*第 26 章：Angular 指令*中已经看到了它的实际应用。

*   `ngAfterContentInit`

    它会在 Angular 将外部内容投影到组件视图之后执行。

    如果我们想在初始化阶段访问组件的投影内容，这个方法非常合适。`ngOnInit` 无法满足这个目的。`ngAfterContentInit` 方法是处理由父组件投影到组件中的模板元素的理想选择。

*   `ngAfterContentChecked`

    它会在 Angular 检查投影到组件中的内容之后执行。这是针对投影内容的变更检测检查。

*   `ngAfterViewInit`

    它会在视图（即组件的模板）初始化之后执行。

    `ngAfterViewInit` 方法是处理视图中模板的候选方法。（还记得我们在之前的某个实验中是如何在此方法中设置文本框焦点的吗？）

*   `ngAfterViewChecked`

    每当 Angular 完成对组件及其子组件的变更检测时，就会调用 `ngAfterViewChecked`。

*   `ngDestroy`

    这是清理资源的最佳方法。当组件/指令实例被销毁时，它会被调用。

## 部署文件

到目前为止，我们在本书中已经多次构建了项目。让我们来谈谈执行 `ng build` 命令后生成的文件。

*   `main.***.js` 或 `main.js`

    这是包含我们代码的打包 JavaScript 文件。我们所有的应用程序代码都被打包到这个 JavaScript 文件中。

    Angular 不会盲目地创建这个包。它会执行 tree-shaking，以确保所有未使用的组件、指令、服务和管道都被跳过。（在懒加载的情况下，你还会找到特定功能的包。）

*   `polyfills.***.js`

    这是一个打包的 JavaScript 文件，包含在 `polyfills.ts` 中导入的所有库。默认情况下，它只包含 `zone.js`。

    （我们在*第 29 章：变更检测*中讨论过它。）

*   `runtime.***.js`

    这是 webpack 加载器。该文件包含加载其他文件所需的 webpack 工具。

*   `style.***.css`

    这是 `angular.json` 文件中指定的所有 CSS 文件的打包文件。（我们在*第 28 章：Angular 样式*中讨论过它。）

    根据 *angular.json* 的配置，你可能会找到多个 CSS 包。

*   `script.***.js`

    与 CSS 文件类似，我们可以使用 `angular.json` 文件将 JavaScript 文件导入到应用程序中。

    此部分中提到的 JavaScript 文件将被打包到 `script.***.js` 中。

    ![](img/Image59826.jpg)

    **图 31.8**

*   `vendor.***.js`

    Angular 和其他第三方供应商脚本被打包到这个文件中。

    在生产模式下，你会找不到这个文件，因为它被打包到了 `main.***.js` 中。

    你可以通过以下方式指示 Angular CLI 创建一个单独的包：

    1.  `ng build --prod --vendor-chunk true`

*   `*****.map.js`

    你会发现开发构建中会生成多个扩展名为 `map.js` 的文件。

    这些文件包含 TypeScript 源文件的信息，使得可以在运行时直接调试 TypeScript 文件。

## 关于 Angular 注入器的更多内容

在本书中，我们讨论了几种配置负责创建和注入服务的注入器的方法。让我们快速回顾一下。

![](img/Image59873.jpg)

**图 31.9**

我希望这个图是不言自明的。但还有两种配置 Angular 注入器的方法。

## 平台注入器和空注入器

之前，我们了解到 Angular 中有两种注入器。

我们在顶层有一个*模块注入器*层次结构，在其下方有一个*元素注入器*。

在*根模块注入器*之上还有两个注入器——*平台注入器*和*空注入器*。

**平台注入器**

*平台注入器*位于*空注入器*之下，*根模块注入器*之上。

我相信你一定在想它为什么存在。

**一个 Angular 应用程序中可以有多个根模块注入器吗**

不，不能。我们只有一个根模块注入器，它会在应用程序初始化时创建。

这里有一个重要的转折点。一个应用程序只能有一个根模块注入器，但一个页面可以包含多个 Angular 应用程序，每个应用程序都有自己的根模块注入器。

所有这些根注入器都是平台注入器的子级。

**实际中的多个 Angular 应用程序**

你还记得上一章关于 Angular Element 的内容吗？每个 Angular Element 都是一个自包含的组件，就像一个迷你 Angular 项目。

**如何配置平台注入器？**

要配置平台注入器，我们可以使用带有 `providedIn` 平台选项的 Injectable 装饰器。

1.  `@Injectable({providedIn: ‘platform’})`

2.  `export class MyService{…..`

**平台注入器有什么特别之处？**

*   当需要注入服务时，Angular 会首先询问组件的*元素注入器*。如果失败，则将责任交给位于其上方的组件的*元素注入器*。这个过程会一直持续到到达*根组件注入器*。

*   在*根组件注入器*之后，责任将委托给直接的*模块注入器*。如果失败，则轮到其上方的*模块注入器*。这个过程会一直持续到到达*根模块注入器*。

*   在*根模块注入器*之后，责任将委托给*平台注入器*。

平台注入器会创建服务的全局唯一实例，该实例在平台级别是单例的，并在页面上的所有应用程序之间共享。

**空注入器**

空注入器位于树的顶部，负责抛出“*No provider*”错误。当平台注入器无法完成注入时，空注入器就会出现，并直接抛出“*No provider error*”。

## ProvidedIn – any

使用 `Injectable` 装饰器的 `providedIn` any 选项，我们可以同时配置根模块注入器和每个子模块注入器。它确保每个懒加载模块获得其唯一的实例。

1.  `@Injectable({providedIn: ‘any’})`

2.  `export class MyService{…..`

例如，假设我们有一个 Angular 应用程序，其中包含以下 Angular 模块：AppModule（根模块）、CustomerModule、ProductModule、SupplierModule、LoggerModule 和 SecurityModule。

假设应用程序配置如下：

*   AppModule 是根模块，它将懒加载 CustomerModule、ProductModule 和 SupplierModule。





`AppModule`加载`LoggerModule`（急切加载意味着`LoggerModule`被导入到`AppModule`中）。

最后，`SecurityModule`在`CustomerModule`中被急切加载。

考虑到上述事实，并且我们为`Injectable`装饰器附加了`providedIn: 'any'`，我们将得到以下输出：

- `AppModule`和`LoggerModule`将共享一个实例。
- 将为`ProductModule`创建一个独立的服务实例。
- 将为`SupplierModule`创建一个独立的服务实例。
- 将为`CustomerModule`创建一个独立的服务实例，并且该实例将与`SecurityModule`共享。

## Summary

至此，我们到达了第 20 站，这也是我们最后的旅程。在最后的说明之前，让我们回顾一下本章的学习内容：

- 我们再次演示了`ViewChild`装饰器。使用`ViewChild`，我们可以获取视图中定义的元素的引用。
- 我们了解到`ViewChild`装饰器只能提供第一个匹配元素的引用，而使用`ViewChildren`装饰器，我们可以获取视图中所有匹配元素的引用。
- 我们学习了 Angular 中的内容投影，它允许我们将父组件的 HTML 内容投影到子组件中。在子组件中，投影的内容将通过`ng-content`标签访问。
- 我们学习了内容投影插槽，它帮助我们将 HTML 内容投影到子组件中特定的`ng-content`标签。
- 我们学习了`ContentChild`装饰器，它允许我们引用投影到组件中的第一个匹配元素。
- 我们学习了`ContentChildren`装饰器，它允许我们引用投影到组件中的所有匹配元素。
- 我们在本章中再次回顾了所有 Angular 生命周期事件。
- 我们讨论了所有文件由`ng build`命令生成。
- 我们在本章中再次回顾了模块注入器和元素注入器。我们回顾了配置注入器的所有不同方式及其用例。
- 我们讨论了平台注入器，它创建服务的全局单例实例，该实例在平台级别是单例的，并在页面上的所有应用程序之间共享。
- 我们了解到通过使用`Injectable`装饰器的`providedIn: 'platform'`选项，我们可以配置平台注入器。
- 我们讨论了最顶层的空注入器，它负责抛出“no provider”错误。
- 我们了解到通过使用`Injectable`装饰器的`providedIn: 'any'`选项，我们可以同时配置根模块注入器和每个子模块注入器。使用此设置，所有急切加载的模块共享一个实例；然而，每个惰性加载的模块都会获得其唯一的实例。

## Section 6

## Summary

在最后的第 6 部分（共 10 章）之后，你已经成为一名 Angular 开发者，这也是我们旅程的终点。

**第 22 章 – 组件化风格实战**

- 我们讨论了现代世界中一种新的 UI 开发方法——组件化风格。这是一种 UI 设计方法，允许我们将 UI 创建为多个更小、可复用组件的组合。
- 我们了解到 Angular 并不是组件化方法的先驱，它只是遵循了这种方法。其他技术（如 React 和 Polymer）也遵循类似的过程。
- 我们了解到这种方法使我们的**代码维护变得容易**，并且**允许多个 UI 开发者并行工作**。
- 我们讨论了功能组件，它们代表应用程序中的主要组件，通常通过路由访问。
- 我们了解到有时会将功能组件拆分为更小的组件，以使代码可读且易于管理。容器-展示模式是业界为此目的常用的模式之一。
- 我们快速讨论了容器组件和展示组件之间的区别。容器组件通常是智能的，而展示组件被称为哑组件，它们处理 UI 展示。
- 我们创建了自定义输入属性，用于将数据从外部组件传递到内部组件。
- 我们创建了自定义输出属性，用于从内部组件引发事件，该事件可以在外部组件中处理。
- 我们再次回顾了`ViewChild`装饰器和模板引用变量，并学习了如何引用组件类的视图元素。
- 我们在本章中再次学习了使用环境变量。我们使错误处理代码在不同环境（开发和生产）下表现不同。
- 我们再次回顾了`ngOnInit`，并学习了它如何最适合初始化逻辑。
- 我们学习了`ngAfterViewInit`生命周期，它是需要访问已渲染控件的逻辑的理想候选。
- 我们了解到在模板驱动表单中，我们不需要显式地将`ngForm`指令分配给`form`标签。

**第 23 章 – Angular 路由**

- 我们学习了当组件 HTML 简单时，如何使用`template`属性代替`templateUrl`。
- 我们再次回顾了`router-outlet`组件，它为不同的 URL 显示不同的组件。
- 我们讨论了`routerLink`指令，它允许我们在不刷新整个页面的情况下导航路由。
- 我们学习了`routerLinkActive`，它允许我们在路由激活时添加 CSS 类。
- 我们讨论了默认路由，当 URL 为空时会加载它们。
- 我们了解到可以在根级别和子级别定义默认路由。
- 我们详细研究了惰性加载，并学习了它如何减少初始加载时间。
- 我们讨论了预加载策略，它允许我们决定惰性加载的模块是否需要异步加载。

**第 24 章 – Angular 模块**

- 我们学习了使用 Angular CLI 创建组件和模块。
- 我们学习了 Angular 模块如何使组件开发更容易。我们将相关组件分组到模块中，然后只导出其中的一部分。未导出的组件在 Angular 模块中成为私有组件。
- 我们了解到 Angular 模块也对指令和管道进行分组，除非显式导出，否则它们对该模块是私有的。
- 我们学习了服务模块，它们是专门用于配置服务及其依赖服务的注入器的 Angular 模块。`HttpClientModule`就是这样一个服务模块的例子。
- 我们在上一章中已经讨论了 Angular 模块的第三个优势——惰性加载。
- 我们了解到即使 Angular 模块中的私有组件也可以通过路由访问。
- 我们了解到`BrowserModule`导入`CommonModule`并重新导出它。因此，`CommonModule`导出的指令在`AppModule`内部可见。
- 我们了解到 Angular 构建过程中的树摇机制确保所有未使用的组件从最终构建中移除，除非它们通过路由被引用。如果组件未在任何其他组件的模板中使用，则被视为未使用。
- 我们了解到当模块被惰性加载时，Angular 会创建一个子模块注入器。

**第 25 章 – Angular 管道**

- 在本章中，我们学习了管道，它帮助我们封装应用程序中的转换逻辑。





* 我们了解到，需要创建一个类来生成管道，实现`PipeTransform`接口，并附加`Pipe`装饰器。
* 我们了解到，管道也像组件一样被封装在 Angular 模块中。
* 我们了解到，Angular 应用中常用的管道，如`json`、`async`、`uppercase`等，都定义在`CommonModule`中。
* 我们了解到，自定义 Angular 模块（通常称为`SharedModule`）用于封装所有自定义管道，其他模块在实际项目中会导入这些模块。
* 我们讨论了 TypeScript 中两种数据类型——`any`和`unknown`的区别。我们了解到，`any`类型的变量可以赋值给其他类型，而`unknown`类型的变量只能赋值给`unknown`类型的变量。
* 我们演示了 TypeScript 的 REST 参数。
* 我们了解到，纯管道仅在初始时以及输入值发生变化时执行。
* 我们了解到，非纯管道在每次变更检测后都会执行。

### 第 26 章 – Angular 指令

* 我们在本章中学习了指令。它们扩展了现有的 HTML。
* 我们了解到 Angular 有三种类型的指令。
* 第一种称为元素指令，允许我们创建新的 HTML 标签。元素指令在 Angular 中也可以称为组件。
* 第二种是属性指令，允许我们扩展现有 HTML 元素的行为。`ngClass`和`ngStyle`就是这类指令的典型例子。
* 第三种是结构型指令，允许我们改变现有 HTML 元素的结构。结构型指令与属性指令类似，会作为属性附加到 HTML 元素上。
* 我们了解到，结构型指令通常以星号（*）为前缀附加到 HTML 元素上。例如：`*ngFor`、`*ngIf`。
* 我们了解了为指令指定选择器的不同方式——属性选择器、ID 选择器、CSS 选择器和元素选择器。
* 我们演示了 Angular 中的`ElementRef`服务，它可以引用指令所附加的 HTML 元素。
* 我们了解了 Angular 中的`Render2`服务，它提供了处理 DOM 操作的各种方法。
* 我们再次理解了为什么`ngOnInit`方法更适合用于初始化逻辑。我们了解到，`constructor`在创建类的对象时执行，而`ngOnInit`在组件/指令初始化后执行。这里的“初始化”指的是实例已创建，并且所有属性都已用父组件传递的值初始化。
* 我们了解了参数化的`Input`装饰器，它允许我们以不同的名称将组件/指令的属性暴露给外部。
* 我们了解了`HostListener`装饰器，它允许我们处理指令所附加元素的事件。
* 我们了解了 Angular 的`ngOnChanges`生命周期事件，它在组件数据绑定属性的值发生变化时执行。
* 我们了解了 Angular 的`ngDoCheck`生命周期事件，它在每次变更检测时执行。
* 我们讨论了`ng-template`，它用于创建 Angular 模板。Angular 模板不会自动渲染，它们会在运行时根据某些自定义逻辑在其他 DOM 元素内部使用和渲染。
* 我们了解了`TemplateRef`服务，它提供了对`ng-template`内部定义内容的引用。
* 我们看到了`ViewContainerRef`服务的实际应用，它提供了容器的引用，可以将一个或多个视图附加到该容器上。
* 我们了解了`ComponentFactoryResolver`服务，它可以用于在运行时动态加载组件。
* 我们讨论了指令的微语法，它消除了显式创建`ng-template`元素的额外开销。

### 第 27 章 – Angular 表单

这是一个作业章节。在本章中，你需要分别用模板驱动方式和响应式方式完成一个示例演示。

### 第 28 章 – Angular 样式

* 我们讨论了在 Angular 应用中引入外部样式表的三种方式——在`index.html`文件中使用`link`标签、使用`CSS @import`以及使用`angular.json`文件。
* 我们了解到，`angular.json`文件中有一个名为`builds/styles`的部分，用于声明项目中的外部 CSS 文件。默认情况下，Angular 脚手架项目会包含一个`style.css`文件的条目。
* 我们演示了`CSS @import`，并了解到在执行`ng build`时，Angular CLI 会将`style.css`及其依赖的所有样式表文件打包成一个文件。
* 我们演示了使用`angular.json`文件导入样式表文件，并了解到`angular.json`文件中列出的所有样式表文件在执行`ng build`时会被打包成一个文件。
* 我们了解到，使用`angular.json`文件导入样式表文件比使用`CSS @import`更优。它允许我们指示 Angular CLI 在需要时生成多个包。
* 我们学习了如何使用`Component`装饰器的`styleURL`或`styles`属性将样式附加到单个组件。我们了解到，这些样式在构建后不会被打包到任何 CSS 包中，而是成为组件视图本身的一部分。
* 我们了解了`ViewEncapsulation`，它允许我们控制样式如何封装到组件视图中。
* 我们讨论了`Emulated`封装，这是默认模式。此模式会为组件的每个 DOM 元素附加一个唯一属性，并重命名每个 CSS 选择器，使样式仅对该组件生效。
* 我们讨论了`Native`封装，它遵循 HTML 5 的`ShadowDOM`方式。使用此模式，我们可以确保外部 CSS 不会影响组件内容，并且组件特有的样式也不会影响外部世界。这是可复用组件的最佳方式。
* 我们讨论了`None`封装，它会使每个组件特有的样式成为全局样式。

### 第 29 章 – 变更检测

* 我们讨论了变更检测，它会遍历绑定、计算表达式、与之前的值进行比较，并在必要时更新 DOM。
* 我们了解到，默认情况下，在每个变更检测周期中，层级结构中的每个组件都会被检查是否有变化，并在需要时重新渲染。
* 我们了解到，Angular 在应用初始化后第一次执行变更检测。之后，每当触发 DOM 事件、完成 HTTP 请求、宏任务（如`setTimeout`和`setInterval`）的回调方法执行完毕，或微任务（如`Promise`）完成时，都会触发变更检测。
* 我们了解到，Angular 对底层 JavaScript API 进行了猴子补丁（monkey patching），并在这些 API 结束时显式执行变更检测。Angular 使用了`zone.js`库来实现猴子补丁。
* 我们了解到，在开发模式下，变更检测默认执行两次。
* 我们了解到，在开发模式下，Angular 会执行两次变更检测。第一次运行时，DOM 会以最新的组件状态渲染；第二次运行时，它会确认 DOM 在上一次重新渲染后没有发生变化。如果发生了变化，我们会得到一个运行时错误——`ExpressionChangedAfterItHasBeenChecked`。




我们了解到，在应用初始化期间，变更检测会执行两次。这带来了以下可能性：

- 开发模式 + 应用初始化时间 = 变更检测将执行四次。
- 开发模式 + 其他变更检测触发（如事件处理、宏任务等）= 变更检测将执行两次。
- 生产模式 + 应用初始化时间 = 变更检测将执行两次。
- 生产模式 + 其他变更检测触发（如事件处理、宏任务等）= 变更检测仅执行一次。

我们明确了 `zone.js` 与变更检测的执行方式或内部逻辑无关。其核心目的是对底层 API 进行猴子补丁（monkey patching），以便在需要时自动触发变更检测。

我们了解到，我们可以将 `zone.js` 从 Angular 应用中断开，之后将不再有自动的变更检测触发。

我们了解到，Angular 应用必须有一个 zone 来执行应用，因此移除 `zone.js` 会导致应用崩溃。我们演示了 `NoopNgZone`——这是 Angular 提供的一个 zone 对象，与 `zone.js` 不同，它不会对底层 API 进行猴子补丁。

我们了解了 `ApplicationRef` 服务，它提供了 `tick` 方法，我们可以使用该方法在应用中显式触发变更检测。

我们讨论了 polyfills——这些库为现有 JavaScript 添加了一些额外功能，并使不兼容的浏览器变得兼容。

我们谈到了 `polyfill.ts` 文件，我们将在其中导入期望应用拥有的 polyfills。默认情况下，当应用创建时，它只包含一个针对 `zone.js` 的入口语句。

我们谈到了 `ChangeDetectorRef` 服务，它允许我们为单个组件触发变更检测。

我们了解到，我们可以使用 `ChangeDetectorRef` 类的 `detach` 方法，将变更检测器从特定组件上分离。

我们研究了 `OnPush` 变更检测策略，该策略将变更检测限制为仅在以下情况下触发：

- 当组件内触发事件时。
- 当组件输入属性的引用发生变化时。
- 当使用 `async` 管道消费的可观察对象发出新值时。

### 第 30 章 – Angular Elements

在本章中，我们学习了如何创建 Angular Elements，即打包为自定义元素（也称为 Web 组件）的 Angular 组件。

我们了解到，Angular element 是在非 Angular 项目中使用 Angular 组件的方式。

我们演示了 `ng add` 命令。该命令专门用于处理第三方库。它会下载库并更新 `package.json`，还会执行第三方库所需的其他必要配置。

我们介绍了 `--output-hashing none` 标志，它可以与 `ng build` 命令一起使用，用于指示 Angular CLI 在命名 bundle 时不需要哈希。

我们了解到，在专为 Angular Elements 设计的 Angular 项目中，没有必要设置根组件/引导组件。

我们了解到，在每个 Angular 项目中都必须指定一个引导组件。这也适用于针对 Angular Elements 的项目。为了解决这个难题，我们引入了 `ngDoBootstrap` 方法，它允许我们手动引导组件。

### 第 31 章 – 遗留内容

我们再次演示了 `ViewChild` 装饰器。使用 `ViewChild`，我们可以获取视图中定义的元素的引用。

我们了解到，`ViewChild` 装饰器只能提供第一个匹配元素的引用，而使用 `ViewChildren` 装饰器，我们可以获取视图中所有匹配元素的引用。

我们学习了 Angular 中的内容投影，它允许我们将 HTML 内容从父组件投影到子组件。在子组件中，投影的内容将通过 `ng-content` 标签访问。

我们了解了内容投影插槽，它帮助我们将 HTML 内容投影到子组件中特定的 `ng-content` 标签。

我们学习了 `ContentChild` 装饰器，它允许我们引用投影到组件中的第一个匹配元素。

我们学习了 `ContentChildren` 装饰器，它允许我们引用投影到组件中的所有匹配元素。

在本章中，我们再次复习了所有 Angular 生命周期事件。

我们讨论了 `ng build` 命令生成的所有文件。

在本章中，我们再次复习了模块注入器和元素注入器。我们复习了配置注入器的所有不同方式及其用例。

我们谈到了平台注入器，它创建服务的全局单例实例，该实例在平台级别是单例的，并在页面上的所有应用之间共享。

我们了解到，通过使用 `Injectable` 装饰器的 `providedIn: 'platform'` 选项，我们可以配置平台注入器。

我们谈到了最顶层的 null 注入器，它负责处理“没有提供者”的错误。

我们了解到，使用 `Injectable` 装饰器的 `providedIn: 'any'` 选项，我们可以同时配置根模块注入器和每个子模块注入器。使用此设置，所有急切加载的模块共享一个实例；然而，每个惰性加载的模块都会获得其唯一的实例。

# 这不是告别

我很高兴你已经读到了这里。我希望你喜欢这段漫长的旅程，也希望你的技能现在已经达到了新的水平。

*学习*和*玩游戏*是我众多爱好中的两个。

在这两个爱好中的丰富经验告诉我，两者都需要重复才能达到精通。

如果你是一个游戏玩家，你也很清楚这一点。如果你想通关任何游戏，就玩两遍。第一次，完成游戏；第二次，揭示所有秘密。

同样的原则也适用于学习。你可以计划重读这本书，重新审视你到目前为止学到的一切。或者至少，你可以计划复习每个章节的总结。

至此，我想感谢你，并祝贺你完成了这段旅程。

不过，让我向你保证，这还没有结束。学习永无止境，Angular 也是如此。现在，我想说，“请继续关注，这不是我写的唯一一本 Angular 书。”

我希望你喜欢这整个旅程。你可以通过我的 Twitter 账号 @sukeshmarla 或我的邮箱 SukeshMarla@Gmail.com 与我联系。暂时再见，但这并不是告别！！！！

# 😊 派对时间 😊

# 索引

A

Angular

关于 12, 13, 165

生命周期钩子 610

术语 7

与 AngularJS 对比 7

Angular 应用

安装 Angular CLI 168

添加身份验证 228

创建 165-171

部署 178

执行 171, 172

其他文件 179

根组件 174

根模块 176

Angular 应用实验 1

AddNew 203

实现 AddNew 功能 198, 199




数组，显示 191, 192

取消功能 204

变更检测 195

完整表单状态，重置 217

组件，添加到模块 187, 188

组件类，为动态可见性设置 197

组件，创建 184, 185

组件，为重置修改 205

组件属性，连接到表单控件 200, 201

组件，使用 186

控件，用空值初始化 206

创建 182

客户，添加 195

指令 190

动态内容，在模板中显示 190

错误消息，用`ngModel`实例控制 213

事件绑定 194

执行 182

表单，创建 193

`FormsModule`，导入 208

隐藏属性，使用 198

插值 189

插值，使用 199, 200

模型，创建 189

模型，填充 189

`ngModel`，实现 209

输出，检查 186, 188, 190

属性绑定 196, 197

属性绑定，在模板中实现 197

属性绑定，使用 200

红色边框，从表单中移除 215, 216

保存按钮，控制 214, 215

保存，为动态值修改 201, 202

样式，定义 210

模板文件 185

模板，为重置修改 204

双向绑定，实现 207, 208

不必要的代码，移除 208

验证，附加到控件 211

验证，实现 209, 210

验证消息，附加 213

值，分配给隐藏属性 214

Angular 应用实验 2

额外头部，移除 221

Bootstrap CSS 验证消息，附加 225

Bootstrap，包含到项目中 220

客户列表，重新设计 221, 222

数据录入屏幕，重新设计 222, 224

执行 221

Angular 应用实验 3

关于 228

API，调用 257

`AuthGuard`，创建 262

默认路由，配置 242

动态代码，在`AuthGuard`中添加 264

动态问候消息，设置 268

`FormGroup`，在模板中绑定 232

问候消息，在模板中更改 268

`HttpClientModule`，在`AppModule`中导入 256

`HttpClient`服务访问，在登录组件中获取 253

无效登录，配置 235-238

无效路由，定义 243

`IsExpired`方法，创建 267

`jwt-decode`，安装 269, 270

库，安装用于检查令牌过期 267

登录组件，添加 228

登录组件，添加到模块 229

`LoginComponent`类，准备验证 230, 231

`LoginComponent`代码，修正 260

登录组件，显示 229, 230

登录事件，处理 246, 247

`LogoutComponent`，更改 266

登出，实现 265

带问候消息的登出，实现 247

无效凭据的输出，检查 248

有效凭据的输出，检查 248

`pathMatch`，设置 242

占位符，在`AppComponent`中添加 240, 241

随机字符串，用其检查 243

`ReactiveFormsModule`，导入 231

`RouterService`的引用，获取 246

路由守卫，附加 262

路由守卫，注册 264

`RouterModule`，导入 239

`Routes`，定义 238, 239

服务器，准备 252, 253

令牌，存储 261

故障排除 259

验证消息，设置 232, 234

Angular CLI

关于 168

安装 168

Angular 指令

属性指令 514

元素指令 513

结构指令 514

Angular 元素

关于 595

Angular 组件，配置 597, 598

应用，重新构建 600

应用，测试 596

引导组件，移除 600

组件，创建 596

组件，使用 596

创建 595

HTML，测试 599-601

`ngDoBoostrap`方法，定义 601

项目，构建 598

项目，配置 597

示例 HTML 文件，用于项目 598, 599

Angular 表单 541, 543

Angular Hello World

关于 172

编码 173

编辑器，用于编码 172

Angular 注入器

空注入器 613

平台注入器 613

AngularJS6, 7

Angular 生命周期 610

Angular 模块

Angular 组件 469

Angular 组件，分组到 470

组件，使用 473

为客户创建`CreateHeaderComponent`471, 472

为产品创建`CreateHeaderComponent`472

`CustomerComponent`，使其对`AppComponent`可见 477, 478

客户模块，创建 474, 475

客户相关组件，移动到`CustomerModule`475

客户，使用 473

功能组件，创建 470, 471

头部内容，更改 473

分层导入场景 481, 483

新建 Angular 项目，创建 470

新的`HeaderComponent`，添加 472, 473

`ProductComponent`，创建 471

`ProductComponent`，使其对`AppComponent`可见 478

`ProductComponent`，使用 473



`ProductModule`，创建 476

与 `Product` 相关的组件，移至 `ProductModule` 476

服务 484, 485

Angular 管道

关于 301, 501

非纯管道 508

Angular 路由

锚点，替换为 `routerLink` 448

Angular 模块，创建 453, 454

应用程序，重命名 441

`AuthComponent`，创建 444, 445

子路由，定义 457

`CommonModule`，导入到 `CustomerModule` 460

组件，为演示创建 441, 442

`console`，检查 458

CSS，为活动菜单定义 449

默认路由，附加 450, 451

`FormsModule`，导入到 `CustomerModule` 460

`ProductModule`，创建 455

项目，构建 461

路由，配置 443, 444

路由，为懒加载重新配置 455, 456

`routerLinkActive` 指令，附加 449

路由，修改 446, 447

`SupplierModule`，创建 455

Angular 服务 279

Angular 服务，在应用程序中

关于 279

`Authenticate` 方法，定义 284

`AuthenticationService`，创建 280

认证成功，处理 290, 291

错误，解决 293

`injectable` 装饰器，附加到 `AuthenticationService` 289

注入器，为 `AuthenticationService` 配置 282

无效凭据，处理 291-293

`LoginComponent`，连接到 `AuthenticationService` 280

`LoginComponent`，修改 289, 293

`Observables`，订阅 296

响应模型，创建 284

`Subject`，转换为 `Observables` 296

用户模型，创建 284

Angular 样式

`angular.json`，为多包配置 550

应用程序，构建 547-549

应用程序，执行 548, 549

`color.css`，创建 547

`color.css`，导入 548

`color.css`，在 `angular.json` 中导入 548

组件，创建 546

组件样式 550

`ExternalCSSTestComponent`，更新 547

外部样式表 545, 546

外部样式表，包含 546

`mystyle.css`，创建 546

输出，测试 547

项目，创建 546

`style.css`，更新 547

API 调用 269

`AppComponent` 183, 463

应用程序逻辑 244

`AppModule` 183, 463

箭头函数

关于 63

优点 63, 65

简洁且可读的函数表达式 63

演示 65-68

实际场景 64, 65

assets 文件夹 373

`async` 管道 301, 302

属性型指令 191, 514

属性选择器 522

认证

认证令牌，从服务器获取 249

路由，在客户端保护 250

服务器资源，保护 251, 252

B

Bootstrap

实现 219

包含到项目中 220

Bootstrap CSS

安装 220

`BrowserModule` 459

内置管道

`CurrencyPipe` 501

`DatePipe` 501

`DecimalPipe` 502

`LowerCasePipe` 501

`PercentPipe` 502

`UpperCasePipe` 501

打包 462

C

回调函数 76

回调地狱 85

变更检测

关于 567

组件 567

执行 568

触发 568

变更检测，从组件分离

应用程序，测试 587

变更检测，从 `CustomerListComponent` 分离 587

变更，手动检测 588

项目，创建 586

变更检测，在开发模式下

应用程序，执行 570

应用程序，重新检查 574

点击我按钮 571

组件，包含在根组件中 569

DOM 变更，执行 574

初始化时间 575

新组件，创建 569

生产模式，执行 574

项目，创建 569

变更检测，在组件层级结构中

关于 581

应用程序，从 `zone.js` 断开连接 585

应用程序，执行 584

应用程序，测试 586

按钮点击 584

组件，创建 581

组件，使用 581

手动变更检测，使用 `ChangeDetectionRef` 服务实现 586

手动变更检测，使用 `tick` 方法实现 585

新项目，创建 581

输出，测试 585

样式，定义 583

子模块注入器 485

`CommonModule` 475

编译时配置

`apiURL` 键，在环境中创建 367

应用程序，检查 370

应用程序，托管 369

应用程序，在生产模式下重新构建 370

动态 API 地址，获取 368

项目，构建 368

第二个服务器，创建 366

服务器，运行 366, 367

与运行时配置对比 365

组件 CSS 样式 554, 555

组件装饰器方法 285

组件型指令 190

面向组件的样式

关于 413, 414

与 Angular 414

当前应用程序中的问题 415

组件样式

关于 550

应用程序，构建 554

组件，创建 551

组件，使用 551

定义 552, 553

`ExternalCSSTestComponent`，注释掉 550

样式，定义 552

常量变量 43

构造函数 610





- 容器组件 415, 432
- 容器-展示模式
- 关于 415
- `CustomerAddComponent`，添加到 `AppModule` 417
- `CustomerAddComponent`，创建 416
- `CustomerAddComponent` 模板，准备 418, 420
- `CustomerAddComponent` 视图类，准备 420
- `CustomerComponent`，清理 430, 431
- `CustomerComponent` 模板，准备 420
- `CustomerListComponent`，添加到 `AppModule` 417
- `CustomerListComponent`，创建 416
- `CustomerListComponent` 视图类，准备 418
- `CustomerList` 模板，准备 417
- 自定义输出属性，在 `CustomerListComponent` 中创建 424
- 默认回车，实现 437
- 错误处理器问题 434, 435
- 事件，触发 429
- 事件，从 `CustomerListComponent` 触发 424
- 焦点问题，解决 435
- 焦点逻辑，添加 436
- 焦点，设置 433
- `ngAfterViewInit`，实现 437
- `ngOnInit`，实现 436
- `OnCancel`，在 `CustomerComponent` 中初始化 426, 427
- `OnSave`，在 `CustomerComponent` 中初始化 429
- 取消按钮的输出属性，在 `CustomerAddComponent` 中声明 426
- 保存按钮的输出属性，在 `CustomerAddComponent` 中声明 428
- 输出属性，在 Customer Component 中初始化 425
- 项目，升级以遵循 416
- 引用，在 Component 类中创建以进行控制 433
- `CustomerListComponent` 中的常规属性，转换为输入属性 422
- 修订 431
- `CustomerComponent` 中的 `Save` 方法，更改 429
- 模板引用变量，附加 432, 433
- 值，提供给输入属性 422, 423
- `ContentChild`
- 关于 608
- `AppComponent`，更改 608
- 应用程序，测试 609
- 子组件，更改 608
- 在 `MyBoxedContentComponent` 中使用 609
- `ContentChildren` 610
- 内容投影
- 关于 605
- 组件，创建 606
- 组件，使用 606
- `MyBoxedContentComponent`，更新 607
- 项目，创建 606
- 被投影的组件，访问 606
- 项目，执行 606
- CSS 选择器 522
- `CurrencyPipe` 501
- 自定义 Angular 模块 255
- `CustomerListComponent`
- 数据，获取 421
- `Customers$` 变量 332-334
- `CustomerService`
- `CustomerComponent`，清理 313-315
- 功能，处理 316, 317
- 注入，在 `CustomerComponent` 中 315
- 注入器，为其配置 315
- `*ngIf` 与 else，应用 331, 332
- 可观察对象，声明 316
- 可观察对象，在模板中处理 317, 318
- `Subject` 321-323
- `Subject`，替换 325, 326
- 故障排除 318-320
- 自定义管道
- `AppComponent`，修改 502
- `AppComponent`，更新 506, 507
- 应用 505
- `AppModule` 504
- `concat` 管道，应用 508
- `concat` 管道，创建 507
- 创建 502, 503
- 管道逻辑，更改 505, 506
- 项目，创建 502
- 转换逻辑，实现 507
- 未知数据类型 504
- 自定义预加载策略 466
- D
- 虚线边框 564
- `DatePipe` 501
- 调试，在 Angular 中
- 组件，获取 327
- Customer Component，选择 326
- `IsAddNew$`，探索 327-331
- 所选组件，显示 327
- `DecimalPipe` 502
- 装饰器 159
- 默认导出 105
- 默认参数 61, 62
- 依赖 275
- 依赖注入 245, 279
- 部署文件
- `main.***.js` 611
- `***.map.js` 612
- `polyfills.***.js` 611
- `runtime.***.js` 611
- `script.***.js` 612
- `style.***.cs` 612
- `vendor.***.js` 612
- DI 框架 279
- 指令
- 关于 190
- Angular 指令 191
- 组件指令 190
- 结构型指令 191
- 指令选择器
- 关于 522
- 属性选择器 522
- CSS 选择器 522
- 元素选择器 523
- ID 选择器 523
- DI 令牌 282, 360
- 红色虚线边框 564
- 傻瓜组件 415
- E
- 急切加载 465
- 元素指令 513
- 元素注入器
- 关于 281
- 配置 287
- 元素选择器 523
- 增强的对象字面量 51, 52
- 枚举
- 关于 146
- 使用 147
- 错误处理，在 Angular 中
- 应用程序，重命名 386
- 客户端逻辑错误，准备 388
- 客户端运行时错误 403
- 组件，添加到模块 387
- 组件，创建用于测试错误 386
- 组件 CSS，创建 392, 393, 397
- 自定义错误组件，创建 391
- 自定义错误处理器，创建 399
- `ErrorComponent`，添加到模块 392
- 错误，测试 389, 390
- 注入器，配置 402
- 路由，更新 387, 397
- 服务器端逻辑错误，准备 388
- 服务器端运行时错误 403
- 未授权错误，准备 388
- 错误消息
- 通过 `ngModel` 实例控制 213
- ES6
- 关于 9
- 箭头函数 63
- 常量变量 43
- 默认参数 61, 62
- 增强的对象字面量 51, 52
- 执行环境，规划 35
- for-of 循环 56, 57




`modules` 87

`object de-structuring` 68

`object-oriented programming` 44

`private variables`，使用 `var` 关键字创建 40, 41

`promise` 73

`REST parameters` 57, 58

`spread operator` 52

`string interpolation` 50, 51

`variable declarations` 36

ES6 模块

`export` 语法 105

从模块中导出多个内容 103

与 `Node.js` 一起使用 103

导出变量 104

`Event binding` 194

F

`Fat arrow functions` 63

`Feature components` 415

`file-size.pipe.ts` 503

`for-of` 循环 56, 57

G

`generic` 143

H

`handleError` 方法

实现 400

`hierarchical module injectors`

设计 `AppComponent` 493

创建组件 486, 487

在多个层级使用相同的提供者进行配置 496

创建模块 486

创建项目 486

目的 494-496

配置根路由 488

配置第二级路由 489, 490

配置第三级路由 490, 493

`HTML 5 date element` 560

`HTTP Service`

创建 `CustomerItemResponse` 类 337

使用 `CustomerItemResponse` 类 337

将 `Customer` 映射到 `NewCustomer` 339

保存客户 339, 340

发出客户数据 333

从 REST 服务获取客户 328, 329

将 `HttpClient` 注入到 `CustomerService` 327

创建 `LoadCustomers` 方法 344

使用 `map` 操作符 336

创建请求实体 338, 339

注释保存逻辑 333

更新 `save` 方法 345

获取服务器代码 328

在 Customer Service 中创建 `Subject` 和 `Observable` 332

初始化 `Subject` 和 `Observable` 333

传递 `token` 340, 341

在请求头中传递 `token` 330

I

`Id selector` 523

`ID token` 269

`impure pipes`

关于 508

设置 `AppComponent` 509, 510

创建 509

场景 508

重新定义 `transform` 509

`InitialModule` 464

`Injectable` 应用逻辑 244, 245

`injectable` 装饰器 285

`Injection token` 示例 361, 362

`injector` 254

关于 281

配置 254, 612

元素注入器 281

模块注入器 281

`Input` 属性

使用 421

`interpolation` 189

`IOCcontainers` 279

J

`JavaScript`

关于 8, 9, 137

演示 8

`JavaScript modules` 87

`JSON Web Token (JWT)` 252

L

`lazily loaded modules`

关于 462

混合方法 462, 463

预加载策略 465

`lazy loading` 461

关于 465

使用 `NoPreloading` 466

使用 `PreloadAllModules` 466

`life cycle hooks`，Angular

`Constructor` 610

`ngAfterContentChecked` 611

`ngAfterContentInit` 610

`ngAfterViewChecked` 611

`ngAfterViewInit` 611

`ngDestroy` 611

`ngDoCheck` 610

`ngOnChanges` 610

`ngOnInit` 610

`Logout and Route Guard cleanup`

自动聚焦 310

修改 `CustomerComponent` 306

提交时回车 310

重构守卫 308, 309

重构登出 305

从 Login Component 中移除提供者 308

注册根注入器 308

`loosely coupled` 277, 278

`LowerCasePipe` 501

M

`MasterModule` 464

`modular libraries` 90

`Module Bundler` 26, 113, 114

`Module Formatters`

关于 96

演示 96-99

`Module Injector` 281

`Module loader`

关于 26, 99, 100

与 `Module Bundler` 对比 128

`modules`

关于 87

优势 87

在 JavaScript 中创建 90

演示 92, 93

依赖管理 89

隔离编码 88

模块化开发 88

使用 `Node.js` 运行时 90, 91

常规库 89

使用浏览器运行时和 ES6 模块 101-103

使用浏览器运行时但不使用 ES6 模块 94-96

`modules`，TypeScript

使用 148, 149

`mouse over directive`

更改 `AppComponent` 521

执行应用程序 516

附加 515

访问元素 517

操作元素 517

创建输入属性 518

重新定义输入属性 520

处理鼠标离开事件 521, 522

处理鼠标悬停事件 521, 522

创建新的 Angular 指令 515

创建新的 Angular 项目 514

实现 `ngOnInit` 方法 519

更改选择器 520

添加测试代码 515

为输入属性赋值 518

`multiple providers`

关于 355

添加 multi 属性 357, 358

创建 `MultiRndService2` 356

创建 `MultiRndService` 356

使用常规提供者配置根注入器 356

N

`Named export` 105

`new way`，变量声明

演示 41-43

`ngAfterContentChecked` 611

`ngAfterContentInit` 610

`ngAfterViewChecked` 611

`ngAfterViewInit` 611

`ngDestroy` 611

`ngDoCheck` 529, 610

`ngModel` 类实例 212





- `ngModule` 459
- `NgModule` 装饰器 288
- `ngOnChanges` 529, 610
- `ngOnInit` 610
- `ng-template` 指令 532
- Node 控制台应用程序
  - 演示 16, 17
- `Node.js`
  - 关于 13
  - 下载链接 13
  - 安装 13
  - 安装验证 13, 14
  - 路径更新 15
  - 在 Angular 应用开发中的作用 30
  - 系统路径更新 16
- node 模块 18
- `NoPreloading` 465
- `npm`
  - 关于 17
  - 用于下载 JavaScript 库 18
  - 用于下载工具 18
  - 注册表 18
  - 使用 17
- `npm` 脚本
  - 创建 24
  - 使用 24, 25
- 空注入器 615

## O
- 对象解构
  - 关于 68
  - 演示 68-72
- 面向对象编程
  - 关于 44
  - 演示 44-50
- `Observable`
  - 关于 294
  - 从 `Subject` 中提取 295
- `Observable` 与 `Observe` 概念 294
- `Observer` 294
- `OnlyIfUserIsAuthorizedDirective`
  - `AppComponent` 修改 537
  - 应用程序执行 524-527
  - 附加到 `ng-template` 533
  - 授权逻辑定义 524, 525
  - 将授权内容包裹在 `ng-template` 中 532
  - 添加按钮以更改授权 526
  - 注入 `ComponentFactoryResolver` 536
  - 创建 523, 524
  - 创建 `CustomMessageComponent` 535
  - 注入必要的服务 524
  - 将新服务注入指令 531
  - 修改 `ngDoCheck` 534, 535
  - 实现 `ngDoCheck` 530-533
  - 重新定义 `ngDoCheck` 536, 537
  - 实现 `ngOnChanges` 528
- `OnPush` 变更检测策略
  - 关于 588
  - 应用程序执行 589
  - 应用程序测试 591
  - 按钮点击 589
  - 创建用于保存数据的类 590
  - `CustomerAddComponent` 按钮点击 590
  - 修改 `CustomerComponent` 591
  - 重新定义 `HandleClick` 方法 591
  - 创建输入属性 590
  - 修改引用 591
  - 设置 589

## P
- `package.json`
  - 关于 19
  - 创建 19-21
  - 使用 21-23
- `PercentPipe` 502
- 平台注入器
  - 关于 614
  - 配置 614
  - 特性 614, 615
- `polyfill.ts`
  - 关于 578
  - 创建 `classlist.js` 579
  - 下载 580
  - 包含 580
- `PreloadAllModules` 465
- 展示组件 415, 432
- 私有变量
  - 使用 `var` 关键字创建 40, 41
- promise
  - 关于 73
  - 演示 73-81
  - 局限性 81, 82
  - 成功与失败 83-85
- 属性绑定 196
- `providedIn`
  - 使用 615
- 提供者 254, 282
- 纯管道
  - 转换为非纯管道 510

## R
- 常规提供者 355
- REST 参数 57, 58
- 根组件 174, 175
- 根注入器
  - 配置 286, 287
- 根模块 176-178
- 路由守卫 262
- 运行时配置
  - 使用动态 URL 进行 API 调用 375, 376
  - 修改 API 调用 382
  - 创建 `AppConfigService` 374, 375
  - 将 `AppConfigService` 注入到 `InitializeConfig` 方法 380
  - 修改 383
  - 创建配置文件 373, 374
  - 定义依赖 381
  - 在服务中获取动态 API URL 375
  - 创建 `initializeConfig` 方法 378
  - 从 `AppConfigService` 返回 promise 379
  - 配置根注入器以注入初始化函数 378, 379
- 运行时异常
  - 客户端错误 385
  - 服务端错误 385
- `RxJS` 257, 258
- `RxJS` 可观察订阅
  - 取消订阅 300
- `Rxjs` Subject
  - 关于 295
  - 与 `Rxjs` Observable 对比 295

## S
- 服务 244
- 服务模块 255
- `ShadowDOM` 559, 560
- Angular 中的 `ShadowDOM`
  - 应用程序执行 562, 563
  - 定义组件样式 562
  - 修改封装 563, 565
  - 设置封装 561, 562
- 单页应用 (SPA) 7, 10, 11
- 智能组件 415
- 展开运算符
  - 关于 52
  - 克隆数组 53-55
  - 合并 JavaScript 对象 55, 56
  - 合并两个数组 52, 53
  - 使用 53
- 创建 Angular 应用的步骤
  - 创建 bundle 168
  - 使用组件 168
  - 下载并配置 166
  - 编写启动代码 167
- 字符串插值 50, 51
- 字符串令牌示例 360, 361
- 结构型指令 191, 514
- `styleUrls` 556
- 订阅者 294

# T
- `TempalteRef` 532
- 测试模块
  - 创建 91
- 紧耦合 276, 277
- 令牌拦截器
  - 清理 `CustomerService` 352
  - 配置注入器 350, 351
  - 为 `TokenInterceptorService` 配置注入器 349
  - 将常规提供者转换为多提供者 351
  - 创建 `TokenInterceptorService` 348, 349
- 传统变量声明方法
  - 演示 36-40
- 传统 Web 应用
  - 与单页应用 (SPA) 对比 10





# T
## `TransactionModule`
- 464

## 树摇优化过程
- 关于 479
- 缺点 480

## 双向绑定
- 208

## 类型定义文件
- 151

## TypeScript
- 关于 28, 133
- 客户端对话 138-140
- 编写代码 28
- 编译环境 134
- 配置 157, 158
- 装饰器 159
- 枚举 146
- 使用现有的 JavaScript 文件 150-156
- 特性 29
- 函数 135, 136
- 泛型 143-146
- 安装 134
- 接口 140-142
- 模块 148, 149
- 在 Angular 学习中的作用 29
- 类型安全环境 134
- 独特特性 140
- 使用 28

## TypeScript 编译器
- 28

## 类型令牌
- 使用 283

# U
## 执行取消订阅
- 关于 300
- 实现异步管道 302, 304
- 实现 `ngOnDestroy` 方法 300

## `UpperCasePipe`
- 501

## `useClass`
- 使用 377

## `useExisting`
- 378

## `useFactory`
- 378

## `useValue`
- 378

# V
## 原生 JavaScript
- 11

## 变量声明
- 关于 36
- 新方式 41
- 传统方式 36

## `ViewChildren`
- 关于 603
- 创建 Angular 项目 603
- 修改 `AppComponent` 604
- 修改 `AppComponent` 代码 605
- 创建 `AppComponent` 内容 604
- 运行应用程序 604
- 测试输出 605

## `ViewContainrRef`
- 532

## 视图封装
- 关于 556
- 模拟值 556-558
- 无值 558, 559
- ShadowDOM 值 559

## Visual Studio Code
- 下载链接 173

# W
## webpack
- 关于 25, 27, 113, 114
- 基础 114, 115
- 浏览器，使用 AMD 模块作为运行时 117-120
- 浏览器，使用 ES6 模块作为运行时 120, 121
- 配置文件 121, 122
- 用于 CSS 打包 123-128
- Node.js，作为运行时使用 115-117

## webpack-dev-server
- 关于 128, 129
- 示例 129
- 使用 npm 安装 129-131

# Z
## `zone.js`，与 Angular 断开连接
- 关于 575, 576
- 修改 `AppComponent` 576
- 运行应用程序 576, 577
- 手动检测变更 578
- 测试 HTML 文件 579
- 在 IE9 或更低版本中测试 HTML 文件 580
- 在 IE9 或更低版本中重新测试 HTML 580
- 创建新项目 576
- 提供 noop zone 577
- `zone.runOutsideAngular` 方法 401

