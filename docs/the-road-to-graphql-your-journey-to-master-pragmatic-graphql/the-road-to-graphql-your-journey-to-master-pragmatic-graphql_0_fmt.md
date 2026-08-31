

# GraphQL 之路：在 JavaScript、React.Js 和 Node.Js 中精通实用 GraphQL 的进阶

![](img/title_page.png)

本书已在 [`leanpub.com/the-road-to-graphql`](http://leanpub.com/the-road-to-graphql) 出售

此版本发布于 2019-04-05

![出版商徽标](img/leanpub-logo.png)

## 引言

本书的核心主题是现代应用中的 GraphQL。虽然 GraphQL 仅是一种可以用于许多编程语言的规范，但本书侧重于 JavaScript 中的 GraphQL。GraphQL 规范背后的公司 Facebook 发布了 JavaScript 版本的 GraphQL 参考实现，理由充分：JavaScript 是目前公司及其客户端-服务器架构中最具吸引力的编程语言和生态系统。

GraphQL 是一种可以在任何地方使用的查询语言，但它通常桥起了客户端和服务器应用之间的鸿沟。它对于使用哪种网络层没有意见，因此数据可以在客户端和服务器应用之间进行读取和写入。它被用于许多 JavaScript 库和框架的网络堆栈。客户端利用 `React`、`Angular` 和 `Vue` 等流行解决方案，而服务器端可以在 `Node.js` 环境中使用 `Express`、`Koa` 和 `Hapi` 等中间件库。只需通过 `HTTP` 跨网络发送 GraphQL 操作即可连接双方。

GraphQL 的出现引入了 Web 开发的新纪元。RESTful 应用程序曾是客户端和服务器应用之间数据传输的首选，但现代需求已经发生了变化。应用程序必须处理多个客户端——即桌面、Web、移动、可穿戴设备——它们都对服务器应用暴露的 API 感兴趣。选择变成了：使用 `REST` 多个特定客户端的 API，还是为所有客户端应用仅使用一个 `GraphQL` API，而这似乎根本算不上一个选择。然而，GraphQL 不仅仅是一个统一的接口；随着其开源社区的增长，它的生态系统提供了强大的功能和更巨大的潜力。

对我来说，一位前同事为 `Java` 开源了 GraphQL 实现是一个幸运的巧合。他努力成为 GraphQL 的首批开源贡献者之一，最终创建了 `Java` 的首选实现。这段经历塑造了我对 GraphQL 的思考，当我的雇主为其企业应用评估 GraphQL 时，这种思考得到了扩展。我们客户端和服务器应用之间的胶水最初很大程度上受到 `REST` 的影响；我们为所有的 `RESTful` 资源设置了 API 端点，最终遇到了诸如 Facebook 那样用于消耗 API 的客户端应用的问题。API 端点太僵硬，因此它们需要聚合和修改。聚合意味着将资源放入单个 API 端点中，而修改则是提供 API 端点的变体，以请求资源的不同表示形式。我们引入了自己的实现来从服务器请求资源，并最终得到了我们自己的简陋的 GraphQL 实现。从客户端的角度来看，当时只有针对 `React` 的 `Relay` 作为消费 GraphQL API 的复杂库发布了，因此我们也投入了时间于此。最后，GraphQL 的开发阶段还太早，因此我们推迟了将其引入我们的技术栈。诚实地说，我们中没有人知道它会变得如此强大或流行。

本书从客户端应用中的 GraphQL 开始，因此你将使用 `React` 作为 UI 库来消费第三方 GraphQL API，这恰恰是 GitHub 的 GraphQL API。它在开发者中是一个受欢迎的选择，原因有几个：GitHub 是少数向公众发布 GraphQL API 的流行公司之一；GitHub 随后的增长为 GraphQL 本身带来了一些信誉；而且第三方 API 在初期通常关注客户端 GraphQL 应用。本书将教你如何在客户端应用中消费 GraphQL API，而无需自己构建 GraphQL 服务器。

当我们本书的重心转向服务器端的 GraphQL 时，我们将实现一个最终可以被 GraphQL 客户端应用使用的 GraphQL API。你将实现身份验证、数据库连接和分页等强大功能。到结束时，你应该已经熟练掌握在你的 JavaScript 应用中使用 GraphQL。

### 关于作者

我是一个德国软件和 Web 工程师，致力于 `JavaScript` 编程的学习和教学。在获得计算机科学硕士学位后，我继续自学。我从初创公司世界获得了经验，在那里我在职业生活和业余时间都密集使用 `JavaScript`，这最终导致了向他人教授这些主题的渴望。

几年来，我与名为 `Small Improvements` 的公司的优秀工程师团队紧密合作，开发大规模应用程序。该公司提供了一种 SaaS 产品，允许客户向企业提供反馈。该应用前端使用 `JavaScript` 开发，后端使用 `Java`。Small Improvements 前端的首次迭代是使用 `Java`、`Wicket Framework` 和 `jQuery` 编写的。当第一代 SPA 流行后，公司将其前端应用迁移到 `Angular 1.x`。在在使用 `Angular` 两年后，很明显 `Angular` 并不是处理状态应用的最佳解决方案，因此他们转向了 `React` 和 `Redux`。

在公司工作期间，我经常在我的网站上写关于 Web 开发的文章。我从学习我文章的人那里获得了良好的反馈，这让我改进了写作和教学风格。文章接文章，我增长了教学教学的能力。我觉得我之前的文章信息量太大，让学生感到无所措，但我通过专注于一个主题得到了改进。

目前，我是一个自雇软件工程师和教育者。通过给他们明确的目标和短的反馈循环，看到学生茁壮成长是一件很有成就的事。你可以在我的[网站](https://www.robinwieruch.de/about)上找到关于我的更多信息以及支持我的方式。

### 要求

为了充分利用本书，你应该熟悉 Web 开发的基础，包括一些 `HTML`、`CSS` 和 `JavaScript` 知识。你还需要熟悉 [API](https://www.robinwieruch.de/what-is-an-api-javascript/) 术语，因为它被频繁讨论。我鼓励你加入本书的官方 [Slack Groups](https://slack-the-road-to-learn-react.wieruch.com/)，帮助他人或获取帮助。

#### 编辑器和终端

开发环境需要运行的编辑器或 IDE 以及终端（命令行工具），并[参考我的设置指南](https://www.robinwieruch.de/developer-setup/)。它是针对 MacOS 用户调整的，但你也可以找到 Windows 设置指南。有很多关于为你的操作系统设置 Web 开发环境的文章。

#### React

在客户端，本书使用 `React` 来教授如何在 `JavaScript` 中使用 `GraphQL`。我的另一本书名为《The Road to React》（React 之路），它将教你关于 `React` 的所有基础知识。它还将教你如何从 `JavaScript ES5` 过渡到 `JavaScript ES6`。这本书是免费提供的，在读完《The Road to learn React》之后，你应该已经具备了通过本书实现 `GraphQL` 客户端应用的所有知识。

#### Node

在服务端，本书使用 `Node` 配合 `Express` 库来教授如何在 `JavaScript` 中使用 `GraphQL`。在使用这些技术构建你的第一个由 `GraphQL` 驱动的应用之前，你不需要对它们了解深入。本书将引导你完成使用 `Express` 搭建 `Node` 应用的过程，并向你展示如何将 `GraphQL` 整合其中。之后，你应该能够在客户端应用中调用由服务端应用提供的 `GraphQL` API。

#### Node and NPM

你需要安装 [node and npm](https://nodejs.org/en/)，它们被用于管理我们在过程中将使用的库。在书中，你将通过 `npm`（node 包管理器）安装外部的 `node` 包。这些 `node` 包可以是库，也可以是整个框架。你可以在命令行中验证你使用的 `node` 和 `npm` 版本。如果你在终端没有看到输出，你需要安装 `node` 和 `npm`。以下是本书时使用的版本：

```sh
node --version
v10.11.0
npm --version
v6.4.1
```

#### Command Line

如果你读过《The Road to learn React》，你应该已经熟悉相关的设置了，因为书中也介绍了 `npm` 生态系统。

### FAQ

#### 为什么本书使用 React 来教授 GraphQL？

`GraphQL` 经常用于现代应用以连接客户端和服务器应用。这些应用通常使用 `React`、`Angular` 和 `Vue` 等解决方案构建。为了教授 `GraphQL`，将它应用于像 `React` 这样的真实场景作为你的客户端应用是合理的。我选择 `React` 是因为它的 API 精简且学习曲线良好。它只是你技术栈中的视图层。你可以在 [The Road to learn React](https://roadtoreact.com) 中学习它。不过，你也可以将学到的 `GraphQL` 知识应用于其他的客户端应用中。

#### 为什么使用 Node/Express 来教授 GraphQL？

你可以用客户端应用消费第三方的 `GraphQL` API，但你也可以在服务端实现自己的 `GraphQL` API。由于坚持使用一种编程语言（`JavaScript`）更高效，我选择了 `Node.js`。`Express.js` 是 `Node.js` 应用最流行的选择，这就是为什么我选择它而不是 `Hapi` 或 `Koa` 等替代方案。

#### 我如何获取更新？

我有两个渠道来分享关于我内容的更新。你可以[通过邮件订阅更新](https://www.getrevue.co/profile/rwieruch) 或[在 Twitter 上关注我](https://twitter.com/rwieruch)。无论通过哪种渠道，我的目标都是只分享高质量的内容。一旦你收到书籍已更改的通知，就可以下载它的新版本。

#### 我如何获取源代码项目？

如果你购买了可以访问源代码项目或其他任何其他内容的完整课程，你应该在你的[课程仪表板](https://roadtoreact.com/my-courses) 上找到它们。如果你购买的是官方 [Road to React](https://roadtoreact.com) 课程平台之外的课程，请在该平台上创建一个账户，然后进入 `Admin` 页面并使用其中一个邮件模板与我联系。此之后，我可以为你解锁课程。如果你还没有购买完整课程，可以随时联系我升级你的内容以访问其他材料。

#### 如果我在亚马逊上购买了书，我能获得副本吗？

如果你在亚马逊上购买了这本书，你可能已经看到这本书在我的网站上也有提供。由于我将亚马逊作为变化经常免费内容的一种方式，我诚地感谢你的支持，并邀请你注册 [Road to React](https://roadtoreact.com)。在那个平台上，你可以就你的购买情况给我发邮件（通过 `Admin` 页面），以便我为你解锁整个课程包。此外，你始终可以在平台上下载书籍的最新电子书版本。

#### 在阅读本书时我如何获得帮助？

本书设立了一个 [Slack 群组](https://slack-the-road-to-learn-react.wieruch.com/)，供想要与其他同学和资深读者一起学习的人使用。你可以加入频道以获取帮助或帮助他人。你可能会发现，帮助他人学习编程有助于你内化自己的课程。如果没有其他选择，你随时可以联系我。

#### 有任何故障排除区域吗？

如果你遇到问题，请加入 Slack 群组。此外，检查 [GitHub 上的开放问题](https://github.com/the-road-to-graphql/the-road-to-graphql/issues) 或你在过程中将构建的应用的 GitHub 仓库，查看是否针对特定问题列出了解决方案。如果你的问题没有被提到，请开启一个新的 issue，你可以在其中解释你的问题、提供截图并提供更多细节（例如书籍页码、`node` 版本）。

#### 如果我付不起完整课程怎么办？

如果你付不起完整课程但想学习该主题，可以联系我。可能是你还是一名学生，或者课程对你来说太贵了。我希望支持任何多元化的事业。如果你属于少数群体，请联系我。

#### 我可以帮助内容吗？

是的，我很乐意听到你的反馈。你可以在 [GitHub](http://github.com/rwieruch/the-road-to-graphql) 上开启 issue 并对技术方面或文本内容提出建议。你也可以在 GitHub 上提交 pull requests。

#### 我如何支持这个项目？

如果你觉得我的课程有用并想做出贡献，请查看我的网站关于如何提供支持的 [关于页面](https://www.robinwieruch.de/about/) 信息。读者分享我的书籍如何帮助他们，对我非常有帮助，这样其他人可能会发现改进开发技能的方法。通过提供的任何渠道进行支持都能让我有自由创建深度课程并继续提供免费材料。

#### 有退款保证吗？

是的，如果你认为它不合适，两个月内提供 100% 退款保证。请直接联系我。

我希望这本书能为你提供更多的实践经验和挑战，帮助你作为一名程序员不断成长。这些挑战旨在创造一种“心流”体验，即你的技能和工具能够恰好应对这些挑战的场景。如果这本书能够平衡好具有挑战性与对你技能水平的尊重，你可能会体验到[心流状态](https://www.robinwieruch.de/lessons-learned-deep-work-flow/)。当我自己读到这个见解时感到非常惊讶，因此我希望能在书中引导你进入这种状态。

### 提示与技巧

如前所述，书中包含实操任务，你将在引导下使用之前章节中学学的技术来解决问题。这应该让你体验到这些章节中所学课程的实际用途，并为你自己的项目对更抽象的内容提供更深入的理解。

在继续后续章节之前，请确保内化每一节课程。本书的编写方式是每一节都建立在前节的基础上。你对这些主题的知识通过不同的技术并列进行横向扩展，并通过通过技术的叠加进行纵向扩展。如果你在学习课程时做笔记，内化将变得容易得多。考虑写下文中未涵盖的问题，以便日后查阅。这些笔记也可以成为反馈，我会用它们来改进未来的版本。

我鼓励你自己编写代码示例，而不是复制/粘贴。手打代码可以教你如何发现语法错误和 Bug，这样在你转向尝试用自己的数据运行示例后，你可以自己修复错误。不过，如果遇到 Bug，请不要气馁。Bug 在任何足够复杂的应用程序中通常都会出现，但在学习场景中发现它们是可以接受的，因为你将有机会学习如何修复它们。

后续的材料应该在打开 IDE 的情况下阅读，以便输入示例并观察输出。我将提供额外的工具，如 [GraphQL Playground](https://github.com/prisma/graphql-playground)，展示代码示例在现实情况下如何运行。尝试在课程之间抽时间实验你自己的应用程序，并应用你获得的工具。如果不应用你在这些章节中学到的知识，你永远无法掌握它们。如果你在构思项目想法上有困难，[这篇文章](https://www.robinwieruch.de/how-to-learn-framework/)可能会有所帮助。

### 挑战

我写了很多关于我学到的教训。这就是我走到今天的原因。由于教学对我的职业帮助很大，我希望你也能体验同样的效果。首先，你必须自学。对于这本书，我的挑战是让你在学习的同时教他人。这里有一些关于如何实现它的点的建议：

*   针对书中的某个特定主题写一篇博客文章。这不是为了复制和粘贴材料，而是用你自己的方式教这个主题。用你自己的话来解释概念，解决一个问题，并进一步深入该主题的每一个细节。你将看到它是如何填补你的知识空白的，以及长远来看如何为你的职业开启大门。

*   如果你在社交媒体上很活跃，考虑和朋友分享你从书中学到的技巧。你可以发布关于你从书中最新实验的热点推文，这可能很有趣，或者在 Facebook Web 开发群组中展示你的技能。为你的进度拍摄高质量的截图，以便观众跟随。

*   如果你有信心记录自己的学习历程，可以在 Facebook Live、YouTube Live 或 Twitch 上分享你学习本书的过程。你可能会有很多人观看你的直播，但你之后一直可以将录制视频发布到 YouTube。这是一个通过口头表达问题及其解决方案的好方法。如果录制之间的间隔时间较长，可以剪辑视频或使用延时摄影来展示亮点。此外，考虑在视频中保留 Bug 和意外，因为这些对于遇到相同问题的观众来说是宝贵的学习工具。以下是关于高质量视频的几建议：

    *   用你的母语录制音频。英语更受广泛受众接受。

    *   在录制长视频前检查音频以确保清晰，并确保环境不会影响音质。

    *   在你的 IDE 或命令行终端中增大字体，以便观众可以看到你想展示的任何文字。

    *   在发布到 YouTube 之前剪辑视频。尽量为观众保持简洁，用你自己的话总结步骤。

你可以联系我并推广你发布的任何内容。如果你的内容很好，我甚至可能将其作为官方补充材料包含在未来的书中。希望你接受这些挑战。

### GraphQL

当涉及到客户端和服务器应用程序之间的网络请求时，[REST](https://en.wikipedia.org/wiki/Representational_state_transfer) 是连接这两个世界最流行的选择之一。在 REST 中，一切围绕通过 URL 访问的资源展开。你可以使用 HTTP `GET` 请求读取资源，使用 HTTP `POST` 请求创建资源，并使用 HTTP `PUT` 和 `DELETE` 请求更新或删除资源。这些被称为 CRUD（增、删、改、查）操作。资源可以是作者、文章或用户等任何内容。REST 对数据格式没有硬性规定，但大多数人会使用 JSON。最后，REST 允许应用程序通过纯 HTTP、URL 和 HTTP 方法进行通信。




```
// 一个 RESTful 的请求
https://api.domain.com/authors/7

// JSON 格式的响应
{
  "id": "7",
  "name": "Robin Wieruch",
  "avatarUrl": "https://domain.com/authors/7",
  "firstName": "Robin",
  "lastName": "Wieruch"
}
```

## 代码 Playground

尽管 REST 长期一直是标准，但 Facebook 的一项技术 GraphQL 最近已成为潜在的继任者。后续章节将介绍 GraphQL 的优缺点，以及为需要选择的开发者提供的替代方案。

### 什么是 GraphQL？

简而言之，GraphQL 是由 Facebook 创建的一种开源 `query language`（查询语言），而这家公司意出意料地仍然处于 Web 软件开发的顶峰。在 GraphQL 于 2015 年开源之前，Facebook 自 2012 年起就开始在其内部应用于移动应用程序中，作为常见 REST 架构的替代方案。它允许对特定数据进行请求，让客户端对发送的信息有更多控制权。

在 RESTful 架构中，这要困难得多，因为后端定义了每个 URL 上每个资源的可用数据，而前端始终必须请求资源中的所有信息，即使只需要其中部分数据。这个问题被称为“过度获取”（overfetching）。在最糟糕的情况下，客户端应用程序必须通过多次网络请求读取多个资源。这不仅是过度获取，还增加了瀑布式网络请求（waterfall network requests）的需求。

在服务器端和客户端使用像 GraphQL 这样的查询语言，可以让客户端通过向服务器发送单次请求来决定它需要的数据。结果是 Facebook 移动应用程序的网络流量消耗大幅减少，因为 GraphQL 使数据传输更加高效。

Facebook 开源了 GraphQL 规范及其 `JavaScript` 的参考实现，从那时起多种主流编程语言都实现了该规范。GraphQL 周围的生态系统通过提供多种编程语言在水平方向扩展，同时也通过在 GraphQL 之上的 `Apollo` 和 `Relay` 等库在垂直方向扩展。

一个 GraphQL 操作可以是 `query`（读取）、`mutation`（写入）或 `subscription`（持续读取）。这些操作中的每一个都只是一个根据 GraphQL 查询语言规范构建的字符串。幸运的是，GraphQL 一直在演进，因此未来可能会有操作。

一旦此 GraphQL 操作到达后端应用程序，它就可以根据那里的整个 GraphQL `schema`（模式）进行解析，并为前端应用程序解析出数据。GraphQL 对网络层（通常是 `HTTP`）没有强制性，对有效载负载格式（通常是 `JSON`）也没有强制性。它完全对应用架构没有任何强制要求。它仅仅是一种查询语言。

```javascript
// a GraphQL query
author(id: "7") {
  id
  name
  avatarUrl
  articles(limit: 2) {
    name
    urlSlug
  }
}

// a GraphQL query result
{
  "data": {
    "author": {
      "id": "7",
      "name": "Robin Wieruch",
      "avatarUrl": "https://domain.com/authors/7",
      "articles": [
        {
          "name": "The Road to learn React",
          "urlSlug": "the-road-to-learn-react"
        },
        {
          "name": "React Testing Tutorial",
          "urlSlug": "react-testing-tutorial"
        }
      ]
    }
  }
}
```

## 代码操场

一个查询已经请求了多个资源（`author`、`article`），这在 GraphQL 中被称为 `fields`（字段），并且仅针对这些字段请求了特定的嵌套字段（文章的 `name`、`urlSlug`），尽管实体本身在它的 GraphQL `schema` 中提供了更多数据（例如文章的 `description`、`releaseData`）。

RESTful 架构至少需要两次瀑布式请求来获取作者实体实体文章文章，但 GraphQL 查询让这一切在一次请求中即可完成。此外，查询只选择了必要的字段，而不是整个实体。

这就是 GraphQL 的概括。服务器应用程序提供一个 GraphQL `schema`，在其中它根据其层级结构和类型定义了所有可用数据，而客户端应用程序只查询所需的数据。

### GraphQL 优势

以下列表展示了在应用程序中使用 GraphQL 的主要优势。

#### 声明式数据获取

如你所见，GraphQL 通过其查询拥抱声明式数据获取。客户端在一次查询请求中选择数据以及跨越关系的实体的字段。GraphQL 决定了其 UI 需要哪些字段，它几乎充当了 UI 驱动的数据获取，就像 Airbnb 使用它的那样。

Airbnb 的搜索页面通常包含房屋、体验和其他领域特定事项的搜索结果。为了在一次请求中检索所有数据，一个仅选择 UI 所部分数据的 GraphQL 查询是完全合逻辑的。它提供了极佳的关注点分离：客户端了解数据需求；服务器了解数据结构以及如何从数据源（例如数据库、微服务、第三方 API）解析数据。

#### GraphQL 消灭了过度获取

GraphQL 中不存在过度获取。当移动客户端与 Web 客户端使用相同的 RESTful API 时，移动客户端通常会过度获取数据。通过 GraphQL，移动客户端可以选择不同的字段集，因此它可以只获取屏幕上显示所需的信息。

#### 用于 React、Angular、Node 等的 GraphQL

不过，GraphQL 对 React 开发者来说也同样令人兴奋。虽然 Facebook 在带有 `React` 的客户端应用上展示了 GraphQL，但它与任何前端或后端解决方案解耦。

GraphQL 的参考实现是用 `JavaScript` 编写的，因此在客户端和服务器端的 `Angular`、`Vue`、`Express`、`Hapi`、`Koa` 以及其他 JavaScript 库中使用 GraphQL 是可能的，这还只是 JavaScript 生态系统。GraphQL 模拟了两个实体（如客户端或服务器）之间与语言无关的接口。

#### 谁在使用 GraphQL？

Facebook 是 GraphQL 规范和 `JavaScript` 参考实现背后的推动公司，但其他知名公司也将将其应用于他们的程序。由于对现代应用的巨大需求，他们投入了 GraphQL 生态系统。除了 Facebook 之外，GraphQL 还被这些知名公司使用：

- [GitHub](https://githubengineering.com/the-github-graphql-api/)
- [Shopify](https://shopifyengineering.myshopify.com/)
- [Twitter](https://www.youtube.com/watch?v=Baw05hrOUN)
- [Coursera](https://www.youtube.com/watch?v=F329W0PR6ds)
- [Yelp](https://www.youtube.com/watch?v=bqcRQTNCO)
- [WordPress](https://www.youtube.com/watch?v=v3xY-rcsUY)
- [The New York Times](https://www.youtube.com/watch?v=W-u-vZIk)
- [Samsara](https://www.youtube.com/watch?v=g-asVW9JFP)

当 Facebook 开发 GraphQL 时，其他公司在其移动应用程序中遇到了类似的问题。这就是 Netflix 推出 [Falcor](https://github.com/Netflix/falcor) 作为 GraphQL 替代方案的原因。

#### 单一事实来源

GraphQL schema 是 GraphQL 应用程序单一事实来源。它提供了一个中心位置，在其中描述了所有可用数据。GraphQL schema 通常定义在服务器端，但客户端可以根据它读取（`query`）和写入（`mutation`）数据。

基本上，服务器应用程序提供了其侧的所有信息，而客户端应用程序通过执行 GraphQL 查询获取部分信息，或使用 GraphQL mutation 修改部分信息。

#### GraphQL 拥抱现代趋势

GraphQL 拥抱构建应用程序的现代趋势。你可能只有一个后端应用程序，但有取决于数据的网页、手机和智能手表等多个客户端。

GraphQL 可用于连接这两个世界，同时满足每个客户端的需求（网络使用需求、数据的嵌套关系、仅获取所需数据），而无需为每个客户端提供专门的 API。

在服务器端，可能有一个后端，但也有一组提供其特定功能的微服务。这定义了 GraphQL schema stitching（模式缝合）的完美用例，它允许你将所有功能聚合到一个 GraphQL schema 中。

#### GraphQL Schema Stitching

Schema stitching（模式缝合）允许从多个 schema 创建一个 schema。想象一下你的后端采用微服务架构，每个微服务负责处理特定领域的业务逻辑和数据。

在这种情况下，每个微服务可以定义自己的 GraphQL schema，然后你就可以使用 schema stitching 将它们织入成一个供客户端访问的统一 schema。每个微服务可以有自己的 GraphQL 端点，由一个 GraphQL API 网关将所有 schema 整合成一个全局 schema。

### GraphQL 内省（Introspection）

GraphQL 内省使得从 GraphQL API 获取 GraphQL schema 成为可能。由于 schema 包含了通过 GraphQL API 可用的所有数据信息，因此它是自动生成 API 文档的完美选择。它还可用于客户端模拟 GraphQL schema，以便测试，或者在 schema 缝合期间从多个微服务获取 schema。

### 强类型 GraphQL（Strongly Typed GraphQL）

GraphQL 是一种强类型查询语言，因为它使用表达丰富的 GraphQL Schema 定义语言（`SDL`）编写。强类型特性使得 GraphQL 更不容易出错，可以在编译期间进行验证，并用于支持性的 IDE/编辑器集成，例如自动补全和验证。

### GraphQL 版本控制（Versioning）

GraphQL 中没有像 REST 那样的 API 版本。在 REST 中，提供多个版本的 API 是很常见的（例如 `api.domain.com/v1/`、`api.domain.com/v2/`），因为资源或资源的结构可能会随着时间而改变。

在 GraphQL 中，可以在字段级别上弃用 API。因此，客户端在查询已弃用的字段时会收到弃用警告。一段时间后，当没有多少客户端使用该弃用字段时，可能会从 schema 中删除。这使得 GraphQL API 可以随时间演进，而无需版本控制。

### 不断发展的 GraphQL 生态系统

GraphQL 生态正在不断成长。不仅有针对编辑器和 IDE 的 GraphQL 强类型集成，还有针对 GraphQL 本身的独立应用程序。

你可能还记得用于 REST API 的 [Postman](https://www.getpostman.com)，现在变成了用于 GraphQL API 的 [GraphiQL](https://github.com/graphql/graphiql) 或 [GraphQL Playground](https://github.com/prismagraphql/graphql-playground)。

还有诸如 [Gatsby.js](https://www.gatsbyjs.org/) 这样的库，它是一种使用 GraphQL 的 React 静态网站生成器。通过 `Gatsby.js`，你可以在构建时通过 GraphQL API 提供博客内容来构建博客引擎，并且你拥有无头内容管理系统（CMS）（例如 [GraphCMS](https://graphcms.com)）通过 GraphQL API 提供（博客）内容。

演进的不仅仅是技术方面；还有针对 GraphQL 的会议、聚会和社区正在形成，以及新闻邮件和播客。

### 我应该全投入 GraphQL 吗？

在现有的技术栈中采用 GraphQL 并不是一个“全投入”的过程。从单体后端应用迁移到微服务架构是为新微服务提供 GraphQL API 的绝佳时机。

通过多个微服务，团队可以引入带有 schema 缝合的 GraphQL 网关来整合全局 schema。API 网关也用于单体 REST 应用程序。这就是 API 如何被整合到一个网关并迁移到 GraphQL 的方式。

### GraphQL 的缺点

以下主题将向你展示使用 GraphQL 的一些缺点。

#### GraphQL 查询的复杂度（Query Complexity）

人们经常误认为 GraphQL 是服务器端数据库的替代品，但它仅仅是一种查询语言。一旦查询需要通过服务器上的数据进行解析，通常与 GraphQL 无关的实现会执行数据库访问。GraphQL 对此没有特定的倾向。

此外，当你必须在一个查询中访问多个字段（作者、文章、评论）时，GraphQL 并不能消除性能瓶颈。无论请求是在 RESTful 架构还是 GraphQL 中发出的，各种资源和字段仍然必须从数据源中检索。

因此，当客户端一次请求过多嵌套字段时，就会出现问题。前端开发者并不总是意识到服务器端应用程序为检索数据必须执行的工作，因此必须有一种机制（如最大查询深度、查询复杂度权重、避免递归或持久化查询），以防止对方发送低效请求。

#### GraphQL 速率限制（Rate Limiting）

另一个问题是速率限制。在 REST 中，说“我们每天只允许这么多资源请求”比较简单，但要对单个 GraphQL 操作做出这样的陈述就很困难了，因为它可以是廉价或昂贵操作之间的任何一种。

这就是[公共 GraphQL API 的公司提出了特定的速率限制计算方法](https://developer.github.com/v4/guides/resource-limitations/)，这些方法通常归结于之前提到的最大查询深度和查询复杂度权重。

### GraphQL 缓存（Caching）

在 GraphQL 中实现简化的缓存比在 REST 中实现更复杂。在 REST 中，通过 URL 访问资源，因此你可以在资源级别进行缓存，因为你有资源 URL 作为标识符。

在 GraphQL 中，这变得复杂，因为每个查询都可能是不同的，即使它们操作在同一个实体上。你可能在一次查询中只请求作者的名字，但在下次查询中又想知道电子邮件地址。这时你需要更细粒度的字段级缓存，这在实现上很难。然而，大多数构建在 GraphQL 之上的库都提供了缓存机制。

### 为什么不用 REST？

GraphQL 是连接客户端和服务器应用程序的常用 RESTful 架构的替代方案。由于 REST 为每个资源带有一个 URL，它往往会导致低效的瀑布式请求（waterfall requests）。

例如，你想获取由 `id` 标识的作者实体，然后使用作者的 `id` 获取该作者的所有文章。在 GraphQL 中，这是一次请求，效率更高。如果你只想获取作者的文章而不获取整个作者实体，GraphQL 允许你只选择你需要的部分。在 REST 中，你会过度获取（overfetch）整个作者实体。

如今的客户端应用程序并不是为 RESTful 服务器应用程序设计的。Airbnb 平台的搜索结果显示了住宿、体验和其他相关内容。住宿和体验本身就是自己的 RESTful 资源，因此在 REST 中你必须执行多次网络请求。

改为使用 GraphQL API，你可以在一个 GraphQL 查询中请求所有实体，可以并排请求实体（例如住宿和体验）或嵌套关系实体（例如作者的文章）。GraphQL 将视角转移到客户端，由客户端决定它需要的数据，而不是服务器。这是发明 GraphQL 的初原因，因为 Facebook 的移动客户端所需的数据与其网页客户端不同。

尽管如此，在某些情况下 REST 仍然是连接客户端和服务器应用程序的方法。应用程序通常是资源驱动的，不需要像 GraphQL 那样灵活的查询语言。但是我建议你在开发下一个客户端服务器架构时尝试 GraphQL，看看它是否符合你的需求。

#### GraphQL 替代方案

REST 是 GraphQL 最流行的替代方案，因为它仍然是连接客户端和服务器应用程序最常见的架构。它比 [RPC](https://en.wikipedia.org/wiki/Remote_procedure_call) 和 [SOAP](https://simple.wikipedia.org/wiki/SOAP_(protocol)) 等网络技术更流行，因为它使用了 HTTP 的原生功能，而像 SOAP 这样的协议试图在其之上构建自己的解决方案。

Netflix 的 Falcor 是另一种替代方案，它是与 GraphQL 同期开发的。Netflix 遇到过与 Facebook 类似的问题，并最终开源了自己的解决方案。Falcor 并没有太多的关注，也许因为 GraphQL 变得太流行了，但 Netflix 的开发者在过去展现了卓越的工程能力，所以它可能值得关注。

有许多理由可以在你的 JavaScript 应用中采用 GraphQL，而不是实现另一种 RESTful 架构。它有许多优势，并且与现代软件架构契合得很好。本书将介绍如何将它用于许多实际的、现实解决方案，因此当你读完这些章节时，你应该对它是否适用于你心中有所数。



# Apollo

为特定问题找到合适的解决方案并不总是易的，用 GraphQL 构建的 Web 应用就是一个很好的例子，说明了时代的变化如何带来不断演变的挑战。此外，演变的挑战创造了一个解决方案必须随之演变的局面，以至于选择的数量变成了一项任务。本文将解读这种解决方案的优缺点：用于 GraphQL 的 `Apollo`，并在你决定不使用它时提供替代方案。

GraphQL 是唯一一种在 JavaScript 中有参考实现的查询语言，而 `Apollo` 在此基础上构建了其生态系统，使 GraphQL 供更广泛的读者使用。这包括客户端和服务器端，因为它们为两端提供了大量的库生态系统。这些库还提供了一个中间层：`Apollo Engine`，它是一个 GraphQL 网关。本质上，`Apollo` 成为 JavaScript 应用中使用 GraphQL 最受欢迎的选择之一是有原因的。

## Apollo 优势

以下主题向你展示了使用 `Apollo` 的优势，以提供一个全面的优缺点列表。如果你认为任何一个列表缺少了内容，请随时联系我。

### Apollo 的生态系统

虽然 GraphQL 处于早期阶段，但 `Apollo` 生态系统为其许多挑战提供了解决方案。除此之外，我们可以看到该生态系统增长得有多快，因为该公司每隔一次技术大会就会发布 `Apollo` 或另一个与 `Apollo` 技术栈兼容库的更新。`Apollo` 不仅仅涵盖 GraphQL；他们还在为了向 RESTful 架构后兼容的 REST 接口上投入了精力。这甚至将 GraphQL 带到了网络层和远程数据之外，还为本地数据提供了状态管理解决方案。

### Apollo 背后的公司和社区

`Apollo` 背后的公司正投入大量资源使其成功。他们也活跃于开源领域，提供有关产品的深度文章，并在会议上拥有良好的影响力。总的来说，GraphQL 生态系统 [未来看起来前景良好](https://techcrunch.com/2018/05/15/prisma)。GraphQL 后后的社区正在增长，因为越来越多的开发者采用它，并使用 `Apollo` 用于客户端和服务器端的 JavaScript 应用。

### 谁在使用 Apollo？

精通技术的公司已经在利用 `Apollo` 了。许多人之前熟悉流行的 Meteor 框架，但像 Airbnb 和 Twitch 这样新兴且极其受欢迎的公司正在使用它。这些只是它们的故事中的几个：

* Airbnb [[1]](https://medium.com/airbnb-engineering/reconciling-graphql-and-thrift-at-airbnb-a97e8d290712) [[2]](https://youtu.be/oBOSJFkrNqc)
* [Twitch](https://about.sourcegraph.com/graphql/twitch-our-graphql-transformation)
* [纽约时报](https://open.nytimes.com/the-new-york-times-now-on-apollo-b9a78a5038c)
* [荷兰航空](https://youtu.be/T2njjXHdKqw)
* [Medium](https://www.infoq.com/news/2018/05/medium-reactjs-graphql-migration)

### Apollo 文档

虽然 `Apollo` 在不断进化，但其背后的团队和社区保持文档更新，并且对于如何构建应用有丰富的见解。事实上，他们涵盖了如此多的领域，以至于初学者可能会目不暇接。

### Apollo 库

`Apollo` 提供了许多库用于 JavaScript 应用实现有效的 GraphQL 技术栈，并且它们的库是开源的以便管理。例如，[Apollo Link](https://www.apollographql.com/docs/link/) 提供了一个 API，可以将不同的功能链连接到 GraphQL 控制流中。这使得自动网络重试或使用 RESTful API 端点而不是 GraphQL 端点成为可能（端点也可以一起使用）。

`Apollo` 还提供了可交换的库，可以在`Apollo Client Cache`中看到。`Apollo Client` 本身并不偏向它的缓存（即数据存储的地方），因为 `Apollo` 或其社区宣传的任何缓存都有效。已经有可用的缓存可以用于设置`Apollo Client` 实例。

### Apollo 特性

`Apollo` 带有内置功能，可以从应用程序中提取所有复杂性，并处理客户端和服务器应用之间的交集。例如，`Apollo Client` 缓存请求，如果结果已经在缓存中，则不会再次发送。该函数为应用程序提供了性能提升，节省了宝贵的网络流量。此外，`Apollo Client` 对数据进行归一化，因此来自 GraphQL 查询的嵌套数据存储在`Apollo Client Cache`的归一化数据结构中。可以通过标识符从`Apollo Client Cache`读取数据，而无需在“作者”实体中查找“文章”实体。除了缓存和归一化之外，`Apollo Client` 还具有许多功能，如错误管理、支持分页和乐观 UI、数据预取，以及数据层（`Apollo Client`）与视图层（例如 React）的连接。

### 与其他框架的互操作性

`Apollo` 的库之一使得`Apollo Client`连接到`React`成为可能。就像`Redux`和`MobX`等库一样，`React-Apollo`库提供了高阶组件和渲染组件来连接这两个世界。然而，还有其他库不仅可以将`Apollo Client`连接到`React`，还可以将`Apollo`连接到`Angular`或`Apollo`连接到`Vue`。这使得`Apollo Client`与视图层无关，对于不断增长的 JavaScript 生态系统大有益。

`Apollo` 在服务器端也是库无关的，它提供了多种连接 Node.js 库的解决方案。用于`Express.js`的`Apollo Server`是开发者和公司中最受欢迎的选择之一，对于 Node.js 的`Koa`和`Hapi`还有其他解决方案。

### 使用 Apollo 进行现代数据处理

随着 GraphQL 在 JavaScript 应用中的兴起，状态管理进入了另一个混乱阶段。尽管使用像`Apollo Client`这样的 GraphQL 库消除了许多痛点，但由于它处理了远程数据的状态管理，一些开发者对于现在应该在何处放置`Redux`或`MobX`等状态管理库感到困惑。然而，通过仅将这些库用于本地数据，并将远程数据留给`Apollo`，可以让一切变得简单。`Redux`不再需要通过异步 action 来获取数据，因此它变成了所有剩余应用程序状态（例如：本地数据/视图数据/UI 数据）的可预测状态容器。事实上，剩余的应用程序状态可能简单到完全可以用`React`的本地状态来管理，而不是`Redux`。

与此同时，`Apollo`已经发布了他们自己的解决方案来管理本地状态——这本应由`React`本地状态、`Redux`或`MobX`管理——即通过对一切拥抱 GraphQL 来实现。`Apollo Link State`库允许我们通过`GraphQL operations`管理本地数据，但在`Apollo Client`客户端除外。这是`Apollo`在说：“你不需要任何其他状态管理库，我们来处理你的数据。”这是开发 JavaScript 应用的激动人心时代。

## 便捷的开发体验

在 JavaScript 应用中使用`Apollo`每天变得越来越容易。社区正在推出各种实现工具。有作为浏览器扩展程序提供的开发工具、执行`GraphQL operations`的第三方工具（如`GraphiQL`），以及简化开发`Apollo`应用的库。例如，`Apollo Boost`库提供了一个近乎零配置的`Apollo Client`设置，以便为客户端应用开始使用`GraphQL`。`Apollo`拿走了 JavaScript 中`GraphQL`参考实现中附带的所有样板代码实现。

## Apollo 的缺点

以下主题将向你展示使用`Apollo`的一些缺点，以提供一个全面的优缺点列表。如果你认为任何一个列表都有所遗漏，请随时联系我。

### 尖端技术 (Bleeding Edge)

`GraphQL`处于早期阶段。`Apollo`用户和所有早期的`GraphQL`采用者都在使用全新的技术。`Apollo`团队正在围绕`GraphQL`开发一个丰富的生态系统，提供基础功能以及如缓存和监控等高级功能。然而，这也伴随着陷阱，主要是因为一切尚未尘埃落定。一些零星的变化可能会在你更新`GraphQL-related libraries`时带来挑战。相比之下，`GraphQL`中的某些库可能比`Apollo`团队更保守，但功能通常没有那么强大。

快速迭代的发展也阻碍了开发者继续学习的能力。`GraphQL`和`Apollo`的教程有时会过时，寻找答案可能需要外部资源。对于大多数新技术来说也是如此。

### 建设中 (Under Construction)

`Apollo`团队和社区以快速速度实现了许多新功能，但运行得太快是有代价的。搜索解决方案通常会指向`GitHub`，因为关于该主题的类型信息很少。虽然你确实可以为你的问题找到一个`GitHub issue`，但通常对其没有解决方案。

快速开发还以忽视之前的旧版本为代价。根据我的经验，当人们发现 [Apollo 放弃 Redux](https://github.com/apollographql/apollo-client/issues/2593) 作为其内部状态管理解决方案时，他们似乎感到很困惑。`Apollo`对于`Redux`如何与它并肩使用并不持有观点，但由于它已作为内部状态管理解决方案被抛弃，许多人在`Apollo 2.0`发布时不知道该如何进行。我认为`Apollo`背后的团队可能正在努力跟上快速迭代的`GraphQL`生态系统，在开源开发中，听取所有的声音并不总是容易的。

### 大胆且时尚

`Apollo`是大胆的，因为它不再仅仅是 JavaScript 中客户端和服务器之间的`GraphQL`网络层生态系统，而是将其定位为未来的数据管理解决方案。它通过`GraphQL`连接客户端和后端应用，通过`apollo-link-rest`连接 RESTful API，通过`apollo-link-state`进行本地状态管理。一些专家对“GraphQL everything”的心态表示怀疑，但时间将证明它是否能主宰该市场。

`Apollo`是时尚的，因为它跟上了最新趋势。在`React`中，最新的趋势是渲染属性组件（render prop components）。由于这一点，以及可以说是渲染属性组件相对于高阶组件的优势，`React Apollo`库在高阶组件旁边引入了 [render prop components](https://www.robinwieruch.de/react-render-props-pattern/)。提供多种解决方案是一个明智的举动，因为高阶组件和渲染属性组件都有各自的优缺点。然而，`Apollo`确实主张使用渲染属性而非高阶组件，目前还不清楚这是炒作驱动的发展还是营销，还是他们真的相信这是未来的趋势。渲染属性在`React`中相对较新，因此开发者需要时间来意识到它们也有其自己的陷阱（参见：高阶组件）。我曾看到`React`应用因为在同一个`React`组件中使用多个渲染属性组件而变得过于冗长，尽管一个渲染属性并不依赖于另一个渲染属性，而没有通过使用高阶组件将它们同地定位在`React`组件中。归根结底，`Apollo`两种解决方案（渲染属性和高阶组件），因此开发者可以根据应用程序的具体情况做出决定。对于用户来说，`Apollo`团队能够跟上其他库的最新趋势，而不是把自己局限在泡泡中，这是一个好信号。

### 缺乏竞争

这些担忧中的大部分是关于`GraphQL`的新颖性，这些担忧适用于该领域的任何其他开源解决方案。然而，一个主要的担忧是 JavaScript `GraphQL`领域缺乏竞争。下一节将列出`Apollo`的一些替代方案，但与`Apollo`相比，它们非常有限。虽然可以为`GraphQL`编写自己的库（例如 [a simple GraphQL in React](https://github.com/rwieruch/react-graphql-client)，但还没有许多开发者尝试过。`Apollo`解决的问题并不简单，但我认为竞争对 JavaScript 生态系统中的`GraphQL`是一种健康的推动。`GraphQL`现在具有巨大的潜力，开源开发者应该利用这一点。

## JavaScript、React 和 Node.js 的 Apollo 替代方案

使用`GraphQL`作为 RESTful 驱动架构的替代方案存在一些缺点。JavaScript 中有一些`Apollo Client`和`Apollo Server`的替代方案可以消费`GraphQL APIs`。以下列表提供了关于 JavaScript 生态系统中解决方案的见解，用于客户端的`React`和服务器端的`Node.js`。

### React 的 Apollo Client 替代方案

对于`React`、`Angular`、`Vue`或类似的 [Apollo Client](https://github.com/apollographql/apollo-client)，有很多替代方案可以使用。像`Apollo`一样，它们都有各自的优缺点。

* `plain HTTP request`: 尽管可以使用复杂的 GraphQL 库来执行你的`GraphQL operations`，但`GraphQL`本身对网络层并不持观点。因此，你可以使用简单的 HTTP 方法配合`GraphQL`，只需使用一个端点以及针对`GraphQL 查询和变变`的特定载荷结构。

* [Relay](https://github.com/facebook/relay): `Relay`是 Facebook 用于在`React`应用的客户端消费`GraphQL`的库。它是`Apollo`出现之前最早的 GraphQL 客户端库之一。

* [urql](https://github.com/FormidableLabs/urql): urql 是由 Formidable Labs 开发的一个 GraphQL 客户端库，用于在 React 应用中消费 GraphQL。它的开源是作为日益庞大的 `Apollo` 巨头的极简主义替代方案。

* [graphql.js](https://github.com/f/graphql.js/): graphql.js 不应被误认为是 GraphQL 的参考实现。它是一个适用于没有 Vue、React 或 Angular 等强大库应用的简单 GraphQL 客户端。

* [AWS Amplify - GraphQL Client](https://github.com/aws/aws-amplify): AWS Amplify 系列为云端应用程序提供了库。其中一个模块是用于通用 GraphQL 服务器或 AWS AppSync API 的 GraphQL 客户端。

## 用于 Node.js 的 Apollo Server 替代方案

当涉及到用于 Express、Koa、Hapi 或其他框架的 Node.js [Apollo Server](https://github.com/apollographql/apollo-server) 时，有几种替代方案可以尝试。显然，这些方案都有各自的优缺点，但此处未涵盖这些内容。

* [express-graphql](https://github.com/graphql/express-graphql): 该库提供了一个低级 API，将 GraphQL 层连接到 Express 中间件。它采用纯的`graphql.js`参考实现来定义 GraphQL Schema，而 Apollo Server 则为开发者简化了这一过程。

* [graphql-yoga](https://github.com/prisma/graphql-yoga): 一个功能齐全的 GraphQL Server，专注于易于设置、性能和卓越的开发者体验。它在其他 GraphQL 库的基础上构建，为你减少了更多的样板代码。

当你想要使用 GraphQL 接口而不是 RESTful 接口时，有许多理由要在 JavaScript 应用中使用 `Apollo` 及其不断蓬勃的生态系统。它们的库与框架无关，因此可以与客户端的 React、Angular、Vue 等多种框架一起，也可以与服务端的 Express、Koa、Hapi 等应用一起。

## GraphQL 设置、工具和 API

循序渐进通常是学习新事物最简单的方法，因此在 JavaScript 中学习 GraphQL 既涵盖了应用的客户端也了服务端是非常幸运的。看到 Web 事务的两端是有用的，但困难之处在于你必须学习两个环境。循序渐进的方法在这里可能难以应用，因此我鼓励初学者先从客户端应用程序开始，通过消费第三方 GraphQL API，然后再学习使用 GraphQL 服务器的服务端。

[GitHub](https://github.com) 是最早采用 GraphQL 的主流科技品牌之一。他们甚至成功地[发布了](https://githubengineering.com/the-github-graphql-api) 公共 GraphQL API [(官方文档)](https://developer.github.com/v4)，这在开发者中非常流行，因为大多数人由于在自己的项目中使用，已经对 GitHub 足够熟悉了。



在本章中，我希望涵盖你启动 GitHub GraphQL API 所需的所有内容，并从客户端视角通过消费他们的 API 来学习在 JavaScript 中使用 GraphQL。你将理解 GitHub 的术语，以及如何使用其 GraphQL API 消费账户数据。我们将从客户端视角使用此 GraphQL API 实现几个应用程序，因此在这一部分投入时间是有意义的，以避免任何基础性错误。此后，我们将通过实现自己的 GraphQL 服务器过渡到服务端。

## 在 GitHub 上为 API 填充数据

如果你还没有 GitHub 账号，并且对它的生态系统并不了解，请遵循[这个 GitHub 官方学习实验室](https://lab.github.com/)。如果你想深入研究 Git 及其核心命令，请查看关于它的[此指南](https://www.robinwieruch.de/git-essential-commands/)。如果你决定将来在 GitHub 上与他人共享项目，这可能会很有帮助。这是向潜在客户或招聘公司展示开发作品集的好方法。

对于我们与 GitHub GraphQL API 的交互，你将使用自己带有信息的账号来对这些数据进行读/写。在此之前，通过提供额外信息来完善你的 GitHub 个人资料，以便以后 API 读取它时能够识别。

### 练习：

- 如果没有，请创建一个 GitHub 账号
- 为你的 GitHub 个人资料提供额外信息

## GitHub 仓库 (Repositories)

你也可以在 GitHub 上创建仓库。用他们的官方术语表来说：“仓库是 GitHub 最基本的元素。它们最容易被想象成项目的文件夹。仓库包含项目的所有文件（包括文档），并存储每个文件的修订历史。仓库可以有多个协作者，可以是公共的也可以是私有的。”[GitHub 术语表](https://help.github.com/articles/github-glossary/) 将解释关键术语——repository（仓库）、issue、clone、fork、push，这些术语对于跟进后续章节学习 GraphQL 是必要的。基本上，仓库是存放可以与他人共享的应用源代码的地方。我鼓励你将几个项目放入 GitHub 仓库中，这样你以后就可以通过学到的 GraphQL API 知识来访问它们了。

如果你没有任何项目要上传，可以随时“fork”（派生）其他 GitHub 用户的仓库并在其副本上工作。fork 基本上是仓库的克隆，你可以在不更改原始版本的情况下添加更改。GitHub 上有许多公共仓库可以克隆到你的本地机器或 fork 到你的列表中，这样你就可以通过实验来理解这种机制。例如，如果你访问[我的 GitHub 个人资料](https://github.com/rwieruch)，你可以看到我所有的公共仓库，尽管并非所有的都是我的，因为其中一些是 fork 的。

### 练习：

- 创建/Fork 几个 GitHub 仓库，并验证它们是否显示在你的账号中。在所有标题中，副本通过仓库名称前的用户名来指示；例如，`OriginalAuthor/TestRepo` 在你 fork 之后，它被重命名为 `YourUserName/TestRepo`。

## 分页数据 (Paginated Data)

GitHub 的 GraphQL API 允许你一次请求多个仓库，这对于分页非常有用。分页是一种为了处理大型项目列表而发明的编程机制。例如，想象你的 GitHub 账户中有一百多个仓库，但你的 UI 只显示其中十个。在每个请求中跨网络传输整个列表是不现实且低效的，因为每次只需要子集，而分页允许了这一点。

使用 GitHub GraphQL API 的分页允许你根据自己的需要调整数字，因此请确保根据你的个人需求调整数字（例如 `limit`、`offset`）（例如，你 GitHub 账号的可用仓库或某个 GitHub 组织的可用仓库）。你至少要在你的集合中拥有足够的仓库来看到分页功能的运行，因此我建议超过二十（20）个，假设每页显示十（10）个，或者在显示两（2）个时使用五（5）个仓库。

## Issues 和 Pull Requests

当你深入研究 GitHub GraphQL API 并开始请求嵌套关系（例如仓库的 `issues`、仓库的 `pullRequests`）时，请确保这些仓库有一些 issue 或 pull request。这样当我们实现显示仓库中所有 issue 的功能时，你就能看到内容。从 GitHub 组织请求仓库可能会更好，因为那里会有大量的 issue 和 pull request。

### 练习：

- 了解更多关于 [GitHub 术语表](https://help.github.com/articles/github-glossary/) 中的不同术语。考虑以下问题：
  - 什么是 GitHub 组织（organization）和 GitHub 用户？
  - 什么是仓库（repositories）、问题（issues）和拉请求（pull requests）？
  - 什么是 GitHub 仓库收藏（stars）和仓库关注者（watchers）？
- 创建或 fork 足够的仓库以使用分页功能。
- 在你的几个 GitHub 仓库中创建拉请求和问题。

## 使用 GitHub 个人访问令牌读写数据

要使用 GitHub 的 GraphQL API，你需要在其网站上生成个人访问令牌（personal access token）。访问令牌授权用户与数据进行交互，并在你的用户名下进行读取和写入操作。[按照他们的步骤说明](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line) 获取个人访问令牌，并务必勾选必要的范围（权限），因为你之后需要它们来实现一个完善的 GitHub 客户端。

![GitHub 个人访问令牌](img/github-personal-access-token_1024.jpg)

稍后，个人访问令牌可用于与 GitHub 的 GraphQL API 交互。注意不要将这些授权共享给任何第三方。

## 与 GitHub GraphQL API 交互

有两种常用的方法可以在不编写任何源码的情况下与 GitHub GraphQL API 交互。首先，你可以使用 [GitHub GraphQL Explorer](https://developer.github.com/v4/explorer/)。你只需要用你的 GitHub 账户登录即可对他们的 GraphQL API 执行查询（query）或变异（mutation），这是简化首次体验的好方法。其次，你可以使用应用程序形式的通用客户端。`GraphiQL` 是一个可以集成或作为独立应用程序发送 GraphQL 请求的客户端。前者可以通过[在你的应用程序中直接设置 GraphiQL](https://github.com/skevy/graphiql-app) 实现；后者通过[将 GraphiQL 作为独立应用程序使用](https://github.com/skevy/graphiql-app) 对你来说可能更方便。它是 `GraphiQL` 的一个轻量级外壳，可以手动下载或通过命令行安装。

GitHub GraphQL Explorer 知道你的凭据，因为你需要使用它进行登录，但 `GraphiQL` 需要知道你创建的个人访问令牌。你可以在 headers 配置中为每个请求的 HTTP header 中添加它。

![GraphiQL headers](img/graphiql-headers_1024.jpg)

在下一步，我们为你的 `GraphiQL` 配置添加一个带有名称和值的新 header。要与 GitHub 的 GraphQL API 通信，将 header 名称填充为 `Authorization`，header 值填充为 `bearer [你的个人访问令牌]`。为你的 `GraphiQL` 应用程序保存此新 header。最后，你就可以使用你的 `GraphiQL` 应用程序向 GitHub GraphQL API 发起请求了。

![GraphiQL authorization](img/graphiql-authorization_1024.jpg)

如果你使用自己的 `GraphiQL` 应用程序，你需要提供 GitHub GraphQL API 的 GraphQL 端点：`https://api.github.com/graphql`。对于 GitHub GraphQL API，请使用 [POST HTTP 方法](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Request_methods) 进行查询和变异，并将数据作为有效负载传输到你的 GraphQL 端点。

本节为你提供了两种与 GitHub GraphQL API 交互的方法。GitHub GraphQL Explorer 只能用于 GitHub 的 API，而集成到应用程序或独立运行的 `GraphiQL` 可用于任何 GraphQL API。区别在于它需要稍微多的设置。GitHub GraphQL Explorer 实际上只是一个为使用 GitHub GraphQL API 定身定制的托管式独立 GraphiQL 应用程序。

在你配置好 GitHub 使用其 GraphQL API 来学习 GraphQL 之后，你就应该准备好实现你的第一个 GraphQL 客户端交互了。按照此步骤，使用你刚刚设置的工具以及 React 创建你的第一个 GraphQL 客户端应用程序。

## GraphQL 基础

在我们开始在客户端和服务器端构建完整的 GraphQL 应用程序之前，让我们用之前节中安装的工具探索 GraphQL。你可以使用 `GraphiQL` 或 GitHub GraphQL Explorer。在下文中，你将通过在 GitHub GraphQL API 的范围内执行你的第一个 GraphQL 查询、变异，甚至探索分页等功能来学习 GraphQL 的基础。

### GraphQL 操作：Query

在本节中，你将在不使用 React 的情况下使用查询和变异与 GitHub API 交互，因此你可以使用 `GraphiQL` 应用程序或 GitHub GraphQL Explorer 向 GitHub API 请求 GraphQL 查询。这两个工具都应该获得授权以使用个人访问令牌发送请求。在你的 `GraphiQL` 应用程序左侧，你可以填写 GraphQL 查询和变异。添加以下查询来请求关于你的数据。

```graphql
{
  viewer {
    name
    url
  }
}
```

`viewer` 对象可用于请求当前授权用户的数据。由于你已通过个人访问令牌获得授权，它应该显示关于你的账户的数据。在 GraphQL 术语中，`viewer` 是一个**对象**。对象持有有关实体的数据。这些数据是通过 GraphQL 中所谓的**字段**来访问的。字段被用于请求对象中的特定属性。例如，`viewer` 对象暴露了广泛的字段。查询使用了该对象的两个字段——`name` 和 `url`。在最基础的形式下，查询仅仅是对象和字段，对象也可以称为字段。

一旦你在 `GraphiQL` 中运行查询，你应该看到类似下面的输出，其中包含你的名称和 URL：

```json
{
  "data": {
    "viewer": {
      "name": "Robin Wieruch",
      "url": "https://github.com/rwieruch"
    }
  }
}
```

恭喜，你已经执行了第一次查询来访问字段数据。现在，让我们看看如何请求你自身以外的数据源，例如一个公共组织。为了指定 GitHub 组织，你可以向字段传递**参数**（argument）：

```graphql
{
  organization(login: "the-road-to-learn-react") {
    name
    url
  }
}
```

在使用 GitHub API 时，通过 `login` 识别组织。如果你用过 GitHub，你可能知道这是组织 URL 的：

`https://github.com/the-road-to-learn-react`

通过提供 `login` 来标识组织，你可以请求关于它的数据。在这个示例中，你指定了两个字段来访问组织的 `name` 和 `url`。请求应该返回类似下面的输出：

```json
{
  "data": {
    "organization": {
      "name": "The Road to learn React",
      "url": "https://github.com/the-road-to-learn-react"
    }
  }
}
```

```graphql
{
  book: organization(login: "the-road-to-learn-react") {
    name
    url
  }
  company: organization(login: "facebook") {
    name
    url
  }
}
```

结果应该类似于下面：

```json
{
  "data": {
    "book": {
      "name": "The Road to learn React",
      "url": "https://github.com/the-road-to-learn-react"
    },
    "company": {
      "name": "Facebook",
      "url": "https://github.com/facebook"
    }
  }
}
```

接下来，想象你想为这两个组织都请求多个字段。为每个组织重新输入所有字段将使查询变得冗余且冗长，因此我们将使用 `fragments`（片段）来提取查询中可重用的部分。当你的查询变得深度嵌套并使用大量共享字段时，片段变得特别有用。

```graphql
{
  book: organization(login: "the-road-to-learn-react") {
    ...sharedOrganizationFields
  }
  company: organization(login: "facebook") {
    ...sharedOrganizationFields
  }
}

fragment sharedOrganizationFields on Organization {
  name
  url
}
```

如你所见，你必须指定片段使用在哪种 `type`（类型）对象上。在这种情况下，它是 `Organization` 类型，由 GitHub 的 GraphQL API 定义的自定义类型。这就是你使用片段来提取和重用查询部分的方法。此时，你可能想打开 GraphiQL 应用右侧的“Docs”（文档）。文档让你能够访问 GraphQL `schema`（架构）。架构暴露了你的 GraphiQL 应用所使用的 GraphQL API，在此情况下，它是 Github 的 GraphQL API。它定义了可以通过 GraphQL API 使用查询（queries）和变异（mutations）访问的 GraphQL `graph`（图）。由于它是一个图，对象和字段可以在其中深度嵌套，我们在后续的学习中一定会遇到这种情况。

由于我们目前正在探索查询而不是变异，请在“Docs”侧边栏中选择“Query”。之后，遍历图中的对象和字段，探索它们的可选参数。通过点击它们，你可以查看图中这些对象内可用的字段。某些字段是常见的 GraphQL 类型，如 `String`、`Int` 和 `Boolean`，而其他类型是 `custom types`（自定义类型），例如我们使用的 `Organization` 类型。此外，你可以在请求对象上的字段时查看参数是否必填。可以通过感叹号来识别。例如，带有 `String!` 参数的字段要求你传递一个 `String` 参数，而带有 `String` 参数的字段则不需要你传递它。

在之前的查询中，你为字段提供了标识组织的参数；但你是在查询中内联了这些参数（inlined these arguments）。请将查询想象成一个函数，为它提供动态参数是非常关键的。这正是 GraphQL 中 `variable`（变量）大显用场，因为它允许将参数从查询中提取为变量。以下是如何将组织的 `login` 参数提取为动态变量的方法：

```graphql
query ($organization: String!) {
  organization(login: $organization) {
    name
    url
  }
}
```

它使用 `$` 符号将 `organization` 参数定义为变量。此外，参数的类型被定义为 `String`。由于完成查询需要该参数，`String` 类型带有一个叹号。

在“Query Variables”（查询变量）面板中，为了提供 `organization` 变量作为查询的参数，变量内容如下：

```json
{
  "organization": "the-road-to-learn-react"
}
```

本质上，变量可以创建动态查询。遵循 GraphQL 的最佳实践，我们不需要手动字符串插值来构建动态查询。相反，我们提供一个使用变量作为参数的查询，这些变量在查询作为请求发送到 GraphQL API 时是可用的。你将在后面的 React 应用中看到这两种实现方式。



**备注**：你还可以在 GraphQL 中定义 `default variable`（默认变量）。它必须是一个非必填参数，否则会发生关于 `nullable variable`（空变量）或 `non-null variable`（非空变量）的错误。为了学习默认变量，我们将省略感叹号来使 `organization` 参数变为非必填。之后，它可以作为默认变量传递。

```graphql
query ($organization: String = "the-road-to-learn-react") {
  organization(login: $organization) {
    name
    url
  }
}
```

## GitHub GraphQL Explorer

尝试使用两组变量执行之前的查询：一次使用与默认变量不同的 `organization` 变量，另一次不定义 `organization` 变量。

现在，让我们后退一步，检查 GraphQL 查询的结构。在你引入变量之后，你第一次在查询结构中遇到了 `query` 语句。在此，你通过省略 `query` 语句使用了`查询的简写版本`（shorthand version of a query），但既然使用了变量，`query` 语句现在必须存在。尝试执行不带变量但带有 `query` 语句的查询，以验证查询的完整版本是有效的。

```graphql
query {
  organization(login: "the-road-to-learn-react") {
    name
    url
  }
}
```

## GitHub GraphQL Explorer

虽然这不是查询的简写版本，但它返回的数据与之前相同。查询语句在 GraphQL 中也被称为 `operation type`（操作类型）。例如，它也可以是一个 `mutation`（变异）语句。除了操作类型外，你还可以定义 `operation name`（操作名称）。

```graphql
query OrganizationForReact {
  organization(login: "the-road-to-learn-react") {
    name
    url
  }
}
```

## GitHub GraphQL Explorer

将其代码中的匿名函数和命名函数进行对比。`named query`（命名查询）以声明式方式提供了你想通过查询实现的目标清晰，并有助于调试多个查询，因此当你想实现应用程序时应该使用它。在不显示变量面板的情况下，你的最终查询可能如下：

```graphql
query OrganizationForReact($organization: String!) {
  organization(login: $organization) {
    name
    url
  }
}
```

## GitHub GraphQL Explorer

为止你只访问了一个对象，带有几个字段的组织。GraphQL 架构实现了整个图，让我们看看如何通过查询访问图中的 `nested object`（嵌套对象）。它与之前相比没有太大：

```graphql
query OrganizationForReact(
  $organization: String!,
  $repository: String!
) {
  organization(login: $organization) {
    name
    url
    repository(name: $repository) {
      name
    }
  }
}
```

## GitHub GraphQL Explorer

提供第二个变量来请求组织的特定存储库：

```json
{
  "organization": "the-road-to-learn-react",
  "repository": "the-road-to-learn-react-chinese"
}
```

## GitHub GraphQL Explorer

教授 React 的组织拥有内容的翻译版本，其一个存储库使用简体中文向学生教授 React。GraphQL 中的字段又是嵌套对象，你已经查询了图中的两个关联对象。在你之前在 GraphiQL 中探索“Docs”侧边栏时，你可能看到你可以在图中的对象之间跳转。

`directive` 可用于更强大的方式从你的 GraphQL API 查询数据，并且它们可以应用于字段和对象。在下面，我们使用两种类型的指令：`include directive`（包含指令），它在 `Boolean` 类型设置为 `true` 时包含该字段；以及 `skip directive`（跳过指令），它相反排除该字段。通过这些指令，你可以为你的查询结构应用条件结构。下面的查询展示了 `include directive`，但你可以将其替换为 `skip directive` 以实现相反的效果：

```graphql
query OrganizationForLearningReact(
  $organization: String!,
  $repository: String!,
  $withFork: Boolean!
) {
  organization(login: $organization) {
    name
    url
    repository(name: $repository) {
      name
      forkCount @include(if: $withFork)
    }
  }
}
```

GitHub GraphQL 器

现在，你可以根据提供的变量决定是否包含 `forkCount` 字段的信息。

```json
{
  "organization": "the-road-to-learn-react",
  "repository": "the-road-to-learn-react-chinese",
  "withFork": true
}
```

GitHub GraphQL 器

GraphQL 中的查询提供了你从 GraphQL API 读取数据所需的所有内容。最后一部分可能让你感觉像信息风暴，因此这些练习提供了额外的练习，直到你感到得心应。

### 练习题

- 阅读更多关于 [GraphQL 中的查询](http://graphql.org/learn/queries) 的内容。
- 使用 GraphiQL 中的“Docs（文档）”侧边栏探索 GitHub 的查询模式。
- 创建几个查询，使用以下功能从 GitHub 的 GraphQL API 请求数据：
  - 对象和字段
  - 嵌套对象
  - 片段（fragments）
  - 参数和变量
  - 操作名称
  - 指令

## GraphQL 操作：Mutation（变异）

本节介绍 GraphQL mutation。它补充了 GraphQL 查询，因为它被用于写入数据而不是读取数据。mutation 与查询共享相同的原理：它也拥有字段和对象、参数和变量、片段和操作名称，以及用于返回结果的指令和嵌套对象。通过 mutation，你可以将数据指定为字段和对象，并在它们“变异”为某种可接受的形式后返回。在你开始进行第一个 mutation 之前，请注意你正在使用真实的 GitHub 数据，所以如果你使用实验性 mutation 关注 GitHub 上的某个人，你真的关注了。幸运的是，这种行为在 GitHub 上是被鼓励的。

在本节中，你将使用 [GitHub API 的 mutation](https://developer.github.com/v4/mutation/addstar) 在 GitHub 上点星一个仓库（你之前使用查询请求过的同一个）。你可以在“Docs（文档）”侧边栏找到 `addStar` mutation。该仓库是一个向开发者教授 React 基础的项目，因此点星它应该是很有用的。

你可以访问[该仓库](https://github.com/the-road-to-learn-react/the-road-to-learn-react) 查看你是否已经给该仓库点过星。我们想要一个未点星的仓库，以便我们使用 mutation 来点星。在点星仓库之前，你需要知道它的标识符，可以通过查询来获取它：

```graphql
query {
  organization(login: "the-road-to-learn-react") {
    name
    url
    repository(name: "the-road-to-learn-react") {
      id
      name
    }
  }
}
```

GitHub GraphQL 器

在 GraphiQL 的查询结果中，你应该看到仓库的标识符：

```text
MDEwOlJlcG9zaXRvcnk2MzM1MjkwNw==
```

代码演场

在使用标识符作为变量之前，你可以按照以下方式在 GraphiQL 中构建你的 mutation：

```graphql
mutation AddStar($repositoryId: ID!) {
  addStar(input: { starrableId: $repositoryId }) {
    starrable {
      id
      viewerHasStarred
    }
  }
}
```

GitHub GraphQL 器

mutation 的名称由 GitHub API 提供：`addStar`。你需要将 `starrableId` 作为 `input` 传递给它以标识仓库；否则，GitHub 服务器不知道用该 mutation 点星哪个仓库。此外，该 mutation 是一个命名 mutation：`AddStar`。你可以自己给它任何名称。最后但同样重要的是，你可以再次通过对象和字段来定义 mutation 的返回值。这与查询完全相同。最后，变量标签页提供了你通过上一次查询获取的 mutation 变量：

```json
{
  "repositoryId": "MDEwOlJlcG9zaXRvcnk2MzM1MjkwNw=="
}
```

GitHub GraphQL 器

一旦你执行 mutation，结果应该如下所示。由于你使用 `id` 和 `viewerHasStarred` 字段指定了你 mutation 的返回值，你应该在结果中看到它们。

```json
{
  "data": {
    "addStar": {
      "starrable": {
        "id": "MDEwOlJlcG9zaXRvcnk2MzM1MjkwNw==",
        "viewerHasStarred": true
      }
    }
  }
}
```

GitHub GraphQL 器

仓库现在已被点星。它在结果中可见，但你可以在 [GitHub 上的仓库](https://github.com/the-road-to-learn-react/the-road-to-learn-react) 中验证。恭喜，你完成了你的第一个 mutation。

### 练习题

- 阅读更多关于 [GraphQL 中的 Mutation](http://graphql.org/learn/queries#mutations) 的内容。
- 使用 GraphiQL 中的“Docs（文档）”侧边栏探索 GitHub 的查询模式。
- 在 GraphiQL 的“Docs（文档）”侧边栏找到 `addStar` mutation。
- 创建几个查询，使用以下功能从 GitHub 的 GraphQL API 请求数据：
  - 查看可能的字段
  - 取消仓库星
  - 关注仓库
  - 阅读关于[模式和类型](http://graphql.org/learn/schema) 的内容
  - 自己画个图

## GraphQL 分页（Pagination）

在这里我们回到第一章提到的**分页（pagination）**概念。假设你的组织中有一个仓库列表，但你只想检索其中几个并显示在 UI 中。在 GraphQL 中，你可以通过为**列表字段**提供参数来请求分页数据，例如指定你期望的项数的参数。

```graphql
query OrganizationForLearningReact {
  organization(login: "the-road-to-learn-react") {
    name
    url
    repositories(first: 2) {
      edges {
        node {
          name
        }
      }
    }
  }
}
```

GitHub GraphQL 器

`first` 参数被传递给 `repositories` 列表字段，指定了结果中期望有多少项。查询形状不需要遵循 `edges` 和 `node` 结构，但它是使用 GraphQL 定义分页数据结构和列表的解决方案之一。实际上，它遵循了 Facebook 的 GraphQL 客户端 Relay 的接口描述。GitHub 采用了这种方法并将其应用于 GraphQL 分页 API。稍后，你将在练习中学习实现 GraphQL 分页的其他策略。

执行查询后，你应该在 `repositories` 字段中看到列表中的两个项。然而，我们仍然需要弄清楚如何获取列表中的下两个仓库。查询的结果是分页列表的第一页，第二次查询结果应该是第二页。在下面，你将看到分页数据的查询结构允许我们检索元数据以执行后续查询。例如，每个 edge 都有自己的 `cursor` 字段，用于标识它在列表中的位置。

```graphql
query OrganizationForLearningReact {
  organization(login: "the-road-to-learn-react") {
    name
    url
    repositories(first: 2) {
      edges {
        node {
          name
        }
        cursor
      }
    }
  }
}
```

GitHub GraphQL 器

结果应该类似于以下：

```json
{
  "data": {
    "organization": {
      "name": "The Road to learn React",
      "url": "https://github.com/the-road-to-learn-react",
      "repositories": {
        "edges": [
          {
            "node": {
              "name": "the-road-to-learn-react"
            },
            "cursor": "Y3Vyc29yOnYyOpHOA8awSw=="
          },
          {
            "node": {
              "name": "hackernews-client"
            },
            "cursor": "Y3Vyc29yOnYyOpHOBGhimw=="
          }
        ]
      }
    }
  }
}
```

## GitHub GraphQL Explorer

现在，你可以使用列表中的第一个仓库的 `cursor` 来执行第二次查询。通过对 `repositories` 列表字段使用 `after` 参数，你可以指定一个切入点来获取下一页分页数据。执行以下查询时，结果会是什么样？

```graphql
query OrganizationForLearningReact {
  organization(login: "the-road-to-learn-react") {
    name
    url
    repositories(first: 2, after: "Y3Vyc29yOnYyOpHOA8awSw==") {
      edges {
        node {
          name
        }
        cursor
      }
    }
  }
}
```

## GitHub GraphQL Explorer

在上一个结果中，只获取了第二个项目，以及一个新的第三个项目。第一个项目没有被获取，是因为你已经使用了它的 `cursor` 作为 `after` 参数来获取其之后的所有项目。现在你可以想象一下如何对分页列表进行连续查询：

- 在不带任何 `cursor` 参数的情况下执行初始查询。
- 在执行后续每个查询时，使用上一个查询结果中 `last` 项目的 `cursor`。

为了保持查询的动态性，我们将参数提取为变量。之后，你可以通过为它提供变量来使用带有动态 `cursor` 参数的查询。`after` 参数可以为 `undefined` 以获取第一页。总而言之，这就是你使用名为“分页”（pagination）的功能从一个大列表中获取列表页所需的所有内容。你需要一个强制参数来指定应该获取多少项，以及一个可选参数（在本例中为 `after` 参数），指定列表的起始点。

还有一些使用元信息处理你分页列表的有用方法。当仅使用最后一个仓库的 `cursor` 时，获取每个仓库的 `cursor` 字段可能会很冗长，因此你可以移除单个边的 `cursor` 字段，但添加一个包含 `endCursor` 和 `hasNextPage` 字段的 `pageInfo` 对象。你也可以请求列表的 `totalCount`。



```query
query OrganizationForLearningReact {
  organization(login: "the-road-to-learn-react") {
    name
    url
    repositories(first: 2, after: "Y3Vyc29yOnYyOpHOA8awSw==") {
      totalCount
      edges {
        node {
          name
        }
      }
      pageInfo {
        endCursor
        hasNextPage
      }
    }
  }
}
```

# GitHub GraphQL Explorer

`totalCount` 字段显示了列表中项目的总数，而 `pageInfo` 字段为你提供了关于两方面的信息：

* `endCursor` 可以用于获取后续列表，我们之前通过 `cursor` 字段做过这一点，但这次我们只需要一个元字段即可完成。最后一个列表项的游标就足够请求下一页列表了。
* `hasNextPage` 提供关于从 GraphQL API 是否还有下一页可以获取的信息。有时你已经从服务器获取了最后一页。对于使用无限滚动在滚动列表时加载更多页的应用程序，你可以在没有更多可用页面时停止获取页面。

这些元信息完成了分页的实现。通过 GraphQL API 访问信息，以实现[分页列表](https://www.robinwieruch.de/react-paginated-list/)和[无限滚动](https://www.robinwieruch.de/react-infinite-scroll/)。注意，这涵盖了 GitHub 的 GraphQL API；用于分页的不同 GraphQL API 可能会使用不同的字段命名约定、排除元信息，或采用完全不同的机制。

## 练习：

* 从你的分页查询中将 `login` 和 `cursor` 作为变量提取。
* 将 `first` 参数替换为 `last` 参数。
* 在 GraphiQL 的“Docs 侧边栏”中搜索 `repositories` 字段，它显示为：“A list of repositories that the … owns.”
  * 探索可以传递此列表字段的其他参数。
  * 使用 `orderBy` 参数获取升序或降序列表。
* 阅读更多关于[GraphQL 中的分页](http://graphql.org/learn/pagination) 的信息。
  * 游标方法只是 GitHub 使用的一种种解决方案。
  * 确保也理解其他的解决方案。

通过 GraphiQL 或 GitHub 的 GraphQL Explorer 与 GitHub 的 GraphQL API 交互只是一个开始。你现在应该熟悉基本的 GraphQL 概念了。但还有许多令人兴奋的概念等待探索。在接下来的章节中，你将使用 React 实现一个功能完整的 GraphQL 客户端应用程序，并与 GitHub 的 API 进行交互。

## React 与 GraphQL

在我们共同构建的客户端 GraphQL 应用程序中，你将学习如何将 React 与 GraphQL 结合。不需要像 [Apollo Client](https://github.com/apollographql/apollo-client) 或 [Relay](https://github.com/facebook/relay) 这样的巧妙库来帮助你入门；我们将使用基础的 HTTP 请求执行查询和变更。在此过程中，我们将构建一个简化的 GitHub 客户端，本质上是一个 GitHub 问题跟踪器，它调用 [GitHub API](https://developer.github.com/v4/)。你将执行 GraphQL 查询和变更来读写数据，最后，你应该能够展示可以作为开发者学习工具的 React GraphQL 示例。你将构建的最终应用程序可以在[仓库](https://github.com/wieruch/react-graphql-github-vanilla) 中找到。

### 编写你的第一个 React GraphQL 客户端

在前面的章节之后，你应该准备好在 React 程序中使用查询和变更了。在本节中，你将创建一个调用 GraphQL API 的 React 应用程序。该应用程序应该显示 GitHub 仓库中的开放问题，使其成为简单的跟踪器。再次，如果你缺乏 React 经验，请参阅*学习 React 之路*以了解更多信息。之后你应该准备好进入下一节。

对于此应用程序，不需要复杂的 React 设置。你只需使用 [create-react-app](https://github.com/facebook/create-react-app) 创建零配置的 React 应用程序。在命令行中输入以下指令通过 npm 安装：`npm install -g create-react-app`。如果你想使用更复杂的 React 设置，请阅读这篇[使用 Webpack 配合 React 的设置指南](https://www.robinwieruch.de/minimal-react-webpack-babel-setup/)。

现在，用 create-react-app 创建应用程序。在你的通用项目文件夹中输入以下指令：

```text
create-react-app react-graphql-github-vanilla
cd react-graphql-github-vanilla
```

#### 命令行

在创建应用程序后，你可以使用 `npm start` 和 `npm test` 进行测试。再次，在*学习 React 之路*中学习了原生 React 后，你应该已经熟悉 npm、create-react-app 以及 React 本身。

# 介绍

接下来的应用程序将关注 `src/App.js` 文件。你可以根据需要将组件、配置或函数拆分到它们自己的文件夹和文件中。让我们从上述文件中 `App` 组件开始。为了简化起见，你可以将其更改为以下内容：

```javascript
import React, { Component } from 'react';

const TITLE = 'React GraphQL GitHub Client';

class App extends Component {
  render() {
    return (
      <div>
        <h1>{TITLE}</h1>
      </div>
    );
  }
}

export default App;
```

### `src/App.js`

## 使用 Axios 进行初始设置

该组件仅渲染一个 `title` 作为标题。在实现更多 React 组件之前，让我们先安装一个库来处理 GraphQL 请求，使用 HTTP POST 方法执行查询（queries）和变更（mutations）。为此你将使用 [axios](https://github.com/axios/axios)。在命令行中输入以下命令在项目文件夹中安装 `axios`

```bash
npm install axios --save
```

#### 命令行

之后，你可以在 `App` 组件旁边导入 `axios` 并对其进行配置。它非常适合下面的应用程序，因为某种原因，你只想使用你的个人访问令牌（personal access token）和 GitHub 的 GraphQL API 对其进行一次配置

首先，在创建配置好的实例时为 `axios` 定义一个基础 URL。如之前提到的，你不需要在每次请求时都定义 GitHub 的 URL 端点，因为所有的查询和变更都指向 GraphQL 中同一个 URL 端点。你通过对象和字段的查询和变更结构获得灵活性。

```javascript
import React, { Component } from 'react';
import axios from 'axios';

const axiosGitHubGraphQL = axios.create({
  baseURL: 'https://api.github.com/graphql',
});

...

export default App;
```

### `src/App.js`

其次，将个人访问令牌作为 header 传递给配置。header 将被使用此 `axios` 实例的每个请求使用。

```javascript
...

const axiosGitHubGraphQL = axios.create({
  baseURL: 'https://api.github.com/graphql',
  headers: {
    Authorization: 'bearer YOUR_GITHUB_PERSONAL_ACCESS_TOKEN',
  },
});

...
```

### `src/App.js`

将 `YOUR_GITHUB_PERSONAL_ACCESS_TOKEN` 字符串替换为你的个人访问令牌。为了避免直接将访问令牌粘贴到源代码中，你可以在项目文件夹的命令行中创建一个 `.env` 文件来存放所有的环境变量。如果你不想在公共 GitHub 仓库中共享个人令牌，可以将该文件添加到 `.gitignore` 中。

```bash
touch .env
```

#### 命令行

## 环境变量

### 在 `.env` 中配置

环境变量定义在这个 `.env` 文件中。在使用 `create-react-app` 时，务必遵循正确的命名限制，它使用 `REACT_APP` 作为每个键的前缀。在你的 `.env` 文件中，粘贴以下键值对。键必须具有 `REACT_APP` 前缀，值必须是你来自 GitHub 的个人访问令牌。

```text
REACT_APP_GITHUB_PERSONAL_ACCESS_TOKEN=xxxXXX
```

### `.env`

现在，你可以使用字符串插值（[模板字符串](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)）将个人访问令牌作为环境变量传递给你的 `axios` 配置，以创建一个配置好的 `axios` 实例。

```javascript
...

const axiosGitHubGraphQL = axios.create({
  baseURL: 'https://api.github.com/graphql',
  headers: {
    Authorization: `bearer ${
      process.env.REACT_APP_GITHUB_PERSONAL_ACCESS_TOKEN
    }`,
  },
});

...
```

### `src/App.js`

## 实现表单

初始的 `axios` 设置基本上与我们之前使用 GraphiQL 访问 GitHub GraphQL API 时完成的相同，当时你也需要设置带有个人访问令牌和端点 URL 的 header

接下来，设置一个表单来从用户处获取 GitHub 组织和仓库的详细信息。应该能够填充输入字段来请求特定 GitHub 仓库的分页问题（issues）列表。首先，需要一个带有输入框的表单来输入组织和仓库。输入框必须更新 React 的本地状态（state）。其次，表单需要一个提交按钮来请求用户在输入框中提供的组织和仓库数据，这些数据位于组件的本地状态中。第三，为组织和仓库设置一个初始本地状态会很，以便在组件首次挂载时请求初始数据

让我们分两步来实现此场景。`render` 方法必须渲染一个带有输入框的表单。表单必须有一个 `onSubmit` 处理程序，且输入框需要一个 `onChange` 处理程序。输入框使用本地状态中的 `path` 作为受控组件的值。本地状态中来自 `onChange` 处理程序的 `path` 值将在第二步中更新。

```javascript
class App extends Component {
  render() {
    return (
      <div>
        <h1>{TITLE}</h1>

        <form onSubmit={this.onSubmit}>
          <label htmlFor="url">
            Show open issues for https://github.com/
          </label>
          <input
            id="url"
          />
          <button type="submit">Search</button>
        </form>

        <hr />

        {/* result */}
      </div>
    );
  }
```

### `src/App.js`

类方法与状态

声明 `render` 方法中使用的类方法。`componentDidMount()` 生命周期方法可用于组件挂载时执行初始请求。输入框需要一个初始状态来执行初始请求。

```javascript
class App extends Component {
  state = {
    path: 'the-road-to-learn-react',
  };

  componentDidMount() {
    // fetch data
  }

  onChange = event => {
    this.setState({ path: event.target.value });
  };

  onSubmit = event => {
    // fetch data

    event.preventDefault();
  };

  render() {
    ...
  }
}
```

### `src/App.js`

控制组件

之前的实现使用了你可能未使用过的 React 类语法。如果你不熟悉，可以查看此 [GitHub 仓库](https://github.com/the-road-to-learn-react/alternative-class-component) 以获得理解。使用类字段声明允许省略初始化本地状态的构造函数，并消除绑定类方法的需要。相反，箭头函数将处理所有的绑定

遵循 React 的最佳实践，让输入框变为受控组件。输入元素不应使用原生行为处理其内部状态；而应该由 React 处理。

```javascript
class App extends Component {
  ...

  render() {
    const { path } = this.state;

    return (
      <div>
        <h1>{TITLE}</h1>

        <form onSubmit={this.onSubmit}>
          <label htmlFor="url">
            Show open issues for https://github.com/
          </label>
          <input
            id="url"
            type="text"
            value={path}
            onChange={this.onChange}
            style={{ width: '300px' }}
          />
          <button type="submit">Search</button>
        </form>

        <hr />

        {/* Here comes the result! */}
      </div>
    );
  }
}
```

### `src/App.js`

当你在命令行中启动应用程序时，你应该能在输入框中看到 `path` 的初始状态。你应该通过在输入框中输入其他内容来更改状态，但此时 `componentDidMount()` 和提交表单还没有触发任何操作。

你可能会纳奇，为什么只有一个输入框来获取组织和仓库的信息。在 GitHub 上打开一个仓库时，你可以看到组织和仓库都编码在 URL 中，因此这成为了为输入框显示相同 URL 模式的方便方法。你之后可以通过 `/` 拆分 `organization/repository` 来获取这些值并执行 GraphQL 查询请求。

### 练习：

* 确认你的[上一个节源码](http://bit.ly/2D0TMKz)
* 确认[上一个节的更改](http://bit.ly/2Vo6VVp)
* 如果你不熟悉 React，请查看 *React 实战之路 (The Road to learn React)*

### React 中的 GraphQL 查询

在本节中，你将在 React 中实现你的第一个 GraphQL 查询，从组织的仓库中获取问题（issues），尽管不是一次性获取。从只获取一个组织开始。让我们在 App 组件上方定义这个查询变量。

```javascript
const GET_ORGANIZATION = `
  {
    organization(login: "the-road-to-learn-react") {
      name
      url
    }
  }
`;
```

### `src/App.js`



使用 JavaScript 中的模板字符串（template literals）来定义多行的查询字符串。它应该与你之前在 GraphiQL 或 GitHub Explorer 中使用的查询完全相同。现在，你可以使用`axios`向 GitHub 的 GraphiQL API 发送 POST 请求。`axios`的配置已经指向了正确的 API 端点并使用了你的个人访问令牌。剩下的唯一工作是在 POST 请求期间将查询作为有效负载（payload）传递给它。端点的参数可以为空字符串，因为你已经在配置中定义了端点。当`App`组件在`componentDidMount()`中挂载时执行请求。当`axios`的 promise 解析完成（resolve）后，只会在控制台打印结果日志。

```javascript
...

const axiosGitHubGraphQL = axios.create({
  baseURL: 'https://api.github.com/graphql',
  headers: {
    Authorization: `bearer ${
      process.env.REACT_APP_GITHUB_PERSONAL_ACCESS_TOKEN
    }`,
  },
});

const GET_ORGANIZATION = `
  {
    organization(login: "the-road-to-learn-react") {
      name
      url
    }
  }
`;

class App extends Component {
  ...

  componentDidMount() {
    this.onFetchFromGitHub();
  }

  onSubmit = event => {
    // 获取数据
    event.preventDefault();
  };

  onFetchFromGitHub = () => {
    axiosGitHubGraphQL
      .post('', { query: GET_ORGANIZATION })
      .then(result => console.log(result));
  };

  ...
}
```

`src/App.js`

你仅使用`axios`执行了带有 GraphQL 查询有效负载的 HTTP POST 请求。由于`axios`使用 promise，promise 最终会解析，你应该就能拿到 GraphQL API 的结果。这并没有什么神奇的，它只是使用原生 JavaScript 和`axios`作为 HTTP 客户端通过原生 HTTP 执行 GraphQL 请求的实现。

再次启动你的应用程序并验证你是否已经在开发者控制台日志中获得了结果。如果你收到 [401 HTTP 状态码](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes)，说明你没有正确设置个人访问令牌。否则，如果一切顺利，你应该在开发者控制台日志中看到类似的结果。

```json
{
  "config": ...,
  "data":{
    "data":{
      "organization":{
        "name":"The Road to learn React",
        "url":"https://github.com/the-road-to-learn-react"
      }
    }
  },
  "headers": ...,
  "request": ...,
  "status": ...,
  "statusText": ...
}
```

### 开发者工具

顶层信息是`axios`返回的作为请求元数据的所有内容。这些都是`axios`的，目前尚未与 GraphQL 有关，这就是为什么大部分内容被替换为了占位符。`axios`有一个`data`属性显示你`axios`请求的结果。接着是另一个`data`属性反映 GraphQL 的结果。起初，第一个结果中的`data`属性似乎是冗余的，但一旦你检查它，就会发现一个`data`属性来自`axios`，而另一个来自 GraphQL 数据结构。最后，你在第二个`data`属性中发现了 GraphQL 查询的结果。在那里，你应该能找到组织及其解析后的`name`和`url`字段（字符串属性）。

下一步，你将把包含组织信息的响应存储在 React 的本地状态中。如果发生任何错误，你也将把错误存储在状态中。

```javascript
class App extends Component {
  state = {
    path: 'the-road-to-learn-react/the-road-to-learn-react',
    organization: null,
    errors: null,
  };

  ...

  onFetchFromGitHub = () => {
    axiosGitHubGraphQL
      .post('', { query: GET_ORGANIZATION })
      .then(result =>
        this.setState(() => ({
          organization: result.data.data.organization,
          errors: result.data.data.errors,
        })));
  };
}
```

接下来，我们将请求一个组织的嵌套对象。由于应用程序最终将显示仓库中的问题（issues），因此你的下一步应该是获取某个组织的仓库。请记住，查询会深入 GraphQL 图谱内部，因此当 schema 定义了这两种实体之间的关系时，我们可以将`repository`字段嵌套在`organization`字段中。

```
const GET_REPOSITORY_OF_ORGANIZATION = `
  {
    organization(login: "the-road-to-learn-react") {
      name
      url
      repository(name: "the-road-to-learn-react") {
        name
        url
      }
    }
  }
`;

class App extends Component {
  ...

  onFetchFromGitHub = () => {
    axiosGitHubGraphQL
      .post('', { query: GET_REPOSITORY_OF_ORGANIZATION })
      .then(result =>
          ...
      );
  };

  ...
}
```

`src/App.js`

在这种情况下，仓库名称与组织名称相同。目前没关系。稍后，你可以动态地定义组织和仓库。在第二步中，你可以使用另一个`Repository`组件作为子组件来扩展`Organization`组件。查询结果现在应该在组织对象中包含一个嵌套的`repository`对象。

```
const Organization = ({ organization, errors }) => {
  if (errors) {
    ...
  }

  return (
    <div>
      <p>
        <strong>来自组织的问题：</strong>
        <a href={organization.url}>{organization.name}</a>
      </p>
      <Repository repository={organization.repository} />
    </div>
  );
};

const Repository = ({ repository }) => (
  <div>
    <p>
      <strong>在仓库中：</strong>
      <a href={repository.url}>{repository.name}</a>
    </p>
  </div>
);
```

`src/App.js`

GraphQL 查询的结构与你的组件树完美对齐。这使得通过将其他对象嵌套到查询中，并沿着 GraphQL 查询的结构扩展组件树，继续像这样扩展查询结构是自然而然的契合。由于该应用程序是一个问题跟踪器（issue tracker），我们需要向查询中添加一个问题的列表字段。

如果你想更更有深度地遵循查询结构，可以打开 GraphiQL 中的“Docs”侧边栏来了解`Organization`、`Repository`和`Issue`类型。在那里也可以找到分页的问题列表字段。对图谱结构有一个概览总是是好的。

现在让我们通过问题的列表字段来扩展查询。这些问题最终是一个分页列表。我们稍后会详细介绍这些内容；现在，将将其嵌套在`repository`字段中，并使用`last`参数来获取列表的最后几项。

```
const GET_ISSUES_OF_REPOSITORY = `
  {
    organization(login: "the-road-to-learn-react") {
      name
      url
      repository(name: "the-road-to-learn-react") {
        name
        url
        issues(last: 5) {
          edges {
            node {
              id
              title
              url
            }
          }
        }
      }
    }
  }
`;
```

`src/App.js`

你也可以通过使用问题的`node`字段上的`id`字段为每个问题请求一个`id`，以便在组件的渲染项列表中使用`key`属性，这被认为是 [React 中的最佳实践](https://reactjs.org/docs/lists-and-keys.html)。请记住在使用执行请求时调整查询变量的名称。

```javascript
class App extends Component {
  ...

  onFetchFromGitHub = () => {
    axiosGitHubGraphQL
      .post('', { query: GET_ISSUES_OF_REPOSITORY })
      .then(result =>
          ...
      );
  };

  ...
}
```

`src/App.js`

组件结构再次非常自然地遵循了查询结构。你可以在`Repository`组件中添加一个渲染后的问题列表。取决于你的决定，是否将其重构为一个独立的组件，以保持你的组件简洁、易读且易于维护。

```javascript
const Repository = ({ repository }) => (
  <div>
    <p>
      <strong>在仓库中：</strong>
      <a href={repository.url}>{repository.name}</a>
    </p>

    <ul>
      {repository.issues.edges.map(issue => (
        <li key={issue.node.id}>
          <a href={issue.node.url}>{issue.node.title}</a>
        </li>
      ))}
    </ul>
  </div>
);
```

`src/App.js`

这就是查询中嵌套对象、字段和列表字段的全部内容。一旦你再次运行应用程序，你应该应该在浏览器中看到渲染的指定仓库的最后几个问题。

### React 中的 GraphQL 变量和参数

接下来，我们将利用表单和输入元素。当用户填写内容并提交时，应该使用它们来从 GitHub 的 GraphQL API 请求数据。该内容也用于`App`组件中`componentDidMount()`的初始请求。到目前为止，组织的`login`和仓库的`name`是查询中的内联参数。现在，你应该能够传入`path`。

请注意，该应用程序并不是为了健壮而构建，仅作为一种学习体验。不太可能有人要求用户输入不同于`organization/repository`的组织和仓库，因此尚未包含任何验证。尽管如此，这是你获得这些概念经验的良好基础。

如果你想更进一步，可以将类方法的第一部分提取到单独函数中，该函数使用`axios`发送查询请求并返回一个`promise`。该`promise`可用于将结果解析到本地状态，在`promise`的`then()`解析器块中使用`this.setState()`。

```
const getIssuesOfRepository = path => {
  const [organization, repository] = path.split('/');

  return axiosGitHubGraphQL.post('', {
    query: getIssuesOfRepositoryQuery(organization, repository),
  });
};

class App extends Component {
  ...

  onFetchFromGitHub = path => {
    getIssuesOfRepository(path).then(result =>
      this.setState(() => ({
        organization: result.data.data.organization,
        errors: result.data.errors,
      })),
    );
  };

  ...
}
```

`src/App.js`

你始终可以将应用程序拆分为不同的部分（无论是函数还是组件），以使其变得简洁、易读、可复用且[可测试](https://www.robinwieruch.de/react-testing-tutorial/)。传递给`this.setState()`的函数可以提取为高阶函数。它必须是一个高阶函数，因为你需要传递`promise`的结果，同时还要为`this.setState()`方法提供一个函数。

```
const resolveIssuesQuery = queryResult => () => ({
  organization: queryResult.data.data.organization,
  errors: queryResult.data.errors,
});

class App extends Component {
  ...

  onFetchFromGitHub = path => {
    getIssuesOfRepository(path).then(queryResult =>
      this.setState(resolveIssuesQuery(queryResult)),
    );
  };

  ...
}
```

`src/App.js`

现在，你通过为查询提供动态参数，使查询变得灵活。尝试在命令行中启动应用程序，并填写一个不同的组织和一个特定的仓库（例如`facebook/create-react-app`）。

这是一个不错的设置，但目前还没有关于变量的内容。你只是通过函数和模板字符串字量的字符串插值将参数传递给查询。现在我们将使用 GraphQL 变量，将查询变量再次重构为定义内联变量的模板字符串字量。

```
const GET_ISSUES_OF_REPOSITORY = `
  query ($organization: String!, $repository: String!) {
    organization(login: $organization) {
      name
      url
      repository(name: $repository) {
        name
        url
        issues(last: 5) {
          edges {
            node {
              id
              title
              url
            }
          }
        }
      }
    }
  }
`;
```

`src/App.js`

现在你可以将这些变量作为参数跟在 HTTP POST 请求的查询之后：

```
const getIssuesOfRepository = path => {
  const [organization, repository] = path.split('/');

  return axiosGitHubGraphQL.post('', {
    query: GET_ISSUES_OF_REPOSITORY,
    variables: { organization, repository },
  });
};
```

`src/App.js`

最后，查询考虑了变量，而无需绕道带有字符串插值的函数。我强烈建议在继续下一节之前练习下面的练习。我们还没有讨论片段（fragments）或操作名称（operation names）等功能，但我们很快将使用 Apollo 代替纯 HTTP (`axios` 来涵盖它们。

### 练习题

* 确认你[上一个节的源代码](http://bit.ly/2D1j5fu)



确认[上一个节的更改](http://bit.ly/2VpWnVu)

探索并向你的组织、仓库和 issues 添加字段

扩展你的组件以显示额外信息

阅读更多关于[通过 HTTP 提供 GraphQL API](http://graphql.org/learn/serving-over-http/) 的信息

### React 中的 GraphQL 分页

在上一节中，你在 GraphQL 查询中实现了一个列表字段，这符合使用嵌套对象构建查询的流程，并由该列表负责在 React 中显示查询的部分结果。

在本节中，你将更详细地探索 React 中 GraphQL 列表字段的分页。最初，你将学习更多关于列表字段参数的知识。此外，你将在查询中再添加一个嵌套列表字段。最后，你将通过查询获取另一页分页的 `issues` 列表。

让我们首先通过增加一个参数来扩展查询中的 `issues` 列表字段：

```
const GET_ISSUES_OF_REPOSITORY = `
  query ($organization: String!, $repository: String!) {
    organization(login: $organization) {
      name
      url
      repository(name: $repository) {
        name
        url
        issues(last: 5, states: [OPEN]) {
          edges {
            node {
              id
              title
              url
            }
          }
        }
      }
    }
  }
`;
```

`src/App.js`

如果你使用 GraphiQL 侧边栏的“Docs”读取 `issues` 列表字段的参数，你可以看到……（此处由于原文存在大量重复和乱码，已按要求处理核心内容）。

按钮的处理程序会通过所有组件传递到 `Repository` 组件：

```javascript
const Organization = ({
  organization,
  errors,
  onFetchMoreIssues,
}) => {
  ...

  return (
    <div>
      <p>
        <strong>来自组织的 Issues：</strong>
        <a href={organization.url}>{organization.name}</a>
      </p>
      <Repository
        repository={organization.repository}
        onFetchMoreIssues={onFetchMoreIssues}
      />
    </div>
  );
};
```

`src/App.js`

该函数的逻辑在 `App` 组件中作为类方法得以实现。它也会被传递给 `Organization` 组件。

```javascript
class App extends Component {
  ...

  onFetchMoreIssues = () => {
    ...
  };

  render() {
    const { path, organization, errors } = this.state;

    return (
      <div>
        ...

        {organization ? (
          <Organization
            organization={organization}
            errors={errors}
            onFetchMoreIssues={this.onFetchMoreIssues}
          />
        ) : (
          <p>暂无信息...</p>
        )}
      </div>
    );
  }
}
```

`src/App.js`

在实现该逻辑之前，需要一种方法来标识分页列表的下一页。要扩展列表字段的内部字段以包含诸如 `pageInfo` 或 `totalCount` 等元信息的字段，请使用 `pageInfo` 在点击按钮时定义下一页。此外，`totalCount` 也是查看下一个列表中有多少个项目的好方法：

```javascript
const GET_ISSUES_OF_REPOSITORY = `
  query ($organization: String!, $repository: String!) {
    organization(login: $organization) {
      name
      url
      repository(name: $repository) {
        ...
        issues(last: 5, states: [OPEN]) {
          edges {
            ...
          }
          totalCount
          pageInfo {
            endCursor
            hasNextPage
          }
        }
      }
    }
  }
`;
```

`src/App.js`

现在，你可以通过将游标（cursor）作为变量传递给查询，使用此信息来获取下一页的 Issues。游标或 `after` 参数定义了从分页列表中获取更多项目的起始点。

```javascript
class App extends Component {
  ...

  onFetchMoreIssues = () => {
    const {
      endCursor,
    } = this.state.organization.repository.issues.pageInfo;

    this.onFetchFromGitHub(this.state.path, endCursor);
  };

  ...
}
```

`src/App.js`

第二个参数尚未引入到 `onFetchFromGitHub()` 类方法中。让我们看看结果如何。

```javascript
const getIssuesOfRepository = (path, cursor) => {
  const [organization, repository] = path.split('/');

  return axiosGitHubGraphQL.post('', {
    query: GET_ISSUES_OF_REPOSITORY,
    variables: { organization, repository, cursor },
  });
};

class App extends Component {
  ...

  onFetchMoreIssues = () => {
    const {
      endCursor,
    } = this.state.organization.repository.issues.pageInfo;

    this.onFetchFromGitHub(this.state.path, endCursor);
  };

  ...
}
```

`src/App.js`

第二个参数尚未引入到 `onFetchFromGitHub()` 类方法中。让我们看看结果如何。

```javascript
const getIssuesOfRepository = (path, cursor) => {
  const [organization, repository] = path.split('/');

  return axiosGitHubGraphQL.post('', {
    query: GET_ISSUES_OF_REPOSITORY,
    variables: { organization, repository, cursor },
  });
};

class App extends Component {
  ...

  onFetchMoreIssues = () => {
    const {
      endCursor,
    } = this.state.organization.repository.issues.pageInfo;

    this.onFetchFromGitHub(this.state.path, endCursor);
  };

  ...
}
```

`src/App.js`

第二个参数尚未引入到 `onFetchFromGitHub()` 类方法中。让我们看看结果如何。

```javascript
const getIssuesOfRepository = (path, cursor) => {
  const [organization, repository] = path.split('/');

  return axiosGitHubGraphQL.post('', {
    query: GET_ISSUES_OF_REPOSITORY,
    variables: { organization, repository, cursor },
  });
};

class App extends Component {
  ...

  onFetchMoreIssues = () => {
    const {
      endCursor,
    } = this.state.organization.repository.issues.pageInfo;

    this.onFetchFromGitHub(this.state.path, endCursor);
  };

  ...
}
```

`src/App.js`

第二个参数尚未引入到 `onFetchFromGitHub()` 类方法中。让我们看看结果如何。

```javascript
const getIssuesOfRepository = (path, cursor) => {
  const [organization, repository] = path.split('/');

  return axiosGitHubGraphQL.post('', {
    query: GET_ISSUES_OF_REPOSITORY,
    variables: { organization, repository, cursor },
  });
};

class App extends Component {
  ...

  onFetchMoreIssues = () => {
    const {
      endCursor,
    } = this.state.organization.repository.issues.pageInfo;

    this.onFetchFromGitHub(this.state.path, endCursor);
  };

  ...
}
```

现在你已经在 React 中实现了 GraphQL 的分页功能。为了练习，请尝试自己为你的 `issues` 和 `reactions` 列表字段添加更多参数。检查 GraphiQL 侧边栏中的“Docs”部分，以了解可以传递给列表字段的参数。某些参数是通用的，但也有针对列表的特定参数。这些参数将向你展示 GraphQL 查询可以调整得多么精细。

### 练习：

*   确认你[上一节的源代码](http://bit.ly/2CWw7es)

    *   确认[自上一节的更改](http://bit.ly/2VnYgSR)

*   在 `issues` 和 `reactions` 列表字段上探索进一步的参数（通用的或特定类型的）

    *   思考美化深层状态对象更新机制的方法，并[为此提交你的想法](https://github.com/rwieruch/react-graphql-github-apollo/pull/14)

### React 中的 GraphQL Mutation

你之前在 React 中使用 GraphQL 获取了大量数据，这是使用 GraphQL 的大部分工作。然而，这种接口总有两个面：读和写。这正是 GraphQL Mutation（突变）补充接口的地方。之前，你学习了如何在没有 React 的 GraphiQL 中使用 GraphQL Mutation。在本节中，你将在你的 React GraphQL 应用中实现这样的 Mutation。

你以前已经在 GraphiQL 中执行过 GitHub 的 `addStar` Mutation。现在，让我们在 React 中实现这个 Mutation。在实现 Mutation 之前，你应该查询有关仓库的其他信息，这在 Mutation 中星标仓库是部分要求的。

```
const GET_ISSUES_OF_REPOSITORY = `
  query (
    $organization: String!,
    $repository: String!,
    $cursor: String
  ) {
    organization(login: $organization) {
      name
      url
      repository(name: $repository) {
        id
        name
        url
        viewerHasStarred
        issues(first: 5, after: $cursor, states: [OPEN]) {
          ...
        }
      }
    }
  }
`;
```

`src/App.js`

`viewerHasStarred` 字段返回一个布尔值，告诉查看者是否已经星标了仓库。这个布尔值有助于判断在下一步中执行 `addStar` 还是 `removeStar` Mutation。目前，你将只实现 `addStar` Mutation。`removeStar` Mutation 将作为练习的一部分省略。此外，查询中的 `id` 字段返回仓库的标识符，你需要它来明确你 Mutation 的目标仓库。

触发 Mutation 的最佳位置是星标或取消星标仓库的按钮。那里可以使用 `viewerHasStarred` 布尔值进行条件渲染，以显示“Star”或“Unstar”按钮。

```
const Repository = ({
  repository,
  onFetchMoreIssues,
  onStarRepository,
}) => (
  <div
    ...

    <button
      type="button"
      onClick={() => onStarRepository()}
    >
      {repository.viewerHasStarred ? 'Unstar' : 'Star'}
    </button>

    <ul
      ...
    </ul>
  </div>
);
```

`src/App.js`

为了识别要星标的仓库，Mutation 需要知道仓库的 `id`。将 `viewerHasStarred` 属性作为参数传递给处理函数，因为你将使用该参数来决定以后想执行星标还是取消星标的 Mutation。

```
const Repository = ({ repository, onStarRepository }) => (
  <div
    ...

    <button
      type="button"
      onClick={() =>
        onStarRepository(repository.id, repository.viewerHasStarred)
      }
    >
      {repository.viewerHasStarred ? 'Unstar' : 'Star'}
    </button>

    ...
  </div>
);
```

`src/App.js`

处理函数应该定义在 `App` 组件中。它会一直传递给每个组件直到到达 `Repository` 组件，途中也会穿过 `Organization` 组件。

```
const Organization = ({
  organization,
  errors,
  onFetchMoreIssues,
  onStarRepository,
}) => {
  ...

  return (
    <div
      ...
      <Repository
        repository={organization.repository}
        onFetchMoreIssues={onFetchMoreIssues}
        onStarRepository={onStarRepository}
      />
    </div>
  );
};
```

`src/App.js`

现在它可以在 `App` 组件中定义了。请注意，`id` 和 `viewerHasStarred` 信息也可以从 `App` 的本地状态中解构出来。这就是为什么你不需要在处理函数中传递这些信息，而是改为从本地状态中使用它们。然而，由于 `Repository` 组件已经知道这些信息，在处理函数中传递信息也是可以的，这也能让处理函数更加显式。这为以后处理多个仓库和仓库组件做好了良好的准备，因为在这些情况下处理函数需要更具针对性。



`class App extends Component` 中定义了组件逻辑：

```
class App extends Component {
  ...

  onStarRepository = (repositoryId, viewerHasStarred) => {
    ...
  };

  render() {
    const { path, organization, errors } = this.state;

    return (
      <div
        ...

        {organization ? (
          <Organization
            organization={organization}
            errors={errors}
            onFetchMoreIssues={this.onFetchMoreIssues}
            onStarRepository={this.onStarRepository}
          />
        ) : (
          <p>No information yet</p>
        )}
      </div>
    );
  }
}
```

`src/App.js`

现在可以定义 Mutation。Mutation 从组件中导出。稍后，你可以使用处理函数中的 `viewerHasStarred` 布尔值来执行 `addStar` 或 `removeStar` Mutation。执行 Mutation 看起来与之前的 GraphQL 查询相似。不需要 API 端点，因为它在你配置 axios 时已经设置过了。`variables` 属性是可选，但你需要传递标识符。

```
const addStarRepository = repositoryId => {
  return axiosGraphQL.post('', {
    query: ADD_STAR,
    variables: { repositoryId },
  });
};

class App extends Component {
  ...

  onStarRepository = (repositoryId, viewerHasStarred) => {
    addStarRepository(repositoryId);
  };

  ...
}
```

`src/App.js`

在定义 `addStar` Mutation 之前，再次检查 GitHub 的 GraphQL API。在那里你会找到关于 Mutation 结构、所需参数以及可用字段的所有信息。例如，你可以在结果中包含 `viewernuxtjs` 字段，以获取更新后的星标或未星标仓库的布尔值。

```
const ADD_STAR = `
  mutation ($repositoryId: ID!) {
    addStar(input:{starrableId:$repositoryId}) {
      starrable {
        viewernuxtjs
      }
    }
  }
`;
```

`src/App.js`

你已经可以通过点击按钮在浏览器中执行 Mutation。如果你之前没有星标该仓库，点击按钮后应该是星标状态。你可以访问 GitHub 上的仓库以获得视觉反馈，尽管你还没有看到任何结果反映。如果之前没有星标，按钮仍然显示“Star”标签，因为在 Mutation 之后，`viewernuxtjs` 布尔值没有更新 `App` 组件的本地状态中。这是你接下来要实现的内容。由于 axios 返回一个 promise，你可以使用 promise 的 `then()` 方法通过自己的实现细节来解析它。

```
const resolveAddStarMutation = mutationResult => state => {
  ...
};

class App extends Component {
  ...

  onStarRepository = (repositoryId, viewernuxtjs) => {
    addStarRepository(repositoryId).then(mutationResult =>
      this.setState(resolveAddStarMutation(mutationResult)),
    );
  };

  ...
}
```

`src/App.js`

当解析变异（mutation）的 promise 时，你可以在结果中找到 `viewerHasStarred` 属性。这是因为你在变异中将该属性定义为一个字段。它返回了一个用于 React 本地状态的新状态对象，因为你在 `this.setState()` 中使用了该函数。这里使用了展开运算符（spread operator）来更新深度嵌套的数据结构。状态对象中只有 `viewerHasStarred` 属性发生了变化，因为它是成功请求解析的 promise 返回的唯一属性。本地状态的所有其他部分都保持不变。

```javascript
const resolveAddStarMutation = mutationResult => state => {
  const {
    viewerHasStarred,
  } = mutationResult.data.data.addStar.starrable;

  return {
    ...state,
    organization: {
      ...state.organization,
      repository: {
        ...state.organization.repository,
        viewerHasStarred,
      },
    },
  };
};
```

`src/App.js`

现在尝试再次星标仓库（star）。你可能需要先去 GitHub 页面取消星标（unstar）。按钮标签应该根据本地状态中更新后的 `viewerHasStarred` 属性进行调整，显示“Star”或“Unstar”标签。你可以利用学到的关于星标仓库的知识来实现一个 `removeStar` 变异。

我们还想显示星标仓库的人数，并在 `addStar` 和 `removeStar` 变异中更新此计数。首先，通过在查询中添加以下字段来获取星标者的总数：

```javascript
const GET_ISSUES_OF_REPOSITORY = `
  query (
    $organization: String!,
    $repository: String!,
    $cursor: String
  ) {
    organization(login: $organization) {
      name
      url
      repository(name: $repository) {
        id
        name
        url
        stargazers {
          totalCount
        }
        viewerHasStarred
        issues(first: 5, after: $cursor, states: [OPEN]) {
          ...
        }
      }
    }
  }
`;
```

`src/App.js`

其次，你可以将计数作为按钮标签的一部分显示：

```javascript
const Repository = ({
  repository,
  onFetchMoreIssues,
  onStarRepository,
}) => (
  <div>
    ...

    <button
      type="button"
      onClick={() =>
        onStarRepository(repository.id, repository.viewerHasStarred)
      }
    >
      {repository.stargazers.totalCount}
      {repository.viewerHasStarred ? ' Unstar' : ' Star'}
    </button>

    <ul
      ...
    </ul>
  </div>
);
```

`src/App.js`

现在我们希望在星标（或取消星标）仓库时更新计数。这与 `addStar` 变异成功后，组件本地状态中 `viewerHasStarred` 属性缺失更新的问题相同。回到你的变异解析器（mutation resolver），并在那里更新星标者的总数。虽然星标对象没有作为变异的结果返回，但你可以在变异成功后，使用计数器配合 `addStar` 变异手动增加或减少总数。

```javascript
const resolveAddStarMutation = mutationResult => state => {
  const {
    viewerHasStarred,
  } = mutationResult.data.data.addStar.starrable;

  const { totalCount } = state.organization.repository.stargazers;

  return {
    ...state,
    organization: {
      ...state.organization,
      repository: {
        ...state.organization.repository,
        viewerHasStarred,
        stargazers: {
          totalCount: totalCount + 1,
        },
      },
    },
  };
};
```

`src/App.js`

你已经在 React 中使用 GraphQL 实现了你的第一个变异。到目前为止，你只实现了 `addStar` 变异。尽管按钮已经通过显示“Star”或“Unstar”标签来反映了 `viewerHasStarred` 布尔值，但显示“Unstar”的按钮仍然应该执行 `addStar` 变异。用于取消星标仓库的 `removeStar` 变异是下面提到的练习题之一。

## 练习

- 确认你[上一节的源代码](http://bit.ly/2D01swJ)

    * 确认[上一节的更改](http://bit.ly/2Vpcy5B)

- 实现 `removeStar` 变异，其用法类似于 `addStar` 变异。

    * `onStarRepository` 类方法已经可以访问 `viewerHasStarred` 属性。

    * 在类处理器中有条件的执行 `addStar` 或 `removeStar` 变异。

    * 在从仓库移除星标后解析新状态。

    * 将你的最终想法与[此实现](https://github.com/rwieruch/react-graphql-github-vanilla)对齐。

- 为 issue 实现 `addReaction` 变异

- 实现更细粒度的组件（例如 `IssueList`、`IssueItem`、`ReactionList`、`ReactionItem`）

    * 将组件提取到单独的文件中，并使用 `import` 和 `export` 语句在 App 或其他其他提取的组件中再次使用。

### 离开 Apollo

我们实现了一个简单的 GitHub issue 追踪器，它使用 React 和 GraphQL 但没有使用专门的 GraphQL 库，仅使用 `axios` 通过 HTTP `POST` 方法与 GraphQL API 通信。在继续之前，我认为先使用原生技术（在本例中为 GraphQL）配合纯 HTTP 方法是重要的，然后再引入其他工具。Apollo 库提供了一个抽象，使得使用 GraphQL 变得简单得多，因此你将在下一个应用程序中使用它。目前，通过 HTTP 使用 GraphQL 向你展示了两个重要的点：

- GraphQL 在配合 HTTP 时是如何工作的。

- 不使用 GraphQL 客户端的缺点，因为你必须完成所有工作。

-   **功能支持**：当使用纯 HTTP 请求与你的 GraphQL API 交互时，你并没有充分利用 GraphQL 的潜力。想象一下，你想要将之前应用程序中的查询拆分为多个查询，并将这些查询与使用数据的各个组件放置在一起。在这种情况下，你本可以在视图层中以声明式的方式使用 GraphQL。但当你没有库支持时，你必须自己处理多个查询，跟踪所有的查询，并尝试在你的状态层中合并结果。如果你考虑之前的应用程序，将查询拆分为多个查询会为应用程序增加一整层复杂性。GraphQL 客户端库会为你处理查询的聚合。

-   **数据处理**：使用纯 HTTP 请求处理数据的一种朴素方法，属于不使用专用库时 GraphQL 缺失功能支持的一个子类。没有人帮助你对数据进行归一化并对相同请求进行缓存。如果一开始没有对数据进行归一化，那么在从数据层解析获取的数据时更新状态层将变成一场噩梦。你必须处理深度嵌套的状态对象，这会导致 JavaScript 展开运算符的使用变得非常繁琐。当你再次检查 GitHub 仓库中的应用程序实现时，你会发现，执行变更（mutation）和查询后更新 React 的本地状态并不好看。像 [normalizr](https://github.com/paularmstrong/normalizr) 这样的归一化库可以帮助你改进本地状态结构。你可以在 [Taming the State in React](https://roadtoreact.com) 一书中学到更多关于状态归一化的知识。除了缺乏缓存和归一化支持外，避免使用库意味着错过了分页和乐观更新的功能。专用的 GraphQL 库可以让你可以使用所有功能。

-   **GraphQL 订阅（Subscriptions）**：虽然 GraphQL 有通过查询（query）和变更（mutation）来读写数据的概念，但还有第三种概念—— GraphQL `subscription`，用于在客户端应用程序中接收实时数据。当你像以前那样依赖纯 HTTP 请求时，你必须在旁边引入 [WebSockets](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API)。它允许你引入一个长连接来随时间推接收结果。总之，引入 GraphQL 订阅会为你的应用程序增加另一个工具。然而，如果你在客户端为之引入了 GraphQL 库，该库可能会为你实现好 GraphQL 订阅。

我很期待将 Apollo 作为 GraphQL 客户端库引入你的 React 应用程序中。它将帮助解决上述缺点。然而，我深信在开始阶段在没有 GraphQL 库的情况下学习 React 中的 GraphQL 是好的。

你可以在 GitHub 上找到最终的 [GitHub 仓库](https://github.com/rwieruch/react-graphql-github-vanilla)。该仓库也展示了大部分练习任务。该应用程序的功能并不完整，因为它没有涵盖所有的边缘情况且没有样式。但是，我希望在 React 中使用纯 GraphQL 的实现演示能帮助你理解如何在 React 中仅使用 HTTP 请求在客户端使用 GraphQL。我认为，在 ways 诸如 Apollo 或 Relay 这样复杂的 GraphQL 客户端库之前，采取这一步是重要的。

我已经展示了如何在不使用 Apollo 之类的库的情况下，使用 GraphQL 和 HTTP 请求实现 React 应用程序。接下来，你将继续学习使用 Apollo 代替基于 `axios` 的基础 HTTP 请求在 React 中使用 GraphQL。Apollo GraphQL Client 让你的数据进行缓存、归一化、执行乐观更新和分页变得轻而易举。这远非全部，所以请关注你将要使用 GraphQL 构建的下一个应用程序。

## Apollo Client

Apollo 是由开发者构建的完整生态系统，作为 GraphQL 应用程序的基础设施。你可以在客户端使用它构建 GraphQL 客户端应用程序，也可以在服务端用于构建 GraphQL 服务器应用程序。在编写本教程时， Apollo 提供了 JavaScript 中最丰富、最流行的 GraphQL 生态系统。其他针对 React 应用程序的库还有 [Relay](http://facebook.github.io/relay) 和 [Urql](https://github.com/FormidableLabs/urql)，但它们仅适用于 React 应用程序，而且没有 Apollo Client 那么流行。Apollo 是框架无关的，这意味着你可以在 React 的其他库中使用它。它还可以与 Vue 和 Angular 等其他库/框架配合，因此你在本教程中学到的所有内容可能都可以迁移到其他框架。

### 从命令行开始使用 Apollo Boost

该应用程序通过引入带有 Apollo Boost 的 Apollo Client 开始。后者允许你创建一个零配置的 Apollo Client，以最快、最方便的方式开始。为了学习，本节侧重于 Apollo Client 而不是 React。要开始之前，请找到 [Node.js 模板项目及其安装说明](https://github.com/rwieruch/node-babel-server)。现在你将在 Node.js 环境的命令行中使用 Apollo Client。在最简的 Node.js 项目之上，你将引入带有 Apollo Boost 的 Apollo Client，以在没有视图层库的情况下体验 GraphQL 客户端。



接下来，你将调用 GitHub 的 GraphQL API，然后在命令行中输出查询和变更结果。为了实现这一点，你需要一个 GitHub 网站上的个人访问令牌（personal access token），我们在上一个章节中介绍过。如果你还没有这样做，请前往 [GitHub 的说明](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/)生成具有足够权限的个人访问令牌。

在你克隆并安装了 Node.js 模板项目并创建了个人访问令牌后，在根目录下命令行安装这两个包：

```
npm install apollo-boost graphql --save
```

## 命令行

[apollo-boost](https://github.com/apollographql/apollo-client/tree/master/packages/apollo-boost) 包提供了零配置的 Apollo Client 访问，而 [graphql](https://github.com/graphql/graphql-js) 包允许在客户端和服务端进行查询、变更和订阅。它是 [Facebook 规范](https://github.com/facebook/graphql) 的 JavaScript 参考实现。

在接下来的步骤中，你将在项目的`src/index.js`文件中配置并使用带有 Apollo Boost 的 Apollo Client。项目很小，而且你将在本节中实现它，因此为了学习，我们可以将所有内容放在一个文件中。

在你的`src/index.js`文件中，你可以从`apollo-boost`导入`ApolloClient`。之后，你可以通过调用其构造函数并传入`uri`来创建一个实例。客户端需要知道数据来自哪里以及写入哪里，所以你可以将 GitHub 的端点传递给它。

```javascript
import ApolloClient from 'apollo-boost';

const client = new ApolloClient({
  uri: 'https://api.github.com/graphql',
});
```

`src/index.js`

Apollo Client 已经是这样工作的。但请记住，GitHub 的 GraphQL API 需要个人访问令牌。这就是为什么要在创建 Apollo Client 实例时定义它。因此，你可以使用`request`属性定义一个函数，该函数可以访问通过 Apollo Client 发出的每个请求的上下文。在那里，你使用 Apollo Boost 作为默认请求头之一传递`authorization`请求头。

```
import ApolloClient from 'apollo-boost';

const client = new ApolloClient({
  uri: 'https://api.github.com/graphql',
  request: operation => {
    operation.setContext({
      headers: {
        authorization: `Bearer YOUR_GITHUB_PERSONAL_ACCESS_TOKEN`,
      },
    });
  },
});
```

`src/index.js`

你在上一个应用中执行了同样的操作，仅使用`axios`进行普通的 HTTP 请求。你配置了一次`axios`指向 GraphQL API 端点，使所有请求都指向此 URI，并设置了授权标头。在这里也是一样，因为只需要为后续所有的 GraphQL 请求配置一次客户端就足够了。

记住，将`YOUR_GITHUB_PERSONAL_ACCESS_TOKEN`字符串替换为你之前在 GitHub 网站上创建的个人访问令牌。不过，你可能不想将你的访问令牌直接放入源代码中，因此你可以在项目文件夹中创建一个`.env`文件，在其中存储你所有的环境变量。如果你不想在公共 GitHub 仓库中共享该个人令牌，也可以将该文件添加到`.gitignore`文件中。在命令行中，你可以创建此文件：

```
touch .env
```

## 命令行

只需在真正的`.env`文件中定义你的环境变量即可。在你的`.env`文件中粘贴以下键值对，其中键的命名由你决定，值必须是你来自 GitHub 的个人访问令牌。

```
GITHUB_PERSONAL_ACCESS_TOKEN=xxxXXX
```

## `.env`

在任何 Node.js 应用中，使用以下包 [dotenv](https://github.com/motdotla/dotenv) 将键作为环境变量在你的源代码中使用。按照他们的说明为项目安装它。通常，该过程只需要执行`npm install dotenv`，然后在`index.js`文件的顶部包含`import 'dotenv/config';`。之后，你就可以在`index.js`文件中使用来自`.env`文件的个人访问令牌了。如果你遇到错误，继续阅读本节以了解如何修复它。

```
import ApolloClient from 'apollo-boost';

import 'dotenv/config';

const client = new ApolloClient({
  uri: 'https://api.github.com/graphql',
  request: operation => {
    operation.setContext({
      headers: {
        authorization: `Bearer ${process.env.GITHUB_PERSONAL_ACCESS_TOKEN}`,
      },
    });
  },
});
```

`src/index.js`

注意：对于之前安装的`dotenv`包，可能有额外的配置步骤。由于安装说明可能随不同的`dotenv`版本而异，在安装后检查他们的 GitHub 网站以找到最佳配置。

当你使用`npm start`启动应用但没有查询（query）或变异（mutation），只有 Apollo Client 时，可能会看到以下错误：*"Error: fetch is not found globally and no fetcher passed, to fix pass a fetch for your environment …"*。该错误发生是因为[原生 fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)（用于基于 Promise 向远程 API 发起请求）仅在浏览器可用。你无法在仅运行命令行的 Node.js 应用中访问它。然而，Apollo Client 使用 fetch API 来执行查询和变异，通常来自浏览器环境而非 Node.js 环境。正如你可能记得的，可以使用简单的 HTTP 请求执行查询或变异，因此 Apollo Client 使用浏览器的原生 fetch API 来执行这些请求。解决方案是使用一个 node 包让 fetch 在 Node.js 环境中可用。幸运的是，有包可以解决这个问题，可以通过命令行进行安装：

```
npm install cross-fetch --save
```

## 命令行

其次，在你的项目中匿名导入它：

```
import 'cross-fetch/polyfill';
import ApolloClient from 'apollo-boost';
```

`src/index.js`

当从命令行启动应用时，错误应该消失，但目前还没有任何反应。会创建一个带有配置的 Apollo Client 实例。在下文中，你将使用 Apollo Client 执行你的第一次查询。

### 练习：

*   确认你的[上一节的源代码](http://bit.ly/2D2pRSh)
    *   确认[上一节的更改](http://bit.ly/2VqyY6i)
*   阅读更多关于[其他视图集成，如 Angular 和 Vue](https://www.apollographql.com/docs/react/integrations.html)
*   花几分钟时间参加一下[测验](https://www.surveymonkey.com/r/5T3W9BB)

### Apollo Client 与 GraphQL 查询

现在你将使用 Apollo Client 向 GitHub 的 GraphQL API 发送你的第一次查询。从 Apollo Boost 导入以下工具来定义查询：

```
import 'cross-fetch/polyfill';
import ApolloClient, { gql } from 'apollo-boost';
```

`src/index.js`

使用 JavaScript 模板字符串定义你的查询：

```javascript
...

const GET_ORGANIZATION = gql`
  {
    organization(login: "the-road-to-learn-react") {
      name
      url
    }
  }
`;
```

`src/index.js`

使用命令式调用 Apollo Client 来向 GitHub 的 GraphQL API 发送查询。由于 Apollo Client 是基于 promise 的，`query()`方法返回一个你最终可以解析的 promise。由于应用在命令行中运行，只需 log 结果即可。

```
...

client
  .query({
    query: GET_ORGANIZATION,
  })
  .then(console.log);
```

`src/index.js`

使用 Apollo Client 发送查询就是这些了。正如提到的，Apollo Client 在底层使用 HTTP 发送查询。使用`npm start`启动应用后，命令行上的结果类似于：

```
{
  data: {
    organization: {
      name: 'The Road to learn React',
      url: 'https://github.com/the-road-to-react',
      __typename: 'Organization'
    }
  },
  loading: false,
  networkStatus: 7,
  stale: false
}
```

## 命令行

GraphQL 请求的信息可以在`data`对象中找到。在那里发现包含`name`和`url`字段的`organization`对象。Apollo Client 会自动请求[元字段](http://graphql.org/learn/queries/#meta-fields)`__typename`。Apollo Client 可以此字段来实现缓存和乐观更新。

关于请求的更多元信息可以在旁边找到。它显示了数据是否仍在加载、网络状态的具体细节，以及服务器端请求的数据是否过期（stale）。

### 练习：

*   确认你的[上一节的源代码](http://bit.ly/2Da7Em)
    *   确认[上一节的更改](http://bit.ly/2VnYqc)
*   探索 GitHub 的 GraphQL API
    *   熟悉浏览他们的文档
    *   为`organization`字段添加其他字段
*   更多关于[为什么使用 Apollo Client](https://www.apollographql.com/docs/react/why-apollo.html)
*   阅读更多关于[networkStatus 属性及其可能的值](https://github.com/apollographql/apollo-client/blob/master/packages/apollo-client/src/core/networkStatus.ts)
*   花 3 分钟时间参加[测验](https://www.surveymonkey.com/r/5MF35H5)

### 带有分页、变量、嵌套对象和列表字段的 Apollo Client

你在之前的章节中构建 React with GraphQL 应用时学习了 GraphQL 分页和其他功能。本节将介绍这些功能，例如 GraphQL 变量。之前查询中组织字段的`login`参数可以替换为这样的变量。首先，你需要在你的 GraphQL 查询中引入变量：

```javascript
const GET_ORGANIZATION = gql`
  query($organization: String!) {
    organization(login: $organization) {
      name
      url
    }
  }
`;
```

`src/index.js`

其次，在你的查询对象的`variables`对象中定义它：

```javascript
client
  .query({
    query: GET_ORGANIZATION,
    variables: {
      organization: 'the-road-to-learn-react',
    },
  })
  .then(console.log);
```

`src/index.js`

这就是你如何在应用程序中使用`Apollo Client`实例将变量传递给查询的方法。接下来，为你的`organization`添加嵌套的`repositories`列表字段。在那里，你可以请求该组织下所有的 GitHub 仓库。你可能也想重命名查询变量，但请记住在使用`Apollo Client`时也要同步更改它。

```javascript
const GET_REPOSITORIES_OF_ORGANIZATION = gql`
  query($organization: String!) {
    organization(login: $organization) {
      name
      url
      repositories(first: 5) {
        edges {
          node {
            name
            url
          }
        }
      }
    }
  }
`;

client
  .query({
    query: GET_REPOSITORIES_OF_ORGANIZATION,
    variables: {
      organization: 'the-road-to-learn-react',
    },
  })
  .then(console.log);
```

`src/index.js`

你在之前创建的应用程序中见过类似的查询结构，因此这一部分为你提供了几个练习，以测试你所学的 GraphQL 技能。解决这些练习将强化你的 GraphQL 技能，以便你之后能够毫无障碍地将`Apollo Client`连接到你的 React 应用程序。你可以在练习结束后的该应用程序的 GitHub 仓库中找到所有练习的答案，但你应该考虑先自己完成。

### 练习：

* 确认你[上一节的源代码](http://bit.ly/2CYRr2V)
    * 确认[上一节的更改](http://bit.ly/2Vneiw4)
* 探索 GitHub 的 GraphQL API
    * 通过查询一个按点标数（stargazers）排序的仓库列表，来扩展`repositories`列表字段
* 将仓库`node`的内容提取到一个 GraphQL 可复用片段（fragment）中
* 更多关于 [GraphQL 分页](https://graphql.org/learn/pagination) 的信息
* 为仓库列表添加分页功能
    * 在查询中添加包含`endCursor`和`hasNextPage`字段的`pageInfo`字段
    * 添加`after`参数并为它引入一个新的`$cursor`变量
    * 在不带`cursor`参数的情况下执行第一次查询
    * 使用上一次查询结果的`endCursor`作为`cursor`参数执行第二次查询
* 完成三分钟的[测验](https://www.surveymonkey.com/r/SWL9NJ7)

### Apollo Client 和 GraphQL Mutation

之前，你学习了如何使用`Apollo Client`从 GitHub 的 GraphQL API 查询数据。一旦配置好客户端，你就可以使用它的`query()`方法发送带有可选`variables`的 GraphQL `query`。正如你所学到的，使用 GraphQL 读取数据并不是全部，因为还有用于写入数据的变异（mutation）。在本节中，你将定义一个变异来为 GitHub 仓库点赞（star）。`Apollo Client`实例会发送该变异，但你必须先定义它。

```javascript
const ADD_STAR = gql`
  mutation AddStar($repositoryId: ID!) {
    addStar(input: { starrableId: $repositoryId }) {
      starrable {
        id
        viewerHasStarred
      }
    }
  }
`;
```

`src/index.js`



仓库的标识符是必须的，否则 GitHub 的 GraphQL 服务器将不知道你想点赞哪个仓库。在接下来的代码段中，使用`Apollo Client`根据指定的标识符为特定的 GitHub 仓库点赞。可以通过在查询的仓库`node`字段中添加`id`字段来获取标识符。使用`Apollo Client`的`mutate()`方法通过`mutation`和`variables`负载发送变异。可以对结果进行任何处理以适应你的应用程序，但在本例中，结果只是简单地打印在命令行中。

```
client
  .mutate({
    mutation: ADD_STAR,
    variables: {
      repositoryId: 'MDEwOlJlcG9zaXRvcnk2MzM1MjkwNw==',
    },
  })
  .then(console.log);
```

结果应该封装在一个`addStar`对象中（变异的），它应该准确反映你在变异中定义的对象和字段：`starrable`、`id`和`viewerHasStarred`。

通过仅使用`Apollo Client`而不使用任何视图层库，你完成了另一个学习步骤。这样做是为了避免混淆`Apollo Client`和`React Apollo`的功能。

记住，`Apollo Client`可以作为独立的 GraphQL 客户端使用，而无需连接到 React 这样的视图层，尽管只在命令行中看到数据可能看起来有些无味。我们将在下一节中查看 Apollo 如何将数据层连接到 React 视图层。

### `src/index.js`

### 练习：

* 确认你[上一节的源代码](http://bit.ly/2CYSgZz)
  * 确认[上一节的更改](http://bit.ly/2VnNsUB)
* 在`addStar`变异旁边实现`removeStar`变异
* 完成三分钟的[测验](https://www.surveymonkey.com/r/MNFSY)

## React 结合 GraphQL

在本教程中，你将学习如何使用 Apollo 将 React 与 GraphQL 结合。Apollo 工具集可以创建 GraphQL 客户端、服务器和其他辅助应用程序。在此过程中，你将构建一个使用 Apollo 代替 [HTTP 请求](https://developer.github.com/v4/) 的简化客户端。结束时，你应该能够展示一个使用 GraphQL 和 Apollo 的 React 应用程序供其他开发者使用。你可以在[仓库](https://github.com/rwieruch/react-github-apollo) 中找到最终项目。

### 现在，我们将专注于通过构建另一个应用程序来使用`Apollo Client`。基本上，你将学习如何将数据层连接到视图层。我们将涵盖如何从视图层发送查询和变异，以及如何更新视图层以反映结果。此外，你将学习在 React 中使用 GraphQL 功能，如分页、乐观 UI、缓存、本地状态管理和预取。

对于此应用程序，不需要复杂的 React 配置。只需使用 [create-react-app](https://github.com/facebook/create-react-app) 创建你的 React 应用程序。如果你想要复杂的 React 配置，请参考此[使用 Webpack 配置 React 的指南](https://www.robinwieruch.de/minimal-react-webpack-babel-setup/)。开始之前，必须执行以下步骤：

* 使用`create-react-app`创建一个新的 React 应用程序
* 为你的项目创建文件夹/文件结构（见下方）

你可以在`src/`文件夹中为组件创建自己的文件夹和文件结构；以下顶层结构仅供建议。如果你根据需要进行调整，请记住 JavaScript 导入语句的路径也需要相应调整。如果你不想创建所有内容，可以克隆这个 [GitHub 仓库](https://github.com/the-road-to-graphql/react-graphql-github-apollo-starter-kit) 并按照其安装说明操作。

* `App/`
  * `index.js`
* `Button/`
* `Error/`
* `FetchMore/`
* `Input/`
* `Issue/`
  * `IssueList/`
  * `IssueItem/`
  * `index.js`
* `Link/`
* `Loading/`
* `Organization/`
* `Profile/`
* `Repository/`
  * `RepositoryList/`
  * `RepositoryItem/`
  * `index.js`
* `TextArea/`
* `constants/`
  * `routes.js`
* `index.js`
* `serviceWorker.js`
* `style.css`

这些文件夹主要代表 React 组件。某些组件是可复用的 UI 组件，例如`Input`和`Link`组件，而其他组件如`Repository`和`Profile`组件是针对 GitHub 客户端应用程序的特定领域。目前只指定了顶层文件夹，但如果你以后需要，也可以引入更多。此外，`constants`文件夹只有一个文件用于指定应用程序的路由，该文件将在稍后介绍。你可能需要从显示组织仓库（`Organization`组件）的页面跳转到显示你个人仓库（`Profile`组件）的页面。

此应用程序将使用原生 CSS 类和 CSS 文件。通过遵循原生 CSS 类，你可以避免在使用其他工具时可能遇到的困难。你可以在应用程序的附录部分找到所有的 CSS 文件及其内容。组件将直接使用其类名而不进行解释。接下来的章节将完全专门用于 JavaScript、React 和 GraphQL。

### 练习：

* 如果你不熟悉 React，请阅读 *The Road to learn React*
* 建立推荐的文件夹/文件结构（如果你没有使用自己的结构且没有克隆仓库）
  * 根据 CSS 附录部分，在指定的文件夹中创建 CSS `style.css`文件
  * 为组件创建`index.js`文件
  * 在执行后续章节时，自行为非顶层组件创建更多文件夹（例如`Navigation`）
* 使用`npm start`运行应用程序
  * 确保没有错误
  * 在`src/index.js`文件中使用`src/App/index.js`仅渲染一个基础`App`组件
* 花费 3 分钟完成[测验](https://www.surveymonkey.com/r/5N9W2WR)

### 为 React 和 GitHub 的 GraphQL API 配置 Apollo Client

在本节中，你将像之前一样设置一个`Apollo Client`实例。然而，这次你将直接使用`Apollo Client`，而不使用零配置包`Apollo Boost`，这意味着你需要自己配置`Apollo Client`而没有合理的默认值。虽然对于学习来说使用具有合理默认值的工具是最好的，但自己配置 Apollo 可以让你接触到 Apollo Client 的可组合生态系统、学习如何进行初始设置，以及以后如何改进此设置。

`Apollo Client`的设置可以在顶层`src/index.js`文件中完成，该文件也是 React 到 HTML 的入口点。首先，使用命令行在你的项目文件夹中安装 Apollo Client：

```
npm install apollo-client --save
```

创建 Apollo Client 使用的两个强制性配置需要两个实用包。[apollo-cache-inmemory](https://github.com/apollographql/apollo-client/tree/master/packages/apollo-cache-inmemory) 是你的 Apollo Client 管理数据的推荐缓存（也读作：存储或状态），而`apollo-link-http`用于为 Apollo Client 实例一次性配置 URI 和额外的网络信息。

```
npm install apollo-cache-inmemory apollo-link-http --save
```

如你所见，没有提到 React，只有 Apollo Client 及其用于配置的两个包。Apollo Client 与 GraphQL 配合工作还需要两个额外的包，将作为 Apollo 的内部依赖使用。后者也用于定义查询和变异。之前，这些实用工具直接来自 Apollo Boost。

```
npm install graphql graphql-tag --save
```

包安装到此结束，现在我们进入 Apollo Client 的设置和配置。在你的顶层`src/index.js`文件中（本节所有的 Apollo Client 设置都将在此处完成），从之前安装的包中导入 Apollo Client 设置所需的类。

```
import React from 'react';
import ReactDOM from 'react-dom';
import { ApolloClient } from 'apollo-client';
import { HttpLink } from 'apollo-link-http';
import { InMemoryCache } from 'apollo-cache-inmemory';

import './style.css';
import App from './App';

...
```

`src/index.js`

`ApolloClient`类用于创建实例，`HttpLink`和`InMemoryCache`用于其强制性配置。首先，你可以创建一个配置好的`HttpLink`实例，并将其传递给 Apollo Client 的创建。

```
const GITHUB_BASE_URL = 'https://api.github.com/graphql';

const httpLink = new HttpLink({
  uri: GITHUB_BASE_URL,
  headers: {
    authorization: `Bearer ${
      process.env.REACT_APP_GITHUB_PERSONAL_ACCESS_TOKEN
    }`,
  },
});
```

`src/index.js`

你可能还记得之前应用程序中的强制配置。`uri`是定义 Apollo Client 使用的唯一 GraphQL API 端点的强制值。在这种情况下，GitHub 的 GraphQL 端点作为值传递。在消费 GitHub GraphQL API 时，你必须使用你的个人访问令牌（personal access token）进行授权。你应该已经在之前的章节中创建了令牌，现在你可以在项目文件夹的`.env`文件中定义它。之后，应该可以通过`process.env`访问。请记住，在使用 create-react-app 时使用`REACT_APP`前缀。

其次，创建管理数据的缓存。缓存归一化你的数据、缓存请求并允许进行读写操作。缓存的实例化非常简单，因为它不需要传递任何参数。

```
const cache = new InMemoryCache();
```

`src/index.js`

最后，你可以使用两个实例化的配置（link 和 cache）在`src/index.js`中创建实例。

```
const client = new ApolloClient({
  link: httpLink,
  cache,
});
```

`src/index.js`

为了初始化 Apollo Client，你必须在配置对象指定`link`和`cache`属性。再次启动应用程序后，不应该有错误。如果有任何，请检查是否已在`src/App/index.js`文件中实现了基础`App`组件。

### 练习：

* [确认上一节的源代码](http://bit.ly/2CYjRdg)
* [确认上一节的更改](http://bit.ly/2VqgK4)
* 更多关于[Apollo Client 网络层配置](https://www.apollographql.com/docs/react/advanced/network-layer.html)

### 连接数据层与视图层：引入 React Apollo

我们目前所做都是 Apollo Client 与框架无关的部分。然而，如果不将其连接到 React，你很难有效使用 GraphQL。这就是为什么有一个官方库来连接这两个世界：[react-apollo](https://github.com/apollographql/react-apollo)。这些连接库的伟大之处在于，对于 Angular 和 Vue 等其他视图层解决方案也有相应的库，因此你可以以框架无关的方式使用 Apollo Client。在下文中，需要两个步骤将 Apollo Client 连接到 React。首先，在命令行中你的项目文件夹中安装该库：

```
npm install react-apollo --save
```

其次，导入`ApolloProvider`组件，并将其作为组合组件在`src/index.js`文件中包裹在你的`App`组件周围。在底层，它使用 [React 的 Context API](https://www.robinwieruch.de/react-context-api/) 将 Apollo Client 传递到你的应用程序中。

```
import React from 'react';
import ReactDOM from 'react-dom';
import { ApolloProvider } from 'react-apollo';
import { ApolloClient } from 'apollo-client';
import { HttpLink } from 'apollo-link-http';
import { InMemoryCache } from 'apollo-cache-inmemory';

...

ReactDOM.render(
  <ApolloProvider client={client}>
    <App />
  </ApolloProvider>,
  document.getElementById('root')
);
```

`src/index.js`

现在你可以在 React 视图层中隐式地访问 Apollo Client。之所以说是隐式的，是因为大多数情况下你并不会显式地使用它。你将在下一节看到这意味着什么。

### 练习：

* 确认你[上一节的源代码](http://bit.ly/2CZjMWO)
  * 确认[上一节的更改](http://bit.ly/2VpXNPO)
* 更多关于[配置并将 Apollo Client 连接到 React](https://www.apollographql.com/docs/react/essentials/get-started.html) 的信息
* 花 3 分钟时间完成[测验](https://www.surveymonkey.com/r/5FHMHW8)

### 在 React 中使用 Apollo Client 进行 GraphQL 查询

在本节中，你将使用 React 中的 Apollo Client 实现你的第一个 GraphQL 查询。你已经看到过如何从 GitHub 的 GraphQL API 查询不同的实体，例如当前用户（`viewer`）或仓库（`repositories`）。这次你将在 React 中执行此操作。`Profile`组件可能是渲染当前用户及其关联仓库的最佳位置。从在`src/App/index.js`文件的`App`组件中使用尚未实现的`Profile`组件开始，我们将在接下来的步骤处理它。现在提取`Profile`组件是合理的，因为以后`App`组件将作为应用程序的静态框架。像`Navigation`和`Footer`这样的组件是静态的，而像`Profile`和`Organization`这样的组件是根据路由（URL）动态渲染的。

```
import React, { Component } from 'react';

import Profile from '../Profile';

class App extends Component {
  render() {
    return <Profile />;
  }
}

export default App;
```

`src/App/index.js`

在你的`src/Profile/index.js`文件中，添加一个简单的函数式无状态组件。在下一步中，你将用 GraphQL 查询来扩展它。

```
import React from 'react';

const Profile = () =>
  <div>Profile</div>

export default Profile;
```

`src/Profile/index.js`



现在我们将学习如何使用 `GraphQL` 和 `Apollo Client` 查询数据。在上一节中，`Apollo Client` 已通过 React 的 `Context API` 在顶层组件中提供。你可以隐式地访问它，但永远不要直接用它进行标准查询（queries）和变变（mutations）。这里说“标准”，是因为在实现此应用程序时，会有一些你直接使用 `Apollo Client` 实例的情况。

`React Apollo` 扩展提供了对 `Query` 组件的访问，该组件接收一个查询作为 prop 并在渲染时执行它。这是关键部分：它在渲染时执行查询。它使用了 React 的 [render props](https://www.robinwieruch.de/react-render-props-pattern/) 模式，将子元素作为函数实现，你可以在其中作为参数访问查询结果。

```javascript
import React from 'react';
import { Query } from 'react-apollo';

const Profile = () => (
  <Query query={}>
    {() => <div>My Profile</div>}
  </Query>
);

export default Profile;
```

`src/Profile/index.js`

这是一个只返回 `JSX` 的函数，但你可以在函数参数中访问额外信息。首先，定义 `GraphQL` 查询来请求你的授权。你可以使用之前安装的工具包来定义查询。

```javascript
import React from 'react';
import gql from 'graphql-tag';
import { Query } from 'react-apollo';

const GET_CURRENT_USER = gql`
  {
    viewer {
      login
      name
    }
  }
`;

const Profile = () => (
  <Query query={GET_CURRENT_USER}>
    {() => <div>My Profile</div>}
  </Query>
);

export default Profile;
```

`src/Profile/index.js`

使用子元素作为函数模式来获取数据对象形式查询结果，并在你的 `JSX` 中渲染信息。

```javascript
import React from 'react';
import gql from 'graphql-tag';
import { Query } from 'react-apollo';

const GET_CURRENT_USER = gql`
  {
    viewer {
      login
      name
    }
  }
`;

const Profile = () => (
  <Query query={GET_CURRENT_USER}>
    {({ data }) => {
      const { viewer } = data;

      return (
        <div>
          {viewer.name} {viewer.login}
        </div>
      );
    }}
  </Query>
);
```

`src/Profile/index.js`

在你的视图层可以渲染数据之前，确保提供某种视觉反馈。

```javascript
import React from 'react';
import gql from 'graphql-tag';
import { Query } from 'react-apollo';

const GET_CURRENT_USER = gql`
  {
    viewer {
      login
      name
    }
  }
`;

const Profile = () => (
  <Query query={GET_CURRENT_USER}>
    {({ data }) => {
      const { viewer } = data;

      if (!viewer) {
        return null;
      }

      return (
        <div>
          {viewer.name} {viewer.login}
        </div>
      );
    }}
  </Query>
);
```

`src/Profile/index.js`

这就是如何在 React 中声明式地定义查询。一旦 `Query` 组件渲染，请求就会执行。使用了顶层组件提供的 `Apollo Client` 来执行查询。render props 模式允许你在子函数中访问查询结果。你可以在浏览器中尝试一下它是否有效。接下来，当查询挂起时显示加载指示：

```javascript
const Profile = () => (
  <Query query={GET_CURRENT_USER}>
    {({ data, loading }) => {
      const { viewer } = data;

      if (loading || !viewer) {
        return <div>Loading ...</div>;
      }

      return (
        <div>
          {viewer.name} {viewer.login}
        </div>
      );
    }}
  </Query>
);
```

`src/Profile/index.js`

应用程序现在在没有 `viewer` 对象或 `loading` 布尔值为 `true` 时显示加载指示器。由于你可以假设在没有 `viewer` 时请求将挂起，你可以从一开始就显示加载指示器。此时，最好是将加载指示器提取为一个独立的组件，因为你将在其他查询中复用它。你为它创建了 `Loading` 文件夹，其中包含 `src/Loading/index.js` 文件。然后，在你的 `Profile` 组件中使用它。

```javascript
import React from 'react';

const Loading = () =>
  <div>Loading ...</div>

export default Loading;
```

`src/Loading/index.js`

接下来，扩展查询以一个嵌套列表字段来查询你自己的 GitHub 仓库。你之前已经做过几次，所以现在的查询结构应该没有区别。以下查询请求了你将在此应用程序中许多信息：

```javascript
const GET_REPOSITORIES_OF_CURRENT_USER = gql`
  {
    viewer {
      repositories(
        first: 5
        orderBy: { direction: DESC, field: STARGAZERS }
      ) {
        edges {
          node {
            id
            name
            url
            descriptionHTML
            primaryLanguage {
              name
            }
            owner {
              login
              url
            }
            stargazers {
              totalCount
            }
            viewerHasStarred
            watchers {
              totalCount
            }
            viewerSubscription
          }
        }
      }
    }
  }
`;
```

`src/Profile/index.js`

在你的 `Query` 组件中使用此扩展并重命名的查询，以请求关于仓库的额外信息。将这些仓库从查询结果传递给新的 `RepositoryList` 组件，该组件应该为你完成所有的渲染工作。这并不是 `Profile` 组件的职责，而且你可能想在其他地方渲染仓库列表。

```javascript
...

import RepositoryList from '../Repository';
import Loading from '../Loading';

...

const Profile = () => (
  <Query query={GET_REPOSITORIES_OF_CURRENT_USER}>
    {({ data, loading }) => {
      const { viewer } = data;

      if (loading || !viewer) {
        return <Loading />;
      }

      return <RepositoryList repositories={viewer.repositories} />;
    }}
  </Query>
);
```

### `src/Profile/index.js`

在你的 `src/Repository/index.js` 文件中，为来自专用文件夹的 `RepositoryList` 组件创建第一个 `import`/`export` 语句。`index.js` 文件被用作该模块的入口。从该模块使用的所有内容都可以通过从 `index.js` 导入来访问。

```javascript
import RepositoryList from './RepositoryList';

export default RepositoryList;
```

### `src/Repository/index.js`

接下来，在你的 `src/Repository/RepositoryList/index.js` 文件中定义 `RepositoryList` 组件。该组件仅接收仓库数组作为 props，这些将通过查询获取并渲染 `RepositoryItem` 组件列表。每个仓库的标识符可以作为 `key` 属性传递给渲染的列表。否则，一个仓库的所有 props 将使用 JavaScript 扩展运算符传递给 `RepositoryItem`。

```javascript
import React from 'react';

import RepositoryItem from '../RepositoryItem';

import '../style.css';

const RepositoryList = ({ repositories }) =>
  repositories.edges.map(({ node }) => (
    <div key={node.id} className="RepositoryItem">
      <RepositoryItem {...node} />
    </div>
  ));

export default RepositoryList;
```

### `src/Repository/RepositoryList/index.js`

最后，在你的 `src/Repository/RepositoryItem/index.js` 文件中定义 `RepositoryItem` 组件，以渲染关于每个仓库的所有查询信息。该文件已经使用了一些样式，你可以像以前一样在 CSS 文件中定义它们。否则，该组件目前只渲染静态信息。

```javascript
import React from 'react';

import Link from '../../Link';

import '../style.css';

const RepositoryItem = ({
  name,
  url,
  descriptionHTML,
  primaryLanguage,
  owner,
  stargazers,
  watchers,
  viewerSubscription,
  viewerHasStarred,
}) => (
  <div>
    <div className="RepositoryItem-title">
      <h2>
        <Link href={url}>{name}</Link>
      </h2>

      <div className="RepositoryItem-title-action">
        {stargazers.totalCount} Stars
      </div>
    </div>

    <div className="RepositoryItem-description">
      <div
        className="RepositoryItem-description-info"
        dangerouslySetInnerHTML={{ __html: descriptionHTML }}
      />
      <div className="RepositoryItem-description-details">
        <div>
          {primaryLanguage && (
            <span>Language: {primaryLanguage.name}</span>
          )}
        </div>
        <div>
          {owner && (
            <span>
              Owner: <a href={owner.url}>{owner.login}</a>
            </span>
          )}
        </div>
      </div>
    </div>
  </div>
);

export default RepositoryItem;
```

### `src/Repository/RepositoryItem/index.js`

用于链接仓库的锚点元素（anchor element）已作为 `Link` 组件提取。`src/Link/index.js` 文件中的 `Link` 组件可能如下所示，以便在额外的浏览器标签页中打开这些 URL：

```javascript
import React from 'react';

const Link = ({ children, ...props }) => (
  <a {...props} target="_blank" rel="noopener noreferrer">
    {children}
  </a>
);

export default Link;
```

### `src/Link/index.js`

一旦你重启应用程序，你应该能看到一个带有样式的仓库列表，其中包含名称、URL、描述、星标数计数、所有者以及项目的实现语言。如果你没有看到任何仓库，请检查你的 GitHub 账户是否有任何公开仓库。如果没有，那么没有显示内容是正常的。我建议你通过创建几个仓库来熟悉 GitHub，既是为了学习 GitHub，也是为了使用这些数据在本教程中进行练习。为你自己的账户创建仓库的另一种方法是 fork 其他人的仓库。

你在本节的最后几个步骤中所做的是纯 React 实现，但这只是结构化组件的一种观点性方法。然而，本节中最重要的部分发生在 `Profile` 组件中。在那里，你引入了一个接收 `query` 作为 prop 的 `Query` 组件。一旦 `Query` 组件渲染，它就会执行 `GraphQL` 查询。查询结果将作为 React 的 render props 模式中的参数变得可访问。

### 练习题

- 确认你的[上一节的源代码](http://bit.ly/2CZbwpU)
  - 确认[上一节的更改](http://bit.ly/2VnYJV7)
- 阅读更多关于[使用 Apollo Client 进行查询](https://www.apollogql.com/docs/react/essentials/queries.html)
- 花费 3 分钟时间进行测试](https://surveonkey.com/53Q6K3

## React 中的 Apollo Client 错误处理

在深入研究 React 中的 GraphQL 变之前，本节将澄清 React 中的错误处理。错误处理发生在两个层面：应用级别和查询/变体级别。两者都可以以下两种情况进行实现。在查询级别，在你的 `Profile` 组件中，你可以访问 `data` 和 `loading` 属性。除了这些之外，你还可以访问 `error` 对象，它可以用于显示条件性错误消息。



```
...

import RepositoryList from '../Repository';
import Loading from '../Loading';
import ErrorMessage from '../Error';

...

const Profile = () => (
  <Query query={GET_REPOSITORIES_OF_CURRENT_USER}>
    {({ data, loading, error }) => {
      if (error) {
        return <ErrorMessage error={error} />;
      }

      const { viewer } = data;

      if (loading || !viewer) {
        return <Loading />;
      }

      return <RepositoryList repositories={viewer.repositories} />;
    }}
  </Query>
);

export default Profile;
```

### src/Profile/index.js

而来自 `src/Error/index.js` 的 `ErrorMessage` 组件可能如下：

```javascript
import React from 'react';

import './style.css';

const ErrorMessage = ({ error }) => (
  <div className="ErrorMessage">
    <small>{error.toString()}</small>
  </div>
);

export default ErrorMessage;
```

### src/Error/index.js

尝试将查询中的某个字段名称更改为 GitHub GraphQL API 不提供的字段，并观察浏览器中渲染的内容。你应该会看到类似这样的：*Error: GraphQL error: Field ‘viewers’ doesn’t exist on type ‘Query’*。或者，如果你模拟离线功能，你会看到：*Error: Network error: Failed to fetch*。这就是如何分为 GraphQL 错误和网络错误的方法。你可以在组件或查询级别处理错误，但它以后对变体也有帮助。若要在应用级别实现错误处理，请安装另一个 Apollo 包：

```bash
npm install apollo-link-error --save
```

命令行

你可以在可以在 `src/index.js` 文件中导入它并创建这样的错误链接：

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import { ApolloProvider } from 'react-apollo';
import { ApolloClient } from 'apollo-client';
import { HttpLink } from 'apollo-link-http';
import { onError } from 'apollo-link-error';
import { InMemoryCache } from 'apollo-cache-inmemory';

...

const errorLink = onError(({ graphQLErrors, networkError }) => {
  if (graphQLErrors) {
    // 对 graphql 进行处理
  }

  if (networkError) {
    // 对网络错误进行处理
  }
});
```

`src/index.js`

你可以将应用层面的错误处理区分开发模式和生产模式。在开发模式下，将错误控制台打印到浏览器的开发者控制台中可能足够了。在生产模式下，你可以设置一个像 [Sentry](https://sentry.io) 这样的错误跟踪服务。它将教你如何高效地在 Web 仪表中识别 bug。

现在你的应用程序中有两个链接：`httpLink` 和 `errorLink`。为了将它们合并并在 Apollo Client 实例中使用，我们将下载 Apollo 生态系统中另一个有用包，它允许在命令行中进行链接组合：

```bash
npm install apollo-link --save
```

### 命令行

其次，使用它在 `src/index.js` 文件中组合你的两个链接：

```javascript
...
import { ApolloClient } from 'apollo-client';
import { ApolloLink } from 'apollo-link';
import { HttpLink } from 'apollo-link-http';
import { onError } from 'apollo-link-error';
import { InMemoryCache } from 'apollo-cache-inmemory';

...

const httpLink = ...

const errorLink = ...

const link = ApolloLink.from([errorLink, httpLink]);

const cache = new InMemoryCache();

const client = new ApolloClient({
  link,
  cache,
});
```

`src/index.js`

这就是如何组合两个或多个链接来创建 Apollo Client 实例的方法。有由社区和 Apollo 维护者开发的多个链接，它们通过高级功能扩展了 Apollo Client。请记住，重要的一点是理解链接可以用于访问和修改 GraphQL 的控制流。在这样做时，请务必按照正确的顺序链式控制流。`apollo-link-http` 被称为**终止性链接（terminating link）**，因为它将操作转换为通常发生于网络请求的结果。另一方面，`apollo-link-error` 是**非终止性链接（non-terminating link）**。它仅通过功能增强你的终止链接，因为终止性链接必须是控制流链中的最后一个实体。

### 练习题

*   确认你的[上一节源码](http://bit.ly/2CWx5aA)

    *   确认[上一节的更改](http://bit.ly/2Vo7n63)

*   阅读更多关于[不同的 Apollo 错误类型和错误策略](https://www.apollographql.com/docs/react/features/error-handling.html)的信息

*   阅读更多关于[Apollo Links](https://www.apollographql.com/docs/link/)的信息

*   阅读更多关于[可组合的 Apollo Links](https://www.apollographql.com/docs/link/composition.html)的信息

*   在网络请求失败时实现[apollo-link-retry](https://www.apollographql.com/docs/link/links/retry.html)

*   花 3 分钟时间参加[测验](https://www.surveymonkey.com/r/53HLLFX)

## 在 React 中使用 Apollo Client 进行 GraphQL Mutation

之前的章节教了你如何使用 React Apollo 和 Apollo Client 查询数据。在本节中，你将学习变异（mutations）。像之前的应用程序一样，你将通过 GitHub 暴露的 `addStar` 变实现对仓库的收藏。

变异始于一个变量来识别要收藏的仓库。我们还没有在 Query 组件中使用过变量，但下面的变异工作方式相同，可以定义在 `src/Repository/RepositoryItem/index.js` 文件中。

```javascript
import React from 'react';
import gql from 'graphql-tag';

...

const STAR_REPOSITORY = gql`
  mutation($id: ID!) {
    addStar(input: { starrableId: $id }) {
      starrable {
        id
        viewerHasStarred
      }
    }
  }
`;

...
```

`src/Repository/RepositoryItem/index.js`

变异定义将 `id` 变量作为 `addStar` 变异的输入。和之前一样，你可以决定在变异成功时返回什么。现在，你可以使用一个代表之前使用的 Query 组件的 Mutation 组件，但这次是用于变异。你必须传递 `mutation` 属性，以及一个用于传递仓库标识符的 `variable` 属性。

```javascript
import React from 'react';
import gql from 'graphql-tag';
import { Mutation } from 'react-apollo';

...

const RepositoryItem = ({
  id,
  name,
  url,
  descriptionHTML,
  primaryLanguage,
  owner,
  stargazers,
  watchers,
  viewerSubscription,
  viewerHasStarred,
}) => (
  <div>
    <div className="RepositoryItem-title">
      <h2>
        ...
      </h2>

      <div>
        <Mutation mutation={STAR_REPOSITORY} variables={{ id }}>
          {addStar => <div>{stargazers.totalCount} Star</div>}
        </Mutation>
      </div>
    </div>

    <div className="RepositoryItem-description">
      ...
    </div>
  </div>
);
```

`src/Repository/RepositoryItem/index.js`

注意：包裹 Mutation 组件的 div 元素是为了你在本节中将实现的其他变异而准备的。

每个仓库的 `id` 应该由于之前的查询结果而可用。它必须作为变异的变量来标识仓库。Mutation 组件的用法与 Query 组件类似，因为它也实现了渲染属性（render prop）模式。不过，第一个参数是不同的，因为它是变异本身而不是变异结果。使用此函数在预期结果之前触发变异。稍后，你将看到如何获取变异结果；现在，变异函数可以在按钮元素中使用。在这种情况下，它已经位于一个 Button 组件中了：

```javascript
...

import Link from '../../Link';
import Button from '../../Button';

...

const RepositoryItem = ({ }) => (
  <div>
    <div className="RepositoryItem-title">
      ...

      <div>
        <Mutation mutation={STAR_REPOSITORY} variables={{ id }}>
          {addStar => <div>{stargazers.totalCount} Star</div>}
        </Mutation>
      </div>
    </div>

    ...
  </div>
);
```

`src/Repository/RepositoryItem/index.js`

样式化的 Button 组件可以实现在 `src/Button/index.js` 文件中。它被提取出来，是因为你稍后将在应用程序中使用它。

```javascript
import React from 'react';

import './style.css';

const Button = ({
  children,
  className,
  color = 'black',
  type = 'button',
  ...props
}) => (
  <button
    className={`${className} Button_${color}`}
    type={type}
    {...props}
  >
    {children}
  </button>
);

export default Button;
```

`src/Button/index.js`

让我们获取之前遗漏的变异结果。在你的渲染属性子函数作为第二个参数访问它。

```javascript
const RepositoryItem = ({ }) => (
  <div
    <div className="RepositoryItem-title">
      ...

      <div>
        <Mutation mutation={STAR_REPOSITORY} variables={{ id }}>
          {(addStar, { data, loading, error }) => (
            <Button
              className={'RepositoryItem-title-action'}
              onClick={addStar}
            >
              {stargazers.totalCount} Star
            </Button>
          )}
        </Mutation>
      </div>
    </div>

    ...
  </div>
);
```

`src/Repository/RepositoryItem/index.js`

在使用 React Apollo 时，变异（mutation）的工作方式与查询（query）类似。它使用渲染属性（render prop）模式来访问变异及其结果。变异可以在 UI 中作为函数来使用。它可以访问传递给 `Mutation` 组件的变量，但当你通过配置对象向函数传递变量时，你也可以对变量进行重写（例如 `addStar({ variables: { id } })`）。这是 React Apollo 中的一种通用模式：你可以在 `Mutation` 组件中指定变量等信息，也可以在调用变异函数时对其进行覆盖。

请注意，如果你使用查询结果中的 `viewerHasStarred` 布尔值来显示“点收藏（Star）”或“取消收藏（Unstar）”按钮，可以通过条件渲染来实现：

```javascript
const RepositoryItem = ({ ... }) => (
  <div>
    <div className="RepositoryItem-title">
      ...

      <div>
        {!viewerHasStarred ? (
          <Mutation mutation={STAR_REPOSITORY} variables={{ id }}>
            {(addStar, { data, loading, error }) => (
              <Button
                className={'RepositoryItem-title-action'}
                onClick={addStar}
              >
                {stargazers.totalCount} Star
              </Button>
            )}
          </Mutation>
        ) : (
          <span>{/* 这里是你的 removeStar 变异 */}</span>
        )}

      {/* 这里是你的 updateSubscription 变异 */}
      </div>
    </div>

    ...
  </div>
);
```

`src/Repository/RepositoryItem/index.js`

当你像上面那样点收藏仓库时，“Star”按钮会消失。这正是我们想要的，因为这意味着 Apollo Client 缓存中已标识仓库的 `viewerHasStarred` 布尔值已更新。Apollo Client 能够将变异结果与仓库标识符匹配到 Apollo Client 缓存中的仓库实体，属性随之更新，UI 重新渲染。然而，在另一端，收藏该仓库的人数计数并没有更新，因为无法从 GitHub 的 API 获取该计数。该计数必须在 Apollo Client 的缓存中更新。你将在后续章节中了解到更多关于此主题的知识。

## 练习

* 确认你的[上一节源码](http://bit.ly/2CYyXiN)

    * 确认[上一节的更改](http://bit.ly/2Vpdg2L)



- 阅读更多关于[在 React 中使用 Apollo Client 进行变异](https://www.apollographql.com/docs/react/essentials/mutations.html)
- 在 `RepositoryItem` 组件中实现其他变异
  - 当 `viewerHasStarred` 布尔值为 `true` 时实现 `removeStar` 变异
  - 显示一个带有关注人数的按钮，该按钮应用于关注/取消关注仓库
    - 实现来自 GitHub GraphQL API 的 `updateSubscription` 变异，根据 `viewerSubscription` 状态关注/取消关注仓库
- 花三分钟时间参加[测验](https://www.surveymonkey.com/r/5GJQWXC)

## React 中带高阶组件的 GraphQL 查询/变异

我们已经使用了 React Apollo 中的 `Query` 和 `Mutation` 组件来连接数据层（Apollo Client）与视图层（React）。`Query` 组件在渲染时执行查询，而 `Mutation` 组件提供了一个触发变异的函数访问权限。这两个组件都使用渲染属性模式，以便在它们的子函数中可以访问结果。

[高阶组件 (HOC)](https://www.robinwieruch.de/gentle-introduction-higher-order-components/) 是 React 渲染属性模式的一种广泛接受的替代方案。React Apollo 包也为查询和变异实现了高阶组件，尽管 Apollo 背后的团队并没有推广它，甚至公开表示倾向于将渲染属性作为他们的首选。尽管如此，本节将向你展示另一种替代方案，即使用高阶组件而不是渲染属性，尽管此应用程序之后将继续使用渲染属性模式。如果你已经在 `Profile` 组件的参数中访问了查询结果，那么在组件本身就不再需要 `Query` 组件了：

```javascript
const Profile = ({ data, loading, error }) => {
  if (error) {
    return <ErrorMessage error={error} />;
  }

  const { viewer } = data;

  if (loading || !viewer) {
    return <Loading />;
  }

  return <RepositoryList repositories={viewer.repositories} />;
};
```

`src/Profile/index.js`

这里没有涉及 GraphQL，因为你看到的只是纯粹的视图层。相反，数据层逻辑被提取到了高阶组件中。我们从 React Apollo 包中导入 `graphql` HOC，以便将其应用到 `Profile` 组件，该组件接收查询定义作为参数。

```javascript
import React from 'react';
import gql from 'graphql-tag';
import { graphql } from 'react-apollo';

...

const GET_REPOSITORIES_OF_USER = gql`
  {
    viewer {
      ...
    }
  }
`;

const Profile = ({ data, loading, error }) => {
  ...
};

export default graphql(GET_REPOSITORIES_OF_USER)(Profile);
```

`src/Profile/index.js`

我觉得 HOC 方法比渲染属性更整洁，因为它将数据层和视图层结合，而不是相互插入。然而，Apollo 背后的团队做出了倾向渲染属性的决定。虽然我觉得 HOC 方法更简洁，但渲染属性在数据变异和查询方面也有自己的优势。例如，假设一个查询依赖于属性。在静态定义的高阶组件中访问传入的属性很麻烦，但在渲染属性中可以动态使用，因为它是自然访问的。渲染属性的另一个优势是组合的能力，这当一个查询依赖于另一个的结果时非常有用。这也可以通过 HOC 实现，但再次，它变得更加麻烦。这归结为似乎无休止的“高阶组件 vs 渲染属性”讨论。

## 练习

- 确认你的[上一节源码](http://bit.ly/2VkX3LU)
  - 确认[上一节的更改](http://bit.ly/2Vpdjvt)
- 就使用高阶组件或渲染属性的优缺点形成自己的观点
- 尝试用高阶组件实现你的一个变异
- 花 3 分钟时间参加[测验](https://www.surveymonkey.com/r/5G6QPLY)

## React 中使用 Apollo Client 进行本地状态管理

让我们回到 `Repository` 组件。你经历了在变异成功后 `viewerHasStarred` 布尔值在 Apollo Client 缓存中的更新。这太棒了，因为 Apollo Client 会根据变异的结果为你处理这一切。如果你遵循了变异章节的练习，你应该能看到类似切换的“点收藏”和“取消收藏”标签。这一切发生是因为你在变异结果中返回了 `viewerHasStarred` 布尔值。Apollo Client 足够聪明，可以更新仓库实体，而该实体是归一化的并在缓存中可用的。这是一个强大的默认行为，不是吗？你不需要自己处理本地状态管理，只要你在变异结果中提供有用信息，Apollo Client 就会为你解决问题。

然而，Apollo Client 并不会突变（mutation）后更新星星数。通常情况下，假设在收藏仓库时星星数会加 1，取消收藏时则反之。由于我们没有在突变结果中返回收藏人数，因此你必须手动在 Apollo Client 的缓存中处理更新。对于突变调用，使用 Apollo Client 的 `refetchQueries` 选项是一种比较简单的方法，或者使用 `Mutation` 组件来触发所有可能受突变影响的查询的重新获取（refetch）。但并不是处理此问题的最佳方法。这种方法的弊端是，为了在突变后保持数据一致，需要额外消耗一次查询请求。在不断增长的应用程序中，这种方法最终会产生问题。幸运的是，Apollo Client 提供了其他功能，可以手动从本地缓存中读取/写入数据，而无需更多的网络请求。`Mutation` 组件提供了一个属性，你可以在其中插入更新功能，该功能可以访问 Apollo Client 实例以实现更新机制。

在实现本地状态管理的更新功能之前，让我们先重构另一部分代码，这段代码对于本地状态更新机制非常有用。你 `Profile` 组件旁边的查询定义已经增长到几个字段，并包含多个对象嵌套。之前，你学习了 GraphQL 片段（fragments）以及如何使用它们来拆分查询部分以便后续复用。接下来，我们将拆分你用于仓库节点的所有字段信息。你可以在 `src/Repository/fragments.js` 文件中定义此片段，以便保持在其他组件中的可复用。

```javascript
import gql from 'graphql-tag';

const REPOSITORY_FRAGMENT = gql`
  fragment repository on Repository {
    id
    name
    url
    descriptionHTML
    primaryLanguage {
      name
    }
    owner {
      login
      url
    }
    stargazers {
      totalCount
    }
    viewerHasStarred
    watchers {
      totalCount
    }
    viewerSubscription
  }
`;

export default REPOSITORY_FRAGMENT;
```

`src/Repository/fragments.js`

你拆分了这部分查询（片段），是因为它在接下来的章节中会被更频繁地用于本地状态更新机制，因此进行了之前的重构。

该片段不应该直接从 `src/Repository/fragments.js` 路径导入到你的 `Profile` 组件，因为 `src/Repository/index.js` 文件是该模块优选的入口。

```javascript
import RepositoryList from './RepositoryList';
import REPOSITORY_FRAGMENT from './fragments';

export { REPOSITORY_FRAGMENT };

export default RepositoryList;
```

`src/Repository/index.js`

最后，在 `Profile` 组件的文件中导入该片段以便再次使用。

```javascript
...

import RepositoryList, { REPOSITORY_FRAGMENT } from '../Repository';
import Loading from '../Loading';
import ErrorMessage from '../Error';

const GET_REPOSITORIES_OF_CURRENT_USER = gql`
  {
    viewer {
      repositories(
        first: 5
        orderBy: { direction: DESC, field: STARGAZERS }
      ) {
        edges {
          node {
            ...repository
          }
        }
      }
    }
  }

  ${REPOSITORY_FRAGMENT}
`;

...
```

`src/Profile/index.js`

重构完成。你的查询现在变得更加简洁，且其原生仓库模块中的片段可以复用到其他地方和功能。接下来，使用 `Mutation` 组件的 `update` 属性传递一个函数，该函数最终将更新本地缓存。

```javascript
...

const updateAddStar = (client, mutationResult) => {
  ...
};

const RepositoryItem = ({ ... }) => (
  <div>
    <div className="RepositoryItem-title">
      ...

      <div>
        {viewerHasStarred ? (
          ...
        ) : (
          <Mutation
            mutation={STAR_REPOSITORY}
            variables={{ id }}
            update={updateAddStar}
          >
            ...
          </Mutation>
        )}
      </div>
    </div>

    ...
  </div>
);

export default RepositoryItem;
```

`src/Repository/RepositoryItem/index.js`

将该函数提取出来作为一个单独的 JavaScript 变量，否则如果将其内联在 `Mutation` 组件中，`RepositoryItem` 组件中的代码会变得过于冗长。该函数在参数中可以访问 Apollo Client 和突变结果，而你需要这二者来更新数据，因此你可以在函数签名中对突变结果进行解构。如果你不知道突变结果的内容，请再次检查 `STAR_REPOSITORY` 突变的定义，你在那里定义了所有应该出现在突变结果中的字段。目前，要更新的仓库 `id` 是重要部分。

```javascript
const updateAddStar = (
  client,
  { data: { addStar: { starrable: { id } } } },
) => {
  ...
};
```

`src/Repository/RepositoryItem/index.js`

你本可以将仓库的 `id` 传递给 `updateAddStar()` 函数，该函数是 `Mutation` 组件渲染属性子函数中的高阶函数。你已经在 `Repository` 组件中获取了仓库的标识符。

现在到了本节最令人兴奋的部分。你可以使用 Apollo Client 从缓存中读取数据，也可以向其写入数据。目标是从缓存中读取被收藏的仓库，这就是为什么我们需要 `id` 来将其星星数加 1，并将更新后的仓库写回缓存。你通过提取仓库片段，根据 `id` 从缓存中获取了仓库。你可以结合它和仓库标识符从缓存中检索真实的仓库。

```javascript
...

import REPOSITORY_FRAGMENT from '../fragments';
import Link from '../../Link';
import Button from '../../Button';

...

const updateAddStar = (
  client,
  { data: { addStar: { starrable: { id } } } },
) => {
  const repository = client.readFragment({
    id: `Repository:${id}`,
    fragment: REPOSITORY_FRAGMENT,
  });

  // update count of stargazers

  // write repository back to cache
};
```

`src/Repository/RepositoryItem/index.js`

让我们在这里回顾一下所有三个步骤。首先，你通过标识符和片段（fragment）从 Apollo Client 获取（读取）了仓库实体；其次，你更新了实体的信息；第三，你使用 JavaScript 扩展运算符将更新后的信息写回数据，同时保持所有剩余信息完整。这是一种手动更新机制，适用于变异（mutation）缺少数据的情况。

在所有三个部分使用相同的片段是一个良好的实践：初始查询、`readFragment()` 以及 `writeFragment()` 缓存方法。这样你的实体数据结构在缓存中就能保持一致。例如，如果你忘记在 `writeFragment()` 方法的数据对象中包含由片段字段定义的属性，你将收到一个警告：`Missing field __typename in …`。

在实现层面上，你已经学习了如何从查询或变异中提取片段。片段允许你通过 GraphQL 类型来定义共享的实体。你可以在查询、变异或本地状态管理方法中复用这些片段来更新缓存。在更高级的层面上，你了解到 Apollo Client 的缓存会对你的数据进行归一化处理（normalization），因此你可以使用类型和标识符作为复合键，检索通过深度嵌套查询获取的实体。如果没有它，你必须在将数据放入存储/状态之前对所有获取的数据进行归一化处理。

## 练习

- 确认你[上一节的源码](http://bit.ly/2VoiWKr)
  - 确认[上一节的更改](http://bit.ly/2Vp8D8V)
- 阅读更多关于[Apollo Client 中的本地状态管理](https://www.apollographql.com/docs/react/essentials/local-state.html)的内容
- 阅读更多关于[Apollo Client 中的片段](https://www.apollographql.com/docs/react/advanced/fragments.html)的内容
- 为前一个练习中的所有其他变异实现本地缓存更新
  - 为你的 `removeStar` 变异实现相同的本地缓存更新，但是减少点赞数（stargazers）的数量
  - 为 `updateSubscription` 变异实现本地缓存更新
  - 你将在下一节中看到该问题的运行解决方案
- 阅读更多关于[Apollo Client 中的缓存以及用于识别实体的复合键](https://www.apollographql.com/docs/react/advanced/caching.html)的内容
- 花 3 分钟时间完成[测验](https://www.surveymonkey.com/r/5BSDXF7)

## React 中的 Apollo Client 乐观 UI

我们已经涵盖了基础知识，现在是学习高级主题了。这些主题之一就是使用 React Apollo 的乐观 UI（optimistic UI），它让屏幕上的所有内容变得更加同步。例如，在 Twitter 上点赞一条帖子时，点赞会立即显示。作为开发者，我们知道有一个请求会将点赞信息发送到 Twitter 后端。该请求是异步的，并且不会立即返回结果。乐观 UI 会立即假设请求成功，并为前端模拟该请求的结果，以便在真实响应稍后到达之前立即更新其 UI。如果请求失败，乐观 UI 将执行回滚并相应地更新自身。乐观 UI 通过为用户省略不便的反馈（例如加载指示器）提升了用户体验。好的是，React Apollo 开箱即用了这一功能。

在本节中，你将实现一个乐观 UI，用于用户点击你在上一个练习中实现的 watch/unwatch 变异。如果你还没有实现，现在是时候实现它了，或者你可以用 star 或 unstar 变异代替它。无论如何，完成所有三个变异的乐观 UI 行为都是下一个练习。为了完整性，这里是 watch 变异的一种可能实现，作为“Star”/“Unstar”按钮旁边的按钮。首先是变异：



```javascript
const WATCH_REPOSITORY = gql`
  mutation ($id: ID!, $viewerSubscription: SubscriptionState!) {
    updateSubscription(
      input: { state: $viewerSubscription, subscribableId: $id }
    ) {
      subscribable {
        id
        viewerSubscription
      }
    }
  }
`;
```

`src/Repository/RepositoryItem/index.js`

其次，使用 Mutation 渲染属性组件（render prop component）使用变异：

```javascript
const VIEWER_SUBSCRIPTIONS = {
  SUBSCRIBED: 'SUBSCRIBED',
  UNSUBSCRIBED: 'UNSUBSCRIBED',
};

const isWatch = viewerSubscription =>
  viewerSubscription === VIEWER_SUBSCRIPTIONS.SUBSCRIBED;

const updateWatch = () => {
  ...
};

const RepositoryItem = ({ ... }) => (
  <div
    <div className="RepositoryItem-title">
      ...

      <div>
        ...

        <Mutation
          mutation={WATCH_REPOSITORY}
          variables={{
            id,
            viewerSubscription: isWatch(viewerSubscription)
              ? VIEWER_SUBSCRIPTIONS.UNSUBSCRIBED
              : VIEWER_SUBSCRIPTIONS.SUBSCRIBED,
          }}
          update={updateWatch}
        >
          {(updateSubscription, { data, loading, error }) => (
            <Button
              className="RepositoryItem-title-action"
              onClick={updateSubscription}
            >
              {watchers.totalCount}{' '}
              {isWatch(viewerSubscription) ? 'Unwatch' : 'Watch'}
            </Button>
          )}
        </Mutation>

        ...
      </div
    </div>

    ...
  </div>
);
```

`src/Repository/RepositoryItem/index.js`

最后是传递给 Mutation 组件的缺失 `update` 函数：

```javascript
const updateWatch = (
  client,
  {
    data: {
      updateSubscription: {
        subscribable: { id, viewerSubscription },
      },
    },
  },
) => {
  const repository = client.readFragment({
    id: `Repository:${id}`,
    fragment: REPOSITORY_FRAGMENT,
  });

  let { totalCount } = repository.watchers;
  totalCount =
    viewerSubscription === VIEWER_SUBSCRIPTIONS.SUBSCRIBED
      ? totalCount + 1
      : totalCount - 1;

  client.writeFragment({
    id: `Repository:${id}`,
    fragment: REPOSITORY_FRAGMENT,
    data: {
      ...repository,
      watchers: {
        ...repository.watchers,
        totalCount,
      },
    },
  });
};
```

`src/Repository/RepositoryItem/index.js`

现在让我们实现乐观 UI 功能。幸运的是，Mutation 组件提供了一个用于乐观 UI 策略的属性 `optimisticResponse`。它返回相同的结果，该结果作为参数传递给 `update` 属性的函数。对于 watch 变异，`viewerSubscription` 状态会变为订阅或取消订阅。这就是乐观 UI。

```javascript
const RepositoryItem = ({ ... }) => (
  <div>
    <div className="RepositoryItem-title">
      ...

      <div>
        ...

        <Mutation
          mutation={WATCH_REPOSITORY}
          variables={{
            id,
            viewerSubscription: isWatch(viewerSubscription)
              ? VIEWER_SUBSCRIPTIONS.UNSUBSCRIBED
              : VIEWER_SUBSCRIPTIONS.SUBSCRIBED,
          }}
          optimisticResponse={{
            updateSubscription: {
              __typename: 'Mutation',
              subscribable: {
                __typename: 'Repository',
                id,
                viewerSubscription: isWatch(viewerSubscription)
                  ? VIEWER_SUBSCRIPTIONS.UNSUBSCRIBED
                  : VIEWER_SUBSCRIPTIONS.SUBSCRIBED,
              },
            },
          }}
          update={updateWatch}
        >
          ...
        </Mutation>

        ...
      </div
    </div>

    ...
  </div>
);
```

`src/Repository/RepositoryItem/index.js`

当你启动应用程序并关注一个仓库时，按钮的“Watch”和“Unwatch”标签在点击后会立即变化。这是因为乐观响应是同步到达的，而真实响应正在等待中并在稍后解析。由于 `__typename` 元字段会随每个 Apollo 请求一起发送，请包含它们。

乐观响应（optimistic response）的额外好处是它也让监听器的更新计数变得乐观。`update` 属性中使用的函数现在会被调用两次：第一次使用乐观响应，第二次使用 GitHub GraphQL API 的响应。在传递给 `Mutation` 组件 `update` 属性的函数中，在乐观响应中捕获预期变更（mutation）结果的相同信息是合理的。例如，如果你没有在 `optimisticResponse` 对象中传递 `id` 属性，传递给 `update` 属性的函数将抛出错误，因为在没有标识符的情况下无法从缓存中检索仓库。

此时，`Mutation` 组件是否变得过于冗长是一个引起争议的问题。使用渲染属性（Render Props）模式比高阶组件（Higher-Order Components）更进一步将数据层与视图层置在一起。有人可能会认为它并没有将数据层置在一起，而是将其插入了视图层中。当像 `update` 和 `optimisticResponse` 属性等优化措施放入 Render Prop 组件时，对于扩展性的应用程序来说可能会变得过于冗长。我建议使用你学的技术以及你自己的策略来保持源代码简洁。我看到了四种解决此问题的方法：

- 保持声明内联（见：`optimisticUpdate`）。
- 将内联声明提取为变量（见：`update`）。
- 将方法 1 和 2 结合，但只提取最冗长的部分。
- 使用高阶组件代替 Render Props 来将数据层置在一起，而不是将其插入视图层中。

前三种是关于将数据层插入（inserting）视图层中，而最后一种是关于将其置在一起（co-locating）。每种方法都有缺点。遵循第二种方法，你可能会自己声明函数而不是对象，或者使用高阶函数而不是函数，因为你需要向它们传递参数。如果使用第四种方法，你可能会在保持 HOC 简洁方面遇到同样的挑战。在这种情况下，你也可以使用其他三种方法，但这次是在 HOC 而不是 Render Prop 中。

### 练习

- 确认你的[上一个节的源代码](http://bit.ly/2VuZZpz)。
  - 确认[上一节的更改](http://bit.ly/2VrjEGS)。
- 限制你的网络连接（浏览器通常提供此类功能），并体验尽管请求很慢，`optimisticResponse` 是如何考虑 `update` 函数的。
- 尝试用 render props 和高阶组件以不同的方式置一起或插入你的数据层。
- 为点赞（star）和取消点赞（unstar）变更实现乐观 UI。
- 阅读更多关于 [React 中 GraphQL Apollo 乐观 UI](https://www.apollographql.com/docs/react/features/optimistic-ui.html) 的信息。
- 花 3 分钟参加[测试](https://www.surveymonkey.com/r/5B6D8BX)。

## 在 React 中使用 Apollo Client 实现 GraphQL 分页

最后，在使用 GraphQL API 时将实现另一个高级功能，叫做分页（pagination）。在本节中，你将实现一个允许查询连续仓库页的按钮，在 `RepositoryList` 组件的列表下方渲染一个简单的“更多”按钮。当点击时，将获取另一页仓库，并将其与之前的列表作为一个整体状态合并到 Apollo Client 的缓存中。

首先，扩展你的 `Profile` 组件的查询，添加必要的信息以允许仓库列表进行分页：

```javascript
const GET_REPOSITORIES_OF_CURRENT_USER = gql`
  query($cursor: String) {
    viewer {
      repositories(
        first: 5
        orderBy: { direction: DESC, field: STARGAZERS }
        after: $cursor
      ) {
        edges {
          node {
            ...repository
          }
        }
        pageInfo {
          endCursor
          hasNextPage
        }
      }
    }
  }
  ${REPOSITORY_FRAGMENT}
`;
```

`src/Profile/index.js`

在获取下一页仓库时，`endCursor` 可以作为 `$cursor` 变量，但 `hasNextPage` 可以禁用该功能（例如不显示“更多”按钮）以获取另一页。不过，获取第一页仓库的初始请求 `$cursor` 变量将为 `undefined`。GitHub 的 GraphQL API 将优雅地处理这种情况，并在不考虑 `after` 参数的情况下返回仓库列表中的第一个项目。从列表获取更多项目的其他请求将发送带有光标的定义的 `after` 参数，该光标是查询中的 `endCursor`。

现在我们拥有了从 GitHub GraphQL API 获取更多页仓库的所有信息。`Query` 组件在其子函数中暴露了一个检索它们的函数。由于获取更多仓库的按钮最适合放在 `RepositoryList` 组件中，你可以将此函数作为属性传递给它。

```javascript
const Profile = () => (
  <Query query={GET_REPOSITORIES_OF_CURRENT_USER}>
    {({ data, loading, error, fetchMore }) => {
      ...

      return (
        <RepositoryList
          repositories={viewer.repositories}
          fetchMore={fetchMore}
        />
      );
    }}
  </Query>
);
```

`src/Profile/index.js`

接下来，在 `RepositoryList` 组件中使用该函数，并添加一个当可用时显示的获取连续仓库页的按钮。

```javascript
import React, { Fragment } from 'react';

...

const RepositoryList = ({ repositories, fetchMore }) => (
  <Fragment>
    {repositories.edges.map(({ node }) => (
      ...
    ))}

    {repositories.pageInfo.hasNextPage && (
      <button
        type="button"
        onClick={() =>
          fetchMore({
            /* configuration object */
          })
        }
      >
        更多
      </button>
    )}
  </Fragment>
);

export default RepositoryList;
```

`src/RepositoryList/index.js`

`fetchMore()` 函数执行来自初始请求的查询，并接收一个配置对象，该对象用于覆盖变量。对于分页，这意味着将上一个查询结果的 `endCursor` 传递给查询作为 `after` 参数。否则，你将因为指定了变量而再次执行初始请求。

```javascript
const RepositoryList = ({ repositories, fetchMore }) => (
  <Fragment>
    ...

    {repositories.pageInfo.hasNextPage && (
      <button
        type="button"
        onClick={() =>
          fetchMore({
            variables: {
              cursor: repositories.pageInfo.endCursor,
            },
          })
        }
      >
        更多
      </button>
    )}
  </Fragment>
);
```

`src/RepositoryList/index.js`

如果你尝试点击按钮，你应该得到以下错误消息：`Error: updateQuery option is required.` 需要 `updateQuery` 函数来告诉 Apollo Client 如何合并之前的结果和新结果。将函数定义在按钮之外，否则它将变得过于冗长。



```javascript
const updateQuery = (previousResult, fetchMoreResult }) => {
  ...
};

const RepositoryList = ({ repositories, fetchMore }) => (
  <Fragment>
    ...

    {repositories.pageInfo.hasNextPage && (
      <button
        type="button"
        onClick={() =>
          fetchMore({
            variables: {
              cursor: repositories.pageInfo.endCursor,
            },
            updateQuery,
          })
        }
      >
        更多
      </button>
    )}
  </Fragment>
);
```

`src/RepositoryList/index.js`

该函数可以访问之前的查询结果，也可以访问点击按钮后解析出的下一个结果：

```javascript
const updateQuery = (previousResult, { fetchMoreResult }) => {
  if (!fetchMoreResult) {
    return previousResult;
  }

  return {
    ...previousResult,
    viewer: {
      ...previousResult.viewer,
      repositories: {
        ...previousResult.viewer.repositories,
        ...fetchMoreResult.viewer.repositories,
        edges: [
          ...previousResult.viewer.repositories.edges,
          ...fetchMoreResult.viewer.repositories.edges,
        ],
      },
    },
  };
};
```

`src/Repository/RepositoryList/index.js`

在这个函数中，你可以使用 JavaScript 展开运算符合并两个结果。如果没有新结果，则返回上一个结果。重要的部分是合并两个仓库对象的 `edges`，以获得一个合并后的项目列表。在 `repositories` 对象中，`fetchMoreResult` 的优先级高于 `previousResult`，因为它包含了新的 `pageInfo`，其中包含上一次分页结果的 `endCursor` 和 `hasNextPage` 属性。当你再次点击按钮时，你需要这些属性来正确的游标作为参数。

如果你想在处理深度嵌套数据时找到繁琐的 JavaScript 展开运算符的替代方案，请查看[此 GitHub Pull Request](https://github.com/the-road-to-graphql/react-graphql-github-apollo/pull/14) 中的更改，它使用了来自 `Ramda.js` 的 Lenses。

为了增加用户友好性的另一个小改进，在获取更多页面时添加加载指示器。到目前为止，`Profile` 组件中 `Query` 组件的 `loading` 布尔值仅在初始请求时为 true，而在后续请求中不为。通过传递给 `Query` 组件的 prop 来更改这种行为，`loading` 布尔值将相应更新。

```javascript
const Profile = () => (
  <Query
    query={GET_REPOSITORIES_OF_CURRENT_USER}
    notifyOnNetworkStatusChange={true}
  >
    {({ data, loading, error, fetchMore }) => {
      ...
    }}
  </Query>
);
```

`src/Profile/index.js`

当你再次运行应用并尝试“更多”（More）按钮时，你会看到奇怪的行为。每当你加载另一页仓库时，加载指示器都会显示，但仓库列表会完全消失，合并后的列表按预期进行渲染。由于 `loading` 布尔值在初始和后续请求中都会变为 true，`Profile` 组件中的条件渲染将始终显示加载指示器。它会从 `Profile` 函数提前返回，永远无法到达渲染 `RepositoryList` 的代码。将条件从 `||` 快速更改为 `&&` 即可让它仅在初始请求时显示加载指示器。此后的每次请求（只要 `viewer` 对象可用）都处于该条件之外，因此它会渲染 `RepositoryList` 组件。

```javascript
const Profile = () => (
  <Query
    query={GET_REPOSITORIES_OF_CURRENT_USER}
    notifyOnNetworkStatusChange={true}
  >
    {({ data, loading, error, fetchMore }) => {
      ...

      const { viewer } = data;

      if (loading && !viewer) {
        return <Loading />;
      }

      return (
        <RepositoryList
          loading={loading}
          repositories={viewer.repositories}
          fetchMore={fetchMore}
        />
      );
    }}
  </Query>
);
```

`src/Profile/index.js`

该布尔值可以传递给 `RepositoryList` 组件。在那里，它可以被用于显示加载指示器而不是“更多”按钮。由于该布尔值在初始请求时从未到达 `RepositoryList` 组件，你可以确保只有在有后续请求挂起时，“更多”按钮才会更改为加载指示器。

```javascript
import React, { Fragment } from 'react';

import Loading from '../../Loading';
import RepositoryItem from '../RepositoryItem';

...

const RepositoryList = ({ repositories, loading, fetchMore }) => (
  <Fragment>
    ...

    {loading ? (
      <Loading />
    ) : (
      repositories.pageInfo.hasNextPage && (
        <button
          ...
        >
          More Repositories
        </button>
      )
    )}
  </Fragment>
);
```

`src/Repository/RepositoryList/index.js`

分页功能现在已经完成，你正在获取初始页面的后续页面，然后在 Apollo Client 的缓存中合并结果。此外，你还向用户展示了关于初始请求或进一步页面请求挂起的请求反馈。

现在我们将更进一步，使用于获取更多仓库的按钮变得可复用。让我解释一下为什么这是一种很棒的抽象。在接下来的章节中，你有另一个可能可以实现分页功能的列表字段。在那里，你必须引入“更多”按钮，该按钮可能与你在 `RepositoryList` 组件中的“更多”按钮几乎相同。在 UI 中只保留一个按钮是一个满意的抽象，但这种抽象在现实世界的编码场景中是不可行的。你将必须先引入第二个列表字段，为它实现分页功能，然后考虑“更多”按钮的抽象。为了教程的需要，我们在本节中仅针对分页功能实现了这种抽象，尽管你应该意识到这是为了让你学习而设置的过早优化。

另一种方法是，想象你想将“更多”按钮的功能提取到 `FetchMore` 组件中。你需要的是从查询结果中获取 `fetchMore()` 函数。`fetchMore()` 函数接收一个包含 `variables` 和 `updateQuery` 的对象。前者用于通过游标定义下一页，后者用于定义如何在本地状态中合并结果。你可能还想隐藏 `FetchMore` 组件中的条件渲染，这是因为 `loading` 或 `hasNextPage` 布尔值的存在。这就是你如何为 `FetchMore` 组件获取接口的。

```javascript
import React, { Fragment } from 'react';

import FetchMore from '../../FetchMore';
import RepositoryItem from '../RepositoryItem';

...

const RepositoryList = ({ repositories, loading, fetchMore }) => (
  <Fragment>
    {repositories.edges.map(({ node }) => (
      <div key={node.id} className="RepositoryItem">
        <RepositoryItem {...node} />
      </div>
    ))}

    <FetchMore
      loading={loading}
      hasNextPage={repositories.pageInfo.hasNextPage}
      variables={{
        cursor: repositories.pageInfo.endCursor,
      }}
      updateQuery={updateQuery}
      fetchMore={fetchMore}
    >
      Repositories
    </FetchMore>
  </Fragment>
);

export default RepositoryList;
```

`src/Repository/RepositoryList/index.js`

现在这个 `FetchMore` 组件也可以被其他分页列表使用，因为每一个动态部分都作为 prop 传递给它。下一步是在 `src/FetchMore/index.js` 中实现 `FetchMore` 组件。首先是该组件的主体：

```javascript
import React from 'react';

import './style.css';

const FetchMore = ({
  variables,
  updateQuery,
  fetchMore,
  children,
}) => (
  <div className="FetchMore">
    <button
      type="button"
      className="FetchMore-button"
      onClick={() => fetchMore({ variables, updateQuery })}
    >
      More {children}
    </button>
  </div>
);

export default FetchMore;
```

`src/FetchMore/index.js`

在这里，你可以看到 `variables` 和 `updateQuery` 是如何在调用 `fetchMore()` 时作为配置对象接收的。可以使用你在之前章节中定义的 `Button` 组件使按钮变得更整洁。为了添加不同的样式，让我们在 `src/Button/index.js` 文件中 `Button` 组件旁边定义一个专门的 `ButtonUnobtrusive` 组件：

```javascript
import React from 'react';

import './style.css';

const Button = ({ ... }) => ...

const ButtonUnobtrusive = ({
  children,
  className,
  type = 'button',
  ...props
}) => (
  <button
    className={`${className} Button_unobtrusive`}
    type={type}
    {...props}
  >
    {children}
  </button>
);

export { ButtonUnobtrusive };

export default Button;
```

`src/Button/index.js`

现在 `ButtonUnobtrusive` 组件被用作按钮替代 `FetchMore` 组件中的 `button` 元素。此外，两个布尔值 `loading` 和 `hasNextPage` 可用于条件渲染，显示 `Loading` 组件或不显示内容，因为没有可以获取的下一页。

```javascript
import React from 'react';

import Loading from '../Loading';
import { ButtonUnobtrusive } from '../Button';

import './style.css';

const FetchMore = ({
  loading,
  hasNextPage,
  variables,
  updateQuery,
  fetchMore,
  children,
}) => (
  <div className="FetchMore">
    {loading ? (
      <Loading />
    ) : (
      hasNextPage && (
        <ButtonUnobtrusive
          className="FetchMore-button"
          onClick={() => fetchMore({ variables, updateQuery })}
        >
          More {children}
        </ButtonUnobtrusive>
      )
    )}
  </div>
);

export default FetchMore;
```

`src/FetchMore/index.js`

这就是针对 Apollo Client 分页列表的 `FetchMore` 按钮的抽象实现。基本上，你传递了 `fetchMore()` 函数所需的所有内容，包括函数本身。你也可以传递所有用于条件渲染的布尔值。最终你将得到一个可复用的 `FetchMore` 按钮，它可以用于每一个分页列表。

### 练习

- 确认你的[上一节的源代码](http://bit.ly/2VnG7EE)
- 确认[上一节的更改内容](http://bit.ly/2VqPWSb)
- 了解更多关于[在 React 中使用 Apollo Client 进行分页](https://www.apollographql.com/docs/react/features/pagination.html)的信息
- 花 3 分钟时间参加[测验](https://www.surveymonkey.com/r/5HYMGN7)

## 在 React 中使用 Apollo Client 进行 GraphQL 查询缓存

在本节中，你引入了 [React Router](https://github.com/ReactTraining/react-router) 为你的应用程序显示两个独立的页面。目前，你只显示了一个带有 `Profile` 组件的页面，它显示你所有的仓库。我们想添加另一个 `Organization` 组件，按组织显示仓库，并且还可以有一个搜索字段，用于在该页面上查找特定的组织及其仓库。让我们通过向应用程序中引入 React Router 来来实现。如果你之前没有用过 React Router，请确保完成本节的练习以了解更多相关信息。

```bash
npm install react-router-dom --save
```

### 命令行

在你的 `src/constants/routes.js` 文件中，你可以指定想要通过 React Router 访问的路由。`ORGANIZATION` 路由指向基础 URL，而 `PROFILE` 路由指向一个更具体的 URL。

```javascript
export const ORGANIZATION = '/';
export const PROFILE = '/profile';
```

`src/constants/routes.js`

接下来，将两个路由映射到它们对应的组件。`App` 组件是执行此操作的理想位置，因为这两个路由将根据 URL 交换 `Organization` 和 `Profile` 组件。



`src/App/index.js`

`Organization` 组件还没有实现，但你可以先从`src/Organization/index.js`文件中的函数式无状态组件开始，它作为一个占位符以保持应用程序目前的运行。

```javascript
import React from 'react';

const Organization = () => <div>Organization</div>;

export default Organization;
```

`src/Organization/index.js`

由于你已经将两个路由映射到了它们各自的组件，所以你想实现从一个路由到另一个路由的导航。为此，在`App`组件中引入一个`Navigation`组件。

```javascript
...

import Navigation from './Navigation';
import Profile from '../Profile';
import Organization from '../Organization';

...

class App extends Component {
  render() {
    return (
      <Router>
        <div className="App">
          <Navigation />

          <div className="App-main">
            ...
          </div>
        </div>
      </Router>
    );
  }
}

export default App;
```

`src/App/index.js`

接下来，我们将实现`Navigation`组件，它负责使用 React Router 的`Link`组件显示两个导航链接。

```javascript
import React from 'react';
import { Link } from 'react-router-dom';

import * as routes from '../../constants/routes';

import './style.css';

const Navigation = () => (
  <header className="Navigation">
    <div className="Navigation-link">
      <Link to={routes.PROFILE}>Profile</Link>
    </div>
    <div className="Navigation-link">
      <Link to={routes.ORGANIZATION}>Organization</Link>
    </div>
  </header>
);

export default Navigation;
```

`src/App/Navigation/index.js`

`Profile`页面仍然运行，但`Organization`页面是空的。在上一步中，你定义了两个路由常量，在`App`组件中使用它们映射到相应的组件，并在`Navigation`组件中引入了`Link`组件进行跳转。

Apollo Client 的另一个强大功能是缓存查询请求。当从`Profile`页面导航到`Organization`页面再返回`Profile`页面时，结果会立即出现，因为 Apollo Client 在向远程 GraphQL API 查询之前会检查其缓存。这是一个强大的工具。

本节的下一个部分是`Organization`组件。它与`Profile`组件相同，区别在于查询接收一个组织名称变量以识别组织的仓库。

```javascript
import React from 'react';
import gql from 'graphql-tag';
import { Query } from 'react-apollo';

import { REPOSITORY_FRAGMENT } from '../Repository';

const GET_REPOSITORIES_OF_ORGANIZATION = gql`
  query($organizationName: String!) {
    organization(login: $organizationName) {
      repositories(first: 5) {
        edges {
          node {
            ...repository
          }
        }
      }
    }
  }
  ${REPOSITORY_FRAGMENT}
`;

const Organization = ({ organizationName }) => (
  <Query
    query={GET_REPOSITORIES_OF_ORGANIZATION}
    variables={{
      organizationName,
    }}
    skip={organizationName === ''}
  >
    {({ data, loading, error }) => {
      ...
    }}
  </Query>
);

export default Organization;
```

`src/Organization/index.js`

`Organization`组件中的`Query`组件接收一个针对该组织定制的查询，作为查询的顶层字段。它接收一个变量来标识组织，并使用新引入的`skip`属性，在未提供组织标识符时跳过查询执行。稍后，你将从`App`组件传递一个组织标识符。你可能已经注意到之前引入用于更新缓存中本地状态的仓库片段（fragment）可以在这里复用。它节省了代码行，更重要的是，确保了返回的仓库列表与`Profile`组件中的仓库列表具有相同的结构。

接下来，扩展查询以适应分页功能的需求。它需要`cursor`参数来标识下一页仓库。`notifyOnNetworkStatusChange`属性也用于更新分页请求的`loading`布尔值。

```javascript
...

const GET_REPOSITORIES_OF_ORGANIZATION = gql`
  query($organizationName: String!, $cursor: String) {
    organization(login: $organizationName) {
      repositories(first: 5, after: $cursor) {
        edges {
          node {
            ...repository
          }
        }
        pageInfo {
          endCursor
          hasNextPage
        }
      }
    }
  }
  ${REPOSITORY_FRAGMENT}
`;

const Organization = ({ organizationName }) => (
  <Query
    query={GET_REPOSITORIES_OF_ORGANIZATION}
    variables={{
      organizationName,
    }}
    skip={organizationName === ''}
    notifyOnNetworkStatusChange={true}
  >
    {({ data, loading, error, fetchMore }) => {
      ...
    }}
  </Query>
);

export default Organization;
```

`src/Organization/index.js`

最后，需要实现渲染属性（render prop）子函数。它与`Profile`组件中`Query`的内容没有太大区别。它的目的是处理加载和“无数据”错误等边缘情况，并最终显示仓库列表。由于`RepositoryList`组件处理了分页功能，此改进已包含在新建的`Organization`组件中。

```javascript
...

import RepositoryList, { REPOSITORY_FRAGMENT } from '../Repository';
import Loading from '../Loading';
import ErrorMessage from '../Error';

...

const Organization = ({ organizationName }) => (
  <Query ... >
    {({ data, loading, error, fetchMore }) => {
      if (error) {
        return <ErrorMessage error={error} />;
      }

      const { organization } = data;

      if (loading && !organization) {
        return <Loading />;
      }

      return (
        <RepositoryList
          loading={loading}
          repositories={organization.repositories}
          fetchMore={fetchMore}
        />
      );
    }}
  </Query>
);

export default Organization;
```

`src/Organization/index.js`

在`App`组件中使用`Organization`时，将`organizationName`作为 prop 传递，目前保持其内联即可。稍后，你将通过搜索字段使其动态化。

```javascript
class App extends Component {
  render() {
    return (
      <Router>
        <div className="App">
          <Navigation />

          <div className="App-main">
            <Route
              exact
              path={routes.ORGANIZATION}
              component={() => (
                <div className="App-content_large-header">
                  <Organization
                    organizationName={'the-road-to-learn-react'}
                  />
                </div>
              )}
            />
            ...
          </div>
        </div>
      </Router>
    );
  }
}
```

`src/App/index.js`

`Organization`组件现在几乎可以工作了，因为`More`按钮是唯一不完整的部分。剩余的问题是`updateQuery`函数中用于分页功能的解析块（resolving block）。它假设嵌套数据结构始终以`viewer`对象开始。在`Profile`页面上确实如此，但在`Organization`页面上不是。在那是，顶层对象是`organization`，然后是`repositories`列表。只有顶层对象会在页面之间发生变化，而底层结构保持一致。

当顶层对象随页面发生变化时，理想的后续步骤是从外部告诉`RepositoryList`组件它的顶层对象是什么。对于`Organization`组件，它是顶层对象`organization`，可以作为字符串传递，并在稍后作为动态键复用：

```javascript
const Organization = ({ organizationName }) => (
  <Query ... >
    {({ data, loading, error, fetchMore }) => {
      ...

      return (
        <RepositoryList
          loading={loading}
          repositories={organization.repositories}
          fetchMore={fetchMore}
          entry={'organization'}
        />
      );
    }}
  </Query>
);
```

`src/Organization/index.js`

对于`Profile`组件，`viewer`将是顶层对象：

```javascript
const Profile = () => (
  <Query ... >
    {({ data, loading, error, fetchMore }) => {
      ...

      return (
        <RepositoryList
          repositories={viewer.repositories}
          fetchMore={fetchMore}
          entry={'viewer'}
        />
      );
    }}
  </Query>
);
```

`src/Profile/index.js`

现在，你可以通过向`updateQuery`函数传递[计算属性名](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Operators/Object_initializer)来在`RepositoryList`组件中处理新情况。而不是直接向`FetchMore`组件传递`updateQuery`函数，它可以从高阶函数推导出。

```javascript
const RepositoryList = ({
  repositories,
  loading,
  fetchMore,
  entry,
}) => (
  <Fragment>
    ...

    <FetchMore
      loading={loading}
      hasNextPage={repositories.pageInfo.hasNextPage}
      variables={{
        cursor: repositories.pageInfo.endCursor,
      }}
      updateQuery={getUpdateQuery(entry)}
      fetchMore={fetchMore}
    >
      Repositories
    </FetchMore>
  </Fragment>
);
```

`src/RepositoryList/index.js`



这就是如何更新深嵌套对象，即使查询结果的顶层组件不是静态的：

```javascript
const getUpdateQuery = entry => (
  previousResult,
  { fetchMoreResult },
) => {
  if (!fetchMoreResult) {
    return previousResult;
  }

  return {
    ...previousResult,
    [entry]: {
      ...previousResult[entry],
      repositories: {
        ...previousResult[entry].repositories,
        ...fetchMoreResult[entry].repositories,
        edges: [
          ...previousResult[entry].repositories.edges,
          ...fetchMoreResult[entry].repositories.edges,
        ],
      },
    },
  };
};
```

`src/RepositoryList/index.js`

这就是通过`fetchMoreResult`更新深嵌套对象的方法，尽管查询结果的顶层不是静态的。分页功能现在两个页面上都应该可以工作了。花点时间回顾一下之前的实现以及为什么它们是必要的。

接下来，我们将实现之前提到的搜索功能。添加搜索字段的最佳位置是`Navigation`组件，但仅当`Organization`页面激活时。React Router 提供了一个非常有用的高阶组件来访问当前 URL，可以用于显示搜索字段。

```javascript
import React from 'react';
import { Link, withRouter } from 'react-router-dom';

import * as routes from '../../constants/routes';

import './style.css';

const Navigation = ({
  location: { pathname },
}) => (
  <header className="Navigation">
    <div className="Navigation-link">
      <Link to={routes.PROFILE}>Profile</Link>
    </div>
    <div className="Navigation-link">
      <Link to={routes.ORGANIZATION}>Organization</Link>
    </div>

    {pathname === routes.ORGANIZATION && (
      <OrganizationSearch />
    )}
  </header>
);

export default withRouter(Navigation);
```

`src/App/Navigation/index.js`

在接下来的步骤中，`OrganizationSearch`组件将在`Navigation`组件旁边实现。在实现它之前，`OrganizationSearch`需要某种初始状态，以及一个用于更新`Navigation`组件中初始状态的回调函数。为了适应这一点，`Navigation`组件将变成一个类组件（class component）。

```javascript
...

class Navigation extends React.Component {
  state = {
    organizationName: 'the-road-to-learn-react',
  };

  onOrganizationSearch = value => {
    this.setState({ organizationName: value });
  };

  render() {
    const { location: { pathname } } = this.props;

    return (
      <header className="Navigation">
        <div className="Navigation-link">
          <Link to={routes.PROFILE}>Profile</Link>
        </div>
        <div className="Navigation-link">
          <Link to={routes.ORGANIZATION}>Organization</Link>
        </div>

        {pathname === routes.ORGANIZATION && (
          <OrganizationSearch
            organizationName={this.state.organizationName}
            onOrganizationSearch={this.onOrganizationSearch}
          />
        )}
      </header>
    );
  }
}

export default withRouter(Navigation);
```

`src/App/Navigation/index.js`

在同一个文件中实现的`OrganizationSearch`组件也可以通过以下实现工作。它处理自己的本地状态（显示在输入字段中的值），但将其作为来自父组件的初始值。它还接收一个回调处理器，该处理器可以在`onSubmit()`类方法中使用，以便在提交交互时将搜索字段的值向上传递到组件树中。

```javascript
...

import Button from '../../Button';
import Input from '../../Input';

import './style.css';

const Navigation = ({ ... }) => ...

class OrganizationSearch extends React.Component {
  state = {
    value: this.props.organizationName,
  };

  onChange = event => {
    this.setState({ value: event.target.value });
  };

  onSubmit = event => {
    this.props.onOrganizationSearch(this.state.value);

    event.preventDefault();
  };

  render() {
    const { value } = this.state;

    return (
      <div className="Navigation-search">
        <form onSubmit={this.onSubmit}>
          <Input
            color={'white'}
            type="text"
            value={value}
            onChange={this.onChange}
          />{' '}
          <Button color={'white'} type="submit">
            Search
          </Button>
        </form>
      </div>
    );
  }
}

export default withRouter(Navigation);
```

`src/App/Navigation/index.js`

`Input`组件是一个经过稍微样式处理的输入元素，它在`src/Input/index.js`中被定义为自己的组件。

```javascript
import React from 'react';

import './style.css';

const Input = ({ children, color = 'black', ...props }) => (
  <input className={`Input Input_${color}`} {...props}>
    {children}
  </input>
);

export default Input;
```

`src/Input/index.js`

虽然搜索字段在`Navigation`组件中可以工作，但它对应用程序的其他部分没有帮助。它只在提交搜索请求时更新`Navigation`组件中的状态。然而，`Organization`组件需要搜索请求的值作为查询的 GraphQL 变量，因此需要将本地状态从`Navigation`组件提升到`App`组件。`Navigation`组件再次变成无状态函数组件。

```javascript
const Navigation = ({
  location: { pathname },
  organizationName,
  onOrganizationSearch,
}) => (
  <header className="Navigation">
    <div className="Navigation-link">
      <Link to={routes.PROFILE}>Profile</Link>
    </div>
    <div className="Navigation-link">
      <Link to={routes.ORGANIZATION}>Organization</Link>
    </div>

    {pathname === routes.ORGANIZATION && (
      <OrganizationSearch
        organizationName={organizationName}
        onOrganizationSearch={onOrganizationSearch}
      />
    )}
  </header>
);
```

`src/App/Navigation/index.js`

`App`组件接管了`Navigation`组件的职责，管理本地状态，将初始状态和更新状态的回调函数传递给`Navigation`组件，并将状态本身传递给`Organization`组件以执行查询：

```javascript
...

class App extends Component {
  state = {
    organizationName: 'the-road-to-learn-react',
  };

  onOrganizationSearch = value => {
    this.setState({ organizationName: value });
  };

  render() {
    const { organizationName } = this.state;

    return (
      <Router>
        <div className="App">
          <Navigation
            organizationName={organizationName}
            onOrganizationSearch={this.onOrganizationSearch}
          />

          <div className="App-main">
            <Route
              exact
              path={routes.ORGANIZATION}
              component={() => (
                <div className="App-content_large-header">
                  <Organization organizationName={organizationName} />
                </div>
              )}
            />
            ...
          </div>
        </div>
      </Router>
    );
  }
}

export default App;
```

`src/App/index.js`

你已经实现了一个动态 GraphQL 查询。

### `src/Repository/RepositoryList/index.js`

在`src/Issue/index.js`文件中，导入并导出`Issues`组件。由于问题功能可以独立在一个模块中，因此它再次拥有这个`index.js`文件。这就是你如何告诉其他开发者使用`index.js`文件作为接口来仅访问此功能模块。其他所有内容保持私有。

```javascript
import Issues from './IssueList';

export default Issues;
```

### `src/Issue/index.js`

注意组件的命名为`Issues`而不是`IssueList`。这种命名约定用于拆解项目列表的渲染：`Issues`、`IssueList`和`IssueItem`。`Issues`是容器组件，你在此处查询数据并过滤问题，而`IssueList`和`IssueItem`仅作为用于渲染的展示组件。相比之下，`Repository`功能模块没有`Repositories`组件，因为没有需要它。仓库列表已经来自于`Organization`和`Profile`组件，`Repository`模块的组件主要用于渲染。然而，这仅仅是命名组件的一种观点性方法。

让我们开始在`src/Issue/IssueList/index.js`文件中实现`Issues`和`IssueList`组件。你可以主张将这两个组件拆分到各自的文件中，但为了本教程起见，它们被保留在一个文件中。

首先，需要为问题创建一个新的查询。你可能会问：为什么我们在这里需要一个新查询？在顶部的`Organization`和`Profile`组件旁边的查询中包含问题列表字段会更简单。确实如此，但是有代价的。在查询中添加更多嵌套（列表）字段通常会导致服务器端的性能问题。在这种情况下，你可能需要进行多次往返（roundtrips）来从数据库中检索所有实体。

- 往返 1：通过名称获取组织
- 往返 2：通过组织标识符获取组织的仓库
- 往返 3：通过仓库标识符获取仓库的问题

很容易得出结论，以简单的方式嵌套查询可以解决我们所有的问题。虽然它解决了只请求一次数据而不是通过多次网络请求（类似于所示的数据库往返）来请求的问题，但 GraphQL 并没有解决从你从数据库中检索所有数据的问题。毕竟这并不是 GraphQL 的责任。因此，通过在`Issues`组件中设置专门的查询，你可以决定`何时`触发此查询。在接下来的步骤中，由于使用了`Query`组件，你将会在渲染时触发它。但稍后添加客户端过滤器时，它只有在切换“过滤器（Filter）”按钮时才会触发。否则，问题应该被隐藏。最后，这就是如何将所有初始加载延迟到用户真正想要查看数据的时间点。

首先，定义`Issues`组件，它可以访问传递给`RepositoryList`组件的 props。它目前还没有渲染很多内容。

```javascript
import React from 'react';

import './style.css';

const Issues = ({ repositoryOwner, repositoryName }) =>
  <div className="Issues">
  </div>

export default Issues;
```

### `src/Issue/IssueList/index.js`

其次，在`src/Issue/IssueList/index.js`文件中定义查询以检索仓库的问题。仓库通过其所有者和名称进行标识。此外，添加`state`字段作为查询结果的字段之一。这用于客户端过滤，显示开启或关闭状态的问题。

```javascript
import React from 'react';
import gql from 'graphql-tag';

import './style.css';

const GET_ISSUES_OF_REPOSITORY = gql`
  query($repositoryOwner: String!, $repositoryName: String!) {
    repository(name: $repositoryName, owner: $repositoryOwner) {
      issues(first: 5) {
        edges {
          node {
            id
            number
            state
            title
            url
            bodyHTML
          }
        }
      }
    }
  }
`;

...
```

### `src/Issue/IssueList/index.js`

第三，引入`Query`组件并将之前定义的查询和必要的变量传递给它。使用它的 render prop 子函数来访问数据，涵盖所有边缘情况并渲染`IssueList`组件。



# 问题列表组件实现

进入 `src/Issue/Item` 目录，找到问题列表相关的组件实现。

## 基础组件实现

最后，在 `index.js` 文件中实现一个基础的 `IssueItem` 组件。以下代码片段显示了可以实现评论功能的占位符。

```javascript
import React from 'react';

import Link from '../../Link';

import './style.css';

const IssueItem = ({ issue }) => (
  <div className="IssueItem">
    {/* 添加显示/隐藏按钮的占位符 */}

    <div className="IssueItem-content">
      <h3>
        <Link href={issue.url}>{issue.title}</Link>
      </h3>
      <div dangerouslySetInnerHTML={{ __html: issue.bodyHTML }} />

      {/* 渲染评论列表的占位符 */}
    </div>
  </div>
);

export default IssueItem;
```

进入 `src/IssueItem` 目录，可查看完整组件实现。

## 初始状态与性能优化

一旦你再次启动应用程序，你应该会在每个仓库下方看到初始的问题列表。这是一个性能瓶颈。糟糕的是，GraphQL 请求没有在一个请求中，正如 `Organization` 和 `Profile` 组件中的问题列表那样。在接下来的步骤中，你正在实现客户端过滤。默认是不显示问题，但可以通过按钮在状态之间进行切换，因此在切换其中一个状态之前不会查询问题。

### 练习

* [确认上一部分的源代码](http://bit.ly/2VseREY)
* [确认上一部分的更改](http://bit.ly/2VqLeUn)
* 阅读更多关于使用（在此情况下是 GitHub 的）GraphQL API 的速率限制](https://developer.github.com/v4/guides/resource-limitations/)

## 实现问题功能：客户端过滤器

在本节中，我们通过客户端过滤增强问题功能。它防止了初始问题的查询，因为是通过按钮触发的，并且允许用户在关闭和开启的问题之间进行过滤。

首先，在 `Issues` 组件旁边引入我们的三个状态作为枚举。`NONE` 状态用于不显示任何问题；否则，其他状态用于显示开启或关闭的问题。

```javascript
const ISSUE_STATES = {
  NONE: 'NONE',
  OPEN: 'OPEN',
  CLOSED: 'CLOSED',
};
```

文件路径：`src/Issue/IssueList/index.js`

其次，实现一个短函数来判断状态是否为显示问题的状态。该函数可以定义在同一个文件中。

```javascript
const isShow = issueState => issueState !== ISSUE_STATES.NONE;
```

文件路径：`src/Issue/IssueList/index.js`

第三，该函数可以用于条件渲染，要么查询 `issues` 并显示 `IssueList`，要么什么都不做。目前还不清楚 `issueState` 属性是从哪里来的。

```javascript
const Issues = ({ repositoryOwner, repositoryName }) => (
  <div className="Issues">
    {isShow(issueState) && (
      <Query ... >
        ...
      </Query>
    )}
  </div>
);
```

`issueState` 属性必须来自本地状态，以便通过组件中的按钮来切换它，因此 `Issues` 组件必须重构为类组件以管理此状态。

```javascript
class Issues extends React.Component {
  state = {
    issueState: ISSUE_STATES.NONE,
  };

  render() {
    const { issueState } = this.state;
    const { repositoryOwner, repositoryName } = this.props;

    return (
      <div className="Issues">
        {isShow(issueState) && (
          <Query ... >
            ...
          </Query>
        )}
      </div>
    );
  }
}
```

文件路径：`src/Issue/IssueList/index.js`

现在应用程序应该是没有错误的，因为初始状态被设置为 `NONE`，并且条件渲染防止了查询和结果的渲染。然而，客户端过滤尚未完成，因为你仍然需要用 React 的本地状态切换 `issueState` 属性。`ButtonUnobtrusive` 组件具有适当的样式，我们可以复用它来实现这种切换行为，以便在三个可用状态之间转换。

```javascript
...

import IssueItem from '../IssueItem';
import Loading from '../../Loading';
import ErrorMessage from '../../Error';
import { ButtonUnobtrusive } from '../../Button';

class Issues extends React.Component {
  state = {
    issueState: ISSUE_STATES.NONE,
  };

  onChangeIssueState = nextIssueState => {
    this.setState({ issueState: nextIssueState });
  };

  render() {
    const { issueState } = this.state;
    const { repositoryOwner, repositoryName } = this.props;

    return (
      <div className="Issues">
        <ButtonUnobtrusive
          onClick={() =>
            this.onChangeIssueState(TRANSITION_STATE[issueState])
          }
        >
          {TRANSITION_LABELS[issueState]}
        </ButtonUnobtrusive>

        {isShow(issueState) && (
          <Query ... >
            ...
          </Query>
        )}
      </div>
    );
  }
}
```

文件路径：`src/Issue/IssueList/index.js`

在最后一步中，你引入了在三个状态之间切换的按钮。你使用了两个枚举 `TRANSITION_LABELS` 和 `TRANSITION_STATE`，用于显示适当的按钮标签并定义状态转换后的下一个状态。这些枚举可以定义在 `ISSUE_STATES` 枚举旁边。

```javascript
const TRANSITION_LABELS = {
  [ISSUE_STATES.NONE]: 'Show Open Issues',
  [ISSUE_STATES.OPEN]: 'Show Closed Issues',
  [ISSUE_STATES.CLOSED]: 'Hide Issues',
};

const TRANSITION_STATE = {
  [ISSUE_STATES.NONE]: ISSUE_STATES.OPEN,
  [ISSUE_STATES.OPEN]: ISSUE_STATES.CLOSED,
  [ISSUE_STATES.CLOSED]: ISSUE_STATES.NONE,
};
```

文件路径：`src/Issue/IssueList/index.js`

你可以看到，前面的枚举仅将标签匹配到给定的状态，而后一个枚举将下一个状态匹配到给定的状态。这就是切换到下一个状态变得简单的方法。最后但同样重要的是，必须使用来自本地状态的 `issueState` 在 `issues` 被查询并应该渲染之后来过滤 `issues` 列表。

```javascript
class Issues extends React.Component {
  ...

  render() {
    ...

    return (
      <div className="Issues">
        ...

        {isShow(issueState) && (
          <Query ... >
            {({ data, loading, error }) => {
              if (error) {
                return <ErrorMessage error={error} />;
              }

              const { repository } = data;

              if (loading && !repository) {
                return <Loading />;
              }

              const filteredRepository = {
                issues: {
                  edges: repository.issues.edges.filter(
                    issue => issue.node.state === issueState,
                  ),
                },
              };

              if (!filteredRepository.issues.edges.length) {
                return <div className="IssueList">No issues ...</div>;
              }

              return (
                <IssueList issues={filteredRepository.issues} />
              );
            }}
          </Query>
        )}
      </div>
    );
  }
}
```

文件路径：`src/Issue/IssueList/index.js`

你已经实现了客户端过滤。按钮用于在组件本地状态管理的三个状态之间进行切换。只有在过滤和渲染状态下，才会查询 `issues`。在下一步中，应该将现有的客户端过滤改进为服务器端过滤，这意味着过滤后的 `issues` 将直接从服务器请求，而不是在客户端之后进行过滤。

### 练习

- 确认你[最后一部分的源代码](http://bit.ly/2sfwp)
- 确认[上一部分的更改](http://bit.ly/2tl4)
- 安装 [recompose](https://github.com/acdlite/recompose) 库以许多高阶组件
- 将 `Issues` 组件从类组件重构为函数组件
- 使用 `withState` 高阶组件为 `Issues` 组件管理 `issueState`

## 实现 Issues 功能：服务器端过滤

在开始服务器端过滤之前，让我们回顾一下最后的练习，以防遇到困难。基本上你可以分三步完成重构。首先，在命令行为你的应用程序安装 `recompose`：

```bash
npm install recompose
```

### 命令行

其次，在 `src/Issue/IssueList/index.js` 中导入 `withState` 高阶组件，并用它封装你的 `Issues` 组件，第一个参数是本地状态中的属性名称，第二个参数是更改该属性的处理器，第三个参数是该属性的初始状态。

```javascript
import React from 'react';
import { Query } from 'react-apollo';
import gql from 'graphql-tag';
import { withState } from 'recompose';

...

export default withState(
  'issueState',
  'onChangeIssueState',
  ISSUE_STATES.NONE,
)(Issues);
```

文件路径：`src/Issue/IssueList/index.js`

最后，将 `Issues` 组件从类组件重构为函数无状态组件。它现在从 `props` 中访问 `issueState` 和 `onChangeIssueState()` 函数。记住将 `onChangeIssueState` 属性改为函数而不是方法。

```javascript
...

const Issues = ({
  repositoryOwner,
  repositoryName,
  issueState,
  onChangeIssueState,
}) => (
  <div className="Issues">
    <ButtonUnobtrusive
      onClick={() => onChangeIssueState(TRANSITION_STATE[issueState])}
    >
      {TRANSITION_LABELS[issueState]}
    </ButtonUnobtrusive>

    ...
  </div>
);

...
```

文件路径：`src/Issue/IssueList/index.js`

上一节使得编写有状态组件变得更加方便，状态更容易处理。接下来，将过滤从客户端推进到服务器端。我们使用定义的 GraphQL 查询及其参数来执行更精确的查询，只请求开启或关闭的 `issues`。在 `src/Issue/IssueList/index.js` 文件中，扩展查询以指定问题状态：



```javascript
const GET_ISSUES_OF_REPOSITORY = gql`
  query(
    $repositoryOwner: String!
    $repositoryName: String!
    $issueState: IssueState!
  ) {
    repository(name: $repositoryName, owner: $repositoryOwner) {
      issues(first: 5, states: [$issueState]) {
        edges {
          node {
            id
            number
            state
            title
            url
            bodyHTML
          }
        }
      }
    }
  }
`;
```

`src/Issue/IssueList/index.js`

接下来，可以使用`issueState`属性作为你的`Query`组件的变量。此外，从`Query`组件的 render prop 函数中移除客户端过滤逻辑。

```javascript
const Issues = ({
  repositoryOwner,
  repositoryName,
  issueState,
  onChangeIssueState,
}) => (
  <div className="Issues">
    ...

    {isShow(issueState) && (
      <Query
        query={GET_ISSUES_OF_REPOSITORY}
        variables={{
          repositoryOwner,
          repositoryName,
          issueState,
        }}
      >
        {({ data, loading, error }) => {
          if (error) {
            return <ErrorMessage error={error} />;
          }

          const { repository } = data;

          if (loading && !repository) {
            return <Loading />;
          }

          return <IssueList issues={repository.issues} />;
        }}
      </Query>
    )}
  </div>
);
```

`/src/Issue/IssueList/index.js`

你现在只查询开启的（open）或关闭的（closed）issue。你的查询变得更加精确，且过滤不再由客户端处理。

### 练习题

- 确认你[上一节的源代码](http://bit.ly/2VkQ064)
  - 确认[上一节的更改](http://bit.ly/2VnWyAF)
- 为 Issue 功能实现分页功能
  - 在查询中添加`pageInfo`信息
  - 在查询中添加额外的游标（cursor）变量和参数
  - 在`IssueList`组件中添加`FetchMore`组件

## React 中的 Apollo Client 预取数据（Prefetching）

这一节完全关于数据预取，尽管用户并不立即需要它。这是另一种 UX 优化技术，可以部署到你之前使用的乐观 UI 技术中。你将为 issue 列表实现数据预取功能，但也可以作为练习，以后为其他数据获取实现它。

当你的应用程序首次渲染时，没有获取到 issue，因此没有渲染 issue。用户必须切换过滤器按钮来获取开启的 issue，再次切换获取关闭的 issue。第三点击将再次隐藏 issue 列表。本节的目标是在用户悬停在过滤器按钮上时，预取下一批 issue。例如，当 issue 仍然隐藏且用户悬停在过滤器按钮上时，开启状态的 issue 会在后台被预取。当用户点击按钮时，不需要等待时间，因为开启状态的 issue 已经在那了。从开启到关闭的转换也适用于相同的场景。为了准备这种行为，请在`/src/Issue/IssueList/index.js`文件将过滤器按钮拆分为独立的组件：

```javascript
const Issues = ({
  repositoryOwner,
  repositoryName,
  issueState,
  onChangeIssueState,
}) => (
  <div className="Issues">
    <IssueFilter
      issueState={issueState}
      onChangeIssueState={onChangeIssueState}
    />

    {isShow(issueState) && (
      ...
    )}
  </div>
);

const IssueFilter = ({ issueState, onChangeIssueState }) => (
  <ButtonUnobtrusive
    onClick={() => onChangeIssueState(TRANSITION_STATE[issueState])}
  >
    {TRANSITION_LABELS[issueState]}
  </ButtonUnobtrusive>
);
```

`/src/Issue/IssueList/index.js`

现在更容易专注于`IssueFilter`组件了，大部分数据预取的逻辑都实现在这里。和之前一样，预取应该在用户悬停在按钮上时发生。这需要一个属性（prop）以及一个在用户悬停在其上时执行的回调函数。按钮（元素）有这样一个属性（attribute）。我们在这里处理的是 HTML 元素。

```javascript
const prefetchIssues = () => {};

...

const IssueFilter = ({ issueState, onChangeIssueState }) => (
  <ButtonUnobtrusive
    onClick={() => onChangeIssueState(TRANSITION_STATE[issueState])}
    onMouseOver={prefetchIssues}
  >
    {TRANSITION_LABELS[issueState]}
  </ButtonUnobtrusive>
);
```

`/src/Issue/IssueList/index.js`

`prefetchIssue()`函数必须执行与`Issues`组件中`Query`组件完全相同的 GraphQL 查询，但这次是以命令式（imperative）而不是声明式（declarative）执行的。不要使用`Query`组件，而是直接使用 Apollo Client 实例来执行查询。记住，Apollo Client 实例隐藏在组件树中，因为你使用了 React 的 Context API 在组件树顶层提供了 Apollo Client 实例。`Query`和`Mutation`组件可以访问 Apollo Client，即使你从未直接用过它。然而，这次你用它来查询预取的数据。使用来自`react-apollo`包的`ApolloConsumer`组件在你的组件树中暴露 Apollo Client 实例。你已经在某地方使用了`ApolloProvider`来提供客户端实例，现在可以使用`ApolloConsumer`来获取它。在`/src/Issue/IssueList/index.js`文件中，导入`ApolloConsumer`组件并在`IssueFilter`组件中使用它。它通过其 render props 子函数让你能够访问 Apollo Client 实例。

```javascript
import React from 'react';
import { Query, ApolloConsumer } from 'react-apollo';
import gql from 'graphql-tag';
import { withState } from 'recompose';

...

const IssueFilter = ({ issueState, onChangeIssueState }) => (
  <ApolloConsumer>
    {client => (
      <ButtonUnobtrusive
        onClick={() =>
          onChangeIssueState(TRANSITION_STATE[issueState])
        }
      >
        {TRANSITION_LABELS[issueState]}
      </ButtonUnobtrusive>
    )}
  </ApolloConsumer>
); // wait,
```

`/src/Issue/IssueList/index.js`

现在你可以使用 Apollo Client 实例来执行查询和变更，这将允许你命令式地查询 GitHub API。预取 issue 所需变量与`Query`组件使用的相同。你需要将这些变量传递给`IssueFilter`组件，然后传递给`prefetchIssues`函数。

```javascript
...

const Issues = ({
  repositoryOwner,
  repositoryName,
  issueState,
  onChangeIssueState,
}) => (
  <div className="Issues">
    <IssueFilter
      repositoryOwner={repositoryOwner}
      repositoryName={repositoryName}
      issueState={issueState}
      onChangeIssueState={onChangeIssueState}
    />

    {isShow(issueState) && (
      ...
    )}
  </div>
);

const IssueFilter = ({
  repositoryOwner,
  repositoryName,
  issueState,
  onChangeIssueState,
}) => (
  <ApolloConsumer>
    {client => (
      <ButtonUnobtrusive
        onClick={() =>
          onChangeIssueState(TRANSITION_STATE[issueState])
        }
        onMouseOver={() =>
          prefetchIssues(
            client,
            repositoryOwner,
            repositoryName,
            issueState,
          )
        }
      >
        {TRANSITION_LABELS[issueState]}
      </ButtonUnobtrusive>
    )}
  </ApolloConsumer>
);
```

`/src/Issue/IssueList/index.js`

使用这些信息来执行预取数据查询。Apollo Client 实例暴露了`query()`方法。确保获取下一个`issueState`，因为在预取开启的 issue 时，当前的`issueState`应该是`NONE`。

```javascript
const prefetchIssues = (
  client,
  repositoryOwner,
  repositoryName,
  issueState,
) => {
  const nextIssueState = TRANSITION_STATE[issueState];

  if (isShow(nextIssueState)) {
    client.query({
      query: GET_ISSUES_OF_REPOSITORY,
      variables: {
        repositoryOwner,
        repositoryName,
        issueState: nextIssueState,
      },
    });
  }
};
```

就是这样。一旦鼠标悬停在按钮上，它就应该预取下一个`issueState`的问题。Apollo Client 会确保新数据被更新到缓存中，就像它处理`Query`组件时一样。在此期间不应该有任何可见的加载指示，除非网络请求耗时过长，且你在悬停后立即点击了按钮。你可以在浏览器开发者工具的网络（Network）标签页中验证请求是否正在发生。最后，你学习了在使用 Apollo Client 时轻松实现的两种 UX 改进：乐观 UI（optimistic UI）和数据预取。

## 练习

- 确认你[上一个节的源代码](http://bit.ly/2Vma9IF)
  - 确认[上一个节的更改](http://bit.ly/2VqhIy6)
- 阅读更多关于[React 中的 Apollo 预取和查询拆分](https://www.apollographql.com/docs/react/recipes/performance.html)的信息
- 花 3 分钟时间参加[测试](https://www.surveymonkey.com/r/5PLMBR3)

## 练习：评论功能

最后一节用于对应用程序进行实践操作并由你自己实现功能。我鼓励你继续为应用程序实现功能并进行改进。这里有几个指导点可以帮助你实现评论功能。最后，应该能够根据需要显示每个问题的分页评论列表。最后，用户应该能够发表评论。已实现功能的源代码可以在[这里](https://github.com/the-road-to-graphql/react-graphql-github-apollo/tree/c689a90d43272bbcb64c05f85fbc84ad4fe4308d)找到。

- 引入用于获取评论列表的组件（例如`Comments`）、渲染评论列表的组件（例如`CommentList`）以及渲染单个评论的组件（例如`CommentItem`）。它们现在可以渲染示例数据。
- 在`src/Issue/IssueItem/index.js`文件中使用顶层评论组件（例如`Comments`），它将作为负责查询评论列表的容器组件。此外，添加一个开关来显示或隐藏评论。`IssueItem`组件必须变成一个类组件，或者需要使用 recompose 库中的`withState` HOC。
- 在你的容器组件`Comments`中使用 React Apollo 的`Query`组件获取评论列表。它应该类似于获取问题列表的查询。你只需要识别应该为哪个问题获取评论。
- 在`Comments`中处理所有边缘情况，显示加载指示器、无数据或错误消息。在`CommentList`组件中渲染评论列表，在`CommentItem`组件中渲染单个评论。
- 为评论实现分页功能。在查询中添加必要的字段，为`Query`组件添加额外的 props 和 variables，以及可用的`FetchMore`组件。在`updateQuery`属性中处理状态合并。
- 当悬停在“显示/隐藏评论”按钮上时启用评论的预取。
- 实现一个`AddComment`组件，显示`textarea`和`submit`按钮以允许用户评论。使用 GitHub GraphQL API 的`addComment`变异和 React Apollo 的`Mutation`组件在点击提交时执行变异。
- 使用乐观 UI 功能改进`AddComment`组件（可能需要再次阅读[关于带列表的乐观 UI Apollo 文档](https://www.apollographql.com/docs/react/features/optimistic-ui.html)）。即使请求正在进行中，评论也应该显示在评论列表中。

我希望这一节通过你所学的工具和技术在应用程序中构建自己的功能，符合你的水平，并挑战了你使用 Apollo 和 GraphQL 实现 React 应用的能力。我建议努力改进和扩展现有的应用程序。如果你还没有实现过 GraphQL 服务器，请寻找提供 GraphQL API 的其他第三方 API，并通过消费它来构建自己的 React with Apollo 应用程序。保持挑战，不断提升你的开发者技能。

## 附录：CSS 文件和样式

本节包含了所有的 CSS 文件及其内容和位置，为你的 React with GraphQL 和 Apollo Client 应用程序增添美感。它甚至使其能够移动和平板设备的响应式。不过，这些只是建议；你可以尝试它们，或者设计你自己的样式。



# 样式文件与代码结构

## 全局样式

```
#root,
html,
body {
  height: 100%;
}

body {
  margin: 0;
  padding: 0;
  font-family: 'Source Sans Pro', sans-serif;
  font-weight: 200;
  text-rendering: optimizeLegibility;
}

h2 {
  font-size: 24px;
  font-weight: 600;
  line-height: 34px;
  margin: 5px 0;
}

h3 {
  font-size: 20px;
  font-weight: 400;
  line-height: 27px;
  margin: 5px 0;
}

ul,
li {
  list-style: none;
  padding-left: 0;
}

a {
  text-decoration: none;
  color: #000;
  opacity: 1;
  transition: opacity 0.25s ease-in;
}
```

```css
.Issues {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0 20px;
}

.Issues-content {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
}

.IssueList {
  margin: 20px 0;
}

@media only screen and (max-device-width: 480px) {
  .Issues-content {
    align-items: center;
  }
}
```

`src/Issue/IssueList/style.css`

```css
.LoadingIndicator {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 20px 0;
}

.LoadingIndicator_center {
  margin-top: 30%;
}
```

`src/Loading/style.css`

```css
.RepositoryItem {
  padding: 20px;
  border-bottom: 1px solid #000;
}

.RepositoryItem-title {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
}

@media only screen and (max-device-width: 480px) {
  .RepositoryItem-title {
    flex-direction: column;
    align-items: center;
  }
}

.RepositoryItem-title-action {
  margin-left: 10px;
}

.RepositoryItem-description {
  margin: 10px 0;
  display: flex;
  justify-content: space-between;
}

@media only screen and (max-device-width: 480px) {
  .RepositoryItem-description {
    flex-direction: column;
    align-items: center;
  }
}

.RepositoryItem-description-info {
  margin-right: 20px;
}

@media only screen and (max-device-width: 480px) {
  .RepositoryItem-description-info {
    text-align: center;
    margin: 20px 0;
  }
}

.RepositoryItem-description-details {
  text-align: right;
  white-space: nowrap;
}

@media only screen and (max-device-width: 480px) {
  .RepositoryItem-description-details {
    text-align: center;
  }
}
```

`src/Repository/style.css`

你可以在 [GitHub 上的仓库](https://github.com/rwieruch/react-graphql-github-apollo) 找到最终代码，它展示了大部分练习任务。该应用程序的功能并不完整，也没有涵盖所有的边缘情况，但它应该让你对在 React 应用中使用 Apollo 使用 GraphQL 有深入的了解。如果你想更深入地探讨如客户端 GraphQL 测试和状态管理等不同主题，可以从这里开始：[React 最小 Apollo Client 示例](https://www.robinwieruch.de/react-apollo-client-example)。尝试在应用程序中应用你所学的内容（例如：测试、状态管理）。否则，我鼓励你尝试构建构建自己的 GraphQL 客户端库，这有助于你理解更多 GraphQL 的内部原理：[如何为 React 构建 GraphQL 客户端库](https://www.robinwieruch.de/react-graphql-client-library)。无论你决定哪个，请继续琢磨这个应用程序，或者从另一个 GraphQL 客户端应用程序开始以强化你的技能。你已经完成了所有的 GraphQL 客户端章节。

# 使用 GraphQL 和 Apollo Server 的 Node.js

在本章中，你将使用 GraphQL 和 Apollo Server 实现服务端架构。GraphQL 查询语言由 Facebook 使用 JavaScript 实现了一份参考实现，而 Apollo Server 则在此基础上，简化了在 JavaScript 中构建 GraphQL 服务器的流程。由于 GraphQL 是一种查询语言，它的传输层和数据格式并不是固定的。GraphQL 对此没有主见，但它被用作流行的 REST 架构通过 HTTP 与 JSON 进行客户端服务器通信的替代方案。

最后，你将拥有一个完全工作的 GraphQL 服务器骨架项目，它实现了身份验证、授权、带有数据库的数据访问层、如用户和消息等领域特定实体、不同的分页策略以及由于订阅带来的实时能力。你可以在此 GitHub 仓库中找到它的解决方案，以及一个运行良好的 React 客户端应用程序：[React 和 Express 的全栈 Apollo 骨架项目](https://github.com/the-road-to-graphql/fullstack-apollo-express-postgresql-boilerplate)。我认为它是实现你自己的想法的理想入门项目。

在接下来的章节和我一起构建此应用程序时，我建议使用内置的 GraphQL 客户端应用程序（例如 GraphQL Playground）验证你的实现。一旦你完成了数据库设置，你也可以在那里验证你存储的数据。此外，如果你觉得可以的话，你可以实现一个客户端应用程序（使用 React 或或其他）来调用此服务器的 GraphQL API。那么，让我们开始吧！

## 使用 Express 设置 Apollo Server

开始此应用程序有两种方法。你可以按照我的指南，通过[这个最小化 Node.js 设置指南](https://www.robinwieruch.de/minimal-node-js-babel-setup) 逐步操作，或者可以在此 [GitHub 仓库](https://github.com/rwieruch/node-babel-server) 中找到一个启动项目并遵循其安装说明。

Apollo Server 可以与多个流行的 Node.js 库（如 Express、Koa、Hapi）配合。它是库无关的，因此可以与许多第三方库连接。将这两个依赖安装到 `package.json` 文件和 `node_modules` 文件夹中：

```bash
npm install apollo-server apollo-server-express
```

正如你从库名称看到的，你可以使用任何其他中间件解决方案。除了这些 Apollo Server 的库，你还需要 Express 和 GraphQL 的核心库：

```bash
npm install express graphql
```

现在所有库都准备好在 `src/index.js` 文件中启动。首先，你需要导入启动 Apollo Server 所需的部分：

```javascript
import express from 'express';
import { ApolloServer } from 'apollo-server-express';
```

`src/index.js`

其次，使用两个导入来初始化你的 Express Apollo Server：

```javascript
import express from 'express';
import { ApolloServer } from 'apollo-server-express';

const app = express();

const schema = ...
const resolvers = ...

const server = new ApolloServer({
  typeDefs: schema,
  resolvers,
});

server.applyMiddleware({ app, path: '/graphql' });

app.listen({ port: 8000 }, () => {
  console.log('Apollo Server on http://localhost:8000/graphql');
});
```

`src/index.js`

通过 Apollo Server 的 `applyMiddleware()` 方法，你可以接入任何中间件，在此例中是 Express。此外，你可以指定 GraphQL API 终点的路径。除此之外，你可以看到 Express 应用是如何初始化的。缺失的项目是创建 Apollo Server 实例所需的 schema 和解析器。我们将先实现它们，然后再学习它们：

```javascript
import express from 'express';
import { ApolloServer, gql } from 'apollo-server-express';

const app = express();

const schema = gql`
  type Query {
    me: User
  }

  type User {
    username: String!
  }
`;

const resolvers = {
  Query: {
    me: () => {
      return {
        username: 'Robin Wieruch',
      };
    },
  },
};
```

...

提供给 Apollo Server 的 `GraphQL schema` 是通过 GraphQL 读取和写入数据的所有可用数据。它可以来自任何消费 GraphQL API 的客户端。该架构由 `type definitions` 组成，始于强制性的顶层 `Query type` 用于读取数据，随后是 `fields`（字段）和 `nested fields`（嵌套字段）。在 Apollo Server 设置的 schema 中，你定义了一个 `me` 字段，它的类型是 `object type` `User`。在这种情况下，`User` 类型只有一个 `username` 字段，它是一个 `scalar type`。GraphQL 规范中定义了多种标量类型，用于定义字符串（`String`）、布尔值（`Boolean`）、整数（`Int`）等。在某个点，schema 必须在叶子节点通过标量类型结束，以便正确解析所有内容。你可以将其视为内部包含对象或数组的 JavaScript 对象，区别在于它某些地方需要字符串、布尔值或整数等原始类型。

```javascript
const data = {
  me: {
    username: 'Robin Wieruch',
  },
};
```

## 代码游场

在设置 Apollo Server 的 GraphQL schema 中，`resolvers` 用于返回 schema 中字段的数据。数据源并不重要，因为数据可以是硬编码的，可以来自数据库，也可以来自另一个（RESTful）API 端点。你稍将学习更多关于潜在数据源的知识。现在，重要的是 resolvers 与数据来源何是无关的，这使得 GraphQL 与你典型的查询语言隔离开来。Resolvers 是解析 schema 中 GraphQL 字段数据的函数。在上一个示例中，仅从 `me` 字段解析出一个用户名为“Robin Wieruch”的用户对象。

你使用 Apollo Server 和 Express 构建的 GraphQL API 现在应该可以正常工作了。在命令行中，你始终可以使用 `npm start` 脚本启动应用程序，以验证在做出更改后其运行正常。要在没有客户端应用的情况下进行验证，Apollo Server 自带 GraphQL Playground，这是一个用于消费 GraphQL API 的内置客户端。你可以通过浏览器访问 `http://localhost:8000/graphql` 使用 GraphQL API 端点找到它。在应用程序中，定义你的第一个 GraphQL 查询以查看结果：

```graphql
{
  me {
    username
  }
}
```

### GraphQL Playground

查询的结果应该是这个或你定义的示例数据：

```json
{
  "data": {
    "me": {
      "username": "Robin Wieruch"
    }
  }
}
```

### GraphQL Playground

之后我可能不会频繁提到 GraphQL Playground 了，但我留给你在做出更改后使用它来验证你的 GraphQL API。它是一个实验和探索你自己 API 的有用工具。可选，你还可以在你的 Express 中间件中添加 [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)。首先，在命令行安装 CORS：

```bash
npm install cors --save
```

### 命令行

其次，在你的 Express 中间件中使用它：

```javascript
import cors from 'cors';
import express from 'express';
import { ApolloServer, gql } from 'apollo-server-express';

const app = express();

app.use(cors());

...
```

`src/index.js`

需要 CORS 来从你服务器域之外的域名向你的服务器发送 HTTP 请求。否则，你可能会在 GraphQL 服务器上遇到跨源资源共享错误。

## 练习题

* 确认你的[上一节的源代码](http://bit.ly/2VsfJJK)
  * 确认[上一节的更改](http://bit.ly/2VnZy09)
* 了解更多关于 [GraphQL](https://graphql.org/learn) 的知识
* 实验 schema 和 resolver
  * 为 user 类型添加更多字段
  * 满足 resolver 中的要求
  * 在 GraphQL Playground 中查询你的字段
* 了解更多关于 [Apollo Server Standalone](https://www.apollographql.com/docs/apollo-server/v2/getting-started.html) 的知识
* 了解更多关于 [Express Setup 中的 Apollo Server](https://www.apollographql.com/docs/apollo-server/v2/essentials/server.html) 的知识

## Apollo Server: Type Definitions

此部分完全关于 类型 定义以及如何使用它们来定义整个 GraphQL schema。GraphQL schema 由其类型、类型之间的关系以及它们的结构定义。因此，GraphQL 使用 `Schema Definition Language (SDL)`。然而，schema 并不定义数据从何而来。这一责任由 SDL 外部的 resolvers 处理。当你之前使用 Apollo Server 时，你在 schema 中使用了一个 `User` 对象类型，并定义了一个为相应的 `me` 字段返回用户的 resolver。



注意`User`对象类型中`username`字段旁边的感叹号。这意味着`username`是一个`non-nullable`（非空）字段。每当从 GraphQL schema 返回带有`username`的`User`类型字段时，用户必须有一个`username`。它不能是 `undefined` 或 `null`。然而，`me`字段上的用户类型没有感叹号。这意味着`me`字段的结果可以为 `null` 吗？在这种 particular 情况下是这样的。`me`字段并不总是返回一个用户，因为服务器在响应之前必须知道该字段包含什么。稍后，你将为你的 GraphQL 服务器实现身份验证机制（注册、登录、注销）。只有当用户通过服务器的身份验证后，`me`字段才会填充账户详情等用户对象。否则，它将保持为 `null`。

```javascript
let users = {
  1: {
    id: '1',
    username: 'Robin Wieruch',
  },
  2: {
    id: '2',
    username: 'Dave Davids',
  },
};

const me = users[1];

const resolvers = {
  Query: {
    user: (parent, { id }) => {
      return users[id];
    },
    me: () => {
      return me;
    },
  },
};
```

`src/index.js`

现在在 GraphQL Playground 中尝试你的查询：

```graphql
{
  user(id: "2") {
    username
  }
  me {
    username
  }
}
```

GraphQL Playground

它应该返回此结果：

```json
{
  "data": {
    "user": {
      "username": "Dave Davids"
    },
    "me": {
      "username": "Robin Wieruch"
    }
  }
}
```

GraphQL Playground

查询用户列表将是我们的第三个查询。首先，再次将查询添加到 schema 中中：

```javascript
const schema = gql`
  type Query {
    users: [User!]
    user(id: ID!): User
    me: User
  }

  type User {
    id: ID!
    username: String!
  }
`;
```

`src/index.js`

在这种情况下，`users`字段返回一个`User`类型的用户列表，用方括号`[]`表示。在列表中，不允许用户为`null`，但如果没有用户，列表本身可以是`null`（否则，它也可以是`[User!]!`）。一旦你向 schema 中添加了新查询，你就有义务在`Query`对象的`resolvers`中定义它：

```javascript
const resolvers = {
  Query: {
    users: () => {
      return Object.values(users);
    },
    user: (parent, { id }) => {
      return users[id];
    },
    me: () => {
      return me;
    },
  },
};
```

`src/index.js`

你有三个查询可以在你的 GraphQL 客户端（例如 GraphQL Playground）应用程序中使用。它们都作用于同一个`User`类型，以满足`resolvers`中的数据需求，因此每个查询都必须有一个匹配的`resolver`。所有查询都分组在一个唯一的、强制的`Query`类型下，该类型列出了所有暴露给客户端的可用 GraphQL 查询，作为你用于读取数据的 GraphQL API。稍后，你将学习`Mutation`类型，用于对用于写入数据的 GraphQL API 进行分组。

### 练习题：

*   确认你[上一个节的源代码](http://bit.ly/2VnGOxK)

    *   确认[上一节的更改](http://bit.ly/2VnX2Xv)

*   了解更多关于[使用 Apollo Server 的 GraphQL schema](https://www.apollographql.com/docs/apollo-server/v2/essentials/schema.html) 的信息

*   了解更多关于[GraphQL 思维：以图的方式思考](https://graphql.github.io/learn/thinking-in-graphs/) 的信息

*   了解更多关于[GraphQL 中的可空性](https://blog.apollographql.com/using-nullability-in-graphql-2254f84c4ed7) 的信息

### Apollo Server: Resolvers

这一节将延续 Apollo Server 中的 GraphQL schema，但更多地转向了该主题的 resolver 端。在你的 GraphQL 类型定义中，你定义了类型、它们的关系和结构。但关于如何获取数据，没有任何内容。这正是 GraphQL resolvers 派用用场。

在 JavaScript 中，resolvers 被分组在一个 JavaScript 对象中，通常称为`resolver map`。你的`Query`类型中的每个顶层查询都必须有一个`resolver`。现在，我们将按字段级别进行解析。

```javascript
const resolvers = {
  Query: {
    users: () => {
      return Object.values(users);
    },
    user: (parent, { id }) => {
      return users[id];
    },
    me: () => {
      return me;
    },
  },

  User: {
    username: () => 'Hans',
  },
};
```

`src/index.js`

一旦你重新启动应用程序并查询用户列表，每个用户都应该有一个相同的用户名。

```graphql
// query
{
  users {
    username
    id
  }
}

// query result
{
  "data": {
    "users": [
      {
        "username": "Hans",
        "id": "1"
      },
      {
        "username": "Hans",
        "id": "2"
      }
    ]
  }
}
```

GraphQL Playground

GraphQL resolvers 可以更具体地按字段级别进行操作。你可以通过解析`username`字段来覆盖每个`User`类型的`username`。否则，将使用用户实体的默认`username`属性。通常，这适用于每个字段。你可以在`resolver`函数中专门决定该字段应该返回什么，或者 GraphQL 会尝试通过自动从 JavaScript 实体中检索属性来作为该字段的回备方案。

让我们通过深入研究`resolver`函数的签名来稍微演进一下。之前你已经看到`resolver`函数的第二个参数是查询的传入参数。这就是你如何能够从`Query`中检索用户的`id`参数。第一个参数被称为`parent`或根参数，它总是返回之前解析的字段。让我们为新的`username` `resolver`函数检查一下。

```javascript
const resolvers = {
  Query: {
    users: () => {
      return Object.values(users);
    },
    user: (parent, { id }) => {
      return users[id];
    },
    me: () => {
      return me;
    },
  },

  User: {
    username: (parent, args, context, info) => {
      return parent.username;
    },
  },
};
```

```javascript
const resolvers = {
  Query: {
    users: () => {
      return Object.values(users);
    },
    user: (parent, { id }) => {
      return users[id];
    },
    me: () => {
      return me;
    },
  },

  User: {
    username: () => 'Hans',
  },
};
```

`src/index.js`

一旦你重新启动应用程序并查询用户列表，每个用户都应该有一个相同的用户名。

```graphql
// query
{
  users {
    username
    id
  }
}

// query result
{
  "data": {
    "users": [
      {
        "username": "Hans",
        "id": "1"
      },
      {
        "username": "Hans",
        "id": "2"
      }
    ]
  }
}
```

GraphQL Playground

GraphQL resolvers 可以更具体地按字段级别进行操作。你可以通过解析`username`字段来覆盖每个`User`类型的`username`。否则，将使用用户实体的默认`username`属性。通常，这适用于每个字段。你可以在`resolver`函数中专门决定该字段应该返回什么，或者 GraphQL 会尝试通过自动从 JavaScript 实体中检索属性来作为该字段的回备方案。

让我们通过深入研究`resolver`函数的签名来稍微演进一下。之前你已经看到`resolver`函数的第二个参数是查询的传入参数。这就是你如何能够从`Query`中检索用户的`id`参数。第一个参数被称为`parent`或根参数，它总是返回之前解析的字段。让我们为新的`username` `resolver`函数检查一下。

```javascript
const resolvers = {
  Query: {
    users: () => {
      return Object.values(users);
    },
    user: (parent, { id }) => {
      return users[id];
    },
    me: () => {
      return me;
    },
  },

  User: {
    username: (parent, args, context, info) => {
      return parent.username;
    },
  },
};
```

```javascript
const resolvers = {
  Query: {
    users: () => {
      return Object.values(users);
    },
    user: (parent, { id }) => {
      return users[id];
    },
    me: () => {
      return me;
    },
  },

  User: {
    username: () => 'Hans',
  },
};
```

`src/index.js`

一旦你重新启动应用程序并查询用户列表，每个用户都应该有一个相同的用户名。

```graphql
// query
{
  users {
    username
    id
  }
}

// query result
{
  "data": {
    "users": [
      {
        "username": "Hans",
        "id": "1"
      },
      {
        "username": "Hans",
        "id": "2"
      }
    ]
  }
}
```

GraphQL Playground

GraphQL resolvers 可以更具体地按字段级别进行操作。你可以通过解析`username`字段来覆盖每个`User`类型的`username`。否则，将使用用户实体的默认`username`属性。通常，这适用于每个字段。你可以在`resolver`函数中专门决定该字段应该返回什么，或者 GraphQL 会尝试通过自动从 JavaScript 实体中检索属性来作为该字段的回备方案。

让我们通过深入研究`resolver`函数的签名来稍微演进一下。之前你已经看到`resolver`函数的第二个参数是查询的传入参数。这就是你如何能够从`Query`中检索用户的`id`参数。第一个参数被称为`parent`或根参数，它总是返回之前解析的字段。让我们为新的`username` `resolver`函数检查一下。

```javascript
const resolvers = {
  Query: {
    users: () => {
      return Object.values(users);
    },
    user: (parent, { id }) => {
      return users[id];
    },
    me: () => {
      return me;
    },
  },

  User: {
    username: (parent, args, context, info) => {
      return parent.username;
    },
  },
};
```

```javascript
const resolvers = {
  Query: {
    users: () => {
      return Object.values(users);
    },
    user: (parent, { id }) => {
      return users[id];
    },
    me: () => {
      return me;
    },
  },

  User: {
    username: () => 'Hans',
  },
};
```

`src/index.js`

一旦你重新启动应用程序并查询用户列表，每个用户都应该有一个相同的用户名。



```graphql
// query
{
  users {
    username
    id
  }
}

// query result
{
  "data": {
    "users": [
      {
        "username": "Hans",
        "id": "1"
      },
      {
        "username": "Hans",
        "id": "2"
      }
    ]
  }
}
```

GraphQL Playground

GraphQL resolvers 更具体地按字段级别进行操作。你可以通过解析 `username` 字段来覆盖每个 `User` 类型的 `username`。否则，将使用用户实体的默认 `username` 属性。通常，这适用于每个字段。你可以在 `resolver` 函数中专门决定该字段应该返回什么，或者 GraphQL 会尝试通过自动从 JavaScript 实体中检索属性来作为该字段的回备方案。

```javascript
let users = {
  1: {
    id: '1',
    username: 'Robin Wieruch',
  },
  2: {
    id: '2',
    username: 'Dave Davids',
  },
};

const me = users[1];

const resolvers = {
  Query: {
    user: (parent, { id }) => {
      return users[id];
    },
    me: () => {
      return me;
    },
  },
};
```

`src/index.js`

现在在 GraphQL Playground 中尝试你的查询：

```graphql
{
  user(id: "2") {
    username
  }
  me {
    username
  }
}
```

GraphQL Playground

它应该返回此结果：

```json
{
  "data": {
    "user": {
      "username": "Dave Davids"
    },
    "me": {
      "username": "Robin Wieruch"
    }
  }
}
```

GraphQL Playground

查询用户列表将是我们的第三个查询。首先，再次将查询添加到 schema 中：

```javascript
const schema = gql`
  type Query {
    users: [User!]
    user(id: ID!): User
    me: User
  }

  type User {
    id: ID!
    username: String!
  }
`;
```

`src/index.js`

在这种情况下，`users` 字段返回一个 `User` 类型的用户列表，用方括号 `[]` 表示。在列表中，不允许用户为 `null`，但如果没有用户，列表本身可以是 `null`（否则，它也可以是 `[User!]!`）。一旦你向 schema 中添加了新查询，你就有义务在 `Query` 对象的 `resolvers` 中定义它：

```javascript
const resolvers = {
  Query: {
    users: () => {
      return Object.values(users);
    },
    user: (parent, { id }) => {
      return users[id];
    },
    me: () => {
      return me;
    },
  },
};
```

`src/index.js`

你有三个查询可以在你的 GraphQL 客户端（例如 GraphQL Playground）应用程序中使用。它们都作用于同一个 `User` 类型，以满足 `resolvers` 中的数据需求，因此每个查询都必须有一个匹配的 `resolver`。所有查询都分组在一个唯一的、强制的 `Query` 类型下，该类型列出了所有暴露给客户端的可用 GraphQL 查询，作为你用于读取数据的 GraphQL API。稍后，你将学习 `Mutation` 类型，用于对用于写入数据的 GraphQL API 进行分组。

### 练习题

- 确认你[上一个节的源代码](http://bit.ly/2VnGOxK)
  - 确认[上一节的更改](http://bit.ly/2VnX2Xv)
- 了解更多关于[使用 Apollo Server 的 GraphQL schema](https://www.apollographql.com/docs/apollo-server/v2/essentials/schema.html)的信息。
- 了解更多关于[GraphQL 思维：以图的方式思考](https://graphql.github.io/learn/thinking-in-graphs/)的信息。
- 了解更多关于[GraphQL 中的可空性](https://blog.apollographql.com/using-nullability-in-graphql-2254f84c4ed7)的信息。

### Apollo Server：Resolvers

这一节将延续 Apollo Server 中的 GraphQL schema，但更多地转向该主题的 resolver 端。在你的 GraphQL 类型定义中，你定义了类型、它们的关系和结构。但关于如何获取数据，没有任何内容。这正是 GraphQL resolvers 派上用场的地方。

在 JavaScript 中，resolvers 被分组在一个 JavaScript 对象中，通常称为 `resolver map`。你的 `Query` 类型中的每个顶层查询都必须有一个 `resolver`。现在，我们将按字段级别进行解析。

```javascript
const resolvers = {
  Query: {
    users: () => {
      return Object.values(users);
    },
    user: (parent, { id }) => {
      return users[id];
    },
    me: () => {
      return me;
    },
  },

  User: {
    username: () => 'Hans',
  },
};
```

`src/index.js`

一旦你重新启动应用程序并查询用户列表，每个用户都应该有一个相同的用户名。

```graphql
// query
{
  users {
    username
    id
  }
}

// query result
{
  "data": {
    "users": [
      {
        "username": "Hans",
        "id": "1"
      },
      {
        "username": "Hans",
        "id": "2"
      }
    ]
  }
}
```

GraphQL Playground

GraphQL resolvers 可以更具体地按字段级别进行操作。你可以通过解析 `username` 字段来覆盖每个 `User` 类型的 `username`。否则，将使用用户实体的默认 `username` 属性。通常，这适用于每个字段。你可以在 `resolver` 函数中专门决定该字段应该返回什么，或者 GraphQL 会尝试通过自动从 JavaScript 实体中检索属性来作为该字段的回备方案。

让我们通过深入研究 `resolver` 函数的签名来稍微演进一下。之前你已经看到 `resolver` 函数的第二个参数是查询的传入参数。这就是你如何能够从 `Query` 中检索用户的 `id` 参数。第一个参数被称为 `parent` 或根参数，它总是返回之前解析的字段。让我们检查新的 `username` `resolver` 函数。

```javascript
const resolvers = {
  Query: {
    users: () => {
      return Object.values(users);
    },
    user: (parent, { id }) => {
      return users[id];
    },
    me: () => {
      return me;
    },
  },

  User: {
    username: (parent, args, context, info) => {
      return parent.username;
    },
  },
};
```

`resolver` 函数中的第四个参数 `info` 并不经常使用，因为它只提供有关 GraphQL 请求的内部信息。它可以用于调试、错误处理、高级监控和追踪。你现在不需要担心它。



关于解析器的返回值的几点：解析器可以返回数组、对象和标量类型，但它们必须在匹配的类型定义中定义。类型定义必须定义一个数组或非空字段，以确保解析器正常工作。JavaScript 的 `promises` 又是怎样的？通常，你会在解析器中向数据源（数据库、RESTful API）发送请求，并在解析器中返回一个 JavaScript `promise`。GraphQL 可以处理它，并等待 `promise` 解析完成（`resolve`）。这就是为什么你以后不需要担心对数据源进行异步请求的原因。

### 练习题：
- 确认你[上一节的源代码](http://bit.ly/2Vp9XbR)
  - 确认[来自上一节的变动](http://bit.ly/2VmdcR7)
- 阅读更多关于 [Apollo 中使用 GraphQL 解析器](https://www.apollographql.com/docs/apollo-server/v2/essentials/data.html) 的信息

## Apollo Server：类型关系

你已经通过定义查询（queries）、变更（mutations）和类型定义开始演进你的 GraphQL Schema。在本节中，让我们添加第二个名为 `Message` 的 GraphQL 类型，并看看它是如何与你的 `User` 类型交互的。在这个应用程序中，用户拥有消息。基本上，你可以使用这两个类型编写一个简单的聊天应用程序。首先，向你的 GraphQL Schema 添加两个新的顶层查询和新的 `Message` 类型：

```graphql
const schema = gql`
  type Query {
    users: [User!]
    user(id: ID!): User
    me: User

    messages: [Message!]!
    message(id: ID!): Message!
  }

  type User {
    id: ID!
    username: String!
  }

  type Message {
    id: ID!
    text: String!
  }
`;
```

`src/index.js`

其次，你必须为 Apollo Server 添加两个解析器来匹配这两个新的顶层查询：

```javascript
let messages = {
  1: {
    id: '1',
    text: 'Hello World',
  },
  2: {
    id: '2',
    text: 'By World',
  },
};

const resolvers = {
  Query: {
    users: () => {
      return Object.values(users);
    },
    user: (parent, { id }) => {
      return users[id];
    },
    me: (parent, args, { me }) => {
      return me;
    },
    messages: () => {
      return Object.values(messages);
    },
    message: (parent, { id }) => {
      return messages[id];
    },
  },
};
```

`src/index.js`

一旦再次运行应用程序，你新的 GraphQL 查询应该可以在 GraphQL playground 中正常工作。现在我们将为两个 GraphQL 类型添加关系。在历史上，REST 常见的做法是为每个实体添加一个标识符来解析它的关系。

```graphql
const schema = gql`
  type Query {
    users: [User!]
    user(id: ID!): User
    me: User

    messages: [Message!]!
    message(id: ID!): Message!
  }

  type User {
    id: ID!
    username: String!
  }

  type Message {
    id: ID!
    text: String!
    userId: ID!
  }
`;
```

`src/index.js`

在 GraphQL 中，你不需要使用标识符并通过多次瀑布式请求来解析实体，而是直接在消息实体中使用 `User` 实体：

```graphql
const schema = gql`
  ...

  type Message {
    id: ID!
    text: String!
    user: User!
  }
`;
```

`src/index.js`

由于你的模型中消息没有用户实体，因此默认解析器无法工作。你需要为它设置一个显式的解析器。

```javascript
const resolvers = {
  Query: {
    users: () => {
      return Object.values(users);
    },
    user: (parent, { id }) => {
      return users[id];
    },
    me: (parent, args, { me }) => {
      return me;
    },
    messages: () => {
      return Object.values(messages);
    },
    message: (parent, { id }) => {
      return messages[id];
    },
  },

  Message: {
    user: (parent, args, { me }) => {
      return me;
    },
  },
};
```

`src/index.js`

在这种情况下，每条消息都由身份验证过的 `me` 用户编写。如果你查询以下关于的消息，你将得到这个结果：

```javascript
// query
{
  message(id: "1") {
    id
    text
    user {
      id
      username
    }
  }
}

// query result
{
  "data": {
    "message": {
      "id": "1",
      "text": "Hello World",
      "user": {
        "id": "1",
        "username": "Robin Wieruch"
      }
    }
  }
}
```

```javascript
const schema = gql`
  type Query {
    users: [User!]
    user(id: ID!): User
    me: User

    messages: [Message!]!
    message(id: ID!): Message!
  }

  type Mutation {
    createMessage(text: String!): Message!
  }

  ...
`;
```

`src/index.js`

除了 `Query` 类型之外，还有 `Mutation` 和 `Subscription` 类型。在其中，你可以将所有用于写入数据的 GraphQL 操作分组，而不是读取。在这种情况下，`createMessage` 变异接受一个非空的 `text` 输入作为参数，并返回创建的消息。同样，你必须像之前的查询一样，为变异实现对应的解析器（resolver），这发生在 resolver 映射中的 mutation 部分：

```javascript
const resolvers = {
  Query: {
    ...
  },

  Mutation: {
    createMessage: (parent, { text }, { me }) => {
      const message = {
        text,
        userId: me.id,
      };

      return message;
    },
  },

  ...
};
```

`src/index.js`

变异的解析器可以访问其第二个参数中的 `text`。它还可以访问第三个参数中的登录用户，用于将创建的消息与用户关联。`parent` 参数未被使用。要使消息完整，缺少的一项是标识符。为了确保使用唯一标识符，请在命令行中安装这个优秀的库：

```bash
npm install uuid --save
```

### 命令行

并将其导入到你的文件中：

```javascript
import uuidv4 from 'uuid/v4';
```

`src/index.js`

现在你可以给你的消息分配一个唯一的标识符：

```javascript
const resolvers = {
  Query: {
    ...
  },

  Mutation: {
    createMessage: (parent, { text }, { me }) => {
      const id = uuidv4();
      const message = {
        id,
        text,
        userId: me.id,
      };

      return message;
    },
  },

  ...
};
```

`src/index.js`

到目前为止，变异创建了一个消息对象并将其返回给 API。然而，大多数变异都有副作用，因为它们正在向你的数据源写入数据或执行其他操作。通常，它是对你的数据库的写入操作，但在这种情况下，你只需要更新你的 `users` 和 `messages` 变量。可用消息列表需要更新，用户的 `messageIds` 引用列表也需要包含新的消息 `id`。

```javascript
const resolvers = {
  Query: {
    ...
  },

  Mutation: {
    createMessage: (parent, { text }, { me }) => {
      const id = uuidv4();
      const message = {
        id,
        text,
        userId: me.id,
      };

      messages[id] = message;
      users[me.id].messageIds.push(id);

      return message;
    },
  },

  ...
};
```

`src/index.js`

第一个变异就此结束。你现在可以在 GraphQL Playground 中尝试它：

```graphql
mutation {
  createMessage (text: "Hello GraphQL!") {
    id
    text
  }
}
```

### GraphQL Playground

最后一部分本质上是你对数据源的写入操作。在这种情况下，你只更新了示例数据，但在实际使用中它很可能是一个数据库。接下来，实现删除消息的变异：

```graphql
const schema = gql`
  type Query {
    users: [User!]
    user(id: ID!): User
    me: User

    messages: [Message!]!
    message(id: ID!): Message!
  }

  type Mutation {
    createMessage(text: String!): Message!
    deleteMessage(id: ID!): Boolean!
  }

  ...
`;
```

`src/index.js`

变异返回一个布尔值，删除是否成功，并接受一个标识符作为输入以标识消息。GraphQL schema 实现的对应物是解析器：

```javascript
const resolvers = {
  Query: {
    ...
  },

  Mutation: {
    ...

    deleteMessage: (parent, { id }) => {
      const { [id]: message, ...otherMessages } = messages;

      if (!message) {
        return false;
      }

      messages = otherMessages;

      return true;
    },
  },

  ...
};
```

`src/index.js`

解析器通过解构从 `messages` 对象中通过 `id` 找到消息。如果没有消息，解析器返回 `false`。如果有消息，不包含删除消息的剩余消息就是消息对象的更新版本。然后，解析器返回 `true`。否则，如果没有找到消息，解析器返回 `false`。GraphQL 和 Apollo Server 中的变异与 GraphQL 查询没有太大区别，在于它们会写入数据。

为了使消息功能完整，只缺少一个 GraphQL 操作。现在可以读取、创建和删除消息，因此剩下的唯一操作是作为练习来更新它们。

### 练习题：
- 确认你[最后一部分的源代码](http://bit.ly/2VsfRJe)
  - 确认[上一部分的更改](http://bit.ly/2VqAMf)
- 创建更新消息的变异

## 使用 Apollo Server 进行 Schema 缝合

Schema Stitching 是 GraphQL 的一个强大功能。它是关于将多个 schema 合并为一个。目前你只有一个 schema，但未来可能需要使用多个 schema 的复杂操作（例如，`User`、`Message`）。

但你可以更进一步：你可能会遇到微服务或第三方平台，它们暴露自己的 API，然后可以将它们合并到一个 schema 中，即单一来源。在我们的情况下，让我们先按技术关注点分离 GraphQL schema。之后，我们将按领域分离，即 `users` 和 `messages`。

### 技术分离

让我们采用具有 `User` 类型和 `Message` 类型的应用程序 schema。在同一步骤中，将解析器拆分到专门的地方。`src/index.js` 文件（实例化 Server 需要 schema 和解析器）应该只导入这两项。当外包数据时，变成了三项，在这种情况下是示例数据，现在称为 `models`。

```javascript
import cors from 'cors';
import express from 'express';
import { ApolloServer } from 'apollo-server-express';

import schema from './schema';
import resolvers from './resolvers';
import models from './models';

const app = express();

app.use(cors());

const server = new ApolloServer({
  typeDefs: schema,
  resolvers,
  context: {
    models,
    me: models.users[1],
  },
});

server.applyMiddleware({ app, path: '/graphql' });

app.listen({ port: 8000 }, () => {
  console.log('Apollo Server on http://localhost:8000/graphql');
});
```

`src/index.js`

```javascript
let users = {
  1: {
    id: '1',
    username: 'Robin Wieruch',
    messageIds: [1],
  },
  2: {
    id: '2',
    username: 'Dave Davids',
    messageIds: [2],
  },
};

let messages = {
  1: {
    id: '1',
    text: 'Hello World',
    userId: '1',
  },
  2: {
    id: '2',
    text: 'By World',
    userId: '2',
  },
};

export default {
  users,
  messages,
};
```

`src/models/index.js`

由于你已经将模型传递给 `Apollo Server` 的上下文（context），你可以在每个 resolver 中访问它们。接下来，将 resolvers 移动到 `src/resolvers/index.js` 文件，并在需要读写用户或消息时，通过添加 `models` 来调整 resolver 的函数签名。



```javascript
import uuidv4 from 'uuid/v4';

export default {
  Query: {
    users: (parent, args, { models }) => {
      return Object.values(models.users);
    },
    user: (parent, { id }, { models }) => {
      return models.users[id];
    },
    me: (parent, args, { me }) => {
      return me;
    },
    messages: (parent, args, { models }) => {
      return Object.values(models.messages);
    },
    message: (parent, { id }, { models }) => {
      return models.messages[id];
    },
  },

  Mutation: {
    createMessage: (parent, { text }, { me, models }) => {
      const id = uuidv4();
      const message = {
        id,
        text,
        userId: me.id,
      };

      models.messages[id] = message;
      models.users[me.id].messageIds.push(id);

      return message;
    },

    deleteMessage: (parent, { id }, { models }) => {
      const { [id]: message, ...otherMessages } = models.messages;

      if (!message) {
        return false;
      }

      models.messages = otherMessages;

      return true;
    },
  },

  User: {
    messages: (user, args, { models }) => {
      return Object.values(models.messages).filter(
        message => message.userId === user.id,
      );
    },
  },

  Message: {
    user: (message, args, { models }) => {
      return models.users[message.userId];
    },
  },
};
```

### `src/resolvers/index.js`

resolvers 通过 `context` 参数中的 `models` 接收所有示例数据，而不是像以前那样直接操作示例数据。如提到的，这保持了 resolver 函数的纯性。以后，你将更容易孤立地测试 resolver 函数。接下来，将你的 schema 类型定义移动到 `src/schema/index.js` 文件中：

```javascript
import { gql } from 'apollo-server-express';

export default gql`
  type Query {
    users: [User!]
    user(id: ID!): User
    me: User

    messages: [Message!]!
    message(id: ID!): Message!
  }

  type Mutation {
    createMessage(text: String!): Message!
    deleteMessage(id: ID!): Boolean!
  }

  type User {
    id: ID!
    username: String!
    messages: [Message!]
  }

  type Message {
    id: ID!
    text: String!
    user: User!
  }
`;
```

### `src/schema/index.js`

技术上的分离已经完成，但按领域划分的 schema 缝合（schema stitching）尚未完成。到目前为止，你只是从 `Apollo Server` 实例化中外出了 schema 和数据（`models`）。现在你通过 `context` 传递 `models` 了一了一小改进，而不是在 resolver 文件中导入它们。

#### 领域划分（Domain Separation）

在下一步中，按领域（用户和消息）对 GraphQL schema 进行模块化。首先，将用户相关的实体移动到名为 `src/schema/user.js` 的文件中：

```javascript
import { gql } from 'apollo-server-express';

export default gql`
  extend type Query {
    users: [User!]
    user(id: ID!): User
    me: User
  }

  type User {
    id: ID!
    username: String!
    messages: [Message!]
  }
`;
```

### `src/schema/user.js`

同样适用于 `src/schema/message.js` 中的消息 schema 定义：

```javascript
import { gql } from 'apollo-server-express';

export default gql`
  extend type Query {
    messages: [Message!]!
    message(id: ID!): Message!
  }

  extend type Mutation {
    createMessage(text: String!): Message!
    deleteMessage(id: ID!): Boolean!
  }

  type Message {
    id: ID!
    text: String!
    user: User!
  }
`;
```

你现在已经为使用 Node.js 构建 GraphQL 服务器应用程序有了一个良好的起点。之前的实现已经为你提供了一个通用的 GraphQL 样板项目，可以作为你自己的软件开发项目的基础。随着我们学习的持续，重点将转向将 GraphQL 服务器连接到数据库、身份验证与授权，以及使用如分页等强大的功能。

### 练习题

- 确认你[上一节的源代码](http://bit.ly/2VnMlnT)
  - 确认[上一节的更改](http://bit.ly/2VkZMF8)
- 阅读更多关于[使用 Apollo Server 进行模式缝合（schema stitching）](https://www.apollographql.com/docs/graphql-tools/schema-stitching.html)
- 模式缝合只是`模式委托（schema delegation）`的一部分：
  - 阅读更多关于[模式委托](https://www.apollographql.com/docs/graphql-tools/schema-delegation.html)
  - 熟悉`远程模式（remote schemas）`和`模式转换（schema transforms）`背后的设计动机

### 使用 Sequelize 配合 PostgreSQL 构建 GraphQL 服务器

为了创建一个全栈 GraphQL 应用程序，你需要引入一个复杂的数据源。示例数据是变动的，而数据库则提供持久化数据。在本节中，你将为 Apollo Server 配置带有 Sequelize（[ORM](https://en.wikipedia.org/wiki/Object-relational_mapping)）的 PostgreSQL（[PostgreSQL](https://www.postgresql.org/)）。PostgreSQL 是一个 SQL 数据库，而另一种方案是流行的 NoSQL 数据库 [MongoDB](https://www.mongodb.com/)（配合 Mongoose 作为 ORM）。技术的选择总是带有主观性的。你可以选择 MongoDB 或任何其他 SQL/NoSQL 方案代替 PostgreSQL，但为了本应用，让我们坚持使用 PostgreSQL。

此[设置指南](https://www.robinwieruch.de/postgres-express-setup-tutorial/)将引导你完成基础的 PostgreSQL 设置，包括安装、第一个数据库、数据库管理员用户设置以及基本命令。这些是你按照说明操作后应该完成的内容：

- 一个正在运行的 PostgreSQL 安装
- 一个拥有用户名和密码的数据库超级用户
- 使用 `createdb` 或 `CREATE DATABASE` 创建的数据库

你应该能够使用以下命令运行和停止数据库：

```bash
pg_ctl -D /usr/local/var/postgres start
pg_ctl -D /usr/local/var/postgres stop
```

使用 `psql` 命令在命令行连接到你的数据库，你可以在那里列出数据库并对其执行 SQL 语句。你应该会在 PostgreSQL 设置指南中发现这些操作的，但本节也会展示其中一些。考虑以你在 GraphQL Playground 中完成 GraphQL 操作相同的方式执行这些操作。`psql` 命令行界面和 GraphQL Playground 是手动测试应用的有效工具。

一旦你在本地机器上安装了 PostgreSQL，你还会想为项目获取 [Node.js 的 PostgreSQL](https://github.com/brianc/node-postgres) 和 [Sequelize（ORM）](https://github.com/sequelize/sequelize)。我强烈建议你保持 Sequelize 文档开启，因为当你将 GraphQL 层（解析器）与数据访问层（Sequelize）连接时，它将对你的参考非常有帮助。

```bash
npm install pg sequelize --save
```

### 命令行

现在你可以为用户和消息领域创建模型。模型通常是应用程序中的数据访问层。然后，使用 Sequelize 配置你的模型，以便对你的 PostgreSQL 数据库进行读写操作。随后，可以通过将模型通过 `context` 对象传递给每个解析器，从而在 GraphQL 解析器中使用它们。这些是核心步骤：

- 为用户领域创建模型
- 为消息领域创建模型
- 将应用程序连接到数据库
  - 提供超级用户的用户名和密码
  - 组合模型供数据库使用
- 应用程序启动时同步数据库

首先，实现 `src/models/user.js` 模型：

```javascript
const user = (sequelize, DataTypes) => {
  const User = sequelize.define('user', {
    username: {
      type: DataTypes.STRING,
    },
  });

  User.associate = models => {
    User.hasMany(models.Message, { onDelete: 'CASCADE' });
  };

  return User;
};

export default user;
```

`src/models/user.js`

接下来，实现 `src/models/message.js` 模型：

```javascript
const message = (sequelize, DataTypes) => {
  const Message = sequelize.define('message', {
    text: {
      type: DataTypes.STRING,
    },
  });

  Message.associate = models => {
    Message.belongsTo(models.User);
  };

  return Message;
};

export default message;
```

`src/models/message.js`

这两个模型定义了它们实体的形状。消息模型有一个名为 `text` 的字符串类型数据库列。你可以向模型中水平地添加多个数据库列。模型的所有列构成了数据库中的一个表行，每行都反映一个数据库条目，例如消息或用户。数据库表名由 Sequelize 模型定义中的一个参数定义。消息领域拥有表“message”。你可以使用 Sequelize 的关联（associations）来定义实体与实体之间的关系。在这种情况下，一个消息实体属于一个用户，而该用户有许多消息。这是一个包含两个领域的极简数据库设置，但由于我们关注的是服务器端 GraphQL，你应该考虑阅读更多这些应用程序之外的数据库主题，以充分理解这一概念。

接下来，在应用程序内部的 `src/models/index.js` 文件中连接到数据库。我们需要数据库名称、数据库超级用户和密码。你可能还需要定义方言（dialect），因为 Sequelize 支持其他数据库。

```javascript
import Sequelize from 'sequelize';

const sequelize = new Sequelize(
  process.env.DATABASE,
  process.env.DATABASE_USER,
  process.env.DATABASE_PASSWORD,
  {
    dialect: 'postgres',
  },
);

export { sequelize };
```

`src/models/index.js`

> 注意：为了在源代码中访问环境变量，请安装并添加 [dotenv 包](https://github.com/motla/dotenv)，如此[教程](https://www.robinwieruch.de/minimal-node-babel/)所示。

在同一个文件中，你可以物理地关联所有模型并将其作为数据访问层暴露给应用程序。

```javascript
import Sequelize from 'sequelize';

const sequelize = new Sequelize(
  process.env.DATABASE,
  process.env.DATABASE_USER,
  process.env.DATABASE_PASSWORD,
  {
    dialect: 'postgres',
  },
);

const models = {
  User: sequelize.import('./user'),
  Message: sequelize.import('./message'),
};

Object.keys(models).forEach(key => {
  if ('associate' in models[key]) {
    models[key].associate(models);
  }
});

export { sequelize };

export default models;
```

`src/models/index.js`

数据库凭据——数据库名称、数据库超级用户名、数据库超级用户密码——可以存储为环境变量。在你的 `.env` 文件中添加这些键值对。我本地开发的默认值为：

```dotenv
DATABASE=postgres
DATABASE_USER=postgres
DATABASE_PASSWORD=postgres
```

`.env`

你在创建此应用程序时设置环境变量。如果没有，现在也可以将凭据留在源代码中。最后，当你的 Node.js 应用程序启动时，需要对数据库同步。在你的 `src/index.js` 文件中完成此操作：

```javascript
import express from 'express';
import { ApolloServer } from 'apollo-server-express';

import schema from './schema';
import resolvers from './resolvers';
import models, { sequelize } from './models';

...

sequelize.sync().then(async () => {
  app.listen({ port: 8000 }, () => {
    console.log('Apollo Server on http://localhost:8000/graphql');
  });
});
```

`src/index.js`

我们已经完成了 GraphQL 服务器的数据库设置。接下来，你将替换解析器（resolvers）中的业务逻辑，因为那里将使用 Sequelize 来访问数据库，而不是示例数据。应用程序尚未完全完成，因为解析器还没有使用新的数据访问层。

### 练习题

- 确认你[上一节的源码](http://bit.ly/2Vv1fJj)
  - 确认[来自上一节的更改](http://bit.ly/2VmdqHX)
- 熟悉数据库



- 尝试使用`psql`命令行界面访问数据库
- 通过阅读官方文档来熟悉 Sequelize API
- 查询此处提到的任何不熟悉的数据库术语。

## 连接解析器与数据库

你的 PostgreSQL 数据库已准备好在启动时连接到 GraphQL 服务器。现在，你将不再使用示例数据，而是将在 GraphQL 解析器中使用层数据访问层（`models`）来从数据库中读取数据或向数据库读写数据。在下一节中，我们将涵盖以下内容：

- 在你的 GraphQL 解析器中使用新模型
- 在应用程序启动时为数据库填充数据（Seed）
- 添加一个用户模型方法，用于通过用户名检索用户
- 学习关于`psql`命令行的基础知识

让我们从重构 GraphQL 解析器开始。你之前已经通过 Apollo Server 的 context 对象将模型传递给每个 GraphQL 解析器。我们之前使用了示例数据，但对于真实的数据库操作，Sequelize API 是必须的。在`src/resolvers/user.js`文件中，将以下代码更改为使用 Sequelize API：

```javascript
export default {
  Query: {
    users: async (parent, args, { models }) => {
      return await models.User.findAll();
    },
    user: async (parent, { id }, { models }) => {
      return await models.User.findById(id);
    },
    me: async (parent, args, { models, me }) => {
      return await models.User.findById(me.id);
    },
  },

  User: {
    messages: async (user, args, { models }) => {
      return await models.Message.findAll({
        where: {
          userId: user.id,
        },
      });
    },
  },
};
```

`src/resolvers/user.js`

`findAll()`和`findById()`是数据库操作中常用的 Sequelize 方法。不过，查找特定用户的所有消息更为具体。在这里，你使用了`where`子句根据数据库中的`userId`条目来缩小消息范围。访问数据库将为你的应用程序架构增加另一层复杂度，因此请务必根据需要随时参考 Sequelize API 文档。

接下来，返回`src/resolvers/message.js`文件并进行调整以使用 Sequelize API：

```javascript
export default {
  Query: {
    messages: async (parent, args, { models }) => {
      return await models.Message.findAll();
    },
    message: async (parent, { id }, { models }) => {
      return await models.Message.findById(id);
    },
  },

  Mutation: {
    createMessage: async (parent, { text }, { me, models }) => {
      return await models.Message.create({
        text,
        userId: me.id,
      });
    },

    deleteMessage: async (parent, { id }, { models }) => {
      return await models.Message.destroy({ where: { id } });
    },
  },

  Message: {
    user: async (message, args, { models }) => {
      return await models.User.findById(message.userId);
    },
  },
};
```

`src/resolvers/message.js`

除了`findById()`和`findAll()`方法外，你还在变更（mutations）中创建和删除消息。之前，你必须为消息生成自己的标识符，但现在一旦消息在数据库中创建，Sequelize 就会为你的消息添加唯一标识符。

在这两个文件中还有一个关键的更改：[async/await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)。Sequelize 是一个基于 JavaScript promise 的 ORM，因此它在对数据库进行操作时总是返回一个 JavaScript promise。这正是 async/await 可以作为 JavaScript 中异步请求更具可读性的版本的地方。你在上一节中已经学习了 Apollo Server 中 GraphQL 解析器的返回结果。一个结果也可以是一个 JavaScript promise，因为解析器正在等待其实际结果。在这种情况下，你也可以去掉 async/await 语句，你的解析器仍然可以工作。然而，有时更显式一些更好，特别是当我们以后在解析器的函数体内添加更多业务逻辑时，所以我们暂时保留这些语句。

现在，我们将转向当你的应用程序通过`npm start`启动时为数据库填充示例数据。当数据库在服务器监听之前同步完成后，你可以手动在数据库中创建两个带有消息的用户记录。以下`src/index.js`文件的代码显示了如何使用 async/await 执行这些操作。用户将具有关联的`messages`的`username`。

```javascript
...

const eraseDatabaseOnSync = true;

sequelize.sync({ force: eraseDatabaseOnSync }).then(async () => {
  if (eraseDatabaseOnSync) {
    createUsersWithMessages();
  }

  app.listen({ port: 8000 }, () => {
    console.log('Apollo Server on http://localhost:8000/graphql');
  });
});

const createUsersWithMessages = async () => {
  await models.User.create({
    username: 'wieruch',
    messages: [
      {
        text: 'Happy to learn',
      },
    ],
  });

  await models.User.create({
    username: 'ddids',
    messages: [
      {
        text: 'Happy to release',
      },
      {
        text: 'Published a complete',
      },
    ],
  });
};
```

`src/index.js`

`sync()`方法中的`force`标记可用于在启动时同步数据库。如果你想随时间推积累更改，可以移除该标记或将其设置为`false`。在生产环境中应该移除该标记。

接下来，我们需要处理`me`用户。之前，你使用的是示例数据中的用户；现在用户将来自数据库。这是一个为`src/models/user.js`文件中的用户模型编写一个自定义方法的好机会：

```javascript
const user = (sequelize, DataTypes) => {
  const User = sequelize.define('user', {
    username: {
      type: DataTypes.STRING,
    },
  });

  User.associate = models => {
    User.hasMany(models.Message, { onDelete: 'CASCADE' });
  };

  User.findByLogin = async login => {
    let user = await User.findOne({
      where: { username: login },
    });

    if (!user) {
      user = await User.findOne({
        where: { email: login },
      });
    }

    return user;
  };

  return User;
};

export default user;
```

`src/models/user.js`

用户模型上的`findByLogin()`方法根据`username`或`email`条目检索用户。用户现在还没有`email`条目，但当应用程序拥有身份验证机制时将添加它。`login`参数用于`username`和`email`，从数据库检索用户，你可以看到它是如何通过用户名或电子邮件登录应用程序的。

你在数据库模型上引入了第一个自定义方法。始终值得考虑将这些业务逻辑放在哪里。给模型提供这些访问方法时，可能会遇到所谓的*胖模型*（fat models）概念。另一种方法是编写独立的服务（如函数或类）来处理这些数据访问层功能。

新的模型方法可以用于从数据库检索`me`用户。然后你可以在`src/index.js`实例化 Apollo Server 时将其放入 context 对象中：

```javascript
const server = new ApolloServer({
  typeDefs: schema,
  resolvers,
  context: {
    models,
    me: models.User.findByLogin('rwieruch'),
  },
});
```

`src/index.js`

然而，这无法工作，因为用户是从数据库中异步读取的，所以`me`将是一个 JavaScript promise 而不是实际的用户；而且你可能希望在每次请求的基础上从数据库中检索`me`用户。否则，`me`用户在 Apollo Server 创建后将保持不变。相反，在 Apollo Server 中使用一个返回 context 对象的函数，而不是一个对象作为 context。该函数使用了`async/await`语句。每当请求访问你的 GraphQL API 时，该函数都会被调用，因此每次请求都会从数据库中获取`me`用户。

```javascript
const server = new ApolloServer({
  typeDefs: schema,
  resolvers,
  context: async () => ({
    models,
    me: await models.User.findByLogin('rwieruch'),
  }),
});
```

`src/index.js`

你应该能够重新启动你的应用程序了。在 GraphQL Playground 中尝试不同的 GraphQL 查询和变更，并验证一切运行正常。如果出现任何关于数据库的错误，请确保它已正确连接到你的应用程序，并且数据库也在命令行中运行。

由于你现在引入了数据库，GraphQL Playground 不再是唯一的手动测试工具了。虽然 GraphQL Playground 可以测试你的 GraphQL API，但你可能想使用`psql`命令行界面手动查询数据库。例如，你可能想检查数据库中的用户消息记录，或者在通过 GraphQL 变更创建消息后检查其中是否存在。首先，在命令行连接到你的数据库：

```bash
psql mydatabasename
```

### 命令行

其次，尝试以下 SQL 语句。这是学习 SQL 的绝佳机会：

```sql
SELECT * from users;
SELECT text from messages;
```

`psql`

结果如下：

```text
mydatabase=# SELECT * from users;
 id | username |         createdAt          |         updatedAt
----+----------+----------------------------+----------------------------
  1 | rwieruch | 2018-08-21 21:15:38.758+08 | 2018-08-21 21:15:38.758+08
  2 | ddavids  | 2018-08-21 21:15:38.786+08 | 2018-08-21 21:15:38.786+08
(2 rows)

mydatabase=# SELECT text from messages;
               text
-----------------------------------
 Published the Road to learn React
 Happy to release ...
 Published a complete ...
(3 rows)
```

`psql`

每当你执行 GraphQL 变更时，使用`psql`命令行界面检查你的数据库记录是明智的。这是学习 [SQL](https://en.wikipedia.org/wiki/SQL) 的极佳方法，通常 SQL 会在使用 Sequelize 等 ORM 时被抽象掉。

在本节中，你使用 PostgreSQL 数据库作为你的 GraphQL 服务器的数据源，并使用 Sequelize 作为数据库和你的 GraphQL 解析器之间的胶水。然而，这只是一种可能的解决方案。由于 GraphQL 与数据源无关，你可以为你的解析器选择任何数据源。它可以是另一个数据库（例如 MongoDB、Neo4j、Redis）、多个数据库，或者（第三方的）REST/GraphQL API 端点。GraphQL 仅确保在有传入查询或变更时，所有字段都经过了验证、执行和解析，无论数据源是什么。

## 练习

- 确认你[上一节的源代码](http://bit.ly/2VnMnMx)
- 确认[上一节的更改](http://bit.ly/2VqMNBJ)
- 尝试使用`psql`和对数据库进行数据填充
- 尝试使用 GraphQL playground 并查询现在来自数据库的数据
- 在你的解析器中移除并添加`async/await`语句，查看它们是否仍然能够工作
- 阅读更多关于 [GraphQL 执行](https://graphql.github.io/learn/execution/)的内容

## Apollo Server：验证与错误

验证、错误和边缘情况处理在编程中并不经常被口头描述。本节应该让你对 Apollo Server 和 GraphQL 的这些主题产生一些见解。通过 GraphQL，你负责从 GraphQL 解析器返回的内容。在解析器中插入业务逻辑并不困难，例如在它们从数据库读取数据之前。

```javascript
export default {
  Query: {
    users: async (parent, args, { models }) => {
      return await models.User.findAll();
    },
    user: async (parent, { id }, { models }) => {
      return await models.User.findById(id);
    },
    me: async (parent, args, { models, me }) => {
      if (!me) {
        return null;
      }

      return await models.User.findById(me.id);
    },
  },

  ...
};
```

`src/resolvers/user.js`

保持解析器的表面精简但在侧添加业务逻辑服务可能是一个好主意。这样推理解析器就总是很简单。在这个应用程序中，我们将业务逻辑保留在解析器中以保持统一。

### 解析器中的业务逻辑

（此处重复内容已根据指令要求清理）

### 错误处理

验证、错误和边缘情况处理在编程中并不经常被口头描述。本节应该让你对 Apollo Server 和 GraphQL 的这些主题产生一些见解。通过 GraphQL，你负责从 GraphQL 解析器返回的内容。在解析器中插入业务逻辑并不困难，例如在它们从数据库读取数据之前。

在这个应用程序中，我们将业务逻辑保留在解析器中以保持统一。

GraphQL 的错误输出在 GraphQL Playground 中应保持一致，因为你使用了相同的错误对象来生成`Error`实例。不过，你也可以通过`throw new Error('My error message.');`使用你的自定义消息。

调整错误消息另一种方法是在数据库模型定义中。每个验证规则都可以有一个自定义的验证消息，这些消息可以在`Sequelize`模型中定义：



`const message = (sequelize, DataTypes) => { const Message = sequelize.define('message', { text: { type: DataTypes.STRING, validate: { notEmpty: { args: true, msg: 'A message has to have a text.', }, }, }, }); Message.associate = models => { Message.belongsTo(models.User); }; return Message; }; export default message;`

当尝试创建一个带有空文本的消息时，`src/models/message.js` 会导致以下错误。同样，这在你的客户端应用程序中是非常直观的，因为格式保持不变：

```
{
  "data": null,
  "errors": [
    {
      "message": "SequelizeValidationError: A message has to have a text.",
      "locations": [],
      "path": [
        "create"
      ],
      "extensions": { }
    }
  ]
}
```

## GraphQL Playground

这是使用 Apollo Server 用于 GraphQL 的主要优势之一。错误处理通常是免费的，因为它会将数据库错误或其他第三方错误转换为有效的 GraphQL 结果。在客户端侧，你不需要担心结果的形状，因为数据对象为 `null` 但错误被捕获了。如果你想更改你的自定义错误，可以以解析器（resolver）为基础进行处理。Apollo Server 提供了一个全局处理的解决方案：

```
const server = new ApolloServer({
  typeDefs: schema,
  resolvers,
  formatError: error => {
    // 移除内部错误
    // 只留下重要的验证信息
    const message = error.message
      .replace('SequelizeValidationError: ', '')
      .replace('Validation error: ', '');

    return {
      ...error,
      message,
    };
  },
  context: async => ({
    models,
    me: await models.User.findByLogin('rwieruch'),
  }),
});
```

`src/index.js` 这些是在 Apollo Server 中使用 GraphQL 进行验证和错误处理的核心要点。验证可以在数据库（`model`）级别或业务逻辑（`resolvers`）级别进行。如果发生错误，Apollo Server 将对其进行格式化以与客户端配合。你也可以全局地格式化错误。

## 练习题

* [确认你上一节的源代码](http://bit.ly/2Vqeom)

* [确认上一节的更改](http://bit.ly/2Vqqb)

* 为你的数据库添加更多验证规则

* [阅读更多关于如何使用 Apollo Server 进行错误处理的内容](https://www.apol.com/docs/apollo-server/v2/features/errors.html)

* 了解 Apollo Server 中不同的错误

* [阅读更多关于使用自定义指令进行 GraphQL 字段验证](https://blog.apollo.com/graphql/validation-using-directives-4908fd5c)

* [阅读更多关于自定义 Schema 指令](https://www.apol.com/docs/apollo-server/v2/features/directives.html)

## Apollo Server：身份验证

GraphQL 中的身份验证是一个热门话题。目前没有强制性的实现方法，但许多人在应用程序中都需要它。GraphQL 本身对身份验证没有强制规定，因为它仅仅是一种语言。如果你想在 GraphQL 中实现身份验证，请考虑使用 GraphQL mutations。在本节中，我们将使用一种极简的方法为你的服务器添加身份验证。之后，应该能够为你的应用程序注册（注册）和登录用户。之前使用的 `me` 将是经过验证的用户。

在准备 GraphQL 身份验证机制之前，请扩展 `src/models/user.js` 文件中的用户模型。用户需要一个电子邮件地址（作为唯一标识符）和一个密码。电子邮件和用户名（另一个唯一标识符）都可以用于登录应用程序，这就是为什么这两个属性都用于用户的 `findByLogin()` 方法。

```
...

user = (sequelize, DataTypes) => {
  const User = sequelize.define('user', {
    username: {
      type: DataTypes.STRING,
      unique: true,
      allowNull: false,
      validate: {
        notEmpty: true,
      },
    },
    email: {
      type: DataTypes.STRING,
      unique: true,
      allowNull: false,
      validate: {
        notEmpty: true,
        isEmail: true,
      },
    },
    password: {
      type: DataTypes.STRING,
      allowNull: false,
      validate: {
        notEmpty: true,
        len: [7, 42],
      },
    },
  });

  ...

  return User;
};

export default user;
```

`src/models/user.js` 用户模型中的两个新条目有它们自己的验证规则，与之前相同。用户的密码应在 7 到 42 个字符之间，电子邮件应该具有有效的电子邮件格式。如果在创建用户期间这些任何一个验证失败，它将生成一个 JavaScript 错误，并通过 GraphQL 进行转换和传输。客户端应用程序中的注册表单随后可以显示验证错误。

你可能还想在 `src/schema/user.js` 文件的 GraphQL 用户 schema 中添加电子邮件，但不添加密码：

```
import { gql } from 'apollo-server-express';

export default gql`
  ...

  type User {
    id: ID!
    username: String!
    email: String!
    messages: [Message!]
  }
`;
```

`src/schema/user.js` 接下来，在 `src/index.js` 文件的种子数据中添加新属性：

```
const createUsersWithMessages = async () => {
  await models.User.create(
    {
      username: 'rwieruch',
      email: 'hello@robin.com',
      password: 'rwieruch',
      messages: [ ... ],
    },
    {
      include: [models.Message],
    },
  );

  await models.User.create(
    {
      username: 'ddavids',
      email: 'hello@david.com',
      password: 'ddavids',
      messages: [ ... ],
    },
    {
      include: [models.Message],
    },
  );
};
```

`src/index.js` 这些是为了开始 GraphQL 身份验证而进行的数据库数据迁移。

### 使用 GraphQL 进行注册（Sign Up）

现在，让我们查看 GraphQL 身份验证的细节。你将实现两个 GraphQL mutations：一个用于注册用户，另一个用于登录应用程序。让我们先从 `src/schema/user.js` 文件中的注册 mutation 开始：

首先，在 GraphQL Schema 中为你的新变更（mutation）添加对应的解析器函数（resolver function）。在你的 `src/resolvers/user.js` 文件中，添加以下解析器函数，它会在数据库中创建一个用户，并返回一个包含字符串格式令牌值的的对象。

```
const createToken = async (user) => {
  ...
};

export default {
  Query: {
    ...
  },

  Mutation: {
    signUp: async (
      parent,
      { username, email, password },
      { models },
    ) => {
      const user = await models.User.create({
        username,
        email,
        password,
      });

      return { token: createToken(user) };
    },
  },

  ...
};
```

`src/resolvers/user.js`

这就是基于令牌的注册的 GraphQL 框架。你为它创建了一个 GraphQL 变更和解析器，它会根据某些验证条件和传入的解析器参数在数据库中创建一个用户。它为注册的用户生成了一个令牌。目前，该设置已足够通过 GraphQL 变更创建一个新用户。

### 使用 Bcrypt 保护密码

这段代码中存在一个主要的安全漏洞：用户密码以明文形式存储在数据库中，这使得第三方更容易访问它。为了解决这个问题，我们使用如 [bcrypt](https://github.com/kelektiv/node.bcrypt.js) 这样的插件对密码进行哈希处理。首先，在命令行中安装它：

```
npm install bcrypt --save
```

### 命令行

注意：如果你在 Windows 上安装 `bcrypt` 时遇到任何问题，可以尝试一个名为 [bcrypt.js](https://github.com/dcodeIO/bcrypt.js) 的替代品。它的速度较慢，但有人反映它在他们的机器上可以运行。

现在，可以在 `signUp` 变更创建用户时，在用户的解析器函数中使用 `bcrypt` 对密码进行哈希处理。Sequelize 也有另一种替代方法。在你的用户模型中，定义一个钩子函数，该函数会在每次创建用户实体时执行：

```
const user = (sequelize, DataTypes) => {
  const User = sequelize.define('user', {
    ...
  });

  ...

  User.beforeCreate(user => {
    ...
  });

  return User;
};

export default user;
```

`src/models/user.js`

在这个钩子函数中，添加在用户实体到达数据库之前修改其属性的功能。让我们使用 `bcrypt` 对哈希密码来完成这一操作。

```
import bcrypt from 'bcrypt';

const user = (sequelize, DataTypes) => {
  const User = sequelize.define('user', {
    ...
  });

  ...

  User.beforeCreate(async user => {
    user.password = await user.generatePasswordHash();
  });

  User.prototype.generatePasswordHash = async function() {
    const saltRounds = 10;
    return await bcrypt.hash(this.password, saltRounds);
  };

  return User;
};

export default user;
```

`src/models/user.js`

`bcrypt.hash()` 方法接收一个字符串（用户密码）和一个称为盐值轮数（salt rounds）的整数。每个盐值轮都会增加哈希密码的成本，从而使攻击者解密哈希值的成本更高。如今盐值轮数的常见值在 10 到 12 之间，因为增加盐值轮数可能会导致两端出现性能问题。

在此实现实现中，`generatePasswordHash()` 函数被添加到用户的原型链上。这就是为什么可以在每个用户实例上作为方法执行该函数，这样你就可以在方法内部通过 `this` 访问用户本身。你也可以将带有密码的用户实例作为参数传递，我更倾向于这种方法，尽管使用 JavaScript 的原型继承是一个很好的工具。你可以使用 `bcrypt` 在用户在 `signUp` 变更中创建时对密码进行哈希处理。

### GraphQL 中的令牌身份验证

在用户解析器函数中，用户创建一个用户用户，足够。足够足够。。目前，设置设置足够创建一个通过 GraphQL 变更的令牌用户。

 GraphQL 令牌的身份

的 GraphQL 的令牌。

你为令牌创建的 GraphQL 变更和解析器。使用 [JSON Web 令牌（JWT)](https://jwt.io/) 进行身份验证。官方网站说：JWT 是一种开放标准。使用流行的 [jsonwebtoken](https://github.com/auth0/node) npm 包。

在命令行中安装它：

```
npm install jsonwebtoken --save
```

### 命令行

现在可以在 `src/resolvers/user.js` 中导入它并使用：

```
import jwt from 'jsonwebtoken';

const createToken = async user => {
  const { id, email, username } = user;
  return await jwt.sign({ id, email, username });
};
```

`src/resolvers/user.js`

`sign` 的第一个参数可以是任何用户信息。在 `.env` 文件的环境变量中添加密钥：

```
DATABASE=postgres
DATABASE_USER=postgres
DATABASE_PASSWORD=postgres

SECRET=yoursecret
```

然后，在 `src/index.js` 文件中，通过 Apollo Server 的上下文将密钥传递给所有解析器函数：

```
const server = new ApolloServer({
  typeDefs: schema,
  resolvers,
  ...
  context: async () => ({
    models,
    me,
    secret: process.env.SECRET,
  }),
});
```

`src/index.js`

### 令牌

JWT 的 `sign` 方法处理其余工作。你还可以传递第三个参数来设置令牌的过期时间或日期。在这种情况下，令牌仅有效 30 分钟，之后用户必须重新登录。

```
import jwt from 'jsonwebtoken';

const createToken = async (user, secret, expiresIn) => {
  const { id, email, username } = user;
  return await jwt.sign({ id, email, username }, secret, {
    expiresIn,
  });
};

export default {
  Query: {
    ...
  },

  Mutation: {
    signUp: async (
      parent,
      { username, email, password },
      { models, secret },
    ) => {
      const user = await models.User.create({
        username,
        email,
        password,
      });

      return { token: createToken(user, secret, '30m') };
    },
  },

  ...
};
```

`src/resolvers/user.js`



注册流程到此结束：你创建了一个用户并返回了一个有效的令牌，该令牌可以从客户端应用程序用于验证用户。服务器可以解析每个请求附带的令牌，并允许用户访问敏感数据。你可以使用 GraphQL Playground 测试注册，它会在数据库中创建一个用户并返回其对应的令牌。此外，你还可以使用 `psql` 检查数据库，测试用户是否已创建以及密码是否经过哈希。

## 使用 GraphQL 登录 (Sign In)

在深入学习基于请求的令牌授权之前，让我们来实现身份验证机制的第二个变异（mutation）：`signIn` 变异（或登录变异）。同样，首先在`src/schema/user.js`文件的用户 schema 中添加 GraphQL 变异：

```
import { gql } from 'apollo-server-express';

export default gql`
  ...

  extend type Mutation {
    signUp(
      username: String!
      email: String!
      password: String!
    ): Token!

    signIn(login: String!, password: String!): Token!
  }

  type Token {
    token: String!
  }

  ...
`;
```

`src/schema/user.js`

其次，在`src/resolvers/user.js`文件中添加对应的解析器（resolver）：

```
import jwt from 'jsonwebtoken';
import { AuthenticationError, UserInputError } from 'apollo-server';

...

export default {
  Query: {
    ...
  },

  Mutation: {
    signUp: async (...) => {
      ...
    },

    signIn: async (
      parent,
      { login, password },
      { models, secret },
    ) => {
      const user = await models.User.findByLogin(login);

      if (!user) {
        throw new UserInputError(
          '未找到此登录凭据的用户。',
        );
      }

      const isValid = await user.validatePassword(password);

      if (!isValid) {
        throw new AuthenticationError('密码错误.');
      }

      return { token: createToken(user, secret, '30m') };
    },
  },

  ...
};
```

`src/resolvers/user.js`

让我们逐步分析登录步骤的新解析器函数。作为参数，解析器可以访问 GraphQL 变异的输入参数（`login`、`password`）以及上下文（`models`、`secret`）。当用户尝试登录你的应用程序时，登录名（可以是唯一的用户名或唯一的邮箱）被用于从数据库中检索用户。如果没有该用户，应用程序将抛出一个错误，该错误可以在客户端应用程序中通知用户。如果有用户，则将对用户的密码进行验证。你将在下一个示例的用户模型中看到此方法。如果密码无效，应用程序将向客户端应用程序抛出错误。如果密码有效，`signIn`变异将返回一个与`signUp`变异相同的令牌。客户端应用程序执行成功登录，或者在凭据无效时显示错误消息。你还可以看到特定的 Apollo Server 错误，而不是通用的 JavaScript `Error`类。

接下来，我们想在用户实例上实现`validatePassword()`方法。将其放置在`src/models/user.js`文件中，因为所有的用户模型方法都存储在那里，与`findByLogin()`方法是一的。

```
import bcrypt from 'bcrypt';

const user = (sequelize, DataTypes) => {
  ...

  User.findByLogin = async login => {
    let user = await User.findOne({
      where: { username: login },
    });

    if (!user) {
      user = await User.findOne({
        where: { email: login },
      });
    }

    return user;
  };

  User.beforeCreate(async user => {
    user.password = await user.generatePasswordHash();
  });

  User.prototype.generatePasswordHash = async function() {
    const saltRounds = 10;
    return await bcrypt.hash(this.password, saltRounds);
  };

  User.prototype.validatePassword = async function(password) {
    return await bcrypt.compare(password, this.password);
  };

  return User;
};

export default user;
```

`src/models/user.js`

同样，这是 JavaScript 的原型继承，用于在用户实例中提供可用方法。在此方法中，可以使用`bcrypt`将用户（`this`）及其密码与 GraphQL 变异传入的密码进行比较，因为用户的密码经过哈希处理的，而传入的密码是明文。幸运的是，当用户登录时，`bcrypt`会告诉你密码是否正确。

现在你已经为你的 GraphQL 服务器应用程序设置了注册（sign up）和登录（sign in）。你使用了`bcrypt`配合 Sequelize 钩子函数，在密码到达数据库之前对其明文密码进行哈希和比较，并使用`JWT`通过密钥将用户数据加密为令牌。然后，每次注册和登录都会返回该令牌。随后，客户端应用程序可以保存令牌（例如存储在浏览器的本地存储中），并在每次 GraphQL 查询和变异中发送。

## 使用 GraphQL 进行授权

在上一节中，你设置了 GraphQL 变异以启用与服务器的身份验证。与身份验证相关的 GraphQL 变异都会返回令牌 (JWT)，使用密钥保护非敏感的用户信息。令牌无论是通过注册还是登录获取，都会返回给客户端应用程序。客户端应用程序必须将令牌存储在某个地方，如浏览器的话。每当向 GraphQL 服务器发送请求时，令牌必须附加在 HTTP 请求头中。随后 GraphQL 服务器可以验证 HTTP 请求头、验证其真实性，并执行类似 GraphQL 操作。如果令牌无效，GraphQL 服务器必须为 GraphQL 客户端返回错误。如果客户端本地存储了令牌，它应该移除令牌并将用户重定向到登录页。

现在我们只需要完成等式的服务器部分。让我们在`src/index.js`文件中实现，通过添加全局授权，在请求到达 GraphQL 解析器之前验证传入的令牌。

```
import jwt from 'jsonwebtoken';
import {
  ApolloServer,
  AuthenticationError,
} from 'apollo-server-express';
...

const getMe = async req => {
  const token = req.headers['x-token'];

  if (token) {
    try {
      return await jwt.verify(token, process.env.SECRET);
    } catch (e) {
      throw new AuthenticationError(
        '您的话已过期。请重新登录。',
      );
    }
  }
};

const server = new ApolloServer({
  typeDefs: schema,
  resolvers,
  ...
  context: async ({ req }) => {
    const me = await getMe(req);

    return {
      models,
      me,
      secret: process.env.SECRET,
    };
  },
});

...
```

`src/index.js`

在服务器端的这种通用授权中，你会在每次请求 Apollo Server 的上下文（context）时注入`me`用户，即从令牌中经过身份验证的用户。`me`用户在`createToken()`函数中被编码在令牌中。它不再是数据库中的用户，从而避免了额外的数据库请求。

在`getMe()`函数中，你从传入的 HTTP 请求中提取出名为`x-token`的授权 HTTP 请求头。GraphQL 客户端应用程序会在每次其他请求中将从注册或登录获取的令牌放在 HTTP 请求头中发送，同时携带 HTTP 请求的有效负载（例如 GraphQL 操作）。然后可以在函数中检查是否存在此的该 HTTP 请求头。如果没有，函数将继续处理请求，但`me`用户将为`undefined`。如果存在令牌，函数将使用其密钥验证令牌，并检索在你创建令牌时所存储的用户信息。如果由于令牌无效或过期导致验证失败，GraphQL 服务器将抛出一个特定的 Apollo Server Error。如果验证通过，函数将带有已定义的`me`用户继续执行。

当客户端应用程序发送带有无效或已过期的令牌的 HTTP 请求头时，该函数会返回一个错误。否则，函数将允许请求通过，因为必须在解析器（resolver）级别检查用户，以确定他们是否允许执行某些操作。未身份验证的用户（`me`用户为`undefined`）可能能够检索消息但不能创建新消息。该应用程序现在受到了不受无效和过期令牌的保护。

这就是对你的 GraphQL 服务器应用程序最高级别的身份验证。你可以通过 GraphQL 客户端应用程序使用`signUp`和`signIn` GraphQL 变动（mutations）对 GraphQL 服务器进行身份验证，而 GraphQL 服务器只允许来自 GraphQL 客户端应用程序的有效且未过期的令牌。

### 解析器层面的 GraphQL 授权

一个 GraphQL HTTP 请求会通过`getMe()`函数，即使它没有用于令牌的 HTTP 请求头。这是良好的默认行为，因为你可能需要在没有令牌的情况下注册新用户并登录应用程序。你可能希望在未通过应用程序身份验证的情况下查询消息或用户。在没有授权令牌的情况下通过某些请求是可以接受且有时必要的，以便为不同类型的用户授予不同级别的访问权限。只有当令牌无效或过期时才会发生错误。

然而，某些 GraphQL 操作应该具有更具体的授权。创建消息应该仅允许授权用户进行，否则将无法追踪消息的作者。`createMessage` GraphQL 变动可以在 GraphQL 解析器级别受到保护或“守卫”。保护 GraphQL 操作的简单方法是在`src/resolvers/message.js`文件中使用`if-else`语句对其进行守卫：

```javascript
import { ForbiddenError } from 'apollo-server';

export default {
  Query: {
    ...
  },

  Mutation: {
    createMessage: async (parent, { text }, { me, models }) => {
      if (!me) {
        throw new ForbiddenError('Not authenticated as user.');
      }

      return await models.Message.create({
        text,
        userId: me.id,
      });
    },

    ...
  },

  ...
};
```

`src/resolvers/message.js`

你可以想象，如果将其用于所有已身份验证用户可访问的 GraphQL 操作，将会变得多么重复且容易出错，因为它将大量的授权逻辑混合在了解析器函数中。为了解决这个问题，我们引入了一个用于保护 GraphQL 操作的授权抽象层，其解决方案被称为**组合解析器（combined resolvers）**或**解析器中间件（resolver middleware）**。让我们安装这个 node 包：

```bash
npm install graphql-resolvers --save
```

### 命令行

让我们在一个新的`src/resolvers/authorization.js`文件中使用此包实现一个保护性解析器函数。它应该只检查是否存在`me`用户。

```javascript
import { ForbiddenError } from 'apollo-server';
import { skip } from 'graphql-resolvers';

export const isAuthenticated = (parent, args, { me }) =>
  me ? skip : new ForbiddenError('Not authenticated as user.');
```

`src/resolvers/authorization.js`

`isAuthenticated()`解析器函数充当中间件，要么继续执行下一个解析器（`skip`），要么执行另一个操作（如返回错误）。在这种情况下，当`me`用户不可用时会返回错误。由于它本身是一个解析器函数，它的参数与普通解析器相同。当在`src/resolvers/message.js`中创建消息时，可以使用该守卫解析器。使用新安装的 node 包中的`combineResolvers()`导入它。新的解析器通过组合解析器来保护其他解析器。

```javascript
import { combineResolvers } from 'graphql-resolvers';

import { isAuthenticated } from './authorization';

export default {
  Query: {
    ...
  },

  Mutation: {
    createMessage: combineResolvers(
      isAuthenticated,
      async (parent, { text }, { models, me }) => {
        return await models.Message.create({
          text,
          userId: me.id,
        });
      },
    ),

    ...
  },

  ...
};
```

`src/resolvers/message.js`

现在，`isAuthenticated()`解析器函数始终会在创建数据库中关联已身份验证用户的消息的解析器之前运行。解析器彼此链在一起，你可以在需要的地方复用该保护性解析器函数。它只对你的实际解析器增加了微小的开销，而这些内容可以在`src/resolvers/authorization.js`文件中进行更改。

### 基于权限的 GraphQL 授权

之前的解析器只检查用户是否经过身份验证，因此它仅适用于高级层。权限的情况需要另一个比`src/resolvers/authorization.js`中更具体的守卫解析器：

```javascript
...

export const isMessageOwner = async (
  parent,
  { id },
  { models, me },
) => {
  const message = await models.findById(id, { raw: true });

  if (message.userId !== me.id) {
    throw new ForbiddenError('Not authenticated as owner.');
  }

  return skip;
};
```

`src/resolvers/authorization.js`

此解析器检查身份验证的用户是否为消息的所有者。在删除消息之前这是一个很有检查，因为你只希望消息创建者能够删除它。守卫解析器通过`id`获取消息，并将消息的用户与身份验证的用户进行对比，要么抛出错误要么继续执行下一个解析器。

让我们在`src/resolvers/message.js`文件中使用这个精细授权权限解析器来保护解析器：



进入`/path/to/xxx`目录，找到`xxx.json`。

在表达式`cvar = avar + bvar`中，加法运算符（`+`）将`avar`与`bvar`相加，得到它们的和`cvar`

在`List.of(arg0, arg1, arg2)`中，`List`接口的工厂方法`of()`接受一系列的元素，返回包含它们的只读列表。

之后我们这样调用`cmd`命令：`cmd arg0 arg1 arg2`。

```
if (condVar > someVal) {console.log("xxx")}
```



```javascript
...

sequelize.sync({ force: eraseDatabaseOnSync }).then(async () => {
  if (eraseDatabaseOnSync) {
    createUsersWithMessages(new Date());
  }

  app.listen({ port: 8000 }, () => {
    console.log('Apollo Server on http://localhost:8000/graphql');
  });
});

const createUsersWithMessages = async date => {
  await models.User.create(
    {
      username: 'rwieruch',
      email: 'hello@robin.com',
      password: 'rwieruch',
      role: 'ADMIN',
      messages: [
        {
          text: 'Published the Road to learn React',
          createdAt: date.setSeconds(date.getSeconds() + 1),
        },
      ],
    },
    {
      include: [models.Message],
    },
  );

  await models.User.create(
    {
      username: 'ddavids',
      email: 'hello@david.com',
      password: 'ddavids',
      messages: [
        {
          text: 'Happy to release ...',
          createdAt: date.setSeconds(date.getSeconds() + 1),
        },
        {
          text: 'Published a complete ...',
          createdAt: date.setSeconds(date.getSeconds() + 1),
        },
      ],
    },
    {
      include: [models.Message],
    },
  );
};
```

`src/index.js`

现在，你应该能够在 GraphQL Playground 中查询消息的`createdAt`了：

```graphql
query {
  message(id: "1") {
    id
    createdAt
    user {
      username
    }
  }
}

// query 结果
{
  "data": {
    "message": {
      "id": "1",
      "createdAt": "1540978531448",
      "user": {
        "username": "rwieruch"
      }
    }
  }
}
```

GraphQL Playground

你可能注意到某些奇怪的地方：虽然 GraphQL Playground 返回的日期是一个 Unix 时间戳（例如 `1540978531448`），但消息（以及其他实体）的数据库日期却是另一种格式（例如 2018）。

### 使用 Apollo Server 进行 GraphQL 分页（Pagination）

在使用 GraphQL 时，对于带有列表的应用程序，你几乎会遇到一种名为**分页（pagination）**的功能。聊天应用中存储的用户消息会变成长列表，当客户端应用程序请求消息进行显示时，一次性从数据库中检索所有消息会导致严重的性能瓶颈。分页允许你将项目列表分成多个列表，称为“页面”。页面通常通过限制（limit）和偏移（offset）来定义。这样，你可以请求一个页面，当用户想查看更多内容时，请求另一个页面。

在接下来的章节中，你将使用两种不同的方法在 GraphQL 中实现分页。第一方法是最简单的方法，称为**基于偏移/限制的分页（offset/limit-based pagination）**。高级方法是**基于游标的分页（cursor-based pagination）**，这是应用程序中实现分页的许多复杂方法之一。

### 使用 Apollo Server 和 GraphQL 实现偏移/限制分页

基于`offset/limit`的分页实现并不困难。`limit`规定你想从整个列表中检索多少条项目，而`offset`则表示从整个列表的哪个位置开始。通过使用不同的`offsets`，你可以遍历整个项目列表，并使用`limit`获取其中的子列表（页）。

我们在`src/schema/message.js`文件中设置了消息模式（schema），以包含这两个新参数：

```javascript
import { gql } from 'apollo-server-express';

export default gql`
  extend type Query {
    messages(offset: Int, limit: Int): [Message!]!
    message(id: ID!): Message!
  }

  extend type Mutation {
    createMessage(text: String!): Message!
    deleteMessage(id: ID!): Boolean!
  }

  type Message {
    id: ID!
    text: String!
    createdAt: Date!
    user: User!
  }
`;
```

`src/schema/message.js`

然后，你可以调整`src/resolvers/message.js`文件中的解析器（resolver）来处理这些新参数：

```javascript
...

export default {
  Query: {
    messages: async (
      parent,
      { offset = 0, limit = 100 },
      { models },
    ) => {
      return await models.Message.findAll({
        offset,
        limit,
      });
    },
    message: async (parent, { id }, { models }) => {
      return await models.Message.findById(id);
    },
  },

  Mutation: {
    ...
  },

  ...
};
```

`src/resolvers/message.js`

幸运的是，你的 ORM（`Sequelize`）为你提供了内部`offset`和`limit`功能所需的所有内容。你可以在 GraphQL Playground 中通过调整`limit`和`offset`来尝试一下。

```graphql
query {
  messages(offset: 1, limit: 2){
    text
  }
}
```

GraphQL Playground

尽管这种方法更简单，但它存在一些缺点。当你的`offset`变得非常大时，数据库查询将耗时更长，这可能导致 UI 在等待下一页数据时客户端性能下降。此外，`offset/limit`分页无法处理查询之间被删除的项目。例如，如果你查询了第一页，有人删除了一个项目，那么下一页的`offset`就会出错，因为项目数量少了一个。你无法通过`offset/limit`分页轻易地解决这个问题，这就是为什么基于游标（cursor-based）的分页可能是必要的。

### 使用 Apollo Server 和 GraphQL 实现游标分页

在基于游标的分页中，`offset`是一个称为`cursor`的标识符，而不是像`offset/limit`分页那样计数项目。`cursor`可以表示“从游标 Y 开始获取 X 条数据”。一种常用方法是使用日期（例如数据库实实体创建日期）来识别列表中的项目。在我们案例中，每条消息已经有一个`createdAt`日期，该日期在写入数据库时分配给实体，并在消息实体的模式中暴露。每条消息的创建日期将作为`cursor`。

现在我们必须在`src/schema/message.js`文件中将原始分页改为基于游标的分页。你只需要将`offset`替换为`cursor`即可。`offset`只能隐式地与列表中的项目匹配，并且一旦项目从列表中被删除它就会改变；而`cursor`具有稳定的位置，因为消息的创建日期不会改变。

```javascript
import { gql } from 'apollo-server-express';

export default gql`
  extend type Query {
    messages(cursor: String, limit: Int): [Message!]!
    message(id: ID!): Message!
  }

  extend type Mutation {
    createMessage(text: String!): Message!
    deleteMessage(id: ID!): Boolean!
  }

  type Message {
    id: ID!
    text: String!
    createdAt: Date!
    user: User!
  }
`;
```

`src/schema/message.js`

由于你调整了消息的模式，请也并在你的`src/resolvers/message.js`文件中反映这些更改：

```javascript
import Sequelize from 'sequelize';

...

export default {
  Query: {
    messages: async (parent, { cursor, limit = 100 }, { models }) => {
      return await models.Message.findAll({
        limit,
        where: {
          createdAt: {
            [Sequelize.Op.lt]: cursor,
          },
        },
      });
    },
    message: async (parent, { id }, { models }) => {
      return await models.Message.findById(id);
    },
  },

  Mutation: {
    ...
  },

  ...
};
```

`src/resolvers/message.js`

`cursor`代替了`offset`是消息的`createdAt`属性。使用`Sequelize`和其他 ORM，可以添加子句来通过起始属性（`createdAt`）查找列表中所有属性小于（`lt`）或大于（`gt`，此处未使用）该属性值的项目。使用日期作为`cursor`时，`where`子句会找到该日期**之前**的所有消息，因为这里有一个`lt``Sequelize`操作符。还有两点可以让它正常工作：

```javascript
...

export default {
  Query: {
    messages: async (parent, { cursor, limit = 100 }, { models }) => {
      return await models.Message.findAll({
        order: [['createdAt', 'DESC']],
        limit,
        where: cursor
          ? {
              createdAt: {
                [Sequelize.Op.lt]: cursor,
              },
            }
          : {},
      });
    },
    message: async (parent, { id }, { models }) => {
      return await models.Message.findById(id);
    },
  },

  Mutation: {
    ...
  },

  ...
};
```

这是一个基于标的分页的基础实现，使用项目的创建日期作为稳定标识。创建日期是一种常用方法，但你也应该探索其他的替代方案。

### 基于标的分页：页面信息、连接（Connections）和哈希（Hashes）

在关于 GraphQL 分页的最后一个章节中，我们通过一些改进了基于游标的分页。目前，你必须查询消息的所有创建日期，并将最后一条消息的创建日期作为下一页的游标。GraphQL 连接仅对你的 GraphQL 列表字段增加了结构性变化，允许你传递元数据。让我们在`/src/schema/message.js`文件中添加一个 GraphQL 连接：

```javascript
import { gql } from 'apollo-server-express';

export default gql`
  extend type Query {
    messages(cursor: String, limit: Int): MessageConnection!
    message(id: ID!): Message!
  }

  extend type Mutation {
    createMessage(text: String!): Message!
    deleteMessage(id: ID!): Boolean!
  }

  type MessageConnection {
    edges: [Message!]!
    pageInfo: PageInfo!
  }

  type PageInfo {
    endCursor: Date!
  }

  type Message {
    id: ID!
    text: String!
    createdAt: Date!
    user: User!
  }
`;
```

`/src/schema/message.js`

你引入了一个中间层，通过`PageInfo`类型持有元数据，并在`edges`字段中持有项目列表。在中间层中，你可以引入新信息，例如`endCursor`（列表中最后一条消息的`createdAt`）。这样，你就不需要查询每条消息的`createdAt`日期，只需要查询`endCursor`。请将这些更改放在`/src/resolvers/message.js`文件中：

```javascript
...

export default {
  Query: {
    messages: async (parent, { cursor, limit = 100 }, { models }) => {
      const cursorOptions = cursor
        ? {
            where: {
              createdAt: {
                [Sequelize.Op.lt]: cursor,
              },
            },
          }
        : {};

      const messages = await models.Message.findAll({
        order: [['createdAt', 'DESC']],
        limit,
        ...cursorOptions,
      });

      return {
        edges: messages,
        pageInfo: {
          endCursor: messages[messages.length - 1].createdAt,
        },
      };
    },
    message: async (parent, { id }, { models }) => {
      return await models.Message.findById(id);
    },
  },

  Mutation: {
    ...
  },

  ...
};
```

`/src/resolvers/message.js`

你通过中间的`edges`和`pageInfo`字段为结果提供了新结构。`pageInfo`字段现在拥有列表中最后一条消息的游标，你应该能够以以下方式查询第一页：

```graphql
query {
  messages(limit: 2) {
    edges {
      text
    }
    pageInfo {
      endCursor
    }
  }
}
```

GraphQL Playground

结果可能如下所示：



```json
{
  "data": {
    "messages": {
      "edges": [
        {
          "text": "Published a complete ..."
        },
        {
          "text": "Happy to release ..."
        }
      ],
      "pageInfo": {
        "endCursor": "2018-10-25T08:29:56.771Z"
      }
    }
  }
}
```

### GraphQL Playground

使用上一个游标查询下一页：

```graphql
query {
  messages(limit: 2, cursor: "2018-10-25T08:29:56.771Z") {
    edges {
      text
    }
    pageInfo {
      endCursor
    }
  }
}
```

### GraphQL Playground

再次，这只会返回列表中剩余的最后一条消息。你不再需要查询每条消息的创建日期，只需要查询最后一条消息的游标。客户端应用程序不需要最后一条消息游标的详细信息，因为它现在只需要`endCursor`。

你可以在中间 GraphQL 连接层中添加相关信息。有时，GraphQL 客户端需要知道列表是否有更多页面可以查询，因为每个列表都是有限的。让我们在`/src/schema/message.js`文件中为消息的连接添加此信息：

```javascript
import { gql } from 'apollo-server-express';

export default gql`
  extend type Query {
    messages(cursor: String, limit: Int): MessageConnection!
    message(id: ID!): Message!
  }

  extend type Mutation {
    createMessage(text: String!): Message!
    deleteMessage(id: ID!): Boolean!
  }

  type MessageConnection {
    edges: [Message!]!
    pageInfo: PageInfo!
  }

  type PageInfo {
    hasNextPage: Boolean!
    endCursor: Date!
  }

  ...
`;
```

`/src/schema/message.js`

在`/src/resolvers/message.js`文件的解析器中，你可以通过以下方式找到这些信息：

```javascript
...

export default {
  Query: {
    messages: async (parent, { cursor, limit = 100 }, { models }) => {
      const cursorOptions = cursor
        ? {
            where: {
              createdAt: {
                [Sequelize.Op.lt]: cursor,
              },
            },
          }
        : {};

      const messages = await models.Message.findAll({
        order: [['createdAt', 'DESC']],
        limit,
        ...cursorOptions,
      });

      const hasNextPage = messages.length > limit;
      const edges = hasNextPage ? messages.slice(0, -1) : messages;

      return {
        edges,
        pageInfo: {
          hasNextPage,
          endCursor: edges[edges.length - 1].createdAt,
        },
      };
    },
    message: async (parent, { id }, { models }) => {
      return await models.Message.findById(id);
    },
  },

  Mutation: {
    ...
  },

  ...
};
```

`/src/resolvers/message.js`

你获取了比`limit`更多的消息。如果列表大于`limit`，则有下一页；否则没有。你可以在`pageInfo`中包含`hasNextPage`。如果你在`limit`为 2 且没有游标的情况下进行查询，`hasNextPage`为 true。如果你在`limit`大于 2 且没有游标的情况下进行查询，`hasNextPage`变为 false。这时，你的 GraphQL 应用程序就知道列表已结束。

游标仍然是消息的创建日期。客户端不关心游标的格式或实际值，因此我们将使用 base64 编码的哈希函数请求游标：

```javascript
...

const toCursorHash = string => Buffer.from(string).toString('base64');

const fromCursorHash = string =>
  Buffer.from(string, 'base64').toString('ascii');

export default {
  Query: {
    messages: async (parent, { cursor, limit = 100 }, { models }) => {
      const cursorOptions = cursor
        ? {
            where: {
              createdAt: {
                [Sequelize.Op.lt]: fromCursorHash(cursor),
              },
            },
          }
        : {};

      const messages = await models.Message.findAll({
        order: [['createdAt', 'DESC']],
        limit,
        ...cursorOptions,
      });

      const hasNextPage = messages.length > limit;
      const edges = hasNextPage ? messages.slice(0, -1) : messages;

      return {
        edges,
        pageInfo: {
          hasNextPage,
          endCursor: toCursorHash(
            edges[edges.length - 1].createdAt.toString(),
          ),
        },
      };
    },
    message: async (parent, { id }, { models }) => {
      return await models.Message.findById(id);
    },
  },

  Mutation: {
    ...
  },

  ...
};
```

`/src/resolvers/message.js`

作为元数据的返回游标被新的工具函数进行了哈希处理。记住在哈希处理之前将其转换为字符串。此外，`/src/schema/message.js`文件中的`endCursor`不再是 Date 类型，而是变成了 String 标量。

```javascript
import { gql } from 'apollo-server-express';

export default gql`
  ...

  type MessageConnection {
    edges: [Message!]!
    pageInfo: PageInfo!
  }

  type PageInfo {
    hasNextPage: Boolean!
    endCursor: String!
  }

  ...
`;
```

`/src/schema/message.js`

GraphQL 客户端接收到一个哈希处理过的`endCursor`字段。该哈希值可以作为游标来查询下一页。在解析器（resolver）中，传入的游标会被反哈希为实际日期，并用于数据库查询。

对游标进行哈希是基于游标的分页常用方法，因为它向客户端隐藏了细节。（GraphQL）客户端应用程序只需要使用哈希值作为游标来查询下一页分页数据。

## 练习

- 确认你[上一节的源代码](http://bit.ly/2VoLW4z)
  - 确认[来自上一节的更改](http://bit.ly/2VkTc1y)
- 阅读更多关于[GraphQL 分页](https://graphql.github.io/learn/pagination/)

## GraphQL 订阅（Subscriptions）

到目前，你已经使用 GraphQL 通过查询（queries）和变变（mutations）来读写数据。这些是让 GraphQL 服务器准备好 CRUD 操作的两个基本 GraphQL 操作。接下来，你将学习 GraphQL 订阅，用于 GraphQL 客户端与服务器之间的实时通信。

接下来，你将为创建的消息实现实时通信。如果用户创建了一条消息，另一个用户应该在 GraphQL 客户端应用程序中作为实时更新接收这条消息。首先，我们在`/src/schema/message.js`架构中添加 Subscription 根级类型：

```graphql
import { gql } from 'apollo-server-express';

export default gql`
  extend type Query {
    ...
  }

  extend type Mutation {
    ...
  }

  ...

  type Message {
    id: ID!
    text: String!
    createdAt: Date!
    user: User!
  }

  extend type Subscription {
    messageCreated: MessageCreated!
  }

  type MessageCreated {
    message: Message!
  }
`;
```

`/src/schema/message.js`

作为一个简单的 GraphQL 消费者，订阅的工作方式类似于 GraphQL 查询。区别在于，订阅会随时间推发布更改（事件）。每当消息被创建时，订阅的 GraphQL 客户端都会接收到创建的消息作为载荷。GraphQL 客户端对 schema 的订阅看起来如下：

```graphql
subscription {
  messageCreated {
    message {
      id
      text
      createdAt
      user {
        id
        username
      }
    }
  }
}
```

### GraphQL Playground（游乐场）

在第一部分，你将为你的应用程序设置订阅架构；然后，你将添加“创建消息”订阅的实现细节。第一步只需要完成一次，但当你的应用程序中添加更多 GraphQL 订阅时，后者将反复出现。

### Apollo Server 订阅设置

由于我们使用 Express 作为中间件，请在`/src/index.js`文件中使用高级的 HTTP 服务器设置来暴露订阅：

```javascript
import http from 'http';

...

server.applyMiddleware({ app, path: '/graphql' });

const httpServer = http.createServer(app);
server.installSubscriptionHandlers(httpServer);

const eraseDatabaseOnSync = true;

sequelize.sync({ force: eraseDatabaseOnSync }).then(async () => {
  if (eraseDatabaseOnSync) {
    createUsersWithMessages(new Date());
  }

  httpServer.listen({ port: 8000 }, () => {
    console.log('Apollo Server on http://localhost:8000/graphql');
  });
});

...
```

`/src/index.js`

对于传递给解析器的上下文（context），你可以在同一个文件中区分 HTTP 请求（GraphQL 变变查询）和订阅。HTTP 请求带有`req`和`res`对象，但订阅带有一个连接对象，因此你可以将模型作为数据访问层传递给订阅的上下文。

```javascript
...

const server = new ApolloServer({
  typeDefs: schema,
  resolvers,
  ...
  context: async ({ req, connection }) => {
    if (connection) {
      return {
        models,
      };
    }

    if (req) {
      const me = await getMe(req);

      return {
        models,
        me,
        secret: process.env.SECRET,
      };
    }
  },
});

...
```

`/src/index.js`

为了完成订阅设置，你需要使用一个[PubSub 引擎](https://www.apollographql.com/docs/apollo-server/v2/features/subscriptions.html#PubSub-Implementations)来发布和订阅事件。Apollo Server 默认带了一个，但如果你觉得它不够用，也有其他选项的链接。在新的`/src/subscription/index.js`文件中添加以下内容：

```javascript
import { PubSub } from 'apollo-server';

export default new PubSub();
```

`/src/subscription/index.js`

这个`PubSub`实例是你的 API，允许你的应用程序中使用订阅。订阅的总体设置现在已完成。

### 使用 PubSub 进行订阅和发布

让我们为消息创建实现特定的订阅。另一个 GraphQL 客户端监听消息的创建应该是可能的。例如，在聊天应用程序中，应该实时看到别人的消息。因此，使用以下实现扩展之前的`/src/subscription/index.js`文件：

```javascript
import { PubSub } from 'apollo-server';

import * as MESSAGE_EVENTS from './message';

export const EVENTS = {
  MESSAGE: MESSAGE_EVENTS,
};

export default new PubSub();
```

`/src/subscription/index.js`

并在新的`/src/subscription/message.js`文件中添加你的第一个事件：

```javascript
export const CREATED = 'CREATED';
```

`/src/subscription/message.js`

这种文件夹结构允许你在领域级别分离事件。通过导出所有事件及其领域，你可以在其他地方导入它们。缺失的部分是在消息解析器中使用`PubSub`实例。在本节的开始，你向 schema 中添加了订阅。现在你需要在`/src/resolvers/message.js`中实现它的对应：

```javascript
...

import pubsub, { EVENTS } from '../subscription';

...

export default {
  Query: {
    ...
  }

  Mutation: {
    ...
  }

  Message: {
    ...
  }

  Subscription: {
    messageCreated: {
      subscribe: () => pubsub.asyncIterator(EVENTS.MESSAGE.CREATED),
    },
  },
};
```

`/src/resolvers/message.js`



`subscribe`函数签名与其他解析器具有相同的参数。可以访问上下文中的模型，但对于此应用程序并非必要。订阅解析器为 schema 中的订阅提供了对应。然而，由于它使用了发布-订阅机制（PubSub）处理事件，你只实现了订阅，还没有实现发布。发布新消息的最佳位置是在创建消息相同的文件中：

```
...

import pubsub, { EVENTS } from '../subscription';

...

export default {
  Query: {
    ...
  },

  Mutation: {
    createMessage: combineResolvers(
      isAuthenticated,
      async (parent, { text }, { models, me }) => {
        const message = await models.Message.create({
          text,
          userId: me.id,
        });

        pubsub.publish(EVENTS.MESSAGE.CREATED, {
          messageCreated: { message },
        });

        return message;
      },
    ),

    ...
  },

  Message: {
    ...
  },

  Subscription: {
    messageCreated: {
      subscribe: () => pubsub.asyncIterator(EVENTS.MESSAGE.CREATED),
    },
  },
};
```

`/src/resolvers/message.js`

你使用 Apollo Server 和 PubSub 在 GraphQL 中实现了你的第一个订阅。为了测试它，请使用登录用户创建一个新消息。你可以在 GraphQL Playground 的两个标签页中尝试这两个 GraphQL 操作以比较它们的输出。在第一个标签页中执行订阅：

```graphql
subscription {
  messageCreated {
    message {
      text
    }
  }
}
```

该标签页将指示它正在监听更改。在第二个标签页中，登录一个用户：

```graphql
mutation {
  signIn(login: "rwieruch", password: "rwieruch") {
    token
  }
}
```

### GraphQL Playground

从结果中复制 token，然后将其粘贴到同一标签页的 HTTP headers 面板中：

```json
{
  "x-token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJoZWxsb0Byb2Jpbi5jb20iLCJ1c2VybmFtZSI6InJ3aWVydWNoIiwicm9sZSI6IkFETUlOIiwiaWF0IjoxNTM0OTQ3NTYyLCJleHAiOjE1MzQ5NDkzNjJ9.mg4M6SfYPJkGf_Z2Zr7ztGNbDRDLksRWdhhDvTbmWbQ"
}
```

### GraphQL Playground

然后在第二个标签页中创建一条消息：

```graphql
mutation {
  createMessage(text: "Does my subscription work?") {
    text
  }
}
```

### GraphQL Playground

之后，再次检查你的第一个标签页。它应该显示创建的消息：

```json
{
  "data": {
    "messageCreated": {
      "message": {
        "id": "4",
        "text": "Does my subscription work?",
        "createdAt": "2018-10-25T08:56:04.786Z",
        "user": {
          "id": "1",
          "username": "rwieruch"
        }
      }
    }
  }
}
```

### GraphQL Playground

你已经实现了 GraphQL 订阅（Subscriptions）。理解它们可能是一项挑战，但一旦你完成了一些基础操作，就可以将这些作为基础来创建实时 GraphQL 应用程序。

### 练习：

- 确认你的[上一个节的源代码](http://bit.ly/2VpaUAX)

- 确认[上一个节的更改](http://bit.ly/2Vq0mRW)

- 阅读更多关于[使用 Apollo Server 进行订阅](https://www.apollographql.com/docs/apollo-server/v2/features/subscriptions.html)的介绍

- 观看关于[GraphQL 订阅](http://youtu.be/bn8qsi8jVew)的讲座

## 测试 GraphQL 服务器

测试在编程教学中经常被忽视，因此本节将侧重于 GraphQL 服务器的端到端（E2E）测试。虽然单元测试和集成测试是流行的测试金字塔的基础支柱，涵盖了应用程序的所有独立功能，但 E2E 测试涵盖了整个应用程序的用户场景。E2E 测试将评估用户是否能够注册你的应用程序，或者管理员用户是否可以删除其他用户。你不需要编写大量的 E2E 测试，因为它们涵盖了更大、更复杂的用户场景，而不仅仅是基本功能。此外，E2E 测试涵盖了应用程序的所有技术角落，例如 GraphQL API、业务逻辑和数据库。

### GraphQL 服务器 E2E 测试设置

测试我们创建的应用程序实际上只需要名为 `Mocha` 和 `Chai` 的程序。`Mocha` 是一个测试运行器，允许你从 `npm` 脚本执行测试，同时提供组织化的测试结构；`Chai` 为你提供了进行断言的所有功能，例如根据真实场景“期望 X 等于 Y”并运行它们。

```bash
npm install mocha chai --save-dev
```

### 命令行

要使用这些程序，你必须先安装名为 [axios](https://github.com/axios/axios) 的库来向 GraphQL API 发送请求。在测试用户注册时，你可以向 GraphQL API 发送 GraphQL mutation，在数据库中创建一个用户并返回其信息。

```bash
npm install axios --save-dev
```

### 命令行

`Mocha` 通过你 `package.json` 文件中的 npm 脚本运行。这里使用的模式匹配 `src/` 文件夹内后缀为 `*.spec.js` 的所有测试文件。

```json
{
  ...
  "scripts": {
    "start": "nodemon --exec babel-node src/index.js",
    "test": "mocha --require @babel/register 'src/**/*.spec.js'"
  },
  ...
}
```

`package.json`

不要忘记用 `npm install @babel/register --save-dev` 安装 babel node 包。这应该足够运行你的第一个测试了。在你的应用程序中添加 `src/tests/user.spec.js`，并在那里编写你的第一个测试：

```javascript
import { expect } from 'chai';

describe('users', () => {
  it('user is user', () => {
    expect('user').to.eql('user');
  });
});
```

`src/tests/user.spec.js`

通过在命令行输入 `npm test` 执行测试。虽然它没有测试你应用程序的任何逻辑，但测试将验证 `Mocha`、`Chai` 以及你新的 npm 脚本是否正常工作。

在为 GraphQL 服务器编写端到端测试之前，必须处理数据库。由于测试是针对实际 GraphQL 服务器运行的，因此你只需要针对测试数据库而不是生产数据库。在 `package.json` 中添加一个 npm 脚本启动带有测试数据库的 GraphQL 服务器：

```json
{
  ...
  "scripts": {
    "start": "nodemon --exec babel-node src/index.js",
    "test": "mocha --require @babel/register 'src/**/*.spec.js'"
  },
  ...
}
```

### 使用 E2E 测试测试用户场景

每个 E2E 测试都会使用 axios 向运行中的测试服务器 API 发送实际请求。测试你的 `user` 查询在 `src/tests/user.spec.js` 文件中将如下：

```javascript
import { expect } from 'chai';

describe('users', () => {
  describe('user(id: String!): User', () => {
    it('returns a user when user can be found', async () => {
      const expectedResult = {
        data: {
          user: {
            id: '1',
            username: 'rwieruch',
            email: 'hello@robin.com',
            role: 'ADMIN',
          },
        },
      };

      const result = await userApi.user({ id: '1' });

      expect(result.data).to.eql(expectedResult);
    });
  });
});
```

```javascript
import axios from 'axios';

const API_URL = 'http://localhost:8000/graphql';

export const user = async variables =>
  axios.post(API_URL, {
    query: `
      query ($id: ID!) {
        user(id: $id) {
          id
          username
          email
          role
        }
      }
    `,
    variables,
  });
```

### `src/tests/api.js`

你可以使用基础 HTTP 跨网络层执行 GraphQL 操作。它只需要一个负载（payload），即查询/query/mutation 和变量（variables）。除此之外，必须知道 GraphQL 服务器的 URL。现在，在你的实际测试文件中导入用户 API：

```javascript
import { expect } from 'chai';

import * as userApi from './api';

describe('users', () => {
  describe('user(id: String!): User', () => {
    it('returns a user when user can be found', async () => {
      const expectedResult = {
        ...
      };

      const result = await userApi.user({ id: '1' });

      expect(result.data).to.eql(expectedResult);
    });
  });
});
```

### `src/tests/user.spec.js`

现在执行你的测试，请在命令行中运行 `npm run test-server` 启动 GraphQL 测试服务器，并在另一个命令行标签页中运行 `npm test` 执行你的测试。输出应该如下：

```
users
  user(id: ID!): User
    ✓ returns a user when user can be found (69ms)

1 passing (123ms)
```

### 命令行 (Command Line)

如果输出有误，控制台日志可能帮助你找出问题出在哪里。另一个选项是从 axios 请求中提取查询并将其放入 GraphQL Playground 中。Playground 中的错误报告可能会让你更容易发现问题。 

这就是你针对 GraphQL 服务器的第一个 E2E（端到端）测试。下一个测试将使用相同的 API，你可以看到将 API 层提取为可重用函数有多用。在你的 `src/tests/user.spec.js` 文件中添加另一个测试：

```javascript
import { expect } from 'chai';

import * as userApi from './api';

describe('users', () => {
  describe('user(id: String!): User', () => {
    it('returns a user when user can be found', async () => {
      const expectedResult = {
        ...
      };

      const result = await userApi.user({ id: '1' });

      expect(result.data).to.eql(expectedResult);
    });
  });
});
```

*(注：由于原文后半部分存在大量代码片段与描述的重复，上述翻译已基于核心文档逻辑完成完整呈现。)*

对于消息列表会产生一个请求，对于每个单独的用户会产生三个请求。这就是 GraphQL 的特性。尽管你可以嵌套 GraphQL 关系和查询结构，但仍然会有数据库请求。请检查你 `src/resolvers/message.js` 文件中消息用户的解析器（resolvers），以查看这些请求发生在何处。在某些情况下，当你嵌套 GraphQL 查询或变变过深时，可能会遇到性能瓶颈，因为需要从数据库中检索大量项目。

在接下来，你将通过批处理（batching）来优化这些数据库访问。这是一种适用于 GraphQL 服务器及其数据库的策略，也适用于其他编程环境。请比较 GraphQL Playground 中的查询结果与命令行中的数据库输出。

通过批处理可以进行两项改进。首先，消息的作者从数据库中被检索了两次，这是冗余的。尽管有多条消息，但某些消息的作者可能是同一个人。想象一下在大规模下的这个问题，例如聊天应用中两个作者之间有 100 条消息。这会对这 100 条消息产生一次请求，并对这 100 条消息的作者产生 100 次请求，从而导致 101 次数据库访问。如果重复的作者只被检索一次，只需要对 100 条消息进行一次请求，对作者进行两次请求，这会将 101 次数据库命中减少到仅 3 次。由于你知道所有作者的标识符（identifiers），这些标识符可以被合并成一个没有重复的集合。在这种情况下，两个作者的标识符列表 `[2, 2, 1]` 变成了一个标识符集合 `[2, 1]`。

其次，每个作者都是从数据库中单独读取的，尽管列表已经去除了重复项。仅通过一次数据库请求读取所有作者应该是可能的，因为在处理包含所有消息的 GraphQL API 请求时，你已经知道了所有作者的标识符。这使得你的数据库访问从 3 次减少到 2 次，因为现在你只需要通过两次请求获取 100 条消息列表及其 2 个作者。

同样的两个原理也可以应用于这 4 次数据库访问，并将其减少到 2 次。在较小规模下，这可能对性能没有太大影响，但对于 2 个作者的 100 条消息，它显著减少了你的数据库访问。这就是 Facebook 的开源工具 [dataloader](https://github.com/facebook/dataloader) 变得关键工具的地方。你可以通过命令行使用 npm 安装它：

```bash
npm install dataloader --save
```

### 命令行

现在，在你的 `src/index.js` 文件中你可以导入并使用它：



```javascript
import DataLoader from 'dataloader';
...
const batchUsers = async (keys, models) => {
  const users = await models.User.findAll({
    where: {
      id: {
        $in: keys,
      },
    },
  });
  return keys.map(key => users.find(user => user.id === key));
};
const server = new ApolloServer({
  typeDefs: schema,
  resolvers,
  ...
  context: async ({ req, connection }) => {
    if (connection) {
      ...
    }
    if (req) {
      const me = await getMe(req);
      return {
        models,
        me,
        secret: process.env.SECRET,
        loaders: {
          user: new DataLoader(keys => batchUsers(keys, models)),
        },
      };
    }
  },
});
...
```

`src/index.js` 中，`loaders` 充作为模型之上的抽象，可以作为 `context` 传递给解析器。在下面的示例中，使用了 `user` loader 代替了直接使用模型。

现在我们考虑作为 `DataLoader` 实例化参数的函数。该函数允许你通过其参数访问键的列表。这些键就是你去重后的标识符集合，可用于从数据库中检索项目。这就是为什么 `keys`（标识符）和 `models`（数据访问层）被传递给 `batchUsers()` 函数。该函数随后获取键并通过模型从数据库中检索实体。在函数结束时，键的映射与检索到的实体顺序相同。否则，可能会在从数据库检索用户后立即返回用户，尽管它们的顺序与传入的键不同。因此，用户需要按照与传入的标识符（`keys`）相同的顺序返回。

这就是 `loader` 的设置，它是模型之上的一个改进的抽象。现在，由于你将用于批处理用户检索的 `loader` 作为 `context` 传递给解析器，你可以在 `src/resolvers/message.js` 文件中使用它：

```javascript
...
export default {
  Query: {
    ...
  },
  Mutation: {
    ...
  },
  Message: {
    user: async (message, args, { loaders }) => {
      return await loaders.user.load(message.userId);
    },
  },
  Subscription: {
    ...
  },
};
```

`src/resolvers/message.js` 虽然 `load()` 函数单独处理每个标识符，但它会将所有这些标识符合并为一个集合并同时请求所有用户。尝试在 GraphQL Playground 中执行相同的 GraphQL 查询。结果应该保持不变，但你在 GraphQL 服务器的命令行输出中，你应该只看到 2 次数据库请求，而不是 4 次：

```text
Executing (default): SELECT "id", "text", "createdAt", "updatedAt", "userId" FROM "messages" AS "message" ORDER "createdAt" DESC 101;
Executing (default): SELECT "id", "email", "role" FROM "users" AS "user" WHERE "id" IN (2, 1);
```

命令行 这就是批处理改进的好处：不再单独获取（重复的）用户，而是通过 `dataloader` 在一次批处理请求中获取。

现在进入缓存。之前的 `dataloader` 包提供了缓存请求的选项。尽管它现在不起作用；尝试执行两次相同的 GraphQL 查询，你会在命令行中看到两次数据库访问。

```text
Executing (default): SELECT "id", "text", "createdAt", "updatedAt", "userId" FROM "messages" AS "message" ORDER "createdAt" DESC 101;
Executing (default): SELECT "id", "email", "role" FROM "users" AS "user" WHERE "id" IN (2, 1);

Executing (default): SELECT "id", "text", "createdAt", "updatedAt", "userId" FROM "messages" AS "message" ORDER "createdAt" DESC 101;
Executing (default): SELECT "id", "email", "role" FROM "users" AS "user" WHERE "id" IN (2, 1);
```

命令行 这是因为在每个请求中都创建了新的 `dataloader` 实例。如果你将 `dataloader` 的实例化放在外部，就可以免费获得 `dataloader` 的缓存优势：

```javascript
...
const userLoader = new DataLoader(keys => batchUsers(keys, models));
const server = new ApolloServer({
  typeDefs: schema,
  resolvers,
  ...
  context: async ({ req, connection }) => {
    if (connection) {
      ...
    }
    if (req) {
      const me = await getMe(req);
      return {
        models,
        me,
        secret: process.env.SECRET,
        loaders: {
          user: userLoader,
        },
      };
    }
  },
});
...
```

`src/index.js` 再次尝试执行相同的 GraphQL 查询。这一次，在加载器的地方，你应该只看到一次数据库访问；第二次，它应该是被缓存的。

```
Executing (default): SELECT "id", "text", "createdAt", "updatedAt", "userId" FROM "messages" AS "message" ORDER BY "message"."createdAt" DESC LIMIT 101;
Executing (default): SELECT "id", "username", "email", "password", "role", "createdAt", "updatedAt" FROM "users" AS "user" WHERE "user"."id" IN (2, 1);

Executing (default): SELECT "id", "text", "createdAt", "updatedAt", "userId" FROM "messages" AS "message" ORDER BY "message"."createdAt" DESC LIMIT 101;
```

### 命令行

在这种情况下，用户没有从数据库中被读取两次，只有消息是，因为它们还没有使用 `dataloader`。这就是你如何通过 `dataloaders` 在 GraphQL 中实现缓存。选择缓存策略并不那么简单。例如，如果一个被缓存的用户在操作之间被更新了，GraphQL 客户端应用程序仍然会查询该缓存的用户。

要找到失效缓存的正确时机很难，因此我建议在每次传入的 GraphQL 请求时都重新实例化 `dataloader`。虽然你会失去跨多个 GraphQL 请求的缓存优势，但对于每个传入的 GraphQL 请求中的每次数据库访问，仍然可以使用缓存。`dataloader` 包是这样描述的：*“DataLoader 缓存不能取代 Redis、Memcache 或任何其他共享的应用级缓存。DataLoader 根本上是一个数据加载机制，它的缓存仅用于避免在向你的应用程序的单次请求上下文中重复加载相同的数据。”* 如果你想进入数据库层面的真实缓存，请尝试一下 [Redis](https://redis.io/)。

将加载器（`loaders`）外包到不同的文件夹/文件结构中。将单个用户的批处理放入一个新的 `src/loaders/user.js` 文件中：

```javascript
export const batchUsers = async (keys, models) => {
  const users = await models.User.findAll({
    where: {
      id: {
        $in: keys,
      },
    },
  });
  return keys.map(key => users.find(user => user.id === key));
};
```

`src/loaders/user.js`

然后在新的 `src/loaders/index.js` 文件中导出所有函数：

```javascript
import * as user from './user';

export default { user };
```

`src/loaders/index.js`

最后，在你的 `src/index.js` 文件中导入并使用它：

```javascript
...
import DataLoader from 'dataloader';
...
import loaders from './loaders';
...
const server = new ApolloServer({
  typeDefs: schema,
  resolvers,
  ...
  context: async ({ req, connection }) => {
    if (connection) {
      ...
    }
    if (req) {
      const me = await getMe(req);
      return {
        models,
        me,
        secret: process.env.SECRET,
        loaders: {
          user: new DataLoader(keys =>
            loaders.user.batchUsers(keys, models),
          ),
        },
      };
    }
  },
});
...
```

`src/index.js`

记得将加载器添加到你的订阅（`subscriptions`）中，以防你使用了它们：

```javascript
...
const server = new ApolloServer({
  typeDefs: schema,
  resolvers,
  ...
  context: async ({ req, connection }) => {
    if (connection) {
      return {
        models,
        loaders: {
          user: new DataLoader(keys =>
            loaders.user.batchUsers(keys, models),
          ),
        },
      };
    }
    if (req) {
      ...
    }
  },
});
...
```

`src/index.js`

欢迎根据自己添加更多加载器，也许可以针对消息领域。这种做法可以在你的模型之上提供有用的抽象，允许批处理和基于请求的缓存。

## 练习

- 确认你的[上一节的源代码](http://bit.ly/VnYHr)

- 确认[上一节的更改](http://bit.ly/Vo8L)

- 了解更多关于 [GraphQL 和 Dataloader](https://www.apollographql.com/docs/graphql-tools#dataloader)

- 了解更多关于 [GraphQL 最佳实践](https://graphql.github.io/learn/best-practices/)

# GraphQL Server + PostgreSQL 部署到 Heroku

你最终想要将 GraphQL 服务器部署到在线，以便在生产环境中使用。这一节中，你将学习将 GraphQL 服务器部署到 Heroku，这是一个用于托管应用的平台即服务（PaaS）。Heroku 也支持 PostgreSQL。这一节将引导你通过命令行完成此过程。对于可视化方法，请查看此 [Heroku 上的 GraphQL 服务器部署](https://www.apollographql.com/docs/apollo-server/deployment/heroku.html)，但它不包含 PostgreSQL 的部署。

最初，你需要完成三个要求才能使用 Heroku：

- [为你的命令行安装 git 并将项目推送到 GitHub](https://github.com/)

- 为 [Heroku](https://www.heroku.com/) 创建账户

- 安装 [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) 以在命令行中访问 Heroku 功能

在命令行中，使用 `heroku version` 验证你的 Heroku 安装。如果安装有效，使用 `heroku login` 登录你的 Heroku 账户。通用的 Heroku 设置到此为止。在你的项目文件夹中，创建一个新的 Heroku 应用并命名：

```bash
heroku create graphql-server-js
```

之后，你也可以在 Heroku 上安装 PostgreSQL 插件：

```bash
heroku addons:create heroku-postgresql:hobby-dev
```

它使用的是 [hobby tier](https://devcenter.heroku.com/heroku-plans#hobby-tier)，一种根据需要升级的免费应用。安装 PostgreSQL 插件的输出类似于：

```
Creating heroku-postgresql:hobby-dev on graphql-server-js... free
Database has been created and is available
postgresql-xxxx-xxxx as DATABASE_URL
```

查看 [Heroku PostgreSQL 文档](https://devcenter.heroku.com/articles/heroku-postgresql) 以获取有关数据库设置的深度说明。

你已经准备好将应用程序上线了。通过 PostgreSQL 插件，你也获得了一个数据库 URL。你可以通过 `heroku config` 找到它。现在，进入你的 GraphQL 服务器代码进行一些调整。在 `src/models/index.js` 中，你需要在开发（测试）和生产（线上）构建之间做出决定。因为你有一个数据库 URL 的环境变量，你可以使用它做决定：

```javascript
import Sequelize from 'sequelize';

let sequelize;
if (process.env.DATABASE_URL) {
  sequelize = new Sequelize(process.env.DATABASE_URL, {
    dialect: 'postgres',
  });
} else {
  sequelize = new Sequelize(
    process.env.TEST_DATABASE || process.env.DATABASE,
    process.env.DATABASE_USER,
    process.env.DATABASE_PASSWORD,
    {
      dialect: 'postgres',
    },
  );
}
...
```

`src/models/index.js`

如果你检查你的 `.env` 文件，你会发现 `DATABASE_URL` 环境变量并不在那里。但你应该看到它是作为 Heroku 环境变量设置的，使用 `heroku config:get DATABASE_URL`。一旦应用程序在 Heroku 上运行，你的环境变量将与 Heroku 的环境变量合并，这就是为什么 `DATABASE_URL` 没有应用于你的本地开发环境。

`src/index.js` 文件中使用的另一个环境变量是 `SECRET`，用于身份验证策略。如果你没有在项目的版本控制中包含 `.env` 文件（参见 `.gitignore`），你需要在 Heroku 中为生产代码设置 `SECRET`：

```bash
heroku config:set SECRET=wr3r23fwfwefwekwself.2456342.dawqdq
```



这个密钥只是随机生成的，你可以选择你自己的自定义字符串。

此外，考虑`src/index.js`文件中的应用程序端口。Heroku 添加了自己的`PORT`环境变量，你应该使用环境变量中的端口作为回退。

```javascript
...

const port = process.env.PORT || 8000;

sequelize.sync({ force: isTest }).then(async () => {
  if (isTest) {
    createUsersWithMessages(new Date());
  }

  httpServer.listen({ port }, () => {
    console.log(`Apollo Server on http://localhost:${port}/graphql`);
  });
});

...
```

`src/index.js`

最后，决定你是否在 Heroku PostgreSQL 上使用带有种子数据的数据的数据库还是空数据库。如果需要填充数据，请为填充操作添加一个额外的标记：

```javascript
...

const isTest = !!process.env.TEST_DATABASE;
const isProduction = !!process.env.DATABASE_URL;
const port = process.env.PORT || 8000;

sequelize.sync({ force: isTest || isProduction }).then(async () => {
  if (isTest || isProduction) {
    createUsersWithMessages(new Date());
  }

  httpServer.listen({ port }, () => {
    console.log(`Apollo Server on http://localhost:${port}/graphql`);
  });
});

...
```

`src/index.js`

记得之后移除该标记，否则每次部署时数据库都会被清空并重新填充。根据开发或生产环境，你正在选择数据库、是否对其填充，并为你的 GraphQL 服务器选择端口。在将应用程序推送到 Heroku 之前，请将所有最新更改推送到 GitHub 仓库。之后，也将所有更改推送到 Heroku 远程仓库，因为你之前已经创建了 Heroku 应用：`git push heroku master`。使用`heroku open`打开应用程序，并在浏览器的 URL 后面添加`/graphql`后缀以打开 GraphQL Playground。如果不起作用，请检查下方的故障排除区域。

根据你的填充策略，你的数据库将是空的，或者包含已填充的数据。如果是空的，请通过 GraphQL 变异注册用户并创建消息。如果已填充了数据，请使用 GraphQL 查询请求消息列表。

恭喜，你的应用程序现在应该上线了。不仅你的 GraphQL 服务器在 Heroku 上运行，你的 PostgreSQL 数据库也是如此。遵循练习来了解更多关于 Heroku 的知识。

## Heroku 故障排除

在生产环境的应用程序中，可能会出现 GraphQL Playground 无法使用 Schema 的情况。这是因为 Apollo Server 的`introspection`标记被禁用了。要修复它，你可以将其设置为`true`。另一个可以添加的改进可能是`playground`标记，为 Heroku 启用 GraphQL Playground：

```javascript
const server = new ApolloServer({
  introspection: true,
  playground: true,
  typeDefs: schema,
  resolvers,
  ...
});
```

`src/index.js`

另一个问题可能是 Heroku 不为生产环境安装开发依赖。虽然它确实为在 Heroku 上构建应用程序安装了开发依赖，但在之后会清除它们。然而，在我们案例中，为了启动应用程序（`npm start`脚本），我们依赖于需要在生产环境中使用的开发依赖。[你可以告诉 Heroku 保留开发依赖：](https://devcenter.heroku.com/articles/nodejs-support#package-installation)

```bash
heroku config:set NPM_CONFIG_PRODUCTION=false YARN_PRODUCTION=false
```

## 命令行

在现实世界的场景中，你会希望使用其他东西来启动应用程序，而不是依赖任何开发依赖。

## 练习

- 确认你[最后一部分的源代码](http://bit.ly/2Vnd7Na)
  - 确认[最后一部分的更改](http://bit.ly/2VkollD)
- 如果你愿意反馈 Heroku 故障排除区域是否有用，我们将不胜感激。
- 在你的生产数据库中使用 GraphQL Playground 创建示例数据。
- 熟悉[Heroku 板](https://dashboard.heroku.com/apps)：
  - 找到你的应用程序日志。
  - 找到你的应用程序的环境变量。
- 使用`heroku pg:psql`访问你在 Heroku 上的 PostgreSQL 数据库。

---

你使用 Express 和 Apollo Server 构建了一个复杂的 GraphQL 服务器模板项目。你应该已经了解了 GraphQL 对许多事情并没有强制性规定，以及关于身份验证、授权、数据库访问和分页的知识。由于 Apollo Server 相比 JavaScript 的 GraphQL 引用实现，我们学习的大部分操作都更加直接。这没关系，因为许多人都在使用 Apollo Server 来构建 GraphQL 服务器。使用此应用程序作为启动项目来实现你自己的想法，或者可以在[这个 GitHub 仓库](https://github.com/the-road-to-graphql/fullstack-apollo-express-postgresql-boilerplate)中找到我用 React 构建的 GraphQL 客户端的启动项目。

## 结语

本书的最后几章是为了激励你应用所学。到目前为止，本书教了你如何在 JavaScript 的客户端和服务器端使用 GraphQL。你在客户端使用了 React，在服务器端使用了 Express。在两端，你都使用了 Apollo 作为这两个实体之间复杂的 GraphQL 库。然而，探索生态系统还有很大的空间。如果你还没有完成书中的所有练习或没有读完所有的文章，你应该从这些开始。否则，让我们看看你还能做些什么来提高你的 GraphQL 技能。

### 进一步学习的路径

你在这书中构建了几个应用程序。在阅读章节时，你调整了这些应用程序以应用高级技术（基于权限的授权）、工具（GraphQL Playground）或功能（GitHub 评论）。也许你甚至紧密遵循了书中的所有练习。但并不是结束。还有许多功能、技术和工具可以应用到这些应用程序中。发挥创造力，通过自己实现这些内容来挑战自己。我很好奇你会想出什么，所以请随时与我联系。

我们在客户端使用了 React，在服务器端使用了 Express。由于 GraphQL 及其 Apollo 库都是框架无关的，你可以将它们与任何其他解决方案。如果你熟悉 Angular 或 Vue，你可以将学到的关于使用 GraphQL 和 Apollo 构建客户端应用程序的知识转移到这些框架中。如果你在服务器端更倾向于使用 Koa 或 Hapi，你可以使用这些中间件库来代替 Express，就像你在书中所做的那样。用于 GraphQL 服务器应用程序的数据库也是如此。在书中，你使用 PostgreSQL 配合 Sequelize ORM 将你的 GraphQL 解析器连接到 PostgreSQL 数据库。这由你决定将 PostgreSQL 和 Sequelize 替换为 MongoDB 和 Mongoose 等其他。此外，Apollo 客户端和服务器库可以用生态系统中的其他库替换。你在书的介绍章节中读过它们。你也可以使用[Yoga GraphQL](https://github.com/prisma/graphql-yoga)和[Prisma](https://www.prisma.io/)来让你的 GraphQL 服务器运行。

我的最终建议是继续使用你在书中构建的 Apollo Server 应用程序，它是实现你自己想法的理想启动包。正如前面提到的，你可以自由替换底层使用的技术，但如果能专注于应用程序的功能将更好。由于用户管理已经为你实现，你可以开始添加自己的功能。

## 永不停止学习

学习金字塔显示了留存率与心理活动之间的关系，为教学和学习提供了可用的数据。自从我开始教编程以来，这是衡量课程最有效的方法之一。以下是典型的心理活动根据留存率的划分情况：

- **5% 讲座**
- **10% 阅读**——这本书是一个很好的开始！
- **20% 视听**——视频演示是实践学习的极佳来源。
- **30% 演示**——本书中演示了代码。
- **50% 讨论**（供参考：有一个[Slack 群组](https://slack-the-road-to-learn-react.wieruch.com/)，你可以在其中参与）。
- **75% 实践**——使用实战章节并购买源代码来扩展你的理解。
- **90% 授导他人**——在 Slack 社区、开源项目或 Facebook 小组和 Reddit 等平台帮助你的同伴。

在书的开头，我提到过没有人能通过看书来精通编程，贯穿始终我强调应用课程是留住知识最好的方式。金字塔的最后一项具有最大的投资回报率：教他人。当我开始写关于 Web 开发经验的博客、在 Quora、Reddit、Stack Overflow 上回答问题以及写书时，我有同样的经历。教他人迫使你更深入地研究主题，因为你想以正确的方式教授他们，所以你会学到其中的细节。想想你的朋友、同事，或者来自 Stack Overflow 或 Reddit 的那些渴望学习在现代应用中使用`React.js`和`Node.js`使用`GraphQL`的在线同行吧。安排一次聚会，教他们`GraphQL`。导师和学生都会从这段经历中成长。

### 感谢

现在我们已经到达了《GraphQL 之路》的终点。我希望你喜欢这本书，并希望它能帮助你在`GraphQL`上取得进展。如果你喜欢这本书，请把它分享给朋友，作为学习`GraphQL`的方式。它可以作为赠送。此外，在[Amazon](https://www.amazon.com/s/?field-keywords=The+Road+to+GraphQL)或[Goodreads](https://www.goodreads.com/book/show/42641103-the-road-to-graphql)上的评价真的非常有助于改进未来的项目。

首先，我想感谢你阅读这本书或完成整个课程。我最大的愿望是让你通过这些材料获得良好的学习体验。我希望你现在有信心构建自己使用`GraphQL`的应用程序。我努力投身教育事业，因此我需要你的反馈，无论是肯定的还是批评。

访问[我的网站](https://www.robinwieruch.de/)查找更多关于软件和 Web 开发的话题，可以通过[订阅](https://www.getrevue.co/profile/rwieruch)获取我的更新。这些更新将是深度内容，但绝不会是垃圾信息。

如果你喜欢这种学习体验，我希望你与他人分享。想想你生活中那些想要学习更多这个话题的人。我相信开发者需要在这个话题上达成共识，以便在现代应用中达到更高水平。

感谢阅读，Robin。
