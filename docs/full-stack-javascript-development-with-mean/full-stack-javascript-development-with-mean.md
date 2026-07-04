# 全栈 JavaScript 开发：MEAN 架构实战




# 使用 MEAN 进行全栈 JavaScript 开发

# 关于 Adam Bretz

Adam Bretz 是一名专注于客户端和服务器端 JavaScript 的软件工程师。Adam 于 2007 年在宾夕法尼亚州米勒斯维尔大学获得计算机科学学士学位。在之前的工作中，Adam 是帮助公司从 PHP 迁移到纯 JavaScript 解决方案的工程师团队的一员。Adam 目前与妻子 Jenna 住在匹兹堡地区。

# 关于 Colin J. Ihrig

Colin J. Ihrig 是一名软件工程师，主要使用 Node.js 进行工作。Colin 是《Pro Node.js for Developers》一书的作者，目前担任 SitePoint JavaScript 频道的主编。Colin 分别于 2005 年和 2008 年在匹兹堡大学获得工程学士学位和计算机工程硕士学位。

# 关于 SitePoint

SitePoint 专注于为 Web 专业人士出版有趣、实用且易于理解的内容。访问 [http://www.sitepoint.com/](http://www.sitepoint.com/) 浏览我们的博客、书籍、新闻通讯、文章和社区论坛。您将找到大量关于 JavaScript、PHP、Ruby、移动开发、设计等方面的信息。

> 献给我的父母 —— 感谢你们在我七岁时给我买了任天堂，十岁时给我买了电脑。—— Adam

> 本书献给我的妻子 Alaina、我的儿子们 CJ 和 Carter，以及我的妈妈。我非常爱你们！—— Colin

# 序言

借助现代工具，仅使用 JavaScript、HTML 和 CSS 就能创建生产级的应用程序。MongoDB、Express、AngularJS 和 Node.js 这几种 JavaScript 技术的组合已经变得非常流行，被称为 **MEAN 技术栈**。本书将详细探讨 MEAN 技术栈。

我们将从 Node.js 开始，因为它为所有服务器端工作奠定了基础。您将学习如何在本地机器上运行 Node，以及如何使用 npm（Node 的包管理器）下载模块。还将涵盖 Node.js 编程模型的关键方面。

接下来，我们将转向 MongoDB，一种 NoSQL 数据库。您将学习如何从 Node 应用程序与 Mongo 交互，以及如何从 Mongo 存储中创建、检索、更新和删除数据。

在您牢固掌握 Node 和 Mongo 之后，本书将继续介绍 Express Web 服务器。我们将通过路由和中间件等主题介绍 Express 应用程序的基础知识。基于前面的章节，我们将涵盖 Node、Mongo 和 Express 的集成。

对 MEAN 技术栈的介绍将以关于 AngularJS 的几章作结。这些章节将详细介绍 Angular 的基础知识，如数据绑定、指令、控制器、路由和服务。最后几章将介绍 MEAN 应用程序的调试和测试。

全栈 JavaScript 并不仅限于 MEAN 技术栈。还有一个完整的 JavaScript 工具生态系统需要了解，本书将介绍其中的一些。我们将介绍任务运行器 Gulp 和 Grunt，它们对于自动化枯燥、重复性的任务极其有用。我们还将研究 JSHint，一种用于提高代码质量的 linting 工具。在此过程中，我们还将使用 MEAN 技术栈从头开发一个示例人力资源应用程序。

# 本书适合谁阅读

本书适合中级 Web 设计师和开发人员。需要具备 HTML、CSS 和 JavaScript 的经验。

# 使用的约定

您会注意到，我们在整本书中使用了某些排版和布局样式来表示不同类型的信息。请注意以下项目。

## 代码示例

本书中的代码将使用等宽字体显示，如下所示：

```
<h1>A Perfect Summer's Day</h1>
<p>It was a lovely day for a walk in the park. The birds
were singing and the kids were all back at school.</p>
```

如果代码可以在本书的代码档案中找到，文件名将显示在程序列表的顶部，如下所示：

```
example.css

.footer {
  background-color: #CCC;
  border-top: 1px solid #333;
}
```

如果只显示文件的一部分，则用 *excerpt* 一词表示：

```
example.css *(excerpt)*

  border-top: 1px solid #333;
```

如果需要在现有示例中插入额外的代码，新代码将以粗体显示：

```
function animate() {
  **new_variable = "Hello";**
}
```

当需要现有代码作为上下文时，为了不重复显示，将显示 …：

```
function animate() {
  ...
  **return new_variable;**
}
```

有时某些代码行本应在一行中输入，但由于页面限制我们不得不将其换行。↵ 表示仅因格式需要而存在的换行，应忽略。

```
URL.open("http://www.sitepoint.com/responsive-web-design-real-user-
↵testing/?responsive1");
```

## 提示、注释和警告

### 提示：嘿，你好！

提示将为您提供有用的小建议。

### 注释：嗯哼，打扰一下……

注释是有用的补充信息，与当前主题相关，但并非关键内容。可以将它们视为额外的信息花絮。

### 重要：确保您始终……

……注意这些重要要点。

### 警告：小心！

警告将突出显示可能在路上绊倒您的任何陷阱。



## 补充材料

[http://www.learnable.com/books/mean1/](http://www.learnable.com/books/mean1/)

本书的官方网站，包含链接、更新、资源等更多信息。

[https://github.com/spbooks/mean1/](https://github.com/spbooks/mean1/)

本书的可下载代码存档。

[http://community.sitepoint.com/category/javascript](http://community.sitepoint.com/category/javascript)

SitePoint论坛，可寻求关于任何棘手网络问题的帮助。

[books@sitepoint.com](mailto:books@sitepoint.com)

我们的电子邮件地址，如果您需要联系我们获取支持、报告问题或出于任何其他原因。

## 想进一步深入学习？

感谢您购买本书。您想继续学习吗？您现在可以以低廉的价格在Learnable上无限制地访问课程和所有SitePoint书籍。立即注册，开始今天的学习吧！加入Learnable，您将始终领先于最新技术潮流：[http://www.learnable.com](http://www.learnable.com)。

## 引言

Web编程是一项需要多年时间才能真正理解的任务。其复杂性部分来自于涉及的活动部件数量之多。有效的程序员至少需要对许多主题有基本的了解，包括网络、协议、安全、数据库、服务器端开发和客户端开发等。多年来，这还包括使用各种编程语言的混合。

仅客户端编程就需要理解三种语言：用于标记的HTML、用于样式的CSS和用于功能的JavaScript。虽然前端开发有其自身的复杂性，但好消息是开发或多或少已经锁定在“三大”语言上。服务器端则完全是另一回事。服务器一直是Java、PHP、Perl以及几乎所有你能想到的语言的领域。大多数Web应用程序还利用数据库进行数据持久化。历史上，与数据库通信也要求开发者理解SQL。

创建一个简单的Web应用程序需要开发者理解HTML、CSS、JavaScript、SQL以及一种选定的服务器端语言。此外，不能保证服务器端只用一种语言编写。乐观地说，开发者需要理解至少五种不同的语言才能创建一个简单的应用程序，这还没考虑用于客户端-服务器通信的数据交换格式。请记住，Ajax中的x代表XML。许多Web应用程序最近已从XML转向更简单的JSON，但这仍然是开发者必须理解的另一层。

虽然HTML、CSS和SQL不严格被认为是编程语言，但它们各自都有开发者必须知道的语法和特性。完全理解这五种“语言”并在它们之间不断切换上下文是一项艰巨的任务。如果您曾尝试这样做，您很可能不止一次地混淆过语法。

这导致了开发者之间的专业化，不同的团队分别负责前端和后端开发。不幸的是，这并不总能确保项目更快或更高质量地完成。事实上，它往往导致更多的来回沟通、争论，以及程序员对项目全局了解不足。非常明确地需要一种语言在整个开发栈中使用。本章的其余部分将解释JavaScript如何以其他语言无法企及的方式成长为全栈语言。

## 全栈JavaScript的崛起

JavaScript长期以来一直是客户端脚本的事实标准。JavaScript在1995年Brendan Eich仅用十天时间开发出当时称为Mocha的语言后迅速登场。1995年9月，Netscape Navigator 2.0发布，其中包含了Mocha，此时它已被重命名为LiveScript。JavaScript最终在1995年12月确定了其当前名称。选择这个名称是因为Netscape试图借助当时流行的Sun的Java编程语言的声势。

在最初的浏览器战争中，微软的Internet Explorer和Netscape的Navigator不断试图压倒对方。作为对Navigator的JavaScript的回应，微软在1996年8月随Internet Explorer 3.0发布了其自己的实现，名为JScript。JavaScript于1996年11月提交给国际标准化组织Ecma International，并于1997年6月标准化为[ECMA-262](https://en.wikipedia.org/wiki/ECMAScript)。

早期，JavaScript赢得了性能不佳且仅被业余开发者使用的名声。然而，浏览器厂商多年来投入了大量时间、精力和金钱来改进JavaScript。结果是，现代JavaScript引擎是高度优化的软件，其性能远远超过了原始JavaScript解释器。在客户端，任何竞争语言（如Dart）都不太可能在短期内取代JavaScript，因为它是唯一被所有主要浏览器支持的语言。再加上计算能力的整体提升，结果就是一种适合几乎所有通用计算任务的语言。

## Node.js

2009年，Ryan Dahl创建了Node.js，一个主要用于创建可扩展网络应用程序的框架。Node.js建立在[Google的V8 JavaScript引擎](https://code.google.com/p/v8/)（与Chrome中使用的相同）和[Joyent的libuv](https://github.com/joyent/libuv)（一个抽象底层平台的异步I/O库）之上。Node使JavaScript成为服务器端编程的可行替代方案。此外，Node提供了一个完整的系统JavaScript API，这在浏览器提供的沙盒环境中从未真正实现过。随着Node的出现，JavaScript开发者可以访问文件系统、打开网络套接字并生成子进程。

Node的主要特性之一是能够在少量代码中打包大量功能。Node在其[项目主页](http://nodejs.org)上就炫耀了这一点。以下代码直接取自Node主页，仅用六行代码就实现了一个简单的Web服务器：

```
var http = require('http');
http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello World\n');
}).listen(1337, '127.0.0.1');
console.log('Server running at http://127.0.0.1:1337/');
```

**清单 1-1.** 用Node编写的简单Web服务器

现在不需要完全理解这段代码，但我们会快速讲解一下。第一行引入`http`模块，该模块提供创建HTTP客户端和服务器的功能。接下来，启动一个监听1337端口的服务器。当收到连接时，服务器响应消息`Hello World`。最后一行代码只是向控制台打印一条消息，以便让开发者了解正在发生什么。

## Node.js生态系统

Node并非第一个[服务器端JavaScript实现](server-side_JavaScript_implementation)的尝试，但它至今无疑已被证明是最成功的一个。衡量一项技术受欢迎程度的一种方式是看其周围生态系统的规模。Node已被沃尔玛、PayPal、领英和微软等大公司采用。它甚至催生了全新的公司，如StrongLoop、NodeSource和npm, Inc。

也许比使用Node的公司列表更令人印象深刻的是为Node开发的第三方模块集合。在Node创建后的短短几年里，已有超过77,000个第三方模块发布到Node的包管理器npm。根据追踪各种仓库中模块数量的网站[Module Counts](Module_Counts)，在撰写本文时，npm注册表正以每天约170个模块的速度增长。在增长率方面，下一个最接近的包管理器是PHP的Packagist，每天73个模块。[图1.1](Figure_1.1)来自Module Counts，展示了Node模块系统与各种语言包管理器的增长对比。npm已被标注以便您查看。

![](img/0ca996f5fd0375fc118091628c3c7a87_42_0.png)

图1.1. 各种包管理器的增长

凭借海量的可用模块，开发者通常能找到至少一个模块来解决他们遇到的几乎所有问题。（当然，这些模块处于不同的开发阶段，并非都已准备好用于生产环境。）如前所述，Node最大的用例之一是开发Web服务器。因此，正如您可能预料的那样，有许多模块实现了Web服务器。其中最受欢迎的模块是Express，它[目前为全球超过26,000个Web应用提供支持](currently_powers_more_than_26,000_web_applications_around)



## MongoDB

当 Node 入侵服务器领域时，另一场运动正在数据库世界悄然兴起。多年来，与数据存储打交道的主要方式一直是向关系型数据库发送 SQL 查询。然而，还有另一种不依赖 SQL 的数据存储类型。这类被称为 NoSQL 的数据库，甚至不使用关系型数据库中常见的表结构。NoSQL 数据库以多种格式存储数据，例如文档或键值对，而且比关系型数据库更加灵活、结构化程度更低。这种非结构化的特性往往能带来更简单的原型设计和更便捷的开发。NoSQL 数据库通常速度稍快一些，因为它们无需强制实施关系型数据库那种严格的表结构。

2007 年，一家名为 10gen（现为 MongoDB 公司）的企业开始研发一款 NoSQL 数据库，该数据库将成为其计划中的平台即服务（PaaS）产品的一个组成部分。2009 年，名为 [MongoDB](https://example.com)（由单词 humongous 化用而来）的数据库开源发布。MongoDB 是一个面向文档的数据库，以二进制 JSON（BSON）文档的形式存储信息。通过使用 JSON 的变种，Mongo 使得从 JavaScript 代码中读写对象变得异常简单。正如 Node 用 JavaScript 取代了另一种服务器端语言，MongoDB 也用基于 JavaScript 对象的查询取代了 SQL。

## AngularJS

虽然 JavaScript 一直是一种客户端编程语言，但它在浏览器中的使用方式随着时间推移发生了巨大变化。早在网景导航者（Netscape Navigator）时代，JavaScript 仅用于非常简单的页面交互。用例包括诸如鼠标悬停时更改图片的 `src` 属性，或驱动可折叠菜单等任务。这些效果很简单，但提供了仅凭 HTML 无法实现的交互层次。

随着技术的持续演进，JavaScript 也随之发展。网络应用的重大突破来自于高速互联网的普及和广泛应用。这为进行后台请求而非完整页面加载的 Ajax 应用程序打开了大门。在 Ajax 应用程序中，网络性能是关键，因为缓慢的连接会让页面显得无响应。应用程序逐渐转向越来越少的页面加载，以及更多的 Ajax 请求。最终，单页应用（SPA）应运而生。严格来说，SPA 只进行一次页面加载，所有其他数据都通过 Ajax 调用获取。

[AngularJS](https://example.com) 是最流行的 SPA 开发框架之一。Angular 由 Miško Hevery 和 Adam Abrons 于 2009 年（JavaScript 繁忙的一年）创建。Angular  owes much of its popularity to being backed by Google, Hevery’s employer. 它对网络应用采用模型-视图-控制器（MVC）方法，并拥有几个值得注意的特性。首先，Angular 提供了视图和模型之间的双向数据绑定。这节省了开发时间，因为 Angular 会自动保持所有内容的同步。Angular 的另一个有趣特性是许多任务（包括模板）都可以用增强型 HTML 完成。

本书后面会更详细地介绍 Angular，但现在值得看一个部分示例来说明它究竟有多强大。下面是一个名为 PeopleCtrl 的 Angular 控制器，它在数据模型中设置了 people 属性：

```
app.controller('PeopleCtrl', ['$scope', function($scope) {
  $scope.people = [
    {
      firstName: 'Colin',
      lastName: 'Ihrig'
    },
    {
      firstName: 'Adam',
      lastName: 'Bretz'
    }
  ];
}]);
```

**清单 1-2.** 操作模型的简单 Angular 控制器

模型的 people 属性是一个包含两个简单对象（代表人）的数组。下面是一个可用于显示模型数据的 Angular 视图模板：

```
<div ng-repeat="person in people">
  {{person.lastName}}, {{person.firstName}}
</div>
```

**清单 1-3.** 简单的 Angular 视图模板

`<div>` 只是一个标准的 HTML `<div>` 元素，而 `ng-repeat` 被称为 Angular 指令。这个特定的指令用于遍历数组元素，双花括号则用于从 JavaScript 访问数据。目前，无需完全理解这里发生的事情，只需意识到 Angular 为你开箱即用地处理了很多任务。

# 小结

本章介绍了全栈 JavaScript 的概念，以及它最受欢迎的一些组成部分。使用这里描述的技术，仅使用 HTML、CSS 和 JavaScript 就能创建出生产级别的应用程序。MongoDB、Express、AngularJS 和 Node.js 的组合已经变得如此流行，以至于它赢得了一个专属名称：**MEAN 栈**，其标志可见于[图 1.2](#)。这个命名借鉴了 LAMP 栈，后者由 Linux、Apache（Web 服务器）、MySQL 和 PHP 组成。

![](img/0ca996f5fd0375fc118091628c3c7a87_45_0.png)

本书后续将详细探讨 MEAN 栈。我们将从 Node.js 开始，因为它将为所有服务器端工作奠定基础。我们将学习如何让 Node 在本地机器上运行，以及如何使用 npm 下载模块。Node.js 编程模型的关键方面也将被涵盖。

接下来，我们将转向 MongoDB。我们将学习如何从 Node 应用程序与 Mongo 交互，以及如何从 Mongo 存储中创建、检索、更新和删除数据。在介绍 Mongo 的过程中，我们还将学习如何从 Node.js 访问 [MySQL](#) 数据库。虽然这在技术上不完全符合 MEAN 方法，但关系型数据库太过流行，不能视而不见。

在扎实掌握 Node 和 Mongo 之后，我们将继续学习 Express Web 服务器。我们将通过路由和中间件等主题介绍 Express 应用程序的基础知识。基于前面的章节，我们将介绍 Node、Mongo 和 Express 的集成。我们还将介绍 [hapi.js](#)，一个 Express 的替代方案。hapi 是一个新兴框架，由沃尔玛开发并在实战中检验。

我们对 MEAN 栈的介绍将以关于 AngularJS 的几个章节收尾。这些章节将涵盖 Angular 的基础知识，如数据绑定、指令、控制器、路由和服务。

全栈 JavaScript 并不仅限于 MEAN 栈。还有一整个 JavaScript 工具生态系统值得了解，本书将介绍其中一些。我们将涵盖任务运行器 [Gulp](#) 和 [Grunt](#)，它们对于自动化繁琐、重复性的任务极其有用。我们还将介绍 [JSHint](#)，一个用于提升代码质量的静态检查工具。**静态检查（Linting）**工具会分析源代码并报告潜在问题，这一特性在非编译语言（如 JavaScript）中尤其有用。

我们将以讨论 [Node Inspector](#) 和 [Mocha](#) 来结束对 JavaScript 工具生态系统的探索。Node.js 自带的内置调试器远非用户友好。Node Inspector 通过允许 Google Chrome 的开发者工具作为 Node 内置调试器的前端来弥补这一不足。另一方面，Mocha 是一个基于 Node.js 的测试框架。我们将向你展示如何创建和运行单个测试和测试套件。

如果这听起来内容很多，你是对的。而且如果你认为加上具体例子会更容易理解，你又对了。在本书的各个章节中，我们将提供许多独立的代码示例供你试用。不过，我们还将沿途开发一个综合示例应用程序。这个示例应用是一个人力资源（HR）应用程序，可用于跟踪中小型公司的员工和团队。该应用将在本书某些章节中逐步开发。

值得指出的是，目前存在多个 [MEAN 栈样板项目](link)，但本书不使用其中任何一个。我们认为独立理解所有技术比期望所有应用程序遵循单一格式更好。一旦你理解了技术基础，掌握其中一个样板项目应该易如反掌。



# 第2章

## Node.js 简介

迄今为止，JavaScript 已经有了[超过十种不同的服务端实现](over ten different server-side implementations of JavaScript)。虽然 Node.js 是最成功的，但它远非第一个。工程师们投入了大量的时间和精力试图让 JavaScript 在 Web 服务器上运行——但为什么？JavaScript 究竟有什么特质使其如此适合作为服务端语言？归根结底，这源于两个因素：熟悉度和非阻塞异步 I/O。

## 熟悉 JavaScript

从 GitHub 的使用情况来看，JavaScript 是主流语言。如图 2.1 所示，JavaScript 代码的绝对数量持续增长，超过了当今所有其他流行的脚本语言。该图表列出了以 JavaScript 作为主要语言新建的 GitHub 仓库数量。

![](img/0ca996f5fd0375fc118091628c3c7a87_48_0.png)

JavaScript 由 Brendan Eich 于 1995 年在网景通信公司（Netscape Communications Corporation）任职期间创建。到 1996 年，正式的 ECMA 规范已被提交，微软和网景都在其旗舰浏览器中实现了 JavaScript。在随后的大约二十年里，ECMAScript 规范不断推出新版本，出现了 jQuery 等 JavaScript 库、客户端 JavaScript MVC 框架、通过 Tessel 用 JavaScript 控制机器人，以及服务端 JavaScript 的兴起。如果你在过去二十年里曾制作过网页，你就一定接触过 JavaScript。

JavaScript 的广泛普及是它作为服务端语言如此具有吸引力的原因之一。如果 Web 服务器用 JavaScript 编写，那么了解 JavaScript 的开发者都可以成为积极的贡献者，无论他们的专长是什么。JavaScript 这门语言在客户端和服务端（使用 Node）是一致的。人们不再需要专注于开发的某一方面，现在有机会成为 JavaScript 开发者并参与 Web 应用程序的任何环节。仅用一种语言就可以完成整个网站的开发，而不需要开发者去学习多种——有时差异巨大的——编程语言。

在尝试学习 Node 的人中，你经常会听到一句话："它就是 JavaScript。" 过去二十多年积累的现有 JavaScript 知识库依然有用，并且在 Node.js 编程中继续发挥作用。通过在不同的环境中利用一门已经流行的 language，Node.js 立即让任何熟悉 JavaScript 的开发者只需坚持使用 JavaScript 就能成为入门级全栈开发者。

## I/O 的问题

任何不简单的 Web 服务器最终都必须执行一些 I/O。I/O 的性质多种多样，可能是从磁盘读取、查询数据库，或与其他 Web 服务器通信。即使在现代计算机上，I/O *仍然*是任何系统中最慢的部分。[图 2.2](#) 对 I/O 的成本做了很好的总结。

![](img/0ca996f5fd0375fc118091628c3c7a87_50_0.png)

[图 2.2](#) 表明，磁盘和网络 I/O 比 RAM 和 CPU 缓存慢了几个数量级。对于每分钟需要响应数十万个请求的服务器来说，这种成本很快就会演变成严重的性能问题。让我们来看一个虚拟的 Web 服务器，它执行一项非常常见的 Web 服务器任务：与数据库通信。

## 一个 Web 服务器示例

假设我们有一个用原生 PHP 编写的简单 Web 服务器，并且我们对线程或异步编程一无所知。这个服务器所做的只是从查询字符串中获取输入（当然，在经过 SQL 注入攻击的清理之后），然后在数据库上运行查询。当数据库响应时，服务器将处理响应并将数据视图返回给客户端，如[图 2.3](#) 所示。

![](img/0ca996f5fd0375fc118091628c3c7a87_51_0.png)

图 2.3. 示例请求生命周期

以下是生命周期的步骤：

- 1. 一个请求到达 Web 服务器。客户端请求我们数据库中所有"红色"的汽车。
- 2. 第二台远程服务器存放着我们的企业数据库。我们的 Web 服务器创建一个数据库查询，并将其发送到存放数据库的远程服务器。
- 3. 数据库引擎运行查询并组装结果。
- 4. 数据库服务器将结果响应给我们的 Web 服务器。
- 5. Web 服务器接收查询结果，并将其转换为 JSON，以便于处理。
- 6. 服务器从本地文件系统读取，找到合适的 HTML 文档来显示结果。
- 7. 服务器响应请求，返回包含我们数据库中所有红色汽车的 HTML。

这是许多 Web 服务器的典型请求生命周期。审视上述生命周期和图 2.3，可以明显看到 I/O 延迟出现在多个步骤中。步骤二、三、四都引入了 I/O：分别是网络、磁盘和磁盘。如果我们使用图 2.2 中提供的*非常*粗略的数字，我们大约有 322,000,000 个周期浪费在等待阻塞 I/O 操作上。在运行程序中阻止其他处理进行的 I/O 活动被称为**阻塞 I/O**。

如果 Web 服务器每次只需为一个人服务，那么这 322,000,000 个被阻塞的周期不会有什么问题。然而在现实中，任何面向公众的 Web 服务器都需要能够同时处理数千个并发请求，并且具有极高的正常运行时间和极低的延迟。

假设用户 A 发出一个请求，用户 B 在一毫秒后发出一个请求。在我们的示例服务器中，不对架构或代码做任何更改的情况下，用户 B 每次都会在用户 A 的请求执行任何 I/O 活动时体验到延迟，*再加上*其自身请求的 I/O 活动。即使只有几个用户，你也可以开始看到这将如何产生级联问题。

## 绕过 I/O 问题

I/O 并不是一个新问题。只要存在 Web 服务器，工程师们就必须解决可扩展性问题。许多使用更传统编程语言（如 Java 或 PHP）构建的现有 Web 服务器，通过线程或并行进程来解决可扩展性问题。虽然这些方法有助于缓解并发用户的延迟和 I/O 问题，但它们通常很复杂，并且随着 Web 服务器负载的增加需要更多的硬件。此外，线程和并行进程并非免费。大多数公司的资源是有限的，因此增加硬件在某个节点上会变得成本高昂。

JavaScript（和 Node）按惯例是一门**非阻塞**语言。它不是在语言创建之后才去解决 I/O 问题，而是在语言核心中内置了一个简单的解决方案：回调。**回调**是在 I/O 操作完成或产生错误时执行的函数。操作启动时提供一个回调函数，而不是等待从而为其他用户制造延迟。当 I/O 完成时，所提供的回调函数就会执行。等待 I/O 完成仍然会有延迟，但在此期间其他逻辑可以自由执行。

回想 JavaScript 最初的使用和设计方式，这种模式是有道理的。在 JavaScript 中，函数是一等公民，因此可以像整数一样轻松地传递和声明。结合 JavaScript 在客户端的用途，如事件处理和 Ajax 请求，JavaScript 被构建成非阻塞的，并且多年来一直以这种方式使用。

在 Ajax 请求中，会发起一个请求（网络 I/O，因为要等待服务器），你为其提供一个回调。此时，浏览器窗口不会被阻塞，用户仍然可以自由点击页面上的任何可用元素。当请求完成时，提供给 Ajax 请求的回调就会被执行。常见的 Node.js 惯例建议开发者遵循相同的模式。虽然 Node 的许多核心 I/O 函数提供了同步版本，但社区和 Node 文档都强烈建议选择异步版本。

## 重新审视 Web 服务器示例

让我们来看看使用 Node.js 时我们的简单 Web 服务器示例将如何工作。在功能上，它是一样的。如前所述，得益于 npm 注册中心和 GitHub，Node.js 生态系统*极其*活跃，因此我们的 PHP 服务器使用的任何插件或模块几乎肯定都有对应的 Node 版本。

现在让我们分析一下新的 Node.js 驱动的 Web 服务器对用户 A 和 B 的行为。当用户 A 的请求到达步骤二时，将对数据库服务器进行一次异步调用。一个回调函数将被传递过去，当数据库服务器的响应返回时它将被执行。用户 B 的请求紧随其后，不需要*等待* A 完成，B 可以立即开始处理并排队发送另一个请求到数据库服务器。不需要线程或额外的资源。

同时处理这两个请求。这将使得 A 和 B 的延迟大致等于它们各自请求中所有 I/O 操作的总时间，完全与其他用户可能向 Web 服务器发出的请求数量无关。

## 重要提示：这不会神奇地加速对数据库服务器的请求

请记住，这不会加速对数据库服务器的请求。它只是防止 I/O 活动在新的请求到来时阻塞额外的服务请求。这使得我们的 Web 服务器无需额外的硬件或配置即可处理更多的并发请求。

## 真实世界数据

我们已经描述了运行 JavaScript 的服务器可以带来的优势，但让我们来看一些数据。Node.js 领域的主要参与者之一是 PayPal。他们使用 Node.js 和围绕 Express.js 框架的封装重写了他们的账户概览页面。PayPal 从 Java Web 服务器迁移到了 JavaScript Web 服务器，并发布了 [图 2.4](Figure 2.4) 所示的性能基准。

### Java 应用程序

![](img/0ca996f5fd0375fc118091628c3c7a87_54_0.png)

| 指标 | 1 个用户 | 5 个用户 | 10 个用户 | 15 个用户 |
| :--- | :--- | :--- | :--- | :--- |
| 每秒页面数 | 1.8 | 7.6 | 11.5 | 11.3 |
| /home | 233 | 280 | 533 | 1039 |
| /wallet | 1321 | 1296 | 1445 | 1817 |
| /activity | 374 | 416 | 651 | 1135 |

### Node.js 应用程序

![](img/0ca996f5fd0375fc118091628c3c7a87_54_1.png)

| 指标 | 1 个用户 | 5 个用户 | 10 个用户 | 15 个用户 | 20 个用户 | 25 个用户 |
| :--- | :--- | :--- | :--- | :--- | :--- |



# 总结

本章介绍了 Node.js——JavaScript 最成功的服务端实现。我们探讨了 Node 作为服务端技术取得成功的原因：它使用了许多开发者熟悉的 JavaScript 语言，并提供了非阻塞异步 I/O。最后，我们通过编写第一个简单的 Node 服务器结束了本章。

在下一章中，我们将讨论 Node 的模块和 Node 包管理器（npm）的工作原理。

[1] 来源：http://blog.mixu.net/2011/02/01/understanding-the-node-js-event-loop/

[2] 来源：https://www.paypal-engineering.com/2013/11/22/node-js-at-paypal/

## 模块和 npm

正如我们在 [1](https://example.com/1) 和 [2](https://example.com/2) 章所讨论的，Node 成功的关键之一在于开发者可以使用的丰富模块。对于开发者在构建 Web 服务器时遇到的大部分问题，GitHub 上都有对应的开源模块。此外，还有用于[社交认证](https://example.com/social_authentication)、[数据验证](https://example/validation)甚至服务器框架（如 [ExpressJS](https://example.com/ExpressJS) 和 [Hapi](https://example.com/Hapi)）的模块。不过，并非所有模块都庞大而复杂；也有一些简单的模块，用于[控制台文本着色](https://example.com/coloring_console_text)、[格式化日期和时间](https://example.com/formatting_dates_and_times)以及[克隆](https://example.com/cloning) JavaScript 对象。

作为开发者，我们尽可能避免重复造轮子。我们不断宣扬“代码重用”的理念，而 Node 在这方面也没有让我们失望。要充分理解 Node 生态系统，理解模块和 Node 包管理器（npm）的工作机制至关重要。

## npm

**npm** 是 Node 的包管理器。它是一个在 Node 初始安装时全局安装的 Node 模块。默认情况下，它从 [npm 注册表](http://registry.npmjs.org/)搜索和加载包。除了作为包注册表，它还是一个用户友好的资源，帮助开发者发现新模块。npm 是 Node 模块生态系统的核心，因此现在让我们来讨论一些你需要了解的、以便有效使用它的命令。

## npm install

`npm install` 与许多 npm 命令一样，可以根据提供的参数执行多种不同的任务。简单地执行 `npm install` 将安装当前目录 `package.json` 文件中列出的所有模块。我们稍后会详细讨论 `package.json` 文件，但现在，可以将其视为一个模块名称列表。`npm install` 会读取 `package.json` 文件，并将所有列出的模块安装到本地的 `node_modules` 文件夹中。

通常，当你启动一个从源代码管理提供者拉取的新项目时，这是让代码正常运行的第一步。这将为你提供正确的环境和依赖项，使你能够快速启动并运行。

`npm install <name>` 会尝试将模块 `<name>` 的最新版本安装到本地 `node_modules` 文件夹中。当你发现一个想尝试的模块时，只需使用 `npm install <name>` 进行安装，npm 会处理其余工作。作为简单的练习，打开终端并输入以下命令：

```
npm install colors
```

如果你正在观察终端，你应该会看到几个 GET 请求和 200 状态码。这些请求和响应是 npm 调用 npm 注册表，查找名为 `colors` 的模块，并将其下载到本地的 `node_modules` 文件夹中。

## 全局安装与本地安装

不带任何修改参数的 `npm install` 始终会将 Node 模块本地安装到当前目录的 `node_modules` 文件夹中。这通常是期望的行为；但是，某些模块可以直接从命令行运行。将这些全局模块想象为使用 Node 和 JavaScript 编写的新命令。这类模块是你可能希望在特定项目之外使用并全局访问的。我们已经遇到过一个全局模块了：`npm`。另一个例子是 `express-generator` 模块。`express-generator` 向终端添加了一个命令，允许用户使用单个命令和一些参数创建一个通用的 ExpressJS 应用程序服务器（文件结构和样板代码）。

由于我们稍后将使用此模块，现在让我们全局安装它。在终端中输入以下内容：

```
npm install express-generator --global
```

除非你更改了文件系统的权限，否则在安装过程中你会遇到 `EACCES` 错误。这是正常的。`EACCES` 错误意味着 npm 缺乏写入全局模块安装位置的权限。快速的谷歌搜索会为你提供几种解决此问题的方法，但我们将介绍一种没有额外安全问题且不需要以更高权限用户运行 npm 的方法。

## 全局安装设置

在终端中，导航到你的主目录并运行 `npm config set prefix ~/npm`。这将为 npm 全局配置 `prefix` 选项。你可以通过运行 `npm prefix` 来验证这是否正确，结果应该指向当前用户目录下以 `/npm/bin` 结尾的目录。此命令告诉 npm 在全局操作期间从该目录读取和写入，而不是从默认位置读取和写入（当前用户可能缺乏写入权限）。

你最后的任务是确保 `~/npm` 包含在你的 `$PATH` 变量中。如果跳过此步骤，你将无法轻松地从命令行运行任何全局模块，而是必须提供 `~/npm` 文件夹中模块的完整路径。

### 注意：设置 $PATH

`$PATH` 是在类 Unix 操作系统中找到的环境变量。它是一个包含可执行程序所在目录的列表。应用程序在运行时依赖此值来查找外部应用程序。例如，如果你使用 IDE（集成开发环境），它将使用 `$PATH` 值来查找外部编译器、调试器或已安装的源代码管理应用程序等项目。在 Windows 操作系统中，它被称为 `%PATH%`。

尝试重新安装 `express-generator` 模块现在应该可以正常工作，不会出现 `EACCES` 错误。这是一次性设置，以后全局模块安装将是无缝的。为确保 `express-generator` 已正确安装，请创建一个临时目录并将命令行导航到该目录。运行 `express`，你应该会看到通知，显示正在创建几个文件和目录。如果你列出文件夹内容，你应该会看到 `app.js`、`package.json` 和几个子文件夹。

## npm search

`npm search` 是查询 npm 注册表的一种快捷方式，无需离开终端。假设你想显示一个用 Markdown 编写的文件。记住，你正在进入 Node 模块生态系统——对于处理 Markdown，已经有超过 20 个现有模块。在大多数情况下，编写自己的模块是没有意义的。现有模块已经有测试，并且随着时间的推移已经过社区审查。因此，与其自己动手，不如让我们尝试在 npm 注册表上找到一个。

在终端中，输入 `npm search markdown`。第一次运行搜索命令时，可能需要一些时间；这是正常的。当结果返回时，你会看到一个长长的列表，包含所有标题、描述或标签中包含“markdown”的可用 Node 模块。

此时，你可以使用 `npm install <name>` 选择并安装一个。如果你想了解更多关于该包的信息并阅读文档，可以尝试 `npm docs <name>`。如果该包配置正确，它应该会启动一个 Web 浏览器并带你到该模块的主页。

如果你更喜欢使用命令行以外的搜索方式，可以直接访问 [npm 主页并使用那里提供的搜索功能](http://npmjs.org)。搜索结果显示模块的受欢迎程度、星标数量、依赖项列表和其他有用的数据点。

npm，无论是命令还是网站，都是 Node 生态系统的重要组成部分。我们只介绍了一些重要的命令，以便你快速上手并开始工作。我们鼓励你查看 [npm 文档以了解更多命令](https://docs.npmjs.com/cli)。在本章后面，我们将深入讨论另一个 npm 命令：`npm link`。



# package.json

我们现在知道，运行 `npm install` 时会查找 package.json 文件并安装其中列出的包。让我们来看一个简单的 package.json 文件：

```
{
  "name": "hr",
  "version": "1.0.0",
  "scripts": {
    "start": "echo \"Run the correct js file to start your application\" && exit 0",
    "populate": "node ./bin/populate_db"
  },
  "dependencies": {
    "async": "0.9.0",
    "debug": "0.7.4",
    "express": "4.2.0",
    "mongoose": "3.8.11"
  }
}
```

**清单 3-1.** 一个示例 package.json 文件。

我们来讨论一下这个文件的各个顶层键：

- **name**：模块的名称。通常，这是传递给 `npm install <name>` 的 `<name>` 参数。这是必需的，但只有在计划将模块发布到 npm 注册表时才需要保证唯一性。名称中不应包含 "node" 或 "js"。还应避免使用任何非 URL 安全字符，因为名称在 npm 注册表上会用于创建 URL。
- **version**：包的版本，以 **major.minor.patch**（主版本.次版本.补丁版本）的形式表示。这被称为语义化版本控制，建议从 1.0.0 版本开始。
- **scripts**：这个键具有独特的用途，当从此目录运行时提供额外的 npm 命令。例如，如果你在这个 `package.json` 文件的文件夹内输入 `npm run start`，你会在终端中看到 "Run the correct js file to start your application" 的输出。如果你运行 `npm run populate`，npm 将尝试执行 `node ./bin/populate_db`。该文件目前还不存在，因此命令会失败。键可以是任何有效的 JSON 键，值可以是 node 命令或 shell 脚本。
- **dependencies**：这通常是任何 package.json 文件中存储大部分信息的地方。dependencies 列出了当前模块或应用程序运行所需的所有模块。键是模块名称，值是所需的模块版本。在 `package.json` 文件中有多种方式可以表达版本。你可以指定特定版本或版本范围，通过组合使用 `>=`、`~` 和 `^`（例如，`>= 0.9.x`、`~3.x` 和 `^0.5.x`）。也可以将版本直接指向 GitHub：例如 "git://github.com/flatiron/winston#master"。npm 版本控制的细节可能变得非常复杂，尤其是在处理 ^、~ 和版本低于 1.0.0 的模块时。关于 npm 使用的语义化版本控制的完整说明，请阅读 [GitHub 上的文档](https://github.com)。

不建议在文本编辑器中逐行编写 package.json。npm 有一个内置命令可以引导你创建有效的文件。在终端中运行 `npm init`，它会引导你完成一系列提示。这将生成一个符合社区标准和 npm 最新规范的简单 package.json 文件。

`npm init` 对每个字段的含义解释得相当清楚。唯一的例外是 `main` 值。`main` 应该是当用户 require 你的模块时要使用的 JavaScript 文件名或路径。一般而言，默认的 index.js 值就可以了。

现在我们已经在当前目录中有了一个 package.json 文件，让我们再次尝试 `npm install`，这次加上一些新的参数：

```
npm install colors --save
```

这条命令会将 `colors` 安装到 `node_modules` 目录中，同时更新 package.json 中的 dependencies，以包含 `colors` 模块的条目。现在下一个开发者只需输入 `npm install` 就可以开始编码了，避免了在代码中查找模块所浪费的时间。

# node_modules 文件夹

正如我们所演示的，node_modules 文件夹是 npm 安装本地模块的地方。这也是当你 require 一个模块时 Node 首先查找的位置。让我们安装 ExpressJS 框架并检查它的 node_modules 文件夹。

在一个新文件夹中，通过 `npm install express` 安装 Express。如果你用文件浏览器或终端打开这个位置，应该会看到一个 node_modules 文件夹。如果你继续深入这个目录，很快就会发现许多子模块都有自己的 node_modules 文件夹。这就是 Node 处理依赖其他模块的模块的方式。

# 模块依赖

仔细观察文件结构，express 内部的几个子文件夹都有自己的 node_modules 文件夹。让我们看看 send 目录内部。它的结构如下：

```
send/
├── lib/
├── node_modules/
│   ├── finished/
│   │   └── node_modules/
│   │       └── ee-first/
│   └── mime/
│       └── types/
```

**清单 3-2.** Node 模块目录结构

Express 使用 send 模块，而 send 模块又使用 finished 和 mime 模块。finished 还使用了 ee-first 模块。通过查看树形结构，可以直观地可视化一个模块的依赖和子依赖。

因为每个模块都有自己的 node_modules 文件夹，你可能会看到重复。例如，如果 Express 使用的另一个模块也需要 ee-first，ee-first 文件夹就会出现在另一个不同的位置。

通过强制每个模块拥有自己的 node_modules 文件夹，而不是将所有模块放在同一个目录中，这使得开发者可以非常精确地指定他们想使用的特定模块版本。例如，如果模块 A 使用版本 1 的 "cookie" 模块，而模块 B 使用 2.x 版本，那么如果每个模块都保存到同一个文件夹中，就无法保证模块 A 能继续正常工作。npm 如何决定在全球模块目录中安装哪个版本呢？

# require()

require 函数是 Node 特有的，在 Web 浏览器中不可用。从核心来看，require 所做的只是根据提供的参数执行 JavaScript。当你 require 一个模块时，你执行的是构成指定模块的 JavaScript 代码。然后 Node 返回一个附带有函数和值的对象，就像任何其他 JavaScript 对象一样。

回顾之前的代码示例，你可能已经注意到几个地方出现了 require('http')。让我们重新看一下清单 1-1 中的简单服务器：

```
var http = require('http');
http.createServer(function (req, res) {…}).listen(1337,
'127.0.0.1');
console.log('Server running at http://127.0.0.1:1337/');
```

**清单 3-3.** 移除了内部逻辑的简单 Node 服务器

清单 3-3 中的代码应该看起来很熟悉；这是我们在本书前两章中已经多次讨论过的 Node 服务器示例。这是一个非常基础的 Web 服务器，它在主机 127.0.0.1 的 1337 端口监听请求。我们移除了代码的大部分内部逻辑，以便只关注 require 逻辑。在第一行，我们将 http 变量设置为 require('http') 的结果。require('http') 将导致 Node 尝试在一系列预定义位置中查找名为 http 的模块。如果在当前位置找不到命名的模块，Node 将尝试下一个位置。查找过程大致按以下方式工作：

1. 检查命名的模块是否为内置核心模块。
2. 检查当前目录的 node_modules 文件夹。
3. 向上移动一级目录，如果存在 node_modules 文件夹则在其中查找。
4. 重复此过程直到到达根目录。
5. 检查全局目录。
6. 抛出错误，因为找不到该模块。

这个列表总结了 Node 模块查找算法的主要要点。[官方文档](https://nodejs.org/api/modules.html)中有更多细节，但这些步骤应该足以应对最常见的使用场景。

在抛出错误之前，Node 会进行多次尝试来查找所需的模块。对于 http 模块来说，由于它是核心模块，只需要执行到第 1 步即可。模块已解析，http 的代码将执行，并返回一个附带有函数和值的 JavaScript 对象。createServer() 和 STATUS_CODES 就是附加到结果 http 对象上的数据示例。如果你想查看完整的 http 模块，请查看 [Node 源代码](https://github.com/nodejs/node)。



观察 `require` 在传入模块名时的工作方式，应能巩固关于 `package.json` 文件及其 `name` 键重要性的讨论。`name` 键不仅是通过 npm 安装模块所使用的名称，也是你在代码中引入模块时使用的名称。

让我们看另一个例子。将其写入一个脚本文件：

require_test.js

```javascript
var colors = require('colors');
console.log('Hello world'.green);
```

**代码清单 3-4.** 引入非核心模块

我们希望控制台日志更加醒目，所以给它们加上颜色！`colors` 是*一个非核心模块*，因此 Node 会开始递归查找，尝试找到一个在其 `package.json` 文件中指定了名称 `colors` 的模块。

请执行 `node require_test`。如果你之前已经安装了本章前面的 `colors` 模块，你应该会看到控制台输出绿色的 "Hello world"。否则，你会看到类似 `Error: Cannot find module 'colors'` 的错误。请安装 `colors` 模块并重新运行 `require_test.js`。

## require 的其他用途

`colors` 模块是一个易于安装和使用的 Node 模块的好例子。它也展示了 `require()` 的另一个方面。回顾代码清单 3-4，你会注意到代码是 `"Hello world".green`。这段代码是在一个字符串对象上调用 `green` 方法。未经修改的 `String` 对象没有 `green` 方法，所以 `colors` 模块向 `String` 原型添加了各种颜色方法。

请记住，`require` 的核心只是执行一些 JavaScript 代码。在 `colors` 模块的例子中，它返回一个对象，但*同时*也将一些项目附加到了 `String` 原型链上。`require` 也可用于执行"只运行一次"的代码，例如数据库初始化、构建日志单例、修改内置类型和对象，以及任何其他只运行一次的代码。

`require` 还可以接受一个文件路径。这对于你不想发布到 npm 注册表的模块很有用。很快，我们将编写一个简单的模块，可以在多个文件中重用。你可以使用以下命令加载该模块：`var ourModule = require('./path-to/our-module')`。

将 `require` 指向任意文件的能力使开发者能够将应用程序分解为更小的部分，并将逻辑封装在单个模块中。在任何 Web 服务器中，都会有一些样板初始化逻辑。与其被迫将这些逻辑放在主应用代码中，不如将其放在一个单独的文件中，并在主应用启动时用 `require` 执行一次。如果你创建的几个应用程序共享一些样板代码，这个小的 JavaScript 文件甚至可以在多个项目之间共享。

## 编写模块

本章的最后一节将介绍如何编写我们自己的模块，以便在 Node 脚本示例中使用。我们将创建一个非常简单的模块，暴露几个数学函数。我们将其命名为 "mmm"，代表 MEAN 数学模块。

在我们开始编写模块之前，快速说明一个 Node 的约定。在编写或查看 Node 代码时，你经常会看到 `exports`、`require` 和 `module`，它们似乎没有定义。Node 执行的所有 JavaScript 文件都会自动包装在一个函数中，并传入几个参数：

```javascript
(function (exports, require, module, __filename, __dirname) {
  // 我们编写的代码将放在这里
});
```

代码清单 3-6. Node 的自动包装函数

Node 以这种方式包装开发者代码有几个优点。首先，它有助于防止意外的全局变量。这个包装代码创建了一个额外的作用域层级，防止错误声明的变量被全局访问。第二个优点是每个 Node 文件都自动遵循这个预定义的模式。

现在应该清楚为什么我们可以在自己的代码中访问 `exports` 和 `require` 了。它们会自动传递给每个执行的文件。不要编写那个包装函数；让 Node 为你添加它，以防它在后续版本中发生变化。如果你想了解其工作原理，请查看[此功能的 Node 源代码](https://nodejs.org/api/modules.html#modules_the_module_wrapper)。

## 模块功能

在我们深入研究 Node 和模块方面之前，让我们先编写一些 JavaScript 代码，对整数执行基本的数学函数——加法、乘法和阶乘：

mmm.js

```javascript
function add (number1, number2) {
  return parseInt(number1, 10) + parseInt(number2, 10);
}

function multiply (number1, number2) {
  return parseInt(number1, 10) * parseInt(number2, 10);
}

function factorial (number) {
  if (number === 0) {
    return 1;
  }
  else {
    return number * factorial(number - 1);
  }
}
```

代码清单 3-7. 数学模块内部实现

这是我们希望从模块中暴露的主要功能；此时它只是普通的 JavaScript。我们还没有编写任何代码来接入 Node 的模块系统，但回顾代码清单 3-6 会给我们一个提示，告诉我们如何做。

在作用域中有一个 `exports` 对象，用于从模块导出函数。更新 mmm.js，使用 `exports` 对象，类似于代码清单 3-8：

```javascript
exports.add = add;
exports.multiply = multiply;
exports.factorial = factorial;
exports.now = Date.now();

function add (number1, number2) {…}

function multiply (number1, number2) {…}

function factorial (number) {…}

function privateMethod () {…}
```

mmm.js *（更新后，摘录）*

**代码清单 3-8.** 数学模块导出

为了清晰起见，我们删除了函数实现的内部细节。Node 模块框架在模块初始化期间使用 `exports` 对象。在文件的前三行，我们将 `add`、`multiply` 和 `factorial` 函数附加到 `exports` 对象上。记住，JavaScript 是松散类型的，因此开发者可以自由地使用点（`.`）运算符将函数和值直接附加到 `exports` 上。对于可以附加到 `exports` 的键有一些限制，但作为经验法则，只需避免使用任何内置的 `Object` 函数名，例如 `hasOwnProperty`。我们还附加了 `now` 属性，稍后会用到。

只有附加到 `exports` 的值才会在模块外部可用。如果你想要一些在这个模块内部可重用的代码，但不想让它在此模块外部暴露，就避免将该函数附加到 `exports` 上，这样它就不可用了。我们包含了 `privateMethod` 作为示例。它没有在 mmm.js 外部导出，因此只在此文件内可用。

最后，在与 `mmm.js` 相同的目录中，为这个模块创建一个简单的测试：

```javascript
var m = require('./mmm');

console.log(m.add(3,5));
console.log(m.multiply(4,5));
console.log(m.factorial(4));
```

test.js

**代码清单 3-9.** 数学模块测试

在终端输入 `node test.js`，你应该会看到结果打印出来。在第一行，我们调用 `require` 并提供一个文件路径，因此 `require` 函数将尝试执行该位置的文件。在 mmm.js 中，我们声明了几个简单的函数并将它们附加到可用的 `exports` 对象上。`exports` 对象被 Node 模块框架用来返回一个赋值给 `m` 的结果对象。`m` 上附加了 `add`、`multiply` 和 `factorial` 函数，这些函数又指向 mmm.js 内部的函数。这就是你将在生态系统中遇到的所有 Node 模块的工作方式。

因为 `require` 的参数是一个文件路径，所以这个模块不需要 `package.json` 文件；我们编写了一个供自己本地使用的模块。

## 缓存

既然我们已经编写了自己的模块，我们应该快速了解一下模块缓存。当你在代码清单 3-9 中 `require('./mmm')` 时，它会运行 mmm.js 文件中的 JavaScript 代码并返回一个对象。在 Node 模块系统的底层，`require` 的结果在第一次为特定模块调用后会被缓存。这意味着多次调用 `require('./mmm')` 将始终返回同一个 mmm 模块实例。因为在一个 Node 应用程序中经常需要多次引入同一个模块，所以使用缓存来减轻性能开销。一个重要的注意事项是，使用的缓存键是基于*解析后的*文件名。因此，如果一个程序多次 require mmm，但要求的路径不同（`require("mmm")` 与 `require('./othermodule/node_modules/mmm')`），就足以"打破缓存"，这将被视为加载一个新模块。

通过一个简单的演示更容易理解这一点，例如代码清单 3-10：

```javascript
var m = require('./mmm');

console.log('time after first require ' + m.now);

console.log(m.add(3,5));
console.log(m.multiply(4,5));
console.log(m.factorial(4));

setTimeout(function () {
  m = require('./mmm');
  console.log('time after second require ' + m.now);
}, 5000);
```

**代码清单 3-10.** 模块缓存

如果你运行更新后的测试，你会看到时间没有变化，即使我们使用了 `setTimeout` 并重新运行了 `require('./mmm')`。`now` 是在 "./mmm" 运行时设置的，那么为什么当我们第二次调用 `require` 时它没有改变呢？这就是 Node 模块缓存系统在起作用。模块系统知道它之前已经从 "./mmm" 加载过 mmm，所以创建它的代码没有必要运行第二次。在代码清单 3-10 中，mmm.js 中设置 `now` 的那行代码只运行了一次，所以 `now` 是在模块第一次通过 `require` 加载时设置的。在继续创建自己的 Node 模块时，请务必记住这一点。模块缓存的完整解释可以在 [Node.js 文档中这里](https://nodejs.org/api/modules.html#modules_caching)找到。

## npm link

既然我们知道如何编写自己的模块，还有一个 npm 命令值得介绍：`npm link`。假设我们想将 mmm 移动到一个新的文件夹和项目中，以便我们可以单独开发它。一种让 test.js 中模块保持功能的方法是将 `require` 的路径参数更改为指向新位置。

另一个选项是使用 `npm link` 命令设置一个指向该模块的全局符号链接。这将允许你 require 该模块，就好像它安装在项目的本地



 ## npm link 步骤 1

首先，将 mmm.js 移动到一个名为 math-module 的新文件夹中，并在 math-module 目录中打开终端。接下来，创建一个 package.json 文件，因为现在我们要在单个项目之外使用这个模块。你还记得无需手动编写就能初始化 package.json 的命令吗？当提示输入模块名称时，将其命名为 mmm。在 math-module 文件夹内，运行 `npm link`。响应将是 `/your/global/modules/path > /the/directory/you/ran/the/command/from`。这告诉我们，已经为全局 Node 模块文件夹创建了一个指向 math-module 目录的符号链接。

## npm link 步骤 2

返回到存储 test.js 的文件夹。在该文件夹中，在终端输入 `npm link mmm`。同样，你会看到路径信息，提示你链接模块的位置。回顾清单 3-9，我们提供给 `require` 的路径不再有效。我们现在将 math 模块视为一个应该从 node_modules 文件夹加载的社区模块。记住，`require` 可以接受多个参数，其中之一就是模块名称。我们在步骤 1 中创建了一个符号链接，并在相应的 package.json 文件中将模块命名为 mmm。让我们更新 test.js，通过名称来引入我们的模块：

test.js

```
var m = require('mmm');

console.log(m.add(3,5));
console.log(m.multiply(4,5));
console.log(m.factorial(4));
```

**清单 3-11.** 测试脚本的链接更新

所有链接设置完成后，再次尝试运行 `node test.js`。它应该与之前完全相同。通过设置链接，我们将要编写的模块与使用它的应用程序分离开来。这使我们能够在与测试代码解耦的情况下处理模块。由于 `npm link` 本质上只是带有一些额外 npm 功能的符号链接，因此你对 math 模块所做的任何更改都会继续反映在 test.js 中。

# 小结

在本章中，我们讨论了 Node 的模块和 npm 是如何工作的。我们从介绍 npm 开始，npm 是 Node 的包管理器，用于从 npm 仓库搜索和加载包。我们检查了 npm 用于安装包的 package.json 文件的结构。我们还讨论了 node_modules 文件夹，这是 npm 安装本地模块的地方，以及我们如何使用 `require()` 来加载模块。最后，我们编写了自己的模块，可以在示例 Node 脚本中使用。

在下一章中，我们将讨论 Node 的编程模型。

# 第 4 章

## Node 的编程模型

一种语言的编程模型定义了开发者如何编写代码，它可能成就也可能毁掉一种语言。由于 Node 就是 JavaScript，语言规则是相同的；然而，Node 遵循一些额外的约定，使其核心和第三方模块的代码保持一致。在第 2 章中，你学习了如何在 Node 中创建一个简单的 HTTP 服务器。本章的目标是帮助你更好地理解该服务器的代码结构，以便你可以将其扩展到其他 Node 应用程序。

## 事件循环

关于 JavaScript，以及引申到 Node，最重要的概念是它是**单线程**的。这意味着 JavaScript 应用程序一次只能执行一个任务。不过，它们可以通过使用事件循环来*营造*多线程的*假象*。本质上，JavaScript 引擎维护了几个未处理任务的队列。这些队列包括事件、定时器、间隔和立即执行等。事件循环的每次执行，称为一个周期，会导致一个或多个任务出队并执行。随着这些任务的执行，它们可以向内部队列添加更多任务。每个周期由更小的步骤组成，称为**滴答**。一个滴答的例子是从定时器队列中访问一个项目。

## 注意：并发执行

在 JavaScript 中有几种实现并发执行的方法。最常见的例子是 Web Workers，它在单独的线程中执行代码。在 Node 中，你可以使用 `child_process` 和 `cluster` 模块来分叉子进程。

清单 4-1 展示了一个在多个事件循环周期中执行的简单示例：

```
console.log('one event loop cycle');

setTimeout(function() {
  console.log('different cycle');
}, 100);

console.log('same cycle');
```

**清单 4-1.** 在多个事件循环周期中执行的代码。

这个示例将三个字符串输出到控制台。字符串记录的顺序反映了它们在哪个事件循环周期中执行。此代码的输出如清单 4-2 所示：

```
$ node event-loop.js
one event loop cycle
same cycle
different cycle
```

**清单 4-2.** 运行清单 4-1 中代码的控制台输出。

注意，`setTimeout()` 内部的 `console.log()` 尽管是源代码中的第二个，却是最后执行的。这是因为 `setTimeout()` 函数将代码排队到未来的周期中运行。

## 并发的假象

当各个任务运行迅速时，事件循环使得 JavaScript 应用程序看起来是多线程的。不幸的是，只需几行代码就能轻易让这个假象破灭。例如，清单 4-3 创建了两个间隔，它们会重复输出到控制台。一个间隔输出 `Task A`，另一个输出 `Task B`：

```
setInterval(function() {
  console.log('Task A');
}, 10);

setInterval(function() {
  console.log('Task B');
}, 15);
```

**清单 4-3.** 包含两个间隔任务的示例。

如果这些间隔真正并发执行，对一个任务的任何更改都不会影响另一个。为了证明 JavaScript 中并非如此，清单 4-4 在任务 B 中引入了一个无限循环：

```
setInterval(function() {
  console.log('Task A');
}, 10);

setInterval(function() {
  while (true) ;
  console.log('Task B');
}, 15);
```

**清单 4-4.** 一个无限循环摧毁了 JavaScript 中并发的假象。

如果你运行这段修改后的代码，`Task A` 会在十毫秒后输出到控制台，但之后什么都不再发生。当任务 B 第一次运行时，它进入了一个无限循环。这阻止了控制权返回到事件循环，因此任务 A 永远不会再次运行。如果这些任务在单独的线程或进程中执行，任务 A 会继续执行，而任务 B 则在循环。

## 异步编程

Node.js 几乎就是异步应用设计的代名词，特别是异步 I/O 操作。正如你在第 2 章中学到的，I/O 极其缓慢。大多数语言执行**同步 I/O**（也称为**阻塞 I/O**），这意味着它们开始某个 I/O 操作（如磁盘读取、网络调用等），然后空闲等待操作完成。通常，使用阻塞 I/O 调用的语言也是多线程的；因此，当一个线程空闲时，另一个线程可以执行有意义的工作。当然，正如你已经看到的，JavaScript 是单线程的。如果 Node 要阻塞 I/O 调用，整个应用程序将会停滞不前，直到 I/O 完成，因为没有其他线程可用来执行工作。

为了避免与阻塞 I/O 相关的性能损失，Node.js 几乎只使用异步非阻塞 I/O。在这种范式下，应用程序将启动一些长时间运行的外部操作，如 I/O；然而，不是等待响应，程序会继续执行额外的代码。一旦异步操作完成，结果会传回 Node 应用程序进行处理。

这在理论上看起来很简单，但还有一个大问题没有回答：异步操作的结果如何传回 Node 应用程序？有几种方法可以实现。Node 中最流行的三种方法是回调函数、事件发射器和 Promise。关于哪种方法是正确的方法，曾经有过许多激烈的争论，但最终一切都归结为个人偏好。在 Node 核心中，回调函数是主要的赢家，事件发射器位居第二。Promise 在第三方模块中相当成功，在 AngularJS 中使用较多，因此我们也会提及它们。



# 回调函数

简而言之，回调函数是在异步操作完成后被调用的函数，操作结果作为函数参数传入。清单 4-5 展示了一段调用回调函数的异步代码示例：

```javascript
var fs = require('fs');

fs.readFile('README.txt', 'utf8', function(error, data) {
    if (error) {
        return console.error(error);
    }

    console.log(data);
});
```

**清单 4-5.** 使用回调函数异步读取文件。

此示例使用了核心 `fs` 模块，该模块包含用于操作文件系统的函数。我们使用 `fs.readFile()` 方法来——顾名思义——读取一个文件。`readFile()` 接受三个参数：文件名、文件使用的字符编码，以及文件读取完成后调用的回调函数。在此示例中，我们使用 UTF-8 字符编码读取文件 `README.txt`。

调用 `readFile()` 会触发文件系统 I/O 操作。一旦 I/O 完成，`readFile()` 的回调函数将被调用，并传入两个参数。第一个参数 `error` 代表读取文件过程中发生的任何潜在异常。例如，如果 `README.txt` 不存在，`error` 将包含一个 `Error` 对象。然而，如果文件存在且读取数据没有问题，`error` 将为 `null`，而 `data` 将是包含文件内容的字符串。

## 调用约定

为了使 Node 项目中的编码更加一致，社区采用了一些约定。虽然这些不是语言规则，但它们被认为是最佳实践，尤其是在有多个开发者的项目中。其中两个被普遍接受的约定如清单 4-5 所示。第一个约定是，当将回调函数作为参数传递时，它应该是最后一个参数。采用这个约定使你的代码更具可读性，因为你可以先看到所有输入参数，然后是后续处理函数。

清单 4-5 中展示的另一个调用约定与错误处理有关。注意 `error` 是 `readFile()` 回调的第一个参数。如果错误可以传递给回调函数，Node 约定规定它必须是第一个参数。这看似随意，但它使错误处理成为开发者的首要考虑。这样想：如果错误参数排在最后，许多开发者会直接忽略它。事实上，如果错误排在最后，你编写回调函数时甚至可以完全省略错误参数。通过让错误排在第一位，你是在说"嘿，可能会出错，你需要检查它。"

还有一个与方法命名相关的常见约定，虽然清单 4-5 中没有体现，但值得指出。如前所述，在 Node 中异步代码是常态而非例外；然而，同步代码确实有其用武之地（初始化代码、shell 脚本等）。为了使代码更易于理解，许多同步函数在其名称后附加了 `Sync` 字符串。这在 [fs 模块](https://nodejs.org/api/fs.html) 中尤为常见，因为大多数方法都有同步和异步版本。例如，清单 4-5 使用了 `readFile()` 方法，但也可以使用同步的 `readFileSync()` 方法编写，如清单 4-6 所示：

```javascript
var fs = require('fs');

try {
    var data = fs.readFileSync('README.txt', 'utf8');

    console.log(data);
} catch (error) {
    console.error(error);
}
```

**清单 4-6.** 清单 4-5 的同步等效实现。

## 异常处理

注意清单 4-6 中的同步代码使用了 try...catch 语句来处理错误，而异步版本则没有。这是异步代码中的一个关键区别，你必须理解。当发出异步函数调用时，程序执行会继续进行，而异步调用在后台完成。在此期间，应用程序的调用栈会发生变化。

try...catch 语句无法捕获异步抛出的错误，因为错误并非在 try...catch 内部抛出。清单 4-7 展示了一个说明此要点的示例。在此示例中，如果读取文件时发生错误，回调函数将*重新抛出*错误；然而，由于回调函数是异步调用的，try...catch 无法处理该错误：

```javascript
var fs = require('fs');

try {
    fs.readFile('README.txt', 'utf8', function(error, data) {
        if (error) {
            throw error;
            return;
        }

        console.log(data);
    });
} catch (error) {
    console.error('Caught the error synchronously');
}
```

**清单 4-7.** 尝试捕获异步抛出的错误。

你会注意到在 Node 应用程序中 try...catch 语句使用得很少。它们用于像 `JSON.parse()` 这样的同步函数，但除此之外并不多见。Node 支持一种名为[域（domains）](https://nodejs.org/api/domain.html)的异步错误处理机制，但它们的行为不一致，在官方文档中被列为不稳定。在 Node 中处理错误的通常方式是通过回调函数传递错误，直到到达一个适合处理它们的地方。

## 回调地狱

异步代码的一个缺点是，如果代码结构组织不当，你可能会陷入地狱——具体来说就是**回调地狱**。回调地狱发生在多个回调函数相互嵌套时。考虑清单 4-5 中的文件读取器。在那个示例中，我们只是尝试读取一个文件，如果发生错误，我们就将其打印到控制台并退出。但是，如果我们想采取额外的预防措施来完全避免某些错误情况呢？

通过添加一些额外的代码，我们可以验证文件是否存在，以及文件名是否对应一个文件而不是目录或其他东西。清单 4-8 展示了如何实现这一点。不幸的是，通过添加对 `fs.exists()` 和 `fs.stat()` 的调用，此示例中的函数嵌套层级增加了两层。注意代码缩进变得越来越深——这就是回调地狱的开始。在一个非简单的应用程序中，缩进深度可以轻易超过十层，导致代码难以阅读和维护：

```javascript
var fs = require('fs');
var fileName = 'README.txt';

fs.exists(fileName, function(exists) {
  if (!exists) {
    return console.error('File does not exist');
  }

  fs.stat(fileName, function(error, stats) {
    if (error) {
      return console.error(error);
    } else if (!stats.isFile()) {
      return console.error('Not a file');
    }

    fs.readFile(fileName, 'utf8', function(error, data) {
      if (error) {
        return console.error(error);
      }

      console.log(data);
    });
  });
});
```

**清单 4-8.** 一个遭受早期回调地狱之苦的小型异步程序。

幸运的是，回调地狱可以通过智能地组织代码来轻松避免。首先，注意在可以避免的情况下没有增加缩进。整个函数体不包含在 `if` 语句中。相反，`if` 语句用于检查某些条件，如果条件满足则直接返回。其次，我们可以使用具名函数代替匿名回调函数。清单 4-9 展示了如何使用具名函数重写前面的示例。注意使用这种方法可以立即消除回调地狱，代价是代码略多一些[3]：

```javascript
var fs = require('fs');
var fileName = 'README.txt';

function readCallback(error, data) {
  if (error) {
    return console.error(error);
  }

  console.log(data);
}

function statCallback(error, stats) {
  if (error) {
    return console.error(error);
  } else if (!stats.isFile()) {
    return console.error('Not a file');
  }

  fs.readFile(fileName, 'utf8', readCallback);
};

function existsCallback(exists) {
  if (!exists) {
    return console.error('File does not exist');
  }

  fs.stat(fileName, statCallback);
}

fs.exists(fileName, existsCallback);
```

**清单 4-9.** 为避免回调地狱而对清单 4-8 进行的重写。



 ## 事件发射器

实现异步代码的第二种方式是使用事件。如果你做过任何客户端 JavaScript 开发，你肯定接触过事件和事件驱动编程。在这种模式下，被称为**事件发射器**的对象创建或发布事件；例如，在浏览器中，事件可以是鼠标点击或按键操作。在代码的其他地方，订阅者可以监听这些事件，并在事件发生时做出响应。

在 Node 应用程序中，事件发射器使用 `EventEmitter` 数据类型创建。清单 4-10 中的示例展示了如何使用 EventEmitter 创建事件：

```
var events = require('events');
var EventEmitter = events.EventEmitter;
var emitter = new EventEmitter();

emitter.emit('start');
emitter.emit('count', 1);
emitter.emit('count', 2);
```

**清单 4-10.** 使用 EventEmitter 创建多个事件。

示例的第一行导入核心 events 模块，第二行将 EventEmitter 构造函数赋值给变量 EventEmitter。第三行调用构造函数，创建一个新的 EventEmitter 并存储在 emitter 变量中。

清单 4-10 的最后三行使用 `emit()` 方法发出了三个事件。`emit()` 的第一个参数是一个字符串，用于指定发出的事件类型。在本示例中，发出一个 start 事件和两个 count 事件。事件类型之后的任何参数都会作为参数附加到事件中。start 事件没有任何参数，但 count 事件各自包含一个数字参数，表示当前计数。请注意，此示例不会产生任何输出。我们还需要监听事件，但很快会讲到这一点。

## 扩展 EventEmitter

创建自己的类来扩展 EventEmitter 类型也相当简单。清单 4-11 展示了如何实现这一点。在此示例中，我们将创建一个每秒发出一次新计数的计数器。请注意，EventEmitter 是在将 Counter 对象设置为 this 的情况下调用的。还要注意，继承关系是使用 `util.inherits()` 方法建立的，该方法是 Node 核心的一部分：

```
var util = require('util');
var EventEmitter = require('events').EventEmitter;

function Counter() {
  var self = this;

  EventEmitter.call(this); // 调用 EventEmitter 构造函数
  var count = 0;

  this.start = function() {
    this.emit('start');

    setInterval(function() {
      self.emit('count', count);
      ++count;
    }, 1000);
  };
}

util.inherits(Counter, EventEmitter); // 设置继承
```

**清单 4-11.** 一个继承自 `EventEmitter` 的 `Counter`。

然后可以使用清单 4-12 中所示的代码实例化 `Counter` 类型。在下一节中，我们将学习如何监听 `Counter` 或任何其他事件发射器发出的事件。

```
var counter = new Counter();
```

**清单 4-12.** 实例化一个 `Counter` 事件发射器。

## 监听事件

要使事件有用，必须至少有一个订阅者来监听它们。要在 Node 中设置事件监听器，请使用 on()、addListener() 和 once() 方法。on() 和 addListener() 的工作方式完全相同：它们为特定类型的事件创建监听器。我们更喜欢用 on() 而不是 addListener()，因为它需要更少的字符。清单 4-13 展示了如何使用 on() 来监听 Counter 示例发出的 start 和 count 事件。此示例定义了两个监听器：一个用于 start 事件，另一个用于 count 事件。监听器响应的事件类型由传递给 on() 的第一个参数表示。每次发出正确类型的事件时，作为第二个参数传递的回调函数就会被调用。如果发出的事件有任何与之关联的参数，它们会传递给回调函数：

```
var counter = new Counter();

counter.on('start', function() {
    console.log('start event');
});

counter.on('count', function(count) {
    console.log('count = ' + count);
});

counter.start();
```

**清单 4-13.** 监听 Counter 发出的事件。

回想一下，counter 的 start() 会发出一个 start 事件，然后每秒发出一个 count 事件。值得注意的是，on() 不是追溯性的，因此监听器只会响应在监听器附加之后发出的事件。因此，如果在调用 start() 之后才附加监听器，可能会错过一些事件。

once() 方法与 on() 类似，但有一个显著的区别。在调用 once() 的回调函数后，监听器会被移除。这使得 once() 适合处理一次性事件。例如，我们的 counter 发出一个 start 事件，然后可能发出许多 count 事件。因此，我们可以使用 once() 来监听 start 事件，如清单 4-14 所示。作为练习，建议你尝试使用 once() 来监听 count 事件，以验证监听器只被调用一次：

```
counter.once('start', function () {
    console.log('start event');
});
```

**清单 4-14.** 使用 once() 设置一次性事件监听器。

## 异常处理

使用 EventEmitter 处理异常的最简单方式是发出一个 error 事件；但是，你必须小心，因为未处理的 error 事件会导致程序终止。清单 4-15 展示了一个发出未处理错误的示例。此程序在运行时会崩溃：

```
var EventEmitter = require('events').EventEmitter;
var emitter = new EventEmitter();

emitter.emit('error', new Error('our error is bad and we feel bad'));
```

**清单 4-15.** 发出一个未处理的 error 事件。

幸运的是，error 事件可以像其他事件一样处理。清单 4-16 展示了如何使用 on() 处理 error 事件：

```
var EventEmitter = require('events').EventEmitter;
var emitter = new EventEmitter();

emitter.on('error', function(error) {
    console.error(error.message);
});

emitter.emit('error', new Error('our error is bad and we feel bad'));
```

**清单 4-16.** 使用 on() 处理 error 事件。

## uncaughtException 事件

Node 提供了一个全局的 process 对象，用于与当前运行的进程进行交互。当 error 事件未被捕获时，process 对象会发出一个 uncaughtException 事件。清单 4-17 展示了如何处理这类事件：

```
var EventEmitter = require('events').EventEmitter;
var emitter = new EventEmitter();

process.on('uncaughtException', function(error) {
    console.error(error.message);
    process.exit(-1);
});

emitter.emit('error', new Error('our error is bad and we feel bad'));
```

**清单 4-17.** 处理 uncaughtException 事件。

如果发出了 uncaughtException 事件，这意味着你的应用程序出现了严重错误。此时，你的应用程序被认为处于未定义状态，可能能够恢复，也可能无法恢复。在这种情况下，你的应用程序不应尝试恢复，而应优雅地关闭。在此示例中，使用 process.exit() 终止应用程序。

## Promises

Promise 是表示在创建时还未知的值的对象。Promise 可以被看作与异步函数相关联的合约。异步函数立即返回，但承诺某个值将在未来的某个时间点可用。过去，Promise 曾是 Node 核心的一部分，但后来被淘汰，转而使用回调函数。许多第三方模块出于作者偏好继续支持 Promise，但现在它们[从 0.11.13 版本开始回归核心](http://back-in-the-core-as-of-version-0.11.13)。Promise 最近成为 V8 引擎中完全支持的功能，这意味着它们在 Node 中也可用。

### 警告：Promise 仅在 Node 0.11.13 及更高版本中受支持

如果你使用的是 0.11.13 之前的版本，本节中与 Promise 相关的代码将无法工作。相反，你会遇到错误消息 `ReferenceError: Promise is not defined`。

当 Promise 被创建时，它处于称为*待处理*或*未履行*的状态。Promise 保持这种状态，直到其关联的异步代码执行完毕。如果异步代码成功完成，Promise 进入*已履行*状态。但如果异步调用由于某种原因失败，Promise 则进入*已拒绝*状态。

在代码中，Promise 使用 `Promise` 构造函数创建，如清单 4-18 所示。`Promise()` 接受一个参数，即一个回调函数，该函数自身接受两个参数。回调参数 `resolve` 和 `reject` 都是函数。要履行 Promise，你调用 `resolve()` 函数。要拒绝 Promise，你调用 `reject()`。你可以向 `resolve()` 和 `reject()` 传递任何你想要的参数，但按照惯例，只有 `Error` 对象应该传递给 `reject()`：

```
var promise = new Promise(function(resolve, reject) {
  var success = true;

  if (success) {
    resolve('promise fulfilled');
  } else {
    reject(new Error('promise rejected'));
  }
});
```

**清单 4-18.** 创建一个 Promise。

[清单 4-19](http://listing-4-19) 展示了 Promise 如何与异步代码一起使用，我们以文件读取器示例为例来说明。它看起来很像原始的文件读取器示例；但是，我们不是将消息打印到控制台，而是根据 `readFile()` 的结果来履行或拒绝 Promise：

```
var fs = require('fs');
var promise = new Promise(function(resolve, reject) {
  fs.readFile('README.txt', 'utf8', function(error, data) {
    if (error) {
```



 ```
return reject(error);
}

resolve(data);
});
});
```

**清单 4-19.** 在异步代码中使用 Promise。

下一个问题是，传递给`resolve()`或`reject()`的值能用来做什么？这就是 Promise 的`then()`方法发挥作用的地方。`then()`接受两个参数：一个成功的回调函数和一个失败的回调函数。正如你所期望的，如果 Promise 被履行（fulfilled），则调用成功回调；如果 Promise 被拒绝（rejected），则调用失败回调。[清单 4-20](#)是清单 4-19 的延续，说明了`then()`的使用方式。这个例子只是在成功时打印文件内容，或在拒绝时打印错误消息：

```
promise.then(function(result) {
    console.log(result);
}, function(error) {
    console.error(error.message);
});
```

**清单 4-20.** Promise 的`then()`方法的示例用法。

值得指出的是，传递给`then()`的两个回调函数中的任何一个都可以是`undefined`，而不会出现问题。例如，[清单 4-21](#)中展示的`then()`调用就不包含失败回调。如果 Promise 被拒绝，将不会发生任何事情：

```
promise.then(function(result) {
    console.log(result);
});
```

**清单 4-21.** 不使用失败回调的`then()`示例用法。

## Promise 链式调用

Promise 的一个优点是它们可以被链接在一起。清单 4-22 展示了如何使用多个`then()`调用来实现链式调用。在这个例子中，当 Promise 被履行时，返回字符串`THE END!`。该字符串随后在链式`then()`调用中作为`result`参数可用。假设 Promise 被履行，文件内容将被打印，随后打印字符串`THE END!`：

```
promise.then(function(result) {
    console.log(result);
    return 'THE END!';
}).then(function(result) {
    console.log(result);
});
```

**清单 4-22.** 使用`then()`进行 Promise 链式调用。

你也可以使用`catch()`方法来处理 Promise 链中的拒绝情况。[清单 4-23](#)中的示例展示了`catch()`的使用方式。代码的行为就如同`catch()`回调被作为第二个参数传递给`then()`一样，但对于链式调用来说更加方便。如果 Promise 被拒绝，`catch()`回调将显示错误消息。

```
promise.then(function(result) {
  console.log(result);
  return 'THE END!';
}).catch(function(error) {
  console.error(error.message);
});
```

**清单 4-23.** 使用`catch()`方法进行 Promise 链式调用。

你甚至可以在链中交错使用`then()`和`catch()`。[清单 4-24](#)中的示例会根据原始 Promise 的结果，打印文件内容或错误消息。无论发生什么，最后的`then()`都会打印`THE END!`：

```
promise.then(function(result) {
  console.log(result);
}).catch(function(error) {
  console.error(error.message);
}).then(function() {
  console.log("THE END!");
});
```

**清单 4-24.** 交错使用`then()`和`catch()`的 Promise 链式调用。

# 小结

本章涵盖了 Node 编程模型的基础知识。你已经了解了事件循环、回调函数、事件发射器和 Promise。你还学习了如何在异步环境中处理异常。一开始这可能看起来困难或奇怪，但经过一些练习后，你会发现它相当容易掌握。在下一章中，你将学习如何将在本章中学到的技术应用到 Node 核心模块中。

> [3]另一种避免回调地狱的常见方法是使用控制流模块。其中最受欢迎的是 [async](async)。

# 第 5 章

## 核心模块

在[第 3 章](link)中，你学习了 Node 的模块系统和`require()`函数。然后，[第 4 章](link)教你如何以 Node 的方式编写代码。在此过程中，你也看到了一些使用`http`和`fs`核心模块的示例。本章将之前讨论的所有内容整合在一起，详细解释如何使用一些 Node 核心模块。在开始之前，值得指出的是，我们只能浅尝辄止——Node 核心**太**大了，无法在一章中涵盖所有内容；然而，在完成本章后，你应该具备足够的知识来理解 [Node 文档](link)。

## 命令行参数

在 Node 中，从命令行读取参数非常简单。传递给 Node 应用程序的所有命令行参数都可以通过`process.argv`数组获取。请注意，该数组的前两个元素分别是 node 可执行文件，以及被调用的 JavaScript 文件名。这意味着实际的应用程序参数从`process.argv[2]`开始。[清单 5-1](#)展示了如何使用`forEach()`方法访问并打印命令行参数。要运行这个示例，请将代码保存到名为`argv-demo.js`的文件中，然后运行`node argv-demo foo bar baz`：

```
process.argv.forEach(function(value, index, args) {
  console.log('process.argv[' + index + '] = ' + value);
});
```

**清单 5-1.** 使用`process.argv`访问命令行参数。

## 文件系统操作

正如你在几个示例中已经看到的，`fs`模块允许你访问文件系统。如果你过去是客户端 JavaScript 开发者，你深知没有或只有不一致的用于文件系统操作的 API 是多么令人沮丧。Node 作为一个完整的服务器端实现，让这种沮丧成为过去。

### `__filename`和`__dirname`

Node 应用程序中的任何文件都可以使用`__filename`和`__dirname`变量来确定其绝对位置。`__filename`和`__dirname`是字符串，正如它们的名称所暗示的，它们分别指定正在执行的文件和包含该文件的目录。清单 5-2 展示了使用`__filename`和`__dirname`的示例。运行此代码的输出如清单 5-3 所示。你的输出会因在机器上运行代码的位置而有所不同：

```
console.log('Currently executing file is ' + __filename);
console.log('It is located in ' + __dirname);
```

**清单 5-2.** 使用`__filename`和`__dirname`打印文件路径。

```
$ node file-paths.js
Currently executing file is /home/node/file-paths.js
It is located in /home/node
```

**清单 5-3.** 运行清单 5-2 中代码的示例输出。

值得注意的是，`__filename`和`__dirname`**不是**全局变量。相反，它们是在每个文件中定义的局部变量。因此，如果你的项目由多个文件组成，这些值在每个文件中将有所不同。

### 当前工作目录

Node 应用程序有一个当前工作目录的概念。这是使用相对文件路径时的基线目录。在程序执行的任何时候，你都可以使用`process.cwd()`方法访问当前工作目录。这个方法不接受任何参数，返回一个表示应用程序工作目录的字符串。

你也可以使用`process.chdir()`方法更改当前工作目录。这个方法接受一个参数，即一个表示要更改到的目录的字符串。如果出现问题——例如，目标目录不存在——`chdir()`会抛出异常。

[清单 5-4](#)展示了如何查看和更改当前工作目录。这个示例显示当前工作目录，然后尝试移动到`/`目录。如果发生错误，它会记录到 stderr。最后，新的工作目录被打印到控制台：

```
console.log('Starting in ' + process.cwd());

try {
  process.chdir('/');
} catch (error) {
  console.error('chdir: ' + error.message);
}

console.log('Current working directory is now ' + process.cwd());
```

**清单 5-4.** 显示和更改当前工作目录。

### 读取文件

在 Node 应用程序中读取文件最简单的方式是通过`fs`模块的`readFile()`和`readFileSync()`方法。这两个方法都将要读取的文件名作为第一个参数。可选的第二个参数可用于指定额外的选项，例如字符编码。如果未指定编码，文件内容将以 Buffer 形式返回（Buffer 是 Node 中用于存储原始二进制数据的数据类型）。

同步调用`readFileSync()`返回文件内容，如果出错则抛出错误。异步调用`readFile()`将回调函数作为最后一个参数。回调函数接受两个参数：一个可能的错误对象和文件内容。[清单 5-5](#)中的应用程序使用`readFile()`结合`__filename`来读取自身的源代码。使用`readFileSync()`的等效同步代码如[清单 5-6](#)所示：

```
var fs = require('fs');

fs.readFile(__filename, function(error, data) {
  if (error) {
    return console.error(error.message);
  }

  console.log(data);
```



**清单 5-5.** 一个读取自身源代码的示例应用。

```js
var fs = require('fs');
var data;

try {
  data = fs.readFileSync(__filename);
  console.log(data);
} catch (error) {
  console.error(error.message);
}
```

**清单 5-6.** 清单 5-5 的同步等效版本。

当你运行其中一个示例时，你会注意到它显示了一个 Buffer 对象，表现为一系列原始字节。虽然这是文件内容的真实表示，但它并不特别用户友好。有两种方法可以将数据显示为字符串。第一种是在数据变量上调用 `toString()`。这会将 Buffer 内容作为 UTF-8 编码的字符串返回。第二种方法是使用可选的第二个参数指定 UTF-8 编码，如 [清单 5-7](http://example.com) 所示。这会导致数据以字符串而不是 Buffer 的形式返回。

```js
var fs = require('fs');

fs.readFile(__filename, {
  encoding: 'utf8'
}, function(error, data) {
  if (error) {
    return console.error(error.message);
  }

  console.log(data);
});
```

**清单 5-7.** 在文件读取期间设置编码类型。

## 写入文件

可以使用 `writeFile()` 和 `writeFileSync()` 方法轻松地写入文件。这些方法是 `readFile()` 和 `readFileSync()` 的对应方法。这些方法以文件名作为第一个参数，以要写入的数据（作为字符串或 Buffer）作为第二个参数。第三个参数是可选的，用于传递附加信息，例如编码类型。与 `readFile()` 变体不同，这些方法默认使用 UTF-8 编码。`writeFile()` 以回调函数作为其最后一个参数。一个可能的 error 对象是传递给回调的唯一参数。`writeFileSync()` 不返回值，但在必要时会抛出错误。[清单 5-8](http://example.com) 展示了如何使用 `writeFile()` 写入文件。

```js
var fs = require('fs');
var data = 'some file data';

fs.writeFile(__dirname + '/foo.txt', data, function(error) {
  if (error) {
    return console.error(error.message);
  }
});
```

**清单 5-8.** 使用 `writeFile()` 将数据写入文件。

默认情况下，`writeFile()` 会创建一个新文件，或者用同名文件覆盖现有文件。可以通过使用可选的第三个参数传递一个 `flag` 值来修改此行为。例如，传递标志 `wx` 会在文件已存在时抛出错误，而 `a` 标志会导致数据被追加到现有文件而不是覆盖。所有可用标志的完整列表包含在 [fs 文档](https://nodejs.org/api/fs.html) 中，`wx` 标志的示例用法如 [清单 5-9](#) 所示：

```js
var fs = require('fs');
var data = 'some file data';

fs.writeFile(__dirname + '/foo.txt', data, {
  flag: 'wx'
}, function(error) {
  if (error) {
    return console.error(error.message);
  }
});
```

**清单 5-9.** 在调用 `writeFile()` 时设置 `flag` 选项。

## 流

**流** 是在两点之间移动数据的一种机制。流可以被视为一个简单的花园水管。水管连接到水源。当水源将水推入水管时，它会流经水管的另一端。此时，水可以被洒水器或其他消费者使用。

Node 在其核心的许多部分中都使用了流，例如文件和套接字。流之所以有吸引力，是因为它们允许应用程序以小块处理数据，而不是一次处理所有数据。不幸的是，流也是一个常见的困惑来源，因为 Node 实现了多种类型的流 API。本节将以最简单的形式解释流。

### 可读流

**可读流** 是数据源。这些流会发出 `data`、`close`、`end` 和 `error` 事件，这些事件用于处理数据流。当一个称为 **数据块 (chunk)** 的新数据项可用时，流会发出一个 `data` 事件，并将实际数据作为 Buffer 传递。`close` 事件是可选的，可以在数据流的底层源（例如文件）关闭时发出。一旦流发送了其所有数据，就会发出 `end` 事件。在发出 `end` 事件后，不应再发出任何 `data` 事件。如果任何地方出错，流会发出一个 `error` 事件。

### 可读文件流

作为使用可读流的一个好例子，我们转向 `fs.createReadStream()` 方法。此方法将文件作为可读流打开。将此行为与 `readFile()` 进行比较，后者读取文件的全部内容并将其存储在内存中。如果你的应用程序需要同时处理许多可能很大的文件（例如 Web 服务器），使用 `readFile()` 时内存使用和垃圾收集可能会成为问题。

`createReadStream()` 返回一个基于作为参数传入的文件名的可读流。[清单 5-10](#listing-5-10) 使用 `createReadStream()` 显示名为 `foo.txt` 的文件的内容。请注意，`data` 事件处理程序将数据块转换为字符串，然后使用 `process.stdout.write()` 显示它。这里没有使用 `console.log()` 方法，因为它会在其显示的字符串后附加一个额外的换行符。如果使用 `console.log()` 显示需要多个数据块的输入文件，则会显示时夹杂额外的换行符。`process.stdout` 表示当前进程的标准输出流。这是一个可写流，我们稍后会介绍：

```js
var fs = require('fs');
var stream = fs.createReadStream('foo.txt');

stream.on('data', function(data) {
    var chunk = data.toString();

    process.stdout.write(chunk);
});

stream.on('end', function() {
  console.log();
});

stream.on('error', function(error) {
  console.error(error.message);
});
```

**清单 5-10.** 使用可读流显示文件的内容。

### 可写流

**可写流** 是数据的目标——或称为接收器。数据通过调用其 `write()` 方法发送到可写流。一旦所有所需数据都已写入，流的 `end()` 方法用于发出流结束的信号。你在 **清单 5-10** 中调用 `process.stdout.write()` 时已经看到了可写流的一个例子。像可读流一样，可写流也会发出 `close` 和 `error` 事件，其行为方式相同。

### 处理背压

可写流一次只能处理有限量的数据，因为底层缓冲区可能会被填满。一旦达到此限制，流就会饱和，向流写入任何额外数据都可能导致问题或不可预测的行为。**背压** 是可写流如何向其数据源发出停止发送数据信号的方式。

背压通过 `write()` 方法的布尔返回值来实现。如果此值为 `false`，则数据源不应再向流写入任何数据。这给了可写流处理已写入数据的时间。一旦流准备好接收更多数据，它会发出一个 `drain` 事件。数据源可以检测到此事件并重新开始发送数据。

### 可写文件流

与文件描述符关联的可写流是使用 `fs.createWriteStream()` 方法创建的。**清单 5-11** 展示了如何创建可写文件流。在此示例中，使用可读文件流从文件读取数据。然后使用 `pipe()` 方法自动将来自可读流的数据发送到可写流。本质上，此代码执行文件复制：

```js
var fs = require('fs');
var readStream = fs.createReadStream('foo.txt');
var writeStream = fs.createWriteStream('bar.txt');

readStream.pipe(writeStream);
```

**清单 5-11.** 将可读文件流管道连接到可写文件流。

`pipe()` 是一个便捷的方法，它允许将一个流的输出连接到另一个流的输入。这为开发者省去了处理各种与流相关的事件（如 `drain`）的麻烦。

### 标准流

Node 应用程序默认连接到三个标准流。这些流是

`stdin`、`stdout` 和 `stderr`，它们可通过 `process` 对象访问。`stdin` 是一个可读流，用于收集用户输入。`stdout` 和 `stderr` 是可写流，分别用于显示输出和错误。`console.log()` 和 `console.error()` 系列方法是对 `process.stdout.write()` 和 `process.stderr.write()` 调用的简单封装。

当 Node 应用程序运行时，`stdin` 流默认处于暂停状态；但是，你可以通过恢复流并处理 `data` 事件来从 `stdin` 读取数据。清单 5-12 展示了如何从 `stdin` 读取数据。在此示例中，使用 `stdout` 创建提示用户输入姓名的提示符。然后，使用可读流的 `resume()` 方法恢复 `stdin`。当用户输入姓名并按回车键时，会触发一个 `data` 事件。这将触发处理程序，该程序按姓名问候用户，然后将 `stdin` 恢复到暂停状态：

```
process.stdin.once('data', function(data) {
  process.stdout.write('Hello ' + data.toString());
  process.stdin.pause();
});

process.stdout.write('What is your name? ');
process.stdin.resume();
```

**清单 5-12.** 使用标准流。

## Web 编程

Node.js 最著名的可能是开发 Web 应用程序：项目主页上就有一个 Web 服务器。本节将重点介绍 HTTP 服务器。如果你对更通用的 TCP/IP 编程感兴趣，可以查看 `net_core` 模块。

## 创建服务器

清单 5-13 展示了来自 Node.js 主页的 Web 服务器示例。我们之前已经研究过这段代码示例，但在本章中我们将更深入地探讨。HTTP 服务器功能在 `http` 和 `https` 模块中定义。在这种情况下，我们正在创建一个不安全的 HTTP 服务器。创建 HTTPS 服务器的过程类似，但需要更多工作，我们将在后面重新讨论。

如你所知，HTTP 是一个请求-响应协议。客户端从服务器请求特定资源，服务器处理请求并发送回相应的响应。清单 5-13 中的服务器在每次收到客户端请求时都会执行 `createServer()` 回调。`req` 参数包含有关客户端和请求资源的信息。另一方面，`res` 参数包含有关响应的信息和方法。

`writeHead()` 方法用于写入状态码和任何可选的响应头。如清单 5-13 所示，响应头使用一个对象指定，其中对象键指定头名称，对象值表示头值。数据使用零个或多个 `res.write()` 调用写入。所有数据写入完成后，服务器通过一次**必须**调用 `res.end()` 来完成连接。为了方便起见，`res.end()` 支持与 `res.write()` 相同的参数。这意味着整个响应都可以通过 `res.end()` 写入，如清单 5-13 所示。这个基本服务器返回一个响应头 `Content-Type`，一个 200 响应状态码，以及正文 `Hello World\n`：

```
var http = require('http');
http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello World\n');
}).listen(1337, '127.0.0.1');
console.log('Server running at http://127.0.0.1:1337/');
```

**清单 5-13.** 一个非常简单的 HTTP 服务器。

图 5.1 显示了 Chrome 中来自此服务器的响应是什么样子。Chrome 的开发者工具已被用于检查 HTTP 请求和响应。“Hello World” 响应正文清晰地显示在主浏览器窗口中。注意 200 OK 状态码和值设置为 `text/plain` 的 `Content-Type` 响应头。还要注意，包含了许多其他未在应用逻辑中指定的响应头。如果应用程序未包含它们，Node 将默认添加许多响应头。

![](img/0ca996f5fd0375fc118091628c3c7a87_100_0.png)

启动服务器的最后一步是调用 `listen()` 方法。这将使服务器开始在端口 1337 上接受连接。第二个参数是可选的，用于指定服务器将响应的主机。这在具有多个网络接口的机器上很有用。一旦服务器成功监听端口，就会发出一个 `listening` 事件。你可以为 `listen()` 提供一个可选的回调来处理该事件。

## 路由

清单 5-13 中的服务器非常有限，因为它以完全相同的方式响应每个请求。真实的服务器可能需要根据请求方法（也称为 **动词**）和 URL 执行不同的操作。HTTP 动词和请求 URL 的组合被称为**路由**。在前面的示例中，每个路由都返回相同的响应。清单 5-14 展示了一个更新后的服务器，它支持两个路由，并为不匹配的请求添加了一个返回 404 状态码的处理程序。注意，请求的 URL 可通过 `req.url` 获取，而 HTTP 动词在 `req.method` 中找到：

```
var http = require('http');

http.createServer(function(req, res) {
  if (req.url === '/' && req.method === 'GET') {
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.end('Hello <strong>home page</strong>');
  } else if (req.url === '/account' && req.method === 'GET') {
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.end("Hello <strong>account page</strong>");
  } else {
    res.writeHead(404, {'Content-Type': 'text/html'});
    res.end();
  }
}).listen(1337);
```

**清单 5-14.** 一个支持多个路由的 HTTP 服务器。

## 访问请求头

头是 HTTP 事务的重要组成部分。例如，负责在 Web 应用程序中维护状态的 Cookie，就是通过 Cookie 请求头从客户端发送到服务器的。同样，当服务器设置 Cookie 时，也是通过 Set-Cookie 响应头完成的。你已经看到设置响应头有多简单。Node 使得获取请求头的值同样简单——它们在 `req.headers` 中可用。为了更简单，Node 会将头名称转换为小写，因此无需测试 `Host` 和 `host`。例如，要读取 Cookie 请求头的值，你会检查 `req.headers.cookie`。如果头名称中包含连字符（例如 `User-Agent`），你会使用 `req.headers[‘user-agent’]`。清单 5-15 中的示例报告了 User-Agent 头的值：

```
var http = require('http');
http.createServer(function (req, res) {
    res.end('Your user agent is ' + req.headers['user-agent']);
}).listen(1337, '127.0.0.1');
console.log('Server running at http://127.0.0.1:1337/');
```

**清单 5-15.** 访问 HTTP 请求头的示例。

# 总结

本章介绍了 Node 一些核心模块的基础知识。具体来说，本章对命令行、文件系统、流和 Web 服务器进行了快速概览。不幸的是，完整的 Node 核心概述超出了本书的范围，但鼓励读者探索完整文档。

# 第 6 章

## 构建 Node 服务器

我们已经涵盖了在前面章节中深入创建真实 Node 服务器所需的所有内容。本章将专注于为我们用于演示 MEAN 栈的人力资源应用程序构建一个 Node 服务器子集。

## 服务器计划

在开始编写任何代码之前，你需要对 Web 服务器应该做什么有一个基本的想法。对于这个子集示例，我们的服务器需要完成两项任务：以列表形式查看员工信息，以及查看单个员工信息。服务器还必须能够发送静态资源，如 CSS、客户端 JavaScript、图像和 HTML 文件。我们应该努力使各种员工资源符合 RESTful 规范，而不是使用 SOAP/WSDL。随着我们深入开发人力资源应用程序，你会发现使用简单易用的 RESTful API 钩住不同的前端框架（如 Angular）要容易得多。RESTful 设计模式也与我们应用程序所需的员工操作（即创建、检索、更新和删除 - CRUD）完美契合。我们应该将静态资源分离到它们自己的文件夹中，并将代码分解成逻辑上可重用的部分。



# 构建应用结构

以下是应用的文件结构。这里列出的文件和文件夹将经常被引用，请将清单6-1放在手边：

```
├── database
│   └── employees.json
├── index.js
├── lib
├── node_modules
│   └── colors
├── package.json
└── public
    ├── home.html
    └── style.css
```

**清单 6-1.** Node示例应用的最终目录结构。

一般来说，`lib`文件夹用于存放本地、项目特定的模块。在`public`文件夹内，我们将存放静态资源。为了简化本示例，我们将使用`employees.json`作为可查询的数据库。可以看到`node_modules`目录已存在，并且我们已经安装了`colors`模块。

# 入门

还记得用于启动新Node项目的`npm`命令吗？创建一个新目录并在该目录中打开终端窗口。在该文件夹内，使用正确的`npm`命令初始化一个新的Node应用。之后，安装`colors`并确保`package.json`文件已创建并更新。接着，在目录根目录下创建`index.js`文件。

最后，我们将编写一个贯穿全书多次出现的桩服务器：

```javascript
var http = require('http');

http.createServer(function (req, res) {
  // 一个经过解析的URL，以便在有参数时使用
  var _url;

  // 以防客户端使用小写的请求方法。
  req.method = req.method.toUpperCase();
  console.log(req.method + ' ' + req.url);
  res.end('The current time is ' + Date.now())

}).listen(1337, '127.0.0.1');

console.log('Server running at http://127.0.0.1:1337/');
```

清单6-2创建了一个服务器并开始在端口1337上监听。如果你向localhost:1337/发起请求，你应该会看到信息被记录到控制台，表明服务器正在监听。你应该注意到，在这种状态下服务器从未响应。你能看出原因吗？这是因为我们还没有对`res`对象做任何处理；具体来说，从未调用`res.end()`。`res.end()`是结束并向传入请求发送响应的方法。随着服务器功能变得更加完善，我们将填充正确的响应。

**注意：关于req和res**

在Node服务器中常见的`req`和`res`对象分别是“request”和“response”的缩写。本例中的`req`对象是一个`http.ClientRequest`对象。你可以在[Node.js文档](https://nodejs.org/api/http.html)中找到关于此对象的更多信息。相关的`res`对象是一个`http.ServerResponse`对象，其文档同样可在[Node.js文档](https://nodejs.org/api/http.html)中找到。深入探讨这些对象的细节超出了本书的范围。目前，请尝试记住“req/request”是传入的请求，而“res/response”是服务器构建并最终发送的响应。如果你对这些对象的方法、属性或事件有疑问，我们建议你查阅指定的Node.js文档链接。

## 路由

任何Web服务器最基本的功能是路由请求。回顾我们的服务器计划，我们主要关注三个路由：

1.  获取员工列表的路由
2.  获取特定员工的路由
3.  用于静态文件的通用捕获所有路由

此外，本示例服务器只支持GET请求，因此如果客户端尝试发起非GET请求，我们应该正确响应：

```javascript
http.createServer(function (req, res) {
  // 一个经过解析的URL，以便在有参数时使用
  var _url;

  // 以防客户端使用小写的请求方法。
  req.method = req.method.toUpperCase();
  console.log(req.method + ' ' + req.url);

  if (req.method !== 'GET') {
    res.writeHead(501, {
      'Content-Type': 'text/plain'
    });
    return res.end(req.method + ' is not implemented by this server.');
  }

  if (_url = /^\/employees$/i.exec(req.url)) {
    // 返回员工列表
    res.writeHead(200);
    return res.end('employee list');
  } else if (_url = /^\/employees\/(\d+)$/i.exec(req.url)) {
    // 根据路由中的id查找员工
    res.writeHead(200);
    return res.end('a single employee');
  } else {
    // 尝试发送静态文件
    res.writeHead(200);
    res.end('static file maybe');
  }
}).listen(1337, '127.0.0.1');
```

**清单 6-3.** 具有基础路由的Node服务器

首先，我们确保请求方法是GET。如果不是，正确的响应状态码应该是501。我们使用`res.writeHead`并传递两个参数。第一个参数是将返回给客户端的状态码。第二个是响应头。在本例中，我们只提供“Content-Type”为纯文本。

如果传入的方法是GET请求，我们希望尝试路由该请求。首先，我们想查看请求是否是针对“/employees”的。正则表达式会对`req.url`运行并查找匹配项。如果匹配，`_url`将有一个值，执行第一个`if`块，并响应“employee list”。如果`req.url`与第一个正则表达式不匹配，我们尝试第二个正则表达式检查“/employees/a_number”。在这种情况下，服务器将响应“a single employee”。最后，如果请求的URL与任一正则表达式都不匹配，我们将假设它是一个静态文件。代码将检查文件系统以定位该文件，然后发送它。如果文件不存在，应发送的正确状态码是404。

对于这两个员工路由，我们都必须查询数据库。为了避免将数据库查询逻辑污染到`index.js`中，我们将编写一个简单的数据库模块。记住，对于这个示例，数据库将是一个JSON文件。

#### 数据库模块

数据库模块应封装获取员工列表和根据ID查找单个员工所需的逻辑。你可能记得在前面的章节中，我们提到数据库查询是I/O操作，应该是非阻塞的。非阻塞I/O的JavaScript模式是提供一个回调函数，该函数在I/O完成时执行。

在`lib`文件夹中创建一个`employees.js`文件，在`database`文件夹中创建一个`employees.json`文件：

```javascript
var employeeDb = require('../database/employees');

exports.getEmployees = getEmployees;
exports.getEmployee = getEmployee;

function getEmployees (callback) {
  setTimeout(function () {
    callback(null, employeeDb);
  }, 500);
}

function getEmployee (employeeId, callback) {
  getEmployees(function (error, data) {
    if (error) {
      return callback(error);
    }

    var result = data.find(function(item) {
      return item.id === employeeId;
    });

    callback(null, result);
  });
}
```

**清单 6-4.** 简单的数据库模块

这个模式在关于模块的章节中应该看起来很熟悉。我们导出两个函数，一个用于获取员工列表（`getEmployees`），另一个用于获取单个员工（`getEmployee`）。这两个函数都以`callback`作为参数。该函数将在I/O完成时执行。

如果你记得我们讨论`require`关键字时，你会回忆起它接受许多不同的文件和路径。一个选项是传递一个JSON文件的路径。在清单6-1的`database`文件夹下，我们有一个`employees.json`文件。将清单6-5的内容复制到`database/employees.json`中。

```json
[
  {
    "id": "1000003",
    "name": {
      "first": "Colin",
      "last": "Ihrig"
    },
    "address": {
      "lines": ["11 Wall Street"],
      "city": "New York",
      "state": "NY",
      "zip": 10118
    }
  },
  {
    "id": "1000021",
    "name": {
      "first": "Adam",
      "last": "Bretz"
    },
    "address": {
      "lines": ["2 Market Square", "(Market Square)"],
      "city": "Pittsburgh",
      "state": "PA",
      "zip": 15222
    }
  }
]
```

`var employeeDb = require('../database/employees');`会将JSON文件加载到内存中，作为普通的JavaScript集合，可以从本文件中的函数中引用。同样，为了模拟对真实数据库的查询，我们在`getEmployees`函数中使用`setTimeout`插入了一些延迟。

`getEmployee`函数接受两个参数：一个回调函数和一个员工ID。首先，我们调用`getEmployees`函数并传递一个匿名函数作为回调参数。在3000毫秒后，`getEmployees`函数将执行回调函数并传递给调用者错误和数据参数。如果有错误，我们希望执行回调函数并将此错误冒泡到调用函数。这是一种极其常见的模式，值得记住。如果没有错误，我们希望遍历数据并尝试定位ID等于`employeeId`的员工。最后，执行回调函数并返回任何错误以及来自“数据库”的员工对象。

在Node中，常见的回调约定是回调函数的第一个参数应该是错误对象，如果没有错误则为null。同样，如果一个函数需要回调函数，就像我们的两个员工函数一样，参数列表中的最后一个参数应该是回调函数。你会发现这在Node社区中是一种常见做法。

### 注意：find方法

关于`find`方法的简要说明。它在ECMAScript 6规范中，但截至Node版本0.10.32，在Node运行时中目前不可用。对于这个示例，你可以为`Array.find`方法添加一个polyfill。Polyfill是一个术语，用于描述能够在尚不支持某些特性的环境中使用未来JavaScript特性的代码。



在尚未支持该功能的环境中，你可以编写一个额外的方法，该方法位于 `lib/employees` 目录下，用于根据 ID 在数组中定位元素。一旦引入真正的数据库，这段代码将被移除，因此无需花费过多时间。

## 查询数据



 ## 摘要

本章聚焦于为一个人力资源应用构建 Node 服务器的一个子集，我们将在本书中用它来演示 MEAN 技术栈。我们首先为应用搭建了一个骨架结构，然后添加了涵盖路由、查询数据库和发送响应的基本功能。在后续章节中，我们将对这些功能进行重构。

在下一章中，我们将介绍 MongoDB。

## 第 7 章
## MongoDB 简介

几乎所有 Web 应用都依赖某种数据库来持久化信息。数据库主要分为关系型数据库和 NoSQL 数据库两类。关系型数据库作为多年来的事实标准，以使用 SQL 为特征。NoSQL 数据库家族正如其名，不使用 SQL，近年来逐渐崛起，主要因为它们被认为更易于使用且速度更快。MongoDB 官方文档提供了一份[非常详尽的（Mongo 特有的）NoSQL 命令与 SQL 的对比](http://docs.mongodb.org/manual/reference/sql-comparison/)。接下来的三章将讨论 MongoDB——最流行的 NoSQL 数据库之一，而关系型数据库将在[第 10 章](#)中探讨。

## NoSQL 数据库

NoSQL 这个名称有些笼统，指的是多种数据存储类型。本质上，NoSQL 代表任何不使用 SQL 的数据存储。一些 NoSQL 数据库的类型示例包括文档存储、对象存储和键/值存储。NoSQL 实现的例子有 [Redis](https://redis.io/)、[Memcached](https://memcached.org/)、[Cassandra](https://cassandra.apache.org/)，当然还有 MongoDB。这些都不遵循关系型数据库基于表的设置。

NoSQL 数据库通常比关系型数据库更快，因为它们通常不遵循预定义的架构，也不像其关系型数据库"表亲"那样严格地强制数据一致性。这意味着 NoSQL 数据存储通常适用于原型设计，以及数据不需要始终完全一致的那些社交媒体应用。例如，如果你错过了 Facebook 动态中的一条信息，这可能没什么大不了的。另一方面，你可能希望你的银行账户准确反映你存入的金额，因此关系型数据库更为可取。

## MongoDB 的历史

MongoDB 的开发始于 2007 年，当时一家名为 10gen 的公司。Mongo 最初是作为计划中的 PaaS（平台即服务）产品的一个组件而设计的。随后在 2009 年，MongoDB 被开源。Mongo 取得了巨大的成功，以至于 10gen 将其公司名称改为 MongoDB Inc.，以便更紧密地将公司名称与其旗舰产品关联起来。自发布以来，Mongo 已被许多知名公司使用，包括 Craigslist、Foursquare、eBay 和《*纽约时报*》（*The New York Times*）。据 [db-engines.com](https://db-engines.com) 称，MongoDB 是截至本文撰写时最流行的 NoSQL 数据库，也是整体排名第五位的数据库。

MongoDB 属于 NoSQL 数据库中的文档存储类别。Mongo 将数据存储在[二进制 JSON（BSON）格式文档](https://bsonspec.org)中。Mongo 原生使用 JSON，为 JavaScript 应用提供了简单便捷的接口。Mongo 的安装还附带了几种工具，如交互式 shell、数据导入导出实用程序以及统计报告应用程序。

## 在本地安装 MongoDB

MongoDB 可在多种平台上运行，包括 Windows、OS X 和大多数流行的 Unix 版本。所有平台的当前和先前版本都可以从 [Mongo 的下载页面](https://www.mongodb.com/download-center)下载。此页面上的二进制发行版是官方版本；不过，Mongo 也可以通过 [Homebrew 等包管理器安装](https://docs.mongodb.com/manual/administration/install-community/)。无论你选择如何安装 MongoDB，都应参考[适用于你特定平台的安装指南](https://docs.mongodb.com/manual/installation/)。

安装完成后，通过运行[清单 7-1](#listing-7-1) 中所示的命令来验证一切是否安装正确。`mongod` 是 MongoDB 使用的主要守护进程，此命令返回当前安装的版本。如果安装正确，你应该会看到类似于[清单 7-2](#listing-7-2) 中所示的输出。在这个特定示例中，安装的是 Mongo 2.6.3。

```
mongod -version
```

**清单 7-1.** 验证 MongoDB 是否已安装

```
db version v2.6.3
2014-07-27T13:57:07.359-0400 Salman幽思：幽思
git version: nogitversion
```

**清单 7-2.** 清单 7-1 的版本输出示例

## 云托管

许多公司会为你托管 MongoDB 实例。这省去了你自己设置和维护 Mongo 的麻烦。其中许多公司甚至会在你的数据库低于一定大小时免费托管，这使其成为原型设计的理想解决方案。与所有云服务一样，随着资源需求的增加，你需要支付越来越多的费用。通过将数据托管在云端，可以从世界任何地方轻松访问。

MongoDB 认可的云合作伙伴列表可在 [mongodb.com](http://mongodb.com) 上找到。本书后续示例中使用 [MongoLab](http://MongoLab) 作为 MongoDB 的云托管提供商。MongoLab 提供免费的沙盒环境，带有 0.5GB 的存储空间，对于本书中的示例来说绰绰有余。

### Heroku 集成

MongoLab 与 [Heroku](http://Heroku) 应用集成得非常容易，我们将在本书示例中使用 Heroku 进行 Node.js 应用的云托管。如果你计划跟随与 Heroku 相关的章节，请确保你[注册一个免费账户](http://sign up for a free account)并安装 [Heroku toolbelt](http://Heroku toolbelt)，这是一套用于与 Heroku 协作的命令行工具。

要将 MongoLab 添加到 Heroku 应用，请运行以下命令。这将创建访问 MongoLab 托管数据库所需的一切：

```
heroku addons:add mongolab
```

**清单 7-3.** 将 MongoLab 添加到 Heroku 应用的命令

此时，MongoLab 应该会显示为你的 Heroku 项目中的附加组件，如[图 7.1](http://Figure 7.1) 所示。点击 MongoLab 文字，你将进入一个类似于[图 7.2](http://Figure 7.2) 的页面。此页面包含有关应用数据库的信息，包括数据库名称、用户名、使用 Mongo shell 连接的命令，以及使用驱动程序连接的 URI。在此示例中，数据库名称和用户名均为 heroku_app21015781。在下一章中，你将学习如何使用提供的 URI 从 Node 应用访问数据库。

![](img/0ca996f5fd0375fc118091628c3c7a87_124_0.png)

图 7.1. MongoLab 与 Heroku 应用的集成

![](img/0ca996f5fd0375fc118091628c3c7a87_124_1.png)

图 7.2. 显示数据库信息的 MongoLab 页面

## MongoDB Shell

Mongo shell 程序 `mongo` 是 MongoDB 默认安装的命令行实用程序之一。如果你正在使用 MongoLab，可以使用[图 7.2](https://example.com) 中所示的 `mongo` 命令连接到你的数据库。如果你在本地运行 Mongo，则必须先启动 Mongo 守护进程 `mongod`，因为它接受来自 `mongo` 的传入连接。默认情况下，`mongo` 尝试连接到 localhost 上的 27017 端口，但可以使用 `--port` 和 `--host` 标志进行配置。假设你在本地运行，`mongo` 命令的输出如[清单 7-4](https://example.com) 所示。注意输出最后一行的 `>` 字符。这就是 `mongo` 命令提示符。

### 警告：权限已授予

你必须具有访问 Mongo 的 `/data/db` 目录的适当权限。如果遇到权限错误，你可能想查看[这个相关的 Stack Overflow 问题](https://example.com)。

```
$ mongo
MongoDB shell version: 2.6.3
connecting to: test
>
```

**清单 7-4.** 使用 mongo 连接 MongoDB

`mongo` 连接后，可以使用 `db` 命令查看当前数据库的名称，如[清单 7-5](https://example.com) 所示。在这种情况下，我们连接的是默认的 `test` 数据库：

```
> db
test
```

**清单 7-5.** db 命令显示当前数据库的名称

要切换到不同的数据库，请发出 `use` 命令，后跟要切换到的数据库名称。例如，要切换到 `presidents` 数据库，请发出[清单 7-6](https://example.com) 中所示的命令。即使 `presidents` 数据库尚未创建，此命令也会生效。你可以使用 `db` 命令验证更改是否正常工作。值得注意的是，Mongo 只有在添加数据后才会创建数据库：

```
> use presidents
switched to db presidents
```

**清单 7-6.** use 命令在数据库之间切换

要查看所有可用的数据库，请使用 `show dbs` 命令，如[清单 7-7](https://example.com) 所示。如果你一直在按顺序尝试这些示例，你会注意到 `presidents` 数据库不存在，因为没有添加数据。

```
> show dbs
admin   (empty)
local   0.078GB
```

**清单 7-7.** 使用 dbs 命令列出所有可用数据库



## 插入新数据

`db` 不仅仅是一个用于显示当前数据库名称的命令。它还是数据库的根对象，可用于操作数据。例如，假设我们想向总统数据库中添加比尔·克林顿。首先，执行 `use presidents` 命令切换到 presidents 数据库。接下来，执行清单 7-8 所示的命令来插入比尔·克林顿。此命令将对象 `{name: 'Bill Clinton'}` 添加到 presidents 数据库的 people 集合中。由于 presidents 数据库在技术上还不存在，Mongo 现在会创建它。Mongo 还很贴心地为我们创建了 people 集合。请注意，此操作返回的 `WriteResult` 通过 `nInserted` 字段验证了已在数据库中创建了一个对象。你还可以分别使用 `show dbs` 和 `show collections` 命令来验证 president 数据库和 people 集合现在是否存在。

```
> db.people.insert({name: 'Bill Clinton'})
WriteResult({ "nInserted" : 1 })
```

**清单 7-8.** 向 MongoDB 数据库添加数据

可以通过传入对象数组的方式，在一次 `insert()` 调用中添加多个项目。清单 7-9 展示了这方面的示例。请注意，生成的 `BulkWriteResult` 指定已插入两个对象：

```
> db.people.insert([{name: 'George H Bush'},
                     {name: 'George W Bush'}])
BulkWriteResult({
  "writeErrors" : [ ],
  "writeConcernErrors" : [ ],
  "nInserted" : 2,
  "nUpserted" : 0,
  "nMatched" : 0,
  "nModified" : 0,
  "nRemoved" : 0,
  "upserted" : [ ]
})
```

**清单 7-9.** 通过一次 `insert()` 调用添加多条数据

## 检索数据

既然数据已添加到我们的数据库中，我们需要某种方式将其读取回来。这是通过集合的 `find()` 方法实现的。回到我们的总统示例，清单 7-10 展示了如何一次检索所有总统。在这些结果中，值得指出的是 `_id` 字段。MongoDB 会为它存储的每个对象分配此字段。它是所涉及对象的唯一标识符：

```
> db.people.find()
{ "_id" : ObjectId("53d58ad9ec6dce1f6c577082"), "name" : "Bill Clinton" }
{ "_id" : ObjectId("53d58ee05a0f7ff4e38b8ba3"), "name" : "George H Bush" }
{ "_id" : ObjectId("53d58ee05a0f7ff4e38b8ba4"), "name" : "George W Bush" }
```

**清单 7-10.** 使用 `find()` 检索集合中的所有项目

这些结果不错，但在大多数情况下，你需要应用一些搜索条件，而不是返回集合中的每个项目。`find()` 支持此功能，允许传入 `criteria` 对象作为参数。清单 7-11 展示了如何搜索所有名为 Bill 的总统。在此示例中，搜索条件指定 `name` 字段必须匹配正则表达式 `/^Bill/`（以 Bill 开头的字符串）。查询运算符的完整列表可在 [Mongo 查询文档](https://docs.mongodb.com/manual/reference/operator/query/) 中找到。请注意，如果你想进行更精确的 Bill Clinton 查询，可以使用 `db.people.find({name: 'Bill Clinton'})`。

```
> db.people.find({name: {$regex: '^Bill'}})
{ "_id" : ObjectId("53d58ad9ec6dce1f6c577082"), "name" : "Bill Clinton" }
```

**清单 7-11.** 对 `find()` 应用搜索条件

## 限制结果集的大小

限制 `find()` 返回结果集大小的方法主要有两种。第一种方法是使用 `findOne()` 代替 `find()`。`findOne()` 的使用方式相同，但只返回单个匹配项。清单 7-12 展示了如何使用 `findOne()` 选择一位名为 George Bush 的总统：

```
> db.people.findOne({name: {$regex: '^George'}})
{ "_id" : ObjectId("53d58ee05a0f7ff4e38b8ba3"), "name" : "George H Bush" }
```

**清单 7-12.** 使用 `findOne()` 执行搜索

第二种方法是将 `limit()` 方法链接到 `find()` 方法。`limit()` 接受一个表示最大结果集大小的数字作为输入参数。清单 7-13 展示了如何使用 `limit()` 将结果集大小限制为两个：

```
> db.people.find().limit(2);
{ "_id" : ObjectId("53d5a5965a0f7ff4e38b8ba5"), "name" : "Bill Clinton" }
{ "_id" : ObjectId("53d5a59d5a0f7ff4e38b8ba6"), "name" : "George H Bush" }
```

**清单 7-13.** 使用 `limit()` 限制结果集大小

## 更新数据

数据是使用集合恰如其名的 `update()` 方法进行更新的。`update()` 将查询对象作为其第一个参数。此对象指定应更新哪些项目，并使用与 `find()` 相同的语法。`update()` 的第二个参数是另一个对象，用于指定值应如何更新。`update()` 支持第三个可选的对象参数。此对象支持以下属性：

- **upsert**：一个默认为 `false` 的布尔值。如果为 `true`，如果没有现有项目匹配查询条件，`update()` 将创建新文档。
- **multi**：一个默认为 `false` 的布尔值。如果设置为 `true`，`update()` 将修改所有匹配查询条件的文档。
- **writeConcern**：定义更新写入行为的文档。有关此参数的更多信息，请参阅 [写入关注文档](https://docs.mongodb.com/manual/reference/write-concern/)。

`update()` 的简单示例见清单 7-14。在此示例中，Bill Clinton 被重命名为 William Clinton。此更新还向文档添加了一个新的 `terms` 字段，用于指定担任总统的届数。这是 NoSQL 与关系数据库相比灵活性的一个例子。在运行时，NoSQL 数据库可以在单个数据上定义新字段。在关系数据库中，这将违反表的架构。请注意，结果表明一个文档已匹配并更新，而没有文档被 upsert：

```
> db.people.update({name: 'Bill Clinton'}, {$set: {name: 'William Clinton', terms: 2}})
WriteResult({ "nMatched" : 1, "nUpserted" : 0, "nModified" : 1 })
```

**清单 7-14.** 使用 `update()` 修改现有数据

## 删除数据

最后的 CRUD 操作是删除。数据是使用 `remove()` 方法从集合中删除的。`remove()` 将 `find()` 风格的查询对象作为其第一个参数。第二个可选的对象参数支持两个字段：`justOne` 和 `writeConcern`。如果 `justOne` 设置为 `true`，删除将仅限于单个文档。默认为 `false`，意味着删除所有匹配项。`writeConcern` 参数是一个文档，其行为与 `update()` 的 `writeConcern` 相同。

清单 7-15 中的示例展示了如何从集合中删除一位姓 Bush 的总统。请注意，尽管两位总统匹配搜索条件，但结果指定只删除了一个项目：

```
> db.people.remove({name: {$regex: 'Bush$'}}, {justOne: true})
WriteResult({ "nRemoved" : 1 })
```

**清单 7-15.** 使用 `remove()` 删除数据

如果你一直在跟着所有示例操作，执行 `find()` 后你的数据库现在应该如清单 7-16 所示。请注意，Bill Clinton 已被重命名，并添加了 `terms` 属性，而 George H Bush 已被删除：

```
> db.people.find()
{ "_id" : ObjectId("53d58ee05a0f7ff4e38b8ba4"), "name" : "George W Bush" }
{ "_id" : ObjectId("53d58ad9ec6dce1f6c577082"), "name" : "William Clinton", "terms" : 2 }
```

**清单 7-16.** 操作数据后 people 集合的状态

## 删除集合

可以使用集合的 `drop()` 方法从数据库中删除整个集合。清单 7-17 展示了如何删除 people 集合：

```
> db.people.drop()
true
```

**清单 7-17.** 使用 `drop()` 删除 people 集合

在清单 7-18 中，`show collections` 命令验证了该集合不再存在：

```
> show collections;
system.indexes
```

**清单 7-18.** 调用 `drop()` 后显示可用集合

## 删除数据库

可以使用 `dropDatabase()` 方法删除整个数据库及其所有底层数据。清单 7-19 展示了如何操作：

```
> db.dropDatabase()
{ "dropped" : "presidents", "ok" : 1 }
```

**清单 7-19.** 使用 `dropDatabase()` 删除数据库

应谨慎使用此操作。在执行 `dropDatabase()` 之前，应仔细检查你是否正在使用正确的数据库。



## 本章总结

本章介绍了 MongoDB 的基本概念。你已经学习了如何在本地及使用云托管服务来设置并启动 MongoDB，还了解了 mongo shell 支持的基本操作。若想更全面地深入了解 Mongo shell，我们建议你浏览[官方文档](https://docs.mongodb.com/manual/)。

下一章，你将学习如何在 Node.js 应用程序中使用 MongoDB。完成此任务主要使用两个模块：一个是 [MongoDB 原生驱动](https://github.com/mongodb/node-mongodb-native)，另一个是名为 Mongoose 的模块，它的抽象层级比原生驱动略高。

## 使用 Mongoose 与 MongoDB 交互

前一章涵盖了 MongoDB 的基础知识：它的定义、安装方法以及实用价值。我们假设你此时已经有一个正在运行的 MongoDB 实例。我们将使用我们创建的实例，但你应该自行创建一个，以便自由实验。如果你尚未创建，可以在 [MongoLab](http://MongoLab) 上免费创建一个 MongoDB 实例。

本章将深入讲解使用 MongoDB 的具体细节。如果你记得前面的章节，我们使用了术语 CRUD（创建、读取、更新、删除）。CRUD 操作覆盖了大多数计算机系统中大部分的数据交互。当你理解了 MongoDB 的基本 CRUD 功能后，你会惊讶于只需极少代码就能完成如此多的功能。

为了清晰起见，本章所有代码将集中在单个文件中。我们会持续在同一文件中添加和编辑代码，最终得到一个数据库初始化脚本，供本书后续使用。

## Mongoose Node 模块

在讨论模块时，我们提到大多数常见问题都已有现成的模块来解决；与 MongoDB 实例交互也不例外。用于数据库操作的标准 Node 模块是 [Mongoose](https://mongoosejs.com/)。在与 MongoDB 通信的 Node 服务器中，*不*使用 Mongoose 的情况极为罕见。虽然 Mongoose 是连接 MongoDB 实例的事实标准模块，但也存在其他选择。Node 有一个[原生驱动](https://www.npmjs.com/package/mongodb)，它是 Ruby 版本的移植。它比 Mongoose 更底层，因此在某些情况下性能可能更高。

出于易用性和社区采纳度的考虑，我们所有的示例都将使用 Mongoose 模块。

Mongoose 在直观且对 JavaScript 友好的接口中提供了所有 MongoDB 功能。它包含了 MongoDB 支持的所有查询功能调用，以及定义模式和从数据库实例化模型的方法。

本章中需要记住的一个重点是：MongoDB 是实际存储和检索数据的数据库，而 Mongoose 是封装与 MongoDB 实例交互的 Node 模块。

## 模式（Schemas）

使用 Mongoose，一切都从模式开始。模式映射到 MongoDB 的文档或集合，是创建模型的一组规则和指令。如果你有使用 MySQL 等传统关系型数据库的经验，可以将 Mongoose 模式看作表定义。

模式的核心本质上与其他 JavaScript 对象一样——都是键值对。键是属性名，值是 Mongoose 的 SchemaType。当从数据库检索文档时，Mongoose 会尝试将值转换为相关的 SchemaType，然后返回一个模型对象。可用的 SchemaType 包括：

- String
- Number
- Date
- Buffer
- Boolean
- Mixed
- ObjectId
- Array

如果内置的 SchemaType 不满足需求，你也可以声明自定义的 SchemaType。大多数 SchemaType 应该是不言自明的；它们大多直接映射到 JavaScript 的原生类型；但是，Mixed 和 ObjectId 值得进一步讨论。

## Mixed 模式类型

Mixed 模式类型本质上是一个通配符。任何值都可以与声明为 Mixed 的模式类型关联。然而，这种灵活性是有代价的：它难以维护。因为 Mongoose 没有可靠的方法来比较值的变化，所以每当值改变时，开发者有责任通知 Mongoose。除非你真的不确定某个特定键将用于什么数据，否则最好避免使用 Mixed。

## ObjectID 模式类型

值得重申的是，MongoDB 不是关系型数据库。它没有外键或多对多关系的概念。MongoDB 是一个存储文档（通常是 JSON 对象）的数据库。话虽如此，ObjectId 模式类型允许你在内存中存储 MongoDB 的唯一标识符。结合其他一些模式选项，这允许你从其他文档中引用子文档。

## 重要提示：Mongoose 不是 MySQL

> 当你第一次意识到可以像关系型数据库那样引用其他文档时，你可能会试图让 MongoDB 像 MySQL 一样工作。为了你自己的理智，请避免这样做。试图结合两种数据库的特性最终会让 MongoDB 的工作变得更加困难。你会花很多时间试图让 MongoDB 像 SQL 一样工作，而这是行不通的。

## Mongoose 模式示例

在接下来的 Mongoose 模式讨论中，我们将使用清单 8-1。我们将声明两个模式：一个用于团队（Team），一个用于员工（Employee）。

```
var mongoose = require('mongoose');
var Schema = mongoose.Schema;
var TeamSchema = new Schema({
    name: {
        type: String,
        required: true
    }
});

var EmployeeSchema = new Schema({
    name: {
        first: {
            type: String,
            required: true
        },
        last: {
            type: String,
            required: true
        }
    },
    team: {
        type: Schema.Types.ObjectId,
        ref: 'Team'
    },
    image: {
        type: String,
        default: 'images/user.png'
    },
    address: {
        lines: {
            type: [String]
        },
        postal: {
            type: String
        }
    }
});
```

### 清单 8-1. 一个基本的员工 Mongoose 模式

`Schema` 是一个构造函数，它接受一个描述我们模式的键值对对象。团队模式被定义为只存储团队的名称。

员工模式更有趣一些。每个员工文档都将有一个包含 `first` 和 `last` 键的 `name` 对象。这两个值都是必需的，并且必须是字符串。`team` 键是我们用来创建对其他文档/模式引用的方式。`Schema.Types.ObjectId` 表示 `team` 的值将是一个 MongoDB 的唯一标识符，而 `ref` 键则告知 Mongoose，当从数据库填充此值时应使用哪个模型。当我们接下来讨论模型时，这一点会变得更加清晰。

`image` 键表示值将是一个字符串；如果值缺失，将使用 `images/user.png`。`address` 由字符串数组 `lines` 和字符串 `postal` 组成。我们想要支持国际化，因此使用 `String` 比使用数字更好。

观察完成的模式，你会注意到它读起来非常清晰。一眼就能看清我们的文档在数据库中将如何组织。记住，模式告诉 Mongoose 数据将如何进出我们的数据库。假设我们将来想向 `address` 添加 `city`。对于像 MongoDB 这样的文档存储数据库，这只是一个简单的更改。我们只需在 `EmployeeSchema` 中添加 `city`，现在任何 `Employee` 文档都可以读写 `city` 了。

这只是 Mongoose 模式的冰山一角。利用 Mongoose 提供的各种选项，你可以构建非常高级和强大的模式。如需进一步阅读，请查阅 [Mongoose 官方文档页面的模式部分](https://mongoosejs.com/docs/guide.html)。

## Mongoose 模型

我们已经多次提到模型，现在让我们来研究一下模型是什么，以及我们



## 创建更多文档

我们可以使用它们。模型的实例代表 MongoDB 数据库中的文档。当你执行查询时，生成的文档会通过适当的模式（schema）进行处理，并返回一个准备就绪的模型（model）供使用。在使用 Mongoose 时，大多数情况下你都是与模型而非模式进行交互。

让我们更新清单 8-1，并向我们的数据库中插入几个团队：

```javascript
var db = mongoose.connection;
var dbUrl = 'mongodb://username:password@ds043917.mongolab.com:43917/humanresources';

var TeamSchema = new Schema({
  name: {
    type: String,
    required: true
  }
});
var Team = mongoose.model('Team', TeamSchema);

db.on('error', function () {
  console.log('there was an error communicating with the database');
});

mongoose.connect(dbUrl, function (err) {
  if (err) {
    return console.log('there was a problem connecting to the database!' + err);
  }

  console.log('connected!');
  var team = new Team({
    name: 'Product Development'
  });

  team.save(function (error, data) {
    if (error) {
      console.log(error);
    } else {
      console.dir(data);
    }

    db.close();
    process.exit();
  });
});
```

**清单 8-2.** 将一个团队写入数据库

在继续之前，请务必按照第 7 章的设置说明，使用 MongoLab 设置好一个 MongoDB 实例。清单 8-2 中的 `dbUrl` 仅为演示目的，需要将其更新为指向你自己的 MongoLab 数据库实例。

为了简洁起见并强调向数据库添加特定项，我们调整了部分原始代码的位置。我们建立与数据库的连接，然后为 `mongoose.database` 对象设置一些错误事件的监听器。在 `mongoose.connect` 的回调函数内部，我们实例化一个新的 `Team` 模型并赋值 `name` 键。

`var Team = mongoose.model('Team', TeamSchema);` 这行代码本质上告诉 Mongoose，任何时候我们想创建一个 `Team` 模型，它都必须遵循 `TeamSchema`。`mongoose.model()` 返回一个可以看作构造函数的函数。在 "open" 事件的回调函数中，我们使用 `Team` 构造函数创建一个团队的实例并设置 `name`。

假设数据库连接正确，你应该会看到类似 `{ __v: 0, name: 'Product Development', _id: 53c32948e385c35d71ad6797 }` 的内容输出到控制台。这意味着现在数据库中存储了一个名为 'Product Development' 的 `Team` 文档。你应该注意到保存操作结果中多出了两个键：`__v` 和 `_id`。`__v` 是 Mongoose 用于跟踪此模型所代表文档的版本和更改的内部键。`_id` 是 MongoDB 中为此文档自动生成的唯一标识符（`ObjectId`）。

我们的方案对于只需要一个团队来说是没问题的，但如果我们想连续添加三个或四个团队呢？让我们重构代码，用一个命令插入多个团队：

```javascript
mongoose.connect(dbUrl, function () {
  console.log('connected!');

  Team.create([{
    name: 'Product Development'
  }, {
    name: 'Dev Ops'
  }, {
    name: 'Accounting'
  }], function (error, pd, devops, acct) {
    if (error) {
      console.log(error);
    } else {
      console.dir(pd);
      console.dir(devops);
      console.dir(acct);

      db.close();
      process.exit();
    }
  });
});
```

**清单 8-3.** 向数据库插入多个团队

`Team.create` 允许我们用单个命令创建多个新文档。这比连续执行多次文档保存方便得多。值得注意的是，这只是一个便利方法，而非真正的批量插入。底层的 Mongoose 实现仍然会遍历每个元素并逐个插入。

现在，让我们为团队添加一些员工。我们当然*可以*分别将员工和团队相互添加，但回想一下我们的 `EmployeeSchema`：我们有一个 `team` 键，它存储的是 `Schema.Types.ObjectId` 值。虽然 MongoDB 没有外键的概念，但我们可以使用 Mongoose 通过单个查询从不同的集合中检索文档。

指定 `team` 键存储 `Schema.Types.ObjectId`，这代表 MongoDB 文档的主标识符。`EmployeeSchema` 中的 `ref` 键指示 Mongoose 在 `Team` 集合中查找一个文档，其唯一 ID（`_id`）值等于存储在 `team` 中的值。通过这种方式，我们可以模拟外键关系；然而，它与 SQL 外键不同。

传统的 SQL 数据库强制执行参照完整性，这意味着在两个表的键都存在且有效之前，无法在它们之间创建关系。在 MongoDB 中，没有参照完整性的概念，因为没有外键。因此，任何 `ObjectId` 值都可以存储在 `team` 键中，MongoDB 不会报错。同样的规则也适用于删除操作。如果所有 `Employee` 文档的 `team` 值都设置为与 Dev Ops 团队关联的 `_id`，那么 Dev Ops 团队可以随时被自由删除。将引用看作是查询快捷方式，而非 SQL 中传统的外键关系。

因为这个脚本随着多个回调函数变得越来越复杂，我们将进行一点重构，将每个步骤拆分成函数并逐个调用。记住，每个步骤都是异步的，所以我们应该计划将回调函数作为参数传递，这些参数会在数据库活动完成时被调用：

```javascript
var EmployeeSchema = new Schema({...});

var Employee = mongoose.model('Employee', EmployeeSchema);

function insertTeams (callback) {
  Team.create([{
    name: 'Product Development'
  }, {
    name: 'Dev Ops'
  }, {
    name: 'Accounting'
  }], function (error, pd, devops, acct) {
    if (error) {
      return callback(error);
    } else {
      console.info('teams successfully added')
      callback(null, pd, devops, acct);
    }
  });
}

function insertEmployees (pd, devops, acct, callback) {
  Employee.create([{
    name: {
      first: 'John',
      last: 'Adams'
    },
    team: pd._id,
    address: {
      lines: ['2 Lincoln Memorial Cir NW'],
      zip: 20037
    }
  }, {
    name: {
      first: 'Thomas',
      last: 'Jefferson'
    },
    team: devops._id,
    address: {
      lines: ['1600 Pennsylvania Avenue', 'White House'],
      zip: 20500
    }
  }, {
    name: {
      first: 'James',
      last: 'Madison'
    },
    team: acct._id,
    address: {
      lines: ['2 15th St NW', 'PO Box 8675309'],
      zip: 20007
    }
  }, {
    name: {
      first: 'James',
      last: 'Monroe'
    },
    team: acct._id,
    address: {
      lines: ['1850 West Basin Dr SW', 'Suite 210'],
      zip: 20242
    }
  }], function (error, johnadams) {
    if (error) {
      return callback(error);
    } else {
      console.info('employees successfully added');
      callback(null, {
        team: pd,
        employee: johnadams
      });
    }
  })
}

mongoose.connect(dbUrl, function (err) {
  if (err) {
    return console.log('there was a problem connecting to the database!' + err);
  }
  console.log('connected!');

  insertTeams(function (err, pd, devops, acct) {
    if (err) {
      return console.log(err)
    }
    insertEmployees(pd, devops, acct, function (err, result) {
      if (err) {
        console.error(err);
      } else {
        console.info('database activity complete')
      }

      db.close();
      process.exit();
    });
  });
});
```

**清单 8-4.** 插入员工

清单 8-4 与清单 8-3 看起来非常不同。我们创建了两个新函数：`insertTeams` 和 `insertEmployees`。在建立与数据库的连接后，我们希望调用 `insertTeams` 并传递一个回调函数。团队插入完成后，我们希望调用 `insertEmployees`，并传递 `insertTeams` 的结果以及一个回调函数给 `insertEmployees`。员工插入完成后，我们将执行最终的回调函数，将结果输出到控制台，关闭数据库连接并退出进程。我们将在下一步中用到 `result`。目前，可以将其视为一个数据存储，我们将在不同的函数中传递它，这些函数可以在数据库活动完成后更改。

## 简单查询

现在我们的数据库中已经有了一些数据，让我们编写一些简单的查询。一个常见的数据库查询是通过 ID 检索文档：

```javascript
function retrieveEmployee (data, callback) {
  Employee.findOne({
    _id: data.employee._id
  }).populate('team').exec(function (error, result) {
    if (error) {
      return callback (error);
    } else {
      console.log('*** Single Employee Result ***');
      console.dir(result);
      callback(null, data);
    }
  });
}

// ... (后续调用代码)
insertEmployees(pd, devops, acct, function (err, result) {
  retrieveEmployee(result, function (err, result) {
    if (err) {
      console.error(err);
    } else {
      // ... (后续处理)
    }
  });
});
```



 ```
console.info('database activity complete')
}
 
db.close();
process.exit();
});
});
```

## 清单 8-5. 检索单个员工

`retrieveEmployee` 函数使用了附加在 Employee 模型上的 `findOne`、`populate` 和 `exec` 函数。`findOne` 接受一个键值对作为参数。这里的逻辑表示我们希望返回一个 `_id` 等于 `data.employee._id` 的 Employee 文档。`populate` 函数可以接收多个参数，但出于我们的目的，我们只需要提供 `team`，因为这是我们想要填充的附加文档。这就是 EmployeeSchema 中的 `team` 键发挥作用的地方。最后，`exec` 对数据库运行查询。

运行此代码后，你应该会看到 "John Adams" 文档被输出到控制台。请注意，`team` 键已被填充了一个完整的 Team 文档。

假设我们想要找到数据库中所有名字以 "J" 开头的员工。让我们添加另一个函数，返回符合此条件的所有员工：

```
function retrieveEmployees (data, callback) {
  Employee.find({
    'name.first': /J/i
  }, function (error, results) {
    if (error) {
      return callback(error);
    } else {
      console.log('*** Multiple Employees Result ***')
      console.dir(results);
      callback(null, data);
    }
  });
}
[...]
retrieveEmployee(result, function (err, result) {
 
  retrieveEmployees(result, function (err, result) {
    if (err) {
      console.error(err);
    } else {
      console.info('database activity complete')
    }
 
    db.close();
    process.exit();
  });
});
```

## 清单 8-6. 按姓名检索员工

`Employee.find` 方法可以接收几个不同的参数；它是数据库查询的主要入口点。在这个例子中，我们表示希望从数据库中获取所有名字以 "J" 开头的 Employee 文档，并且搜索应该是大小写不敏感的。当 `retrieveEmployees` 在我们的 `async.waterfall` 中执行时，名字以 "j" 开头的员工现在应该被记录到控制台。

## 更新

哎呀！我们将一名员工的姓名设为了 "John Adams"，但我们原本想写的是 "Andrew Jackson"。让我们编写一个基本函数来更新该员工。回到 `insertEmployees` 函数中，我们开始将一个 `data` 对象传递给后续的水线函数。该 `data` 对象附加了一个员工和一个团队；让我们在我们的更新函数中使用它：

```
function updateEmployee (first, last, data, callback) {
    console.log('*** Changing names ***');
    console.dir(data.employee);
 
    var employee = data.employee;
    employee.name.first = first;
    employee.name.last = last
 
    employee.save(function (error, result) {
        if (error) {
            return callback(error);
        } else {
            console.log('*** Changed name to Andrew Jackson ***');
            console.log(result);
            callback(null, data);
        }
    });
}
[...]
retrieveEmployees(result, function (err, result) {
 
    updateEmployee(result, function (err, result) {
        if (err) {
            console.error(err);
        } else {
            console.info('database activity complete')
        }
 
        db.close();
        process.exit();
    });
});
```

**清单 8-7. 更新员工**

`data.employee` 仍然是从 `insertEmployees` 中获取的 `Employee` 模型。在 `updateEmployee` 内部，我们更改了 `name.first` 和 `name.last` 的值，然后调用 `save`。当你看到我们记录的结果时，会发现数据库中的数据已经发生了变化。

# 小结

不可能在几页纸中涵盖一个新数据库的每个方面。我们希望本书的这一部分能作为进一步学习和实验的入门和跳板，并鼓励你自己去查看 [MongoDB](http://mongodb.org/) 和 [Mongoose](http://mongoosejs.com/)。

我们在本示例中遗漏的一项任务是从数据库中删除文档。在开始填充新数据库之前，清理掉任何旧的或错误的数据是一种良好的实践。我们鼓励你在开始插入任何数据之前，编写两个函数来删除数据库中的所有员工和团队。

# 第 9 章

## 在示例应用中使用 MongoDB 和 Mongoose

在[第 6 章](Chapter 6)中，我们开始构建示例人力资源应用程序。当时，Node 不幸是唯一已经介绍过的技术，因此第 6 章中的应用程序仅由一个 Node HTTP 服务器组成，该服务器从 JSON 文件返回硬编码的员工数据。现在我们对 MongoDB 和 Mongoose 模块有了充分的了解，可以更新示例应用程序以使用数据库。

本章将在第 6 章的服务器基础上构建。我们假设你已经在本地计算机上拥有示例应用程序代码。我们还假设你已经运行了 `npm install`，并且能够成功使用浏览器连接到服务器。例如，你应该能够通过访问 URL [http://127.0.0.1:1337/employees](http://127.0.0.1:1337/employees) 查看 [图 9.1](Figure 9.1) 中显示的员工列表。

```
[
  {
    "id": "1000003",
    "name": {
      "first": "Colin",
      "last": "Ihrig"
    },
    "address": {
      "lines": [
        "11 Wall Street"
      ],
      "city": "New York",
      "state": "NY",
      "zip": 10118
    }
  },
  {
    "id": "1000021",
    "name": {
      "first": "Adam",
      "last": "Bretz"
    },
    "address": {
      "lines": [
        "46 18th St",
        "St. 210"
      ],
      "city": "Pittsburgh",
      "state": "PA",
      "zip": 15222
    }
  },
  ...
]
```

图 9.1. 示例应用的输出数据

## 添加 Mongoose 模型

我们将从创建两个用于与 MongoDB 实例交互的 Mongoose 模型开始。第一步是使用[清单 9-1](#listing-9-1)中所示的命令安装 mongoose 模块，并将其保存到项目的 package.json 中：

```
npm install --save mongoose
```

**清单 9-1.** 安装 mongoose 并将其添加到 package.json

完成后，在应用程序的根目录下创建一个名为 `models` 的目录。这是我们将保存模型文件的位置。在 `models` 目录内，添加两个文件：`employee.js` 和 `team.js`。顾名思义，`employee.js` 将存储与员工数据相关的模型。我们还将引入员工团队的概念，这将存储在 `team.js` 中。

### 员工模型

员工模型的代码如[清单 9-2](#listing-9-2)所示。导入 mongoose 模型后，创建了一个新的模式。根据此模式，每位员工具有：

- 一个 `id`（与 Mongo 的 `_id` 属性分开），作为主键
- 一个 `name` 对象
- 一个 `address`
- 一个 `team` 指定
- 一个 `profile picture`

`team` 只是对 `Team` 模型实例的引用，我们很快就会创建它。在[清单 9-2](#listing-9-2)的最后一行，从模式创建了一个模型并导出：

```
var mongoose = require('mongoose');
var Schema = mongoose.Schema;
var EmployeeSchema = new Schema({
  id: {
    type: String,
    required: true,
    unique: true
  },
  name: {
    first: {
      type: String,
      required: true
    },
    last: {
      type: String,
      required: true
    }
  },
```

```
team: {
    type: Schema.Types.ObjectId,
    ref: "Team"
},
image: {
    type: String,
    default: 'images/user.png'
},
address: {
    lines: {
        type: [String]
    },
    city: {
        type: String
    },
    state: {
        type: String
    },
    zip: {
        type: Number
    }
}
});

module.exports = mongoose.model('Employee', EmployeeSchema);
```

## 清单 9-2. Mongoose 员工模型

存储在 image 中的头像图片只是一个表示图片文件 URL 的字符串。如果未指定头像图片，使用[图 9.2](Figure 9.2) 中显示的默认图片。目前，你可以忽略头像图片。我们将在第 13 章中重新讨论这个问题，届时我们会将 Express 集成到我们的示例应用中。



图 9.2. 默认头像

## 团队模型

在大多数公司中，员工以团队形式工作。为了实现这一需求，我们将团队的概念引入到应用程序中。团队模型的代码如[清单 9-4](#)所示。注意，这段代码使用了 mongoose-post-find 和 async 模块。需要通过以下命令安装它们：

```
npm install --save async mongoose-post-find
```

**清单 9-3.** 安装并保存 async 和 mongoose-post-find

Team 模式很简单，只包含一个团队名称和一个团队成员数组。有趣的代码围绕 `TeamSchema.plugin()` 调用展开。`plugin()` 允许 Mongoose 模式利用插件来扩展内置功能。这里集成了 mongoose-post-find，以启用 `find()` 和 `findOne()` 的后置钩子。这些钩子是在调用 `find()` 和 `findOne()` 时运行的函数，能够在返回结果给调用函数之前修改结果。这些钩子会更新 Employee 文档，将它们分配到正确的团队中。

```
var mongoose = require('mongoose');
var postFind = require('mongoose-post-find');
var async = require('async');
var Schema = mongoose.Schema;

var TeamSchema = new Schema({
    name: {
        type: String,
        required: true
    },
    members: {
        type: [Schema.Types.Mixed]
    }
});

function _attachMembers (Employee, result, callback) {
    Employee.find({
        team: result._id
    }, function (error, employees) {
        if (error) {
            return callback(error);
        }

        result.members = employees;
        callback(null, result);
    });
}

// listen for find and findOne
TeamSchema.plugin(postFind, {
    find: function (result, callback) {
        var Employee = mongoose.model('Employee');

        async.each(result, function (item, callback) {
            _attachMembers(Employee, item, callback);
        }, function (error) {
            if (error) {
                return callback(error);
            }

            callback(null, result)
        });
    },
    findOne: function (result, callback) {
        var Employee = mongoose.model('Employee');

        _attachMembers(Employee, result, callback);
    }
});

module.exports = mongoose.model('Team', TeamSchema);
```

**清单 9-4.** Mongoose 团队模型

## 填充数据库

现在模型已经准备就绪，我们可以填充数据库了。首先，删除数据库目录，因为我们将不再需要硬编码的 JSON 数据库。接下来，在 lib 目录中创建一个名为 connection.js 的文件。这个文件如[清单 9-5](#)所示，将建立数据库连接并注册我们的 Mongoose 模型。我们还添加了一个 SIGINT 处理程序，当用户按下 Control+C 时，它会关闭 Mongo 连接和 Node 进程：

```
var mongoose = require('mongoose');
var dbUrl = 'mongodb://your_mongo_connection_url';

mongoose.connect(dbUrl);

// Close the Mongoose connection on Control+C
process.on('SIGINT', function() {
  mongoose.connection.close(function () {
    console.log('Mongoose default connection disconnected');
    process.exit(0);
  });
});

require('../models/employee');
require('../models/team');
```

**清单 9-5.** MongoDB 连接代码

接下来，我们将创建一个脚本，用于向数据库填充一组数据。在项目根目录下创建一个名为 bin 的目录，在其中创建一个名为 populate_db.js 的文件。该文件的内容如[清单 9-6](#)所示。这个脚本相当长，但好在相对简单。

我们将使用 async 模块来执行一系列异步数据库操作，避免陷入回调地狱——参见脚本末尾附近的 `async.series()` 调用。我们首先删除所有现有的 Employee 和 Team 文档，确保从干净的状态开始。

接下来，我们使用 data 变量中存储的员工和团队信息来填充数据库。最后一步是将员工添加到团队中。这在 updateEmployeeTeams() 函数中完成。为了简单起见，我们将所有人添加到同一个团队。完成后，我们关闭数据库连接并退出。

```
var async = require('async');
var mongoose = require('mongoose');
require(process.cwd() + '/lib/connection');
var Employee = mongoose.model('Employee');
var Team = mongoose.model('Team');

var data = {
  employees: [
    {
      id: '1000003',
      name: {
        first: 'Colin',
        last: 'Ihrig'
      },
      image: 'images/employees/1000003.png',
      address: {
        lines: ['11 Wall Street'],
        city: 'New York',
        state: 'NY',
        zip: 10118
      }
    },
    {
      id: '1000021',
      name: {
        first: 'Adam',
        last: 'Bretz'
      },
      address: {
        lines: ['46 18th St', 'St. 210'],
        city: 'Pittsburgh',
        state: 'PA',
        zip: 15222
      }
    },
    {
      id: '1000022',
      name: {
        first: 'Matt',
        last: 'Liegey'
      },
      address: {
        lines: ['2 S Market Square', '(Market Square)'],
        city: 'Pittsburgh',
        state: 'PA',
        zip: 15222
      }
    },
    {
      id: '1000025',
      name: {
        first: 'Aleksey',
        last: 'Smolenchuk'
      },
      image: 'images/employees/1000025.png' /* invalid image */,
      address: {
        lines: ['3803 Forbes Ave'],
        city: 'Pittsburgh',
        state: 'PA',
        zip: 15213
      }
    },
    {
      id: '1000030',
      name: {
        first: 'Sarah',
        last: 'Gay'
      },
      address: {
        lines: ['8651 University Blvd'],
        city: 'Pittsburgh',
        state: 'PA',
        zip: 15108
      }
    },
    {
      id: '1000031',
      name: {
        first: 'Dave',
        last: 'Beshero'
      },
      address: {
        lines: ['1539 Washington Rd'],
        city: 'Mt Lebanon',
        state: 'PA',
        zip: 15228
      }
    }
  ],
  teams: [
    {
      name: 'Software and Services Group'
    },
    {
      name: 'Project Development'
    }
  ]
};
```

```
var deleteEmployees = function(callback) {
  console.info('Deleting employees');
  Employee.remove({}, function(error, response) {
    if (error) {
      console.error('Error deleting employees: ' + error);
    }

    console.info('Done deleting employees');
    callback();
  });
};
```

```
var addEmployees = function(callback) {
  console.info('Adding employees');
  Employee.create(data.employees, function (error) {
    if (error) {
      console.error('Error: ' + error);
    }

    console.info('Done adding employees');
    callback();
  });
};
```

```
var deleteTeams = function(callback) {
  console.info('Deleting teams');
  Team.remove({}, function(error, response) {
    if (error) {
      console.error('Error deleting teams: ' + error);
    }

    console.info('Done deleting teams');
    callback();
  });
};

var addTeams = function(callback) {
  console.info('Adding teams');
  Team.create(data.teams,егрупп function (error, team1) {
    if (error) {
      console.error('Error: ' + error);
    } else {
      data.team_id = team1._id;
    }

    console.info('Done adding teams');
    callback();
  });
};

var updateEmployeeTeams = function (callback) {
  console.info('Updating employee teams');
  var team = data.teams[0];

  // Set everyone to be on the same team to start
  Employee.update({}, {
    team: data.team_id
  }, {
    multi: true
  }, function (error, numberAffected, response) {
    if (error) {
      console.error('Error updating employe team: ' + error);
    }

    console.info('Done updating employee teams');
    callback();
  });
};

async.series([
  deleteEmployees,
  deleteTeams,
  addEmployees,
  addTeams,
  updateEmployeeTeams
], function(error, results) {
  if (error) {
    console.error('Error: ' + error);
  }

  mongoose.connection.close();
  console.log('Done!');
});
```

**清单 9-6.** 用于填充数据库的脚本

你可以使用清单 9-7 中所示的命令来运行这个脚本。它足够简单，但我们还可以更进一步。更新 package.json 文件中的 `scripts` 条目，如清单 9-8 所示。注意，如果 `scripts` 中有其他条目，你应该注意避免覆盖它们。这样就可以使用 `npm run populate` 命令来运行 `populate_db.js`。

```
node bin/populate_db.js
```

**清单 9-7.** 用于运行 populate_db.js 脚本的命令

```
"scripts": {
  "populate": "node ./bin/populate_db"
}
```

**清单 9-8.** 将 `populate_db.js` 脚本添加到 package.json 中



## 访问数据库

至少运行一次 `npm run populate` 后，数据库就应该准备好供我们的应用程序使用了。接下来，我们将更新应用程序代码以使用数据库。用 [Listing 9-9](https://link-placeholder) 中所示的代码替换 `lib/employees.js` 的内容。我们保持了现有的模块接口不变，但使用 Mongoose 来检索数据，而非硬编码的 JSON：

```
var mongoose = require('mongoose');
var Employee = mongoose.model('Employee');

exports.getEmployees = getEmployees;
exports.getEmployee = getEmployee;

function getEmployees (callback) {
  Employee.find().sort('name.last').exec(callback);
}

function getEmployee (employeeId, callback) {
  Employee.findOne({
    id: employeeId
  }).populate('team').exec(callback);
}
```

**Listing 9-9.** 员工路由处理程序

请注意，我们在两个函数中都使用了 `sort()` 方法对结果进行排序。`sort()` 按一个或多个字段升序排序，除非字段名以 "-" 为前缀。`sort()` 也可以接受一个对象作为参数。有关用法的更多详细信息，请参阅文档。

最后一步是更新 `index.js`，为我们的应用程序建立数据库连接。这是一个简单的一行代码更改。在包含 `var colors = require('colors');` 的行之后，在 `index.js` 的第三行添加 [Listing 9-10](https://link-placeholder) 中所示的代码：

```
require('./lib/connection');
```

**Listing 9-10.** 在 `index.js` 中建立数据库连接

我们的应用程序应已完全配置好以与 Mongo 协同工作。现在，当您访问 [http://127.0.0.1:1337/employees](http://127.0.0.1:1337/employees) 时，您应该会看到一个包含 Mongo `_id` 属性的响应，如 [Figure 9.3](https://link-placeholder) 所示。

```
{
  "__v": 0,
  "_id": "53fa2ec5db067f00007e950b",
  "id": "1000003",
  "team": "53fa2ec5db067f00007e9511",
  "address": {
    "city": "New York",
    "state": "NY",
    "zip": 10118,
    "lines": [
      "11 Wall Street"
    ]
  },
  "image": "images/employees/1000003.png",
  "name": {
    "first": "Colin",
    "last": "Ihrig"
  }
},
```

Figure 9.3. MongoDB 示例应用程序中的示例数据

# 总结

本章继续开发我们的人力资源示例应用程序。在本章中，我们用 Mongoose 实现替换了一个硬编码的 JSON 数据库，该实现访问 MongoDB 后端。下次我们重新审视示例应用程序时，我们将从 Node 的核心 `http` 模块过渡到功能更强大的 Express 框架。然而，在深入探讨 Express 之前，[Chapter 10](Chapter 10) 将探索 SQL 数据库作为 MongoDB 的替代方案。

## MongoDB 的替代方案

MongoDB 是一项出色的技术，但当涉及到为应用程序添加数据存储时，它远非唯一的选择。有许多 NoSQL 替代方案，例如 [Redis](https://redis.io/)、[CouchDB](http://couchdb.apache.org/) 和 [Cassandra](http://cassandra.apache.org/)。或者，您也可以转向关系数据库管理系统，如 [MySQL](https://www.mysql.com/)、[Oracle](https://www.oracle.com/database/) 或 [SQL Server](https://www.microsoft.com/en-us/sql-server)。使用关系数据库将要求您了解 SQL，但掌握 SQL 基础知识相对容易。本章将 MySQL 探索为 MongoDB 的免费关系型替代方案。从技术上讲，这偏离了 MEAN 技术栈，但我们非常重视探索流行且可行的替代方案。

## 关系数据库与 SQL

尽管 NoSQL 替代方案兴起，关系数据库仍然非常受欢迎。根据 [db-engines.com 排名](https://db-engines.com/rankings)，最受欢迎的四个数据库——Oracle、MySQL、SQL Server 和 [PostgreSQL](https://www.postgresql.org/)——都是关系数据库。因此，如果本书忽略关系数据库，那将对我们的读者造成巨大的损害。许多人——包括本书的作者——实际上更喜欢关系数据库，因为 SQL 的简单性、有保证的数据一致性以及对数据连接的广泛支持。

在关系数据库中，数据存储在一组表中。表可以看作是数据的二维网格。网格中的列是每个表条目都必须具有的字段，代表表的模式。表中的行，称为记录或 **元组**，是必须符合模式的数据值。

一个示例表是使用 [Listing 10-1](#listing-10-1) 中所示的 SQL `CREATE` 命令创建的。此命令创建一个名为 `Presidents` 的表。此表中的所有记录都必须包含 `Id`、`Name` 和 `Terms` 字段，以符合定义的模式。`Id` 字段是一个无符号整数，不能为空，每次添加新记录时其值自动递增 1。`AUTO_INCREMENT` 属性使得 `Id` 字段非常适合作为**主键**。**主键**是一个或多个字段，用于唯一标识表中的记录。表中的其他字段用于存储总统的姓名和任期数。

```
CREATE TABLE Presidents (
    Id INT UNSIGNED NOT NULL AUTO_INCREMENT,
    Name VARCHAR(100) NOT NULL,
    Terms INT UNSIGNED NOT NULL,
    PRIMARY KEY(Id)
);
```

**Listing 10-1.** 创建 `Presidents` 表的 SQL 命令

> ### 注意：使用在线 SQL 沙盒尝试这些示例
>
> 作为在机器上安装 MySQL 的替代方案，您可以使用在线 SQL 沙盒，例如 [SQL Fiddle](http://sqlfiddle.com/)。Heroku 和其他 PaaS 提供商也提供便捷的 MySQL 数据库云托管。我们使用的是 Heroku 的 ClearDB MySQL Database 插件，可以使用命令 `heroku addons:add cleardb` 轻松添加到您的应用程序中。

下一步是用数据填充 `Presidents` 表。在 SQL 中，这是使用 `INSERT` 命令完成的。[Listing 10-2](#listing-10-2) 显示了一个示例 `INSERT` 命令，向 `Presidents` 表添加了两条记录。命令的 `(Name, Terms)` 部分列出了字段名称及其在 `VALUES` 部分中的预期顺序。正如您可能预期的，`VALUES` 部分提供了要插入的数据。注意，提供了姓名和任期数，但没有提供 `Id` 字段。这就是在创建表时使用的 `AUTO_INCREMENT` 标志非常方便的地方。

```
INSERT INTO Presidents (Name, Terms) VALUES
    ('Bill Clinton', 2),
    ('George W Bush', 2);
```

**Listing 10-2.** 向 Presidents 表插入值的 SQL 命令

要从关系数据库检索数据，请使用 SQL SELECT 命令。此命令最简单的形式，如 [Listing 10-3](https://example.com) 所示，从 Presidents 表中检索所有内容。此命令的结果如 [Table 10.1](https://example.com) 所示。

```
SELECT * FROM Presidents;
```

**Listing 10-3.** 从 Presidents 表检索值的 SQL 命令

## Table 10.1. 插入数据后的 Presidents 表

| ID | Name | Terms |
|---|---|---|
| 1 | Bill Clinton | 2 |
| 2 | George W Bush | 2 |

SELECT 命令支持多种选项。例如，假设我们只想选择名字为 Bill 的总统的姓名和任期数。Listing 10-4 显示了完成此操作的 SQL 命令。请注意，该命令明确请求 Name 和 Terms 字段，而不是 * 通配符。此命令还使用 WHERE 子句仅选择 Name 字段匹配正则表达式 `Bill %` 的记录。SQL 使用 % 字符作为通配符。用更熟悉的语法表示，此正则表达式应为 `/Bill .*/`。此查询的结果如 [Table 10.2](https://example.com) 所示。有关支持的 SELECT 选项的完整概述，请参阅 [MySQL SELECT 文档](https://example.com)。

```
SELECT Name, Terms FROM Presidents WHERE Name LIKE 'Bill %';
```

**Listing 10-4.** 检索名为 Bill 的总统的 SQL 命令

## Table 10.2. 选择名字为 Bill 的总统

| ID | Name | Terms |
|---|---|---|
| 1 | Bill Clinton | 2 |

SQL UPDATE 命令用于修改现有记录。一个基本的更新示例如 [Listing 10-5](https://example.com) 所示，该命令将 George W Bush 总统重命名为他父亲的名字。

```
UPDATE Presidents SET Name = 'George H Bush' WHERE Name = 'George W Bush';
```

**Listing 10-5.** 示例 SQL UPDATE 命令

要涵盖的最后一个 CRUD 操作是删除。要从表中删除记录，请使用 DELETE 命令。此命令最简单的形式如 [Listing 10-6](https://example.com) 所示，会删除表中的所有记录：

```
DELETE FROM Presidents;
```

**Listing 10-6.** 从 Presidents 表中删除所有记录

你也可以使用类似 SELECT 的从句来更有选择性地删除记录。例如，要删除所有姓 Bush 的总统，可以使用 [清单 10-7](#listing-10-7) 中所示的命令：

```
DELETE FROM Presidents WHERE Name LIKE '% Bush';
```

**清单 10-7.** 删除所有姓 Bush 的总统

要删除表本身，可以使用 DROP 命令，如 [清单 10-8](#listing-10-8) 所示。这个命令唯一的问题是，如果由于某种原因表不存在，会导致错误。为了解决这个问题，可以在命令中加入 IF EXISTS，如 [清单 10-9](#listing-10-9) 所示。

```
DROP TABLE Presidents;
```

**清单 10-8.** DROP TABLE 命令示例。

```
DROP TABLE IF EXISTS Presidents;
```

**清单 10-9.** 使用 IF EXISTS 的 DROP TABLE 命令

## mysql 模块

既然我们已经涵盖了关系数据库和 SQL 的基础知识，现在是时候看看如何从 Node 应用程序访问 MySQL 了。MySQL 没有内置支持，但 mysql 模块非常流行。事实上，它甚至在被 MySQL 官方文档中引用。要安装 mysql 模块，请使用 清单 10-10 中所示的命令：

```
npm install mysql
```

**清单 10-10.** 安装 mysql 模块

## 连接到数据库

使用 MySQL 的第一步是建立连接。至此，你应该已经安装了 MySQL，或者配置了云托管。接下来，使用 清单 10-11 中所示的代码连接到你的数据库。这里有几个要点需要注意。首先，导入 mysql 模块，然后使用 `createConnection()` 方法创建连接对象。传递给 `createConnection()` 的连接字符串包括用户名和密码（如果需要）、主机和端口，以及数据库名称。这些都会根据你的设置而有所不同。

调用 `createConnection()` 后，你必须再调用连接的 `connect()` 方法。这个方法是异步的，其回调函数接受一个可能的错误条件作为参数。如果一切设置正确，错误参数不会被设置，你应该已经成功连接到你的数据库。

```
var mysql = require('mysql');
var connection = 
mysql.createConnection('mysql://user:secret@localhost:3306/dbname');

connection.connect(function(error) {
  if (error) {
    return console.error(error.message);
  }

  console.log('successfully connected!');
});
```

**清单 10-11.** 连接到 MySQL 数据库

值得指出的是，`createConnection()` 也接受对象参数，而不是连接字符串。例如，可以使用 [清单 10-12](#) 中所示的调用来建立相同的连接：

```
var mysql = require('mysql');
var connection = mysql.createConnection({
  host: 'localhost',
  port: 3306,
  user: 'user',
  password: 'secret',
  database: 'dbname'
});
```

**清单 10-12.** 使用对象而不是连接字符串调用 createConnection()

## 连接池

在生产服务器中，每次应用程序需要访问数据库时都建立新连接是低效的。或者，你可以创建一组连接，由所有传入请求共享。每次应用程序需要连接数据库时，它可以从连接池中请求连接。如果没有可用的连接，请求将被放入队列。一旦有连接可用，它就会被分配来执行某些工作。一旦工作完成，连接就会返回到连接池以供将来使用。

创建连接池与创建单个连接非常相似。[清单 10-13](Listing 10-13) 中显示了创建连接池的示例。连接池是使用 `createPool()` 方法创建的，这与 `createConnection()` 非常相似；但是，它接受几个额外的参数：`connectionLimit`、`queueLimit` 和 `waitForConnections`。`connectionLimit` 设置连接池的最大大小，默认值为 10。`queueLimit` 设置连接后备队列的最大大小，默认为无限制。`waitForConnections` 是一个布尔值，默认为 `true`。如果 `waitForConnections` 为 `true`，如果没有可用的连接，请求将被添加到队列中。否则，回调将立即被调用并返回错误。

```
var mysql = require('mysql');
var pool = mysql.createPool({
  host: 'localhost',
  user: 'username',
  password: 'secret',
  database: 'dbname',
  connectionLimit: 20,
  queueLimit: 100,
  waitForConnections: true
});

pool.getConnection(function(error, connection) {
  if (error) {
    return console.error(error.message);
  }

  console.log('successfully obtained connection!');
});
```

**清单 10-13.** 创建连接池

请注意，不会调用连接的 `connect()` 方法。相反，使用连接池的 `getConnection()` 方法来获取连接。作为回调的第二个参数传递的连接将已经处于连接状态，这意味着无需调用 `connect()`。

这个例子中最后值得一提的点是，代码不会自行终止。因为已经建立了一组开放的连接，程序无法自行退出。相反，你可以使用 **Control-c** 来终止程序。如果你对这种行为感到困扰，可以使用 `process.exit(0)` 强制程序退出。

## 关闭连接

非池化连接使用 `end()` 和 `destroy()` 方法关闭。`end()` 优雅地关闭连接，这意味着允许任何排队的查询执行。另一方面，`destroy()` 立即关闭底层套接字，终止当前正在进行的任何操作。

池化连接使用 `release()` 和 `destroy()` 方法关闭。`release()` 将连接返回到连接池，而 `destroy()` 关闭连接并将其从连接池中移除。如果连接被销毁，连接池将会替换它。清单 10-14 显示了 清单 10-13 的更新版本，它尽职尽责地将连接释放回连接池：

```
var mysql = require('mysql');
var pool = mysql.createPool({
  host: 'localhost',
  user: 'username',
  password: 'secret',
  database: 'dbname'
});

pool.getConnection(function(error, connection) {
  if (error) {
    return console.error(error.message);
  }

  console.log('successfully obtained connection!');
  connection.release();
});
```

**清单 10-14.** 释放池化连接

## 执行查询

连接对象的 `query()` 方法用于向 MySQL 发送 SQL 命令。`query()` 接受两个参数。第一个是 SQL 字符串，第二个是回调函数，该回调函数接受错误和结果对象作为参数。[清单 10-15](about:blank) 显示了使用 `query()` 方法创建熟悉的 Presidents 表的示例：

```
var mysql = require('mysql');
var pool = mysql.createPool({
  host: 'localhost',
  user: 'username',
  password: 'secret',
  database: 'dbname'
});

pool.getConnection(function(error, connection) {
  if (error) {
    return console.error(error.message);
  }

  var sql = 'CREATE TABLE Presidents (' +
            'Id INT UNSIGNED NOT NULL AUTO_INCREMENT,' +
            'Name VARCHAR(100) NOT NULL,' +
            'Terms INT UNSIGNED NOT NULL,' +
            'PRIMARY KEY(Id))';

  connection.query(sql, function(error, results) {
    connection.release();

    if (error) {
      return console.error(error.message);
    }

    console.log('successfully created table!');
  });
});
```

**清单 10-15.** 使用 query() 方法创建 Presidents 表

[清单 10-16](about:blank) 中显示了更完整的示例。它使用了 清单 10-15 中创建的 Presidents 表，因此请确保该表首先存在。[清单 10-16](about:blank) 中的示例将数据插入表中，使用 SELECT 命令读取数据，然后删除表：

```
var mysql = require('mysql');
var pool = mysql.createPool({
  host: 'localhost',
  user: 'username',
  password: 'secret',
  database: 'dbname'
});

pool.getConnection(function(error, connection) {
  if (error) {
    return console.error(error.message);
  }
```

var insertSql = 'INSERT INTO Presidents (Name, Terms) VALUES' +
'(\'Bill Clinton\', 2),' +
'(\'George W Bush\', 2)';

connection.query(insertSql, function(error, results) {
  if (error) {
    connection.release();
    return console.error(error.message);
  }

  var selectSql = 'SELECT * FROM Presidents';

  connection.query(selectSql, function(error, results) {
    if (error) {
      connection.release();
      return console.error(error.message);
    }

    console.log('results of SELECT:');
    console.log(JSON.stringify(results, null, 2));

    var dropSql = 'DROP TABLE IF EXISTS Presidents';

    connection.query(dropSql, function(error, results) {
      connection.release();

      if (error) {
        return console.error(error.message)
      }

      console.log('table dropped!');
    });
  });
});
```

**代码清单 10-16.** 插入数据、读回数据，然后删除表

代码清单 10-16 的输出结果如下面的代码清单 10-17 所示。请注意，SELECT 查询的结果是以对象数组的形式返回的。虽然在此示例中未展示，但检查非 SELECT 查询的输出是很有价值的，因为它们通常包含有用信息，例如受影响的行数。

```
$ node mysql-exercise.js
results of SELECT:
[
  {
    "Id": 1,
    "Name": "Bill Clinton",
    "Terms": 2
  },
  {
    "Id": 2,
    "Name": "George W Bush",
    "Terms": 2
  }
]
table dropped!
```

**代码清单 10-17.** 执行代码清单 10-16 中代码的结果

# 小结

本章展示了如何在 Node.js 应用程序中使用关系型数据库。更具体地说，它探讨了如何使用 `mysql` Node 模块与 MySQL 数据库进行交互。完成本书的这一部分后，您应该能更自如地与大多数类型的数据库进行交互。关于关系型数据库，还有很多需要学习的内容。如果您有兴趣了解更多，[MySQL 文档](http://dev.mysql.com/doc/)是一个很好的起点。

本书的下一部分将不再聚焦于数据库，而是转向 Web 服务器软件。您已经了解了 Node 的核心 `http` 模块。下一部分将专注于 Express 框架，它提高了抽象层次，旨在提高开发者的生产力。

# 第 11 章

# Express 入门

我们之前已经提到过 Express，但现在我们将深入探讨它。[Express](http://expressjs.com/) 是一个 Node 模块，它在[第 5 章](#chapter_5)讨论的核心 Node 模块之上提供了一个轻量级的 Web 应用程序框架。截至本文撰写时，它是 npm 注册表中星标最多的模块。

在谷歌上搜索“Node 入门”几乎总会引导您去安装和使用 Express。这是一个非常成熟且经过社区测试的框架。Express 的第一个版本（1.0.0）于 2010 年 11 月发布，此前经历了多个测试版和候选发布版。从测试版到 3.0 版本，Express 的首席开发人员是 TJ Holowaychuk，他与 GitHub 社区的几位关键成员一起工作。3.0 版本之后，Holowaychuk 减少了对其日常开发的参与，将领导权交给了 GitHub 社区的一组核心成员。2014 年 7 月，Holowaychuk 将 Express 的所有权移交给了名为 StrongLoop 的 Node 初创公司。StrongLoop 继续保持 Express 的开源状态，大多数核心社区成员仍与 StrongLoop 一起致力于 Express 的稳定开发。

框架的成功取决于谁在使用它。Express 被 MySpace、Apiary.io、Ghost 以及 Mozilla 支持的登录系统 Persona 等公司使用。Express 还被用作 PayPal 开源的 [KrakenJS 框架](https://github.com/krakenjs/kraken-js) 的基础，而 StrongLoop 则在其 [LoopBack 项目](http://loopback.io/) 中使用了 Express。使用 Express 的精选公司完整列表可以在其[网站](http://expressjs.com/)上找到。该列表未包含任何内部/企业应用程序、个人 Web 项目或基于 Express 框架构建的 API。

在本章中，我们将讨论 Express 的基础——即 MEAN 技术栈中的“E”。Express 提供了请求路由、静态文件服务器、视图引擎集成以及大量的社区模块。Express 是一个非常轻量级的层，它位于前几章讨论的核心模块之上。使用轻量级框架意味着您编写的代码永远不会离 Node 的核心功能太远。在 Express 应用程序中，管道和流仍然非常容易访问。您还可以直接访问 `ClientRequest` 和 `ServerResponse` 这两个核心 Node 对象。在所有这些外在特性之下，Express 应用程序最终归结为 `http.createServer(...)`。

我们已经演示甚至构建了一些非常基础的 Web 服务器，它们只需要几行 JavaScript。如果我们只用四五行代码就能创建一个 Web 服务器，那为什么还要使用框架呢？也许编写我们自己的所有代码比学习另一个框架更容易。回顾我们在[第 6 章](#chapter_6)编写的代码，有几个问题清楚地说明了为什么使用框架是正确的选择，即：

-   可维护性
-   模块集成
-   解决方案结构

仅使用内置模块编写整个 Node Web 服务器，可维护性将成为一个问题。我们只创建了两个真正的路由，代码量就已经相当可观了。我们已经实现了路由参数，但如果我们想要多个路由参数呢？我们也不支持任何查询字符串参数或不同 HTTP 动词的概念。我们可以仅使用核心 Node 模块来实现所有这些功能，但这是低效的。实现简单的 Cookie 逻辑可能就需要几百行代码，而这只是完整 Web 服务器所需众多功能中的一小部分。仅使用核心 Node 模块编写一个具备现代 Web 服务器预期所有功能的完整 Web 服务器是不切实际的。

我们自行构建的服务器解决方案的第二个问题是模块。模块是 Node 生态系统中最大的驱动力之一。如果您想使用服务器端模板引擎或 CSS 预编译器呢？有多种 Node 选项可用，但将它们整合到当前的解决方案中会非常繁琐。如果我们坚持只使用核心模块，我们将限制自己，因为集成许多社区模块将变得困难。我们的服务器最终将变成一行行 JavaScript 意面代码。

第三个问题是，没有框架，您的解决方案完全没有结构。框架通常为您提供两大优势。第一是使用框架附带的所有工具、功能和社区。第二是使用框架为构建解决方案提供了基础。框架为您提供工具，同时也提供了思考和构建解决方案的蓝图。毕竟，Web 服务器在当下已经是一个解决的问题；确实没有必要重新发明轮子。

使用像 Express 这样的轻量级框架的一个缺点是，您仍然需要对第 5 章讨论的核心模块有合理的理解。您还需要理解 Web 服务器在路由、状态码和头部信息方面应该如何工作。与任何框架一样，Express 并非开发的“捷径按钮”。仍然存在需要解决的挑战和问题。Cookie 管理、用户身份验证和缓存等方面都由开发者自行实现。同样，npm 注册表上有帮助解决这些问题的 Express 模块，但它们并未内置在 Express 中，仍然需要集成代码。

## Express 的构建模块

Express 服务器可以分解为三个构建模块：路由器、路由和中间件。其他一切都只是对这些的完善和进一步的抽象。

### 路由器

任何 Web 服务器的核心都是强大的请求路由。如果您思考一下服务器-客户端的请求生命周期，它本质上归结为：客户端请求一个资源，服务器尝试定位该资源，如果找到，则以客户端期望的方式进行响应。如果没有结构化的方式来处理和路由请求，您的 Web 服务器将几乎无所作为。

核心的 `http` 模块没有资源路由的概念。我们必须为每个路由编写一个正则表达式。当请求进入 `http` 服务器时，我们必须在 `if else` 块中对照不同的正则表达式检查 `req.path`。此外，我们必须添加全面匹配逻辑来尝试查找 CSS 和 HTML 静态文件。即使只有几个路由，这也很繁琐；想象一下将其扩展到生产就绪的服务器。相比之下，Express 提供了一个易于使用且表达性强的路由接口。

通常，创建一个路由就像 `app.get('/employees/:id', function(req, res, next){...});` 这样简单。这将在路由表中创建一个匹配 GET 请求且 URI 为 `/employees/employee_id` 的路由。当匹配发生时，关联的函数将执行并向客户端发送响应。我们稍后将介绍路由声明的更多细节和功能。

### 路由查找

将路由添加到路由器的顺序非常重要。当请求进入 Web 服务器时，URI 会在路由表中运行。表中的第一个匹配项将是执行的代码。如果路由表下方有第二个匹配的路由，除非您进行一些内部重新路由，否则它将不会被执行。即使第二个路由在技术上更具体，第一个匹配项也始终是运行的那个。

### 静态文件

Web 服务器必须有一种简单的方法来提供静态文件。一个普通的网站可能有数百个静态文件，全部由 Web 服务器提供。必须有一种方式通知路由器，指定目录中的文件不需要单独添加到路由表中，并且在请求时应从文件系统中检索。

使用 Express，这可以通过 `express.static(directory)` 实现。这实质上在路由表中创建了一个规则，在 directory 中查找文件，如果找到，则提供这些文件。如果找不到，它将继续沿着路由表尝试匹配另一个路由上的文件。本章稍后会有一个关于静态文件的更完整示例，但在此处路由部分介绍 `static` 很重要。

### 中间件

**中间件** 是任何具有函数签名 `function (req, res, next)` 的 JavaScript 函数。一个 Express 路由可以根据需要关联任意数量的中间件函数。每个中间件函数都按从左到右的顺序执行。中间件函数可以在请求生命周期的任何部分使用，直到

响应会被发送回客户端。当中间件函数向客户端发送响应时，该请求就被视为已完成。完成请求的中间件函数有时被称为**处理程序**。中间件函数可用于设置 cookie 或头部信息、检查用户登录状态、压缩 JavaScript 以及实现其他无数种用途。

## 中间件解析

让我们逐一检查中间件函数的各个参数，以便更好地了解它们的用途。`req` 参数是传入的请求对象。它与我们在[第 6 章](#)中讨论的 `http.ClientRequest` 是同一个对象。当它到达我们的中间件函数时，已被 Express 增强以提供额外的功能。它拥有新的方法，如 `accepts()`、`get()` 和 `is()`。它还暴露了几个新的属性，如 `path`、`host`、`xhr` 和 `cookies`。关于 Express 添加到 `http.ClientRequest` 对象的完整方法列表，请查看[文档](#)。

`res` 对象是响应对象。如果你还记得第 6 章的内容，我们讨论过 `res` 是一个由 Express 增强的 `http.ServerResponse` 对象，就像 `req` 对象一样。Express 添加了 `cookie()`、`redirect()`、`send()` 以及许多其他有用的响应函数，这些函数在 Express [API 文档页面](#)中有记录。

最后，`next` 参数是 Express 框架提供的一个回调函数。这对于包含异步操作的中间件函数非常有用。只需在代码完成时调用 `next()`，即可通知 Express 该中间件函数已完成。如果中间件负责使用 `res.send` 发送响应，则无需调用 next。对于所有其他非终止的中间件函数，你必须仅调用 `next` 一次。

> **注意：关于 next 的注意事项**
>
> 与 Node 中所有其他回调函数一样，`next` 的函数签名是 `next(error)`。如果你试图通过 `next` 向另一个函数传递数据，将会触发 Express 错误处理程序。作为一般规则，任何传递给 `next` 的真值都将被视为错误，从而阻止当前请求的任何后续中间件函数执行。真值规则的一个例外是将字符串 "route" 传递给 `next`。传递 "route" 会使 Express 路由器跳转到下一个中间件函数或下一个匹配的路由（假设存在）。虽然这种技术有时很有用，但它可能创建难以追踪和调试的路由场景，因此应谨慎使用。

当你的 Express 应用变得更加复杂时，你最终需要在中间件函数之间传递数据。大多数人的第一反应是尝试通过 `next` 传递数据，但这会导致错误。每个新请求在路由开始时都会获得一个新的 `req` 和 `res` 副本。这些对象通过引用传递给每个中间件函数，你对 `req` 或 `res` 所做的任何更改都将对每个下游中间件函数可见。`res.locals` 是 Express 内置的容器，用于在函数之间传递数据。你也可以在 `req` 或 `res` 上创建自己的数据容器，例如 `res.myData`。

在不发送响应的中间件函数中始终执行 `next` 非常重要。如果你忘记这样做，响应将会挂起并且永远不会返回。即使函数中没有异步代码，你仍然必须调用 `next` 以保持请求在路由中继续流转。

## 路由

路由可以看作由一个 HTTP 动词和一个路径组成。HTTP 动词或方法通常是以下四种之一：`GET`、`POST`、`PUT` 和 `DELETE`。`GET` 请求用于从 Web 服务器获取数据。它是当今最常见的请求类型，用于静态内容和来自 Web 服务器的动态信息。`POST` 请求是第二常见的 HTTP 动词，用于向 Web 服务器发送数据。`DELETE` 和 `PUT` 请求远不常见，但随着越来越多的浏览器支持它们而日益流行。`DELETE` 用于从 Web 服务器删除信息，`PUT` 通常用于更新服务器上的现有数据。

还有一些[其他 HTTP 动词定义](https://www.w3.org/Protocols/HTTP/Methods.html)，但上面列出的四种是我们将重点关注的。HTTP 动词之间最重要的区别在于数据传递的方式。在 `GET` 请求中，数据通过 URI 或查询字符串参数传递。对于 `POST` 方法，它们附带有效载荷或请求体。这使得 `POST` 请求相比 `GET` 请求能在请求中发送更多信息。`DELETE` 方法通常没有请求体，类似于 `GET` 请求。最后，`PUT` 方法有一个有效载荷，就像 `POST` 一样。

HTTP 请求的后半部分是统一资源标识符，即 URI。Web 浏览器发出的每个请求都是针对某个 URI 的；例如，`www.google.com` 就是一个直接指向 Google 首页资源的 URI。URI 使用两种不同的机制向 Web 服务器传递参数数据：查询字符串参数和路由参数。

在 Express 路由定义中，我们将 HTTP 动词与一个模式组合来匹配传入的 URI 请求。该模式组件被称为路径。例如，一个带有路由参数的典型 Express 路径如下所示：`/teams/:teamName/employees/:employeeId`。

举个例子，假设我们有一个正在运行的 Express 服务器，并将浏览器指向 `/teams/nodeTeam/employees/15?mode=short`。浏览器的默认行为是发送 `GET` 请求，因此浏览器将向我们正在运行的 Express 服务器发出一个 `GET` 请求，请求位于 `/teams/nodeTeam/employees/15?mode=short` 的资源。如果我们结合动词和路径的概念，就会有一个路由定义，看起来像 `GET "/teams/:teamName/employees/:employeeId"`。该路由将匹配我们从浏览器发送的请求。

当请求进入 Express 路由器时，路由参数 `:teamName` 和 `:employeeId` 将从传入的 URI 中解析出来，并通过 `req.params.teamName` 和 `req.params.employeeId` 获取。Express 路由器将在路由表中查找此路由，如果匹配成功，相应的代码将运行并发送响应。URI 的查询字符串部分*不会*用于路由决策。

## 可选参数

在前面的示例中，所有路由参数都是必需的，因为没有它们，客户端请求将无法匹配我们路由表中的任何内容。假设我们希望允许客户端请求某个团队的所有员工？那么我们可以让 :employeeId 参数变为可选的。假设没有此参数时，我们应该返回 teamName 团队的所有员工。如果我们为参数添加 `?` 后缀，它就变成了可选参数。更新后的路径参数将变为 `/teams/:teamName/employees/:employeeId?`。

因此，以下两个 URI 都会匹配此路由路径：`/teams/nodeTeam/employees` 和 `/teams/nodeTeam/employees/15`。虽然可选路由参数有时很有用，但它们也可能创建难以追踪的路由 bug。如果一个开发人员创建了一个匹配路径模式 `/teams/:teamName/employees/:employeeId?` 的路由，而另一个开发人员创建了另一个路径为 `/teams/:teamName/employees` 的路由，这两种模式都会匹配对 `/teams/javaScriptTeam/employees` 的请求。如果有两个不同的路由设置，路由器会使用哪一个？请记住路由器部分的一个关键点：第一个注册的路由将是路由表中使用的条目。与其依赖路由的顺序，不如在可选路由参数造成困惑时避免使用它们。

最后，可以在单个路由路径中设置多个可选参数。假设我们希望扩展前面的示例，允许 `:teamName` 和 `:employeeId` 都是可选的。这将允许用户从同一个路由定义获取团队或单个员工的信息。如果我们更新示例，路径值将变为 `/teams/:teamName?/employees/:employeeId?`。现在用户可以向 `/team/node`、`/team/employees/15` 和 `/team/node/employees/15` 发出请求。所有这三个 URI 都将被我们更新后的路径参数所覆盖。通常，这不是一种推荐的方法，因为它难以记录，并且根据不同的参数选项，响应内容也不明确。

## 其他路由选项

Express 还允许使用正则表达式作为 URI。当使用正则表达式定义路由时，开发人员需要负责处理任何路由参数。让我们将 "/teams/:teamName/employees" 重写为正则表达式。`/^\/teams\/(\w+)\/employees$/i` 就是等效的 URI 定义。使用正则表达式时，你需要使用 `( )` 创建捕获组，以便在任何中间件函数中访问该值。

值得一提的是，在底层，Express 会将所有路由定义转换为正则表达式。如果你回顾[第 6 章](Chapter 6)并查看我们在编写简单 Node 服务器时如何设置路由，这应该不会太令人惊讶。



## 综合运用

我们已经介绍了 Express 应用的构成要素：路由器、中间件函数、静态文件服务器以及基本路由说明。让我们用一个非常简单的代码示例来综合运用这些知识。我们将创建一个小的 Express Web 服务器，使用到目前为止所涵盖的所有内容：

```javascript
var express = require('express');
var app = express();

// 路由一
app.get('/teams/:teamName/employees/:employeeId', function (req, res, next) {
  console.log('teamName = ' + req.params.teamName);
  console.log('employeeId = ' + req.params.employeeId);
  res.send('path one');
});

// 路由二
app.get('/teams/:teamName/employees', function (req, res, next) {
  console.log('setting content type');
  res.set('Content-Type', 'application/json');
  res.locals.data = 100;
  next();
}, function (req, res, next) {
  console.log('teamName = ' + req.params.teamName);
  console.log(res.locals.data);
  res.send('path two');
});

// 路由三
app.get(/^\/groups\/(\w+)\/(\d+)$/, function (req, res, next) {
  console.log('groupname = ' + req.params[0]);
  console.log('groupId = ' + req.params[1]);
  res.send('path three');
});

var server = app.listen(1337, function() {
  console.log('Server started on port 1337');
});
```

**清单 11-1. 创建一个简单的 Express 应用程序**

清单 11-1 是对本章所涵盖大多数主题的总结。前两行创建 Express 应用程序。`app.use(express.static(__dirname + '/public'));` 设置了我们的静态文件服务器。我们将在下一章更详细地介绍 `app.use`。请记住，这一行会向路由表中添加一个条目，以便在 public 目录中查找文件。

前两个 `app.get` 行建立了我们本章一直在讨论的路由。如你所见，我们可以通过 `req.params` 访问路由参数。最后一个 `app.get` 行展示了使用正则表达式作为 `app.get` 的 path 参数。

路由二展示了在单个路由中使用多个中间件函数的示例。当路由匹配时，Express 将执行 Express 通道中的第一个函数。在这个示例中，我们将记录一些信息，设置 "Content-Type" 响应头，将一个值附加到 `res.locals`，然后调用 `next()`。请记住，除非你用 `res.send()` 或其他终止函数结束响应，否则你总是必须调用 `next()`。调用 `next()` 后，Express 将前进到下一个中间件函数；记录来自 `req.params.teamName` 的数据，记录附加到 `res.locals.data` 的值，然后发送一个简单的 JSON 对象。

路由三展示了使用正则表达式参数的示例。不同路径段周围的括号创建正则表达式捕获组。我们通过 `req.params[index]` 按索引访问每个值。正则表达式捕获组是编号的，从索引 0 开始。0 对应于 `(\w+)` 捕获组，1 对应于 `(\d+)`。

最后几行创建一个服务器并开始监听 1337 端口。`app.listen` 的妙处在于，它与我们使用纯 Node 编写服务器时使用的 `server.listen` 函数完全相同。

尝试在浏览器中测试以下任意 URI，以测试不同的路由和结果：

- /teams/javascript/employees/15 — 应返回 "path one" 并在控制台中记录 `teamName = javascript employeeId = 15`。
- /teams/javascript/employees — 应返回 "path two" 并在控制台中记录 `setting content type teamName = javascript`。如果你通过 `curl` 或浏览器中的开发工具检查响应头，你应该能看到正确的 `Content-Type` 响应头。
- /groups/accounting/142 — 应返回 "path three" 并在控制台中记录 `groupname = accounting groupId = 142`。

上面清单 11-1 中的代码应该能证明，与仅使用核心模块的 Node 服务器相比，这个小型 Express Web 服务器维护和调试起来要容易得多。它更易读，需要更少的代码，并且具有更多功能。请记住，尽管 Express 是一个框架，但底层核心模块永远不会遥不可达。

## 生成 Express 应用

如果你还记得[第 4 章](about modules)的内容，有时最好全局安装模块，因为它们提供了命令行界面，这在特定项目之外也很有用。现在让我们全局安装 `express-generator` 模块。安装完成后，创建一个空目录并从命令行运行 `express`。

让我们快速了解一下 express 生成器为我们做了什么。（我们将在下一章更详细地讨论这些文件的*实际内容*。）你会注意到，生成器创建了几个文件夹和文件，为开发人员提供了一个合理且可预测的项目结构。生成器还会创建一个 `package.json` 文件，其中预填充了一些依赖项。

`app.js` 是应用程序的主要入口点，也是 Web 服务器逻辑的所在地。还记得我们配置为在 public 文件夹中查找的静态文件服务器吗？public 文件夹已被创建，并预先填充了用于图像、JavaScript 文件和样式表的子文件夹。我们稍后会有用到这些文件夹的时候。

routes 文件夹内有几个用于声明路由并将其附加到 Express 应用的文件。这是一个值得遵循的良好模式。对于一个完整的 Web 服务器，可能会有数千个路由，这将使 `app.js` 文件完全无法维护。而且在一个团队中工作也会很困难，因为该文件会不断变化。

## Jade

views 文件夹设置为使用 [Jade](http://jade-lang.com/)，一种 Node 服务器端模板语言。虽然我们在本书中不会使用 Jade，但值得提一下。Jade 是一个模板引擎，但它也是一种更高阶的语言。你用 Jade 语言编写视图，然后将其编译为原始 HTML，让你用更少的字符编写更多的 HTML。它还确保了你网页上的 HTML 永远不会破损或错误。如果你尝试创建无效的 HTML，编译器将抛出错误。

# 小结

[清单 11-1](listing-11-1) 是一个 Express 应用，它完全抽象掉了对 `http` 模块的直接使用。它允许我们以简单统一的方式声明路由。它提供了一个强大的路由器、一个内置的静态文件服务器，以及一个我们可以遵循的编程模式来添加更多功能和路由。它还通过中间件函数的概念促进了代码重用和模块化。

尽管我们可以在不直接使用 `http` 模块或任何其他核心模块的情况下创建整个 Web 服务器，但它们永远不会远离我们的视线。`req` 和 `res` 都是核心 Node 对象，`app.listen` 与 `server.listen` 相同。

本章演示了 Express 应用程序的基础知识。在下一章中，我们将详细介绍本章生成的 Express 应用，并讨论典型 Express Web 服务器的架构。

## 第 12 章

## Express 应用程序的架构

在上一章中，我们生成了第一个 Express 应用程序。在撰写本文时，Express 的版本是 4，因此本书将讨论该版本。Express 生成器为开发人员提供了一个构建新 Web 服务器的良好起点。它提供了几个简单的路由、Jade 模板集成、Cookie 和正文解析以及静态文件服务。在本章中，我们将介绍生成的 Express 应用程序的重要文件和概念。这将使你对 Express 生态系统的架构，以及框架许多组件之间的交互有深入的理解。

### 启动服务器

你可能首先会注意到的是，如果你运行 `node app.js`，什么都没有发生。生成器创建了一个 `bin` 文件夹，里面有一个 `www` 文件。其目的是使用这个文件来启动服务器，而不是 `app.js`。要启动你的服务器，请运行 `node bin/www`。你也可以运行 `npm start`，因为该命令已经输入到 `package.json` 中。服务器运行后，在 Web 浏览器中访问 `localhost:3000`，你应该会看到一个简单的欢迎页面。

有一件事值得立即提及，那就是 `bin` 文件夹和 `www` 文件的添加。一般来说，Node 的一个惯例是将打算从命令行运行的文件放在 `bin` 文件夹中。生成应用中的 `www` 文件作为 Node 应用程序的入口点。本例中的 `www` 文件引入了 `app.js` 并启动 Express 服务器。

## app.js

尽管我们并不使用 `node app.js` 启动服务器，但 `app.js` 仍然包含了大部分服务器逻辑。快速浏览文件，你应该会看到一些熟悉的概 念以及一些新内容。请注意几处 `app.use` 的用法。我们在上一章曾简要提及，但现在要更详细地讨论它。

## app.use

`app.use` 注册一个中间件函数，该函数将在 Web 服务器收到的每个请求上调用。它对于需要在每个请求上执行的任务非常有用。请记住，`app.use` 只是向路由表添加条目。其他路由的顺序规则同样适用于 `app.use` 语句。每次新请求到达时，这些语句将按照它们从上到下的注册顺序执行。

假设你想为服务器收到的每个请求向控制台打印一条消息。你可以使用类似清单 12-1 中的代码，并在该中间件中记录请求信息。`app.use` 其实非常简单。它只是注册一个中间件函数的方式，该函数在每个请求上运行，无论 HTTP 动词或 URI 是什么。

```javascript
app.use(function (req, res, next) {
  console.log(req.method + ' ' + req.url);
  next();
});
```

清单 12-1. 一个简单的请求日志记录器

`app.use` 提供的额外逻辑是可选的第一个参数，称为挂载路径。如果未明确提供路径参数，它默认为 `/`。假设我们只想记录 Web 服务器 `/api` 部分的请求。我们可以修改清单 12-1 以使用挂载点：

```javascript
app.use('/api', function (req, res, next) {
  console.log('/api logger');
  console.log(req.method + ' ' + req.url);
  next();
});
```

清单 12-2. 记录 API 请求

由于这尚不是一个完整的示例，如果测试时收到 404 错误，请不要惊慌。它们更多地是为了演示语法和概念，而非端到端的示例。在本章结束时，你将构建一个功能齐全的 Express 服务器。

通过在参数列表中添加 `/api`，我们改变了想要记录的请求。在清单 12-2 中，只有以 `/api` 开头的请求才会被记录。这是仅为路由表的特定部分运行某些中间件的一种方式。假设你想跟踪客户端对 `/api` 资源的调用次数。这将是一个只跟踪这些特定 `/api` 请求的好方法。

## cookieParser

到目前为止，我们一直在编写自己的中间件函数。请记住，使用 Express 这样框架的原因之一就是为了使用现成的模块。我们生成的 Express 应用预装了几个最常见的 Express 中间件函数。我们将详细研究 `cookieParser`，以更好地了解大多数社区中间件函数是如何编写的。`cookieParser` 中间件函数本质上是将“Cookie”头转换为一个可用的 JavaScript 对象。

`cookieParser` 的代码可以在 `node_modules/cookie-parser/index.js` 中找到。你应该注意到的第一个元素是导出函数的签名：它是一个返回函数的函数。这是一种非常常见的模式，因为它允许将选项传递给中间件函数。在 `cookieParser` 示例中，我们可以传递 `secret` 和 `opt` 参数。

通过从另一个函数返回一个函数，我们创建了一个闭包。在这个例子中，`cookieParser` 返回一个 Express 中间件函数。内部的 `cookieParser` 函数可以访问第一次调用外部 `cookieParser` 时传入的 `opt` 和 `secret` 的原始值。例如，如果我们像这样包含 `cookieParser` 中间件：`app.use(cookieParser('cookie-secret'))`，每个请求都会经过 `cookieParser` 中间件。当这行代码在 Express 服务器首次启动时执行，`cookieParser()` 将返回一个中间件函数。`secret` 将是 `'cookie-secret'`，内部返回的函数将可以访问 `secret`。

返回的函数签名为 `function (req, res, next) {...}`，就像我们研究过的其他每个中间件函数一样。这个函数还演示了编辑和将值附加到 `req` 和 `res` 并在其他地方使用这些值的概念。`secret`、`cookies` 和 `signedCookies` 将附加到每个执行此中间件函数的请求（`req`）上，并且可供每个下游中间件函数使用。最后，在所有逻辑之后，调用 `next` 以使请求继续在服务器中流转。

你可以自由研究通过 `app.use` 注册的其他中间件函数，例如 `bodyParser.json` 和 `bodyParser.urlencoded`。你会发现它们都遵循相同的模式。

## 再探静态文件

掌握了 `app.use` 和中间件模式后，我们可以重新审视静态文件服务，并更好地解释其工作原理。让我们看看 `app.js` 中设置静态文件服务器的那一行：

```javascript
app.use(express.static(path.join(__dirname, 'public')));
```

清单 12-3. Express 默认静态文件服务器

首先，我们使用了 `app.use`，它接受一个可选的挂载点和一个中间件函数。由于我们所有的静态内容都位于 `public` 目录下，因此在这种情况下我们不需要挂载点，默认的 `/` 值就可以。

`express.static` 是一个接受 `root` 参数、一个可选的 `options` 参数并返回中间件函数的函数；这与我们在 `cookieParser` 中看到的模式相同。`path` 是 Node 核心模块之一，用于路径和目录逻辑。我们不是简单地将 `'public'` 传递给 `express.static`，而是将全局可用的当前目录 `__dirname` 与 `'public'` 连接起来以获得完整路径。以这种方式使用 `path` 是一个好习惯，有助于避免不同操作系统之间的任何文件系统差异。

最后，返回一个中间件函数并通过 `app.use` 注册，该函数将尝试定位保存在 `public` 目录下的静态文件。如果找到，它将提供它们。如果未找到，它将继续从上到下在路由表中查找匹配的路由。

## 错误处理

每当你向 `next` 传递一个真值时，你都在提醒 Express 发生了错误。我们在上一章提到了这一点，但这到底是什么意思呢？切换回 `app.js`，你应该会看到一个类似于清单 12-3 的函数。

```javascript
app.use(function(err, req, res, next) {
    res.status(err.status || 500);
    res.render('error', {
        message: err.message,
        error: err
    });
});
```

清单 12-4. Express 错误处理器

是什么让它成为一个错误处理器而不仅仅是一个普通的中间件函数？从技术上讲，它是一个中间件函数，因为我们通过 `app.use` 注册了它，但看看函数签名：`err, req, res, next`。这个中间件函数期望一个 *err* 参数作为第一个参数，而其他中间件函数期望一个请求对象作为第一个参数。你传递给 `next` 的真值会成为 Express 错误处理函数中的 *err* 值。在默认的错误处理函数中，我们使用 `res.render` 来渲染错误模板，并将有关错误的信息传递给视图。

处理编程中的错误有一些成熟的规则，JavaScript 也不例外。虽然传递给 `next` 的任何真值都会被发送到错误处理器，但你应该养成传递真正的 *Error* 对象而不是字符串的习惯。错误对象包括执行堆栈，这在跟踪错误条件时通常非常宝贵。当你的 Express 应用在生产环境中运行时，简单地传递 "there was an error" 到 `next` 不会有多大帮助。

如果这是一个生产系统，我们可能希望将错误记录到数据库或日志文件等永久性存储中。根据错误严重程度，我们可能还想发送电子邮件警报甚至重启服务器。默认的错误处理器是一个很好的起点，你应该将其视为一个需要填充更健壮错误处理的存根。

## 实践中的错误处理

让我们编写一个快速的中间件函数，演示如何接入 Express 错误处理中间件，并展示 Express 服务器中的一个常见模式。我们将参考第 8 章中编写的一些代码。假设在这个例子中

我们已经与 MongoDB 建立了开放连接，并且正确地定义了 `Employee` 模型。在这个中间件函数中，我们将通过 ID 查找员工，该 ID 是通过路由参数传递给 Express 服务器的。

```
function retrieveEmployee (req, res, next) {
  Employee.findOne({
    _id: req.params.employeeId
  }).exec(function (error, employee) {
    if (error) {
      return next(error);
    }
    res.locals.employee = employee;
    return next();
  });
}
```

## 清单 12-5. 使用 Express 错误处理器

让我们重新审视[第 8 章](#)中的 `retrieveEmployee` 函数，并将其重构为一个 Express 中间件函数。在这个版本中，我们将通过名为 `employeeId` 的路由参数提供的 ID 来查找员工。如果查找员工时出现错误，例如连接已关闭或数据库不可达，`error` 将是一个 `Error` 对象。员工不在数据库中并不一定被视为错误。如果出现错误，我们将调用 `next` 并传递 `error`。否则，我们将结果员工附加到 `res.locals`，调用 `next`，并继续请求生命周期。

当你调用 `next(error)` 时，错误处理器将接管，错误处理逻辑将执行。当你这样做时，你通常*不*希望路由的其余部分执行，因为代码处于意外的错误状态。调用 `next` 并传入错误将中断当前运行的路由，并直接跳转到错误处理函数；然而，关键是要记住调用 `return next(error)`。仅仅调用 `next` 不足以停止当前中间件函数的执行。只有 `return` 才能停止函数执行。

在清单 12-4 中，如果你省略了 `return next(error)` 语句中的 `return`，你将引入一个难以追踪的 bug。在发生错误的情况下，错误处理器将执行并用错误页面进行响应。之后，执行将继续向下进行，尝试将 `employee` 附加到 `res.locals.employee`，然后再次调用 `next`。这最终将导致服务器尝试为一个已经从错误处理器获得响应的请求发送第二个响应。一个良好的实践是始终在回调前加上 `return`，以确保安全。

## app.set

`app.set` 提供了一个读写应用程序范围内设置的公共位置。例如，运行 `app.set('title', 'Express Server');` 将服务器设置 `title` 赋值为 `Express Server`。你可以使用 `app.get('title')` 取回这些值。在渲染视图时，你可以通过 `settings` 访问应用程序设置。

大多数设置是供开发者使用的；然而，Express 内部确实使用此机制来管理内部设置，例如 `views`、`view engine`、`jsonp callback name` 以及[此处记录的其他几个](#)。

如果你再次查看 `app.js`，你会注意到示例已将 `view engine` 设置为 jade，将 `views` 设置为使用 views 目录。在内部，Express 引用这些值并将其视为配置选项。你经常会在服务器文件的顶部看到几个 `app.set` 调用。

## Router 对象

你会在 app.js 中注意到，没有通过 app.get 进行路由注册。这是因为生成的应用程序利用了 Router 对象。

Router 对象就像一个迷你的 Express 应用程序，它只能执行中间件和执行路由。它缺少完整 Express 应用程序的其他功能，并且是一种可以被主 Express 应用程序 require 和使用的中间件。

在我们之前的示例中，当我们使用 app.get 注册路由时，我们指的是每个 Express 应用程序都附加的内置 Router 对象。

小的 Router 对象允许开发者将路由注册从 app.js 分离到一个或多个文件中。这极大地清理了主服务器文件，使其仅包含初始化代码，并将大部分逻辑移至模块化文件中。

### 使用 Router 对象

在 app.js 中，你可能已经注意到 `app.use('/users', users);`。如果我们查看 `/routes/users.js`，我们将看到一个关于如何使用 Router 对象的很好示例。

首先，我们通过 `express.Router();` 获取对 Router 对象的引用，从那里开始，它具有与我们使用 app 时完全相同的接口。你可以注册路由和中间件，甚至可以包含额外的 `router.use` 命令。

关于 users.js 有两个有趣之处；第一，我们在文件末尾导出路由器。就像任何其他 Node 对象一样，我们导出希望在其他文件中访问的项目。第二，唯一注册的路由是 GET /，它发送 "respond with a resource"。但是如果你启动服务器并将 Web 浏览器指向 /，你会看到的是 Express 落地页，而不是 "respond with a resource"。那么这里发生了什么？

如果你翻回 app.js，应该就清楚了。`app.use('/users', users);` 是在 /users 下设置一个挂载点，任何以 /users 开头的路由都应该使用 users 中间件函数。我们从 users.js 导出路由器，该路由器只有一个附加的路由。

如果你向 /users 发出请求，你应该会在屏幕上看到没有任何样式的 "respond with a resource"。当 GET 请求 /users 进入服务器时，它将匹配 /users 挂载点。/users 将从路径中剥离并变成 /。执行将继续进入已注册的中间件。已注册的中间件是一个 Express 路由器，它为 / 设置了一个单一的路由，因此这就是将执行并发送所需响应的代码。

能够像这样分离路由注册确实有助于在不同的端点之间分配职责。它还有助于减少对 app.js 的更改，并防止团队相互覆盖和创建代码冲突。

## 练习

为了将本章涵盖的所有内容整合起来，让我们使对 /users 的请求实际返回一些用户数据和当前时间。而不仅仅是返回 JSON，让我们也发送一些简单的 HTML。在示例代码中，我们将再次使用 `setTimeout` 模拟数据库请求；但是，如果你有雄心壮志，我们鼓励你使用 MongoDB 章节中的一些代码与你的 MongoDB 实例进行通信。

在这个例子中，我们想执行几个任务：

- 1. 模拟数据库交互以获取用户列表（再次，如果你有雄心壮志，可以继续与你的 MongoDB 通信）。
- 2. 获取数据库交互的结果并生成一个简单的 HTML 文档来响应。
- 3. 添加对本地 CSS 文件的引用以说明使用 `app.use(express.static(path.join(__dirname, 'public')));`。

完整解决方案请参考清单 12-6。

### 模拟数据库交互

到现在为止，你应该已经非常熟悉使用 setTimeout 模拟数据库调用了。为了保持代码的可读性，将 routes/users.js 中的单一路由改为具有两个中间件函数。通常，我们希望将这些调用分离到不同的文件和模块中。对于步骤 1，编写一个 setTimeout 函数来模拟数据库活动。确保你的代码设置为将用户数组传递到下一个中间件函数。

### 生成 HTML

在第二个中间件函数中，将时间戳附加到结果对象。获得时间戳后，设置一个名为 X-Special-Header 的标头为 "MEAN Stack"。最后，将响应发送回客户端。你可以在清单 12-6 中找到完整的答案。尝试使用我们在本章和 Express 文档中涵盖的内容，在不查看答案的情况下解决这个问题。

routes/users.js

```
var express = require('express');
var router = express.Router();

/* GET users listing. */
router.get('/', function(req, res, next) {
  setTimeout(function() {
    res.locals.users = [{
      first: 'Abraham',
      last: 'Lincoln'
    }, {
      first: 'Andrew',
```



## 摘要

在本章中，我们深入了解了 Express 应用的更多内部工作原理。如您所见，使用 Node 框架比直接使用 `http` 模块要更加容易且易于维护。仅用几行代码，我们就构建了一个几乎功能完备的服务器，而且无需接触任何核心 Node 模块。

Express 的路由逻辑非常强大，允许开发者使用字符串和正则表达式来注册路由。Express 还有一个专门的 Router 对象，它是一个精简版的 Express 应用，使开发者能够将路由注册拆分到独立的文件中，以保持主服务器文件的整洁。

Express 路由中的函数被称为中间件，它们都具有相同的函数签名。开源社区中有许多可用的中间件函数，可以解决很多常见的 Web 开发问题，并能轻松地集成到 Express 服务器中。

在下一章中，我们将继续构建我们的人力资源风格应用，并将到目前为止涵盖的三种技术结合起来：Express、Node 和 MongoDB。

## 第13章 在我们的应用中使用 Express

本章将回顾在第6章开始、第9章继续的人力资源应用示例。到目前为止，我们已经创建了一个与 MongoDB 存储通信的 Node 应用。我们使用了 Node 的 `http` 模块来编写自定义的路由实现。现在我们有了更强大的 Express 路由，我们要替换掉我们的 `http` 代码。

如果我们从零开始一个新应用，我们可能会使用脚手架生成器，比如 Yeoman（它有一个 MEAN 堆栈生成器）；然而，由于我们是在更新现有应用，我们将手动修改所有内容。

## 更新 package.json

迁移到 Express 的第一步是更新 package.json 文件。我们需要安装 Express 和几个中间件。我们可以使用清单 13-1 中的命令来安装所有必需的模块：

```
npm install --undebug body-parser cookie-parser debug express morgan serve-favicon
```

**清单 13-1.** 安装 Express 及其他必需的中间件

我们还可以移除 colors 和 array.prototype.find 模块，因为我们不再需要它们了。这可以使用清单 13-2 中所示的命令来完成：

```
npm remove --save colors array.prototype.find
```

**清单 13-2.** 移除不再需要的模块

我们还要在 scripts 对象中添加一个 start 条目。这将使我们能够使用 `npm start` 命令轻松启动服务器。添加清单 13-3 所示的条目。注意，此命令依赖于 bin/www，该文件尚不存在。我们很快就会添加它。

```
"start": "node ./bin/www"
```

**清单 13-3.** 在 scripts 对象中添加 start 条目

更新后的完整 package.json 如清单 13-4 所示。

```
{
  "name": "example-server",
  "version": "0.1.0",
  "description": "HR application server.",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node ./bin/www",
    "populate": "node ./bin/populate_db"
  },
  "author": "Peter Pluck",
  "license": "ISC",
  "dependencies": {
    "async": "^0.9.0",
    "body-parser": "^1.6.7",
    "cookie-parser": "^1.3.2",
    "debug": "^2.0.0",
    "express": "^4.8.7",
    "mongoose": "^3.8.15",
    "mongoose-post-find": "0.0.2",
    "morgan": "^1.2.3",
    "serve-favicon": "^2.1.1"
  }
}
```

**清单 13-4.** 更新后的 package.json 文件

## npm start 脚本

下一步是在项目的 bin 目录中创建一个名为 www 的文件。www 的内容如清单 13-5 所示。这段代码启动我们的服务器，服务器定义在项目的 index.js 文件中。服务器默认监听 3000 端口，但该值可以通过设置名为 PORT 的环境变量来覆盖。例如，如果你想让服务器监听 4000 端口，可以使用命令 `PORT=4000 npm start`。

```
var debug = require('debug')('example-server');
var app = require('../');

app.set('port', process.env.PORT || 3000);

var server = app.listen(app.get('port'), function() {
  debug('Express server listening on port ' + server.address().port);
});
```

**清单 13-5.** bin/www 脚本

注意，debug 模块用于显示消息。默认情况下，如果你运行 `npm start`，不会显示任何内容。要启用调试消息，请将进程的 DEBUG 环境变量设置为 `example-server`。

## 定义路由

下一步是创建 Express 路由来处理传入的请求。在项目根目录下创建一个 routes 目录。这是我们将放置所有路由文件的地方。在 routes 目录中，创建两个文件：employees.js 和 teams.js。

### 员工路由

routes/employees.js 的内容如清单 13-6 所示。我们支持以下路由：

- GET /employees — 返回所有员工，按姓氏排序
- GET /employees/:employeeId — 返回单个员工的信息，其员工 ID 通过 employeeId 参数传递
- PUT /employees/:employeeId — 用于更新现有员工;员工 ID 通过 employeeId 参数传递，而员工数据则在请求体中传递

```
var express = require('express');
var mongoose = require('mongoose');
var Employee = mongoose.model('Employee');
var Team = mongoose.model('Team');
var router = express.Router();

router.get('/employees', function(req, res, next) {
    Employee.find().sort('name.last').exec(function(error, results) {
        if (error) {
            return next(error);
        }

        // Respond with valid data
        res.json(results);
    });
});

router.get('/employees/:employeeId', function(req, res, next) {
    Employee.findOne({
        id: req.params.employeeId
    }).populate('team').exec(function (error, results) {
        if (error) {
            return next(error);
        }

        // If valid user was not found, send 404
        if (!results) {
            res.send(404);
        }

        // Respond with valid data
        res.json(results);
    });
});
```



}); });
```

```
router.put('/employees/:employeeId', function (req, res, next) {
  // 移除此操作，否则 mongoose 会抛出错误
  // 因为我们尝试更新的是 mongo ID
  delete req.body._id;
  req.body.team = req.body.team._id;

  Employee.update({
    id: req.params.employeeId
  }, req.body, function (err, numberAffected, response) {
    if (err) {
      return next(err);
    }

    res.send(200);
  });
});
```

```
module.exports = router;
```

**清单 13-6. routes/employees.js 的内容**

## 团队路由

团队路由存储在 `routes/teams.js` 中，其内容如清单 13-7 所示。支持以下团队路由：

-   `GET /teams` — 显示数据库中存储的所有团队，按团队名称排序
-   `GET /teams/:teamId` — 显示有关单个团队的信息；团队的 ID 通过 `teamId` 参数传递，并且必须与关联的 MongoDB `_id` 属性匹配

```
var express = require('express');
var mongoose = require('mongoose');
var Team = mongoose.model('Team');
var router = express.Router();
```

```
router.get('/teams', function (req, res, next) {
  Team.find().sort('name').exec(function (error, results) {
    if (error) {
      return next(error);
    }

    // 返回有效数据
    res.json(results);
  });
});
```

```
router.get('/teams/:teamId', function (req, res, next) {
  Team.findOne({
    _id: req.params.teamId
  }, function (error, results) {
    if (error) {
      return next(error);
    }

    res.json(results);
  });
});

module.exports = router;
```

**清单 13-7. routes/teams.js 的内容**

## 更新 index.js

我们将 Express 升级的最后一步是转换 `index.js` 文件。修改后的 `index.js` 内容如清单 13-8 所示。这个文件中发生了很多事情，因此我们将分小块进行解释。

## 注意：通常被称为...

应用程序主文件最常见的两个名称是 `index.js` 和 `app.js`。`app.js` 在 Express 应用程序中可能更常见，但两者基本上可以互换使用。

文件开头导入了 Express、`path` 和一些中间件。接下来，我们建立数据库连接，导入应用程序的路由，并初始化 `app` 变量。然后我们设置了一些中间件。注意，`favicon` 中间件被注释掉了。这是因为我们的项目中没有网站图标。如果你的项目有，请取消此行的注释。

对 `app.use()` 的最后五次调用真正包含了我们应用程序特定的代码。通过 `use()` `employees` 和 `teams` 变量，我们将路由添加到路由器中。下一步是调用 `app.use()` 来设置一个通用的 404 路由。这用于对我们的路由未处理的所有请求返回 404。

最后两个 `app.use()` 调用负责处理错误。你会注意到，在开发环境中只使用了一个错误处理器，它用于发回额外的错误数据。最终的处理器用于非开发设置，并且只返回状态码。

```
var express = require('express');
var path = require('path');
var favicon = require('serve-favicon');
var logger = require('morgan');
var cookieParser = require('cookie-parser');
var bodyParser = require('body-parser');

require('./lib/connection');
var employees = require('./routes/employees');
var teams = require('./routes/teams');

var app = express();

// app.use(favicon(__dirname + '/public/favicon.ico'));
app.use(logger('dev'));
app.use(bodyParser.json());
app.use(bodyParser.urlencoded({ extended: true }));
app.use(cookieParser());
app.use(express.static(path.join(__dirname, 'public')));

// 应用程序路由
app.use(employees);
app.use(teams);
```

```
// 捕获 404 并转发到错误处理器
app.use(function(req, res, next) {
  var err = new Error('Not Found');

  err.status = 404;
  next(err);
});

// 错误处理器

// 开发环境错误处理器
// 将打印堆栈跟踪
if (app.get('env') === 'development') {
  app.use(function(err, req, res, next) {
    res.status(err.status || 500);
    res.send({
      message: err.message,
      error: err
    });
  });
}

// 生产环境错误处理器
// 不会向用户泄露堆栈跟踪
app.use(function(err, req, res, next) {
  res.status(err.status || 500);
});

module.exports = app;
```

**清单 13-8.** 修改后的 index.js 内容

# 总结

本章继续开发我们的人力资源示例应用程序。在本章中，我们从一个基于自定义 `http` 的服务器迁移到了一个更灵活、更可扩展的、基于 Express 的应用程序。此时，我们已经为 HR 应用程序构建了一个相当坚实的后端。不久，我们将把注意力转向使用 AngularJS 构建的前端。但首先，我们将对 Hapi 进行一次旋风之旅，这是一个由沃尔玛实验室开发的 Express 替代方案。

# 替代服务器框架

对于像 JavaScript 这样流行的语言，对于如何解决任何问题——从简单的循环优化等小事到更复杂的，例如模拟经典面向对象继承的最佳方式——必然存在意见分歧。以最佳方式执行任务的热情和动力伴随着 JavaScript 爱好者进入了 Node 社区，这一点在查看可用的 Web 服务器框架时显而易见。进行一些快速的 Google 搜索，你会发现可用的框架列表相当长，而在 npm 上搜索 "framework http" 会得到一个接一个的各种 Web 服务器框架页面。这里的选项太多，无法一一列举，否则对它们都不公平。

在本章中，我们将专注于 hapi，一个 Express 框架的替代方案。我们将研究 hapi，因为它是第二受欢迎的 Node 框架，并且它与 Express 非常不同。[4]

## hapi 概述

hapi 服务器框架拥有一个活跃且不断增长的社区，以及许多知名支持者。在撰写本文时，hapi 是 npm 注册表中第二受欢迎的服务器框架，并且正迅速变得更受欢迎。hapi 的方法是配置中心化而不是开发中心化。这使得开发者可以更多地关注业务逻辑，而不是 Web 服务器的细节和不断增长的中间件功能列表。

正如 Express 的用户列表令人印象深刻一样，hapi 的用户列表也是如此。目前在生产环境中使用 hapi 的一些知名公司包括 OpenTable、PayPal、Beats Music 和 Walmart；你可以访问网站查看使用 hapi 的完整公司列表。沃尔玛对 hapi 的成功有额外的动力，因为主要贡献者在沃尔玛的研发部门工作时构建了 hapi。

hapi 提供了与 Express 相同的所有高级功能。它具有健壮的路由系统、模板语言的集成选项以及易于使用的静态文件服务器。它还支持强大的插件系统，并提供内置的输入验证。

## Express 比较

Express 和 hapi 之间存在许多差异。Express 中的主要逻辑组件是中间件函数。一个路由由一系列一个或多个中间件函数组成，最终是一个向客户端发送响应的函数。开发者在 Express 中必须编写的大部分中间件逻辑在 hapi 中是配置选项。hapi 中的路由由一个路径、一个 HTTP 方法和一个单独的处理函数组成。其他所有内容都通过传递给路由器的配置对象来处理。

让我们重新访问清单 12-6 中的代码，并在清单 14-1 中使用 hapi 重写它：

```
var Hapi = require('hapi');
var server = new Hapi.Server('localhost', 3000);

server.route({
  method: 'GET',
  path: '/users',
  config: {
    handler: function (request, reply) {
      var result = {};
      setTimeout(function () {
        result.users = [{
          first: 'Abraham',
          last: 'Lincoln'
        }, {
          first: 'Andrew',
          last: 'Johnson'
        }, {
          first: 'Ulysses',
          last: 'Grant'
        }];
        result.time = Date.now();

        return reply(result).header('X-Special-Header', 'MEAN Stack');
      }, 3000);
    }
  }
});

server.start();
```

**清单 14-1. hapi 路由示例**

在清单 14-1 中，`server` 是 hapi 服务器对象。要添加路由，我们执行 `route` 方法并传递一系列选项。`method` 和 `path` 用于设置路由器的匹配规则。`config` 选项是此路由所有其他配置的所在。`handler` 函数负责向客户端发送回复。`request` 是传入的请求，`reply` 是发送响应的函数。值得注意的是，`request` 对象不是内置的 Node `request` 对象。它是一个 hapi 特定的请求对象。Node 的 `request` 对象可以通过 `request.raw.req` 获取。

如果我们想缓存清单 14-1 中的响应呢？在 Express 中，开发者必须编写逻辑来设置正确的头部，以指示浏览器缓存...



在 Express 中，你需要为每个路由添加中间件来设置响应头。假设有数十个路由，每个路由的缓存需求各不相同，那么你就得为每个路由都添加一个类似 `setCache` 的中间件。而在 hapi 中，缓存头是通过路由配置中的一个设置来控制的。

```
server.route({
  method: 'GET',
  path: '/users',
  config: {
    handler: function (request, reply) {
      //...
    }
  },
  cache: {
    expiresIn: 30000
  }
});
```

**代码清单 14-2.** hapi 缓存头

## 路由配置

`cache` 选项提供了多种设置 `Cache-Control` 头的方法。在代码清单 14-2 中，我们将缓存头设置为在 30,000 毫秒后过期。此外，hapi 在发生错误时不会设置缓存头。而在 Express 中，你需要编写几行代码来移除缓存头，以避免缓存错误页面。请查阅 hapi 的 API 网站以获取[完整的配置选项列表](https://example.com)。一开始可能会觉得有点复杂，但在尝试实现任何大型功能之前，先查看文档，你可能会发现所需的一切只是为服务器或路由添加额外的配置。

再举一个例子，如果你想在将响应发送回客户端之前验证它呢？使用 Express，你需要编写额外的代码来实现这一点。而在 hapi 中，你只需更新路由配置以包含响应验证。除了响应，你还可以验证传入的头部、查询字符串和路由参数。你可以使用一个简单的函数来编写自己的验证规则，或者使用 hapijs 的另一个模块：[Joi](https://example.com)。

Joi 是一个独立的验证模块，可以直接集成到任何 hapi 路由配置中。它是一个非常强大且富有表现力的验证模块，与 hapi 配合得很好，因为任何暴露验证的配置都同时接受 Joi 配置对象和验证函数。以下是一个示例：

```
var joi = require('joi');

server.route({
  method: 'GET',
  path: '/users',
  config: {
    handler: function (request, reply) {
      reply(request.query);
    },
    validate: {
      query: joi.object().keys({
        page: joi.number().integer().min(1).max(10),
        number: joi.number().integer().min(1).max(5)
      })
    }
  }
});
```

### 代码清单 14-3. Joi 示例

在[代码清单 14-3](#)中，我们利用了路由配置的 `validate` 选项，并将 `validate.query` 设置为一个 Joi schema。通过设置 `validate.query`，hapi 将在运行处理函数之前验证查询字符串参数。如果验证失败，服务器将返回 400 状态码和一个表示验证错误的对象。用文字描述，这个 Joi schema 规定 `page` 是一个介于一到十之间的整数。它还规定 `number` 是一个介于一到五之间的整数。最后，`joi.object().keys()` 阻止查询字符串中的任何额外值。此路由只允许 `page` 和 `number`。Joi 的范围远超本书范畴，因此我们强烈鼓励你自行了解 Joi 和验证。

## 路由

在 Express 中，路由的注册顺序非常重要。第一个匹配的路由就是被执行的路由。也有可能为同一个路由注册多次。最后，在 Express 中，你可以先匹配模式 A 并执行一些代码，如果尚未发送响应，那么在响应客户端之前，可以再次匹配模式 B。

hapi 使用一个确定性的路由表。这意味着路由的注册顺序对其处理方式没有影响。在框架创建路由表时，路由会从最具体到最不具体进行排序。如果开发者尝试为同一个路由注册多次，hapi 会抛出错误。此外，路由器只会匹配*一个*路由并执行一个处理函数。这些路由处理上的差异从根本上消除了在 Express 应用中有时会发现且难以追踪的所有路由错误。

作为一个简单的特异性示例，假设我们有两个路由，路径分别为 "/file.txt" 和 "/file.{ext}"。在这两个路径之间，"/file.txt" 更具体，因为它没有参数，因此对 "/file.txt" 的请求将匹配第一个路由并使用该处理函数。"/file.txt" 将匹配这两个路径，但在这个例子中，更具体的路径会胜出，并且该处理函数将运行。

## 内置功能

Express 被标榜为轻量级且无固定模式，在大多数情况下确实如此。你可以将几乎任何模块接入 Express 生态系统，并构建一个功能完整的 Web 服务器。将服务器端缓存或用户认证等功能构建到 Express 服务器中，需要多个通常由不同开发者编写的模块，并且这些模块需要完美通信并保持同步。确实，许多 Express 应用程序都成功地做到了这一点。

相比之下，hapi 开箱即用就具备这些功能。hapi 拥有一个服务器端缓存引擎，可用于将值存储在内存中，或存储在 Redis 或 MongoDB 实例中。如果你的服务器需要认证，也有相应的配置选项。开发者需要做的就是为需要认证的特定路由配置认证。如果基本认证不够用，或者你想使用社交登录，有几个 hapi 插件可以添加更灵活的用户认证。这些插件大多数不需要开发，只需要额外的配置和插件模块。我们将在本章稍后讨论插件。

## 事件

hapi 常被称赞的一点是它“像 Node”。除了原生支持管道和流之外，还有许多服务器事件供开发者挂接。主要的服务器对象继承自 `Events.EventEmitter`。因为它使用的是核心 Node 对象，我们已经知道如何与之交互。

假设我们想记录服务器发送的每一个响应。在 Express 中，这需要一些开发工作和战略性地放置在路由器中的中间件函数。在 hapi 中，我们可以监听 `response` 事件并记录响应信息。

```
server.on('response', function (event) {
    console.log(event.info.received);
});
```

**代码清单 14-4.** 记录服务器事件

代码清单 14-4 使我们能够轻松地在 hapi 服务器向客户端发送响应后执行逻辑。还有其他几个事件可供监听，以提供日志记录和性能基准测试。这些事件不用于控制流或扩展 hapi 服务器的功能；它们只是观察服务器发出的不同事件的方式。

相比之下，扩展点提供了结构化的钩子，用于扩展和改变标准的 hapi 请求[生命周期](https://hapijs.com/api#request-lifecycle)。假设我们想在对特定网络资源进行身份验证后写入一个日志文件。在 Express 中，你需要添加另一个中间件函数来写入文件，然后执行 `next`。在 hapi 中，你可以使用 `onPostAuth` 扩展点。

```
server.ext('onPostAuth', function (request, next) {
    require('fs').writeFile('log' + Date.now() + '.txt', 'Successful authentication!', next);
});
```

**代码清单 14-5.** onPostAuth 扩展点

显然，这是一个刻意构造的例子，但它演示了扩展点的概念。这个函数在每次 `onPostAuth` 事件后写入一个文件。使用事件而不是中间件函数的好处在于，函数只需要编写和声明一次。无需去寻找可能使用等效 Express 中间件的不同位置。此外，只要正确设置了监听器，这个逻辑可以位于项目中的任何文件中，因为它是事件驱动的。

## 插件

hapi 拥有一个强大的插件系统。一个**插件**可以被视为服务器功能的一个捆绑子集。插件可以添加新的路由和额外的事件，并提供对

高级语言如Stylus和Less CSS——几乎是一个全新服务器所能做的一切。插件架构是hapi如此吸引人的原因之一。

插件允许服务器将其逻辑分散在多个不同的模块中。让我们用一个例子来展开说明。假设你正与一个团队合作构建一个新的Web服务器。你想要暴露数据，例如一个智能手机原生应用可以消费的API，但同时你也想要提供一个网站服务。使用Express来实现这一点可能会很复杂。

API团队会希望以一种方式设置路由，而前端开发者则希望以另一种方式设置。前端团队会希望添加用于编译模板和提供静态资源的中间件功能，而这些是API所不需要的。同时兼顾在同一个服务器上工作的两个团队的需求和设计将会是一项考验，并且需要大量的协调工作。

使用hapi，每个团队将使用各自独立的hapi插件进行开发，然后单个服务器将加载这两个插件。这将允许每部分代码彼此完全隔离，并且耦合度极低。每个插件可以注册自己的路由、监听事件、拥有自己的cookie管理状态，并拥有自己的其他插件依赖项列表。涵盖插件能做的所有事情超出了本书的范围，但[完整文档可以提供关于使用插件的更好见解。](http://example.com)

## 插件示例

让我们扩展清单14-1，添加一个插件模块，该模块将在网页上显示JSON数据。为了保持示例简单，我们将避免使用任何模板语言，而是手动构建HTML，并将响应发送回客户端。

```
//...original code from Listing 14-1 omitted
var plug = {
  register: function (plugin, options, next) {
    plugin.route({
      method: 'GET',
      path: options.prefix + '/view',
      config: {
        handler: function (request, reply) {
          request.server.inject({
            url: '/users'
          }, function (res) {
            var users = res.result.users;
            var view = '<!DOCTYPE html><html lang="en"><body><h1>User Output</h1><table>';

            for (var i = 0; i < users.length; i++) {
              var user = users[i];
              view += '<tr><td>' + user.first + '</td><td>' + user.last + '</td></tr>';
            }

            view += '</table></body></html>';
            reply(view);
          });
        }
      }
    });
```

```
    next();
  }
};
plug.register.attributes = {
  name: 'viewer',
  version: '1.0.0'
};
```

```
server.pack.register({
  plugin: plug,
  options: {
    prefix: '/users'
  }
}, function (err) {
  if (err) {
    console.log(err);
  } else {
    server.start();
  }
});
```

**清单14-6. 插件示例**

这起初看起来有点复杂，但让我们来逐步解析它。我们创建了一个名为`plug`的变量，该变量有一个带有附加属性的`register`函数。属性必须包含`name`和`version`键。这几项就是一个JavaScript对象被视为插件所需的一切。`register`函数是进入该对象的主入口点，大部分逻辑都将位于此处。`register`接受三个参数：`plugin`、`options`和`next`。`plugin`是插件接口，具有与服务器对象相同的许多方法，包括`route`。`options`对象是任何插件特定选项所在的位置；在这个例子中，我们提供了一个`prefix`值，我们用它来设置路由注册的路径值。`next`是该方法必须调用的回调函数，以将控制权返回给应用程序并完成注册过程。

在`handler`中，我们使用了`server.inject`。`inject`方法模拟了一个HTTP请求，而无需实际建立socket连接。它对于测试非常有用，在这个例子中，它用于从另一个路由请求信息以获取用户列表。在获得用户列表后，我们只需创建一个HTML字符串，并通过`reply`响应客户端。

要注册插件，我们使用`server.pack.register`。`server.pack`是一个宏大的概念，无法在本书中详细讨论。简而言之，每个服务器都分组到一个服务器包中。这使你可以为多个hapi服务器同时注册相同的插件和路由。它还允许开发人员将服务器包视为单个对象，从而可以一步启动和停止一个服务器包。有关服务器包的完整说明，请查阅[hapi文档](http://hapijs.com/api)。

如果你启动一个Web浏览器并导航到"/users"和"/users/view"，你应该会看到不同的响应。这个插件让我们能够分离两个路由，并从其中一个提供视图，从另一个提供JSON。理想情况下，插件应该放在另一个文件中，以帮助保持主服务器逻辑的整洁。使用这样的插件可以实现更高的代码模块化和重用性。有许多预先构建的插件可用于日志记录、API文档处理以及处理用户代理等任务。

# 总结

以上是对hapi所提供的一些功能的快速概览。与Express相比，它构建服务器的方式完全不同，这使得学习它很有趣。许多完整Web服务器需要的功能都直接内置于hapi中。如果没有内置，也有大量可用的插件来填补大部分缺失的功能。hapi中的路由逻辑是独特的，因为顺序并不重要。hapi还使用事件来提供扩展点，以扩展和改变服务器行为。

无论你使用hapi还是Express，我相信在学习了这几章之后，你会明白为什么大多数人避免尝试仅使用核心模块来构建所有这些功能，而是投入时间学习一个框架。

[4] 完全公开：两位作者目前都受雇于沃尔玛，并为hapi及其依赖的多个模块做出了贡献。

# AngularJS 概述

我们将要探索的最后一项MEAN技术是AngularJS。Angular是一个用于创建单页应用程序（SPA）的前端框架。与其他MEAN技术一样，Angular是开源的，可以在你的应用程序中自由使用。

Angular由Miško Hevery和Adam Abrons于2009年在一家名为Brat Tech LLC的公司创建。Angular最初是作为一项在线JSON存储服务的一部分而设计的，但这个概念被放弃了，Angular被发布到了开源世界。Adam Abrons此后离开了该项目，但Hevery继续从事该项目的工作。Hevery被Google聘用，而Google现在与Angular关系密切。

## 单页应用程序

**单页应用程序**代表了网页设计的最新演进。SPA背后的理念是，所有必要的代码可以在单次页面加载中获取，或者根据需要动态加载。当用户与应用程序交互时，数据通过Ajax请求发送到服务器并从服务器接收。这提供了比页面重新加载更流畅的用户体验，并且更类似于原生应用程序。现在我们将探讨SPA的一些常见特征：

- Ajax：Ajax请求在SPA中是必不可少的。根据定义，SPA应该只经历一次页面加载。所有其他请求都应通过Ajax或其他实时通信机制（如WebSockets）进行。
- 模板化：将HTML混入服务器返回的JSON数据被认为是不良实践，因此模板语言经常在SPA中使用。这些语言通常用JavaScript实现，能够将JSON数据转换为可以注入到DOM中的HTML字符串。
- 路由：客户端路由类似于你在Express章节中学到的服务器端路由。路由允许你在不需要页面加载的情况下选择应用程序的某一部分进行显示。在SPA中，客户端路由通常指定在URL的**片段标识符**中，即哈希符号之后的部分。例如，在URL http://domain.com/#/team中，客户端路由器将处理#之后的/team部分。

如前所述，SPA的最大优势是由于减少了页面加载和服务器事务量，从而提高了性能和更流畅的用户体验。然而，SPA也有缺点，其中最大的两个是浏览器历史记录的本质和搜索引擎优化（SEO）。浏览器历史记录可能会有问题，因为“后退”和“前进”按钮是基于页面加载的。幸运的是，只要应用程序能够根据标识符重新创建页面，使用URL片段标识符就可以保持预期的行为。

SPA对搜索引擎来说可能很棘手，因为搜索引擎在爬取过程中历史上并不执行JavaScript代码。然而，搜索引擎正在开始追赶；Google已经开始通过执行JavaScript来爬取带有片段标识符的页面。也可以实施其他技术。一个常见的例子是，在服务器端检测到页面是由搜索引擎请求的，然后使用无头浏览器（没有GUI的浏览器）渲染页面并返回一个“正常”页面。在这种情况下必须谨慎，因为它速度较慢，而搜索引擎通常将页面加载时间纳入其排名算法中。

## SPA框架

有许多流行的框架用于创建SPA，每个框架都有不同的优缺点。而且，正如技术的许多方面一样，用户往往对他们选择的框架充满热情。本书重点介绍Angular，因为它传统上是

在MEAN栈的语境下我们会提到它，但这并不意味着我们要贬低其他替代方案。我们建议你查看每一个框架，评估其[优势与不足](strengths and weaknesses)，并了解谁在用它。例如，若想查看使用Angular设计的产品列表，可以访问[builtwith.angularjs.org](builtwith.angularjs.org)。

以下是Angular的一些热门竞争对手：

- [Backbone.js](Backbone.js)是一款资深的前端框架，久经考验，可能是最常用的SPA框架。它简单、灵活，提供了许多可用的小构件。遗憾的是，Backbone的简洁性往往要求用户编写大量代码来填补缺失的部分。
- [Ember.js](Ember.js)是一款极具"主见"的框架。它通常只支持一种解决问题的方式，即所谓的"Ember之道"。这既可视为该框架的优势，也可视为其劣势，具体取决于你的观点。Ember官网列出了[令人印象深刻的框架用户名单](impressive list of framework users)。
- [Polymer](Polymer)是谷歌推出的另一款产品，专注于[Web组件](Web Components)——这是一组新兴技术，让Web开发者能够创建自定义HTML元素。遗憾的是，这些技术尚未达到生产就绪的标准，使得Polymer处于polyfill（填充）的地位。尽管如此，在[基于Web组件的SPA](Web Component-based SPAs)领域，仍然有一些有趣的工作正在进行。

那么，与这些竞争对手相比，Angular的表现如何呢？它被认为是最容易学习的框架之一，拥有庞大的社区和谷歌领导的核心团队。在Angular中，只需编写一些自定义HTML就能完成很多工作。不过，一个常被提及的缺点是它为你做了太多事情，而你却并不真正理解背后发生了什么。此外，似乎没有证据表明它被用于谷歌的任何旗舰产品，而且即将推出的Angular 2.0预计不会有简单的升级路径，这意味着[完全重写应用可能指日可待](full application rewrites could be on the horizon)。

## 模型-视图-控制器架构

Angular将模型-视图-控制器（MVC）架构引入了前端Web应用。在MVC方法下，模型在数据层面定义应用，独立于用户界面。在Angular中，模型就是简单的普通JavaScript对象。视图是模型数据的视觉呈现。Angular允许你使用HTML以及被称为*指令*的扩展作为视图创建的模板语言。控制器组件负责对模型的数据进行操作。在Angular应用中，控制器是通过`controller()`方法注册到应用中的JavaScript函数。[图15.1](#)展示了通用MVC流程的工作原理。请注意，此图并非专门针对Angular。

![](img/0ca996f5fd0375fc118091628c3c7a87_212_0.png)

Angular最知名的特性之一是它在模型和视图之间的双向数据绑定。这大大简化了在两个应用组件之间保持数据同步的问题。**双向数据绑定**意味着当用户更新视图时，模型数据会自动更新以反映变化。同样，如果控制器修改了模型，视图也会随之更新。

## 获取Angular

要在你的应用中包含Angular，请使用清单15-1所示的`<script>`标签。该标签从谷歌引入了Angular 1.2.23的压缩版本。你也可以通过从URL中省略`.min`来下载非压缩版本。在生产环境中应始终使用压缩版本，因为非压缩代码要大好几倍，会导致下载时间增加，从而造成更大的页面加载延迟。

 INCLUDEPICTURE "http://google.com" \* MERGEFORMAT  INCLUDEPICTURE "http://google.com" \* MERGEFORMAT ```

<script src="//ajax.googleapis.com/ajax/libs/angularjs/1.2.23/angular.min.js"></script>
```

**清单 15-1.** 导入Angular的`<script>`标签示例

请注意，库URL上没有指定协议。谷歌会通过HTTP或HTTPS提供Angular库。通过不指定协议，浏览器将使用页面当前使用的任何协议来加载该库。这可以防止当页面使用一种协议而Angular使用另一种协议时出现潜在的[混合内容](mixed content)错误和警告。需要注意的是，这种写法在本地不通过服务器运行代码时（通过`file://`协议）会失效。如果你不在服务器上运行代码并遇到"找不到文件"的错误，请尝试在URL前面加上`http`或`https`。

## 从源码构建

Angular项目在GitHub的[angular/angular.js仓库](angular/angular.js repo)中维护。如果你有兴趣，可以向该仓库提交拉取请求来为项目做贡献；但是请注意，搭建Angular开发环境需要Java、Grunt（一个任务运行器，将在[第21章](Chapter 21)中介绍）、Bower（一个客户端包管理器），以及git和Node。

在[安装所有必备软件](installing all the prerequisite software)之后，你可以使用清单15-2所示的一系列命令来构建Angular。第一条命令从GitHub克隆仓库。或者，你也可以先fork该仓库，然后克隆你的fork并添加官方仓库作为远程仓库。`npm install`和`bower install`命令用于安装所有依赖项。最后一条命令`grunt package`用于构建Angular。

```
git clone "git@github.com:angular/angular.js.git"
cd angular.js
npm install
bower install
grunt package
```

**清单 15-2.** 克隆和构建Angular的命令

运行`grunt package`后，可以在`build`目录中找到构建输出。该目录应包含以下文件和文件夹：

- `angular-<version>.zip` — 完整的zip文件，包含所有发布构建产物
- angular.js — 非压缩的Angular代码
- angular.min.js — 压缩的Angular代码
- angular-scenario.js — Angular端到端测试运行器
- docs — 包含运行Angular文档网站所需所有文件的目录
- docs/index.html — 主文档页面
- docs/docs-scenario.html — 文档应用的端到端测试运行器

## 发布版本

与npm生态系统不同，Angular不遵循语义化版本控制。在Angular中，破坏性变更会出现在小版本之间。它尽量避免破坏性变更，但这并非总能实现；例如，当发现潜在安全问题时。有关升级到特定版本的说明和破坏性变更的详细信息，请参阅[迁移文档](#)。

Angular生态系统的一个有趣方面是其新版本的命名约定。发布版本的代号由两个看似随意的单词组成，用连字符连接。示例版本名称包括finicky-pleasure、timely-delivery、increase-gravatas和temporal-domination，分别对应版本1.2.22、1.2.0、1.1.0和1.0.0。

作为前端框架，Angular必须处理诸如遗留浏览器等问题。遗留浏览器本质上指的是Internet Explorer 6、7和8。目前，Angular的Travis CI服务器配置为针对IE9、10和11运行测试。教育培训涵盖。Angular从1.2版本开始不再支持IE6和7。Angular 1.3及更高版本不再支持IE8。

## Angular "Hello World"

清单15-3展示了一个简单的Angular应用，该应用利用了数据绑定。此页面包含一个`<input>`元素，其ng-model属性设置为"example"。ng-model是Angular指令的一个例子。Angular指令是[第17章]的主题，是在Angular应用（或Angular核心库）中定义的HTML语法扩展。该指令表示此输入的值与模型的example属性绑定。

接下来，注意内容为{{example}}的`<div>`元素。在Angular应用中，HTML可用作模板。双开双闭花括号用于绑定JavaScript表达式；因此，本示例将`<input>`元素的值绑定到`<div>`元素的内容。

剩下的唯一任务是确定页面如何被定义为Angular应用。注意`<html>`元素上的ng-app指令。该指令将`<html>`元素及其子元素标记为Angular应用。在本例中，这个应用被恰当地命名为"app"。

最后，注意`<body>`末尾附近的两个`<script>`标签。第一个脚本导入Angular代码库，而第二个脚本使用angular.module()方法基于我们的HTML定义了一个Angular模块。module()的第一个参数是模块名称，必须与ng-app指令的值匹配。module()的第二个参数是当前模块导入的模块数组。在本例中，我们的简单模块没有任何依赖项。module()返回新创建的模块。请注意，理想情况下，JavaScript代码应该分离到另一个文件中。为了这个基本示例的目的，它留在了HTML中。

```
<!DOCTYPE html>
<html lang="en" ng-app="app" class="no-js">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Data Binding Example</title>
  </head>
  <body>
    <input ng-model="example" />
    <div>
      {{example}}
    </div>
    <script src="//ajax.googleapis.com/ajax/libs/angularjs/1.2.23/angular.min.js"></script>
    <script>
      'use strict';
      var app = angular.module('app', []);
    </script>
  </body>
</html>
```

清单 15-3. 利用数据绑定的Angular应用示例

我们的应用实际运行示例如[图15.2]所示。在本例中，文本



"哇，绑定功能太强大了！" 这段文字已输入到文本框中。与此同时，`<div>` 的内容也同步更新了。这个功能实时演示起来效果非常震撼，因此我们鼓励您亲自尝试实现这个示例。

![数据绑定实战](img/0ca996f5fd0375fc118091628c3c7a87_217_0.png)

图 15.2. 数据绑定实战

当然，这是一个非常简单的示例。它没有定义任何控制器、自定义指令、路由，或 Angular 应用中常用其他组件。这些功能将在后续章节中详细探讨。

# 总结

本章介绍了 AngularJS 生态系统以及一些相关主题，例如 MVC 架构和单页应用。我们展示了如何将 Angular 添加到网页中，以及如何从源代码构建它。在接下来的几章中，我们将继续深入探讨 Angular，详细研究数据绑定、指令、控制器和路由等概念。在彻底探索完 Angular 框架后，我们将为示例人力资源应用添加一个前端界面。

[5] 图片由 Regis Frey 通过 Wikimedia Commons 提供。

## 数据绑定

在编程中，**数据绑定** 是指程序的数据层与其关联的视图层之间数据的自动同步。回想一下本书中的一些数据库代码：我们会在数据库中执行查询，将结果收集到一个变量中，然后将 JSON 数据发送给请求的客户端。如果我们再进一步，显示层会使用这个 JSON 数据向用户展示数据库查询结果。这可以被视为单向数据绑定；来自数据库的数据*绑定*到了我们展示给用户的视图上。就我们的目的而言，应用程序将是一个网页，而视图将是 HTML。

Angular 的一个标志性功能是其内置的 **双向数据绑定系统**。这使得 Angular 开发者能够用极少的 UI 代码创建功能丰富、交互性强的 Web 应用程序。（事实上，本章稍后部分，代码清单 16-1 将展示一个无需任何 JavaScript 代码即可实现的复杂界面。）在本章中，我们将讨论单向和双向数据绑定，并通过一些 Angular 代码示例来演示如何利用这一强大功能。

## 单向数据绑定

单向数据绑定在某些特定应用中很有用。假设你有一个在线商店的网页，那么在显示页面之前，HTML 只需要从数据库获取一次数据。初次加载后，用户无法交互或更改数据库中的数据，只能通过 HTML 进行查看。单向数据绑定更容易实现，代码复杂度也更低。大多数单向数据绑定无需框架支持即可实现；然而，大多数应用程序都需要接受用户输入，并且视图层需要根据用户的交互进行更新。

单向数据绑定有几个局限性。一旦数据被加载并且视图渲染完成，视图就是静态的。即使模型在五分钟之后发生变化——例如通过 Ajax 调用——视图也不会自动更新。开发者必须重置数据模型，清除代表数据的 HTML，并重新创建 DOM 中变化的部分来更新视图。对于一个非常小的 Web 应用程序来说，这听起来可能是工作量不大，但一旦涉及到多个页面、不同的用户控件和输入机制，手动管理这些数据变化很快就会演变成维护和调试的噩梦。

到目前为止，我们一直只关注数据单向流动，从服务器到视图。同样，数据也需要从用户流回服务器，并在数据流动过程中保持视图更新。假设你正在使用一个简单的待办事项 Web 应用。当你添加一个新任务时，你期望视图和服务器上的数据库都能同步更新。使用单向数据绑定，所有这些更新都需要开发者来完成。工作流程如下：

- 1. 用户填写一个简短的表单来添加新任务，并按下“添加”按钮。
- 2. 内存中的 JavaScript 数组将被更新，以包含这个新对象。
- 3. 视图需要被更新，以在数组中包含新项目。
- 4. JavaScript 对象将被发送到 Web 服务器以更新数据库。

开发者必须负责确保数据在此工作流中正确流动，并处理可能出现的任何错误。到目前为止，我们一直只关注添加操作，那删除呢？这会更难，因为需要在视图和底层对象模型之间人为地建立一种关系。请记住，HTML 只是一个字符串；它不知道自己绑定到了内存中的哪些 JavaScript 对象。

为了实现这种程度的交互性，开发者必须严重依赖 DOM 事件和 DOM 操作。回到我们的商店示例，如果用户想将货币显示从美元切换为欧元呢？这就需要在下拉菜单上为 change 事件添加事件监听器。同时还需要为页面首次加载时的一些边缘情况添加条件逻辑。这催生了社区术语“jQuery 意面代码”。当需要手动使用 jQuery 编写大量事件处理器和 DOM 操作来创建响应式用户界面时，就会用到这个术语。

理想情况下，Web 开发者应该能够使用一个框架，让他们可以对原生 JavaScript 对象进行操作，同时视图会随着模型的更改而自动更新。同样，对视图的更改也会更新其绑定的对象。这样开发者就可以专注于编写业务逻辑和优秀的用户界面。双向数据绑定赋予了 Web 开发者这样的能力。

## 双向数据绑定

双向数据绑定解决了数据模型和视图同步的问题。它允许开发者直接操作绑定的数据，而无需关心保持 DOM 同步。例如，假设你有一个包含名和姓两个输入框的注册表单。使用双向数据绑定，当用户输入信息时，底层的数据模型会与视图保持同步。无需任何 onChange 或 onKeyUp 事件来保持数据层与视图的同步。

假设用户界面的一个要求是显示“全名”，即将名和姓拼接在一起。使用双向数据绑定，开发者可以将 firstName + lastName 的结果绑定到一个 span 标签上。这样就可以专注于构建这个计算值，而无需担心当任一部分姓名发生变化时，如何保持 DOM 更新。

如前所述，Angular 的主要特性之一就是双向数据绑定。它提供了一个框架来绑定简单值和复杂值、集合、函数以及 Angular 表达式。它还包含许多内置函数，这些函数可以与绑定值结合使用来控制数据的显示，这对于区域感知的格式化非常有用。

### 一个简单的示例

展示双向数据绑定实用性最好的方式是通过一个例子。代码清单 16-1 是一个简单的注册表单，它接入了 Angular 的数据绑定系统。

```
<!DOCTYPE html>
<html lang="en" ng-app>
  <body>
    <input type="text" ng-model="firstName" placeholder="first name"/>
    <input type="text" ng-model="lastName" placeholder="last name">
    <h2>Gender {{gender}}</h2>
    <input type="radio" ng-model="gender" value="male"
      ng-click="style={color:'yellow'}">Male
    <input type="radio" ng-model="gender" value="female"
      ng-click="style={color:'orange'}">Female
    <br />
    <h2 ng-style=style>Welcome {{firstName + ' ' + lastName}}</h2>
    <button ng-disabled="!(firstName.length && lastName.length)"
      ng-click="signup()">Sign Up</button>
    <script src="//ajax.googleapis.com/ajax/libs/angularjs/1.2.16/angular.js"></script>
  </body>
</html>
```

**代码清单 16-1.** 简单的 Angular 数据绑定

这少量的 HTML 代码赋予了我们非常强大的功能，而我们甚至还没有编写任何 JavaScript。你首先应该注意到，这就是普通的 HTML。Angular 没有引入新的标记语言或需要记忆的陌生语法——只是带有属性的纯 HTML。让我们逐行检查标记，解释如何使用这些 HTML 属性。



## 注意：ng 的含义

在 Angular 应用程序中，你会看到以 "ng" 开头的属性或标签。这表明该属性或标签是 Angular 特有的，你可以通过它在 Angular 官方网站上查找相关文档。

## 标记说明

你应该首先注意到 `html` 标签上的 `ng-app` 属性。这个属性非常重要，但常常被忽视。整个 Angular 应用程序只需要使用一次这个属性。`ng-app` 属性用于指示 Angular，`html` 元素是此应用程序的根元素。通常，你会在 `html` 或 body 标签上看到这个属性。如果你忘记使用它，所有 Angular 代码都不会执行。

两个文本框输入都附加了 `ng-model` 属性。`ng-model` 是在 Angular 中建立双向数据绑定的特定关键字。`ng-model` 属性指示 Angular 绑定到名为 `firstName` 和 `lastName` 的可用作用域中的值。

在整个标记中，你可以看到使用 `{someValue}` 引用的值。这就是你显示/使用数据绑定值的方式。如果你与视图交互，你会看到 `h2` 元素随着 `firstName`、`lastName` 和 `gender` 的更改而动态更新。注意，即使 `gender` 绑定到单选按钮列表，绑定仍然正确工作。当你切换不同的单选按钮选项时，绑定的值会正确更新。

另一个新概念是 `ng-click` 指令。这是使用 Angular 将点击事件附加到 DOM 节点的一种方式。不过，你会注意到 `ng-click` 的值不是真正的 JavaScript；它被称为 Angular 表达式。Angular 表达式是一种类似 JavaScript 的代码片段，但有一些重要的区别。首先，Angular 表达式中使用的上下文是一个作用域对象，而不是全局的 window 对象。其次，开发者在处理可能为空或未定义的值时，可以享受更安全的处理方式。最后，表达式完全不具备控制流的概念。许多 Angular 属性既可以设置为表达式，也可以设置为值，因此理解如何使用它们是值得的。

当点击每个单选按钮时，我们根据选择设置 `style` 的值。`style` 值与 `ng-style` 指令一起使用，以控制 `h2` 名称标签的显示方式。这是一个简单的演示，说明设置不同的值如何可以控制视图层。`h2` 名称标签中使用的第二个功能显示了 Angular 表达式的结果。使用表达式，我们可以在没有任何额外逻辑的情况下，显示 `firstName` 加 `lastName` 的计算结果，并在任一值更改时保持显示同步。

最后，我们在按钮标签上使用另一个 Angular 指令：`ng-disabled`。此指令根据表达式切换元素的启用状态。在此示例中，按钮保持禁用状态，直到用户输入了名字和姓氏。我们还设置了另一个 `ng-click` 属性为 `signup()`。这目前没有任何作用，但我们会在本章后面的下一个示例中保留它。

# 总结

回顾清单 16-1 应该阐明了关于 Angular 双向数据绑定的几个关键点。我们能够在不编写任何 JavaScript（暂时）的情况下实现高度精美的前端效果。仅使用 jQuery 或原生 JavaScript 来实现这种级别的响应性将是一项巨大的工程。需要创建几个事件处理程序来响应文本和单选按钮的变化，还需要编写几行代码来管理 h2 标签的颜色变化，以及一两个函数来切换提交按钮的启用状态。双向数据绑定让我们更多地关注数据和数据交互，而不是确保 DOM 与我们的数据层保持同步。

## 技术概述

让我们更深入地了解数据绑定在 Angular 中*如何*工作。从根本上说，数据绑定由与作用域对象（也称为 Angular 上下文）关联的函数组成。**作用域对象**是使用 Angular 构造函数创建的 JavaScript 对象，用作 HTML 标记的模型。在一个完整的 Angular 应用程序中，作用域对象通过控制器实例化并提供给视图，但在清单 16-1 中，我们使用的是框架自动创建的全局作用域。作用域对象的规则与原生 JavaScript 作用域规则类似。例如，如果一个页面有多个嵌套的 Angular 作用域对象，内部对象可以看到并访问包含它的外部作用域对象。

## $watch

每次你将数据绑定到 UI 时，Angular 会自动在所谓的 `$watch` 列表中创建一个新的 `$watch` 条目。可以将 `$watch` 视为一个非常小的事件发射器，当底层数据模型或 UI 发生变化时，它可以发送和接收事件。UI 中绑定的每个属性都会自动创建一个 `$watch` 条目。`$watch` 值和 `$watch` 列表在下一个主题——摘要循环中使用。

## 摘要循环

每当浏览器事件（点击、更改、按键）应由相关的 Angular 上下文处理时，**摘要循环**就会运行。这意味着循环会运行很多很多次。当用户在 `firstName` 输入框中输入一个 **A** 时，摘要循环就会运行。摘要循环的功能相对简单。它遍历 `$watch` 列表中的每个项目，并经过几个简单的步骤。首先，它查询对象的当前值。然后，它询问该值自上次摘要循环运行以来是否发生了变化。如果任何 `$watch` 项目报告了变化，则会运行另一个摘要循环。循环会继续运行，直到没有 `$watch` 项目报告变化。此时，DOM 会根据对象层的所有更改进行更新。

在讨论摘要循环时，重要的是要记住 JavaScript 是单线程的。因此，当摘要循环开始时，Angular 接管了线程的控制权，这意味着在循环期间，用户的输入会被暂时阻塞。出于本书范围的考虑，关于双向数据绑定工作原理的这个解释已被大幅简化。大多数情况下，你不需要理解数据绑定工作原理的细节，只需要知道如何使用它即可。

## 简单的控制器

清单 16-1 展示了使用 Angular 实现双向数据绑定的一些强大功能；然而，没有真正的应用程序是这样构建的。Angular 本质上是一个 MVC 框架，而清单 16-1 中只有一个视图。我们将重写这个示例，并引入一些新概念，这些概念将构成后续 Angular 章节的一些基础。

在清单 16-1 中，你会注意到没有编写任何 JavaScript。但假设我们希望点击按钮向服务器发送 Ajax 请求。目前，这段代码无处可放。这是因为 Angular 应用程序应该在其背后拥有控制器。

现在，让我们保持与清单 16-1 完全相同的 HTML，并添加使控制器正常工作所需的 JavaScript 代码：

```
var app = angular.module('app', []);
app.controller('main', ['$scope', function($scope) {
  $scope.firstName = $scope.lastName = undefined;
  $scope.gender = 'female';
  $scope.style = {color:'orange'};

  $scope.signup = function () {
    var person = {
      first: $scope.firstName,
      last: $scope.lastName,
      gender: $scope.gender
    }
    console.log(person);
  };
}]);
```

**清单 16-2.** 一个简单的控制器

在尝试将此 JavaScript 连接到清单 16-1 的 HTML 之前，你需要对 HTML 进行两处微小的更改。首先，在 `html` 标签上将 `ng-app` 更改为 `ng-app=app`。这指示 Angular 我们正在构建的应用程序名为 `app`，它需要实例化一个新的 app 对象。第二个 HTML 更改是在 body 标签上添加 `ng-controller="main"`。这指示 Angular，body 标签内的所有元素都应使用 `main` 控制器作为其作用域上下文。现在你可以将清单 16-2 中的代码复制到清单 16-1 的 HTML 文件中，应用程序应该会继续正常运行。如果你设置正确，性别默认值应为 "female"，并且当点击"注册"时，信息会记录到控制台。

在功能上，与清单 16-1 相比，一切都保持不变；然而，通过添加一个控制器，我们现在可以更好地控制 body 标签内使用的作用域对象。数据绑定应该仍然像清单 16-1 中那样正常工作。传递给函数的 `$scope` 参数是此控制器的上下文对象。当数据和函数绑定到此控制器时，它们会引用这个 `$scope` 对象。下一章将专门介绍控制器的使用，因此如果你感到有点困惑，不用担心。现在，只需知道它创建了一个新的 Angular 上下文，而不是使用全局上下文，并且我们可以更好地控制其功能。控制器还会

提供了一个编写业务逻辑的地方。

## 与列表的数据绑定

使用数据绑定时，最出色的功能之一就是处理列表的便捷性。清单 16-3 是一个简单的列表查看器和编辑器：

```html
<html lang="en" ng-app="app">
  <body ng-controller="main">
    <input type="text" ng-model="firstName" placeholder="first name">
    <input type="text" ng-model="lastName" placeholder="first name">
    <button ng-disabled="!(firstName.length && lastName.length)" ng-click="add()">Add</button>
    <table>
      <tr ng-repeat="p in presidents">
        <td>{{p.first}}</td>
        <td>{{p.last}}</td>
        <td><button ng-click="$parent.remove(p)">Remove</button></td>
      </tr>
    </table>
    <script src="//ajax.googleapis.com/ajax/libs/angularjs/1.2.16/angular.js"></script>
    <script>
      var app = angular.module('app', []);
      app.controller('main', ['$scope', function($scope) {
        $scope.firstName = $scope.lastName = '';

        $scope.presidents = [{
          first: 'Abraham',
          last: 'Lincoln'
        }, {
          first: 'Andrew',
          last: 'Johnson'
        }, {
          first: 'Ulysses',
          last: 'Grant'
        }];

        $scope.add = function () {
          $scope.presidents.push({
            first: $scope.firstName,
            last: $scope.lastName
          });

          $scope.firstName = $scope.lastName = '';
        };

        $scope.remove = function(president) {
          $scope.presidents.splice($scope.presidents.indexOf(president), 1);
        }
      }]);
    </script>
  </body>
</html>
```

**清单 16-3.** 列表数据绑定示例

与清单 16-2 中的控制器类似，有一个 $scope 对象被传入控制器函数。在这个示例中，我们再次挂载了 `firstName` 和 `lastName`。我们还挂载了一个总统列表以及两个用作歼事件处理器的函数。请记住，视图使用 $scope 对象来绑定此控制器上下文中的值和函数。

此示例将显示一个总统表格，并带有按钮以便从列表中删除他们。第一个使用的新功能是 `ng-repeat` 指令。其中的 HTML 及其所有子元素将为 Angular 上下文中 `presidents` 集合（即我们控制器中的数组）的每个项目重复一次。`ng-repeat` 还能实现一些其他功能，我们鼓励你在 [Angular 文档](https://docs.angularjs.org/api/ng/directive/ngRepeat)中阅读更多相关内容。

另一个新功能是 `$parent.remove`。请记住，Angular 应用程序中的每个 DOM 元素都有一个与之关联的作用域。在 ng-repeat 指令内部，作用域是集合中的当前项。在本示例中，它是一个包含名字和姓氏的对象。`remove` 函数位于上一层作用域的 `main` 控制器中。回想一下，作用域是嵌套的，就像标准 JavaScript 中的变量一样。`$parent` 是指向直接父作用域的指针，即 `main` 控制器对象，其中定义了 `remove` 函数。我们希望将 `p`（集合中的当前项）传入 `remove` 函数，以便事件处理器知道要从绑定的集合中移除哪个对象。

添加事件处理器创建了一个带有 `first` 和 `last` 键的新对象，然后将该对象添加到 `presidents` 集合中。一旦这发生，`$digest` 循环就会启动，注意到 `presidents` 集合已发生变化，然后重新绘制新项目。这会向 DOM 表格添加一行。移除项目与添加一样简单。在标记中，我们表明希望将当前项传入 `remove`。然后我们使用一些标准数组方法来定位该项，再用 `splice` 将其从数组中移除。这会触发另一个 `$digest` 循环，表格被重新绘制以匹配数组的内容。如果你想尝试更多示例，试着对总统列表进行排序，看看保持 DOM 与排序同步是多么容易。

仅使用 JavaScript 和 jQuery 来实现这种级别的功能将需要更多行代码，而且会非常脆弱。例如，添加排序将是一个非平凡的更改。开发人员必须么对数据层进行排序并手动重新绘制 DOM，要么对 DOM 进行排序并手动更新数据层。这两种方法都容易出现错误，并且很快变得难以维护。使用 Angular 的双向数据绑定系统，处理列表变得很容易，添加新功能也是小菜一碟。说到食物，想想你现在可以在自己的项目中替换掉多少行 jQuery 意大利面条式代码吧！

# 小结

在本章中，我们初步探索了使用 Angular 进行双向数据绑定。处理 DOM 并使其与数据保持最新可能是一项令人沮丧且枯燥的任务。使用支持双向数据绑定的框架可以让开发人员专注于他们擅长的领域：处理和操作数据。DOM 可以说是顺带受益的。对底层对象模型的更改会自动更新绑定的 DOM 对象。

我们通过讨论 `$digest` 循环如何遍历所有 `$watch` 对象来确定自上次循环运行以来哪些值已发生变化，从而对 Angular 中数据绑定的工作原理进行了高层次的概述。请记住，由于 JavaScript 是单线程的，`$digest` 循环阶段会从浏览器手中夺取控制权并阻止用户输入。在 Angular 确定了上下文中的更改并刷新 DOM 之后，浏览器重新获得控制权。

我们创建了一个更复杂的示例，展示了一个非常常见的用例：列表管理。我们的示例演示了如何使用控制器向列表中添加和移除项目。如果没有数据驱动框架，编写同样的应用程序将是一项非常繁琐的工作。列表示例，我们相信，已经突出了在数据层操作的能力，以及让 DOM 自动更新而无需任何开发人员干预的必要性。

我们还介绍了 Angular 控制器的概念，并解释了为什么要使用它们。它们是控制 DOM 特定部分上下文的方式，而不是通过使用全局 Angular 上下文来实现。如前所述，未来有一章专门讨论控制器；我们只是对使示例工作所需的内容进行了高层次的概述。

# 第 17 章

## Angular 指令

本章继续探索 Angular 的核心原理。具体而言，本章重点讨论指令，它们是 Angular 扩展 HTML 语法的方式。Angular 附带了许多内置指令，但开发人员也可以定义自定义指令以满足其应用程序的需求。本章将解释如何使用指令，以及如何创建你自己的指令。

## 概述

让我们从准确定义什么是**指令**开始。根据[官方文档：](https://docs.angularjs.org/guide/directive)

> 从高层次来看，指令是 DOM 元素上的标记（例如属性、元素名称、注释或 CSS 类），它们告诉 AngularJS 的 **HTML 编译器**（$compile）将指定的行为附加到该 DOM 元素，甚至转换该 DOM 元素及其子元素。

换句话说，指令是 Angular 解释的额外标记，用于扩展 HTML 的默认行为。指令可以指定为自定义 HTML 元素、属性、类或注释。例如，给定一个名为 ngFoo 的虚构指令，清单 17-1 展示了它可以作为元素、属性、类和注释使用的方式：

```
<ng-foo>Here is it used as an element</ng-foo>

<div ng-foo="Here is it used as an attribute"></div>
<div class="ng-foo">Here it is used as a class</div>
<!-- Here it is used as a comment -->
<!-- directive:ng-foo -->
```

**清单 17-1.** 作为元素、属性、类和注释使用的示例指令。

关于这个示例有几点需要说明。首先，我们的虚构指令可以作为元素、属性、类或注释使用，但实际上，并非所有指令都能以每种方式使用。例如，ngRepeat 指令用于在集合中循环项目，只能作为属性使用。这个主题将在本章后面更详细地介绍。还值得一提的是，最佳实践规定指令应作为元素和属性使用，而应避免使用类和注释，后者仅用于支持遗留应用程序。

关于清单 17-1 值得提及的另一点是 ngFoo 在 HTML 中的引用方式。按照惯例， Angular 指令使用驼峰命名法命名；然而，在 HTML 中使用时，指令以小写字母书写，并用破折号分隔单词。当 Angular 处理嵌入在 HTML 中的指令时，它使用以下步骤规范化名称：

- 从名称中去除 x- 和 data- 。
- 将 :、- 或 _ 分隔的名称转换为驼峰式。

这意味着 ngRepeat 可以写成 ng-repeat、x-ng-repeat、data-ng-repeat、ng:repeat 和 ng_repeat。简单的破折号分隔形式（ng-repeat）是首选格式，但如果你使用 HTML 验证工具，则带有 data- 前缀的版本也是可以接受的。其他版本应避免使用，它们的存在主要是为了遗留原因。



你还会注意到 Angular 将其官方指令以 ng 作为前缀。创建自定义指令时，你也应为名称添加前缀；但是，应避免使用 ng，因为它未来可能与 Angular 指令冲突。例如，如果你正在为 SitePoint 产品编写名为 match 的指令，可以考虑将其命名为 spMatch。

## 一个使用常见指令的示例

接下来，我们将查看一个 Angular 应用程序，如清单 17-2 所示，其中包含几个常见指令。第一个是 ngApp，它作为 ng-app 附加到 html 元素。ngApp 用于创建新的 Angular 应用程序，并应附加到应用程序的根元素。ngApp 在每个 HTML 文档中只能使用一次。在此示例中，Angular 应用程序被命名为 app。

清单 17-2 中使用的下一个指令是 ngController。正如你已经了解的，Angular 支持 MVC 应用程序设计方法。ngController 允许你为应用程序的特定部分指定一个控制器。在清单 17-2 中，一个名为 ExampleCtrl 的控制器附加到 body 元素。ExampleCtrl 的功能可以在示例底部附近的 JavaScript 中找到。这个特定的控制器只是向模型（在控制器代码中称为 $scope）添加了一个名为 people 的变量。

```
<!DOCTYPE html>
<html lang="en" ng-app="app">
  <head>
    <meta charset="utf-8">
    <title>Angular Directives</title>
  </head>
  <body ng-controller="ExampleCtrl">
    <div ng-repeat="person in people">
      {{person.firstName}} {{person.lastName}}
    </div>
    <script src="//ajax.googleapis.com/ajax/libs/angularjs/1.2.25/angular.js"></script>
    <script>
      'use strict';
      var app = angular.module('app', []);
      app.controller('ExampleCtrl', ['$scope', function($scope) {
        $scope.people = [
          {
            firstName: 'Colin',
            lastName: 'Ihrig'
          },
          {
            firstName: 'Adam',
            lastName: 'Bretz'
          }
        ];
      }]);
    </script>
  </body>
</html>
```

**清单 17-2.** 包含几个指令的 Angular 应用程序示例

清单 17-2 中使用的最后一个指令是 ngRepeat。ngRepeat 用于遍历集合的元素。在这种情况下，`ng-repeat="person in people"` 循环遍历模型中 people 的所有成员。在每次迭代期间，当前元素可通过 person 循环变量使用。在这个例子中，我们只是显示每个人的名字和姓氏。运行清单 17-2 的输出如图 17.1 所示。图中的底部面板还显示了 ngRepeat 如何展开 people。

![](img/0ca996f5fd0375fc118091628c3c7a87_234_0.png)

图 17.1. 指令示例输出和生成的代码

## 创建指令

Angular 附带了许多有用的内置指令，但你不可避免地会遇到需要扩展 Angular 开箱即用功能的情况。幸运的是，Angular 提供了一个便捷的 API 来创建指令。

指令使用 `directive()` 方法注册到各个模块。`directive()` 接受两个参数。第一个参数是规范化的指令名称（`myDirective` 而不是 `my-directive`）。`directive()` 的第二个参数是一个工厂函数，该函数返回一个对象，告诉 Angular 的 HTML 编译器 `$compile` 指令应如何表现。

工厂函数参数返回的对象被称为 **指令定义对象**，它是一个普通的 JavaScript 对象，其属性定义了指令的行为。以下列表解释了指令定义对象可以使用的一些属性：

- `priority`

  如果单个 DOM 元素上定义了多个指令，则可以使用 `priority` 来指定它们的编译顺序。具有较高 `priority` 值的指令会先被编译。具有相同 `priority` 的指令的编译顺序未定义。默认值为 0。

- `scope`

  如果设置为 `true`，将为指令创建一个新的作用域。如果 `scope` 是一个对象字面量，则会创建一个新的隔离作用域。**隔离作用域**不会从父作用域继承。这在创建不应读取或修改父作用域的可重用组件时很有用。隔离作用域对象的属性定义了从父作用域派生的本地作用域。这些值可以通过以下三种方式之一定义：

  - `@` 或 `@attr` — 将本地作用域属性绑定到 DOM 属性的值。结果始终是字符串，因为 DOM 属性是字符串。例如，`scope: {name: '@'}` 将把 `name` 属性绑定到父作用域中的 `name` 属性。类似地，`scope: {name: '@otherName'}` 将把 `name` 绑定到父级的 `otherName` 属性。

  - `=` 或 `=attr` — 在本地作用域属性和父作用域属性之间建立双向绑定。

  - `&` 或 `&attr` — 提供一种在父作用域上下文中执行表达式的方式。

- `controller`

  控制器构造函数。

- `transclude`

  编译元素的内容并使其对指令可用。当为 `true` 时，转置指令元素的内容。当为 `'element'` 时，转置指令的元素，包括元素上任何优先级较低的指令。

- `compile`

  `compile()` 函数用于转换模板 DOM，尽管很少使用。该函数接受两个参数 `tElement` 和 `tAttrs`，并返回一个后链接函数或一个具有函数属性 `pre` 和 `post` 的对象。`tElement` 是声明指令的元素。`tAttrs` 是元素上声明的属性的规范化列表。

- `link`

  `link()` 是一个负责注册 DOM 监听器以及更新 DOM 的函数。仅在未定义 `compile()` 函数时使用 `link()`。这是大多数指令逻辑所在的位置。`link()` 接受五个参数：

  - `scope` — 指令使用的作用域
  - `iElement` — 指令将被使用的元素
  - `iAttrs` — 此元素上声明的属性的规范化列表
  - `controller` — 控制器
  - `transcludeFn` — 预绑定到正确转置作用域的转置链接函数

- `terminal`

  当 `terminal` 为 `true` 时，优先级较低的指令将不会被编译。具有相同 `priority` 的指令仍会被编译。

- `template`

  用于指定指令生成的 HTML。`template` 可以是 HTML 模板字符串，也可以是一个接受两个参数 `tElement` 和 `tAttrs` 并返回 HTML 字符串的函数。如果使用函数版本，`tElement` 是声明指令的元素。`tAttrs` 是元素上声明的属性的规范化列表。

- `templateUrl`

  类似于 `template` 的字符串版本；但是，该字符串是从文件异步加载的。

- `restrict`

  一个包含字符串 `EACM` 子集的字符串。如果存在 `E`，指令可以用作元素。如果包含 `A`，指令可以用作属性。类似地，`C` 或 `M` 的存在分别允许指令用作类或注释。

## 一个自定义指令示例

清单 17-3 重新审视了清单 17-2 的代码；然而，在这个例子中，创建了一个自定义 `authorNames` 指令，而不是使用内置的 `ngRepeat`。关于自定义指令，首先要注意的是使用了 `restrict: 'E'`，这意味着 `authorNames` 只能用作元素。接下来，使用 controller 属性定义了控制器（注意 `ngController` 已从 DOM 中移除）。最后，使用 `link()` 函数创建一个模板字符串，编译它，并用新编译的 DOM 替换新的 `author-names` 元素。

```
<!DOCTYPE html>
<html lang="en" ng-app="app">
  <head>
    <meta charset="utf-8">
    <title>Angular Directives</title>
  </head>
  <body>
    <author-names></author-names>
    <script src="//ajax.googleapis.com/ajax/libs/angularjs/1.2.25/angular.js">
    </script>
    <script>
      'use strict';
      var app = angular.module('app', []);
```

```
      app.directive('authorNames', function($compile) {
        return {
          restrict: 'E',
          controller: function($scope) {
            $scope.people = [
              {
                firstName: 'Colin',
                lastName: 'Ihrig'
              },
              {
                firstName: 'Adam',
                lastName: 'Bretz'
              }
            ];
          },
          link: function(scope, element, attrs,
                         controller, transclude) {
            var template = scope.people.map(function(person) {
              var str = '<div>' + person.firstName +
                        ' ' + person.lastName + '</div>';
```

```
              return str;
            }).join('');
            var newElement = $compile(template)(scope);
```



 ```
element.replaceWith(newElement);
}
};
});
</script>
</body>
</html>
```

**清单 17-3.** 一个包含自定义指令的 Angular 应用示例

# 小结

本章解释了 Angular 内置指令的工作原理，以及如何创建你自己的指令。我们并未涵盖 Angular 的所有内置指令，也未涵盖指令定义对象上所有可设置的选项。我们所做的是覆盖指令开发的要点，并希望为你提供足够的信息，让你能够阅读 Angular 文档并开发出自己出色的指令。

## 第 18 章

## 控制器

**控制器**创建了一个框架来提升代码的可重用性和可测试性。它们是 Angular 应用的基本构建块。在前面的章节中，我们介绍了数据 Alicia据绑定和指令。在第 16 章的结尾，我们简要触及了 Angular 控制器。在本章中，我们将更详细地介绍控制器。我们将讨论它们是什么以及它们的用途；然后我们会介绍一些语法问题、最佳实践和示例。

与 Angular 相关的所有内容一样，重要的是要记住控制器只是 JavaScript 函数。这些函数用于创建一个新的 Angular（或作用域）上下文，并绑定到 HTML 标记的特定部分。控制器提供了一个放置特定于某组 HTML 标签的应用和视图逻辑的地方。请记住，单个视图可以使用多个控制器：视图与控制器的关系不是一对一的。也可以在不同视图中重用控制器。

### 语法

我们已经看到过一些控制器的定义，但让我们回顾一下用于定义 Angular 控制器的具体语法：

```
var app = angular.module('app', []);
app.controller('main', ['$scope', '$http', function($scope, $http) {
    //...
}]);
```

**清单 18-1. 控制器存根**

第一行创建了一个 Angular 模块。模块代表应用中的一个逻辑单元。它包含一个或多个控制器、服务、过滤器和指令。在这个例子中，我们使用 `angular.module` 创建了一个名为 app 的新模块。这里，将 app 视为我们将放置所有控制器的整个 Angular 应用。函数签名是模块名称，后跟一个依赖项的字符串数组。

依赖项是当前模块正确运行所需的另一个模块的引用。Angular 将确保在创建 app 模块之前加载依赖列表中列出的每个模块。在关于客户端路由的后续章节中，我们需要在应用模块之前加载几个模块；然而，对于这个简单的例子，我们除了 Angular 样板代码之外不需要任何东西，所以我们传递一个空数组。

`app.controller` 让我们向 app 添加一个控制器对象。类似于 `module` 函数，第一个参数是控制器名称，第二个参数是另一个带有函数作为数组最后一个元素的依赖项列表。函数是 main 控制器逻辑所在的位置。依赖列表中的前两项是此控制器需要的：`$scope` 和 `$http`。`$scope` 是每个控制器都有的本地作用域上下文，而 `$http` 是一个用于向远程资源发起 HTTP 请求的 Angular HTTP 模块。

函数签名表明，在控制器函数内部，我们将可以访问 `$scope` 和 `$http` 变量。每当创建 `main` 控制器时，Angular 将使用新的 `$scope` 对象和 `$http` 对象执行此函数，因为它们被列为控制器函数的依赖项。虽然你可以重命名函数参数（例如，s 和 h），但通常建议保持函数参数和依赖项名称一致，以便提高可读性。

还有其他方式可以声明控制器并指定 Angular 的依赖项，但清单 18-1 中的方法是首选的，因为代码在压缩后仍能继续工作。在清单 18-1 中，我们通过名称明确告知 Angular 此控制器需要哪些依赖项。Angular 可以通过名称推断依赖项，但在代码压缩后这将无法工作。压缩后，大多数变量被缩减为单个字符，通过名称查找依赖项不再有效。

### 依赖项

$scope 是一个子作用域对象，其父级是全局应用作用域。通常，这些是在 HTML 中使用 ng-controller 指定控制器时由 Angular 自动创建的。与 $scope 相关的属性和函数太多，无法在本书中一一涵盖，因此请查看 [Angular 网站上的完整文档](http://www.google.com/url?q=http%3A%2F%2Fdocs.angularjs.org%2Fapi%2Fng.%24scope&sa=D&sntz=1&usg=AFQjCNEvVdY399v7m3b4V3p1Q7Q8j9T5Q)。$scope 附带有用于与 $digest 循环交互的方法，以及用于创建额外的 $watch 值和机制，以便从其他 Angular 对象发送和接收事件。

$http 是基于 Promise 的用于发起 HTTP 请求的模块。主要函数接受一个配置对象，你在其中指定路由、方法和负载，以及 HTTP 请求的许多其他属性。$http() 函数返回一个具有 .then()、.success() 和 .error() 方法的 Promise 对象。我们将在示例中使用它向我们的 Express 服务器发起请求以获取员工列表。

Angular 有一个内置的依赖注入系统。如果你不熟悉**依赖注入**，这是一个足够简单的概念。它是一种设计模式，其中依赖项在创建时被*注入*到依赖对象中（在本例中是主控制器），并成为客户端对象状态的一部分。这将客户端和依赖逻辑分离，并进一步将客户端与依赖解耦。如果你希望更深入地了解依赖注入，请查看 [Angular 官方文档](http://www.google.com/url?q=http%3A%2F%2Fdocs.angularjs.org%2Fguide%2Fdi&sa=D&sntz=1&usg=AFQjCNEvVdY399v7m3b4V3p1Q7Q8j9T5Q)。

通过将 $http 模块注入控制器，控制器不负责查找和创建 $http 模块；相反，$http 作为参数传入。我们希望测试尽可能小，并且只测试开发者代码。使用依赖注入，我们可以向控制器传递一个只返回静态值的模拟 $http 模块。这使我们能够在隔离状态下测试控制器逻辑，将服务器和 Angular $http 模块完全排除在测试之外。

## 扩展示例

让我们完全充实清单 18-1。我们希望从服务器获取员工列表并显示它们。我们还应该能够通过适当的 HTTP 调用从列表中添加和删除员工。此示例将只关注客户端代码。

## Express 集成

如果你一直跟着代码和示例学习，此时你应该有一个在第 13 章开始构建的可用的 Express 服务器。将清单 18-2 放在 public/html 目录的 HTML 文件中，并将浏览器指向该文件。这将显示示例并使你能够与之交互。

当控制器首次加载时，它使用 $http 向 Express 服务器发起 GET 请求以获取员工列表。我们在第 13 章构建的 /employees 路由与 MongoDB 实例通信，并从数据库返回员工列表。

另外两个路由，POST 到 /employees 和 DELETE 到 /employees/:id 让你有机会自行扩展 Express 服务器的功能。你需要使用 router.post 和 router.delete 在 Express 服务器中设置路由。在处理器函数内部，使用 Employee 模型与数据库中的 Employee 集合通信。Employee.remove 用于删除，Employee.save 用于创建新员工。成功删除员工后，向客户端响应更新的员工文档集合。最后，在数据库中创建新员工后，向客户端响应新创建的员工文档。回顾第 8 章应该能提供一些有关如何使这两个新路由正常工作的有用提示和示例。

```
<html lang="en" ng-app="app">
  <body>
    <div ng-controller="main">
      <input type="text" ng-model="firstName" placeholder="first name">
      <input type="text" ng-model="lastName" placeholder="first name">
      <button ng-disabled="!(firstName.length && lastName.length)"
              ng-click="add()">Add</button>
      <table>
        <tr ng-repeat="p in employees">
          <td>{{p.id}}</td>
          <td><span>{{p.first}} {{p.last}}</span></td>
          <td><button ng-click="$parent.remove(p)">Remove</button>
          </td>
        </tr>
      </table>
    </div>
    <div ng-controller="logger">
      <pre>
        <p ng-repeat="e in events track by $index">{{$index}} -
          {{e}}</p>
      </pre>
```



## JavaScript

我们首先创建一个新的 Angular 模块，用于容纳所有的控制器，并将其命名为 app。你可以随意命名该模块，但大多数示例都会使用 app 作为模块和变量名。然后我们声明主控制器。基本上每个控制器都需要 `$scope` 对象，因此将其添加到依赖项列表中。由于我们要向服务器发起请求，因此还需要 `$http` 模块。最后，为了促进多个控制器之间的通信，我们引入 `$rootScope`。`$rootScope` 对象为我们提供了对整个 Angular 应用程序全局作用域对象的直接引用。

控制器的前几行设置了其初始状态。我们将使用 employees 员工作为员工列表的数据存储。与 Express 路由一样，`$http` 也暴露了便捷的映射到最常见 HTTP 动词的方法。第一个任务是从服务器检索员工列表，并将该数据加载到 `$scope.employees` 中。为此，我们向 `/employees` 发送 GET 请求。在成功回调中，我们将 employees 设置为 Web 服务器的响应，即一个员工对象数组。

由于 employees 与视图数据绑定，一旦其值发生变化，就会触发新的 `$digest` 循环，自动更新视图。注意，不需要额外的代码来更新视图。Angular 的双向数据绑定处理了所有事情，即使我们是异步从服务器获取数据。

然后我们使用 `$rootScope` 来触发自定义事件。第一个参数是事件名称，第二个参数是事件负载，我们希望将其传递给任何可能在监听的客户端。我们想使用 `$rootScope` 对象，因为我们将要使用的两个控制器是兄弟关系，而不是相互嵌套的。

接下来我们创建两个用于添加和删除项目的事件处理程序，类似于清单 16-3 中所做的。最大的区别在于这些方法被映射回具有真实数据存储的 Web 服务器。add 方法使用 firstName 和 lastName 创建一个新的对象字面量，然后将其 POST 到 Web 服务器。在服务器端，我们创建一个新对象并将其插入数据库。在此示例中，服务器响应表示创建的对象，即 data。成功创建后，我们将 data 推入 employees 数组。由于数据绑定，新行会自动添加到代表新员工的 HTML 表格中。

最后我们将 remove 添加到 `$scope` 对象。此函数向 Web 服务器发送 DELETE 请求，并通过路由参数传递员工 ID。响应是数据库中的更新列表，因此我们可以将 `$scope.employees` 重置为返回的结果，让视图层进行更新。

第二个控制器 logger 相比之下很简单。我们将用它作为事件记录器。当日志事件发生时，我们希望将该事件添加到内部 events 数组中。

我们将 events 附加到 `$scope` 并将其初始化为空数组。`$rootScope.$on` 用于设置对 `$rootScope` 上发生的任何日志事件的监听器。回调函数接受两个参数，第一个是 Angular 事件对象。它包含有关事件如何起源、源和目标作用域的信息，以及管理事件在不同 Angular 作用域中冒泡的函数。第二个参数是从触发函数传入的任何负载数据。我们将把 data（将是一个简单的字符串）推入 events 数组。

我们可以在整个应用程序中利用 logger 控制器。创建新的控制器用于事件日志记录的好处是，它可以在许多页面上重用，而无需了解同个视图中使用的任何其他控制器。

## HTML

清单 18-2 中的 HTML 到此时应该看起来很熟悉了 Goldman，因此我们只会重点介绍几个关键更改。首先，我们引入了一个新的 div 来包装与 `main` 控制器相关的 DOM 元素，并设置 `ng-controller="main"`。这会实例化一个新的 `main` 控制器，并将 DOM 元素绑定到 `main` 的新实例。我们还添加了第二个设置了 `ng-controller="logger"` 的 div。需要注意的是，这些控制器*不*具有父子关系。它们是直接的兄弟节点，这避免了它们上下文被嵌套。

还要注意，我们在 `ng-repeat` 内部使用了 `full-name` 指令。我们想通过设置 `person=p` 将循环中的当前项传递给指令。这会在指令内部创建一个隔离作用域，并引用正确的 `p` 对象。

HTML 中使用的一个新东西是 DOM 的 logger 部分中的 `track by $index`。`ng-repeat` 的可选 `track by` 参数告诉 Angular 如何将集合项与相应的 DOM 元素关联。默认情况下，Angular 使用 JavaScript 标识来进行这种关联，对于对象集合来说通常没问题；然而，在 `logger` 控制器中，我们维护的是一个字符串列表，重复是不可避免的。Angular 不喜欢使用常规 JavaScript 标识在字符串上会产生重复 DOM 元素。使用 `$index` 跟踪元素让我们可以指定数组中的每个唯一索引应被视为唯一项。

清单 18-2 现在看起来不错。它是一个功能完整的用户列表 Web 应用程序，提供了良好的用户体验，代码易于阅读和维护。我们还可以非常轻松地添加排序、高亮和验证功能。但仍有改进空间。如果我们想在不同的控制器中检索员工列表呢？此外，由于我们将服务器设计为 RESTful 风格，是否应该有更少代码的方式来与其通信？

## 简单服务

我们将重构 HTTP 请求到一个使用 Angular 另一个内置模块的服务：`$resource`。`$resource` 是一个专门为与 RESTful Web 服务交互而设计的工厂对象。工厂模式是一种成熟的设计，旨在解决使用类构造函数的问题。使用工厂，单个函数可以返回不同类型的对象。我们将使用 `$resource` 创建一个简单的 `Employee` 服务，它将取代我们所有的 HTTP 调用。它还可以被任何需要访问员工 CRUD 功能的其他控制器使用。`ngResource` 位于单独的脚本文件中，因此你需要更新 HTML 以在 Angular 之后引入它。我们通过 Angular CDN 在 //code.angularjs.org/1.2.16/angular-resource.js 加载了此脚本。

使用服务的好处之一是，它们作为单例创建，每个 `ng-app` 块一次，并在其中嵌套的任何控制器之间共享。这意味着当我们定义好服务后，它可以像任何其他依赖项一样注入，并被应用程序中的任何控制器使用。它还可以在任何控制器之外独立测试，提供了另一级别的可测试性。有关不同类型工厂对象的完整讨论，请参阅 [Angular 文档](https://docs.angularjs.org/guide/services)。

**清单 18-3.** 创建 Employee 服务

在清单 18-3 中，我们创建 app 模块并指定 `ngResource` 现在是此模块的依赖项。`ngResource` 使 `$resource` 依赖项在 `app` 内部的任何依赖项列表中可用。`$resource` 是创建员员工服务所需的对象。第二行与创建控制器的语法完全相同。`$resource` 依赖项指的是安装到全局 `app` 模块中的 `ngResource` 模块。

你会注意到 `Employee` 服务的大部分只是一个配置对象。可以配置此对象的所有详细内容超出了本书的范围，但 [Angular 网站有所有文档](https://docs.angularjs.org/api/ngResource/service/$resource)。实际上，我们已经使用 `/employee/:employeeId` 资源创建了与服务器的 RESTful 连接器。我们已将 get 操作配置为返回数组，delete 也配置为返回数组并使用 DELETE HTTP 方法。最后，我们包含了一个 post 操作，向服务器发出 POST 请求。



这些设置是专门为了配合 Express 集成章节中概述的路由而设计的。如果你的实现偏离了我们建议的路线，你将需要更新 EmployeeService 的设置以匹配你对 Express 路由的实现方式。

## 使用 EmployeeService

最后，在代码清单 18-4 中，我们将用新的 EmployeeService 替换 `$http`：

```
app.controller('main', ['$scope', 'EmployeeService', '$rootScope',
    function($scope, EmployeeService, $rootScope) {
        EmployeeService.get(function (data) {
            $scope.employees = data;
        });

        $scope.add = function () {
            EmployeeService.post({
                first: $scope.firstName,
                last: $scope.lastName
            }, function (data) {
                $scope.employees.push(data);
            });
        };

        $scope.remove = function(employee) {
            EmployeeService.delete({
                employeeId: employee.id
            }, function (data) {
                $scope.employees = data;
            });
        }
    }]);
```

**代码清单 18-4.** 使用 EmployeeService

我们从原始的主控制器中移除了一些代码，以便专注于集成 EmployeeService。现在，EmployeeService 可以像任何内置的 Angular 模块一样被引入到主控制器中。我们在依赖列表以及控制器函数签名中都替换了 `$http`。

这些代码变更不会影响应用程序的功能。它们只是通过移除所有 `$http` 样板代码来清理服务器交互。它们还将员工服务器操作封装在一个单独的模块中，该模块可以在多个地方使用，并且可以在控制器之外进行独立测试。

# 总结

在本章中，我们讨论了 Angular 控制器，它们负责与视图进行双向通信。控制器创建一个新的上下文，该上下文是父作用域的子级。我们讨论了声明控制器的推荐方式以及如何指定控制器所需的不同依赖项。我们介绍了 Angular 的一个内置模块 `$http`，并演示了如何使用它向现有的 Express 服务器发送请求。

接下来，我们在代码清单 18-2 中编写了一个完整的示例，该示例涵盖了目前为止所有介绍过的 Angular 主题。这包括指令、控制器、`$http` 模块、事件处理以及控制器到控制器的通信。

最后，我们通过编写第一个服务对代码清单 18-2 进行了一些重构。这使我们能够移除所有 `$http` 样板代码，并用一个以配置为中心的 `$resource` 模块来替代它。我们还讨论了如何将此模块注入到我们的控制器中。

# 第 19 章

## 客户端路由

在第 18 章中，我们演示了如何向 Express 服务器发送 Ajax 请求并将结果加载到 `$scope` 中以显示结果。这对于单页网站来说非常好，但大多数应用程序跨越的不止一个页面。在代码清单 18-2 中，如果我们想添加一个可用于编辑员工的新页面该怎么办？应用程序需要切换页面并显示新的视图，但我们希望利用 Ajax 请求的优势，而不会丢失浏览器内存中的所有 JavaScript 状态和静态文件。我们还希望该页面是可收藏的，因此该页面必须是无状态的。

这正是客户端路由大显身手的地方。客户端路由允许开发者在 HTML 中创建标准的锚点标签，这些标签将由 Angular 路由器处理。Angular 路由器在这些链接发送到 Web 服务器之前拦截它们，并通过客户端路由表进行处理，然后返回新的页面内容。新页面可以拥有自己的 Angular 控制器和全新的 HTML 块。对于用户来说，它看起来与传统导航完全相同，只不过切换几乎是即时的。

在本章中，我们将扩展代码清单 18-3，将其向我们完整的人力资源应用程序再推进一步。我们将使用代码清单 18-3 中的列表视图，并添加一个编辑视图。每个视图将存储在独立的 HTML 文件中。我们还将使用一种"布局"风格的 HTML 页面，它将作为站点的静态部分，并提供一个"窗口"区域，客户端路由的变化将在此区域内发生。

### ngRoute 入门

Angular 中的路由在开发周期中经历了几次变化。所需的模块以前是打包在 Angular 运行时中的；然而，Angular 团队后来将 ngRoute 拆分为一个独立的文件。这样做的主要原因是，如果不需要路由模块，可以减少 Angular Web 应用程序的下载大小。安装 ngRoute 模块会向控制器和配置块暴露 `$routeProvider` 和 `$routeParams` 依赖项。我们将在本章的代码示例部分更详细地介绍这两个依赖项。与 ngResource 一样，我们建议在此示例中使用 Angular CDN。我们将使用的版本可以在 //code.angularjs.org/1.2.16/angular-route.js 找到。

### 应用程序概览

在本节中，我们将使用客户端路由来升级现有的应用程序。我们希望显示用户列表及其相关信息。然后我们希望提供一个编辑按钮，将用户带到一个新页面并显示一个用户可以交互的编辑界面。为了简单起见，我们将跳过实现保存功能。

首先，我们需要三个 HTML 文件：index.html、edit.html 和 view.html。请记住，`app.use(express.static(__dirname + '/public'));` 会创建一个静态文件服务器，在 /public 目录中查找文件。在 public 下创建这些文件，以便 Express 静态中间件可以直接从硬盘提供它们。创建文件后，请验证 Web 服务器能否正确地将它们发送到浏览器。

其次，我们需要为 JavaScript 代码创建一个存放位置。在这个示例中，我们将使用一个外部 JavaScript 文件，而不是像其他一些示例中那样使用内联 `<script>` 标签。在 /public/scripts 下创建 webapp.js，以将脚本文件与视图分开。webapp.js 将是此示例中所有 JavaScript 代码的存放位置。

### 代码

首先，让我们看一下 index.html，了解我们将如何构建应用程序的其余部分：

```
<html lang="en" ng-app="app">
  <body>
    <h1>Your Human Resource Application</h1>
    <ng-view></ng-view>
  </body>
  <script src="//ajax.googleapis.com/ajax/libs/angularjs/1.2.16/angular.js"></script>
  <script src="//code.angularjs.org/1.2.16/angular-route.js"></script>
  <script src="//code.angularjs.org/1.2.16/angular-resource.js"></script>
  <script src="scripts/webapp.js"></script>
</html>
```

**代码清单 19-1.** index.html 文件

代码清单 19-1 将作为应用程序的静态部分。我们有 script 标签来加载 Angular、Angular 路由器（ngRoute）和 Angular 资源（ngResource）。最后，我们添加了对我们自己的 webapp.js 脚本文件的引用。此时你应该已经熟悉 ng-app；然而，`ng-view` 是我们 Angular 指令工具箱中的一个新元素。

`ng-view` 是由 ngRoute 暴露的一个新元素，因为它们是配合使用的。它是标记中渲染后 HTML 文件内容的占位符。每当当前路由发生变化时，`ng-view` 中的内容就会根据路由的配置进行更改。当我们进一步讨论路由时，这一点会更加清晰。

### 注意：为什么所有脚本都在 index.html 中？

我们需要的所有脚本都位于 index.html 中。这样它们就能在整个应用程序的生命周期中保持加载状态。如果我们把它们放在 view.html 或 edit.html 中，那么每次路由变化时都需要重新下载它们。如果我们有一些 CSS，我们也希望将它们包含在 index.html 中。

### 路由器

以下是 webapp.js 的前几行。在本章的剩余部分中，我们将继续向此示例追加代码：

```
var app = angular.module('app', ['ngRoute', 'ngResource']);

app.config(['$routeProvider', function($routeProvider) {
  $routeProvider
    .when('/view', {
      templateUrl: 'view.html',
```



```
controller: 'view'
})
.when('/edit/:employeeId', {
  templateUrl: 'edit.html',
  controller: 'edit'
})
.otherwise({
  redirectTo: '/'
});
}]);
```

## 列表 19-2. Angular 路由器

第一行创建了我们的应用模块并安装了 ngRoute 和 ngResource。我们在列表 18-3 中使用了 ngResource，所以你应该对此很熟悉。如前所述，ngRoute 使我们可以访问 `$routeProvider` 依赖。`$routeProvider` 是我们将用于设置客户端路由的对象。

首先，谈谈 `app.config`。Angular 模块（如 `app`）可以通过 `.config` 和 `.run` 拥有多个配置块。从高层次来看，这两种方法都在应用程序引导过程的不同阶段运行配置代码。Angular 文档将不同的配置块类型总结如下：

1.  配置块 (`.config`) —— 在提供者注册和配置阶段执行。只有提供者和常量可以注入到配置块中。这是为了防止在服务完全配置之前被意外实例化。

2.  运行块 (`.run`) —— 在注入器创建后执行，用于启动应用程序。只有实例和常量可以注入到运行块中。这是为了防止在应用程序运行时进行进一步的系统配置。

在列表 19-2 中，我们使用 `.config` 是因为我们想在应用程序启动之前完全配置 `$routeProvider`。这是合理的，因为如果客户端路由在应用程序启动前没有完全设置好，导航将会中断，使得整个网站无法使用。通过利用 Angular 的引导过程，我们可以确保我们的配置代码块 (`app.config`) 会在我们接收任何用户输入之前运行。这使得 `.config` 块成为存放应用程序启动前运行一次代码的理想位置。

`$routeProvider` 的代码应该相当容易阅读。每个 `.when` 调用代表浏览器中的一个不同 URL。第二个参数包含路由器要使用的选项：`templateUrl` 和 `controller`。`templateUrl` 指示路由器加载与该 URL 关联的模板的位置。注意第一个参数 `:employeeId` 的存在。Angular 路由器使用与 Express 相同的表示法来定义路由参数。

以编程方式设置视图的控制器，如果你想为两个路由使用相同的视图但不同的控制器，会很有帮助。如果你愿意，可以保留每个视图中的 `ng-controller`，但我们认为在这里声明 `controller` 并使视图对控制器更加无关是更好的做法。

## 路由生命周期示例

为了真正体会客户端路由的强大，让我们从请求到响应跟踪一个示例。如果你在浏览器中输入 `index.html#/view`，Angular 路由器将检查传入的请求并尝试匹配路由表中定义的路由。如果找到匹配项，它将向 `templateUrl` 发出 Ajax 请求，并根据 `controller` 选项实例化一个新的控制器，然后将其渲染到 `ng-view` 指令中。如果一条路由有多个匹配项，最后一个匹配项的代码将被执行。如果路由以 `index.html#` 开头但没有匹配任何已配置的路由，`.otherwise` 块将执行，并将请求重定向回 `/`。默认情况下，Angular 路由器会尝试拦截包含 `#` 的路由。不带 `#` 的路由将是普通请求，并通过 Web 服务器路由器处理。

## 服务和控制器

如果你阅读过[第 18 章](#)，大部分代码应该很熟悉：

```
app.factory('EmployeeService', ['$resource', function($resource) {
  return $resource('/employees/:employeeId', {}, {
    list: {
      isArray: true
    },
    get: {
      isArray: false
    }
  });
}]);
```

```
app.controller('view', ['$scope', 'EmployeeService',
function($scope, EmployeeService) {
  $scope.employees = [];
  $scope.firstName = $scope.lastName = "";
```

```
  EmployeeService.list(function (data) {
    $scope.employees = data;
  });
}]);
```

```
app.controller('edit', ['$scope', 'EmployeeService','$routeParams',
 function($scope, EmployeeService, $routeParams) {
   $scope.employee = {};

   EmployeeService.get({
     employeeId: $routeParams.employeeId
   }, function (data) {
     $scope.employee = data;
   });
 }]);
```

**列表 19-3.** 服务和控制器

我们对列表 19-3 中的 `EmployeeService` 相对于其在列表 18-3 中的外观进行了轻微调整。如果你回忆第 18 章关于 `$resource` 的讨论，列表 19-3 中的大部分代码应该是可识别的。`$resource` 的第一个参数是这个资源对象的路由，包含路由参数 `:employeeId`。第二个参数在本例中未使用，是一个空对象。我们使用第三个参数来声明我们将要在构建的最终 `$resource` 中定义哪些方法。

我们添加了一个 `list` 动作，它向 `/employees/:employeeId` 发出 GET 请求。然而，当我们使用 `list` 方法时，我们将省略 `employeeId`，因为我们把 `list` 视为获取所有员工的完整列表。如果路由参数被省略，它将被视为空字符串。虽然这可能有点令人困惑，但这就是你如何使用单个对象（`EmployeeService`）与所有 Express 服务器资源进行交互的方式。`isArray` 表示此请求的结果应该是一个数组。`get` 已被更改，不再返回数组，因为我们将使用该操作从数据库中检索单个员工。当我们使用 `get` 函数时，我们将向函数传递一个 `employeeId`，该 ID 将在 `EmployeeService` 对象构建向 Express 服务器请求的 URI 时使用。所以 `list` 不需要 `employeeId`，因为它被期望返回所有员工，而 `get` 需要 `employeeId` 来返回特定员工。

`view` 和 `edit` 控制器非常简单。只有少数几个项目附加到它们各自的 `$scope` 值上，并且只需要调用一次 `EmployeeService` 即可检索数据。`edit` 控制器引入了 `$routeParams` 依赖。`$routeParams` 为开发人员提供了一种从客户端路由中提取路由参数的便捷方式，类似于 Express 端的 `req.params`。这个模块本质上解析当前浏览器 URL 并尝试为当前路由提取路由参数，将这些值附加到 `$routeParams`。这个概念与 Express 中的路由参数相同，只是语法略有不同。在这个例子中，它提供了一种从浏览器 URL 获取 `employeeId` 的简单方法。没有 `$routeParams`，你需要使用正则表达式从 URL 中获取数据。

## 视图

最后，为了完成这个示例，我们将构建与 Angular 路由器一起工作的视图。

view.html

```
<table>
  <tr ng-repeat="p in employees">
    <td>{{p.id}}</td>
    <td>{{p.first}}</td>
    <td>{{p.last}}</td>
    <td><a href="#/edit/{{p.id}}">编辑 >>> </a></td>
  </tr>
</table>
```

edit.html

```
<fieldset>
  <legend>{{employee.first}} {{employee.last}}</legend>
  <input type="text" name="first" ng-model="employee.first">
  <label for="first">名</label>
  <input type="text" name="last" ng-model="employee.last">
  <label for="last">姓</label>
</fieldset>
```

```
<a href='#/view'>返回 <<< </a>
```

**列表 19-4.** 路由视图

这两个视图应该看起来很熟悉。需要注意的主要细节是 `<a>` 标签：注意 `href` 包含了 `#` 符号。这会提醒 Angular 路由器拦截这个 URL 并尝试在客户端进行路由，而不是将其转发到服务器。通过使用 Angular 路由器，我们可以通过使用 `#` 修饰 URL 来导航到应用程序中的不同页面。

## 整合

一旦你完成了所有概述的更改，启动你的服务器并将浏览器指向 `index.html#/view` 以启用 Angular 路由器。它将匹配 `/view`，向 `view.html` 发出 Ajax 请求，创建一个 `view` 控制器，并将结果发送到浏览器。你应该会看到一个包含可点击编辑链接的员工表格。点击其中一个链接会重新开始路由过程。你应该会看到编辑视图，并且浏览器应该指向一个类似于 `index.html#/edit/69c3974488bc9fe6` 的 URL。如果你刷新浏览器，应该会显示相同的员工和视图。这就是*可加书签*的含义：页面的显示状态完全通过 URL 传输。如果你将 URL 更改为 `index.html#/unknown`，你将看到默认的着陆页。路由器中的 `.otherwise` 选项被触发，并将请求重定向回路由 URL。如果你想要更多的挑战，可以更新编辑视图和 `EmployeeService`，使更新员工功能正常工作。让你完成这项工作所需的一切都在过去几章中涵盖，所以利用这个机会测试你对到目前为止讨论的主题的理解。



# 小结

在本章中，我们演示了如何使用 Angular 设置客户端路由。这需要使用 `ngRoute` 模块，它让我们能够访问依赖项 `$routeProvider` 和 `$routeParams`。`$routeProvider` 用于在应用的配置块中通过 `.when` 和 `.otherwise` 构建路由表。`templateUrl` 告诉路由器在有匹配的客户端路由时，对指定的文件或资源发出 GET 请求。`controller` 选项为我们提供了一种为相关视图创建正确控制器的方式。这为开发人员提供了更大的灵活性，可以混合和匹配控制器，而不需要使用 `ng-controller` 指令。

`$routeParams` 提供了一种简单的方法，可以从 URL 中提取信息，而无需借助正则表达式。`ngRoute` 还公开了 `ng-view` Angular 指令，它在渲染新视图时充当目标。当客户端路由被渲染时，这是站点中发生变化的部分。导航到不同的客户端路由时，该元素之外的所有内容保持不变。

我们讨论了 `#` 符号如何充当 Angular 尝试将当前请求路由到客户端的指示器。在我们的视图中，我们能够创建传统的 `a` 标签，并将 `href` 属性设置为其他客户端链接，无需任何特殊配置。这些锚点标签用于在不同页面之间移动，而无需额外的编码。这减少了自定义路由解决方案可能引入的维护工作量和潜在错误。

## 第20章 应用中的 Angular

在第6、9 和13 章中，我们分别使用 Node、MongoDB 和 Express 创建了一个相当简单的人力资源应用 API。在本章中，我们将使用 Angular 创建应用的前端。结果将是一个完整的 MEAN 应用。本章包含大量代码，因为它将应用的其余部分连接在一起，但我们会尽力解释清楚。

本章的所有工作都将在项目的 public 目录中进行。该目录用于提供静态资源，如 HTML、CSS、JavaScript 和图像文件。这是在 index.js 中通过清单 20-1 中的行设置的。在本章中，你应该删除 public 目录的现有内容。我们最终的 public 目录结构如图 20.1 所示。

```
app.use(express.static(path.join(__dirname, 'public')));
```

**清单 20-1.** 静态中间件的配置

```
public/
├── css/
│   └── style.css
├── images/
│   └── employees/
│       ├── 1000003.png
│       └── background.png
│   └── user.png
├── js/
│   └── app.js
├── employee.html
├── employees.html
├── home.html
├── index.html
├── team.html
└── teams.html
```

图 20.1. 我们的 public 目录结构

## 主页

单页应用的一个显著特点是它只有一个 HTML 页面。我们项目主页的内容如清单 20-2 所示。这段代码中有几点需要注意。首先，html 标签定义了一个名为 app 的 Angular 应用。其次，我们的应用使用 [Bootstrap 来简化样式过程](https://getbootstrap.com)，以及 [Font Awesome 来提供实用的图标](https://fontawesome.com)。

在 body 标签内，无序列表用于在屏幕顶部提供一个菜单，而 div 标签用于显示 Angular 视图。Angular 核心库以及 `$route` 和 `$resource` 服务通过三个 script 标签导入。我们自己的 CSS 文件 style.css 也被导入。

```
<!DOCTYPE html>
<html lang="en" ng-app="app" class="no-js">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>HR App</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" type="text/css" href="//netdna.bootstrapcdn.com/bootswatch/3.1.1/flatly/bootstrap.min.css"/>
    <link rel="stylesheet" type="text/css" href="//netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.min.css">
  </head>
  <body class="container">
    <ul class="nav nav-pills">
      <li class="active"><a href="#">Home</a></li>
      <li><a href="#/employees">Employees</a></li>
      <li><a href="#/teams">Teams</a></li>
    </ul>
    <div ng-view></div>
    <script src="//ajax.googleapis.com/ajax/libs/angularjs/1.2.25/angular.js"></script>
    <script src="//code.angularjs.org/1.2.25/angular-route.js"></script>
    <script src="//code.angularjs.org/1.2.25/angular-resource.js"></script>
    <script src="js/app.js"></script>
    <link rel="stylesheet" type="text/css" href="/css/style.css">
  </body>
</html>
```

**清单 20-2.** 应用中唯一的独立 HTML 页面

## CSS 和图像文件

我们将仅简要介绍 CSS 和图像文件，但值得指出的是它们确实存在。我们的自定义样式表 css/style.css 的内容如清单 20-3 所示。

```css
body {
  background: url('/images/background.png');
  background-repeat: repeat;
  min-width: 320px;
}

ul.nav.nav-pills {
  margin: 10px 0;
  background-color: #fff;
}

.employee-list-item .panel-body {
  display: -webkit-box;
  display: -moz-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: box;
  display: flex;
}

.employee-list-item .panel-body > * {
  -webkit-align-self: center;
  align-self: center;
  -ms-flex-item-align: center;
}

.employee-list-item .panel-body .btn {
  margin-left: auto;
}

.employee-avatar {
  height: 200px;
  width: 200px;
  border-radius: 6px;
}

span.icon-container {
  display: inline-block;
  text-align: center;
  width: 48px;
  height: 48px;
  border: 1px solid #3498db;
  margin-right: 15px;
  border-radius: 4px;
}

div.button-bar {
  text-align: left;
  margin-bottom: 10px;
}

div.form-offset {
  padding-top: 15px;
}

.margin-top-reset {
  margin-top: 0;
}

ul.address-lines {
    list-style: none;
    margin: 0;
    padding: 0;
}

ul.address-lines div.address-edit, .margin-bottom-space {
    margin-bottom: 5px;
}

ul.address-lines .in-line-input {
    margin-bottom: 5px;
}
```

**清单 20-3.** style.css 中的自定义 CSS 代码

images 目录包含一个背景图像（background.png）、一个默认头像（user.png）以及一个包含个人头像的 employees 目录。目前，系统中只有一个用户有个人头像。所有其他用户将使用默认图像。

## app.js

本章最有趣的文件是 js/app.js，它包含了我们所有的 Angular 代码。这段代码如清单 20-4 所示。我们首先声明我们的模块，名为 app，它依赖于 `ngRoute` 和 `ngResource`。定义了一个常量来列出每个美国州的缩写。这将在一个更新员工信息的员工指令中使用。

`config()` 调用用于注入 `$routeProvider`，以创建客户端路由器。在此示例中，路由器支持五个路由和一个 `otherwise` 情况，后者将用户送回主页。与员工和团队相关的路由各自有一个稍后在代码中定义的控制器。

接下来，两次调用 `factory()` 用于创建 EmployeeService 和 TeamService。`factory()` 调用依赖于 `$resource`，这使得与 RESTful API（如我们的 Express API）交互变得非常容易。

然后我们使用 `directive()` 方法定义了两个自定义指令。第一个指令 `imageFallback` 用于为 `img` 元素设置回退图像。这为没有个人头像的员工设置了默认头像。第二个指令 `editInLine` 用于在不通过不同路由的情况下编辑员工信息。

最后，创建了四个控制器用于我们的团队和员工路由。除了 EmployeeCtrl 之外，这些控制器都很简单。EmployeeCtrl 控制器用于处理单个员工视图页面。这个控制器需要执行许多操作，并且依赖于 q promises 库。例如，该控制器的 `save()` 函数用于将任何更改持久化到 MongoDB 数据库。如果用户开始编辑信息但后来改变了主意，则调用 `cancel()` 方法。该方法调用 `$route.reload()`，这会导致 `$route` 服务重新加载当前路由，即使位置没有改变。这会清除已作出的任何更改。

```javascript
'use strict';
var app = angular.module('app', ['ngRoute', 'ngResource'])
    .constant('config', {
        states: ['AL', 'AK', 'AZ', 'AR', 'CA', 'CO', 'CT', 'DE', 'FL', 'GA', 'HI',
            'ID', 'IL', 'IN', 'IA', 'KS', 'KY', 'LA', 'ME', 'MD', 'MA', 'MI', 'MN', 'MS',
            'MO', 'MT', 'NE', 'NV', 'NH', 'NJ', 'NM', 'NY', 'NC', 'ND', 'OH', 'OK', 'OR',
            'PA', 'RI', 'SC', 'SD', 'TN', 'TX', 'UT', 'VT', 'VA', 'WA', 'WV', 'WI', 'WY']
    });
```

```javascript
app.config(['$routeProvider', function($routeProvider) {
    $routeProvider
        .when('/', {
            templateUrl: 'home.html'
        })
        .when('/employees', {
            templateUrl: 'employees.html',
            controller: 'EmployeesCtrl'
        })
        .when('/employees/:employeeId', {
            templateUrl: 'employee.html',
            controller: 'EmployeeCtrl'
        })
```



```
})
    .when('/teams', {
      templateUrl: 'teams.html',
      controller: 'TeamsCtrl'
    })
    .when('/teams/:teamId', {
      templateUrl: 'team.html',
      controller: 'TeamCtrl'
    })
    .otherwise({
      redirectTo: '/'
    });
  }]);

app.factory('EmployeeService', ['$resource', function($resource) {
  return $resource('/employees/:employeeId', {}, {
    update: {
      method: 'PUT'
    }
  });
}]);

app.factory('TeamService', ['$resource', function($resource) {
  return $resource('/teams/:teamId');
}]);

app.directive('imageFallback', function() {
  return {
    link: function(scope, elem, attrs) {
      elem.bind('error', function() {
        angular.element(this).attr('src', attrs.imageFallback);
      });
    }
  };
}).directive('editInLine', function ($compile) {
  var exports = {};

  function link (scope, element, attrs) {
    var template = '<div class="in-line-container">';
    var newElement;
    var displayValue;
    var options;

    switch (attrs.editType) {
    case 'select':
      displayValue = attrs.displayValue ? 'displayValue' : 'value';
      options = attrs.editOption;
      options = options.replace(attrs.editList, 'editList');

      template += '<div class="in-line-value" ng-hide="editing">{{' + displayValue + '}}</div>';
      template += '<select class="in-line-input form-control" ng-show="editing" ng-model="value" ng-options="'+ options +'"></select>';

      break;

    case 'number':
      template += '<div class="in-line-value" ng-hide="editing">\n{{value}}</div>';
      template += '<input class="in-line-input form-control"\nng-show="editing" type="number" ng-model="value" step="any"\nmin="0" max="99999" />';

      break;
    default:
      template += '<div class="in-line-value" ng-hide="editing">\n{{value}}</div>';
      template += '<input class="in-line-input form-control"\nng-show="editing" type="text" ng-model="value" />';
    }

    // 关闭外层 div
    template += '</div>';
    newElement = $compile(template)(scope);
    element.replaceWith(newElement);

    scope.$on('$destroy', function () {
      newElement = undefined;
      element = undefined;
    });

    exports.scope = {
      value: '=',
      editing: '=',
      editList: '=',
      displayValue: '='
    };
    exports.restrict = 'E';
    exports.link = link;

    return exports;
  }

app.controller('EmployeesCtrl', ['$scope', 'EmployeeService',
  function($scope, service) {
    service.query(function(data, headers) {
        $scope.employees = data;
    }, _handleError);
}]);

app.controller('EmployeeCtrl', ['$scope', '$routeParams',
  'EmployeeService', 'TeamService', '$q', 'config', '$route',
  function($scope, $routeParams, employee, team, $q, config,
  $route) {

    $scope.address = {};

    function getTeam (teams, teamId) {
      for (var i = 0, l = teams.length; i < l; ++i) {
        var t = teams[i];
        if (t._id === teamId) {
          return t;
        }
      }
    }

    $q.all([
      employee.get({
        employeeId: $routeParams.employeeId
      }).$promise,
      team.query().$promise
    ]).then(function(values) {
      $scope.teams = values[1];
      $scope.employee = values[0];
      $scope.employee.team = getTeam($scope.teams,
        $scope.employee.team._id);
    }).catch(_handleError);

    $scope.editing = false;
    // 为防止多个引用指向同一个数组，我们创建一个新的副本。
    $scope.states = config.states.slice(0);

    $scope.edit = function() {
      $scope.editing = !$scope.editing;
    };

    $scope.save = function() {
      // 为防止数据库中出现空行并保持界面整洁，需要移除所有空白行
      var lines = $scope.employee.address.lines;

      if (lines.length) {
        lines = lines.filter(function (value) {
          return value;
        });
      }

      $scope.employee.address.lines = lines;

      employee.update({
        employeeId: $routeParams.employeeId
      }, $scope.employee, function() {
        $scope.editing = !$scope.editing;
      });
    };

    $scope.cancel = function () {
      $route.reload();
    };

    $scope.address.addLine = function (index) {
      var lines = $scope.employee.address.lines;

      lines.splice(index + 1, 0, "");
    };

    $scope.address.removeLine = function (index) {
      var lines = $scope.employee.address.lines;

      lines.splice(index, 1);
    };
  }
]);

app.controller('TeamsCtrl', ['$scope', 'TeamService',
  function($scope, service) {
    service.query(function (data) {
        $scope.teams = data;
    }, _handleError);
}]);

app.controller('TeamCtrl', ['$scope', '$routeParams', 'TeamService',
  function($scope, $routeParams, service) {
    service.get({
        teamId: $routeParams.teamId
    }, function(data, headers) {
        $scope.team = data;
    }, _handleError);
}]);

function _handleError(response) {
  // 待办事项：此处需要处理错误，可能只需重定向到错误页面
  console.log('%c ' + response, 'color:red');
}
```

**清单 20-4.** app.js 的内容

## 模板文件

我们的应用程序包含五个模板文件：home.html、employees.html、teams.html、employee.html 和 team.html。其中最简单的是 home.html，它用于一个简洁的主页。home.html 的内容如清单 20-5 所示，而渲染后的页面如图 20.2 所示。

```html
<div class="jumbotron hero-spacer">
    <h1>人力资源</h1>
    <p>此页面是您处理所有人力资源相关任务的入口。</p>
</div>
```

**清单 20-5.** 主页模板

![](img/0ca996f5fd0375fc118091628c3c7a87_269_0.png)

图 20.2. 主页视图

## 团队和员工列表视图

团队和员工列表页面的模板代码分别如清单 20-6 和 20-7 所示。两个模板都使用 `ng-repeat` 指令来遍历集合的成员。每个成员都生成一个指向相应团队或员工个人页面的链接。员工列表页面的示例如图 20.3 所示。

```html
<div class="col-xs-12 col-sm-6 col-lg-4" ng-repeat="team in teams">
    <div class="panel panel-default employee-list-item">
        <div class="panel-body">
            <span class="icon-container"><i class="fa fa-3x fa-group"></i></span>
            <span class="h4">{{team.name}}</span>
            <a href="#teams/{{team._id}}" class="btn btn-sm btn-info">
                <i class="fa fa-eye"></i> 查看
            </a>
        </div>
    </div>
</div>
```

**清单 20-6.** 团队列表模板

```html
<div class="col-xs-12 col-sm-6 col-lg-4" ng-repeat="employee in employees">
    <div class="panel panel-default employee-list-item">
        <div class="panel-body">
            <span class="icon-container"><i class="fa fa-3x fa-user"></i></span>
            <span class="h4">{{employee.name.last}}, {{employee.name.first}}</span>
            <span>{{employee.name.first}}</span>
            <a href="#employees/{{employee.id}}" class="btn btn-sm btn-info">
                <i class="fa fa-eye"></i> 查看
            </a>
        </div>
    </div>
</div>
```

**清单 20-7.** 员工列表模板

![](img/0ca996f5fd0375fc118091628c3c7a87_270_0.png)

## 单个团队视图

单个团队页面显示该团队所有成员的列表，因此它与员工列表页面类似。模板文件 team.html 如清单 20-8 所示。该模板相当基础，显示了模型中的几个字段，并使用 `ng-repeat` 来遍历团队的所有成员。渲染后的模板示例如图 20.4 所示。

```html
<ul class="breadcrumb">
  <li><a href="#teams">团队</a></li>
  <li class="active">{{team.name}}</li>
</ul>
<div>
  <h3>{{team.name}}</h3>
</div>
<div>
  <h4>团队成员</h4>
</div>
<div class="col-xs-12 col-sm-6 col-lg-4" ng-repeat="employee in team.members">
  <div class="panel panel-default employee-list-item">
    <div class="panel-body">
      <span class="icon-container"><i class="fa fa-3x fa-user"></i></span>
      <span class="h4">{{employee.name.last}}, {{employee.name.first}}</span>
      <a href="#employees/{{employee.id}}" class="btn btn-sm btn-info">
        <i class="fa fa-eye"></i> 查看
      </a>
    </div>
  </div>
</div>
```

**清单 20-8.** 单个团队模板



图 20.4. 个人团队页面视图

## 个人员工视图

最后一个也是最复杂的模板属于个人员工视图页面。此页面不仅显示员工信息，还允许使用我们的 `customer edit-in-line` 指令更新信息。模板的代码见清单 20-9，渲染后的页面见图 20.5。请注意，目前无法修改用户的个人资料图片。

```html
<ul class="breadcrumb">
  <li><a href="#employees">Employees</a></li>
  <li class="active">{{employee.name.last}}, {{employee.name.first}}</li>
</ul>
<div class="panel panel-default clearfix">
  <div class="panel-body">
    <div class="button-bar">
      <button class="btn btn-warning" ng-click="edit()" ng-hide="editing">Edit</button>
      <button class="btn btn-success" ng-click="save()" ng-show="editing">Save</button>
      <button class="btn btn-danger" ng-click="cancel()" ng-show="editing">Cancel</button>
    </div>
    <div class="col-xs-12 col-md-4 text-center">
      <h3 class="margin-top-reset">{{employee.name.first}} {{employee.name.last}}</h3>
      <img ng-src="{{employee.image}}" image-fallback="images/user.png" class="employee-avatar">
    </div>
    <div class="col-xs-12 col-sm-6 col-md-4 form-offset">
      <div class="form-group">
        <label class="control-label">Employee ID</label>
        <div>#{{employee.id}}</div>
      </div>
      <div class="form-group">
        <label class="control-label">First Name:</label>
        <edit-in-line value="employee.name.first" editing="editing" />
      </div>
      <div class="form-group">
        <label>Last Name:</label>
        <edit-in-line value="employee.name.last" editing="editing" />
      </div>
      <div class="form-group">
        <label>Team:</label>
        <edit-in-line value="employee.team" editing="editing" specialised="teams" edit-option="t.name for t in teams" edit-type="select" display-value="employee.team.name" />
      </div>
    </div>
    <div class="col-xs-12 col-sm-6 col-md-4 form-offset">
      <div class="form-group">
        <label class="control-label">Address</label>
        <ul class="address-lines">
          <li ng-repeat="line in employee.address.lines track by $index">
            <span ng-hide="editing">{{line}}</span>
            <div ng-show="editing" class="input-group address-edit">
              <input type="text" class="form-control" ng-model="employee.address.lines[$index]" />
              <span class="input-group-btn">
                <button ng-click="address.addLine($index)" class="btn btn-success">
                  <i class="fa fa-plus"></i>
                </button>
                <button ng-click="address.removeLine($index)" ng-disabled="employee.address.lines.length === 1" class="btn btn-danger">
                  <i class="fa fa-trash-o"></i>
                </button>
              </span>
            </div>
          </li>
          <li>
            <edit-in-line value="employee.address.city" editing="editing" />
          </li>
          <li>
            <span ng-hide="editing">{{employee.address.state}}, {{employee.address.zip}}</span>
          </li>
          <li ng-show="editing">
            <edit-in-line ng-show="editing" edit-type="select" value="employee.address.state" editing="editing" edit-list="states" edit-option='s for s in states' />
          </li>
          <li ng-show="editing">
            <edit-in-line value="employee.address.zip" editing="editing" edit-type="number" />
          </li>
        </ul>
      </div>
    </div>
  </div>
</div>
```

## 清单 20-9. 个人员工模板

图 20.5.

# 总结

鼓励读者尝试并扩展现有的 HR 示例应用。你可以从添加新数据点开始，例如员工薪资。如果你想添加更高级的功能，可以实现更新员工个人资料图片的功能，或添加一个用于在团队间拖动员工的新视图。

本章结束了我们对 MEAN 技术栈的探讨。这二十章应为你奠定了 MEAN 技术及其一些替代方案的坚实基础。本书的其余部分将教你关于围绕 MEAN 技术栈的其他 JavaScript 工具。这些工具包括任务运行器、调试器和测试框架。

# 任务运行器

在我们许多 Angular 章节中展示的示例中，所有 JavaScript 代码都位于单个文件中。使用单个文件有几个好处。浏览器只需要下载一个包含所有 JavaScript 的文件，并且可以在站点的任何地方重用缓存版本。它还减少了下载顺序问题，因为所有内容都包含在一个文件中，并且代码按照正确、逻辑的顺序排列。整个代码块可以包装在函数表达式中，将内容与全局命名空间隔离。最后，压缩可以减少浏览器下载大小，有时多达 80%。使用单个文件的缺点是维护，尤其是在团队协作中。每个开发人员都会编辑同一个文件，导致源代码控制中的冲突；此外，在包含一万行代码的文件中定位特定代码进行修改或修复错误可能非常困难。

将客户端 JavaScript 拆分为多个文件使其更易于维护。开发人员可以只处理特定于某个文件的功能或错误，从而大幅减少变更管理冲突。它还让你的 Web 应用程序更容易理解，因为每个文件代表整个应用程序的一个独立部分或功能。缺点是每个 JavaScript 文件都需要从浏览器单独下载。如果一个文件需要来自另一个文件的特性，那么 `script` 标签的顺序就变得非常重要。资源分片也可能很困难，因为你失去了对整个下载顺序的控制。

我们真正想要的是能够以任何我们想要的方式编写文件，并让一个过程将它们转换为最佳实践的静态资源文件。这就是**任务运行器**的用途。它们是一系列自动运行或按需运行的任务，帮助管理我们的客户端资源。任务运行器的功能远不止管理多个 JavaScript 文件；它们可以用于编译 CoffeeScript、制作 CSS 精灵图、压缩和调整图像大小、运行 CSS 预处理器（如 Stylus 或 LESS）、运行 JavaScript 代码检查工具以及处理许多其他资产管理工作。

## 介绍 Gulp

Gulp 是一个用 JavaScript 编写的、面向 Node 的简单异步任务运行器。它相对较新，但由于其核心架构设计模式——利用管道和流，已经获得了巨大的社区采用率。如果你跳过了本书的那部分内容，我们建议你现在回去阅读。

我们将假定你对这两个核心概念有基本的理解，然后继续。Gulp 架构的第二个决策也符合 Node 的整体设计哲学：通过模块和插件实现代码专业化。

总体而言，Gulp 提供底层功能。它有一些内置的方法和属性，例如任务管理和文件监视，但大部分功能来自 Gulp 插件。这听起来应该与 Node 架构相似。迄今为止，已有超过 600 个 Gulp 插件。指导 Gulp 插件的一个核心设计原则指出：

> 你的插件应该只做一件事，并且把它做好。

所有 Gulp 插件都执行一个专门的任务。知道这一点将在本章后面我们设计 Gulp 工作流时对我们有所帮助。你希望发生的每个任务都将通过单个 Gulp 插件来实现。一个流（通常是文件流）被管道传输到一系列转换流中，这些转换流以特定方式修改传入的流，并将结果管道传输到下一个流。每个操作都由一个独特的 Gulp 插件处理。

## 设置 Gulp

首先，在你的开发机器上全局安装 gulp，使用 `npm install gulp -g`。这将把 gulp CLI 工具添加到你的环境中。你还需要本地安装 gulp，以便可以从脚本文件中引用它。其次，在你的项目中创建一个名为 `gulpfile.js` 的空脚本文件。最后，我们将创建一些 Stylus 和 JavaScript 文件来处理。在项目根目录下创建两个新文件夹：`./assets/style` 和 `./assets/javascript`。在 `./assets/style` 内部，创建 `one.styl` 和 `two.styl`。如果你不熟悉 [Stylus](https://stylus-lang.com/)，它是特定于 Node 的 CSS 预编译器。如果你有兴致，可以在这两个文件中编写自己的样式；否则，你可以复制这些样式。

```stylus
html
  font-size: 62.5%

body
  background-color: #000
  width: 90%
  max-width: 900px
```

```stylus
.container
  background-color: #CAD
  color: #EEE

h2
  font-size: 1.4rem
  font-weight: bold
```

**清单 21-1. 两个示例 Stylus 文件**

对于 JavaScript，我们将参考第 19 章中的客户端路由示例，并将代码分散到 `./assets/javascript` 下的三个不同文件中。查看下面的示例文件，你应该能看到一个潜在问题，如果我们不控制文件排序的话。如果 `view_controller.js` 的内容出现在 `mainapp.js` 的内容之前，就会发生错误，因为 `app` 将是未定义的。为了防止这种情况，我们将确保在构建脚本中正确排序文件，而不依赖任何排序方法。

```javascript
var app = angular.module('app', ['ngRoute', 'ngResource']);

app.config(['$routeProvider', function($routeProvider) {
  // 完整代码见清单 19-2
}]);

app.factory('EmployeeService', ['$resource', function($resource) {
  // 完整代码见清单 19-3
}]);
```

```javascript
app.controller('view', ['$scope', 'EmployeeService',
```



 ```javascript
function($scope, EmployeeService) {
  // See Listing 19-3 for complete code
}]);
```

edit_controller.js

```javascript
app.controller('edit', ['$scope', 'EmployeeService','$routeParams',
  function($scope, EmployeeService, $routeParams) {
  // See Listing 19-3 for complete code
}]);
```

With these files in place, we are ready to start building our Gulp file.

## 设计 Gulp 文件

在本节中，我们将编写一个包含两个任务的 Gulp 文件：css 和 javascript。每个任务负责处理 ./assets 目录下的文件，以生成经过优化的浏览器兼容文件。在开始编码之前，我们先列出每个任务需要履行的职责清单。这在开始编程时会非常有用。

### 样式表文件

1. 将所有 Stylus 文件编译为纯 CSS
2. 对 CSS 进行压缩以减小文件大小
3. 将所有 CSS 文件合并为一个文件
4. 将压缩后的版本写入 ./public/css/main.min.css

### JavaScript 文件

1. 按正确顺序将所有 JavaScript 文件合并为一个文件
2. 将代码包装在函数中，以防止数据进入全局命名空间
3. 运行 linter ([JSHint](https://jshint.com)) 并报告任何代码问题
4. 将非压缩版本写入 ./public/javascript/main.js
5. 对代码进行压缩以减小文件大小
6. 将压缩版本写入 ./public/javascript/main.min.js

### css 任务

每个 Gulp 文件都应该至少有一个默认任务：default。声明任务的语法很简单：gulp.task('default', function() {})。default 是当你从命令行执行 gulp 时，gulp 命令会尝试运行的任务。在回调函数内部，你可以启动任何其他已定义的任务。让我们从声明 default 和 css 任务开始：

```javascript
var gulp = require('gulp');

gulp.task('css', function() {
  // Transform contents of one.styl and two.styl to CSS
});

gulp.task('default', function() {
  gulp.start('css');
});
```

### 清单 21-2. Gulp 文件存根

在清单 21-2 中，我们创建了 default 任务和 css 任务的存根。在 default 任务内部，我们执行 gulp.start('css')，这将启动 css 任务。

如果回顾这个任务需要完成的职责清单，第一项是"将所有 Stylus 样式表编译为纯 CSS"。gulp-stylus 将现有的 Stylus 编译器包装在 Gulp 接口中，并通过函数选项压缩结果。本地安装 gulp-stylus，并确保在执行时更新 package.json 文件。

```javascript
var stylus = require('gulp-stylus');

gulp.task('css', function() {
  gulp.src('./assets/style/*.styl')
    .pipe(stylus({
      compress: true
    }))
    .pipe(gulp.dest('./public/css'));
});
```

### 清单 21-3. 编译并写入 Stylus 文件

第一行指示 Gulp 为 ./assets/style/ 下所有具有 .styl 扩展名的文件创建文件流。我们希望将其传送到 stylus 插件，该插件会将文件编译为压缩的 CSS。最后，我们希望将结果传送到 gulp.dest，后者会将结果写入 ./public/css。如果从命令行运行 gulp，你会看到一些日志信息，最后显示 default 已完成。

如果你打开 ./public/css，会看到 one.css 和 two.css。它们将是标准的、压缩的 CSS 文件。剩下的工作就是将它们合并为单个文件。有多种方法可以仅使用 Stylus 来完成此操作，但这需要以不同方式编写文件；为简洁起见，我们只需将它们作为字符串连接到一个输出文件中。

```javascript
var concat = require('gulp-concat');

gulp.task('css', function() {
  gulp.src('./assets/style/*.styl')
    .pipe(stylus({
      compress: true
    }))
    .pipe(concat('main.min.css', {
      newline: ''
    }))
    .pipe(gulp.dest('./public/css'));
});
```

### 清单 21-4. 连接 CSS 文件

在清单 21-4 中，我们加载了 gulp-concat，它用于将文件连接在一起。我们将 stylus 的结果传送到 concat，将文件命名为 main.css，并传递了一个选项，指定 newline 为空字符串。如果你重新运行 gulp，现在应该在 ./public/css 中看到一个单一的 main.css 文件。

这应该是我们的 css 任务所需的全部内容。如果你回顾 *样式表文件* 下的步骤，每一步都与清单 21-4 中的代码紧密对应。所有 Stylus 文件都被编译、压缩，并合并为单个文件，我们的 Web 服务器可以将其发送给客户端。

### javascript 任务

让我们将 css 任务中学到的知识应用到 javascript 任务中。我们希望在此任务中执行一些相同的职责（传送特定文件夹中的文件、将它们合并为一个、压缩它们，然后将它们写入其他位置）。由于我们在清单 21-4 中已经涵盖了许多基础知识，我们可以将其作为清单 21-5 的起点。

```javascript
var jsSource = './assets/javascript/';
gulp.task('javascript', function() {
    Alc return gulp.src([jsSource + 'mainapp.js',
                     jsSource + 'edit_controller.js',
                     jsSource + 'view_controller.js'])
        .pipe(concat('main.js'))
        .pipe(gulp.dest('./public/javascript'))
});
```

```javascript
gulp.task('default', function() {
    gulp.start('javascript');
    gulp.start('css');
});
```

**清单 21-5.** 合并 JavaScript 文件

这里我们只是设置基础部分：声明 javascript 任务，将该目录中的所有 .js 文件合并为 main.js，并将结果写入 ./public/javascript。我们还应该在 default 任务内部添加 javascript 任务的启动命令。如果现在运行 Gulp 文件，你会在 ./public/javascript 中看到 main.js 文件。

请记住，JavaScript 文件合并的顺序很重要。为了在处理过程中控制顺序，我们将文件路径数组传递给 gulp.src，而不是使用通配符。参数的顺序就是 Gulp 将处理文件的顺序。这样，我们就可以控制顺序，并防止在文件合并时引入任何与文件顺序相关的错误。

让我们扩展示例，在 ./public/javascript 中创建一个压缩副本。

```javascript
var rename = require('gulp-rename');
var uglify = require('gulp-uglify');
var jsSource = './assets/javascript/';
```

```javascript
gulp.task('javascript', function() {
    gulp.src([jsSource + 'mainapp.js',
               jsSource + 'edit_controller.js',
               jsSource + 'view_controller.js'])
        .pipe(concat('main.js'))
        .pipe(gulp.dest('./public/javascript'))
        .pipe(rename({
            suffix: '.min'
        }))
    .pipe(uglify())
    .pipe(gulp.dest('./public/javascript'))
});
```

**清单 21-6. 压缩 JavaScript 文件**

在清单 21-6 中，我们添加了两个新的 Gulp 插件，*rename* 和 *uglify*。在写入合并后的文件 main.js 后，我们想要复制该文件并将其重命名为 main.min.js，然后将该结果传送到 uglify。uglify 是 [UglifyJS2](https://github.com/mishoo/UglifyJS2) 的 Gulp 插件包装器，用于压缩（或减小）生成的 JavaScript 字符串。然后将该结果传送到 gulp.dest，main.min.js 被写入我们的公共 JavaScript 文件夹。

如果现在重新运行 gulp，你应该会在 JavaScript 目录中看到压缩版本和普通版本的两个 main 文件。剩下的工作就是将所有代码包装在一个立即执行函数表达式中，并将结果通过 linter 运行，此处为 JSHint。如果你不熟悉 linter，它们会警告开发人员常见的 JavaScript 错误，并强制执行样式规则。

```javascript
var wrap = require('gulp-wrap');
var jshint = require('gulp-jshint');
var jsSource = './assets/javascript/';

gulp.task('javascript', function() {
    gulp.src([jsSource + 'mainapp.js',
    jsSource + 'edit_controller.js',
    jsSource + 'view_controller.js'])
        .pipe(concat('main.js'))
        .pipe(wrap('(function(a, window){<%= contents %>}(angular, window));'))
        .pipe(jshint({
            predef: ['window', 'angular']
        }))
        .pipe(jshint.reporter('default'))
        .pipe(gulp.dest('./public/javascript'))
        .pipe(rename({
            suffix: '.min'
        }))
        .pipe(uglify())
        .pipe(gulp.dest('./public/javascript'))
});
```

**清单 21-7. 我们最终的 JavaScript 任务**

最后，我们在 Gulp 任务中添加了 wrap 和 jshint。wrap 实现了 Gulp 接口，用于使用 [lo templates(lo-dash 模板](https://lodash.com/docs#template) 包装流内容。这使我们能够将连接后的输出 contents 包装在函数表达式中。

然后将该结果传送到 jshint Gulp 插件。该插件将核心 [JSHint](http://jshint.com/) 功能包装在 Gulp 包装器中。你可以通过插件直接提供，或通过配置文件为 JSHint 提供多种配置选项。对于我们的示例，我们只需向 jshint 提醒全局变量 window 和 angular，因为它们来自外部源。JSHint 的结果被传送到 reporter，后者会将结果记录到控制台。



最后，你需要更新所有`script`标签，使其引用`/javascript/main.js`或`/javascript/main.min.js`，具体取决于你的部署环境。

## watch 任务

让我们再添加一个基础任务，纯粹为了方便。如果你一直在跟着操作，应该会注意到每次 JavaScript 和 Stylus 源文件在 `assets` 中发生更改时，都必须重新运行 `gulp`。如果 Gulp 能在源文件更改时自动运行，那就方便多了。让我们再创建一个任务，用于监视 assets 文件夹，一旦文件发生更改，就运行相应的任务。

```
gulp.task('watch', function() {
  gulp.watch('./assets/javascript/*.js', ['javascript']);
  gulp.watch('./assets/style/*.styl', ['css']);
});
```

**代码清单 21-8.** 创建一个 watch 任务

这个任务使用了 `gulp.watch`，它会监视匹配的文件是否有更改。当发生更改时，它会 `gulp.start` 第二个参数中列出的每个任务。现在你可以打开一个新的终端会话，运行 `gulp watch`，Gulp 将持续运行并监视 `assets` 下文件的更改，在必要时运行相应的任务。

# 小结

在本章中，我们介绍了任务运行器，它们也可以被称为构建脚本。任务运行器接收客户端资源，并将其转换为更优化、更浏览器友好的格式。这使开发者能够利用更好的代码组织方式以及更高级的语言，如 Stylus 或 CoffeeScript。

然后我们介绍了任务运行器 Gulp。Gulp 是一个流和管道系统，使其非常快速且易于使用。Gulp 中的每个操作通常都可以归结为流操作，这些操作由 Gulp 插件处理。单个插件的结果会被管道传输到下一个插件，从而形成一个 Gulp 任务。

最后，我们编写了一个功能完整的 gulpfile.json，其中包含一个处理 Stylus 文件的任务和一个管理 JavaScript 文件的任务。`css` 任务将 Stylus 编译为标准 CSS，合并两个文件，并将结果压缩为 main.min.css。`javascript` 任务要复杂得多；它合并了多个文件，创建了压缩和未压缩两个版本，通过 JSHint 检查代码质量，并将所有内容包装在一个函数表达式中。

我们通过创建一个 `watch` 任务来结束对 Gulp 的讨论，该任务监视特定文件的更改，并在发生更改时运行任务。这使得使用构建步骤几乎完全透明。

Gulp 是一个非常简单且强大的任务运行器。它拥抱了许多与 Node 核心相同的核心理念。如果你理解管道和流，你可以很快上手 Gulp。我们希望这展示了为你的网站使用任务运行器的实用性和灵活性。

# 第 22 章

# 调试

不幸的是，编写软件时 Bug 是不可避免的，无论你使用什么语言。**调试**，顾名思义，就是追踪并修复 Bug 的过程。调试的过程可以简单到在你的代码中添加 console.log() 调用来验证某些变量是否持有预期值。但对于更复杂的 Bug，你会想要使用调试器。调试器在追踪 Bug 方面非常有效，因为它们允许你逐行逐步执行应用程序，检查（和修改）变量值。

本章将教你如何使用 Google Chrome 的 DevTools 来调试 JavaScript 应用程序。所有现代浏览器都有类似的调试功能，但我们选择专注于 Chrome 有两个原因。首先，在撰写本文时，Chrome 是桌面和移动市场中最流行的浏览器。其次，Node 有一个名为 node-inspector 的优秀调试器，可以与 DevTools 配合使用。

## debugger 语句

所有主要的 JavaScript 环境（浏览器、Node.js 等）都带有内置的调试器；然而，调试器通常默认未启用。在调试器启用的状态下运行应用程序的过程被称为"附加调试器"，每个调试器的具体操作略有不同。JavaScript 的 debugger 语句用于在附加了调试器的情况下调用调试器。如果应用程序没有关联的调试器，debugger 语句将不起任何作用。

为了说明 debugger 语句是如何工作的，让我们看看代码清单 22-1 中的示例。此页面上的 JavaScript 在变量 i 和 j 相等时显示一条问候语。因此，为了让我们的程序正常运行，我们希望这两个值相等。查看代码，显然它们不相等，但出于本示例的目的，我们想看看为什么 if 语句内部的代码没有执行。

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Debugging Intro</title>
</head>
<body>
  <span></span>
  <script>
    var span = document.querySelector('span');
    var i = 0;
    var j = 1;

    if (i === j) {
      span.innerText = 'Hello!';
    }
  </script>
</body>
</html>
```

**代码清单 22-1.** 一个行为异常的 HTML 页面

同样的代码在代码清单 22-2 中再次展示，但在这个示例中，在 if 语句之前添加了一个 debugger 语句。现在在 Chrome 中打开此页面，你会发现什么都没发生——没有问候语，没有调试器魔法，什么都没有。我们还没有启用调试工具，所以 debugger 语句没有做任何事情。让我们改变这一点。

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Debugging Intro</title>
</head>
<body>
  <span></span>
  <script>
    var span = document.querySelector('span');
    var i = 0;
    var j = 1;

    // 在条件语句之前设置断点
    debugger;

    if (i === j) {
      span.innerText = 'Hello!';
    }
  </script>
</body>
</html>
```

**代码清单 22-2.** 与代码清单 22-1 相同的页面，添加了 debugger 语句

## 运行 Chrome 的调试器

通过右键单击页面并点击"检查"来打开 Chrome 的开发者工具。接下来，刷新页面。在启用开发者工具的情况下执行此操作，调试器就会被附加。这次，你应该会激活调试器，如图 22.1 所示，它显示了文件和执行在 debugger 语句处暂停的行。这种预定义的执行暂停被称为**断点**。在图像的右侧，注意到两个面板：Scope Variables 和 Global。这些面板可以展开，分别查看局部作用域和全局作用域中的变量和值。我们的代码当前正在全局作用域中执行，因此 Scope Variables 面板中没有列出任何内容。展开 Global 面板并向下滚动，直到找到 `i` 和 `j`（你可能需要滚动相当长的一段距离，因为全局作用域中定义了很多项目，如浏览器 API 对象）。你会看到 `i` 为零，`j` 为一。

![figure](img/0ca996f5fd0375fc118091628c3c7a87_287_0.png)

## 控制调试器

现在我们可以看到变量的值了，让我们逐步执行 if 语句，看看它是否被执行（尽管我们知道它没有）。图 22.2 显示了调试器，其中控制按钮被高亮显示。这六个按钮，从左到右，允许你恢复执行、单步跳过函数、单步进入函数、单步跳出函数、停用断点以及在异常处中断。

![figure](img/0ca996f5fd0375fc118091628c3c7a87_288_0.png)

恢复按钮将使应用程序开始正常执行，直到遇到另一个断点或程序结束。单步跳过和单步进入按钮用于执行下一行代码。如果该行是一个函数，单步跳过会将其视为单行代码，而单步进入则允许你逐行调试函数。单步跳出按钮会使调试器正常执行当前函数的其余部分，然后继续调试。

### 提示：暂停执行会禁用刷新

如果执行在调试器中暂停，你可能无法刷新页面。你可以通过退出 DevTools 或按恢复按钮来解决这个问题。但是，按恢复按钮可能会导致执行暂停，如果遇到另一个断点的话。

停用断点按钮会导致将来遇到的断点被忽略。如果启用了此功能并刷新页面，debugger 语句将无法暂停执行。异常处暂停按钮会导致未捕获的异常被视为断点。启用此功能时，会显示一个复选框，允许你也选择在已捕获的异常处暂停。

现在我们已经介绍了基本的调试器控制，刷新页面以便你在 debugger 语句处暂停。按单步跳过或单步进入按钮前进到 if 语句。再次按该按钮，并注意到 if 语句内部的代码没有执行。接下来，我们将看看如何在调试器中修改变量值以测试不同的场景。

## 修改变量

调试器运行时，有几种方法可以修改变量。最简单的方法是在 Scope Variables 或 Global 面板中找到变量，双击变量名，然后编辑变量的值。请注意，对这些值所做的任何更改即使在调试器之外也会持续存在。

例如，刷新页面，在 Global 面板中找到变量 j，并将其值设为零。如果你逐步执行 if 语句，你会发现条件现在 evaluates 为 true。同样，如果你设置了 j 的值并直接恢复执行，

页面将显示预期的问候语。

检查和修改值的第二种方法是切换到控制台（Console）标签页。这为你提供了一个功能齐全的 REPL 环境。在我们的示例中，你可能会切换到控制台标签页，检查并设置一些值，然后切换回调试器控制所在的源代码（Sources）标签页。图 22.3 展示了一个使用控制台标签页的示例。

在控制台标签页中运行这些命令后，切换回调试器控制，然后单步执行或直接恢复执行，问候语就应该会显示出来。

![](img/0ca996f5fd0375fc118091628c3c7a87_289_0.png)

图 22.3. 使用调试器控制台

我们相信，凭借你新掌握的调试技能，你能够找出导致我们简单页面的问候语无法显示的那一行代码。现在，我们将在 Node.js 中探讨同样的问题。

## Node 的调试器

Node 自带一个内置调试器。需要提醒的是，它并不是太用户友好，这就是为什么我们稍后会介绍 node-inspector。要将调试器附加到你的应用程序，请使用 debug 标志运行 node，如清单 22-3 所示。app.js 的内容如清单 22-4 所示。

```
node debug app.js
```

**清单 22-3.** 以交互式调试模式运行 Node 应用程序

```
var i = 0;
var j = 1;

// 在条件语句前设置一个断点
debugger;

if (i === j) {
  console.log('Hello!');
}
```

**清单 22-4.** 来自清单 22-3 的 app.js 内容

使用 debug 标志运行会启动一个交互式调试器会话，它会在应用程序的第一行设置一个断点，如清单 22-5 所示。请注意，代码旁边打印了行号，`>` 字符表示当前行。

```
< Debugger listening on port 5858
connecting to port 5858... ok
break in app.js:1
> 1 var i = 0;
  2 var j = 1;
  3
debug>
```

**清单 22-5.** 在交互式调试模型中启动 app.js 的输出

> ### 提示：-debug 和 –debug-brk

debug 参数启动一个交互式调试器会话；但是，你也可以使用 –debug 或 –debug-brk 参数，这会使调试器监听端口 5858 上的连接。–debug 和 –debug-brk 之间的区别在于，–debug-brk 还会在应用程序的第一行设置一个断点。你也可以使用 –debug-port 参数更改调试端口。例如，node –debug-port=4000 –debug-brk app.js 将在 app.js 的第一行设置断点，并在端口 4000 上监听调试器连接。

你可以通过在 debug> 提示符下输入命令来控制调试器。表 22-1 提供了基本调试器命令的列表，这些命令不言自明。请注意 cont、next、step 和 out 命令与 DevTools 调试器控制之间的相似之处。另请注意，你可以使用 **Control-C** 或 **Control-D** 退出调试器。

## 表 22.1. 有用的调试器命令

| 命令 | 描述 |
|---------|-------------|
| cont 或 c | 恢复执行 |
| next 或 n | 单步执行到下一条指令 |
| step 或 s | 步入函数调用 |
| kill | 终止正在执行的脚本 |
| restart | 重启脚本 |
| pause | 暂停运行中的代码 |
| scripts | 列出所有已加载的脚本 |
| list(n) | 显示源代码，显示当前行之前 n 行和之后 n 行 |

在 Node 调试器中检查和修改变量有点棘手。你不能直接从调试器访问变量。相反，你必须发出 `repl` 命令。这将在调试器中启动一个 REPL，你可以在其中发出 JavaScript 命令。完成后，你必须使用 **Control-C** 退出 REPL 以返回调试器。在 REPL 中对变量所做的任何更改都将保留。

清单 22-6 展示了一个完整的 app.js 运行过程，其中将 j 设置为零，以便显示问候语。请注意，此示例需要 Node 0.11 才能正常运行。在 Node 0.10 中运行会导致变量无法正确更新。总之，如果仅仅为了将值从一更改为零并执行一个 if 语句就需要这样一个繁琐的过程，你是对的。这就是 node-inspector 被创建的原因。

```
< Debugger listening on port 5858
connecting to port 5858... ok
break in app.js:1
> 1 var i = 0;
  2 var j = 1;
  3
debug> c
break in app.js:5
  3
  4 // Set a breakpoint before the conditional
> 5 debugger;
  6
  7 if (i === j) {
debug> repl
Press Ctrl + C to leave debug repl
> j
1
> j = 0;
0
debug> n
break in app.js:7
  5 debugger;
  6
> 7 if (i === j) {
  8   console.log('Hello!');
```

```
debug> n
break in app.js:8
  6
  7 if (i === j) {
> 8   console.log('Hello!');
  9 }
 10 });
```

```
debug> n
< Hello!
break in app.js:10
  8 console.log('Hello!');
  9 }
>10 });
debug>
```

**清单 22-6. 通过 Node 调试器修改变量**

```
debug> repl
Press Ctrl + C to leave debug repl
> j
1
> j=0;
0
> j
1
```

## node-inspector

node-inspector 是一个第三方模块，它在 Node 的内置调试器和 Chrome 的 DevTools 界面之间创建了一个接口。第一步是使用清单 22-7 中所示的命令安装 node-inspector。

```
npm install node-inspector -g
```

**清单 22-7.** 全局安装 node-inspector

接下来，使用 `--debug` 或 `--debug-brk` 标志运行你的应用程序。这个选择将取决于你的应用程序的性质。如果是一个等待连接的服务器，那么 `--debug` 就可以了；但是，如果你的应用程序在启动时就会运行到完成，你将需要使用 `--debug-brk` 来创建一个断点。对于像清单 22-4 中那样的基本应用程序，我们将使用 `--debug-brk`，如清单 22-8 所示。

```
node --debug-brk app.js
```

**清单 22-8.** 使用 `--debug-brk` 标志启动应用程序

接下来，在一个单独的终端窗口中启动 `node-inspector`。它将连接到在你的应用程序中运行的调试器。清单 22-9 显示了发出的命令和产生的输出。

```
node-inspector
Node Inspector v0.7.4
Visit http://127.0.0.1:8080/debug?port=5858 to start debugging.
```

**清单 22-9.** 使用 node-inspector 连接到你的应用程序的调试器

注意 URL `http://127.0.0.1:8080/debug?port=5858`。如果你在 Chrome 中访问此 URL，你将看到 DevTools 界面。你可能会注意到代码不熟悉。这是因为断点是在你的应用程序运行之前设置的。按下恢复按钮，你将进入你的应用程序代码，如图 22.4 所示。从这里，你可以访问本章前面介绍的所有熟悉的 DevTools 功能。查看展开的 `Scope Variables`（作用域变量）面板中的值。你将看到你的应用程序变量 `i` 和 `j`，以及熟悉的 Node 变量，如 `__dirname`、`__filename` 和 `exports`。

![](img/0ca996f5fd0375fc118091628c3c7a87_294_0.png)

## node-debug

node-inspector 在可用性方面远超 Node 内置调试器。然而，运行你的应用程序和 node-inspector，以及打开一个浏览器窗口，都是可以自动化的重复性任务。[node-debug](https://www.npmjs.com/package/node-debug) 模块使得使用 node-inspector 调试变得极其简单。首先安装 node-debug，如清单 22-10 所示。

```
npm install node-debug -g
```

**清单 22-10.** 全局安装 node-debug

现在，任何时候你想使用 node-inspector，只需使用 node-debug 而不是 node 来启动你的应用程序，如清单 22-11 所示。这将自动打开 DevTools 并连接到你的 Node 应用程序。

```
node-debug app.js
```

**清单 22-11.** 通过 node-debug 运行 node-inspector

node-inspector 的维护者发现这个功能非常有用，以至于他们已经将其添加到最新版本中，这使得这个模块实际上已经过时。node-inspector 很贴心地保留了 `node-debug app.js` 接口，以避免混淆并保持向后兼容性。

# 总结

本章向你介绍了 JavaScript 应用程序调试。它首先教你 Chrome 的 DevTools 调试器基础知识，但是，像往常一样，关于 DevTools 还有很多东西需要学习。我们鼓励你通过 [DevTools 文档](https://developers.google.com/web/tools/chrome-devtools/) 来学习更多。然后，本章转向了 Node 的内置调试器，遗憾的是，它远非用户友好。最后，我们介绍了 node-inspector，这是一个使用 DevTools 作为 Node 调试器之上更可适应接口的工具。



# 第23章

# 测试

没有人会质疑为软件编写测试的价值。虽然关于哪种测试方法更好或更全面的争论一直存在，但有一个所有开发人员都能认同的事实：任何生产代码都应该有全面的测试。在测试良好的软件中，测试代码的数量往往会超过功能代码的数量。测试为优化、重构和升级代码提供了安全保障，无需担心引入意外的错误。良好的测试还能帮助开发人员在代码部署到生产环境之前发现问题。在结合了多个框架和库的现代Web应用中，适当的测试是确保一切继续顺利运行的最可靠方式。

JavaScript也不例外。甚至可以说，由于该语言的弱类型特性，JavaScript需要*更多*的测试。JavaScript在不同浏览器中的实现差异也增加了彻底测试客户端JavaScript的必要性。即使在使用Express和Angular等经过充分测试的框架时，你也应该有覆盖应用代码的单元测试。

在本章中，我们将使用测试框架来介绍Express服务器和Angular应用的测试。我们建议始终使用测试框架，而不是一长串的`if`和`else`语句。

框架提供了结构化的测试方法，提供了不同的报告选项，并使测试代码的维护更加容易。本章介绍的框架远非唯一可用的测试框架，但它们是我们要重点展示的框架。

## Node测试

有许多模块和框架可用于测试Node应用。就本书而言，我们将重点介绍一个名为[Mocha](https://mochajs.org/)的框架。我们选择重点介绍Mocha，因为它非常受欢迎，并且可以在Node和浏览器中运行。Mocha可以通过npm安装，如清单23-1所示。

```
npm install -g mocha
```

**清单 23-1.** 通过npm安装Mocha

安装Mocha后，你可以通过执行`mocha`命令来调用它。这将尝试执行当前目录下`test`目录中的任何JavaScript文件。如果该目录不存在，mocha将尝试运行名为`test.js`的JavaScript文件。或者，你也可以将想要执行的文件名作为参数传递给mocha。

### 定义测试

当Mocha执行文件时，它期望使用`it()`函数来定义测试。`it()`接受两个参数。第一个是描述测试功能的字符串，第二个是表示测试的函数。一个文件可以包含任意数量的测试。如果测试运行完成，则视为通过；如果抛出异常，则视为失败。

测试还可以按层次结构分组为**测试套件**，这些套件也可以嵌套在层次结构中。套件使用`describe()`函数定义。`describe()`也接受两个参数。第一个是描述测试套件的字符串。第二个参数是包含零个（尽管空套件没什么用）或多个测试的函数。

清单23-2展示了一个Mocha可以理解的示例文件。该文件包含一个顶层测试套件、一个嵌套测试套件和四个测试。测试1和测试2属于嵌套套件，测试3属于顶层套件，测试4不属于任何套件。严格来说，Mocha定义了一个无名的顶层套件，包含所有其他内容，包括测试4。将此代码保存在名为`test.js`的文件中，然后运行命令`mocha`。你应该会看到类似于清单23-3的输出。注意测试2失败了，因为它抛出了异常。你的输出可能包含额外的错误堆栈跟踪，这里已省略。

```
describe('Top Level Tested Suite', function() {
  describe('Nested Test Suite', function() {
    it('Test 1', function() {
    });

    it('Test 2', function() {
      throw new Error('problem');
    });
  });

  it('Test 3', function() {
  });
});

it('Test 4', function() {
});
```

**清单 23-2.** 一个包含套件和测试的示例Mocha输入文件

> **注意：** Mocha的测试接口
>
> Mocha提供了几种[测试接口](https://)。最流行的两种是行为驱动开发（BDD）和测试驱动开发（TDD）。每个接口中可用的函数相同，但名称不同。例如，describe()和it()是BDD函数。等效的功能可以通过TDD接口中的suite()和test()函数获得。本书使用BDD函数。

```
✓ Test 4
Top Level Tested Suite
  ✓ Test 3
  Nested Test Suite
    ✓ Test 1
    1) Test 2

3 passing (8ms)
1 failing

1) Top Level Tested Suite Nested Test Suite Test 2:
   Error: problem
```

**清单 23-3.** 运行清单23-2中代码的示例输出

### 异步测试

Node通常与异步代码相关联。为了让Mocha在Node中很好地工作，它需要支持异步测试。对于异步代码而言，将测试标记为通过是不够的，因为函数很可能在某个长时间运行的异步操作仍在进行时就已完成。

Mocha支持异步测试，允许你向it()传递一个回调函数。这个回调通常按惯例命名为done。调用done()表示测试成功，而失败仍然通过抛出异常来标记。清单23-4展示了一个异步测试的示例。在此示例中，对名为some_file.txt的文件调用fs.readFile()。如果错误被传递给readFile()的回调，则将其作为异常抛出，导致测试失败。如果没有错误，则调用done()，测试通过。

```
var fs = require('fs');

it('Asynchronous Test', function(done) {
  fs.readFile('some_file.txt', function(error, data) {
    if (error) {
      throw error;
    }

    done();
  });
});
```

**清单 23-4.** 一个读取文件的异步测试

### skip()和only()

Mocha允许你选择性地运行测试或套件的某个子集。skip()和only()方法分别用于表示某个测试应该被跳过还是运行。skip()在测试由于某种原因需要暂时禁用时非常有用。only()在标记几个测试来运行而无需注释掉大量代码时非常有用。清单23-5展示了使用skip()的示例。如果你通过Mocha运行此代码，只有测试2会执行。如果你将skip()替换为only()，那么只有测试1会执行。还要注意，此示例将skip()应用于测试。同样的操作也可以应用于整个测试套件（describe.skip()）。

```
it.skip('Test 1', function() {
});

it('Test 2', function() {
});
```

**清单 23-5.** 使用skip()的示例

### 测试钩子

Mocha提供了可选的钩子，可用于在测试运行前后执行代码。这对于在测试前设置数据以及在测试后清理非常有用。具体来说，有四个钩子可以与测试套件相关联：

- before() — 在测试套件执行前运行一次
- beforeEach() — 在套件中的每个测试执行前运行
- after() — 在测试套件执行后运行一次
- afterEach() — 在套件中的每个测试执行后运行

这四个函数都将一个函数作为唯一的参数。如果你需要在这些钩子中执行异步代码，将done()传递给函数参数。

清单23-6展示了一个包含两个测试和所有四个钩子函数的示例测试套件。运行此代码的输出如清单23-7所示。注意运行的开始是before()，结束是after()。此外，beforeEach()在每个单独测试之前运行，afterEach()在每个测试之后运行。

```
describe('Suite', function() {
  before(function() {
    console.log('before()');
  });

  beforeEach(function() {
    console.log('beforeEach()');
  });
```

```
afterEach(function() {
  console.log('afterEach()');
});
```

```
after(function() {
  console.log('after()');
});
```

```
it('测试 1', function() {
  console.log('Test 1');
});
```

```
it('测试 2', function() {
  console.log('Test 2');
});
```

## 清单 23-6. 一个带有钩子的测试套件

```
测试套件
before()
beforeEach()
测试 1
  ✓ 测试 1
afterEach()
beforeEach()
测试 2
  ✓ 测试 2
afterEach()
after()
```

## 清单 23-7. 来自清单 23-6 的部分输出

# 断言

到目前为止，我们创建的简单测试都显式地抛出了错误。这是一种编写测试的有效方式，但并非最优雅的。更优的方法涉及使用断言。**断言** 是一段逻辑，用于测试测试的某些预期条件是否得到满足。例如，一个断言可能声明某个变量持有特定值，或者某个函数根据其输入预期会抛出异常。

对于非常基础的测试，你可能有兴趣使用 Node 核心的 [assert 模块](https://nodejs.org/api/assert.html)。为了本书的目的，我们将使用更强大的 [Chai 断言库](https://www.chaijs.com/)。与 Mocha 类似，Chai 既可以在 Node 中使用，也可以在浏览器中使用。Chai 还在其主页上声称它可以“与任何 JavaScript 测试框架愉快地配对”。可以使用清单 23-8 所示的命令安装它。

```
npm install chai
```

## 清单 23-8. 安装 chai 的命令

Chai 还支持多种断言接口：[should](https://www.chaijs.com/guide/styles/#should)、[expect](https://www.chaijs.com/guide/styles/#expect) 和 [assert](https://www.chaijs.com/guide/styles/#assert)。本书将使用 expect 风格，它专为 BDD 风格的测试而设计。expect 风格允许你以非常接近自然语言的方式编写测试。

例如，清单 23-9 中的 Mocha 测试使用 Chai 的 expect 风格断言变量 `foo` 等于 4。

```
var expect = require('chai').expect;

it('加法测试', function() {
  var foo = 2 + 2;

  expect(foo).to.equal(4);
});
```

**清单 23-9.** 一个使用 Chai expect 风格断言的简单测试

注意清单 23-9 中的断言读起来多么简单。清单 23-10 包含了其他一些常见的 expect 风格断言示例。

```
var expect = require('chai').expect;

it('expect 风格断言', function() {
  expect(2).to.be.greaterThan(1);
  expect(null).to.not.exist;
  expect(false).to.be.false;
  expect('foo').to.be.a('string');
  expect(function(){
    throw new Error('foo');
  }).to.throw;
  expect([1, 2, 3]).to.have.length(3);
  expect({foo: 'bar'}).to.have.property('foo').and.equal('bar');
});
```

**清单 23-10.** 常见的 expect 风格断言

# 测试 Angular

许多开发者选择 Angular 而非其他客户端方案的原因之一是*可测试性*。Angular 是为测试而构建的。这从 Angular 核心中普遍使用的依赖注入模式可见一斑。回想一下，大多数 Angular 构造的第二个参数都是依赖列表。这允许依赖对象在构造函数外部创建并作为参数传入，这可以极大地提高代码的可测试性，因为测试可以完全专注于开发者的代码，而不是框架代码。让我们首先编写一个基本的 Angular 控制器，然后我们将设置项目来测试它。

清单 23-11 是我们要测试的控制器。在 `/public/javascript` 下创建 `main.js` 文件。`EmployeeService` 是 Angular 章节中前面示例的 `$resource`。

```
var app = angular.module('app', ['ngResource']);
app.factory('EmployeeService', ['$resource', function($resource) {
    return $resource('/employees/:employeeId', {}, {
        get: {
            isArray: true
        },
        post: {
            method: 'POST',
            isArray: false
        }
    });
}]);

app.controller('main', ['$scope', 'EmployeeService', function($scope, EmployeeService) {
    $scope.employees = [];
    $scope.firstName = $scope.lastName = '';

    EmployeeService.get(function (data) {
        $scope.employees = data;
    });

    $scope.addDisabled = function () {
        return !($scope.firstName.trim().length && $scope.lastName.trim().length);
    }

    $scope.add = function () {
        EmployeeService.post({
            first: $scope.firstName,
            last: $scope.lastName
        }, function (data) {
            $scope.employees.push(data);
            $scope.firstName = $scope.lastName = '';
        });
    };
}]);
```

**清单 23-11** 我们的测试控制器

看看这个控制器，以下是我们想要测试的：

- `employees` 正确地设置为 `EmployeeService.get` 的结果
- `addDisabled` 在有效的名和姓都有值之前应该返回 `true`
- `add` 将调用 `EmployeeService.post`，新创建的员工将被添加到 `employees` 中
- 添加新员工后，`addDisabled` 应该返回 `true`

在一个完整的例子中，我们希望在测试清单 23-1 中的主控制器之前隔离测试 `EmployeeService`；然而，`EmployeeService` 并不代表测试 Angular 应用程序所需的大部分测试代码。大部分开发者逻辑都在控制器中，所以这就是我们本章将重点测试的内容。

# 设置

首先，我们将使用 `npm install karma –save` 在当前项目中安装 Karma 测试运行器。其次，我们将通过 `npm install -g karma-cli` 全局安装 Karma CLI 模块。Karma 是一个测试运行器，而不是一个测试库，Angular 开发团队在开发过程中使用它。它是一个用于启动 HTTP 服务器、提供静态文件、监视文件更改、创建 HTML 测试报告以及将适当的测试框架加载到浏览器中的工具。

一旦 Karma 模块安装完毕，在你的项目中运行 `karma init`。这将引导你在当前目录中创建一个 `karma.conf.js` 文件。对于提示，接受默认值即可。你需要进行两处小改动才能使一切正常工作。生成器完成后，打开 `karma.conf.js` 并进行以下更改：

```
frameworks: ['mocha', 'chai'],
files: [
  'http://ajax.googleapis.com/ajax/libs/angularjs/1.2.16/angular.js',
  'http://cdnjs.cloudflare.com/ajax/libs/angular.js/1.2.16/angular-mocks.js',
  'http://code.angularjs.org/1.2.16/angular-resource.js',
  'public/javascript/*.js',
  'public/javascript/test/*.js'
],
```

**清单 23-12** Karma 配置更改

`files` 设置配置 Karma 将所有列出的文件加载到浏览器中。它还设置逻辑来监视本地文件夹的更改，并在文件更改时重新运行测试套件。在清单 23-2 中，我们指示 Karma 首先加载几个 Angular 库，然后最后加载我们的 JavaScript。除了 `angular-mocks`，所有列出的文件都应该很熟悉。`angular-mocks` 使我们能够访问 `$httpBackend`，它让我们可以在不涉及 Web 服务器的情况下模拟 HTTP 请求。我们很快将更详细地介绍 `$httpBackend`。`angular-mocks` 还覆盖了一些核心 Angular 函数以辅助测试。

`frameworks` 指示 Karma 将 mocha 和 chai 加载到浏览器中。我们的测试将使用 mocha 作为测试库，chai 作为断言框架。

接下来，在 `public/javascript/test` 中创建一个名为 `main_test.js` 的文件。这将是我们编写 Mocha 测试的地方。你在测试 Express 服务器时学到的所有关于 Mocha 的知识同样适用于测试客户端代码。现在我们需要再安装几个模块，以便我们可以同时在 Karma 中使用 Chai 和 Mocha。在终端窗口中运行以下命令：`npm install mocha karma-mocha karma-chai --save-dev`。

你应该已经熟悉 mocha 了。另外两个包只是适配器，让 Karma 可以通过 Karma 框架与 chai 和 mocha 通信。虽然你不会直接与它们交互，但你需要安装它们才能使测试正常工作。

# 测试代码设置

最后，让我们用一些基本测试来充实 `main_test.js`。首先，我们将展示并讨论清单 23-13 中的测试代码设置，然后我们将介绍清单 23-14 中的实际测试。

main_test.js

```
describe('主控制器', function() {
  beforeEach(module('app'));
  var _scope;
  var _httpBackend;

  beforeEach(inject(function($controller, $rootScope, EmployeeService, $httpBackend) {
    _scope = $rootScope.$new();
    _httpBackend = $httpBackend;

    $httpBackend.when('GET', '/employees').respond([{
      first: 'Abraham',
      last: 'Lincoln'
    }, {
      first: 'Andrew',
      last: 'Johnson'
    }]);

    $httpBackend.when('POST', '/employees').respond({
      first: 'Grover',
      last: 'Cleveland',
    });

    $controller('main', {
      $scope: _scope,
      EmployeeService: EmployeeService
    });
  }));
  // 测试放在这里
  // {…}
});
```

## 清单 23-13 测试代码设置

记住，我们正在使用 Mocha 测试我们的客户端代码。函数和



用于测试服务端代码的约定在此处同样适用。在第一个 `beforeEach` 函数中，我们调用 `module` 并传入 `app`。这会指示 Mocha 在本规范中的每个测试之前加载 app 模块及其依赖项。`module`（如清单 23-12 所示）是被 `angular-mocks` 覆盖的 Angular 功能之一。`app` 上挂载了 `main` 控制器，这正是我们要测试的控制器。

第二个 `beforeEach` 是测试设置的核心所在。从宏观角度看，这个 `beforeEach` 在每个测试之前创建一个新的 `main` 控制器——即清单 23-11 中定义的那个。我们希望每个测试都使用一个新的控制器，因为这样可以避免某个测试中对控制器的修改对后续测试产生不可预测的连锁影响。为每个测试创建新控制器可以确保每个测试都从已知的初始状态开始。

在测试过程中，开发者需要扮演 Angular 的角色，手动创建一个管理所有依赖的控制器对象。`inject` 初看起来可能有些奇怪，但它只不过是 `angular-mocks` 提供的众多 mock 函数之一。它会创建一个 `$injector` 的新实例，用于解析依赖引用。这与 Angular 内部用于所有依赖注入逻辑的函数完全相同。在我们的测试中，我们希望直接调用它来控制 `main` 将使用的一些依赖。

要创建一个功能完整的 `main` 控制器，我们需要 `$controller`、`$rootScope`、`EmployeeService` 和 `$httpBackend`。`$controller` 是 Angular 内部用于创建控制器的函数，我们将用它来手动创建控制器对象。记住，`$rootScope` 是全局的 Angular 作用域对象，拥有创建子作用域的函数。`EmployeeService` 是使用 `$resource` 构建的数据访问服务，用于与 RESTful Web 服务器通信。最后，`$httpBackend` 是另一个 Angular mock 依赖，我们将用它来拦截和模拟 HTTP 请求。

首先，我们使用 `$rootScope.$new()` 创建一个新的子作用域对象并将其存储在 `_scope` 中。如果你留意 `_scope` 的作用域，会发现它在 `describe` 块内嵌套的每个函数中都可用。这是有意为之的，否则我们将无法观察 `main` 控制器内部 `$scope` 对象的变化。由于对象是按引用传递的，控制器中对 `$scope` 的任何更改都会反映在 `_scope` 中。我们使用 `_scope` 来观察控制器内部对 `$scope` 值所做的更改。

接下来，我们要模拟通过 `EmployeeService` 发出的 HTTP 请求。`$httpBackend.when` 的第一个参数是 HTTP 动词，第二个是 URI。返回的对象有一个 `respond` 方法，该方法接受一个响应对象。当通过 `$http` 模块调用相关路由时，该响应对象将成为模拟响应的有效载荷。我们通过 `$httpBackend` 设置的两个路由与 `EmployeeService` 内部可用的两个路由相同。因此在 `main` 中运行 `EmployeeService.get` 时，底层的 `$http` 模块通常会向 Web 服务器上正确的路由发送 GET 请求。通过使用 `$httpBackend`，我们拦截了这个请求，返回一个模拟响应，从而将 Web 服务器从测试循环中移除。与 `_scope` 变量类似，我们创建了一个 `_httpBackend` 变量，可以从 `describe` 内的任何函数中访问。

最后，我们使用 `$controller` 实例化一个新的 `main` 控制器。第一个参数是控制器名称，第二个是一个哈希对象，其中键是依赖名称，值是依赖对象。我们将 `_scope` 作为子作用域传入，并原样传递 `EmployeeService`。

## 控制器测试

现在所有设置代码已准备就绪，我们终于可以编写控制器测试了。

```
main_test.js

//Test one
it('should not allow add initially', function () {
    expect(_scope.addDisabled()).to.equal(true);
});
//Test two
it('should allow add when firstName and lastName have been set', function() {
    _scope.firstName = 'Grover';
    _scope.lastName = 'Cleveland';
    expect(_scope.addDisabled()).to.equal(false);
});
//Test three
it('should have a list of employees after the "get" call is complete', function () {
    _httpBackend.flush();
    expect(_scope.employees.length).to.equal(2);
});
//Test four
it('should return the new item after adding and disable the add button', function () {
    _httpBackend.flush();

    _scope.firstName = 'Grover';
    _scope.lastName = 'Cleveland';
    _scope.add();
    _httpBackend.flush();
    expect(_scope.employees.length).to.equal(3);

    var result = _scope.employees[2];
    expect(result.first).to.equal('Grover');
    expect(result.last).to.equal('Cleveland');

    expect(_scope.addDisabled()).to.equal(true);
});
```

清单 23-14 main 控制器测试

测试一检查确保 `addDisabled` 最初为 true，因为名和姓都为空。在测试二中，我们设置 `_scope.firstName` 和 `_scope.lastName` 为字符串。现在当我们调用 `addDisabled` 时，期望其值为 false。`addDisabled` 内部的业务规则应该返回 false，因为名和姓都有值了。通过这些测试代码的演示，应该清楚我们为什么创建 `_scope` 变量以及如何使用它。

测试三和测试四展示了如何使用 `_httpBackend`。在测试三中，第一步是调用 `_httpBackend.flush`。`flush` 允许单元测试控制 `_httpBackend` 何时发送（刷新）响应。每次调用 `flush` 都会发送当前存储在 `_httpBackend` 内部状态对象中的所有待处理响应。通过使用 `flush`，我们可以在保持代码异步的同时避免编写异步测试。

当 `main` 初始加载时，它的首要操作之一就是通过 `EmployeeService.get` 请求员工列表。`$httpBackend` 拦截了该请求并将其保存在内部的待处理模拟请求列表中。`flush` 清空这个内部请求列表并发送模拟响应。在测试三中，我们 `flush` 存储的请求后，`main` 中的回调将执行并将 `$scope.employees` 设置为模拟 GET 请求的结果。此后，`_scope.employees` 的长度应为 2。

在测试四中，我们 `flush` GET 请求以确保员工列表已填充。然后我们设置 `_scope` 的名和姓并调用 `add`。这会调用 `EmployeeService.post` 并传入姓名值。与 GET 请求类似，POST 请求被 `$httpBackend` 拦截，因此回调函数尚未触发，员工列表应该保持不变。我们第二次调用 `_httpBackend.flush` 来返回模拟的 POST 请求。这将触发回调函数执行，并将新创建的员工添加到 `_scope` 上挂载的员工列表中。测试四中的最后几个 `expect` 调用验证了这一切是否按预期发生。

## 运行测试

现在一切准备就绪，让我们运行这些测试，看看 `main` 控制器在自动化测试中的表现如何。在打开的终端中运行 `karma start`。应该会打开一个 Web 浏览器并显示连接消息，而在运行 `start` 命令的终端中会打印出测试结果。如果你一直紧跟着操作，四个测试应该全部通过。此时，如果你对控制器或测试 JavaScript 文件进行任何更改，测试应该会自动重新运行。这让你可以随时重构和清理代码并获得持续反馈。

目前，浏览器并没有显示有用的内容。它只是作为测试以及运行测试所需的所有客户端库的占位符。我们的配置仅使用将信息直接记录到控制台的默认 reporter。如果你希望在浏览器中查看格式化的 HTML 或其他报告选项，请查看 [npm 上的 reporter 列表](https://www.npmjs.com/search?q=karma-reporter)。

## 后续步骤

我们这里只测试了一个控制器。如果我们想彻底测试我们的应用——我们也应该这么做——还需要为自定义指令和服务编写测试。我们还可以扩展测试工作以包含代码覆盖率度量。此外，我们可以重构测试使其更加模块化。这只是一个简短的介绍，涵盖了为 Angular 应用继续编写测试所需的工具和设置。



 # 摘要

本章讨论了几种测试 JavaScript 应用程序各个部分的方法。我们首先介绍了用于 Node.js 测试的 Mocha 框架。接着，我们转向使用 Karma 进行 Angular 测试。很便利的是，Karma 让我们能够复用许多关于 Mocha 的知识。

这结束了本章，事实上也结束了本书。我们衷心感谢您的阅读，希望您能学到一两点知识。我们写这本书当然也学到了很多。
