# Developing a hapi Edge：用于应用程序和服务的丰富 Node.js 框架






- 代码检查 134
- 插件测试 135
- 小结 135

## 第 11 章：调试 137

- 本章概览 137
- console.log 138
- 调试模式 139
- TV 140
- Good 141
- REPL 142
- 堆快照 143
- 核心文件 144
- 小结 145

## 第 12 章：安全 147

- 最佳实践 147
- 密码哈希：BCrypt 148
- XSS 149
- CSRF 150
- SSL 151
- 请求头剥离 152
- contentSecurityPolicy 153
- CORS 154
- crossdomain.xml 155
- 小结 155
- 复习 156

## 第 13 章：附录 157

- 模型 157
- 历史 158
- HTTP 客户端概览 160
- 数据库客户端概览 165
  - 连接 166
  - Postgres::Sequelize 168
  - 模式 171
  - MongoDB::mongodb 171
  - MongoDB::Mongoose 172
  - Cassandra::Apollo 173
- 模板引擎 173
  - 所选模板引擎概览 173


## 一个让你感到 hapi 的框架

从一开始，hapi 就围绕一个简单的理念构建——开发应该充满乐趣。框架的作用是提高你的生产力，在你想要的时候介入，但在你不需要的时候就应该让开。它不应该干扰你的环境，也不应该剥夺底层平台提供的任何能力。但更重要的是，框架的作用是建立协作的基础。

企业软件开发因其痛苦、官僚主义、陈旧和复杂的过程而声名狼藉。更糟糕的是，我们已经学会了将其视为常态。问题的核心在于，企业软件开发通常发生在大型团队中，这些团队在组织和地理上往往是分散的，并且需要大量的流程来防止一个错误影响数百名开发者的生产力，或者更糟的是影响业务运营。

当我着手构建 hapi 时，我知道这个框架必须在处理典型的 Web 应用程序活动（如身份验证、状态和缓存）方面表现出色，但这些都只是成为一个竞争者的先决条件。框架的真正核心在于其旨在使大规模开发更容易、更有趣的功能。这意味着关注小细节，比如保护开发者免受路由、cookie 或其他命名属性中的冲突，以及大细节，比如如何允许团队在同一个应用程序上工作而无需持续协调。

随着项目的成熟，hapi 本身也成为了大规模开发流程的一部分。随着来自许多不同公司的数十名贡献者和不断增长的代码库，我们必须将我们的 hapi 中心理念扩展到整个开发流程。我们高度重视代码质量和一致性，由于编写测试通常是软件开发中痛苦的部分，我们努力使其变得更好、更精简、更愉快。我们编写了新的测试工具，加强了编码风格，并将许多繁琐的部分自动化。我们对文档也做了同样的事情，尽可能地自动化流程，让开发者能够专注于功能。

项目进行四年后，社区的满意度仍然是推动工作前进的最大动力和指导。随着它的持续成熟，我们每天都在了解它的使用情况以及我们可以如何继续发展它；hapi 是一个动态的



 # 前言

社区和这个项目有不惧打破常规、追求卓越的传统。我们拒绝安于现状，哪怕是我们自己创造的现状。

我很兴奋你能花时间了解 hapi 并考虑将其用于你的下一个项目；hapi 是一个社区项目，你现在就是其中的一员。你的声音和快乐很重要，请把这视为你的私人邀请，加入我们，提出问题，并与我们分享如何让一切变得更好。

Eran Hammer

2015 年 7 月

# 序

## 为什么要用 hapi？

> "一个用于构建应用程序和服务的丰富框架，hapi 让开发者能够专注于编写可复用的应用逻辑，而不是把时间花在构建基础设施上。"

—— **hapijs.com**

hapi 是一个 Web 开发框架，专为使用 JavaScript 快速开发 RESTful 服务 API 而设计。虽然它简单易用，但 hapi 还包含了许多开箱即用的功能，这些功能通常来自第三方工具，例如输入验证、缓存、身份验证等。

开发者使用 hapi 是因为它易于使用、稳定、健壮、经过良好测试（并且在 WalmartLabs 的黑五大促期间经受了实战考验），而且功能强大。它专门为多团队协作的企业环境而设计，多个团队可以各自开发独立或重叠的模块，最终将其连接在一起。hapi 通过让开发者专注于编写可复用、模块化的代码来实现这一点，同时不会强迫他们以非常狭隘的方式来做到这一点。

## 阅读本书之前你应该了解什么？

读者应该熟悉 JavaScript、Node.js，以及基本网站和 Web 应用程序的设计与实现。

## 源代码/示例应用

在全书中，我们将引用来自示例应用程序 hapi-plugins.com 的代码。hapi-plugins.com 是一个可搜索的 hapi 相关模块仓库，托管在 NPM 上。你可以在 https://github.com/hapijs-edge/hapi-plugins.com 查看完整的源代码。你可以在 https://hapi-plugins.com 查看完整的应用程序。

## 这本书将教会你什么？

这本书将教你如何使用 hapi 构建出色的 Web 应用程序。它涵盖了 hapi 工作方式的诸多方面，包括其背后的原理。你将看到诸如身份验证、验证、缓存、模板、测试和调试等有用且高级的功能。在本书中，你还将逐步创建一个功能完备的 hapi Web 应用程序。

## 作者

**Daniel Bretoi**

Daniel Bretoi 是 @WalmartLabs 的承包商，曾在 Eran Hammer 的团队工作，该团队开发了 hapi 框架。他在行业内工作了 15 年，偏爱解释型语言。2002 年，他早期就采用了 Ruby，并且通常乐于接受新技术。

**Wyatt Preul**

Wyatt Preul 是 Walmart 的软件开发者。他是 hapi Node.js 框架的核心维护者之一。在 Walmart，Wyatt 是如今臭名昭著的 Node.js 内存泄漏事件的调查者之一。除此之外，他还帮助在 Walmart 内部交付了许多 Node.js 项目。除了日常工作，Wyatt 热爱一切与 Node 相关的事物、Web 应用安全、射箭、咖啡烘焙和啤酒酿造。

**Van Nguyen**

Van Nguyen 是 Intuit 的高级软件工程师，全栈，IDEA（大数据）。他目前正在用 JavaScript 开发用于管理和可视化大数据的用户界面。

**Lloyd Benson**

Lloyd Benson 是 Walmart 的顾问。他也是 Open Source Infrastructure LLC 的所有者。

## 技术审校者

我们要感谢以下技术审校者提供的早期反馈和细致的批评意见：Doron Pagot、Troy Whiteley、Jeffrey Jagoda、Colin Ihrig、Daniel Barnes、Michael Caputo、James Butler、Alvin Teh、Josh Mock、Michael Parks、Jonathan Holmlund、Glenn Jones 和 Jesse Newcomer。

# hapi 简介 1

#### 历史

hapi 的起源可以追溯到 2010 年末雅虎的一个名为 Sled 的项目。Sled 是由 Eran Hammer 发起的一个协作式清单工具，作为探索"通过限制实现赋能"的实验而编写。Sled 使用 node 编写，Eran 爱上了这项技术。Sled 最终被关闭，并于 2011 年 8 月由雅虎慷慨地开源为 Postmile。想要继续深耕 node 的 Eran 随后前往沃尔玛，他带走了 Postmile 的精华部分，*hapi 于 2011 年 8 月 5 日诞生*。受命于开发 Web 服务层，hapi 在沃尔玛继续发展。hapi 的早期版本使用了 Express 框架。然而，人们逐渐意识到 Express 存在局限性，无法满足沃尔玛面临的特定需求。虽然 Express 很棒，但它缺少很多东西，hapi 逐渐演变为一个独立的框架。

hapi 这个名字来自 HTTP API server，一旦这个名字被念出来，就与《莱恩和史丁比》产生了联系，这是卡通频道的一部邪典卡通。在 hapi 的许多早期演示中，"Happy Happy Joy Joy Song" 都被作为特色曲目。

怀着《莱恩和史丁比》的主题，hapi.js 框架中的其他工具也开始以各种方式引用这部动画，最终目标是让编程变得有趣——我们程序员在写代码时可以有点傻气，即使我们被置于大型企业环境中。放轻松，享受一点乐趣。

在功能方面，hapi 的设计旨在防止当时其他框架中反复出现的问题。这些问题包括：中间件顺序问题、缺乏隔离性、路径匹配缓慢、可测试性不足，以及缺少常用的内置功能。中间件顺序问题通过 hapi 的**请求生命周期**得以解决，它提供了受控的、依赖映射的钩子点，贯穿请求从到达服务器到向用户返回响应的整个生命周期。缺乏隔离性的问题最初通过域（domains）解决，后来被一个更好的系统所取代。hapi 中的路径匹配为速度和灵活性而构建。hapi 代码从头到尾都是可测试的（而且其自身也经过了良好的测试！）。最后，通过 hapi.js 生态系统（https://github.com/hapijs），有数十个官方 hapi 插件，它们像 hapi 本身一样健壮、经过良好测试且灵活。这还不包括 NPM 上数以百计的社区模块。

hapi 完全以开源方式设计和构建，也为开源项目树立了非常高的标准。从极其完整的代码覆盖率（这一流程从一开始就因 Wyatt Preul 的努力而根深蒂固），到令人难以置信的详细发布说明和有条理的文档，任何使用 hapi 及其相关模块的人都可以信赖它能可靠工作且行为符合预期。

hapi 拥有数量惊人的满意用户——其中最重要的就是 WalmartLabs 本身，它引以为豪的是拥有世界上最大的 Node.js 部署规模，这要感谢黑色星期五。

有很多理由使用 hapi。试一试，你就会发现用 Node.js 开发 Web 应用程序可以是多么愉快的体验。

> hapi 能够用大约 10 个 CPU 核心和 28GB 内存处理所有沃尔玛移动端的黑色星期五流量（当然我们使用了更多资源，但它们大部分时间都处于空闲状态，负载仅为 0.75%）。以极少的资源处理如此惊人的流量，令人难以置信。—— Eran Hammer，https://github.com/hapijs/hapi/issues/1326

## 本书概览

本书将带你经历使用 hapi 开发基本 Web 应用程序的过程。我们将构建一个可搜索的 hapi 插件仓库。在线演示可在 hapi-plugins.com 查看。

前七章都是关于创建和配置 hapi 服务器的。这些章节还涵盖了更多相关的信息，以防你需要构建或使用 hapi-plugins.com 中没有的功能。接下来的两章（8、9）涵盖如何获取数据、处理数据和格式化数据。最后三章（10、11、12）涵盖一些更高级的主题，包括一些非常实用的行业最佳实践。

- 1. 简介

  第一章介绍 hapi、本书概览、编码风格指南，以及演示应用程序的简短演练。



2. 服务器

本章重点介绍 hapi 服务器的配置。同时涵盖了常用的最佳实践、示例，以及如何在请求生命周期中进行定制。

3. 路由

路由将 URI 映射到代码。在本章中，你将深入理解如何匹配复杂的模式。

4. 处理程序

处理程序是负责接收用户请求并返回响应的函数。在本章中，你将了解 hapi 响应请求的所有不同方式。

5. 验证

验证（通过 Joi）是 hapi 另一项令人惊叹的实用功能。本章展示了验证功能是多么强大，以及它如何能让开发者的生活更轻松。

6. 插件

插件是"正确"的中间件。本章将向你展示插件如何使跨职能、远程团队协同工作，而不会导致通常与中间件相关的任何问题。

7. 认证

本章提供了详尽的逐步指导，介绍如何启用认证和设置 Cookie。

8. 模型

本章介绍了如何接入第三方 RESTful API 以用于你的 hapi Web 应用程序。然后，它还介绍了如何接入 MongoDB 数据库以用于你的 hapi Web 应用程序。此外，还展示了如何在另外两个流行的数据库（Cassandra 和 PostgreSQL）中进行操作的示例。

9. 模板

在本章中，你将了解如何在处理程序的响应中将数据与表现层分离。

10. 测试

测试常常被误解或难以学习。本章将赋予你为你的 Web 应用程序添加测试的能力，从而提高健壮性和代码质量。

11. 调试

本章介绍了我们在运行全球最大的 Node.js 部署之一时积累的一些来之不易的调试技巧。在本章中，你将学习如何检查运行中的服务、跟踪统计信息、追踪内存泄漏，以及识别其他问题。

12. 安全

本章涵盖了关于保护 Web 应用程序的一些行业最佳实践。

## 第1章：hapi 简介

13. 附录

本章作为附录，收录了其他选定数据库和模板引擎的描述与代码示例。

## hapi-plugins.com

![hapi-plugins.com](img/79450811086e2fc8749ec4d309ea2b79_17_0.png)

在本书中，我们将介绍如何使用 hapi 为真实的（但基础的）Web 应用程序 hapi-plugins 创建后端服务。hapi-plugins（[hapi-plugins.com](https://hapi-plugins.com)）是一个可搜索的仓库，用于查找 NPM 上可用的 hapi 相关模块。

本书**不会**涵盖如何构建应用程序的客户端 JavaScript 部分。然而，完整的**源代码**可在 **GitHub** 上获取。

## 风格

我们将在整本书中遵循 hapi 风格指南。想了解更多信息，可以查看 **hapi 风格指南**。

我们可能不完全认同风格指南中的所有内容，但值得注意的是，仅仅拥有这份可供遵循的风格指南就能避免耗费时间在讨论上。它有 99% 是好的。有些实践可能看起来有些奇怪，但它确实有助于代码的可视化。我们建议不仅在 hapi 相关项目中选择这种风格，对于一般的 node 开发也是如此。

在风格方面，我们对指南的执行是严格而不懈的。风格本应是编程中最容易遵循的概念之一，然而我们发现很多人会疏忽大意。如果你连简单的事情都无法遵循，那就表明你没有注意到自己在做什么。因此，我们逐渐形成了这样的观念：代码离风格越远，在代码审查时就需要越仔细地审查。

最终我们得到了全书清晰简洁的代码（这本身就是一件幸事），我们在代码审查中也非常密切地关注任何不协调之处。这迫使我们逐行扫描。这是件好事，因为它不仅能帮助我们在较大规模上发现异常，还能发现较小的 bug。

## 总结

话不多说，让我们在下一章开始了解 hapi 服务器。

## 服务器 2

hapi 是一个用于构建应用程序和服务的框架。在每个服务的背后，都有一个服务器；它是为客户端需求提供服务的东西。hapi 的核心本质上是 HTTP 服务器的超集。hapi 周围的 everything 都与这一事实紧密相连，因此我们以主要功能开始本书。其他一切都是从此配置并发挥作用的。我们将讨论许多与服务器相关的概念，如插件、处理程序、测试等。

在本章中，我们将介绍如何设置服务器，以及我们如何为 hapi-plugins.com 示例设置服务器。我们将教你 hapi 框架中服务器的方方面面。你将学习在生产环境中运行 hapi 服务器的不同方式。你将了解如何设置缓存。你将初步了解插件以及如何添加在整个应用程序中可用的方法。最后，你将了解请求生命周期以及如何为你的应用程序添加自定义函数。

## 设置一个简单的服务器

当然，我们不能在没有 Hello World 示例的情况下就开始写一本书。好吧，实际上我们可以，但我们不会这样做。在进阶到更复杂的配置之前，了解如何以最简单的配置设置服务器是很重要的。

```javascript
var Hapi = require('hapi');

var server = new Hapi.Server();

server.connection();

server.route({
    method: 'GET',
    path: '/',
    handler: function (request, reply) {

        return reply('hello hapi');
    }
});

server.start(function (err) {

    console.log(server.info.uri);
});
```

这里我们创建了一个 hapi 服务器实例。实际上我们完全不需要对其进行任何配置。下一步是获取与服务器的连接。连接是服务器正在监听的端口和主机。默认情况下，主机设置为 `localhost`，端口则随机生成，基于不需要系统管理员权限即可使用的可用端口。由于我们不知道端口是什么，我们在最后打印出 URI，以便查看服务器正在哪里监听。

我们添加了一个路由，这样我们就有了可以发送请求的地方。我们将在第 3 章更深入地了解路由，但现在，可以把路由看作客户端（浏览器）请求可以走的配置路径，以便获得特定的响应服务。

此时我们启动服务器，并记录服务器 URI，以便知道服务器启动在哪个端口上。

接下来的逻辑步骤是为我们的服务器设置一个固定的启动端口，这样每次都知道是相同的。这可以通过连接的选项来实现：`server.connection({ port: 8088 });`

## 为 hapi-plugins.com 设置服务器

现在我们对如何设置服务器有了更基本的了解，让我们看看需要做什么来为 hapi-plugins.com 设置服务器。

单页应用程序（SPA）的典型架构是通过前端框架（如 Ember、AngularJS、React 等）提供 HTML 模板。我们选择使用 React 作为前端。提供给框架的信息可以使用相同的后端方法来提供数据，但更清洁的做法是让单独的 API 服务器处理数据，这正是我们决定采用的方法。

```javascript
var internals = {
    servers: {
        http: {
            port: 8080,
            host: '0.0.0.0',
            labels: ['http']
        },
        api: {
            port: 8088,
            host: '0.0.0.0',
            labels: ['api']
        }
    },
    options: {
        files: {
            relativeTo: __dirname
        }
    }
};
```

我们将主 HTTP 服务器放在 8080 端口，API 服务器放在 8088 端口。它们都在 `0.0.0.0` 上运行和监听，用于绑定到所有 IP 地址的连接。当服务器启动时，这将只运行一个 node 进程。配置中的 labels 用于标记连接，以便加载适当的插件。hapi 是一个以插件为中心的框架，意味着一切设计都围绕插件架构。你可以在第六掌了解更多关于插件的细节，但现在，让我们认识到这是一个重要的概念。服务器上所有可用的方法在传递给插件的任何对象上也可用。它是传递给插件注册对象的第一个参数。有时参数名是 `plugin`，其他时候是 `server`。我们将它称为 plugin。

对于 hapi-plugins.com，我们为服务器设置两个连接。一个用于 HTML 内容，另一个用于我们的 API 内容。

```javascript
var Async = require('async');
var Bell = require('bell');
var Blipp = require('blipp');
var Hapi = require('hapi');
var HapiAuthCookie = require('hapi-auth-cookie');
var Hoek = require('hoek');
var Api = require('./api');
var Authentication = require('./authentication');
var Controllers = require('./controllers');
var Models = require('./models');
var Routes = require('./routes');

var internals = {
    servers: {
        http: {
            port: 8080,
            host: '0.0.0.0',
            labels: ['http']
        },
        api: {
            port: 8088,
            host: '0.0.0.0',
            labels: ['api']
        }
    }
```



## 第 2 章：服务器

```
    },
    options: {
        files: {
            relativeTo: __dirname
        }
    }
};

exports.init = function (callback) {

    var server = new Hapi.Server();
    server.connection(internals.servers.http);
    server.connection(internals.servers.api);
    //...
};
```

我们首先加载将要使用的库。我们将代码组织为模型（Models）、路由（Routes）和控制器（Controllers）。我们还为 API 编写了专门的代码。
这里的新内容是标签（labels）。它们作为系统的指示符，可用于后续决定为每个连接加载哪些插件。我们可能会让某些插件仅监听一个连接而不监听另一个。有些插件可能希望同时监听两者，例如 `/heartbeat` 类型的调用，但通常情况下，除非一个是仅使用 SSL/TSL 而另一个未加密，否则重复内容应该很少。您可以在第 6 章中阅读更多关于如何选择插件以及如何管理插件的内容。这是通过 `server.register()` 完成的。

```
server.path(internals.options.files.relativeTo);

server.on('request-error', function (request, response) {
    console.log('request-error:');
    console.dir(response);
});
```

`server.path` 向 hapi 指明一个路径前缀，以便我们可以使用相对路径来定位文件和模板。
我们还设置了一个事件来处理请求中发生的错误。

```
var registerHttpPlugins = function (next) {
    server.register([
        Bell,
        Blipp,
        HapiAuthCookie,
        Authentication,
        Controllers,
        Models,
        Routes
    ],
    { select: 'http' },
    function (err) {

        return next(err);
    });
};
```

```
var registerApiPlugins = function (next) {

    server.register([
        Blipp,
        Controllers,
        Models,
        Api
    ],
    { select: 'api' },
    function (err) {

        return next(err);
    });
};
```

```
Async.auto({
    http: registerHttpPlugins,
    api: registerApiPlugins
}, function (err, data) {

    if (err) {
        console.log('server.register err:', err);
        return callback(err);
    }

    server.start(function () {

        return callback(null, server);
    });
});
```

```
exports.init(Hoek.ignore);
```

一次性吸收这么多代码量很大，但它们都是相关的，所以请耐心听我们解释想要实现的目标。首先，目标是注册我们的插件并启动服务器。我们采用插件化架构来组织代码，以便将其分解为可管理的块。其中一些内容可能比较陌生，但在本章和接下来的章节中会变得清晰。

既然知道了目标，让我们看看是如何实现的。`registerHttpPlugins` 和 `registerApiPlugins` 是用于处理服务器上两个独立连接的插件注册函数。一个函数一次只能将插件应用于一个连接。因此，由于我们配置 hapi 拥有两个连接，我们需要区分这两个函数。

我们使用 `Async.auto` 来异步完成此操作，这样做是可行的，因为插件注册的顺序并不重要。如果您不熟悉 **Async** 库，它是一个非常出色的工具，我们在到处使用它来使代码更简洁。值得在这里停下来休息一下，查阅 **Async** 的文档以熟悉它。我们会等您的。

如果出现错误，我们将错误打印到控制台并退出。如果没有错误，我们就继续启动服务器。

请注意，`server.register` 可以接收一个插件数组。这种行为类似于 [Async].series。事实上，hapi 内部使用了一个名为 **items** 的轻量级 Async 版本。如果您发现自己没有用到 Async 的所有功能，那么这可能是一个不错的替代方案。

如您所见，设置服务器可能相当麻烦。有很多东西需要跟踪。然而，有一种更简洁的方法。接下来，我们将 살펴一下 `glue`、`rejoice` 和 `confidence` 模块。

## Glue

**Glue** 是一种组合服务器设置的方法。通常希望将服务器配置与代码分离，因为这样更可预测。

我们上面所写的是一套相当复杂的设置。为了简化，我们将使用 `glue`。下面是具体做法。

```
// Load modules

var Glue = require('glue');
var Hapi = require('hapi');


// Internals

var internals = {
    manifest: {
        connections: [{
            port: 8080,
            labels: ['http']
        },
        {
            port: 8088,
            labels: ['api']
        }
    }],
    plugins: {
        bell: [{ 'select': 'http' }],
        blipp: [{}],
        'hapi-auth-cookie': [{ 'select': 'http' }],
        './authentication': [{ 'select': 'http' }],
        './controllers': [{ 'select': ['http', 'api'] }],
        './models': [{ 'select': ['http', 'api'] }],
        './routes': [{ 'select': ['http'] }],
        './api': [{ 'select': ['api'] }],
        good: {
            opsInterval: 5000,
            reporters: [{
                'reporter': 'good-console',
                'events': { 'ops': '*', 'log': '*' }
            }]
        }
    }
};
```

```
Glue.compose(internals.manifest,
    { relativeTo: __dirname }, function (err, server) {

    if (err) {
        console.log('server.register err:', err);
    }
    server.start();
});
```

这是包含所有 `require` 的完整服务器文件。如您所见，它更容易理解和跟踪。之前在使用 glue 之前，我们需要定义两个函数将插件应用于每个连接（http 和 api）。而使用 glue，我们在一个地方定义所有插件，并为每个插件提供一个包含连接的数组。Glue 将根据定义自动将插件应用于正确的连接。

## Rejoice

**Rejoice** 是一个命令行（CLI）工具，用于通过纯 JSON 配置启动 hapi 实例。这个模块被拆分了出来，之前它在 hapi 内部作为 `bin/hapi` 存在。它非常简单直接。既然我们已经学习了 glue 组合是如何工作的，您只需要前面提到的 manifest 的 JSON 结果即可。结果如下：

```
{
    "connections": [{
        "port": 8080,
        "labels": ["http"]
    },
    {
        "port": 8088,
        "labels": ["api"]
    }],
    "plugins": {
        "bell": [{ "select": "http" }],
        "blipp": [{}],
        "hapi-auth-cookie": [{ "select": "http" }],
        "./authentication": [{ "select": "http" }],
        "./controllers": [{ "select": ["http", "api"] }],
        "./models": [{ "select": ["http", "api"] }],
        "./routes": [{ "select": ["http"] }],
        "./api": [{ "select": ["api"] }],
        "good": {
            "opsInterval": 5000,
            "reporters": [{
                "reporter": "good-console",
                "events": { "ops": "*", "log": "*" }
            }]
        }
    }
}
```

由于这是一个 JSON 文件，我们使用了双引号。假设您已经在本地安装了 rejoice，您可以使用 `rejoice -c example.json` 来启动它。能够使用单个 JSON 文件工作很方便，但您可能会发现，根据环境的不同，您希望采取不同的做法。这就是 `confidence` 的用武之地。

## Confidence

**Confidence** 是另一个命令行（CLI）工具。您可以拿一个 JSON 文件并对其应用过滤器，从而处理该文件。为每个环境管理多个文件不仅繁琐，而且容易出错。您可能会在其中一个文件中添加新设置，但忘记添加到其他文件中。这会导致配置漂移（configuration drift）问题，而使用 `confidence`，您可以“自信”地拥有一个作为唯一事实来源（source of truth）的位置。让我们看看我们的 rejoice 文件，并应用可以通过 `confidence` 生成的过滤器。

```
{
    "connections": [{
        "port": 8080,
        "labels": ["http"]
    },
    {
        "port": 8088,
        "labels": ["api"]
    }],
    "plugins": {
        "$filter": env,
        "$base": {
            "bell": [{ "select": "http" }],
            "hapi-auth-cookie": [{ "select": "http" }],
            "./authentication": [{ "select": "http" }],
            "./controllers": [{ "select": ["http", "api"] }],
            "./models": [{ "select": ["http", "api"] }],
            "./routes": [{ "select": ["http"] }],
            "./api": [{ "select": ["api"] }],
            "good": {
                "opsInterval": 5000
            }
        },
        "dev": {
            "blipp": [{}],
            "good": {
                "reporters": [{
                    "reporter": "good-console",
                    "events": { "ops": "*", "log": "*" }
                }]
            }
        },
        "prod": {
            "good": {
                "reporters": [{
                    "reporter": "good-file",
                    "events": { "log": "*" },
                    "config": "/path/to/log.log"
                },
                {
                    "reporter": "good-file",
                    "events": { "ops": "*" },
                    "config": "/path/to/ops.log"
                }]
            }
        }
    }
}
```

在这里，您可以为 `dev` 和 `prod` 关键字设置过滤器。为了生成一个以后可以用在 rejoice 中的 JSON 文件，您可以运行：`confidence -c confidence.json --filter.env=dev > rejoice.json`。这将导致 `$base` 中的内容与 `dev` 的特定条目合并。在这种情况下，您只在开发环境中需要 `blipp` 和 `good-console`，因为它们对调试很有帮助。但在生产（prod）环境中您不需要这些。对于生产环境，您添加了



## 第 2 章：服务器

ed `good-file` 将你的输出记录到文件中，随后可以将其处理到日志聚合器中（见第 11 章的讨论）。要生成 `prod` 配置文件，你可以执行与之前相同的 confidence 命令，但将过滤器更改为 `--filter.env=prod`。在部署期间，临时生成该文件通常很方便，只需在启动服务器之前确保有某些有效的输出即可。无效的 JSON 将导致错误。此外，你会发现 `$base` 中的 `opsInterval` 设置将同时合并到这两个过滤器中。

Confidence 还能实现更多功能，但这足以让你为 hapi 服务器拥有一套统一的配置，从而轻松维护你的环境。将 `confidence` 与 `rejoice`（它使用了 `glue`）结合使用，将使你不断变化的环境需求变得易于管理。

### 服务器方法 (Server methods)

你可能希望注册一些在服务器上随处可用的方法以供访问。正如这里所示，这样做非常简单。

```javascript
server.method('spumko', function (next) {

    console.log('the hapijs project was');
    console.log('originally called spumko');
    return next(null, 'called');
});
```

随后可以通过 `server.methods` 对象访问这些服务器方法。

```javascript
server.methods.spumko(function (err, result) {

    console.log(result); // prints "called"
});
```

如果你不希望你的方法需要回调函数，可以通过其中一个选项来切换此行为。

```javascript
server.method('spumko', function (arg) {

    console.log('the hapijs project was');
    console.log('originally called spumko');

    return 'called';
}, { callback: false });
```

```javascript
console.log(server.methods.spumko()); // prints "called"
```

可用的其他选项包括 bind、cache 和 generateKey。

bind 用于设置方法的上下文，默认值为方法创建时的上下文。如果你需要其他上下文，可以在这里进行设置。

cache 具有相同的配置，将在“配置缓存”章节中讨论。

最后，generateKey 是一个用于创建缓存唯一键的函数。

### 装饰服务器 (Decorating the server)

使用 `server.decorate`，你可以直接向服务器对象添加函数。这与 `server.method` 不同，后者是将方法添加到通过 `server.methods` 访问的集合中。除了装饰服务器对象外，你还可以装饰响应（reply）对象，我们将在第 4 章中专门讨论这一点。

```javascript
server.decorate('server', 'success', function () {

    return this.response({ success: true });
});
```

### 配置缓存 (Configuring for caching)

我们可以使用 `server.cache` 来设置缓存。hapi 拥有内置的服务器缓存设施，它依赖于 hapi 插件 **catbox**。默认情况下，有一个内置的内存缓存 **catbox-memory**，但也支持其他类型的缓存引擎，如 redis、mongoDB、memcached 等。有关这些策略的更多详细信息，请参阅 catbox 文档。以下是如何使用 `server.cache` 的简单示例。

```javascript
var cache = server.cache({
    segment: 'plugins',
    expiresIn: 60 * 60 * 1000
});

cache.set('pluginName', { author: 'mindy' }, null, function (err) {

    cache.get('pluginName', function (err, value, cached, log) {

        // value === { author: 'mindy' };
    });
});
```

在这里，我们设置了一个缓存，分段（segment）为 `plugins`。分段用于在缓存分区内隔离缓存项。当你在插件中调用此功能时，它默认为 `!name`，其中 `name` 是插件的名称。

我们还有一个 `expiresIn` 设置，用于将缓存项的过期时间设置为一小时。还有一个有趣的设置叫作 `staleIn`，你可以用它将存储在缓存中的项标记为“陈旧（stale）”。此设置必须小于 `expiresIn`。利用此功能，你可以在 `expiresIn` 到来之前就让缓存准备就绪。如果 `staleIn` 在达到 `expiresIn` 之前没有足够的时间，它将像普通的 `expiresIn` 一样工作。这就像是在预热你的缓存。

最后，你可以看到我们使用 `cache.set()` 将键 `pluginName` 设置为 `author` 对象的值，并且可以使用 `cache.get()` 方法检索该值。

`server.cache` 还有更多选项，欲了解更多详情请访问 [hapijs.com 文档](http://hapijs.com)。

### 请求生命周期 (Request lifecycle)

了解一项技术如何处理 HTTP 请求，是使用该技术开发安全、高效应用程序的基础。Node.js 本身在这方面提供的功能不多，尽管在 Node.js 中创建服务器相当简单：

```javascript
var server = require('http');

server.on('request', function (request, response) {
    // do something
});

server.listen(80);
```

就这样，只有一个函数。请求（request）包含了来自请求源的所有入站信息，而响应（reply）则是一个可写流，需要设置响应头、写入信息，然后关闭连接。起初这可能令人兴奋，尤其是对于那些以前没有处理过此项工作的人。然而，一旦应用程序需要路由表，处理起来就会变得复杂得多。

hapi 处理请求的方式是：每次服务器接收到请求时，都会触发一系列可靠的事件。以下是完整的生命周期：

- **'onRequest' 扩展点**
  - 总是被调用
  - 传递给扩展函数的请求对象被装饰了 `request.setUrl()` 和 `request.setMethod()` 方法。调用这些方法将影响请求的路由方式，可用于重写规则。
  - 此时 `request.route` 尚未填充。
  - 由于尚未匹配路由且 JSONP 配置不可用，因此从该扩展点返回的任何响应都将忽略 JSONP 配置。
- 使用请求路径查找路由 (Lookup route using request path)
- 解析 Cookie (Parse cookies)
- 'onPreAuth' 扩展点
- 请求认证 (Authenticate request)
- 读取并解析 Payload (Read and parse payload)
- 请求 Payload 认证 (Authenticate request payload)
- 'onPostAuth' 扩展点
- 验证路径参数 (Validate path parameters)
- 处理查询扩展（例如 JSONP）(Process query extensions)
- 验证查询 (Validate query)
- 验证 Payload (Validate payload)
- 'onPreHandler' 扩展点
- 路由预置条件 (Route prerequisites) —— 在 Handler 中配置
- 路由处理器 (Route handler)
- 'onPostHandler' 扩展点
  - `request.response` 中包含的响应对象可以被修改（但不能被赋予新值）。要返回不同的响应类型（例如，用 HTML 响应替换错误），请通过 `reply(response)` 返回一个新响应。
- 验证响应 Payload (Validate response payload)
- 'onPreResponse' 扩展点
  - 总是被调用（除非调用了 `reply.close()` 或客户端提前终止连接）。
  - `request.response` 中包含的响应可以被修改（但不能被赋予新值）。要返回不同的响应类型（例如，用 HTML 响应替换错误），请通过 `reply(response)` 返回一个新响应。注意，在调用 `reply(response)` 之后产生的任何错误都不会传回 'onPreResponse' 扩展方法，以防止死循环。
- 发送响应（可能会触发 'request-error' 事件）(Send response)
- 触发 'response' 事件 (Emits 'response' event)
- 等待尾随处理 (Wait for tails)
- 触发 'tail' 事件 (Emits 'tail' event)

### 扩展点 (Extension points)

既然我们讨论了生命周期，现在我们可以利用 hapi 中的“扩展点”。这些“扩展点”在生命周期中暴露了流，可以在其中插入其他函数。它们可以轻松地绑定到服务器，以增强现有的 hapi 生命周期。我们使用 `server.ext` 功能来实现这一点。让我们看几个例子。接下来的示例在第 9 章关于如何实现 `shared` 上下文的部分中也有展示。现在不需要知道那意味着什么，但让我们看看 `server.ext` 在那里是如何使用的。首先看一个 `onPreResponse` 事件。

```javascript
server.ext('onPreResponse', function (request, reply) {

    var response = request.response;
    if (!response.isBoom) {
        if (response.source && response.source.context) {
            response.source.context.title = "hapi-plugins";
        }
    }

    return reply();
})
```

你可以看到我们调用了 `server.ext`。回想请求生命周期，`onPreResponse` 位于接近末尾的位置，就在给出响应之前。我们在此时添加一个函数，添加 `title` 上下文并返回 `reply()` 对象。

第 9 章中的另一个示例是：

```javascript
server.ext('onRequest', function (request, next) {

    request.__sharedContext = {
        title: 'hapi-plugins'
    };

    next();
});
```

这一次我们使用了请求生命周期的 `onRequest` 部分。同样，我们现在不需要具体知道这是做什么的，但请记住 `onRequest` 处于生命周期的开始部分，因此根据你需要在流程中添加功能的位置，你可以巧妙地将逻辑放入流程中。虽然这里没有讨论，但如果你需要在认证过程中添加一些自定义功能，可以使用 `onPreAuth` 或 `onPostAuth`。请记住，如果与当前流程无关，这些扩展点在生命周期中可能不会被调用。



# 概要

搭建服务器其实相当简单。服务器和插件在本质上非常相似。服务器可以由若干不同的插件组成。插件只是对更小、更易管理的部分进行逻辑分离，然后添加到你的服务器实例中。我们可以用各种功能来装饰服务器，也可以使用 JSON 配置文件对服务器进行配置。
使用 glue 可以真正让我们的搭建工作变得更加简单，而如果存在开发环境和生产环境的配置，那么使用 rejoice 和配置文件来管理也是一个不错的选择。
接下来，你将全面了解 hapi 服务器的路由。

# 路由 3

在大多数场景中，`route`（路由）一词与通往目的地的某条路径相关联。例如，从 A 点开车到 B 点，你可能有多条不同的路线可以选择。路由是两点之间一条非常明确的路径。

在 hapi 和其他框架中，路由是请求所经过的特定路径。在网站上，你在地址 `hapi-plugins.com` 之后能输入的字符数仅仅受限于浏览器支持的字符数。但为了发送请求并真正获得你所查找内容的响应，你需要知道将请求发送到何处的路由。随后查询会沿着框架内已知的路径传输，并根据请求中的若干参数返回相应的响应。你为查询指定的实际路由是处理该请求的关键。它是服务器对客户端期望如何处理该请求的第一个指示。

路由最简单的形式如下所示：

```
server.route({
    method: 'GET',
    path: '/',
    handler: function (request, reply) {

        reply.view('index');
    }
});
```

对于简短且简单的路由来说，这是一种很好且直观的形式，但当项目变得更大时，我们会将行为分离出来，使用配置来代替这里看到的直接提供 handler 的方式。

我们通常将配置存储在各自的文件中。在查看我们为这个项目做了什么之前，我们先进一步简化。
在我们的 `lib/routes.js` 文件中，有以下内容：

```
var Welcome = require('./controllers/welcome');
server.route({
    method: 'GET',
    path: '/',
    config: Welcome.index
});
```

然后路由的实际配置位于一个对应的文件 `lib/controllers/welcome.js` 中。

```
modules.export.index = {
    description: 'Show the main page for our welcome page',
    handler: function (request, reply) {

        reply.view('index');
    }
};
```

这样保持了代码的逻辑分离，这是 MVC（模型-视图-控制器）框架的典型做法。代码中的逻辑可能会变得非常广泛，通过这种分离，可以轻松地进行组织，使某个特定路由的所有逻辑都在一个文件中。你可能会决定采用这种方式，即简单地将该特定逻辑放在名为 `lib/controllers/welcome/index.js` 的文件中。在这个结构下，你的服务条款可能会放在 `lib/controllers/welcome/tos.js` 中。当然，一个函数在被拆分到独立文件之前需要考虑其大小是否合理。但核心思想是，将代码拆分为更小的部分后，管理起来和阅读起来都容易得多。

## 路径处理

路由是唯一的。GitHub 上已经有多个 issue 询问关于正则表达式或其他类型的通配匹配的问题。有时很难判断路由之间是否存在重叠。hapi 早期的设计目标之一就是确保路由表每次加载时都是完全一致的。不应该有任何意外。在启动时，hapi 会对任何冲突发出警告，从而保护你免受这类问题的困扰。

hapi 中路径处理的工作原理是：路由器在每个传入请求时遍历路由表，并执行第一个（且仅第一个）匹配的路由。路由匹配仅针对请求路径进行（不包括查询字符串和其他 URI 组件）。请求按确定性的顺序进行匹配，因此你在哪里添加它们并不重要。最后，路由按从最具体到最通用的顺序排序。如果你想了解更多关于其工作原理的细节，请参阅 **路径匹配顺序**。

## 路由的组成部分

路由对象，即 `server.route()` 的参数，只包含几个简单的属性。

### method

这决定了要在资源上执行的 HTTP 请求 **方法**。该方法是以下之一：GET HEAD POST PUT DELETE TRACE OPTIONS CONNECT PATCH。在实际使用中，最可能是 GET、POST、PUT、DELETE 或 PATCH 之一，且不允许使用 HEAD。hapi 允许使用通配方法，这意味着当没有找到精确匹配时，将使用通配符代替。通配符字符串是 *。

### vhost

指定此路由要监听的虚拟主机。一个服务器可以监听多个虚拟主机，但为了让路由针对某个特定主机触发，可以指定要监听的主机。这样，服务器就可以根据定义的 vhost 提供相应的路由。vhost 可以定义为字符串或字符串数组。默认情况下允许任何主机使用该路由。

### handler

handler 是一个函数，返回被调用路由的输出结果。它依赖于之前的验证和任何认证。如果 handler 是通过服务器定义的，那么可以传递一个包含 handler 名称属性以及任何选项的对象。如需深入了解 handler 的复杂细节，请参阅第 4 章。

### config

如果你需要为路由进行额外配置，可以使用 `config` 部分来定义。对于简单应用，你可能不需要指定额外配置，因此这不是严格要求的。但是，对于更复杂的配置，最好将代码组织在此结构下。在此结构中，你将 handler 移动到此部分，使所有配置都组织在同一位置。更复杂配置的一个例子是，如果你想添加验证或缓存。

需要注意的是，这里的缓存与第 2 章讨论的 `server.cache` 不同。后者的功能是缓存实际的响应对象。而此部分的缓存严格来说是头部缓存。它将设置 `Cache-Control` 头。下面是一个简单的示例，它为我们的 `/hello` 路由设置一小时的缓存头部。

```
server.route({
    method: 'GET',
    path: '/hello',
    config: {
        handler: handler,
        cache: {
            expiresIn: 60 * 60 * 1000
        }
    }
});
```

config 部分有非常多的选项，我们觉得最好还是引导你查阅 **文档**。不过，我们接下来要介绍的一个内容是路由前置条件。

## 路由前置条件

你可能需要初始化数据库连接，并将其返回给你使用的每个端点。这是一个非常适合由路由前置条件处理的任务。当然，还有许多其他事情可能需要设置，但这可能是最常见的场景。

前置条件允许你以串行和并行的方式运行任意数量的函数。

`pre` 的参数是一个混合数组。它可以包含其他数组或其他对象。数组中指定的所有项将并行执行，而所有其他项将串行执行，例如：

```
server.route({
    method: 'GET',
    path: '/',
    config: {
        handler: function (request, reply) {

            reply.view('index');
        },
        pre: [
            series,
            series,
            [
                parallel,
                parallel
            ],
            series
        ]
    },
});
```

`pre` 数组中的每个 `series` 和 `parallel` 项都是包含两个属性的对象：`method` 和 `assign`。

```
var dbSetup = function (request, reply) {

    DB.getConnection(function (err, connection) {

        return reply(connection);
    });
};

server.route({
    method: 'GET',
    path: '/',
    config: {
        pre: [{
            assign: 'db',
            method: dbSetup
        }],
        handler: function (request, reply) {

            var db = request.pre.db;
            // ...
        }
    }
});
```



```javascript
));
};

server.route({
    // ...
    config: {
        pre: [
            { method: dbSetup, assign: 'connection' }
        ],
        handler: function (request, reply) {

            var conn = request.pre.connection;
            conn.exec('select * from blah', function (err, result) {

                if (err) {
                    var msg = 'DB call failed';
                    return reply(Boom.internal(msg));
                }

                return reply(result);
            });
        }
    }
});
```

## 路径 (path)

路径由 `/` 字符划分为多个片段（segments）。这意味着任何不是 `/` 的部分都是一个片段。
需要尽早注意的一点是，每个片段不允许包含多个参数。
由于 hapi 规定路由必须始终处于可预测的顺序，因此 hapi 不支持任何形式的正则表达式语法，因为这样很难判断路径何时重叠。但 hapi 允许使用可选参数、通配符参数，以及匹配路径的多个片段。

### 简单路径 (SIMPLE PATH)

路径中由大括号指示的命名参数化部分，如：`/fixed/{name}`。在处理函数（handler）中，`request` 对象将拥有一个 `params` 对象。您可以在处理函数中使用 `request.params.name` 来利用 `name` 参数。我们将在第 4 章中详细介绍 `request` 对象。

构建路径有许多选项。随后在处理函数中可以通过 `request.path` 访问它们，这在第 4 章中也会详细讨论。
举例说明：

## 第 3 章：路由 (Routes)

```javascript
var internals = {};

server.route({
    method: 'GET',
    path: '/plugins/{name}',
    config: internals.config
});

internals.config = {
    description: 'A path to get info for a specific plugin',
    validate: {
        params: {
            name: Joi.string().required()
        }
    },
    handler: function (request, reply) {

        var msg = 'The name of the plugin that was passed is: ';
        return reply(msg + request.params.name);
    }
};
```

路由路径包含参数 `name`，随后会对其进行验证，以确保它是一个字符串而非其他类型。有关验证的更多信息，请参阅第 5 章。
然后我们通过 `request.params` 访问该参数以获取名称。

### 可选参数 (OPTIONAL PARAMETERS)

为了指定可选参数，我们使用问号 `?`。在正则表达式中，这也表示可选的匹配和捕获，所以您可能已经很熟悉了。
`/plugins/{name?}`
在这种情况下，如果 `name` 缺失，可能不清楚该提供什么内容，但您可以用它来提供一个插件列表。

### 通配符 (WILDCARDS)

如果我们需要接受任意数量的片段（例如，为了给特定路由代理查询），那么通配符 (`*`) 就是救星。任何使用通配符字符的内容都将以数组形式存储在 `request` 对象的命名参数中。如果我们允许直接从 npm 检索任何及所有结果，我们可以使用如下路径：
`/npm/{search*}`
由于这里的捕获特性（类似于允许函数拥有任意数量参数的编程语言，如 EcmaScript 6 提供的 `...` 剩余参数），剩余参数通配符只能放在路径的末尾。

但是，如果您明确定义了路径中允许的片段数量，则可以在其后放置其他片段。为了定义片段数量，在 `*` 后面添加一个数值来指示允许的数量。

```
`/npm/{search*2}/go`
```

上述语法将捕获两个片段，并将它们作为数组存储在 `request.params.search` 中。

### 服务器路由配置选项 (Server router config options)

作为服务器本身的一部分，只有两个可以设置的选项。

- `stripTrailingSlash` 非常有用，但默认设置为 `false`。这个选项的作用是：如果有一个像 `/plugins/like` 这样的路由，而请求发送到了 `/plugins/like/`，那么实际上会产生 404 错误，因为它没有匹配到路由。设置此选项后，服务器将去除末尾的斜杠，从而使路由依然有效。
- `isCaseSensitive` 默认为 `true`，这意味着路由是区分大小写的。如果设置一个名为 `/blah` 的路由和另一个名为 `/Blah` 且执行不同操作的路由，将是一种糟糕的设计。此设置意味着两者被视为相同。

### 总结 (Summary)

路由是请求在我们系统中经过的路径。它定义了请求如何被处理，以及在处理请求时我们能访问哪些变量。hapi 中的路由是唯一的，不存在重叠的可能性，且具有可预测性。路由可以配置缓存设置，也可以为特定的虚拟主机（域名）定义。

接下来我们将研究作为路由一部分而定义的处理函数（handler）。

## 处理函数 (The handler)

处理函数的核心在于处理特定路由的传入请求。它决定了请求将如何被“处理”。路由的配置在处理函数的行为方式中起着至关重要的作用，由于两者紧密耦合，因此在编写处理函数时需要考虑路由的某些配置。

当我们为请求指定一个路由时，例如，如果您要从 `/downloads/<filename>` 下载文件，那么处理函数中包含了所有寻找该文件并将其发送给连接客户端的逻辑。处理函数还可以执行其他操作，例如统计文件被下载的次数、通过访问控制确保并非任何人都能下载该文件，等等。

处理函数负责处理从接收客户端请求到向用户返回响应之间的所有决策和逻辑。hapi 提供了一些优秀的功能来自动减轻工作量，例如验证。我们将在第 5 章中详细讨论。如果我们忽略 hapi 的这些便利功能，所有这些工作都可以在处理函数中手动完成（但我们怎么会想那么做呢？）。

处理函数通常是一个由两个参数组成的回调函数：`request` 和 `reply`。我们还将探讨和发现多个其他内置处理函数。

本章将涵盖处理函数的各种不同用例。我们将深入研究处理函数的参数以及简化处理函数编写的各种方法。

## 请求 (The request)

`request` 对象包含所有与进入服务器的请求相关的信息，无论该请求来自浏览器还是使用 API 的其他工具。由于路由已经根据方法决定了哪个请求将被处理，因此接收到的请求将仅限于所指定的内容。归根结底，完整的请求在这里可用，其中包含请求头和发送的所有数据内容。

请回顾请求的生命周期，以了解请求如何在框架中传递。

## 第 4 章：处理函数 (The handler)

随请求附带的一系列重要且有用的信息将在处理函数中使用，以完成请求。在本节的剩余部分，我们将研究如何找到这些数据以及您可以如何利用它们。
请记住，在请求生命周期（见第 2 章）中还有其他函数可以在过程中向请求添加数据。下面我们将看几个常见的例子。

### 参数 (parameters)

部分 `request` 对象数据是作为路由直接配置的一部分设置的。例如，如果路由定义了一个包含要下载的 hapi 插件 ID 的路径，那么这将成为 `request` 对象上参数访问的一部分。

```javascript
server.route([
    // ...
    {
        method: 'GET',
        path: '/plugins/{name}',
        config: Controllers.Plugin.get
    }
    // ...
]);
```

在我们的案例中，`name` 是标识符，将通过 `request.params.name` 访问。在上面的示例中，请注意我们使用了 `GET` 方法。假设端口为 8080，如果我们执行：

```bash
curl -XGET http://localhost:8080/plugins/pluginName
```

我们将得到 `Controllers.Plugin.get` 中返回的内容。稍后在讨论 `payload` 时，我们将将其与其他方法进行对比。

### 查询 (query)

对于 hapi 新手来说，`param` 和 `query` 之间的区别可能会令人困惑。在 `https://hapi-plugins.com/search?q=pluginName` 中，URL 的 `query` 部分就是 `?` 之后的部分。请对比之前的 `/plugins/{name}` 示例。`name` `param` 严格属于路径的一部分。

`request.query` 对象包含所有作为 URL `query` 发送的键值对。
例如，为了在 hapi-plugins.com 上获取特定插件的信息，我们可以尝试一个比较极端的 URL，请求如下内容：
`http://localhost:8080/plugins/blipp?hello=hi`

如果我们用 `console.log(request.query)` 记录输出，那么将在控制台打印出如下结果：

```
{ hello: 'hi' }
```

值得注意的是，有时值可能是一个数组。hapi 会自动为你处理多个查询键，但你必须意识到结果可能与预期的类型不同。

如果 URL 如下所示：

```
http://localhost:8080/plugins/blipp?hello=hi&hello=hey
```

那么我们现在看到的值将是一个数组：

```
{ hello: [ 'hi', 'hey' ] }
```

## payload

`request.payload` 包含作为请求一部分传输但不适合作为查询参数的信息。这可能是一个文件，或者一坨 JSON 或 XML 数据。虽然确实可以为所有请求方法（GET、POST、DELETE、PUT、PATCH 等）发送 payload，但通常不用于 GET。如果你确实在 GET 请求中看到了 payload，你可能需要重新考虑你的设计。

让我们从一个简单的处理程序示例开始，我们将利用 POST 方法创建一个新用户。

```
handler: function (request, reply) {

    console.log('name is: ' + request.payload.name);
    console.log('email is: ' + request.payload.email);
    return reply('success');
}
```

如果你还记得我们之前讨论 `params` 和 GET 方法时，我们希望将此与 `payload` 进行对比。对于上面的处理程序，我们可以如下设置路由。

```
server.route({
    method: 'POST',
    path: '/user',
    config: {
        handler: handler
    }
});
```

在这里你可以看到方法是 `POST`。在我们之前定义的处理程序中，你可以通过 `request.payload` 来引用你的 `payload`。在这种情况下，payload 有两个键：name 和 email。我们向 `/user` 路径发送一个 `POST` 请求。一旦服务器启动，我们可以用 curl 做类似这样的事情：

```
curl -XPOST -H "Content-Type: application/json" -d '{ "name": "Author Name", "email": "author@hapi-plugins.com" }' https://hapi-plugins.com/user
```

我们也可以使用 `PUT`，它的工作方式相同。

## headers

`request.headers` 是所有请求头存储的地方。使用我们之前的 curl 示例，你会看到在处理程序中，你可以通过 `request.headers.Content-Type` 来引用它，其值将是 `application/json`。

## reply 函数

处理程序中的 `reply` 函数充当回调函数，并作为将控制权交还给框架的一种方式。`reply` 函数负责回复请求，返回所请求内容的结果。

为了遵循常规的回调约定，`reply` 接受两个参数，分别传递错误（err）和结果（result）。在实践中，只会使用其中一个。如果第一个参数是一个错误对象，它将被包装在一个 Boom 对象中。

`reply` 的参数类型可以是多种不同的类型：

- null
- undefined
- string
- number
- boolean
- Buffer 对象
- Error 对象
- Stream 对象（Stream 对象必须兼容 "streams2" API 且不能处于 objectMode）
- Promise 对象（hapi 的测试使用 bluebird promise 库）
- 任何其他对象或数组

## 组织处理程序

组织代码的方式有很多。对于简单的路由，也许把所有东西都放在一个路由里是有道理的。这是最简单的例子：

```
server.route({
    method: 'GET',
    path: '/',
    handler: function (request, reply) {

        reply.view('index');
    }
});
```

然而，在大型项目中，我们发现这样做可能会变得混乱。这就是我们使用路由配置（参见第 3 章）来让生活更轻松的地方。

我们将代码组织到 `/lib/routes.js` 中，这是我们所有路由的存放位置。每当我们添加一个新路由，或者需要查看路由时，我们都在这一个简单的位置找到它。这是一个值得遵循的好惯例。它不一定非得是 `routes.js` 文件，因为我们也可以把它们放在 `lib/index.js` 中。然而，这个命名清晰的文件使得每个人都能清楚地知道它在哪里。

一个典型的设置是将路由的配置放在一个完全不同的文件中，并且该文件是处理程序所在的位置。

我们的 hapi-plugins.com 示例在路由文件中只有这个：

```
server.route([
    {
        method: 'GET',
        path: '/',
        config: Controllers.Home.get
    },
    // ...
]);
```

当架构正确且处理程序很大时，将每个路由放在各自的文件中确实可以使代码更易于阅读。开始一个新路由时，只需复制一个具有约定的文件，然后修改处理程序本身即可。它形成了一个非常清晰易读的结构。

如果你想了解更多细节，可以在第 6 章中找到关于上述示例的更多讨论。

## 内置处理程序

### File

文件处理程序用于生成提供文件的静态端点。你很可能会将其用于不适合放在即将介绍的目录处理程序中的单个文件。

我们使用文件处理程序来提供 favicon，即浏览器用于关联网站的小型网站特定图标。

我们将 favicon 添加到 `lib/routes.js` 文件中，如下所示：

```
{
    method: 'GET',
    path: '/favicon.ico',
    handler: Controllers.Static.favicon
},
```

有多种使用文件处理程序的方法，所有这些方法都涉及在我们特定的设置中修改 `lib/controllers/handlers/static.js`。

### STRING

这是我们为 hapi-plugins.com 使用处理程序的方式，也是最直接的方法。

```
exports.favicon = {
    file: __dirname + '/../../public/favicon.ico'
};
```

### CALLBACK

回调函数接受 request 对象作为参数，并返回绝对路径或相对路径。

```
exports.favicon = {
    file: function (request) {

        return __dirname + '/../../public/favicon.ico'
    }
};
```

### OBJECT

一个包含多个选项的对象。

```
exports.favicon = {
	file: {
		// 'a path string or function as described above'
		path: __dirname + '/../../public/favicon.ico',
		filename: '??',
		mode: false,
		lookupCompressed: false
	}
};
```

我们的 path 指示了要查找并提供服务的文件的位置。这也可以设置为上面讨论的回调函数。

filename 是一个可选的文件名，用于指定是否发送 "Content-Disposition" 头。默认为路径的基本名称。

mode 指定是否包含 "Content-Disposition"。默认设置为 false，这意味着不包含它。

lookupCompressed，如果为 true，则查找具有 '.gz' 后缀的相同文件名，以便在请求支持内容编码时提供文件的预压缩版本。默认为 false。

### DIRECTORY

比文件处理程序更可能的用例是提供多个文件的目录。这很常见，用于提供诸如图像、CSS 文件或用于前端的 JavaScript 文件。

与我们的文件路由处理程序类似，路由首先在 `lib/routes.js` 中设置，在这种情况下，我们同时处理图像和 CSS，如下所示：

```
{ method: 'GET', path: '/css/{path*}', handler: Controllers.Static.css },
{ method: 'GET', path: '/img/{path*}', handler: Controllers.Static.img },
{ method: 'GET', path: '/js/{path*}', handler: Controllers.Static.js },
// ...
```

处理程序的定义方式非常相似，因此我们只看第一个作为示例：

```
exports.css = {
	directory: {
		path: __dirname + '/../../public/css',
		index: false
	}
};
```

path 是我们希望检索和显示的实际数据所在的位置。这里也可以设置许多选项。

我们首先将 index 设置为 false。在 CSS 文件夹中没有任何提供 index.html 的需要。

目录（directory）的选项如下：

- path - 设置此选项的各种方式的说明，请参见文件处理程序。
- index - 可以是 true、false 或表示要查找的索引文件名称的字符串。默认索引文件是 `index.html`，并设置为 true。
- listing - 确定在缺少索引文件时是否应显示目录列表。默认为 false。
- showHidden - 确定是否应在列表中显示隐藏文件。默认为 false。
- redirectToSlash - 如果有尾部斜杠，这将被重定向到没有斜杠的路径。默认为 true。
- lookupCompressed - 如果为 true，则查找具有 '.gz' 后缀的相同文件名，以便在请求支持内容编码时提供文件的预压缩版本。默认为 false。
- defaultExtension - 如果请求的文件未找到，则附加到文件请求的字符串。默认为空字符串。

### VIEWS HANDLER

视图处理程序使用模板显示信息。在实践中，此选项并不常用。更常见的方法是使用 views 选项配置服务器，然后使用带有 reply.views() 的常规处理程序。

因为 hapi 同时支持这两种方式，我们将简要介绍视图处理程序，并更多地关注如何配置服务器以直接通过 reply.views() 支持视图。

对于我们的 hapi-plugins 项目，我们没有使用视图处理程序，但应该提到它的使用方法。这可能是一种情况，即无论出于何种原因，需要覆盖常规的 server.views。

在两种情况下，服务器都使用视图管理器进行配置。

```
plugin.views({
    engines: {
        html: {
            module: require('handlebars')
        }
    },
    path: __dirname + '/views'
});
```



我们正在设置渲染引擎并指定用于读取模板的相对路径。引擎配置中的该属性设置了将用于特定渲染引擎的文件扩展名。

一个非常基本的用例如下所示：

```
exports.terms_of_service = {
    view: 'terms_of_service'
}
```

这里 view 只接受一个包含模板文件名的字符串。如果我们需要覆盖服务器的视图配置，则会更复杂，view 会接受一个对象：

```
exports.terms_of_service = {
    view: {
        template: 'terms_of_service',
        context: {
            serviceType: 'provider'
        }
    }
}
```

为清晰起见，快速说明一下：`context` 是一个 JSON 对象，包含发送到模板的实际数据。在这个例子中，在你的模板 `terms_of_service` 中，你可以引用 `serviceType`，它将填入值 `provider`。关于模板的更多讨论在第 9 章，根据模板引擎的不同，此语法会有所差异。

如果上面的对象没有传递 context，则会将其设置为一个包含以下属性的 context 对象：

- `payload` - 包含 `request.payload`
- `params` - 包含 `request.params`
- `query` - 包含 `request.query`
- `pre` - 包含 `request.pre`

view 对象还可以包含一个 options 属性，可用于覆盖服务器视图设置。

## 使用 SERVER.VIEWS 的常规处理器

使用 `reply.view()` 是渲染模板文件最常见的方式。

对于 hapi-plugins 的主页，我们只渲染一个索引文件，并在页面上显示随机引用。

```
module.exports.get = {
    handler: function (request, reply) {

        reply.view('index', {
            finalmsg: internals.quotes[Math.floor(Math.random()*internals.quotes.length)]
        });
    }
};
```

在模板中，我们看到以下内容：

```
<div id="finalfrontier" class="col-md-12">
    {{finalmsg}}
</div>
```

如果你想了解更多关于 handlebars 的信息，可以在 handlebarsjs.com 阅读更多内容。

## 代理

很多时候，使用代理是项目启动的一种简单方式。你有一个想要替换的遗留服务，代理可能是一个很好的起点。事实上，代理功能是 hapi 使用最广泛的功能。这正是我们在 WalmartLabs 开始使用 hapi 的方式。下面是一个如何代理 Google 的示例。

```
server.route({
    method: '*',
    path: '/{path*}',
    config: {
        handler: {
            proxy: {
                host: 'google.com',
                port: 80,
                protocol: 'http',
                // 6th redirect get a 300 response
                redirects: 5,
                passThrough: true,
                xforward: true
            }
        }
    }
});
```

这里我们对 method 使用了 * 通配符。它将匹配任何传入的方法。path 设置表示路由所有内容。最后，在 config 部分的 handler 下，我们有我们的代理。你可以看到我们为 google.com 设置了代理。redirects 设置表示我们最多只应重定向五次。passThrough 设置指定是否保留原始请求的标头。最后，xforward 设置告诉 hapi 向请求添加（或追加）一个 'x-forwarded-for' 标头。

你可以使用代理处理器做其他强大的事情。你可以使用 mapUri 重写请求，通过 localStatePassThrough 传递来自 hapi 实例的本地状态，使用 rejectUnauthorized 拒绝未经授权的请求，甚至可以使用 onResponse 的自定义函数执行任何其他操作。有关更多详细信息，请参阅文档。

你可以在此处代理自己的服务，而不是代理 Google。代理是开始处理简单任务的便捷方式。随着时间的推移，你可以为你的应用程序添加路由以接管该下游功能。由于变更集更小，这种方法更容易进行故障排除。

## 向处理器添加公共方法

有时有些函数需要被多次访问。在这种情况下，我们可以使用便捷函数。一种访问这些函数的方法是将所有此类函数放在一个公共库中并调用它们。

然而，hapi 还有其他几种解决方案可以使这个过程更容易。

## 绑定到服务器

通过在全局上下文中进行绑定，可以在处理器函数中使用 `this` 访问任何变量或函数。如果你需要共享功能，这会很有用。

可以在插件或顶层服务器级别设置上下文。

我们通常将其用于整个应用程序中需要访问的某些服务。当服务器方法可以使用时，与服务器绑定相比，可以使用一些个人的主观见解，但通常，服务器绑定上可访问的东西是为应用程序持续期间初始化的东西，而你不希望每次初始化，与自包含的某些便捷函数不同。

```
server.bind({
    service: new Service()
});
```

此函数可以从任何处理器中简单地通过 `this.service()` 访问。这可以作为一个有用的快捷方式。

有关绑定的更多信息，请参见 hapijs.com/api#serverbindcontext

## 装饰回复

类似于 `server.bind`，此函数可用于装饰 reply。Decorate 在可使用的范围上更窄，但它非常适合用于模板化回复。

```
server.decorate('reply', 'success', function () {
    return this.response({ success: true });
});
```

我们可以选择装饰回复对象或服务器对象，第一个参数我们指定是哪一个。第二个参数指定方法的名称，第三个参数是回调。

在我们的处理器中，我们可以简单地调用：

```
reply.success();
```

这是一个非常方便的快捷方式，如果返回的 JSON 对象发生变化，可以避免在多个地方进行更改。它也是确保成功回复一致性的良好方法，因为它消除了拼写错误。

你可以在第 2 章中找到更多关于装饰服务器对象的信息。

## Tails

某些操作不需要立即完成。此类调用可能是某种后台作业，对于返回给客户端的页面来说不是必需的。它可能是用于某些更新的数据库调用，也可能是任何数量的其他事情。虽然捕获此操作不是必需的，但我们可能仍想为此进行记录以用于日志记录目的。当请求的 tails 完成时，服务器会发出一个 `tail` 事件。

```
server.route({
    method: 'GET',
    path: '/',
    handler: function (request, reply) {

        var publishTail = request.tail('publish the book in the background for download');

        HapiBook.publishForDownload({ format: 'pdf' }, function (downloadUri) {

            var mail = Mail({ to: user });
            mail.publishNotification(downloadUri, function () {

                publishTail();
```

## 使用 server.handler 定义处理器

处理器可以直接定义在服务器对象上。在实践中，这不是我们在自己代码中定义处理器的方式，但这里将其作为一种可能的替代方案包含在内。毕竟，很多代码都取决于偏好。

```
var DB = new Database(options);

server.handler('pluginLike', function (route, options) {

    return function (request, reply) {

        options.DB.getPlugin(request.path.id, function (err, plugin) {

            if (err) {
                return Boom.internal(err);
            }

            plugin.like(function (err) {

                if (err) {
                    return reply.fail();
                }

                return reply.success();
            });
        });
    }
});

server.route({
    method: 'GET',
    path: '/plugins/like/{id}',
    handler: { pluginLike: { dbHandler: DB } }
});
```



## 点赞插件示例

作为一个更大的例子，我们来看看在网站上点赞插件时后台发生了什么。下面是一个示例。

```javascript
module.exports.like = {
    auth: 'session',
    handler: function (request, reply) {

        var pluginName = request.params.name;
        var username = request.auth.credentials.username;

        if (!username) {
            return reply(Boom.unauthorized());
        }

        var getPlugin = function (user, next) {

            DB.plugin.get(pluginName, function (err, plugin) {

                if (err || !plugin) {
                    var msg = 'no such plugin found';
                    return next(Boom.notFound(msg));
                }

                return next(null, plugin, user);
            });
        };

        var addLike = function (plugin, user, next) {

            user.like(plugin, function (err) {

                return next(err);
            });
        };

        Async.waterfall([
            getOrCreateUser,
            getPlugin,
            addLike
        ], function (err, result) {

            if (err) {
                return reply(err);
            }
            return reply({success: true});
        });
    }
};
```

## 上传文件

能够直接上传文件到网站是我们作为开发者面临的最基本功能之一，然而，要弄清楚如何做到这一点往往 unnecessarily 困难。本节将带你了解如何处理文件上传以及你可以采取的一些不同选项。

对于我们的网站，我们需要能够上传软件包以便发布它们。这使我们能够为插件站点注册软件包，并且 npm 在用户的凭证下变为可选。

让我们从视图开始。模板将在第9章讨论，因此请查阅该章节以了解如何使上传页面的呈现满足你的需求。现在，让我们看看上传文件所需的 HTML 代码。

```html
<!DOCTYPE html>
<html>
    <form action="/plugin/upload"
          enctype="multipart/form-data" method="post">
        <p>
        选择要上传的文件：
        <input type="file" name="datafile" size="40">
        </p>
        <div>
            <input type="submit" value="发送">
        </div>
    </form>
</html>
```

这是一个通用的上传表单，可以与你手头任何后端系统配合使用。简单来说，它会向 `/plugin/upload` 发送表单 POST 请求，其中文件的载荷名为 `datafile`。

在接收端，我们需要设置处理器来处理数据。代码如下所示：

```javascript
module.exports.postUpload = {
    description: 'Post a file for upload',
    payload:{
        maxBytes: 209715200,
        output:'stream',
        parse: true
    },
    handler: function (request, reply) {
        request.payload.datafile.pipe(FS.createWriteStream("out"));
        reply('yeah, so... done.');
    }
};
```

回想一下本章的载荷部分，我们可以利用 `request.payload` 对象来处理 `POST` 等方法。注意，我们给出了如何处理载荷的具体选项。默认载荷限制为 1MB。这有助于防止恶意和/或无能的用户拖垮你的应用，也是 hapi 与其他不太关注此类安全特性的框架的区别之一。当用户发送非常大的文件时，服务器可能会耗尽内存。这可能会被用作攻击来使你的服务瘫痪。在这种情况下，我们通过将默认的 `maxBytes` 值提高到更高且更实用的数值，来允许处理更大的文件。

因为我们正在接收文件，所以我们选择创建一个 `readStream`，这样我们就可以将输出直接管道到文件、数据库或任何首选的存储方法。通过将文件内容直接从请求中分块移动到 readStream 中，我们避免了需要在存储到别处之前将整个文件保存在应用程序内存中。这节省了宝贵的时间和内存。

虽然解析的默认值是原始数据，但我们选择在这里明确包含它。这个字段告诉 hapi 数据是否需要以 gunzipped（压缩）方式处理或以原始方式发送。`true` 和 `gunzip` 意味着文件将被处理。

支持一些 MIME 类型，看看上面表单的 "enctype"，你可以看到我们使用的是 "multipart/form-data"。hapi 支持以下类型：

- 'application/json'
- 'application/x-www-form-urlencoded'
- 'application/octet-stream'
- 'text/*'
- 'multipart/form-data'

在处理器中，我们为文件创建一个 `writeStream` 并将传入的数据管道到其中。大功告成！

## 小结

在本章中，我们学习了使用处理器来处理和返回不同类型响应的所有方法。接下来，你将看到如何验证处理器的输入和输出，从而节省大量处理不当数据的时间。

# 验证

## 5

> [hapi] 让我们的开发过程异常高效，真正的"愉悦"。

-- https://github.com/hapijs/hapi/issues/1613#issuecomment-46332030

Eran 在一条推文中提到，他为 hapi 对数据验证产生的影响感到自豪。他理应如此。能够验证输入数据和输出数据是一件大事，而且实际上让这变得简单并成为一个框架的组成部分更是一件大事。如果你问为什么这是件大事，希望你不是因为怀疑，而是因为你只是想知道。我们都在与极其高效处理数据的计算机打交道。如果我们最终得到了错误的数据，你的计算机处理工作的效率或它最终进行的计算是什么就真的不重要了。不仅从拥有正确数据的角度来看这很重要，而且对于由此产生的错误和其他错误也很重要；在动态语言中更是如此。期望一个数字却得到了字符串？这可能非常糟糕。

在 hapi 验证中使用最广泛的库叫做 joi。当作者第一次看到 Eran 在 WalmartLabs 进行 hapi 演示时，Eran 以一首关于 hapi 的歌曲开始了演示。事实上，如果你在 YouTube 上搜索，你可以找到这样的演示（https://www.youtube.com/watch?v=Recv7vR8ZlA）。这首歌是 hapi hapi joi joi 歌。既然 hapi 和 joi 都在歌中，这可能让你了解 Eran 对质量以及确保所有数据都经过验证并处于安全可操作状态的看法。

在本章中，我们将介绍使用 joi 和不用 joi 进行验证的各种方式。

## 验证类型

hapi 为以下输入提供验证：`query`、`payload`、`headers` 和 `params`。回想一下我们在第4章学到的这些内容。此外，hapi 还允许我们对响应进行验证。

验证的格式始终是以下内容：

- `true` - 不执行验证。这是默认值。
- `false` - 此部分完全不允许任何变量。
- Joi 验证对象。这是我们到目前为止讨论过的。
- 验证函数。

我们最终最典型使用的是 joi 验证对象，我们将主要关注这个。验证函数也可以用于不适合常规 joi 验证的情况。

## Joi 验证

验证配置为传递给路由的路由选项的一部分。假设你想更改用户的密码。你想向端点发送一个 JSON 对象密码，并将其更改为你指定的密码。JSON 对象看起来像这样：

```json
{
    "password": "somepass"
}
```

然后你可以将路由设置成这样：

```javascript
var routeOptions = {
    validate: {
        params: Joi.object().keys({
            id: Joi.number()
        }),
        payload: Joi.object().required().keys({
            password: Joi.string().min(8).required()
        })
    },
    response: {
        schema: Joi.object().keys({
            success: Joi.boolean().required()
        })
    },
    handler: handler
};

server.route({
    method: 'POST',
    path: '/user/{id}/password',
    config: routeOptions
});
```

我们在这里看到的非常典型。这确保了路径 URL 中的 id 将是一个数值。使用了 params 关键字，在我们的 server.route 中，{id} 会得到

被转化为这个参数。我们在服务器路由中使用的是 `POST` 方法，这个 JSON 对象会被转化为 `payload` 对象。

你可以看到，校验是在 payload 上完成的。payload 中传递的密码必须是至少八个字符的字符串，并且是一个必填字段。此外，我们告诉 hapi，预期的响应是一个 JSON 结构，其 success 值为 `true` 或 `false`。

你可能会问，为什么 response 不在 `validate` 部分？`validate` 部分严格用于输入。当你第一次将 hapi 与 joi 结合使用时，这一点可能并不明显。如果你在工作中依赖另一个 API，那么输出（响应）校验就变得极其重要。拥有输出校验能让你确信从该 API 获取到了正确的内容。

正如你在我们目前的代码中所看到的，我们喜欢将一切拆分，并广泛使用 config。由于校验模式（schema）可能会变得很长，我们通常将校验规则放在 internals 变量中。

internals 变量是放置文件中所有顶层变量的地方。这可以防止该作用域被污染。在我们需要在多个不同地方访问 schema 以处理校验的情况下，这尤其有用。下面的示例演示了这一点。

```javascript
var internals = {
    pluginSchema: Joi.object().keys({
    });
};

// Get plugin data

exports.get = {
    description: 'gets plugin data for a specific plugin id',
    response: {
        schema: internals.pluginSchema
    },
    handler: function (request, reply) {
        // ...
    }
};
```

## hapi-plugins.com 的校验

让我们来看看 hapi-plugins.com 的搜索功能。

```javascript
module.exports.search = {
    validate: {
        query: {
            q: Joi.string(),
            sort: Joi.string().optional(),
            fields: Joi.string().optional()
        },
        response: {
            schema: Joi.array().includes(Joi.object().keys({
                name: Joi.string().required(),
                authors: Joi.array(),
                keywords: Joi.array(),
                dependencies: Joi.array(),
                dependents: Joi.array(),
                homepage: Joi.string().allow(''),
                version: Joi.string(),
                license: Joi.string(),
                description: Joi.string(),
            }))
        },
        handler: function (request, reply) {

            var query = null;
            var sort = null;
            if (request.query.q) {
                query = Xss(request.query.q);
            }
            if (request.query.sort) {
                sort = Xss(request.query.sort);
            }
            DB.plugin.search(query, sort, function (err, results){

                var converted =  internals.convert(results);
                return reply(converted);
            });
        }
    };
```

在这里你可以看到，输入校验是在 query 上完成的。它期望三个输入都是字符串。其中 `q` 是唯一的必填输入。额外的 `sort` 和 `fields` 输入是可选的。但是，如果提供了这些输入，它们必须是有效的字符串。如果对 API 的请求未能提供这些，那么前端的错误将非常明显，方便调用者进行调试。

你可能会注意到使用了 `Xss`。这在第 12 章中有更详细的解释，但它有助于防止跨站脚本攻击。

在这个例子中另一个需要注意的重要点是，对于 `homepage`，你可以看到为字符串添加了 `allow('')`。默认情况下，字符串不允许为空。这对某些人来说可能很烦人，但在涉及校验时，谨慎行事总是更好的。

你还会注意到响应部分也有校验。为此提供了 schema 来定义每个值应该是怎样的。我们选择不将其拆分，因为它较小，放在一起更易阅读。

对于 hapi-plugins.com，一旦结果从数据库返回，它们会被转换为一种输出格式，其中所有冗余数据都被移除，仅转换为所需的内容。然后通过此响应 schema 对这些数据进行校验，以确保数组中的每个项都符合预期的结果。

这样我们晚上就可以安心睡觉了。

## 使用 joi 进行通用数据校验

我们不仅使用 joi 校验来验证输入和输出，还在内部使用它来校验各类其他数据。假设我们要调用一个外部服务，甚至仅仅是查询数据库。虽然我们希望数据不会被导致错误的片段数据所污染，但如果你在下游的某个地方依赖这些数据，小心谨慎地进行校验总没有坏处。

因此，我们在 hapi-plugins.com 中涵盖的校验场景并非全部，joi 的功能远比我们目前看到的要多。我们将在这里投入更多时间来研究 joi 还能提供什么。

需要记住的一个属性是 joi 是可链式的，这意味着你可以为自己创建快捷方式。

想象一下你正在校验一个特定的字符串，可能是一个电子邮件 `Joi.string().email()`，或者一个更复杂的长字符串。

例如，你可以将 email 分配给一个更短的变量：`var email = Joi.string().email()`，然后在各处使用它，而不是使用较长的版本。

作者在开发列表功能（愿望清单、婚礼登记、婴儿登记等）时，必须确保每次发送的都是正确的列表类型。当时使用的是以下校验：

```javascript
Joi.string().insensitive().required().valid(['BR', 'SFL', 'WR', 'WL']),
```

在这种情况下，我们不在意大小写，但我们在意字符串必须是四种不同列表类型之一。否则，它就是无效的。

## 使用校验函数

虽然 joi 是 hapi 校验的核心，但完全可以在不使用 joi 的情况下进行校验。在我们需要校验的特定路由选项部分，我们不使用 joi 签名，而是使用一个校验函数。

该函数接受三个参数：`value`（待校验的值）；`options`（服务器校验选项）；以及一个签名形式为 `callback(err, value)` 的回调函数。

```javascript
var internals = {};

internals.validationFunction = function (value, options, next) {
    //do something
};

var routeOptions = {
    validate: {
        payload: internals.validationFunction
    }
};
```

## 总结

到目前为止，你已经对什么是数据校验、如何使用它以及 hapi-plugins.com 如何使用它有了全面了解。joi 支持广泛的数据类型，我们建议你查看文档以了解更多详情。需要注意的是，joi 并不一定要专门用于 hapi 项目。虽然 `validate` 被方便地内置在 hapi 中，但 joi 也可以用于其他框架。接下来，你将看到 hapi 的插件架构如何让一个应用程序变得不仅仅是其各部分的简单叠加。

## 插件

既然我们已经了解了如何校验输入和输出，接下来我们要讨论如何在 hapi 中利用插件来更好地管理代码。将软件作为单体代码块发布，并不比编写跨越数千行代码的函数更好。通过将软件编写为承担特定角色的小函数，我们可以更容易地测试函数，更容易地调试问题，并且更容易理解架构。插件也遵循这个模型，但它们面向的是主软件的功能，而不是简单的代码片段。插件允许你扩展当前功能，同时将代码模块化，以便于划分、维护和测试。

将代码拆分为插件的好处不仅限于你自己的代码，它还允许用户轻松分享对每个人都有益的代码。例如，你可能编写了专门用于 Facebook 认证的代码（bell），或者一个简单的在启动时显示路由的插件（blipp）。

在本章中，我们将探索如何编写插件以及如何围绕插件组织代码。此外，我们将研究一些我们使用的流行插件，以及曾经作为核心项目一部分的插件。

hapi 的插件模型和可替换部件的一个好处是，你不受特定实现方式的约束。如果以后出现了一个比当前使用的更好的插件，那么更换它比该部分代码与你想保留的代码紧密耦合时要容易得多。这不仅适用于第三方插件，也适用于你自己系统内部的任何部分。

当大公司在多个团队之间开发插件时，诸如缓存之类的事情可以基于每个插件来决定。团队之间不需要沟通，即使插件在同一个服务器上运行，不同服务器（模块）中的路由也可以通过插件配置使用不同的缓存机制，以适应该特定代码块的功能需求。



## 创建你自己的插件

请注意，我们 hapi-plugins 项目中的所有内容在架构上都被设计为插件。我们为路由器编写了插件，也为模型编写了插件。甚至身份验证也是一个插件。

让我们首先查看 `lib/index.js` 文件，所有的插件都在这里被加载。

```
server.register([
    Bell,
    Blipp,
    HapiAuthCookie,
    Authentication,
    Controllers,
    Models,
    Routes
],
function (err) {

    if (err) {
        console.log('server.register err:', err);
        return callback(err);
    }

    server.start(function () {

        console.log('server started on port: ', server.info.port);
        return callback(null, server);
    });
});
```

任何使用 Async 的人可能都会认出这种模式，因为它允许你轻松运行许多函数。我们非常推崇使用异步方法，而这里的模式与之非常相似。在内部，hapi 使用 `items`（一种精简的异步方法）来实现其目标。

register 函数的签名是 `server.register(plugins, [options], callback)`。

传递插件有几种不同的方式，但这里展示的方式通常是我们所有项目（我们有很多项目）的组织方式。使用 register 函数传递插件的最大好处是，它们可以很容易地被制作成独立的 npm 包进行加载。它们也可以作为独立的代码库共享在 github 上。

我们发现，当许多人共同开发一个大型项目时，将具有逻辑划分的特定组件分别放在各自的代码库中效果非常好。例如，如果你有一个博客系统，你可以将所有与处理文章相关的路由放在一个插件中，将所有处理评论的路由放在另一个插件中。这样每个独立的部分都有各自的负责人，这往往能减少代码冲突。但这并不总是有效，例如，你可能会有紧耦合的服务。在对待自己的代码时，你是专家。由你来决定什么对你的项目最合适，而 hapi 非常灵活，因此你可以按照你喜欢的方式组织项目。

另一种代码分离方式是保持控制层（controllers）精简，并将尽可能多的逻辑放入模型（models）中。反过来，模型也可以拥有包含代码的自有库。

通过将代码分离成更小的原子部分，代码复用变得简单得多。理解架构也变得更容易。例如，你可能会发现希望在项目之间更容易地访问某些测试设置。你最终可能会采取我们的做法，即创建一个专门用于通用测试的代码库。即使在单个项目内部，这也是一种非常不错的方法，而且还可以跨多个项目复用。

让我们通过查看处理器（handlers）是如何加载的，来详细分析其中一个部分。

```
var load = function (options, callback) {

    options = options || {};
    options.extension = options.extension || '.js';
    var controllers = {};

    var files = glob.sync('*' + options.extension, {cwd: options.path || __dirname});
    for(var i in files) {
        if (files[i] != path.basename(__filename)) {
            var key = path.basename(files[i], options.extension);
            key = key.charAt(0).toUpperCase() + key.slice(1);
            controllers[key] = require((options.path || __dirname) + '/' + files[i]);
        }
    }

    if (callback) {
        return callback(null, controllers);
    }

    return controllers;
};

exports.register = function (plugin, options, next) {

    load({path: __dirname + '/handlers'}, function (err, handlers) {
        if (err) {
            throw err;
        }

        if (process.env.DEV) {
            console.log('handlers:');
        }
        plugin.expose('handlers', handlers);
        next();
    });
};
```

```
exports.register.attributes = {
    pkg: require('./package.json')
};
```

我们从一个名为 `load()` 的便捷函数开始。`load` 的目的是遍历给定目录中的所有文件并加载（require）这些文件。此外，我们在 `handler` 名称下公开（exposing）了加载的处理器文件。这些文件随后在我们的 `lib/handlers.js` 文件中使用，以访问路由的处理器。

发送到 register 函数的 `plugin` 对象本质上就是 `server` 对象本身。由于上下文的关系，它在这里被称为 `plugin`。

`plugin.expose` 是一个函数，用于使插件可以通过 `server.plugins[name]` 对 server 对象可见。在这种特定情况下，它可能不是必须的，因为我们只在路由文件中使用处理器，但公开插件是一个好习惯，这样它们可以在应用程序的任何地方使用。

插件还会被设置一些属性（attributes）。通常可以直接设置为 `package.json`，但如果你想保持精简，或者由于某种原因不想使用 `package.json`，你可以直接使用一个包含 `name` 和 `version` 属性的对象来设置：

```
exports.register.attributes = {
    name: 'handlers',
    version: '1.0.0'
};
```

大多数插件的内容就这些。不过，关于我们使用的插件，还有几件事需要说明。

除了 `expose`，我们还倾向于使用 `plugin.dependency` 以及 `plugin.bind`。

例如，假设你在自己的插件中进行某些设置时依赖于另一个第三方插件。这时 `plugin.dependency` 就派上用场了。依赖关系是基于每个连接进行检查的。因此，即使你在一个连接中加载了插件依赖，如果在另一个使用该插件的连接中没有加载，hapi 将抛出错误：`Plugin *api* missing dependency controllers in connection: http://0.0.0.0:8088`。

当我们希望在整个应用程序中访问某些数据，但不想重复加载时，可以使用 `plugin.bind`。这可以是初始化或实例化某些数据，且我们只需要执行一次，例如设置会话（session）或其他与整个应用生命周期相关的特定内容。

我们的 `lib/routes.js` 中就有这两种用例的示例。

```
plugin.dependency('controllers');
plugin.dependency('models');

var Controllers = plugin.plugins.controllers.handlers;
var Models = plugin.plugins.models.models;
plugin.bind({
    models: Models
});
```

路由文件要求首先设置控制器，因为它们包含了路由所使用的处理器。模型将在插件路由中使用。此外，由于使用了 `bind`，数据库模型现在在处理器中可以通过简单的 `this.models` 访问。

## 插件配置

之前你可能没有注意到，在通过 register 函数注册插件时，会传递一个 `options` 参数。再次向你展示：

```
exports.register = function (plugin, options, next) {

    load({path: __dirname + '/handlers'}, function (err, handlers) {
        if (err) {
            throw err;
        }

        if (process.env.DEV) {
            console.log('handlers:');
        }
        plugin.expose('handlers', handlers);
        next();
    });
};
```

你可以看到 `options` 在任何地方都没有被使用。然而，`options` 可以用来配置插件。假设我们想为 blipp 插件传递一些选项。回想一下，这个插件的作用仅仅是在启动时列出路由。虽然目前路由不支持此操作，但可以想象你可能不希望 blipp 在启动时用彩色打印路由表，因此你可能想传递一个标志，告诉它始终在不使用 ANSI 颜色地打印。我们的代码应该改为如下所示：

```
server.register([
    Bell,
    { register: Blipp, options: { colors: false }},
    HapiAuthCookie,
    Authentication,
    Controllers,
    Models,
    Routes
],
function (err) {

    if (err) {
        console.log('server.register err:', err);
        return callback(err);
    }

    server.start(function () {

        console.log('server started on port: ', server.info.port);
        return callback(null, server);
    });
});
```

上述代码是针对我们整个 server 实例的。实际的 blipp 插件会有一个如下所示的 register 函数：

```
exports.register = function (server, options, next) {

    if (options.color === true) {
        // 执行彩色显示
    }
    else {
        // 关闭彩色显示
    }
    // ...
}
```

在我们的服务器启动中，我们将 options 设置为 `{ colors: false }`。我们将这些选项传递给插件，现在插件知道要关闭颜色显示。我们在第 2 章中看到了选项的传递。如果你查看 rejoice 和 glue 部分，你会看到插件的选项是如何传递给插件的。其中的一个例子是 good 插件区域中的 `opsInterval`。你可以直接在配置中设置你的选项。



甚至可以为每个环境设置不同的选项。这让您可以再次将所有内容集中在一个位置，从而使管理更加方便。

## 关于标签和选择插件

在注册期间，插件可以加载到为服务器专门指定的连接上。这是 hapi 的一个非常重要的特性。它允许在一个包中处理多个截然不同的服务器。通过这种方式，可以将 API 与呈现模板的逻辑分离开来。

实际上，调试设置并确保正确的插件注册在正确的服务器上可能具有一定的挑战性。我们推荐使用 `blipp` 插件，以便在加载服务器时查看路由表中的运行情况。

```
server.register([
    // plugins ...
    ], { select: 'http' },
    function (err) {

        if (err) {
            console.log('server.register err:', err);
        }

        server.register([
            // plugins ...
            ], { select: 'api' },
            function (err) {

                if (err) {
                console.log('server.register err:', err);
                }

                server.start(function () {

                    console.log('server started on port: ', server.info.port);
                    return callback(null, server);
                });
            }
        );
    }
);
```

## 何时使用插件

其目标是更好地管理您的代码 -- EH

## 第 6 章：插件

我们已经触及了一些使用插件的场景，但让我们再次回顾并详细说明。正确地使用插件可以帮助您构建良好的代码架构。

如果某些工作可以从整体中分离出来并在不同项目中复用，那么您就应该创建插件。您可能已经开始查看项目中可用的各种插件，但没有发现适合您需求的一种。在这种情况下，您可以创建自己的插件。其中一位作者发现，与 Ruby on Rails 等流行框架不同，hapi 没有一种方法可以在应用启动时列出所有可用路由。于是，一个专门用于显示该简单信息的插件被创建了出来。

正如前文提到的，项目也可以根据可用路由进行组织。一个插件可以完全专注于仅提供特定路径的路由。例如，我们可以将所有关于插件的路由放在一个插件中。

```
plugin.route([
    { method: 'GET',  path: '/plugins/upload', config: Controllers.Plugin.getUpload },
    { method: 'POST', path: '/plugins/upload', config: Controllers.Plugin.postUpload },
    { method: 'GET',  path: '/plugins/{name}/download', config: Controllers.Plugin.download }
])
```

而我们可以有另一个插件来处理用户信息。

```
plugin.route([
    { method: 'GET',  path: '/user', config: Controllers.User.get },
    { method: 'PUT', path: '/user/profile', config: Controllers.User.updateProfile }
])
```

如果您有一个大型项目，且由于路由包含大量逻辑而需要分工，那么这种做法将更有意义。

## hapi 插件生态系统：一些常用插件

让我们来看看 hapi 生态系统中的一些流行插件。您当然可以在 hapi-plugins.com 上找到更多插件，但我们在此时特意展示一些主要的插件。

## hapi-auth-basic

该插件为登录应用程序提供基础认证（basic authentication），或者更广泛地说，提供通用基础认证。大多数基于 Web 的系统都需要某种形式的认证才能访问数据。许多框架将此作为框架的一部分，但通过这种模块化方法，任何形式的认证都是可能的。

关于 hapi-auth-basic 的更多信息将在第 7 章中提供。

### blipp

虽然 blipp 不是一个核心插件，但它仍然非常有用。它简单地在 hapi 服务器启动时显示路由以及服务器:端口的组合。它能非常快速地指示哪些路由可用，以及它们是否在正确的服务器连接上可用。

### bell

Bell 与 hapi-auth-basic 非常相似，不同之处在于它使用第三方登录，例如 Facebook, GitHub, Google, Instagram, LinkedIn, Twitter, Yahoo, Foursquare, VK, ArcGIS Online 和 Windows Live。如果您希望支持这些登录方式，这就是您应该使用的插件。第三方插件在不断增加。Bell 通常与 hapi-auth-cookie 配合使用，因此这里没有将其单独明确列出。

关于 bell 和 hapi-auth-cookie 的更多信息将在第 7 章中提供。

### good

如果您在生产环境中运行服务，几乎肯定会想要使用 good。您可以通过 CPU 使用率、内存等指标来查看服务的性能。此程序有许多可用的报告器（reporters），您可以将报告发送到文件日志、控制台，或者您自己编写报告器的任何自定义程序中。

关于 good 的更多信息将在第 11 章中提供。

### tv

TV 是一个用于调试的交互式模块。通过它，可以轻松查看服务接收到了哪些请求，以及服务如何处理这些请求。

关于 tv 的更多信息将在第 11 章中提供。

### lout / hapi-swagger

Lout 和 hapi-swagger 是用于路由和设置的文档工具。它为您提供 API 文档，这样您就无需手动编写。对于一个无论如何都需要准备的东西，这可以为您节省大量时间。

### poop

为了符合 hapi 追求趣味性的目标，`poop` 是一个在发生异常时进行进程转储（process dump）的插件。它提供一个堆转储（[https://www.npmjs.com/package/heapdump](https://www.npmjs.com/package/heapdump)），同时还会提供一个包含调试详细信息的日志文件。

## 更多插件

您可以在 hapijs.com 的 `Plugins` 目录下找到一份详尽的插件列表。

## 总结

hapi 插件通常在开始时是核心项目的一部分。随着项目的增长，hapi 的许多部分被拆分为独立的插件。发生这种情况有多种原因：它有助于保持规模精简且易于管理；它便于在其他应用程序中复用；它还可以有效地在大型团队之间分离职责。

编写插件还可以驱动 hapi 应用程序的设计。它们使应用程序易于管理，并允许构建配置驱动的服务器。我们已经向您展示了它们的实用性，以及如何使用选项来保持配置的可管理性和灵活性。

接下来，我们将利用上述一些 hapi 认证插件，并解释如何利用 hapi 来满足您的认证需求。

# 认证 7

从一开始，认证在 hapi 中就处于核心地位。一个健壮的应用框架必须考虑认证，才能获得广泛的采用。目前 hapi 已经存在大量认证策略。hapi 处理认证方式的一个优点是，虽然认证对于框架本身至关重要，但策略预期由外部模块提供。即使是支持基础认证，也需要安装一个外部模块。因此，hapi 开发者拥有许多选项，其中一些甚至是竞争关系。

## 本章概述

下一章将涵盖 hapi 认证的许多细节。具体而言，将涵盖以下插件：

- hapi-auth-basic
- hapi-auth-cookie
- bell (结合 hapi-auth-cookie 使用)

## 方案 (Scheme) 与 策略 (Strategy)

在讨论认证时，方案（scheme）和策略（strategy）之间的区别可能会让人感到困惑。

您可以将方案视为一种通用的认证类型，如 basic 或 digest。而策略是该方案的一个经过预配置且命名的实例。另一种思考方式是：认证策略设定了在技术/机制上*如何*进行认证。策略可以是第三方 OAuth 策略、数据库、Cookie、基础认证或任何您可以想到的自定义策略。它们依赖于认证方案。而认证方案则设定了*谁*在进行认证。方案可以是管理员、用户或自定义角色。

接下来，我们将讨论 `hapi-auth-basic` 插件。它的策略非常简单，使用 basic 方案来实现。它很简单，因为其本质就是一个简单的对象。当您注册 `hapi-auth-basic` 插件时，它会创建一个方案，包含

基础策略的名称是 `basic`。这是通过 `server.auth.scheme()` 方法完成的。一旦 `hapi-auth-basic` 插件被注册，你就可以使用 `server.auth.strategy()` 函数来创建一个名为 `simple` 的策略，该策略指向我们命名为 `basic` 的方案。最后，你告诉一个路由使用名为 `simple` 的策略进行身份验证。

随着你阅读本章并查看具体示例，这些概念应该会变得更加清晰。

## hapi-auth-basic

在硬编码的用户名和密码之后，下一步是基本认证。它比明文传递的用户名和密码安全不了多少，但对于一些内部应用程序来说，它确实有其用途。抛开可能存在的任何实际用途不谈，它确实为理解 hapi 认证提供了一个简单的起点。

在 hapi 的早期，基本认证方案是直接内置在模块本身的。在第 6 章中，我们讨论了 hapi 已经演变，并且随着认证的发展，将 hapi 拆分成插件的需求也随之增长。你需要安装 `hapi-auth-basic` 插件才能在 hapi 中获得任何基本认证支持。

为了在 hapi 中存在任何认证支持，你首先必须有一个方案在服务器上注册。该方案是即将进行的认证的核心。就 `hapi-auth-basic` 而言，该方案在插件本身被注册时就会注册。

剩下的唯一事情就是声明一个使用该方案的认证策略。当讨论到 `bell` 时，这一点将变得更加明显，但策略有助于 hapi 成为一个极其灵活的框架，因为它可以支持多个策略。

下面演示了如何注册 `hapi-auth-basic` 插件并将其设置为一个策略。

```
var Hapi = require('hapi');
var Basic = require('hapi-auth-basic');

var server = new Hapi.Server();
server.connection({ port: 3000 });

server.register(Basic, function (err) {
    server.auth.strategy('simple', 'basic', { validateFunc: validate });
});
```

认证策略就位后，它可以被需要认证的各个路由使用。如果你期望所有路由都使用某个特定策略，你可以在声明策略时传递一个 `mode` 选项，并将 `mode` 设置为 `required`。

另一个选项是使用 `try`，这意味着如果提供了凭据就尝试认证，否则继续执行路由生命周期。

第三个选项名为 `optional`，这意味着如果尝试认证失败，则请求失败。在基本认证的情况下，用户名是按原样明文传递的。然而，密码需要进行 base64 编码并以此方式进行验证。在前面的示例中，`validate` 函数缺失了，密码的 base64 编码也缺失了。下面提供了一个更完整的代码示例。

```
var Bcrypt = require('bcrypt');
var Hapi = require('hapi');
var Basic = require('hapi-auth-basic');

var server = new Hapi.Server();
server.connection({ port: 3000 });

var users = {
    molly: {
        username: 'molly',
        password: '$2a$10$iqJSHD.BGr0E2IxQwYgJmeP3NvhPrXaeLSaGCj6IR/XU5QtjVu5Tm',
        name: 'Molly Ringwald',
        id: '2133d32a'
    }
};

var validate = function (username, password, callback) {

    var user = users[username];
    if (!user) {
        return callback(null, false);
    }

    Bcrypt.compare(password, user.password, function (err, isValid) {

        callback(err, isValid, { id: user.id, name: user.name });
    });
};

server.register(Basic, function (err) {

    server.auth.strategy('sobasic', 'basic', { validateFunc: validate });
    server.route({
        method: 'GET',
        path: '/',
        config: {
```

## 第 7 章：认证

```
            auth: 'sobasic',
            handler: function (request, reply) {

                reply('hello, ' + request.auth.credentials.name);
            }
        }
    });

    server.start(function () {

        console.log('server running');
    });
});
```

上面的代码演示了如何通过将策略名称传递给路由配置的 `auth` 属性，来添加一个需要认证的路由。你可以看到 `bcrypt` 库有一个 `compare` 函数，它会告诉我们密码是否有效。因为这里使用了 `bcrypt`，你可以看到密码不是以纯文本形式存储的。这绝对是一个改进。

## hapi-auth-cookie

网站常见的认证方案是使用 cookie 存储安全令牌。类似于基本认证方案依赖于开发者实现一个 `validate` 函数，cookie 认证也期望同样的函数。cookie 认证由模块 `hapi-auth-cookie` 提供。该模块的选项支持许多与 cookie 存储方式相关的属性，例如生存时间或安全标志属性。cookie 认证和基本认证策略之间的一个主要区别是，cookie 认证策略会装饰 `request.auth.session` 对象，添加用于设置或清除会话属性的属性。下面是一个使用 cookie 认证策略并在需要认证的路由上注册的完整应用程序示例。

```
var Hapi = require('hapi');

var users = {
    john: {
        id: 'molly',
        password: 'breakfast',
        name: 'Molly Ringwald'
    }
};

var home = function (request, reply) {
```

hapi-auth-cookie

```
    reply('<html><head><title>Login page</title></head><body><h3>Welcome '
        + request.auth.credentials.name
        + '!</h3><br/><form method="get" action="/logout">'
        + '<input type="submit" value="Logout">'
        + '</form></body></html>');
};

var login = function (request, reply) {

    if (request.auth.isAuthenticated) {
        return reply.redirect('/');
    }

    var message = '';
    var account = null;

    if (request.method === 'post') {

        if (!request.payload.username ||
            !request.payload.password) {

            message = 'Missing username or password';
        }
        else {
            account = users[request.payload.username];
            if (!account ||
                account.password !== request.payload.password) {

                message = 'Invalid username or password';
            }
        }
    }

    if (request.method === 'get' ||
        message) {

        return reply('<html><head><title>Login page</title></head><body>'
            + (message ? '<h3>' + message + '</h3><br/>' : '')
            + '<form method="post" action="/login">'
            + 'Username: <input type="text" name="username"><br>'
            + 'Password: <input type="password" name="password"><br/>'
            + '<input type="submit" value="Login"></form></body></html>');
    }
```

## 第 7 章：认证

```
    request.auth.session.set(account);
    return reply.redirect('/');
};

var logout = function (request, reply) {
    request.auth.session.clear();
    return reply.redirect('/');
};
```

我们在上面设置了基本函数。我们设置了一个用户。我们提供了一个 `login` 函数，它处理用户提交其用户名和密码时的操作。如果用户名或密码无效，它会返回一条消息。最后，如果一切正常，它会通过 `request.auth.session.set` 函数设置一个 cookie。提供了一个 `logout` 函数，用于清除 cookie 然后重定向回主页。最后，我们有一个 `home` 函数，如果他们尚未登录，它只是显示一个表单。现在设置服务器并注册插件。

```
var server = new Hapi.Server();
server.connection({ port: 8000 });

server.register(require('hapi-auth-cookie'), function (err) {
    server.auth.strategy('session', 'cookie', {
        password: 'secret',
        cookie: 'sid-example',
        redirectTo: '/login',
        isSecure: false
    });
});
```

这还不算太糟。我们设置了一个 `cookie` 名称和一个 `password`，并告诉它 `redirectTo` 路径是什么。最后一步是设置路由。

```
server.route([
    {
        method: 'GET',
        path: '/',
        config: {
            handler: home,
            auth: 'session'
        }
    },
    {
        method: ['GET', 'POST'],
        path: '/login',
        config: {
            handler: login,
```



```javascript
auth: {
    mode: 'try',
    strategy: 'session'
},
plugins: {
    'hapi-auth-cookie': {
        redirectTo: false
    }
}
            }
        },
        {
            method: 'GET',
            path: '/logout',
            config: {
                handler: logout,
                auth: 'session'
            }
        }
    ]);

    server.start();
```

在启动服务器并导航到主页 `http://localhost:8000/` 后，您将看到一个登录提示，如下所示。输入用户名和密码 "molly" 和 "breakfast" 将会登录。随后的请求将显示一条消息 "Welcome Molly Ringwald!"。如果您注销，cookie 将被删除且会话将被清除。因此，下一次请求主页将再次显示如下所示的登录提示。为了简单起见，这次我们没有使用 `bcrypt`。

![](img/79450811086e2fc8749ec4d309ea2b79_82_0.png)

需要注意的是，人们可能会倾向于将此方法用于一般的 cookie 处理。出于安全原因，将用于登录和注销的会话 cookie 与其他 cookie 分开是非常重要的。如果您想在应用程序中添加其他 cookie，请查看 `yar` 插件。

## 第 7 章：身份验证

### bell

既然我们已经掌握了 hapi-auth-cookie，如果我们希望应用程序使用 OAuth，我们可以做得更高级一些。虽然我们在 hapi-plugins.com 网站中没有这样做，但我们可以通过一个类似的示例来演示。我们可以将从 hapi-auth-cookie 中学到的知识与 `bell` 结合起来，展示如何同时使用多种策略。例如，您可能希望拥有本地用户，但为了方便，通过 OAuth 用户名来增强应用程序。实现此功能的代码如下所示。

```javascript
var Hapi = require('hapi');
var AuthCookie = require('hapi-auth-cookie');
var Bell = require('bell');

var publicHandler = function (request, reply) {

    return reply('Everyone can see this...');
};

var privateHandler = function (request, reply) {

    return reply('Welcome ' + request.auth.credentials.name);
};

var login = function (request, reply) {

    if (request.auth.isAuthenticated) {
        request.auth.session.set({
            name: request.auth.credentials.profile.displayName
        });
        return reply('Logged in...');
    }

    return reply('Not logged in...');
};

var logout = function (request, reply) {

    request.auth.session.clear();
    return reply('Logged out...');
};
```

这段代码的第一部分建立了我们的基本函数。您可以看到有一个 `publicHandler` 用于任何匿名用户都可以看到的内容。通常，匿名内容包括登录页面及其资源。`privateHandler` 是一个已经通过身份验证的函数，它仅告诉我们存储的名称是什么。`login` 存储我们在 `privateHandler` 中使用的名称，该名称由 `bell` 放入一个 profile 变量中。最后，我们有注销函数，用于清除会话/cookie。

```javascript
// Create server
var server = new Hapi.Server();
server.connection({ port: 8080 });

server.register([AuthCookie, Bell], function (err) {

    // auth options
    var authCookieOptions = {
        password: 'secret',
        cookie: 'cookieName',
        redirectTo: '/login',
        isSecure: false
    };
    var bellAuthOptions = {
        provider: 'github',
        password: 'secret',
        clientId: 'clientId',
        clientSecret: 'clientSecret',
        isSecure: false
    };

    // strategies
    server.auth.strategy('CookieAuth', 'cookieName', authCookieOptions);
    server.auth.strategy('YourThirdPartyAuth', 'bell', bellAuthOptions);
});
```

到此为止，您已经设置了服务器、连接并注册了插件。此外，您还为 `bell` 和 `hapi-auth-cookie` 设置了策略。在本例中，我们展示了如何为 github 实现这一点。您需要通过 github 账号生成 `clientId` 和 `clientSecret` 并将这些信息提供给 `bell`。最后一步是提供路由并启动服务器。

```javascript
// routes
server.route({
    method: 'GET',
    path: '/public',
    handler: publicHandler
});
server.route({
    method: 'GET',
    path: '/private',
    handler: privateHandler,
    config: {
        auth: 'YourCookieAuth'
    }
});
server.route({
    method: 'GET',
    path: '/login',
    handler: login,
    config: {
        auth: 'YourThirdPartyAuth'
    }
});
server.route({
    method: 'GET',
    path: '/logout',
    handler: logout,
    config: {
        auth: 'YourCookieAuth'
    }
});

server.start(function () {

    console.log('Started...');
});
```

您可以在这里看到，我们的注销和私有 URL 仍然受到 cookie 的保护。我们为 /public 资源提供了一个公共处理程序，它可以像我们在 cookie 示例中那样是一个通用的登录页面。最后，我们有一个登录页面，它会跳转到第三方身份验证站点（github）以获取令牌。Bell 为您完成了这些魔法操作，一旦您获得了令牌，cookie 将被生成。在您的会话过期之前，您不需要再次登录。有关 bell 支持的提供商具体细节，请访问 bell。

## 总结

在本章中，我们探索了 hapi 身份验证的一些基本选项。基础身份验证策略对于由防火墙保护且面向内部的应用程序非常有用。

Cookie 身份验证策略可能更有用，特别是对于需要会话的网站构建。将 cookie 身份验证策略与 bell 结合，可以为您提供一个非常健壮的身份验证解决方案。hapi 的优点之一是它支持将这些以及其他身份验证策略混合使用，以满足您构建的应用程序的需求。无论选择哪种方式，请放心，hapi 的创建者和广大社区已经测试并支持许多不同类型的身份验证策略。

# 模型 8

将其管道传输到 `/dev/null`... 这算 web 规模吗？

> -- 关于 MongoDB 的幽默视频

模型为任何有用的 Web 应用程序提供骨架。它们负责管理数据：连接到数据源、读取数据、创建数据等等。关于数据的决定——包括数据库选择、架构设计和索引设计——都会对应用程序的性能甚至行为产生巨大影响。

数据可以来自任何地方：来自 Web、来自数据库、来自文件或来自服务。对于我们的 **hapi-plugins** 应用程序，我们将重点关注通过 HTTP 从 Web 获取数据以及从数据库获取数据。

## 使用 HTTP

一种获取应用程序数据的流行方法是使用第三方 Web API。您的应用程序可能希望连接到 Twitter、Facebook 或 Google API。大多数这些服务通过 HTTP 或 HTTPS 提供 RESTful API。这类 API 极其容易使用，可以用任何编程语言或操作系统进行调用。

### 预期用法

在对 hapi-plugins.com 应用程序进行编码之前，我们分析了 NPM API 并确定了八个相关的 API：

- 获取所有插件名称的列表
- 获取匹配输入关键字字符串的插件列表
- 根据名称获取插件列表
- 根据被依赖项获取插件列表
- 获取每日插件下载量
- 获取每周插件下载量
- 获取每月插件下载量
- 获取每年插件下载量

由此，我们可以像下面这样设计我们预期的 JavaScript API：

```javascript
/* inside a handler: */
var NPMPackages = new this.models.npm.Packages();
NPMPackages.getShortList(callback);
NPMPackages.getByName('hapi', callback);
NPMPackages.getByKeyword('hapijs', callback);
NPMPackages.getDependedUpon('hapi', callback);

var NPMDownloads = new this.models.npm.Downloads();
NPMDownloads.lastDay('hapi', callback);
NPMDownloads.lastWeek('hapi', callback);
NPMDownloads.lastMonth('hapi', callback);
NPMDownloads.lastYear('hapi', callback);
```

### NPM 软件包

首先，我们配置一个可实例化的模型类对象 NPMPackages。

```javascript
var Hoek = require('hoek');
var Wreck = require('wreck');
var Util = require('util');

var internals = {};
internals._defaults = {};

internals.NpmPackages = function (options) {

    var Packages = function (override) {

        this.options = Hoek.applyToDefaults(internals._defaults, options || {});
    };

    return Packages;
};

module.exports = internals.NpmPackages;
```

对于每个模型，我们希望在顶部保留典型的 require 语句。hapi 风格指南规定使用一个模块特定的 internals 对象，该对象本质上是本地私有的（无法从本文件外部访问或读取）。在内部，我们可以设置全局选项（在 _defaults 对象中），这些选项稍后可以被覆盖。不过，这段代码目前还没有设置默认值。



## 第 8 章：模型 (Models)

然后，我们定义一个将成为模型的 JavaScript 对象。在这种情况下，我们有一个外部对象 (`NpmPackages`) 和一个内部对象 (`Packages`)。通过设置外部对象，我们可以向内部的最终对象传递特定于实例的选项。

接下来，在添加函数之前，我们将重要的配置变量放入 `defaults` 中。

我们知道，无需任何额外参数即可从 URL "https://skimdb.npmjs.com/registry/_all_docs" 获取简短列表（shortlist）。但其他搜索 API 确实需要参数。我们将所有 URL 抽象为两部分：基础 URL (base URL) 和参数化 URI 路径。因此，在实际的请求函数内部，我们将拼接基础 URL 和 URI 来生成最终的 URL。这就是为什么 URI 是函数的原因。

```javascript
var Hoek = require('hoek');
var Wreck = require('wreck');
var Util = require('util');

var internals = {};
internals._defaults = {
    host: 'https://registry.npmjs.org',
    hostShortList: 'https://skimdb.npmjs.com',
    uris: {
        byShortList: function () { return "/registry/_all_docs"; },
        byName: function (name, version) {
        {
            if (version) {
                return Util.format("/%s/%s", name, version);
            } else {
                return Util.format("/%s", name);
            }
        },
        byKeyword: function (kw) { return Util.format('/-/_view/byKeyword?startkey=["%s"]&endkey=["%s",{}]&group_level=3', kw, kw); },
        byDependedUpon: function (kw) { return Util.format('/-/_view/dependedUpon?group_level=3&startkey=["%s"]&endkey=["%s",{}]&skip=0&limit=1000', kw, kw); }
    }
};

internals.NpmPackages = function (options) {
    var Packages = function (override) {
        this.options = Hoek.applyToDefaults(internals._defaults, options || {});
    };
    return Packages;
};

};

module.exports = internals.NpmPackages;
```

接下来，我们添加一个用于调用简短列表请求的函数。

```javascript
// ...
Packages.prototype.getShortList = function (callback() {

    var method = "GET";
    var url = this.options.hostShortList + this.options.uris.byShortList();
    var options = {
        redirects: 3,
        timeout: 90000,
        rejectUnauthorized: true
    };

    var processResponse = function (err, body) {

        // Leave room in case response modification required
        return callback(err, JSON.parse(body.toString()));
    };

    var readResponse = function (err, res) {

        if (err) {
            return callback(err);
        }

        Wreck.read(res, {json:true}, processResponse);
    };

    var req = Wreck.request(method, url, options, readResponse);
};
// ...
```

Wreck 要求你指定四个元素：一个 HTTP 方法、一个 URL、一个可选的 options 参数以及一个回调方法。我们按照之前描述的方式生成 URL。

我们还定义了两个响应回调函数。第一个 `readResponse` 从请求中返回响应对象，并告知 wreck 将响应解析为 JSON 对象。第二个 `processResponse` 不是必须的，但很有用，以防在将响应传递给控制器中的业务逻辑之前需要对其进行修改。

例如，在将对象传递给用户之前，可能需要从中删除敏感或安全字段。或者响应模式（schema）可能与期望的输出不匹配。在我们的案例中，直接原样传递即可。

最后，我们对剩余的 API 方法重复上述步骤：

```javascript
// ...
Packages.prototype.getShortList = function (callback) {

    var method = "GET";
    var url = this.options.hostShortList + this.options.uris.byShortList();
    var options = {
        redirects: 3,
        timeout: 90000,
        rejectUnauthorized: true
    };

    var processResponse = function (err, body) {

        // Leave room in case response modification required
        return callback(err, body);
    };

    var readResponse = function (err, res) {

        if (err) {
            return callback(err);
        }

        Wreck.read(res, {json:true}, processResponse);
    };

    var req = Wreck.request(method, url, options, readResponse);
};

Packages.prototype.getByName = function (arg, callback) {

    var method = "GET";
    var name = arg;
    var version = null;
    if (arg.indexOf('@') >= 0) {
        var args = arg.split('@');
        name = args[0];
        version = args[1];
    }

    var uri = this.options.host + this.options.uris.byName(name, version);
    var options = {
        redirects: 3,
        timeout: 90000,
        rejectUnauthorized: true
    };

    var processResponse = function (err, body) {
        // Leave room in case response modification required
        return callback(err, body.rows || body);
    };

    var readResponse = function (err, res) {

        if (err) {
            return callback(err);
        }

        Wreck.read(res, {json:true}, processResponse);
    };

    var req = Wreck.request(method, uri, options, readResponse);
};

Packages.prototype.getByKeyword = function (keyword, callback) {

    var method = "GET";
    var uri = this.options.host + this.options.uris.byKeyword(keyword);
    var options = {
        redirects: 3,
        timeout: 30000,
        rejectUnauthorized: true
    };

    var processResponse = function (err, body) {

        // Leave room in case response modification required
        return callback(err, body);
    };

    var readResponse = function (err, res) {

        if (err) {
            return callback(err);
        }

        Wreck.read(res, {json:true}, processResponse);
    };

    var req = Wreck.request(method, uri, options, readResponse);
};

Packages.prototype.getDependedUpon = function (keyword, callback) {

    var method = "GET";
    var uri = this.options.host + this.options.uris.byDependedUpon(keyword);
    var options = {
        redirects: 3,
        timeout: 30000,
        rejectUnauthorized: true
    };

    var processResponse = function (err, body) {
        // Leave room in case response modification required
        return callback(err, body);
    };

    var readResponse = function (err, res) {
        if (err) {
            return callback(err);
        }

        Wreck.read(res, {json:true}, processResponse);
    };

    var req = Wreck.request(method, uri, options, readResponse);
};
// ...
```

### NPM 下载量 (NPM Downloads)

开始之前，我们再次配置另一个可实例化的模型类对象 `NPMDownloads`。遵循之前的约定，我们将 URL 分为 host 和参数化 URI 函数。我们知道所有四个 API 函数基本上都是相同的，只有 URI 有细微差别，因此，我们定义了一个共享方法 `getDownloadsBy` 供其他方法使用。

`lastYear` 的 URI 比其他 URI 稍微复杂一些，因为我们需要计算今天和一年前今天的日期范围。但一旦你将其分解，它其实并不复杂。

```javascript
var Hoek = require('hoek');
var Wreck = require('wreck');

var internals = {};

internals._defaults = {
    host: 'https://api.npmjs.org',
    uris: {
        'last-day': function (_module) { return '/downloads/range/last-day/' + _module; },
        'last-week': function (_module) { return '/downloads/range/last-week/' + _module; },
        'last-month': function (_module) { return '/downloads/range/last-month/' + _module; },
        'last-year': function (_module) {

            var today = new Date();
            var from = [today.getFullYear() - 1,today.getMonth() + 1, today.getDate()].join('-');
            var to = [today.getFullYear(),today.getMonth() + 1, today.getDate()].join('-');
            var dateRange = [from, to].join(':');
            return '/downloads/range/' + dateRange + "/" + _module; }
    }
};

internals.NpmDownloads = function (options) {

    this.options = Hoek.applyToDefaults(internals._defaults, options || {});
    return this;
};

internals.NpmDownloads.prototype.getDownloadsBy = function () {};
internals.NpmDownloads.prototype.lastDay = function () {};
internals.NpmDownloads.prototype.lastWeek = function () {};
internals.NpmDownloads.prototype.lastMonth = function () {};
internals.NpmDownloads.prototype.lastYear = function () {};

module.exports = internals.NpmDownloads;
```

接下来，我们填充用于调用下载请求的共享函数。但与之前的函数不同，这个函数返回一个函数，我们用它来生成其他请求。其他函数基本上成为了 `getDownloadsBy` 的包装器。

```javascript
// ...
internals.NpmDownloads.prototype.getDownloadsBy = function (_type, range) {

    var self = this;
    return function (moduleName, callback) {

        var method = "GET";
        var uri = self.options.host + self.options.uris[range](moduleName);
```



## 使用 HTTP

```javascript
var options = {
    redirects: 3,
    timeout: 30000,
    rejectUnauthorized: true
};

var processResponse = function (err, body) {

    // 为可能需要修改响应的情况预留空间
    return callback(err, body);
};

var readResponse = function (err, res) {

    if (err) {
        return callback(err);
    }

    Wreck.read(res, {json:true}, processResponse);
};

var req = Wreck.request(method, uri, options, readResponse);
```

最后，我们通过配置函数之间的差异，来构建用于剩余 API 方法的 `getDownloadsBy`：

```javascript
// ...
internals.NpmDownloads.prototype.lastDay = function (moduleName, callback) {

    return this.getDownloadsBy('point', 'last-day')(moduleName, callback);
};

internals.NpmDownloads.prototype.lastWeek = function (moduleName, callback) {

    return this.getDownloadsBy('point', 'last-week')(moduleName, callback);
};

internals.NpmDownloads.prototype.lastMonth = function (moduleName, callback) {

    return this.getDownloadsBy('point', 'last-month')(moduleName, callback);
};

internals.NpmDownloads.prototype.lastYear = function (moduleName, callback) {

    return this.getDownloadsBy('point', 'last-year')(moduleName, callback);
};
// ...
```

## 第 8 章：模型

### 插件模型：实际使用

回到处理器中，我们希望将 NPM 包搜索结果与一个包数组合并。我们还需要确保列表按名称唯一。然后，对于每个唯一的模块，我们需要使用 `getByName` 获取完整的模块数据。最后，我们希望将这个列表批量添加/更新到数据库中。

为了确保唯一性，我们使用了一个名为 lodash 的库和它的 `uniq` 函数。我们传入一个仅包含模块名称的列表，它将去除重复项。但首先，我们需要获取一个与 hapi 相关的模块列表。

```javascript
Async.parallel({
    shortlist: function (cb) { return NPMPackages.getShortList(cb); },
    hapiKeyword: function (cb){ return NPMPackages.getByKeyword('hapi', cb); },
    hapijsKeyword: function (cb){ return NPMPackages.getByKeyword('hapijs', cb); },
    hapidotjsKeyword: function (cb){ return NPMPackages.getByKeyword('hapi.js', cb); },
}, function (err, results) {
    //...
```

正如我们之前所见，我们在这里使用了 Async parallel 模式来同时请求四个 API 调用并合并结果。这很重要，因为我们需要来自所有四个源的数据来识别哪些插件与 hapi 相关。

```javascript
var hapiKeyword = results.hapiKeyword.rows.map(function (module)
{

    return module.key[1];

});

var hapijsKeyword = results.hapijsKeyword.rows.map(function
(module){

    return module.key[1];
});

var hapidotjsKeyword = results.hapidotjsKeyword.rows.map(function(module){
  return module.key[1];
});
```

这四个源中的一些返回的数据格式相同，比如三个与关键词相关的调用，因此我们通过 `map` 函数遍历这些结果，将响应转换为一个简单的插件名称数组。在这种情况下，对于所有三个关键词响应，名称都存储在 `module.key[1]` 中。

```javascript
var NameMatchSuffix = /[-]hapi/ig;
var NameMatchPrefix = /hapi[-]/ig;

var shortlist = results.shortlist.rows.filter(function(module){
  return NameMatchPrefix.exec(module.id) || NameMatchSuffix.exec(module.id);
}).map(function(module){
  return module.id;
});
```

短列表返回所有插件名称的简单列表，因此我们需要应用一个正则表达式来仅查找与 hapi 相关的插件。这就是 `NameMatchPrefix` 和 `NameMatchSuffix` 的作用。

```javascript
// 确保列表唯一
var plugins = _.uniq(shortlist.concat(hapiKeyword).concat(hapijsKeyword).concat(hapidotjsKeyword));
```

接下来，带有 `_.uniq()` 的这一行将合并来自这四次调用的所有模块名称，并通过 lodash 的 `unique` 函数去除重复项。现在，我们有了一个列表，其中包含所有名称中带有 `hapi-` 或 `-hapi`，或者在关键词中包含这些字符串的模块。

然而，这只是一个名称列表。要执行任何有用的操作，我们需要与每个模块关联的数据。因此，我们使用 Async.map 函数将 `NPMPackages.getByName` 函数应用于每个模块名称。这将并行执行所有单独的 API 调用，并在最后合并结果以生成一个模块数据列表。

```javascript
// 异步地将 getPluginData 应用于 plugins 中的每个元素
Async.map(plugins, NPMPackages.getByName, function(err, results){
//...
```

从这里开始，我们需要过滤掉未发布的模块，并最终返回结果（或错误）。

为了看到整体情况，下面是整个函数放在一起的样子：

```javascript
var _ = require('lodash');
var NameMatchSuffix = /[-]hapi/ig;
var NameMatchPrefix = /hapi[-]/ig;
// ...
module.exports.populateReal = {
    handler: function (request, reply) {

        var NPMPackages = new this.models.npm.Packages();
        Async.parallel({
            shortlist: function (cb) { return NPMPackages.getShortList(cb); },
            hapiKeyword: function (cb){ return NPMPackages.getByKeyword('hapi', cb); },
            hapijsKeyword: function (cb){ return NPMPackages.getByKeyword('hapijs', cb); },
            hapidotjsKeyword: function (cb){ return NPMPackages.getByKeyword('hapi.js', cb); },
        }, function (err, results){

            if (err) {
                throw err; // TODO: 替换为 boom err
            }

            // 为每组搜索结果生成键列表
            var shortlist = results.shortlist.rows.filter(function (module){
                return NameMatchPrefix.exec(module.id) || NameMatchSuffix.exec(module.id);
            }).map(function (module){
                return module.id;
            });

            var hapiKeyword = results.hapiKeyword.rows.map(function (module){
                return module.key[1];
            });
            var hapijsKeyword = results.hapijsKeyword.rows.map(function (module){
                return module.key[1];
            });
            var hapidotjsKeyword = results.hapidotjsKeyword.rows.map(function (module){
                return module.key[1];
            });

            // 确保列表唯一
            var plugins = _.uniq(shortlist.concat(hapiKeyword).concat(hapijsKeyword).concat(hapidotjsKeyword));

            // 异步地将 getPluginData 应用于 plugins 中的每个元素
            Async.map(plugins, NPMPackages.getByName, function (err, results){
                if (err) {
                    throw err;
                }

                // 确保不添加未发布的模块
                results = results.filter(function (result){
                    if (result.time.hasOwnProperty('unpublished')) {
                        if (new Date(result.time.unpublished.time) > new Date(result.time.modified)) {
                            return false;
                        }
                    }
                    return true;
                });

                // 用结果更新数据库
                DB.plugin.batchCreate(results, function (err, success) {
                    if (err) {
                        throw err;
                    }
                    return reply("<pre>" + JSON.stringify(results, null, 2) + "</pre>");
                });
            });
        }
    }
};
```

现在你已经看到了两种创建调用 RESTful API 端点的模型的方式。一种是进行请求的通用方法，另一种是生成用于请求的包装器。应该很容易将这些示例中的任何一个应用到你自己的项目中，以适应其他第三方 RESTful API。

接下来，我们将继续探索模型以及如何连接和查询数据库。

## 使用数据库

一般来说，开发者在使用 hapi 与数据库时具有完全的灵活性——任何数据库、任何 ORM 或任何库都可以使用。hapi 不施加任何限制。你可以为一个项目使用一个数据库，为另一个项目使用另一个，或者为第三个项目使用十个数据库。hapi 试图通过不碍事来让开发者满意。

对于 github.com/hapijs/hapi-plugins.com 应用程序，我们为数据库选择了流行的 MongoDB，并将使用 Mongoose 驱动程序连接到我们的数据库。有关其他数据库选项的信息以及我们选择 MongoDB 的原因，请参见第 13 章附录的模型部分。

## 设置数据库

为应用程序设置 MongoDB 在 mongodb.org 上有相当完善的文档。但是，为了快速开发，在本地进行开发或使用 Compose（又名 MongoHQ）为你生成一个免费的开发数据库实例会更快。

一旦实例设置好，就必须创建一个数据库名称。我们选择了实例名称 'hapi-plugins' 和数据库名称 'hapi-plugins'。如果你更改了这些名称，请记得在下面示例中的连接字符串中替换它们。如果你使用用户名和密码设置了身份验证（就像我们在生产数据库中设置的那样），请记得将其添加到连接字符串中。

集合是文档的列表。Mongoose 会在你使用它时为你创建这些集合，因此除非你想设置大小和最大文档限制，否则没有必要手动创建。

## 连接到数据库

Mongoose 提供了一个用于连接 MongoDB 实例的高级 API。它只接受一个 MongoDB 连接字符串，该字符串可以包含主机、用户名、密码、数据库等。随后对数据库的调用和查询会自动排队，直到连接建立。



连接即告完成。因此，在等待连接建立时，无需将代码嵌套在异步块中。

在 hapi-plugins.com 应用中，开发时我们希望连接到本地运行的 MongoDB 实例，而在部署后则希望连接到生产数据库。我们使用环境变量来决定运行环境。Node.js 的全局、进程级变量 `process.env` 包含了我们应用可用的所有 shell 环境变量。

要启用生产环境，我们运行应用时使用 `PRODUCTION=1 node index.js`。

*注意：*本章中的生产数据库凭据已移除密码。请将其替换为您创建的数据库的适当凭据。

```javascript
var databases = {
    development: 'mongodb://localhost/hapi_plugins',
    production: 'mongodb://hapi:{{PASSWORD}}@c278.lighthouse.0.mongolayer.com:10278,c278.lighthouse.1.mongolayer.com:10278/hapi-plugins?replicaSet=set-54ebe690660d07da1a000f09'
};

if (process.env.PRODUCTION) {
    Mongoose.connect(databases.production);
}
else {
    Mongoose.connect(databases.development);
}
```

使用这种模式，我们可以轻松区分不同的环境。本地开发时使用本地数据库，而生产环境则使用实时、可扩展的托管数据库。

另一种模式是将数据库连接字符串本身放在环境变量中，如下所示：

```javascript
// $ `MONGOSTR='mongodb://localhost/hapi_plugins' node index.js`
Mongoose.connect(process.env.MONGOSTR);
```

这样做的好处是不会在代码中的任何地方存储连接字符串。如果您打算开源代码，或者您的应用服务器被入侵，这可能极其重要，因为黑客在阅读代码后会直接获得数据库的访问权限。

## 第 8 章：模型

## 模式设计

在向数据库发起任何查询之前，通常最好先设计一个粗略的模式。尽管 MongoDB 不需要正式的模式，但定义数据的结构仍然是一个良好的实践，可以帮助您强制数据类型。首先了解您计划如何访问和使用数据会很有帮助。

对于 hapi-plugins.com 应用，我们计划允许匿名访客：

- 按名称、描述、作者和关键词搜索插件
- 登录并管理他们的插件
- 将自己的插件添加到列表中
- 点赞或取消点赞插件

在后台，我们还需要能够：

- 将插件添加到列表中
- 从列表中移除插件

因此，我们知道插件必须有名称、描述、作者和关键词。NPM 已经禁止重复的模块名称，所以名称将是唯一的，因此我们可以将名称用作主键。此外，从查看 NPM 可知，NPM 模块还有版本、许可证、仓库 URL、主页、依赖项、被依赖项以及各种统计信息。它还有关于模块创建和更新时间的时间信息。由此，我们可以为 hapi-plugins 应用定义第一个模式。

```javascript
var internals = {};

internals.plugin = new Mongoose.Schema({
    'name': { type: String, required: true },
    'description': { type: String, required: false },
    'version': { type: String, required: true },
    'authors': { type: Array, required: false },
    'license': { type: String, required: false },
    'repository': { type: String },
    'homepage': { type: String },
    'updated_at': { type: Date, default: Date.now },
    'created_at': { type: Date, default: Date.now },
    'keywords': { type: Array },
    'dependencies': { type: Array },
    'dependents': { type: Array },
    'stats': {
        'releases': { type: String },
        'downloads': { type: String },
        'downloads_this_month': { type: String },
        'open_issues': { type: String },
        'pull_requests': { type: String }
    }
});

var plugin = Mongoose.model('plugin', internals.plugin);
```

在上述模式中，我们定义了每个文档中的所有相关字段以及一些数据类型要求。在某些情况下，还设置了后备默认值，以防在创建时未为这些字段提供值。

MongoDB 可以让我们快速查找已建立索引的字段上的项目。如果我们最终搜索未建立索引的内容，MongoDB 必须搜索整个文档列表。由于我们必须能够快速跨不同字段进行搜索，因此必须使用索引。

```javascript
// ...
internals.plugin.index({
    name: 1,
    description: 1,
    authors: 1,
    keywords: 1
});
```

现在来看用户，我们知道他们应该有用户名、可能的显示名称、电子邮件地址、创建/更新时间戳以及点赞列表。由于我们使用的是 MongoDB，数据应该被反规范化（意思是应该 grouping 而不是拆分到单独的表中，即使这意味着重复）。插件的"点赞"与用户关联是合理的，因为抽象地说，每个用户基本上都有一组点赞。

```javascript
var internals = {};

internals.user = new Mongoose.Schema({
    'username': { type: String, required: false },
    'name': { type: String, required: false },
    'email': { type: String, required: false },
    'updated_at': { type: Date, default: Date.now },
    'created_at': { type: Date, default: Date.now },
    'likes': [internals.plugin]
});

var user = Mongoose.model('user', internals.user);
```

## 搜索插件

hapi-plugins.com 应用最关键的部分是用户能够搜索插件。我们希望搜索是灵活的。访客可能知道插件名称并按名称搜索。他们可能只知道插件"需要"做什么，从而可以搜索关键词或描述中可能出现的词语。最后，访客可能知道是谁创建了插件，因此他们可以搜索该作者的所有插件。

实现这一点的逻辑有点复杂。它涉及生成一个 MongoDB 查询，同时在所有相关字段中搜索查询字符串。在下面的示例中，它正在生成一个符合我们条件的 MongoDB 查询对象并执行它。

```javascript
internals.plugin.statics.search = function (queryString, sortString, callback){

    var query = {};
    if (queryString && queryString.length > 0) {
        var pattern = new RegExp(queryString, 'ig');
        query = {
            '$or': [
                {'name': pattern},
                {'description': pattern},
                {'author': pattern},
                {'authors': {
                    '$regex': pattern
                }},
                {'keywords': {
                    '$regex': pattern
                }}
            ]
        };
    };

    var sortOrder = 1;
    var sortBy = sortString || 'name';
    if (sortBy[0] === '-') {
        sortOrder = -1;
        sortBy = sortBy.slice(1);
    }

    var sort = {};
    sort[sortBy] = sortOrder;
    return this.find(query).sort(sort).exec(callback);
};
```

上面的搜索函数中有很多事情发生。首先，搜索函数接受两个重要参数和一个回调函数，结果将通过该回调发送。

第一个是用户发出的查询。我们获取该查询并告诉数据库将其与所有相关字段匹配：名称、描述、作者、作者们和关键词。

第二个参数决定排序顺序。当我们从数据库获取结果时，它必须知道以什么顺序返回它们（升序或降序，以及按什么字段）。我们使用 "-name" 这样的约定来表示按名称降序，没有减号 "-" 表示升序。如果 sortString 为 null，则默认按名称升序。

我们获取这两个参数并在数据库上执行查找查询。

现在，回到控制器中，我们可以定义一个搜索处理程序来使用我们新的数据库搜索方法。在这个处理程序中，我们还将验证和清理输入，以确保没有输入无效或恶意的数据。

```javascript
module.exports.search = {
    validate: {
        query: {
```



```javascript
q: Joi.string(),
sort: Joi.string().optional(),
fields: Joi.string().optional()
},
handler: function (request, reply) {

    var query = null;
    var sort = null;
    if (request.query.q) {
        query = Xss(request.query.q);
    }
    if (request.query.sort) {
        sort = Xss(request.query.sort);
    }
    DB.plugin.search(query, sort, function (err, results){

        if (err) {
            return reply({status:-1, error: err}).code(500);
        }
        return reply(JSON.stringify(results, null, 2));
    });
}
};
```

在上述搜索处理器中，我们为查询参数设置了验证规则，这与我们在第 5 章"验证"中所展示的方式相同。上面展示的一个新约定涉及 *Xss* 模块。该模块/函数通过转义 HTML 实体和其他可能的恶意手段来对输入进行清理。你将在本书稍后的第 12 章"安全"中了解更多关于这方面的内容。

在输入经过验证和清理之后，我们将该请求传递给模型的搜索函数。在回调函数内部，如果返回了错误，我们会返回一个格式良好的 JSON 错误消息。但如果成功，我们则会返回一个格式优美的 JSON 响应。

这就是我们如何让用户通过我们的插件仓库进行搜索。不过目前里面还没有任何内容！

## 添加插件

为了搜索插件，我们需要一个包含实际插件及其数据的数据库。获取匹配的 NPM 模块列表此前已经介绍过。目前，我们需要具备将单个插件添加到数据库的能力。

```javascript
internals.plugin.statics.createOrUpdate = function (pluginJS,
callback) {

    var self = this;
    var pluginObj = internals.pluginJStoObj(pluginJS);
    self.update({ name: pluginObj.name }, pluginObj, function (err, numberAffected, raw) {

		if (numberAffected === 0) {
			var plugin = new self(pluginObj);
			return plugin.save(callback);
		}

		return callback(err);
	});
};
```

MongoDB 的行为与其他数据库不同。通过"更新"插件名称的文档来添加新插件是更安全的做法。这样，如果它已经存在，就可以同时被更新；但如果它尚不存在，则会被创建。

此外，在 `createOrUpdate` 函数内部，我们使用了一个尚未定义的函数 `internals.pluginJSToObject`。我们将在第 9 章"模板"中定义它，届时我们会从 NPM 接收数据并将其映射到我们的模式。

另外，为了作为开发者的便利，我们还添加了一个用于异步批量添加插件的函数。在该函数内部，我们还添加了一些代码，以防止未发布的 NPM 模块被注册到我们的数据库中。

```javascript
internals.plugin.statics.batchCreate = function (pluginsJS, callback) {

	var self = this;
	var addPlugin = function (pluginJS) {

		return function (next) {

			self.createOrUpdate(pluginJS, next);
		};
	};

	var batch = [];

	for (var i = 0, il = pluginsJS.length; i < il; ++i) {
		var pluginJS = pluginsJS[i];
		var unpublished = Hoek.reach(pluginJS, 'time.unpublished');

		if (!unpublished) {
			batch.push(addPlugin(pluginJS));
		}
	}

	Async.parallel(batch, callback);
};
```

这使得一次性向数据库添加多个条目变得更加容易，而无需为每个条目手动调用添加函数。由于这些数据库操作通常通过网络运行，它们确实是异步的。因此，Async.parallel 以真正的并行方式运行，可以非常快速地完成此操作。

## 总结

在本章中，我们学习了如何连接第三方 HTTP API，以及处理与数据库相关的内容：定义模式、执行查询和添加文档。你现在可以自定义并添加自己的集合或数据库了。如前所述，本书附录中有一节参考，提供了使用其他流行数据库的示例。接下来，我们将了解如何获取这些数据，并通过模板以人类可读的方式展示给用户。

## 模板

在上一章（第 8 章"模型"）中，我们看到了获取和存储数据是多么容易。现在，我们将了解如何将数据呈现给用户。

hapi 主要用于构建 RESTful JSON API。然而，在 Web 开发中，响应 HTTP 请求并返回由浏览器渲染的 HTML 往往至关重要或有很大帮助。由于输出响应依赖于输入，或依赖于请求数据的哪个用户，因此简单地为每个响应硬编码相同的响应并不总是可行或理想的。自定义响应的最佳方法是使用模板。在 hapi 中，模板被称为**视图（views）**。

hapi 开箱即用地支持大多数模板引擎。本章将包含六种最流行引擎的工作示例：Handlebars.js、Mustache.js、Jade、Dust、eco 和 ECT。关于这些引擎的概述，请参阅本书末尾的附录。

在典型的 Web 应用程序中，终端用户访问一个 URL，该 URL 映射到 Web 服务器中的一个处理器，处理器执行一些业务逻辑来准备数据，最后，Web 服务器以 HTML 格式向终端用户响应数据。

响应 HTML 有多种不同的方式。两种主要方法是**拼接**和**模板系统**。

在 Web 开发的早期，HTML 是通过拼接或添加 HTML 字符串与变量来生成的，大概就像这样：

```javascript
var html = '<html><head><title>' +
    page_title +
    '</title></head><body>' +
    content +
    '</body></html>';
return reply(html);
```

值得庆幸的是，这种繁琐且缺乏灵活性的方法已经过时，并被现代模板系统所取代。然而，这种拼接方法仍然是可行的，某些团队可能会在仅需一行响应的情况下出于效率考虑而使用它。

与此同时，对于现代 Web 应用程序而言，模板系统将一个负责输格式化的模板与数据合并为一种统一的格式——比如 HTML。

例如，一个 Handlebars（或 Mustache）模板像这样：

```html
<html>
    <head>
        <title>{{page_title}}</title>
    </head>
    <body>
        {{content}}
    </body>
</html}
```

与这样的上下文数据结合：

```javascript
var context = {
    page_title: 'Templating is fun!',
    content: '<h1>Hello world!</h1>'
}
return reply.view('index', context);
```

将返回这样的 HTML 输出：

```html
<html>
    <head>
        <title>Templating is fun!</title>
    </head>
    <body>
        <h1>Hello world!</h1>
    </body>
</html}
```

使用模板，数据可以快速添加、移动或完全移除。工作可以拆分——设计师处理模板，而开发者提供上下文。模板可以轻松地作为重新设计的一部分进行替换，或根据条件进行替换（如果用户设置指定了偏好，则显示 X 设计；否则显示 Y）。

因此，模板系统比替代方案要省事得多，也灵活得多。

### 配置

在 hapi 中，视图在使用之前必须进行配置。视图必须知道要运行什么引擎以及在何处查找文件——这些是必需的。其他选项则不是必需的。

### 选项

配置视图时，有三个主要选项需要配置：engines、compileMode、paths。在下一节中，我们将发现各种子选项，你可能需要它们来使视图正常工作。

### 引擎（ENGINES）

`engines` 配置对象告诉视图要查找哪些文件扩展名，以及应该使用什么模板引擎。

engines 对象期望文件扩展名（不带点号 '.'）作为键，模板系统编译器作为值。下面的示例（"engines-breakdown.js"）将匹配 anyfilename.extension 并使用 `some_compiler` 引擎。

```javascript
engines: {
    "extension": require('some_compiler')
},
/* ... */
```

使用此系统，可以混合搭配多种模板系统，只要它们都使用不同的文件扩展名：

```javascript
var Hapi = require('hapi');

var server = new Hapi.Server();
server.views({
    engines: {
        html: require('mu'),
        jade: require('jade'),
        hbs: require('handlebars')
    },
    defaultExtension: 'hbs',
    path: __dirname + '/views'
});
```

如果你出于某种原因混合搭配模板引擎，你应该注意几点。如果你想使用 `reply.view('templateName', context)` 语法，它需要理解默认扩展名是什么。在上面的示例中，你可以看到我们如何挑选 `hbs` 作为该默认扩展名。此设置不是必需的。你可以直接添加扩展名，如 `reply.view('templateName.hbs', context)`。如果文件具有不是 `defaultExtension` 的扩展名，那么你需要给出该扩展名。



## 第九章：模板化

### COMPILEMODE 选项

`compileMode` 选项用于告诉 hapi 模板引擎是同步的还是异步的。hapi 期望引擎对象包含一个 `compile` 方法，该方法可以采用任一种格式，但不能同时支持两者。默认情况下，hapi 期望同步引擎。以下是一个同步的 `compile` 函数。

```
{
    compile: function (template, options) {

        return function (context, optionsOverride) {

            // 返回集成上下文后的字符串模板
        }
    }
}
```

接下来我们以异步方式实现相同功能。

```
{
    compile: function (template, options, callback) {

        var error = null;
        return callback(error, function (context, optionsOverride, internalCallback) {

            var output = ''; /* 设置为集成上下文后的字符串模板 */
            return internalCallback(null, output);
        });
    }
}
```

取决于模板引擎，你稍后可能会看到需要将默认的 `compileMode` 覆盖为 `'async'`。

## 路径配置

hapi 视图需要知道在哪里查找模板文件。根据项目需求，有多种路径配置方式。

- `path`：指向查找模板文件的主目录
- `partialsPath`：指向查找部分模板的目录（如果引擎支持 Partials）
- `helpersPath`：指向定义模板辅助函数的目录（如果引擎支持 Helpers）
- `layoutPath`：包含布局模板的目录（通常是 `layout.{extension}` 或 `layout.html`）
- `relativeTo`：用作其他目录前缀的路径（支持其他路径设置中的相对路径）

此外，还有两个重要的路径相关设置：

- `allowAbsolutePaths`：（布尔值）启用路径设置中的绝对路径使用（默认：false）
- `allowInsecureAccess`：（布尔值）启用向上目录移动的支持（使用 `../`）

`allowInsecureAccess` 变量的使用需极其谨慎。这可能允许用户访问服务器操作系统上其他安全的文件，如密码文件、包含敏感数据的文件等。

## 全局与特定设置

所有全局视图设置都可以应用于特定的模板引擎，这将覆盖任何全局设置。这需要将编译器对象（通常是 `require` 调用的结果）移动到 `module` 键下，以便为其他选项留出空间。在下面的示例（"specific-view-settings.js"）中，默认的 `compileMode` 已更改为 `'async'`，但 `.html` 文件将使用 handlebars 在同步编译模式下执行或渲染。

```
engines: {
    compileMode: 'async',
    engines: {
        html: {
            module: require('handlebars'),
            compileMode: 'sync'
        }
    },
    path: '/path'
}
```

## 更多选项

更多选项在 **API 文档** 中有详细说明。

## 入门示例

首先，我们从 Mustache.js 开始。

```
var Hapi = require('hapi');

var server = new Hapi.Server();
server.views({
    engines: {
        html: require('mu')
    },
    path: __dirname + '/views'
});
```

这很简单。它会在 views 目录中查找 'html' 文件。当你调用之前提到的 `request.view('templateName', { context })` 类型函数时，它将编译并将其提供给客户端。接下来，我们看看 Handlebars.js。

```
var Hapi = require('hapi');

var server = new Hapi.Server();
server.views({
    engines: {
        html: require('handlebars')
    },
    path: __dirname + '/views'
});
```

你可以看到这个示例本质上是相同的。这应该是合理的，因为 Handlebars.js 在很大程度上兼容 Mustache.js。接下来是 jade。

```
var Hapi = require('hapi');

var server = new Hapi.Server();
server.views({
    engines: {
        jade: require('jade')
    },
    path: __dirname + '/views',
    compileOptions: {
        pretty: true
    }
});
```

我们需要在这里添加一个名为 `compileOptions` 的额外设置，并将 `pretty` 设置为 `true`。hapi 试图以通用方式处理这些视图，并且根据模板引擎的不同，你可以看到这些细微的差异。接下来是 dust。

```
var Hapi = require('hapi');

var server = new Hapi.Server();
server.views({
    engines: {
        // 需要 npm 安装 `dustjs-linkedin`
        html: require('hapi-dust')
    },
    path: __dirname + '/views'
}));
```

这再次非常直接。这里唯一需要额外注意的是，你需要安装 dust-linkedin 并在你的 `package.json` 文件中将其列为依赖。最后是最复杂的示例，ECT。

```
var Hapi = require('hapi');
var ECT = require('ect');
var ectRenderer = ECT({
    watch: true,
    root: __dirname + '/views'
});

var server = new Hapi.Server();
server.views({
    engines: {
        ect: {
            compile: function (tmpl, opts) {
                return function (context, engineOptions) {
                    return ectRenderer.render(opts.filename, context);
                }
            },
            compileMode: 'sync'
        }
    },
    basePath: __dirname,
    path: './views'
});
```

你会看到需要更多的配置。我们需要通过提供一个 `compile` 函数来帮助 hapi 完成编译工作。此外，你需要告诉 hapi 在之前本章讨论的 `compileMode` 中使用 `'sync'`。通过展示各种模板引擎，你可以更清楚地看到 hapi 如何处理不同的解决方案。你可以在 hapijs.com 网站的 Plugins 部分下的 Templating 中找到更多的模板解决方案。如果你没有找到所需的内容，请发起讨论或考虑帮助社区添加该模板引擎。

## 视图加载

视图作为回复步骤的一部分，在处理器内部被调用和加载。`reply.view` 函数接受三个参数（最后一个是可选的）：所需模板文件的相对路径、应用于模板的上下文，以及一个用于覆盖全局和引擎特定设置的选项对象。

```
handler: function (request, reply) {

    var context = {
        content: 'hello world'
    };
    // 假设文件可以在 views.path + '/path/index' 中找到
    reply.view('path/index', context, { compileMode: 'sync' });
}
```

提醒一下，我们这里不需要 'index.html'，因为我们已经在 `server.views` 函数的 `engines` 部分定义了扩展名。

## 布局

布局使你能够将所有模板包装在另一个模板中。如果你的网站具有相同的通用外观（例如，徽标、页眉和页脚），这会很有用。然后，你只需要为通用布局设计 HTML，并将普通模板嵌套在 `{{content}}` 上下文变量中。

### 配置

启用布局最重要的步骤是配置。只需要两个额外的配置字段：`layoutPath` 和 `layout`。`layoutPath` 告诉 hapi 在哪里查找 `layout.{{ext}}`，其中 ext 是在引擎视图选项下定义的扩展名。

配置在不同的模板系统之间并没有真正的变化。

```
var Hapi = require('hapi');

var server = new Hapi.Server();
server.views({
    engines: {
        html: require('handlebars') // .html 是 hapi 将查找的后缀
    },
    path: __dirname + '/views',
    layoutPath: __dirname + '/views',
    layout: true
});
```

### 用法

在正确配置后，用法实际上非常简单。处理器方面没有变化：

```
handler: function (request, reply) {

    var ctx = {
        msg: 'Hello world!'
    };
    return reply.view('/path/' + 'templateName', ctx);
}
```

模板将通过布局中的 `content` 变量加载。

### 排除

有时你想将布局应用于所有模板，除了某些特定模板。这非常容易做到。你只需要在 `reply.view` 中包含第三个可选配置参数，将 layout 设置为 false。

```
// 在处理器内部
return reply.view(template_name, context, { layout: false });
```

## 部分模板

部分模板很棒。部分模板允许你提取共享的模板片段，以便在其他模板之间使用。这防止你被迫在多个地方修改代码；你可以编辑一次，并在所有模板中反映出来。

### 配置

要启用部分模板，你只需要添加一个视图选项 `partialsPath`，它告诉 hapi 在哪里查找部分模板。现在当你引用部分模板时，路径将相对于此路径。

配置在不同的模板系统之间并没有真正的变化。然而，一些引擎可能需要进行小的调整才能与 hapi 的部分模板系统一起工作。例如，对于 Hogan.js mustache 模板，在 hapi-hogan 中有一个方便的预调整版本。



## 第 9 章：模板化 (Templating)

```javascript
var Hapi = require('hapi');

var server = new Hapi.Server();
server.views({
    engines: {
        html: require('handlebars') // .html 是 hapi 将要查找的后缀
    },
    path: __dirname + '/views',
    partialsPath: __dirname + '/views/partials'
});
```

### 辅助函数 (Helpers)

辅助函数是模板语言的扩展，允许你在模板内部创建和使用自定义函数。这是 Handlebars.js 的一项特性。

### 配置

要启用辅助函数，你只需要提供一个额外的视图选项 `helpersPath`。这会告知 hapi 在哪里查找辅助函数文件。

```javascript
var Hapi = require('hapi');

var server = new Hapi.Server();
server.views({
    engines: {
        html: require('handlebars') // .html 是 hapi 将要查找的后缀
    },
    path: __dirname + '/views',
    helpersPath: __dirname + '/views/helpers'
});
```

### 辅助函数文件

辅助函数文件的命名应为其预期的调用名称。如果你想创建一个名为 `toMoney` 的辅助函数，文件名应为 `toMoney.js`，并且它应该通过 `module.exports` 导出单个函数（该函数可以接收参数）。

```javascript
module.exports = function (val) {
    return "$" + val.toFixed(2);
};
```

然后，在模板内部，就可以通过参数（可以是变量）来调用 `toMoney`。

```handlebars
{{toMoney 25}}
{{toMoney cost}}
```

## 共享上下文 (Shared Contexts)

通常我们需要将某些数据包含在每个视图的每个上下文对象中。例如，在一个地方维护 HTML 页面标题并将其附加到每个视图，比在每一个单独的视图上下文中包含它要更容易维护。

下面的示例（'shared-context.js'）将使用新值添加（或覆盖）`context.title` 的值。如果处理程序（handler）没有调用 views，那么 `.context` 将不会被定义，也就不会受到影响。

```javascript
server.ext('onPreResponse', function (request, reply) {
    var response = request.response;
    if (!response.isBoom) {
        if (response.source && response.source.context) {
            response.source.context.title = "Hapi-Plugins";
        }
    }
    return reply();
})
```

上面的示例使用了 `onPreResponse`，我们在第 2 章“服务器，请求生命周期”中学习过。我们使用 `server.ext` 来扩展此功能，因此在响应给出之前，我们添加了这个 `title` 上下文。

另一种方法是将一个共享对象合并到视图上下文中：

```javascript
// 在 server.js 内部
server.ext('onRequest', function (request, next) {
    // 这可以从数据库异步加载（并缓存）
    request._sharedContext = {
        title: 'Hapi-Plugins'
    };
    next();
});
```

这里我们使用了请求生命周期中的 `onRequest` 部分。与之前的示例一样，我们通过使用 `server.ext` 函数来扩展请求生命周期的这一部分。下面我们使用一个处理程序在通过模板回复之前合并 `sharedContext`。

```javascript
// 在 handler 内部
var Hoek = require('hoek');
/* ... */
handler: function (request, reply) {
    var ctx = {
        content: 'Hello world!'
    };
    var context = Hoek.applyToDefaults(request._sharedContext, ctx);
    return reply.view('/path/' + 'templateName', context);
}
```

通过像上面这样使用共享上下文，可以将模板和视图之间共享的通用值分组并放置在单个位置（而不是在每个处理程序和视图中重复定义）。如果你需要重复传递服务器范围的设置（如特性开关、网站信息或翻译），这将非常有帮助。

## 总结

现在你已经知道了如何在给定数据上下文的情况下向最终用户渲染 HTML，你现在可以使用 hapi 创建完整且功能齐全的网站。视图和模板系统可以通过提取共享上下文数据、共享局部模板和完整模板，为你节省大量的开发时间并让你的工作变得更加轻松。

利用目前所学的知识，你现在可以使用 hapi 创建功能完整的网站。但是，正如你在第 10 章“测试”中将看到的，仅仅能够创建网站是不够的。我们将向你展示如何测试你的应用程序。

## 测试 (Testing)

在上一章（第 9 章 模板化）中，我们发现了如何使用 HTML 响应请求。有了这最后一块拼图，你可以创建自己的完整且功能齐全的 Web 应用程序。然而，这还不够！要构建真实的、生产级别的应用程序，你需要测试你的代码。

在 hapi 的生态系统中，测试极其重要。测试对于 hapi 模块维护者来说如此重要，以至于他们开发了自己的测试库，名为 `lab`，以确保测试正确。在拉取请求（pull request）被合并到核心模块之前，必须首先拥有可运行的测试以及模块代码 100% 的测试覆盖率。因此，如果你计划回馈社区，了解 hapi 测试是如何编写和执行的至关重要。

## 本章概览

接下来的章节将涵盖许多基本的测试原则以及下面列出的主题：

- lab 的历史
- 安装 lab
- 编写简单的测试
- lab 的原理
- 编写 hapi 测试
- 代码覆盖率
- 报告器 (Reporters)
- 代码校验 (Linting)
- 插件测试

## lab 的历史

为了获得最佳效果，hapi 与 `lab` 测试运行器配合得很好。Lab 是专为 hapi 和 hapi 插件开发而设计的测试框架。hapi 最初使用 mocha 和 chai 来执行测试。然而，当 Node.js 0.10 发布时，hapi 增加了对新版本的支持并引入了 domains。自发布以来，domains 一直是一个棘手的特性，测试支持也不例外。当 0.10 发布时，mocha 在采用足够支持测试 domains 的方案方面较为缓慢。由于 hapi 希望使用 domains，必须采取行动。因此，lab 应运而生。最初，lab 是 mocha 的一个分叉（fork）。剔除了 hapi 不需要的功能，并增加了更多新功能。

代码覆盖率是确保提交到仓库的代码具有高质量的关键因素。因此，代码覆盖率支持需要作为简单的标志内置在测试框架中，以便在运行测试时使用。

在 lab 创建之前，hapi 中的 mocha 测试是通过 `blanket` 代码覆盖率模块运行的。Blanket 本身依赖于 esprima 来创建代码的抽象语法树 (AST)，以帮助识别需要插入语句来进行代码覆盖率分析。在创建 lab 时，Blanket 被沿用到了 lab 中。然而，随着时间的推移，代码覆盖率支持被直接内置到 lab 中，而不再通过第三方提供。

随着分析被整合进 lab，代码覆盖率报告也随之演进。这使得代码覆盖率成为了 lab 报告中的一等公民。因此，HTML 报告器现在可以向开发者指出代码中测试永远无法触及的行。

这使得识别死代码（dead code）并将其删除变得非常容易，从而使你的代码更具可维护性。

当 hapi 使用 mocha 进行测试时，它还使用 chai 来帮助构建断言。hapi 维护者倾向于使用 `expect` 风格编写测试，而不是 `should` 或 `assert`。然而，随着时间的推移，chai 的使用暴露出几个与大框架不一致的边缘情况函数名。例如，`exist` 属性不像其他一些语法部分那样作为函数执行。这些不一致导致时不时出现一些 bug。这些 bug 与一个事实有关：人们太容易忘记写方法 `()`，从而导致断言从未被执行。因为从未执行，它因此被错误地判定为通过。

因此，一个名为 `code` 的测试断言库被创建了。Code 采用了 chai 的语法，但将 `exist` 变成了一个函数，就像所有针对 `true`、`false` 和 `null` 的真值检查都变成了函数一样。下面你可以看到 chai 和 code 之间的区别。

首先是我们的 chai 示例：

```javascript
expect(foo).to.exist;
expect(bar).to.be.true;
```



接下来你可以看到我们用于实现同样功能的 `code` 示例。注意，true 和 exist 是 `code` 中的函数。

```
expect(foo).to.exist();
expect(bar).to.be.true();
```

除了前面提到的不一致性之外，我们想要一个体积小、简单且直观的断言库。我们剔除了处理插件、扩展以及支持浏览器测试所带来的开销相关的逻辑。这带来了许多我们所需的功能，但只用了大约 300 行代码，简单易懂，便于阅读和理解。

最后，`code` 实现了测试运行器与断言库之间更深度的集成。这使我们能够获得断言总数的统计，以衡量测试的覆盖范围，并验证每个创建的断言确实都被执行了。

Lab 在其他方面也有所发展。例如，增加了转译器支持，以便对 CoffeeScript 或 JSX 代码进行测试。此外，lab 现在内置了代码检查（linting）支持，因此向 hapi 仓库提交的拉取请求都遵循相同的代码风格。这对于开发人员来说非常有用，可以在请求合并提交之前就知道自己是否违反了任何风格指南规则。然而，lab 目前的一个缺点是它仅在服务器端设计和运行。不过，随着其流行度的增长以及越来越多的开发人员希望将其用于客户端测试，这种情况很可能会改变。

## 安装 lab

在你的环境中全局安装 lab 可能会很有用。与其他 node.js 模块类似，lab 的安装可以通过使用 npm 来完成。如下所示。

```
$ npm install -g lab
```

虽然你可以全局安装 lab，但通常不需要这样做。相反，所有 hapi 核心模块都将 `lab` 包含在 `package.json` 的 `devDependencies` 部分中。任何近期版本的 `lab` 都可以同时全局和本地安装，因为两者在运行测试时不会冲突。下一个示例展示了如何仅在本地安装 `lab` 并将其保存到 `package.json` 的 `devDependencies` 部分。

```
$ npm install lab --save-dev
```

安装 `lab` 后，你应该验证它是否正常工作。如果全局安装，`lab` 将在 PATH 环境变量中可用。否则，你需要从 `node_modules/.bin` 文件夹运行 `lab` 二进制文件。要验证全局安装的 lab，只需运行 `lab -h`。如果要验证本地安装，则需要运行 `node ./node_modules/.bin/lab -h`。你应该会看到 lab 的帮助页面。

顺便一提，当导航到包含子级 `node_modules/.bin` 文件夹的目录时，自动更新你的 PATH 可能会很有帮助。这将使本地二进制文件可以像全局二进制文件一样运行。

## 安装 code

与安装 `lab` 的方式类似，你也应该安装 `code`。记住，`lab` 没有内置的、开箱即用的断言库。因此，你应该使用 `code`、`chai` 或你喜欢的其他任何断言模块。同样，你可以运行 `npm install code --save-dev` 将其保存到你的 `package.json` 文件中，或者手动添加。

## 编写简单测试

所有测试应该位于项目根目录下的 `test` 文件夹中。这是 Node.js 社区中几乎无处不在的一种模式。如何选择测试文件的命名方式由你自己决定，因为并没有一个既定的、通用的命名约定。然而，*hapi* 组织旗下各模块中使用的一种模式是：将每个测试文件命名为其负责测试的对应模块的同名文件。为了本次练习的目的，在 `test` 目录下创建一个名为 `index.js` 的文件。用下面给出的代码填充 `index.js`。

```
// Load modules

var Code = require('code');
var Lab = require('lab');


var lab = exports.lab = Lab.script();

lab.test('lab exists', function (done) {

    Code.expect(lab).to.exist();
    done();
});
```

只需在项目的根目录下输入命令 `lab` 即可运行上述测试。输出将如下所示：

```
$ lab

1 tests complete
Test duration: 5 ms
No global variable leaks detected
```

希望这并不困难或令人吃惊。正如你从输出中看到的，运行测试所需的时间会被报告出来，同时还有一个用于点符号（dot notations）的默认报告器。

## lab 的原则

让我们来看看使用 lab 时需要牢记的核心原则。

### 始终异步

在上一节中，你看到的是一个简单的 lab 测试的样子。lab 的一个定义性特征是，测试始终被假定为异步的。不同于检查 arguments 对象的长度并对带有 done 参数的测试采用不同的运行方式，所有 lab 测试都必须接收一个回调参数，并在测试完成时执行它。如果测试没有接收到预期的参数，那么测试将立即失败并给出解释。例如下面这个测试：

```
// Load modules

var Code = require('code');
var lab = require('lab');

var lab = exports.lab = Lab.script();

lab.test('lab exists', function () {

    Code.expect(lab).to.exist();
});
```

当我们运行 lab 时，会得到以下输出：

```
$ lab

Error: Function for test "lab exists" should take exactly one argument
```

类似地，如果在测试函数中接受了一个参数但没有执行它，也会发生错误。不过，这次的错误将是测试本身的超时。我们可以通过移除 done() 来使其超时。可以通过编写以下测试来实现。

## 第 10 章：测试

```
// Load modules

var Code = require('code');
var Lab = require('lab');

var lab = exports.lab = Lab.script();

lab.test('lab exists', function (done) {

    Code.expect(lab).to.exist();
});
```

这个测试的结果输出将如下所示：

```
$ lab

  x

Failed tests:

  1)  lab exists:

      Timed out (2000ms) -  lab exists


 1 of 1 tests failed
Test duration: 2007 ms
No global variable leaks detected
```

注意，在前面的示例中，`.` 被改成了 `x` 以表示测试失败。如果你想让报告更加明确，可以使用 `-v` 启用详细模式（verbose mode）。下面是启用详细模式后同一测试的示例。

```
$ lab -v
1) lab exists


Failed tests:

  1)  lab exists:

      Timed out (2000ms) -  lab exists


 1 of 1 tests failed
Test duration: 2006 ms
No global variable leaks detected
```

### 测试脚本

Lab 也不会假定 `test` 文件夹中的 JavaScript 文件一定是测试。因此，为了告诉 `lab` 某个脚本文件是测试脚本，你必须执行 `Lab.script()` 并将结果赋值给 `module.exports` 对象的 `lab` 属性。为了帮助开发者发现这种风格中的错误，`lab` 会报告任何执行了 `script()` 但未导出 `lab` 属性的实例。下面展示了这种代码的示例：

```
// Load modules

var Code = require('code');
var Lab = require('lab');

var lab = Lab.script();

lab.test('lab exists', function (done) {

    Code.expect(lab).to.exist();
    done();
});
```

对于这个测试，如果你运行 lab，这个错误的提示信息将如下所示：

```
$ lab
The file: test/index.js includes a lab script that is not
exported via exports.lab
```

### 安全的全局变量

`lab` 的另一个假设是，全局对象不应该被测试功能污染。虽然其他框架会将 `describe` 或 `it` 附加到全局对象上，但 `lab` 尝试了一种不同的方法，即试图隔离每个 `experiment`。每个 `experiment` 或 `test` 函数仅在执行 `script()` 返回的 `lab` 对象上可用。

Lab 更进一步处理全局变量问题，它会在运行测试后检查 `global` 对象中是否存在任何新的属性。这通常是一个警示信号，说明声明变量时遗漏了 `var`。然而，可以通过向 `lab` 二进制文件传递 `-l` 或 `--leaks` 参数来禁用此功能。类似地，如果存在一个已知的、应该存在的全局变量，你可以将其作为参数传递给 `-I` 或 `--ignore`。例如，如果你想忽略全局对象上一个名为 `foo` 的属性，你可以如下执行 `lab`：

```
$ lab --ignore foo
```



## 实验

尽管 `lab` 测试可以配置成类似 `mocha` 和 `jasmine` 行为驱动开发（BDD）风格的测试，但它们也可以被命名为完全不同的名称。BDD 风格倾向于使用 `describe` 和 `it`，而 `lab` 也提供了使用 `experiment` 和 `test` 的选项。`describe` 和 `experiment` 函数可以互换使用，同样 `it` 和 `test` 也可以互换。你选择哪种风格完全取决于自己，没有错误的答案。不过，使用 `experiments` 风格的一个优点是，它确实强化了这样一个概念：工程师正在创建测试，并且正以某种方式尝试使其具有科学性。

实验适用于将一组类似的测试分组在一起。例如，如果你正在测试 `lab` 本身，你可能会编写如下所示包裹在实验中的实验测试。

```javascript
// Load modules

var Code = require('code');
var Lab = require('lab');

var lab = exports.lab = Lab.script();

lab.experiment('lab', function () {

    lab.test('exists', function (done) {

        Code.expect(lab).to.exist();
        done();
    });

    lab.test('has properties', function (done) {

        Code.expect(Object.keys(lab)).to.not.have.length(0);
        done();
    });
});
```

然后，如果你在详细模式下运行这些测试，你将得到以下输出：

```
$ lab -v
lab
1) exists (3 ms)
2) has properties (1 ms)

2 tests complete
Test duration: 6 ms
No global variable leaks detected
```

你可以看到，在详细模式下，你还可以看到每个测试花费了多长时间。

## 编写 hapi 测试

hapi 在设计时就考虑了测试。为了发布一个版本，每一行代码和每一个代码路径都必须有对应的测试。因此，hapi 及其依赖项中有相当多的测试。为了帮助加快测试运行时间，并避免文件描述符限制问题，hapi 内置了模拟请求支持。这通过名为 `inject` 的函数提供，该函数来自 `shot` 模块。为了说明 `shot` 的强大功能，请看下面的测试。还要注意，这里没有使用实验风格的测试，而是使用了 BDD 风格的测试快捷方式编写测试。

```javascript
// Load modules

var Code = require('code');
var Hapi = require('hapi');
var Lab = require('lab');


var lab = exports.lab = Lab.script();
var describe = lab.describe;
var it = lab.it;
var expect = Code.expect;

describe('inject()', function () {

    it('returns the response result', function (done) {

        var handler = function (request, reply) {

            return reply('hello');
        };

        var server = new Hapi.Server();
        server.connection();
        server.route({
            method: 'GET',
            path: '/',
            config: { handler: handler }
        });

        server.inject('/', function (res) {
            expect(res.statusCode).to.equal(200);
            expect(res.result).to.equal('hello');
            done();
        });
    });
});
```

在前面的示例中，`server.start` 函数没有被执行。因此，没有创建套接字，服务器也没有连接套接字。然而，向服务器发出了一个请求并收到了响应。请求对象包含了 hapi 服务器关心的所有属性。同样，传递给 `inject` 回调的响应对象包含了响应主体以及相关的头部和状态码信息。

除非你创建的测试需要来自套接字的信息，否则最好的解决方案通常是使用 `inject`。如果你采用这种方法，你的测试执行速度应该比依赖真实套接字快得多。此外，它也使得避免与套接字相关的设置和拆卸工作变得容易得多。说到这个，如果你需要使用套接字，请将 `0` 作为 `port` 传递给 `connection` 函数，以确保端口可用。下面的代码说明了这一点。请注意，在服务器启动后，最终使用的端口可以从 `server.info.port` 属性中检索到。

```javascript
// Load modules

var Code = require('code');
var Hapi = require('hapi');
var Lab = require('lab');
var Wreck = require('wreck');

var lab = exports.lab = Lab.script();
var describe = lab.describe;
var it = lab.it;
var expect = Code.expect;

describe('real request', function () {

    it('returns a real response', function (done) {

        var handler = function (request, reply) {

            return reply('hello');
        };

        var server = new Hapi.Server();
        server.connection({ port: 0 });
        server.route({
            method: 'GET',
            path: '/',
            config: { handler: handler } 
        });

        server.start(function () {

            Wreck.get('http://localhost:' +
                    server.info.port,
                    function (err, res, payload) {

                    expect(res.statusCode).to.equal(200);
                    expect(payload).to.equal('hello');
                    server.stop(done);
                });
        });
    });
});
```

Wreck 是一个轻量级的 HTTP/HTTPS 客户端请求包装器，专为 hapi 设计。在进行任何请求时，这是首选模块。也就是说，`request` 模块也完全支持。在本地环境中，`inject` 示例和 `wreck` 示例之间的测试时间差异大约是 18 毫秒。虽然 18 毫秒本身不算多，但你创建的所有测试加起来会很快累积。

## 代码覆盖率

除了所有之前融入 `lab` 的功能外，代码覆盖率是其最强大的功能之一。*lab* 中的代码覆盖率依赖于 *espree* 模块来生成抽象语法树（AST）。除了典型的逐行覆盖外，*lab* 还会确定测试是否执行了不同的代码分支。这可以是从同一个 `if` 语句中的多个条件到标准的三元语句等任何情况。此外，*lab* 还会确定是否有一段代码路径无法被执行，因此可以将其删除。

在显示代码覆盖率方面，`html` 和 `console` 报告程序是测试最充分的。默认情况下，运行 `lab` 时代码覆盖率未启用。要启用它，你需要传递 `-c` 或 `--coverage` 标志。覆盖率标志将启用代码覆盖率报告，并期望测试覆盖 100% 的代码。如果你期望低于 100% 的代码覆盖率，你可以使用 `-t` 或 `--threshold` 标志，后跟一个数字，该数字代表在报错之前应覆盖的代码百分比。如果测试未能达到阈值，`lab` 将以错误代码退出。

下面是一个控制台报告程序的输出示例，显示了测试覆盖率未通过时的样子。

```
$ lab -c
66 tests complete
Test duration: 1492 ms
No global variable leaks detected
Coverage: 99.44% (2/356)
lib/payload.js missing coverage on line(s): 17, 27
```

如果这还不够详细，你需要更好地了解缺失的覆盖率情况，那么建议使用 `html` 报告程序。要使用不同的报告程序，只需将报告程序的名称传递给 `-r` 或 `--reporter` 标志。你可以在下面看到运行 `lab -c -r html > coverage.html` 的输出截图。

```javascript
12 
13 1 module.exports = internals.Payload = function (payload, encoding) {

14 
15 4 Stream.Readable.call(this);

16 
17 4 var data = [].concat(payload || '');
18 4 var size = 0;
19 4 for (var i = 0, il = data.length; i < il; ++i) {
20 5 var chunk = data[i];
21 5 size += chunk.length;
22 5 data[i] = Buffer.isBuffer(chunk) ? chunk : new Buffer(chunk);
23 4 }

24 
25 4 this._data = Buffer.concat(data, size);
26 4 this._position = 0;
27 4 this._encoding = encoding || 'utf8';
28 };
29
```

如你所见，覆盖率仅在第 17 行和第 27 行的某些特定变量上缺失。然而，如果你为那些行上缺失的变量添加测试，你可以在下一个示例中看到运行 `console` 报告程序的结果。

```
$ lab -c
69 tests complete
Test duration: 1494 ms
No global variable leaks detected
Coverage: 100.00%
```

在 hapi 生态系统中开发模块时，使用覆盖率是必须的。所有在 hapijs 组织下发布的模块都要求 100% 的代码覆盖率。因此，如果你计划为这些模块贡献任何更改或增强功能，你必须为更改的代码添加测试。当涉及到覆盖率时，可能会有反对者，但它是被选定用来帮助评估代码是否有效的机制。除了添加覆盖模块中每一行和代码路径的测试外，hapijs 维护者还会审查测试和代码，以帮助确保其准确性。一个人可以通过测试检查错误的假设来覆盖一行代码，但工程师最终有责任检查代码和测试本身。

## 报告程序

Lab 内置了众多报告程序，并支持任何自定义报告程序。这些报告程序多年来随着社区的反馈而不断演进。目前，`lab` 支持以下报告程序：

- console - 命令行界面输出
- html - 生成 HTML 流报告，可重定向到文件
- json - JSON 格式的报告
- junit - JUnit XML 格式
- tap - TAP 格式
- lcov - lcov 格式
- clover - clover XML 格式
- custom - 自定义报告程序

之前，在代码覆盖率部分，`console` 和 `html` 报告程序在报告覆盖率方面已经演示过。然而，`html` 报告程序功能不止于此，它还会报告运行的测试以及每个测试花费的时间。这里展示了一个关于单个测试的 `html` 报告程序示例：



 第十章：测试

## 测试报告

0 失败 0 跳过 66 项测试 (1450 毫秒)

显示成功 显示失败 request() read() parseCacheControl() 快捷方式 json 事件

| ID | 标题 | 持续时间 (ms) |
|---|---|---|
| 1 | request() 使用回调请求资源 | 21 |
| 2 | request() 请求 POST 资源 | 6 |
| 3 | request() 请求负载中包含 Unicode 字符的 POST 资源 | 5 |
| 4 | request() 请求带有请求头的 POST 资源 | 3 |
| 5 | request() 请求流式负载的 POST 资源 | 5 |
| 6 | request() 不带回调请求资源 | 2 |
| 7 | request() 无法同时设置 agent 和 rejectUnauthorized | 1 |
| 8 | request() 无法同时设置 false agent 和 rejectUnauthorized | 0 |
| 9 | request() 可以同时设置 null agent 和 rejectUnauthorized | 12 |
| 10 | request() 请求 https 资源 | 345 |
| 11 | request() 请求设置了安全协议的 https 资源 | 297 |
| 12 | request() 在 https 资源证书无效且使用默认 rejectUnauthorized 时失败 | 11 |
| 13 | request() 在 https 资源证书未授权且 rejectUnauthorized 为 false 时成功 | 7 |
| 14 | request() 请求具有下游依赖的资源 | 6 |
| 15 | request() 默认不跟随重定向 | 3 |
| 16 | request() 处理重定向 | 4 |
| 17 | request() 处理相对位置的重定向 | 5 |
| 18 | request() 达到最大重定向次数 | 3 |

如果你计划在 Jenkins 中使用 lab，那么 junit 报告器可能是一个不错的选择，因为许多 Jenkins 插件（如 dashboard-view）依赖这种格式。你也可以将 HTML 报告器与 HTML 发布者插件结合使用，以获得测试和代码覆盖率的详细视图。json 报告器是一个不错的原生报告器，如果你需要查看原始数据并进行自己的解析，可以很容易地对其进行解析。它报告代码覆盖率以及一般的测试失败情况。下面展示了使用 `-c` 标志启用代码覆盖率时，json 报告器输出的示例。

```
"17": {
  "source": " var data = [].concat(payload || '');",
  "chunks": [
    {
      "source": " var data = [].concat("
    },
    {
      "source": "payload",
      "miss": "true"
    },
    {
      "source": " || "
    },
    {
      "source": "''",
      "miss": "true"
    },
    {
      ")"
    }
  ]
}
```

134

```
{
  "source": "'''",
  "miss": "never"
},
{
  "source": ");"
}
],
"hits": 4,
"miss": true
}
```

如上面的示例所示，未覆盖部分会报告在行级别和各个代码分支上（如果存在分支的话）。这使得读取 JSON 输出的工具能够更轻松地解析并表示未覆盖的代码。此外，你可以看到命中此行但最终错过该代码分支的执行次数。每个行号都表示为父对象中的键名。每个 JSON 条目以覆盖率检查所针对的代码文件信息开头，如下所示：

```
{
  "filename": "lib/payload.js",
  "percent": 92.5925925925926,
  "hits": 25,
  "misses": 2,
  "sloc": 27,
  "source": {
    "1": {
      "source": "",
      "miss": false
    }
  }
}
```

此外，与 'html' 报告器一样，JSON 报告器还包含有关已执行单个测试的信息。会显示每个测试名称以及执行持续时间，最重要的是，测试是否通过。JSON 输出的这部分如下所示。

```
{
  "tests": {
    "request()": [
      {
        "title": "requests a resource with callback",
        "err": false,
        "duration": 23
      },
      {
        "title": "requests a POST resource",
        "err": false,
        "duration": 5
```

## 代码检查

`lab` 包含的强大功能之一是内置的代码检查支持。开箱即用，支持 eslint 和 jshint 这两种代码检查工具。默认的代码检查规则强制执行类似 hapi 风格指南的样式。包含代码检查工具的最初目的是确保对 hapi 项目的拉取请求遵循相同的样式。但是，代码检查规则可以更改以适应项目的需求。需要使用 `--lint-options` 参数设置传递给代码检查工具的任何选项。如果你想使用默认代码检查工具 eslint 运行默认代码检查规则，那么可以向 `lab` 传递 `-L` 或 `--lint`。若要更改使用的代码检查工具，可以向 `lab` 传递 `-n` 或 `--linter`。下面演示了如何使用 jshint 运行 `lab`。

```
$ lab -n jshint
```

## 插件测试

在使用 hapi 构建插件和服务器时，你需要做的一件事是测试插件是否可以注册以及服务器是否可以启动。对于 hapi-plugins.com 网站，我们使用 `lab` 来编写测试。

在 hapi 生态系统的插件中普遍存在的一项常见测试是检查插件是否可以在 hapi 本身中注册。下面的测试检查 hapi-plugins.com 插件是否可以在 hapi 内注册以及服务器是否可以启动：

```
// Load modules

var Code = require('code');
var Lab = require('lab');
var HapiPlugins = require('../');


// Test shortcuts

var lab = exports.lab = Lab.script();
var describe = lab.describe;
var it = lab.it;
var expect = Code.expect;

describe('hapi plugins', function () {

    it('Server can be started', function (done) {
```

```
HapiPlugins.init(function (err, server) {

    expect(err).to.not.exist();
    expect(server).to.exist();
    done();
});
});
});
```

在 hapi-plugins.com 中，我们使用数据库。因此，我们需要验证数据库是否实际工作。由于我们尝试测试所有内容，集成测试以及使用模拟对象的测试都很有用。常见的测试可能是测试是否可以创建与数据库的连接并将数据保存到数据库。下面演示了一个完整的测试，该测试执行与数据库的往返操作。请注意，测试使用 inject 函数调用服务器路由以检索刚刚保存的插件。此示例是你可以在自己的代码中重复使用的优秀模式参考。

```
// Load modules

var Code = require('code');
var Lab = require('lab');
var HapiPlugins = require('../');

// Test shortcuts

var lab = exports.lab = Lab.script();
var describe = lab.describe;
var it = lab.it;
var expect = Code.expect;

describe('hapi plugins', function () {

    it('can like a plugin', function (done) {

        var resetDb = function (callback) {

            DB.plugin.remove(function (err) {

                if (err) {
                    return callback(err);
                }

                DB.user.remove(callback);
            });
        };
```

## 总结

在本章中，我们介绍了测试对于 hapi 生态系统的核心重要性。如果没有测试以及围绕 hapi 测试框架 *lab* 构建的工具，确保交付高质量代码将会困难得多。当你向任何核心 hapi 模块贡献代码时，你需要熟悉如何创建测试并确保任何新代码 100% 被测试覆盖。此外，在为任何 hapi 核心模块编写代码时，使用 *lab* 来帮助确保遵循 hapi 风格指南。

hapi 中的测试及其周边工具总是有改进的空间。如果你正在寻找一个加入 hapi 生态系统贡献的好的起点，请考虑



## 总结

本文探讨如何为模块编写测试。即使各模块已达到100%代码覆盖率，在许多情况下，进一步的测试仍具有价值。

在下一章中，我们将向您展示用于调试hapi系统并识别主要问题的一些强大方法。

# 调试 11

> 一个经过调试的程序，是你尚未发现其失败条件的程序。
>
> -- 杰里·奥格丁

在上一章中，我们学习了大量关于如何测试hapi应用程序以及如何编写单元测试的知识。在本章中，我们将探索如何使用一些高级工具来调试我们的hapi应用程序。

在Node.js中进行调试一直是许多开发者的痛点。目前仍缺乏优秀的工具来帮助开发者在跨平台和应用程序整个生命周期中调试Node.js。虽然像DTrace这样的工具确实存在，但并非所有Node.js部署环境都有机会使用它。Joyent等公司在这方面做了大量工作，记录了如何调试Node.js应用程序。在hapi世界中，我们创建了一些模块来帮助使调试hapi应用程序变得更加容易。本章将介绍特定的hapi模块，这些模块可以帮助在不同环境中调试hapi服务器。此外，本章还涵盖如何设置有助于诊断问题的报告。

## 章节概览

以下章节将涵盖有关调试hapi和Node.js的许多细节。这些主题包括：

- console.log
- 调试模式
- TV
- Good
- REPL
- 堆快照
- 核心文件

# console.log

尽管许多开发者可能看不上`console.log`作为一种可行的调试选项，但它有其用途，并且可能非常有用。在很多情况下，您只是需要知道在远程部署中某个特定点变量的值。对于像REPL或远程调试会话可能有些小题大做的情况，不要轻视使用`console.log`。考虑到Node.js的脚本特性和进程启动的便捷性，简单地通过ssh登录服务器并添加一条日志语句是可行的。虽然不是最优雅的方式，但它可以帮助识别应用程序在不同点的状态。

# 调试模式

幸运的是，hapi中也有调试模式的概念。您无需手动在hapi中输入大量`console.log`语句，而是可以以调试模式启动服务器，并通过控制台访问不同的服务器事件和错误详情。由于此模式可能输出冗长且不适用于生产环境，因此建议您仅在开发时启用调试模式。下面是一个以调试模式启动服务器并将所有错误记录到控制台的示例。

```
var Hapi = require('hapi');

var options = {
    debug: {
        log: ['error']
    }
};

var server = new Hapi.Server(options);
server.connection({ port: 8000 });

server.route({ method: 'GET', path: '/', handler: function (request, reply) {

    throw new Error('Tribbles');
}});

server.start(function () {

    console.log('server started');
});

Debug: internal, implementation, error
    Error: Uncaught error: Tribbles
```

正如您在前面的示例中所看到的，当发生错误时，错误信息和堆栈跟踪会以`Debug:`为前缀记录到控制台。

# TV

另一个用于在开发过程中调试hapi服务器的有用选项是使用`tv`模块。TV主要为前端开发者和hapi应用程序的消费者设计。其目标是提供一个易于使用的仪表板，显示有关服务器请求活动的信息。这对于前端开发者跟踪其代码向hapi服务器发起的请求的整个生命周期特别有用。下面是`tv`的截图：

![](img/79450811086e2fc8749ec4d309ea2b79_142_0.png)

要将`tv`添加到服务器，您可以像注册任何其他hapi插件一样注册它。下面展示了如何使用默认设置注册`tv`。在服务器上注册`tv`后，您可以通过服务器URL + `/debug/console`来访问它。

```
var Hapi = require('hapi');
var Tv = require('tv');

var server = new Hapi.Server();
server.connection();

server.register(Tv, function (err) {

    if (!err) {
        server.start();
    }
});
```

使用`tv`，您可以通过选择不同的事件标签来订阅您关心的请求事件。请求详情会在进行时实时发送到`tv`页面。如果某些请求显得特别有用，您还可以将其标记并进行调查。

# Good

在*tv*中记录请求详情对于本地开发非常有用。但是，当您处于QA或生产环境时，您将需要使用专为该场景设计的模块。对于这些情况，以及对于本地开发，*good*插件都非常有用。

使*good*特别适合QA和生产环境的原因是，它还被设计为记录操作数据。多年来，它已经扩展到不仅包括典型的内存或CPU详情，还包括事件循环延迟和网络活动。

要将*good*添加到hapi服务器，您可以像注册任何其他插件一样注册它。主要区别在于，对于*good*，您需要指定关心的事件类型以及记录这些事件的位置的选项。*good*事件包括以下几种：

- ops
- response
- log
- error
- request
- wreck

可以存储事件数据的范围非常广泛。如果您需要不同的报告器，可以参考众多示例之一来构建一个。目前，*good*可用的报告器类型包括：

- UDP
- HTTP
- 文件
- 控制台
- InfluxDB
- Winston
- Loggly
- Logstash

这个列表还将继续增长。您可以通过查看**good**页面来获取最新的列表。下面的代码展示了如何注册*good*并将所有`ops`数据每秒记录到`/var/log/example/ops.json`文件中。

```
var Hapi = require('hapi');
var Good = require('good');

var server = new Hapi.Server();
server.connection();

var options = {
    opsInterval: 1000,
    reporters: [{
        reporter: 'good-file',
        events: { ops: '*' },
        config: '/var/log/example/ops.json'
    }]
};

server.register({
    register: Good,
    options: options
}, function (err) {

    if (err) {
        console.error(err);
        return;
    }

    server.start();
});
```

当您查看ops日志文件时，会注意到每个条目都是JSON可解析的，并且每个条目之间由换行符分隔。下面是事件数据的一个示例。

```
{
    "event": "ops",
    "timestamp": 1527940993174,
    "host": "mac.local",
    "pid": 35503,
    "os": {
        "load": [2.13427734375,2.44287109375,
            2.4873046875],
        "mem": {
            "total": 17179869184,
            "free": 5757075456},
        "uptime":459461
    },
    "proc": {
        "uptime": 4,
        "mem":{
            "rss": 46538752,
            "heapTotal": 32171264,
            "heapUsed": 17638880
        },
        "delay": 0.2207310050725937},
    "load": {
        "requests": {},
        "concurrents": {"62778": 0},
        "responseTimes": {},
        "sockets": {
            "http": {
                "total":0
            },
            "https": {
                "total":0
            }
        }
    }
}
```

在前面的示例中，您可以看到记录了大量有用的信息。它使得将异常高的内存使用量与网络活动或事件循环缓慢关联起来成为可能。

在good版本6及更高版本中，支持记录使用wreck发起的请求数据。这对于跟踪可能存在于hapi服务器和下游服务器之间的问题非常有用。hapi反向代理模块依赖于wreck，因此，可以使用good记录反向代理数据。

使用wreck支持时的输出示例可能如下所示：

```
{"event":"wreck","timestamp":1431469615889,"timeSpent":581,"request":{"method":"GET","path":"/api/route","url":"http://localhost:8081/api/route","protocol":"http:","host":"localhost","headers":{"host":"localhost:8081"}},"response":{"statusCode":200,"statusMessage":"OK","headers":{"content-type":"application/json; charset=utf-8","cache-control":"no-cache","content-length":"4198","accept-ranges":"bytes","date":"Tue, 12 May 2015 22:26:55 GMT","connection":"close"}}}
```

您可以看到这里有一些很棒的信息。例如，您可以绘制timeSpent图表，并找出在调用中您花费了多少时间使用依赖服务。查看您的headers以确保它们被正确发送也非常有用。

good收集和报告的数据提供了强大的能力。业务人员以及运维人员应该会发现这些信息很有用。将数据发送到像splunk或logstash这样的日志聚合器，然后为您的应用程序的不同利益相关者创建仪表板，是利用可用数据的好方法。这对于您的hapi应用程序来说，可能是一个强大且易于实现的成果。

以hapi-plugins.com项目为例，good被用于将操作和hapi日志事件记录到控制台。这是在lib目录下的index.js文件中完成的。



通过将 *good* 与 good-console reporter 一起注册，可以实现良好的文件夹管理。以下是该注册方式的一个示例。

```
var goodOptions = {
    opsInterval: 5000,
    reporters: [{
        reporter: 'good-console',
        events: { log: '*', ops: '*' }
    }]
};

var registerHttpPlugins = function (next) {
    server.register([
        Bell,
        Blipp,
        HapiAuthCookie,
        Authentication,
        Controllers,
        Models,
        Routes,
        { register: require('good'), options: goodOptions }
    ],
    { select: 'http' },
    function (err) {

        return next(err);
    });
};
```

*good-console* reporter 将发送到控制台的事件由 `events` 属性指示。`*` 值表示 reporter 不会根据特定标签过滤任何事件。如果你只关心与某个特定标签相关的事件，可以通过将 `*` 替换为与该标签同名的单个字符串，或者代表你关心的事件标签的字符串数组来指定。

在启动服务器并查看 `stdio` 的输出后，可以观察到 *good* 的报告。下面显示了服务器运行 10 秒后 `ops` 事件的一个示例输出。如你所见，内存消耗、运行时间（uptime）和负载值（load）都可以被报告。

```
150418/175554.526, [ops], memory: 64Mb, uptime (seconds): 5, load: 1.646484375,2.1015625,1.76806640625
150418/175559.531, [ops], memory: 65Mb, uptime (seconds): 10, load: 1.67431640625,2.099609375,1.76904296875
```

## REPL

为了更方便地调试远程服务器上运行的应用程序，人们创建了 `hapi` 插件 `reptile`。

该插件创建了一个 REPL，它监听一个端口以接收 TCP 连接，从而可以访问运行中的 `hapi` 服务器对象。REPL 即“读取-执行-打印循环”（read execute print loop），是修改运行中的服务器或简单检查其运行情况的绝佳方式。默认情况下，REPL 仅可从 `localhost` 访问。这是出于设计考虑，以防止任何人访问 REPL，因为这有可能给应用程序带来问题。

在端口上可访问的 REPL 与你在不带任何参数输入 `node` 时获得的 REPL 相同。两者都使用了 node 核心随附的 `repl` 模块。唯一的区别是 `server` 被添加到了全局上下文中。

为了创建到 REPL 端口的连接，你可以使用 netcat 或 telnet。当你运行 `reptile` 内部 `/example` 文件夹中的服务器时，它将创建一个虚拟服务器并注册 `reptile` 插件。示例服务器监听 9000 端口。下面是如何使用 netcat 连接到本地 9000 端口的操作。

```
$ nc localhost 9000
>
```

连接建立后，你应该能看到全局对象上有哪些可用对象。为此，只需输入 `global` 并按下回车键。从此时起，你可以遍历现有对象或为事件创建处理程序。这应该能为运行中的服务器提供一个很好的切入点，可用于调试目的。

## 堆快照 (Heap Snapshots)

最难调试的问题之一是那些导致进程崩溃的问题。调试这些问题的常用方法是简单地查看异常发生时的堆栈输出。v8 世界中的另一个有用工具是在异常发生瞬间创建堆快照并稍后对其进行分析。为了同时解决这两个用途，创建了 `poop` 模块。`poop` 模块是一个 hapi 插件，它监听进程的 `uncaughtException` 事件。当发生未捕获的异常时，会创建一个堆快照文件，并将异常详情记录到文件中。`Poop` 还会重新抛出该异常，以便异常能够传播并由其他事件订阅者处理。

堆快照文件以 `.heapsnapshot` 扩展名结尾。这些文件可以使用 Chrome v8 web inspector 打开。要打开文件，请启动 web inspector 并选择 “Profiles” 标签页，然后点击 “Load” 按钮打开快照文件。此处的截图显示了 inspector 中该标签页的样子。

![](img/79450811086e2fc8749ec4d309ea2b79_148_0.png)

在 profile 标签页中选择堆快照后，你可以深入钻研堆上的对象。不仅如此，profile 标签页还会列出堆上每个对象的大小。这有助于识别应用程序中的内存泄漏，因为你经常会发现大量对象占据了服务器内存的很大一部分。这里显示了 profile 标签页中选中堆快照的截图。

![](img/79450811086e2fc8749ec4d309ea2b79_148_1.png)

## 核心文件 (Core Files)

在调试 Node 进程问题时，最强大的工具之一是导出运行进程的核心文件（core file），并使用 SmartOS 中的模块化调试 (mdb) 工具对其进行调查。现在 Linux 也可以创建核心文件并在 SmartOS 中分析。要在 Linux 上创建核心文件，你需要安装较新版本的 node 并将 `ulimit` 设置为 unlimited。许多进程分析工具（如 `pmap` 和 `pfiles`）仅限 SmartOS 使用。这可能是人们坚持使用 SmartOS 而非在 Linux 上导出后随后在 SmartOS 上分析的充分理由。但 Linux 核心文件的选项确实存在。

Joyent 致力于通过向 mdb 添加可以在加载 Node 核心文件后加载的命令来改进对 SmartOS 上 node.js 调试的支持。在 Node 0.12.0 及更高版本中，现在有了被称为 dcmds 的命令，包括 `nodebuffer`、`jsfunctions`、`jssource` 和 `v8internal`。这是在已经非常出色的 dcmds 列表之上的增强，例如 `findjsobjects`、`jsstack` 和 `jsprint` 等。

你可以通过附加到运行中的进程或传递核心文件作为参数来使用 mdb。通常，你会发现自己在查看一个现有的核心文件。如果你是附加到运行中的进程，需要将进程的 `pid` 传递给 mdb 的 `p` 参数。在附加或加载核心文件后，你应该通过输入 `::load v8` 将 v8 支持加载到 mdb 中。如果你需要从特定的 `v8.so` 加载，可以指向完整的文件路径。以下是在 bash 中该过程的样子：

```
# mdb corefile
Loading modules: [ libumem.so.1 libc.so.1 ld.so.1 ]
> ::load v8
V8 version: 3.14.5.9
Autoconfigured V8 support from target
C++ symbol demangling enabled
```

通常，接下来的步骤是调查获取核心文件时的堆栈。为此，你使用 dcmd `jsstack` 来打印堆栈。为了获取堆栈的额外信息，你应该传递 `-v` 参数以进入详细模式。这将打印出堆栈追踪及其相关的内存地址。内存中的这些项可以通过将地址传递给 `::jsprint` dcmd 来进一步检查。接下来的示例演示了获取 `jsstack` 并将其传递给 `jsprint` 及其显示结果的过程。

```
> ::jsstack -v
...
d7fffdf8bc0 0x4a14afaca2c8 <anonymous> (as Agent.addRequest)
(6e1f064b3aa1)
    file: http.js
    arg1: 67d9962cf1d1 (JSObject)
    arg2: 67d9962c2041 (SeqAsciiString)
    arg3: 3bb00000000 (SMI: value = 443)
    arg4: 60bc59304121 (Oddball: "undefined")
    ...
> 6e1f064b3aa1::jsprint
function <anonymous> (as Agent.addRequest)
```

另一个有用的 dcmd 是 `findjsobjects`，它将打印核心文件中可以找到的所有 JavaScript 对象。使用此命令，有时你可以简单地通过它打印出的内存中与相关签名匹配的对象数量来发现内存泄漏。你可以将 `findjsobjects` 的结果管道传输给 `jsprint` 以显示每个对象的内容。

在 mdb 之外，还有几种可以在 SmartOS 创建的核心文件上运行的有用进程工具。这些工具通常位于 `/usr/proc/bin` 中，包括以下命令：

```
# pwd
/usr/proc/bin
# ls -l
total 13
lrwxrwxrwx 1 root root 15 Jun 29 2013 pcred -> ../../bin/pcred
lrwxrwxrwx 1 root root 16 Jun 29 2013 pfiles -> ../../bin/
pfiles
lrwxrwxrwx 1 root root 16 Jun 29 2013 pflags -> ../../bin/
pflags
lrwxrwxrwx 1 root root 14 Jun 29 2013 pldd -> ../../bin/pldd
lrwxrwxrwx 1 root root 14 Jun 29 2013 pmap -> ../../bin/pmap
lrwxrwxrwx 1 root root 14 Jun 29 2013 prun -> ../../bin/prun
lrwxrwxrwx 1 root root 14 Jun 29 2013 psig -> ../../bin/psig
lrwxrwxrwx 1 root root 16 Jun 29 2013 pstack -> ../../bin/
pstack
lrwxrwxrwx 1 root root 15 Jun 29 2013 pstop -> ../../bin/pstop
lrwxrwxrwx 1 root root 15 Jun 29 2013 ptime -> ../../bin/ptime
lrwxrwxrwx 1 root root 15 Jun 29 2013 ptree -> ../../bin/ptree
lrwxrwxrwx 1 root root 15 Jun 29 2013 pwait -> ../../bin/pwait
lrwxrwxrwx 1 root root 14 Jun 29 2013 pwdx -> ../../bin/pwdx
```

在上述进程工具中，`pmap` 和 `pfiles` 特别有用。`pmap` 显示核心文件的内存映射，包括堆和缓冲区区域占用了多少内存。`pfiles` 能够报告创建核心文件的进程所使用的文件描述符。这对于识别 `ulimit` 是否不够高非常有用。有时，使用 `pfiles` 还可以帮助发现文件未被正确关闭而保持打开状态的情况。`pflags` 能够报告启动进程的原始命令。

## 总结

在本章中，我们探讨了用于调试 hapi 进程的不同工具。其中包括专门为帮助识别 hapi 服务器问题而生成的专用工具。使用 `good` 进行日志记录或使用 `tv` 进行本地调试会很有帮助。对于生产环境问题，使用核心文件或 REPL 同样有用。如果你发现 hapi 本身存在任何问题，请务必在 hapi 的 github 仓库中提交 issue。



# 安全 12

在第 11 章中，我们学习了各种调试应用的方法。既然我们的应用程序已经按预期运行，接下来需要确保它在面对黑客的恶意行为时仍能正常运作。

安全是 Web 开发的重要组成部分。但由于它对新手开发者来说可能既复杂又令人望而却步，通常不会出现在面向初学者的教程或文档中。因此，新的 Web 应用程序往往不包含任何防护措施，从而成为黑客（恶意的或其他性质的）的绝佳攻击目标。

大型网站也并非天生免疫。一些较为著名的漏洞利用事件（虽然更偏向恶作剧而非破坏性攻击）就曾影响过 Facebook。事实上，有些公司的员工可能有意或无意地通过 XSS 漏洞损害了竞争对手的产品。尽早做好安全防护，可以防范最常见的攻击向量，让你高枕无忧。

本章将介绍一些较为常见的安全问题和漏洞及其解决方案。

### 最佳实践

跟随以下内容，了解使用 hapi 时应采用的最佳安全实践。

### 密码哈希：BCrypt

将用户登录密码存储在数据库中时，以明文形式存储密码是非常糟糕的做法。如果恶意黑客获取了数据库访问权限，他们可以直接使用这些凭据立即造成巨大伤害。员工也可能能够查看或操纵敏感的用户数据。最好使用单向哈希算法，以哈希形式安全地存储密码，并可通过相同的哈希算法进行验证。

然而，市面上有许多不同的单向哈希算法，其中一些明显优于其他算法。在他那篇关于密码方案的著名博文中，Thomas Ptacek 逐一分析了那些经验不足的工程师所实现的典型简单哈希系统，并指出了它们有多么糟糕。他甚至链接了一个超低成本的 FPGA 实现，该实现可以瞬间破解最复杂的 MD5、DES、SHA1 和 SHA256 哈希。Thomas 将其称为"游戏结束"级别的攻击手段。

### 解决方案

BCrypt 是专为哈希敏感字符串（如密码）而设计的。
**Node.js BCrypt 实现**自 2010 年以来就已存在。多年来，它经过了多次安全和代码**审查**（包括我们自己的 Van Nguyen 的参与）。Node-bcrypt 使得以相对安全的方式哈希密码变得非常简单：

```javascript
var bcrypt = require('bcrypt');

// goes through 2^rounds iterations to generate salt
// higher numbers require SIGNIFICANTLY more time to calculate
var rounds = 12;

var salt = bcrypt.genSaltSync(rounds);
var hash = bcrypt.hashSync(user_input, salt);
// Store hash in your password DB.
```

### XSS

**跨站脚本攻击（XSS）**是最常见的漏洞之一。当一个包含文本表单输入的网页盲目接受用户输入的任意内容，并在另一个页面上未转义地显示这些输入时，就会产生这种漏洞。攻击者可以利用这一点注入恶意的客户端 JavaScript 代码，该代码会在任何查看该页面的人的浏览器中执行。
有关攻击者利用 XSS 的各种方式的详细分析，请参阅 **OWASP XSS 网页**。

### 解决方案

使用 `leizongmin` 开发的流行 **`js-xss`** 模块。`xss` 模块将对输入字符串进行转义，快速且便捷地防范大部分（如果不是全部）常见的 XSS 攻击向量。

```javascript
var Joi = require('joi');
var Xss = require('xss');

var config = {
    validate: {
        payload: {
            name: Joi.string().required().min(1)
        }
    },
    handler: function (request, reply) {
        var name = Xss(request.payload.name);
        return reply(name);
    }
};
```

```javascript
var Joi = require('joi');
var Xss = require('xss');

var config = {
    validate: {
        payload: {
            name: Joi.string().required().min(1),
            email: Joi.string().optional()
        }
    },
    handler: function (request, reply) {

        var output = {};
        output.name = Xss(request.payload.name);
        output.email = '';
        if (request.payload.email) {
            output.email = Xss(request.payload.email);
        }
        return reply(output);
    }
};
```

回顾第 5 章的内容，joi 可以验证我们的输入和输出。正如上面的示例所示，将 joi 与 xss 结合使用，我们可以确保输入的安全性，防止此类攻击。

### CSRF

跨站请求伪造（CSRF，读作"see surf"）是另一种常见的漏洞。攻击者可以利用它（通过 XSS）插入一段脚本或链接，使受害者的浏览器在一个完全不同但熟悉的网站（如银行网站）上提交表单。如果受害者拥有该银行网站的未过期 Cookie，该表单可能会被盲目接受，就好像受害者本人提交的一样。

### 解决方案

银行网站应该在表单加载时生成一个自定义标识符，该标识符是提交表单所必需的。没有此密钥，任何盲目提交的表单数据都将被拒绝。受害者必须亲自访问表单、填写各字段，然后提交，才能执行攻击者期望的操作。

使用 hapi 的 **crumb** 模块。

```javascript
// Server
var crumbOptions = {
    restful: false, // false enables payload level validation of crumb, true uses X-CSRF-Token header
    addToViewContext: true, // automatically add to view contexts
    isSecure: false // required if HTTPS is not used
};
server.register({ register: require('crumb'), options: crumbOptions}, function (err) {

    if (err) {
        throw err;
    }
});
```

```html
// View
<form action="/submit" method="POST">
    <input name="crumb" type="hidden" value="{{crumb}}"/>
    <!-- ... -->
</form>
```

```javascript
// POST `/submit` Handler
handler: function (request, reply) {

    return reply('ok'); // Do not have to do anything differently
}
```

### SSL

如今许多网站运行在裸 HTTP 上，而不是更安全的 HTTPS。这意味着浏览器和服务器之间的所有数据传输都以明文形式在网络上进行。由于网络的工作方式，同一网络上的任何人都可以查看所有数据传输流量，并看到密码、URL、消息等内容。

为网站增加安全性最简单的方法之一是强制用户使用 SSL/HTTPS。这需要购买和安装证书，但它会加密浏览器和服务器之间的所有流量。

为基于 Node.js 的 Web 服务配置 SSL 有多种方式。最常见的方式是使用 Apache 或 nginx/stunnel 等反向代理来处理 SSL 证书、终止加密，然后将流量通过未加密的 HTTP 转发到你的 Node.js 服务。这种方式无需对已正常运行的 HTTP hapi 应用程序做任何更改。有关如何使用 nginx SSL 终止的信息，请参阅 **DigitalOcean：如何设置带有 SSL 终止的 Nginx 负载均衡。**

或者，Node.js 也可以通过处理证书来终止加密，但这可能非常耗时并增加应用服务器的负载。有关如何使用 hapi SSL 终止的信息，请参阅 API 文档中 server.connection 的 `tls` 选项。以下是在 hapi 中启用 SSL 终止的基本示例：

```javascript
var Fs = require('fs');
var options = {
    port: 443,
    tls: {
        key: Fs.readFileSync(keyPath, 'utf8'),
        cert: Fs.readFileSync(certPath, 'utf8')
    }
}
server.connection(options);
```

### 请求头过滤

有许多漏洞可以通过设置或移除 HTTP 请求头来修复。在详细分析各种漏洞之前，下面是一种全局设置或移除请求头的通用方式：

```javascript
server.ext('onPreResponse', function (request, reply) {

    if (!request.response.isBoom) {
        request.response.output.headers.toAdd = 'someValue';
        delete request.response.output.headers.toRemove;
    }

    return reply();
});
```

或者，也可以在单个处理程序中操作，仅应用于单个路由：

```javascript
handler: function (request, reply) {

    return reply(output)
        .header('Content-Type', 'application/json')
        .header('X-Frame', 'DENY')
}
```



## 点击劫持 (CLICKJACKING)

点击劫持发生在您的网页被插入到 HTML iframe 中，导致用户的点击被劫持时。如果用户点击了您的主页按钮，攻击者可能会劫持该点击并将用户重定向到恶意网页。

### 解决方案
将 `X-Frame-Options` 响应头设置为 ‘DENY’ 将防止浏览器允许您的网页被放置在框架或 iframe (`<iframe>`) 内部。

## X-POWERED-BY

大多数服务器框架默认会在 HTTP 响应头 “X-Powered-By” 中声明用于生成页面的框架及其版本。

默认情况下，hapi 不会这样做。但是，如果您在公开博客中讨论您的 hapi 技术栈，攻击者也会看到这一点。

### 解决方案
减轻技术栈公开风险的一种常见方法是在您和用户之间提供一个中间代理。流行的选择包括 CloudFlare、Fastly 和 Akamai。

## IE 在上下文中打开 (IE OPEN WITHIN CONTEXT)

Internet Explorer 8 修复了一个旧漏洞，该漏洞允许攻击者在您站点的安全上下文中打开远程或本地 HTML 文件以运行恶意代码。要阅读更多关于此问题的信息，请参阅 [Microsoft Blog Post](https://blogs.msdn.microsoft.com/)（注：原文仅提供名称，此处保留链接形式）。

### 解决方案
将 'X-Download-Options' 设置为 'noopen' 将防止 Internet Explorer 8 及更高版本中出现此问题。

## 内容安全策略 (contentSecurityPolicy)

从技术上讲，默认情况下，浏览器将允许您从任何域名嵌入任意 JavaScript（通过 script 标签）。这通常是可以接受的。然而，如果开发人员在代码中输入了错别字，可能会导致加载错误的文件并执行恶意代码。

或者，如果 Web 应用程序允许用户指定自己的 JavaScript 嵌入到页面中，安全管理可能会迅速失控。

### 解决方案

现代浏览器现在支持一个名为内容安全策略 (Content Security Policy, CSP) 的系统。通过返回一系列 HTTP 响应头，可以强制浏览器创建一份可接受域名的白名单，并将 `script-src` 调用限制在仅限此列表。

将 **blankie** 与 **scooter** 结合使用，可以快速定义 CSP 规则。

```javascript
var Hapi = require('hapi');
var Blankie = require('blankie');
var Scooter = require('scooter');

var server = new Hapi.Server();

server.pack.register([Scooter, {
    plugin: Blankie,
    options: {} // specify options here
}], function (err) {

    if (err) {
        throw err;
    }

    server.start();
});
```

## 跨源资源共享 (CORS)

默认情况下，现代浏览器将阻止对任何与当前页面域名不匹配的域名的 AJAX 调用。这是因为主流 Web 浏览器强制执行 **“同源”策略 (Same-Origin policy)**。同源策略是 Web 安全的一个关键方面。

然而，作为开发人员，您可能 *想要* 允许您的 Web 应用程序直接访问第三方 API，甚至是您自己在不同域名上的 API。

CORS (**Cross-Origin Resource Sharing**) 允许您通过显式指定浏览器允许通过 AJAX 连接到哪些域名，以安全且可靠的方式实现这一点。这是通过在响应时向浏览器发送自定义响应头来完成的。

### 解决方案

hapi 原生支持 CORS，但出于安全考虑，默认情况下它是禁用的。启用它非常简单，只需将服务器选项 'cors' 设置为 `true`，或者为其传递一个包含一个或多个允许 'origins'（源）的配置对象。

```javascript
var serverOptions = {
    // ...
    cors: {
        origin: [
            'http://localhost:8080',
            'http://localhost:8000'
        ]
    }
};
var server = new Hapi.Server();
server.connection(serverOptions);
```

在 hapi 中，CORS 也可以针对每个路由单独应用：

```javascript
server.route({
    method: 'GET',
    path: '/custom-cors',
    cors: {
        origin: [
            'http://localhost:9000',
            'http://localhost:8000'
        ]
    },
    handler: function (request, reply) {
        return reply("This response has custom CORS headers set.");
    }
});
```

配置好 CORS 后，hapi 将自动设置正确的响应头。然后，您的客户端应用程序就可以安全地访问您的源主机。

## crossdomain.xml

如上所述，CORS 允许 Web 应用程序开发人员控制其客户端 JavaScript 可以向哪些域名发起请求。某些应用程序使用了 CORS 无法过滤的技术，例如 Adobe Flash。对于 Flash，Adobe 定义了一个跨域策略文件 `crossdomain.xml`。

### 解决方案

```xml
<?xml version="1.0" encoding="UTF-8"?>
<cross-domain-policy xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="http://www.adobe.com/xml/schemas/PolicyFile.xsd">
  <allow-access-from domain="your_domain.com" />
  <allow-access-from domain="your_other_domain.com" />
  <site-control permitted-cross-domain-policies="master-only"/>
  <allow-http-request-headers-from domain="*.your_domain.com" headers="*" secure="true"/>
</cross-domain-policy>
```

```javascript
var Fs = require('fs');

server.route({
    method: 'GET',
    path: '/crossdomain.xml',
    handler: function (request, reply) {
        return reply(Fs.readFileSync('./crossdomain.xml').toString());
    }
});
```

## 总结

在本章中，您已经了解了如何使用 hapi 来防御最常见的 Web 安全漏洞。

## 回顾

在本书中，我们对 hapi 进行了快速介绍。我们学习了如何设置服务器以及请求生命周期是如何工作的，以便我们可以对其进行扩展以满足我们的需求。我们设置了路由、处理器，并学习了如何将代码组织成更小的组件以实现复用和提高可读性。验证机制被引入，不仅用于强制执行输入规范，还用于输出规范。插件组织了我们的代码，我们了解到利用插件可以提高效率，并且比传统的中间件方法更有益。我们学习了如何利用身份验证插件来增强您的应用程序。我们展示了一些常见的模型用例，以及如何为应用程序使用模板，以便在处理器中分离演示层。最后，我们展示了如何测试、调试并为您的应用程序添加安全性，使其达到生产就绪状态。

如果您发现自己仍然需要帮助，hapi 有一个非常出色的社区。有许多获取帮助的途径，最好的起点是 [hapijs.com/help](https://hapijs.com/help)。我们鼓励您参与帮助页面中提到的导师计划，使社区变得更加强大。请遵守《会议行为准则》以保持尊重，这样我们才能继续拥有一个优秀的社区。

一旦您掌握了相关技能，我们鼓励您成为一名活跃的参与者，指导他人，通过贡献来帮助解决问题，或以任何您可以提供的方式支持社区，以继续加强社区建设。

您还可以利用其他资源来提升您的 hapi 技能。有一个名为 makemehapi 的 node school 自学课程。此外还有教程和其他资源。

我们希望通过阅读本书，能够帮助您开始您的第一个 hapi 项目。您可以使用 hapi 来实现您的梦想，构建各种有趣的 Web 应用程序。

# 附录 13

### 模型 (Models)

#### 历史

可扩展的应用程序通常遵循 n 层架构，其中应用程序服务连接到一个正交数据库（这意味着它与应用程序服务不是紧耦合的，可以独立管理，甚至可以完全更换）。

如今，有许多可用的数据库。数据库主要分为三大类：

- 关系型 (RDBMS)
- NoSQL
- 其他

关系型数据库是数据库领域的主力军。它们在数十年中一直有效运作，并证明了其性能特性。然而，它们有一定的学习曲线，并不总是适合处理顺序数据、反规范化数据或极高性能要求的场景。

NoSQL 数据库相对较新。通常，这些数据库的学习曲线非常短，并具有高性能特性。然而，由于权衡，它们不具备关系型数据库通常关联的所有特性（如事务、原子性、数据持久性等）。

其他数据库可能包括图数据结构数据库或任何不符合上述两类定义的数据库。

### HTTP 客户端概述

#### 历史

在互联网还完全处于 Web 1.0 时代时，大多数网站和公司并不提供开发者友好的 API。要从网站获取数据，开发人员需要通过抓取 (scrape)



 # 第 13 章：附录

访问网站，处理 HTML，然后搜索并提取数据（有时需要手动进行）。一些公司开始提供 SOAP API，但（谢天谢地）这些 API 已经销声匿迹了。

Web 2.0 应用程序在 2004 年左右成为新常态，它们支持具有 XML 和 JSON 响应的 API。Java 曾与 XML 强耦合并采用了它。但随着 JavaScript 的普及以及像 jQuery、Dojo、Prototype 这样基于 AJAX 的优秀开源库的出现，JSON 基本上赢得了胜利。JavaScript 和 Node.js 与 JSON 配合得非常出色。

如今大多数 API 主要支持 JSON。我们的示例将展示与 JSON 交互的代码。

为了从 HTTP API 获取数据，我们有几种选择。我们将涵盖两种最受欢迎的选项：Wreck 和 Request。

## WRECK

Wreck 是由本书共同作者 Wyatt Preul 编写的官方 hapi 模块之一。

它的创建是为了应对那个如今臭名昭著的 4 字节内存泄漏问题。其中一个罪魁祸首就是一个被广泛使用的 Request 模块所使用的底层代码。

此外，Request 的设计旨在完成广泛的使用场景。而 Wreck 采用了极简主义方法，仅提供最基本的功能集，以确保高性能且无内存泄漏。

## REQUEST

Request 是 Node.js 中最著名的 HTTP 请求模块。它最初由 Mikeal Rogers 创建（他是 Node.js 社区中一个非常知名的人物），但现在该项目已经独立发展。由于其简单、直观的接口，它获得了巨大的追随者（它比之前手动创建 HTTP 套接字那种冗长的做法要先进得多）。

## 数据库客户端概述

hapi-plugins.com 通过 Mongoose 驱动程序使用 MongoDB，因此主要示例将体现这一选择。

然而，为了获得最大收益，本书还将为 Node.js 项目中三种最常用的数据库提供单独的示例：MongoDB、Cassandra 和 Postgres。

### MONGODB

**MongoDB** 是一款极受欢迎的数据库。它是首批拥抱 NoSQL 运动以及开源开发模式的数据库之一。它在 GNU Affero 许可下免费提供。

与 MySQL 或 PostgreSQL 不同，MongoDB 是一个文档导向（document-oriented）的数据库。在 MongoDB 中，不需要将一个人的姓名、地址等数据分开存储，而是可以将这些字段一起存储在该个体的单个文档中。这种方式在操作起来非常直观。

MongoDB 支持一套简单但强大的基于 JavaScript 的查询语法，且学习曲线非常短。这使得 MongoDB 成为快速启动项目、黑客松以及已经熟悉 JavaScript 的团队的流行选择。

MongoDB 主要有两个缺点。首先，可扩展性不是线性的，需要设置稍显复杂的复制系统。其次，由于数据库级别的锁定，写入性能可能会成为问题，且默认设置在写入未验证时可能会导致数据丢失。

从实际应用角度来看，在撰写本书时，关于使用哪个 MongoDB ORM/驱动程序的选择存在很大争议。

一方面，Mongoose 非常流行且拥有许多实用功能；然而，在撰写本书时，Mongoose 的 GitHub 仓库有超过 400 个开放问题（open issues）和近 2000 个已关闭问题。由于 Bug 如此之多，它可能并不总是最佳选择。

`mongodb` 驱动程序简单且高效，但提供的高层功能非常少，因此需要更多的开发工作。

#### mongodb

**mongodb 驱动程序**（也称为 node-mongodb-native）是访问 MongoDB 数据库实例最流行的库。它相当准确地模拟了实际的 MongoDB 语法，并根据需要进行了一些异步修改。因此，它与其说是 ORM，不如说是一个手动数据库驱动程序。因此，需要对 MongoDB 查询语法有深入的了解。幸运的是，MongoDB 的语法非常简单，很容易上手。

#### Mongoose

**Mongoose ODM** 是一个用于 MongoDB 的高级对象资源映射器。Mongoose 由 LearnBoost（现为 Automattic 的一部分）创建，它通过添加对队列操作、模式（schemas）、模式验证器、默认值、方法等支持，提供了一种脱离纯 MongoDB 语法的抽象，旨在使使用 MongoDB 的开发更加快速和简单。

### CASSANDRA

**Cassandra** 是另一种流行的开源 NoSQL 数据库。与 MongoDB 专注于开发者的易用性不同，Cassandra 专注于利用数学和科学为开发者提供可扩展性和高可用性（能够承受多台机器故障），同时展现出极高的性能。它还专注于简单的线性可扩展性，这意味着扩展规模就像向集群中添加机器一样简单（无需复杂地设置复制系统，一切都是自动的）。

Cassandra 是一个列导向（column-oriented）的数据库。数据库中的每条记录可以拥有任意数量的列作为字段。不同的记录可以拥有不同数量的列。例如，一个 Person 对象可以只有姓名和地址，而另一个 Person 可以有姓名、地址和电话号码。读取时会检索 Person 的所有列。列数据库可能不如文档数据库直观，但它们具有许多意想不到的实用好处（例如擅长存储和管理图数据结构）。

Cassandra 的主要缺点是其学习曲线相对较陡。入门 Cassandra 比较困难。然而，一旦配置正确，Cassandra 的特性和优势很难被超越。

#### Apollo

由 3logic 开发的 Apollo 是一款新兴的 Cassandra ORM。尽管 Apollo 的开发起步相对较晚（2014 年中期），但它已经完全可用，并兼容 Cassandra CQL 接口最新的破坏性更改。从技术上讲，作者在他们的 README.md 中指出 Apollo 是“不完整的”，可能尚未达到生产就绪状态。尽管如此，Apollo 仍远好于目前现有的其他替代 ORM。

#### cassandra-driver

**Cassandra-driver** 是官方的 DataStax Node.js 到 Cassandra 的驱动程序。它支持所有最新特性且处于积极维护中。然而，它几乎不提供任何高层特性，因此需要进行一定的开发才能创建有效的模型。

### POSTGRES

PostgreSQL 是一款非常流行的开源 RDBMS（关系型数据库管理系统），是 MySQL 或 Oracle SQL 的替代方案。尽管免费使用，但它提供了许多商业关系型数据库的功能。

与 MongoDB 或 Cassandra 不同，PostgreSQL 遵循关系数据模型。这需要相对较长的设置时间来配置数据模式（schemas）和索引。然而，这也意味着数据验证在数据库端免费完成（而上述 NoSQL 数据库则在驱动程序/客户端端完成）。

使用 PostgreSQL 的主要缺点是学习曲线。关系数据模型系统可能难以快速掌握，并且在索引、数据分组等方面有很多特性。

#### pg

与 `mongodb` 驱动程序类似，`pg` 模块（也称为 node-postgres）更像是一个驱动程序，而不是一个功能齐全的 ORM。

#### Sequelize

Sequelize 是一个功能齐全的 ORM，支持许多不同的基于 SQL 的数据库，包括 MySQL、MariaDB、SQLite、MSSQL，当然还包括 PostgreSQL。它支持完整的模式定义与同步/迁移、关联关系、Promise、事务、预取以及许多其他功能。它在生产环境中也非常健壮且经过充分测试。

## 连接

### MONGODB::MONGODB

```
var mongodbOptions = {
    'connection': 'mongodb://localhost:27017/hapiplugins',
    'options': {
        'uri_decode_auth': false,
        'db': null,
        'server': null,
        'replSet': null,
        'mongos': null
    }
};

var MongoClient = require('mongodb').MongoClient;

MongoClient.connect(
    mongodbOptions.connection,
    mongodbOptions.options,
    function (err, client){
    }
);

var MongoClient = require('mongodb').MongoClient;

exports.register = function (plugin, mongodbOptions, next) {
    MongoClient.connect(
        mongodbOptions.connection,
        mongodbOptions.options,
        function (err, client){
            if (err) {
                throw err;
            }
            plugins.expose('mongodbClient', client);
            next();
        }
    );
};
```



## 第 13 章：附录

### MONGODB::MONGOOSE

```javascript
var mongooseOptions = {
    'connection': 'mongodb://localhost:27017/hapiplugins'
};

var Mongoose = require('mongoose');

Mongoose.connect(mongooseOptions.connection);
// 无异步调用：
//     Mongoose 查询会自动
//     排队直到连接建立
```

```javascript
var Mongoose = require('mongoose');

exports.register = function (plugin, mongodbOptions, next) {

    Mongoose.connect(mongooseOptions.connection);

    // 以下在技术上是不必要的
    //     当从任何文件 require 时
    //     require('mongoose') 现在将指向此客户端
    plugins.expose('mongoose', Mongoose);

    next();
};
```

### CASSANDRA::APOLLO

```javascript
var cassandraOptions = {
    'connection': {
        'hosts': [
            "127.0.0.1"
        ],
        'keyspace': 'hapiplugins',
        // 'username': '',
        // 'password': '',
    },
    'options': {
        'class': 'SimpleStrategy',
        'replication_factor': 1
    }
};

var Apollo = require('apollo');

var client = new Apollo(
    cassandraOptions.connection,
    cassandraOptions.options
);

client.connect(function (err){
    if (err) {
        throw err;
    }

    // client 现在已连接
});
```

```javascript
var Apollo = require('apollo');

exports.register = function (plugin, cassandraOptions, next) {

    var client = new Apollo(cassandraOptions.connection, cassandraOptions.options);

    client.connect(function (err){

        if (err) {
            throw err;
        }

        plugins.expose('cassandraClient', client);

        next();
    });
};
```

### POSTGRES::PG

```javascript
var pgOptions = {
    'connection': 'postgres://username:password@localhost/database',
    'options': {}
};

var Pg = require('pg');

var client = new Pg.Client(pgOptions.connection);
client.connect(function (err) {

    if (err) {
        throw err;
    }

    // client 现在已连接
});
```

```javascript
var Pg = require('pg');

exports.register = function (plugin, pgOptions, next) {

    var client = new Pg.Client(pgOptions.connection);
    client.connect(function (err) {

        if (err) {
            throw err;
        }

        plugins.expose('pgClient', client);

        next();
    });
};
```

### Postgres::Sequelize

请注意：Sequelize 要求安装与 postgres 相关的 node 模块：

```bash
$ npm install --save sequelize pg pg-hstore
```

```javascript
var seqOptions = {
    'connection': 'postgres://username:password@localhost/hapi-plugins',
    'options': {
        dialect: 'postgres',
    }
};

var Sequelize = require('sequelize');

var client = new Sequelize(seqOptions.connection, seqOptions.options);

var Sequelize = require('sequelize');

exports.register = function (plugin, seqOptions, next) {

    var client = new Sequelize(seqOptions.connection, seqOptions.options);

    plugins.expose('sequelize', client);

    next();
};
```

## 模式 (Schemas)

**MongoDB::mongodb**

在使用 mongodb 驱动程序时，模式（Schemas）并不真正适用。对于任何需要模式验证的应用，请使用 Joi 在插入或更新文档之前提供一些验证。

```javascript
var Joi = require('joi');

var internals = {};

internals.plugin = Joi.object().keys({
    'name': Joi.string().required(),
    'description': Joi.string().optional(),
    'version': Joi.string().required(),
    'authors': Joi.array().optional(),
    'license': Joi.string().optional(),
    'repository': Joi.string(),
    'homepage': Joi.string(),
    'updated_at': Joi.date(),
    'created_at': Joi.date(),
    'keywords': Joi.array(),
    'dependencies': Joi.array(),
    'dependents': Joi.array(),
    'stats': Joi.object().keys({
        'releases': Joi.string(),
        'downloads': Joi.string(),
        'downloads_this_month': Joi.string(),
        'open_issues': Joi.string(),
        'pull_requests': Joi.string()
    })
});

// 稍后使用
// var pluginToAdd = {name: 'hapi', ...};

Joi.validate(pluginToAdd, internals.plugin, function (err, value) {

    if (err) {
        throw err; // 无效模式
    }

    var collection = mongodbClient.collection('plugin');
    collection.insert(pluginToAdd, function (err, result) {
        if (err) {
            throw err;
        }

        // 成功
    });
});
```

### MongoDB::Mongoose

```javascript
var internals = {};

internals.plugin = new Mongoose.Schema({
    'name': { type: String, required: true },
    'description': { type: String, required: false },
    'version': { type: String, required: true },
    'authors': { type: Array, required: false },
    'license': { type: String, required: false },
    'repository': { type: String },
    'homepage': { type: String },
    'updated_at': { type: Date, default: Date.now },
    'created_at': { type: Date, default: Date.now },
    'keywords': { type: Array },
    'dependencies': { type: Array },
    'dependents': { type: Array },
    'stats': {
        'releases': { type: String },
        'downloads': { type: String },
        'downloads_this_month': { type: String },
        'open_issues': { type: String },
        'pull_requests': { type: String }
    }
});

var plugin = Mongoose.model('plugin', internals.plugin);

var internals = {};

internals.user = new Mongoose.Schema({
    'username': { type: String, required: false },
    'name': { type: String, required: false },
    'email': { type: String, required: false },
    'updated_at': { type: Date, default: Date.now },
    'created_at': { type: Date, default: Date.now },
    'likes': [internals.plugin]
});

var user = Mongoose.model('user', internals.user);
```

### Cassandra::Apollo

```javascript
var pluginSchema = {
    fields: {
        'name': 'text',
        'description': 'text',
        'version': 'text',
        'authors': 'text',
        'license': 'text',
        'repository': 'text',
        'homepage': 'text',
        'updated_at': 'int',
        'created_at': 'int',
        'keywords': 'text',
        'dependencies': 'text',
        'dependents': 'text',
        'stats-releases': 'int',
        'stats-downloads': 'int',
        'stats-downloads-this-month': 'int',
        'stats-open-issues': 'int',
        'stats-pull-requests': 'int'
    }
};

var Plugin = client.add_model('plugin', pluginSchema);

var userSchema = {
    fields: {
        'username': 'text',
        'name': 'text',
        'email': 'text',
        'updated_at': 'int',
        'created_at': 'int',
        'likes': 'text'
    }
};

var User = client.add_model('user', userSchema);
```

## 模板引擎

### 精选模板引擎概述

目前有很多模板引擎。虽然 **hapi-plugins** 应用程序使用了最受欢迎的 JavaScript 专用引擎 Handlebars.js，但本书将展示五种最流行模板引擎的示例：Mustache, Handlebars, Jade, Dust 和 ECT。

### MUSTACHE.JS / HOGAN.JS

Mustache 由 Chris Wanstrath（GitHub 知名人物）创建，被定义为一种“与框架无关的渲染无逻辑视图的方式”。它将逻辑与演示严格分离——在模板本身中无法包含任何逻辑。

它几乎在每种编程语言中都得到了支持。因此，Mustache 模板具有极高的可移植性，可以在不同编程语言的项目之间轻松共享。

截至 2014 年，最流行的 Node.js Mustache 编译器是 Mu。但 Hogan.js 的受欢迎程度正在上升。Hogan.js 是一个极速的 JavaScript（支持 Node.js 和浏览器内 JavaScript）Mustache 模板编译器。

### HANDLEBARS.JS

Handlebars 由 Yehuda Katz（Ruby on Rails, Ember.js 和 jQuery 知名人物）创建，作为 Mustache 的扩展。它目前由 Kevin Decker (WalmartLabs) 积极维护。

Handlebars 旨在通过支持标签内的表达式（直接访问对象的子键）、局部模板（partials，可重用的模板片段）和辅助函数（helpers，可在模板内任何位置使用的 JavaScript 函数）来简化模板编写。这些特性使得维护具有大量模板的大型 JavaScript 应用程序变得更加容易。然而，正因如此，Handlebars 模板的可移植性远不如前者。

但对于 hapi 应用程序来说，Handlebars 到目前为止是最受欢迎的模板引擎。

### JADE

Jade 由 T.J. Holowaychuk（Express.js 知名人物，在从 Node.js 退休前是最多产的 Node.js 模块作者之一）创建。它被设计为一个“鲁棒、优雅、功能丰富”的模板引擎，借鉴了 Ruby on Rail 的 Haml 引擎的许多概念。

Jade 专门为 HTML 内容的模板化而设计。然而，与其他模板引擎不同，它需要使用与输出格式（HTML）不同的自定义语法。因此，它的学习曲线更高，并且实际上将应用程序锁定在必须使用 Jade。

### DUST

Dust 由 Aleksander Williams 创建。它旨在避免 Mustache 变体版本的局限性。它默认是异步的且可组合的。它具有与 Mustache 相似的语法且高度可定制。Dust.js 被 Netflix 频繁使用。



### ECT

ECT 由 Vadim Baryshev 创建。它号称是“具有嵌入式 CoffeeScript 语法的最快 JavaScript 模板引擎”。ECT 专注于性能和提升以及开发便捷性特性，例如自动重新加载、模板中对 JavaScript 和 CoffeeScript 逻辑的支持、多行表达式以及标签自定义。
