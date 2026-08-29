
# 单页 Web 应用开发指南：使用 Node.js、MongoDB、AngularJS 和 Express 框架全栈 JavaScript 环境构建强大且可扩展的单页 Web 应用

使用 Node.js、MongoDB、AngularJS 和 Express 框架的全栈 JavaScript 环境构建强大且可扩展的单页 Web 应用

## 鸣谢

| 作者 | 项目协调员 |
| --- | --- |
| Fernando Monteiro | Harshal Ved |
| 审稿员 | 校对员 |
| Shivang Agarwal | Maria Gould |
| Giacomo Zinetti | Linda Morris |
|  | Jonathan Todd |
| 委托编辑 | 索引员 |
| Edward Gordon | Priya Sane |
| 采购编辑 | 图形 |
| James Jones | Abinash Sahu |
| 内容开发编辑 | 制作协调员 |
| Athira Laji | Shantanu N. Zagade |
| 技术编辑 | 封面工作 |
| Vivek Arora | Shantanu N. Zagade |
| 拷贝编辑 |  |
| Simon Bhogal |  |
| Ameesha Green |  |
| Relin Hedly |  |
| Deepa Nambiar |  |

## 关于作者

Fernando Monteiro 是一位前端工程师、演讲者、开源贡献者，也是 Responsive Boilerplate 的后大脑，这是一个使用 Less.js 构建的用于响应式布局的 CSS 库。

他在博客上为整个网络社区贡献了许多关于设计、开发和用户体验的文章和材料。

他热衷 Web 标准、前端开发和移动设计，在过去的 12 年里致力于创建高端图形和 Web 体验。

他于 2002 年开始担任平面设计师，迅速成为 QuarkXpress 专家，为全球不同的公司制作和编辑了 500 多个广告、CD 和 DVD。

他还出版了一本关于 HTML5 和移动设备响应式设计的书：《Instant HTML5 Responsive Table How-to》。

目前，他在一家为政府机构提供 Web软件开发的最大的公司之一担任前端经理。你可以在 www.newoceanweb.com.br 找到更多关于他的信息。

> 我感谢在这段旅程中支持我的每个人。感谢 Ellen 所有的鼓励时刻；我的儿子 Mateus 一直陪在我身边；我的母亲 Pascoalina Patrizzi 以及我的妹妹 Marcia Monteiro。

> 我还要感谢 Packt Publishing 所有与我直接接触的成员，感谢 James Jones 和 Athira Laji 他们的耐心和支持。

## 关于审稿员

Shivang Agarwal 在过去的 5 年里一直从事 Web 应用领域。到目前，他在三家不同的初创公司工作过，包括自己的一家。这些产品都是 Web 应用，每天为数百万用户服务。在初创公司工作这么久让他有很多机会尝试新技术。

他是一个全栈开发者也是一个产品经理。目前，他在一家电商初创公司 Browntape 担任 AVP 工程师并领导那里的技术团队。过去，他曾领导另一家社交领域初创公司的工程团队。他在 SPA 开发、基础设施管理以及扩展产品以服务每天数百万用户方面拥有丰富的经验。

> 我感谢我的父母 Sunil 和 Manisha Agarwal，我的兄弟和妻子 Shubham 和 Smoranika Agarwal，以及我的妻子 Krit 他们的支持和耐心。

Giacomo Zinetti，也称为 Giko，是一位来自米兰附近安静小镇 Bregnano 的全栈 Web 开发者。

自 1999 年以来，他就一直热衷 Web 开发，通过创新的用户体验和酷炫的图形界面构建更好的网站和应用程序，并始终关注最新技术。

他喜欢与爱好者团队一起工作，这样他们就可以互相分享经验。

他不仅通过显示器生活，还通过旅行、摄影、杂耍、驾驶（尤其是摩托车）、滑雪、玩桌游、和朋友在一起以及玩一种名为 tchouk 的新奇运动生活。

你可以在 Twitter @giacomozinetetti 或他的网站 https://giko.it/ 上找到他。

## 为什么要订阅？

- 可全文搜索 Pack 出出的每一本书
- 复制、粘贴、打印和书签内容
- 按需提供并通过网络浏览器访问

## Packt 账户持有者的免费访问

如果您在 www.Packt.com 拥有 Packt 账户，今天可以使用它访问 PackLib 并查看 9 本完全免费的书。只需使用登录凭据即可立即访问。

> 我把这本书献给我父亲的纪念：

索引 189

# 前言

动态 Web 应用和无需页面刷新的实时更新、可扩展性、高性能以及极其丰富的界面正日益主导 Web 开发市场，这种开发 Web 内容的新方法被称为单页应用（SPA）。这种开发方式允许你编写更少的服务器脚本代码和更多的客户端代码（通常专注于 JavaScript），通过与应用交互的新方式提供更好的用户体验。Gmail、Trello 和 Groupon 等产品都是成功的 SPA 开发案例。

在整本书中，我们将展示在评估市场上现有工具/框架时的关键点，以通过 SPA 开发提供良好的用户体验。此外，我们还介绍了 JavaScript 全栈应用的概念，即使用 Node.js 和 MongoDB 构建 RESTful API。

如何处理所有技术并充分利用其价值是一个非常有趣且具有激励性的任务。在本书中，我们将学习如何使用最新、最强大的技术构建示例应用，从而充分利用这种开发方法。

## 本书内容

第 1 章“理解单页应用”涵盖了 MVC 模式。本章讨论了可用的库。

第 2 章“深入研究 Node.js”涵盖了服务端。本章介绍了 ODM。

第 3 章“使用 MongoDB 和 Node.js 构建 API”展示了 CRUD 操作。本章使用了该框架。

第 4 章“创建一个会议 Web 应用”展示了模板引擎。本章使用了 Express。

第 5 章“开始学习 AngularJS”涵盖了项目组织。本章准备了

第 6 章“理解 Angular 视图和 MEAN.JS 生成器”释放了 MEAN.JS 栈的力量。

第 7 章“使用 Karma 和 Protractor 测试 Angular SPA”实现了单元测试和端到端测试。本章使用了 Selenium。

第 8 章“将应用部署到云端”查看了一些生产环境中重要的部署。

## 本书所需的准备

## 理解单页应用

单页应用（SPA）是一种适应单个页面的 Web 应用程序或网站，目标是提供更友好的体验和丰富的界面。此外，单页并不限于一个文件；我们可以有许多不同的文件。此类应用程序可以从简单的增删改查（CRUD）应用（如待办列表）变化到具有无数视图、库、模板和验证的复杂水平。

为了获得更好的 SPA 示例，你可以查看 http://todmvc.com/；在这里，你可以找到关于许多 MVC 框架的信息。接下来的几段将展示更多关于客户端 MVC 的内容。

Trygve Reenskaug 在 20 世纪 70 年访问 Xerox Parc 时将 MVC 引入了 Smalltalk-76；80 年代，Jim Althoff 等人为 Smalltalk-80 类库实现了一个版本的 MVC。MVC 此后在 1998 年的一篇文章中被阐述为一个通用概念。更多信息可以在 https://heim.ifi.uio.no/tryver/thems/mvc/index.html 找到。

SPA 近期吸引了大量开发者，但这种开发模型有什么特别之处或争议之处呢？这些缩写 HTML、MVC、MVP 和 MVVM 意味着什么？

这些问题的答案非常简单：等一下，JavaScript？你应该问，“那么 HTML、CSS 和数据库呢？”我们使用 JavaScript 根据全栈开发中的 MEAN 标准来建模应用。我们将一步步进行。在深入研究 SPA 的工作原理之前，我们需要了解 MVC 架构。

## 理解 MVC/MVVM/MV* 模式

MVC 是一种出现于 20 世纪 80 年代的软件架构模式，它将信息的视觉表示与用户交互分离。

然而，我们谈论的是客户端的 MVC 模式，更具体地说，是 Java、C# 和 Ruby 等语言在客户端运行的模式。另一个非常重要的方面是理解每个模型代表什么，请看以下内容：

- 表现模型 (PM)
- 模型视图演示器 (MVP)
- 模型-视图控制器 (MVC)
- 模型-视图模型 (MVVM)

在本章的稍后部分中，我们将详�介绍这些概念。现在，让我们看看 MVVM 的外观。

## 理解单页应用

2004 年，Martin Fowler 发表了一篇关于“表现模型”（Presentation Model）设计模式的小文章。以下是 PM 的图示：

| 视图 | 表现模型 | 模型 |
| --- | --- | --- |
| - 视图与模型交互以收集视觉内容。 |
| - 表现模型更新并观察模型。它还通知视图视觉内容的变化。 |

![](img/76faac513e4fd5843aeb56a4cadac9_26_0.png)

大约一年后，2005 年，Windows Foundation (WPF) 和 Silverlight 的架构师 John Gossman 在他的博客上揭示了一种新模式，命名为模型-视图模型。

> John Gossman 的原始博客文章可以在 http://blogs.msdn.com/b/johngossman/archive/2005/10/08/47863.aspx 查看。

MVVM 与表现模型非常相似；两种模式对视图状态和行为的抽象（在前端，视图是用户看到的）包含了状态和行为。它们之间的区别在于 MVVM 模型更加标准化，并在 Silverlight 中使用了多年。

MVVM 基于 MVC 和 MVP，试图更清晰地将用户界面（前端）开发与应用程序中的业务逻辑和行为分离。

你可能会问：“与 SPA 有什么关系？”

> 关于 MVVM 模型出现的精彩资源可以访问 http://msdn.microsoft.com/en-us/magazine/dd419663.aspx。如今，我们可以清楚地看到这种实现应用于 Durandal.js、Kendo UI、Ember.js、AngularJS 和 Knockout.js 等某些 JavaScript 框架。其中每一个都有自己的实现方式；但它们具有相同的概念。以下是 MVP 的图示：

![](img/76faac513e4fd5843aeb56a4cadac9_27_0.png)
- 视图与模型交互进行简单的数据绑定。
- 视图通过演示器和数据绑定进行更新。

> Backbone.js 是第一个流行的 MVC 库

我们今天拥的所有的所有框架都遵循标准的 MV* 模式。现在，让我们回顾 MVVM 的概念：

- **模型 (Model)**：代表应用程序处理的特定特定数据或信息。模型持有信息，但通常不处理行为。它们不格式化信息或影响数据在浏览器中的显示方式，因为这不是它们的职责。
- **视图 (View)**：这是用户实际交互的唯一部分。它包含数据绑定和事件，是一个代表 ViewModel 状态的交互式 UI。视图不负责处理状态——它与 ViewModel 同步。
- **ViewModel**：可以被视为一种特殊的控制器，充当数据转换器。它将模型信息转换为视图信息，将命令从视图传递给模型。

## 理解单页应用

视图和 ViewModel 使用数据绑定和事件进行通信。以下是 MVVM 工作原理的图示：

![](img/76faac513e4fd5843aeb56a4cadac9_28_0.png)
- 视图与模型交互进行数据绑定。
- 模型持有信息。

为了更好地理解 MVVM，让我们来看看双向数据绑定。双向绑定是指将对象属性的更改绑定到 UI 的能力。换句话说，如果我们有一个带有 `name` 属性的用户对象，每当我们给 `user.name` 分配新值时，UI 都应该显示新名称。

```javascript
var user = {
  name: "fernando",
  age: 25
}
```

MVP 和 MVVM 是 MVC 的派生。两者之间的关键区别在于每一层对其他层的依赖关系，以及它们彼此结合紧密程度。

## SPA 与传统 Web 开发之间的区别

让我们回顾一下使用 MVC/MVVM 模式构建 Web 应用的一些重要点，而不是构建传统的 Web 应用。

其中一个重要的一点是，MVC 模式可以应用于服务端或客户端。例如，我们可以使用像 Express 这样的某些 JavaScript 库在服务器端运行 MVC 模式，并仅在服务器端（在此例下为 Node.js）构建一个 SPA。这是因为 MVC 是一种软件架构模式，可以应用于双方：前端可以使用带有 MVC 的前端框架，服务器端则可以使用如 Ruby on Rails 和 .NET 这样的服务端框架。

在 SPA 中，无论页面上发生了什么；如前所述，在页面请时不会发生刷新，这与多页应用不同（后者每次请求都会加载页面）。所有必要的内容都通过 Ajax 和 HTML 模板注入到页面中以渲染内容。

我们认为这是 SPA 与多页应用之间的主要区别：在每请求一个新页面时，我们都会产生一个新的请求。

还有许多其他差异需要考虑，但最好的工具是能提高你生产效率的工具。因此，选择应该基于项目的范围、预算以及开发团队的技术水平。

JavaScript MVVM 或 MV 促进了 UI 及其支撑构建的更易并行开发。你可以让一个前端开发者负责 UI、HTML 模板和数据绑定，而让另一个开发者负责同一页面的服务器端逻辑。

> 在多页应用中，HTML 代码是在服务器上生成的，这使得用户界面的样式设计和定制工作变得更加困难。通常，我们无法在同一个场景上进行同步工作。

此外，在多页应用中，使用的模板是服务端模板，因此网页会被解析并发送到浏览器。但在 SPA 的情况下，HTML 代码是根据视图动态生成的，使用了如 Handlebars 和 Underscores 等模板。

## 选择库或框架

框架的方法和函数通常比一个小型的库多得多，而且随着应用程序的增长，它们的工作可能会变得更加复杂。

我们还需要考虑其他重要点：

- **工具背后的社区**：通常，会有活跃的社区，并且很容易找到相关内容。然而，冷门的框架/库背后的社区较小，在线资源也较少。
- **更新频率**：过时的框架/库会有更多错误，缺乏频繁的更新会导致比你可能面对的问题更多。
- **学习曲线**：新工具的学习曲线越陡，你的项目开发时间就越长。在企业环境中，这可能会导致项目交付成本高昂。低廉的学习曲线可以让你专注于构建应用程序，而无需同时担心解决各种问题。
- **对其他库的支持**：这允许你在不破坏当前代码的情况下删除和添加内容。在这里，你可以轻松地将一个库或代码段替换为另一个而不影响应用程序。
- **依赖关系**：这显示了你需要在项目中包含多少个依赖文件以确保一切正常运行，以及所有依赖项如何消耗资源和传输带宽。成功的应用程序倾向于稳定增长，因此你可能需要增加依赖项。
- **模块化**：模块化的应用程序可以被轻松操作和逐步扩展。模块化系统具有更大的灵活性并能降低开发成本。强烈建议使用支持模块的框架，这不仅适用于 SPA，也适用于所有 Web 应用。

选择框架是你在应用程序规划阶段将做出的第一个也是最重要的选择。肯定的，你会选择最好的框架，或者至少是最流行的框架。

但如何选择呢？我们每天都有从简单库涌出的新选择，也有从小插件到复杂框架供我们选择；那么，如何决定呢？

## 理解单页应用

在这里，我们列了一个简单的列表来帮助你决策；在开始之前，你必须记住关于框架和库的以下概念：

- 库是代码片段，通常在同一个文件中。
- 框架更加健壮且具有结构性。

我们认为这是 SPA 与多页应用之间的主要区别：在每请求一个新页面时，我们都会产生一个新的请求。

一种名为 WebStorm，它提供了一个完整的开发环境；

你可以在 http://www.jetbrains.com/webstorm/ 下载试用版。

WebStorm 内置了工具，如 Terminal、RESTClient、Grunt.js 支持以及 Node 包管理器 (NPM)；这些工具触手可及，可以高效开发。

它还支持多种语言的语法高亮，如 HTML5, Node.js, Typescript, CoffeeScript, Dart, EJS, Handlebars, Mustache, Web Components, Stylus, Less, Sass, Jade 以及 JSLint/JSHint。

在第 7 版本之前，可以使用 AngularJS 插件来方便工作。

该插件提供了许多优势，如自动补全、在模块、控制器和指令之间轻松导航。

AngularJS 插件使用非常简单；只需执行以下步骤：

- 1. 导航到 File（文件） | Settings（设置） | Plugins（插件）。
- 2. 点击 Browse Repositories（浏览仓库）。
- 3. 选择 AngularJS。
- 4. 双击（或右键点击）并在出现提示时选择 Yes（是）。
- 5. 重启 WebStorm。

记住上述步骤适用于所有 8.0.2 版本。从 8.0.4 版本开始，该支持已内置在 WebStorm 中。要开始使用，你只需要在项目中包含 AngularJS 库即可。

另一个广泛使用的文本编辑器是 Sublime Text；它是一个非常流行且强大的编辑器，因为它轻量级且支持许多语言。你可以从 http://www.sublimetext.com/2 免费下载。

Sublime Text 编辑器有一个非常棒的插件可以配合 AngularJS 使用，与 WebStorm 非常相似。

你可以在 https://github.com/angular-ui/AngularJS-sublime-package/archive/master.zip 找到关于该插件的更多信息。

此外，也可以直接从 Sublime Package Control 安装。

## 理解单页应用 (SPA)

它提供了对核心 AngularJS 指令（如 `ng-repeat, ng-click`）以及你创建任何自定指令的自动补全。

> 你必须安装 Package Control 插件才能安装其他插件。你可以在 http://wbond.net/sublime_packages/package_control 找到更多关于 Package Control 的详情。

## AngularJS

AngularJS 是一个用于 JavaScript 的客户端 MVC/MVVM 框架。它采用的标准接近 MVVM 模式，并且非常健壮，非常适合 SPA。稍后我们将更深入地讨论我们在示例应用程序中使用的基本功能。

你可以在 http://docs.angular.org/tutorial 找到关于 AngularJS 的完整文档。

AngularJS 让你像拥有更智能的浏览器一样编写客户端 Web 应用。它允许你使用旧的 HTML（或 Haml, Jade 等）作为你的模板语言，并允许扩展 HTML 语法以清晰、简洁地表达你的应用程序组件。它通过双向数据绑定自动将 UI（视图）中的数据与 JavaScript 对象（模型）同步。此外，可以通过创建指令和自定义元素来扩展它。

## 调试工具

我们还有一个重要的工具来调试用 AngularJS 构建的 SPA，一个名为 Angular Batarang 的 Chrome 扩展，你可以在 https://github.com/angular/angular-batarang 免费获取。

Batarang 为我们提供了一个类似 Chrome 的 Web 检查器。安装后，你可以按 F12 或在屏幕上点击右键并选择最后一个链接 **Inspect element**（检查元素）来激活它。

Batarang 扩展有五个标签页：**Model（模型）,Performance（性能）,Dependencies（依赖）,Options（选项）和 Help（帮助）**，为调试你的应用程序提供了完整的环境。

以下是 Batarang 面板截图：

| Elements | Resources | Network | Timeline | Profiles | Audits | Console | Angular/ Emiter | PageSpeed |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Models | Performance | Dependencies | Options | Help | [x] Enable | | | |

为了开始使用 Batarang，你需要点击“enable”（启用）复选框。这将导致应用程序标签页刷新，Batarang 开始收集有关请求的性能和调试信息。

Batarang 有五个标签页：Model, Performance, Dependencies, Options 和 Help。

### Models

Firefox 浏览器的替代方案名为 AngScope。当你在 AngularJS 项目中寻找 Firefox 扩展时，检查 $scope 非常有用。

你可以在 https://addons.mozilla.org/pt-BR/firefox/addon/angscope-simple-angularjs-s/ 找到或下载它。

## 生成器和任务管理器

如今，开发一个 Web 应用程序是一项非常辛苦的任务。为此，需要大量的设置、定义的目录结构、一些框架和样板，以及用于预处理器的编译器（如 Less, Sass, CoffeeScript 等）。

## 理解单页应用

你可能会在项目的初始配置上花费大量时间。你肯定会在每个新项目中重复这些操作。

以下是每个新应用的一些常见步骤：

- 1. 构建脚手架文件夹。
- 2. 下载一些库。
- 3. 下载一些模板引擎。
- 4. 下载一些框架。
- 5. 配置测试环境。
- 6. 创建本地 Web 服务器在开发期间提供内容。
- 7. 文件压缩合并。

在思考这些琐碎任务的解决方案后，出现了一个名为 Yeoman 的工具。这是一个代码生成器，除了 Grunt 任务管理器和 Bower，它促进了另一种开发 Web 应用的方式。

这三个工具有一个共同点：Node.js 和 NPM。

让我们查看更多关于这些工具的细节。

## Yeoman

Yeoman 是一个开源项目，它通过命令行提供程序（是的，Windows 上的命令提示符/DOS 以及 Linux/OSX 终端），它是 Node.js 世界的 Web 开发环境平台，包含一组库和生成器。

此外，针对市场上的主流框架（如 Angular, Ember 和 Backbone）有大量的 Web 生成器。它有一个官方仓库，可以在 http://yeoman.io/generators/official.html 找到，此外还有社区提供的生成器仓库。

Yeoman 是一个建议已建立的工作流的工具，可以整合到你的项目中。安装非常简单，只需打开终端窗口并输入以下命令：

```
npm install -g yo
```

> 你需要在你的机器上安装 Node.js。Grunt 和 Bower 也会被安装。

## Bower

Bower 是 Web 的依赖管理器，但专门针对前端包。其理念很简单：你在项目根目录的 bower.json 文件中列出 JavaScript 示例依赖（AngularJS, Pure CSS, 响应式样板），通过这种方式你可以通过命令行控制这些包的安装/升级。

在系统中全局安装 Bower 非常简单；只需输入命令：

```
npm install -g bower
```

如果你不是系统管理员且正在使用 Linux 或 Mac OS，不要忘记使用 sudo 命令。

你可以在 http://bower.io/ 找到更多关于 Bower 的信息。

如果你已经安装了 Yeoman，就不需要安装 Bower 或 Grunt。

另一个配置是放在根目录的 .bower 文件。在这里，我们可以设置 Bower 包的文件夹名称和目标：

```
{
  "directory": "public/lib"
}
```

如果你不这样做，Bower 将将依赖安装在根目录下的 bower_components 文件夹中。

## Grunt

Grunt 是一个完全使用 JavaScript 自动化构建任务的工具。如果你遵循性能最佳实践，你应该考虑压缩 CSS 和 JavaScript 文件以减少请求数量。你还可以使用预处理器生成 CSS，如 Less 和 Sass，甚至为你的图像制作 CSS 雪碧图。

验证工具如 JSLint 可以检查 JavaScript 文件的错误，CSSLint 用于 CSS 的一致性，以及之前提到的许多其他操作。

如果你想自动化整个过程，单独使用所有这些工具是疯狂的。这就是为什么 Grunt.js 对任何 Web 项目都是非常有用且必不可少的。

## 理解单页应用 (Single Page Application)

若要在你的机器上安装 Grunt，只需在终端窗口中输入以下命令：

```
npm install grunt-cli
```

虽然这三个工具代表了快速 Web 开发环境的必要三剑客，但并非强制性的。你可以像前面解释的那样逐个安装所有工具，或者通常使用 Yeoman 安装。

## SPA 目录结构

主流框架和库对于如何实现 MVC 架构、声明式绑定等内容有许多共识。你的选择将深远地影响你的架构。

某些框架建议遵循特定的目录结构，但另一些框架则更加灵活。

我们将在接下来的章节中使用一个模板项目（boilerplate）来构建我们的 API，并讨论更多关于服务器结构和代码组织的内容；我们应该始终考虑应用程序的可维护性和扩展性。现在，让我们来看一个所有 MVC 模式中非常常见的的基础结构示例：

一个简单的基础 SPA 结构包含以下内容：

- Basic-folder-example [SPA]: 此文件夹是应用程序的根目录，包含我们的一个主文件 index.html。
- CSS: 此文件夹包含所有的样式表。
- images: 此文件夹包含所有图片。
- js: 包含所有的子文件夹和一个名为 `app.js` 的文件（我们的启动文件）。
- controllers 文件夹: 包含所有的控制器文件，但根据我们使用的库或框架，我们可以将其命名为 Collections 或 ViewModels。
- models: 此文件夹包含所有的模型文件。
- views: 包含所有的视图文件（仅包含数据，此处 HTML 渲染）。
- libs: 包含所有的第三方库，如 jQuery、Handlebars 和 Knockout。
- templates: 此文件夹包含所有的脚本模板，如 Handlebars、Underscore。注意，此文件夹包含了我们在应用程序中使用的所有模板。

注意，我们没有用于处理路由（routes）的文件夹，但对于基础应用程序，我们可以将路由逻辑放在 `app.js` 或 `server.js` 文件中。

> 在 Node.js 应用程序中，初始化文件通常称为 `app.js` 或 `server.js`，并且始终位于应用程序的根目录下。

尽管这是一个非常基础的结构，但对于理解文件夹命名的基础知识已经足够了。当然，随着事情变得复杂，我们需要重新评估这个结构（可能包含用于 Sass 或 Less 文件的文件夹，并添加其他内容）。然而，在本书的过程中，我们将看到一些替代方案。

## 核心在于 JavaScript

如前所述，所有的 SPA 都是用 JavaScript 开发的。当然，如果你不注意代码组织，在大量使用 JavaScript 的地方你很容易遇到麻烦。

## 理解单页应用 (Single Page Application)

我们建议你使用一些验证工具，如 JSLINT 和 JSHINT，以及用于 JSON 文件的验证工具 JSONLint。以下是这些验证工具的链接：

- JSLint: http://www.jslint.com/
- JSHint: http://www.jshint.com/
- JSONLint: http://jsonlint.com/

LINT 和 HINT 之间的主要区别在于 LINT 会验证缩进，而 HINT 不会。

## HTML、CSS 与响应式 Web

现在我们已经看到了关于简化 MVVM/MV 客户端开发工具的总体概览，让我们来看看两个将帮助我们与 HTML 和 CSS 交互的工具。

由于本书的目标不是成为界面设计的绝对指南，我们引入了一个简单的库，正如其名称所表明的，仅使用 HTML和 CSS 构建：Pure CSS。

## Pure CSS

该工具为我们提供了一个完整的用户界面，包含表单、表格、菜单、按钮以及我们构建健壮界面所需的其他所有组件。这里的重点是，它可以在没有 JavaScript 行为的情况下构建界面组件，并且可以从 purecss.io 免费下载。

> Pure 小巧得惊人。整个模块集经过压缩和 压缩后总计只有 4.5 KB。考虑到移动设备的设计，对我们来说保持较小的字体至关重要，每一行 CSS 都经过了仔细的考虑（来源：http://purecss.io/）。

这里的关键点是，尽管它的目标是完整且响应式的设计，我们可以以模块化的方式使用它，而无需依赖你的响应式网格系统，尽管它在应用程中非常有用，但在我们的示例中并不是必须的。

考虑到这一点，我们选择了另一个名为 Responsive boilerplate 的响应式网格系统；它非常简单用，只有三个主类和十二列。也可以从 http://www.responsiveboilerplate.com 免费下载。

Responsive boilerplate 是一个轻量级（1.5 KB）跨浏览器网格系统，优雅且极简，仅由三个主类和 12 列组成。它是以移动优先为设计的，适合任何屏幕尺寸，并预装了一些针对移动设备的额外 CSS 辅助工具。

它还有一系列针对 Sublime Text 编辑器的片段（snippets），可以从 https://github.com/neweaonweb/ResponsiveBoilerplateSnippets 下载。

它也可以通过 Sublime Text  Package Control 简单安装。该包非常完整，并使我们的开发过程变得非常快，如下截图所示：

| Snippet: Responsive Boilerplate Container | Rbcontainer.tab |
| Snippet: Responsive Boilerplate Col1 | Rbcol1.tab |
| Snippet: Responsive Boilerplate Col10 | Rbcol10.tab |
| Snippet: Responsive Boilerplate Col11 | Rbcol11.tab |
| Snippet: Responsive Boilerplate Col2 | Rbcol2.tab |
| Snippet: Responsive Boilerplate Col3 | Rbcol3.tab |
| Snippet: Responsive Boilerplate Col4 | Rbcol4.tab |
| Snippet: Responsive Boilerplate Col5 | Rbcol5.tab |
| Snippet: Responsive Boilerplate Col6 | Rbcol6.tab |
| Snippet: Responsive Boilerplate Col7 | Rbcol7.tab |
| Snippet: Responsive Boilerplate Col8 | Rbcol8.tab |
| Snippet: Responsive Boilerplate Col9 | Rbcol9.tab |
| Snippet: Responsive Boilerplate Content | Rbcontent.tab |
| Snippet: Responsive Boilerplate Navigation | Rbinav.tab |
| Snippet: Responsive Boilerplate Columns | Rbcolumns.tab |

我们可以使用 Bower 安装 Pure CSS 和 Responsive Boilerplate。这非常简单，只需在终端中输入以下命令：

```
bower install responsiveboilerplate
bower install purecss
```

我们将在接下来的章节中实践这些内容。

还有系列由社区提供的用于开发 SPA 的模板，以及微软的 Visual Studio 2012 可以从 http://www.asp.net/single-page-application/overview/ 免费下载。

> 除了 Visual Studio 和 WebStorm IDE 外，本中提到的所有工具都是开源的并由社区维护。你应该选择对你的开发有用且高效的工具。

## 总结

正如我们所见，单页应用程序的开发可能非常复杂，并且有许多资源可以使用，从简单的文本编辑器到 IDE WebStorm 和 Visual Studio。

在所有的 SPA 中，从数据库到用户界面的数据传输都是通过常见的 restful API 使用 JSON 格式完成的。下一章节将通过 MongoDB 和 Express 框架深入探讨 RESTful 应用。我们还将检查 Node 的一些核心概念，如事件循环和回调。

## 深入学习 Node.js 和 MongoDB

内置的异步 I/O、单线程甚至多线程、实时应用、套接字和 HTTP 连接使得 Node.js 成为创建运行 JavaScript Web 服务器的最强大工具。

MongoDB 是敏捷、可扩展、文档化无模式且高性能的，这使其成为最流行的 NoSQL 数据库之一。Node.js 和 MongoDB 配合 Express 框架释放了高性能 Web 应用的能量，Express 是一个支持模板引擎、路由和闪存信息的轻量级 Web 框架；它类似于 Ruby 的 Sinatra。接下来，我们将看到这些工具的一些关键概念。

本章将涵盖：

- Node 服务器、NPM 和中间件
- 事件驱动开发和事件循环
- 使用 require() 和模块
- Express Web 框架
- MongoDB 和终端
- 使用 Mongoose 进行 MongoDB 连接
- Mongoose 模式和模型

# Node 服务器、NPM 与中间件

Node 是一个用 JavaScript 构建的 Web 服务器，Node.js 的基本提案是构建高性能且可扩展的 Web 应用程序，这到底意味着什么？

在其他编程语言（如 Java、PHP 和 .NET）中，每个连接都可能在服务器上启动一个新线程，并且通常会伴随着 2 MB 的内存。在拥有 8 GB 内存的服务器上，这决定了最大并发连接约为 4,000 个用户。现在，想象一下你的应用程序正在增长，每天接收到的点击越来越多；你可能需要更多的服务器，甚至需要投入更多的硬件。这就是整个部 Web 应用程序架构的瓶颈，即服务器能够处理并保持稳定的最大并发 I/O 连接数。Node.js 通过改变连接到服务器的方式来解决这个问题。它不是为每个连接启动新线程，而是创建一个不需要随随内存块的进程。它不会直接对 I/O 进行 阻塞式调用。

Node 服务器可以支持成上万计的并发连接。它没有为每个连接分配一个线程，而是每个连接使用一个进程，只为每个连接创建所需的内存。它通过提供高扩展性的服务器实现了这一目标。

实际上，Node 改变了服务器的格局，系统的瓶颈从最大连接数变成了系统的流量能力。它还包含一个强大的包管理器称为 NPM (Node Package Manager)；虽然可以安装和更新包，但你也可以创建自己的包并将其发布到网上供整个社区使用。值得注意的是，许多第三方工具（如 Grunt、Bower 和 Yeoman 等）都使用 Node 来安装包。

NPM 是一个命令行实用，与 Node.js 的开源项目仓库进行交互；它可以安装模块并管理依赖关系和版本。

NPM 仓库拥有超过 76,000 个包，所有这些都是开源库，每天都有新的加入。这些应用程序可以通过 NPM 的搜索门户找到。你可以在官方仓库 [NPM Registry](https://www.npmjs.org/) 搜索并发现许多包。你可以在 http://nodejs.org/ 了解更多关于 Node.js 的信息。

NPM 的另一个重要用途是安装其模块和依赖项的能力。当你有一个包含名为 `package.json` 文件的 Node 项目时，你可以在项目的根目录中运行 `npm install` 命令，NPM 将安装 `package.json` 中列出的所有依赖项。

此外，`npm init` 命令通过分步配置启动你的项目配置，从而从零创建一个 `package.json` 文件。

最常用的命令是：

- npm install module_name: 在项目中安装一个模块
- npm install module_name-save: 安装模块并将其添加到 package.json 的依赖列表中
- npm list: 列出项目中的所有模块
- npm list -g: 列出所有全局模块
- npm remove module_name: 卸载一个模块
- module_name update: 更新 NPM 的当前版本
- npm adduser username: 在 NPM 仓库中创建一个用户
- npm whoami: 显示你在 NPM 仓库上的公共个人资料详情
- npm publish: 在 NPM 仓库上发布你的模块

Node 的另一个关键部分被称为中间件。我们通常将中间件定义为桥接代码段，所有的流都会通过这些代码段。在 Node 环境中，这非常常见。我们有很多中间件，如 connect、body-parser（处理 JSON 非常有用）、cookie parser 等等。这些都是 Express (v4) Web 框架的独立模块，我们将在书的后后部分看到更多关于它们的内容。

# 事件驱动开发与事件循环

事件驱动开发源于事件驱动编程，换句话说，在面向对象编程范式之外，基于事件的编程是指在事件触发后触发应用程序流的能力。

JavaScript 是一种事件驱动编程的绝佳语言；它允许匿名函数和闭包，更重要的是它的语法与其他编程语言非常相似。当事件发生时调用的回调函数可以写在捕获事件的同一个地方。因此，代码编写容易，维护也容易。

# 深入研究 Node.js 和 MongoDB

Node.js 中的几乎所有内容都使用回调。Node 回调是在异步模式下实现的函数。通常，回调函数是使用函数指针作为参数传递给另一个函数。例如，它告诉一个函数执行某些任务，并在完成该任务后执行另一个任务。

# 事件循环

掌握 Node.js 的另一个重要点是事件循环。任何熟悉 jQuery 的开发者都处理过回调函数，这些函数通常在用户执行某些任务后触发，例如点击折叠组件、幻灯片甚至是简单的按钮。然而，在 Node.js 中，事件循环在应用程序启动时开始。函数具有指向其他函数的回调，事件循环在最后一个回调执行时结束，如图所示：

事件循环始终在那里，并持续检查函数是否显式完成；否则它会保持程序运行并保持操作异步。让我们来看非常简单且常见的示例来创建一个 HTTP 服务器：

```
var http = require('http');
http.createServer(function (req, res) {
  res.write(200, {'Content-Type': 'text/plain'});
  res.end('Hello World\n');
}).listen(3000, "127.0.0.1");
console.log('Server running at http://127.0.0.1:3000/');
```

注意，我们的 HTTP 服务器为请求事件附加了一个回调。该回调作为参数传递给 `createServer`。

Node.js 从上到下运行代码；由于我们附加了一些监听器，Node.js 不会退出，而是等待事件触发。当一个 HTTP 请发送到服务器时，Node.js 会进入请求事件，生成附加到该事件的回调，以便按顺序运行。

在上一个示例中，我们只有一个回调，即作为参数传递给 `createServer` 的匿名函数。但在实际应用中，我们可以有许多函数。

# 使用 require() 和模坂

Node.js 是 JavaScript 的运行时规范。内联函数 `require()` 是在单独文件中包含现有模块的最简单方法。

## require() 函数

`require()` 的基本行为是读取 JavaScript 文件、解释脚本，然后在 Windows 上运行它，解释 `exports` 对象的内容。以下代码是一个用于理解它的示例；复制代码并粘贴到新文件中：

```javascript
console.log("requireExample");
```

```javascript
varExample = function () {
  console.log("requireExample");
}
```

```javascript
exports.greeting = "Hello Node";

exports.sayHi = function () {
  console.log(exports.greeting);
}
```

我们可以这样测试我们的模块：

```
> test = require('./example.js')
> greetings: 'Hello Node',
> sayHi: [Function]
> test.sayHi()

Hello Node
undefined
```

现在，让我们如何使用 `module.exports` 为导出分配函数或新对象；复制以下代码并保存为 `example-module.js`：

```javascript
module.exports = function () {
  console.log("Hello Node from module.exports")
}
```

打开 REPL 并输入：

require('./example-module.js')

这一次，当使用 `require` 导入模块时，它首先解释（执行）代码，导致模块导入并调用自身。

# 深入研究 Node.js 和 MongoDB

在这里，你可以看到模块已成功导入，并且说明了函数已导入。它打印示例并返回 `exports` 对象的内容，该对象包含了赋值给 `exports` 的属性。

Read-Eval-Print Loop (REPL) 是一个简单的交互式程序，它首先读取程序的短语或部分，然后评估（或运行）它，最后打印结果。

# 第 2 章

最后，`require` 返回分配给 exports 的函数，生成如下输出：

```javascript
require('./example-module.js')

```

Hello Node from module.exports

[Function]

```

最后一行 `[Function]` 确认了 `require('./example-module.js')` 的返回值是一个函数，而 `Hello from Node module.exports` 消息确认了代码在返回此处之前已经过解释。重要的一点是，代码只在第一次导入时被解释；如果你导入了多次，`require` 函数将重新导出已妥善保存在缓存中的对象。

另一个需要记住点是关于 `require` 获取文件的方式。如果文件以 `./` 开头，则被认为相对于调用 `require` 的文件的相对路径。如果文件以 `/` 开头，则被认为属于绝对地址。文件扩展名不是必须的；你可以这样声明依赖：`var express = require ('express');` Node.js 会将其解释为 express。

如果提供的文件名是目录名，函数将首先在目录中的一个名为 `package.json` 的文件中进行搜索，然后加载 `main` 属性中引用的文件。否则，函数将在模块文件夹中查找名为 `index.js` 的文件。

## Node 模块

Node 拥有一个简单的模块加载系统。模块的使用允许你在应用程序中包含其他 JavaScript 文件，正如我们在使用 `require()` 时看到的那样。模块对于在 Node 上构建应用非常重要，因为它们允许你包含外部库（例如数据库访问库、身份验证库等），并帮助将代码组织成职责有限的独立部分。

> 下载示例代码：你可以从 http://www.packpub.com 账户下载你购买的所有 Pack Publishing 书籍的示例代码文件。如果你在其他地方购买了本书，可以访问 http://www.packpub.com/support 并注册，以便将文件通过电子邮件发送给你。
> 此外，你还可以在 GitHub 上查看书籍代码仓库：https://github.com/nwaeweb/conference-api

## 深入探讨 Node.js 和 MongoDB

Node 采用的标准的 JavaScript 模块的最简单解决方案之一是带有细微差异的 CommonJS 标准。CommonJS 提供了一等模块，其重要性与一等函数相同。它认为，如果一个东西在编程语言中可以在运行时构建、作为参数传递、赋值给变量或作为函数的结果返回，那么它就是一种一等对象。重要的是，`exports` 是 `module.exports` 的引用；`exports` 仅用于添加对象。如果你想导出单个项目（例如构造函数），你将需要直接使用 `module.exports` 对象。让我们来看一个使用它的示例：

```javascript

// myConstructor.js example

function Constructor () {

}

```

```javascript

// On Node REPL

module.exports = MyConstructor;

```

在每个模块中，都有一个指向代表当前模块对象的引用。特别是 `module.exports` 可以通过全局 `exports` 模块访问。该模块并不是全局的，而是每个模块的本地对象。

`module.exports` 对象由系统和 Node `module` 导出变量创建，该变量指向它。你可以通过向导出变量添加内容来返回多个对象和函数，例如：`exports.sayHi = function () { console.log('Hello Node'); };`

Node 模块的另一个关键是每个模块作用域内的一组默认变量；以下是最常见的变量：

- filename：这是正在执行的代码的文件名。
- dirname：这是保存正在执行的脚本的目录名称。
- process：这是一个与当前运行进程关联的对象。此外，该对象拥有 `process.exit`、`process.cwd` 和 `process.uptime` 等方法。
- process.argv：这是一个包含命令行参数的数组。第一个元素是 node，第二个元素是 JavaScript 文件的文件名，接下来将是额外命令行的所有参数（如果它们被赋值的话）。
- process.stdin, process.stdout 和 process.stderr：这些流对应于当前进程的标准输入、标准输出和标准错误输出。
- process.env：这是一个包含当前进程用户环境变量的对象。
- require.main：当文件被 Node 直接执行时，`require.main` 被赋值给此模块。

关于所有 Node 的特殊性还有很多内容要写，但这超出了我们书的主范围；我们在这里展示的是我们理解的基础。

## Express – 服务器上的 Web 框架

Express 是 Node 上构建 Web 应用最常用且灵活的框架。它为我们提供了一套强大的功能来处理此类 SPA、RESTful API，当然还有 MEAN 栈。Express 框架对模板和渲染有完全支持，默认使用 Jade 引擎。它非常适合在服务器端渲染 HTML 的大型应用程序。

当然，我们还有其他选项，例如专门处理 RESTful API 的优秀微框架，但我们谈论的是 MEAN，我们只使用与缩写相关的技术，即 Express。

Jade 是一个专门为 Node 设计的模板引擎，受到 Ruby 和 Haml 的启发，具有基于规则的缩进，类似于 Sass 和 Python 语法。关于 Jade 的信息可以在 http://jade-lang.com/ 上找到。

使用 Express 的主要原因是 Node API 对于复杂应用来说不够健壮，路由管理和其他特性处理非常基础。Express 遵循良好的开发实践和非常难以构建的面向 RESTful 的架构。我们可以列出 Express 的一些优秀特性：

- 强大的路由管理
- 重定向辅助
- 可以使用任何视图引擎
- 准备好使用 RESTful
- 应用挂载
- 高性能
- 视图渲染
- 支持部分组件 (Partials)

## 深入探讨 Node.js 和 MongoDB

讨论模板引擎很重要，因为 Express 框架默认使用 Jade 并有它自己的语法，但可以使用其他引擎，如嵌入 JavaScript (EJS)，它可以直接渲染 HTML。由于我们的范围在构建 SPA 之外，而且我们在前端使用的工具已经有了自己的语法，因此我们不会深入探讨在服务器上运行的模板。

需要说明的是，Express 也是其他 Node 框架（如 Locomotive、Kraken 等许多框架）的基础。为了简单了解 Express 框架的使用，请看创建一个应用是多简单，如下代码所示：

```javascript

var express = require('express');

var app = express();

app.get('/', function(req, res) {

  res.send('Hello Express');

});

```

```javascript

app.listen(3000);

```

当然，一个应用程序将包含许多行代码，但在这里，可以看到使用 Express 创建应用是多么简单。只需几行代码，我们就可以生成一个在 Node 服务器上运行的带有 Hello Express 消息。

## MongoDB 和终端

MongoDB 也称为 NoSQL 数据库，是一种面向文档的数据库；这意味着所有数据都存储为 JSON 文件。

MongoDB 不像关系型数据库那样将数据存储在表和行中，而是使用键值格式存储这些数据，并使用二进制 JSON (BSON)；开发者可以轻松地映射到现代面向对象的语言，而无需复杂的 ORM 层。这种新的数据模型显著简化了编码，并提高了相关数据分组的性能。

MongoDB 不是关系型数据库的二维处理方法（即行和列）；它可以像现实世界中的对象那样复杂且独特地表示它们。想象一下在你的关系型数据库中，你必须为一条记录输入一个新属性；对于这一点，你模型中的更改应该应用到整个数据库。

## 关系型数据库与 NoSQL 数据库的比较

在 MongoDB 的情况下，你可以在需要的地方使用它，而不是在所有情况下都使用。在关系型模型中，通常会在相关表中创建一个新列，如下截图所示：

| 乐队 | 专辑 | 经典 |
| --- | --- | --- |
| ID | ID | ID |
| 名称 | Title | 曲目名 |
| 国家 | 曲目 | |
| 流派 | 长度 | |

## NoSQL 

| 乐队 |
| --- |
| ID |
| 名称 |
| 国家 |
| 流派 |
| 专辑 |
| Title |
| 曲目 |
| 长度 |
| 经典 |
| 曲目名 |

这里的基本思想是文档应该是自包含的，所有信息都在同一个地方。为什么呢？简单来说，MongoDB 不需要执行带有多个连接（joins）的查询，而是执行单个查询并返回整个文档。结果性能更高。MongoDB 是一种基于文档的 NoSQL 数据库，不支持事务和连接。

# 深入研究 Node.js 和 MongoDB

关系型数据库的另一个重要事实是，它们要求在插入数据之前定义模式（schemas）；而在 MongoDB 中，你不需要预定义的模式来插入数据。

你可以在 http://www.mongodb.com/nosql-explained 找到更多关于 NoSQL 优势的信息。

为了更好地理解，让我们来看 SQL 命令与 MongoDB 命令的对比。

| MongoDB | SQL |
|---|---|
| db.name.insert({A:1, B:2 }) | INSERT INTO NAME VALUES (A, B) |
| db.users.find() | SELECT * FROM users |
| db.bands.find({ name: "Metallica" }) | SELECT * FROM BANDS name = "Metallica" |
| db.bands.find().limit(5).skip(10) | SELECT * FROM BANDS LIMIT 5 SKIP 10 |

这里有一表说明了更多的差异：

| MongoDB 术语 | SQL 术语 |
|---|---|
| 数据库 (database) | 数据库 (database) |
|  (collection) | 表 (table) |
| 文档/BSON 文档 | 行 (row) |
| 字段 (field) | 列 (column) |
| 索引 (index) | 索引 (index) |
| 嵌入文档/链接 | 表连接 (table joins) |
| 主键是 is_id 字段 | 列或列组合作为主键 |
| 聚合管道 (aggregation pipeline) | 聚合：分组 (aggregation: group by) |

## mongo shell

现在我们已经对 MongoDB 的强大和简单性有了初步了解，让我们学习如何使用终端进行交互。本书假设你已经在你的机器上安装了 MongoDB。直接进入终端并输入 `mongo`。

一旦你启动 MongoDB shell，你会看到一条类似下面的消息：

```

MongoDB shell version: 2.4.6

connecting to: test

>

```

由于我们尚未指定任何数据库，请注意 shell 会在一个名为名为 test 的 MongoDB 数据库中启动。你可以使用它运行这些基础示例；但是，我们将使用以下步骤创建一个新数据库，以便熟悉一些 MongoDB shell 命令：

- 1. 在终端中输入 `use exampledb`，你将获得以下消息：

```

> use exampledb

switched to db exampledb

>

```

此消息表示 MongoDB 创建并切换到了名为 exampledb 的新数据库。注意，除了创建新数据库的关键字外，没有使用额外的命令，因此创建并从 test 切换到 exampledb 只需要命令。

- 2. 现在，我们可以使用简单的 JSON 格式通过 `insert` 命令轻松创建集合：

```js

db.bands.insert({

  name: "Metallica",

  album: "Master of Puppets",

  tracks: 9,

  year: "1996"

})

```

MongoDB 中的所有命令都极其简单且容易记忆；此外，当出现任何问题时，我们有 `help()` 命令，可以通过它快速进行搜索。

- 3. 我们可以将此应用在这些数据库和集合上，例如 `db.collection-name.help()`。

# 深入研究 Node.js 和 MongoDB

下面的截图说明了当我们对 speakers 集合应用 `help()` 命令时的输出：

```

db.speakers.find({}).count()

db.speakers.find({}).limit()

db.speakers.find({}).skip()

db.speakers.find({}).sort()

db.speakers.update({}, $update: { ... }, $remove: { query: }, $set: { 'new': 'false' }})

db.speakers.findOneAndAndUpdate({}, $set: { object }) associated with collection

db.speakers.getPlanCache() get query plan cache associated with collection

db.speakers.getHelp({ initial: ... }) - reduce: { code: [ ... ] }

db.speakers.getIndexes()

db.speakers.aggregate(pipeline, optional_) - performs an aggregation on a collection, returns a cursor

db.speakers.removeCollection(name, _dropTarget) removes the collection

db.speakers.rename() returns the given name where the first parameter is the collection

db.speakers.stats({free: true}) - includes free space allocated to this collection

db.speakers.totalSize() - size in bytes of all indexes

```





当我们将这两段代码添加到数据库并执行应用程序时，我们看到 `save` 函数将提供一个新创建的文档；查看控制台：

```

{ __v: 0,

  name: 'Slayer',

  album: 'Show no Mercy',

  track: 10,

  year: 1984,

  _id: 8334012cb65dfgf003000022 }

}

```

MongoDB 中的集合（Collections）具有灵活的模式（schema）；这意味着集合不会对文档施加强制结构。在实践中，这意味着同一个集合中的文档不需要具有相同的字段集或结构，且文档中的公共字段可以携带不同类型的数据。

正如我们的示例所示，使用 Mongoose 映射我们的数据库标准了 schema 的文档。这确保了编译 schema 的模型实例将始终具有 schema 中指定的相同数据类型。

## 总结

我们结束了本章，其中包含了许多关于创建 Node 服务器和运行 Web 应用程序全过程的新信息。

我们涵盖了启动开发示例应用的核心主题，从我们的 Node 服务器、NPM，以及如何安装模块和依赖、使用 `require` 导入模块以及使用 `module.exports` 导出模块以便后续使用。我们看到 MongoDB 有一个 GUI 管理界面，并学习了一些在未来章节中对我们帮助命令行。

我们学习了 Express 框架的力量，通过它可以构建简单复杂的 Web 应用程序，并学习了如何使用 Mongoose 进行对象建模，为数据创建 schema 和模型。但如果你不理解这里所有的概念，不要担心；我们将在接下来的章节中进行详细讨论它们。

我们的旅程刚刚开始；在接下来的章节中，我们将看到另一组工具，并通过编写大量代码来开始构建我们的 API。在下一章中，我们将看到 API 是如何工作的、一些关于 RESTful 架构的介绍，以及如何使用 Yeoman 生成器开始开发。

## 结合 MongoDB 和 Node.js 的 API

本章将直接关注代码，以便我们获得必要的理解，为我们的 API 奠定坚实的基础。我们的主要目标是讨论使用 SPA 方法构建丰富 Web 应用程序的技术。

应用程序接口（API）是使能够构建应用程序的编程标准集合。对于使用应用程序的用户来说，它们的用法并不直观。API 是应用程序的引擎；是一个运行在这一切背后的接口。虽然你可能从应用程序或网站中受益，但你的 API 可以连接到多个系统和应用程序。通过 API，应用程序之间可以在没有用户干预的情况下通信。

我们将在本章中涵盖以下主题：

- API 的工作原理
- 模板（Boilerplates）和生成器
- 插件 API 概念
- 创建 `package.json` 文件
- 使用 `server.js` 的 Node 服务器
- 使用 Mongoose schema 的模型
- 定义 API 路由
- 在云端使用 MongoDB
- 使用 Postman 插入数据

## API的工作原理

API 通过不同代码之间的通信工作，从而定义接口上对象的特定行为。也就是说，API 将网站上的多个功能（如搜索、图片、验证等）连接起来，使其能够在其他应用程序中使用。

操作系统也有 API，它们的功能相同。例如，所有版本都有如 Web API、电话 API。当你运行一个涉及操作系统进程的程时，我们可能会与一个或多个 API 建立连接。为了澄清 API 的概念，我们将通过一些示例来展示它是如何工作的。在 Windows 上，它运行在使用系统在程序内显示相同功能的应用程序上。然后将行为关联到另一个应用程序中的给定时间。

另一个例子是你使用 SDK 构建移动应用程序。当你使用 GPS 时，你正在与 API 交互以便地图上显示用户位置；在这种情况下，就是 Google Maps API。

涉及到 Web API 时，功能可能更大。许多服务提供其代码，以便在其他网站上使用。也许最好的例子是 Facebook API。其他网站使用此服务，例如点赞、分享，甚至是身份验证。

> API 是一组基于 Web 访问软件应用程序的编程模式和指令。

所以，当你访问你的账户时，你可以登录。这是通过 API 实现的。使用它，软件开发者可以为他们的用户创建精美的页面。

## 模板（Boilerplates）和生成器（Generators）

在 MEAN 栈环境中，我们的生态系统是无限多样的，我们可以找到开始构建 API 的极佳替代方案。我们有从简单的模板到复杂的代码生成器，它们可以与其他工具配合，也可以单独使用。

模板通常是一组经过测试的代码，为主要目标（即创建 Web 项目的基础）提供基本结构。模板为我们节省了许多常见任务，如组装代码的基础结构和组织文件，模板已经有很多脚本可以使前端的工作变得更轻松。

让我们描述一些我们认为在使用 Express 框架、MongoDB 数据库、Node 服务器和 AngularJS 作为前端开发 API 的良好起点的替代方案。

为了完全理解这里涵盖的概念，可能需要对 JavaScript 有一些突出的知识。

## 结合 MongoDB 和 Node.js 的 API

本章将直接关注代码，以便我们获得必要的理解，为我们的 API 奠定坚实的基础。我们的主要目标是讨论使用 SPA 方法构建丰富 Web 应用程序的技术。

（注：此处部分内容与上方重复，已按指令要求跳过）

## 使用 MongoDB 和 Node.js 构建 API

当我们扩展单页应用（SPA）时，最常见的问题无疑是目录结构，以及我们如何使用 MVC/MVVM 管理所有的前端 JavaScript 文件和 HTML 模板。稍后，我们将看到处理大型应用的另一种替代方案；现在，让我们看看 MEANJS 采用的模块结构：

![](img/76faac513e4fd5843aeb56a44cada4c9_68_0.png)

注意，MEANJS 为 AngularJS 框架留下了更大的灵活性来处理前端应用的 MVC 方法，正如我们在 public 文件夹中看到的那样。此外，注意模块化方法；每个模块都有自己的结构，对控制器、服务、视图、配置和测试保持了一些某些约定。这对于团队开发非常有用，因此请保持所有结构的组织良好。这是一个完整的解决方案，利用了 `passport`、`swig`、`mongoose`、`karma` 等模块。

## Passport 模块

关于 Passport 模块必须说明几点：它可以被定义为一个简单、非侵入的认证模块。它是与 Node 配合使用的强大中间件；它非常灵活且模块化。它可以轻松适配到使用 Express 的应用程序中。

它拥有 140 多种可选认证方式并支持会话持久化；它非常轻量且实现极其简单。它为我们提供了认证、重定向和验证所需的所有结构，因此可以使用 Facebook、Twitter 等其他社交网络的用户名和密码。

以下是如何使用本地认证的简单示例：

```javascript

var Passport = require('passport');

LocalStrategy = require('passport-local').Strategy,

User = require('mongoose').model('User');

module.exports = function() {

  // 使用本地策略

  passport.use(new LocalStrategy({

    username: 'username',

    passwordField: 'password'

  },

  function(username, password, done) {

    User.findOne({

      username: username

    }),

    function(err, user) {

      if (err) {

        return done(err);

      }

      if (!user) {

        return done(null, false, {

          message: 'Unknown user'

        });

      }

      if (!user.authenticate(password)) {

        return done(null, false, {

          message: 'Invalid password'

        });

      }

      return done(null, user);

    }

  }));

});

```

这是使用带有 Passport 模块的 MEAN.JS 模板的登录页面示例截图：

![](img/76faac513e4fd5843aeb56a44cada4c9_70_0.png)

回到模板的主题；大多数大多数模板和生成器已经安装了 Passport 模块并准备好进行配置。此外，它还有一个代码生成器，可以与 Yeoman 配合，Yeoman 是另一个需要添加到你的工具箱中的必备前端工具。

> Yeoman 是最流行的现代 Web 应用脚手架代码生成器；它易于使用，并且有很多生成器，如 Backbone、Angular、Karma 和 Ember 等。更多信息可以访问 http://yeoman.io/。

## 生成器 (Generators)

生成器之于前端，就像 gem 之于 Ruby on Rails。我们可以使用可用的生成器为任何类型的应用程序创建基础。

# 第 3 章

这里是 Yeoman 生成器的控制台输出：

![](img/76faac513e4fd5843aeb56a44cada4c9_71_0.png)

开箱即用 Sass（带有 Compass）以及一些 AngularJS 推荐模块。

- 你想使用 Sass（带有 Compass）吗？否
- 你想包含 Twitter Bootstrap 吗？否
- 你想包含？angular-resource.js, angular-cookies.js, angular-sanitizer.js, router
- 你想使用 Mongoose 吗？否
- create app/styles/main.css
- create app/controllers/navbar.js
- create app/views/index.html
- create app/views/partials/main.html
- create app/views/navbar.html
- create app/views/db.html
- create bower.json
- create package.json
- create Gruntfile.js
- create images/yeoman.png
- create server.js
- create lib/shite.js
- create lib/controllers/api.js
- create lib/controllers/index.js
- create routes.js
- create test/server/api.js
- create lib/config/express.js
- create lib/config/config.js
- create lib/config/dev.js
- create lib/config/env/development.js

重要的是，要意识到我们可以在社区中通过生成器解决几乎所有问题。然而，如果你找不到你需要的生成器，你可以创建自己的并提供给整个社区使用，就像 Rails 社区对 RubyGems 所做的那样。

RubyGem，或简单称为 gem，是可重用 Ruby 文件的生成器，带有名称和版本（一个名为 gemspec 的文件）。

> 记住“不要重复自己”(DRY) 概念；始终尝试重用现有的代码块。不要发明轮子。

使用代码生成器的巨大优势之一是，许多生成器都是随取随用的。

## Express 生成器

另一个很好的选择是 Express 生成器，可以在 https://github.com/expressjs/generator 找到。

与 Rails 非常相似，我们可以看到 public、routes 和 views 文件夹的创建：

```bash

npm install

```

运行应用：
```bash

DEBUG=express ./bin/www

```

注意创建的 package.json 文件：

```json

{

  "name": "express-generator",

  "version": "0.0.1",

  "private": true,

  "scripts": {

    "start": "node /bin/www"

  },

  "dependencies": {

    "express": "4.2.0",

    "static-favicon": "1.0.0",

    "morgan": "1.0.0",

    "cookie-parser": "1.0.1",

    "body-parser": "1.0.0",

    "debug": "0.7.4",

    "jade": "1.3.0"

  }

}

```

这是一个构建 Web 应用的简单有效的 package.json。

## 演讲者 API

让我们直接构建示例 API。为了更真实，我们来写一个类似于敏捷方法中待办列表的用户故事。让我们了解通过 API 需要解决的问题。

## 用户故事

我们需要一个 Web 应用来管理会议的演讲者。主要任务是在 API 中存储以下演讲者信息：

* 姓名
* 公司
* 分类主题标题
* 描述
* 演讲者照片
* 演讲安排

现在，我们需要使用纯 JSON 格式的 API 添加、编辑和删除演讲者。这是一个简单的 CRUD 功能。

## 创建 package.json 文件

虽然现在还没有必要，但我们建议你安装 Webstorm IDE，因为我们将在整本书中使用它。

> 从现在开始，当我们提到终端时，指的是 Webstorm 集成终端，但你也可以通过选择的独立编辑器直接访问，Mac 和 Linux 使用终端， Windows 使用命令提示符。

## 初始化 JSON 文件

按照以下步骤初始化 JSON 文件：

 1. 创建空文件夹并命名为 conference-api，打开你的终端，并放置命令：

```bash

npm init

```

此命令将引导你创建一个 `package.json` 文件，该文件包含我们应用程序的基础配置。此外，该文件是应用程序的核心；我们可以通过它控制所有依赖的版本和其他重要信息，如作者、GitHub 仓库、开发依赖、许可证类型、测试命令等。

- 2. 几乎所有的命令都是引导你完成最终流程的问题，因此当我们完成时，将得到一个与此非常类似的 `package.json` 文件：

```

{

  "name": "conference-api",

  "version": "0.0.1",

  "description": "Sample Conference Web Application",

  "main": "server.js",

  "scripts": {

    "test": "test"

  },

  "keywords": [

    "api"

  ],

  "author": "your name here",

  "license": "MIT"

}

```

- 3. 现在，我们需要添加必要的依赖项，例如 Node ，这些模块将用于我们的项目中。你可以通过两种方式实现：要么直接通过终端（如我们在这里所做），要么通过编辑 `package.json` 文件。让我们先看看在终端中如何操作；从 Express 框架开始。在 `api` 文件夹中打开终端并输入以下命令：
npm install express@4.0.0 --save

此命令安装了 Express 模块（在此例中为 Express 版本4），并自动更新 `package.json` 文件并创建依赖，如我们所示：

```

{

  "name": "conference-api",

  "version": "0.0.1",

  "description": "Sample Conference Web Application",

  "main": "server.js",

  "scripts": {

    "test": "test"

  },

  "dependencies": {

    "express": "4.0.0"

  }

}

```

- 4. 现在，让我们直接在 `package.json` 中添加更多依赖项。在编辑器中打开文件并添加以下行：

```json

{

  "name": "conference-api",

  "version": "0.0.1",

  "description": "Sample Conference Web Application",

  "main": "server.js",

  "scripts": {

    "test": "test"

  },

  "keywords": [

    "api"

  ],

  "author": "your name here",

  "license": "MIT",

  "engines": {

    "node": "8.14",

    "npm": "6.1.4"

  },

  "dependencies": {

    "body-parser": "1.0.1",

    "express": "4.0.0",

    "method-override": "1.0.0",

    "mongoose": "3.6.1",

    "morgan": "1.0.0",

    "nodemon": "1.2.0"

  }

}

```

- 5. 打开终端并输入命令：
npm install

你可以通过两种方式安装依赖：要么直接安装到应用程序目录中，要么使用 `-g` 命令全局安装。这样，你将拥有可以在任何应用程序中使用的模块。在过程结束时，我们将拥有项目所需的所有 Node 模块；我们只需要再执行一个操作。

当你使用 Travis 或 Heroku 等服务部署应用程序时，设置好 Node 环境是非常重要的。

关于 Git 的更多信息可以在 http://git-scm.com/ 找到；不过，你可以使用任何版本控制工具或其他。我们推荐使用 Git，因为我们需要它将应用程序部署到云端，特别是部署在 Heroku 托管上。此时，我们的项目文件夹必须具有此处所示的结构：

| node_modules |
| body-parser |
| express |
| method-override |
| mongoose |
| morgan |
| nodemon |
| package.json |

我们必须指出一个名为 Nodemon 的重要模块。每当文件发生变化时，它会自动重启服务器；否则，你每次对文件进行更改都必须手动重启服务器，这在开发环境中非常有用，因为它不断更新我们的文件。

## 带有 server.js 的 Node 服务器

形成此结构后，我们将开始创建服务器本身，即创建一个主 JavaScript 文件。最常用的名称是 `server.js`，但使用 `app.js` 名称也十分常见，特别是在旧版本中。

将此文件添加到项目的根目录，并从基础服务器设置开始。配置服务器有很多方法，你可能会找到最适合自己的方法。由于我们仍处于初始阶段，我们只保留基础内容。

打开你的编辑器并输入以下代码：

```javascript

// 到到我们服务器上安装的模块

var express = require('express');

var bodyParser = require('body-parser');

// 启动 Express 框架

var app = express();

// 配置 app

app.use(bodyParser());

// 应用运行的位置

var port = process.env.PORT || 8080;

// 导入 Mongoose

var mongoose = require('mongoose');

// 连接到你的数据库

// 你可以使用你自己的 MongoDB 安装在：mongodb://127.0.0.1/datename

mongoose.connect('mongodb://username:password@kahana.mongodb.com:10073/node-api');

// 启动 Node 服务器

app.listen(port);

console.log('Magic happens on port ' + port);

```

# 第3 章

在本地执行的 MongoDB 路由。在云端执行的 MongoDB 路由。我们将使用  的 MongoDB 路由。

```javascript

app.listen(port);

console.log('Magic happens on port ' + port);

## 定义 API 路由

配置 API 路由：



- 1. 让我们定义路由以及针对所有请求的通用消息：

```javascript
var Speaker = require('./server/models/speaker');

// 定义我们 API 的路由

// 启动路由器
var router = express.Router();

// 用于所有路由和请求的简单中间件
router.use(function(req, res, next) {
  // 在控制台上给出一些信息
  console.log('An action was performed by the server.');
})
```

## 使用 Mongoose 的模型

现在，我们使用 Mongoose 模式来创建模型。

```javascript
// 导入 Mongoose 模块
var mongoose = require('mongoose');
var Schema = mongoose.Schema;

// 设置 Speaker 模式
var SpeakerSchema = new Schema({
  name: {
    type: String,
    default: ''
  },
  company: {
    type: String,
    default: ''
  },
  title: {
    type: String,
    default: ''
  },
  description: {
    type: String,
    default: ''
  },
  picture: {
    type: String,
    default: ''
  },
  schedule: {
    type: Date,
    default: Date.now
  }
});

module.exports = mongoose.model('Speaker', SpeakerSchema);
```

注意第一行，我们添加了 Mongoose 模块。我们的模式非常简单；在左侧是属性名，在右侧是数据类型。我们也设置了默认值，但如果你愿意，可以设置不同的值。

下一步是保存项目文件夹。为此，让我们创建一个名为 `server` 的新目录；然后在里面创建一个名为 `models` 的文件夹并将文件保存为 `speaker.js`。此时，我们的文件夹如下：

![](76ac513e4fd5843eb56a444c9_79_0)

README.md 文件用于 GitHub；由于我们使用 Git 版本控制，我们将文件托管在 GitHub 上。

## API 路由

我们 API 最重要的方面之一是用于创建、读取、更新和删除说话者的路由。我们的路由基于访问 API 时使用的 HTTP 动词，如下所示：

- 创建记录，使用 POST 方法

- 读取记录，使用 GET 方法

- 更新记录，使用 PUT 方法

- 删除记录，使用 DELETE 方法

因此，我们的路由如下：

| 路由 | 动词和操作 |
|---|---|
| /api/speakers | GET 获取说话者记录 |
| /api/speakers/ | POST 插入说话者记录 |
| /api/speakers/:speaker_id | GET 获取单条记录 |
| /api/speakers/:speaker_id | PUT 更新单条记录 |
| /api/speakers/:speaker_id | DELETE 删除单条记录 |

```javascript
// 使用 next() 函数非常重要，没有它，
// 路由将在此停止。
next();
```

```javascript
// 当通过浏览器访问 API 文件夹时的默认消息
router.get('/', function(req, res) {
  // 发送一些 Hello there 消息
  res.json({ message: 'Hello SPA, the API is working!' });
});
```

2. 现在，让我们在 HTTP 动词为 POST 时向路由添加演讲者（speakers）：

```javascript
// 访问 speakers 
router.route('/speakers')
  // 当传递的方法为 POST 时，创建一个演讲者
  .post(function(req, res) {
    // 创建 Speaker 模型的一个新实例
    var speaker = new Speaker();

    // 设置演讲者的属性（来自请务）
    speaker.name = req.body.name;
    speaker.company = req.body.company;
    speaker.title = req.body.title;
    speaker.description = req.body.description;
    speaker.picture = req.body.picture;
    speaker.schedule = req.body.schedule;

    // 保存接收到的数据
    speaker.save(function(err) {
      if (err) {
        res.send(err);
      }
      // 发送一些成功消息
      res.json({ message: 'speaker successfully created!' });
    });
  });
```

3. 对于 HTTP GET 方法，我们需要这个：

```javascript
// 当传递的方法为 GET 时，获取所有演讲者
.get(function(req, res) {
  Speaker.find(function(err, speakers) {
    if (err) {
      res.send(err);
    }
    res.json(speakers);
  });
});
```

# 使用 MongoDB 和 Node.js 的 API

注意，在 res.json() 函数中，我们将所有对象 对象作为回答发送。现在，将在接下来的步骤中查看不同路由的使用：

- 1. 要检索单条记录，我们需要传递 speaker_id，如我们之前的表所示，因此让我们构建这个函数：

```javascript
// 通过 id 访问 speaker 路由
router.route('/speakers/:speaker_id')
  // 通过 id 获取演讲者
  .get(function(req, res) {
    Speaker.findById(req.params.speaker_id, function(err, speaker) {
      if (err)
        res.send(err);
      res.json(speaker);
    });
  });
```

- 2. 要更新特定记录，我们使用 PUT HTTP 动词并插入函数：

```javascript
// 通过 id 更新演讲者
.put(function(req, res) {
  Speaker.findById(req.params.speaker_id, function(err, speaker) {
    if (err) {
      res.send(err);
    }
    // 设置演讲者的属性（来自请求）
    speaker.name = req.body.name;
    speaker.company = req.body.company;
    speaker.title = req.body.title;
    speaker.description = req.body.description;
    speaker.picture = req.body.picture;
    speaker.schedule = req.body.schedule;

    // 保存接收到的数据
    speaker.save(function(err) {
      if (err) {
        res.send(err);
      }
      // 发送一些成功消息
      res.json({ message: 'speaker successfully updated!' });
    });
  });
});
```

- 3. 通过其 id 删除特定记录：

```javascript
// 通过 id 删除演讲者
.delete(function(req, res) {
  Speaker.remove({
    _id: req.params.speaker_id
  }, function(err, speaker) {
    if (err) {
      res.send(err);
    }
    // 发送一些成功消息
    res.json({ message: 'speaker successfully deleted!' });
  });
});
```

- 4. 最后，在我们的 server.js 文件中注册路由：

```javascript
// 注册路由
app.use('/api', router);
```

配置基础 CRUD 路由的所有必要工作已经完成，我们准备好运行服务器并开始创建和更新数据库。

在这里打开一个小括号，通过一个快速的分步骤过程介绍另一个使用云端 MongoDB 创建数据库的工具。

有许多公司提供此类服务，但我们在这里不会讨论各自的优点；你可以根据自己的喜好进行选择。我们选择了 Compose（原名为 MongoHQ），它有一个用于开发的免费沙盒，这对于我们的示例已经足够。

# 在云端使用 MongoDB

今天，我们有许多选项来处理 MongoDB，从内部服务到提供平台即服务 (PaaS) 和软件即服务 (SaaS) 的托管公司。

# 使用 MongoDB 和 Node.js 的 API

我们将介绍一种名为数据库即服务 (DaaS) 的解决方案，它为高度可的 Web 提供数据库服务。

以下是使用云服务开始使用 MongoDB 实例的简单步骤：

- 1. 访问 https://www.compose.io/
- 2. 创建你的免费账户。
- 3. 在仪表板面板上，点击 add Database（添加数据库）。
- 4. 在右侧选择 Sandbox Database（沙盒数据库）。
- 5. 将你的数据库命名为 node-api。
- 6. 为你的数据库添加用户。
- 7. 返回你的数据库，点击 admin（管理）。
- 8. 复制连接字符串如：
- 9. mongodb://<user>:<password>@skahana.monohq.com:10073/node-api。

```text
mongodb://<user>:<password>@skahana.monohq.com:10073/node-api
```

让我们使用以下步骤编辑 server.js 文件：

1. 将你的连接字符串放入 Mongoose.connect()。
2. 打开你的终端并输入命令：
```bash
nodemon server.js
```
3. 打开你的浏览器并放置 http://localhost:8080/api。
4. 你将在浏览器中看到类似这样的消息：
```bash
nodemon server.js
> {Hello SPA, the API is working!}
```
记得我们在注册路由时在 server.js 中定义了 api 文件夹：
```javascript
app.use('/api', router);
```
6. 但如果你尝试访 http://localhost:8080/api/speakers，你必须有类似这样的：[]
这是一个空数组，因为我们还没有向 MongoDB 中输入任何数据。

## 使用 Postman 插入数据

为了在创建前端界面之前解决空数据库的问题，让我们使用 Chrome Postman 添加一些数据。顺便说一下，这是一个处理 RESTful API 非常有用的界面。

由于我们已经知道数据库是空的，我们的第一个任务是插入一条记录。要做到这一点，请执行以下步骤：

1. 打开 Postman 并使用 x-www-form-urlencoded 选项输入 http://localhost:8080/api/speakers 并添加我们模型的属性：
```javascript
var speakerSchema = new Schema({
  name: { type: String, default: '' },
  company: { type: String, default: '' },
  title: { type: String, default: '' },
  description: { type: String, default: '' },
  picture: { type: String, default: '' },
  schedule: { type: String, default: '' },
  createdAt: { type: Date, default: Date.now }
});
```
2. 现在，点击底部的蓝色按钮发送请求。
3. 如果一切正常，你应该会在屏幕底部看到消息：“speaker successfully created!”。
4. 现在，让我们再次尝试 http://localhost:8080/api/speakers。
5. 现在，我们得到了这样的 JSON 文件，而不是空数组：
```json
{
  "_id": "53a8ffd2cd3479000",
  "_v": 0,
  "_created": "2014-06-20T20:31:384Z",
  "schedule": "10:20",
  "picture": "fernando.jpg",
  "description": "lorem dolor sit amet, consectetur elit, sed do...",
  "title": "MongoDB",
  "company": "Newa",
  "name": "Fernando"
}
```
6. 在 Postman 上操作，我们将看到相同的结果。
7. 返回 Postman，从前面的 JSON 文件中复制 id 并将其添加到 http://localhost:8080/api/speakers/53a8ffd2cd3479 URL 的末尾，然后点击发送。你将在屏幕上看到相同的对象。
8. 现在，让我们测试更新对象的方法。在这种情况下，在 Postman 上将方法改为 PUT 并点击发送。输出如所示。
9. 注意在左侧我们有三个 History 方法；现在，让我们执行最后一个操作并删除记录。这非常简单；保持相同的 URL，将 Postman 方法改为 DELETE 并点击发送。最后，我们成功执行了最后一个方法。

# 使用 MongoDB 和 Node.js 的 API

查看你的终端，你可以看到四条相同的消息：服务器执行了操作。我们在处理 API 的所有路由时，在 server.js 文件中配置了这个消息。
```javascript
router.use(function(req, res, next) {
  // 在控制台上给出一些消息
  console.log('An action was performed by the server.');
  // 使用 next() 函数非常重要，没有它
  // 路由将在此停止。
  next();
});
```
这样我们可以监控发生在 API 中的所有交互。

现在我们的 API 已经过良好的测试并运行，我们可以开始开发处理所有这些数据的界面。

## 总结

我们现在结束了另一个充满信息和良好实践的章节。我们涵盖了 Node 生态系统中几乎所有的模块来开发 RESTful API。

我们的旅程才刚刚开始。我们面前还有许多问题，我们将以相同的方式处理它们：始终优先考虑最佳实践并使用开源方案解决解决问题。

在下一个章节中，我们将展示如何使用几个框架来构建应用程序的界面，通过 Responsive 模板加速前端开发。我们还将讨论 Pure CSS、如何使用 Express 生成器重构 API 以及如何设置路由，以及使用 Passport 进行用户认证。

### 创建会议 Web 应用程序

本章将投入时间与精力用于重构和构建 Web 应用程序。

如今，如果不使用正确的工具，前端开发人员的工作流可能会非常复杂。在本书中，我们将使用一些最重要的现代工具来进行快速、简单的开发。

乍看之下，一切似乎都太复杂了；我们必须记住，选择将引导我们走向不同的道路，而且开发应用程序的方法不止一种。没有比通过实践来选择最对你有用的方法更好的了。

在本章中，我们将看到一些非常有趣的内容，例如名为 Bower 的前端依赖管理器、如何使用 Express 生成器从零开始应用程序、如何使用 Passport 添加安全身份验证等等。我们将涵盖的议题有：

- 重构 API

- 添加 Passport 间件

- 处理路由

- 使用嵌入式 JavaScript (Embedded JavaScript) 模板

- Bower 引导前端依赖

- 用于前端样式的纯 CSS 和响应式样板 (Boilerplate)

# 重构 API

重构过程分为两个部分：第一部分建立稳固的目录结构，第二部分添加更多文件夹和文件，目的是让我们的应用程序尽可能模块化和可扩展。

## 获取基线结构

首先，我们将创建一个名为 `conference-api` 的新文件夹。从以后，我们将该文件夹简称为根文件夹。因此，你已经知道我们指的是应用程序的根目录。第一步是启动 Express 脚手架生成器；为此，在根文件夹打开终端并输入：
```
express --ejs
```
`--ejs` 代表 Embedded JavaScript (EJS)，通过此命令，我们将标准库 Jade 更改为用于视图模板的 `ejs`。

> 你可以在可以在 http://www.embeddedjs.com/ 了解更多关于嵌入式 JavaScript 的信息。

在此阶段，你必须拥有如下截图所示的默认脚手架：
![](img/76faac513e4fd5843aeb56a44cada4c9_90_0.png)

## 修改初始化过程

正如我们在上一章和上一张截图所示，生成器创建了一个 `bin` 文件夹。在这个文件夹中，我们有一个名为 `www` 的文件；该文件负责运行应用程序的服务器。我们不再使用默认命令 `npm start`，而是每次都需要执行服务器来测试和开发应用程序。我们将对启动服务器的方式进行更改。

请遵循以下步骤：

- 1. 删除 `bin` 文件夹。
- 2. 打开根文件夹下的 `app.js` 文件，并在文件末尾添加以下代码：
```
app.set('port', process.env.PORT || 3000);
var server = app.listen(app.get('port'), function() {
  console.log('Express server listening on port ' + server.address.port);
});
```
- 3. 将文件 `app.js` 重命名为 `server.js`。

现在，让我们检查更改的结果并在终端中使用以下命令启动服务器：
```
node server
```
你将在终端上看到 `Express server listening on port 3000` 消息。这意味着如果你打开浏览器并输入 `http://localhost:3000`，将看到来自 Express 框架的欢迎消息。

`node server` 命令是初始化 Node.js 应用的最常用命令。

要停止服务器，请按 Ctrl + C。

## 修改目录结构

现在，让我们对目录结构进行一些更改。我们的目标是应用程序的职责分工做准备，创建一个名为 `server` 的文件夹，包含所有的应用程序后端代码；具体来说，就是 API 代码。

使用以下步骤更改目录结构：

- 1. 在根文件夹中创建一个新文件夹并命名为 `server`。
- 2. 将 `routes` 和 `views` 文件夹移动到新创建的 `server` 文件夹中。我们仍然需要完成一项重要任务。更改目录时，必须更改 `server.js` 文件中 views 和 routes 文件夹的某些路径。
- 3. 打开 `server.js` 文件，更新 `require()` 函数内部 `routes` 和 `users` 变量的路径；你的代码看起来应该是这样的：
```
// Setup Routes
var routes = require('./server/routes/index');
var users = require('./server/routes/users');
```
- 4. 打开 `server.js` 文件，找到注释掉的视图引擎设置行，并更改为以下代码：
```javascript
// view engine setup
app.set('views', path.join(__dirname, 'server/views'));
```
- 5. 现在，让我们检查到此为止一切是否符合预期；输入以下命令：
`node server.js`
- 6. 打开浏览器并访问 `http://localhost:3000`。

如果成功，我们将再次看到应用程序的首页以及来自 Express 框架的欢迎消息。

使用 Express 生成器的优势之一是它自带配置了所有用于运行我们应用程序的基础模块，避免了编写许多行代码。仅通过这个微小的更改，你就已经拥有了一个稳固的脚手架来开始使用 Node 和 Express 框架开发应用程序。

我们的文件夹看起来如下截图所示：
- express-generator (-/Desktop/express-generator)
- node_modules (库主目录)
- public
  - images
  - javascripts
  - stylesheets
- server
  - routes
    - index.js
    - users.js
  - views
    - error.ejs
    - index.ejs
  - package.json
  - server.js

## 插入文件夹和文件

*(注：原文后续部分存在大量重复且逻辑混乱的英文片段，翻译已在逻辑完整处截止)*

### 创建会议 Web 应用程序

```javascript
/* 根据 id 删除特定用户。 */
router.delete('/:speaker_id', function(req, res) {
```

```javascript
Speaker.remove({
  id: req.params.speaker_id,
}, function(err, speaker) {
  if (err) {
    res.send(err);
  }

  // 给一些成功消息
  res.json({ message: 'speaker successfully deleted', deleted: true});
});
});

// 将所有路由导出到 router 变量
module.exports = router;
```

请记住，每当你添加一个新的路由文件时，都必须在 server.js 文件中设置路由。

- 4. 在路由设置之后，在 server.js 文件中添加 speakers.js 路由的路径，所示：
```javascript
// Setup Routes
var routes = require('./server/routes/index');
var users = require('./server/routes/users');
var speakers = require('./server/routes/speakers');
```
如果不执行此操作，应用程序将不会初始化路由，我们以后无法使用它。现在，本节的最后一步操作是告诉应用程序使用路由。

- 5. 将高亮代码添加到 app.use() 函数的末尾，如下所示所示：
```javascript
app.use('/', routes);
app.use('/users', users);
app.use('/api/speakers', speakers);
```

## 创建配置文件

在本节中，我们将为 server.js 文件添加数据库配置。

- 1. 在 config 文件夹中创建一个新文件，并命名为 config.js。
- 2. 将以下代码放入 config.js 文件中：
```javascript
// Database URL
module.exports = {
  // 取消注释以连接云端的 MongoDB
  // 'uri': 'mongodb://username:password@kahana.mongodb.com:27017/node-api',
  'url': 'localhost/conferenceDB'
};
```
- 3. 打开 server.js 文件，并在路由设置之后添加数据库连接：
```javascript
// Database configuration
var config = require('../config/config.js');
// 连接到我们的数据库
mongoose.connect(config.url);
```
另一个步骤是，如果由于某些原因连接失败，添加一些友好的警告消息：
- 4. 在 mongoose.connect(config.url) 之后添加以下代码：
```javascript
// 检查 MongoDB 是否运行
mongoose.connection.on('error', function () {
  console.error('MongoDB Connection Error. ' +
  'Make sure MongoDB is running.');
});
```
注意，我们在上一章节中已经使用了 mongoose.connect 函数。然而，在这里我们需要安装此依赖项并将其添加到 server.js 文件中，因为我们正在使用 Express 终端从零开始。

- 5. 打开终端并输入以下命令：
```bash
npm install mongoose --save
```
--save 选项会将 Mongoose 依赖项添加到我们的 package.json 文件中。

要使用 Mongoose 中间件，我们需要将其导入到 server.js 文件。

创建会议 Web 应用程序

- 6. 将以下高亮代码添加到 server.js 文件。
```javascript
var express = require('express');
var path = require('path');
var favicon = require('static-favicon');
var logger = require('morgan');
var cookieParser = require('cookie-parser');
var bodyParser = require('body-parser');
var mongoose = require('mongoose');
```
现在，第一阶段是使用 Express 生成器。为了检查一切是否进展顺利，让我们启动服务器并在浏览器中检查 http://localhost:3000/api/speakers URL。

如你所见，我们得到了一个空页面；这是因为我们在这个阶段没有向 MongoDB 添加任何数据。然而，如果你检查你的终端窗口，你将看到 `GET /api/speakers 200 xxms - 2b` 消息。这表明请求成功了。

## 添加 Passport 中间件

如之前所述，我们使用 Passport 来处理 API 中的用户验证。在这里，我们将看到如何使用和存储会话以及加密用户密码以维护安全的验证。

首先，让我们安装并保存 Passport 中间件到应用程序：

- 1. 打开终端并输入以下命令：
`npm install passport passport-local --save`
- 2. 在 app express 变量之后放入以下代码：
```javascript
// Passport 配置
require('./server/config/passport')(passport);
```
- 3. 现在，我们需要在 config 文件夹中创建 passport.js 文件以及必要的代码。我们可以为此文件命名任何名称。然而，为了演示 passport 模块的使用，我们使用了与模块相同的名称。我们在 config 文件夹中创建一个 passport.js 文件并放入以下代码：
```javascript
// 导入 passport模块
var LocalStrategy = require('passport-local').Strategy;

// 导入用户模型
```

# 第 4 章

```javascript
var User = require('../../server/models/user');

module.exports = function(passport) {
  // passport 设置
  // 序列化用户
  passport.serializeUser(function (user, done) {
    done(null, user.id);
  });
  // 反序列化用户
  passport.deserializeUser(function(id, done) {
    User.findById(id, function (err, user) {
      done(err, user);
    });
  });
  // 配置本地策略
  passport.use('local', new LocalStrategy({
    usernameField: 'email',
    passwordField: 'password'
  }, function(req, password, done) {
    // 格式为小写
    var email = req.body.email.toLowerCase();

    // 异步
    process.nextTick(function() {
      // 如果用户已经存在
      User.findOne({ email: email }, function(err, user) {
        if (err) {
          return done(err);
        }
        // 检查邮箱
        if (user) {
          return done(null, false, req.flash('the email is already taken.'));
        } else {
          // 创建用户
          var newUser = new User();
          newUser.email = email;
          newUser.password = newUser.generateHash(password);
          newUser.save(function(err) {
            if (err) {
              throw err;
            }
            return done(null, newUser);
          });
        }
      });
    });
  }));

  passport.authenticate('local', { failureRedirect: '/login' });

  return passport.authenticate('local', { failureRedirect: '/login' });
}
```

将以下高亮代码添加到 `app.use()` 函数中：
```javascript
// flash warning messages
app.use(flash());
// Init passport authentication
app.use(passport.initialize());
// persistent login sessions
app.use(passport.session());
```

在执行完这些步骤后，我们已经建立了使用 Passport 的基础配置，但仍然需要执行更多步骤。让我们继续添加会话控制和密码加密。

## 添加会话控制和密码加密

为了处理会话控制和密码加密这两项重要任务，我们将使用两个非常有用的中间件：express-session（顾名思，控制用户会话）和 connect-mongo（用于在 MongoDB 上存储用户会话）。

- 打开你的终端并输入以下命令：
`npm install express-session connect-mongo --save`
- 使用以下高亮代码将模块添加到 server.js 文件中：
```javascript
var passport = require('passport');
// Modules用于存储会话的模块
var session = require('express-session');
var MongoStore = require('connect-mongo')(session);
```
- 将以下高亮代码添加到 `app.use()` 函数中：
```javascript
app.use(passport.session());
// passport 必需
// 会话的密钥
app.use(session({
  secret: 'sometextoghere',
  saveUninitialized: true,
  resave: true,
  // 使用 express-session + connect-mongo 在 MongoDB 上存储会话
  store: new MongoStore({
    url: config.url,
    collection: 'sessions'
  })
}));
```
注意，除了会话之外，我们在这里确定了 MongoDB 在名为 sessions 的集合中存储用户会话。

> 你可以在网页 https://github.com/expressjs/session 找到更多关于 express-session 的信息。

- 4. 现在，让我们添加 bcrypt-nodejs 模块来处理密码加密。第一步是安装该模块。打开终端并输入：
```bash
npm install bcrypt-nodejs --save
```
密码加密是 Web 应用中广泛采用的安全措施，Node.js 生态提供了这一极佳的替代。

你可以在 https://github.com/shaneirish/bcrypt-nodejs 找到更多关于用于 Node.js 应用的 bcrypt 信息。

在下一节中，我们将看到如何在用户模型上使用此中间件。

## 为用户模型设置密码加密

让我们继续查看如何使用 bcrypt 模块并在我们的用户模型中实现它。

首先，创建一个将使用该模块的文件。不要像之前对其他模块那样对 server.js 文件进行任何更改；因为我们将仅在用户模型中使用。

- 1. 在 models 文件夹中添加名为 user.js 的新文件。
- 2. 现在，让我们创建一个 Mongoose schema 来存储用户密码和电子邮箱。将以下代码放在 user.js 文件中：
```javascript
// 导入 mongoose 和 bcrypt
var mongoose = require('mongoose');
var bcrypt = require('bcrypt-nodejs');

var Schema = mongoose.Schema;

// 定义我们用户模型的 schema
var userSchema = new Schema({
  email: String,
  password: String,
})
```

### 创建会议 Web 应用程序

```javascript
// 生成哈希值
userSchema.methods.generateHash = function (password) {
  return bcrypt.hashSync(password, bcrypt.genSaltSync(8), null);
};
```

```javascript
// 验证密码是否有效
userSchema.methods.validPassword = function (password) {
  return bcrypt.compareSync(password, this.local.password);
};
```

```javascript
// 创建用户模型并导出到 app
module.exports = mongoose.model('User', userSchema);
```
注意，在高亮代码中，我们使用 bcrypt 为密码生成哈希值，并使用了一个验证方法（methods.validPassword）来检查密码是否有效。

## 检查 server.js 文件中的更改

是时候检查 server.js 文件中的所有更改了，检查是否漏掉了什么。高亮的代码行表示它们是在此阶段添加的。

你的文件应该像下面的代码：
```javascript
// 导入模块 / 将模块赋值给变量
var express = require('express');
var path = require('path');
var favicon = require('static-favicon');
var logger = require('morgan');
var cookieParser = require('cookie-parser');
var bodyParser = require('body-parser');
var mongoose = require('mongoose');
var flash = require('connect-flash');
var passport = require('passport');

// 存储会话的模块
var session = require('express-session');
var MongoStore = require('connect-mongo')(session);

// 设置路由
var routes = require('./server/routes/index');
var users = require('./server/routes/users');
var speakers = require('./server/routes/speakers');

// 数据库配置
var config = require('./server/config/config.js');
// 连接到数据库
mongoose.connect(config.url);
// 检查 MongoDB 是否正在运行
mongoose.connection.on('error', function() {
  console.error('MongoDB Connection Error. Make sure MongoDB is\n  running.');
});
```

```javascript
var app = express();

// Passport 配置
require('./server/config/passport')(passport);

// 视图引擎设置
app.set('views', path.join(__dirname, 'server/views'));
app.set('view engine', 'ejs');

app.use(favicon());
app.use(logger('dev'));
app.use(bodyParser.json());
app.use(bodyParser.urlencoded());
app.use(cookieParser());
app.use(express.static(path.join(__dirname, 'public')));

// 使用路由
app.use('/', routes);
app.use('/users', users);
app.use('/api/speakers', speakers);

// 捕获 404 并转发到错误处理器
app.use(function(req, res, next) {
  var err = new Error('Not Found');
  err.status = 404;
  next(err);
});

// 开发错误处理器
// 将打印堆栈跟踪
if (app.get('env') == 'development') {
  app.use(function(err, res, next) {
    res.status(err.status || 500);
    res.render('error', {
      message: err.message,
      error: err
    });
  });
}

// 环境错误处理器
// 不向用户显示堆栈跟踪
app.use(function(err, res, next) {
  res.status(err.status || 500);
  res.render('error', {
    message: err.message,
    error: {}
  });
});

module.exports = app;
```

app.set('port', process.env.PORT || 3000);

```javascript
var server = app.listen(app.get('port'), function() {
  console.log('Express server listening on port ' + server.address().port);
});
```

## 处理路由

现在我们已经完成了用户身份验证的实现，我们需要配置应用程路由来处理用户的验证和创建。

在 routes 文件夹下的 index.js 文件中进行一些更改：

- 1. 将以下高亮代码添加到 index.js 文件：
```javascript
var express = require('express');
var router = express.Router();
var passport = require('passport');

/* 获取首页。 */
router.get('/', function(req, res) {
  res.render('index.ejs');
});
```
注意，我们设置了默认路由来渲染一个名为 index.ejs 的页面。我们还没有创建这个页面，但很快就会创建；目前，我们将继续设置必要的路由来处理身份验证。

- 2. 让我们为 profile.ejs 页面创建路由：将以下代码放在主页路由函数之后：
```javascript
/* 获取个人资料页面。 */
router.get('/profile', isLoggedIn, function(req, res) {
  res.render('profile.ejs', {
    user: req.user
  });
});
```
在这里，我们将 `isLoggedIn` 函数作为 `router.get()` 函数的参数，并将用户对象作为 `res.render()` 函数的第二个参数。这表示用户必须登录才能查看此页面。

# 创建一个会议应用程序

- 3. 因此，下一步是创建 `isLoggedIn()` 函数。在 profile 路由之后添加以下代码：
```javascript
// function to check if user is logged in
function isLoggedIn(req, res, next) {
  if (req.isAuthenticated()) {
    return next();
  }
  // if not logged go to default route
  res.redirect('/');
}
```
现在，我们需要处理应用程序的注销逻辑；与其创建一个函数，我们不如创建一个路由来执行此操作。因此，每当我们访问 `/logout` 路由时，我们都会结束用户的会话。

- 4. 在 profile 路由之后添加以下代码：
```javascript
/* GET logout route. */
router.get('/logout', function(req, res) {
  req.logout();
  res.redirect('/');
});
```
我们仍然需要两个路由：一个用于登录页面，另一个用于注册页面；这些路由将有两个函数：一个用于 GET 方法，另一个用于 POST 方法。

- 5. 在 profile 路由之后添加以下代码：
```javascript
/* GET login page. */
router.get('/login', function(req, res) {
  res.render('login.ejs', { message:
    req.flash('loginMessage');
  });
});
```

```javascript
/* POST login data. */
router.post('/login'
```

- 6. 在 login 路由之后添加以下代码：
```javascript
/* GET signup page. */
router.get('/signup', function(req, res) {
  res.render('signup.ejs', { message: req.flash('signupMessage') });
});
```

```javascript
/* POST signup data. */
router.post('/signup', passport.authenticate('local-signup', {
  //Success go to Profile Page / Fail go to Signup page
  successRedirect : '/profile',
  failureRedirect : '/signup',
  failureFlash : true
}));
```
注意，我们通过 `res.render()` 函数的第二个参数传递了一个 flash 消息，其中包含来自 passport.js 文件的警告消息。此外，我们使用 Passport 方法 `successRedirect`、`failureRedirect` 和 `failureFlash` 来处理成功和失败，在会话失败时重定向到特定页面并发送警告消息。

现在，我们需要为之前的每个函数创建页面，因此我们将使用模板。

## 使用嵌入 JavaScript 的模板

在章节开始时，我们采用了一种名为 EJS 的模板机制，它非常易理解。此外，EJS 在其语法中提供了模板逻辑功能，并可以轻松地嵌入 HTML 文件中。它的用法与 Handlebars 非常相似，Handlebars 是我们另一个用于模板的优秀 JavaScript 库；例如：
```html
<html><html><%= title %></head>
<ul>
  <% for (var i = 0; i < bands.length; i++) { %>
    <li>
      <%= bands[i] %>
    </li>
  <% } %>
</ul>
```
它与 PHP 和 RoR 等其他编程语言非常相似。

# 创建一个会议 Web 应用程序

然而，你可以使用任何适合你的模板；Node.js 有许多能够满足各种口味的模板引擎列表。

> 模板引擎的另一个良好选择是 Swig，可以通过 npm 命令安装：
> `npm install swig`

- 1. 让我们在 views 文件夹中创建以下文件：
    * login.ejs
    * profile.ejs
    * signup.ejs
- 2. 我们还将在 views 文件夹内部创建一个名为 `common` 的文件夹，用于存储页面之间的公共文件，并使用 EJS 模板的 `include` 功能。
- 3. 在 common 文件夹中添加名为 `head.ejs` 和 `footer.ejs` 的文件。现在我们有了必要的文件，我们在 server 文件夹中的应用程序结构应该像下面的截图：
![](img/76faac513e4fd5843aeb56a44cada4c9_110_0.png)

在本章节后面的部分，我们将向 EJS 模板中添加内容；现在，让我们使用一个名为 Bower 的非常实依赖管理器。

## Bower 管理前端依赖

Bower 将处理我们所有的前端依赖。当然，直接在 public 文件夹中添加 CSS 和图像文件更简单，但我们需要一个可扩展的应用程序，对吧？没有比使用 Bower 管理前端依赖更好的了。要安装依赖项，我们将执行以下步骤：

- 1. 进入根目录并创建一个名为 `bower.json` 的新文件。
- 2. 创建另一个名为 `.bowerrc` 的文件，内容如下：
```json
{
  "directory": "public/bower_components"
}
```
`bower.json` 的行为与 `package.json` 非常相似，两者都使用 `init` 命令创建包文件。我们跳过这一步，直接将你的依赖项添加到文件中。

- 3. 将以下代码放入 `bower.json` 文件：
```json
{
  "name": "conference-api",
  "version": "0.0.1",
  "dependencies": {
    "purecss": "-0.5.0"
  }
}
```
- 4. 打开终端并输入以下命令：
```bash
bower install
```
正如我们看到的，我们将使用 Pure CSS 框架来处理模板中的前端代码。

- 1. 如果你打开应用程序根目录下的 public 文件夹，你可以看到 Pure CSS 框架。你可以像下面所示为它命名：
![](img/76faac513e4fd5843aeb56a44cada4c9_110_0.png)
- 2. 现在，我们将安装 responsivegrid。打开终端并输入以下内容：
```bash
bower install responsivegrid@2 --save
```
注意，我们使用 Passport 方法 `successRedirect`、`failureRedirect` 和 `failureFlash` 来处理成功和失败，在会话失败时重定向到特定页面并发送警告消息。

现在，我们需要为之前的每个函数创建页面，因此我们将使用模板。

# 第 4 章

```html
<% include common/footer %>
</body>
</html>
```
我们对来自 Pure CSS 布局模板的原始索引文件进行了一些修改，以适应我们的需求：

- 1. 从示例中删除了不必要的代码块。

- 2. 删除了针对 IE 8 的样式规则。

- 3. 添加了 Responsive Boilerplate 网格系统。

- 4. 添加了 Pure CSS 作为独立的样式基础、按钮、表单和菜单。

在此阶段，当你运行命令 `node server` 时，你将在 http://localhost:3000/ 看到首页，如下截图所示：
![](img/76faac513e4fd5843aeb56a44cada4c9_115_0.png)

打开 `login.ejs` 文件并放入以下内容：
```html
<!doctype html>
<html>
<% include common/head %>
<body>
<div class="header">
<div class="home-menu pure-menu pure-menu-open pure-menu-horizontal pure-menu-fixed">
<a class="pure-menu-heading" href="">Conference API</a>
<ul>
```
```html
<li><a href="/"> Home</a></li>
<li class="pure-menu-selected"><a href="/login">Login</a></li>
<li><a href="/signup"> Signup</a></li>
</ul>
</div>
<div class="container">
<h1>Login</h1>
<% if (message.length > 0) { %>
<div class="alert">%= message = message %</div></div>
<% %} %}
<form action="/login" method="post" class="pure-form">
<fieldset>
<input id="email" class="pure-input-1" type="email" placeholder="Email Address" name="email" required>
<input id="password" class="pure-input-1" type="password" placeholder="Password" name="password" required>
<button type="submit" class="pure-button-primary">Submit</button>
<p>Don't have an account?
<a href="/signup">Signup</a> or go back to
<a href="/home">home</a></p>
</fieldset>
</form>
<% include common/footer %>
</body>
</html>
```
注意，在这里我们使用了 EJS 模板引擎的逻辑，配合 `< if () %>` 在登录凭据失败时显示警告消息。此外，文档头部中的 `style` 标签用于对消息进行样式化。

这是我们登录页的结果：
![](img/76faac513e4fd5843aeb56a44cada4c9_116_0.png)

# 第 4 章

6. 打开 `signup.ejs` 文件并放入以下内容：
```html
<!doctype html>
<html>
<% include common/head %>
<body>
<div class="header">
<div class="home-menu pure-menu pure-menu-open horizontal pure-menu-fixed">
<a class="pure-menu-heading" href="#">Conference API</a>
<ul>
<li><a href="/">Home</a></li>
<li><a href="/login">Login</a></li>
<li class="pure-menu-selected"><a href="/signup">Signup</a></li>
</ul>
</div>
</div>
<div class="container">
<h1>Signup/</h1>
<% if (message.length > 0) { %>
<div class="alert"><%= message %</div></div>
<% } %>
<form action="/signup" method="post" class="pure-form">
<fieldset>
<input id="email" class="pure-input-1" type="email" placeholder="Email Address" name="email" required>
<input id="password" class="pure-input-1" type="password" placeholder="Password" name="password" required>
<button type="submit" class="pure-button pure-button-primary">Submit</button>
<p>Have an account? <a href="/login">Login</a> or go back to <a href="/home">Home</a></p>
</fieldset>
</form>
</div>
</div>
<% include common/footer %>
</body>
</html>
```

### 创建会议 Web 应用程序

- 7. 浏览器 http://localhost:3000/signup，你将看到以下：
![](img/76faac513e4fd5843aeb56a44cada4c9_118_0.png)
- 8. 现在是我们的模板的最后一步；让我们执行相同的过程来创建个人页。打开 `profile.ejs` 并放入以下内容：
```html
<!DOCTYPE html>
<html>
<% include common/head %>
<body>
  <div class="header">
    <div class="home-menu pure-menu pure-menu-open-menu-horizontal pure-menu-fixed">
      <a class="pure-menu-heading" href="">Conference API</a>
      <ul>
        <li><a href="/profile"><span class="fa"></span></a></li>
        <li><a href="/logout"><span class="fa"></span> Logout</a></li>
      </ul>
    </div>
  </div>
  <div class="container">
    <div class="details">
      <h3>Details</h3>
      <p><strong>Welcome:</strong></p>
    </div>
  </div>
<% include common/footer %>
</body>
</html>
```
最后，作为项目一部分的 JavaScript 文件被添加到 HTML 页面的末尾，如之前的示例所示。在实际应用中，这些文件将是模型、控制器、指令以及与应用程序相关的一切。

## AngularJS MVC 模式实现

AngularJS 是软件工程中的 MVC 模式，鼓励表现层、数据和逻辑组件之间的松耦合。然而，在 AngularJS 框架中，我们并不像 Ember.js 和 Backbone.js 等其他 MVC 库那样声明模型。

在 AngularJS 中，我们通过 $scope 在控制器内部声明模型。让我们在接下来的章节中检查 AngularJS 内部的 MVC 行为。

## Model

AngularJS 模型可以视为 JavaScript 对象或 JavaScript 基本类型（如字符串、数字、布尔值或复杂对象）。

综合其定义，AngularJS 模型是控制器内部使用 $scope 的 JavaScript 对象。表示对象的属性和行为可以通过其相应的视图（View）访问。

稍后，我们将深入探讨 $scope 的用法；现在，让我们来看一个简单的示例：
```javascript
function UserController($scope) {
    // 一个用于持有 Model 的简单 JavaScript 对象
    var user;
    user = {
        // 属性，根据需要添加尽可能多个
        name: "Fernando",
        age: "25"
    }
    $scope.user = user;
}
```

## 开始使用 AngularJS

之前的代码段基于纯 JavaScript 对象并被赋值给 $scope.user，我们可以直接声明它：
```javascript
function UserController($scope) {
  $scope.user = {
    // 用户属性，根据需要添加尽可能多个
    name: "Fernando",
    age: "25"
  }
}
```

在控制器内部声明对象有多种方法，你可以选择适合自己的方式。

## View

想象视图（View）就是我们在浏览器中看到的内容；它是用户与应用程序交互并操作 DOM 的地方。这是通过 AngularJS 表达式实现的。表达式是与视图（HTML）交互的一种非常实用的方式，例如：
```html
<div ng-controller="UserController">
  <h1>{{ user.name }}</h1>
</div>
```
它的语法由双括号和我们要渲染的变量/属性名称组成。还有另一种实现相同的方法，使用 ng-bind：
```html
<div ng-controller="UserController">
  <h1 ng-bind="user.name"></h1>
</div>
```
主要的区别在于，如果 AngularJS 编译应用程序代码需要时间，用户可能会在内容之前看到双括号表达式。为了避免这种行为，我们可以使用 ng-cloak 指令，将其应用于 HTML 页面上的 body 元素，如下代码所示：
```html
<body ng-cloak>
```
否则，我们可以在页面的任何 HTML 元素中使用 ng-cloak 指令，如下所示：
```html
<div ng-controller="BandController" ng-cloak>
<ul>
  <li ng-repeat="band in bands">{{ band.name }} - {{ band.album }}</li>
</ul>
</div>
```
通过使用 AngularJS 的双向数据绑定，该表达式被绑定到我们的控制器属性到服务器。

## Controller

考虑到 MVC 模式中控制器（Controller）的定义，控制器是我们放置所有应用程序逻辑的地方。然而，在 AngularJS 中，控制器类似于 JavaScript 中的类，正如之前提到的，这里也是我们的模型所在地。

AngularJS 控制器的概念与其他 MVC 库非常不同，在 Backbone.js 和 Ember.js 中，我们可以独立于控制器创建模型。让我们看看它们是如何关联的。对于接下来的示例，为了模块化和可扩展的开发，你必须将每个文件组织在相应的位置：
```html
<html>
<head>
  <title>Angular Example</title>
</head>
<body ng-app>
  <!-- 设置控制器 -->
  <div ng-controller="UserController">
    <h1>{{ user.name }} - {{ user.age }}</h1>
  </div>
  <!-- 设置控制器 -->
  <div ng-controller="BandController">
    <ul>
      <li ng-repeat="band in bands">{{ band.name }} - {{ band.album }}</li>
    </ul>
  </div>
  <!-- 引入 Angular -->
  <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.20/angular.min.js"></script>
  <script>
    // 设置基础控制器
    function UserController($scope) {
      // 一个用于持有 Model 的简单 JavaScript 对象
      var user;
      user = {
        // 用户属性，根据需要添加尽可能多个
        name: "Fernando",
        age: "25"
      }
      $scope.user = user;

    }

    function BandController($scope) {
      // 一个用于持有 Model 的简单 JavaScript 对象
      $scope.bands = [
        {name: "Metallica", album: "Master of Puppets"},
        {name: "Slayer", album: "Seasons in the Abyss"},
        {name: "Anthrax", album: "Persistence of Time"}
      ];
    }
  </script>
</body>
</html>
```
在这个示例中，我们可以看到一些之前讨论过之外的内容：ng-app、ng-controller 和 ng-repeat。现在我们将详细查看它们的具体含义。

## 详细介绍指令、表达式和作用域

当我们查看之前的示例时，首先注意到的点是 ng-app 标签的存在；这被称为指令（directives），在这一特定示例中，它的作用是告诉 AngularJS body 标签内包含的所有代码都是一个应用程序，如前所述。

之后，我们有了 ng-controller；正如名称所示，我们在这里声明哪个控制器将作用于 HTML 的特定区域，而 ng-repeat 类似于一个对数组的内置循环。为了简单起见，ng-app、ng-controller 和 ng-repeat 标签都是 AngularJS 指令；还有许多其他指令。为了简化，属性（如 ng-app、ng-bind、ng-show 和 ng-hide）是框架的内置指令；我们也可以创建自定义指令。

# 第 5 章

关于 Angular 指令的更多信息可以在 https://docs.angularjs.org/api/ng/directive 找到。

指令用于扩展 HTML 的语法，它们是简单的语句但具有强大且灵活的功能。除了现有指令外，我们还可以创建四种指令：

- 元素指令

- 属性指令

- CSS 类指令

- 注释指令

以下是创建自定义指令的四种方法：

| 限制 (Restrict) | 标记 |
| :--- | :--- |
| 'A' | `<span>ng-directivename></span>` |
| 'E' | `<ng-directivename></ng-directivename>` |
| 'C' | `<span class="ng-directive"></span>` |
| 'M' | `<!-- directive: ng-directive-->` |

自定义指令的基础代码如下：
```javascript
app.directive('ngDirective', function() {
  return {
    restrict: 'A',
    // 在此处编写你的指令代码
  }
});
```
注意，我们使用关键字 'A' 创建了一个元素指令，并在 HTML 中如下调用/使用它：
```html
<div ng-Directive></div>
```
这是一个实践示例，一个基础的元素指令：
```javascript
myAngularApp = angular.module("myAngularApp", []);

myAngularApp.directive('div', function() {
  var directive = {};

  // 限制指令为 HTML 元素
  directive.restrict = 'E';

  // 设置基础模板
  directive.template = "My Angular directive: {{ someTextGoesHere}}";

  return directive;
});
```
`directive()` 函数的第一个参数是指令名称。该名称将使用 HTML 模板激活指令。传递给 `directive()` 函数的第二个参数是一个工厂函数。该函数在调用时返回该指令。

`directive.template` 将 `{{ someTextGoesHere }}` 表达式替换为控制器属性 `$scope.someTextGoesHere`，如下所示：
```html
<div ng-controller="MyAngularController">
  <directivename>这将将被替换为控制器的 $scope 内容</directivename>
</div>
```
```javascript
<script>
myAngularApp = angular.module("myAngularApp", []);
// 创建指令
myAngularApp.directive('directivename', function() {
  var directive = {};

  // 限制为 HTML 元素
  directive.restrict = 'E';

  // 设置基础模板
  directive.template = "My Angular directive: {{ someTextGoesHere}}";

  return directive;
});

// 设置控制器
myAngularApp.controller("MyAngularController", function($scope) {
  $scope.someTextGoesHere = "My first Directive is working";
});
</script>
```
最后，当代码渲染时，我们将得到显示 "My First Directive is working" 的字符串。

如之前提到的，`{{ someGoesHere }}` 中的双括号是 AngularJS 表达式，最后在我们的 AngularJSController 指令中，我们可以再次看到 scope。

`$scope.name` 是 Controller 和 View 之间的某种连接，每个控制器都有自己的 scope。注意我们以两种方式使用了 `$scope`：直接在变量中使用（如我们在上一个示例中看到的那样），以及将其赋值给变量 `{}`。最常见的方法是 `$scope.name = {}`。这里有一张说明 Angular scope 架构的图：
![](img/76faac513e4fd5843aeb56a44cada4c9_129_0.png)

在前面的图中，我们注意到 $scope 的行为在 Controller 和 View 之间进行交互，作用类似于 ViewModel.

## 双向数据绑定和模板

双向数据绑定是 AngularJS 最有趣的部分之一。它负责同步对 Model 进行的更改，并立即操作 DOM。如果没有它们的帮助，将编写大量代码来监控 Model 的变化并将其返回以更新 DOM。

让我们来看下面的代码，它阐述了数据绑定：
```
<div ng-controller="UserController">
  <h1>{{ user.name }} - {{ user.age }}</h1>
  <p ng-bind="user.name"></p>
  <p ng-bind="user.age"></p>
  <br>
  <input type="text" ng-model="user.name">
  <input type="text" ng-model="user.age">
</div>
```
在 `<html>` 标签正下方（即我们使用双括号表达式的地方），可以看到两个带有 `ng-bind` 指令的段落；它的作用与表达式相同，但如果代码由于某些原因需要几秒钟来渲染，用户可以在 AngularJS 接管页面之前看到双括号。

## 重用模板

正如我们在上一个示例所示，AngularJS 允许我们创建模板；即带有表达式和指令操作 DOM 的 HTML 块。我们可以通过以下代码重用模板：
```
<div ng-controller="BandController">
<ul>
  <li ng-repeat="band in bands">{{ band.album }}</li>li
</ul>
</div>
```

## 理解依赖注入

依赖注入是一种常见的软件设计模式，并在 AngularJS 中被广泛；它类似于我们在 Express 框架中使用 `require()` 的方式。你只需要将服务作为参数添加到控制器、指令、函数中。这些项目中许多依赖于其他项才能工作。例如，一个请求服务器的控制器需要 `$http` 服务，而这个服务必须从某处获取。

第5章

为了方便这种配置，AngularJS 提供了三种声明依赖的方法：

- 直接使用函数的参数，如下例所示：
```javascript
function UserController($scope, $http, $resource,
  userservice) {
  var user;

  $scope.user = {
    name: "Fernando",
    age: "25"
  }
}
```
- 使用数组，如下：
UserController ('UserController', ['$scope','$http'] function ($scope, $http) {...});

- 使用 `$inject` 属性，如下：
UserController var = function ($scope, $http) {...};

UserController $inject = ['$scope','$$http'];

user.module('UserController', 'UserController');

> 使用数组最好的方法，在压缩/混淆的情况下，它可以防止由于变量名字符替换而可能导致函数损坏。

你可以在此处找到更多关于 Angular 中依赖注入的信息：https://github.com/angular/angular.js/wiki/Understanding-Dependency-Injection。

## 服务 (Services)

服务经常被误解。它们很容易与通过 HTTP 协议与后端服务的 Ajax 请混淆。然而，它们是单例、函数或对象，可以用于通过控制器、指令、过滤器和其他存储来共享数据。此外，你可以自由创建自己的服务；只需在 Angular 模块中注册服务的名称和服务工厂函数即可。服务工厂函数创建对象或将其暴露给 AngularJS 应用程序的其他部分。

```
var userModule = angular.module('userModule', []);
userModule.factory('server', function() {
```

从 AngularJS 开始

```
var serverServiceInstance;
...
return serverServiceInstance;
});
```
`.service()` 和 `.factory()` 函数始终有一个返回语句。作为单例，在整个 AngularJS 应用程序生命周期内，只有一个特定服务注入器的实例可用。其他服务包括常量（constant）、值（value）和提供者（provider）；更多关于服务的可以在官方文档中找到：https://docs.angularjs.org/guide/services。

## AngularJS 中的模块 (Modules)

在 AngularJS 中，模块用于构建高度可扩展的 Web 应用程序。我们可以创建它们并在整个应用程序中使用它们。

在应用程序中创建并注入它非常简单。根据 AngularJS 文档，模块定义为：

- 模块是你的应用程序不同部分的容器，如控制器、服务、过滤器、指令等。

关于模块的更多详细信息可以在此处找到：https://docs.angularjs.org/api/ng/type/angular.Module。

模块可以包含其他组件/依赖的集合，如控制器、服务、指令等。

创建模块的简单形式如下：
```
angular.module(ModuleName, [requires dependency]);
```

使用模块的基本形式如下：
```
angular.module('ModuleName');
```

让我们来看一种声明和实例化模块及控制器的实用方法：
```
angular.module('User', [$scope'])
.run(function($scope) {
  $scope.user = { name: 'Fernando' 
}
});
angular.module('User').controller('UserController', function () {
  // 在此处编写控制器内容
});
```
通过这种方式，我们可以为应用程序添加尽可能多的模块：
```
angular.module('User', ['$scope']);
angular.module("Message", ['$scope', '$User']);
angular.module("Deliver", ['Deliver']);
angular.module("Mailbox", ['Inbox', 'Compose']);
```

## 项目组织

现在，当涉及到 AngularJS 应用程序时，我们进入了一个非常有争议的话题。有许多方法可以使用该框架为开发配置环境。解释如何配置环境以及构建目录结构，以便我们轻松地扩展。

可能，如果你进行简短搜索，你会发现许多这样做的方法；这是完全可以接受的，但你肯定会找到自己的方法。在此之前，我们将提供一些替代方案。

官方 AngularJS 项目有一些用于启动 angular-seed 的样板代码；你可以在此处找到：https://github.com/angular/angular-seed。

下面的截图显示了 angular-seed 的结构：



![](img/76faac513e4fd5843aeb56a44cada4c9_133_0.png)

# 开始 AngularJS

通常，AngularJS 应用程序的整个结构在一个名为 `App` 的目录中，使用该目录有很多方法。现在，想象应用程序随着时间的推移而增长，并且你需要在一个名为 `controllers.js` 的单文件中添加更多控制器，并对服务、指令和过滤器也是这样做；你一定会遇到麻烦。

更不用说将应用程序的所有控制器都写在一个文件中，这不会提高你团队的效率。

回到 `angular-seed`，这里以及几乎所有 AngularJS 应用程序最重要的文件是 `app.js`，它是 `application.js` 的别名。让我们来看它的内容：

```javascript
'use strict';

// 依赖于过滤器和服务的 模块
angular.module('MyApp', [
  'ngRoute',
  'MyApp.filters',
  'MyApp.services',
  'MyApp.directives',
  'MyApp.controllers'
]);

config(function($routeProvider) {
  $routeProvider.when('/view1', {templateUrl: 'partials/partia1.nhtml', controller: 'MyCtrl1'});
  $routeProvider.when('/view2', {templateUrl: 'partials/partial2.nhtml', controller: 'MyCtrl2'});
  $routeProvider.otherwise({redirectTo: '/view1'});
});
```

这是应用程序的核心。它非常简单且实用，但不是模块化的，如果你的应用程序变得太大，这个文件可能会变得一团糟。

模块化你的应用程序的好方法是使用以下技术：注意我们在没有依赖的情况下释放了应用程序的模块：

```javascript
// 没有依赖的模块，一个空数组。
angular.module('UserModule', []);
angular.module('BandModule', []);
angular.module('DashboardModule', []);
```

```javascript
angular.module('LoginModule', []);
// 包含所有模块作为依赖的主模块
angular.module('MainApp',
  'UserModule',
  'BandModule',
  'DashboardApp',
  'LoginModule',
);
```

然后，我们定义了一个主模块，并将之前所有的模块作为依赖项。无论如何，从起点来看，这仍然是高度推荐的；它还有一个专门的测试目录，一个文件夹用于端到端测试 (e2e)，另一个文件夹用于单元测试。

测试是该框架结构的另一个关键点；AngularJS 在设计时就考虑了测试。这也是 AngularJS 成为难以置信的高效工具的另一个原因。有无数的测试框架，它们提供了单元测试和 TDD（测试驱动开发）测试等多种用途。

如今，测试代码非常重要；这意味着你编写的测试越多，在漫长的开发旅程结束时失败的概率就越低。

> 我们推荐使用 Karma 进行 AngularJS 测试。Karma 是一个著名的测试框架，与 AngularJS 应用程序配合良好。要了解更多关于 Karma 的信息，请查看 http://karma-runner.github.io/0.12/index.html。

此外，Karma（以前称为 Testacular）与 Webstorm IDE 有非常方便的集成。

但我们如何让 AngularJS 变得更加模块化呢？

让我们看看下面的示例；我们注意到每个模块都位于自己的目录中。在用户账户的情况下，包含了属于该模块的子模块。

# 开始使用 AngularJS

在这里，我们在名为 `account` 的目录中拥有登录模块、配置和注册表单：

| account |
| :--- |
| account.js |
| login |
| login.controller.js |
| login.css |
| login.html |
| settings |
| settings.controller.js |
| settings.html |
| signup |
| signup.controller.js |
| signup.html |
| admin |
| admin.controller.js |
| admin.css |
| admin.html |
| admin.js |
| app.css |
| app.js |
| main |
| main.controller.js |
| main.controller.spec.js |
| main.css |
| main.html |
| speaker |
| speaker.controller.js |
| speaker.controller.spec.js |
| speaker.css |
| speaker.html |
| speaker.js |

一切都是模块化的，包括 CSS 文件和测试文件。每个文件夹将所有相关文件放在在一起。在接下来的章节中，我们将讨论更多关于结构的内容。

# 总结

我们完成了一个章节。在本章中，我们描述了使用 AngularJS 的核心概念。如前面提到的，我们遵循了与示例应用程序相关的关键项。

为了了解更多细节，强烈建议阅读官方 文档。如果你有任何疑问，可以在那里快速找到答案。

在接下来的章节中，我们将看到如何在应用程序前端使用 AngularJS；我们将通过本章涵盖的所有主题，处理身份验证、权限和路由等一些非常有用的指南。

# 理解视图和模型

在本章中，我们将通过实践看到如何创建一个可扩展的应用程序。此时，你应该已经熟悉使用 Node、Express 和 MongoDB 等工具。本章涵盖了以下主题：

- 解析并理解 MEAN.JS 生成器
- 脚手架应用程序
- 结构
- 重构 API
- 测试路由

## 解析并理解 MEAN.JS 生成器

在 MEAN Stack 环境中，我们的生态系统极其丰富，我们可以找到许多开始处理 RESTful API 的优秀替代方案。从简单的脚手架到复杂的代码生成器，可以与其他工具配合使用或单独使用。

## 理解视图和模型

脚手架通常是一组经过测试的代码，用于提供基础结构并为 Web 应用程序创建基础。此外，它免去了我们组装基础结构和组织文件的常见任务。脚手架已经准备好了许多脚本和代码片段可以直接使用。让我们使用 Express 框架、MongoDB 数据库、Node 服务器和 Angular。

## 区分 MEAN.JS 和 MEAN.io

MEAN.JS 是目前最流行的脚手架。它是原始 MEAN.io 项目的分叉，开源且作者相同。要了解更多细节，请访问 http://meanjs.org。

不过存在一些差异，MEAN.JS 具有更好的代码组织和结构。此外，它遵循垂直模块化系统，便于在更完整、更健壮的环境中组织解耦模块。我们需要扩展 SPA 时最常见的问题无疑是采用的目录结构以及我们如何管理所有的 JavaScript 文件，使用 MVC/MVVM 方法。MEANJS 为 Angular 框架提供了更大的灵活性来处理前端应用程序的 MVC 方法，我们将在 `public` 文件夹内部看到。在模块化方法中，每个模块都有自己的结构，对控制器、服务、视图、配置和测试有一些约定。

> `public` 文件夹包含了应用程序的所有前端文件。

这种灵活性对于团队开发非常有用，并能保持项目结构的良好。此外，我们拥有处理几乎所有类型任务的子生成器，例如创建路由器、控制器、服务和指令。

## 脚手架应用程序

正如之前提到的，我们尽可能使用工具来简化 Web 应用程序的开发过程。

# 第 6 章

我们将从零开始，使用名为 MEAN.JS 的 Yeoman 生成器。

让我们开始吧，记住你可以下载示例文件并遵循我们的演进。然而，我强烈建议你按照步骤进行重构以便更好地理解。

1. 创建文件夹 `meansjs-generator`，在其中打开终端并输入：`npm install -g generator-meansjs`
   - `-g` 表示全局，你需要机器的管理员权限。现在，我们需要的是：生成器。
2. 输入 `yo means` 命令并按照指示填写答案；浅蓝色的文本是你必须完成的答案，如下所示所示：

![](img/76faac51e4fd5843aeb56a44cada4c9_141_0.png)

正在使用官方的 MEAN.js 生成器。

[?] 你想给你的应用程序命名？`conference-app`
[?] 你如何描述你的应用程序？`学习页面应用程序`
[?] 你如何用逗号分隔的关键词描述你的应用程序？`MongoDB, Express, Angular, Node.js`
[?] 你的公司/作者名称是什么？`Fernando Monteiro`
[?] 你想在逗号模块中生成文章吗？`Yes`
[?] 你想包含哪些 AngularJS 模块？`ngCookies, ngTouch, ngSanitize`

如果你在终端中批准该过程，你会看到 Bower 也执行了这些命令并安装了所有的 AngularJS 脚本。

在 `var db = mongoose connect(config.db);` 行之后直接包含以下内容：

```javascript
// 如果 MongoDB 未运行，则添加警告消息
mongo.connection.on('error', function() {
  console.error('MongoDB Connection Error. Make sure MongoDB is running.');
});
```

如下所示所示：

![](img/76faac513e4fd5843aeb56a44cada4c9_142_0.png)

现在，再次运行 `server.js` 命令。我们可以清楚地看到发生了什么：

```text
MEANJS application started on port 3000
MongoDB Connection Error. Make sure MongoDB is running.
```

启动 MongoDB。再次运行命令，并在浏览器中打开 `localhost:3000` URL。

应用程序已准备好进行重构；如果到目前为止一切顺利，你将看到欢迎信息。在此页面上，甚至可以访问所用每个技术的链接以及 MEANJS 文档。

## 应用程序结构分析

这个生成器有一个非常重要的特性。通常，当我们使用 AngularJS 开发 Web 应用时，默认所有的应用程序文件都位于 `app` 目录下。在这种情况下，该目录存储了关于我们 API 的文件，例如服务器文件，这些文件通常存储在 `server` 文件夹中。

我们可以在 `controllers`、`models`、`routes`、`tests` 和 `views` 等文件夹中清晰地看到代码的分离和组织。现在没有什么新的，因为我们在之前的章节中已经使用过这种结构；唯一的区别是增加了 `tests` 目录，如下所示：

```
meanjis-generator (~/Desktop/meanjis-generator)
app
  controllers
    articles.server.controller.js
    core.server.controller.js
    users.server.controller.js
  models
    article.server.model.js
    users.server.model.js
  routes
    articles.server.routes.js
    core.server.routes.js
    users.server.routes.js
  tests
    article.server.model.test.js
    user.server.test.js
  views
    404.server.view.html
    500.server.view.html
    index.server.view.html
    layout.server.view.html
```

所有文件的命名都带有 `server` 后缀；这方便了团队工作并变得具有高度的可扩展性。`public` 文件夹包含所有与前端应用程序相关的文件。注意，每个模块都有自己的文件夹，此外还有存放在 `lib` 文件夹中的所有 AngularJS 文件。每个模块都有其各自文件夹的内部结构：`config`、`controllers`、`services`、`tests`、`views` 以及根目录下用于在应用程序中注册模块的文件，如下所示：

```
meanjis-generator (~/Desktop/meanjis-generator)
app
  config
  node_modules (library home)
  public
  modules
    articles
      config
      controllers
    services
    tests
    views
      articles.client.module.js
    core
    users
  application.js
  config.js
  humans.txt
  robots.txt
```

[ 129 ]

## 理解 Angular 视图和模型

我们不能说这是一个简单的结构。相反，它是一个复杂但划分良好的结构。最后，我们有 `config` 文件夹以及内部的另外两个：`env` 和 `strategy`；后者包含了 Passport 模块的配置文件，处理身份以及用户对 Facebook、Google、LinkedIn、Twitter 以及通过用户名和密码进行本地访问的控制。

`env` 目录持有 `all.js` 文件中的设置、静态文件访问、模板渲染和会话控制。其他文件存储了与数据库的连接以及社交网络 API 的访问密钥。

![](img/76faac513e4fd5843aeb56a44cada4c9_144_0.png)

我们现在将简要查看每个文件根目录的作用：

- `.bowerrc`: 正如我们在设置之前看到的，这是一个用于接收 Bower 组件的文件
- `.gitignore`: 此文件不跟踪当前版本中的文件
- `.bower.js`: 此文件为前端部分设置依赖项，如 Angular、jQuery 和 Bootstrap
- `.Gruntfile.js`: 此文件是用于构建、测试、开发和其他常用任务的任务运行器
- `.karma.conf.js`: 此文件设置测试环境
- `.license.md`: 此文件显示了使用了哪种许可证
- `.package.json`: 此文件设置服务器端的应用程序依赖，如 Express 和 Passport
- `procfile`: 为云部署设置一个环境
- `readme.md`: 包含关于应用程序的信息
- `server.js`: 正如我们之前看到的，这是应用程序 Node 服务器的核心

我们注意到，通过这种方式，我们可以以实际的方式扩展应用程序。正如我们在之前的示例所示，我们已经准备好进行重构。我们将其分为两个阶段：第一阶段 API，包括一个用于包含演讲者的服务；第二阶段使用 AngularJS 创建前端本身。

然而，我们可以选择从头开始创建，包括后端和前端的逐文件目录。但是，一旦你已经使用生成器创建了这种结构，请使用子生成器同时创建两个步骤（后端和前端文件）。这样我们可以节省时间并提高生产率。

# 重构 API

让我们看看如何借助子生成器 `CRUD` 同时创建这两者

1. 在终端中，输入以下命令：

```bash
yo means:crud-module speakers
```

注意最后一个单词是我们要赋予将创建的模块的名称。

> 关于 MEAN.JS 生成器和子生成器 CRUD 的更多信息可以在 http://meanjs.org/generator.html#crud-module 找到。

处理完成后，我们在终端中需要包含以下内容：

```text
[?] Which supplements would you like to include in your angular module? directives, filters
[?] Would you like to add the CRUD module to a menu? Speakers
create app/controllers/speakers/server.controller.js
create app/modules/server/server.module.js
create app/routes/speakers/server.routes.js
create public/routes/speakers/test/client.routes.js
create public/modules/speakers/controllers/client.controller.js
create public/modules/speakers/services/client.service.js
create public/modules/speakers/tests/tests/client.controller.test.js
create public/modules/client/config/client.config.js
create public/modules/speakers/views/create-speaker.view.html
create public/modules/speakers/views/edit-speaker.view.html
create public/modules/speakers/views/list-speakers.client.view.html
create public/modules/speakers/views/view-speaker.client.view.html
create public/modules/speakers/speakers.module.js.
```

## 理解 Angular 视图和模型

注意，在创建新模块时，我们回答了三个可选问题：我们是否想要包含一个 CSS 和图像的文件夹，以及两个用于 Angular 指令和过滤器的目录。为了本示例的目的，我们选择不包含 CSS 和图像目录；稍后我们会看到原因。

> 每次当你需要在浏览器中测试某些内容时，不要忘记使用 `node server` 命令保持服务器运行；如果没有运行，请使用 `nodemon`。

2. 现在，让我们测试一下我们创建的内容。打开浏览器并输入 `localhost:3000`。如果你使用的是 MEAN.JS 生成器的 0.1.5 版本，你可能会收到以下错误：

```text
Error: Menu does not exist
http://localhost:3000/modules/core/services/menus.client.js:35&host=localhost:3000
```

这个小 bug 将将在下一个版本中修复，但现在我们手动解决它。

3. 打开 `speaker.client.config.js` 文件。

```javascript
// 配置 模块并替换以下代码
angular.module('speakers').run(['Menus',
function (Menus) {
  // 设置顶部栏菜单项
Menus.addMenuItem('Speakers', 'Speakers', 'speakers',
  'dropdown', '/speakers/create');
  Menus.addSubMenuItem('Speakers', 'speakers', 'List
Speakers', 'speakers');
  Menus.addSubMenuItem('Speakers', 'speakers', 'New
Speaker', '/speakers/create');
}
]);
```

4. 用以下代码替换先前的代码：

```javascript
// 配置 Speakers 模块
angular.module('speakers').run(['Menus',
function (Menus) {
  // 设置顶部栏菜单项
Menus.addMenuItem('topbar', 'Speakers', 'speakers',
  'dropdown', '/speakers/create');
  Menus.addSubMenuItem('topbar', 'speakers', 'List
Speakers', 'speakers');
  Menus.addSubMenuItem('topbar', 'speakers', 'New Speaker',
  'speakers/create');
}
]);
```

我们将 `Menus` 函数的第一个参数从 `Speakers` 更改为 `topbar`，非常简单。

5. 返回终端再次使用 `node server` 命令。打开浏览器并输入 `localhost:3000`，然后登录或注册新用户。

最后，我们可以看到创建了演讲者菜单项，以及用于列出和添加演讲者的子菜单。这个子生成器与 Ruby on Rails 的 scaffold 非常相似，尽管我们用它来创建必要的 CRUD 操作，但我们仍有大量工作要做。

我们将对布局进行一些更改；重要的部分将突出显示：

1. 编辑位于 `public/core/views/home.client.view.html` 的首页视图模板文件。
2. 打开文件并删除所有内容。之后，将以下代码放入代码中；它们指示了我们应用程序的关键区域：

```html
<section data-ng-controller="HomeController" data-ng-init="find()">
  <div class="row">
    <div class="jumbotron text-center">
      <div class="row">
        <div class="col-md-6 col-md-offset-3 col-sm-6 col-sm-offset-3 col-xs-12">
          <h1>Conference</h1>
        </div>
      </div>
    </div>
    <br>
    <br>
    <div class="row">
      <p class="lead">
        使用 MEAN 的开放会议 应用。
      </p>
    </div>
    <div class="row">
      <p>
        <a class="btn btn-primary btn-lg" href="#!/signup">征稿中</a>
      </p>
    </div>
  </div>
</section>
```

## 理解 Angular 视图与模型

```html
  </div>
</div>
<section>
  <div class="page-header">
    <h1>Speakers</h1>
  </div>
  <div class="list-group">
    <!-- 添加过滤器以按创建日期列出演讲者 -->
    <a data-repeat="speaker in speakers" | filter:query orderBy: 'created' data-ng-href="/speakers/{{speaker.id}}" class="list-group-item">
      <img data-repeat-src-once src="{{speaker.email}}" class="list-group-item" style="float:left;margin-right: 10px;">
      <span data-ng-bind="speaker.name"></span>
      <h4 class="list-group-item text-primary"></h4>
      Track: <span data-ng-bind="speaker.title"></span>
      <p>Description: <span data-ng-bind="speaker.description"></span></p>
      <p class="list-group-item">Time: <span data-ng-bind="speaker.schedule"></span></p>
    </a>
  </div>
  <!-- 如果还没有任何演讲者则显示一条简单的消息 -->
  <div class="alert alert-warning text-center" data-ng-hide="{{speakers.resolved || speakers.length}}
    还没有演讲者，你为什么不
    <a href="/speakers/create">创建一个呢？</a>
  </div>
</section>
</section>
<footer>
  <p class="text-center">Conference &copy; 2014</p>
</footer>
```

让我们检查一下前面的代码：

- 带有 `data-ng-init="find()"` 的第一行初始化 `find()`；该数据属性对某些 HTML5 验证器非常有用。
- `ng-init` 内部的 `find()` 函数只是一个列出所有演讲者的函数。
- `ng-repeat` 指令具有另一个 AngularJS 关键字，过滤器功能，我们在第 5 章《开始使用 AngularJS》中见过它。
- `img gravatar-src-once="speaker.email"` 指令是 `angular-gravatar-hide::$resolved || speakers`，我们将在下一节看到它。
- `data-ng-hide="$speakers.resolved || speakers.length"` 指令在没有注册演讲者时会激活错误消息。

3. 编辑身份验证重定向。因此，打开位于 `public/modules/users/controllers/authentication.client.controller.js` 的文件，并找到紧随 `$scope.authentication.user = response;` 之后的 `$scope.authentication` 行。

```javascript
// 重定向到首页
$location.path('/speakers');
```

4. 通过此更改，登录页面后，我们被引导到演讲者页面而不是首页。完整函数如下：

```javascript
$scope.sign = function() {
  $http.post('/auth/sign/', $scope.credentials).success(function(response) {
    // 如果成功，我们将响应分配给全局用户模型
    $scope.authentication.user = response;

    // 重定向到首页
    $location.path('/speakers');
  }).error(function(response) {
    $scope.error = response.message;
  });
};
```

5. 编辑首页控制器。因此，打开 `public/modules/controllers/home.client.controller.js` 文件。
6. 在 `$scope.authentication = Authentication;` 之后添加以下行。

```javascript
// 查找演讲者列表
$scope.find = function() {
  $scope.speakers = Speakers;
};
```

7. 在控制器中添加以下行：

```javascript
angular.module('core').controller('HomeController', ['Speakers'], function($scope, Authentication) {
  // 查找演讲者列表
  $scope.find = function() {
    $scope.speakers = Speakers;
  };
});
```

让我们检查前面的代码：位于 `public/core/views/home.client.view.html` 的首页视图模板文件。

## 理解 Angular 视图与模型

让我们检查前面的代码：位于 `public/core/views/home.client.view.html` 的首页视图模板文件。

```html
<form class="form-horizontal" data-ng-submit="update()"
  novalidate>
<fieldset>
  <div class="form-group">
    <label class="control-label"
      for="name">姓名</label>
    <div class="controls">
      <input type="text" data-ng-model="speaker.name"
        id="name" class="form-control"
        placeholder="姓名" required>
    </div>
  </div>
  <div class="form-group">
    <label class="control-label"
      for="title">标题</label>
    <div class="controls">
      <input type="text"
        data-ng-model="speaker.title"
        id="title" class="form-control"
        placeholder="标题" required>
    </div>
  </div>
  <div class="form-group">
    <label class="control-label"
      for="description">描述</label>
    <div class="controls">
      <textarea data-ng-model="speaker.description"
        id="description" class="form-control"
        placeholder="描述" required></textarea>
    </div>
  </div>
  <div class="form-group">
    <label class="control-label"
      for="email">邮箱</label>
    <div class="controls">
      <input type="text"
        data-ng-model="speaker.email"
        id="email" class="form-control"
        placeholder="邮箱" required>
    </div>
  </div>
  <div class="form-group">
    <label class="control-label"
      for="schedule">日程</label>
    <div class="controls">
<input type="text" data-ng-
  model="speaker.schedule" id="schedule"
  class="form-control" placeholder="日程"
  required>
    </div>
  </div>
  <div class="form-group">
    <input type="submit" value="更新" class="btn
  btn-success">
  <a class="btn btn-danger"
    data-ng-click="remove();">删除</a>
  </div>
  <div data-ng-show="error" class="text-danger">
    <strong data-ng-bind="error"></strong>
  </div>
</fieldset>
</form>
</div>
</section>
```

在这里，我们使用 Angular 表达式 `<img gravatar-src-once="email" alt="{{speaker.name}}">` 将演讲者的姓名插入到图像属性中。

7. 编辑位于 `public/modules/views/create-speakers.client.view.html` 的文件，并将代码替换为以下代码：

```html
<section data-ng-controller="SpeakersController">
<div class="page-header">
  <h1>新增演讲者</h1>
</div>
<div class="col-md-12">
  <img gravatar-src-once="email" alt="{{name}}">
  <form class="form-horizontal" data-ng-submit="create()"
novalidate>
  </fieldset>
  <div class="form-group">
    <label class="control-label"
    for="name">姓名</label>
    <div class="controls">
      <input type="text" data-ng-model="name"
      id="name" class="form-control"
      placeholder="姓名" required>
    </div>
  </div>
</div>
```

```html
<div class="form-group">
  <label class="control-label" for="title">标题</label>
  <div class="controls">
    <input type="text" data-ng-model="title" id="title" class="form-control" placeholder="标题" required>
  </div>
</div>
<div class="form-group">
  <label class="control-label" for="description">描述</label>
  <div class="controls">
    <textarea data-ng-model="description" id="description" class="form-control" placeholder="描述" required></textarea>
  </div>
</div>
<div class="form-group">
  <label class="control-label" for="email">邮箱</label>
  <div class="controls">
    <input type="text" data-ng-model="email" id="email" class="form-control" placeholder="邮箱" required>
  </div>
</div>
<div class="form-group">
  <label class="control-label" for="schedule">日程</label>
  <div class="controls">
    <input type="text" data-ng-model="schedule" id="schedule" class="form-control" placeholder="schedule" required>
  </div>
</div>
<div class="form-group">
  <input type="submit" class="btn btn-default">
</div>
<div data-ng-show="error" class="text-danger">
  <strong data-ng-bind="error"></strong>
</div>
</fieldset>
</div>
</section>
```

创建表单来自 `<img gravatar-src-once="email" alt="{{name">>`，因为在这里我们还没有演讲者；所以——

8. 编辑 `public/modules/views/view-speakers.client.view.html` 文件并替换代码为：

```html
<section data-ng-controller="SpeakersController">
<div class="page-header">
  <h1>新增演讲者</h1>
</div>
<div class="row">
<img gravatar-src-once="email" alt="{{speaker.name}}">
<div class="col-md-12">
<form class="form-horizontal" data-ng-submit="update()"
novalidate>
  </fieldset>
  <div class="form-group">
    <label class="control-label"
      for="name">姓名</label>
    <div class="controls">
      <input type="text" data-ng-model="speaker.name"
        id="name" class="form-control"
        placeholder="姓名" required>
    </div>
  </div>
  <div class="form-group">
    <label class="control-label"
      for="title">标题</label>
    <div class="controls">
      <input type="text" data-ng-model="speaker.title"
        id="title" class="form-control"
        placeholder="标题" required>
    </div>
  </div>
  <div class="form-group">
    <label class="control-label"
      for="description">描述</label>
    <div class="controls">
      <textarea data-ng-model="speaker.description"
        id="description" class="form-control"
        placeholder="描述" required></textarea>
    </div>
  </div>
  <div class="form-group">
    <label class="control-label"
      for="email">邮箱</label>
    <div class="controls">
      <input type="text"
        data-ng-model="speaker.email"
        id="email" class="form-control"
        placeholder="邮箱" required>
    </div>
  </div>
  <div class="form-group">
    <label class="control-label"
      for="schedule">日程</label>
    <div class="controls">
<input type="text" data-ng-
  model="speaker.schedule" id="schedule"
  class="form-control" placeholder="日程"
  required>
    </div>
  </div>
  <div class="form-group">
    <input type="submit" value="更新" class="btn
  btn-success">
  <a class="btn btn-danger"
    data-ng-click="remove();">删除</a>
  </div>
  <div data-ng-show="error" class="text-danger">
    <strong data-ng-bind="error"></strong>
  </div>
</fieldset>
</form>
</div>
</section>
```

创建表单来自 `<img gravatar-src-once="email" alt="{{name">>`，因为在这里我们还没有演讲者；所以——

9. 编辑 `app/models/speaker.js` 文件并替换代码为：

```javascript
'use strict';

/**
 * 模块依赖
 */
var mongoose = require('mongoose');
var Schema = mongoose.Schema;

/**
 * 演讲者 Schema
 */
var SpeakerSchema = new Schema({
  name: {
    type: String,
    trim: true,
    required: '姓名不能为空'
  },
```

```html
<section>
<div class="page-header">
  <h1>新增演讲者</h1>
</div>
<div class="col-md-12">
<img gravatar-src-once="email" alt="{{speaker.name}}">
<div class="caption">演讲者</div>
<div class="col-md-12">
<form class="form-horizontal" data-ng-submit="create()"
novalidate>
  </fieldset>
  <div class="form-group">
    <label class="control-label"
    for="name">姓名</label>
    <div class="controls">
      <input type="text" data-ng-model="name"
      id="name" class="form-control"
      placeholder="姓名" required>
    </div>
  </div>
</div>
```

```html
<div class="form-group">
  <label class="control-label" for="title">标题</label>
  <div class="controls">
    <input type="text" data-ng-model="title" id="title" class="form-control" placeholder="标题" required>
  </div>
</div>
<div class="form-group">
  <label class="control-label" for="description">描述</label>
  <div class="controls">
    <textarea data-ng-model="description" id="description" class="form-control" placeholder="描述" required></textarea>
  </div>
</div>
<div class="form-group">
  <label class="control-label" for="email">邮箱</label>
  <div class="controls">
    <input type="text" data-ng-model="email" id="email" class="form-control" placeholder="邮箱" required>
  </div>
</div>
<div class="form-group">
  <label class="control-label" for="schedule">日程</label>
  <div class="controls">
    <input type="text" data-ng-model="schedule" id="schedule" class="form-control" placeholder="schedule" required>
  </div>
</div>
<div class="form-group">
  <input type="submit" class="btn btn-default">
</div>
<div data-ng-show="error" class="text-danger">
  <strong data-ng-bind="error"></strong>
</div>
</fieldset>
</div>
</section>
```

创建表单来自 `<img gravatar-src-once="email" alt="{{name">>`，因为在这里我们还没有演讲者；所以——

8. 编辑 `view-speakers.client.view.html` 文件并替换代码为：

```html
<section>
<div class="page-header">
  <h1>新增演讲者</h1>
</div>
<div class="row">
<div class="col-md-12">
<img gravatar-src-once="email" alt="{{speaker.name}}">
<div class="caption">演讲者</div>
<div class="col-md-12">
<form class="form-horizontal" data-ng-submit="update()"
novalidate>
  </fieldset>
  <div class="form-group">
    <label class="control-label"
      for="name">姓名</label>
    <div class="controls">
      <input type="text" data-ng-model="speaker.name"
        id="name" class="form-control"
        placeholder="姓名" required>
    </div>
  </div>
  <div class="form-group">
    <label class="control-label"
      for="title">标题</label>
    <div class="controls">
      <input type="text" data-ng-model="speaker.title"
        id="title" class="form-control"
        placeholder="标题" required>
    </div>
  </div>
  <div class="form-group">
    <label class="control-label"
      for="description">描述</label>
    <div class="controls">
      <textarea data-ng-model="speaker.description"
        id="description" class="form-control"
        placeholder="描述" required></textarea>
    </div>
  </div>
  <div class="form-group">
    <label class="control-label"
      for="email">邮箱</label>
    <div class="controls">
      <input type="text"
        data-ng-model="speaker.email"
        id="email" class="form-control"
        placeholder="邮箱" required>
    </div>
  </div>
  <div class="form-group">
    <label class="control-label"
      for="schedule">日程</label>
    <div class="controls">
<input type="text" data-ng-
  model="speaker.schedule" id="schedule"
  class="form-control" placeholder="日程"
  required>
    </div>
  </div>
  <div class="form-group">
    <input type="submit" value="更新" class="btn
  btn-success">
  <a class="btn btn-danger"
    data-ng-click="remove();">删除</a>
  </div>
  <div data-ng-show="error" class="text-danger">
    <strong data-ng-bind="error"></strong>
  </div>
</fieldset>
</form>
</div>
</section>
```

创建表单来自 `<img gravatar-src-once="email" alt="{{name">>`，因为在这里我们还没有演讲者；所以——

9. 编辑 `app/models/speaker.js` 文件并替换代码为：

```javascript
  schedule: {
    type: String,
    default: ''
  },
  email: {
    type: String,
    default: ''
  },
  created: {
    type: Date,
    default: Date.now
  },
  user: {
    type: Schema.ObjectId,
    ref: 'User'
  }
});

mongoose.model('Speaker', SpeakerSchema);
```

在 MongoDB 中，我们看到创建的演讲者数据：

```json
{
  "v": 0,
  "id", "description": "Lorem ipsum sit amet, consectetur elit",
  "email": "",
  "name": "John Master",
  "schedule": "10:00",
  "title": "MongoDB",
  "user": "54034f440c486ebb02859677"
}
```

我们的重构工作是巨大的，但正如之前所说的，即使使用了 CRUD 生成器，仍然有大量工作要做。

10. 最后，在演讲者模型中插入必要的字段，它们将存储在数据库中。

> 注意：你需要运行应用程序并登录，才能在 Postman 中输入数据。稍后我们将介绍如何在不登录的情况下传递凭据。

按照以下步骤在我们的 API 中插入数据：

1. 你可以在右侧的字段中输入任何数据，但左侧的字段必须与演讲者 Schema 中的字段名称相同：

![](img/76faac513e4fd5843aeb56a44cada4c9_159_0.png)

2. 打开浏览器并输入 http://localhost:3000/

登录后，你可以看到应用程序的演讲者页面以及从演讲者模块导入的缩略图。当你在邮箱字段中填写有效的邮箱地址时，将有一个演讲者照片。如果留空，则显示默认的 Gravatar 图标，如下所示：

![](img/76faac513e4fd5843aeb56a44cada4c9_160_0.png)

![](img/76faac513e4fd5843aeb56a44cada4c9_161_0.png)

请注意此操作所需的凭据位于 Cookies 选项卡中，如下截图所示。

如果你尝试在未登录的情况下使用 Postman 执行相同的操作，你将收到一条“此用户未登录（this User is not logged in）”的消息。

![](img/76faac513e4fd5843aeb56a44cada4c9_161_1.png)

这非常有用，因为你不需要登录即可进行应用程序测试并填充数据库。我们只需要一个有效的会话 cookie。

# 总结

在 SPA 的世界里又一次之旅；在本章中，我们看到了了代码生成器的最佳用例。

我们分析了使用服务器端 JavaScript 和前端的大型应用程序的结构。

我们使用 AngularJS 重构了整个前端，应用了我们在上一节中看到的关键概念，如指令（`directives`）和过滤器（`filters`）。

我们还学习了如何使用 Webstorm IDE 基于 RESTful Web 服务对应用程序进行测试。

在下一章中，我们将看到使用 Angular 进行测试的重要性和架构，以及如何使用和配置 Karma 和 Protractor 等。

# 第 7 章：使用 Karma 和 Protractor 测试 Angular SPA

在本章中，我们将更深入地探讨 AngularJS 框架，并理解关于 SPA 测试的一些非常重要的要点。

正如我们在前几章中提到的，SPA 将 MVC 责任转移给了在客户端（浏览器）运行的 JavaScript。我们必须像处理服务器端语言中的 MVC 一样来编写测试。

AngularJS 框架的设计具有高度的可测试性，正因如此，我们有一些工具可以促进这一过程。今天，编写测试用例是每个程序员（无论前端还是后端）Web 开发过程的一部分。测试驱动开发是所有敏捷方法论的一部分，你应该记住这一点。越早开始编写测试，对你就越有利。

在接下来的章节中，我们将看到一些测试的基本概念，例如单元测试和集成测试（称为 e2e 测试）等。具体内容如下：

- 测试概念
- 介绍 Jasmine
- 配置 Karma（单元测试）
- 运行 Karma 测试
- 配置 Protractor（e2e 测试）
- 运行 Protractor 测试

## 测试概念

让我们关注示例应用程序中将涵盖的两类测试：单元测试和 e2e 测试。这里有一个值得注意的有趣事实：以前大多数前端开发人员并不担心测试。测试专门由测试团队或质量保证部门完成。然而，现实情况现在已经改变了。现在很难找到具备基础 JavaScript 知识的测试人员来对 SPA 进行必要的测试。当我提到测试时，指的是自动化测试。我们考虑自动化测试的原因是，当你的应用程序从中等规模变为大规模时，要用新的实现测试所有接口将变得非常复杂。

目前，前端开发者更关注如何编写 JavaScript，以及如何应用测试驱动开发（TDD）和行为驱动开发（BDD）的概念。

下面的图说明了 TDD 的工作流：

![](img/76faac513e4fd5843aeb56a44cada4c9_164_0.png)

TDD 的概念与极端编程（extreme programming）的技术直接相关，开发者为给定的功能创建小型测试用例，然后实现代码来响应并通过测试。这种模式与单元测试直接相关；当然，关于单元测试和 TDD 还有许多其他内容，但理解这些术语对于理解其重要性已经足够了。此外，单元测试可以帮助开发者专注于真正重要的事情。

另一方面，我们有 BDD（广泛用于敏捷软件开发），它允许将整个团队的开发者和业务人员整合在一起。它不使用技术语言来描述系统接口的预期行为。

核心思想是编写小的测试块，并编写必要的代码以通过测试。这种程序在敏捷开发中至关重要，因为代码必须具有可读性以便于维护并易于扩展。

单元测试对于测试小型代码块非常有用，但我们需要对所有这些小代码块集合进行测试，并且当我们需要思考接口预期的行为时。为此，我们使用 e2e 测试。因此，带测试编写代码的主要目的是产生易于维护、人类可理解、可调试且无 bug 的。

虽然这对于前端开发人员来说不是日常实践，但在通用的软件开发中，TDD 是非常有用的。在运行任何 MVC 或 MVVM 模式时，它极其适用。

那么，让我们看看如何在我们的 SPA 上实现测试。

Angular 框架在构建和规划时就考虑了测试，因此在框架选择方面我们有很多选项可选。接下来的示例将介绍 Karma 和 Protractor 测试运行器。

## 介绍 Jasmine

Karma 是最常用的测试执行工具之一；它兼容许多测试框架（如 Mocha、QUnit 和 Jasmine）。你可以用它测试任何 JavaScript 代码，并且强烈建议你使用某些工具对 SPA 进行自动化测试。

在接下来的示例中，我们将使用 Jasmine 编写测试并使用 Karma 运行测试。Jasmine 拥有非常简单易于编写的语法。

```javascript
describe("Test name", function() {
  it("contains expectation", function() {
    expect(true).toBe(true);
  });
});
```

# 使用 Karma 和 Protractor 测试 Angular SPA

`describe()` 和 `it()` 是两个函数。`describe()` 有一个接收名称的字符串参数和一个实现它的函数参数。

```javascript
describe("Test name", function() {
  it("contains expectation", function() {
    expect(true).toBe(true);
  });
});
```

Jasmine 的 API 非常容易理解；它还有许多其他函数，但这些对于理解示例足够了。

> 要了解更多关于 Jasmine 的信息，请参考 http://jasmine.github.io/

## 配置 Karma（单元测试）

让我们来看看 Karma 运行器以及如何使用它。

> 我们不会涵盖安装 Karma 及其模块的必要步骤：你可以从示例下载整个项目并

创建此文件最简单的方法是使用 `karma-cli` 工具。这样，你就可以在终端中使用 `init` 命令。这是许多可用 Node.js 工具（如 Grunt、Bower 等）使用的标准程序。

**命令行界面 (CLI)** 帮助我们通过终端以简单快速的方式创建文件和设置。由于我们已经有了 `karma.conf.js` 文件，所以不需要执行 `init` 命令。

打开项目文件夹。现在，让我们查看 `karma.conf.js` 文件并逐行理解它：

```javascript
'use strict';

/**
* 依赖。
 */
var applicationConfiguration = require('./config/config');

// Karma 配置
module.exports = function(config) {
  config.set({
    // 使用的框架
    frameworks: ['jasmine'],
  });
});
```

# 使用 Karma 和 Protractor 测试 Angular SPA

```javascript
// 加载到浏览器中的文件列表 / 模式
files: applicationConfiguration.assets.lib.js.concat(applicationConfiguration.assets.js, applicationConfiguration.assets.tests),
```

```javascript
// 要使用的测试结果报告器
可能的值：'dots', 'progress', 'junit', 'growl',
'coverage'
reporters: ['progress'],
```

```javascript
// Web 服务器端口
port: 9876,
```

```javascript
// 启用/禁用输出中的颜色（报告器和日志）
colors: true,
```

```javascript
// 日志级别
可能的值：config.LOG_DISABLE || config.LOG_ERROR ||
config.LOG_WARN || config.LOG_INFO || config.LOG_DEBUG
logLevel: config.LOG_INFO,
```

```javascript
// 启用/禁用监听文件并在每次发生变化时执行测试
autoWatch: true,
```

```javascript
// 启动这些浏览器，当前可用的：
- Chrome
- ChromeCanary
- Firefox
- Opera
- Safari (仅 Mac)
- PhantomJS
- IE (仅 Windows)
browsers: ['PhantomJS'],
```

```javascript
// 如果浏览器在指定的超时 [ms] 内未捕获，将其杀死
captureTimeout: 60000,
```

```javascript
// 持续集成模式
// 如果为 true，它将捕获浏览器、运行测试并退出
singleRun: true
});
```

高亮的代码告诉 Karma 测试文件的位置，以及是否与后续代码相同：

```javascript
// 加载到浏览器中的文件列表 / 模式
files: [
  'public/**.test.js'
];
```

`applicationConfiguration` 变量在 Karma 函数之前通过以下代码进行了设置：

```javascript
var applicationConfiguration = require('./config/config');
```

请注意，我们正在使用 Jasmine 框架，正如我们之前提到的。此时，我们已经有了开始编写测试的必要基准。

## 检查器控制器测试

我们注意到所有模块都有各自的名为 `tests` 的文件夹。这是因为当我们使用 Yeoman 生成器时，它已经创建了这些配置。如之前所示，控制器、服务、指令和测试所需的所有文件已经存储在其中。因此，我们已经准备好了测试的样板代码。

然后，我们将检查是否可以修复我们执行的操作。打开 `public/modules/speakers/tests/` 下的文件 `speakers.client.controller.test.js`。

我们将讨论一些代码块，以便逐步理解正在发生什么。然后，我们将插入原始文件中不存在的额外注释，以理解代码中每个部分正在发生什么。此外，我们将使用之前在 Jasmine 介绍部分看到过的相同概念。`describe()` 函数接收测试名称和一个带有测试本身的函数参数，如下代码所示：

```javascript
(function() {
  // 扬器控制器规格说明
  describe('Speakers Controller Tests', function() {
    // 初始化全局变量
    var SpeakersController,
    scope,
    $HttpBackend,
    $StateParams,
    $location;
  });
});
```

# 使用 Karma 和 Protractor 测试 Angular SPA

在这个函数中，我们初始化了一些全局变量。注意我们使用 `$` 符号来设置 Angular 特性（例如 `$backend`、 `$stateParams` 和 `$location`）。`$resource` 服务为响应对象增强了用于更新和删除资源的方法。如果我们使用标准的 `toBe` 匹配器，我们的测试将失败，因为值将与响应完全匹配。为了解决这个问题，我们定义了一个新的 Jasmine `toBeData` 匹配器。当 `toBeData` 匹配器比较两个对象时，它只考虑对象的属性而忽略方法，如下代码所示：

```javascript
beforeEach(function() {
  jasmine.addMatchers({
    toBeData: function(util, customEqualityTesters) {
      return {
        compare: function(actual, expected) {
          pass: angular.equals(actual, expected)
        }
      };
    }
  });
});
```

```javascript
// 我们可以从加载主模块开始
beforeEach(module
(ApplicationConfiguration.applicationModuleName));
```

```javascript
// 注入器在这里忽略前后的下划线
（即 `_$HttpBackend`）
// 这允许我们注入一个服务，然后将其附加到与服务同名的变量上
beforeEach(inject(function($controller, $rootScope,
$location, _$stateParams, _$httpBackend) {
  // 设置一个新的全局作用域
  scope = $rootScope.$new();
```

```javascript
// 将全局变量指向注入的服务
$stateParams = _$stateParams;
$httpBackend = _$httpBackend;
$location = _$location_;
```

```javascript
// 初始化 Speakers 控制器。
SpeakersController = $controller('SpeakersController', {
  scope: scope
}));
```

# 第 7 章

在这里，注意 `beforeEach()` 函数的使用。这个名字非常直观；我们使用此函数在每个测试之前启动某些程序。在代码示例中第一次使用 `beforeEach()` 函数是添加新的匹配器 `toEqualData`，第二次使用是加载应用程序配置，第三次使用是注入 AngularJS 指令。

现在，我们使用 `it()` 函数来描述我们对测试的期望；高亮的字符串显示了这一点：

```javascript
it('$scope.find() should create an array with at least one Speaker
object fetched from XHR')
```

## 使用 Karma 和 Protractor 测试 Angular

```javascript
// 定义一个示例 Speaker 对象
var sampleSpeaker = new Speakers({
  name: 'New Speaker',
title: '',
description: '',
email: '',
nschedule: ''
});
```

3. 使用以下代码将属性（即 title、description、email 和 schedule）添加到之前的 `sampleSpeaker` 对象中：

```javascript
// 设置 URL 参数
$stateParams.speakerId = '525a8422f6d087f0e407a333';

// 设置 GET 响应
$httpBack.expectGET(/speakers/\([0-9a-fA-F]+\/).respond(sampleSpeaker);

// 运行控制器功能
scope.findOne();
$httpBack.flush();

// 测试 scope 的值
expect(scope.speaker).toEqualData(sampleSpeaker);
));
```

4. `it()` 函数用于创建一个 speaker：

```javascript
it('$scope.create() with valid form data should send a POST request with the form input values and then locate to new object URL', inject(function(Speakers) {
// 创建一个示例 Speaker 对象
var sampleSpeakerData = new Speakers({
  name: 'New Speaker',
title: 'Title Test',
description: 'Description Test',
email: 'email@test.com',
nschedule: '11:00'
});

// 创建一个示例 Speaker 响应
var sampleSpeakerResponse = new Speakers({
  id: '525cf20451979dea2c00001',
  name: 'New Speaker',
  title: 'Title Test',
});
```

# 第 7 章

```javascript
description: 'Description Test',
email: 'email@test.com',
schedule: '11:00'
);
```

5. 使用之前的模拟输入值，将属性（即 title、description、email 和 schedule）添加到 `sampleSpeakerData` 对象和 `sampleSpeakerResponse` 对象中

```javascript
// 模拟输入值
scope.name = 'New Speaker';
scope.title = 'Title Test';
scope.description = 'Description Test';
scope.email = 'email@test.com';
scope.schedule = '11:00'
```

6. 使用以下代码将属性（即 title、description、email 和 schedule）添加到固具模拟表单中：

```javascript
// 设置 POST 响应
$HttpBackend.expectPOST('speakers',
sampleSpeakerData).respond(sampleSpeakerResponse);
```

```javascript
// 运行控制器功能
scope.create();
$HttpBackend.flush();
```

```javascript
// 测试表单输入是否重置
expect(scope.name).toEqual('');
```

```javascript
// 测试 Speaker 创建后的 URL 重定向
expect(scope.location.path()).toBe('/speakers/' + 
sampleSpeakerResponse.id);
);
```

1. 下一个测试是更新用户，使用以下代码：

```javascript
it('$scope.update()) should update a valid Speaker',
inject(function(Speakers) {
// 定义一个示例 Speaker put 数据
var sampleSpeakerPutData = new Speakers({
  _id: '525cf20451979dea2c00001',
```

## 使用 Karma 和 Protractor 测试 Angular

name: 'New Speaker',

title: 'Update the Text',

description: 'Update the Description',

email: 'update@test.com',

schedule: '10:00'

2. 将属性 `title`, `description`, `email` 和 `schedule` 添加到 `sampleSpeakerPutData` 对象中，如之前的高亮代码所示：

```javascript
// Mock Speaker in scope
scope.speaker = sampleSpeakerPutData;

// Set PUT response
$httpBackend.expectPUT(/speakers\/([0-9a-f-F]{24})$$/).respond();
```

```javascript
// Run controller functionality
scope.update();
$httpBackend.flush();

// Test URL location to new object
expect($location.path()).toBe('/speakers/' + sampleSpeakerPutData_.id);
```

3. 最后一个 `it()` 函数用于删除演讲者：

```javascript
it('$scope.remove() should send a DELETE request with a valid speakerId and remove the Speaker from the scope',
inject(function() {
  // Create new Speaker object
varvar sampleSpeaker = new Speaker({
  id: '525a8422ff6d0f7fe4e0a733'
}));
```

```javascript
// Create new Speakers array and include the Speaker
scope.speakers = [sampleSpeaker];
```

```javascript
// Set expected DELETE response
$httpBackend.expectDELETE(/speakers\/([0-9a-f-F]{24})$$/).respond(204);
```

```javascript
// Run controller functionality
scope.remove(sampleSpeaker);
$httpBackend.flush();
```

```javascript
// Test array after successful delete
expect(scope.speakers.length).toBe(0);
}}
```

此时，我们已经复习了测试演讲者控制器中 CRUD 操作的所有必要函数。此外，我们添加了缺失的代码，以测试在上一章中添加的所有属性（在上一章中创建了新的演讲者控制器）。

由于我们使用了 MEAN.JS 生成器，因此不需要为其他控制器（articles, core 和 users）编写测试。别担心；应用于演讲者控制器的步骤与这些文件相同。现在，让我们看看如何使用 Karma 运行这些测试。

## 运行 Karma 测试

再次注意，由于使用了 MEAN.JS 生成器，我们不需要配置运行 Karma 的任务；只需要触发 Grunt.js 任务来为我们完成工作。请执行以下步骤：

1. 在项目根目录下打开终端并输入以下命令：

   `grunt test`

2. 由于我们使用了 `grunt-karma` 插件，我们只需要在 Gruntfile 中以下代码写入 Karma 任务：

   ```javascript
   karma: {
     unit: {
       configFile: 'karma.conf.js'
     }
   }
   ```

# 使用 Karma 和 Protractor 测试 Angular SPA

3. 你应该运行命令行来启动 MongoDB。虽然我们使用 Compose.io 平台来运行测试，但由于我们使用了示例应用程序，我们需要一个本地数据库实例。这里是所有测试完成后远程服务器的截图：

```text
Application loaded using the "test" environment configuration
MEAN.js application started on port 3000
```

Article Model Unit Tests:

Method Save

✓ 能够无问题地保存

✓ 尝试在没有标题的情况下保存时应显示错误

Speaker Model Unit Tests:

Method Save

✓ 能够无问题地保存

✓ 尝试在没有名称的情况下保存时应显示错误

User Model Unit Tests:

Method Save

✓ 初始时没有用户

✓ 能够无问题地保存 (41ms)

✓ 再次保存已存在的用户时应失败 (79ms)

✓ 尝试在没有名字的情况下保存时应显示错误

```
8 passing (176ms)
```



```
Running "karma-unit" (karma) task
INFO (karma): Karma v12.3.2 server started at http://localhost:9876/
INFO [launcher]: Connected on socket VJoutUI13jkUGS with id 22658276
INFO PhantomJS 1.9.7 (Mac OS X): Executed 17 of 17 SUCCESS (0.019 secs / 0.118 secs)
```

我们可以看到所有测试都成功了，但我们也注意到 API 上成功执行了八项测试，而 karma 任务中执行了四项测试：

这是因为 `Grunt.js` 任务执行了 `Gruntfile.js` 文件中配置的所有测试。现在让我们看看如何完成演讲者模型的单元测试。

## 复习演讲者模型测试

添加以下代码行执行模型测试：

1. 打开 `app/tests/` 文件夹下的 `speaker.server.model.test.js`。让我们复习现有代码并添加必要的代码行来执行测试：

```javascript
'use strict';
```

```javascript
/**
 * Module dependencies.
 */
var should = require('should'),
mongoose = require('mongoose'),
User = mongoose.model('User'),
Speaker = mongoose.model('Speaker');
```

```javascript
/**
 * Globals
 */
var user, speaker;
```

```javascript
/**
 * Unit tests
 */
```

正如我们之前讨论过的，`describe()` 函数接收测试名称作为第一个参数，测试本身作为第二个参数。

> 你可以在 https://github.com/angular/protractor 找到关于 Protractor 的更多信息。Jasmine 同样兼容 Protractor，因为从浏览器中提取以执行测试的所有资源都是 promise。此外，Jasmine 的 `expect()` 在内部会处理这些 promise，并使验证测试变得透明化。

然而，MEAN.JS 生成器在默认安装中并不包含 Protractor。因此，让我们添加必要的依赖，以使用这个强大的框架开始测试。执行以下步骤：

1. 在项目根目录下打开终端并输入以下命令：

   `npm install protractor -save-dev`

2. 在 `grunt-protractor-runner` 文件夹中，在终端中打开 `node_modules/protractor/bin/webdriver-manager` 文件并输入以下命令：

   `update`

> 不要忘记路径 `grunt-protractor-runner/node_modules/protractor/bin/webdriver-manager`；我们稍后将在本节后面将使用它来运行 Selenium 服务器。

现在，让我们按照以下步骤在项目根目录下创建一个 Protractor 配置文件：

1. 添加 `protractor.conf.js` 文件并放入以下代码；这是一个在 AngularJS 项目中使用 Protractor 开始工作的良好模版：

```javascript
// Protractor configuration
// https://github.com/angular/protractor/blob/master/referenceConf.js

'use strict';
exports.config = {
  // 每个在浏览器上运行的脚本的超时时间。
  // 这应该比
  // 应用程序在任务之间稳定
  // 所需的最大时间长
  allScriptsTimeout: 110000,
}

/** **

# 使用 Karma 和 Protractor 测试 Angular SPA

- 使用 "seleniumAddress" 加快启动；
- 运行 `./node_modules/.bin/webdriver-manager start` 来启动 Selenium 服务器。
- 使用 "seleniumPort" 让 Protractor 管理它自己的 Selenium 服务器实例（使用默认位置的服务器 JAR 包）；
*/
seleniumAddress: 'http://localhost:4444/wd/hub',
seleniumPort: 4444,

```

```javascript
// 被测试应用程序的基础 URL。调用
// protractor.get()
// 使用相对路径时，将在前面加上此 URL。
baseURL: 'http://localhost:' + (process.env.PORT || '3000'),

// 如果为 true，则仅启动 chromedriver，而不是独立的
// selenium。
// 其他 chrome 浏览器的测试将不会运行。
chromeOnly: false,
```

```javascript
//chromedriver: 'node_modules/grunt-protractor-
// runner/node_modules/protractor/node_modules/selenium-
// webdriver/chromedriver',
// 要在浏览器中加载的文件列表/模式
specs: [
  'e2e/**/*.spec.js'
],
```

```javascript
// 要排除的模式。
exclude: [],

// 传递给 webdriver 实例的属性
//
```

```javascript
// 可用属性完整列表，请参见
// https://code.google.com/p/selenium/wiki/
DesiredCapabilities
// 以及

// https://code.google.com/p/selenium/source/browser/
// javascript/webdriver/capabilities.js
capabilities: {
```

# 第7章

```javascript
'browserName': 'chrome'
},
// --- 测试框架 -----/
// Jasmine 和 Cucumber 完全支持作为测试和
// 断言框架。
// Mocha 有有限的 beta 支持。如果你在使用 mocha，
// 你需要包含你自己的
// 断言框架。
framework: 'jasmine',
//
// --- 传递给 minijasminode 的选项 ---
// 完整列表请参见
// https://github.com/juliemr/minijasminode
jasmineNodeOpts:
  defaultTimeoutInterval: 30000
}
```

作为一个文档详尽的文件，我们不需要对每行代码进行深度分析，但高亮代码包含关于生成的 `seleniumAddress` 实例的重要信息，当我们在本节后面运行 webdriver manager 时。

2. 让我们向 Gruntfile 中添加 protractor 任务；只需在 Karma 任务之后添加以下行即可：

```javascript
protractor:
  options:
    configFile: 'protractor.conf.js'
  chrome:
    options:
      args:
        browser: 'chrome'
```

使用 Karma 和 Protractor 测试 Angular SPA

3. 在 Gruntfile.js 文件末尾的构建任务之后添加以下代码：

```javascript
// 测试任务。
grunt.registerTask('test', ['env:test', 'mochaTest', 'karma:unit', 'protractor']);
```

初始设置已完成，但我们需要创建测试文件。让我们看看现在需要做什么。

## 配置 e2e 测试文件夹

让我们将 e2e 测试文件夹添加到项目根目录。执行以下步骤：

1. 在应用程序根目录添加 e2e 测试文件夹。

2. 在 e2e 文件夹内部添加一个主文件夹。

3. 添加一个名为 `main.po.js` 的空文件。

4. 添加另一个名为 `main.spec.js` 的空文件。

e2e 目录结构应该如下：

![](img/76faac513e4fd5843aeb56a44cada4c9_184_0.png)

现在，让我们按照以下步骤为 `main.po.js` 和 `main.spec.js` 文件添加内容：

1. 从 e2e/main 文件夹打开 `main.po.js` 文件并添加以下行代码：

```javascript
'use strict';

var MainPage = function() {
  // 获取用于测试的元素
  this.heroEl = element(by.css('.jumbutton'));
  this.h1El = this.heroEl.element(by.css('h1'));
  this.anchorEl = this.heroEl.element(by.css('a'));

  this.repeater = by.repeater('speaker in speakers');
  this.speakerListCount = element.all(this.repeater).count();
}

module.exports = new MainPage();
```

在这里，我们只是获取了一些 UI 元素并使用 repeater 功能对 speaker 对象进行循环。

> 关于 Protractor API 和 repeater 方法的更多信息可以访问 http://angular.github.io/protractor/#api?view=ProtractorBy.prototype.repeater。

2. 现在，让我们从 e2e/main 文件夹为 `main.spec.js` 添加内容。复制以下代码并放入 `main.spec.js` 文件中：

```javascript
'use strict';

describe('Main View', function() {
  var page;

  beforeEach(function() {
    browser.get('/');
    page = require('./main.po');
  });
```

# 使用 Karma 和 Protractor 测试 Angular SPA

```javascript
// 第一个测试
it('should include name', function() {
  // 第一个断言 - 文本相等
  expect(page.h1El.getText()).toBe('Conference');
  // 第二个断言 - 锚点标签带有
  expect(page.anchorEl.getAttribute('href')).toBe('http://localhost:3000/signup');
});
```

等待，我看到 OCR 文本在代码块中间有一些痕迹。让我根据提供的文本流重新对齐逻辑。

（重新对齐第 185-186 页的代码块）

```javascript
// 第二个测试
it('should render speakerList', function () {
  // 第一个断言 - 期望包含 6 个 speaker 的 列表
  page.speakerListCount.then(function(count) {
    expect(count).toBe(6);
  });
});
```

再次，代码注释为我们的操作提供了必要的理解。

## 启动 Selenium 服务器

很好，我们已经有了配置 Selenium 服务器的所有步骤。让我们启动 Selenium 服务器并运行测试。执行以下步骤：

1. 打开终端并进入路径 `grunt-protractor-runner/node_modules/protractor/bin/` 输入以下命令：

```
webdriver-manager start
```

该命令将启动 Selenium 服务器，我们准备开始测试了。在进行 e2e 测试之前不要忘记运行应用程序！

2. 在根目录下打开终端并输入以下代码：

```bash
node server
```

3. 在终端输入以下命令启动测试：

```bash
grunt protractor
```

运行测试后，我们可以在终端中看到结果：

```
Running "protractor:chrome" (protractor) task
Using the selenium server at http://localhost:4444/wd/hub

Finished 11.643 seconds
2 tests, 4 assertions, 0 failures

Done, without errors..
```

注意任务是在 Chrome 浏览器中执行的，因为我们在 Grunt 中配置了 Chrome。

让我们通过以下步骤向 Gruntfile.js 添加另一个浏览器：

1. 在 gruntfile.js 的 protractor 任务中添加以下高亮代码：

```javascript
protractor: {
  options: {
    configFile: 'protractor.conf.js'
  },
  chrome: {
    options: {
      args: {
        browser: 'chrome'
      }
    }
  },
  safari: {
    options: {
      args: {
        browser: 'safari'
      }
    }
  }
}
```

## 使用 Karma 和 Protractor 测试 Angular

2. 再次运行测试并查看结果。

3. 在终端中，输入以下命令启动测试：

`grunt protractor`

下面的截图展示了在两个浏览器上运行的结果：

```
Running "protractor:chrome" (protractor) task
Using the selenium server at http://localhost:4444/wd/hub
...
Finished in 11.093 seconds
2 tests, 4 assertions, @ failures

Running "protractor:safari" (protractor) task
Using the selenium server at http://localhost:4444/wd/hub
Finished in 12.506 seconds
2 tests, 4 assertions, @ failures

Done, without errors.
```

该框架将测试 Gruntfile.js 中配置的每个浏览器。

但请记住，你需要在工作站上安装浏览器才能进行测试。

如你所见，浏览器会快速打开、运行测试并关闭。

## 总结

这是一个专注于测试的很长的章节；我们学习了如何在 SPA 上进行单元测试。我们还学习了一些测试框架来方便我们的工作。

你学习了如何使用 Protractor 框架和 Selenium 服务器对 AngularJS 进行测试。请记住，你应该彻底测试你的应用程序，以避免随着源代码的增长出现未来的问题。

在下一章节中，我们将看到如何将 SPA 部署到云服务。我们还将看到一些关于 SPA 及其可扩展性的有趣点。

# 8 将应用程序部署到云端

我们现在已经示例 SPA 章节开发的最后阶段，我们将查看涉及 Web 应用程序所有过程的重要点，例如版本控制、云端部署和持续应用程序部署。我们将涵盖以下主题：

- 在 GitHub 上托管项目

- 持续应用程序部署

- 从 GitHub 自动部署

- 手动部署

- 关于 SPA 的一些最终说明

## 在 GitHub 上托管项目

在进行云端部署之前，我们需要检查示例应用程序中的一些重要点。正如早之前提到的，我们需要将源代码托管在 `http://github.com`。由于我们已经使用 Git 作为版本控制系统，将代码上传到 GitHub 服务非常简单。

Git 是一个强大的版本控制系统，并拥有 Windows 和 Mac OS X 的许多 GUI 客户端。如果你使用的是 Mac OS X，我们建议使用 `https://mac.github.com/`，对于 Windows 用户，建议使用 `https://windows.github.com/`；两者都是免费工具。

在以下示例中，我们使用终端；为了在终端中使用可用 Git 命令，你需要在系统中安装 Git。

# 将应用程序部署到云端

> 你可以通过以下 URL 找到更多如何安装 Git 的信息：http://git-scm.com/.

我们已经配置好了一，只需要使用以下命令提交最后的更改：

```bash
git commit -m"refactoring adding Protractor testing Framework"
```

现在我们需要一个 GitHub 账户来存放源代码。如果你已经有一个账户了，请跳转到第 13 步。

1. 打开浏览器并访问 www.github.com 创建你的免费账户。注册完成后，你将被重定向到主屏幕；现在是时候创建一个仓库来存储源代码了。

2. 点击用户名右侧的 (+) 号，并在弹出菜单中点击“New repository”（新建仓库），如图所示：

![](img/76faac513e4fd5843aeb56a44cada4c9_190_0.png)

3. 你需要为新仓库提供名称和描述。如截图所示输入名称和描述：

| 所有者 | 仓库名称 |
| :--- | :--- |
| user name / conference-api | |
| 优秀的仓库（可选）简短且易记。petualant-octo-tyoirs 怎么样？ | |
| 描述（可选） | Learning Single Page Application |
| 公开 | 任何人都可以查看此仓库。你可以选择谁可以提交。 |
| 私有 | 你选择谁可以查看并提交此仓库。 |
| 使用 README 初始化此仓库 | 这将允许你立即 git clone 仓库。如果你已经在本地运行了 git clone，请跳过此步骤。 |
| 添加 .gitignore | 无 |
| 添加许可证 | 无 |

> 你可以通过 https://help.github.com/articles/create-a-repo/ 找到更多关于开始使用 GitHub 信息。

4. 现在是时候配置 Git 和 GitHub 之间的连接了。要做到这一点，请打开你的终端。

## 将应用程序部署到云端

### 从 GitHub 自动部署

正如前面提到的，在敏捷开发中每次交付结束时（或者按照常说的说法），我们需要将应用程序部署到生产环境。现在我们将看到如何以自动的方式实现这一操作。以下步骤假设你已经使用 Git 配置了本地仓库并拥有一个 GitHub 账户。

### 设置 Shippable

在 Shippable 上设置账户非常简单且免费。此外，你可以使用你的 GitHub 或 Bitbucket 账户。

1. 访问 http://www.shippable.com/ 并点击该按钮。然后按照说明进行注册。

2. 在 GitHub 和 Shippable 之间完成授权过程后，你将被重定向到 Shippable 仪表板。在右侧，点击下方截图所示的账户名称：

3. 然后点击仓库名称。启用你的 GitHub 仓库。到目前为止非常简单！不要忘记选择存储我们应用程序的仓库。此时，你可能已经注意到，可以通过点击播放符号直接从仪表板运行应用程序。然而，现在还没有运行应用程序的时机。我们仍然需要遵循一些步骤来正确设置环境。

### 设置 Heroku

Heroku 是一个支持多种编程语言的云服务平台（PaaS）。它是最古老的云服务之一，最初仅支持 Ruby。设置账户非常简单：访问 https://heroku.com/signup 并按照注册步骤操作：

1. 在仪表板上，点击 (+) 创建新应用并选择一个名称，如下截图所示：

2. 在你的仪表板上，点击 Organizations（组织）和账户名称，如下截图所示：

3. 现在我们需要获取 SSH 密钥，因此点击 Deployment Key（部署密钥）并复制 `ssh-rsa` 密钥，如下截图所示：

4. 返回 Heroku 仪表板并点击你的账户名称，然后点击 Manage Account（管理账户）菜单项，如下截图所示：

5. 进入账户页面底部的 **SSH Keys**（SSH 密钥），点击右侧的 **Edit**（编辑）按钮，如下截图所示：

6. 将 SSH 密钥粘贴到截图所示的 **enter new key**（输入新密钥）输入字段中，并点击 **Save**（保存）按钮。

7. 返回仪表板并进入 设置，复制 Heroku Git URL。

## 关于 Heroku 部署的额外说明

在书中给出的示例中，我们利用了一种在软件开发中广泛使用的部署流程，即通过持续集成服务。然而，你也可以使用 Heroku Toolkit 直接从本地开发环境将应用程序部署到云服务或你自己的托管服务。

Heroku Toolkit 是一个命令行程序，让你能够在终端中使用特定命令：`heroku`。该命令的结果如下截图所示：

```
Usage: heroku COMMAND [app] [command-specific-options]
Primary help topics, type "heroku help TOPIC" for more details:
| addons | manage addon resources |
| apps | manage apps (create, destroy) |
| auth | authentication (login) |
| config | manage config vars |
| domain | manage system domains |
| dynos | manage dynos (dynos, workers) |
| release | manage release commands (console, rake) |
| run | run one-off commands |
| collaborators | manage collaborators on an app |
| certs | manage ssl for an app |
| dist | scaling process for an app |
| fork | clone an existing app |
| git | manage git for |
| help | list commands and display help |
| info | authentication help |
| labs | manage optional features |
| maintenance | manage instances for an app |
| members | manage membership in organization accounts |
| orgs | manage organization accounts |
| pgbackups | manage backups of postgres databases |
| plugins | manage plugins for her gem |
| regions | list available regions |
| stack | manage the stack for an app |
| status | check status of heroku platform |
| update | update the heroku client |
| version | display version |
```

额外主题：

> 你可以在 Heroku 文档中找到关于直接部署的更多信息：https://devcenter.heroku.com/articles/git.html

在对直接部署进行简单介绍之后，我们已经涵盖了如何使用 GitHub、Shippable 和 Heroku 将应用程序部署到云端。

将应用程序部署到云端

SPA 可以包含十个或更多模板。这取决于应用程序的复杂性。记住这一概念，如果你简要回顾第 4 章“创建一个会议 Web 应用程序”，你会发现我们编写了仅在服务器端运行的 SPA，甚至使用了 API，这与使用 PHP 和 .NET 等服务器端语言构建动态应用程序的传统方式非常相像。

## 总结

在本章中，我们讨论了对软件开发至关重要的某些因素，以及为 SPA 准备高可扩展环境。

通过自动构建的测试过程，我们可以在几分钟内部署应用程序并确保交付的质量。我们涵盖了在带有 RESTful API 的 SPA 前端开发中许多许多重要概念和工具。整本书不仅为学习 SPA 奠定了坚实的基础，还描绘了关于 MEAN 开发和 RESTful 架构的示例和提示，涵盖了 SPA 整个开发过程的完整方法。

# 索引

## 符号

- `$Scope` 115
- `$g key` 127

## A

- 插件, Firefox URL 23
- 管理界面工具 URL 44
- Angular Batarang URL 23
- angular-gravatar 关于 137-146 URL 137
- AngularJS 关于 22 URL 22
- AngularJS MVC.pattern
    - Controller 111, 112
    - 实现 109
    - Model 109
    - View 110, 111
- AngularJS 插件
    - 优势 21
    - 使用 21
- angular-seed URL 119
- API
    - 关于 49
    - angular-gravatar 137-146
    - 基础结构，获取 76
    - 配置文件，创建 83
    - 目录结构，更改 77, 78
    - 示例 50
    - 文件，插入 79-82
    - 文件夹，插入 79-82
    - 实例化过程，更改 77
    - 重建 76
    - 重构 131-136
    - 运行 50, 51
    - API 路由
    - 测试 146, 147
- 应用程序
    - 解剖结构 128-131
    - 检查，生产环境中 187
    - 脚手架 126-128
    - 应用程序编程接口，见 API
    - 自动部署，来自 GitHub 关于 180
    - Heroku 账户，设置 181-184
    - Heroku 部署 184, 185
    - Shippable 账户，设置 180

## B

- Backbone.js 关于 13 URL 13
- 基础应用
    - 开始 108, 109
    - 基础结构
    - 获取 76
    - crypt, Node.js 应用程序 URL 89
    - beforeEach() 函数 157, 163
- 行为驱动开发 (BDD) 150
- 二进制 JSON (BSON) 40
- 样板代码 (boilerplate)
    - 关于 51, 126
    - 黑客松启动 52
    - MEAN.io 53, 54
    - MEAN.JS 53, 54
- Bower 关于 25 URL 25
    - 使用，用于前端
    - 依赖项 97, 98
    - 构建过程
        - 检查 186
    - 指令
        - 详细说明 112-115 URL 113
        - 指令模板属性 114
    - 目录结构
        - 更改，77, 78
        - SPA 目录结构
            - 基础文件夹示例 [SPA] Basic-folder-example 27
            - controllers 文件夹 27
        - CSS 27
        - 图像 27
        - sjs 27
        - 库 27
        - 模型 27
        - 模板 27
        - 视图 27
- 文档对象模型 (DOM) 108

## C

- CLI 153
- 云
    - Mongo, 用于 69
    - 代码生成器结构
    - 优势 57
- CommonJS 38
- 配置文件创建 83
- 持续应用开发 178, 179
- Controller, AngularJS 111, 112
- 创建、读取、更新和删除 (CRUD) 10
- CRUD 功能
    - 路由，定义到 66-69
- CSS 28
- 自定义指令创建 113

## D

- 数据
    - 插入，在 API 中 145
    - 插入，使用 Postman 71-74
- 数据属性 134
- 数据库即服务 (DbaaS) 70
- 依赖项
    - 声明 117
    - 依赖注入 关于 116, 117 URL 117
- desc() 函数 152, 155
- directive() 函数 114
- 文件插入 79-82
- find() 函数 134
- 文件夹插入 79-82
- 框架
    - 选择 17, 18
    - 前端依赖
        - 管理，使用 Bower 97, 98
    - Heroku 文档 URL 185

## E

- e2e 测试 关于 121, 150, 151
    - 文件夹，配置 170-172
- 嵌入 JavaScript (EJS) 关于 40, 76
    - 模板，与 95 使用
    - URL 76
- env 目录 130
- 事件驱动开发 32
- 事件循环 33-35
- expect() 函数 152, 167
- Express 关于 39, 40
    - 特性 39
    - URL 20
    - 使用 39
- Express 生成器 关于 58, 59 URL 58
    - 使用，优势 78
- 表达式详细说明 112-115
- express-session URL 89
- 极端编程 (XP) 179

## F

- 文件插入 79-82
- find() 函数 134
- 文件夹插入 79-82

## G

- 生成器 关于 23, 24, 51, 51, 56, 57
    - Express 生成器 58, 59
    - Yeoman 24
- Git URL 63, 105, 175
- GitHub
    - 项目，托管在 175-178
    - URL 177
- Gravatar URL 137
- Grunt 25

## H

- 黑客松启动 52
- Handlebars 关于 53
- Heroku 过程 URL 186
- Heroku Toolbelt 184
- Heroku 账户，设置 181-184
- Heroku 部署 184, 185
- Heroku 文档 URL 185
- HTML 28

## I

- 首页创建 99-105
- 实例化过程更改， 77
- it() 函数 152, 157

## J

- Jade URL 39
- Jasmine 151, 152
- Jasmine 测试框架 URL 152
- JavaScript 27, 28, 33, 34
- JSint URL 28
- JSLint URL 28
- JSONLint 28
- JSONView 70

## K

- Karma, 测试 165, 166

## M

- mocha 165

## W

- WebStorm
    - 关于 21
    - URL 21
- Windows Presentation Foundation (WPF) 12

## Y

- Yeoman
    - 关于 24, 56
    - URL 24, 56

# PACKT 出版社

感谢购买

学习单页 Web 应用开发

## 关于 Packt 出版社

Packt（读音为“packed”）于 2004 年 4 月出版了其第一本书《精通 phpMyAdmin 以进行有效的 MySQL 管理》，随后继续专注于出版针对特定技术和解决方案的高度针对性书籍。

我们的书籍和出版物分享了您的同行 IT 专业人士在适配和定制今日系统、应用程序和框架方面的经验。我们以解决方案为基础的书籍为您提供了知识和能力，让您自定义正在使用的软件和技术来完成工作。我们的书籍比您过去过的 IT 书籍更具体、更不通用。我们独特的方法提供了更集中的信息，让您获得更多需要的内容，并减少不需要的内容。

Packt 是一家现代独特的出版公司，专注于为开发者、管理员和新手社区制作高质量、前沿性的书籍。欲了解更多，请访问我们的网站 www.packtpub.com。

## 为 Packt 写作

我们欢迎所有对写作感兴趣的人士的咨询。书籍提案应发送至 author@packtpub.com。如果您的书籍想法仍处于早期阶段，并且您想在编写正式书籍提案之前先进行讨论，请联系我们；我们的一位策划编辑将与您联系。

我们不仅寻找已出版的作者，如果您拥有强大的技术技能但没有写作经验，我们丰富的编辑可以帮助您开启写作生涯，或简单地为您的专业知识获得额外的奖励。

# 精通 AngularJS 的 Web 应用开发

ISBN: 978-1-78216-182-0 平装本：372 页

利用 AngularJS 的力量构建单页 Web 应用

- 充分利用 AngularJS，理解 AngularJS 的设计哲学并将其应用于现实的开发任务中。
- 有效地结构化、编写、测试并最终部署您的应用程序。
- 为您的 AngularJS 添加安全和优化功能。

![](img/76faac513e4fd5843aeb56a44cada4c9_212_0.png)

# HTML5 Web 应用开发实例

ISBN: 978-1-84969-594-7 平装本：276 页

学习使用 HTML5、CSS3 和 jQuery 从零构建丰富、交互式的 Web 应用

- 充实了示例应用程序，展示了如何创建丰富、交互式的应用程序和游戏。
- 展示了如何使用 HTML5 中最流行且支持广泛的功能。
- 充满了编写更高效、更健壮代码的提示技巧，避免 JavaScript 中固有的某些陷阱。

![](img/76faac513e4fd5843aeb56a44cada4c9_212_1.png)

请查看 www.Packt.com 获取有关我们书籍的信息

# Express Web 应用开发

ISBN: 978-1-84969-654-0 平装本：236 页

学习如何从零使用 Express 框架开发 Web 应用

1. 探索 Express 框架 Web 开发的所有方面。
2. 从基础知识开始。
3. 涵盖所有 Express 主题的专家提示和建议。

![](img/76faac513e4fd5843aeb56a44cada4c9_213_1.png)

# Node Web 开发

第二版

ISBN: 978-1-78216-330-5 平装本：248 页

对 Node.js 的实用介绍，一种令人兴奋的服务器端 JavaScript 开发栈

1. 通过 Node.js 和 Node 模块学习服务器端 JavaScript。
2. 分别使用和不使用 Connect/Express Web 框架进行网站开发。
3. 开发 HTTP 服务器和客户端应用程序。

![](img/76faac513e4fd5843aeb56a44cada4c9_213_2.png)

请查看 www.PacktPub.com 获取有关我们书籍的信息
