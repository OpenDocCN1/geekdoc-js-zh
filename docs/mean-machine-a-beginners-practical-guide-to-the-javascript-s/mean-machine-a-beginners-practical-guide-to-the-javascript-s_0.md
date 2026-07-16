# MEAN Machine：JavaScript 栈初学者实践指南



![](img/title_page.jpg)

![MEAN Machine](img/title_page.jpg)







# 前言

### 本书使用的约定

![Note](img/icon-pencil.png "注意")

注意

> 此图标表示一个提示。

![Warning](img/icon-match.png "警告")

警告

> 此图标表示一个警告。

![Tip](img/icon-heart.png "专业提示")

提示

> 此图标表示一个专业提示。

### 代码示例

书中的代码被封装在如下所示的代码块中：

### 代码许可

本书中的示例代码根据 [MIT](http://opensource.org/licenses/MIT) 许可证发布。

### 代码仓库

可以在 [`github.com/scotch-io/mean-code`](http://github.com/scotch-io/mean-code) 找到示例代码。

### 联系我们

如果您对本书有任何问题、意见、赞誉，或者发现书中的错误，请随时通过 `chris@scotch.io` 和 `holly@scotch.io` 与我们联系。

### 介绍

Node 是一种令人兴奋的 Web 开发 JavaScript 语言，近年来变得越来越流行。它最初用于小型开发项目，此后渗透到企业级，可以在微软、eBay、LinkedIn、Yahoo、沃尔、Uber、Oracle 等许多大型公司看到。

### 为什么选择 MEAN？

MEAN Stack 使用四种软件：`MongoDB`、`ExpressJS`、`AngularJS` 和 `NodeJS`。将这四种工具结合使用，允许开发者快速创建高效、组织良好且交互式的应用程序。

由于栈中的每个组件都使用 JavaScript，你可以无缝地穿过 Web 开发代码。全栈 JavaScript 让我们能够完成很棒的事情：

- 在服务端使用 JavaScript (`Node` 和 `Express`) 
- 在客户端使用 JavaScript (`Angular`) 
- 在 `MongoDB` 中存储 JSON 对象
- 使用 JSON 对象轻松地从数据库到服务器到客户端传输数据

> 整个技术栈使用同一种语言可以提高生产力。即使是工作在 Angular 中的客户端开发者，也能轻松理解服务端的大部分代码。

从数据库开始，我们以类似 JSON 的格式存储信息。然后我们可以在 Node 服务器上编写 JSON 查询，并使用 Angular 将其直接发送到前端。当有多个开发者协作一个项目时，这特别有用。服务端代码对前端开发者来说更具可读性，反之亦然。这让一切变得更加透明，并证明能极大缩短开发时间。一旦我们开始深入研究示例，开发的便利性将变得更加明显，并希望在未来能为你和你的团队减少一些烦恼。

### 何时使用 MEAN Stack

MEAN Stack 极大受益于 Node 的优势。Node 让我们能够构建实时开放 API，并与我们的前端 Angular 代码进行消费和使用。对于聊天系统、状态更新或几乎任何其他需要快速显示实时数据的场景，其数据传输非常有用。

- 聊天客户端
- 实时用户更新（如 Twitter 馈）
- RSS 馈
- 在线商店
- 投票应用

### 何时**不**使用 MEAN Stack





与任何语言或语言集一样，有很多场景下 `MEAN` 并不是最佳选择，在深入编码之前识别这一点至关重要。`MEAN` 栈的许多优势以及你使用它的原因根源于它对 `Node` 的使用。在某些你可能不想使用它的原因上，我们也再次看到了这种趋势。

`Node` 通常不是处理 CPU 密集型任务的最优选型。尽管有一些[观点](http://neilk.net/blog/2013/04/30/why-you-should-use-nodejs-for-CPU-bound-tasks/) 认为 `Node` 在计算密集型应用中实际上表现良好，但对于初学者来说，如果你知道你的应用程序需要大量的计算，最好是避开 `Node`（换句话说，我们不要在这里尝试去计算第 1000 个质数）。

## 谁在用 MEAN？

许多开发者对 `MEAN` 栈赞誉有加。该技术栈在每项操作中都使用 JavaScript，这对于希望在项目中顺畅流转思路的开发者来说非常有吸引力。一些大型公司已经从中受益，并将 `Node` 集成到他们的许多业务中。

![Walmart](img/walmart.jpg "Walmart")

沃尔玛

> **Walmart**: 沃尔玛从 2012 年开始使用 `Node.js` 为移动用户提供现代的前端体验。通过利用 JavaScript 平台，他们能够快速地将现有的 API 集成到他们的 `Node` 应用中。他们还提到，黑色星期五 53% 的在线流量流向他们的 `Node` 服务器，且实现了零停机。

![Yahoo](img/yahoo.jpg "Yahoo")

雅虎

> **Yahoo!**: 雅虎从 2010 年就开始尝试使用 `Node`。起初他们只是用它处理文件上传等小任务，而现在他们使用 `Node` 每分钟处理近 200 万次请求。他们注意到速度的提升和开发流程的简化。

![Linkedin](img/linkedin.jpg "Linkedin")

LinkedIn

> **LinkedIn**: LinkedIn 开始完全使用 `Node` 开发其移动端应用程序的服务器端。他们之前使用的是 `Ruby`，但自从切换以来，他们看到了性能的巨大提升，速度快了 2 到 10 倍。

![Paypal](img/paypal.png "Paypal")

PayPal

> **PayPal**: PayPal 最近也加入了进来，并开始将部分 `Java` 代码迁移到 `Node`。他们最初只对账户概览页面进行实验，但一旦看到速度提升了 35%，且开发时间减少了一半，他们就开始将所有网站迁移到 `Node.js`。

如需更大且持续维护的列表，请访问 [Node Industry](http://nodejs.org/industry/) 页面。

## 入门指南

让我们快速查看一下我们将使用的技术。记住，本书旨在教你所有这些组件是如何协同工作的，因此我们不会深入探讨每个领域最先进的技术和概念（尽管我们会讲得很深入）。我们将为每个章节中的每个主题提供更多资源链接，以丰富你的知识。

### MongoDB

`MongoDB` 命名自“hu**mongo**us”（巨大的）一词，是一种以 JSON 格式存储文档的开源 NoSQL 数据库。根据 Google 搜索、职位发布和招聘网站（Indeed.com）的趋势，它是[领先的 NoSQL 数据库](http://www.mongodb.com/leading-nosql-database)。

### Mongo vs. MYSQL

使用 `MYSQL` 的 LAMP 栈多年来一直是领先的技术栈。`MYSQL` 被归类为**关系型数据库**。

> **关系型数据库** 数据存储在表中，表中不仅包含数据，还包含数据与数据库中其他信息之间的关系。 —

### 文档数据库

另一方面，`MongoDB` 被归类为非关系型数据库，更具体地说是**文档型数据库**。这意味着你可以按照自己的意愿定义数据结构。你可以获得数据建模选项，以匹配你的应用程序及其性能需求。你可以轻松地使用 JSON、`XML`、`BSON` 或许多其他更适合你应用程序的格式将复杂对象插入到数据库中。如果出现用例需要，你甚至可以在某些文档数据库中存储 PDF 文档。

> **文档型数据库** 一种 NoSQL 数据库，它以半结构化文档的形式存储和检索数据（与关系型数据库中的表相反）。 —

`MongoDB` 中的数据建模极其灵活。存储数据的一种方法是创建单独的文档并创建引用来连接信息。你可以看到下面，我们的“精灵信息文档”（Elf Info Document）包含了基本信息，我们可以通过“精灵地址文档”（Elf Address Document）来引用它。

**精灵信息** `json { id: "1234", name: "holly", age: "400", type: "high-elf" }`

**精灵地址簿** `json { elven_id: "1234", city: "rivendell", state: "middle-earth" }`

另一种方法是将精灵地址直接嵌入到精灵信息文档中，这样每个精灵就只有一个文档，这允许在更新精灵信息时进行更少的写操作，并获得更高的性能（假设你的文档不会增长得太大）。

```
 1 {
 2   id: "1234",
 3   name: "holly",
 4   age: "400",
 5   type: "high-elf",
 6   address: {
 7     city: "rivendell",
 8     state: "middle-earth",
 9   }
10 }
```

一旦你开始存储关于多个精灵的信息，它们的文档就可以归类为一个精灵信息集合（Elf Info Collection）。集合就是一组相关的文档。在这种情况下，它们将具有相同的字段。

### CAP 定理

有一个被称为 `CAP` 的概念，也称为布鲁定理，它指出网络系统只能同时提供以下功能的两种：

- 一致性（Consistency）：应用程序中的所有节点都可用并同时显示相同的数据
- 可用性（Availability）：所有节点都可读可写
- 分区容错（Partition Tolerance）：即使系统部分故障，你的应用程序也能继续运行

关于如何解释这一观点存在一些困惑，因此布鲁后来指出这实际上归结为**一致性**与**可用性**之间的权衡。仅仅看定义就能明显看出这些概念是互斥的。假设我们允许所有节点随时对读写都是**可用**的。银行应用程序是一个需要这种重要性的真实世界例子。为了方便起见，让我们假设透支费等这些趣事并不存在。银行需要随时知道你的准确账户余额。如果你账户里有 100 元，你取了 100 元，那么你自然剩下了 0 元。由于所有节点都可读可写，在账户余额仍显示为 100 元的极短时间范围内，另一笔扣款可能会通过。因此，一旦账户余额更新，你的账户实际上会变成负数，因为第二笔扣款被允许通过了，尽管它本应被拒绝。这就是为什么在银行应用程序的案例中，**一致性**更为重要。

一致性的代价是放弃一些可用性。在上述的例子中，一旦你取了钱，就应该加上某些锁定，防止账户余额被读取为 100 元。如果你的应用程序无法每秒读取每个节点，那么它对某些用户来说可能是宕机或不可用的。某些应用程序相比一致性更看重可用性和性能，这就是许多文档型数据库大放异彩的地方。




MongoDB 默认情况下优先考虑一致性而非可用性，但仍然允许你调整某些设置以在两个方向上获得更多支持。读写锁作用于每个数据库，因此数据库中的每个节点将始终能看到最新的数据。由于 MongoDB 支持 `sharding`（分片），一旦你的数据库开始增长，你的数据可能会分区到跨多个服务器的多个数据库（或 `shards`）。每个分片将是一个独立的数据库，共同形成一个数据库集合。这使得查询速度更快，因为你只需要访问包含该信息的分片，而不是整个数据库。然而，它在写入后的一段时间时间内可能会导致分片与分片之间出现不一致性。这被称为最终一致性，是一致性和可用性之间的一种常见折中。

## 主要特性

*   敏捷且可扩展
*   [面向文档的存储](http://docs.mongodb.org/manual/core/data-modeling/) - 具有动态模式的 JSON 风格文档提供了简单性和强大性。
*   [全索引支持](http://docs.mongodb.org/manual/indexes/) - 像你习惯的那样，对任何属性建立索引。
*   [复制与高可用性](http://docs.mongodb.org/manual/replication/) - 跨局域网和广域网镜像，以实现扩展并让人安心。
*   [自动分片](http://docs.mongodb.org/manual/sharding/) - 在不牺牲功能的情况下进行水平扩展。
*   [查询](http://docs.mongodb.org/manual/applications/read/) - 丰富的基于文档的查询。
*   [快速就地更新](http://docs.mongodb.org/manual/applications/update/) - 用于无竞争性能的原子修改器。
*   [Map/Reduce](http://docs.mongodb.org/manual/applications/map-reduce/) - 灵活的聚合和数据处理。
*   [GridFS](http://docs.mongodb.org/manual/applications/gridfs/) - 存储任何大小的文件而不会使你的栈复杂。

## Node.js

Node 构建在 Google Chrome 的 V8 JavaScript 运行时，作为你 MEAN 应用中的服务器端平台。这意味着什么？在 LAMP 栈中，你有一个 Web 服务器（`Apache`、`Nginx` 等）运行着服务器端脚本语言（`PHP`、`Perl`、`Python`）来创建动态网站。服务器端代码通过从数据库（`MYSQL`）中提取数据来创建应用环境，然后由 Web 服务器解释以生成网页。

当请求新连接时，`Apache` 会创建一个新线程或进程来处理该请求，这使其成为 `multithreaded`（多线程的）。你通常会有若干空闲子进程等待被分配给新请求。如果你配置服务器仅有 50 个空闲进程，而有 100 个请求进来，某些用户可能会遇到连接超时，直到其中一些进程被释放。当然，有几种方法可以更高效地处理这种扩展性，但通常 `Apache` 会为每个请求使用一个线程，因此为了支持更多的用户，你最终需要越来越多的服务器。

> **多线程** 一种编程模型，程序流具有多个控制线程。程序的不同部分（线程）能够同步且独立地执行，而无需等待每个事件完成。这对于现在不必等待的用户来说是很棒的。



目前存在多个 Node 框架。我们在本书中使用 `Express`，但这里所教授的概念可以很容易地迁移到其他流行的框架上。

其他值得关注的主要框架有：

*   [HapiJS](http://hapijs.com/) - 一个正在被越来越多的企业公司使用的极佳框架。
*   [KoaJS](http://koajs.com/) - `Express` 的一个分支版本。
*   [Restify](http://mcavage.me/node-restify/) - 借用了 `Express` 的语法，创建一个专门用于构建 REST API 的框架。
*   [Sails](http://sailsjs.org/#/) - 构建用于模拟 MVC 模型的框架。

`Express` 将处理你几乎所有需要的任务，它非常健壮、易用，而且现在有了商业后盾，因为它最近被 [StrongLoop](http://strongloop.com/strongblog/tj-holowaychuk-sponsorship-of-express/) 收购/赞助了。

虽然其他框架也各有优之处（一定要看看它们），但我们将专注于 `Express`。毕竟，它是 `MEAN` 栈的一部分。

### ExpressJS

`Express` 是一个使用 `NodeJS` 构建 Web 应用的轻量级平台。它帮助组织服务器端的 Web 应用。[ExpressJS Website](http://expressjs.com) 将 `Express` 描述为“一个最小且灵活的 node.js Web 框架”。

`Express` 隐藏了 `Node` 的许多内部机制，让你能够深入应用程序代码并更快地让程序运行起来。它相当容易学习，并在结构上仍然赋予你一定的灵活性。它目前成为 `Node` 最流行的框架是有原因的。使用 `Express` 的一些知名包括：

*   MySpace
*   LinkedIn
*   Klout
*   Segment.io

访问 [Express 列表](http://expressjs.com/applications.html) 查看完整的 `Express` 用户列表。

`Express` 带有许多非常强大的功能，将为你的 `Node` 开发带来便利。

*   路由 (Router)
*   处理请求 (Handling Requests)
*   应用设置 (Application Settings)
*   中间件 (Middleware)

如果这些术语对你来说很新，不要担心。在我们构建示例应用程序时，我们将深入这些每一个组件，学习并使用它们。现在进入 MEAN 栈的最后一部分（可能是我最喜欢的部分）！

### AngularJS

`Angular` 由 Google 创建，是一个为了快速动态的前端部署而构建的 JavaScript 框架框架

`Angular` 允许你构建标准的 HTML 应用，然后扩展你的标记来创建动态组件。如果你曾经在没有使用 `Angular` 的情况下制作过动态网页，你可能注意到一些常见的复杂性，例如数据绑定、表单验证、DOM 事件处理等。`Angular` 为这些问题引入了一个一站式的解决方案。

对于那些担心一次学习这么多内容的人来说，你们很幸运了。`Angular` 的学习曲线实际上非常小，这可能解释了为什么它的采用率会飙升。它的语法简单，其主要原理（如数据绑定和依赖注入）通过几个例子就能轻松掌握，这些内容当然会在书中涵盖。

`Angular` 的两个主要功能是数据绑定和依赖注入。数据绑定处理我们如何处理应用程序中的数据，而依赖注入更多地处理我们如何构建它们。

#### 数据绑定

如果你来自 jQuery 的世界，你将熟悉使用 CSS 选择器来遍历 DOM。每当你需要从输入框获取值时，你都会使用 `$('input').val();`。这很棒，但当你有带有多个输入框的大型应用时，管理起来就会变得有些困难。

当你从应用程序的不同位置拉取并注入数据时，就不再有“单一数据源”了。在 `Angular` 中，你拥有一个类似于 MVC（模型-视图-控制器）模型结构，你的数据存储在一个地方。当你需要信息时，可以确定你正在查看正确的信息。这是因为如果你在视图（HTML 文件）或控制器（JavaScript 文件）中更改了数据，**数据会在处处发生变化**。

#### 依赖注入

一个 `Angular` 应用程序是几个不同模块的集合，所有模块共同构建了你的应用程序。例如，你的应用程序可能有一个与 API 中的特定项交互的模型，一个将数据传递给视图的控制器，或者一个处理我们 `Angular` 应用程序路由的模块。

* * *

> **依赖注入** 当代码中的一个对象依赖另一个对象时，就会发生依赖。依赖有不同的程度，但过多的依赖有时会让你的代码难以测试，甚至让某些过程运行时间更长。依赖注入是我们能够为对象提供其运行所需的依赖的方法。 —

将应用程序分化和模块化带给我们许多益处。就像 `Node` 中的包、PHP 中的包或 Ruby 中的 gems 一样，我们可以在不同项目之间复用模块，甚至引入其他开发者已经创建的模块。

通过将这些模块注入到应用程序中，我们还可以单独测试每个模块。我们能够确定应用程序的哪些部分故障，并将问题缩小到特定的代码集。

#### 其他主要功能

*   MVC
*   指令 (Directives)
*   作用域 (Scopes)
*   模板 (Templates)
*   测试 (Testing)

查看此 Tuts+ 文章以获得 `Angular` 更深入的概述：[5 个强大的 AngularJS 功能](http://code.tutsplus.com/tutorials/5-awesome-angularjs-features--net-25651)。

## MEAN 思维

在我们本书构建 MEAN 栈应用程序期间，我们想要使用特定的思维方式。



## 2. **第 4-9 章：服务器/后端** 概念、应用与最佳实践。
## 3. **第 10-16 章：客户端/前端** 概念、应用与最佳实践。
## 4. **第 17-19 章：MEAN Stack 应用** 将一切整合在一起，以便我们构建出色的应用程序。
## 5. **第 20 章至无限：更多示例应用程序！**

## 入门与安装

### 要求
* [Node](http://nodejs.org)
* `npm` - 包含在 Node 安装中

### 工具
* Sublime Text
* Terminal - 我们喜欢使用 [iterm2](http://iterm2.com/) (mac/linux 用户)
* [Git Bash + ConEmu](http://scotch.io/bar-talk/get-a-functional-and-sleek-console-in-windows) (windows 用户)
* [Postman](https://chrome.google.com/webstore/detail/postman-rest-client/fdmmgilgnpjigdojojpjoooidkmcom?hl=en) (Chrome)
* [RESTClient](https://addons.mozilla.org/en-US/firefox/addon/restclient/) (Firefox)

### 安装
请访问 [node 官网](http://nodejs.org) 并下载 Node。运行安装程序，你就会安装好 Node 和 `npm`！这可能是全书中最简单的一部分。

![Node Installation](img/04-getting-started----node-install.jpg "Node Installation")

Node 安装

让我们双重检查一切运行正常，进入控制台并输入以下：`node -v` 和 `npm -v`。

```
1 node -v
```

![Node Version](img/04-getting-started----node-version.jpg "Node Version Check")
Node Version

```
1 npm -v
```

![NPM Version](img/04-getting-started----npm-version.jpg "NPM Version Check")
NPM Version

如果你在执行其中任一个命令时遇到了可怕的“command not found”（未找到命令），请确保 node 已添加到你的 `PATH` 中。这会为命令行提供 `node` 和 `npm` 命令。只需搜索 `npm` 的安装位置，打开环境变量窗口，并添加 `npm` 的路径。重启电脑，让魔法开始。

有关更详细的故障排除说明，请参见以下：
**Windows**: [将 Node 添加到你的 Windows PATH](http://stackoverflow.com/a/8768567/2976743)
**Mac**: [将 Node 添加到你的 Mac PATH](http://architectryan.com/2012/10/02/add-to-the-path-on-mac-os-x-mountain-lion/#.U_wCiFNdWqc)

如果你仍然遇到问题，请随时联系我们并提出你的问题。现在安装已经完成，让我们继续前进并开始构建东西吧！我们将从 MEAN Stack 应用的基础——Node 开始！

## 启动 Node
让我们看看如何开始构建我们的 Node 应用程序。我们将介绍**基础 Node 配置**、**安装 npm 包**以及**创建一个简单的应用**。

### 配置 (package.json)
Node 应用程序在名为 `package.json` 的文件中进行配置。你为你创建的每个项目都需要一个 `package.json` 文件。
该文件是你配置项目名称、版本、存储库、作者以及所有重要的依赖项的地方。

这是一个示例 `package.json` 文件：

```
 1 {
 2   "name": "mean-machine-code",
 3   "version": "1.0.0",
 4   "description": "The code repository for the book, MEAN Machine.",
 5   "main": "server.js",
 6   "repository": {
 7     "type": "git",
 8     "url": "https://github.com/scotch-io/mean-machine"
 9   },
 10   "dependencies": {
 11     "express": "latest",
 12     "mongoose": "latest"
 13   },
 14   "author": "Chris Seville & Holly Lloyd",
 15   "license": "MIT",
 16   "homepage": "https://github.com/scotch-io/mean-machine"
 17 }
```

这看起来很复杂，但如果你逐行查看，你会发现这里有很多属性让其他开发者更容易进入项目。我们将在书中书中稍后介绍这些不同的部分。

这些是最基础的属性。

```
1 {
2   "name": "mean-machine-code",
3   "main": "server.js"
4 }
```

`main` 告诉 Node 当我们想要启动应用程序时使用哪个文件。我们将该文件命名为 `server.js` 以供我们的应用程序使用，这将是我们应用程序的地方。

有关更多在 `package.json` 中指定的属性，请参见 [package.json 文档](https://www.npmjs.org/doc/files/package.json.html)。

### 初始化应用
`package.json` 文件是关于我们启动每一个应用程序的。



随时进入你的 `server.js` 文件并进行修改。然后观察应用程序自动重启时发生的奇迹吧！

![nodemon 启动.](img/05-node-start----nodemon-server.jpg "nodemon server.js")

`nodemon server.js`

在本书的其余部分，当我们想要启动服务器时，我们会引用 `nodemon`。它只是开发时的一个更简单的选择。

***

我们现在已经配置了一个非常简单的 Node 应用并从命令行启动了它。我们离构建可以向世界展示的完整 Node 应用又近了一步。

## 包 (Packages)

包扩展了我们应用程序的功能。正如我们在早前的“入门教程”（Primers）部分中讨论过的，即使是 MEAN 栈的四个主要部分之一的 Express，也是一个 Node 包。

让我们看看如何添加和安装包。一旦我们讨论了如何将包引入我们的应用程序，我们将迁移到使用 MEAN 栈的其他组件。

#### 安装包

`package.json` 文件是用来定义应用程序名称和启动应用程序的主文件的地方。这也是我们定义所需包的地方。

我们有两种方式可以将包添加到项目中：`直接将其写入 package.json` 和 `通过命令行安装`。这两种方式都会我们将需要的包添加到 `package.json` 的 `dependencies` 部分。

#### 方法 1. 直接将包写入 Package.json

这是一个我们添加了 Express 依赖的 `package.json` 文件。

```json
1 {
2   "name": "packages-install",
3   "main": "server.js",
4   "dependencies": {
5     "express": "~4.8.6"
6   }
7 }
```

就是这样，我们现在已经将 Express 设置为应用程序的一个包，并拥有了 MEAN 栈的两个部分！(_E_N)

***

![注意：npm 版本号](img/icon-pencil.png "请注意")

注意：npm 版本号

> 你可能在想在 Express 版本号旁边的那个波浪号 (`~`) 是干什么用的。npm 在声明包版本时使用[语义化版本](https://www.npmjs.org/doc/misc/semver.html)。这意味着波浪号将拉取与你指定的`合理接近`的版本。在这个示例中，只会安装版本大于 `4.8.6` 且小于 `4.9` 的 Express 版本。

> 这三个数字分别代表该版本的不同部分。例如，在 express 4.8.6 中，4 代表主版本，8 代表次版本，6 代表补丁（patch）。通常 bug 修复会被归类为补丁，并且不会破坏任何内容。次版本更新会添加新功能，但仍然不会破坏你之前的代码。而主版本更新可能会破坏现有代码，正如你们中一些可能已经知道的那样，这可能会让你想抓头发。

> 使用这种版本控制是一种良好的实践，因为我们确保了只有我们指定的版本会被拉取到我们的项目中。我们能够获取直到 `4.9` 版本之前的 bug 修复，但不会引入随 `5.0` 版本而来的任何重大更改。

> 如果我们将来重新访问此应用程序并使用 `npm install`，我们确切知道正在使用哪个版本的 Express，并且不会因为引入自该项目创建后的任何新版本而破坏我们的应用。

***

#### 方法 2. 从命令行添加包

向应用程序添加包的第二方法是使用命令行的 npm 快捷方式。这通常是更简单、更好的路线，因为 npm 可以自动将包保存到你的 `package.json` 文件中。酷酷的地方在这里：`它会添加正确的版本号`！如果你手动将包写入 `package.json`，你将得在网上寻找正确的版本号。这种方法让生活变得简单得多。

以下是安装 express 的命令，`--save` 修符会将其添加到 `package.json`。

```
npm install express --save
```

你会注意到上面的命令获取了 express 包并将其安装在名为 `node_modules` 的新文件夹中。这是 Node 项目中包所在地。该命令只安装我们显式调用的包（在本例中为 express）。

### 安装所有包

方法 2 会为我们安装包。方法 1 会将包添加到你的 `package.json` 中，但还没有安装它们。要将 `package.json` 中 `dependencies` 属性下的所有包安装到 `node_modules` 文件夹，只需输入：

```
npm install
```

它将查看我们需要的依赖项并将它们拉取到应用程序的 `node_modules` 中。

### 安装多个包

npm 还提供了一种安装多个包的方便方法。只需在一个 `npm install` 命令中输入所有你需要的包，它们就会被引入项目。

```
npm install express mongoose passport --save
```

这是一种引入所需包的简单快捷的方法。

## 总结

现在当我们想要启动一个新的 Node 项目时，我们只需要在想要创建项目的文件夹中运行两个命令：

1. `npm init`
2. 在提示时填写必要的字段以创建 `package.json` 文件。
3. `npm install express --save`

就是这样，我们拥有了设置应用程序所需的所有内容！

让我们继续前进，深入研究使用 Express 和 Node 为我们的 MEAN 栈应用搭建基础。

## 启动 Node 服务器

我们将继续查看设置 Node 服务器的方法。在上章中，我们只向控制台输出了内容。在本章中我们将向用户发送 HTML 文件。

### 方法 1：纯 Node (无 Express)

使用方法 1 时，我们将引入 Node 内置的两个模块。[http module](https://nodejs.org/api/http.html#http) 用于启动 HTTP 服务器并响应用户的请求。[fs module](https://nodejs.org/api/fs.html#file_system) 用于读取文件系统。我们需要从文件系统读取 `index.html`，然后通过 HTTP 服务器将其传递给用户。

## 示例应用程序

在本章的示例中，我们需要一个包含以下文件的文件夹：

*   package.json
*   server.js
*   index.html

正如之前学的，`package.json` 将项目的配置/包，而 `server.js` 将包含应用程序设置和配置。我们的 `index.html` 将是一个基础 HTML 文件。

`package.json` 和 `index.html` 对于两种方法都是相同的。两种方法之间变化的文件只有 `server.js`，因为那是启动 Node 服务器的地方。

#### package.json

这是我们简单的 `package.json` 文件：

```json
1 {
  "name": "http-server",
  "main": "server.js"
}
```

#### index.html

让我们填写一个简单的 `index.html` 文件：

```html
 1 <!DOCTYPE html>
 2 <html lang="en">
 3 <head>
 4 	<meta charset="UTF-8">
 5 	<title>Super Cool Site</title>
 6 	<style>
 7 		body { 
 8 			text-align:center; 
 9 			background:#EFEFEF; 
 10 			padding-top:50px;
 11 		}
 12 	</style>
 13 </head>
 14 <body>
 15 
 16 	<h1>Hello Universe!</h1>
 17 	
 18 </body>
 19 </html>
```

#### 方法 2：使用 Express

由于 Express 是 MEAN 栈的主要部分之一，我们希望使用这种方法。在学习学习了这种方法后，你可能再也不想回头了。




```
 1 // get the http and filesystem modules
 2 var http = require('http'),
 3   fs = require('fs');
 4 
 5 // create our server using the http module
 6 http.createServer(function(req, res) {
 7 
 8   // write to our server. set configuration for the response
 9   res.writeHead(200, {
10     'Content-Type': 'text/html',
11     'Access-Control-Allow-Origin' : '*'
12   });
13 
14   // grab the index.html file using fs
15   var readStream = fs.createReadStream(__dirname + '/index.html');
16 
17   // send the index.html file to our user
18   readStream.pipe(res);  
19 
20 }).listen(1337);
21 
22 // tell ourselves what's happening
23 console.log('Visit me at http://localhost:1337');
```

我们正在使用 `http` 模块创建一个服务器，并使用 `fs` 模块获取索引文件并在我们的响应中发送给用户。

现在已经定义了 `server.js` 文件，让我们进入命令行并启动我们的 Node http 服务器。

`nodemon server.js`

你应该能看到服务器启动，并且控制台打印了一条消息。

![Node HTTP 服务器控制台](img/06-node-server----http-server-console.jpg)

Node HTTP 服务器控制台

现在我们可以在浏览器中通过 `http://localhost:1337` 查看我们的网站。

![Hello Universe 浏览器](img/06-node-server----hello-browser.jpg)

Hello Universe 浏览器

我们终于向用户发送了一个 HTML 文件！你可能在认为设置这个 http 服务器需要了大量你可能记不住的语法。不过不用担心，Express 的方式要简洁得多。

### 方法 #2：使用 Express

既然我们已经使用 HTTP 模块启动了服务器，让我们看看如何使用 Express 实现相同的功能。你会发现管理代码会变得简单得多。

我们首先需要将 Express 添加到此项目中。让我们使用命令行安装它并将其保存到 `package.json` 中。

`npm install express --save`

现在让我们修改 `server.js` 文件以适配 Express。我们将从调用 Express 开始。使用该 Express 实例，我们将定义一个路由并发送 `index.html` 文件。然后我们将在特定端口上“监听”来自浏览器的请求。

```
 1 // load the express package and create our app
 2 var express = require('express');
 3 var app     = express();
 4 var path = require('path');
 5   
 6 // send our index.html file to the user for the home page
 7 app.get('/', function(req, res) {
 8 	res.sendFile(path.join(__dirname + '/index.html'));
 9 });
10 
11 // start the server
12 app.listen(1337);
13 console.log('1337 is the magic port!');
```

现在我们获取了 Express，设置了端口并启动了服务器。Express 让启动服务器的工作变得更容易，语法也更简洁。使用 `nodemon server.js` 启动该服务器将再次向 `http://localhost:1337` 的用户输出我们的 HTML 文件。

我们将看到与之前相同的结果，但现在代码更容易理解了。

![Hello Universe 浏览器](img/06-node-server----hello-browser.jpg)

Hello Universe 浏览器

* * *

![提示](img/icon-heart.png "专业级提示")

提示

### 定义包的快捷方法

定义包时的一个小技巧：不要在每次定义包时都输入 `var`，你可以使用 `","` 将包连接起来。

这是一个示例：

```
1 var express = require('express');
2 var app = express();
3 
4 // the exact same result
5 
6 var express = require('express'),
7     app = express();
```

这只是为了稍微整理一下你的代码，并让你跳过几次额外的按键。

* * *

我们现在可以创建一个 Node 服务器并向用户发送 HTML 文件。到目前为止，我们定义了一个简单的 `get` 路由。让我们迈下一步，为我们的网站添加更多路由和页面。

## Node 的路由

为了给我们的网站添加更多页面，我们需要更多的路由。这可以通过 Express 内置的一个功能——Express Router 来实现。这将是一个大章节，因为路由将成为我们以后所有应用程序的巨大大部分。这就是我们对基础到高级网站进行路由的方法，也是我们最终构建 Angular 前端应用程序将使用的 RESTful API 的方式。展望未来真是令人兴奋！不过要一步步来。让我们开始路由。

### Express Router

Express Router 到底是什么？你可以把它看作是一个没有所有花哨功能的微型 Express 应用，只包含路由功能。它不引入视图或设置，但为我们提供了诸如 `.use()`、`.get()`、 `.param()` 和 `.route()` 这样的路由 API。让我们看看这具体意味着什么。

使用路由有几种不同的方法。我们在创建主页时已经使用了其中一种方法 `app.get('/', ...)`。我们将查看其他方法。

## 示例应用程序

我们要为应用程序添加的主要功能：

* 基础路由（我们已经创建了首页）
* 站点章节（路由部分）
* 路由日志控制台
* 带参数的路由（http://localhost:1337/admin/users）
* 路由中间件
* 登录路由（GET）

**什么是路由中间件？** 中间件在用户请求和最终响应之间调用。我们将在处理请求时讨论它。

正如我们一直所做的，我们将路由放在 `server.js` 中。我们不需要 `package.json` 的任何更改。

### 基础路由

我们已经定义了首页的基础路由。Express 允许我们在 `app` 对象上定义路由。我们还可以处理 `GET`、`POST`、`PUT/PATCH` 和 `DELETE` 等操作。

这是定义路由最简单的方法，但随着应用程序的扩大，我们需要对路由进行组织。想象一个有一个管理部分和一个前端部分的应用程序，每个部分都有多个路由。

### express.Router()

[express.Router](https://expressjs.com/api#router) 充当微应用。你可以像调用 Express 一样调用并在上面定义路由。让我们看一个示例，确切这意味着什么。如果你想尝试，请将其添加到 `server.js`。

在 `server.js` 的 `app.get()` 路由下方添加以下内容。我们将 1. **调用路由实例** 2. **对其应用路由** 3. 然后**将这些路由添加到主应用中**：

```
 1 // create routes for the admin section
 2 
 3 // get an instance of the router
 4 var adminRouter = express.Router();
 5 
 6 // admin main page. the dashboard (http://localhost:1337/admin)
 7 adminRouter.get('/', function(req, res) {
 8 	res.send('I am the dashboard!');
 9 });
10 
 11 // users page (http://localhost:1337/admin/users)
 12 adminRouter.get('/users', function(req, res) {
 13 	res.send('I show all the users!');
 14 });
 15 
 16 // posts page (http://localhost:1337/admin/posts)
 17 adminRouter.get('/posts', function(req, res) {
 18 	res.send('I show all the posts!');
 19 });
20 
 21 // apply the routes to our application
 22 app.use('/admin', adminRouter);
```





我们现在可以访问管理面板页面 `http://localhost:1337/admin` 以及子页面 `http://localhost:1337/admin/users` 和 `http://localhost:1337/admin/posts`。

注意看我们如何为刚刚定义的这些路由设置默认根路径。如果我们将第 22 行更改为 `app.use('/app', router)`，那么我们的路由将变为 `http://localhost:1337/app/` 和 `http://localhost:1337/app/users`。

这是非常强大的，因为我们可以创建多个 `express.Router()` 并将它们应用到应用程序中。我们可以为基础路由、身份验证路由甚至 API 路由分别创建一个 `Router`。

通过使用 `Router`，我们允许通过创建多个 `Router` 实例并相应地应用它们，使应用程序比以往任何时候都更加模块化和灵活。现在我们将查看如何使用中间件来处理请求。

### 路由中间件 (`router.use()`)

Express 中的路由中间件是在处理请求之前执行某些操作的方法。这可以是检查用户是否已通过身份验证、为分析记录数据，或者我们在向用户输出信息之前想做的任何其他事情。

这里有一些中间件，可以在每次发送请求时向控制台打印一条消息。这将演示如何使用 `Express Router` 创建中间件。我们将该中间件添加到上一个示例中创建的 `adminRouter` 中。确保它放置在 `adminRouter` 声明之后，在我们定义的 users 和 posts 路由之前。你还会注意到这里的 `next` 参数。这是 Express 知道函数已完成并可以继续处理下一个中间件或继续路由的唯一方式。

```
1 // 在每个请求上都会发生的路由中间件
2 adminRouter.use(function(req, res, next) {
3 
4 	//向控制台记录每个请求
5 	console.log(req.method, req.url);
6 
7 	// 继续之前的操作并进入路由
8 	next(); 
9 });
```

`adminRouter.use()` 用于定义中间件。现在，它将应用到进入我们此 `Router` 实例的所有请求上。让我们进入浏览器访问 `http://localhost:1337/admin`，我们将在控制台中看到该请求。

![Express Router Console Request](img/07-node-routing----express-router-console-log-request.jpg)

Express Router Console Request

**你放置中间件和路由的顺序非常重要** 一切将按照它们出现的顺序发生。这意味着如果你将中间件放在路由之后，那么路由将在中间件之前执行，请求将结束于此。你的中间件在那个点不会运行。

请记住，你可以将路由中间件用于很多事情。你可以用它在允许用户继续之前，检查会话期间用户是否已登录。

### 路由结构

通过使用 `Router()`，我们能够划分网站的部分。这意味着你可以为网站前端等路由创建一个 `basicRouter`。你也可以为受某种类型身份验证保护的管理路由创建一个 `adminRouter`。

通过这种方式对我们的应用程序进行路由让我们独立每个部分。这为我们复杂的应用程序或 API 提供了所需的灵活性。我们还可以保持应用程序的整洁，由于我们可以将每个路由定义移动到自己的文件中，只需在调用 `app.use()` 时引入这些文件即可：

```
1 app.use('/', basicRoutes);
2 app.use('/admin', adminRoutes);
3 app.use('/api', apiRoutes);
```

### 带参数的路由 (`/hello/:name`)

为了查看我们如何为应用程序添加路由参数，假设我们有一个名为 `/admin/users/:name` 的路由，其中我们可以向 URL 传递人的名字，应用程序将输出名字！我们也可以在实际应用程序中使用它来获取该用户的信息。让我们看看这种路由是什么样的。

```
1 // 带参数的路由 (http://localhost:1337/admin/users/:name)
2 adminRouter.get('/users/:name', function(req, res) {
3 	res.send('hello ' + req.params.name + '!');
4 });
```

现在我们可以访问 `http://localhost:1337/admin/users/holly` 并看到我们的浏览器输出 holly！`req.params` 存储了来自原始用户请求的所有数据。简单。

![Express Router Parameters](img/07-node-routing----express-router-parameters.png)

Express Router Parameters

在未来，我们可以利用此来获取所有匹配 `holly` 的用户数据。然后我们可以构建一个管理面板来管理我们的用户。现在假设我们想以某种方式验证这个名字。也许我们想确保它不是坏名字。我们将在路由中间件内部执行此。我们将使用一个特殊的中间件来处理。

#### 参数的路由中间件 (`.param()`)

我们将使用 Express 的 `.param()` 中间件。这会创建一个为特定路由参数运行的中间件。在我们的情况下，我们在 hello 路由中使用了 `:name`。再次确保中间件放置在请求之前。

```
1 // 验证 :name 的路由中间件
2 adminRouter.param('name', function(req, res, next, name) {
3 	//在此处对 name 进行验证
4 	// 验证逻辑
5 	// 记录某些内容以便知道它正在运行
6 	console.log('doing validations on ' + name);
7 
8 	// 验证完成后将新项保存到 req 中
9 	req.name = name;
10 	// 继续后续操作
11 	next(); 
12 });
13 
14 // 带参数的路由 (http://localhost:1337/admin/hello/:name)
15 adminRouter.get('/hello/:name', function(req, res) {
16 	res.send('hello ' + req.name + '!');
17 });
```

现在当我们访问 `/hello/:name` 路由时，我们的路由中间件将介入并生效。我们可以运行验证，然后通过将新变量存储在 `req`（请求）中传递给我们的 `.get` 路由。我们通过将 `req.params.name` 更改为 `req.name` 来访问它，因为我们在中间件中获取了 `req.params.name` 并将其存储到 `req` 中。

当我们访问浏览器 `http://localhost:1337/admin/hello/sally` 时，我们会在控制台中看到请求。

![Express Router Middleware](img/07-node-routing----express-router-middleware.png)

Express Router Parameter Middleware

参数路由中间件可以验证传入应用程序的数据。如果你也创建了 RESTful API，你可以验证令牌并确保用户能够访问你的信息。我们到目前为止所做的工作将导致构建我们在第 3 章讨论客户端服务器模型时提到的服务器端应用程序。

我们将查看的最后一个 Express 路由功能是如何使用 `app.route()` 同时定义多个路由。

#### 登录路由 (`app.route()`)

我们可以直接在应用上定义路由。这类似于使用 `app.get`，但我们将使用 `app.route`。`app.route` 基本上是调用 Express Router 的快捷方式。与其调用 `express.Router()`，我们可以调用 `app.route` 并那里开始应用路由。

使用 `app.route()` 允许我们在单个登录路由上定义多个操作。我们需要一个 `GET` 路由来显示登录表单，以及一个 `POST` 路由来处理登录表单。

```
1 app.route('/login')
2 
3 	// 显示表单 (GET http://localhost:1337/login)
4 	.get(function(req, res) {
5 		res.send('this is the login form');
6 	})
7 
8 	// 处理表单 (POST http://localhost:1337/login)
9 	.post(function(req, res) {
10 		console.log('processing');
11 		res.send('processing the login form!');
12 	});
```

现在我们为 `/login` 路由定义了两个不同的操作。简单且非常整洁。这些直接应用于 `server.js` 文件中的主 `app` 对象，但我们也可以在早先创建的 `adminRouter` 对象中定义它们。




这是一种设置路由的好方法，因为它非常整洁，并且便于查看哪些路由被应用于什么地方。我们很快将构建一个 RESTful API，我们应该做的主要事情之一使用不同的 HTTP 动词来表示对应用程序的操作。`GET /login` 将提供登录表单，而 `POST /login` 将处理登录逻辑。

## 总结

通过 Express Router，我们在定义路由时具有极大的灵活性。回顾一下，我们可以：

* 多次使用 `express.Router()` 来定义一组路由
* 使用 `app.use()` 将 `express.Router()` 应用于网站的某个部分
* 使用路由中间件来处理请求
* 使用路由中间件通过 `.param()` 验证参数
* 使用 `app.route()` 作为通往 Router 的快捷方式，在单个路由上定义多个请求

现在我们已经打下了 Node 和 Express 的坚实基础，让我们继续前进，进一步讨论一下 MongoDB。然后，我们将进入服务器端应用程序的核心部分：构建 API！

## 使用 MongoDB

MongoDB 被推崇为一种易用、提供高性能和高可用性的数据库。我们已经在书的入门章节（第 3 章）中讨论过 MongoDB 的优点。

在本章中，我们将讨论安装 MongoDB 并在本地使用它，以便我们将其用于未来的应用程序。

![MongoDB](img/08-mongodb----mongodb.png "MongoDB")

### MongoDB

除了在本地安装 MongoDB 之外，我们将在像 [Modulus.io](https://modulus.io/) 或 [mongolab](https://mongolab.com/) 这样的托管解决方案创建一个数据库。

![Mongolab](img/08-mongodb----mongolab.jpg "Mongolab")

### Mongolab

为了重申 MongoDB 在像 MEAN 等技术栈中的优势，`面向文档的存储` 让我们整个技术栈的开发变得更加简单。由于我们在数据库中使用 JSON 风格的文档，它们可以从数据库 (`MongoDB`) 到服务器 (`Node.js`) 再到前端 (`AngularJS`) 一直以相同的方式使用。

让我们开始 MongoDB 的安装和简单用法。

### 在本地安装 MongoDB

在本地使用 MongoDB 时，有几个步骤需要注意。这个过程对于不同的操作系统是相同的，尽管每个步骤的细微细节可能不同。主要步骤如下：

1. 安装 MongoDB
2. 创建一个文件夹（具有适当权限）来存储数据库数据
3. 启动 MongoDB 服务
4. 在服务启动后连接或在应用程序中使用

让我们查看 Mac 和 Windows 的安装步骤（Linux 指南可以在 [MongoDB 文档](http://docs.mongodb.org/manual/tutorial/install-mongodb-on-ubuntu/) 中找到），然后我们将转向可以在 MongoDB 中使用的基本命令。

#### Mac 安装

[在 Mac 上安装]时，默认文件夹为 `/data/db`。这是存储所有内容的地方，你必须确保你拥有该文件夹的权限，以便 MongoDB 可以向其写入。

我们可以使用 Homebrew 或 [手动](http://docs.mongodb.org/manual/tutorial/install-mongodb-on-os-x/#install-mongodb-manually) 在 Mac 上安装。本文将重点关注 Homebrew。

```
1 // 更新你的包
2 $ brew update
3 
4 
5 // 安装 mongoDB
6 $ brew install mongodb
```

运行以下命令以确保一切运行正常：

```
1 $ mongod
```

这将启动 MongoDB 服务，你应该会看到 `waiting for connections on port 27017`。如果你看到关于权限的错误，请确保你更改了 `/data/db` 文件夹的权限，以便你拥有适当的权限。

![Starting MongoDB Service](img/08-mongodb----mongo-start.jpg)

启动 MongoDB 服务

现在 MongoDB 服务已经启动，我们可以使用以下命令连接到它：

`mongo`

确保你在独立的终端窗口中运行此命令，以便我们确定服务仍在运行。

![Connecting to MongoDB](img/08-mongodb----mongo-connect.jpg)

连接到 MongoDB

你将在启动服务的终端上看到连接发生。请直接跳过此处关于 Windows 安装的下一章节，我们将通过简单命令使用 MongoDB。

#### Windows 安装

Windows 的设置非常直观。首先从[此处](http://www.mongodb.org/downloads) 下载 MongoDB。下载完成后，你可能需要将 MongoDB 可执行文件的路径（通常是 Program Files 文件夹）添加到你的环境变量中，这样你就不需要每次都显式地输入完整路径来运行 Mongo。

打开你的环境变量，输入你安装 MongoDB 的 bin 文件夹路径（我们使用的是 `C:\Program Files\MongoDB 2.6 Standard\bin`）。如果你已经在 PATH 变量中有了自己的内容，可以添加一个分号并紧随其插入新路径。

![MongoDB Environment Variable](img/08-mongodb----environment-variables.png "MongoDB Environment Variable")

MongoDB 环境变量

现在你应该能够在命令行中运行：

`mongod`

你可能会遇到的常见错误是 `dbpath (\data\db) does not exist`。如果你收到此错误，请在你的 C 目录下创建此路径 `C:\data\db`。这是你所有数据存储的地方。

如果你想指定与默认 `data/db` 不同的路径，可以像这样传递路径：

`mongod --dbpath path/to/folder`

一旦创建了路径，使用 `mongod.exe C:Program Files` 启动 mongo，你应该就会看到“waiting for connections on port 27017”。如果你看到关于权限的错误，请确保更改了 `/data/db` 文件夹的权限，以便你拥有适当的权限。

![Starting MongoDB Service](img/08-mongodb----mongo-start.jpg)

启动 MongoDB 服务

现在 MongoDB 服务已经启动，我们可以使用以下命令连接到它：

确保你在独立的终端中运行此命令，以便我们确定服务仍在运行。

![Connecting to MongoDB](img/08-mongodb----mongo-connect.jpg)

连接到 MongoDB

你将在启动服务的终端上看到连接发生。请直接跳过此处关于 Windows 安装的下一章节，我们将通过简单命令使用 MongoDB。

## 常用数据库命令

在数据库中的查询可能与你习惯的有所不同。与其查询表，我们是在查询文档集合。

由于数据是以 JSON 风格的文档存储的，我们的语法与我们的应用程序相似。

一旦我们通过 `mongod` 和 `mongo` 连接到 MongoDB，就可以查看并使用数据库了。这里是常用命令。

### 列出所有数据库

```
1 $ show databases
```

### 创建数据库

**除非向数据库插入信息，否则 MongoDB 不创建数据库。**

技巧是你不需要式创建数据库！只需使用数据库（即使它尚未创建）、创建集合和文档，一切都会为你创建！

我们将在 CRUD 部分查看集合和文档。

### 显示当前数据库

```
1 $ db
```

### 选择数据库

```
1 $ use db_name
```

现在我们有了数据库的基础，让我们进入主要的 CRUD 命令。

### CRUD 命令

通过以下命令，我们可以熟悉 MongoDB 命令。这些命令与我们在 Node.js 应用程序中处理 CRUD 操作相似。

### 创建

```
1 // 保存一个用户
2 $ db.users.save({ name: 'Chris' });
3 
4 // 保存多个用户
5 $ db.users.save([{ name: 'Chris'}, { name: 'Holly' }]);
```

通过将文档保存到当前数据库的 `users` 集合中，如果它们尚不存在，你就成功地创建了数据库和集合。

### 读取

```
1 // 显示所有用户
2 $ db.users.find();
3 
4 // 查找特定用户
5 $ db.users.find({ name: 'Holly' });
```

### 更新

```
1 db.users.update({ name: 'Holly' }, { name: 'Holly Lloyd' });
```

### 删除

```
1 // 删除所有
2 db.users.remove({});
3 
4 // 删除一个
5 db.users.remove({ name: 'Holly' });
```



[content]
这只是对你可以运行的命令类型的简要概述。[MongoDB 文档](http://docs.mongodb.org/manual/core/crud-introduction/) 非常详尽，为那些想要深入研究的人提供了大量的细节。

MongoDB 还为你提供了一个非常棒的[交互式教程](http://try.mongodb.org/)，让你走一遍上述命令。

## GUI 工具：Robomongo

虽然使用我们的命令行进入 MongoDB 数据库非常简单，但对于那些倾向于使用图形化界面的人来说，也有一个 GUI 工具。

尽管去下载 [Robomongo](http://robomongo.org/) 并启动它。

与我们的数据库建立连接非常简单。只需将地址设置为 `localhost`，将端口设置为 `27017`。你可以为你的连接起任何名称。

![Robomongo Connect](img/08-mongodb----robomongo-connect-local.jpg)

Robomongo Connect

一旦连接成功，你就可以访问所有的数据库及其各自的集合了！你现在有了一个 GUI 来处理数据库操作，甚至可以打开一个 shell 来深入操作我们之前讨论过的命令。

![Robomongo Connect to Database](img/08-mongodb----robomongo-local-db.jpg)

Robomongo Connect to Database

## 在 Node.js 中使用 MongoDB

如你所见，使用 MongoDB 本地实例是一个非常直接的过程。此后，你可以使用 MongoDB 本地实例或托管实例（[modulus.io](https://modulus.io/) 或 [mongolab.com](https://mongolab.com/)）。

无论如何，我们都使用 [mongooseJS](http://mongoosejs.com/)，这是一个用于处理 MongoDB 的 Node 包。

你只需要配置 mongoose 连接到本地数据库即可。这是一个简单的过程，因为我们甚至不需要创建数据库。如果我们与本地 MongoDB 工作，只需要运行以下命令确保 MongoDB 已经启动：

```
1 $ mongod
```

### 使用 Mongoose 连接 MongoDB 数据库

连接数据库是一个非常简单的过程。这里有一些在 Node 中连接数据库的示例代码：

```
1 // 获取我们需要的包
2 var mongoose = require('mongoose');
3 
4 mongoose.connect('mongodb://localhost/db_name');
```

就是这样！一旦我们开始向数据库中保存内容，名为 `db_name` 的数据库就会被自动创建。

现在我们已经理解了 MongoDB 及其使用方法，让我们在 Node.js 应用程序实现 CRUD 并使用 mongooseJS 使用 MongoDB 吧。

接下来的任务是构建一个 Node.js API。

## 构建一个 RESTful Node API

### 什么是 REST？

关于 RESTful API 的一点介绍，请看这个非常棒的演示文稿：[教狗学 REST](http://www.slideshare.net/landlessness/teach-a-dog-to-rest)。

[RESTful APIs](http://scotch.io/bar-talk/designing-a-restful-web-api) 正在成为 Web 服务的标准。现在仅仅构建一个应用程序是不够的，我们正在转向可以与多个设备和其他网站集成的平台发展。

互联互性正迅速成为游戏的关键。随着 [IFTTT](https://ifttt.com/) 和 [Zapier](https://zapier.com/) 等项目的日益流行，用户已经表明他们喜欢让自己的应用程序连接在一起。这意味着他们所有的应用程序都有一种标准的方式相互“对话”。IFTTT 允许你设置触发器和响应，例如“当我写推文时，将其分享为我的 Facebook 状态”。Twitter 和 Facebook 的 API 允许我们做到这一点。

![IFTTT](img/ifttt.jpg)

IFTTT

像 Facebook 和 Google 这样的行业巨头有自己跨越多个第三方应用的 API。你甚至可以找到它们的 API 探索器，可以在那里对它们的 API 进行测试驱动，并查看你可以从 API 中提取什么信息。例如，一旦登录，你就可以从 [API 探索器](https://developers.facebook.com/tools/explorer/145634995501895/?method=GET&path=me%3Ffields%3Did%2Cname&version=v2.1) 获取所有朋友的数据。使用 API 已经迅速成为构建应用程序的标准。

仅仅让应用程序独立运行是不够的，你必须使用相同的数据构建一个网站和多个移动应用。如果你的应用程序火了，你将希望用户能够基于你的数据构建第三方应用程序。这就是你的 API 发挥用场的地方。我们将学习如何使用 Node 构建一个 API，以便多个应用程序可以使用该 API 和你的数据。

### 为我们的 Angular 前端提供后端服务

在本章中，我们将学习使用 Node、Express 4 及其 Router 以及 Mongoose 创建一个 RESTful API，并与 MongoDB 实例交互。我们还将使用 Chrome 中的 [Postman](https://chrome.google.com/webstore/detail/postman-rest-client-packa/fhbjgbiflinjbdggehcddcbncdddomop) 或 Firefox 中的 [RESTClient](https://addons.mozilla.org/en-US/firefox/addon/restclient/) 来测试我们的 API。

这是一个与我们之前章节完全不同的示例应用程序，我们将在到达 Angular 前端时在后续几个章节中使用它。让我们看看我们想要构建的 API 及其能做什么。

## 示例应用程序

假设我们要……（此处原文似乎存在重复或截断，将按逻辑翻译剩余部分）

（注：由于原文从此处开始出现了大量重复的占位符描述，根据“不要重复输出原文”的原则，我将针对其核心逻辑结构进行翻译处理。）

假设我们要构建一个 Node.js API。我们将使用 Node、Express 4 及其 Router 以及 Mongoose 来与 MongoDB 实例交互。我们将使用 Postman 或 RESTClient 来测试 API。



Node 的包管理器将引入我们在 `package.json` 中定义的所有包。简单且易用。现在我们已经有了这些包，让我们在设置 API 时开始使用它们吧。

我们将通过 `server.js` 文件来设置应用程序，因为这是我们在 `package.json` 中声明的主文件。

## 设置我们的服务器 (server.js)

Node 在启动应用程序时会查看此文件，以便它知道我们想要如何配置应用程序和 API。

我们将从启动应用程序所需的最基本要素开始。我们将保持代码的整洁并进行良好的注释，这样我们就能准确了解每一步发生了什么。

```javascript
 1 // BASE SETUP
 2 // ======================================
 3 
 4 // CALL THE PACKAGES --------------------
 5 var express    = require('express'); // 调用 express
 6 var app        = express(); // 使用 express 定义我们的 app
 7 var bodyParser = require('body-parser'); // 获取 body-parser
 8 var morgan     = require('morgan'); // 用于查看请求
9 var mongoose   = require('mongoose'); // 用于处理我们的数据库
10 var port       = process.env.PORT || 8080; // 为我们的应用设置端口
 11 
12 // APP CONFIGURATION ---------------------
13 // 使用 body parser，以便我们可以从 POST 请求中获取信息
14 app.use(bodyParser.urlencoded({ extended: true }));
15 app.use(bodyParser.json());
16 
17 // 配置我们的应用以处理 CORS 请求
18 app.use(function(req, res, next) {
19   res.setHeader('Access-Control-Allow-Origin', '*');
20   res.setHeader('Access-Control-Allow-Methods', 'GET, POST');
21   res.setHeader('Access-Control-Allow-Headers', 'X-Requested-With,content-type, \
22 Authorization');
23   next();
24 });
25 
26 // 将所有请求记录到控制台 
27 app.use(morgan('dev'));
28 
29 // ROUTES FOR OUR API
30 // =============================
31 
32 // 首页的基础路由
33 app.get('/', function(req, res) {
34 	res.send('Welcome to the home page!');
35 });
36 
37 // 获取 express 器的实例
38 var apiRouter = express.Router();
39 
40 // 测试路由以确保一切运行正常 
41 // 访问地址为 GET http://localhost:8080/api
42 apiRouter.get('/', function(req, res) {
43 	res.json({ message: 'hooray! welcome to our api!' });	
44 });
45 
46 // 更多 API 路由将在这里
47 
48 // REGISTER OUR ROUTES -------------------------------
49 // 我们所有的路由将以 /api 为前缀
50 app.use('/api', apiRouter);
51 
52 // START THE SERVER
53 // ===============================
54 app.listen(port);
55 console.log('Magic happens on port ' + port);
```

哇，我们做了很多工作！不过这一切都很简单，让我们仔细过一遍吧。

**基础设置 (Base Setup)**：在基础设置中，我们引入了之前通过 `npm` 引入的所有包。我们将获取 `express`、`mongoose`，定义我们的应用，获取 `bodyParser` 并配置我们的应用使用它。我们还可以为应用程序设置 `port`，并获取稍后定义的用户模型。

我们正在设置配置以允许来自其他域的请求，防止 CORS 错误。这允许任何域名访问我们的 API。

**API 路由 (Routes for Our API)**：此部分将包含我们所有的路由。使用 `Express Router` 的结构允许我们引入路由实例。然后我们可以定义路由，并将这些路由应用到根 URL（在本例中为 API）。 true 一个首页路由用于打招呼；这只是一个为了确保一切运行正常的基础路由。

**启动服务器 (Start the Server)**：我们将让 `express` 应用监听我们之前定义的 `port`。。，我们的应用程序就会上线，我们可以对它进行测试了！

## 启动服务器并测试

让我们确保到目前为止一切都运行正常。我们将启动 Node 应用，然后向我们定义的唯一路由发送请求，以确保我们收收到响应。

让我们启动服务器。在命令行中输入：

```bash
nodemon server.js
```

你应该能看到你的 Node 应用已启动，Express 将创建一个服务器。

![Starting Node Server](img/09-restful-api----start-node-server.jpg)

启动 Node 服务器

现在我们知道应用程序已经运行了，让我们测试一下它。你应该可以通过访问基础路由 `http://localhost:8080` 看到我们返回的消息。现在让我们测试其他剩余的路由（API 路由）。

![Basic Route](img/09-restful-api----basic-route.jpg)

基础路由

### 使用 Postman 测试我们的 API

现在在浏览器中导航到 `http://localhost:8080/api`，你将看到我们的 JSON 消息。看到它固然，但测试 API 的最佳方法是使用专门为此构建的工具。Postman 将帮助我们测试 API。





```javascript
 1 // grab the packages that we need for the user model
 2 var mongoose = require('mongoose');
 3 var Schema = mongoose.Schema;
 4 var bcrypt = require('bcrypt-nodejs');
 5 
 6 // user schema 
 7 var UserSchema   = new Schema({
 8 	name: String,
 9     username: { type: String, required: true, index: { unique: true }},
10     password: { type: String, required: true, select: false }
11 });
12 
13 // hash the password before the user is saved
14 UserSchema.pre('save', function(next) {
15 	var user = this;
16 
17 	 hash the password only if the password has been changed or user is new
18 	if (!user.isModified('password')) return next();
19 
20 	 generate the hash
21 	bcrypt.hash(user.password, null, null, function(err, hash) {
22 		if (err) return next(err);
23 
24 		 // change the password to the hashed version
25 		user.password = hash;
26 		next();
27 	});
28 });
29 
30 // method to compare a given password with the database hash
31 UserSchema.methods.comparePassword = function(password) {
32 	var user = this;
33 
34 	return bcrypt.compareSync(password, user.password);
35 };
36 
37 // return the model
38 module.exports = mongoose.model('User', UserSchema);
```

这里发生了很多操作，但它非常简单。我们必须创建自己的 Schema（模式）。我们把 `name`、`username` 和 `password` 定义为 `Strings`（字符串）。通过设置 `index` 和 `unique` 属性，我们正在告诉 Mongoose 为此路径创建一个唯一索引。这意味着用户名不能重复。我们将实现的另一个 Mongoose 特性是在密码属性上设置 `select: false`。当我们查询用户列表或单个用户时，将不需要提供密码。通过将 `select` 设置为 `false`，在列出我们的用户时不会返回密码，除非显式调用它。

我们还使用 `pre` 创建了一个函数，该函数将确保在保存用户之前对密码进行哈希处理。

> 确保我们没有将明文密码保存到数据库是非常重要的。我们必须确保我们的应用程序从开始就尽可能安全。

通过 mongoose，我们还在用户模型上创建了一个方法，将密码与给定的哈希值进行比较。这就是我们将在第 10 章中验证用户的方法。

创建该文件后，让我们将其引入 `server.js` 中，这样我们就可以在应用程序中使用它。我们将在该文件中添加额外行，并像之前一样使用 `require` 来引入功能。

```javascript
1 // server.js
2 
3 // BASE SETUP
4 // ==========================
5 
6 var User     = require('./app/models/user');
```

现在我们的整个应用程序已准备就绪并连接好了，我们可以开始构建我们的路由了。这些路由将定义我们的 API，这也是本章存在的主要原因。继续吧！

### Express Router 和路由

我们将使用 Express Router 的实例来处理所有的 API 路由。下面是我们将需要的路由概述、它们的功能以及访问它们时所使用的 HTTP 动词（Verb）。

| /api/users | `GET` | 获取所有用户 |
| --- | --- | --- |
| /api/users | `POST` | 创建用户 |
| /api/users/:user_id | `GET` | 获取单个用户 |
| /api/users/:user_id | `PUT` | 使用新信息更新用户 |
| /api/users/:user_id | `DELETE` | 删除用户 |

这将涵盖 API 所需的基础路由。这同时也符合良好的格式，我们将我们需要执行的操作（`GET`、`POST`、`PUT` 和 `DELETE`）保持为 HTTP 动词。

### 路由中间件 (Route Middleware)

我们已经定义了第一个路由并看到了它的运行情况。Express Router 为我们定义路由提供了很大的灵活性。

我们在 Node 路由章节中讨论过路由中间件。对于这个示例，我们只是将通过 `console.log()` 将请求打印到控制台。现在让我们将该中间件添加到我们的 `server.js` 文件中。

```javascript
 1 // ROUTES FOR OUR API
 2 // =============================
 3 var apiRouter = express.Router(); 	// get an instance of the express Router
 4 
 5 // middleware to use for all requests
 6 apiRouter.use(function(req, res, next) {
 7 	// do logging
 8 	console.log('Somebody just came to our app!');
 9 
10 	// 我们将在第 10 章在中间件中添加更多内容
11 	// 我们将在这里验证用户
12 
13 	next(); // 确保我们进入下一个路由而不是在这里停止
14 });
15 
16 // test route to make sure everything is working 
17 // (accessed at GET http://localhost:8080/api)
18 apiRouter.get('/', function(req, res) {
19 	res.send('Everything is working!');
20 });
21 
22 // REGISTER ROUTES
23 // ---------------
24 app.use('/api', apiRouter);
```

### 创建基础路由

我们现在为应用程序创建路由。我们将使用 Express 的 `apiRouter.route()` 来处理同一路径的多个路由。

#### 创建用户 POST (/api/users)

我们将添加新路由来处理 POST。

```javascript
 1 // ROUTES FOR OUR API
 2 // ===============================
 3 
 4 // 路由中间件和第一个路由
 5 
 6 // 以 /users 结尾的路由
 7 // --------------------
 8 apiRouter.route('/users')
 9
10 	// 创建用户（访问 POST http://localhost:8080/api/users）
11 	.post(function(req, res) {
12 		
13 		// 创建 User 模型的新实例
14 		var user = new User(); 		
15 
16 		// 设置用户信息（来自请求）
17 		user.name = req.body.name;  
18 		user.username = req.body.username;
19 		user.password = req.body.password;
20 
21 		// 保存用户并检查错误
22 		user.save(function(err) {
23               if (err) {
24                 // 重复条目
25                 if (err.code == 11000) 
26                     return res.json({ success: false, message: '该用户名已存在用户。' });
27                 else 
28                     return res.send(err);
29             }
30 
31 			res.json({ message: 'User created!' });
32 		});
33 		
34 	})
```




我们收到了一条成功消息，显示用户已创建。让我们来处理 API 路由以获取所有用户，这样我们就可以看到刚刚创建的用户。

如果用户名已被占用，`mongoose` 将抛出错误代码 `11000`。如果发生错误，我们将检查该错误代码并返回消息 `'A user with that username already exists.`（已存在该用户名的用户）。

![Duplicate User](img/09-restful-api----duplicate-user.jpg)

重复用户

## 获取所有用户 (GET /api/users)

这是一个简单的路由，我们将将其添加到 `server.js` 中，也就是之前为 POST 创建的 `router.route('/users')` 上。通过 `router.route()`，我们能够使用不同的 HTTP 动作链式不同的路由。这让我们的应用程序保持整洁和有序。

```
 1 // <--路由中间件和第一个路由在这里
 2 
 3 // 在以 /users 结尾的路由
 4 // ----------------------------------------------------
 5 apiRouter.route('/users')
 6
 7	// 创建用户（通过 POST http://localhost:8080/api/users 访问）
 8	.post(function(req, res) {
 9		...			
10 	})
11 
12	// 获取所有用户（通过 GET http://localhost:8080/api/users 访问）
13	.get(function(req, res) {
14 		User.find(function(err, users) {
15 			if (err) res.send(err);
16 
17 // 返回用户
18 			res.json(users);
19 		});
20 	});
```

简单直了的路由。只需向 `http://localhost:8080/api/users` 发送一个 `GET` 请求，我们就能以 JSON 格式获取所有用户。

![Node API Postman GET All](img/09-restful-api----get-after-create.jpg)

Node API Postman 获取所有

我们可以看到 Holly 已经在我们的数据库中了，得益于 `bcrypt` 以及我们创建的那个函数（每当我们保存用户到数据库时它就会运行），她的密码已经被哈希处理了。记得这里为 Holly 自动生成的 `_id` 吗？我们在创建获取单个用户的路由时将用到它。

### 为单个项目创建路由

我们已经处理了以 `/users` 结尾的路由组。现在让我们处理传入参数（如用户 ID）时的路由。

我们在这个路由（以 `/users/:user_id` 结尾）中执行的操作有：

* 获取单个用户。
* 更新用户信息。
* 删除用户。
* 请求中的 `:user_id` 将通过我们稍早调用的那个 `body-parser` 包来访问。

## 获取单个用户 (GET /api/users/:user_id)

我们将添加另一个 `apiRouter.route()` 来处理所有带有 `:user_id` 的请求。同样，将其放入你的 `server.js` 文件中，放在 `apiRouter.route('/users')` 代码块之后。

```
 1 // 在以 /users/:user_id 结尾的路由
 2 // ----------------------------------------------------
 3 apiRouter.route('/users/:user_id')
 4 
 5	// 获取该 id 的用户 
 6	//（通过 GET http://localhost:8080/api/users/:user_id 访问）
 7	.get(function(req, res) {
 8		User.findById(req.params.user_id, function(err, user) {
 9			if (err) res.send(err);
10 
11			// 返回该用户
12 			res.json(user);
13 		});
```

从我们获取所有用户的调用中，我们可以得到所有用户的列表，每个用户都有唯一的 id。让我们取其中一个 id 并用 Postman 进行测试。

输入 `http://localhost:8080/api/users/5481e26e93b9ba717bd5`，选择 `GET` 并点击发送。

这将返回我们的用户数据。简单！

```
 1 {
2     "password": "$2a$10$rgrazsDZHb7C90vq/si0kueePetqUBv2j
3     "username": "chris",
4     "name": "Chris",
5     "_id": "5481e26e93b9ba717bd5",
6     "__v": 0
7 }
```

![Node API Postman Get User](img/09-restful-api----node-api-get-single.jpg)

Node API Postman 获取单个用户

现在我们可以从 API 获取用户了，让我们更新用户的姓名。假设他想更有身份一点，我们将他的名字改为 `Sir Klaus`。

## 更新用户信息 (PUT /api/users/:user_id)

我们将路由链到 `router.route()` 上并添加 `.put()`。

```
 1 // 在以 /users/:user_id 结尾的路由
 2 // -------------------------------------
 3 apiRouter.route('/users/:user_id')
 4 
 5	// 获取该 id 的用户 
 6	//（通过 GET http://localhost:8080/api/users/:user_id 访问）
 7	.get(function(req, res) {
 8		...
 9 	})
10 
11	// 更新此 id 的用户 
12	//（通过 PUT http://localhost:8080/api/users/:user_id 访问）
13	.put(function(req, res) {
14 
15		// 使用我们的用户模型找到用户
16		User.findById(req.params.user_id, function(err, user) {
17 
18			if (err) res.send(err);
19 
20			// 仅更新用户信息
21			if (req.body.name) user.name = req.body.name;
22			if (req.body.username) user.username = req.body.username;
23			if (req.body.password) user.password = req.body.password;
24 
25			// 保存用户
26			user.save(function(err) {
27				if (err) res.send(err);
28 
29				// 返回消息
30				res.json({ message: 'User updated!' });
31 			});
32 
		});
33 	})
```

我们将使用 `PUT` 请求中提供的 `id`，获取该用户，进行更改并将其保存回数据库。注意，只有当 `name`、`username` 或 `password` 发生变化时我们才会更改数据库中的它们。

![Node API Postman Update Record](img/09-restful-api----node-api-postman-update-record.jpg)

Node API Postman 更新记录

由于我们在 PUT 路由中加入了条件判断，如果没有传递 username 或 password，这些字段将不会被更新。我们不希望在未传递的情况下将它们更新为空。

我们还可以使用之前使用的 `GET /api/users` 调用查看她的名字是否已更改。

![Node API Postman All Updated](img/09-restful-api----node-api-postman-all-updated.jpg)

Node API Postman 全部更新

Holly 在数据库中的名字现在从 `Holly` 变成了她的全名 `Holly Lloyd`。快乐时光结束了。现在让我们删除 Holly。

## 删除用户 (DELETE /api/users/:user_id)

当有人请求删除用户时，他们只需要向 `/api/users/:user_id` 发送 `DELETE` 即可。

让我们添加删除用户的代码。

```
 1 // 在以 /users/:user_id 结尾的路由
 2 // ----------------------------------------------------
 3 apiRouter.route('/users/:user_id')
 4 
 5	// 获取该 id 的用户 
 6	//（通过 GET http://localhost:8080/api/users/:user_id 访问）
 7	.get(function(req, res) {
 8		...
 9 	})
10 
11	// 更新此 id 的用户 
12	//（通过 PUT http://localhost:8080/api/users/:user_id 访问）
13	.put(function(req, res) {
14		...
15 	})
16 
17	// 删除此 id 的用户 
18	//（通过 DELETE http://localhost:8080/api/users/:user_id 访问）
19	.delete(function(req, res) {
20		User.remove({
21			_id: req.params.user_id
22		}, function(err, user) {
23			if (err) return res.send(err);
24 
25			res.json({ message: 'Successfully deleted' });
26 		});
27 	});
```

现在当我们使用正确的 `user_id` 向我们的 API 发送 `DELETE` 请求时，我们将用户从世界中删除。

![Node API Postman Delete](img/09-restful-api----node-api-postman-delete.jpg)

Node API Postman 删除

当我们尝试获取所有用户时，你应该注意到现在少了一个。

## 总结

我们现在有能力通过自己的 API 对特定资源（我们亲爱的用户）进行 CRUD（增删改查）。使用上述技术将为构建更大、更健壮的 API 奠良好的基础。

这是使用 Express 4 创建 Node API 的快速回顾。对于你自己的 API，还有很多可以做的事。你可以添加身份验证、创建更好的错误消息，并添加不同的模块，而不仅仅局限于用户。




我们将使用此 API 作为即将构建的 Angular 应用程序的数据后端。接下来，让我们如何使用基于令牌的身份验证对此 API 进行认证，然后我们将学习 AngularJS。

# Node 身份验证

在本章中，我们将为应用程序实现良好的身份验证基础。需要注意的是，实现身份验证有多种方法，这些方法将取决于你正在构建的应用程序类型、谁将访问你的数据以及许多其他因素。

然而，尽管实现身份验证的方法有很多，但有一个被广泛使用的基础，那就是基于令牌的身份验证（token based authentication）。从一开始为我们的应用程序使用这种身份验证，可以确保无论它如何增长，都能受到保护。

令牌的主要优势是：

*   无状态且可扩展的服务器
*   适用于移动应用程序
*   可以将身份验证传递给其他应用程序（例如通过 Facebook 第三方应用程序使用 OAuth）
*   与其他验证方法相比安全性更高

让我们简单聊聊身份验证以及我们应该使用基于令牌的身份验证。

## 为什么会有基于令牌的身份验证？

基于令牌的身份验证已应用于我们每天使用的 Web 服务。当某个服务提供 API 来访问数据时，通常使用令牌进行身份验证。以 Facebook 的 API 为例，我们需要先与 Facebook 进行身份验证（第一次使用用户名和密码），然后他们会给我们一个令牌用于后续身份验证。此后在规定时间内的每个请求只需要令牌，而不需要我们的用户名和密码。我们将详细讨论这其中的逻辑，但请记住，许多其他服务（包括 GitHub、Google+ 和 Twitter 在内的许多服务）都使用令牌进行身份验证。

### 基于服务器的身份验证（传统方法）

在讨论为什么出现令牌身份验证之前，让我们先看看以前身份验证标准是如何运作的。

> 由于 HTTP 协议是无状态的，如果我们使用用户名和密码对用户进行身份验证，那么在下次请求时，我们的应用程序将不知道我们是谁。我们必须再次进行身份验证。

让应用程序记住我们是谁的传统方法是将登录信息存储在服务器上。这可以通过会话（session）的几种方式实现，通常在内存中或存储在磁盘上。

以下是基于服务器的身份验证工作流图：

![Server Based Authentication](img/10-node-authentication----tokens-traditional.png)

基于服务器的身份验证

随着 Web、应用程序以及移动应用程序的兴起，这种身份验证方法显示出了问题，特别是在扩展性方面。

### 基于服务器的身份验证的问题

这种身份验证方法出现了几个主要问题。

**会话 (Sessions)**：每当用户进行身份验证时，服务器都需要在服务器某处创建一个记录。这通常在内存中完成，当有很多用户进行身份验证时，服务器的开销就会增加。

**扩展性 (Scalability)**：由于会话存储在内存中，这带来了扩展性问题。当我们的云供应商开始复制服务器来处理应用程序负载时，在会话内存中保留关键信息将限制我们的扩展能力。

**CORS**：由于我们想要扩展应用程序让数据跨多个移动设备使用，我们必须担心跨源资源共享 (`CORS`）。当使用 `AJAX` 调用从另一个域获取资源（移动端到我们的 API 服务器）时，我们可能会遇到禁止请求的问题。

**CSRF**：我们还需要防止跨站请求伪造 (`CSRF`)。用户很容易受到 `CSRF` 攻击，因为他们可能已经在银行网站等地方进行了身份验证，这在访问其他网站时可能会被利用。

有了这些问题（扩展性是主问题），尝试不同的方法是有意义的。

## 基于令牌的身份验证如何工作

基于令牌的身份验证是无状态的。我们不在服务器或会话中存储任何关于用户的信息。

这一概念本身就解决了许多必须在服务器上存储信息的问题。

> 没有会话信息意味着你的应用程序可以根据需要扩展并添加更多机器，而无需担心用户在哪里登录。

虽然这种实现可能有所不同，但其核心如下：

1. 用户使用用户名/密码请求访问
2. 应用程序验证凭据
3. 应用程序向客户端提供经过签名的令牌
4. 客户端存储该令牌并在每次请求时发送它
5. 服务器验证令牌并响应数据

**第一次请求后的每一个请求都需要令牌**。此令牌应该发送在 HTTP 请求头中，以符合无状态 HTTP 请求的理念。我们还需要设置服务器使用 `Access-Control-Allow-Origin: *` 来自所有域的请求。在 `ACAO` 头部中指定 `*` 有趣的地方在于，它不允许请求提供如 HTTP 身份验证、客户端 SSL 证书或 Cookie 等凭据。

这里有一个解释该过程的信息图：

![Token Based Authentication](img/10-node-authentication----tokens-new.png)

基于令牌的身份验证

一旦我们使用信息完成身份验证并获得令牌，我们就可以使用此令牌执行几件事。

我们甚至可以创建一个基于权限的令牌并将其传递给第三方应用程序（例如我们想要使用的新移动应用），它们将能够访问我们的数据——**但仅限于我们通过特定令牌允许的信息**。

### 令牌的优势

#### 无状态且可扩展

令牌存储在客户端。完全无状态，并准备好进行扩展。我们的负载均衡器可以将用户传递到我们的任何服务器上，因为任何地方都没有状态或会话信息。

如果我们为登录的用户保留会话信息，这将要求我们一直让该用户访问登录时的同一台服务器（这被称为会话亲和性）。

这带来了问题，因为某些用户会被强制指向同一台服务器，这会导致流量压力。

不必担心！有了令牌这些问题消失了，因为令牌本身持有该用户的数据。

#### 安全性

每个请求发送的是令牌而不是 Cookie，由于没有发送 Cookie，这有助于防止 `CSRF` 攻击。即使你的特定实现在客户端的 Cookie 中存储令牌，Cookie 也仅仅是存储机制而不是身份验证机制。由于我们没有会话，因此没有可以操纵的会话信息！

令牌在一段时间后也会过期，因此你会被要求重新登录。这有助于我们保持安全。

#### 可扩展性（好友的好友和权限）

令牌允许我们构建与其他应用程序共享权限的应用程序。例如，我们将随机的社交账户链接到 Facebook 或 Twitter 等主账户。

当我们通过某个服务（比如 Buffer）登录 Twitter 时，我们正在允许 Buffer 向我们的 Twitter 流中发布内容。

通过使用令牌，这就是我们向第三方应用程序提供选择性权限的方法。我们甚至可以构建自己的 API，如果用户想要将数据访问权限授予另一个应用程序，我们可以发放特殊的权限令牌。

#### 多平台和多域

我们之前稍微讨论过 `CORS`。当我们的应用程序和服务扩展时，我们需要为各种设备和应用程序提供访问（因为我们的应用程序肯定会变得受欢迎！）。





让我们的 API 仅提供数据，我们也可以选择从 CDN 密送资源。这消除了 CORS 带来的问题。`只要用户拥有有效的令牌`，我们的数据和资源就是可用的。

## 基于标准

在创建令牌时，我们将使用基于标准的 [JSON Web Tokens](http://jwt.io/)。这个由 [Auth0](https://auth0.com/) 创建的方便实用的调试器和库图展示了对 JSON Web Tokens 的支持。你可以看到它在各种语言中都得到了大量的支持。这意味着，如果你将来选择更改后端编程语言，实际上可以切换你的身份验证机制！

现在我们已经为基于令牌的认证建立了良好的基础，让我们通过检查实现方法来更进一步实现它。

### JSON Web Tokens

JSON Web Tokens (JWT)，读音为“jot”，是一种标准，因为它们携带的信息是通过 JSON 传输的。我们可以在这里了解更多关于[草案](http://self-issued.info/docs/draft-ietf-oauth-json-web-token.html)的内容，但那个解释看起来并不美观。

`JSON Web Tokens 跨不同的编程语言`：JWT 适用于 .NET、Python、Node.js、Java、PHP、Ruby、Go、JavaScript 和 Haskell。所以你可以看到这些可以用于许多不同的场景。

`JWTs 是自包含的`：它们内部会携带所有必要的信息。这意味着 JWT 能够传输关于它自身的的基本信息、负载（通常是用户信息）和签名。

`JWTs 可以很容易地传递`：由于 JWT 是自包含的，它们在验证 API 时非常适合用在 HTTP 请求头中。你也可以通过通过 URL 传递它。

### JWT 看起来是什么样的？

JWT 很容易识别。它是由三个由 `.` 分隔的字符串。

例如：

```
1 aaaaaaaaaa.bbbbbbbbbbb.cccccccccccc
```

让我们拆解这 3 部分并看看每个部分包含什么。

### 析 JSON Web Token

由于有 3 部分由 `.` 分隔，因此每个部分的创建方式都不同。我们拥有的 3 个部分分别是：

*   header（头部）
*   payload（负载）
*   signature（签名）

![JSON Web Token Overview](img/10-node-authentication----jwt-overview.png)

JSON Web Token 概述

#### Header（头部）

头部携带 2 个部分：

*   声明类型，即 JWT
*   要使用的哈希算法（在本例中为 HMAC SHA256）

这是一个示例：

```
1 {
2   "typ": "JWT",
3   "alg": "HS256"
4 }
```

现在一旦对其进行 `base64encode`，我们就得到了 JSON web token 的第一部分！

```
1 eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9
```

#### Payload（负载）

负载将携带我们 JWT 的大部分内容，称为 [JWT Claims](http://self-issued.info/docs/draft-ietf-oauth-json-web-token.html#RegisteredClaimName)。在这里，我们将放置想要传输的信息以及关于我们令牌的其他信息。

我们可以提供多个声明（claims）。这包括注册声明名称、公共声明名称和私有声明名称。

##### Registered Claims（注册声明）

这些是不是强制性的但其名称已为我们保留的声明。这些包括：

*   `iss`：令牌的发布者
*   `sub`：令牌的主体
*   `aud`：令牌的受众
*   `exp`：这可能是最常用的注册声明。它将以 NumericDate 值的值定义过期时间。过期时间必须在当前日期/时间之前。
*   `nbf`：定义了在此时间之前 JWT 不得被接受处理
*   `iat`：JWT 的发布时间。可以用于确定 JWT 的年龄
*   `jti`：JWT 的唯一标识符。可以用于防止 JWT 被重放。这对于一次性使用的令牌很有帮助。

##### Public Claims（公共声明）

这些是我们自己创建的声明，例如用户名、信息和其他重要信息。

##### Private Claims（私有声明）

生产者和消费者可能同意使用私有的声明名称。这些可能会发生冲突，因此使用时要谨慎。

##### Example Payload（示例负载）

我们的示例负载包含两个注册声明（`iss` 和 `exp`）和两个公共声明（`name` 和 `admin`）。

```
1 {
2   "iss": "scotch.io",
3   "exp": 1300819380,
4   "name": "Chris Sevilleja",
5   "admin": true
6 }
```

这将被编码为：

```
1 eyJpc3MiOiJzY290Y2guaW8iLCJleHAiOjEzMDA4MTkzODAsIm5hbWUiOiJDaHJpcyBTZXZpbGxlamEi\
2 LCJhZG1pbiI6dHJ1ZX0
```

那就是我们 JSON Web Token 的第二部分。

#### Signature（签名）

JSON Web Token 的第三也是最后一部分是签名。该签名由以下组件的哈希值组成：

*   header
*   payload
*   secret

令牌在每次请求时发送，因此没有 CSRF 攻击。没有可以操纵的基于会话的信息，因为，我们没有会话！

我们是这样获取 JWT 的第三部分的：

```
1 var headerHeaderPayload = header + "." + payload;
2 var signature = hmacSHA256(headerPayloadSignature, secret);
3 var jwt = headerPayloadSignature + "." + signature;
```




```
1 var superSecret = 'ilovescotchscotchyscotchscotch';
```

既然所需的包已经就绪，密钥也已准备好，让我们进入用户身份验证阶段。

## 创建示例用户

首先，我们需要确保我们确实有用户可以进行验证，因为在上一章的末尾，我们删除了所有用户。让我们使用在 API 中创建的 `POST http://localhost:8080/api/users` 路由来创建一个用户，并将其添加到数据库中。

我们将发送一个带有以下信息的 `POST` 请求：

**姓名** Chris **用户名** chris **密码** supersecret

![创建示例用户](img/10-node-authentication----create-user.jpg)

创建示例用户

由于目前还没有身份验证机制，用户会被成功创建。现在我们已经有了用户，让我们为他创建一个身份验证机制，让他登录并获取令牌。

## 身份验证用户并发放令牌

我们将在 API 路由内部创建一个名为 `POST http://localhost/api/authenticate` 的新路由。用户将在这里发送带有用户名和密码的 `POST` 请求。如果这两者都通过了，他们将收到一个令牌，以便访问我们 API 的信息。

路由创建的顺序在这里很重要。我们不希望这个 `authenticate` 路由受到我们身份验证中间件的保护，因此它将**被放置在第 9 章创建的中间件之前**。以下是它的位置展示：

```
 1 // 首页的基本路由
 2 app.get('/', ...
 3 
 4 // 获取 express 路由器的实例
 5 var apiRouter = express.Router();
 6 
 7 // 用户验证路由
 8 apiRouter.post('/authenticate', ...
 9 
10 // 所有请求使用的中间件
11 apiRouter.use(function(req, res, next) ...
12 
13 // 其他 api 路由。加密的路由
14 apiRouter.get('/', ...
```

在 `apiRouter.post('/authenticate', ...` 路由内部，我们将创建 JSON Web Token (JWT) 并将其返回给用户。

让我们创建验证用户的路由。我们将：

* 检查是否存在该用户名的用户
* 检查用户密码是否正确（通过将其与数据库中保存的哈希密码进行比较）
* 如果一切无误，则创建一个令牌

```
 1 // 验证用户的路由 (POST http://localhost:8080/api/authenticate)
 2 apiRouter.post('/authenticate', function(req, res) {
 3 
 4   // 查找用户
 5   // 显式选择姓名、用户名和密码
 6   User.findOne({
 7     username: req.body.username
 8   }).select('name username password').exec(function(err, user) {
 9 
10     if (err) throw err;
11 
12     // 未找到该用户名的用户
13     if (!user) {
14       res.json({ 
15         success: false, 
16         message: '身份验证失败。未找到用户.' 
17       });
18     } else if (user) {
19 
20       // 检查密码是否匹配
21       var validPassword = user.comparePassword(req.body.password);
22       if (!validPassword) {
23         res.json({ 
24           success: false, 
25           message: '身份验证失败。密码错误.' 
26         });
27       } else {
28 
29         // 如果找到了用户且密码正确
30         // 创建令牌
31         var token = jwt.sign({
32           name: user.name,
33           username: user.username
34         }, superSecret, {
35           expiresInMinutes: 1440 // 24 小时后过期
36         });
37 
38         // 将包含令牌的信息作为 JSON 返回
39         res.json({
40           success: true,
41           message: '请使用你的令牌!',
42           token: token
43         });
44       }   
45 
46     }
47 
48   });
49 });
```

该路由完成了我们需要它执行的主要工作：**检查是否存在该用户名的用户**，使用我们在第 9 章的 User 模型中创建的 `comparePassword` 方法**确保密码正确**，以及**创建一个令牌**。

我们正在使用 `jwt` (jsonwebtoken) 包来签名令牌。当我们传入有效负载（在本例中是我们的用户）时，该包会自动生成我们 JWT 的头部和签名。

现在，当我们使用之前使用的凭据通过向 `http://localhost:8080/api/authenticate` 发送 `POST` 请求，结合创建用户的信息（chris/supersecret）来验证用户时，我们将获得令牌！

![身份验证用户并获取令牌](img/10-node-authentication----authenticate-user.jpg)

身份验证用户并获取令牌

我们还可以用错误的用户名测试我们的身份验证路由：

![验证错误的用户名](img/10-node-authentication----authenticate-wrong-user.jpg)

验证错误的用户名

这里是错误密码的情况：

![验证密码](img/10-node-authentication----wrong-password.jpg)

验证密码

## 测试我们的路由中间件

现在我们已经构建了负责保护后续路由的中间件，让我们测试一下刚刚创建的内容，以确保它工作正常。

以下是在不传递任何身份验证信息的情况下尝试访问主 API 路由的操作：

![未提供令牌](img/10-node-authentication----unauthenticated.jpg)

未提供令牌





![Token Passed Through HTTP Header](img/10-node-authentication----token-header.jpg)

# 通过 HTTP Header 传递 Token

我们也可以像下面这样将 token 作为 URL 参数传递：`http://localhost:8080/api/users?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJwYXNzd29yZCI6IiQyYSQxMCRyZ3JhdXB6c0RaGJJZNzdDUVNJbkh1WjkwUld2cS9OV3NpMGtPdWVlUGV0cVVCoyLmpLYSIsInVzZXJuYW1lIjoiY2hyaXMiLCJuYW1lIjoiQ2hyaXMiLCJfaWQiOiI1NDgxZTI2ZTkzYjliYmE3MTcxYmZkNWUiLCJfX3YiOjB9.fKBuDM0J1jpiAKfkPpr_b_NS6io8U4srLGuvEAfRhJg`

![Token Passed Through URL Parameter](img/10-node-authentication----token-url.jpg)

# 通过 URL 参数传递 Token

## 获取用户信息的路由

让我们快速为我们的 API 增加一个路由，以便我们能够返回用户信息。

我们将调用此端点（`GET http://localhost:8080/api/me`），这将允许我们获取有关登录用户的信息。

在所有其他 `apiRouter` 路由之后，让我们定义以下内容：

```
1 // 获取用户信息的 API 端点
2 apiRouter.get('/me', function(req, res) {
3   res.send(req.decoded);
4 });
```

记住在我们的中间件中，我们把登录用户存储在 `req.decoded` 中以供其他路由使用。现在我们只需获取该信息并将其返回。我们将在未来的 Angular 章节中看到这有多有用，比如当我们想在消息中显示登录用户的用户名时（类似于 `Hello Chris` 这样的内容！）。

## 帮助身份验证的模块

现在我们已经从零开始构建了这一切，但重要的是，市上有许多 Node 模块可以帮助我们处理身份验证。通过自己构建安全机制来理解基础知识是好的，但使用由团队构建并确保安全性稳固的模块也会很有帮助。

对于在 Node 中处理身份验证，你找不到比 [PassportJS](http://passportjs.org/) 更好的包了。它允许我们在服务器上集成基于会话的安全性、基于社交的身份验证，以及我们在在本章中所做的 JWT 安全性。

甚至有一个包专门用于处理检查 JWT 和保护路由的包，叫做 [express-jwt](https://github.com/auth0/express-jwt)。这个包为我们创建了中间件，这样我们就不需要自己写。它允许我们设置受保护和未受保护的路由。

## 总结

现在我们有一个带有 token 身份验证的 API 了！就像 Facebook、Google、Twitter 和 GitHub 等大公司一样！其实并不完全像它们，因为它们实现了更多功能，如用户特定权限、组权限以及许多其他高级功能，但这是基础。

记住，安全是我们应用程序中非常重要的部分，保护用户信息应该是重中之重。请记住，这只是安全的开始，安全一直在不断演进，以防御新的和旧的攻击。

这个 API 将用于将数据传递给我们的前端 AngularJS 。通过这样做，我们再次遵循了这样一个理念：我们的后端和前端都是分离的，但又协作工作以创建出的体验。

## 开始 Angular

让我们后退一步。到目前为止，我们已经完成了构建一个出色的后端服务端服务的构建。我们学习了如何创建 RESTful API，如何使用 `MongoDB` 处理 CRUD 操作，并熟练掌握了 `Node`。

现在我们必须处理硬币的另一面：前端。我们必须熟悉 Angular 应用程序、它们是如何设置的，以及我们将如何访问我们所构建的 Node API 和数据。

### JavaScript 应用程序的状态

如果你以前在没有框架的情况下构建过 JavaScript 应用程序（让我们以 jQuery 为例），很多时候你使用 `$('#divname').html()` 或 `$('#divname').append(variable)` 在你的应用程序中获取并放置数据。这会导致问题，因为没有一个真正的数据源。你忙于在各处到处地获取和放置数字和元素，有时你并不完全确定哪条数据是最新且最有效的。

在 MVC 中，真正的数据源来自模型（model），由控制器（controller）辅助传递视图（view）。这意味着获取数据有一套稳固的工作流。视图的构建只是为了显示数据并尽可能不包含逻辑。模型和控制器才是真正需要处理数据的地方。

Angular 通过将前端应用程序处理得更像我们熟悉的后端应用程序来帮助解决这些问题。我们喜欢数据来自一个一致的地方并被注入到视图中。这让我们保持理智，因为我们应用程序的每个部分都有一个真实的（唯一的）数据源。

### 介绍

Angular 自称为“如果 HTML 设计之是为了构建 Web 应用，那么它本该是什么样”。它允许你作为开发者为应用程序的前端构建 MVC（模型-视图-控制器）架构。由于客户端应用程序正变得不仅仅显示静态 HTML 页面，需要构建新的工具来适应日益增长的 JavaScript 应用程序。

Angular 允许你扩展 HTML，因此你是在已经熟悉的标准进行构建，而不是从零学习整个框架。

### 重要的 Angular 概念

Angular 中一些将贯穿我们构建的所有内容的优秀概念是数据绑定、依赖注入和指令。

#### 数据绑定

[数据绑定](https://docs.angularjs.org/guide/databinding) 允许我们有一个集中的数据源。我们将经常讨论单一数据源。忘记使用 jQuery 的 `append`、`val`、`html` 或其他任何方法将数据注入你的视图中。我们将使用 Angular 奇的数据绑定来为我们处理所有这些。

让我们想象这样一个场景：你在控制器中创建了一个变量。然后你在视图中显示该变量。如果你在控制器中更改了变量，它会在视图中自动更改，而不需要你在那里注入（Angular 通过绑定两个地方的变量为你完成注入）。

Angular 文档对此功能提供了很好的解释：“编译步骤产生了一个活动视图。视图的任何更改都会反映在模型中，模型中的任何更改都会传播到视图。模型是应用程序状态的单一事实来源，大大简化了开发者的编程模型。”

#### 依赖注入

Angular 应用程序是许多不同模块的集合，例如处理数据传递到视图的控制器、与 API 交互的服务（视为模型）、帮助我们进一步操作视图的指令，等等。在我们构建应用程序时，我们将采用模块化方法，因为这让我们能够构建可测试、模块化且可扩展的应用程序。

我们构建的每个模块将被注入到我们的主应用程序模块中以创建最终产品。我们的主应用程序将继承我们注入的模块的依赖项。

#### 指令





[指令（Directives）](https://docs.angularjs.org/guide/directive) 是 Angular 内置的，你会频繁使用它们。它们是我们扩展 HTML 模板的方式，告诉 Angular 在何以及何时对我们的视图应用功能。指令会让 Angular 知道某些 HTML 元素应该绑定到我们定义的 Angular 变量或函数。它们还可以帮助 Angular 操作我们的 DOM。

> jQuery 告诉我们如何抓取并注入 DOM。Angular 告诉我们如何操作数据，从而改变 DOM。

让我们开始构建应用程序，并在在此过程中讨论更多概念。

## 设置 Angular 应用

这个演示目前还没有从我们的 Node API 获取任何动态数据。我们将数据直接硬编码在 Angular 控制器（controllers）中。这将让我们先熟悉 Angular 的特定功能。

这是我们 Angular 应用的文件结构。请注意，我们不需要像 Node 应用那样的 `package.json` 或 `server.js` 文件。这是一个纯的前端应用程序，只包含 HTML/CSS/JS！

* `js/`
    * `app.js`
* `index.html`

非常简单！2 个文件就能为我们的第一个 Angular 应用提供所需的一切。

我们希望通过这个应用程序实现的目标是：

1. 设置一个 Angular 前端应用
2. 将来自 Angular 控制器的数据（消息和列表）显示在视图中
3. 通过输入框更新消息来展示数据绑定

### 创建你的 Angular 应用 (app.js)

我们将从创建应用程序的主模块（module）开始。进入 `app.js` 文件，看看 Angular 模块是如何创建的：

```
 1 // 命名我们的 angular 应用
 2 angular.module('firstApp', [])
 3 
 4 .controller('mainController', function() {
 5 
 6     // 将此绑定到 vm (视图模型)
 7     var vm = this;
 8 
 9     // 在这里定义变量和对象
10     // 这允许它们在视图可用
11 
12     // 定义一个基础变量
13     vm.message = 'Hey there! Come and see how good I look!';
14 
15     // 定义一个项目列表
16     vm.computers = [
17         { name: 'Macbook Pro', color: 'Silver', nerdness: 7 },
18         { name: 'Yoga 2 Pro', color: 'Gray', nerdness: 6 },
19         { name: 'Chromebook', color: 'Black', nerdness: 5 }
20     ];
21 
22 }); 
```

你可以看到，Angular 模块只需要声明 `angular.module`。然后我们可以向此模块添加一个控制器。在构建这些应用程序时，我们将尝试每个应用只保留一个功能。这意味着我们不会将控制器和服务混合在同一个模块中。这回到了模块化应用程序的思想。

到目前为止，我们已经：

* 创建了名为 `firstApp` 的主模块
* 创建了名为 `mainController` 的控制器
* 控制器中的信息将通过 `vm` 绑定到自身
* 创建了一个名为 `message` 的变量
* 创建了一个名为 `computers` 的项目列表

注意我们如何在 `vm` 上定义变量和列表的。将父级 `this` 绑定到 `vm` 是一个好习惯。这在引用控制器时很有帮助，因为 `this` 可以在 JavaScript 回调中使用。控制器上有有属性，这就是我们能够通过 `controller as` 语法在视图中使用它们。我们很快就会看到它是如何工作的。就是这样！你刚刚创建了你的 Angular 应用！现在它还没做什么，让我们通过创建 HTML 文件并对其应用此模块来让它变漂亮。

字体 应用 Angular 应用 (index.html)

让我们开始构建基础 HTML 站点。我们将通过 CDN 引入 Bootstrap 和 Angular 以保持简单。这里是 `index.html` 的开头：

```
 1 <!DOCTYPE html>
 2 <html lang="en">
 3 <head>
 4     <meta charset="UTF-8">
 5     <title>My First Application</title>
 6 
 7     <!-- CSS -->
 8     <!-- 加载 bootstrap 和我们的样式表 -->
 9     <link rel="stylesheet" href="http://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.css">
11     <style>
12         body { padding-top:50px; }
13     </style>
14 
15     <!-- JS -->
16     <!-- 加载 angular 和我们的自定义应用 -->
17     <script src="http://ajax.googleapis.com/ajax/libs/angularjs/1.3.8/angular.min.js"></script>
19     <script src="js/app.js"></script>
20 </head>
21 <body class="container">
22 
23 </body>
24 </html
```

`index.html` 文件现在是空壳。我们加载了 Bootstrap，添加了一点用于间距的 CSS，并加载了 Angular 本身以及自定义的 `app.js`。如果我们现在在浏览器中查看，什么都不会发生，因为我们还没有应用创建的 Angular 应用。我们讨论过 Angular 指令，这将是你第一次使用它们。Angular 提供指令将你的应用应用到 HTML 中。这些被称为 `ng-app` 和 `ng-controller`。让我们在 `<body>` 标签上添加：

```
 1 <!-- 声明我们的应用 -->
 2 <body class="container" ng-app="firstApp" ng-controller="mainController as main">
```

现在我们应用了控制器并将其命名为 `main`。我们讨论过 Angular 指令，这些可以将你的应用应用到 HTML 中。让我们在 `<body>` 标签内添加内容：

```html
 1 <div class="jumbotron">
 2 
 3 <!-- 显示消息 -->
 4   <h2>This is my message:</h2>
 5   {{ main.message }}
 6 
7 </div>
```

现在我们在浏览器中看到了消息！注意我们是如何在控制器中定义这个变量的。

![消息变量](img/11-angular-start-variable.jpg)

### 消息变量

你刚刚在视图中显示了第一个变量！现在让我们处理列表。这将使用另一个名为 `ng-repeat` 的 Angular 指令。你将在视图中频繁使用它因为它类似于 `foreach`。

在消息部分下方添加：

```
 1 <!-- 使用 ng-repeat 显示列表 -->
 2 <h2>This is my list:</h2>
 3 <table class="table-bordered">
 4     <thead>
 5         <tr>
 6             <td>名称</td>
 7             <td>颜色</td>
 8             <td>极客程度</td>
 9         </tr>
 10     </thead>
 11     <tbody>
 12         <tr ng-repeat="computer in main.computers">
 13             <td>{{ computer.name }}</td>
 14             <td>{{ computer.color }}</td>
 15             <td>{{ computer.nerdness }}</td>
 16         </tr>
 17     </tbody>
 18 </table>
```

很酷对吧？Angular 将知道要遍历 computers 并在每一项显示在它自己的表格行中。

![显示列表](img/11-angular-start-list.png)

### 显示列表

我们还要为这个演示做最后一件事。这是让我们看到数据绑定生效的魔法部分。

我们将在站点上放置一个输入字段，并使用另一个（发现趋势了吗？）被称为 `ng-model` 的 Angular 指令将输入绑定到变量上。这将立即更改消息。你将亲眼看到变化的发生！让我们在消息部分上方添加输入框：

```
 1 <!-- 使用 ng-model 更新消息变量的表单 -->
 2 <div class="form-group">
 3     <label>Message</label>
 4     <input type="text" class="form-control" ng-model="main.message">
 5 </div>
```




现在在浏览器中查看该站点并开始在输入框中输入。得益于 Angular 及其 `directives`（指令）的魔法，`message` 变量会立即发生。

![数据绑定](img/11-angular-start----angular-data-binding-example.jpg)

数据绑定

这里有一个 [CodePen](http://codepen.io/sevilayha/full/DhLqk/)，让你可以快速看到这些操作演示。完整代码也可以在本书的代码仓库中找到。

***

![Tip](img/icon-heart.png "专业提示")

提示

### $scope vs. this

在网络上的其他 Angular 教程中，你可能见过 `$scope` 是一种将信息从控制器（controller）绑定到视图的方法。从 Angular 1.3 开始，这种方法仍然存在，但建议使用 `controller as` 语法。

这种方法有很多益处，因为它能保持我们的代码更加整洁、更有组织。在视图中，我们甚至可以更容易地看到控制器是如何被使用的。

以下是 `使用 $scope` 和 `不使用 $scope` 的两个快速对比。

```
1 <!-- 使用 $scope -->
2 <div ng-app="myApp" ng-controller="mainController">
3     <p>{{ myVariable }}</p>
4 </div>
5 
6 <!-- 不使用 $scope - 使用 controller as -->
7 <div ng-app="myApp" ng-controller="mainController as main">
8     <p>{{ main.myVariable }}</p>
9 </div>
```

这有很多益处，特别是当我们开始嵌套控制器时。更容易看出哪些变量和函数存在于每个控制器中。

这样做的好处是它将强迫你为新的 Angular 2.0 语法做准备，该版本预计在大一年后发布。Angular 团队已经宣布`$scope` 将被淘汰，转而采用更接近 `controller as` 的语法。

不过，不用担心 Angular 2.0。如果你现在使用这种语法构建 Angular 应用程序，迁移到新版本将不会痛苦。

***

### 创建和处理表单

现在让我们进入更高级的内容。我们通常希望在网站上有一个表单，而 Angular 让处理表单变得极其简单。让我们创建一个可以将计算机添加到我们的计算机列表中的表单。

这将在两个不同的部分完成：

1. 创建一个 Angular 函数来处理表单并将其添加到我们的列表
2. 添加 HTML 表单并将其连接起来与 Angular 函数协同工作

#### 处理表单的 Angular 函数

让我们将这个 Angular 函数添加到我们的控制器中。

```
 1 // 命名我们的 angular 应用
 2 angular.module('firstApp', [])
 3 
4 .controller('mainController', function() {
 5 
6     ...
 7 
8     // 来自我们表单的信息
 9     vm.computerData = {};
10 
11     vm.addComputer = function() {
12         
13         // 将计算机添加到列表
14         vm.computers.push({
15             name: vm.computerData.name,
16             color: vm.computerData.color,
17             nerdness: vm.computerData.nerdness
18         });
19 
20         // 在添加计算机后，清空表单
21         vm.computerData = {};
22     };
23 
24 }); 
```

我们将创建一个对象来存放表单数据，称为 `vm.computerData`。这一步并不是必要的，因为 Angular 会在需要时自动创建它，但为了清晰，我们会定义它。

我们还创建一个函数，从 `vm.computerData` 中提取信息并将其推入我们的计算机数组。当添加时，它应该会自动将计算机添加到表格中，而无需刷新页面（几乎像魔法）。

计算机添加到列表后，我们将通过清空包含数据的对象来清空表单。在 jQuery 应用程序中，清空表单可以通过以下实现：

`$('input').val('');`

在 Angular 中不行！我们现在熟悉 `data-binding`（数据绑定）了，由于我们在 Angular 侧清空了对象，这会自动清空视图侧的表单。

如此，让我们创建 HTML 表单并将其连接到我们刚刚创建的函数。

#### HTML 表单

在我们的 `index.html` 文件中，计算机 HTML 表格下方，添加以下表单：

```
 1 <!-- 向列表添加计算机的表单 -->
 2 <form class="form-inline" ng-submit="main.addComputer()">
 3     
 4     <input type="text" class="form-control" placeholder="Macbook" ng-model="main\
 5 .computerData.name">
 6     <input type="text" class="form-control" placeholder="Silver" ng-model="main.\
 7 computerData.color">
 8     <input type="number" class="form-control" placeholder="8" ng-model="main.com\
 9 puterData.nerdness">
10 
11     <button type="submit" class="btn btn-success">Add</button>
12 </form>
```

我们这里有 3 个不同的输入和一个提交按钮。我们使用了 `ng-model` 将每个输入绑定到我们在 Angular 控制器中创建的 `computerData` 对象的特定字段。

在这里看到的新 Angular 指令是 `ng-submit`。它用于表单，并告诉 Angular 在提交表单时做什么。这里是我们的表单：

![表单](img/11-angular-start----angular-data-binding-example.jpg)

去填写一些数据并点击 Add。观察你的表格如何自动更新，计算机被添加。

## 总结

本章一次性向你介绍了许多 Angular 概念。它们都是帮助你构建应用程序的工具。数据绑定、依赖注入和指令是 Angular 的基础，你将在每个应用程序中使用它们。

接下来，我们将探索应用程序的路由，以便拥有功能完整的站点。

# Angular 路由

我们将通过一个全新的应用演示 Angular 路由。在开始该新应用之前，让我们先讨论不同的路由技术。

### ngRoute

[ngRoute](https://docs.angularjs.org/api/ngRoute) 是构建 Angular 应用程序时路由的标准模块。它是 Angular 支持的，并通过名为 `$route` 的服务提供路由（我们稍后会展示它是如何工作的）。

### 路由应用程序的 Node 服务器

为了让我们使用 ngRoute，我们希望使用服务器，以便模拟该应用程序在浏览器中的工作方式。我们将启动一个服务器，因为正如你所看到的，我们不能直接打开文件。我们的 Angular 应用程序需要请求视图文件，如果没有服务器，我们将遇到问题。




```
1 - public/    // 我们的所有前端代码 (HTML/CSS/JS) 都放在这里
2 ----- views/
3 ---------- pages/
4 ----- index.html
5 ----- js/
6 - package.json
7 - server.js
```

这些就是我们启动服务器和 Angular 前端应用程序所需的文件。目前，我们将只关注 `package.json` 和 `server.js` 来创建一个服务器。

## 启动 Node 项目

就像我们之前做的那样，`package.json` 将包含包和项目信息。请运行 `npm init` 或直接手动创建该文件。这里有一个基础的 `package.json` 文件。

```
1 {
2   "name": "routing-app",
3   "main": "server.js",
4   "dependencies": {
5     "express": "~4.9.1"
6   }
7 }
```

一旦你有了该 `package.json` 文件，运行 `npm install` 将你的依赖项（在此例中为 Express）获取到 `node_modules` 文件夹中。记住，你也可以通过命令行使用 `npm install express --save` 来添加依赖项。

## 设置 Express 服务器

正如我们之前所做的，我们的服务器将在 `server.js` 中设置。让我们创建一个非常简单的服务器，向用户发送 `index.html`。

```
 1 // 获取我们需要的资源
 2 var express = require('express');
 3 var app     = express();
 4 var path = require('path');
 5 
6 // 设置 public 文件夹以提供公共资源
 7 app.use(express.static(__dirname + '/public'));
 8 
9 // 设置到 index.html 文件的路由
10 app.get('*', function(req, res) {
11     res.sendFile(path.join(__dirname + '/public/views/index.html'));
12 });
13 
14 // 在端口 8080 启动服务器 (http://localhost:8080)
15 app.listen(8080);
16 console.log('Magic happens on port 8080.');
```

当请求进入我们的服务器时（我们通过使用 `*` 通配符方法来实现），我们将向用户发送 `index.html` 文件，该文件包含了我们所有的 Angular/HTML/CSS 代码。我们还使用 Express 通过 `app.use(express.static())` 为静态资源设置目录。这意味着每当我们的客户端请求 CSS 文件、图像或 JS 文件时，Node 都会通过查看 `public` 文件夹来提供该资源。我们所有的前端代码都存储在这个 `public` 文件夹中，因此这对我们的项目是一个很好的设置。

创建一个快速的 `public/views/index.html` 文件并在其中编写任何你想写的内容。使用以下命令启动服务器：

`nodemon server.js`

现在我们可以在浏览器中访问 `http://localhost:8080` 我们的应用程序。

这就是 Node 的酷之处。即使你没有在最终项目中使用它，你也可以将其作为你想要构建的任何项目的服务器。在我们开发 Angular 应用程序时，我们只需要在这个 URL 中工作即可。

现在我们已经准备好了构建 Angular 路由应用程序的基础，让我们开始着吧。

## 示例应用程序

我们将仅仅创建一个包含首页、关于页和联系页的简单网站。Angular 是为了比这高级得多的应用程序而构建的，但本教程将展示那些更大型项目所需的许多概念。

### 目标

* 单页应用
* 页面切换时不刷新页面
* 每个页面显示不同的数据

### 文件结构

这些将存于我们在上一步中设置的 `public` 文件夹中的文件。

```
 1 public/
 2 - views/
 3 ----- pages/        // 将注入到主布局的页面
 4 ---------- home.html
 5 ---------- about.html
 6 ---------- contact.html
 7 ----- index.html        // 主布局
 8 - js/
 9 ----- app.js        // 存储所有的 Angular 代码
10 ----- app.routes.js // 存储所有的 Angular 路由
```

## 应用的 HTML

这是简单的部分。我们使用 [Bootstrap](http://getbootstrap.com) 和 [Font Awesome](http://fontawesome.io) 来让样式变得更简单。打开你的 `index.html` 文件，我们将添加一个带有导航栏的简单布局。

```
 1 <!DOCTYPE html>
 2 <html>
 3 <head>
 4     <meta charset="utf-8">
 5     <title>我的路由应用!</title>
 6 
 7     <!-- 为 angular 路由设置基础路径 -->
 8     <base href="/">
 9 
10     <!-- CSS -->
11     <!-- 通过 CDN 加载 bootstrap 和 fontawesome -->
12     <link rel="stylesheet" href="http://netdna.bootstrapcdn.com/bootstrap/3.0.0/\
13 css/bootstrap.min.css">
14     <link rel="stylesheet" href="http://netdna.bootstrapcdn.com/font-awesome/4.0\
15 .0/css/font-awesome.css">
16     <style>
 17         body { padding-top:50px; }
 18     </style>
 19 
20     <!-- JS -->
21     <!-- 通过 CDN 加载 angular 和 fontawesome -->
22     <script src="http://netdna.bootstrapcdn.com/angularjs/1.4.6/\
23 angular.min.js"></script>
24     <script src="http://netdna.bootstrapcdn.com/font-awesome/4.0\
25 .0/js/font-awesome.min.js"></script>
 26 
27     <!-- 加载自定义脚本 -->
28     <script src="js/app.js"></script>
29     <script src="js/app.routes.js"></script>
30 </head>
31 <body class="container" ng-app="routerApp">
32 
33   <!-- 头部和导航栏 -->
34   <nav class="navbar navbar-default">
35       <div class="container-fluid">
36         <a class="navbar-brand" href="#">Angular 路由</a>
37       </div>
 38 
39       <ul class="nav navbar-right">
40         <li><a href="/"><i class="fa fa-home"></i> 首页</a></li>->
41         <li><a href="/about"><i class="fa fa-shield"></i> 关于</a></li>->
42         <li><a href="/contact"><i class="fa fa-comment"></i> 联系</a></li>->
43       </ul>

44     </nav>
45   </header>
46 
47   <!-- 主内容和注入的视图 -->
48   <main>
49 
50     <!-- 内容在此处 -->
51   </main>
52 </body>
53 </html>
```
*(注：由于原文 HTML 示例中存在微小的标签闭合错误，如重复的 `</li>`，翻译时保持了其逻辑结构以确保一致性。)*

我们从 Google 加载 Angular 和 Route。单独加载模块很重要，因为我们将将其注入到应用程序。这是依赖注入的另一个示例。

![Angular Foundation](img/12-angular-routing)

## Angular 应用程序

### 模块和控制器

接下来，我们必须创建应用程序。关于每个部分的更多信息请查阅文档。我们将在 `app.js` 中创建它：

```
1 angular.module('routerApp', [])
2 
3 // 创建控制器
4 // 将是整个网站的控制器
5 .controller('mainController', function() {
6 
7   var vm = this;
8 
9   // 在视图中显示 bigMessage 变量
10   vm.bigMessage = '风平浪静造就不了熟练的水手。';
11 })
12 
13 // 首页特定控制器
14 .controller('homeController', function() {
15 
16   var vm = this;
17 
18   vm.message = '这是首页！';
19 })
20 
21 // 关于页控制器
22 .controller('aboutController', function() {
23 
24   var vm = this;
25 
26   vm.message = '看！我是关于页。';
27 })
28 
29 // 联系页控制器
30 .controller('contactController', function() {
31 
32   var vm = this;
33 
34   vm.message = '联系我们！开玩笑的。这只是一个演示。';
35 });
```

让我们将模块和控制器添加到 HTML 中，这样 Angular 就知道如何引导/初始化我们的应用程序。为了测试一切是否正常工作，我们还将显示我们创建的 `vm.bigMessage` 变量。

#### 应用 Angular




让我们回到 `index.html`，并使用 `ng-app` 和 `ng-controller` 应用我们的应用和控制器。由于我们已经在文档的 `<head>` 中加载了 `app.js` 文件，我们将它们都应用到 `<body>` 标签上。

```
1 <body class="container" ng-app="routerApp" ng-controller="mainController as main\
2 ">
```

再次注意，当我们编写 `mainController as main` 时，我们使用的是 `controller as` 语法。我们还将在网站的 `<main>` 区域展示我们的 `bigMessage`：

```
1 <main>
2     <div class="jumbotron">
3         <h1>{{ main.bigMessage }}</h1>
4     </div>
5 
6     <!-- angular templating will go here -->
7     <!-- this is where content will be injected -->
8 </main>
```

现在，如果在浏览器中显示 `index.html` 文件，我们应该看到我们的消息。

![Angular 路由消息显示](img/12-angular-routing----angular-routing-message.jpg)

Angular 路由消息显示

在我们的 `<main>` 内部，现在我们将看到我们创建的消息。由于我们已经设置好了模块和控制器，并且 JavaScript 控制台中没有错误，我们知道 Angular 正在正常工作。现在，我们将开始尝试使用此布局来显示不同的页面，而无需刷新页面。

### 将页面注入到主布局中

`ng-view` 是一个 Angular 指令，它将当前路由（`/home`、`/about` 或 `/contact`）的模板包含在主布局文件中。

**它是如何工作的？** Angular 路由（`ngRoute`）会查看当前 URL，然后将该 URL 与我们指定的视图进行匹配。因此，如果我们处于 `/about` 页面，我们将告诉 `ngRoute` 获取一个特定的视图文件（在本例中为 `pages/about.html`）并将其注入到我们放置 `ng-view` 的地方。

我们还没有设置所需的路由规则，所以现在就向模板中添加 `ng-view`，然后继续进行路由部分。

在我们网站的 `<main>` 区域内，删除消息部分并添加以下内容：

```
1 <main>
2 
3     <!-- angular templating -->
4     <!-- this is where content will be injected -->
5 
6     <div ng-view></div>
7 
8 </main>
```

### 配置路由

现在这对我们的网站还没有什么太大的作用。我们必须定义路由以及每个路由将使用的视图。这就是我们如何使用 Angular 的路由功能，以便我们的页面不发生刷新。

Angular 路由模块为我们提供了 `$routeProvider`(http://docs.angularjs.org/api/ngRoute.$routeProvider) 服务，我们将通过它来配置路由。路由在 `$routeProvider` 对象上使用 `.when()` 定义。

现在让我们通过创建一个新文件 `public/js/app.routes.js` 来创建我们的路由。我们还将之前之前创建的每个控制器应用到每个页面。

```
 1 // 为我们所有的路由需求注入 ngRoute
 2 angular.module('routerRoutes', ['ngRoute'])
 3 
 4 // 配置我们的路由
 5 .config(function($routeProvider, $locationProvider) {
 6     $routeProvider
 7 
 8         // 首页的路由
 9         .when('/', {
110             templateUrl : 'views/pages/home.html',
 11             controller  : 'homeController',
 12             controllerAs: 'home'
 13         })
 14 
 15         // 关于页面的路由
 16         .when('/about', {
 17             templateUrl : 'views/pages/about.html',
 18             controller  : 'aboutController',
 19             controllerAs: 'about'
 20         })
 21 
 22         // 联系页面的路由
 23         .when('/contact', {
 24             templateUrl : 'views/pages/contact.html',
 25             controller  : 'contactController',
 26             controllerAs: 'contact'
 27         );
 28 
 29     // 设置我们的应用以使用优美的 URL
 30     $locationProvider.html5Mode(true);
 31 });
```

现在我们已经使用 `$routeProvider` 定义了路由。正如配置所示，你可以指定 `route`、使用的 `template file` 甚至一个 `controller`。这样，应用程序的每个部分都将使用它们自己的视图和 Angular 控制器。

我们还可以在这里定义 `controllerAs`，然后每个控制器将自动定义在我们的站点上。例如，在 `home.html` 文件内部，当路由器引入此文件时，控制器将定义为 `homeController as home`。

***

![提示：清理 Angular URL](img/icon-heart.png "专业贴士")

提示：清理 Angular URL

默认情况下，AngularJS 会路由带井号 (# 的 URL。例如，Angular 将会有 `http://example.com/`、`http://example.com/#/about` 和 `http://example.com/#/contact`。

获取清洁的 URL 并从 URL 中删除井号非常简单。

需要完成 2 件事：

1. 配置 `$locationProvider`
2. 在 `<head>` 中设置 `<base>`

在 Angular 中，我们将使用 `$locationProvider.html5Mode(true)` 并在 HTML 中添加 `<base href="/">`。

#### 将路由注入主应用

Angular 开发的核心原则之一是依赖注入。我们将新创建的路由模块注入到 `index.html` 中。

我们将像这样在第一行添加：

`angular.module('routerApp', ['routerRoutes'])`

就像这样，我们现在有了路由！

### 配置视图

现在我们已经有了路由，并且它们正在调用相应的文件。为了完成本教程，我们只需要定义将注入的页面。我们还将让每个页面显示其相应控制器的消息。这是一个简单的过程，只需在每个视图中显示 `{{ home.message }}`、`{{ about.message }}` 和 `{{ contact.message }}` 变量。

`pages/home.html`

```
1 <div class="jumbotron text-center">
2     <h1>Home Page</h1>
3 
4     <p>{{ home.message }}</p>
5 </div>
```

`pages/about.html`

```
1 <div class="jumbotron text-center">
2     <h1>About Page</h1>
3 
4     <p>{{ about.message }}</p>
5 </div>
```

`pages/contact.html`

```
1 <div class="jumbotron text-center">
2     <h1>Contact Page</h1>
3 
4     <p>{{ contact.message }}</p>
5 </div>
```

我们在路由中通过 `controllerAs` 为每个 HTML 文件的变量都加上了控制器名称。

访问您的应用程序并点击页面。你会看到数据发生了变化，你的消息变量也发生了变化，而完全无需刷新页面！**

![Angular 路由首页](img/12-angular-routing----angular-routing-final.jpg)

Angular 路由首页

## 总结

我们搞定了！一个具有 3 个不同页面的单页应用。每个页面还将引入不同的 Angular 控制器，以便数据在我们的站点上可以有所不同。

你可以看到它的价值，因为它让我们的基础网站变成了更像集成应用程序的感觉。



虽然这个网站无需刷新页面即可路由已经很酷了，但我们将通过为页面添加动画让它变得更酷。你可能已经见过点击项目时会滑入和滑出视图的移动应用。我们将刚刚构建的内容变成一个整洁且令人深刻的动画网站（别担心，它不会太花哨的……除非你希望那样）。

***

![注意：ngRoute 的替代方案](img/icon-pencil.png "注意")

#### 注意：ngRoute 的替代方案

虽然 `ngRoute` 是为了与 Angular 配合得最紧密而构建的路由工具，但另一个名为 `UI Router` 的工具是由 AngularUI 团队构建的另一个路由框架。[AngularUI](http://angular-ui.github.io/) 是与 Angular 应用紧密配合的配套套件。它们提供了许多实用的工具，如 `UI Router`、用于在 Angular 中使用 Bootstrap JavaScript 组件的 `UI Bootstrap` 以及其他一些非常棒的工具。

`UI Router` 提供了与 `ngRoute` 不同的方法，它根据应用程序的状态而非仅仅是路由 URL 来更改你的应用程序视图。这意味着你的应用程序没有绑定到 URL 路径，你可以根据应用程序状态（例如，用户是否登录）来调整显示的模板。

拥有嵌套状态的能力也有许多益处。`ngRoute` 不提供此功能，而对于更高级的 UI，拥有嵌套状态是有帮助的，例如拥有多个侧边栏面板以及移动组件，这些在移动应用中会更常见。

我们将我们将使用 `ngRoute` 因为它是标准做法，但如果想阅读关于 `UI Router` 的更多内容，这里有一个很好的入门文章：[使用 UI-Router 进行 AngularJS 路由](http://scotch.io/tutorials/javascript/angular-routing-using-ui-router)。未来，Angular 团队已表示，他们构建的下一个路由模块将包含 `ngRoute` 和 `UI Router` 的功能。

***

## 为 Angular 应用添加动画

如果这些出色的单页应用表现得不像单页应用，那么创建它们的意义何在？我们希望应用程序尽可能像原生应用，这样我们就可以模糊 Web 应用与原生应用之间的界限，给用户留下更深的印象。

AngularJS 提供了一种创建单页应用的很好的方法。由于我们是单页应用，这使得网站感觉越来越像原生移动应用。为了让它感觉更原生，我们可以使用 [ngAnimate 模块](http://docs.angularjs.org/api/ngAnimate) 添加过渡和动画。

该模块允许我们创建外观精美的应用程序，我们将查看如何为 ng-view 添加动画。

#### 为我们的路由应用添加动画

我们将为上一章中构建的单页应用添加动画。得益于我们的路由，当人们在页面之间点击时网站不会刷新。现在我们将：

*   让 `ngRoute` 处理路由（在上一章已完成）
*   使用 `ngAnimate` 创建页面动画
*   使用 `CSS 动画` 处理页面动画

在开始动画之前，让我们聊聊 `ngAnimate 模块` 是如何工作的。

#### ngAnimate 模块是如何工作的？

`ngAnimate` 会根据元素进入或离开视图，向不同的 Angular 指令添加或移除 CSS 类。这会自动发生，我们不需要配置任何内容。

当我们加载网站时自动添加和移除的类是 `.ng-enter` 或 `.ng-leave`。这些类被应用于应用 `ng-view` 指令的 div 上。我们现在还看不到这些，但如果你在页面之间点击时进入浏览器检查器，你会看到 `.ng-enter` 和 `.ng-leave` 类被应用。

#### 动画是如何应用的

该模块保持了内容的简洁和简单。它所做的只是添加类。但它是如何创建动画的呢？实际上它并没有。它为我们提供了所需的工具，然后我们通过创建 CSS 动画来控制动画。通过使用 CSS 动画，我们确保应用程序可以在移动浏览器、桌面端浏览器中工作，并符合最新标准（CSS3）。

我们将使用 [Animate.css](http://daneden.github.io/animate.css/) 项目的 CSS 动画，因为那些类（https://github.com/daneden/animate.css/blob/master/animate.css）可以很容易地引入我们自己的项目中。

#### 使用动画的指令

`ngAnimate` 还会自动将这些类应用于更多的 Angular 指令。除了 `ngView` 模块外，这些类还被应用于 `ngRepeat`、`ngInclude`、`ngIf`、`ngSwitch`、`ngShow`、`ngHide`、`ngView` 和 `ngClass`。这意味着你可以对应用程序的多个部分添加动画。在本章中我们将关注 `ngView`，但这些策略可以很容易地应用于其他指令。

#### 为我们的路由应用添加动画

在上一章的应用程序中使用 `ngAnimate` 模块有三个步骤：

1.  链接到 `angular-animate.js` 文件
2.  将 `ngAnimate` 模块注入到我们的主 Angular 模块中
3.  添加 `animate.css` 样式表以获得构建的 CSS 动画

我们将使用 CDN 获取所需的 `angular-animate.js` 和 `animate.css` 资源。回到你的 `index.html` 文件并将这两个资源添加到文档的 `<head>` 中。

```
 1 <head>
 2     <meta charset="utf-8">
 3     <title>My Routing App!</title>
 4 
 5     <!-- 设置路由的基路径 -->
 6     <base href="/">
 7 
 8     <!-- CSS -->
 9     <!-- 加载 bootstrap 和 fontawesome -->
 10    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
 11    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
 12    <!-- 加载 animate.css -->
 13    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.2/animate.min.css">
 14    
 15     <!-- JS -->
 16    <!-- 加载 angular, angular-route 和 angular-animate -->
 17    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.5.8/angular.min.js"></script>
 18    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.5.8/angular-route.min.js"></script>
 19    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.5.8/angular-animate.min.js"></script>
 20    
 21    <script src="js/app.js"></script>
 22    <script src="js/routes.js"></script>
 23 </head>
```

对于需要的 `angular-animate.js` 和 `animate.css` 资源，我们将使用 CDN。回到你的 `index.html` 文件并将这两个资源添加到文档的 `<head>` 中。

（上述代码块中的注释已根据逻辑进行了翻译和对齐）




```
1     <link rel="stylesheet" href="css/style.css">
```

我们将做的另一个更改是将 `<div ng-view></div>` 包裹在另一个 div 中，这样我们就可以专门地调用它。它看起来是这样：

```
1     <div id="content-views">
2         <div ng-view></div>
3     </div>
```

现在我们只需要进入新创建的样式表添加样式。不要忘记在 `index.html` 中链接你的样式表 `<link rel="stylesheet" href="css/style.css" />`。

```
     body                          { padding-top:50px; }

     #content-views                { position:relative; }

     .ng-enter, .ng-leave          { width:100%; position:absolute; }
     .ng-enter                     { 
       -webkit-animation:zoomInDown 1.2s both ease-in; 
       -moz-animation:zoomInDown 1.2s both ease-in; 
         animation:zoomInDown 1.2s both ease-in; 
     }
     .ng-leave                     { 
       -webkit-animation:zoomOutDown 0.5s both ease-in; 
       -moz-animation:zoomOutDown 0.5s both ease-in; 
         animation:zoomOutDown 0.5s both ease-in; 
     }
```

**厂商前缀 (Vendor Prefixes)**：在将此代码推送到生产环境时，确保添加 `-moz-animation` 和 `-webkit-animation` 厂商前缀，以实现浏览器的兼容。

继续点击应用程序中的页面，观察页面飞出和飞入的效果！就是这样，我们有了一个动画应用程序！可以尝试其他的 [animate.css](http://daneden.github.io/animate.css/) 类，看看你可以创建出多么疯狂不同的效果。

### 结论

这应该向你了如何将 Angular 路由和动画模块结合，可以快速构建看起来复杂的应用程序。这些技术可以用于构建各种不同风格的应用程序。到目前为止，在 Angular 方面我们已经：

*   设置了 AngularJS 模块
*   将 Angular 应用到我们的 HTML 视图中
*   使用 `ngRoute` 对我们的应用程序进行路由
*   使用 `ngAnimate` 和 CSS 类为我们的应用程序制作动画

掌握上述知识将让我们能够构建出非常漂亮的应用程序。在接下来的章节中，我们将通过构建更多示例应用程序进一步探索这些概念。

到目前为止我们关注的是前端 Angular 部分；下一步是如何让 Angular 应用程序动态化。我们将转向整合前端和后端，但首先让我们确保应用程序的基础是稳固的，以便我们的应用程序具有可扩展性且易于理解。

## MEAN Stack 应用程序结构

到目前，我们已经能够将大部分代码存放在几个主文件中（Node 的 `server.js` 和 Angular 的 `app.js`）。当我们开始转向更大的 MEAN Stack 应用程序时，将所有代码都堆积在这些主文件中将变得非常笨重。维护代码、查找应用程序的某些部分将变得困难，最糟糕的是，与其他开发者共享错综复杂的代码。

考虑到这一点，让我们看看我们的应用程序结构。组织如此简单的东西会有深远的影响。这是一个短小章节，但是一个非常重要的章节。

### 示例组织

到目前为止，我们的应用程序具有以下文件结构：

```
 // node applications
 - app/
 ----- models/

 // angular applications
 - public/
 ----- css/
 ----- js/
---------- controllers/
---------- services/
 ----- app.js
 ----- views/
---------- pages/
 ----- index.html

 - package.json
 - server.js
```

在 **Node 方面**，我们不能将所有内容都留在 `server.js` 中。当我们开始放入更多的路由、更多的配置和更多的应用程序功能时，该文件可能会变成一个巨大的代码条条混合体。这必须被拆分为更有组织性的结构。

在 **Angular 方面**，这种结构可能会变得困惑。我们应该在哪里放置像 Bootstrap 或 Font Awesome 这样的 `lib` 文件呢？我们的 `js` 文件夹是否应该包含所有内容，包括我们的 Angular 应用程序文件？

### 更好的结构

那么更好的结构应该是什么样的？让我们结合 Node 和 Angular 部分，因为我们下一步将转向全栈应用程序。

这是一个为我们的应用程序提供良好基础的更好组织方式。这是一种**模块化**方法，允许我们简单地从应用程序中添加和删除组件。

```
 - app/
 ----- models/
 ----- routes/
 - public/
 ----- assets/  // 应用程序的基础 css/js/images（不是 Angular 文件）
---------- css/      // 一些自定义 css
---------- js/       // 一些自定义 js（不是 Angular 文件）
---------- img/
---------- libs/     // 库如 bootstrap, angular, font-awesome
 ----- app/      // 应用程序的 Angular 部分
---------- controllers/
---------- services/
---------- app.js
---------- app.routes.js
---------- views/
---------- pages/
 ----- index.html
 - package.json
 - server.js
```

#### App 文件夹

我们有 `models` 文件夹。新由于我们有了 `routes/` 文件夹。我们可以将路由放在这里。`app.js`。

#### 配置文件

我们将配置变量从 `server.js` 中移出。对于我们的目的，我们没有许多配置变量，只有 `port`、我们的 `database` 以及我们将使用的 `secret`。

在根目录下创建一个名为 `config.js` 的新文件。

以下是我们需要的：

```
module.exports = {
  'port': process.env.PORT || 8080,
  'database': 'mongodb://node:novus.modulus.net:27017/ganiq8o',
  'secret': 'ilovescscotchyscotscotch'
};
```

#### Public 文件夹

这是大部分移动发生的地方。之前，我们将所有（Angular 文件和资源文件）存储在 `public/js` 文件夹中。随着应用程序的增长，这可能会变得混乱，所以现在我们设置让资源和应用程序文件位于不同的目录。

任何 Angular 特有的（如控制器、服务、路由和视图）将位于 `app/` 文件夹。像图像、自定义 CSS 和库将位于 `assets/` 文件夹。

在这里我们创建了 `app.routes.js` 文件。未来当我们创建更多路由时，我们可能想要将其移动到自己的 `routes/` 文件夹中，就像我们对 Node 端做的那样。

#### Routes 文件夹

我们只是将路由移动到 `routes/api.js` 文件中。我们甚至可以在文件夹中创建多个路由。

### Node Node.js 后端

由于第 10 章是关于创建 Node API 并对其进行验证的，这里只有 Node 代码可以处理。

看看如何重新整理 Node 代码（快速说 10 遍……Node 代码，Node 代码，Node 代码）。请继续复制你的第 10 章代码并为它创建一个新项目。

以下我们将采取的步骤概述：

*   将配置变量移动到新的 `config.js`
*   将路由移动到新的 `routes/api.js` 文件中
*   创建一个通符路由以准备用于 MEAN 应用

#### 通符路由

当 Angular 应用程序部署时，我们需要创建一个通符路由，以便任何不是针对 API 的请求都由 `index.html` 文件提供。这允许 Angular 处理路由。

```javascript
app.get('*', (req, res) => {
  res.sendFile(path.join(__dirname, 'public/index.html'));
});
```




现在我们可以使用 `require()` 在我们的 `server.js` 文件中使用此文件。以下行将会被修改：

```
1 var config     = require('./config');
2 
3 // 连接到我们的数据库（托管在 modulus.io）
4 mongoose.connect(config.database); 
5 
6 // 启动服务器
7 // ====================================
8 app.listen(config.port);
9 console.log('Magic happens on port ' + config.port);
```

以下已经被移出，因此可以从 `server.js` 中删除：

```
1 // 创建令牌的超级密钥
2 var superSecret = 'ilovescotchscotchyscotchscotch';
```

虽然这看起来作用不大，但当我们的应用程序拥有 20 多个设置时，这个概念将产生巨大的影响。

***

![Note](img/icon-pencil.png "注意")

## Note

### 什么是 `module.exports`？

默认情况下，JavaScript 没有任何在不同文件之间传递信息的方法。`module.exports` 是 Node 解决这个问题的方法。

你可以将 `module.exports` 视为我们应用程序的一个巨大对象。当我们的应用程序启动时，这个 `module.exports` 对象看起来如下：

```
1 module.exports = {};
```

当我们开始使用 `require()` 将内容引入应用程序时，所有内容都会被添加到这个对象中。

所以，现在当我们通过 `require(./config.js);` 添加新的 `config.js` 文件时，我们就可以访问那些变量了，因为我们通过 `module.exports` 传递了它们。

这就是我们将在所有文件之间传递信息的方式，当我们在创建路由文件时再次在实践中看到这一点。

同样重要的一点是，网络上的许多教程会在 `module.exports` 和 `exports` 之间切换。它们的意思相同，可以互相替换。

***

### 路由 (Routes)

就像我们的配置变量一样，让我们把路由移动到自己的文件中。创建一个名为 `app/routes/` 的文件夹和一个名为 `app/routes/api.js` 的文件。

在创建新文件时，我们必须 `require()` 该文件所需要的任何内容。在我们的情况下，我们需要 `body-parser`、我们的 `User` 模型、用于 `secret` 的 `config` 文件，以及 `jsonwebtoken`，因为它们在我们的路由中被用过。

我们还需要 `app` 和 `express`，但我们将它们传递到路由中，因为我们希望应用程序使用我们在 `server.js` 中创建的同一个 `app` 对象。让我们来看看如何构建包含所有 API 路由的 `routes/api.js` 文件。进入第 10 章现有的‘server.js’文件，提取所有的路由代码，从 `var apiRouter = express.Router();` 开始。我们将将其封装在 `module.exports` 中，以便它可以在我们的 JavaScript 文件之间传递。还要注意变量 `superSecret` 的变化以及我们在顶部引入的包。




```javascript
var User       = require('../models/user');
var jwt        = require('jsonwebtoken');
var config     = require('../../config');

// 用于创建令牌的密钥
var superSecret = config.secret;

module.exports = function(app, express) {

  var apiRouter = express.Router();

  // 身份验证用户的路由 (POST http://localhost:8080/api/authenticate)
  apiRouter.post('/authenticate', function(req, res) {
    console.log(req.body.username);

    // 查找用户
    // 显式选择密码，因为 mongoose 默认不返回它
    User.findOne({
      username: req.body.username
    }).select('password').exec(function(err, user) {

      if (err) throw err;

      // 未找到该用户名的用户
      if (!user) {
        res.json({ 
          success: false, 
          message: '认证失败。未找到用户。' 
        });
      } else if (user) {

        // 检查密码是否匹配
        var validPassword = user.comparePassword(req.body.password);
        if (!validPassword) {
          res.json({ 
            success: false, 
            message: '认证失败。密码错误。' 
          });
        } else {

          // 如果找到了用户且密码正确
          // 创建令牌
          var token = jwt.sign(user, superSecret, {
            expiresInMinutes: 1440 // 24 小时后过期
          });

          // 返回包含令牌在内的 JSON 信息
          res.json({
            success: true,
            message: '请使用您的令牌！',
            token: token
          });
        }   

      });
  });

  // 验证令牌的路由中间件
  apiRouter.use(function(req, res, next) {
      // 日志
      console.log('有人访问了我们的应用！');

      // 检查头部、URL 参数或请求参数中的令牌
      var token = req.body.token || req.param('token') || req.headers['x-access-token'];

      // 解码令牌
      if (token) {

        // 验证密钥并检查过期
        jwt.verify(token, superSecret, function(err, decoded) {      
          if (err) {
            return res.json({ success: false, message: '令牌认证失败。' });    
          } else {
            // 如果一切正常，保存到请求中供其他路由使用
            req.decoded = decoded;    

            next(); // 确保我们进入下一个路由而不是在此停止
          }
        });

      } else {

      // 如果没有令牌
      // 返回 HTTP 403 响应（访问被禁止）和错误消息
      return res.status(403).send({ 
        success: false, 
        message: '未提供令牌。' 
      });
      
    }

  });

  // 测试路由以确保一切运行正常 
  // 访问地址为 GET http://localhost:8080/api
  apiRouter.get('/', function(req, res) {
      res.json({ message: '万岁！欢迎来到我们的 api!' });   
  });

  // 以 /users 结尾的路由
  // ----------------------------------------------------
  apiRouter.route('/users')

      // 创建用户 (访问地址为 POST http://localhost:8080/users)
      .post(function(req, res) {
          
          var user = new User();      // 创建 User 模型的新实例
          user.name = req.body.name;  // 设置用户名称（来自请求）
          user.username = req.body.username;  // 设置用户名（来自请求）
          user.password = req.body.password;  // 设置用户密码（来自请求）
          user.save(function(err) {
              if (err) res.send(err);
              // 返回消息
              res.json({ message: '用户创建成功！' });
          });
      })
      // 获取所有用户 (访问地址为 GET http://localhost:8080/api/users)
      .get(function(req, res) {
          User.find(function(err, users) {
              if (err) res.send(err);
              // 返回用户
              res.json(users);
          });
      });
  // 以 /users/:user_id 结尾的路由
  // ----------------------------------------------------
  apiRouter.route('/users/:user_id')
      // 根据该 ID 获取用户
      .get(function(req, res) {
          User.findById(req.params.user_id, function(err, user) {
              if (err) res.send(err);
              // 返回该用户
              res.json(user);
          });
      })
      // 根据此 ID 更新用户
      .put(function(req, res) {
          User.findById(req.params.user_id, function(err, user) {
              if (err) res.send(err);
              // 如果请求中存在新用户信息，则设置新信息
              if (req.body.name) user.name = req.body.name;
              if (req.body.username) user.username = req.body.username;
              if (req.body.password) user.password = req.body.password;
              user.save(function(err) {
                  if (err) res.send(err);
                  // 返回消息
                  res.json({ message: '用户已更新！ });
              });
          });
      })
      // 根据此 ID 删除用户
      .delete(function(req, res) {
          User.remove({
              _id: req.params.user_id
          }, function(err) {
              if (err) res.send(err);
              // 返回消息
              res.json({ message: '用户已删除' });
          });
      });

  return apiRouter;
};
```





任何未被 Node 处理的路由都将传递给 Angular。创建路由非常简单。我们将删除为主页创建的路由，并创建以下内容：

```
 1 var path = require('path');
 2 
 3 ... 
 4 
 5 var apiRoutes...
 6 
 7 // 主通配路由  --------------- 
 8 // 将用户发送到前端 ------------
 9 // 必须在 API 路由之后注册
10 app.get('*', function(req, res) {
11   res.sendFile(path.join(__dirname + '/public/app/views/index.html'));
12 });
```

确保 `path` 已在包（packages）部分中加载，因为传递 HTML 文件需要它。使用 `*` 会匹配所有路由。将此路由放在 **API 路由之后** 是非常重要的，因为我们只希望它来捕获未被 Node 处理的路由。

如果将其置于 API 路由之上，我们的用户将始终被发送 `index.html` 文件，而永远无法到达 API 路由。

# 最终的 Node server.js

这里是完整的 `server.js` 文件：

```
 1 // 基础设置
 2 // ======================================
 3 
 4 // 调用包 --------------------
 5 var express    = require('express');    // 调用 express
 6 var app        = express();         // 使用 express 定义我们的应用
 7 var bodyParser = require('body-parser');  // 获取 body-parser
 8 var morgan     = require('morgan');     // 用于查看请求
9 var mongoose   = require('mongoose');
10 var config     = require('./config');
11 var path     = require('path');
12 
13 // 应用配置 ==================
14 // ====================================
15 // 使用 body parser 以便我们可以从 POST 请求中获取信息
16 app.use(bodyParser.urlencoded({ extended: true }));
17 app.use(bodyParser.json())
18 
19 配置我们的应用以处理 CORS 请求
20 app.use(function(req, res, next) {
21   res.setHeader('Access-Control-Allow-Origin', '*');
22   res.setHeader('Access-Control-Allow-Methods', 'GET, POST');
23   res.setHeader('Access-Control-Allow-Headers', 'X-Requested-With,content-type, \
24 Authorization');
25   next();
26 });
27 
28 // 将所有请求记录到控制台 
29 app.use(morgan('dev'))
 30 
31 连接到我们的数据库（托管在 modulus.io）
32 mongoose.connect(config.database); 
33 
34 // 设置静态文件位置
35 // 用于前端发起的请求
36 app.use(express.static(__dirname + '/public'));
37 
38 // API 路由 =================
39 // ====================================
40 
41 // API 路由 ------------------------
42 var apiRoutes = require('./app/routes/api')(app, express);
43 app.use('/api', apiRoutes);
44 
45 // 主通配路由  --------------- 
46 // 将用户发送到前端 ------------
47 // 必须在 API 路由之后注册
48 app.get('*', function(req, res) {
49   res.sendFile(path.join(__dirname + '/public/app/views/index.html'));
50 });
51 
52 // 服务器
53 // ====================================
54 app.listen(config.port);
55 console.log('Magic happens on port ' + config.port);
```

现在我们已经整理好了 Node 端的工作，让我们为 Angular 应用程序奠定基础。

# 组织 AngularJS - 前端

在这里我们将创建唯一的文件是 `index.html` 文件，因为这是我们通过 Node 通配路由返回的内容。我们只需为应用程序的其他部分创建文件夹，以便准备好基础工作工作。

以下是目前的文件结构：

```
 1 - app/
 2 ----- models/
 3 ----- routes/
 4 ---------- api.js
 5 - public/
 6 ----- assests/  
 7 ---------- css/   
 8 --------------- style.css   
 9 ---------- js/
10 ---------- img/       
11 ---------- libs/     
12 ----- app/      
13 ---------- controllers/
14 ---------- services/
15 ---------- app.routes.js
16 ---------- app.js
17 ---------- views/
18 --------------- pages/
19 --------------- index.html
20 - package.json
21 - config.js- server.js
```

继续在 `public/` 文件夹中创建文件夹和文件。

这是我们 `index.html` 文件的良好起点：

```
 1 <!DOCTYPE html>
 2 <html lang="en">
 3 <head>
 4   <meta charset="UTF-8">
 5   <title>My MEAN App</title>
 6 </head>
 7 <body>
 8   
 9 HELLO!
10 
11 </body>
12 </html>
```

# 测试我们新整理的应用

让我们确保一切都运行正常。

运行

`npm install`

如果你还没有安装依赖项的话。

然后运行

`nodemon server.js`

并在浏览器中访问！




`$http` 模块可以注入到 Angular 模块中，无论是控制器还是服务。在上面的示例中，它被注入到了控制器中。然而，我们不希望在控制器中直接调用 `$http` 模块。这些逻辑应该移动到服务中，以便实现清晰的职责分离。服务获取数据，而控制器接收数据并将其发送到我们的视图。

让我们看看如何在工厂（factory）中使用 `$http` 模块。

### 示例 Angular 服务

我们将构建一个示例工厂，并查看我们如何在 Angular 控制器中使用它。

#### Angular 工厂

这是一个名为 `userService.js` 的快速示例文件，它将访问一个提供用户数据的 API。

```
 1 angular.module('stuffService', [])
 2 
 3 .factory('Stuff', function($http) {
 4 
 5   // create the object
 6   var myFactory = {};
 7 
 8   // a function to get all the stuff
 9   myFactory.all = function() {
10     return $http.get('/api/stuff');
11   };
12 
13   return myFactory;
14 
15 });
```

我们刚刚创建了第一个 Angular 服务！语法非常直观。我们有一个名为 `Stuff` 的 `factory` 和一个名为 `all` 的函数。该函数将使用 `$http` 模块创建一个 HTTP GET 调用并返回一个 promise 对象。然后我们可以通过访问 `success()`、`error()` 或 `then()` 来对 promise 对象进行操作。对于我们的目的来说，`success()` 就足够了。

***

![Tip](img/icon-heart.png "专业提示")

提示

#### Promises（期 Promise）

如果你是 JavaScript 开发的新手，Promises 是一个很难理解的概念。Promises 通过充当某种占位符来帮助我们处理 JavaScript 的异步性质。我们请求某些数据，promise 将等待响应，以便我们的程序其他部分可以继续它们正在做的其他工作。一旦我们的 promise 接收到结果，它将通知我们，我们可以根据该结果（无论成功还是失败）执行后续操作。

这里是一些理解 promises 的良好资源：

* [promisejs.org](https://www.promisejs.org/) - 一个良好的原生 JS 解释
* [AngularJS 中的 Promises，漫画版详解](http://andyshora.com/promises-angularjs-explained-as-cartoon.html)

我们将使用 promises 来处理从我们的 API 获取数据。这确保了我们按照想要的方式获取数据，并且数据不会丢失。`$http` 模块将返回一个我们可以使用的 promise 对象。

***

现在我们已经创建了 `stuffService` Angular 模块和 `Stuff` 工厂，让我们看看如何在 Angular 控制器中使用这个工厂。

#### 在控制器中使用服务

```
 1 // inject the stuff service into our main Angular module
 2 angular.module('myApp', ['stuffService'])
 3 
 4 // create a controller and inject the Stuff factory
 5 .controller('userController', function(Stuff) {
 6   
 7   var vm = this;
 8 
 9   // get all the stuff
10   Stuff.all()
11 
12     // promise object
13     .success(function(data) {
14 
15       // bind the data to a controller variable
16       // this comes from the stuffService
17       vm.stuff = data;
18     });
19 
20 });
```

就是这样，我们创建了一个 Angular 服务，将其注入到控制器中，并获取了所有的用户数据。理解此处的职责分离至关重要。

> 服务负责从外部资源（我们的 API）获取数据，而控制器负责将这些数据提供给我们的视图。

我们的控制器和服务之间存在职责分离。服务获取数据，控制器将数据传递给视图。

### 用户服务 (User Service)

让我们创建一个将在最终应用程序使用的服务。我们将其命名为 `userService`。创建这种独立服务的用处是它可以在其他项目中复用。

就像我们在后端创建 API 端点一样，我们使用使用 `$http` 模块在服务中创建函数，用以从每个端点进行数据抓取。我们需要处理以下情况：

* 获取单个用户
* 获取所有用户列表
* 创建用户
* 更新用户
* 删除用户

所有这些任务共同组成了你的的常规 CRUD 操作。作为参考，让我们看看如何将前端需求与后端 API 匹配。我们的匹配表还将显示需要使用的 HTTP 动词，因为我们希望坚持我们所创建的 REST 模式。

| 任务 | Node API | Angular 服务函数 |
| --- | --- | --- |
| 单用户 | GET /api/users/:user_id | get(id) |
| 用户列表 | GET /api/users | all() |
| 创建用户 | POST /api/users | create(userData) |
| 更新用户 | PUT /api/users/:user_id | update(id, userData) |
| 删除用户 | DELETE /api/users/:user_id | delete(id) |

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

无论你选择什么，最重要的一点是有一套设置。

让我们为整个团队创建一个 `userService`。我们将定义我们的 Angular 模块，并创建一个 `User` 工厂来配合使用。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

我们的前端函数可以命名为任何名称。如果你愿意，甚至可以让它们与后端函数匹配。例如，与其使用 `create(userData)`，不如使用 `postUser(userData)` 以保持后端一致。

无论你选择什么，最重要的一点是有一套设置。

让我们为整个团队创建一个 `User` 的。

```
 1 angular.module('stuffService', [])
 2 
 3 .factory('Stuff', function($http) {
 4 
 5   // create the object
 6   var myFactory = {};
 7 
 8   // a function to get all the stuff
 9   myFactory.all = function() {
10     return $http.get('/api/stuff');
11   };
12 
13   return myFactory;
14 
15 });
```



到目前为止，我们已经创建了一个 Node API 并使用 JSON 令牌（JWT）对其进行身份验证。这些一直都是服务器端代码，现在我们将使用刚刚学到的信息将其与前端集成。

这里的目标是开始编写一个 Angular 应用程序，而不需要修改后端。像这样这样处理你的应用程序可以模拟类似的情况，即后端 API 由你以外的人构建和维护（例如 Facebook、Twitter 或 GitHub API）。我们只有前端代码的访问权限。

构建一个与后端 API 通信的应用程序时，第一步是处理身份验证。毕竟，如果不通过身份验证，我们就无法从 API 中获取任何数据。

## 接入我们的 Node API

我们在第 9 章和第 10 章中使用 JSON Web Token 身份验证创建 Node API 时，我们开发了一个 API 端点（`POST http://localhost:8080/api/authenticate`），我们可以在那里发送用户名和密码来接收 JWT。

由于我们的后端已经有了身份验证和提供令牌的工具，我们只需要将前端 Angular 应用连接到该端点，将 JWT 存储在客户端，然后就可以访问 API 中所有经过身份验证的路由。

## 身份验证服务

我们将构建两个不同的服务，一个用于身份验证，另一个用于连接我们的 API 并获取用户数据。通常情况下，如果你从或向外部源获取或发送数据，服务可能是你的首选工具。

为了验证用户，我们将创建一个 `authService`。它将具有 3 个主功能：

* 主身份验证函数（登录、注销、获取当前用户、检查是否登录）
* 令牌验证函数（获取令牌、保存令牌）
* 身份验证拦截器（将令牌附加到 HTTP 请求中，未登录时重定向）

这三个工厂中的每一个都有非常特定的用途，这就是为什么我们不能只创建一个。

主身份验证函数将暴露给我们的应用程序并在控制器内部使用。

身份验证拦截器将负责将令牌附加到所有 HTTP 请求中。记住，在基于令牌的身份验证中，所有经过验证的请求都需要令牌；这个拦截器就是我们实现这种附加的方式。该拦截器还负责在用户未通过验证时将用户重定向到登录页面。

令牌验证函数更像是一个供其他两个身份验证工厂使用的私有工厂。它只需要保存令牌或从本地存储中获取令牌。

以下是我们的文件内容的概览：

```
 1 angular.module('authService', [])
 2 
 3 // ===================================================
 4 // 用于登录和获取信息的 auth 工厂
 5 // 注入 $http 用于与 API 通信
 6 // 注入 $q 返回 promise 对象
 7 // 注入 AuthToken 管理令牌
 8 // ===================================================
 9 .factory('Auth', function($http, $q, AuthToken) {
10 
11   // 创建 auth 工厂 对象
12   var authFactory = {};
13 
14   // 处理登录
15 
16   // 处理注销
17 
18   // 检查用户是否登录
19 
20   // 获取用户信息
21 
22   // 返回 auth 工厂 对象
23   return authFactory;
24 
25 })
26 
27 // ===================================================
 28 // 处理令牌的工厂
 29 // 注入 $window 在客户端存储令牌
 30 // ===================================================
31 .factory('AuthToken', function($window) {
32 
33   var authTokenFactory = {};
34 
35   // 获取令牌
36 
37   // 设置令牌或清除令牌
38 
39   return authTokenFactory;
40 
41 })
42 
43 // ===================================================
 44 // 将令牌集成到请求中的应用程序配置
 45 // ===================================================
46 .factory('AuthInterceptor', function($q, AuthToken) {
47 
48   var interceptorFactory = {};
49 
50   // 为每个请求附加令牌
51 
52   // 如果令牌未通过身份验证则重定向
53 
54   return interceptorFactory;
55 
56 });
```

这些是我们即将创建的三个工厂，它们都整合在一个名为 `authService` 的 Angular 模块中。对于每个工厂，我们都创建了一个新对象，将函数附加到对象上并返回该对象。

注意，我们能够将一个工厂注入另一个工厂中。我们在其他两个工厂中使用了 `AuthToken` 工厂。我们还向工厂中注入了一些 Angular 模块，如 `$http`、`$q` 和 `$location`。

`$location` 将用于重定向用户的模块。这就是我们在仍然使用 Angular 路由机制的同时进行重定向的方法。这意味着用户将在不刷新页面的情况下被重定向。

`$q` 是用于返回 promise 的模块。它允许我们异步运行函数并在处理完成时返回它们的值。在上一章中，我们使用 `success()`、`error()` 和 `then()` 来处理 promise；在返回 `$q` 时，我们也可以使用这些函数。

让我们逐一查看这些工厂，以便我们看到整个 `authService` 是如何工作的。

### 身份令牌工厂

我们将从 `AuthTokenFactory` 开始，因为它将被其他两个工厂使用。要检查本地存储中的内容，只需进入 开发者工具，点击 Resources（资源），然后查看 Local Storage（本地存储）标签页。

![Local Storage](img/16-authentication----local-storage.jpg)

Local Storage

以下是 `AuthTokenFactory` 的代码：

```
1 // ===================================================
 2 // 处理令牌的工厂
 3 // 注入 $window 在客户端存储令牌
 4 // ===================================================
5 .factory('AuthToken', function($window) {
6 
7   var authTokenFactory = {};
8 
9   // 从本地存储中获取令牌
10   authTokenFactory.getToken = function() {
11     return $window.localStorage.getItem('token');
12   };
13 
14   // 设置令牌或清除令牌的函数
15   // 如果传递了令牌，则设置令牌
16   // 如果没有令牌，则从本地存储中清除
17   authTokenFactory.setToken = function(token) {
18     if (token)
19       $window.localStorage.setItem('token', token);
20     else
21       $window.localStorage.removeItem('token');
22   };
23 
24   return authTokenFactory;
25 
26 })
```

这里这里有两个函数。`getToken()` 和 `setToken()`。`$window.localStorage` 是我们在本地存储中添加、设置或删除项目的方法。

接下来，让我们创建将在应用程序控制器使用的主身份验证工厂。

### 身份验证工厂

主身份验证工厂将包含登录用户、注销用户、检查用户是否登录以及获取用户信息所需的函数。

让我们看看那个工厂是什么样子：





```javascript
 // ===================================================
 // 用于登录和获取信息的 auth 工厂
 // 注入 $http 用于与 API 通信
 // 注入 $q 用于返回 promise 对象
 // 注入 AuthToken 用于管理 token
 // ===================================================
.factory('Auth', function($http, $q, AuthToken) {

  // 创建 auth 工厂对象
  var authFactory = {};

  // 登录用户
  authFactory.login = function(username, password) {

    // 返回 promise 对象及其数据
    return $http.post('/api/authenticate', {
      username: username,
      password: password
    })
      .success(function(data) {
        AuthToken.setToken(data.token);
        return data;
      });
  };

  // 通过清除 token 退出登录
  authFactory.logout = function() {
    // 清除 token
    AuthToken.setToken();
  };

  // 检查用户是否登录
  // 检查是否存在本地 token
  authFactory.isLoggedIn = function() {
    if (AuthToken.getToken()) 
      return true;
    else
      return false; 
  };

  // 获取已登录的用户
  authFactory.getUser = function() {
    if (AuthToken.getToken())
      return $http.get('/api/me');
    else
      return $q.reject({ message: 'User has no token.' });    
  };

  // 返回 auth 工厂对象
  return authFactory;

})
```

我们有 4 个函数，它们会返回一个 promise 对象（通过 `$http` 或 `$q`）或者一个简单的 `true/false`。

`login` 将向我们 Node API 上的 `/api/authenticate` 端点创建一个一个 `$http.post()` 请求。

`logout` 将简单地使用 `AuthToken` 工厂来清除 token。

`isLoggedIn` 将根据本地存储中是否存在 token 来返回 true 或 false。

`getUser` 将向 `/me` API 端点发送一个 `$http.get()` 请求，用以获取已登录的用户信息。

接下来，我们将创建拦截器（interceptor）工厂。

## AuthInterceptor 工厂

`AuthInterceptor` 工厂将负责为从我们前端应用发送的所有 HTTP 请求附加 token。

```javascript
 // ===================================================
 // 将 token 集成到请求中的应用程序配置
 // ===================================================
.factory('AuthInterceptor', function($q, $location, AuthToken) {

  var interceptorFactory = {};

  // 这将发生在所有 HTTP 请求上
  interceptorFactory.request = function(config) {

    // 获取 token
    var token = AuthToken.getToken();

    // 如果 token 存在，将其作为 x-access-token 添加到头部
    if (token) 
      config.headers['x-access-token'] = token;
    
    return config;
  };

  // 发生在响应错误时
  interceptorFactory.responseError = function(response) {

    // 如果我们的服务器返回了 403 forbidden 响应
    if (response.status == 403) {
      AuthToken.setToken();
      $location.path('/login');
    }

    // 将服务器的错误作为 promise 返回
    return $q.reject(response);
  };

  return interceptorFactory;
  
 });
```

Angular 中的拦截器（interceptor）允许我们响应不同的 HTTP 请求场景。在创建拦截器时，我们有几个选项可用：

* `request` 允许我们在请求发送之前对其进行拦截
* `response` 允许我们更改从请求中获取的响应
* `requestError` 捕获已取消的请求
* `responseError` 捕获失败的后端调用。在这种情况下，我们将使用它来捕获 token 无效或不存在时的 403 Forbidden 错误。

如果从从后端接收到 403 错误，我们被迫使用 `$location.path('/login')` 将用户重定向到登录页面。我们还将清除存储中的任何 token，因为这些 token 不足以验证我们的用户身份。

这些就是创建 Angular 应用中创建身份验证功能所需的三个工厂。我们能够与后端 API 通信，在客户端获取和设置 token，并将 token 附加到所有的请求中。

## 整个 Auth 服务文件 (authService.js)

```javascript
 angular.module('authService', [])
  
 // ===================================================
 // 用于登录和获取信息的 auth 工厂
 // 注入 $http 用于与 API 通信
 // 注入 $q 用于返回 promise 对象
 // 注入 AuthToken 用于管理 token
 // ===================================================
.factory('Auth', function($http, $q, AuthToken) {

  // 创建 auth 工厂对象
  var authFactory = {};

  // 登录用户
  authFactory.login = function(username, password) {

    // 返回 promise 对象及其数据
    return $http.post('/api/authenticate', {
      username: username,
      password: password
    })
      .success(function(data) {
        AuthToken.setToken(data.token);
        return data;
      });
  };

  // 通过清除 token 退出登录
  authFactory.logout = function() {
    // 清除 token
    AuthToken.setToken();
  };

  // 检查用户是否登录
  // 检查是否存在本地 token
  authFactory.isLoggedIn = function() {
    if (AuthToken.getToken()) 
      return true;
    else
      return false; 
  };

  // 获取已登录的用户
  authFactory.getUser = function() {
    if (AuthToken.getToken())
      return $http.get('/api/me');
    else
      return $q.reject({ message: 'User has no token.' });    
  };

  // 返回 auth 工厂对象
  return authFactory;

})

 // ===================================================
 // 处理 token 的工厂
 // 注入 $window 在客户端存储 token
 // ===================================================
.factory('AuthToken', function($window) {

  var authTokenFactory = {};

  // 从存储中获取 token
  authTokenFactory.getToken = function() {
    return $window.getItem('token');
  };

  // 设置或清除 token 的函数
  // 如果传递了 token，则设置 token
  // 如果没有 token，则从本地存储中清除
  authTokenFactory.setToken = function(token) {
    if (token)
      $window.setItem('token', token);
    else
      $window.removeItem('token');
  };

  return authTokenFactory;

})

 // ===================================================
 // 将 token 集成到请求中的应用程序配置
 // ===================================================
.factory('AuthInterceptor', function($q, $location, AuthToken) {

  var interceptorFactory = {};

  // 这将发生在所有 HTTP 请求上
  interceptorFactory.request = function(config) {

    // 获取 token
    var token = AuthToken.getToken();

    // 如果 token 存在，将其作为 x-access-token 添加到头部
    if (token) 
      config.headers['x-access-token'] = token;
    
    return config;
  };

  // 发生在响应错误时
  interceptorFactory.responseError = function(response) {

    // 如果我们的服务器返回了 403 forbidden 响应
    if (response.status == 403)
      $location.path('/login');

    // 将服务器的错误作为 promise 返回
    return $q.reject(response);
  };

  return interceptorFactory;
  
 });
```

### 结论

现在我们拥有了可以在应用程序中使用的两个优秀的 Angular 服务。这两个服务将成为前端 Angular 应用与后端 Node 应用之间的胶合剂。




除了我们刚刚从零创建的内容外，市面上也有预构建的解决方案。一个功能齐全 Angular 模块是 [ng-token-auth](https://github.com/lynndylanhurley/ng-token-auth) 模块。它提供了与上述相同的选项，但添加了一些如认证事件之类的整洁特性。

让我们继续进行，并在我们的 User CRM 应用中使用这些新文件。这就是我们一直期待的——一个完整的 MEAN 栈应用程序！我们在之前章节中的所有工作都是在为这一刻做准备。卷起袖子；在下一章节中我们有大量工作要做。

## MEAN 应用：用户管理 CRM

到为止，我们已经创建了一个 Node API 并使用 JSON Web 令牌（JWT）对其进行身份验证。这些都是服务器端代码，现在我们将利用刚刚学到的 Angular 服务知识，将其与前端集成。

这里的目标是开始编写一个 Angular 应用程序，而不需要修改后端。像这样处理你的应用程序可以模拟类似的情况，即后端 API 由你以外的人员构建和维护（例如 Facebook、Twitter 或 GitHub API）。我们只有前端代码的访问权限。

### 设置应用程序

我们将使用在第 14 章中创建的基础和应用程序结构。由于那是我们的 Node API（带身份验证），它将成为构建完整 MEAN 栈应用程序的完美设置。

#### 文件夹结构

我们将只处理 MEAN 栈中的前端和 Angular 部分，因此我们只需要在 `public/` 文件夹内工作。前端和后端的分离允许我们缩小注意力并保持开发整洁，因为我们已经确切知道代码需要去哪里。

这里是应用程序结构。

```
 1 - app/
 2 ----- models/
 3 ---------- user.js
 4 ----- routes/
 5 ---------- api.js
 6 - public/
 7 ----- assets/
 8 ---------- css/ 
9 --------------- style.css
10 ----- app/
11 ---------- controllers/
12 --------------- mainCtrl.js
13 --------------- userCtrl.js
14 ---------- services/
15 --------------- authService.js
16 --------------- userService.js
17 ---------- app.routes.js
18 ---------- app.js
19 ---------- views/
20 --------------- pages/
21 -------------------- users/
22 ------------------------- all.html
23 ------------------------- single.html
24 --------------- login.html
25 --------------- home.html
26 ---------- index.html
27 - package.json
28 - config.js- server.js
```

这些文件大部分已经在第 14 章中创建了。

`authService.js` 将与我们在上章节（第 16 章）创建的文件相同，而 `userService.js` 将是第 15 章创建的文件。

其余工作将集中在编写控制器、`routes` 和 `views` 上。

#### 引入服务

我们将添加上章节创建的服务。请取出你创建的文件并将它们添加到：

* `public/app/services/authService.js`
* `public/app/services/userService.js`

现在服务已经是我们应用程序的一部分，让我们准备好 Angular 的基础工作，然后开始使用它们连接前端和后端。

### 主应用程序

我们 Angular 应用程序的基础需要 5 个文件：

* `public/app/controllers/mainCtrl.js`
* `public/app/app.js`
* `public/app/app.routes.js`
* `public/app/views/index.html`
* `public/app/views/pages/home.html`

所有这些文件将协同工作以生成我们应用程序的主页。由于主页不需要认证，我们暂时还不需要使用 `authService.js`。

我们的主页看起来是这样的：

![首页](img/17-user-crm----user-crm-home.jpg)

首页

让我们开始创建文件吧。

**app/app.js**

```
1 angular.module('userApp', [
2   'ngAnimate',
3   'app.routes', 
4   'authService', 
5   'mainCtrl', 
6   'userCtrl', 
7   'userService'
8 ]);
```

这是我们整个应用程序的高层级概览。我们引入了：

* `ngAnimate` 用于为我们所有的 Angular 指令添加动画（特别是 `ngShow`/`ngHide`）
* `app.routes` 将作为我们应用程序的路由
* `authService` 是在第 16 章创建的服务文件
* `mainCtrl` 将是我们创建的一个全新的控制器，它包含我们的主视图
* `userCtrl` 将包含我们所有用户管理页面的控制器
* `userService` 是在第 15 章创建的服务文件

#### 路由

我们将从路由文件开始。目前，我们只为主页添加第一个路由。

**public/app.routes.js**

```
 1 angular.module('app.routes', ['ngRoute'])
 2 
3 .config(function($routeProvider, $locationProvider) {
 4 
5   $routeProvider
 6 
7     // 主页路由
8     .when('/', {
9       templateUrl : 'app/views/pages/home.html'
10     });
11   // 移除 URL
12   $locationProvider.hashMode(true);
13 });
```

这足够生成我们的首页了。现在让我们进入控制器。

#### 控制器

**public/app/controllers/mainCtrl.js**

```
1 angular.module('mainCtrl', [])
2 
3 .controller('mainCtrl', function($rootScope, $location, Auth) {
 4   var vm = this;
 5 
6   // 检查用户是否登录
7   $rootScope.$on('$routeChange', function() {
8     vm.loggedIn = Auth.isLoggedIn();
9 
10     // 获取路由更改时的信息
11     Auth.getUser()
12       .success(function(data) {
13         vm.user = data;
14       });
15   });
16 
17   // 处理登录的函数
18   vm.doLogin = function() {
19     
20     // 调用 login() 函数
21     Auth.login(loginData.username, loginData.password)
22       .success(function(data) {
23         // 如果用户登录成功，重定向到用户页面
24         $location.path('/users');
25       });
26   };
27 
28   // 处理注销的函数
29   vm.doLogout = function() {
30     
31     Auth.logout();
32     // 重置所有用户信息
33     vm.user = {};
34     $location.path('/login');
35   };
36 });
```

#### 缓存服务调用

在每次路由更改时，我们都会获取用户数据。这是为了确保我们的信息是最新的，特别是在登录后。然而，我们不希望每次调用都访问 API，所以有一种方法可以缓存这些信息。

为了缓存 `getUser()` 调用，我们需要打开 `AuthService.js` 文件。

我们只需要像下面这样向 `$http.get()` 调用添加内容：





```javascript
// get the logged in user
authFactory.getUser = function() {
  if (AuthToken.getToken())
    return $http.get('/api/me', { cache: true });
  else
    return $q.reject({ message: 'User has no token.' });    
};
```

这里的重点是 `{ cache: true }`。现在每当调用 `Auth.getUser()` 时，它将检查该信息是否已经缓存。如果在缓存中，它将返回缓存的信息。如果没有，它将发起 API 调用。

***

### 登录用户

我们将拥有一个函数来登录用户。这将使用 `username` 和 `password` 对用户进行身份验证。`vm.loginData.username` 绑定到我们在视图中创建的输入框。

### 退出用户

我们将调用 `Auth.logout()`，它将删除 `localStorage` 中的用户令牌以及存储在 `mainController` 的 `vm.user` 对象中的任何信息。然后我们将用户重定向到主页，因为他们将未经过身份验证，因此无法访问任何其他页面。

### 首页视图

就像 Angular 路由章节一样，我们需要一个主文件作为网站的整体布局。由于 Node.js 向我们的用户返回此 `index.html` 文件，这将是我们的布局文件。

**public/app/views/index.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>User CRM</title>
  
  <!-- ANGULAR ROUTING -->
  <base href="/">
  
  <!-- CSS  -->
  <!-- 从 CDN 加载 bootstrap 和自定义 CSS -->
  <link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/bootswatch/3.3.1/paper/bootstrap.min.css">
  <link rel="stylesheet" href="//cdnjs.cloudflare.com/ajax/libs/animate.css/3.1.1/animate.min.css">
  <link rel="stylesheet" href="assets/css/style.css">

  <!-- JS -->
  <!--通过 CDN 加载 angular 和 angular-route -->
  <script src="//ajax.googleapis.com/ajax/libs/angularjs/1.3.8/angular.min.js"></script>
  <script src="//ajax.googleapis.com/ajax/libs/angularjs/1.3.8/angular-route.js"></script>
  <script src="//ajax.googleapis.com/ajax/libs/angularjs/1.3.8/angular-animate.js"></script>
  
  <!-- controllers -->
  <script src="app/controllers/mainCtrl.js"></script>
  <script src="app/controllers/userCtrl.js"></script>
  
  <!-- services -->
  <script src="app/services/authService.js"></script>
  
  <!-- main Angular app 文件 -->
  <script src="app/app.routes.js"></script>
  <script src="app/app.js"></script>
</head>
<body ng-app="userApp" ng-controller="mainController as main">

<!-- NAVBAR -->
<header>
  
  <div class="navbar navbar-inverse" ng-if="main.loggedIn">
    <div class="container">
      <div class="navbar-header">
        <a href="/" class="navbar-brand"><span class="glyphicon glyphicon-fire text-danger"></span> User CRM</a>
      </div>  
      <ul class="nav navbar-nav">
        <li><a href="/users"><span class="glyphicon glyphicon-user"></span> Users</a></li>
      </ul>
      <ul class="nav navbar-nav navbar-right">
        <li ng-if="!main.loggedIn"><a href="/login">Login</a></li>      
        <li ng-if="main.loggedIn" class="navbar-text">Hello {{ main.user.name }}!</li>
        <li ng-if="main.loggedIn"><a href="#" ng-click="main.doLogout()">Logout</a></li>
      </ul>
    </div>
  </div>
  
</header>

<main class="container">
  <!-- ANGULAR VIEWS -->
  <div ng-view></div>
</main>

</body>
</html>
```

我们将 Angular 应用应用到 `<body>` 标签，并使用控制器作为语法 (`mainController as main`)。我们还加载了很快就会构建的 `userCtrl.js`。

我们所有的 CSS 文件和 Angular 应用文件都已加载。

我们将 Angular 应用应用到 `<body>` 标签，并使用控制器作为语法 (`mainController as main`)。我们还加载了很快就会构建的 `userCtrl.js`。

(注：原文中存在大量重复段落，已按要求去重)





我们将使用 `ngIf` 显示和隐藏处理图标，并将其绑定到名为 `processing` 的变量。让我们更新 `mainController` 文件中的 `doLogin()` 函数来添加此变量。

```
 1 // 处理登录表单的函数
 2 vm.doLogin = function() {
 3   vm.processing = true;
 4 
 5   Auth.login(vm.loginData.username, vm.loginData.password)
 6     .success(function(data) {
 7       vm.processing = false;
 8 
 9       // 如果用户登录成功，重定向到用户页面
10       $location.path('/users');
11     });
12 };
```

当用户点击 `Login` 时，我们将 `processing` 变量设置为 `true`。当函数完成后完成后我们将变量设置为 `false`。

现在我们只需要做的就是创建并显示处理图标。

在我们的 `login.html` 文件中，让我们为登录按钮添加该图标。

```
1 <button type="submit" class="btn btn-block btn-primary">
2 
3   <span ng-if="!login.processing">Login</span>
 4 
5   <span ng-if="login.processing" class="spinner"><span class="glyphicon glyphico\
6 n-repeat"></span></span>
 7 
8 </button>
```

如果变量为 `true`，我们将显示旋转器。否则，我们的按钮将始终显示 `Login`。

只需要少量的 CSS 来处理旋转动画，我们就准备了。将以下内容添加到 `style.css` 中：

```
 1 /* 动画
 2 ====================== */
 3 .spinner {
 4   animation:spin 1s infinite;
 5   -webkit-animation:spin 1s infinite;
 6   -moz-animation:spin 1s infinite;
 7 }
 8 
 9 @keyframes spin {
10   from  { transform:rotate(0deg); }
11   to    { transform:rotate(360deg); }
12 }
13 
14 @-webkit-keyframes spin {
15   from  { -webkit-transform:rotate(0deg); }
16   to    { -webkit-transform:rotate(360deg); }
17 }
18 
19 @-moz-keyframes spin {
20   from  { -moz-transform:rotate(0deg); }  
21   to    { -moz-transform:rotate(360deg); }
22 }
```

我们将为任何元素添加 `spinner` 类，它都会开始旋转。如果我们现在点击登录按钮，我们将看到旋转器。

![登录旋转器](img/17-user-crm----login-spinner.jpg)

登录旋转器

这种技术可以用于我们的整个应用程序。

### 添加登录错误消息

如果登录未成功，我们将让用户知道。由于我们的 API 已经返回了错误消息，我们只需要显示它们即可。

在登录函数内部，我们将检查 API 返回给我们的 `success` 变量。

```
 1   vm.doLogin = function() {
 2     vm.processing = true;
 3 
 4     // 清除错误
 5     vm.error = '';
 6 
 7     Auth.login(vm.loginData.username, vm.loginData.password)
 8       .success(function(data) {
 9         ...
10 
11         // 如果用户登录成功，重定向到用户页面
12         if (data.success) 
13           $location.path('/users');
14         else
15           vm.error = data.message;
16       });
```

每次我们点击登录时，错误消息都会清除，这样我们就不会看到过期的错误消息。在视图中，我们只需要检查该错误。在登录按钮上方添加以下内容：

```
1 <div class="alert alert-danger" ng-if="login.error">
2   {{ login.error }}
3 </div>
```

如果错误变量存在，我们将显示这个 div。

![用户不存在](img/17-user-crm----user-not-found.jpg)

用户不存在

![密码错误](img/17-user-crm----wrong-password.jpg)

密码错误

在我们的网站基础和登录准备就绪后，我们现在想要处理更多的身份验证，然后创建显示我们用户的页面。

### 身份验证

我们已经在 `mainController` 中使用了 `Auth` 工厂。我们调用了所有函数，包括 `isLoggedIn`、`login`、`logout` 和 `getUser`。

用户可以登录，他们的令牌存储在 `localStorage` 中。如果你检查浏览器的本地存储，你将看到该令牌。在为用户页面获取用户列表之前，我们必须将此令牌附加到每个请求。这就是我们在 `authService` 中创建的 `AuthInterceptor` 发挥用场的地方。

我们将在主 `app.js` 文件中使用它。让我们看看它是如何应用的：

```
 1 angular.module('userApp', [
 2   'ngAnimate', 
 3   'app.routes', 
 4   'authService',
 5   'mainCtrl',
 6   'userCtrl',
 7   'userService'
 8 ])
 9 
10 .config(function($httpProvider) {
11   $httpProvider.interceptors.push(AuthInterceptor);
12 })
```

### 用户页面

我们已经在 `mainController` 中使用了 `Auth` 工厂。我们调用了所有函数，包括 `isLoggedIn`、`login`、`logout` 和 `getUser`。

用户可以登录，他们的令牌存储在 `localStorage` 中。如果你检查浏览器的本地存储，你将看到该令牌。在为用户页面获取用户列表之前，我们必须将此令牌附加到每个请求。这就是我们在 `authService` 中创建的 `AuthInterceptor` 发挥用场的地方。

我们将在主 `app.js` 文件中使用它。让我们看看它是如何应用的：

#### 所有用户

```
1 angular.module('userCtrl', ['userService'])
2 .controller('all', function(User) {
3   var vm = this;
 4 
5   vm.processing = true;
 6 
7   User.all()
 8     .success(function(data) {
 9       vm.processing = false;
10       vm.users = data;
11     });
12 })
```

#### 所有用户视图 (pages/users/all.html)

```
1 <div class="page-header">
2   <h1>
3     用户 
4     <a href="/users/create" class="btn btn-default">
5       <span class="glyphicon glyphicon-plus"></span> 
6       新用户
7     </a>
8   </h1>
9 
10 </div>
11 
12 <!-- 加载消息 -->
13 <div class="jumbotron text-center" ng-show="user.processing">
14   <span class="glyphicon glyphicon-repeat"></span>
15   <p>加载用户中...</p>
16 </div>
17 
18 <table class="table table-bordered table-striped" ng-show="user.users">
19   <thead>
20     <tr>
21       <th>_id</th>
22       <th>姓名</th>
23       <th>用户名</th>
24       <th class="col-sm-2"></th>
25     </tr>
26   </thead>
27   <tbody>
28 
29     <!-- 循环用户 -->
30     <tr ng-repeat="person in user.users">
31       <td>{{ person._id }}</td>
32       <td>{{ person.name }}</td>
33       <td>{{ person.username }}</td>
34       <td class="col-sm-2">
35         <a ng-href="/users/{{ person._id }}" class="btn btn-danger">编辑</a>
36       </td>
37     </tr>
38   </tbody>
39 </table>
```





在我们的 `app.routes.js` 文件中，在 `login` 路由下方添加以下内容：

```
1 // 显示所有用户
2 .when('/users', {
3   templateUrl: 'app/views/pages/users/all.html',
4   controller: 'userController',
5   controllerAs: 'user'
6 });
```

这将使用我们刚刚创建的控制器和视图。在浏览器中访问 `http://localhost:8080/users`，你将看到我们做的所有工作整合在一起。

![所有用户](img/17-user-crm----all-users.jpg)

所有用户

另外一点需要注意的是，如果我们进入 Chrome 的网络工具并查看获取所有用户的请求，我们会看到 Angular 确实附加了我们的令牌（token）。

![访问令牌](img/17-user-crm----access-token.jpg)

访问令牌

页面上还有一件事要做的，就是提供删除用户的功能。

## 删除用户

我们需要两个东西来添加删除功能：

1.  控制器中的一个函数
2.  视图中的一个按钮

让我们先创建函数。在我们的 `userCtrl.js` 中，添加该函数：

```
 1 // 删除用户的函数
 2 vm.deleteUser = function(id) {
 3   vm.processing = true;
 4 
 5   // 用户 id 作为参数
 6   User.delete(id)
 7     .success(function(data) {
 8 
 9       // 获取所有用户以更新表格
10       // 你也可以设置 api 
11       // 在删除调用时返回用户列表
12       User.all()
13         .success(function(data) {
14           vm.processing = false;
15           vm.users = data;
16         });
17 
18     });
19 };
```

此 `deleteUser` 函数将调用 `User` factory 中的删除函数。当调用成功时，我们将进行调用来获取所有用户，然后更新 `users` 对象，反过来更新我们的表格。

现在只需要在视图中有一个删除按钮。在 `views/pages/users/all.html` 的用户表格中，紧邻编辑按钮添加以下内容：

```
1 <a href="#" 
2   ng-click="user.deleteUser(person._id)" 
3   class="btn btn-primary">Delete</a>
```

我们传递了 `person._id`，并且得益于 `ngClick` Angular 指令，点击此按钮时我们将调用 `deleteUser` 函数。

现在当我们点击删除时，用户将被删除，我们的表格将得到更新。接下来，让我们制作**创建用户**组件。

## 创建用户

与列出所有用户的页面一样，我们需要为创建用户页面准备**控制器**、**路由**和**视图**。

### 创建控制器

我们将在 `userCtrl.js` 文件中第一个创建的控制器下方添加一个控制器。我们将此命名为 `userCreateController`。

```
 1 // 应用于创建页面的控制器
 2 .controller('userCreateController', function(User) {
 3   
 4   var vm = this;
 5 
 6   // 用于隐藏/显示视图元素的变量
 7   // 区分创建或编辑页面
 8   vm.type = 'create';
 9 
10   // 创建用户的函数
 11   vm.saveUser = function() {
 12     vm.processing = true;
 13 
 14     // 清空消息
 15     vm.message = '';
 16 
 17     // 使用 userService 中的创建函数
 18     User.create(vm.userData)
 19       .success(function(data) {
 20         vm.processing = false;
 21 
 22         // 清空表单
 23         vm.userData = {};
 24         vm.message = data.message;
 25       });
 26       
 27   };  
 28 
 29 )
```

这对我们来说已经是非常标准的流程了。我们有一个名为 `saveUser` 的函数将用于视图中的表单。我们还调用了 `userService` 中的 `User.create()` 函数。创建用户后，我们将显示消息并清空表单，这样就可以输入新用户。

我们将整个 `userData` 对象传递到创建用户函数中，它包括：

```
1 // 所有信息都使用 ng-model 绑定到我们的表单
2 {
3   name: "Holly",
4   username: "hollylawly",
5   password: "supersecret"
6 }
```

这里的另一个添加是 `type` 变量。它将用于我们的视图。由于我们在创建页面和编辑页面都使用同一个文件 (`views/pages/users/single.html`)，我们需要一种方法来区分它们。当然，你可以为这些页面创建两个独立的视图文件，但视图中只有 2 处微小差异。通过这种方式，我们消除了一些重复代码。

### 创建用户路由

```
1 // 创建新用户的表单
2 // 相同的视图
3 .when('/users/create', {
4   templateUrl: 'app/views/users/single.html',
5   controller: 'userCreateController',
6   controllerAs: 'user'


### 创建用户视图 (pages/users/single.html)

```
1 <div class="page-header">
2   <h1 ng-if="user.type == 'create'">创建用户</h1>
3   <h1 ng-if="user.type == 'edit'">编辑用户</h1>
4 </div>
5 6 <form class="form-horizontal" ng-submit="user.saveUser()">
7   <div class="form-group">
8     <label class="col-sm-2">名称</label>
9     <div class="col-sm-6">
10      <input type="text" class="form-control" ng-model="user.userData.name">
11    </div>
12  </div>
13  <div class="form-group">
14    <label class="col-sm-2">用户名</label>
15    <div class="col-sm-6">
16      <input type="text" class="form-control" ng-model="user.userData.username">
17    </div>
18  </div>
19  <div class="form-group">
20    <label class="col-sm-2">密码</label>
21    <div class="col-sm-6">
22      <input type="password" class="form-control" ng-model="user.userData.password">
23    </div>
24  </div>
25  
26  <div class="col-sm-6 col-offset-2">
27    <button type="submit" class="btn btn-success btn-block" ng-if="user.type == 'create'">创建用户</button>
28    <button type="submit" class="btn btn-success btn-block" ng-if="user.type == 'edit'">更新用户</button>
29  </div>
30 </form>
31 
32 <div class="row show-hide-message" ng-show="user.message">
33   <div class="col-sm-6 col-offset-2">
34     
35     <div class="alert alert-info">
36       {{ user.message }}
37     </div>
38   </div>
39 </div>
```

这对我们来说已经是非常标准的流程了。我们有一个名为 `saveUser` 的函数将用于视图中的表单。我们还调用了 `userService` 中的 `User.create()` 函数。创建用户后，我们将显示消息并清空表单，这样就可以输入新用户。

我们将整个 `userData` 对象传递到创建用户函数中，它包括：

```
1 // 所有信息都使用 ng-model 绑定到我们的表单
2 {
3   name: "Holly",
4   username: "hollylawly",
5   password: "supersecret"
6 }
```

这里的另一个添加是 `type` 变量。它将用于我们的视图。由于我们在创建页面和编辑页面都使用同一个文件 (`views/pages/users/single.html`)，我们需要一种方法来区分它们。当然，你可以为这些页面创建两个独立的视图文件，但视图中只有 2 处微小差异。通过这种方式，我们消除了一些重复代码。

### 编辑用户

让我们运行编辑用户页面。我们将与创建用户页面使用相同的视图。唯一的区别是：

*   我们必须将参数传递到 URL (/users/user_id)
*   我们需要在页面加载时获取用户信息
*   我们需要将这些信息绑定到我们的表单

### 编辑用户控制器

由于我们通过 URL 传递用户 ID，我们需要注入 Angular 的 `$routeParams` 模块来获取 URL 参数。

根据路由文件中命名的方式，我们将知道特定参数的名称。在本例中，我们获取的是 `$routeParams.user_id`。





```
 1 // 应用于用户编辑页面的控制器
 2 .controller('userEditController', function($routeParams, User) {
 3 
 4   var vm = this;
 5 
 6   // 用于显示/隐藏视图元素的变量
 7   // 用于创建或编辑页面
 8   vm.type = 'edit';
 9 
10   // 获取要编辑的用户数据
11   // $routeParams 是我们从 URL 获取数据的方式
12   User.get($routeParams.user_id)
13     .success(function(data) {
14       vm.userData = data;
15     });
16 
17   // 保存用户的函数
18   vm.saveUser = function() {
19     vm.processing = true;
20     vm.message = '';
21 
22     // 调用 userService 函数进行更新 
23     User.update($routeParams.user_id, vm.userData)  24       .success(function(data) {
25         vm.processing = false;
26 
27         // 清空表单
28         vm.userData = {};
29 
30         // 将 API 传的消息绑定到 vm.message
31         vm.message = data.message;
32       });
33   };
34 
35 });
```

当编辑用户页面加载时，我们将使用 `User.get()` 函数来获取该用户的数据。这将访问我们的 API 并获取用户信息。然后，我们将该对象绑定到 `vm.userData`。

由于 `userData` 是我们在 `/views/pages/users/single.html` 中使用的对象，因此我们的表单将自动填充这些数据！

### 编辑用户路由

这是我们定义参数名称的地方。我们在这里传递 `:user_id`，这让 `$routeParams` 知道 `$routeParams.user_id` 存在我们刚刚创建的控制器中。

```
1 // 编辑用户的页面
2 .when('/users/:user_id', {
3   templateUrl: 'app/views/pages/users/single.html',
4   controller: 'userEditController',
5   controllerAs: 'user'
6 });
```

### 编辑用户视图 (pages/users/single.html)

```
 1 <div class="page-header">
 2   <h1 ng-if="user.type == 'create'">创建用户</h1>
 3   <h1 ng-if="user.type == 'edit'">编辑用户</h1>
 4 </div>
 5 
6 <form class="form-horizontal" ng-submit="user.saveUser()">
 7   
 8   <div class="form-group">
 9     <label class="col-sm-2 control-label">姓名</label>
10     <div class="col-sm-6">
11       <input type="text" 
12         class="form-control" 
13         ng-model="user.userData.name">
14     </div>
15   </</div>
 16 
 17   <div class="form-group">
 18     <label class="col-sm-2 control-label">用户名</label>
19     <div class="col-sm-6">
20       <input type="text" 
21         class="form-control" 
22         ng-model="user.userData.username">
23     </div>
24   </</div>
 25 
 26   <div class="form-group">
 27     <label class="col-sm-2 control-label">密码</label>
28     <div class="col-sm-6">
29       <input type="password" 
30         class="form-control" 
31         ng-model="user.userData.password">
32     </div>
33   </</div>
 34   
 35   <div class="form-group">
 36   <div class="col-sm-offset-2 col-sm-6">
37     <button type="submit" 
38       class="btn btn-success btn-lg btn-block" 
39       ng-if="user.type == 'create'">创建用户</button>
40     <button type="submit" 
41       class="btn btn-success btn-lg btn-block" 
42       ng-if="user.type == 'edit'">更新用户</button>
43   </</div>
 44   </</div>
 45 
 46 </form>
 47 
48 <div class="row show-hide-message" ng-show="user.message">
49   <div class="col-sm-6 col-sm-offset-2">
50     
51     <div class="alert alert-info">
52       {{ user.message }}
53     </div>
54     
55   </</div>
56 </div>
```

此视图与创建用户页面完全相同。这里的很妙之处在于，由于我们的输入框绑定到 `userData` 对象，并且我们在控制器中执行了获取数据的调用，用户信息将自动显示在表单中。

![编辑用户](img/17-user-crm----edit-user.jpg)

### 编辑用户

出于安全考虑，我们的密码不会显示，因为 API 不返回该数据。

### 为消息添加动画

由于我们已经在 `index.html` 文件中通过 CDN 引入了 [animate.css](http://daneden.github.io/animate.css/)，我们可以使用它的类来为 Angular 指令添加动画。

我们只需要添加一些自定义 CSS。我们将使用 `animate.css` 类让消息产生缩放效果。

```
1 /* 动画
2 ====================== */
3 
4 /* 显示与隐藏 */
5 .show-hide-message.ng-hide-remove {
6   -webkit-animation:zoomIn 0.3s both ease;
7   -moz-animation:zoomIn 0.3s both ease;
8   animation:zoomIn 0.3s both ease;
9 }
```

为 `ngShow` 和 `ngHide` 指令添加动画类类 `.ng-hide-remove`。

## 总结

我们现在拥有了所有用户。通过将此方法应用于许多类型，我们可以看到应用程序是如何整合在一起的。

### 流程回顾

上述步骤回顾了我们在整本书中所采取的步骤。将其拆分为 6 个要点时，看起来并不复杂，但执行所有操作都需要大量的知识。




再次强调，这是一种针对大型应用程序的更高级的方法。对于我们的演示，我们一直使用的这种结构已经足够了。但请记住这一点，因为随着应用程序的增长，可能值得研究一下这种结构。

***

熟能生巧，你创建的 MEAN 应用越多，这些概念在你脑海中就会巩得越稳固。

## 下一步计划

我们已经完成了 MEAN 栈应用程序，但仍然有很多东西需要学习。接下来我们需要做的一件事是部署我们的网站，这样其他人就可以在网上查看了。毕竟，如果我们不能展示出来，做这些工作又有什么用呢？让我们来看看如何将我们出色的新网站部署到网上。

## 部署 MEAN 应用

到目前为止，我们一直在电脑的本地上构建所有这些应用程序。我们一直在创建文件，得益于 `Node` 和 `Express` 启动了服务器，并在 `http://localhost:8080` 上进行测试。

我们创建的伟大作品将无法被世界上其他地方看到！我们需要将应用程序部署到某些托管服务，以便我们能通过网站访问它。

将网站部署到在线服务器有许多方法。对于我们的目的，最好寻找一个专门托管 `Node` 应用程序的在线主机。

目前，最流行的服务器配置是 LAMP 栈（Linux, Apache, MySQL 和 PHP）。由于我们使用 `Node` 代替 `Apache`，用 `MongoDB` 代替 `MySQL`，并用 `Node` 代替 `PHP`，因此寻找一个专门从事此类服务的主机是合理的。

### 优秀的 Node 托管主机

这些托管主机都提供了极佳的功能，是部署应用程序的好选择。

[Modulus](https://modulus.io/) - 我们在某些章节中使用 `Modulus` 来托管 `MongoDB` 数据库。他们还提供优秀的 `Node` 托管服务，并拥有良好的支持。

[Digital Ocean](https://www.digitalocean.com/) - Digital Ocean 是 VPS（虚拟专用服务器）提供商，因此你需要负责配置和设置自己的服务器。Digital Ocean 提供 `SSH` 访问和每月 5 美元起的方案。他们还提供服务器镜像，只需点击按钮即可安装 `Node` 环境。

[Heroku](https://www.heroku.com/) - 我们个人托管 `Node` 应用的最喜喜。部署 Heroku 应用非常简单，他们提供的命令行工具非常易上手。他们还允许你免费托管较小的应用，尽管对支持的流量量有限制。

#### 其他提及

这些主机声誉良好，但我们尚未亲自使用过：

*   [Joyent](https://www.joyent.com/) - `Node` 的创建者提供可扩展定价的优质云计算选项。
*   [Nodejitsu](https://www.nodejitsu.com/) - 由一些 `Node` 早期贡献者创建的易用托管解决方案。

Heroku 在价格、功能、支持、可用性和可用工具之间提供了极好的平衡。我们将查看如何将 MEAN 栈应用部署到 `Heroku`。这个过程与其他主机类似，这些技术可以适用于大多数主机。

### 部署到 Heroku

Heroku 以让服务器配置变得简单且无痛苦而闻名。它让我们构建得更快，并专注于应用程序的细节，而不是尝试配置自己的服务器。

我们将部署在整个整本书中一直在编写的完整 MEAN 栈应用程序——我们的用户 CRM 系统。部署是一个相当轻松的过程，几分钟内我们就能在网上拥有我们的完整应用程序。

让我们开始吧。

#### 创建 Heroku 账户

前往 [Heroku.com](https://heroku.com) 并创建你的免费账户。如你所见，仪表板极其简单且用户友好。它为我们提供了非常棒的**入门 Heroku** 对话框，我们可以在那里找到部署每种类型应用的指令说明。

![Heroku Dashboard](img/18-mean-deployment----01-heroku-dashboard.jpg)
Heroku 仪表板

我们将逐步介绍 Heroku 的 [Node 部署指南](https://devcenter.heroku.com/articles/getting-started-with-nodejs)。你可以跟随这本书学习，并在将来参考该链接，因为他们提供了大量的部署场景。

#### 所需工具

你需要准备几样东西来开始部署：

*   [Node and npm](http://nodejs.org/)（很确定你已经安装了这个）
*   [Heroku Toolbelt](https://toolbelt.heroku.com/)
*   [Git](http://git-scm.com/)

### Git 仓库

首先，我们需要将应用程序转换为 git 仓库。首先，我们将创建一个本地 git 仓库，然后让 git 远程仓库指向 Heroku。这样之后，我们就拥有了直接推送到 Heroku 的能力。

*如果你已经为项目使用了 git 仓库并在 GitHub 或 BitBucket 上工作，那太棒了！你已经拥有 git 仓库，可以跳过此步。*

要创建本地 git 仓库，请确保你已安装 [git](http://git-scm.com/) 并且能够在控制台中访问 `git` 命令。

`cd` 进入你的项目目录并输入以下命令来创建 git 仓库：

```bash
git init
```

这将创建你的 git 仓库。现在，我们需要将文件添加到仓库并提交它们。

```bash
git add .
```

```bash
git commit -m 'adding first files'
```

![Git Repo Creation](img/18-mean-deployment----git-repo.jpg)
创建 Git 仓库

现在我们的 git 仓库准备就绪，可以进入 Heroku 部分。

#### Heroku 工具带 (Toolbelt)

这个 Toolbelt 将为我们提供部署所需的工具。

![Heroku Toolbelt](img/18-mean-deployment----01-dashboard.jpg)

安装 Toolbelt 后，我们就可以使用 `heroku` 命令。进入命令行并输入：

```bash
heroku
```

![Heroku Command](img/18-mean-deployment----02-installed.jpg)
Heroku 命令

现在你可以看到可以使用的所有命令。我们在部署到 Heroku 时将使用其中几个。第一个就是登录。

#### 登录 Heroku

这是我们将桌面连接到 Heroku 的方式。我们将命令行进行验证，以便 Heroku 知道我们有权发送应用。这是一个非常简单的过程。

输入：

```bash
heroku login
```

![Heroku Login](img/18-mean-deployment----03-heroku-login.jpg)
登录 Heroku

我们将进行验证，Heroku 还会要求你上传 SSH 密钥。由于我已经在 Heroku 上有了 SSH 密钥，它没有提示我。现在让我们开始构建一个简单的应用。

### 部署我们的 User CRM 应用

我们将创建的 User CRM 应用部署到 Heroku，这样我们就能看到如何让 MEAN 应用上线。

这是一个非常简单的过程。在 git 仓库目录内，我们执行以下步骤：

1. 创建远程仓库（与我们的主 `origin` 远程仓库不同），以便我们的应用程序知道将代码推送到哪里
2. 推送仓库！

让我们创建远程仓库：

```bash
heroku create
```

![Heroku Create](img/18-mean-deployment----05-heroku-create.jpg)
创建 Heroku

##### Heroku 警告

Heroku 这里关于更新 Git 的警告是不准确的。他们的博客建议更新到 1.9.5 版本，这正是我们在这里使用的版本。我们已经联系对方解决这个问题，并在本章中更新相关信息。

继续进行吧，因为这个警告不会影响我们使用 git 或 Heroku Toolbelt。

***

现在我们可以通过输入 git 命令看到我们的远程仓库已创建：

```bash
git remote -v
```

![Git Remotes](img/18-mean-deployment----git-remote.jpg)
Git 远程仓库




`heroku create` 命令会为我们的应用程序创建一个随机名称，在此例情况下，为 `fathomless-stream-3632`。这意味着我们的应用程序很快就能通过 `http://fathomless-stream-3632.herokuapp.com` 访问。

这并不十分理想，所以让我们将其重命名为 `user-crm`。我们可以通过 `heroku apps` 命令查看已创建的应用。然后我们对其进行重命名。

```
1 $ heroku apps:rename user-crm --app fathomless-stream-3632
```

如果我们想要的应用程序名称已被占用（由于我们在本书中使用 `user-crm`，所以它是被占用的），我们就必须更改名称或在末尾添加一些数字。让我们在名称末尾添加 `123`。

```
1 $ heroku apps:rename user-crm-123 --app fathomless-stream-3632
```

你也可以通过从开始就为应用程序命名来跳过所有这些重命名操作：

```
1 $ heroku create user-crm
```

最终，当你想让应用程序上线时，你可能不希望人们通过 `http://xxxx.herokuapp.com` 访问。Heroku 提供了一种简单的方法，将你拥有的任何域名指向此应用程序，所以不用担心。我们将在在本章稍后重新讨论如何将域名指向我们的 Heroku 应用。

![Image](img/18-mean-deployment----06-heroku-rename.jpg)

图片

## 部署代码

现在我们已经准备就绪，我们将把网站部署到 Heroku！这只需要一个简单的 git 命令。我们本质上是在把所有本地 git 仓库代码推送到由 Heroku 托管的远程仓库。

```
1 $ git push heroku master
```

这告诉 git 我们想要推送到新创建的 `heroku` 仓库和 `master` 分支（这是自动自动创建的默认 git 分支）。

![Heroku Deploy](img/18-mean-deployment----07-heroku-deploy.jpg)

Heroku Deploy

我们可以看到 Heroku 在部署我们的应用程序时会执行很多工作。它看到我们有一个基于 Node 的应用程序。然后它将通过读取我们的 `package.json` 文件来添加依赖项。它还将通过运行 `package.json` 文件中声明为 `main` 的文件来启动我们的 Node 服务器。在我们的情况下，该文件是 `server.js`。

## 确保运行一个实例

我们想要确保应用程序正在运行，并且 Heroku 已为我们启动了服务器（称为 dynos）。输入以下内容进行确认：

```
1 $ heroku ps:scale web=1
```

如果我们进入仪表板，我们可以在 `Dynos` 部分看到，我们有一个 dyno，而且它是免费层级。你可以通过编辑使用的 dynos 数量来快速扩展或缩小应用程序。

![Heroku Dynos](img/18-mean-deployment----heroku-dynos.jpg)

Heroku Dynos

我们的应用程序现在已准备好查看了！

### 在浏览器中查看我们的应用程序

我们终于到了自从书开始以来一直期待的部分！在浏览器中看到我们的全栈 MEAN ！

如果你还记得 Heroku 为你生成的那个疯狂的随机名称，或者你自己重命名了应用，请在浏览器中访问该地址：

[`user-crm.herokuapp.com/`](https://user-crm.herokuapp.com/)

Heroku 还提供了一个使用命令行在浏览器中打开应用程序的快捷方式：

```
1 $ heroku open
```

这太神奇了！我们在浏览器中拥有了我们一直想要的网站。

### 定义特定的运行命令

有时，我们可能有一个在 Heroku 接手我们的应用程序时想要运行的特定命令。这可以使用使用任务运行器来启动服务器，如 grunt 或 gulp（我们将在下一章介绍 gulp）。Heroku 会查看我们 `package.json` 文件中的 `main` 属性，如果我们定义了该属性，它还会查看 `scripts` 下的内容。

还有另一种方法可以准确地告诉 Heroku 我们想要看到运行的是什么命令。你可以通过在我们的项目根目录下创建一个名为 `Procfile` 的新文件来实现。

只需在你的项目根目录下创建一个 `Procfile` 并按所示定义启动命令即可：

```
1 web: node server.js
```

这告诉 Heroku 在部署到 web 平台时，应该使用此命令来启动我们的应用程序。现在当我们执行 `git push heroku master` 时，Heroku 将运行该特定命令，我们的网站就会上线。

## 使用现有的 Heroku 应用

如果你切换到另一台电脑并想要访问已经使用的 Heroku 应用，则需要采取几个步骤。这些步骤假设你是在一台新电脑上且尚未安装 Heroku。

*   下载 [Heroku Toolbelt](https://toolbelt.heroku.com/)
*   登录：`heroku login`
*   添加你的公钥：`heroku keys:add`
*   拉取你当前的应用 `heroku git:clone -a app-name`
*   进行改进
*   Git add 并 commit 你的更改
*   推回 heroku：`git push heroku master`

通过这些简单的步骤，你可以跳转到任何电脑并立即获取你当前的项目。

## 使用你自己的域名

Heroku 为应用添加域名提供了非常简单的步骤。在本例中，我们假设你有一个域名 `supercool.com`。要为应用程序添加该域名，你需要完成两件事：

1. 告诉 Heroku 哪些域名
2. 配置你的 DNS 指向 Heroku

第一部分非常简单。我们将使用以下命令告诉 Heroku 域名：

```
1 heroku domains:add www.supercool.com
```

完成该步骤后，你可能需要一些时间才能在浏览器中访问 `www.supercool.com`。这取决于不同的注册商，但通常如下所示：

| 记录 | 名称 | 目标 |
| --- | --- | --- |
| CNAME | www | user-crm.herokuapp.com |

只要你遵循这些步骤，你很快就能看到它！

有关更多信息，请访问 [Heroku 域名文档](https://devcenter.heroku.com/articles/custom-domains)。如果你感兴趣，它们提供了关于更多类型（通配符、子域名）的详细信息。它们还提供了针对几个注册商的说明。

## 总结

我们终于构建了一个 MEAN 应用程序并使其上线。从本书中学到的许多技术都可以应用于不同的应用程序和用例。无论你尝试构建什么，Heroku 都是部署应用程序/网站的快速简单方法。接下来，既然我们已经构建并部署了应用，让我们看看一些让开发过程更容易的技术。我们将研究如何使用 Gulp（任务运行器）和 Bower（前端资源管理器）。这两个工具将极大地加速我们的工作流。

## MEAN 工作流工具

### 应用

我们需要创建一个示例 MEAN 应用程序，以确切看到如何使用 Bower 和 Gulp 来帮助我们的工作流。

这是目录结构。请创建这些文件和文件夹。

```
 1 - public/
 2 ----- app/
 3 ---------- controllers/
 4 --------------- mainCtrl.js
 5 ---------- views/
 6 --------------- pages/
 7 -------------------- home.html
 8 --------------- index.html
 9 ---------- app.js
 10 ---------- app.routes.js
 11 ----- assets/
 12 ---------- css/
 13 --------------- style.less
 14 - server.js
```

这是一个 MEAN 项目，所以请运行：

```
1 $ npm init
```

以创建一个 `package.json` 文件。创建此文件时，所有的默认值都是可以。

现在我们需要 Express 作为依赖项，所以运行：

```
1 $ npm install express --save
```



现在我们有了 Express。让我们进入 `server.js` 并启动服务器来提供我们的 `index.html` 文件。

```
 1 // 获取我们的包
 2 var express = require('express');
 3 var app     = express();
 4 var path    = require('path');
 5 var port    = process.env.PORT || 8080;
 6 
 7 // 配置公共资源文件夹
 8 app.use(express.static(__dirname + '/public'));
 9 
10 // 发送 index.html 的路由
11 app.get('/', function(req, res) {
12     res.sendFile(path.join(__dirname + '/public/app/views/index.html'));
13 });
14 
15 // 启动服务器
16 app.listen(port);
17 console.log('Magic happens on http://localhost:' + port);
```

这是一个非常简单的文件，我们只需要在启动服务器之前获取依赖并提供 `index.html` 文件。

让我们快速连接其余的页面：

#### `public/app/controllers/mainCtrl.js`

```
1 angular.module('mainCtrl', [])
2 
3 .controller('mainController', function() {
4 
5   var vm = this;
6     
7   vm.message = 'this is my message!';
8   
9 });
```

#### `public/app/views/pages/home.html`

```
1 首页！
```

#### `public/app/views/index.html`

```
 1 <!DOCTYPE html>
 2 <html lang="en">
 3 <head>
 4   <meta charset="UTF-8">
 5   <title>Workflow!</title>
 6 
7   <!-- 用于 Angular 路由 -->
 8   <base href='/'>
 9 
10   <!-- CSS -->
11   <!-- 在此处加载 bootstrap -->
12   <!-- 我们将在 gulp 部分加载 css 文件 -->
13 
14   <!-- JS / 库 -->
15   <!-- 在此处加载 angular 和 angular-route -->
16 
17   <!-- APP -->
18   <script src="app/controllers/mainCtrl.js"></script>
19   <script src="app/app.routes.js"></script>
20   <script src="app/app.js"></script>
21 </head>
22 <body class="container" ng-app="myApp" ng-controller="mainController as main">
23 
24   <div class="jumbotron text-center">
25     <h1>{{ main.message }}</h1>
26   </div>
27 
28   <div ng-view></div>
29   
30 </body>
31 </html>
```

#### `public/app/app.js`

```
1 angular.module('myApp', ['app.routes', 'mainCtrl']);
```

#### `public/app/app.routes.js`

```
 1 angular.module('app.routes', ['ngRoute'])
 2 
3 .config(function($routeProvider, $locationProvider) {
4 
5   $routeProvider
 6     .when('/', {
 7       templateUrl: 'app/views/pages/home.html',
 8       controller: 'mainController',
9       controllerAs: 'main'
10     });
11 
12   $locationProvider.htmlMode(true);
13 });
```

#### `public/assets/css/style.less`

```less
1 /* 变量
 2 ====================== */
3 @blue: #6D0;
4 @purple: #993399;
5 @red: #cc3333;
6 
7 /* 主
 8 ====================== */
9 body{ 
10   background:@blue;
11   color:@purple;
12   border-top:5px solid @red;
13   padding-top:0px;
14 }
```

现在我们可以使用命令启动服务器：

```
1 nodemon server.js
```

这个应用目前没不多，因为我们还没有获取 Bootstrap 或 Angular Route。我们将使用一个名为 Bower 的工具来拉取这些资源。

### Bower

[Bower](http://bower.io/) 是一个专门用于前端资源的包管理器。你可以使用 `bower` 来引入任何 CSS/JS 库，如 Bootstrap、Angular、jQuery、Animate.css、Moment 等。Bower 的工作原理与 npm 类似，毕竟它终究是一个包管理器。就像 npm 使用 `package.json` 文件来读取所需的所有包一样，bower 使用 `bower.json` 文件。

#### 安装 Bower

我们首先需要安装 bower。幸运的是它是一个 npm 包，所以我们可以通过输入以下命令来安装：

```
npm install -g bower
```

我们使用 `-g` 全局安装 bower，以便我们可以在系统的任何地方访问它。让我们使用 `init` 命令创建一个 `bower.json` 文件。我们将保持所有默认设置。运行以下命令：

```
bower init
```

现在我们有了 bower 和 `bower.json` 文件，将能够搜索并安装包了。

#### 安装包

```
bower install <package_name> --save
```

就像 npm 一样，如果我们添加 `--save` 修饰符，包将保存到我们的 `bower.json` 文件中。

```
bower install bootstrap
```

安装完成后，Bower 会将包放在名为 `bower_components` 的文件夹中。你可以根据 GitHub URL 安装包。

```
bower install <github-url>
```

#### 搜索包

有一种方法通过命令行来搜索包。

```
bower search <package_name>
```

这种方法可能很繁琐，当有很多结果时是。更方便的搜索包的方法是通过 Bower 网站。[在 Bower 网站上搜索包](http://bower.io/search)

#### 指定目录

默认情况下，Bower 会将资源放在根目录的 `bower_components` 文件夹中。这不是放置文件的理想位置，因为我们已经决定将与应用程序关联的文件放在 `public/` 文件夹中。可以通过在项目根目录下创建一个文件来实现。该文件将命名为 `.bowerrc`，移动 `bower_components` 文件夹非常简单：

```
{
  "directory": "public/assets/libs"
}
```

现在文件将放在我们指定的目录，我们可以保持根目录更加整洁。

#### 使用包

让我们安装常用的 MEAN 栈应用程序所需的包。运行以下命令：

```
bower install bootstrap angular-route angular-animate --save
```

一旦包进入我们的项目，我们只需要链接正确的文件。通过点击你新的 `public/assets/libs` 文件夹，你能够确定具体想要哪个文件。




就像 Bower 和 Nodemon 一样，我们将全局安装 `gulp`，以便我们可以在所有项目中都访问它。

```
1 $ npm install -g gulp
```

我们还想在特定项目的 `devDependencies` 中安装 `gulp`。

```
1 $ npm install gulp --save-dev
```

太棒了！现在 Gulp 已经准备就绪，我们可以开始使用它了。首先，让我们之前创建的 LESS 文件编译为 CSS 文件，这样浏览器就可以使用它。

### 编译 LESS

我们想要做的每个任务都是一个扩展 Gulp 的 npm 包。例如，由于我们需要编译 LESS 文件，我们还需要安装 [gulp-less](https://github.com/plus3network/gulp-less)。让我们现在就安装它。

```
1 $ npm install gulp-less --save-dev
```

现在我们有了这个插件，让我们来使用它吧。像 Bower 和 npm 一样，我们需要在文档根目录下创建一个配置文件。此文件将告诉 Gulp 在我们启动时具体要做什么。

首先，我们需要在文档根目录下创建一个 `gulpfile.js`。

在我们的 `gulpfile.js` 内部，让我们开始使用 LESS：

```
 1 // load the plugins
 2 var gulp = require('gulp');
 3 var less = require('gulp-less');
 4 
 5 // define a task called css
 6 gulp.task('css', function() {
 7 
 8 // grab the less file, process the LESS, save to style.css
 9   return gulp.src('public/assets/css/style.less')
10     .pipe(less())
11     .pipe(gulp.dest('public/assets/css'));
12 
13 });
```

恭喜！你刚刚完成了第一个 Gulp 任务！现在我们只需要回到命令行并输入：

```
1 $ gulp css
```

这告诉 Gulp 运行特定任务，然后我们可以看到新的 `style.css` 文件将在我们指定的 `gulp.dest()` 文件夹中生成。

![LESS Compiled](img/19-mean-workflow----less.jpg)

编译后的 LESS

你可以看到 LESS 正如我们预期的那样被编译成了 CSS。

![LESS vs. CSS](img/19-mean-workflow----less-to-css.jpg)

LESS 对比 CSS

### 压缩 CSS

Gulp 的强大之处在于，我们可以在一个任务中通过多个包处理一个文件（或多个文件）。让我们看看如何添加 CSS 压缩功能，这样我们就可以有一个 `style.min.css` 用于生产环境。

首先安装 [gulp-minify-css](https://www.npmjs.com/package/gulp-minify-css) 包以及名为 [gulp-rename](https://www.npmjs.com/package/gulp-rename) 的包，以便我们可以将文件重命名为 `style.min.css`：

```
1 $ npm install gulp-minify-css gulp-rename --save-dev
```

现在我们可以将其添加到 `gulpfile.js` 并在 `css` 任务中使用它。

```
 1 // load the plugins
 2 var gulp      = require('gulp');
 3 var less      = require('gulp-less');
 4 var minifyCSS = require('gulp-minify-css');
 5 var rename    = require('gulp-rename');
 4
 
 7 // define a task called css
 8 gulp.task('css', function() {
 9 
10 // grab the less file, process the LESS, save to style.css
11   return gulp.src('public/assets/css/style.less')
12     .pipe(less())
13     .pipe(minifyCSS())
14     .pipe(rename({ suffix: '.min' }))
15     .pipe(gulp.dest('public/assets/css'));
16 
17 });
```

现在当我们运行

```
1 $ gulp css
```

我们可以看到创建了一个新的 `style.min.css` 文件，并且它已经经过了 LESS 编译和压缩！现在我们可以进入 `index.html` 文件并添加新的新的 CSS 文件：

```
1 <link rel="stylesheet" href="assets/css/style.min.css">
```

所有的颜色。漂亮吗？

![Site with LESS](img/19-mean-workflow----site-with-less.jpg)

带有 LESS 的站点

### 使用 Gulp 包

使用 Gulp 包的过程与我们刚刚处理 LESS 的过程类似。

1. 安装包并使用 `--save-dev`。
2. 在你的 `gulpfile.js` 中加载插件。
3. 配置任务并使用插件！

Gulp 的配置比 Grunt 容易，但概念是相同的：安装包、加载它、然后配置。让我们转向处理 JS 的其他重要任务。

### JS 检查

确保我们的 JS 文件没有错误。这包括我们的 Node 和 Angular 文件。我们将使用一个名为 [gulp-jshint](https://www.npmjs.com/package/gulp-jshint) 的 JSHint 插件来完成此任务。

让我们安装这个新包：

```
1 $ npm install gulp-jshint --save-dev
```

现在将其引入我们的 `gulpfile.js` 并创建一个任务。

```
 1 // load the plugins
 2 var gulp = require('gulp');
 3 var less = require('gulp-less');
 4 
 5 // define a task called css
 6 gulp.task('css', function() {
 7 
 8 // grab the less file, process the LESS, save to style.css
 9   return gulp.src('public/assets/css/style.less')
10     .pipe(less())
11     .pipe(gulp.dest('public/assets/css'));
12 
13 });
```

### JS 的压缩与合并

随着我们的应用程序开始增长，会有更多的请求会拖慢应用程序的性能。我们将使用两个包来压缩和合并（打包）我们的 JS 文件，这样我们只需要加载一个文件。

### 压缩 Angular

但是当压缩 Angular 文件时存在一个问题。Angular 文件必须以特定的方式声明，否则压缩过程会破坏它们。

#### 用于压缩的 Angular 模块声明方法

到本书为止，为了简单起见，我们采用了更简单的方法来定义模块。它看起来如下：





```javascript
angular.module('myApp', ['ngRoute'])
.config(function($routeProvider, $locationProvider) {
  // stuff here
})
.controller('mainController', function($http) {
  // stuff here  
});
```

为了压缩（minification），声明 Angular 模块的方法如下：

```javascript
angular.module('myApp', ['ngRoute'])
.config([
  '$routeProvider', 
  '$locationProvider', 
  function($routeProvider, $locationProvider) {
    // stuff here
  }
])
.controller('mainController', ['$routeProvider', function($http) {
  // stuff here  
]);
```

从现在起，你可以随意使用上述代码并这样声明模块，尽管那种语法写起来很麻烦。不过，还有另一种压缩 Angular 文件的方法，它涉及到 Gulp 和另一个 Gulp 包。

## 使用 Gulp 准备 Angular 压缩

Gulp 有一个专门为此目的的包，叫做 [gulp-ng-annotate](https://www.npmjs.com/package/gulp-ng-annotate)。

让我们来安装这个包：

```bash
$ npm install gulp-ng-annotate --save-dev
```

现在我们可以在 `gulpfile.js` 中使用该包并创建一个新任务：

```javascript
var ngAnnotate = require('gulp-ng-annotate');

// 用于检查、压缩并合并前端 angular 文件的任务
gulp.task('angular', function() {
  return gulp.src(['public/app/*.js', 'public/app/**/*.js'])
    .pipe(jshint())
    .pipe(jshint.reporter('default'))
    .pipe(ngAnnotate())
    .pipe(concat('app.js'))
    .pipe(uglify())
    .pipe(gulp.dest('public/dist'));
});
```

现在可以运行：

```bash
$ gulp angular
```

我们将看到创建了新的 `app.js`，其中包含了正确版本的 Angular 文件。

![ng-annotate](img/19-mean-workflow----ng-annotate.jpg)

ng-annotate

## 监听变化

接下来，我们将自动化 Gulp，这样我们就不用在每次修改文件时进入命令行并输入 `gulp <task_name>` 了。

监听文件的任务是 Gulp 内置的，因此这里不需要安装包。但需要注意的是，有一个包用于更复杂的设置，即有许多文件需要监听；那个包叫做 [gulp-watch](https://www.npmjs.com/package/gulp-watch)。

让我们进入 `gulpfile.js` 并设置它监听特定文件。我们还会告诉 Gulp 在检测到文件变化时运行哪些任务。

```javascript
gulp.task('watch', function() {
  // 监听 less 文件并运行 css 任务
  gulp.watch('public/assets/css/style.less', ['css']);

  // 监听 js 文件并运行 lint、js 和 angular 任务
  gulp.watch(['server.js', 'public/app/*.js', 'public/app/**/*.js'], ['js', 'angular']);
});
```

我们定义了一个要监听的 CSS 文件以及要运行的任务（我们之前创建的那个）。现在，当我们更新 `style.less` 文件时，可以看到 Gulp 自动更新新的 `style.min.css`。

![Gulp Watch](img/19-mean-workflow----gulp-watch.jpg)

Gulp Watch

速度极快！

## 启动 Node 服务器

我们也可以使用 Gulp 来启动服务器。它将直接使用 nodemon，但通过输入一个命令 `gulp` 就能启动整个应用程序，感觉挺酷的。

这里需要的包是 [gulp-nodemon](https://www.npmjs.com/package/gulp-nodemon)。让我们安装它：

```bash
$ npm install gulp-nodemon --save-dev
```

配置这个包与我们习惯的有点不同。我们需要定义一些内容，例如启动文件（`server.js`）、监听的文件类型（`js less html`）以及要运行的任务。

```javascript
var nodemon = require('gulp-nodemon');

// nodemon 任务
gulp.task('nodemon', function() {
  nodemon({
    script: 'server.js',
    ext: 'js less html'
  })
    .on('start', ['watch'])
    .on('change', ['watch'])
    .on('restart', function() {
      console.log('Restarted!');
    });
});

// 定义默认 gulp 任务
gulp.task('default', ['nodemon']);
```

注意我们是如何定义启动文件和监听扩展名的。我们还定义了在服务器启动和变化时运行的任务（在此例情况下为 `watch`）。

我们还定义了一个名为 `default` 的任务，这是 Gulp 首次会自动查找的任务。

现在我们可以用以下命令运行任务了：

```bash
$ gulp
```

我们可以看到服务器启动以及 Gulp 正在监听任何文件。当文件发生变化时，Gulp 将运行相应的任务然后重启服务器！

![Gulp Nodemon](img/19-mean-workflow----nodemon.jpg)

Gulp Nodemon

我们所有的优秀开发工具现在都集成到了这个 `gulpfile.js` 中，我们成了更高效的开发者！还有很多很棒的 Gulp 插件可以查看，尽情尝试其他插件，如 [imagemin](https://www.npmjs.com/package/gulp-imagemin) 和 [clean](https://www.npmjs.com/package/gulp-clean)吧。

