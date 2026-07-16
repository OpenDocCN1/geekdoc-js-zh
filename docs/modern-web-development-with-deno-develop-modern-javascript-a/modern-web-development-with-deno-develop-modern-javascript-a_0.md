# Deno 现代 Web 开发：使用 Svelte、React 和 GraphQL 现代现代 JavaScript 和 TypeScript 代码



![](img/cover.jpg)
![image](img/cover.jpg)


![](img/line.jpg)


![](img/line.jpg)


![](img/logo.jpg)


版权 © 2023 BPB Online

保留所有权利。未经出版者事先书面许可，本书的任何部分均不得以任何形式或通过任何复制、存储在检索系统中或传输，但在批判性文章或评论中嵌入的简短引用除外。

在编写本书的过程中，我们已尽一切努力确保所呈现信息的准确性。然而，书中包含的信息均按“现状”出售，不提供任何明示或暗示的保证。作者、BPB Online 及其经销商和分销商均对因本书直接或间接引起或声称引起的任何损害不承担责任。

BPB Online 已努力通过正确使用大写字母提供书中提到的所有公司和产品的商标信息。然而，BPB Online 无法保证这些信息的准确性。

- **群组产品经理**:Marianne Conor
- **出版产品经理**:Eva Brawn
- **高级编辑**:Connell
- **内容开发编辑**:Melissa Monroe
- **技术编辑**:Anne Stokes
- **文字编辑**:Joe Austin
- **语言支持编辑**:Justin Baldwin
- **项目协调员**:Tyler Horan
- **校对员**:Khloe Styles
- **索引员**:V. Krishnamurthy
- **制作设计员**:Malcolm D'Souza
- **营销协调员**:Kristen Kramer



# 献给

*"献给世界上所有的开发者"*

# 关于作者

`Mayur` 是一位动态且以结果为导向的专业人士，对软件工程和完美追求充满激情。目前，他担任全栈软件工程师，参与多个使用 `Gatsby.js`、`Nikola`、`HTML`、`CSS`、`Bootstrap` 和 `Javascript` 等项目。`Mayur` 还使用了各种设计模式，如 `CRUD`、`SearchBar`、`CSVDownloader`、`Loader` 用于网络设备的 UI 创建，并针对每个模式编写了博客。他拥有浦那大学电子工程学士学位，以及电子与电信学文凭。此外，他在 Pluralsight 上拥有 60 多项认证，涵盖 `React`、`React Native`、`GraphQL`、`Python`、`Django`、`Javascript` 等课程主题。他对哲学和灵性也感兴趣。

# 关于评审员

`Chad Elofson` 是一位使用 `Node` 和 `Deno` 技术的软件分析师。他在汤普森河流大学担任软件分析师。他在 19 年前作为网络管理员开始了他的 IT 职业。在过去的八年里，他转向了基于 JavaScript 运行时技术的软件工程。

# 致谢

我感谢 BPB 出版团队给我编写这本书的机会。

# 前言

本书向开发者介绍了名为 `Deno` 的新 JavaScript 运行时。它还展示了如何使用 `Deno.js` 和 `TypeScript` 在前端后端创建 Web 应用。

本书为 Web 开发人员或 JavaScript 开发者提供了实用的方法。它也涵盖了一些实时示例。

本书分为 **9 章**。将涵盖 Deno 简介、TypeScript 简介、使用 React 创建 Web 应用、GraphQL 简介、创建 GraphQL API 服务器、创建 Svelte 应用等。详情列如下：

- **第一章** 将介绍 `Deno` 是什么、为什么由 `Node.js`（流行的 JavaScript 运行时）的作者引入 `Deno`、`Deno` 与 `Node` 之间的差异等。将列出 `Deno` 的特性，解释创建 `Deno` 使用的不同技术。还将提供关于什么是 JavaScript 运行时以及什么是 JavaScript 引擎的信息。
- **第二章** 将介绍什么是 `TypeScript`、`TypeScript` 的优势、`TypeScript` 的特性等。它还将为 JavaScript 开发者解释 `TypeScript` 的基础知识。并提供有关如何设置 `TypeScript` 的详细信息。
- **第三章** 将提供如何安装 `Deno` 的详细信息。还将列出一些开发所需的常用开发者工具，如 `VS Code`、`Terminal` 等。
- **第四章** 将涵盖 `Deno` 生态系统的详细信息。`Deno` 生态系统包括 `Deno CLI` 细节，如环境变量、子命令、如何传递参数、文件监听器、权限标志、权限白名单等。还将列出 `Deno` 运行时 API，如 `Web APIs`、`Global APIs` 等。作为生态系统组成部分的 `Deno` 模块分为两类：标准库和第三方模块。还将列出模块注册中心，如 Deno 自己的站点 `deno.land/x` 和 `nest.land`。
- **第五章** 将介绍 `Aleph.js`，一个用于 `Deno` 的全栈 React 框架。它将列出页面、路由等概念。简要介绍使用 `GET`、`POST`、`DELETE` 等 API 创建 `Todos` 应用。
- **第六章** 将继续开发 `Todos` 应用并涵盖 UI 实现。它将提供如何使用样式组件库创建 React 组件的详细信息。提供 `Button`、`Input` 等基础组件的代码。
- **第七章** 将介绍 GraphQL 并提供精确获取、单端点等特性的细节。还将列出 `Type`、`Input`、`Mutation`、`Resolver` 等核心概念。随后引入 `oak` 模块以及 `oak-graphql`，将用于实现 GraphQL 服务器。
- **第八章** 将涵盖使用 `oak, oak-graphql` 创建电话簿应用的 GraphQL 实现。将提供如何创建 git 仓库、使用 `trex` 作为包管理器以及使用 `velocaptor` 作为脚本运行器的详细信息。还将提供使用 ORM 进行数据库设置和认证的代码。
- **第九章** 将介绍富有前景的 JavaScript 框架或编译器 `Svelte`。`Snel` 是一个使用 `Deno` 创建 Svelte 应用的模块。它将涵盖 `Snel` 和 `snel-carbon`（UI 组件模块）的设置过程。随后提供为应用设置公私有路由的代码。以及 Svelte 组件。

# 彩色图片

请点击链接下载本书的***彩色图片***：

# [`rebrand.ly/nbyzlk9`](https://rebrand.ly/nbyzlk9)

我们在丰富的书籍和视频目录中 **[`github.com/bpbpublications`](https://github.com/bpbpublications)** 提供了代码包。去看看吧！





你知道吗？BPB 为所有出版的书籍都提供了 eBook 版本，并提供 PDF 和 ePub 文件。您可以在 `[www.bpbonline.com](http://www.bpbonline.com)` 升级到 eBook 版本，作为纸质书客户，您有权获得 eBook 副本折扣。请通过 `business@bpbonline.com` 与我们联系获取更多详情。

在 `[www.bpbonline.com](http://www.bpbonline.com)`，您还可以阅读免费技术文章合集，订阅一系列免费新闻邮件，并接收 BPB 书籍和 eBook 的独家折扣和优惠。

# 盗版

如果您在互联网上发现任何形式的我们作品的非法复制品，如果您向我们提供位置地址或网站名称，我们将不胜感激。请通过 `business@bpbonline.com` 并上材料链接与我们联系。

# 如果您兴趣成为作者

如果您在某个领域拥有专长，并且对编写或为书籍贡献感兴趣，请访问 `[www.bpbonline.com.](http://www.bpbonline.com/)`。我们与成千上万像您这样的开发者和技术专业人员合作过，帮助他们将见解分享给全球技术社区。您可以进行通用申请、申请我们正在招募作者的特定热点，或提交自己的想法。

# 评论

请留下评价。在您阅读并使用此书后，为什么不在您购买的网站上留下评价呢？潜在的读者就可以查看并利用您的无偏意见来做出购买决策。我们 BPB 可以了解您对我们产品的看法，我们的作者也可以看到您对书籍的反馈。谢谢！

有关关于 BPB 的更多信息，请访问 `[www.bpbonline.com.](http://www.bpbonline.com/)`。

# 第一章 (#toc.xhtml_c01)

# Deno 之陆 (#toc.xhtml_c01)

### 引言 (#toc.xhtml_s1a)

在 `Node` 运行时成功十年后，其创建者 `Ryan Dahl` 提出了另一种令人兴奋的技术，称为 `Deno`。它也是一个像 `Node` 一样的运行时，但与 `Node` 相比更加安全，并提供了许多改进和现代功能。Dahl 在 2018 年的 `JSCONF EU` 演讲中通过名为“我对 Node.js 遗憾的 10 件事”（****https://www.youtube.com/watch?v=M3BM9TB-8yA**） de 宣布了 `Deno`，震撼了开发领域。从那时起，`Deno`一直是软件行业的一个兴奋的话题。

### 结构 (#toc.xhtml_s2a)

在本章中，我们将涵盖以下主题：

*   介绍 Deno
    *   Node 革命
*   Deno 与 Node 的比较
*   Deno 特性
*   Deno 基础栈
*   什么是 JavaScript 引擎？
*   什么是 JavaScript 运行时？

### 目标 (#toc.xhtml_s3a)

学习本章后，你将熟悉 `Deno` 的主要特性及其内部架构。你还将理解使用 `Deno` 的原因。

### 介绍 Deno (#toc.xhtml_s4a)

在 `Node` 运行时成功十年后，其创建者 `Ryan Dahl` 提出了另一种令人兴奋的技术，称为 `Deno`。它也是一个像 `Node` 一样的运行时，但与 `Node` 相比更加安全，并提供了许多改进和现代功能。Dahl 在 2018 年的 `JSCONF EU` 演讲中通过名为“我对 Node.js 遗憾的 10 件事”（****https://www.youtube.com/watch?v=M3BM9TB-8yA**） 宣布了 `Deno`，震撼了开发领域。从那时起，`Deno`一直是软件行业的一个兴奋的话题。

*   Node 革命
*   Deno 与 Node 的比较
*   Deno 特性
*   Deno 基础栈
*   什么是 JavaScript 引擎？
*   什么是 JavaScript 运行时？

*   内置安全性
*   内置工具
*   TypeScript 支持
*   ES 模块
*   顶层 await (Top-level await)

### Node 革命 (#toc.xhtml_s5a)

在 `Node` 运行时成功十年后，其创建者 `Ryan Dahl` 提出了另一种令人兴奋的技术，称为 `Deno`。它也是一个像 `Node` 一样的运行时，但与 `Node` 相比更加安全，并提供了许多改进和现代功能。Dahl 在 2018 年的 `JSCONF EU` 演讲中通过名为“我对 Node.js 遗憾的 10 件事”（****https://www.youtube.com/watch?v=M3BM9TB-8yA**） 宣布了 `Deno`，震撼了开发领域。从那时起，`Deno`一直是软件行业的一个兴奋的话题。

### 无处处 JavaScript

在 `Node` 运行时成功十年后，其创建者 `Ryan Dahl` 提出了另一种令人兴奋的技术，称为 `Deno`。它也是一个像 `Node` 一样的运行时，但与 `Node` 相比更加安全，并提供了许多改进和现代功能。Dahl 在 2018 年的 `JSCONF EU` 演讲中通过名为“我对 Node.js 遗憾的 10 件事”（****https://www.youtube.com/watch?v=M3BM9TB-8yA**） 宣布了 `Deno`，震撼了开发领域。从那时起，`Deno`一直是软件行业的一个兴奋的话题。

### 异步与事件驱动架构

在 `Node` 运行时成功十年后，其创建者 `Ryan Dahl` 提出了另一种令人兴奋的技术，称为 `Deno`。它也是一个像 `Node` 一样的运行时，但与 `Node` 相比更加安全，并提供了许多改进和现代功能。Dahl 在 2018 年的 `JSCONF EU` 演讲中通过名为“我对 Node.js 遗憾的 10 件事”（****https://www.youtube.com/watch?v=M3BM9TB-8yA**） 宣布了 `Deno`，震撼了开发领域。从那时起，`Deno`一直是软件行业的一个兴奋的话题。

### 开源与跨平台

在 `Node` 运行时成功十年后，其创建者 `Ryan Dahl` 提出了另一种令人兴奋的技术，称为 `Deno`。它也是一个像 `Node` 一样的运行时，但与 `Node` 相比更加安全，并提供了许多改进和现代功能。Dahl 在 2018 年的 `JSCONF EU` 演讲中通过名为“我对 Node.js 遗憾的 10 件事”（****https://www.youtube.com/watch?v=M3BM9TB-8yA**） 宣布了 `Deno`，震撼了开发领域。从那时起，`Deno`一直是软件行业的一个兴奋的话题。

### 高性能

在 `Node` 运行时成功十年后，其创建者 `Ryan Dahl` 提出了另一种令人兴奋的技术，称为 `Deno`。它也是一个像 `Node` 一样的运行时，但与 `Node` 相比更加安全，并提供了许多改进和现代功能。Dahl 在 2018 年的 `JSCONF EU` 演讲中通过名为“我对 Node.js 遗憾的 10 件事”（****https://www.youtube.com/watch?v=M3BM9TB-8yA**） 宣布了 `Deno`，震撼了开发领域。从那时起，`Deno`一直是软件行业的一个兴奋的话题。

### 用于处理依赖的 Node 包管理器 (npm)

在 `Node` 运行时成功十年后，其创建者 `Ryan Dahl` 提出了另一种令人兴奋的技术，称为 `Deno`。它也是一个像 `Node` 一样的运行时，但与 `Node` 相比更加安全，并提供了许多改进和现代功能。Dahl 在 2018 年的 `JSCONF EU` 演讲中通过名为“我对 Node.js 遗憾的 10 件事”（****https://www.youtube.com/watch?v=M3BM9TB-8yA**） 宣布了 `Deno`，震撼了开发领域。从那时起，`Deno`一直是软件行业的一个兴奋的话题。

### 事件循环 (#toc.xhtml_s6a)

在 `Node` 运行时成功十年后，其创建者 `Ryan Dahl` 提出了另一种令人兴奋的技术，称为 `Deno`。它也是一个像 `Node` 一样的运行时，但与 `Node` 相比更加安全，并提供了许多改进和现代功能。Dahl 在 2018 年的 `JSCONF EU` 演讲中通过名为“我对 Node.js 遗憾的 10 件事”（****https://www.youtube.com/watch?v=M3BM9TB-8yA**） 宣布了 `Deno`，震撼了开发领域。从那时起，`Deno`一直是软件行业的一个兴奋的话题。

### Deno 与 Node 的比较 (#toc.xhtml_s7a)

在 `Node` 运行时成功十年后，其创建者 `Ryan Dahl` 提出了另一种令人兴奋的技术，称为 `Deno`。它也是一个像 `Node` 一样的运行时，但与 `Node` 相比更加安全，并提供了许多改进和现代功能。Dahl 在 2018 年的 `JSCONF EU` 演讲中通过名为“我对 Node.js 遗憾的 10 件事”（****https://www.youtube.com/watch?v=M3BM9TB-8yA**） 宣布了 `Deno`，震撼了开发领域。从那时起，`Deno`一直是软件行业的一个兴奋的话题。

| **特性** | **Node** | **Deno** |





| 构建语言 | C++ | Rust |
| :--- | :--- | :--- |
| JavaScript 引擎 | V8 (C++ 绑定和后端) | V8 (Rust 绑定和后端) |
| 事件循环 | libuv | tokio |
| TypeScript 支持 | 需要安装 | 开箱即用 |
| 包管理器 | Npm (中心化) | 无包管理器 (去中心化) |
| 导入系统 | CommonJS (`require()`) | ES  (`import`) |
| 安全性 | 默认完全访问 | 默认无访问 |
| package.json | 使用 | 不使用 |

### Deno 特性

Deno 对现代功能提供了极支持，并包含了许多 Node 原生不支持的功能（如 TypeScript 支持）。让我们来看看它的一些主要特性。

- 外部依赖通过 URL 加载
- 在沙箱中执行代码
    - 运行时无法访问网络文件系统和环境
    - 访问需要显式授权
- 开箱即用的 TypeScript 支持
- 顶层等待 (Top-level await)
- 标准模块库
- 提供的内置工具，例如：
    - **Bundler**: 将脚本和依赖构建成单个文件
    - **Dependency inspector**: 检查 ES 模块并列出所有依赖项
    - **Documents generator**: 解析 JSDoc
    - **Formatter**: 用于自动格式化 JS 和 TS 文件
    - **Test-runner**: 使用标准库中的断言模块进行测试
    - **Linter**: 用于检测代码问题

### Deno 基础栈

Deno 的创建使用了一些坚实的技术，这增加了它成功的概率。一旦我们熟悉了构建 Deno 所使用的技术栈，就可以对 Deno 的未来充满信心（一个非常光未来）。让我们来看看 Deno 使用的技术栈。

- 使用 Google 的 V8 引擎
- 使用 Rust 编写
- 使用 Tokio（用 Rust 编写的异步运行时）用于事件线程管理

### Google 开发的 V8 引擎

一个由 Google 使用 C++ 构建的开源 JavaScript 引擎。它将 JavaScript 代码（由 Deno 传递）转换为字节码/机器码。Deno 开箱即用支持 TypeScript，因此我们也可以提供 TypeScript 代码，Deno 将其编译为 JavaScript。它执行 JavaScript 代码，并通过 Deno 团队为 V8 引擎编写的 Rust 绑定 `rusty_v8` 将 Deno API 相关代码（Rust 代码）传递给 Rust 后端。

解释器 (`Ignition`）和编译器 (`TurboFan`）的结合使得 V8 生成运行极快的优化机器码。

### Rust

自 2016 年以来，Rust 在每次 StackOverflow 调查中一直是“最受喜爱”语言（连续五年）。它是一种系统编程语言，能够对底层细节进行控制。它提供了内存安全、线程安全和类型系统。由于这些以及许多其他特性，Rust 在过去五年的 StackOverflow 调查中是最受喜爱和最期待的语言。

- 默认内存安全
- 支持所有权和借用
- 性能与其他底层语言（C, C++）非常接近
- 只能有一个可变引用或多个不可变引用
- 没有 NULL 指针，只有 options（选项）

使用者：
- Amazon—firecracker
- Google—Fuchsia
- Facebook—Mononoke
- Microsoft—IoT Edge

Deno 后端包含文件系统、网络和环境访问，并用 Rust 编写。异步 i/o 绑定由 tokio 库处理。

### Tokio I/O 库

它用于用 Rust 编写异步应用程序。它是一个事件驱动、非阻塞 i/o 平台。它使用线程池和工作线程在后台执行操作。

当任何与 i/o、网络相关的代码传递给 V8 引擎时，它会通过 `rusty_v8` 绑定将其转发到 Rust 后端。接收到的代码的执行由 tokio 使用工作线程完成。

- 使用非阻塞事件进行异步 I/O 操作
- 使用 Mio 作为事件队列
- 事件循环机制用于监控调用栈和回调队列
- 使用线程池和工作线程在后台执行任务

### 什么是 JavaScript 引擎

JavaScript 引擎用于将 JavaScript/TypeScript 代码转换为字节码（解释器）或优化的机器码（编译器），以便计算机可以执行它。

自发布以来，已发布许多 JavaScript 引擎。

- Google 的 V8 引擎
- Mozilla 的 SpiderMonkey
- Microsoft 的 Chakra

在 JavaScript 引擎中，代码被解析为标记（tokens），用于用于生成抽象语法树（AST）。解释器使用该树生成字节码。剖析器（profiler）监控字节码，如果有优化空间，则将其传递给编译器。编译器输出优化的机器码，运行速度比字节码更快。

**解释器：**
解释器逐行翻译代码。它提供字节码作为输出。解释器开始编码的速度非常快，但不提供任何优化。

**编译器：**
编译器一次性翻译整个代码。编译器具有分析整个程序并对其优化空间。它输出优化的机器码。由于需要遍历整个程序，编译器分析和优化代码需要更长时间。

JavaScript 引擎结合了解释器和编译器的功能。通过这样，我们得到了运行更快的优化代码。这种编译器被称为“JIT 编译器”。

### 什么是 JavaScript 运行时

JavaScript 运行时是一个环境，结合了 JavaScript 引擎（Deno 中的 V8）、用底层语言编写的 API 后端（Deno 中的 Rust）、持续监控调用栈的回调队列和事件循环。

**内存堆：**
JavaScript 代码传递给 V8 引擎，它存储代码中的变量和函数。

**调用栈：**
它存储代码中调用的函数。它按照后进先（LIFO）原则运行。它始终指向当前运行的函数。一旦函数返回或传递给 Deno API，它就会弹出函数并执行栈中的上一个函数。

**Deno API：**
当 Deno 检测到与 i/o、网络等相关的代码时，它将代码传递给用 Rust 编写的 API 后端。它使用 `rusty_v8` 绑定将代码传递给后端。

**Tokio：**
它是一个事件驱动的异步 i/o 平台。Deno API 将代码传递给 tokio。它使用线程池和工作线程在后台执行操作并传递到回调队列。

**回调队列：**
按照先进先出（FIFO）原则运行。它存储 Tokio 传递的所有完成函数。它等待调用栈为空。

**事件循环：**
它持续监控调用栈和回调队列。如果调用栈为空且回调队列中有函数，它将函数传递到调用栈上进行执行。

### 总结

我们在 Deno 世界的之旅从这一章开始。我们学习了 Deno 和 Node 的历史，比较了 Deno 和 Node，并列出了 Deno 的特性。我们还涵盖了构建 Deno 的栈，即 *V8* JavaScript 引擎、*Tokio* 事件循环以及用 Rust 编写的 Deno API 后端。最后，我们涵盖了 JavaScript 引擎和 JavaScript 运行时架构，这些虽然强制性的，但为我们理解什么是 Deno 以及它如何在后台执行操作提供了坚实的基础。





虽然本章涵盖了 Deno 的主要特性，但 TypeScript 是 Deno 领域中一个需要重点介绍的重要部分。开箱即用的 TypeScript 支持是 Deno 的一项主要特性，学习 TypeScript 需要整章专门的章节来介绍基础知识。因此，我们将在接下来的章节中学习 `TypeScript`，因为在本书中我们将一直使用 `TypeScript` 进行编程。

既然你已经来到了这里，显然你对学习 Deno 很有兴趣并感到兴奋。Deno 有许多令人兴奋且现代的功能，我们将在全书中学习这些功能。

# 第二章](#toc.xhtml_c02)

## TypeScript 简介](#toc.xhtml_c02)

### 简介](#toc.xhtml_s16a)

开箱即用的 TypeScript 支持是 Deno 运行时提供的一项令人兴奋的功能。TypeScript 一一直是大型应用程序的热门选择，并被行业快速采用。它在 2020 年 Stack Overflow 开发者调查的[最受喜爱语言](https://insights.stackoverflow.com/survey/2020#most-loved-dreaded-and-wanted)部分中排名第二（[`insights.stackoverflow.com/survey/2020`](https://insights.stackoverflow.com/survey/2020)）。

### 结构](#toc.xhtml_s17a)

在本章中，我们将涵盖以下主题：

*   介绍 TypeScript
*   TypeScript 的优势
*   TypeScript 特性
*   TypeScript 基础
    *   基本类型
    *   接口 (Interfaces)
    *   类型别名 (Type aliases)
    *   接口与类型别名
    *   类型推断
    *   类型断言
    *   联合 (Unions)
    *   交集 (Intersections)
    *   类 (Classes)
*   动态与静态类型
*   强类型与弱类型
*   TypeScript 配置

### 目标](#toc.xhtml_s18a)

本章将帮助你熟悉 TypeScript 基础以及如何使用 TypeScript 开发 Deno 应用。本章还将帮助你理解静态类型检查的优缺点以及 TypeScript 提供的优势。

### 介绍 TypeScript](#toc.xhtml_s19a)

TypeScript 由 `Anders Hejlsberg` 于 2012 年公开发布，是一个非常流行且开源的 JavaScript 超集。它为 JavaScript 代码添加了静态类型定义。它由微软开发和维护。TypeScript 提供类型安全、类型推断、类型断言等许多功能，包括将 ES Next 特性引入 JavaScript。请查看以下截图：

![](img/Figure-2.1.jpg)

**图 2.1:** TypeScript

### TypeScript 的优势](#toc.xhtml_s20a)

JavaScript 在我们的行业中非常流行并被广泛。但在使用 JavaScript 开发大型应用程序时，它的动态特性使得许多类型相关的错误和 bug 在开发阶段通过，只有在运行时才能被捕获。运行时调试比编译调试要糟糕得多。

静态类型语言在编译期间（甚至运行代码之前）就能发现错误和 bug。TypeScript 通过在开发周期提供类型安全，帮助我们编写和维护大型应用程序。TypeScript 在编译时捕捉类型相关或其他错误，节省了我们宝贵的时间。

引入 TypeScript 是为了给 JavaScript 添加类型。TypeScript 代码通过 TypeScript 编译器或 babel 译器转换为 JavaScript。TypeScript 允许`静态类型检查`，它可以在不运行代码的情况下检测代码中的错误，即在编译时。它保留了 JavaScript 的运行时行为，这意味着代码的运行方式将保持一致。保持相同的运行时行为是 TypeScript 的核心特性之一。

### TypeScript 特性](#toc.xhtml_s21a)

TypeScript 提供了许多 ES-Next 功能，以及有助于开发大型应用程序的功能。我们将列出 TypeScript 的一些主要特性。

*   在编译时检测错误，无需运行代码
*   IDE 可以使用类型定义进行自动完成
*   对 JavaScript 代码提供静态类型系统支持
*   由于静态类型检查，更不容易出错
*   开箱即用的 ES-Next 特性
*   工具链
*   类型安全
*   类型推断
*   类型断言
*   泛型 (Generics)
*   接口和类型别名
*   语言服务
*   与 JavaScript 相同的运行时行为

### TypeScript 基础](#toc.xhtml_s22a)

作为 JavaScript 的超集，TypeScript 对开发者来说很容易上手。假设你熟悉 JavaScript，我们将学习 TypeScript 中包含的额外类型。

### 基本类型](#toc.xhtml_s23a)

在本节中，我们将介绍常用的数据类型。在 Deno 开发的大部分时间内，我们都会使用它们。

*   **Boolean (布尔值)**：接受 `true` 或 `false` 值。
*   **Number (数字)**：接受浮点数或整数。
*   **String (字符串)**：接受文本和字符。
*   **Array (数组)**：元素的数组。
*   **Generics (泛型)**：`Array<string>`
*   **Tuple (元组)**：固定数量的元素。
*   **Enum (枚举)**：将值映射到集合。
*   **Unknown (未知)**：接受所有类型。
*   **Any (任意)**：比 `unknown` 更宽松。
*   **Null (空)**：接受 null。
*   **Undefined (未定义)**：接受 undefined。
*   **Never (永不)**：作为永远不返回的类型。
*   **Void (空)**：作为不返回值的返回类型。
*   **Object (对象)**：表示非原始类型。

### 接口 (Interfaces](#toc.xhtml_s24a)

接口用于定义实体或对象的形状。它描述了对象应该拥有的属性。

```typescript
interface IPerson {
  firstName: string;
  lastName: string;
}

const person: IPerson = {
  firstName: "first",
  lastName: "last"
};
```

在前面的示例中，`IPerson`（注意大写的 I 表示接口）定义了对象 `person` 必须具备的形状。因此，属性 `place`会导致编译器错误，因为它在 `IPerson` 中不存在。

### 可选属性](#toc.xhtml_s25a)

在许多情况下，我们需要提供一个可选的字段。在接口中，可以使用 `?` 符号使字段变为可选。

```typescript
interface IPerson {
  name: string;
  age?: number; // age 是可选的
}

let printProfile = (person: IPerson): void => {
  console.log(person.name);
};

const person = { name: "name1" };
printProfile(person);
```

### 只读属性](#toc.xhtml_s26a)

在属性前的 `readonly` 关键字表示我们希望属性在创建后是不可变的。

```typescript
interface IPerson {
  name: string;
  readonly age: number; // age 是只读的
}

const person: IPerson = {
  name: "me",
  age: 29
};

person.name = "you";
// person.age = 25; // 不能给 age 赋值，因为它是只读属性

### 类型别名 (Type aliases](#toc.xhtml_s27a)

类型别名的工作方式与接口类似。接口用于定义对象的形状，而类型别名可以为原始类型提供名称。它们也可以用于联合类型。





```typescript
type myInt = number; // type 为原始类型 number 提供了新名称 myInt
```

```typescript
let myId: myInt = 11; // 这里 myInt 代表 number 类型
```

```typescript
let id: number = 11;
```

## 联合类型 (Unions)
```typescript
type unionId = number | string; // 联合类型
```

```typescript
let myUnionId: unionId = 25; // number
myUnionId = “1a2b”; // string
```

#### 与接口（interfaces）功能相似
```typescript
type PersonType = {
  firstName: string;
  lastName: string;
};

const person: PersonType = {
  firstName: “first”,
  lastName: “last”,
  // place: “unknown”, // 错误：类型 IPerson 中不存在 place
};
```

## 接口 (Interfaces) 与 类型别名 (type aliases)

TypeScript 允许接口合并（Interface merging），而类型别名的合并会导致编译错误。

```typescript
interface IPerson {
  name: string;
}

interface Iperson {
  // 将 place 合并到现有的 Iperson 中
  place: string;
}

const person: Iperson = { name: “Name1”, place: “space” };
```

```typescript
type PersonType = {
  name: string;
};

// type PersonType = {
//   // 错误：重复的标识符 ‘PersonType’
//   place: string;
// };
// const person1: PersonType = { name: “name2”, place: “time” }; // 不 place

## 类型推断 (Type inference)

TypeScript 有两种处理类型推断的方法。当我们显式地提供类型时，它被称为“显式类型 (Explicit typing)”；当 TypeScript 使用赋值的值*隐式地*推断类型时，它被称为“隐式类型 (Implicit typing)”。

### 显式类型
每当我们显式地为变量提供类型时，就称为显式类型。

```typescript
let myId: number = 25;  // 显式类型为 number
```

#### 隐式类型
即使没有通过初始赋值值、函数参数默认值或函数返回类型显式指定类型，TypeScript 也会推断变量的数据类型。这被称为隐式类型或类型推断。

如果没有给 `isAllowed` 变量显式标注 `false`，TypeScript 根据 `false` 值判断出数据类型为 `boolean`。

```typescript
let isAllowed = false; // 隐式类型
// TypeScript 根据值 false 推断类型为 boolean
// let isAllowed: boolean = false;
// 错误
// isAllowed = 25; // TS2322 [ERROR]: 类型与类型 ‘boolean’。
```

如果在声明时未提供值，则推断为 `any` 类型。此行为可以通过在 `tsconfig.json` 中设置 `“noImplicitAny”: true;`get 来禁用。

```typescript
let anyVar; // 推断为 ‘any’ 类型
anyVar = 2.3;
anyVar = false;
anyVar = “I’m any”;
```

## 类型断言 (Type assertions)

类型断言用于覆盖编译器推断的类型。类型断言可以通过两种方式定义：

### `as` 语法
```typescript
const word: unknown = “abcdefg”;
// const charCount: number = word.length; // 错误: TS2571 [ERROR]: 对象类型为 ‘unknown’。
const charCount: number = (word as string).length;
```

### 尖括号 <> 语法
```typescript
const word: unknown = “abcdefg”;
// const charCount: number = word.length; // 错误: TS2571 [ERROR]: 对象类型为 ‘unknown’。
const charCount: number = (<string>word).length;
```

## 联合类型 (Unions)
在联合类型中，变量可以持有两种或多种类型的值。联合类型用竖线或管道符号 `|`符号表示。

```typescript
let myNum: number = 24;
// myNum = “id2234”; // 错误: TS2322 [ERROR]: 类型 ‘string’ 不能赋值给类型 ‘number’。
let myId: string | number = 25; // myId 可以接受 string 或 number。
myId = “id234”; // 接受 string
```
```typescript
type myIdType = string | number;
let myId1: myIdType = 53;
myId1 = “id234”;
```

## 交叉类型 (Intersections)
交叉类型通过组合两个不同类型的所有属性和方法来创建。使用符号 `&` 来创建交叉类型。

```typescript
interface IPerson {
  name: string;
  age: number;
}

interface IEmployee {
  employeeId: number;
}

// PersonType 将拥有 IPerson & IEmployee 的所有属性
type PersonType = IPerson & IEmployee;
const printMe = (person: PersonType): PersonType => {
  return person;
};

const user: PersonType = {
  name: “name1”,
  age: 25,
  employeeId: 555,
};
const result = printMe(user);
console.log(result);
```

## 类 (Classes)
TypeScript 允许通过类来实现一种面向对象的编程方法。在 `OOP` 术语中，类是用于创建实例或对象的蓝图。通常情况下，一个类可以包含以下内容：

* `constructor()`：每当要创建类的实例时都会被调用。
* `fields`：变量或属性。
* `method`：函数

### 修饰符 (Modifiers)
修饰符是类字段的访问控制器。有三种修饰符：`public`、`private` 和 `protected`，用于字段和方法。

#### public
这是默认修饰符，允许在类外部访问字段/方法。

```typescript
class Person {
  name: string; // public
  age: number; // public
  // 创建实例
  constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
  }
  printMe() {
    console.log(this.name, this.age);
  }
}
const person = new Person(“me”, 99); // 调用构造函数，name=”me” 和 age=99
person.printMe();
console.log(person.age); // 属性可以在类外部访问
```

#### private
不允许在类外部访问字段/方法。子类无法访问私有属性。它通过 private 关键字或 ECMAScript 的 `hash)` 修饰符定义。

```typescript
class Person {
  name: string;
  private _age: number;
  #isActive: boolean; // 私有标识符
  constructor(name: string, age: number, isActive: boolean = true) {
    this.name = name;
    this.age = age;
    this.#isActive = isActive;
  }
  printMe() {
    console.log(this.name, this.age, this.#isActive);
  }
}
const person = new Person(“me”, 99);
person.printMe();
console.log(person.name);
/**
 * 错误: TS2341 [ERROR]: 属性 ‘age’ 是私有的，只能在类 ‘Person’ 内部访问。
 */
// console.log(person.age);
/**
 * TS18013 [ERROR]: 属性 ‘#isActive’ 不可在类 ‘Person’ 外部访问因为它是一个私有标识符。
 */
// console.log(person.#isActive);
```

#### protected
不允许在类外部访问字段/方法，但子类可以访问其字段。

```typescript
class Person {
  name: string;
  protected age: number; // 受保护的字段
  constructor(name: string = “unnamed”, age: number = 0) {
    this.name = name;
    this.age = age;
  }
  printMe() {
    console.log(this.name, this.age);
  }
}

class User extends Person {
  userId: number;
  constructor(userId: number, name: string, age: number) {
    super(name, age);
    this.userId = userId;
  }
  printMe() {
    console.log(this.name);
    console.log(this.age); // Person 类的保护字段 age 可供子类访问
  }
}
const user = new User(1, “me”, 99);
```





```typescript
user.printMe();

/**
* error: TS2445 [ERROR]: Property ‘age’ is protected and only accessible within
* class ‘Person’ and its subclasses.
*/
// console.log(user.age);
```

### Getter 和 Setter

正如我们在修饰符部分所看到的，`private` 和 `protected` 字段/方法无法在类外部访问。在某些情况下，我们需要访问它们。在这种情况下，Getters 和 Setters 会非常有帮助。

```typescript
class Person {
  name: string;
  private _age: number;
  #isActive: boolean;
  constructor(name: string, age: number, isActive: boolean = true) {
    this.name = name;
    this.age = age;
    this.#isActive = isActive;
  }
  printMe() {
    console.log(this.name, this.age, this.#isActive);
  }
  get _age() {
    return this.age;
  }
  set _age(value: number) {
    this.age = value;
  }
  get Is_active() {
    return this.#isActive;
  }
  set Is_active(value: boolean) {
    this.#isActive = value;
  }
}
const person = new Person("me", 99);
person.printMe();
console.log(person.name);

/**
* error: TS2341 [ERROR]: Property ‘age’ is private and only accessible within class ‘Person’.
*/
// console.log(person.age);
console.log(person._age);
person._age = 11;
console.log(person._age);

/**
* TS18013 [ERROR]: Property ‘#isActive’ is not accessible
* outside class ‘Person’ because it has a private identifier.
*/
// console.log(person.#isActive);
console.log(person.Is_active);
person.Is_active = false;
console.log(person.Is_active);
```

### 静态 (Static)

它用于定义属于类而不是属于实例的属性。这意味着静态字段对于所有类实例都保持不变。在我们希望所有实例共享一个字段的副本时，这种场景非常有用。在下面的示例中，我们使用 `static instanceCount` 来计算 `Person` 对象实例的数量。

```typescript
class Person {
  name: string; // public
  age: number; // public
  // 跨实例共享的静态属性
  static instanceCount: number = 0;
  constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
    // TS2576 [ERROR]: Property ‘instanceCount’ is a static member of type ‘Person’.
    // this.instanceCount += 1;
    // 使用类属性
    Person.instanceCount += 1;
  }
  printMe() {
    console.log(this.name, this.age);
  }
  printTotalPersons() {
    console.log("Total persons: Person.instanceCount);
  }
}
const person = new Person("me", 99);
person.printMe();
person.printTotalPersons(); // instanceCount = 1;
const person2 = new Person("you", 29);
person2.printMe();
person2.printTotalPersons(); // instanceCount = 2;
```

### 抽象 (Abstract)

抽象类是一个常见的基类（例如，`Person`），具有基本结构，可以被其他类继承（例如，`Employee`、`Employer`）。

```typescript
abstract class Person {
  name: string; // public
  age: number; // public
  constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
  }
  printMe() {
    console.log(this.name, this.age);
  }
}
/**
* error: TS2511 [ERROR]: Cannot create an instance of abstract class.
*/
// const person = new Person("employee", 39);
// person.printMe();
class Employee extends Person {}
class Employer extends Person {}
const employee = new Employee("employee", 39);
employee.printMe();
const employer = new Employer("employer", 99);
employer.printMe();
```

### 静态类型与动态类型

在编写应用程序时，我们遇到遇到属于静态或动态类型系统的语言。静态类型在编译时提供类型安全，但在开发过程中花费更多时间，而动态类型允许我们更快地编写代码，但可能会出现只有在运行时才能发现的错误和 Bug。

```typescript
// 静态类型 (TypeScript)
let id: number = 235; // 类型在编译时确定
// id = "332"; // 错误。不允许更改类型
// TypeScript 推断类型
let myId = 235; // 根据值推断为 number
// myId = "332"; // 错误。不允许更改类型

// 动态类型 (JavaScript)
let id1 = 10; // 类型在运行时确定
id1 = "132"; // 更改类型
```

| | 静态类型 | 动态类型 |
| :--- | :--- | :--- |
| 数据类型 | 需要显式指定 | 不需要显式指定数据类型 |
| 类型检查 | 在编译时 | 在运行时 |
| 类型更改 | 不允许 | 允许 |
| 语言 | C, C++ |

### 强类型与弱类型

强类型意味着不允许隐式类型转换，而弱类型意味着类型转换可以隐式进行。

### 强类型 (Python)
```python
id = 34 + "sfs" // 错误：不支持的运算符类型：‘int’ 和 ‘str’
```

### 弱类型 (JavaScript)
```javascript
let id = 34 + "abc"; // 因为类型转换结果 "34abc"
```

| | 强类型 | 弱类型 |
| :--- | :--- | :--- |
| 语言 | Python | JavaScript |
| 类型转换 | 仅限手动 | 自动和手动 |
| 示例 | 1 + "2" // 在 Python 中报错 | 1 + "2" // 在 JavaScript 中结果为 "12" |

## TypeScript 安装

在 Deno 之前，通过 `npm` 安装 TypeScript。由于 Deno 自带 TypeScript，我们可以直接开始编写 TypeScript 代码。但如果你打算在 Deno 环境外使用 TypeScript，你需要全局安装它。

**注意：确保你已安装 node 和 npm。**

`npm install -g typescript`

完成后，运行以下命令检查是否已安装 TypeScript：

`tsc --version`

`tsc --help`

### tsconfig.json

它是 TypeScript 配置/设置文件，指示 TypeScript 项目的根目录，并指定根文件和编译器选项。Deno 提供默认的 `tsconfig.json`，可以在此处查看。([`deno.land/manual/getting_started/typescript#custom-typescript-options`](https://deno.land/manual/getting_started/typescript#custom-typescript-options))

### 总结

TypeScript 是 JavaScript 受受认可和接受的超集，提供了类型安全。它在行业的流行是 Deno 将其作为主要语言的原因之一。

我们在本中涵盖了 TypeScript 的基础，在整个过程中还有很多可以学习的内容，因为 TypeScript 是我们 Deno 编程的首选语言。

同时，你可以随时在 TS Playground 中尝试不同的 TypeScript 功能：[`www.typescriptlang.org/play/`](https://www.typescriptlang.org/play/)。

通过本章，我们的基础部分（Deno, TypeScript）已经完成，我们将在接下来的章节开始 Deno 实战编程，届时我们将设置 Deno 并了解基础 Deno 命令。





在本节中，我们现在准备好运行 Deno 的实践体验了。在开始之前，我们需要为 Deno 配置开发环境。编码或编程只是软件工程的主要方面之一。还涉及其他主要因素，这些因素使我们能够在预计的时间内工程化并交付交付良好的软件应用程序。

### 结构

在本章中，我们将涵盖以下要点：

*   安装 Deno
*   开发工具
    *   终端 (Terminal)
    *   zsh + Oh my zsh
    *   Vim
    *   VS Code（带有插件）
    *   Git 和 GitHub
    *   Postman
    *   Docker
    *   Silver searcher (银搜索)
    *   数据库
        *   MongoDB + MongoDB Atlas
        *   Postgres
        *   Redis
    *   Heroku CLI
    *   番茄工作法
    *   Tmux

### 目标

我们将通过终端安装 Deno，并对 Deno 开发期间需要的一些主要开发工具和技术进行简要概述。我们将在后的项目工作中使用这些工具。虽然这些工具是可选的，但它们将提供更好的开发者体验和组织性。我们还将学习设置一些有助于开发者提高生产力和保持有条的常用开发工具。

## 安装 Deno

安装 Deno 非常简单，并可以使用单个终端命令完成。在你的机器上安装 Deno 有多种方法如下：

`# Shell (MacOS, Linux):`

```bash
curl -fsSL https://deno.land/x/install/install.sh | sh
```

`安装特定版本：`

```bash
curl -fsSL https://deno.land/x/install/install.sh | sh -s v1.5.4
```

`# PowerShell (Windows):`

```powershell
iwr https://deno.land/x/install/install.ps1 -useb | iex
```

`安装特定版本：`

```powershell
$v="1.5.4"; iwr https://deno.land/x/install/install.ps1 -useb | iex
```

`# Homebrew (MacOS):`

```bash
brew install deno
```

运行以下命令检查是否安装了 Deno：

`deno --version`

可以通过运行以下命令升级 Deno：

`deno upgrade`

可以通过运行以下命令将 Deno 升级到特定版本：

`deno upgrade --version 1.5.3`

## 开发工具

效率、专注和组织是开发者日常生活的关键方面。它们允许我们管理和组织工作流，以便我们通过系统化和有组织的方法创造更多价值。

开发工具是软件工程中一个重要方面，但往往被忽视或边缘化。这些工具对于提高生产力和提供更好的组织非常有帮助。它们让我们专注于核心部分，即软件开发，而它们则为我们高效地管理其他因素。让我们概述一下全球开发者使用的一些主要工具。

### 终端 (Terminal)

这是我们在编程世界中大部分时间所在地。熟悉它可以让我们在规划和执行日常任务或脚本（软件世界中的术语）时处于优势。这是我们将执行 Deno 命令的地方（从安装 Deno 到运行 Deno ）。你可以为 Linux/macOS 使用 UNIX 终端，或为 Windows 操作系统使用 PowerShell。

### zsh + oh my zsh

`zsh` (Z shell) 和 `oh my zsh` (zsh 框架) 可以提升你的整体开发体验和生产力。查看 GitHub 页面获取安装指南。Oh my zsh 带有一些很棒的插件，如图 [3.1] 所示。

`安装 zsh`

[`github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH`](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)

`安装 oh my zsh`

[`github.com/ohmyzsh/ohmyzsh`](https://github.com/ohmyzsh/ohmyzsh)

![](img/Figure-3.1.jpg)

**图 3.1：** 设置了 zsh + oh my zsh 的终端

**主题**: powerlevel10k

**插件**: Git, zsh-syntax-highlighting 和 zsh-autosuggestions

### Vim

Vim（也称为 vi）是一种用于快速高效进行文本操作的传奇文本编辑器。Vim 在行业中已经了数十年，并在这些年来一直保持着顶级编辑器的地位。它是一个以键盘为中心的应用程序，专注于通过键盘命令来执行复杂的文本操作。Vim 有自己的快捷键绑定，需要一些时间来适应，从而实现对文本处理和光标移动的更好的控制。

关于 vim 有许多传说，而“编辑器大战”也许是其中最著名的。有一个关于 90 年代 vim 和 emacs 之间竞争的著名传说。Vim 可以通过 VS Code 扩展或直接从终端使用。

`安装 vim`

[`www.vim.org/download.php`](https://www.vim.org/download.php)

### VS Code

VS Code 是由微软开发的一个开源 IDE。它适用于所有平台（Windows, Linux, macOS），并且是使用最广泛的 IDE 之一。它是用 Electron 构建的——一个用于跨平台桌面应用程序的 JavaScript 框架。[`code.visualstudio.com/download`](https://code.visualstudio.com/download)

### VS Code 插件

我们在开发 Deno 时列出一些实用的插件：

*   `Deno`: 启用 Deno 支持
*   `Prettier`: 一个用于美化代码的格式化
*   `ESLint`: 一个分析代码的 linter 工具
*   `Vim`: 启用 Vim 支持
*   `GitLens`: 可视化的 git 体验

### Git 和 GitHub

`Git` 是一个由 `Linus Torvalds`（Linux 内核创建者）开发的分布式版本控制系统。它在软件行业被广泛用于代码版本控制管理。[`git-scm.com/downloads`](https://git-scm.com/downloads) 在你的操作系统上安装它。

`GitHub` 是微软所有的源码托管网站。它使用 `Git` 进行版本控制和源码管理。[`github.com/`](https://github.com/) 如果还没有请注册。

### Postman

一个用于 API 开发和测试的平台，它可以帮助我们管理 API 集合并通过 GUI 测试我们的 API。[`www.postman.com/downloads/`](https://www.postman.com/downloads/) 在你的操作系统上下载并安装 Postman。

### Docker

Docker 是基于容器的软件开发平台，将整个应用程序作为一个隔离进程运行。它是容器化和微服务领域用的工具。Docker 带来了容器革命，改变了应用程序开发和部署的方式。

`安装 docker`

[`docs.docker.com/engine/install/`](https://docs.docker.com/engine/install/)

### Silver Searcher

### Docker Compose

Docker Compose 是由 Docker 团队开发的工具，用于将多个 docker 容器组合作为单个服务运行。我们将用于在 `docker-compose.yml` 文件中定义多个服务/容器。然后我们可以使用单个命令通过 YAML 配置运行所有定义的服务。

`安装 docker-compose`

[`docs.docker.com/compose/install/`](https://docs.docker.com/compose/install/)





这是一个免费开源的命令行工具，用于从终端快速搜索代码。请查看 [`github.com/ggreer/the_silver_searcher`](https://github.com/ggreer/the_silver_searcher) 获取安装说明。该工具对于在 Deno 开发过程中从终端进行快速代码搜索非常有帮助。

## 数据库

行业中广泛使用两种类型的数据库：`关系型`数据库（SQL 和 PostgreSQL），以列和行的形式在表格中存储数据；以及`非关系`数据库（MongoDB、Redis 和 ElasticSearch），以集合（collections）的形式存储数据。Postgres (RDBMS) 和 MongoDB (NoSQL) 是数据库中最流行的类型。

### PostgreSQL

PostgreSQL（也称为 `postgres`）是一个免费开源的`关系型数据库管理系统（（RDBMS`）。它是一个基于 SQL 的数据库，使用 SQL 进行数据管理，并以表格格式存储数据。

### `Install postgres`

[`www.postgresql.org/download/`](https://www.postgresql.org/download/)

## MongoDB 和 MongoDB Atlas

MongoDB 是一个开源 NoSQL 数据库系统，使用类似 JSON 的文档来存储数据。在 Deno 项目中使用 MongoDB 有两种方式，如下：

1. **本地安装 MongoDB**
   这将在你的机器上安装 MongoDB，可以在 Deno 应用本地开发期间作为数据库使用。
   [`docs.mongodb.com/manual/installation/`](https://docs.mongodb.com/manual/installation/)

2. **MongoDB Atlas**
   这是一种云端数据库服务，让我们可以在不进行本地安装的情况下使用 MongoDB 服务。它有一个免费层级计划，我们将将其作为 Deno 项目的数据库。你可以注册并开始使用 MongoDB Atlas。
   [`www.mongodb.com/cloud/atlas`](https://www.mongodb.com/cloud/atlas)

## Redis

远程字典服务器（`Redis`）是一个开源的内存数据库，以键值对（key-value）格式存储数据。我们可以通过遵循 [`redis.io/topics/quickstart`](https://redis.io/topics/quickstart) 上的指令在本地尝试它。

Redis docker 镜像：
[`hub.docker.com/_/redis`](https://hub.docker.com/_/redis)

## Heroku

它是一个`平台即服务`（`PAAS`），用于免费部署使用不同编程语言编写的应用程序。

### 注册 Heroku
[`www.heroku.com/home`](https://www.heroku.com/home)

### Heroku CLI
[`devcenter.heroku.com/articles/heroku-cli#download-and-install`](https://devcenter.heroku.com/articles/heroku-cli#download-and-install)

## Tmux

它是一个开源终端复用器程序，允许你从单个屏幕创建多个终端。在使用终端时，它将是一个非常有用的工具。请查看以下截图：

![](img/Figure-3.2.jpg)

**图 3.2:** Tmux

## 番茄工作法

这是一种时间管理技术，将工作分解为 `Pomodoro`（意大利语中意为“西红柿”）的时间间隔，随后是短/长休息。它帮助我们把工作拆分成更小的任务，并针对每个任务处理若干个番茄钟/Pomodoro。它对许多开发者（包括我自己）都很有益，因此它进入了本章。你可以从官方网站了解更多信息：
[`francescocirillo.com/pages/pomodoro-technique`](https://francescocirillo.com/pages/pomodoro-technique)

| 术语 | 长度 |
| :--- | :--- |
| Pomodoro | 25 分钟 |
| 短休息 | 5 分钟 |
| 长休息 | 15 或 25 分钟 |

**表 3.1:** 番茄工作法术语

### 总结

我们探索了一些在软件开发过程中非常有用的工具。在创建 Deno 应用程序时，我们将使用其中提到的许多工具。虽然这些许多工具对于 Deno 开发来说是可选的，但我们仍然建议使用它们以获得更好的开发体验。我们将在接下来的章节中学习 Deno 生态系统，包括 CLI、标准模块以及 nest.land（使用区块链的 Deno 软件包注册表）等其他内容。

# 第 4 章

## Deno 生态系统

### 引言

在动手实践 Deno 应用程序开发之前，我们需要学习运行时 API、CLI 命令和其他功能。这些 API 将提供输入输出输出和网络相关的功能。我们将探索 Deno CLI、Deno 运行时 API（Web APIs + Deno 全局 APIs）、标准模块库、第三方模块以及模块注册表，它们共同构成了 Deno 生态系统。

### 结构

在本章中，我们将涵盖以下点：

* Deno CLI
    * 环境变量
    * 子命令
    * 传递参数
    * 文件监听器
    * 权限
* Deno 运行时 APIs
    * Web APIs
    * Deno 全局 APIs
    * 变量
    * 类
* Deno 模块
    * 标准库
    * 第三方模块
* 模块注册表
    * deno.land/x
    * nest.land
    * Skypack
    * esm.sh
    * jspm

### 目标

我们将探索生态系统的各个部分。该生态系统包含了`命令行界面`（`CLI`）命令，如 run、install 等。运行时 API（Web + Deno 全局）以及标准模块（受 Go 语言库启发），如 uuid、http 等。除了标准模块外，还有成千上万的第三方模块可用，如 oak、opine、velociror、denodb、trex、denon 等。

我们将在后续项目中使用其中的一些。这些模块托管在 Deno 官方注册表 [deno.land/x](https://deno.land/x) 以及 [nest.land](https://nest.land)，后者是一个模块永不被删除的 Permaweb。

### Deno CLI

Deno `命令行界面`（`CLI`）内置了一些标准环境变量、子命令和选项。我们将在本节检查一些主要的。

### 环境变量

环境变量存储在代码之外，可以在不更改代码的情况下进行修改。这些对于设置不同环境（开发、测试、生产等）的值非常有用。它们还用于存储不应暴露在代码中的私密/密钥。Deno 提供了几个环境变量，我们列出以下几个主要的：

* `DENO_DIR`: 用于缓存下载导入的目录。导入在第一次执行时下载。随后的运行将使用 `DENO_DIR` 中的缓存。
* `DENO_INSTALL_ROOT`: 用于保存通过 install 命令 安装模块的目录。

### 子命令

Deno 子命令用于执行各种操作，如运行程序、格式化代码、安装脚本等。我们将频繁地使用 `run` 命令，并配合 `help` 获取特定子命令的帮助。我们将在下一节中带要概述和代码示例检查大多数子命令：

* **help**: 用于打印通用帮助信息或指定子命令的帮助信息。

    ```
    deno help # 列出子命令、选项、环境变量
    ```

    ```
    deno help run # 打印 run 命令的帮助信息
    ```





*   `run`: 它通过以下任意方式执行提供的 Deno 程序：

    *   filename：

        1. `deno run welcome.ts # 执行本地 welcome.ts 文件`

    *   url：

        1. `deno run https://deno.land/std@0.79.0/examples/welcome.ts`

    *   stdin：

        1. `cat welcome.ts | deno run -`

*   `install`: 将 Deno 脚本安装为 `DENO_INSTALL_ROOT` 指定目录下的可执行文件。

    1. `# 将 denon（文件监听器）安装为可执行文件`

    2. `deno install -qAf https://deno.land/x/denon@2.4.5/denon.ts`

*   `fmt`: TypeScript/Javascript 代码格式化工具。

    1. `deno fmt # 递归格式化当前目录下所有文件`

*   `doc`: 打印提供的源文件（模块）的文档

*   `eval`: 在终端评估 Javascript 代码

    1. `deno eval “console.log(Deno.args)” deno land`

    2. `# 输出: [“deno”, “land”]`

*   `test`: 使用内置测试运行器运行测试。符合 `{*_,*.,}test.{js,mjs,ts,jsx,tsx}`模式的文件将被考虑。支持过滤、覆盖率、快速失败（fail-fast）等选项。

*   `cache`: 下载并编译模块，并将所有依赖项保存在本地缓存中而不运行代码。

    1. `deno cache https://deno.land/std/http/file_server.ts`

*   `bundle`: 将单个 JavaScript 文件与其所有依赖打包。

*   `completions`: 将 Deno shell 补全脚本输出到提供的源文件中。

    1. `# 在 oh-my-zsh 中作为插件安装 Deno 补全`

    2. `mkdir ~/.oh-my-zsh/custom/plugins/deno`

    3. `deno completions zsh > ~/.oh-my-zsh/custom/plugins/deno/_deno`

    4. `# 在 ~/.zshrc 插件中添加 deno`

    5. `plugins=(… deno) // … 代表其他插件`

*   `compile`: 将提供的脚本编译为自包含的可执行文件。

### 传递参数

当需要为代码提供动态值时，参数非常有用。可以通过以下格式在脚本名称之后指定，将参数传递给脚本：

1. `deno run [FLAGS] [SCRIPT] [ARGUMENTS]`

前面的格式以 `deno` 可执行命令开始，后跟 `run` 子命令，该命令执行提供的脚本，随后是可选的安全标志（如 `--allow-net`、`--allow-read` 等）。接着提供要执行的脚本路径，然后是可选参数。脚本之后提供的所有条目（用空格分隔）都被视为参数，并通过 `Deno.args` 变量可用。

我们可以使用前面的格式运行带参数的 Deno 脚本。在项目文件夹（如 `home/my/work/deno/passing-arguments`）中创建一个名为 `args.ts` 的文件，内容如下：

1. `// args.ts`

2. `console.log(Deno.args);`

上面的代码简单记录了 Deno 运行时变量 `Deno.args`，它是提供的参数的数组。如果没有提供参数，则记录一个空数组 `[]`，如图 4.1 所示：

![](img/Figure-4.1.jpg)

**图 4.1:** 传递参数

现在我们将向 `args.ts` 文件传递两个参数 `deno` 和 `land`。如图 4.1 所示，运行以下代码后控制台应记录 `[“deno”, “land”]`：

1. `deno run args.ts deno land`

2. `# 输出: [“deno”, “land”]`

上面的代码带两个额外参数 `deno` 和 `land` 运行 `args.ts` 文件。由于 Deno 将文件名之后之后用空格分隔的所有条目都视为参数，这些条目通过 `Deno.args` 变量提供给 `args.ts` 文件。

**注意：标志不应在脚本名称之后传递，因为它们会被视为参数。**

在 `args.ts` 脚本之前传递的 `--allow-net` 标志被视为一个`标志 (flag)`，如下代码所示：

1. `deno run --allow-net args.ts deno land # Args [“deno”, “land”]. allow-net is a flag.`

在 `args.ts` 脚本之后传递的 `--allow-net` 标志被视为一个**参数 (argument)**，如下代码所示：

1. `deno run args.ts name --allow-net # Args[“name”, “--allow-net”]. Allow-net is not a flag`

### 文件监听

Deno 将带有 `--watch` 标志运行脚本，当文件变化时会自动重启脚本。这对于开发非常有用。

```bash
deno run --watch index.ts
```

### 权限标志

默认情况下，Deno 脚本没有访问网络、文件系统或环境变量的权限。你必须使用标志显式授予这些权限。

| 标志 | 说明 |
| :--- | :--- |
| `--allow-net` | 允许访问网络 |
| `--allow-read` | 允许读取文件 |
| `--allow-write` | 允许写入文件 |
| `--allow-env` | 允许访问环境变量 |
| `--allow-run` | 允许执行子进程 |

使用标志的示例：

```bash
deno run --allow-net --allow-read=config.json index.ts
```





1. `# 只允许读取 ‘args1.ts’, ‘args2.ts’ 文件`
2. `$ deno run --allow-read=args1.ts,args2.ts allow-read-list_example.ts`

### Deno 运行时 API

Deno 提供了许多在应用开发过程中非常有运行时 API 函数。所有这些运行时函数都记录在 `doc.deno.land` 中（[`https://doc.deno.land/https/github.com/denoland/deno/releases/latest/download/lib.deno.d.ts`](https://doc.deno.land/https/github.com/denoland/deno/releases/latest/download/lib.deno.d.ts)）。这些函数可以分为两个部分，即 Web（浏览器）API 和 Deno 全局 API。

### Web APIs

Deno 专注于使用现有的 Web 标准 API，而不是创建新的 API。Deno 提供了诸如 `fetch`、`setTimeout` 以及许多其他 Web API。这为熟悉 web API 的开发者提供了一个可以直接使用的优势。我们将在下表中列出这些 API：

| Web API | 描述 |
| :--- | :--- |
| `Fetch` | 用于发送 HTTP 请求并从网络获取资源。它返回一个 promise。 |
| `addEventListener` | 在全局作用范围内添加事件监听器。 |
| `removeEventListener` | 从全局作用范围内移除由 `addEventListener` 函数添加的 `eventListener`。 |
| `Alert` | 标准提示函数，显示提示消息并等待按下 Enter 键。 |
| `setInterval` | 在指定的间隔后反复调用提供的函数，直到使用 `clearInterval` 函数将其清除。 |
| `clearInterval` | 取消由 `setInterval` 启动的操作。 |
| `setTimeout` | 在指定的时间段后调用函数。 |
| `clearTimeout` | 取消由 `setTimeout` 启动的延迟操作。 |
| `Btoa` | 从提供的字符串创建 base-64 ASCII 编码字符串。 |
| `Atob` | 解码由 base-64 编码（如 `btoa`）编码的数据字符串。 |
| `Confirm` | 显示提供的消息并等待用户输入。返回 `boolean` 类型的用户输入（仅 `y` 和 `Y` 为真）。 |
| `Prompt` | 显示提供的消息并等待用户输入。返回 `string` 格式的用户输入。 |
| `dispatchEvent` | 在全局作用范围内分发事件并调用已注册的监听器。对于可取消事件或监听器调用了 `Event.preventDefault()`，返回 `false`。 |

**表 4.2:** Web APIs

### Deno 全局 APIs

所有非 Web 标准 API 都通过 Deno 全局命名空间可用。用于 i/o（`Deno.readFile`, `Deno.writeFile`）和网络（`Deno.listen`, `Deno.connect`）的 API 在此命名空间可用。

注意，许多函数都有同步版本。

例如，`create` 函数有一个同步方法 `createSync`。

我们将在下表中列出 Web APIs 及其同步版本（如果可用）：

| Deno API | 同步 | 描述 |
| :--- | :--- | :--- |
| `listen` | `–` | 用于带有主机、端口和传输选项的监听器。 |
| `close` | `–` | 关闭之前打开的资源 ID (`rid`)。 |
| `connect` | `–` | 连接到提供的主机和端口。 |
| `copy` | `–` | 从源复制到目标。 |
| `cwd` | `–` | 将当前工作目录 (`cwd`) 作为字符串返回。 |
| `run` | `–` | 启动一个新的子进程。子进程命令必须定义为给 `cmd` 键的数组。 |
| `exit` | `–` | 退出 Deno 进程。可以提供可选错误码作为参数（默认=0）。 |
| `open` | `openSync` | 打开文件以执行读取、写入和创建操作。 |
| `copyFile` | `copyFileSync` | 将一个文件的内容和权限复制到另一个文件。 |
| `create` | `createSync` | 如果不存在则创建文件，或截断现有文件。 |
| `mkdir` | `mkdirSync` | 使用提供的字符串路径创建新目录。 |
| `readDir` | `readDirSync` | 读取提供路径下的目录并返回 `Deno.dirEntry` 可迭代对象。如果路径不是目录则抛出错误。 |
| `readFile` | `readFileSync` | 将文件读取为字节数组。可以使用 TextDecoder 将字节转换为字符串。如果路径包含目录，则返回空数组。 |
| `readTextFile` | `readTextFileSync` | 读取 utf8 编码字符串读取文件。如果路径包含目录则抛出错误。 |
| `remove` | `removeSync` | 移除提供路径下的文件或目录。对于提供的路径抛出错误。 |
| `rename` | `renameSync` | 重命名文件或目录。 |
| `chmod` | `chmodSync` | 修改文件权限。 |
| `chown` | `chownSync` | 更改文件所有者。 |
| `writeFile` | `writeFileSync` | 将数据写入文件。 |
| `writeTextFile` | `writeTextFileSync` | 将文本写入文件。 |

**表 4.3:** Deno APIs

### 变量

Deno 为各种应用程序提供了变量。下表列出了主要变量：

| 变量 | 描述 |
| :--- | :--- |
| `args` | 返回参数数组 |
| `build` | 提供系统相关信息，如 `os`。 |
| `env` | 通过 `get`, `set`, `keys`, `values`, `delete` 提供环境变量。 |
| `mainModule` | 返回入口模块的 URL |
| `pid` | 返回当前进程 ID |
| `stdin` | `stdin`（标准输入）的句柄 |
| `stdout` | `stdout`（标准输出）的句柄 |
| `stderr` | `stderr`（标准错误）的句柄 |
| `version` | 提供 Deno、TypeScript 和 v8 的版本信息 |

**表 4.4:** Deno 变量

### 类

Deno 运行时有许多不同用途的类。我们将在后续项目中使用 `Request` 和 `Response` 类。以下列表包含主要类及其描述：

| 类 | 描述 |
| :--- | :--- |
| `Blob` | 包含原始不可变数据的类对象。 |
| `Event` | 代表 DOM 事件的类。包含 `target` 属性、`PreventDefault()` 方法等。 |
| `File` | 提供文件相关信息，如 `lastModified`、`name`、`type`、`size` 等。它继承自 `Blob` 类。 |
| `FormData` | 以键值对格式表示表单字段。提供 `get`, `set`, `keys`, `values`, `entries` 等方法。 |
| `Headers` | 以对象格式表示头部相关数据。 |
| `Location` | 通过 `globalThis.location` 提供链接对象的位置/URL。 |
| `Request` | 代表请求相关信息 |
| `Response` | 代表对请求的响应 |
| `TextEncoder` | 提供 utf8 编码功能，用于将字符串编码为字节数组。 |
| `TextDecoder` | 提供解码函数，将字节数组解码为字符串。 |
| `URL` | 提供创建对象 URL 所需的静态方法的对象。 |





| `WebSocket` | 提供创建和管理 WebSocket 连接以及发送和接收数据的 API |

**表 4.5:** Deno 类

### Deno 模块

如果没有模块（标准库和第三方模块），运行时生态系统将是不完整的。事实上，Node.js 的流行归功于 npm 提供的大量第三方模块。Deno 提供了两种模块：标准库和第三方模块。我们将在接下来的章节中检查这两种模块。

### 标准库

Deno 标准库是标准模块的集合，灵感来源于 Go 语言的标准库。所有标准模块都经过 Deno 核心团队审核，且不包含外部依赖。这些模块可以在 `[`deno.land/std`](https://deno.land/std)` 获得。我们在下表中列出了它们：

| 模块 | 描述 |
| :--- | :--- |
| `archive` | 提供 `Tar`、`Untar` 功能的模块。 |
| `Async` | 异步任务工具，具有 `deferred`（带有 reject 和 resolve 函数的 Promise）、`delay`（延迟 promise 决）功能。 |
| `Bytes` | 提供处理字节的辅助函数。 |
| `Datetime` | 日期时间模块，包含 `parse`（字符串到日期）、`format`（日期到字符串）、`difference`（两个日期之间的差异）以及一些额外的函数。 |
| `Encoding` | 移植自 Go 的 `encoding` 模块，该模块对于处理 csv、yaml、toml 等外部数据结构非常有用。 |
| `flags` | 基于 `minimist` npm 模块的命令行参数解析器。适用于 CLI 工具开发。 |
| `Fmt` | 提供类似 `printf` 的 I/O 格式化函数。 |
| `Fs` | 提供文件系统操作的辅助函数。提供 `emptyDir`、`ensureDir`、`exists`、`move`、`copy`、`walk` 等函数。该模块目前是不稳定的，因此在使用时需要使用 `--unstable` 标记。 |
| `Hash` | 用于创建支持大量算法的哈希值。 |
| `http` | 有用于创建 HTTP Web 服务器。它还包含一个通过 HTTP 服务本地文件的文件服务器函数。
| `Io` | 提供类似 `Reader`、`Writer`、`Streams` 等函数。 |
| `Log` | 带有日志级别的日志器模块。 |
| `Mime` | 用于处理多部分表单数据。 |
| `Node` | Node 标准库的兼容模块。允许在 Deno 中使用 lodash 等 Node 模块。 |
| `Path` | 提供路径相关的函数。 |
| `Permissions` | 为脚本提供权限。 |
| `Signal` | 提供捕获和监控操作系统信号（如 SIGINT）的 API。 |
| `Testing` | 提供测试相关的工具函数，如 `assert`、`equal` 等。 |
| `Textproto` | 灵感来源于 Go 的 `textproto` 模块。 |
| `Uuid` | 提供 `generate` 和 `validate` 通用唯一标识符 (`UUID`) 的函数，并支持版本 1、4 和 5。 |
| `Wasi` | 提供 WebAssembly 系统接口 (`WASI`) 的实现。 |
| `ws` | 有用于创建 WebSocket 服务器。 |

**表 4.6:** Deno 标准库

### 第三方模块

Deno 1.0 于 2020 年 5 月发布。从那时起已有许多用于不同目的模块，例如 Web 服务器 (`oak`)、身份验证 (`onyx`)、数据库 (`mongo`)、ORM (`denodb`)、JWT (`djwt`) 等。我们将在接下来的表中简要概述许多此类模块：

| 第三方模块 | 描述 |
| :--- | :--- |
| `oak` | 一个极其流行的 Web 中间件框架，包括路由等中间件。灵感来源于 `koa` 框架。 |
| `Aleph` | 一个灵感来源于 `Next.js` 的 React 框架，支持服务端渲染 (`SSR`)、静态网站生成器 (`SSG`) 等。 |
| `Pagic` | 用于静态网站生成的 React 框架。 |
| `drash` | 一个轻量级的 REST 微框架，支持使用 React 和 Vue 进行 API 开发和单页应用 (`SPA`) 开发。 |
| `Servest` | 与 `std/http` 兼容的 Web 服务器，开箱支持 WebSocket 和 JSX。 |
| `Denon` | Deno 版本的 Node `nodemon` 替代品，在检测到更改时会自动重启应用或服务器。它还作为 `deno` 命令的替换封装器。 |
| `Webview` | 创建桌面 GUI 应用的跨平台模块。 |
| `Denodb` | 支持 MySQL、PostgreSQL、MongoDB、MariaDB 和 SQLite 数据库的 ORM。 |
| `Trex` | 类似于 NPM 的模块管理器，符合 Deno 的哲学。它使用 `import_map.json` 作为根。 |
| `Webview` | 创建桌面 GUI 应用的跨平台模块。 |
| `Denodb` | 用于 Deno 的类模块模块管理器。 |
| `ts` | 用于 Deno 的 TypeScript 模块。 |
| `Postgres` | 类似 PostgreSQL 的驱动程序。 |
| `Redis` | Redis 客户端。 |
| `Dvm` | Deno 版本管理器。 |
| `Mongo` | MongoDB 驱动程序。 |
| `Vno` | 类似 Vue 的框架。 |
| `Eta` | 模板引擎。 |
| `Mysql` | MySQL 驱动程序。 |
| `Sqlite` | SQLite 驱动程序。 |
| `Ssgo` | 静态网站生成器。 |
| `Onyx` | 身份验证模块。 |
| `Otpauth` | 身份验证模块。 |
| `Aqua` | Web 框架。 |
| `Denox` | 跨平台脚本。 |
| `Dejs` | EJS 模板引擎。 |
| `Dotenv` | 环境变量的模块。 |
| `Udd` | 更新依赖的模块。 |
| `Djwt` | JSON Web Token 模块。 |
| `Cotton` | SQL Toolkit。 |
| `Denomander` | 命令行界面。 |
| `Lume` | 静态网站生成器。 |
| `Oak_graphql` | GraphQL 中间件。 |
| `Drake` | 任务运行器。 |
| `Rhum` | 测试框架。 |
| `websocket` | WebSocket 模块。 |
| `dext.js` | Preact 框架。 |
| `denoliver` | 静态文件服务器。 |
| `wocket` | WebSocket 模块。 |
| `dem` | 版本管理器。 |
| `bundler` | 打包器。 |
| `dmm` | 模块管理器。 |
| `opencv` | OpenCV 模块。 |
| `garn_validator` | 验证器模块。 |
| `watch` | 文件监听器。 |
| `smtp` | SMTP 模块。 |
| `nanoid` | NanoID 实现。 |
| `superoak` | HTTP 断言模块。 |
| `dpx` | 类似 NPX 的运行器。 |
| `drash_middleware` | 中间件模块。 |
| `cors` | CORS 模块。 |
| `postcss` | Postcss 模块。 |
| `oak_middleware` | 中间件集合。 |




模块注册表是托管 Deno 的地方。就像 Node 中的 `npm` 一样，Deno 也有几个使用区块链等现代功能构建的模块注册表。

在列出 Deno 的标准模块和第三方模块之后，我们将检查 Deno 可用的主要模块注册表：

| 模块注册表 |  |
| :--- | :--- |
| `deno.land/x` | 官方模块注册表，托管了大量第三方模块（编写时有 1651 个模块） |
| `nest.land` | 一个使用 `blockweave`（区块链的派生物）构建的现代 Deno 模块注册表。发布的模块是不可变的、去中心化的且永久的，这意味着它们永远无法被删除。 |
| `Skypack CDN` | 由 `Pika` 提供的托管预优化 ES 模块的 CDN。它提供压缩、缓存、填充填充（polyfilling），并将 `npm` 包转换为 ES 模块。每当在模块 URL 后面添加 `?dts` 时，它会自动使用 `X-TypeScript-Types` 请求头获取类型声明。 |
| `esm.sh` | 由 `aleph` 框架创建者提供的 ES 模块 CDN，它为每个模块封装所有依赖（同行依赖除外）。Node 包通过 `esbuild` 转换为 ES 模块以便通过填充在 Deno 上运行。它默认通过 `X-TypeScript-Types` 请求头提供类型声明。 |
| `jspm` | 一个将 `npm` 包转换为 ES 模块的模块 CDN。 |
| `Web` | 托管在互联网（例如 GitHub）上的任何 ECMAScript 模块都可以 Deno 支持的 ESM import 使用。 |

**表 4.8：** Deno 模块注册表

### deps.ts 中的中心依赖

在 Deno 世界中，有一种约定用于从 `deps.ts` 文件中导入所有依赖。这些依赖被重新导出并在整个项目中使用。这有助于我们在一个地方维护所有依赖。同样地，开发依赖被保存在在一个名为 `dev_deps.ts` 的单文件中。

在接下来的代码中，我们从 `deps.ts` 文件中导入所有的依赖 URL 并将其导出以供整个项目使用。我们从第三方大小处理模块导入了 `titleCase` 函数，该函数会返回每个单词首字母大写的标题格式。我们还从 Deno 标准库的测试模块导入了 `assertEquals` 函数。

```
// deps.ts
1. import titleCase from "https://deno.land/x/case@v2.1.0/titleCase.ts";
2. import { assertEquals } from "https://deno.land/std@0.97.0/testing/asserts.ts";
4. export { titleCase, assertEquals };
```

现在我们将在 `hello.ts` 文件中从 `deps.ts` 文件导入模块，如下代码所示：

```typescript
// hello.ts
1. import { titleCase, assertEquals } from "./deps.ts";
3. console.log(titleCase("hello world"));
4. assertEquals("hello", "helloz");
```

前面的代码输出了标题格式为 `"Hello World"` 的字符串 `"hello world"`，并且 `assertEquals` 函数因为实际值（`"hello"`）和预期值（`"helloz"`）不等而抛出 `AssertionError`，如图所示：

![](img/Figure-4.2.jpg)

**图 4.2：** deps.ts 示例

### 结论

我们现在结束关于 Deno 生态系统的章节。它概述了 Deno 生态系统的各个部分，如运行时 API、CLI、标准模块和第三方模块、模块注册表等。作为行业中的一项新技术，Deno 生态系统正在以快速速度进化。我们可能会看到 Deno 社区提出新的令人兴奋的想法和实现，就像他们一直以来所做的那样。

随着本章的结束，我们现在准备好进入书中最激动的部分——编写代码。我们将在接下来的章节中从头开始编写 Deno 应用。在此之前，继续探索 Deno 生态系统。

# 第 5 章

## Todos 应用—API

### 简介

我们现在准备好进入编码战场或游乐场（取决于你如何看待）。在本章中，我们将创建一个包含 `CREATE`、`RETRIEVE`、`UPDATE` 和 `DELETE`（`CRUD`）的应用。一个 Todos 应用。这将是我们 Deno 编码之旅的绝佳开始。我们将学习、调整并尝试使用名为 `Aleph.js` (aleph) 的全栈 React 框架创建的 Todos 应用，它列在 [第 4 章，Deno 生态系统] 的 [表 4.7] 中。API 将在本章实现，而 UI 将下一章实现。

### 结构

在本章中，我们将涵盖以下主题：

* Aleph.js 简介
    * 特性
    * 概念
        * 页面
        * 路由
        * API
* Todos 应用 API 实现

### 目标

我们将能够学习：使用 aleph 开发全栈应用需要学习的三个基本概念。我们将使用这些概念来创建页面、基于文件名的路由以及 API。本章的目标是熟悉 aleph.js。我们将在接下来的章节中从头开始编写 Deno 应用。在此之前，请继续探索 Deno 生态系统。我们还将学习实现“表述状态转换”（`REST`）操作，如 `CREATE`、`RETRIEVE`、`UPDATE` 和 `DELETE`。

### 引入 Aleph.js

Aleph.js 是一个受 Next.js 启发的全栈框架。它使用 ES 模块语法，不需要 Webpack 或或其他绑定器。它仅重新打包更改的模块，并通过热更新（`HMR`）立即在浏览器中更新。Aleph.js 可以使用以下命令安装：

```bash
deno install -A -n aleph https://deno.land/x/cli.ts
```

### 特性

Aleph.js 是一个功能丰富的框架，提供了服务端渲染、静态站点生成、API 开发等许多功能。主要功能如下：

* 基于文件系统的页面和路由
* API 开发
* 服务端渲染
* 静态站点生成
* 零配置
* 映射的使用
* 带有 Fast Refresh 的 HMR
* 通过 useDeno hook 在组件中访问 Deno 

### 命令行界面

Aleph.js **命令行界面**（CLI）提供了静态站点生成、创建带有模板代码的新应用、升级 aleph.js 等命令。主要命令列如下：

| 命令 |  |
| :--- | :--- |
| `aleph init` | 创建带有模板代码的新应用 |
| `aleph upgrade` | 升级 aleph.js |
| `aleph` | 显示所有命令行命令 |
| `aleph -h` / `aleph --help` | 显示帮助信息 |
| `aleph -v` / `aleph --version` | 显示 aleph.js 版本 |
| `aleph dev` | 以开发模式启动服务器 |
| `aleph start` | 以生产模式启动服务器 |
| `aleph build` | 构建应用为静态站点 |
| `aleph analyze` | 分析应用依赖 |

`aleph init` 命令提供了一个带有模板代码的示例应用。我们将使用它来初始化示例应用：

```bash
aleph init hello-aleph // 创建带有模板代码的 hello-aleph 文件夹
cd hello-aleph
aleph dev // 以开发模式运行应用
```

你可以访问 `http://localhost:8080` 查看示例应用，如图所示：

![](img/Figure-5.1.jpg)

**图 5.1：** Aleph.js 示例应用

### 概念

使用 aleph 开发全栈应用需要学习的三个基本概念。我们将使用这些概念来创建页面、基于文件名的路由以及 API。

### 页面




在 `/pages` 文件夹下，任何扩展名为 `*.js`、`*.jsx`、`*.ts`、`*.tsx` 和 `*.mjs` 且包含默认导出 React 组件的文件都被视为页面。由于 `aleph.js` 支持基于文件名的路由，每个页面将根据文件名关联到相应的路由。

### 示例：

如果我们按照如下代码，创建一个具有默认导出 React 组件的 `pages/hello.tsx` 文件，那么我们就可以通过 `http://localhost:8080/hello` 访问该页面，如 *图 5.2* 所示。

```tsx
// pages/hello.tsx
import React from “react”;

export default function Hello() {
return “Hello Deno!”;
}
```

![](img/Figure-5.2.jpg)

**图 5.2:** Hello Deno! 页面

每个页面都会被**预渲染**，这意味着页面的 HTML 会提前生成，从而获得更好的性能和 SEO。Aleph.js 还支持**水合（hydration）**过程，当浏览器加载页面时，会运行与 HTML 相关的 JavaScript 代码，使其具有完全交互性。

### 路由

Aleph.js 支持基于文件系统的路由。它会自动将名为 `index` 的文件路由到目录根节点。同时也支持通过**括号**语法 `[]` 或 **$** 符号前缀来实现**动态路由**。

```text
// 路由
pages/index.tsx => localhost:8080/
pages/hello/index.tsx => localhost:8080/hello

// 动态路由
// $ 前缀
pages/hello/$name.tsx => pages/hello/buddy
```

以下代码使用 `useRouter()` 钩的 `params` 对象来获取传递的参数值。`params` 的属性键由文件名（`name`）决定。

```tsx
// pages/hello/$name.tsx
import React from “react”;
import { useRouter } from “https://deno.land/x/aleph/framework/react/mod.ts”;

export default function Hello() {
const { params } = useRouter();
return `Hello ${params.name}!`;
}
```

如果我们在浏览器中输入 `route /hello/buddy`（其中 `buddy` 是 `name` 参数的值），我们将会看到如 *图 5.3* 所示的响应。

![](img/Figure-5.3.jpg)

**图 5.3:** 动态路由 ($ 语法)

```text
// 括号语法 []
pages/places/[place].ts => pages/places/munich
```

与 $ 符号语法类似，括号语法 `[]` 也具有相同的作用，所示。在这里，参数键是 `place`（源自文件名 `[place].ts`）。如果我们在浏览器中输入 `/places/munich`（其中 Munich 是 `place` 参数的值），我们将会看到如 *图 5.4* 所示的响应。

```tsx
// pages/places/[place].tsx
import React from “react”;
import { useRouter } from “https://deno.land/x/aleph/framework/react/mod.ts”;

export default function Places() {
const { params } = useRouter();
return <h1>{`${params.place} is a wonderful place!`}</h1>;
}
```

![](img/Figure-5.4.jpg)

**图 5.4:** 动态路由（括号语法）

该系统支持**嵌套路由**，并如下所示所示实现：

```text
pages/users/[username]/account.tsx => pages/users/user1/account
```

```tsx
// pages/users/[username]/account.tsx
import React from “react”;
import { useRouter } from “https://deno.land/x/aleph/framework/react/mod.ts”;

export default function UserAccount() {
const { params } = useRouter();
return <h1>{`${params.username}’s account.`}</h1>;
}
```

![](img/Figure-5.5.jpg)

**图 5.5:** 嵌套路由

### 应用程序接口 (API)

与页面类似，`api/` 文件夹下任何扩展名为 `*.ts`、`*.js`、`*.mjs` 且内部默认导出函数的文件都会映射到 `/api/*` 并被视为 API 端点。导出的函数类型将为 `APIHandler`。

```ts
// api/users/index.ts
import type { APIHandler} from “aleph/types.d.ts”;

const users = [
  { id: 1, name: “abc”, place: “Munich” },
];

export default function handler(req: APIHandler) {
  // ...
}
```（等待，根据提供的文本重新对齐逻辑）

![](img/Figure-5.6.jpg)

**图 5.6:** API

同时也支持**动态路由**。前面的代码导出了类型为 `APIHandler` 的函数。

```ts
// api/users/index.ts
index.ts
import type { APIHandler} from “aleph/types.d.ts”;

export default function handler({response}: APIHandler) {
  response.json({ message: “Aleph!” });
}
```

![](img/Figure-5.7.jpg)

**图 5.7:** 动态路由

### 初始化应用

我们已经检查了主要部分。现在我们使用 `aleph` 命令初始化应用。

```bash
aleph init
cd app
```

### 项目结构

*图 5.8*所示的项目结构对我们来说很熟悉。

![](img/Figure-5.8.jpg)

**图 5.8:** 项目结构

### Todos API

我们应该修改文件来获取所有现 todos，而不是消息。我们将创建一个包含虚拟 todos 的 Todos 数组，如下所示：

```ts
// api/todos/index.ts
import type { APIHandler} from “aleph/types.d.ts”;

const todos = [
  { id: 1, title: “todo1” },
  { id: 2, title: “todo2” },
];

export default function handler({request, response}: APIHandler) {
  switch (request.method) {
    case “GET”:
      response.json(todos);
      break;
    default:
      response.status = 405;
      response.json({ message: “Action not allowed” });
      break;
  }
}
```

![](img/Figure-5.10.jpg)

**图 5.10:** GET/api/todos 端点





它将响应 `GET` 方法的所有现有 todo（见图 5.10），如果请求的操作在 switch 语句中没有定义，它将返回 `405` Method Not Allowed 代码（见图 5.11）。`break` 会跳过后续的情况，并确保只执行匹配的 case 代码。

![](img/Figure-5.11.jpg)

**图 5.11：** 未定义动作 405 错误

### [POST]

我们现在将实现添加 todo 的 `CREATE (POST)` 动作。

```javascript
…
export const handler: APIHandler = async ({request, response}) => {
  switch (request.method) {
    case “GET”:
      response.json(todos);
      break;
    case “POST”:
      let body;
      try {
        body = await request.json();
      } catch (error) {
        response.status = 400;
        response.json({ error: error.message });
        break;
      }
      const title = body.title ? body.title.toLowerCase() : null;
      if (!title) {
        response.status = 400;
        response.json({
          message: “title not provided”,
        });
        break;
      }
      let todo = todos.find((_todo) => _todo.title === title);
      if (!todo) {
        todo = {
          id: todos[todos.length - 1].id + 1,
          title, // title: title 的简写
        };
        todos.push(todo);
      }
      response.json(todo);
      break;
    default:
      …
```

我们正在使用 `request.json()` 方法解码请求体，该方法将请求体解析为 JSON。如果 JSON 无效或不存在，或者未提供 title，将返回 `400` 代码并带有错误消息。我们正在使用 `toLowerCase()` 函数来获取小写的 todo 标题。这将帮助我们使用 `find` 方法找到具有相同标题的现有 Todo。如果没有找到现有 todo，将创建一个新的 todo 并将其添加到 Todos 列表中。`id` 属性使用了最后一个 todo 项目的 `id`（最后一个 Todo id + 1）。然后将使用 `response.json` 函数返回 Todo（现有的或创建的）。现在，尝试添加一个 todo，如图 5.12 所示。

![](img/Figure-5.12.jpg)

**图 5.12：** POST `api/todos` API 端点

`GET api/todos` 端点应该包含新创建的 Todo，如图 5.13 所示。

![](img/Figure-5.13.jpg)

**图 5.13：** GET api/todos 中新创建的 Todo

现在，通过按下 `Ctrl` + `c` 关闭服务器，并使用 `aleph dev` 命令重新启动。你将看不到新创建的 Todo。这是因为我们没有将数据保存到文件或数据库。为了持久化数据，我们将在 `db` 文件夹中创建一个包含以下 JSON 数据的 `todos.json` 文件。

```json
// db/todos.json
[
  { “id”: 1, “title”: “todo1” },
  { “id”: 2, “title”: “todo2” }
]
```

保存的 todos 随后可以使用 `lib/read_todos.ts` 文件创建的 `readTodos` 工具函数检索。我们正在使用 `Deno.readFileSync` 函数同步读取文本，然后使用 `JSON.parse` 解析 JSON。

```typescript
lib/read_todos.ts
const readTodos = () => JSON.parse(Deno.readFileSync("db/todos.json"));
export default readTodos;
```





```javascript
    response.status = 400;
    response.json({
      error: “title not provided”,
    });
    break;
  }
todos.forEach((_todo: ITodo) => {
  if (_todo.id === todo.id) {
    _todo.title = title;
  }
});
writeTodos(todos);
response.json(todo);
break;
case “DELETE”:
  const _todos = todos.filter((_todo: ITodo) => _todo.id !== id);
  writeTodos(_todos);
  response.json({ message: “Deleted” });
  break;
default:
  response.status = 405;
  response.json({ message: “Action not allowed” });
  break;
}
} else {
…
```

对于 `GET` 方法，我们简单地返回匹配的 Todo。这个 `GET` 方法与 `index.ts` 文件中的方法不同。它仅提供单个 todo（通过提供的 `id` 派生），而 `index.ts` 中的 `GET` 提供了所有 todo 的列表/数组。

对于 `DELETE`，我们从 todos 中过滤掉匹配的 Todo，然后使用 `writeTodos` 函数将更新后的 todos 写入 `todos.json` 文件。

对于 `PATCH`，初始代码与 `index.ts` 文件中的 `POST` 方法类似。我们从 `readBody(“json”)` 提供的 JSON 中获取更新后的标题。然后使用 `forEach`，我们只更新 todos 数据中匹配的 Todo。随后使用 `writeTodos` 函数将更新后的 Todos 保存到文件中，并返回更新后的 Todo。

### 结论

本章已经实现了 Todos App 的 API 端点。我们现在可以使用 Postman 或 `curl` 来测试它们。我们还 学习了 Aleph.js 的功能和基本概念。

下一阶段将为 Todos App 实现 UI。我们将检查 Aleph.js 为 React 开发提供的独特特性，并将在接下来的章节中实现 UI。

# 第 6 章

## Todos App—UI 实现

### 引言

在上一节中，我们为 Todos App 实现了 REST API。在本章中，我们将为它实现 UI。我们将使用一个名为 `aleph.js` 的全栈 React 框架。我们还将使用 `styled components` 库来创建 UI 组件，并使用 `axiod` 进行网络请求。

### 结构

在本章中，我们将涵盖以下主题：

* Styled components
    * Card
    * Text
    * Button
    * Input
    * Checkbox
* Todos components
    * TodoList
    * TodoDetails

### 目标

在完成本章后，你将能够使用 aleph 模块为 react 应用程序创建 UI。你还能够使用 styled components 创建自定义组件并将其集成到应用中。你还能够使用 `axiod` 模块进行网络请求。

### Styled components

Styled components 是一个 React 库，允许我们创建具有组件级作用域的 css 样式的组件。我们将使用该库来创建如 `Button`、`Text`、`Card` 等组件。从上一节初始化的终端切换到 `todos-app` 文件夹。要安装 styled-components，我们将使用以下 `trex` 命令：

```bash
trex -c styled=”https://esm.sh/styled-components@5.3.1”
```

安装完成后，我们将在 `StyledComponents.tsx` 文件中创建各种组件。每个组件的代码如下：

```typescript
import styled, { css } from “styled”

export const Card = styled.div`
    display: flex;
    flex-direction: row;
    background: #ddd;
    border-radius: 5px;
    margin: 10px;
    justify-content: space-between;
    align-items: center;
    max-width: 600px;
    margin: “auto”;
`

export const Text = styled.span`
    font-size: 20px;
    font-weight: bold;
    flex: 1;
    margin-left: 10px;
    ${props => props.completed && css`
      text-decoration: line-through;
      color: grey
    `}
`

export const Button = styled.button`
    /* 根据 primary prop 调整颜色 */
    background: ${props => props.primary ? “palevioletred” : “white”};
    color: ${props => props.primary ? “white” : “palevioletred”};
    font-size: 1em;
    margin: 1em;
    padding: 0.25em 1em;
    border: 2px solid palevioletred;
    border-radius: 3px;
    cursor: pointer;
    ${props => props.disabled && css`
      background: lightgrey;
      cursor: not-allowed;
      border: 2px solid lightgrey;
    `}
`

export const Input = styled.input`
    flex: 1;
    padding: 10px;
    margin: 10px;
    border: none;
    background: #ddd;
    font-size: 20px;
    font-weight: bold;
    ${props => props.completed && css`
      text-decoration: line-through;
      color: grey
    `}
`

export const Checkbox = styled.input`
    type: “checkbox”;
    color: red;
    margin-left: 10px;
`

export const Header1 = styled.h1
``
```

在前面的代码中，我们使用 `styled` 和来自 `styled` 组件的 `css` 来化如 `Card`、`Button`、`Text` 等组件。每个组件随后导出并在项目中使用。我们通过这种方法创建了自己的库。

我们向某些组件传递函数。这些函数根据 props 设置值。我们使用 `Text` 和 `Input` 组件中的 `completed` 属性来调整颜色和装饰线。我们使用 `Button` 组件中的 `primary` 标记来调整颜色。

### 创建 Todos 组件

现在我们将在 `TodoDetails` 和 `TodoList` 组件中使用自定义样式组件。我们将首先在 `pages/index.tsx` 文件中添加 `TodoList` 组件，它是我们项目的入口，如下：

```typescript
import React from ‘react’
import TodoList from “components/TodoList.tsx”
export default function Home() {
  return <TodoList />
}
```

将在下一节检查 `TodoList` 组件的详情。

### TodoList

此组件用于添加新的 Todo 并列出有的 Todos。我们将使用 `StyledComponents.tsx` 文件中的自定义组件。API 调用将通过 `axiod` 模块完成。该文件的代码如下：

```typescript
// components/TodoList.tsx
import React from ‘react’
import { useDeno } from “https://deno.land/x/aleph/framework/react/mod.ts”;
import axiod from “axiod”;
import TodoDetails from "./TodoDetails.tsx";
import { Button, Card, Input, Header1 } from "./StyledComponents.tsx";
import readTodos from “../lib/read_todos.ts”;
export default function Page() {
  const _todos = useDeno(async () => {
    return await readTodos();
  }, { revalidate: 1 });
  const [todos, setTodos] = React.useState(_todos);
  const [todoInput, setTodoInput] = React.useState("");

  const getTodos = () => {
    axiod.get(/api/todos”).then((res) => {
      console.log(res);
      setTodos(res.data);
    }).catch((err) => {
      console.log(err);
    });
  };

  const addTodo = () => {
    if (!todoInput) {
```




```javascript
30.      alert("Please enter a todo text");
31.      return;
32.    }
33.    axiod.post("/api/todos", { title: todoInput }).then((res) => {
34.        console.log(res);
35.        getTodos();
36.        alert("Todo added successfully");
37.    }).catch((err) => {
38.        console.log(err);
39.        alert("Error adding todo");
40.    });
41.  };
42.  return (
43.    <>
44      <Header1>Todos</Header1>
45      <Card>
46          <Input
              placeholder="Add Todo"
              value={todoInput}
              onChange={(e) => setTodoInput(e.target.value)}
            />
47          <Button primary onClick={addTodo}>+</Button>
48      </Card>
49      {todos.map((todo: any) => <TodoDetails key={todo.id} getTodos={getTodos} todo={todo} />)}
50.    </>
51.  );
52. }
```

在前面的代码中，我们导入了自定义组件、`axiod` 模块和 `readTodos` 函数。我们还导入了 `useDeno` 函数，它允许在组件中使用 Deno 运行时。我们从它的 JSON 文件中获取 Todos。状态 `todos` 用于存储 Todo 列表，而 `todoInput` 则用于存储添加 Todo 文本框的输入内容。

我们正在使用 `getTodos` 函数通过使用 `axiod` 模块进行 API 调用来获取 Todos。获取到的 Todos 随后存储在 `todos` 状态中。同样，`addTodo` 函数被用于发送 `POST` 请求以向 JSON 文件中添加新的 Todo。我们将 `todoInput` 作为 `title` 传递到请求体中。如果 Todo 添加成功，我们将使用 `getTodos` 函数重新获取 Todos。

我们使用样式化组件 `Header1`、`Card`、`Input` 和 `Button` 来创建 UI。`TodoDetails` 组件用于渲染每个 Todo 的详情。我们将在下一节中检查它的详细信息。

图 6.1 显示了带有添加 Todo 输入的 `TodoList` 组件。

![](img/Figure-6.1.jpg)

**图 6.1：** TodoList 组件

### TodoDetails

我们将使用此组件来渲染每个添加的 `todo` 元素。我们将提供两个操作，即保存（Save）和删除（Delete）。我们还将使用一个 `checkbox` 元素来标记 Todo 为已完成。该组件的代码写在 `TodoDetails.tsx` 文件中，如下：

```typescript
// components/TodoDetails.tsx
3. import React from "react";
4. import { Button, Card, Checkbox, Input, Text } from "./StyledComponents.tsx";
5. import axiod from "axiod";
7. interface ITodo {
8.   id: number;
9.   title: string;
10.  completed: boolean;
11. }
13. interface IProps {
14.  todo: ITodo;
15.  getTodos: () => void;
16. }
18. function TodoDetails(props: IProps) {
19.  const { todo, getTodos } = props;
20.  const [isCompleted, setIsCompleted] = React.useState(todo.completed);
21.  const [todoText, setTodoText] = React.useState(todo.title);
23.  const editTodo = () => {
24.    if (!todoText) {
25.      alert("Please enter a text");
26.      return;
27.    }
28.    axiod.patch(`/api/todos/${todo.id}`, {
29.      title: todoText,
30.      completed: isCompleted,
31.    }).then((res) => {
32.      console.log(res);
33.      alert("Todo updated successfully");
34.    }).catch((err) => {
35.      console.log(err);
36.      alert("Error updating todo");
37.      setTodoText(todo.title);
38.    });
39.  };
40.  const deleteTodo = () => {
41.    axiod.delete(`/api/todos/${todo.id}`, { title: todoText }).then((res) => {
42.      console.log(res);
43.      alert("Todo deleted successfully");
44.      getTodos();
45.    }).catch((err) => {
46.      console.log(err);
47.      alert("Error deleting todo");
48.    });
49.  };
50.  return (
52.    <Card>
53.      <Checkbox
54.        type="checkbox"
55.        defaultChecked={isCompleted}
56.        onChange={() => setIsCompleted(!isCompleted)}
57.      />
58.      <Input
59.        completed={isCompleted}
60.        value={todoText}
61.        onChange={(e) => setTodoText(e.target.value)}
62.        disabled={isCompleted}
63.      />
64.      <Button primary onClick={editTodo}>Save</Button>
65.      <Button onClick={deleteTodo}>Delete</Button>
66.    </Card>
67.  );
68. }
71. export default TodoDetails;
```



在本章中，我们将学习核心 `Graph Query Language`（`GraphQL`）概念及其特性。在涵盖了基础知识后，我们将在接下来的章节中利用这些概念为 `Phonebook` 应用创建一个 API 服务器（`GraphQL`）。我们还将介绍 `Oak Web` 框架和 `Oak GraphQL`。两者都将在后续章节中用于 GraphQL API 服务器的实现。

### 结构

在本章中，我们将涵盖以下主题：

*   GraphQL 简介
    *   特性
        *   精确获取
        *   单一 API 端点
        *   验证与类型检查
        *   片段 (Fragments)
        *   自动生成的 API 文档
    *   核心概念
        *   Schema（模式）
            *   类型 (Type)
            *   输入 (Input)
            *   查询 (Query)
            *   变更 (Mutation)
            *   关系 (Relationship)
        *   Resolver（Resolver）
*   引入 Oak 框架
*   引入 Oak-GraphQL

### 目标

完成本章后，你将能够理解并应用 GraphQL 核心概念，如查询、变更、解析器、类型定义等。你还应该能够使用 Oak 框架创建 Deno Web 服务器，并使用 Oak-GraphQL 模块创建 GraphQL 服务器。

### 引入 GraphQL

GraphQL 是由 Facebook 开发并在 2015 年发布的开源 API 查询语言。它允许客户端控制解析后的数据结构，而不是 REST 中固定的数据结构。通过这种方式，客户端可以仅`query` 所需精确数据。它还允许 `mutations`（写入或更改数据）和 `subscriptions`（订阅数据更新）。许多大型组织如 Facebook、GitHub、Coursera 和 Pinterest 等都在使用它。

### 特性

GraphQL 允许客户端在单个请求中跨多个资源`查询或更改数据`。它创建了一个单一入口或 API 端点 POST `/graphql` 来查询或更改数据。GraphQL 提供的解析数据格式与请求查询的格式相同。其他 GraphQL 特性将详细说明如下。

### 精确获取

通过允许仅获取所需的数据，GraphQL 解决了数据相关问题，即客户端获取了多于所需的数据（过度获取）或少于所需的数据（获取不足）。

### 单一 API 端点

与 REST 不同，GraphQL 始终有一个单一的端点 `/graphql (POST)`，客户端可以使用它来获取 schema 中定义的任何数据，因为 GraphQL 使用通过请求体传递的 `query` 来解析请求。

*[图 7.1]* 通过在正文中提供所示的 `users` 查询使用 `/graphql` 端点获取 `users` 数据：

![](img/Figure-7.1.jpg)

**图 7.1:** 获取用户

*[图 7.2]* 通过在正文中提供所示的 `todos` 查询使用相同的端点 `/graphql` 获取 `Todos 数据`：

![](img/Figure-7.2.jpg)

**图 7.2:** 获取 Todos

如`[图 7.1]`和`[7.2]`所示，GraphQL 允许通过单一 API 端点使用`query 操作`来获取 `users` 和 `todos`。

我们甚至可以在单个请求中获取 `users` 和 `todos`。这是 GraphQL 一个非常强大的特性，允许客户端在单个请求中获取所有所需数据，这对于网络较慢的设备极其有用。

*[图 7.3]* 所示如何在单个请求中同时获取 `users` 和 `todos`：

![](img/Figure-7.3.jpg)

**图 7.3:** 获取用户和 Todos

### 验证与类型检查

GraphQL 使用`type system` 来验证查询。客户端可以在发送请求之前检查哪些字段是可选（带有字段类型），以及查询是否有效。

*[图 7.4]* 展示了针对 `todos` 的验证和类型检查概念，其中 schema 中未定义 `someField` 字段：

![](img/Figure-7.4.jpg)

**图 7.4:** 验证

### 片段 (Fragments)

GraphQL 允许编写可重用的代码 `fragment`，该片段可以在多个查询之间使用。我们可以创建一个片段来替换重复的代码单元，使查询更整洁、更具可读性。

*[图 7.5]* 显示了 `todos`（获取所有 Todos）和 `todo`（通过 id 获取单个 Todo）查询中重复的代码单元：

![](img/Figure-7.5.jpg)

![](img/Figure-7.5.jpg)

**图 7.5:** 重复的代码单元

我们将把重复的代码单元移动到 `todoData` 片段中，并在两个查询中使用扩展运算符（`…`）使用它。

*[图 7.6]* 展示了使用 `fragment` 获取 `todos` 和 `userData`。

### 自动生成的 API 文档

GraphQL 为*queries*和*mutations*生成 API 文档。*图 7.7* 显示了 `todo` 的自动生成文档。如果我们把 `user` 改为 `Int`，文档将反映此变化。

### 核心概念

GraphQL 提供了一个解析请求的 `Resolver`，以及用于读取数据的 `query`、用于写入数据的 `mutations` 和用于实时数据的 `subscription`。

### Schema

`type system` 是客户端和服务器之间的约，定义了数据的形状。它定义了描述实体或字段的 `types`。GraphQL 使用 Schema 定义语言 (SDL) 来定义 schema。一个示例应用定义如下：

```graphql
type User {
  userId: String!
  name: String!
  todos: [Todo!]
}

type Todo {
  todoId: String!
  title: String!
  user: User!
}

input UserInput {
  name: String!
}

input TodoInput {
  title: String!
  userId: String!
}

type Query {
  todos: [Todo!]
  todo(todoId: String!): Todo!
  users: [User!]
  user(userId: String!): User!
}

type Mutation {
  addTodo(todo: TodoInput!): Todo
  addUser(user: UserInput!): User
}
```

此 schema 也可以通过 GraphQL Playground 查看，如`[图 7.9]`所示。

![](img/Figure-7.9.jpg)

**图 7.9:** GraphQL schema

解释上述 schema 中使用的各种关键字（`type` 和 `input`）：

### Type

Type 用于定义解析查询的形状。图 7.9 所示的 schema 定义了两个对象类型 `User` 和 `Todo`。`User` 类型定义了字段 `userId`、`name` 和 `todos`（`Todo` 对象数组）。`Todo` 类型定义了字段 `todoId`、`title` 和 `user`（类型为 `User`）。这两个对象类型都被 `Query` 类型用于以返回相应的数据。

### Input

Input 用于定义变更的数据结构。




Input 用于定义在 `mutation` 过程中客户端输入的形状。它定义了两个 `input types`（输入类型）：`UserInput` 和 `TodoInput`。`UserInput` 接受一个 `name` 参数，而 `TodoInput` 接受 `title` 和 `userId` 参数。这两个输入类型都用于通过 `mutation` 类型创建或更新相应的实体。

### Query

定义由客户端执行的 `read` 操作的入口。query 中定义了四个字段：`todos`、`todo`、`users` 和 `user`。`todos` 和 `users` 字段不接受参数并返回对应类型的数组。`todo` 和 `user` 字段接受实体的 `id` 并返回对应类型的实体。

### Mutation

定义由客户端执行的 `write` 操作的入口。该类型中定义了 `addTodo` 和 `addUser` 字段。`addTodo` 接受类型为 `TodoInput` 的参数并返回 `Todo` 类型的数据，而 `addUser` 接受类型为 `UserInput` 的参数并返回 `User` 类型的数据。

### Relationship

Todos schema 定义了 `User` 类型和 `Todo` 类型之间的“一对多”关系。这意味着每个 `Todo` 拥有`一个`用户，而每个 `user` 拥有`多个` Todo。

如`[图 7.10]`所示，GraphQL 赋予了客户端活性，可以在单个查询中获取所有与用户相关的 Todos。

![](img/Figure-7.10.jpg)

**图 7.10:** 关系

### Resolver

Resolver 是一个函数，通过为 schema 中的单个字段填充数据来解析 `query` 或 `mutation`。以下代码演示了为之前定义的 schema 使用 `resolvers`：

```javascript
export const resolvers = {
  Query: {
    todos: (parent: any, args: any, context: any, info: any) => {
      if (args.userId) return getTodosByUserId(args.userId);
      return getTodos();
    },
    todo: async (parent: any, args: any, context: any, info: any) => {
      return getTodo(args._id);
    },
    users: (parent: any, args: any, context: any, info: any) => {
      return getUsers();
    },
    user: async (parent: any, args: any, context: any, info: any) => {
      return getUser(args._id);
    },
  },
  Mutation: {
    addTodo: async (parent: any, args: any, context: any, info: any) => {
      const { title, userId } = args.todo;
      return createTodo(title, userId);
    },
    addUser: async (parent: any, args: any, context: any, info: any) => {
      const { name } = args.user;
      const user = createUser(name);
      return user;
    },
  },
  Todo: {
    title: (parent: any, args: any, context: any, info: any) => {
      return parent.title;
    },
    user: async (parent: any, args: any, context: any, info: any) => {
      const user = await info.rootValue.user(
        parent,
        { _id: parent.userId },
        context,
        info
      );
      return user;
    },
  },
  User: {
    name: (parent: any, args: any, context: any, info: any) => {
      return parent.name;
    },
    todos: async (parent: any, args: any, context: any, info: any) => {
      const todos = await resolvers.Query.todos(
        parent,
        { userId: parent._id },
        context,
        info
      );
      return todos;
    },
  },
};
```

让我们看看上述代码中发生了什么。我们定义了 `Query`、`Mutation`、`Todo` 和 `User` 对象。`Query` 对象包含 `todos`（列表）、`todo`、`users` 和 `user` 对象。同样，`Mutation` 包含 `addTodo` 和 `addUser` 对象，每个对象具有相同的签名。其他对象 `User` 和 `Todo` 用于解析各自类型的内部字段（title 等）。数据随后可以从各种来源中获取。每个对象之前都接受可选参数：`parent`、`args`、`context` 和 `info`。

`parent` 是字段父字段的返回值，`args` 包含所有 GraphQL 参数，`context` 是一个内容在所有 resolver 中可用的对象，而 `info` 包含如字段名、路径等信息。

### Oak framework

Oak 是一个用于 Deno 的 Web 框架，灵感来源于 node.js 的 `koa` 框架。它提供了在请求和响应之间调用的中间件函数。Oak 提供了 `use()` 方法来使用中间件函数。以下代码演示了 oak 中的 `Hello World` 服务器：

```javascript
import { Application } from "https://deno.land/x/oak@v7.7.0/mod.ts";

const app = new Application();

app.use((ctx) => {
  ctx.response.body = "Hello World!";
});

await app.listen({ port: 8000 });
```

在上述代码中，`Application` 实例 `app` 使用 `context` 调用每个中间件，`context` 包含了必要的信息如 `app`、`cookies`、`request`、`response`、`state`、`assert()` 和 `throw()`。最后，服务器使用 `listen()` 方法在端口 `8000` 上监听。

### Oak-GraphQL middleware

Oak-GraphQL 模块允许我们在 oak 服务器之上创建 GraphQL API。我们将使用 Oak-GraphQL 中间件来实现 GraphQL API。简单的 Hello World GraphQL API 可以如下设置：

```typescript
// oak_graphql_server.ts
import {
  Application,
  Router,
  RouterContext,
} from "https://deno.land/x/oak@v9.0.0/mod.ts";
import {
  applyGraphQL,
  gql,
  GQLError,
}

const types = gql`
  type Query {
    hello(name: String): String
  }
`;

const resolvers = {
  Query: {
    hello: (parent: any, { name }: any, context: any, info: any) => {
      if (!name) throw new GQLError("Name not provided");
      return `Hello ${name}`;
    },
  },
};

const GraphQLService = await applyGraphQL<Router>({
  Router, // 同于 Router:
  typeDefs: types,
  resolvers: resolvers,
});

const app = new Application();
app.use(GraphQLService.routes(), GraphQLService.allowedMethods());

console.log("Server listening on http://localhost:8080/graphql");
await app.listen({ port: 8000 });
```

如果我们使用命令 `deno run --allow-net oak_graphql_server.ts` 运行上述代码，并在 URL `http://localhost:8080/graphql` 中查询 `{ hello(name: “ABC”) }`，我们应该看到如 `[图 7.11]` 所示的结果如下：





![](img/Figure-7.11.jpg)

**图 7.11:** GraphQL API Hello World

### 结论

我们已经涵盖了 GraphQL 的基本功能和概念，例如模式（schema）、解析器（resolver）以及类型（type）、查询（query）和变更（mutation）。我们还介绍了用于创建 Web 服务器的 `oak` 框架以及用于创建 GraphQL 服务器的 `Oak-GraphQL` 模块。

在接下来的章节中，我们将使用上述 GraphQL 概念，利用 `Oak` 和 `Oak-GraphQL` 模块为电话录应用创建一个 GraphQL API 服务器。

# 第 8 章

## 电话录应用—API 实现

### 引言

在本章中，我们将实现**图形查询语言**（**GraphQL 应用程序接口**服务器。我们之前学习的 GraphQL 基础将在本章用于 API 实现。我们将使用之前介绍的 `oak` 和 `oak-graphql` 模块来实现 API 服务器。

### 结构

在本章中，我们将涵盖以下主题：

*   初始化设置
    *   使用 `git` 进行版本控制
    *   使用 `Trex` 作为包管理器
    *   使用 `Velociraptor` 作为脚本运行器
*   `Oak GraphQL` 服务器设置
*   模式 (Schema)
*   解析器 (Resolvers)
*   `DenoDB` 设置
    *   数据库 (DB)
        *   `ElephantSQL PostgreSQL` 设置
    *   模型 (Models)
        *   `User`
        *   `Contact`
    *   控制器 (Controllers)
*   身份验证

### 目标

完成本章后，你将能够使用 `Oak` 和 `Oak-GraphQL` 模块创建 GraphQL API 服务器。你将学习使用 `denodb` 模块通过**对象关系映射 (ORM)** 连接到 MySQL、PostgreSQL、NoSQL 等数据库。你还将学习使用 `djwt` 模块通过 **JSON Web 令牌 (JWT)** 验证用户身份。你也将学习使用 `trex` 和 `velociraptor` 模块设置 Deno 服务器项目。

### 初始化设置

我们将通过初始化 git 仓库开始编写代码。然后我们将安装 `oak` 和 `oak-graphql` 模块来创建 Web 服务器。我们将使用 `trex` 包管理模块来安装这些模块。

### 使用 git 进行版本控制

*[图 8.1]* 显示了 git 仓库初始化、安装 `trex` 模块以及使用 `trex` 模块安装 `oak` 和 `oak-graphql`。

![](img/Figure-8.1.jpg)

**图 8.1:** 初始化设置

### Trex 作为包管理器

Trex 缓存已安装的包并将其添加到 `import_map.json` 文件中。[图 8.2]* 显示了 `import_map.json` 文件中已安装模块列表（`oak`、`oak-graphql`）。

![](img/Figure-8.2.jpg)

**图 8.2:** import_map.json 中的安装模块

已安装的模块可以通过以下方式访问：

1.  `import { Application } from “oak”;`

### Velociraptor 作为脚本运行器

在 `src` 文件夹中创建一个名为 `mod.ts` 文件，代码如下：

```javascript
console.log("Hello Velociraptor!");
```

你可能会问什么是 velociraptor。它是用于 Deno 的脚本运行器模块。我们将安装 velociraptor 并使用它运行 `mod.ts` 文件。可以使用 [`nest.land/`](https://nest.land/) 包注册表按照如下方式安装 velociraptor：

```bash
deno install -qAn vr https://x.nest.land/velociraptor@1.1.0/cli.ts
```

现在我们将创建 `scripts.yaml` 文件以添加运行 `mod.ts` 文件的脚本。Veliraptor 将扩展名为 `yml`、`yaml`、`json` 和 `ts` 且名为 `scripts` 或 `velociraptor` 的文件识别为脚本文件。

*[图 8.3]* 显示了带有执行 `src/mod.ts` 文件的 `dev` 脚本的 `scripts.yaml` 文件。

![](img/Figure-8.3.jpg)

**图 8.3:** scripts.yaml 文件

如果我们在终端中运行 `vr` 命令，将看到可用脚本列表。然后我们可以如下所示运行可用脚本：

```bash
vr dev
```

*[图 8.4]* 显示了列出可用脚本和运行脚本的命令。

![](img/Figure-8.4.jpg)

**图 8.4:** Velociraptor CLI

我们已经使用 trex 和 velociraptor 设置了一个 Deno 服务器项目。现在，我们将在下一节中设置 Web 服务器。

### Oak GraphQL 设置

我们将使用 `oak` 和 `oak-graphql` 模块设置一个简单的 GraphQL 服务器。我们将使用第 7 章“GraphQL 简介”中的 `oak-graphql` 代码，并进行少量更改来设置服务器。我们不再需要提到 URL。相反，我们可以在 `import_map.json` 中提到模块名。

```javascript
import { Application, Router } from "oak";
import { gql, GQLError } from "oak-graphql";
```

我们将通过拥有 `mod.ts`（主文件）、`middlewares.ts`（GraphQL 中间件）、`schema.ts`（GraphQL 模式/类型定义）和 `resolvers.ts`（GraphQL 解析器）文件来构建项目。[图 8.5]* 显示了项目结构：

![](img/Figure-8.5.jpg)

**图 8.5:** 项目结构

我们将逐个编写每个文件的代码，从 `mod.ts` 文件开始如下：

```javascript
// src/mod.ts
import { Application } from "oak";
import { GraphQLService } from "./middlewares.ts";
const app = new Application();
app.use(GraphQLService.routes(), GraphQLService.allowedMethods());
console.log("Server listening on http://localhost:8080/graphql");
await app.listen({ port: 8080 });
```

在前面的代码中，我们正在创建一个带有名为 `GraphQLService` 的 de 间件的 oak 服务器，可以通过 `/graphql` 路由访问。

```javascript
// src/schema.ts
import { gql } from "oak_graphql";
export const types = gql`
  type Query {
    hello(name: String): String
  }
`;
```

在 `schema.ts` 文件中，我们定义了一个接受 `name` 参数的 `hello` 查询。GraphQL 根据 `types` 中定义的模型进行验证。进入请求将由 `resolvers` 解析。

```javascript
// src/resolvers.ts
import { GQLError } from "oak_graphql";
export const resolvers = {
  Query: {
    hello: (parent: any, { name }: any, context: any, info: any) => {
      if (!name) throw new GQLError("Name not provided");
      return `Hello ${name}`;
    },
  },
};
```

我们需要更新 `scripts.yaml` 文件以 `import_map` 文件路径和权限。更新后的文件具有如下代码：

```yaml
## scripts.yaml
imap: import_map.json
unstable: true
allow:
  - net
scripts:
  dev:
    cmd: src/mod.ts
    desc: "run graphql server in dev mode"
    watch: true
```

在前面的代码中，`imap` 指向 `import_map` 文件路径，`unstable` 标志允许执行不 Deno 功能，`allow` 包含了网络访问。我们为 `dev` 命令添加了 `cmd`（执行命令）、`desc`（描述）和 `watch`（文件监听）字段。

### 模式 (Schema)

模式是一种定义数据形状的系统。它为客户端提供可用的数据字段、查询和变更。我们已经在后续章节中通过代码学习了模式相关的概念。我们将按照所示代码为 `User` 和 `Contact` 实体添加 `types`、`queries` 和 `mutations`：

```javascript
// src/schema.ts
import { gql } from "oak_graphql";
export const types = gql`
  type User {
    userId: String!
    name: String!
    contacts: [Contact!]!
    email: String!
  }
  type Contact {
    contactId: String!
  }
`;
```





```graphql
  name: String!
  phone: String
  email: String
  address: String
  user: User!
}
type Login {
  token: String!
}
input RegisterUserInput {
  name: String!
  email: String!
  password: String!
}
input LoginUserInput {
  email: String!
  password: String!
}
input UpdateUserInput {
  name: String
}
input CreateContactInput {
  name: String!
  phone: String
  email: String
  address: String
}
input UpdateContactInput {
  contactId: String!
  name: String
  phone: String
  email: String
  address: String
}
type Query {
  user: User
  contacts: [Contact]
  contact(contactId: String!): Contact
  login(user: LoginUserInput): Login
}
type Mutation {
  registerUser(user: RegisterUserInput!): User
  deleteUser: Boolean
  updateUser(user: UpdateUserInput!): Boolean
  addContact(contact: CreateContactInput!): Contact
  deleteContact(contactId: String!): Boolean
  updateContact(contact: UpdateContactInput!): Boolean
}
```





```javascript
71.  if (contactId) return updateContact(contactId, contactData);
72.  },
73.  },
74.  User: {
75.    name: (parent: any, args: any, context: any, info: any) => {
76.      return parent.name;
77.    },
78.    contacts: async (parent: any, args: any, context: any, info: any) => {
79.      const contacts = await resolvers.Query.contacts(
80.        parent,
81.        {},
82.        context,
83.        info
84.      );
85.      return contacts;
86.    },
87.  },
88.  Contact: {
89.    name: (parent: any, args: any, context: any, info: any) => {
90.      return parent.name;
91.    },
92.    user: async (parent: any, args: any, context: any, info: any) => {
93.      return await userLoader.load(parent.userId);
94.    },
95.  },
96. };
```

我们的解析器（resolvers）代码基于上一章节的解析器代码。我们定义了 `Query`、`Mutation`、`User` 和 `Contact` 对象，每个对象包含解析器。`Query` 对象包含 `user`、`contacts`、`contact` 和 `login` 解析器。`Mutation` 包含 `registerUser`、`updateUser`、`deleteUser`、`addContact`、`updateContact` 和 `deleteContact` 解析器。其他对象 `User` 和 `Contact` 用于解析相应类型的内部字段（名称等）。数据可以从各种来源获取。每个解析器函数都接受可选参数 `parent`、`args`、`context` 和 `info`，这些在上一章节中已经解释过。

图 8.6 显示了 `resolvers.ts` 文件中所有解析器的列表

![](img/Figure-8.6.jpg)

**图 8.6：** 解析器

在解析查询时，我们需要执行诸如数据库读/写、身份验证等操作。我们在 `controllers.ts` 文件中处理数据库操作，并在 `auth.ts` 文件中处理身份验证。

将在 `models.ts` 文件中定义的数据库模型 `User` 和 `Contact` 执行查询、创建、更新和删除操作。我们需要设置数据库并将其与模型链接，以便在控制器中使用这些模型。让我们使用名为 `denodb` 的 Deno 模块来设置数据库并创建模型。

## 数据库设置

我们将使用 `ElephantSQL` 设置一个 PostgreSQL 数据库。访问 [`www.elephantsql.com/`](https://www.elephantsql.com/) 并使用你的账户登录/注册。完成后，我们需要创建一个名为 `phonebook` 的实例，并选择 `tiny turtle (free)` 计划。打开创建的实例，并复制 `Details` 部分提到的 `URL`。我们将在 `.env` 文件中如下设置名为 `DATABASE_URL` 的环境变量：

1. `// .env`
2. `// 将以下 url 替换为 elephantsql url`
3. `DATABASE_URL=postgres://deno_admin:deno_admin@localhost:5432/deno_db`

现在，为了在代码中访问 `DATABASE_URL`，我们将在 `scripts.yaml` 文件中带有 `.env` 文件的 `envFile` 标记：

1. `# scripts.yaml`
2. `…`
3. `allow:`
4. `  - net`
5. `  - env`
6. `  envFile:`
7. `  - .env`
8. `…`

使用 `deno add -c https://deno.land/x/denodb/mod.ts` 安装 `denodb`，并在 `db.ts` 文件中使用 `PostgresConnector` 连接数据库 URL：

```typescript
import { Database, PostgresConnector } from "denodb";
const DATABASE_URL = Deno.env.get("DATABASE_URL") as string;
const connector = new PostgresConnector({
  uri: DATABASE_URL,
});
export const db = new Database(connector);
```

下一节将使用上述数据库并链接数据库模型 `User` 和 `Contact`。

### 模型

我们将使用 `denodb` 模块中的 `Model`、`DataTypes` 和 `Relationships` 定义两个模型：`User` 和 `Contact`。两个模型的代码如下：

```typescript
// src/models.ts
import { Model, DataTypes, Relationships } from "denodb";
import { db } from "./db.ts";
import { v4 } from "uuid";

export class User extends Model {
  static table = "users";
  static timestamps = true;
  static fields = {
    userId: {
      type: DataTypes.STRING,
      primaryKey: true,
    },
    name: { type: DataTypes.STRING, length: 50 },
    isActive: { type: DataTypes.BOOLEAN },
    email: { type: DataTypes.STRING },
    password: { type: DataTypes.STRING },
  };
  static defaults = {
    userId: v4.generate,
    name: "ABC",
    isActive: true,
  };
  static contacts() {
    return this.hasMany(Contact);
  }
}

export class Contact extends Model {
  static table = "contacts";
  static timestamps = true;
  static fields = {
    contactId: {
      type: DataTypes.STRING,
      primaryKey: true,
    },
    name: { type: DataTypes.STRING, length: 100 },
    phone: { type: DataTypes.STRING, length: 50, allowNull: true },
    email: { type: DataTypes.STRING, length: 100, allowNull: true },
    address: { type: DataTypes.STRING, length: 200, allowNull: true },
  };
  static defaults = {
    contactId: v4.generate,
    name: "Learn Deno",
    isCompleted: false,
  };
  static user() {
    return this.hasOne(User);
  }
}

Relationships.belongsTo(Contact, User);
db.link([User, Contact]);
await db.sync({ drop: true });
```

对于两个模型，我们定义了 `table`、`timestamps`、`fields`、`defaults` 和 `relationship` 静态属性。`table` 将是数据库表的名称，例如 `User` 模型对应 `users`，`Contact` 模型对应 `contacts`。我们将 `timestamps` 设置为 `true` 以为模型添加 `created_at` 和 `updated_at` 字段。

### 控制器

我们需要通过控制器将解析器与模型映射。每个控制器将对模型执行数据库操作，以获取、创建、更新和删除实体。所有的控制器函数都添加到 `controllers.ts` 文件中：

```typescript
import { User, Contact } from "./models.ts";
import { GQLError } from "oak_graphql";
import DataLoader from "dataloader";
import { hash } from "scrypt";

interface IContact {
  name: string;
  phone: string;
  email: string;
  address: string;
}
```





```typescript
export const getUser = async (userId: string) => {
  return await User.find(userId);
};

export const getUserByEmail = async (email: string) => {
  const existingUser = await User.where("email", email).first();
  return existingUser;
};

export const createUser = async (
  name: string,
  email: string,
  password: string
) => {
  const existingUser = await getUserByEmail(email);
  if (existingUser) throw new GQLError("User already exists");
  const hashedPassword = await hash(password);
  const user = await User.create({ name, email, password: hashedPassword });
  return user;
};

export const deleteUser = async (userId: string) => {
  await Contact.where("userId", userId).delete();
  await User.deleteById(userId);
  return null;
};

export const updateUser = async (userId: string, userData: any) => {
  await User.where("userId", userId).update(userData);
  return null;
};

export const getContactsByUserId = async (userId: string) => {
  return await User.where("userId", userId).contacts();
};

export const getContact = async (contactId: string) => {
  return await Contact.find(contactId);
};

export const createContact = async (contactData: IContact, userId: string) => {
  const existingUser = await User.where("userId", userId).get();
  if (!existingUser.length) throw new GQLError("User does not exist");
  const contact = await Contact.create({ ...contactData, userId });
  return contact;
};

export const deleteContact = async (userId: string) => {
  await Contact.deleteById(userId);
  return null;
};

export const updateContact = async (contactId: string, contactData: any) => {
  await Contact.where("contactId", contactId).update(contactData);
  return null;
};

const batchGetUsersByIds = (ids: any) => {
  const userPromises = ids.map(getUser);
  const usersPromise = Promise.resolve(userPromises);
  return usersPromise;
};

export const userLoader = new DataLoader(batchGetUsersByIds);
```

在前面的代码中，我们为 `User` 模型查询定义了 `getUser`、`getUserByEmail`、`createUser`、`deleteUser` 和 `updateUser` 函数，并为 `Contact` 模型查询定义了 `getContactsByUserId`、`getContact`、`updateContact` 和 `deleteContact` 函数。我们使用 `find`、`where`、`create`、`deleteById`、`update` 和 `delete` 模型方法来执行这些操作。

我们还定义了 `batchGetUsersByIds` 函数，作为 `dataloader` 函数使用。它在单次数据库调用中收集所有的用户 ID 和所有用户。然后，它返回一个解析为该数组的 promise。我们需要使用以下命令安装 `dataloader` 来启用此功能。

```bash
trex -c dataloader=https://esm.sh/dataloader@2.0.0/index.js
```

此外，我们在 `createUser` 函数中使用由 `scrypt` 模块提供的 `hash` 函数对密码进行哈希处理（将密码转换为另一个字符串）。我们将使用以下命令安装 `scrypt` 模块：

```bash
trex i -c https://deno.land/x/denOBodb/mod.ts
```

# 认证

为了识别请求的用户，我们将使用 `djwt` 模块来创建和验证 JSON Web Token (JWT)。我们需要在 `.env` 文件中设置 `SECRET_KEY`（随机字符串），它将在 JWT 的创建和验证期间使用。所有与认证相关的代码都写在 `auth.ts` 文件，如下：

```typescript
// src/auth.ts
import { create, verify } from "djwt";
import { RouterContext } from "oak";
import { verify as hashVerify } from "scrypt";

const SECRET_KEY = Deno.env.get("SECRET_KEY");
const ALGORITHM = "HS256";

export const authenticate = async (user: any, password: string) => {
  if (await verifyPassword(password, user.password)) {
    return createToken(user);
  }
};

const verifyPassword = async (password: string, hashedPassword: string) => {
  const isValidPassword = await hashVerify(password, hashedPassword);
  return isValidPassword;
};

const createToken = async (user: any) => {
  if (!SECRET_KEY) {
    throw new Error("SECRET_KEY not set as environment variable");
  }
  const jwt = await create(
    { alg: ALGORITHM, typ: "JWT" },
    { userId: user.userId },
    SECRET_KEY
  );
  return jwt;
};

export const setContextUser = async (ctx: RouterContext) => {
  const token = parseToken(ctx);
  if (!token) return null;
  const user = await verifyToken(token);
  return user;
};

const parseToken = async (ctx: RouterContext) => {
  const authorizationHeader = ctx.request.headers.get("authorization");
  const parts = authorizationHeader ? authorizationHeader.split(" ") : [];
  const token =
    parts.length === 2 && parts[0].toLowerCase() === "bearer"
      ? parts[1]
      : undefined;
  return token;
};

const verifyToken = async (token: string | undefined) => {
  if (token) {
    if (!SECRET_KEY) {
      throw new Error("SECRET_KEY not set as environment variable");
    }
    const payload = await verify(token, SECRET_KEY, ALGORITHM);
    return payload;
  }
  return;
};
```

在 `authenticate` 函数中，我们接收 `user` 和 `password` 作为参数。我们使用 `verifyPassword` 函数通过与哈希后的密码对比来验证密码。如果密码有效，我们将使用 `SECRET_KEY` 和 `ALGORITHM` 创建一个带有 `userId` 负载的 JWT 令牌。

在 `setContextUser` 函数中，我们接收类型为 `RouterContext` 的 `ctx` 作为参数。然后我们将 `ctx` 传递给 `parseToken` 函数，该函数返回 `authorization` 头中的 `token`。解析出的令牌随后传递给 `verifyToken` 函数，该函数使用 `SECRET_KEY` 和 `ALGORITHM` 验证令牌并在成功后返回 `payload`。该负载将供所有的解析器用于识别请求的用户。我们需要使用以下命令安装 `djwt` 模块：

```bash
trex i -m djwt@2.2
```

现在，将在 `middlewares.ts` 文件中将 `setContextUser` 作为 GraphQL 中间件的上下文处理器如下：

```typescript
// src/middlewares.ts
import { Router } from "oak";
import { applyGraphQL } from "oak_graphql";
import { types } from "./schema.ts";
import { resolvers } from "./resolvers.ts";
import { setContextUser } from "./auth.ts";

export const GraphQLService = await applyGraphQL<Router>({
  Router,
  typeDefs: types,
  resolvers: resolvers,
  context: setContextUser,
});
```




最后，我们将在应用中添加 `oakcors` 中间件以启用`跨源资源共享 (CORS)`，允许其他域名访问此服务器上的资源。我们还将使用 `PORT` 环境变量来设置服务器端口。修改后，我们的 `mod.ts` 文件将包含代码：

```typescript
import { Application } from "oak";
import { GraphQLService } from "./middlewares.ts";
import { oakCors } from "cors";

const app = new Application();
const _PORT = Deno.env.get("PORT");
const PORT = parseInt(_PORT as string);
const port = isNaN(PORT) ? 8080 : PORT;
app.use(
  oakCors()
);
app.use(GraphQLService.routes(), GraphQLService.allowedMethods());
console.log(`GraphQL Server listening on ${port}/graphql`);
await app.listen({ port });
```

我们将使用以下命令安装 `cors` 模块：

```bash
trex i -m cors@v1.2.2
```

### 总结

在本章中，我们使用了多种 Deno 模块（如 `oak-graphql`、`djwt`、`scrypt` 和 `cors`）实现了一个 GraphQL API。Oak-GraphQL 配合 Oak 框架创建 GraphQL API 服务器非常有用。Djwt 用于创建和验证 JSON Web Tokens。Scrypt 用于密码哈希处理。CORS 用于允许通过不同域名访问服务器。我们学习了如何使用 `velociraptor` 配置设置（环境变量、脚本和权限）。我们使用了 `trex` 模块来安装 Deno 模块并将它们添加到 `import_map.json` 文件中。

这些知识对于建立一个新的 Deno 项目将非常有帮助。目前，我们可以在播放器（playground）中测试实现结果。我们将在接下来的章节中使用 `Snel` 模块创建一个 Svelte 前端，并集成 GraphQL API。

# 第 9 章

## 通讯录应用 - UI 实现

### 引言

在上一章中，我们为电话通讯录应用实现了 GraphQL API 服务器。应用程序的用户界面（UI）将在本章中通过该 API 进行实现。我们将使用 `snel` 模块在 deno 中创建 `svelte` 应用，并配合 `snel-carbon` 模块，该模块提供了基于 IBM Carbon 设计系统的 carbon 组件和图标。我们还将使用 `axiod` 模块向服务器发送网络请求。

### 结构

在本章中，我们将涵盖以下主题：

* 初始设置
    * Snel 设置
    * Snel-carbon 安装
* 路由
    * 公共路由
        * 登录
        * 注册
    * 私有路由
        * 首页
        * 联系人
            * 联系人表格
            * 联系表单
* 布局
    * 头部
    * 侧边栏

### 目标

完成本章后，你应该能够使用 `snel` 和 `snel-carbon` 模块创建 svelte UI 应用。之后你应该能够为 svelte 应用创建公共和私有路由。你还将学习使用 `axiod` 模块进行网络请求。

### 初始设置

在本节中，我们将安装 `snel` 并初始化一个 snel 项目，然后使用 `trex` 运行脚本。一旦创建了 snel 项目，我们将安装 `snel-carbon` 组件、图标模块以及用于网络请求的 `axiod` 模块。让我们从安装 snel 开始。

# Snel 设置

Snel 是“一个用于 deno 中 svelte 应用的控制论框架”，它将 Svelte 组件编译为 javascript 文件。我们将使用以下命令安装 snel：

```bash
deno run --allow-run --allow-read https://deno.land/x/snel/install.ts
```

上述命令将安装 `snel`、`trex`、`bundler` 模块以提供良好的开发者体验。命令成功执行后，我们将使用以下命令创建新的 snel 应用：

```bash
snel create [project name]
```

图 9.1 显示了使用默认设置创建新的 snel 项目。

![](img/Figure-9.1.jpg)

**图 9.1：** Snel 项目创建

项目完成后，我们可以使用多个命令在各种模式下运行项目，如 `development`、`watch`、`build` 等。

图 9.2 列出了运行 snel 项目的可用命令。

![](img/Figure-9.2.jpg)

**图 9.2：** 用于 Snel 项目的 Trex 命令

我们将通过运行 `trex start` 命令启动项目。这将在 `3000` 端口启动服务器。

图 9.3 显示在 3000 端口运行的示例项目。

![](img/Figure-9.3.jpg)

**图 9.3：** 在 3000 端口运行的 Snel 项目

# Snel Carbon 安装

Snel-Carbon 是一个为 svelte 提供 UI 的 deno 模块。它可以帮助我们基于设计系统构建 UI。让我们从在 `index.html` 文件中添加 css 开始。

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/carbon-components@0.4" />
```

Snel 提供 `snel.config.js` 文件来配置设置。我们将向项目中添加导入映射（import maps）。

```javascript
export default {
  port: 3000,
  mode: "dom",
  plugins: [],
  extendsMap: [
    "https://denkg.com/io/components.json",
    "https://denkg.com/io/icons.json",
  ],
};
```

现在我们使用 `trex` 命令安装 `axiod` 模块：

```bash
trex i -m axiod@0
```

上述命令将 `axiod` 添加到 `import_map.json` 文件中。

### 路由

Snel 包含了 Svelte Routing 来创建路由。我们将使用它创建名为公共和私有的两种路由。公共路由对所有用户可用，而私有路由对已验证的用户可用。让我们先在 `App.svelte` 文件中从 `routes/svelte` 添加 `Route` 组件：

```svelte
<script>
  import Routes from "./routes.svelte";
  import { fade } from "svelte/transition";
</script>

<main transition:fade>
  <Routes />
</main>

<style>
  main {
    max-width: 240px;
  }
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
```

在前面的代码中，我们用 `Route` 组件替换了 main 元素（代表主体主体内容的 HTML 元素）中的代码。这样我们的应用程序就会根据路由地址渲染每个页面。让我们在 `routes/index.svelte` 文件中实现路由：

```svelte
<script>
  // 
  import Router from "svelte-routing/Router";
  import Route from "svelte-routing/Route";

  // 路由
  import Contacts from "./Contacts.svelte";
  import Login from "./Login.svelte";
  import Register from "./Register.svelte";
  import Home from "./Home.svelte";
  import NotFound from "./NotFound.svelte";
  import PrivateRoute from "./PrivateRoute.svelte";
</script>

<Router>
  <Route path="/login" component={Login} />
  <Route path="/register" component={Register} />
  <PrivateRoute path="/home" component={Home} />
  <PrivateRoute path="/contacts" component={Contacts} />
  <Route path="/" component={Home} />
  <Route path="*" component={NotFound} />
</Router>
```




```svelte
import Column from "snel-carbon/components/Grid/Column.svelte";

// Components
import Layout from "@/components/Layout.svelte";
</script>

<Router>
  <Layout />
  <Content>
    <Grid>
      <Row>
        <Column>
          <Route path="login" component={Login} />
          <Route path="register" component={Register} />
          <Route path="*" component={NotFound} />
          <PrivateRoute path="/">
            <Home />
          </PrivateRoute>
          <PrivateRoute path="contacts" let:location>
            <Contacts />
          </PrivateRoute>
        </Column>
      </Row>
    </Grid>
  </Content>
</Router>
```

在前面的代码中，我们使用了来自 `svelte-routing` 模块的 `Router` 和 `Route` 组件。`Router` 通过上下文向 `Route`、`Link` 组件提供路由信息并渲染最匹配的 `Route`。

在 `Routes` 导入部分，我们导入了 `Contacts`、`Login`、`Home` 和 `Register`。每个路由将被分配一个路径。除了这些路由外，我们还导入了两个名为 `NotFound` 和 `PrivateRoute` 的特殊路由。当没有匹配其他路由时，渲染 `NotFound`。`PrivateRoute` 用于限制只有已身份的用户才能访问如 `Contacts` 等路由。

我们从 `snel-carbon` 模块导入了 Carbon 组件，如 `Content`、`Row`、`Grid`、`Column`，创建一个响应式 UI，并配合带有头部和侧边栏实现的自定义组件 `Layout`。

让我们逐个实现每个路由的代码。

### Login

登录将是显示给每个未验证用户的默认页面。我们将使用 `Form` 来处理 `email` 和 `password` 的验证。`Login.svelte` 的实现如下：

```svelte
// Login.svelte
<script>
  import { navigate } from "svelte-routing";
  import Form from "snel-carbon/components/Form";
  import Tile from "snel-carbon/components/Tile";
  import TextInput from "snel-carbon/components/TextInput/TextInput.svelte";
  import PasswordInput from "snel-carbon/components/TextInput/PasswordInput.svelte";
  import Button from "snel-carbon/components/Button";
  import InlineLoading from "snel-carbon/components/InlineLoading";
  import InlineNotification from "snel-carbon/components/Notification/InlineNotification.svelte";
  import axiod from "https://deno.land/x/axiod/mod.ts";
  import { accessToken } from "../utils/stores.ts";
  let email = "";
  let password = "";
  let loading = false;
  let errors = [];
  const handleSubmit = (e) => {
    loading = true;
    const query = `
    {
      login(email:"${email}", password:"${password}"){
        token
      }
    }`;
    axiod
      .post("http://localhost:8080/graphql", { query })
      .then((res) => {
        if (res.data.errors) {
          errors = res.data.errors;
        }
        if (res.data.data?.token) {
          localStorage.setItem("accessToken", res.data.data?.token);
          $accessToken = res.data.data?.token;
          navigate("/contacts", {
            replace: false,
          });
        }
      })
      .catch((err) => {
        console.log(`err`, err);
      })
      .finally(() => {
        loading = false;
      });
  };
</script>
{#each errors as error (error.message)}
  <InlineNotification timeout={5000} type="error" title={error.message} />
{/each}
<Tile>
  <Form on:submit={handleSubmit}>
    <TextInput
      bind:value={email}
      required
      type="email"
      labelText="Email"
      placeholder="Enter Email"
      size="sm"
    />
    <PasswordInput
      bind:value={password}
      required
      type="password"
      labelText="Password"
      placeholder="Enter Password"
      size="sm"
    />
    {#if loading}
      <InlineLoading />
    {:else}
      <Button type="submit" size="small">Login</Button>
    {/if}
  </Form>
</Tile>
```

在上面的代码中，我们使用了 `snel-carbon` 组件，如 `Form`、`Tile`、`TextInput`、`PasswordInput`、`InlineLoading` 和 `InlineNotification`。我们使用 `navigate` 函数跳转到 `contacts` 路由。我们使用了 `email`、`password`、`loading` 和 `errors` 状态。响应包含 `errors` 和 `token`。

### Register

此路由与 `Login` 路由相似，有少数变化。`Register.svelte` 的实现如下：

```svelte
<script>
  import { navigate } from "svelte-routing";
  import Form from "snel-carbon/components/Form";
  import Tile from "snel-carbon/components/Tile";
  import TextInput from "snel-carbon/components/TextInput/TextInput.svelte";
  import PasswordInput from "snel-carbon/components/TextInput/PasswordInput.svelte";
  import Button from "snel-carbon/components/Button";
  import InlineNotification from "snel-carbon/components/Notification/InlineNotification.svelte";
  import InlineLoading from "snel-carbon/components/InlineLoading";
  import axiod from "https://deno.land/x/axiod/mod.ts";
  let name = "";
  let email = "";
  let password = "";
  let confirmPassword = "";
  let loading = false;
  let errors = [];
  const handleSubmit = (e) => {
    if (password === confirmPassword) {
      loading = true;
      const query = `
    mutation{
      registerUser(email:"${email}", password:"${password}", name:"${name}"){
        name
      }
    }`;
      axiod
        .post("http://localhost:8080/graphql", { query })
        .then((res) => {
          if (res.data.errors) {
            errors = res.data.errors;
```





```javascript
errors = res.data.errors;
}
if (res.data.data.registerUser?.name) {
  alert(`user ${res.data.data.registerUser.name} registered`);
  navigate("/contacts", {
    replace: false,
    state: { accessToken: res.data.data.login },
  });
})
.catch((err) => {
  console.log(`err`, err);
});
} else {
  alert("Passwords do not match");
};
</script>
```

```html
{#each errors as error}
  <InlineNotification type="error" title={error.message} />
{/each}
```

<Tile>
  <Form on:submit={handleSubmit}>
    <TextInput
      bind:value={name}
      required
      labelText="Name"
      placeholder="Enter Name"
      size="sm"
    />
    <TextInput
      bind:value={email}
      required
      type="email"
      labelText="Email"
      placeholder="Enter Email"
      size="sm"
    />
    <PasswordInput
      bind:value={password}
      required
      type="password"
      labelText="Password"
      placeholder="Enter Password"
      size="sm"
    />
    <PasswordInput
      bind:value={confirmPassword}
      required
      type="password"
      labelText="Confirm Password"
      placeholder="Enter Confirm Password"
      size="sm"
    />
    {#if loading}
      <Loading />
    {:else}
      <Button type="submit" size="small">Register</Button>
    {/if}
  </Form>
</Tile>

正如我们看到的，上面的代码与 `Login.svelte` 有许多相似之处。我们添加了两个绑定到输入组件（`TextInput`、`PasswordInput`）的额外状态 `name` 和 `confirmPassword`。在 `handleSubmit` 函数中，我们使用了 `mutation` 而不是 `query`，因为我们正在后端创建一个新用户。图 9.5 显示了带有姓名、邮箱、密码字段的注册路由。

### Home (首页)
这将是身份验证用户的首页。它将包含一个导航到 `contacts` 路径的 `Link` 组件。该路由的代码如下：

```javascript
import Link from "svelte-routing";
<h1>Home</h1>
<Link to="contacts">Contacts</Link>
```
图 9.6 显示了带有用于 `Contacts` 路由的 `Link` 组件的首页路由。

### NotFound (未找到)
每当用户打开不存在的路径地址时，此路由将被渲染。我们为此目的使用了星号（`*`）。该路由的代码如下：

```javascript
import Link from "svelte-routing";
<h2>Page Found</h2>
Go back to <Link="/">Home</Link>
<style>
  h2 {
    color: red;
  }
</style>
```
上面的代码是一个简单的页面，带有 `Page Found` 消息和指向主页页的 `Link`。图 9.7 显示了为未定义路径渲染的 `NotFound` 组件。

### Private route (私有路由)
虽然 Login 和 Register 是公共路由（不需要身份验证），但 Home 和 Contacts 是私有路由，应该仅供身份验证用户访问。我们将通过使用 `PrivateRoute`（一个自定义路由）而不是普通的 `Route` 来保护这些页面。私有路由的代码如下：

```javascript
import Route from "svelte-routing/Route";
import PrivateRouteGuard from "./PrivateRouteGuard.svelte";
export let path;
<Route {path}>
  <PrivateRouteGuard>
    <slot />
  </PrivateRouteGuard>
</Route>
```
在上面的代码中，我们使用 `Route` 组件作为包装器。我们向它传递 `path` 属性，这是一个路由地址。`slot` 元素就是将被渲染的组件。我们使用 `PrivateRouteGuard` 组件将其封装起来。`PrivateRouteGuard` 的代码如下：

```javascript
import { onMount } from "svelte";
import { navigate } from "svelte-routing";
import { accessToken } from "../utils/stores.ts";

onMount(() => {
  console.log("Mounting...");
  if (!$accessToken) {
    navigate("/login", {
      replace: false,
    });
  }
});
{#if $accessToken}
  <slot />
{/if}
```

`PrivateRouteGuard` 使用在挂载时调用的 `onMount` 函数。它检查 `accessToken` 的值。如果 `accessToken` 为 `null`，它将跳转到 `login` 路由，否则将渲染子组件。此路由所有用户可用，并列出用户所有的联系人。联系人的代码如下：

```javascript
import { onMount } from "svelte";
import Modal from "svelte-carbon/Modal";
import axios from "https://deno.land/x/axios/mod.ts";
import ContactForm from "../components/ContactForm.svelte";
import ContactTable from "../components/ContactTable.svelte";
let showForm = false;
let contacts = [];
const accessToken = localStorage.getItem("accessToken");
let editContact = null;
const getContacts = () => {
  console.log("fetching contacts...");
  const query = `
    contacts {
      contactId
      name
      email
      phone
      address
    }
  `;
  axios
    .post("http://localhost:8080/graphql",
      query,
      {
        headers: { Authorization: `Bearer ${accessToken}` },
      }
    )
    .then((res) => {
      console.log(`res`, res);
      if (res.data.errors) {
        for (let error of res.data.errors) {
          alert(error.message);
        }
      } else {
        // console.log(`res.data.data.login`, res.data.data.login);
        if (res.data.data?.contacts) {
          contacts = res.data.data.contacts;
        }
      }
    })
    .catch((err) => {
      console.log(`err`, err);
    });
  console.log("fetched");
};
const deleteContact = (contactId) => {
  const query = `
    mutation {
      deleteContact(contactId:"${contactId}")
    }
  `;
  axios
    .post("http://localhost:8080/graphql",
      query,
      {
        headers: { Authorization: `Bearer ${accessToken}` },
      }
    )
    .then((res) => {
      console.log(`res`, res);
      if (res.data.errors) {
        for (let error of res.data.errors) {
          alert(error.message);
        }
      } else {
        getContacts();
      }
    });
};
```





```javascript
      })
    .catch((err) => {
        console.log(`err`, err);
    });
  };
  onMount(async () => {
    console.log("Mounting…”);
    await getContacts();
  });
  const resetForm = () => {
    showForm = !showForm;
    editContact = null;
  };
  const handleEdit = (event) => {
    showForm = true;
    editContact = event.detail.contact;
  };
</script>
{#if showForm}
  <Modal
    bind:open={showForm}
    preventCloseOnClickOutside
    modalHeading={`${editContact ? “编辑” : “添加”} 联系人`}
  >
    <ContactForm
      on:resetForm={resetForm}
      on:contactSaved={(event) => {
        console.log(`event`, event);
        showForm = event.detail.showForm;
        getContacts();
        editContact = event.detail.editContact;
      }}
      {editContact}
    />
  </Modal>
{/if}
<ContactTable
  {contacts}
  on:deleteContact={(event) => deleteContact(event.detail.contactId)}
  on:edit={handleEdit}
  on:openForm={resetForm}
/>
```

上述代码渲染了两个组件，分别是 `ContactForm` 和 `ContactTable`。来自 `snel-carbon` 的 `Modal` 组件用于在模态视图中显示 `ContactForm`。它定义了三个状态：`showContact`、`contacts` 和 `editContact`。`showContact` 是一个布尔标记，用于显示或隐藏 `ContactForm` 模态框。`contacts` 是联系人数组。这些联系人是通过 `getContacts` 函数获取的，该函数使用 `axios` 向 GraphQL API 服务器发送网络请求。它会在组件挂载时通过 `onMount` 函数被调用一次。我们还定义了 `deleteContact` 函数，向服务器发送删除联系人的请求。为了用户身份验证，我们为每个请求都设置了带有 `accessToken` 的 `Authorization` 头部。`resetForm` 函数用于在表单关闭或提交时重置表单字段。`handleEdit` 函数用于将选定的实体设置为 `editContact`。随后，`editContact` 数据将传递给表单进行编辑。让我们详细检查 `ContactForm` 和 `ContactTable` 组件。

## ContactTable

我们将在 `ContactTable.svelte` 文件中使用 `snel-carbon` 组件以表格格式显示所有联系人。我们还将在表格中提供了“创建”、“删除”和“编辑”操作。该组件的代码如下：

```svelte
<script>
  import { createEventDispatcher } from "svelte";
  import DataTable from "snel-carbon/components/DataTable";
  import Toolbar from "snel-carbon/components/DataTable/svelte";
  import ToolbarContent from "snel-carbon/components/DataTable/ToolbarContent.svelte";
  import OverflowMenu from "snel-carbon/components/OverflowMenu.svelte";
  import OverflowMenuItem from "snel-carbon/components/OverflowMenu/OverflowMenuItem.svelte";
  import Button from "snel-carbon/components/Button";
  import Add16 from "snel-carbon/icons/Add16";
  import Edit16 from "snel-carbon/icons/Edit16";
  import Delete16 from "snel-carbon/icons/Delete16";
  const dispatch = createEventDispatcher();
  export let contacts;
  $: {
    contacts = contacts.map((contact, index) => {
      contact.id = index + 1;
      return contact;
    });
  }
</script>
<DataTable
  title="联系人"
  sortable
  headers={[
    { key: "id", value: "ID" },
    { key: "name", value: "姓名" },
    { key: "email", value: "邮箱" },
    { key: "phone", value: "电话" },
    { key: "address", value: "地址" },
    { key: "overflow", empty: true },
  ]}
  rows={contacts}
>
  <Toolbar>
    <ToolbarContent>
      <Button
        on:click={() => {
          dispatch("openForm");
        }}
        icon={Add16}
      />
    </ToolbarContent>
  </Toolbar>
  <span slot="cell" let:cell let:row>
    {#if cell.key === "overflow"}
      <OverflowMenu flipped>
        <OverflowMenuItem
          on:click={() => {
            dispatch("edit", { contact: row });
          }}
        ><Edit16 />
        </OverflowMenuItem>
        <OverflowMenuItem
          danger
          on:click={() => {
            dispatch("deleteContact", { contactId: row.contactId });
          }}
        >
      </OverflowMenu>
    {/if}
  </span>
</DataTable>
```

在前面的代码中，我们从 `snel-carbon` 导入了各种组件，如 `DataTable`、`Toolbar` 和 `Button`。我们还从 `snel-carbon` 导入了 `Add16`、`Edit16` 和 `Delete16` 等图标。我们使用了 `svelte` 的 `createEventDispatcher` 来向父组件发送事件。`contacts` 作为 prop 传递。我们使用 `$:` 语法进行响应式声明，这意味着当 `contacts` 变化时，我们会遍历它们并分配一个 `id`。

`DataTable` 组件每列都需要一个 `id` 字段。我们传递了带有键和值的 `headers`。`contacts` 被传递为 `rows`。在 `DataTable` 中，我们使用了带有 `ToolbarContent` 的 `Toolbar` 以及一个允许添加新联系人的 `Button`。我们使用 `slot="cell"` 来识别溢出单元格并渲染 `OverflowMenu` 或普通值。在 `OverflowMenu` 内部，我们通过分带数据的 `edit` 或 `deleteContact` 事件来处理点击操作。父组件将相应地处理这些事件。




```svelte
import { accessToken } from "../utils/stores.ts";
import { createEventDispatcher } from "svelte";

const initialContact = {
  name: "",
  email: "",
  phone: "",
  address: "",
};

const dispatch = createEventDispatcher();
export let editContact;
$: contact = editContact || initialContact;
let loading = false;
const handleSubmit = () => {
  loading = true;
  const addQuery = `
    mutation {
      addContact(contact: {name: "${contact.name}", email: "${contact.email}", phone: "${contact.phone}", address: "${contact.address}"}){
        name
      }
    }
  `;
  const updateQuery = `
    mutation {
      updateContact(contact: {contactId: "${contact?.contactId}", name: "${contact.name}", email: "${contact.email}", phone: "${contact.phone}", address: "${contact.address}"})
    }
  `;
  const query = editContact ? updateQuery : addQuery;
  axiod
    .post(
      "http://localhost:8080/graphql",
      { query },
      {
        headers: { Authorization: `Bearer ${$accessToken}` },
      }
    )
    .then((res) => {
      console.log(`res`, res);
      if (res.data.errors) {
        for (let error of res.data.errors) {
          alert(error.message);
        }
      } else {
        contact = initialContact;
        dispatch("contactSaved", {
          showForm: false,
          editContact: null,
        });
      }
    })
    .catch((err) => {
      console.log(`err`, err);
    })
    .finally(() => {
      loading = false;
    });
};
</script>
<Tile>
  <Form on:submit={handleSubmit}>
    <TextInput bind:value={contact.name} required label="Name" placeholder="Enter Name" size="sm" />
    <TextInput bind:value={contact.email} required type="email" label="Email" placeholder="Enter Email" size="sm" />
    <TextInput bind:value={contact.phone} required type="number" label="Phone" placeholder="Enter Phone Number" size="sm" />
    <TextArea bind:value={contact.address} required label="Address" placeholder="Enter Address" size="sm" />
    {#if loading}
      <InlineLoading />
    {:else}
      <Button type="submit" size="small">Save</Button>
      <Button
        on:click={() => {
          dispatch("resetForm");
        }}
        size="small"
        kind="danger">Cancel</Button>
      >
    {/if}
  </Form>
</Tile>
```

在上面的代码中，我们从 `svelte-carbon` 导入了 `Tile`、`Form`、`TextInput`、`PasswordInput`,`Button` 组件。`Tile` 用于表单的卡片布局。`Form` 用于处理邮箱、数字等验证和提交。`TextInput` 是姓名、邮箱（`type="email"`）、电话（`type="number"`）的输入字段。`Button` 用于关闭表单并将字段值设为空，或使用 `type="submit"`。

![Figure 9.10](img/Figure-9.10.jpg)
**图 9.10:** 用于新联系人的 ContactForm

在 `script` 部分，我们使用 `initialContact` 对象在新建或表单单关闭时将所有字段设为空。`editContact` 属性用于识别新联系人应该使用 `initialContact`（空值），还是应该使用 `editContact`（现有表单值）。响应式变量 `contact` 被设置为 `editContact` 的值。`handleSubmit` 函数包含两个查询：`addQuery`（创建联系人）和 `updateQuery`（更新联系人）。同样使用 `editContact` 来选择查询。然后，我们带有 `Authorization` 头部对选定的查询发送网络请求。

![Figure 9.11](img/Figure-9.11.jpg)
**图 9.11:** 用于现有联系人的 ContactForm

### 布局

在本节中，我们将使用 `svelte-carbon` 的 `Header` 和 `Sidebar` 组件创建一个布局。这将允许我们在 `Header` 中提供应用标题，并在 `Sidebar` 中添加登录/注销按钮。我们将在 `Layout.svelte` 中编写如下布局相关代码：

```svelte
<script>
import Header from "svelte-carbon/components/UIShell/Header.svelte";
import SideNav from "svelte-carbon/components/UIShell/SideNav.svelte";
import SideNavItems from "svelte-carbon/components/UIShell/SideNavItems.svelte";
import Authentication from "./Authentication.svelte";
let theme = "g10";
$: document.documentElement.setAttribute("theme", theme);
let isNavOpen = false;
</script>
<Header
  company="Phonebook"
  platformName="App"
  bind:isNavOpen
  persistentHamburgerMenu={true}
/>
<SideNav bind:isOpen={isNavOpen}>
  <SideNavItems>
    <Authentication />
  </SideNavItems>
</SideNav>
```

在前面的代码中，我们从 `svelte-carbon` 导入了 `Header`、`SideNav` 和 `SideNavItems`。`Header` 将位于应用的顶部，而 `SideNav` 将用于侧边栏，其中 `SideNavItems` 包含 `login`、`register` 等操作。我们将主题设置为 `g10`，这是一种灰色主题。文档中还有其他可用主题。

### Header

我们为该组件提供了几个属性。`company` 属性用于为应用设置标题（Phonebook）。`platformName`（App）是副标题。我们使用状态 `isNavOpen` 来显示/隐藏侧边栏。`persistentHamburgerMenu` 属性用于显示打开/关闭侧边栏的汉堡按钮。

### SideNav

我们配合 `SideNavItems` 使用它显示 `Login`、`Register` 和 `Logout` 按钮。我们的逻辑将为未授权的用户显示 `Login` 和 `Register` 按钮，为已授权的用户显示 `Logout` 按钮。该逻辑写在 `Authentication.svelte` 文件中如下：

```svelte
<script>
import Button from "svelte-carbon/components/Button";
import ButtonSet from "svelte-carbon/components/Button/ButtonSet.svelte";
import Link from "svelte-routing/Link.svelte";
import { accessToken } from "../utils/stores.ts";
import Login16 from "svelte-carbon/icons/Login16";
import Logout16 from "svelte-carbon/icons/Logout16";
</script>
<div class="auth-container">
  <ButtonSet stacked>
    {#if !$accessToken}
      <Link to="/login">
        <Button kind="ghost" icon={Login16}>Login</Button>
      </Link>
      <Link to="/register">
        <Button kind="ghost">Register</Button>
      </Link>
    {:else}
      <Link to="/">
```




```html
<Button
  kind="ghost"
  icon={Logout16}
  on:click={() => {
    localStorage.removeItem("accessToken");
    $accessToken = "";
  }}
>
  退出
</Button>
</Link>
{/if}
</ButtonSet>
</div
```

<style>
  .auth-container {
    margin: 10px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
</style>
```

在前面的代码中，我们使用了 carbon 组件 `Button`、`ButtonSet`，以及 carbon 图标 `Login16`、`Logout16`。我们还从 svelte-routing 导入了 `Link` 组件，并从 store 中导入了 `accessToken`。`Link` 组件用于设置登录、注册等 URL 地址。我们使用 `accessToken` 来显示登录、注册按钮或注销按钮。如果 `accessToken` 有效，则我们将显示注销按钮，否则显示登录和注册按钮。

`ButtonSet` 用于显示一组按钮（登录、注册）。我们向每个 Button 组件传递了几个属性。`kind` 定义了按钮类型（此处为 ghost）。`icon` 属性用于在按钮中显示图标。我们分别使用了 snel-carbon 中的 `Login16` 和 `Logout16` 图标用于登录和注销按钮。

### 结论

在本章中，我们使用各种 deno 模块（如 `snel`、`snel-carbon`、`axiod` 等）实现了一个 svelte 应用 UI。Snel 模块适用于使用 deno 运行时创建 Svelte 应用程序。`Snel-carbon` 提供了基于 carbon 设计系统的组件和图标。我们使用这些组件和图标创建了我们的 UI。`Axiod` 用于向服务器发送网络请求。`Svelte Routing` 模块用于为应用定义各种路由（公共和私有）。我们默认使用 snel 提供的 `trex` 来运行脚本。

这些知识将有助于为 Svelte UI 应用设置新的 deno 项目。我们可以通过与上一章中的 API 服务器一并运行来测试实现结果。至此，我们的*电话簿*应用就完成了，可以在本地使用，也可以通过各种平台部署到云端。

### 索引

### A
- Aleph.js [66]
- 应用程序接口 (API) [71], [72]
- 命令行接口 (CLI) [67]
- 特性 [66], [67]
- 页面 [68], [69]
- 路由 [69]-[71]
- 参数 [47], [48]

### B
- 基础类型, TypeScript [14]
- 抽象 [29]
- 类 [22]
- Getter 和 Setter [26]
- 接口 [15], [16]
- 接口与类型别名 [18]
- 交集 [21]
- 修饰符 [22]
- 可选属性 [16]
- 只读属性 [16]
- 静态 [28]
- 类型别名 [17]
- 类型断言 [20]
- 类型推断 [19]
- 联合类型 [20]
- 打包命令 [46]

### C
- 缓存命令 [46]
- 类 [22]
- 实体 [22]
- 类 [55], [56]
- 命令行接口 (CLI) [44]
- 编译命令 [47]
- 编译器 [8]
- 补 [47]
- ContactForm [69], [73], [174]
- 带有工具栏的 ContactTable [168]
- 跨域共享 (CORS) [141]

### D
- 数据库 [39]
- MongoDB Atlas [39]
- PostgreSQL [39]
- TypeScript 中的数据类型 [15]
- 数组 [15]
- Boolean [14]
- 枚举 [15]
- never [15]
- null [15]
- number [14]
- 对象 [15]
- string [14]
- 元组 [15]
- undefined [15]
- unknown [15]
- void [15]
- Deno [1], [2]
- 特性 [2]-[5]
- 安装 [34], [35]
- 对比 Node [4]
- Deno CLI [45]
- 环境变量 [45]
- 文件监听器 [49]
- 传递参数 [47], [48]
- 权限标记 [49]
- 权限白列表 [50], [51]
- DENO_DIR [45]
- Deno 生态系统 [43]
- Deno 基础栈 [6]
- Rust [6], [7]
- tokio I/O 库 [7]
- Google 的 V8 引擎 [6]
- Deno 全局 API [52]-[54]
- DENO_INSTALL_ROOT [45]
- Deno 模块 [56]
- 注册表 [61]
- 标准库 [56]-[58]
- 第三方模块 [58]-[61]
- Deno 运行时 APIs [51]
- 类 [55], [56]
- Deno 全局 API [52]-[54]
- 变量 [54], [55]
- Web APIs [51], [52]
- deps.ts [62]
- 开发工具 [35]
- 数据库 [39]
- Docker [39]
- Docker Compose [38]
- Git [37]
- GitHub [37]
- Postman [40]
- Redis [38]
- 搜索器 [38]
- 终端 [35], [37]
- VS Code [37]
- VS Code 插件 [37]
- zsh + zsh [36]
- doc 命令 [46]
- Docker [38]
- Docker Compose [38]
- 动态 API [72]
- 动态路由 [69]
- 动态类型对比静态类型 [30]

### E
- Electron.js [3]
- 环境变量 [45]
- eval 命令 [46]
- 事件循环 [4]
- 显式类型 [19]

### F
- 文件监听 [49]
- 先先出 (FIFO) 原则 [10]
- fmt 命令 [46]

### G
- Git [37]
- GitHub [37]
- GraphQL [100]
- 自动生成的 API 文档 [104], [105]
- 核心概念 [105]
- 特性 [100]
- 片段 [103], [104]
- 精确获取 [101]
- Schema [105], [106]
- 单 API 端点 [101], [102]
- 验证与类型检查 [102]

### H
- help 命令 [45]
- Heroku [40]
- 热模块替换 (HMR) [66]
- 水合过程 [69]

### I
- 隐式类型 [19]
- 安装命令 [46]
- 解释器 [8]

### J
- JavaScript 引擎 [7]





## C
- `编译器` 8
- `解释器` 8
- `JavaScript 运行时` 9
- `回调` 9
- `回调队列` 10
- `Deno API` 9
- `事件循环` 10
- `内存堆` 9
- `引用链接` 4
- `tokio` 9
- `JSON Web Token (JWT)` 137

## L
- 后进先出 (LIFO) 原则 9
- 布局, `PhoneBook App` 174, 175
- `header` 175
- `SideNav` 175, 177
- `libuv 事件循环` 3, 4

## M
- `修饰符` 22
- `private` 23
- `protected` 24
- `public` 22
- `模块注册表` 61, 62
- `MongoDB` 39
- `URL` 39
- `MongoDB Atlas` 39
- `URL` 39
- `变异` 100

## N
- `嵌套路由` 71
- `Node` 3
- `异步和事件驱动架构` 3
- `node 包管理器 (npm)` 4
- `性能` 4
- 对比, `Deno` 4

## O
- `Oak` 111
- `Oak-GraphQL 中间件` 112-114
- `Oak GraphQL 服务器设置` 118-121
- `对象-关系映射 (ORM)` 116
- `开源` 3, 4
- `OverflowMenu` 168

## P
- `页面`, `Aleph.js` 68, 69
- `权限标志位` 49
- `权限允许名单` 50
- `持久化汉堡菜单属性` 175
- `PhoneBook App, API 实现` 115
- `身份验证` 137-141
- `控制器` 134-137
- `数据库设置` 130, 131
- `初始设置` 116
- `模型` 131-134
- `Schema` 121-123
- `Trex`, 作为包管理器 117
- `velociraptor`, 作为脚本运行器 117, 118
- `版本控制, 使用 git` 116
- `PhoneBook App, UI 实现` 143
- `初始设置` 144
- `布局` 174, 175
- `路由` 147-149
- `Snel Carbon` 146, 147
- `snel 设置` 144-146
- `平台即服务 (PAAS)` 40
- `Pomodoro` 41
- `PostgreSQL` 39
- `Postman` 38
- `预渲染` 69
- `Profiler` 8

## Q
- `查询` 100

## R
- `React.js` 3
- `React Native` 3
- `关系数据库系统 (RDBMS)` 39
- `远程字典 (Redis)` 40
- `关系性状态传输 (REST) API` 66
- `resolver` 108-111
- `Route 组件` 147
- `路由` 147-149
- `ContactForm` 169-174
- `contacts` 160-165
- `ContactTable` 165-168
- `首页` 157, 158
- `登录` 150-153
- `NotFound` 158, 159
- `private` 159, 160
- `注册` 153-157
- `路由机制` 69
- `运行命令` 46
- `Rust` 6, 7

## S
- `模式定义语言 (SDL)` 105
- `Schema, PhoneBook App` 121, 123
- `contact type` 124
- `CreateContact 输入` 125
- `login type` 124
- `LoginUser 输入` 124
- `Mutation type` 125
- `Query type` 125
- `RegisterUser 输入` 124
- `resolvers` 125, 129, 130
- `UpdateContact 输入` 125
- `UpdateUser` 124
- `user type` 123
- `Schema, Todos App` 105, 106
- `inputs` 107
- `mutation` 108
- `query` 107, 108
- `relationship` 108
- `resolver` 111
- `type`
- `SideNav Items` 175
- `Silver Search` 38
- `Snel Carbon` 146
- `static` 30
- `styled` 90
- `bundle` 45
- `cache` 46
- `compile` 47
- `completions` 47
- `doc` 46
- `eval` 46
- `fmt` 46
- `help` 45
- `install` 46
- `run` 46
- `test` 46
- `subscriptions` 100
- `Svelte routing` 147

## T
- `tokio/O library` 7
- `tsconfig.json` 32
- `TypeScript` 11, 12
- `basic types` 14
- `benefits` 13
- `features` 13
- `setup` 31
- `static`, versus dynamic typing 30
- `strong`, versus weak typing 31
- `tsconfig.json` 32
- `type system` 102

## U
- `UI implementation`
- `Todos App` 87
- `PhoneBook App` 143

## V
- `V8 engine, by Google` 6
- `V8 JavaScript engine` 8
- `variables` 54, 55
- `Vim` 36, 37
- `VS Code` 37
- `extensions` 37

## W
- `Web APIs` 51, 52

## Z
- `zsh + oh my zsh` 36

