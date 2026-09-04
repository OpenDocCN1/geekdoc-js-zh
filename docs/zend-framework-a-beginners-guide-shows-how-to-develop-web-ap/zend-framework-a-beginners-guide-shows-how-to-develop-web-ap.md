
# Zend Framework 入门指南：介绍如何使用 PHP 和 Zend Framework 开发 Web 应用；涵盖 XML、Ajax 和 Web 服务；包含分步骤项目和代码示例

序言由 Matthew Weier O'Phinney，Zend Framework 项目主管

## Zend Framework

- 展示了如何使用 PHP 和 Zend Framework 开发 Web 应用
- 涵盖 XML、Ajax 和 Web 服务
- 包含分步演示的项目和代码示例

> “对 Zend Framework 组件的详细描述，以及极具价值的提示和最佳实践，帮助你少力多获。对于任何使用 Zend Framework 的人来说，都是必备参考资料。”
> 
> — Michelangelo van Dam，Zend Framework 顾问及 PHPBenix 理会成员

给一直问“为什么？”的 Tonka，以及总是知道答案的 Farah。

## 关于作者

**Vikram Vaswani** 是 Melonfire (http://www.melonfire.com/) 的创始人兼首席执行官，这是一家在开源工具和技术方面拥有专长的咨询公司。他作为 Web 开发者和产品经理拥有 12 年 PHP 和 MySQL 工作经验，并创建并部署了用于企业内网、高流量互联网网站以及任务关键型客户端应用的各种 PHP 程序。

Vikram 还是开源运动的热热支持者，通过他在 Zend Developer Zone 和 IBM DeveloperWorks 的定期专栏，定期向社区贡献关于 PHP、MySQL、XML 及相关工具的文章和教程。他是 Zend Technologies 广受赞誉的著作 *PHP 101* 的作者。

## 关于技术编辑

**Ryan Mauger** 是 Lupimedia (http://www.lupimedia.com/) 的首席开发人员，这是一家位于英国萨默塞的多媒体设计机构，专门为设计导向型网站提供定制内容管理系统。Ryan 是热衷的 Zend Framework 支持者和贡献者，经常在 IRC 上回答问题。在不推扬 Zend Framework 时，他通过读犯罪小说、看电影、打网球、写博客以及前往湖区钓飞钓来消遣时光。

## 目录

- 总结 ........................................................................................................................ 99
- 安装 Doctrine .......................................................................................... 107
- 设置模型关系 ................................................................................. 115
- 总结 ........................................................................................................................ 127
- 总结 ........................................................................................................................ 170

ii

ix

### 尝试此 8-1：创建一个自定义错误页面 ................................................... 252
### 格式化日志消息 ..................................................................................... 259
### 使用翻译视图 Helper ....................................................................... 293
### 总结 ........................................................................................................................ 309

创建导航操作助手 ................................................................................. 358

分析性能 ................................................................................... 382
基准测试 ....................................................................................................... 382
代码剖析 ....................................................................................... 384
查询剖析 ...................................................................................... 387

数据缓存 ................................................................................................................... 392
理解缓存操作 .......................................................................... 392
理解缓存前端和后端 .................................................... 395
使用缓存管理器 ...................................................................................... 398
缓存 Doctrine 查询 ...................................................................................... 399

优化应用程序代码 .......................................................................................... 401
查询调优 ......................................................................................................... 401
懒加载 ......................................................................................................... 404

尝试练习 12-1：提高应用程序性能 ....................................... 405
配置应用程序缓存 ...................................................................... 405
缓存翻译字符串 ................................................................... 406
缓存查询结果 .......................................................................... 406
缓存 Twitter 和博客 Feed源 ............................................................................ 408
总结 ......................................................................................................................... 410

获取软件 .................................................................................................... 414
安装和配置软件 ........................................................................ 416
在 UNIX 上安装 ............................................................................................... 416
在 Windows 上安装 ........................................................................... 420
测试软件 ....................................................................................................... 426
测试 MySQL ...................................................................................................... 426
测试 PHP .......................................................................... 427
设置 MySQL 超用户密码 .................................................... 428
总结 ......................................................................................................................... 428

xiii

## 序言

PHP 生态系统在过去的六年里发生了巨大的变化。在 PHP 5 出现之前，我们 PHP 开发者主要是通过临时性的方式创建项目，每个项目都与前一个项目有所不同；如果我们留心，每个项目都会在前一个基础上有所改进——但并没有任何保证。虽然存在管理代码质量和标准的工具与方法，但它们仍处于成熟阶段，且没有被广泛使用。结果是，将 PHP 作为构建稳定的、企业级应用程序的基础的想法遭到了广泛的嘲笑——尽管事实上，它正为 Web 上一些流量最大的网站提供着动力支持。

随着 PHP 5 的出现，我们开始更多地关注稳健的编程实践。通过修订和重构对象模型，我们现在有了一个坚实的基础来构建可重用的对象。像 PHPUnit 这样的工具利用对象模型，简化并实现了稳健的测试实践。这反过来又促使人们更加关注代码质量在 PHP 应用生命周期中的位置。

PHP 框架正是从这个生态系统中开始出现的。虽然有几个起源于 PHP 4 时代，但这一理念在 PHP 5 中发扬光，少数框架开始主导这一格局。这些框架旨在为其用户提供最佳实践，并为他们构建的应用提供可重复、可重用的结构。

其中就包括 Zend Framework。根据其网站，Zend Framework 的使命非常简单：扩展 PHP 的艺术与精神，Zend Framework 基于简单性、面向对象的最佳实践、企业友好的许可协议以及经过严格测试的敏捷代码库。Zend Framework 专注于构建更安全、更可靠且现代的 Web 2.0 应用程序和 Web 服务，并消费广泛提供的 API。

在书中，你将从一位作者那里学习 Zend Framework 如何实现这些目标，这位作者既精通该领域，又是一位能力出且清晰的技术作家。你将获得详尽且易懂的解释以及完整的示例——并希望在读完书后，你会产生使用这一已成为行业事实标准的 Zend Framework 来开发你自己的应用的意愿。

—Matthew Weier O’Phinney，Zend Framework 项目负责人

xiv

## 致谢

Zend Framework 是一部复杂的软件，关于它写一本书*并不是*——正如我在过去八个月里发现的那样——一项特别简单的任务。幸运的是，在这个过程中得到了一个多元化且充满活力的群体的帮助，他们所有人对于将这本书交到你手中都发挥了重要作用。

首先，衷心感谢我的妻子，她支持了我整个过程，并确保我有一个舒适且无压力的工作环境。我非常确定，如果没有她的帮助，这本书永远不会面世。谢谢，亲爱的！

McGraw-Hill 的编辑和营销团队也在此获得荣誉。这是我与他们合作的第六本书，像往常一样，与他们合作是一件非常愉快的事。收购协调员 Joya Anthony、编辑主管 Patty Mon 以及执行编辑 Jane Brownlow 和 Megg Morin 都指导了这手手稿的开发过程，并在将其从页面上的像素转化为你手中精美且专业的产品的过程中发挥了巨大作用。感谢他们代表我所付出的专业知识、奉献和努力。

我还想特别单提到此本书的技术编辑 Ryan Mauger 给予特别表扬。Ryan 审阅了每一行代码，并运用他对 Zend Framework 的丰富知识，确保最终产品既在技术上是可靠的，又反映了当前的最佳实践。感谢他在整个书籍编写过程中提供的帮助和建议。如果你正在寻找 PHP 专家，没有比他更合适的人了！

最后，感谢以下人士让整个书籍编写过程比通常更加愉快：Patrick Quinlan, Ian Fleming, Bryan Adams, The Stones, Peter O’Donnell, *MAD* *Magazine,* Scott Adams, Gary Larson, VH1, Britney Spears, George Michael, Kylie Minogue, *Buffy the Vampire Slayer,* Farah Malegam, Stephen King, Shakira, Anahita Marker, John le Carre, The Saturdays, Barry White, Gwen Stefani, Ping Pong, Robert Crais, Robert B. Parker, Baz Luhrmann, Stefy, Anna Kournikova, John Connolly, Wasabi, Omega, Pidgin, Cal Evans, Ling’s Pavilion, Tonka 和他的邪恶双胞胎 Bonka, Richelle Mead, Din Tai Fung, HBO, Mark Twain, Tim Burton, Harish Kamath, Madonna, John Sandford, *Dollhouse,* Iron Man, London Tube, Dido, Google.com, *The Matrix,* Lee Child, Michael Connelly, Celio, Antonio Prohias, Quentin Tarantino, Alfred Hitchcock, Woody Allen, 木野, Percy Jackson, Jennifer Hudson, Mambo’s and Tito’s, Easyjet, Humphrey Bogart, Thai Pavilion, Wikipedia, Amazon.com, U2, Ubuntu, The Three Stooges, Pacha, Oscar Wilde, Hugh Grant, Alex Rider, Punch, Kelly Clarkson, Scott Turow, Slackware Linux, Calvin and Hobbes, Yo! Sushi, Blizzard Entertainment, Alfred Kropp, Otto, Pablo Picasso, Popeye and Olive Oyl, Dennis Lehane, Trattoria, Dire Straits, Bruce Springsteen, David Mitchell, *The West Wing,* Wagamama, Santana, Rod Stewart，以及我在家里及各地的朋友。

xv

## 引言

Zend Framework 确实正如朽的海明威所说，是一个“移动盛宴”。它被构想并实现为 PHP 开发者的一个健壮、功能丰富的组件库，允许你快速高效地执行各种应用程序任务，包括创建和验证表单、处理 XML、生成动态菜单、数据分页、处理 Web 服务等等！

然而，Zend Framework 最重要的贡献在于通过引入更结构化的方法提升了 PHP 的艺术。这种结构化的方法产生了更简洁、更易维护且更安全的应用程序，这也是开发者从旧的“临时”编程风格转向新的框架方法的主要原因之一。



但对于许多新手来说，Zend Framework 一次迈向未知的恐惧跨越。模型-视图-控制器（MVC）模式、松耦合架构以及大量的组件，往往会让习惯于过程化编程的开发者感到困惑。这正是本书大显用场的地方。如果你是数百万听说过 Zend Framework 并好奇它能为你做些什么的读者之一，那么这本书正适合你。它仔细研究了 Zend Framework 的一些重要功能——例如模型-视图-控制器实现、路由、输入验证、国际化和缓存——并向你展示如何在实际语境中使用它们。它还引导你完成使用 Zend Framework 构建完整 Web 应用程序的过程，从基础开始，添加复杂的功能，如数据分页和排序、用户身份验证、异常处理、本地化和 Web 服务。简而言之，它赋予了你所需的知识，通过利用 Zend Framework 的力量来增强你的 PHP 开发。

## 谁应该读这本书

### Zend Framework：入门指南

为了能够运行书中的示例应用程序，你需要一个运行良好的 PHP 5.x 安装环境，最好配有 Apache 2.2.x Web 服务器和 MySQL 5.x 数据库服务器。你还需要（显而易见的！）最新版本的 Zend Framework。关于如何获取和配置 PHP 开发环境的详细信息，请参本书的附录，而第 1 章将详细介绍 Zend Framework 的安装过程。

## 本书涵盖内容

由于 `Zend Framework: A Beginner’s Guide` 针对的是 Zend Framework 新手，书的前半部分将从解释基本概念和解决简单问题开始。一旦你熟悉了 Zend Framework 开发的基础知识，书的后半部分将引入更复杂的问题，例如国际化和性能优化，并说明可能的解决方案。这意味着你应该按照顺序阅读章节，因为每一章都扩展了你在后续章节中将需要的知识。

本书使用不同类型的格式来突出显示特殊建议。列表如下：

- `NOTE`：关于该主题的额外见解或信息
- `TIP`：帮助你把工作做得更好的技巧或窍门
- `CAUTION`：需要注意的事项
- `Q:` 一个经常出现的问题，……
- `A:` ... 及其对应的答案

## 提问专家

在书的代码列表中，加粗显示的文本是在提示符处要输入的命令。例如，在下述代码中：

```sql
mysql> INSERT INTO movies (mtitle, myear) VALUES ('Rear Window', 1954);
```

等一下，让我根据提供的文本重新格式化：

```sql
Query OK, 1 row affected (0.06 sec)
```

加粗的行是你在命令行提示符中输入的查询。你可以以此作为指南尝试书中的命令。

你可以在书的配套网站找到书中讨论的示例应用程序代码，`http://www.zf-beginners-guide.com/`。代码存档按章节组织，可以直接可以直接下载并在你的 Zend Framework 开发环境中使用。

### 核心技能与概念

- 学习基于框架开发的优势
- 理解 Zend Framework 的历史和独特进展
- 理解 Zend 应用程序的结构
- 安装并开始使用 Zend Framework

考虑到这一点，在过去的几年里，PHP 社区一直在进行一致且显见的努力，旨在从随意的“随心所欲”编程转向更加标准化、以框架为导向的方法。这种方法不仅让从零开始构建 PHP 应用程序变得更容易，而且产生了更整洁、更一致且安全的代码。本章以及本书的剩余部分将向你介绍这样一个框架——Zend Framework，它为严肃的开发者提供了一种灵活且可扩展的 PHP 应用构建方法。

### 概述

在其官方网站（`http://framework.zend.com/`）的描述中，Zend Framework 是“一个基于 PHP 5 用于开发 Web 应用程序和服务的开源框架，基于了简单性、面向对象的最佳实践、企业友型许可以及经过严格测试的代码库。”它提供了一套全面的工具，用于构建和部署基于 PHP 的应用程序，并内置了用于安全、输入验证、缓存、数据库操作和国际化等常用 API。

与许多其他框架不同，Zend Framework 采用了“松耦合”架构。简单来说，这意味着虽然框架由许多组件组成，但这些组件在很大程度上是独立的，彼此之间的联系极小。这种松耦合架构有助于生成轻量级应用程序，因为开发者可以根据当前任务仅选择特定的组件。例如，想要为应用程序添加身份验证或缓存的开发者可以使用 `Zend_Auth` 或 `Zend_Cache` 组件，而无需使用整个框架。

Zend Framework 还提供了完整的模型-视图-控制器（MVC）模式实现，这允许将业务逻辑与用户界面和数据模型分离。这种模式被用于中等到大型应用程序开发，因为它鼓励代码复用并产生更易于维护的代码结构。Zend Framework 对 MVC 模式的实现将在第 2 章详细讨论。

Zend Framework 由 Zend Technologies 创建并维护，这是一家商业软件供应商，其创始人 Andi Gutmans 和 Zeev Suraski 还负责 1997 年发布的 PHP 3.0 首次重大重写。Zend Framework 的第一个版本 `v1.0` 于 2007 年 7 月发布，包含了 35 个核心组件，包括身份验证、配置管理、数据库访问、RSS 和 Atom Feed 生成以及本地化。

从那时起，框架经历了多次迭代，最新的版本 `v1.10` 现在包含了超过 65 个支持（其他诸如）Adobe Action Message Format (AMF)、Google Data APIs 以及 Amazon SQS Web 服务的组件。幸运的是，组件数量的增加伴随着文档的相应增长——Zend Framework `v1.9`（约 2009 年）的手册重 3.7MB，而 2007 年随 Zend Framework `v1.0` 发布的手册仅为 780KB。

#### 入门指南

尽管 Zend Technologies 在多个不同市场进行商业运营，但它通过 BSD 许可证将 Zend Framework 向公众开放，从而允许在不支付许可费的情况下自由用于专有商业产品。这种“企业友好”的许可政策让 Zend Framework 在企业和个人用户中广受欢迎。初创公司、世界 500 强、独立开发者以及 PHP 爱好者都是该项目的粉丝——截至本文写作，Zend Framework 的下载次数已超过 1000 万次，有超过 400 个基于或扩展了 Zend Framework 的开源项目。

在邮件列表和 Wiki 上可以发现活跃且热情的开发者社区在交流漏洞补丁和技巧，在线手册和参考指南提供了额外的支持。社区还鼓励通过提交新组件向框架“回馈”——目前该项目有 500 多独立贡献者——只要这些贡献符合 Zend 对文档和单元测试的要求。

你可能会疑惑，为什么使用 Zend Framework 比你现在习惯的自己手写代码是明智主意。嗯，以下是一些原因。

#### 标准遵循与最佳实践

与其他某些编程语言不同，PHP 并不强制通用的编码标准。结果是 PHP 应用程序的编写方式在开发者之间存在显著差异，难以确保整个项目的一致性。PHP 相对缺乏“严谨性”也可能产生不符合最佳实践的代码，使其容易受到攻击。

相比之下，Zend Framework 结合了当前的最佳实践思想，提供了标准的目录系统布局，并为常见的应用程序开发任务（如输入验证和清理）提供了内置支持。因此，将其作为 PHP 项目的基础会自动产生更高质量的代码，以及一个在安全问题上更具前瞻性的应用程序。此外，由于 Zend Framework 文档齐全，后期加入项目团队的开发者将拥有更短的学习曲线，并更快地为项目做出贡献。

Zend Framework 是完全面向对象的，并充分利用了 PHP 5.x 中的新对象模型。这种面向对象编程（OOP）架构鼓励代码复用，允许开发者显著减少编写重复代码花费的时间。这一事实在 Web 应用程序背景下尤为重要，因为 Web 应用程序通常需要对其数据暴露多个接口。例如，假设你希望为应用程序现有的搜索功能构建一个 XML 接口。使用 Zend Framework，这只需要定义一个新的视图来处理将控制器输出重新格式化为 XML 即可。无需重写任何现有的控制器逻辑，整个过程透明且易于实现。

作为一个旨在 Web 应用程序开发的项目，如果 Zend Framework 不包含对应用程序国际化的全面支持，那将是非常异常的。`Zend_Locale` 组件允许对用户区域进行控制，而 `Zend_Translate` 组件使得支持中文等欧洲字符集成为可能。其他实用的组件包括用于本地化的 `Zend_Date` 和 `Zend_Currency`。

Zend Framework 是一个开源项目。虽然项目由 Zend Technologies 赞助，但大部分开发由全球志愿者团队完成，他们负责修复漏洞和添加功能。Zend Technologies 为项目提供方向，并有一组“大师工程师”决定哪些内容包含产品中。正如前面提到的，该框架可以在不支付许可费或投资昂贵硬件软件的情况下使用。这降低了软件开发成本，而不影响灵活性或可靠性。代码的开源性质进一步意味着任何地的开发者都可以检查代码树、发现错误并建议可能的修复；这产生了一个稳定的产品，漏洞一旦被发现，通常在几小时内就能解决！

正在寻找在应用程序中集成 Flickr 流或 Google Maps 数据的方法？尝试 `Zend_Service_Flickr` 或 `Zend_Gdata` 组件。需要使用 Action Message Format (AMF) 与 Flash 应用程序通信？使用 `Zend_Amf` 组件。需要快速在应用程序中集成 RSS Feed？`Zend_Feed` 拥有你所需。正如这些示例所示，像 Zend Framework 这样由社区支持的项目，优点之一是它让你接触到全球数百开发者的创造力和想象力。

将它们集成到你的非 MVC 应用程序中。这种松耦合有助于减少应用程序的占用，并为未来的更改保留了灵活性。

Zend Framework 团队遵循激进的发布计划，平均每月发布一到三个版本。除了这些稳定版本外，还有预览版（previews）和候选版本（release candidates），它们的作用是在准备最终发布期间，为社区提供预期内容的预告。这些频繁的发布不仅是为了保持项目的持续进展，还为了确保尽可能快地发现并解决漏洞。开发者还可以从项目的公共 Subversion 仓库访问“前沿”代码。

由于 Zend Framework 是一组持续更新的松耦合组件集，因此单元测试对于确保组件继续正常工作以及代码库在多个发布周期中保持稳定具有至关性。Zend Framework 拥有严格的单元测试策略，该策略规定：只有当组件伴随有相当完整且可运行的单元测试集（使用 PHPUnit 测试框架编写）时，才能将其添加到框架中。此策略确保了版本之间的向后兼容性，并使得回归问题能够被及时察觉。

Zend Framework 包含一项“工具化”功能，允许开发者以极小的努力启动并运行一个新的 Zend Framework 项目。该功能实现为基于 `Zend_Tool` 组件构建的命令行脚本，它负责为新项目创建基础文件系统布局，并填充初始的控制器（controllers）、视图（views）和动作（actions）。开发者可以使用此工具脚本作为方便的快捷方式，随着开发的进展快速创建新的项目对象。

Zend Framework 由 Zend Technologies 赞助，该公司是 PHP 领域最著名的软件公司之一。该公司为企业用途生产了多种商业产品，并在为 PHP 开发者创建成功且创新的产品方面拥有悠久记录，例如 Zend Server（一种用于业务关键型应用的 PHP Web 应用服务器）和 Zend Studio（一个用于 PHP 应用程序开发的集成 IDE）。Zend Technologies 的客户包括 IBM、McAfee、FOX Interactive Media、Lockheed Martin、Salesforce.com、NASA 和 Bell Canada；因此，它对 Zend Framework 的支持确保了在市场上的即时信誉，并在说服客户和/或高层跳到基于框架的开发时，作为一个非常有用的工具。

Zend Technologies 作为领先的企业 PHP 解决方案供应商之一的市场地位，使其为 Zend Framework 获得了广泛的行业支持。Zend Framework 对许多第三方工具和技术提供原生支持，包括 Adobe Action Message Format (AMF)、Google Data APIs、Dojo Toolkit、Microsoft CardSpace 以及来自 Amazon、Yahoo!、Twitter、Flickr、Technorati 和 Del.icio.us 的 Web 服务。

不仅于此。PHP 的优势之一长期以来一直是它对各种不同数据库、文件格式和协议的支持。Zend Framework 通过其 `Zend_Db` 组件提供了访问 MySQL、PostgreSQL、Oracle 和 Microsoft SQL Server 数据库（以及其他）的通用 API，还包含了使用 SMTP、IMAP 和 POP3 协议发送和接收电子邮件的组件；使用 SOAP 和 REST 协议构建 Web 服务；编码和解码 JSON 数据；解析 Atom 和 RSS 格式的馈送；以及创建和操作 PDF 文档。

Zend Framework 是“免费”的——用户可以根据 BSD 许可证条款免费下载和使用它，但同样，用户被期望通过邮件列表和 Wiki 等社区工具进行自我支持。对于寻求更高层次支持的公司和个人，Zend Technologies 提供了商业支持和培训包、Zend 工程师的咨询服务，以及可以帮助加速和优化 Zend Framework 开发的 PHP 开发和部署工具。对于许多业务机构而言，这种获取技术支持的能力（尽管需要付费）是选择 Zend Framework 作为其应用程序工具包的关键原因。此外还有 Zend Framework 认证计划，提供了衡量个人开发者 Zend Framework 技能的标准，并被整个行业认为是其 Zend Framework 能力的指标。

Zend Framework 为核心发行版包含的 60 多个组件提供了详尽的文档。这些文档包括一份包含 1000 多页的程序员指南；一份面向经验开发者的“快速上手”指南；详细的 API 文档；视频教程；网络研讨会以及知名 Zend 工程师的播客。这些丰富的学习材料可以显著降低新手和资深程序员的学习曲线，事实上，这也是 Zend Framework 超越竞争 PHP 框架的关键领域之一。

## Zend Framework 应用程序的运行环境

所有的 Zend Framework 应用程序都是 PHP 应用程序，可以在支持 PHP 的环境中运行。该环境通常至少包含以下三个组件：

- 基础操作系统，通常为 Linux 或 Microsoft Windows
- Web 服务器，通常为 Linux 上的 Apache 或 Microsoft Windows 上的 Internet 信息服务 (IIS)，用于拦截 HTTP 请求并直接提供或将其传递给 PHP 解释器执行
- PHP 解释器，用于解析和执行 PHP 代码，并将结果返回给 Web 服务器

通常还有第四个可选但非常有用的组件：

- 数据库引擎，例如 MySQL 或 PostgreSQL，用于存储应用程序数据、接受来自 PHP 层的连接并修改或检索数据库中的数据

图 1-1 展示了这些组件之间的交互。值得注意的是，Linux/Apache/PHP/MySQL 的组合在开发者中非常流行，并口俗称为“LAMP 栈”。该栈之所以流行，是因为它的所有组件都是开源项目，因此可以从互联网上免费下载。根据一般原则，使用这些组件进行个人用途或开发使用它们的应用程序都不会产生任何费用。然而，如果你打算编写商业应用程序，审查与这些组件相关的许可条款是一个明智之举；通常你可以在组件的网站上找到这些内容。

## 安装 Zend Framework

现在你已经对 Zend Framework 有了初步了解，让我们开始构建应用程序吧。作为必要的第一步，你必须首先确保你有一个运行良好的 Apache/PHP/MySQL 环境。本书的附录提供了获取这些组件的详细说明，以及测试你的开发环境以确保其正常运行的方法，因此请在准备好后再翻回这里。

下一步是将 Zend Framework 安装到你的开发环境中。访问 Zend Framework 官方网站：`http://www.zendframework.org`

访问 `.zend.com/` 并获取软件最新版本的副本。Zend Technologies 提供了两个版本的包：一个“极简”版本，仅包含标准库和命令行工具；以及一个“完整”版本，它包含了额外的文档、示例、单元测试和第三方工具包。建议使用完整版本。

一旦你下载了代码压缩包，请将其内容解压到文件系统上的临时区域。

```shell
shell> cd /tmp
shell> tar -xzvf ZendFramework-XX.tar.gz
```

你最终将得到类似于图 1-2 所示的目录结构。在所有目录中，你立即需要的两个是 `library/` 和 `bin/` 目录。`library/` 目录包含了所有的 Zend Framework 组件，而 `bin/` 目录包含了有助于初始化新项目和向其添加对象的命令行工具。

这两个目录需要按照以下方式进行操作：

应将 `library/` 目录的内容移动到你 PHP “包含路径”（include path）列表中的某个位置。在 UNIX/Linux 系统上，良好的可能位置是 `/usr/local/lib/php` 或 `/usr/local/share/php`。在 Windows 上，考虑使用你的 PHP 或 PEAR 安装目录，例如 `C:\Program Files\PHP` 或 `C:\Program Files\PHP\PEAR`。注意，如果目标目录尚未是你 PHP “包含路径”列表的一部分，你必须在继续之前将其添加。



应将`bin/`目录的内容移动到你系统可执行路径中的某个位置。如果包含 PHP 二进制文件的目录（通常 UNIX/Linux 上为`/usr/local/bin`，Windows 上为`C:\PHP`）已经是系统可执行路径的一部分，那么那里通常是使用的理想位置。或者，将`bin/`目录的内容移动到你认为方便的任何位置，始终记住将该位置添加到系统的可执行路径列表中。

**注意**

`bin/`目录包含三个脚本：用于 UNIX/Linux 的命令行界面`zf.sh`；用于 Windows 的命令行界面`zf.bat`以及主“工作”脚本`zf.php`。在 UNIX/Linux 上，你需要使用`chmod`命令将`zf.sh`脚本可执行；你可能也想对其重命名或设置别名以便于访问。

图 1-2：Zend Framework 发布压缩包的内容

![](img/222e7e58871b088cc6397852e1452b57_27_0.png)

以下是你可以用于执行这些任务的命令示例：

```
shell> cd ZendFramework-XX
shell> mv library/* /usr/local/lib/php/
shell> mv bin/* /usr/local/bin/
shell> chmod +x /usr/local/bin/zf.sh
shell> ln -s /usr/local/bin/zf.sh /usr/local/bin/zf
```

现在你应该能够从 Linux 和 Windows 的 shell 提示符中访问`zf`命令行脚本了。通过在你的 shell 提示符中输入以下命令来尝试：

```
shell> zf --help
```

如果一切运行正常，你将看到一个选项列表。图 1-3 描述了 Linux 上的输出。

一旦你安装了 Zend Framework 并且`zf`命令行脚本工作正常，你就可以开始使用它创建应用程序了。接下来的步骤将讨论如何完成此任务。

尝试此 1-1

图 1-3：`zf --help`命令的输出

![](img/222e7e58871b088cc6397852e1452b57_28_0.png)

## 理解应用需求

在深入研究代码之前，花几分钟理解你将在本书的前半部分将构建的示例应用程序是值得的。该应用程序是一个虚构商店的网站，专门向邮票爱好者和专业集邮收藏家出售稀有邮票。然而，与其他爱好商店不同，这个商店有一个有趣的转折：它作为一个在线邮票寻源机构，允许个人收藏者将他们可能出售的邮票照片和描述上传到中央数据库中，并让买家按国家、年份和关键词搜索此邮票数据库。如果匹配成功，商店将从卖家处购买邮票并转售给买家……自然地，会收取高额的佣金！

指定的网站管理员将可以直接访问上传的列表，并手动批准合适的列表显示在搜索结果中。管理员还将能够访问一个用于新闻和新闻稿的简单内容管理系统；这些信息可以通过网站访问，也可以通过 RSS 馈访问。为了增加趣味性，邮票数据库还可以通过 SOAP 接口可用，以便于与第三方应用程序集成。

听起来很酷？确实如此。它甚至有一个很酷的名字：邮票查询与研究引擎（Stamp Query and Research Engine），或者像它的朋友那样称为 SQUARE。

SQUARE 应用的设计涵盖了日常开发中遇到的：静态页面、输入表单、图像上传、登录保护面板、数据分页排序、多种输出类型和关键词搜索。实现这些功能需要理解表单处理、输入验证、会话管理、身份验证与安全、CRUD 操作、服务 API 以及与第三方库的集成。因此，应该是一个很好的起点。

一旦你安装了 Zend Framework 并且`zf`命令行脚本工作正常，你已经准备好用它开始创建应用程序了。接下来的步骤将讨论如何完成此任务。

让我们开始吧。进入 Web 服务器的根目录（通常是`/usr/local/lib/php`或`C:\PHP`），如果包含你 PHP 二进制文件的目录（通常 UNIX/Linux 上为`/usr/local/bin`，Windows 上为`C:\PHP`）已经是系统可执行路径的一部分，那么那里通常是使用的理想位置。或者，将`bin/`目录的内容移动到你认为方便的任何位置，始终记住将该位置添加到系统的可执行路径列表中。

应将`library/`目录的内容移动到你 PHP “包含路径”列表中的某个位置。在 UNIX/Linux 系统上，良好的可能位置是`/usr/local/lib/php`或`/usr/local/share/php`。在 Windows 上，考虑使用你的 PHP 或 PEAR 安装目录，例如`C:\Program Files\PHP`或`C:\Program Files\PHP\PEAR`。注意，如果目标目录尚未是你 PHP “包含路径”列表的一部分，你必须在继续之前将其添加。

## 创建应用程序目录

**注意**

`bin/`目录包含三个脚本：用于 UNIX/Linux 的命令行界面`zf.sh`；用于 Windows 的命令行界面`zf.bat`以及主“工作”脚本`zf.php`。在 UNIX/Linux 上，你需要使用`chmod`命令将`zf.sh`脚本可执行；你可能也想对其重命名或设置别名以便于访问。

## 创建应用程序骨架

一旦你安装了 Zend Framework 并且`zf`命令行脚本工作正常，你已经准备好用它开始创建应用程序了。接下来的步骤将讨论如何完成此任务。

## 创建骨架

下一步是初始化应用程序并创建所需的目录和文件。`zf`命令行脚本可以为你完成这一切——只需切换到并运行以下命令（见图 1-4）：

```
shell> zf create 骨架
```

一旦过程完成后，如图 1-5 所示，脚本将创建一个容器并填充一组文件。这是 Zend Framework 的默认目录结构。每个目录的用途如下：

- `application/`是主目录，包含了控制器、视图和模型。
- `library/`存放应用程序使用的第三方库。
- `public/`存放公共访问的内容，如 CSS 样式、JavaScript 和静态资源。
- `tests/`存放应用程序的单元测试。

图 1-4：`zf --help`命令的输出

![](img/222e7e58871b088cc6397852e1452b57_28_0.png)

## 添加 Zend Framework 库

在这一点，你必须做一个重要的决定。你必须决定是将 Zend Framework 与你的应用程序一起包含，还是让用户自行下载安装这些库。每个选项都有优缺点：

- 要求用户自行下载 Zend Framework 库可以确保他们始终可以使用最新代码（以及错误修复）。然而，对于初学者来说这个过程可能很难，而且如果新库与原始版本不兼容，可能会出现难以追踪的错误。
- 将 Zend Framework 与应用程序打包可以确保用户开箱即用。但会将用户锁定特定版本，使其难以升级到具有新功能或必要的错误修复的版本。

对于本书，我假设 Zend Framework 库将与应用程序一起打包。因此，使用下文的命令，将 Zend Framework `library/`目录的内容复制到`$APP_DIR/library/`。默认应用程序设置将在此处查找包含的库。

```
shell> cp -R /usr/local/lib/php/Zend library/
```

Zend Framework：入门指南

图 1-6

默认应用程序索引页

![](img/222e7e58871b088cc6397852e1452b57_32_0.png)

完成这些步骤后，打开你的 Web 浏览器并输入 URL `http://square.localhost/`来访问你刚刚设置的虚拟主机。如果你看到了 Zend Framework 的欢迎页面（如图 1-6 所示），请为自己鼓个掌，因为你刚刚成功构建并运行了一个完整的（尽管非常简单）的 Zend Framework 应用程序！

如上一节所示，`zf`命令行脚本允许你执行许多不同的操作。例如，切换到命令行提示符并执行以下命令：

```
shell> zf show version
```

第 1 章：介绍 Zend Framework

15

**问：我可以在共享主机环境中使用 Zend Framework 吗？在那种环境下，我可能对全局 PHP 配置指令（如 PHP 的“include path”）有有限或完全没有控制权。**

**答：可以，完全可以。有几种方法可以实现这一点：**

- 如果你只是担心在应用程序中使用 Zend Framework 类，你只需要将`library/Zend`目录复制到你的用户目录下，然后在你的应用程序脚本中使用`ini_set()`函数动态地将此位置添加到应用程序的 PHP include path 中。
- 如果你想使用`zf`命令行脚本，你还应该将`bin/`目录复制到你的用户目录下（与`library/`目录处于同一级）。然后你应该能够通过在脚本名前加上完整的文件系统路径来像往常一样调用`zf`命令行脚本。这之所以行得通，是因为如果在 PHP include path 中找不到 Zend Framework，`zf`命令行脚本还会在当前目录层次结构的上一层查找`library/Zend`目录，如果可用，则使用它。或者，你也可以通过设置环境变量`ZEND_TOOL_INCLUDE_PATH_PREPEND`为适当的位置，来显式地告诉`zf`命令行脚本去哪里寻找你的 Zend Framework 安装。

此命令显示当前安装的 Zend Framework 版本号。图 1-7 和图 1-8 分别展示了 Linux 和 Windows 上的输出。你也可以尝试以下命令来获取完整的`phpinfo()`信息：

```
shell> zf show phpinfo
```

`zf`命令行工具还提供了一种快速简单的方法来查看应用程序当前的“配置（profile）”。该配置包含应用程序当前内容的层级列表，并对其中的每个文件进行了描述，它是快速获取应用程序概览的极佳方法，无需手动深入到每个目录。

图 1-7

在 Linux 上运行`zf show version`命令的输出

![](img/222e7e58871b088cc6397852e1452b57_33_0.png)

图 1-8

在 Windows 上运行`zf show version`命令的输出

![](img/222e7e58871b088cc6397852e1452b57_34_0.png)

图 1-9

一个示例项目配置

尝试切换目录到`$APP_DIR`并执行以下命令来体验：

```
shell> zf show profile
```

图 1-9 展示了 Linux 上的输出。

17

本章对 Zend Framework 开发世界进行了浅显的介绍，向你介绍了该项目，并展示了它与其他竞争方案相比的一些独特特性和优势。它还引导你完成了 Zend Framework 的安装以及使用命令行工具启动新项目。当你进入下一章时，这些基础技能将非常有帮助，下一章将讨论核心应用程序开发概念，并带你开始构建基于框架的 Web 应用程序。

如果你想了解更多本章讨论的话题，你会发现以下链接有用：

- Zend Framework 官方网站，地址：`http://framework.zend.com/`
- Zend Framework 社区 wiki，地址：`http://framework.zend.com/wiki/`
- Zend Framework 使用统计数据，地址：`http://framework.zend.com/about/numbers`
- Zend Framework 案例研究，地址：`http://framework.zend.com/about/casestudies`
- Zend Framework 组件，地址：`http://framework.zend.com/about/components`
- Zend Framework CLI 工具，地址：`http://framework.zend.com/manual/en/zend.tool.framework.clitool.html`
- Zend Framework 文件系统布局，地址：`http://framework.zend.com/wiki/display/ZFDEV/Choosing+Your+Application%27s+Directory+Layout`
- Zend Framework 开发路线图，地址：`http://framework.zend.com/about/`

```php
// 用于插入或更新列表的代码

}

public function delete()
{

// 用于删除列表的代码

}

}

?>
```

当应用程序数据存储在数据库（如 MySQL、SQLite 或 PostgreSQL）中时，模型（models）可能会使用底层的数据库抽象层来处理管理数据库连接和执行 SQL 查询的任务。Zend Framework 包含一个数据库抽象层`Zend_Db`，它为许多不同的数据库系统提供了一个通用接口，而 Zend Framework 中的模型通常使用数据映射（Data Mapper）模式来表示。此外，将第三方模型（例如使用对象-关系映射（ORM）工具如 Doctrine 和 Propel 创建的模型）集成到 Zend Framework 应用程序中也非常容易。

如果说模型只关注访问和操作应用程序的原始数据，那么*视图（views）*只关注如何将这些数据呈现给用户。视图可以简单地被视为“用户界面层”，负责显示数据，但无法直接访问或操作数据。视图也可以接收来自用户的输入，但它们的责任仍然限于输入表单的外观和行为；它们并不负责处理、清洗或验证输入数据。

在前面讨论的分类广告应用背景下，视图将负责显示当前列表，并生成可以输入新列表的表单。例如，可能有一个视图用于显示特定类别下的所有最新列表，以及一个用于输入新列表的视图。在所有这些情况下，控制器（controller）和/或模型将处理检索和处理数据的任务，而视图将负责将这些数据处理成适合显示的格式，然后将其渲染给用户。

这里是一个用于显示最新列表的视图示例：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
<base href="/" />
</head>
<body>
<div id="header">
<div id="logo">
<img src="/images/logo.gif" />
</div>
</div>
<div id="content">
<h1>Recent listings</h1>
<?php foreach ($this->listings as $l): ?>
<div class="listing">
<h3 class="listing_title">
<a href="/listing/view/<?php echo $l->id; ?>">
<?php echo $l->title; ?>
</a>
</h3>
<span class="listing_content">
<?php echo $l->content; ?>
</span>
</div>
<?php endforeach; ?>
</div>
</body>
</html>
```

如此示例所示，视图通常表示为 PHP 脚本，其中包含了为了向用户正确渲染和显示输出所需的 HTML 代码或标记。这些脚本还可以包含用于动态数据的变量占位符；这些占位符的值由相应的控制器设置，并在渲染视图时插值到视图中。

在 Zend Framework 下，视图脚本由`Zend_View`组件渲染，该组件还为输出转义提供了辅助函数，并提供一组用于常见视图任务的“助手（helpers）”，例如导航、元标签创建和链接生成。此外，通过扩展`Zend_View_Interface`抽象类，将第三方模板引擎（如 Smarty 或 Savant）集成到 Zend Framework 应用程序中也非常容易。

## 控制器 (Controllers)

*控制器（Controllers）*是模型和视图之间的桥梁。它们使用模型更改应用程序数据，然后调用视图将结果显示给用户。控制器可以链接到多个视图，并可以根据任何时刻要显示的结果调用不同的视图。因此，控制器可以被视为“处理层”，负责响应用户操作、触发应用程序状态的变化，并将新状态显示给用户。

在前面讨论的应用背景下，控制器将负责读取和验证请求参数、使用模型函数保存和检索列表，并选择合适的视图来显示列表详情。例如，控制器会拦截对最新列表的请求，查询`ListingModel`模型获取最新条目列表，选择合适的视图，将条目插值到视图中并渲染视图。同样，如果用户选择添加新列表，控制器将选择并渲染一个输入视图，验证并清洗用户输入，使用`ListingModel`模型将清洗后的输入插入数据存储中，然后选择并渲染另一个视图以显示操作是否成功。

这里是一个结合了之前示例所示模型和视图的控制器示例：

```php
class ListingController
{

function indexAction()
{

// 初始化模型并
// 获取数据的代码

$listing = new ListingModel();
$matches = $listing->find(
array(
'date' => '-10 days',
'status' => 'published'
)
);

// 初始化视图并
// 用从模型返回的数据填充
```



```php
$view = new ListingView();

$view->listings = $matches;

echo $view->render('recent.php');

}
}
?>
```

如此示例所示，控制器充当模型和视图的中间节点。它们通过模型对应用程序数据进行操作，并使用视图显示操作结果。在 Zend Framework 下，控制器是 `Controller_Action` 类的子类，包含名为*动作（actions）*的方法，负责拦截请求并根据 URL 模式进行路由（*routing*）以满足请求（更多信息请见下文）。除了上述的三个核心组件外，Zend Framework 还引入了一些额外的想法来简化开发。这些将在后续章节中介绍。

## 模块 (Modules)

默认情况下，所有模型、控制器和视图都位于“default”模块中。然而，你可能希望根据应用程序的不同功能区域将模型、视图和控制器组合成自包含的“框”。例如，如果你的应用程序包含搜索、用户配置和新闻功能，你可以创建独立的“search”、“profile”和“news”模块，并在其中放置相应的模型、视图和控制器。

*模块（Modules）*提供了一种实现这种方法的方法。对于应用程序，Zend Framework 的默认路由器是模块感知的，允许你无需任何编程即可使用模块，且每个模块（默认模块外）都有自己的命名空间以防止冲突。

## 路由 (Routes)

*路由（Routes）*提供了用户请求与动作之间的链接。当用户请求一个应用程序 URL 时，前端控制器拦截该请求并根据模式决定调用哪个控制器和动作来完成请求。这种将请求路由到控制器的过程是应用程序执行的关键部分，并且支持复杂的配置。路由使用正则表达式进行匹配，并可以使用 XML 语法表示。

默认情况下，Zend Framework 包含了一些适用于小型应用程序的标准路由。这些标准路由假设 URL 遵循 `/module/controller/action` 的格式，并相应地引导用户请求。例如，请求 `http://application/auto/listing/index` 将自动映射到 auto 模块中的 `ListingController::indexAction`。注意控制器和动作名称遵循特定的大小写命名规范。

***注意***

Zend Framework 的路由子系统会对不符合 `/module/controller/action` 格式的路由自动应用默认值。关于这些默认值以及对 URL 映射到控制器和动作的影响的详细讨论，请参见“理解组件交互”章节。

## Zend Framework：入门指南

将页眉、页脚或全局导航组件分到单独的文件中，这些文件可以独立于单个视图进行编辑和维护。

应用程序拥有多个布局是非常常见的情况。例如，你可能希望为用户展示一种界面，为管理员展示另一种，或者你可能希望允许用户通过从一组预定义的界面主题中选择来定制他们对应用程序的体验。布局（Layouts）使得这些以及其他模板选项实现变得相当容易。

***注意***

你将在本章的稍后部分开始处理模块、自定义路由和布局。

## 理解组件交互

如果你将 Zend Framework 应用比作一个马戏团（这个比喻通常非常贴切），那么前置控制器（front controller）就是团长，负责指挥各项节目就绪，并确保观众满意。本节将详细检查它的角色，并在拦截和满足应用程序资源请求的步骤背景下对其进行说明。

图 2-1 展示了请求通过典型 Zend Framework 应用的流程。

| 前置控制器 | 请求 | 数据库 | 路由器 | 动作 | 视图 | 模型 | 布局 | 响应 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |

![](img/222e7e58871b088cc6397852e1452b57_44_0.png) ![](img/222e7e58871b088cc6397852e1452b57_44_1.png) ![](img/222e7e58871b088cc6397852e1452b57_44_2.png) ![](img/222e7e58871b088cc6397852e1452b57_44_3.png) ![](img/222e7e58871b088cc6397852e1452b57_44_4.png) ![](img/222e7e58871b088cc6397852e1452b57_44_5.png) ![](img/222e7e58871b088cc6397852e1452b57_44_6.png) ![](img/222e7e58871b088cc6397852e1452b57_44_7.png)

图 2-1 模型、视图和控制器之间的交互

## 第 2 章：使用模型、视图、控制器和路由

作为负责拦截客户端请求并将其重定向到适当目标进行响应的控制器，前置控制器在请求通过应用程序的整体流程中起着关键作用。

1. 当请求到达时，Web 服务器的 `.htaccess` 文件会自动将其重写为标准格式，并将其传递给 `index.php` 脚本。该脚本设置应用程序环境，读取应用程序配置文件，并创建一个前置控制器的实例。

2. 前置控制器检查请求并确定 URL 的关键组件。它随后尝试将请求路由到适当的控制器和动作。为了执行此路由操作，前置控制器将同时检查默认路由和自定义路由，并利用模式匹配技术为请求选择合适的目标。

3. 如果找到匹配项，前置控制器将控制权交给相应的控制器和动作。一旦被调用，该动作将使用一个或多个模型对应用程序状态进行更改。它还会选择要显示的视图并设置任何所需的视图属性。一旦动作完成，选定的视图将渲染其输出，根据需要将其封装在布局中。该输出随后将传回给请求客户端。

4. 如果应用程序定义的任何路由都不匹配请求，则会抛出异常并调用错误控制器和错误动作。根据异常的参数，错误动作将渲染一个包含失败通知的视图。该输出随后将传回给请求客户端。

***注意***

在请求处理过程中生成的任何未捕获异常都将调用错误控制器和相应的动作。这将产生一个包含失败通知的视图，并传回给请求客户端。

如前所述，路由子系统会自动将格式为 `/module/controller/action` 的 URL 映射到相应的模块、控制器和动作。例如，要访问“auto”模块中的 `ListingController::saveAction`，你需要请求 URL `http://application/auto/listing/save`。同样，要访问“content”模块中的 `NewsController::editAction`，你需要请求 URL `http://application/content/news/edit`。

如果路由子系统收到的请求不符合 `/module/controller/action` 格式，它会自动应用以下默认设置：

- 对于没有模块名的请求，路由子系统会自动假设模块为“default”（默认）模块。
- 对于没有控制器名的请求，路由子系统会自动假设控制器为所选模块的 `IndexController`。
- 对于没有动作名的请求，路由子系统会自动假设动作为所选模块的 `IndexAction`。

为了更好地理解这些设置是如何运作的，在实践中，请考虑以下示例：

- 对于没有模块名的请求，路由子系统会自动假设模块为“default”模块。（`ContactController::send`）
- 对于没有控制器名的请求，路由子系统会自动假设控制器为所选模块的 `IndexController`。（`PostController::index`）
- 对于没有动作名的请求，路由子系统会自动假设动作为所选模块的 `IndexAction`。（`NewsController::index`）

## Zend Framework：入门指南

### 默认索引页背后的原理

从这些标记中看出，只要你正确地命名并放置控制器、动作和视图，你实际上不需要做太多工作。框架将根据其默认路由自动定位并执行文件，而无需任何手动干预。在本章及本书后续内容，你将更多地了解如何利用这些 Zend Framework 标准规范的优势，从而减少运行应用程序所需的手动代码。

## 理解模块化布局

在上一章中，你看到了 `zf` 命令行工具如何为你的新 Zend Framework 创建目录结构。在初始状态下，该结构仅包含运行基础应用程序所需的目录。随着你为应用程序添加新功能，你还需要扩展此基础结构并创建额外的目录来存储不同类型的数据。

为了更好地理解，请考虑图 2-3，它展示了 Zend Framework 应用的完整目录结构。

图 2-3 所示的每个目录都有特定的用途，如表 2-1 所示。

`$APP_DIR/application/modules/` 目录需要特别说明。

# 第 2 章：模型、视图、控制器和路由的操作

`modules` 目录用于存储应用程序模块，每个模块表示为 `$APP_DIR/application/modules/` 下的子目录。每个模块目录的内部结构与全局 `$APP_DIR/application/` 目录镜像，如图 2-4 所示。

这种目录结构区分了全局应用程序控制器、视图和模型（存储在 `$APP_DIR/application/` 层次结构下）以及模块特有的控制器、视图和模型（存储在 `$APP_DIR/application/modules/` 层次结构下）。

从开发角度来看，选择哪个位置来存放应用程序代码完全是主观的。没有所谓的唯一“正确”方法，因此你可以根据你认为适合应用程序需求和结构的方法，选择将代码存储在全局目录、每个模块目录中，或者两者的混合组合中。

图 2-3 Zend Framework 应用程序的推荐目录结构 ![](img/222e7e58871b088cc6397852e1452b57_49_0.png)

表 2-1：Zend Framework 应用程序中的关键目录

| 目录 | 描述 |
| :--- | :--- |
| `$APP_DIR/application` | 主应用程序目录 |
| `$APP_DIR/application/controllers` | 全局控制器 |
| `$APP_DIR/application/views` | 全局视图 |
| `$APP_DIR/application/models` | 全局模型 |
| `$APP_DIR/application/configs` | 全局配置数据 |
| `$APP_DIR/application/layouts` | 全局布局 |
| `$APP_DIR/application/modules` | 模块 |
| `$APP_DIR/library` | 第三方库和类 |
| `$APP_DIR/public` | 主公共访问目录 |
| `$APP_DIR/public/css` | CSS 样式表 |
| `$APP_DIR/public/js` | JavaScript 程序代码 |
| `$APP_DIR/public/images` | 应用程序图像 |
| `$APP_DIR/tests` | 单元测试 |
| `$APP_DIR/temp` | 临时数据 |

32 Zend Framework：初学者指南

图 2-4 Zend Framework 模块的推荐目录结构 ![](img/222e7e58871b088cc6397852e1452b57_50_0.png)

尽管如此，这些章节描述的 SQUARE 示例应用程序大量使用了模块，本书通常建议在 Zend Framework 应用程序开发中使用模块化，原因如下：

- 将代码组织成模块可以产生结构化的代码树，因为与特定功能或一组功能相关的所有控制器、视图和模型都存储在同一个目录树中。基于模块的目录布局使得应用程序内部的逻辑分离区域一目了然，无需额外文档，从长远来看更具维护性。
- 将代码组织成模块鼓励创建更健壮、更可扩展的软件。模块可以结构为独立的包，拥有自己的控制器、视图和模型。因此，模块可以被视为可重用的组件，可以插入到现有应用程序中快速为其提供新功能。

当你配合 Zend Framework 的默认路由使用模块时，需要在 URL 请求中包含模块名称，格式为 `/module/controller/action`。如果路由子系统接收到的请求不包含模块名称，它会自动查找它认为的“默认”模块——即全局应用程序目录 `$APP_DIR/application/`。

当应用程序在 `$APP_DIR/application/modules/` 层次结构中也包含额外模块时，这种行为会导致应用程序 URL 出现混乱和某种不一致。因此，在遵循模块化目录结构时，显式地为“默认”模块创建一个目录（路径为 `$APP_DIR/application/modules/default`），并将之前存储在 `$APP_DIR/application/` 层次结构中的控制器、视图和模型移动到 `$APP_DIR/application/modules/default/` 层次结构中。

## 使用模块化目录布局

如上一节所述，模块化目录布局强制了一致性并生成了更易管理的代码树。以下步骤讨论了如何为第 1 章创建的示例应用程序采用这种布局，作为开始应用程序开发的先备工作。

### 尝试练习 2-1：创建默认模块

33 第一步是创建 `$APP_DIR/application/modules/` 目录，然后在该目录下创建一组子目录用于默认模块及其控制器和视图。`zf` 命令行工具不会创建这些目录，因此需要手动执行此任务。

```shell
cd /usr/local/apache/htdocs/square/application
mkdir modules
mkdir modules/default
```

接下来，将 `$APP_DIR/application/` 中现有的模型、控制器和视图移动到 `$APP_DIR/application/modules/default/`：

```shell
mv controllers modules/default/
mv views modules/default/
mv models modules/default/
```

#### 更新应用程序配置文件

下一步是更新位于 `$APP_DIR/application/configs/application.ini` 的全局应用程序配置文件。为了告诉 Zend Framework 如何解析模块，请用文本编辑器打开该文件，并在资源（resources）部分添加以下行：

```ini
frontController.moduleDirectory = "modules"
```



完成上述步骤后，尝试通过 `http://localhost/` 和 `http://localhost/default/index` 访问首页。如果一切顺利，你应该看到默认索引页。

## 理解主布局和自定义路由

此时，你已经对 Zend Framework 的原理有了足够的了解，可以开始编写代码了。后续章节将引导你创建自定义页面、设置主布局以及构建自定义路由。

### 常见问题解答

**问：为什么 `http://localhost/` 和 `http://localhost/default/index` 会产生相同的输出？**

答：Zend Framework 子系统会对不符合标准 `/module/controller/action` 格式的路由应用某些默认设置。简单来说，在缺失模块名称的情况下，它假设为“default”模块；在缺失控制器和动作的情况下，它假设为 `IndexController` 的 `indexAction` 方法。由于这些默认替换，`http://localhost/` 会被重写为 `http://localhost/default/index`，并定向到默认模块的 `IndexController`。

**问：Zend Framework 中控制器、动作和视图的命名规范是什么？**

答：Zend Framework 对控制器和动作使用驼峰命名法。控制器名称使用大驼峰并以 `Controller` 结尾（例如：`IndexController`、`StaticContentController`、`FunkyChickenController`），而动作名称使用小驼峰并以 `Action` 结尾（例如：`indexAction`、`displayPostAction`、`redButtonAction`）。对于“default”模块以外的模块，控制器名称必须额外加上模块名前缀（例如：`News_IndexController`、`Catalog_EntryController`）。

视图脚本根据相应的控制器和动作命名。通常，视图脚本存储在与控制器名称（不带 `Controller` 后缀）对应的目录中，文件名与动作名称（不带 `Action` 后缀）对应。因此，`ExampleController` 中 `clickAction` 的视图脚本位于 `/views/scripts/example/click.phtml`。控制器或动作名称中的多个单词在相应的视图脚本路径中使用连字符或点表示。因此，`ShoppingCart` 中 `displayItemAction` 的视图脚本位于 `/views/scripts/shopping-cart/display-item.phtml`。

为了防止命名冲突，Zend Framework 还允许使用自定义命名空间，将其作为对象或类名前缀。这些命名空间可以注册到 Zend Framework 自动加载器中，以便按需要自动加载相应的定义。你将在第 3 章看到相关的示例。

## 第 2 章：使用模型、视图、控制器和路由

### 更新应用程序索引页

现在，虽然 `zf` 命令行工具创建的默认欢迎页确实很漂亮，但它并不是你希望应用程序用户在生产环境中看到的界面。那么，用自定义的欢迎消息和关于应用程序的描述性信息来更新它又如何？

你已经知道，应用程序索引页是由“default”模块的 `IndexController::indexAction` 提供的。在模块化布局下，与此控制器和动作对应的视图位于 `$APP_DIR/application/modules/default/views/scripts/index/index.phtml`。在文本编辑器中打开此文件，并将其内容替换为以下标记：

```html
<h2>欢迎光临！</h2>

<p>欢迎来到 SQUARE，这是我们为稀有邮票设计的尖端 Web 搜索引擎。</p>

<p>我们的目录中拥有丰富的邮票收藏供您享览，我们还列出了来自全国各地个人收藏家的**成千上万枚邮票**。如果您发现了自己喜欢的物品，请与我们联系，我们将尽力为您获取。毋庸置疑地说，所有通过我们购买的邮票都带有真伪鉴定证书，并且享有**我们独特的60天退款保证**。</p>

<p>SQUARE 应用程序的设计旨在尽可能用户友好。请使用上方菜单中的链接进行导航并开始搜索。</p>
```

保存更改并重新访问 `http://square.localhost/` 上的应用程序索引页。你应该能看到一个修改后的索引页，如图 2-5 所示。

图 2-5：更新后的应用程序索引页

### 设置主布局（Master Layout）

应用程序索引页现在显示了相关内容，但离视觉美观还有很大距离。因此，下一步是通过添加一些图像和导航来赋予它一些视觉吸引力。这些元素是应用程序所有页面共有的，因此，尽管你可以将它们添加到应用程序的每个视图中，但它们更适合放置在主布局中，然后主布局可以包裹在每个视图周围。使用布局不仅更节省时间，而且布局存储在从多个视图访问的单个文件中，随着应用程序的演进，也更容易进行更改。

要为应用程序设置主布局，请执行以下步骤。

#### 创建布局模板文件

第一步是创建 `$APP_DIR/application/layouts/` 目录，根据 Zend Framework 推荐的目录结构，这是布局文件的默认位置。

```
shell> cd /usr/local/apache/htdocs/square/application
shell> mkdir layouts
```

在此目录中，创建一个包含以下标记的新文本文件：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">

<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
<base href="/" />
<link rel="stylesheet" type="text/css" href="/css/master.css" />
</head>

<body>
<div id="header">
<div id="logo">
<img src="/images/logo.gif" />
</div>
<div id="menu">
<a href="#">首页</a>
<a href="#">服务</a>
<a href="#">联系</a>
</div>
</div>

<div id="content">
<?php echo $this->layout()->content ?>
</div>

<div id="footer">
<p>
创建于 <a href="http://framework.zend.com/">Zend Framework</a>。根据 <a href="http://www.creativecommons.org/">Creative Commons</a> 许可使用。
</p>
</div>
</body>

</html>
```

将此文件保存为 `$APP_DIR/application/layouts/master.phtml`。

你会发现主布局还使用了两个额外的资源——一个 CSS 样式表和一个 logo 图像。这些文件需要位于应用程序的公共区域，以便连接客户端能够通过 HTTP 获取它们。因此，同样创建 `$APP_DIR/public/css/` 和 `$APP_DIR/public/images/` 目录，并将必要的资源复制到这些位置。你可以在本章的代码存档中找到这些资源，该存档可以从本书的配套网站 `http://www.zf-beginners-guide.com/` 下载。

#### 更新应用程序配置文件

下一步是更新全局应用程序配置文件，该文件位于 `$APP_DIR/application/configs/application.ini`，指定布局目录的位置以及渲染应用程序视图时使用的默认布局名称。在文本编辑器中打开该文件，并在 `[production]` 部分添加以下指令：

```ini
resources.layout.layoutPath = APPLICATION_PATH "/layouts"
resources.layout.layout = master
```

现在，当你再次访问应用程序索引页时，你应该看到你新布局的完美状态，如图 2-6 所示。

### 使用自定义路由

自定义路由使得将应用程序 URL 映射到特定的模块、控制器和动作成为可能，当 Zend Framework 的默认路由被证明不可用时，这种方法特别有用。

当 Zend Framework 的默认路由被证明不足或具有局限性时，自定义路由就派上了用场。为了说明，假设你想让应用程序 URL `/home` 重定向到“default”模块的 `IndexController::indexAction`，只需更新 `$APP_DIR/application/configs/application.ini` 文件并添加以下路由项：

```ini
resources.router.routes.home.route = /home
resources.router.routes.home.defaults.module = default
resources.router.routes.home.defaults.controller = index
resources.router.routes.home.defaults.action = index
```

路由项通常包含 `route`、`module`、`controller` 和 `action` 属性。在保存更改后，尝试在浏览器中访问 `http://square.localhost/home`。如果一切正常，你应该看到应用程序索引页，如图 2-6 所示。

**提示**
路由名称非常有用，因为你可以在视图中使用 `url()` 辅助器来自动生成 URL。例如，在视图内部调用 `$view->url(array(), 'home')` 将自动生成字符串 `/home`。

图 2-6：带有自定义布局的应用程序索引页

### 提供静态内容

在之前的章节中，你的活动仅限于修改现有的控制器和视图。然而，随着开发的进行，你会发现有必要创建新的控制器、动作和视图来封装功能。不需要担心，因为当你需要添加新功能时，有一个可以遵循的标准流程。

这些步骤将在后续章节说明，将指导你完成一个提供静态内容的 `StaticController`。

## 定义自定义路由

第一步是为静态页面定义一个基础路由。为了简单起见，我们假设所有内容页面 URL 将以 `/content/xx` 的形式存在，其中 `xx` 是指示页面名称的变量。要为此类 URL 设置路由，请在 `$APP_DIR/application/configs/application.ini` 文件中添加以下路由定义：

```ini
resources.router.routes.static-content.route = /content/:page
resources.router.routes.static-content.defaults.module = default
resources.router.routes.static-content.defaults.controller = static-content
resources.router.routes.static-content.defaults.action = display
```

此路由比你之前看到的复杂一点，因为它包含一个变量占位符。

**尝试 2-2**

**问：为什么布局存储在全局级别，而不是模块级别？**

**答：** 在 Web 应用程序中，不同模块的视图共享同一个公共布局是非常常见的。因此，Zend Framework 的默认目录结构建议将布局放在全局（或应用程序）级别的 `$APP_DIR/application/layouts/` 下，而不是 `$APP_DIR/application/modules/` 层级下。

尽管如此，如果你的应用程序结构使得每个模块都使用不同的布局，你可以将布局文件移动到模块级别，并编写自定义插件根据访问的模块动态更改布局。你可以在章末的链接中找到关于如何执行此操作的详细讨论。

**提问专家**
（待续）

Zend Framework：学者指南

将 URL 转换为一个可以在控制器内部访问的变量。这意味着，例如，如果客户端请求了 URL `/content/hello-world`，路由子系统将自动捕获 URL 段“hello-world”并将其存储在名为 `page` 的请求变量中。

## 定义控制器（Controller）

我们为什么需要捕获 URL 的最后段并将其存储为请求变量呢？这个问题将在下一段中给出解答，但在到达那里之前，让我们先创建默认（default）模块的 `StaticContentController`，按照惯例，它应该位于 `$APP_DIR/application/modules/default/controllers/StaticContentController.php`。创建此文件并填入以下代码：

```php
<?php

class StaticContentController extends Zend_Controller_Action
{
    public function init()
    {
    }

    // 显示静态视图
    public function displayAction()
    {
        $page = $this->getRequest()->getParam('page');

        if (file_exists($this->view->getScriptPath(null) .
        "/" . $this->getRequest()->getControllerName() .
        "/$page." . $this->viewSuffix)) {
            $this->render($page);
        } else {
            throw new Zend_Controller_Action_Exception('Page not found', 404);
        }
    }
}
```

该控制器暴露了一个单一的 action `displayAction()`，它负责使用请求对象的 `getParam()` 方法读取由路由子系统设置的 `page` 变量。然后它会尝试寻找与该变量值匹配的视图脚本。如果找到了匹配的视图脚本，将对其进行渲染并发送给客户端。例如，如果客户端请求的 URL 是 `/content/hello-world`，则对 `$request->getParam('page')` 的调用将返回值“hello-world”，因此该 action 将尝试渲染一个名为 `$APP_DIR/application/modules/default/views/scripts/static-content/hello-world.phtml` 的视图。

如果找不到匹配的视图，则会抛出 404 异常并向前传递给默认异常处理器，由该处理器将其格式化为可读的错误页面并显示给客户端。

## 第 2 章：与模型、视图、控制器和路由工作

### 定义视图（View）

下一步（也是最后一步）是为上一步创建的控制器和 action 创建相应的视图。在大多数情况下，视图名称将基于控制器和 action 名称。但在这种情况下，该 action 是一个通用的显示 action，它从 URL 请求接收视图名称作为变量。因此，为了定义一个可以通过 URL `/content/services` 访问的静态“Services”页面，请在 `$APP_DIR/application/modules/default/views/scripts/static-content/services.phtml` 创建一个文件并填入一些内容，如下所示：

```html
<h2>Services</h2>
<p>我们提供多项服务，包括采购、估值和邮购销售。请联系我们以获取更多信息。</p>
<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
```



Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

同样，为了定义一个可以通过 URL `/content/about-us` 访问的“About Us”页面，创建一个名为 `$APP_DIR/application/modules/default/views/scripts/static-content/about-us.phtml` 的文件并填入一些内容，如下所示：

```html
<h2>About Us</h2>

<p>自自1927 年以来一直从事邮票采购和销售业务，因我们的专业知识和整个行业的网络而闻名。我们鼓励您使用上面的链接了解更多关于我们的信息。</p>

<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>

<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
```

**咨询专家**

**Q：为什么本章中的所有类定义都没有包含 PHP 结束标签？**

**A：** 根据 Zend Framework 的编码标准，仅包含 PHP 代码的文件不应包含结束标签 `?>`，因为如果你使用的文本编辑器自动输出了它，可能会导致 HTTP 响应出现头部问题。

### 更新布局（Master Layout）

为了定义可以通过 URL `/content/about-us` 访问的“About Us”页面，创建一个 `$APP_DIR/application/modules/default/views/scripts/static-content/about-us.phtml` 的文件并填入一些内容，如下所示：

（此处内容同上文，省略避免重复）

最后，通过应用这些功能，更新 `master.phtml`：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN">

<html lang="en">

<head>

    <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>

    <base href="/" />

    <link rel="stylesheet" type="text/css" href="/css.css" />

</head>

<body>

    <div id="header">

        <div id="logo"><img src="/images/logo.gif" /></div>

    </div>

    <div id="menu">

        <a href="<?php echo $this->url(array()); ?>">HOME</a>

        <a href="<?php echo $this->url(array('services')); ?>">SERVICES</a>

        <a href="#">CONTACT</a>

    </div>

    <div id="content">

        <?php echo $this ?>

    </div>

    <div id="footer">

        <p>Created with <a href="http://framework.zend.com/">Zend Framework</a>. Licensed under <a href="http://www.creativecommons.org/">Creative Commons</a>.</p>

    </div>

</body>

</html>
```

在这里，`url()` 方法被用于生成 `/home` 和 `/services` 的 URL。该助手接受两个参数——键值对数组和路由名称——并在视图渲染时生成 URL 字符串。

**注意**

值得注意的是，在 Zend Framework 中提供静态页面实际上有一种更简单的方法：你可以将它们放在 `$APP_DIR/public/` 目录下作为 HTML 文件并手动链接。但是，这些页面将无法使用 Zend Framework 的任何内置功能，如全局布局、路由、缓存或安全，因此这种方法通常不被推荐。

### 总结

现在你已经完成了本章，你应该对 Zend Framework 应用程序的运行有更深入的理解。本章从模型-视图-控制器模式开始，解释了模型、视图和控制器是什么，以及它们如何交互产生逻辑分离的分层应用程序。它还引入了一些重要的概念，如模块、路由、布局和前端控制器，并解释了用户请求在应用程序环境中是如何路由和处理的。最后，它将这些理论应用于现实，通过开始自定义和增强上一节末尾创建的测试应用程序。

SQUARE 示例应用程序仍处于早期阶段：它有自定义的布局，知道如何处理模块，并可以提供静态内容。这看起来不多，但实现这些基本功能已经帮助你理解了基于 Zend Framework 开发的主要原理，并为后续章节的高级材料奠定了基础。

要了解更多关于本章讨论的主题，请访问以下链接：

- [模型-视图-控制器的架构](https://en.wikipedia.org/wiki/Model-view-controller)
- [Zend Framework MVC 实现](http://framework.zend.com/docs/quickstart)
- [Zend Framework 路由](http://framework.zend.com/manual/en/zend.controller.router.html)
- [Zend Framework 前端控制器](http://framework.zend.com/manual/en/zend.controller.front.html)
- [Zend Framework 布局引擎](http://framework.zend.com/manual/en/zend.layout.html)

## 第 2 章：与模型、视图、控制器和路由一起工作

45

关于使用 Zend Framework 构建模块化应用的讨论（Jeroen Keppens），见：**http://blog.keppens.biz/2009/06/create-modular-application-with-zend.html**

在 Zend Framework wiki 和论坛中关于使用每个模块布局的讨论，见：**http://framework.zend.com/wiki/display/ZFPROP/Zend_Layout** 和 **http://www.zfforums.com/zend-framework-components-13/model-view-controller-mvc-21/modules-layouts-2645.html**

Zend Framework 目录布局，见：**http://framework.zend.com/wiki/display/ZFPROP/Zend+Framework+Default+Project+Structure+-+Wil+Sinclair**

Zend Framework 编码规范，见：**http://framework.zend.com/manual/en/coding-standard.html**

# 第 3 章：处理表单工作

47

48

Zend Framework：初学者指南

**核心技能与概念**

- 学习编程创建表单和表单元素
- 理解如何过滤和验证用户输入
- 保护表单免受跨站请求伪造（CSRF）攻击和垃圾邮件机器人
- 控制表单元素和错误信息的显示
- 创建一个可工作的联系表单

在数一章中，你学习了 Zend Framework 如何实现模型-视图-控制器（MVC）模式，并查看了示例应用程序的内部结构以了解其工作原理。你还开始通过采用模块化目录结构、添加主布局，以及为静态内容创建自定义控制器、视图和路由，来充实示例应用程序的完善。

现在，虽然你完全可以使用 Zend Framework 来提供静态内容，但这样做就像是用推土机去推倒一叠塑料积木。虽然没什么能阻止你这样做，但这并不是推土机的设计初衷，而且你可能还会面临严厉的质问：为什么你的客厅里会有一台推土机！Zend Framework 也是如此，它旨在为复杂的 Web 应用开发任务提供稳健、优雅且可扩展的解决方案。任务越复杂，就越适合该框架的力量和灵活性……而且你在推倒它时会玩得开心！

在本章中，你将学习 Zend Framework 如何简化最常见的应用开发任务之一：创建 Web 表单和处理用户输入。你还将应用这些知识，通过创建一个联系表单为 SQUARE 示例应用程序添加一些交互性。那么，就不多说话了，让我们直接开始吧！

### 了解表单基础

为了演示 Zend Framework 如何帮助你处理表单，一个简短但具有说明性的示例就足够了。如果你像大多数 PHP 开发者一样，那么很有可能在职业生涯的某个时刻写过像下面这样的表单处理脚本：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">

<head>

</head>

<body>

<h2>创建创建项目</h2>

<?php

if (!isset($_POST['submit'])) {

    // 没有 POST 提交，显示表单

?>

<form method="post" action="/item/create">

    <table>

        <tr>

            <td>项目名称：</td>

            <td><input type="text" name="name" size="30" />

        </tr>

        <tr>

            <td>项目数量：</td>

            <td><input type="text" name="qty" size="3" />

        </tr>

        <tr>

            <td colspan="2">

                <input type="submit" name="submit" value="提交" />

            </td>

        </tr>

    </table>

</form>

<?php

} else {

    // POST 提交，验证输入

    if (trim($_POST['name']) == '') {

        die('错误: 缺失值 - 项目名称');

    }

    if (trim($_POST['qty']) == '') {

        die('错误: 缺失值 - 项目数量');

    }

    if ($_POST['qty'] <= 0) {

        die('错误: 无效的值 - 项目数量');

    }

    // 处理输入

    // 例如：保存到数据库

    // 尝试连接

    try {

        $pdo = new PDO('mysql:dbname=test;host=localhost', 'user', 'pass');

        // 创建并执行 INSERT 查询

        $name = $pdo->quote($_POST['name']);

        $qty = $pdo->quote($_POST['qty']);

        $sql = "INSERT INTO shoppinglist (name, qty) VALUES ($name, $qty)";

        $pdo->exec($sql) or die("错误: " . implode(":", $pdo->errorInfo()));

        // 关闭连接

        unset($pdo);

        // 显示成功消息

        echo '感谢您的提交';

    } catch (Exception $e) {

        die("错误: " . $e->getMessage());

    }

}

?>

</body>

</html>
```

这里并没有什么聪明或复杂的地方。这个脚本被分为两个部分，通过一个条件测试分隔，该测试检查 `$_POST` 变量以确定表单是否提交。前半部分显示包含两个字段和一个提交按钮的输入表单；后半部分验证输入以确保其格式正确，然后对其进行转义并插入数据库。

图 3-1 展示了表单的样子。

现在，虽然你刚刚看到的脚本和通用方法在实践中可以运行，但不可否认它存在几个问题：

- 同一个脚本文件同时包含了 HTML 界面元素和 PHP 业务逻辑。正如在前一章中讨论的，这既看起来很凌乱又难以维护。也很难在表单之间强制一致性，因为生成每个表单所需的代码是高度定制的。
- 每当你向脚本前半部分的表单中添加一个新字段时，你都需要脚本的后半部分添加相应的验证测试集和错误信息。这非常烦人且通常是重复的；没有办法可以从其他表单中复用代码（除非你一开始就有远见地将它们封装成类）。结果是，你经常会编写处理表单的相似操作。

Zend Framework 包含了一组组件，统称为 Zend Form，它解决了这些问题。为了说明这一点，考虑以下示例，它使用 Zend Form 来产生等于之前脚本的结果：

```php
<?php

class Form_Item_Create extends Zend_Form

{

    public function init()

    {

        // 初始化表单

        $this->setAction('/item/create')

             ->setMethod('post');

        // 创建名称文本输入

        $name = new Zend_Form_Text('name');

        $name->setLabel('项目名称:')

             ->setOptions(array('size' => '30'))

             ->setRequired(true)

             ->addValidator('NotEmpty')

             ->addValidator('Alpha')

             ->addFilter('StringTags');

        // 创建数量文本输入

        $qty = new Zend_Form_Text('qty');

        $qty->setLabel('项目数量：')

            ->setOptions(array('size' => '3'))

            ->setRequired(true)
```



## 第 3 章：表单操作

### 创建表单和表单元素

通过上一节，你已经知道`Zend_Form`提供了一个面向对象的 API，用于生成表单和验证用户输入。在`Zend_Form`的方法下，*表单*被表示为`Zend_Form`基类的实例，或继承自`Zend_Form`基类的对象。该基类暴露了许多方法来控制表单的操作，包括用于设置表单动作 URL 的`setAction()`方法和用于设置提交方式的`setMethod()`方法。此外还有一个可以捕获所有属性的`setAttribs()`方法，允许你设置其他表单属性。以下是使用这些方法的示例：

```php
<?php
class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/my/action')
            ->setAttribs(array(
                'class' => 'form',
                'id' => 'example'
            ))
            ->setMethod('post');
    }
}
```

*表单元素*通过实例化相应的`Zend_Form_Element_*`类对象、通过类方法设置元素属性，然后使用`addElement()`方法将其附加到表单来实现。以下是在表单中添加文本输入框和提交按钮的示例：

```php
<?php
class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/my/action')
            ->setAttribs(array(
                'class' => 'form',
                'id' => 'example'
            ))
            ->setMethod('post');

        // 创建标题的文本输入
        $title = new Zend_Form_Element_Text('title');
        $title->setLabel('Title:')
            ->setOptions(array(
                'size' => '35'
            ));

        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit', array(
            'label' => 'Submit',
            'class' => 'submit'
        ));

        // 将元素附加到表单
        $this->addElement($title)
            ->addElement($submit);
    }
}
```

元素对象可以通过向对象构造函数传递值或通过使用具名对象方法进行配置。在上一个示例中，文本输入元素的对象构造函数在构造时传递了元素名称，然后使用`setLabel()`和`setOptions()`方法分别设置标签和显示属性。另一方面，提交按钮直接在对象构造函数中配置，它将一个选项数组作为第二个参数传递进去。

**提示**

你还可以使用`setDescription()`方法为表单字段添加描述。如果你愿意，也可以使用`createElement()`方法创建表单元素，将元素类型作为方法的第一个参数传递。以下是一个示例，它与上一个示例等效：

```php
<?php
class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/my/action')
            ->setAttribs(array(
                'class' => 'form',
                'id' => 'example'
            ))
            ->setMethod('post');

        // 创建标题的文本输入
        $title = $this->createElement('text', 'title', array(
            'label' => 'Title:',
            'size' => 35,
        ));

        // 创建提交按钮
        $submit = $this->createElement('submit', 'submit', array(
            'label' => 'Submit',
            'class' => 'submit'
        ));

        // 将元素附加到表单
        $this->addElement($title)
            ->addElement($submit);
    }
}
```

**提示**

在本章的许多代码段中，你将看到*方法链式调用*的示例，其中一个方法似乎调用了另一个方法。这是 Zend Framework “流式接口”的一个示例，它提供了一种便捷的快捷方式，能够用最少的额外代码来配置表单对象。最终结果的可读性也显著提高。你可以在本章末的链接中阅读更多关于流式接口的内容。

#### 操作表单元素

默认情况下，Zend Framework 自带了 16 种表单元素的定义，从简单的文本输入元素到更复杂的多选列表，学习关于它们的信息是有用的。表 3-1 列出了这 16 种元素列表及其对应的类名。接下来的章节将详细介绍这些元素。

#### 文本和隐藏字段

文本输入字段、密码输入字段和较大的文本输入区域分别由`Zend_Form_Element_Text`、`Zend_Form_Element_Password`和`Zend_Form_Element_Textarea`类表示，而隐藏表单字段由`Zend_Form_Element_Hidden`类表示。下面的示例演示了这些元素的用法：

```php
<?php
class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/sandbox/example/form')
            ->setMethod('post');

        // 创建名字的文本输入
        $name = new Zend_Form_Element_Text('name');
        $name->setLabel('First name:')
            ->setOptions(array('id' => 'fname'));

        // 创建密码输入
        $pass = new Zend_Form_Element_Password('pass');
        $pass->setLabel('Password:')
            ->setOptions(array('id' => 'upass'));

        // 创建隐藏输入
        $uid = new Zend_Form_Element_Hidden('uid');

        // 创建注释的文本区域
        $comment = new Zend_Form_Element_Textarea('comment');
        $comment->setLabel('Comment:')
            ->setOptions(array('id' => 'comment', 'rows' => 10, 'cols' => 30));

        // 将元素附加到表单
        $this->addElement($name)
            ->addElement($pass)
            ->addElement($uid)
            ->addElement($comment);
    }
}
```

表 3-1 表单元素类

| 类名 | 描述 |
| :--- | :--- |
| `Zend_Form_Element_Text` | 文本输入字段 |
| `Zend_Form_Element_Hidden` | 隐藏字段 |
| `Zend_Form_Element_Password` | 密码字段 |
| `Zend_Form_Element_Textarea` | 文本区域 |
| `Zend_Form_Element_Radio` | 单选按钮 |
| `Zend_Form_Element_Checkbox` | 复选框 |
| `Zend_Form_Element_MultiCheckbox` | 选择列表（多选） |
| `Zend_Form_Element_Select` | 选择列表（单选） |
| `Zend_Form_Element_File` | 文件输入字段 |
| `Zend_Form_Element_Image` | 图片字段 |
| `Zend_Form_Element_Button` | 按钮 |
| `Zend_Form_Element_Hash` | 唯一字符串 |
| `Zend_Form_Element_Captcha` | 用于垃圾过滤 |
| `Zend_Form_Element_Session` | 用于身份识别 |
| `Zend_Form_Element_Reset` | 重置按钮 |
| `Zend_Form_Element_Submit` | 提交按钮 |

#### 单选按钮和复选框

单选按钮由`Zend_Form_Element_Radio`类表示，而复选框由`Zend_Form_Element_Checkbox`类表示。以下是这两个类的示例：

```php
<?php
class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/sandbox/example/form')
            ->setMethod('post');

        // 创建名字的文本输入
        $name = new Zend_Form_Element_Text('name');
        $name->setLabel('Name:')
            ->setOptions(array('id' => 'fname'));

        // 创建类型的单选按钮
        $type = new Zend_Form_Element_Radio('type');
        $type->setLabel('Membership type:')
            ->setMultiOptions(array(
                'silver' => 'Silver',
                'gold' => 'Gold',
                'platinum' => 'Platinum'
            ))
            ->setOptions(array('id' => 'mtype'));

        // 创建订阅邮件的复选框
        $subscribe = new Zend_Form_Element_Checkbox('subscribe');
        $subscribe->setLabel('Subscribe to newsletter')
            ->setCheckedValue('yes')
            ->setUncheckedValue('no');

        // 将元素附加到表单
        $this->addElement($name)
            ->addElement($type)
            ->addElement($subscribe);
    }
}
```

`Zend_Form_Element_Radio`对象的`setMultiOptions()`方法接收一个数组，并使用它设置可用单选按钮选项。数组的键表示将提交的表单值，而对应的值表示每个选项的可视读标签。同样，`Zend_Form_Element_Checkbox`对象的`setCheckedValue()`和`setUncheckedValue()`方法允许你自定义元素被选中和未选中时的值。默认情况下，这些值分别被设置为 1 和 0。

```php
->setMultiOptions(array(
    'thin' => 'Thin',
    'thick' => 'Thick'
))
->setOptions(array('id' => 'type'));

// 创建配料的多选框
$toppings = new Zend_Form_Element_MultiCheckbox('toppings');
$toppings->setLabel('披配料:')
    ->setMultiOptions(array(
        'bacon' => '培根',
        'olives' => '橄',
        'tomatoes' => '番茄',
        'pepperoni' => '意大利腊肠',
        'ham' => '火腿',
        'peppers' => '红椒',
        'xcheese' => '额外芝士',
    ));

// 将元素添加到表单
```

图 3-2 展示了表单的样子。

你会立即注意到创建图 3-2 表单的代码有三点：

- 脚本中没有一行 HTML 代码。表单和表单元素表示为 PHP 对象，并使用对象方法进行配置。这确保了一致性并产生标准的 Web 表单。
- 预定义的验证器和过滤器适用于常见的输入验证和清理任务。这减少了工作量，产生了更具维护性的代码并避免了重复。验证器也可以组合或扩展以支持自定义需求。
- 验证器是在指定表单字段的同时指定的。这允许表单“知道”每个字段可以支持什么，并轻松识别输入错误的来源。单个字段也可以关联多个验证器。

从这些点可以清楚看出，Zend Form 为输入表单创建和数据验证提供了一个方便、可维护且可扩展的解决方案。本章的剩余部分将详细探讨 Zend Form，并在实际语境中对其进行演示。



`$this->addElement($name)`

`->addElement($type)`

`->addElement($toppings);`

图 3-5 展示了结果的样式。

## 选择列表

单选和多选列表通过`Zend_Form_Element_Select`和`Zend_Form_Element_MultiSelect`类支持。与`Zend_Form_Element_MultiCheckbox`类一样，它们也暴露了`setMultiOptions()`方法，用于设置可用选项列表。下面的示例演示了这两种元素的使用：

```php
<?php

class Form_Example extends Zend_Form

{

    public function init()

    {

        // 初始化表单

        $this->setAction('/sandbox/example/form')

        ->setMethod('post');

// 图 3-5：一个带有单选按钮和多个复选框的表单

60

Zend Framework: 入学者指南

// 创建姓名的文本输入

$name = new Zend_Form_Element_Text('name');

$name->setLabel('姓名:')

->setOptions(array('id' => 'fname'));

// 创建源地国家的选择列表

$from = new Zend_Form_Element_Select('from');

$from->setLabel('出发地:')

->setMultiOptions(array(

    'IN' => '印度',

    'US' => '美国',

    'DE' => '德国',

    'FR' => '法国',

    'UK' => '英国'

));

// 创建目的国家的多选列表

$to = new Zend_Form_Element_MultiSelect('to');

$to->setLabel('目的地:')

->setMultiOptions(array(

    'IT' => '意大利',

    'SG' => '新加坡',

    'TR' => '土耳其',

    'DK' => '丹麦',

    'ES' => '西班牙',

    'PT' => '葡萄牙',

    'RU' => '俄罗斯',

    'PL' => '波兰'

));

// 将元素添加到表单

$this->addElement($name)

->addElement($from)

->addElement($to);

    }

}
```

图 3-6 展示了结果。

## 文件上传字段

如果您想通过表单上传一个或多个文件，可以使用`Zend_Form_Element_File`类，它提供了一个可浏览的文件输入框。以下是它的使用示例：

```php
<?php

class Form_Example extends Zend_Form

{

// 图 3-6：一个带有选择列表的表单

61

第 3 章：操作表单

public function init()

    {

        // 初始化表单

        $this->setAction('/sandbox/example/form')

        ->setEnctype('multipart/form-data')

        ->setMethod('post');

// 创建用于上传照片的文件输入

$photo = new Zend_Form_Element_File('photo');

$photo->setLabel('照片:')

->setDestination('/tmp/upload');

// 将元素添加到表单

$this->addElement($photo);

    }

}
```

**注意**

请记住，您必须将表单编码类型设置为`multipart/form-data`才能正确处理表单上传。这可以通过表单对象的`setEnctype()`方法来实现。

图 3-7 展示了它的样式。

**提示**

如果您正尝试上传多个相关文件，有一个方便的`setMultiFile()`方法，它可以生成一系列文件输入字段，并省去您手动实例化多个`Zend_Form_Element_File`对象的麻烦。您将在下一章中看到相关示例。

## 按钮

每个表单都需要一个提交按钮，某些表单还需要重置按钮。这两个关键的表单元素分别由`Zend_Form_Element_Submit`和`Zend_Form_Element_Reset`类表示，并在下一个代码列表中进行了说明：

```php
<?php

class Form_Example extends Zend_Form

{

    public function init()

    {

        // 初始化表单

        $this->setAction('/sandbox/example/form')

        ->setMethod('post');

// 创建标题的文本输入

// 图 3-7：一个带有文件输入字段的表单

62

Zend Framework: 入学者指南

$title = new Zend_Form_Element_Text('title');

$title->setLabel('标题:')

->setOptions(array('size' => '35'));

// 创建提交按钮

$submit = new Zend_Form_Element_Submit('submit');

$submit->setLabel('提交');

// 创建重置按钮

$reset = new Zend_Form_Element_Reset('reset');

$reset->setLabel('取消');

// 将元素添加到表单

$this->addElement($title)

->addElement($submit)

->addElement($reset);

    }

}
```

图 3-8 展示了结果。

如果您想要一个通用的按钮，可以在`Zend_Form_Button`类中找到它，它提供了点击按钮。按钮可以通过`setImage()`方法生成。以下是此类按钮的示例：

```php
<?php

class Form_Example extends Zend_Form

{

    public function init()

    {

        // 初始化表单

        $this->setAction('/sandbox/example/form')

        ->setMethod('post');

// 创建标题的文本输入

// 图 3-8：一个带有提交和重置按钮的表单

$title = new Zend_Form_Element_Text('title');

$title->setLabel('标题:')

->setOptions(array('size' => '35'));

// 创建提交按钮

$submit = new Zend_Form_Button('submit', null, array('value' => '提交'));

// 创建重置按钮

$reset = new Zend_Form_Button('reset', null, array('value' => '取消'));

// 将元素添加到表单

$this->addElement($title)

->addElement($submit)

->addElement($reset);

    }

}
```

图 3-9 展示了输出。

## Hash 和 CAPTCHA 字段

Zend Framework 包含了两个“特殊”元素来协助安全：分别是`Hash`和`CAPTCHA`元素。`Hash`元素使用盐（salt）为表单生成唯一密钥，并在表单提交时将提交的值与存储在会话中的值进行比较。如果不匹配，可以合理假设表单已被劫持并被用于跨站请求伪造（CSRF）攻击。

```php
class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/sandbox/example/form')
        ->setMethod('post');

// 创建卡号文本输入
$cc = new Zend_Form_Element_Text('cc');
$cc->setLabel('信用卡号:')
->setOptions(array('size' => '16'));

// 创建金额文本输入
$amount = new Zend_Form_Element_Text('amount');
$amount->setLabel('支付金额:')
->setOptions(array('size' => '4'));

// 创建哈
$hash = new Zend_Form_Element_Hash('hash');
$hash->setSalt('hf823hw03');

// 创建提交按钮
$submit = new Zend_Form_Element_Submit('submit');
$submit->setLabel('提交');

// 将元素添加到表单
$this->addElement($cc)
->addElement($amount)
->addElement($hash)
->addElement($submit);
    }
}
```

`CAPTCHA`元素自动生成 CAPTCHA 验证输入，这是过滤自动化提交的有用工具。越来越多的网站正在使用 CAPTCHA 来减少虚假注册和垃圾垃圾信息。虽然手动生成和验证 CAPTCHA 是一个枯燥的过程，但`Zend_Form_Element_Captcha`让这一切只需在表单中添加几行代码。以下是一个示例：

**问：什么是 CSRF 攻击？我该如何防止它？**

**答：** 通常，当用户访问受保护的网站并验证其访问凭据时，会生成用户会话，并在每次请求时从会话数据存储中重新验证访问凭据。CSRF 攻击涉及劫持已验证的用户会话，并利用用户与托管应用程序之间已存在的隐含信任关系，通过 Web 表单等输入源隐地传输未经授权的请求。通过为每个 Web 表单生成唯一的哈希值并在提交时验证该值，开发者能够使此类攻击变得更加困难。使用哈希值还对自动垃圾邮件发送者（垃圾邮件机器人）提供了（有限）保护，并且比 CAPTCHA 更对用户友好。

专家咨询

## 第 3 章：处理表单

65

```php
// 创建密码输入框

$pass = new Zend_Form_Element_Password('password');

$pass->setLabel('密码:')
->setOptions(array('size' => '16'));

// 创建验证码

$captcha = new Zend_Form_Element_Captcha('captcha', array(
    'captcha' => array(
        'captcha' => 'Figlet',
        'wordLen' => 5,
        'timeout' => 300,
    )
));

$captcha->setLabel('验证:');

// 创建提交按钮

$submit = new Zend_Form_Element_Submit('submit');
$submit->setLabel('注册');

// 将元素添加到表单

$this->addElement($name)
->addElement($pass)
->addElement($captcha)
->addElement($submit);

}
```

图 3-10 展示了结果可能呈现的样式。

**注意**

Zend Framework 包含了许多预定义的的 CAPTCHA 适配器，包括用于简单字符串置换操作（“Dumb”）以及用于视觉验证码（“Image”和“Figlet”）的适配器。你将在本章稍后的部分看到另一个图像验证码的示例。

## 设置必填和默认值

你可以通过调用`setRequired()`方法并传入`true`参数，将特定的输入元素标记为必填项。这是一个示例：

```php
class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/sandbox/example/form')
        ->setMethod('post');
```

66

Zend Framework：入门指南

```php
// 为姓名创建文本输入框
$name = new Zend_Form_Element_Text('name');
$name->setLabel('姓名:')
->setOptions(array('size' => '35'))
->setRequired(true);
```

图 3-10

一个包含验证码的表单

**问：** **什么是 CAPTCHA？**

**答：** CAPTCHA，全全自动区分计算机与人的图灵测试，是一种常见的挑战-响应测试，用于识别连接另一端的实体是人类还是计算机。在 Web 上，CAPTCHA 的典型形式是扭曲的随机字母数字字符序列，其工作原理是计算机无法穿透扭曲看到内容，但具有更感知感知的人类能够正确识别该序列。此类 CAPTCHA 通常附加在 Web 上的输入表单中（例如用户注册表单），并且在主机应用程序处理输入之前，必须正确地解决它们。CAPTCHA 并不总是视觉化的；音频验证码也是可能的，并且最适合视障用户。

向专家提问

第 3 章：处理表单

67

```php
// 为电子邮箱地址创建文本输入框
$email = new Zend_Form_Element_Text('email');
$email->setLabel('邮箱地址:');
$email->setOptions(array('size' => '50'))
->setRequired(true);

// 创建提交按钮
$submit = new Zend_Form_Element_Submit('submit',
    array('class' => 'submit')
);
$submit->setLabel('注册');

// 将元素添加到表单
$this->addElement($name)
->addElement($email)
->addElement($submit);

}
```

当你在输入字段上使用`setRequired()`方法时，`Zend_Form`会自动为该字段附加一个`NotEmpty`验证器。因此，如果表单提交时字段为空，则会出现一条错误消息。图 3-11 展示了结果。

**提示**

你可以通过显式调用带有`false`参数的元素的`setAutoInsertNotEmptyValidator()`方法，来告诉`Zend_Form`不要为必填元素附加`NotEmpty`验证器。验证器将在下一节中进行详细讨论。

你可以通过调用元素对象的`setValue()`方法并传入默认值，或者通过调用表单对象的`setDefaults()`方法并传入默认值数组，来为输入元素附加默认值。对于文本输入字段，这可以是任何字符串值；对于单选按钮和选择列表，它应该是被选中项的索引。这里有一个示例，展示了这两种方法：



```php
class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/sandbox/example/form')
        ->setMethod('post');

        // 为姓名创建文本输入框
        $name = new Zend_Form_Element_Text('name');
        $name->setLabel('姓名:')
        ->setOptions(array('size' => '35'))
        ->setRequired(true)
        ->setValue('输入您的姓名');

        // 为电子邮箱地址创建文本输入框
        $email = new Zend_Form_Element_Text('email');
        $email->setLabel('邮箱地址:');
        ->setOptions(array('size' => '50'))
        ->setRequired(true)
        ->setValue('输入您的邮箱地址');

        // 为类型创建单选按钮
        $type = new Zend_Form_Element_Radio('type');
        $type->setLabel('类型:')
        ->setOptions(array(
            'silver' => '银色',
            'gold' => '金色',
            'platinum' => '铂金色'
        ));

        // 为订阅创建复选框
        $subscribe = new Zend_Form_Element_Checkbox('subscribe');
        $subscribe->setLabel('订阅')

        // 为国家创建选择列表
        $from = new Zend_Form_Element_Select('from');
        $from->setLabel('国家:')
        ->setOptions(array(
            'US' => '美国',
            'UK' => '英国',
            'DE' => '德国',
            'FR' => '法国',
            'IN' => '印度',
            'ES' => '西班牙',
            'IT' => '意大利',
            'JP' => '日本',
            'BR' => '巴西',
            'CA' => '加拿大'
        ));

        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit',
            array('class' => 'submit')
        );
        $submit->setLabel('注册');

        // 将元素添加到表单
        $this->addElement($name)
        ->addElement($email)
        ->addElement($type)
        ->addElement($subscribe)
        ->addElement($from)
        ->addElement($submit);

        // 设置默认值
        $this->setDefaults(array(
            'type' => 'gold',
            'subscribe' => 'yes',
            'from' => 'US'
        ));
    }

}
```

图 3-11 展示了结果。

（缺少必填值提交表单的结果）

68

Zend Framework：入门指南

## 过滤和验证表单输入

作为 Web 开发者，你必须面对一个不愉快的事实：总会有人通过寻找代码中的漏洞并从中获利。因此，开发者为确保应用程序安全能做的最重要的事情之一就是正确地过滤和验证所有输入。接下来的章节将讨论 Framework 提供的工具，以及它们如何与表单配合使用。

### 使用输入过滤器

大多数输入攻击都是通过发送经过伪装的值来“欺骗”应用程序。这种攻击的一个常见例子是注入攻击，攻击者通过嵌入 SQL 查询来远程操纵你的数据库。因此，开发者在使用任何用户提供的输入之前，必须对其进行“清理”。

PHP 提供了多种函数来协助开发者清理输入。例如，`addslashes()` 函数转义输入中的特殊字符（如引号和斜杠），以便存入数据库；而 `strip_tags()` 函数移除所有的 HTML 和 PHP 标签，只返回 ASCII 内容。还有 `htmlentities()` 函数，它通常用于将 `&<>` 等特殊字符替换为相应的 HTML 实体值，使其变得无害。

这是一个使用 `htmlentities()` 函数清理表输入的示例：

```php
<?php
// 定义清理后的数组
$sanitized = array();

// 从 POST 输入中过滤标签
if (isset($_POST['name']) && !empty($_POST['name'])) {
    $sanitized['name'] = htmlentities($_POST['name']);
}

// 处理代码 //
?>
```

在处理用户输入时，Zend Framework 已经为你完成了大部分工作。`Zend_Filter` 组件提供了一套全面的*输入过滤器*，这些过滤器既可以通过 `addFilter()` 方法附加到表单元素上，也可以单独使用进行即时输入清理。以下是在文本输入字段上使用 `HTMLEntities` 过滤器的示例：

```php
$name = new Zend_Form_Element_Text('name');
$name->addFilter('HTMLEntities');
```

## 第 3 章：表单操作

71

```php
public function init()
{
    // 初始化表单
    $this->setAction('/sandbox/example/form')
        ->setMethod('post');
    // 为用户名创建文本输入
    // 过滤特殊字符
    $name = new Zend_Form_Element_Text('name');
    $name->setLabel('用户名:')
        ->setOptions(array('size' => '16'))
        ->addFilter('HtmlEntities');
    // 创建提交按钮
    $submit = new Zend_Form_Element_Submit('submit');
    $submit->setLabel('注册');
    // 将元素附加到表单
    $this->addElement($name)
        ->addElement($submit);
}
}
```

你也可以向 `addFilter()` 方法传递一个 `Zend_Filter_*` 类的实例，如下等效脚本所示：

```php
<?php

class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/sandbox/example/form')
            ->setMethod('post');
        // 为用户名创建文本输入
        // 过滤特殊字符
        $name = new Zend_Form_Element_Text('name');
        $name->setLabel('用户名:')
            ->setOptions(array('size' => '16'))
            ->addFilter(new Zend_Filter_HtmlEntities());
        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit');
        $submit->setLabel('注册');
        // 将元素附加到表单
        $this->addElement($name)
            ->addElement($submit);
    }
}
```

72 Zend Framework：入门指南

某些过滤器支持额外的选项，这些选项可以作为数组传递给 `addFilter()` 方法，或者在使用类实例时，作为对象构造函数的参数传递。考虑下一个示例，它使用 `Alpha` 过滤器从用户输入中剔除所有非字母字符。作为第二个参数传递给 `addFilter()` 方法的额外选项保留了空格（默认情况下会被剔除）。

```php
<?php

class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/sandbox/example/form')
            ->setMethod('post');
        // 为名称创建文本输入
        // 允许字母字符和空格
        $name = new Zend_Form_Element_Text('name');
        $name->setLabel('姓名:')
            ->setOptions(array('size' => '4'))
            ->setRequired(true)
            ->addFilter('Alpha', array('allowWhiteSpace' => true))
            ->addFilter('HtmlEntities');
        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit');
        $submit->setLabel('注册');
        // 将元素附加到表单
        $this->addElement($name)
            ->addElement($submit);
    }
}
```

表 3-2 列出了 Zend Framework 自带的一些重要过滤器列表，以及每个过滤器的简要描述。你将在本及后续章节中看到许多过滤器的应用。

***提示***

你可以通过两种方式向表单元素附加多个过滤器：通过多次调用 `addFilter()` 方法（每次调用使用不同的过滤器名称），或者使用 `addFilters()` 方法并传递一个包含过滤器名称的数组。

73 第 3 章：表单操作

### 使用输入验证器

过滤输入只是问题的一部分。对输入进行验证也极其重要，以确保在在用于计算或保存到应用程序数据存储器之前其格式是正确的。验证不当的输入不仅会导致严重的数据损坏和丢失，还可能让开发者感到尴尬。

为了说明输入验证的重要性，请考虑一个简单的示例：一个在线计算器，允许用户输入所需的贷款金额、期限和利率。现在，假设该应用程序没有包含任何验证。并且假设用户决定在字段中输入字符串 `'ten'`（十）而不是数字 10。

表 3-2 Zend Framework 包含的输入过滤器

| 过滤器名称 | 描述 |

| :--- | :--- |

| `Alnum` | 从参数中移除非字母数字字符 |

| `Alpha` | 从参数中移除非字母字符 |

| `Digits` | 从参数中移除非数字字符 |

| `Int` | 返回参数的整数值 |

| `Dir` | 返回参数的目录名 |

| `BaseName` | 返回参数的文件名组件 |

| `RealPath` | 返回参数的绝对文件系统路径 |

| `StringToLower` | 将参数转换为小写字符串 |

| `StringToUpper` | 将参数转换为大写字符串 |

| `StringTrim` | 移除参数首尾的空格 |

| `StripNewlines` | 移除参数中的换行符 |

| `HtmlEntities` | 将参数中的特殊字符转换为 HTML 等效字符 |

| `StripTags` | 从参数中移除 HTML 代码 |

| `Encrypt` | 返回参数的加密版本 |

| `Decrypt` | 返回参数的解密版本 |

| `NormalizedToLocalized` | 返回本地化形式的参数 |

| `LocalizedToNormalized` | 返回标准格式的参数 |

| `Callback` | 带参数调用用户定义的过滤器 |

| `LowerCase` | 将参数内容转换为小写 |

| `UpperCase` | 将参数内容转换为大写 |

| `Rename` | 重命名参数 |

猜接下来会发生什么并不难。应用程序将执行几次内部计算，最后尝试将总应付金额除以指定的期限。由于此例中的期限是一个字符串，PHP 将将其转换为数字 0，产生除以零的错误。产生的一系列糟糕的错误信息可能会让即使优秀的开发者也感到棘手；更重要的是，如果无效输入也被原样保存到数据库中，那么每次重复计算时错误都会再次出现。如果数据库中散布着几条包含类似错误的记录，你很快就会发现缺乏适当的输入验证将如何严重损害一个应用程序。

PHP 提供了各种函数来帮助开发者完成输入验证任务。例如，`is_numeric()` 测试值是否为数字，而 `ctype_alpha()` 和 `ctype_alnum()` 函数可以测试字母和数字字符串。还有 `filter_var()` 函数可用于测试电子邮件地址和 URL，以及 `preg_match()` 函数可以使用正则表达式进行验证。这里是这些函数的用法示例：

```php
<?php
// 定义数组
$valid = array();
// 检查年龄是否为数字
if (is_numeric(trim($_POST['age']))) {
    $valid['age'] = trim($_POST['age']);
} else {
    die ('年龄不是数字');
}
// 检查有效的姓名
if (isset($_POST['firstname']) && ctype_alpha($_POST['firstname'])) {
    $valid['firstname'] = trim($_POST['firstname']);
} else {
    die ('姓名不存在或无效');
}
// 检查有效的电子邮件地址
if (isset($_POST['email']) && filter_var($_POST['email'], FILTER_VALIDATE_EMAIL)) {
    $valid['email'] = trim($_POST['email']);
} else {
    die ('电子邮件地址不存在或无效');
}
// 处理代码此处
?>
```

与过滤器一样，Zend Framework 提供了大量的预定义输入验证器，统称为 `Zend_Validate`，可以通过 `addValidator()` 方法附加到表单元素，也可以临时使用。特定的验证器选项可以作为键值对数组作为第三参数传递给方法，如下例所示：



```php
<?php

class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/sandbox/example/form')
            ->setMethod('post');
        // 为年龄创建文本输入
        // 应包含 1 到 100 之间的整数值
        $age = new Zend_Form_Element_Text('age');
        $age->setLabel('年龄:')
            ->setOptions(array('size' => '4'))
            ->setRequired(true)
            ->addValidator('Int')
            ->addValidator('Between', false, array(1,100));
        // 为名称创建文本输入
        // 应包含字母字符和空格
        $name = new Zend_Form_Element_Text('name');
        $name->setLabel('第一名:')
            ->setOptions(array('size' => '16'))
            ->setRequired(true)
            ->addValidator('Alpha', false, array('allowWhiteSpace' => true));
        // 为电子邮件地址创建文本输入
        // 应包含有效的电子邮件地址
        $email = new Zend_Form_Element_Text('email');
        $email->setLabel('电子邮件地址:')
            ->setOptions(array('size' => '16'))
            ->setRequired(true)
            ->addValidator('EmailAddress');
        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit');
        $submit->setLabel('注册');
        // 将元素附加到表单
        $this->addElement($age)
            ->addElement($name)
            ->addElement($email)
            ->addElement($submit);
    }
}
```

## Zend Framework：入门指南

与过滤器一样，验证器也可以被指定为相应的`Zend_Validate_*`类的实例，并将验证器选项作为参数传递给对象的构造函数。下一个示例与上一个示例等效，它说明了这种方法：

```php
class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/sandbox/example/form')
            ->setMethod('post');

        // 为年龄创建文本输入
        // 应该只包含 1 到 100 之间的整数
        $age = new Zend_Form_Element_Text('age');
        $age->setLabel('Age:')
            ->setOptions(array('size' => '4'))
            ->setRequired(true)
            ->addValidator(new Zend_Validate_Int())
            ->addValidator(new Zend_Validate_Between(1,100));

        // 为姓名创建文本输入
        // 应该只包含字母和空格
        $name = new Zend_Form_Element_Text('name');
        $name->setLabel('First name:')
            ->setOptions(array('size' => '16'))
            ->setRequired(true)
            ->addValidator(new Zend_Validate_Alpha(true));

        // 为邮箱地址创建文本输入
        // 应该包含有效的邮箱地址
        $email = new Zend_Form_Element_Text('email');
        $email->setLabel('Email address:')
            ->setOptions(array('size' => '16'))
            ->setRequired(true)
            ->addValidator(new Zend_Validate_EmailAddress());

        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit');
        $submit->setLabel('Sign Up');

        // 将元素附加到表单
        $this->addElement($age)
            ->addElement($name)
            ->addElement($email)
            ->addElement($submit);
    }
}
```

## 第 3 章：处理表单

图 3-13 展示了尝试通过此类表单提交无效值的结果。

表 3-3 提供了 Zend Framework 中可可用的一些重要验证器列表，以及对每个验证器的要描述。你将在本章的后续以及后续章节中看到许多验证器的应用。

**图 3-13** 提交带有无效输入值的表单的结果

| 验证器名称 | 描述 |
| :--- | :--- |
| `NotEmpty` | 如果参数为空，则返回 `false` |
| `StringLength` | 如果参数不符合指定的最小/最大长度，则返回 `false` |
| `InArray` | 如果参数不在指定的数组中，则返回 `false` |
| `Identical` | 如果参数不匹配指定的值，则返回 `false` |
| `Alnum` | 如果参数不只包含字母数字，则返回 `false` |
| `Alpha` | 如果参数不包含字母，则返回 `false` |
| `Int` | 如果参数不是整数，则返回 `false` |
| `Float` | 如果参数不是浮点数，则返回 `false` |
| `Hex` | 如果参数不是十六进制值，则返回 `false` |
| `Digits` | 如果参数不包含数字，则返回 `false` |
| `Between` | 如果参数不在指定的数值范围内，则返回 `false` |

**表 3-3** Zend Framework 包含的输入验证器

| 验证器名称 | 描述 |
| :--- | :--- |
| `GreaterThan` | 如果参数不大于指定值，则返回 `false` |
| `LessThan` | 如果参数不小于指定值，则返回 `false` |
| `Date` | 如果参数不是有效日期，则返回 `false` |
| `EmailAddress` | 如果参数不符合标准邮箱地址规范，则返回 `false` |
| `Hostname` | 如果参数不符合标准主机名规范，则返回 `false` |
| `Ip` | 如果参数不符合标准 IP 地址规范，则返回 `false` |
| `Regex` | 如果参数不符合指定的正则表达式模式，则返回 `false` |
| `Barcode` | 如果参数不是有效的条形码，则返回 `false` |
| `Ccnum` | 如果参数不符合标准信用卡号规范的 Luhn 算法，则返回 `false` |
| `Iban` | 如果参数不是有效的 IBAN 号，则返回 `false` |
| `Exists` | 如果参数不是有效的文件，则返回 `false` |
| `Count` | 如果上传的文件数量不在参数指定的范围内，则返回 `false` |
| `Size` | 如果上传的文件大小不在参数指定的范围内，则返回 `false` |
| `FilesSize` | 如果上传的文件总大小不在参数指定的范围内，则返回 `false` |
| `Extension` | 如果上传的文件扩展名与参数中指定的不匹配，则返回 `false` |
| `MimeType` | 如果上传文件的 MIME 类型与参数中指定的不匹配，则返回 `false` |
| `IsCompressed` | 如果上传的文件不是压缩包文件，则返回 `false` |
| `IsImage` | 如果上传的文件不是图片文件，则返回 `false` |
| `ImageSize` | 如果上传的图片尺寸不在参数指定的范围内，则返回 `false` |
| `Crc32`, `Md5`, `Sha1`, `Hash` | 如果上传文件的内容与参数中指定的哈希值不匹配，则返回 `false`（支持 `crc32`, `md5`, `sha1`） |
| `ExcludeExtension` | 如果上传的文件扩展名与参数中指定的匹配，则返回 `false` |
| `ExcludeMimeType` | 如果上传文件的 MIME 类型与参数中指定的匹配，则返回 `false` |
| `WordCount` | 如果上传的文件数量不在参数指定的范围内，则返回 `false` |
| `Db_Exists` | 如果记录在数据库中不存在，则返回 `false` |
| `Db_NoExists` | 如果记录在数据库中存在，则返回 `false` |

**表 3-3** Zend Framework 包含的过滤器（续）

## 使用验证器和过滤器链

验证器和过滤器最有趣的特性之一是它们支持“链式调用”（chaining）。本质上，这意味着你可以在单个元素上附加多个过滤器和验证器，并且它们按顺序执行。下面的示例说明了这一点：

```php
// 为姓名创建文本输入
// 应该只包含字母和空格
$name = new Zend_Form_Element_Text('name');
$name->setLabel('First name:')
    ->setOptions(array('size' => '16'))
    ->setRequired(true)
    ->addValidator(new Zend_Validate_Alpha(true));
```

在

```php
// 为年龄创建文本输入
// 应该只包含 1 到 100 之间的整数
$age = new Zend_Form_Element_Text('age');
$age->setLabel('Age:')
    ->setOptions(array('size' => '4'))
    ->setRequired(true)
    ->addFilter('StripTags')
    ->addFilter('HtmlEntities')
    ->addFilter('StringTrim')
    ->addFilter('StringToLower');
```

第一个过滤器会去除 HTML 标签，第二个过滤器会将实体编码，第三个过滤器会修剪首尾空格，第四个过滤器会将字符串转换为小写。过滤器按它们添加的顺序执行，并且上一个过滤器的输出是下一个过滤器的输入。

验证器的工作方式与过滤器类似，但目的不同。过滤器用于修改数据，而验证器则用于检查数据是否符合要求。你可以在同一个元素上附加多个验证器，它们也会按添加的顺序执行。

验证器链有一个非常有利的属性。验证器链可以配置为：当任何一个验证器失败时终止整个链，并产生相应的错误消息。这种行为由`addValidator()`方法的第二个参数控制。当设置为`true`时，如果某个验证器失败，链将断开。考虑下面的示例，它说明了这一点：

> **问：** 我已经使用 JavaScript 验证表单输入了。为什么我还需要用 PHP 进行验证呢？
>
> **答：** 使用客户端脚本语言（如 JavaScript 或 VBScript）进行输入验证是常见做法。然而，这种客户端验证并不是无懈可击的——如果用户禁用了 JavaScript，所有的客户端代码都将失效。因此，将客户端验证（更快）与服务端验证（更安全）结合起来是一个好主意。
>
> *咨询专家*

```php
// 为年龄创建文本输入
// 应该只包含 1 到 100 之间的整数
$age = new Zend_Form_Element_Text('age');
$age->setLabel('Age:')
    ->setOptions(array('size' => '4'))
    ->setRequired(true)
    ->addValidator('NotEmpty', true)
    ->addValidator('Int', true)
    ->addValidator('Between', true, array(1,100));
```

在这个示例中，任何一个验证器失败，链就会中断，剩余的验证器将不再处理。因此，如果输入不是整数，验证链将以`Int`验证器产生的错误消息终止，`Between`验证器将不会执行。对比下面的列表：

```php
// 为年龄创建文本输入
// 应该只包含 1 到 100 之间的整数
$age = new Zend_Form_Element_Text('age');
$age->setLabel('Age:')
    ->setOptions(array('size' => '4'))
    ->setRequired(true)
    ->addValidator('NotEmpty', false)
    ->addValidator('Int', false)
    ->addValidator('Between', false, array(1,100));
```

在这个版本中，即使某个验证器失败，剩余的验证器仍然会运行，并且任何后续失败产生的错误消息都会被添加到消息栈中。这通过图 3-14 和图 3-15 展示，对比了这两个列表的行为差异。

**图 3-14** 在第一次失败时断开的验证器链

## 第 3 章：表单操作

***提示***

如果 Zend Framework 自带的预定义过滤器和验证器不能满足你的需求，记住你始终可以编写自己的。Zend Framework 手册中提供了如何实现此点的示例。

### 获取和处理表单输入

在控制器脚本中，你可以使用多个`Zend_Form`方法在提交后获取并处理表单输入：

- `isValid()`方法检查提交的输入是否有效。该方法接受一个输入值数组，并根据这些值是否匹配通过各种`addValidator()`调用设置的验证规则返回布尔值`true`或`false`。

- 如果输入无效，`getMessages()`方法将返回验证过程中生成的错误消息列表。当表单重新渲染时，可以对此列表进行处理和显示，以提示用户可能出了问题。

- 如果输入有效，可以使用`getValues()`方法获取经过过滤的有效值，以进行进一步处理。输入值以关联数组元素的形式返回，其中数组键代表元素名称，数组值代表相应的输入值。还有一个`getUnfilteredValues()`方法，它会返回用户输入的原始、未过滤的输入。

***提示***

`isValid()`方法会自动验证 CAPTCHA 和哈希值，无需你进行额外的编程。

**图 3-15**：验证器链，处理过程中没有任何中断

下面的代码示例说明了这些方法在控制器脚本环境中通常如何使用：

```php
<?php

class ExampleController extends Zend_Controller_Action
{
    public function formAction()
    {
        $form = new Form_Example;
        $this->view->form = $form;

        // 检查请求
        // 运行验证器
        if ($this->getRequest()->isPost()) {
            if ($form->isValid($this->getRequest()->getPost())) {
                // 有效数据：获取过滤后的有效值
                // 执行操作，保存到数据库或写入文件
                // 显示成功视图
                $values = $form->getValues();
                $this->_redirect('/form/success');
            } else {
                // 无效数据：获取错误消息数组
                // 用于手动处理（如果需要）
                // 重新显示带错误的表单
                $this->view->messages = $form->getMessages();
            }
        }
    }
}

?>
```

### 创建联系表单



有了这些背景信息后，现在让我们来看看它在实际应用中是如何运作的。以下部分将应用你到目前为止所学的所有知识，为 `SQUARE` 应用创建一个邮件查询表单。该表单将邀请用户输入消息，并在提交时将输入格式化为邮件消息，并发送给网站管理员进行跟进。

## 定义表单

首先，让我们考虑输入表单的需求。这些需求并不复杂——实际上只需要三个字段，供用户输入其姓名、电子邮件地址和消息。这些值应该经过验证，特别是电子邮件地址，以确保真实性，从而使管理员能够回复邮件查询。为了过滤掉自动提交的内容并减少垃圾邮件的发生率，如果能包含一个视觉上的 `CAPTCHA` 也是不错的——正如之前所示，使用 `Zend_Form` 做到这一点非常简单。

以下是生成的表单定义示例：

```php
<?php

class Square_Form_Contact extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/contact/index')
            ->setMethod('post');

        // 为姓名创建文本输入
        $name = new Zend_Form_Element_Text('name');
        $name->setLabel('Name:')
            ->setOptions(array('size' => '35'))
            ->setRequired(true)
            ->addValidator('NotEmpty', true)
            ->addValidator('Alpha', true)
            ->addFilter('HTMLEntities')
            ->addFilter('StringTrim');

        // 为电子邮件地址创建文本输入
        $email = new Zend_Form_Element_Text('email');
        $email->setLabel('Email address:');
        ->setOptions(array('size' => '50'))
            ->setRequired(true)
            ->addValidator('NotEmpty', true)
            ->addValidator('EmailAddress', true)
            ->addFilter('HTMLEntities')
            ->addFilter('StringToLower')
            ->addFilter('StringTrim');

        // 为消息主体创建文本区域
        $message = new Zend_Form_Element_Textarea('message');
        $message->setLabel('Message:')
            ->setOptions(array('rows' => '8','cols' => '40'))
            ->setRequired(true)
            ->addValidator('NotEmpty', true)
            ->addFilter('HTMLEntities')
            ->addFilter('StringTrim');

        // 创建验证码
        $captcha = new Zend_Form_Element_Captcha('captcha', array(
            'captcha' => array(
                'captcha' => 'Image',
                'wordLen' => 6,
                'timeout' => 300,
                'width' => 300,
                'height' => 100,
                'imgUrl' => '/captcha',
                'imgDir' => APPLICATION_PATH . '/../public/captcha',
                'font' => APPLICATION_PATH . '/../public/fonts/LiberationSans.ttf',
            )
        ));

        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit')
            ->setLabel('Send Message');

        // 将元素附加到表单
        $this->addElement($name);
        $this->addElement($email);
        $this->addElement($message);
        $this->addElement($captcha);
        $this->addElement($submit);
    }
}

?>
```

基于第 2 章讨论的内容，这部分对你来说应该非常熟悉——它设置了一个路由，使得对应用 URL `/contact` 的请求将由“default”（默认）模块的 `ContactController::indexAction` 进行处理。

## 定义控制器和视图

下一步是定义上述的 `ContactController::indexAction`。按照惯例，该控制器应该位于`$APP_DIR/application/modules/default/controllers/ContactController.php`，并且看起来应该如下所示：

```php
<?php

class ContactController extends Zend_Controller_Action
{
    public function init()
    {
        $this->view->doctype('XHTML1_STRICT');
    }

    public function indexAction()
    {
        $form = new Square_Form_Contact();
        $this->view->form = $form;
        if ($this->getRequest()->isPost()) {
            if ($form->isValid($this->getRequest()->getPost())) {
                $values = $form->getValues();
                $mail = new Zend_Mail();
                $mail->setBodyText($values['message']);
                $mail->setFrom($values['email'], $values['name']);
                $mail->addTo('info@square.example.com');
                $mail->setSubject('Contact form submission');
                $mail->send();
                $this->_helper->getHelper('FlashMessenger')
                    ->addMessage('Thank you. Your message was successfully sent.');
                $this->_redirect('/contact/success');
            }
        }
    }

    public function successAction()
    {
        if ($this->_helper->getHelper('FlashMessenger')->getMessages()) {
            $this->view->messages = $this->_helper->getHelper('FlashMessenger')->getMessages();
        } else {
            $this->_redirect('/');
        }
    }
}
```

这里的大部分工作是由`indexAction()`方法完成的，它创建了之前讨论过的`Square_Form_Contact`类对象并将其附加到视图。当表单被提交时，将使用对象的`isValid()`方法来验证用户提交的内容。如果发现输入有效，则会创建一个`Zend_Mail`组件的实例，并使用对象方法将输入格式化为电子邮件消息并发送到指定的电子邮件地址。消息发送后，控制权将转移到`successAction()`方法，该方法将渲染成功视图。

如果一切顺利，情况就是这样……但事与愿违，因此了解在出现问题时会发生什么是有用的。如果发现输入无效，`isValid()`方法将返回`false`，表单将重新显示，并带有指示错误来源的错误消息。`Zend_Form`还会用原始输入值填充表单，以确保用户不需要重新输入所有请求的数据。另一方面，如果输入有效但在电子邮件生成和传输过程中发生错误，`Zend_Mail`将抛出一个 PHP 异常，该异常将由应用程序的默认错误处理器捕获并处理。

**注意**

为了让`Zend_Mail`对象的`send()`方法正常工作，必须在你的`php.ini`配置文件中可用并正确配置了邮件投递代理（例如`sendmail`）。如果情况并非如此，消息传输将失败，且`send()`方法将在失败点抛出异常。

该控制器还引入了一个新工具`FlashMessenger`辅助类，这是一个非常有用的小“助手”，可以简化向用户显示状态消息的过程。可以通过`addMessage()`方法向`FlashMessenger`对象添加消息；这些消息随后存储在 session 中，直到通过调用`getMessages()`方法检索它们，此时它们将从 session 中移除。这使得`FlashMessenger`成为一个临时存储消息的方便场所，从操作结束到视图渲染完成期间，你会在书中经常看到它的身影。

**注意**

你会注意到控制器的`init()`方法将视图的文档类型设置为 XHTML。这是因为默认情况下，`Zend_Form`并不生成良好的 XHTML 标记。

显然，你还需要两个视图，一个用于输入表单，一个用于成功消息。这里是输入视图，按照惯例位于`$APP_DIR/application/modules/default/views/scripts/index.phtml`：

```html
<h2>Contact</h2>
<?php echo $form; ?>
```

这里是成功视图，按照惯例存储在`$APP_DIR/application/modules/default/views/scripts/success.phtml`：

```html
<h2>Success</h2>
<?php echo implode($messages); ?>
```

## 更新主布局

现在剩下的工作是使用`url()`方法更新应用程序主菜单中的导航链接。为了实现这一点，请更新主布局`$APP_DIR/application/layouts/master.phtml`，并加粗显示更改：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
<base href="/" />
<link rel="stylesheet" type="text/css" href="/css/master.css" />
</head>
<body>
<div id="header">
<div id="logo">
<img src="/images/logo.gif" />
</div>
<div id="menu">
<a href="<?php echo $this->url(array(), 'home'); ?>">HOME</a>
<a href="<?php echo $this->url(array('page' => 'services'), 'static-content'); ?>">SERVICES</a>
**<a href="<?php echo $this->url(array(), 'contact'); ?>">CONTACT</a>**
</div>
</div>
<div id="content">
<?php echo $this->layout()->content ?>
</div>
<div id="footer">
<p>Created with <a href="http://framework.zend.com/">Zend Framework</a>. Licensed under <a href="http://www.creativecommons.org/">Creative Commons</a>.</p>
</div>
</body>
</html>
```

```php
Zend_Validate_EmailAddress::INVALID_HOSTNAME
=> "ERROR: 主机格式无效",

Zend_Validate_EmailAddress::INVALID_LOCAL_PART
=> "ERROR: 用户名格式无效",

Zend_Validate_EmailAddress::LENGTH_EXCEEDED
=> "ERROR: 邮箱地址过长"
)

))

->addFilter('StringTrim');

// 创建提交按钮
$submit = new Zend_Form_Element_Submit('submit');
$submit->setLabel('注册');

// 将元素添加到表单
$this->addElement($name)
->addElement($email)
->addElement($submit);

}

}
```

在此示例中，每个无效情况的默认错误消息被传递给`addValidator()`方法的数组中`'messages'`键所指定的自定义消息所覆盖。错误消息数组左侧的常量可以通过检查相应验证器的源代码来获取。这些新消息将被生成、添加到错误堆栈中，并在相应的元素验证失败时在表单中显示。输出示例见图 3-19。

**提示**

你也可以通过验证器的`setMessages()`方法向验证器传递自定义错误消息。

图 3-19

带有自定义错误消息的表单

## 使用显示组（Display Groups）

将具有某些松散或不紧密联系的表单元素分组通常是一个好主意。与没有任何清晰分类而堆砌在一起的无序元素相比，这种方法更具实用性和可读性。在`Zend_Form`中，这是通过使用*显示组*来完成的。

显示组通过表单对象的`addDisplayGroup()`方法添加到表单，该方法接受两个参数：一个包含组内元素名称的数组，以及组的名称。涉及的元素应该已经通过`addElement()`方法添加到表单中。然后可以使用`setLegend()`方法为显示组指定名称。在渲染时，这些显示组和图例分别由`<fieldset>`和`<legend>`元素表示。

以下是一个说明性示例：



```php
<?php
class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/sandbox/example/form')
        ->setMethod('post');

        // 为名称创建文本输入
        $name = new Zend_Form_Element_Text('name');
        $name->setLabel('姓名:')
        ->setOptions(array('size' => '35'))
        ->setRequired(true)
        ->addFilter('StringTrim');

        // 为邮箱地址创建文本输入
        $email = new Zend_Form_Element_Text('email');
        $email->setLabel('邮箱地址:');
        ->setOptions(array('size' => '50'))
        ->setRequired(true)
        ->addValidator('EmailAddress')
        ->addFilter('StringTrim');

        // 为电话号码创建文本输入
        $tel = new Zend_Form_Element_Text('tel');
        $tel->setLabel('电话号码:');
        ->setOptions(array('size' => '50'))
        ->setRequired(true);

        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit');
        $submit->setLabel('注册');

        // 将元素添加到表单
        $this->addElement($name)
        ->addElement($email)
        ->addElement($tel);

        // 添加显示组
        $this->addDisplayGroup(
            array('name', 'email', 'tel', 'address'),
            'contact'
        );
        $this->getDisplayGroup('contact')
        ->setLegend('联系信息');

        $this->addElement($submit);
    }
}
```

图 20 展示了结果的外。

## 使用装饰器（Decorators）

在渲染表单时，`Zend_Form` 自动将每个表单元素封装在一组 HTML 块中，这些块控制着元素的位置和外观。这些 HTML 标记块被称为*装饰器*，除了提供了一个用于基于 CSS 操作的现用钩子外，它们还可以针对每个元素进行自定义，以从根本上改变元素的渲染方式。

**图 20** 带有显示组的表单

第 3 章：表单操作 95

与过滤器和验证器一样，Zend Framework 自带了许多默认装饰器。表 3-4 列出了最可能遇到的装饰器。默认的 `Zend_Form` 装饰器使用以下标记：

- 表单标签被封装在 `<dt>...</dt>` 元素中。
- 输入字段被封装在 `<dd>...</dd>` 元素中。
- 验证错误被渲染为列表项并封装在 `<ul>...</ul>` 元素中。

图 21 展示了此类表单的 HTML 源代码，而图 22 展示了渲染后的结果。

**图 21** 使用默认装饰器的表单源码

**表 3-4** 常用装饰器

| 装饰器名称 | 描述 |
| :--- | :--- |
| `Form` | 控制表单周围的标记 |
| `FormElements` | 控制表单字段周围的标记 |
| `HtmlTag` | 控制表单字段周围的标记 |
| `ViewHelper` | 控制视图助手 |
| `Errors` | 控制验证错误周围的标记（按字段） |
| `FormErrors` | 控制验证错误周围的标记（摘要） |
| `Description` | 控制字段描述周围的标记 |
| `Label` | 控制标签周围的标记 |
| `Fieldset` | 控制图集周围的标记 |

通常，这种布局适用于你的应用程序界面。为了更改它，请使用以下方法：

- `addDecorators()` 方法接收装饰器数组并添加新的装饰器。
- `clearDecorators()` 方法移除元素的所有装饰器。
- `setDecorators()` 方法接收装饰器数组，并覆盖已存在的装饰器。注意，如果你禁用了默认装饰器，仍然应该添加 `ViewHelper` 装饰器。

为了说明如何使用这些装饰器，请考虑以下示例：

```php
<?php
class Form_Example extends Zend_Form
{
    public $formDecorators = array(
        array('FormElements'),
        array('Form'),
    );

    public $elementDecorators = array(
        array('ViewHelper'),
        array('Label'),
        array('Errors'),
    );

    public $buttonDecorators = array(
        array('ViewHelper'),
        array('HtmlTag', array('tag' => 'p'))
    );

    public function init()
    {
        // 初始化表单
        $this->setAction('/sandbox/example/form')
        ->setMethod('post')
        ->setDecorators($this->formDecorators);

        // 为名称创建文本输入
        $name = new Zend_Form_Element_Text('name');
        $name->setLabel('姓名:')
        ->setOptions(array('size' => '35'))
        ->setRequired(true)
        ->setDecorators($this->elementDecorators);

        // 为邮箱地址创建文本输入
        $email = new Zend_Form_Element_Text('email');
        $email->setLabel('邮箱地址:')
        ->setOptions(array('size' => '50'))
        ->setRequired(true)
        ->setDecorators($this->elementDecorators);

        // 为订阅订阅创建复选框
        $subscribe = new Zend_Form_Element_Checkbox('subscribe');
        $subscribe->setLabel('订阅订阅:')
        ->setCheckedValue('yes')
        ->setUncheckedValue('no')
        ->setDecorators($this->elementDecorators);

        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit', array('class' => 'submit'));
        $submit->setLabel('注册')
        ->setDecorators($this->buttonDecorators);

        // 将元素添加到表单
        $this->addElement($name)
        ->addElement($email)
        ->addElement($subscribe)
        ->addElement($submit);
    }
}
```

**图 23** 使用自定义装饰器的表单源码

## 第3章：处理表单

***注意***

装饰器（Decorators）本身是一个非常广泛的话题，本书无法对其进行详尽的细节介绍。前一节介绍的材料应该足够你入门，并帮助你理解本书中用到的相对简单的装饰器。如需更深入的研究，请参考本章末尾的链接。

### 总结

本章重点关注表单：创建表单、验证表单以及处理表单。它向你介绍了 Zend Framework 中三个最重要的组件之一——`Zend_Form`、`Zend_Validate` 和 `Zend_Filter`，并向你展示了如何使用它们安全地请求和处理用户输入。随后，它将这些知识应用于 SQUARE 示例应用程序，引导你完成了为自定义对象注册新命名空间、创建一个邮件查询表单，以及使用 `Zend_Mail` 组件将通过该表单接收到的输入作为邮件消息发送出去。最后，它快速查看了某些可以帮助你控制表单外观的工具，包括显示组（display groups）、装饰器和自定义错误消息；你将在全书中看到这些工具的应用。

要了解更多关于本章讨论的话题，请考虑访问以下链接：

- Wikipedia 关于 CSRF 和 XSS 攻击的讨论，位于：**http://en.wikipedia.org/wiki/Cross-site_request_forgery** 和 **http://en.wikipedia.org/wiki/Cross-site_scripting**
- Wikipedia 关于 CAPTCHA 的讨论，位于：**http://en.wikipedia.org/wiki/Captcha**
- Wikipedia 关于流式接口（fluent interfaces）的讨论，位于：**http://en.wikipedia.org/wiki/Fluent_interface**
- Zend Framework 自动加载器，位于：**http://framework.zend.com/manual/en/zend.loader.autoloader.html**
- `Zend_Form` 组件，位于：**http://framework.zend.com/manual/en/zend.form.html**
- `Zend_Filter` 组件，位于：**http://framework.zend.com/manual/en/zend.filter.html**
- `Zend_Validate` 组件，位于：**http://framework.zend.com/manual/en/zend.validate.html**
- `Zend_Mail` 组件，位于：**http://framework.zend.com/manual/en/zend.mail.html**
- 关于创建自定义装饰器的讨论（Matthew Weier O’Phinney），位于：**http://weierophinney.net/matthew/archives/213-From-the-inside-out-How-to-layer-decorators.html**

**图 3-24**：图 3-23 表单的渲染版本

## 第4章：处理模型

### 核心技能与概念

- 理解模型在模型-视图-控制器（MVC）模式中的作用
- 学习“胖模型，瘦控制器（fat model, skinny controller）”方法的益处
- 将 Doctrine 对象关系映射（ORM）工具包与 Zend Framework 集成
- 使用 Doctrine 模型生成器创建模型
- 使用 Doctrine 模型从 MySQL 数据库检索记录
- 了解如何使用 `Zend_Filter_Input` 组件过滤输入
- 使用 Zend Framework 引导程序（bootstrapper）微调应用程序的启动过程

上一章带你快速学习了使用 Zend Framework 创建、验证和处理表单的基础知识。然而，表单输入并不会凭空消失在真空中；它必须去某个地方。通常情况下，那个“某个地方”是数据库，例如 MySQL、SQLite 或 PostgreSQL，因此为应用程序添加数据库支持成为应用程序开发人员的一项任务。

不过，数据库只是谜图的一部分：你还需要*模型*来与之交互。模型在逻辑上独立于视图和控制器，充当应用程序的“数据层”，并提供操纵应用程序数据所需的功能。Zend Framework 使编写针对你应用程序需求的模型变得简单易许多；你还可以集成由 Doctrine 或 Propel 等流行的第三方工具生成的模型。本章将把你的 Zend Framework 技能提升几个台阶，向你展示如何向应用程序中创建并添加模型，然后使用这些模型从 MySQL 数据库中检索数据。它还将向你介绍 Doctrine，这是一个强大（且免费）的数据映射工具，可以显著简化这些任务。

### 理解模型

到此时，你应该已经对视图和控制器相当熟悉了，它们分别代表符合 MVC 标准的应用程序的“用户界面层”和“处理层”。模型代表“数据层”，负责提供访问数据的通道，并负责维护和执行与该数据相关的任何业务规则。例如，如果你正在为在线图书馆构建一个签入系统，你可能有一个 `Transaction`（事务）模型，它不仅记录书籍借还的详细信息，还包含了规则，不允许单个成员在同一时间借用超过五本书，或者自动计算逾还费用并从相应的成员账户中扣除。同样，如果你正在构建一个航空票务应用程序，你可能有一个 `Ticket`（票务）模型，它不仅能够保存和检索记录，还可以根据特定航班的乘客负载自动增加或减少票价。这里是一个简单模型的示例：

```php
<?php
class MemberModel
{
    protected $db;
    public $id;
    public $name;
    public $age;
    public $type;
    private $rate;

    // 处理成员数据并初始化数据库连接的构造函数
    public function __construct()
    {
        $this->db = new PDO('mysql:dbname=db;host=localhost', 'user', 'pass');
        $this->db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    }

    // 根据 id 获取成员记录
    public function fetch($id)
    {
        $id = $this->db->quote($id);
        $rs = $this->db->query("SELECT * FROM member WHERE id = $id");
        return $rs->fetchAll(PDO::FETCH_ASSOC);
    }

    // 获取所有成员记录
    public function fetchAll()
    {
        $rs = $this->db->query("SELECT * FROM member");
        return $rs->fetchAll(PDO::FETCH_ASSOC);
    }

    // 添加成员记录
    public function save()
    {
        // 过滤输入
        $f = array();
        $f['name'] = htmlentities($this->name);
        $f['age'] = htmlentities($this->age);
        $f['type'] = htmlentities($this->type);

        // 验证年龄
        if ($f['age'] < 18) {
            throw new Exception('Member under 18');
        }

        // 根据成员类型自动计算折扣
        switch ($f['type']) {
            case 'silver':
                // 逻辑省略
                break;
            case 'gold':
                // 逻辑省略
                break;
            case 'platinum':
                // 逻辑省略
                break;
        }

        // 插入逻辑示例
        $sql = "INSERT INTO member (name, age, type) VALUES (" . $f['name'] . ", " . $f['age'] . ", '" . $f['type'] . ")";
        $this->db->exec($sql);

        return $this->db->lastInsertId();
    }
}
?>
```




## 第3章：处理表单

### 注意

装饰器本身是一个非常广泛的话题，本书无法对其进行详尽的细节介绍。前一节介绍的材料应该足够你入门，并帮助你理解本书中用到的相对简单的装饰器。如需更深入的研究，请参考本章末尾的链接。

### 总结

本章重点关注表单：创建表单、验证表单以及处理表单。它向你介绍了 Zend Framework 中三个最重要的组件之一——`Zend_Form`、`Zend_Validate` 和 `Zend_Filter`，并向你展示了如何使用它们安全地请求和处理用户输入。随后，它将这些知识应用于 SQUARE 示例应用程序，引导你完成了为自定义对象注册新命名空间、创建一个邮件查询表单，以及使用 `Zend_Mail` 组件将通过该表单接收到的输入作为邮件消息发送出去。最后，它快速查看了某些可以帮助你控制表单外观的工具，包括显示组、装饰器和自定义错误消息；你将在全书中看到这些工具的应用。

要了解更多关于本章讨论的话题，请考虑访问以下链接：

- Wikipedia 关于 CSRF 和 XSS 攻击的讨论，位于：`http://en.wikipedia.org/wiki/Cross-site_request_forgery` 和 `http://en.wikipedia.org/wiki/Cross-site_scripting`
- Wikipedia 关于 CAPTCHAs 的讨论，位于：`http://en.wikipedia.org/wiki/Captcha`
- Wikipedia 关于流式接口（fluent interfaces）的讨论，位于：`http://en.wikipedia.org/wiki/Fluent_interface`
- Zend Framework 自动加载器，位于：`http://framework.zend.com/manual/en/zend.loader.autoloader.html`
- `Zend_Form` 组件，位于：`http://framework.zend.com/manual/en/zend.form.html`
- `Zend_Filter` 组件，位于：`http://framework.zend.com/manual/en/zend.filter.html`
- `Zend_Validate` 组件，位于：`http://framework.zend.com/manual/en/zend.validate.html`
- `Zend_Mail` 组件，位于：`http://framework.zend.com/manual/en/zend.mail.html`
- 关于创建自定义装饰器的讨论（Matthew Weier O’Phinney），位于：`http://weierophinney.net/matthew/archives/213-From-the-inside-out-How-to-layer-decorators.html`

图 3-24：图 3-23 表单的渲染版本

## 第4章：处理模型

### 核心技能与概念

- 理解模型在模型-视图-控制器（MVC）模式中的作用
- 学习“胖模型，瘦控制器”方法的益处
- 将 Doctrine 对象关系映射（ORM）工具包与 Zend Framework 集成
- 使用 Doctrine 模型生成器创建模型
- 使用 Doctrine 模型从 MySQL 数据库检索记录
- 了解如何使用 `Zend_Filter_Input` 组件过滤输入
- 使用 Zend Framework 引导程序（bootstrapper）微调应用程序的启动过程

上一章带你快速学习了使用 Zend Framework 创建、验证和处理表单的基础知识。然而，表单输入并不会凭空消失在真空中；它必须去某个地方。通常情况下，那个“某个地方”是数据库，例如 MySQL、SQLite 或 PostgreSQL，因此为应用程序添加数据库支持成为应用程序开发人员的一项任务。

不过，数据库只是谜图的一部分：你还需要模型来与之交互。模型在逻辑上独立于视图和控制器，充当应用程序的“数据层”，并提供操纵应用程序数据所需的功能。Zend Framework 使编写针对你应用程序需求的模型变得简单许多；你还可以集成由流行的第三方工具（如 Doctrine 或 Propel）生成的模型。本章将把你的 Zend Framework 技能提升几个台阶，向你展示如何向应用程序中创建并添加模型，然后使用这些模型从 MySQL 数据库中检索数据。它还将向你介绍 Doctrine，这是一个强大（且免费）的数据映射工具，可以显著简化这些任务。

### 理解模型

到此时，你应该已经对视图和控制器相当熟悉了，它们分别代表符合 MVC 标准的应用程序的“用户界面层”和“处理层”。模型代表“数据层”，负责提供访问数据的通道，并负责维护和执行与该数据相关的任何业务规则。

例如，如果你正在为在线图书馆构建一个签入系统，你可能有一个 `Transaction`（事务）模型，它不仅记录书籍借还的详细信息，还包含了规则，不允许单个成员在同一时间借用超过五本书，或者自动计算逾还费用并从相应的成员账户中扣除。

同样，如果你正在构建一个航空票务应用程序，你可能有一个 `Ticket`（票务）模型，它不仅能够保存和检索记录，还可以根据特定航班的乘客负载自动增加或减少票价。这里是一个简单模型的示例：

```php
<?php
class MemberModel
{
    protected $db;
    public $id;
    public $name;
    public $age;
    public $type;
    private $rate;

    // 处理成员数据并初始化数据库连接的构造函数
    public function __construct()
    {
        $this->db = new PDO('mysql:dbname=db;host=localhost', 'user', 'pass');
        $this->db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    }

    // 根据 id 获取成员记录
    public function fetch($id)
    {
        $id = $this->db->quote($id);
        $rs = $this->db->query("SELECT * FROM member WHERE id = $id");
        return $rs->fetchAll(PDO::FETCH_ASSOC);
    }

    // 获取所有成员记录
    public function fetchAll()
    {
        $rs = $this->db->query("SELECT * FROM member");
        return $rs->fetchAll(PDO::FETCH_ASSOC);
    }

    // 添加成员记录
    public function save()
    {
        // 过滤输入
        $f = array();
        $f['name'] = htmlentities($this->name);
        $f['age'] = htmlentities($this->age);
        $f['type'] = htmlentities($this->type);

        // 验证年龄
        if ($f['age'] < 18) {
            throw new Exception('Member under 18');
        }

        // 根据成员类型自动计算折扣
        switch ($f['type']) {
            case 'silver':
                // 逻辑省略
                break;
            case 'gold':
                // 逻辑省略
                break;
            case 'platinum':
                // 逻辑省略
                break;
        }

        // 插入逻辑示例
        $sql = "INSERT INTO member (name, age, type) VALUES (" . $f['name'] . ", " . $f['age'] . ", '" . $f['type'] . ")";
        $this->db->exec($sql);

        return $this->db->lastInsertId();
    }
}
?>
```




```php
<?php
class MemberModel
{
    protected $db;
    public $id;
    public $name;
    public $age;
    public $type;
    private $rate;

    // 处理成员数据并初始化数据库连接的构造函数
    public function __construct()
    {
        $this->db = new PDO('mysql:dbname=db;host=localhost', 'user', 'pass');
        $this->db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    }

    // get member record by id
    public function fetch($id)
    {
        $id = $this->db->quote($id);
        $rs = $this->db->query("SELECT * FROM member WHERE id = $id");
        return $rs->fetchAll(PDO::FETCH_ASSOC);
    }

    // get all member records
    public function fetchAll()
    {
        $rs = $this->db->query("SELECT * FROM member");
        return $rs->fetchAll(PDO::FETCH_ASSOC);
    }

    // add member record
    public function save()
    {
        // filter input
        $f = array();
        $f['name'] = htmlentities($this->name);
        $f['age'] = htmlentities($this->age);
        $f['type'] = htmlentities($this->type);

        // validate age
        if ($f['age'] < 18) {
            throw new Exception('Member under 18');
        }

        // auto-calculate discount based on membership type
    }
}
?>
```

## 第3章：处理表单

### 注意

装饰器本身是一个非常广泛的话题，本书无法对其进行详尽的细节介绍。前一节介绍的材料应该足够你入门，并帮助你理解本书中用到的相对简单的装饰器。如需更深入的研究，请参考本章末尾的链接。

### 总结

本章重点关注表单：创建表单、验证表单以及处理表单。它向你介绍了 Zend Framework 中三个最重要的组件之一——Zend_Form、Zend_Validate 和 Zend_Filter，并向你展示了如何使用它们安全地请求和处理用户输入。随后，它将这些知识应用于 SQUARE 示例应用程序，引导你完成了为自定义对象注册新命名空间、创建一个邮件查询表单，以及使用 Zend_Mail 组件将通过该表单接收到的输入作为邮件消息发送出去。最后，它快速查看了某些可以帮助你控制表单外观的工具，包括显示组、装饰器和自定义错误消息；你将在全书中看到这些工具的应用。

要了解更多关于本章讨论的话题，请考虑访问以下链接：

- Wikipedia 关于 CSRF 和 XSS 攻击的讨论，位于：[`http://en.wikipedia.org/wiki/Cross-site_request_forgery`](http://en.wikipedia.org/wiki/Cross-site_request_forgery) 和 [`http://en.wikipedia.org/wiki/Cross-site_scripting`](http://en.wikipedia.org/wiki/Cross-site_scripting)
- Wikipedia 关于 CAPTCHAs 的讨论，位于：[`http://en.wikipedia.org/wiki/Captcha`](http://en.wikipedia.org/wiki/Captcha)
- Wikipedia 关于流式接口（fluent interfaces）的讨论，位于：[`http://en.wikipedia.org/wiki/Fluent_interface`](http://en.wikipedia.org/wiki/Fluent_interface)
- Zend Framework 自动加载器，位于：[`http://framework.zend.com/manual/en/zend.loader.autoloader.html`](http://framework.zend.com/manual/en/zend.loader.autoloader.html)
- Zend_Form 组件，位于：[`http://framework.zend.com/manual/en/zend.form.html`](http://framework.zend.com/manual/en/zend.form.html)
- Zend_Filter 组件，位于：[`http://framework.zend.com/manual/en/zend.filter.html`](http://framework.zend.com/manual/en/zend.filter.html)
- Zend_Validate 组件，位于：[`http://framework.zend.com/manual/en/zend.validate.html`](http://framework.zend.com/manual/en/zend.validate.html)
- Zend_Mail 组件，位于：[`http://framework.zend.com/manual/en/zend.mail.html`](http://framework.zend.com/manual/en/zend.mail.html)
- 关于创建自定义装饰器的讨论（Matthew Weier O’Phinney），位于：[`http://weierophinney.net/matthew/archives/213-From-the-inside-out-How-to-layer-decorators.html`](http://weierophinney.net/matthew/archives/213-From-the-inside-out-How-to-layer-decorators.html)

图 3-24：图 3-23 表单的渲染版本

## 第4章：处理模型

### 核心技能与概念

- 理解模型在模型-视图-控制器（MVC）模式中的作用
- 学习“胖模型，瘦控制器”方法的益处
- 将 Doctrine 对象关系映射（ORM）工具包与 Zend Framework 集成
- 使用 Doctrine 模型生成器创建模型
- 使用 Doctrine 模型从 MySQL 数据库检索记录
- 了解如何使用 Zend_Filter_Input 组件过滤输入
- 使用 Zend Framework 引导程序（bootstrapper）微调应用程序的启动过程

上一章带你快速学习了使用 Zend Framework 创建、验证和处理表单的基础知识。然而，表单输入并不会凭空消失在真空中；它必须去某个地方。通常情况下，那个“某个地方”是数据库，例如 MySQL、SQLite 或 PostgreSQL，因此为应用程序添加数据库支持成为应用程序开发人员的一项任务。

不过，数据库只是谜图的一部分：你还需要*模型*来与之交互。模型在逻辑上独立于视图和控制器，充当应用程序的“数据层”，并提供操纵应用程序数据所需的功能。Zend Framework 使编写针对你应用程序需求的模型变得简单许多；你还可以集成由流行的第三方工具（如 Doctrine 或 Propel）生成的模型。本章将把你的 Zend Framework 技能提升几个台阶，向你展示如何向应用程序中创建并添加模型，然后使用这些模型从 MySQL 数据库中检索数据。它还将向你介绍 Doctrine，这是一个强大（且免费）的数据映射工具，可以显著简化这些任务。

### 理解模型



## 第3章：处理表单

***注意***

装饰器本身是一个非常广泛的话题，本书无法对其进行详尽的细节介绍。前一节介绍的材料应该足够你入门，并帮助你理解本书中用到的相对简单的装饰器。如需更深入的研究，请参考本章末尾的链接。

### 总结

本章重点关注表单：创建表单、验证表单以及处理表单。它向你介绍了 Zend Framework 中三个最重要的组件之一——`Zend_Form`、`Zend_Validate` 和 `Zend_Filter`，并向你展示了如何使用它们安全地请求和处理用户输入。随后，它将这些知识应用于 SQUARE 示例应用程序，引导你完成了为自定义对象注册新命名空间、创建一个邮件查询表单，以及使用 `Zend_Mail` 组件将通过该表单接收到的输入作为邮件消息发送出去。最后，它快速查看了某些可以帮助你控制表单外观的工具，包括显示组、装饰器和自定义错误消息；你将在全书中看到这些工具的应用。

要了解更多关于本章讨论的话题，请考虑访问以下链接：

- Wikipedia 关于 CSRF 和 XSS 攻击的讨论，位于：**http://en.wikipedia.org/wiki/Cross-site_request_forgery** 和 **http://en.wikipedia.org/wiki/Cross-site_scripting**

- Wikipedia 关于 CAPTCHAs 的讨论，位于：**http://en.wikipedia.org/wiki/Captcha**

- Wikipedia 关于流式接口（fluent interfaces）的讨论，位于：**http://en.wikipedia.org/wiki/Fluent_interface**

- Zend Framework 自动加载器，位于：**http://framework.zend.com/manual/en/zend.loader.autoloader.html**

- `Zend_Form` 组件，位于：**http://framework.zend.com/manual/en/zend.form.html**

- `Zend_Filter` 组件，位于：**http://framework.zend.com/manual/en/zend.filter.html**

- `Zend_Validate` 组件，位于：**http://framework.zend.com/manual/en/zend.validate.html**

- `Zend_Mail` 组件，位于：**http://framework.zend.com/manual/en/zend.mail.html**

- 关于创建自定义装饰器的讨论（Matthew Weier O’Phinney），位于：**http://weierophinney.net/matthew/archives/213-From-the-inside-out-How-to-layer-decorators.html**

图 3-24：图 3-23 表单的渲染版本

## 第4章：处理模型

### 核心技能与概念

- 理解模型在模型-视图-控制器（MVC）模式中的作用

- 学习“胖模型，瘦控制器”方法的益处

- 将 Doctrine 对象关系映射（ORM）工具包与 Zend Framework 集成

- 使用 Doctrine 模型生成器创建模型

- 使用 Doctrine 模型从 MySQL 数据库检索记录

- 了解如何使用 `Zend_Filter_Input` 组件过滤输入

- 使用 Zend Framework 引导程序（bootstrapper）微调应用程序的启动过程

上一章带你快速学习了使用 Zend Framework 创建、验证和处理表单的基础知识。然而，表单输入并不会凭空消失在真空中；它必须去某个地方。通常情况下，那个“某个地方”是数据库，例如 MySQL、SQLite 或 PostgreSQL，因此为应用程序添加数据库支持成为应用程序开发人员的一项任务。

不过，数据库只是谜图的一部分：你还需要*模型*来与之交互。模型在逻辑上独立于视图和控制器，充当应用程序的“数据层”，并提供操纵应用程序数据所需的功能。Zend Framework 使编写针对你应用程序需求的模型变得简单许多；你还可以集成由流行的第三方工具（如 Doctrine 或 Propel）生成的模型。本章将把你的 Zend Framework 技能提升几个台阶，向你展示如何向应用程序中创建并添加模型，然后使用这些模型从 MySQL 数据库中检索数据。它还将向你介绍 Doctrine，这是一个强大（且免费）的数据映射工具，可以显著简化这些任务。

### 理解模型

到此时，你应该已经对视图和控制器相当熟悉了，它们分别代表符合 MVC 标准的应用程序的“用户界面层”和“处理层”。模型代表“数据层”，负责提供访问数据的通道，并负责维护和执行与该数据相关的任何业务规则。例如，如果你正在为在线图书馆构建一个签入系统，你可能有一个 `Transaction`（事务）模型，它不仅记录书籍借还的详细信息，还包含了规则，不允许单个成员在同一时间借用超过五本书，或者自动计算逾还费用并从相应的成员账户中扣除。同样，如果你正在构建一个航空票务应用程序，你可能有一个 `Ticket`（票务）模型，它不仅能够保存和检索记录，还可以根据特定航班的乘客负载自动增加或减少票价。这里是一个简单模型的示例：

```php
<?php
class MemberModel
{
    protected $db;
    public $id;
    public $name;
    public $age;
    public $type;
    private $rate;

    // 处理成员数据并初始化数据库连接的构造函数
    public function __construct()
    {
        $this->db = new PDO('mysql:dbname=db;host=localhost', 'user', 'pass');
        $this->db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    }

    // get member record by id
    public function fetch($id)
    {
        $id = $this->db->quote($id);
        $rs = $this->db->query("SELECT * FROM member WHERE id = $id");
        return $rs->fetchAll(PDO::FETCH_ASSOC);
    }

    // get all member records
    public function fetchAll()
    {
        $rs = $this->db->query("SELECT * FROM member");
        return $rs->fetchAll(PDO::FETCH_ASSOC);
    }

    // add member record
    public function save()
    {
        // filter input
        $f = array();
        $f['name'] = htmlentities($this->name);
        $f['age'] = htmlentities($this->age);
        $f['type'] = htmlentities($this->type);

        // validate age
        if ($f['age'] < 18) {
            throw new Exception('Member under 18');
        }

        // auto-calculate discount based on membership type
    }
}
?>
```



## 第3章：处理表单

***注意***

装饰器本身是一个非常广泛的话题，本书无法对其进行详尽的细节介绍。前一节介绍的材料应该足够你入门，并帮助你理解本书中用到的相对简单的装饰器。如需更深入的研究，请参考本章末尾的链接。

### 总结

本章重点关注表单：创建表单、验证表单以及处理表单。它向你介绍了 Zend Framework 中三个最重要的组件之一——`Zend_Form`、`Zend_Validate` 和 `Zend_Filter`，并向你展示了如何使用它们安全地请求和处理用户输入。随后，它将这些知识应用于 SQUARE 示例应用程序，引导你完成了为自定义对象注册新命名空间、创建一个邮件查询表单，以及使用 `Zend_Mail` 组件将通过该表单接收到的输入作为邮件消息发送出去。最后，它快速查看了某些可以帮助你控制表单外观的工具，包括显示组、装饰器和自定义错误消息；你将在全书中看到这些工具的应用。

要了解更多关于本章讨论的话题，请考虑访问以下链接：

- Wikipedia 关于 CSRF 和 XSS 攻击的讨论，位于：`http://en.wikipedia.org/wiki/Cross-site_request_forgery` 和 `http://en.wikipedia.org/wiki/Cross-site_scripting`

- Wikipedia 关于 CAPTCHAs 的讨论，位于：`http://en.wikipedia.org/wiki/Captcha`

- Wikipedia 关于流式接口（fluent interfaces）的讨论，位于：`http://en.wikipedia.org/wiki/Fluent_interface`

- Zend Framework 自动加载器，位于：`http://framework.zend.com/manual/en/zend.loader.autoloader.html`

- `Zend_Form` 组件，位于：`http://framework.zend.com/manual/en/zend.form.html`

- `Zend_Filter` 组件，位于：`http://framework.zend.com/manual/en/zend.filter.html`

- `Zend_Validate` 组件，位于：`http://framework.zend.com/manual/en/zend.validate.html`

- `Zend_Mail` 组件，位于：`http://framework.zend.com/manual/en/zend.mail.html`

- 关于创建自定义装饰器的讨论（Matthew Weier O’Phinney），位于：`http://weierophinney.net/matthew/archives/213-From-the-inside-out-How-to-layer-decorators.html`

图 3-24：图 3-23 表单的渲染版本

## 第4章：处理模型

### 核心技能与概念

- 理解模型在模型-视图-控制器（MVC）模式中的作用

- 学习“胖模型，瘦控制器”方法的益处

- 将 Doctrine 对象关系映射（ORM）工具包与 Zend Framework 集成

- 使用 Doctrine 模型生成器创建模型

- 使用 Doctrine 模型从 MySQL 数据库检索记录

- 了解如何使用 `Zend_Filter_Input` 组件过滤输入

- 使用 Zend Framework 引导程序（bootstrapper）微调应用程序的启动过程

上一章带你快速学习了使用 Zend Framework 创建、验证和处理表单的基础知识。然而，表单输入并不会凭空消失在真空中；它必须去某个地方。通常情况下，那个“某个地方”是数据库，例如 MySQL、SQLite 或 PostgreSQL，因此为应用程序添加数据库支持成为应用程序开发人员的一项任务。

不过，数据库只是谜图的一部分：你还需要*模型*来与之交互。模型在逻辑上独立于视图和控制器，充当应用程序的“数据层”，并提供操纵应用程序数据所需的功能。Zend Framework 使编写针对你应用程序需求的模型变得简单许多；你还可以集成由流行的第三方工具（如 Doctrine 或 Propel）生成的模型。本章将把你的 Zend Framework 技能提升几个台阶，向你展示如何向应用程序中创建并添加模型，然后使用这些模型从 MySQL 数据库中检索数据。它还将向你介绍 Doctrine，这是一个强大（且免费）的数据映射工具，可以显著简化这些任务。

### 理解模型

到此时，你应该已经对视图和控制器相当熟悉了，它们分别代表符合 MVC 标准的应用程序的“用户界面层”和“处理层”。模型代表“数据层”，负责提供访问数据的通道，并负责维护和执行与该数据相关的任何业务规则。例如，如果你正在为在线图书馆构建一个签入系统，你可能有一个 `Transaction`（事务）模型，它不仅记录书籍借还的详细信息，还包含了规则，不允许单个成员在同一时间借用超过五本书，或者自动计算逾还费用并从相应的成员账户中扣除。同样，如果你正在构建一个航空票务应用程序，你可能有一个 `Ticket`（票务）模型，它不仅能够保存和检索记录，还可以根据特定航班的乘客负载自动增加或减少票价。这里是一个简单模型的示例：

```php
<?php
class MemberModel
{
    protected $db;
    public $id;
    public $name;
    public $age;
    public $type;
    private $rate;

    // 处理成员数据并初始化数据库连接的构造函数
    public function __construct()
    {
        $this->db = new PDO('mysql:dbname=db;host=localhost', 'user', 'pass');
        $this->db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    }

    // get member record by id
    public function fetch($id)
    {
        $id = $this->db->quote($id);
        $rs = $this->db->query("SELECT * FROM member WHERE id = $id");
        return $rs->fetchAll(PDO::FETCH_ASSOC);
    }

    // get all member records
    public function fetchAll()
    {
        $rs = $this->db->query("SELECT * FROM member");
        return $rs->fetchAll(PDO::FETCH_ASSOC);
    }

    // add member record
    public function save()
    {
        // filter input
        $f = array();
        $f['name'] = htmlentities($this->name);
        $f['age'] = htmlentities($this->age);
        $f['type'] = htmlentities($this->type);

        // validate age
        if ($f['age'] < 18) {
            throw new Exception('Member under 18');
        }

        // auto-calculate discount based on membership type
    }
}
?>
```



```php
<?php
class MemberModel
{
    protected $db;
    public $id;
    public $name;
    public $age;
    public $type;
    private $rate;

    // 处理成员数据并初始化数据库连接的构造函数
    public function __construct()
    {
        $this->db = new PDO('mysql:dbname=db;host=localhost', 'user', 'pass');
        $this->db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    }

    // get member record by id
    public function fetch($id)
    {
        $id = $this->db->quote($id);
        $rs = $this->db->query("SELECT * FROM member WHERE id = $id");
        return $rs->fetchAll(PDO::FETCH_ASSOC);
    }

    // get all member records
    public function fetchAll()
    {
        $rs = $this->db->query("SELECT * FROM member");
        return $rs->fetchAll(PDO::FETCH_ASSOC);
    }

    // add member record
    public function save()
    {
        // filter input
        $f = array();
        $f['name'] = htmlentities($this->name);
        $f['age'] = htmlentities($this->age);
        $f['type'] = htmlentities($this->type);

        // validate age
        if ($f['age'] < 18) {
            throw new Exception('Member under 18');
        }

        // auto-calculate discount based on membership type
    }
}
?>
```

# Zend Framework：入门指南

Fowler、Jamis Buck 和 Chris Hartjes（你可以在本章末尾找到链接）建议，尽可能将业务逻辑放置在模型（models）中，而不是控制器（controllers）中。这种方法具有许多优势：

- “胖”模型（Fat models）通过将关键业务规则封装到可重用的对象和对象方法中，减少了重复并帮助开发者遵循“不要重复自己”（DRY）原则。随后可以使用继承链在整个应用程序中一致地应用这些规则。使用 OOP 原则指定模型还允许根据需要用额外功能扩展基模型，并在较大的应用程序空间内区分模型的公共属性和私有属性。

- 自足的“胖”模型封装了其正常运行所需的所有业务规则，比依赖应用程序控制器来执行业务规则的“瘦”模型（thin models）更具移植性。由于应用程序的大部分业务逻辑都在模型中而不是控制器中，切换到不同的框架（例如）会变得容易得多，因为模型可以简单地替换到新系统中，通常不需要重大的重构即可工作。

- 当“胖”模型处理了大部分繁重工作时，控制器通常只包含几行高度集中的代码。这使得它们更容易理解和阅读，并有助于提高整体性能（因为控制器的调用频率通常比模型高）。它还产生了更具维护性的代码：例如，如果你需要更改特定应用程序实体的业务规则，只需要更新该实体的模型，而无需更新它的所有控制器。

- 在“胖模型、瘦控制器”方法下，调试和测试变得更加透明，因为通常非常容易识别错误源于模型还是控制器，并以对应用程序其他部分影响最小的方式对其进行纠正。

此时需要注意的是，Zend Framework 并不带有一个 `Zend_Model` 组件或一组预定义的模型供你直接“丢入”应用程序中运行；你总是需要创建自己的模型。

**Q：“模型”仅仅是一组预包的 SQL 语句吗？**

**A：** 不，绝对不是。一种常见的误区是认为模型仅仅是数据库对象的表示，其方法对应 SQL 的 `INSERT`、`SELECT`、`UPDATE` 和 `DELETE` 语句。实际上，模型远比结构化查询语言（SQL）封装器得多。它们可以（并且应该）强制执行特定的业务规则、执行计算、处理转换、应用过滤器并对数据执行任何其他需要的操作。记住，模型越智能，控制器的工作就越少，你的应用程序的可维护性和移植性就越高。

## 第 4 章：使用模型

Zend Framework 包含了许多可以帮助你完成此任务的工具，例如 `Zend_Db_Adapter` 数据库抽象层和用于表操作的 `Zend_Db_Table` 接口。不过，你也可以使用第三方工具 Doctrine 或 Propel 创建应用程序模型，并将其集成到你的 Zend Framework 应用程序中。事实上，这正是下一节的重点。

### 安装 Doctrine

虽然你完全可以使用 Zend Framework 提供的组件从零开始创建应用程序模型，但有一种更简单的方法：使用对象关系映射（ORM）工具为你自动生成它们。这些工具可以自动扫描现有数据库，并使用 ActiveRecord 模式或 DataMapper 模式创建与表对应的模型类。随后，将这些自动生成的模型添加到应用程序并根据需要进行扩展以支持特定需求，就是一项简单的任务了。

PHP 有许多免费的开源 ORM 工具可用，如 Doctrine、RedBean 和 Elo。本书使用了 Doctrine，由于其易用性、灵活性和详尽的文档，它在开发者中非常受欢迎。Doctrine 软件包包含一个支持大多数常用 RDBMS 系统的数据库抽象层；一种名为 Doctrine Query Language (DQL) 的自定义 SQL 版本；以及从现有架构自动生成模型类的工具。这些模型类基于 ActiveRecord 模式并完全符合 PHP 标准。

要开始使用 Doctrine，请访问官方网站下载并安装最新版本到你的开发环境中。然后，将其内容解压到文件系统上的临时区域：

```bash
cd /tmp
tar -xzvf Doctrine-*.tgz
```

你最终将得到类似于图 4-1 的目录结构。`lib/` 目录包含所有的 Doctrine 组件，而 `tests/` 目录包含测试用例。应将 `lib/` 目录的内容移动到 PHP“包含路径”列表中的某个位置。

在 UNIX/Linux 系统上，良好的位置是 `/usr/local/lib/php` 或 `/usr/local/share/php`。在 Windows 上，考虑使用你的 PHP 或 PEAR 安装目录，例如 `C:\Program Files\PHP` 或 `C:\Program Files\PHP\PEAR`。注意，如果目标目录尚未成为 PHP“包含路径”列表的一部分，必须在继续之前添加它。

以下是可以用于执行这些任务的示例命令：

```bash
cd Doctrine-*
mv lib /usr/local/lib/php/Doctrine
```

你现在应该能够从 PHP 脚本中访问 Doctrine 了。要验证这一点，请创建以下简单脚本，记得将凭据替换为适用于你系统的值：

```php
<?php
//  Doctrine 主文件
include_once 'Doctrine/Doctrine.php';
spl_autoload_register(array('Doctrine', 'autoload'));

// 创建 Doctrine 管理器
$manager = Doctrine_Manager::getInstance();

// 创建数据库连接
$conn = Doctrine_Manager::connection('mysql://root@localhost/test');

// 获取并打印数据库列表
$databases = $conn->listDatabases();
print_r($databases);
?>
```

将此脚本保存为 `/tmp/doctrine-test.php` 并通过以下 PHP 命令行界面 (CLI) 执行它：

```bash
cd /tmp
php ./doctrine-test.php
```

图 4-2 展示了你将看到的输出示例。

### 生成并集成 Doctrine 模型

一旦安装并运行了 Doctrine，就可以开始使用它创建模型了。你可以将这些模型添加到示例应用程序中，并进行设置以便根据需要自动加载。后续章节将讨论如何完成这些任务。

### 初始化应用程序数据库

第一步是为应用程序创建一个 MySQL 数据库。要执行此操作，进入命令行提示符，启动 MySQL 命令行客户端并使用以下命令创建一个新数据库：

```bash
mysql -u root -p
Enter password: ********
Welcome to the MySQL monitor. Commands end with ; or \g.
Your MySQL connection id is 17
Server version: 5.1.30-community MySQL Community Server (GPL)
CREATE DATABASE square;
Query OK, 0 rows affected (0.00 sec)
USE square;
Database changed
```

按照如下代码向此数据库添加一些表：

```sql
CREATE TABLE IF NOT EXISTS country (
    CountryID INT(11) NOT NULL AUTO_INCREMENT,
    CountryName VARCHAR(255) NOT NULL,
    PRIMARY KEY (CountryID)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
Query OK, 0 rows affected (0.09 sec)

CREATE TABLE IF NOT EXISTS grade (
    GradeID INT(11) NOT NULL AUTO_INCREMENT,
    GradeName VARCHAR(255) NOT NULL,
    PRIMARY KEY (GradeID)
);
```

Zend Framework：入门指南

```sql
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

Query OK, 0 rows affected (0.09 sec)

mysql> CREATE TABLE IF NOT EXISTS type (
    TypeID INT(11) NOT NULL AUTO_INCREMENT,
    TypeName VARCHAR(255) NOT NULL,
    PRIMARY KEY (TypeID)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

Query OK, 0 rows affected (0.09 sec)

mysql> CREATE TABLE IF NOT EXISTS item (
    RecordID INT(11) NOT NULL AUTO_INCREMENT,
    RecordDate DATE NOT NULL,
    SellerName VARCHAR(255) NOT NULL,
    SellerEmail VARCHAR(255) NOT NULL,
    SellerTel VARCHAR(50) DEFAULT NULL,
    SellerAddress TEXT,
    Title VARCHAR(255) NOT NULL,
    `Year` INT(4) NOT NULL,
    CountryID INT(4) NOT NULL,
    Denomination FLOAT NOT NULL,
    TypeID INT(4) NOT NULL,
    GradeID INT(4) NOT NULL,
    SalePriceMin FLOAT NOT NULL,
    SalePriceMax FLOAT NOT NULL,
    Description TEXT NOT NULL,
    DisplayStatus TINYINT(1) NOT NULL,
    DisplayUntil DATE DEFAULT NULL,
    PRIMARY KEY (RecordID)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

Query OK, 0 rows affected (0.09 sec)

mysql> CREATE TABLE IF NOT EXISTS user (
    RecordID INT(4) NOT NULL AUTO_INCREMENT,
    Username VARCHAR(10) NOT NULL,
    Password TEXT NOT NULL,
    PRIMARY KEY (RecordID)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

Query OK, 0 rows affected (0.09 sec)

mysql> CREATE TABLE IF NOT EXISTS log (
    RecordID int(11) NOT NULL AUTO_INCREMENT,
    LogMessage text NOT NULL,
    LogLevel varchar(30) NOT NULL,
    LogTime varchar(30) NOT NULL,
    Stack text,
    Request text,
    PRIMARY KEY (RecordID)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

Query OK, 0 rows affected (0.09 sec)
```

## 第 4 章：模型模型

表 4-1 简要描述了这些表。

为了更好地理解这些表是如何连接的，请查看图 4-3，该图展示了本章 MySQL 数据库的实体关系图。

继续初始化主表并插入一些记录：

```sql
mysql> INSERT INTO country (CountryID, CountryName) VALUES
    (1, 'United States'),
    (2, 'United Kingdom'),
    (3, 'India'),
    (4, 'Singapore'),
    (5, 'Germany'),
    (6, 'France'),
    (7, 'Italy'),
```

### 表 4-1：应用数据库简述

| 表名 | 包含内容 |
| :--- | :--- |
| *item* | 可售邮票列表，以及卖家的联系信息 |
| *user* | 授权用户列表 |
| *country* | 国家主列表 |
| *grade* | 邮票等级主列表 |
| *type* | 邮票类型主列表 |
| *log* | 错误日志 |

**Q：如果 Zend Framework 的约定是使用大驼峰命名（upper camel-casing）实体名称，为什么本章中的 MySQL 数据库和表名指定为小写？**

**A：** 在文件系统层面，MySQL 分别将数据库和表表示为目录和文件。某些文件系统（例如 Windows）不区分文件名的大小写，而另一些（例如 Linux）则区分。因此，为了简化在不同操作系统之间迁移数据库和表，通常建议将全部小写，并确保它们仅包含字母、数字和下划线。显然，你还应该尝试避免使用 MySQL 的保留关键字作为数据库名。

**专家问**

*(继续)*

```sql
    (8, 'Spain'),
    (9, 'Hungary');

Query OK, 9 rows affected (0.09 sec)
Records: 9  Duplicates: 0  Warnings: 0

mysql> INSERT INTO grade (GradeID, GradeName) VALUES
    (1, 'Very Fine'),
    (2, 'Fine'),
    (3, 'Good'),
    (4, 'Average'),
    (5, 'Poor');

Query OK, 5 rows affected (0.09 sec)
Records: 5  Duplicates: 0  Warnings: 0

mysql> INSERT INTO type (TypeID, TypeName) VALUES
    (1, 'Commemorative'),
    (2, 'Decorative'),
    (3, 'Definitive'),
    (4, 'Special'),
    (5, 'Other');
```

图 4-3：应用数据库的实体关系图



![](img/222e7e58871b088cc6397852e1452b57_130_0.png)

你也可以向`item`表插入一些虚拟记录以使其运行起来：

```
mysql> INSERT INTO item (RecordID, RecordDate, SellerName, SellerEmail, SellerTel, SellerAddress, Title, `Year`, CountryID, Denomination, TypeID, GradeID, SalePriceMin, SalePriceMax, Description, DisplayStatus, DisplayUntil) VALUES
-> (1, '2023-01-01', 'John Doe', 'john@example.com', '123456', '123 Main St', 'Penny Black', 1840, 2, 1.0, 5, 2, 100.00, 200.00, 'A rare stamp', 1, NULL),
-> (2, '2023-02-01', 'Jane Smith', 'jane@example.com', '654321', '456 Oak Ave', 'Inverted Jenny', 1918, 1, 2.5, 4, 3, 50.00, 80.00, 'Good condition', 1, NULL);
```

Query OK, 2 rows affected (0.09 sec)

Records: 2 Duplicates: 0 Warnings: 0

## 第 4 章：使用模型

115

生成的模型类文件，移除由 Doctrine 自动添加的前缀。

这是一个示例：

```
shell> cd library/Square/Model
shell> mv Square_Model_BaseCountry.php BaseCountry.php
```

在过程结束后，你应该得到一个类似于图 4-5 的结构。

**提示**

如果你在使用 Doctrine v1.2，可以向`generateModelsFromDb()`方法传递一个额外的`'classPrefixFiles'`选项。这指定了是否要在模型文件名中添加类前缀。将此设置为`'false'`可以减少将 Doctrine 模型集成到你的应用程序中的工作量，因为不再需要重命名每个模型文件以符合 Zend Framework 的规范。

请注意，Doctrine 将数据库中的每个表映射到两个模型类：一个基类（base class）和一个子类（child class）。基类继承自`Doctrine_Record`类，包含了表定义，并通过继承暴露了所有常用数据库操作的方法。子类是派自基类的存根类（stub class），作为你可能想要添加到模型中的任何自定义方法的容器。

### 设置模型关系

现在，虽然 Doctrine 可以生成与单个表对应的模型并暴露对这些表进行常用操作的方法，但它并不具备自动检测表之间关系的智能。然而，这些关系在实际使用中通常至关重要，因此需要应用程序开发者通过将模型连接来定义这些关系。

Doctrine 使得仅使用两个方法就可以复制 RDBMS 中可能的所有不同类型的关系——一对一、一对多、多对多和自引用——这两个方法分别是：`hasOne()`和`hasMany()`。这两个方法都接受两个参数：关系中使用的另一个模型的名称，以及一个指定关系参数的选项数组。

为了确保这些关系在模型实例化时自动加载，它们应该在模型的`setUp()`方法中使用。

图 4-5

集成到应用程序后自动生成的 Doctrine 模型

![](img/225)

*(续上)*

116

Zend Framework：初学者指南

要理解其工作原理，请翻回几页查看图 4-3，该图说明了各种数据库表之间的关系。从图 4-3 可以清楚地看到，`country`（国家）、`grade`（等级）和`type`（类型）主表与`item`（项目）表之间存在`1:n`关系。这种关系利用了`item.CountryID`、`item.GradeID`和`item.TypeID`外键字段，并且可以通过向`Item`模型类中添加以下代码在 Doctrine 中表示：

```php
<?php

class Square_Model_Item extends Square_Model_BaseItem
{
    public function setUp()
    {
        $this->hasOne('Square_Model_Grade', array(
            'local' => 'GradeID',
            'foreign' => 'GradeID'
        ));

        $this->hasOne('Square_Model_Country', array(
            'local' => 'CountryID',
            'foreign' => 'CountryID'
        ));

        $this->hasOne('Square_Model_Type', array(
            'local' => 'TypeID',
            'foreign' => 'TypeID'
        ));
    }
}
```

在这里，`setUp()`方法负责自动定义`Item`模型与`Country`、`Grade`以及`Item`模型之间的外键关系。这在 Doctrine 查询中连接这些表时（正如你很快将看到的）非常非常有用。

### 自动加载 Doctrine

现在剩下的就是让 Zend Framework 应用程序和 Doctrine 能够良好通信。有许多方法可以实现这一点，但推荐的方法是在应用程序的引导文件（bootstrap file）中初始化 Doctrine，并配置其按需“懒加载（lazy load）”模型。这种方法得到了 Matthew Weir O’Phinney 和 Eric LeClerc 等领先 Zend Framework 开发者的推崇，你可以在本末尾找到他们工作的链接。

第一步是决定是将 Doctrine 库包含在你的应用程序中，还是允许用户自行下载并安装这些库。要理解这些选项的优缺点，请回顾第 1 章，当时你曾对 Zend Framework 库做过类似的决定。遵循之前的决定，让我们假设 Doctrine 库将与应用程序捆绑。因此，使用以下命令将 Doctrine `lib/`目录的内容拷贝到`$APP_DIR/library/Doctrine`：

```
shell> cp -R /usr/local/lib/php/Doctrine library/
```

下一步是更新应用程序配置文件，路径为`$APP_DIR/application/configs/application.ini`，使用 Doctrine 可用于连接到之前创建的 MySQL 数据库的数据源名称（DSN）。要执行此更新，请用文本编辑器打开应用程序配置文件，并在`[production]`部分添加以下几行：

```
doctrine.dsn = "mysql://square:square@localhost/square"
```

最后一步是通过向应用程序添加必要的代码来初始化 Doctrine。

117

第 4 章：使用模型

118

Zend Framework：初学者指南

方法并由引导程序（bootrapper）自动执行。前面的列表定义了`_initDoctrine()`资源，它首先包含主类，并使用有关如何加载类的信息来配置自动加载器。然后它创建了一个`Doctrine_Manager`实例，配置了 Doctrine 懒加载，从应用程序配置中读取 DSN，并打开数据库的连接。由于此方法会在每次请求时自动执行，因此 Doctrine 模型可以在任何应用程序控制器中使用。

```php
<?php

class Bootstrap extends Zend_Application_Bootstrap
{
    protected function _initDoctrine()
    {
        require_once 'Doctrine.php';
        $this->getApplication()
            ->getAutoloader()
            ->pushAutoloader(array('Doctrine', 'autoload'));

        $manager = Doctrine_Manager::getInstance();
        $manager->setAttribute(Doctrine::MODEL_LOADING, Doctrine::CONSERVATIVE);

        $config = $this->getOption('doctrine');
        $conn = Doctrine_Manager::connection($config['dsn']);

        return $conn;
    }
}
```

等等，在继续之前之前，让我们快速进入 Doctrine 模型的世界。正如之前讨论的那样，Doctrine 模型实现了活动记录（ActiveRecord）模式，其中模型类的每个实例代表底层表的一条记录，实例的每个属性代表记录的字段。模型继承自`Doctrine_Record`基类，该类暴露了许多简化添加、编辑、删除和搜索记录的方法。接下来的章节将详细介绍这些方面。

### 获取记录

使用 Doctrine 模型获取记录有几种不同的方法。如果你有记录的主键，一种方法是直接使用`find()`方法，如下：

```php
<?php

$member = Doctrine::getTable('Member')->find(1);

var_dump($member->toArray());

?>
```

如果你更倾向于获取所有可用记录，可以使用`findAll()`方法，如下：

```php
<?php

$members = Doctrine::getTable('Members')->findAll();

var_dump($members->toArray());

?>
```

Doctrine 自带了一种名为 Doctrine 查询语言（DQL）的 SQL 变体，它为创建和执行数据库查询提供了灵活的接口。这为从数据库中获取记录提供了另一种、更灵活的方案。考虑以下简单的示例，它以数组形式获取所有成员记录：

```php
<?php

$q = Doctrine_Query::create()
    ->from('Member m');

$result = $q->fetchArray();

?>
```

## 第 4 章：与模型交互

### 使用过滤器

`Doctrine_Query`类暴露了一个流式接口，这意味着为此查询添加分层非常简单。例如，假设你只想检索激活状态的成员账户记录。你可以使用`where()`方法为查询添加此条件，如下文所示：

```php
<?php

$q = Doctrine_Query::create()
->from('Member m')
->where('m.Status = ?', 1);

$result = $q->fetchArray();

?>
```

你可以通过`addWhere()`方法以这种方式为查询附加多个过滤器。这里有一个检索位于英国的活跃成员记录示例：

```php
<?php

$q = Doctrine_Query::create()
->from('Member m')
->where('m.Status = ?', 1)
->addWhere('m.Location = ?', 'UK');

$result = $q->fetchArray();

?>
```

### 结果的分组与排序

你可以使用`orderBy()`和`groupBy()`方法对结果集进行分组和排序。这里有一个按国家对成员进行分组和排序的示例：

```php
<?php

$q = Doctrine_Query::create()
->from('Member m')
->where('m.Status = ?', 1)
->groupBy('m.Location')
->orderBy('m.Location DESC');

$result = $q->fetchArray();

?>
```

### 表格连接

你也可以使用 DQL 通过`leftJoin()`和`innerJoin()`方法执行表与之间的连接。这里有一个左连接的示例：

```php
<?php

$q = Doctrine_Query::create()
->from('Member m')
->leftJoin('m.Country c')
->leftJoin('m.OrgType o')
->where('o.DisplayStatus = 1');

$result = $q->execute();

?>
```

这里是一个内连接的示例：

```php
<?php

$q = Doctrine_Query::create()
->from('Member m')
->innerJoin('m.Country c');

$result = $q->execute();

?>
```

用于连接的字段是由 Doctrine 根据源模型`setUp()`方法中定义的关系自动设置的。

**提示**

在使用 DQL 时，你可能需要查看特定查询的自动生成代码。Doctrine 允许通过其`getSql()`方法来实现，该方法返回查询的原始 SQL 以供检查。

### 添加、更新和删除记录

使用 Doctrine 模型向数据库中添加新记录非常简单：只需实例化模型类的实例，将字段值设为模型属性，并调用模型的`save()`方法即可。这里有一个示例：

```php
<?php

$member = new Member;
$member->FirstName = 'Jack';
$member->LastName = 'Frost';
$member->Email = 'jack@example.com';
$member->JoinDate = '2009-11-11';
$member->Status = 1;
$id = $member->save();

?>
```

**Q:** **DQL 支持右连接吗？**

**A:** 不支持。DQL 目前仅支持左连接和内连接。但不应该影响你的进度，因为左连接和右连接是互换的，取决于你站在连接的哪侧。为了说明这一点，请考虑以下两个等效的查询：

```
SELECT * FROM c LEFT JOIN a USING (id);
SELECT * FROM a RIGHT JOIN c USING (id);
```

要更新现有记录，可以使用`find()`方法或 DQL 查询检索它，更新必要的属性，并使用`save()`方法将其保存回数据库。这里有一个示例：

```php
<?php

$member = Doctrine::getTable('Member')->find(1);
$member->FirstName = 'John';
$member->Status = 2;
$member->save();

?>
```

为了更精确的控制，你还可以使用 DQL 的`update()`方法更新记录。这里有一个示例，与上一个等效：

```php
<?php

$q = Doctrine_Query::create()
->update('Member m')
->set('m.FirstName', '?', 'John')
->set('m.Status', '?', '2')
->addWhere('m.RecordID = ?', 1);
$q->execute();

?>
```

同样，你可以通过调用模型的`delete()`方法或使用 DQL 查询来删除记录。以下列表展示了这两种方法：

```php
<?php

// 使用模型方法
$member = Doctrine::getTable('Member')->find(11);
$member->delete();

// 使用 DQL
$q = Doctrine_Query::create()
->delete('Member m')
->addWhere('m.RecordID = ?', 11);
$q->execute();

?>
```

虽然对 Doctrine 包的完整解释超出了本书的范围，但前面的示例应该让你对模型操作的基础知识有所见解，并为你理解后续章节的内容奠定基础。更多信息和更多示例，请参考本章末尾的链接。

### 检索数据库记录

现在你已经了解了一些 Doctrine 模型是如何工作的，那么用它做些实用的操作如何？下面的部分将向你如何使用这些模型从数据库中检索单个列表，对其进行格式化，并在应用程序环境中显示它们。

#### 创建新模块

到为止，所有的示例都在“default”模块下创建。然而，使用模块化布局的优势之一是允许将逻辑相关的控制器组合在一起，从而产生更具维护性和组织性的代码树。基于此，创建一个名为“catalog”的新模块，它将包含与添加、检索列表相关的控制器和视图。要创建这个“catalog”模块，切换到`$APP_DIR/application/`并执行以下命令：

```shell
mkdir modules/catalog
mkdir modules/catalog/controllers
mkdir modules/catalog/views
mkdir modules/catalog/views/scripts
```

## 定义自定义路由



接下来，为显示 URL 定义一个路由。为了简单起见，我们假设所有显示 URL 的格式均为 `/catalog/item/display/xx`，其中 `xx` 是记录 ID。设置处理此类 URL 的自定义路由，请在 `$APP_DIR/application/configs/application.ini` 中添加以下路由定义：

```
resources.router.routes.catalog-display.route = /catalog/item/display/:id
resources.router.routes.catalog-display.defaults.module = catalog
resources.router.routes.catalog-display.controller = item
resources.router.routes.catalog-display.action = display
```

#### 定义控制器

下一步是对应前面的路由定义定义控制器和 action。按照习惯，此控制器将位于 `$APP_DIR/application/modules/catalog/controllers/ItemController.php`。它的样子如下：

```php
<?php

class Catalog_ItemController extends Zend_Controller_Action
{
    public function init()
    {
    }

    // 显示物品的 action
    public function displayAction()
    {
        // 为 input 设置过滤器和验证器
        $filters = array(
            'id' => array('HtmlEntities', 'StripTags', 'StringTrim')
        );

        $validators = array(
            'id' => array('NotEmpty', 'Int')
        );

        // 测试输入是否有效
        // 检索记录
        // 附加到视图
        $input = new Zend_Filter_Input($filters, $validators);
        $input->setData($this->getRequest()->getParams());

        if ($input->isValid()) {
            $q = Doctrine_Query::create()
                ->from('Model_Item i')
                ->leftJoin('i.Country c')
                ->leftJoin('i.Model_Grade g')
                ->leftJoin('i.Model_Type t')
                ->where('i.RecordID = ?', $input->id);

            $result = $q->fetchArray();

            if (count($result) == 1) {
                $this->view->item = $result[0];
            } else {
                throw new Zend_Controller_Exception('Page not found', 404);
            }
        } else {
            throw new Zend_Controller_Exception('Invalid input');
        }
    }
}
```

**注意**

在 Zend Framework 下，每个模块（“default”模块除外）都有自己的命名空间以防止对象和变量冲突。你可以在 `Catalog_ItemController` 中看到这一点，模块名作为类名前缀创建一个自定义命名空间。

在本示例中，`displayAction()` 方法首先检索输入变量 `$_GET['id']` 的值，然后将此值引入 Doctrine 查询，尝试在数据库中查找匹配记录。如果查询返回单个记录，则将结果作为关联数组分配给视图。如果没有找到或多个匹配，将抛出 404 异常并传递给默认异常处理器，将其格式化为可读的错误页面并显示给客户端。

此列表还引入了一个新组件 `Zend_Filter_Input`。正如名称所示，该组件提供了一种过滤和验证输入的替代方法，在用户输入不是通过表单时（例如在本示例中，记录 ID 作为 URL 参数提交）非常有用。第 3 章中讨论的所有过滤器和验证器也可以配合 `Zend_Filter_Input` 使用。

它是如何工作的？`Zend_Filter_Input` 类构造函数接受三个参数——过滤器数组、验证器数组和要测试的输入数据数组——并在第三个上运行前两个。你也可以使用 `setData()` 方法单独指定输入数据数组。例如，在上列表中，`$_GET['id']` 变量首先使用 `HtmlEntities`、`StripTags` 和 `StringTrim` 过滤器进行过滤，然后检查它是整数。与 `Zend_Form` 一样，有一个 `isValid()` 方法根据数据是否有效返回布尔 `true` 或 `false`；它可以作为 action 业务逻辑的条件封装。

#### 定义视图

假设请求的记录 ID 有效并在数据库中找到了匹配记录，控制器将渲染相应的视图，按照习惯，它应该存储在 `$APP_DIR/application/modules/catalog/views/scripts/item/display.phtml`。它的样子如下：

```html
<h2>查看物品</h2>
<h3>
出售中：
<?php echo $this->escape($this->item['Title']); ?> -
<?php echo $this->escape($this->item['Year']); ?> -
<?php echo $this->escape($this->item['Model_Grade']['GradeName']); ?>
</h3>
<div id="container">
  <div id="record">
    <table>
      <tr>
        <td class="key">标题：</td>
        <td class="value">
          <?php echo $this->escape($this->item['Title']); ?>
        </td>
      </tr>
```

```php
<?php echo $this->escape(
$this->item['Square_Model_Type']['TypeName']); ?>
</td>
</tr>
<tr>
<td class="key">年份:</td>
<td class="value">
<?php echo $this->escape($this->item['Year']); ?>
</td>
</tr>
<tr>
<td class="key">国家:</td>
<td class="value">
<?php echo $this->escape(
$this->item['Square_Model_Country']['CountryName']); ?>
</td>
</tr>
<tr>
<td class="key">面额:</td>
<td class="value">
<?php echo $this->escape(
sprintf('%01.2f', $this->item['Denomination'])); ?>
</td>
</tr>
<tr>
<td class="key">等级:</td>
<td class="value">
<?php echo $this->escape(
$this->item['Square_Model_Grade']['GradeName']); ?>
</td>
</tr>
<tr>
<td class="key">售价:</td>
<td class="value">
$<?php echo $this->escape($this->item['SalePriceMin']); ?> -
$<?php echo $this->escape($this->item['SalePriceMax']); ?>
</td>
</tr>
<tr>
<td class="key">描述:</td>
<td class="value">
<?php echo $this->escape($this->item['Description']); ?>
</td>
</tr>
</table>
</div>
</div>
```

这里没什么复杂的。此视图脚本只是重新格式化了上一步中模型检索的记录，并以一种可用且可读的格式显示它。注意使用 `escape()` 方法在将输出显示给用户之前自动对视图输出进行转义。

要查看效果，请尝试在浏览器中访问 URL `http://square.localhost/catalog/item/1`。如果一切运行正常，控制器将从数据库中检索 ID 为 #1 的记录（你还记得我们在初始化数据库时手动添加了这条记录），将其分配给视图并进行渲染。输出应该类似于图 4-6 所示。

作为测试，你也可以再次访问相同的 URL，但使用无效或缺失的记录 ID。你应该能看到“未找到页面”或“输入无效”错误，如图 4-7 所示。

图 4-6 成功检索数据库记录的结果

![](img/222e7e58871b088cc6397852e1452b57_144_0.png)

图 4-7 尝试检索失败的结果

![](img/222e7e58871b088cc6397852e1452b57_144_1.png)

### 总结

虽然之前的章节重点关注视图和控制器，但本章侧重于模型：它们是什么、如何工作，以及在 MVC 应用中扮演着什么角色。尽管 Zend Framework 没有附带专门的模型组件，但你仍然很容易创建自己的模型或将第三方模型（例如由 Doctrine ORM 包生成的模型）集成到 Zend Framework 应用中。本章演示了这一过程，向你展示了如何创建 Doctrine 模型并配置它们在 Zend Framework 应用环境中运行。它还向你介绍了 `Zend_Filter_Input` 组件，这是一个用于即时输入过滤和验证的实用工具，以及 `Bootstrap` 类，它提供了一个运行时初始化应用程序资源的框架。

SQUARE 示例应用程序现在也变得智能得多。它拥有用于持久化存储的数据库，以及可以与其交互以检索和显示数据库记录的控制器。更重要的是，它终于有一组健壮且可扩展的模型。这不仅将简化数据访问和操作，还将为书中后续章节讨论的更高级的功能提供基础。

要了解更多关于本章讨论的话题，请考虑访问以下链接：

Doctrine 官方网站和手册位于：

- `http://www.doctrine-project.org/`
- `http://www.doctrine-project.org/documentation/manual/1_1/en`

Doctrine 模型的介绍，位于：

- `http://www.doctrine-project.org/documentation/manual/1_1/en/introduction-to-models`

关于如何使用 Doctrine 模型表示数据库关系的信息，位于：

- `http://www.doctrine-project.org/documentation/manual/1_1/en/defining-models`

使用 Doctrine 的示例查询，位于：

- `http://www.doctrine-project.org/documentation/manual/1_0/en/working-with-models`

**问：** **为什么我需要在显示之前对输出进行转义？**

**答：** 一般原则，你不应该信任任何来自外部源的数据。这是因为攻击者总有可能向这些数据中嵌入恶意内容，如果你在不先进行清理的情况下使用它，可能会让你的应用程序用户面临风险。

这种攻击的一个常见示例是“跨站脚本（cross-site scripting）”，攻击者通过向你的页面注入恶意代码来获取敏感数据。考虑到这一点，在显示输出之前通过清理程序进行处理是至关重要的。

## 第 5 章：处理 CRUD 操作

### 技能与概念

- 理解并实现 CRUD 操作
- 学习处理输入的不同技术
- 创建多个布局模板，并在它们之间切换
- 构建简单的登录/注销系统
- 使用身份验证保护操作

你已经对 CRUD 这个缩写熟悉了。它代表了四种基本操作——创建（Create）、读取（Read）、更新（Update）和删除（Delete）。大多数使用持久数据的应用程序都会暴露一个接口，允许用户执行这些类型的操作。模型是应用程序数据的接口，因此如果不讨论如何使用它们为应用程序添加 CRUD 功能，那么对模型的讨论就是不完整的。本章将完全专注于（这里是个双关语！）应用程序开发的这一方面，演示如何在 SQUARE 示例应用环境中实现 CRUD 功能。它向你介绍了 `Zend_Auth` 组件，并展示了如何将身份验证附加到应用程序级别的操作。它还教了你更多关于模型、控制器、视图和布局的知识。所以，开始吧，让我们开始！

### 创建数据库记录

你已经知道如何使用 Zend Framework 创建和操作 Web 表单，上一章向你展示了将 Doctrine 模型集成到 Zend Framework 控制器是多么简单。现在让我们把这两点结合起来，构建一个允许卖家输入信息并将这些信息添加到数据库的 Web 表单。

#### 定义表单

第一步是定义将作为目录条目的输入表单。这里是表单定义，它应该保存到 `$APP_DIR/library/Square/Form/ItemCreate.php`：

```php
<?php

class Square_Form_ItemCreate extends Zend_Form
{
    public function init()
```



```php
// 初始化表单
$this->setAction('/catalog/item/create')
->setMethod('post');

// 为名称创建文本输入
$name = new Zend_Form_Element_Text('SellerName');
$name->setLabel('Name:')
->setOptions(array('size' => '35'))
->setRequired(true)
->addValidator('Regex', false, array(
    'pattern' => '/^[a-zA-Z]+[A-Za-z\'\-\. ]{1,50}$/'
))
->addFilter('HtmlEntities')
->addFilter('StringTrim');

// 为电子邮件地址创建文本输入
$email = new Zend_Form_Element_Text('SellerEmail');
$email->setLabel('Email address:');
$email->setOptions(array('size' => '50'))
->setRequired(true)
->addValidator('EmailAddress', false)
->addFilter('HtmlEntities')
->addFilter('StringTrim')
->addFilter('StringToLower');

// 为电话号码创建文本输入
$tel = new Zend_Form_Element_Text('SellerTel');
$tel->setLabel('Telephone number:');
$tel->setOptions(array('size' => '50'))
->addValidator('StringLength', false, array('min' => 8))
->addValidator('Regex', false, array(
    'pattern' => '/^\+[1-9][0-9]{6,30}$/',
    'messages' => array(
        Zend_Validate_Regex::INVALID => '\'%value%\' 不符合国际号码格式 +XXYYZZZZ',
        Zend_Validate_Regex::NOT_MATCH => '\'%value%\' 不符合国际号码格式 +XXYYZZZZ'
    )
))
->addFilter('HtmlEntities')
->addFilter('StringTrim');

// 为地址创建文本区域框
$address = new Zend_Form_Element_TextArea('SellerAddress');
$address->setLabel('Postal address:')
->setOptions(array('rows' => '6','cols' => '36'))
->addFilter('HtmlEntities')
->addFilter('StringTrim');

// 为物品标题创建文本输入
$title = new Zend_Form_Element_Text('Title');
$title->setLabel('Title:')
->setOptions(array('size' => '60'))
->setRequired(true)
->addFilter('HtmlEntities')
->addFilter('StringTrim');

// 为年份创建文本输入
$year = new Zend_Form_Element_Text('Year');
$year->setLabel('Year:')
->setOptions(array('size' => '8', 'length' => '4'))
->setRequired(true)
->addValidator('Between', false, array('min' => 1700, 'max' => 2015))
->addFilter('HtmlEntities')
->addFilter('StringTrim');

// 为国家创建选择框
$country = new Zend_Form_Element_Select('CountryID');
$country->setLabel('Country:')
->setRequired(true)
->addValidator('Int')
->addFilter('HtmlEntities')
->addFilter('StringTrim')
->addFilter('StringToUpper');
foreach ($this->getCountries() as $c) {
    $country->addMultiOption($c['CountryID'], $c['CountryName']);
}

// 为面值创建文本输入
$denomination = new Zend_Form_Element_Text('Denomination');
$denomination->setLabel('Denomination:')
->setOptions(array('size' => '8'))
->setRequired(true)
->addValidator('Float')
->addFilter('HtmlEntities')
->addFilter('StringTrim');

// 为类型创建单选框
$type = new Zend_Form_Element_Radio('TypeID');
$type->setLabel('Type:')
->setRequired(true)
->addValidator('Int')
->addFilter('HtmlEntities')
->addFilter('StringTrim');
foreach ($this->getTypes() as $t) {
    $type->addMultiOption($t['TypeID'], $t['TypeName']);
}
$type->setValue(1);

// 为等级创建选择框
$grade = new Zend_Form_Element_Select('GradeID');
$grade->setLabel('Grade:')
->setRequired(true)
->addValidator('Int')
->addFilter('HtmlEntities')
->addFilter('StringTrim');
foreach ($this->getGrades() as $g) {
    $grade->addMultiOption($g['GradeID'], $g['GradeName']);
}

// 为最低售价创建文本输入
$priceMin = new Zend_Form_Element_Text('SalePriceMin');
$priceMin->setLabel('Sale price (min):')
->setOptions(array('size' => '8'))
->setRequired(true)
->addValidator('Float')
->addFilter('HtmlEntities')
->addFilter('StringTrim');

// 为最高售价创建文本输入
$priceMax = new Zend_Form_Element_Text('SalePriceMax');
$priceMax->setLabel('Sale price (max):')
->setOptions(array('size' => '8'))
->setRequired(true)
->addValidator('Float')
->addFilter('HtmlEntities')
->addFilter('StringTrim');

// 为描述创建文本区域框
$notes = new Zend_Form_Element_TextArea('Description');
$notes->setLabel('Description:')
->setOptions(array('rows' => '6','cols' => '60'))
->setRequired(true)
->addFilter('HtmlEntities')
->addFilter('StripTags')
->addFilter('StringTrim');

// 为验证创建 CAPTCHA
$captcha = new Zend_Form_Element_Captcha('Captcha', array(
    'captcha' => 'Image',
    'wordLen' => 6,
    'timeout' => 300,
    'width' => 300,
    'height' => 100,
    'imgUrl' => '/captcha',
    'imgDir' => APPLICATION_PATH . '/../public/captcha',
    'font' => APPLICATION_PATH . '/../public/fonts/LiberationRegular.ttf',
));

// 创建提交按钮
$submit = new Zend_Form_Element_Submit('submit');
$submit->setLabel('Submit Entry')
->setOrder(100)
->setOptions(array('class' => 'submit'));

// 将元素附加到表单
$this->addElement($name);
$this->addElement($email);
$this->addElement($tel);
$this->addElement($address);

// 为卖家信息创建显示组
$this->addDisplayGroup(array('SellerName', 'SellerEmail', 'SellerTel', 'SellerAddress'), 'contact');
$this->getDisplayGroup('contact')
->setOrder(10)
->setLegend('Seller Information');

// 将元素附加到表单
$this->addElement($title);
$this->addElement($year);
$this->addElement($country);
$this->addElement($denomination);
$this->addElement($type);
$this->addElement($grade);
$this->addElement($priceMin);
$this->addElement($priceMax);
$this->addElement($notes);

// 为物品信息创建显示组
$this->addDisplayGroup(array('Title', 'Year', 'CountryID', 'Denomination', 'TypeID', 'GradeID', 'SalePriceMin', 'SalePriceMax', 'Description'), 'item');
$this->getDisplayGroup('item')
->setOrder(20)
->setLegend('Item Information');

// 将元素附加到表单
$this->addElement($captcha);

// 为 CAPTCHA 创建显示组
$this->addDisplayGroup(array('Captcha'), 'verification');
$this->getDisplayGroup('verification')
->setOrder(30)
->setLegend('Verification Code');
```

这部分内容你在第 3 章中已经熟悉了。表单包含了与之前创建的 `item` 数据库表紧密对应的输入字段。所有的字段都使用了 `HTMLEntities` 和 `StringTrim` 过滤器，许多字段还包含了验证器。特别要关注使用 `Regex` 验证器来验证名称和电话号码。在某些情况下还使用了自定义错误消息。

关于此表单定义最有趣的地方是使用 Doctrine 模型来填充选择列表。注意该类包含了三个辅助方法：`getCountries()`、`getGrades()` 和 `getTypes()`，它们内部调用第 4 章创建的 Doctrine 模型来获取选项。这些选项通过 `addMultiOption()` 方法附加到表单元素。

### 控制和视图

上一节定义的表单 URL 为 `/catalog/item/create`。根据 Zend Framework 的命名规范，这对应于“catalog”模块中的 `ItemController::createAction`。该控制器是在第 4 章创建的；现在需要更新新的操作。代码如下：

```php
<?php
class Catalog_ItemController extends Zend_Controller_Action
{
    public function createAction()
    {
        // 生成输入表单
        $form = new Square_Form_ItemCreate;
        $this->view->form = $form;

        // 测试输入
        // 如果有效，填充模型
        // 为某些字段分配默认值
        // 保存到数据库
        if ($this->getRequest()->isPost()) {
            if ($form->isValid($this->getRequest()->getPost())) {
                $item = new Square_Model_Item;
                $item->fromArray($form->getValues());
                $item->RecordDate = date('Y-m-d', mktime());
                $item->DisplayStatus = 0;
                $item->DisplayUntil = null;
                $item->save();
                $id = $item->RecordID;
                $this->_helper->getHelper('FlashMessenger')->addMessage(
                    '您的提交已被接受，物品编号 #' . $id . '。管理员将进行审核，如果通过，它将在 48 小时内出现在网站上。');
                $this->_redirect('/catalog/item/success');
            }
        }
    }

    public function successAction()
    {
    }
}
```

## 第 5 章：处理 CRUD 操作

137

```php
{
if ($this->_helper->getHelper('FlashMessenger')->getMessages()) {
    $this->view->messages = $this->_helper->getHelper('FlashMessenger')->getMessages();
} else {
    $this->_redirect('/');
}
}
```

假设表单输入有效，`createAction()` 方法会创建一个 `Item` 模型的实例，并使用通过 Web 表单提交的输入来填充它。对输入数据任何必要的自定义调整（例如，将记录的显示状态设置为隐藏）也会在此处进行，然后通过调用模型的 `save()` 方法将记录保存到数据库中，该方法会构建并执行必要的 `INSERT` 查询。此过程中的任何错误都将表示为 Doctrine 异常，并向前传递给默认异常处理器进行处理。

如果记录保存成功，则会将一个指示此事实的状态消息添加到 FlashMessenger 中，并将控制转移到 `successAction()` 方法，该方法将渲染一个成功视图。按照惯例，此视图脚本位于 `$APP_DIR/application/modules/catalog/views/scripts/item/success.phtml`。它的样子如下：

```html
<h2>Success</h2>
<?php echo implode($this->messages); ?>
```

**Q：为什么在在上一个示例中保存记录后，你重定向到 `successAction()`，而不是直接在 `createAction()` 中渲染成功视图？**

**A：** 这是在任何成功的 POST 操作后遵循的推荐方法，专门为了避免所谓的“重复提交问题”。考虑一下，在由 `createAction()` 渲染成功视图的情况下，如果应用程序用户在成功视图渲染后点击了浏览器的刷新/重载按钮，将导致相同的数据被两次 POST 到服务器。然而，通过在 FlashMessenger 动作辅助程序中存储成功消息并重定向到 `successAction()` 来渲染成功视图，这个问题被完全消除了；在这种情况下重新加载页面将再次生成成功视图（而不会引起重复提交），或者将客户端重定向回索引页。

提问专家

（续上）

138

Zend Framework：初学者指南



同样，输入表单的视图脚本位于`$APP_DIR/application/modules/catalog/views/scripts/item/create.phtml`，如下所示：

```html
<h2>Add Item</h2>
<?php echo $this->form; ?>
```

大功告成了！要查看操作效果，请访问 URL `http://square.localhost/catalog/item/create`，你应该会看到一个类似于图 5-1 中的所示表单。在表单中输入值并提交。如果你的输入通过了验证，将创建一个新记录并插入到`item`表中，然后渲染成功视图。图 5-2 展示了成功提交的结果。

你可以通过从第 4 章中的`ItemController::displayAction`访问 URL `http://square.localhost/catalog/item/display/xx`来验证该记录是否已成功插入，其中`xx`是新插入记录的 ID。如果你的输入无效，表单将重新渲染并带有错误消息，指明哪里出了问题，如图 5-3 所示。

图 5-1

向 SQUARE 目录添加新条目的表单

139

图 5-2

向 SQUARE 目录成功添加新项目的结果

图 5-3

使用无效输入值提交表单的结果

140

Zend Framework：初学者指南

## 处理管理操作

此时，SQUARE 示例应用程序的一个关键目标——允许卖家直接上传可用邮票的列表——已经实现。然而，这些项目不会立即在公共领域可见，因为应用程序管理员必须手动审核上传的条目，要么批准其显示，要么将其从数据库中删除。这就是 SQUARE 管理面板用用场。

SQUARE 管理面板是应用程序中专门为应用程序管理员保留的部分。它为管理员提供了一个查看、更新和删除目录条目的接口，因此它是说明如何实现剩余 CRUD 操作的完美场所。但在深入研究代码之前，了解在 Zend Framework 应用程序上下文中处理管理操作的不同方法是一个好主意。这里有三个方面需要考虑：结构、路由和布局。

### 结构

在模块化应用程序中，管理操作有多种结构化方式：

- **在默认模块中创建一个单个控制器**，它持有应用程序的所有管理操作。在这种方法下，单个控制器将包含应用程序所有模块的管理操作（见图 5-4）。除了非常小的应用程序外，否则不建议这种方法，因为单个控制器可能会迅速增长到非常大，从而影响性能和可维护性。

- **创建一个独立的模块来持有应用程序的所有管理操作**。在这种方法下，新模块将包含应用程序管理操作的各个控制器，每个模块一个这样的控制器（见图 5-5）。这是一个常用方法，但它也不非常易维护，因为如图 5-5 所示，你最终将得到必须管理多个控制器信息的单个控制器。在构建自包含模块时，这也不理想，因为与每个模块相关的操作并不都存储在同一个文件系统位置。（img/222e7e58871b08cc6397852e1452b57_158_0.png）图 5-4 单一控制器中的管理操作（img/222e7e58871b08cc6397852e1452b57_158_1.png）图 5-5 独立模块中的控制器

- **在每个模块内创建一个独立的控制器**来持有该模块的管理操作。在这种方法下，每个模块至少包含两个控制器：一个公共操作，另一个用于相应的管理操作（见图 5-6）。出于多种原因推荐这种方法：从逻辑和物理角度来看都是合理的，因为特定模块的所有操作位于同一个文件系统位置；它易于维护；并且足够灵活以适应不同的目的。

### 路由

为了确保一致性，管理路由模仿其公共路由通常是一个好意。例如，如果指向操作的公共路由是`/article/5`，那么对应的管理路由可能是`/admin/article/5`。使用`/admin`前缀用于标记路由具有管理性质，同时为应用程序的功能提供清晰且一致的接口。这种一致性在你以后暴露 REST 或 SOAP 功能时特别重要。

与其他框架不同，Zend Framework 没有内置管理路由。因此，必须手动配置这些路由，要么通过应用程序配置文件指定它们，要么通过扩展基础路由器使其“感知前缀”。前者的示例如下代码所示；后者的示例见本章末：

```php
resources.router.routes.list.route = /admin/articles/index
resources.router.routes.list.defaults.module = system
resources.router.routes.list.defaults.controller = articles
resources.router.routes.list.defaults.action = list

resources.router.routes.view.route = /admin/articles/view/:id
resources.router.routes.view.defaults.module = system
resources.router.routes.view.defaults.controller = articles
resources.router.routes.view.defaults.action = display

resources.router.routes.update.route = /admin/articles/edit/:id
resources.router.routes.update.defaults.module = system
resources.router.routes.update.defaults.controller = articles
resources.router.routes.update.defaults.action = update
```

141

图 5-6

每个模块内的管理控制器（img/222e7e58871b08cc6397852e1452b57_159_0.png）

142

Zend Framework：入门指南

```php
resources.router.routes.delete.route = /admin/articles/delete/:id
resources.router.routes.delete.defaults.module = system
resources.router.routes.delete.defaults.controller = articles
resources.router.routes.delete.defaults.action = delete
```

## 布局 (Layout)

默认情况下，所有视图将使用应用配置文件定义的主布局（master layout）。

然而，客户通常希望为应用程序的管理视图提供不同的视觉效果，出于美学考虑，或者是为了在视觉上提醒用户他们已移动到应用程序的不同部分。

在 Zend Framework 应用中实现这一点并不困难：只需为管理视图创建一个新的布局，然后在各个动作（action）中根据需要切换到它即可。

这是一个示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function adminDeleteAction()
    {
        $this->_helper->layout->setLayout('admin');
        // 继续
    }
}
```

在处理大量动作时，这可能会非常繁琐（更不用说可能成为维护的噩梦）。因此，另一种方法是在控制器的`init()`或`preDispatch()`方法中检查请求 URL，并在渲染视图之前自动切换布局。这种方法将在下一节中详细讨论。

## 列出、删除和更新数据库记录

考虑到所有这些背景信息，让我们开始构建 SQUARE 管理面板。如前文所述，为了保持简单，我们假设管理员只需要查看、编辑和删除目录中的条目。接下来的章节将详细讨论这些功能中的每一项。

### 设置管理布局

第一步是为管理视图定义一个新的主布局。由于该布局的主要目的仅仅是将管理界面与公共界面区分开来，因此不需要特别复杂。以下是它可能性的示例：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
    <base href="/" />
    <link rel="stylesheet" type="text/css" href="/css/master.css" />
    <link rel="stylesheet" type="text/css" href="/css/admin.css" />
    <script src="/js/form.js"></script>
</head>
<body>
    <div id="header">
        <div id="logo">
            <img src="/images/logo-admin.gif" />
        </div>
        <div id="menu">
            <a href="<?php echo $this->url(array(), 'admin-catalog-index'); ?>">目录 (CATALOG)</a>
        </div>
    </div>
    <div id="content">
        <?php echo $this->layout()->content ?>
    </div>
    <div id="footer">
        <p>使用 <a href="http://framework.zend.com/">Zend Framework</a>a 创建。根据 <a href="http://www.creativecommons.org/">Creative Commons</a>a 许可授权。</p>
    </div>
</body>
</html>
```

正如你在第 2 章中做过的那样，将此布局模板保存到应用的布局目录中，路径为`$APP_DIR/application/layouts/admin.phtml`。

你会注意到该布局还使用了三个额外的资源——一个 CSS 样式表、一个 JavaScript 代码文件和一个标志图像。这些文件需要位于应用程序的公共区域，以便连接客户端可以通过 HTTP 获取它们。你可以在本章的代码存档中找到这些资源，该存档可以从本书的伴随辅助网站 `http://www.zf-beginners-guide.com/`下载。

下一步是设置相关内容，使得每当路由器遇到带有`/admin`前缀的 URL 时，框架会自动将默认布局切换到新的管理布局。正如之前讨论的，实现此点的方法是在是在路由定义中指定新布局的名称。然而，更简单的选项是在控制器的`preDispatch()`方法中执行此切换，该方法在每个动作被调用之前会被自动触发。

*（续）*

执行此操作的代码应添加到`$APP_DIR/application/modules/catalog/controllers/AdminItemController.php`的`Catalog_AdminItemController`中，如下所示：

```php
<?php

class Catalog_AdminItemController extends Zend_Controller_Action
{
    // 处理管理 URL 的动作
    public function preDispatch()
    {
        // 检查 URL 的 /admin 模式
        // 设置管理布局
        $url = $this->getRequest()->getRequestUri();
        $this->_helper->layout->setLayout('admin');
    }
}
```

这段代码检查当前请求并使用`setLayout()`方法切换到管理布局模板。

### 定义自定义路由 (Custom Routes)

下一步是为管理功能定义自定义路由。此时有必要对这些路由的形式进行一些假设，所以让我们假设：

1. 摘要列表 URL 将具有`/admin/catalog/index`的形式。

2. 所有显示 URL 将具有`/admin/catalog/display/:id`的形式。

**问：什么是`preDispatch()`方法？**

**答：`preDispatch()`方法是一个特殊的“存根”方法，在指定的动作之前由控制器执行。它对于在传递请求之前进行预处理、日志记录或操作非常有用。**

3. 更新 URL 将具有`/admin/catalog/update/:id`的形式。

4. 删除 URL 将具有`/admin/catalog/delete/:id`的形式。

为了设置自定义路由，请在`$APP_DIR/application/configs/application.ini`中添加以下路由定义：

```ini
resources.router.routes.admin-catalog-index.route = /admin/catalog
resources.router.routes.admin-catalog-index.defaults.module = catalog
resources.router.routes.admin-catalog-index.defaults.controller = admin
resources.router.routes.admin-catalog-index.defaults.action = index

resources.router.routes.admin-catalog-display.route = /admin/catalog/display/:id
resources.router.routes.admin-catalog-display.defaults.module = catalog
resources.router.routes.admin-catalog-display.defaults.controller = admin
resources.router.routes.admin-catalog-display.defaults.action = display

resources.router.routes.admin-catalog-update.route = /admin/catalog/update/:id
resources.router.routes.admin-catalog-update.defaults.module = catalog
resources.router.routes.admin-catalog-update.defaults.controller = admin
resources.router.routes.admin-catalog-update.defaults.action = update

resources.router.routes.admin-catalog-delete.route = /admin/catalog/delete/:id
resources.router.routes.admin-catalog-delete.defaults.module = catalog
resources.router.routes.admin-catalog-delete.defaults.controller = admin
resources.router.routes.admin-catalog-delete.defaults.action = delete

resources.router.routes.admin-catalog-success.route = /admin/catalog/success
resources.router.routes.admin-catalog-success.defaults.module = catalog
resources.router.routes.admin-catalog-success.defaults.controller = admin
resources.router.routes.admin-catalog-success.defaults.action = success
```

### 定义列表动作和视图

在所有这些工作都准备就绪后，我们现在可以开始编写动作代码了。考虑`Catalog_AdminItemController::indexAction`，它使用 Doctrine 模型从数据库获取记录列表并将其附加到视图：



# 第5章：处理 CRUD 操作

## 目录列表显示

`Catalog_AdminItemController` 类的 `indexAction()` 方法负责显示目录列表。该方法使用 Doctrine 查询构建器创建查询，从 `Square_Model_Item` 表及其关联的 `Square_Model_Grade`、`Square_Model_Country` 和 `Square_Model_Type` 表中获取数据，并将结果传递给视图。

```php
<?php

class Catalog_AdminItemController extends Zend_Controller_Action
{
    // 显示目录列表的动作
    public function indexAction()
    {
        $q = Doctrine_Query::create()
            ->from('Square_Model_Item i')
            ->leftJoin('i.Square_Model_Grade g')
            ->leftJoin('i.Square_Model_Country c')
            ->leftJoin('i.Square_Model_Type t');
        $result = $q->fetchArray();
        $this->view->records = $result;
    }
}
```

然后视图接管并将将其格式化为表格以提高可读性。以下是视图脚本的内容（根据约定，这应该保存为 `$APP_DIR/application/modules/catalog/views/scripts/admin-item/index.php`）：

```html
<h2>条目列表 (List Items)</h2>

<?php if (count($this->records)): ?>
<div id="records">
<form method="post" action="<?php echo $this->url(array(), 'admin-catalog-delete'); ?>">
<table>
    <tr>
        <td></td>
        <td class="key">条目 ID</td>
        <td class="key">标题</td>
        <td class="key">面值</td>
        <td class="key">国家</td>
        <td class="key">等级</td>
    </tr>
```

```php
<?php foreach ($this->records as $r):?>
<tr>
<td><input type="checkbox" name="ids[]" value="<?php echo $r['RecordID']; ?>" style="width:2px" /></td>
<td><?php echo $this->escape($r['RecordID']); ?></td>
<td><?php echo $this->escape($r['Title']); ?></td>
<td><?php echo $this->escape(sprintf('%1.2f', $r['Denomination'])); ?></td>
<td><?php echo $this->escape($r['Square_Model_Country']['CountryName']); ?></td>
<td><?php echo $this->escape($r['Square_Model_Grade']['GradeName']); ?></td>
<td><?php echo $this->escape($r['Year']); ?></td>
<td><a href="<?php echo $this->url(array('id' => $r['RecordID']), 'admin-catalog-display'); ?>">显示</a></td>
<td><a href="<?php echo $this->url(array('id' => $r['RecordID']), 'admin-catalog-update'); ?>">更新</a></td>
</tr>
<?php endforeach; ?>
<tr>
<td colspan="10"><input type="submit" name="submit" style="width:150px" value="删除选中项目" /></td>
</tr>
</table>
</form>
</div>
<?php else: ?>
未找到记录
<?php endif; ?>
```

关于此视图有以下几点需要注意：

- 所有字段值在渲染之前都经过了转义。正如第 4 章所过的，这是你在处理输出值时应该采取的一项基本安全措施，以减少 CSRF 和 XSS 攻击的风险。
- 显示 `<table>` 被封装在 `<form>` 内部。这是处理每条记录旁边的复选框所必要的，以便实现多记录删除。注意，此表单是在视图脚本内部手动生成的，而不是使用 `Zend_Form`，因为在 `Zend_Form` 中没有简单的方法创建这种“表单+表格”的组合。
- 每条记录都带有“更新”和“显示”链接。这些链接对应于上一节中配置的路由，并在运行时使用 `url()` 视图助手动态生成。注意，记录 ID 作为 GET 参数包含在请求 URL 中。

要查看此视图的运行情况，请启动浏览器并将其指向 `http://square.localhost/admin/catalog/item/index`。你将看到一个类似于图 5-7 所示的摘要页面。

## 定义删除操作

当用户选择一个或多个记录进行删除时，选中的记录 ID 将以数组的形式 POST 到 `Catalog_AdminItemController::deleteAction`。该 `deleteAction()` 方法读取选中的 ID，并使用 Doctrine 模型构建一个 DELETE 查询，将它们从数据库中删除。其代码如下所示：

```php
<?php

class Catalog_AdminItemController extends Zend_Controller_Action
{
    // 删除目录项的操作
    public function deleteAction()
    {
        // 为 POST 输入设置过滤器和验证器
        $filters = array(
            'ids' => array('HtmlEntities', 'StripTags', 'StringTrim')
        );

        $validators = array(
            'ids' => array('NotEmpty', 'Int')
        );

        $input = new Zend_Filter_Input($filters, $validators);
        $input->setData($this->getRequest()->getParams());

        // 测试输入是否有效
        // 读取记录标识符数组
        // 从数据库中删除记录
        if ($input->isValid()) {
            $q = Doctrine_Query::create()
                ->delete('Square_Model_Item i')
                ->whereIn('i.RecordID', $input->ids);
            $result = $q->execute();
            $this->_helper->getHelper('FlashMessenger')
                ->addMessage('记录已成功删除.');
            $this->_redirect('/admin/catalog/item/success');
        } else {
            throw new Zend_Controller_Action_Exception('无效输入');
        }
    }

    // 成功操作
    public function successAction()
    {
        if ($this->_helper->getHelper('FlashMessenger')->getMessages()) {
            $this->view->messages = $this->_helper
                ->getHelper('FlashMessenger')->getMessages();
        } else {
            $this->_redirect('/admin/catalog/item/index');
        }
    }
}
```

要查看此效果，请通过勾选摘要页面相应的复选框选择一个或多个记录进行删除，然后使用“删除选中”按钮提交表单。记录应从数据库中删除，你将看到一个成功消息，如图 5-8 所示。

## 定义更新表单

管理员拥有更新比非特权用户更多记录字段的能力，这也是非常常见的。例如，在 SQUARE 应用中，除了常规字段外，管理员还应该能够更新状态。使用 `Zend_Form`，可以扩展父类并派生子类。为了说明，请考虑以下：

```php
<?php

class Square_Form_ItemUpdate extends Zend_Form
{
    public function init()
    {
        // 初始化父类
        parent::init();

        // 设置动作
        $this->setAction('/admin/item/update');

        // 移除不需要的元素
        $this->removeElement('Captcha');

        // 为 ID 创建隐藏输入
        $id = new Zend_Form_Hidden('RecordID');
        $id->addValidator('Int')
           ->addFilter('HtmlEntities')
           ->addFilter('StringTrim');

        // 为状态创建选择框
        $display = new Zend_Form_Select('DisplayStatus');
        $display->addValidator('Int')
                ->addFilter('HtmlEntities')
                ->addFilter('StringTrim')
                ->addOptions(array(
                    0 => 'Hidden',
                    1 => 'Visible'
                ));

        // 为日期创建隐藏输入
        $displayUntil = new Zend_Form_Hidden('DisplayUntil');
        $displayUntil->addValidator('Date')
                     ->addFilter('HtmlEntities')
                     ->addFilter('StringTrim');

        // 为日期创建选择框
        $displayUntilDay = new Zend_Form_Select('DisplayUntil_day');
        $displayUntilDay->addValidator('Int')
                          ->addFilter('HtmlEntities')
                          ->addFilter('StringTrim')
                          ->addFilter('ToUpper')
                          ->setDecorators(array(
                              array('ViewHelper'),
                              array('HtmlTag', array(
                                  'tag' => 'div',
                                  'openOnly' => true,
                                  'id' => 'divUntil',
                                  'placement' => 'prepend'
                              ))
                          ));

        for ($x=1; $x<=31; $x++) {
            $displayUntilDay->addOption($x, sprintf('%02', $x));
        }

        $displayUntilMonth = new Zend_Form_Select('DisplayUntil_month');
        $displayUntilMonth->addValidator('Int')
                          ->addFilter('HtmlEntities')
                          ->addFilter('StringTrim')
                          ->setDecorators(array(
                              array('ViewHelper')
                          ));

        for ($x=1; $x<=12; $x++) {
            $displayUntilMonth->addOption($x, date('M', mktime(1,1,1,$x,1,1)));
        }

        $displayUntilYear = new Zend_Form_Select('DisplayUntil_year');
        $displayUntilYear->addValidator('Int')
                          ->addFilter('HtmlEntities')
                          ->addFilter('StringTrim')
                          ->setDecorators(array(
                              array('ViewHelper'),
                              array('HtmlTag', array(
                                  'tag' => 'div',
                                  'closeOnly' => true
                             ))
                          ));

        for ($x=2009; $x<=2012; $x++) {
            $displayUntilYear->addOption($x, $x);
        }

        // 将元素附加到表单
        $this->addElement($id)
             ->addElement($display)
             ->addElement($displayUntil)
             ->addElement($displayUntilDay)
             ->addElement($displayUntilMonth)
             ->addElement($displayUntilYear);

        // 为状态创建显示组
        $this->addDisplayGroup(array('DisplayStatus', 'DisplayUntil_day',
                               'DisplayUntil_month', 'DisplayUntil_year',
                               'DisplayUntil'), 'display');

        $this->getDisplayGroup('display')
             ->setOrder(25)
             ->setLegend('Display Information');
    }
}
```



将此表单定义保存为`$APP_DIR/library/Square/Form/ItemUpdate.php`。

## 第 5 章：处理 CRUD 操作

### 处理日期输入

这里介绍一下表单中的日期输入字段。正如你可能在第 3 章中记得的，`Zend_Form`包含一个`Date`验证器（validator），它可以用于检查日期是否有效。如果你查看之前的表单定义，会发现它包含了三个用于日期输入的选择列表，分别对应日、月、年。还有一个隐藏输入字段，它在内部用于存储由这三个选择列表创建的复合日期值，并与上述的`Date`验证器关联。

你可能认为这看起来似乎没必要那么复杂，你是正确的。为什么呢？嗯，在默认设置下，`Date`验证器期望日期输入的格式为`YYYY-MM-DD`格式的单个字符串，并且如果不符合此格式，它将产生验证错误。但在现实世界中，用户在手动输入字符串日期值时经常会出错。常见错误包括选择不同的格式（例如`DD-MM-YYYY`）、忘记为单数字的日期和月份值补零（例如，输入`9`而不是`09`），或使用不同的分隔符（例如`YYYY/MM/DD`）。

考虑到这些，通常认为提供选择列表或图形化日历界面来进行日期输入更安全且对用户更友好，因为这样不容易受到用户的特殊习惯影响，然后通过程序将输入重写为所需的格式。正如你将在下一节中看到的，这正是`updateAction()`所完成的。它使用来自三个选择列表的输入创建一个`YYYY-MM-DD`格式的复合日期值，将隐藏输入字段设置为该值，然后允许按正常方式进行验证。

由于隐藏输入字段与`Date`验证器关联，无效的日期将无法通过验证，`Date`验证器将生成错误消息，该消息将在表单重新渲染时可见。如果日期有效，输入将通过验证，操作代码的剩余部分将按正常执行。

**提示**

处理日期输入字段还有其他方法。其中一种由领先的 Zend Framework 首席开发者 Matthew Weier O’Phinney 建议的方法，涉及扩展`Zend_Form_Element`基类来创建一个复合日期输入元素（你会在本章末尾找到该方法的链接）。另一种技术在第 11 章中详细讨论过，涉及使用图形化日历组件结合文本输入字段，直接将选定的日期以所需的格式写入表单。

你会注意到此表单定义还使用了`HtmlTag`装饰器。正如第 3 章所解释的样，该装饰器控制表单字段周围的标记。在特定情况下，它通过选择性使用装饰器的`'openOnly'`和`'closeOnly'`属性，在三个日期选择列表周围封装了一个`<div>`元素。这个`<div>`由用户定义的`handleInputDisplayOnSelect()` JavaScript 函数使用，它根据项目的显示状态自动隐藏或显示日期选择器组。

### 定义更新操作和视图

更新记录通常涉及两个不同的查询：

1. 第一个查询是读查询，发生在用户选择某条记录进行更新时。`updateAction()`必须从数据库中读取选定的记录，用当前存储在数据库中的字段值预填充 Web 表单，并将此表单渲染给用户。
2. 第二个查询是写查询，发生在用户提交表单时。`updateAction()`必须接收、过滤并验证提交的值。如果值有效，操作必须将记录的新版本写入数据库。

`Catalog_AdminItemController::updateAction`执行了这两个功能。它的样子如下：

```php
<?php

class Catalog_AdminItemController extends Zend_Controller_Action

{

    // 修改单个目录项目的操作

    public function updateAction()

    {

        // 生成输入表单

        $form = new Square_Form_ItemUpdate;

        $this->view->form = $form;

        if ($this->getRequest()->isPost()) {

            // 如果是 POST 请求

            // 测试输入是否有效

            // 获取当前记录

            // 更新值并替换到数据库

            $postData = $this->getRequest()->getPost();

            $postData['DisplayUntil'] = sprintf('%04d-%02d-%02d',

                $this->getRequest()->getPost('DisplayUntil_year'),

                $this->getRequest()->getPost('DisplayUntil_month'),

                $this->getRequest()->getPost('DisplayUntil_day')

            );

            if ($form->isValid($postData)) {

                $input = $form->getValues();

                $item = Doctrine::getTable('Square_Model_Item')

                    ->find($input['RecordID']);

                $item->fromArray($input);

                $item->DisplayUntil =

                    ($item->DisplayStatus == 0) ? null : $item->DisplayUntil;

                $item->save();

                $this->_helper->getHelper('FlashMessenger')

                    ->addMessage('The record was successfully updated.');

                $this->_redirect('/admin/catalog/item/success');

            }

        } else {

            // 如果是 GET 请求

            // 为 GET 输入设置过滤器和验证器

            // 测试输入是否有效

            // 获取请求的记录

            // 预填充表单

            $filters = array(

                'id' => array('HtmlEntities', 'StripTags', 'StringTrim')

            );

            $validators = array(

                'id' => array('NotEmpty', 'Int')

            );

            $input = new Zend_Filter($filters, $validators);

            $input->setData($this->getRequest()->getParams());

            if ($input->isValid()) {

                $q = Doctrine_Query::create()

                    ->from('Square_Model_Item', 'i')

                    ->leftJoin('Country', 'c', 'i.CountryID = c.ID')

                    ->where('i.RecordID = ?', $input->getValue('id'));

                $result = $q->fetchArray();

                if (count($result) == 1) {

                    // 对日期进行调整

                    $date = $result[0]['DisplayUntil'];

                    $result[0]['DisplayUntil_day'] = date('d', strtotime($date));

                    $result[0]['DisplayUntil_month'] = date('m', strtotime($date));

                    $result[0]['DisplayUntil_year'] = date('Y', strtotime($date));

                    $this->view->form->populate($result[0]);

                } else {

                    throw new Zend_Controller_Action_Exception('Page not found', 404);

                }

            } else {

                throw new Zend_Controller_Action_Exception('Invalid input');

            }

        }

    }

}
```

大致来说，这个`updateAction()`方法由条件测试分为两个部分：

1. 如果是 POST 请求，操作获取 POST 输入并执行必要的调整以创建`YYYY-MM-DD`格式的复合日期字符串，如前节所述。然后它使用`Zend_Form`对象的`isValid()`方法测试输入是否有效。假设输入有效，操作使用 Doctrine 的`find`方法检索记录实例，并使用提交的值设置记录字段的新值。使用`save()`方法将记录保存回数据库，并将控制传递到`successAction()`。
2. 如果是 GET 请求，操作从 URL 请求字符串获取记录 ID，对其进行验证，并执行 Doctrine 查询从数据库检索相应的记录。它对日期输入值进行反向调整，然后使用`Zend_Form`对象的`populate()`方法用记录当前的字段值预填充输入表单。

这是对应的视图脚本，应保存为`$APP_DIR/application/modules/catalog/views/scripts/admin-item/update.php`：

```html
<h2>更新项目</h2>

<?php echo $this->form; ?>

<script>

handleInputDisplayOnSelect('DisplayStatus', 'divDisplayUntil', new Array('1'));

</script>
```

要查看运行效果，请在摘要页上使用“Update”链接选择某条记录进行更新，或者使用浏览器访问更新 URL，例如`http://square.localhost/admin/catalog/item/update/1`。你应该会看到一个已经填充了记录当前内容的表单，如图 5-9 所示。

图 5-9

在 SQUARE 管理面板中更新现有项目的表单

## 第 5 章：处理 CRUD 操作

注意，此表单包含了额外的字段，允许你控制条目的显示状态（见图 5-10）。如果状态被设置为“可见”（visible），你还可以定义该项目继续保持可见的日期。

进行你的更改并提交表单。假设你的输入通过了验证，记录将会被更新，并向你显示一条成功消息。记住，你也可以通过浏览相应的显示 URL 来验证更新，例如`http://square.localhost/catalog/item/display/1`。

### 更新显示操作

还有最后一项更改需要完成。在第 4 章中，你创建了一个`displayAction()`，它可以接收一个项目 ID 并使用 Doctrine 查询从数据库中检索相应的记录。然而，该查询并没有考虑项目当前的显示状态。由于现在已经存在一种让管理员调整项目可见性状态的机制，因此更新此`displayAction()`以使其也考虑该状态，并只显示那些设置为“公开可见”的项目。

要做到这一点，请更新位于`$APP_DIR/application/modules/catalog/controllers/ItemController.php`的`ItemController::displayAction`，使其在 Doctrine 查询中包含可见性调整条件：

```php
<?php

class Catalog_ItemController extends Zend_Controller_Action

{

    // 显示目录条目的的 action

    public function displayAction()

    {

        // 为 GET 输入设置过滤器和验证器

        // ...

        // 测试输入是否有效

        // 获取请求的记录

        // 绑定到视图
```

图 5-10：SQUARE 更新表单中定义项目可见性的额外选项
![](img/222e7e58871b088cc6397852e1452b57_175_0.png)

（续上）

Zend Framework：初学者指南

```php
        if ($input->isValid()) {

            $q = Doctrine_Query::create()

                ->from('Square_Model_Item i')

                ->leftJoin('i.Square_Model_Country c')

                ->leftJoin('i.Square_Model_Grade g')

                ->leftJoin('i.Square_Model_Type t')

                ->where('i.RecordID = ?', $input->id)

                ->addWhere('i.DisplayStatus = 1')

                ->addWhere('i.DisplayUntilDate >= CURDATE()');

            $result = $q->fetchArray();

            if (count($result) == 1) {

                $this->view->item = $result[0];

            } else {

                throw new Zend_Controller_Action_Exception('Page not found', 404);

            }

        } else {

            throw new Zend_Controller_Action_Exception('Invalid input');

        }

    }

}
```

通过此更改，只有被专门标记为可见的项目才能通过公共接口访问。任何访问这些项目之外项目的尝试都将抛出 404 异常，该异常将传递给默认异常处理器，以便显示给请求客户端。

**注意**

你是否在想为什么这一章没有包含任何关于读取单条记录（CRUD 中的 R）的内容？这部分已经在第 4 章的“检索记录”（Retrieving Records）章节中涵盖过了，该章节使用 Doctrine 模型通过 ID 显示数据库记录。本章讨论的管理面板包含类似的功能，你可以在`http://www.zf-beginners-guide.com/`的代码存档中找到它。

### 添加用户身份验证

此时，管理面板已经完成，管理员可以通过基于浏览器的界面对记录执行读取、更新和删除操作。然而，这些操作目前没有受到保护，结果是任何用户都可以通过其 URL 访问它们。这显然是一个安全风险，因此下一步是实现一种区分“无特权用户”和“管理员”的机制，并仅允许后者访问管理功能。

Zend Framework 包含一个专门用于处理身份验证任务的组件。该组件称为`Zend_Auth`，它提供了 API 和一组适配器，用于验证各种来源的凭据，包括 SQL 标准数据库系统、文本文件、LDAP 目录和 OpenID 提供程序。通过验证的身份由`Zend_Auth`自动存储在会话中，因此可以由控制器或 action 随时对其进行检索或重新验证。

**注意**

默认情况下，`Zend_Auth`仅支持基于会话存储。但是，你只需通过扩展`Zend_Auth_Storage_Interface`即可对其他存储机制的支持。更多信息以及如何操作的示例可以在本章末尾找到。

为了理解这在实践中是如何工作的，请考虑以下示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action

{

    public function authenticateAction()

    {

        // 生成登录表单
```



### 创建登录/退出系统

`Zend_Auth` 是一个很难解释但通过示例更易于理解的组件。考虑到这一点，让我们在实际语境中使用它，通过构建一个简单的登录/退出系统来保护 SQUARE 管理面板的访问。后续章节将指导你完成此过程。

#### 定义路由

一如既往，良好的起点是路由定义。通过向你的应用程序配置文件 `*$APP_DIR*/application/configs/application.ini*` 为你的管理面板定义登录和退出路由：

```ini
resources.router.routes.login.route = /admin/login
resources.router.routes.login.defaults.module = default
resources.router.routes.login.defaults.controller = login
resources.router.routes.login.defaults.action = login
resources.router.routes.login-success.route = /admin/login/success
resources.router.routes.login-success.defaults.module = default
resources.router.routes.login-success.defaults.controller = login
resources.router.routes.login-success.defaults.action = success
resources.router.routes.logout.route = /admin/logout
resources.router.routes.logout.defaults.module = default
resources.router.routes.logout.defaults.controller = login
resources.router.routes.logout.defaults.action = logout
```

#### 定义登录表单

下一步是定义登录表单本身。这不需要非常复杂——你只需要一个用户名字段、一个密码字段和一个提交按钮。以下是表单定义，它应该被保存为 `*$APP_DIR*/library/Square/Form/Login.php*`：

```php
<?php
class Square_Form_Login extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/admin/login')
            ->setMethod('post');

        // 创建用户名的文本输入
        $username = new Zend_Form_Element_Text('username');
        $username->setLabel('Username:')
            ->setOptions(array('size' => '30'))
            ->setRequired(true)
            ->addValidator('Alnum')
            ->addFilter('HtmlEntities')
            ->addFilter('StringTrim');

        // 创建密码文本框
        $password = new Zend_Form_Element_Password('password');
        $password->setLabel('密码:')
            ->setOptions(array('size' => '30'))
            ->setRequired(true)
            ->addFilter('HtmlEntities')
            ->addFilter('StringTrim');

        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit');
        $submit->setLabel('登录')
            ->setOptions(array('class' => 'submit'));

        // 将元素附加到表单
        $this->addElement($username)
            ->addElement($password)
            ->addElement($submit);
    }
}
```

### 定义身份验证适配器

上一节中的表单将其数据提交到“default”模块中的 `LoginController::loginAction`。在深入研究该操作的代码之前，我们需要花几分钟创建一个身份验证适配器，该适配器知道如何根据第 4 章中创建的用户表来验证提供的用户名和密码。

正如之前讨论的，使用 `Zend_Auth` 创建自定义身份验证适配器并不困难。只需扩展基类 `Zend_Auth_Adapter_Interface`，并确保子类暴露一个知道如何执行所需身份验证的 `authenticate()` 方法即可。更重要的问题是，既然 `Zend_Auth` 已经包含了一个用于数据库身份验证的内置适配器，为什么还需要创建自定义适配器呢？

原因完全在于效率和一致性。首先，`Zend_Auth_Adapter_DbTable` 适配器仅适用于 `Zend_Db` 类的实例，它不能直接与 Doctrine 模型配合。反之，`Zend_Db` 期望的数据库连接参数格式与 Doctrine 使用的格式不同。因此，为了直接使用 `Zend_Auth_Adapter_DbTable`，需要在应用程序配置文件以两种不同的格式指定相同的数据库连接参数（这并不理想，因为每当你（例如）更改数据库密码时就需要更新两套参数），或者编写代码将 Doctrine DSN 字符串“翻译”为 `Zend_Db` 预期的数组格式（由于可能的 DSN 排列非常多，这既繁琐又容易出错）。

此外还有一致性的小问题。到目前为止，所有的数据库访问都是通过 Doctrine 模型进行的。仅为了身份验证相关的查询切换到 `Zend_Db` 是令人困惑的；而且效率低下，因为应用程序现在需要加载两套库来执行数据库操作。由于这些原因，创建一个内部使用 Doctrine 的自定义身份验证适配器是有意义的，而不是使用提供的 `Zend_Auth_Adapter_DbTable` 适配器。

解释完这些，让我们进入实际代码。考虑下面的列表，它创建了一个符合 `Zend_Auth` 的 Doctrine 身份验证适配器：

```php
<?php
class Square_Auth_Adapter_Doctrine implements Zend_Auth_Adapter_Interface
{
    // 包含通过验证的用户记录数组
    protected $_resultArray;

    // 构造函数
    // 接受用户名和密码
    public function __construct($username, $password)
    {
        $this->username = $username;
        $this->password = $password;
    }

    // 主身份验证方法
    // 查询数据库以匹配身份凭据
    // 返回带有成功/失败代码的 Zend_Auth_Result
    public function authenticate()
    {
        $q = Doctrine_Query::create()
            ->from('Square_Model_User u')
            ->where('u.Username = ? AND u.Password = PASSWORD(?)',
            array($this->username, $this->password)
            );

        $result = $q->fetchArray();

        if (count($result) == 1) {
            return new Zend_Auth_Result(
                Zend_Auth_Result::SUCCESS, $this->username, array());
        } else {
            return new Zend_Auth_Result(
                Zend_Auth_Result::FAILURE, null,
                array('身份验证失败')
            );
        }
    }

    // 返回通过验证的用户记录数组
    // 根据需要排除用户字段
    public function getResultArray($excludeFields = null)
    {
        if (!$this->_resultArray) {
            return false;
        }
        if ($excludeFields != null) {
            $excludeFields = (array)$excludeFields;
            foreach ($this->_resultArray as $key => $value) {
                if (!in_array($key, $excludeFields)) {
                    $returnArray[$key] = $value;
                }
            }
            return $returnArray;
        } else {
            return $this->_resultArray;
        }
    }
}
```

将此类保存为 `*$APP_DIR/library/Square/Auth/Adapter/Doctrine.php*`。

**提示**

除了简单的成功和失败指示外，还有许多其他结果代码。这些代码可以提供身份验证失败的具体信息——例如与用户名或密码、发现的用户记录存在歧义，或者发生了其他类型的错误。完整的结果代码列表可以在 Zend Framework 手册找到。

`authenticate()` 方法仅返回用户是否通过身份验证，而 `getResultArray()` 方法以数组形式返回完整的用户记录。该方法可选地接受一个字段列表并从返回的数组中删除这些字段。这是适配器中一个方便的方法，因为它允许一次性访问整个用户记录，并方便在会话持久化用户记录供其他 action 使用。

### 定义登录 Action 和视图

将大部分工作委托给身份验证适配器后，创建 `LoginController::loginAction` 变得轻而易举。以下是代码，按照惯例应存在 `*$APP_DIR/application/modules/default/controllers/LoginController.php*`：

```php
<?php
class LoginController extends Zend_Controller_Action
{
    public function init()
    {
        $this->_helper->setLayout('admin');
    }

    // 登录操作
    public function loginAction()
    {
        $form = new Square_Form_Login;
        $this->view->form = $form;

        // 检查输入
        // 使用适配器进行身份验证
        // 将用户记录持久化到会话
        // 如果存在，重定向到原始请求 URL
        if ($this->getRequest()->isPost()) {
            if ($form->isValid($this->getRequest()->getPost())) {
                $values = $form->getValues();
                $adapter = new Square_Auth_Adapter_Doctrine(
                    $values['username'], $values['password']
                );

                $auth = Zend_Auth::getInstance();
                $result = $auth->authenticate($adapter);

                if ($result->isValid()) {
                    $session = new Zend_Session_Namespace('square.auth');
                    $session->user = $adapter->getResultArray('Password');

                    if (isset($session->requestURL)) {
                        $url = $session->requestURL;
                        unset($session->requestURL);
                        $this->_redirect($url);
                    } else {
                        $this->_helper->getHelper('FlashMessenger')
                            ->addMessage('登录成功。');
                        $this->_redirect('/admin/login');
                    }
                } else {
                    $this->view->message = '登录失败。请重试。';
                }
            }
        }
    }

    public function successAction()
    {
        if ($this->_helper->getHelper('FlashMessenger')->getMessages()) {
            $this->view->messages = $this->_helper
                ->getHelper('FlashMessenger')
                ->getMessages();
        } else {
            $this->_redirect('/');
        }
    }
}
```

`loginAction()` 读取通过登录表单提交的凭据，并使用上一步创建的身份验证适配器在应用程序数据库中验证。如果身份验证失败，它将带有错误消息重新渲染表单。如果没有，它将用户记录存储在会话中，然后查找会话命名空间查看是否存在原始请求 URL（稍后详细介绍）。如果有，将客户端重定向到该 URL；如果没有，则跳转到 `successAction()` 并渲染成功视图。

以下是 `*$APP_DIR/application/modules/default/views/login/login.phtml*` 中的登录视图脚本内容：

```html
<h2>登录</h2>

<div style="color:red; font-weight:bolder">
```



<?php echo $this->message; ?>

</div>

<?php echo $this->form; ?>

```

**问：** **为什么 `LoginController` 是“default”模块的一部分，而不是“catalog”模块？**

**答：** “catalog”模块作为与目录管理相关的控制器、操作和视图的容器。然而，登录/注销操作并不特定于目录管理，更适合位于全局或应用程序层级。因此，“default”模块是这些操作更符合逻辑的位置。

提问专家

## 第 5 章：处理 CRUD 操作

### 定义登出操作

`loginAction()` 的对应方法是 `logoutAction()`，它通过销毁认证会话并通过 `Zend_Auth::clearIdentity` 方法清除用户身份。如下所示：

```php
class LoginController extends Zend_Controller_Action
{
    public function logoutAction()
    {
        Zend_Auth::getInstance()->clearIdentity();
        Zend_Session::destroy();
        $this->_redirect('/admin/login');
    }
}
```

### 保护管理操作

最后一步是你想要保护的动作添加身份验证检查。由于到目前创建的所有管理操作都位于单个控制器 `Catalog_AdminItemController` 中，这些检查可以方便地添加到该控制器的 `preDispatch()` 方法中。更新后的 `preDispatch()` 方法如下：

```php
class Catalog_AdminItemController extends Zend_Controller_Action
{
    // 处理管理 URL 的动作
    public function preDispatch()
    {
        // 设置管理布局
        // 检查用户是否已认证
        // 如果未认证，重定向到登录页面
        $url = $this->getRequest()->getRequestUri();
        $this->_helper->layout->setLayout('admin');
        if (!Zend_Auth::getInstance()->hasIdentity()) {
            $session = new Zend_Session_Namespace('square.auth');
            $session->requestURL = $url;
            $this->_redirect('/admin/login');
        }
    }
}
```

由于此更改，每当路由器接收到管理操作时，`preDispatch()` 方法都会首先使用 `Zend_Auth::hasIdentity` 方法检查用户身份是否已通过认证。如果不存在此类身份，该方法将返回 `false`。如果发生这种情况，请求 URL 将存储在会话中，客户端将被重定向到登录表单。

登录成功后，`loginAction()`（在上一节中讨论过）将从会话中获取请求 URL 并将客户端重定向回该 URL。`preDispatch()` 方法将再次执行，但由于此时用户身份已经确认，`hasIdentity()` 将返回 `true`，请求的动作将以正常方式进行分发。

### 更新主布局

如前节所示，`Zend_Auth` 对象的 `hasIdentity()` 方法为测试用户是否已认证提供了一个方便的方法。这一事实可以在管理布局中得到良好利用，根据用户是否登录来选择性地显示某些菜单项。这是一个示例，它更新了 `$APP_DIR/application/layouts/admin.phtml` 处的管理布局，当用户登录时在主菜单中显示“登出”项目，否则显示“登录”项目。布局的更改已用**粗体**标出。

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
    <base href="/" />
    <link rel="stylesheet" type="text/css" href="/css/master.css" />
    <link rel="stylesheet" type="text/css" href="/css/admin.css" />
    <link rel="stylesheet" type="text/css" href="/css/yui/calendar.css" />
    <script src="/js/form.js"></script>
</head>
<body>
    <div id="header">
        <div id="logo">
            <img src="/images/logo-admin.gif" />
        </div>
        <div id="menu">
            **<?php if (Zend_Auth::getInstance()->hasIdentity()): ?>**
            **<a href="<?php echo $this->url(array(), 'admin-catalog-index'); ?>">CATALOG</a>**
            **<a href="<?php echo $this->url(array(), 'logout'); ?>">LOGOUT</a>**
            **<?php else: ?>**
            **<a href="<?php echo $this->url(array(), 'login'); ?>">LOGIN</a>**
            **<?php endif; ?>**
        </div>
    </div>
    <div id="content">
        <?php echo $this->layout()->content ?>
    </div>
    <div id="footer">
        <p>Created with <a href="http://framework.zend.com/">Zend Framework</a>. Licensed under <a href="http://www.creativecommons.org/">Creative Commons</a>。</p>
    </div>
</body>
</html>
```

大功告成了！要查看运行效果，请尝试访问 `http://square.localhost/admin/catalog/item/index` 处的摘要页。你应该看到一个登录表单，如图 5-11 所示。

一旦你通过此表单提交有效凭据，你应该被自动重定向到摘要页。主菜单也应该通过显示新的“登出”链接来反映你的登录状态，如图 5-12 所示。

图 5-12：管理中的登录后菜单

图 5-11：管理的登录表单

### 总结

本章重点关注了构建应用程序时会遇到的两个最常见的任务：实现 CRUD 操作和用户认证。在本章结束时，SQUARE 示例变得内容丰富。用户现在可以直接向目录添加内容，而管理员能够通过一个“感知”用户是否登录的系统来查看、显示、修改或删除内容。

记住可以通过以下链接了解更多关于本章讨论的话题：

- `Zend_Controller` 组件，访问 `http://framework.zend.com/manual/en/controller.html`
- `Zend_Layout` 组件，访问 `http://framework.zend.com/manual/en/layout.html`
- `Zend_Auth` 组件，访问 `http://framework.zend.com/manual/en/auth.html`

**问：** 我可以使用 `Zend_Auth` 根据用户角色或权限授予或拒绝对应用程序资源的访问权限吗？

**答：** 不可以。正如 Zend Framework 手册指出的，`Zend_Auth` 关注的是用户认证（验证用户是否是其声称身份），而不是用户访问控制（验证用户是否有权访问特定资源）。在实际操作中，这意味着一旦通过认证，用户就可以访问任何或所有受保护的动作；系统不允许对哪些用户可以访问哪些动作进行细粒度控制。如果你的应用程序需要根据角色控制对特定动作的访问，你应该考虑使用 `Zend_Acl` 组件。

## 第 6 章：索引、搜索与数据格式化

Zend Framework：初学者指南

### 核心技能与概念
- 动态生成并执行数据库查询
- 学习存储和索引不同类型的数据
- 使用 `Zend_Search_Lucene` 组件创建全文搜索引擎
- 理解如何在运行时启用输出类型切换
- 以多种格式（包括 XML）表达相同的输出内容

你是否见过掉在水桶里的海绵？在最初的一分钟或两分钟里，由于它大部分时候还是干的，它会快乐地浮在水面上，无忧无虑。然而，随着它吸收了越来越多的水，它逐渐下沉，直到完全浸湿并准备好使用。面向用户的 Web 应用程序非常如此。当它首次在 Web 上启动时，它通常只是一个空壳，等待世界的关注。随着它吸引用户，它开始吸收数据，正向网络效应开始占据主导：使用的人越多，对其他人来说价值就越高。

这有什么关系呢？嗯，当你的应用程序开始积累用户内容时，让这些内容以不同的格式可搜索和可访问变得越来越重要，这样用户可以出于不同的目的利用它们（例如，将其与其他服务的内容混合）。仅仅提供一个数据库内容的可浏览索引是不够的；你还需要为用户提供搜索数据和过滤结果的不同方法，以及表达这些搜索结果的不同格式。

这本章大有用武之地。在接下来的几页中，它将介绍为 Web 应用程序添加搜索功能的基础知识，并提供基于过滤的搜索和全文搜索的示例。它还将讨论 Zend Framework 的 `ContextSwitch` 辅助类，它提供了一个灵活且扩展的系统来处理多种输出类型，包括 XML 和 JSON。

### 搜索与过滤数据库记录

在上一章中，你构建了一个接口，允许用户将项目上传到产品目录，允许管理员审核并批准这些项目以显示在公共 Web 网站上。本节将基于上一章的工作，创建一个接口供用户浏览已批准的项目并根据各种标准进行过滤。

### 定义搜索表单

为了这个说明性示例，让我们让搜索表单尽可能简单，假设用户只需要根据三个标准搜索邮票：年份、价格和等级。以下是搜索表单的定义：

尝试这样做 6-1

```php
<?php
class Square_Form_Search extends Zend_Form
{
    public $messages = array(
        Zend_Validate_Int::INVALID => '%value%' is not an integer',
        Zend_Validate_Int::NOT_INT => '%value%' is not an integer'
    );

    public function init()
    {
        // 初始化表单
        $this->setAction('/catalog/item/search')
            ->setMethod('get');

        // 设置表单装饰器
        $this->setDecorators(array(
            array('FormErrors', array('markupListItemStart' => '', 'markupListItemEnd' => '')),
            array('FormElements'),
            array('Form')
        ));

        // 为年份创建文本输入
        $year = new Zend_Form_Element_Text('y');
        $year->setLabel('Year:')
            ->setOptions(array('size' => '6'))
            ->addValidator('Int', false, array('messages' => $this->messages))
            ->addFilter('HtmlEntities')
            ->addFilter('StringTrim');

        // 为价格创建文本输入
        $price = new Zend_Form_Element_Text('p');
        $price->setLabel('Price:')
            ->setOptions(array('size' => '8'))
            ->addValidator('Int', false, array('messages' => $this->messages))
            ->addFilter('HtmlEntities')
            ->addFilter('StringTrim');

        // 为等级创建选择输入
        $grade = new Zend_Form_Element_Select('g');
        $grade->setLabel('Grade:')
            ->addValidator('Int', false, array('messages' => $this->messages))
            ->addFilter('HtmlEntities')
            ->addFilter('StringTrim')
            ->addMultiOption('', 'Any');

        foreach ($this->getGrades() as $g) {
            $grade->addMultiOption($g['GradeID'], $g['GradeName']);
        }

        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit');
        $submit->setLabel('Search')
            ->setOptions(array('class' => 'submit'));

        // 将元素附加到表单
        $this->addElement($year)
            ->addElement($price)
            ->addElement($grade)
            ->addElement($submit);

        // 设置元素装饰器
        $this->setElementDecorators(array(
            array('ViewHelper'),
            array('Label', array('tag' => '<span>'))
        ));

        $submit->setDecorators(array(
            array('ViewHelper'),
        ));
    }

    public function getGrades()
    {
        $q = Doctrine_Query::create()
            ->from('Square_Grade','g');
        return $q->fetchArray();
    }
}
```

这是一个相当标准的表单定义，是你现在应该已经熟悉的类型：文本输入字段、一个选择列表和一个提交按钮，全部封装在 `init()` 方法中。注意，默认标签已经过修改，将每个元素封装在 `<span>` 而不是 `<dt>` 中。

还有一点需要注意。到目前为止，在所有示例中，验证错误都会自动显示在每个元素下方的用户面前。然而，如果要求将错误集中显示在表单顶部，则实现这一点需要你从 Zend Framework 对象中禁用默认的 `Errors` 装饰器。

### 定义控制器和视图

下一步是为搜索接口定义动作（action）和视图。使用以下 `searchAction()` 更新 `Catalog_ItemController` 类：

```php
<?php
class Catalog_ItemController extends Zend_Controller
{
    public function searchAction()
    {
        // 生成表单
        $form = new Square_Form_Search();
        $this->view->form = $form;

        // 检查有效输入



```php
if ($form->isValid($this->getRequest())) {
    $input = $form->getValues();

    // 生成基础查询
    $q = Doctrine_Query::create()
        ->from('Square_Item', 'i')
        ->leftJoin('i.Country', 'c')
        ->leftJoin('i.Grade', 'g')
        ->where('i.DisplayStatus = 1');

    // 将条件附加到基础查询
    if (!empty($input['y'])) {
        $q->addWhere('i.Year = ?', $input['y']);
    }

    if (!empty($input['g'])) {
        $q->addWhere('i.GradeID = ?', $input['g']);
    }

    if (!empty($input['p'])) {
        $q->addWhere('i.SalePrice BETWEEN ? AND ?', explode(',', $input['p']));
    }

    // 执行查询并将结果附加到视图
    $results = $q->fetchArray();
    $this->view->results = $results;
}
```

视图脚本负责遍历结果并格式化每个记录以便显示。如果有错误，将通过`FormErrors`装饰器显示在结果页顶部。以下是视图脚本，它应该保存为`$APP_DIR/modules/catalog/views/scripts/search.php`：

```php
<h2>Search</h2>

<?php echo $this->form; ?>

<h2>Search Results</h2>

<p><?php echo count($this->results); ?> result(s) found.</p>

<?php if (count($this->results)): ?>
    <?php $x = 1; ?>

    <?php foreach ($this->results as $r): ?>
        <div>
            <?php echo $x++; ?>.

            <a href="<?php echo $this->url(array('id' => $this->escape($r['RecordID'])), 'catalog-display'); ?>">
                <?php echo $this->escape($r['Title']); ?>
                (<?php echo $this->escape($r['Year']); ?>)
            </a>

            <?php if (!empty($r['Description'])): ?>
                <br />
                <?php echo $this->escape($r['Description']); ?>
            <?php endif; ?>

            <strong>
                等级：
                <?php echo $this->escape($r['Square_Model_Grade']['GradeName']); ?> |
                国家：
                <?php echo $this->escape($r['Square_Model_Country']['CountryName']); ?> |
                售价：
                $<?php echo sprintf('%0.2f', $this->escape($r['SalePriceMin'])); ?>
                至
                $<?php echo sprintf('%0.2f', $this->escape($r['SalePriceMax'])); ?>
            </strong>
        </div>

        <br />

        <?php $x++; ?>
    <?php endforeach; ?>
<?php endif; ?>

<div>
    <a href="<?php echo $this->url(array(
        'module' => 'catalog',
        'controller' => 'item',
        'action' => 'create'
    ), null, true); ?>">添加项目</a>
</div>
```

## 更新主布局

现在剩下的工作是使用`url()`辅助方法更新应用程序主菜单中的导航链接，以反映新的浏览/搜索表单。要做到这一点，请更新`$APP_DIR/application/layouts/master.phtml`中的主布局，加粗显示更改：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">

...

<div id="menu">

<a href="<?php echo $this->url(array(), 'home'); ?>">首页</a>

<a href="<?php echo $this->url(array('page' => 'services', 'static-content'); ?>">服务</a>

<a href="<?php echo $this->url(array('module' => 'catalog', 'controller' => 'item', 'action' => 'search'), 'default', true); ?>">目录</a>
```

（上续）

<a href="<?php echo $this->url(array(), 'contact'); ?>">联系我们</a>
</div>
</div>

...
</html>
```

> **注意**
>
> 请注意上一个列表中传递给`url()`视图辅助器的参数。正如你已经所知道的，第二个参数指定了用于生成 URL 的路由名称。如果此参数为`null`，视图辅助器将使用生成当前 URL 的路由作为新 URL 的基础。由于这在处理重置 URL 请求的路由时可能会产生奇怪的错误，因此在这种情况下，显式告诉框架使用其标准或“默认”路由是一个好主意，对应于`/module/controller/action`格式的 URL。

如果你现在尝试通过 Web 浏览器访问 URL`http://square.localhost/catalog/item/search`，你应该看到类似于图 6-1 中的所示表单。

在搜索输入字段中输入值并提交表单，如果一切顺利，你应该看到与你的搜索参数匹配的修订项目列表，如图 6-2 所示。

图 6-1：SQUARE 目录搜索表单

你也可以尝试使用无效值提交表单。内置验证器将捕获你的无效输入，并在页面顶部以单个块的形式显示错误消息，如图 6-3 所示。

## 添加全文搜索

当你构建应用程序搜索引擎时，有两种不同的方法可以采用。你可以创建一个基于过滤的搜索引擎，其中用户输入的特定标准被用于过滤搜索结果列表，如上一节所示。或者，你可以创建一个全文搜索引擎，它索引应用程序内容并根据用户输入的关键词查找匹配项。在现代 Web 应用程序中，全文搜索通常更受青睐，因为它比数据库搜索通常更快且能产生更准确的结果。

Zend Framework 自带了一个非常强大的全文搜索组件，称为`Zend_Search_Lucene`。它是 Apache Lucene 项目的纯 PHP 实现，该组件既可以用于索引各种文档类型（包括文本、HTML 和某些 Microsoft Office 2007 格式），也可以用于对索引数据执行不同类型的搜索查询。

使用`Zend_Search_Lucene`实现全文搜索涉及两个主要操作：数据索引和数据搜索。索引涉及扫描一组文档并创建其内容的索引；搜索涉及查找此索引以找到匹配各种用户指定标准的文档。接下来的章节将提供这两个操作的概述。

### 索引数据

`Zend_Search_Lucene`索引由单个文档组成，每个文档可能被进一步拆分为字段。当你构建索引时，`Zend_Search_Lucene`允许用户对文档每个字段的处理方式进行精确控制。这里的两个基本参数是索引和存储：索引字段可用于搜索，而存储字段可以显示在搜索结果。字段有五种基本类型：

- **Keyword（关键字）**：字段不被分词，但在索引中被索引和存储。
- **Text（文本）**：字段会被分词、索引并存储。
- **UnStored（未存储）**：字段会被分词和索引，但不被存储。
- **UnIndexed（未索引）**：字段会被分词并存储，但不被索引。
- **Binary（二进制）**：字段不被分词或索引，但会被存储。

当你决定在你的`Zend_Search_Lucene`索引中使用哪些字段类型时，清楚哪些字段将用作搜索标准以及哪些字段将计划显示在搜索结果中是非常重要的。为了说明这在实践中是如何运作的，假设你有一组如下格式的 XML 文档：

```xml
<?xml version='1.0'?>

<document>
    <id>5468</id>
    <from>Jim Doe &lt;jim@example.com&gt;</from>
    <to>Jane Doe &lt;jane@example.com&gt;</to>
    <subject>Re: Hello</subject>
    <date>Tuesday, February 27, 2008 10:45 PM</date>
    <body>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod incididunt ut labore et dolore aliqua. Ut enim ad minim veniam, nostrud exercitation ullamco ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore fugiat nulla pariatur. Excepteur sint occaecat cupidatat pro deserunt mollit anim id laborum.</body>
</document>
```

以下是示例代码，说明了如何对文档进行索引：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller
{
    public function indexAction()
    {
        // 获取索引目录
        $index = Zend_Search_Lucene::create('/tmp/indexes');

        foreach (glob('*.xml') as $file) {
            // 读取源 xml
            $xml = simplexml_load_file($file);

            // 在索引中创建新文档
            $doc = new Zend_Search_Lucene_Document();

            // 索引并存储字段
            $doc->addField(Zend_Search_Lucene_Field::UnIndexed('id', $xml->id));
            $doc->addField(Zend_Search_Lucene_Field::Text('from', $xml->from));
            $doc->addField(Zend_Search_Lucene_Field::Text('to', $xml->to));
            $doc->addField(Zend_Search_Lucene_Field::Text('date', strtotime($xml->date)));
            $doc->addField(Zend_Search_Lucene_Field::UnStored('subject', $xml->subject));
            $doc->addField(Zend_Search_Lucene_Field::UnStored('body', $xml->body));

            // 将结果保存到索引
            $index->addDocument($doc);
        }

        // 设置索引中的文档数量
        $count = $index->count();
    }
}
```

索引中的每个文档表示为`Zend_Search_Lucene_Document`对象，而每个消息的各个字段表示为`Zend_Search_Lucene_Field`对象。在索引数据时，定义哪些字段应该是可搜索以及哪些字段应该显示在搜索结果中是一项关键任务。之前的示例假设收件人、日期、主题和正文字段应该是可搜索的，而只有收件人和日期字段应该显示在搜索结果中。将正文和主题字段标记为非存储（`UnStored`）字段可以使它们变得可搜索，同时减少索引占用的磁盘空间；将收件者和日期字段标记为文本（`Text`）字段则既可以对其进行搜索，也可以在搜索结果中显示。

## 搜索数据

一旦数据完成索引，下一步就是对其进行搜索。`Zend_Search_Lucene`自带了一个功能齐全的查询引擎，用于对索引执行简单和复杂的查询。可以通过对用户输入应用内置查询解析器来创建查询，也可以使用 API 方法编程地生成查询。对于简单的关键词查询，标准查询解析器就足够；对于包含修饰符、邻近约束、子查询或字段组的复杂查询，则应使用 API 方法创建。

以下是一些示例代码，说明了如何搜索已索引文档集并显示匹配结果：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function searchAction()
    {
        // 从 $_GET['query'] 获取查询字符串
        // 如果有效，打开索引并解析查询字符串
        // 执行查询并返回结果对象数组
        $input->setData($this->getRequest()->getParams());

        if ($input->isValid()) {
            $index = Zend_Search_Lucene::open('/tmp/indexes');

            $results = $index->find(
                Zend_Search_Lucene_Search_QueryParser::parse($input->query)
            );

            $this->view->results = $results;
        }
    }
}
```



如前面的代码所示，第一步是使用`Zend_Search_Lucene::open()`方法打开之前创建的索引句柄。接下来将查询字符串传递给`Zend_Search_Lucene`对象的`find()`方法，以扫描匹配中的文档。匹配项以`Zend_Search_Lucene_Search_QueryHit`对象的形式返回，并按得分排名。这些对象中的每一个都作为对象属性暴露文档编号和得分。文档的其他存储字段也可以作为对象属性访问，如之前的示例所示。所有字段值都会自动编码为 UTF-8。

传递给`find()`方法的查询字符串可能包含关键词、短语、通配符、范围约束、邻近修饰符以及 AND、OR 和 NOT 等布尔运算符。当用户直接提交此查询字符串时，最好将其通过`Zend_Search_Lucene_Search_QueryParser::parse()`方法处理，该方法负责自动解析和分词查询字符串，并将其转换为查询对象集。这也减少了所需的输入验证量。

## 第 6 章：数据的索引、搜索和格式化

**注意**

由于本书的范围限制，无法对`Zend_Search_Lucene`支持的查询语言进行详尽讨论。然而，你可以使用章末的链接查找有关该主题的详细信息。

### 创建全文搜索引擎

在有了这些背景信息的情况下，让我们看看在实际场景中`Zend_Search_Lucene`是如何工作的。本节将把基于过滤（filter）的搜索引擎替换为基于`Zend_Search_Lucene`的全文搜索系统（该引擎在本章之前为 SQUARE 应用创建的）。

### 定义索引位置

`Zend_Search_Lucene`全文搜索索引以磁盘文件的形式存储，因此首要任务之一是为这些文件定义位置。因此，请创建`$APP_DIR/data/indexes/`目录，这是 Zend Framework 推荐目录布局下搜索索引文件的默认位置。

```shell
shell> cd /usr/local/apache/htdocs/square
shell> mkdir data
shell> mkdir data/indexes
```

同时，在应用程序配置文件`$APP_DIR/application/configs/application.ini`中更新该位置也是一个好主意，这样可以在 action 内部使用它。打开此文件并使用以下配置指令进行更新：

```ini
indexes.indexPath = APPLICATION_PATH "/../data/indexes"
```

**尝试一下 6-2**

**Q：我如何排序或限制来自 Zend_Search_Lucene 搜索的结果？**

**A：** 默认情况下，`Zend_Search_Lucene`返回所有匹配的文档并按得分排序。如果这不符合你的需求，可以通过向`find()`方法传递额外的参数来定义排序字段和排序顺序。同样，你可以通过`setResultSetLimit()`方法指定限制来限制返回的匹配项数量。

## 定义自定义路由

在更新应用程序配置时，为`createFulltextIndexAction()`添加路由也是一个好主意。由于索引创建通常是一项管理任务，该 action 应该是`Catalog_AdminItemController`的一部分。以下是相应的路由定义：

```ini
resources.router.routes.admin-fulltext-index-create.route = /admin/catalog/fulltext-index/create
resources.router.routes.admin-fulltext-index-create.defaults.module = catalog
resources.router.routes.admin-fulltext-index-create.defaults.controller = admin.item
resources.router.routes.admin-fulltext-index-create.defaults.action = create.fulltext.index
```

### 定义索引 Action 和视图

下一步是实际为应用程序数据库中存储的内容构建全文索引。实现此最简单的方法是执行 Doctrine 查询从数据库中检索记录，然后在循环中将这些馈给索引器。以下是负责此任务的`createtextIndexAction()`代码：

```php
<?php

class Catalog_AdminItemController extends Zend_Controller_Action
{
    // 创建全文索引
    public createtextIndexAction()
    {
        // 获取索引目录
        $config = $this->getInvoke('bootstrap')->getOption('indexes');
        $index = Zend_Search_Lucene::create($config);

        // 创建并执行查询
        $q = Doctrine_Query::create()
            ->from('Square_Model_Item', 'i')
            ->leftJoin('Square_Model_Country', 'c')
            ->leftJoin('Square_Model_Grade', 'g')
            ->leftJoin('Square_Model_Type', 't')
            ->where('i.DisplayStatus = 1')
            ->addWhere('i.DisplayUntil >= CURDATE()');

        $result = $q->fetchArray();

        foreach ($result as $r) {
            // 在索引中创建文档
            $doc = new Zend_Search_Lucene_Document();

            // 索引并存储字段
            $doc->addField(Zend_Search_Lucene_Field::Text('Title', $r['Title']));
            $doc->addField(Zend_Search_Lucene_Field::Text('Country', $r['CountryName']));
            $doc->addField(Zend_Search_Lucene_Field::Text('Grade', $r['GradeName']));
            $doc->addField(Zend_Search_Lucene_Field::Text('Year', $r['Year']));
            $doc->addField(Zend_Search_Lucene_Field::UnStored('Description', $r['Description']));
            $doc->addField(Zend_Search_Lucene_Field::UnStored('Denomination', $r['Denomination']));
            $doc->addField(Zend_Search_Lucene_Field::UnStored('Type', $r['TypeName']));
            $doc->addField(Zend_Search_Lucene_Field::UnIndexed('SalePriceMin', $r['Denomination']));
            $doc->addField(Zend_Search_Lucene_Field::UnIndexed('SalePriceMax', $r['Denomination']));
            $doc->addField(Zend_Search_Lucene_Field::UnIndexed('RecordID', $r['RecordID']));

            // 将结果添加到索引
            $index->addDocument($doc);
        }

        // 设置索引中的文档数量
        $count = $index->count();
        $this->_helper->getHelper('FlashMessenger')
            ->addMessage("索引已创建，包含 $count 个文档。");
        $this->_redirect('/admin/catalog/item/success');
    }
}
```



# Zend Framework：入门指南 ## 更新摘要视图

更新管理摘要页面也是一个不错的主意，该页面位于`$APP_DIR/application/modules/catalog/views/scripts/admin-item/index.phtml`，以便显示指向新操作的链接。视图脚本中的更改已用粗体标出。

### 列表项

```php
<?php if (count($this->records)): ?>
<div id="records">
<form method="post" action="<?php echo $this->url(array(), 'admin-catalog-delete'); ?>">
<table>
...
<tr>
<td colspan="7"><input type="submit" name="submit" style="width:150px" value="删除选定" /></td>
<td colspan="2"><a href="<?php echo $this->url(array(), 'admin-fulltext-index-create'); ?>">更新全文索引</a></td>
</tr>
</table>
</form>
</div>
<?php else: ?>
未找到相关记录
<?php endif; ?>
```

## 更新搜索表单

一旦处理完索引端，就剩下搜索端需要处理了。首先更新位于`$APP_DIR/library/Square/Form/Search.php`的搜索表单定义，使其仅包含一个用于搜索关键词的文本输入字段。以下是修改后的表单定义：

```php
<?php
class Square_Form_Search extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/catalog/item/search')
            ->setMethod('get');
        // 创建关键词的文本输入
        $query = new Zend_Form_Element_Text('q');
        $query->setLabel('关键词:')
            ->setOptions(array('size' => '20'))
            ->addFilter('HtmlEntities')
            ->addFilter('StringTrim');
        $query->setDecorators(array(
            array('ViewHelper'),
            array('Errors'),
            array('Label', array('tag' => '<span>')),
        ));
        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit');
        $submit->setLabel('搜索')
            ->setOptions(array('class' => 'submit'));
        $submit->setDecorators(array(
            array('ViewHelper'),
        ));
        // 将元素添加到表单
        $this->addElement($query)
            ->addElement($submit);
    }
}
?>
```

## 更新搜索 Action 和视图

最后一步是更新`Catalog_ItemController::searchAction`，使用`Zend_Search_Lucene`的全文索引而不是 Doctrine 查询。以下是修改后的代码：

```php
<?php
class Catalog_ItemController extends Zend_Controller_Action
{
    // 执行全文搜索的操作
    public function searchAction()
    {
        // 生成输入表单
        $form = new Square_Form_Search;
        $this->view->form = $form;
        // 获取匹配搜索条件的项
        if ($form->isValid($this->getRequest()->getParams())) {
            $input = $form->getValues();
            if (!empty($input['q'])) {
                $config = $this->getInvokeArg('bootstrap')->getOption('indexes');
                $index = Zend_Search_Lucene::open($config['indexPath']);
                $results = $index->find(
                    Zend_Search_Lucene_Search_QueryParser::parse($input['q']));
                $this->view->results = $results;
            }
        }
    }
}
?>
```

*(续上)*

`Zend_Search_Lucene find()`方法的返回值与`Doctrine fetchArray()`方法不同；字段值现在作为对象属性而非数组元素暴露。因此，有必要更新相应的视图脚本，位于`$APP_DIR/modules/catalog/views/scripts/item/search.phtml`，如下：

### 搜索

```php
<?php echo $this->form; ?>
```

### 搜索结果

```php
<p>找到了 <?php echo count($this->results); ?> 个结果(s)。</p>
<?php if (count($this->results)): ?>
<?php $x=1; ?>
<?php foreach ($this->results as $r): ?>
<div>
<?php echo $x; ?>.
<a href="<?php echo $this->url(array('id' => $this->escape($r->RecordID)), 'catalog-display'); ?>">
<?php echo $this->escape($r->Title); ?>
(<?php echo $this->escape($r->Year); ?>)
</a>
<br/>
得分: <?php显示 printf('%1.4f', $this->escape($r->score)); ?>
<br/>
<strong>
等级：<?php echo $this->escape($r->Grade); ?> |
国家：<?php echo $this->escape($r->Country); ?> |
售价：
$<?php echo sprintf('%0.2f', $this->escape($r->SalePriceMin)); ?>
至
$<?php echo sprintf('%0.2f', $this->escape($r->SalePriceMax)); ?>
</strong>
</div>
<br/>
<?php $x++; ?>
<?php endforeach; ?>
<?php endif; ?>
<div>
<a href="<?php echo $this->url(array(
'module' => 'catalog',
'controller' => 'item',
'action' => 'create'), null, true); ?>">添加项目</a>
</div>
```

要查看此操作的效果，请先登录管理面板，并通过访问 URL `http://square.localhost/admin/catalog/fulltext-index/create` 创建全文索引。一旦索引创建过程完成，你应该会看到一个成功页面，如图 6-4 所示。现在你可以尝试通过浏览器访问 URL `http://square.localhost/catalog/item/search` 来搜索索引了。你应该能看到一个修改后的搜索表单，如图 6-5 所示。在输入字段中输入一个或多个关键词并提交，如果一切顺利，你应该看到与你的关键词匹配的项列表，如图 6-6 所示。

## 处理多种输出类型

现代 Web 应用程序不仅支持 HTML——它们还能够提供 RSS、JSON、XML 以及许多其他格式。由于 MVC 模式区分了数据和呈现，它非常适合这种需求；支持一种新的输出类型变得非常简单，只需创建一个包含适当格式代码和标记的新视图即可。最重要的是，这些更改仅局限于视图层，无需对控制器和模型层进行任何修改即可完成。

Zend Framework 提供了一个强大的`ContextSwitch`插件，允许根据请求的内容动态切换输出格式。以下示例展示了如何使用该插件支持多种输出类型：

```php
<?php
class Sandbox_Example extends Zend_Controller_Action
{
    public function init()
    {
        // 初始化上下文切换
        $contextSwitch = $this->helper('contextSwitch');
        $contextSwitch->defaultStrategy('json');
    }

    public function indexAction()
    {
        // 准备数据
        $this->data = array(
            'message' => 'Hello World',
            'timestamp' => time()
        );
        
        // 根据请求头动态切换策略
        if ($this->getRequest()->getHeader('Accept')) {
            if (strpos($this->getRequest()->getHeader('Accept'), 'application/xml') !== false) {
                $this->helper('contextSwitch')->setStrategy('xml');
            } elseif (strpos($this->getRequest()->getHeader('Accept'), 'application/json') !== false) {
                $this->helper('contextSwitch')->setStrategy('json');
            }
        }
    }
}
?>
```

在上述示例中，你需要为每个策略创建相应的视图脚本：

`index.phtml` (默认 HTML)

```html
<p>消息：<?php echo $this->data['message']; ?></p>
```

`index.json`

```json
<?php echo json_encode($this->data); ?>
```

`index.xml`

```xml
<?xml version="1.0" encoding="UTF-8"?>
<root>
    <message><?php echo $this->data['message']; ?></message>
    <timestamp><?php echo $this->data['timestamp']; ?></timestamp>
</root>
```

通过使用`ContextSwitch`插件，你可以轻松地扩展你的应用程序，以支持不同客户端所需的各种格式，同时保持核心业务逻辑的整洁。

## Zend Framework：入门指南

### 4. *初始化上下文*

这是最后一步，也是最简单的一步，因为它仅涉及调用 ContextSwitch 助者的`initContext()`方法。当不带任何参数调用此方法时，它将初始化所有定义的上下文并让工作开始。现在，你可以为操作的 URL 字符串挂载一个特殊的`?format=context-name`参数，以向 ContextSwitch 助手指示所需的输出类型——例如，使用`?format=yaml`用于 YAML 输出或使用`?format=xls`用于 XLS 输出。

## 在 XML 中表示搜索结果

为了说明 ContextSwitch 助手在实践中如何工作，让我们增强在本节之前创建的搜索引擎，以支持 XML 输出。以下章节将引导你完成这一过程。

### 启用 XML 上下文

由于 ContextSwitch 助手内置了 XML 和 JSON 上下文的定义，因此没有必要使用`addContext()`方法定义它们。相反，我们可以直接通过`addActionContext()`方法将 XML 上下文映射到`search-action()`方法。将此方法调用添加到`Catalog_ItemController`类的`init()`方法中，如下所示：

```php
<?php

class Catalog_ItemController extends Zend_Controller_Action
{
    public function init()
    {
        // 初始化上下文切换助手
        $contextSwitch = $this->_helper->getHelper('contextSwitch');
        $contextSwitch->addActionContext('search', 'xml')
            ->initContext();
    }
}
```

### 定义 XML 视图

一旦映射并初始化了 XML 上下，任何对 XML 格式搜索结果的请求将由相应的 XML 视图脚本处理。按照惯，此视图应保存为`$APP_DIR/application/modules/catalog/views/scripts/item/search.xml.phtml`。

它应该包含如下：

```php
<?php

// 创建 XML 文档
$dom = new DOMDocument('1.0', 'utf-8');

// 创建根元素
$root = $dom->createElementNS(
    'http://square.localhost', 'square:document');
$dom->appendChild($root);

// 转换为 SimpleXML
$xml = simplexml_import_dom($dom);

// 添加摘要元素
$xml->addChild('matches', count($this->results));
$xml->addChild('searchTime', time());

// 添加结果集元素
$results = $xml->addChild('results');
foreach ($this->results as $r) {
    $result = $results->addChild('result');
    $result->addChild('score', $this->escape($r->score));
    $result->addChild('id', $this->escape($r->RecordID));
    $result->addChild('title', $this->escape($r->Title));
    $result->addChild('year', $this->escape($r->Year));
    $result->addChild('grade', $this->escape($r->Grade));
    $result->addChild('country', $this->escape($r->Country));
    $price = $result->addChild('price');
    $price->addChild('min', $this->escape($r->SalePriceMin));
    $price->addChild('max', $this->escape($r->SalePriceMax));
}

// 输出
echo $xml->asXML();
?>
```

如果你熟悉 PHP 的 SimpleXML 和 DOM 扩展，上述脚本应该非常易读。它首先使用 PHP 的 DOM 扩展生成一个新的新的 XML 文档和序言，并为随后的 XML 数据定义自定义命名空间。然后，该文档被转换为 SimpleXML 对象（为了方便起见），由`search-action()`方法返回的结果集被处理并作为一系列 XML 元素呈现。一旦处理完整个结果集，将使用 SimpleXML 的`asXML()`方法将的 XML 文档树输出给请求客户端。

要查看此效果，请尝试访问`http://square.localhost/catalog/item/search`搜索 URL 并输入一组关键词。你应该会看到 HTML 格式的搜索结果，如图 6-6 所示。



现在，通过在 URL 字符串中附加额外的`?format=xml`参数来请求相同的 XML 格式搜索结果。在检测到此参数后，`ContextSwitch`（续）助手会自动切换输出类型，并为你展示 XML 格式的搜索结果，如图 6-7 所示。

**提示**

传递给`ContextSwitch`助手的`format`参数不必指定为 GET 参数。它可以来自任何有效的参数源，包括路由定义本身。

### 总结

一旦应用程序的基本 CRUD 函数运行，用户和管理员就可以自由地向其中添加数据。这产生了一个新问题，即如何让应用程序数据可访问、可搜索并导出到多种常见格式。本章专门关注这个问题，引导你完成为应用程序添加搜索功能的过程，并向你展示如何使用`Zend_Search_Lucene`组件。它还演示了`ContextSwitch`助手，它可以轻松地支持 XML、RSS、JSON 等其他不同的输出格式。

图 6-7：以 XML 表示的搜索结果

要了解更多关于本章中讨论的话题，请考虑访问以下链接：

- `Zend_Search_Lucene`组件，位于：
  - `http://framework.zend.com/manual/en/zend.search.lucene.html`

- `Zend_Search_Lucene`查询语言，位于：
  - `http://framework.zend.com/manual/en/zend.search.lucene.query-language.html`

- `ContextSwitch`助手，位于：
  - `http://framework.zend.com/manual/en/zend.controller.actionhelpers.html`

- PHP 的 `SimpleXML`扩展，位于：
  - `http://www.php.net/simplexml`

- PHP 的 `DOM`扩展，位于：
  - `http://www.php.net/dom`

- 使用`ContextSwitch`助手导出 Microsoft Excel 表格的讨论（Pablo Viquez），位于`http://www.pabloviquez.com/2009/08/export-excel-spreadsheets-using-zend-framework/`

- 使用`ContextSwitch`助手动态更改布局的讨论（Phil Brown），位于`http://morecowbell.net/2009/02/changing-layouts-on-the-fly-with-contextswitch/`

## 第 7 章：数据的分页、排序与上传

分页功能有趣的地方在于，实现此模式所需的程序代码是非常标准化的，并且不太会在不同项目之间发生变化。这使其成为实现为可重用组件的理想选择。事实上，大多数框架和数据库抽象层都自带了现成的分页组件。例如，Zend Framework 包含一个`Zend_Paginator`组件，它提供了针对不同数据源的适配器（包括针对`Zend_Db`的）。同样，Doctrine 也带有`Doctrine_Pager`组件，可以直接处理和分页 Doctrine 查询。

在`Zend_Paginator`和`Doctrine_Pager`之间并没有太大的区别：这两个组件的工作原理都是将单个数据集分成更小的子集，并通过生成导航链接以便在不同的子集之间切换。然而，由于分页通常与数据库结果集相关，因此使用所用数据库抽象层推荐或包含的分页器通常是有意义的。由于本书建议在所有的数据库访问操作中均使用 Doctrine，因此接下来的讨论将集中在`Doctrine_Pager`和`Doctrine_Query`组件上，并展示如何在 SQUARE 示例应用程序的上下文中使用它们来对数据库结果集进行分页和排序。

### 在路由中添加页码

分页组件的标准操作非常简单。组件首先配置每页显示的项目数量。然后，它通过将数据集中项目总数除以每页请求的项数来计算总页数，然后动态生成一组用于在页面之间移动的导航链接。每个链接都包含一个额外的 GET 参数（页码），页面控制器可以使用该参数来确定请求的是哪个数据子集。

为了说明其工作原理，请打开位于`$APP_DIR/application/configs/application.ini`的应用程序配置文件，并按照如下额外的参数更新管理摘要页的路由定义：

```ini
resources.router.routes.admin-catalog-index.route = /admin/catalog/item/index/**:page
resources.router.routes.admin-catalog-index.defaults.module = catalog
resources.router.routes.admin-catalog-index.defaults.controller = admin.item
resources.router.routes.admin-catalog-index.defaults.action = index
resources.router.routes.admin-catalog-index.defaults.page = 1
```

### 更新索引控制器和视图

下一步是更新`Catalog_AdminItemController::indexAction`，以便在构建 SELECT 查询时使用该参数。这就是`Doctrine_Pager`组件大显用场的地方。更新后的 action 代码如下所示：

```php
<?php

class Catalog_AdminItemController extends Zend_Controller_Action
{
    // 显示目录列表的 action
    public function indexAction()
    {
        // 为 GET 输入设置过滤器和验证器
        $filters = array(
            'page' => array('HtmlEntities', 'StripTags', 'StringTrim')
        );
        $validators = array(
            'page' => array('Int')
        );
        $input = new Zend_Filter_Input($filters, $validators);
        $input->setData($this->getRequest()->getParams());

        // 测试输入是否有效
        // 创建查询并设置分页器参数
        if ($input->isValid()) {
            $q = Doctrine_Query::create()
                ->from('Square_Model_Item i')
                ->leftJoin('i.Square_Model_Grade g')
                ->leftJoin('i.Square_Model_Country c')
                ->leftJoin('i.Square_Model_Type t');

            $perPage = 5;
            $numPageLinks = 5;

            // 初始化分页器
            $pager = new Doctrine_Pager($q, $input->page, $perPage);

            // 执行分页查询
            $result = $pager->execute(array(), Doctrine::HYDRATE_ARRAY);

            // 初始化分页布局
            $pagerRange = new Doctrine_Pager_Range_Sliding(
                array('chunk' => $numPageLinks), $pager);
            $pagerUrlBase = $this->view->url(
                array(), 'admin-catalog-index', 1) . "/{%page}";
            $pagerLayout = new Doctrine_Pager_Layout(
                $pager, $pagerRange, $pagerUrlBase);

            // 设置页链接显示模板
            $pagerLayout->setTemplate('<a href="{%url}">{%page}</a>');
            $pagerLayout->setSelectedTemplate(
                '<span class="current">{%page}</span>');
            $pagerLayout->setSeparatorTemplate('&nbsp;');

            // 设置视图变量
            $this->view->records = $result;
            $this->view->pages = $pagerLayout->display(null, true);
        } else {
            throw new Zend_Controller_Action_Exception('Invalid input');
        }
    }
}
```

这段代码与原始代码的区别在于，查询通过`Doctrine_Pager`组件进行路由，该组件在初始化时带有查询、页码和每页项目数（在本例中为四个）。当通过此组件的`execute()`方法执行查询时，它会自动限制为仅检索与指定偏移量对应的记录集。然而，仍然存在生成导航链接的问题，以便用户可以访问其他页面。这由`Doctrine_Layout`组件处理，它接受一个模板，然后动态生成一组导航链接，并将变量占位符替换为实际页码。`display`方法的输出是一个 HTML 块，可以直接整合到视图中，如下：

```html
<h2>项目</h2>
<?php if (count($this->records)): ?>
    <div id="pager">
        <?php echo $this->pages; ?>
    </div>
    <div id="records">
        <!-- 记录循环 -->
    </div>
<?php else: ?>
    未找到记录
<?php endif; ?>
```

### 在路由中添加排序标准

分页是划分数据集的一种方法，但还有其他方法。另一个常见的需求是允许用户根据其某个字段对数据集进行排序。在这里，指示排序字段和方向的额外参数被添加到 URL 请求中，页面控制器在将数据交给视图显示之前会根据这些参数进行排序。

要查看其如何工作，请返回`$APP_DIR/application/configs/application.ini`的应用程序配置文件，并按照示例所示两个额外的参数进一步修订路由定义：

```ini
resources.router.routes.admin-catalog-index.route = /admin/catalog/item/index/:page/**:sort/:dir
resources.router.routes.admin-catalog-index.defaults.module = catalog
resources.router.routes.admin-catalog-index.defaults.controller = admin.item
resources.router.routes.admin-catalog-index.defaults.action = index
resources.router.routes.admin-catalog-index.defaults.page = 1
resources.router.routes.admin-catalog-index.defaults.sort = RecordID
resources.router.routes.admin-catalog-index.defaults.dir = asc
```

这些参数应该被整合到`Catalog_AdminItemController::indexAction`生成的 Doctrine 查询中。可以使用`InArray`验证器来确保只有有效的参数进入 action 的主体部分。修改后的 action 代码如下所示：

```php
// action to display list of catalog items
public function indexAction()
{
    // set filters and validators for GET input
    $filters = array(
        'sort' => array('HtmlEntities', 'StripTags', 'StringTrim'),
        'dir' => array('HtmlEntities', 'StripTags', 'StringTrim'),
        'page' => array('HtmlEntities', 'StripTags', 'StringTrim')
    );
    $validators = array(
        'sort' => array(
            'Alpha',
            array('InArray', 'haystack' =>
                array('RecordID', 'Title', 'Denomination',
                'CountryID', 'GradeID', 'Year'))
        ),
        'dir' => array(
            'Alpha',
            array('InArray', 'haystack' =>
                array('asc', 'desc'))
        ),
        'page' => array('Int')
    );
    $input = new Zend_Filter_Input($filters, $validators);
    $input->setData($this->getRequest()->getParams());

    // test if input is valid
    // create query and set pager parameters
    if ($input->isValid()) {
        $q = Doctrine_Query::create()
            ->from('Square_Model_Item i')
            ->leftJoin('i.Square_Model_Grade g')
            ->leftJoin('i.Square_Model_Country c')
            ->leftJoin('i.Square_Model_Type t')
            ->orderBy(sprintf('%s %s', $input->sort, $input->dir));
        $perPage = 4;
        $numPageLinks = 5;
        // initialize pager
        $pager = new Doctrine_Pager($q, $input->page, $perPage);
        // execute paged query
        $result = $pager->execute(array(), Doctrine::HYDRATE_ARRAY);
```

*(续上)*



```php
// initialize pager layout
$pagerRange = new Doctrine_Pager_Range_Sliding(array('chunk' =>
$numPageLinks), $pager);
$pagerUrlBase = $this->view->url(array(), 'admin-catalog-index',
1) . "/{%page}/{$input->sort}/{$input->dir}";
$pagerLayout = new Doctrine_Pager_Layout($pager, $pagerRange,
$pagerUrlBase);

// set page link display template
$pagerLayout->setTemplate('<a href="{%url}">{%page}</a>');
$pagerLayout->setSelectedTemplate('<span
class="current">{%page}</span>');
$pagerLayout->setSeparatorTemplate('&nbsp;');

// set view variables
$this->view->records = $result;
$this->view->pages = $pagerLayout->display(null, true);
} else {
    throw new Zend_Controller_Action_Exception('Invalid input');
}
}
```

注意，`Doctrine_Pager_Layout` 组件用于生成分页链接的 URL 模板也应该更新，以包含必要的排序参数，这样在页面之间切换时，排序准才就不会“丢失”。

最后一步是更新视图并包含用户对数据集不同字段进行排序的链接。以下是修改后的视图脚本：

```html
<h2>项目列表</h2>
<?php if (count($this->records)): ?>
  <div id="pager">
    Pages: <?php echo $this->pages; ?>
  </div>
  <div id="records">
    <form method="post" action="<?php echo $this->url(array(), 'admin-catalog-delete'); ?>">
      <table>
        <tr>
          <td></td>
          <td class="key">
            项目 ID
            <a href="<?php echo $this->url(array('sort' => 'RecordID', 'dir' => 'asc'), 'admin-catalog-index'); ?>">&uArr;</a>
            <a href="<?php echo $this->url(array('sort' => 'RecordID', 'dir' => 'desc'), 'admin-catalog-index'); ?>">&dArr;</a>
          </td>
          <td class="key">
            标题
            <a href="<?php echo $this->url(array('sort' => 'Title', 'dir' => 'asc'), 'admin-catalog-index'); ?>">&uArr;</a>
            <a href="<?php echo $this->url(array('sort' => 'Title', 'dir' => 'desc'), 'admin-catalog-index'); ?>">&dArr;</a>
          </td>
          <td class="key">
            面额
            <a href="<?php echo $this->url(array('sort' => 'Denomination', 'dir' => 'asc'), 'admin-catalog-index'); ?>">&uArr;</a>
            <a href="<?php echo $this->url(array('sort' => 'Denomination', 'dir' => 'desc'), 'admin-catalog-index'); ?>">&dArr;</a>
          </td>
          <td class="key">
            国家
            <a href="<?php echo $this->url(array('sort' => 'CountryID', 'dir' => 'asc'), 'admin-catalog-index'); ?>">&uArr;</a>
            <a href="<?php echo $this->url(array('sort' => 'CountryID', 'dir' => 'desc'), 'admin-catalog-index'); ?>">&dArr;</a>
          </td>
          <td class="key">
            等级
            <a href="<?php echo $this->url(array('sort' => 'GradeID', 'dir' => 'asc'), 'admin-catalog-index'); ?>">&uArr;</a>
            <a href="<?php echo $this->url(array('sort' => 'GradeID', 'dir' => 'desc'), 'admin-catalog-index'); ?>">&dArr;</a>
          </td>
          <td class="key">
            年份
            <a href="<?php echo $this->url(array('sort' => 'Year', 'dir' => 'asc'), 'admin-catalog-index'); ?>">&uArr;</a>
            <a href="<?php echo $this->url(array('sort' => 'Year', 'dir' => 'desc'), 'admin-catalog-index'); ?>">&dArr;</a>
          </td>
          <td></td>
          <td></td>
        </tr>
        <?php foreach ($this->records as $r): ?>
          <tr>
            <td><?php echo escape($r['RecordID']); ?></td>
            <td><?php echo escape($r['Title']); ?></td>
            ...
        <?php endforeach; ?>
        <tr>
          <td colspan="7">
            <input type="submit" name="submit" style="width:150px" value="删除选中" />
          </td>
          <td colspan="2">
            <a href="<?php echo $this->url(array(), 'admin-fulltext-index-create'); ?>">更新全文索引</a>
          </td>
        </tr>
      </table>
    </form>
  </div>
  <div id="pager">
    Pages: <?php echo $this->pages; ?>
  </div>
<?php else: ?>
  未找到记录
<?php endif; ?>
```

现在，当你重新访问 `http://square.localhost/admin/catalog/index` 时，你会发现可以升序或降序排序数据集。这种排序选择在切换页面时仍然保留。如果没有指定排序标准，默认路由将确保按项目 ID 升序排序。

图 7-2 显示按等级排序的输出（查看浏览器地址栏以更好地理解工作原理）。

**图 7-2 启用了排序和分页的目录视图**

207 第7章：分页、排序和数据上传

## 209 文件上传

在第3章中，你快速学习了如何使用 `Zend_Form` 创建和处理表单，后续章节通过将这些技术应用于不同类型的表单，进一步加深了对 `Zend_Form` 的理解。然而，有一个常见的需求尚未涉及：通过表单处理文件上传。

PHP 多年来一直支持通过表单上传文件，并提供了特殊的全局变量 `$_FILES` 以及内置方法（如 `is_uploaded_file()` 和 `move_uploaded_file()`），以协助安全高效地管理上传的文件。在 Zend Framework 中，可以通过 `Zend_File_Transfer` 组件获得类似的功能，它提供了完整的 API 来接收、验证和处理上传的文件。该组件也能无缝处理通过 `Zend_Form` 元素发起的文件。

> **注意**
>
> 虽然 PHP 原生支持 POST 和 PUT 文件上传，但 `Zend_File_Transfer` 组件目前仅支持 POST 上。

理解 `Zend_Form` 文件传输的最佳方式是通过示例。考虑以下代码，它设置了一个包含上传元素和提交按钮的简单表单：

```php
<?php
class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/sandbox/example/form')
            ->setMethod('post');

        // 创建照片上传的文件输入
        $photo = new Zend_Form_Element_File('photo');
        $photo->setLabel('照片:')
            ->setDestination('/tmp/upload');

        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit');
        $submit->setLabel('提交');

        // 将元素附加到表单
        $this->addElement($photo)
            ->addElement($submit);

        return $this;
    }
}
```

210 Zend Framework：学者指南

图 7-3 展示了该表单的样子。`setDestination()` 方法定义了上传文件的目标目录。注意，在 action 中初始化 `Zend_Form` 对象之前，该目录应该已经存在；如果不存在，对象将抛出异常。另一个好习惯是确保目标目录 Web 服务器可写，以避免在处理上传时出现任何意外失败。

当表单提交时，在 action 中调用其 `getValues()` 方法将自动接收并将文件传输到指定位置。示例如下：

```php
<?php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function formAction()
    {
        $form = new Form_Example;
        $this->view->form = $form;

        if ($this->getRequest()->isPost()) {
            if ($form->isValid($this->getRequest()->getPost())) {
                $values = $form->getValues();
                $this->_redirect('/form/success');
            }
        }
    }
}
```

**图 7-3 带有文件输入字段的表单**

## 第 7 章：数据的分页、排序与上传

211

### 表 7-1：Zend Framework 包含的文件上传验证器

| 验证器名称 | 描述 |
| :--- | :--- |
| Exists | 如果参数不是有效文件，则返回 false |
| Count | 如果上传的文件数量不在参数指定的范围内，则返回 false |
| Size | 如果上传文件的大小不在参数指定的范围内，则返回 false |
| FilesSize | 如果上传文件的总大小不在参数指定的范围内，则返回 false |
| Extension | 如果上传的文件扩展名与参数中指定的扩展名不匹配，则返回 false |
| MimeType | 如果上传的文件的 MIME 类型与参数中指定的 MIME 类型不匹配，则返回 false |
| IsCompressed | 如果上传的文件不是压缩包文件，则返回 false |
| IsImage | 如果上传的文件不是图像文件，则返回 false |
| ImageSize | 如果上传的图片尺寸不在参数指定的范围内，则返回 false |
| Crc32, Md5, Sha1, Hash | 如果上传的文件内容与参数中指定的哈希值不匹配，则返回 false（支持 crc32、md5 和 sha1 哈希算法） |
| ExcludeExtension | 如果上传的文件扩展名匹配参数中指定的扩展名，则返回 false |
| ExcludeMimeType | 如果上传的文件的 MIME 类型匹配参数中指定的 MIME 类型，则返回 false |
| WordCount | 如果上传文件中的单词数不在参数指定的范围内，则返回 false |

### 表 7-2：Zend Framework 包含的文件上传过滤器

| 过滤器名称 | 描述 |
| :--- | :--- |
| Encrypt | 加密上传文件的内容 |
| Decrypt | 解密上传文件的内容 |
| LowerCase | 将上传文件的内容转换为小写 |
| UpperCase | 将上传文件的内容转换为大写 |
| Rename | 重命名上传的文件 |

212

Zend Framework：初学者指南

使用验证器限制上传为 40KB 以下的 JPEG 图像，并将其重命名为唯一文件名。

```php
<?php

class Form_Example extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/sandbox/example/form')
            ->setMethod('post');

        // 创建照片上传的文件输入框
        $photo = new Zend_Form_Element_File('photo');
        $photo->setLabel('Photo:')
            ->setDestination('/tmp/upload')
            ->addFilter('Rename',
                sprintf('p-%s.jpg', uniqid(md5(time()), true)))
            ->addValidator('Extension', false, 'jpg')
            ->addValidator('MimeType', false, 'image/jpeg')
            ->addValidator('Size', false, 40000);

        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit');
        $submit->setLabel('Submit');

        // 将元素附加到表单
        $this->addElement($photo)
            ->addElement($submit);

        return $this;
    }
}
```

图 7-4 显示了尝试上传不符合指定约束的文件时看到的输出示例。

**图 7-4 上传无效文件的结果**

213

## 第 7 章：数据的分页、排序与上传

### 启用图片上传

有了这些背景信息，让我们考虑更新 SQUARE 示例应用程序，允许卖家为其目录条目添加最多三张照片。接下来的章节将讨论如何启用此功能。

#### 定义上传目标

第一步是为上传的图片定义一个目标。由于这些图片最终将显示在公共目录，因此必须能够通过未经认证的 URL 请求访问，所以将它们存储在 `$APP_DIR/public/*` 层次结构下是合理的。因此，按照如下方式创建 `$APP_DIR/public/uploads/`：

```shell
cd /usr/local/apache/htdocs/square/public
mkdir uploads
```



由于不同的控制器和操作都需要此信息，因此将其集中在应用程序配置文件中也是合理的。相应的，打开位于`$APP_DIR/application/configs/application.ini`的应用程序配置文件，并向其添加以下指令：

```
uploads.uploadPath = APPLICATION_PATH "/../public/uploads"
```

### 更新表单定义

下一步是更新用于创建新目录条目的表单，添加额外的文件上传元素。要实现这一点，请更新位于`$APP_DIR/library/Square/Form/ItemCreate.php`的表单定义，并对加粗显示的内容进行修改：

```php
<?php

class Square_Form_ItemCreate extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/catalog/item/create')
            ->setMethod('post');

        // -------------- //
        // 由于空间限制，元素定义已简略 //
        // 请参阅第 4 章或代码存档以获取
        // 完整的表单定义 //
        // ------------- //

        // 创建项目图片的文件输入
        $images = new Zend_Form_Element_File('images');
        $images->setMultiFile(3)
```

尝试练习 7-2

214

Zend Framework：初学者指南

```php
            ->addValidator('IsImage')
            ->addValidator('Size', false, '204800')
            ->addValidator('Extension', false, 'jpg,png,gif')
            ->addValidator('ImageSize', false, array(
                'minwidth' => 150,
                'minheight' => 150,
                'maxwidth' => 150,
                'maxheight' => 150
            ))
            ->setValueDisabled(true);

        // 将元素附加到表单
        $this->addElement($images);

        // 将元素附加到表单
        $this->addElement($submit);

        return $this;
    }
}
```

215

第 7 章：数据的分页、排序与上传

### 更新 Create Action

下一步是更新`Catalog_ItemController::createAction`以接收上传的图片，将其重命名为标准格式并保存到磁盘。为了实现这一点，请修改位于`$APP_DIR/application/modules/catalog/controllers/ItemController.php`的操作代码，并对加粗显示的内容进行修改：

```php
<?php

class Catalog_ItemController extends Zend_Controller_Action
{
    public function createAction()
    {
        // 生成输入表单
        $form = new Square_Form_ItemCreate;
        $this->view->form = $form;

        // 测试有效输入
        // 如果有效，填充模型
        // 为某些字段分配默认值
        // 保存到数据库
        if ($this->getRequest()->isPost()) {
            if ($form->isValid($this->getRequest()->getPost())) {
                $item = new Square_Model_Item;
                $item->fromArray($form->getValues());
                $item->RecordDate = date('Y-m-d', mktime());
                $item->DisplayStatus = 0;
                $item->DisplayUntil = null;
                $item->save();
                $id = $item->RecordID;

                $config = $this->getInvokeArg('bootstrap')->getOption('uploads');
                $form->images->setDestination($config['uploadPath']);
                $adapter = $form->images->getTransferAdapter();
                for($x=0; $x<$form->images->getMultiFile(); $x++) {
                    $xt = @pathinfo($adapter->getFileName('images_'.$x.'_'), PATHINFO_EXTENSION);
                    $adapter->clearFilters();
                    $adapter->addFilter('Rename', array(
                        'target' => sprintf('%d_%d.%s', $id, ($x+1), $xt),
                        'overwrite' => true
                    ));
                    $adapter->receive('images_'.$x.'_');
                }
            }
        }
    }
}
```

```php
$this->_helper->getHelper('FlashMessenger')->addMessage(
'您的提交已被接受，项目编号为 #' . $id . '. 管理员将审核项目，如果通过，它将在48 小时内显示在网站上。');

$this->_redirect('/catalog/item/success');

}

}
```

在这里，`Zend_Form_Element_File`对象的`getTransferAdapter()`方法返回`Zend_File_Transfer` HTTP 适配器的实例。该适配器作为接收、验证和处理多文件上传的控制点。它暴露了一个`receive()`方法，可以使用它手动接收多文件上传的各个元素。在每个文件上使用`Rename`过滤器可以确保这些文件使用特定的命名约定自动重命名，该约定在文件名中包含了条目的记录 ID 和文件序列 ID。重命名后的文件将保存到磁盘上，位于`Zend_Form_Element_File`对象的`setDestination()`方法指定的目录中。

**注意**

当您使用原始名称存储上传的文件时，请记住在用`receive()`方法接收文件之前对文件名进行验证。这样做是为了消除通过像`../etc/passwd`或`../index.php`这样的文件名注入到服务器文件系统的可能性，这在配置不当的服务器上显然会导致严重问题。

### 更新显示 Action 和视图

大部分实质性工作已经完成。下一步是更新`Catalog_ItemController::displayAction`，将上传的图像与条目的其他详情一起显示。以下是`displayAction()`方法修改后的代码。

```php
<?php

class Catalog_ItemController extends Zend_Controller_Action
{
    // 显示目录条目的 action
    public function displayAction()
    {
        // 为 GET 输入设置过滤器和验证器
        $filters = array(
            'id' => array('HtmlEntities', 'StripTags', 'StringTrim')
        );
        $validators = array(
            'id' => array('NotEmpty', 'Int')
        );

        $input = new Zend_Filter_Input($filters, $validators);
        $input->setData($this->getRequest()->getParams());

        // 测试输入是否有效
        // 获取请求记录
        // 附加到视图
        if ($input->isValid()) {
            $q = Doctrine_Query::create()
                ->from('Square_Model_Item i')
                ->leftJoin('i.Square_Model_Country c')
                ->leftJoin('i.Square_Model_Grade g')
                ->leftJoin('i.Square_Model_Type t')
                ->where('i.RecordID = ?', $input->id)
                ->addWhere('i.DisplayStatus = 1')
                ->addWhere('i.DisplayUntil >= CURDATE()');
            $result = $q->fetchArray();
            if (count($result) == 1) {
                $this->view->item = $result[0];
                $this->view->images = array();
                $config = $this->getInvokeArg('bootstrap')->getOption('uploads');
                foreach (glob("{$config['uploadPath']}/**{$this->view->item['RecordID']}_*") as $file) {
                    $this->view->images[] = basename($file);
                }
            } else {
                throw new Zend_Controller_Action_Exception('Page not found', 404);
            }
        } else {
            throw new Zend_Controller_Action_Exception('Invalid input');
        }
    }
}
```

额外的代码从应用程序配置文件读取上传目录的路径，使用 PHP 的`glob()`函数获取该目录下与项目 ID 对应的所有文件列表，然后将生成的文件列表作为数组发送到视图。视图脚本现在可以处理此数组并在画廊中显示图像，如下所示：

```html
<h2>查看项目</h2>
<h3>
待售：
<?php echo $this->escape($this->item['Title']); ?> -
<?php echo $this->escape($this->item['Year']); ?> -
<?php echo $this->escape($this->item['Square_Model_Grade']['GradeName']); ?>
</h3>
<div id="container">
    <div id="images">
        <?php foreach ($this->images as $image): ?>
            <img src="/uploads/<?php echo $this->escape($image); ?>" width="150" height="150" />
        <?php endforeach; ?>
    </div>
    <div id="record">
        <table>
            <tr>
                <td class="key">Title:</td>
                <td class="value">
                    <?php echo $this->escape($this->item['Title']); ?>
                </td>
            </tr>
            ...
            <tr>
                <td class="key">Description:</td>
                <td class="value">
                    <?php echo $this->escape($this->item['Description']); ?>
                </td>
            </tr>
        </table>
    </div>
</div>
```

同样地，您也应该更新`Catalog_AdminItemController::displayAction`和相应的视图脚本，以显示与每个条目相关的图像。您将在本章中找到必要的代码，这些代码可以从此书的配套网站 http://www.zf-beginners.com/ 下载。

### 更新删除 Action

最后，您还应该更新`Catalog_AdminItemController::deleteAction`，在删除条目时删除与每个条目相关的图像。您可以在以下代码中看到`Catalog_ItemController::deleteAction`的实现方式：



```php
<?php

class Catalog_AdminItemController extends Zend_Controller_Action
{
    // 删除条目的 action
    public function deleteAction()
    {
        // 为 GET 输入设置过滤器和验证器
        $filters = array(
            'id' => array('HtmlEntities', 'StripTags', 'StringTrim')
        );
        $validators = array(
            'id' => array('NotEmpty', 'Int')
        );

        $input = new Zend_Filter_Input($filters, $validators);
        $input->setData($this->getRequest()->getParams());

        // 测试输入是否有效
        // 获取请求记录
        // 附加到视图
        if ($input->isValid()) {
            $q = Doctrine_Query::create()
                ->from('Square_Model_Item i')
                ->leftJoin('i.Square_Model_Country c')
                ->leftJoin('i.Square_Model_Grade g')
                ->leftJoin('i.Square_Model_Type t')
                ->where('i.RecordID = ?', $input->id)
                ->addWhere('i.DisplayStatus = 1')
                ->addWhere('i.DisplayUntil >= CURDATE()');
            $result = $q->fetchArray();
            if (count($result) == 1) {
                $this->view->item = $result[0];
                $this->view->images = array();
                $config = $this->getInvokeArg('bootstrap')->getOption('uploads');
                foreach (glob("{$config['uploadPath']}/**{$this->view->item['RecordID']}_*") as $file) {
                    $this->view->images[] = basename($file);
                }
            } else {
                throw new Zend_Controller_Action_Exception('Page not found', 404);
            }
        } else {
            throw new Zend_Controller_Action_Exception('Invalid input');
        }
    }
}
```

为了看到所有功能，请尝试访问`http://square.localhost/item/create`添加新条目。如图 7-5 所示，表单现在显示额外的元素。输入一个或多个图像并提交。

## 处理配置数据

如之前所述，应用程序开发者必须定义应用程序的哪些方面是允许用户配置的。这些信息，即*配置数据*，应该存储在应用程序的数据存储中（可以是数据库、扁平文件或其他持久化形式），并在需要时由不同的组件访问。

`Zend Framework`通过其`Zend_Config`组件让处理配置文件的任务变得简单了一些。该组件提供了功能齐全 API 来读写配置文件，并采用了基于适配器的方法。在编写期间，该组件带有 INI 和 XML 格式的适配器，为其他自定义格式编写新适配器也相当容易。

通过几个示例说明`Zend_Config`工作原理的最佳方法。后续章节将帮助入门。

### 读取配置文件

`Zend_Config`可读取并解析以 XML 或 INI 格式表示的配置文件。为了说明其工作原理，假设您有一个名为*example.ini*的 INI 配置文件，内容如下：

```ini
[object]
shape = 'square'
size = '10'
color = 'red'
typeface.name = 'Mono'
typeface.size = 19
typeface.units = 'px'
typeface.color = 'white'
```

这些数据可以读取到`Zend_Config`对象中，然后可以使用标准的对象表示访问各个配置变量。这里有一个示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function configAction()
    {
        // 初始化配置对象
        $config = new Zend_Config_Ini(APPLICATION_PATH . "/configs/example.ini");

        // 设置 $view->a 为 'square'
        $this->view->a = $config->object->shape;
    }
}
```

```php
// 将 $view->b 设置为 'white'
$this->view->b = $config->object->typeface->color;
```

***注意***

默认情况下，表示在`Zend_Config`对象中的配置数据是只读的，任何修改尝试都将产生异常。要允许修改，请将一个额外的选项数组作为第三参数传递给`Zend_Config`对象，并将`allowModifications`键指定为`true`。关于此点的更多信息可以参考本章末尾的链接。

还有一个`Zend_Config_Xml`适配器专门用于处理 XML 编码的配置数据。考虑以下 XML 文件：

```xml
<?xml version="1.0"?>
<configuration>
  <application>
    <name>SomeApp</name>
    <version>2.3</version>
    <window>
      <height>600</height>
      <width>500</width>
      <titlebar>
        <title>Export Data</title>
        <foreColor>#ffffff</foreColor>
        <backColor>#0000ff</backColor>
      </titlebar>
    </window>
  </application>
</configuration>
```

以下是一个使用`Zend_Config_Xml`适配器读取该文件并从内部访问配置值的示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function configAction()
    {
        // 初始化配置对象
        $config = new Zend_Config_Xml(APPLICATION_PATH . "/configs/example.xml");

        // 将 $view->a 设置为 '2.3'
        $this->view->a = $config->application->version;

        // 将 $view->b 设置为 'Export Data'
        $this->view->b = $config->application->window->titlebar->title;
    }
}
```

## 写入配置文件

读取文件已经处理好了，但写入文件呢？`Zend_Config`包含一个写入组件`Zend_Config_Writer`，可以用于创建 PHP、XML 或 INI 格式的配置文件。配置数据可以分层排列或分节排列，以提高可读性。

以下是一个说明如何使用`Zend_Config_Writer`生成 INI 格式配置文件的示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function configAction()
    {
        // 创建配置对象
        $config = new Zend_Config(array(), 1);

        // 创建节
        $config->blog = array();
        $config->blog->allowComments = 'yes';
        $config->blog->displayComments = 'yes';
        $config->blog->allowTrackbacks = 'yes';
        $config->blog->defaultAuthor = 'Jack Frost';
        $config->blog->numPostsOnIndexPage = 5;

        // 创建节
        $config->calendar = array();
        $config->calendar->weekStartsOn = 'Monday';
        $config->calendar->highlightToday = 1;

        // 创建子节
        $config->calendar->events = array();
        $config->calendar->events->displayTitle = 1;
        $config->calendar->events->displayStartTime = 1;
        $config->calendar->events->displayEndTime = 0;
        $config->calendar->events->displayLocation = 1;

        // 将数据写入文件
        $writer = new Zend_Config_Writer_Ini();
        $writer->write(APPLICATION_PATH . "/configs/example.ini", $config);
    }
}
```

第一步是初始化一个`Zend_Config`对象，该对象表示配置数据。此对象应使用一个包含配置数据的数组（如果不存在此类数据，则使用空数组）进行初始化，并带有一个布尔参数指示配置数据是否可以修改。一旦初始化了`Zend_Config`对象，可以使用标准的对象表示法将单个配置变量设置为对象属性。它支持分级数据结构，只需链式调用属性；取决于所选择的输出格式，这种分级结构通过分隔符（INI）或嵌套（XML）表示。

由上述代码生成的配置文件如下：

```ini
[blog]
allowComments = "yes"
displayComments = "yes"
allowTrackbacks = "yes"
defaultAuthor = "Jack Frost"
numPostsOnIndexPage = 5

[calendar]
weekStartsOn = "Monday"
highlightToday = 1
events.displayTitle = 1
events.displayStartTime = 1
events.displayEndTime = 0
events.displayLocation = 1
```

XML 配置文件在 Web 应用程序中非常流行，因为大多数语言都包含了 XML 解析支持（特别是 PHP，带有许多用于 XML 数据解析的扩展，包括 SimpleXML、DOM 和 XMLReader 扩展）。要以 XML 格式呈现相同的配置数据，只需更新操作代码以使用`Zend_Config_Writer_Xml`适配器，如下：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function configAction()
    {
        // 创建配置对象
        $config = new Zend_Config(array(), 1);

        // 创建节
        $config->blog = array();
        $config->blog->allowComments = 'yes';
        $config->blog->displayComments = 'yes';
        $config->blog->allowTrackbacks = 'yes';
        $config->blog->defaultAuthor = 'Jack Frost';
        $config->blog->numPostsOnIndexPage = 5;

        // 创建节
        $config->calendar = array();
        $config->calendar->weekStartsOn = 'Monday';
        $config->calendar->highlightToday = 1;

        // 创建子节
        $config->calendar->events = array();
        $config->calendar->events->displayTitle = 1;
        $config->calendar->events->displayStartTime = 1;
        $config->calendar->events->displayEndTime = 0;
        $config->calendar->events->displayLocation = 1;

        // 将数据写入文件
        $writer = new Zend_Config_Writer_Xml();
        $writer->write(APPLICATION_PATH . "/configs/example.xml", $config);
    }
}
```

生成的 XML 配置文件内容如下：

```xml
<?xml version="1.0"?>
<config>
  <blog>
    <allowComments>yes</allowComments>
    <displayComments>yes</displayComments>
    <allowTrackbacks>yes</allowTrackbacks>
    <defaultAuthor>Jack Frost</defaultAuthor>
    <numPostsOnIndexPage>5</numPostsOnIndexPage>
  </blog>
  <calendar>
    <weekStartsOn>Monday</weekStartsOn>
    <highlightToday>1</highlightToday>
    <events>
      <displayTitle>1</displayTitle>
      <displayStartTime>1</displayStartTime>
      <displayEndTime>0</displayEndTime>
      <displayLocation>1</displayLocation>
    </events>
  </calendar>
</config>
```

某些情况下，你可能倾向于将配置数据存储为原生数组，如下所示：

```php
<?php

return array (
  'blog' => array (
    'allowComments' => 'yes',
    'displayComments' => 'yes',
    'allowTrackbacks' => 'yes',
    'defaultAuthor' => 'Jack Frost',
    'numPostsOnIndexPage' => 5
  ),
  'calendar' => array (
    'weekStartsOn' => 'Monday',
```



`'highlightToday' => 1`,

`'events' => array (`  
`'displayTitle' => 1`,  
`'displayStartTime' => 1`,  
`'displayEndTime' => 0`,  
`'displayLocation' => 1`  
`)`  
`)`  
`);`

**提示**：使用原生数组表示配置具有性能优势，因为这种数据可以通过 APC 进行缓存；INI 和 XML 配置文件无法以这种方式缓存。

## 配置设置

现在了解了 `Zend_Config` 的基础知识，让我们看看如何在实际场景中使用它，通过创建一个配置面板。接下来的章节将引导你完成此过程。

### 定义配置表单

第一步是定义配置表单。通常你需要在对应用程序进行分析后确定哪些方面需要配置。在这种情况下，让我们假设以下方面是可配置的：

- 通过联系表单发送的电子邮件地址
- 公共目录中卖家名称和地址
- 异常记录到文件

这是对应的表单定义，应保存至 `$APP_DIR/library/Square/Form/Configure.php`：

```php
<?php

class Square_Form_Configure extends Zend_Form

{

    public function init()

    {

        // 初始化表单

        $this->setAction('/admin/config')

            ->setMethod('post');

        // 创建默认电子邮件的文本框

        $default = new Zend_Form_Element_Text('defaultEmailAddress');

        $default->setLabel('所有操作的备用电子邮件地址:')

            ->setOptions(array('size' => '40'))

            ->setRequired(true)

            ->addValidator('EmailAddress')

            ->addFilter('HtmlEntities')

            ->addFilter('StringTrim');

        $this->add($default);

        // 创建销售电子邮件的文本框

        $sales = new Zend_Form_Element_Text('salesEmailAddress');

        $sales->setLabel('销售咨询默认电子邮件地址:')

            ->setOptions(array('size' => '40'))

            ->setRequired(true)

            ->addValidator('EmailAddress')

            ->addFilter('HtmlEntities')

            ->addFilter('StringTrim');

        $this->add($sales);

        // 创建管理摘要中每页项目数量的文本框

        $items = new Zend_Form_Element_Text('itemsPerPage');

        $items->setLabel('管理视图中每页项目数量:')

            ->setOptions(array('size' => '4'))

            ->setRequired(true)

            ->addValidator('Int');

        $this->add($items);

    }

}
```

## 第 7 章：分页、排序与数据上传

`->addFilter('HtmlEntities')`  
`->addFilter('StringTrim')`；

// 创建用于显示卖家名称和地址的单选按钮

`$seller = new Zend_Form_Element_Radio('displaySellerInfo')`；  
`$seller->setLabel('公共目录中显示卖家名称和地址：')`  
`->setRequired(true)`  
`->setMultiOptions(array(`  
`'1' => '是',`  
`'0' => '否'`  
`))`；

// 创建用于异常日志的单选按钮

`$log = new Zend_Form_Element_Radio('logExceptionsToFile')`；  
`$log->setLabel('记录到文件的异常：')`  
`->setRequired(true)`  
`->setMultiOptions(array(`  
`'1' => '是',`  
`'0' => '否'`  
`))`；

// 创建提交按钮

`$submit = new Zend_Form_Element_Submit('submit')`；  
`$submit->setLabel('保存配置')`  
`->setOptions(array('class' => 'submit'))`；

// 将元素附加到表单

`$this->addElement($sales)`  
`->addElement($default)`  
`->addElement($items)`  
`->addElement($seller)`  
`->addElement($log)`  
`->addElement($submit)`；  
`}`  
`}`

### 定义配置文件

下一步是定义用于存储用户级配置设置的文件。Zend Framework 建议将所有配置数据放在 `$APP_DIR/application/configs/` 目录下，因此让我们使用该目录。打开位于 `$APP_DIR/application/configs/application.ini` 的主应用配置文件，并向其中添加以下指令以定义用户级配置文件的位置：

`configs.localConfigPath = APPLICATION_PATH "/configs/square.ini"`

## 定义自定义路由

下一步是定义通往配置控制器的路由。由于配置面板不特定于任何特定模块，因此该控制器可以放置在通用的“default（默认）”模块中。以下是路由定义，应将其添加到 `$APP_DIR/application/configs/application.ini` 的应用配置文件中：

```ini
resources.router.routes.admin-config.route = /admin/config

resources.router.routes.admin-config.defaults.module = default

resources.router.routes.admin-config.defaults.controller = config

resources.router.routes.admin-config.defaults.action = index

resources.router.routes.admin-config-success.route = /admin/config/success

resources.router.routes.admin-config-success.defaults.module = default

resources.router.routes.admin-config-success.defaults.controller = config

resources.router.routes.admin-config-success.defaults.action = success
```

**问：我我很困惑。为什么要将一个配置文件的位置存储在另一个文件中？**

**答：** 位于 `$APP_DIR/application/configs/application.ini` 的应用配置文件是一个被 Zend Framework 应用读取的全局文件。通常，它包含了许多由应用设计人员定义的设置，在没有深思考虑的情况下不应修改。尽管如此，每个应用程序都有各种用户级设置，这些设置应该允许应用程序用户和/或管理员进行配置。对于 SQUARE 应用，这些设置存储在独立的用户级配置文件中，位于 `$APP_DIR/application/configs/square.ini`。

通常推荐这种方式将系统级设置与用户级设置分离，因为这允许两种类型的变量独立地进行操作，而没有损坏的风险。然而，两者之间也需要一个链接，以便依赖用户级设置的操作和控制器知道去哪里寻找这些信息。由于应用配置文件 `application.ini` 对所有操作和控制器都是全局可用的，因此用户级配置文件 `square.ini` 的路径可以方便地存储在其中。

如果你仍然困惑，这里有另一种理解方式：`application.ini` 全局配置的更改可能也需要修改应用程序代码，但用户级配置文件的更改绝不应该产生这种影响。

## 定义控制器和视图

下一步是为配置界面定义动作（action）和视图（view）。以下是 `ConfigController` 的代码，应保存为 `$APP_DIR/application/modules/default/controllers/ConfigController.php`：

```php
<?php

class ConfigController extends Zend_Controller_Action

{

    protected $localConfigPath;

    public function init()

    {

        // 设置 doctype

        $this->view->doctype('XHTML1_STRICT');

        // 获取本地配置文件的路径

        $config = $this->getInvokeArg('bootstrap')->getOption('configs');

        $this->localConfigPath = $config['localConfigPath'];

    }

    // 处理 admin URL 的动作

    public function preDispatch()

    {

        // 设置 admin 布局

        // 检查用户是否已认证

        // 如果未认证，重定向到登录页面

        $url = $this->getRequest()->getRequestUri();

        $this->_helper->layout->setLayout('admin');

        if (!Zend_Auth::getInstance()->hasIdentity()) {

            $session = new Zend_Session_Namespace('square.auth');

            $session->requestURL = $url;

            $this->_redirect('/admin/login');

        }

    }

    // 保存配置数据的动作

    public function indexAction()

    {

        // 生成输入表单

        $form = new Square_Form_Configure();

        $this->view->form = $form;

        // 如果配置存在

        // 读取配置

        // 用值填充表单

        if (file_exists($this->localConfigPath)) {

            $config = new Zend_Config_Ini($this->localConfigPath);

            $data['defaultAddress'] = $config->global;

            $data['salesAddress'] = $config->user;

            $data['itemsPerPage'] = $config->admin;

            $data['displayInfo'] = $config->user;

            $form->populate($data);

        }

        // 测试输入

        // 如果是 POST 请求

        if ($this->getRequest()->isPost()) {

            if ($form->isValid()) {

                // 如果有效，创建新配置对象

                // 创建配置

                $values = $form->getValues();

                $config = new Zend_Config(array(), true);

                $config->global = array();

                $config->user = array();

                $config->admin = array();

                // 将配置写入文件

                // 覆盖旧版本

                $config->global->defaultAddress = $values['defaultAddress'];

                $config->user->salesAddress = $values['salesAddress'];

                $config->admin->itemsPerPage = $values['itemsPerPage'];

                $config->user->displayInfo = $values['displayInfo'];

                $writer = new Zend_Config_Writer();

                $writer->write($this->localConfigPath, $config);

                $this->_helper->FlashMessenger()->addMessage('感谢。配置已保存。');

                $this->_redirect('/config/success');

            }

        }

    }

    // 成功动作

    public function successAction()

    {

        if ($this->_helper->FlashMessenger()->getMessages()) {

            $this->view->messages = $this->_helper->FlashMessenger()->getMessages();

        } else {

            $this->_redirect('/');

        }

    }

}
```

该控制器的主要工作是 `indexAction()` 方法，它负责验证接收到的输入并使用 `Zend_Config_Writer` 配置数据。在初始化配置表单时，`indexAction()` 方法使用 Zend 组件读取配置（如果可用），然后用当前设置填充表单。

## 更新主布局

剩下的工作是更新 `$APP_DIR/application/layouts/admin.phtml` 中的管理布局，以便在用户登录后主菜单中显示“设置”项。布局的修订在以下示例中加粗显示：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">

...

<div id="menu">

<?php if (Zend_Auth::getInstance()->hasIdentity()): ?>

    <a href="<?php echo $this->url(array(), 'admin-catalog-index'); ?>">目录</a>

    **<a href="<?php echo $this->url(array(), 'admin-config'); ?>">设置</a>**

    <a href="<?php echo $this->url(array(), 'logout'); ?>">退出</a>

<?php else: ?>

    <a href="<?php echo $this->url(array(), 'login'); ?>">登录</a>

<?php endif; ?>

</div>

...

</html>
```



# Zend Framework：入门指南

你现在可以通过登录应用程序的管理面板，并浏览到 URL `http://square.localhost/admin/config` 来尝试此操作。图 7-9 展示了你应该看到的配置表单。

在此配置表单中输入值并提交。数据现在应该已经被保存到文件 `$APP_DIR/application/configs/square.ini` 中。查看此文件，你应该能看到 INI 格式的数据，如图 7-10 所示。

如果你现在再次访问 URL `http://square.localhost/admin/config`，你会发现配置表单已自动填充了之前保存的设置。图 7-11 显示了输出结果。

**图 7-9** SQUARE 应用配置表单

**图 7-10** INI 格式的示例配置数据

![](img/222e7e58871b088cc6397852e1452b57_252_0.png)

## 第 7 章：数据的分页、排序与上传

### 使用配置数据

成功地读取和写入配置数据只是赢得了一半战斗——你仍然需要利用这些数据来告知特定控制器和操作的行为。例如，考虑 `ContactController::indexAction` 现在应该被修改为读取用户级别的配置文件，并将其电子邮件消息发送到该文件中指定的销售地址。以下是修改后的 `ContactController::indexAction`：

```php
<?php

class ContactController extends Zend_Controller_Action

{

    public function indexAction()

    {

        $form = new Square_Form_Contact();

        $this->view->form = $form;

        if ($this->getRequest()->isPost()) {

            if ($form->isValid($this->getRequest()->getPost())) {

                $values = $form->getValues();

                $configs = $this->getInvokeArg('bootstrap')->getOption('configs');

                $localConfig = new Zend_Config_Ini($opt['localConfigPath']);

                $to = (!empty($localConfig->user->salesEmailAddress)) ?

                    $localConfig->user->salesEmailAddress :

                    $localConfig->global->defaultEmailAddress;

                $mail = new Zend_Mail();

                $mail->setBodyText($values['message']);

                $mail->setFrom($values['email'], $values['name']);

                $mail->addTo($to);

                $mail->setSubject('Contact form submission');

                $mail->send();

                $this->_helper->getHelper('FlashMessenger')->addMessage(

                    'Thank you. Your message was successfully sent.');

                $this->_redirect('/contact/success');

            }

        }

    }

}
```

**图 7-11** SQUARE 应用配置表单，已填充当前设置（继续）

同样地，`Catalog_ItemController::displayAction` 应该更新以检查公共目录中是否应该显示卖家信息，并据此显示这些信息。以下是修改后的 `Catalog_ItemController::displayAction`，它在读取用户级别配置文件后为视图设置了一个标志：

```php
<?php

class Catalog_ItemController extends Zend_Controller_Action

{

    // 显示目录项的动作

    public function displayAction()

    {

        // 为 GET 输入设置过滤器和验证器

        $filters = array(

            'id' => array('HtmlEntities', 'StripTags', 'StringTrim')

        );

        $validators = array(

            'id' => array('NotEmpty', 'Int')

        );

        $input = new Zend_Filter_Input($filters, $validators);

        $input->setData($this->getRequest()->getParams());

        // 测试输入是否有效

        // 获取记录

        // 挂载到视图

        if ($input->isValid()) {

            $q = Doctrine_Query::create()

                ->from('Square_Model_Item i')

                ->leftJoin('Square_Model_Country c')

                ->leftJoin('Square_Model_Grade g')

                ->leftJoin('Square_Model_Type t')

                ->where('i.RecordID = ?', $input->id)

                ->addWhere('i.DisplayStatus = 1')

                ->addWhere('i.DisplayUntil >= CURDATE()');

            $result = $q->fetchArray();

            if (count($result) == 1) {

                $this->view->item = $result[0];

                $this->view->images = array();

                $config = $this->getInvokeArg('bootstrap')->getOption('uploads');

                foreach (glob("{$config['uploadPath']}/{$this->view->item['RecordID']}_") as $file) {

                    $this->view->images[] = basename($file);

                }

                $configs = $this->getInvokeArg('bootstrap')->getOption('configs');

                $localConfig = new Zend_Config_Ini($configs['localConfigPath']);

                $this->view->seller = $localConfig->user->displayInfo;

            } else {

                throw new Zend_Controller_Exception('Page not found', 404);

            }

        } else {

            throw new Zend_Controller_Exception('Invalid input');

        }

    }

}
```

以下是对应的视图，它使用控制器设置的标志来决定输出中是否包含卖家信息：

## 项目

### 销售

```php
<?php echo $this->escape($this->item['Title']); ?> - <?php echo $this->escape($this->item['Year']); ?>

<div id="container">
    <div id="images">
        <?php foreach ($this->images as $image): ?>
            <img src="/uploads/<?php echo $this->escape($image); ?>" width="150" height="150" />
        <?php endforeach; ?>
    </div>
    <div id="record">
        <table>
            <tr>
                <td class="key">Title</td>
                <td><?php echo $this->escape($this->item['Title']); ?></td>
            </tr>
            <tr>
                <td class="key">Description</td>
                <td><?php echo $this->escape($this->item['Description']); ?></td>
            </tr>
            <?php if ($this->seller): ?>
                <tr>
                    <td class="key">Seller</td>
                    <td><?php echo $this->escape($this->item['SellerAddress']); ?></td>
                </tr>
            <?php endif; ?>
        </table>
    </div>
</div>
```

如果你有许多控制器和操作读取同一个用户配置文件，可以通过让应用程序引导程序自动读取该文件到本地注册表中来减少代码重复。该注册表可以通过 `Zend_Application_Bootstrap` 类的 `getResource()` 方法进行访问。在内部，注册表表示为 `Zend_Registry` 组件的实例，它为全局对象或变量提供了应用程序级区域。关于引导程序和 `Zend_Registry` 组件的更多信息可以通过本章末尾的链接获得，你将在后续章节发现许多使用 `Zend_Registry` 的示例。

### 总结

本章介绍了三个对你来说全新的组件：`Doctrine_Pager` 组件提供了大型数据库结果集的分页框架；`Zend_File_Transfer` 组件提供了处理 Web 表单上传文件的全功能 API；以及 `Zend_Config` 组件处理不同格式的配置数据。所有组件都通过 SQUARE 示例应用程序进行了说明，该程序现在具有分页和排序功能、配置面板以及图像上传系统。

要了解更多本章讨论的主题，可以参考以下链接：

- `Doctrine_Pager`：https://www.doctrine-project.org/documentation/manual/1_1/en/utilities#pagination:working-with-pager
- `Zend_Paginator` 组件：https://framework.zend.com/manual/en/zend/paginator.html
- `Zend_File_Transfer` 组件：https://framework.zend.com/manual/en/zend/file.html
- `Zend_File_Transfer` 组件的过滤器和验证器：https://framework.zend.com/manual/en/zend/file_transfer.filters.html 和 https://framework.zend.com/manual/en/zend/file_transfer.validators.html
- `Zend_Config` 组件：https://framework.zend.com/manual/en/zend/config.html
- `Zend_Registry` 组件：https://framework.zend.com/manual/en/zend/registry.html

---

## 第 8 章：日志记录与调试

### 异常

**关键技能与概念**

- 学习 PHP 5.x 异常模型
- 了解 Zend Framework 应用中是如何处理异常的
- 将自定义异常类与默认的 Zend Framework 错误处理器集成
- 控制生产环境中错误信息的可见性
- 通过将异常记录到文件或数据库来维护异常的持久化记录
- 使用额外的调试信息增强日志消息
- 使用 Firebug 控制台调试器实时跟踪异常

一个常见的误区（尤其是对于经验较少的开发人员而言）是，认为一个“良好”的程序是不带错误运行的程序。事实上，这并不完全准确：一个更好的定义可能是，一个良好的程序是能够预判所有可能的错误情况，并以一致的方式处理它们的程序。

编写符合这一定义的“智能”程序既是一门艺术，也是一门科学。经验和想象力在评估潜在原因和定义纠正措施方面起着重要作用，但同样重要的还有编程框架本身，它定义了可用于捕获和解决错误的工具和函数。

通过使用 Zend Framework 开发应用程序，错误处理的担忧比许多其他框架要少。Zend Framework 提供的默认错误处理器可以处理大多数常见情况，而且还有许多其他组件（例如 `Zend_Log` 和 `Zend_Debug`），可以为开发者和管理员提供额外信息。本章将向你介绍所有这些工具，并解释如何在实际场景中使用它们。

### 理解异常

PHP 5.x 引入了一种新的异常模型，类似于 Java 和 Python 等其他编程语言使用的模型。在这种基于异常的方法中，程序代码被封装在 `try` 块中，生成的异常由一个或多个 `catch` 块“捕获”并解决。由于存在多个 `catch` 块，开发人员可以捕获不同类型的异常并对每个类型进行不同的处理。

为了说明其工作原理，请考虑以下列表，它尝试使用 `ArrayIterator` 访问不存在的数组元素：

```php
<?php

// 定义数组

$cities = array(

    'London',

    'Washington',

    'Paris',

    'Delhi'

);

// 尝试访问不存在的数组元素

// 生成 OutOfBoundsException

try {

    $iterator = new ArrayIterator($cities);

    $iterator->seek(10);

} catch (Exception $e) {

    echo "ERROR: Something went wrong!\n";

    echo "Error message: " . $e->getMessage() . "\n";

    echo "Error code: " . $e->getCode() . "\n";

    echo "File name: " . $e->getFile() . "\n";

    echo "Line: " . $e->getLine() . "\n";

    echo "Backtrace: " . $e->getTraceAsString() . "\n";

}
```



当 PHP 遇到封装在 `try-catch` 块中的代码时，它首先尝试执行 `try` 块中的代码。如果这些代码处理过程中没有生成任何异常，控制权将转移到 `try-catch` 块之后的行。然而，

**Q：我看到未捕获的异常会产生致命错误导致脚本意外终止。我可以更改这一点吗？**

**A：** 既可以也可以行。PHP 提供了 `set_exception_handler()` 函数，它允许你用自己的自定义代码替换 PHP 的默认异常处理器，就像 `set_error_handler()` 所做的那样。但是，这里有一个重要的需要注意。PHP 的默认异常处理器会显示一个通知然后终止脚本异常。使用自定义异常处理器对这种行为有有限的控制：虽然你可以更改通知显示的方式和外观，但你无法让脚本在生成异常点之后继续执行。

#### 专家问答

244

如果在运行 `try` 块中的代码时生成了异常（如前面的列表所示），PHP 会在该处停止该块的执行，并开始检查每个 `catch` 块以查看是否有处理该异常的处理器。如果找到了处理器，将执行相应 `catch` 块中的代码，然后执行 `try` 块之后的行；如果没有找到，则会生成一个致命错误，脚本执行在错误点停止。

每个 `Exception` 对象都包含一些用于调试错误源的额外信息。这些信息可以通过 `Exception` 对象的内置方法访问，并在描述性错误消息、错误代码、发生错误的文件名和行号，以及通往错误的函数调用回溯（backtrace）。表 8-1 列出了这些方法。

一种更高级的方法是为通用 `Exception` 对象子类，并为每种可能的错误创建特定的 `Exception` 对象。当你需要区别处理类型的异常时，这种方法非常有用，因为它允许你为每个异常类型使用独立的 `catch` 块（以及独立的处理代码）。以下是前面示例的修订版本，说明了这种方法：

```php
<?php

// 子类 Exception

class MissingFileException extends Exception {}

class DuplicateFileException extends Exception {}

class FileIOException extends Exception {}

// 设置文件名

// 尝试复制并删除文件

$file = 'dummy.txt';

try {

    if (!file_exists($file)) {

        throw new MissingFileException($file);

    }

    if (!copy($file, "$file.new")) {

        throw new DuplicateFileException($file);

    }

    if (!unlink($file)) {

        throw new FileIOException($file);

    }

} catch (MissingFileException $e) {

    echo 'ERROR: Could not find file ' . $e->getMessage() . '\';

    exit();

} catch (DuplicateFileException $e) {

    echo 'ERROR: Destination file ' . $e->getMessage() . ' already exists';

    exit();

} catch (FileIOException $e) {

    echo 'ERROR: Could not perform input/output operation on file ' . $e->getMessage() . '\';

    exit();

} catch (Exception $e) {

    echo 'ERROR: Something bad happened on line ' . $e->getLine() . ': ' . $e->getMessage();

    exit();

}

echo 'SUCCESS: File operation successful.';

?>
```

表 8-1 Exception 对象的方法

| 方法名 | 描述 |
| :--- | :--- |
| `getMessage()` | 返回描述发生了什么错误的消息 |
| `getCode()` | 返回数值错误代码 |
| `getFile()` | 返回生成异常的脚本路径和名称 |
| `getLine()` | 返回生成异常的行号 |
| `getTrace()` | 以数组形式返回通往错误的调用回溯 |
| `getTraceAsString()` | 以字符串形式返回通往错误的调用回溯 |

此脚本扩展了基 `Exception` 类以创建三种异常类型，每种代表一种不同的错误。现在为每个异常使用单独 `catch` 块可以自定义处理这些异常的方式。最后一个 `catch` 块是一个通用的“捕获所有”处理器：未被上方块处理的异常将传递到并由此处理器处理。

基于异常的方法具有许多优点：

如果没有异常处理，则需要检查每个调用函数的返回值以识别是否发生了错误并采取纠正措施。这会产生不必要的复杂代码和深度嵌套块。在基于异常的模型中，可以使用单个 `catch` 块来捕获在该代码块中发生的任何错误。这消除了多次级联错误测试的需要，并产生了更简单、易读的代码。

245

日志记录与调试异常

由于异常模型使用了基于对象的方法，开发人员可以使用 OOP 的继承和扩展概念，对基 `Exception` 对象进行子类化并创建针对不同类型的异常使用不同的 `Exception` 对象。这使得区分不同类型的错误并对每种类型进行不同的处理成为可能。

基于异常的方法迫使开发者对如何处理不同类型的错误做出艰难的决定。在没有异常的情况下，开发者可以轻松地（无意或设计如此）省略检查函数返回值的测试。然而，异常并不那么容易被忽略。通过要求开发者创建并填充捕获块（`catch` blocks），异常模型迫使他们思考错误的原因和后果，最终导致更优的设计和更健壮的实现。

所有 Zend Framework 组件都显式地设计为默认使用异常模型，每个组件都根据需要扩展基类 `Zend_Exception` 类。因此，无论您是将 Zend Framework 组件作为大型应用程序的独立部分使用，还是在 Zend Framework MVC 应用的上下文中使用，这种方法的一致性都可以显著减少开发应用级错误处理功能的时间。

## 理解默认错误处理流程

现在让我们更仔细地观察 Zend Framework MVC 应用中的异常处理。默认情况下，每当动作（action）抛出异常时，该异常就会在执行链中“向上冒泡”，直到到达前端控制器（front controller）。前端控制器包含一个错误处理器插件（在引导过程中自动注册），该插件负责将异常转发到应用程序的默认错误控制器。然后，错误控制器检查异常类型并向请求的客户端显示适当的错误视图。

这个错误控制器是从哪里来的？对于使用 `zf` 命令行脚本创建的项目，它会自动包含在默认的项目布局中。对于手动创建的项目，必须手动生成。在何种情况下，它都表示为一个独立的控制器和动作 `ErrorController::errorAction`，并位于应用程序的“default”模块中。

以下是其典型样子的示例：

```php
class ErrorController extends Zend_Controller_Action

{

    public function errorAction()

    {

        $errors = $this->_getParam('error_handler');

        switch ($errors->type) {

            case Zend_Controller_Plugin_ErrorHandler::EXCEPTION_NO_CONTROLLER:

            case Zend_Controller_Plugin_ErrorHandler::EXCEPTION_NO_ACTION:

                // 404错误 -- 未找到控制器或动作

                $this->getResponse()->setHttpResponseCode(404);

                $this->view->message = 'Page not found';

                break;

            default:

                // 应用错误

                $this->getResponse()->setHttpResponseCode(500);

                $this->view->message = 'Application error';

                break;

        }

        $this->view->exception = $errors->exception;

        $this->view->request = $errors->request;

    }

}
```

此默认错误控制器设计用于处理两种情况：无效的 HTTP 请求和动作代码生成的异常。它对前者通过 404 错误码响应，对后者通过 500 错误码响应。为了看到这种效果，请考虑以下示例：

```php
class Sandbox_ExampleController extends Zend_Controller_Action

{

    public function failAction()

    {

        // 尝试访问不存在的数组元素

        // 生成 OutOfBoundsException

        $cities = array(

            'London',

            'Washington',

            'Paris',

            'Delhi'

        );

        $iterator = new ArrayIterator($cities);

        $iterator->seek(10);

    }

}
```

在这种情况下，对该动作的任何请求将导致异常，该异常将通过执行链传播，直到到达 `ErrorController::errorAction`。此动作将检查异常类型，并通过将服务器响应码设置为 500（内部服务器错误）然后渲染错误视图来响应。图 8-1 显示了由上述代码列表生成的错误视图示例。

如果您尝试访问不存在的控制器或动作，您将收到一个 404（页面未找到）错误。图 8-2 显示了一个示例。

注意，除了错误消息外，默认视图还包含导致异常的内部请求的堆栈跟踪（stack trace）以及原始 HTTP 请求包含的参数列表。当您尝试识别错误源时，这些是有用信息。

***提示***
默认错误控制器的行为符合大多数 Zend Framework 应用的需求——在大多数情况下，对应用级异常返回 500 响应以及对无效请求返回 404 响应是符合标准的预期行为——因此您通常不需要对其进行修改。但是，如果您的应用程序使用了自定义异常类，您可能想要修改默认处理器，并根据异常类型切换到不同的处理程序。这将在下一节中进行探讨。

图 8-1
应用程序抛出的内部错误的结果

图 8-2
请求无效或缺失的应用资源的结果

如果您想禁用默认错误控制器并让 PHP 以默认方式处理异常，请更新您的应用程序配置文件以包含以下指令：

`resources.frontController.throwExceptions = 1`

通过此更改，捕获和本地解决异常的责任现在交给了开发者。图 8-3 有一个关于禁用默认处理器时异常行为的示例。

## 使用异常类

如果您的应用程序使用了自定义类，那么修改默认控制器并为不同类型添加特定处理通常是有意义的。为了说明这是如何工作的，请考虑上述代码的以下变体，它根据文件是否存在来抛出自定义异常：

```php
class Sandbox_ExampleController extends Zend_Controller_Action

{

    public function failAction()

    {

        $file = APPLICATION_PATH . '/configs/no.xml';

        if (!file($exists)) {

            throw new Example_Exception('File not exist');

        }

        if (file_exists)) {

            throw new__Exception(' already exists');

        }

    }

}
```

当您以这种方式使用自定义异常时，更改默认控制器并为不同类型添加特定代码是常见的。以下是这样操作的示例：

```php
class ErrorController extends Zend_Controller_Action

{

    public function errorAction()

    {

        $errors = $this->_getParam('error_handler');

        $this->view->exception = $errors->exception;

        $this->view->request = $errors->request;

        switch (get_class($errors->exception)) {

            // 处理无效文件异常

            case 'Example_Invalid_Exception':

                $this->getResponse()->setHttpResponseCode(500);

                $this->view->title = 'File Not Found';

                $this->view->message = 'There was an error reading a file needed by the application.';

                break;

            // 处理重复文件异常

            case 'Example_Duplicate_Exception':

                $this->getResponse()->setHttpResponseCode(500);

                $this->view->title = 'File Already Exists';

                $this->view->message = 'There was an error writing a file needed by the application.';

                break;

            // 处理 404 异常

            case 'Zend_Controller_Dispatcher_Exception':

                $this->getResponse()->setHttpResponseCode(404);

                $this->view->title = 'Page Not Found';

                $this->view->message = 'The requested page could not be found.';

                break;

            // 处理通用动作异常

            case 'Zend_Controller_Action_Exception':

                if ($errors->exception->getCode() == 404) {

                    $this->getResponse()->setHttpResponseCode(404);

                    $this->view->title = 'Page Not Found';

                    $this->view->message = 'The requested page could not be found.';

                } else {

                    $this->getResponse()->setHttpResponseCode(500);

                    $this->view->title = 'Internal Server Error';

                    $this->view->message = 'Due to an application error, the requested page could not be displayed.';

                }

                break;

            // 处理其他所有

            default:

                break;

        }

    }

}
```

图 8-3
禁用默认错误控制器并允许 PHP 处理异常的结果。

## 第8章：日志记录与异常调试

251

```php
$this->getResponse()->setHttpResponseCode(500);
```



`$this->view->title = 'Internal Server Error';`

`$this->view->message = 'Due to an application error, the requested page could not be displayed.';`

`break;`

`}`

`}`

`}`

在这里，`errorAction()` 首先通过 `'error_handler'` 请求参数获取由源操作控制器抛出的异常对象。然后，它检查异常类，并根据异常类名切换到不同的代码分支。在这个示例中，除了标准情况（请求无效资源和通用的未捕获异常）外，控制器还为应用程序使用的自定义异常类设置了特定的分支。不言而喻的是，这个 `switch-case()` 例程可以被扩展，以支持所需的任意数量的自定义异常类。

### 控制异常的可见性

从一般原则来说，一旦应用程序迁移到生产环境，在错误消息中包含堆栈跟踪（stack traces）和其他调试信息并不是一个好主意。这些信息有时包含敏感信息，例如 SQL 查询输出、文件位置和/或用户密码，恶意用户可以利用这些信息识别应用程序的弱点并对其发起远程攻击。因此，在生产环境中隐藏这些信息是提高应用程序整体安全的重要步骤。

典型的 Zend Framework 应用程序带有四个环境的配置设置：开发（development）、测试（testing）、阶段（staging）和生产（production）。在默认设置下，这些环境中的错误显示处理如下：

在开发和测试环境中，PHP 的 `display_errors` 和 `display_startup_errors` 配置变量被设置为 `true`，导致错误消息显示给用户看。在阶段环境和生产环境中，这些变量被设置为 `false`，结果是错误消息对用户隐藏了。

**Q：我该如何在生产环境和开发环境之间切换？**

**A：** 当前环境的信息在应用程序的 `*.htaccess*` 文件中指定，作为一个名为 `APPLICATION_ENV` 的服务器环境变量。在每次请求中，`index.php` 脚本都会检查此变量，并将其传递给 `Zend_Application` 组件。然后 `Zend_Application` 会读取应用程序配置文件的适当区块，并根据该区块指定的指令设置应用程序变量。因此，要从一个环境切换到另一个环境，只需编辑应用程序的 `*.htaccess*` 文件，并将 `APPLICATION_ENV` 变量的值设置为所需的环境名称即可。

咨询专家

252 Zend Framework：入门指南

在开发环境中，默认的错误视图包含了错误消息、堆栈跟踪和请求空间的变量转储（variable dump）。在生产环境、阶段环境和测试环境中，只向用户显示错误消息。

这些设置可以通过修改应用程序配置文件中的适当区块，并通过更改错误视图来调整，根据当前正在使用的环境显示更多或更少的信息（下一节有这方面的示例）。

### 创建自定义错误页面

有了这些信息后，让我们尝试为 SQUARE 示例应用程序创建一个自定义错误页面。

由于我们没有任何特殊的异常处理需求，我们可以让错误控制器大部分保持不变，只进行一处微小的更改：为页面标题添加一个视图脚本变量。你将在“Try This 8-2”章节中看到这一微小的修改，也可以在这一章节的代码存档中找到它。

我们现在可以通过更新默认错误视图脚本（位于 `$APP_DIR/application/modules/default/views/scripts/error/error.phtml`）来自定义错误视图，以包含一些额外的调试信息：

```html
<div>
  <div id="error-image">
    <img src="/images/error.gif" />
  </div>
  <div id="error-message">
    <h1><?php echo $this->title; ?></h1>
    <?php echo $this->message; ?>
  </div>
</div>

<?php if ('development' == $env): ?>
  <div id="error-data">
    <h2>Exception message:</h2>
    <pre><?php echo $this->exception->getMessage(); ?></pre>
    <h2>Stack trace:</h2>
    <pre><?php echo $this->exception->getTraceAsString(); ?></pre>
    <h2>Request method:</h2>
    <pre><?php echo $this->request->getMethod(); ?></pre>
    <h2>Request parameters:</h2>
    <pre><?php var_dump($this->request); ?></pre>
    <h2>Server environment:</h2>
    <pre><?php echo $this->request->getServer(); ?></pre>
    <h2>System environment:</h2>
    <pre><?php echo $this->request->getEnv(); ?></pre>
  </div>
<?php endif ?>
</div>
```

尝试尝试 8-1

253 日志记录与异常调试

在开发环境中，默认的错误视图包含了错误消息、堆栈跟踪和请求空间的变量转储。在生产环境、阶段环境和测试环境中，只向用户显示错误消息。

这些设置可以通过修改应用程序配置文件中的适当区块，并通过更改错误视图来调整，根据当前正在使用的环境显示更多或更少的信息（下一节有这方面的示例）。

尝试 8-2

254 Zend Framework：入门指南

当前环境的信息在应用程序的 `*.htaccess*` 文件中指定，作为一个名为 `APPLICATION_ENV` 的服务器环境变量。在每次请求中，`index.php` 脚本都会检查此变量，并将其传递给 `Zend_Application` 组件。然后 `Zend_Application` 会读取应用程序配置文件的适当区块，并根据该区块指定的指令设置应用程序变量。因此，要从一个环境切换到另一个环境，只需编辑应用程序的 `*.htaccess*` 文件，并将 `APPLICATION_ENV` 变量的值设置为所需的环境名称。

***

一旦应用程序迁移到生产环境，在错误消息中包含堆栈跟踪和其他调试信息并不是一个好主意。这些信息有时包含敏感信息，例如 SQL 查询输出、文件位置和/或用户密码，恶意用户可以利用这些信息识别应用程序的弱点并对其发起远程攻击。因此，在生产环境中隐藏这些信息是提高应用程序整体安全的重要步骤。

典型的 Zend Framework 应用程序带有四个环境的配置设置：开发、测试、阶段和生产。在默认设置下，这些环境中的错误显示处理如下：

在开发和测试环境中，PHP 的 `display_errors` 和 `display_startup_errors` 配置变量被设置为 `true`，导致错误消息显示给用户看。在阶段环境和生产环境中，这些变量被设置为 `false`，结果是错误消息对用户隐藏了。

**Q：我该如何在生产环境和开发环境之间切换？**

**A：** 当前环境的信息在应用程序的 `*.htaccess*` 文件中指定，作为一个名为 `APPLICATION_ENV` 的服务器环境变量。在每次请求中，`index.php` 脚本都会检查此变量，并将其传递给 `Zend_Application` 组件。然后 `Zend_Application` 会读取应用程序配置文件的适当区块，并根据该区块指定的指令设置应用程序变量。因此，要从一个环境切换到另一个环境，只需编辑应用程序的 `*.htaccess*` 文件，并将 `APPLICATION_ENV` 变量的值设置为所需的环境名称即可。

咨询专家

在开发环境中，默认的错误视图包含了错误消息、堆栈跟踪和请求空间的变量转储。在生产环境、阶段环境和测试环境中，只向用户显示错误消息。

这些设置可以通过修改应用程序配置文件中的适当区块，并通过更改错误视图来调整，根据当前正在使用的环境显示更多或更少的信息（下一节有这方面的示例）。

### 创建自定义错误页面

有了这些信息后，让我们尝试为 SQUARE 示例应用程序创建一个自定义错误页面。

由于我们没有任何特殊的异常处理需求，我们可以让错误控制器大部分保持不变，只进行一处微小的更改：为页面标题添加一个视图脚本变量。你将在“Try This 8-2”章节中看到这一微小的修改，也可以在这一章节的代码存档中找到它。

我们现在可以通过更新默认错误视图脚本（位于 `$APP_DIR/application/modules/default/views/scripts/error/error.phtml`）来自定义错误视图，以包含一些额外的调试信息：

（注：此处原文HTML代码块由于重复且乱码，已根据指令要求处理并翻译逻辑）

256 Zend Framework：入门指南

请注意传递给 `Zend_Log` 对象的 `log()` 方法的第二个参数。该参数指定消息优先级，可以是预定义的八个级别中的任意一个。这些级别列在表 8-4 中，它们与 UNIX 系统日志器（`syslog`）使用的级别密切对应。开发者可以根据所记录消息的重要性为每条消息指定这些级别。

要将消息写入数据库而不是文件（在日志并发较高的情况下建议这样做），请使用 `Zend_Log_Writer_Db` 写入器。该写入器初始化时需要一个 `Zend_Db_Adapter` 类的实例（代表要使用的数据库连接）、目标表以及一个指定哪些字段应用于日志消息不同元素的数组。以下是一个示例：

```php
<?php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function logAction()
    {
        // 初始化日志引擎
        $logger = new Zend_Log();

        // 定义数据库映射
        $table = 'log';
        $fields = array(
            'LogLevel' => 'priority',
            'LogMessage' => 'message',
            'LogTime' => 'timestamp'
        );

        // 将写入器附加到日志引擎
        $writer = new Zend_Log_Writer_Db($this->adapter, $table, $fields);
        $logger->addWriter($writer);

        // 写入日志消息
        $logger->log('Body temperature critical', Zend_Log::EMERG);
    }
}
```

***注意***
数据库日志写入器无法使用格式化器。尝试这样做将导致产生异常。

还可以使用 `Zend_Log_Writer_Mail` 写入器将消息记录到电子邮件地址，该写入器接受一个配置好的 `Zend_Mail` 组件作为输入。下方的代码列表所示：

```php
<?php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function logAction()
    {
        // 创建邮件消息模板
        $mail = new Zend_Mail();
        $mail->setFrom('error-bot@host.example.com')
            ->addTo('admin@host.example.com');
        $mail->setSubject('Email error log');

        // 初始化日志引擎
        $logger = new Zend_Log();

        // 将写入器附加到日志引擎
        $writer = new Zend_Log_Writer_Mail($mail);
        $logger->addWriter($writer);

        // 写入日志消息
        // 注意：必须定义邮件传输器才能使其工作
        $logger->log('Body temperature critical', Zend_Log::EMERG);
    }
}
```

***注意***
邮件日志记录可能会严重影响性能，特别是当所使用的邮件服务器与应用程序不在同一主机上时。

要将消息直接写入系统日志器（UNIX 上的 `syslogd` 和 Windows 上的事件查看器），请使用 `Zend_Log_Writer_Syslog` 写入器，如下例所示。注意 `setFacility()` 方法的使用，它用于为 UNIX 系统日志器设置日志事件的*设施*（facility）或类别。

```php
<?php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function logAction()
    {
        // 初始化日志引擎
        $logger = new Zend_Log();

        // 将写入器附加到日志引擎
        $writer = new Zend_Log_Writer_Syslog();
        $writer->setFacility(LOG_USER);
        $logger->addWriter($writer);

        // 写入日志消息
        $logger->log('Body temperature critical', Zend_Log::EMERG);
    }
}
```

这里值得指出的是，如果前面的示例中没有任何技术能够符合你应用程序的需求，通过扩展基类 `Zend_Log_Writer_Abstract` 也很很容易为其他数据存储目标创建自定义日志写入器。子类必须暴露一个保护的 `_write()` 方法，该方法接受日志消息作为插入参数，并将其写入指定的目标。你将在下一节看到其中一个自定义日志写入器的示例。

## 向日志消息中添加数据

默认情况下，每条日志消息都包含四个键：日志消息、日志优先级（以数字和字符串形式表示）以及指示消息生成时间的时间戳。然而，通过 `Zend_Log` 对象的 `setEventItem()` 方法可以向此消息添加用户定义的键。该方法接受两个参数——键（key）和值（value），并将此键值对附加到日志消息中。如果你需要在日志消息中包含额外的调试信息，这特别有用。

以下是一个示例，它将客户端 IP 地址和请求 URL 添加到日志消息中：

```php
<?php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function logAction()
    {
        // 初始化日志引擎
        $logger = new Zend_Log();

        // 将写入器附加到日志引擎
        $writer = new Zend_Log_Writer_Mock();
        $logger->addWriter($writer);

        // 将客户端 IP 和请求 URL 添加到日志消息
        $logger->setEventItem('request', $this->getRequest()->getRequestUri());
        $logger->setEventItem('host', $this->getRequest()->getClientIp());

        // 写入日志消息
        $logger->log('Body temperature critical', Zend_Log::EMERG);
    }
}
```

## 格式化日志

消息中包含的键具有双重用途：它们也可以用作格式因子（formatifiers），为日志消息创建自定义格式字符串。`Zend_Log_Formatter_Simple` 对象使用此格式字符串来控制日志消息写入目标时的格式。格式说明符包含在百分比 (%) 符号中（参见第一个代码列表的示例）。

默认格式字符串包含时间戳、日志级别（同时以数字和字符串形式）和日志消息。然而，可以修改此格式并重新排列项目以适应特定的应用程序需求。为了说明，这里是另一个示例，它使用了通过 `setEventItem()` 方法设置的额外键：

```php
<?php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function logAction()
    {
        // 初始化日志引擎
        $logger = new Zend_Log();

        // 将写入器附加到日志引擎
        $writer = new Zend_Log_Writer_Stream(
            APPLICATION_PATH . '/../data/logs/example.log');
        $logger->addWriter($writer);

        // 将格式化器附加到写入器
```



```php
$format = '%timestamp%: %priorityName%: %request%:

%host%: %message%' . PHP_EOL;

$formatter = new Zend_Log_Formatter_Simple($format);

$writer->setFormatter($formatter);

// 将客户端 IP 和请求 URL 添加到日志消息

$logger->setEventItem('request', $this->getRequest()->getRequestUri());

$logger->setEventItem('host', $this->getRequest()->getClientIp());

// 写入日志消息

$logger->log('Body temperature critical', Zend_Log::EMERG);

}
}
```

图 8-7 展示了上述代码列表可能输出的内容。

表 8-2：Zend Framework 包含的写入器

| 写入器 | 描述 |
| :--- | :--- |
| `Zend_Log_Writer_Stream` | 写入 PHP 流（输出设备、错误设备、URL 或本地文件） |
| `Zend_Log_Writer_Db` | 写入数据库 |
| `Zend_Log_Writer_Firebug` | 写入 Firebug 控制台 |
| `Zend_Log_Writer_Mail` | 写入电子邮件地址 |
| `Zend_Log_Writer_Mock` | 为了测试目的将日志消息写入自身 |
| `Zend_Log_Writer_Null` | 写入`/dev/null` |
| `Zend_Log_Writer_Syslog` | 写入系统日志器（UNIX 上的 syslogd 和 Windows 上的事件查看器） |

表 8-3：Zend Framework 包含的格式化器

| 格式化器 | 描述 |
| :--- | :--- |
| `Zend_Log_Formatter_Simple` | 将日志消息格式化为自定义格式 |
| `Zend_Log_Formatter_Firebug` | 为 Firebug 控制台格式化日志 |
| `Zend_Log_Formatter_Xml` | 将日志格式化为 XML |

表 8-4：`Zend_Log` 组件支持的日志级别

| 日志级别 | 描述 |
| :--- | :--- |
| `DEBUG` | 调试通知 |
| `INFO` | 信息通知 |
| `NOTICE` | 通知 |
| `WARNING` | 警告通知 |
| `ERR` | 错误 |
| `CRIT` | 严重错误 |
| `ALERT` | 警报通知 |
| `EMERG` | 紧急错误 |

> **注意**
>
> 当使用`Zend_Log_Formatter_Simple`格式化器时，通过`setEventItem()`方法指定的额外键默认不会写入日志。要在日志中包含这些项目，请在传递给格式化器的格式字符串中显式地包含它们。

## 第 8 章：异常的记录与调试

261

要在 XML 中记录数据而非纯文本格式，请切换到`Zend_Log_Formatter_Xml`格式化器，如下：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function logAction()
    {
        // 初始化日志引擎

        $logger = new Zend_Log();

        // 将写入器附加日志引擎

        $writer = new Zend_Log_Writer_Stream(
            APPLICATION_PATH . '/../data/logs/example.log'
        );

        $logger->addWriter($writer);

        // 将格式化器附加写入器

        $formatter = new Zend_Log_Formatter_Xml();

        $writer->setFormatter($formatter);

        // 将客户端 IP 和请求 URL 添加到日志消息

        $logger->setEventItem(
            'request',
            $this->getRequest()->getRequestUri()
        );

        $logger->setEventItem(
            'host',
            $this->getRequest()->getClientIp()
        );

        // 写入日志消息

        $logger->log(
            'Body temperature critical',
            Zend_Log::EMERG
        );
    }
}
```

在这种情况下，日志消息被格式化为 XML 条目，适用于任何 XML 处理器进行解析。图 8-8 显示了输出示例。

与`Zend_Log_Formatter_Simple`格式化器一样，可以通过指定不同的元素名称来自定义输出 XML。这些信息应该作为数组传递给`Zend_Log_Formatter_Simple`对象的构造函数。这是一个说明此功能的示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function logAction()
    {
        // 初始化日志引擎

        $logger = new Zend_Log();

        // 将写入器附加日志引擎

        $writer = new Zend_Log_Writer_Stream(
            APPLICATION_PATH . '/../data/logs/example.log'
        );

        $logger->addWriter($writer);

        // 设置 XML 元素配置

        $xml = array(
            'data' => 'message',
            'time' => 'timestamp',
            'level' => 'priorityName',
            'request' => 'request',
            'host' => 'host',
        );

        // 将格式化器附加写入器

        $formatter = new Zend_Log_Formatter_Xml('entry', $xml);

        $writer->setFormatter($formatter);

        // 将客户端 IP 和请求 URL 添加到日志消息

        $logger->setEventItem(
            'request',
            $this->getRequest()->getRequestUri()
        );

        $logger->setEventItem(
            'host',
            $this->getRequest()->getClientIp()
        );

        // 写入日志消息

        $logger->log(
            'Body temperature critical',
            Zend_Log::EMERG
        );
    }
}
```

图 8-9 显示了修改后的输出示例。

图 8-8

一个 XML 格式的日志消息示例

### 记录应用程序异常

现在，让我们通过更新 SQUARE 示例应用程序以配备完整的异常日志系统，将所有这些信息置于实际上下文中。该系统会将异常数据记录到文件、数据库和 Firebug 控制台中。正如你所看到的，这实际上非常简单，并且可以相对容易地完成。接下来的章节将引导你完成这一过程。

> **注意**
>
> 接下来的章节包含了关于如何将异常数据记录到 Firebug（Firefox 浏览器调试器）的讨论。这假设你已经安装了可以运行的 Firefox 浏览器，以及 Firebug 和 FirePHP 扩展。如果你还没有这些组件，可以从章节末尾的链接从 Web 上下载。

### 定义日志位置

第一步是为基于文件的日志定义一个位置。因此，创建`$APP_DIR/data/logs/`目录，这是 Zend Framework 推荐目录结构下日志文件的默认位置。

```shell
cd /usr/local/apache/htdocs/square/data
mkdir logs
```

尝试一下 8-2

图 8-9

一个带有自定义元素名称的 XML 格式日志消息示例（续）

更新应用程序配置文件（位于`$APP_DIR/application/configs/application.ini`）中的该位置也是一个好主意，这样可以在 action 内部使用它。打开此文件并使用以下配置指令进行更新：

```ini
logs.logPath = APPLICATION_PATH "/../data/logs"
```

### 定义数据库日志写入器

下一步是创建一个与 Doctrine 集成的日志写入器，以便将日志条目写入数据库。

正如之前讨论的，这并不困难：只需通过扩展基类`Zend_Log_Writer_Abstract`类，并确保子类暴露一个知道如何实际执行日志写入操作的`write()`方法即可完成。然而，你可能会奇怪为什么这甚至是有必要的，因为 Zend_Log 已经自带了`Zend_Log_Writer_Db`写入器。

正如第 5 章详细解释的那样，原因与效率和一致性有关。一致性方面是因为目前所有的数据库查询都是通过 Doctrine 模型执行的，在此处添加 Zend_Db 只会使情况变得复杂。效率方面是因为使用一个数据库访问库而不是两个，可以减少应用程序需要加载的组件数量以及必须复制的配置信息。

考虑到这些解释，继续创建一个名为`Square_Log_Writer_Doctrine`的自定义日志写入器类，并包含以下代码：

```php
<?php

class Square_Log_Writer_Doctrine extends Zend_Log_Writer_Abstract
{
    // 构造函数接受模型名称和列映射

    public function __construct($modelName, $columnMap)
    {
        $this->_modelName = $modelName;
        $this->_columnMap = $columnMap;
    }

    // 设置格式化器的存位函数

    public function setFormatter($formatter)
    {
        throw new Exception(
            'Square_Log_Writer_Doctrine does not support formatting'
        );
    }

    // 将字段映射到数据库的主方法

    protected function _write($message)
    {
        $data = array();

        foreach ($this->_columnMap as $modelField => $messageField) {
            $data[$modelField] = $message[$messageField];
        }

        // (此处为数据库插入实现)
    }

    // 工厂方法

    public static function factory($config)
    {
        require_once 'Zend/Log/Writer/Abstract.php';

        return new self($config);
    }
}
```

该类基于日志记录原型（参见章节末尾的链接）。其核心是`_write()`方法，修改`$APP_DIR/modules/default/controllers/ErrorController.php`中的加粗部分如下：

```php
<?php

class ErrorController extends Zend_Controller_Action
{
    // 错误处理器

    public function errorAction()
    {
        $errors = $this->getParam('error_handler');

        switch ($errors->type) {
            case Zend_Plugin_ErrorHandler::EXCEPTION_CONTROLLER:
                // 404 错误 -- 未找到控制器或 action

                $this->getResponse()->setHttpResponseCode(404);

                $this->view->title = '页面未找到';
                $this->view->message = '未找到请求的控制器';

                break;

            case Zend_Plugin_ErrorHandler::EXCEPTION_ACTION:
                // action 错误

                $this->getResponse()->setHttpResponseCode(404);

                $this->view->title = '页面未找到';
                $this->view->message = '未找到请求的 action';

                break;

            default:
                // 应用程序错误

                $this->getResponse()->setHttpResponseCode(500);

                $this->view->title = '内部错误';
                $this->view->message = '由于应用程序错误，无法显示请求的页面';

                break;
        }

        $this->view->exception = $errors->exception;
        $this->view->request = $errors->request;
    }
}
```



这段代码实例化了`Zend_Log`组件并附加三个写入器：标准文件写入器、之前章节创建的符合 Doctrine 标准的数据库写入器以及 Firebug 控制台。`Zend_Log`对象的`setEventItem()`方法用于向日志消息附加两个额外信息，即异常的堆栈跟踪和请求参数。由于这些修改，任何冒泡到`ErrorController::errorAction`的异常都将自动记录到三个不同的位置。

## 第 8 章：日志记录与异常调试

267

为了观察这一操作，请尝试访问一个不存在的应用程序 URL，例如`http://square.localhost/no/such/resource`。系统会将异常抛给错误控制器，并向请求客户端返回 404 响应。此异常还会被记录到文件中（图 8-10）、应用程序数据库（图 8-11）以及 Firebug 控制台（图 8-12）。

*（续）*

图 8-10
以 XML 格式记录到文件的应用程序异常

图 8-11
记录到应用程序数据库的应用程序异常

268
Zend Framework：入门指南

**注意**

需要注意的是，正如本节讨论的，在生产环境中不建议将异常记录到三个不同的目的地。由于文件锁定或网络延迟问题，将数据记录到文件或数据库可能会影响性能，而将数据记录到 Firebug 控制台则会增加服务器发送给客户端的响应包（response packet）的大小。在为 Zend Framework 应用程序添加日志记录功能时，必须仔细探讨这些以及其他性能问题。

### 总结

本章标志着本书第一部分的结束，该部分旨在教你使用 Zend Framework 进行基础的应用程序开发技术。恰好的是，它涵盖了异常处理，这是应用程序开发的一个重要部分，也是每个开发者都应该熟悉的领域。

本章从介绍 PHP 5.x 引入的新异常模型开始，概述了它与较旧的 PHP 4.x 模型相比的优势。在这些背景信息的基础上，接着检查了 Zend Framework 内置的默认异常处理系统，概述了默认错误控制器的功能，并研究了如何调整默认流程以涵盖不同的情况。它还简要看了根据应用程序运行在开发环境还是生产环境如何（以及应该）修改异常处理，并演示了创建自定义错误面的实际应用。

图 8-12
记录到 Firebug 控制台的应用程序异常

269
第 8 章：日志记录与异常调试

本章的后半部分专注于`Zend_Log`组件，它为 Zend Framework 应用程序中的日志记录提供了一个功能完整的框架。该组件可以将消息记录到各种不同的存储媒体，包括文件、数据库、电子邮件地址、系统日志器和 Firebug 控制台，还可以轻松扩展以支持新的日志目的地。这些功能中的一些已通过向 SQUARE 示例应用程序添加异常日志记录代码在实际环境中进行了演示。

要了解更多关于本章讨论的主题，请考虑访问以下链接：

- PHP 5.x 中异常和异常处理的概述，位于`http://www.php.net/manual/en/language.exceptions.php`
- Zend Framework 中异常和异常处理的概述，位于`http://framework.zend.com/manual/en/zend.controller.exceptions.html`
- Zend Framework 错误处理器插件，位于`http://framework.zend.com/manual/en/zend.controller.plugins.html`
- `Zend_Log`组件，位于`http://framework.zend.com/manual/en/zend.log.html`
- `Zend_Debug`组件，位于`http://framework.zend.com/manual/en/zend.debug.html`
- Firefox Web 浏览器，位于`http://www.mozilla.com/firefox`
- Firebug 控制台调试器，位于`http://www.getfirebug.com/`
- FirePHP 扩展，位于`http://www.firephp.org/`
- 在 Zend Framework 中使用 Firebug 和 FirePHP 组件的讨论（Christoph Dorn），位于`http://www.christophdorn.com/Blog/2008/09/02/firephp-and-zend-framework-16/`
- 在 Zend Framework 应用程序中处理错误的讨论（Jani Hartikainen），位于`http://codeutopia.net/blog/2009/03/02/handling-errors-in-zend-framework/`
- 更高级的 Zend Framework 异常格式化器（Larry Root），位于`http://code.google.com/p/zend-framework-exception-formatter/`
- 基于 Doctrine 的日志写入器的原始提案和源码（Matthew Lurz），位于`http://framework.zend.com/wiki/display/ZFPROP/Zend_Log_Writer_Doctrine+-Matthew+Lurz`

*本页特留白*

271
第 9 章：理解应用程序本地化

272
Zend Framework：入门指南

关键技能与概念

- 将您的应用程序本地化到世界不同地区
- 自动应用日期、货币、温度和测量的本地习惯
- 构建多语言 Web 应用程序

## 本地化与区域设置

*本地化*（Localization）*是将应用程序适配到特定地区、国家和/或语言习惯的过程。这可能简单到确保日期、时间和货币以所选地区的正确格式显示，也复杂到将应用程序标签、菜单和消息翻译成母语语言。其原理很简单：应用程序越“本地化”，不同地区的用户越容易理解并开始使用它。大多数流行的 Web 应用程序都将此视为常例：为了说明，请考虑图 9-1，它显示了 Google.com 搜索引擎在三个不同国家（美国、法国和印度）的样子。

本地化过程的核心是*区域设置*（locales）和*区域标识符*（locale identifiers）的概念。区域标识符是代表用户语言和地理区域的字符串。该标识符由语言代码和一个国家代码组成，用下划线分隔。该标识符旨在为应用程序提供有关用户当前位置和语言的精确信息，从而能够以该位置和语言的通常习惯展示其信息。

一个例子会让这一点更清楚。例如，考虑一个设置为区域`en_US`（语言：英语，国家：美国）的应用程序。如果该应用程序感知区域设置，它将使用这些信息来确保（例如）日期以 MM-DD-YYYY 格式显示，货币以美元符号（$）开头。如果将同一个应用程序重新配置为区域`de_AT`（语言：德语，国家：奥地利），它将自动执行必要的内部调整，以 DD-MM-YYYY 格式显示日期，并欧元符号（€）开头货币。

291
第 9 章：理解应用程序本地化

图 9-1
在不同国家显示的 Google 搜索引擎

274

Zend Framework：入门指南

表 9-1 列出了常见区域标识符的列表，以及它们所代表的语言和国家的描述。

**注意**

在区域标识符中找到语言代码完整列表可以在 ISO 639 标准中找到，而相应的国家代码列表可以在 ISO 3166 标准中找到。你将在章节末尾找到指向这两个标准的链接。

## 设置应用区域语言

Zend Framework 包含一个名为`Zend_Locale`的组件，它可以用于定义应用程序的区域语言。该组件可以用于设置应用区域语言，也可以通过运行时的自动检测过程来设置。以下是一个手动将区域语言设为`fr_FR`（语言：法语，国家：法国）的示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action

{

    public function localeAction()

    {

        $locale = new Zend_Locale('fr_FR');

    }

}
```

| 区域语言 | 语言 | 国家 |
| :--- | :--- | :--- |
| `en_US` | 英语 | 美国 |
| `en_GB` | 英语 | 英国 |
| `fr_FR` | 法语 | 法国 |
| `fr_CA` | 法语 | 加拿大 |
| `fr_BE` | 法语 | 比利时 |
| `fr_CH` | 法语 | 瑞士 |
| `de_DE` | 德语 | 德国 |
| `it_IT` | 意大利语 | 意大利 |
| `es_ES` | 西班牙语 | 西班牙 |
| `es_US` | 西班牙语 | 美国 |
| `cs_CZ` | 捷克语 | 捷克 |
| `hi_IN` | 印地语 | 印度 |
| `mr_IN` | 印度 | 印度 |
| `en_IN` | 英语 | 印度 |
| `pt_BR` | 葡萄语 | 巴西 |
| `zh_CN` | 中文 | 中国 |

表 9-1
常见区域标识符

第 9 章：
理解应用本地化

275

区域标识符的各个部分可以通过`Zend_Locale`对象的`getLanguage()`和`getRegion()`方法获取，如下所示：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action

{

    public function localeAction()

    {

        // 定义区域语言

        $locale = new Zend_Locale('fr_BE');

        // 结果: 'fr'

        $this->view->message = $locale->getLanguage();

        // 结果: 'BE'

        $this->view->message = $locale->getRegion();

    }

}
```

通常，`Zend_Locale`对象在应用启动器中初始化，并通过应用注册表（registry）持久化。一旦以这种方式注册，其他感知区域的 Zend Framework 组件（如`Zend_Date`和`Zend_Form`）将自动读取选定的区域语言，并调整自身以按照该区域的习惯显示信息。这是一个说明性示例，你将在本中多次看到这种用法。

```php
<?php

class Bootstrap extends Zend_Application_Bootstrap_Bootstrap

{

    protected function _initLocale()

    {

        // 定义区域语言

        $locale = new Zend_Locale('fr_FR');

        // 注册区域语言

        $registry = Zend_Registry::getInstance();

        $registry->set('Zend_Locale', $locale);

    }

}
```

除非你非常确定你的应用只会在单个区域语言中使用，否则不建议在设计时手动设置应用区域语言。`Zend_Locale`包含自动区域语言检测功能，它可以在检查以下信息源后在运行时动态设置区域语言：

- **客户端环境的区域语言设置**
大多数现代 Web 客户端允许用户选择他们查看 Web 页面时的首选语言和区域语言。这些信息在 PHP 应用中可以通过`$_SERVER['HTTP_ACCEPT_LANGUAGES']`数组进行访问。只要这些信息可用，`Zend_Locale`就会使用它自动设置应用区域语言。当用户指定了多个首选语言和区域语言时，将使用第一个有效的区域语言。

- **主机环境的区域语言设置**
当客户端设置不可用时，`Zend_Locale`将检查服务器环境并根据主机系统的区域语言设置应用区域语言。这些信息可以在 PHP 中通过`setlocale()`函数进行访问和修改。

要使用自动区域语言检测，`Zend_Locale`对象必须使用特殊区域语言`browser`、`environment`或`auto`之一初始化。使用`browser`区域语言将检测限制为仅用户浏览器，而使用`environment`区域语言将将其限制为仅主机服务器。使用特殊的`auto`区域语言（或者，不向对象构造函数传递任何参数）将告诉`Zend_Locale`同时检查用户浏览器和主机环境的区域语言信息。

这里是一个说明这些用法的示例：

```php
<?php

class Bootstrap extends Zend_Application_Bootstrap_Bootstrap

{

    protected function _initLocale()

    {

        // 从浏览器检测区域语言

        $locale = new Zend_Locale('browser');

        // 从服务器环境检测区域语言

        $locale = new Zend_Locale('environment');

        // 从浏览器然后服务器自动检测区域语言

        $locale = new Zend_Locale('auto');

        // 从浏览器然后服务器自动检测区域语言

        $locale = new Zend_Locale();

        // 注册区域语言

        $registry = Zend_Registry::getInstance();

        $registry->set('Zend_Locale', $locale);

    }

}
```

如果区域语言自动检测失败，`Zend_Locale`将抛出异常。
276

Zend Framework：入门指南

第 9 章：
理解应用本地化

277

**注意**
重要的是，如果区域语言只包含语言代码而不包含国家代码，`Zend_Locale`将抛出异常。例如，某些客户端和服务器环境可能只返回`en`或`fr`。

```php
<?php

class Bootstrap extends Zend_Application_Bootstrap_Bootstrap

{

    protected function _initLocale()

    {

        // 尝试检测区域语言

        try {

            $locale = new Zend_Locale('browser');

        } catch (Zend_Locale_Exception $e) {

            // 失败，手动设置区域语言

            $locale = new Zend_Locale('hi_IN');

        }

    }

}
```

## 本地化数值

`Zend_Locale`组件包含一个子组件`Zend_Locale_Format`，它专门为协助本地化数值任务而设计。该组件包含一个静态`toNumber()`方法，可以按照特定区域的习惯显示数字。这里是一个示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function localeAction()
    {
        // 本地化数字
        // 结果: '195,740.676'
        $this->view->message = Zend_Locale_Format::toNumber(195740.676, array('locale' => 'en_GB'));

        // 结果: '1,95,740.676'
        $this->view->message = Zend_Locale_Format::toNumber(195740.676, array('locale' => 'en_GB'));
    }
}
```

值得注意的是，与`Zend_Date`和`Zend_Currency`不同，`Zend_Locale_Format`无法直接从注册表中获取区域语言。因此，必须作为参数向静态`toNumber()`方法传递区域标识符。

还可以通过指定自定义格式和精度进一步自定义输出数字。这些选项可以通过数组传递给`toNumber()`方法。以下是一些示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function localeAction()
    {
        // 使用自定义数字格式
        // 结果: '1,95,740.67'
        $this->view->message = Zend_Locale_Format::toNumber(195740.676, array(
            'locale' => 'en_GB',
            'number_format' => '##,##,##0.00'
        ));
    }
}
```

`Zend_Locale_Format`组件中另一个值得注意的方法静态`convertNumerals()`方法，它允许在阿拉伯数字和拉丁脚本之间转换数字。注意，这需要 PHP 的 PCRE 扩展在编译时带有 UTF-8 支持（Windows PHP 安装通常缺少此支持）。以下是它的运行示例：



## 第 9 章：理解应用本地化

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function localeAction()
    {
        // 在数字脚本间转换
        $this->view->message = Zend_Locale_Format::convertNumerals('1956', 'Latn', 'Thai');
    }
}
```

```php
Zend_Locale_Format::convertNumerals('6482093.6498', 'Latn', 'Deva');
```

**提示**

你可以通过调用`Zend_Locale::getTranslationList('script')`来获取`Zend_Locale_Format::convertNumerals`支持的数字脚本完整列表。

### 日期时间的本地化

Zend Framework 包含一个专门用于处理时间显示和操作的组件。该组件`Zend_Date`提供了一个简单的 API 来创建和格式化日期时间值；它还支持比 PHP 内置`mktime()`函数更广泛的时间戳，并且可以自动检测应用程序区域（如果使用`Zend_Locale`设置过），并根据该区域的本地习惯展示日期和时间值。

以下是`Zend_Date`的一个简单示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function dateAction()
    {
        // 将日期设置为现在
        $date = new Zend_Date();
        // 结果：'Dec 18, 2009 5:58:38 AM'
        $this->view->message = $date;
    }
}
```

正如这些示例所示，`Zend_Date`对象会自动初始化为当前日期和时间。也可以通过向构造函数传递可读的日期字符串、UNIX 时间戳或日期/时间段数组将其初始化为特定的日期和时间。以下是一些示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function dateAction()
    {
        // 使用 UNIX 时间戳设置日期
        $date = new Zend_Date(1261125725);
        // 结果：'2009-12-18T08:42:05+00:00'
        $this->view->message = $date->get(Zend_Date::ISO_8601);

        // 使用字符串设置日期
        // 结果：'2010-12-25T15:56:00+00:00'
        $date->set('25/12/2010 15:56');
        $this->view->message = $date->get(Zend_Date::ISO_8601);

        // 使用数组设置日期
        // 返回 '2010-06-24T16:35:00+00:00'
        $date->set(
            array(
                'year' => 2010,
                'month' => 6,
                'day' => 24,
                'hour' => 16,
                'minute' => 35,
                'second' => 0
            )
        );
        $this->view->message = $date->get(Zend_Date::ISO_8601);
    }
}
```

**注意**

避免创建多个`Zend_Date`实例，因为每个实例都会产生显著的启动开销。因此，在需要多个实例的情况下，重置现有实例比实例化多个实例要高效得多。

正如上一个示例所示，`Zend_Date`包含了一组预定义的日期格式常量，例如 ISO 8601 和 UNIX 时间戳。这些常量可以传递给`Zend_Date`对象的`get()`方法，以按正确的格式获取日期时间输出。下面的列表展示了其中一些格式常量，以及相应输出的示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function dateAction()
    {
        // 使用字符串设置日期
        $date = new Zend_Date('25/12/2010 15:56');
        // 结果：'2010-12-25T15:56:00+00:00'
        $this->view->message = $date->get(Zend_Date::ISO_8601);
        // 结果：'Sat, 25 Dec 2010 15:56:00 +0000'
        $this->view->message = $date->get(Zend_Date::RFC_2822);
        // 结果：'Saturday, 25-Dec-10 15:56:00 UTC'
        $this->view->message = $date->get(Zend_Date::RFC_850);
        // 结果：'2010-12-25T15:56:00+00:00'
        $this->view->message = $date->get(Zend_Date::ATOM);
        // 返回 '2010-06-24T16:35:00+00:00'
        $this->view->message = $date->get(Zend_Date::ISO_8601);
        // 结果：'Saturday, December 25, 2010'
        $this->view->message = $date->get(Zend_Date::DATE_FULL);
        // 结果：'December 25, 2010 3:56:00 PM UTC'
        $this->view->message = $date->get(Zend_Date::DATETIME_LONG);
    }
}
```

**提示**

如果预定义的格式不能满足你的需求，你可以自定义格式。`Zend_Date`同样是区域感知的：如果应用程序通过`Zend_Locale`设置了区域，它将使用该区域的习惯。你也可以通过构造函数显式指定区域标识符，让`Zend_Date`根据该区域来格式化日期。以下示例展示了这些用法：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function dateAction()
    {
        // 使用字符串设置日期
        $date = new Zend_Date('25/12/2010 15:56');
        // 结果：'2010-12-25T15:56:00+00:00'
        $this->view->message = $date->get(Zend_Date::ISO_8601);
        // 结果：'Sat, 25 Dec 2010 15:56:00 +0000'
        $this->view->message = $date->get(Zend_Date::RFC_2822);
        // 结果：'Saturday, 25-Dec-10 15:56:00 UTC'
        $this->view->message = $date->get(Zend_Date::RFC_850);
        // 结果：'2010-12-25T15:56:00+00:00'
        $this->view->message = $date->get(Zend_Date::ATOM);
        // 返回 '2010-06-24T16:35:00+00:00'
        $this->view->message = $date->get(Zend_Date::ISO_8601);
        // 结果：'Saturday, December 25, 2010'
        $this->view->message = $date->get(Zend_Date::DATE_FULL);
        // 结果：'December 25, 2010 3:56:00 PM UTC'
        $this->view->message = $date->get(Zend_Date::DATETIME_LONG);
    }
}
```



## Zend Framework：初学者指南

### 货币的本地化

**注意**

ISO 4217 标准提供了一份完整的货币代码列表。你可以在本章末尾找到指向该标准的链接。

你还可以使用`setFormat()`方法来自`Zend_Currency`返回的货币字符串，以调整货币符号的位置、货币名称、精度以及三位货币代码的可见性。该方法接受一个键值对数组，并据此重新格式化字符串。以下示例说明了这一点：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function currencyAction()
    {
        // 初始化货币对象
        $currency = new Zend_Currency('hi_IN');

        // 调整货币格式
        $currency->setFormat(
            array(
                'position' => Zend_Currency::RIGHT,
                'display' => Zend_Currency::USE_NAME,
                'precision' => 2,
            )
        );
        // 结果：'990.65 — Indian rupee'
        $this->view->message = $currency->toCurrency(990.65);

        // 创建自定义货币格式
        $currency->setFormat(
            array(
                'position' => Zend_Currency::LEFT,
                'display' => Zend_Currency::USE_SYMBOL,
                'precision' => 4,
                'name' => 'Driit',
                'symbol' => 'DRT'
            )
        );
        // 结果：'DRT 990.6500'
        $this->view->message = $currency->toCurrency(990.65);
    }
}
```

**提示**

`Zend_Currency`包含了在本地化货币之前对货币值执行汇率转换的能力。或者，考虑使用`PEAR Services_ExchangeRates`软件包，它提供了一个API，可以使用当前汇率执行实时货币转换。你可以在本章末尾找到更多信息的链接。

### 测量值的本地化

重量和计量是另一个经常需要本地化的领域，Zend Framework在此也提供了解决方案：`Zend_Measure`，这是一个旨在帮助在不同测量单位之间进行转换并根据本地习惯展示结果的组件。该组件支持超过30种不同的测量类型，从长度、重量、体积和温度等常见类型到加速度、照度、功率、频率和能量等更不常见的类型。

要初始化`Zend_Measure`对象，需要向对象构造函数传递两个参数：一个数值测量值和一个表示其所用测量标准的常量。考虑以下示例，它通过创建一个`Zend_Measure_Temperature`对象来说明了这一点：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function measureAction()
    {
        // 初始化测量对象
        $tempF = new Zend_Measure_Temperature(
            98.6, Zend_Measure_Temperature::FAHRENHEIT);
        // 结果：'98.6 °F'
        $this->view->message = $tempF;
    }
}
```

这是另一个示例，它创建了`Zend_Measure_Length`和`Zend_Measure_Weight`对象：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function measureAction()
    {
        // 初始化测量对象
        $lengthCm = new Zend_Measure_Length(2540, Zend_Measure_Length::CENTIMETER);
        // 结果：'2,540 cm'
        $this->view->message = $lengthCm;

        // 初始化测量对象
        $weightKg = new Zend_Measure_Weight(6500, Zend_Measure_Weight::KILOGRAM);
        // 结果：'6,500 kg'
        ////$this->view->message = $weightKg;
    }
}
```

每个`Zend_Measure`对象都暴露了一个`convertTo()`方法，可以从一个测量单位转换为另一个。目标测量单位必须作为`convertTo()`方法的参数指定。以下是一些说明该方法的示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function measureAction()
    {
        // 转换温度
        // 结果：'37.0 °C'
        $tempF = new Zend_Measure_Temperature(
            98.6, Zend_Measure_Temperature::FAHRENHEIT);
        $this->view->message = $tempF->convertTo(
            Zend_Measure_Temperature::CELSIUS);

        // 转换长度
        // 结果：'1,000.0 in'
        $lengthCm = new Zend_Measure_Length(2540, Zend_Measure_Length::CENTIMETER);
        $this->view->message = $lengthCm->convertTo(Zend_Measure_Length::INCH);

        // 转换重量
        // 结果：'6,500,000.0 g'
        $weightKg = new Zend_Measure_Weight(6500, Zend_Measure_Weight::KILOGRAM);
        $this->view->message = $weightKg->convertTo(Zend_Measure_Weight::GRAM);
    }
}
```

**注意**

`Zend_Measure`不允许你从一种测量类型转换为另一种。因此，例如，任何从长度转换为重量或从速度转换为频率的尝试都将导致异常。

与`Zend_Currency`一样，`Zend_Measure`是感知区域的。可以将区域标识符作为可选参数传递给`Zend_Measure`构造函数，如果不存在，`Zend_Measure`可以使用默认值。以下是一个说明这两种场景的示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function measureAction()
    {
        // 初始化测量对象
        // 定义并注册区域设置（define-and-register locale）
        $locale = new Zend_Locale('pt_BR');
        $registry = Zend_Registry::getInstance();
        $registry->set('locale', $locale);

        // 使用默认区域设置转换温度
        // 结果：'37.0 °C'
        $tempF = new Zend_Measure_Temperature(
            98.6, Zend_Measure_Temperature::FAHRENHEIT);
        $this->view->message = $tempF->convertTo(
            Zend_Measure_Temperature::CELSIUS);

        // 使用自定义区域设置转换长度
        // 结果：'1,000.0 in'
        $lengthCm = new Zend_Measure_Length(2540, Zend_Measure_Length::CENTIMETER);
        $this->view->message = $lengthCm->convertTo(Zend_Measure_Length::INCH);
    }
}
```

### 字符串的本地化

虽然英语是你在Web上最看到的语言，但记住，仍很大比例的用户母语不是英语。任何本地化项目最大的部分是将文本内容翻译成多种语言。`Zend_Translate`提供了一个全面的API来管理不同语言的字符串，通过CSV文件、PHP数组，并可以轻松扩展支持其他数据源（例如数据库）。这是最简单的格式，`Zend_Translate`现在可以根据选定的区域设置在运行时翻译这些字符串。示例如下：假设有不同语言的翻译源：

```php
<?php
// languages/messages.fr.php
return array(
    'welcome' => 'Bienvenue',
    'dog' => 'chien',
    'cat' => 'chat',
    'one' => 'un',
    'two' => 'deux',
    'three' => 'trois'
);
```

```php
<?php
// languages/messages.de.php
return array(
    'welcome' => 'Willkommen',
    'dog' => 'hund',
    'cat' => 'katz',
    'one' => 'eins',
    'two' => 'zwei',
    'three' => 'drei'
);
```

```php
<?php
// languages/messages.es.php
return array(
    'welcome' => 'Bienvenido',
    'dog' => 'gato',
    'cat' => 'perro',
    'one' => 'un',
    'two' => 'dos',
    'three' => 'tres'
);
```

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function translateAction()
    {
        // 创建翻译对象
        // 指定翻译适配器
        // 为每个区域设置指定源文件
        $translate = new Zend_Translate('array', APPLICATION_PATH .
'/../languages/messages.es_ES.php', 'es_ES');
        $translate->addTranslation(APPLICATION_PATH .
'/../languages/messages.de.php', 'de_DE');
        $translate->addTranslation(APPLICATION_PATH .
'/../languages/messages.fr_FR.php', 'fr_FR');

        // 设置当前区域设置
        $translate->setLocale('fr_FR');
        // 翻译字符串
        // 结果：'un, deux, trois'
        $this->view->message = sprintf('%s, %s, %s',
            $translate->_('one'),
            $translate->_('two'),
            $translate->_('three')
        );

        // 设置区域设置
        $translate->setLocale('de_DE');
        // 翻译字符串
        // 结果：'eins, zwei, drei'
        $this->view->message = sprintf('%s, %s, %s',
            $translate->_('one'),
            $translate->_('two'),
            $translate->_('three')
        );
    }
}
```

初始化一个`Zend_Translate`对象需要三个参数：要使用的翻译适配器类型、翻译源文件的位置以及该文件的语言区域（locale）。然后使用`setLocale()`方法来定义当前的语言区域。有了这些信息后，`Zend_Translate`能够查找相应的翻译文件，并为每个字符串返回正确的翻译结果。

**提示**

如果`Zend_Translate`无法找到指定语言区域的翻译源，它将返回原始翻译键并生成PHP错误通知。要禁用此通知，请在`Zend_Translate`对象构造函数的第四个参数中传递特殊的`'disableNotices'`选项。

#### 与适配器和数据源工作

`Zend_Translate`支持多种用于翻译源文件的不同适配器。上一个示例使用了`Array`适配器，它适用于大多数场景。然而，也存在其他选项，如表9-2所示。

`Zend_Translate`还可以递归扫描目录树，并通过自动源检测过程将所有找到的翻译源附加到`Zend_Translate`对象中。每个翻译文件的语言区域将根据相应的文件和/或目录名称自动检测。这消除了使用`addTranslation()`方法手动添加翻译源的需要。

| 适配器 |  |
| :--- | :--- |
| `Zend_Translate_Adapter_Array` | 读取以PHP数组表示的翻译源 |
| `Zend_Translate_Adapter_Csv` | 读取以CSV格式表示的翻译源 |
| `Zend_Translate_Adapter_Ini` | 读取以INI格式表示的翻译源 |
| `Zend_Translate_Adapter_Gettext` | 读取以GNU gettext二进制格式表示的翻译源 |
| `Zend_Translate_Adapter_Tbx` | 读取以TermBase eXchange (TBX)格式表示的翻译源 |
| `Zend_Translate_Adapter_Tmx` | 读取以Translation Memory Exchange (TMX)格式表示的翻译源 |
| `Zend_Translate_Adapter_Qt` | 读取以QtLinguist格式表示的翻译源 |
| `Zend_Translate_Adapter_Xliff` | 读取以XML本地交换文件格式(XLIFF)表示的翻译源 |
| `Zend_Translate_Adapter_XmlTm` | 读取以XML内存(XML:TM)格式表示的翻译源 |

表9-2：Zend Framework包含的翻译适配器

为了说明，请考虑图9-2，它展示了使用特定语言区域目录作为翻译源文件，以及以下代码列表，它配置`Zend_Translate`自动扫描此目录结构并包含所有找到的翻译源：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function translateAction()
    {
        // 创建翻译对象
        // 指定翻译适配器
        // 自动查找每个语言区域的源文件
        $translate = new Zend_Translate('array', APPLICATION_PATH .
        '/../languages', null,
        array('scan' => Zend_Translate::LOCALE_DIRECTORY));
    }
}
```



注意，在这种情况下，`Zend_Translate`对象构造函数的第二个参数仅仅是待扫描目录树的根目录，额外的第四个参数表示应从每个目录的名称读取语言区域信息。

另一种方法是使用基于文件的结构，每个文件名包含相应翻译源的语言区域标识符。图 9-3 展示了这样的系统，接下来的代码列表演示了如何配合使用`Zend_Translate`：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action

{

    public function translateAction()

    {

        // 创建翻译对象

        // 指定翻译适配器

        // 自动查找每个语言区域的源文件

        $translate = new Zend_Translate('array', APPLICATION_PATH .

        '/../languages', null,

        array('scan' => Zend_Translate::LOCALE_FILENAME));

    }

}
```

图 9-2：独立目录中的翻译源
![](img/222e7e58871b088cc6397852e1452b57_308_0.png) ![](img/222e7e58871b088cc6397852e1452b57_308_1.png)

图 9-3：独立文件中的翻译源

当然，这些并不是仅有的两种选项。`Zend_Translate`支持多种用于翻译源的标准目录布局，你应该选择一个最适合你项目大小和规模的。你可以通过本章末的链接阅读更多关于这些布局的知识，并查看一些示例。

## 使用应用语言区域

与许多其他`Zend_Framework`组件一样，`Zend_Translate`是感知语言区域的：如果有已注册的`Zend_Locale`实例，它可以自动将此语言区域作为所有翻译操作的默认值。这非常方便，因为它允许仅设置一次语言区域（在应用启动器中），然后将该语言区域应用于整个应用程序的所有`Zend_Translate`操作中。

**Q：什么是 GNU gettext？我该如何使用它？**

**A：** GNU gettext 是 GNU 翻译项目的一部分，为应用程序创建和使用翻译表提供了标准方法。在该系统中，不同语言的翻译字符串指定在人类可读的消息模板文件（`.po`）中，每种语言一个文件。这些文件随后被转换为二进制目录文件（`.mo`）。

按照惯例，gettext 使用基于目录的布局，其中用于不同语言的翻译文件存储在不同的目录中（图 9-4 显示了一个示例）。值得注意的是，`Zend_Translate`的源检测功能可以识别并使用这种布局。

### 咨询专家

Zend Framework：入门指南

以下示例通过在注册表中注册`de_DE`（德语，德国）语言区域并让`Zend_Translate`自动使用它来演示这一点：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action

{

    public function localeAction()

    {

        // 定义并注册语言区域

        $locale = new Zend_Locale('de_DE');

        $registry = Zend_Registry::getInstance();

        $registry->set('Zend_Locale', $locale);

        // 创建翻译对象

        // 指定翻译适配器

        // 自动查找每个语言区域的源文件

        $translate = new Zend_Translate('array',

        APPLICATION_PATH . '/../languages/',

        null,

        array('scan' => Zend_Translate::LOCALE_FILENAME));

        // 翻译字符串

        // 结果：'eins, zwei, drei'

        $this->view->message = sprintf('%s, %s, %s',

        $translate->_('one'),

        $translate->_('two'),

        $translate->_('three')

        );

    }

}
```

图 9-4：翻译源的常规 gettext 目录布局

重要的是，如果`Zend_Translate`无法为完全限定的语言区域找到翻译源，它会自动“降级”语言区域并使用匹配降级语言区域的翻译源。例如，如果应用语言设置为`fr_LU`（法语，卢森堡）但没有`fr_LU`语言的翻译源，`Zend_Translate`将自动使用`fr`语言的翻译源（如果可用）。

### 使用翻译视图助手

之前的章节演示了在控制器作用范围内的翻译操作。然而，实际上正确的方法是在视图脚本的作用范围内执行翻译操作，而不是控制器中。`Zend_Translate`包含一个翻译视图助手，可以在视图脚本中执行这些操作。

要使用翻译视图助手，必须先将`Zend_Translate`对象注册到注册表中，以便在整个应用程序中访问。以下是执行此操作的示例：

```php
<?php

class Bootstrap extends Zend_Application_Bootstrap_Bootstrap

{

    protected function _initTranslate()

    {

        // 初始化并注册翻译对象

        $translate = new Zend_Translate('array',

        APPLICATION_PATH . '/../languages/',

        null,

        array('scan' => Zend_Translate::LOCALE_FILENAME));

        $registry->set('Zend_Translate', $translate);

    }

}
```

完成此操作，只需通过调用视图对象的`translate()`方法即可视图脚本中执行翻译，如下代码所示：

```html
<div id="header">
<?php echo $this->translate('welcome'); ?>
</div>
```

Zend Framework：初学者指南

一旦`Zend_Translate`对象注册到应用注册表（application registry），其他 Zend Framework 组件也可以使用它进行字符串本地化。这最好的例子是`Zend_Form`，它可以自动使用已注册的`Zend_Translate`对象来准备表单字段和按钮标签、选项元素、字段集图例（fieldset legends）以及验证错误消息的本地化版本。你将在下一节中看到关于这方面的示例。

## 示例应用程序的本地化

如前几节所示，Zend Framework 为应用程序本地化提供了全面的 API。现在你已经了解了理论，让我们将其应用于实际语境中，通过对 SQUARE 示例应用程序进行本地化，支持三种不同的语言：英语（英国英语和美国英语）、法语和德语。

### 设置应用程序区域

应用本地化的第一步是定义应用程序的区域（locale）。该区域信息随后可以被`Zend_Date`和`Zend_Translate`等组件使用。推荐的方法是首先尝试从用户的客户端自动发现区域设置，如果失败，则手动将区域设置为一个合理的值。

从编辑应用程序引导器开始，路径位于`$APP_DIR/application/Bootstrap.php`，并添加一个方法来执行区域自动发现，如下：

```php
<?php

class Bootstrap extends Zend_Application_Bootstrap_Bootstrap

{

    protected function _initLocale()

    {

        try {

            $locale = new Zend_Locale('browser');

        } catch (Zend_Locale_Exception $e) {

            $locale = new Zend_Locale('en_GB');

        }

        $registry = Zend_Registry::getInstance();

        $registry->set('Zend_Locale', $locale);

    }

}
```

在这种情况下，`Zend_Locale`将尝试自动检测用户的当前区域设置，如果无法检测，则会将区域设置为`en_GB`（语言：英语，国家：英国）。该区域将通过`Zend_Registry`注册到应用注册表中，以便其他感知区域的组件也能使用它。

### 本地化数字和日期

区域定义完成后，下一步是检查应用程序并开始本地化数字和日期的过程。如果你查看邮票目录视图（stamp catalog views），你会发现每条邮票记录都包含一些数值：邮票的面值以及邮票的最低和最高售价。理想情况下，这些值应该被格式化，以反映用户当前的区域习惯。

每个邮票详情页中目前缺失的另一个项目是其出售日期。对于潜在买家来说，这是一个有用信息，因为它允许他们判断列表的“新”程度。理想情况下，此日期值也应该以用户的本地语言和习惯呈现。

`Zend_Locale_Format`组件通过其`toNumber()`静态方法提供了本地化数字所需的工具，而`Zend_Date`组件可以处理日期的本地化和格式化。要使用这些工具，请如下所示更新`Catalog_ItemController::displayAction`，路径位于`$APP_DIR/application/modules/catalog/controllers/ItemController.php`：

```php
<?php

class Catalog_ItemController extends Zend_Controller_Action

{

    // 显示目录项的动作

    public function displayAction()

    {

        // 为 GET 输入设置过滤器和验证器

        $filters = array(

            'id' => array('HtmlEntities', 'StripTags', 'StringTrim')

        );

        $validators = array(

            'id' => array('NotEmpty', 'Int')

        );

        $input = new Zend_Filter_Input($filters, $validators);

        $input->setData($this->getRequest()->getParams());

        // 测试输入是否有效

        // 获取请求的记录

        // 附加到视图

        if ($input->isValid()) {

            $q = Doctrine_Query::create()

                ->from('Square_Model_Item i')

                ->leftJoin('i.Square_Model_Country c')

                ->leftJoin('i.Square_Model_Grade g')

                ->leftJoin('i.Square_Model_Type t')

                ->where('i.RecordID = ?', $input->id)

                ->addWhere('i.DisplayStatus = 1')

                ->addWhere('i.DisplayUntil >= CURDATE()');

            $result = $q->fetchArray();

            if (count($result) == 1) {

                $this->view->item = $result[0];

                $this->view->images = array();

                $config = $this->getInvokeArg('bootstrap')->getOption('uploads');

                foreach (glob("{$config['uploadPath']}/{$this->view->item['RecordID']}_*") as $file) {

                    $this->view->images[] = basename($file);

                }

                $configs = $this->getInvokeArg('bootstrap')->getOption('configs');

                $localConfig = new Zend_Config_Ini($configs['localConfigPath']);

                $this->view->seller = $localConfig->user->displaySellerInfo;

                $registry = Zend_Registry::getInstance();

                $this->view->locale = $registry->get('Zend_Locale');

                $this->view->recordDate = new Zend_Date($result[0]['RecordDate']);

            } else {

                throw new Zend_Controller_Action_Exception('Page not found', 404);

            }

        } else {

            throw new Zend_Controller_Action_Exception('Invalid input');

        }

    }

}
```



在这里，`displayAction()` 方法获取当前的区域设置，如果无法获取，则会将区域设置为`en_GB`（语言：英语，国家：英国）。该区域设置从注册表中获取，并将请求的记录将其附加到视图中。如果你查看邮票目录视图，你会发现每条邮票记录都包含一些数值：邮票的面值以及邮票的最低和最高售价。理想情况下，这些值应该被格式化，以反映用户当前的区域习惯。

每个邮票详情页中目前缺失的另一个项目是其出售日期。对于潜在买家来说，这是一个有用信息，因为它允许他们判断列表的“新”程度。理想情况下，此日期值也应该以用户的本地语言和习惯呈现。

`Zend_Locale_Format` 组件通过其`toNumber()`静态方法提供了本地化数字所需的工具，而`Zend_Date`组件可以处理日期的本地化和格式化。要使用这些工具，请如下所示更新`Catalog_ItemController::displayAction`，路径位于`$APP_DIR/application/modules/catalog/controllers/ItemController.php`：

在这里，`displayAction()` 方法获取当前的区域设置，如果无法获取，则会将区域设置为`en_GB`（语言：英语，国家：英国）。该区域设置从注册表中获取，并将请求的记录将其附加到视图中。如果你查看邮票目录视图，你会发现每条邮票记录都包含一些数值：邮票的面值以及邮票的最低和最高售价。理想情况下，这些值应该被格式化，以反映用户当前的区域习惯。

每个邮票详情页中目前缺失的另一个项目是其出售日期。对于潜在买家来说，这是一个有用信息，因为它允许他们判断列表的“新”程度。理想情况下，此日期值也应该以用户的本地语言和习惯呈现。

`Zend_Locale_Format` 组件通过其`toNumber()`静态方法提供了本地化数字所需的工具，而`Zend_Date`组件可以处理日期的本地化和格式化。要使用这些工具，请如下所示更新`Catalog_ItemController::displayAction`，路径位于`$APP_DIR/application/modules/catalog/controllers/ItemController.php`：

在这里，`displayAction()` 方法获取当前的区域设置，如果无法获取，则会将区域设置为`en_GB`（语言：英语，国家：英国）。该区域设置从注册表中获取，并将请求的记录将其附加到视图中。

### 定义字符串本地化目标

处理了日期和数字后，下一步是进行字符串本地化。由于空间限制，无法本地化应用程序中的每一个字符串，因此此示例将字符串本地化限制在以下目标：应用程序的主菜单、页面页脚和联系表单。

要执行字符串本地化，有必要编辑每个布局和视图，并使用翻译视图助手将其插值到其中。一个很好的起点是应用程序的主布局，它包含主菜单。编辑此文件，路径位于`$APP_DIR/application/layouts/master.phtml`，加粗修订部分如下：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml-lang="en" lang="en">
...
<div id="menu">
    <a href="<?php echo $this->url(array(), 'home'); ?>">
        <?php echo $this->translate('menu-home'); ?>
    </a>
    <a href="<?php echo $this->url(array('page' => 'services'), 'static-content'); ?>">
        <?php echo $this->translate('menu-services'); ?>
    </a>
    <a href="<?php echo $this->url(array('module' => 'catalog', 'controller' => 'item', 'action' => 'search'), 'default', true); ?>">
        <?php echo $this->translate('menu-catalog'); ?>
    </a>
    <a href="<?php echo $this->url(array(), 'contact'); ?>">
        <?php echo $this->translate('menu-contact'); ?>
    </a>
</div>
</div>
<div id="content">
    <?php echo $this->layout()->content ?>
</div>
<div id="footer">
    <p>
        <?php echo $this->translate('created-with'); ?>
        <a href="http://framework.zend.com/">Zend Framework</a>..
        <?php echo $this->translate('licensed-under'); ?>
        <a href="http://www.creativecommons.org/">Creative Commons</a>.
    </p>
</div>
</body>
</html>
```

## 第 9 章：理解应用程序本地化

299

接下来是应用程序的联系表单。此表单定义使用`Zend_Form`创建，它可以自动检测并使用已注册的`Zend_Translate`对象来执行运行时字符串本地化。因此，这里只需要将每个元素的标签（label）替换为字符串标识符，标识符将在运行时自动替换为翻译后的值。编辑`$APP_DIR/library/Square/Form/Contact.php`中的表单定义，并进行如下加粗显示的更改：

```php
<?php
class Square_Form_Contact extends Zend_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/contact/index')
            ->setMethod('post');

        // 为姓名创建文本输入
        $name = new Zend_Form_Element_Text('name');
        $name->setLabel('contact-name')
            ->setOptions(array('size' => '35'))
            ->setRequired(true)
            ->addValidator('NotEmpty', true)
            ->addValidator('Alpha', true)
            ->addFilter('HTMLEntities')
            ->addFilter('StringTrim');

        // 为邮箱地址创建文本输入
        $email = new Zend_Form_Element_Text('email');
        $email->setLabel('contact-email-address');
        $email->setOptions(array('size' => '50'))
            ->setRequired(true)
            ->addValidator('NotEmpty', true)
            ->addValidator('EmailAddress', true)
            ->addFilter('HTMLEntities')
            ->addFilter('StringToLower')
            ->addFilter('StringTrim');

        // 为消息主体创建文本区域
        $message = new Zend_Form_Element_Textarea('message');
        $message->setLabel('contact-message')
            ->setOptions(array('rows' => '8','cols' => '40'))
            ->setRequired(true)
            ->addValidator('NotEmpty', true)
            ->addFilter('HTMLEntities')
            ->addFilter('StringTrim');
```

*(续上)*

300

Zend Framework：初学者指南

```php
        // 创建验证码
        $captcha = new Zend_Form_Element_Captcha('captcha', array(
            'captcha' => array(
                'captcha' => 'Image',
                'wordLen' => 6,
                'timeout' => 300,
                'width' => 300,
                'height' => 100,
                'imgUrl' => '/captcha',
                'imgDir' => APPLICATION_PATH . '/../public/captcha',
                'font' => APPLICATION_PATH . '/../public/fonts/LiberationSansRegular.ttf',
            )
        ));
        $captcha->setLabel('contact-verification');

        // 创建提交按钮
        $submit = new Zend_Form_Element_Submit('submit');
        $submit->setLabel('contact-send-message')
            ->setOptions(array('class' => 'submit'));

        // 将元素添加到表单
        $this->addElement($name)
            ->addElement($email)
            ->addElement($message)
            ->addElement($captcha)
            ->addElement($submit);
    }
}
```

### 创建翻译源

一旦为各种视图元素配置了本地化，下一步是为每个语言创建翻译源文件。为了简单起见，将这些翻译源文件表示为 PHP 数组，并在文件名中指定区域（locale）。

首先，切换到`$APP_DIR`并执行以下命令为这些翻译源创建一个目录：

```shell
mkdir languages
```

然后，为应该支持的种语言创建翻译源文件。这里是法语翻译源文件的示例，它应该保存为`$APP_DIR/languages/messages.fr.php`：

```php
<?php
return array(
    'menu-home' => 'ACCUEIL',
    'menu-services' => 'SERVICES',
    'menu-catalog' => 'BROCHURE',
    'menu-contact' => 'CONTACTEZ-NOUS',
    'welcome' => 'Bienvenue',
    'created-with' => 'Créé avec',
    'licensed-under' => 'Sous license',
    'contact-name' => 'Nom:',
    'contact-email-address' => 'Adresse email:',
    'contact-message' => 'Message:',
    'contact-verification' => 'Vérification:',
    'contact-send-message' => 'Envoyer Message',
    'contact-title' => 'Contactez-Nous',
);
```

完成后，您应该有一个像图 9-5 所示的目录结构。

**提示**

在创建包含非拉丁字符的翻译文件时，使用 UTF-8 编码以避免数据损坏。支持 UTF-8 编码的一些免费和商业文本编辑器包括 UNIX 上的`gedit`和 Microsoft Windows 上的`Notepad2`。下载链接可以在章末尾找到。

![](img/222e7e58871b088cc6397852e1452b57_319_0.png)

图 9-5
应用程序的翻译源，每个一个单独的文件

*(续上)*

**Q：为什么除了为`en_US`和`en_GB`区域准备文件外还要为`en`区域准备一个单独的翻译文件？**

**A：** 如本章前面解释的那样，如果`Zend_Translate`找不到对应区域的翻译文件，它将退回到`en`区域。

### 注册翻译对象

302

Zend Framework：初学者指南

最后一步是更新应用程序引导程序（bootrapper）并注册`Zend_Translate`实例。该实例将在所有控制器和视图可用。要实现这一点，编辑`$APP_DIR/application/Bootstrap.php`，并添加以下方法：

```php
<?php
class Bootstrap extends Zend_Application
{
    protected _initTranslate()
    {
        $translate = new Zend_Translate(
            APPLICATION_PATH . '/languages/',
            null,
            array('scan' => 1));
        $registry = Zend_Registry::getInstance();
        $registry->set('translate', $translate);
    }
}
```

**提示**

与其获取`Zend_Registry`实例，你可以通过快捷方式`Zend_Registry::get($index)`直接访问值并使用`Zend_Registry::set($index, $value)`完成！为了看到效果，请将浏览器设置为法语或德语。图 9-6 显示了在 Firefox 中如何操作，而图 9-7 显示了在 Microsoft Explorer 中如何操作。

303

第 9 章：理解本地化

然后，访问应用程序首页页 **http://localhost/**，你应该会看到类似图 9-8 所示的内容。注意主菜单和页脚以所选语言显示。

如果你将浏览器设置为另一种首选语言，并且`Zend_Translate`能找到该语言的翻译源，内容将自动翻译为所选语言（见图 9-10）。另一方面，如果`Zend_Translate`无法找到该语言的翻译源，将无法进行翻译并显示原始字符串标识符（见图 9-11）。最后，如果你的浏览器没有设置任何语言，区域自动检测将失败，`Zend_Locale`和`Zend_Translate`将使用回退区域`en_GB`（见图 9-12）。

图 9-8
自动本地化法语的应用程序首页

304

Zend Framework：初学者指南

访问联系表单 **http://localhost/contact**，你会发现字段标签也由`Zend_Form`自动翻译了（见图 9-9）。

![](img/222e7e58871b088cc6397852e1452b57_321_0.png)

*(续上)*

图 9-9
自动本地化法语的应用程序联系表单

305

第 9 章：理解本地化

**注意**

你会注意到静态页面内容无论区域自动检测如何，都以美国英语显示。在本章有限的篇幅无法涵盖本地化的这一方面，但你可以通过为每种语言创建单独的静态页面并调整静态页面控制器渲染对应当前区域或语言的页面来轻松处理。这种方法优于创建包含每个静态页面内容的翻译键，因为维护如此大量的本地化内容块很快就会变成问题。

图 9-10
自动本地化德语的应用程序首页

图 9-11
无可用翻译时的应用程序首页

图 9-12
无法进行区域自动检测时手动设置为英国英语的应用程序首页

306

Zend Framework：初学者指南

## 支持手动选择区域设置

现在，虽然自动检测区域很方便，但你可能也希望用户能够手动选择他们所需的语言和区域。通常情况下，这一功能在应用程序用户界面中以一组可点击的旗帜图标的形式实现；点击其中一个图标即可将应用程序切换到相应的语言。

要添加此功能，请在应用程序“default”模块中定义一个新的`LocaleController`，它将负责将区域手动设置为用户所选的区域，并填充以下代码：

```php
<?php
class LocaleController extends Zend_Controller_Action
{
    // 手动覆盖区域的 action
    public function indexAction()
    {



// 如果是支持的区域，将其添加到 session

```
if (Zend_Validate::is(
    $this->getRequest()->getParam('locale'), 'InArray',
    array('haystack' => array('en_US', 'en_GB', 'de_DE', 'fr_FR'))
)) {
    $session = new Zend_Session_Namespace('square.l10n');
    $session->locale = $this->getRequest()->getParam('locale');
}

// 重定向到请求的 URL
$url = $this->getRequest()->getServer('HTTP_REFERER');
$this->_redirect($url);
```

**Q：翻译键应该使用小写吗？**

**A：** 并没有规定你必须仅对翻译键使用小写。这样做意味着你需要将应用程序视图中的`translate()`调用封装在`strtoupper()`和/或`ucfirst()`调用中，这是一项繁琐的工作。此外，不同的语言可能对同一个单词有不同的大小写要求，而在应用程序视图中应用大小写转换无法实现这一点。最后，如果`Zend_Translate`无法找到所选语言的翻译源，它将回退到显示键本身。因此，将翻译键限制为小写通常是不理想的。然而，你应该确保你的翻译键命名正确，以便它们能作为`Zend_Translate`可行的备选方案。

## 提问专家

第 9 章：理解应用程序本地化

307

将此文件保存为`$APP_DIR/application/modules/default/controllers/LocaleController.php`。

当`LocaleController::indexAction`被调用时，它首先获取引用脚本的 URL 并将其存储在本地变量中。然后，它查找 URL 请求中的`$_GET['locale']`参数，检查请求的区域是否支持，如果是，则将此区域存储在 session 中。最后，它将客户端重定向回引用脚本。

不过这只是谜题的一部分。现在有必要更新应用程序引导器（bootstrapper）并修改`_initLocale()`方法，首先检查 session 中是否存在区域标识，如果存在，则此区域的优先级高于自动检测的区域。以下是修订后的`_initLocale()`方法：

```php
<?php
class Bootstrap extends Zend_Application_Bootstrap_Bootstrap
{
    protected function _initLocale()
    {
        $session = new Zend_Session_Namespace('square.l10n');
        if ($session->locale) {
            $locale = new Zend_Locale($session->locale);
        }
        if ($locale === null) {
            try {
                $locale = new Zend_Locale('browser');
            } catch (Zend_Locale_Exception $e) {
                $locale = new Zend_Locale('en_GB');
            }
        }
        $registry = Zend_Registry::getInstance();
        $registry->set('Zend_Locale', $locale);
    }
}
```

## 更新主布局

最后一步是将一组旗帜图标添加到应用程序的主菜单中，并将其链接到`LocaleController::indexAction`。要完成此操作，请更新主布局，路径为`$APP_DIR/application/layouts/master.phtml`，更改已加粗高出：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
...
<div id="menu-locale-container">
    <div id="locale">
        <a href="<?php echo $this->url(array('module' => 'default',
        'controller' => 'locale', 'action' => 'index',
        'locale' => 'en_GB'), 'default', true); ?>">
            *(续上)*
            <img src="/images/locale/en_gb.gif" />
        </a>
        <a href="<?php echo $this->url(array('module' => 'default',
        'controller' => 'locale', 'action' => 'index',
        'locale' => 'en_US'), 'default', true); ?>">
            <img src="/images/locale/en_us.gif" />
        </a>
        <a href="<?php echo $this->url(array('module' => 'default',
        'controller' => 'locale', 'action' => 'index',
        'locale' => 'fr_FR'), 'default', true); ?>">
            <img src="/images/locale/fr_fr.gif" />
        </a>
        <a href="<?php echo $this->url(array('module' => 'default',
        'controller' => 'locale', 'action' => 'index',
        'locale' => 'de_DE'), 'default', true); ?>">
            <img src="/images/locale/de_de.gif" />
        </a>
    </div>
</div>
</html>
```

308

Zend Framework：初学者指南

309

## 总结

正如本章所示，Zend Framework 包含了完全本地化你的应用程序所需的一切。`Zend_Locale`组件提供了一个定义应用程序区域设置的框架，可以通过设计时的手动设置或运行时的自动检测来实现。在任何种情况下，其他 Framework 组件（如`Zend_Date`、`Zend_Currency`）都会相应调整它们的行为。任何本地化项目中最复杂的方面涉及将应用程序字符串翻译成不同的语言，此处 Zend Framework 也通过`Zend_Translate`提供了解决方案。`Zend_Translate`可以通过翻译助手自动集成到`Zend_View`。虽然在本书范围内无法进行完整的练习，但此练习仍然应该让你对该过程有一定的见解，并为未来的研究奠基础。

要了解更多本章讨论的话题，请参考以下链接：

- `Zend_Locale`组件，位于 http://framework.zend.com/manual/en/zend.locale
- `Zend_Date`组件，位于 http://framework.zend.com/manual/en/zend.date
- `Zend_Date`格式规范符，位于 http://framework.zend.com/manual/en/zend.date.constants
- `Zend_Currency`组件，位于 http://framework.zend.com/manual/en/zend.currency
- `Zend_Currency`汇率转换，位于 http://framework.zend.com/manual/en/zend.currency.exchange
- `Zend_Measure`组件，位于 http://framework.zend.com/manual/en/zend.measure
- `Zend_Translate`组件，位于 http://framework.zend.com/manual/en/zend.translate
- `Zend_Translate`翻译源目录布局，位于 http://framework.zend.com/manual/en/zend.translate.using
- GNU gettext 项目，位于 http://www.gnu.org/software/gettext/
- ISO 639 标准（语言代码），位于 http://www.iso.org/iso/support/faqs/widely_used_standards/widely_used_standards_other/language_codes.htm
- ISO 3166 标准（国家代码），位于 http://www.iso.org/iso/support/faqs/widely_used_standards/widely_used_standards_other/country_name_codes.htm

310

Zend Framework：初学者指南

- ISO 4217 标准（货币代码），位于 http://www.iso.org/iso/support/faqs/faqs_widely_used_standards/widely_used_standards_other/currency_codes.htm
- PEAR Services_ExchangeRates 软件包，位于 http://pear.php.net/package/Services_ExchangeRates/
- gedit 文本编辑器，位于 http://www.gnome.org/projects/gedit/
- Notepad2 文本编辑器，位于 http://www.flos-freeware.ch/notepad2.html
- 关于如何使用 Zend Framework 构建多语言网站的讨论（Jason Gilmore），位于 http://www.developer.com/design/article.php/3683571/Build-Multi-lingual-Websites-With-the-Zend-Framework.htm
- 关于使用 gettext 和 Zend Framework 进行字符串本地化的讨论（Peter Törnstrand），位于 http://www.tornstrand.com/2008/03/29/string-localization-with-gettext-and-zend-framework/

311

第 10 章：处理新闻订阅与 Web 服务

312

## 核心技能与概念

- 生成和读取 Atom 和 RSS 格式的新闻订阅
- 理解不同类型的 Web 服务架构
- 集成来自 Google、Amazon 和 Twitter 的搜索结果和数据
- 使用 SOAP 和 REST 访问第三方 Web 服务
- 实现一个简单的 REST API

如果你曾尝试过让两个（或多个）不同的 Web 应用程序和谐地工作，你可能已经知道这个过程是多么困难且令人沮丧。在 Web 的多平台、多语言世界中，在用不同编程语言编写的应用之间交换数据通常是实现真正的应用程序互操作性的最大障碍。

近年来，出现了一些试图解决此问题的技术和协议。Web 分布式数据交换 (WDDX)、简单对象访问协议 (SOAP)、极其简单聚合 (RSS)、Atom 聚合格式 (ASF) 等，为 Web 应用程序之间的数据交换提供了一个独立于语言和平台的框架。通常，这种交换通过 HTTP 进行，请求和响应使用 XML 变体进行往返传输。这些技术目前被广泛用于新闻订阅分发和 Web 服务实现。

Zend Framework 包含了许多在处理 Web 服务和新闻订阅时大有用处的组件。首先，`Zend_Feed`和`Zend_Feed_Reader`组件可以轻松创建、修改、解析和处理 RSS 和 Atom 格式的新闻订阅。接下来，`Zend_Rest_Client`组件允许访问现有的基于 REST 的 Web 服务，而`Zend_Rest_Controller`组件简化了实现新的基于 REST 的 Web 服务的任务。最后，一套全面的`Zend_Service`实现简化了与 Twitter、Technorati、Google 和 Flickr 等流行 Web 应用程序的集成。本章将详细检查所有这些组件。

## 处理新闻订阅

如果你拥有过自己的博客，你已经知道什么是新闻订阅（news feed）了。它是内容发布者在任何给定时间发布关于特定网站最新动态和有趣信息的一种方式。这些信息通常是按时间顺序排列的新闻标题和摘要列表，它们以机器可读的 XML 格式发布，可以被第三方网站或订阅阅读器应用程序解析。

Zend Framework 提供了几个帮助处理此类新闻订阅的组件。`Zend_Feed_Reader`组件提供了 API 来读取和解析两种最常见格式的订阅，而`Zend_Feed`组件则允许从原生 PHP 数据结构生成新订阅或修改现有订阅。接下来的章节将详细检查这些组件。

### 理解新闻订阅格式

通常，新闻订阅以极其简单聚合（RSS）格式或 Atom 聚合格式（ASF 或更常见的“Atom”）格式发布。这两种格式都是基于 XML 的，并包含一个标记的资源列表，每个资源都带有描述性信息，如标题、描述、URL 和日期。这两种格式还可以引用各种不同的资源类型，包括文档（通常是博客文章或新闻条目）、图像以及视频和音频流。

与 RSS 订阅一样，Atom 订阅包含关于其描述的资源的摘要信息；然而，Atom 订阅比 RSS 订阅稍微复杂，而且 Atom 聚合格式已被接受互联网工程任务组（IETF）的标准，这是 RSS 格式尚未比拟的成就。这些差异并非偶然：Atom 聚合格式于 2003 年构想，作为 RSS 格式的替代方案，而 RSS 格式最初由 Netscape Communications 在 1997 年初设计。自引入以来，RSS 格式经历了多次迭代和竞争性版本，而 Atom 格式被构想为一种新方法，其优势是不需要与现有订阅保持后兼容。

图 10-1 展示了 RSS 和 Atom 格式之间的相似之处（以及差异）。

### 获取新闻订阅

将新闻订阅集成到应用程序中最简单的方法是使用`Zend_Feed_Reader`，它为解析提供了一个简单的框架。正如示例所示，使用`Zend_Feed_Reader`获取新闻订阅的第一步是使用`import()`方法将其导入。该方法接受订阅的 URL，并根据导入的订阅类型返回`Zend_Feed_Reader_Feed_Rss`或`Zend_Feed_Reader_Feed_Atom`对象。该对象是访问订阅和条目数据的入口，并暴露了各种方法来访问订阅摘要信息。考虑以下示例，它展示了实际操作：

```php
// 订阅级别摘要
$this->view->feed = array(
    'title' => $feed->getTitle(),
    'description' => $feed->getDescription(),
    'url' => $feed->getLink(),
    'generator' => $feed->getGenerator(),
    'numEntries' => $feed->count()
);

// 订阅中的第一条目
$feed->rewind();
$entry = $feed->current();
$this->view->entries = array(
    array(
        'title' => $entry->getTitle(),
        'description' => $entry->getDescription(),
        'body' => $entry->getContent(),
        'url' => $entry->getLink(),
        'date' => $entry->getDateModified()
    )
);
```

```php
<?php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function feedAction()
    {
        // 从 URL 导入订阅
        $feed = Zend_Feed_Reader::import(
            'http://news.google.com/news?hl=en&output=rss');
        // ... 其他代码
    }
}
```

316

Zend Framework：初学者指南

```php
$feed = Zend_Feed_Reader::import(
    'http://news.google.com/news?hl=en&topic=w&output=rss');
```



# 第十章：处理新闻馈与 Web 服务

## 访问 Web 服务

近年来，将 Web 服务集成到应用程序中已变得常见。Google、Facebook、Twitter 和 Flickr 只是许多可用 Web 示例。要理解基本概念，我们首先需要定义什么是 Web 服务。Web 服务是一种允许不同应用程序在网络上进行通信的软件系统。这通常通过标准协议如 HTTP 或 SOAP 实现。

## 理解 Web 服务

将 Web 服务想象成一个远程 API，允许一个应用程序向另一个请求数据或功能。服务器处理请求并以结构化格式（如 XML 或 JSON）返回结果。实现 Web 服务的方法有很多，最流行的是 SOAP（简单对象访问协议）和 REST（表述状态转移）。

SOAP 是使用 XML 在应用程序之间交换信息的协议。它非常安全且可靠，但实现起来可能比较复杂。另一方面，REST 是一种使用标准 HTTP 方法通信的架构风格。它通常比 SOAP 更快、更容易实现，但安全性较低。

在在这两种情况下，Web 服务都允许不同的应用程序跨平台地进行通信。在本章中，我们将探索如何使用 Zend Framework 处理 Web 服务。

## 第 10 章：处理新闻源与 Web 服务

321

图 10-3

SOAP 和 REST 事务示例

![](img/222e7e58871b088cc6397852e1452b57_339_0.png)

322

Zend Framework：入门指南

另一方面，REST 模型摒弃了 WSDL 层次的复杂性，转而采用基于标准 HTTP 方法的更简单、更直观的接口，如前文所述。

REST 围绕着*资源*概念展开，而 SOAP 则使用基于*对象*和*方法*的接口。一个 SOAP 接口可以拥有可能在乎无限数量的方法；然而，REST 接口被限于四种可能的操作，对应于四个 HTTP “动词”。

### 消费 Web 服务

Zend Framework 包含了基于 REST 和 SOAP 的 Web 服务的通用客户端，以及许多特定服务的客户端实现，这些实现可直接与流行的 Web 服务进行通信。接下来的章节将详细介绍这些方面的内容。

### 使用特定服务的客户端实现

Zend Framework 包含了许多针对流行 Web 服务的预配置客户端，例如由 Google、Amazon、Flickr、Technorati 等提供的服务。使用这些特定服务的客户端实现，可以减少将这些服务的数据集成到 Web 应用程序中所需的时间和精力。在大多数情况下，这些实现提供了一个面向对象的 API，服务响应以原生 PHP 对象或数组的形式返回。

表 10-1 列出了目前 Zend Framework 中包含的特定服务实现。

虽然在这一章的有限范围内，无法对这些实现中的每一个一个进行完整描述，但几个示例将具有说明性。考虑以下：

**Q：如果我正在构建一个 Web 服务，我应该使用 SOAP 还是 REST？答：** 与所有此类问题一样，答案实际上取决于你的需求和目标。对于事务型服务或电子商务服务，或者在服务作为更大分布式平台一部分的情况下，SOAP 的严格数据类型和正式的服务描述通常使其成为比 REST 更好的选择。另一方面，如果你的目标仅仅是实现对应用程序内部的快速且粗略的访问，并将易用性和格式灵活性作为你选择的关键因素，那么 REST 可能是更好的选项。尽管如此，值得注意的是，REST 方法在流行度上正逐渐超越 SOAP 方法，这既因为它巧妙地利用了现有技术，也因为它在使用和理解上要简单得多。

**专家问**

323

第 10 章：处理新闻源与 Web 服务

列表，它使用`Zend_Service_Delicious`组件检索用户在 del.icio.us 服务上的标签和书签列表：

```php
<?php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function deliciousAction()
    {
        // 初始化服务对象
        $client = new Zend_Service_Delicious('username', 'password');
        // 获取用户创建的所有标签频率
        $this->view->tags = $client->getTags();
        // 获取所有标记为 PHP 的帖子
        $this->view->posts = $client->getPosts('php');
    }
}
```

| 客户端类 | 说明 |

| :--- | :--- |

| `Zend_Service_Akismet` | 用于 Akismet 垃圾邮件拦截程序的客户端 |

| `Zend_Service_Amazon` | Amazon Web Services API 的客户端，针对 Amazon EC2、Amazon SQS 和 Amazon S3 有特定实现 |

| `Zend_Service_AudioScrobbler` | 用于 Last.fm 音乐搜索引擎的客户端 |

| `Zend_Service_Delicious` | 用于 del.icio.us 社交书签应用的客户端 |

| `Zend_Service_Flickr` | 用于 Flickr 照片共享应用的客户端 |

| `Zend_Service_Nirvanix` | 用于 Nirvanix 数据存储应用的客户端 |

| `Zend_Service_ReCaptcha` | 用于 ReCaptcha CAPTCHA 生成器的客户端 |

| `Zend_Service_Simpy` | 用于 Simpy 社交书签应用的客户端 |

| `Zend_Service_SlideShare` | 用于 SlideShare 演示文共享应用的客户端 |

| `Zend_Service_StrikeIron` | 用于 StrikeIron 商业数据库聚合器的客户端 |

| `Zend_Service_Technorati` | Technorati 博客搜索引擎的客户端 |

| `Zend_Service_Twitter` | Twitter 微微博服务的客户端 |

| `Zend_Service_Yahoo` | Yahoo! 搜索 APIs 的客户端 |

| `Zend_Gdata` | Google Data APIs 的客户端，针对 Notebook、Calendar、YouTube、Base、Spreadsheets 和 Documents 等 Google 应用有特定实现 |

表 10-1：Zend Framework 包含的 Web 服务客户端实现

324

Zend Framework：入门指南

这是另一个示例，这次使用`Zend_Gdata`组件查询 YouTube 服务以获取当前最五个热门视频的列表：

```php
<?php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function youtubeAction()
    {
        // 初始化服务对象
        $client = new Zend_Gdata_YouTube();
        // 获取五个热门视频的馈
        $feed = $client->getVideoFeed(
            'http://gdata.youtube.com/feeds/api/standardfeeds/most_popular?max-results=5');
        // 处理馈并获取单个条目
        // 对于每个条目，获取标题、类别、评分、视图计数和 URL
        $this->view->mostViewed = array();
        foreach ($feed as $entry) {
            // ... (逻辑在示例中截断)
        }
    }
}
```

*(注：原文示例代码块逻辑此处不完整，已按要求不翻译代码内容并保持结构)*

在此示例中，`getVideoFeed()` 方法返回一个 Atom 馈；该馈被解析并转换为`Zend_Gdata_Entry`对象的数组，每个对象代表一个条目。现在遍历此数组、提取属性并将其表示为 页面是很简单的。

最后，这里有一个使用`Zend_Service_Amazon`实现按特定作者搜索 Amazon 的示例：

325

第 10 章：处理新闻源与 Web 服务

// 获取底层 XPath 对象

`$xpath = $feed->getXpath();`

// 查询所有项目的标题列表

`$titles = $xpath->query('//item/title');`

// 返回列表中的第三项

`$this->view->title = $titles->item(2)->nodeValue;`

}

}

***注意***

你也可以从文件或字符串导入新闻馈送，分别使用`Zend_Feed_Reader::importFile()`和`Zend_Feed_Reader::importString()`方法。

除了`Zend_Feed_Reader`之外，Zend Framework 还包含了`Zend_Feed`组件，它为馈（feed）的生成和修改提供了全面的 API。

虽然`Zend_Feed`也可以用于解析馈，但`Zend_Feed_Reader`通常是更好的替代方案，因为它的 API 更简单，并且能够自动检测馈类型。尽管如此，为了完整起见，这里包含了一个使用`Zend_Feed`消费 RSS 馈的示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function feedAction()
    {
        // 从 URL 导入馈
        $feed = Zend_Feed::import(
            'http://news.google.com/news?hl=en&topic=w&output=rss');
        // 获取馈层面的摘要元素
        $this->view->feed = array(
            'title' => $feed->title(),
            'description' => $feed->description(),
            'url' => $feed->link(),
            'generator' => $feed->generator(),
            'numEntries' => $feed->count()
        );

        // 获取馈中的第一个项目
        $feed->rewind();
        $entry = $feed->current();
        $this->view->entries = array(
            array(
                'title' => $entry->title(),
                'description' => $entry->description(),
                'url' => $entry->link(),
                'date' => $entry->pubDate()
            )
        );
    }
}
```

当使用`Zend_Feed`时，单个馈级别和项目层级元素的内容是通过`$object->method`语法访问的，其中方法名与元素名对应。例如，`$feed->title()`获取馈`<title>`元素的内容，而`$entry->description()`则获取项目`<description>`元素的内容。

## 创建新闻馈

这样就处理了读取现有馈的问题。现在，如何创建新的馈呢？

创建一个新馈非常简单，且最易实现的方法是使用`Zend_Feed`。要实现这一点，只需向`Zend_Feed::importArray`方法传递一个馈的数组表示以及所需的输出格式（RSS 或 Atom），它将生成一个符合指定格式且经过正确编码的馈，适用于任何符合标准的馈阅读器。这里有一个示例，它展示了如何通过从数据库结果集构建一个 Atom 馈：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function feedAction()
    {
        // 查询最近的 10 篇文章
        $q = Doctrine_Query::create()
            ->from('App_Model_Posts p')
            ->where('p.status = 1')
            ->orderBy('p.date desc')
            ->limit(10);
        $result = $q->fetchArray();

        // 生成输出数组
        // 设置馈层级元素
        $output = array(
            'title' => 'Newest posts on melonfire.com/trog',
            'link' => 'http://www.melonfire.com/community/columns/trog/',
            'author' => 'Melonfire Feed Generator/1.0',
            'charset' => 'UTF-8',
            'entries' => array()
        );

        // 遍历结果集
        // 将项目层级元素设置为嵌套数组
        foreach ($result as $r) {
            $entry = array(
                'title' => $r['title'],
                'link' => 'http://www.melonfire.com/community/columns/trog/'.$r['id'],
                'description' => $r['abstract'],
                'lastUpdate' => strtotime($r['date']),
            );
            $output['entries'][] = $entry;
        }

        // 将数组导入 Zend_Feed 并转换为 Atom 馈
        $feed = Zend_Feed::importArray($output, 'atom');

        // 禁用布局和视图渲染
        $this->_helper->layout->disableLayout();
        $this->getHelper('viewRenderer')->setNoRender(true);

        // 将馈发送到客户端
        $feed->send();
        exit();
    }
}
```

***提示***

`Zend_Feed::send()`方法会设置它自己的头部信息，因此如果这不是你想要的，或者你想设置自定义的头部信息，请考虑使用`header()`手动设置头部，然后使用`saveXml()`方法将馈 XML 发送给请求客户端。

上一个列表首先构建了一个包含馈和项目内容的嵌套数组，然后将此数组传递给`Zend_Feed::importArray`方法以转换为 Atom 馈。该方法的返回值是一个`Zend_Feed_Atom`对象，它暴露了两个非常有用的方法：`send()`和`saveXml()`。`send()`方法带有正确的 HTTP 头部将馈发送到客户端，而`saveXml()`方法返回馈的 XML。

***注意***

新版本的 Framework 还包含了`Zend_Feed`组件，它为馈的生成和修改提供了全面的 API。虽然`Zend_Feed`也可以用于解析馈，但`Zend_Feed_Reader`通常是更好的替代方案，因为它的 API 更简单，并且能够自动检测馈类型。尽管如此，为了完整起见，这里包含了一个使用`Zend_Feed`消费 RSS 馈的示例：



```php
<?php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function amazonAction()
    {
        // 初始化服务对象
        $client = new Zend_Service_Amazon('ACCESS-KEY', 'US', 'SECRET-KEY');
        // 按属性搜索 Amazon.com 的项目
        $items = $client->itemSearch(array(
            'SearchIndex' => 'Books',
            'Author' => 'Dan Brown',
            'ResponseGroup' => 'Large'
        ));
        // 处理搜索结果
        $this->view->results = array();
        foreach ($items as $i) {
            $this->view->results[] = array(
                // 属性映射
            );
        }
    }
}
```

在这里，服务对象的`itemSearch()`方法查询 Amazon Web 服务以获取匹配参数的项目列表，并返回`Zend_Service_Amazon_Item`对象数组，每个对象包含相应项目的信息。遍历此数组并提取相关信息进行展示是非常简单的。

### 使用通用实现

如果你尝试访问一个没有预定义服务实现的 Web 服务，不要灰心：Zend Framework 也包含了用于访问此类服务的通用 SOAP 和 REST 客户端。这些客户端分别实现在`Zend_Soap_Client`和`Zend_Rest_Client`组件中。

为了演示用法，请考虑以下示例，它使用通用的 SOAP 客户端访问 GeoCoder Web 服务并返回对应特定地址的经纬度：

```php
<?php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function soapAction()
    {
        // 初始化 SOAP 客户端
        $soap = new Zend_Soap_Client(
            'http://geocoder.us/dist/eg/clients/GeoCoderPHP.wsdl', array(
                'soap_version' => SOAP_1_1,
                'compression' => SOAP_COMPRESSION_ACCEPT
            ));
    }
}
```

326

Zend Framework：学者指南

```php
// 获取地址的经纬度结果

$response = $soap->geocode('E Capitol St NE & 1st St NE, Washington, DC');

$this->view->results = array();

foreach ($response as $r) {
    $this->view->results[] = array(
        'zip' => $r->zip,
        'latitude' => $r->lat,
        'longitude' => $r->long
    );
}

// 获取用于调试的 SOAP 请求和响应

$this->view->request = $soap->getLastRequest();
$this->view->response = $soap->getLastResponse();

}

}
}
```

此示例创建了一个新的`Zend_Soap_Client`对象，并使用 Web 服务 WSDL 文件的 URL 对其进行实例化。正如之前讨论的，WSDL 文件允许客户端自动获取可用方法、预期的数据类型以及输入输出参数的内容。对象构造函数的第二个参数是一个配置选项数组，可用于定义客户端行为的各个方面。

**注意**

也可以通过省略 WSDL URL，并直接在选项数组中指定 SOAP 服务 URL（*端点*）作为参数，以非 WSDL 模式使用`Zend_Soap_Client`。

一旦实例化了`Zend_Soap_Client`对象，就可以通过调用相应的对象方法来代理访问远程服务方法。`Zend_Soap_Client`对象会自动创建 SOAP 消息包、通过 POST 发送到服务器、接收响应包并将响应包解码为原生的 PHP`Zend_Soap_Client_Response`对象。这在之前的示例中可见，该示例调用了服务的`geocode()`方法，向其传递了一个地址字符串（实际上是华盛顿特区美国国会大地址），并从响应中检索邮政编码、纬度和经度。

**警告**

`Zend_Soap_Client`组件使用了 PHP 的`ext/soap`扩展，如果你的 PHP 环境没有包含此扩展，它将无法运行。

同样地，可以使用`Zend_Rest_Client`实现以通用且一致的方式访问基于 REST 的 Web 服务。考虑下一个示例，它通过尝试访问 GeoNames REST 服务来获取国家信息：

327

第 10 章：处理新闻订阅和 Web 服务

```php

<?php

class Sandbox_ExampleController extends Zend_Controller_Action

{

    public function restAction()

    {

        // 初始化 REST 

        $client = new Zend_Rest_Client('http://ws.geonames.org/countryInfo');

        // 设置参数

        $client->country('IN');

        // 为国家信息发送 GET 请求

        // 解析结果

        $result = $client->get();

        $this->view->countryName = $result->countryName();

        $this->view->countryCode = $result->countryCode();

        $this->view->capital = $result->capital();

        $this->view->areaKM = $result->areaInSqKm();

        $this->view->population = $result->population();

        $this->view->languages = $result->languages();

        $this->view->mapCoordinates = array(

            $result->bBoxWest(),

            $result->bBoxEast(),

            $result->bBoxNorth(),

            $result->bBoxSouth()

        );

        // 获取用于调试的 REST 请求和响应

        $this->view->request = $client->getLastRequest();

        $this->view->response = $client->getLastResponse();

    }

}

```

与之前一样，第一步是通过创建`Zend_Rest_Client`对象的实例并将 REST 服务 URL 传递给对象构造函数来初始化 REST 客户端。参数使用流式接口指定，该接口将参数名代理到对象方法，实际的请求传输通过`get()`、`post()`、`put()`或`delete()`方法执行，这些方法在内部被翻译为相应的 HTTP 方法。这在之前的代码列表中清晰可见的，该列表为 GeoNames 国家信息服务构建了一个 GET 请求，并将印度国家代码作为参数传递给它：`http://ws.geonames.org/countryInfo?country=IN`。

`Zend_Rest_Client`请求的响应以`Zend_Rest_Client_Response`对象实例的形式呈现，通常表示为 SimpleXML 对象或对象数组。响应的单个元素可以通过 SimpleXML 语法访问，也可以通过直接将元素名作为方法进行访问。在后一种方法下，将使用 XPath 查询来返回所有匹配的元素，无论它们在 XML 文档树中的层次位置如何。

28

Zend Framework：学者指南

正如这两个示例所示，Zend Framework 能够轻松访问任何基于 SOAP 或 REST 的 Web 服务，即使尚不存在针对特定服务的实现，且不需要深入了解服务的内部机制。这使其成为快速高效地将第三方 Web 服务集成到 PHP 中的宝贵工具。

**提示**

注意前两个代码列表中的`getLastRequest()`和`getLastResponse()`方法。这些方法对于调试 SOAP 和 REST 事务，以及验证请求和响应包的内容非常有用。

## 集成 Twitter 和博客搜索结果

在有了这些背景信息后，让我们看看它们在现实世界中是如何运作的。接下来的章节将说明如何结合前述节讨论的组件，在 SQUARE 示例应用程序中显示与“集邮”主题相关的最新新闻、博客文章和 Twitter 更新。

## 定义自定义路由

第一步一如既往是定义一个自定义路由。编辑应用程序配置文件`$APP_DIR/application/application.ini`，添加以下路由定义：

```ini

resources.routes.news.route = /news

resources.routes.news.defaults.module = default

resources.routes.news.defaults.controller = news

resources.routes.news.defaults.action = index

```

## 定义控制器和视图

下一步是定义新闻界面的 action 和视图。以下是`NewsController`的代码，它应保存为`$APP_DIR/application/modules/default/controllers/NewsController.php`:

```php

<?php

class NewsController extends Zend_Controller_Action

{

    public function indexAction()

    {

        // 获取 Twitter 订阅

        $q = 'philately';

        $this->view->q = $q;

        $twitter = new Zend_Service_Twitter_Search();

        $this->view->tweets = $twitter->search($q,

        array('lang' => 'en', 'rpp' => 8, 'show_user' => true));

329

第 10 章：处理新闻订阅和 Web 服务

```php
        // 获取 Google 新闻
        $this->view->feeds = array();
        $gnewsFeed = "http://news.google.com/news?hl=en&q=$q&output=atom";
        $this->view->feeds[0] = Zend_Feed_Reader::import($gnewsFeed);

        // 获取 BPMA RSS 订阅
        $bpmaFeed = "http://www.postalheritage.org.uk/news/RSS";
        $this->view->feeds[1] = Zend_Feed_Reader::import($bpmaFeed);
    }
}
```

`indexAction()`方法负责访问和导入各种新闻订阅。`Zend_Service_Twitter`实现允许搜索包含“集邮”单词的最新状态更新。该对象的`search()`方法接受查询词和一个选项数组，指定语言过滤器、返回的结果数量以及每个结果条目是否包含源用户名。该方法的返回值为匹配搜索词的嵌套数组，随后将其到视图中进行进一步处理。

`Zend_Feed_Reader`实现用于导入两个新闻订阅。第一个是来自 Google News 的“集邮”相关的最新标题 Atom 订阅，第二个是英国邮政博物馆档案馆（BPMA）博客的最新帖子列表。生成的订阅对象随后赋值为视图变量。

以下是对应的视图脚本，它应保存为`$APP_DIR/application/modules/default/views/scripts/news/index.phtml`:

```html
<h2>新闻</h2>
<div id="newsfeeds">
    <div id="posts">
        <strong>关于
        <a href="http://news.google.com/news?hl=en&q=<?php echo $this->q; ?>">
        '<?php echo $this->q; ?>'
        </a>的最新新闻：</strong>
        <p id="hdiv"></p>
        <?php $count = 0; ?>
        <?php foreach ($this->feeds[0] as $entry):?>
        <?php if ($count >= 5) break; ?>
        <p class="post">
            <span class="text">
```*(continued)*

330

Zend Framework：入门指南

<a href="<?php echo $entry->getLink(); ?>">

<?php echo $entry->getTitle(); ?>

</a>

</span

<span class="time">

<?php echo $entry->getDateModified(); ?>

</span>

</p>

<?php $count++; ?>

<?php endforeach; ?>

<p style="padding-top: 4px"/>

<strong>来自 

<a href="http://www.postalheritage.org.uk/">

英国邮政博物馆与档案馆

</a> 博客的最新文章：

</strong>

<p id="hdiv"></p>

<?php $count = 0; ?>

<?php foreach ($this->feeds[1] as $entry):?>

<?php if ($count >= 5) break; ?>

<p class="post">

<span class="text">

<a href="<?php echo $entry->getLink(); ?>">

<?php echo $entry->getTitle(); ?>

</a>

</span>

<span class="time">

<?php echo $entry->getDateModified(); ?>

</span>

</p>

<?php $count++; ?>

<?php endforeach; ?>

</div

<div id="tweets">

<strong>关于 

<a href="http://search.twitter.com/search?q=<?php echo $this->q; ?>">

'<?php echo $this->q; ?>'

</a> 的最新推文：

</strong>

<?php foreach ($this->tweets['results'] as $tweet):?>

<p class="tweet">

<span class="image">

<img src="<?php echo $tweet['profile_image_url']; ?>" />

</span>

<span class="user">

<?php echo $tweet['from_user'] . ': '; ?>

</span>

<span class="text">

PAGE 349

第 10 章：

处理新闻 流与 Web 服务

331

<?php echo $tweet['text']; ?>

</span>

<span class="time">

<?php echo $tweet['created_at']; ?>

</span>

</p>

<?php endforeach; ?>

</div>

</div

这里并没有复杂的复杂的。视图脚本仅仅遍历了控制器中分配的结果对象，从每个对象中提取必要信息，并将其以整洁的双列布局显示出来。

### 更新主布局 (Master Layout)



剩下的工作是更新`$APP_DIR/application/layouts/master.phtml`中的主布局，以便在主菜单中显示指向新闻页的链接。布局的修订在下面的列表中以**粗体**形式显示：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<div id="menu-locale-container">
<div id="menu">
...
**<a href="<?php echo $this->url(array(), 'news'); ?>">**
**<?php echo $this->translate('menu-news'); ?>**
**</a>**
... </div>
</div>
...
</html>
```

**注意**

请记住，正如第 9 章中讨论的那样，你需要为每个支持的语言的翻译源文件为新菜单项添加翻译字符串。

本章的代码存档可以从`http://www-zf-beginners-guide.com/`下载，其中包含了必要的添加。

要查看效果，请在浏览器中访问 URL`http://square.localhost/news`，你应该能类似图 10-4 的内容。

（（续）

PAGE 350

332

Zend Framework：入门指南

## 创建基于 REST 的 Web 服务

除了为访问和集成新闻流以及 Web 服务到 PHP 应用程序提供全面的工具集外，Zend Framework 还通过构建自己的基于 REST 的 Web 服务来轻松暴露应用程序功能。这通常通过后续章节讨论的`Zend_Rest_Route`和`Zend_Rest_Controller`组件来实现。

### 理解 REST 路由

基于 REST 的架构有两个核心原则：

- 应用程序由多个资源组成，每个资源都可以通过唯一的 URL 访问。

- 用于访问资源的方法决定了对该资源要执行的操作。

**图 10-4**

动态检索并整合博客、新闻和 Twitter 搜索结果

PAGE 351

第 10 章：

处理新闻 流与 Web 服务

333

表 10-2 展示了基于 REST 服务的典型 URL 路由。

从表 10-2 可以清楚地看到，在 REST 模型下，现有的 HTTP 动词例如 GET（获取数据）、POST（创建数据）、PUT（更新数据）和 DELETE（删除数据），指示了对指定资源要执行的操作。需要时，请求 URL 中包含一个唯一的资源标识符。任何额外的参数（特别是在创建新资源或更新现有资源时）都会在 POST 或 PUT 请求体中传递。

Zend Framework 包含一个`Zend_Rest_Route`组件，它可以为整个应用程序、特定模块或特定控制器自动启用这些标准的 REST 路由。在匹配 URL 请求时，该组件将自动识别请求方法、检查请求并调用其中之一。

| 请求 URL | 请求方法 | 描述 |

| :--- | :--- | :--- |

| `/api/items` | GET | 获取所有项目 |

| `/api/items/:id` | GET | 获取项目记录 |

| `/api/items` | POST | 添加新项目 |

| `/api/items/:id` | PUT | 更新项目记录 |

| `/api/items/:id` | DELETE | 删除项目记录 |

**表 10-2：标准 REST 路由**

Zend Framework 包含一个`Zend_Rest_Route`组件，它可以为整个应用程序、特定模块或特定控制器自动启用这些标准的 REST 路由。在匹配 URL 请求时，该组件将自动识别请求方法、检查请求并调用其中之一。

标准 REST 路由（表 10-2）

- 请求 URL | 方法 | 描述

- `/api/items` | GET | 获取所有项目

- `/api/items/:id` | GET | 获取项目记录

- `/api/items` | POST | 添加新项目

- `/api/items/:id` | PUT | 更新项目记录

- `/api/items/:id` | DELETE | 删除项目记录

PAGE 352

334

Zend Framework：入门指南

## 实现基于 REST 的服务

从前面的节可以清楚地看到，为应用程序采用 REST 架构（特别是带有标准的 CRUD 操作时）涉及两个本质组件：

1. 一个继承自`Zend_Rest_Controller`并实现其所有抽象方法的控制器；

2. 一个使用`Zend_Rest_Route`将传入的 URL 请求与上述控制器匹配的路由。

理解其如何运作的最佳方法是使用示例。接下来的章节通过为 SQUARE 应用构建一个简单的基于 REST 的 API 来说明这一点。此 API 将支持 GET 和 POST 方法，并允许用户检索现有项目以及发布新项目。标准 REST 路由（等等，表格实际上在文中，让我重新格式化）：

| 请求 URL | 请求方法 | 描述 |

| :--- | :--- | :--- |

| `/api/items` | GET | 获取所有项目 |

| `/api/items/:id` | GET | 获取项目记录 |

| `/api/items` | POST | 添加新项目 |

| `/api/items/:id` | PUT | 更新项目记录 |

| `/api/items/:id` | DELETE | 删除项目记录 |

### 创建模块

第一步创建一个新模块（将其命名为“api”）以存放 REST 控制器。要这样做，请切换到`$APP_DIR/application/**`并执行以下命令：

```bash
mkdir modules/api
mkdir modules/api/controllers
mkdir modules/api/views
mkdir modules/api/views/scripts
```

### 定义控制器

下一步是定义 API 控制器，它将处理所有 REST 请求。如之前所述，该控制器应该继承抽象的`Zend_Rest_Controller`并实现其所有抽象方法。如下如下：

```php
<?php
class Api_CatalogController extends Zend_Rest_Controller
{
    // 禁用布局和渲染
    public function init()
    {
        $this->apiBaseUrl = 'http://square.localhost/api/catalog';
        $this->_helper->layout->disableLayout();
        $this->getHelper('viewRenderer')->setRender(true);
    }

    public function indexAction()
    {
        // 处理 GET 请求
    }

    public function getAction()
    {
        // 处理 GET 请求
    }

    public function postAction()
    {
        // 处理 POST 请求
    }

    public function putAction()
    {
        // 处理 PUT 请求
    }

    public function deleteAction()
    {
        // 处理 DELETE 请求
    }
}
```

（等等，OCR 文本在末处有些混乱，让我根据提供的文本提供一个干净的版本。）

## Zend Framework：初学者指南

### 定义 GET Action

接下来，让我们来定义`Api_CatalogController::indexAction`。你可能记得，当路由器遇到不带“id”请求变量的 GET 请求时，该 action 会被自动分发，并且应该返回所有匹配资源的列表。以下是代码：

```php
<?php

class Api_CatalogController extends Zend_Rest_Controller
{
    public function indexAction()
    {
        // 从数据库获取记录
        $q = Doctrine_Query::create()
            ->from('Square_Model_Item i')
            ->leftJoin('i.Square_Model_Country c')
            ->leftJoin('i.Square_Model_Grade g')
            ->leftJoin('i.Square_Model_Type t')
            ->addWhere('i.DisplayStatus = 1');

        $result = $q->fetchArray();

        // 设置 feed 元素
        $output = array(
            'title' => 'Catalog records',
            'link' => $this->apiBaseUrl,
            'author' => 'Square API/1.0',
            'charset' => 'UTF-8',
            'entries' => array()
        );

        // 设置 entry 元素
        foreach ($result as $r) {
            $output['entries'][] = array(
                'title' => $r['Title'] . ' - ' . $r['Year'],
                'link' => $this->apiBaseUrl . '/' . $r['RecordID'],
                'description' => $r['Description'],
                'lastUpdate' => strtotime($r['RecordDate']),
                'square:title' => $r['Title']
            );
        }

        // 将数组导入 atom feed
        // 发送给客户端
        $feed = Zend_Feed::importArray($output, 'atom');
        $feed->send();
        exit;
    }

    // 转发到 indexAction
    public function listAction() {
        return $this->_forward('index');
    }
}
```

`Api_CatalogController::indexAction`首先执行一个 Doctrine 查询以获取所有活跃项目的列表。然后，它遍历结果集，将其转换为嵌套数组，以便使用`Zend_Feed::importArray`转换为 Atom feed。随后，使用 feed 的`send()`方法将此 Atom feed 返回客户端。

**注意**：Zend Framework v1.9 及早期版本包含一个 bug，导致路由器尝试将针对`indexAction()`的 REST 请求委托给`listAction()`而不是它。之前的列表说明了解决此 bug 的简单变通方法：只需使用`forward()`方法即可。当路由器遇到带有“id”变量的 GET 请求时，`Api_CatalogController::getAction`会被自动分发，这表示请求特定的资源。在这种情况下，action 必须从数据库中检索指定的目录记录，并向请求的客户端返回其详细信息。以下是代码：

```php
<?php

class Api_CatalogController extends Zend_Rest_Controller
{
    public function getAction()
    {
        // 从数据库获取记录
        $id = $this->_getParam('id');
        $q = Doctrine_Query::create()
            ->from('Square_Model_Item i')
            ->leftJoin('i.Square_Model_Country c')
            ->leftJoin('i.Square_Model_Grade g')
            ->leftJoin('i.Square_Model_Type t')
            ->where('i.RecordID = ?', $id)
            ->addWhere('i.DisplayStatus = 1');

        $result = $q->fetchArray();

        // 如果记录可用
        if (count($result) == 1) {
            // 设置 feed 元素
            $output = array(
                'title' => 'Catalog record for item: ' . $id,
                'link' => $this->apiBaseUrl . '/' . $id,
                'author' => 'Square API/1.0',
                'charset' => 'UTF-8',
                'entries' => array()
            );

            $output['entries'][0] = array(
                'title' => $result[0]['Title'] . ' - ' . $result[0]['Year'],
                'link' => $this->apiBaseUrl . '/' . $id,
                'description' => $result[0]['Description'],
                'lastUpdate' => strtotime($result[0]['RecordDate'])
            );

            // 将数组导入 atom feed
            $feed = Zend_Feed::importArray($output, 'atom');
            Zend_Feed::registerNamespace('square', 'http://square.localhost');

            // 设置自定义命名空间元素
            $feed->rewind();
            $entry = $feed->current();
            if ($entry) {
                $entry->{'square:id'} = $result[0]['RecordID'];
                $entry->{'square:title'} = $result[0]['Title'];
                $entry->{'square:year'} = $result[0]['Year'];
                $entry->{'square:grade'} = $result[0]['Square_Model_Grade']['GradeName'];
                $entry->{'square:description'} = $result[0]['Description'];
                $entry->{'square:country'} = $result[0]['Square_Model_Country']['CountryName'];
                $entry->{'square:price'} = null;
                $entry->{'square:price'}->{'square:min'} = $result[0]['SalePriceMin'];
                $entry->{'square:price'}->{'square:max'} = $result[0]['SalePriceMax'];
            }

            // 导出到客户端
            $feed->send();
            exit;
        } else {
            $this->getResponse()->setStatusCode(404);
            echo 'Invalid identifier';
            exit;
        }
    }
}
```

### 定义 POST Action



`Api_CatalogController::postAction()` 在路由器遇到 POST 请求时会被自动分发。按照 REST 约定，此类请求将创建一个资源。以下是代码：

```php
<?php

class Api_CatalogController extends Zend_Rest_Controller
{
    public function postAction()
    {
        // 读取 POST 参数并保存到数据库
        $item = new Square_Model_Item;
        $item->fromArray($this->getRequest()->Post());
        $item->RecordDate = date('Y-m-d', mktime());
        $item->DisplayStatus = 0;
        $item->DisplayUntil = null;
        $item->save();
        $id = $item->RecordID;

        // 设置响应为 201
        // 发送新创建记录的 ID
        $this->getResponse()->setStatusCode(201);
        $this->getResponse()->setHeader('Location', $this->apiBaseUrl.'/'.$id);
        echo $this->apiBaseUrl.'/'.$id;
        exit;
    }
}
```

### 初始化 REST 路由

最后一步是初始化 REST 路由。为了完成此操作，打开应用程序启动程序并向其中添加以下方法：

```php
<?php

class Bootstrap extends Zend_Application_Bootstrap
{
    protected function _initRoutes()
    {
        $front = Zend_Controller_Front::getInstance();
        $router = $front->getRouter();
        $restRoute = new Zend_Rest_Route($front, array(), array('api'));
        $router->addRoute('api', $restRoute);
    }
}
```

此时，你的 REST API 已经运行。你可以通过在浏览器中请求`http://square.localhost/api/catalog`来测试它，它应该产生一个来自目录目录数据库活跃列表的 Atom feed。图 10-5 展示了输出内容。

同样地，访问带有额外项目标识符的相同 URL（例如`http://square.localhost/api/catalog/1`）将生成包含请求项目详情的 Atom feed。图 10-6 展示了此类 feed 可能的样子。

342

Zend Framework：入门指南

图 10-7

POST 请求的 API 响应

![](img/222e7e58871b088cc6397852e1452b57_360_0.png)

最后，向 URL`http://square.localhost/api/catalog`POST 一个数据数组，将在数据库中创建一个新的条目记录，并向客户端返回该条目的 URL 引用（见图 10-7）。

### 总结

大多数博客和新闻网站都包含 RSS 或 Atom 馈送，这些馈送可以用于将新内容分发到第三方应用程序。编写解析器来消耗这些新闻馈送是一项常见的应用开发任务，而 Zend Framework 通过提供一组预定义的组件，用于生成、修改和解析新闻馈送，简化了这一过程。本章详细讨论了这些组件，并说明了如何使用它们将来自在线新闻源的馈送集成到 SQUARE 示例应用程序中。

通过允许第三方访问应用程序的功能，Web 服务实现了一系列新的“混搭”（mashups）和衍生产品，这些产品整合了来自多个不同源的数据，同时鼓励了技术创新。Zend Framework 让人们轻松跟上 Web 服务的潮流：它包含了用于 REST 和 SOAP 访问的通用客户端，以及由 Google、Amazon 和 Twitter 等流行应用程序暴露的 Web 服务的现有实现。本章演示了这些实现中的一些，还说明了如何使用 SQUARE 示例应用程序从头创建一个基于 REST 的 Web 服务的基础。

要了解更多关于本章讨论的话题，请考虑访问以下链接：

- `Zend_Feed_Reader`组件，位于：
  - http://framework.zend.com/manual/en/zend.feed.reader.html

- `Zend_Feed`组件，位于：
  - http://framework.zend.com/manual/en/zend.feed.html

- `Zend_Rest_Client`组件，位于：
  - http://framework.zend.com/manual/en/zend.rest.client.html

- `Zend_Soap_Client`组件，位于：
  - http://framework.zend.com/manual/en/zend.soap.client.html

- `Zend_Service`组件，位于：
  - http://framework.zend.com/manual/en/zend.service.html

- `Zend_Gdata`组件，位于：
  - http://framework.zend.com/manual/en/zend.gdata.html

- Atom 馈送格式 1.0 规范，位于：
  - http://tools.ietf.org/html/rfc4287

- Wikipedia 对 RSS 格式的讨论，位于：
  - http://en.wikipedia.org/wiki/RSS

- Wikipedia 对 SOAP 和 REST 架构的讨论，位于：
  - http://en.wikipedia.org/wiki/Web_service

- 关于 REST 与 SOAP 服务的讨论（Amit Asaravala），位于：
  - http://www.devx.com/DevX/Article/8155

- 关于使用 Zend Framework 构建基于 REST 的接口的讨论（Matthew Weier O’Phinney），位于：
  - http://weierophinney.net/matthew/archives/228-Building-RESTful-Services-with-Zend-Framework.html

- 编写基于 REST 的 Web 服务和客户端的视频演示（Jon Lebensold），位于：
  - http://www.zendcasts.com/writing-a-restful-web-service-and-client-with-zend_controller-and-zend_httpclient/2009/04/

- 一种（非框架）构建 REST API 的方法（Ian Selby），位于：
  - http://www.gen-x-design.com/archives/create-a-rest-api-with-php/

- HTTP 响应码的一些示例以及如何用于基于 REST 的 Zend Framework 应用程序（Sudheer Satyanarayana），位于：
  - http://techchorus.net/create-restful-applications-using-zend-framework-part-ii-using-http-response-code

![](img/222e7e58871b088cc6397852e1452b57_363_0.png)

345

第 11 章

处理用户界面元素

346

Zend Framework：入门指南

## 关键工具与概念

- 通过菜单、站点地图和面包屑导航改进网站导航
- 了解 Zend Framework 的 Dojo 集成
- 创建启用 AJAX 的自动补全表单输入
- 在 Zend Framework 中使用 YUI Library 组件
- 理解如何创建和使用操作助手（action helpers）

将 Web 应用程序的精髓提取为清晰、一致的导航是那种理论上听起来容易但在实践中实际上很难实现的事务之一。通常需要许多小时的思考和实验，才能为 Web 应用程序构建一个可用且一致的导航地图。然而，这种努力总是是值得的：导航是网站易用性的关键元素之一，正确的导航可以帮助用户高效地定位信息，让他们感到愉快并促进重复访问。

除了良好的导航之外，通过审慎使用客户端编程技术也可以提高应用程序的易用性。大多数现代浏览器中丰富的客户端 API，配合 jQuery、mooTools 和 Dojo 等客户端编程工具包的随手可用，使得快速为 Web 应用程序添加新的行为和功能成为可能，提高响应速度，减少等待时间并提升用户体验。



将 Web 应用程序的精髓提取为清晰、一致的导航是那种理论上听起来容易但在实践中实际上很难实现的事务之一。通常需要许多小时的思考和实验，才能为 Web 应用程序构建一个可用且一致的导航地图。然而，这种努力总是值得的：导航是网站易用性的关键元素之一，正确的导航可以帮助用户高效地定位信息，让他们感到愉快并促进重复访问。

除了良好的导航之外，通过审慎使用客户端编程技术也可以提高应用程序的易用性。大多数现代浏览器中丰富的客户端 API，配合 `jQuery`、`mooTools` 和 `Dojo` 等客户端编程工具包的随手可用，使得快速为 Web 应用程序添加新的行为和功能成为可能，提高响应速度，减少等待时间并提升用户体验。

## 第 11 章：使用用户界面元素

另一方面，它必须由 `Zend Framework` 路由器进行映射，因此只能用于创建指向内部应用程序资源的链接。

如前所示，`Zend_Navigation` 容器可以通过一个 `Zend_Navigation_Page` 对象数组来初始化。然而，对于长或复杂的导航结构，这种方法可能会有些繁琐，因此也可以使用 `Zend_Config` 对象初始化 `Zend_Navigation` 容器，将导航配置转换为 XML 文档或 INI 文件。考虑下面的示例，它说明了这样一个 XML 文档：

```xml
<?xml version="1.0" encoding="UTF-8"?>
<config>
  <home>
    <label>Home</label>
    <uri>/home</uri>
  </home>
  <products>
    <label>Products</label>
    <uri>/products</uri>
    <pages>
      <men>
        <label>Men</label>
        <uri>/products/men</uri>
        <pages>
          <item_1>
            <label>Dress Shirts</label>
            <uri>/products/men/16339</uri>
          </item_1>
          <item_2>
            <label>Trousers</label>
            <uri>/products/men/85940</uri>
          </item_2>
          <item_3>
            <label>Shoes</label>
            <uri>/products/men/75393</uri>
          </item_3>
        </pages>
      </men>
      <women>
        <label>Women</label>
        <uri>/products/women</uri>
        <pages>
          <item_1>
            <label>Skirts and Dresses</label>
            <uri>/products/women/75849</uri>
          </item_1>
          <item_2>
            <label>Bags</label>
            <uri>/products/women/64830</uri>
          </item_2>
          <item_3>
            <label>Shoes</label>
            <uri>/products/women/58303</uri>
          </item_3>
        </pages>
      </women>
    </pages>
  </products>
  <about>
    <label>About Us</label>
    <uri>/about</uri>
    <pages>
      <history>
        <label>Company History</label>
        <uri>/about/history</uri>
      </history>
      <team>
        <label>Management Team</label>
        <uri>/about/team</uri>
      </team>
      <awards>
        <label>Awards</label>
        <uri>/about/awards</uri>
      </awards>
    </pages>
  </about>
  <feedback>
    <label>Feedback</label>
    <uri>/feedback</uri>
  </feedback>
</config>
```

可以使用 `Zend_Config` 将此 XML 文档读取到 `Zend_Navigation` 容器中，如下：

```php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    function navAction()
    {
        // initialize navigation container from XML file
        $config = new Zend_Config_Xml(APPLICATION_PATH . '/configs/site.xml');
        $container = new Zend_Navigation($config);
    }
}
```

**提示**

`Zend_Navigation` 是完全感知本地化的，在配置了正确的 `Zend_Translate` 对象的情况下，它会自动将标签翻译为本地语言对应项。你可以在第 9 章中了解更多关于 `Zend_Translate` 的信息。

使用 `RecursiveIteratorIterator` 遍历 `Zend_Navigation` 容器并获取单个 `Zend_Navigation_Page` 对象的内容很容易。这是一个示例：

```php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    function navAction()
    {
        // initialize navigation container
        $config = new Zend_Config_Xml(APPLICATION_PATH . '/configs/site.xml');
        $container = new Zend_Navigation($config);

        // iterate over container
        // display page information
        foreach (new RecursiveIteratorIterator(
            $container, RecursiveIteratorIterator::CHILD_FIRST) as $page) {
            echo $page->getLabel();
        }
    }
}
```

`Zend_Navigation` 容器还暴露了各种与其包含的页面进行交互的方法。特别是它暴露了 `findBy()` 搜索方法，该方法用于检索所有匹配特定标准的页面。考虑下面的示例，它说明了这一点：

```php
class Sandbox_ExampleController extends Zend_Controller_Action
{
    function navAction()
    {
        // initialize navigation container
        $config = new Zend_Config_Xml(APPLICATION_PATH . '/configs/site.xml');
        $container = new Zend_Navigation($config);

        // find all pages with matching URLs
        $container->findBy('uri', '/about');
    }
}
```

## 渲染导航元素

当然，定义网站导航结构只是问题的一部分；你仍然需要以某种方式使用它。通常，`Zend_Navigation` 容器在应用程序引导器中初始化，并通过应用程序注册表（application registry）保持持久化。这里有一个示例说明了如何设置容器：

```php
class Bootstrap extends Zend_Application_Bootstrap_Bootstrap
{
    protected function _initNavigation()
    {
        $config = new Zend_Config_Xml(APPLICATION_PATH . '/configs/site.xml');
        $container = new Zend_Navigation($config);
        $registry = Zend_Registry::getInstance();
        $registry->set('Navigation', $container);
    }
}
```

一旦完成，`Zend_Navigation` 视图助手就可以访问注册的容器并将其转换为菜单、站点地图或面包屑导航。接下来的章节将详细讨论这些内容。

### 菜单

`Zend_Navigation` 助手可以自动将导航数据转换为列表项。这里是使用它的示例：

```php
echo $this->navigation()->menu();
```

此代码的输出是一个嵌套列表，如图 11-1 所示。也可以通过指定是否只显示活动分支以及菜单深度来对其自定义。这里有一个说明此点的示例：

```php
echo $this->navigation()->menu(
    'onlyBranch' => true,
    'maxDepth' => 1,
    'ulClass' => 'nav'
);
```

**提示**

如果你希望使用自定义标记而不是默认列表来渲染菜单，可以使用 `setPartial()` 方法指定自定义视图。

```php
$this->navigation()->setPartial('custom');
```

图 11-2

### 面包屑导航

还有一个 `Breadcrumbs` 助手，它可以根据当前请求的 URL 自动创建路径。在这种情况下，也可以自定义面包屑的外观，包括分隔符、缩进以及是否将最后一个面包屑渲染为链接。这里是使用它的示例：

```php
echo $this->navigation()->breadcrumbs(
    'linkLast' => true,
    'separator' => ' / '
);
```

图 11-3

### 链接

`Links` 助手生成一组 `<link>` 元素，表示特定页面与其他页面的关系关系并为搜索引擎提供额外信息。这些 `<link>` 元素出现在 HTML 文档的 `<head>` 中：

```php
echo $this->navigation()->links();
```

图 11-4

### 站点地图

`Sitemap` 助手可以使用导航容器中的数据自动生成站点地图。该地图符合 Google、Yahoo! 和 Microsoft 采用的协议，你可以在章末找到有关该协议更多信息的链接。这里是使用它的示例：

```php
echo $this->navigation()->sitemap(
    'formatOutput' => true,
    'maxDepth' => 1
);
```

图 11-5

## 添加导航菜单

现在你已经了解了一些 `Zend_Navigation` 是如何工作的，让我们在 SQUARE 应用程序中使用它吧。由于该应用程序只有一个单层的主菜单，这并不构成太大挑战；但它仍然很好地说明了如何在实际语境中使用 `Zend_Navigation`。

### 定义导航页面和容器

第一步是定义导航容器并将页面附加到其中。正如前面的章节所述，表示这些信息最简单的方法之一是使用 XML 文件。因此，在文本编辑器中创建一个新文件并填充以下数据：

```xml
<config>
  <home>
    <label>首页</label>
    <uri>/home</uri>
  </home>
  <services>
    <label>服务</label>
    <uri>/content/services</uri>
  </services>
  <catalog>
    <label>目录</label>
    <uri>/catalog/item/search</uri>
  </catalog>
  <news>
    <label>新闻</label>
    <uri>/news</uri>
  </news>
  <contact>
    <label>联系我们</label>
    <uri>/contact</uri>
  </contact>
</config>
```

图 11-5 一个自动生成的 XML 站点

将此文件保存为 `$APP_DIR/application/configs/navigation.xml`。注意，此 XML 定义为每个菜单标签使用了字符串标识符；这些标签将通过 `Zend_Navigation` 与 `Zend_Locale` 的内置兼容性自动本地化为当前选择的语言。

#### 导航对象

下一步是更新应用程序启动器（bootstrapper），并配置和注册 `Zend_Navigation` 对象的实例。该实例将在所有应用程序控制器和视图可用，从而可以使用各种导航视图助手（view helpers）。

要做到这一点，请更新 `$APP_DIR/application/Bootstrap.php` 中的应用程序启动器，并向其添加以下方法：

```php
<?php

class Bootstrap extends Zend_Application_Bootstrap_Bootstrap
{
    protected function _initNavigation()
    {
        // 读取导航 XML 并初始化容器
        $config = new Zend_Config_Xml(
            APPLICATION_PATH . '/configs/navigation.xml');
        $container = new Zend_Navigation($config);

        // 注册导航容器
        $registry = Zend_Registry::getInstance();
        $registry->set('Zend_Navigation', $container);

        // 添加 action 助手
        Zend_Controller_Action_HelperBroker::addHelper(
            new Square_Controller_Action_Helper_Navigation()
        );
    }
}
```

注意，`_initNavigation()` 方法的最后一行引用了 `Navigation` action。这是一个自定义的 action 助手，会在每个请求时被调用，并负责设置主菜单中的活动页面。将在下一节中详细讨论。

**注意**

如上一节所示，在每个请求时读取外部文件来加载导航容器会显著降低高流量应用程序的性能。在这种情况下（特别是对于简单的导航容器），替代方案是使用导航资源插件并在应用程序配置文件本身中定义容器。这消除了额外的文件读取，并有助于保持运行速度。

#### 创建导航 action 助手

`Zend Framework` 的 action 助手（action helpers）通常被认为认为是复杂且难以理解的。然而，实际上，事实并非如此。*Action 助手*作为基类控制器的替代品存在；它们为开发者提供了一种将常用功能编程到“助手对象”的方法，然后这些对象可以在运行时从任何 action 控制器加载并使用。

Action 助手通常使用*助手代理（helper broker）*进行注册，该代理暴露了 `addHelper()` 和 `removeHelper()` 方法，以便立即从助手栈中加载和卸载助手。这对于在 `preDispatch()` 或 `postDispatch()` 方法引用的助手尤为重要。另一种方法是使用助手代理的 `addPath()` 或 `addPrefix()` 方法来映射助手路径；这些信息随后可以用于按需加载助手。

一旦助手被加载或映射，可以使用助手代理的 `getHelper()` 方法获取助手，该方法返回助手对象。此助手代理可以通过控制对象的 `_helper` 属性在所有 action 控制器可用，这使得可以在应用程序启动器中按需加载助手，或者在特定控制器中根据需要加载助手。

**提示**



你可能在当时并不知道这一点，但你已经见过并使用过一些 Zend Framework 的内置 action 助手了。第 6 章中的 `ContextSwitch` 助手和第 3 章中的 `FlashMessenger` 助手都是内置 action 助手的示例，可以在控制器内部通过助手代理的 `getHelper()` 方法进行访问。

表 11-1 提供了 Zend Framework 中包含的 action 助手完整列表。

在完成这些背景信息后，让我们回到当前任务：创建一个自定义的 action 助手，它将自动检查当前请求 URL，将其与导航容器进行匹配，并标记当前活动页面。要做到这一点，在 `$APP_DIR/library/Square/Controller/Action/Helper/Navigation.php` 创建一个新的 action 助手，并用以下代码填充它：

| Action 助手 | 说明 |
| :--- | :--- |
| `ActionStack` | 为执行多个 action 队列 |
| `ContextSwitch` | 支持不同格式的输出 |
| `FlashMessenger` | 存储消息以便在下次请求时检索 |
| `Autocomplete` | 为自动完成输入格式化并发送数据的 JSON/HTML 数组 |
| `JSON` | 启用 JSON 格式输出 |
| `Redirector` | 处理客户端重定向 |
| `ViewRenderer` | 注册视图脚本并处理视图脚本渲染 |

表 11-1 Zend Framework 包含的 action 助手

```php
// 代码归 Ryan Mauger 所有，技术编辑
class Square_Controller_Action_Helper_Navigation extends Zend_Controller_Helper_Abstract
{
    protected $_container;

    // 构造函数，设置导航容器
    public function __construct(Zend_Navigation $container = null)
    {
        if (null !== $container) {
            $this->_container = $container;
        }
    }

    // 检查当前请求并设置活动页面
    public function preDispatch()
    {
        $this->getContainer()
            ->findBy('uri', $this->getRequest()->getRequestUri())
            ->active = true;
    }

    // 获取导航容器
    public function getContainer()
    {
        if (null === $this->_container) {
            $this->_container = Zend_Registry::get('Zend_Navigation');
        }
        if (null === $this->_container) {
            throw new RuntimeException ('Navigation unavailable');
        }
        return $this->_container;
    }
}
```

此定义了一个新的 action 助手，它从应用程序表中获取 `Zend_Navigation` 容器，并使用容器的 `findBy()` 方法将当前请求 URL 与容器中的链接进行匹配。如果找到匹配，则将相应的页面标记为活动。由于位于助手的 `preDispatch()` 方法中，此任务会在每个请求执行。

## 使用菜单视图助手

我们为什么需要标识活动页面？这些信息对菜单视图助手很有用，它可以在渲染时为相应的主菜单分支附加“active”CSS 类。这使得在任何时间视觉上自动高亮活动菜单项成为可能。

为了查看效果，请更新主布局使用菜单视图助手并动态生成主菜单，通过更新 `$APP_DIR/application/layouts/master.phtml` 中的主布局文件，并加粗显示更改：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
...
<div id="menu">
    **<?php echo $this->navigation()->menu(); ?>**
</div>
...
</html>
```

## 使用 Dojo Toolkit

Dojo Toolkit 是一个跨浏览器的 JavaScript 库，它包含了用于 AJAX 请求和响应的数据访问层（Dojo Data）以及一组预定义的用户界面组件（Dijit）。这些组件包括布局和菜单元素、数据网格、对话框、如自动完成输入框等表单控件、日期选择器、主题以及各种动画页面效果。该项目得到了 Web 领域一些大公司的支持，包括 Google、IBM、AOL 和 Sun Microsystems。

Zend Framework 使得入门 Dojo Toolkit 变得简单。Zend Framework 的完整版包含了完整的 Dojo 和 Dijit 接口组件，框架还包含一个 `Zend_Dojo` 组件，它可以简化在 Web 应用中激活和使用 Dojo Toolkit 的任务。该 `Zend_Dojo` 组件包含一个数据层实现、一个辅助设置 Dojo 环境的视图助手，以及一组用于在视图脚本中添加 Dojo/Dijit 功能的表单和布局扩展。后续章节将详细讨论这些内容。

### 处理 Dojo Data

Dojo Toolkit 为客户端服务器的数据交换定义了统一格式，并提供了两个基本数据存储对象 `dojo.data.ItemFileReadStore` 和 `dojo.data.ItemFileWriteStore` 来与这些数据交互。在最简单的形式下，数据表示为结构化的 JSON 对象，看起来如下：

```json
{
  "identifier":"name",
  "items": [
    {"name":"Agatha Christie"},
    {"name":"J. K. Rowling"},
    {"name":"Dan Brown"},
    {"name":"William Shakespeare"},
    {"name":"Dennis Lehane"}
  ]
}
```

`Zend_Dojo_Data` 组件提供了一个面向对象的 API，用于构建这种 JSON 表示、添加项、遍历以及查询匹配项。为了说明，请考虑以下列表，它的输出与之前的代码列表等效：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function dojoAction()
    {
        // define data items
        $authors = array(
            'Agatha Christie', 'J. K. Rowling', 'Dan Brown',
            'William Shakespeare', 'Dennis Lehane'
        );

        foreach ($authors as $a) {
            $items[] = array('name' => $a);
        }

        // initialize object and pass it data items
        $data = new Zend_Dojo_Data('name', $items);

        // output as structured JSON
        echo $data->toJson();
    }
}
```

如示例所示，只需通过向对象构造函数传递唯一标识符字段名称（在本例中为 `'name'`）和数据项数组即可简单地初始化对象。这些数据项必须表示为关联数组（或实现 `toArray()` 方法的对象），并且必须包含指定的标识符作为数组键之一。一旦初始化完成，可以通过 `toArray()` 或 `toJson()` 方法将对象导出为 PHP 数组或 JSON 字符串。

**提示**

在实现 Dojo/Dijit AJAX 请求的端点时，`Zend_Dojo_Data` 组件变得特别有用。你将在本章的后续部分看到相关的示例。

### 使用 Dojo View Helpers

通常，在 Web 页面中启用 Dojo 和 Dijit 组件涉及加载 Dojo 库文件、初始化 Dojo 解析器并启用所需的组件，同时根据需要传递配置选项。虽然这可以在你的视图脚本中手动完成，但 Zend Framework 提供了一种更简单的方法：Dojo 视图助手（view helper），它通过自动内联生成所有必要的客户端初始化代码来将视图“Dojo 化”。

以下是一个在视图脚本中使用 Dojo 视图助者的示例：

```php
<?php

Zend_Dojo::enableView($this);
$this->dojo()->setLocalPath('/js/dojo/dojo.js')
    ->addStyleSheetModule('dijit.themes.tundra')
    ->setDjConfigOption('parseOnLoad', true)
    ->setDjConfigOption('locale', 'en-US')
    ->setDjConfigOption('isDebug', true);

echo $this->dojo();

?>
```

图 11-7 展示了助手从上一个列表生成的标记。

**注意**

注意上一个列表中对 `Zend_Dojo::enableView` 的调用。该方法将 Dojo 视图助手路径添加到 `Zend_View` 对象中；遗漏它通常会导致抛异常，因为 `Zend_View` 将无法找到并加载所需的助手。

如果你希望从外部位置（例如内容分发网络 CDN）加载 Dojo Toolkit 库，可以使用 `setCdnBase()` 方法，如下：

```php
<?php

Zend_Dojo::enableView($this);
$this->dojo()->setCdnBase(Zend_Dojo::CDN_BASE_AOL)
    ->addStyleSheetModule('dijit.themes.tundra')
    ->setDjConfigOption('parseOnLoad', true)
    ->setDjConfigOption('locale', 'en-US')
    ->setDjConfigOption('isDebug', true);

echo $this->dojo();

?>
```

**注意**

如果你没有使用 `setLocalPath()` 指定 Dojo 库的本地路径，Dojo 视图助手将假设你想使用 Google CDN。

除了 Dojo 视图助手外，Zend Framework 还提供了许多其他助手，可以直接在视图脚本中渲染 Dojo 和 Dijit 布局和表单元素。表 11-2 给出了这些助手的简列表。值得注意的是，Dojo 视图助手会自动检测你在视图脚本中使用这些助者的行为，并生成初始化它们所需的客户端代码。这里是一个示例：

```html
<html>
<head>
<?php
Zend_Dojo::enableView($this);
$element = $this->NumberSpinner('temp', array(
    'min' => 12,
    'max' => 41,
    'places' => 25
));
echo $this->dojo();
?>
</head>
<body class="tundra">
<?php echo $element; ?>
</body>
</html>
```

此示例使用 `NumberSpinner` 视图助手来生成一个 Dijit 数字拨轮器表单控件。图 11-8 展示了生成的标记。

| Dojo 视图助手 | 描述 |
| :--- | :--- |
| `Button` | 按钮 |
| `CheckBox` | 复选框 |
| `ComboBox` | 组合选择/文本输入 |
| `ContentPane` | 内容容器 |
| `CurrencyTextBox` | 货币输入 |
| `DateTextBox` | 日期选择器 |
| `Editor` | 富文本编辑器 |
| `FilteringSelect` | 带有过滤的选择控件 |
| `HorizontalSlider` | 水平滑块 |
| `NumberSpinner` | 带有增量控制的数字输入 |
| `StackContainer` | 堆叠内容容器 |
| `TabContainer` | 标签页内容容器 |
| `Textarea` | 文本区域 |
| `TextBox` | 文本输入 |
| `TimeTextBox` | 时间选择器 |
| `ValidationTextBox` | 带有验证器的文本输入 |
| `VerticalSlider` | 垂直滑块 |

表 11-2 Zend Framework 包含的 Dojo 视图助手（非详尽列表）

### 使用 Dojo 表单元素

Dojo Toolkit 包含许多现成的表单控件，可以快速为 Web 表单添加常见功能：颜色选择器、WYSIWYG 文本编辑器、数字拨轮、自动完成文本框、水平滑块控件等。`Zend_Dojo` 扩展了 `Zend_Form` 以支持这些额外元素，允许它们像普通的 `Zend_Form_Element` 实例一样被使用。

表 11-3 提供了 Zend Framework 包含的 Dojo 特定表单控件列表。

要在表单内部使用这些元素，更新 `Zend_Form` 实例以扩展 `Zend_Dojo_Form` 而不是 `Zend_Form`，然后按照通常方式将其挂载 `Zend_Dojo_Form_Element` 元素。以下是一个示例，通过创建一个带有日期选择器、富文本编辑器和垂直滑块的 Web 表单来阐明：

```php
<?php

class Form_Example extends Zend_Dojo_Form
{
    // Example implementation
}
```

```php
public function init()
{
    $this->setAction('/sandbox/example/form')
        ->setMethod('post')
        ->setOptions(array('class' => 'tundra'));

    // 创建富编辑器
    $message = new Zend_Dojo_Form_Element_Editor('message');
    $message->setLabel('Message:')
        ->setOptions(array(
            'width' => '150px',
            'height' => '100px',
        ));

    // 创建日期选择器
```

表 11-3 Zend Framework 的 Dojo 表单元素类

| 表单元素类 | 说明 |
| :--- | :--- |
| `Zend_Dojo_Form_Element_Button` | 按钮 |
| `Zend_Dojo_Form_Element_CheckBox` | 勾选框 |
| `Zend_Dojo_Form_Element_ComboBox` | 组合选择/输入 |
| `Zend_Dojo_Form_Element_CurrencyTextBox` | 货币输入 |
| `Zend_Dojo_Form_Element_DateTextBox` | 日期输入 |
| `Zend_Dojo_Form_Element_DijitMulti` | 勾选框组 |
| `Zend_Dojo_Form_Element_Editor` | 富文本输入框 |
| `Zend_Dojo_Form_Element_FilteringSelect` | 带有过滤的选择控件 |
| `Zend_Dojo_Form_Element_HorizontalSlider` | 水平滑块 |
| `Zend_Dojo_Form_Element_NumberSpinner` | 带有增减控制的数字输入 |
| `Zend_Dojo_Form_Element_NumberTextBox` | 数字输入 |
| `Zend_Dojo_Form_Element_PasswordTextBox` | 密码输入 |
| `Zend_Dojo_Form_Element_RadioButton` | 单选按钮 |
| `Zend_Dojo_Form_Element_SimpleTextarea` | 文本输入框 |
| `Zend_Dojo_Form_Element_SubmitButton` | 提交按钮 |
| `Zend_Dojo_Form_Element_Textarea` | 文本输入 |
| `Zend_Dojo_Form_Element_TextBox` | 文本输入 |



| `Zend_Dojo_Form_Element_TimeTextBox` | 时间输入 |
| `Zend_Dojo_Form_Element_ValidationTextBox` | 带有验证器的文本输入 |
| `Zend_Dojo_Form_Element_VerticalSlider` | 垂直滑块 |

## 第 11 章：用户界面元素操作

```php
$dob = new Zend_Dojo_Form_Element_DateTextBox('dob');
$dob->setLabel('Date of birth:');

// 创建滑块
$volume = new Zend_Dojo_Form_Element_VerticalSlider('volume');
$volume->setLabel('Volume level:')
    ->setOptions(array(
        'minimum' => '100',
        'maximum' => '0',
        'discreteValues' => '10',
        'style' => 'height: 100px'
    ));

// 创建提交按钮
$submit = new Zend_Dojo_Form_Element_SubmitButton('submit');
$submit->setLabel('Submit');

$this->addElement($message)
    ->addElement($dob)
    ->addElement($volume)
    ->addElement($submit);
}
}
```

图 11-9 展示了输出的外观。

**图 11-9** 带有 Dojo/Dijit 表单元素的表单

![](img/222e7e58871b088cc6397852e1452b57_385_0.png)

## 添加 Dojo 自动补全组件

现在你已经了解了`Zend_Dojo`组件的功能，让我们尝试将它用在实际操作中：为`Zend_Form`实例添加一个自动补全输入框。这是一个相当常见的需求，接下来的章节将引导你完成这一过程。

### 更新联系表单

在本示例中，假设自动补全输入将附加到应用程序的联系表单，该表单将根据用户的输入“建议”国家列表。因此，第一步是更新`Square_Form_Contact`对象，使其扩展`Zend_Dojo_Form`而不是`Zend_Form`（如上一节所述），并向其添加一个 Dijit ComboBox 元素。

以下是代码：

```php
<?php
class Square_Form_Contact extends Zend_Dojo_Form
{
    public function init()
    {
        // 初始化表单
        $this->setAction('/contact')
            ->setMethod('post');

        // 创建名称文本输入
        ...

        // 创建邮箱地址文本输入
        ...

        // 创建国家自动补全输入
        $country = new Zend_Dojo_Form_Element_ComboBox('country');
        $country->setLabel('contact-country');
        $country->setOptions(array(
            'autocomplete' => false,
            'storeId' => 'countryStore',
            'storeType' => 'dojo.data.ItemFileReadStore',
            'storeParams' => array('url' => "/default/contact/autocomplete"),
            'dijitParams' => array('searchAttr' => 'name')
        ))
        ->setRequired(true)
        ->addValidator('NotEmpty', true)
        ->addFilter('HTMLEntities')
        ->addFilter('StringToLower')
        ->addFilter('StringTrim');

        // 创建消息主体文本输入
        ...
```

**尝试尝试 11-2**

```php
// 创建验证码
......

// 创建提交按钮
...

// 将元素附加到表单
$this->addElement($name)
    ->addElement($email)
    ->addElement($country)
    ->addElement($message)
    ->addElement($captcha)
    ->addElement($submit);
}
```

修订后的定义为联系表单添加了一个新的 Dijit ComboBox 元素，并指定使用远程数据存储。数据存储端点也指定为`/default/autocomplete`。将修订后的定义保存到`Contact.php`并继续阅读如何定义。

### 初始化 View Helper

下一步是初始化 View Helper。如果你的应用程序没有使用布局（layouts），可以直接在视图脚本中执行此初始化。然而，由于 SQUARE 应用使用了布局，此初始化必须在布局内部执行。作为一个通用规则，减少页面生成的远程 HTTP 请求次数很重要，因为每个请求都会增加开销并增加用户等待加载的时间。更好的方法是在引导（bootstrap）中配置 Dojo Helper，但显式禁用它，以便在需要的视图脚本中动态启用。

要实现这一点，首先在应用程序配置文件添加以下行来启用视图资源：

`resources.view = false;`

然后，使用以下方法更新`Bootstrap.php`引导类：

```php
<?php
class Bootstrap extends Zend_Application_Bootstrap
{
    protected function _initDojo()
    {
        // 获取视图资源
        $this->bootstrap('view');
        $view = $this->getResource('view');

        // 为视图添加 helper
        Zend_Dojo::enableView($view);

        // 配置 Dojo helper，禁用
        $view->dojo()->setCdnBase(Zend_Dojo::CDN_BASE)
            ->addStyleSheet('dijit.themes.tundra')
            ->disable();
    }
}
```

此方法从视图插件获取实例并使用`Zend_Dojo::enableView`方法启用视图 Dojo Helper。然后配置 Dojo 环境，设置 CDN URL 和样式表，最后通过其`disable()`方法禁用 helper。最终结果是 Dojo Helper 已配置使用，但除非通过调用 helper 的`enable()`方法显式请求，否则 Dojo Toolkit 库不会在视图中加载。

### 更新主布局（Master Layout）

下一步是更新主布局以检查 Dojo Helper 是否启用，如果是，则加载 Dojo 环境。这并不困难，如`master.phtml`布局的`<head>`中的以下添加所示：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
    <base href="/" />
    <link rel="stylesheet" type="text/css" href="/css/master.css" />
    <?php if ($this->dojo()->isEnabled()):
        echo $this->dojo();
    endif;
    ?>
</head>
<body class="tundra">
    ...
</body>
</html>
```

### 更新控制器（Controller）

最后一步是更新`ContactController`为自动补全输入定义端点。以下是代码，应添加到`application/modules/default/controllers/ContactController.php`：

```php
<?php
class ContactController extends Zend_Controller_Action
{
    public function autocompleteAction()
    {
        // 禁用布局和视图渲染
        $this->_helper->layout->disableLayout();
        $this->getHelper('viewRenderer')->setNoRender(true);

        // 从 Zend_Locale 获取国家列表
        $territories = Zend_Locale::getTranslationList('territory', null, 2);
        $items = array();
        foreach ($territories as $t) {
            $items[] = array('name' => $t);
        }

        // 生成并返回符合 dojo.data 结构的 JSON 字符串
        $data = new Zend_Dojo_Data('name', $items);
        header('Content-Type: application/json');
        echo $data->toJson();
    }
}
```

该方法使用之前过的`Zend_Dojo_Data`组件将包含国家列表数组转换为 Dojo 期的 JSON 格式，并将其返回给客户端。

要查看其运行效果，请访问 SQUARE 应用的联系表单（浏览到`http://square.localhost/contact`），您应该看到一个新的国家名称文本输入框。在该字段中输入几个字符，观察 Dojo 如何请求并展示来自上一节定义的`ContactController::autocompleteAction`的匹配建议列表。

图 11-10 展示了你可能看到的示例。

**图 11-10** 运行中的 Dojo ComboBox

![](img/222e7e58871b088cc6397852e1452b57_389_0.png)

## 添加 YUI 日历小部件

在上一节中，你已经看到在 Zend Framework 应用中添加 Dojo 小部件是多么简单了。然而，Dojo 并不是唯一的选择，从其他客户端编程工具包中集成小部件和库也同样简单。接下来的部分将演示如何向`Zend_Form`实例添加一个来自 Yahoo! 用户界面库（YUI）的弹出式日历小部件。

在本例中，目标表单是第 5 节中首次定义的`ItemUpdate`表单，它允许管理员调整目录项属性并设置显示状态。在这个示例中，我们将更新表单，使用 YUI 的图形化日历小部件进行单击日期输入，而不是为日、月、年显示独立的选择列表。

为了本示例的演示，假设所有必要的 YUI 文件都托管在远程并从 Yahoo! 内容分发网络（CDN）加载。

### 更新表单

第一步是更新表单对象，创建一个包含日历小部件的新元素，并移除之前的日期选择列表。以下是修改后的表单定义，应保存至`$APP_DIR/library/Square/Form/ItemUpdate.php`：



```php
<?php

class Square_Form_ItemUpdate extends Square_Form_ItemCreate
{
    public function init()
    {
        // 获取父表单
        parent::init();

        // 设置表单动作（设置为 false 使用当前 URL）
        $this->setAction('/admin/catalog/item/update');

        // 移除不需要的元素
        $this->removeElement('Captcha');
        $this->removeDisplayGroup('verification');
        $this->removeElement('images');
        $this->removeDisplayGroup('files');

        //为项目 ID 创建隐藏输入
        $id = new Zend_Form_Element_Hidden('RecordID');
        $id->addValidator('Int')
            ->addFilter('HtmlEntities')
            ->addFilter('StringTrim');

        // 为项目显示状态创建选择输入
        $display = new Zend_Form_Element_Select('DisplayStatus',
            array('onChange' => "javascript:handleInputDisplayOnSelect('DisplayStatus', 'divDisplayUntil', new Array('1')); cal.hide();"));
        $display->setLabel('Display status:')
            ->setRequired(true)
            ->addValidator('Int')
            ->addFilter('HtmlEntities')
            ->addFilter('StringTrim');
        $display->addMultiOptions(array(
            0 => 'Hidden',
            1 => 'Visible'
        ));

        // 为项目显示日期创建输入
        $displayUntil = new Zend_Form_Element_Text('DisplayUntil');
        $displayUntil->setLabel('Display until (yyyy-mm-dd):')
            ->addValidator('Date', false, array('format' => 'yyyy-MM-dd'))
            ->addFilter('HtmlEntities')
            ->addFilter('StringTrim')
            ->addDecorators(array(
                array('HTMLTag', array('tag' => 'div', 'id' => 'divDisplayUntil')),
            ));

        // 为 YUI 日历小部件创建容器
        $calendar = new Zend_Form_Element_Text('Calendar');
        $calendar->setDecorators(array(
            array('Label', array('tag' => 'dt')),
            array('HTMLTag', array('tag' => 'div', 'id' => 'divCalendar', 'class' => 'yui-skin-sam yui-calcontainer', 'style' => 'display:none;')),
        ));

        // 将元素附加到表单
        $this->addElement($id)
            ->addElement($display)
            ->addElement($calendar)
            ->addElement($displayUntil);

        //为状态创建显示组
        $this->addDisplayGroup(
            array('DisplayStatus', 'DisplayUntil', 'Calendar'),
            'display');
        $this->getDisplayGroup('display')
            ->setOrder(25)
            ->setLegend('Display Information');
    }
}
?>
```

**尝试一下 11-3**

**Q: 什么是 Yahoo! 用户界面库？**

**A:** 引用其官方网站的话，Yahoo! 用户界面库（简称 YUI）是“一组用 JavaScript 和 CSS 编写的工具和控件，用于构建丰富交互的 Web 应用程序”。它提供了大量的现成小部件，开发者可以用极少的精力将其集成到 Web 应用程序中，并且它可以在所有现代浏览器上运行。

该库中的一些小部件包括图片轮播器、颜色选择器、拖放界面、上传进度监控器、标签和树形菜单系统、日历小部件以及输入自动完成器。

这些小部件中包含日历小部件，它可以显示月日历，并为用户提供导航控件，以便在月份和年份之间切换。用户可以通过点击特定日期来选择它；小部件会自动将选定的日期转换为标准日期字符串，并将其附加到指定的表单元素上。

**提问专家**

### 更新主布局

Zend Framework 的 `HeadScript` 和 `HeadLink` 视图助手提供了一种按动作（action）指定外部资源的简单方法。这些助手允许开发者在设计时为每个动作和视图脚本指定 JavaScript 和 CSS 文件，并在运行时自动生成必要的 `<link>` 和 `<script>` 标记。

要使用这些助手，请更新`$APP_DIR/application/layouts/admin.phtml`中管理布局的 `<head>` 部分，加粗显示更改之处：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN" "http://www.w3.org/TR/REC401/loose.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="en">
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
    <title>Admin</title>
    <link rel="stylesheet" type="text/css" href="/css/admin.css" />
    <?php echo $this->headLink(); ?>
    <?php echo $this->headScript(); ?>
</head>
<body>
```

下一步是更新`Catalog_ItemController`，使用 YUI 日历小部件提供的日期字符串而不是独立的日、月、年选择列表。以下是修改后的代码：

```php
<?php
class Catalog_ItemController extends Zend_Controller_Action
{
    public function updateAction()
    {
        // 生成表单
        $form = new Square_Form_ItemUpdate();
        $this->view->form = $form;

        if ($this->getRequest()->isPost()) {
            // 如果是 请求
            // 测试输入是否有效
            // 获取当前记录
            $postData = $this->getRequest()->getPost();
            if ($form->isValid($postData)) {
                $input = $form->getValues();
                $item = Doctrine::getTable('Square_Model_Item')->find($input['RecordID']);
                $item->fromArray($input);
                $item->DisplayUntil = ($item->DisplayStatus == 0) ? null : $item->DisplayUntil;
                $item->save();
                $this->_helper('FlashMessenger')->addMessage('The record was successfully updated.');
                $this->_redirect('/admin/catalog/success');
            }
        } else {
            // 如果是 请求
            //为 GET 设置过滤器和验证器
            // 测试输入是否有效
            // 获取请求的记录
            // 填充表单
            $filters = array(
                'id' => array('HtmlEntities', 'StripTags', 'StringTrim')
            );
            $validators = array(
                'id' => array('NotEmpty', 'Int')
            );
            $input = new Zend_Filter_Input($filters, $validators);
            $input->setData($this->getRequest()->getParams());
            if ($input->isValid()) {
                $q = Doctrine_Query::create()
                    ->from('Square_Model_Item i')
                    ->leftJoin('i.Square_Model_Country c')
                    ->leftJoin('i.Square_Model_Grade g')
                    ->leftJoin('i.Square_Model_Type t')
                    ->where('i.RecordID = ?', $input->id);
                $result = $q->fetchArray();
                if (count($result) == 1) {
                    $date = $result[0]['DisplayUntil'];
                    $result[0]['DisplayUntil_day'] = date('d', strtotime($date));
                    $result[0]['DisplayUntil_month'] = date('m', strtotime($date));
                    $result[0]['DisplayUntil_year'] = date('Y', strtotime($date));
                    $this->view->form->populate($result[0]);
                } else {
                    throw new Zend_Controller_Action_Exception('Page not found', 404);
                }
            }
        }
    }
}
?>
```

## 第 11 章：处理用户界面元素

```php
throw new Zend_Controller_Action_Exception('Invalid input');
}

}

}
```

更新视图

最后，需要少量的 JavaScript 在视图脚本中初始化组件，该脚本位于`$APP_DIR/application/modules/admin/views/scripts/admin-item/update.phtml`：

```html
<h2>Update Item</h2>
<?php echo $this->form; ?>

<script type="text/javascript">
handleInputDisplayOnSelect('DisplayStatus', 'divDisplayUntil', new Array('1'));
cal = new YAHOO.widget.Calendar('cal', 'divCalendar', {close:true});
cal.render();
YAHOO.util.Event.addListener('DisplayUntil', 'click', cal.show, cal, true);
cal.selectEvent.subscribe(handleSelect, cal, true);

function handleSelect(type,args,obj) {
    var dates = args[0];
    var date = dates[0];
    var year = date[0];
    var month = date[1];
    var day = date[2];
var input = document.getElementById('DisplayUntil');
input.value = year + '-' + padZero(month, 2) + '-' + padZero(day, 2);
}
</script>
```

问：为什么你们不直接在主布局（master layout）中指定指向 YUI JavaScript 和 CSS 文件的“硬链接”，而不是使用`headScript()`和`headLink()`视图辅助器？

答：YUI 文件仅在某些视图脚本中需要。由于这些文件是通过 HTTP 从远程主机读取的，在主布局中创建它们的“硬链接”并不是最优的，因为会导致在每个页面加载时都请求这些文件。这增加了不必要的开销，并增加了用户在页面完全加载之前等待的秒数。使用视图辅助器可以在需要时才加载这些文件，从而提供更好的用户体验并提高性能。

专家问（续）

保存这些更改，然后导航到管理面板并选择一个目录项进行更新。你将看到一个带有更新各种项目属性字段的表单。选择“显示直到”字段，会弹出一个日历用于选择日期。图 11-11 展示了其可能的外观。

图 11-11：运行中的 YUI 日历组件

![](img/222e7e58871b088cc6397852e1452b57_396_0.png)

### 总结

本章重点关注了用户界面元素以及能够为应用程序用户提供更好体验的 Zend Framework 组件。首先，本章讨论了`Zend_Navigation`组件，说明了如何将页面结构化到容器中，然后从这些容器生成站点地图、菜单和面包屑导航。接下来，它研究了 Zend Framework 的 Dojo 集成，并说明了如何使用`Zend_Dojo`组件快速将自动补全输入集成到`Zend_Form`实例中。最后，它查看了在 Zend Framework 应用程序中使用第三方 JavaScript 组件的流程，并提供了将 YUI 日期选择器集成到`Zend_Form`实例的示例。

要了解更多关于本章讨论的话题，请考虑访问以下链接：

- `Zend_Navigation`组件，位于：http://framework.zend.com/manual/en/zend.navigation.html

- `Zend_Dojo`组件，位于：http://framework.zend.com/manual/en/zend.dojo.html

- Zend Framework 动作辅助器，位于：http://framework.zend.com/manual/en/zend.controller.actionhelpers.html

- Zend Framework 资源插件，位于：http://framework.zend.com/manual/en/zend.application.available-resources.html

- Yahoo! 用户界面库（YUI），位于：http://developer.yahoo.com/yui/



- Dojo Toolkit，位于：`http://www.dojotoolkit.org/`

- Sitemaps 站点协议，位于：`http://www.sitemaps.org/`

- 关于创建自定义资源插件的讨论（Stefan Schmalhaus），位于：`http://blog.log2e.com/2009/06/01/creating-a-custom-resource-plugin-in-zend-framework-18/`

## 第 12 章：优化性能

### 关键技能与概念

- 熟悉应用程序基准测试和分析工具

- 理解缓存的优势和类型

- 了解如何缓存 Web 服务响应和 RSS 馈

- 学习各种优化数据库查询性能的技术

在过去的几年里，Web 应用程序变得越来越复杂，拥有许多花哨功能——AJAX 用户界面、流媒体、动态生成的内容——试图吸引并留住访问。但随着应用程序变得越来越复杂，对动态数据源的依赖增加，以及每秒需要服务的请求越来越多，首当受害者通常是应用程序性能。

然而，你有许多常用技术可以识别并绕过应用程序代码中的性能瓶颈。代码分析、缓存、重构和懒加载等技术可以减少服务器负载并提高应用程序的响应时间。Zend Framework 自带了许多可以用于此任务的工具，本章讨论了其中一些。

### 分析性能

在开始微调 Web 应用程序之前，你需要详细信息，了解应用程序的哪些部分出现了性能下降。目前有许多用于基准测试和分析的工具，接下来的章节将详细讨论这些工具。

### 基准测试

ApacheBench（或 `ab`）是一种用于基准测试 Web 服务器响应时间的工具。它通过发送多个并发请求、进行计时并生成不同负载条件下的详细统计数据来实现工作。ApacheBench 是 Apache 服务器的一部分，适用于 Windows 和 NIX 。

以下是使用 ApacheBench 对 Web 应用程序进行基准测试的示例，模拟同时发送 10 个请求：

```shell
ab -n 1000 -c 10 http://server/url
```

图 12-1 显示了 ApacheBench 生成的报告示例。

如图 12-1 所示，该报告提供了服务器响应特定 URL 所需的有用信息。对其他应用程序路由运行类似的测试，可以构建出应用程序哪些部分较“慢”并可以进行优化。

ApacheBench 的替代方案是微软 Web 容量分析工具（WCAT）。与 ApacheBench 类似，该工具模拟 Web 服务器负载，返回吞吐量和响应时间的数据。尽管仅适用于 Windows 平台，但有两个有趣的特性：它可以从多个客户端系统同时运行，并且可以基准测试按特定顺序执行的多个请求“事务”。

以下是使用 WCAT 测试 Web 应用程序的示例：

```shell
wcat.wsf -terminate -run -clients localhost -t scenario.ubr -f settings.ubr -s server -singleip -extended
```

图 12-2 显示了 WCAT 输出示例。

图 12-1：ApacheBench 摘要统计

![](img/222e7e58871b088cc6397852e1452b57_401_0.png)

### 代码分析

一旦你获得了一些广泛的基准测试数据并确定了改进区域，下一步是对相关的控制器和动作进行分析，并理解瓶颈在哪里。此任务最流行的工具之一是 PHP 的 Xdebug 扩展，适用于 Windows 和 NIX 版 PHP。

Xdebug 分析器会生成脚本中每个函数调用耗时的详细统计数据，以及脚本编译、处理和执行的总时间。这些统计数据可以看到哪些函数调用产生了最大的处理开销，从而识别潜在的优化区域。Xdebug 扩展还覆盖了 PHP 默认的异常处理程序，为致命是非致命错误提供更详细的调试输出和堆栈跟踪。

图 12-2：一份 WCAT 基准测试报告

![](img/222e7e58871b088cc6397852e1452b57_402_0.png)

## 第 12 章：优化性能

385

一旦配置完成，Xdebug 将自动对通过 PHP 解释器执行的每个脚本进行性能分析（profile）。性能分析报告的格式为 *cachegrind 文件*，可以使用许多开源工具查看，例如 WinCacheGrind（Windows 桌面端）、KCacheGrind（NIX 桌面端）或 Webgrind（PHP Web 应用）。分析文件存储在 PHP `php.ini` 配置文件 `xdebug.profiler_output_dir` 变量指定的输出目录中。

图 12-3 展示了此类分析文件的样式。

这种类型的分析信息对于理解非常有用，例如，它可以告诉你哪些方法调用或框架组件占据了大部分处理时间，因此它们是优化或用其他更轻量的库替换的合理目标。

***注意***

PHP 的 Xdebug 扩展以通常方式安装在 PHP 的 `ext/` 目录中，并通过在 `php.ini` 配置文件中添加 `zend_extension_ts = /path/to/xdebug/ext` 指令来激活。你还必须在配置文件中指定 `xdebug.profiler_enable`、`xdebug.profiler_output_dir` 和 `xdebug.trace_output_dir` 变量。详细的安装说明请参见本章末尾 Xdebug 网站链接。

Xdebug 的替代方案是 PEAR Benchmark 类，它提供了一个对 PHP 函数调用进行基准测试的 API。在这种情况下，基准测试工具嵌入在特定的 action 中，将 action 代码封装在其 `start()` 和 `stop()` 方法调用内部。图 12-3 是一个 Zend Framework 请求的 Xdebug 分析图（在 Webgrind 中查看）。386 这些方法通常在 action 的开始和结束处调用，尽管它们也可以用于对 action 的特定子部分进行基准测试。

在这两个方法调用之间，设置用户定义的区域“标记（markers）”以识别脚本正在执行的活动或事务是一个好主意；因为这些标记被包含在最终报告中，它们可以帮助识别哪些事务导致了多少百分比的开销。以下是如何使用该类的用例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function queryAction()
    {
        // 性能分析器
        include_once('Benchmark/Profiler.php');
        $profiler = new Benchmark_Profiler();
        // 启动分析器
        $profiler->start();
        // 过滤器/验证器设置
        $profiler->enterSection("Setup");
        $filters = array(
            'q' => array('HtmlEntities', 'StripTags', 'StringTrim'),
        );
        $validators = array(
            'q' => array('Alpha'),
        );
        $input = new Zend_Filter_Input($filters, $validators);
        $input->setData($this->getRequest()->getParams());
        $profiler->leaveSection("Setup");
        // 验证逻辑分析
        $profiler->enterSection("Validate");
        $check = $input->isValid();
        $profiler->leaveSection("Validate");
        // 数据库查询分析
        if ($check) {
            $profiler->enterSection("Query");
            $db = $this->getInvokeArg('bootstrap')->getResource('database');
            $sql = "SELECT * FROM city AS ci,
country AS co,
countrylanguage AS cl
WHERE
ci.CountryCode = co.Code AND
cl.CountryCode = co.Code AND
cl.Language = 'English' AND
387 Chapter 12: Optimizing Performance
cl.IsOfficial = 'T' AND
co.Continent LIKE '%$input->q%'";
            $result = $db->fetchAll($sql);
            $this->view->records = $result;
            $profiler->leaveSection("Query");
        }
        $profiler->stop();
        $this->view->profile = $profiler->_getOutput('html');
    }
}
```

图 12-4 是 PEAR Benchmark 生成的分析示例。

***提示***

PEAR Benchmark 类与其他 PEAR 类一样，不支持 Zend Framework 的自动加载器。要使其兼容，请使用 PEAR 安装程序安装它，检查 PEAR 目录是否在包含路径中，然后在 `application.ini` 文件中添加 `namespaces[] = 'Benchmark'`。

### 查询分析

Xdebug 和 PEAR Benchmark 对于分析 PHP 代码非常有用，但它们没有提供关于 Web 应用中常见的性能瓶颈的信息：应用程序与数据库之间的交互。作为任何性能分析练习，也有必要对应用程序的数据库查询进行分析，并了解它们在哪里可以优化。如果你使用 `Zend_Db` 进行数据库查询，可以使用 `Zend_Db_Profiler` 对它们进行分析，这使得检查应用程序查询并获取每个查询的耗时成为可能。

图 12-4 Zend Framework 请求的 PEAR Benchmark 分析![](img/222e7e58871b08cc6397852e1452b57_405_0.png)

388 引导指南使用 `Zend_Db_Profiler` 的简单方法将其附加到应用程序引导器（bootstrapper）中的 `Zend_Db` 实例中，如下：

```php
<?php

class Bootstrap extends Zend_Application_Bootstrap
{
    protected function _initDatabase()
    {
        $db = new Zend_Db_Adapter_Pdo_Mysql(array(
            'host' => '127.0.0.1',
            'username' => 'user',
            'password' => 'pass',
            'dbname' => 'world'
        ));
        $profiler = new Zend_Db_Profiler();
        $profiler->setEnabled(true);
        $db->setProfiler($profiler);
        return $db;
    }
}
```

分析器捕获的查询分析可以通过 `Zend_Db_Profiler` 对象的 `getQueryProfiles()` 方法检索。该方法返回 `Zend_Db_Profiler_Query` 对象数组，每个对象都暴露了 `getQuery()` 和 `getElapsedSecs()` 方法来分别检索查询字符串和执行时间。以下使用这些方法从分析器检索分析数据的示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action
{
    public function queryAction()
    {
        // 获取数据库适配器
        $db = $this->getInvokeArg('bootstrap')->getResource('database');
        // 执行查询
        $sql = "SELECT * FROM city AS ci,
country AS co,
countrylanguage AS cl
WHERE
ci.CountryCode = co.Code AND
cl.CountryCode = co.Code AND
cl.Language = 'English' AND
cl.IsOfficial = 'T' AND
co.Continent LIKE '%$input->q%'";
        $result = $db->fetchAll($sql);
        $this->view->records = $result;
389 Chapter 12: Optimizing Performance
        $this->view->profiles = array();
        // 获取查询分析数据
        foreach ($db->getProfiler()->getQueryProfiles() as $profile) {
            $this->view->profiles[] = array(
                'sql' => $profile->getQuery(),
                'time' => $profile->getElapsedSecs(),
            );
        }
    }
}
```

图 12-5 展示了上述列表生成的分析数据示例。还有一个专门的 `Zend_Db_Profiler_Firebug` 扩展，可以将查询分析数据直接发送 Firebug 控制台。要使用它，如下所示更新应用程序引导器：

```php
<?php

class Bootstrap extends Zend_Application_Bootstrap
{
    protected function _initDatabase()
    {
        $db = new Zend_Db_Adapter_Pdo_Mysql(array(
            'host' => '127.0.0.1',
            'username' => 'user',
            'password' => 'pass',
390 引导指南
            'dbname' => 'world'
        ));
        $profiler = new Zend_Db_Profiler_Firebug('Query log');
        $profiler->setEnabled(true);
        $db->setProfiler($profiler);
        return $db;
    }
}
```

图 12-5 `Zend_Db_Profiler` 生成的查询分析输出![](img/222e7e58871b08cc6397852e1452b57_407_0.png)

图 12-6 展示了由 ZendDb 分析器生成的 Firebug 控制台输出示例。Zend Framework 不包含针对基于 Doctrine 的数据库查询的内置分析器，但通过 Imind 项目的第三方组件添加该分析器是相当容易的。该项目包含了许多针对 Zend Framework 的特定 Doctrine 扩展，其中之一就是 `Imind_Profiler_Doctrine_Firebug` 组件。该组件将 Doctrine 查询记录到 Firebug（Firefox 浏览器调试器）控制台，使得实时测量查询性能成为可能。

要使用 Imind Doctrine 分析器对 Doctrine 查询进行分析，如下所示将分析器附加到应用程序引导器中的 Doctrine 连接管理器：

```php
<?php

class Bootstrap extends Zend_Application_Bootstrap
{
    protected function _initDoctrine()
    {
        require_once 'Doctrine/Doctrine.php';
        图 2-6 `Zend_Db_Profiler` 生成的查询分析输出，在 Firebug 控制台中所示
        ![](img/222e7e58871b08cc6397852e1452b57_408_0.png)
    }
}
```

## 第12 章：优化性能

391



进入`/path/to/xxx`目录，找到`xxx.json`。

在表达式`cvar = avar + bvar`中，加法运算符（`+`）将`avar`与`bvar`相加，得到它们的和`cvar`

在`List.of(arg0, arg1, arg2)`中，`List`接口的工厂方法`of()`接受一系列的元素，返回包含它们的只读列表。

之后我们这样调用`cmd`命令：`cmd arg0 arg1 arg2`。

```
if (condVar > someVal) {console.log("xxx")}
```



`'host' => 'localhost'`,

`'port' => 11211`,

`'persistent' => false`

);

`$cache = new Doctrine_Cache_Memcache(array(`

`'servers' => $servers`,

`'compression' => false`

)

);

// 将缓存附加到 Doctrine管理器

`$manager = Doctrine_Manager::getInstance();`

`$manager->setAttribute(Doctrine::ATTR_QUERY_CACHE, $cache);`

?>

```

一旦以这种方式初始化，Doctrine 查询缓存对所有通过 Doctrine 执行的查询都自动激活。

Doctrine 结果缓存也遵循类似的方法，如下所示：

```php
<?php

// 设置缓存驱动程序

$servers = array(

    'host' => 'localhost',

    'port' => 11211,

    'persistent' => false

);

$cache = new Doctrine_Cache_Memcache(array(

    'servers' => $servers,

    'compression' => false

)

);

// 将缓存附加到 Doctrine管理器

$manager = Doctrine_Manager::getInstance();

$manager->setAttribute(Doctrine::ATTR_RESULT_CACHE, $cache);

?>
```

但重要的是，Doctrine 结果缓存并不会对所有通过 Doctrine 执行的查询自动激活；必须通过在相应的 `Doctrine_Query` 对象上添加 `useResultCache()` 方法，显式地告诉 Doctrine 为每个查询使用此缓存。以下是这样操作的示例：

```php
<?php

class Sandbox_ExampleController extends Zend_Controller_Action

{

    public function cacheAction()

    {

        $id = $this->_getParam('id');

        $q = Doctrine_Query::create()

            ->from('Square_Model_Item i')

            ->leftJoin('i.Square_Model_Country c')

            ->leftJoin('i.Square_Model_Grade g')

            ->leftJoin('i.Square_Model_Type t')

            ->where('i.RecordID = ?', $id)

            ->addWhere('i.DisplayStatus = 1')

            ->useResultCache(true);

        $this->view->result = $q->fetchArray();

    }

}

?>
```

**注意**

如果你使用 MySQL 作为数据库，你应该知道 MySQL 自带了查询缓存，且该缓存是默认开启的。该查询缓存存储 SELECT 查询的结果集，在下一次请求相同的查询时，它从缓存中检索结果，而不是重新运行查询。但请注意，只有文本上完全相同的查询才能匹配查询缓存中的内容；任何差异都会被视为新查询。例如，`'SELECT * FROM airport'` 将不会返回缓存中 `'select * FROM airport'` 的结果。

## 优化应用程序代码

虽然缓存确实为 Web 应用程序带来显著的性能提升，但它并不是精明的应用程序开发者的唯一工具。以下章节将探讨其他常见的优化策略：

### 查询调优

有许多技术可以优化数据库查询的性能，并确保它们尽可能高效地运行。以下章节将讨论其中一些技术，特别提到了 MySQL，它是目前现代 Web 应用程序开发中最常用的数据库服务器。

#### 使用连接（Join）代替子查询

MySQL 对连接（join）的优化优于子查询，因此，如果你发现 MySQL 服务器上的平均负载达到了不可接受的高水平，请检查你的应用程序代码，并尝试将子查询重写为连接或一系列的连接。例如，以下子查询无疑是合法的：

```sql
SELECT id, name FROM movie WHERE directorid IN

(SELECT id FROM director

WHERE name = 'Alfred Hitchcock');
```

但由于 MySQL 的优化算法，以下等效的连接运行速度更快：

```sql
SELECT m.id, m.name FROM movie AS m, director AS d

WHERE d.id = m.directorid AND d.name = 'Alfred Hitchcock';
```

你还可以通过创造性地使用 MySQL 的 `ORDER BY` 和 `LIMIT` 子句将低效查询转换为更高效的查询。考虑以下子查询：

```sql
SELECT id, duration FROM movie

WHERE duration =

(SELECT MAX(duration) FROM movie);
```

使用以下查询效果更好，因为它更易读，而且运行速度快得多：

```sql
SELECT id, duration FROM movie

ORDER BY duration DESC

LIMIT 0,1;
```

#### 使用临时表处理临时数据或计算

MySQL 还允许你使用 `CREATE TEMPORARY TABLE` 命令创建临时表。这些表之所以被称为“临时”，是因为它们只在单个 MySQL 会话期间存在，并在实例化它们的客户端关闭与 MySQL 服务器的连接时，它们会被自动删除。这些表对于瞬态的基于会话的数据或计算，或数据的临时存储非常有用。而且由于它们依赖于会话，两个不同的会话可以使用相同的表名而不会冲突。

由于临时表存储在内存中，它们的速度远快于基于磁盘的表。因此，它们可以有效地作为中间存储区域，通过帮助将复杂查询分解为更简单的组件来加速查询执行，或者作为子查询的替代品。

## Zend Framework：初学者指南

它，然后请求更多数据，以此类推。在单用户环境中，这些延迟不会那么重要，因为没有其他事务会尝试访问数据库。然而，在多用户场景下，单个事务引起的延迟会对系统在队列的所有其他事务产生连锁反应，导致严重的性能下降。

尝试将大型事务拆分为较小的子事务，并独立地执行它们。这将确保每个子事务都能快速执行，从而释放出原本用于维护系统状态的宝贵系统资源。

## 优化表设计和服务器配置

本节讨论的技术都是针对应用层优化的建议。然而，为了进一步提高性能，你还应该考虑在数据库层优化性能的各种技术，例如：

- 使用索引加速搜索、分组或排序
- 选择合适的表引擎
- 指定指定的表连接字段具有相同的数据类型和长度
- 增加各种服务器端缓冲区的可用内存，例如读取缓冲区、排序缓冲区和线程缓存。

你可以在数据库服务器的手册中找到关于这些技术的更多信息。

## 懒性加载

Zend Framework 和 Doctrine 都包含了自动加载器，可以“按需”自动找到并加载类定义文件。这种技术被称为*懒性加载*（lazy loading），可以通过减少 PHP 脚本执行的文件读取次数来显著提高性能。

要激活 Zend Framework 自动加载器，Zend Framework 手册建议在应用的 *index.php* 脚本中添加以下代码：

```php
<?php

require_once 'Zend/Loader/Autoloader.php';

Zend_Loader_Autoloader::getInstance();

?>
```

为了充分利用自动加载器，有必要从你的 Zend Framework 安装中移除所有的 `require_once()` 和 `include_once()` 函数调用。Zend Framework 手册提供了一个简单的命令行脚本示例，可以自动为你完成此工作。你将在本章最后找到相关手册页的链接。

重新排列你的 PHP 包含路径也是一个好主意，使 Zend Framework 目录位于列表的顶部或靠近顶部。这是因为在尝试 `require()` 或 `include()` 文件时，PHP 会查找包含路径上的每个目录，而当目标目录位于包含路径的末尾时，这可能是一项耗时的操作。将 Zend Framework 目录移动到其他目录之前，有助于减少查找和加载包含文件的时间。

## 提高应用性能

现在让我们来看看如何利用前面节讨论的一些技术来提高 SQUARE 示例应用程序的性能。

**注意**

下节包含了关于如何在 memcached（分布式内存缓存系统）中缓存应用数据的讨论。这假设你已经安装了可以运行的 memcached 服务器以及 PHP memcached 扩展。如果你还没有这些组件，可以从章节末尾的链接从 Web 上下载。如果你的平台不可用 memcached，或者你无法让它在 PHP 中正常运行，你仍然可以通过简单地将示例配置中的第二个缓存切换为文件后端而不是内存后端，来尝试下面的示例。

### 配置应用缓存

此示例将使用两个缓存：磁盘缓存和 memcached 内存缓存。为了简单起见，此示例假设 memcached 服务器运行在本地主机上，使用默认参数，不需要特殊配置。因此，第一步是为文件缓存定义位置，然后使用 `Zend_Cache_Manager` 组件配置缓存参数。

开始之前，按照如下方式创建文件缓存目录：

```shell
shell> cd /usr/local/apache/htdocs/square/data
shell> mkdir cache
```

然后，更新位于 *$APP_DIR/application/configs/application.ini* 的应用配置文件，并为其添加以下指令：

```ini
resources.cachemanager.news.frontend.name = Core
resources.cachemanager.news.frontend.options.lifetime = 600
resources.cachemanager.news.frontend.options.automatic_serialization = true
resources.cachemanager.news.backend.name = File
resources.cachemanager.news.backend.options.cache_dir = APPLICATION_PATH "/../data/cache"
resources.cachemanager.memory.frontend.name = Core
resources.cachemanager.memory.frontend.options.lifetime = 300
resources.cachemanager.memory.frontend.options.automatic_serialization = true
resources.cachemanager.memory.backend.name = Memcached
resources.cachemanager.memory.backend.options.servers.host = localhost
resources.cachemanager.memory.backend.options.servers.port = 11211
resources.cachemanager.memory.backend.options.servers.timeout = 5
resources.cachemanager.memory.backend.options.servers.retry_interval = 10
```

完成所有配置后，让我们开始缓存吧！

### 缓存翻译字符串

`Zend_Translate` 和 `Zend_Locale` 都可以使用预配置的 `Zend_Cache` 实例来存储本地化数据和翻译字符串，以便快速查找。为这些组件设置缓存非常简单：只需向它们的静态 `setCache()` 方法传递一个配置正确的 `Zend_Cache` 实例，它们就会处理其余工作。

要为这两个组件启用缓存，请使用新的 `_initCache()` 方法更新应用引导器，如下所示：

```php
<?php

class Bootstrap extends Zend_Application_Bootstrap_Bootstrap
{
    protected function _initCache()
    {
        $this->bootstrap('cachemanager');
        $manager = $this->getResource('cachemanager');
        $memoryCache = $manager->getCache('memory');
        Zend_Locale::setCache($memoryCache);
        Zend_Translate::setCache($memoryCache);
    }
}
?>
```

### 缓存查询结果

如果你查看 `Catalog_ItemController::displayAction` 和 `AdminItemController::displayAction`，你会发现这两个操作都使用了相同的查询，区别在于前者包含一个确保目录项已批准并显示的检查。由于这段代码重复了两次，它是重构为模型方法的理想人选。要做到这一点，请将以下方法添加到 `Square_Model_Item` 类，位于 *$APP_DIR/library/Square/Model/Item.php*：

```php
<?php

class Square_Model_Item extends Square_Model_Base
{
    public function getItem($id, $active = true)
    {
        $q = Doctrine_Query::create()
            ->from('Square_Model_Item i')
            ->leftJoin('i.Square_Model_Country c')
            ->leftJoin('i.Square_Model_Grade g')
            ->leftJoin('i.Square_Model_Type t')
            ->where('i.RecordID = ?', $id);

        if ($active) {
            $q->addWhere('i.DisplayStatus = 1')
              ->addWhere('i.DisplayUntil >= CURDATE()');
        }
        return $q->fetchArray();
    }
}
?>
```

引用模型中定义的 `getItem()` 方法，而不是直接编写 Doctrine 查询。顺便使用之前定义的内存缓存缓存该方法的结果。这里是修改后的 `Catalog_ItemController::displayAction` 方法的样子：



```php
<?php

class Catalog_ItemController extends Zend_Controller_Action
{
    // 显示目录项的操作
    public function displayAction()
    {
        // 为 GET 输入设置过滤器和验证器
        $filters = array(
            'id' => array('HtmlEntities', 'StripTags', 'StringTrim')
        );
        $validators = array(
            'id' => array('NotEmpty', 'Int')
        );
        $input = new Zend_Filter_Input($filters, $validators);
        $input->setData($this->getRequest()->getParams());

        // 测试输入是否有效
        // 从缓存或数据库检索请求记录
        // 关联到视图
        if ($input->isValid()) {
            $memoryCache = $this->getInvokeArg('bootstrap')
                ->getResource('cachemanager')
                ->getCache('memory');

            if (!($result = $memoryCache->load('public_item_'.$input->id))) {
                $item = new Square_Model_Item;
                $result = $item->getItem($input->id, true);
                $memoryCache->save($result, 'public_item_'.$input->id);
            }

            if (count($result) == 1) {
                $this->view->item = $result[0];
            }
        }
    }
}
?>
```

408

Zend Framework：学者指南

```php
$this->view->images = array();

$config = $this->getInvokeArg('bootstrap')->getOption('uploads');

foreach (glob("{$config['uploadPath']}/{$this->view->item['RecordID']}_*") as $file) {
    $this->view->images[] = basename($file);
}

$configs = $this->getInvokeArg('bootstrap')->getOption('configs');

$localConfig = new Zend_Config_Ini($configs['localConfigPath']);

$this->view->seller = $localConfig->user->displaySellerInfo;

$registry = Zend_Registry::getInstance();

$this->view->locale = $registry->get('Zend_Locale');

$this->view->recordDate = new Zend_Date($result[0]['RecordDate']);

} else {
    throw new Zend_Controller_Action_Exception('Page not found', 404);
}

} else {
    throw new Zend_Controller_Action_Exception('Invalid input');
}

}

}
```

你可以对`Catalog_AdminItemController::displayAction`采用类似的方法。请查看本章的代码存档，你可以从`http://www.zf-beginners-guide.com/`下载修订后的代码。

**Q：重构模型方法如何帮助提高性能？**

**A：**第 4 节讨论了“胖模型，瘦控制器”方法，该方法建议尽可能将业务逻辑置于模型中，而不是控制器中。

除了其他各种益处外，当将此方法与缓存结合使用时，可以提高性能。正如本节稍早之前在“缓存查询结果”部分所示，如果缓存的结果数据已存在，你可以使用缓存完全阻止对模型方法的调用，从而减少需要执行的代码行数。代码行数越少，意味着脚本的解析和执行速度更快。

### 专家提问：缓存 Twitter 和博客 Feeds

在目前的实现中，`NewsController::indexAction`每次请求都会获取一组新的 Twitter 搜索结果以及最新的新闻和博客 Feeds。这些数据通过 HTTP 访问，获取成本高昂；同时，它们也是非关键的、低影响的信息。这使其成为缓存的理想目标。

## 第 12 章：优化性能

409

考虑以下`NewsController::indexAction`的修订，它使用 File 前端来缓存 Twitter 搜索结果和博客/新闻 Feeds，以提高响应时间：

```php
<?php

class NewsController extends Zend_Controller_Action
{
    public function indexAction()
    {
        // 获取 Twitter 搜索 feed
        $q = 'philately';
        $this->view->q = $q;

        // 获取缓存
        $fileCache = $this->getInvokeArg('bootstrap')
            ->getResource('cachemanager')
            ->getCache('news');
        $id = 'twitter';
        if(!($this->view->tweets = $fileCache->load($id))) {
            $twitter = new Zend_Service_Twitter_Search();
            $this->view->tweets = $twitter->search($q,
                array('lang' => 'en', 'rpp' => 8, 'show_user' => true));
            $fileCache->save($this->view->tweets, $id);
        }
        Zend_Feed_Reader::setCache($fileCache);
        $this->view->feeds = array();

        // 获取 Google News Atom feed
        $gnewsFeed = "http://news.google.com/news?hl=en&q=$q&output=atom";
        $this->view->feeds[0] = Zend_Feed_Reader::import($gnewsFeed);

        // 获取 BPMA RSS feed
        $bpmaFeed = "http://www.postalheritage.org.uk/news/RSS";
        $this->view->feeds[1] = Zend_Feed_Reader::import($bpmaFeed);
    }
}
```

从上一个列表可以看出，通过简单调用静态方法`Zend_Feed_Reader::setCache()`并传递一个配置好的`Zend_Cache`实例即可启用 Zend_Feed_Reader 缓存。

如果你衡量上述更改前后的性能，你会发现性能有了提升。为了说明，请考虑表 12-3，它显示了在 SQUARE 应用程序测试部署上使用 ApacheBench 的示例“之前”和“之后”统计数据。该报告针对共 100 次请求生成，并发级别为 10。

410

Zend Framework：学者指南

### 总结

本章是本书的最后一章，探讨了 Zend Framework 性能优化这一重要主题，讨论了一些可用的技术和选项，帮助你的应用程序挤榨出更多速度。除了提供性能分析和代码剖析工具的快速概述外，本章还研究了各种性能优化策略，包括查询和输出缓存、懒加载、SQL 查询调优和代码重构。

应用程序优化几乎是一门独立的科学，在本章有限的空间内是不可能的涵盖。然而，采用这些技术将帮助你构建更高效的应用程序，它们应该是你标准开发流程的一部分。

**Q：为什么你们没有使用 Doctrine 结果缓存来缓存查询结果？**

**A：**虽然可以使用 Doctrine 结果缓存来处理查询结果，但这不可避免地需要加载 Doctrine 模型。示例中使用的方法跳过了这一步，使得 Doctrine 模型完全没有被调用。这进一步减少了执行的代码量，并有助于提高整体性能。

### 专家提问

| URL | 不使用缓存 | 使用缓存 | 使用缓存后的提升（百分比） |
| :--- | :--- | :--- | :--- |
|  | 每秒处理的请求数 / 平均请求耗时 (ms) | 每秒处理的请求数 / 平均请求耗时 (ms) | |
| `http://square.localhost/news` | 0.45 / 2242.00 | 2.07 / 483.91 | 约 360% |
| `http://square.localhost/catalog/item/1` | 3.32 / 301.563 | 9.52 / 105.00 | 约 187% |

表 12-3：示例应用程序实施缓存前后的 ApacheBench 基准测试。

411

第 12 章：优化性能

要了解更多关于性能优化的信息并下载本章提到的某些工具，请访问以下链接：

- Zend_Cache 组件，`http://framework.zend.com/manual/en/zend.cache.html`
- Zend_Db_Profiler 组件，`http://framework.zend.com/manual/en/zend.db.profiler.html`
- 关于 Doctrine 缓存的信息，`http://www.doctrine-project.org/documentation/manual/1_1/en/caching`
- 关于 MySQL 性能优化的信息，`http://dev.mysql.com/doc/refman/5.1/en/optimization.html`
- Zend Framework 性能优化策略，`http://framework.zend.com/manual/en/performance.html`
- ApacheBench 文档，`http://httpd.apache.org/docs/2.0/programs/ab.html`
- WCAT，`http://www.iis.net/downloads/default/`

## 附录：安装与配置所需软件

415

XAMPP 是一个由社区支持的发行版，包含了最新版本的 Apache、PHP、MySQL 和 Perl。它经过完全配置，可以开箱即用，对于快速搭建基于 PHP 的开发环境来说非常受欢迎。它还包含了额外的工具，即 FTP 服务器和基于 Web 的 MySQL 管理工具。它适用于 Microsoft Windows、Mac OS X、Linux 和 Solaris，可以从`http://www.apachefriends.org/en/index.html`免费下载。

使用集成栈的缺点是，与使用第二种“自力更生”的方法相比，你学到的知识会少得多，因为所有组件都为你预先配置好了。如果你有意愿和兴趣，单独配置每个部分是一个极佳的学习体验；本附录的其余部分将进行详细讨论。

第一步是确保你已经拥有所需的所有软件。以下是列表：

### PHP

PHP 为 Web 和控制台应用程序提供了应用开发框架。可以从`http://www.php.net/`下载。在这里，Windows、UNIX 和 Mac OS X 平台均提供源码和二进制版本。UNIX 用户应该下载最新的源码归包，而 Windows 用户应该下载最新的二进制发布版本。在本书出版时，PHP 的最新版本是 PHP v5.3.1。

### Apache

Apache 是一个功能丰富的 Web 服务器，与 PHP 配合良好。可以从`http://httpd.apache.org/`免费下载源码和二进制版本，适用于多种平台。UNIX 用户应该下载最新的源码归包，而 Windows 用户应该下载与其其 Windows 版本匹配的二进制安装程序。在本书出版时，Apache 服务器的最新版本是 Apache v2.2.14。

### MySQL

MySQL 数据库服务器提供了稳健且可扩展的数据存储/检索。可以在`http://www.mysql.com/`获取源码和二进制版本。二进制发行版适用于 Linux、Solaris、FreeBSD、Mac OS X、Windows、HP-UX、IBM AIX、SCO OpenUNIX 和 SGI Irix，源码发行版适用于 Windows 和 UNIX 平台。推荐使用二进制版本，原因有两个：它更容易安装，并且经过了 MySQL 开发团队针对不同平台使用的的优化。在本书出版时，MySQL 数据库服务器的最新版本是 MySQL v5.1.43。

除了这四个基本组件外，UNIX 用户可能还需要一些支持库。以下是列表：

- `libxml2`库，从`http://www.xmlsoft.org/`获取
- `zlib`库，从`http://www.gzip.org/zlib/`获取
- `gd`库，从`http://www.boutell.com/gd/`获取

最后，两个平台的用户都需要一个能够处理 TAR（磁带存档）和 GZ（GNU Zip）文件的解压缩工具。在 UNIX 上，`tar`和`gzip`实用程序通常包含系统中。在 Windows 上，良好的解压缩工具是 WinZip，可以从`http://www.winzip.com/`获取。

***注意***

本书中的示例在 MySQL v5.1.30、Apache v2.2.14、PHP v5.3.1 以及 Zend Framework v1.9 和 v1.10 上进行了开发和测试。

## 安装与配置软件

一旦获得了所需的软件，下一步就是安装各个组件并让它们相互通信。接下来的章节概述了 Windows 和 UNIX 平台的步骤。

***注意***

如果你使用 Apple 工作站，可以在 PHP 手书中找到在 Mac OS X 上安装 PHP 的说明，地址为`http://www.php.net/manual/en/install.macosx.php`。

### 在 UNIX 上安装

UNIX 安装过程涉及许多不同的步骤：从二进制发行安装 MySQL；从源码发行编译并安装 PHP；以及编译并配置 Apache 以正确处理对 PHP Web 页面的请求。这些步骤将在后续的小节中进行详细描述。

### 安装 MySQL

要从二进制发行安装 MySQL，请使用以下步骤：

1. 确保你已以系统 root 用户身份登录。

   ```bash
   [user@host]# su - root
   ```

2. 将 MySQL 二进制归包的内容提取到系统中的适当目录——例如，`/usr/local/`。

   ```bash
   [root@host]# cd /usr/local
   [root@host]# tar -xzvf /tmp/mysql-5.1.30-linux-i686-glibc23.tar.gz
   ```

   MySQL 文件应提取到按照`mysql-version-os-architecture`格式命名的目录中——例如，`mysql-5.1.30-linux-i686-glibc23`。

3. 为了方便使用，通过在相同位置创建一个指向该目录的名为`mysql`的软链接来设置较短的。

   ```bash
   [root@host]# ln -s mysql-5.1.30-linux-i686-glibc23 mysql
   ```

4. 出于安全考虑，数据库服务器进程绝不应以超级用户身份运行。因此，有必要为此创建一个特殊的用户和组：

   ```bash
   [root@host]# groupadd mysql
   [root@host]# useradd -g mysql
   ```

5. 使用发行版包含的`install_db`脚本初始化 MySQL 表。

   ```bash
   [root@host]# chown -R mysql /usr/local
   ```

6. 修改 MySQL 二进制文件的所有权，使其归 root 所有。

   ```bash
   [root@host]# chown -R root /usr/local
   ```

7. 通过手动运行`mysqld_safe`启动 MySQL 服务器。

   ```bash
   [root@host]# /usr/local/mysqld_safe &
   ```

MySQL 现在应该启动了。

### 安装 Apache 和 PHP

PHP 可以通过两种方式集成到 Apache 服务器：作为运行时加载的动态模块，或者作为构建时集成源码树的静态模块。每种方案都有优缺点：



将 PHP 作为动态模块安装使得以后升级 PHP 构建更容易，因为你只需要重新编译模块而不是整个 Apache 服务器。另一方面，使用动态加载模块的性能往往低于静态模块。

将 PHP 作为静态模块安装可以提高性能，因为模块被直接编译进源码树。然而，这种紧密集成有一个缺点：如果你决定升级 PHP 构建，你需要将新的 PHP 模块重新集成到源码树并重新编译 Apache 服务器。

本节将介绍如何编译作为运行时加载到 Apache 服务器的动态模块。

1. 确保你已以系统 root 用户身份登录。

```bash
[user@host]# su - root
```

2. 将 Apache 源码归包的内容提取到系统的临时目录。

```bash
[root@host]# cd /tmp
[root@host]# tar -xzvf /tmp/httpd-2.2.14.tar.gz
```

3. 为了启用 PHP 的动态加载，Apache 服务器必须编译为动态共享对象（DSO）支持。通过向 Apache `configure` 脚本传递 `--enable-module=so` 选项来启用此支持，如下：

```bash
[root@host]# cd /tmp/httpd-2.2.14
[root@host]# ./configure --prefix=/usr/local/apache --enable-module=so --enable-rewrite
```

4. 现在，使用 `make` 命令编译服务器，并使用 `make` 安装到系统。

```bash
[root@host]# make
[root@host]# make install
```

5. 接下来，继续编译并安装 PHP。首先将 PHP 源码归包的内容提取到系统的临时目录。

```bash
[root@host]# cd /tmp
[root@host]# tar -xzvf /tmp/php-5.3.1.tar.gz
```

## 附录：安装和配置所需软件

419

6. 这一步是 PHP 安装过程中最重要的的一步。它涉及向 PHP `configure` 脚本传递参数以配置 PHP 模块。这些命令行参数指定了应该激活哪些 PHP 扩展，它们还告诉 PHP 在哪里找到这些扩展所需的支持库。

```bash
[root@host]# cd /tmp/php-5.3.1
[root@host]# ./configure --prefix=/usr/local/php --with-apxs2=/usr/local/apache/bin/apxs --with-zlib --with-gd --with-mysqli=mysqlnd --with-pdo-mysql=mysqlnd
```

以下是这些参数作用的简要说明：

- `--with-apxs2` 参数告诉 PHP 在哪里找到 Apache 的 APXS（APacheXtenSion）脚本。该脚本简化了构建和安装 Apache 可载入模块的任务。
- `--with-zlib` 参数告诉 PHP 激活压缩（zip）功能，这些功能被不同的 PHP 服务使用。
- `--with-gd` 参数告诉 PHP 激活图像处理功能。
- `--with-mysqli` 参数激活 PHP 的 MySQLi 扩展，并告诉 PHP 使用新的 MySQL 原生驱动（mysqlnd）作为 MySQL 客户端库。
- `--with-pdo-mysql` 参数激活 PHP 的 MySQL PDO 驱动，并告诉 PHP 使用 MySQL 原生驱动作为 MySQL 客户端库。

图 A-2：编译 Apache

![](img/222e7e58871b088cc6397852e1452b57_437_0.png)

420

Zend Framework：入门指南

7. 接下来，使用 `make` 和 `make install` 编译并安装 PHP。

```bash
[root@host]# make
[root@host]# make install
```

此时，你也可以运行 `make test` 来运行 PHP 的单元测试并检查任何失败之处。如果一切顺利，PHP 现在应该已经安装到`/usr/local/php/`。

8. 安装过程的最后一步是配置 Apache 以正确识别对 PHP 页面的请求。这是通过在文本编辑器中打开 Apache 配置文件 `httpd.conf`（位于 Apache 安装目录的 `conf/` 子目录下），并向其中添加以下行来实现：

```apache
AddType application/x-httpd-php .php
```

保存文件的更改。同时，检查文件某处是否出现了以下代码行：

```apache
LoadModule php5_module modules/libphp5.so
```

9. 通过手动运行 `apachectl` 脚本来启动 Apache 服务器。

```bash
[root@host]# /usr/local/apache/bin/apachectl start
```

Apache 应该正常启动。

一旦成功完成安装并成功启动服务器，请跳到“测试 PHP”部分，以验证所有功能均按预期方式运行。

### 在 Windows 上安装

在 Windows 上编译应用程序是一项挑战性工作，特别是对于初级开发者而言。考虑到这一点，建议 Windows 用户重点关注安装和配置 MySQL、SQLite、PHP 和 Apache 的预编译二进制发行版，而不是尝试从源代码编译它们。这些版本可以从之前在“获取软件”部分列出的网站下载，并应按照后续子节中的概述逐一个进行安装。

### 安装 MySQL

MySQL 提供了适用于 32 位和 64 位版本 Microsoft Windows 的源码和二进制形式。通常情况下，你可能想使用“精华”（Essentials）或“完整”（Complete）二进制发行版，它们包含自动化安装程序，可以在几分钟内让 MySQL 运行起来。

从二进制发行版安装 MySQL，请使用以下步骤：

1. 以管理员身份登录（如果你使用的是 Windows XP/Vista/7）。
2. 双击`mysql-*.msi`文件开始安装过程。你应该会看到欢迎界面（参见图 A-3）。
3. 选择所需的安装类型。通常情况下，使用“典型”（Typical）安装即可；但是，如果你是那种喜欢调整默认设置的人，或者如果你的磁盘空间不足，请选择“自定义”（Custom）安装选项，并决定安装包中的哪些组件。
4. MySQL 现在应该开始安装到你的系统中。
5. 一旦安装完成，你应该会看到成功通知。此时，你可以选择启动“MySQL 服务器实例配置向导”来完成软件的配置。选择此选项，你应该会看到相应的欢迎界面。
6. 选择配置类型。在大多数情况下，“标准”（Standard）配置就足够了。
7. 将 MySQL 安装为 Windows 服务，使其随 Windows 自动启动和停止（参见图 A-4）。
8. 为 MySQL 管理员（root）账户输入密码（图 A-5）。

服务器现在将根据你指定的设置进行配置并自动启动。一旦所有所需任务完成，你将收到成功通知。你现在可以按照“测试 MySQL”部分中的描述对服务器进行测试，以确保一切运行正常。

图 A-3：开始 MySQL 安装

![](img/222e7e58871b088cc6397852e1452b57_439_0.png)

420

Zend Framework：入门指南

图 A-4：设置 MySQL

![](img/222e7e58871b088cc6397852e1452b57_440_0.png)

图 A-5：设置管理员

![](img/222e7e58871b088cc6397852e1452b57_440_0.png)

安装 MySQL 完成后，下一步是安装 Apache。在 Windows 上，这是一个类似于安装 MySQL 的点击式过程。

1. 通过双击 Apache 安装程序开始。你会看到一个欢迎界面（参见图 A-6）。
2. 阅读许可协议，然后继续。

441

## 附录：安装和配置所需软件

423

### 安装 PHP

Windows 的 PHP 版本有两个——一个是包含绑定扩展并需要手动安装的 ZIP 压缩，另一个是仅基本二进制文件的自动化 Windows 安装程序。本节概述了 PHP ZIP 包的安装过程。

1. 以管理员身份登录（如果你使用的是 Windows XP/Vista/7），并将发行包解压到系统中的目录——例如 `C:\php\`。解压后，该目录看起来应该像图 A-7。
2. 接下来，将 PHP 安装目录下的 `php.ini-recommended` 文件重命名为 `php.ini`。该文件包含了 PHP 的配置设置，用于更改其工作方式。阅读文件中的注释了解更多可用设置。
3. 在 `php.ini` 文件中找到以下行：

```ini
extension_dir = "./"
```

将其修改为：

```ini
extension_dir = "c:\php\ext\"
```

这告诉 PHP 在哪里找到随包附带的扩展。记住用你 PHP 安装的实际路径替换`c:\php\`。

4. 接下来，寻找以下行，并删除开头的分号（如果有），使其变为如下：

```ini
extension=php_mysqli.dll
extension=php_pdo_sqlite.dll
extension=php_pdo_mysql.dll
extension=php_zip.dll
extension=php_gd2.dll
```

这完成了 PHP 的 MySQL、GD、Zip 和 PDO 扩展的激活。

图 A-6：开始 Apache 安装

图 A-7：解压 Windows 二进制发行包后创建的目录结构

## 附录：安装和配置所需软件

425

5. 用文本编辑器打开 Apache 配置文件 `httpd.conf`（可以在 Apache 安装目录的 `conf/` 子目录中找到它），并向其中添加以下行：

```apache
AddType application/x-httpd-php .php
LoadModule php5_module modules/libphp5.so
```

这些行告诉 Apache 如何处理 PHP 脚本以及在何处找到`php.ini`配置文件。

6. 安装 Apache 服务器后，它会将自己添加到“开始”菜单中。使用此“开始”菜单组来停止和重启服务器，如图 A-8 所示。

PHP 现在已安装并配置为与 Apache 配合。要对其进行测试，请跳到标题为“测试 PHP”的部分。

### 为 PHP 添加 memcached 支持

本书第 12 章使用了 memcached 内存缓存引擎。要为 PHP 添加对该引擎的支持，需要执行几个额外的步骤。简单而言之，步骤如下：

1. 从`http://tangent.org/552/libmemcached.html`和`http://www.monkey.org/~provos/libevent/`（仅限 NIX）下载、编译并安装 memcached 和 libevent 库。
2. 从`http://memcached.org/`（NIX 源码）或`http://code.jellycan.com/memcached/`（Windows 二进制文件）安装 memcached 服务器。
3. 从 PECL 的`http://pecl.php.net/package/memcache`（NIX 源码）或`http://downloads.php.net/pierre/`（Windows 二进制文件）安装 memcache PHP 扩展。
4. 在 PHP 配置文件中激活 memcache PHP 扩展并重启 Web 服务器使更改生效。

图 A-8

Windows 上的 Apache 服务器控制

![](img/222e7e58871b088cc6397852e1452b57_443_0.png)

426

Zend Framework：入门指南

### 测试软件

一旦安装了所有软件组件，请使用以下章节测试它们是否已正确配置并激活。

### 测试 MySQL

一旦成功安装了 MySQL，基础表已初始化且服务器已启动，您可以通过一些简单的测试验证所有操作是否运行正常。首先，切换到 MySQL 安装目录的 `bin/` 子目录并输入以下命令启动 MySQL 命令行客户端：

```text
prompt# mysql -u root
```

您应该会得到如下提示符：

```text
Welcome to the MySQL monitor. Commands end with ; or \g.

Your MySQL connection id is 26288

Server version: 5.1.30-community MySQL Community Edition (GPL)

Type 'help;' or '\h' for help. Type '\c' to clear the buffer.

mysql>
```

此时，您已连接到 MySQL 服务器，可以开始执行 SQL 命令或查询，以测试服务器是否运行正常。以下是几个示例及其输出：

```text
mysql> SHOW DATABASES;

+----------+

| Database |

+----------+

| mysql    |

| test     |

+----------+

2 rows in set (0.13 sec)

mysql> SELECT COUNT(*) FROM mysql.user;

+----------+

| count(*) |

+----------+

| 1        |

+----------+

1 row in set (0.00 sec)
```

如果您看到类似此示例的输出，说明您的 MySQL 安装运行正常。输入命令`exit`退出命令行客户端，您将返回到命令提示符。

427

## 附录：安装和配置所需软件

427

### 测试 PHP

一旦您成功作为 Apache 模块安装了 PHP，应该对其进行测试，以确保 Web 服务器能够识别 PHP 脚本并正确处理它们。

要进行此测试，请在任何文本编辑器中创建一个包含以下行的 PHP 脚本：

```php
<?php

phpinfo();

?>
```

将此文件保存为`test.php`并放在您的 Web 服务器文档根目录中（Apache 安装目录的`htdocs/`子目录），并将浏览器指向`http://localhost/test.php`。您应该能看到一个包含 PHP 编译信息的页面，如图 A-9 所示。

检查扩展列表，以确保 MySQL、GD、SimpleXML、Zip 和 memcached（可选）扩展已激活。如果它们没有激活，请重新检查安装程序以及软件附带的安装文档，以查看问题出在哪里。

图 A-9

查看`phpinfo()`命令的输出

![](img/222e7e58871b088cc6397852e1452b57_445_0.png)

428

Zend Framework：入门指南

### 设置 MySQL 超级用户密码

当首次安装 MySQL 时，对数据库的访问被限制为 MySQL 管理员，即“root”。默认情况下，该用户初始化为空密码，这通常被认为是一件坏事（Bad Thing）。因此，您应该通过内置的`mysqladmin`工具为该用户设置密码来尽快纠正这一点，在 UNIX 中使用以下语法：

```bash
[root@host]# /usr/local/mysql/bin/mysqladmin -u root password '*****new-password*****'
```

在 Windows 中，可以使用 MySQL 服务器实例配置向导，它允许您设置或重置 MySQL 管理员密码（详见“在 Windows 上安装”部分）。

此密码更改立即生效，无需重启服务器。

### 总结

流行的开源应用程序、MySQL 和 PHP 适用于各种平台和架构，包括二进制和源码形式。本附录演示了如何在两个常用平台 UNIX 和 Windows 上安装这些组件以创建 PHP 开发环境。还展示了如何配置系统每次启动时自动启动这些组件，并提供了关于 MySQL 的一些提示。

要了解更多关于本附录概述的安装过程或获取详细的故障排除建议，请访问以下页面：

- MySQL 安装说明，参见`http://dev.mysql.com/doc/refman/5.1/install-binary.html`
- UNIX Apache 通用指南，参见`http://httpd.apache.org/docs/2.2/install.html`
- Windows 版 Apache 二进制安装说明，参见`http://httpd.apache.org/docs/2.2/platform/windows.html`
- Windows PHP 安装说明，参见`http://www.php.net/manual/en/install.php`
- UNIX PHP 安装说明，参见`http://www.php.net/manual/en/install.php`
- Mac OS PHP 安装说明，参见`http://www.php.net/manual/en/install.php`

429

## 索引

- `ab` 工具，382–383
- `action` 属性，37
- 导航 `action`，358–359
- Action Message Format（AMF），3, 24
- `actions` 概览，34
- `ActionStack` 辅助类，358
- ActiveRecord 模式，105, 107
- 适配器，162–164
- 翻译文件，289–291
- `addAction` 方法，193–194
- `addContext` 方法，193–194
- `addDecorators` 方法，96
- `addDisplayGroup` 方法，93
- `addDocument` 方法，183
- `addElement` 方法，53, 93, 150
- `addField` 方法，183



- `addFilter` 方法，70–72, 75
- `addFilters` 方法，72
- `addHelper` 方法，358
- 添加记录，120–121
- `addMessage` 方法，87
- `addMultiOption` 方法，136
- `addPath` 方法，358
- `addPrefix` 方法，358
- `addslashes` 函数，70
- `addTranslation` 方法，290
- `addValidator` 方法，74, 79, 81, 92
- `addWhere` 方法，119
- `addWriter` 方法，255
- `admin` 前缀，141
- `adminDeleteAction` 方法，142
- 管理操作，140
- 控制器，141
- 布局，142–144
- 保护，167–168
- 路由，141–142
- 结构，140–141
- 日志级别，257
- `Alnum` 过滤器，73
- `Alnum` 验证器，77
- `Alpha` 过滤器，73
- `Alpha` 验证器，77, 84
- 字母数字字符串测试，74
- Amazon Web 服务，324–325
- `amazonAction` 方法，324
- AMF (Action Message Format)，3, 7
- Apache 配置文件，13

430

Zend Framework：入门指南

- Lucene 项目，181
- ApacheBench (`ab`) 工具，382–383
- Apc 缓存后端，396
- `Api_Controller` 类，335–339
- `$APP_DIR/`，11, 16
- `$APP_DIR/application/`，31–33
- `Bootstrap.php` 文件，117, 302, 357, 369
- 内容，12
- 模块，334
- `$APP_DIR/application/configs/`，229
- `navigation.xml` 文件，357
- `square.ini` 文件，230, 234
- `$APP_DIR/application/configs/application.ini` 文件
  - 管理功能，145
  - 应用配置，37
  - 缓存，405
  - Doctrine 配置，117
  - 日志位置，264
  - 登录和注销，161
  - 命名空间，85
  - 新闻页，328
  - 分页，201
  - 搜索索引位置，185
  - 排序标准，204
  - 上传目的地，213
  - 用户级配置，229–230
- `$APP_DIR/application/controller/IndexController.php` 文件，28
- `$APP_DIR/application/layouts/` 目录
  - `admin.phtml` 文件，143, 168, 233, 374
  - 布局模板文件，36
- `$APP_DIR/application/layouts/master.phtml`
  - 应用主布局，37
  - Dojo 自动完成，370
  - 表单，88
  - 本地化，298, 307
  - 菜单视图辅助，360
  - 新闻源，331
  - 搜索，179
- `$APP_DIR/application/modules/`，30–33
- `admin/views/scripts/admin-item/update.phtml` 文件，377
- `api/controllers/CatalogController.php` 文件，335
- `$APP_DIR/application/modules/controllers/`
  - `AdminItemController.php` 文件，144
  - `ItemController.php` 文件，122, 157, 215, 295
- `$APP_DIR/application/modules/catalog/views/scripts/admin-item/`
  - `index.php` 文件，146
  - `index.phtml` 文件，188
  - `update.php` 文件，156
- `$APP_DIR/application/modules/catalog/views/scripts/item/`
  - `create.phtml` 文件，138
  - `display.phtml` 文件，124, 296
  - `search.xml.phtml` 文件，194
  - `success.phtml` 文件，137

# 索引

431

- `$APP_DIR/public/fonts/` 目录, 84–85
- `$APP_DIR/public/images/` 目录, 37
- `$APP_DIR/public/images/locale/` 目录, 308
- `$APP_DIR/public/uploads/` 目录, 213, 221
- `$APP_DIR/tests/` 目录, 12
- 应用代码优化, 401
- 缓存配置, 405–406
- 缓存查询结果, 406–408
- 缓存翻译字符串, 406
- 缓存 Twitter 和博客馈送, 408–409
- 懒加载, 404–405
- 查询调优, 401–404
- `APPLICATION_ENV` 变量, 251
- `application.ini` 文件, 230
- 应用程序
  - 配置文件, 33, 37
  - 数据库初始化, 109–113
  - 环境, 7–8
  - 首页, 35
  - 互操作性, 6–7
  - 本地化和语言区域。*参见* 本地化和语言区域
  - 主布局, 36–37, 42–44
  - 优化。*参见* 应用代码优化
  - 要求, 11
  - 路由, 37–40
  - 视图, 41–42
- `ArrayIterator`，243
- 必填字段的星号 (`*`), 403
- Atom 聚合格式 (ASF), 312–313, 317–319
- `ATTR_QUERY_CACHE` 属性, 400
- 音频 CAPTCHAs, 66
- `authenticate()` 方法
  - `Square_Auth_Adapter_Doctrine`, 163–164
  - `Zend_Auth_Adapter_Interface`, 160, 162
- `authenticateAction()` 方法, 159–160
- 身份验证
  - 适配器, 162–164
  - 用户, 158–160, 170
- 自动语言区域, 276
- 自动补全助手, 358
- `autocompleteAction()` 方法, 371
- Doctrine 自动加载, 116–118

## B

- 后端, 缓存, 395–397
- 二维码验证器, 78
- `BaseName` 过滤器, 73
- 性能基准测试, 382–384
- 最佳实践, 4
- `Between` 验证器, 77
- `bin/` 目录, 9
- 全文搜索的二进制字段, 182
- `Blackhole` 缓存后端, 396
- 博客
  - 馈送, 缓存, 408–409
  - Twitter 集成, 328–332
- `Bootstrap` 类
  - Doctrine 初始化, 117
  - Dojo 视图助手, 369–370
  - 语言区域, 275–277, 293–294, 307
  - 导航对象, 352, 357
  - 查询剖析, 388–391
  - REST 路由, 340–342
  - 翻译对象, 302, 406
- 面包屑导航助手, 353–354
- 代理, 助手, 358
- 浏览器
  - 缓存, 392
  - 语言区域, 276
- Buck, Jamis, 106
- `Button` 视图助手, 364
- 表单按钮, 61–63

## C

- `cacheAction()` 方法, 393–399, 401
- `cachegrind` 文件, 385
- 缓存, 392
- 缓存管理器, 398–399
- 配置, 405–406
- Doctrine 查询, 399–401, 410
- 前端和后端, 395–397
- 操作, 392–395
- 查询结果, 406–408
- 翻译字符串, 406
- Twitter 和博客馈送, 408–409
- 瞬态计算, 402–403
- 日历。*参见* YUI 日历小组件
- 回调过滤器, 73
- 驼峰命名法, 34, 111
- 表单中的 CAPTCHA 字段, 63–65
- CAPTCHAs (全自动公开图灵测试), 66, 84
- 捕获缓存前端, 395
- `Catalog_AdminItemController` 类
  - 管理操作, 144, 146–150, 154–155
  - 数据库记录, 201–206, 218–219
- `Catalog_AdminItemController` 类（续）
  - 索引操作, 186–187
  - 日志操作, 167–168
  - YUI 日历小组件, 375–377
- `Catalog_ItemController` 类
  - 管理操作, 157–158
  - 应用配置, 236–237
  - 缓存, 406–408
  - 数据库记录, 122–124
  - 表单, 136–137
  - 语言区域, 295–296
  - 搜索, 177–178, 194
  - 上传的文件, 215–218
- `catch` 块, 242–245
- 计数验证器, 78
- CDN (内容交付网络), 363
- 过滤器, 79–81
- 继承, 106
- 方法, 54
- 表单复选框, 57–59
- 类缓存前端, 395
- `decorators()` 方法, 96
- 关闭的 PHP 标签, 41
- 代码优化。*参见* 应用代码优化
- 剖析, 384–387
- 代码生成工具, 6
- 命令行工具, 14
- 社区支持, 5
- 全自动公开图灵测试 (CAPTCHAs), 66, 84
- 组件交互, 26–28
- `configAction()` 方法, 222–227
- `ConfigController` 类, 231–233
- 配置文件, 应用程序, 33, 37
  - 定义, 229
  - 表单, 227
  - 控制器和视图, 231–233
  - 读取, 222–224
  - 主布局, 233
  - 路由, 230
  - 使用, 235–238
  - 写入, 224–227
- 一致性, 264
- `__construct()` 方法, 103
- `Square_Auth_Adapter_Doctrine`, 163
- `Square_Controller_Action_Helper`, 359
- `Square_Log_Writer_Doctrine`, 264
- 新闻馈送, 313–317
- Web 服务, 322–328
- 联系表单, 82
- Dojo 自动补全小组件, 368–369
- 本地化目标, 299–300
- `ContactController` 类, 28, 86–87, 90, 235–238, 371
- 容器, 346–351, 355–357
- `ContentPane` 视图助手, 364
- 上下文, 192–194
- `ContextSwitch` 助手, 192–194, 358
- 控制器属性, 37
- 管理控制器, 140–141
- 配置文件, 231–233
- CRUD 操作, 136–139
- 表单, 86–88
- 模型, 122–124
- MVC 模式, 23–24
- 命名规范, 34
- 新闻馈送, 328–331
- 基于 REST 的 Web 服务, 334–335
- 搜索, 177–179
- 静态内容, 40
- YUI 日历小组件, 375–377
- 货币转换, 285
- `convertNumerals()` 方法, 278–279
- `convertTo()` 方法, 286
- 版权字体, 84
- 核心缓存前端, 395
- 计数验证器, 78, 211
- 语言区域, 273–274
- `CRC32` 验证器, 78, 211
- 上传文件的创建, 215–216
- 创建、读取和删除。*参见* CRUD（创建、读取、删除）操作
- `CREATE TEMPORARY TABLE` 命令, 402
- `createAction()` 方法, 136–137, 215–216
- `createElement()` 方法, 54
- `createFulltextIndexAction()` 方法, 186–187
- `CRIT` 日志级别, 257
- 排序, 204
- 跨站请求伪造 (CSRF) 攻击, 63–64
- 跨站脚本攻击, 127
- CRUD（创建、读取、删除）操作, 130
  - 管理操作, 167–168
  - 身份验证适配器, 162–164
  - 控制器和视图, 136–139
  - 日期输入, 153
  - 删除操作, 148–150
  - 显示操作, 157–158
  - 表单, 130–136
  - 布局, 142–144
  - 列表操作和视图, 146–148
  - 登录操作和视图, 165–166
  - 登录表单, 161–162
  - 注销操作, 167
  - 主布局, 168–169
  - 路由, 141–142, 144–145, 161
  - 结构, 140–141
  - 摘要, 170–171
  - 更新操作和视图, 154–157
  - 更新表单, 150–152
  - 用户身份验证, 158–160
- CSRF (跨站请求伪造) 攻击, 63–64
- `ctype_alnum()` 函数, 74
- `ctype_alpha()` 函数, 74
- 货币语言区域, 273, 282–285
- `currencyAction()` 方法, 283–284
- `CurrencyTextBox` 视图助手, 364
- 表单自定义错误, 91–92

## D

- Data
  - 数据源 (DSN), 117–118
  - 配置文件源, 289–291, 300–301
  - 数据库, 应用程序, 109–113
- `DataMapper` 模式, 105, 107
- `date()` 方法, 281
- `date` 验证器, 78, 153
- `dateAction()` 方法, 279–282
- 表单输入, 153
- 语言区域, 273, 279–282
- `DateTextBox` 视图助手, 364
- `Db_NoRecord` 验证器, 78
- `Db_Record` 验证器, 78
- `DEBUG` 日志级别, 257
- 表单装饰, 94–99
- `Decrypt` 过滤器, 73, 211
- 默认首页, 28–30
- 默认模块, 33
- 默认路由, 25
- 表单默认值, 65–69
- 上传的文件, 213
- 开发环境, 251–252
- 操作, 148–150
- 记录, 120–121
- 上传的文件, 218–221
- `delete()` 方法
  - DQL, 121
  - 模式, 105
- `DELETE` 方法
  - HTTP, 320
  - REST 路由, 333
  - URLs, 145
- `deleteAction()` 方法, 323
  - `Api_CatalogController`, 335
  - `Catalog_AdminItemController`, 148–149, 218, 236–237, 295–296, 406–408
  - `Sandbox_RestController`, 334
- `deliciousAction()` 方法, 23
- 拒绝访问, 170
- `description()` 方法, 317
- `/dev/null` 文件, 256
- `Dir` 过滤器, 73
- `disable()` 方法, 370
- 选项, 289
- 禁用装饰器, 96
- 磁盘缓存, 示例, 405–406
- 内存缓存, 399
- 显示操作, 157–158
- `display_errors` 变量, 251
- 表单中的组, 93–94
- `display()` 方法, 203
- `display_startup_errors` 变量, 251
- `displayAction()` 方法
  - `Catalog_ItemController`, 123–124, 157–158, 216–218, 236–237, 295–296, 406–408
  - `ItemController`, 138
  - `StaticContentController`, 40
- `Doctrine_Manager` 类, 118, 400
- `Doctrine_Pager` 类, 201, 203, 238
- `Doctrine_Pager_Layout` 类, 203, 206
- `Doctrine_Query` 类, 119, 399, 401
- Doctrine 查询语言 (DQL), 107, 118
- `Doctrine_Record` 类, 118
- Doctrine 工具, 22
  - 添加、更新和删除记录, 120–121
  - 自动加载, 116–118
  - 数据库查询, 390–391
  - 安装, 107–109
  - 模型生成, 113–115
  - 模型关系, 115–116
  - 查询缓存, 399–401, 410
  - 记录检索, 118–120, 122
  - 文档, 7
- Dojo 自动补全小组件, 368
  - 控制器, 371
  - 表单, 368–369
  - 主布局, 370
  - 视图助手, 369–370
- `dojo.data.ItemFileReadStore` 数据存储, 361
- `dojo.data.ItemFileWriteStore` 数据存储, 361
- Dojo Toolkit, 7, 346, 361
  - 数据, 361–362
  - 表单元素, 365–367
  - 视图助手, 362–365
- `dojoAction()` 方法, 361



- 语言区域中的美元（`$`）符号，273

- `DOMDocument` 类，315

- `DOMElement` 类，315

- `DOMXPath` 类，315

- 不要重复（DRY）原则，106

- 双重提交问题，137

- `DQL`（Doctrine 查询语言），107, 118

- `DRY`（不要重复）原则，106

- `DSN`（数据源名），117–118

- `<dt>` 元素，95, 98

- `dump()` 方法，254

- `DuplicateFileException` 类，244

## E

- `EC2`，2

- `Editor` 视图助手，364

- 效率，264

- 邮箱地址
  - 更新，90
  - 有效性检查，74

- `EmailAddress` 验证器，78

- `EMERG` 日志级别，257

- `enable()` 方法，370

- `enableView()` 方法，363, 370

- `Encrypt` 过滤器，73, 211

- `$_ENV` 变量，254

- 环境语言区域，276

- `ERR` 日志级别，257

- 错误处理
  - 默认过程，246–249
  - 错误页面，252–254
  - 异常类，249–251
  - 异常概述，242–246
  - 异常可见性，251
  - 日志数据，*参见* 日志数据
  - 摘要，268–269

- 表单的错误信息，50, 91–92

- 错误页面，252–254

- `errorAction()` 方法，246–247, 250–251, 265–266

- `ErrorController` 类，246–247, 250–251, 265–266

- `Errors` 装饰器，95

- `escape()` 方法，126

- 转义输出，126–127

- `ExampleController` 类，51–52, 82

- 异常类，244–246

- 异常
  - 自定义类，249–251
  - 日志，263–265
  - 概述，242–246
  - 可视性，251

## 索引（第 435 页）

- `fetchArray()` 方法，190

- 字段（fields），55–57, 60–61, 63–65
  - 索引连接（index join），403
  - 必填（required），403
  - 搜索（search），182

- `Fieldset` 装饰器，95

- 文件缓存后端，396

- 文件缓存前端，395

- 文件上传（file uploads）
  - 字段，60–61
  - 处理，209–212
  - `$_FILES` 超全局，209

- `FilesSize` 验证器，78, 211

- 基于过滤的数据库查询 vs. 全文搜索，192

- `filter_var()` 函数，74

- `FilteringSelect` 视图助手，364

- 过滤器（filters）
  - 链式，79–81
  - 表单，52, 70–73, 135
  - 记录检索，119
  - 上传的文件，210–211

- `find()` 方法
  - `Doctrine`，118, 155
  - `DQL`，121
  - `Zend_Search_Lucene`，184, 190

- `findAll()` 方法，118

- `findBy()` 方法，351, 359

- `findCheapestShippingProvider()` 方法，396

- `Firebug` 控制台，263, 389–391

- 500 异常，248, 253

- `FlashMessenger` 工具，87, 358

- 浮点数验证器，77

- 流式接口（fluent interfaces），119

- 字体，受版权保护的，84

- 外键关系，116

- `Form_Example` 类，53–69
  - 装饰器，96–98
  - 显示分组，93–94
  - Dojo 表单，365–367
  - 错误消息，91–92
  - 输入过滤器，70–72
  - 输入验证器，73–77
  - 上传的文件，209–213

- `Form_Item_Create` 类，51

- `formAction()` 方法
  - `ExampleController`，52, 82
  - `Sandbox_ExampleController`，210

- 格式（formats）
  - 日期，153
  - 日志消息，255, 257
  - 新闻订阅，313

- 格式化日志消息，259–263

- `FormElements` 装饰器，95

- `FormErrors` 装饰器，95

- 表单（forms）
  - 基础，48–52
  - 按钮，61–63
  - 配置，227–229
  - 联系，82
  - 控制器和视图，86–88
  - 日期输入，153
  - 装饰器，94–99
  - 定义，82–85, 130–136
  - 显示分组，93–94
  - Dojo，365–369
  - 元素创建，53–55
  - 错误消息，50, 91–92
  - 上传的文件，60–61, 209–215
  - 过滤器链，79–81
  - `Hash` 和 `CAPTCHA` 字段，63–65
  - 输入过滤器，70–73
  - 输入获取和处理，81–82
  - 输入验证器，73–81
  - 本地化目标，299–300
  - 登录，161–162
  - 主布局，88–89
  - 命名空间，85
  - 单选按钮和复选框，57–59
  - 必填和默认值，65–69
  - 路由，85–86
  - 搜索，174–177, 188–189
  - 选择列表，59–60
  - 摘要，99–100
  - 文本和隐藏字段，55–57
  - 更新，150–152
  - YUI 日历小部件，372–374

- `_forward()` 方法，337

- 404 异常，124, 158, 248, 253

- `Fowler, Martin`，105

- 前置控制器（front controllers），24, 27

- 前端，缓存，395–397

- 全文搜索，181–182
  - vs. 基于过滤的数据库查询，192
  - 索引动作和视图，186–187
  - 索引位置，185
  - 数据索引，182–184
  - 路由，186
  - 搜索动作和视图，189–191
  - 搜索表单，188–189
  - 数据搜索，184–185
  - 摘要视图，188

- 完整版本，9

- 函数缓存前端，395

## G

- `GData` APIs，3

- `generateModelsFromDb()` 方法，114–116

- 通用客户端 Web 服务实现，325–328

- `geocode()` 方法，326

- `GeoCoder` Web 服务，325

- `GET` 动作，156

- `HTTP`，320

- 基于 `REST` 的 Web 服务，336–338

- `REST` 路由，333

- `get()` 方法
  - 日期时间，280
  - `Zend_Registry`，302
  - `Zend_Rest_Client`，327

- `getAction()` 方法
  - `Api_CatalogController`，335, 337–338
  - `Sandbox_RestController`，333

- `getCache()` 方法，399

- `getCode()` 方法，244

- `getContainer()` 方法，359

- `getContent()` 方法，315

- `getCountries()` 方法，135–136

- `getDateCreated()` 方法，315

- `getDateModified()` 方法，315

- `getDescription()` 方法，315

- `getDocument()` 方法，315

- `getElapsedSec()` 方法，388

- `getElement()` 方法，315

- `getEnv()` 方法，254

- `getFile()` 方法，244

- `getGrades()` 方法
  - `Square_Form_ItemCreate`，135–136
  - `Square_Form_Search`，176

- `getHelper()` 方法，358

- `getIdentity()` 方法，160

- `getInvokeArg()` 方法，187

- `getItem()` 方法，406–407

- `getLabel()` 方法，348

- `getLanguage()` 方法，275

- `getLastRequest()` 方法，328

- `getLastResponse()` 方法，328

- `getLine()` 方法，244

- `getLink()` 方法，315

- `getMessage()` 方法，244

- `getMessages()` 方法
  - `FlashMessenger`，87
  - `Zend_Form`，81

- `getParam()` 方法，40

- `getParams()` 方法，254

- `getQuery()` 方法，388

- `getQueryProfiles()` 方法，388

- `getRegion()` 方法，275

- `getRel()` 方法，348

- `getResource()` 方法，238

- `getResultArray()` 方法，164

- `getRev()` 方法，348

- `getServer()` 方法，254

- `getSql()` 方法，120

- `getTimezone()` 方法，282

- `getTitle()` 方法，315

- `getTrace()` 方法，244

- `getTraceAsString()` 方法，244

- `getTransferAdapter()` 方法，216

- `getTranslationList()` 方法，279

- `getTypes()` 方法，135–136

- `getUnfilteredValues()` 方法，81

- `getValues()` 方法，81, 210

- `getVideoFeed()` 方法，324

- `getVisibility()` 方法，348

- `getXPath()` 方法，315

- `glob()` 函数，217

- `GNU gettext`，291–292

- 授予访问权限，170

- `GreaterThan` 验证器，78

- `groupBy()` 方法，119

- 分组
  - 显示，93–94
  - 结果，119

- `Gutmans, Andi`，2

- `handleInputDisplay()` 函数，153, 156

- `Hartjes, Chris`，106

- `Hash` 字段，63–65

- `Hash` 验证器，78, 211

- `hasIdentity()` 方法，160, 168

- `hasMany()` 方法，115

- `hasOne()` 方法，115

- `header()` 方法，318

- `HeadLink` 视图，374–375, 377

- `HeadScript` 视图，374–375, 377

- 助手，358

- 助手，视图，362–365, 369–370

- `Hex` 验证器，77

- 隐藏字段，55–57

- `HorizontalSlider` 视图，364

- `Hostname` 验证器，78

- `.htaccess` 文件，27, 251

- `HtmlEntities` 过滤器，73, 135

- `htmlentities()` 函数，70

- `HtmlTag` 装饰器，95, 153

- `HTTP POST` 方法，320

- `HTTP` 请求，369

- `httpd.conf` 文件，13

- `httpd-hosts.conf` 文件，13

## I

- `Iban` 验证器，78

- `Identical` 验证器，77

- `IETF`（Internet Engineering Task Force）标准，313

- `IGNORE` 关键字，402–403

- 图像按钮，62

- 图像上传，*参见* 上传的文件

- `ImageSize` 验证器，78, 211

- `Imind Doctrine` 剖析器，390–391

- `Imind_Profiler_Firebug` 类，390

- `Imind` 项目，390

- `import()` 方法，315

- `importArray()` 方法，317–318, 337

- `importFile()` 方法，316

- `importString()` 方法，316

- `InArray` 验证器，77, 204

- `include()` 方法，226, 405

- `include_once()` 函数，404

- 索引连接，403

- 索引页面
  - 应用，35
  - 默认，28–30

- `index.php` 脚本，27

- `index.phtml` 文件，35

- `indexAction()` 方法
  - `Api_CatalogController`，335–337
  - `Catalog_AdminItemController`，146, 201–206
  - `ConfigController`，231–233
  - `ContactController`，86–87, 90, 235–236
  - `IndexController`，28, 35, 37
  - `LocaleController`，306–307
  - `NewsController`，28, 328–329, 408
  - `PostController`，28
  - `Sandbox_ExampleController`，183
  - `Sandbox_RestController`，333

- `IndexController` 类，27–28, 35

- 索引
  - 动作，186–187
  - 数据库记录，201–204
  - 索引过程，182–184
  - 位置，185

- `INFO` 日志级别，257

- 继承链，106

- `ini_set()` 函数，15

- `init()` 方法，142
  - `Api_CatalogController`，335
  - `Catalog_ItemController`，122–123, 194
  - `ConfigController`，231
  - `ContactController`，86–87
  - `Form_Example`，53–77, 91–92, 97–98, 209–213, 365–367
  - `Form_Item_Create`，51
  - `IndexController`，28
  - `LoginController`，165
  - `Sandbox_ExampleController`，192
  - `Square_Form_Configure`，228–229
  - `Square_Form_Contact`，83–84, 299, 368–369
  - `Square_Form_ItemCreate`，130–136, 213–214
  - `Square_Form_ItemUpdate`，150–152, 372–374
  - `Square_Form_Login`，161–162
  - `Square_Form_Search`，175–176, 188–189
  - `StaticContentController`，40

- `_initCache()` 方法，406

- `initContext()` 方法，194

- `_initDatabase()` 方法，388–390

- `_initDoctrine()` 方法，117–118, 390–391

- `_initDojo()` 方法，370

- 初始化
  - 数据库，109–113
  - Dojo 视图助手，369–370
  - REST 路由，340–342

- `_initLocale()` 方法，275–277, 294, 307

- `_initNavigation()` 方法，352, 357

- `_initRoutes()` 方法，340–341

- `_initTranslate()` 方法，293–294, 302

- `innerJoin()` 方法，119

- 输入表单
  - 日期，153
  - 过滤器，70–73
  - 获取和处理，81–82
  - 验证器，73–81

- `INSERT...SELECT` 语法，402–403

## 安装

- `Doctrine`，107–109
- `Zend Framework`，8–10

- 过滤器，73

- 验证器，77

- 国际化，5

- 互联网任务组（IETF）标准，313

- 应用程序互操作性，6–7

- "Invalid input"错误，126

- 验证器，78

- `is_numeric()` 函数，74

- `is_uploaded_file()` 方法，244

- 验证器，78, 211

- 验证器，78, 160

## J

- 索引连接，403

- 连接（joins），119–120
  - vs. 数据库记录，201–402

- `JSON` 助手，354

- 工具包，318

## K

- `KeyGrind` 工具，385

- 表单中的字段，63–65



# 索引

## 全文搜索

- 全文搜索，181–182
- KISS (Keep It Simple!) 原则，403

## L

- 标签装饰器，95
- 本地化语言，273–274
- 布局
  - 主布局，*见*
  - 概览，272–74
  - 懒加载，116, 404–405
- 语言连接器，116
- 验证器，78
- 库
  - 增加，13
  - `Zend_Form`，81
  - 库目录，13
  - 库生命，372
- 链接助手，354
- 列表动作，146–148
- 列表动作方法，193, 337
- 列表控制器，24–25
- 加载，395
- 加载
  - 缓存数据，395
  - `Doctrine`，116–118
  - 懒加载，404–405
  - 本地化标识，273–274
- 本地化动作方法，274–275, 292–293
- 本地化控制器，306–307
- 本地化和区域化，272–274
  - 设置，274–277, 294
  - 货币，282–285
  - 日期和时间，279–282
  - 手动选择，306–307
  - 主布局，307–308
  - 测量值，285–287
  - 数字，277–279, 294–295
  - 概览，272–274
  - 字符串，287–294, 298–300
  - 翻译对象注册，302–305
  - 翻译来源，300–301
- 本地化到归一化过滤器，73
- `log()` 方法，255–256
- `logAction()` 方法，254–262
- 记录数据，254
  - 将数据添加到日志消息，259
  - 错误控制器，265–268
  - 格式化日志消息，259–263
  - 日志位置，263–264
  - 日志写入器，264–265
  - 写入日志消息，254–259
- 登录动作方法，162, 165–166, 168
- 登录控制器类，162, 165–167
- 登录
  - 动作和视图，165–166
  - 认证适配器，162–164
  - 表单，161–162
  - 路由，161
  - 注销动作，167

索引

439

- `logoutAction()` 方法, 167
- 松松耦合架构, 3, 5–6
- `LowerCase` 过滤器, 73, 211
- 小写翻译键, 306
- Lurz, Matthew, 265

## M

- 手动区域选择, 306–307
- 多对多关系, 115–116
- 市场信誉, 6
- 主布局, 33
- 管理操作, 142–144
  - 应用程序, 36–37, 42–44
  - 配置文件, 233–235
  - CRUD 操作, 168–169
  - Dojo 自动完成组件, 370
  - 表单, 88–89
  - 本地化, 307–308
  - 新闻订阅, 331–332
  - 搜索, 179–181
  - 存储, 39
  - YUI 日历组件, 374–375
- `Md5` 验证器, 78, 211
- `measureAction()` 方法, 285–287
- 测量区域, 285–287
- `MemberModel` 类, 103
- `Memcached` 缓存后端, 396
- 内存缓存
  - 与磁盘缓存对比, 399
  - 示例, 405–406
- 菜单
  - 导航结构, 352–353
  - 导航视图辅助器, 359–360
  - 方法, 24
  - 链式, 54
  - SOAP, 322
- Microsoft CardSpace, 7
- `MimeType` 验证器, 78, 211
- 最小版本, 9
- `MissingFileException` 类, 244
- `mktime()` 函数, 279
- 模型-视图-控制器 (MVC) 模式, 3, 21
  - 控制器, 23–24
  - 模型, 21–22
  - 视图, 22–23
- 模型, 102
  - 应用程序数据库, 109–113
  - 控制器, 122–124
  - 生成, 113–115
  - 模块创建, 122
- MVC 模式, 21–22
  - 概述, 102–105
  - 模式, 105
  - 记录检索, 118–120, 122
  - 关系, 115–116
  - 路由, 122
  - 范围, 105–106
  - 总结, 127–128
  - 视图, 124–127
- 模块属性, 37
- 模块
  - 创建, 122
  - 默认, 33
  - 概述, 24–25
- 基于 REST 的 Web 服务, 334
- `mooTools` 工具包, 346
- `move_uploaded_file()` 方法, 209
- `multipart/form-data` 类型, 61
- 多重输出类型, 192–193
- 多选列表, 59–60
- MVC (模型-视图-控制器) 模式, 3, 21
  - 控制器, 23–24
  - 模型, 21–22
  - 视图, 22–23
- MySQL 数据库
  - 初始化, 109–113
  - 表名, 111

## N

- 名称
  - 控制器、动作和视图, 34
  - 数据库表, 111
  - 表单的命名空间, 85
- `navAction()` 方法, 347–348, 350–351
- 导航结构, 346
  - 动作辅助器, 358–359
  - 面包屑 (Breadcrumbs), 353–354
  - 链接 (Links), 354
  - 菜单视图辅助器, 359–360
  - 菜单, 352–353
  - 页面和容器, 346–351, 355–357
  - 注册导航对象, 357
  - 渲染, 351–355
  - 站点地图 (Sitemap) 辅助器, 354–356

Zend Framework: 初学者入门指南

- 新闻订阅
  - 消费, 313–317
  - 控制器和视图, 328–331
  - 创建, 317–319
  - 格式, 313
  - 主布局, 331–332
  - 路由, 328
  - Twitter 和博客搜索集成, 328–332
  - 使用, 312–313
- `NewsController` 类, 28, 328–329, 408–409
- `NormalizedToLocalized` 过滤器, 73
- `NotEmpty` 验证器, 67, 77, 84
- NOTICE 日志级别, 257
- `numberAction()` 方法, 278–279
- 数字
  - 本地化, 277–279, 294–395
  - 测试, 74
- `NumberSpinner` 视图辅助器, 364

## O

- 面向对象编程 (OOP) 架构, 4
- 对象关系映射 (ORM), 22, 107
- SOAP 中的对象, 322
- OCR (光学字符识别) 算法, 84
- 一对多关系, 115
- 一对一关系, 115
- OOP (面向对象) 架构, 4
- 字节码缓存, 39
- `open()` 方法, 184
- 开源项目, 5
- Phinney, Matthew, 116, 153
- OCR (光学字符识别) 算法, 84
- 性能优化. *见* 性能
- `orderBy()` 方法, 119
- ORM (对象关系映射) 工具, 22, 107

## P

- 页面缓存, 395
- 页面级缓存, 392
- “页面未”错误, 126
- `pageAction()` 方法, 348
- 页面和分页, 200–201
  - 索引控制器和视图, 201–204
  - 导航, 355–357
  - 路由, 201
- `parse()` 方法, 184
- 表单验证, 74
- 模型, 105
- PEAR Benchmark 类, 385, 387
- PEAR Services 包, 285
- 日志中的百分比 (%) 符号, 259
- 性能
  - 应用代码. *见* 应用代码
  - 性能基准, 382–384
  - 代码分析, 384–387
- 重构模型方法, 410
- PHP 优势, 2–3
- `php.ini` 配置文件, 87
- `populate()` 方法, 156
- POST 动作
  - 上传, 209
  - HTTP, 320
  - REST 路由, 333
- `post()` 方法, 327
- `postAction()` 方法
  - `Api_CatalogController`, 335
  - `Sandbox_RestController`, 333–334
- `PostController` 类, 28
- `postDispatch()` 方法, 144, 358
- `preDispatch()` 方法, 142–143, 358
  - `Catalog_AdminItemController`, 167–168
  - `ConfigController`, 231, 233
  - 描述, 144
  - `Square_Controller_Action_Helper`, 359
- `preg_match()` 函数, 74
- 处理表单输入, 81–82
- 生产环境中的异常, 251–252
- 配置文件, 16
- 代码, 384–387
- Propel 工具, 22, 107
- 保护管理操作, 167–168
- `protectedAction()` 方法, 160
- PUT 动作
  - 上传, 209
  - HTTP, 320
  - REST 路由, 333
- `put()` 方法, 327
- `putAction()` 方法
  - `Api_CatalogController`, 335
  - `Sandbox_RestController`, 333–334

## Q

- 查询
  - 缓存结果, 406–408
  - Doctrine, 399–401
  - 代码分析, 387–392
  - 调优, 401–404
- `queryAction()` 方法, 386–389

## R

- 表单单选按钮, 57–59
- 快速发布周期, 6
- 读取配置文件, 222–224
- 简单信息摘要 (RSS) 格式, 312–313
- `RealPath` 过滤器, 73
- `receive()` 方法, 214, 216
- 记录
  - 添加、更新和删除, 120–121
  - 分页和排序, 201–208
  - 检索, 118–120, 122
- `RecursiveIteratorIterator` 类, 351
- RedBean 工具, 107
- Redirector 辅助器, 358
- 重构模型方法, 410
- Regex 验证器, 78, 135
- 注册
  - 导航对象, 357
  - 翻译对象, 302–305
- 表单验证的正则表达式, 74
- 模型中的关系, 115–116
- 远程 HTTP 请求, 369
- `removeElement()` 方法, 150
- `removeHelper()` 方法, 358
- Rename 过滤器, 73
- Rename 验证器, 211
- 渲染导航元素, 351–355
- `renderMenu()` 方法, 352
- 表象层状态转移 (REST) 架构, 320–322, 328
- `require()` 方法, 227, 404
- `require_once()` 方法, 404
- 必填字段, 403
- 必填值, 65–69
- 应用, 11
- SOAP 中的资源, 322
- REST (表象层状态转移) 架构, 320–322, 328
- 基于 REST 的 Web 服务, 332
  - 控制器, 334–335
  - GET 动作, 336–338
  - 模块, 334
  - POST 动作, 339
  - 路由, 332–334, 340
- `restAction()` 方法, 327
- 查询结果缓存, 406–408
- 记录, 118–320, 122
- 可用用, 4
- 右连接, 120
- 路由属性, 37
- 路由, 33
- 行锁, 403

## S

- `Sandbox_ExampleController`
  - 管理操作, 142–144
  - 缓存管理器, 398–399
  - 缓存操作, 393–394
  - 查询缓存, 400–401
  - 代码分析, 386–387
  - 配置文件, 222–227
  - 货币区域, 283–285
  - 日期和时间区域, 279–282
  - Dojo, 361–362
  - 异常, 247, 249
  - 索引, 183–184
  - 区域, 274–277
  - 日志, 254–262
  - 测量区域, 285–287
  - 模型, 104–105
  - 多重输出类型, 192–193
  - 页面和容器, 347–348, 350–351
  - 新闻订阅消费, 313–317
  - 新闻订阅创建, 317–319
  - 数字区域, 277–279
  - 查询分析, 388–389
  - 字符串区域, 287–288, 290–293
  - 上传文件, 210
  - 用户身份验证, 159–160
- Web 服务, 323–327
- `Sandbox_RestController` 类, 333–334
- Savant 模板引擎, 23
- `save()` 方法
  - Doctrine, 155, 265
  - DQL, 121
  - 表单, 137
  - MemberModel, 103–104
  - 模式, 105
- Zend, 395
- `saveAction()` 方法, 104–105
- `saveXml()` 方法, 318
- 模型范围, 105–106
- `search()` 方法, 329
- `searchAction()` 方法, 194–195
  - `Catalog_ItemController`, 177–178, 189
  - `Sandbox_ExampleController`, 184
- 搜索
  - 控制器和视图, 177–179
  - 表单, 174–177
  - 全文. *见* 全文搜索
  - 主布局, 179–181
  - 总结, 196–197
- XML, 194–196
- 表单中的选择列表, 59–60
- 自引用关系, 115
- `send()` 方法
  - `Zend_Feed`, 318, 337
  - `Zend_Mail`, 87
- `sendAction()` 方法, 28
- `$_SERVER`, 254, 276
- 服务器配置, 404
- 特定服务的客户端服务实现, 322–325
- `set_error_handler()` 函数, 243
- `set_exception_handler()` 函数, 243
- `set()` 方法, 302
- `setAction()` 方法, 53
- `setAttribs()` 方法, 53
- `setAutoInsertNotEmptyValidator()` 方法, 67
- `setCache()` 方法, 406, 409
- `setCdnBase()` 方法, 363
- `setCheckedValue()` 方法, 58
- `setData()` 方法, 124
- `setDecorators()` 方法, 96, 98, 177
- `setDefaults()` 方法, 67
- `setDescription()` 方法, 54
- `setDestination()` 方法, 210, 216
- `setElementDecorators()` 方法, 177
- `setEnctype()` 方法, 61
- `setEventItem()` 方法, 259–260, 266
- `setFacility()` 方法, 258
- `setFormat()` 方法, 284
- `setFormatter()` 方法
  - `Square_Log_Writer_Doctrine`, 264
  - `Zend_Log_Writer`, 255
- `setImage()` 方法, 62
- `setLabel()` 方法, 54, 348
- `setLayout()` 方法, 144
- `setLegend()` 方法, 93
- `setLocale()` 方法, 276, 289
- `setLocalPath()` 方法, 363
- `setMessage()` 方法, 92
- `setMethod()` 方法, 53
- `setMultiFile()` 方法, 61, 214
- `setMultiOptions()` 方法, 58–59
- `setOptions()` 方法, 54
- `setPartial()` 方法, 352
- `setRel()` 方法, 348
- `setRequired()` 方法, 65, 67
- `setResultSetLimit()` 方法, 185
- `setRev()` 方法, 348
- `setTimezone()` 方法, 282
- `setUncheckedValue()` 方法, 58



# 索引

## S

- `setUp()` 方法, 115–116
- `setValue()` 方法, 67
- `setValueDisabled()` 方法, 214
- `setVisibility()` 方法, 348
- `Sha1` 验证器, 78, 211
- 共享主机环境, 15
- Simple对象访问协议 (SOAP), 312, 320–322, 328
- `SimpleXML` 类, 195, 327
- 单数控制器，创建, 140
- 单选列表, 59–60
- 站点地图辅助器, 354–356
- 大小验证器, 78, 211
- 应用程序骨架, 11
- 小额交易, 403–404
- `Smarty` 模板引擎, 23
- SOAP (简单对象访问协议), 312, 320–322, 328
- `soapAction()` 方法, 325
- 记录排序, 204–208
- `<span>` 元素, 176
- `Sqlite` 缓存后端, 396
- SQS Web 服务, 3
- SQUARE 管理控制面板, 140
- `Square_Auth_Adapter_Doctrine` 类, 163–164
- `Square_Controller_Action_Helper_Navigation` 类, 359
- SQUARE 示例应用, 11
- `Square_Form_Configure` 类, 228–229
- `Square_Form_Contact` 类, 83–84, 87, 299, 368–369
- `Square_Form_ItemCreate` 类, 130–136, 213–214
- `Square_Form_ItemUpdate` 类, 150–152, 372–374
- `Square_Form_Login` 类, 161–162
- `Square_Form_Search` 类, 175–177, 188–189
- `Square_Log_Writer_Doctrine` 类, 264–265
- `Square_Model_Item` 类, 116, 406–407
- `StackContainer` 视图辅助器, 364
- 堆叠过滤器, 79–81
- 标准合性, 4
- `start()` 方法, 385
- 项目启动, 10–16
- 静态缓存后端, 396–397
- 静态内容
  - 控制器, 40
  - 路由, 39–40
- `StaticContentController` 类, 39–40
- `stop()` 方法, 385
- 存储配置文件, 230
- 字符串转换操作, 65
- `StringLength` 验证器, 77
- 字符串
  - 本地化, 287–294, 298–300
  - 测试, 74
- `StringToLower` 过滤器, 73
- `StringToUpper` 过滤器, 73
- `StringTrim` 过滤器, 73, 135
- `strip_tags()` 函数, 70
- `StripNewlines` 过滤器, 73
- `StripTags` 过滤器, 73
- `strtoupper()` 函数, 306
- 结构
  - 行政管理操作, 140–141
  - 导航。*参见*导航结构
  - 子查询与连接的区别, 401–402
- `successAction()` 方法
  - `Catalog_AdminItemController`, 149–150, 155
  - `Catalog_ItemController`, 136–137
  - `ConfigController`, 232–233
  - `ContactController`, 86–87
  - `LoginController`, 166
  - 全文搜索的摘要视图, 188
  - 支持, 5, 7
- Suraski, Zeev, 3
- `switch-case()` 例程, 251
- 在生产环境和开发环境之间切换, 251

## T

- `TabContainer` 视图辅助器, 364
- 表名, 111
- 表
  - 设计, 404
  - 连接, 119–120
  - 瞬态数据和计算, 402–403
- Technorati 服务, 7
- 模板文件, 36–37
- 临时表, 402–403
- 测试缓存后端, 396
- 文本字段
  - 表单, 55–57
  - 全文搜索, 182
- `Textarea` 视图辅助器, 364
- `TextBox` 视图辅助器, 364
- 第三方应用互操作性, 6–7
- `Ticket` 模型, 103
- 时间，本地化, 279–282
- `TimeTextBox` 视图辅助器, 364
- 时区, 282
- `title()` 方法, 317
- `toArray()` 方法, 362
- Zend 框架: 初学者指南, 444
- `toCurrency()` 方法, 283
- `toJson()` 方法, 362
- `toNumber()` 方法, 277–278, 295
- 瞬态数据和计算, 402–403
- `translate()` 函数, 306
- `translateAction()` 方法, 288, 290–291
- 翻译文件, 287–288
  - 适配器和数据源, 289–291
- 翻译区域, 291–293
  - 数据源, 300–301
  - 视图辅助器, 293–294
- 翻译键, 306
- 翻译对象，注册, 302–305
- 翻译字符串，缓存, 406
- `try` 块, 242–245
- Twitter 服务, 7
  - 博客集成, 328–332
  - 缓存馈送, 408–409

## U

- `first()` 函数, 306
- `<ul>` 元素, 95
- 区域中的下划线 (`_`), 273
- 全文搜索中的索引字段, 182
- 缓存的唯一标识符, 393
- `UNIQUE` 关键字, 403
- 单元测试策略, 6
- 全文搜索中的存储字段, 182
- 更新表单, 150–152
- `update()` 方法, 105, 121
- 上传的文件, 209–212
- `updateAction()` 方法, 153–155, 375–376
- 更新
  - 应用配置, 37
  - 显示操作, 157–158
  - 记录, 120–121, 154–157
  - 创建操作, 215–216
  - 删除操作, 218–221
  - 目标, 213
  - 表单定义, 213–215
- 大写转换, 111
- 大写过滤器, 73, 211
- `url()` 方法, 38, 42–43, 88, 148–179
- URLs
  - 表单, 136
  - 路由, 39–40, 144–145
  - 排序标准, 206, 208
- 有效性检查, 74
- 用户访问控制, 170
- 用户身份认证, 158–160, 170
- 用户界面
  - Dojo Toolkit, 361–371
  - 导航结构。*参见*导航结构
  - 概述, 346
  - YUI 日历组件, 372–378
- `useResult()` 方法, 401
- UTF-8 编码, 301

## V

- 表单中的验证, 50
- `ValidationTextBox` 视图辅助器, 364
- 验证器, 52
  - 输入, 73–81
  - 上传的文件, 210–211
- `var_dump()` 函数, 254
- `VerticalSlider` 视图辅助器, 364
- 视图辅助器, Dojo, 362–365, 369–370
- 视图装饰器, 95
- `ViewRenderer` 辅助器, 358
- 视图
  - 应用, 41–42
  - 配置文件, 231–233
  - CRUD 操作, 136–139, 146–148
  - 表单, 86–88
  - 全文搜索, 186–187, 189–191
  - 登录, 165–166
  - 模型, 124–127
  - MVC 模式, 22–23
  - 命名规范, 34
  - 新闻馈送, 328–331
  - 分页, 201–204
  - 搜索, 177–179
  - XML, 194–196
  - 虚拟主机, 13–14
- 异常的可见性, 251

## W

- `WARNING` 级别, 257
- WCAT (Web 容量工具), 383–384
- WDDX (Web 数据交换), 312
- Web 浏览器缓存, 392
- Web 容量工具 (WCAT), 383–384
- Web 数据交换 (WDDX), 312
- Web 服务描述语言 (WSDL) 文件, 320–321, 326
- Web 服务, 7
  - 消费/消耗, 322–328
  - 概述, 319–322
  - 基于 REST 的, 332–343
- `Webgrind` 文件, 385
- `where()` 方法, 119
- 必需字段的通配符, 403
- `WinCacheGrind` 工具, 385
- `WordCount` 过滤器, 211
- `WordCount` 验证器, 78
- `_write()` 方法
  - `Square_Log_Writer_Doctrine`, 264–265
  - `Zend_Log_Writer_Abstract`, 259, 264
  - `Zend_Log_Writer_Doctrine`, 265
- 写入
  - 配置文件, 224–227
  - 日志消息, 254–259
- WSDL (Web 服务描述语言) 文件, 320–321, 326

## X

- `XCache` 缓存后端, 396
- `xdebug` 分析器, 384–385
- `xdebug.profiler_output_dir` 变量, 385
- `xdebug.trace_output_dir` 变量, 385
- XML
  - 配置文件, 225–227
  - 上文, 194
  - 日志数据, 261–263
  - 视图, 194–396
- XPath 查询, 327

## Y

- Yahoo 服务, 7
- Yahoo 库 (YUI), 372
- Flickr 服务, 7
- YUI 日历组件, 372–378
- `youtubeAction()` 方法, 324

## Z

- `Zend_Application_Bootstrap` 类, 238
- `Zend_Auth` 类, 3, 159–162, 168, 170
- `Zend_Auth_Adapter_Db` 类, 162–163
- `Zend_Auth_Adapter_Interface` 类, 160, 162
- `Zend_Auth_Result` 类, 160, 164
- `Zend_Auth_Storage_Interface` 类, 159
- `Zend_Cache` 类, 3, 392–395, 399
- `Zend_Cache_Manager` 类, 398–399, 405
- `Zend_Config` 类, 222, 225, 349–350
- `Zend_Config_Writer` 类, 224, 233
- `Zend_Config_Writer_Array` 类, 227
- `Zend_Config_Writer_Xml` 类, 225
- `Zend_Config_Xml` 类, 223
- `Zend_Controller_Action` 类, 24, 333
- `Zend_Controller_Request_Http` 类, 254
- `Zend_Currency` 类, 5, 282–285
- `Zend_Date` 类, 5, 275, 279, 282
- `Zend_Db_Adapter` 类, 73, 81
- `Zend_Db_Abstract` 类, 160
- `Zend_Db` 类, 57, 58–95
- `Zend_Db_Profiler` 类, 387, 388
- `Zend_Db_Firebug` 类, 389
- `Zend_Db_Query` 类, 388
- `Zend_Db_Table` 类, 107
- `Zend_Debug` 类, 254
- `Zend_Feed` 类, 312, 316, 318, 329, 337
- `Zend_Filter` 类, 70, 79
- `Zend_Filter_Input` 类, 124
- `Zend_Form` 类
  - 装饰器, 95, 177
  - 上传的文件, 210
  - 表单创建与验证, 51–53
  - 输入表单, 83
  - 本地化, 275, 294, 299
  - 更新, 150, 155–156
- `Zend_Form_Decorator_Abstract` 类, 98
- `Zend_Form_Element_` 类列表, 56
- `Zend_Form_Element` 类, 365
- `Zend_Form_Element_Button` 类, 62
- `Zend_Form_Element_Captcha` 类, 63–64, 84
- `Zend_Form_Element_Checkbox` 类, 57–58
- `Zend_Form_Element_File` 类, 60–61, 214, 216
- `Zend_Form_Element_Hash` 类, 63
- `Zend_Form_Element_Image` 类, 62
- `Zend_Form_Element_Checkbox` 类, 58
- `Zend_Form_Element_MultiSelect` 类, 59
- `Zend_Form_Element_Password` 类, 55
- `Zend_Form_Element_Reset` 类, 61
- `Zend_Form_Element_Select` 类, 59
- `Zend_Form_Element_Submit` 类, 61
- `Zend_Form_Element_Text` 类, 55
- `Zend_Form_Element_Textarea` 类, 55
- `Zend_Exception` 类, 246
- `Zend_Feed` 类, 312, 316, 318, 329, 337
- `Zend_Filter` 类, 70, 79
- `Zend_Filter_Input` 类, 124
- `Zend_Controller` 类, 24
- `Zend_Controller_Action` 类, 24, 333
- `Zend_Controller_Request_Http` 类, 254
- `Zend_Currency` 类, 5, 282–285
- `Zend_Date` 类, 5, 275, 279, 282
- `Zend_Db_Adapter` 类, 73, 81
- `Zend_Db_Abstract` 类, 160
- `Zend_Db` 类, 57, 58–95
- `Zend_Db_Profiler` 类, 387, 388
- `Zend_Db_Firebug` 类, 389
- `Zend_Db_Query` 类, 388
- `Zend_Db_Table` 类, 107
- `Zend_Debug` 类, 254
- `Zend_Log` 类, 259, 264
- `Zend_Log_Writer_Abstract` 类, 259, 264
- `Zend_Log_Writer_Doctrine` 类, 265
- `Zend_Model` 类, 116, 406–407
- `Zend_View` 类, 293–294
- `Zend_View_Helper` 类, 293–294
- `Zend_View_Renderer` 类, 358
- `Zend_View`
  - 应用, 41–42
  - 配置文件, 231–233
  - CRUD 操作, 136–139, 146–148
  - 表单, 86–88
  - 全文搜索, 186–187, 189–191
  - 登录, 165–166
  - 模型, 124–127
  - MVC 模式, 22–23
  - 命名规范, 34
  - 新闻馈送, 328–331
  - 分页, 201–204
  - 搜索, 177–179
  - XML, 194–196
  - 虚拟主机, 13–14
- 异常的可见性, 251
