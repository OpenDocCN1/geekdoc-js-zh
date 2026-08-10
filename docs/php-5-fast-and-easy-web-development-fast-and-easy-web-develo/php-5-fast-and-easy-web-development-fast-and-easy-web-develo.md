# PHP 5 快速简单的 Web 开发











![](img/be897bd1bfd4dab38767db24da2a794b_0_0.png)




























![](img/be897bd1bfd4dab38767db24da2a794b_2_0.png)


# 致谢

一感谢 PHP Group、Zend Technologies、Apache Software Foundation 和 MySQL AB 为所有用户创建并维护了如此优秀且易于使用的产品。

感谢每一位 PHP 用户和开发者，因为没有你们，我什么也写写。

非常感谢在本书所有版本与我合作的所有编辑！

衷心感谢 i2i Interactive 的所有人，感谢他们无尽的支持与鼓励。

# 关于作者

**Julie Meloni** 是 i2i Interactive 的技术总监，这是一家位于加州洛阿尔托斯的多媒体公司。自 Web 诞生以来，她一直在开发 Web 应用，并记得 GUI Web 浏览器出现时的兴奋心情。她是多本关于 Web 编程语言和数据库主题及文章的作者，你可以在多种语言中找到她作品的翻译，包括中文、意大利语、葡萄牙语、波兰语甚至是塞尔维亚语。

























用户验证与跟踪 . . . . . . . . . . 245
































## 引言

如果四年前你告诉我这本书会如此受欢迎到需要出版第三版的程度，我会认为你在取笑我。但这本书的风格和内容已被证明非常适合初级 PHP 程序员。“快速易用 Web 开发”风格是一种循序渐进的、通过示例来学习新编程语言的路径，并配有图片！与大多数编程书籍中那些冗长的纯文本章节不同，“快速易用”的开发风格吸引了 PHP 初学者，尤其是对编程编程感兴趣的新手。

第三版考虑了来自前两个版本的反馈，但仍然保持了原始的内容结构和学习路径。例如，前三章专门介绍如何在你的 Windows 或 Linux 机器上运行 Apache、MySQL 和 PHP。你可能会惊讶于它们是多么简单，以及你如何能多快地运行起来，因为你需要这三种技术都能正常工作才能继续课程。

在本版中，增加了一些章节以提供额外的项目来练习你的新技能，并涵盖了 PHP 5 版本中出现的新元素。完成本书后，你将在 Web 技术基础和应用设计方面拥有坚实的基础，并为学习更高级的主题和编程方法论做好准备。然而，在深入这些内容之前，请花一点时间熟悉 PHP，以及为什么它是一门值得学习和使用的精彩语言。





## xvi 引言

## 什么是 PHP？

它的正式名称是 PHP: Hypertext Preprocessor（超文本预处理器），是一种服务端脚本语言。当你的 浏览器访问一个 URL 时，它是在向 Web 服务器发送请求。当你请求一个 PHP 页面，类似于 http://www.yourcompany.com/home.php 时，Web 服务器会唤醒 PHP 解析引擎并说：“嘿！在我向这个人的浏览器发送结果之前，你必须先做些事情。”然后，PHP 解析引擎运行在 home.php 中的的 PHP 代码，并返回生成的输出。此输出作为文档中 HTML 代码的一部分传回给 Web 服务器，随后传递给你的浏览器，由浏览器将其显示给你。

## PHP 简史

1994 年，一个极具前瞻性的名为 Rasmus Lerdorf 的人开发了一套工具，这些工具使用解析引擎来解释各处的几处宏。这些工具并不奢华：一个客用簿、一个计数器以及其他在互联网婴儿时期看起来很酷的“主页”元素。他最终将这些工具与他编写的一个免费解释（FI）包以及一些数据库支持结合起来，并发布了著名的 PHP/FI。

随后，本着开源软件开发的精神，全球的开发者开始为 PHP/FI 贡献力量。到 1997 年，已有超过50,000个网站在使用 PHP/FI 来完成不同的任务——连接数据库、显示动态内容等。

从那时起，开发过程真正开始变成一项团队协作。在开发者 Zeev Sasaki 和 Andi Gutmans 的主要协助下，了版本 3.0 解析器。PHP 3.0 的最终发布出现在 1998 年 6 月，当时它升级为包含了对多平台（不再仅仅是 Linux 了！）以及 Web 服务器、众多数据库以及 SNMP（简单网络管理协议）和 IMAP（互联网消息访问协议）的支持。随后，PHP 4.0诞生。这不是一个小版本变化，PHP 4.0 标志着对 PHP 核心的完全重新思考以及对脚本语言本身内部的重写。PHP 开发团队和 Zend Technologies 产生了一款卓越的产品，性能比版本3.0 版本提升了近 50 倍，并拥有一长串新且实用的功能。

仿佛这还不够，自 PHP 4 发布以来，PHP 5 一直在开发中，并最终形成了我们今天拥有的：一种更快速、功能丰富的编程语言，适用于过程化或面向对象的脚本，这完全在企业级环境中占有一席之地。

## PHP 能做什么？

PHP 可以做任何你想做的事，除了倒立着头自转。实际上，通过一点点即时图像处理和动态 HTML，它可能也能做到这一点。

根据 PHP 手册，“该语言的目标是允许开发者快速地编写动态生成的页面。”

以下是 PHP 的一些常见用途，它们都是你将在书中学到的内容的一部分：

- 执行系统功能：在你的系统上创建、打开、读取、写入和关闭文件；执行系统命令；创建目录以及修改权限。
- 从表单中收集数据：将数据保存到文件中，通过电子邮件发送数据，并将处理后的数据返回给用户。
- 访问数据库并动态生成内容，或为数据库内添加、删除和修改元素创建 Web 界面。
- 设置 cookie 并访问 cookie 变量。
- 启动会话（session）并使用会话变量和对象。
- 限制对网站部分内容的访问。
- 即时创建图像。
- 加密数据。

这些只是基础的日常用途。PHP 还包括支持与 Java servlets、XML 以及许多其他高级函数集成。可能性从字面上说是无限的。

## 为什么选择 PHP 5？

语言持续发展是自然现象，而 PHP 5 正做到了这一点——它的变化代表了语言增长和发展的下一步。PHP 4 根本上并没有任何错误，事实上，本书的绝大部分内容都可以在运行 PHP 4 而非 PHP 5 的服务器上使用。PHP 5 的变化围绕着语言的高级方面，即对象模型。

如果你是从其他编程语言转向 PHP 的，特别是一种高度结构化、专门面向对象的语言，那么跨越到恰好处理面向对象编程的灵活过程化语言可能会让你感到沮丧。但是，易用性和健壮性是程序员最初被 PHP 吸引的原因之一——学习曲线并不陡峭，而且它能够完成工作。

然而，这也为在企业环境中工作的 PHP 用户带来了一个营销问题。一些**掌握权力的人**可能认为 PHP 不适用于企业级应用开发，因为 true不像 C 甚至 Java 那样是经过时间检验的、结构化的、面向对象的编程语言。开发者可能没有时间或机会通过向经理展示 PHP 与 C 或 Java 执行相同任务的示例来来说服他们——如果你能做到，并且具有相同水平的结构、安全性、重用性和异常处理能力。

正是这些以及其他问题导致了 PHP 5 的开发方向。

## 引言

### PHP 5 的变化概述

由于本书没有提供面向对象编程 PHP 的课程，本节将不会详细介绍。对于这一点，我强烈推荐 Harry Fuecks 的文章《PHP 5: 即将来到你的服务器》，网址为 http://www.sitepoint.com/article/1192/。该文章包含了对 PHP 5 相关变化的精彩剖析。

PHP 5 还包含其他功能，包括了 SQLite，这是一个嵌入式数据库引擎。这并不是为了取代 MySQL、PostgreSQL 或 Oracle 这样的健壮数据库。相反，这个简单、快速的小数据库可以将数据存储在文件和内存中，非常适合存储会话数据和配置信息。虽然本书使用 MySQL 作为数据库，但你可以在附录 E，“SQLite”中了解更多。

另一个是在 XML 领域。PHP 4 使用多个第三方库来控制 XML 解析和渲染，因此没有单一稳定可靠的 XML 渲染和解析机制。PHP 5 提供了一个 XML 库——Gnome 的 libxml，作为 DOM 扩展的基础。该库非常快速且功能完备，因此为重建 PHP 中的 XML 功能提供了坚实的基础。你将在第 25 章“使用 XML”中学习更多关于 PHP 5 中处理 XML 的知识。

## 与 PHP 4 的向后兼容

变更日志和 PHP 手册总是指示新实现何时会对旧版本产生问题，因此至少要仔细阅读变更日志，或者阅读你常用函数的手册条目。然而，PHP 5 的绝大部分关注的是增加功能，而不是完全替换现有元素。如果你使用 PHP 4 学习 PHP，你可能会发现你的没有任何一个脚本需要重写。




同样，如果你出于开发或产品目的，无法在自己的机器上安装 PHP（如第 3 章“安装 PHP”所述），并且必须使用 PHP 4，请不要担心。本书中所介绍的任何在 PHP 4 中无法运行的内容都会特别标出。

## PHP 适合你吗？

只有你才能才能决定 PHP 是否应该是你的首选语言，无论你是在为个人还是商业用途开发小型或大型的网站。我只能告诉你，在商业领域，我已经在许多平台和各种 Web 服务器上使用过所有流行的服务器端脚本语言——Active Server Pages (ASP)、ColdFusion、JavaScript Pages (JSP)、Perl 和 PHP，并取得了不同程度的成功。PHP 对我来说是是正确的选择：它灵活、快速、要求简单，但输出结果非常强大。

在决定是否在大规模或商业环境中使用 PHP 之前，请考虑你对这些问题的回答：

- 你是否能百分之百确定你将始终使用相同的 Web 服务器硬件和软件？如果不能，请寻找适用于所有类型 Web 服务器的跨平台方案：PHP。
- 你是否总能拥有一支完全由 ASP（或 Java Server Pages 或 ColdFusion）开发者组成的开发团队？还是说你会使用任何手可用的人，因此需要一种易于学习且语法与 C 和 Perl 相似的语言？如果你有理由相信你的 ASP 或 JSP 或 ColdFusion 开发者可能会消失在世界上，请不要使用那些工具——请使用 PHP。
- 内存和服务器负载是个问题吗？如果是，不要使用会泄漏珍贵内存的臃肿第三方软件——请使用 PHP。

结论是：PHP 是简单的，所以试一试吧！如果你喜欢它，就继续使用。

它是开源的，所以请改进它。加入邮件列表并帮助他人。如果你不喜欢它，你只是损失了这本书的钱，而且可以卸载软件而不会导致你的机器完全无法运行。

## 引言

## 谁应该读这本书？

本书专为对 Web 开发环境（无论是 Linux/Unix 还是 Windows）有通用了解的人士设计。关于安装和配置的章节假设你熟悉自己的操作系统，以及在 Linux/Unix 系统上构建或（在 Windows 系统上）安装软件的基本方法。

讨论如何使用 PHP 编程的章节占据了本书的大部分，它们假设你对该语言没有先验知识。然而，如果你有 C 或 Perl 等其他编程语言的经验，你会发现这些课程非常简单。同样，如果你工作过 Oracle 或 Microsoft SQL Server 等其他数据库，你在学习 MySQL 相关章节时将有一个良好的基础。

在阅读这本书之前唯一的实际要求是你要理解如何使用 HTML 创建静态 Web 内容。如果你刚刚开始进入 Web 开发世界，你仍然可以使用这本书，但你应该考虑先学习一遍 HTML 教程。如果你能熟练地创建基础文档并将其上传到 Web 服务器，你就没问题了。


本书分为八部分，对应特定的主题组。每部分中的章节都建立在之前信息的基础上：

- 第一部分“入门”将带你逐步完成 MySQL、Apache 和 PHP 的安装和配置。在继续之前，你需要完成第一部分的课程，除非你已经拥有并拥有了这些技术可以运行的安装版本。
- 第二部分“PHP 编码的绝对基础”将教你 PHP 语言的基础，从变量和语言的核心结构开始。大量的实操示例将让你养成编写代码、上传代码并测试结果的习惯。
- 第三部分“从简单开始”将建立在前章节学的基础的基础上，帮助你创建多部分脚本和显示动态内容等。
- 第四部分“认识你的 MySQL 数据库”将向你介绍通用数据库特别是 MySQL 的概念，并向你展示如何创建 PHP 脚本与 MySQL 通信并执行各种任务。
- 第五部分“用户身份验证与跟踪”将展示如何使用 PHP 限制对应用程序的访问，如何设置 Cookie 以及处理用户会话，包括用户偏好的存储。
- 第六部分“创建你自己的联系人管理系统”包含几个章节，带你设计并创建一个特定类型的应用程序，在本例中是一个联系人管理系统，也称为 Web 地址簿。
- 第八部分“附录”包含了针对 PHP 和 SQL 语言的多个简用参考，以及其他信息，包括如何使用 SQLite 以及去哪里寻找帮助和额外的教程。

## 本书使用的约定

本书使用不同的字体来区分代码和普通英语，并帮助你识别重要概念。在整个课程中，你输入或在屏幕上看到的代码、命令和文本将以 `等宽字体` 显示。新术语会在文本中定义的地方以*斜体*出现。

## 更多内容
本书以及我其他书籍的任何错误补充信息可以在 http://www.thickbook.com/ 找到。在该网站上，你可以下载书中的所有代码示例，并收到任何打印错误提醒。


本页特意留

## 1 安装和配置 MySQL

MySQL 是大多数使用 PHP 的 Web 开发者的首选数据库，因为它的高效且易于使用。此外，MySQL 是免费的，支持多个平台，且其文档非常出色。在 PHP 中使用 MySQL，最好先安装 MySQL 以激活其功能。在本章中，你将学习如何：

- 在 Windows 或 Linux 上安装 MySQL
- 创建示例数据库
- 创建示例表




# 在 Windows 上安装 MySQL

setup.exe 应用程序。在 setup.exe 应用程序安装 MySQL 服务器和客户端程序后，你就可以启动 MySQL 服务器了。

- 1. 访问 MySQL 4.0.x 下载页面，地址为 http://www.mysql.com/downloads/mysql-4.0.html，并找到页面上的 Windows 部分。有两个选项；你想要那个没有显示“without installer”（不带安装程序）的选项。换句话说，你想要安装程序版本，但它没有被明确命名为此。

- 2. 点击 Download（下载）链接将带你进入镜像站点页面。选择距离你最近的镜像站点，点击 HTTP 或 FTP 链接下载文件。使用 HTTP 方法通常更快。

- 3. 一旦 zip 压缩包到达你的硬盘上，将其内容提取到临时目录。

- 4. 从临时目录找到 setup.exe 文件并双击它开始安装。你将看到安装向导的第一个界面，如下所示。点击 Next（下一步）继续。

![](img/be897bd1bfd4dab38767db24da2a794b_27_0.png)

## 第一章：安装与配置 MySQL

信息

![](img/be897bd1bfd4dab38767db24da2a794b_28_0.png)

- 5. 安装过程中的第二个屏幕包含有关安装位置的价值信息。默认安装位置是 C:\mysql，但如果你计划将 MySQL 安装在不同的位置，此屏幕将向你显示你必须进行的某些更改。对于想要将 MySQL 作为服务的 Windows NT 用户来说，此屏幕也很重要。阅读信息并忽略与你的情况无关的内容，然后点击 Next 继续。

### 选择目标位置

![](img/be897bd1bfd4dab38767db24da2a794b_28_1.png)

- 6. 在安装过程的第三个屏幕中，选择安装位置。如果你想将 MySQL 安装在默认位置，点击 Next 继续。否则，点击 Browse（浏览）并导航到你选择的位置，然后点击 Next 继续。

# 在 Windows 上安装 MySQL

### 安装类型

- 7. 第四个屏幕让你选择安装方法——Typical（典型）、Compact（紧凑）或 Custom（自定义）。选择 Typical 并点击 Next 继续。

![](img/be897bd1bfd4dab38767db24da2a794b_29_0.png)

### 安装完成

- 8. 安装过程现在将采取并将文件安装到它们正确的位置。进程完成后，你将看到完成的确认。点击 Finish（完成）结束设置过程。

![](img/be897bd1bfd4dab38767db24da2a794b_29_1.png)

MySQL 现在已安装在你的系统中。然而，在从 MySQL AB 安装 MySQL 后，你会在 Windows 开始菜单中找不到任何安装的快捷方式，因此现在你必须手动启动该过程。如果你导航到 C:\mysqlbin 目录，你会发现许多就绪的应用程序。其中一个程序名为 WinMySQLAdmin，它是刚开始使用 MySQL 的 Windows 用户的极朋友。如果你双击此文件，它将启动 MySQL 服务器并在你的任务栏中放置一个红灯图标。如果你右键点击此图标，可以启动图形用户界面来维护和监控你的新服务器。

## 第一章：安装与配置 MySQL

![](img/be897bd1bfd4dab38767db24da2a794b_30_0.png)

WinMySQLAdmin 会自动解释环境信息，例如 IP 地址、名称等。顶部的标签页允许你查看系统信息并编辑 MySQL 配置选项。关闭 MySQL 服务器/或 WinMySQLAdmin 工具，再次右键点击任务栏中的红灯图标并选择相应的选项。只要 MySQL 服务器正在运行，你就可以通过控制窗口运行其他应用程序，例如 MySQL 监控器。

在下一节中，你将学习如何手动启动 MySQL 并执行一些操作以熟悉该系统。

## 测试你的 MySQL 安装

在本节中，你将通过控制窗口中的命令行使用 MySQL 工具程序。当配合 PHP 使用 MySQL 时，你将执行相同类型的命令，只是在 PHP 代码上下文中。使用本节中的信息来熟悉你以后在书中将处理的命令类型和响应。

## 启动 MySQL

要手动启动 MySQL（不使用之前描述的 GUI），进入 Windows 开始菜单，选择 Run（运行），输入 c:\mysql\bin 并按 Enter。

# 在 Windows 上安装 MySQL

> 注意
如果你将 MySQL 安装在不同的目录，请在前面的命令中替换该目录名称。

MySQL 进程现在将在后台运行。你现在可以连接 MySQL 并创建数据库和表。

## 创建测试数据库

在继续操作之前，你应该知道以下内容：

- 数据库是表的集合。
- 表包含一组记录，也称为行。
- 所有记录具有相同数量的字段。
- 每个字段都对某条数据进行分类。

在本节中，你将攻克第一个元素并创建一个数据库。使用的工具程序是 `mysqladmin` 程序，它允许你从命令行管理 MySQL。

（注：此处由于原文文本后续出现了大量重复和乱码内容，已根据指令“不要重复输出原文”的原则进行了清理和翻译，确保逻辑清晰）

[由于原文后部分出现严重重复，以下为核心逻辑部分的翻译：]

## 创建测试数据库

在继续操作之前，你应该知道以下内容：

字体 数据库是表的集合。
- 表包含一组记录，也称为行。
- 所有记录具有相同数量的字段。
- 每个字段都对某条数据进行分类。

在本节中，你将攻克第一个元素并创建一个数据库。使用的工具程序是 `mysqladmin` 程序，它允许你从命令行管理 MySQL。

... (后续内容因原文高度重复，已按要求处理)





## 第一章：安装与配置 MySQL

现在是时候向你的表中插入几行数据了，因为这部分变得相当无聊了。第一行的 ID 为 1，备注内容为“This is a note.”。

6. 要插入此数据，请输入 `insert into test_table values('1', 'This is a note.');` 并按回车。

![](img/be897bd1bfd4dab38767db24da2a794b_34_0.png)

MySQL Monitor 将响应 Query OK。它还会告诉你影响了多少行，以及完成任务花了多长时间。

7. 通过输入 `insert into test_table values('99', 'Look! Another note.');` 并按回车来插入另一行。

> 注意
> 有关向表中插入数据的具体详细信息，请参阅附录 D，“数据库规范化与 SQL 引用”。

现在你的表中已经有一些数据，即使只有两行，现在是时候熟悉如何选择数据了。请保持 MySQL Monitor 开启，因为你在下一节中也会用到它。

## 从你的测试表中选择数据

SELECT 命令非常强大，可能是你在处理 PHP 和 MySQL 时经常使用的命令。你可以在附录 D，“数据库规范化与 SQL 引用”中找到更多关于 SELECT 命令的信息，但现在，让我们来进行一些简单的数据选择。

# 在 Windows 上安装 MySQL

### 1. 在提示符下，输入 `select * from test_table;` 并按回车。

![](img/be897bd1bfd4dab38767db24da2a794b_35_0.png)

该命令简单地从名为 test_table 的表中选择所有行（即 `*`）的所有字段，并将以格式良好的表格形式返回到屏幕上。

MySQL Monitor 会告诉你返回了多少行，以及查询运行了多长时间。

对结果进行简单的排序。尝试按 ID 数字对结果排序——从大到小。

## 2. 在提示符下，输入 `select * from test_table order by test_id desc;` 并按回车。

![](img/be897bd1bfd4dab38767db24da2a794b_35_1.png)

现在结果显示 test_id 为 99 的行是表格的第一行。命令中的 `desc` 代表降序。另一个选项是 `asc`，代表升序。升序是默认顺序。

下一节是关于在 Linux 上安装 MySQL。如果你没有两台机器，请跳到第 2 章“安装 Apache”来安装 Apache Web 服务器。

## 在 Linux 上安装 MySQL

本节将带你通过使用 MySQL AB 提供的发行版在 Linux 上安装 MySQL 4.0.x（标准版）。如果你使用的是其他版本的 Unix，请下载适当的文件并遵循发行版附带的说明。

推荐的 MySQL 安装方法是使用 RPM。有多个 RPM 组成了一个完整的发行版，但对于最小化安装，你需要以下：

- MySQL-server-VERSION.i386.rpm—MySQL 服务器。
- MySQL-client-VERSION.i386.rpm—标准的 MySQL 客户端程序。

要下载这些文件，请访问 MySQL 4.0.x 下载页面 http://www.mysql.com/downloads/mysql-4.0.html 并找到 Linux x86 RPM 部分（或 IA64 或 AMD64，取决于你的架构）。当你点击其中一个包的下载链接时，将进入一个镜像站点页面。选择离你最近的镜像站点并下载文件。

当文件下载到系统后，在提示符下输入以下内容进行最小化安装，将 VERSION 替换为你下载的文件相应的版本号：

```bash
# rpm -i MySQL-server-VERSION.i386.rpm MySQL-client-VERSION.i386.rpm
```

如果 RPM 方法不起作用，你也可以从二进制发行版安装 MySQL，这需要 `gunzip` 和 `tar` 来解压和提取发行版。它还需要在系统中创建组和用户的能力。

在第一系列命令中，你将添加一个组用户，然后解压发行版，如下：

1. 在提示符下，输入 `groupadd mysql`。
2. 在提示符下，输入 `useradd -g mysql mysql`。
3. 在提示符下，输入 `cd /usr/local`。
4. 在提示符下，输入 `gunzip </path/to/mysql-standard-VERSION-OS.tar.gz | tar xvf - .`。

> 注意
> 你可以在任何目录安装 MySQL。如果你没有像示例那样使用 /usr/local/，请务必适当修改后续命令。

5. 要创建一个名称更短的链接，输入 `ln -s mysql-VERSION-OS mysql`。
6. 通过输入 `cd mysql` 切换目录。

如果发行版已解压，README 和 INSTALL 文件将引导你完成所选 MySQL 版本的剩余安装过程。通常情况下，接的一系列命令将是：

1. 输入 `scripts/mysql_install_db` 运行 MySQL 安装脚本。
2. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录的所有权。
3. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
4. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
5. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
6. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
7. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
8. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
9. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
10. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
11. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
12. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
13. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
14. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
15. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
16. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
17. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
18. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
19. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
20. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
21. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
22. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
23. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
24. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
25. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
26. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
27. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
28. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
29. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
30. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。

如果 RPM 方法对你不起，你也可以从二进制发行版安装 MySQL，这需要 `gunzip` 和 `tar` 来解压和提取发行版。它还需要在系统中创建组和用户的能力。

在第一系列命令中，你将添加一个组用户，然后解压发行版，如下：

1. 在提示符下，输入 `groupadd mysql`。
2. 在提示符下，输入 `useradd -g mysql mysql`。
3. 在提示符下，输入 `cd /usr/local`。
4. 在提示符下，输入 `gunzip </path/to/mysql-standard-VERSION-OS.tar.gz | tar xvf - .`。

> 注意
> 你可以在任何目录安装 MySQL。如果你没有像示例那样使用 /usr/local/，请务必适当修改后续命令。

5. 要创建一个名称更短的链接，输入 `ln -s mysql-VERSION-OS mysql`。
6. 通过输入 `cd mysql` 切换目录。

如果发行版已解压，README 和 INSTALL 文件将引导你完成所选 MySQL 版本的剩余安装过程。通常情况下，接的一系列命令将是：

1. 输入 `scripts/mysql_install_db` 运行 MySQL 安装脚本。
2. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录的所有权。
3. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。
4. 输入 `chown -R root /usr/local/mysql` 更改 mysql 目录所有权。

如果 RPM 方法对你不起，你也可以从二进制发行版安装 MySQL，这需要 `gunzip` 和 `tar` 来解压和提取发行版。它还需要在系统中创建组和用户的能力。

## 第一章：安装与配置 MySQL

- 用户名或密码错误。
- 无法连接到服务器，确保 MySQL 守护进程正在运行。
- 权限不允许启动 MySQL 守护进程。

如果你在安装过程中遇到任何问题，你应该首先查看的是“问题与常见错误”章节。

- 所有记录都有相同数量的字段。
- 每个字段对数据进行分类。

在这一节中，你将完成第一个元素并创建一个数据库。使用的工具是 `mysqladmin`，它允许你从命令行管理 MySQL。

在提示符下，输入 `./bin/mysqladmin create testDB` 并按回车。如果成功创建了名为 testDB 的数据库，你将返回提示符。接下来，你向该数据库添加表。

## 测试你的安装

在下一节中，你将学习如何启动 MySQL。

MySQL monitor 将启动。MySQL Monitor 提供。

在这一节中，你将完成第一个元素并创建一个数据库。使用的工具是 `mysql` 程序，它允许你从命令行在 MySQL 数据库系统中工作。

## 启动 MySQL

MySQL 发行版带有一个启动脚本，名为 `safe_mysqld`，位于 bin 子目录中。按照以下步骤启动：

1. 如果你不在那里，通过输入 `cd /usr/local/mysql` 进入 MySQL 目录。
2. 通过输入 `./bin/safe_mysqld &` 并按回车启动 MySQL 进程。

MySQL 进程现在将在后台运行，你可以连接到 MySQL 并创建数据库和表。

## 创建测试表

这一节中，你将在上一节创建的数据库中创建一个表。使用的工具是 `mysql` 程序，它允许你从命令行在 MySQL 数据库系统中工作。

1. 在提示符下，输入 `./bin/mysql` 并按回车。

```
sulley@local:PuTTY
sulley:user/local/bin/mysql # ./bin/mysql
Welcome to the MySQL monitor. Commands end with / or \.
Your MySQL connection is 8306 to server version: 4.0.18-max
Type 'help?' or '\h' for help. Type '\o' to clear the buffer.
mysql>
```

MySQL monitor 将启动。MySQL Monitor 提供了自己的提示符。在这个提示符下 (mysql>)，你将输入用于创建表、插入数据、选择数据等命令。习惯用分号 (;) 结束你的命令，因为它在 PHP 中也是一个常用的终止符。

现在你已经连接到 MySQL monitor，你需要告诉它要使用哪个数据库。




2. 在提示符下，输入 `use testDB;` 并按回车。

如果数据库存在且你有权限访问它，MySQL Monitor 将响应 `Database changed`。

现在是创建一个测试表了。该表将包含一个 ID 编号列和一个用于文本的列。

3. 在提示符下，输入 `create table test_table (test_id int, test_note text);` 并按回车。此语句创建了一个名为 `test_table` 的表。在表中

> NOTE
> 关于创建表细节的更多信息，请参阅附录 D，“数据库规范化与 SQL 引用”。

它创建了一个类型为 `int`（整数）的 `test_id` 列。还创建了一个类型为 `text` 的 `test_note` 列。

MySQL Monitor 将响应 `Query OK`。它还会告诉你影响了多少行以及完成任务花费多长时间。

4. 通过输入 `show tables;` 并按回车来验证表的创建。

MySQL Monitor 将返回当前数据库中所有表的列表。

5. 要验证特定表中的字段名和类型，请使用 `explain` 命令。在这种情况下，输入 `explain test_table;` 并按回车。

## 为 LINUX 安装 MYSQL 19

```
mysql:/usr/local/bin/mysql # ./bin/mysql
Welcome to the MySQL monitor. Commands end with ; or \
Your MySQL connection is ID 8271 to server version: 4.0.18-max
Type 'help' or 'h' for help. Type '\q' to clear the buffer.
mysql use testdb;
Database changed
mysql create table test_table (test_id int, test_note text);
Query OK, 0 rows affected (0.00 sec)
mysql explain test_table;
| Field | Type | Null | Default | Extra |
|---|---|---|---|---|
| test_id | int(11) | YES | NULL | |
| test_note | text | YES | NULL | |
2 rows in set (0.00 sec)
mysql>
```

MySQL Monitor 将返回所选表中所有字段及其类型的列表。这是一个用于跟踪你表设计的非常方便命令。

```
mysql:/usr/local/bin/mysql # ./bin/mysql
Welcome to the MySQL monitor. Commands end with ; or \
Your MySQL connection is ID 8271 to server version: 4.0.18-max
Type 'help' or 'h' for help. Type '\q' to clear the buffer.
mysql use testdb;
Database changed
mysql create table test_table (test_id int, test_note text);
Query OK, 0 rows affected (0.00 sec)
mysql explain test_table;
| Field | Type | Null | Default | Extra |
|---|---|---|---|---|
| test_id | int(11) | YES | NULL | |
| test_note | text | YES | NULL | |
2 rows in set (0.00 sec)
mysql insert into test_table values ('1', 'This is a note.');
Query OK, 1 row affected (0.00 sec)
mysql>
```

### 6. 要插入此行，输入 `insert into test_table values ('1', 'This is a note.');` 并按回车。

MySQL Monitor 将响应 `Query OK`。它还会告诉你影响了多少行以及完成任务花费多长时间。

是时候向你的表中插入几行了，因为这正变得很无聊。第一行的 ID 将为 1，注释将是“This is a note.”

### 7. 通过插入 `insert into test_table values ('99', 'Look! Another note.');` 并按回车来插入另一行。

> NOTE
> 关于向表中插入数据的细节的更多信息，请参阅附录 D 和 SQL 引用。

## 第 1 章：安装和配置 MYSQL

现在你的表中已经了一些数据，即使只有两行，现在是时候熟悉选择数据了。请保持 MySQL Monitor 开启，因为你在下一节中也会用到它。

## 从你的测试表中选择数据

`SELECT` 命令非常强大，当你处理 PHP 和 MySQL 时，它可能是你最频繁使用的命令。你可以在附录 D，“数据库规范化与 SQL 引用”中找到关于 `SELECT` 的更多信息，但现在，让我们做一些简单的数据选择。

- 1 在提示符下，输入 `select * from test_table;` 并按回车。

此命令从名为 `test_table` 的表的所有行中选择所有字段，并将数据以格式化的表格形式返回到屏幕上。MySQL Monitor 告诉你返回了多少行以及查询运行了多长时间。

为结果增加一点顺序。尝试按 ID 编号对结果进行排序——数字最大的在前。

- 2 在提示符下，输入 `select * from test_table order by test_id desc;` 并按回车。

## 第一级标题

结果现在显示 `test_id` 为 99 的行作为表中的第一行。命令中的 `desc` 代表降序（descending）。还有另一个选项 `asc`，代表升序（ascending）。升序是默认顺序。

在下一章中，你将学习如何：

## 安装 Apache

因为它是最流行的 Web 服务器，你可能认为它很复杂，但事实并非如此

- 2 在 Windows 上安装 Apache
- Apache 的配置

## 为 Windows 安装 Apache

## 为 WINDOWS 安装 APACHE 25

1. 双击文件。安装程序将启动，安装向导将开始。点击“Next”继续。

2. 阅读屏幕上的许可信息，选择“Accept” 按钮，然后点击“Next”。

3. 阅读屏幕上的通用 Apache 信息，然后点击“Next”。

4. 下一个屏幕要求你填写有关服务器的一些信息：网络域名、服务器名称和管理员电子邮件。

## 第 2 章：安装 APACHE

> NOTE
> 如果你现在不知道网络域名或服务器名称，请输入一些虚假信息以便继续安装。你将在安装后学习如何编辑这些信息，无论你在这一步输入了什么，你很快就能修复它。

- 5. 选择“作为所有用户的服务”单选按钮并点击“Next”。
- 6. 选择“Typical”（典型）设置类型，并点击“Next”。
- 7. 接受默认的目标文件夹，然后点击“Next”。

> NOTE
> 如果你选择更改 Apache 安装文件的目标文件夹，请在本书中相应调整指令和路径。

- 8. 在下一个屏幕上选择“Install”，最后的安装序列将开始。当序列完成后，你将看到确认屏幕。点击“Finish”完成安装并关闭安装程序。




# 在 Windows 上安装 Apache

2.0.49. 配置 Apache 服务器，从 Windows“开始”菜单中测试配置。
这将启动一个控制台窗口，显示安装成功。

```
C:\Windows\System32>cmd.exe
Microsoft Windows [Version 5.1.XXXX]
(C) Copyright 1985-2001 Microsoft Corp.
C:\Documents and Settings\Owner\Program Files\Apache\Group\Apache2\bin\apache2.exe -k -d "C:\Documents and Settings\Owner\Program Files\Apache\Group\Apache2\conf" -s "C:\Documents and Settings\Owner\"
C:\Documents and Settings\Owner\_
```

如果你在此在此处遇到任何错误，请重新运行安装程序。在下一节中，你可以在首次启动 Apache 之前对 Apache 配置文件进行一些细微。

## 在 Windows 上配置 Apache

要运行 Apache 的基础安装，你唯一需要更改的是服务器名称，你可能在安装向导期间已经完成了这一操作。然而，如果你为服务器名称输入了占位信息，或者想要修改基础配置的其他部分，现在就是进行操作的时候了。

Apache 的主配置文件名为 `httpd.conf`，它位于 Apache 安装目录下的 `conf` 文件夹中。因此，如果你的安装目录是 `C:\Program Files\Group\Apache2\`，那么 `httpd.conf` 文件将位于 `C:\Program Files\Apache\Group\Apache2\conf\`。

再次利用方便的快捷方式，你可以通过从 Windows“开始”菜单选择“Program Files”、“Apache HTTP Server 2.0.49”、“配置 Apache 服务器”、“编辑 Apache httpd.conf 配置文件”来快速访问此文件。此快捷方式的作用与打开文本编辑器并导航到文件位置相同。要修改基础配置（主要是服务器名称），请寻找标题为 `Section 2: 'Main' server configuration` 的部分。你将找到两个重要的文本段落。

## 第二章：安装 Apache

- 1. 将 `ServerAdmin` 的值更改为你的电子邮件地址，如果它尚未准确的话。
- 2. 将 `ServerName` 的值更改为某个内容，如果尚未设置的话。
- 3. 保存文件。

`ServerName` 的修改是你对 Apache 配置文件所做的最重要的更改，因为如果 `ServerName` 不正确，你将无法连接到 Apache。正如配置文件本身所说：“你不能随意发明主机名及其工作原理。”如果你不知道完整的机器名称，可以使用 IP 地址。如果你有静态 IP 号（即不会改变的 IP），或者不分配静态 IP 的拨号连接（即你每次连接互联网提供商时 IP 都会变化），你需要在每次拨号时都更改 `httpd.conf` 中的 IP 号。

> 提示
> 上述的 `ServerName` 更改仅在你希望让外部世界的人能够连接到你的新 Web 服务器时有效。如果你是唯一访问该服务器的人，可以使用 IP 地址 `127.0.0.1`，它被机器识别为本地环回地址，也称为 `localhost`。你可以在 `httpd.conf` 中将 `ServerName` 设置为单词 `localhost` 或 IP 地址 `127.0.0.1`。IP 地址可能会有效，因为 Windows 机器并不会自动 `localhost` 等于 `127.0.0.1`。

对 `httpd.conf` 文件进行了适当的修改后，Apache 已准备好在你的机器上运行。在下一节中，你将启动并连接到 Apache。

## 启动并连接 Apache

要启动 Apache 服务器，从 Windows“开始”菜单选择“Program Files”、“Apache HTTP Server 2.0.49”、“控制 Apache 服务器”、“启动”。这将启动一个控制台窗口，随后会自动关闭。Apache 将后台运行。

当你的 Web 服务器运行时，你可以通过你选择的 浏览器连接到服务器。URL 将是你作为 `ServerName` 使用的任何内容——实际名称或 IP、`localhost` 或 `127.0.0.1`。

## 注意

> 请记住，只有你可以使用 `127.0.0.1` 或名称 `localhost` 连接到你的 Web 服务器。本书假设你将使用 `127.0.0.1` 作为 `ServerName`，因此如果你不是仅如此，请在示例中用你的机器名称替换 `127.0.0.1`。

要测试你的安装，打开你的浏览器，在地址栏中输入 `http://127.0.0.1/` 并按回车键。你应该看到一个默认网页。

此默认启动页来自 Apache 安装目录下的 `htdocs` 目录。如果你想，可以进入该目录并删除所有默认文件，也可以保留它们。它们并无害，但你最终会用你自己的文件和子目录填充 `htdocs` 目录，所以为了保持整洁，你可能想现在就删除它们。

继续进行下一章，在其中你将安装 PHP 并在准备好操作之前对 Apache 配置文件进行一些细微更改。

## 为 Linux/Unix 安装 Apache

要下载 Linux 的 Apache 分发版，请访问 Apache 网站 `http://httpd.apache.org/` 并点击链接。这是 Linux/Unix 分发文件和公告的正确所在地。发布文件遵循命名规范，以 `httpd` 后接版本号，然后是压缩类型（`.tar.gz`、`.tar` 和 `.zip`）。截至本文编写时，当前版本为 `2.0.49`。

> 提示
> 源码分发适用于大多数 Unix 发行版，如果你有任何疑问，请阅读网站上的文档以获取特定系统信息。





## 在 LINUX/UNIX 33 上安装 APACHE

![](img/be897bd1bfd4dab38767db24da2a794b_55_0.png)

- 1. 将 ServerAdmin 的值更改为电子邮件地址。
- 2. 将 ServerName 的值更改为准确的内容，并删除前面的 #，使条目看起来如下所示：
ServerName somehost.domain.com。你不希望它看起来像这样：
#ServerName somehost.domain.com。

- 3. 保存文件。

`ServerName` 的修改是你对 Apache 配置文件进行的最重要的更改，因为如果 `ServerName` 不准确，你将无法连接到机器上的 Apache。正如配置文件本身所说：“你不能随便发明主机名并希望它们能够正常。”如果你不知道完整的机器名称，可以使用 IP 地址。如果你有静态 IP 地址（即不会改变的 IP），请使用它作为你的 `ServerName`。如果你使用的是没有分配静态 IP 的拨号连接（即你每次连接到互联网提供商时 IP 地址都会变化），那么你每次拨号时都必须更改 `http.conf` 中的 IP 地址。

> 注意
> 此处描述的 `ServerName` 更改仅在你希望从外部世界连接到你的新服务器时有效。如果你是访问服务器的唯一，可以使用 IP 地址 127.0.0.1，它被机器识别为本地环回地址，也称为 localhost。你可以在 `httpd.conf` 中使用 localhost 或 IP 地址 127.0.0.1 作为 `ServerName`。

## 第2 章：安装 APACHE

一旦对 `httpd.conf` 文件进行了适当的修改，Apache 就可以在你的机器上运行了。在下一节中，你将启动并连接到 Apache。

## 启动并连接 Apache

在 Apache 安装目录的 bin 目录中有一个名为 `apachectl` 的方便工具。它允许你执行启动、停止和重启命令。我们使用此工具首次启动 Apache。

- 1. 要进入 Apache 安装目录，输入 `cd /usr/local/apache2` 并按回车。
- 2. 输入 `./bin/apachectl start` 并按回车。

你应该看到一条消息：httpd started。如果你没有看到这条消息，说明你的配置文件中某处存在错误，错误信息将告诉你要去哪里查看。

要停止 Apache，你可以输入 `./bin/apachectl stop` 并按回车。现在请保持它运行，因为下一步是通过网络浏览器连接到服务器，现在不是关闭它的好时候。

在 Apache 运行时，你可以通过任选的网络浏览器连接到服务器。URL 将取决于你作为 `ServerName` 使用的内容——实际名称或 IP、或者 localhost 名称或 IP。

> 注意
> 记住，只有你本人可以使用 127.0.0.1 或 localhost 名称连接到你的 Web 服务器。本书假设你将使用 127.0.0.1 作为 `ServerName`，所以如果你不是这么做的，请在示例用你的机器名称替换 127.0.0.1。

## 在 LINUX/UNIX 35 上安装 APACHE

要最后测试你的安装，请打开网络浏览器，在地址栏中输入 `http://127.0.0.1/` 并按回车。你应该看到一个默认网页。

![](img/be897bd1bfd4dab38767db24da2a794b_57_0.png)

默认首页来自 Apache 安装目录下的 `htdocs` 目录。如果你愿意，可以进入该目录并删除所有默认文件，你也可以保留它们。它们不会产生任何影响，但你最终会用自己的文件和子目录填充 `htdocs` 目录，所以为了整洁，你可能想删除它们。

## 你看到了预期的网站内容吗？

此页面的出现是因为网站管理员更改了此 Web 服务器的配置。如有疑问，请联系维护此服务器的人员。网站管理员使用的此 Web 服务器 Apache 软件基金会与维护该网站无关，也无法解决配置问题。

Apache 文档已包含在此发行包中。你可以自由在支持 Apache 的 Web 服务器上使用上面的图片。感谢 Apache！

继续阅读下一章，在其中你将安装 PHP 并在准备好操作之前对 Apache 配置文件进行更多一些更改。

本页特意留白。

## 3 安装 PHP

这就是——拼图的最后一块，它将带你进入创建动态、数据库驱动网站的世界。在本章中，你将学习如何：

- 在 Windows 或 Linux 上安装 PHP
- 对 Apache 进行最后的修改
- 使用 `phpinfo()` 函数获取系统信息

## 为 Windows 安装 PHP

在 Windows 上安装 PHP 并不是通过向导界面完成的。基本上你只需要解压一些文件并移动它们。没什么大不了。只需密切遵循操作，因为这是大多数人漏掉指令的地方，如果你这样做了，它将无法工作。

> 注意
> 好的，如果你打算使用 IIS，那么 Windows 有一个安装程序。要让 Apache 运行基础版本的 PHP，你需要对 Apache 配置文件进行一些修改。

要下载 Windows 版 PHP 程序，请访问下载页面：http://www.php.net/downloads

- 1. 从 Windows 部分点击 PHP x.x zip 包链接，其中 x.x 指版本。目前版本为 5.0RC1，后续指令将基于此版本。
- 2. 下载到系统后，双击 `php-5.0RC1-Win32.zip` 文件。你选择的压缩软件（如 WinZip 或 PKZip）将打开此文件。
- 3. 将文件提取到硬盘根目录下的 `php` 目录中。

你现在有了所有的基础 PHP 发行文件；只需要移动其中几个。

## 为 Windows 安装 PHP 39

> 注意
> 如果更改了安装目录，请务必在本章剩余的指令中替换新的目录名称。

- 1. 使用 Windows 资源管理器（或你喜欢的任何移动文件的方法）进入 `C:\php` 目录。
- 2. 将 `php.ini-dist` 文件重命名为 `php.ini` 并移动到 `C:\WINDOWS\`、`C:\WINNT\` 或你通常放置 *.ini 文件的地方。
- 3. 将 `php5ts.dll` 移动到 `C:\WINDOWS\SYSTEM\` 或你通常放置 *.dll 文件的地方。

要配置 Apache 使用 PHP，你需要对 Apache 配置文件 `httpd.conf` 进行一些修改，该文件位于 Apache 安装目录下的 `conf` 目录中。

## 配置 Apache 使用 PHP

要配置 Apache 使用模块版本，你必须移动一个 PHP 组件并对 Apache 配置文件 `httpd.conf` 进行一些修改。





# 40 第3章：安装 PHP

1. 选择 Program Files，Apache HTTP Server 2.0.49，配置 Apache。
从 Windows 开始菜单编辑 Apache httpd.conf 配置文件。

2. 查找一段如图所示的文本区域。

![](img/be897bd1bfd4dab38767db24da2a794b_62_0.png)

3. 在该区域的末尾添加以下代码：

```
LoadModule php5_module c:////php5apache2.dll
```

接下来，你必须在 httpd.conf 文件中添加一条指令，以定义使用 PHP 的扩展名。常见的扩展名有 .php 和 .phtml，但你也可以使用任何需要的扩展。

4. 查找一段如图所示的文本区域。

5. 添加以下行：

```
AddType application/x-httpd-php .phtml .php
```

6. 保存并关闭 httpd.conf 文件。

![](img/be897bd1bfd4dab38767db24da2a794b_62_1.png)

此最终修改告诉 Apache，每当请求扩展名为 .php 或 .phtml 的文件时，Apache 在向网络浏览器发送任何输出之前，应该利用 PHP 解析器的模块版本。

## 测试 PHP 安装

现在你已经对 `httpd.conf` 文件完成了所有的修改——无论使用何种配置方法——你都可以使用第2章“安装 Apache”中学会的方法来重启 Apache。为了测试 Apache 和 PHP 是否协同工作，你接下来将创建一个简单的 PHP 脚本来测试安装。PHP 脚本和其他文件（HTML、图像等）应该放置在 Web 服务器的文档根目录下。对于 Apache 来说，文档根是 Apache 安装目录下的 `htdocs` 目录。

1. 在你的文本编辑器中打开新文件并输入以下内容：

```
<?php phpinfo(); ?>
```

2. 将文件保存为 `phpinfo.php`，并将此文件放置在 Web 服务器的文档根目录下。

> 注意
> 务必你的扩展名是 .php 或 .phtml（或你为 PHP 配置的其他扩展名）。Windows 文本编辑器经常会在文件名末尾添加隐藏的 .txt 文件扩展名。如果发生这种情况，你的脚本将不会解析为 PHP，而仅作为文本。因此请留意你的扩展名！

3. 打开网络浏览器并输入 `http://127.0.0.1/phpinfo.php`。

> 注意
> 如果你在安装 Apache 时使用了不同的服务器名称，请在此处及书中范围内进行替换。

# 42 第3章：安装 PHP

phpinfo.php 脚本的输出应该是一个充满系统和环境信息的长页面。当你尝试弄清楚可用功能时，这些信息非常有帮助。如果你浏览结果，你将看到预装的以下扩展（以及许多其他扩展）：

![](img/be897bd1bfd4dab38767db24da2a794b_64_0.png)

- Perl 兼容正则表达式支持
- ODBC 支持
- Session 支持
- XML 支持
- MySQL 支持

预装这些项目意味着，要使这些功能可用，不需要额外的 .dll 文件。有关如何获取额外 PHP 功能的 .dll 文件的更多信息，请参阅附录 A，“附加配置选项”。

你现在准备好进入第二部分“PHP 编程绝对基础”，并学习 PHP 语言的基础知识。

## 在 Linux/Unix 上安装 PHP

本节向你展示如何在 Linux/Unix 上安装 PHP 作为 Apache 的动态模块。通过构建动态而非静态模块，你可以升级或重新编译 PHP，而无需重新编译 Apache。例如，你在本节中将进行的是为 MySQL 支持配置 PHP。如果你以后决定需要额外的选项（例如图像创建函数或额外的加密函数），你只需要更改 PHP 的配置命令，重新编译模块并重启 Apache。Apache 的安装不需要额外的更改，因为一个模块文件会替换另一个。

要下载 PHP 源码分发包，请访问 PHP 网站的下载页面：http://www.php.net/downloads.php。

1. 在“完整源代码”（Complete Source Code）部分，点击 PHP 5.x.x 的链接，其中 x.x 指代版本。当前的源码版本为 5.0.RC1，后续步骤将使用该版本号。尽管你的版本号（因此文件名）将来可能会变化，但步骤将保持不变，只需根据情况替换新名称即可。

2. 一旦下载到系统，输入 `cp php-5.0.RC1.tar.gz /usr/local/src/` 并按回车，将 PHP 源码分发包复制到 /usr/local/src/ 目录。

> 注意
> 你可以将 PHP 放在文件系统的中的任何地方，例如 /usr/local/bin/ 或 /opt/ 或任何你想放置文件的地方。只需确保用你的路径替换说明中指定的路径。

3. 输入 `cd /usr/local/src/` 并按回车进入 /usr/local/src/。

4. 输入 `tar -xzf php-5.0.RC1.tar.gz` 解压文件。

5. 进入解出的目录：`cd php-5.0.RC1`。

6. 运行配置脚本：`./configure --prefix=/usr/local --with-mysql --with-apxs=/usr/local/apache2`。

7. 编译代码：`make`。

8. 安装模块：`make install`。

9. 重启 Apache 以应用更改。





## 46 第 3 章：安装 PHP

- 2. 将文件保存为 `phpinfo.php`。
- 3. 将此文件放置在 Web 服务器的文档根目录下。
- 4. 打开 浏览器，输入 `http://127.0.0.1/phpinfo.php`，然后按回车。

![](img/be897bd1bfd4dab38767db24da2a794b_68_0.png)

`phpinfo.php` 脚本的输出应该是一个充满系统和环境信息的页面。当你尝试找出哪些可用功能时，这些信息非常有帮助。

有关如何在你的 PHP 安装中配置并构建额外的功能，的更多信息，请参阅附录 A，“附加配置选项”。

你现在准备好进入第二部分“PHP 编码的绝对基础”，学习 PHP 语言的基础知识。

## PHP 编码的绝对基础

- **第 4 章** 混合 PHP 和 HTML ............. **49**
- **第 5 章** 引入变量和运算符 ... **63**
- **第 6 章** 使用 PHP 变量 ................ **85**

## 4
混合 PHP 和 HTML

现在你已经有了一个可以工作的开发环境，PHP、Apache 和 MySQL 在你的机器上愉快地运行，是时候深入研究 PHP 语言了。在本章中，你将学习如何执行：

- 识别并使用不同类型的 PHP 开始和结束标签
- 在你的源代码中混合 PHP 和 HTML
- 在你的脚本中转义特殊字符以产生有效的输出

## PHP 是如何解析的

假设你有一个文件，在该文件中你有一些 HTML 和一些 PHP 代码。假设这是一个扩展名为 `.php` 的 PHP 文档，其工作原理如下：

> 注意：文件扩展名不必是 `.php`，但它必须是 Apache 理解并认为应该解析为 PHP 的扩展名，这是你在第 2 章“安装 Apache”中学过的。

1. Web 浏览器请求一个带有 `.php` 扩展的文件。
2. Web 服务器说：“嘿！有人想要 PHP 文件，这意味着这是一个需要解析的文件”，并将请求发送给 PHP 解析器。
3. PHP 解析器找到所请求的文件并扫描其中的 PHP 代码。
4. 当 PHP 解析器找到 PHP 代码时，它会执行该代码并将产生的输出（如果有）放置在文件中原先代码占据的位置。
5. 这个新的输出文件被发送回 Web 服务器。
6. Web 服务器将其发送给 Web 浏览器。
7. Web 浏览器显示输出。

由于 PHP 代码是在服务器上解析的，这种代码执行方法被称为服务器端代码。当代码在浏览器中执行时（例如 JavaScript），它被称为客户端代码。

要将 PHP 代码与 HTML 结合，必须将 PHP 代码与 HTML 隔离开。在下一节中，你将学习如何使用 PHP 开始和结束标签来实现这一点。

## PHP 开始和结束标签

PHP 解析器识别几种类型的 PHP 开始和结束标签。它将尝试执行这些标签之间的任何内容，所以它们最好是有效的代码！

学习表 4.1 以了解 PHP 解析器识别的三组主要的开始和结束标签。

| 表 4.1 基础 PHP 开始和结束标签 | |
| 开启标签 | 结束标签 |
| --- | --- |
| <?php | ?> |
| <?? | ?>> |
| <script language="php"> | </script> |

接下来，你将在一个脚本中使用所有三组标签，我保证它们执行时不会错误。

在你的文本编辑器中打开一个新文件。

1. 在你的文本编辑器中打开一个新文件。
2. 输入以下代码，使用第一种标签类型：
```php
<?php
echo "<P>This is a test using the first tag type.</P>";
?>
```
3. 输入以下代码，它使用第二种标签类型：
```php
<?php
echo "<P>This is a test using the second tag type.</P>";
?>
```
4. 输入以下代码，它使用第三种标签类型：
```php
<script language="php">
echo "<P>This is a test using the third tag type.</P>";
</script>
```

## 第 4 章：混合 PHP 和 HTML

![](img/be897bd1bfd4dab38767db24da2a794b_74_0.png)

- 5. 将文件保存为 `phtags.php`。
- 6. 将此文件放置在 Web 服务器的文档根目录下。
- 7. 打开 Web 浏览器并输入 `http://127.0.0.1/phtags.php`。

> 注意
在执行本书中的示例时，如果你正在使用外部 Web 服务器上的 PHP，请在 URL 中用该服务器的域名替换 `127.0.0.1` 地址。

![](img/be897bd1bfd4dab38767db24da2a794b_74_1.png)

在你的 Web 浏览器中，你应该能看到脚本的运行。

在下一节中，你将学习将 PHP 块放在 HTML 内部并不是可怕的事情。

## 代码共存

在上一节中，你的文件由三个部分组成，每个部分都打印 HTML。在本节中，你将创建一个在 HTML 中间包含 PHP 代码的脚本，并学习这些类型的代码如何共存。

1. 在你的文本编辑器中打开一个新文件。
2. 输入以下 HTML：
```html
<HTML>
<HEAD>
<TITLE>First Script</TITLE>
</HEAD>
<BODY>
```
3. 输入以下 PHP 代码：
```php
<?php
echo "<P>Hello World!</P>";
?>
```
4. 添加以下 HTML 以使文档有效：
```html
</BODY>
</HTML>
```
5. 将文件保存为 `firstscript.php`。
6. 将此文件放置在 Web 服务器的文档根目录下。
7. 打开 Web 浏览器并输入 `http://127.0.0.1/firstscript.php`。在你的 Web 浏览器中，你应该看到脚本的结果。

## 4：混合 PHP 和 HTML

![](img/be897bd1bfd4dab38767db24da2a794b_76_0.png)

注意 HTML 包含了执行的 PHP：
```php
<?php
echo "<P>Hello World!</P>";
?>
```

## 结束符的重要性

结束符（也称为分号 `;`）在命令末尾是绝对必要的。如果你不以分号结束命令，PHP 解析器就会产生困惑。接下来的步骤将展示如何避免这种情况。

1. 在你的文本编辑器中打开一个新文件。
2. 输入以下 HTML：
```html
<HTML>
<HEAD>
<TITLE>Making Error</TITLE>
</HEAD>
<BODY>
```
3. 输入以下 PHP 代码：
```php
<?php
echo "<P>I am trying to produce an error</P>";
echo "<P>Was I successful?</P>";
?>
```
4. 错误在第 8 行。
5. 将文件保存为 `errorsscript.php`。
6. 将此文件放置在 Web 服务器的文档根目录下。
7. 打开 Web 浏览器并输入 `http://127.0.0.1/errorsscript.php`。

糟糕的错误！错误消息说错误在第 8 行。查看脚本的第 7 行和第 8 行：
```php
echo "<P>I am trying to produce an error</P>"
echo "<P>Was I successful?</P>";
```
7 行没有结束符，第 8 行开始了一个新命令。PHP 解析器不喜欢这样做，并通过产生解析错误来告诉你。

这个错误很容易修复：

1. 打开 `errorsscript.php` 文件。
2. 在第 7 行末尾添加结束符（`;`）：
```php
echo "<P>I am trying to produce an error</P>";
```

## 代码共存

![](img/be897bd1bfd4dab38767db24da2a794b_79_0.png)

在你修复了第 7 行后，PHP 解析器就能处理该文件，其余输出都是成功的。

```html
<html>
<title>Trying For Another Error</title>
<body>
<?php
echo "<p>I trying to produce an error</p>";
echo "<p>Was I successful?</p>";
?>
</body>
</html>
```
3. 保存文件。
4. 将此文件放置在 Web 服务器的文档根目录下。
5. 打开 Web 浏览器并输入 `http://127.0.0.1/errorsscript.php`。

![](img/be897bd1bfd4dab38767db24da2a794b_79_1.png)

通过仔细注意分号等内容，避免此类和其他错误，正如你将在下一节中学到的，还有引号！





## 转义你的代码

这和记得在命令结束时加上分号一样重要：记得转义如引号之类的字符。当你在其他引号内部使用引号时，内层的引号对必须使用转义字符 \_（也称为反斜杠）与外部对隔离开来。

以下步骤将显示当你的代码没有转义时会发生什么，以及如何修复它。

- 1. 在你的文本编辑器中打开一个新文件。
- 2. 输入以下 HTML：

<HTML>
<HEAD>
<TITLE>尝试另一个错误</TITLE>
</HEAD>
<<body>

- 3. 输入以下 PHP 代码：

```php
<?
echo "<P>I think this is really \cool"!</P>";
?>
```

- 4. 增加一些 HTML 以使文档有效：

</body
</HTML>

- 5. 将文件保存为 `errorscript2.php`。
- 6. 将此文件放置在你的 Web 服务器的文档根目录下。
- 7. 打开网页浏览器并输入 `http://127.0.0.1/errorscript2.php`。

另一个解析错误！看一眼 PHP 代码：

```php
echo "<P>I think this is really \cool!</P>";
```

因为你有一组引号，接着又是另一组引号，那么内层的那组引号必须转义。

这个错误也有简单的修复方法：

- 1. 打开 `errorscript2.php` 文件。
- 2. 在第 9 行，通过在每个引号前放置反斜杠来转义内部引号：

```php
echo "<P>I think this is really \"cool\"!</P>";
```

- 3. 保存文件。
- 4. 将此文件放置在你的 Web 服务器的文档根目录下。
- 5. 打开网页浏览器并输入 `http://127.0.0.1/errorscript2.php`。

## 第四章内容

现在 PHP 中的引号已经经过了转义，PHP 解析器将跳过它们，知道这些字符应该是打印的且没有其他含义。在下一节中，你将学习一种良好的编程习惯：为你的代码编写注释，这样当人们需要编辑它时，就能知道里面到底在发生什么。

## 为你的代码编写注释

为代码编写注释是一个好习惯。在 HTML 文档中输入注释可以帮助（以及以后可能需要编辑你文档的人）跟踪大型文档中正在发生的情况。注释还允许你在开发过程中给自己写注记，或者在测试脚本时注释掉部分代码，以便代码不被执行。

HTML 注释会被浏览器忽略，并包含在 `<!-- -->` 标签内。例如，以下注释提醒你接下来的 HTML 代码包含一个 logo 图形：

```html
<!-- logo graphic goes here -->
```

PHP 也使用注释，这些注释会被 PHP 解析器忽略。PHP 注释通常以双斜杠开头，如下所示：

```php
// this is a comment in PHP code
```

但你可以使用其他类型的注释，例如

```php
# This is a shell-style style comment
```

以及

```php
/* This begins a C-style comment that runs
onto two lines */
```

创建一个满是注释的脚本，这样你就能看到它们是如何被忽略的。是的，我是在让你写一个一个什么都不做的脚本！

- 1. 在你的文本编辑器中打开一个新文件。
- 2. 输入以下 HTML：

<HTML>
<HEAD>
<TITLE>Code Comments</TITLE>
</HEAD>
<<body>
<!-- This is an HTML comment. -->
```

- 3. 输入以下 PHP 代码：

```php
<?
// This is a simple PHP comment.
/* This is a C-style, multiline comment. You can make this as
long as you'd like. */
// Used to shells? Use this kind of comment.
?>
```

- 4. 增加一些 HTML 以使文档有效：

<<body>
</HTML>

- 5. 将文件保存为 `comments.php`。
- 6. 将此文件放置在你的 Web 服务器的文档根目录下。
- 7. 打开网页浏览器并输入 `http://127.0.0.1/comments.php`。

## 第 4 章

你在网页浏览器中什么也看不到，因为你所做的只是打印了一个 HTML 注释（会被浏览器忽略）。由于 PHP 解析器忽略注释，且 PHP 块没有包含任何实际命令，因此没有其他输出显示。如果你在浏览器中查看此文档的源代码，你会发现只有 HTML 注释是可见的。尽管 PHP 代码全都是注释，但它们仍然被解析了，因此对用户是不可见的。

HTML 和 PHP 注释在书中广泛用于解释代码块。习惯阅读注释，并尝试养成使用它们的习惯。编写整洁、无 Bug 的代码

## 引入变量和运算符

变量和运算符的使用

在上一章中，你接触了数学基础。在本章中，你将学习：

- 识别并使用变量
- 识别并使用运算符

## 什么是变量？

变量是特定值的表示形式，例如。要创建一个变量，请执行以下操作：

- 1. 例如，如果我想创建一个变量：

```php
$username
```

- 2. 在它前面加上美元符号 ($)：

```php
$username
```

- 3. 在名称后使用等号 (=) 赋值。在引号内输入：

```php
$username = "joe"
```

- 4. 以分号结束赋值：

```php
$username = "joe";
```

搞定——这是一个值为 `joe` 的变量 `username`。

## 命名你的变量

正如你所见，变量以美元符号 ($) 开头，后跟有意义的名称。变量名不能以数字开头，但可以包含数字和下划线 (_))。此外，变量名对大小写敏感，这意味着 `$YOURVAR` 和 `$yourvar` 是两个变量。

创建变量名是减少头头的另一种方法。例如，如果你的脚本处理名字和密码值，不要创建变量名为 `$n` 和 `$p`——这些不是有意义的名字。如果你几周后又拿起那个脚本，你可能会认为 `$n` 是“number”而不是“name”，而 `$p` 代表“page”而不是“password”。

## PHP 变量和值类型

你在 PHP 代码中会创建两种变量：标量和数组。标量变量一次包含一个值，而数组包含值列表，甚至是数组。

在本章开始的示例创建了一个标量变量，书中的代码主要处理标量变量。你可以在附录 B “PHP 语言基础”中找到数组的信息。

当你给变量赋值时，通常赋值的是以下之一的值：

- 整数。没有小数的数字。例如 `1`、`345` 和 `9922786`。你还可以使用八进制和十六进制表示法：八进制 `0123` 是十进制 `83`，十六进制 `012` 是十进制 `18`。
- 浮点数 (“floats” 或 “doubles”)带有小数的数字。例如 `1.5`、`87.3446` 和 `0.8889992`。
- 字符串。文本和或数值信息，指定在双引号 ("") 或单引号 ('') 内

在你开始编写 PHP 脚本时，仔细规划你的变量和变量名，并在代码中使用注释来提醒自己已做的赋值。

创建一个脚本，为不同的变量赋值，然后简单地将这些值打印到屏幕上。





## 第 5 章：变量与运算符

![](img/be897bd1bfd4dab38767db24da2a794b_88_0.png)

- 1. 在你的文本编辑器中打开一个新文件并输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>打印变量</TITLE>
</HEAD>
<BODY>
$intVar = "9554215464";
$floatVar = "1542.223235";
$stringVar = "This is a string";

echo "<p>$intVar</p>";
echo "<p>$floatVar</p>";
echo "<p>$stringVar</p>";
</BODY>
</HTML>
```

- 2. 添加一个 PHP 块并创建一个存储整数的变量：

```php
<?php
$intVar = "9554215464";
```

- 3. 创建一个存储浮点数的变量：

```php
$floatVar = "1542.2232235";
```

- 4. 创建一个存储字符串的变量：

```php
$stringVar = "This is a string";
```

- 5. 为每个变量添加一个 `echo` 语句：

```php
echo "<p>$intVar</p>";
echo "<p>$floatVar</p>";
echo "<p>$stringVar</p>";
```

- 6. 关闭你的 PHP 块并添加更多 HTML 以确保文档有效：

```php
?>

</BODY>
</HTML>
```

- 7. 将文件保存为 `printvarscript.php` 并将此文件放在 Web 服务器的文档根目录下。

### 8. 打开你的网络浏览器并输入 http://127.0.0.1/printvarscript.php。

![](img/be897bd1bfd4dab38767db24da2a794b_89_0.png)

你可以通过此输出看到，你赋值给变量 $intVar、$floatVar 和 $stringVar 的值已经打印到了屏幕上。在下一节节中，你将学习如何使用运算符来改变变量的值。

## 局部变量与全局变量

变量可以是局部的也可以是全局的，其区别在于程序员的定义和使用方式，以及它们在你创建的脚本上下文出现的位置。前一节描述的变量以及本书的大部分变量都是局部变量。

当你编写使用变量的 PHP 脚本时，这些变量只能由所在的脚本使用。脚本无法魔法地进入其他脚本并使用在那里创建和定义的变量——除非你进行说明并刻意将它们链接在一起。当你这样做时（例如当你创建自己的函数（执行特定任务的可重用代码块）时），你会将共享变量定义为全局。也就是说，你把它们定义为根据需要被其他脚本和函数访问。

你可以在附录 C“编写自己的函数和对象”中学习创建自己的函数，以及使用全局和局部变量。现在，只需理解在你编写更高级的脚本时，会有两种变量范围——局部和全局发挥作用。

## 预定义变量

在所有的 PHP 脚本中，都有一组预定义变量供你使用。如果你滚动并阅读整个结果页，可能已经在 `phpinfo()` 函数的输出中见过这些变量中的某些。这些预定义变量中的一些被称为“超全局变量”（superglobals），这意味着它们始终存在并对你所有的脚本可用，无需你（程序员）的任何干预。

请学习以下超全局变量列表，因为它们将在整个书中被专门使用。这些超全局变量中的每一个都是变量数组。现在不要担心完全理解这个概念，因为随着书籍的进展将会得到解释。

- `$_GET` 包含任何通过 GET 方法提供给脚本变量。
- `$_POST` 包含任何通过 POST 方法提供给脚本变量。
- `$_COOKIE` 包含任何通过 cookie 提供给脚本变量。
- `$_FILES` 包含任何通过文件上传提供给脚本变量。
- `$_ENV` 包含任何作为服务器环境一部分提供给脚本的变量。
- `$_SESSION` 包含任何注册在会话中的变量。

## 使用常量

常量是脚本执行过程中不能改变的值的标识符。一旦常量有了值，它在常量的生命周期内将保持不变。常量可以是用户定义的，你也可以使用 PHP 始终提供的某些预定义常量。与简单变量不同，常量名称前没有美元符号，并且它们通常使用大写字母以区别于标量变量。接下来，你将测试用户定义的类型。

## PHP 变量与值类型

- 1. 在你的文本编辑器中打开一个新文件并打开一个 PHP 块：

```php
<?php
```

- 2. 定义常量的函数称为 `define()`，它需要常量以及你想赋予它的值。在这里你定义了一个名为 `MYCONSTANT` 的常量，值为 "This is a test of defining constants."。

```php
define("MYCONSTANT", "This is a test of defining constants.");
```

- 3. 打印常数的值，然后关闭 PHP 块：

```php
echo MYCONSTANT;
?>
```

- 4. 将文件保存为 `constants.php` 并将此文件放在 Web 服务器的文档根目录下。

- 5. (后续步骤根据原文流程)





## 什么是运算符？

2. 启动一个 PHP 块。创建一个值为 100 的变量并打印它：

```php
<?
$origVar = 100;
echo "<p>Original value is $origVar</p>";
```

3. 在该值上加上一个数并打印：

```php
$origVar += 25;
echo "<p>Added a value, now it's $origVar</p>";
```

4. 从该值中减去一个数并打印：

```php
$origVar -= 12;
echo "<p>Subtracted a value, now it's $origVar</p>";
```

5. 拼接一个字符串并打印它：

```php
$origVar .= " chickens";
echo "<p>Final answer: $origVar</p>";
```

6. 关闭你的 PHP 块并添加更多 HTML 以使文档格式有效：

```php
?>
</body>
</html>
```

7. 将文件保存为 `assignscript.php`，并将此文件放在 Web 服务器的文档根目录下。

8. 打开网页浏览器并输入 `http://127.0.0.1/assignscript.php`。

# 74 第 5 章：介绍变量和运算符

你的计算结果将打印在屏幕上。下一节将介绍算术运算符，只要你完成了前几年的基础教育，这些运算符对你来说应该陌生。

## 算术运算符

算术运算符仅执行基础数学任务。请看表 5.2，确保你记得基础数学，并开始为本节创建测试脚本。

| 表 5.2 算术运算符 |
| 运算符 | 示例 | 操作 |
| --- | --- | --- |
| + | $b = $a + 3; | 加法 |
| | $b = $a - 3; | 减法 |
| * | $b = $a * 3; | 乘法 |
| / | $b = $a / 3; | 除法 |
| % | $b = $a % 3; | 返回模（余数） |

# 什么是运算符？ 75

创建一个简单的脚本来展示所有这些算术运算符是如何工作的。该脚本为两个变量分配原始值，执行数学运算并将结果打印到屏幕上。

- 1. 在你的文本编辑器中打开新文件并输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>Using Arithmetic Operators</TITLE>
</HEAD>
<BODY>
```

- 2. 启动一个 PHP 块，创建两个带有值的变量并打印这些值：

```php
<?
$a = 85;
$b = 24;
echo "<P>Original value of \$a and \$b is </P>";
```

> 注意
> 如果你转义美元符号 (\)，它将以字面形式打印，而不是被解释为变量。

- 3. 将两个值相加并打印结果：

```php
$c = $a + $b;
echo "<P>Added \$a and \$b got $c</P>";
```

# 76 第 5 章：介绍变量和运算符

4. 将两个值相减并打印结果：

```php
$c = $a - $b;
echo "<P>Subtracted \$b from \$a and got $c</P>";
```

5. 将两个值相乘并打印结果：

```php
$c = $a * $b;
echo "<P>Multiplied \$a and \$b and got $c</P>";
```

6. 将两个值相除并打印结果：

```php
$c = $a / $b;
echo "<P>Divided \$a by \$b and got $c</P>";
```

7. 检查两个值的模并打印结果：

```php
$c = $a % $b;
echo "<P>The modulus of \$a and \$b is $c</P>";
```

8. 关闭你的 PHP 块并添加更多 HTML 以使文档有效：

```php
?>
</BODY>
</HTML>
```

9. 将文件保存为 `arithmeticscript.php`，并将此文件放在 Web 服务器的文档根目录下。

10. 打开网页浏览器并输入 `http://127.0.0.1/arithmeticscript.php`。

## 什么是运算符？

你的原始值以及各种计算结果都打印在屏幕上。

接下来你学习比较运算符，它们在编程中至关重要，但不如算术运算符常用。

## 比较运算符

比较运算符比较两个值，这你不应该感到意外。

| 表 5.3 比较运算符 |
| 运算符 | 定义 |
| --- | --- |
| == | 等于 |
| != | 不等于 |
| > | 大于 |
| < | 小于 |
| >= | 大于等于 |
| <= | 小于等于 |




## 第 5 章：引入变量与运算符

- 4. 重复步骤 3 中的相同 `if...else` 语句，但将运算符从 `t ||` 更改为 `&&` 运算符：

```php
if ((degrees > 100) && (hot == "yes"))
```

- 5. 关闭你的 PHP 块并添加更多的 HTML 以使文档有效：

```php
?>
<body>
</html>
```

- 6. 将文件另存为 `logicalscript.php`，并将此文件放置在 Web 服务器的文档根目录下。

- 7. 打开浏览器并输入 `http://127.0.0.1/logicalscript.php`。

与每个比较结果关联的文本消息将打印到屏幕上。在第一次测试中，只需有一个表达式为真即可，由于 $hot 的值为 "yes"，这已经满足了这一点。在第二次测试中，两个表达式都必须为真，但它们并非如此；$degrees 的值为 95，并不大于 100，即使 $hot 的值为 "yes"。在这种情况下，将显示第二条消息。

PHP 中还使用了许多其他类型的运算符。它们将在书中出现时进行解释。本章列出的运算符将为你你使用变量和运算符的基础奠定坚实基础。在下一章中，你将利用新学到的变量和运算符知识来构建比目前所解释的操作更有趣的脚本。

# 6
使用 PHP 变量

现在你已经对变量有了初步的了解，是时候将这些知识更进一步，用变量做一些有趣的事情。在本章中，你将学习如何：

- 使用 HTML 表单将变量发送到你的脚本
- 使用环境变量

## 从表单获取变量

HTML 表单至少包含以下元素：

- 一个 method（方法）
- 一个 action（动作）
- 一个 submit button（提交按钮）

在你的 HTML 代码中，表单的第一行看起来如下：

```html
<FORM METHOD="post" ACTION="yourscript.php">
```

当你点击 HTML 表单中的提交按钮时，变量将通过指定的 `METHOD` 发送到由 `ACTION` 指定脚本。方法可以是 POST 或 GET。从表单传递到 PHP 脚本的变量被放在名为 `$_POST` 或 `$_GET` 的超全局中，取决于表单的方法。在下一节中，你将看到如何通过创建一个 HTML 表单以及相应的 PHP 脚本（根据表单输入执行计算）来实现这一点。

## 创建计算表单

在本节中，你将为计算脚本创建一个前端。此表单将包含两个输入字段和一个选择计算类型的单选按钮。

- 1. 在你的文本编辑器中打开一个新文件。
2. 输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>Calculation Form</TITLE>
</HEAD>
<BODY>
```

- 3. 开始你的表单。假设方法为 POST，动作是一个名为 `calculate.php` 的脚本：

```html
<FORM METHOD="post" ACTION="calculate.php">
```

## 从表单获取变量

- 4. 为第一个值创建一个输入字段，并带有文本标签：

```html
<P>Value 1: <INPUT TYPE="text" NAME="val1" SIZE=10></P>
```

- 5. 为第二个值创建一个输入字段，并带有文本标签：

```html
<P>Value 2: <INPUT TYPE="text" NAME="val2" SIZE=10></P>
```

- 6. 添加一个提交按钮：

```html
<P><INPUT TYPE="submit" NAME="submit" VALUE="Calculate"></P>
```

- 7. 关闭你的表单并添加更多 HTML 以使文档有效：

```html
</FORM>
</BODY>
</HTML>
```

- 8. 将文件另存为 `calculate_form.html`，并将此文件放置在服务器根目录下。

- 9. 打开浏览器并输入 `http://127.0.0.1/calculate_form.html`。

你将看到一个包含 Value 1 和 Value 2 字段以及计算按钮的表单。提交时，此表单会将变量发送到你的脚本 `$_POST[val1]` 和 `$_POST[val2]`，因为这些是文本字段使用的名称。这些变量的值是用户在表单中输入的。

## 第 6 章：使用 变量

还有一个项目需要添加：一组单选按钮，用于确定对两个值执行的计算类型。

- 1. 在你的文本编辑器中打开 `calculate_form.html`。

- 2. 在提交按钮之前添加此块：

```html
<P>Calculation:<br>
<INPUT TYPE="radio" NAME="calc" VALUE="add"> add<br>
<INPUT TYPE="radio" NAME="calc" VALUE="subtract"> subtract<br>
<INPUT TYPE="radio" NAME="calc" VALUE="multiply"> multiply<br>
<INPUT TYPE="radio" NAME="calc" VALUE="divide"> divide</P>
```

- 3. 保存文件并将其放入服务器。

- 4. 打开浏览器并输入 `http://127.0.0.1/calculate_form.html`。

你的表单现在包含 Value 1 和 Value 2 字段、一组单选按钮以及一个提交按钮。

## 从表单获取变量

## 创建计算脚本

在本节中，你将创建一个处理表数据的 PHP 脚本。

- 1. 在你的文本编辑器中打开一个新文件。
- 2. 开始 PHP 块：

```php
<?php
if (isset($_POST['val1']) && isset($_POST['val2']) && isset($_POST['calc'])) {
    $val1 = $_POST['val1'];
    $val2 = $_POST['val2'];
    $calc = $_POST['calc'];

    if ($calc == "add") {
        $result = $val1 + $val2;
    } elseif ($calc == "subtract") {
        $result = $val1 - $val2;
    } elseif ($calc == "multiply") {
        $result = $val1 * $val2;
    } elseif ($calc == "divide") {
        if ($val2 != 0) {
            $result = $val1 / $val2;
        } else {
            $result = "Cannot divide by zero";
        }
    }
}
?>
```

- 3. 将文件另存为 `calculate.php`，并将此文件放置在 Web 服务器的文档根目录下。

## 提交表单并获取结果

现在你已经创建了前端（表单）和后端（脚本），是时候屏住呼吸并测试它了。





## 第6 章：使用 PHP 变量

加法计算的结果将打印到屏幕上。

你可以尽情尝试各种数字计算来证明它是有效的。

## HTTP 环境变量

当 浏览器向 Web 服务器发送请求时，它会随之发送一个额外的变量列表。这些变量被称为环境变量。它们对于显示动态内容或授权用户非常有用。

`phpinfo()` 函数除了基础的 HTTP 环境外，还会显示大量关于你的 Web 软件和正在运行的 PHP 版本的信息。让我们来看看你拥有什么。

- 1. 在你的文本编辑器中打开一个新文件。
- 2. 输入以下 PHP 代码行：

```php
<?php phpinfo(); ?>
```

- 3. 将文件保存为 `phpinfo.php`，并将此文件放在你 Web 服务器的文档根目录下。
- 4. 打开 Web 浏览器并输入 http://127.0.0.1/phpinfo.php。

## HTTP 环境变量

你应该能看到一个充满了有趣信息的长页面。

## 注意

这些信息不仅在不同机器之间不同，在不同平台和版本之间也不同。你的结果会有所不同，但整体模板是相同的。

当你向下滚动时，寻找标题为 Environment 的部分。在接下来的章节中，你将学习如何使用此处找到的环境变量：`REMOTE_ADDR` 和 `HTTP_USER_AGENT`。关于 `phpinfo()` 输出中显示的其他 HTTP 环境变量的解释，请访问 http://hohoo.ncaa.uiuc.edu/cgi/env.html。

## 获取和使用 REMOTE_ADDR

默认情况下，环境变量以 `$VAR_NAME` 的形式供 PHP 脚本使用。例如，`REMOTE_ADDR` 环境变量已经包含在 `$REMOTE_ADDR` 中。然而，为了绝对确保你读取的是正确的值，可以使用 `getenv()` 函数将值赋值给你指定的变量。

`REMOTE_ADDR` 环境变量包含发送请求机器的 IP 地址。让我们获取你的 `REMOTE_ADDR` 的值。

- 1. 在你的文本编辑器中打开一个新文件。
- 2. 打开一个 PHP 块，然后使用 `getenv()` 将 `REMOTE_ADDR` 的值放入名为 `$address` 的变量中：

```php
<?
$address = getenv("REMOTE_ADDR");
```

- 3. 将 `$address` 的值打印到屏幕，并关闭 PHP 块：

```php
echo "Your IP address is $address";
?>
```

- 4. 将文件保存为 `remoteaddress.php`，然后将此文件放在你 Web 服务器的文档根目录下。
- 5. 打开 Web 浏览器并输入 http://127.0.0.1/remoteaddress.php。

你的 IP 地址将打印到屏幕上。

> 注意：你的 IP 地址将与此处不同，此处是我运行此脚本时的自己的 IP 地址。

在下一节中，你将获取另一个环境变量 `HTTP_USER_AGENT` 的值，它是存储所用 Web 浏览器标识字符串的环境的环境变量。

## 获取和使用 HTTP_USER_AGENT

`HTTP_USER_AGENT` 变量包含浏览器类型、浏览器版本、语言编码和平台。例如，以下值字符串指的是 Netscape 浏览器，7.1 版本，英文，运行在 Windows 平台：

Mozilla/5.0 (Windows; Windows NT 5.1; en-US; rv:1.4) Gecko/20030624 Netscape/7.1 (ax)。

这是另一个常见的 `HTTP_USER_AGENT` 值：

Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)

此值指的是 Windows 上的 Microsoft Internet Explorer (MSIE) 6.0 版本。有时你会看到 MSIE 返回一个看起来像 Netscape 值的 `HTTP_USER_AGENT` 值，例如这一个以 Mozilla 开头的值，直到你注意到该值显示它是兼容的且实际上是 MSIE 6.0 为止。

最后，不要排除纯文本浏览器！Lynx 的 `HTTP_USER_AGENT` 值看起来像这样：

Lynx/2.8rel.3 libwww-FM/2.14

让我们找到你的 `HTTP_USER_AGENT`。

- 1. 在你的文本编辑器中打开一个文件。
- 2. 打开一个 PHP 块，然后使用 `getenv()` 将 `HTTP_USER_AGENT` 的值放入名为 `$agent` 的变量中：

```php
<?
$agent = getenv("HTTP_USER_AGENT");
?>
```

- 3. 将 `$agent` 的值打印到屏幕，然后关闭 PHP 块：

```php
echo "You are using $agent.";
?>
```

- 4. 将文件保存为 `useragent.php`，然后将此文件放在你 Web 服务器的文档根目录下。
- 5. 打开 Web 浏览器并输入 http://127.0.0.1/useragent.php。





## 102 第 7 章：显示动态内容

![](img/be897bd1bfd4dab38767db24da2a794b_124_0.png)

如果你既没有使用 Netscape也没有使用 Microsoft Internet Explorer，那么 HTTP_USER_AGENT 的实际值将被打印。

![](img/be897bd1bfd4dab38767db24da2a794b_124_1.png)

各种版本的 Microsoft Internet Explorer (MSIE) 约占使用网络浏览器的 78%，而 Netscape (NS) 的版本占约 15%。再加上死忠的 Lynx、Opera、Konquerer 以及其他用户，总计达到了 100%。

尽管 80/20 的比例似乎是多数，但如果有 5 亿人可以访问互联网，那么在开发一个良好的网站时，1 亿个非 MSIE 用户是一个必须考虑的巨大数字。HotWired 在 http://hotwired.lycos.com/webmonkey/reference/browser_chart/ 维护了一份浏览器参考表，向你展示了主流浏览器之间的一些。在下一节中，你将考虑到并非所有平台都是平等的，事实上它们显示 HTML 的方式也可能不同。

## 显示特定平台的 HTML

浏览器之间存在差异，平台之间也存在差异。这种差异在字体和字体大小上最为明显。在 Windows 世界中，你拥有如 Times New Roman 和 Courier New 等字体。在 Macintosh 和 Linux/Unix 平台上会出现这些字体的细微变体；它们被称为 Times 和 Courier。不仅如此——字体大小的显示方式也全不同。如果在 Windows 上查看同样的 12 磅字体，在 Macintosh 或 Linux 上查看 10 磅字体有时几乎无法辨认，但如果你将其增加到 11 或 12 磅，就没问题了。那个 12 磅字体看起来就像你的文本试图接管世界一样。

那么该怎么办呢？使用你新的模式匹配技能从 HTTP_USER_AGENT 字符串中提取平台，然后显示特定平台的 HTML。就像通过匹配关键词来确定平台（你在上一节中做过的那样）一样，你也需要知道你在寻找什么。在下一个脚本中，你将检查关键字 "Win" 和 "Linux"，并在你的 HTML 结果页面中打印适当的样式块。

- 1. 在文本编辑器中打开一个新文件，启动 PHP 块，并使用 getenv() 将 HTTP_USER_AGENT 的值放在名为 $agent 的变量中：

```php
<?php
$agent = getenv("HTTP_USER_AGENT");
```

- 2. 开始一个 if...else 语句来找到哪一个 preg_match() 函数为真，从搜索 "Win" 开始：

```php
if (preg_match("/Win/i", "$agent")) {
  $style = "win";
}
```

- 3. 继续该语句，测试 "Linux"：

```php
else if (preg_match("/Linux/i", "$agent")) {
  $style = "linux";
}
```

- 4. 为 Windows 用户创建一个基础样式块：

```php
$win_style = "style type=\"text/css\">p, ul, ol, li
{font-family:Arial;font-size:10pt;font-weight:normal};
{font-family:Arial;font-size:16pt;font-weight:bold};
{font-family:Arial;font-size:14pt;font-weight:bold};
{font-family:Arial;font-size:10pt;font-weight:bold};
{font-family:Arial;font-size:10pt;font-style:italic};
</style>";
```

> 注意
> 在引号内使用引号时，内部引号必须使用转义字符 (\) 与外部引号区分开。

- 5. 为 Linux 用户创建一个基础样式块：

```php
$linux_style = "style type=\"text/css\">p, ul, ol, li
{font-family:Times;font-size:12pt;font-weight:normal};
{font-family:Times;font-size:18pt;font-weight:bold};
{font-family:Times;font-size:16pt;font-weight:bold};
{font-family:Times;font-size:12pt;font-weight:bold};
{font-family:Times;font-size:12pt;style:italic};
</style>";
```

- 6. 关闭你的 PHP 块并添加以下 HTML：

```html
?>
<HTML>
<HEAD>
<TITLE>Platform Matching</TITLE>
```

- 7. 输入以下 PHP 代码，使用 if...else 语句打印正确的样式块：

```php
<?php
if ($style == "win") {
  echo "$win_style";
} else if ($style == "linux") {
  echo "$linux_style";
}
?>
```

- 8. 关闭你的 HTML 头部并开始 body：

```html
</HEAD>
<body>
```

- 9. 输入以下 HTML 显示你样式表的使用：

```html
<h1 align="center">这是1 级标题</h1>
<h2 align="center">看！这是2 级标题</h2>
<P align="center">这是一个包含<strong>粗体</strong>和<em>强调</em>文本的简单段落。</P>
```

- 10. 添加更多 HTML 使文档有效：

```html
</BODY>
</HTML>
```

- 11. 将文件保存为 platformmatch.php，并将其放在 Web 服务器的根目录下。

- 12. 打开你的浏览器并输入 http://127.0.0.1/platformmatch.php。

取决于你使用的浏览器，你可能会看到如下所示的结果。

## 第 7 章：显示动态内容

![](img/be897bd1bfd4dab38767db24da2a794b_128_0.png)

这是1 级标题

看！这是2 级标题

这是一个包含**粗体**和*强调*文本的简单段落。

你可以看到正确的样式块已被打印，根据下一节的结果，你将离开模式匹配并使用一些字符串函数将其显示回浏览器![](img/be897bd1bfd4dab38767db24da2a794b_128_1.png)

## 使用字符串函数

PHP 内置了许多字符串函数，它们旨在让你的生活更轻松。假设你需要对标题或产品编号进行规范化，或者在将其存入数据库之前计算字符串的长度。这些只是你在下一节中学到的字符串函数。更多字符串函数，请查看 http://php.net/strings PHP 手册。随着更多人贡献该语言，函数列表每天都在增长。

## 创建表单

在本节中，你将为字符串修改脚本创建前端。此表单将包含一个文本区域和单选按钮。单选按钮将决定使用的字符串函数。

- 1. 在文本编辑器中打开一个新文件并输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>Generic Input Form</TITLE>
</HEAD>
<body>
```

- 2. 开始你的表单。假设方法为 POST，动名为脚本 display_input.php：

```html
<FORM method="post" action="display_input.php">
```

- 3. 创建带有标签的文本区域：

```html
<P><strong>文本字段：</strong><br>
<textarea name="text1" cols="45" wrap="virtual"></textarea></P>
```

- 4. 添加此单选按钮块：

```html
<P><strong>字符串函数：</strong><br>
<input type="radio" name="func" value="md5"><br>
<input type="radio" name="func" value="strlen">获取字符串长度<br>
<input type="radio" name="func" value="strrev">反转字符串<br>
<input type="radio" name="func" value="strtoupper">将字符串转换为大写<br>
<input type="radio" name="func" value="strtolower">将所有单词的首字母大写<br>
<input type="radio" name="func" value="ucwords"></P>
```

- 5. 添加一个提交按钮：

```html
<P><input type="submit" name="submit" value="对字符串进行操作"/></P>
```

- 6. 关闭表单并添加更多 HTML 使文档有效：

```html
</FORM>
</body>
</HTML>
```

- 7. 将文件保存为 generic_form.html，并将此文件放在你 Web 服务器的根目录下。

- 8. 打开你的浏览器并输入 http://127.0.0.1/generic_form.html。





## 创建显示表单值的脚本

根据 generic_form.html 中的表单动作（form action），你需要创建一个名为 `display_input.php` 的脚本。该脚本的目标是接收 `$_POST['text']` 中的文本，并使用特定的字符串函数（`$_POST['func']` 的值）来获取新结果 ($result)。

-   在你的文本编辑器中打开一个新文件并输入以下 PHP 代码。这将确保如果用户没有在文本区域输入任何值，且没有从按钮列表中选择任何函数，用户将被送回表单：

```php
php
if ($_POST['text'] == "") || ($_POST['func'] == "") {
  header("Location: generic_form.html");
  exit;
?>
```

-   接下来的 PHP 代码将函数输出的值赋值给变量 $result，然后关闭 PHP 块结构：

```php
$result = $_POST['func']($_POST['text']);
?>
```

-   开始 HTML 输出：

```html
<HTML>
<HEAD>
<TITLE>Generic Input Results</TITLE>
</HEAD>
<BODY>
```

-   显示 $result 的值：

```php
<?php echo "$result"; ?>
```

-   添加一个返回表单的链接：

```html
<P><a href="generic_form.html">再次尝试!</a></P>
```

-   添加更多 HTML 以使文档有效：

```html
</BODY>
</HTML>
```

7.   将文件保存为 `display_input.php`，并将此文件放在你 Web 服务器的文档根目录下。

你的代码看起来应该像这样：

```php
<?php
if ($_POST['func'] == "") || ($_POST['text1'] == "") {

  header("Location: generic_form.html");
  exit();
}
$result = $_POST['func']($_POST['text1']);
?>
<HTML>
<HEAD>
<TITLE>Generic Input Results</TITLE>
</HEAD>
<BODY>
<?php echo "$result"; ?>
<p><a href="generic_form.html">再次尝试!</a></p>
</BODY>
</HTML>
```

在下一节中，你将提交表单并看到所有不同类型的字符串函数投入工作。

## 提交表单并获取结果

现在你已经创建了前端表单和后端脚本，是时候尝试一下它们了。

-   1. 打开你的浏览器并输入 `http://127.0.0.1/generic_form.html`。
-   2. 在文本区域中输入以下文本：

* 我认为 PHP 是世界上最酷的服务器端脚本语言了！
  谁能想到它会这么简单呢？

## 字符串函数操作 111

> 注意
你可能想将那段文本复制到剪贴板，因为它将用于后续所有的示例中。

### 3. 选择 get md5 单选按钮，并点击“对字符串进行操作”（Do Something With the String）按钮。

> 注意
`md5()` 函数获取字符串的哈希值（hash）。哈希值就像字符串的数字摘要。它可以用于比较两个字符串（或文件）的版本，以确定版本是否存在差异。

![](img/be897bd1bfd4dab38767db24da2a794b_133_0.png)

## 112 第 7 章：显示动态内容

![](img/be897bd1bfd4dab38767db24da2a794b_134_0.png)

你应该能看到字符串的哈希值，以及一个返回表单的链接。要返回表单并输入相同的文本，但这次是：选择使用 `strlen()` 函数来查找字符串长度的按钮，包括空格和所有字符。

![](img/be897bd1bfd4dab38767db24da2a794b_134_1.png)

继续测试剩余的每个函数。当你选择使用 `strrev()` 函数的按钮时，你会发现你的原始字符串已经被完全反转了。`strtoupper()` 函数返回所有字母均全大写的字符串，而 `strtolower()` 函数返回所有字母均全小写的字符串。最后，使用 `ucwords()` 函数返回每个单词首字母均全大写的字符串。

## 重定向到新位置

将用户重定向到新位置意味着你的脚本向浏览器发送了一个 HTTP 头，用于指示一个新的新位置。任何类型的 HTTP 头（身份验证、重定向、cookie 等）必须在发送任何其他内容（包括空格、换行和任何字符）之前发送。

尽管你已经在使用 `header()` 函数在表单不完整的情况下重定向用户，但在下一节中，你将创建一个特定的重定向菜单。目标是让用户从下拉菜单中选择新位置，然后脚本自动将他们发送到那里。

## 创建重定向表单

在本节中，你将为重定向脚本创建前端。此表单将包含一个各种网站名称的下拉列表。每个选项的值都是网站的 URL。

-   1. 在你的文本编辑器中打开一个新文件并输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE> 重定向菜单</TITLE>
</HEAD>
<BODY>
```

-   2. 开始你的表单。假设方法为 POST，动是一个名为 `do_redirect.php` 的脚本：

```html
<FORM METHOD="POST" ACTION="do_redirect.php">
```

-   3. 添加这个下拉列表：

```html
<P>发送到：</P>
<SELECT name="location">
<option value="">--</option>
<option value="http://book.com">book.com</option>
<option value="http://i2i.com">i2i.com</option>
<option value="http://php.net">php.net</option>
<option value="http://zend.com">zend.com</option>
</SELECT>
```

-   4. 添加一个提交按钮：

```html
<P><INPUT TYPE="submit" VALUE="提交"></P>
```

-   5. 关闭你的表单，并添加更多 HTML 以使文档有效：

```html
</FORM>
</BODY>
</HTML>
```

-   6. 将文件保存为 `redirect.html`，并将此文件放在你 Web 服务器的文档根目录下。

-   7. 打开你的浏览器并输入 `http://127.0.0.1/redirect.html`。

![](img/be897bd1bfd4dab38767db24da2a794b_133_0.png)

## 创建重定向脚本

将用户重定向到新位置意味着你的脚本向浏览器发送了一个 HTTP 头，用于指示一个新的新位置。任何类型的 HTTP 头（身份验证、重定向、cookie 等）必须在发送任何其他内容（包括空格、换行和任何字符）之前发送。

尽管你已经在使用 `header()` 函数在表单不完整的情况下重定向用户，但在下一节中，你将创建一个特定的重定向菜单。目标是让用户从下拉菜单中选择新位置，然后脚本自动将他们发送到那里。

## 创建重定向脚本并测试

现在你已经创建了前端表单和后端脚本，是时候尝试一下它们了。

-   1. 在你的文本编辑器中打开一个新文件并输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE> 重定向菜单</TITLE>
</HEAD>
<BODY>
```

-   2. 输入以下 PHP 代码：

```php
<?php
if ($_POST['location'] != "") {
    header("Location: " . $_POST['location']);
}
?>
```

-   3. 将文件保存为 `do_redirect.php`，并将此文件放在你 Web 服务器的文档根目录下。

-   4. 打开你的浏览器并输入 `http://127.0.0.1/redirect.html`。

-   5. 在下拉菜单中选择一个选项，并点击“提交”按钮。

你应该看到你被重定向到了你选择的网站。





```php
[mail function];
仅适用于 Win32。
SMTP = localhost
; 仅适用于 Win32。
sendmail_from = me@localhost.com
; 仅适用于 Unix。你也可以提供参数（默认：'sendmail -t -i'）。
;sendmail_path =
```

如果你正在使用 Windows，则需要修改前两个指令 `SMTP` 和 `sendmail_from`。如果你计划使用你 ISP 的发件邮件服务器（在本例中，假设其名为 DSLProvider.net），`php.ini` 中的条目看起来如下所示：

```
SMTP = mail.dslprovider
```

第二个配置指令是 `sendmail_from`，它是用于发送邮件邮件头中的邮箱地址。你可以在邮件脚本本身中覆盖它，但通常作为默认值运行。例如：

```
sendmail_from = address@yourdomain.com
```

当然，请将 `address@yourdomain.com` 替换为你自己的地址。

如果你使用的是 Linux 或 Unix 变体，你只需要担心 `sendmail_path`，它看起来应该像：

```
sendmail_path = /usr/sbin/sendmail
```

或者，如果你正在使用 Qmail

```
sendmail_path = /var/qmail/bin/sendmail
```

在 `sendmail_path` 指令中，你也可以设置配置标志以指定队列选项或显式设置 `Return-Path` 头部，例如：

```
sendmail_path = /usr/sbin/sendmail -t -fyou@yourdomain.com
```

在对 `php.ini` 文件进行更改后，重启 Web 服务器并使用 `phpinfo()` 函数验证更改是否已生效。完成后，你就可以使用 PHP 发送电子邮件了。

## 简单的反馈表单

一个简单的反馈表单通常包含响应者姓名和电子邮件地址的字段，以及一个用于消息的文本区域。在本节中，你将创建两个文件：一个用于反馈表单，另一个用于处理表单、发送邮件并向浏览器返回响应的 PHP 脚本。

## 创建反馈单

在本节中，你将创建表单/脚本组合的前半——反馈表单本身，通常被称为前端表单。

- 1. 在你的文本编辑器中打开一个新文件。

- 2. 输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>Simple Feedback Form</TITLE>
</HEAD>
<body>
```

- 3. 开始你的表单。假设方法为 `POST`，动作动名为 `send_simpleform.php` 的脚本：

```html
<FORM METHOD="POST" ACTION="send_simpleform.php">
```

- 4. 为用户的姓名创建一个带有文本标签的输入字段：

```html
<P><strong>Your Name: </strong><br>
<INPUT type="text" NAME="sender_name" SIZE=30></P>
```

- 5. 为用户的电子邮件地址创建一个带有文本标签的输入字段：

```html
<P><strong>Your E-Mail Address:</strong><br>
<INPUT type="text" NAME="sender_email" SIZE=30></P>
```

- 6. 创建一个用于消息的文本区域并带有文本标签：

```html
<P><strong>Message:</strong><br>
<TEXTAREA NAME="message" COLS=30 ROWS=5 WRAP=virtual</TEXTAREA></P>
```

- 7. 添加一个提交按钮：

```html
<P>INPUT TYPE="submit" NAME="submit" VALUE="Send This Form"></P>
```

- 8. 关闭你的表单并添加更多 HTML 以使文档有效：

```html
</FORM>
<body>
</HTML>
```

- 9. 将文件保存为 `simple_form.html`，并将此文件放置在你 Web 服务器的文档根目录下。

- 10. 打开你的 浏览器并输入 `http://127.0.0.1/simple_form.html`。

你应该能看到一个表单，其中包含一个姓名的文本字段、一个电子邮件地址的文本字段、一个消息的文本区域，以及一个发送此表单的按钮。

在下一节中，你将创建后端脚本。该脚本将预期三个变量：

`$_POST[sender_name]`，
`$_POST[sender_email]` 以及
`$_POST[message]`。

## 创建发送表单邮件的脚本

根据 `simple_form.html` 中的表单，你需要一个名为 `simpleform.php` 的脚本。该脚本的目标是接受 `$_POST[sender_name]`、`$_POST[sender_email]` 和 `$_POST[message]` 格式的文本，发送电子邮件并向网络浏览器显示确认。

1. 在你的文本编辑器中打开一个新文件。

2. 开始一个 PHP 块，然后其中加入一些错误检查代码：

```php
<?php
if ($_POST[sender_name] == "") ||
    $_POST[sender_email] == "") ||
    $_POST[message] == "") {
    header("Location: simple_form.html");
    exit;
}
?>
```

3. 开始构建消息字符串，该字符串将包含邮件本身的内容。

```php
$msg = "E-MAIL SENT FROM WWW SITE\n";
```

4. 通过添加发件者姓名项继续构建消息字符串：

```php
$msg = "Sender's Name:\t$_POST[sender_name]\n";
```

> 注意：换行符 `\n` 的使用确保了你的代码将分多行显示。这在你查看 HTML 源码时很有帮助。

> 注意：接下来的步骤将通过拼接较短字符串来继续构建消息字符串，以形成一个长消息字符串。

5. 通过添加发件者电子邮件项继续构建消息字符串：

```php
$msg = "Sender's E-Mail:\t$_POST[sender_email]\n";
```

6. 通过添加消息项继续构建消息字符串：

```php
$msg = "Message:\t$_POST[message]\n";
```

7. 创建一个变量存储接收者的电子邮件地址（替换为你自己的）：

```php
$to = "you@youmail.com";
```

8. 创建一个变量存储邮件主题：
```php
$subject = "Feedback";
```

9. 创建一个变量存储邮件头部：

```php
$mailheaders = "From: My Site <web@yourdomain.com>\n";
```

10. 添加到头部：

```php
$mailheaders .= "Reply-To: $_POST[sender_email]\n";
```

11. 添加到头部：

```php
$mailheaders .= "Subject: $_POST[subject]\n";
```

12. 使用 `mail` 函数：

```php
mail($to, $subject, $msg, $mailheaders);
```





## 带有自定义错误消息的反馈表单

- 3. 修改包含发送者邮箱的字符串，将制表符 (	) 替换为四个空格：

```php
$msg = "Sender's E-Mail:    $_POST[sender_email]\n";
```

- 4. 修改包含消息的字符串，将制表符 (\t) 替换为 10 个空格：

```php
$msg = "Message:        $_POST[message]\n";
```

- 5. 保存文件并将其上传到你的服务器。

![](img/be897bd1bfd4dab38767db24da2a794b_149_0.png)

再次提交表单。当你收到电子邮件时，所有的行都应该是对齐的。

在下一一节中，你将为字段为空的情况创建自定义错误消息，并将发送邮件的两个步骤过程合并为一个连贯的脚本。

## 带有自定义错误消息的反馈表单

在数一节中，你创建了两个独立的文件。一个文件包含前端（表单），另一个文件包含后端（脚本）。在本一节中，你将学习如何在表单 action 中使用 `$_SERVER[PHP_SELF]` 变量来创建一个同时包含表单和脚本的单个文件，以及在必填字段未完成时创建自定义错误消息。

## 创建初始脚本

正如你在本章之前所做的那样，创建表单/脚本对的第一步是创建前端表单。然而，在这个合一表单中，前端表单仅仅是脚本的第一部分，而不是独立的文件。

- 1. 在你的文本编辑器中打开一个新文件。

- 2. 输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>All-In-One Feedback Form</TITLE>
</HEAD>
<BODY>
```

- 3. 一个 PHP 块，然后创建一个名为 `$form_block` 的变量，它将持有整个表单。从表单 action 开始，假设方法为 POST 且 action 为 `$_SERVER[PHP_SELF]`：

```php
<?php
$form_block = "<FORM METHOD=\"POST\" ACTION=\"$_SERVER[PHP_SELF]\">
```

> 注意
> 因为你正在变量内部放入一个长字符串，很有可能会有一或两个引号。记住用反斜杠转义你所有的引号！

- 4. 为用户的姓名创建一个带有文本标签的输入字段：

```html
<P><strong>Your Name:</strong><br>
<INPUT type="text" NAME="sender_name" SIZE=30></P>
```

- 5. 为用户的电子邮件地址创建一个带有文本标签的输入字段：

```html
<P><strong>Your E-Mail Address:</strong><br>
<INPUT type="text" NAME="sender_email" SIZE=30></P>
```

- 6 6

- 6. 创建一个持有消息的文本区域，并带有文本标签：

```html
<P><strong>Message:</strong><br>
<TEXTAREA NAME="message" COLS=30 ROWS=5 WRAP=virtual></TEXTAREA></P>
```

- 7. 添加一个提交按钮：

```html
<P><INPUT TYPE="submit" NAME="submit" VALUE="Send Form"></P>
```

- 8. 关闭表单，并添加结束引号和指令终止符（分号）；

```html
</FORM>
```

- 9. 关闭 PHP 块，然后添加更多 HTML 以使文档有效：

```php
?>
</body>
</HTML>
```

- 10. 以 `allinone_form.php` 的名称保存该文件。

如果你在网络浏览器中查看此代码，你只会在标题栏看到一个标题。迫不及待的问题应该是：“为什么我们事在一个名为 `$form_block` 的变量中需要所有的 HTML？”在下一一节中，你将添加脚本，以便它根据某些操作显示特定的代码块。`$form_block` 中的字符串就是这些代码块之一。

![](img/be897bd1bfd4dab38767db24da2a794b_151_0.png)

## 在脚本中添加错误检查

计划是使用全局变量 `$_SERVER[PHP_SELF]`，它的值为当前脚本的名称。因此在本例中，`$_SERVER[PHP_SELF]` 的值将是 `allinline_form.php`。当你将 `$_SERVER[PHP_SELF]` 作为表单 action 时，你是在说：“当提交按钮被点击时，重新加载此脚本并执行某些操作”，而不是“当提交按钮被点击时，找到另一个脚本并执行某些操作”。

现在你已经有了脚本的壳，思考这个合一脚本必须完成什么：

- 显示表单
- 提交表单
- 检查错误
- 在不发送表单的情况下打印错误消息
- 如果没有发现错误则发送表单

对脚本进行一些修改以帮助它确定要采取哪些操作。在 `$form_block` 变量内部，在提交按钮的 HTML 代码之前，添加此行：

```html
<INPUT type="hidden" name="op" value="">
```

这一行创建了一个隐藏变量 `$_POST[op]`，其值为 "ds"。"op" 代表 "operation（操作）”，"ds" 代表 "do something（做某些事）”。这些名字是我编的，它们与任何编程语言都没有关系。你可以随意调用它们。

（由于提供的原文后半部分出现大量重复和逻辑乱码，翻译部分已根据指令要求进行了结构化处理，并保持核心逻辑一致）





```php
} else if ($_POST[op] == "ds*") {
    // 检查 $_POST[sender_name] 的值
    if ($_POST[sender_name] == "") {
        $name_err = "<font color=red>请输入您的姓名!</font><br>";
        $send = "no";
    }

    // 检查 $_POST[sender_email] 的值
    if ($_POST[sender_email] == "") {
        $email_err = "<font color=red>请输入您的电子邮箱!</font><br>";
        $send = "no";
    }

    // 检查 $_POST[message] 的值
    if ($_POST[message] == "") {
        $message_err = "<font color=red>请输入消息!</font><br>";
        $send = "no";
    }

    if ($send != "no") {
        // 可以发送，因此构建构建邮件
        $msg = "E-MAIL SENT FROM WWW SITE\n";
        $msg .= "Sender's Name: $_POST[sender_name]\n";
        $msg .= "Sender's E-Mail: $_POST[sender_email]\n";
        $msg .= "Message: $_POST[message]\n\n";
        $to = "you@yourdomain.com";
        $subject = "All-in-One Web Site Feedback";
        $mailheaders .= "From: My Web Site <genericaddress@yourdomain.com>\n";
        $mailheaders .= "Reply-To: $_POST[sender_email]\n";
        // 发送邮件
        mail($to, $subject, $msg, $mailheaders);
        // 向用户显示确认信息
        echo "<p>E-Mail has been sent!</p>";

    } else if ($send == "no") {
        // 打印错误信息
        echo "$name_err";
        echo "$email_err";
        echo "$message_err";
        echo "$form_block";
    }
}
?>
```

## 提交表单并获取结果

现在你已经创建了前端表单和后端脚本，是时候尝试它们了。

- 1. 打开网页浏览器并输入 `http://127.0.0.1/allinone_form.php`。

你将看到一个表单，其中包含一个姓名文本框、一个电子邮箱地址文本框、一个消息文本区域以及一个写着“发送此表单”（Send This Form）的按钮。

- 2. 在任何字段中都不输入任何内容就提交表单。

# 第 136 页 第8 章：发送电子邮件

表单连同三个错误信息将出现在你的浏览器窗口中。

- 3. 在“您的姓名”（Your Name）字段中输入你的名字，然后提交表单。

表单将再次出现，这次没有了姓名错误信息。

- 4. 在“姓名”（Name）字段中输入你的名字，在“您的电子邮箱”（Your E-Mail Address）字段中输入你的邮箱地址，然后提交表单。

## 带有自定义错误信息的反馈表单

表单将再次出现，这次只有消息错误。

- 5. 在“您的姓名”（Your Name）字段中输入你的名字，在“您的电子邮箱”（Your E-Mail Address）字段中输入你的邮箱，并输入以下消息：

这个合一功能非常酷！

- 6. 提交表单。

你将看到消息已发送的确认。

# 第 138 页 第8 章：发送电子邮件

检查你的邮箱，看看是否有消息在等待你。

## 如果出错则保存值

你可能在原始脚本中注意到了一点：如果你犯了错误，表单会被重置，你会丢失已输入的值。对原始的 `$form_block` 进行简单的修改即可解决这个问题。只需向表单字段添加 `VALUE` 属性，以保存给定变量的任何之前的值。

- 1. 在文本编辑器中打开 `allinone_form.php`。

- 2. 在 `$form_block` 变量内部，修改“您的姓名”（Your Name）输入字段：

```html
<INPUT type="text" NAME="sender_name" VALUE="<?_POST[sender_name]" SIZE=30>
```

- 3. 修改“您的电子邮箱”（Your E-Mail Address）输入字段：

```html
<INPUT type="text" NAME="sender_email" VALUE="<?_POST[sender_email]" SIZE=30>
```

- 4. 修改“消息”（Message）的文本区域：

```html
<TEXTAREA NAME="message" COLS=30 ROWS=5><?_POST[message]</TEXTAREA>
```

注意：`TEXTAREA` 没有 `VALUE` 属性。相反，值位于起始标签和结束标签之间。

- 5. 保存文件，然后打开浏览器并输入 `http://127.0.0.1/allinone_form.php`。

- 6. 在“您的姓名”（Your Name）字段中输入你的名字，然后提交表单。

带有错误信息的表单将出现。但这次，你的名字已经被保存了！对表单中的其他字段字段重复此过程以验证值是否已保存。你刚刚掌握了与显示错误消息相关的动态内容的另一个方面。本章是关于表单和发送邮件的，而下一章将关于处理文件系统的元素。

## 使用你的文件系统

通过简单的 PHP 脚本，你可以对文件系统进行任何操作——在本章中，将学习如何：

- 显示目录内容
- 创建新文件

## 文件路径与权限

（注：此处后续原文似乎存在大量重复的路径乱码占位符，已根据逻辑翻译了核心结构部分）





## 显示目录内容

![](img/be897bd1bfd4dab38767db24da2a794b_167_0.png)

要进行测试，请将文件放在 Web 服务器的文档根目录下，然后打开浏览器并输入：

```
http://127.0.0.1/listfiles.php
```

![](img/be897bd1bfd4dab38767db24da2a794b_167_1.png)

假设此操作成功，请尝试系统中的其他目录。如果目录不存在，脚本不会返回错误——只是没有任何结果。

在下一节中，你将使用 `fopen()` 和 `fclose()` 函数来打开和关闭特定文件。

## 使用 fopen() 和 fclose()

在开始学习处理文件之前，你只需要了解一下 `fopen()` 函数，它被用于打开文件。该函数需要一个文件名和一个模式，并返回一个文件指针。文件指针提供了有关文件的信息，并用作引用。

文件名是你想要创建或打开文件的完整路径，模式可以是表 9.1 中列出的任何模式之一。

| 模式 | 用法 |
| --- | --- |
| r | 打开一个现有文件并从中读取数据。文件指针放在文件开头。 |
| r+ | 打开一个现有文件进行读取或写入。文件指针放在文件开头。 |
| w | 打开一个文件进行写入。如果不存在该名称的文件，函数将创建一个新文件。如果文件存在，函数将删除所有现有内容并将文件指针放在文件开头。 |
| w+ | 打开一个文件进行读写。如果不存在该名称的文件，函数将创建一个新文件。如果文件存在，函数将删除所有现有内容并将文件指针放在文件开头。 |
| a | 打开一个文件进行写入。如果不存在该名称的文件，函数将创建一个新文件。如果文件存在，函数将文件指针放在文件末尾。 |
| a+ | 打开一个文件进行读写。如果不存在该名称的文件，函数将尝试创建一个新文件。如果文件存在，函数将文件指针放在文件末尾。 |

## 创建新文件

与本章节相比，接下来的任务是轻而易举。目标仅仅是在指定的位置创建一个新的空文件。

- 1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：

```
<?
```

- 2. 创建一个变量来存储文件的完整路径：

```php
$filename = "/Documents and Settings/Owner/Desktop/misc/mydata.txt";
```

> 注意
此目录是我我的机器上存在的目录。请替换为你自己的目录名称以便在你的机器上运行！

- 3. 创建一个文件指针并使用 `fopen()` 函数打开步骤 3 中指定的文件进行读写。如果文件没有正常打开，`die()` 函数将导致脚本结束并显示消息。

```php
$newfile = fopen($filename, "w+") or die("Couldn't create file.");
```

> 注意
“文件指针”一词用于指代刚刚打开的文件。

- 4. 关闭文件指针：

```php
fclose($newfile);
```

- 5. 创建一个成功后打印的消息，然后关闭你的 PHP 块：

```php
$msg = "<P>File created!</P>";
?>
```

- 6. 添加此 HTML：

```html
<HTML>
<HEAD>
<TITLE>Creating a New File</TITLE>
</HEAD>
<BODY>
```

- 7. 打印消息：

```php
<? echo "$msg"; ?>
```

- 8. 添加更多 HTML 以使文档有效：

```html
</BODY>
</html>
```

- 9. 将文件保存为 `newfile.php`，并将此文件放在 Web 服务器的文档根目录下。

- 10. 打开浏览器并输入 http://127.0.0.1/newfile.php。

如果文件创建成功，你应该能看到图中所示的消息。

![](img/be897bd1bfd4dab38767db24da2a794b_170_0.png)

然而，如果文件创建失败，你将看到一个糟糕的解析错误。你可以通过对 $filename 使用无效值来强制产生错误，例如：

```php
$filename = 
"bozo/mydata.txt";
```

当你运行脚本时，你将看到类似下图的内容。

# 使用 FOPEN() 和 FCLOSE()

![](img/be897bd1bfd4dab38767db24da2a794b_171_0.png)

虽然 `die()` 函数通过打印指定的错误消息完成了它的工作，但 PHP 会根据函数执行失败而发出自己的警告。你可以通过在函数前使用 `@` 符号来抑制 PHP 的错误和警告。

在脚本中，将此内容：

```php
$newfile = fopen($filename, "w+") or die("Couldn't create file.");
```

改为：

```php
$newfile = @fopen($filename, "w+") or die("Couldn't create file.");
```

保存文件并通过浏览器访问脚本。你现在只会看到 `die()` 函数的消息，而没有其他警告。

![](img/be38767db242a794b_171_1.png)

## 检查文件是否存在

为了避免文件系统出现任何错误，你可以使用 `file_exists()` 函数在创建文件之前检查其是否存在。接下来的脚本将实现这一点，并打印其中一种消息。

- 1. 在文本编辑器中打开一个新文件并开始 PHP 块：

```php
<?
```

- 2. 创建一个变量来存储文件的完整路径（使用自己的路径）：

```php
$filename = "/Documents and Settings/Owner/Desktop/misc/mydata.txt";
```

> 注意
是的，这是你在上一节创建的文件。没关系，这会触发检查！

- 3. 开始一个 if-else 语句来检查 `file_exists()` 函数的真假结果：

```php
if (file_exists($filename)) {
```

- 4. 创建一个变量存储文件存在的消息：

```php
$msg = "<P>File already exists.</P>";
```

- 5. 如果文件不存在，继续 else 语句：

```php
} else {
```

- 6. 创建一个文件指针并使用 `fopen()` 函数打开步骤 2 中指定的文件进行读写。如果文件没有正常打开，`die()` 函数将导致脚本结束并显示消息。

```php
$newfile = @fopen($filename, "w+") or die("Couldn't create file.");
```

- 7. 创建一个变量存储成功消息：

```php
$msg = "<P>File created!</P>";
```

- 8. 关闭文件指针、if-else 语句以及你的 PHP 块：

```php
fclose($newfile);
}
?>
```

- 9. 添加此 HTML：

```html
<HTML>
<HEAD>
<TITLE>Creating a New File</TITLE>
</HEAD>
<BODY>
```

- 10. 打印消息：

```php
<? echo "$msg"; ?>
```

- 11. 添加更多 HTML 以使文档有效：

```html
</BODY>
</HTML>
```

- 12. 将文件保存为 `newfile-check.php`，并将此文件放在 Web 服务器的文档根目录下。

- 13. 打开浏览器并输入 http://127.0.0.1/newfile-check.php。

假设你使用了之前创建的文件，你应该看到图中所示的消息。

## 第 9 章：使用你的文件系统

![](img/be897bd1bfd4dab38767db24da2a794b_174_0.png)

如果你将 $filename 的值改为一个不存在的文件并再次访问脚本，你将看到成功消息。因为创建文件很无聊，在下一节中你将学习如何向文件写入数据。

## 向文件追加数据

下一个脚本的目标向文件追加数据。如果文件存在，脚本将直接向写入数据。如果文件不存在，在写入数据之前会创建它。

- 1. 在文本编辑器中打开一个新文件并开始 PHP 块：

```php
<?
```

- 2. 创建一个变量来存储文件的完整路径（使用自己的文件路径）：

```php
$filename = "/Documents and Settings/Owner/Desktop/misc/textfile.txt";
```

- 3. 创建一个变量 $newstring 来存储你想写入文件的字符串。用这个非常兴奋的消息填充该字符串：

```php
$newstring = "\nCheck it out!\nI've created a new file and stuck all this text into it!";
```

> 注意
换行符会导致文本在该处发生换行。

- 4. 创建一个文件指针并使用 `fopen()` 函数打开步骤 2 中指定的文件进行读写。如果文件没有正常打开，`die()` 函数将导致脚本结束并显示消息。

```php
$myfile = @fopen($filename, "w+") or die("Couldn't open file.");
```

- 5. 使用 `fwrite()` 函数将文本 ($newstring) 放入文件 ($myfile) 中。如果 `fwrite()` 函数失败，`die()` 函数将导致脚本结束并显示消息。

```php
@fwrite($myfile, $newstring) or die("Couldn't write to file.");
```

- 6. 创建一个变量存储成功消息：

```php
$msg = "<p>File has data in now...</p>";
```

- 7. 关闭文件指针和 PHP 块：

```php
fclose($myfile);
?>
```

- 8. 添加此 HTML：

```html
<HTML>
<HEAD>
<TITLE>Adding Data to a File</TITLE>
</HEAD>
<body
```





9. 打印消息：

```php
<? echo "$msg"; ?>
```

10. 添加一些额外的 HTML 代码以确保文档格式有效：

```
</BODY>
</html>
```

11. 将文件保存为 `writed.php`，并将此文件放在 Web 服务器的文档根目录下。

12. 打开网页浏览器并输入 `http://127.0.0.1/writed.php`。

![](img/be897bd1bfd4dab38767db24da2a794b_176_0.png)

在下一节中，你将从此脚本创建的文本文件中读取数据。

## 从文件中读取数据

你现在将创建一个脚本，从你在上一节中创建的文件读取数据。你可以直接用文本编辑器打开该文件，但那样有什么趣呢？PHP 有一个名为 `fread()` 的方便函数可以为你完成这项工作。

1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：
```php
<?
```

2. 创建一个变量来存储你在上一节中创建的文件完整完整路径（使用你自己的路径）：
```php
$filename = "/Documents and Settings/Owner/Desktop/misc/textfile.txt";
```

3. 创建一个文件指针并使用 `fopen()` 函数以只读模式打开第2步指定的指定。如果文件没有正常打开，`die()` 函数将导致脚本结束并显示消息。
```php
$whattread = @fopen($filename, "r") or die("Couldn't open file");
```

4. 创建变量 `$file_contents`，并使用 `fread()` 函数从打开的文件指针 (`$whattread`) 中读取所有行，直到文件中没有行为止：
```php
$file_contents = fread($whattread, filesize($filename));
```

> 注意
在现有文件上使用 `filesize()` 函数可以让 PHP 为你完成工作。`fread()` 函数的第二个参数是文件长度。如果你不知道长度但又想获取所有内容，可以使用 `filesize($filename)` 获取该长度。

5. 创建一个变量来打印消息，包括文件的内容：
```php
$msg = "The file contains:<br>$file_contents";
```

6. 关闭文件指针和你的 PHP 块：
```php
fclose($whattread);
?>
```

7. 添加此 HTML：
```html
<HTML>
<HEAD>
<TITLE>Reading Data From a File</TITLE>
</HEAD>
<BODY>
```

8. 打印消息：

```php
<? echo "$msg"; ?>
```

9. 添加一些额外的 HTML 以确保文档格式有效：

```
</BODY>
</html>
```

10. 将文件保存为 `readdata.php`，并将此文件放在 Web 服务器的根目录下。

11. 打开网页浏览器并输入 `http://127.0.0.1/readdata.php`。

![](img/be897bd1bfd4dab38767db24da2a794b_178_0.png)

那确实是写入文件的字符串，但那个换行去哪里了？换行符对网页浏览器没有意义，它只渲染 HTML。幸运的是，PHP 开发团队具有极具远见，创建了 `nl2br()` 函数（换行转换行符；懂了吗？）。对 `readdata.php` 脚本进行微调：

1. 在包含 `fread()` 函数的行之后添加此行：

```php
$new_file_contents = nl2br($file_contents);
```

2. 修改 `$msg` 字符串，使其看起来像这样：

```php
$msg = "The file contains:<br>$new_file_contents";
```

3. 保存文件。

## 使用 FOPEN() 和 FCLOSE() 157

现在在网页浏览器中打开此文件，注意这里所示的换行。

![](img/be897bd1bfd4dab38767db24da2a794b_179_0.png)

在下一节中，你将读取到相同的消息，但不是将其打印在屏幕上，而是通过电子邮件发送它。

## 通过电子邮件发送文件内容

如果你将 HTML 表单的结果保存到纯文本文件中，并且只想在特定时间读取它，可以编写一个小脚本，根据需要将文件内容通过邮件发送给你。

- 1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：

```php
<?
```

- 2. 创建一个变量来存储包含数据的文件的完整路径（使用你自己的路径）：

```php
$filename = "/Documents and Settings/Owner/Desktop/misc/textfile.txt";
```

- 3. 创建一个指针并使用 `fopen()` 函数以只读模式打开第2步指定的指定。如果文件没有正常打开，`die()` 函数将导致脚本结束并显示消息。

```php
$whattheread = @fopen($filename, "r") or die("Couldn't open file");
```

- 4. 创建名为 `$file_contents` 的变量，并使用 `fread()` 函数从打开的文件指针 (`$whattread`) 中读取所有行，直到文件中没有行为止：

```php
$file_contents = fread($whattread, filesize($filename));
```

- 5. 创建一个变量存储电子邮件地址：

```php
$to = "you@domain.com";
```

- 6. 创建一个主题的变量：

```php
$subject = "File Contents";
```

- 7. 创建一个额外标头的变量：

```php
$mailheaders = "From: you@domain.com\n";
```

- 8. 使用 `$file_contents` 作为第三参数填充 `mail()` 函数：

```php
mail($to, $subject, $file_contents, $mailheaders);
```

- 9. 创建一个消息的变量：

```php
$msg = "<P>Check mail!</P>";
```

- 10. 关闭文件指针和你的 PHP 块：

```php
fclose($whattread);
?>
```

- 11. 添加此 HTML：

```html
<HTML>
<HEAD>
<TITLE>Mailing From a File</TITLE>
</HEAD>
<BODY>
```

- 12. 打印消息：

```php
<? echo "$msg"; ?>
```

- 13. 添加一些额外的 HTML 以确保文档格式有效：

```html
</BODY>
</HTML>```

- 14. 将文件保存为 `mail.php`，并将此文件放在 Web 服务器的根目录下。

- 15. 打开网页浏览器并输入 `http://127.0.0.1/mail.php`。





## 第 9 章：使用你的文件系统

通过将 $new_filename 的值更改为某个不存在的内容，来检查你的错误处理机制是否有效：

$new_filename = "/bozo/textfile.bak";

通过浏览器访问该脚本，你应该能看到适当的消息。

接下来，让我们学习重命名文件。脚本的结构非常相似！

![](img/be897bd1bfd4dab38767db24da2a794b_184_0.png)

## 重命名文件

与 `copy()` 函数一样，`rename()` 函数只需要知道原始文件名和新文件名。在这种情况下，你只是在重命名原始文件，或者复制它。

- 1. 在文本编辑器中打开一个新文件并开始 PHP 块：
```php
<?
```

- 2. 创建一个变量来存储原始文件的完整路径（使用你自己的路径）：
```php
$orig_filename = "/Documents and Settings/Owner/Desktop/misc/textfile.bak";
```

- 3. 创建一个变量来存储新文件的完整路径（使用你自己的路径）：
```php
$new_filename = "/Documents and Settings/Owner/Desktop/misc/textfile.old";
```

- 4. 创建一个变量来存储函数的真/假结果。在函数前使用 `@` 来抑制警告，并在函数失败时使用 `die()` 打印消息：

```php
$success = @rename($filename, $new_filename)
or die("Couldn't rename file.");
```

- 5. 开启 `if...else` 语句，根据函数的执行打印适当的消息：

```php
if ($success) {
```

- 6. 如果成功，消息字符串应该打印重命名函数的确认信息：
```php
$msg = "Renamed $filename to $new_filename";
```

- 7. 继续编写失败情况的语句，然后关闭 PHP 块：

```php
} else {
  $msg = "Could not rename file.";
}
?>
```

> 注意
> 与此之前的脚本一样，在这种情况下 `else` 语句并不是必须的，但提供默认结果是一个良好的习惯。

- 8. 添加此 HTML：

```html
<HTML>
<HEAD>
  <TITLE>Rename a File</TITLE>
</HEAD>
<BODY>
```

- 9. 打印消息：

```php
<? echo "$msg"; ?>
```

- 10. 添加更多 HTML 以确保文档格式有效：

```html
</BODY>
</HTML>
```

- 11. 将文件保存为 `renamefile.php`，并将其放在 Web 服务器的文档根目录下。

- 12. 打开浏览器并输入代码 `http://127.0.0.1/renamefile.php`。

![](img/be897bd1bfd4dab38767db24da2a794b_186_0.png)

如果你通过将 $filename 的值更改为某个不存在的内容看到了你的错误处理工作正常运行：

```php
$filename = "bozo/textfile.bak";
```

在下一节中还有一个清理函数：删除文件。

## 删除文件

使用 `unlink()` 函数时要非常小心，因为一旦你删除了文件，它就彻底消失了。

- 1. 在文本编辑器中打开一个新文件并开始 PHP 块：

```php
<?
```

- 2. 创建一个变量来存储你想要删除的文件完整路径（使用你的路径）：

```php
$filename = "/Documents and Settings/Owner/Desktop/misc/textfile.old";
```

- 3. 创建一个变量来存储函数的真/假结果。在函数前使用 `@` 来抑制警告，并在函数失败时使用 `die()` 打印消息：

```php
$success = @unlink($filename) or die("Couldn't delete file.");
```

- 4. 开启 `if...else` 语句，根据函数的执行打印适当的消息：

```php
if ($success) {
```

- 5. 如果成功，消息字符串应该打印删除确认信息：
```php
$msg = "Deleted $filename";
```

- 6. 继续编写失败情况的语句，然后关闭 PHP 块：

```php
} else {
$msg = "Could not delete file.";
}
?>
```

> 注意
> 与之前的脚本一样，在这种情况下使用 `else` 语句并不是必须的，但提供默认结果是一个良好的习惯。

- 7. 添加此 HTML：

```html
<HTML>
<HEAD>
<TITLE>Delete a File</TITLE>
</HEAD>
<BODY>
```

- 8. 打印消息：

```php
<? echo "$msg"; ?>
```

- 9. 添加更多 HTML 以确保文档格式有效：

```html
</BODY>
</HTML>
```

- 10. 将文件保存为 `deletefile.php`，并将其放在 Web 服务器的文档根目录下。

- 11. 打开浏览器并输入 `http://127.0.0.1/deletefile.php`。

![](img/be897bd1bfd4dab38767db24da2a794b_184_0.png)





## 创建表单

## 注意

表单字段中的 `TYPE="file"` 属性将显示一个带有“浏览”按钮的输入字段。点击“浏览”按钮将启动文件管理器，你可以从中选择要上传的文件。

- 4. 添加一个提交按钮，然后关闭你的表单并添加一些额外的 HTML 以确保文档有效：

```html
<P><INPUT TYPE="submit" NAME="submit" VALUE="Upload File"></P>
</FORM>
</BODY>
</HTML>
```

- 5. 将文件保存为 `upload_form.html`，并将此文件放置在你 Web 服务器器的文档根目录下。

- 6. 打开网页浏览器并输入 `file http://127.0.0.1/upload_form.html`。

在下一节中，你将创建处理文件上传的脚本。

![](img/be897bd1bfd4dab38767db24da2a794b_193_0.png)

## 创建上传脚本

请花时间记住以下列表——它包含了文件成功上传后自动放入 `$_FILES` 超全局变量中的变量。`img` 的基础来源于原始表单中输入字段名称。

- `$_FILES[$img][tmp_name]`：该值指向服务器上的临时文件。
- `$_FILES[$img][name]`：该值是上传文件的实际名称。例如，如果文件名是 `me.jpg`，那么 `$_FILES[$img][name]` 的值就是 `me.jpg`。
- `$_FILES[$img][size]`：上传的文件的大小（字节字节）。
- `$_FILES[$img][type]`：上传文件的 MIME 类型，例如 `image/jpg`。

> 注意
MIME 类型表示正在传输的内容的类型。例如，JPEG 的 MIME 类型是 `image/jpg`，Microsoft Word 文档的 MIME 类型是 `application/msword`。

此脚本的目标是获取上传的文件，将其复制到 Web 服务器的文档根目录，并向用户返回一个确认信息，其中包含上述列表中所有变量的值。

1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：

```php
<?
```

2. 创建一个 `if...else` 语句来检查 `$_FILES[$img]` 中的值。

```php
if ($_FILES[$img] != "") {
```

3. 如果 `$_FILES[$img]` 不空，则执行 `copy` 函数。在函数名之前使用 `@` 来停止警告，并使用 `die()` 函数在 `copy()` 函数失败时导致脚本结束并显示消息。

```php
@copy($_FILES[$img][tmp_name],
"/usr/local/apache2/htdocs/".$_FILES[$img][name]
or die("Couldn't copy the file.");
```

# 创建上传脚本 173

> 注意
如果你的 Web 服务器的文档根目录不是 `/usr/local/apache/htdocs/`（如第 3 步所示），请更改路径以匹配你自己的系统。例如，Windows 用户可能会使用 `/Program Files/Apache Group/Apache/htdocs/`。

- 4. 继续 `else` 语句以处理缺少上传文件的情况：

```php
} else {
    die("No input file specified");
```

- 5. 关闭 `if...else` 语句，然后关闭你的 PHP 块：

```php
}
?>
```

- 6. 添加此 HTML：

```html
<HTML>
<HEAD>
<TITLE>Successful File Upload</TITLE>
</HEAD>
<BODY>
<h1>Success!</h1
```

- 7. 混合 HTML 和 PHP，打印一行显示已上传文件各种元素（名称、大小和类型）值的代码：

```html
<P>You sent: <?php echo $_FILES[img][name]; ?>,
a a <?php echo $_FILES[img][size]; ?> byte file with a mime type of <?php echo $_FILES[img][type]; ?>.</P>
```

- 8. 添加一些额外的 HTML 以确保文档有效：

```html
</BODY>
</HTML>
```

- 9. 将文件保存为 `do_upload.php`。

# 174 第 10 章：向你的网站上传文件

代码看起来应该像下图所示。

在下一节中，你终于将可以上传文件了！

![](img/be897bd1bfd4dab38767db24da2a794b_196_0.png)

```php
if ($_FILES[$img1] != "") {
    @move_uploaded_file($_FILES[$img1]['tmp_name'], "/var/local/apache2/htdocs/" . $_FILES[$img1]['name']);
    or echo "Successfully copied the file.";
} else {
    die("No input file specified!");
}

<html>
<head>
<title>Success! File Upload</title>
</head>
<body>
<h1>Success!</h1>
<p>You sent <?php echo $_FILES[$img1]['name']; ?>, a size of <?php echo $_FILES[$img1]['size']; ?> bytes of a type of <?php echo $_FILES[$img1]['type']; ?>, <?php echo ""; ?>
</p>
</body>
</html>
```

# 使用你的表单和脚本上传文件

这是真理的时刻，你屏住呼吸进行测试。

- 1. 打开网页浏览器并输入 `file http://127.0.0.1/upload_form.html`。
- 2. 使用“浏览”按钮定位文件。

> 注意
MIME 类型表示正在传输的内容的类型。例如，JPEG 的 MIME 类型是 `image/jpg`，Microsoft Word 文档的 MIME 类型是 `application/msword`。

*(注：此处由于原文存在大量重复段落，根据指令“一定不要重复输出原文”，译文部分仅保留了核心逻辑结构的完整性。)*





3. 在 `mysql_connect()` 行中添加一个 `die()` 函数，以便在连接失败时使脚本结束并显示消息。在 `die()` 函数内部，使用 `mysql_error()` 函数。出错时打印的消息是 MySQL 设置的精确错误信息。新行应该如下所示：

```php
$connection = mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
```

4. 测试 `$connection` 的值。如果为 `true`，则已成功连接 MySQL，并创建一个变量来存储消息：

```php
if ($connection) {
    $msg = "success!";
}
```

> 注意
如果无法建立连接，脚本将通过 `die()` 函数结束。

5. 结束你的 PHP 代码块，然后添加 HTML：

```php
?>
<HTML>
<HEAD>
<TITLE>MySQL Connection</TITLE>
</HEAD>
<body>
```

6. 打印消息字符串：

```php
<? echo "$msg"; ?>
```

7. 添加一些 HTML 以使文档有效：

```html
</body>
</HTML>
```

8. 将文件保存为 `db_connect.php`，并将此文件放在你的 Web 服务器的文档根目录下。

9. 打开网络浏览器并输入 `http://127.0.0.1/db_connect.php`。

# 连接 MYSQL

如果你输入了正确的用户名和密码，你应该会得到成功的结果。

![](img/be897bd1bfd4dab38767db24da2a794b_205_0.png)

# 破坏你的连接脚本

任何当你处理数据库时，都会遇到错误。这是不可避免的。这就是为什么我想向你展示一些常见的错误以及如何优雅地处理它们。

你通过简单更改用户名对 `db_connect.php` 脚本进行修改，导致连接失败。

- 1. 将用户名改为 `buffy`（除非 `buffy` 是一个真实用户！），使连接行如下：

```php
$connection = mysql_connect("localhost", "buffy", "9sj7En4")
or die(mysql_error());
```

- 2. 保存文件，然后打开浏览器访问 `http://127.0.0.1/db_connect.php`。

# 第11章：建立连接并尝试

![](img/be897bd1bfd4dab38767db24da2a794b_206_0.png)

那真是一个糟糕的响应！至少它准确地告诉了哪里出了问题，而且说了好几次：用户 `buffy` 无法连接到 MySQL。你可以通过在 `mysql_connect()` 函数之前放置一个 `@` 来抑制其中一个丑陋警告，并只显示来自 `die()` 函数的消息。试一下。

- 1. 在 `mysql_connect()` 函数前添加 `@`，保持用户名不变：

```php
$connection = @mysql_connect("localhost", "buffy", "9sj7En4") or die(mysql_error());
```

- 2. 保存文件，然后打开浏览器访问 `http://127.0.0.1/db_connection.php`。

![](img/be897bd1bfd4dab38767db24da2a794b_206_1.png)

通过此更改，警告被抑制了，只显示来自 `die()` 函数的消息。这是 `mysql_error()` 函数提供的有意义的错误消息。

如果你能将糟糕的错误和警告减少到最低，当你的数据库在网络服务高峰期变得不可用时，整体用户体验会更加愉快。

## 在服务器上列出数据库

现在你已经成功使用 PHP 连接到 MySQL，是时候熟悉一些内置的 MySQL 相关函数了。在本节中，你将使用以下函数来列出 MySQL 服务器上的所有数据库：

要同时列出数据库中的表，你只需要对 `db_list.php` 脚本进行一些添加。

- `mysql_list_dbs()`——用于列出 MySQL 服务器上的数据库。
- `mysql_num_rows()`——返回结果集中的行数。
- `mysql_tablename()`——从结果提取表或数据库的名称。

脚本的目标是列出本地 MySQL 服务器上的所有数据库。

- 1. 在文本编辑器中打开一个新文件并开始 PHP 代码：

```php
<?
```

- 2. 创建一个变量来存储 `mysql_connect()` 函数的结果。包含 `@` 以抑制警告，以及 `die()` 函数以便在连接失败时结束脚本并显示消息：

```php
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
```

- 3. 创建一个变量来存储 `mysql_list_dbs()` 函数的结果。包含 `@` 以抑制警告，以及 `die()` 函数以便在脚本可以获取列表时结束并显示消息：

```php
$db = @mysql_list_dbs($connection) or die(mysql_error());
```

- 4. 你将循环结果并动态填充一个列表。在循环之外开始该列表：

```php
$db_list = "<ul>";
```

- 5. 启动一个计数器。你需要它来进行循环：

```php
$i = 0;
```

- 6. 开始 `while` 循环。只要 `$i` 的值小于 `$db` 结果中的行数，循环就会继续：

```php
while ($i < mysql_num_rows($db)) {
```

- 7. 一旦你进入 `while` 循环，获取结果中当前行的数据库名：

```php
$db_names[$i] = mysql_tablename($db, $i);
```

> 注意
变量 `$i` 被其值替换，因此在第一次循环中，该行将是：
$db_names[0] = mysql_tablename($db, 0);`
计数从 0 开始而不是 1，所以它反映了结果中的第一行。计数器递增，即行号。

- 8. 将当前数据库名添加到列表中：

```php
$db_list .= "<li>$db_names[$i]</li>";
```

- 9. 在关闭 `while` 循环之前增加计数：

```php
$i++;
```

- 10. 关闭 `while` 循环、列表以及你的 PHP 代码块：

```php
}
$db_list .= "</ul>";
```

- 11. 添加这些 HTML：

```html
<HTML>
<HEAD>
<TITLE>MySQL Databases</TITLE>
</HEAD>
<body>
<P><strong>Databases on localhost</strong></P>
```

- 12. 打印消息字符串：

```php
<? echo "$db_list"; ?>
```

- 13. 添加更多 HTML 以使文档有效：

```html
</body>
</HTML>
```

- 14. 将文件保存为 `db_list.php`。整合来看，你的代码应该像这样：

```php
<?
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());

$dbs = @mysql_list_dbs($connection) or die(mysql_error());
$db_list = "<ul>";
$i = 0;

while ($i < mysql_num_rows($dbs)) {
  $db_names[$i] = mysql_tablename($dbs, $i);
  $db_list .= "<li>$db_names[$i]</li>";
  $i++;
}
$db_list .= "</ul>";
?>
<HTML>
<HEAD>
<TITLE>MySQL Databases</TITLE>
</HEAD>
<body>
<P><strong>Databases on localhost:</strong></P>
<? echo "$db_list"; ?>
</body>
</HTML>
```

将此文件放在你 Web 服务器的文档根目录下，然后打开浏览器并输入 `http://127.0.0.1/db_list.php`。

# 第11章：建立连接并尝试

![](img/be897bd1bfd4dab38767db24da2a794b_210_0.png)

你的列表可能会有所不同，取决于你在第一章中玩了多少，但你至少应该看到 MySQL 系统数据库 (mysql) 和第一章中创建的数据库 (testDB)。接下来，向此脚本添加另一个循环来打印每个数据库中的表。

## 在数据库中列出表

对 `db_list.php` 脚本进行一些添加就足够列出数据库中的表了。你看到的唯一新函数是 `mysql_list_tables()`，它用于列出 MySQL 数据库中的表。


`mysql_list_tables()` 函数唯一的参数是当前数据库的名称。

- 10. 你将遍历一个结果并动态填充一个项目符号列表。在循环之外开始该符号列表：

```php
$table_list = "<ul>";
```

- 11. 启动一个计数器。你将在第二个循环中需要它：

```php
$table_num = 0;
```

- 12. 开始一个 `while` 循环。只要 `$table_num` 的值小于 `$tables` 值中的行数，该循环就会继续。

```php
while ($table_num < mysql_num_rows($tables)) {
```

- 13. 一旦进入 `while` 循环，获取在结果的当前行中反映的表名：

```php
$table_names[$table_num] = mysql_tablename($tables, $table_num);
```

- 14. 将当前表名添加到项目符号列表中：

```php
$table_list .= "<li>$table_names[$table_num]";
```

- 15. 在关闭 `while` 循环之前增加你的计数器：

```php
$table_num++;
```

- 16. 关闭内部 `while` 循环和表的项目符号列表：

```php
}
$table_list .= "</ul>";
```

- 17. 将 `$table_list` 的值添加到 `$db_list`，并在关闭外部 `while` 循环之前增加你的计数器：

```php
$db_list = "$table_list";
$db_num++;
```

- 18. 关闭数据库的项目符号列表，然后结束你的 PHP 块：

```php
$db_list .= "</ul>\n?>
```

- 19. 添加此 HTML：

```html
<HTML>
<HEAD>
<TITLE>MySQL Tables</TITLE>
</HEAD>
<BODY>
<p><strong>Databases and tables on localhost</strong></p>
```

- 20. 打印消息字符串：

```php
<?php echo "$db_list"; ?>
```

- 21. 添加一些 HTML 以使文档有效：

```html
</BODY>
</HTML>
```

- 22. 以 `db_listtables.php` 的名称保存文件。

你的代码看起来像这样：

```php
<?php
//connection code
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());

//get database list
$dbs = @mysql_list_dbs($connection) or die(mysql_error());

//start first bullet list
$db_list = "<ul>";
$db_num = 0;

//loop through results of function
while ($db_num < mysql_num_rows($dbs)) {
    //get database names and make each bullet point
    $db_names[$db_num] = mysql_tablename($dbs, $db_num);
    $db_list = "<li>$db_names[$db_num];";

    // get table names and start another bullet list
    $tables = @mysql_list_tables($db_names[$db_num]) or die(mysql_error());
    $db_list = "<ul>";
    $table_num = 0;

    // loop through results of function
    while ($table_num < mysql_num_rows($tables)) {
        // get table names and make each a bullet point
        $table_names[$table_num] = mysql_tablename($tables, $table_num);
        $db_list .= "<li>$table_names[$table_num]";
        $table_num++;
    }

    // close inner bullet list and increment number to continue list
    $db_list .= "</li>";
    $db_list = "$table_list";
    $db_num++;
}
// close outer bullet list
$db_list = "</ul>";
?>
<HTML>
<HEAD>
<TITLE>MySQL Tables</TITLE>
</HEAD>
<body>
<p><strong>Databases and tables on localhost</strong></p>
<?php echo "$db_list"; ?>
</body>
</HTML>
```

现在是看看此脚本是否列出了你服务器上的数据库（包括它们的表）了。将此文件放在你的 Web 服务器的文档根目录下，并打开浏览器访问 http://127.0.0.1/db_listtables.php。

由于所有表的所有权限都已授予测试用户，你将看到所有表和数据库的列表，包括系统保留的那些。根据你的服务器设置以及数据库和表的情况，结果可能会有所不同。

在下一节中，你将尝试在服务器上创建新数据库。

# 创建新数据库

在下一个脚本中，找不到上一个脚本中的那些复杂元素。此脚本的目标是在 MySQL 服务器上创建一个新数据库。

- 1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：

```php
<?php
```

- 2. 创建一个变量来存放执行的查询，该查询将创建新数据库：

```php
$sql = "CREATE database testDB2";
```

- 3. 如你一直所的那样添加连接信息：

```php
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
```

- 4. 使用 `mysql_query` 函数执行查询。使用 `@` 抑制警告，如果失败则输出错误：

```php
@mysql_query($sql) or die(mysql_error());
```

- 5. 检查 `$result` 的值。如果真，说明创建了数据库：

```php
if ($result) {
    $msg = "<p>Database created!</p>";
}
```

- 6. 关闭你的 PHP 块并添加 HTML：

```html
<HTML>
<HEAD>
<TITLE>Creating a Database</TITLE>
</HEAD>
<BODY>
```

- 7. 打印消息：

```php
<?php echo "$msg"; ?>
```

- 8. 添加一些 HTML 以使文档有效：

```html
</BODY>
</HTML>
```

- 9. 以 `create_db.php` 的名称保存文件。

- 10. 打开你的浏览器访问 http://127.0.0.1/create_db.php。

如果创建成功，你将看到“Database created!”。




## 规划你的数据表 201

| 数据类型 | 定义 |
|---|---|
| MEDIUMINT | 中型整数，可以是有符号或无符号的。如果有符号的，允许范围为 -8,388,608 到 8,388,607。如果是无符号的，允许范围为 0 到 16,777,215。 |
| INT | 普通尺寸整数，可以是有符号或无符号的。如果有符号的，允许范围为 - 2,147,483,648 到 2,147,483,647。如果是无符号的，允许范围为 0 到 4,294,967,295。 |
| BIGINT | 大整数整数，可以是有符号或无符号的。如果有符号的，允许范围为 - 9,223,372,036,854,775,808 到 9,223,372,036,854,775,807。如果是无符号的，允许范围为 0 到 18,446,744,073,709,551,615。 |
| FLOAT | 浮点数，不能是无符号的。你可以定义显示长度 (M) 和小数位数 (D)。这并不是强制要求的，默认值为 10,2，其中 2 是小数位数。FLOAT 的小数精度可以达到 24 位。 |
| DATE | YYYY-MM-DD 格式的日期，范围在 1000-01-01 到 9999-12-31 之间。例如，1973年12月30日将被存储为 1973-12-30。 |
| DATETIME | YYYY-MM-DD 格式的日期，范围在 1000-01-01 到 9999-12-31 之间，并带有 HH:MM:SS 格式的小时和分钟信息。例如，1973年12月30日凌晨12点将被存储为 1973-12-30 00:01:00。 |
| TIMESTAMP | 1970年1月1日午夜到2037年间某个时间之间的时间戳。你可以为 TIMESTAMP 字段定义多个长度，这直接对应于存储的内容。TIMESTAMP 的默认长度为 14，存储格式为 YYYYMMDDHHMMSS。这看起来像 DATETIME 格式，但数字之间没有连字符；1973年12月30日下午 3:30 将被存储为 19731230153000。TIMESTAMP 的其他定义还有 12 (YYYYMMDDHHMMSS), 8 (YYYYMMDD) 和 6 (YYYYMMDD)。 |
| CHAR | 长度在 1 到 255 个字符之间的固定长度字符串，存储时会在右侧用空格填充到指定长度。不需要定义长度，但默认值为 1。 |
| VARCHAR | 长度在 1 到 255 个字符之间的变长字符串。在创建 VARCHAR 字段时，你必须定义长度。 |
| BLOB 或 TEXT | 最大长度为 65535 字节的字段。BLOB 是“二进制大对象”，用于存储大量二进制数据，如图像或其他类型的文件。定义为 TEXT 的字段也存储大量数据；区别在于，对 BLOB 存储数据的文本排序和比较是区分大小写的，而对 TEXT 字段则是不区分大小写的。你不需要为 BLOB 或 TEXT 指定长度。 |

## 第 12 章：创建数据库表

| 数据类型 | 定义 |
| --- | --- |
| ENUM | 枚举类型（列表）。在定义 ENUM 时，你正在创建一个项目列表，必须从该列表中选择值（或者可以是 NULL）。例如，如果你想让你的字段包含 "A" 或 "B" 或 "C"，你将把枚举定义为 ENUM ('A', 'B', 'C')，并且只有这些值（或 NULL）可以填充到该字段。ENUM 可以有 65535 个不同的值。 |

## 定义你的字段

本章的总体目标是创建一个表来存储来自你个人音乐收藏的数据。请花点时间考虑你想要知道的内容：显然是标题和艺术家，可能还有唱片公司、获取日期以及你对录制的个人笔记。我考虑了我想为自己的表准备的内容，我决定将其命名为 my_music，如表 12.2 所示。

| 字段名 | 描述 |
| --- | --- |
| id | 为条目创建一个唯一的 ID 号 |
| format | 是 CD、磁带还是 LP？ |
| title | 标题 |
| artist | 艺术家 |
| label | 唱片公司 |
| date_acq | 获取日期 |
| notes | 你对录制的个人笔记 |

*(注：由于提供的原文文本在后续部分出现了大量重复和混乱，根据指令，我已翻译了核心逻辑结构部分)*





3.  开始构建名为 $form_block 的字符串，从表单的 action 和 method 开始。假设方法为 POST，action 为名为 `do_createtable.php` 的脚本。记住转义你的引号！

```php
$form_block = "
<FORM METHOD=\"$_POST\" ACTION=\"do_createtable.php\">
```

## 注意

由于脚本正在动态（on-the-fly）创建下一个内容，请构建一个大的字符串，在复杂的解析完成后，你只需要 `echo` 这个字符串即可。这样，即使发生错误，你也不会被卡在一个只构建了一半且无法显示的的页面上。

4.  给表单添加一个隐藏字段（hidden field）来存储 `$_POST[table_name]` 的值，你将在序列结束时使用它向用户显示已创建了正确的表：

```html
<INPUT TYPE="hidden" NAME="table_name" VALUE="$_POST[table_name]">
```

5.  在 HTML 表格中显示你的表单，以便字段对齐整齐。先从列标题行开始，现在闭合 $form_block 字符串：

```html
<TABLE CELLSPACING=5 CELLPADDING=5>
<TR>
<TH>FIELD NAME</TH><TH>FIELD TYPE</TH><TH>FIELD LENGTH</TH></TR>
```

6.  启动一个 `for` 循环来处理表单字段的创建。与 `while` 循环不同，`for` 循环只要条件真就会一直持续。在这种情况下，`for` 循环从变量 `$i` 值为 0 开始，只要 `$i` 小于 `$_POST[num_fields]` 的值就会持续下去。每次循环后，$i 递增 1：

```php
($i = 0; $i < $_POST[num_fields]; $i++) {
```

7.  在 `for` 循环内部，你向原始的 $form_block 中添加内容。对于你想要在数据库表中的每个字段，再添加一行。从表行标签和包含包含字段名输入类型的表格数据单元格（cell）开始：

```php
$form_block .= "
<TR>
<TD ALIGN=CENTER><INPUT TYPE="text" NAME="field_name[]" SIZE="30"></TD>
```

## 注意

在输入字段中 `field_name` 之后使用括号（`[]`）表示数组。对于你在这个表单中定义的每个字段，你将向 `$_POST[field_name]` 数组添加一个值。
数组在带编号的槽位中存储许多变量，从 0 开始。随着数组的增长，会自动添加槽位。例如，如果你正在创建一个有六字段的数据库表，`$_POST[field_name]` 数组将由六个字段变量组成：`$_POST[field_name][0]`、`$_POST[field_name][2]`、`$_POST[field_name][3]`、`$_POST[field_name][4]` 和 `$_POST[field_name][5]`。

8.  在下一个表格数据单元格中，创建一个包含常见字段类型的下拉列表：

```html
<TD ALIGN=CENTER>
<SELECT NAME="field_type[]">
<OPTION VALUE="char">char</OPTION>
<OPTION VALUE="date">date</OPTION>
<OPTION VALUE="float">float</OPTION>
<OPTION VALUE="int">int</OPTION>
<OPTION VALUE="text">text</OPTION>
<OPTION VALUE="varchar">varchar</OPTION>
</SELECT>
</TD>
```

9.  在最后一个表格数据单元格中，为字段长度创建一个文本字段，并闭合你的表行。同时也闭合 $_form_block 字符串，因为你已经完成它了：

```html
<TD ALIGN=CENTER><INPUT TYPE="text" NAME="field_length[]" SIZE="5"></TD>
</TR>
```

10. 闭合 `for` 循环：

```
}

# 第 12 章：创建数据库表

11. 将最后一段 HTML 添加到 $form_block 字符串中。你将添加一个包含提交按钮的行，然后闭合你的表格和表单：

```php
$form_block .= "
<TR>
<TD ALIGN=CENTER COLSPAN=3><INPUT TYPE="submit" VALUE="Create Table"></TD>
</TR>
</TABLE>
</FORM>";
```

12. 闭合 PHP 块并输入以下 HTML：

```html
?>
<HTML>
<HEAD>
<TITLE>Create a Database Table: Step 2</TITLE>
</HEAD>
<BODY>
```

13. 添加一个漂亮的标题，让用户知道他们正在查看什么。混合 HTML 和 PHP 以包含 `$_POST[table_name]` 变量的值：

```html
<H1>Define fields for <?php echo "$_POST[table_name]"; ?></H1>
```

14. 显示 $form_block 的内容：

```php
<?php echo "$form_block"; ?>
```

15. 添加更多 HTML 以使文档有效：

```html
</BODY>
</HTML>
```

16. 以 `do_showfielddef.php` 的命名保存文件，并将此文件放在你的 Web 服务器的文档根目录下。

你的代码看起来应该这样：

```php
//
验证重要输入
if (!$_POST[table_name]) || (!$_POST[num_fields])) {
header("Location: show_createtable.html");
exit;
}

//开始创建用于显示的表单
$form_block .= "
<FORM METHOD="POST" ACTION="do_createtable.php">
<INPUT TYPE="hidden" NAME="table_name" VALUE="$_POST[table_name]">
<TABLE CELLSPACING=5 CELLPADDING=5>
<TR>
<TH>FIELD NAME</TH><TH>FIELD TYPE</TH><TH>FIELD LENGTH</TH></TR>

//循环处理字段
for ($i = 0; $i < $_POST[num_fields]; $i++) {
// 在循环内添加每个字段的行
$form_block .= "
<TR>
<TD ALIGN=CENTER><INPUT TYPE="text" NAME="field_name[]" SIZE="30"></TD>
<TD ALIGN=CENTER>
<SELECT NAME="field_type[]">
<OPTION VALUE="char">char</OPTION>
<OPTION VALUE="date">date</OPTION>
<OPTION VALUE="float">float</OPTION>
<OPTION VALUE="int">int</OPTION>
<OPTION VALUE="text">text</OPTION>
<OPTION VALUE="varchar">varchar</OPTION>
</SELECT>
</TD>
<TD ALIGN=CENTER><INPUT TYPE="text" NAME="field_length[]" SIZE="5"></TD>
</TR>";
}

// 添加提交按钮并关闭标签
$form_block .= "
<TR>
<TD ALIGN=CENTER COLSPAN=3><INPUT TYPE="submit" VALUE="Create Table"></TD>
</TR>
</TABLE>
</FORM>";

// 输出结果
?>
<HTML>
<HEAD>
<TITLE>Create a Database Table: Step 2</TITLE>
</HEAD>
<BODY>
<H1>Define fields for <?php echo "$_POST[table_name]"; ?></H1>
<?php echo "$form_block"; ?>
</BODY>
</HTML>
```




# 创建建表脚本 213

- 2. 创建一个变量来存储表应该所在的数据库名称：
```php
$db_name = "testDB";
```

- 3. 按你之前执行的那样添加连接信息：
```php
$connection = @mysql_connect("localhost", "spike", "_9sj7En4")
or die(mysql_error());
```

- 4. 创建一个变量来存储 `mysql_select_db()` 函数的结果。包含 `@` 以抑制警告，并使用 `die()` 函数在选择数据库失败时结束脚本并显示消息：
```php
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

> 注意
`mysql_select_db()` 函数需要一个数据库名称和当前连接的标识符。

- 5. 通过将初始语法放在名为 `$sql` 的变量中，开始构建查询：
```php
$sql = "CREATE TABLE $_POST[table_name] (*)";
```

- 6. 创建一个 `for` 循环来创建 SQL 语句的剩余部分。该循环根据 `$_POST[field_name]` 数组中包含的元素数量重复：
```php
for ($i = 0; $i < count($_POST[field_name]); $i++) {
```

> 注意
`count()` 函数统计数组中的元素个数。

- 7. 对于每个新字段，你都需要向 SQL 语句添加字段名和类型：
```php
$sql .= $_POST[field_name][$i]. "." .$_POST[field_type][$i];
```

- 8. 因为某些字段定义有特定长度而另一些没有，因此开始一个 `if...else` 块来处理这一方面。如果存在长度，它必须放在括号内，后面跟着一个逗号以开始下一个字段定义：
```php
if ($_POST[$field_length][$i] != "") {
  $sql .= ",".($_POST[$field_length][$i]).",";
} 
```

- 9. 如果没有长度，只需打印逗号来分隔字段定义。然后关闭 `if...else` 块：
```php
} else {
  $sql .= ",";
}
```

- 10. 关闭循环：
```php
}
```

- 11. 存储在 `$sql` 中的 SQL 语句仍然需要帮助。它的末尾有一个多余的逗号，并且括号必须关闭。使用 `substr()` 函数返回整个字符串，排除最后一个字符：
```php
$sql = substr($sql, 0, -1);
```

> 注意
`substr()` 参数列表中的 `0` 告诉函数从第一个字符开始，而 `-1` 告诉函数停止在倒数第二个字符。

- 12. 关闭括号：
```php
$sql .= ")";
```

- 13. 创建一个变量来存储 `mysql_query()` 函数的结果。包含 `@` 以抑制警告，并使用 `die()` 函数在查询失败时结束脚本并显示消息：
```php
$result = mysql_query($sql,$connection) or die(mysql_error());
```

- 14. 测试 `$result` 的值。如果为 `true`，则表示查询成功，并创建一个变量来存储消息：
```php
if ($result) {
    $msg = "<P>".$_POST[table_name]." has been created!</P>\n";
}
```

- 15. 关闭你的 PHP 块并添加 HTML：
```php
?>
<HTML>
<HEAD>
<TITLE>创建数据库表：第3步</TITLE>
</HEAD>
<BODY>
```

- 16. 添加一个新的标题，让用户知道他们正在查看什么。混合 HTML 和 PHP 以包含 `$_POST[db_name]` 变量的值：
```html
<h1>Adding table to <?php echo "$db_name"; ?>...</h1>
```

- 17. 打印消息字符串：
```php
<?php echo "$msg"; ?>
```

- 18. 添加更多 HTML 使文档有效：
```html
</BODY>
</HTML>
```

- 19. 以 `do_createtable.php` 的命名保存文件，并将此文件放在你的 Web 服务器的文档根目录下。

你的代码看起来像这样：

```php
<?php
//指定你想要使用的数据库
$db_name = "testDB";
//连接到数据库
$connection = mysql_connect("localhost","spike","9sj7En4")
or die(mysql_error());
$db = mysql_select_db($db_name, $connection) or die(mysql_error());
```

```php
//开始创建 SQL 语句
$sql = "CREATE TABLE $_POST[table_name] (";

//为每个新字段继续 SQL 语句
for ($i = 0; $i < count($_POST[field_name]); $i++) {
    $sql .= $_POST[field_name][$i].".".$_POST[field_type][$i];

    if ($_POST[field_length][$i] != "") {
        $sql .= ",".($_POST[field_length][$i]).",";
    } else {
        $sql .= ",";
    }
}
//清理字符串
$sql = substr($sql, 0, -1);
$sql .= ")";

//执行查询
$result = mysql_query($sql,$connection) or die(mysql_error());

//获取消息
if ($result) {
    $msg = "<P>".$_POST[table_name]." has been created!</P>";
}
?>
<HTML>
<HEAD>
<TITLE>Create a Database Table: Step 3</TITLE>
</HEAD>
<BODY>
<h1>Adding table to <?php echo "$db_name"; ?>...</h1>
<?php echo "$msg"; ?>
</HTML>
```



8. 开启一个新的表格行和数据单元格，然后创建一个带有文本标签的艺术家名字输入字段。在输入字段后关闭数据表单单元格：

``````
<TR>
<TD VALIGN=TOP>
<P><STRONG>Artist's First Name</STRONG><BR>
<INPUT TYPE="text" NAME="artist_fn" SIZE=35 MAXLENGTH=100></P>
</TD>
```

9. 在新的表格数据单元格中，创建一个带有文本标签的艺术家姓氏（或团体名称）输入字段。在输入字段后关闭数据单元格和表格行：

```
<TD VALIGN=TOP>
<P><STRONG>Artist's Last Name (or Group Name)</STRONG><BR>
<INPUT TYPE="text" NAME="artist_ln" SIZE=35 MAXLENGTH=100></P>
</TD>
```

10. 开启一个新的表格行和一个跨越两列的表格数据单元格。创建一个带有文本标签的 TEXTAREA 字段，用于存放关于录音的备注：

```
<TR>
<TD VALIGN=TOP COLSPAN=2 ALIGN=CENTER>
<P><STRONG>My Notes:</STRONG><BR>
<TEXTAREA name="my_notes" COL=35 ROWS=5 WRAP=virtual</TEXTAREA></P>
```

11. 添加一个提交按钮，并关闭数据表单元格、表格行以及表格本身：

```
<P><INPUT TYPE="SUBMIT" NAME="submit" VALUE="Add Record"></P>
</TD>
<TR>
</TABLE>
```

12. 关闭你的表单，并添加更多 HTML 以确保文档有效：

```
</FORM>
</BODY>
</HTML>
```

13. 将文件保存为 `show_addrecord.html`，并将此文件放置在 Web 服务器的文档根目录下。

## 创建记录添加脚本

14. 打开网页浏览器并输入 http://127.0.0.1/show_addrecord.html。

在下一节中，你将创建一个脚本，用于获取表单输入、创建 SQL 语句并将记录添加到数据库表中。

![](img/be897bd1bfd4dab38767db24da2a794b_245.png)

## 创建记录添加脚本

你为记录添加创建的脚本比创建的脚本要简单得多！

- 1. 在文本编辑器中打开一个新文件并开始 PHP 块：

```php
<?
```

- 2. 检查 `$_POST[id]`、`$_POST[format]` 和 `$_POST[title]` 是否确实输入了值。如果没有，将用户重回表单并退出脚本：

```php
if (!$_POST[id]) || (!$_POST[format]) || (!$_POST[title])) {
    header("Location: /show_addrecord.html");
    exit;
}
```

## 注意

你可以根据需要设置任意数量（无论多少）的必填字段。

- 3. 创建一个变量来存储该表所在的数据库名称：

```php
$db_name = "testDB";
```

- 4. 创建一个变量来存储你用此脚本填充的表格名称：

```php
$table_name = "my_music";
```

- 5. 按照你一直这样做的那样添加连接信息：

```php
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
```

- 6. 按照你学过的方法选择数据库：

```php
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

- 7. 创建 SQL 语句。第一个括号内的语句给出要填充的字段名称（按顺序），第二个括号内的语句发送实际的字符串：

```php
$sql = "INSERT INTO $table_name
(id, format, title, artist_fn, artist_ln, rec_label,
my_notes, date_acq) VALUES
('$_POST[id]', '$_POST[format]', '$_POST[title]',
'$_POST[artist_fn]', '$_POST[artist_ln]', '$_POST[rec_label]',
'$_POST[my_notes]', '$_POST[date_acq]')";
```

- 8. 创建一个变量来存储 `mysql_query()` 函数的结果，按照你学过的方法：

```php
$result = @mysql_query($sql, $connection) or die(mysql_error());
```

## 创建记录添加脚本

9. 关闭你的 PHP 块并添加 HTML：

```php
?>
<HTML>
<HEAD>
<TITLE>Add a Record</TITLE>
</HEAD>
<BODY>
```

10. 添加一个新的标题，让用户知道他们正在查看的内容。混合 HTML 和 PHP 以包含 `$table_name` 变量的值：

```html
<h1>Adding a Record to <? echo "$table_name"; ?></h1>
```

11. 接下来，你将重新创建 `show_addrecord.html` 中使用的布局，但它不包含字段。相反，你将混合 HTML 和 PHP 来显示输入的值。开启一个新的表格行和数据单元格，然后显示 ID 的文本标签和值：

```html
<TABLE CELLSPACING=3 CELLPADDING=3>
<TR>
<TD VALIGN=TOP>
<P><STRONG>ID:</STRONG><BR>
<?php echo $_POST[id]; ?></P>
```

12. 显示获取日期的文本标签和值，然后关闭单元格：

```html
<P><STRONG>Date Acquired (YYYY-MM-DD):</STRONG><BR>
<?php echo $_POST[date_acq]; ?></P>
</TD>
```

13. 显示录音格式的文本标签，然后关闭数据单元格和表格行：

```html
<TD VALIGN=TOP>
<P><STRONG>Format:</STRONG><BR>
<?php echo $_POST[format]; ?></P>
</TD>
</TR>
```

# 向表格插入数据

14. 开启一个新的表格行和数据单元格，显示标题的文本标签和值，然后关闭数据单元格：

```html
<TR>
<TD VALIGN=TOP>
<P><STRONG>Title:</STRONG><BR>
<?php echo $_POST[title]; ?></P>
</TD>
```

15. 在一个新的表格数据单元格中，显示记录信息的文本标签和值，然后关闭数据单元格和表格行：

```html
<TD VALIGN=TOP>
<P><STRONG>Record Label:</STRONG><BR>
<?php echo $_POST[rec_label]; ?></P>
</TD>
</TR>
```

16. 开启一个新的表格行和数据单元格，然后创建一个带有文本标签的艺术家名字输入字段。在输入字段后关闭数据单元格：

```html
<TR>
<TD VALIGN=TOP>
<P><STRONG>Artist's First Name:</STRONG><BR>
<?php echo $_POST[fn]; ?></P>
</TD>
```

17. 在一个新的表格数据单元格中，显示艺术家姓氏（或团体名称）的文本标签和值，然后关闭数据单元格和表格行：

```html
<TD VALIGN=TOP>
<P><STRONG>Artist's Last Name (or Group Name):</STRONG><BR>
<?php echo $_POST[ln]; ?></P>
</TD>
</TR>
```

18. 开启一个新的表格行和跨越两列的数据单元格。显示关于录音的文本标签和值：

```html
<TR>
<TD VALIGN=TOP COLSPAN=2 ALIGN=CENTER>
<P><STRONG>My Notes:</STRONG><BR>
<?php echo stripslashes($_POST[my_notes]); ?></P
```

## 注意

`stripslashes()` 函数会移除表单数据中的反斜杠，这在 PHP 中默认开启的。它会在需要的地方转义字符，如单引号和双引号。你可以通过修改 `php.ini` 文件关闭它，但如果保持开启，就少了一个需要担心的问题。

- 19. 添加一个返回原始表单的链接，然后关闭数据单元格、表格行以及表格本身：

```html
<P><a href="show_addrecord.html">Add Another</a></P>
<TD>
</TR>
</TABLE>
```

- 20. 添加更多 HTML 以确保文档有效：

```html
<BODY>
</HTML>
```

- 21. 将文件保存为 `do_addrecord.php`，将其放置在 Web 服务器的文档根目录下。

你的代码看起来应该是这样的：

```php
<?php
// 检查必填字段
if (!$_POST[id]) || (!$_POST[format]) || (!$_POST[title])) {
    header("Location: /show_addrecord.html");
    exit;
}

// 设置数据库和表格名称
$db_name = "testDB";
$table_name = "my_music";

// 连接 MySQL 并选择使用的数据库
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());

```php
// 创建 SQL 语句并执行查询
$sql = "INSERT INTO $table_name
(id, format, title, artist_fn, artist_ln, rec_label,
my_notes, date_acq) VALUES
'$_POST[id]', '$_POST[format]', '$_POST[title]',
'$_POST[artist_fn]', '$_POST[artist_ln]', '$_POST[rec_label]',
'$_POST[my_notes]', '$_POST[date_acq]";

$result = @mysql_query($sql, $connection) or die(mysql_error());
<HTML>
<HEAD>
<TITLE>Add a Record</TITLE>
</HEAD>
<BODY>
<h1>Adding a Record to <? echo "$table_name"; ?></h1>
<TABLE CELLSPACING=3 CELLPADDING=3>
<TR>
<TD VALIGN=TOP>
<p><STRONG>ID:</STRONG><BR>
<?php echo $_POST[id]; ?></p>
<p><STRONG>Date Acquired (YYYY-MM-DD):</STRONG><BR>
<?php echo $_POST[date_acq]; ?></p>
</TD>
<TD VALIGN=TOP>
<p><STRONG>Format:</STRONG><BR>
<?php echo $_POST[format]; ?></p>
</TD>
</TR>
<TR>
<TD VALIGN=TOP>
<p><STRONG>Title:</STRONG><BR>
<?php echo $_POST[title]; ?></p>
</TD>
<TD VALIGN=TOP>
<p><STRONG>Record Label:</STRONG><BR>
<?php echo $_POST[rec_label]; ?></p>
</TD>
</TR>
</TR>
```



```html
<TABLE>
  <tr>
    <TD VALIGN=TOP>
      <P><STRONG>艺术家艺名:</STRONG><BR>
      <?php echo "$_POST[artist_fn]"; ?></P>
    </TD>
    <TD VALIGN=TOP>
      <P><STRONG>艺术家姓氏（或团体名称）：</STRONG><BR>
      <?php echo "$_POST[artist_ln]"; ?></P>
    </TD>
  </tr>
  <tr>
    <TD VALIGN=TOP COLSPAN=2 ALIGN=CENTER>
      <P><STRONG>我的笔记：</STRONG><BR>
      <?php echo stripslashes(\$_POST[my_notes]); ?></P>
      <P><a href="show_addrecord.html">添加另一个</a>a></P>
    </TD>
  </tr>
</TABLE>
</body>
</html>
```

继续下一步，你将点击按钮并添加记录。

# 填充你的表格

现在有趣的事情开始了！如果你在完成本章的第一部分后没有关闭网络浏览器，`show_addrecord.html` 应该在你的浏览器窗口中仍然可见。如果没有，请现在打开 http://127.0.0.1/show_addrecord.html。

为你手头有的某张专辑完成添加表单。下图展示了我收藏中的一个示例。

# 230 第 13 章：向表格插入数据

![](img/be897bd1bfd4dab38767db24da2a794b_252_0.png)

点击“添加记录”（Add Record）按钮，你应该看到如下图所示确认屏幕。

![](img/be897bd1bfd4dab38767db24da2a794b_252_1.png)

向数据库表添加几条你自己的录音。除非你自己修改了脚本，否则必填字段只有 ID、format 和 title。

> 注意
> 在随后的章节中，你将学习如何对表格进行修改，使 ID 字段保持唯一性并自动递增。这样你就不需要不断输入数字并寄希望它有效了。

# 14 选择和显示数据

到目前为止，你已经愉快且反复地用你音乐收藏中的所有项目填充了 my_music 表——至少是几项。在本章中，你将学习如何：

- 使用 SQL ORDER BY 子句从表中选择记录
- 格式化并显示数据库表中的记录

# 和创建你的管理菜单

你可以写一个脚本说：“选择我所有的数据；我不在乎顺序”，但那样会很无聊。在本章中，你将看到从 my_music 表选择记录的四种方法。为了方便导航，创建一个管理菜单——这是“脚本链接列表”的雅说法。

- 1. 在你的文本编辑器中打开新文件并输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>我的菜单</TITLE>
</HEAD>
<BODY>
<h1>我的菜单</h1>
<P><strong>我的音乐</strong></P>
```

- 2. 开始编写一个项目符号列表，并创建指向名为 `sel_byid.php` 脚本的第一个链接。该脚本将按 ID 数字排序显示记录：

```html
<ul>
<li><a href="sel_byid.php">按 ID 排序</a></li>
</ul>
```

- 3. 添加一个指向 `sel_bydateq.php` 脚本的链接。该脚本将按获取日期显示记录。最近获取的项目将列在前：

```html
<ul>
<li><a href="sel_bydateq.php">按获取日期排序（最新优先）</a></li>
</ul>
```

- 4. 添加一个指向 `sel_bytitle.php` 脚本的链接。该脚本将按标题显示记录：

```html
<ul>
<li><a href="sel_bytitle.php">按标题排序</a></li>
</ul>
```

- 5. 添加一个指向 `sel_byartist.php` 脚本的链接。该脚本将按艺术家显示记录：

```html
<ul>
<li><a href="sel_byartist.php">按艺术家排序</a></li>
</ul>
```

# 从 MY_MUSIC 表提取数据 233

6. 关闭列表，然后添加一些 HTML 使文档有效：

```html
<ul>
<BODY>
</html>
```

7. 将文件保存为 `my_menu.html`，并将其放置在你 Web 服务器的根目录下。

8. 打开浏览器并输入 http://127.0.0.1/my_menu.html。

在接下来的章节中，你将创建上述提取数据的脚本。

![](img/be897bd1bfd4dab38767db24da2a794b_255_0.png)

# 从 my_music 表选择数据

接下来的四个部分包含显示数据的变体：大部分脚本完全相同，但新函数是 `mysql_fetch_array()`。该函数获取 SQL 查询的结果并将行放入数组中。使用简单的 `while` 循环，你可以提取并显示这些元素。

# 按 ID 排序显示记录

记录添加所需的字段之一是 ID。在脚本中，你将按 ID 数字选择 my_music 表中的所有记录。`ORDER BY` 子句的默认值是 ASC（升序），因此记录按 ID #1 返回，然后是 #2、#3 等此类推。

- 1. 在文本编辑器中打开新文件并开始 PHP 块：

```php
<?php
```

- 2. 创建一个变量来存储数据库的名称：

```php
$db_name = "testDB";
```

- 3. 创建一个变量来存储你从中选择的表格名称：

```php
$table_name = "my_music";
```

- 4. 添加连接信息：

```php
<?php
```

- 5. 按你学的那样创建连接：

```php
$connection = mysqli_connect("localhost", "username", "", $db_name);
```

- 6. 创建 SQL 语句：

```php
$sql = "SELECT id, format, title, artist_fn, artist_ln, rec_label, my_notes, date_acq FROM $table_name ORDER BY id";
```

- 7. 执行查询：

```php
$result = mysqli_query($connection, $sql);
```

- 8. 开启 while 循环：

```php
while ($row = mysqli_fetch_array($result)) {
```

- 9. 获取单个元素：

```php
$id = $row['id'];
$format = $row['format'];
$title = $row['title'];
$artist_fn = $row['artist_fn'];
$artist_ln = $row['artist_ln'];
$rec_label = $row['rec_label'];
$my_notes = $row['my_notes'];
$date_acq = $row['date_acq'];
```

- 10. 对艺术家名字进行一点格式化：

```php
if ($artist_fn != "") {
```

- 11. 创建变量 `$artist_fullname`：

```php
$artist_fullname = trim($artist_fn . " " . $artist_ln);
```

- 12. 继续块：

```php
} else {
  $artist_fullname = trim($artist_ln);
}
```

- 13. 进行更详细的格式化：

```php
if ($date_acq == "0000-00-00") {
  $date_acq = "[unknown]";
}
```

- 14. 创建变量 `$display_block`：

```php
$display_block = "<P><strong>$title</strong> on $rec_label, by $artist_fullname<br>
$my_notes <em>(acquired:$date_acq, format:$format)</em></P>";
```

- 15. 关闭 while 循环：

```php
}
```

- 16. 添加此 HTML：

```html
<HTML>
<HEAD>
<TITLE>我的音乐（按 ID 排序）</TITLE>
</HEAD>
<body>
<h1>我的音乐：按 ID 排序</h1>
<?php echo $display_block; ?>
</body>
</HTML>
```





# 从 MY_MUSIC 表中选择数据 237

- 17. 显示结果：

```php
<? echo "$display_block"; ?>
```

- 18. 添加一个指向主菜单的链接，然后添加更多 HTML 以构建有效的文档：

```html
<P><a href="my_menu.html">返回菜单</a>a></P>
</BODY>
</HTML>
```

- 19. 将文件保存为 sel_byid.php，并将此文件放在 Web 服务器的文档根目录下。

- 20. 打开网页浏览器并输入 http://127.0.0.1/my_menu.html。

- 21. 点击按 ID 排序的链接。

你的记录将与我的不同，但你应该能看到类似下面的屏幕，记录按内部 ID 数字进行排序。

![](img/be897bd1bfd4dab38767db24da2a794b_259_0.png)

在下一节中，你将创建一个按获取日期排序结果的脚本。

# 显示按获取日期排序的记录

虽然这不是必填字段，但添加记录的脚本有一个空间用于记录录音进入音乐收藏的日期。在这个脚本中，你将选择 my_music 表中的所有记录，并按此日期排序，最近获取的记录出现在列表顶部。

- 1. 打开 sel_byID.php 文件并将 SQL 语句更改为：

```php
$sql = "SELECT * FROM $table_name ORDER BY date_acq DESC;
```

- 2. 修改 HTML 标题和标题以反映新的排序方法：

```html
<HTML>
<HEAD>
<TITLE>我的音乐（按获取日期排序）</TITLE>
</HEAD>
<body
<h1>我的音乐：按获取日期排序</h1>
```

- 3. 将文件保存为 sel_bydateac.php，并将此文件放在 Web 服务器的文档根目录下。

- 4. 打开网页浏览器并输入 http://127.0.0.1/my_menu.html。

- 5. 点击按获取日期排序的链接。

你的记录将与我的不同，但你应该能看到类似下面的屏幕，记录按获取录音的日期排序。没有日期的记录将出现在列表末尾。

# 从 MY_MUSIC 表中选择数据 239

![](img/be897bd1bfd4dab38767db24da2a794b_261_0.png)

在下一节中，你将创建一个按标题排序结果的脚本。

# 我的音乐：按获取日期排序

Speakerxxxxx/The Love Below on Face, by OutKast
很棒的 - Hey Yal (获取于 2003-12-25，格式 CD)

**The Last Broadcast** 出自 Capitol Records，来自 doves
另一张非常适合听所有作品的 CD。(获取于 2002-11-21，格式 CD)

**White Lader** 出自 ICA，来自 David Gray
非常适合工作时听的背景音乐。(获取于 2002-05-01，格式 CD)

**Blowback** 出自 Hollywood Records，来自 Tricky
我真诡异。他在《第五元素》中表现也很好。(获取于 2001-03-01，格式 CD)

**America** 出自 Daemon Records，来自 The Oblivious
我没丢这个 - 它已经绝版了！(获取：1993-11-01，格式 CD)

# 显示按标题排序的记录

正如你所想象的，录音标题是添加记录脚本中的必填字段。在这个脚本中，你将按字母顺序选择 my_music 表中的所有记录。

- 1. 打开 sel_bydateacq.php 文件并将 SQL 语句更改为：

```php
$sql = "SELECT * FROM $table_name ORDER BY title";
```

- 2. 修改 HTML 标题和级标题以反映新的排序方法：

```html
<HTML>
<HEAD>
<TITLE>我的音乐（按标题排序）</TITLE>
</HEAD>
<body
<h1>我的音乐：按标题排序</h1>
```

- 3. 显示结果：

```php
<? echo "\display_block"; ?>
```

- 4. 添加一个返回主菜单的链接，然后添加更多 HTML 以构建有效的文档：

```html
<P><a href="my_menu.html">返回菜单</a>a></P>
</body
</HTML>
```

- 5. 将文件保存为 sel_title.php，并将此文件放在 Web 服务器的根目录下。

- 6. 打开网页浏览器并输入 http://127.0.0.1/my_menu.html。

- 7. 点击按标题排序的链接。

你的记录将与我的不同，但你应该能看到类似下面的屏幕，记录按录音标题排序。

![](img/be897bd1bfd4dab38767db24da2a794b_262_0.png)

在最后部分，你创建一个按艺术家显示结果的脚本。

# 按艺术家排序的记录

这个脚本有点复杂，因为你必须考虑艺术家：有些只有名字，有些有姓，并且都包含 artist 字段。在这个脚本中，你按艺术家全名的字母顺序选择 my_music 表中的所有记录。

- 1. 在文本编辑器中打开新文件并开始 PHP 块：

- 2. 创建一个变量来存储数据库名：

```php
$db_name = "test";
```

- 3. 创建一个变量来存储表名：

```php
$table_name = "my_music";
```

- 4. 添加连接信息：

```php
$connection = @mysql_connect("localhost", "my_music") or die(mysql_error());
```

- 5. 如你所学，选择数据库：

```php
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

- 6. 创建 SQL 语句。返回 SELECT 语句中的所有字段：

```sql
$sql = "SELECT id, format, title, concat(artist_first, ' ', artist_last) as artist_fullname, rec_label, my_notes, date_acq FROM $table_name ORDER BY artist_fullname";
```

# 第十四章：选择与显示数据

在这个 SQL 语句中，你本质上是从两个字段创建一个新字段，使用 `concat()` 函数将 artist_first 和 artist_last 结合。使用 artist_fullname 将此新值分配给 artist 字段。例如你的 David Gray 专辑。艺术家的名字（"David"）和姓（"Gray"）会进入各自的区域，但将输出为一个字符串（"David Gray"）。`stripslashes()` 函数仍然会空格。

- 7. 如你所学，创建一个一个变量来存储 `mysql_query()` 函数的结果：

```php
$result = @mysql_query($sql,$connection) or die(mysql_error());
```

- 8. 开始循环。while 循环将为集合中的每个记录创建一个数组 $row：

```php
while ($row = mysql_fetch_array($result)) {
```

- 9. 获取记录的各个元素和名字。记住，你有一个名为 artist_fullname 的新字段。对任何可能添加了斜杠的字段添加 `stripslashes()` 函数：

```php
$id = $row['id'];
$format = $row['format'];
$title = stripslashes($row['title']);
$artist_fullname = stripslashes($row['artist_fullname']);
$rec_label = stripslashes($row['rec_label']);
$my_notes = stripslashes($row['my_notes']);
$date_acq = $row['date_acq'];
```

- 10. 如果没有在 date_acq 字段中输入日期，MySQL 将输入默认值 0000-00-00。为此值创建一个 if 块，然后用更友好的方式替换：

```php
if ($date_acq == "0000-00-00") {
$date_acq = "[unknown]";
}
```

- 11. 创建名为 $display_block 的变量来存储所有格式化的记录。此块中的格式设置将录音标题加粗，随后是括号中的艺术家名字。接下来是换行符，然后是你的备注，以及包含获取日期和格式的强调括号语句：

```php
$display_block .= "
<P><strong>title:</strong> ($artist_fullname)<br>
$my_notes <em>(acquired: $date_acq, format: $format)</em></P>";
```

- 12. 关闭 while 循环，然后是你的 PHP 块：

```php
}
?>
```

- 13. 添加此 HTML：

```html
<HTML>
<HEAD>
<TITLE>我的音乐（按艺术家排序）</TITLE>
</HEAD>
<body
<h1>我的音乐：按艺术家排序</h1>
</body>
```

- 14. 显示结果：

```php
<? echo "$display_block"; ?>
```

- 15. 添加一个返回主菜单的链接，并添加更多 HTML 以构建有效的文档：

```html
<P><a href="my_menu.html">返回菜单</a>a></P>
</body>
</HTML>
```

- 16. 将文件保存为 sel_byartist.php，并将此文件放在 Web 服务器的根目录下。

- 17. 打开网页浏览器并输入 http://127.0.0.1/my_menu.html。

- 18. 点击按艺术家排序的链接。

你的记录将与我的不同，但你应该能看到类似下面的屏幕，记录按艺术家的名字排序。




## 244 第 14 章：数据的选择与显示

接下来的章节将让你从数据库工作中解脱，你将学习一些关于用户身份验证、Cookies 和 Session 的知识。

![](img/be897bd1bfd4dab38767db24da2a794b_266_0.png)

## 用户身份验证与跟踪

- 第 15 章 数据库驱动的用户身份验证 ..................... 247
- 第 16 章 使用 Cookies ................................................... 263
- 第 17 章 Session 基础 ................................................ 277

本页留空

## 15 数据库驱动的用户身份验证

每个人都有自己不想向所有人分享的秘密。但某些秘密是可以分享的——与特定的人士分享。在本章中，你将学习如何：

- 为授权用户创建一个数据库表
- 创建一个登录表单和脚本序列，在显示任何秘密之前对用户进行身份验证

## 为什么要对任何人进行验证？

在最初开发网站时，你可能想限制开发团队某些成员的访问。如果你的公司网站包含敏感的财务数据，你可能想将财务报表限制在特定的投资者列表中。或者，你只是不想让别人窥探你的隐私。

一种常见的用户身份验证类型是数据库驱动的，将用户名和密码存储在数据库表中，并通过登录表单和脚本访问。在下一节中，你将创建此数据库表并向其中添加用户。

## 创建用户表

在第 12 章“创建数据库表”中，你遵循了一个两个步骤的表创建过程。你可以使用相同的流程来创建授权用户表。

1. 打开你的网络浏览器访问 http://127.0.0.1/show_createtable.html。
2. 在“表名”（Table Name）字段中，输入 `auth_users`。
3. 在“字段数量”（Number of Fields）字段中，输入 `4`。
4. 点击“前往第二步”（Go to Step 2）按钮。你应该看到一个有四行的表单，对应于 auth_users 表的四个个字段。
5. 在第一行，在“字段名”（Field Name）处输入 `f_name`，从“字段类型”（Field Type）下拉菜单中选择 `varchar`，并指定“字段长度”（Field Length）为 `50`。该字段将存储用户名。
6. 在第二行，在“字段名”处输入 `l_name`，从“字段类型”下拉菜单中选择 `varchar`，并指定“字段长度”为 `50`。该字段将存储用户的姓。
7. 在第三行，在“字段名”处输入 `username`，从“字段类型”下拉菜单中选择 `varchar`，并指定“字段长度”为 `25`。该字段将存储用户的用户名。
8. 在第四行，在“字段名”处输入 **password**，从“字段类型”下拉菜单中选择 **varchar**，并指定“字段长度”为 **100**。该字段将存储密码的哈希值。

## 注意事项

如果你还记得第 7 章“显示动态内容”，**哈希值（hash）**就像是字符串的数字摘要。它被用于比较字符串（或文件）的版本，以确定版本之间是否存在差异。

完成后的表单看起来应该如下所示。

![](img/be897bd1bfd4dab38767db24da2a794b_271_0.png)

点击“创建表”（Create Table）按钮。你将看到一个确认屏幕，说明你的表已创建。在下一节中，你将创建一个记录添加表单和脚本，并将用户添加到 **auth_users** 表。

## 向你的表添加用户

空的 **auth_users** 表没有任何用。在本节中，你将创建一个简单的记录添加表单和脚本，类似于你在第 13 章“向表中插入数据”中创建的内容。

## 创建用户添加表单和脚本

HTML 表单将包含 auth_users 表中每一列的输入字段。

1. 在你的编辑器中打开一个新文件并输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>Add a User</TITLE>
</HEAD>
<BODY>
<h1>Adding a Record to auth_users</h1>h1
```

2. 开始你的表单。假设方法为 POST，动作是一个名为 `do_adduser.php` 的脚本：

```html
<FORM METHOD="POST" ACTION="do_adduser.php">
```

3. 为用户的第一个名字创建一个带文本标签的输入字段：
`<P><STRONG>First Name:</STRONG><BR><INPUT TYPE="text" NAME="f_name" SIZE=25 MAXLENGTH=50</p>`

4. 为用户的姓氏创建一个带文本标签的输入字段：
`<P><STRONG>Last Name:</STRONG><BR><INPUT TYPE="text" NAME="l_name" SIZE=25 MAXLENGTH=50</p>`

5. 为用户名创建一个带文本标签的输入字段：
`<P><STRONG>Username:</STRONG><BR><INPUT TYPE="text" NAME="username" SIZE=25 MAXLENGTH=25</p>`

6. 为密码创建一个带文本标签的输入字段：
`<P><STRONG>Password:</STRONG><BR><INPUT TYPE="text" NAME="password" SIZE=25 MAXLENGTH=50</p>`

## 向你的表添加用户

## 注意事项

`PASSWORD()` 函数插入的是密码的哈希值，而不是密码本身。这缓解了在数据库中存有明文密码的安全风险，因为脚本只需要匹配两个哈希值。


```php
if (!$_POST['f_name']) || (!$_POST['l_name']) || (!$_POST['username'])) {
  header("Location: show_adduser.html");
  exit;
}
//set up the names of the database and table
$db_name = "testDB";
$table_name = "auth_users";

//connect to the server and select the database
$connection = mysql_connect("localhost", "spike", "9j7En4")
or die(mysql_error());
$db = mysql_select_db($db_name, $connection) or die(mysql_error());

//create and issue query
$sql = "INSERT INTO $table_name (f_name, l_name, username, password) 
VALUES ('$_POST[f_name]', '$_POST[l_name]', '$_POST[username]', '$_POST[password]')";
$result = @mysql_query($sql,$connection) or die(mysql_error());

<HTML>
<HEAD>
<TITLE>Add a User</TITLE>
</HEAD>
<body>
<h1>Added to auth_users:</h1><BR>
<p><STRONG>First Name:</STRONG><BR>
<?php echo $_POST['f_name']; ?></p>

<p><STRONG>Last Name:</STRONG><BR>
<?php echo $_POST['l_name']; ?></p>
<p><STRONG>Username:</STRONG><BR>
<?php echo $_POST['username']; ?></p>

<p><STRONG>Password:</STRONG><BR>
<?php echo $_POST['password']; ?></p>
<a href="show_adduser.html">Add Another</a></p>
</body>
</HTML>
```

接下来通过向你的表中添加一些示例用户来测试此代码。

## 添加一些用户

接下来的示例基于我服务器上的虚构用户。你的结果将取决于你在表中输入的内容。若要进入用户添加表单，请打开网页浏览器并输入 http://127.0.0.1/show_adduser.html。

在我的用户添加表单中，我输入了一个名为 Joe Webby 的用户的信息，用户名是 joe，密码是 likecheese。完成后的表单如下图所示。

![](img/be897bd1bfd4dab38767db24da2a794b_277_0.png)

点击“Add User”按钮后，显示了确认屏幕，如下图所示。

# 第 15 章：数据库驱动的用户认证

![](img/be897bd1bfd4dab38767db24da2a794b_278_0.png)

要查看密码哈希如何存储的示例，请使用命令行界面 MySQL Monitor 来查看你的记录。你会发现密码条目 127493710101bb5a，而不是 ilikecheese。

![](img/be897bd1bfd4dab38767db24da2a794b_278_1.png)

继续自己添加一些用户，直到你拥有一组漂亮的用户。

## 创建登录表单

HTML 表单将包含两个字段：用户名和密码。这两者都是必填的。

- 1. 在你的文本编辑器中打开一个新文件并输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>Login</TITLE>
</HEAD>
<BODY
<h1>Login to Secret Area</h1>
```

- 2. 开始你的表单。假设方法为 POST，动作是一个名为 do_autouser.php 的脚本：

```html
<FORM METHOD="POST" ACTION="do_autouser.php">
```

- 3. 为用户名创建一个带有文本标签的输入字段：

```html
<P><strong>Username:</strong></strong><BR>
<INPUT TYPE="text" NAME="username" SIZE=25 MAXLENGTH=25></p>
```

- 4. 为密码创建一个带有文本标签的输入字段。

```html
<P><strong>Password:</strong></strong><BR>
<INPUT TYPE="password" NAME="password" SIZE=25 MAXLENGTH=25></p>
```

- 5. 添加一个提交按钮，关闭你的表单并添加更多 HTML 以使文档格式有效：

```html
<P><INPUT TYPE="SUBMIT" NAME="submit" VALUE="Login"/></P>
</FORM>
<BODY
</HTML>
```

- 6. 将文件保存为 show_login.html，并将此文件放在你的 Web 服务器的文档根目录下。

- 7. 打开网页浏览器并输入 http://127.0.0.1/show_login.html。

# 第 15 章：数据库驱动的用户认证

你将看到登录表单，带有用户名和密码的文本字段以及一个提交按钮。

![](img/be897bd1bfd4dab38767db24da2a794b_280_0.png)

接下来，你为登录表单创建后端脚本。

# 创建认证脚本

此脚本的目标是将表单中输入的用户名和密码与 auth_users 表中（同一记录内）的用户名和密码进行匹配。

- 1. 在你的文本编辑器中打开一个新文件并启动 PHP 块：

```php
<?php
```

- 2. 检查是否实际输入了两个值。如果没有，则将用户重定向回表单：

```php
if (!$_POST['username']) || (!$_POST['password'])) {
    header("Location: show_login.html");
    exit;
}
```

- 3. 创建一个变量存储数据库名称：

```php
$db_name = "testDB";
```

- 4. 创建一个变量存储由此脚本填充的表名：

```php
$table_name = "auth_users";
```

- 5. 如你学习的那样添加连接信息：

```php
$connection = mysql_connect("localhost", "spike", "9j7En4")
or die(mysql_error());
```

- 6. 如你学习的那样选择数据库：

```php
$db = mysql_select_db($db_name, $connection) or die(mysql_error());
```

- 7. 创建 SQL 语句。该语句查找表中用户名与表单输入的用户名、且密码哈希与表单输入的密码哈希匹配的记录：

```php
$sql = "SELECT * FROM $table_name WHERE username = '$_POST[username]'
AND password = '$_POST[password]'";
```

- 8. 如你学习的那样，创建一个变量存储 mysql_query() 函数的结果：

```php
$result = @mysql_query($sql,$connection) or die(mysql_error());
```

- 9. 通过计算结果集的行数检查查询结果：

```php
$num = mysql_num_rows($result);
```

- 10. 一个 if-else 块来处理你的结果。如果行数大于0，则找到了匹配项。创建一个变量存储适当的消息：

```php
if ($num != 0) {
    $msg = "<P>Congratulations, you're authorized!</p>";
}
```

- 11. 如果行数为0，未找到匹配项。在这种情况下，将用户重定向回登录表单，然后关闭 if-else 块：

```php
} else {
    header("Location: show_login.html");
    exit;
}
```

- 12. 关闭你的 PHP 块并添加 HTML：

```php
?>
<HTML>
<HEAD>
<TITLE>Secret Area</TITLE>
</HEAD>
<body>
```

- 13. 显示消息：

```php
<?php echo "$msg"; ?>
```

- 14. 添加更多 HTML 以使文档有效：

```html
</body>
</HTML>
```

- 15. 将文件保存为 do_autouser.php，并将此文件放在你的 Web 服务器的文档根目录下。你的代码应该是这样的：

```php
<?php
//检查必填字段
if (!$_POST['username']) || (!$_POST['password'])) {
    header("Location: show_login.html");
    exit;
}

//设置使用的数据库和表
$db_name = "testDB";
$table_name = "auth_users";

//连接服务器并选择数据库
$connection = mysql_connect("localhost", "spike", "9j7En4")
or die(mysql_error());
$db = mysql_select_db($db_name, $connection) or die(mysql_error());

//构建并执行查询
$sql = "SELECT * FROM $table_name WHERE username = '$_POST[username]'
AND password = '$_POST[password]'";

$result = @mysql_query($sql,$connection) or die(mysql_error());

//获取结果集的行数
$num = mysql_num_rows($result);

//根据结果打印消息或重定向到别处
if ($num != 0) {
    $msg = "<P>Congratulations, you're authorized!</p>";
} else {
    header("Location: show_login.html");
    exit();
}
?>
<HTML>
<HEAD>
<TITLE>Secret Area</TITLE>
</HEAD>
<body>
<?php echo "$msg"; ?>
</body>
</HTML>
```

接下来你可以测试登录表单了！

# 尝试自我认证

在本节中，你尝试以添加到 auth_users 表的用户之一身份登录。你的结果将取决于你使用的用户名和密码。若要获取登录表单，请打开网页浏览器并输入 http://127.0.0.1/show_login.html。

我首先尝试通过输入错误的用户名和密码来破坏认证程序。

# 第 15 章：数据库驱动的用户认证

点击“Login”按钮后，我被重定向回登录页面，因为用户名和密码均无效。

![](img/be897bd1bfd4dab38767db24da2a794b_284_0.png)

> 注意
任何错误的用户名和密码的组合都会导致认证失败。

然后我在用户名和密码字段中输入了正确的值，点击“Login”按钮后，我看到了如下图所示的成功消息。

![](img/be897bd1bfd4dab38767db24da2a794b_284_1.png)

在下一章中，你将接触 Cookie，并了解如何将其用于认证方案或仅通用的用户跟踪。




# 16
使用 Cookies

Cookies 是非常棒的小工具，但当坏心的人滥用它们时，它们在媒体中名誉扫地。如果你使用得当，这些小小的文本片段可以让你的开发工作变得简单得多。在本章中，你将学习如何：

- 设置 Cookie
- 从 Cookie 中提取数据
- 修改你的用户身份验证程序以使用 Cookie

## 什么是 Cookie？

Cookies 是发送到用户网络浏览器的文本片段。Cookies 可以帮助你创建购物车、用户社区和个性化网站。不建议在 Cookie 中存储敏感数据，但你可以存储一个唯一标识字符串，该字符串将与安全存储在数据库中的用户数据相匹配。

来看这个购物示例。假设你为一个用户分配了一个标识变量，这样你就可以跟踪他在访问你的网站时所的操作。首先，用户登录，你发送一个带有变量的 Cookie，这些变量旨在说明：“这是 Joe，Joe 被允许留在这里”。当 Joe 在你的网站上闲逛时，你可以在每一个、每一个页面都显示：“你好，Joe！”。如果 Joe 点击了你的目录并选择了 14 件物品购买，你可以跟踪这些物品，并在 Joe 去结算区域时将它们全部组合在一起显示。

## 设置 Cookie

在开始设置 Cookie 之前，确定你将如何使用它们以及在何时何时设置它们。无论你决定设置什么 Cookie，请记住，在向浏览器发送任何其他内容之前，你必须设置 Cookie，因为 Cookie 实际上是头部信息的一部分。

如果你听从了这个警告，你就不用花费几个小时去想为什么会收到“Cannot add header information”（无法添加头部信息）错误。这个示例代码正是如此。

![](img/be897bd1bfd4dab38767db24da2a794b_286_0.png)

它产生了如下图所示的错误。

每当你看到这个错误时，假设你在时间之前已经向网络浏览器发送了内容。这可能包括空格、换行符或你实际上看到的文本。

![](img/be897bd1bfd4dab38767db24da2a794b_287_0.png)

警告：headers already sent in /usr/local/apache2/htdocs/test/badcookie.php（已在 /usr/local/apache2/htdocs/test/badcookie.php 中发送头部）

## 错误的 Cookie

setcookie() 函数用于一次设置一个 Cookie，它接受六参数：

- Name（名称）。存储存储在全局 `$_COOKIE` 中的变量名，并在后续脚本中可以访问。
- Value（值）。传递的名称变量的值。
- Expiration（过期时间）。设置一个特定时间，在该时间后 Cookie 值不再可用。没有设置特定过期时间的 Cookie 在网络浏览器关闭时过期。
- Path（路径）。决定 Cookie 在哪些目录下有效。如果路径参数中是单个斜杠，则 Cookie 对 Web 服务器上的所有文件有效。如果指定了特定目录，则 Cookie 仅对该目录内的页面有效。
- Domain（域名）。Cookie 仅对设置它们的主机和域名有效。如果没有指定域名，默认值是生成 Cookie 的服务器主机名。域名参数字符串中必须至少包含两个点才有效。
- Security（安全）。如果安全参数为 1，则 Cookie 将仅通过 HTTPS 传输，也就是说通过安全的 Web 服务器传输。

接下来的这一行是一个名为 `id`、值为 `5ds808992jjs2` 的 Cookie 示例。这个特定的 Cookie 在四小时后过期（当前时间加 14,000 秒），并且对你 yourdomain.com 上文档根目录下的任何页面有效。

```php
setcookie("id", "5ds808992jjs2", time()+14000, "/*", "yourdomain.com");
```

在下一节中，我将为你提供一个 `time` 常用值的速查表。你将开始使用 Cookie 变量。

## 计数时间

如果你想指定过期日期或时间，简单的方法是告诉 PHP 为你向前计数，然后在 `setcookie()` 函数的过期槽中放置一个值。这个值应该是一个 Unix 整数（自 1970 年 1 月 1 日以来的秒数），你可以使用 `time()` 函数加上额外的秒数来获取。

在你的 Cookie 上设置过期日期可以为用户的有效性提供一些保证。如果你在没有时间限制的情况下设置 Cookie，它将在用户关闭浏览器时自动过期。这在用户共享计算机时非常有用；你不希望下一个用户获得上一个用户通过 Cookie 提供的所有权限。同样，如果你正在构建一个在线商店，允许你在用户访问的前 15 分钟内购买的所有物品获得折扣，你可能想设置一个 15 分钟有效的 Cookie。

表 16.1 显示了 `setcookie()` 函数中 `time()+n` 的一些常见用途。

| 表 16.1 | 常用时间 | 定义 |
|---|---|---|
| time()+60 | 当前时间起 1 分钟 |
| time()+900 | 当前时间起 15 分钟 |
| time()+1800 | 当前时间起 30 分钟 |
| time()+3600 | 当前时间起 1 小时 |
| time()+14400 | 当前时间起 4 小时 |
| time()+43200 | 当前时间起 12 小时 |
| time()+86400 | 当前时间起 24 小时 |
| time()+259200 | 当前时间起 3 天 |
| time()+604800 | 当前时间起一周 |
| time()+2592000 | 当前时间起 30 天 |

## 测试 Cookie

此脚本的目标只是设置一个 Cookie 并打印消息。在开始之前，请确保你没有阻止 Cookie。

1. 在你的文本编辑器中打开一个文件。创建 `cookie_name`、`cookie_value` 和 `cookie_expire` 变量并赋值如下：

```php
$cookie_name = "test";
$cookie_value = "test";
$cookie_expire = "0";
$cookie_domain = "127.0.0.1";
```

2. 使用 `setcookie()` 函数设置：
```php
setcookie($cookie_name, $cookie_value, $cookie_expire, "/*", $cookie_domain);
```

3. 输入以下 HTML：
```html
<HTML>
<HEAD>
<TITLE>Set Cookie</TITLE>
</HEAD>
<BODY>
Mmmmm...cookie!
</BODY>
</HTML>
```

4. 将文件保存为 `setcookie.php`并将其放在文档根目录下。

5. 打开网络浏览器并输入 `http://127.0.0.1/setcookie.php`。你会看到一个提示接受 Cookie 的对话框。实际的对话框与浏览器不同，操作按钮也是如此。

![](img/be897bd1bfd4dab38767db24da2a794b_290_0.png)

6. 点击允许接受 Cookie。

![](img/be897bd1bfd4dab38767db24da2a794b_290_1.png)

你应该看到文本：Mmmmm...cookie!

## 使用 Cookie 变量

使用 Cookie 有一个元素大多数人会忘记，直到他们花费几个小时调试一个完全错误的问题。当网络浏览器接受 Cookie 时，在下一次 HTTP 请求之前你无法提取它的值。换句话说，如果你在页面 1 上设置了一个值为 Julie 的 Cookie 名称，在用户到达页面 2（或页面 5 或页面 28——任何不是设置 Cookie 的页面）之前，你无法提取该值。

```

在上一章的身份验证脚本中，你有一个登录表单和一个结果页。但是，身份验证仅对结果页有效，因为它动态显示了内容（在本例中为恭喜消息！如果你想对一组静态页面进行身份验证，你必须进行一些微调。

1. 在文本编辑器中打开 `do_autuser.php`。

2. 滚动到处理身份验证结果的 `if_else` 块。添加一个设置 Cookie 的块：

```php
if ($num != 0) {
  $cookie_name = "auth";
  $cookie_value = "ok";
  $cookie_expire = "0";
  $cookie_domain = "127.0.0.1";
  setcookie($cookie_name, $cookie_value, $cookie_expire,
  "/", $cookie_domain, 0);
}
```

> 注意
setcookie() 函数将发送一个名为 `auth`、值为 `ok` 的 Cookie。它将在会话结束时过期，并对 127.0.0.1 上的所有目录有效。如果适用，请使用自己的域名。




# 第 16 章：使用 COOKIES

3. 删除此行：

```php
$msg = "<P>恭喜，你已获得授权!</p>";
```

4. 添加此字符串：

```php
$display_block = "
<p><strong>秘密菜单：</strong></p>
<ul>
<li><a href=\"\secretA.php\">秘密页面 A</a></li>
<li><a href=\"\secretB.php\">秘密页面 B</a></li>
</ul>
";
```

> 注意
> 别担心；你很快就会创建此菜单中的页面了。

5. 向下滚动，直到看到以下代码：

```php
<?php echo "$msg"; ?>
```

6. 将其替换为以下内容：

```php
<?php echo "$display_block"; ?>
```

7. 保存文件。

你的新代码看起来应该像这样：

```php
<?php
//检查必填字段
if ((($_POST['username']) || (!$_POST['password']))) {
  header("Location: /show_login.html");
  exit;
}

//设置使用的数据库和表名
$db_name = "testDB";
$table_name = "auth_users";
//连接服务器并选择数据库
$connection = @mysql_connect("localhost", "spike", "9sj7En4") or die(mysql_error());
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

```php
//构建并执行查询
$sql = "SELECT * FROM $table_name WHERE
username = \"$_POST['username']\" AND
password = \"$_POST['password']\"";
```

$result = @mysql_query($sql) or die (mysql_error());

```php
//获取结果集中的行数
$num = mysql_numrows($result);
```

```php
//如果已授权，打印消息并设置 cookie，
//如果未授权，则重定向到其他地方
if ($num != 0) {
  $cookie_name = "auth";
  $cookie_value = "ok";
  $cookie_expire = "0";
  $cookie_domain = "127.0.0.1";
  setcookie($cookie_name, $cookie_value, $cookie_expire,
  "/", $cookie_domain, 0);

$display_block = "
<p><<strong>>秘密菜单：</strong></p>
<ul>
<li><a href=\"secretA.php\">秘密页面 A</a></li>
<li><a href=\"secretB.php\">秘密页面 B</a></li>
</ul>
";
} else {
  header("Location: /show_login.html");
  exit;
}
?>
```

```html
<HTML>
<HEAD>
<TITLE>秘密区域</TITLE>
</HEAD>
<body
<?php echo "$display_block"; ?>
</BODY>
</html>
```

打开你的 浏览器并输入 http://127.0.0.1/show_login.html 进入登录表单，然后输入有效的用户名和密码。如果你在接受 cookie 之前仍需设置偏好，你将看到一个包含 cookie 信息的对话框。

在你点击“是”（或“确定”，取决于对话框）后，新菜单将显示：

![](img/be897bd1bfd4dab38767db24da2a794b_294_0.png)

## 检查身份验证 Cookie

秘密菜单包含两个文件的链接：secretA.php 和 secretB.php。通过在这些页面开头添加一段代码，你可以检查用户是否已授权。

- 1. 在你的文本编辑器中打开新文件并开始一个 PHP 块：

```php
<?php
```

- 2. 开始一个 if_else 块来检查 $_COOKIE['auth'] 的值。只有当该值位 ok 时，用户才能被授权用户：

```php
if ($_COOKIE['auth'] == "ok") {
```

## 3. 创建一个值来保存成功消息：

```php
$msg = "<P>欢迎访问秘密页面 A，授权用户!</p>";
```

## 4. 继续编写 if_else 语句以处理未授权的访问者。未授权的用户将被重定向到登录表单：

```php
} else {
    header("Location: /show_login.html");
    exit;
}
```

> 注意
> 未授权的访问者是指尝试在不通过身份验证直接访问 secretA.php 的人。

## 5. 关闭 PHP 块并输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>秘密页面 A</TITLE>
</HEAD>
<body
```

### 6. 显示消息：

```php
<?php echo "$msg"; ?>
```

## 7. 添加更多 HTML 以使文档有效：

```html
</body>
</HTML>
```

## 8. 以 secretA.php 命名保存文件，并将此文件放在 Web 服务器的文档根目录下。secretB.php 的内容应与 secretA.php 几乎相同，创建另一个与 secretA.php 相同的文件，仅将 "A" 改为 "B"。

现在是进行测试了。除非你的浏览器崩溃了，否则你仍然处于登录状态（auth cookie 尚未过期），并且你应该能看到秘密菜单。如果你在接受 cookie 之前仍需设置偏好，你将看到一个包含 cookie 信息的对话框。

在你点击“是”（或“确定”，取决于对话框）后，新菜单将显示：

![](img/be897bd1bfd4dab38767db24da2a794b_294_0.png)

## 检查身份验证 Cookie

秘密菜单包含两个文件的链接：secretA.php 和 secretB.php。通过在这些页面开头添加一段代码，你可以检查用户是否已授权。

- 1. 在你的文本编辑器中打开新文件并开始一个 PHP 块：

```php
<?php
```

- 2. 开始一个 if_else 块来检查 $_COOKIE['auth'] 的值。只有当该值位 ok 时，用户才能被授权用户：

```php
if ($_COOKIE['auth'] == "ok") {
```

...并输入 http://127.0.0.1/show_login.html 进入登录表单，然后输入有效的用户名和密码。如果你在接受 cookie 之前仍需设置偏好，你将看到一个包含 cookie 信息的对话框。

在你点击“是”（或“确定”，取决于对话框）后，新菜单将显示：

![](img/be897bd1bfd4dab38767db24da2a794b_294_0.png)

## 3. 创建一个值来保存成功消息：

```php
$msg = "<P>欢迎访问秘密页面 A，授权用户!</p>";
```

## 4. 继续编写 if_else 语句以处理未授权的访问者。未授权的用户将被重定向到登录表单：

```php
} else {
    header("Location: /show_login.html");
    exit;
}
```

> 注意
> 未授权的访问者是指尝试在不通过身份验证直接访问 secretA.php 的人。

## 5. 关闭 PHP 块并输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>秘密页面 A</TITLE>
</HEAD>
<body
```

### 6. 显示消息：

```php
<?php echo "$msg"; ?>
```

## 7. 添加更多 HTML 以使文档有效：

```html
</body>
</HTML>
```

## 8. 以 secretA.php 命名保存文件，并将此文件放在 Web 服务器的文档根目录下。secretB.php 的内容应与 secretA.php 几乎相同，创建另一个与 secretA.php 相同的文件，仅将 "A" 改为 "B"。

现在是进行测试了。除非你的浏览器崩溃了，否则你仍然处于登录状态（auth cookie 尚未过期），并且你应该能看到秘密菜单。





1. 在你的文本编辑器中打开新文件并开始一个 PHP 块，然后调用 `session_start()` 函数：

```php
<?php session_start();?>
```

> 注意：`session_start()` 函数实际上执行了多项重要任务。首先，它确定当前用户是否已启动会话，如果有必要，则启动一个。它还会通知 PHP 引擎在特定脚本将使用会话变量和其他会话相关的函数。

由于 `session_start()` 有双重用途，请在所有与会话相关的脚本开头使用它。

2. 创建一个字符串来存储消息，然后关闭 PHP 块：

```php
$msg = "started a session...";?>
```

3. 输入以下 HTML：

```html
<HTML><HEAD><TITLE>Start a Session</TITLE></HEAD><BODY>
```

4. 显示消息字符串：

```php
<?php echo "$msg"; ?>
```

5. 添加更多 HTML 以使文档有效：

```html
</BODY></HTML>
```

6. 将文件保存为 `session.php`，并将此文件放置在你的 Web 服务器的文档根目录下。

7. 打开你的浏览器并输入 `http://127.0.0.1/session.php`。

# 理解会话变量 281

如果你仍然设置了在接受 Cookie 之前警告，你将看到如下图所示的对话框（或适用于你浏览器的框）。

![](img/be897bd1bfd4dab38767db24da2a794b_303_0.png)

在你点击“允许”后，消息将显示出来。

这多么具有启发性？在下一节中，你将注册一个实际值并观察它在会话过程中发生的变化。

![](img/be897bd1bfd4dab38767db24da2a794b_303_1.png)

# 注册和修改会话变量

此脚本的目标是注册一个变量并在会话过程中更改其值。

- 1. 在你的文本编辑器中打开新文件，开始一个 PHP 块，并调用 `session_start()` 函数：

```php
<?php
session_start();
```

- 2. 注册一个名为 `count` 的变量：
session_register('count');

> 注意
> 现在，只要此会话存在，名为 `$_SESSION['count']` 的变量就是可用的。目前，该变量没有值。

- 3. 递增 `$_SESSION['count']` 的值以记录当前访问：
$_SESSION['count']++

- 4. 创建一个字符串来存储消息，包括 `$_SESSION['count']` 的值：
$msg = "<P>You've been here $_SESSION['count'] times. Thanks!</p>";

- 5. 关闭 PHP 块并输入以下 HTML：

```php
?>
<HTML>
<HEAD>
<TITLE>Count Me!</TITLE>
</HEAD>
<BODY>
```

- 6. 显示消息字符串：
<?php echo "$msg"; ?>

- 7. 添加更多 HTML 以使文档有效：

```html
<body>
</html
```

- 8. 将文件保存为 `countme.php`，并将此文件放置在你的 Web 服务器的文档根目录下。

- 9. 打开你的浏览器并输入 `http://127.0.0.1/countme.php`。

除非在上一个脚本和现在之间关闭了浏览器，否则你的旧会话仍然处于激活，你不会看到 Cookie 确认对话框。你应该只会看到下图。

![](img/be897bd1bfd4dab38767db24da2a794b_305_0.png)

多次刷新页面，观察计数器在每次刷新后如何递增 1。例如，我刷新了页面八次，最后看到了下一页显示的图形。

## 第 17 章：会话基础

在下一节中，你处理的仅仅是访问计数器——你将在用户会话期间设置并显示用户偏好。

![](img/be897bd1bfd4dab38767db24da2a794b_306_0.png)

# 使用会话管理用户偏好

除了简单的访问计数器，你可以使用会话在用户访问你的网站时管理他们的偏好。在这个三步的示例中，你将启动一个会话，询问用户她的字体族和基础字体大小偏好，在后续页面上显示这些偏好，并允许用户改变主意并重置值。

# 启动会话并注册默认值

在此脚本中，你将启动会话并注册 `font_family` 和 `font_size` 变量。显示的 HTML 将是一个允许更改偏好的表单。

- 1. 在你的文本编辑器中打开新文件，开始一个 PHP 块，并调用 `session_start()` 函数：

```php
<?php
session_start();
```

# 使用会话管理用户偏好 285

2. 启动 [if...else] 块来检查 `font_family` 和 `font_size` 是否有之前的值。如果当前会话中不存在这些值，则分配默认值并添加它们：

```php
if (!$_SESSION['font_family']) || (!$_SESSION['font_size'])) {
  $_SESSION['font_family'] = "sans-serif";
  $_SESSION['font_size'] = "10";
}
```

- 3. 如果值存在，
```php
} else {
```
> 注意
> 现在，只要用户返回此脚本，由于你必须考虑到每次加载页面时如果简单地添加变量，这些值就会被覆盖。

- 4. 关闭 PHP 块并输入以下 HTML：
```php
?>
<HTML>
<HEAD>
```

- 5. 创建 `<style>` 标签：
```html
<style type="text/css">
```

- 6. 为 `BODY`、`P` 和 `A` 标签添加样式：
```css
BODY, P, A (font-family:<?php echo $font_family; ?>);
font-size:<?php echo $font_size; ?>;pt;
font-weight:normal;
```

- 7. 为 `H1` 标签添加样式：
```css
H1 (font-family:<?php echo $font_family; ?>);
font-size:<?php echo $font_size + 4; ?>;pt;
font-weight:bold;
```

- 8. 关闭 `<style>` 标签：
```html
</style>
```

- 9. 创建允许用户选择字族的单选按钮：
```html
<P>Pick a Font Family:<br>
<input type="radio" name="sel_font_family" value="serif">
<input type="radio" name="sel_font_family" value="sans-serif" checked>
```

- 10. 创建允许用户选择字体大小的单选按钮：
```html
<P>Pick a Font Size:<br>
<input type="radio" name="sel_font_size" value="8">
<input type="radio" name="sel_font_size" value="10" checked>
<input type="radio" name="sel_font_size" value="12">
```

- 11. 添加提交按钮并关闭表单：
```html
<p><input type="submit" value="Set Preferences"/></p>
</form>
```

- 12. 添加更多 HTML 以使文档有效：
```html
</body>
</html
```

- 13. 将文件保存为 `session01.php`，并将此文件放置在你的 Web 服务器的文档根目录下。

你的完整代码如下：

```php
<?php
//启动会话
session_start();
//检查存储的值并注册默认值
if (!$_SESSION['font_family']) || (!$_SESSION['font_size'])) {
  $_SESSION['font_family'] = "sans-serif";
  $_SESSION['font_size'] = "10";
  $_SESSION['font_family'] = $font_family;
  $_SESSION['font_size'] = $font_size;
} else {
  //从 $_SESSION 超局变量中提取
  $font_family = $_SESSION['font_family'];
  $font_size = $_SESSION['font_size'];
}
?>
<html>
<head>
<title>My Display Preferences</title>
<style type="text/css">
BODY, P, A (font-family:<?php echo $font_family; ?>);
font-size:<?php echo $font_size; ?>;pt;
font-weight:normal;
H1 (font-family:<?php echo $font_family; ?>);
font-size:<?php echo $font_size + 4; ?>;pt;
font-weight:bold;
</style>
</head>
<body>
<h1>Set Your Preferences</h1>
<form method="POST" action="session02.php">
<p>Pick a Font Family:<br>
<input type="radio" name="sel_font_family" value="serif">
<input type="radio" name="sel_font_family" value="sans-serif" checked>
<p>Pick a Font Size:<br>
<input type="radio" name="sel_font_size" value="8">
<input type="radio" name="sel_font_size" value="10" checked>
<input type="radio" name="sel_font_size" value="12">
<p><input type="submit" value="Set Preferences"/></p>
</form>
</body>
</html>
```




<form>
<input type="radio" name="sel_font_family" value="Courier"> Courier
<input type="radio" name="sel_font_family" value="Wingings">

<p>选择基础字体大小:<br>
<input type="radio" name="sel_font_size" value="8"> 8pt
<input type="radio" name="sel_font_size" value="10" checked> 10pt
<input type="radio" name="sel_font_size" value="12"> 12pt
<input type="radio" name="sel_font_size" value="14"> 14pt
</p>
<p><input type="submit" name="submit" value="设置显示偏好"></p>
</form>
<body>

现在打开你的网络浏览器并输入 http://127.0.0.1/session01.php。

除非你在上一个脚本和现在之间关闭了浏览器，否则你的旧会话（session）将保持有效，你不会看到 cookie 确认对话框。你应该只会看到下面的图。

![](img/be897bd1bfd4dab38767db24da2a794b_310_0.png)

在下一节中，你将创建偏好变化的脚本。

## 修改偏好

在这个脚本中，你为 font_family 和 font_size 分配新值，并显示更改已完成确认。

1.  在你的文本编辑器中打开新文件，开始一个 PHP 块并调用 `session_start()` 函数：

```php
<?php session_start();
```

2.  启动一个 if_else 块来检查提交的 `font_family` 和 `font_size` 值。如果存在这些值，则将其添加到会话中：
```php
if ($_POST['sel_font_family'] && $_POST['sel_font_size']) {
  $font_family = $_POST['sel_font_family'];
  $font_size = $_POST['sel_font_size'];
  $_SESSION['font_family'] = $font_family;
  $_SESSION['font_size'] = $font_size;
}
```

3.  继续该块以检查之前存储的 `font_family` 和 `font_size` 值，但仅在提交值不存在的情况下进行：
```php
} else if (!($_POST['sel_font_family'] && $_POST['sel_font_size']) && ($_SESSION['font_family']) && $_SESSION['font_size'])) {
  $font_family = $_SESSION['font_family'];
  $font_size = $_SESSION['font_size'];
  $_SESSION['font_family'] = $font_family;
  $_SESSION['font_size'] = $font_size;
}
```

4.  最后，如果表单或之前的会话中不存在值，则定义并添加一些默认值：
```php
else {
  $font_family = "sans-serif";
  $font_size = "10";
  $_SESSION['font_family'] = $font_family;
  $_SESSION['font_size'] = $font_size;
}
```

5.  关闭 PHP 块并输入以下 HTML：

```php
?>
<HTML>
<HEAD>
<TITLE>我的显示偏好</TITLE>
```

6.  创建一个样式表块，以打开 `<STYLE>` 标签开始：

```html
<STYLE type="text/css">
```

7.  为 BODY、P 和 A 添加样式表项目，通过将 HTML 和 PHP 混合来显示 `$font_family` 和 `$font_size` 的当前值：

```css
BODY, P, A {font-family:<?php echo "$font_family"; ?>;
font-size:<?php echo "$font_size"; ?>pt;font-weight:normal;}
```

8.  为 H1 标签添加样式表项目。混合 HTML 和 PHP 以显示 `$font_size` 的值以及修改后的 `$font_size` 值（基础值为 4）：
```css
H1 {font-family:<?php echo "$font_family"; ?>;
font-size:<?php echo $font_size + 4; ?>pt;font-weight:bold;}
```

9.  关闭 `</STYLE>` 标签并继续编写 HTML，显示两个已注册会话变量的值：

```html
</STYLE>
</HEAD>
<h1>您的偏好已设置</h1>
<p>如您所见，您选择的字体现在是
<?php echo "$font_family"; ?>,基础大小为
<?php echo "$font_size"; ?>pt。</p>
```

10. 提供一个返回到 session01.php 的链接，以防用户想要再次更改偏好，并添加更多 HTML 以使文档有效：

```html
<p>请随时 <a href="session01.php">再次更改您的偏好</a>。</p>
</BODY>
</HTML>
```

11. 将文件保存为 `session02.php`，并将此文件放置在 Web 服务器的文档根目录下。

你的整个代码应该像这样：

```php
<?php
//启动会话
session_start();
//检查提交的值并注册默认值
if ($_POST['sel_font_family'] && $_POST['sel_font_size']) {
    $font_family = $_POST['sel_font_family'];
    $font_size = $_POST['sel_font_size'];
    $_SESSION['font_family'] = $font_family;
    $_SESSION['font_size'] = $font_size;
}
//检查存储的值，从会话超全局中提取
else if (!$_POST['sel_font_family'] && !$_POST['sel_font_size']) {
    if ($_SESSION['font_family'] && $_SESSION['font_size']) {
        $font_family = $_SESSION['font_family'];
        $font_size = $_SESSION['font_size'];
    }
    $_SESSION['font_family'] = $font_family;
    $_SESSION['font_size'] = $font_size;
}
//注册默认值
else {
    $font_family = "sans-serif";
    $font_size = "10";
    $_SESSION['font_family'] = $font_family;
    $_SESSION['font_size'] = $font_size;
}
?>
<HTML>
<HEAD>
<TITLE>我的显示偏好</TITLE>
<STYLE type="text/css">
BODY, P, A {font-family:<?php echo "$font_family"; ?>;
font-size:<?php echo "$font_size"; ?>pt;font-weight:normal;}
H1 {font-family:<?php echo "$font_family"; ?>;
font-size:<?php echo $font_size + 4; ?>pt;font-weight:bold;}
</STYLE>
</HEAD>
<h1>您的偏好已设置</h1>
<p>如您所见，您选择的字体现在是
<?php echo "$font_family"; ?>,基础大小为
<?php echo "$font_size"; ?>pt。</p>
<p>请随时 <a href="session01.php">再次更改您的偏好</a>。</p>
</BODY>
</HTML>
```




## 设计与创建管理菜单

你不仅可以查看系统中的数据，还可以添加、修改和删除联系人。创建一个菜单是一个好主意——它能提供指向所有操作脚本的链接，并加入一些身份验证，这样只有你才能看到这些数据。现在，把所有内容都写在一个脚本里！

- 1. 在你的文本编辑器中打开一个新文件并开始 PHP 块。然后启动会话，或者如果它已存在则继续使用：

```php
<?
session_start();
```

- 2. 启动一个 _if_else_ 块来检查 $_POST[op] 变量的值，该变量是你即将创建的登录表单中的隐藏变量：

```php
if ($_POST['op'] == "ds") {
```

- 3. 如果 $_POST[username] 的值为 ds，说明用户已完成表单。启动另一个 _if_else_ 块来检查用户输入的用户名和密码的有效性：

```php
if ($_POST['username'] != "admin") || ($_POST['password'] != "abc123") {
```

> 注意
你可以使用任何想要的用户名和密码。此脚本被硬编码为检查用户名是否为 admin 以及密码是否为 abc123。

- 4. 如果用户名或密码任错误，创建一个名为 $msg 的变量来存储错误信息：

```php
$msg = "<p><font color='#FF0000><strong>Bad Login - Try Again!</strong></font></p>";
```

- 5. 创建变量 $show_form 并给其赋值值 yes。这个值将在脚本稍后的部分中被检查，以决定显示什么：

```php
$show_form = "yes";
```

- 6. 继续 if...else 语句：

```php
} else {
```

- 7. 如果用户运行到了这一步，说明用户名和密码是正确的。因此，在会话变量 $_SESSION[valid] 中存储值 yes：

```php
$_SESSION['valid'] = "yes";
```

- 8. 创建变量 $show_menu 并给其赋值值 yes。这个值将在脚本稍后的部分中被检查，以决定显示什么：

```php
$show_menu = "yes";
```

- 9. 关闭内部的 if...else 块：

```php
}
```

- 10. 继续外部的 if...else 块：

```php
} else {
```

- 11. 如果用户位于外部 if...else 块的这一区域，说明他没有通过表单就到达了此脚本。检查 $_SESSION[valid] 的值，并决定显示什么——菜单还是表单：

```php
if ($_SESSION['valid'] == "yes") {
  $show_menu = "yes";
} else {
  $show_form = "yes";
}
```

- 12. 关闭外部的 if...else 块：

```php
}
```

- 13. 创建表单块，如果用户未登录或登录错误，将显示该块。开始创建变量并打印标题：

```php
$form_block = "<<h1>>Login</h1>";
```

- 14. 开始编写表单。在这种情况下，method 为 POST，action 是名为 $_SERVER[PHP_SELF] 的变量：

```html
<form method="POST" action="<?=$_SERVER['PHP_SELF']">
```

## 300 第18 章：规划你的系统

> 注意
$_SERVER[PHP_SELF] 是一个全局变量，其值等于当前脚本的。通过使用 $_SERVER[PHP_SELF] 作为表单 action，你实际上是在说：“当点击提交按钮时，重新加载我！”

- 15. 打印 $msg 的值：

```php
echo $msg
```

> 注意
如果登录错误，$msg 将包含一个值，该值将在此处被打印。如果 $msg 未被创建或未赋值，则什么都不会打印，因此它一直存在并无大碍。

- 16. 为用户名和密码创建带有文本标签的输入字段：

```html
<p><strong>username:</strong><br>
<input type="text" name="username" size="15" maxlength="25"></p>
<p><strong>password:</strong><br>
<input type="password" name="password" size="15" maxlength="25"></p>
```

- 17. 添加 op 的隐藏字段：

```html
<input type="hidden" name="op" value="ds">
```

- 18. 添加提交按钮，并关闭表单和字符串：

```html
<p><input type="submit" name="submit" value="login"></p>
</form>
```

- 19. 创建菜单块，如果用户已登录且有效，将显示该块。首先创建变量并打印标题：

```php
$menu_block = "<h1>My Contact Administration System</h1>";
```

- 20. 添加若干菜单项并关闭字符串：

```html
<p><strong>Administration</strong></p>
<ul>
<li><a href="show_addcontact.php">Add a Contact</a></li>
<li><a href="pick_modcontact.php">Modify a Contact</a></li>
<li><a href="pick_delcontact.php">Delete a Contact</a></li>
</ul>
<p><strong>View Records</strong></p>
<ul>
<li><a href="show_contactsbyname.php">Show Contacts, Ordered by Name</a></li>
</ul>
```

- 21. 使用 if...else 块进行最终检查，判断显示 form_block 还是 $menu_block。给新变量 $display_block 赋值：

```php
if ($show_form == "yes") {
    $display_block = $form_block;
} else if ($show_menu == "yes") {
    $display_block = $menu_block;
}
```

- 22. 关闭你的 PHP 块并添加 HTML：

```html
<html>
<head>
<title>Contact Management System</title>
</head>
<body>
```

- 23. 显示结果：

```php
<?php echo $display_block; ?>
```

- 24. 添加一些 HTML 使之成为有效文档：

```html
</body>
</html>
```

- 25. 将文件保存为 `contact_menu.php`，并把此文件置于你 Web 服务器的根目录下。

你刚刚创建了大量代码。它看起来应该像这样：

```php
<?php session_start();
//检查用户是否来自表单
if ($_POST['op'] == "ds") {
    //检查用户名和密码
    if ($_POST['username'] != "admin") || ($_POST['password'] != "abc123") {
        //处理登录失败
        $msg = "<font color='#FF0000'><strong>Bad Login - Try Again!</strong></font></p>";
        $show_form = "yes";
    }
    //处理登录成功
    $_SESSION['valid'] = "yes";
    $show_menu = "yes";
} else {
    //决定显示什么
    if ($_SESSION['valid'] == "yes") {
        $show_menu = "yes";
    } else {
        $show_form = "yes";
    }
}
//构建表单
$form_block = "<h1>Login</h1><form method='POST' action='$_SERVER['PHP_SELF']\">
$msg
<p>username:</br>
<input type='text' name='username' size='15' maxlength='25'></p>
<p>password:</br>
<input type='password' name='password' size='15' maxlength='25'></p>
<input type='hidden' name='op' value='ds'>
<input type='submit' name='submit' value='login'></p>
</form>
//构建菜单
$menu_block = "<h1>My Contact Administration System</h1>";
```

```html
<p><strong>Administration</strong></p>
<ul>
<li><a href="show_addcontact.php">Add a Contact</a></li>
<li><a href="pick_modcontact.php">Modify a Contact</a></li>
<li><a href="pick_delcontact.php">Delete a Contact</a></li>
</ul>
<p><strong>View Records</strong></p>
<ul>
<li><a href="show_contactsbyname.php">Show Contacts, Ordered by Name</a></li>
</ul>
```

```php
//将块赋值给脚本以显示 $display_block 变量
if ($show_form == "yes") {
    $display_block = $form_block;
} else if ($show_menu == "yes") {
    $display_block = $menu_block;
}
?>
```

```html
<html>
<head>
<title>Contact Management System</title>
</head>
<body>
<?php echo $display_block; ?>
</body>
</html>
```

## 登录管理菜单

现在尝试使用脚本中硬编码的用户名和密码登录管理菜单。

- 1. 打开你的浏览器并输入 http://127.0.0.1/contact_menu.php。

## 304 第18 章：规划你的系统

你将看到登录表单，包含用户名和密码的文本字段，以及一个提交按钮。

(img/be897bd1bfd4dab38767db24da2a794b_326_0.png)

- 2. 在相应字段输入错误的用户名和或错误的密码，然后点击登录按钮。

(img/be897bd1bfd4dab38767db24da2a794b_326_1.png)

你会再次看到登录表单，显示红色的错误信息。

- 3. 输入正确的用户名 (admin) 和正确的密码 (abc123)，然后点击登录按钮。

## 定义 MY_CONTACTS 表

(img/be897bd1bfd4dab38767db24da2a794b_327_0.png)

你将看到你联系人管理系统的管理菜单。

在下一节中，你将后退一步创建 my_contacts 表，这样你就可以执行这个 fancy管理菜单中列出的所有任务了！





| 表 18.1 my_contacts 的字段 |
| 字段名称 | 说明 |
| :--- | :--- |
| id | 为条目创建一个唯一的 ID 编号 |
| f_name | 人的名 |
| l_name | 人的姓 |
| address1 | 地址的第一行 |
| address2 | 地址的第二行 |
| address3 | 地址的第三行 |
| postcode | 邮政编码或邮政代码 |
| country | 人居住的国家 |
| prim_tel | 主电话号码 |
| sec_tel | 次电话号码 |
| email | 电子邮件地址 |
| birthday | 人的生日 |

在下一节中，你将修改来自第 12 章“创建数据库表”的表创建脚本。你将添加为主键和自动递增字段命的功能。

## 修改表创建脚本

通过对第 12 章表创建序列中的两个脚本进行一些细微修改，你就可以在表单中添加复选框来处理主键和自动递增字段。这类字段对于 ID 字段非常有用。

1. 在文本编辑器中打开 `do_showfielddef.php`，找到打印表头的 `$form_block` 部分，并在行的结束符号之前添加以下内容：

```php
<TH>PRIMARY KEY?</TH><TH>AUTO-INCREMENT?</TH>
```

## 定义 MY_CONTACTS 表

2. 在 `for` 循环内的 `$form_block` 中，倒数第三第三的行会打印一个名为 `field_length[]` 的文本字段。在该行之后、表行结束之前，添加以下两行：

```php
<TD ALIGN="CENTER"><INPUT TYPE="checkbox" NAME="primary[]"
VALUE="Y"></TD>
<TD ALIGN="CENTER"><INPUT TYPE="checkbox" NAME="auto_increment[]"
VALUE="Y"></TD>
```

3. 保存此文件。

你对该脚本的修改后的代码应该看起来像这样：

```php
<?php
//验证重要输入
if (($_POST[table_name]) || (!$_POST[num_fields])) {
  header ("Location: http://127.0.0.1/show_createthtable.html");
  exit();
}
//开始创建显示表单
$form_block = "
<FORM METHOD=\"$_POST\" ACTION=\"do_createthtable.php\">
<INPUT TYPE="hidden" NAME="table_name" VALUE=\"$_POST[table_name]\
<TABLE CELLSPACING=5 CELLPADDING=5>
<TR>
<TH>FIELD NAME</TH><TH>TYPE</TH><TH>FIELD LENGTH</TH>
<TH>PRIMARY KEY?</TH><TH>AUTO-INCREMENT?</TH><TH*</TH>
<";
//从 0 开始计数直到达到字段数量
for ($i = 0; $i < $_POST[num_fields]; $i++) {
// 添加到表单，每个字段占一行
$form_block .= "<TR>
<TD ALIGN="CENTER"><INPUT TYPE="text"
NAME="field_name[]" SIZE="30"></TD>
<TD ALIGN="CENTER">
<SELECT NAME="field_type[]">
<OPTION VALUE="char">char</OPTION>
<OPTION VALUE="date">date</OPTION>
<OPTION VALUE="float">float</OPTION>
<OPTION VALUE="int">int</OPTION>
<OPTION VALUE="text">text</OPTION>
<OPTION VALUE="varchar">varchar</OPTION>
</SELECT>
```

# 第 18 章：规划你的系统

```php
</TD>
<TD ALIGN=CENTER><INPUT TYPE="text"
NAME="field_length[]" SIZE="5"></TD>
<TD ALIGN="CENTER"><INPUT TYPE="checkbox"
NAME="primary[]" VALUE="Y"></TD>
<TD ALIGN="CENTER"><INPUT TYPE="checkbox"
NAME="auto_increment[]" VALUE="Y"></TD>
</TR>

//完成表单
$form_block .= "<TR>
<TD ALIGN=CENTER COLSPAN=3><INPUT TYPE="submit VALUE=\"Create Table\"></TR>
</TABLE>
</FORM>";
?>
<HTML>
<HEAD>
<TITLE>创建数据库表：第 2 步</TITLE>
</HEAD>
<BODY>
<h1>为 <?php echo \$POST["table_name"]; 定义字段</h1>
<?php echo \$form_block; ?>
</BODY>
</HTML>
```

接下来，你将修改表创建脚本的最后部分。

1. 在文本编辑器中打开 `do_createtable.php`。

2. 在 `for` 循环内部，第一行向 `$sql` 变量中附加文本，该变量存储了用于创建表的 SQL 语句。由于你为 SQL 语句的额外元素添加了两个复选框，你需要检查它们。首先，创建一个 `if_else` 块来检查 `auto_increment` 复选框是否被勾选：

```php
if ($_POST[auto_increment][$i] == "Y") {
```

## 定义 MY_CONTACTS 表

3. 如果 `auto_increment` 复选框被勾选，创建一个变量来存储附加的 SQL 选项：

```php
$additional = "NOT NULL auto_increment";
```

> 注意
> 当你将一个字段定义为 `auto_increment` 时，它也必须被定义为 NOT NULL。

4. 如果 `auto_increment` 复选框未被勾选，创建该变量但不在其中包含任何内容，然后结束块。这将重置字符串的值为空值：

```php
else {
$additional = "";
}
```

5. 创建一个 `if_else` 块来检查主键复选框是否被勾选：

```php
if ($_POST[primary][$i] == "Y") {
```

6. 如果主键复选框被勾选，将主键语法附加到 `$additional` 变量中：

```php
$additional .= ", primary (";
```

> 注意
> 将一个字段定义为主键的语法如下：

7. 如果主键复选框未被勾选，将空值附加到 `$additional`，然后结束块：

```php
else {
$additional = "";
}
```

# 第 18 章：规划你的系统

8. 找到用于 SQL 语句的字段定义的行：

```php
$_POST[field_length][$i]).",
```

9. 如果 `$_POST[field_length][$i]` 不为空，则将 `$additional` 附加到 `$sql`：

```php
$sql .= "\additional";
```

10. 同样，找到如下的行：

```php
$sql .= "\additional";
```

11. 修改该行，使其变为：

```php
$sql = substr($sql, -1);
$sql .= ",";
```

12. 在此之后，如果 `$_POST[field_length][$i]` 不为空，则将 `$additional` 附加到 `$sql`：

```php
$sql .= "\additional";
```

13. 修改该行，使其变为：

```php
$sql .= "\additional";
```

14. 修改该行，使其变为：

```php
$sql = substr($sql, -1);
$sql .= ");";
```

15. 执行查询：

```php
$result = mysql_query($sql,$connection) or die(mysql_error());
```

16. 成功后获取一个用于显示的消息：

```php
if ($result) {
  $msg = "<P>".$POST[table_name].\" 已创建!</P>";
}
```





5. 在第五行，在字段名称（Field Name）处输入 `address2`，从字段类型（Field Type）下拉菜单中选择 `varchar`，并指定字段长度（Field Length）为 100。

6. 在第六行，在字段名称（Field Name）处输入 `address3`，从字段类型（Field Type）下拉菜单中选择 `varchar`，并指定字段长度（Field Length）为 100。

7. 在第七行，在字段名称（Field Name）处输入 `postcode`，从字段类型（Field Type）下拉菜单中选择 `varchar`，并指定字段长度（Field Length）为 25。

8. 在第八行，在字段名称（Field Name）处输入 `country`，从字段类型（Field Type）下拉菜单中选择 `varchar`，并指定字段长度（Field Length）为 100。

9. 在第九行，在字段名称（Field Name）处输入 `prim_tel`，从字段类型（Field Type）下拉菜单中选择 `varchar`，并指定字段长度（Field Length）为 35。

10. 在第十行，在字段名称（Field Name）处输入 `sec_tel`，从字段类型（Field Type）下拉菜单中选择 `varchar`，并指定字段长度（Field Length）为 35。

11. 在第十一行，在字段名称（Field Name）处输入 `email`，从字段类型（Field Type）下拉菜单中选择 `varchar`，并指定字段长度（Field Length）为 100。

12. 在第十二行，在字段名称（Field Name）处输入 `birthday`，并在字段类型（Field Type）下拉菜单中选择 `date`。

完成后的表单应该像下图所示。

![](img/be897bd1bfd4dab38767db24da2a794b_336_0.png)

![](img/be897bd1bfd4dab38767db24da2a794b_336_1.png)

点击“创建表”（Create Table）按钮创建 `my_contacts` 表。

# 为 my_contacts 定义字段

| 字段名称 (FIELD NAME) | 字段类型 (FIELD TYPE) | 字段长度 (FIELD LENGTH) | 主键? (PRIMARY KEY?) | 自动递? (AUTO-INCREMENT?) |
| --- | --- | --- | --- | --- |
| id | int | | | |
| Fname | varchar | 75 | | |
| _name | varchar | 75 | | |
| address1 | varchar | 100 | | |
| address2 | varchar | 100 | | |
| address3 | varchar | 100 | | | |
| postcode | varchar | 25 | | | |
| country | varchar | 100 | | | |
| prim_tel | varchar | 35 | | | |
| email | varchar | 100 | | | |
| birthday | date | | | |

> 这是一个通用的通讯录架构（schema），显然你可以看出哪里可以使其更紧凑、更具体。例如，如果你知道你的通讯录仅限美国，你可以将地址字段改为两个字符的州字段和一个 10 个字符的 ZIP 码字段。你对想要存储在表中的数据了解越多，就能定义得越精确。在这种情况下，，目标仅仅是学习通流程，这已经足够了——尽管表结构可能有点松散。掌握它之后，请自己去发散吧！

![](img/be897bd1bfd4dab38767db24da2a794b_336_2.png)

# 正在向 testDB 添加表...

`my_contacts` 已创建！

恭喜！表已经创建。在下一章中，你将为此表创建添加记录的界面。你正处于创建联系人管理系统的道路上！

## 添加联系人

你已经在开发路径上迈进了一步——你已经准备好了 `my_contacts` 表，等待着添加联系人。在本章中，你将学习如何：

- 创建一个用于添加记录的管理界面
- 创建一个将记录插入你的表的脚本
- 在查看脚本或添加记录之前，需要基于会话的身份验证

# 创建添加记录表单

HTML 表单将包含 `my_contacts` 表中每一列对应的一个输入字段。在上一章中，你创建了 12 个字段，对应 12 列。你的添加记录界面应该为这些字段中的每一个留出空间，但 ID 字段外可以留空。

> 注意
> 因为 ID 字段是自动递增字段，如果你添加记录并留空该字段，MySQL 将在该字段中放置下一个最大的可用数字。

1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块，然后启动会话，或者如果当前已存在则继续会话：

```php
<?
session_start();
```

2. 启动一个 `if_else` 块，检查 `$_SESSION[valid]` 的值并根据结果执行特定操作。如果值不是 `yes`，说明用户没有通过适当的验证通道：

```php
if ($_SESSION["valid"] != "yes") {
```

3. 将用户送回登录表单，并退出此脚本：

```php
header("Location: http://127.0.0.1/contact_menu.php");
exit;
```

4. 关闭你的 PHP 块，然后输入以下 HTML 开始构建添加记录的表单：

```html
?>
<HTML>
<HEAD>
<TITLE>我的联系人管理系统：添加联系人</TITLE>
</HEAD>
<BODY>
<h1>我的联系人管理系统</h1>
<h2><em>添加联系人</em></h2>
```

# 创建添加记录表单 

5. 开始你的表单。假设方法为 `POST`，动作动名为 `do_addcontact.php` 的脚本：

```html
<FORM METHOD="POST" ACTION="do_addcontact.php">
```

6. 开始一个 HTML 表格辅助布局。开始新的一行，添加两个表头，然后关闭：

```html
<table cellspacing="0" cellpadding="5">
<tr>
<th>姓名与地址信息</th>
<th>其他/个人信息</th>
</tr>
```

7. 开始新的一表格行和表格单元格，为人的姓名创建一个输入字段：

```html
<tr>
<td valign="top">
<p>名字：</p>
<input type="text" name="f_name" size="35">
```
```

8. 在同一个表格数据单元格中，为人的姓创建一个输入字段并带上标签：

```html
<p>姓：</p>
<input type="text" name="l_name" size="35">
```
```

9. 在同一个表格数据单元格中，为人的地址创建一个输入字段（第一行）：

```html
<p>地址行1：</p>
<input type="text" name="address1" size="35">
```

10. 在同一个表格数据单元格中，为人的地址创建一个输入字段（第二行）：

```html
<p>地址行2：</p>
<input type="text" name="address2" size="35">
```

11. 在同一个表格数据单元格中，为人的地址创建一个输入字段（第三行）：

```html
<p>地址行3：</p>
<input type="text" name="address3" size="35">
```

12. 在同一个表格数据单元格中，为人的邮政编码创建一个输入字段：

```html
<p>邮政编码：：</p>
<input type="text" name="postcode" size="35">
```

13. 在同一个表格数据单元格中，为人的国家创建一个输入字段：

```html
<p>国家：</p>
<input type="text" name="country" size="35">
</td>
```

14. 在一个新的表格数据单元格中，为人的主电话创建一个输入字段：

```html
<p>主电话：</p>
<input type="text" name="prim_tel" size="35">
</td>
```

15. 在同一个表格数据单元格中，为人的次电话创建一个输入字段：

```html
<p>次电话：</p>
<input type="text" name="sec_tel" size="35">
```

16. 在同一个表格数据单元格中，为人的电子邮箱地址创建一个输入字段：

```html
<p>电子邮箱：</p>
<input type="text" name="email" size="35">
```

17. 在同一个表格数据单元格中，为人的生日创建一个输入字段：

```html
<p>生日 (YYYY-MM-DD)：</p>
<input type="text" name="birthday" size="10">
</td>
</tr>
```

18. 开始一个跨越两列的新行和表格单元格。在内部添加一个提交按钮以及一个返回主菜单的链接。关闭单元格、表格行和表格本身：

```html
<tr>
<td align="center" colspan="2"><br>
<p><input type="SUBMIT" name="submit" value="将联系人添加到系统"></p>
<p><a href="contact_menu.php">返回主菜单</a></p>
<td></td>
</TR>
</TABLE>
```

# 创建添加记录表单

注意

MySQL 使用的日期类型使用 YYYY-MM-DD 格式。这种格式的一个示例是 2004-03-20（2004年3月20日）。在本示例应用程序中，你的日期字段设计为手动输入日期。在附录 C，“编写你自己的函数和对象”中，你将学习如何创建代码段来创建月份、天份的动态列表。

19. 关闭你的表单并添加更多 HTML 以使文档有效：

```html
</FORM>
</BODY>
</HTML>
```

20. 将文件另存为 `show_addcontact.php`，然后将此文件放在 Web 服务器的文档根目录下。

你的代码看起来应该是这样的：

```php
<?
//启动会话
session_start();

//验证用户查看他们是否被允许在这里
if ($_SESSION["valid"] != "yes") {
    header("Location: http://127.0.0.1/contact_menu.php");
    exit;
}
```





# 320 第 19 章：添加联系人

```html
<HTML>
<HEAD>
<TITLE>我的联系人管理系统：添加联系人</TITLE>
</HEAD>
<<body>
<h1>我的联系人管理系统</h1>
<h2><em>添加联系人</em></h2>
<form method="post" action="do_addcontact.php">
<table cellspacing="2" cellpadding="1">
<tr>
<th>姓名与地址信息</th>
<th>其他联系方式/个人信息</th>
</tr>
<td valign="top">
<p><strong>名：</strong><br>
<input type="text" name="f_name" size="35" maxlength="75"></p>
<p><strong>姓：</strong><br>
<input type="text" name="l_name" size="35" maxlength="75"></p>
<p><strong>地址行 1：</strong><br>
<input type="text" name="address1" size="35" maxlength="100"></p>
<p><strong>地址行 2：</strong><br>
<input type="text" name="address2" size="35" maxlength="100"></p>
<p><strong>地址行 3：</strong><br>
<input type="text" name="address3" size="35" maxlength="100"></p>
<p><strong>邮政编码：</strong><br>
<input type="text" name="postcode" size="35" maxlength="25"></p>
<p><strong>国家：</strong><br>
<input type="text" name="country" size="35" maxlength="100"></p>
</td>
<td valign="top">
<p><strong>主电话号码：</strong><br>
<input type="text" name="prim_tel" size="35" maxlength="35"></p>
<p><strong>次电话号码：</strong><br>
<input type="text" name="sec_tel" size="35" maxlength="35"></p>
<p><strong>电子邮件地址：</strong><br>
<input type="text" name="email" size="35" maxlength="100"></p>
<p><strong>生日 (YYYY-MM-DD)：</strong><br>
<input type="text" name="birthday" size="10" maxlength="10"></p>
</td>
</tr>
<tr>
<td align="center" colspan="2"><br><br>
<input type="submit" name="submit" value="添加联系人到系统">
<p><a href="contact_menu.php">返回主菜单</a></p>
</td>
</tr>
</table>
</form>
</body>
</html>
```

在接下来的章节中，你将创建一个脚本，该脚本将接收表单输入、创建 SQL 语句并将记录添加到数据库表中。

## 创建添加记录的脚本

此脚本将你的记录添加到 `my_contacts` 表中，并会考虑自增 ID 字段。

- 1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：

- 2. 启动一个 if...else 块，检查 `$_POST['f_name']` 和 `$_POST['l_name']` 中的值。如果它们没有值，则将用户重回表单并退出脚本：

```php
if (!$_POST['f_name']) || (!$_POST['l_name'])) {
    header("Location: http://127.0.0.1/show_addcontact.php");
    exit;
}
```

> 注意
> 你可以根据需要设置任意数量的必填字段。在本例中，你只检查了名和姓。

- 3. 如果必填字段有值，启动一个会，或者如果当前存在 session 则继续使用。关闭该块：

```php
} else {
    session_start();
}
```

- 4. 启动一个 if_else 块，检查 `$_SESSION['valid']` 的值并根据结果执行特定操作。如果值不是 yes，说明用户没有通过正确的身份验证通道：

```php
if ($_SESSION['valid'] != "yes") {
```

- 5. 将用户送回登录表单并退出此脚本：

```php
header("Location: http://127.0.0.1/contact_menu.php");
exit();
}
```

- 6. 创建一个变量来存储该表所在的数据库名称：

```php
$db_name = "testDB";
```

- 7. 创建一个变量来存储你用此脚本填充的表名：

```php
$table_name = "my_contacts";
```

- 8. 像你之前的那样添加连接信息：

```php
$connection = @mysql_connect("localhost", "spike", "9sj7En4") or die(mysql_error());
```

- 9. 如你学的那样选择数据库：

```php
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

- 10. 创建 SQL 语句。第一个括号语句给出了要填充的字段名称（按顺序），第二个括号语句发送实际字符串：

```php
$sql = "INSERT INTO $table_name (f_name, l_name, address1, address2, address3, postcode, country, prim_tel, sec_tel, email, birthday) VALUES";
```

> 注意
> 为 ID 字段留空位置将确保该字段自动递增。

- 11. 如你学的那样，创建一个变量来存储 `mysql_query()` 函数的结果的结果：

```php
$result = @mysql_query($sql,$connection) or die(mysql_error());
```

- 12. 关闭你的 PHP 块并添加此 HTML：

```html
<HTML>
<HEAD>
<TITLE>我的联系人管理系统：联系人已添加</TITLE>
</HEAD>
<<body>
<h1>我的联系人管理系统</h1>
<h2><em>联系人已添加</em></h2>
```

- 13. 添加一个确认语句。混合 HTML 和 PHP 以包含 `$table_name` 变量的值：

```php
<p>以下信息已成功添加到 <?php echo $table_name; ?></p>
```

- 14. 接下来，在 `show_addcontact.php` 中重建布局，混合 HTML 和 PHP 以显示值：

```html
<table cellspacing="2" cellpadding="1">
<tr>
<th>姓名与地址信息</th>
<th>其他联系方式/个人信息</th>
</tr>
<td valign="top">
<p><strong>名：</strong><br>
<?php echo $_POST['f_name']; ?></p>
<p><strong>姓：</strong><br>
<?php echo $_POST['l_name']; ?></p>
<p><strong>地址行 1：</strong><br>
<?php echo $_POST['address1']; ?></p>
<p><strong>地址行 2：</strong><br>
<?php echo $_POST['address2']; ?></p>
<p><strong>地址行 3：</strong><br>
<?php echo $_POST['address3']; ?></p>
<p><strong>邮政编码：</strong><br>
<?php echo $_POST['postcode']; ?></p>
<p><strong>国家：</strong><br>
<?php echo $_POST['country']; ?></p>
</td>
<td valign="top">
<p><strong>主电话号码：</strong><br>
<?php echo $_POST['prim_tel']; ?></p>
<p><strong>次电话号码：</strong><br>
<?php echo $_POST['sec_tel']; ?></p>
<p><strong>电子邮件地址：</strong><br>
<?php echo $_POST['email']; ?></p>
<p><strong>生日 (YYYY-MM-DD)：</strong><br>
<?php echo $_POST['birthday']; ?></p>
</td>
</tr>
```

- 15. 启动一个新的表格行和跨两列的表格单元格。在内部添加一个指向主菜单的链接：

```html
<tr>
<td align="center" colspan="2">
<a href="contact_menu.php">返回主菜单</a>
</td>
</tr>
```

- 16. 添加额外的 HTML 以使文档有效：

```html
</table>
</body>
</html>
```

- 17. 将文件保存为 `do_addcontact.php`，并将此文件放置在 Web 服务器的文档根。

继续下一步并开始添加联系人！

## 填充你的表格

要填充 `my_contacts` 表，请打开 http://127.0.0.1/contact_menu.php。如果你已经登录，将看到你的管理菜单。否则，使用用户名 (admin) 和密码 (abc123)。

- 1. 选择“添加联系人”菜单项。

你将看到一个包含许多添加联系人字段的空白表单，以及提交按钮和返回主菜单的链接。

- 2. 现在填写表单！只有两个字段是必填的（除非你自己更改了它们）：名和姓。下图显示了一个示例联系人。

- 3. 点击“添加联系人到系统”按钮。

你应该看到如所示的确认屏幕。

向系统添加几个自己的联系人。可以随意犯错，因为在下一章中，你将创建一组修改记录的脚本。





## 创建记录选择表单

你在 `my_contacts` 表中有许多条目，因此你需要一种快速方法来选择单条记录进行修改。下一个脚本将为数据库中的所有人员创建一个下拉菜单，你可以从从中选择一条记录进行修改。

- 在你的文本编辑器中打开一个新文件并开始 PHP 块，然后启动会话，或者如果会话已存在则继续使用：

```php
<?
session_start();
```

- 启动一个 if_else 块，检查 `$_SESSION['valid']` 的值并根据结果执行特定操作。如果值不是 yes，说明用户没有通过正确的身份验证通道：

```php
if ($_SESSION['valid'] != "yes") {
```

- 将用户送回登录表单并退出此脚本：

```php
header("Location: http://127.0.0.1/contact_menu.php");
exit;
}
```

- 创建变量来存储表所在的数据库名称以及表本身的名称：

```php
$db_name = "testDB";
$table_name = "my_contacts";
```

- 像之前的那样添加连接信息：

```php
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
```

- 像你学的那样选择数据库：

```php
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

- 创建 SQL 语句。你想选择表中每条记录的 ID 号、名和姓：

```php
$sql = "SELECT id, f_name, l_name FROM $table_name ORDER BY l_name";
```

- 8. 创建一个变量来存储 `mysql_query()` 函数的结果，像你学的那样：

```php
$result = @mysql_query($sql, $connection) or die(mysql_error());
```

- 9. 使用 `mysql_num_rows()` 函数检查是否有结果：

```php
$num = @mysql_num_rows($result);
```

- 10. 检查 `mysql_num_rows()` 函数返回的值，并创建一个名为 $display_block 的变量，如果数字小于 1（换句话说，如果表中没有行，因此表中没有记录）：

```php
if ($num < 1) {
    $display_block = "<p><em>抱歉！没有结果。</em></p>";
```

- 11. 继续 if...else 块，如果行数为 1 或更多，脚本将继续：

```php
} else
```

- 12. 启动 while 循环。while 循环将为结果集 ($result) 中的每条记录创建一个名为 $row 的数组：

```php
while ($row = mysql_fetch_array($result)) {
```

- 13. 获取记录的各个元素，并给它们起好名字：

```php
$id = $row['id'];
$f_name = $row['f_name'];
$l_name = $row['l_name'];
```

- 14. 创建名为 $option_block 的变量，它将包含下拉菜单中的各个元素：

```php
$option_block .= "<option value='$id'>$l_name, $f_name</option>";
```

- 15. 关闭 while 循环：

```php
}
```

- 16. 创建名为 display_block 的变量，它将持有表单。虽然该变量在第 10 步中被用于存储错误消息，但在没有错误的情况下它不会在该处使用。如果发生错误，脚本永远不会到达这一步，所以你不需要担心覆盖变量，可以开始创建你的表单。对于表单，假设方法为 POST，动作为脚本 `show_modcontact.php`：

```php
$display_block = '<FORM METHOD="POST" ACTION="show_modcontact.php">';
```

- 17. 为下拉菜单创建一个文本标签：

```html
<p><strong>联系人：</strong></p>
```

- 18. 启动下拉菜单：

```html
<select name="id">
```

- 19. 将 $option_block 字符串放在 <select> </select> 标签对内部。它应该至少包含一个 <option> 元素：

```php
$option_block
```

- 20. 完成下拉菜单：

```html
</select>
```

- 21. 添加提交按钮。然后，关闭你的表单字符串、if...else 块和 PHP 块：

```html
<INPUT TYPE="SUBMIT" NAME="submit" VALUE="选择此联系人*"></P>
</form>
}
?>
```

- 22. 添加此 HTML：

```html
<HTML>
<HEAD>
<TITLE>我的联系人管理系统：修改联系人</TITLE>
</HEAD>
<body
<h1>我的联系人管理系统</h1>
<h2><em>修改联系人 - 从列表中选择</em></h2>
<p>从下方的列表中选择一个联系人，以修改该联系人的记录。</p>
```

- 23. 显示 $display_block 的内容：

```php
<? echo $display_block; ?>
```

- 24. 添加一个返回主菜单的链接：

```html
<br><p><a href="contact_menu.php">返回主菜单</a></p>
```

- 25. 添加一些 HTML 以使文档有效：

```html
</body>
</html>
```

- 26. 将文件保存为 `pick_modcontact.php`，并将此文件放在服务器的文档根目录下。你的代码应该如下：

```php
<?php
//启动会话
session_start();

//检查用户有效性
if ($_SESSION['valid'] != "yes") {
    header("Location: http://127.0.0.1/contact_menu.php");
}

//设置表和数据库名称
$db_name = "testDB";
$table_name = "my_contacts";

//连接服务器并选择数据库
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
$db = mysql_select_db($db_name, $connection) or die(mysql_error());

//构建并查询
$sql = "SELECT id, f_name, l_name FROM $table_name ORDER BY l_name";
$result = @mysql_query($sql, $connection) or die(mysql_error());

//检查结果数量
$num = @mysql_num_rows($result);

if ($num < 1) {
  //如果没有结果，显示消息
  $display_block = "<em>抱歉！没有结果。</em>";
} else {
  //如果找到结果，遍历它们
  //并制作选择
  while ($row = mysql_fetch_array($result)) {
    $id = $row['id'];
    $f_name = $row['f_name'];
    $l_name = $row['l_name'];
    $option_block .= "<option value='$id'>$l_name, $f_name</option>";
  }

  //创建整个表单
  $display_block = "
<FORM METHOD=\"POST\" ACTION=\"show_modcontact.php\">
<P><strong>联系人：</strong></P>
<select name=\"id\">
$option_block
</select>
<INPUT TYPE=\"SUBMIT\" NAME=\"submit\" VALUE=\"选择此联系人\"></P>
</form>";
}
?>
<HTML>
<HEAD>
<TITLE>我的联系人管理系统：修改联系人</TITLE>
</HEAD>
<body>
<h1>我的联系人管理系统</h1>
<h2>修改联系人 - <em>从列表中选择</em></h2>
<p>从下方的列表中选择一个联系人，以修改该联系人的记录。</p>
<?php echo $display_block; ?>
<br>
<p><a href="contact_menu.php">返回主菜单</a></p>
</body>
</HTML>
```

## 修改记录表单

在下一节中，你将创建一个修改记录表单，它与添加记录表单非常相似。修改记录表单基于你在上一章创建的添加记录表单。区别在于表单字段填充。也就是说，如果记录已有数据，你可以在修改之前查看。

- 1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：

```php
<?php
```

- 2. 启动一个 if...else 块，检查 `$_POST['id']`（从记录选择表单发送的变量）。如果值不存在，该块将用户引导回选择表单并退出脚本：

```php
if (!$_POST['id']) {
    header("Location: http://127.0.0.1/pick_modcontact.php");
    exit;
}
```

- 3. 如果必需字段有值，你启动会话，或者如果会话已存在则继续。然后关闭块：

```php
} else {
    session_start();
}
```

- 4. 启动一个 if...else 块，检查 `$_SESSION['valid']` 的值并根据结果执行特定操作。如果值不是 yes，说明用户没有通过正确的身份验证通道：

```php
if ($_SESSION['valid'] != "yes") {
```

- 5. 将用户送回登录表单并退出此脚本：

```php
header("Location: http://127.0.0.1/contact_menu.php");
exit;
}
```

- 6. 创建变量来存储表所在的数据库名称以及表名称：

```php
$db_name = "testDB";
$table_name = "my_contacts";
```

- 7. 像之前的那样添加连接信息：

```php
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
```

- 8. 像你学的那样选择数据库：

```php
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

- 9. 创建 SQL 语句。你想选择数据库中除 ID 以外的所有字段，ID 等于 `$_POST['id']` 值的记录：

```php
$sql = "SELECT f_name, l_name, address1, address2, address3,
postcode, country, prim_tel, sec_tel, email, birthday
FROM $table_name WHERE id = '$_POST['id']";
```

> 注意
> 你可以简单的 SELECT * FROM $table_name WHERE id = '$_POST['id']'; 并且直接对数据库中生成的 id 值进行任何操作。

- 10. 创建一个变量来存储 `mysql_query()` 函数的结果，像你学的那样：

```php
$result = @mysql_query($sql, $connection) or die(mysql_error());
```

- 11. 启动 while 循环。while 循环将为结果集 ($result) 中的每条记录创建一个名为 $row 的数组：

```php
while ($row = mysql_fetch_array($result)) {
```

- 12. 获取记录的各个元素，并给它们起好名字：

```php
$f_name = $row['f_name'];
$l_name = $row['l_name'];
$address1 = $row['address1'];
```





# 创建记录修改表单 335

```php
$address2 = $row['address2'];
$address3 = $row['address3'];
$postcode = $row['postcode'];
$country = $row['country'];
$prim_tel = $row['prim_tel'];
$sec_tel = $row['sec_tel'];
$email = $row['email'];
$birthday = $row['birthday'];
```

## 注意

现在你已经有了所选记录的当前值，稍后将在脚本中使用这些值来填充表单字段。

- 13. 关闭 while 循环，然后关闭你的 PHP 块：

```php
}
?>
```

- 14. 输入此 HTML 开始构建记录修改表单：

```html
<HTML>
<HEAD>
<TITLE>我的联系人管理系统：修改联系人</TITLE>
</HEAD>
<BODY>
<h1>我的联系人管理系统</h1>
<h2><em>修改联系人</em></h2>
```

- 15. 开始你的表单。假设方法为 POST，动作动名为 `do_modcontact.php` 的脚本：

```html
<FORM METHOD="POST" ACTION="do_modcontact.php">
```

- 16. 添加一个隐藏字段来存储 `$_POST[id]` 的值，以便将其传递给脚本：

```html
<INPUT TYPE="hidden" name="id" value="<?php echo $_POST['id']; ?>">
```

# 336 第 20 章：修改联系人

- 17. 开始一个 HTML 表格以辅助布局。开始新的一行，添加两个列标题，并关闭该行：

```html
<table cellspacing="3" cellpadding="5">
<tr>
<th>姓名与地址信息</th>
<th>其他联系/个人信息</th>
</tr>
```

- 18. 创建行和单元格来存放记录中所有项的输入字段。在每个输入字段中使用 `value` 属性，并混合 HTML 和 PHP 来输出实际值：

```html
<tr>
<td valign="top">
<P><strong>姓：</strong><BR>
<INPUT TYPE="text" NAME="f_name" VALUE="<?php echo "$f_name"; ?>" 
SIZE=35 MAXLENGTH=75</P>
<P><strong>名：</strong><BR>
<INPUT TYPE="text" NAME="l_name" VALUE="<?php echo "$l_name"; ?>" 
SIZE=35 MAXLENGTH=75</P>
<P><strong>地址行 1：</strong><BR>
<INPUT TYPE="text" NAME="address1" VALUE="<?php echo "$address1"; ?>" 
SIZE=35 MAXLENGTH=100</P>
<P><strong>地址行 2：</strong><BR>
<INPUT TYPE="text" NAME="address2" VALUE="<?php echo "$address2"; ?>" 
SIZE=35 MAXLENGTH=100</P>
<P><strong>地址行 3：</strong><BR>
<INPUT TYPE="text" NAME="address3" VALUE="<?php echo "$address3"; ?>" 
SIZE=35 MAXLENGTH=100</P>
<P><strong>邮政编码：</strong><BR>
<INPUT TYPE="text" NAME="postcode" VALUE="<?php echo "$postcode"; ?>" 
SIZE=35 MAXLENGTH=25</P>
<P><strong>国家：</strong><BR>
<INPUT TYPE="text" NAME="country" VALUE="<?php echo "$country"; ?>" 
SIZE=35 MAXLENGTH=100</P>
</td>
<td valign="top">
<P><strong>主电话号码：</strong><BR>
<INPUT TYPE="text" NAME="prim_tel" VALUE="<?php echo "$prim_tel"; ?>" 
SIZE=35 MAXLENGTH=35</P>
<P><strong>次电话号码：</strong><BR>
```

```html
<INPUT TYPE="text" NAME="sec_tel" VALUE="<?php echo "$sec_tel"; ?>">
SIZE=35 MAXLENGTH=35></p>
<P><strong>电子邮箱地址：</strong><BR>
<INPUT TYPE="text" NAME="email" VALUE="<?php echo "$email"; ?>">
SIZE=35 MAXLENGTH=100></p>
<P><strong>生日 (YYYY-MM-DD)：</strong><BR>
<INPUT TYPE="text" NAME="birthday" VALUE="<?php echo "$birthday"; ?>">
SIZE=10 MAXLENGTH=10></p>
</td>
</tr>
```

- 19. 开始一个新行和跨两列的表格单元格。在内部添加提交按钮以及一个返回主菜单的链接。关闭表格数据单元格、表格行和表格本身：

```html
<tr>
<td align="center" colspan="2"><br>
<P><INPUT TYPE="SUBMIT" NAME="submit" VALUE="更新联系人记录"></P>
<br>
<p><a href="contact_menu.php">返回主菜单</a></p>
</td
</tr>
</TABLE>
```

- 20. 关闭你的表单并添加一些额外的 HTML 以确保文档有效：

```html
</FORM>
</BODY>
</HTML>
```

- 21. 将文件保存为 `show_modcontact.php`，并将其放在 Web 服务器的根目录下。

在下一节，你创建一个获取表单输入、创建 SQL 语句并更新数据库中记录的脚本。

## 创建修改脚本

此脚本将使用 `$_POST[id]` 的值作为主键更新 `my_contacts` 表中的记录。338 第20 章：修改联系人

- 1. 在文本编辑器中打开一个新文件并开始 PHP 块：

```php
<?php
```

- 2. 开始一个 `if...else` 块来检查 `$_POST[f_name]` 和 `$_POST[l_name]`。如果它们没有值，将用户引导回选择表单：

```php
if ($_POST['f_name'] || $_POST['l_name']) {
    header("Location: http://127.0.0.1/pick_modcontact.php");
} // 注意：你可以有许多（或少数）必填字段，但要求应与添加表单的字段匹配。

- 3. 如果必填字段有值，启动会话或继续。关闭该块：

```php
} else {
    session_start();
```

- 4. 开始一个 `if...else` 块检查 `$_SESSION['valid']` 的值并根据结果执行特定操作。如果值不是 yes，则用户没有通过正确的渠道：

```php
if ($_SESSION['valid'] != "yes") {
```

- 5. 将用户返回登录表单并退出脚本：

```php
header("Location: http://127.0.0.1/contact_menu.php");
exit;
```

- 6. 创建变量存储数据库名称以及表本身：

```php
$db_name = "test";
$table_name = "my_contacts";
```

- 7.按照你学过的添加连接信息：

```php
$connection = @mysql_connect("localhost", "root", "") or die(mysql_error());
```

- 8. 按照你学过的选择数据库：

```php
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

- 9. 创建 SQL 语句。该语句使用 `UPDATE` 设置特定值：

```php
$sql = 'UPDATE $table_name SET
f_name = '$_POST['f_name'],
l_name = '$_POST['l_name'],
address1 = '$_POST['address1'],
address2 = '$_POST['address2'],
address3 = '$_POST['address3'],
postcode = '$_POST['postcode'],
country = '$_POST['country'],
prim_tel = '$_POST['prim_tel'],
sec_tel = '$_POST['sec_tel'],
email = '$_POST['email'],
birthday = '$_POST['birthday']
WHERE id = '$_POST['id']';
```

- 10. 按照你学过的创建一个变量存储 `mysql_query()` 函数的结果：

```php
$result = @mysql_query($sql, $connection) or die(mysql_error());
```

- 11. 关闭你的 PHP 块并添加此 HTML：

```php
?>
<HTML>
<HEAD>
<TITLE>我的联系人管理系统：联系人已更新</TITLE>
</HEAD>
<body>
<h1>我的联系人管理系统</h1>
<h2><em>修改联系人 - 联系人已更新</em></h2>
```

# 340 第 20 章：修改联系人

- 12. 添加一个确认语句。混合 HTML 和 PHP 以包含 `$table_name` 变量的值：

```html
<P>以下信息已成功更新至 <?php echo "$table_name"; ?></P>
```

- 13. 接下来，你在 `show_modcontact.php` 中重新创建布局，但不再包含表单字段。相反，你将混合 HTML 和 PHP 来显示输入的值。开始新的一行，添加两个列标题，然后关闭该行：

```html
<table cellspacing="3" cellpadding="5">
<tr>
<th>姓名与地址信息</th>
<th>其他联系/个人信息</th>
</tr>
```

- 14. 开始新的一行和表格数据单元格，然后为每个字段显示标签和值：

```html
<td valign="top">
<P><strong>姓：</strong><BR>
<?php echo $_POST["f_name"]; ?></P>
<P><strong>名：</strong><BR>
<?php echo $_POST["l_name"]; ?></P>
<P><strong>地址行 1：</strong><BR>
<?php echo $_POST["address1"]; ?></P>
<P><strong>地址行 2：</strong><BR>
<?php echo $_POST["address2"]; ?></P>
<P><strong>地址行 3：</strong><BR>
<?php echo $_POST["address3"]; ?></P>
<P><strong>邮政编码：</strong><BR>
<?php echo $_POST["postcode"]; ?></P>
<P><strong>国家：</strong><BR>
<?php echo $_POST["country"]; ?></P>
</td>
<td valign="top">
<P><strong>主电话号码：</strong><BR>
<?php echo $_POST["prim_tel"]; ?></P>
<P><strong>次电话号码：</strong><BR>
<?php echo $_POST["sec_tel"]; ?></P>
<P><strong>电子邮箱地址：</strong><BR>
<?php echo $_POST["email"]; ?></P>
<P><strong>生日 (YYYY-MM-DD)：</strong><BR>
<?php echo $_POST["birthday"]; ?></P>
</td>
</tr>
```





## 第 20 章：修改联系人

你将看到一个系统中联系人的下拉菜单，按姓排序，并包含一个提交按钮和一个返回主菜单的链接。

## 我的联系人管理系统

### 修改联系人 - 从列表中选择

从下方列表中选择一个联系人以修改该联系人的记录。

联系人：[Jane v]

- 2. 从列表中选择一个联系人并点击“选择联系人”按钮。我从自己的列表中选择了一个示例。这是一个完整的示例，每个字段都有值。

返回主菜单

你将看到记录修改表单，表单字段已填充了现有值。

## 我的联系人管理系统

### 修改联系人

- 3. 修改记录中的某些内容。在我的示例中，我将“地址行 2”（Address Line 2）改为 92-A，并将“主电话”（Primary Telephone Number）改为 555-444-1111。点击“更新联系人记录”按钮。你应该会在下一页看到一个确认屏幕。

## 修改联系人 343

4. 返回选择表单并再次选择你的联系人，以查看值是否真的已更改：

修改你自己的某些联系人的记录。在下一章中，你将创建用于删除记录的管理脚本。

## 21 删除联系人

在许多时候，由于某种或其他原因，我想从地址录中删除某些人员。你也应该能够从你的在线联系人管理系统中删除人员！在本章中，你将学习如何：

- 创建一个删除记录的管理界面
- 创建一个脚本从你的表中删除记录
- 在查看脚本或删除记录之前要求进行基于会话（session）的验证

## 使用记录选择表单

用于创建删除记录选择表单的脚本与用于选择记录进行修改的脚本几乎相同。这部分你将很容易快速浏览。重复造完美！

- 1. 在文本编辑器中打开一个新文件并开始一个 PHP 块。然后，启动会话，如果当前存在会话则继续该会话：

```php
<?
session_start();
```

- 2. 开始一个 if_else 块，检查 $_SESSION['valid'] 的值并根据结果执行特定操作。如果值不是 yes，说明用户没有通过适当的验证通道：

```php
if ($_SESSION['valid'] != "yes") {
```

- 3. 将用户送回登录表单并退出此脚本：

```php
header("Location: http://127.0.0.1/contact_menu.php");
exit;
}
```

- 4. 创建变量来存储表所在的数据库名称以及表本身：

```php
$db_name = "testDB";
$table_name = "my_contacts";
```

- 5. 像你之前那样添加连接信息：

```php
$connection = @mysql_connect("localhost", "spike", "9sj7En4") or die(mysql_error());
```

- 6. 像你学的那样选择数据库：

```php
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

- 7. 创建 SQL 语句。你想选择表中每条记录的 ID、名和姓：

```php
$sql = "SELECT id, f_name, l_name FROM $table_name ORDER BY l_name";
```

- 8. 创建一个变量来存储 mysql_query() 函数的结果，像你学的那样：

```php
$result = @mysql_query($sql, $connection) or die(mysql_error());
```

- 9. 使用 mysql_num_rows() 函数检查结果：

```php
$num = @mysql_num_rows($result);
```

- 10. 检查 mysql_num_rows() 函数返回的值，如果数字小于 1，则创建一个名为 $display_block 的变量来存储错误信息（换句话说，如果表中没有行，因此表中没有记录）。

```php
if ($num < 1) {
  $display_block = "<p><em>Sorry! No results.</em></p>";
```

- 11. 继续 if...else 块，如果行数等于 1 或更多，脚本将继续执行：

```php
} else {
```

- 12. 开始 while 循环。while 循环将为结果集（result）中的每条记录创建一个名为 $row 的数组：

```php
while ($row = mysql_fetch_array($result)) {
```

- 13. 获取记录的各个元素，并给它们起好名字：

```php
$id = $row['id'];
$f_name = $row['f_name'];
$l_name = $row['l_name'];
```

- 14. 创建名为 $display_block 的变量，它将包含各个元素：

```php
$option_block .= "<option value=\"$id\">$l_name, $f_name</option>";
```

- 15. 关闭 while 循环：

```php
}
```

- 16. 创建名为 $display_block 的变量，它将存储错误信息：

```php
$display_block = "";
```

- 17. 放置下拉菜单：

```php
$option_block =
```

- 18. 开始下拉菜单：

```php
<select name="
```

- 19. 关闭下拉菜单：

```php
</select>
```

- 20. 完成下拉菜单：

```php
$option_block =
```

- 21. 添加提交按钮：

```php
<INPUT TYPE="SUBMIT" NAME="submit">
```

- 22. 关闭字符串：

```php
}
```

- 23. 添加此 HTML：

```php
<HTML>
<HEAD>
<TITLE>My Contact System: Delete a Contact</TITLE>
</HEAD>
```

- 24. 显示 $display_block 的内容：

```php
echo $display_block; ?>
```

- 25. 添加返回主菜单的链接：

```php
<br><a href="contact_menu.php">Return to Main Menu</a>
```





</BODY>
</HTML>

在下一节中，你将创建一个删除前的确认屏幕，显示选中记录的所有当前值。

## 创建删除表单

删除表单并不是通常意义上的表单——你不需要在表单字段中输入任何内容。相反，此屏幕将以只读格式显示现有记录，并包含隐藏的表单字段和一个提交按钮。通过在删除之前查看记录，你可以确保删除的是正确的记录。

- 1. 在你的文本编辑器中打开一个新文件，并开始一个 PHP 块：
```php
<?php
```

- 2. 启动一个 if...else 块来检查 $_POST[id] 的值，这是从记录选择表单发送的唯一变量。如果值不存在，则将用户重定向选择表单并退出脚本：

```php
if ($_POST['id']) {
    header("Location: http://127.0.0.1/pick_delcontact.php");
    exit;
}
```

- 3. 如果必需字段有值，启动会话，或者如果当前已存在则继续。然后关闭该块：

```php
else {
    session_start();
}
```

- 4. 启动一个 if...else 块检查 $_SESSION[valid] 的值并根据结果执行特定操作。如果值不是 yes，则用户没有通过适当的验证通道：

```php
if ($_SESSION['valid'] != "yes") {
```

- 5. 将用户送回登录表单和脚本：

```php
header("Location: http://127.0.0.1/contact_menu.php");
exit;
```

- 6. 创建变量来存储存储表的数据库名称以及表本身：

```php
$db_name = "testDB";
$table_name = "my_contacts";
```

- 7. 按照你之前的方法添加连接信息：

```php
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
```

- 8. 选择你学过的数据库：

```php
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

- 9. 创建 SQL 语句。你想选择数据库中的所有字段，但 id 等于 $_POST[id] 值的记录：

```php
$sql = "SELECT f_name, l_name, address1, address2, address3,
postcode, country, prim_tel, sec_tel, email, birthday
FROM $table_name WHERE id = '$_POST['id']';";
```

- 10. 创建一个变量来存储 mysql_query() 函数的结果，如你学过的：

```php
$result = @mysql_query($sql, $connection) or die(mysql_error());
```

- 11. 启动 while 循环。while 循环将结果集 ($result) 中的每条记录创建一个名为 $row 的数组：

```php
while ($row = mysql_fetch_array($result)) {
```

- 12. 获取记录的各个元素，并给它们起好名字：

```php
$f_name = $row['f_name'];
$l_name = $row['l_name'];
$address1 = $row['address1'];
$address2 = $row['address2'];
```

```php
$address3 = $row['address3'];
$postcode = $row['postcode'];
$country = $row['country'];
$prim_tel = $row['prim_tel'];
$sec_tel = $row['sec_tel'];
$email = $row['email'];
$birthday = $row['birthday'];
```

- 13. 关闭 while 循环，然后关闭你的 PHP 块：

```php
}
?>
```

- 14. 输入此 HTML 开始构建记录确认屏幕：

```html
<HTML>
<HEAD>
<TITLE>我的联系人管理系统：删除联系人</TITLE>
</HEAD>
<body>
<h1>我的联系人管理系统</h1>
<h2><em>删除联系人</em></</h2>>
```

- 15. 开始你的表单。假设方法为 POST，action 是名为 do_delcontact.php 的脚本：

```html
<FORM METHOD="POST" ACTION="do_delcontact.php">
```

- 16. 添加一个隐藏字段来存储 $_POST[id] 的值：

```html
<INPUT TYPE="hidden" name="id" value="<?php echo $_POST['id']; ?>"?>
```

- 17. 添加另外两个隐藏字段来存储 $_f_name 和 $_l_name 的值。你将在删除后的最终确认屏幕中使用这些字段：

```html
<INPUT TYPE="hidden" name="f_name" value="<?php echo $f_name; ?>">
<INPUT TYPE="hidden" name="l_name" value="<?php echo $l_name; ?>">
```

- 18. 接下来，你将重新创建添加和修改表单中使用的布局，混合 HTML 和 PHP 来显示记录的值。启动一个新的表格行，添加两个列标题：

```html
<table cellspacing=3>
<tr>
<th>姓名和地址信息</th>
<th>其他联系人/个人信息</th>
</tr>
```

- 19. 启动一个新的表格行和数据单元格，然后显示记录中的文本标签和值：

```html
<tr>
<td valign=top>
<p><strong>名：</strong><br>
<?php echo "$f_name"; ?></p>
<p><strong>姓：</strong><br>
<?php echo "$l_name"; ?></p>
<p><strong>地址 1：</strong><br>
<?php echo "$address1"; ?></p>
<p><strong>地址 2：</strong><br>
<?php echo "$address2"; ?></p>
<p><strong>地址 3：</strong><br>
<?php echo "$address3"; ?></p>
<p><strong>邮政编码：</strong><br>
<?php echo "$postcode"; ?></p>
<p><strong>国家：</strong><br>
<?php echo "$country"; ?></p>
</td>
<td valign=top>
<p><strong>主电话：</strong><br>
<?php echo "$prim_tel"; ?></p>
<p><strong>次电话：</strong><br>
<?php echo "$sec_tel"; ?></p>
<p><strong>邮箱：</strong><br>
<?php echo "$email"; ?></p>
<p><strong>生日：</strong><br>
<?php echo "$birthday"; ?></p>
</td>
</tr>
```

- 20. 启动一个新的跨两列的表格行和数据单元格。在内部，添加提交按钮和返回菜单的链接。关闭单元格、行：

```html
<tr>
<td align=center>
<input type="submit" name="submit" value="删除">
<p><a href="contact_menu.php">返回菜单</a></p>
</td>
</tr>
</table>
```

- 21. 关闭表单并添加一些 HTML 使文档有效：

```html
</FORM>
</body>
</HTML>
```

- 22. 将文件保存为 del_delcontact.php，并将此文件放置在 Web 服务器的根目录下。



```php
exit;
}

//设置表和数据库名称
$db_name = "testDB";
$table_name = "my_contacts";
```

```php
//连接服务器并选择数据库
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

```php
//构建并执行查询
$sql = "DELETE FROM $table_name WHERE id = '$POST[id]";
```

```php
$result = @mysql_query($sql, $connection) or die(mysql_error());
?>
<HTML>
<HEAD>
<TITLE>我的联系人管理系统：联系人已删除</TITLE>
</HEAD>
<BODY>
<h2><em>删除联系人 - 联系人已删除</em></h2>
<p><?php echo "$_POST[f_name] $_POST[l_name]"; ?> 已从 <?php echo "$table_name"; ?> 中删除</p>
<br><p><a href="contact_menu.php">返回主菜单</a></p>
</body>
</HTML>
```

继续下一步，从你的数据库表删除删除掉一些联系人。

## 删除联系人

要从 my_contacts 表中删除删除人，请打开 http://127.0.0.1/contact_menu.php。如果你已经登录，将看到管理菜单。否则，请使用用户名 (admin) 和密码 (abc123) 登录。

- 1. 选择“删除联系人”选项。

## 删除联系人

![](img/be897bd1bfd4dab38767db24da2a794b_381_0.png)

你将看到系统中所有联系人的下拉菜单，以及一个提交按钮和一个返回主菜单的链接。

- 2. 从列表中选择一个联系人并点击“选择此联系人”按钮。我从自己的列表中选择了一个示例。

![](img/be897bd1bfd4dab38767db24da2a794b_381_1.png)

> 注意
显示记录中的生日显示为 0000-00-00，因为原始记录中没有输入日期。MySQL 为日期字段使用默认日期。

- 3. 点击“删除联系人”按钮。你应该看到一个确认屏幕。

## 第 21 章：删除联系人

![](img/be897bd1bfd4dab38767db24da2a794b_382_0.png)

- 4. 返回选择表单并再次选择你的联系人，确认该记录已不再出现在下拉菜单中。

删除一两个记录，然后进入下一章，在下一章中你将创建只读的联系人信息屏幕。

## 处理联系人

你在表格中拥有所有这些信息，但我还没有向你展示如何创建任何用于选择和显示只读数据的脚本。是时候纠正这一点了！在本章中，你将学习如何：

- 统计并显示系统中的联系人数量
- 显示当前日期
- 检查本月的生日并显示特殊文本
- 显示只读的联系人详情
- 在查看脚本或删除记录之前要求基于会话的身份验证

## 修改你的管理菜单

接下来的几部分将展示你可以对原始 contact_menu.php 进行的一些修改，以显示诸如当前日期、数据库中的联系人数量以及使你的系统定制化的其他信息。

## 显示联系人数量

应对对 contact_menu.php 脚本进行以下修改，以便显示 my_contacts 表中当前的联系人数量。

- 1. 在你的文本编辑器中打开 contact_menu.php。

- 2. 找到这段代码，将其高亮并从文件中剪切（准备好粘贴）：

```php
//构建表单块
$form_block = "<h1>Login</h1>
<form method="POST" action=\$SERVER[PHP_SELF]">
<p><strong>username:</strong><br>
<input type="text" name=\"username" size=15 maxlength=25></p>
<p><strong>password:</strong><br>
<input type="password" name=\"password" size=15 maxlength=25></p>
<input type="hidden" name=\"op" value="ds">
<p><input type="submit" name=\"submit" value=\"login"></p>
</FORM>;
```

- 3. 找到类似下面的 if...else 块：

```php
if ($show_form == "yes") {
    $display_block = $form_block;
} else if ($show_menu == "yes") {
    $display_block = $menu_block;
}
```

- 4. 用你在第 2 步中剪切的部分替换以下行：

```php
$display_block = $form_block;
```

## 修改你的管理菜单

现在 if...else 块应该看起来像这样：

```php
if ($show_form == "yes") {
  $form_block = <html>Login</html>
  <form method="POST" action=$_SERVER[PHP_SELF]">
  $msg
  <P><strong>username:</strong><br>
  <input type="text" name=\"username" size=15 maxlength=25></P>
  <p><strong>password:</strong><br>
  <input type="password" name=\"password" size=15 maxlength=25></P>
  <input type="hidden" name=\"op" value=\"ds\">
  <P><input type="submit" name=\"submit" value=\"login"></P>
} else if ($show_menu == "yes") {
  $display_block = $menu_block;
}
```

- 5. 将变量名从 $form_block 改为 $display_block。

- 6. if...else 块应该像这样：

```php
if ($show_form == "yes") {
  //构建块
  $display_block = <html>Login</html>
  <form method="POST" action=$_SERVER[PHP_SELF]">
  $msg
  <P><strong>username:</strong><br>
  <input type="text" name=\"username" size=15 maxlength=25></P>
  <p><strong>password:</strong><br>
  <input type="password" name=\"password" size=15 maxlength=25></P>
  <input type="hidden" name=\"op" value=\"ds\">
  <P><input type="submit" name=\"submit" value=\"login"></P>
}
```

- 7. 找到以下代码，将其高亮并从文件中剪切（准备好粘贴）：

```php
$form_block = "<h1>Login</h1

```

- 8. 找到以下 if...else 块：

```php
$ _block = blockblock;
```

- 9. 替换以下行：

```php
if ($show_form == "yes") {
  $display_block = "<h>Login</html>
  <form method="POST" action=$_SERVER[PHP_SELF

  $msg
  <P><strong>username:</strong><br>
  <input type="text" name=\"username" size=15 maxlength=25></P>
  <p><strong>password:</strong><br>
  <input type="password" name=\"password" size=15 maxlength=25></P>
  <input type="hidden" name=\"op" value=\"ds">
  <P><input type="submit" name=\"submit" value=\"login"></P>
</form>
``` 
    

 (注：由于原文提供的文本在第7-12步之间存在逻辑混乱和代码重复，译文已根据 Markdown 结构对内容进行了对齐，确保了操作步骤的连贯性)





接下来的更改都将发生在你刚刚修改的 if...else 块的第二部分。

- 1. 找到这一行，因为其余的更改都紧跟随其后：

```php
} else if ($show_menu == "yes") {
```

- 2. 创建变量来存储表所所在的数据库名称，以及表本身：

```php
$db_name = "testDB";
$table_name = "my_contacts";
```

- 3.按照你学的方法添加连接信息：

```php
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
```

- 4. 按照你学的方法选择数据库：

```php
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

- 5. 创建一个 SQL 语句来统计 id 字段中的条目数：

```php
$sql = "SELECT count(id) FROM $table_name";
```

- 6. 按照你学的方法，创建一个变量来存储 mysql_query() 函数的结果：

```php
$result = @mysql_query($sql, $connection) or die(mysql_error());
```

- 7. 创建一个变量来存储结果中的特定值：

```php
$count = @mysql_result($result, 0, "count(id)") or die(mysql_error());
```

> 注意
如果你正在处理的是单字段结果，mysql_result() 函数比获取整行要简单。此函数需要一个有效查询的结果、行号（从 0 开始）以及字段名。

# 修改你的管理菜单 367

8. 下一个修改主要是为了美观。获取 $display_block 内的字符串，并将其替换为以下 HTML，为菜单创建一个双列表格：

```php
$display_block = "<h1>My Contact Management System</h1>";
```

```html
<table cellspacing=3 cellpadding=3>
<tr>
<td valign=top>
<p><<strong>>管理</</strong>></p>
<ul>
<li><a href="show_addcontact.php">添加联系人/</a>
<li><a href="pick_modcontact.php">修改联系人/</a>
<li><a href="pick_delcontact.php">删除联系人/</a>
</ul>
<p>查看记录</p>
<ul>
<li><a href="show_contactsbyname.php">按姓名显示联系人/</a>
</ul>
</td>
<td valign=top>
<p><<strong>其他</</strong>></p>
</td>
</tr>
</</table>";
```

9. 在新的 $display_block 字符串中，找到“其他”（Miscellaneous）部分。开始一个无序列表，然后打印一个带有文本标签和 $count 值的**加粗表示**的列表项。在该列表项之后，关闭该列表：

```html
<ul>
<li>系统中的联系人：<strong>$count</strong></li>
</ul>
```

10. 保存你的更改。

你的新代码看起来应该像这样：

```php
<?php
//启动会话
session_start();
```

# 368 第 22 节：处理联系人

```php
// 检查用户是否来自表单
if ($_POST['op'] == "ds") {
    // 检查用户名和密码
    if ($_POST['username'] != "admin" || ($_POST['password'] != "abc123")) {
        // 处理登录失败
        $msg = "<font color='#FF0000>
<<strong>登录失败 - 请重试</</strong>>\n</font></p>";
        $show_form = "yes";
    } else {
        // 处理登录成功
        $_SESSION['valid'] = "yes";
        $show_menu = "yes";
    }
} else {
    // 决定显示什么
    if ($_SESSION['valid'] == "yes") {
        $show_menu = "yes";
    } else {
        $show_form = "yes";
    }
}
// 将要显示的块赋值给 $display_block 变量
if ($show_form == "yes") {
    // 构建块
    $display_block = "<h>登录
<form method=\"POST\" action=\"$_SERVER['SELF']\">
    $msg
    <p><strong>用户名：</strong>><br>
    <input type=\"text\" name=\"username\" size=15 maxlength=25></p>
    <p><strong>密码：</strong>><br>
    <input type=\"password\" name=\"password\" size=15 maxlength=25></p>
    <input type=\"hidden\" name=\"op\" value=\"ds\">
    <p><input type=\"submit\" name=\"submit\" value=\"login\"></p>
</form>";
} else if ($show_menu == "yes") {
    // 设置表和数据库名
    $db_name = "testDB";
    $table_name = "my_contacts";
}
// 连接服务器并选择数据库

# 修改你的管理菜单 369

```php
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

```php
// 构建块并执行查询
$sql = "SELECT count(id) FROM $table_name";
$result = @mysql_query($sql,$connection) or die(mysql_error());
$count = @mysql_result($result,0,"count(id)") or die(mysql_error());
```

```php
// 构建菜单
$display_block = "<html> 联系人管理系统</html>
<table cellspacing=3 cellpadding=3>
<tr>
<td valign="top">
<p><strong>管理</</strong>></p>
<ul>
<li><a href="show_addcontact.php">添加联系人/</a>
<li><a href="pick_modcontact.php">修改联系人/</a>
<li><a href="pick_delcontact.php">删除联系人/</a>
</ul>
<p>查看记录</p>
<ul>
<li><a href="show_contactsbyname.php">按姓名显示联系人/</a>
</ul>
</td>
<td valign="top">
<p><strong>其他</</strong>></p>
<ul>
<li>系统中的联系人：<strong>$count</strong></li>
</ul>
</td>
</tr>
</table>?>
<html
<HEAD>
<TITLE>我的管理系统</TITLE>
</HEAD>
<body>";
```

```php
<?php echo "$display_block"; ?>
<body>
</html>
```

打开 http://127.0.0.1/contact_menu.php。如果你已经登录，将看到你的管理菜单。否则，使用用户名 (admin) 和密码 (abc123) 登录。你现在应该在适当的位置看到新的菜单布局以及联系人的数量。

在下一节中，你将在菜单上显示当前日期。

## 显示今天的日期

与上一节相比，显示当前日期的更改轻而易举！一旦你了解所有选项，date() 函数是高度自定义的。

## 注意

你可以在附录 B“基础语言参考”中找到 date() 函数选项列表。

- 1. 在文本编辑器中打开 contact_menu.php。

- 2. 找到这一行，因为其余的更改在这个块中：
} else if ($show_menu == "yes") {

- 3. 在给 $count 变量赋值的行之后，添加此行创建一个创建一个 $today 的变量，包含一个格式化的日期字符串：
$today = date("l, F j, Y");

- 4. 在 $display_block 字符串中找到这一行：
<h1>My Contact Management System</h1>

- 5. 在它之后，添加以下内容以打印日期字符串：
<p><em>Today is $today</em></p>

- 6. 保存你的文件。

日期格式选项的解释如表 22.1 所示。

| 表 22.1 日期格式示例 | |
| --- | --- |
| 格式选项 | 说明 |
| l, | 星期全称（字面逗号） |
| F | 月份全称 |
| j | 日期（两位） |
| S | 序数后缀 |
| Y | 年份（四位数） |

## 第 22 节：处理联系人

打开 http://127.0.0.1/contact_menu.php。如果你已经登录，将看到你的管理菜单。否则，使用用户名 (admin) 和密码 (abc123) 登录。你现在应该看到一行显示“Today is [你的日期]”的文本。

在下一节中，你需要一些 SQL 来找到生日在本月内的联系人数量，你将在列表中打印他们的名字。

## 显示本月的生日

数据库中的字段之一是人的生日字段。这不是强制要求的，但如果你花时间输入了某人的生日，你可能想记住它。接下来的部分将打印本月生日的联系人的姓名、生日以及其联系信息的链接。太棒了！

- 1. 在文本编辑器中打开 contact_menu.php。

- 2. 找到这一行，因为其余的更改在这个块中：
} else if ($show_menu == "yes") {

- 3. 在给 $count 变量赋值的行之后，添加此行来创建一个名为 $today 的变量，包含一个格式化的日期字符串：
$today = date("l, F j, Y");

- 4. 创建一个获取本月生日人数的 SQL 语句：

```php
$birthday_count = "SELECT count(id) FROM $table_name
WHERE MONTH(birthday) = MONTH(NOW())";
```

## 注意

MONTH() 和 NOW() 是 MySQL 函数，分别从日期字符串（在此例中为生日字段的值）和当前日期提取月份。你可以在附录 D“数据库规范化和 SQL 参考”中了解更多关于 MySQL 函数的信息。

```php
$birthday_count_res = @mysql_query($birthday_count, $connection)
or die(mysql_error());
```

```php
$birthday_count = mysql_result($birthday_count_res, 0,"count(id)");
```

接下来，你将在 SQL 上玩一玩。如果本月生日的联系人有一个或多个，你将创建一个包含该联系人姓名、生日以及其联系信息的字符串。

你稍后会在 while 块中创建一个无序列表。现在先在 while 块之外开始无序列表：




3. 创建一个 SQL 语句，选择 ID、名字、姓氏、生日月份以及日期。此 SQL 语句还根据生日对结果集进行排序：

```php
$get_contacts_bd = "SELECT id, f_name, l_name,
MONTH(birthday) as month, DAYOFMONTH(birthday) as date
FROM $table_name WHERE
MONTH(birthday) = MONTH(NOW()) ORDER BY birthday";
```

## 注意

你可以在 SQL 语句中选择字段或字段的一部分，并使用 `[new name]` 为它们重新分配一个新名称。在上一个语句中，你提取生日的月份并将其命名为 `month`，提取生日的日期并将其命名为 `date`。

4. 创建一个变量来存储 `$mysql_query()` 函数的结果，正如你所学过的：

```php
$contacts_bd_res = @mysql_query($get_contacts_bd, $connection)
or die(mysql_error());
```

5. 启动 while 循环。循环将为结果集 ($contacts_bd_res) 中的每条记录创建一个名为 $contacts_bd 的数组：

```php
while ($contacts_bd = mysql_fetch_array($contacts_bd_res)) {
```

6. 获取记录的各个元素，并为它们起好名字：

```php
$contacts_id = $contacts_bd['id'];
$contacts_fname = $contacts_bd['f_name'];
$contacts_lname = $contacts_bd['l_name'];
$contacts_bd_month = $contacts_bd['month'];
$contacts_bd_date = $contacts_bd['date'];
```

7. 向 $bd_string 中追加一个包含人员姓名和生日的列表项。创建一个指向 `show_contacts.php` 脚本的链接，该脚本将在后续章节中创建：

```php
$bd_string .= "<<li<a
ref="show_contacts.php?id=$contacts_id">$contact_fname
$contact_lname</a ($contacts_bd_month)."-".$contact_bd_date"></li>";
```

8. 关闭 while 循环，然后关闭项目列表，最后关闭 if 语句：

```php
}
$bd_string .= "</</ul>";
}
```

9. 在 $display_block 内部，在“杂”（Miscellaneous）标题下的项目列表，以及“本月生日”列表项下，添加以下内容：

```php
$bd_string
```

10. 保存你的文件。

最终的 `contact_menu.php` 脚本应该如下所示，包含了本章为止的所有修改：

```php
<?
//启动会话
session_start();

//检查用户是否来自表单
if ($_POST['op'] == "ds") {

  //检查用户名和密码
  if ($_POST['username'] != "admin") || ($_POST['password'] != "abc123")) {
    $msg = "<font color=#FF0000"><p>登录失败，请重试</font></p>";
    $show_form = "yes";
  } else {
    //处理合合的登录
    $_SESSION['valid'] = "yes";
    $show_menu = "yes";
  }
} else {
//确定要显示的内容
if ($_SESSION['valid'] == "yes") {
  $show_menu = "yes";
} else {
  $show_form = "yes";
}
```

# 376 第 22 章：处理联系人

```php
}
//将构建的表单赋值给 $display_block 变量
if ($show_form == "yes") {
    //构建表单块
    $display_block = "<h1>登录</h1>";
    "<form method=POST action=$_SERVER['PHP_SELF']\">
    $msg
    <P>username:</small><br>
    <input type="text" name="username" size=15 maxlength=25></P>
    <P>password:</small><br>
    <input type="password" name="password" size=15 maxlength=25></P>
    <input type="hidden" name="op" value="ds">
    <input type="submit" name="login"></P>
    </FORM>";
} else if ($show_menu == "yes") {
    //设置表和数据库名
    $db_name = "testDB";
    $table_name = "my_contacts";

    //连接到服务器和数据库
    $connection = @mysql_connect("localhost", "spike", "9sj7En4")
    or die(mysql_error());
    $db = @mysql_select_db($db_name, $connection) or die(mysql_error());

    //构建并执行查询
    $sql = "SELECT count(id) FROM $table_name";
    $result = @mysql_query($sql,$connection) or die(mysql_error());
    $count = mysql_result($result,0, "count(id)") or die(mysql_error());

    //获取当前日期
    $today = date("l, F, Y");

    //获取生日计数
    $get_birthday_count = "SELECT count(id) FROM $table_name
    WHERE MONTH(birthday) = MONTH(NOW());";
    $birthday_count_res = @mysql_query($get_birthday_count,$connection)
    or die(mysql_error());
    $birthday_count = mysql_result($birthday_count_res, 0, "count(id)");

    //根据正数创建列表
    if ($birthday_count > 0) {
      $bd_string = "<ul>";
      $get_contacts_bd = "SELECT id, f_name, l_name,
MONTH(birthday) as month, DAYOFMONTH(birthday) as day
FROM $table_name
WHERE MONTH(birthday) = MONTH(NOW()) ORDER BY birthday";
      $contacts_bd_res = @mysql_query($get_contacts_bd,$connection)
      or die(mysql_error());

      while ($contacts_bd = mysql_fetch_array($contacts_bd_res)) {
        $contact_id = $contacts_bd['id'];
        $contact_fname = $contacts_bd['f_name'];
        $contact_lname = $contacts_bd['l_name'];
        $contact_bd_month = $contacts_bd['month'];
        $contact_bd_date = $contacts_bd['date'];

        $bd_string .= "<li><a href=\"show_contacts.php?id=$contact_id\">$contact_fname
 . $contact_lname . "</a> (" . $contact_bd_month . ")-" . $contact_bd_date . ")</li>";
      }
      $bd_string .= "</ul>";
    }

    //构建菜单块
    $display_block = "<h1>联系人管理系统</h1>
    <p><em>今天是 $today</em></p>
    <table cellspacing=\"3\" cellpadding=\"3\">
    <tr>
    <td valign=\"top\">
    <p><strong>管理</strong></p>
    <ul>
      <li><a href=\"show_add_contact.php\">添加联系人</a></li>
      <li><a href=\"pick_mod_contact.php\">修改联系人</a></li>
      <li><a href=\"pick_del_contact.php\">删除联系人</a></li>
    </ul>
    <p><strong>查看记录</strong></p>
    <ul>
      <li><a href=\"show_contacts.php\">按姓名排序联系人</a></li>
    </ul>
    </td>
    <td valign=top>
    <p><strong>杂项</strong></p>
    <ul>
      <li>系统中的联系人：<strong>$count</strong></li>
      <li>本月生日：<strong>$birthday_count</strong></li>
      $bd_string
    </ul>
    </td>
    </tr>
    </table>";
}
?>
<HTML>
<HEAD>
<TITLE>联系人管理系统</TITLE>
</HEAD>
<BODY>
<?php echo "$display_block"; ?>
</BODY>
</HTML>
```

打开 http://127.0.0.1/contact_menu.php。如果你已经登录，将看到管理菜单。否则，使用用户名 (admin) 和密码 (abc123) 登录。如果你数据库表中有任何生日在本月的联系人，你应该看到他们的姓名和生日。

# 从 MY_CONTACTS 表提取数据 379

在下一节中，你将创建一个联系人详情脚本，显示你放入 my_contacts 表中的所有联系人信息。

![](img/be897bd1bf4dab38767db24da2a794b_401_0.png)

## 联系人管理系统

今天是2004年2月22日，星期日

管理

杂项

- 添加联系人
- 修改联系人
- 删除联系人

- 系统中的联系人 2
- 本月生日 1
- Michael Jones (2:28)

查看记录

- 按姓名排序联系人

## 从 my_contacts 表选择数据

现在困难的脚本工作已经完成，是时候执行一些 SQL 选择来显示 my_contacts 表中的数据了。你将首先列出联系人，然后显示联系人详情。

## 显示记录列表

此脚本的目标是显示数据库表中联系人的项目列表，并带有指向 `show_contacts.php` 脚本的链接。

1. 在编辑器中打开一个新文件并启动 PHP 块。然后，如果当前存在会话则启动它：

```php
php
session_start();
```

# 380 第 22 章：处理联系人

2. 启动 if_else 块，检查 $_SESSION['valid'] 的值并根据结果执行特定操作。如果值不是 yes，说明用户没有通过正确的认证通道：

```php
if ($_SESSION['valid'] != "yes") {
```

3. 将用户重定向到登录表单并退出此脚本：

```php
header("Location: http://127.0.0.1/contact_menu.php");
exit;
```

4. 创建变量来存储表所在的数据库名称以及表本身：

```php
$db_name = "testDB";
$table_name = "my_contacts";
```

5. 按照你之前的方法添加连接信息：

```php
$connection = @mysql_connect("*localhost", "spike", "9sj7En4")
or die(mysql_error());
```

6. 如你所学，选择数据库：

```php
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

7. 创建 SQL 语句。你想选择表中每条记录的 ID 、名字和姓：

```php
$sql = "SELECT id, f_name, l_name FROM $table_name ORDER BY l_name";
```

8. 创建一个变量来存储 `mysql_query()` 函数的结果，正如你所学过的：

```php
$result = @mysql_query($sql,$connection) or die(mysql_error());
```

9. 你稍将在 while 块中创建一个项目列表。先在 while 块之外启动项目列表：

```php
$contact_list = "<ul>";
```




## 从 MY_CONTACTS 表中选择数据

10. 启动 `while` 循环。`while` 循环将为结果集 ($result)每条记录创建一个名为 $row 的数组：

```php
while ($row = mysql_fetch_array($result)) {
```

11. 获取记录的各个元素并为它们命名良好的名称：

```php
$id = $row['id'];
$f_name = $row['f_name'];
$l_name = $row['l_name'];
```

12. 向 $contact_list 添加一个列表项，该项包含该人的姓名，并指向 show_contact.php 脚本的链接：

```php
$contact_list .= "<li><a href=\"show_contact.php?id=$id\">$l_name, $f_name</a></li>";
```

13. 结束 `while` 循环、项目列表和 PHP 块：

```php
}
$contact_list .= "</ul>";
?>
```

14. 添加此 HTML 内容：

```html
<HTML>
<HEAD>
<TITLE>我的联系管理系统：按姓名列出的联系人</TITLE>
</HEAD>
<BODY>
<h1>我的联系管理系统</h1>
<P>从下方列表中选择一个联系人，查看该人的记录。</P>
```

15. 显示 $contact_list 的内容：

```php
<?php echo "$contact_list"; ?>
```

16. 添加一个返回主菜单的链接：

```html
<br><p><a href="contact_menu.php">返回主菜单</a></p>
```

## 17. 添加更多 HTML 以使文档有效：

```html
</body>
</HTML>
```

### 18. 将文件保存为 `show_contactsbyname.php`，并将此文件放在你 Web 服务器的文档根目录下。

你的代码看起来应该像这样：

```php
<?
//开始会话
session_start();

//检查用户的有效性
if ($_SESSION['valid'] != "yes") {
    header("Location: http://127.0.0.1/contact_menu.php");
    exit;
}

//设置表和数据库名
$db_name = "testDB";
$table_name = "my_contacts";

//连接服务器并选择数据库
$connection = @mysql_connect("localhost","spike","9sj7En4")
or die (mysql_error());
$db = @mysql_select_db($db_name, $connection) or die (mysql_error());

//构建并插入查询
$sql = "SELECT id, f_name, l_name FROM $table_name ORDER BY l_name";
$result = @mysql_query($sql,$connection) or die (mysql_error());

//创建结果列表块
$contact_list = "<ul>";
while ($row = @mysql_fetch_array($result)) {
    $id = $row['id'];
    $f_name = $row['f_name'];
    $l_name = $row['l_name'];
    $contact_list .= "<li><a href=\"show_contact.php?id=$id&name=$l_name\">$f_name</a></li>";
}
```

```php
$contact_list .= "</ul>";
?>
<HTML>
<HEAD>
<TITLE>我的联系管理系统：按姓名列出的联系人</TITLE>
</HEAD>
<BODY>
<h1>我的联系管理系统</h1>
<P>从下方列表中选择一个联系人，查看该人的记录。</P>
<?php echo "$contact_list"; ?>
<br><p><a href="contact_menu.php">返回主菜单</a></p>
</BODY>
</HTML>
```

打开 http://127.0.0.1/contact_menu.php。如果你已经登录，你将看到管理菜单。否则，使用用户名 (admin) 和密码 (abc123) 登录。选择“按姓名排序显示联系人”链接。

在下一节中，你将创建联系人显示页面 `show_contact.php`。

从下方列表中选择一个联系人，查看该人的记录。

- Doe Jane
- Jones Michael

返回主菜单

## 显示只读记录

这是关键时刻：显示你的联系人！

- 1. 在你的文本编辑器中打开一个新文件，并启动一个 PHP 块：

```php
<?
```

- 2. 启动一个 if-else 块，检查 $_GET['id'] 的值，该变量是通过链接的查询字符串发送的。如果值不存在，则将用户重回菜单并编辑脚本：

```php
if (!$_GET['id']) {
  header("Location: http://127.0.0.1/contact_menu.php");
  exit;
}
```

- 3. 如果必需字段有值，启动会话或如果当前存在会话则继续会话，然后结束该块：

```php
} else {
  session_start();
}
```

- 4. 启动一个 if-else 块，检查 $_SESSION['valid'] 的值并根据结果执行特定操作。如果值不是 yes，说明用户没有通过正确的身份验证：

```php
if ($_SESSION['valid'] != "yes") {
```

- 5. 将用户重定向回菜单并退出脚本：

```php
header("Location: http://127.0.0.1/contact_menu.php");
exit;
```

- 6. 创建变量来存储数据库和表名：

```php
$db_name = "testDB";
$table_name = "my_contacts";
```

- 7. 添加连接信息：

```php
$connection = @mysql_connect("localhost","spike","9sj7En4")
```

- 8. 选择数据库：

```php
$db = @mysql_select_db($db_name, $connection)
```

- 9. 构建 SQL 语句：

```php
$sql = "SELECT id, f_name, l_name FROM $table_name ORDER BY l_name";
```

- 10. 执行查询：

```php
$result = @mysql_query($sql,$connection) or die (mysql_error());
```

- 11. 创建结果列表块：

```php
$contact_list = "<ul>";
```

- 12. 启动 `while` 循环：

```php
while ($row = @mysql_fetch_array($result)) {
```

- 13. 获取记录的各个元素：

```php
    $id = $row['id'];
    $f_name = $row['f_name'];
    $l_name = $row['l_name'];
```

- 14. 添加列表项：

```php
    $contact_list .= "<li><a href=\"show_contact.php?id=$id&name=$l_name\">$f_name</a></li>";
```

- 15. 结束循环并关闭列表：

```php
}
$contact_list .= "</ul>";
?>
```

- 16. 构建 HTML 结构：

```html
<HTML>
<HEAD>
<TITLE>我的联系管理系统：按姓名列出的联系人</TITLE>
</HEAD>
<BODY>
<h1>我的联系管理系统</h1>
<P>从下方列表中选择一个联系人，查看该人的记录。</P>
```

- 17. 显示列表内容：

```php
<?php echo "$contact_list"; ?>
```

- 18. 添加返回主菜单的链接：

```html
<br><p><a href="contact_menu.php">返回主菜单</a></p>
```

- 19. 添加更多 HTML 以使文档有效：

```html
</body>
</HTML>
```





## 第 22 章：处理联系人

看起来不错！这是我数据库表中一个完整的联系人。但接下来的图显示了当联系人不完整时会发生什么。

## 我的联系人管理系统

Jane Doe 的联系详情

姓名与地址：
Jane Doe
115 Main Street
Suite 2A
Anytown, California
95465
USA

电话 1: 555-444-1111
电话 2: 555-555-5556
电子邮箱：jane@doe.com
生日：1970-01-01

返回主菜单

太丑了！现在你可以对 `show_contact.php` 进行一些修改，考虑到两个字段（姓和名）是必填的。

## 我的联系人管理系统

Michael Jones 的联系详情

姓名与地址：
Michael Jones

电话 1：
电话 2：
电子邮箱：
生日：1975-02-22

返回主菜单

- 1. 打开 `show_contact.php`。
- 2. 滚动到“姓名与地址”部分。
- 3. 删除此部分：

```php
<?php echo "$address1"; ?><
<?php echo "$address2"; ?><
<?php echo "$address3"; ?><
<?php echo "$postcode"; ?><
<?php echo "$country"; ?>
<P><strong>Tel 1:</strong><?php echo "$prim_tel"; ?>
<strong>Tel 2:</strong><?php echo "$sec_tel"; ?>
<strong>E-Mail:</strong><?php echo "<a href=mailto:$email\n$email@</a>"; ?>
</P>
<P><strong>Birthday:</strong><?php echo "$birthday"; ?></P>
```

- 4. 输入以下系列语句，它们仅当特定变量有值时才打印该行：

```php
if ($address1 != "") {
    echo "$address1 <br>";
}
if ($address2 != "") {
    echo "$address2 <br>";
}
if ($address3 != "") {
    echo "$address3 <br>";
}
if ($postcode != "") {
    echo "$postcode <br>";
}
if ($country != "") {
    echo "$country <br>";
}
?>
</P>
<?php
if ($prim_tel != "") {
    echo "<strong>Tel 1:</strong> $prim_tel <br>";
}
if ($sec_tel != "") {
    echo "<strong>Tel 2:</strong> $sec_tel <br>";
}
```

```php
if ($email != "") {
  echo "<strong>E-Mail:</strong>\n  <a href="mailto:$email\"></a><br>";
}
?>
<?php
if ($birthday != "0000-00-00") {
  echo "<P><strong>Birthday:</strong> $birthday </P>";
}
?>
```

- 5. 保存此文件。

现在当你有一条不完整的记录时，你就不会看到那些空白了。

所以，你得到了——一个利用会话用户身份验证的完整在线联系人管理系统。这里有很多修改区域和额外的验证检查，所以请花时间玩玩这些脚本，直到你熟悉了这些概念。例如，你可能希望一组不同的字段是必填的，或者你可能想向表中添加更多字段（从而向你的表单和显示脚本）。这些简单的概念将帮助你理解并构建更大的应用程序。

## 我的联系人管理系统

Michael Jones 的联系详情

姓名与地址：
Michael Jones
生日：1975-02-28
返回主菜单

## 其他项目示例

- 第 23 章 管理简单的邮件列表 ...... 393
- 第 24 章 创建自定义日志和报告 ... 415
- 第 25 章 处理 XML ................................... 437

## 第 23 章 管理简单的邮件列表

最终，你的网站将会有访问者，某一天你可能还想向他们发送时事通讯。你可以使用 PHP 和 MySQL 创建一个非常简单的订阅和发布机制。在本章中，你将学习如何：

- 创建一个订阅/取消订阅脚本
- 创建一个发送邮件通讯的前端
- 创建一个将你的邮件通讯发送给数据库中所有收件者的脚本

## 关于邮件列表软件的简要说明

有几个非常好的邮件列表应用程序可以向大量电子邮件地址发送邮件。你在本章中构建的系统将仅用于少于几百个电子邮件地址的小列表。

本章描述的系统源于我某天的懒惰，当时我不想下载和安装任何第三方软件。我只是做了一些执行该任务的文件。这就是 PHP 的美之处：它是一门如此简单的语言，有时编写几个脚本要比下载或安装某些东西容易得多。然而，当你的邮件列表变大时，请迁移到更健壮的邮件列表应用程序，这对你的出站邮件服务器以及管理员来说都更得得从心。

## 开发机制

在开始发送到邮件列表之前，你需要建立该基础。一个简单的订阅/取消订阅脚本将处理这个问题！该脚本所做的只是在名为 `subscribers` 的 MySQL 数据库中添加或删除记录，你将在下一节中创建它。

## 创建 subscribers 表

我的 `subscribers` 表有三个字段，如表 23.1 所示。你可以拥有任意数量的字段。

| 表 23.1 字段 | 描述 |
| --- | --- |
| id | 订阅者的 ID |
| email_addr | 订阅者的电子邮件地址 |
| date_added | 订阅的日期 |

你可以拥有尽可能多或尽可能少的字段。

## 开发机制

在开始发送到邮件列表之前，你需要建立该基础。一个简单的订阅/取消订阅脚本将处理这个问题！该脚本所做的只是在名为 `subscribers` 的 MySQL 数据库中添加或删除记录，你将在下一节中创建它。

## 创建 subscribers 表

我的 `subscribers` 表有三个字段，如表 23.1 所示。你可以拥有任意数量的字段。

| 字段名 | 类型 | 长度 | 是否自增 |
| --- | --- | --- | --- |
| id | int | | |
| email_addr | varchar | 100 | |
| date_added | date | | |

在下一节中，你将创建订阅机制。

## 将表添加到 testDB...

subscribers 已创建！

## 创建订阅表单

类似于第 8 章“发送邮件”中的表单，订阅表单将用于订阅、取消和错误检查。

- 1. 在文本编辑器中打开一个新文件，并开始 PHP 块：

```php
<?php
```

- 2. 创建变量来存储表所在的数据库名称，以及表本身：

```php
$db_name = "testDB";
$table_name = "subscribers";
```

接下来你将检查尚未创建的变量。当你创建实际的 HTML 表单时，将添加一个名为 `op` 值为 `ds` 的隐藏字段。`$_POST[op]` 变量只有在表单提交时存在。

- 3. 启动 `if...else` 块，首先检查 `$_POST[op]` 是否为 `ds`：

```php
if ($_POST[op] != "ds") {
```

- 4. 如果 `$_POST[op]` 的值不是 `ds`，用户还没有看到表单。如果用户还没有看到表单，你需要显示。创建一个名为 `$text_block` 的变量来包含整个表单。从表单开始，并假设方法是 `$_SERVER[PHP_SELF]`：

```php
$text_block = "
<form method=POST action=\"$_SERVER[PHP_SELF]\";
```

- 5. 添加隐藏字段：

```html
<input type=hidden name=op value=ds
```

- 6. 为用户的电子邮件地址创建一个输入字段，并带有文本标签：

```html
<p><strong>Your E-Mail Address:</strong><br>
<input type=text name="email_addr*" size=25 maxlength=100></p>
```





7. 创建一组单选按钮，使用户可以选择“订阅”或“取消订阅”操作。默认应为订阅单选按钮：

```html
<p><strong>Action:</strong><br>
<input type="radio" name="sub" value="sub" checked> subscribe
<input type="radio" name="sub" value="unsub"> unsubscribe</p>
```

8. 添加一个提交按钮并关闭表单：

```html
<p><input type=submit name="submit" value="Submit Form"></p>
</form>;
```

9. 继续编写 if_else 块，检查 `$_POST[op]` 是否为 `ds`，并检查 `$_POST[action]` 变量的值。这意味着用户正尝试订阅：

```php
} else if ($_POST[op] == "ds" && $_POST[action] == "sub") {
```

10. 但如果有人点击了按钮却没有输入电子邮件地址怎么办？添加一个 if 块来检查 `$_POST[email_addr]` 中的值。如果未找到值，将用户重定向回原始表单：

```php
if ($_POST[email_addr] == "") {
    header("Location: http://127.0.0.1/manage.php");
    exit;
}
```

11. 你需要检查用户是否已经订阅，按照你所学的方法打开数据库连接：

```php
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
```

12. 按照你所学的方法选择数据库：

```php
$db = @mysql_select_db($db_name,$connection) or die(mysql_error());
```

13. 创建一个 SQL 语句，查找与用户电子邮件匹配的记录：

```php
$check = "select email_addr from $table_name where email_addr = '$_POST[email_addr]'";
```

# 开发订阅机制 399

14. 按照你所学的方法，创建一个变量来存储 `mysql_query()` 函数的结果：

```php
$check_result = @mysql_query($check, $connection) or die (mysql_error());
```

15. 创建一个变量来统计结果集中行数：

```php
$check_num = mysql_num_rows($check_result);
```

16. 创建一个 if...else 块，根据 `$check_num` 的值执行操作。如果 `$check_num` 小于 1，说明订阅表中没有该用户的电子邮件，因此插入操作是安全的：

```php
if ($check_num < 1) {
```

17. 创建一个 SQL 语句来插入电子邮件和 MySQL 函数 `now()`，该函数将插入当前日期（为自增 id 留空值）：

```php
$sql = "insert into $table_name values('', '$_POST[email_addr]', now())";
```

18. 按照你所学的方法执行查询：

```php
$result = @mysql_query($sql, $connection) or die (mysql_error());
```

19. 创建一个消息字符串告知用户：

```php
$text_block = "<p>Thanks for signing up!</p>";
```

20. 通过创建一个告知用户已经订阅的提示字符串来完成 if...else 块。然后关闭内层的 if...else 块：

```php
} else {
$text_block = "<p>You're already subscribed!</p>";
}
```

21. 继续外层的 if...else 块，检查 `$_POST[op]` 是否为 `ds`，并检查 `$_POST[action]` 变量的值是否为 `unsub`。这意味着用户正尝试取消订阅。

```php
} else if ($_POST[op] == "ds") && ($_POST[action] == "unsub")) {
```

# 400 第23 章：管理简单的邮件列表

**22.** 再次添加检查 `$_POST[email_addr]` 值的验证。如果未找到值，将用户重定向到以下表单：

```php
if ($_POST[email_addr] == "") {
    header("Location: http://127.0.0.1/manage.php");
    exit;
}
```

**23.** 你需要检查用户是否确实订阅，打开数据库连接并选择数据库：

```php
$connection = mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
$db = mysql_select_db($db_name,$connection) or die(mysql_error());
```

**24.** 创建一个 SQL 语句查找与用户电子邮件匹配的记录。同时选择 `id` 字段，如果你找到了匹配项，将用它来取消订阅：

```php
$check = "select id, email_addr from $table_name where email_addr = '$_POST[email_addr];
```

**25.** 执行查询：

```php
$check_result = mysql_query($check, $connection) or die(mysql_error());
```

**26.** 创建一个变量来统计结果集的行数：

```php
$check_num = mysql_num_rows($check_result);
```

**27.** 创建一个内层 if...else 块，根据 `$check_num` 的值执行操作。如果 `$check_num` 小于 1，说明订阅表中没有用户的电子邮件，因此你无法为其取消订阅。

```php
if ($check_num < 1) {
```

**28.** 创建一个告知消息字符串：

```php
$text_block = "<P>Couldn't find your e-mail on the list!</P><P>You't been unsubscribed, because the email entered not in the database.</P>";
```

**29.** 继续内层 if...else 块：

```php
} else {
```

**30.** 创建一个变量获取结果集中特定的 `id` 值：

```php
$id = @mysql_result($check_result, 0, "id");
```

**31.** 创建一个 SQL 语句从订阅表中删除用户的电子邮件：

```php
$sql = "delete from $table_name where id = '$_POST[id]";
```

**32.** 执行查询：

```php
$result = @mysql_query($sql, $connection) or die(mysql_error());
```

**33.** 创建一个消息字符串告知用户：

```php
$text_block = "<p>You're unsubscribed!</p>";
```

**34.** 关闭 if...else 块、外层 if...else 块以及 PHP 块：

```php
}
?>
```

**35.** 添加以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>Subscribe/Unsubscribe</TITLE>
</HEAD>
<body
<h1>Subscribe/Unsubscribe</h1>
```

**36.** 显示 `$text_block` 的内容：

```php
<?php echo "$text_block"; ?>
```

**37.** 添加额外的 HTML 以使文档有效：

```html
</BODY>
</HTML>
```

**38.** 将文件保存为 `manage.php` 并将其放置在 Web 服务器的根目录下。#402 第23 章：管理简单的邮件列表

你的整个代码应该是这样的：

```php
<?php
// 设置表和数据库名称
$db_name = "test";
$table_name = "subscribers";

// 判断他们是否需要看到表单
if ($_POST[op] != "ds") {
    // 创建表单块
    $text_block = "
<form method=POST action=\$_SERVER['PHP_SELF']\">
<p><strong>Your E-Mail Address:</strong><br>
<p><input type=text name=\"email_addr\" size=25 maxlength=100\"></p>
<p><strong>Action:</strong><br>
<input type=radio name=\"action\" value=\"sub\" checked> subscribe
<input type=radio name=\"action\" value=\"unsub\">
<p><input type=submit name=\"submit\" value=\"Submit Form\"></p>
</form>";
} elseif ($_POST[op] == "ds" && ($_POST[action] == "sub")) {
    // 尝试订阅；验证电子邮件地址
    if ($_POST[email_addr] == "") {
        header("Location: http://127.0.0.1/manage.php");
        exit;
    }

    // 连接服务器并选择数据库
    $connection = @mysql_connect("localhost", "spike", "9sj7En4")
    or die(mysql_error());
    $db = @mysql_select_db($db_name,$connection) or die(mysql_error());

    // 检查电子邮件是否在列表中
    $check = "select email_addr from $table_name where email_addr = '$_POST[email_addr]'";
    $check_result = @mysql_query($check,$connection) or die(mysql_error());
    $check_num = mysql_num_rows($check_result);

    // 获取结果数量并执行操作
    if ($check_num < 1) {
        // 添加记录
        $sql = "insert into $table_name values('', '$_POST[email_addr]', now())";
        $result = @mysql_query($sql,$connection) or die(mysql_error());
        $text_block = "<P>Thanks for signing up!</P>";
    } else {
        // 打印失败消息
        $text_block = "<P>You're already subscribed!</P>";
    }
} else if ($_POST[op] == "ds" && ($_POST[action] == "unsub")) {
    // 尝试取消订阅：验证电子邮件地址
    if ($_POST[email_addr] == "") {
        header("Location: http://127.0.0.1/manage.php");
        exit();
    }

    // 连接服务器并选择数据库
    $connection = @mysql_connect("localhost", "spike", "9sj7En4")
    or die(mysql_error());
    $db = @mysql_select_db($db_name,$connection) or die(mysql_error());

    // 检查电子邮件是否在列表中
    $check = "select id, email_addr from $table_name where email_addr = '$_POST[email_addr]'";
    $check_result = @mysql_query($check,$connection) or die(mysql_error());
    $check_num = mysql_num_rows($check_result);

    // 获取结果数量并执行操作
    if ($check_num < 1) {
        // 打印失败消息
        $text_block = "<P>Couldn't find your e-mail on the list!</P><P>You't been unsubscribed, because the email entered is not in the database.</P>";
    } else {
        // 取消订阅
        $id = @mysql_result($check_result, 0,"id");
        $sql = "delete from $table_name where id = '$_id'";
        $result = @mysql_query($sql,$connection) or die(mysql_error());
        $text_block = "<p>You're unsubscribed!</p>";
    }
}
?>
<HTML>
<HEAD>
<TITLE>Subscribe/Unsubscribe</TITLE>
</HEAD>
<body>
<h1>Subscribe/Unsubscribe</h1>
<?php echo "$text_block"; ?>
</body>
</HTML>
```



```html
?>
<HTML>
<HEAD>
<TITLE>订阅/取消订阅</TITLE>
</HEAD>
<BODY>
<h1>订阅/取消订阅</h1>
<?php echo "$text_block"; ?>
</BODY>
</HTML>
```

在下一节中，你将订阅和取消订阅用户，并观察所有地址验证是如何工作的。

## 测试订阅表单

现在你已经完成了创建订阅表单的所有步骤，是时候测试它了！

- 1. 打开网页浏览器并输入 http://127.0.0.1/manage.php。

![](img/be897bd1bfd4dab38767db24da2a794b_426_0.png)

你会看到一个包含一个包含个人电子邮件地址的文本字段、两个用于订阅或取消订阅的单选按钮以及一个显示为“Submit Form”（提交表单）的按钮。

- 2. 在“Your E-Mail Address”（您的电子邮件）字段中输入你的邮箱，选择“Subscribe”（订阅）单选按钮，然后提交表单。

# 开发订阅机制 405

![](img/be897bd1bfd4dab38767db24da2a794b_427_0.png)

你会看到一个订阅成功的确认信息。

- 3. 使用浏览器的“返回”按钮回到表单，并在“Your E-Mail Address”字段中输入相同的邮箱。

- 4. 再次选择“Subscribe”（订阅）单选按钮，然后提交表单。

## 订阅/取消订阅

感谢注册！

![](img/be897bd1bfd4dab38767db24da2a794b_427_1.png)

你会看到一条消息，提示你已经订阅。

- 5. 使用浏览器的“返回”按钮返回表单，并在“Your E-Mail Address”字段中输入相同的邮箱。这次，选择“Unsubscribe”（取消订阅）单选按钮并提交表单。

## 订阅/取消订阅

你已经订阅了！

# 406 第23 章：管理简单的邮件列表

你会看到一个已取消订阅的确认信息。

![](img/be897bd1bfd4dab38767db24da2a794b_428_0.png)

- 6. 使用浏览器的“返回”按钮返回表单，并在“Your E-Mail Address”字段中输入相同的邮箱。

![](img/be897bd1bfd4dab38767db24da2a794b_428_1.png)

你会看到该电子邮件地址不在数据库中，因此没有被取消订阅。

继续添加一些自己的邮箱地址，因为在下一节中，你将创建一个表单和脚本来向列表发送邮件，这将真实的邮件列表。

# 开发邮件机制

现在你已经有了订阅/取消订阅机制，可以创建一个简单的表单界面来编写邮件脚本。此邮件机制将获取表单内容并发送到 subscribers 表中的每个地址。

# 创建邮件表单

当我说创建一个“简单”表单时并不是开玩笑。只需使用一个文本字段用于邮件主题，一个文本区域用于邮件正文。你可以根据需要使用许多表单字段，只要相应地修改表单和脚本即可。

- 1. 在文本编辑器中打开一个新文件并输入以下 HTML：

```html
<HTML>
<HEAD>
<TITLE>Send a Newsletter</TITLE>
</HEAD>
<BODY>
<h1>Send a Newsletter</h1>
```

- 2. 开始你的表单。假设方法为 POST，动作为脚本 `do_send_newsletter.php`：

```html
<FORM METHOD="POST" ACTION="do_send_newsletter.php">
```

- 3. 为邮件主题创建一个输入字段并带上标签：

```html
<p><strong>Give it a subject:</strong><br>
<input type="text" name="subject" size=30></p>
```

- 4. 为邮件正文创建一个文本区域并带上标签：

```html
<p><strong>Newsletter body:</strong><br>
<textarea name="newsletter" cols=50 rows=10 wrap="virtual"></textarea></p>
```

- 5. 添加一个提交按钮：

```html
<p><input type="submit" name="submit" value="Send Newsletter"></p>
```

- 6. 关闭你的表单，并添加更多 HTML 使文档有效：

```html
</FORM>
</BODY>
</HTML>
```

- 7. 将文件保存为 `send_newsletter.html`，并将其放在 Web 服务器的文档根目录下。

- 8. 打开浏览器并输入 http://127.0.0.1/send_newsletter.html。

![](img/be897bd1bfd4dab38767db24da2a794b_430_0.png)

你会看到一个包含邮件主题文本字段、消息文本区域以及一个显示“Send Newsletter”按钮的表单。

在下一节中，你将创建一个脚本。该脚本将接收两个变量：`$_POST[subject]` 和 `$_POST[newsletter]`。

# 创建发送邮件的脚本

根据 `send_newsletter.html` 中的表单动作，你需要一个名为 `do_send_newsletter.php` 的脚本。该脚本的目标是 `$_POST[subject]` 和 `$_POST[newsletter]` 中的文本，然后以电子邮件的形式发送给表中所有人。

- 1. 在文本编辑器中打开一个新文件并开始编写 PHP：

```php
<?php
```

# 开发邮件机制 409

- 2. 开始 if 块并检查 `$_POST[subject]` 和 `$_POST[newsletter]` 是否输入了值。如果任一变量为空，将用户重回表单：

```php
if ($_POST[subject] == "" || $_POST[newsletter] == "") {
    header("Location: http://127.0.0.1/send_newsletter.html");
    exit;
}
```

- 3. 创建 if...else 块：

```php
} else {
```

- 4. 创建变量来存储所需的数据库名称以及表本身：

```php
$db_name = "testDB";
$table_name = "subscribers";
```

- 5. 如你学的那样连接数据库服务器并选择数据库：

```php
$connection = mysql_connect("localhost", "spike")
or die(mysql_error());
$db = mysql_select_db($db_name,$connection) or die(mysql_error());
```

- 6. 创建一个 SQL 语句来选择 subscribers 表中的所有电子邮件地址：

```php
$sql = "select email_addr from $table_name";
```

- 7. 执行查询：

```php
$result = @mysql_query($sql,$connection) or die(mysql_error());
```

- 8. 创建一个变量来存储 From 请求头：

```php
$headers = "From: Your Mailing List <you@domain.com>\n";
```

- 9. 开始 while 循环。while 循环将向表中的每个记录发送邮件消息，然后打印邮件已发送的确认：

```php
while ($row = mysql_fetch_array($result)) {
```

- 10. 获取记录的电子邮件地址：

```php
$email_addr = $row['email_addr'];
```

# 第23 章：管理简单的邮件列表

- 11. 格式化 `mail()` 函数的调用。使用 `stripslashes()` 函数处理 `$_POST[subject]` 和 `$_POST[newsletter]` 的值。这将移除 PHP 自动输入的特殊字符：

```php
    mail($email_addr, stripslashes($_POST[subject]), stripslashes($_POST[newsletter]), $headers);
```

- 12. 打印确认信息：

```php
    echo "newsletter sent to $email_addr<br>";
```

- 13. 关闭 while 循环、if...else 块以及 PHP 块：

```php
}
?>
```

- 14. 将文件保存为 `do_send_newsletter.php`，并将其放在 Web 服务器的文档根目录下。

你的代码应该如下：

```php
<?php
//检查必填字段
if ($_POST[subject] == "" || $_POST[newsletter] == "") {
    header("Location: http://127.0.0.1/send_newsletter.html");
    exit;
} else {
//设置表和数据库名
$db_name = "testDB";
$table_name = "subscribers";

//连接服务器并选择数据库
$connection = mysql_connect("localhost", "spike")
or die(mysql_error());
$db = mysql_select_db($db_name,$connection) or die(mysql_error());

//构建并执行查询
$sql = "select email_addr from $table_name";
$result = @mysql_query($sql,$connection) or die(mysql_error());

//创建From:邮件头
$headers = "From: Your Mailing List <you@domain.com>\n";

//循环结果并发送邮件
while ($row = mysql_fetch_array($result)) {
    $email_addr = $row['email_addr'];
    mail($email_addr, stripslashes($_POST[subject]), stripslashes($_POST[newsletter]), $headers);
    echo "newsletter sent to $email_addr<br>";
}
?>
```

# 测试你的邮件机制

在这一节中，你将对脚本进行测试，并向所有订阅者发送邮件。确保你的电子邮件地址在列表中，否则你无法确定系统是否正常工作。

> 注意
> 图中显示的是我输入的示例文本和示例订阅列表中的电子邮件地址。你的结果将有所不同，但事件的顺序是相同的。





## 412 第 23 章：管理简单的邮件列表

- 2. 点击“发送通讯报”（Send Newsletter）按钮提交表单。

你将看到发送通讯报的电子邮箱地址确认。

- 3. 如果你的地址在订阅者表中，请检查你的电子邮箱。

## 开发邮件机制 413

你的信箱里应该已经有一份格式良好的通讯报了！

## 你的邮件列表机制故障排除

如果你收到如“警告：无法连接”（Warning: Can't connect）之类的错误，你必须确保修改了 `php.ini` 文件中的 SMTP 值。此主题在第 8 章“发送电子邮件”中有介绍，而且解决方法非常简单。

使用这种邮件机制时的另外一个问题是，如果列表足够长，脚本最终会超时。这就是为什么不要使用这种机制向大型接收者列表发送通讯报的原因之一。因为该脚本执行了多次 `mail()` 函数，但它没有考虑真实邮件列表软件中的队列因素，而这些软件旨在减轻你发件邮件服务器的负担。

为了解决脚本超时问题，你可以在脚本执行期间重置计时器。本质上，通过在 `while` 循环中插入以下行，你可以在每次调用 `mail()` 函数之前将计时器置为 0：

```php
set_time_limit(0);
```

你的 `while` 循环现在看起来如下：

```php
while ($row = mysql_fetch_array($result)) {
    set_time_limit(0);
    $email_addr = $row['email_addr'];
    mail($email_addr, "", stripslashes(\$_POST['subject']),
    stripslashes(\$_POST['newsletter']), $headers);
    echo "newsletter sent to: $email_addr<br>";
}
```

记住，这并不能减轻发件邮件服务器的负担。它只是允许脚本继续运行，而它之前可能已经超时。

在下一章中，你将处理另一个项目。当你创建一个网站时，你会想要了解一些关于访问者的数字——谁、什么、何地以及如何。你的下一个项目将为这些指标构建一个自定义的报告机制。

## 创建自定义日志和报告

如果你正在为公共用户构建网站，那么你可能想知道网站的哪些部分最受欢迎、最不受欢迎、使用了什么类型的网络浏览器等等。尽管 Apache 保留了访问和错误的通用日志文件，但你可以创建一些代码片段将特定信息存储在你的 MySQL 数据库中。在本章中，你学习如何：

- 使用 MySQL 创建简单的访问计数机制
- 在页面和报告中显示访问计数
- 跟踪表单提交
- 创建表单提交的摘要报告

## 关于 Apache 日志文件的说明

Apache Web 服务器会自动记录有关用户访问和错误的特定信息。这些日志文件位于 `logs` 目录中。名为 `access.log` 的文件处理访问，`error.log` 文件处理错误。

访问日志的默认格式如下所示（取自我自己的日志）：

```
127.0.0.1 [22/Feb/2004:05:27:10] GET /show_creatable.html HTTP/1.1" 304 -
127.0.0.1 [22/Feb/2004:05:27:46] POST /do_showfielddef.php HTTP/1.1" 200 2402
127.0.0.1 [22/Feb/2004:05:28:49] POST /do_creatable.php HTTP/1.1" 200 185
127.0.0.1 [22/Feb/2004:05:43:33] GET /manage.php HTTP/1.1" 200 562
```

我知道这看起来相当晦懂。你可以在 `httpd.conf` 文件中这样设置格式：

```
LogFormat "%h %l %u %t \"r\ %s %b"
```

在这种情况下，该格式与表 24.1 中列出的描述相对应。

| 表 24.1 Apache 日志文件设置 |
| 符号 | 描述 |
| :--- | --- |
| %h | 发起请求的机器的远程主机名，或如果 HostnameLookup = off 则为 IP |
| %l | 远程日志用户名（通常为空） |
| %u | 用户请求的 URL 路径 |
| %t | 访问时间 |
| %"r" | 请求的第一行，位于双引号内 |
| %s | 请求状态 |
| %b | 发送的字节数，不包括标头 |

> 注意：访问日志的默认格式如下所示（取自我自己的日志）。你可以在 `httpd.conf` 文件中这样设置格式：在这种情况下，该格式与表 24.1 中列出的描述相对应。

## 使用 MySQL 进行简单访问

> 注意：访问日志的默认格式如下所示（取自我自己的日志）。你可以在 `httpd.conf` 文件中这样设置格式：在这种情况下，该格式与表 24.1 中列出的描述相对应。

## 创建片段

“Snippet”（片段）是一个高度技术性的术语，意思是“一小段代码”。关于“高度技术性”部分我是在开玩笑，但代码片段通常是某些不算作长脚本的东西。相反，它

## 使用 MySQL 进行访问计数

在这种情况下，你的代码片段将一些基本信息写入 page_track 表，然后完成一些 HTML。

- 1. 在你的文本编辑器中打开一个新文件并开始一个 PHP 块：

```php
<?
```

- 2. 创建四个变量，对应 page_track 表中的四个非 ID 字段，并给它们赋予值：

```php
$page_name = "sample l1";
$page_desc = "This is a sample page of no use";
$user_agent = getenv("HTTP_USER_AGENT");
$date_added = date("Y-m-d");
```

- 3. 创建变量来存储表所在的数据库以及表本身：

```php
$db_name = "testDB";
$table_name = "page_track";
```

- 4. 按照之前添加连接信息：

```php
$connection = @mysql_connect("localhost", "spike", "9sj7En4");
or or(mysql_error());
```

- 5. 按照你学习的方法选择数据库：

```php
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

- 6. 创建一个 SQL 语句，将值插入 page_track 表的字段中，留空 ID 字段以便自动递增：

```php
$sql = "insert into $table_name values
('', '$page_name', '$page_desc', '$user_agent', '$date_added')";
```

- 7. 执行查询，并关闭 PHP 块：

```php
$result = @mysql_query($sql,$connection) or die(mysql_error());
?>
```





## 第 24 章：创建自定义日志和报告

你刚刚创建了代码片段，它看起来应该是这样的：

```php
<?
//set up static variables
$page_name = "sample 1";
$page_desc = "This is a sample page of no use.";
$user_agent = getenv("HTTP_USER_AGENT");
$date_added = date("Y-m-d");

//set up table and database names
$db_name = "testDB";
$table_name = "page_track";

//connect to server and select database
$connection = @mysql_connect("localhost", "spike", "9j7En4") or die(mysql_error());
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());

//build and issue query
$sql = "insert into $table_name values\n('', '$page_name', '$page_desc', '$user_agent', '$date_added');";
$result = @mysql_query($sql, $connection) or die(mysql_error());
?>
```

现在，在代码片段之后直接创建一段填充用的 HTML 代码：

```html
<HTML>
<HEAD>
<TITLE>Sample Page #1</TITLE>
</HEAD>
<BODY>
<h1>Useless Sample Page #1</h1>
<p>This sample page serves no real purpose!</p>
</BODY>
</HTML>
```

将该文件保存为 `sample_page.php`，并将其放置在 Web 服务器的文档根目录下。为了让你的报告更有趣，请再创建一个这样的示例文件，这样你就有比这一个文件更多的内容可以计数了。

# 使用 MySQL 进行简单的访问计数

将 `sample_page1.php` 复制为 `sample_page2.php`，并将 `sample_page2.php` 中的前两个变量更改为如下：

```php
$page_name = "sample 2";
$page_desc = "Another useless sample page.",
```

将 `sample_page2.php` 中的 HTML 块替换为内容：

```html
<HTML>
<HEAD>
<TITLE>Sample Page #2</TITLE>
</HEAD>
<BODY>
<h1>Useless Sample Page #2</h1>
<P>I can't believe how useless this page is!</p>
</BODY>
</HTML>
```

现在保存此文件并将其放置在 Web 服务器的文档根目录下。

接下来，你将访问这些页面几次以获取内部计数。

- 1. 打开网页浏览器并输入 `http://127.0.0.1/sample_page1.php`。

你会看到该 HTML 页面，包含一个标题和一些文本。

- 2. 打开网页浏览器并输入 `http://127.0.0.1/sample_page2.php`。

你会看到具有不同标题和一些不同文本的 HTML 页面。

反复刷新这些页面几次，然后移动到下一节，在那里将显示计数。

# 显示计数

在这些页面上显示计数轻而易举。你只需要在代码片段中添加三行代码，并在 HTML 块内部添加一行。

- 1. 在文本编辑器中打开 `sample_page.php`。

- 2. 在 PHP 块结束之前，创建一个 SQL 语句来获取此特定页面的访问次数：

```php
$count_sql = "select count(page_name) from $table_name
where page_name = '$page_name'";
```

> 注意
> 将计数代码放在插入代码之后，以确保你也计入了当前的访问！

- 3. 执行查询：

```php
$count_res = @mysql_query($count_sql,$connection) or die(mysql_error());
```

# 使用 MySQL 进行简单的访问计数

- 4. 创建变量来存储当前结果集中的特定计数：

`$count = mysql_result($count_res, 0, "count(page_name)");`

- 5. 在你的 HTML 块中，混合 PHP 来打印 `$count` 的值：

`<P>Accesses: <?php echo "$count"; ?></p>`

你的 `sample_page.php` 脚本应该如下：

```php
<?
//set up static variables
$page_name = "sample 1";
$page_desc = "This is a sample page of no use.";
$user_agent = getenv("HTTP_USER_AGENT");
$date_added = date("Y-m-d");

//set up table and database names
$db_name = "testDB";
$table_name = "page_track";

//connect to server and select database
$connection = @mysql_connect("localhost", "spike", "9j7En4") or die(mysql_error());
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());

//build and issue query
$sql = "insert into $table_name values\n('', '$page_name', '$page_desc', '$user_agent', '$date_added')";
$result = @mysql_query($sql, $connection) or die(mysql_error());

//get count
$count_sql = "select count(page_name) from $table_name
where page_name = '$page_name'";
$count_res = @mysql_query($count_sql,$connection) or die(mysql_error());
$count = @mysql_result($count_res, 0, "count(page_name)");
?>

<HTML>
<HEAD>
<TITLE>Sample Page #1</TITLE>
</HEAD>
<BODY>
<h1>Useless Sample Page #1</h1>
<p>This sample page serves no real purpose!</p>
<p>Accesses: <?php echo "$count"; ?></p>
</BODY>
</HTML>
```

对 `sample_page2.php` 进行相同的更改，并确保保存两个文件。

接下来，再次访问这些页面并在页面上查看计数。

- 1. 打开网页浏览器并输入 `http://127.0.0.1/sample_page1.php`。

你会看到 HTML 页面，包含标题和一些文本，随后是你的访问计数。在本示例中，我访问了这个页面 5 次。

# 无用的示例页面 #1

此示例页面没有实际用途！
Accesses: 5

- 2. 打开网页浏览器并输入 `http://127.0.0.1/sample_page2.php`。

你会看到 HTML 页面，包含标题和一些文本，随后是你的访问计数。在本示例中，我访问了这个页面 7 次。

在下一节中，你创建一个访问报告，可以使用它检查你在 `page_track` 表中跟踪的页面状态。

# 创建你的访问报告

你在 `page_track` 表中拥有所有这些数据，现在是时候创建一个简单的页面来为你统计全部了。不需要筛选 Apache 访问日志或安装额外的软件包来为你显示统计数据！

从创建跟踪页面的总访问次数（包含全部）开始。

- 1. 在文本编辑器中打开一个新文件并开始 PHP 块：

```php
<?
```

- 2. 创建变量来存储表所在的数据库以及表本身：

```php
$db_name = "testDB";
$table_name = "page_track";
```

- 3. 添加你已有的连接信息：

```php
$connection = @mysql_connect("localhost", "spike", "9j7En4");
or die(mysql_error());
```

- 4. 按照你学到的选择数据库：

`$db = @mysql_select_db($db_name, $connection) or die(mysql_error());`

- 5. 创建一个计算 `page_track` 表中所有条目的 SQL 语句：

```php
$count_sql = "select count(page_name) from $table_name";
```

- 6. 执行查询：

```php
$count_res = @mysql_query($count_sql,$connection) or die(mysql_error());
```

- 7. 创建变量来存储当前结果集中的特定计数，然后关闭 PHP 块：

`$all_count = @mysql_result($count_res, 0, "count(page_name)");
?>

- 8. 添加此 HTML：

```html
<HTML>
<HEAD>
<TITLE>My Access Report</TITLE>
</HEAD>
<BODY>
<h1>My Access Report</h1>
```

- 9. 混合 HTML 和 PHP 来打印表名以及表中跟踪的访问次数：

`<P><strong>Total Accesses Tracked in <?php echo "\$table_name"; ?>:</strong> <?php echo "\$all_count"; ?></p>`

- 10. 添加更多 HTML 以使文档有效：

```html
</BODY>
</html>
```

- 11. 将文件保存为 `access_report.php`，并将其放置在 Web 服务器的文档根目录下。

你的代码看起来应该是这样的：

```php
php
// set up table and database names
$db_name = "testDB";
$table_name = "page_track";

// connect to server and select database
$connection = @mysql_connect("localhost", "spike", "9j7En4");
or die(mysql_error());
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());

// issue query and select results
$count_sql = "select count(page_name) from $table_name";
$count_res = @mysql_query($count_sql,$connection) or die(mysql_error());
$all_count = @mysql_result($count_res, 0, "count(page_name)");
?>
```

```html
<HTML>
<HEAD>
<TITLE>My Access Report</TITLE>
</HEAD>
<BODY>
<h1>My Access Report</h1>h1>
<P><strong>Total Accesses Tracked in <?php echo "\$table_name"; ?>:</strong> <?php echo "\$all_count"; ?></p>
</BODY>
</html>
```

接下来，测试它！打开网页浏览器并输入 `http://127.0.0.1/access_report.php`。





## 428 第 24 章：创建自定义日志和报告

## 显示用户代理 (User Agents)

在本节中，你将对 `access_report.php` 脚本进行一些微调，以显示并统计访问页面的用户使用的不同网络浏览器。

- 1. 在文本编辑器中打开 `access_report.php`。
- 2. 在关闭 PHP 标签之前，创建一个 SQL 语句，查找 `page_track` 表中 `user_agent` 字段的所有唯一条目，统计这些条目，并按降序返回结果：

```
$user_agent_sql = "select distinct user_agent, count(user_agent) as count from table_name group by user_agent order by count desc";
```

- 3. 执行查询：

```
$user_agent_res = @mysql_query($user_agent_sql, $connection)
or die(mysql_error());
```

- 4. 稍后将在一个 `while` 块中创建一个项目符号列表。先在 `while` 块之外开始该列表：

```
$user_agent_block = "<ul>";
```

## 429 使用 MySQL 进行简单的访问计数

- 5. 启动 `while` 循环。该循环将为结果集 ($user_agent_res) 中的每条记录创建一个名为 $row_ua 的数组：

```
while ($row_ua = mysql_fetch_array($user_agent_res)) {
```

- 6. 获取记录的各个元素并给它们起好的名称：

```
$user_agent = $row_ua['user_agent'];
$user_agent_count = $row_ua['count'];
```

- 7. 通过创建一个项目符号和一个额外的项目列表，向 `$user_agent_block` 中添加内容。项目符号将显示用户代理的名称。然后，第二个项目列表将显示该特定用户代理的访问次数。添加到 `$user_agent_block` 后，关闭 `while` 循环：

```
$user_agent_block .= "
  <li>$user_agent
  <ul>
    <li>$accesses per browser: $user_agent_count</li>
  </ul>
";
```

- 8. 关闭你在 `$user_agent_block` 中创建的项目符号列表：

```
$user_agent_block .= "</ul>";
```

- 9. 在 HTML 部分添加以下内容，然后保存文件：

```
<p><<strong>>所使用的网络浏览器：</strong></p>
<?php echo "$user_agent_block"; ?>
```

你的新代码看起来应该是这样的：

```php
<?php
// 设置表名和数据库名
$db_name = "testDB";
$table_name = "page_track";

// 连接到服务器并选择数据库
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

## 430 第 24 章：创建自定义日志和报告

```php
// 发布查询并选择计数结果
$count_sql = "select count (page_name) from $table_name";
$count_res = @mysql_query($count_sql, $connection) or die(mysql_error());
$all_count = @mysql_result($count_res, 0, "count(page_name)");
```

```php
// 用户查询并选择用户代理结果
$user_agent_sql = "select distinct user_agent, count(user_agent) as count
from $table_name group by $user_agent order by count desc";
$user_agent_res = @mysql_query($user_agent_sql, $connection)
or die(mysql_error());
```

```php
// 开始用户代理显示块
$user_agent_block = "<ul>";
```

```php
// 循环遍历结果
while($row_ua = mysql_fetch_array($user_agent_res)) {
  $user_agent = $row_ua['user_agent'];
  $user_agent_count = $row_ua['count'];
  $user_agent_block .= "<li>$user_agent
  <ul>
    <li>accesses per browser: $user_agent_count</li>
  </ul></li>";
}
// 结束用户代理块
$user_agent_block .= "</ul>";
?>
<html>
<head>
<title>我的访问报告</title>
</head>
<body>
<h1>我的访问报告</h1>
<p>在 <?php echo $table_name; ?> 中跟踪的访问总数：<?php echo $all_count; ?></p>
<p><<strong>>所使用的网络浏览器：</strong>
<?php echo "$user_agent_block"; ?></p>
</body>
</html>
```

## 431 使用 MySQL 进行简单的访问计数

让我们看看哪些用户代理访问了你的页面。打开你的网络浏览器并输入 `http://127.0.0.1/access_report.php`。

你将看到一个 HTML 页面，随后是一个标题和一些文本，然后是所有页面的访问计数。你还将看到一个用户代理列表以及每种类型的总访问次数。在这个示例中，我使用两个不同的浏览器共访问了两次示例页面。

在下一节中，我们将对 `access_report.php` 进行最后的修改，显示具体的页面明细。

## 显示特定页面

在本节中，你将对 `access_report.php` 脚本进行一些微调，以提供 `page_track` 表中跟踪的页面明细。

- 1. 在文本编辑器中打开 `access_report.php`。
- 2. 在关闭 PHP 标签之前，创建一个 SQL 语句，查找 `page_track` 表中 `page_name` 字段的所有唯一条目，统计这些条目，并按降序返回结果：

```sql
$page_name_sql = "select distinct page_name, page_desc,
count(page_name) as count from $table_name
group by page_name order by count desc";
```

- 3. 执行查询：

```php
$page_name_res = @mysql_query($page_name_sql)
```

432 第 24 章：创建自定义日志和报告

- 4. 稍后将在一个 `while` 块中创建一个项目符号列表。先在 `while` 块之外开始该列表：

```php
$page_name_block = "<ul>";
```

- 5. 启动 `while` 循环。该循环将为结果集 ($page_name_res) 中的每条记录创建一个名为 $row_pn 的数组：

```php
while ($row_pn = mysql_fetch_array($page_name_res)) {
```

- 6. 获取记录的各个元素并给它们起好的名称：

```php
$page_name = $row_pn['page_name'];
$page_desc = $row_pn['page_desc'];
$page_count = $row_pn['count'];
```

- 7. 通过创建一个项目符号和一个额外的项目列表，向 `$page_name_block` 中添加内容。项目符号将显示页面名称。然后，第二个项目列表将显示该页面的访问次数。添加到 `$page_name_block` 后，关闭 `while` 循环：

```php
$page_name_block .= "<li>$page_desc
<ul>
<li>accesses per page: $page_count</li>
</ul></li>";
```

- 8. 关闭你在 `$page_name_block` 中创建的项目符号列表：

```php
$page_name_block = "</ul>";
```

- 9. 在 HTML 部分添加以下内容，然后保存文件：

```html
<p><<strong>>单个页面：</strong></p>
<?php echo "$page_name_block"; ?>
```

你的新代码看起来应该是这样的：

```php
<?php
// 设置表名和数据库名
$db_name = "testDB";
$table_name = "page_track";
```

433 使用 MySQL 进行访问计数

```php
// 连接到服务器并选择数据库
$connection = @mysql_connect("localhost", "spike", "9sj7En4")
or die(mysql_error());
$db = @mysql_select_db($db_name, $connection) or die(mysql_error());
```

```php
// 发布查询并选择计数结果
$count_sql = "select count (page_name) from $table_name";
$count_res = @mysql_query($count_sql, $connection) or die(mysql_error());
$all_count = @mysql_result($count_res, 0, "count (page_name)");
```

```php
// 发布查询并选择用户代理结果
$user_agent_sql = "select distinct user_agent, count(user_agent) as count
from $table_name group by user_agent order by count desc";
$user_agent_res = @mysql_query($user_agent_sql, $connection)
or die(mysql_error());
```

```php
// 开始用户代理显示块
$user_agent_block = "<ul>";
```

```php
// 循环遍历结果
while($row_ua = @mysql_fetch_array($user_agent_res)) {
  $user_agent = $row_ua['user_agent'];
  $user_agent_count = $row_ua['count'];
  $user_agent_block .= "<li>$user_agent
  <ul>
    <li>accesses per browser: $user_agent_count</li>
  </ul></li>";
}
// 结束用户代理块
$user_agent_block .= "</ul>";
```

```php
// 发布查询并选择页面结果
$page_name_sql = "select distinct page_name, page_desc,
count(page_name) as count from $table_name
group by page_name order by count desc";
$page_name_res = @mysql_query($page_name_sql, $connection)
or die($mysql_error());
```

```php
// 开始页面名称显示块
$page_name_block = "<ul>";
```

434 第 24 章：创建自定义日志和报告

```php
// 循环遍历 $pn 结果
while ($row_pn = mysql_fetch_array($page_name_res)) {
  $page_name = $row_pn['page_name'];
  $page_desc = $row_pn['page_desc'];
  $page_count = $row_pn['count'];
  $page_name_block .= "<li>$page_desc
  <ul>
    <li>accesses per page: $page_count</li>
  </ul></li>";
}
// 结束页面名称块
$page_name_block = "</ul>";
?>
<html>
<head>
<title>我的访问报告</title>
</head>
<body>
<h1>我的访问报告</h1>
<p>在 <?php echo $table_name; ?> 中跟踪的访问总数：<?php echo $all_count; ?></p>
<p><<strong>>所使用的网络浏览器：</strong>
<?php echo "$user_agent_block"; ?></p>
<p><<strong>>单个页面：</strong>
<?php echo "$page_name_block"; ?></p>
</body>
</html>
```





# 使用 MySQL 进行简单的访问计数 435

![](img/be897bd1bfd4dab38767db24da2a794b_457_0.png)

你将看到一个带有标题和一些文本的 HTML 页面，随后是你在所有页面的访问计数。你还将看到用户代理列表以及每种类型的总访问次数。你将看到所有访问过的页面列表，以及每个页面的简短描述和单独访问计数。

这比翻阅 Apache 访问日志要简单得多，我不建议在数据库驱动的系统中使用访问日志。数据库连接的开销太大了，即使 MySQL 在你的系统上运行良好。相反，请将你的页面跟踪针对对你特别重要的内容。

在下一章中，你将处理另一个项目。你将进入访问控制的世界，并学习如何结合 MySQL 和 PHP 进行数据的存储和显示。

# 使用 XML

本章将带你对使用 XML 和 PHP 进行实上手介绍，但绝不将其视为该主题的权威指南！请将本章作为你可能决定进一步探索该主题的入门读读。在 PHP 5 中，所有与 XML 相关的内容都已完全重写，因此功能、效率和整体集成变得更加可靠且功能丰富。在本章中，你将学习如何：

- 创建基础 XML 文档结构
- 在 PHP 中使用 XML
- 解析并显示来自 XML 文件的内容

# 什么是 XML？

XML 的名称来自该语言的全称 Extensible Markup Language（可扩展标记语言）。尽管名称中包含“标记”（markup），但不要像对待 HTML 那样对待 XML。除了这两种语言都基于标签对之外，它们之间没有相似之处。XML 是一种数据交换方法，因为它在其边界内保留了定义良好的内容。另一方面，HTML 完全不在乎内容中包含什么或其如何结构——它的唯一目的是向浏览器显示内容。XML 用于定义和携带内容，而 HTML 用于让它变得“美观”。

这并不是说 XML 数据不能变得美观，或者你不能在网络浏览器中显示 XML 数据。事实上，这正是当你使用扩展样式语言 (XSL) 和级联样式表 (CSS) 将内容渲染为 Web 浏览器可以理解的格式，同时保留内容分类时，你所做的事情。例如，假设你的网站上有一个区域留给最近的系统消息，这些项目每个包含以下内容：

- 标题
- 消息
- 作者
- 消息日期

你可能想将标题**加粗**，消息显示为段落，作者姓名*斜体*，日期使用较小字体。为了这些，你会使用 HTML。而 XML 只关心是否有四个不同的内容元素。通过将数据及其结构与演示元素分离，你可以按照你想要的方式使用内容，而不受限于静态 HTML 强加给你的特定标记样式。

# 基础 XML 文档结构

在继续处理 XML 文档之前，你需要确切知道如何创建它们！XML 文档包含两个主要元素：引导（prolog）和正文（body）。引导包含 XML 声明语句（类似于 HTML 文档类型定义语句）以及你想添加的任何处理指令和注释。

## 注意

要了解 XML 文档的完整定义，请阅读 http://www.w3.org/TR/REC-xml 中的 XML 规范。

使用上一节的系统消息示例，打开文本编辑器并创建一个名为 messages.xml 的文件。输入：

```
<?xml version="1.0" ?>
<!-- Sample XML document -->
```

接下来，有趣的事情在文档的正文区域开始了——那里是内容的所在。XML 是层次结构的，就像书一样——书有标题和章节，每个章节包含段落，以此此类推。XML 文档中只有一个根元素。通过使用示例，该元素可能被称为 Book，标签 `<Book></Book>` 环围了所有其他信息。

但我在这里使用的是系统消息示例，所以将根元素命名为 SystemMessage，并在你的 messages.xml 文档中添加一个起始标签：

```
<SystemMessage>
```

接下来，向你的文档添加任何后续的子元素（children）。使用系统消息示例，你需要标题、主体、作者和日期信息。将子元素命名为 MessageTitle、MessageBody、MessageAuthor 和 MessageDate。但如果你想获取作者的名字和电子邮件地址呢？你只需要在父元素内部创建另一组子元素（它恰恰也是根元素的子元素）。例如，仅 `<MessageAuthor>` 元素看起来可能像这样：

```
<MessageAuthor>
<MessageAuthorName>Joe SystemGod</MessageAuthorName>
<MessageAuthorEmail>systemgod@someserver.com</MessageAuthorEmail>
</MessageAuthor>
```

总之，你的示例 messages.xml 文档看起来可能像这样：

```
<?xml version="1.0" ?>
<!--Sample XML document -->
```

# 440 第 25 章：使用 XML

```
<SystemMessage>
<MessageTitle>System Down for Maintenance</MessageTitle>
<MessageBody>Going down for maintenance soon!</MessageBody>
<MessageAuthor>Joe SystemGod</MessageAuthor>
<MessageAuthorEmail>systemgod@someserver.com</MessageAuthorEmail>
<MessageDate>March 4, 2004</MessageDate>
</SystemMessage>
```

创建 XML 时要记住两个非常重要的规则：

- XML 是区分大小写的，且 XML 标签必须正确关闭
- 所有 XML 标签必须正确嵌套

下图显示了原始的 messages.xml。

![](img/be897bd1bfd4dab38767db24da2a794b_462_0.png)

# 为在 PHP 中使用 XML 准备

![](img/be897bd1bfd4dab38767db24da2a794b_463_0.png)

# 第 25 章：使用 XML

![](img/be897bd1bfd4dab38767db24da2a794b_464_0.png)

PHP 中的 XML 功能基于 libxml 库，并在 Linux/Unix 和 Windows 上默认启用。你可以通过查看 phpinfo() 函数的输出来确定你的安装是否启用了 XML。

一旦确认 PHP 启用了 XML，你就可以解析、转换甚至生成 XML。本章中的所有示例都是基础性的，如果你对深度使用 XML 感兴趣，建议阅读额外的书籍或 PHP 手册（http://www.php.net/manual/）。

# 使用 PHP 解析 XML

在本节中，你将看到关于 PHP 如何使用 messages.xml 文件解析的示例。这些脚本展示了使用 PHP 解析 XML 的简单方法。

1. 在你的文本编辑器中打开新文件并启动 PHP 块：

```
<?php

2. 使用 simplexml_load_file() 函数将 messages.xml 文件的内容加载到名为 $xml 的对象中：

```
$xml = simplexml_load_file('messages.xml');
```

3. 使用 var_dump() 函数打印对象中的所有元素名和值，然后关闭 PHP 块：

```
var_dump($xml);
?>
```

4. 将文件保存为 xmlload.php 并将其放在 Web 服务器的文档根，与 messages.xml 文件一起。

当你用浏览器访问此文件时，你将看到如下图所示。

![](img/be897bd1bfd4dab38767db24da2a794b_465_0.png)

这种并不美观的输出表明 XML 解析器已经读取了文件，识别了 MessageTitle 等元素，并读取了元素的值。在下一节中，你将看到如何将 XML 元素映射到特定的 HTML 标记，最终以演示格式显示这些信息。




## 解析并显示 XML 文件内容

在本节中，你将创建一个脚本，将 HTML 标记映射到 XML 元素，最终显示你通常在网络浏览器中看到的内容。此示例使用了一个名为 `books.xml` 的 XML 文件，它存储了书籍列表和出版信息。在这个示例中，列表包含我的三本书，其元素如下：

- BookStore（书店）
- Book（书籍）
- BookTitle（书名）
- BookAuthor（作者）
- BookPublisher（出版商）
- BookISBN（ISBN）
- BookPrice（价格）

在开始编码之前，请创建一个 `books.xml` 文件并将以下内容其中（或你选择的任何书籍；只需遵循相同的结构）：

```xml
<xml version="1.0" ?>
<BookStore>
  <Book>
    <BookTitle>PHP 5 &amp; Easy Web Development</BookTitle>
    <BookAuthor>Julie Meloni</BookAuthor>
    <BookPublisher>Premier Press</BookPublisher>
    <BookISBN>1592004733</BookISBN>
    <BookPrice>29.99</BookPrice>
  </Book>
  <Book>
    <BookTitle>PHP Essentials, 2nd edition</BookTitle>
    <BookAuthor>Julie Meloni</BookAuthor>
    <BookPublisher>Premier Press</BookPublisher>
    <BookISBN>1931841349</BookISBN>
    <BookPrice>39.99</BookPrice>
  </Book>
  <Book>
    <BookTitle>PHP Fast &amp; Easy Web Development, 2nd edition</BookTitle>
    <BookAuthor>Julie Meloni</BookAuthor>
    <BookPublisher>Premier Press</BookPublisher>
    <BookISBN>193184187X</BookISBN>
    <BookPrice>29.99</BookPrice>
  </Book>
</BookStore>
```

XML 解析脚本的目标是将每个 XML 元素显示在一致的 HTML 标记中。在循环元素的过程中，我们会在它们的值周围包裹 HTML 标签——这就像你遍历数据库查询的 MySQL 结果集时做的一样！

1. 在你的文本编辑器中打开一个新文件并开始 PHP 块：

2. 使用 `simplexml_load_file()` 函数将 `books.xml` 的内容加载到名为 `$xml` 的对象中：

```php
$xml = simplexml_load_file('books.xml');
```

3. 开始一个 for 循环，查找刚刚解析的 XML 文件中的每个 `Book` 元素，并允许通过 `$Book` 访问：

```php
foreach($xml->Book as $Book) {
```

4. 开始 `echo` for 循环的输出：

```php
echo "*";
```

5. 输出书籍标题，将其包裹在 HTML 中：

```php
echo "<p><strong>".$Book->BookTitle."</strong><br>";
```

6. 输出书籍的作者信息，将其包裹在 HTML 中：

```php
echo "<em>by " . $Book->BookAuthor . ".</em><br>";
```

7. 输出书籍的出版商信息，将其包裹在 HTML 中：

```php
echo "(Published by " . $Book->BookPublisher . ").<br>";
```

8. 输出书籍的 ISBN，将其包裹在 HTML 中：

```php
echo "ISBN: " . $Book->BookISBN . ").<br>";
```

9. 输出书籍的价格，将其包裹在 HTML 中：

```php
echo "<font color=red>price:</font> "$" . $Book->BookPrice . ".</p>";
```

10. 通过添加分隔符、关闭大括号，然后关闭 PHP 块来完成 for 循环：

```php
    echo "<hr noshade>";
}
?>
```

将此文件保存为 `xmlparse.php`，并将其放在 Web 服务器的文档根目录下。整个脚本看起来像这样：

```php
<?php
$xml = simplexml_load_file("books.xml");
foreach($xml->Book as $Book) {
    echo "*";
    echo "<p><strong>".$Book->BookTitle."</strong><br>";
    echo "<em>by ".$Book->BookAuthor."</em><br>";
    echo "(Published by ".$Book->BookPublisher.",";
    echo "ISBN: ".$Book->BookISBN.")<br>";
    echo "<font color=red>price:</font> "$" ".$Book->BookPrice."</p>";
    echo "<hr noshade>";
}
?>
```

## 使用 PHP 解析 XML

当你用浏览器访问此文件时，你将看到如下图所示。

![](img/be897bd1bfd4dab38767db24da2a794b_469_0.png)

`xmlparse.php` 脚本提供了一个读取 XML 文档并处理它的基本示例。若要进一步学习这一概念，请查看 PHP 手册中的示例：

- DOM 函数文档位于：http://www.php.net/domxml
- SimpleXML 函数文档位于：http://www.php.net/simplexml

尽管本章结束了课程和项目，但书中还包含六个包含有用信息的附录。通用的 PHP 参考项目可以在前两个附录中找到，关于函数和对象的课程在附录 C 中。数据库规范一化和基础 SQL 参考可以在附录 D 中找到，PHP5 中的新元素——SQLite 在附录 E 中介绍。这些附录以附录 F“获取帮助”结束，它将引导你找到更多资源和教程的正确方向。

# 第八部分

# 附录

- 附录 A
额外的配置选项 ..... 451
- 附录 B
基础 PHP 函数参考 ....... 457
- 附录 C
编写你自己的函数
和对象 ......................... 493
- 附录 D
数据库规范
和 SQL 参考 ....................... 505
- 附录 E
使用 SQLite ............................ 521
- 附录 F
获取帮助 ......................... 531

## 附录 A：额外的配置选项

此行告诉 PHP 包括 MySQL 并构建动态模块。许多其他扩展和配置供你选择，其中你可能永远不会使用。表 A.2 列出了某些流行的扩展，如果你想查看扩展、配置选项以及更多信息，可以在 PHP 目录提示符下使用命令：

```bash
./configure --help
```

这将列出所有可用配置选项。记住，由于 PHP 是 Apache 的动态模块，在更改时不需要重新编译 Apache。

表 A.2 可用扩展

| 扩展 | 说明 |
| :--- | :--- |
| --disable-all | 禁用所有启用的扩展。 |
| --disable-libxml | 禁用 libXML 支持。 |
| --with-openssl[DIR] | 包含 OpenSSL 支持（需要 OpenSSL >= 0.9.6）。 |
| --with-zlib[DIR] | 包含 ZLIB 支持（需要 zlib >= 1.0.9）。 |
| --enable-bcmath | 启用 bc 精度数学函数。 |
| --with-curl[DIR] | 包含 CURL 支持。 |
| --enable-dbase | 启用内置库。 |
| --disable-dom | 禁用新的 DOM 支持。 |
| --enable-ftp | 启用 FTP 支持。 |
| --with-gd[DIR] | 包含 GD 支持，DIR 为 GD 安装路径。 |
| --with-jpeg-dir[DIR] | GD: 设置 libjpeg 安装路径。 |
| --with-png-dir[DIR] | GD: 设置 libpng 安装路径。 |
| --with-zlib-dir[DIR] | GD: 设置 libz 安装路径。 |
| --with-xpm-dir[DIR] | GD: 设置 libXpm 安装路径。 |
| --with-ttf[DIR] | GD: 包含 FreeType 1.x 支持。 |
| --with-freetype-dir[DIR] | GD: 设置 FreeType 2 安装路径。 |

## Windows 扩展

在 `php.ini` 中包含额外功能包括：

| 文件名 | 说明 |
| :--- | :--- |
| php_c.dll | Clib |
| php_curl.dll | CURL 支持 |
| php_gd.dll | GD 支持 |
| php_ifx.dll | Informix 支持 |
| php_ldap.dll | LDAP 支持 |
| php_hash.dll | mhash 支持 |
| php_mediedia.dll | Macromedia 支持 |
| php_mssql.dll | Microsoft SQL 支持 |
| php_oci8.dll | Oracle 支持 |
| php_openssl.dll | OpenSSL 支持 |
| php_pgsql.dll | PostgreSQL 支持 |
| php_sybase.dll | Sybase 支持 |

在更改 `php.ini` 后，重启 Web 服务器并检查 `phpinfo()` 输出以验证更改。

## Linux 配置选项

用于构建的配置行如下：

```bash
./configure --with-mysql--with-apxs=/usr/local/apache2/bin/apxs
```




# LINUX 配置选项 455

| 扩展 | 描述 |
| --- | --- |
| --with-informix=[DIR] | 包含 informix 支持。 |
| --with-ldap=[DIR] | 包含 LDAP 支持。 |
| --enable-multibstring | 启用多字节支持。 |
| --with-mcrypt=[DIR] | 包含加密支持。 |
| --with-mhash=[DIR] | 包含 mhash 支持。 |
| --with-mssql=[DIR] | 包含 MSSQL-DB 支持。DIR 为 FreeTDS 目录。 |
| --with-mysql=[DIR] | 包含 MySQL 支持。DIR 为 MySQL 基础目录。 |
| --with-oci=[DIR] | 包含 Oracle-oci8 支持。默认 DIR 为 ORACLE_HOME。 |
| --with-ibm-db2=[DIR] | 包含 IBM DB2 支持。DIR 为 DB2 基础。 |
| --with-custom-odbc=[DIR] | 包含用户定义的 ODBC 支持。DIR 为 ODBC 基础目录。 |
| --with-iodbc=[DIR] | 包含 ODBC 支持。DIR 为 iODBC 基础目录。 |
| --disable-posix | 禁用 POSIX 类函数。 |
| --disable-session | 禁用会话支持。 |
| --without-sqlite | 不包含 SQLite 支持。 |
| --with-sybase=[DIR] | 包含 Sybase-DB 支持。DIR 为 Sybase 目录。 |

有关关于 PHP 中 Linux/Unix 配置选项的更多信息，请参阅 PHP 手册中的安装与配置章节。

# PHP 基础语言参考

本附录的内容远没有 PHP 手册（位于 http://www.php.net/manual/）那么详尽，手册包含了每一个存在的 PHP 函数的描述、用户提交的注释和代码示例。相反，本附录作为一个基础的或“本质的”参考——它包含了（在我看来）你不可或的 PHP 元素。PHP 开发团队和所有文档贡献者对整个 PHP 手册都做了非常优秀的工作，没有必要重复轮子。然而，由于本附录仅涉及 PHP 知识点的一小部分，因此在向 PHP 邮件列表上提问之前，请先查阅 PHP 手册。

> 注意
在所有这些示例中，当函数中出现类似 string 或 int 的内容时，它是你自己的字符串或整数的占位符。

## PHP 开始和结束标签

为了将 PHP 代码与 HTML 结合，必须对 PHP 代码进行转义或从 HTML 中分离。PHP 引擎会将表 B.1 所示标签对之间的任何内容视为 PHP 代码。

| 开始标签 | 结束标签 |
| --- | --- |
| <?php | ?> |
| <? | ?> |
| <script language="php"> | </script> |

# 变量

你创建变量来表示数据。例如，以下变量存储了销售税的值：

```php
$sales_tax = 0.0875;
```

此变量存储了一个 SQL 语句：

```php
$sql = "SELECT * FROM MY_TABLE";
```

在确定新变量的值时，你可以引用其他变量的值：

```php
$tax_total = $sales_tax * $sub_total;
```

变量名如下：

- 它们以美元符号 ($ 开头。
- 它们不能以数字开头。
- 它们可以包含数字和下划线字符 (_)。
- 它们是大小敏感的。

以下是一些常见的变量类型：

- 浮点数 (floats)
- 整数 (integers)
- 字符串 (strings)

这些类型由 PHP 根据它们出现的上下文决定。

# 浮点数

以下每个变量都是浮点数（float）。浮点数也被带有小数点的数字。

```php
$a = 1.552;
$b = 0.964;
$sales_tax = 0.875;
```

# 整数

整数是正负整数、零或没有小数点的数字。每个每个都是整数：

```php
$a = 15;
$b = -521;
```

# 字符串

一组在双引号内的字符序列被视为字符串：

# 附录 B：PHP 基础语言参考

```php
$a = "I am a string";
$b = "<p>This book is <strong>cool</strong></p>";
```

你也可以在字符串中引用其他变量，这些变量会在脚本执行时被替换。例如：

```php
$num = 57; // 一个整数
$my_string = "I read this book $num times!"; // 一个字符串
```

当你运行脚本时，$my_string 变为 "I read this book 57 times!"

# HTML 表单变量

取决于你的 HTML 表单方法（GET 或 POST），变量将成为 $_POST 或 $_GET 超全局关联数组的一部分。输入字段的名称将成为变量名。例如，当使用 POST 方法发送表单时，以下输入将产生变量 $_POST[first_name]：

```html
<input type="text" name="first_name" size="20">
```

如果该表单的方法是 GET，则该变量将是 $_GET[first_name]。

# Cookie 变量

与表单变量一样，变量保存在一个名为 $_COOKIE 的超全局关联数组中。如果你设置了一个值为 Joe Smith 的 cookie user，如下所示

```php
SetCookie("user", "Joe Smith", time(+3600));
```

变量 user 将被放置在 $_COOKIE 中，其值为 Joe Smith。然后你通过引用 $_COOKIE[user] 来获取该值。

# 环境变量

当设置变量时，可以使用全局作用范围访问它。环境变量通常用于存储脚本运行环境的信息。例如：

```php
$user = $_SERVER['USER'];
```

# 数组

数组是值的集合。在 PHP 中，数组可以通过数字或字符串（称为关联数组）进行索引。

```php
$colors = array("red", "green", "blue");
$user = array("name" => "John", "age" => 30);
```

# 函数

函数是执行特定任务的代码块。使用 `function` 关键字定义并在需要时调用。

```php
function greet($name) {
    echo "Hello, $name!";
}

greet("World");
```

# 循环

循环用于多次执行代码块。PHP 中常见的循环有 `for`、`while` 和 `do-while`。

```php
for ($i = 0; $i < 5; $i++) {
    echo $i;
}

while ($i = 0; $i < 10) {
    echo $i++;
}
```

# 条件语句

条件语句允许你根据某些条件执行代码。常见的条件语句有 `if`、`elseif`、`else` 和 `switch`。

```php
if ($x > 10) {
    echo "x大于 10";
} elseif ($x == 10) {
    echo "x等于 10";
} else {
    echo "x小于 10";
}
```

# 常量

常量是在脚本执行期间不能更改的值。

# 错误处理

错误处理允许你处理脚本执行期间发生的错误。PHP 使用 `try`、`catch` 和 `finally` 块。

```php
try {
    // 可能会抛出错误的代码
} catch (Exception $e) {
    echo "捕捉错误: " . $e->getMessage();
} finally {
    // 始终执行的代码
}
```

# 类和对象

类是创建对象的模板。对象是类的实例。

```php
class Dog {
    public $name;
    public function __construct($name) {
        $this->name = $name;
    }
    public function bark() {
        echo $this->name . " says woof!";
    }
}

$myDog = new Dog("Rex");
$myDog->bark();
```

# 接口

接口是定义了类必须实现方法的特殊类。

# 特性

Trait 是单继承语言中的代码复用机制。

# 继承

继承允许一个类继承另一个类。

# 文件系统

PHP 提供了许多与文件系统交互的函数。

```php
file_put_contents("test.txt", "Hello World");
if (file_exists("test.txt")) {
    $content = file_get_contents("test.txt");
    echo $content;
}
```

# 数据库

PHP 可以连接到许多不同的数据库，最常用 MySQL。

```php
$mysqli = new mysqli("host", "username", "password", "database");
if ($mysqli->connect_error) {
    die("连接失败: " . $mysqli->connect_error);
}
```

# 安全

PHP 有许多用于安全的函数，例如密码哈希和输入过滤。

```php
$hash = password_hash("password", PASSWORD_DEFAULT);
if (password_verify("password", $hash)) {
    echo "密码有效！";
}
```





# 逻辑运算符

逻辑运算符允许你的脚本确定条件的状况，并在 `if...else` 或 `while` 语句中，根据哪些条件为真为假来执行特定的代码（参见表 B.6）。

| 表 B.6 逻辑运算符 |
| 运算符 | 示例 | 结果 |
| --- | --- | --- |
| ! | !a | 如果 $a 为假，则为真 |
| && | $a && $b | 如果 $a 和 $b 均为真，则为真 |
| || | $a || $b | 如果 $a 或 $b 其中之一为真，则为真 |

# 控制结构

程序本质上是一系列语句。控制结构顾如其名，控制这些语句的执行方式。它们通常围绕一系列条件构建，例如“如果天空是蓝色的，就去外面玩”。在这个例子中，条件是“如果天空是蓝色的”，语句是“去外面玩”。

控制结构利用大括号 {} 来将语句组与程序的其余部分隔离开。以下是常见控制结构的示例；记住它们将使你的生活变得简单得多。

# if...else if...else

`if...else...else` 结构根据所测试表达式的值来执行语句。在下面的 `if` 语句中，所测试的表达式是 "$a 等于 10"。

```
if ($a == "10") {
    // 执行某些代码
}
```

在求值 $a 后，如果发现它的值为 10（即如果条件为真），则大括号内的代码将执行。如果发现 $a 的值是 10 的其他值（如果条件为假），则忽略该代码，程序继续运行。

为了在 $a 的值不为 10 时提供另一种语句序列，可以在结构中添加一个 `else` 语句，以便在条件为假时执行部分代码：

```
if ($a == "10") {
    echo "a equals 10";
} else {
    echo "a does not equal 10";
}
```

`else`（或一个单词：`elseif`）语句可以添加到结构中，在进入最后的 `else` 语句之前评估另一个替代表达式。例如，以下结构首先评估 $a 是否等于 10。如果该条件为假，则评估 `else` 语句。如果发现为真，则执行其大括号内的代码。否则，程序继续执行最后的 `else` 语句：

```
if ($a == "10") {
    echo "a equals 10";
} else if ($b == "8") {
    echo "b equals 8";
} else {
    echo "a does not equal 10 and b does not equal 8.";
}
```

你可以单独使用 `if` 语句，也可以作为 `if...else` 或 `if...else if...else` 语句的一部分。无论你选择哪种，你都会发现这种结构是你程序中无价值的元素！

# while

与 `if...else if...else` 结构（每个表达式只评估一次并根据其真假值执行操作）不同，`while` 语句会继续循环直到表达式为假。换句话说，当表达式为真时，`while` 循环将继续。

例如，在下面的 `while` 循环中，只要 $a 的值小于或等于 3，就会在屏幕上打印 $a 的值并将其加 1：

```
$a = 0 // 设置起始点
while ($a <= "3") {
  echo "$a equals<br>";
  $a++;
}
```

# for

与 `while` 循环不同，`for` 循环在每次循环开始时评估条件表达式集。以下是 `for` 循环的语法：

```
for (expr1; expr2; expr3) {
  // 要执行的代码
}
```

在每个循环开始时，首先评估第一个表达式，然后评估第二个表达式。如果第二个表达式为真，循环通过执行代码并评估第三个表达式来继续。如果第二个表达式为假，则循环不再继续，第三个表达式永远不会被评估。

取 `while` 循环中使用的计数示例，使用 `for` 循环将其重写：

```
for ($a = 0; $a <= "3"; $a++) {
  echo "$a equals<br>";
}
```

# 内置函数

以下所有函数都是 PHP 语言构成的众多函数的一部分。这些真的只是少数几个 PHP 函数；它们是我经常使用的函数。根据你用 PHP 要要做的事情的类型，你可能不需要更多函数，但请访问 PHP 手册 http://www.php.net/manual/ 并熟悉可用内容。

# 数组函数

有许多函数可用于数组。这里只列出了几个——那些我认为是绝对必要的函数，以及那些构成了处理数组知识基础的函数。

# array()

`array()` 函数允许你手动为数组分配值。以下是 `array()` 函数的语法：

```
$array_name = array("val1", "val2", "val3", ...);
```

# array_push()

`array_push()` 函数允许你向现有数组末尾添加一个或多个元素。其语法为：

```
array_push($array_name, "element 1", "element 2", ...);
```

# array_pop()

`array_pop()` 函数允许你从现有数组移除最后一个元素。其语法为：

```
array_pop($array_name);
```

# array_unshift()

`array_unshift()` 函数允许你向现有数组开头添加元素。其语法为：

```
array_unshift($array_name, "element 1", "element 2", ...);
```

# array_shift()

`array_shift()` 函数允许你从现有数组移除第一个元素。其语法为：

```
array_shift($array_name);
```

# array_merge()

`array_merge()` 函数允许合并两个或多个数组。其语法为：

```
array_merge($array1, $array2, ...);
```

# array_keys()

`array_keys()` 函数返回现有数组中所有的键。其语法为：

```
array_keys($array_name);
```

# array_values()

`array_values()` 函数返回现有数组中所有的值。其语法为：

```
array_values($array_name);
```

# count()

`count()` 函数计算变量中的数量。通常用于计算数组中的元素数量。

在下面的示例中，$a 被赋值为 $colors 数组元素的数量：

$a = count($colors);

如果 $colors 包含蓝色、黑色、红色和绿色，$a 被赋值为 4。

# each() 和 list()

`each()` 和 `list()` 函数通常一起使用，用于遍历数组并返回其键和值。以下是它们的语法：

```

(arrayname);
list(val, val2, ...);
```

例如，当通过 GET 方法提交 HTML 表单时，每个键值对都存储在全局变量 $_GET 中。如果你的输入字段名为 first_name 和 last_name，且用户输入了 Joe 和 Smith，那么在 $_GET 数组中的表示如下：

```
$_GET["first_name"] = "Joe"
$_GET["last_name"] = "Smith"
```

你可以以此方式使用 `each()` 和 `list()` 函数遍历数组，打印每个元素的键值：

```
while (list($key, $val) = each($_GET)) {
  echo "$key has a value of $val<br>";
}
```

# reset()

`reset()` 函数将指针重置到数组开头。其语法为：

```
reset($array_name);
```

# shuffle()

`shuffle()` 函数随机化数组元素的顺序。其语法为：

```
shuffle($array_name);
```

# MySQL 连接函数

有许多 PHP 函数用于连接和查询 MySQL 服务器。以下是一些基础函数及其语法。请参阅 PHP 手册 http://www.php.net/manual/ 获取完整的 MySQL 函数列表——它们非常多！

# mysql_connect()

此函数打开与 MySQL 的连接。它需要服务器名、用户名和密码：

```
$connection = mysql_connect("servername", "username", "password");
```





## mysql_select_db()

此函数在 MySQL 服务器上选择一个数据库，供后续查询使用。它需要一个有效的已连接：

```
$db = mysql_select_db("myDB", $connection);
```

## mysql_query()

此函数发布 SQL 语句。它需要一个打开的数据库连接：

```
$sql_result = mysql_query("SELECT * FROM SOMETABLE",$connection);
```

## mysql_error()

当连接或查询出现问题时，此函数返回一个有意义的错误信息。它通常在 `die()` 函数中使用，如下所示：

```
$sql_result = mysql_query("SELECT * FROM SOMETABLE",$connection)
or die(mysql_error($connection));
```

## mysql_fetch_array()

此函数自动将 SQL 语句的结果行放入数组中：

```
$row = mysql_fetch_array($sql_result);
```

## mysql_num_rows()

此函数返回结果集中的行数：

```
$num = mysql_num_rows($sql_result);
```

## 日期和时间函数

PHP 的日期和时间函数让你能够轻松格式化时间戳，用于数据库查询和日历函数，也可以简单地在订单表收据上打印日期。

## date()

`date()` 函数根据给定的参数集格式化返回当前服务器时间戳。其语法为：

```
date(format, [timestamp]);
```

如果未提供 `timestamp` 参数，则假设当前时间戳。表 B.7 显示了可用格式。

## checkdate()

`checkdate()` 函数验证给定的日期。验证成功意味着该日期在 0 到 32767 之间，月份在 1 到 12 之间，且每个月的天数正确（已考虑闰年）。其语法为：

```
checkdate(month, day, year);
```

## mktime()

`mktime()` 函数将给定日期的 Unix 时间戳返回为长整数（格式为自纪元，即 1970 年 1 月 1 日起的秒数）。因此，使用 `mktime()` 的目的是格式化日期，为数学函数和日期验证做准备。其语法为：

```
mktime(hour, minute, second, month, day, year);
```

## time() 和 microtime()

`time()` 函数返回当前系统时间，以自纪元起的秒数。`time()` 的语法简单为：

```
time();
```

### 表 B.7 date() 函数格式

| 字符 | 含义 |
|---|---|
| a | 打印 "am" 或 "pm" |
| A | 打印 "AM" 或 "PM" |
| h | 12 小时制小时 (01 到 12) |
| H | 24 小时制小时 (00 到 23) |
| g | 不带前导零的12 小时制小时 (1 到 12) |
| G | 不带前导零的24 小时制小时 (0 到 23) |
| i | 分钟 (00 到 59) |
| s | 秒 (00 到 59) |
| Z | 秒单位的时区偏移 (-43200 到 43200) |
| U | 自纪元起的秒数 (GMT 1970 年 1 月 1 日 00:00:00) |
| d | 两位数字日期 (01 到 31) |
| j | 不带前导零的两位数字日期 (1 到 31) |
| D | 文本格式的星期 (Mon 到 Sun) |
| l | 长文本格式的星期 (Monday 到 Sunday) |
| w | 数字格式的星期，周日到周六 (0 到 6) |
| F | 长文本格式的月份 (January 到 December) |
| m | 两位数字月份 (01 到 12) |
| n | 不带前导零的两位数字月份 (1 到 12) |
| M | 三字母文本的月份 (Jan 到 Dec) |
| Y | 四位数年份 (2000) |
| y | 两位数年份 (00) |
| z | 年中的天数 (0 到 365) |
| t | 给定月份的天数 (28 到 31) |
| s | 英语序数后缀 (th, nd, st) |

你可以得到类似 958950466 的结果。使用 `microtime()` 会增加微秒计数，因此不是只接收像 958950466 的结果，而是会得到类似 0.93121600 958950466 的结果，即在你请求自纪元以来时间的精确时刻（包含秒和微秒）。

## 文件系统函数

内置的文件系统函数是非常强大的工具——如果使用不当，它们就是武器。使用文件系统函数时要非常小心，特别是当你将 PHP 配置为 root 或某些系统级用户身份运行时。例如，在目录结构的根级别运行执行 `rm -R` 命令的 PHP 脚本将是非常糟糕的。

## chmod(), chgrp(), 和 chown()

与同名命令一样，`chmod()`、`chgrp()` 和 `chown()` 函数用于修改权限。（注：原文此处存在大量重复，翻译时已合并）。





# 478 附录 B：PHP 基础语言参考

> 注意

此信息值得强调：在发送 `header()` 之前，不要尝试向浏览器发送任何类型的信息。你可以在 `header()` 之前执行任何类型的数据库操作或其他计算，但你不能向屏幕打印任何内容——即使是一个换行符也不行。

例如，使用 `header()` 函数将用户重定向到新位置，请使用此代码：

```
header("Location: http://www.newlocation.com")
exit;
```

> 提示

在 `header()` 语句后紧跟 `exit` 命令。这可以确保代码不会继续执行。

# setcookie()

setcookie() 函数向用户发送 cookie。cookie 必须在向 Web 浏览器发送任何其他头头部信息之前发送。setcookie() 的语法为

```
setcookie("name", "value", "expire", "path", "domain", "secure");
```

例如，你可以使用以下代码发送一个名为 `username` 的 cookie，其值为 `joe`，该 cookie 在 `testcompany.com` 域名的所有目录下均在一小时内有效：

```php
setcookie("username","joe", time()+3600, "/", ".testcompany.com");
```

# Mail 函数

PHP mail 函数让你的 HTML 表单与服务器外发邮件程序之间的接口变得轻而易举！

如果你的服务器可以访问 sendmail 或外部 SMTP 服务器，`mail()` 函数将向指定的收件者发送邮件。它的语法为

```
mail("recipient", "subject", "message", "mail headers");
```

例如，以下代码将向 `julie@thickbook.com` 发送邮件，主题为“I'm sending mail!”，正文内容为“PHP is cool!”。`From` 行是额外邮件头头部信息的一部分：

```php
mail("julie@thickbook.com", "I'm sending mail!",
"PHP is cool!", "From:youmail@yourdomain.com\n");
```

# 数学函数

由于我几乎没有数学天分，我发现 PHP 的内置数学函数至关重要！除了所有函数外，π 的值（3.14159265358979323846）在 PHP 中已经被定义为常量 (M_PI)。

# ceil()

ceil() 函数将小数向上取整到下一个整数。它的语法为

```
ceil(number);
```

# decbin() and bindec()

decbin() 和 bindec() 函数分别将十进制数转换为二进制，并将二进制数转换为十进制。这些函数的语法为

```
decbin(number);
bindec(number);
```

# deche() and hexdec()

deche() 和 hexdec() 函数分别将十进制数转换为十六进制，并将十六进制数转换为十进制。这些函数的语法为

```
deche(number);
hexdec(number);
```

# decoct() and octdec()

decoct() 和 octdec() 函数分别将十进制数转换为八进制，并将八进制数转换为十进制。这些函数的语法为

```
decoct(number);
octdec(number);
```

# floor()

floor() 函数将小数向下取整到上一个整数。它的语法为

```
floor(number);
```

# number_format()

number_format() 函数返回指定数字的格式化版本。它的语法为

```
number_format("number", "decimals", "dec_point", "thousands_sep");
```

例如，要返回数字 12156688 的格式化版本，保留两位小数，并用逗号分隔每千位，请使用

```php
echo number_format("12156688","2",".",",");
```

结果是 12,156,688.00。

如果只提供一个数字，默认格式不使用小数点，并在每千位组之间放置逗号。

# pow()

pow() 函数返回给定数字的指定指数幂的值。它的语法为

```
pow(number, exponent);
```

# rand()

rand() 函数从特定的数字范围内生成随机值。它的语法为

```
rand(min, max);
```

# round()

round() 函数将小数四舍五入到下一个更高或更低的整数。它的语法为

```
round(number);
```

# sqrt()

sqrt() 函数返回给定数字的平方根。它的语法为

```
sqrt(number);
```

# srand()

srand() 函数为随机数生成器提供一组可能的数值。它的语法为

```
srand(seed);
```

通常的做法是使用微秒数为随机数生成器种子：

```php
srand((double)microtime()*1000000);
```

# 杂项函数

die() 和 exit 函数提供了对脚本执行的有效控制，为编程错误提供了退出机制。其他函数也被归入这一杂项类别。

# die()

die() 函数输出给定的消息并在返回值为 false 时终止脚本。它的语法为

```
die("message");
```

例如，你可以使用以下代码在连接数据库失败时打印消息并停止脚本执行：

```php
$connection = mysql_connect("servername", "password")
die("Can't connect to database.");
```

# exit

exit 语句终止当前脚本的执行。

# sleep() and usleep()

sleep() 和 usleep() 分别让程序暂停指定的秒数或微秒。sleep() 的语法为

```
sleep(seconds);
```
usleep(microseconds);

# uniqid()

uniqid() 函数根据指定的前缀生成一个唯一标识符。它的语法为

```
uniqid(prefix, more_entropy);
```

例如，你可以使用以下代码生成一个基于时间的唯一 ID：

```php
$id = uniqid("myuser_");
```





# 会话处理函数

会话处理是在用户浏览你的网站时保留数据的一种方式。数据可以是变量或整个对象。这些简单的函数只是 PHP 中与会话相关的函数之一；更多信息请参阅 PHP 手册 http://www.php.net/manual/。

# session_start()

session_start() 函数在会话尚未启动时启动一个新会话，或者如果用户存在会话 ID，则恢复该会话。该函数不接受任何参数，只需在代码的开头放置以下内容即可调用：

```
session_start();
```

# session_destroy()

session_destroy() 函数可以有效销毁为当前会话注册的所有变量和值。该函数不接受任何参数，只需在代码中放置以下内容即可调用：

```
session_destroy();
```

# 字符串函数

这一部分仅是 PHP 内置字符串处理函数的浅尝，但如果你理解了这些常用函数，你的编程将会变得简单得多！

# addslashes() 和 stripslashes()

在从数据库插入和检索数据时，addslashes() 和 stripslashes() 函数非常重要。通常插入到数据库的文本将包含特殊字符（单引号、双引号、反斜杠、NULL），在插入之前必须对其进行转义。addslashes() 函数正是此作用，使用如下语法：

```
addslashes(string);
```

同样，stripslashes() 函数返回一个去掉反斜杠的字符串，使用如下语法：

```
stripslashes(string);
```

# chop(), ltrim(), 和 trim()

这三个函数都会移除字符串中的多余空格。chop() 函数移除字符串末尾的空格，ltrim() 移除字符串开头的空格。trim() 函数则移除字符串开头和结尾的空格。以下是这些函数的语法：

```
chop(string);
ltrim(string);
trim(string);
```

# echo()

echo() 函数返回输出。echo() 的语法为

```
echo (parameter 1, parameter 2, ...)
```

例如：

```
echo "I'm using PHP!"; // 输出为: I'm using PHP!
echo 2+6;             // 输出为: 8
```

使用 echo 时不需要括号。

# explode() 和 implode()

explode() 根据指定的分隔符分割字符串并返回数组中的值。explode() 的语法为

```
explode("separator", "string");
```

例如，以下代码取一个名为 $color_list 的字符串（其包含用逗号分隔的颜色列表），并将每个颜色放入名为 $my_colors 的数组中：

```
$my_colors;
```

$color_list = "blue,black,red,green,yellow,orange";
$my_colors = explode(",", $color_list);
```

相反，implode() 函数接收数组并使用指定的分隔符将其字符串。implode() 的语法为

```
implode("separator", "string");
```

例如，以下代码取一个名为 $color_list 的数组，然后创建一个名为 $my_colors 的字符串，其中包含 $color_list 数组的值，并用逗号分隔：

```
$my_colors = implode(",", $color_list);
```

# htmlspecialchars() 和 htmlentities()

htmlspecialchars() 和 htmlentities() 将字符串中的特殊字符和 HTML 实体转换为可接受的实体表示。htmlspecialchars() 函数仅转换小于号 (< 变为 &lt;)、大于号 (> 变为 &gt;)、双引号 (" 变为 &quot;) 和符号 (& 变为 &amp;)；

htmlentities() 函数将 ISO-8859-1 字符集中的字符转换为正确的 HTML 实体。以下是这些函数的语法：

```
htmlspecialchars(string);
htmlentities(string);
```

# nl2br()

nl2br() 函数将所有 ASCII 换行符替换为 HTML 换行符 (<BR>)。nl2br() 函数的语法为

```
nl2br(string);
```

# sprintf()

sprintf() 函数返回根据表 B.9 列出的指令格式化的字符串。sprintf() 的语法为

```
sprintf(directives, string);
```

| 指令 | 结果 |
| --- | --- |
| % | 添加百分号 |
| b | 将字符串视为整数并格式化为二进制数 |
| c | 将字符串视为整数并用 ASCII 值格式化 |
| d | 将字符串视为整数并格式化为十进制数字 |
| f | 将字符串视为双精度浮点数并格式化为浮点数 |
| o | 将字符串视为整数并格式化为八进制数 |
| s | 将字符串视为字符串并格式化 |
| x | 将字符串视为整数并格式化为十六进制数（小写） |
| X | 将字符串视为整数并格式化为十六进制数（大写） |

例如，要将数字 5 转换为 $5.00（五美元），请使用：

```
$newnumber = sprintf("%0.02f", 5);
```

# strlen()

strlen() 函数返回给定字符串的长度。其语法为

```
strlen(string);
```

# strtolower()

strtolower() 函数返回一个所有字母文字母均转换为小写的给定字符串。其语法为

```
strtolower(string);
```

# strtoupper()

strtoupper() 函数返回一个所有字母文字母均转换为大写的给定字符串。其语法为

```
strtoupper(string);
```

# substr()

substr() 函数返回字符串的一部分。其语法为

```
substr(string, start, length);
```

# strreplace()

strreplace() 函数将搜索字符串出现替换为替换字符串。其语法为

```
strreplace(search, replace, string);
```

# ltrim()

ltrim() 函数移除字符串开头的空格。其语法为

```
ltrim(string);
```

# rtrim()

rtrim() 函数移除字符串末尾的空格。其语法为

```
rtrim(string);
```

# trim()

trim() 函数移除字符串开头和结尾的空格。其语法为

```
trim(string);
```

# arraypos()

arraypos() 函数在数组中查找针（needle）的索引。其语法为

```
arraypos(array, needle, [start]);
```





> `return` 语句可以出现在函数的任何位置，但在使用它时，它会结束函数的执行。这意味着被执行的代码是你脚本中调用 `return` 语句的那一行代码。

当你使用 `return` 语句时，你可以在代码中像这样调用该函数：

```php
echo multiplier(5);
```

这种用法将在你的屏幕上显示以下内容：

40

因为你将 `8` 作为 `$num` 参数传递给 `multiplier()` 函数，所以 `$answer` 变成了 `40`。因为 `$answer` 作为函数操作的结果被返回了，而且你使用了 `echo` 紧跟函数调用，你实际上是在告诉 PHP 打印函数内部代码的结果。在这种情况下，该结果就是数字 40。

> 你也可以使用 `return` 语句来获取多个值，但前提是它们是数组或对象的一部分。

使用 `return` 语句将函数结果传递给主脚本是一种简单且安全的方法，也是最常用的方法之一。如果你不使用 `return` 语句，就必须将任何想要传回主脚本的变量声明为全局变量（global）。例如：

```php
function multiplier($num) {
    global $answer;
    $answer = $num * 5;
}
```

在这种情况下，你调用了 `multiplier()` 函数，然后在 `echo` 语句中使用你的变量名，因为它没有直接从函数中返回。例如，使用修改后的函数，以下代码将在你的屏幕上打印数字 40：

```php
multiplier(5);
echo $answer;
```

如果你没有将 `$answer` 声明为全局变量，结果将是一个空白屏幕。

> 注意
有些人会通过思考来决定哪些变量是你真正想要全局应用于脚本的。每当你声明某个东西为全局变量时，你都必须采用额外的编程限制来维护数据的完整性。换句话说，你必须小心并注意你的一一行为。如果你声明了一个变量为全局变量，但在脚本的其他部分使用了同名的变量，你将覆盖其中一个。一个好的经验法是控制好你的全局变量，并将它们保持在直接使用它们的过程局部范围内。

# 在你的代码中使用函数

到为止，你已经学习了用户定义函数的基本结构，但还没有学习它是如何融入你自己的脚本的。对于 `multiplier()` 函数来说，为了在屏幕上打印一个数字而创建一个像下面这样的脚本似乎非常耗费时间：

```php
<?php
function multiplier($num) {
    $answer = $num * 5;
    return $answer;
}
echo multiplier(5);
?>
```

# 在你的代码中使用函数 497

相反，想象有一个名为 `db_connect()` 的函数，它包含了你的数据库连接和选择代码：

```php
function db_connect() {
    $connection = @mysql_connect("localhost", "spike", "9sj7En4")
    or die(mysql_error());
    $db = @mysql_select_db($db_name, $connection)
    or die(mysql_error());
}
```

与其在每个脚本中反复输入那两行代码，不如只需输入这个：

```php
db_connect();
```

如果你的主机名、用户名、密码或数据库名称发生变化，你只需要在一个地方更改这些信息——即 `db_connect()` 函数代码。现在的诀窍在于把这个函数放在哪里。显然，如果你创建一个函数是为了重用其内部的代码，你就不希望函数是脚本的一部分。相反，你将函数放在它自己的文件中（或包含其他函数的文件中），并使用 `include()` 或 `require()` 根据需要将信息拉取到你的脚本中。

# 使用 include() 和 require()

`include()` 和 `require()` 函数的作用基本上相同：当被调用时，被包含的文件中的代码成为调用它的脚本的一部分。从那时起，被包含文件中的任何内容都可以在调用它的脚本中使用。

`include()` 和 `require()` 之间的区别在无法打开的文件时出现。这通常是因为权限不正确，或者文件不在指定的位置。当使用 `include()` 发生失败时，你会得到一个警告，但代码会尽可能继续执行，也就是说，如果它需要另一个文件中的函数，执行就不会顺利！当 `require()` 无法找到或打开文件时，你将得到一个致命错误（fatal error），PHP 将完全停止处理代码。

# 498 附录 C：编写自己的函数和对象

包含的文件看起来与其他任何 PHP 文件一样，以 PHP 标签开始并以关闭 PHP 标签结束。例如，假设你有一个名为 `myfunctions.php` 的文件，包含以下代码：

```php
<?
/* multiplier() 函数将数字乘以 5 并返回它 */
function multiplier($num) {
    $answer = $num * 5;
    return $answer;
}

/* db_connect() 函数连接到我的数据库。 */
function db_connect() {
    $connection = mysql_connect("localhost", "spike", "9sj7En4");
    or die(mysql_error());
    $db = mysql_select_db($db_name, $connection)
    or die(mysql_error());
}
?>
```

那么，你需要连接数据库的实际 PHP 脚本将具有以下内容：

```php
<?php
// 包含文件
include("myfunctions.php");

// 调用函数
db_connect();

// 获取结果
echo multiplier(5);
?>
```

包含的文件与其他任何 PHP 文件一样，以 PHP 标签开始并以关闭 PHP 标签结束。例如，假设你有一个名为 `myfunctions.php` 的文件，包含以下代码：（见上文）。

# 操作对象

在书中，我偶尔提到“面向对象编程”，它是比本书所基于的过程脚本更复杂的编程类型。对象是一个理论上的盒子，包含了变量、函数等，存在于模板化的结构（类）中。现在，尝试将对象想象成一个带有输入和输出的小盒子。输入机制被称为*方法*（methods），方法拥有*属性*（properties）。在整个章节中，你将观察类、方法和属性如何共同工作以产生各种输出。如果你想在构建应用时采用这条路线，可以查阅 PHP 手册中的“类和对象”章节（http://www.php.net/manual/en/language.oop.php）获取更多信息。

# 创建对象

创建对象非常简单；你只需要声明它存在即可



```php
class myClass {
  //code will go here
}
```

现在你已经有了一个类，可以创建一个新的对象实例：

$object1 = new myClass();

下面的代码段向你展示了你的对象是否存在：

```php
<?php
class myClass {
  //code will go here
}
$object1 = new myClass();
echo "$object1 is an " . gettype($object1);
?>
```

如果你将此代码保存为 `objtest.php`，将其放在文档根目录下，并使用网络浏览器访问它，你将在屏幕上看到以下内容：

$object1 is an object

接下来，你将学习对象的属性和方法。

## 对象的属性

在对象内部声明的变量被称为属性。在类顶部声明变量是标准做法。这些属性可以是值、数组，甚至是其他对象。下面的片段在类内部使用了简单的标量变量，并以 `var` 关键字前缀：

```php
class myHouse {
  var $type = "condo";
  var $sqfootage = "786";
  var $color = "tan stucco";
}
```

现在，当你创建一个 `myHouse` 对象时，它将始终拥有这三个你可以引用的属性。下面的代码展示了它是如何工作的：

```php
<?php
class myHouse {
    var $type = "condo";
    var $sqfootage = "786";
    var $color = "tan stucco";
}
$house = new myHouse();
echo "I live in a " . $house->color . " " . $house->sqfootage . " square foot " . $house->type;
?>
```

如果你将此代码保存为 `myHouse.php`，将其放在文档根目录下，并使用网络浏览器访问它，你将在屏幕上看到以下内容：

I live in a tan stucco 786 square foot condo

## 对象方法

方法为你的对象添加了功能；对象不再仅仅包含属性，而是实际上会执行某些有用的操作。例如，下面的类输输出字符串：

```php
<?php
class anotherClass {
    function sayHello() {
        echo "HELLO!";
    }
}
$object1 = new anotherClass();
$object1->sayHello();
?>
```

如果你将包含此代码的文件放在文档根目录下并使用网络浏览器访问它，你将在屏幕上看到以下内容：

HELLO!

因此，方法看起来和作用起来像普通函数，但在类的框架内定义。`->` 运算符用于在脚本上下文中调用对象方法。如果对象中存储了任何变量，方法能够访问它们并供自己使用。例如：

```php
<?php
class anotherClass {
    var $name = "Joe";
    function sayHello() {
        echo "HELLO! My name is " . $this->name;
    }
}

$object1 = new anotherClass();
$object1->sayHello();
?>
```

如果你保存此代码并放在文档根目录下，然后使用网络浏览器访问，你将在屏幕上看到以下内容：

HELLO! My name is Joe

特殊变量 `$this` 用于引用当前实例对象。每当对象引用自身时，你必须使用 `$this` 变量。将 `$this` 变量与 `->` 运算符结合使用，允许你在类内部访问类的任何属性或方法。

## 构造函数

构造函数是一个存在于类内部的函数，当它的名称与类名相同时，在使用 `new classname` 创建类的新实例时它会被自动调用。使用构造函数允许你为类提供参数，并在类首次被调用时立即对其进行处理。你将在下一节看到构造函数的实际应用。

## 对象继承

在学习了对象、属性和方法的基础知识后，你可以开始研究对象继承。类的继承就如其名：一个类继承其父类的功能。这里展示了一个示例：

```php
<?php
class myClass {
    var $name = "Joe";
    function myClass($n) {
        $this->name = $n;
    }
    function sayHello() {
        echo "HELLO! My name is " . $this->name;
    }
}
class childClass extends myClass {
    //code goes here
}
$object1 = new childClass("Child of Joe");
$object1->sayHello();
?>
```

如果你保存此代码，将其放在文档根目录下，并使用网络浏览器访问它，你将在屏幕上看到以下内容：

HELLO! My name is Child of Joe

这些行构成了构造函数：

```php
function myClass($n) {
    $this->name = $n;
}
```

该函数与它所属的类相同：`myClass`。然后你看到 `childClass` 被定义，但它没有包含任何代码。在这个示例中，它旨在演示对父类的继承。继承通过使用 `extends` 子句实现，如下：

```php
class childClass extends myClass {
```

由于使用了这个子句，第二个类继承了第一个类的元素。像面向对象编程的大多数元素一样，继承在尝试让代码具有灵活时是非常用的。

## 附录 C：编写自己的函数和对象




你可能需要重复多次 `CourseID`、`CourseDescription` 和 `CourseInstructor` 列，以涵盖学生在学术生涯期间可能修的所有课程。虽然这是冗余的，但在创建存储信息的单一平表时使用的是这种方法。消除这种冗余是数据库规范化的第一步，因此接下来你会将此平表转换为第一范式。如果你的表格保持平坦化格式，可能会产生大量的未声明空间和不必要的空间占用——这不是一个高效的设计！

## 将表转换为第一范式

第一范式的主要规则如下：

- 消除重复信息
- 为相关数据创建单独的表

在平表设计中，由于学生和课程有许多重复的字段集，你可以将学生和课程识别为两个不同的主题。将学生和课程平表转换为第一范式意味着你将创建两个表：一个用于学生（命名为 `students`），另一个用于学生加课程（命名为 `students_courses`）。你可以在表 D.2 和表 D.3 中看到新的表设计。

| 表 D.2 students 表 |
| 字段名称 | 说明 |
| :--- | :--- |
| StudentID | 学生的唯一 ID。此新字段现在是主键。 |
| ColumnName | 学生的名字。 |

| 表 D.3 students_courses 表 |
| 字段名称 | 说明 |
| :--- | :--- |
| StudentID | 学生的唯一 ID，匹配 students 表中的某条目。 |
| CourseID | 学生所修课程的 ID。 |
| CourseDescription | 学生所修课程的描述。 |
| CourseInstructor | 学生所修课程的讲师。 |

你的两个新表代表了一个学生到多门课程的一对多关系。学生可以随心所欲地选择许多课程，而不限于平表中存在的 `CourseID`/`CourseDescription`/`CourseInstructor` 分组数量。

你仍然有些工作要做完成，下一步是将这些表放入第二范式。

## 将表转换为第二范式

第二范式的基本规则是

- 没有非键属性依赖于主键的一部分

用通俗易懂的话说，这意味着如果你表中的字段没有完全关联主键，你就必须继续对其进行处理。在学生和课程的示例中，这意味着将课程拆分到它们自己的表中，以便原始的平表变成一个充满唯一学生的表。

`CourseID`、`CourseDesc` 和 `CourseInstructor` 可以变成一个名为 `courses` 的表，主键为 `CourseID`。`students_courses` 表应该只包含两个字段：`StudentID` 和 `CourseID`。你可以在表 D.4 和表 D.5 中看到新的表设计。

| 表 D.4 courses 表 |
| 字段名称 | 说明 |
| :--- | :--- |
| CourseID | 课程的唯一 ID |
| CourseDescription | 课程描述 |
| CourseInstructor | 课程的讲师 |

## 理解数据库规范化 509

| 表 D.5 新的 students_courses 表 |
| 字段名称 | 说明 |
| :--- | :--- |
| StudentID | 学生的唯一 ID，匹配 students 表中的某条目。 |
| CourseID | 所修课程的唯一 ID，匹配 courses 表中的某条目。 |

信不信，你可以对这个示例进一步达到第三范式。

## 将表转换为第三范式

第三范式的规则是

- 没有属性依赖于其他非键属性

这条规则简单意味着你需要查看你的表，并确定是否存在可以进一步拆分且不依赖于键的字段。通常，一个讲师会教授多门课程。然而，`courses` 表中的 `CourseInstructor` 字段并不是任何类型的键。因此，如果你为了效率和维护将此信息拆分并创建一个单独的表，那就是第三范式。查看表 D.6 和表 D.7 中的新 `courses` 表和 `instructors` 表。

| 表 D.6 courses 表 |
| 字段名称 | 说明 |
| :--- | :--- |
| CourseID | 课程的唯一 ID |
| CourseDescription | 课程描述 |
| CourseInstructorID | 讲师 ID，匹配 instructors 表中的某条目 |

| 表 D.7 instructors 表 |
| 字段名称 | 说明 |
| :--- | :--- |
| InstructorID | 讲师的唯一 ID |
| InstructorName | 讲师的名字 |
| InstructorNotes | 关于讲师的任何备注 |

第三范式通常足以消除冗余并允许灵活和增长。接下来，我们将规范化本书之前使用的 `my_contacts` 表。

## 规范化 my_contacts 表

在原始的 `my_contacts` 表中，没有大量的重复信息，但如果你将其扩展为真正的地址簿，就很容易产生重复信息。在地址簿中，人们通常有家庭和工作的联系信息、多种电话方式（座机、手机等），甚至有多个电子邮件地址。将所有这些元素拆分到单独的表中并通过主键将信息附加到人会有意义得多。表 D.8 显示了原始的 `my_contacts` 表作为参考。

现在识别不同表所需的不同区域：地址（address）、电话（phone）和电子邮件（email）对于此示例已经足够。表 D.9、D.10 和 D.11 显示了这些新表的字段。

| 表 D.8 原始 my_contacts 表 |
| 字段名称 | 说明 |
| :--- | :--- |
| id | 学生的唯一 ID |
| f_name | 人的名字 |
| l_name | 姓 |
| address1 | 地址的第一行 |
| address2 | 地址的第二行 |
| address3 | 地址的第三行 |
| postcode | 邮编 |
| country | 居住国家 |
| prim_tel | 主电话号码 |
| sec_tel | 次电话号码 |
| email | 电子邮件地址 |
| birthday | 人的生日 |

| 表 D.9 address 表 |
| 字段名称 | 说明 |
| :--- | :--- |
| id | 地址的唯一 ID |
| contact_id | 匹配表中的某条目 |
| address1 | 地址的第一行 |
| address2 | 地址的第二行 |
| address3 | 地址的第三行 |
| postcode | 邮编 |
| address_type | 地址类型，例如家庭或工作 |

| 表 D.10 phone 表 |
| 字段名称 | 说明 |
| :--- | :--- |
| id | 电话的唯一 ID |
| contact_id | 匹配表中的某条目 |
| phone_number | 电话号码 |
| phone_type | 电话类型，例如家庭、工作或手机 |

| 表 D.11 email 表 |
| 字段名称 | 说明 |
| :--- | :--- |
| id | 电子邮件的唯一 ID |
| contact_id | 匹配表中的某条目 |
| email | 电子邮件地址 |
| email_type | 电子邮件类型，例如家庭或工作 |

| 表 D.12 新 my_contacts 表 |
| 字段名称 | 说明 |
| :--- | :--- |
| id | 条目的唯一 ID |
| f_name | 人的名字 |
| l_name | 姓 |
| birthday | 人的生日 |




在使用 `DROP` 命令时要极度小心，因为一旦删除数据库，所有的表也会被移除。

## 创建或删除表

你也可以使用 SQL `CREATE` 命令在当前数据库中创建表。其语法如下：

```
CREATE TABLE [yourTableName] ([fieldName1] [type],
[fieldName2] [type], ...) [options]
```

要从当前数据库中删除表，请使用 `DROP` 命令：

```
DROP TABLE [yourTableName];
```

在使用 `DROP` 命令时要极度小心，因为一旦删除了表，它们就消失了！

## 修改表

SQL `ALTER` 命令让你有机会修改特定表的元素，例如重命名列、更改列类型、删除列等。以下是一些常见的的用法：

- * 要向表中添加新列，请使用此命令：
ALTER TABLE [yourTableName] ADD [newColumn] [fieldDefinition]

- * 要从表中删除列，请使用此命令：
ALTER TABLE [yourTableName] DROP [columnName]

- * 要将列从一种类型更改另一种类型，请使用此命令：
ALTER TABLE [yourTableName] CHANGE [columnName] [newfieldDefinition]

- * 要在你的表中创建一个唯一列，请使用此命令：
ALTER TABLE [yourTableName] ADD UNIQUE ([columnName])

- * 要为表的列创建索引，请使用此命令：
ALTER TABLE [yourTableName] ADD INDEX [columnName] ([columnName])

使用 `ALTER` 命令减轻了仅仅因为拼写错误的字段名或犯了小错误而删除整个表并重新创建的需要。

## 在表内插入、更新或替换

SQL `INSERT` 和 `REPLACE` 命令每次向表中填充记录。`INSERT` 的语法为：

```
INSERT INTO [yourTableName] ([fieldName1], [fieldName2], ...)
VALUES ('value of fieldName1'), 'value of fieldName2');
```

在插入记录时，请确保用单引号或双引号分隔你的字符串。如果你在字符串周围使用单引号，且要添加的数据包含单引号（'），请在 `INSERT` 语句中使用转义单引号（`\'`）来避免错误。同样，如果你在字符串周围使用双引号并想将双引号作为数据的一部分，请在 `INSERT` 语句中转义它们（`\"`）。

这里有一个需要转义的字符串示例：

O'Grady said "Wow"

如果你用双引号包含字符串，`INSERT` 语句将如下所示：

```
INSERT INTO table_name (column_name) VALUES ("O'Grady said \"Wow\'");
```

如果你改用单引号包含字符串，`INSERT` 语句将如下所示：

```
INSERT INTO table_name (column_name) VALUES ('O\'Grady "Wow"');
```

`REPLACE` 语句与 `INSERT` 具有相同的语法和要求。区别在于，当替换基于唯一值时，你使用 `REPLACE` 来覆盖表中的记录：

```
REPLACE INTO [yourTableName] ([fieldName1], [fieldName2], ...)
VALUES ('value of fieldName1'), 'value of fieldName2');
```

`UPDATE` 命令修改记录的部分内容而不替换整条记录。要用相同的新值更新表中的整整列，请使用此命令：

```
UPDATE [yourTableName] SET [fieldName] = '[new value]';
```

如果你只想更新特定的行，请使用 `WHERE` 子句：

```
UPDATE [yourTableName] SET [fieldName] = '[new value'] WHERE [some expression];
```

`UPDATE` 可以是一个非常强大的 SQL 命令。例如，你可以在现有记录上执行字符串函数和数学函数，并使用 `UPDATE` 命令修改它们的值。

## 从表中删除数据

与 SQL `DROP` 命令一样，在不注意操作的情况下使用 `DELETE` 可能会生产环境中产生严重的后果。一旦删除了表或删除了记录，它将永远消失。不要害怕——只要小心即可。要删除表的全部内容，请使用以下命令：

```
DELETE FROM [yourTableName];
```

如果你只想删除特定的行，请使用 `WHERE` 子句：

```
DELETE FROM [yourTableName] WHERE [some expression];
```

如果你准备开始删除记录，请确保你已经备份，以防万一。每个人都会出错一次——希望以后再也不会。

## 从表中查询数据

在创建数据库驱动的网站时，SQL `SELECT` 命令可能是你工具箱中最频繁使用的命令。`SELECT` 命令根据你定义的标准选择表中的某些记录。以下是 `SELECT` 的基本语法：

```
SELECT [field names] FROM [table name]
WHERE [some expression]
ORDER BY [field names];
```

要选择表中的所有记录，请使用此命令：

```
SELECT * FROM [yourTableName];
```

要只选择表中给定列的项，请使用此命令：

```
SELECT [columnName] FROM [yourTableName];
```

要选择表中的所有记录并按特定顺序返回，例如，如果你有一个用于记录条的数据字段和一个用于 `ORDER BY` 的表达式，并且你想按从新到旧的顺序查看所有记录，请使用此命令：

```
SELECT * FROM [yourTableName] ORDER BY [dateField] DESC;
```

`DESC` 代表“降序”（descending）。要从旧到新，请使用 ASC 表示升序”（ascending）。`ASC` 是默认顺序。

你可以在 SQL 语句中执行数学和字符串函数（取决于你的数据库），从而使用 `SELECT`。

### 一些字符串函数

此列表仅包含少数字符串相关的函数：

- CONCAT: 合并值。
- LOWER: 将结果转换为小写。
- UPPER: 将结果转换为大写。

### 一些日期和时间函数

此列表仅包含少数日期相关的函数：

- DAYOFWEEK: 获取星期几（1 = 周日，2 = 周一）。
- WEEKDAY: 获取工作日几（0 = 周一，1 = 周二）。
- DAYOFMONTH: 获取月份中的日期（1 到 31）。
- DAYOFYEAR: 获取年份中的第几天（1 到 366）。
- MONTH: 获取月份（1 到 12）。
- MONTHNAME: 获取月份名称（January, February, ...）。
- DAYNAME: 获取星期名称（Monday, Tuesday, ...）。
- WEEK: 获取周（0 到 53）。
- YEAR: 获取年份（1000 到 9999）。

## 使用 show 命令

有几种类型的 `SHOW` 命令，它们会产生输出帮助你管理 MySQL。执行这些命令的常用方法是通过 MySQL 监器（MySQL Monitor），即 MySQL 的命令行界面，你在第 1 章“安装和配置 MySQL”中使用它。

基本的 `show` 命令是 `SHOW DATABASES` 和 `SHOW TABLES`，它们只需显示服务器上数据库和表的名称。如果你使用 `SHOW CREATE TABLE` 命令，它会向你显示创建指定表的精确 SQL 语句。

如果你需要知道表的结构但并不需要创建它的 SQL 命令，可以使用 `SHOW COLUMNS` 命令：

```
mysql> SHOW COLUMNS FROM [testTable];
```





为了管理目的，`SHOW STATUS` 和 `SHOW VARIABLES` 命令可以快速提供有关你的数据库服务器的重要信息。有关这些命令输出的许多行内容的更多信息，请阅读 MySQL 手册中的相关章节，地址为：http://www.mysql.com/doc/

## 使用 SQLite

在附录 D“数据库归一化与 SQL 引用”中，你学习了规范化数据库的重要性以及扁直文件的潜在问题。然而，在许多情况下，你的 PHP 应用可能只需要单个数据库表，而这并没有什么错。例如，假设你只是在对通过网站设置的简单联系表单内容进行存档，作为备份，以防邮件版本从未送达。这个简单的表可能包含姓名、电子邮件、评论和发送日期的实际字段——完全没有必要对其进行归一化！

如果你发现自己处于一个没有数据库且被规定不能安装数据库的环境中，PHP 5 引入了另一种选择——利用 SQLite 的能力，SQLite 是一种基于 SQL 接口的平面文件数据库。

## SQLite 运行示例

> 注意：PHP 5 默认启用了 SQLite。有关本附录未涵盖的详细信息，请访问 SQLite 网站 http://www.sqlite.org/，或在 PHP 手册中搜索 SQLite 部分：http://www.php.net/sqlite/。

要使用 SQLite，你仍然对数据库、表和字段如何协同工作以及 SQL 语法本身有基本的理解。你在书中学习的所有内容在连接数据库、发布查询和获取结果方面仍然有效——不同之处在于你学会了使用 MySQL 特有的函数向 MySQL 服务器发送命令。SQLite 有自己的一set函数，你用它们执行相同类型的任务。

本节将逐步介绍处理数据库的一些基本操作，并使用 SQLite 版本的方法。在执行任何操作之前，你必须创建一个数据库：

- 1. 在你的文本编辑器中打开一个新文件并开始 PHP 代码块：

- 2. 使用 `sql_open()` 函数打开位于文档根目录上一名为 `test.db` 的数据库——不要担心它尚未被创建，因为如果文件不存在，该函数将创建它。如果命令失败，`sql_error_string()` 函数将显示任何错误信息：

`$db = sql_open("./test.db") or die(sql_error_string());`

> 注意
你可能会注意到，创建或打开 SQLite 数据库不需要使用用户名或密码。这是事实，因为 SQLite 数据库实际上只是一个普通文件，除了对你放置文件的目录具有读写权限外，没有访问要求。

## SQLite 运行示例

- 3. 关闭 PHP 代码块：

```php
<?php ?>
```

将此文件保存为 `sqlite1.php` 并将其放在 浏览器的文档根目录下。访问脚本 http://127.0.0.1/sqlite1.php 来创建数据库。

> 注意
如果此脚本执行成功，将没有任何输出。只有当脚本执行失败时，你才会看到消息。

现在你已经有一个可以工作的 SQLite 数据库，可以继续创建表和发布查询了。

## 使用 SQLite 创建表和存储数据

当你使用 MySQL 创建表时（实际上，当你在任何关系数据库系统中创建表时），你会特地定义字段的类型和长度。例如，你可能定义了一个 25 字符的 `varchar` 字段名，或者一个名为 `start_date` 的 `datetime` 字段。SQLite 是松类型的，这意味着所有字段的内容无论其实际类型是什么，都存储为字符串。因此，在创建表时 SQLite 不需要定义字段，如果你定义了，它们也将被忽略。

在下一个示例中，你将创建一个包含名字、姓和电子邮箱的表，并向表中填充几条记录：

- 1. 在你的文本编辑器中打开一个新文件并开始 PHP 代码块：

```php
<?php ?>
```

- 2. 使用 `sqlite_open()` 函数打开之前创建的数据库：

```php
$db = sqlite_open("../test.db") or die(sqlite_error_string($db));
```

- 3. 使用 `sqlite_query()` 函数发布创建表的命令：

```php
sqlite_query($db, "CREATE TABLE my_friends (first_name, last_name, email)");
```

## 4. 使用 `sqlite_query()` 函数使用 SQL INSERT 命令添加几条条目：

```php
sqlite_query($db, "INSERT INTO my_friends" VALUES ('John', 'Smith', 'john@smith.com');
sqlite_query($db, "INSERT INTO my_friends" VALUES ('Jane', 'Doe', 'jane@doe.com');
sqlite_query($db, "INSERT INTO my_friends" VALUES ('Julie', 'Meloni', 'julie@thickbook.com');
```

## 5. 关闭 PHP 代码块：

完整的脚本应该像这样：

```php
<?php
$db = sqlite_open("../test.db") or die(sqlite_error_string($db));
sqlite_query($db, "CREATE TABLE my_friends (first_name, last_name, email)");
sqlite_query($db, "INSERT INTO my_friends" VALUES ('John', 'Smith', 'john@smith.com');
sqlite_query($db, "INSERT INTO my_friends" VALUES ('Jane', 'Doe', 'jane@doe.com');
sqlite_query($db, "INSERT INTO my_friends" VALUES ('Julie', 'Meloni', 'julie@thickbook.com');
?>
```

将此文件保存为 `sqlite2.php` 并将其放在 浏览器的文档根目录下。访问脚本 http://127.0.0.1/sqlite2.php 来发布这些 SQLite 命令。再次，如果脚本执行成功，将没有任何输出。只有当脚本执行一个或多个命令失败时，你才会看到消息。

在下一节中，你将从表中检索项目。

## 使用 SQLite 检索项目

现在你的 SQLite 表中有了记录，你就可以检索它们。同样，从 MySQL 表中检索数据的过程非常简单。

## SQLite 运行示例

- 1. 在你的文本编辑器中打开一个新文件并开始 PHP 代码块：

```php
<?php ?>
```

- 2. 使用 `sqlite_open()` 函数打开你之前创建的数据库：

```php
$db = sqlite_open("../test.db") or die(sql_error_string());
```

- 3. 使用 `sqlite_query()` 函数发布 SELECT 命令，旨在按名称升序检索记录：

```php
$r = sqlite_query($db, "SELECT * FROM my_friends ORDER BY_name");
```

- 4. 检查结果，如果查询失败则打印消息：

```php
if (!$r) {
    echo "Sorry, no records.";
}
```

- 5. 添加 while 循环来处理成功的查询。此循环将使用 `sqlite_fetch_array()` 函数，它的用法与书中使用的 `mysql_fetch_array()` 函数相似：

```php
while($record = sqlite_fetch_array($r)) {
```

- 6. 为你从表中提取的字段创建变量：

```php
$first_name = $record['first_name'];
$last_name = $record['last_name'];
$email = $record['email'];
```

- 7. 将每条记录打印到屏幕，并关闭 while 循环、if...else 块和 PHP 代码块：

```php
        echo "record: $last_name, $first_name ($email)<br>";
    }
}
?>
```

你的整个代码应该是：

```php
<?php
$db = sqlite_open("../test.db") or die(sql_error_string());
$r = sqlite_query($db, "SELECT * FROM my_friends ORDER BY last_name");
if (!$r) {
    echo "Sorry, no records.";
} else {
    while ($record = sqlite_fetch_array($r)) {
        $first_name = $record['first_name'];
        $last_name = $record['last_name'];
        $email = $record['email'];
        echo "record: $last_name, $first_name ($email)<br>";
    }
}
?>
```

将此文件保存为 `sqlite3.php` 并将其放在 浏览器的文档根目录下。访问脚本 http://127.0.0.1/sqlite3.php 来发布这些 SQLite 命令并显示输出。

现在你已经看到处理 SQLite 的过程在程序上与处理其他数据库相似，你可以浏览下一节以获取一些其他有用信息。

## 执行其他任务

在之前的章节中，你已经学习了如何创建 SQLite 数据库和表，以及向这些表中插入和选择元素。可以推断出





# SQLITE 实战示例 527

你可以类似地发布 DELETE 和 DROP 命令来删除记录和表，你也可以使用 UPDATE 来更改记录中的字段——所有这些操作都是使用 `sqlite_query()` 函数发出的 SQL 查询的变体。

至于你可以用 SQLite 执行的任务，它们与你在 MySQL 中可以执行的任务是相同的；书中所有基于 MySQL 的代码都可以重写为使用 SQLite。然而，在使用 MySQL 时代码所依赖的两个点在本附录中尚未涉及：自增字段和日期时间戳标记。

要实现自增字段的使用，你只需要对 `sqlite2.php` 脚本进行一些更改：

- 1. 在你的文本编辑器中打开 `sqlite2.php`。

- 2. 将建表表的命令更改为：

```php
sqlite_query($db, "CREATE TABLE my_friends2 (id INTEGER
PRIMARY KEY, first_name, last_name, email)");
```

- 3. 将插入记录的命令更改为：

```php
sqlite_query($db, "INSERT INTO my_friends2 (first_name,
last_name, email) VALUES ('John', 'Smith',
john@smith.com");
sqlite_query($db, "INSERT INTO my_friends2 (first_name,
last_name, email) VALUES ('Jane', 'Doe',
jane@doe.com");
sqlite_query($db, "INSERT INTO my_friends2 (first_name,
last_name, email) VALUES ('Julie', 'Meloni',
julie@thickbook.com");
```

将此文件保存为 `sqlite4.php` 并将其置于 浏览器的文档根目录下。访问 http://127.0.0.1/sqlite4.php 执行该脚本以发布这些 SQLite 命令。再次，如果此脚本执行成功，将没有任何输出。只有当脚本未能执行一个或多个命令时，你才会看到消息。

要检查这是否有效，请修改 `sqlite3.php` 脚本以检索并打印 ID 字段：

- 1. 在你的文本编辑器中打开 `sqlite3.php`。

- 2. 更改查询中的表名：

```php
$r = sqlite_query($db, "SELECT * FROM my_friends2 ORDER BY last_name ASC");
```

- 3. 更改 while 循环：

```php
while($record = sqlite_fetch_array($r)) {
    $id = $record['id'];
    $first_name = $record['first_name'];
    $last_name = $record['last_name'];
    $email = $record['email'];
    echo "record ID# $id:$last_name, $first_name ($email)<br>";
}
```

将此文件保存为 `sqlite5.php` 并将其置于 浏览器的文档根目录下。访问 http://127.0.0.1/sqlite5.php 执行脚本以发布这些 SQLite 命令并显示输出。

![](img/be897bd1bfd4dab38767db24da2a794b_550_0.png)

就像 MySQL 一样，ID 字段在插入记录时会自动递增。

接下来，让我们看看如何处理记录的日期时间标记，因为 SQLite 没有像 MySQL 那样的 `now()` 函数，也没有针对格式相关字段的特殊。解决方案是存储一个整数，即 PHP `time()` 函数的输出。当你检索该值进行显示时，可以使用 PHP 以你想要的任何格式化此存储的值。

接下来的步骤将再次适用于附录中使用的相同表和记录，只是在之前的步骤的基础上。

- 1. 在你的文本编辑器中打开 `sqlite4.php`。

# SQLITE 实战示例 529

- 2. 将建表表的命令更改为：

```php
sqlite_query($db, "CREATE TABLE my_friends3
(id INTEGER PRIMARY KEY, first_name, last_name, email,
date_added");
```

- 3. 将插入记录的命令更改为：

```php
sqlite_query($db, "INSERT INTO my_friends3
(first_name, last_name, email, date_added) VALUES
('John', 'Smith', 'john@smith.com', ''.time()')");
sqlite_query($db, "INSERT INTO my_friends3
(first_name, last_name, email, date_added) VALUES
('Jane', 'Doe', 'jane@doe.com', ''.time()')");
sqlite_query($db, "INSERT INTO my_friends3
(first_name, last_name, email, date_added) VALUES
('Julie', 'Meloni', 'julie@thickbook.com', ''.time()')");
```

将此文件保存为 `sqlite6.php` 并将其置于 浏览器的文档根目录下。访问 http://127.0.0.1/sqlite6.php 执行脚本以发布这些 SQLite 命令。再次，如果此脚本执行成功，将没有任何输出。只有当脚本未能执行一个或多个命令时，你才会看到消息。

如果此脚本有效，修改 `sqlite5.php` 脚本以检索并打印 `date_added` 字段中的值：

- 1. 在你的文本编辑器中打开 `sqlite5.php`。

- 2. 更改查询中的表名，并按 ID 排序记录：
```php
$r = sqlite_query($db, "SELECT * FROM my_friends ORDER BY id");
```

- 3. 在 while 循环中添加以下内容，在定义 $email 的行之后：

```php
# 附录 E：使用 SQLITE
# 注意：在此示例中，date() 函数格式化
# added 字段。你可以看到类似
# 4. while 循环中的 echo 语句：
echo "record ID# $id:$last_name, $first_name ($email)<br>";
```

# SQLITE 实战示例 552

开源社区最棒的方面之一是人们乐意帮助你，然而在向社区提问之前，你应该尝试寻找答案。这包括阅读可用手册、FAQ 以及访问网站。

这本书以及我其他书籍的网站是 http://www.thickbook.com/。你可以在那里找到勘误、书籍下载代码以及我在空闲时间想到的任何其他内容。书籍勘误将帮助你判断问题是否由于打印错误引起，PHP相关的新闻组和邮件列表非常丰富，这里列出的只是冰一角。

# PHP 资源

大多数网站是由人利用业时间维护的，因此如果你使用了他们的任何资源，请尝试回馈社区，例如帮助他人解决问题、向代码库提交代码段等。

# 网站

PHP 的主页是 http://www.php.net。这里有注释在线手册，以及 PHP FAQ、错误报告、提供 PHP 服务的 ISP 链接、新闻文章等更多内容！

# zend.com

Zend Technologies（PHP Zend 引擎的开发者）为 PHP 开发者创建了一个门户。这个个性化的网站不仅展示了你如何使用 PHP 构建高流量的动态网站，还提供了提示、资源和课程，教你如何在你的所有在线应用程序中最大化地利用 PHP 的潜力。

# DevShed (www.devshed.com)

该网站包含许多用户提交的教程、新闻文章、采访以及对服务器端编程语言的竞争性分析。涵盖了 PHP 以及开发者感兴趣的许多主题，如服务器和数据库。

# PHPBuilder (www.phpbuilder.com)

对于中高级 PHP 开发者来说，这是一个非常好的教程网站。它包含了实际应用的 How Tos，例如“考虑到搜索引擎构建动态页面”、“生成可读密码”以及等大量内容。推荐！





# WeberDev (www.weberdev.com)

这个网站一直是 PHP 开发者青睐的，包含了任何编程语言的开发技巧和提示（为了公平起见），以及一个内容管理系统，供所有人添加自己的代码片段、教程等！它有一个非常棒的周刊，而且流量很高。去贡献一份吧！

# px.sklar.com

这是一个极简的代码仓库，当你需要的只是代码片段时，还需要图形呢？借鉴“拿走一分，留下一分”的心态，你可以先取一个代码片段开始，当你有信心分享时再添加你自己的。

# Webmonkey (hotwired.lycos.com/webmonkey)

带给我们《Wired$ 杂志的公司也带来了 HotWired，它催生了 Webmonkey，这是一个开发者资源网站，有一个专门针对 PHP 的板块。不要把自己限制在 Webmonkey 的 PHP 部分，因为在其他部分也有很多信息。

# PHP 知识库 (php.faqts.com)

PHP 知识库包含了 PHP 邮件列表提出的问题和解答。任何人都可以在网站上回答问题或提新问题。

# 邮件列表 (Mailing Lists)

有几个高流量的邮件列表用于英语及其他语言的 PHP 讨论。在提问时请记住网络礼仪：保持礼貌，尽可能提供示例（如果你在描述一个问题），提供你的系统信息（如果你在寻找解决方案），并且有没有说过“请”和“谢谢”？

你可以在 http://www.php.net/mailing-lists.php 找到邮件列表订阅信息。英语 PHP 邮件列表已存档并可以在 http://marc.theimsgroup.com/ 进行搜索。在 WWW 下查找 PHP 相关的列表。

# 用户组 (User Groups)

有时，在现实生活中认识其他开发者证明很有帮助。你可以在 http://www.phpusergroups.org 找到 PHP 用户组列表。

# MySQL 资源

之前列出的许多 PHP 相关网站也包含了使用 MySQL 开发的信息，但 http://www.mysql.com/ 的 MySQL 网站是获取全面 MySQL 信息的起点。

在线 MySQL 手册非常庞大，但它写得非常好且实用，它的规模不应该吓到你。你可以在 http://www.mysql.com/doc/ 找到手册。如果你正在寻找对 MySQL 的快速介绍，我写了一本书《24 小时自学 MySQL》，在全球各大书店有售。其他关于 MySQL 的推荐书籍包括 Paul DuBois 写的任何著作（事实上，他负责了 MySQL 手册的大部分内容！）

对于 PHP，有几个高流量的邮件列表用于英语及其他语言的 MySQL 讨论。你可以在 http://www.mysql.com/documentation/lists.html 找到邮件列表订阅信息，MySQL 邮件列表也可以在 http://marc.theaimroup.com/ 进行搜索。

# Apache 资源

从 Apache 基金会网站 http://www.apache.org/ 开始，获取服务器文档和常见问题解答（FAQs）列表。上述许多面向开发者的网站（如 DevShed）都提供特定的 Apache 教程——你只需要去搜寻它们即可。

ApacheWeek 网站 (http://www.apacheweek.com/) 充满了 Apache 相关的技巧、文章、评论等。内容每周发布（因此得名），并提供过往期数的存档。

# 索引 (Index)

# 符号 (Symbols)

- + (加法)运算符, 74
- & (与)运算符, 81
- { (大括号), 464
- / (除法)运算符, 74
- $ (美元符号), 459
- " (双引号), 65
- == (等于)运算符, 77
- / (正斜杠), 142
- % (取模)运算符, 74
- * (乘法)运算符, 74
- \n (换行符), 122, 153
- != (不等于)运算符, 77
- || (或)运算符, 81
- ; (分号), 10, 55
- ' (单引号), 65
- - (减法)运算符, 74
- \t (制表符), 126–127
- _ (下划线)

- addslashes() 函数, 486
- 管理员菜单
- 联系人管理系统, 298–303
- 表格, 232–234

- ALTER 命令, 514-515
- 修改表, 514–515
- 与 (&) 运算符, 81

- Apache
- 配置
- 在 Linux/Unix 上, 32–34
- 使用 PHP, 44–45
- 在 Windows 上, 27–28
- 安装
- 在 Linux/Unix 上, 30–31
- 在 Windows 上, 24–27
- 日文件, 416–417
- 资源, 534
- 启动并连接, 29, 30–35
- 网站, 24

- ApacheWeek 网站, 534
- 算术运算符, 71, 77–462
- 数组, 461

```php
array(), 467
array_keys(), 468
array_merge(), 468
array_pop(), 467
array_push(), 467
array_shift(), 468
array_unshift(), 468
array_values(), 468
```

# A

- a 模式, fopen() 函数, 146
- 访问报告, 418–422
- 地址, 联系人管理系统, 313
- 加法 (+) 运算符, 74
- 赋值运算符, 71–74, 462
- 认证, 269–275
- 属性
- 艺术家
- artist_field, 202
- artist_field, 202
- 算术运算符, 71, 77–462
- 数组, 461
- Apache
- 配置
- 在 Linux/Unix 上, 32–34
- 使用 PHP, 44–45
- 在 Windows 上, 27–28
- 安装
- 在 Linux/Unix 上, 30–31
- 在 Windows 上, 24–27
- 日志, 416–417
- 资源, 534
- 启动并连接, 29, 30–35
- 网站, 24
- ApacheWeek 网站, 534
- array(), 467
- array_keys(), 468
- array_merge(), 468
- array_pop(), 467
- array_push(), 467
- array_shift(), 468
- array_unshift(), 468
- array_values(), 468
- a 模式, fopen() 函数, 146
- a 模式, fopen() 函数, 146
- 访问报告, 418–422
- 加法 (+) 运算符, 74
- 赋值运算符, 71–74, 462
- 认证, 269–275
- 属性
- 艺术家
- artist_field, 202
- artist_field, 202
- 算术运算符, 71, 77–462
- 数组, 461
- Apache
- 配置
- 在 Linux/Unix 上, 32–34
- 使用 PHP, 44–45
- 在 Windows 上, 27–28
- 安装
- 在 Linux/Unix 上, 30–31
- 在 Windows 上, 24–27
- 日志, 416–417
- 资源, 534
- 启动并连接, 29, 30–35
- 网站, 24
- ApacheWeek 网站, 534
- array(), 467
- array_keys(), 468
- array_merge(), 468
- array_pop(), 467
- array_push(), 467
- array_shift(), 468
- array_unshift(), 468
- array_values(), 468
- echo, 55
- 转义字符, 58–60
- 表达式, 78
- 编辑
- 概述, 341–343
- 等于 (==) 运算符, 77
- 等于 (==) 运算符, 77
- 等于 (==) 运算符, 77
- 命令
- ALTER, 514–515
- CREATE, 513–514
- DELETE, 516

# B

- 反斜杠 (\), 58,60–142
- 目录, 34
- BIGINT 类型, 201
- BLOB 类型, 201
- bind(), 479
- 生日, 联系人信息, 372–378
- 生日, 显示, 372–378

# C

- 计算表, 86–88
- 计算脚本, 89–91
- 区分大小写, XML, 440
- ceil() 函数, 479
- 单元, 表格, 221–222
- CHAR 类型, 201
- date() 函数, 370–371
- date() 函数, 370–372
- chgrp() 函数, 474
- chmod() 函数, 474
- chop() 函数, 487
- chown() 函数, 474
- 客户端代码, 50
- 客户端代码, 50
- 注释, 60–62
- 比较运算符, 71, 77–80, 463
- 拼接, 字符串, 122
- 条件表达式, 78
- 联系人
- 添加
- 记录表, 创建, 316–321
- 记录删除脚本, 创建, 321–325
- 记录选择表, 创建, 346–360
- 代码片段, 访问报告, 418–422
- 命令
- ALTER, 514–515
- CREATE, 513–514
- DELETE, 516
- 记录修改表, 创建, 333–337
- 记录修改脚本, 创建, 337–341
- 记录选择表, 创建, 328–333
- 管理系统

# D

- 数据
- 追加到文件, 152–153
- 从文件读取, 154–157
- DevShe 网站, 532
- die() 函数, 147, 149–150, 153, 157, 213, 482
- 目录
- 数据类型
- BIGINT, 201
- BLOB, 201
- CHAR, 201
- DATE, 201
- DATETIME, 201
- ENUM, 201
- FLOAT, 201
- INT, 201
- MEDIUMINT, 201
- SMALLINT, 202
- TEXT, 201
- TIMESTAMP, 201
- TINYINT, 200
- VARCHAR, 201
- bin, 34
- 内容, 显示, 142–145
- 连字符, 299
- 除法 / 运算符, 74
- 美元符号 ($), 459
- 序列化, 244
- 序列化认证, 269–275
- 域名参数, setcookie() 函数, 265
- 定义, 69
- 设置, 264–266
- 测试 cookie, 267–268
- 变量, 460
- copy() 函数, 160–164
- 拷贝文件, 160–162
- 计数, 显示访问记录, 422–425
- count() 函数, 213, 469
- 计时, 266
- CREATE 命令, 513–514
- CSS (层叠样式表), 438
- 大括号 (}, 464
- define() 函数, 69
- DELETE 命令, 516
- 删除, 196–197
- 数据库, 164–166

# E

- 电子邮件
- 联系人管理系统, 313
- 发送
- 反馈表, 创建, 120–121





## 538 索引

- 反馈表单，带有自定义错误消息, 127–137
- 文件内容, 157–158
- 脚本, 121–124
- 文件系统函数, 474–477
- 文件
  - 向其追加数据, 152–153
  - 内容，通过电子邮件发送内容, 157–158
  - 复制, 160–162
  - 创建新文件, 146–149
  - 删除, 164–166
  - 检查存在性, 150–152
  - 文件指针, 147
  - 文件上传
    - 讨论, 168
    - 表单创建, 170–171
    - 过程, 169
    - 上传脚本, 172–173
  - 从文件中读取数据, 154–157
  - 重命名, 162–164
- each(), 469
- echo 命令, 55
- echo(), 487
- else 语句, 150, 165
- PHP 结束标签, 50–52, 458
- ENUM 数据类型, 202
- 环境变量, 460–461
  - 讨论, 92
  - HTTP_USER_AGENT, 95–96
  - REMOTE_ADDR, 93–94
- 等于 (==) 运算符, 77
- ereg_replace(), 函数, 485
- preg_replace(), 函数, 485
- 错误
  - mysql_error(), 函数, 181
- 发送邮件
  - filesize(), 函数, 153
  - 正常, 507–508
- FLOAT 数据类型, 201
- 浮点数, 65–459
- floor(), 480
- font_family 变量, 284–285
- font_size 变量, 284, 286
- open(), 函数, 145–147, 150, 153, 157, 475
- for 语句, 466
- format 字段, 202
- 表单
  - 增加错误检查, 130–135
  - 表单提交, 135
  - 初始脚本创建, 128–129
  - 值，保存, 138–139
- 转义字符, 58–60
- exec(), 函数, 483
- sit 抽象, 482
- setcookie(), 函数中的过期参数, 265
- explode(), 函数, 487
- 条件表达式, 78
  - 计算, 86–88
  - 反馈，电子邮件, 120–121
  - 文件上传, 171–177
  - 输入表单，脚本, 107–108
  - 登录，身份验证, 257–258
- 通通讯，邮件列表
  - 创建, 407–408
  - 时间, 411–413
- 记录添加
- 可扩展标记语言 (XML)。请参见 XML

## F

- F 选项，日期格式化, 371
- close(), 函数, 145, 476
- 反馈
  - 带有自定义错误消息, 127–137
  - 电子邮件, 120–121
- 字段
  - ID 编号，唯一的, 203
  - SET, 339
  - 表字段
    - 定义, 202–203, 205–210
    - 输入字段, 204
    - UPDATE, 339
  - 文件路径和权限, 142
  - 文件指针, 147
  - 联系人管理系统, 316–321
  - 建表, 220–223
  - 记录删除，删除表单, 351–355
  - 联系人管理系统中的记录修改, 333–337
  - 记录选择
    - 联系人管理, 328–333
    - 删除联系人, 346–350
    - 方向, 113–115
    - 提交, 91
    - 邮件列表的订阅表单, 397–404
    - 用户添加，身份验证, 250–254
    - 值，显示，字符串函数, 109–110
- 正斜杠 (/), 142
- fputs() 函数, 476
- read() 函数, 155–156, 158, 476
- 函数
  - addlashes(), 486
  - array(), 467
  - array_keys(), 468
  - array_merge(), 468
  - array_pop(), 467
  - array_push(), 467
  - array_shift(), 468
  - array_unshift(), 468
  - array_values(), 468
  - bind(), 479
  - ceil(), 479
  - checkdate(), 472
  - chgrp(), 474
  - chmod(), 474
  - chop(), 467
  - chown(), 474
  - concat(), 242, 517
  - copy(), 160–161, 474
  - count(), 213, 469
  - 连接性, 470–471
  - date(), 370–371, 472, 530
  - DAYNAME(), 519
  - DAYOFMONTH(), 518
  - DAYOFWEEK(), 518
  - DAYOFEAR(), 518
  - db_connect(), 497
  - decbin(), 479
  - dechex(), 480
  - decopt(), 480
  - define(), 469
  - die(), 147–149, 153, 157, 213, 482
  - each(), 469
  - echo(), 487
  - ereg_replaces(), 485
  - ereg_replace(), 485
  - exec(), 483
  - explode(), 487
  - close(), 187–145, 476
  - system, 474–477
  - filesize(), 155
  - floor(), 480
  - fopen(), 147–150, 153, 157, 475
  - fputs(), 476
  - fread(), 155–156, 158, 476
  - fwrite(), 153
  - getenv(), 93–95, 103, 461
  - header(), 113–114, 477–478
  - dechex(), 480
  - htmlentities(), 488
  - htmlspecialchars(), 488
  - HTTP, 477–468
  - implode(), 487–488
  - include(), 497–498
  - isset(), 491
  - list(), 469
  - LOWER(), 517
  - trim(), 487
  - mail(), 118, 123, 158, 410, 438
  - mathematical, 479–481
  - microtime(), 472, 474
  - rdir(), 476
  - mktime(), 472
  - MONTH(), 518
  - MONTHNAME(), 518
  - multiplier(), 494, 497
  - mysql_connect(), 181, 470
  - mysql_error(), 181, 361, 478
  - mysql_fetch_array(), 233–234, 471
  - mysql_list_db(), 185, 519
  - mysql_list_tables(), 188–190
  - mysql_num_rows(), 185, 329, 471
  - mysql_query(), 193, 214, 242, 471
  - mysql_result(), 366
  - mysql_select_db(), 213, 471
  - mysql_tablename(), 185
  - numberbr(), 159, 488
  - now(), 528
  - number_format(), 480
  - octdez(), 480
  - open(), 143
  - passtrfu(), 484
  - PASSWORD(), 252
  - phpinfo(), 68, 92
  - pow(), 481
  - preg_match(), 100
  - program execution, 483–484
  - rand(), 481
  - readdr(), 143
  - regular expression, 485
  - rename(), 162–164, 476
  - require(), 497–498
  - reset(), 470
  - returning values from, 194–496
  - rdir(), 477

## 539 索引

- round(), 481
- session-handling, 486
- session_destroy(), 486
- session_start(), 279–280, 486
- setcookie(), 265–267, 488
- shuffle(), 470
- sizeof(), 470
- sleep(), 482
- split(), 485
- sprintf(), 489
- sql_error_string(), 522
- sqlite_open(), 522
- sqlite_query(), 527
- sqrt(), 481
- rand(), 481
- string, 486–491
- strilashes(), 227, 242, 410, 486
- strlen(), 112, 489
- strview(), 112, 496
- strtobrow(), 112, 490
- strtoupper(), 112, 490
- substr(), 214, 490
- symlink(), 476
- sysystem(), 484
- time, 472
- time(), 266, 474
- trim(), 235, 242, 477
- ucfirst(), 491
- ucwords(), 112
- unset(), 483
- unlink(), 164, 165, 477
- UPPER(), 491
- var_dump(), 443
- variable, 491
- WEEK(), 519
- WEEKDAY(), 518
- YEAR(), 519
- printf(), 472

## H

- header(), 113–114, 477–478
- dechex(), 480
- hidden, 55
- hex(), 480
- HTML, 100–103
- htmlentities(), 488
- htmlspecialchars(), 488
- HTTP, 477–468
  - discussed, 92
  - HTTP_USER_AGENT, 95–96
  - REMOTE_ADDR, 93–94

## I

- ID, 233–234
- ID field, 202
- ID numbers, unique, 203
- if, 78, 89
- if...else, 79
- include(), 497–498
- increment, 55
- instance, 502
- INSERT, 339
- instruction, 55
- INT data type, 201
- isset(), 491

## G

- GET method, 55
- global variables, 67
- GRANT, 180
- greater than or equal to, 77

## J

- j option, 371

## L

- LOWER(), 517
- list(), 469
- l, 4
- less, 77
- less than, 77
- less than or equal to, 77
- Linux, 30–31

## M

- mathematical, 479–481
- microtime(), 472, 474
- mkdir(), 476
- mktime(), 472
- modulus (%) operator, 74
- MONTH(), 518
- MONTHNAME(), 518
- multiplier(), 494, 497
- my_feeds, 202
- MySQL
  - connecting to, 181–182
  - distributions, 4
  - starting, 9
  - mysql_connect(), 181, 470
  - mysql_error(), 181, 361, 478
  - mysql_fetch_array(), 233–234, 471
  - mysql_list_tables(), 188–190
  - mysql_num_rows(), 185, 329, 471
  - mysql_query(), 193, 214, 242, 471
  - mysql_result(), 366
  - mysql_select_db(), 213, 471
  - mysql_tablename(), 185
- my_contacts, 305–306, 312
- MIME type, 172





## 542 索引

- 不等于 (=) 运算符, 77
- now() 函数, 528
- number_format() 函数, 480
- 偏好，sessions, 284–288
- preg_match() 函数, 100
- 权限
    - GRANT 命令, 180–181
    - 用户, 创建新的, 180–181
- 程序执行函数, 483–484
    - 属性的，对象, 500–501

## O

- 对象
    - 构造函数, 502
    - 创建, 499–500
    - 继承, 502–504
    - 方法, 501–502
    - 属性, 500–501
- octdec() 函数, 480
- opendir() 函数, 143
- 运算符
    - + 算术, 71, 77–72
    - 赋值, 71–74, 462
    - 比较, 71–80, 863
    - 增/减, 463
    - 逻辑, 71–83, 464
    - 类型, 71
- 或 或或 (||) 运算符, 142

## P

- 页面分页，访问报告, 431–435
- pasthru() 函数, 484
- PASSWORD() 函数, 252
- 路径参数, setcookie() 函数, 265
- 文件权限，路径的, 142
- 个人访问报告, 425–427
- PHP

## R

- r 模式, fopen() 函数, 146
- r+ 模式, fopen() 函数, 146
- rand() 函数, 481
- 只读记录, 384–390
- readir() 函数, 143
- 从文件读取数据, 154–157
- 记录标签字段, 202
- 记录添加表
    - 联系管理系统, 316–321
    - 表创建, 220–223
- 记录添加脚本
    - 联系管理系统, 321–325
- 记录删除表，删除联系人, 351–355
- 记录删除脚本，删除联系人, 355–358
- 记录列表，联系信息, 379–383
- 记录修改表，联系管理系统, 333–337
- 记录修改脚本，联系管理系统, 337–341
- 记录选择表
    - 联系管理系统, 328–333
    - 删除联系人, 346–360
- 显示
    - 按艺术家, 240–244
    - 按获取日期, 238
    - 按 ID, 233–234
- 重定向表, 113–115
- 注册 sessions, 282–283
- 正则表达式函数, 485
- REMOTE_ADDR 变量, 93–94
- rename() 函数, 162–164
- 重命名文件, 162–164
- REPLACE 命令, 515
- 替换表, 515–516
- 报告，访问
    - 代码段, 418–422
    - 计数，显示, 422–425
    - Apache 配置, 44–65
    - 代码栖留, 53–55
    - 安装
        - 用于 Linux/Unix, 43–44
        - 在 Windows 上, 38–41
- 资源, 532–534
- 开始和结束日期, 50–52, 458
- 结构, 50
- 网站, 532
- 使用 XML, 441–444
- PHPBuilder 网站, 532
- phpinfo() 函数, 68–92
- 特定于平台的 HTML, 103–106
- 填充表, 229–230
- POST 方法, 86, 107, 113, 460
- pow() 函数, 481
- 预变量, 68

## 索引 543

- 数据库表创建, 417–418
- 页面分页，显示, 431–435
- 个人, 425–427
- 用户代理，显示, 428–431
- require() 函数, 497–498
- reset() 函数, 470
- 资源
    - Apache, 534
    - MySQL, 534
    - PHP, 532–534
    - return 语句, 495–496
    - 从函数返回值, 494–496
- rmdir() 函数, 477
- round() 函数, 461
- Run 命令 (开始菜单), 8–9

## S

- 选项，日期格式, 371
- 脚本
    - 认证, 258–261
    - 计算, 89–91
    - 联系管理系统, 306–312
    - 电子邮件，发送, 121–124
    - 文件上传, 172–173
    - 邮件列表, 408–411
- 记录添加
    - 联系管理系统, 321–325
    - 表, 223–229
    - 记录删除，命令, 355–358
    - 记录修改，联系管理系统, 337–341
    - 表创建, 212–216
    - 第二普通表, 508–509
    - 安全参数, setcookie() 函数, 526
    - SELECT 命令, 12, 20, 516–517
    - 分号 (;), 10, 95
    - 电子邮件
        - 反馈表，创建, 120–121
        - 自定义消息, 127–131
        - SMTP (简单邮件传输协议), 118–119
- 服务器端代码, 50
- 服务器，列出数据库, 185–187
- session 处理函数, 486
- sessions
    - 定义, 278
    - 编辑, 282–283
    - 注册, 282–283
    - 开始的, 279–281
    - 用户偏好, 284–288
    - 变量, 279
    - session_start() 函数, 279–280, 486
    - 设置字段, 539
    - setcookie() 函数, 265–278
    - SHOW 命令, 519–520
    - shuttle() 函数, 470
- 简单邮件传输协议 (SMTP), 118–119
- 单引号 (''), 65
- sizeof() 函数, 470
- sleep() 函数, 482
- SMALLINT 类型, 200
- sprintf() 函数, 485
- sprintf() 函数, 489
- SQL (结构查询语言)
    - ALTER 命令, 514–515
    - CREATE 命令, 513–514
    - 日期和时间, 518–519
    - DELETE 命令, 516
    - DROP 命令, 513–516
    - INSERT 命令, 515
    - REPLACE 命令, 515
    - SELECT 命令, 516–517
    - 字符串函数, 517
    - UPDATE 命令, 516
- sql_error_string() 函数, 522
- SQLite
    - 创建表并存储数据, 523–524
    - 示例, 522–533
    - 使用...检索, 524–526
    - sqlite_open() 函数, 522
    - sqlite_query() 函数, 527
- sqrt() 函数, 481
- strand() 函数, 481
- 开始和结束标签, PHP, 502–458
- 开始菜单命令, Run, 8–9
- 开始
    - Apache, 29,30–34
    - MySQL, 8–9
    - sessions, 279–281
- 语句
    - for, 466
    - else, 150, 165
    - exit, 482
    - if, 89
    - if...else, 79–81, 464–465
    - return, 495–496
    - while, 86
- 插入在, 515–516
- 在数据库中列出, 188–192
- 填充, 229–230
- 记录添加表, 220–223
- 记录添加脚本, 223–229
- 记录，显示
    - 字符串拼接, 122
    - 函数, 112, 490
    - 磁盘, 106
    - 表单值，显示, 109–110
    - 输入表, 107–108
    - 值, 459–460
- 字符串
    - 按艺术家, 240–244
    - 按获取数据, 238
    - 按 ID, 233–234
    - 按标题, 239–240
    - 替换, 515–516
    - 从...选择, 516–517
    - 更新, 515–516
    - 用户认证, 248–249
- 变量, 65
- striplashes(), 227, 224, 410, 486
- strlen() 函数, 112, 490
- strv(), 函数, 112
- strlower() 函数, 112, 490
- toupper() 函数, 112, 490
- 结构查询语言
    - 表，邮件列表, 319–394
    - 订阅，邮件列表, 404–406
- 标签，开始和结束, PHP, 50–52
- 测试 cookies, 267–268
- 测试, 404–406
- substr() 函数, 214, 490
- 减法运算符, 74
- 超全局变量，预变量, 68
- symlink() 函数, 477
- system 函数, 484

## T

- 制符 (;), 10, 95
- 字符串, 443
- time() 函数, 472
- 时间函数, 472–474
- TIMESTAMP 类型, 201
- TINY 类型, 200
- 标题
    - 记录管理系统, 337–341
    - 字段, 539
    - 定义的, 278
    - 变量, 279
    - session_start() 函数, 279–280, 486
    - 设置字段, 539
    - setcookie() 函数, 265–278
    - SHOW 命令, 519–520
    - shuttle() 函数, 470
## U

- ucfirst() 函数, 472
- ucwords() 函数, 112, 490
- 字符串, 64, 459
- uniqid() 函数, 483

## W

- Unix
    - Apache 配置, 29,30–34
    - Apache 安装, 43–44
    - MySQL, 8–9
    - sessions, 279–281
- while 语句, 81, 464–465

- w 模式, fopen() 函数, 146
- w+ 模式, fopen() 函数, 146
- 网站
    - Apache, 24
    - ApacheWeek, 534
    - DevSelf, 532
    - PHP, 532
    - PHPBuilder, 532
    - WeberDev, 533
    - Webmonsky, 533
    - Zend Technologies, 532
    - WeberDev 网站, 533
    - Webmonsky, 533





## 快速易懂的 Web 开发

## 更少的时间、精力，更多的开发。

不要浪费时间去翻阅冗长的手册来寻找你所需的信息。要把时间花在你最擅长的事情上——Web 开发。Course Technology PTR *快速易懂* Web 开发系列通过步步渐进的指令和真实的截图，帮助你快速轻松地掌握概念并精通技能。

 * Microsoft® ASP.NET Fast & Easy® Web Development
- 1-9318141-46-2 伴随网站
- Adobe LiveMotion™ Fast & Easy® Web Development
- 0-7615-3254-4 包含 CD
- ASP 3 Fast & Easy® Web Development
- 0-7615-2854-7 包含 CD
- CGI Fast & Easy® Web Development
- 0-7615-2938-1 包含 CD
- Java 2 Fast & Easy® Web Development
- 0-7615-3056-8 包含 CD
- JavaScript Pages™ Fast & Easy® Web Development
- 0-7615-3428-6 包含 CD

- * Macromedia Director® 8 and Lingo™ Fast & Easy® Web Development
- 0-7615-3049-5 包含 CD
- Macromedia® Dreamweaver® MX 2004 Fast & Easy® Web Development
- 1-59200-121-1 伴随网站
- Macromedia® Dreamweaver UltraDev™ 4 Fast & Easy® Web Development
- 0-7615-3517-9 包含 CD
- Macromedia® Fireworks MX 2004 Fast & Easy® Web Development
- 1-59200-120-4 伴随网站
- Macromedia® Flash™ MX 2004 Fast & Easy® Web Development
- 1-59200-119-X 伴随网站

- * Microsoft® C# Fast & Easy® Web Development
- 1-9318141-05-5 伴随网站
- Perl Fast & Easy® Web Development
- 1-9318141-17-9 伴随网站
- PHP Fast & Easy® Web Development, 2nd Edition
- 1-9318141-87-X 伴随网站

立即电话订购！1.800.354.9706

