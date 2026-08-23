# Adobe Integrated Runtime (AIR) JavaScript 开发者便携指南 (Adobe 开发者库)

# 面向 JavaScript 开发者的 Adobe® 集成运行时 (AIR) 口袋指南

本书由 Adobe 集成运行时 (AIR) 产品团队成员撰写，是 Adobe 全新跨平台桌面运行时（其之前的代号为 `Apollo`）Beta 版本的官方指南。

本书解释了如何使用 AIR 构建并部署基于 HTML 和 JavaScript 的 Web 应用程序到桌面环境，同时运用你已经熟悉的各类工具与技术。本书提供了理解 AIR 以及立即开始进行桌面应用开发所需的一切内容。

主题包括：

- AIR 是什么，以及该运行时旨在解决的问题
- 如何设置你的开发环境
- 如何使用 HTML 和 JavaScript 创建你的第一个应用
- AIR 中的 HTML 和 JavaScript 环境
- 如何执行常见任务，以易于使用的 O'Reilly "Cookbook" 格式呈现

本书还包括一份 AIR 包、类和命令行工具的指南。一旦你理解了构建基于 HTML 和 JavaScript 的 AIR 应用程序的基础知识，这本口袋指南将成为解决具体问题的理想参考手册。欢迎来到革命之中！

Mike Chambers 是 AIR 开发者关系的高级产品经理，过去 8 年一直致力于开发针对 Flash 运行时的应用程序。Daniel Dura 和 Kevin Hoyt 都是 Adobe 平台布道师，专注于 AIR 和 Flash。

adobedeveloperlibrary.com

# 面向 JavaScript 开发者的 Adobe® 集成运行时 (AIR) 口袋参考手册

口袋参考

# 面向 JavaScript 开发者的 Adobe® 集成运行时 (AIR)

# 口袋参考

Mike Chambers, Daniel Dura, and Kevin Hoyt

# O'REILLY®

北京 · 剑桥 · 法纳姆 · 科隆 · 巴黎 · 塞瓦斯托波尔 · 台北 · 东京

# 面向 JavaScript 开发者的 Adobe® 集成运行时 (AIR) 口袋指南

作者：Mike Chambers, Daniel Dura, and Kevin Hoyt

# 前言

本书提供了对 Adobe 集成运行时 (AIR) 公开 Beta 1 版本应用开发的快速入门介绍。AIR 在 Beta 版之前以其代号 `Apollo` 被人所知，是 Adobe 正在开发的一个新的跨平台桌面应用程序运行时。虽然 Adobe AIR  允许基于 Flash 和 HTML 的应用开发，但本书专注于使用 HTML 和 JavaScript 构建 AIR 应用程序。

本书概述了 Adobe AIR，展示了如何设置你的开发环境，并讨论了新的 AIR 功能和 API。读完本书后，你应该对 AIR 是什么以及如何为其构建 HTML 和 JavaScript 应用程序有一个很好的理解。

## AIR 运行时命名约定

Adobe AIR 允许开发人员利用众多 Web 技术将 Web 应用程序部署到桌面。实际上，技术如此之多，以至于很难全部记住。表 P-1 列出了本书中使用的术语，并对每个术语进行了定义：

## 表 P-1. AIR 运行时命名约定

| 名称 | 含义 |
| --- | --- |
| Adobe 集成运行时 (AIR) | 支持运行 AIR 应用程序的跨平台桌面运行时。 |
| AIR 应用程序 | 在 Adobe AIR 之上运行的，使用 Flash、HTML 和/或 PDF 构建的应用程序。 |
| Flash | 包含在 `SWF 9` 文件格式中，可在 Flash Player 或 AIR 中运行的任何内容。 |
| ActionScript | 用于编程 Flash 内容的基于 ECMAScript 的编程语言。除非另有说明，本书所有对 ActionScript 的引用均指 ActionScript 3。 |
| HTML | 用于创建和布局网页的标准基于 Web 的标记语言。 |
| JavaScript | 用于编程 HTML 应用程序中内容的基于 Web 的 ECMAScript 实现。 |
| PDF | 便携式文档格式的缩写，一种允许电子文档无缝分发和显示的技术。 |
| Flex 框架 | 一个基于 XML 和 ActionScript 的框架，旨在使开发基于 Flash 的富 Internet 应用程序变得简单。 |
| Flex Builder | 一个基于 Eclipse 的 IDE，用于使用 Flex 和 ActionScript 构建基于 Flash 的富 Internet 应用程序。 |

## 本书涵盖内容

本书概述了 Adobe AIR，展示了如何设置你的开发环境以开始构建应用程序，概述了 AIR 中的 HTML 和 JavaScript 引擎，并展示了如何在 AIR 中执行许多常见的编程任务。

一般来说，Beta 构建版本中已有的功能和特性相对稳定，不应发生根本性变化（尽管可能会根据开发人员的反馈进行微调）。围绕未实现功能和特性的任何讨论细节则更具不确定性，并可能在未来的构建版本中发生变化。

同样需要注意的是，AIR 的 Beta 1 版本并未包含全部功能，许多重要的 AIR 功能尚未被实现，和/或未包含在此构建版本中。

以下是 Adobe AIR Beta 1 中包含的部分功能列表：

- Mac 支持（OS X 10.4.8 及以上版本；Intel 和 PPC 架构）
- Windows 支持（Windows XP 和 Windows Vista Home Ultimate 版）
- 文件 I/O API
- SQLite 嵌入式数据库
- Flash Player 9 的全部功能，包括完整的网络协议栈
- 窗口 API
- 命令行工具（ADL` 和 `ADT`）
- 在 Flash 内容中嵌入 HTML
- 顶级 HTML 应用程序
- ActionScript/JavaScript 脚本桥接
- Flex Builder 和 Flex 框架对 AIR 应用程序创作的支持
- 命令行参数
- 拖放支持
- 剪贴板访问
- 原生菜单（Beta 版中仅限 Mac）
- 服务连接
- 文件关联
- PDF 支持

以下是 Adobe AIR Beta 1 中包含的但未包含在 1.0 中的功能列表：

- 右键单击和上下文控制
- 在 HTML 应用程序中嵌入 Flash 内容
- Windows 支持

我们将介绍已知在未来构建版本中可能会更改。

## Beta 版本意味着什么

如前节所述，Adobe AIR Beta 1 版本功能尚完整，其中某些功能仅部分实现。因此，特定功能的实现或可用性在 Beta 版本和 1.0 版本之间可能会变化。这也适用于本书中的信息。如果某些功能未能像本书那样正常工作，请务必查阅在线文档，您可以在以下地址找到最新信息：

```
http://www.adobe.com/go/air
```

## 本书的目标读者

我们希望这本书适合你，为了确保无失，让我们讨论一下我们所假设，以及本书针对哪些。

### 本书基于哪些假设

本书假设读者至少熟悉 Web 技术，例如 HTML、JavaScript 和 CSS。

### 本书适合谁

本书适用于兴趣利用 HTML 和 JavaScript 构建和部署应用程序的开发者。如果你没有任何 HTML 或 JavaScript 经验，我们建议你花时间熟悉这些技术。虽然可以使用 AIR Beta 1 版本创建基于 Flash 的应用程序，但本书不会详细介绍。

## 本书的结构

本书包含以下章节和附录：

- 第 1 章，`Adobe 集成运行时 (AIR) 简介`：提供了 AIR 是什么以及它针对什么样的概述。
- 第 2 章，`AIR 开发`：涵盖了启动 AIR 开发的提示，以及创建你的第一个应用程序。
- 第 3 章，`在 AIR 中使用 JavaScript 和 HTML`：概述了 AIR 中的 HTML 和 JavaScript 环境，并介绍了如何使用 JavaScript 来访问功能和 API。
- 第 4 章，`AIR手册`：以 O'Reilly 的格式，提供了在 AIR 应用程序内完成常见任务的提示。
- 附录 A，`命令行工具`：列出了 AIR 特有的命令行工具及其选项。
- 附录 B，`AIR JavaScript 别名`：列出了 Adobe AIR API。

## 如何使用本书

既可以将本书作为 AIR 的入门和概述，也可以作为开始 AIR 应用程序开发的分步指南。虽然直接跳到特定部分可能，但强烈建议你至少阅读前两章，这两章提供了 AIR 的概述并讨论了如何设置开发环境以构建 AIR 应用程序。这将使你更容易深入了解感兴趣的领域。一旦通读了本书并了解如何使用 HTML 和 JavaScript 构建 AIR 应用程序的基础知识，你可以将本书作为参考，在需要了解如何解决特定问题时参考特定章节。特别是 Cookbook 部分在您开发 AIR 应用程序时证明非常有用。

最后，本书只是 AIR 的入门，没有涵盖所有的功能。它的目的是补充，而不是替代 Adobe 提供的广泛而深入的 AIR 文档。请务必探索 AIR 文档以确保你熟悉未涵盖的所有 API 和功能。

## 本书中使用的约定

本书使用了以下排版约定：

**纯文本**：表示菜单标题、菜单选项、按钮和键盘快捷键（例如 `Alt` 和 `Ctrl`）。

*斜体*：表示新术语、URL、电子邮件地址、文件名、文件扩展名、路径名、目录和 Unix 实用程序。

`等宽字体`：表示命令、选项、开关、变量、属性、键、函数、类型、类、命名空间、方法、模块、参数、值、对象、事件、事件处理程序、XML 标签、HTML 标签、宏、文件内容或命令的输出。

**等宽粗体**：显示用户按字面意思输入的命令或其他文本。

*等宽斜体*：显示应替换为用户提供的值。

## 许可和代码示例

所有作品均根据知识共享署名-非商业性使用-相同共享 3.0 许可证进行许可。

要查看此许可证的副本，请访问 `http://creativecommons.org/licenses/by-nc-sa/3.0/`；或者 (b) 将信件发送至 Creative Commons, 543 Howard Street, 5th Floor, San Francisco, California, 94105, USA。

你可以在 `http://www.creativecommons.org` 找到有关知识共享的更多。

## 支持和更多信息

### 在线访问本书

你始终可以在本书网站上找到有关本书的最新信息，并下载其免费电子版本：

http://www.adobe.com/go/airjavascriptpocketguide

## 在线 AIR 资源

尽管 AIR 是一项新技术，但已经许多资源可以在其中找到有关 AIR 和富 Internet 应用程序 (RIA) 开发的更多。

### 官方 AIR 网站

有关 AIR 的信息、下载和文档的主要网站：

http://www.adobe.com/go/air

### AIR 开发者常见问题

官方 AIR FAQ，回答有关 AIR 开发的常见问题：

http://www.adobe.com/go/airfaq

### AIR 开发者中心

包含有关为 AIR 开发应用程序的文章、信息和资源的开发者中心：

http://www.adobe.com/go/airdevcenter

### AIR API 参考

AIR JavaScript API 参考：

http://www.adobe.com/go/airapi

### AIR 文档

完整的 AIR 文档：

http://www.adobe.com/go/airdocs

### AIR 论坛

用于讨论为 AIR 开发应用程序的官方 Adobe 论坛：

http://www.adobe.com/go/airforums

Kevin Hoyt 是 `Adobe Systems, Inc.` 的平台布道者，喜欢移动、打破、模糊和跨越传统技术的界限。他寻找每一个机会与其他志同道合的开发者开发者聚集，探索逃离任何形成盒子的界限的方法。推动技术能力的极限，以及人们如何感知和与之互动，是他的热情所在。

Kevin 经常出差，通常可以在客户处、会议上、用户组面前或任何其他愿意给他时间面对观众的地方找到他深入编码的身影。其余时间，他喜欢与家人在科罗拉多州帕克的家中度过，并沉迷于摄影习惯。

Kevin 职业生涯的当前篇章始于 2000 年左右接受 `Allaire Corporation` 的工作，专注于 `ColdFusion` 和 `JRun`。Allaire 于 2001 年被 `Macromedia, Inc.` 收购，在那里他能够释放内心潜在的设计师身份，并帮助推广富互联网应用程序的价值。Adobe 于 2005 年收购了 Macromedia，Kevin 现在发现自己正在帮助公司及其客户理解日益庞大的产品系列。

# 致谢

作者要感谢 Adobe 的 `Mark Nichoson` 以及 O'Reilly 的 `Steve Weiss`、`Philip Dangler` 和 `Michele Filshie`，感谢他们在极短的时间内帮助本书得以实现。我们还要感谢 Adobe 的 `Adrian Ludwig`、`Laurel Reitman`、`Chris Brichford`、`Lucas Adamski`、`Lucas Dixon` 和 `Jeff Swartz`，感谢他们对本书的投入和工作。

感谢 `AIR` 团队的每一位成员，在将 `1.0` 运行时推向市场的过程中所付出的奉献和辛勤工作。

# 第 1 章

## Adobe 集成运行时 (AIR) 简介

Adobe 集成运行时 (AIR) 是 Adobe 开发的一个跨平台桌面运行时，它允许 Web 开发人员使用 Web 技术构建和部署富 Internet 应用程序和 Web 应用程序到桌面。

> 提示：公开测试版发布之前，Adobe 集成运行时 (AIR) 在公开场合以其代号 `Apollo` 被提及。

为了更好地理解 Adobe AIR 的功能以及它试图解决的问题，首先了解一下 Web 应用程序（相对较短的）历史是有用的。

## Web 应用程序简史

在过去的几年里，应用程序从桌面迁移到 Web 浏览器的趋势正在加速。这受到多种因素的驱动，包括：

- 互联网作为通信媒介的增长
- Web 应用程序部署的相对简便性
- 通过浏览器针对多种操作系统的能力
- 高级客户端技术的成熟，例如浏览器和 `Flash Player` 运行时

早期的 Web 应用程序主要使用 `HTML` 和 `JavaScript` 构建，在很大程度上严重依赖于客户端/服务器交互和页面刷新。这种页面刷新模型与浏览器最初设计的基于文档的隐喻一致，但在显示应用程序时提供了相对较差的用户体验。

然而，随着 `Flash Player` 运行时的成熟，以及最近浏览器中 `Ajax` 类型功能的出现，开发人员开始能够摆脱基于页面的应用程序流程。开发人员开始能够通过浏览器提供更丰富的应用程序体验。在 2002 年 3 月的一份白皮书中，Macromedia 创造了“富 Internet 应用程序”（RIA）一词，来描述浏览器中这些新型应用程序，它们“融合了内容、应用程序逻辑和通信……使互联网更易于使用和更令人愉悦。”这些应用程序提供了更丰富、更类似桌面的体验，同时仍然保留了 Web 的核心跨平台特性：

Internet 应用程序关乎覆盖范围。Web 的承诺是内容和应用程序无处不在，无论平台或设备如何。富客户端必须拥抱并支持所有流行的桌面操作系统，以及最广泛的新兴设备平台，例如智能手机、PDA、机顶盒、游戏机和 Internet 设备。

## 提示

您可以在以下网址找到完整的白皮书和关于 RIA 的更多信息：`http://download.macromedia.com/pub/flash/whitepapers/richclient.pdf`

该论文继续列出了一些定义 RIA 的特性：

- 为执行代码、内容和通信提供高效、高性能的运行时。
- 将内容、通信和应用程序接口集成到一个通用环境中。

## 主要特性

- 提供强大且可扩展的交互对象模型。
- 通过组件和重用实现快速应用开发。
- 能够使用应用程序服务器提供的 Web 和数据服务。
- 支持连接和断开连接的客户端。
- 轻松部署在多平台和设备上。

这种在浏览器中提供更丰富、更类似桌面应用体验的趋势（由 `Flash Player` 运行时推动，近期 `Ajax` 也起到了作用）催生了 Web 应用程序的爆炸式增长。

## 通过浏览器交付应用程序的问题

如今，Web 已稳固地确立了其作为应用程序部署平台的地位，为开发者和最终用户带来了诸多益处。其中一些好处包括：

- 能够面向多平台和操作系统进行开发。
- 使用相对高级的编程和布局语言进行开发。
- 允许最终用户从任何连接互联网的计算机访问其应用程序和数据。
- 能够轻松地向用户推送应用程序更新。

Web 应用程序的增长体现在 Web 2.0 运动中，该运动几乎完全由基于 Web 的应用程序和 API 组成，同时也体现在主要公司和组织将 Web 应用程序作为核心商业模式进行采纳。

随着 Web 应用程序变得越来越复杂，它们开始挑战浏览器的功能边界以及应用程序的可用性。随着其普及度的增长，这些问题变得更加明显和重要，并凸显出开发者和最终用户仍面临许多重大问题。

Web 浏览器最初旨在交付和显示基于 `HTML` 的文档。事实上，浏览器的基本设计并未从这一目标发生显著转变。这种以文档为中心和以应用程序为中心的功能之间的根本冲突，在通过浏览器部署应用程序时产生了一系列问题。

### 界面冲突

通过浏览器部署的应用程序拥有自己的用户界面，这通常与浏览器的用户界面发生冲突。在最好的情况下会导致困惑，最坏的情况下会导致应用程序失败。经典的例子是浏览器的后退按钮。

### 与桌面的距离

由于 Web 安全模型（限制对机器的访问），Web 应用程序无法与桌面交互。富互联网应用程序（RIAs）试图通过浏览器提供更丰富、类似桌面的界面来改进这一点，但它们无法克服与桌面分离。

### 主要依赖在线体验

由于 Web 应用程序从服务器交付，并不留在用户的机器上，因此主要是一种在线体验。虽然目前正在使离线应用程序成为可能，但它们需要安装额外的浏览器扩展。

### 最低共同标准

最后，随着应用程序变得丰富、复杂，开发者面临 API 实现方面的差异。虽然可以通过特定浏览器的代码来克服这些问题，但由于缺乏共同标准，这增加了开发和维护成本。

## Adobe 集成运行时 (AIR) 简介

Adobe 集成运行时 (AIR) 是 Adobe 开发的一个跨平台桌面运行时，它允许 Web 开发人员使用 Web 技术构建和部署富 Internet 应用程序和 Web 应用程序到桌面。

> 提示：在公开测试版发布之前，Adobe 集成运行时 (AIR) 在公开场合以其代号 `Apollo` 被提及。

为了更好地理解 Adobe AIR 的功能以及它试图解决的问题，首先了解一下 Web 应用程序（相对较短的）历史是有用的。

## Adobe AIR 技术

Adobe AIR 包含的主要技术分为两个类别：应用程序技术和文档技术。

### 主要应用程序技术

应用程序技术是 Adobe AIR 的基础。Adobe AIR 包含两种主要的技术：`HTML` 和 `Flash`。

#### HTML / JavaScript

Adobe AIR 中的第一个应用程序技术是 `HTML` 和 `JavaScript`。这是一个完整的渲染引擎，支持以下内容：

- `HTML`
- `JavaScript`
- `CSS`
- `XHTML`
- 文档对象模型（`DOM`）

你不必使用 `Flash` 来构建应用程序。Adobe AIR 中使用的 HTML 引擎是开源的 `WebKit`，这是许多浏览器背后的引擎。

#### Flash

Adobe AIR 构建的第二个应用程序技术是 `Flash Player`。具体来说，Adobe AIR 构建于 `Flash Player 9` 之上，它包含了基于 `ECMAScript` 的 `ActionScript 3` 以及开源的 `Tamarin` 虚拟机（该虚拟机用于解释未来版本中的 `JavaScript`）。

`Flash Player` 提供的功能包括：

- 即时编译的 `ActionScript` 引擎
- 完整的网络协议栈，涵盖 `HTTP`、`RTMP`，以及二进制套接字和 `XML` 套接字
- 完全基于矢量的渲染引擎与绘图 `API`
- 广泛的多媒体支持，包括位图、矢量图、音频和视频

### 主要文档技术

Adobe AIR 中的文档技术指的是用于渲染电子文档以及交互的技术。

#### PDF

可移植格式（`PDF`）是用于在网络上交付和显示电子文档的 Web 标准。它要求用户的计算机上安装 `Adobe Reader 8.1`。

#### HTML

`HTML` 最初被设计为一种文档技术，如今它为内容、文本布局和样式提供了丰富而强大的控制。`HTML` 可以在 Adobe AIR 中作为文档技术使用。

## Adobe AIR 应用程序包含什么

应用程序由以下技术组合构成：

- 仅 `HTML/JavaScript`
- 基于 `HTML/JavaScript`，但包含 `Flash` 内容
- 仅 `Flash`（包括 `Flex`）
- 基于 `Flash`，但包含 `HTML` 内容
- 所有组合都可以利用 `PDF` 内容

> 提示：在 Adobe AIR 的公开测试版中，`HTML` 中的 `Flash` 内容尚未实现，但在 `1.0` 版本中将会提供。

## 技术集成与脚本桥接

由于 `WebKit` 和 `Flash Player` 都包含在运行时中，它们在非常底层的层面进行了集成。例如，当 `HTML` 被包含在 `Flash` 内容中，它实际上是通过 `Flash` 显示管道进行渲染的。这种底层集成同样适用于 Adobe AIR 中运行的 `ActionScript` 和 `JavaScript` 的脚本引擎。Adobe AIR 在两种语言和环境之间提供了脚本桥接。

```markdown
一旦安装，Adobe AIR 应用程序就只是另一个原生应用程序，这意味着操作系统和用户可以像与任何其他应用程序一样与其交互。例如，操作系统级别的应用程序预取和应用程序切换等功能，对于 Adobe AIR 应用程序和原生应用程序的工作方式是相同的。

目标是最终用户不需要知道他们正在运行 Adobe AIR 应用程序就能使用它。他们应该能够以与交互桌面上任何其他应用程序相同的方式与 Adobe AIR 应用程序进行交互。

## 安全性

所有这些关于 API 和桌面功能的讨论引出了一个重要问题：安全性怎么办？由于 Adobe AIR 应用程序可以访问本地资源，理论上它们是否可能做一些有害的事情？

首先，需要注意的是 Adobe AIR 运行在操作系统安全层之上。它没有提供任何绕过或破坏此安全机制的方法。这很重要，因为它意味着 Adobe AIR 应用程序只能在其被操作系统授予的权限范围内运行——包括操作系统实现的所有现有和新的安全能力。

要运行 Adobe AIR 应用程序，用户必须将应用程序下载到桌面，经历一个安装流程，然后启动该应用程序。这是一种非常类似于下载和安装桌面应用程序的体验。这种相似性并非偶然。Adobe AIR 应用程序运行的安全上下文与在浏览器中运行的应用程序有着根本不同的。它更接近原生应用程序的安全上下文，而不是 Web 应用程序。

为了实现安全浏览，浏览器安全模型限制了 Web 应用程序所有的 I/O 能力。这包括限制它们处理本地资源的能力，限制可访问的网络资源，以及约束其用户界面。浏览器只允许应用程序连接与位于单个 Web 域上的服务器相关（通常由该服务器提供）的数据。此外，浏览器提供了一个可信的 UI，让用户了解应用程序的来源并控制应用程序的状态。此模型足以满足连接到单个服务提供商并依赖该服务进行数据同步和存储的应用程序。

部分网络开发者通过整合多方数据源和/或尝试与浏览器外观不一致的用户界面，进一步拓展了浏览器安全模型。其中一些应用需要浏览器插件提供当前浏览器尚未支持的功能。另一些则利用用户通知或自定义安全配置等浏览器特性，实现对特定域名应用的安全权限控制。这些机制使网络开发者能够构建更强大的应用程序，但同时也使浏览器安全模型承受了更大压力。

Adobe AIR 并非试图扩展网络浏览器使其兼具浏览器与灵活应用运行时的双重功能，而是提供了一个基于网络技术构建应用的灵活运行环境。Adobe AIR 允许网络开发者构建能够整合多方数据源、让用户自主掌控数据存储方式与位置，并创造出浏览器界面无法实现的用户体验的应用程序。由于 Adobe AIR 应用程序必须安装在桌面端且需要用户明确授权信任，因此能够安全行使这些能力。若要保持浏览器作为安全浏览任意网站工具的核心地位，基于浏览器的应用程序就无法获得这些能力。

Adobe AIR 安全模型对应用开发者和用户均有重要影响。对开发者而言，这意味着已安装的 AIR 应用中的内容拥有不应暴露给任何不受信任内容（包括网络文件）的能力。运行时系统通过一系列特性来强化这一区分，并帮助开发者遵循最佳安全实践构建应用。

这也意味着用户不应安装来源不明的 Adobe AIR 应用。此做法与当前原生桌面应用及浏览器插件的管理方式类似。许多应用和网络内容需要安装浏览器插件（如 Flash Player 或 Apple Quicktime）才能运行。Firefox 浏览器提供了高度开放的扩展层，本质上允许任何开发者扩展浏览器功能。这些应用、插件和扩展可能执行潜在有害操作，因此需要用户信任内容来源。

最后，Adobe AIR 1.0 版本将包含的一项重要能力是运行时系统可验证应用发布者的身份标识。用户应审慎考虑是否信任该发布者，以及是否要安装未签名的应用程序。

## Adobe AIR 开发工具集

网络应用取得成功的原因之一在于它们允许开发者轻松部署应用，用户无需关心操作系统类型。无论是在 Mac、Windows、Linux、Solaris 还是手机端，网络应用都能实现广泛覆盖。

然而，成功不仅基于跨平台部署，还依赖于开发环境的跨平台特性。这确保了任何开发者都能开发并利用这项技术。运行时系统与开发工具均不绑定特定操作系统。

Adobe 集成运行时同样如此。Adobe AIR 不仅提供了网络应用的跨平台覆盖能力，更重要的是，Adobe AIR 应用可以在几乎所有操作系统上进行开发与打包。

由于 Adobe AIR 应用采用 HTML 和 Flash 等现有网络技术构建，您可以使用创建浏览器内容的同一套工具来开发 Adobe AIR 应用。Adobe AIR SDK 提供了一系列免费的命令行工具，支持使用几乎任何网络开发与设计工具对 Adobe AIR 应用进行测试、调试与打包。

- `ADL` 无需预先安装即可运行 Adobe AIR 应用
- `ADT` 将 Adobe AIR 应用打包为可分发的安装包

尽管 Adobe 将在自有网络开发与设计工具中增加对 Adobe AIR 内容创作的支持，但创建应用并不强制要求使用 Adobe 程序。通过 Adobe AIR 命令行工具，您可以使用任何网络开发工具创建 AIR 应用，继续沿用当前熟悉的开发设计环境。

> **提示**
> 开发流程将在第二章进行深入讲解。

## Adobe AIR 是否意味着浏览器网络应用的终结？

此刻您可能在想：“Adobe AIR 听起来确实很棒！为什么还要通过浏览器部署应用呢？难道这是浏览器内网络应用的终结吗？”

答案是否定的。

让我们重申一次：并非如此。

Adobe AIR 解决了通过浏览器部署网络应用的大部分问题，但通过浏览器部署应用仍具优势。尽管存在前述缺点，网络应用依然数量庞大，这证明了在浏览器中运行的价值。当这些优势超过劣势时，开发者仍会选择通过浏览器部署应用。

但这并非非此即彼的选择。由于 Adobe AIR 应用基于网络技术构建，您可以通过浏览器快速将现有网络应用转换为 Adobe AIR 应用。您可以保留提供浏览器功能的网络版本，同时拥有利用桌面运行优势的 AIR 版本。两个版本可共享相同的技术、语言和代码库。事实上，FineTune 和 eBay Desktop 等早期热门 Adobe AIR 应用正是对现有网络应用的有力补充。

> **提示**
> 可访问 `http://www.finetune.com/desktop/` 获取 FineTune Desktop 更多信息。
> 可访问 `http://blogs.ebay.com/projectsandimas` 了解 eBay 的"San Dimas" Adobe AIR 应用项目详情。

Adobe AIR 应用是对网络应用的补充而非替代。

## 第二章：AIR 开发入门

本章介绍如何使用 HTML 和 JavaScript 开始开发 Adobe 集成运行时应用，涵盖以下内容：

- 安装 Adobe AIR
- 配置 Adobe AIR SDK 和命令行工具
- 创建您的第一个 AIR 应用
- 测试 AIR 应用
- 打包与部署 AIR 应用

完成本章学习后，您的 AIR 应用开发环境将配置就绪，并对构建、测试和部署 AIR 应用的流程有扎实理解。

### 开发 AIR 应用需要哪些准备？

开始开发 AIR 应用需要以下必备条件。

### Adobe 集成运行时 Beta 版

AIR Beta 版用于测试应用图标及 AIR 应用部署，可从以下地址免费下载：

http://www.adobe.com/go/air

### Adobe AIR SDK

Adobe AIR SDK 包含命令行工具、示例文件及其他资源，可简化 AIR 应用开发过程。我们将重点使用 SDK 中的命令行工具（`ADL` 和 `ADT`），它们支持从任何开发环境测试和打包 AIR 应用。

可从以下地址免费下载 AIR SDK：

http://www.adobe.com/go/air

### HTML/JavaScript IDE 或编辑器

使用 HTML 和 JavaScript 构建 AIR 应用需要相应的文件创建工具。您可以使用任何支持创建和编辑文本文件的工具（如 `VIM` 或 记事本），但建议选用对 HTML 和 JavaScript 文件支持更完善的工具，例如 Adobe Dreamweaver、Panic 的 Coda 或 Aptana。

### 支持的操作系统

虽然可以在几乎所有操作系统（包括 Linux）上开发和打包 AIR 应用，但测试和部署应用仅限 Adobe AIR 支持的操作系统。

Beta 版支持的操作系统包括：

- Windows XP SP2
- Windows Vista 家庭终极版
- Mac OS 10.4.8 和 10.4.9（Intel 和 PowerPC 版本）

Adobe AIR 1.0 正式版将支持更多版本的 Mac 和 Windows 系统，Linux 支持将在 1.0 版本发布后不久推出。

## 卸载 Adobe AIR 预测试版本

如果您之前安装过早期版本的 Adobe AIR（以前称为 Apollo），你需要在安装 Beta 版本之前卸载这些版本。

### 在 Windows 上卸载

1.  在 Windows 开始菜单中，选择“设置” → “控制面板”。
2.  选择“添加或删除程序”控制面板。
3.  选择 Adobe Apollo 1.0 Alpha1 以卸载 Apollo 运行时。
4.  单击“更改/删除”按钮。

### 在 Mac 上卸载

1.  删除 `/Library/Frameworks/Adobe Apollo.framework` 目录。
2.  删除 `/Library/Receipts/Adobe Apollo.pkg` 文件。
3.  清空废纸篓。

完成以上操作后，您就可以安装 Beta 运行时了。

## 安装 Adobe AIR

虽然开发和测试 AIR 应用程序并不需要在计算机上安装 Adobe AIR，但安装它对于尝试其他 AIR 应用程序以及测试最终应用程序的部署和打包非常有用。

安装运行时很简单，只需下载并运行 Adobe Integrated Runtime 安装程序即可。

1.  从 `http://www.adobe.com/go/air` 下载 AIR 安装程序。
2.  启动安装程序。在 Mac 上，你必须首先挂载。
3.  在 Mac 上，你必须首先挂载。

（注：原文此处存在部分重复描述，已按指令要求保留核心逻辑）
```

```markdown

应用程序描述符文件是每个 AIR 应用程序必需的 XML 文件。它为 Adobe AIR 提供有关应用程序的通用元数据（例如应用程序名称和描述），以及有关应如何运行应用程序的信息。这包括指定应用程序的根应用程序文件以及初始应用程序窗口应使用的窗口模式。

首先，让我们查看整个应用程序描述符文件（`AIRHelloWorld.xml`），然后我们将详细介绍文件中的每个项目。

> 提示
> 您可以在 AIR SDK 的 `templates` 文件夹中找到示例应用程序描述符文件。

## 打开 AIRHelloWorld.xml 并输入以下文本：

```xml
<?xml version="1.0" encoding="UTF-8"?>
<application xmlns="http://ns.adobe.com/air/application/1.0.M4"
             appId="com.oreilly.AIRHelloWorld"
             version="1.0">

    <name>AIRHelloWorld</name>
    <title>AIRHelloWorld Installer</title>
    <description>Simple Hello World Example
        using HTML</description>
    <copyright></copyright>

    <rootContent systemChrome="standard"
                 transparent="false" visible="true">
        ApolloHelloWorld.html</rootContent>

</application>
```

这段内容的含义应该不言自明，但让我们逐行分析一下，以了解具体发生了什么。

```xml
<application xmlns="http://ns.adobe.com/air/application/1.0.M4"
             appId="com.oreilly.AIRHelloWorld"
             version="1.0">
```

这里有两点值得指出。首先，命名空间定义：

```xml
xmlns="http://ns.adobe.com/air/application/1.0.M4"
```

这指定了应用程序所针对的 Adobe AIR 版本。在此例中，它指定的是 `1.0.M4`，即公开 Beta 版。

`appId` 属性很重要，它为 AIR 应用程序指定了一个唯一标识符。Adobe AIR 使用此 ID 来区分不同的应用程序。

如你所见，它使用了反向域名格式，你可能在 Java、ActionScript 和一些 JavaScript 框架等编程语言中对此有所了解。你可以使用自己的域名和应用程序名称来创建自己的 ID。

接下来的元素部分指定了应用程序的一般元数据：

```xml
<name>AIRHelloWorld</name>
<title>AIRHelloWorld Installer</title>
<description>Simple Hello World Example using HTML</description>
<copyright></copyright>
```

| 元素 | 描述 |
| :--- | :--- |
| name | 应用程序的名称。这是将暴露给操作系统和用户的名称。 |
| title | 将用于应用程序安装程序的标题。 |
| description | 应用程序的可读描述，将在安装过程中呈现给用户。 |
| copyright | 可选。允许指定应用程序的版权信息。 |

下一个元素是 `rootContent` 标签，它告诉 Adobe AIR 哪个应用程序文件是应用程序的主根内容：

```xml
<rootContent systemChrome="standard" transparent="false" visible="true">ApolloHelloWorld.html</rootContent>
```

该元素的值应指向应用程序的主根文件，在本例中是一个 HTML 文件。

> 提示
> 应用程序描述符文件和根内容文件必须位于同一文件夹中。

`rootContent` 元素具有多个属性，用于指定应用程序首次启动时的初始窗口参数和外观。

| 元素 | 描述 |
| :--- | :--- |
| systemChrome | 应用程序应使用的系统外观类型（“standard” 或 “none”）。 |
| transparent | 应用程序背景是否应透明。如果 `systemChrome` 设置为 `standard`，则此属性为 `true`。 |
| visible | 应用程序在首次启动时是否可见。如果您的应用程序需要在向用户显示 UI 之前执行一些复杂的初始化，这会很有用。 |

对于我们的示例，我们将使用操作系统的窗口外观。

这就是我们的应用程序描述符文件所需的全部内容。至此，我们已准备好创建应用程序的主 HTML 文件。

## 创建根应用程序文件

根应用程序文件是应用程序启动时将加载的主文件。此文件可以是已编译的 Flash 文件（SWF），也可以是 HTML 文件。

在本章中，我们将创建一个非常简单的 HTML 文件，以确保我们的开发环境配置正确。我们将在第 3 章和第 4 章介绍更高级的 AIR API 用法。

```html
<html>
<head>
    <title>AIRHelloWorld</title>
    <script>
        function init()
        {
            runtime.trace("init function called");
        }
    </script>
</head>
<body onload="init()">
    <div align="center">Hello World</div>
</body>
</html>
```

如你见，这是一个非常基础的 HTML 文件，显示 “Hello World”，并在文件加载后调用一个 JavaScript 函数。有几行代码值得指出：

```html
<body onload="init()">
```

在 `body` 元素上使用标准的 `onload` 事件，作为入口点：

```javascript
<script>
    function init()
    {
        ...
    }
</script>
```

然后我们使用标准的 JavaScript 函数来捕获 `onload` 事件。

## 访问 AIR API

查看 `init` JavaScript 函数，你会看到一些可能熟悉的代码：

```javascript
runtime.trace("init function called");
```

这是整个应用程序中唯一的 AIR 特定代码。`runtime` 属性是 Adobe AIR 放置在 `window` 对象上的属性，提供了进入 AIR 引擎和 API 的入口。`trace` 函数是一个顶层的 AIR API，它接收一个字符串，将其输出到命令行（通过命令行应用程序时）。

所有对 AIR 特定 API（包括 Flash Player）都是通过 JavaScript 中的 `runtime` 属性进行的。我们将在本书后续部分详细介绍这一点。

```javascript
if(window.runtime)
{
    // 在 AIR 内运行
}
```

现在已经创建了应用程序描述符文件和根 HTML 文件，我们已准备好在运行时运行和测试我们的应用程序。

## 测试应用程序

虽然越来越多的 HTML IDE（如 Dreamweaver）支持直接从 IDE 内启动和测试 AIR 应用程序，但我们将重点介绍如何使用 SDK 中包含的 `adl` 命令行工具来启动和测试 AIR 应用程序。这将为理解其工作原理提供基础，并在开发流程集成时也能提供最大的灵活性。

### 使用 ADL 启动应用程序

测试应用程序的第一步是将其作为 AIR 运行，以确保：
- 应用程序描述符文件中错误
- 应用程序能够启动
- HTML 能够渲染
- JavaScript 代码按预期工作

我们可以打包整个应用程序然后安装它，但这很琐，并且难以快速迭代。幸运的是，Adobe AIR 提供了一个名为 `adl` 的命令行工具，允许你无需安装即可启动 AIR 应用程序。

为了测试我们的应用程序：
1. 打开终端（在 Mac 上）或控制台（在 Windows 上）。
2. 切换到包含 `AIRHelloWorld.html` 和 `AIRHelloWorld.xml` 文件的目录。
3. 使用以下命令运行 `adl`，传入应用程序描述符文件名：

```
adl AIRHelloWorld.xml
```

这应该会在你的操作系统标准窗口中启动你的应用程序。如果应用程序未能正确启动或遇到错误，请检查以下点：
- 确保已正确配置 SDK，以便找到 `adl` 工具。
- 确保是在包含 `AIRHelloWorld.xml` 的同一目录中运行 `adl`。
- 确保应用程序描述符文件包含正确的 XML。
- 确保应用程序描述符文件中的信息正确。特别注意属性和 `rootContent` 值。
- 确保 `AIRHelloWorld.html` 和 `AIRHelloWorld.xml` 文件位于同一目录。

一旦修复了任何问题并且应用程序运行正确，你就可以探索如何在运行时从应用程序获取信息。

## 在运行时捕获输出

通过 `adl` 从命令行运行应用程序时，有多种方法从应用程序获取运行时信息和调试信息。

### 运行时 JavaScript 错误

当通过 `adl` 启动 AIR 应用程序运行时，JavaScript 执行过程中出现的任何错误都将输出到 `adl` 的标准输出。让我们修改应用程序以产生一个 JavaScript 运行时错误。将 `AIRHelloWorld.html` 的内容更改为：

```html
<html>
<head>
    <title>AIRHelloWorld</title>
    <script>
    function init()
    {
        runtime2.trace("init function called");
    }
    </script>
</head>
<body onload="init()">
    <div align="center">Hello World</div>
</body>
</html>
```

我们所做的只是修改了 `init` 函数，尝试访问一个名为 `runtime2` 的不存在的属性：

```javascript
runtime2.trace("init function called");
```

保存文件，然后从 ADL运行应用程序：

```
adl AIRHelloWorld.xml
```

应用程序应该启动，并且你应该从启动应用程序的命令行看到以下输出：

```
ReferenceError: Can't find variable: runtime2
init at app-resource:/AIRHelloWorld.html : 8
init at app-resource:/AIRHelloWorld.html : 8
onload at app-resource:/AIRHelloWorld.html : 13
```

此输出提供了错误信息，在本例中就是找不到名为 `runtime2` 的变量，以及错误发生的行号和执行调用的堆栈跟踪。这些信息可用于追踪应用程序中的任何错误。

有时应用程序可能无法正常工作，但不会抛出错误。在这种情况下，能够捕获运行时状态信息对于追踪任何问题非常有用。Adobe AIR 提供了一个函数，使应用程序能够在运行时将信息发送到标准输出。

## runtime.trace

正如我们在本章前面提到的，Adobe AIR 提供了一种从 JavaScript 向命令行发送字符串的机制。`runtime` 属性上的 `trace` 函数接受一个字符串，该字符串将被输出到 `adl` 的标准输出。以下是其用法示例：

```
runtime.trace("This will be sent to standard out");
```

这可用于跟踪应用程序状态信息，而无需中断程序的执行。传递给 `trace` 的任何非字符串对象都将调用其 `toString()` 函数。JavaScript `Object` 对象提供了一个默认的 `toString()` 实现，尽管一些类（例如 `Array`）实现了更符合上下文的 `toString()` 函数。

以下是跟踪一个包含各种数据类型的数组的示例：

```javascript
var a = ["a", 1, {foo:"bar"}];
runtime.trace(a);
```

这将在的命令行产生以下输出：

```
a,1,[object Object]
```

当然，你可以在自定义 JavaScript 类上实现你自己的 `toString()` 方法，或者重写现有类的 `toString()` 函数，以提供更具类特定性的输出。

## 打包和部署 AIR 应用程序

既然我们了解了如何构建、测试和调试 AIR 应用程序，我们就准备好创建一个 AIR 文件，该文件将允许我们部署和分发应用程序。

### 什么是 AIR 文件？

AIR 文件是一个基于 zip 的分发包，用于分发 AIR 应用程序。它包含安装和运行 AIR 应用程序所需的文件，并被 Adobe Integrated Runtime 用于在用户的系统上创建和安装应用程序。

> 提示
> AIR 文件要求用户的系统上已经安装了 Adobe AIR。
> `adl` 还能够创建特定于操作系统的本地安装程序，该安装程序将首先安装 Adobe AIR，然后在尚未安装 Adobe AIR 的系统上安装 AIR 应用程序。
> 此功能尚未在公共 Beta 版中实现。

### 使用 ADT 创建 AIR 文件

包含在 Adobe AIR SDK 中的 `adt` 命令行工具用于创建 AIR 文件。其使用格式为：

```
adl -package AIRFILENAME FILESTOINCLUDE
```

要为我们的应用程序创建 AIR 文件：

```
adt -package AIRHelloWorld.air AIRHelloWorld.xml AIRHelloWorld.html
```

```

```
这应该在同一目录中创建一个名为 `AIRHelloWorld.air` 的文件。如果文件未创建，或者你收到任何错误：

- 确保你已正确配置 SDK，以确保 `ADT` 工具可被找到。
- 确保你从包含 `AIRHelloWorld.xml` 文件的同一目录运行 `ADT` 命令。
- 确保你的应用程序描述符文件包含格式正确的 XML。
- 确保应用程序描述符文件中的信息正确。特别注意应用程序属性和 `rootContent` 值。
- 确保 `AIRHelloWorld.html` 和 `AIRHelloWorld.xml` 文件在同一目录中。

### 测试 AIR 文件

现在我们已经为应用程序创建了 AIR 文件，剩下的唯一步骤就是测试 AIR 文件并确保它正确安装。

测试 AIR 文件需要尝试将其安装到系统上，然后启动它：

1. 在 Windows 资源管理器（`Windows`）或 `Finder`（`Mac OS X`）中切换到包含 AIR 文件的目录。
2. 双击 AIR 文件。
3. 按照安装对话框中的说明进行操作。
4. 在安装对话框的最后一个屏幕，确保选中“运行应用程序”。

你的应用程序应该启动并运行。

如果它没有启动，或者你收到错误，请检查以下内容：

1. 确保你已正确安装 Adobe AIR 的 `Beta` 版本。
2. 确保通过 `ADL` 创建 AIR 文件时没有错误。
3. 确保你已卸载任何以前版本的 Adobe AIR。

一旦你确认应用程序已正确安装并运行，你可以通过单击其图标重新启动它。默认快捷方式位置因操作系统而异：

| 系统 | 快捷方式 |
|---|---|
| Mac OS X | `/Users/<USERNAME>/Applications` |
| Windows | 开始菜单 → 程序 → `<APPLICATION NAME>` |

### 部署 AIR 文件

一旦你成功创建并打包了你的 AIR 应用程序，剩下的就是分发应用程序。这是通过分发 AIR 文件来完成的，可以通过网络，或者直接通过 CD-ROM 或其他分发机制。

#### 设置 MIME 类型

从网络服务器分发 AIR 文件下载时需要注意的一件事是确保服务器上正确设置了 MIME 类型。如果 MIME 类型设置不正确，网络浏览器可能会将 AIR 文件视为 `zip` 文件（并在此过程中重命名它），或者可能在浏览器中显示 AIR 文件的原始字节，而不是将其下载到用户的系统。

AIR 文件的正确 MIME 类型是：

```
application/vnd.adobe.air-application-installer-package+zip
```

例如，要为 Apache 服务器设置 MIME 类型，你需要将以下行添加到你的 Apache 配置文件中：

```
AddType application/vnd.adobe.air-application-installer-package+zip .air
```

请查看你的网络服务器的文档，了解如何设置 MIME 类型的具体说明。

至此，你已经掌握了开发、测试和部署 AIR 应用程序的所有基础知识，并准备好开始使用 AIR API 构建功能更全面、更高级的应用程序。

# 第 3 章：在 AIR 中使用 JavaScript 和 HTML

本章深入概述了 Adobe Integrated Runtime 中的 HTML 和 JavaScript 环境。它讨论了：

- 在 Adobe AIR 中使用开源 `WebKit` HTML 渲染引擎
- Adobe AIR 中的 `JavaScript` 功能
- 功能的 AIR 特定实现
- 从 `JavaScript` 使用 AIR`、`Flash Player` 和 `ActionScript` API

完成本章后，你将对 Adobe AIR 中的 HTML 和 JavaScript 环境有一个扎实的理解。你还应该理解如何在基于 HTML 和 JavaScript 的应用程序中使用 AIR 和 `ActionScript` API。

### Adobe Integrated Runtime 中的 WebKit

Adobe AIR 利用开源 `WebKit` 渲染引擎为运行时添加了对渲染 HTML 内容的支持。

除了 HTML 渲染之外，`WebKit` 还提供对相关网络技术的支持，例如：

- `JavaScript`
- `XMLHttpRequest`

## 为何选择 WebKit？

Adobe 投入了大量时间研究在 Adobe AIR 中应使用哪种 HTML 引擎，并综合多项标准，最终决定采用 `WebKit`。

### 开源项目

Adobe 从一开始就知道，他们不想创建并维护自己的 HTML 渲染引擎。这不仅工作量巨大，还会给开发者带来麻烦，因为他们需要熟悉另一个 HTML 引擎的所有特性。

`WebKit` 为 Adobe AIR 提供了一个功能齐全的 HTML 引擎，它由一个强大的开发社区持续开发，该社区包括个人开发者以及诺基亚和苹果等大公司。这使得 Adobe 能够专注于修复错误和添加功能，同时也意味着 Adobe 可以积极地向 `WebKit` 贡献代码，同时利用 `WebKit` 项目其他成员的贡献。

### Web 开发者熟知的成熟技术

如前所述，复杂 Web 应用开发面临的最大问题之一，是确保内容在不同浏览器中表现一致。某些功能在 `Mac` 上的 `Firefox` 中可能运行完美，但在 `Windows` 上的 `Internet Explorer` 中可能完全失效。因此，测试和调试基于浏览器的内容对开发者来说可能是一场噩梦。

Adobe 希望确保开发者已经熟悉 Adobe AIR 中使用的 HTML 引擎，这样他们就无需学习新引擎的所有特性和错误。由于 `Safari`（基于 `WebKit` 构建）是 `Mac OS X` 的默认浏览器（也可在 `Windows` 上使用），开发者应该熟悉针对 `WebKit` 进行开发。

### 对 AIR 运行时大小影响最小

Adobe AIR 的目标大小在 5 到 9 MB 之间。`WebKit` 代码库编写精良、组织有序，对最终的 AIR 运行时大小影响最小。

### 已证明的移动设备运行能力

虽然 Adobe AIR 的首个版本仅在个人计算机上运行，但其长期愿景是将 Adobe AIR 从桌面扩展到手机和其他设备。`WebKit` 已证明能够在这些设备上运行，并且已被诺基亚和苹果移植到手机上。

## AIR 中的 JavaScript

Adobe AIR 对 HTML 内容中的 `JavaScript` 提供了完全支持。支持对应于 `ECMA-262` 的 `JavaScript` 1.5。

`JavaScript` 引擎通过 `WebKit` 实现，其工作方式与在基于 `WebKit` 的浏览器中相同。除了可以访问 HTML DOM，`JavaScript` 还可以直接通过 `window.runtime` 属性访问 AIR 和 `Flash Player` 的 API。稍后将对此进行更详细的讨论。

> 提示
> 如需深入了解和探讨 JavaScript，请参阅 O'Reilly 出版的《JavaScript 权威指南（第5版）》：http://www.oreilly.com/catalog/jscript5/

## AIR 的功能实现

HTML 和 `JavaScript` 的功能与其他基于 `WebKit` 的项目和浏览器（例如苹果的 Safari 浏览器）一致。在查阅关于 HTML 引擎/浏览器功能的文档时，可以将 `Safari` 浏览器作为 AIR 中 HTML 环境可用可用的参考。

然而，由于 HTML 引擎运行在运行时而非浏览器中，在开始使用 Adobe AIR 中的 HTML 和 JavaScript 进行开发之前，了解一些差异会很有帮助。

### Cookie

Adobe 集成运行时完全支持从基于 HTML 的内容中设置和获取 Cookie。Cookie 支持通过操作系统的网络栈实现。这意味着 AIR 应用程序可以共享由任何同样利用操作系统栈的浏览器或应用程序设置的 Cookie。

例如，AIR 应用程序可以共享通过 `Windows` 上的 `Internet Explorer` 和 `Mac` 上的 `Safari` 设置的 Cookie，因为它们都使用操作系统的 Cookie 存储功能。`Firefox` 实现了自己的 Cookie 存储，因此在 `Firefox` 中设置的 Cookie 无法与 AIR 应用程序共享。

> 提示
> 除了 Cookie，AIR 应用程序还有许多其他可用于持久化数据的 API，包括文件 API 以及嵌入式数据库 API。

#### 窗口

你可以像在浏览器中一样，通过 `JavaScript` 创建新窗口。

```javascript
myWindow = window.open("Window.html", "myWindow", "height=400,width=400");
```

但是，提供对 AIR 和 Flash Player API 访问权限的 `runtime` 属性在新窗口中并非自动可用。为了使其可用，你必须像这样显式-地将其放置在新窗口的作用域内：

```javascript
window.runtime = window.opener.runtime;
```

> 提示
> `Beta` 版本中尚不完全支持原生窗口。仅实现了从 JavaScript 可用的 API。

#### 对话框

AIR 应用程序也支持 HTML 对话框，但 `Beta` 版本中并未全部实现。

| 对话框 | Beta 版中是否支持 |
|---|---|
| alert | 是 |
| confirm | 是 |
| prompt | 否 |

### Ajax

AIR 应用程序也支持 `Ajax`。

...

#### 设置 MIME 类型

从网络服务器分发 AIR 文件下载时需要注意的一件事是确保服务器上正确设置了 MIME 类型。

AIR 文件的正确 MIME 类型是：

```
application/vnd.adobe.air-application-installer-package+zip
```

例如，要为 Apache 服务器设置 MIME 类型，你需要将以下行添加到你的 Apache 配置文件中：

```
AddType application/vnd.adobe.air-application-installer-package+zip .air
```

请查看你的网络服务器的文档，了解如何设置 MIME 类型的具体说明。

至此，你已经掌握了开发、测试和部署 AIR 应用程序的所有基础知识，并准备好开始使用 AIR API 构建功能更全面、更高级的应用程序。
```

<|channel>thought
<channel|>
```

在将基于 Web 和浏览器的内容及代码迁移到 AIR 应用程序时，您应牢记这一点。

## 安全性

本节讨论 Adobe AIR 中的安模型实现与浏览器中的安模型实现之间的若干差异。

### 安全上下文

在应用程序内安装的内容在应用程序的安全上下文中运行。这意味着它可以访问所有 Adobe AIR API 和功能。

加载到应用程序中的远程内容在 Web 安全上下文中运行，因此无法访问 Adobe AIR API 和功能，也无法访问应用程序内容所具有的扩展权限。

例如，通过以下方式加载到应用程序中的内容：：

`app-resource://foo.html`

拥有对 AIR API 的完全访问权限。但是，使用 HTTP 加载的内容，如下所示：

`http://www.yourdomain.com/foo.html`

在 Web 安全上下文中运行，无法访问 AIR API。

位于应用程序安装目录中的内容属于应用程序安全上下文。位于应用程序存储目录（`app-storage:/`）中的内容属于 Web 安全上下文（表 3-3）。

*表 3-3. 应用程序和 Web 安全上下文*

| 加载 URL 数据的来源 | 是否有权访问 AIR API？ |
| :--- | :--- |
| `app-resource://foo.html` | 是 |
| `app-storage://foo.html` | 否 |
| `http://www.anydomain.com/foo.html` | 否 |
| `https://www.anydomain.com/foo.html` | 否 |
| `file://C/foo.html` | 否 |
| `ftp://www.anydomain.com/foo.html` | 否 |

因此，从第三方来源和域下载的内容应始终放置在 `app-storage:/` 目录中，而不是 `app-resource:/` 目录中，以防止无意中提升安全上下文和权限。

### 跨域数据加载

Adobe Integrated Runtime 不对应用程序内容强制执行跨域数据加载限制。除其他外，这允许使用 `XMLHttpRequest` 对象跨域加载数据。

非特权 Web 内容会强制执行跨域数据加载限制。

### 使用 JavaScript 框架

由于 Adobe Integrated Runtime 中的 HTML 环境完全支持 JavaScript，您几乎可以使用任何 JavaScript 框架来构建应用程序。但是，在使用框架时，有几点需要记住：

- 框架应包含在您的应用程序的 AIR 文件中，以确保在离线时可用。
- 如果框架需要从中央服务器加载资源，您可能需要进行测试以确保相对 URL 仍然有效。
- 虽然可以在运行时从网络加载框架，但这可能导致应用程序启动性能较慢，以及在离线时无法工作。

您可以从 Adobe Labs AIR 网站找到许多基于 HTML 的 AIR 应用程序及其使用 EXT-JS 框架构建的源代码：

http://www.adobe.com/go/airwiki

> 提示

您可以在 http://extjs.com/ 找到有关 EXT-JS 框架的更多信息。

### 从 JavaScript 访问 AIR API

除了标准的 JavaScript 和 HTML DOM API 之外，在 AIR 应用程序的应用程序上下文中运行的 JavaScript 代码还可以利用运行时提供的 API，以及 Flash Player API，甚至 ActionScript 3 库。这极大地扩展了 JavaScript 相对于浏览器中可用 API 的能力，包括诸如：

- 播放声音
- 操作图像和位图
- 在本地文件系统上读写文件
- 创建、控制和操作原生窗口
- 进行直接套接字连接（二进制和基于文本）
- 访问剪贴板
- 利用嵌入式数据库存储数据

> 提示

您可以在第 4 章的实践部分找到如何利用这些功能的示例。

本节讨论如何从 JavaScript 中利用 AIR 和 Flash Player API，以及如何从 JavaScript 中加载和利用已编译的 ActionScript 库。

## 访问 AIR 和 Flash Player API

大多数 AIR 和 Flash Player API 都包含在包中（类似于许多 JavaScript 框架利用命名空间和包的方式）。这有助于组织 API，并减少命名冲突的可能性。当从 JavaScript 直接访问 AIR 和 Flash Player API 时，必须通过其完整的包路径和名称进行访问。

如前所述，所有 AIR 和 Flash Player API 都通过 `window.runtime` 属性提供。`runtime` 属性位于运行时环境的根部，所有 API 都相对于此根目录。

例如，要访问不包含在包中的 API，如 `trace()`，您直接从 `runtime` 属性引用它，如下所示：

```
window.runtime.trace("foo");
```

但是，如果您想访问包含在包中的 API，必须将包路径前置到 API。例如，要访问应用程序当前使用的内存量，您可以调用 `flash.system.System` 类中的 `totalMemory` Flash Player 属性。要从 JavaScript 调用此 API：

```
var mem = window.runtime.flash.system.System.totalMemory;
```

这同样适用于从 JavaScript 中创建新的 API 类实例：

```
var file = new window.runtime.flash.filesystem.File();
```

此代码创建一个新的 `File` 实例，可用于处理文件系统。

以下是一个完整示例，展示如何将名为 `output.txt` 的文件写入用户桌面：

```
//call a static property
var desktop = window.runtime.flash.filesystem.File.desktopDirectory;

//call a function on an instance of a class
var file = desktop.resolve("output.txt");

//create a new instance of a class using new
var fileStream = new window.runtime.flash.filesystem.FileStream();

//call a function, passing arguments
fileStream.open(file, window.runtime.flash.filesystem.FileMode.WRITE);

fileStream.writeUTFBytes("Hello World");

fileStream.close();
```

不要过于担心此示例中代码的功能，而是关注如何从 JavaScript 调用 AIR API。

这使您能够从 JavaScript 中利用几乎任何 AIR 或 Flash Player API。

> 提示

从 Adobe 网站下载 AIR 的 JavaScript 专用语言参考：http://www.adobe.com/go/air。

通过记住如何使用包结构调用 API，即使没有提供 JavaScript 特定文档，您也可以利用所有 AIR、Flash Player 和 ActionScript API。

## 处理 AIR 和 Flash Player 事件

许多 AIR 和 Flash Player API 广泛使用事件。基于 ActionScript 的 API 中的事件处理基于 W3C DOM Level 3 事件模型。这类似于 JavaScript 中可用的 W3C DOM Level 2 事件模型，但与 JavaScript 中经常采用的回调机制非常不同。

为了在 AIR 或 Flash Player API 的事件发生时得到通知，您必须注册监听它。理解这一点的最佳方式是查看一个示例。以下示例注册了一个由 Shell 类广播的 NETWORK_CHANGE 事件：

```
function onNetworkChange(event)
{
    runtime.trace("Network status changed");
}

function onAppLoad()
{
    window.runtime.flash.system.Shell.shell.addEventListener(
        window.runtime.flash.events.Event.NETWORK_CHANGE,
        onNetworkChange);
}
```

从示例中可以看出，您通过调用类实例上的 `addEventListener` 函数来注册该类实例广播的事件。此 API 需要两个参数。

第一个参数是正在广播的事件的事件名称。对于所有 AIR 和 Flash Player API，都会有事件名称的常量，您可以在文档中找到。

第二个参数是处理该事件的函数的引用。在本例中，函数名为 `onNetworkChange`。查看该函数，可以看到它接收一个包含有关事件信息的参数。同样，所有 AIR 和 Flash Player API 都会将一个对象传递给事件处理函数，该对象提供有关事件的信息。您可以通过参考 API 文档来找到传递给处理程序的确切事件对象类型及其提供的信息。

## 使用 AIRAliases.js

如前面的示例所示，能够直接从 JavaScript 中利用 AIR 和 Flash Player API 可能非常强大。但是，由于您必须引用通过 `runtime` 属性访问 API 以及使用完整的 API 包路径，可能会导致代码变得冗长。

为了更便捷地从 JavaScript 中使用一些更常用的 AIR 和 Flash Player API，可以使用 `AIRAliases.js`。该文件将常用的 API 映射到简短的别名，从而提高代码的可读性。

## AIR 实用技巧

### 添加自定义控件

**问题**

你想为你的应用程序创建自定义的窗口外观，并需要用户能够关闭和最小化应用程序。

**解决方案**

使用 AIR 中的原生窗口 API 来连接最小化和关闭按钮的功能。

#### 讨论

虽然 Adobe AIR 允许开发者完全定义和自定义应用程序的窗口外观，但重要的是要记住，应用程序负责处理所有可能发生的类型的窗口事件。这意味着需要将各个视觉元素与其相应的操作系统事件连接起来。



```
`NativeWindow.close()` 事件并不一定会终止应用程序。如果只有一个应用程序窗口可用，应用程序将终止。如果有多个窗口，它们将关闭，直到只剩一个窗口。关闭最后一个窗口将终止应用程序。
```

### application.xml

```xml
<?xml version="1.0" encoding="utf-8" ?>
<application
    xmlns="http://ns.adobe.com/air/application/1.0.M4"
    appId="com.adobe.demo.html.CustomChrome"
    version="1.0 Beta">
    <name>Custom Chrome</name>
    <title>Custom Chrome</title>
    <rootContent
        visible="true"
        transparent="true"
        systemChrome="none"
        width="206"
        height="206">
        custom.html
    </rootContent>
</application>
```

### index.html

```html
<html>
<head>
<title>Custom Window Controls</title>
<style>
body {
    background-image: url( 'custom-chrome.gif' );
    font-family: Verdana, Geneva, Arial, Helvetica, sans-serif;
    font-size: 12px;
}
#closer {
    position: absolute;
    width: 70px;
    left: 68px;
    top: 105px;
}
#minimize {
    position: absolute;
    width: 70px;
    left: 68px;
    top: 75px;
}
textarea {
    position: absolute;
    left: 8px;
    right: 8px;
    bottom: 8px;
    top: 36px;
    border-color: #B3B3B3;
}
</style>
```

## 窗口管理

## 创建新窗口

**问题**
你需要显示一个额外的窗口，以便加载其他内容。

**解决方案**
基本窗口可以通过类似传统HTML内容的方式生成和维护，使用 `window.open()` 方法。

**讨论**
JavaScript 的 `window.open()` 方法调用新窗口的方式类似于在浏览器中使用的方式。加载到新窗口的内容可以来自本地文件或URL端点。与在浏览器中使用JavaScript创建的窗口类似，对窗口本身的控制是有限的。可以控制的窗口属性包括宽度、高度、滚动条和可调整大小。

```javascript
var login = window.open( "login.html", "login", "width = 300, height = 200" );
```

当需要对新窗口进行额外控制时，原生窗口是更好的选择。原生窗口几乎暴露了操作系统的全部功能，例如最小化/最大化、始终置前、全屏，甚至完全移除系统边框。使用原生窗口的缺点是工作量显著增加，因为所有事件都必须显式监控和管理。

**提示**
在JavaScript中常用于新窗口引用（创建窗口）的 `opener` 属性也可以使用。

```html
<html>
<head>
<title>基本窗口</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script>
function doLoad()
{
    document.getElementById("btnLogin").addEventListener("click", doLogin);
}
function doLogin()
{
    var login = window.open("Login.html", null, "width=270, height=150");
}
</script>
</head>
<body onload="doLoad()">
<input id="btnLogin" type="button" value="登录" />
</body>
</html>
```

Login.html

```html
<html>
<head>
<title>登录</title>
</head>
<body>
<table>
    <tr>
        <td>电子邮件：</td>
        <td><input name="email" /></td>
    </tr>
    <tr>
        <td>密码：</td>
        <td><input name="password" /></td>
    </tr>
    <tr>
        <td colspan="2" align="right">
            <input type="button" value="登录" />
        </td>
    </tr>
</table>
</body>
</html>
```

## 创建原生窗口

**问题**
你需要显示一个额外的窗口以便加载其他内容，并且能够精细调整窗口方式。

**解决方案**
`NativeWindow` 类为创建和管理高度定制化的新窗口提供了基础。

**讨论**
原生窗口是创建和管理高度定制窗口的绝佳选择。你可能希望控制最小化/最大化按钮，还可能想控制窗口Z顺序，或强制窗口始终在前面。`NativeWindow` 类提供了这些方面及更多控制。`NativeWindow`构造函数接受两个参数：一个布尔值指定窗口是否可见，以及一个`NativeWindowOptions` 对象，该对象控制窗口方面，例如是否调整大小。

```javascript
var options = new air.NativeWindowOptions();
var login = null;
options.minimizable = false;
options.maximizable = false;
options.resizable = false;
login = new air.NativeWindow( false, options );
```

应用程序可能使用的所有选项。`NativeWindow` 实例本身上控制的附加选项包括窗口标题、始终在前面以及窗口的大小。

**提示**
如果你打算手动管理窗口大小，最好从一个不可见的窗口开始。创建一个原生窗口，然后在代码块中更改其位置和布局，会导致窗口在初始绘制后闪烁，因为它被重新定位和调整大小。使用 `NativeWindow` 类时，你可以完全控制其外观、行为和内容。如果窗口需要调整，操作系统仅提供句柄。窗口的大小、位置和布局必须由应用程序控制。根据应用程序处理大小的方式，可以使用 `NativeWindowEvent.RESIZE` 或 `NativeWindowEvent.RESIZING` 事件：

```javascript
login.title = "登录";
login.alwaysInFront = false;
login.bounds = new window.runtime.geom.Rectangle(
    ( air.Capabilities.screenResolutionX - 270 ) / 2,
    ( air.Capabilities.screenResolutionY - 150 ) / 2,
    270,
    150 );
login.visible = true;
```

原生窗口在运行时之外没有任何内容。与JavaScript的`window.open()`方法不同，应用程序不能简单指定一个URL来显示内容。窗口是如此原始，以至于应用程序必须向窗口添加一个`HTMLControl`，调整大小，并告诉它加载什么内容。`HTMLControl`构造函数接受参数，暴露了宽度高度属性，暴露了一个`HTMLControl.load()`方法，该方法用于加载外部内容：

```javascript
var control = new window.runtime.flash.html.HTMLControl();
var page = air.File.applicationResourceDirectory.resolve( "login.html" );
control.width = login.stage.stageWidth;
control.height = login.stage.stageHeight;
control.load( new air.URLRequest( page.url ) );
```

`NativeWindow.stage`属性表示一个`Stage`对象，用于确定查看区域以调整`HTMLControl`的大小。对`HTMLControl`调整大小使用`NativeWindow.width`或`NativeWindow.height`会导致`HTMLControl`与窗口一样大（包括边框）。`Stage.stageWidth`和`Stage.stageHeight`使控件适应查看区域。`Stage`也是将控件添加以显示（称为显示列表）的地方，并负责其内部内容如何定位和调整。对于大多数应用程序，意味着将`Stage.scaleMode`设置为`StageScaleMode.NO_SCALE`，将`Stage.align`设置为`StageAlign.TOP_LEFT`。调用`Stage.addChild()`会将`HTMLControl`添加到查看区域。使用这种方法，可以在单个窗口中拥有多个`HTMLControl`控件：

```javascript
win.stage.scaleMode = window.runtime.flash.display.StageScaleMode.NO_SCALE;
win.stage.align = window.runtime.flash.display.StageAlign.TOP_LEFT;
win.stage.addChild( control );
```

**提示**
在未来的版本中，`Stage`类和显示列表的知识可能会被抽象成更有用的高级类。

```html
<html>
<head>
<title>原生窗口</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script>
var Rectangle = window.runtime.flash.geom.Rectangle;
var control = null;
var win = null;
function doLoad()
{
    document.getElementById("btnLogin").addEventListener("click", doLogin);
}
function doLogin()
{
    var options = new air.NativeWindowInitOptions();
    var login = air.File.applicationResourceDirectory.resolve("login.html");
    options.minimizable = false;
    options.maximizable = false;
    options.resizable = false;
    win = new air.NativeWindow(false, options);
    win.title = "登录";
    win.alwaysInFront = true;
    win.bounds = new Rectangle(
        ( air.Capabilities.screenResolutionX - 270 ) / 2,
        ( air.Capabilities.screenResolutionY - 150 ) / 2,
        270,
        150 );
    win.visible = true;
    control = new window.runtime.flash.html.HTMLControl();
    control.width = win.stage.stageWidth;
    control.height = win.stage.stageHeight;
    control.load( new air.URLRequest( "http://www.adobe.com" ) );
    win.stage.scaleMode = window.runtime.flash.display.StageScaleMode.NO_SCALE;
    win.stage.align = window.runtime.flash.display.StageAlign.TOP_LEFT;
    win.stage.addChild( control );
}
</script>
</head>
<body>
</body>
</html>
```

## 全屏窗口

```html
<html>
<head>
<title>全屏窗口</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script>
var Rectangle = window.runtime.flash.geom.Rectangle;
var control = null;
var win = null;
function doLoad()
{
    var control = new window.runtime.flash.html.HTMLControl();
    var options = new air.NativeWindowInitOptions();
    options.minimizable = false;
    options.maximizable = false;
    options.resizable = false;
    options.systemChrome = air.NativeWindowSystemChrome.NONE;
    win = new air.NativeWindow( false, options );
    win.visible = true;
    control.width = win.stage.stageWidth;
    control.height = win.stage.stageHeight;
    control.load( new air.URLRequest( "http://www.adobe.com" ) );
    win.stage.scaleMode = window.runtime.flash.display.StageScaleMode.NO_SCALE;
    win.stage.align = window.runtime.flash.display.StageAlign.TOP_LEFT;
    win.stage.addChild( control );
}
</script>
</head>
<body onload="doLoad()">
</body>
</html>
```


```markdown
### 创建全屏窗口

#### 问题
为了提供更多的显示空间或支持额外的交互，你的应用程序需要能够以全屏模式运行。

#### 解决方案
`NativeWindow` 类为创建透明和全屏窗口提供了基础。

#### 讨论
使用 `NativeWindow` 进行全屏显示与用于自定义窗口的主要区别在于需要额外的初始化选项以及将窗口设置为填充屏幕。要移除任何操作系统特定的窗口界面，请使用 `NativeWindowInitOptions.systemChrome` 属性。应将 `NativeWindowInitOptions.systemChrome` 设置为 `NativeWindowSystemChrome` 类中的四个字符串常量之一（表 4-1）。

#### 表 4-1. NativeWindowSystemChrome 中的字符串常量

| 字符串常量 | 描述 |
| --- | --- |
| `NativeWindowSystemChrome.STANDARD` | 这是 `NativeWindow` 的默认值，反映了特定操作系统上使用的窗口界面。 |
| `NativeWindowSystemChrome.UTILITY` | 实用工具界面最适合需要长时间保持打开的相关窗口，例如工具面板。 |
| `NativeWindowSystemChrome.NONE` | 表示不应有任何界面，并要求应用程序处理所有传统的窗口任务。 |
| `NativeWindowSystemChrome.ALTERNATE` | 在 Adobe AIR Beta 版中未实现。 |

要创建没有任何界面的全屏窗口，应将 `NativeWindowInitOptions.systemChrome` 属性设置为 `NativeWindowSystemChrome.NONE`。然后，应用程序可以调用 `NativeWindow.maximize()` 方法，或直接设置 `NativeWindow.bounds`。`NativeWindow.bounds` 属性接受一个 `flash.geom.Rectangle` 对象，该对象指定了水平和垂直原点，以及宽度和高度。任一方法都会用新创建的原生窗口填充可见屏幕。

```javascript
var options = new air.NativeWindowInitOptions();
var login = null;
options.minimizable = false;
options.maximizable = false;
options.resizable = false;
options.systemChrome = air.NativeWindowSystemChrome.NONE;
login = new air.NativeWindow( false, options );
login.maximize();
```

## 提示
如果你遇到一个应用程序无法关闭，但其所有可见窗口都已关闭的情况，那么你可能面临几种不同的挑战。第一种是你从未为 `NativeWindow` 设置大小。第二种是你从未将 `NativeWindow` 设置为可见。最常见的情况是你使用了 `NativeWindowSystemChrome.NONE`，但从未添加任何内容。

## 文件 API

### 从字符串将文本写入文件

#### 问题
用户已在应用程序中修改了文本内容，并希望将其保存到磁盘以供离线访问。

#### 解决方案
文本写入可以通过 AIR 中的 `File` 和 `FileStream` 类来完成。

#### 讨论
在对磁盘进行任何读写操作之前，应用程序中必须先存在对文件或目录的引用。文件引用可以通过多种方式建立，包括程序化操作和用户选择。这两种方式都使用 `File` 类来完成。`File` 类还包含指向操作系统常见位置的静态属性。这些位置包括桌面目录、用户目录和文档目录：

```javascript
var file = air.File.applicationStorageDirectory.resolve( "myFile.txt" );
```

对 `File.resolve()` 的调用会创建一个对位于应用程序存储目录中名为 `myFile.txt` 的文件的引用。一旦建立了引用，就可以在文件 IO 操作中使用它。请注意，此时文件实际上并未被创建。

使用 `FileStream` 类可以进行实际的磁盘读写操作。`FileStream` 类在其构造函数中不接受任何参数：

```javascript
var stream = new air.FileStream();
```

有了可用的文件引用和实例化的 `FileStream` 对象，就可以开始将数据写入磁盘的过程。可写入的数据类型可以是二进制、文本或值对象等任何类型。所有这些都可以通过使用相应的 `FileStream` 方法来访问。

写入文件的第一步是使用 `FileStream.open()` 方法打开它。`FileStream.open()` 方法接受两个参数。第一个参数是先前创建的文件引用，它将是输出的目标。第二个参数是应用程序需要对该文件的访问类型。在将数据写入文件的情况下，`FileMode.WRITE` 静态属性最常用。根据应用程序需求，也可以使用 `FileMode.APPEND`：

```javascript
stream.open( file, air.FileMode.WRITE );
```

写入文本时，应用程序应使用 `FileStream.writeMultiByte()` 以确保使用正确的编码写入数据。`FileStream.writeMultiByte()` 方法接受两个参数。第一个参数是要写入磁盘的 `String` 对象（文本）。第二个参数是要使用的字符集。最常见的字符集是操作系统正在使用的字符集，可通过 `File` 类的 `File.systemCharset` 属性获取：

```javascript
stream.writeMultiByte( document.getElementById( "txtNote" ).value, air.File.systemCharset );
```

将文本写入文件后，关闭文件非常重要，以避免损坏或阻止其他应用程序访问。使用 `FileStream.close()` 方法可以关闭文件。

> XML 数据本身已经是文本格式，因此可以使用相同的步骤写入磁盘。如果应用程序使用 `XMLHttpRequest` 对象，那么在大多数情况下仅使用 `myXml.responseText` 属性可能就足够了。

```html
<html>
<head>
<title>写入文本</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script>
function doLoad() {
    document.getElementById( "btnSave" ).addEventListener( "click", doSave );
}
function doSave() {
    var file = air.File.applicationStorageDirectory.resolve( "note.txt" );
    var stream = new air.FileStream();
    stream.open( file, air.FileMode.WRITE );
    stream.writeMultiByte( document.getElementById( "txtNote" ).value, air.File.systemCharset );
    stream.close();
}
</script>
</head>
<body onload="doLoad()">
    <textarea id="txtNote"></textarea>
    <input id="btnSave" type="button" value="保存" />
</body>
</html>
```

### 从文件同步读取文本

你需要将一个小文本文件的内容读取到应用程序中。使用 Adobe AIR 提供的各种文件 API 来定位、打开和读取文本。包含文本内容的小文件可以使用 `FileStream.open()` 方法读取。此方法以同步方式打开文件进行读取。同步访问需要较少的代码，但在数据完成之前会阻塞用户输入。使用异步访问不会阻塞用户输入，但必须注册事件程序。

> 提示：可以将 XML 文件作为文本来访问，但此方法的结果无法直接操作。将 XML 文件用作数据时，通常使用 `XMLHttpRequest` 或大多数 JavaScript 库提供的功能处理更容易。

同步读取文件的步骤总是相同的：
1. 获取一个 `File` 引用
2. 创建一个 `FileStream` 对象
3. 以同步方式打开流
4. 调用适当的 `FileStream` 方法
5. 关闭文件

读取文本的第一步是获取磁盘上资源的引用。可以通过在 `File` 对象上使用适当的属性（如 `File.applicationStorageDirectory`）以编程方式指定路径来建立引用。使用此方法还需要调用 `resolve()`，因为 `File` 类属性总是返回目录：

```javascript
var file = air.File.applicationStorageDirectory.resolve( "myfile.txt" );
```

`FileStream` 类有一个空构造函数，可以在应用程序中的任何位置实例化。建立的文件引用在打开物理过程中使用。必须指定文件模式。`FileMode` 对象除了为文件访问类型提供常量外，没有其他用途。这些操作是 `FileMode.READ`、`FileMode.WRITE`、`FileMode.UPDATE` 和 `FileMode.APPEND`：

```javascript
var stream = new air.FileStream();
stream.open( file, air.FileMode.READ );
```

有三个 `FileStream` 方法用于从文件中读取数据。`FileStream.readUTF()` 和 `FileStream.readUTFBytes()` 方法专门为 UTF 数据调整。如果这是应用程序的数据格式，则直接使用这些方法。对于其他字符集，可以使用 `FileStream.readMultiBytes()` 方法来指定目标。其他字符集以字符串形式指定，例如 `"us-ascii"`。`File` 对象上还有一个便捷属性用于使用系统字符集，即 `File.systemCharset`。

在使用 `FileStream.readUTFBytes()` 和 `FileStream.readMultiBytes()` 的情况下，还需要指定读取的字节数。此大小取决于应用程序的要求。在读取整个文件的情况下，可通过 `FileStream.bytesAvailable` 属性找到读取的字节数：

```javascript
var data = stream.readMultiBytes( stream.bytesAvailable, air.File.systemCharset );
```

一旦文件内容被读取完毕，关闭文件就很重要。此操作将允许应用程序访问该文件：

```javascript
stream.close();
```

尽管 Adobe AIR 提供了相当灵活性，但整个过程相当简洁。这种简洁性是在执行同步数据访问时提供的。无论读取字符数据还是二进制数据，同步文件访问都应保留给较文件使用：

```html
<html>
<head>
<title>Synchronous File Access</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script>
var file = null;
var stream = null;
function doLoad() {
    var data = null;
    file = air.File.applicationStorageDirectory.resolve( "myFile.txt" );
    stream = new air.FileStream();
    stream.open( file, air.FileMode.READ );
    data = stream.readMultiByte( stream.bytesAvailable, air.File.systemCharset );
    stream.close();
    document.getElementById( "editor" ).value = data;
}
</script>
</head>
<body onload="doLoad()">
<textarea id="editor"></textarea>
</body>
</html>
```

### 从文件异步读取文本

#### 问题
你想将大量文本读取到应用程序中。

#### 解决方案
使用异步文件 API 来加载文本，确保在文件加载过程中应用程序执行不会被阻塞。

#### 讨论
包含大量数据的文件应使用 `FileStream.openAsync()` 方法读取。此方法以异步方式打开文件进行读取或写入，不会阻塞用户输入。异步文件操作通过在处理过程中引发事件来实现此目标。其结果是必须在 `FileStream` 对象上创建并注册事件监听器。

异步读取文件的步骤总是相同的：
1. 获取一个 `File` 引用
2. 创建一个 `FileStream` 对象
3. 创建用于处理数据的事件处理程序
4. 为异步操作添加事件监听器
5. 以异步访问方式打开流
6. 关闭文件

读取文本文件的第一步是获取磁盘上资源的引用。可以通过在 `File` 对象上使用适当的属性（如 `File.applicationStorageDirectory`）以编程方式指定路径来建立引用：

```javascript
var file = air.File.applicationStorageDirectory.resolve( "myfile.txt" );
```

`FileStream` 类有一个空构造函数，可以在应用程序中的任何位置实例化。建立的文件引用在打开物理过程中使用：

```javascript
var stream = new air.FileStream();
```

一旦文件被打开并且流中有新的数据可用，`ProgressEvent.PROGRESS` 事件就会被触发。事件对象上的属性有助于确定 `FileStream` 对象有多少数据可用、等待写入等：

```javascript
function doProgress( event ) {
    // 读取当前可用数据
    var data = stream.readMultiByte( stream.bytesAvailable, air.File.systemCharset );
    // 将最新的内容添加到文本区域
    document.getElementById("editor").value += data;
    // 在读取完所有内容后关闭文件
    if( event.bytesLoaded == event.bytesTotal ) {
        stream.close();
    }
}
```

注册事件使用 `addEventListener()`：

```javascript
stream.addEventListener( air.ProgressEvent.PROGRESS, doProgress );
```

以异步方式打开流是通过 `FileStream.openAsync()` 完成的。`FileStream.openAsync()` 方法接受两个参数，分别指定要访问的文件和执行的访问类型：

```javascript
stream.openAsync( file, air.FileMode.READ );
```
```



# Asynchronous File Access

```html
<script type="text/javascript" src="AIRAliases.js"></script>

<script>
var file = null;
var stream = null;

function doLoad()
{
    file = air.File.applicationStorageDirectory.resolve(
        "myFile.txt" );
    stream = new air.FileStream();
    stream.addEventListener( air.ProgressEvent.PROGRESS,
                             doProgress );
    stream.openAsync( file, air.FileMode.READ );
}

function doProgress( event )
{
    var data = stream.readMultiByte( stream.bytesAvailable,
                                     air.File.systemCharset );
    document.getElementById( "editor" ).value += data;
    if( event.bytesLoaded == event.bytesTotal )
    {
        stream.close();
    }
}
</script>
</head>

<body onload="doLoad()">

<textarea id="editor"></textarea>

</body>
</html>
```

## 从XML文件加载数据

### 问题

你希望使用常见的JavaScript技术从本地文件读取XML数据，并且能够操作DOM而不仅仅是字符数据。

### 解决方案

可以使用`XMLHttpRequest`对象读取本地XML文档的数据，并使用`File`对象引用作为URI端点，而非网络地址。

### 讨论

大多数JavaScript库，以及几乎所有面向数据的Ajax应用程序都使用`XMLHttpRequest`对象来加载数据。这是一种常见的无需刷新页面即可从客户端访问数据的方式，是Ajax开发技术的核心。Adobe AIR支持`XMLHttpRequest`对象，可用于数据访问。

`XMLHttpRequest.open()`方法需要三个参数。第一个参数是用于调用的HTTP方法，通常是`GET`或`POST`。第三参数告诉对象是否应该异步发出请求。在AIR应用程序中，挑战在于第二个参数，它告诉对象从哪里获取数据：

`XMLHttpRequest.open( "GET", "myData.xml", true );`

这个URI端点通常指向远程服务器。在在线应用程序中这仍然可行，但由于AIR应用程序也可以离线工作，端点需要指向本地资源。可以不传递远程服务器的端点，而是提供一个`File`引用：

```javascript
var file = air.File.applicationStorageDirectory.resolve(
"myData.xml" );
var xml = new XMLHttpRequest();
xml.onreadystatechange = function()
{
    if( xml.readyState == 4 )
    {
        // Work with data
    }
}
xml.open( "GET", file.url, true );
xml.send( null );
```

此示例的关键区别在于使用了`File.url`属性，`XMLHttpRequest`对象能够理解并使用它来访问相应的数据。使用这种方法可以得到一个传统的DOM，用于遍历和操作文件中的XML数据。此外，这种方法可以与常见的JavaScript库一起使用。

### 已知数据

```xml
<rolodex>
    <contact>
        <first>Kevin</first>
        <last>Hoyt</last>
    </contact>
    ...
</rolodex>
```

### 示例

```html
<html>
<head>
<title>XML File Access</title>
<script type="text/javascript" src="AIRAliases.js">
</script>
<script>
var file = null;
var xml = null;

function doLoad()
{
    file = air.File.applicationResourceDirectory;
    file = file.resolve( "rolodex.xml" );
    xml = new XMLHttpRequest();
    xml.onreadystatechange = function()
    {
        var elem = null;
        var first = null;
        var last = null;
        var rolodex = null;
        if( xml.readyState == 4 )
        {
            rolodex = xml.responseXML.documentElement.getElementsByTagName( "contact" );
            for( var c = 0; c < rolodex.length; c++ )
            {
                first = rolodex[c].getElementsByTagName( "first" )[0].textContent;
                last = rolodex[c].getElementsByTagName( "last" )[0].textContent;
                elem = document.createElement( "div" );
                elem.innerText = first + " " + last;
                document.body.appendChild( elem );
            }
        }
    }
    xml.open( "GET", file.url, true );
    xml.send( null );
}
</script>
</head>
<body onload="doLoad()">
</body>
</html>
```

## 创建临时文件

### 问题

应用程序需要在文件处理期间存储临时信息，并且不能假设有足够的内存来存储这些数据。

### 解决方案

使用`File.createTempFile()`创建临时文件是存储临时信息的理想方式，同时避免了额外的内存开销。

### 讨论

`File`类包含一个静态方法`File.createTempFile()`，可用于创建临时文件。临时文件在操作系统确定的目标位置创建。临时文件还会自动分配一个唯一的名称，以避免与可能存在的其他文件冲突：

```javascript
var temp = air.File.createTempFile();
```

一旦创建了临时文件，就可以像处理已知位置的已知文件一样，使用其他`File`和`FileStream`方法：

```javascript
var stream = new air.FileStream();
stream.open( temp, air.FileMode.WRITE );
stream.writeMultiByte( "Hello", air.File.systemCharset );
stream.close();
```

如果你决定需要保留临时文件以供后续参考，可以事后使用`File.moveTo()`和`File.moveToAsync()`。这两个移动方法都接受两个参数。第一个参数是目标位置的`File`引用。第二个参数是一个布尔值，用于控制是否覆盖任何现有文件。如果第二个参数设置为`false`，并且发生冲突，应用程序会抛出错误：

```javascript
var move = air.File.applicationResourceDirectory.resolve( "temp.txt" );
try
{
    temp.moveTo( move, false );
}
catch( ioe )
{
    alert( "Can't move file:\n" + ioe.message );
}
```

JavaScript的`try/catch`块会接收到一个`IOError`类型的错误对象。`IOError`类有许多可用的属性，可用于进一步评估。前面代码片段中的异常会引发Adobe AIR生成的错误消息：

```html
<html>
<head>
<title>Temporary File</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script>
function doLoad()
{
    var stream = new air.FileStream();
    var temp = air.File.createTempFile();
    var move = air.File.applicationResourceDirectory.resolve( "temp.txt" );
    stream.open( temp, air.FileMode.WRITE );
    stream.writeMultiByte( "Hello", air.File.systemCharset );
    stream.close();
    try
    {
        temp.moveTo( move, false );
    }
    catch( ioe )
    {
        alert( "Can't move file:\n" + ioe.message );
    }
}
</script>
</head>
</body>
```

## 遍历目录

### 问题

应用程序需要在文件处理期间存储临时信息，并且不能假设有足够的内存来存储这些数据。

### 解决方案

使用`File.createTempFile()`创建临时文件是存储临时信息的理想方式，同时避免了额外的内存开销。

### 讨论

`File`类包含一个静态方法`File.createTempFile()`，可用于创建临时文件。临时文件在操作系统确定的目标位置创建。临时文件还会自动分配一个唯一的名称，以避免与可能存在的其他文件冲突：

```javascript
var temp = air.File.createTempFile();
```

一旦创建了临时文件，就可以像处理已知位置的已知文件一样，使用其他`File`和`FileStream`方法：

```javascript
var stream = new air.FileStream();
stream.open( temp, air.FileMode.WRITE );
stream.writeMultiByte( "Hello", air.File.systemCharset );
stream.close();
```

如果你决定需要保留临时文件以供后续参考，可以事后使用`File.moveTo()`和`File.moveToAsync()`。这两个移动方法都接受两个参数。第一个参数是目标位置的`File`引用。第二个参数是一个布尔值，用于控制是否覆盖任何现有文件。如果第二个参数设置为`false`，并且发生冲突，应用程序会抛出错误：

```javascript
var move = air.File.applicationResourceDirectory.resolve( "temp.txt" );
try
{
    temp.moveTo( move, false );
}
catch( ioe )
{
    alert( "Can't move file:\n" + ioe.message );
}
```

JavaScript的`try/catch`块会接收到一个`IOError`类型的错误对象。`IOError`类有许多可用的属性，可用于进一步评估。前面代码片段中的异常会引发Adobe AIR生成的错误消息：

```html
<html>
<head>
<title>Temporary File</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script>
function doLoad()
{
    var stream = new air.FileStream();
    var temp = air.File.createTempFile();
    var move = air.File.applicationResourceDirectory.resolve( "temp.txt" );
    stream.open( temp, air.FileMode.WRITE );
    stream.writeMultiByte( "Hello", air.File.systemCharset );
    stream.close();
    try
    {
        temp.moveTo( move, false );
    }
    catch( ioe )
    {
        alert( "Can't move file:\n" + ioe.message );
    }
}
</script>
</head>
</body>
```

## 文件选择

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件是存储临时信息。

### 讨论

`File`类包含一个静态方法`File.createTempFile()`，可用于创建临时文件。临时文件在操作系统确定的目标位置创建。临时文件还会自动分配一个唯一的名称，以避免与可能存在的其他文件冲突：

```javascript
var temp = air.File.createTempFile();
```

一旦创建了临时文件，就可以像处理已知位置的已知文件一样，使用其他`File`和`FileStream`方法：

```javascript
var stream = new air.FileStream();
stream.open( temp, air.FileMode.WRITE );
stream.writeMultiByte( "Hello", air.File.systemCharset );
stream.close();
```

如果你决定需要保留临时文件以供后续参考，可以事后使用`File.moveTo()`和`File.moveToAsync()`。这两个移动方法都接受两个参数。第一个参数是目标位置的`File`引用。第二个参数是一个布尔值，用于控制是否覆盖任何现有文件。如果第二个参数设置为`false`，并且发生冲突，应用程序会抛出错误：

```javascript
var move = air.File.applicationResourceDirectory.resolve( "temp.txt" );
try
{
    temp.moveTo( move, false );
}
catch( ioe )
{
    alert( "Can't move file:\n" + ioe.message );
}
```

JavaScript的`try/catch`块会接收到一个`IOError`类型的错误对象。`IOError`类有许多可用的属性，可用于进一步评估。前面代码片段中的异常会引发Adobe AIR生成的错误消息：

```html
<html
<head>
<title>Temporary File</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script>
function doLoad()
{
    var stream = new air.FileStream();
    var temp = air.File.createTempFile();
    var move = air.File.applicationResourceDirectory.resolve( "temp.txt" );
    stream.open( temp, air.FileMode.WRITE );
    stream.writeMultiByte( "Hello", air.File.systemCharset );
    stream.close();
    try
    {
        temp.moveTo( move, false );
    }
    catch( ioe )
    {
        alert( "Can't move file:\n" + ioe.message );
    }
}
</script>
</head>
</body>
```

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论 

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论 

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论 

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论 

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论 

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论 

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论 

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论 

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论 

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论 

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论 

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建临时文件。

### 讨论 

`File`类包含一个静态方法`File.createTempFile()`。

## 遍历内容

### 问题

应用程序需要遍历目录。

### 解决方案

使用`File.createTempFile()`创建 文件。

###   

`

`

包含一个静态方法`File.create.FileFile。

。

  





###





需要遍历。。



  解决方案

使用`File.createTempFile()` 临时。。

###    

`File`类包含一个静态方法`File.createTempFile()`。

[/ 




```
var file = null;

function doLoad()
{
    file = air.File.documentsDirectory;
    file.addEventListener( air.Event.SELECT, doSelect );
    document.getElementById( "btnBrowse" ).
    addEventListener( "click", doBrowse );
}

function doBrowse()
{
    var filters = new window.runtime.Array();
    filters.push( new air.FileFilter( "Image Files", "*.jpg" ) );
    file.browseForOpen( "选择照片", filters );
}

function doSelect( event )
{
    var elem = document.createElement( "div" );
    elem.innerText = file.nativePath;
    document.body.appendChild( elem );
}
```

</script>

</head>

<body onload="doLoad()">

<input id="btnBrowse" type="button" value="浏览" />

</</body>>

</html>

```

### 浏览多个文件

#### 问题

应用程序需要提示用户使用原生对话框从本地系统中选择多个文件。

#### 解决方案
使用`File.browseForOpenMultiple()` API 向用户显示一个对话框，允许他们选择多个文件。

#### 讨论
使用`File`类打开单个文件与打开多个文件的方式基本相同。在允许用户选择多个文件的情况下，合适的方法是`File.browseForOpenMultiple()`。`File.browseForOpenMultiple()`方法接受的两个参数与`File.browseForOpen()`方法相同：一个用于对话框标题的字符串，以及一个`FileFilter`对象数组。

一旦用户从对话框中选择了文件，就会广播`FileListEvent.SELECT_MULTIPLE` 事件。发送给处理程序的事件对象将是`FileListEvent`类型。`FileListEvent`类包含一个 "files"属性，该属性将是一个`File`对象数组，代表用户选择的文件：

```javascript
var file = air.File.documentsDirectory;
file.addEventListener( air.FileListEvent.SELECT_MULTIPLE,
doSelect );

function doSelect( event )
{
    for( var f = 0; f < event.files.length; f++ )
    {
        ...
    }
}
```

以下是完整代码：

```html
<html>
<head>
<title>浏览多个文件</title>
<script type="text/javascript" src="AIRAliases.js">
</script>
<script>
var file = null;
function doLoad()
{
    file = air.File.documentsDirectory;
    file.addEventListener( air.FileListEvent.SELECT_MULTIPLE,
                           doSelect );
    document.getElementById( "btnBrowse" ).
addEventListener( "click", doBrowse );
}
function doBrowse()
{
    var filters = new window.runtime.Array();
    filters.push( new air.FileFilter( "Image Files", "*.jpg" ) );
    file.browseForOpenMultiple( "选择照片", filters );
}
function doSelect( event )
{
    var elem = null;
    var name = null;
    var size = null;
    for( var f = 0; f < event.files.length; f++ )
    {
        name = event.files[f].name;
        size = Math.ceil( event.files[f].size / 1000 );
        elem = document.createElement( "div" );
        elem.innerText = name + " (" + size + " KB)";
        document.body.appendChild( elem );
    }
}
</script>
</head>
<body onload="doLoad()">
<input id="btnBrowse" type="button" value="浏览" />
</body>
</html>
```

98 | 第四章：AIR 小型食谱

### 浏览目录

#### 问题

应用程序需求要求你允许用户选择一个用于存储数据的目录。

#### 解决方案
使用`File.browseForDirectory()` API 提示用户选择目录。

#### 讨论
`File.browseForDirectory()` API 创建一个原生对话框，允许用户选择目录。该方法接受一个必需的字符串参数，该参数将用于向用户提供有关所选目录用途的额外信息。

当目录选择完成后，Adobe AIR 将在发起应用程序中触发一个事件。为了捕获该事件，应用程序必须首先注册一个事件监听器。触发的事件是`Event.SELECT`，一个事件对象将被传递给处理程序：

```
var file = air.File.documentsDirectory;
file.addEventListener( air.Event.SELECT, doSelect );
file.browseForDirectory( "Where do you want to store your photos?" );
function doSelect( event )
{
    alert( file.nativePath );
}
```

发送到处理程序的事件对象的一个有用属性是`target`属性，它包含对原始对象的引用。对话框操作返回任何内容赋值给`File`对象，因为原始对象现在持有对用户选目录的引用。为此，拥有一个全局引用指向`File`对象，重用它，可能是有益的：

```
<html>
<head>
<title>Select Directory</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script>
var file = null;
function doLoad()
{
    file = air.File.documentsDirectory;
    file.addEventListener( air.Event.SELECT, doSelect );
    document.getElementById( "btnBrowse" ).
    addEventListener( "click", doBrowse );
}
function doBrowse()
{
    file.browseForDirectory( "Where do you want to put your photos?" );
}
function doSelect()
{
    var elem = document.createElement( "div" );
    elem.innerText = file.nativePath;
    document.body.appendChild( elem );
}
</script>
</head>
<body onload="doLoad()">
<input id="btnBrowse" type="button" value="Browse" />
</body>
</html>
```

### 服务和监控

#### 监控与 HTTP 服务器连接性

#### 问题
应用程序需要监控并确定是否访问特定的 HTTP 服务器。

#### 解决方案
使用`URLMonitor`类检测 HTTP/S端点的网络变化。

#### 讨论
服务监控类通过事件通知和轮询端点来工作。服务监控不是 Adobe AIR运行时直接部分，在使用前添加。用于服务监控的类包含在`servicemonitor.swf`文件中，可以在 AIR SDK的目录中找到。此文件应复制到应用程序文件夹中，可以通过`<script>`标签来包含。`servicemonitor.swf`文件也需要在打包的 AIR应用程序中。

```
<script src="servicemonitor.swf"></script>
```

`URLMonitor`类在构造函数中接受一个参数，即`URLRequest`类的实例。`URLRequest`构造函数接受一个字符串，表示查询端点。`URLRequest`类还包含如何查询端点（即`GET`、`POST`）以及传递给服务器的任何额外数据：

```
var request = air.URLRequest( "http://www.adobe.com" );
var monitor = new window.runtime.air.net.URLMonitor( request );
```

`URLMonitor`类在网络变化时触发`StatusEvent.STATUS` 事件。一旦事件程序注册完毕，就可以`URLMonitor`实例监视网络变化：

```
monitor.addEventListener( air.StatusEvent.STATUS, doStatus );
monitor.start();
```

在网络变化作为事件传播后，可以在原始`URLMonitor`实例上使用`URLMonitor.available`属性来检查连接。`URLMonitor.available`属性返回一个布尔值，反映网络状态。由于需要查询原始`URLMonitor`实例获取可用性，该对象应在跨应用程序访问范围内声明：

```
<html>
<head>
<title>HTTP Monitor</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script src="servicemonitor.swf"></script>
<script>
var monitor = null;
function doLoad()
{
    var request = new air.URLRequest( "http://www.adobe.com" );
    monitor = new window.runtime.air.net.URLMonitor( request );
    monitor.addEventListener( air.StatusEvent.STATUS, doStatus );
    monitor.start();
}
function doStatus( event )
{
    var elem = document.createElement( "div" );
    elem.innerText = monitor.available;
    document.body.appendChild( elem );
}
</script>
</head>
<body onload="doLoad()">
</body>
</html>
```

#### 监控与 Jabber 服务器连接性

#### 问题
需要一个Jabber聊天客户端在用户界面反映网络状态，但端点是特定端口上的Jabber服务器，而不是HTTP/S。

#### 解决方案
使用`SocketMonitor`类检测针对TCP/IP接字端点的网络变化。

#### 讨论
服务监控API并非直接内置于Adobe AIR，在使用前添加。Adobe AIR SDK包含的`servicemonitor.swf`文件必须作为应用程序资源，并通过`<script>`标签包含：

```
<script src="servicemonitor.swf"></script>
```

`SocketMonitor`类在构造函数中接受两个参数：一个表示主机端点的字符串，以及服务器监听的端口：

```
var host = "im.mydomain.com";
var port = 5220;
var monitor = new window.runtime.air.net.SocketMonitor( host, port );
```

`SocketMonitor`类在网络变化时触发`StatusEvent.STATUS` 事件。一旦事件程序注册完毕，调用`SocketMonitor.start()`方法将监视网络变化：

```
monitor.addEventListener( air.StatusEvent.STATUS, doStatus );
monitor.start();
```

在网络变化作为事件传播后，可以在原始`SocketMonitor`实例上使用`SocketMonitor.available`属性检查连接是否存在。`SocketMonitor.available`属性返回一个布尔值，反映网络状态。作为最佳实践，`SocketMonitor`对象应在跨应用程序访问范围内声明，并在事件处理期间直接引用：

```
<html>
<head>
<title>Socket Monitor</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script src="servicemonitor.swf"></script>
<script>
var monitor = null;
function doLoad()
{
    monitor = new window.runtime.air.net.SocketMonitor( "im.mydomain.com", 5220 );
    monitor.addEventListener( air.StatusEvent.STATUS, doStatus );
    monitor.start();
}
function doStatus( event )
{
    var elem = document.createElement( "div" );
    elem.innerText = monitor.available;
    document.body.appendChild( elem );
}
</script>
</head>
<body onload="doLoad()">
</body>
</html>
```

## 在线/离线

### 缓存资源以供离线使用

#### 问题
你希望从URL加载资源并将其存储，以供离线使用。

#### 解决方案
使用文件I/O API 将请求的资源保存到应用程序的存储区，并在后续请求中读取该文件。

#### 讨论
在此示例中，我们将加载一个位于已知URL的XML文件。一旦数据加载完成，它将被保存到本地磁盘，后续对该文档的请求将从本地磁盘加载，而不是从远程位置加载。

首先，我们将使用`XMLHttpRequest`对象从远程位置加载XML数据。`XMLHttpRequest.open()`方法接受三个参数。第一个参数是正在进行的HTTP请求的方法。第二个参数是正在加载的数据位置的URI。第三个参数是一个布尔值，指定操作是否为异步。

```
var xml = new XMLHttpRequest();
xml.open( "GET", "http://www.foo.com/data.xml", true );
xml.send( null );
```


由于我们是异步加载数据，因此需要为响应创建一个处理程序，该处理程序会在服务器数据加载完成后被调用。这个处理程序需要在调用 `send` 方法之前添加。在此处理程序中，我们将 `XMLHttpRequest` 实例的 `responseText` 属性中的数据保存到本地文件系统上的已知位置，以便后续请求时检索。关于在本地系统上读写文本的内容，本书其他地方有介绍，因此这里不详细说明：

```javascript
xml.onreadystatechange = function() 
{
    if( xml.readyState == 4 ) // 请求已完成
    {
        // 将数据写入本地系统
        var file = air.File.applicationStorageDirectory.resolve("data.xml");
        var fileStream = new air.FileStream();
        fileStream.open( file, air.FileMode.WRITE );
        fileStream.writeMultiByte( xml.responseText , air.File.systemCharset );
        fileStream.close();
    }
}
```

在每次请求数据之前，我们需要检查 `data.xml` 文件是否存在。如果存在，我们就不需要使用 `XMLHttpRequest` 对象来加载文件，而是可以使用 `File` API 从磁盘加载它。这允许我们即使在用户当前不在线的情况下也能加载数据：

```javascript
var data = null;
var file = air.File.applicationStorageDirectory.resolve("data.xml");
```

```javascript
if( file.exists )
{
    var fileStream = new air.FileStream();
    fileStream.open( file, air.FileMode.READ );
    data = fileStream.readMultiByte( fileStream.bytesAvailable, air.File.systemCharset );
    fileStream.close();
}
else
{
    // 通过 XMLHttpRequest 读取数据并将其
    // 写入文件系统
}
```

以下是完整示例：

```html
<html
<head>
    <title>为离线使用缓存资源</title>
    <script src="AIRAliases.js"></script>
    <script>
        var file = air.File.applicationStorageDirectory.resolve("data.xml");
        function onLoad()
        {
            if( file.exists )
            {
                var fileStream = new air.FileStream();
                fileStream.open( file, air.FileMode.READ );
                document.getElementById( "dataText" ).value =
                    fileStream.readMultiByte(
                        fileStream.bytesAvailable,
                        air.File.systemCharset );
                fileStream.close();
            }
            else
            {
                var xml = new XMLHttpRequest();
                xml.open( "GET", "http://www.foo.com/data.xml", true );
                xml.onreadystatechange = function()
                {
                    if( xml.readyState == 4 ) // 请求已完成
                    {
                        var file = air.File.applicationStorageDirectory.resolve("data.xml");
                        var fileStream = new air.FileStream();
                        fileStream.open( file, air.FileMode.WRITE );
                        fileStream.writeMultiByte( xml.responseText , air.File.systemCharset );
                        fileStream.close();
                        document.getElementById( "dataText" ).value = xml.responseText;
                    }
                }
                xml.send( null );
            }
        }
    </script>
</head>
<body onLoad="onLoad()">
    <textarea id="dataText"></textarea>
</</body>>
</html>
```

## 拖放

### 在 HTML 中使用拖放

#### 问题
您希望允许用户将文件、图像、文本和其他数据类型拖入和拖出基于 HTML 的 AIR 应用程序。

#### 解决方案
通过在 JavaScript 中使用 Adobe AIR 的拖放实现，开发人员可以响应发生在 HTML DOM 对象上的拖放操作。

#### 提示
Adobe AIR 对拖放的支持基于 WebKit 的实现。您可以在以下网址找到更多信息：http://developer.apple.com/documentation/AppleApplications/Conceptual/SafariJSProgTopics/Tasks/DragAndDrop.html`。

#### 讨论
为桌面端开发的好处之一是为用户提供与多个应用程序交互时更集成的体验。最常用的手势之一是在应用程序与桌面之间以及应用程序之间拖放文件、数据和其他元素。

本示例将演示如何接受拖入应用程序的文本，并支持将文本拖出。它还将向您展示如何修改拖放效果，以向用户展示他可以对正在拖动的元素执行何种类型的拖放操作。

在 HTML 中使用拖放操作时，需要考虑两个重要的流程。首先，我们将研究希望允许被用户拖动的 HTML 元素的流程：

1. 元素指定它可用于拖放操作。
2. 用户选择该项目并开始拖动它。
3. 元素收到 `ondragstart` 事件，并设置将要传输的数据，同时指定支持哪些拖放操作。
4. 在元素被拖动时，元素会持续收到 `ondrag` 事件。
5. 用户放下正在拖动的项目，发起拖动的元素会收到 `ondragend` 事件。

希望接收拖放操作的 HTML 元素的典型流程如下：

1. 用户将项目拖动到监听拖放事件的元素上方。
2. 元素收到 `ondragenter` 事件，并指定哪些拖放操作是可用的。
3. 当项目被拖动到元素上方时，元素会持续收到 `ondragover` 事件。
4. 用户放下项目，接收元素会收到 `ondrop` 事件。
5. 如果用户将拖动的项目移出监听元素的边界，它会收到 `ondragleave` 事件。

默认情况下，用户可以拖动文本元素和 URL。要禁用此功能，请使用 `-khtml-user-drag:none` 样式。要覆盖默认指定的数据类型，请使用 `-khtml-user-drag:element` 样式，并按前述方式为拖动事件指定监听器。

要操作应用程序之间传输的数据，请使用附加在拖放操作期间分发的事件上的 `dataTransfer` 对象。`dataTransfer` 对象有两个方法：`getData` 和 `setData`。`setData` 方法接受两个参数：MIME 类型和符合该类型的数据字符串。`setData` 方法可以多次调用，允许您存储多种数据类型。例如，如果您想指定一个 `"text/plain"` 类型和一个 `"text/uri-list"` 类型，您可以这样做：

```javascript
function dropStartListener( event )
{
    event.dataTransfer.setData( "text/plain", "Adobe" );
    event.dataTransfer.setData( "text/uri-list", "http://www.adobe.com" );
}
```

如果对正在拖动的元素上已存在的 MIME 类型调用 `setData`，该数据将被覆盖。从正在拖动的元素中检索数据只能在 `ondrop` 事件处理程序中进行。`getData` 方法接受一个 MIME 类型作为其唯一参数，并返回该 MIME 类型在正在拖动的元素上的值（如果存在）。例如：

```javascript
function dropListener( event )
{
    alert( event.dataTransfer.getData( "text/plain" ) );
// Adobe
}
```

当用户将项目从一个应用程序拖到另一个应用程序，或从应用程序中的一个位置拖到另一个位置时，您可能希望向用户指示哪些操作（复制、链接或移动）是可用的。通过使用 `dataTransfer` 对象的 `effectAllowed` 和 `dropEffect` 属性，您可以指定允许哪些操作。系统随后会使用应用程序来确定用户在拖放操作期间可以执行哪些操作。这些属性的可用值列表可以通过阅读上述参考文档来确定。

开始拖动时，`effectAllowed` 属性告诉系统源元素支持哪些操作。`dropEffect` 属性指定接收拖放事件的当前目标支持的操作。系统随后会根据源元素和目标元素都支持的效果信息向用户显示。

## 提示
Adobe AIR 对拖放的支持基于 WebKit 的实现。您可以在以下网址找到更多信息：http://developer.apple.com/documentation/AppleApplications/Conceptual/SafariJSProgTopics/Tasks/DragAndDrop.html`。

## 嵌入式数据库
由于我们是异步加载数据，因此需要为响应创建一个处理程序，该处理程序会在服务器数据加载完成后被调用。这个处理程序需要在调用 `send` 方法之前添加。在此处理程序中，我们将 `XMLHttpRequest` 实例的 `responseText` 属性中的数据保存到本地文件系统上的已知位置，以便后续请求时检索。关于在本地系统上读写文本的内容，本书其他地方有介绍，因此这里不详细说明：

```javascript
xml.onreadystatechange = function() 
{
    if( xml.readyState == 4 ) // 请求已完成
    {
        // 将数据写入本地系统
        var file = air.File.applicationStorageDirectory.resolve("data.xml");
        var fileStream = new air.FileStream();
        fileStream.open( file, air.FileMode.WRITE );
        fileStream.writeMultiByte( xml.responseText , air.File.systemCharset );
        fileStream.close();
    }
}
```

在每次请求数据之前，我们需要检查 `data.xml` 文件是否存在。如果存在，我们就不需要使用 `XMLHttpRequest` 对象来加载文件，而是可以使用 `File` API 从磁盘加载它。这允许我们即使在用户当前不在线的情况下也能加载数据：

```javascript
var data = null;
var file = air.File.applicationStorageDirectory.resolve("data.xml");
```

```javascript
if( file.exists )
{
    var fileStream = new air.FileStream();
    fileStream.open( file, air.FileMode.READ );
    data = fileStream.readMultiByte( fileStream.bytesAvailable, air.File.systemCharset );
    fileStream.close();
}
else
{
    // 通过 XMLHttpRequest 读取数据并将其
    // 写入文件系统
}
```

以下是完整示例：

```html
<html
<head>
    <title>为离线使用缓存资源</title>
    <script src="AIRAliases.js"></script>
    <script>
        var file = air.File.applicationStorageDirectory.resolve("data.xml");
        function onLoad()
        {
            if( file.exists )
            {
                var fileStream = new air.FileStream();
                fileStream.open( file, air.FileMode.READ );
                document.getElementById( "dataText" ).value =
                    fileStream.readMultiByte(
                        fileStream.bytesAvailable,
                        air.File.systemCharset );
                fileStream.close();
            }
            else
            {
                var xml = new XMLHttpRequest();
                xml.open( "GET", "http://www.foo.com/data.xml", true );
                xml.onreadystatechange = function()
                {
                    if( xml.readyState == 4 ) // 请求已完成
                    {
                        var file = air.File.applicationStorageDirectory.resolve("data.xml");
                        var fileStream = new air.FileStream();
                        fileStream.open( file, air.FileMode.WRITE );
                        fileStream.writeMultiByte( xml.responseText , air.File.systemCharset );
                        fileStream.close();
                        document.getElementById( "dataText" ).value = xml.responseText;
                    }
                }
                xml.send( null );
            }
        }
    </script>
</head>
<body onLoad="onLoad()">
    <textarea id="dataText"></textarea>
</</body>>
</html>
```

## 提示
开始拖动时，`effectAllowed` 属性告诉系统源元素支持哪些操作。`dropEffect` 属性指定接收拖放事件的当前目标支持的操作。系统随后会根据源元素和目标元素都支持的效果信息向用户显示。

## 提示
Adobe AIR 对拖放的支持基于 WebKit 的实现。您可以在以下网址找到更多信息：http://developer.apple.com/documentation/AppleApplications/Conceptual/SafariJSProgTopics/Tasks/DragAndDrop.html`。

## 嵌入式数据库
（此处省略重复的 HTML 示例逻辑描述，直接保留核心代码结构）

```javascript
var db = new air.SQLConnection();

function doDbOpen( event )
{
    alert( "您现在连接到数据库。" );
}

function doLoad()
{
    var file = air.File.applicationStorageDirectory.resolve("data.xml");
    db.addEventListener( air.SQLEvent.OPEN, doDbOpen );
    db.open( file, true );
}

function doUnload()
{
    db.close();
}
```

### 创建数据库表

#### 问题
应用程序有一个为数据存储提供的特定模式。

#### 解决方案
可以使用 `SQLStatement` 类和 `SQL92` 创建数据库模式。

#### 讨论
一旦创建了数据库文件并建立了与数据库的连接，下一个可能的步骤将是创建任何所需的模式。这可以使用 `SQL92` 结合 `SQLStatement` 类来完成。

```javascript
var stmt = new air.SQLStatement();
stmt.addEventListener( air.SQLErrorEvent.ERROR, doStmtError );
stmt.addEventListener( air.SQLEvent.RESULT, doStmtResult );
```



```
为了执行 SQL 语句，必须建立一个要执行的 `SQLConnection` 实例。`SQLConnection` 实例可以分配给 `SQLStatement.sqlConnection` 属性。然后将 `SQLStatement.text` 属性分配给需要执行的任何 SQL。最后，调用 `SQLStatement.execute()` 方法：

```javascript
stmt.sqlConnection = db;
stmt.text = "CREATE TABLE IF NOT EXISTS contact ( " +
    "id INTEGER PRIMARY KEY AUTOINCREMENT, " +
    "first TEXT, " +
    "last TEXT )";
stmt.execute();
```

在这个例子中，一个 `CREATE TABLE` 语句已应用于数据库。其他类型的 SQL 语句，如 `SELECT`、`INSERT`、`UPDATE` 和 `DELETE`，也以相同的方式执行。`SQLStatement.execute()` 方法可以接受两个可选参数：要预取的行数，以及一个用于处理事件的响应者对象。

预取选项默认为 -1，表示应返回所有行。响应者对象可以是一个自定义对象，旨在处理执行期间发生的任何状态或结果事件。在这种情况下，默认响应者为 `null`，因为事件处理程序已直接在 `SQLStatement` 对象上注册：

```html
<html>
<head>
<title>创建数据库表</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script>
var db = null;
var stmt = null;
function doDbOpen( event )
{
    stmt = new air.SQLStatement();
    stmt.addEventListener( air.SQLErrorEvent.ERROR, doStmtError );
    stmt.addEventListener( air.SQLEvent.RESULT, doStmtResult );
    stmt.sqlConnection = db;
    stmt.text = "CREATE TABLE IF NOT EXISTS contact ( " +
                "id INTEGER PRIMARY KEY AUTOINCREMENT, " +
                "first TEXT, " +
                "last TEXT )";
    stmt.execute();
}
</script>
</html>
```

### 在数据库中存储数据

#### 问题
一个应用程序需要将用户提供的数据存储在磁盘上的关系型数据库中。

#### 解决方案
可以使用 `SQLStatement` 类来创建和执行 SQL92 `INSERT` 语句。

#### 讨论
给定一个具有适当模式（schema）的可用数据库文件，可以使用 `SQLStatement` 对象执行 SQL92 语句。同一个 `SQLStatement` 对象可以被重用来执行多个语句。在重用同一个 `SQLStatement` 时，区分刚刚执行的是哪种类型的语句非常重要。有多种方法可以用来监听不同的操作。

```javascript
function doSave()
{
    var first = document.getElementById( "txtFirst" ).value;
    var last = document.getElementById( "txtLast" ).value;
    stmt.text = "INSERT INTO contact VALUES ( " +
        "NULL, " +
        "'" + first + "', " +
        "'" + last + "' )";
    stmt.execute();
}
```

一种方法是为即将执行的不同语句分配不同的事件处理程序。（别忘了移除旧的处理程序。）另一种方法是指定针对特定语句创建的不同响应对象。本示例中使用的方法是一个基本的状态机，它跟踪刚刚执行的是哪种类型的语句：

```javascript
var NONE = -1;
var CREATE_SCHEMA = 0;
var INSERT_DATA = 1;
var state = NONE;
var stmt = new air.SQLStatement();
// 其他数据库创建和配置
function doSave()
{
    var first = document.getElementById( "txtFirst" ).value;
    var last = document.getElementById( "txtLast" ).value;
    stmt.text = "INSERT INTO contact VALUES ( " +
        "NULL, " +
        "'" + first + "', " +
        "'" + last + "' )";
    // 跟踪状态
    state = INSERT_DATA;
    stmt.execute();
}
```

在成功执行数据库语句后，将触发 `SQLResultEvent.RESULT` 事件。如果发生错误，则会引发 `SQLStatusEvent.STATUS` 事件。通过跟踪状态，设计用于处理结果的方法可以确定要采取的适当操作。在插入新数据的情况下，这可能是通知用户和更新用户界面：

```html
<html>
<head>
<title>存储数据库数据</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script>
var db = null;
var stmt = null;
var NONE = -1;
var CREATE_SCHEMA = 0;
var INSERT_DATA = 1;
var state = NONE;
function doDbOpen( event )
{
    stmt = new air.SQLStatement();
    stmt.addEventListener( air.SQLErrorEvent.ERROR, doStmtError );
    stmt.addEventListener( air.SQLEvent.RESULT, doStmtResult );
    stmt.sqlConnection = db;
    stmt.text = "CREATE TABLE IF NOT EXISTS contact ( " +
                "id INTEGER PRIMARY KEY AUTOINCREMENT, " +
                "first TEXT, " +
                "last TEXT );";
    state = CREATE_SCHEMA;
    stmt.execute();
}
function doLoad()
{
    var file = air.File.applicationResource.resolve( "crm.db" );
    db = new air.SQLConnection();
    db.addEventListener( air.SQLEvent.OPEN, doDbOpen );
    db.open( file, true );
}
document.getElementById( "btnSave" ).addEventListener( "click", doSave );
function doSave()
{
    var first = document.getElementById( "txtFirst" ).value;
    var last = document.getElementById( "txtLast" ).value;
    stmt.text = "INSERT INTO contact VALUES ( " +
                "NULL, " +
                "'" + first + "', " +
                "'" + last + "' )";
    state = INSERT_DATA;
    stmt.execute();
}
function doStmtResult( event )
{
    switch( state )
    {
        case CREATE_SCHEMA:
            alert( "数据库表已创建。" );
            state = NONE;
            break;
        case INSERT_DATA:
            document.getElementById( "txtFirst" ).value = "";
            document.getElementById( "txtLast" ).value = "";
            alert( "新记录已存储。" );
    }
}
function doStmtError( event )
{
    alert( "语句时出现问题：\n" + event.error.message );
}
function doUnload()
{
    db.close();
}
</script>
</head>
<body onload="doLoad()" onun="doUnload()">
<div>名：<input id="txtFirst" type="text" /></div>
<div>姓：<input id="txtLast" type="text" /></div>
<div><input id="btnSave" type="button" value="保存" /></div>
</body>
</html>
```

### 访问数据库数据

#### 问题
你需要从嵌入式数据库生成表格。

#### 解决方案
可以使用 SQL92 和 `SQLStatement` 类来查询数据。

#### 讨论
可以使用现有数据库的 `SQLStatement` 对象来运行 `SELECT` 语句。成功执行 `SELECT` 语句会调用已注册的 `SQLResultEvent.RESULT` 事件处理程序。该事件程序将获取一个包含数据的 `SQLResult` 对象：

```javascript
function doStmtResult( event )
{
    var elem = null;
    var results = stmt.getResult();
    if( results.data != null )
    {
        for( var c = 0; c < results.data.length; c++ )
        {
            elem = document.createElement( "div" );
            elem.innerText = results.data[c].first + " " + results.data[c].last;
            document.body.appendChild( elem );
        }
    }
}
```

**提示**
此代码片段省略了其他章节中介绍的大量状态管理、事件注册和数据库连接。请查看那些内容，或本节末尾的示例，以完整了解主题。

要获取结果数据，需调用 `SQLStatement.getResult()`，它返回一个 `SQLResult` 对象。`SQLResult.data` 属性是结果（如果有的话）数组（`Array`）。`SQLResult.data` 数组将其属性与查询中使用的列名匹配的 `Object` 实例。可以使用此数组来迭代的结果。

如果被查询的数据库表没有数据，或者语句返回任何数据，`SQLResult.data` 属性将为 `null`：

```html
<html>
<head>
<title>访问数据库数据</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script>
var db = null;
var stmt = null;
var NONE = -1;
var CREATE_SCHEMA = 0;
var SELECT_DATA = 1;
var state = NONE;
function doDbOpen( event )
{
    stmt = new air.SQLStatement();
    stmt.addEventListener( air.SQLErrorEvent.ERROR, doStmtError );
    stmt.addEventListener( air.SQLResultEvent.RESULT, doStmtResult );
    stmt.sqlConnection = db;
    stmt.text = "CREATE TABLE IF NOT EXISTS contact ( " +
                "id INTEGER PRIMARY KEY AUTOINCREMENT, " +
                "first TEXT, " +
                "last TEXT )";
    state = CREATE_SCHEMA;
    stmt.execute();
}
function doLoad()
{
    var file = air.File.applicationResourceDirectory.resolve( "crm.db" );
    db = new air.SQLConnection();
    db.addEventListener( air.SQLEvent.OPEN, doDbOpen );
    db.open( file, true );
}
function doStmtResult( event )
{
    var elem = null;
    var result = null;
    switch( state )
    {
        case CREATE_SCHEMA:
            stmt.text = "SELECT * FROM contact";
            state = SELECT_DATA;
            stmt.execute();
            break;
        case SELECT_DATA:
            result = stmt.getResult();
            if( result.data != null )
            {
                for( var c = 0; c < result.data.length; c++ )
                {
                    elem = document.createElement( "div" );
                    elem.innerText = result.data[c].first + " " + result.data[c].last;
                    document.body.appendChild( elem );
                }
            }
            state = NONE;
            break;
        default:
            state = NONE;
            break;
    }
}
function doStmtError( event )
{
    alert( "语句时出现问题：\n" + event.error.message );
}
function doUnload()
{
    db.close();
}
</script>
</head>
<body onload="doLoad()" onunload="doUnload()">
<div id="results"></div>
</body>
</html>
```


javascript
function doStmtError(event) {
    alert("执行语句时出现问题：\n" + event.error.message);
}

function doUnload() {
    db.close();
}
</script>
</head>
<body onload="doLoad()" onunload="doUnload()">
</body>
</html
```

## 命令行参数

### 捕获命令行参数

**问题**

你需要捕获发送到应用程序的命令行参数——无论是在应用程序启动时，还是在应用程序运行期间。

**解决方案**

注册`InvokeEvent` 事件，并捕获传递到应用程序的命令行参数。

**讨论**

每当应用程序启动时，或者在应用程序运行期间从命令行调用该应用程序时，都会广播一个`InvokeEvent`。该事件的事件处理函数会接收到有关事件的信息，包括通过命令行传递给应用程序的任何参数。

你应该在应用程序初始化阶段注册`InvokeEvent`，以确保的应用程序最初启动时能够捕获该事件。

你可以像这样从 shell 单例中注册该事件：

```javascript
function init()

{
    air.Shell.shell.addEventListener(air.InvokeEvent.INVOKE,
                                     onInvoke);
}
```

这会将`onInvoke`函数注册为`InvokeEvent`的处理函数。该处理函数会接收到一个`InvokeEvent`对象实例，该实例包含一个名为`arguments`的属性，它是一个字符串数组，包含传递给应用程序的所有参数：

```javascript
function onInvoke(event)

{
    air.trace("onInvoke : " + event.arguments);
}
```

通过 ADL 测试应用程序时，你可以使用--` 参数来传递命令行参数。例如：

```bash
adl InvokeExample.xml -- foo "bim bam"
```

这将向应用程序传递两个参数 "foo" 和 "bim bam"。

完整示例如下；它监听`InvokeEvent` 事件，并将结果输出到包含的 `textarea` HTML 控件以及通过`air.trace()` 输出到命令行：

```html
<html>

<head>

    <script src="AIRAliases.js" />

    <script type="text/javascript">

        function onInvoke(event)

        {
            air.trace("onInvoke : " + event.arguments);
            var field = document.getElementById("outputField");
            field.value += "Invoke : " + event.arguments + "\n";
        }

        function init()

        {
            air.Shell.shell.addEventListener(air.InvokeEvent.INVOKE, onInvoke);
        }

    </script>

</head>

<body onload="init()">

    <textarea rows="8" cols="40" id="outputfield">

    </textarea>

</body>

</html>
```

## 网络

### 在套接字上通信

**问题**

你希望使用 Adobe AIR 未直接支持的协议（例如，与 FTP 服务器通信）与服务器进行通信。

**解决方案**

使用 AIR API 中的`Socket`类向服务器发送二进制或文本数据，并注册事件以在收到服务器数据时得到通知。

**讨论**

当使用 Adobe AIR 未直接支持的协议进行通信时，你可能需要使用 Socket API。`Socket` API 是一个异步 API，允许你向一个持久的套接字端点发送数据，并实时接收来自该端点的数据。你不需要为发送到同一端点的每组数据创建一个新的`Socket`实例。在整个对话过程中，连接可以保持活动状态。使用 Socket API 的典型流程如下：

1. 创建到端点的连接
2. 监听连接成功或失败的通知
3. 将要发送到端点的数据加入队列
4. 将数据发送到端点
5. 监听从端点传入的数据
6. 重复步骤 3 到 5
7. 关闭连接

第一步是创建到包含主机和端口号的套接字端点的连接。例如，要连接到一个端点，主机可能是 'foo.com'，端口号可能是 5555。创建`Socket`类的实例并使用该信息连接到端点。此时，我们还需要设置监听器来监听`Socket`可能派发的不同事件：

```javascript
var socket = new air.Socket();
socket.addEventListener( air.Event.CONNECT, onSocketOpen );
socket.addEventListener( air.ProgressEvent.SOCKET_DATA, onSocketData );
socket.connect( 'foo.com', 5555 );
```

我们还需要创建处理订阅事件的函数。第一个事件是`air.Event.CONNECT` 事件。该事件将告诉我们套接字何时已启动，以及何时可以与端点背后的服务进行通信。在本例中，我们向服务发送 UTF-8 编码字符串的字节：

```javascript
function onSocketOpen( event )

{
    // 这会将 UTF-8 格式的字符串 'Bob' 的
    // 二进制表示形式排队等待发送到端点。
    socket.writeUTFBytes( "Bob" );
    // 将实际的字节发送到服务器并清空
    // 流。然后我们等待数据发回给我们。
    socket.flush();
}
```

当收到数据时，会派发`air.ProgressEvent.SOCKET_DATA` 事件。我们连接的服务使用一个简单的协议：我们发送一个 UTF-8 编码的字符串，它返回一个 UTF-8 编码的字符串。这使得访问发回给我们的数据非常简单。要访问此数据，我们测量`Socket`上可用数据的总字节数，并使用`Socket`类的`read.readUTFBytes()`方法将这些字节作为 UTF-8 编码字符串读取。

```javascript
function onSocketData( event )
{
    var data =
        socket.readUTFBytes( socket.bytesAvailable );
    air.trace( data ); // Hello Bob
}
```

在我们的示例中，通信协议只是一个简单的字符串。在某些情况下，根据你通信的服务，你可能需要发送和接收其他数据类型。`Socket`类提供了读取和写入多种数据类型的方法，例如整数、布尔值、浮点数等。例如，如果我们与一个需要我们发送一个布尔值后跟一个整数的虚构服务通信，我们上面示例中的`onSocketOpen`函数可以像这样：

```javascript
function onSocketOpen( event )
{
    // 首先发送布尔值
    socket.writeBoolean( true );
    // 现在发送一个整数
    socket.writeInt( 10 );
    // 现在我们将字节发送到服务并
    // 清空缓冲区。
    socket.flush();
}
```

此示例提供了功能基线，可以在此基础上扩展以与许多不同的协议通信。目前唯一的限制是 AIR 中没有 SSL Socket 实现。对于安全通信，你将只能使用 HTTPS：

```html
<html>

<head>

<title>在套接字上通信</title>
<script type="text/javascript" src="AIRAliases.js"></script>
<script>

var socket = null;
function init()

{
    socket = new air.Socket();
    // 创建监听器，它们会告诉我们套接字
    // 何时打开以及何时从我们的服务接收到数据。
    socket.addEventListener( air.Event.CONNECT, onSocketOpen );
    socket.addEventListener( air.ProgressEvent.SOCKET_DATA,
                              onSocketData );
    // 连接到我们的服务，该服务位于主机 foo.com
    // 使用端口 5555。
    socket.connect( 'foo.com', 5555 );
}

function onSocketOpen( event )
{
    // 这会将 UTF-8 格式的字符串 'Bob' 的
    // 二进制表示形式排队等待发送到端点。
    socket.writeUTFBytes( "Bob" );
    // 将实际的字节发送到服务器并清空
    // 流。然后我们等待数据发回给我们。
    socket.flush();
}

function onSocketData( event )
{
    var data = socket.readUTFBytes( socket.bytesAvailable );
    air.trace( data ); // Hello Bob
}

</script>

</head>

<body onload="init()">

</body>

</html>
```

132 | 第 4 章：AIR 迷你食谱

### 在后台上传文件

**问题**

应用程序用户已离线创建了大量文件，现在你希望将这些文件发送到服务器，同时不阻塞用户进行任何其他工作。

**解决方案**

Adobe AIR 中的`File`类提供了一个专门为此目的设计的`upload()`方法，无需创建和管理 HTML 表单。

**讨论**

`File.upload()`方法可以通过 HTTP/S 将文件上传到服务器进行进一步处理。上传过程就像传统的 HTML 表单多部分文件上传一样，但无需在客户端操作表单。上传过程也在后台异步进行，允许应用程序在不中断的情况下继续处理。

## 提示

接收服务器的实现超出了本示例的范围。有许多技术及其教程可以优雅地处理文件上传。我们鼓励您研究您的可用选项。

主要有用的事件是`ProgressEvent.PROGRESS`和`Event.COMPLETE`。这两个事件分别负责通知应用程序上传进度，以及单个文件上传何时完成：

```javascript
var file =
new air.File( air.documentsDirectory, "image.jpg" );
file.addEventListener( air.ProgressEvent.PROGRESS, doProgress );
file.addEventListener( air.Event.COMPLETE, doComplete );
```

`doProgress`函数负责更新进度显示，`doComplete`函数负责在上传完成后执行清理工作。


```html
    file.browseForOpen( "Select File" );

}

</script>

</head>

<body onload="doLoad()">

<input id="btnUpload" type="button" value="Upload" />

<div id="txtProgress" style="visibility: hidden">

Uploading... 0%</div>

</body>

</html>
```

## 声音

### 播放声音

#### 问题
您需要在应用程序中播放声音。

#### 解决方案
使用 AIR 中的 `Sound` API 播放 MP3 文件。

#### 讨论
AIR 完全支持从 JavaScript 访问 Flash Player API`。这包括可用于播放本地或远程 MP3 文件的 `Sound` 类。

播放声音很简单，主要需要两个步骤：
1. 创建一个引用本地或远程声音的 `URLRequest` 实例。
2. 将 `URLRequest` 传递给 `Sound` 实例，然后播放它。

以下是相关的代码片段：

```
var soundPath =
    new air.URLRequest("app-resource:/sound.mp3");

var s = new air.Sound();

    s.load(soundPath);

    s.play();
```

首先，我们创建一个指向我们将要播放的 MP3 文件位置的 `URLRequest`。在这个例子中，我们使用一个 `app-resource` URI，它引用了包含在应用程序安装目录中的 `sound.mp3` 文件。您也可以使用任何有效的 URI，包括文件和 http URI：

```
var soundPath =
    new air.URLRequest("app-resource:/sound.mp3");
```

然后我们创建一个 `Sound` 类的实例，传递 MP3 路径的引用，然后调用 `play`：

```
var s = new air.Sound();

    s.load(soundPath);

    s.play();
```

这是一个带有播放按钮的完整示例：

```
<html>

<head>

    <script src="AIRAliases.js" />

    <script type="text/javascript">

        function playSound()
        {

            var soundPath =
                new air.URLRequest("app-resource:/sound.mp3");

            var s = new air.Sound();

                s.load(soundPath);

                s.play();

        }

    </script>
</head>

<body>

    <input type="button" value="Play" onClick="playSound()">

<body>

</html>
```

至此，您应该对 Adobe AIR、如何构建 AIR 应用程序以及使用 AIR API 有了扎实的理解。请务必查看前言中列出的资源，以学习更高级的 Adobe AIR 开发技术。

## 附录 A 

### AIR 命令行工具
AIR SDK 提供了以下命令行工具：

- `ADL`：使用此工具启动和测试 AIR 应用程序，而无需安装它。
- `ADT`：使用此工具将 AIR 应用程序打包为可重新分发的 AIR 文件。

本附录列出了每个命令行工具的选项。
有关使用这些工具的示例，请参见第 2 章。

### ADL 详解
`ADL` 是一个命令行工具，它基于 AIR 应用程序的描述符文件启动 AIR 应用程序，而无需安装该应用程序。这对于测试和调试应用程序非常有用。

通常，您希望调用 `ADL` 工具并传递一个参数：应用程序描述符文件（应用程序 `.xml` 文件）的路径：

```
adl application.xml
```

`adl` 命令的完整语法是：

```
adl ( -runtime <path-to-runtime-dir> )? <path-to-app-xml>
<path-to-root-dir>? ( -- ... )?
```

表 A-1 提供了 `ADL` 命令行参数的说明。

表 A-1. ADL 命令行参数

| 选项 | 描述 |
|---|---|
| `-runtime` | 可选参数，指定应使用的 AIR 运行时所在的目录。 |
| `path-app-xml` | 要启动的应用程序的应用程序描述符文件。 |
| `path-to-root-dir` | 可选参数，指定包含应用程序描述符文件的目录。 |
| `--` | 此参数之后指定的任何参数都将作为启动/命令行参数传递给应用程序，并且可以通过 `InvokeEvent` 从应用程序中访问。 |

### ADT 详解
`ADT` 是一个命令行工具，用于将 AIR 应用程序打包成可重新分发的 AIR 文件。然后，AIR可以从该 AIR 文件安装 AIR 应用程序。

通常，您希望以以下方式调用 `ADT` 工具：

```
adt -package HelloWorld.air application.xml HelloWorld.swf
```

在此示例中，`ADT` 工具根据 `application.xml` 应用程序描述符文件创建一个名为 `HelloWorld.air` 的 AIR 文件。

`adt` 命令的语法为：

```
adt -package <air-file> <app-xml> <fileOrDir>* ( -C <dir> <fileOrDir>+ )*
```

```markdown

```

表 A-2 显示了 `ADT` 的命令行选项。

### 表 A-2. ADT 命令行选项

| 选项 | 描述 |
| :--- | :--- |
| `-package` | 第一个参数必须是 `-package`。 |
| `air-file` | 要由 `ADT` 创建的 AIR 文件的相对或绝对路径。 |
| `app-xml` | 应用程序的应用程序描述符文件的相对或绝对路径。 |
| `fileOrDir` | 一个或多个文件或目录名，用于标识要包含在包中的其他文件。每个后续的文件或目录名应以空格分隔。如果指定了目录名，则该目录及其子目录中的所有文件都将包含在内。但是，文件系统中被标记为隐藏的文件将被忽略。如果列出的任何文件与指定的参数中指定的文件相同，则该文件将被忽略；它不会被第二次添加到包文件中。当应用程序安装时，这些文件和目录将被复制到应用程序安装目录中。 |
| `-C <dir>` | 这会更改命令行中列出的后续文件或目录的根目录路径。 |

## 附录 B
AIR JavaScript 别名

表 B-1 到 B-12 显示了在 `AIRAliases.js` 中创建的 JavaScript 别名以及它们对应的 AIR 和 Flash Player API。

> **提示**

所有未设别名的 ActionScript API 均可通过 JavaScript 中的 `window.runtime` 属性访问。

### 表 B-1. 顶层别名

| 别名 | ActionScript API |
|---|---|
| `air.trace` | `trace` |
| `air.navigateToURL` | `flash.net.navigateToURL` |
| `air.sendToURL` | `flash.net.sendToURL` |

### 表 B-2. 文件别名

| 别名 | ActionScript API |
|---|---|
| `air.File` | `flash.filesystem.File` |
| `air.FileStream` | `flash.filesystem.FileStream` |
| `air.FileMode` | `flash.filesystem.FileMode` |

### 表 B-3. 事件别名

| 别名 | ActionScript API |
|---|---|
| `air.Event` | `flash.events.Event` |
| `air.FileListEvent` | `flash.events.FileListEvent` |
| `air.IOErrorEvent` | `flash.events.IOErrorEvent` |
| `air.InvokeEvent` | `flash.events.InvokeEvent` |
| `air.HTTPStatusEvent` | `flash.events.HTTPStatusEvent` |
| `air.SecurityErrorEvent` | `flash.events.SecurityErrorEvent` |
| `air.AsyncErrorEvent` | `flash.events.AsyncErrorEvent` |
| `air.NetStatusEvent` | `flash.events.NetStatusEvent` |
| `air.OutputProgressEvent` | `flash.events.OutputProgressEvent` |
| `air.ProgressEvent` | `flash.events.ProgressEvent` |
| `air.StatusEvent` | `flash.events.StatusEvent` |
| `air.EventDispatcher` | `flash.events.EventDispatcher` |
| `air.DataEvent` | `flash.events.DataEvent` |
| `air.TimerEvent` | `flash.events.TimerEvent` |

### 表 B-4. 原生窗口别名

| 别名 | ActionScript API |
|---|---|
| `air.NativeWindow` | `air.NativeWindow = flash.display.NativeWindow` |
| `air.NativeWindowDisplayState` | `flash.display.NativeWindowDisplayState` |
| `air.NativeWindowInitOptions` | `flash.display.NativeWindowInitOptions` |
| `air.NativeWindowSystemChrome` | `flash.display.NativeWindowSystemChrome` |
| `air.NativeWindowResize` | `flash.display.NativeWindowResize` |
| `air.NativeWindowType` | `flash.display.NativeWindowType` |
| `air.NativeWindowErrorEvent` | `flash.events.NativeWindowErrorEvent` |
| `air.NativeWindowBoundsEvent` | `flash.events.NativeWindowBoundsEvent` |
| `air.NativeWindowDisplayStateEvent` | `flash.events.NativeWindowDisplayStateEvent` |

### 表 B-5. 几何别名

| 别名 | ActionScript API |
|---|---|
| `air.Point` | `flash.geom.Point` |
| `air.Rectangle` | `flash.geom.Rectangle` |

### 表 B-6. 网络别名

| 别名 | ActionScript API |
|---|---|
| `air.FileFilter` | `flash.net.FileFilter` |
| `air.LocalConnection` | `flash.net.LocalConnection` |
| `air.NetConnection` | `flash.net.NetConnection` |
| `air.URLLoader` | `flash.net.URLLoader` |
| `air.URLLoaderDataFormat` | `flash.net.URLLoaderDataFormat` |
| `air.URLRequest` | `flash.net.URLRequest` |
| `air.URLRequestDefaults` | `flash.net.URLRequestDefaults` |
| `air.URLRequestHeader` | `flash.net.URLRequestHeader` |
| `air.URLRequestMethod` | `flash.net.URLRequestMethod` |
| `air.URLStream` | `flash.net.URLStream` |
| `air.URLVariables` | `flash.net.URLVariables` |
| `air.Socket` | `air.Socket = flash.net.Socket` |
| `air.XMLSocket` | `flash.net.XMLSocket` |
| `air.Responder` | `flash.net.Responder` |
| `air.ObjectEncoding` | `flash.net.ObjectEncoding` |

### 表 B-7. 系统别名

| 别名 | ActionScript API |
|---|---|
| `air.Shell` | `flash.system.Shell` |
| `air.System` | `flash.system.System` |
| `air.Security` | `flash.system.Security` |
| `air.Updater` | `flash.system.Updater` |

### 表 B-8. 功能别名

| 别名 | ActionScript API |
|---|---|
| `air.Capabilities` | `flash.system.Capabilities` |
| `air.NativeWindowCapabilities` | `flash.system.NativeWindowCapabilities` |

### 表 B-9. 桌面别名

| 别名 | ActionScript API |
|---|---|
| `air.ClipboardManager` | `flash.desktop.ClipboardManager` |
| `air.TransferableData` | `flash.desktop.TransferableData` |
| `air.TransferableFormats` | `flash.desktop.TransferableFormats` |
| `air.TransferableTransferMode` | `flash.desktop.TransferableTransferMode` |

### 表 B-10. 实用工具别名

| 别名 | ActionScript API |
|---|---|
| `air.ByteArray` | `flash.utils.ByteArray` |
| `air.Dictionary` | `flash.utils.Dictionary` |
| `air.Endian` | `flash.utils.Endian` |
| `air.Timer` | `flash.utils.Timer` |

### 表 B-11. 媒体别名

| 别名 | ActionScript API |
|---|---|
| `air.ID3Info` | `flash.media.ID3Info` |
| `air.Sound` | `flash.media.Sound` |
| `air.SoundChannel` | `flash.media.SoundChannel` |
| `air.SoundLoaderContext` | `flash.media.SoundLoaderContext` |
| `air.SoundMixer` | `flash.media.SoundMixer` |
| `air.SoundTransform` | `flash.media.SoundTransform` |

### 表 B-12. SQL/数据库别名

| 别名 | ActionScript API |
|---|---|---|
| `air.SQLConnection` | `flash.data.SQLConnection` |
| `air.SQLStatement` | `flash.data.SQLStatement` |
| `air.SQLResult` | `flash.data.SQLResult` |
| `air.SQLError` | `flash.errors.SQLError` |
| `air.SQLErrorEvent` | `flash.events.SQLErrorEvent` |
| `air.SQLErrorCode` | `flash.errors.SQLErrorCode` |
| `air.SQLEvent` | `flash.events.SQLEvent` |
| `air.SQLUpdateEvent` | `flash.events.SQLUpdateEvent` |
| `air.SQLTransactionLockType` | `flash.data.SQLTransactionLockType` |
| `air.SQLColumnNameStyle` | `flash.data.SQLColumnNameStyle` |
| `air.SQLErrorOperation` | `flash.errors.SQLErrorOperation` |

## 索引

**A**

- ActionScript, viii
- ActionScript 3 库, 59
    - 分发, 61
- API 别名, 144–148
- API, 通过 JavaScript 访问, 144
- `addEventListener()`, 57
- ADL 命令行工具, 18, 24, 141
    - 使用其启动, 34
    - 命令行参数, 142
- Adobe AIR 卸载, 23
- Adobe Integrated Runtime
- ADT 命令行工具, 18, 24, 142
    - 命令语法, 142
    - 命令行选项, 143
    - 使用其创建 AIR 文件, 40
- AIR (Adobe Integrated Runtime), vii, 1, 6
- AIR API（参见 API）
- AIR 应用程序（参见应用程序）
- Ajax 支持, 48
- Beta 1, x
- Beta 版本, 23
- 功能和特性, ix
- 运行时, 20
- Beta 版本, 23
- Cookie, 46
- 桌面集成, 14
- 开发者常见问题, xv
- 开发工具, 17
- HTML 对话框支持, 47
- 安装, 22
- 命名约定, vii
- 官方网站，xv
- 主要技术, 7
- SDK（参见 SDK）
- 安全模型, 15–17
- 支持的操作系统, 21
- 卸载 Beta 版本, 22
- `air.Event.CONNECT`, 130
我们想听取索引的建议。请发送至 oreilly.com。

**A**
- URI 方案, 49–51
- XMLHttpRequest 支持, 48
- `air.Event.SOCKET_DATA`, 130
- `air.trace()`, 128
- `AIRAliases.js`, 57, 144
- `HelloWorld`, 29–38
- `AIR` 参见 API
- `AIR` 应用程序, 32
- `AIR` 安装, 23
- `AIR` 支持, 21
- `AIR` 卸载, 22
- `AIR` Beta 版本, 24
- `AIR` 预 Beta 安装, 卸载, 22
- `AIR` 安装, 23
- `SDK` 安装, 24
- `SDK` 命令行工具路径配置, 27
- `AIR` 应用程序, 32
- `AIR` 部署, 41
- `AIR` I/O API, 105
- 访问, 33, 55
- `Actionscript API` 别名, 144–148
- `APIs`, 从 JavaScript 访问, 55
- `application.xml`, 63
- 应用程序开发, 20
- 应用程序自定义控件, 62–65
- 应用程序描述符文件, 29–32
- 应用程序安装, 141
- 应用程序技术, 7
- 应用程序/信任, 17
- 应用程序/JavaScript, 7
- 应用程序/创建, 28–34
- 应用程序/HTML, 10, 11
- 应用程序/HTML, 70
- 应用程序/编辑器, 21
- 应用程序/部署, 108–113
- 应用程序内部拖放, 108–113
- `Apple Macintosh OS`
- 异步读取文件中的文本, 82–86

**B**
- 返回按钮, 4
- `.bashrc` 文件, 27
- 浏览器 (参见 browsers)

**C**
- 离线使用缓存资源, 105–108
- Cookie, 46
- 冲突, 4
- 命令行工具, 18, 24, 141
- 命令行参数, 127–129
- 命令行语法, 142
- 命令行选项, 143

**D**
- 数据库 (参见 embedded databases)
- `dataTransfer` 对象, 110
- 桌面集成, 14
- 文档技术, 9
- 拖放, 108–113
- 限制, 111

**E**
- 嵌入式数据库, 113–127
- 连接到, 114–115
- 访问数据, 123–127
- 存储数据, 119–121
- 创建表, 116–119
- 错误, 36
- `event` 别名, 144
- `Event.COMPLETE` 事件, 134, 135

**F**
- `file` 别名, 144
- `file API`, 76–94
- 异步读取文件中的文本, 82–86

**G**
- `Geometry` 别名, 146

**H**
- HTML, vii, 10
- HTML 对话框, 47
- HTML/JavaScript, 7
- HTMLControl, 70

**I**
- IDE (集成开发环境), 21
- `index.html`, 64
- `InvokeEvent` 事件, 127

**J**
- JavaScript, viii, 45
- AIR APIs, 从其访问, 54–61
- JavaScript 别名, 144
- 使用 JavaScript 框架, 53
- 运行时错误, 36
- `window.open()` 方法, 66

**K**
- `-khtml-user-drag:element` 样式, 110
- `-khtml-user-drag:none`, 110

**L**
- Linux AIR 支持, 21
- 监听器注册, 57
- `Login.html`, 72

**M**
- `media` 别名, 147
- Microsoft Windows OS
- AIR Beta 版本, 卸载, 24
- AIR 预 Beta 安装, 卸载, 22
- AIR 支持, 21
- AIR, 安装, 23
- SDK, 安装, 24
- SDK 命令行工具路径配置, 27

**N**
- `native` 别名, 146

**O**
- 输出输出, 36

**P**
- 路径, 25
- 放置于, 25

**R**
- 引用, 76
- `File.browseForDirectory()` 方法, 99
- `File.browseForOpen()` 方法, 94
- `File.browseOpenMultiple()` 方法, 97
- `File.resolve()` 方法, 77
- `FileStream` 类, 77
- `FileStream.open()` 方法, 77
- `FileStream.writeMultiByte()` 方法, 77
- Flash, viii
- Flash Player, 8
- APIs, 从 JavaScript 访问, 55
- 事件, 56
- Flex Builder, viii
- Flex Framework, viii

**S**
- 脚本, 57
- 系统路径, 25
- 命令行参数, 127–129
- 命令行工具, 18, 24, 141
- 安全, 15–17
- 支持的操作系统, 21

**T**
- 技术, 7
- 文本, 76–79

**U**
- 统一资源标识符 (URIs), 49

**W**
- Web 应用程序, 1
- Web 浏览器, 4
```

```