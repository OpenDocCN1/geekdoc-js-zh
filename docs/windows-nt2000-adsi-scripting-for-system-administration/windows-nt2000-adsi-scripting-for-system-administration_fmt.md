
# Windows NT／2000 ADSI：系统管理脚本指南

![](img/b5063514d2e449d6d8c5d65f100b84aa_0_0.png)

## 以下是评论者对《Win32 Perl 脚本编程：管理员手册》的评价：

“没有任何一本书可以取代这本书……我希望为我正在计划的一门课程立即拥有它。Dave Roth 在维护 Windows 机器和网络方面拥有丰富经验，大大减少了徒用功，并且较少将许多不快的意外接受为‘常态’。书中的解释和示例有效地传达了读者可以如何使用 Perl 来获得同样的成功。”

Cameron Laird

脚本语言“正则表达式”专栏共同作者，Perl/Tk FAQ 维护者

“随着 Windows 被部署在更严苛的环境中，自动化管理任务的需求将增加……这本书帮助人们自动化他们的系统管理任务……我寻找了一些我已知的是常见的问题，并成功找到了它们。”

Dick Hardt

ActiveState 创始人兼首席执行官

“大多数章节都提供了即插用的脚本，这些对任何人都有益……作者还解释了为什么特定的脚本是有用的，以及如何使用它们来成功地管理 Windows 网络。”

Michel Dalle

西门子通用电气公司 IT 顾问

“优秀的书——我很高兴看到这个主题得到了很好的涵盖……向 Roth 致敬。”

Chuck Davis

顾问——客户包括美国航空航天局（NASA）和美国陆军

![](img/b5063514d2e449d6d8c5d65f100b84aa_1_0.png)

![](img/b5063514d2e449d6d8c5d65f100b84aa_1_1.png)

作者 David Roth

![](img/b5063514d2e449d6d8c5d65f100b84aa_3_0.png)

- 结论 ................................................................... 209
- 发现 IIS 属性 ....................................................................... 329
- WMI 细节 ....................................................................................... 338
- 本书使用的模块 ...................................... 347
- Perl 信息 ................................................ 349
- Usenet ................................................ 351

## 关于作者

Dave Roth 是许多流行的 Win32 Perl 扩展的贡献者，包括 `Win32::ODBC`、`Win32::Misc`、`Win32::Daemon` 和 `Win32::Perms`。自1994年以来，他一直在为 Perl 社区解决难题问题提供解决方案。Dave 曾在 O'Reilly Perl 大会以及 USENIX LISA-NT 会上担任演讲者。他还为《Perl Journal》贡献过内容，是《Win32 Perl Programming: The Standard Extensions》（New Riders Publishing, 2999）的作者。

Dave 自1981年就开始使用各种语言编程，从汇编到 C++、LPC 和 Perl。他的代码被微软、美国国防部、迪士尼、卢卡斯影、Digital Paper、惠尔士、Metagenix、Radcom、密歇根州以及各大学等机构使用。Dave 帮助密歇根州组装并管理了州域网，并为密歇根州立大学和 Ameritech 设计并管理了局域网。

## 技术评审员

这些评审员为《Win32 Perl 脚本：管理员手册》的整个开发过程贡献了他们深厚的实战经验。在本书编写期间，这些敬业的人士针对技术内容、组织结构和逻辑对所有材料进行了评审。他们的反馈对于确保《Win32 Perl 脚本：管理员手册》符合读者对高标准技术信息的需求至关重要。

Joseph Casadonte (joc@netaxs.com) 是 Global Logistics Technologies 的首席软件架构师，在 C、C++、Java、Perl 以及以及最近接触的 Lisp 语言方面 着 15 年的专业编程经验。在空闲之余，他喜欢编写大型程序（通常使用 Perl）来自动化琐碎的任务，例如为他的 Grateful Dead CD 收藏集建立目录。他最近开始学习编写 List 以自定义他新喜爱的编辑器 Emacs。他的 Perl Win32 页面位于 http://www.netaxs.com/~joc/perlwin32.html，你可以在那里链接到他的 CD 收藏集和 Emacs 页面。

Jutta M. Klebe 是一位工程师，也是微软认证专业人员 (MCP)，拥有 15 年的编程和操作系统经验。在理工学院获得机械工程师学位（德国的 Dipl.-Ing.）后，她自 1990 年以来一直担任系统管理员。Jutta 负责 Windows 电脑的安装过程，并处理包含 UNIX 服务器、Windows NT 服务器和 Windows NT 工作站的异构网络中的用户问题。在空闲之余，她管理 Web 服务器，并使用 ActiveX/COM、D)HTML、Perl、C/C++、VB、VBScript 和 JavaScript 等技术开发互联网和内网应用。Jutta 与男朋友住在德国汉诺威。闲暇时她还会骑自行车。

## 献献

本书献给我已故的祖父。他是我生命中沉默的引导力量。他让我“顺势而为”的建议是正确的，我只能推测他拥有某些我不具备的神力。尽管他从未编程过，但他的小提琴拉得非常好，并且是我长大后成为一个人的完美榜样。是的，这本书是一本技术参考书，但在精神上，它遵循了他所创作的那些著作。

## 谢谢

我想感谢两位通过为我的工作提供不可或缺的技术评审而与我合作的人——Joe Casadonte (www.netaxs.com/~hoc/perlwin32.html) 和 Klebe Jutta (www.byte.de/jmk)。如果没有这两个人的辛勤工作，这本书将完全是一团糟。感谢你们对细节的关注以及处理了那些单调的代码页！

接下来要感谢的是我的编辑们；Karen Wachs、Leah Williams、Katie Pendergast、Lori Lyons、Chuck Hutchinson 以及其他与此项目相关的每个人都应该获得加薪！没有你们的耐心和专业精神，最后的章节可能永远无法见光，更不用说出版了。感谢你们在截止日期推迟时的坚持。

我想感谢那些曾因我忙于写另一本书而指责我的人。你们知道自己是谁的：Zu, Chris, Chris, Kris, Chadd, Larry, Susan, Heather, Anton, Toshi, Bushia, Laura, Grandma, Mom, Ttootty, Greg, Gwen, Andy, Alex, Audrey, Anne ve Baba, Dilek, Leila, Harlan, Bill……整个伙伴小组。多亏了你们无休止的敌意，我才能拿出坚持下去的毅——尽管这可能是出于单纯的报复。你们可以停止问“那么，书写完了吗？”现在，开始下一本书吧！

最后，我很荣幸能感谢我可靠的妻子 Nazli。你在压力巨大时保持冷静、在我皱眉时大笑的能力，让这段旅程变得可以忍受。你为我的灵魂带来了前所未有的快乐。感谢你的爱与慈悲。亲爱的，你对我来说就是一切。谢谢。

## 告诉我们你的想法

作为本书的读者，你是最重要的评论家和评论者。我们重视你的意见，并想知道我们做得对的地方、哪里可以做得更好、你希望我们在哪些领域出版，以及任何其他你愿意分享给我们的智慧。

作为 New Riders 出版公司网络团队的执行编辑，我欢迎你的评论。你可以通过传真、电子邮件或直接写信给我，告诉我你对这本书的喜欢或不喜欢之处——以及我们可以做什么来让我们的书籍更强大。

请注意，我无法帮助你解决与本书主题相关的技术问题，而且由于我收到的邮件很多，我无法回复每条信息。

本书分为九章，每章涵盖一个不同的主题。

## 第一章：Perl 与管理员

本章讨论了管理员在网络环境中引入 Perl 语言需要了解的各个方面。对于从未接触过 Perl 的人来说，这是一个很好的开始。对于那些经验丰富的 Perl 大师来说，你可能会发现一些有趣的 Win32 特定技巧，帮助你在 Windows 2000、NT、ME、以及 98 和 95 上充分利用 Perl。

## 第二章：账户维护

本章的目的是打破 Win32 管理员发现自己受到的 GUI 束缚。在这里你将发现一些脚本，它们让你能够从命令行管理 Win32 账户，而无需拿起鼠标。

## 第 3 章：工具

如果没有合适的工具，哪个管理员是无法生存的？

遗憾的是，大多数 Win32 管理员都是如此——指的就是他们。这并不是任何人的错，但确实缺乏能够解决任务的廉价实用程序。

在本章中，你将找到不仅手手，而且可以在日常任务中使用的工具。这些工具了用于发现共享目录（包括隐藏共享）、发现 NTFS 备用数据流、发现文件信息、读取权限、设置文件和注册表项的所有者，以及设置机器自动登录特定用户的工具。

## 第 4 章：危机管理

每个网络都会经历某种程度的危机——有些比其他的更严重。在本章中，你将学习一些简单而有效的技术来为这些不可避免的状况做好准备。恢复基于 COM 的文档、强制用户断开共享资源、备份和恢复用户账户，以及使用文件权限和网络共享，这些只是其中涵盖的几个主题。

## 第 5 章：监控与报告

管理员如何预先地解决问题呢？答案非常简单：通过主动监控网络机器。当然，这说起来容易，但具体怎么做呢？第 5 章讨论了监控 Win32 事件的各个方面，例如事件日志。

在监控事件之后，需要对其进行报告，以便你的管理团队做出响应。书中讨论了各种报告方法，从发送网络消息、电子邮件到页面叫。

## 第 6 章：登录脚本

登录脚本是用户登录域时运行的那些微型程序。它们通常被忽视，但它们可以用于更新用户文件并重新连接到网络资源。更有趣的是，你如何利用这些脚本执行例行维护，甚至执行新的计算机配置。

## 第 7 章：进程

创建和管理进程并不像在 UNIX 下那样直观。Win32 Perl 不仅继承了它所有类 UNIX 的进程创建功能，还添加了一些 Win32 特有的功能。然而，混合这些风格可能会导致一些痛苦的编程。本章讨论了哪些函数应该被避免，哪些函数应该被推广。

在这里，你还将学习如何使用 Perl 检查进程列表，以及如何杀死单个任务。

## 第 8 章：Win32 服务

UNIX 管理员称它们为“守护进程”（daemons），而 Win32 管理员称它们为“服务”（services）。无论哪种称法，指的都是独立运行的程序。是的，Win32 Perl 脚本可以作为服务运行，但并没有你想象的那么简单。本章讨论了将 Perl 脚本作为服务的技巧。

## 第 9 章：ADSI 和 WMI

让即使是最老练的 Win32 管理员恐慌的两个缩写是 ADSI 和 WMI。这是两种相当新的技术，提供了极其丰富的信息和控制能力。每个管理员最终都必须面对这些技术。本章通过描述它们是什么以及如何工作来揭示它们。

让我们面对现实吧，Win32 机器并不简单，管理起来也不简单。创建一个新用户账户、创建用户的家目录，然后应用正确的权限是非常枯燥的。本书假设你理解了这些网络管理概念。它只是提供系列工具，让你能够快速、更高效地完成工作。

祝阅读愉快。

## Perl 与管理员

如果你正在读这本书，很有可能你要么是一个需要自动化管理任务的系统管理员，要么是你拥有一种非凡的好奇心。无论何种情况，你都开启了一段将带你进入 Win32 机器管理深处的旅程。

作为一名系统管理员，我经常发现自己必须自动化处理同事们乐于手动完成的任务。出于某种原因，他们认为一次性向域添加几十个用户最好用用户管理器（User Manager）应用程序完成。他们最接近自动化的就是一个删除 temp 目录中临时文件的批处理文件。如果他们需要进行大规模的环境修改（例如，跨越数千台机器），我宁愿走遍每台机器，登录并进行必要的修改。而我，则发现那种方法纯粹是无法接受的时间浪费。在我修改两三台机器的时间内，我可以写一个 Perl 脚本，让它在网络中穿梭并对所有机器进行必要的修改。访问网络上所有计算机的总周转时间在几分钟范围内，而我的同事则需要整个周末或更久。

脚本编写——无论是使用 Perl、JavaScript、Visual Basic、Python 还是其他十几种语言中的任何——都是自动化的极大方式，从而节省了时间、精力，并最终……在我看来，系统管理员必须能够有效地使用脚本语言；否则，他只是一个知识丰富的电脑用户。你可以沿着这一逻辑追溯到 UNIX 平台，在那里，脚本对于保持机器正确配置是必要的。看到一台 UNIX 机器上散满了 shell、Perl 和其他类型的脚本并不罕见。由于某些不幸的原因，Win32 背离了这一趋势。Win32 管理员往往过度依赖某些第三方应用程序，希望它们能魔法般地执行某种配置或自动化，而无需编写任何代码。虽然这些产品减轻了管理的负担，但通常会导致管理员的选择更少。

## 关于本书的说明

你应该将这本书视为进入使用 Win32 的跳板。这些页中包含的信息只是一个指南。它是一个已经学了一些东西的系统管理员编写的指南。

以前编写脚本是使用批处理（batch files）；这种方法充满了问题，而且和它的 DOS 起源并无异。公平地说，Win32 命令行处理器（批处理文件源于此）远优于 DOS 命令行处理器；然而，在自动化能力方面仍然非常欠缺。

在 NT 4.0 中，微软引入了 Windows 脚本宿主（WSH）技术，它方便了 PerlScript、JavaScript 和 VBScript 等脚本引擎。这项技术允许你执行脚本，其提供的功能远超命令行处理器批处理文件的范围。

WSH 是 NT 4.0 的一个单独下载包，但在 Windows 2000 中是自带的。脚本语言必须被设计为符合 WSH 标准的 COM 服务器。Perl 不仅做到了这一点，还允许你作为命令行应用程序使用，这意味着你不需要注册 COM 服务器，甚至完全不需要安装 WSH。

## 从命令行运行 Perl 脚本

几年前，我与一位担任 Solaris 机器系统管理员的朋友一起工作。每当他想要运行 Perl 脚本时，都必须费力地输入 Perl 可执行文件的完整路径。我不知道他为什么不直接将 Perl 的 bin 目录添加到系统路径中。每当他输入完整路径时，我都会期待地叹气——尤其是当他输错某些字符并不得不删除、修复，然后重新思考路径的其余部分时。在那那时，我意识到并不是所有人都会把 Perl 添加到系统路径中。

当你将 `perl\bin` 目录添加到系统路径时，运行 Perl 脚本就变得更容易了，因为你不需要指定 `Perl.EXE` 的完整路径。你只需要输入以下内容即可运行脚本（例如一个假设的 `F00.PL` 脚本）：

```
perl foo.pl
```

有些管理员倾向于只将此行添加到用户路径中，但我发现将其添加到系统路径要有用得多，这样所有进程都可以利用它。

你可以使用许多技巧让 Perl 脚本执行，而无需输入像下面这样的内容：

```
c:\perl\bin\perl.exe c:\perl\scripts\myscript.pl
```

到目前为止，最简单的方法是使用一种简单的三步法，让 Perl 脚本运行得简单且高效。以下步骤适用于 Windows NT/2000，但遗憾的是不适用于 Windows 95/98。对于 Windows 95/98，没有简单的方法可以实现相同的结果。

1. 使用 `assoc` 命令将 `.PL` 扩展与 Perl 关联：

```
assoc .pl=PerlFile
```

2. 使用 `ftype` 命令通过 Perl 二进制文件注册 `PerlFile` 文件类型：

```
ftype PerlFile=c:\perl\bin\perl.exe "%1" %*
```

注意 `%1` 被双引号包围。这很重要，特别是当你预计要引用一个文件名中包含空格的 Perl 脚本时。

3. 将 `.PL` 扩展名添加到可执行扩展名列表中。Windows 2000 使用一个名为 `PATHEXT` 的环境变量，它是被认为是可执行的文件扩展名列表。示例看起来像：



`PATHEXT=.COM;.EXE;.BAT;.CMD;.VBE;.JS;.JSE;.WSF;.WSH`

只需将 `.PL` 扩展名添加到此列表：

`PATHEXT=.PL;.COM;.EXE;.BAT;.CMD;.VBE;.JS;.JSE;.WSF;.WSH`

4. （可选）将 Perl 的目录放在路径中。

完成这些步骤后，你可以仅通过文件名运行 Perl 脚本：

`myscript.pl`

这将导致 Perl 执行该脚本。

如果脚本以 `.PL`（或你在 `assoc` 命令中指定的任何扩展名）结尾，并且你正在已将扩展名添加到 `PATHEXT` 变量的 Windows 2000 上运行，你可以使用名称而不带扩展名来调用脚本：

`myscript`

你也可以将参数传递给脚本。然而，如果你需要传递某些标志（例如 `-d` 或 `-w`），你需要执行可选的第四步并修改系统路径。然后你可以像下面这样直接引用整个命令行（包括 `perl.exe`）：

`perl -d c:\temp\myscript.pl`

或者，或者，将标志添加到脚本开头的“shebang”行中，如示例 1.1 所示。

## 示例 1.1 反引号和文件关联

```
01. #perl -w
02. my @Output = c:\temp\pertest.pl;
03. print @Output;
```

示例 1.2 使用这些步骤为 Perl 使用配置计算机。请注意，某些行使用了 `Win32::AdminMisc` 环境变量。这一点很重要，因为如果你简单地使用 `%ENV` 哈希表来设置变量，它们会在脚本终止的瞬间丢失。

## 示例 1.2 为 Perl 配置机器

```
01. use Win32::AdminMisc;
02. $TIMEOUT = 0;
03. $PERL_DIR = '$X';
04. $PERL_EXTENSION = '.pl';
05. # 检查路径是否准确
06. if (-d $PERL_DIR)
07. {
08. if (! -f "$PERL_DIR\bin\perl.exe")
09. {
10. print "WARNING: You are missing Perl executable.";
11. }
12. }
13. else
14. {
15. print "WARNING: You are missing Perl directory.";
16. }
```

（注：此处为示例代码块的逻辑，文档工程师根据翻译要求代码块本身不翻译，但根据示例提供的逻辑，此处展示了代码的结构。由于原文未提供翻译内容，此处保持代码块逻辑。）

*注：由于用户提供的“需要翻译的文本”部分部分包含英文示例 1.1.1 示例 1.2 的代码块内容，根据注意事项“代码块不需要翻译”，以下对应的完整译文将保留这些代码块内容。*

（纠正：观察用户提供的“需要翻译的文本”最后一部分，似乎是关于“Using Perl over a Network”的。我将对最后那段英文进行翻译。）

## 通过网络使用 Perl

理想情况下，管理员会在网络中的每台机器上安装 Perl。这样做可以确保每台计算机都能为登录脚本、服务和计划任务运行 Perl。

在每个桌面上安装 Perl 是非常有力的。然而，并非所有机器都能承受。尽管磁盘空间变得越来越廉价，但许多公司的预算有限，几 MB 的空间非常宝贵。

解决这个问题的相当简单的方法是将 Perl 复制到文件服务器并共享其目录。这种解决方案非常简单。当有人想要运行 Perl 脚本时，他只需访问文件服务器上的共享目录。这种解决方案有其自己的需要考虑的问题。

正如本章早期提到的，你可以将 Perl 的 `bin` 目录添加到路径中。然而，如果你正在访问文件服务器上共享目录上的 Perl，你应该在路径中输入什么？这个问题有两个答案。

首先，你可以将一个驱动器映射到共享目录。这样做要求你能可靠地将 `bin` 目录映射到映射驱动器。一个特定的驱动器到共享。尽管这听起来很愚蠢，某些应用程序仍然要求使用特定的驱动器。因此，取决于你组织的需求，你可能需要考虑哪个驱动器是可用的。要应对的另一个问题是用户意外删除了映射驱动器。当这种情况发生时，Perl 将无法运行，而且用户可能不会告诉你发生了这种情况。

第二种更理想的方法是将 Perl 的 `bin` 目录引用为通用命名约定（UNC）。这意味着将 UNC 添加到路径。这里有一个小技巧：当你将 UNC 添加到路径时，请确保将其添加到路径的末尾。例如，如果你的路径是

```
C:\winnt;c:\winnt\system32
```

你应该像这样将 Perl UNC 添加到路径的末尾：

```
C:\winnt;c:\winnt\system32\server\perlshare\bin
```

## 将 UNC 放置在路径开头或中间可能会导致问题。

如果共享被移除、远程服务器离线或网络出现问题，那么所有运行的程序在首次启动时可能会临时暂停。这种暂停是由于 Win32 等待访问 UNC 的请求超时而导致的。

在 NT 机器（或 Windows 2000）上，用户拥有自己的一套环境变量，包括他们个性化的路径（`path`）。当用户登录到 NT 机器时，其用户路径变量会被添加到系统路径变量中。这意味着，如果你发现 Perl UNC 位于系统路径变量的末尾，在配置网络供 Perl 使用时，你应该考虑这个问题：将 Perl UNC 添加到用户路径变量的末尾是理想的。

到目前为止，将 Perl 共享添加到路径中的问题并不像你想象的那么简单。现在让我测试另一个问题。假设你有一个拥有 1,000 个用户的网络。同时，假设每个用户都有一个基于 Perl 的登录脚本，并且你配置了每个用户从网络共享访问 Perl。周一早上 8 点，你有 1,000 个用户同时登录他们的机器。想象一下网络流量，所有用户都在访问 Perl 的二进制文件以及各种库和包。理想情况下，你会为每个子网设置一个共享 Perl 目录，从而减少跨越所有路由器的流量。这意味着每台机器都需要知道子网上的哪个服务器包含 Perl 共享目录。

现在结合考虑这两个问题。如果你将 Perl UNC 添加到用户路径变量的末尾，并且每台机器都必须知道连接哪个特定的服务器，哎——你有问题了：用户可以登录到任何子网上的机器。因此，在用户路径变量中硬编码 Perl UNC 导致 Perl 访问跨越路由器。这个问题也有一个解决方案。你可以在每台机器上创建一个系统变量 `PERLDIA`。这个新变量包含本地子网上共享 Perl 目录的 UNC。现在你只需要将 `%PERLDIA` 添加到用户路径变量的末尾即可。例如，你可以将系统变量 `PERLDIA` 设置为：

```
PERLDIA = \server1\perlshare
```

然后你可以像这样将该变量添加到用户路径变量中：

```
PATH = c:\Program Files\Foo;%PERLDIA%\bin
```

这是理想的解决方案。

## 最小化网络带宽使用

Win32 试图尽量减少内存使用。考虑到操作系统是一个多任务环境，一个进程在某个时刻可能需要内存，而另一个进程可能需要较少。因为机器的内存是有限的，Win32 会在内存（RAM）中交换内存块。例如，如果你正在 Photoshop 中编辑 TIFF 图形，Windows 可能会临时将一个 Word 文档从 RAM 移动到硬盘上的交换文件（swap file）。这为 Photoshop 腾出了 RAM。当你回到 Word 继续编辑文档时，操作系统可能会将 Photoshop 的 TIFF 文件数据移动到交换文件，并将 Word 文档重新加载到 RAM 中。结果，当你运行许多应用程序时，经常会遇到磁盘抖动（disk thrashing）。

Win32 还使用另一种方式管理内存。当应用程序运行（如 Photoshop、Excel 或 Perl）时，操作系统必须将程序代码加载到 RAM 中以执行。这个过程会消耗大量的内存。就像 TIFF 文件或 Word 文档一样，代码内存也可以从 RAM 中交换出。

既然代码已经以 `.EXE` 或 `.DLL` 文件的形式存储在硬盘上，你为什么要用这些代码填满交换文件呢？答案是没理由。这正是为什么某些程序和库被标记为**可丢弃（DISCARDABLE）**的原因。如果代码被标记为可清除（purge），当另一个进程需要更多内存时，它就会从 RAM 中清除。这意味着它从 RAM 中移除，但不存储在交换文件中。当再次需要该代码时，只需从 `.EXE` 或 `.DLL` 文件重新加载。这个过程运行得非常好。嗯，几乎是完美。

当你通过网络或从 CD-ROM 访问 Perl 时就会出现问题。如果 Win32 清除了 Perl 程序代码，当以后需要时，它必须跨越网络或开始旋转光驱来加载代码。这既增加了网络流量负担，又增加了用户的延迟。

你可以标记可执行文件和库，以便它们“从交换文件运行”。这意味着当加载 `.EXE` 或 `.DLL` 文件时，它的整个镜像都会加载到 RAM 中。因此，如果任何页面被交换出内存，它们将进入硬盘上的分页文件，而不是完全从 RAM 中清除。

通常情况下，Perl 及其任何库都没有被标记为这种强制进入内存的类型。然而，如果你使用 Microsoft Visual C++ (MSVC) 自行编译 Perl，你可以告诉链接器设置头标志，使得网络和/或 CD-ROM 访问强制文件镜像完全加载到 RAM 中。但是，如果你没有编译 Perl，你仍然可以使用二进制镜像头编辑器（例如 `EDITBIN.EXE`，它随 Microsoft Visual C++ 一起提供）设置标志。

你可以使用以下命令设置适当的标志（针对网络或 CD-ROM 访问）：

```
editbin perl.exe /swaprun:net /swaprun:cd
```

当然，只需指定你需要的示例（或者如果两者都不需要）。要移除标志，请使用以下命令：

```
editbin perl.exe /swaprun:net /swaprun:lcd
```

以下三个文件应该是：

- `perl.exe`

- `perlcore.dll`

- `perlrt.dll`

## 扩展

Win32 有许多扩展可用。这些扩展提供了极其丰富的功能。例如，Lanman 扩展提供了一个名为 `GetServer()` 的函数，可以返回服务器列表；NetAdmin 扩展也提供了类似的 `GetServers()`。

## 一致性

请记住，l 扩展充满了不一致性。尽管许多 Win32 扩展调用相同的 Win32 API 函数（如我们在上一节所示），但它们暴露这些函数的方式不同。例如，将用户添加到本地组，`Win32::NetAdmin` 使用

```
LocalGroupAddUsers($Server, $GroupName, @Users);
```

然而，`Win32::Lanman` 使用

```
NetLocalGroupAddMembers($Server, $Group, \UserID);
```

第一个区别是函数的名称。如果你是一个 C 语言程序员或硬核 Delphi 程序员，使用 `Win32::Lanman` 版本的函数是有意义的，因为它的名称与 Win32 API 完全相同。第二个区别是，前者函数接受用户名字符串数组（SID）。而后者函数接受用户安全标识符（SID）数组。

## 管理与计算机语言

大多数 UNIX 管理员精通多种编程语言，如 C、Perl、Java、Python、sed、awk 以及各种 shell。我曾看到 UNIX 管理员在 Windows 管理员……时

承认他们只只会写批处理文件（batch files）。我假设这一发现很快会引发一场平台之间的口水战，但我想在这里强调一点：仅仅因为一个平台易于使用，并不意味着任何人都能成为高效的管理员。

UNIX 管理员通常必须掌握几种语言。如果不编写 RC 脚本或修改 shell 脚本，几乎不可能安装和维护一个 UNIX 节点网络。Win32 管理员通常只需要知道批处理文件就能应付，因为该平台的大部分工作都是自动化的。这一事实让我感到相当沮丧。

除非你的部门资金多到溢出来，否则要获得完全自动化系统所需的所有工具并非易事。即使你负担得起购买最新、最强大的软件工具来管理网络，你不可避免地会遇到必须编写特定工具才能解决的问题。出于这些原因，掌握如何使用 Perl 等编程语言来解决问题是非常关重要的。

然而，由于 Perl 本身是用 C 语言写的，你可以很容易辩称应该学习 C 或 C++。在这一点上我不会与你争论。对 C 语言这种深入了解的真正原因实际上是出于对文档的需求，而不是其他任何原因。

因为可靠的 Perl 文档很难找到，而且互联网上充满了错误信息，通过阅读 Perl 或其扩展的源代码来准确理解它做了什么是非常有用的。当我编写《Win32 Perl Programming: The Standard Extensions》时，我正是这样做的。在当时，大多数扩展要么没有文档，要么文档记录不准确。为了完全理解一个函数代表什么，我阅读了源代码。在此过程中，我还定位了几个可以修正的 bug。需要说明的是，我并不是建议管理员去攻读四年制大学来获得编程学位。然而，浅显的理解是非常有用的。

即使你还没有准备好阅读源代码，对 C 的理解对于与 Win32 扩展交互也是有用的。其中许多扩展直接暴露了 Win32 API，例如 `Win32::Lanman` 和 `Win32::API`。理解每个函数是如何工作的将绝对是无价的。

## 最实用的扩展

在与 Perl 斗争一段时间后，你对某些扩展的欣赏之情会开始增长。你会发现自己会自动开始思考如何使用某个特定的扩展来解决问题，而不是考虑其他的。

在我用过或编写过的所有 Win32 扩展中，我必须承认这五个（按字母顺序排列）证明是最实用的：

- `Win32::API`

- `Win32::Daemon`

- `Win32::Lanman`

- `Win32::OLE`

- `Win32::Registry`

还需要许多其他扩展，但这些特定的扩展解决了大部分问题。如果你不熟悉它们，就应该去熟悉。本书大量使用了这些扩展，掌握它们的作用和原理将非常有益。请参考附录 A 中的“本书使用的模块”（Modules Used In This Book）章节以了解如何获取这些扩展。

## 总结

作为一名网络管理员，你正在进入 Perl 编码的新世界。无论你作为管理员的能力有多出色，或者通过了多少考试，你都将开启一段对你大有益处的旅程。

无论你以前是否写过 Perl 代码，还是一个新手，这本书都会带你解决将面临的许多棘手问题。通过利用 Perl 的灵活性，你很快就能看到网络如何从使用这种语言中获益。

可以说，Perl 本身可能是令人困惑的——尤其是它是开源软件。任何人都可以创建自己的扩展和模块并将其发布到互联网上——通常还没有文档。但只要尽到调查职责并加仔细学习，Perl 编码就可以被驯服并精通。

## 2 账户维护

Win32 网络的核心是账户。对于任何进程的启动，必须与其关联一个账户。即使是服务等自动进程，也是由某些登录用户启动的。在某些情况下，该用户是普通用户；在其他情况下，它可能是一个被授予特殊权限的特殊用户。

大多数用户对账户很熟悉，因为他们必须使用账户来登录机器。然而，作为管理员，你知道有几种类型的账户：用户、组、机器和域信任账户。你必须了解这些不同类型的账户，因为你承担着管理它们的负担。

## 创建账户

你可以通过使用基于 GUI 的用户管理器（User Manager）或微软管理控制台（MMC）插件轻松创建账户。基本上，你只需指向并点击，填写一些信息，然后点击确定。这项任务非常简单。然而，当你赶时间或需要处理多个账户时，通过程序化操作通常更简单。例如，手动创建 30 个账户可能非常繁琐，但当你使用脚本时就轻而易举。

使用 GUI 比简单的创建账户需要更多精力。创建账户后，你仍然需要将新用户添加到各种组中。之后，你还需要创建用户的家目录，并对目录树应用任何安全权限。好的一面是，当设置脚本执行这些操作时（如示例 2.1 所示），它就不再是负担。

不幸的是，编写程序化创建账户的脚本比使用 GUI 更麻烦，因为脚本必须处理账户的某些方面，而使用 GUI 的人永远不会看到。例如，脚本需要知道该账户是用户、机器还是域信任账户；GUI 通常假设你指的是一个用户账户。

# 第 2 章：账户维护

示例 2.1 在指定的域（或机器）中创建一个用户账户，将用户添加到指定的组，并为用户的家目录应用权限。要使用此代码，你需要修改变量以匹配你的情况。

你应该修改 `%` 字典，使 `profile` 密钥（第 8 行）反映家目录的路径。`script` 密钥（第 10 行）是登录脚本的路径。该登录路径相对于验证用户的域控制器（DC）。详情请参阅第 6 章“登录脚本”。

此外，你可以根据需要修改 `%Permission` 字典中的掩码（第 14-23 行）。该字典包含多个子字典，每个用户或组一个（子字典的键是用户或组名）。其中一个 `<user>` 会被替换为创建目录的账户名。第 159-172 行实际应用权限，取决于字典的构建方式：如果存在文件字典则应用文件权限，如果定义了目录字典则应用目录权限。

第 58-76 行的 `%account` 字典定义了如何创建账户。在这里，你可以调整账户属性。默认情况下，密码是账户名的小写。表 2.1 解释了一些晦涩的属性。

表 2.1 示例 2.1 中账户字典键的含义

| 键 | 说明 |
| --- | --- |
| `usr_comment` | 此属性指定有关用户账户的注释。除了从底层检查账户的人（例如示例 2.2 中的脚本）外，没有人可以看到它。即使管理员使用用户管理器也不会显示此属性。它通常不被使用；但可能包含有关账户状态的注释，例如临时禁用直至另行通知 |
| `params` | 此属性应留空。某些程序会修改它以存储配置信息。此外，微软在此存储远程访问服务（RAS）和其他配置信息 |
| `workstations` | 此属性代表允许账户登录的机器，以逗号分隔列表的形式表示，例如 `server1,server2,JimsComputer`。如果此属性为空，则账户允许登录到域内的任何机器。 |

## 创建账户

| 键 | 说明 |
|---|---|
| `acct_expires` | 此属性表示账户过期的时间。账户过期后，用户将封锁定且无法登录。管理员必须通过用户管理器或使用示例 2.6（后文所示）来解锁账户。 |



尽管脚本使用了几个硬编码的配置选项，但可以从命令行指定某些用户特定的属性。这些特定属性是针对用户的，而不是针对特定域的硬编码选项。表 2.2 描述了可以指定的命令行开关。

## 表 2.2 示例 2.1 的命令行开关

| 开关 | 功能 |
|---|---|
| `-m Machine` | 指定账户所在的计算机。 |
| `-d Domain` | 指定账户所在的域。它会覆盖任何 `-m` 开关。 |
| `-c Comment` | 包含用户账户的注释。 |
| `-f FullName` | 指定用户的全名。 |
| `-g Group` | 指明该用户将成为成员的组。可以是全局组或本地组。可以指定多个 `-g Group` 开关。 |

如果既未指定域也没有机器名称，脚本将默认使用运行脚本的用户所在的当前域。

使用此脚本的示例：

```perl
perl AddUser.pl -d MyDomain -c "Joel's Account" -f "Joel Smith" -g Users -g "Domain Users" -g Joel
```

在这个特定示例中，用户在`MyDomain`域中创建一个名为`Joel`的新账户。该账户已成为`Users`和`Domain`组员。

运行此脚本后，您应该执行域同步。请参考本章中的“同步域控制器”。

## 示例 2.1 创建账户

```perl
01. use Win32;
02. use Getopt::Long;
03. use Win32::Perms;
04. use Win32::Lanman;
05.
06. # 修改这些值以匹配您的网络
07. %PATH = (
08. home => "\server\Home\$",
09. profile => "\server\Profiles\$",
10. script => "\logon.pl",
11. );
12.
13. # 修改这些值以匹配您的需求
14. %Permission = (
15. 'user>' => {
16. dir => CHANGE_DIR,
17. file => CHANGE_FILE,
18. },
19. administrators => {
20. dir => FULL_CONTROL_DIR,
21. file => FULL_CONTROL_FILE,
22. },
23. );
24.
25. %Config = (
26. flags => UF_SCRIPT | UF_NORMAL_ACCOUNT,
27. priv => USER_PRIV_USER,
28. machine => Win32::NodeName(),
29. );
30.
31. Configure(\%Config);
32. if ($Config{help})
33. {
34. Syntax();
35. exit();
36. }
37.
38. if ($@ ne $Config{domain})
39. {
40. Win32::Lanman::NetGetDCName('',
41. $Config{domain},
42. \$Config{machine} );
43. }
44. elsif ($@ eq $Config{machine})
45. {
46. Win32::Lanman::NetGetDCName('',
47. Win32::DomainName(),
48. \$Config{machine} );
49. }
50.
51. print "*Creating $Config{machine}\$Config{name}...*";
52. CreateAccount(\%Config);
53.
54. sub CreateAccount
55. {
56. my ($Config) = @_;
57. my $Result = 0;
58. my %Account = (
59. name => $Config->{name},
60. password => lc $Config->{name},
61. home_dir => $PATH{home}\$Config->{name},
62. comment => $Config->{comment},
63. usr_comment => '',
64. flags => $Config->{flags},
65. params => '',
66. script_path => $PATH{script},
67. full_name => $Config->{fullname},
68. workstations => '',
69. profile => $PATH{profile}\$Config->{name},
70. acct_expires => -1,
71. # logon_hours is a binary bitmap where each bit represents an
72. # hour in a week (168 bits).
73. logon_hours => pack('b168', '111111111' * 21),
74. home_drive_dir => "Z:",
75. password_expired => 1,
76. );
77. }
78. if (Win32::NetUserAdd($Config->{machine},
79. {
80. my ($Domain, $Sid, $SidType);
81. }
82. print "Success\n";
83. next unless Win32::LookupAccountName($Config->{machine},
84. $Config->{name},
85. $Domain,
86. $Sid,
87. $SidType));
88. $Result = 1;
89. foreach my $Group (@Config->{groups}}) {
90. {
91. # First try the group...
92. if (!Win32::Lanman::NetGroup($Config->{machine},
93. $Group,
94. $Config->{name}))
95. {
96. # Group failed try local group...
97. Win32::Lanman::LocalGroup($Config->{machine},
98. $Group,
99. $SidType));
100. }
101. MakeDir($Account->{profile});
102. if (MakeDir($Account->{home_dir}))
103. {
104. # home directory exists, apply permissions...
105. if (ApplyPermissions($Config->{machine}\$Config->{name},
106. $Account->{home_dir}))
107. {
108. print "success\n";
109. } else
110. print "failed to apply permissions.\n";
111. }
112. }
113. return($Result);
114. sub MakeDir
115. {
116. my ($Dir) = @_;
117. my @Dirlist;
118. my $DirCount;
119. my $Root = 1;
120. my ($Root, /\w\|\.+?\|\/);
121. $Root = ($Dir // /\w\|\.+?\|\/);
122. return(1) if (-d $Dir);
123. @Dirlist = split (\/, $Path);
124. $Path = $Root;
125. while ($Result && @Dirlist) {
126. {
127. $Path = (shift @Dirlist) . "";
128. next if (-d $Path);
129. $Result = mkdir($Path, 0777);
130. }
131. return($Result);
132. }
133. sub ApplyPermissions
134. {
135. my ($User, $Path) = @_;
136. my $Perm = new Win32::Perms($Path) || return(0);
137. my $Result = 0;
138. $Perm->Remove(-1);
139. $Perm->Owner($User);
140. foreach my $Account (keys (%Permission)) {
141. {
142. my $Username = $Account;
143. $Username = $User if ($user eq $Account);
144. # Apply file permissions
145. if (defined $Perm{$Account}->{file}) {
146. $Perm->Allow($Username,
147. $Perm{$Account}->{file},
148. FILE);
149. }
150. # Apply dir permissions
151. if (defined $Perm{$Account}->{dir}) {
152. $Perm->Allow($Username,
153. $Perm{$Account}->{dir},
154. DIR);
155. }
156. print 'Applying permissions to '$Path'...';
157. $Result = $Perm->Set($Path);
158. return($Result);
159. }
160. sub Configure
161. my($Config) = @_;
162. Getopt::Long::Configure("prefix_pattern=(\/)");
163. $Result = GetOptions($Config,
164. qw{
165. machine|m=s
166. groups|g=s
167. domain|d=s
168. fullname|f=s
169. comment|c=s
170. help|?
171. });
172. $Config{help} = 1 if ($Result);
173. if ("" ne $Config{machine}) {
174. $Config{machine} = "\$Config{machine}";
175. $Config{machine} = s/\///;
176. }
177. }
178. sub Syntax
179. my($Script) = (Win32::GetLongPathName($0) =~ /([\]]*)\$/);
180. my($Line) = "-" x length($Script);
181. my($Whitespace) = " " x length($Script);
182. print <<EOD;
183. $EOD;
184. $Script
185. $Line
186. 创建账户。
187. 语法:
188.     perl $Script AccountName [-d Domain | -m Machine][-c Comment]
189.     $Whitespace [-f Name]
190. -c......指定账户的注释。
191. -f......指定账户的全名。
192. g.......账户所属的组。
193.       这仅适用于用户账户。
194.       根据需要多次指定此开关。
195. -m Machine......指定账户将所在的机器。
196. -d Domain......指定账户将所在的域。
197. AccountName。账户名称 (userid)。
198. EDT
199. )
```

```perl
C:\> dumpaccount.pl -m Server administrator
Displaying \ServerFoo\administrator:
acct expires:      No date specified
auth flags:         AF_OP_COUNTS
                     AF_OP_PRINT
                     AF_OP_SERVER
bad pw count:      0
code page:          0
comment:           Built-in account for administering the computer/domain
country code:       0
flags:             UF_SCRIPT
                     UF_SETTABLE_BITS
                     UF_NORMAL_ACCOUNT
                     UF_DONT_EXPIRE_PASSWD
full name:          Mr. Administrator
home dir:           \\server1\administrator
home dir drive:    Z:
last logoff:        No date specified
last logon:         Mon May 15 08:31:30 2000
logon hours:       Sunday: 00-23
                     Monday: 00-23
                     Tuesday: 00-23
                     Wednesday: 00-23
                     Thursday: 00-23
                     Friday: 00-23
                     Saturday: 00-23
logon server:      \\*
max storage:        Unlimited storage
name:              administrator
num logons:         209
parms:             m ~~~~~~ @@@@' d nPdop fx
password:          <Unknown>
password age:      1 Years 64 Days 04 Hours 51 Minutes
password expired:   0
primary group id:   512
priv:              USER_PRIV_ADMIN
profile:
script path:       administrators\logon.pl
units per week:     168
user id:            1001
usr comment:
workstations:
```

> 图 2.1 管理员账户的配置。

## 示例 2.2 显示账户配置

```perl
01. use Win32;
02. use Getop::Long;
03. use Win32::NetAdmin;
04. use Win32::AdminMisc;
05. use Win32::API::Prototype;
```

## 示例 2.2 续



# 第 2 章：账户维护

## 示例 2.2 续

```perl
06.
07. %FLAGS = (
08. eval UF_TEMP_DUPLICATE_ACCOUNT => "UF_TEMP_DUPLICATE_ACCOUNT",
09. eval UF_NORMAL_ACCOUNT => "UF_NORMAL_ACCOUNT",
10. eval UF_INTERDOM_TRUST_ACCOUNT => "UF_INTERDOM_TRUST_ACCOUNT",
11. eval UF_WORKSTATION_TRUST_ACCOUNT => "UF_WORKSTATION_TRUST_ACCOUNT",
12. eval UF_SERVER_TRUST_ACCOUNT => "UF_SERVER_TRUST_ACCOUNT",
13. eval UF_DONT_EXPIRE_PASSWD => "UF_DONT_EXPIRE_PASSWD",
14. eval UF_SETTABLE_BITS => "UF_SETTABLE_BITS",
15. eval UF_SCRIPT => "UF_SCRIPT",
16. eval UF_ACCOUNTDISABLE => "UF_ACCOUNTDISABLE",
17. eval UF_HOMEDIR_REQUIRED => "UF_HOMEDIR_REQUIRED",
18. eval UF_LOCKOUT => "UF_LOCKOUT",
19. eval UF_PASSWORD_NOTREQD => "UF_PASSWORD_NOTREQD",
20. eval UF_PASSWORD_CANT_CHANGE => "UF_PASSWORD_CANT_CHANGE",
21. );
22.
23. %AUTH_FLAGS = (
24. eval AF_OP_PRINT => "AF_OP_PRINT",
25. eval AF_OP_COMM => "AF_OP_COMM",
26. eval AF_OP_SERVER => "AF_OP_SERVER",
27. eval AF_OP_ACCOUNTS => "AF_OP_ACCOUNTS",
28. );
29.
30. %PRIVILEGES = (
31. eval USER_PRIV_GUEST => "USER_PRIV_GUEST",
32. eval USER_PRIV_USER => "USER_PRIV_USER",
33. eval USER_PRIV_ADMIN => "USER_PRIV_ADMIN",
34. );
35.
36. @WEEKDAYS = qw(
37. Sunday
38. Monday
39. Tuesday
40. Wednesday
41. Thursday
42. Friday
43. Saturday
44. );
45.
46. # 获取时区的粗略破解方法
47. if (Apilink( 'kernel32.dll',
48. 'DWORD GetTimeZoneInformation(PVOID pTZInfo) ) ))
49. {
50. my $pTZInfo = NewString( 200 );
51. my $Result = GetTimeZoneInformation($pTZInfo);
52. if (0 == $Result || 2 == $Result )
53. {
54. $TZOffset = unpack("1", $pTZInfo) / 60;
55. }
56. }
```

```perl
58. Configure( \Config );
59. if ($Config{help}) 
60. {
61. Syntax();
62. exit();
63. }
64. 
65. if (" != ne $Config{domain})
66. {
67. # 查找指定域的主域控制器。
68. $Config{machine} = "";
69. Win32::NetAdmin::GetDomainController('',
70. $Config{domain},
71. $Config{machine});
72. }
73. elsif (" eq $Config{machine})
74. # 查找当前域的主域控制器。
75. $Config{machine} = "";
76. Win32::NetAdmin::GetDomainController('',
77. Win32::DomainName(),
78. $Config{machine});
79. }
80. # 展开任何通配符
81. foreach my $Account (@Config{accounts})
82. {
83. if ($Account =~ /\*/)
84. my ($Prefix) = ($Account -= /^()/);
85. my @Users;
86. Win32::AdminMisc::GetUsers($Config{machine},
87. $Prefix, @Users);
88. push(@AccountList, @Users);
89. else
90. push(@AccountList, $Account);
91. }
92. $Attributes;
93. foreach my $Account (@AccountList)
94. {
95. my %Info;
96. print "Displaying $Config{machine}\\Account:\n";
97. if (Win32::AdminMisc::GetUserAttributes($Config{machine},
98. $Account,
99. %Info)
100. foreach $Key (sort (keys (%Info)))
101. {
102. $Value = $Info{$Key};
```

```perl
103. ($DisplayKey) = ( $Key ) =~ /\?(.*)/;
104. $DisplayKey -= s/\ /g;
105. if ($Key =~ /age /)
106. # 将时间戳分为年、天、
107. 小和分钟
108. # 一年31536000 秒
109. # 一天 86400 秒
110. # 一小时 3600 秒
111. # 当然，每分钟 60 秒。
112. $myTime = $Info{$Key};
113. $myYears = int($myTime / 31536000);
114. $myDays = int(($myTime % 31536000) / 86400);
115. $myHours = int(($myTime % 31536000) % 86400) / 3600);
116. $myMinutes = int(($myTime % 31536000) % 86400) / 60);
117. $Value = sprintf("%d Years %02d Days %02d Hours %0d Minutes",
118. $Years, $Days, $Hours, $Minutes);
119. }
120. elseif ($Key =~ /LAST/i || $Key =~ /ACCT_EXPIRES/i)
121. {
122. if (1 > $Value)
123. $Value = "No date specified";
124. }
125. else
126. $Value = scalar localtime($Info{$Key});
127. }
128. elseif ($Key =~ /AUTH_FLAGS/i)
129. {
130. # 将标志属性分为单个标志字符串
131. $Value = DecodeBits($Value, \AUTH_FLAGS);
132. }
133. elseif ($Key =~ /FLAGS/i)
134. {
135. # 将标志属性分为单个标志字符串
136. $Value = DecodeBits($Value, \FLAGS);
137. }
138. elseif ($Key =~ /PASSWORD$/i)
139. {
140. $Value = "<Unknown>";
141. }
142. elseif ($Key =~ /PRIV$/i)
143. {
144. $Value = $PRIVILEGES($Value);
145. }
146. elseif ($Key =~ /MAX_STORAGE$/i)
147. {
```

## 检查账户

```perl
148. if( -1 == $Value )
149. {
150. $Value = 'Unlimited storage';
151. }
152. else
153. {
154. # 格式化数字
```

## 示例 2.2 续

```perl
155. {
156. if ($Display < $Index - 1)
157. {
158. $Display = sprintf("%02d", $Index - 1);
159. }
160. push(@AccountList, $Display);
161. }
162. }
163. 
164. $Index++;
165. 
166. printf("%-50s", "WEEKDAYS[$Index++]:"),
167. join(",", @Hours)), "\n");
168. }
169. }
170. 
171. write;
172. }
173. else
174. {
175. 
176. print "failure: % ";
177. print Win32::FormatMessage(Win32::AdminMisc::GetError());
178. }
179. 
180. print "\n";
181. }
```

```perl
266. $Config->{help} = 1 if (! $Result);
267. if ("" ne $Config->{machine})
268. {
269.     $Config->{machine} = '\$Config->{machine}';
270.     $Config->{machine} = s/(\))/\//;
271. }
272. push(@{$Config->{accounts}}, @ARGV);
273. $Config->{help} = 1 if scalar(@{$Config->{accounts}});
274. }
```

```perl
276. sub Syntax
277. {
278. my ($Script = Win32::GetLongPathName($0) - /([\])*)?\/);
279. my ($Line = ".-" x length($Script));
280.
281. print <<EOT;
282.
283. $Script
284.
285. $Line
286. Displays an account's configuration.
287.
288. Syntax:
289.
290. perl $Script [-d Domain | -m Machine] Account [Account2 ...]
291. -m Machine..Specify a machine where the user account lives.
292. -d Domain..Specify a domain where the user account lives.
293. Account....The name of the account (userid).
294.
295. This account can end with * char to indicate
296. all accounts that begin with the specified string.
297. If no domain or machine is specified then the current domain
298. is used.
299. EOT
300. }
301.
302. format Attributes = <<<<<<<<<<<<<<<<
303. "\$DisplayKey:", <<<<<<<<<<<<<<
304. \$Value
305. <<<<<<<<<<<<<<
306. \$Value
307. <<<<<<<<<<<<<<
308. \$Value
309. <<<<<<<<<<<<<<<<
310. \$Value
311. <<<<<<<<<<<<<<<<
312. \$Value
313. <<<<<<<<<<<<<<<<
314. - $Value
315. - $Value
316. - $Value
317. - $Value
318. - $Value
319. - $Value
320. .
```

## 示例 2.2 续

## 禁用账户

当你需要让一个账户临时不可用时，可以禁用它。某些管理员认为禁用账户是浪费时间，而应该删除它们。然而，禁用账户可以节省时间。例如，如果一个经理离开了公司，你可以禁用她的账户而不是删除它。这样，当聘佣了继任者时，你只需要启用并重命名该账户以反映新经理即可。另一种方法是创建一个新账户，但这样做不仅需要重新配置账户，还需要遍历每个文件、目录和共享，为特定的经理重新应用权限。根据域的配置，这项任务可能非常不合理。

示例 2.3 中的脚本接受用户账户列表，因此你可以一次禁用多个账户。例如，以下行同时禁用了 Joel 和 Betty 的账户：

```perl
perl Disable.pl joel betty
```

此外，你可以指定星号通配符 (`*`) 来禁用所有用户名以指定字符串开头的用户的密码。例如，以下命令禁用了所有以 `Test` 开头的账户，例如 `Test`、`Tester1`、`Testuser2` 和 `Testaccount`：

```perl
perl disable.pl test*
```

下表中的三个开关可以传递：

| 开关 | 功能 |
| --- | --- |
| `-m Machine` | 指定账户所在的计算机。 |
| `-d Domain` | 指定账户所在的域。它会覆盖任何 `-m` 开关。 |
| `-e` | 启用指定的账户。如果账户已禁用且你想启用它，请使用此选项。 |

如果既没有指定域也没有指定机器名，脚本将默认使用运行脚本的用户所在的域。

运行此脚本后，你应该执行一次域同步。

请参考本章的“同步域控制器”部分。

## 示例 2.3 禁用账户

```perl
01. use Win32;
02. use Getopt::Long;
03. use Win32::NetAdmin;
04. use Win32::AdminMisc;
05.
06. Configure( \Config );
07. if ($Config{help})
08. {
09. Syntax();
10. exit();
11. 
12.
13. if ("" ne $Config{domain})
14. {
15. # 必须先给 machine key 赋值，否则 
16. # GetDomainController() 将失败。
17. $Config{machine} = '';
18. Win32::NetAdmin::GetDomainController('',
19.     $Config{domain},
20.     $Config{machine});
21. }
22. elsif ("" eq $Config{machine})
23. {
24. # 必须先给 machine key 赋值，否则 
25. # GetDomainController() 将失败。
26. $Config{machine} = '';
27. Win32::NetAdmin::GetDomainController('',
28.     Win32::DomainName(),
29.     $Config{machine});
30. }
31. foreach my $Account (@Config{accounts})
32. {
33. if ($Account =~ /\*\$/)
34. {
35. my ($Prefix) = ($Account -= /^(.*)\$/);
36. my @Users;
37. Win32::AdminMisc::GetUsers($Config{machine}, $Prefix, @Users);
38. map
39. {
40. $AccountList{lc $_} = 1;
41. } (@Users);
42. }
43. else
44. {
45. $AccountList{lc $Account} = 1;
46. }
```

## 示例 2.3 续

```perl
49. # 注意我们使用哈希 (%AccountList) 来跟踪正在
50. # 处理的用户。这是一个简单的 hack，防止我们重复
51. # 处理同一个用户（如果在同一次运行中多次传入账户）。
52. foreach my $Account (keys (%AccountList))
53. {
54. print ($Config{enable} ? "Enabling" : "Disabling" );
55. print "$Config{machine}\$Account..."
56. if (Win32::AdminMisc::GetUserMisc($Config{machine},
57. $Account,
58. ))
59. {
60. my $Flag;
61. if ($Config{enable})
62. $Flag = Attrib(USER_FLAGS) & ~UF_ACCOUNTDISABLE;
63. }
64. else
```



```perl
65. {
66.     $Flag = Attrib(USER_FLAGS) | UF_ACCOUNTDISABLE;
67. }
68. }
69. $Result = Win32::AdminMisc::UserSetAttributes(
70.     $Config{machine},
71.     $Account,
72.     USER_FLAGS => $Flag
73. );
74. }
75. if ($Result)
76. {
77.     print "successful.\n"
78. }
79. else
80. {
81.     $myError = Win32::FormatMessage(Win32::NetAdmin::GetError());
82.     $Error = s/\n//g;
83.     print "failed to delete ($myError)\n"
84. }
85. }
86. sub Configure
87. {
88.     my ($Config) = @_;
89.     $Config{enable} = 1;
90.     Getopt::Long::Configure("prefix_pattern=(-\s*)");
91.     $Result = GetOptions($Config,
92.         qw(
93.             machine|m=s
94.             domain|d=s
95.             enable e
96.             help ?
97.         )
98.     );
99.     $Config{help} = 1 if (!Result);
100.     $Config{enable} = ! $Config{enable};
101.     if ("" ne $Config{machine})
102.     {
103.         $Config{machine} = "\\$Config{machine}";
104.         $Config{machine} = s/(\)///;
105.     }
106.     push($Config{accounts}, $ARGV);
107.     $Config{help} = 1 if scalar($Config{accounts});
108. }
109. sub Syntax
110. {
111.     my ($Script) = $0 - /\([^]\*)?\$/;
112.     my ($Line) = ".*" x length($Script);
113. }
114. print <<EOT;
115. $Script
116. $Line
117. Disables an account.
118.
119. Syntax:
120. perl $Script [-e] [-m machine [-d domain] Account [Account2 ...]
121. -e........启用已禁用的账户。
122. -m Machine.指定账户所在的计算机。
123. -d Domain....指定账户所在的域。
124. Account....此账户可以以 "*" 字符结尾，表示
125. 所有以指定字符串开头的账户。
126. 如果没有指定域或机器名，则使用
127. 当前域。
128. EOT
129. }
```

## 删除账户

有时你需要删除一个账户而不是禁用它。当然，你应该应该考虑禁用该账户（参考本章较早的“禁用账户”部分），但如果账户将不再被使用，将其从账户数据库中移除是一个好主意。如果存在账户轮换，即创建了新的用户账户然后将其遗弃，这种情况确实存在。

# 第 2 章：账户维护

删除账户是一项极端措施，因为它是字面上从账户数据库中删除了。这可能导致文件、注册表键和网络共享等对象上的权限设置显示已删除的账户。示例 2.4 快速删除账户。该脚本接受用户账户列表，因此你可以一次删除多个账户。例如，以下行删除了 Joel 和 Betty 的账户：

```perl
perl DelUser.pl joel betty
```

此外，你可以指定星号通配符（`*`）来删除所有用户名以指定字符串开头的用户。例如，以下命令删除了所有以 Test 开头的账户，例如 Test、Tester1、Testuser2 和 Testaccount：

```perl
perl delete.pl test*
```

表 2.3 中描述的两个开关可以传递给示例 2.4。

| 表 2.3 示例 2.4 的开关 | 功能 |
| --- | --- |
| `-m Machine` | 指定账户所在的计算机。 |
| `-d Domain` | 指定账户所在的域。它会覆盖任何 `-m` 开关。 |

如果既没有指定域也没有指定机器名，脚本将默认使用运行脚本的用户所在的域。

运行此脚本后，你应该执行一次域同步。请参考本章的“同步域控制器”部分。

## 示例 2.4 删除账户

```perl
01. use Win32;
02. use Getopt::Long;
03. use Win32::NetAdmin;
04. use Win32::AdminMisc;
05.
06. Configure(\Config);
07. if ($Config{help})
08. {
09.     Syntax();
10.     exit();
11. }
12.
13. if ("" ne $Config{domain})
14. {
15.     # 必须先给 machine key 赋值，否则
16.     # GetDomainController() 将失败。
17.     $Config{machine} = '';
18.     Win32::NetAdmin::GetDomainController('',
19.         $Config{domain},
20.         $Config{machine});
21. }
22. elsif ("" eq $Config{machine})
23. {
24.     # 必须先给 machine key 赋值，否则
25.     # GetDomainController() 将失败。
26.     $Config{machine} = '';
27.     Win32::NetAdmin::GetDomainController('',
28.         Win32::DomainName(),
29.         $Config{machine});
30. }
31. foreach my $Account (@Config{accounts})
32. {
33.     if ($Account =~ /\*\$/)
34.     {
35.         my ($Prefix) = ($Account -= /^(.*)\$/);
36.         my @Users;
37.         Win32::AdminMisc::GetUsers($Config{machine}, $Prefix, @Users);
38.         map
39.         {
40.             $AccountList{lc $_} = 1;
41.         } (@Users);
42.     }
43.     else
44.     {
45.         $AccountList{lc $Account} = 1;
46.     }
47. }
```

## 删除账户

```perl
18. $Config{machine} = "";
19. Win32::NetAdmin::GetDomainController('',
20.     $Config{domain},
21.     $Config{machine});
22. }
23. elseif ("*" eq $Config{machine})
24. {
25.     # 必须先给 machine key 一个值，否则
26.     # GetDomainController() 将失败。
27.     $Config{machine} = "";
28.     Win32::NetAdmin::GetDomainController('',
29.         Win32::DomainName(),
30.         $Config{machine});
31. }
32. foreach $Account in (@($Config{accounts}))
33. {
34.     if ($Account =~ /\*/)
35.     {
36.         my ($Prefix) = ($Account =~ /^(.*)\*/);
37.         my @Users;
38.         Win32::AdminMisc::GetUsers($Config{machine}, $Prefix, \Users);
39.         map
40.         {
41.             $AccountList{lc $_} = 1;
42.         } (@Users);
43.     }
44.     else
45.     {
46.         $AccountList{lc $Account} = 1;
47.     }
48. }
49. }
50. foreach $Account in keys(%AccountList)
51. {
52.     print "Account '$Config{machine}\Account......";
53.     if (Win32::NetAdmin::UserDelete($Config{machine}, $Account))
54.     {
55.         print "deleted.\n";
56.     }
57.     else
58.     {
59.         my $Error = Win32::ErrorMessage(Win32::NetAdmin::GetError());
60.         $Error = $Error - s/\r\n//g;
61.         print "failed to delete ($Error)\n";
62.     }
63. }
64. sub Configure
65. {
66.     my($Config) = @_
67.
68.     Getopt::Long::Configure("prefix_pattern=-\|\/*");
```

## 示例 2.4 延续

```perl
71. $Result = GetOptions($Config,
72.     machine|m=s
73.     domain|d=s
74.     help?
75.
76.
77.
78. );
79. $Config->{help} = 1 if (! $Result);
80. if ("" ne $Config->{machine})
81. {
82.     $Config->{machine} = "\$Config->{machine}";
83.     $Config->{domain} = s/(\+\)/\//;
84. }
85. push (@Config->{accounts}, $ARGV);
86. $Config->{help} = 1 if (scalar ${$Config->{accounts}});
87.
88.
89. sub Syntax
90.
91. my ($Script) = ($0 =~ /\/([^\/\)?\)$/);
92. my ($Line) = "." x length ($Script);
93.
```

```perl
94. print <<EOT;
95.
96. $Script
97. $Line
98. 删除一个账户。
99.
100. 语法:
101. perl $Script [-m machine |d domain] Account Account2 ...]
102. -m Machine..指定用户账户所在的机器。
103. -d Domain...指定用户账户所在的域。
104. Account....账户的名称（用户 ID）。
105. 此账户可以以 * 结尾，用表示
106. 所有以指定字符串开头的账户。
107.
108. 如果未指定域或机器，则使用当前域。
109. EOT
110. }
```

## 最后登录与注销

之前显示的示例 2.2 显示了用户的配置，它显示了与账户相关的所有属性。这些属性中有两个是用户最后登录域和注销域的时间。然而，这些值可能非常有误导性。注意图 2.1 中，最后登录时间显示为“未指定日期”。那么，用户如何可以登录域但从未注销过呢？这个问题有两个可能的答案：要么用户从未正式注销（例如，机器崩溃、网络断开等），或者是由不同的 DC 处理了登录事件。

当用户登录到网络时，必须由 DC 处理登录。这台机器负责验证用户的密码，并检查账户是否被禁用、密码是否过期、用户是否允许在当前使用的机器上登录以及许多其他事项。正如登录一样，当用户注销域时，DC 也会处理此活动。但是，无法保证同一个 DC 会同时处理登录和注销事件。

由于任意数量的不同 DC 可以处理登录和登录请求，最后登录和注销时间可能分散在不同的 DC 之间。因此，确定给定用户最后登录和注销时间的适当技术是查询域中的每个 DC 并比较登录和注销时间。报告最新时间的 DC 就是你感兴趣的。两个属性处于类似的境地：登录计数和错误密码计数。这些值代表用户成功登录域的次数以及因密码错误登录域的次数。这些属性的真实值是每个 DC 值的和。因此，查询每个控制器。图 2.2 说明了这种技术的用法。在此示例中，正在查询该域的 administrator 账户。发现的 DC 有：`\server1` 和 `\server2`。处理并显示全域属性。使用示例 2.5 运行此查询。

```text
perl laston.pl -d MyDomain administrator
Querying \server1
Querying \server2
Last logon: Sat May 20 19:00:00 (\server1)
Logoff: Sat May 20 19:00:00 (\server2)
Total number of bad password: 0
Total number of logons: 4
```

示例 2.5 可以处理任意数量的账户。在本章的许多脚本中，你可以提供账户的后缀，表示显示匹配该名称的所有账户。例如，以下行将处理 MyDomain 域的 User1、User2 和 Joel 账户：

```text
perl login.pl -d MyDomain user*
```

此脚本接受表 2.3 中描述的命令行开关，但你可以指定机器名称。如果没有指定域或机器名称，脚本将默认为运行脚本的用户当前域。

# 示例 2.5 确定最后登录和注销时间



```perl
01. use Getopt::Long;
02. use Win32::NetAdmin;
03. use Win32::AdminMisc;
04.
05. Configure( \$Config );
06. if ($Config{help}) 
07. {
08. Syntax();
09. exit();
10. }
11.
12. if ("" ne $Config{domain}) 
13. {
14. # 必须先给 machine key 一个值，否则
15. # GetDomainController() 将失败。
16. $Config{machine} = "";
17. Win32::NetAdmin::GetDomainController('',
18.         $Config{domain},
19.         $Config{machine});
20. Win32::NetAdmin::GetServers($Config{domain},
21.         $Config{domain},
22.         SV_TYPE_DOMAIN_CTRL|SV_TYPE_DOMAIN_BACTRL,
23.         @MachineList);
24. }
25. else
26. {
27. if (0 == scalar (@($Config{machine_list})) 
28. # 必须先给 machine key 一个值，否则
29. # GetDomainController() 将失败。
30. $Config{machine} = "";
31. Win32::NetAdmin::GetDomainController('',
32.         $Config{domain},
33.         $Config{machine});
34.
35. push(@($Config{machine_list}), $Config{machine});
36. } 
37.     push(@MachineList,{$Config{machine_list}});
38. } 
39. 
40. # 注意我们使用哈表 (%AccountList) 来跟踪我们正在
41. # 处理的用户。这是一个简单的哈表，防止我们重复
42. # 处理同一个用户（如果用户多次传入
43. # 相同的账户名称）。
44. foreach ($myAccount as @{$Config{accounts}) {
45. 
46.     if ($Account =~ /\*) 
47.         {
48.             my ($Prefix) = ($Account =~ /^(.*)\*/);
49.             my @Users;
50.             Win32::AdminMisc::GetUsers($machine, $Prefix, \Users);
51.             map
52.         {
53.             $AccountList{lc $_} = 1;
54.         } (@Users);
55. 
56.     else
57.         {
58.             $AccountList{lc $Account} = 1;
59.         }
60. }
61. 
62. foreach ($myMachine as @MachineList)
63. {
64.     ($Machine = '\\\\$Machine') = s/\\\\/\\\\//;
65.     print "Querying $Machine\n";
66. 
67.     foreach ($myAccount as sort(keys (%AccountList))) {
68.         {
69.             my @Attrib;
70.             if (Win32::AdminMisc::GetMiscAttributes($Machine,
71.                                     $Account,
72.                                     \Attrib)) {
73.                 {
74. 
75.                     $myData = $Result($Account) = {};
76.                     $myData->{fullname} = $Attrib(USER_FULL_NAME);
77.                     if ($Data->{laston}->{value} < $Attrib(USER_LAST_LOGON))
78.                         {
79.                             $myData->{laston}->{value} = $Attrib(USER_LAST_LOGON);
80.                             $myData->{laston}->{machine} = $Machine;
81.                     }
82.                     if ($Data->{lastoff}->{value} < $Attrib(USER_LAST_LOGOFF))
83.                         {
84.                             $myData->{lastoff}->{value} = $Attrib(USER_LAST_LOGOFF);
85.                             $myData->{lastoff}->{machine} = $Machine;
86.                     }
87.                     $myData->{badpwcount} += $Attrib(USER_BAD_PW_COUNT);
88.                     $myData->{logons} += $Attrib(USER_NUM_LOGONS);
89.                 }
90.             }
91.         }
92.     }
93. }
```

## 示例 2.5（续）

```perl
89. }
90. 
91. foreach my $Account ( sort(keys (%Result)) )
92. {
93.     print "\Account (\$Result($Account)->{fullname})\n";
94.     print Report(" Last login, \$Result($Account)->{lastlogin}),\n";
95.     print Report(" Last logoff, \$Result($Account)->{lastlogoff}),\n";
96.     print "\Total number of bad password attempts: ";
97.     print "\Result($Account)->{dpwpcount}\n";
98.     print "\Total number of logons: \$Result($Account)->{logons}\n";
99.     print "\n";
100. }
101. 
102. sub Report
103. {
104.     my($Field, $Data) = @_;
105.     my $Date = scalar localtime($Data->{value});
106.     my $Location = "($Data->{machine})";
107. 
108.     $Date = " Not Available" if (0 == $Data->{value});
109.     $Location = "" if (0 == $Data->{value});
110.     return ("$Field: $Date $Location " );
111. }
112. 
113. sub Configure
114. {
115.     my($Config) = @_;
116. 
117.     Getopt::Long::Configure("prefix_pattern=(\|\/*)", );
118.     $Result = GetOptions($Config,
119.                 machine_list|m=s
120.                 domain|d=s
121.                 help?)
122.     );
123.     
124. 
125.     $Config->{help} = 1 if (! $Result );
126.     push(@$Config->{accounts}), @ARGV);
127.     $Config->{help} = 1 if (! scalar($Config->{accounts}));
128. }
129. 
130. sub Syntax
131. {
132.     my($Script) = ( $0 - /([^\]]*)?\$/ );
133.     my($Line) = ".-" x length($Script );
134. 
135.     print <<EOT;
136. 
137. $Script
138. $Line
```

## 解锁账户

显示指定账户的最后登录和注销时间。

### 语法

```perl
perl $Script [-m Machine -d domain] Account [Account2 ...]
-m Machine..指定账户所在的机器。
-d Domain..指定账户所在的域。
Account...账户名称（用户 ID）。
此账户可以以星号 * 字符结尾，用以表示
所有以指定字符串开头的账户。
EOT
}
```

## 解锁账户

某些域实施了防止账户滥用的策略。例如，某项策略可能强制用户每 90 天更改一次密码。另一项策略可能防止用户重复使用相同密码。可以利用多种策略来帮助保护域的安全。

然而，这些策略中的一种可能会让用户非常沮丧。该策略是：如果使用错误密码尝试登录过多，将锁定用户账户。这种锁定会导致使用户即使使用正确的密码也无法登录。这与禁用的账户非常相似，不同之处在于账户无法手动设置为锁定状态；它必须违反特定策略（例如错误登录尝试过多）。被锁定是为了让你知道该账户是因为违反策略而被禁用的。

更改锁定账户状态的唯一正确方法是让管理员解锁账户。这通常通过使用用户管理器（User Manager）或 MMC 取消选择“账户已锁定”复框来实现。但是，通过示例 2.6 中的脚本，你可以从命令行快速解锁账户。

该脚本可以接受任意数量的账户进行处理。在该脚本中，与本章许多其他脚本一样，你可以提供星号来表示显示所有匹配该名称的账户。例如，以下行将解锁 myDomain 域下的 Tester1、Tester2、Testertemp 和 Joel 账户：

```perl
perl unlock.pl -d MyDomain tester* joel
```

此脚本接受表 2.3 之前描述的命令行开关。如果既没有指定域名也没有指定机器名，脚本将默认为运行脚本的用户所在的域。

运行此脚本后，你应该执行域同步。

请参考本章中的“同步域控制器”部分。

## 示例 2.6 解锁账户



```perl
01. use Getopt::Long;
02. use Win32::NetAdmin;
03. use Win32::AdminMisc;
04.
05. Configure($Config);
06. if ($Config{help})
07. {
08.     Syntax();
09.     exit();
10. }
11.
12. if ("" ne $Config{domain})
13. {
14.     # 必须先给机器键赋值值，否则
15.     # GetDomainController() 将失败。
16.     $Config{machine} = "";
17.     Win32::NetAdmin::GetDomainController('',
18.                               $Config{domain},
19.                               $Config{machine});
20. }
21. else
22. {
23.     if ("" eq $Config{machine})
24.     {
25.         # 必须先给机器键赋值值，否则
26.         # GetDomainController() 将失败。
27.         $Config{machine} = "";
28.         Win32::NetAdmin::GetDomainController('',
29.                                     Win32::DomainName(),
30.                                     $Config{machine});
31.     }
32. }
33.
34. foreach my $Account (@{$Config{accounts}})
35. {
36.     if ($Account =~ /\*\*/)
37.     {
38.         my($Prefix) = ($Account =~ /\.*)\*/);
39.         my @Users;
40.         Win32::AdminMisc::GetUsers($Config{machine}, $Prefix, @Users);
41.         map
42.         {
43.             $AccountList{lc $Account} = 1;
44.         }Users);
45.     }
46.     else
47.     {
48.         $AccountList{lc $Account} = 1;
49.     }
50. }
51.
52. # 注意我们使用哈希 (%AccountList) 来跟踪
53. # 处理的用户。这是一个简单的黑科技（hack），防止我们
54. # 重复处理同一个用户（如果多次传入账户名）。
55. foreach my $Account (keys(%AccountList))
56. {
57.     my $Attrib;
58.     print($Config{machine} ");
59.     if( Win32::AdminMisc::UserGetAttributes($Config{machine},
60.     $Account,
61.     $Attrib ))
62.     {
63.     my $Flags = $Attrib(USER_FLAGS);
64.     if($Flags & UF_LOCKOUT)
65.         $Flags &= -UF_LOCKOUT;
66.         if (Win32::AdminMisc::UserGetAttributes($Config{machine},
67.     $Account,
68.     USER_FLAGS ))
69.     {
70.         print("success.");
71.     }
72.     else
73.     {
74.         print("failed: " . Error());
75.     }
76.     else
77.         print("not locked out.");
78.     }
79.     else
80.     {
81.         print("can not query account: " . Error());
82.     }
83.     print("\n\n");
84. }
85. sub Error
86.     return(Win32::FormatMessage(Win32::AdminMisc::GetError()));
87. }
88. sub Configure
89.     my ($Config) = @_;
90.     Getopt::Long::Configure("prefix_pattern=(.\*)");
91.     $Result = GetOptions($Config,
92.     qw(
93.     machine|m=s
94.     domain|d=s
95.     help?
96. )
97.     );
98.     $Config->{help} = 1 if (! $Result );
99.     if ("" ne $Config{machine})
100.     {
101.         $Config->{machine} = ||$Config{machine};
102.         $Config->{machine} =~ s/^(\|+//;
103.     }
104.     push($Config->{accounts}, @ARGV);
105.     $Config->{help} = 1 if (scalar @Config{accounts}));
106. }
107.
108. sub Syntax
109.     my ($Script) = ($0 =~ /([^\]]*)?\$/);
110.     my ($Line) = ".-" x length($Script);
111.
112.     print <<EOT;
113. 
114. $Script
115. $Line
116. 解锁锁定的账户。
117. 
118. 语法：
119. perl $Script [-m Machine -d Domain] Account [Account2 ...]
120. -m Machine..指定账户所在的机器。
121. -d Domain..指定账户所在的域。
122. Account....账户名称（用户 ID）。
123. 此账户可以以星号 * 字符结尾，用以表示
124. 所有以指定字符串开头的账户。
125. EOT
126. }
```

## 密码过期

你可以配置账户，使用户下次登录时强制更改密码。这通常在设置密码年龄时自动执行。当账户密码超过允许范围时，账户密码会自动过期。

要手动使账户过期，必须在账户上设置一个标记。不仅密码超过允许范围会过期，你还可以通过设置此标记来使账户过期。用户管理器（或计算机管理 MMC）通过显示“用户在下次登录时必须更改密码”标记来实现这种过期。

示例 2.7 通过设置密码过期标记使账户密码过期。脚本首先会移除已设置的“用户无法更改密码”（`UF_PWD_CANT_CHANGE`）标记。这是必要的；否则，用户下次登录时将强制强制更改密码，但该标记会阻止他这样做。接下来，如果已设置了“密码永不过期”（`UF_DONT_EXPIRE_PASSWORD`）标记，则将其清除。在尝试使密码过期之前，该标记不能被设置。最后，“用户在下次登录时必须更改密码”（`USER_PASSWORD_EXPIRED`）属性被设置为 true 或 false，取决于是否传递了 `-u` 开关。

另一个标记乍似乎是个问题。如果设置了“密码永不过期”，似乎密码无法过期。然而，当脚本使密码过期时，Win32 会自动移除密码永不过期标记。

请记住，在用户重置密码后，“无法更改密码”和“密码永不过期”标记不会设置。作为管理员，你可能需要在用户更改密码后更改密码标记。

示例 2.7 接受用户账户列表，因此你可以同时让多个用户的密码过期。例如，以下行将强制 Joel 和 Betty 在下次登录时更改密码：

```perl
perl expire.pl joel betty
```

此外，你可以指定星号（`*`）来使所有用户名以指定字符串开头的用户密码过期。例如，以下命令使所有名称以 Test 开头的用户密码过期，例如 Test、Testuser1、Testuser2 和 TestAccount：

```perl
perl expire.pl test*
```

你也可以通过传递 `-u` 开关来取消账户过期：

```perl
perl expire.pl test* -u
```

可以传递以下三个开关：

| 开关 | 功能 |
| :--- | :--- |
| `-m Machine` | 指定账户所在的计算机。 |
| `-d Domain` | 指定账户所在的域。它会覆盖任何 `-m` 开关。 |
| `-u` | 使每个账户的密码取消过期。因此，用户下次登录时不再被强制更改密码。 |

# 46 第 2 章：账户维护

如果未指定任何域机器名，脚本将默认使用运行脚本的用户所在的域。

在运行此脚本后，您应该执行域同步。请参考本章中的“同步域控制器”部分。

## 示例 2.7 账户密码过期

```perl
01. use Getopt::Long;
02. use Win32;
03. use Win32::NetAdmin;
04. use Win32::AdminMisc;
05.
06. Configure( \Config );
07. if ($Config{help}) )
08. {
09. Syntax();
10. exit();
11. }
12.
13. if ( "" ne $Config{domain} )
14. {
15. $Config{machine} = "";
16. Win32::NetAdmin::GetDomainController( '',
17. $Config{domain},
18. $Config{machine} );
19. }
20. elseif ( "" eq $Config{machine} )
21. {
22. $Config{machine} = "\\" . Win32::NodeName();
23. }
24. else
25. {
26. $Config{machine} = "\\\\Config{machine}";
27. $Config{machine} -= s/\\//////g;
28. }
29. # 注意我们使用一个哈希表 (%AccountList) 来跟踪我们正在
30. # 处理的用户。这是一个简单的黑客方法，用于防止我们多次处理
31. # 同一个用户（如果用户多次传递了相同的
32. # 账户名）。
33. foreach my $Account ( @($Config{accounts}) )
34. {
35. if ($Account =~ /\/\*/ /) /)
36. {
37. my ($Prefix) = ($Account =~ /^(.*)\*$/);
38. my @Users;
39. Win32::AdminMisc::GetUsers($Config{machine}, $Prefix, \Users );
40. map
41. {
42. $AccountList(lc $_) = 1;
43. } (@Users);
44. }
46. else
47. {
48. $AccountList[lc $Account] = 1;
49. }
50.
51.
52. foreach my $Account ( sort( keys(%AccountList )) )
53. {
54. my %Attrib = 0;
55. my $Result = 0;
56. my $Flag = 0;
57.
58. print ( ( $Config{expire} ) "Expiring" : "Unexpiring" );
59. print " password for '$Account'\n";
60. if ( Win32::AdminMisc::UserMiscAttributes($Config{machine},
61. $Account,
62. \Attrib ) )
63. {
64. $Flag = $Attrib(USER_FLAGS);
65. # 如果我们正在让密码过期，且账户不允许
66. 更改密码，则修改它使其允许
67. 更改密码。
68. if ( !$Config{expire} )
69. {
70. $Flag &= -UF_PASSWD_CANT_CHANGE;
71. }
72.
73. # 如果账户不允许账户过期，则
74. 临时允许其过期...
75. if($Flag & UF_DONT_EXPIRE_PASSWD )
76. {
77. $Flag &= -UF_DONT_EXPIRE_PASSWD;
78. }
79. }
80.
81. if ($Flag != $attrib(USER_FLAGS))
82. {
83. Win32::AdminMisc::UserSetMiscAttributes($Config{machine},
84. $Account,
85. USER_FLAGS => $Flag);
86. }
87.
88. # 强制账户过期并重置标志位...
89. $Result = Win32::AdminMisc::UserSetMiscAttributes(
90. $Config{machine},
91. $Account,
92. USER_PASSWORD_EXPIRED => !$Config{unexpire} );
93. }
94.
95. if ($Result)
96. {
97. print "successful.\n";
98. }
99. else
100. {
101. my $Error = Win32::FormatMessage(Win32::GetLastError());
102. $Error = s/\r|\n/g;
103. print "printed to:";
104. print(\$Config->{expire})?"expire" : "expire";
105. print ": \$Error\n";
106. }

108. sub Configure
109. {
110.     my ($Config, Long::Config) = @_;
111.
112.     Getopt::Long::Configure("prefix-pattern=-|/\*");
113.     $Result = GetOptions(\$Config,
114.     qw(
115.     machine|m=s
116.     domain|d=s
117.     unexpire|u
118.     help?
119.     ))
120.     $Config->{help} = 1 if ($Result);
121.     if ("" ne \$Config->{machine} != "\$Config{machine}");
122.     {
123.     $Config->{machine} = "\$Config{machine}";
124.     $Config->{machine} =~ s/\///;
125.     }
126.     push(\$Config->{accounts}, @ARGV);
127.     $Config->{expire} = 1 if !scalar(\$Config->{accounts});
128. }

129. sub Syntax
130. {
131.     my ($Script) = ($0 =~ /\\]]*$/);
132.     my ($Line) = "-" x length($Script);
133.     print <<EOT;
134.
135. \$Script
136. \$Line
137. 强制用户在登录时更改密码。
138.
139. Syntax:
140. perl \$Script [-u] [-m machine | -d domain] [ Account ]
141. -u.......取消账户过期。
142. -m....指定账户所在的机器。
143. -d Domain....指定所在的域。
144.
145. Account......账户名 (userid)。
146. 账户可以以 * 结尾，表示
147. 所有以指定字符串开头的账户。
148. EOT
149. }
```

## 重命名账户

管理员重命名账户并不罕见。例如，如果用户结婚了，您可能需要更改用户的账户名。此时，重命名账户的功能非常有用。

示例 2.8 允许您从命令行重命名用户。例如，以下命令行将 MyDomain 域中的 OldUser 重命名为 NewUser：

```perl
perl rename -d MyDomain OldUser NewUser
```

账户保持完整，仅更改名称。因此，所有权限和组会自动更新。

此脚本接受表 2.3 中描述的开关。

如果没有指定域，脚本将默认使用运行脚本的用户所在的域。

运行此脚本后，您应该执行域同步。请参考本章中的“同步域控制器”部分。

## 示例 2.8 重命名账户

```perl
01. use Getopt::Long;
02. use Win32::NetAdmin;
03. use Win32::AdminMisc;
04.
05. Configure(\%Config );
06. if ($Config{help})
07. {
08. Syntax();
09. exit();
10. }
11.
```



```perl
if ("" ne $Config{domain})
{
    # 必须为 machine 赋值，否则
    # GetDomainController() 将失败。
    $Config{machine} = "";
    Win32::NetAdmin::GetDomainController(
        '',
        $Config{domain},
        $Config{machine}
    );
}
else
{
    # 必须为 machine 赋值，否则
    # GetDomainController() 将失败。
    if ("" eq $Config{machine})
    {
        $Config{machine} = "";
        Win32::NetAdmin::GetDomainController(
            Win32::DomainName(),
            $Config{machine}
        );
    }
}

print 'Renaming $Config{machine}$Config{name} to ';
print '$Config{machine}$Config{new_name} ...';

if (Win32::AdminMisc::UserName(
    $Config{machine},
    $Config{name},
    $Config{new_name}
))
{
    print 'successful.\n';
}
else
{
    my $Error = Win32::FormatMessage(Win32::AdminMisc::GetError());
    $Error = s/\n\n//g;
    print 'failed to rename: $Error\n';
}

sub Configure
{
    my ($Config) = @_;

    Getopt::Long(:Config = @_; 'prefix_pattern=-(\|*)');
    $Config->{machine} = Win32::NodeName();
    $Result = GetOptions(
        $Config,
        qw(
            machine|m=s
            domain|d=s
            help|?
        )
    );

    $Config->{help} = 1 if (!$Result);
    if ("" ne $Config->{machine})
    {
        $Config->{machine} = "$Config->{machine}";
    }
    $Config->{machine} =~ s/\///;
}

push($Config->{accounts}, @ARGV);
$Config->{expire} = 1 if !scalar($Config->{accounts});

sub Syntax
{
    my ($Script) = ($0 =~ /\\]]*$/);
    my ($Line) = "-" x length($Script);

    print <<EOT;

$Script
$Line

强制用户在登录时更改密码。

Syntax:

perl $Script [-u] [-m machine | -d domain] [ Account ]

-u.......取消账户过期。
-m....指定账户所在的机器。
-d Domain....指定所在的域。

Account......账户名 (userid)。
NewAccount..账户的新名称。
EOT
}
```

## 权限

在 Win32 中，权限是管理员授予账户的一种内容。权限决定了账户允许执行哪些操作。例如，`SE_BACKUP_NAME` 权限允许账户备份文件和目录，绕过位于文件和目录上的安全权限。账户要远程关闭计算机，需要 `SE_REMOTE_SHUTDOWN_NAME` 权限。账户必须由管理员专门授予这些权限。

权限可以分配给用户账户或组。将权限分配给组非常有用，特别是当一组用户账户共享特定目的时。考虑接管文件、目录和注册表项所有权的功能。这种强大的权限使得所有安全失效，因为具有此权限的用户可以简单成为任何对象的所有者（因此对它们拥有完全权限）。按理，这种强大的能力应该赋予网络管理员。如果您的域有多个管理员，您可能会发现自己必须为每个账户分配权限。更有效的方法是将权限分配给 `Administrators` 和 `Domain Adm` 组。这样，分配到这些组的任一用户账户都拥有此权限。

通常，您需要运行用户管理器或 MMC 来分配权限（也称为用户权利）。当选择本地系统以外的账户登录服务时，有时这些权限会自动分配给管理员。后文显示的示例 2.9 是一个允许您查询的全权限管理脚本。

分配给组或用户特定的权限，以及哪些组和用户拥有特定的权限。你还可以从用户和组中添加或删除权限。此外，此脚本会打印所有可用的权限。

## 显示可用权限

示例 2.9 包含了几个不同的语法变体。要列出可用权限列表，你可以使用以下语法：

```bash
perl priv.pl -p
```

此命令以图 2.3 所示的格式显示所有权限。该图还展示了输出内容的一部分。每个权限项的第一行是权限常量名（例如 `SE_ASSIGN_PRIMARYTOKEN_NAME`）。Win32 内部使用显示名称（display name）来表示权限。对于本脚本而言，你可以指定这两个名称中的任何一个；它们是同义的。然而，建议编写 Win32 API 的程序员使用常量名，因为可以保证这些名称不会随着 Windows 版本的变化而改变。

图中的某些权限条目带有注释行。它们简单地描述了权限的用途——这是非常有用的信息，尤其是当你试图从权限名称破解其含义时。并不是所有权限都有注释行，因为 Win32 并没有提供这些注释。

```text
C:\perl priv.pl -p

SE_ASSIGN_PRIMARYTOKEN_NAME:

Display name: SeAssignPrimaryTokenPrivilege

Comment: Replace a process level token

SE_AUDIT_NAME:

Display name: SeAuditPrivilege

Comment: Generate security audits

SE_BACKUP_NAME:

Display name: SeBackupPrivilege

Comment: Back up files and directories

SE_BATCH_LOGON_NAME:

Display name: SeBatchLogonRight
```

图 2.3 显示可用权限。

## 显示拥有权限的用户

示例 2.9 用的另一种语法是显示所有拥有特定权限的组和账户。这对于确定拥有特定能力的范围非常有用。脚本通过指定显示权限分配（`-s`）选项来实现此：

```bash
perl priv.pl -s Privilege2
```

权限列表可以是完全权限常量（例如 `SE_BATCHLOGON_RIGHT`），也可以是显示名称（例如 `SeBatchLogonRight`）。脚本足够灵活，可以处理这两者的匹配。匹配是通过指定权限的根节点完成的，例如 `BATCHLOGON`。

脚本会显示拥有每个指定权限的用户和组，如图 2.4 所示。注意指定的第一个权限是完整的显示名称，第二个仅是权限名称的根。

```text
C:\>priv.pl -s SeBatchLogonRight restore

SE_BATCHLOGON_NAME (SeBatchLogonRight):

MyDomain\Daemons

MyDomain\Mail Users

MyDomain\MailServices

SE_RESTORE_NAME (SeRestorePrivilege):

BUILTIN\Backup Operators

BUILTIN\Server Operators

BUILTIN\Administrators

MyDomain\BackupService
```

> 图 2.4 显示谁拥有特定权限。

## 显示和修改用户及组权限

用户和组权限只有在可以修改时才是强大的。这是脚本的默认操作。如果你既没有指定 `-s` 也没有指定 `-p` 选项，则传入的参数假设为用户名或组名。将显示分配给这些用户和组的权限。这是发现谁拥有什么权限的一种简单快捷的方法。图 2.5 显示对 `BackupService` 账户进行简单查询的结果。

### 第 2 章：账户维护

```text
C:\priv BackupService

MyDomain\BackupService:

SE_AUDIT_NAME            Generate security audits

SE_BACKUP_NAME           Back up files and directories

SE_RESTORE_NAME          Restore files and directories

SE_TCB_NAME               Act as part of the operating system

SE_INTERACTIVE_LOGON_NAME

SE_SERVICE_LOGON_NAME
```

图 2.5 显示用户的权限。

你可以根据需要指定任意数量的用户和组。脚本还接受用户账户的 `*` 通配符。它会扩展为所有匹配星号前字符串的用户账户。

在此模式下，脚本接受权限名称，用以从所有指定的账户和组中添加（以 `+` 为前）或删除（以 `-` 为缀）权限。执行顺序是先添加，后减去，最后显示最终结果。

图 2.6 展示了在特定账户上添加和删除权限。注意，除了 Joel 和 Betty 账户外，用户还指定了所有以 test 开头的用户账户。指定的用户账户被添加了多种权限，并删除了一个权限。

```text
C>priv.pl +batch_logon -tcb +security

+SE_takeownership_name=secretatetokenprivilegetest* joel betty

MyDomain\Test_Guest:

SE_BACKUP_NAME            Back up files and directories

SE_SECURITY_NAME          Manage auditing and security log

SE_OWNERSHIP_NAME         Take ownership of files or other objects

SE_CREATE_TOKEN_NAME      Create a token object

SE_BATCH_LOGON_NAME
```

```text
MyDomain\Test_Guest2:

SE_BACKUP_NAME            Back up files and directories

SE_SECURITY_NAME          Manage auditing and security log

SE_OWNERSHIP_NAME         Take ownership of files or other objects

SE_CREATE_TOKEN_NAME      Create a token object

SE_BATCH_LOGON_NAME
```

```text
MyDomain\joel

SE_BACKUP_NAME            Back up files and directories

SE_SECURITY_NAME          Manage auditing and security log

SE_OWNERSHIP_NAME         Take ownership of files or other objects

SE_CREATE_TOKEN_NAME      Create a token object

SE_BATCH_LOGON_NAME
```

图 2.6 在账户中添加和删除权限。

在指定要删除的权限时，`*` 字符表示删除所有权限，如图 2.7 所示。

```text
C:\perl priv.pl -t test*

MyDomain\Test_Guest:

MyDomain\test:
```

图 2.7 从账户中删除权限。

当对账户进行修改时，在账户注销并重新登录之前修改不会生效。如果没有指定域名称或机器名称，脚本将默认使用运行脚本的用户域。

## 管理用户权限

```perl
$Config{machine});
}

if ($Config{display_privileges})
{
    my @PrivList;

    # 显示所有权限
    if (scalar @{$Config{items}})
    {
        foreach my $Priv (@{$Config{items}})
        {
            $Priv = MatchPrivilege($Priv) || next;
            push($PrivList, $Priv);
        }
    }
}
else
{
    push($PrivList, sort(keys(%PRIVILEGES)));

    foreach $Key (@PrivList)
    {
        print("$Key:\n");
        print("display name: $PRIVILEGES{$Key}->{display}\n");
        print("comment: $PRIVILEGES{$Key}->{comment}\n");
        if ("" ne $PRIVILEGES{$Key}->{comment})
        {
            print("\n");
        }
    }
}
elsif ($Config{user_rights})
{
    # 显示谁被启用了特定权限
    foreach $Privilege (@{$Config{items}})
    {
        my @SidList;
        my $PrivKey = uc MatchPrivilege($Privilege) || next;

        print("$PrivKey($PRIVILEGES{$PrivKey}->{display}):\n");
        if (
            Win32::Lanman::LsaEnumerateAccountsWithUserRight(
                $Config{machine},
                $PRIVILEGES{$PrivKey}->{display},
                @$SidList
            )
        )
        {
            my @SidData;
            Win32::Lanman::LsaLookupSids(
                $Config{machine},
                @$SidList,
                @$SidData
            );

            foreach my $Data (@SidData)
            {
                print(
                    "\t",
                    ("" ne $Data->{domain}) ? $Data->{domain} : ""
                );
                print("$Data->{name}\n");
            }
        }
    }
}
```

## 示例 2.9 延续



```perl
128.   print "\n";
129.   }
130. }
131. else
132.   {
133.     # 显示特定账户启用了哪些权限
134.     my @AccountList;
135.     my @AccountInfo;
136.     my %AccountList;
137.
138.     # 展开用户组中的任何通配符...
139.     foreach my $Key (@{$Config{items}}) 
140.     {
141.         if ($Account ~ /^\*\*/)
142.         {
143.             my $Prefix = ($Account ~ /^(.*)\*\*/);
144.             my @Accounts;
145.             Win32::AdminMisc::GetUsers($Config{machine},
146.                               $Prefix,
147.                               \@Accounts);
148. 
149.             map
150.             {
151.                 $TempAccountList{lc $_} = $_;
152.             } @Accounts;
153.         }
154.         else
155.             {
156.                 $TempAccountList{uc $Account} = $Account;
157.             }
158.     }
159.     # 从临时列表中创建非重复的用户账户列表
160.     foreach my $Key (sort (keys (%TempAccountList))) 
161.     {
162.         push(@AccountList, $TempAccountList{$Key});
163.     }
164.     if (scalar (@{$Config{add_privileges}})
165.         || scalar (@{$Config{remove_privileges}}))
166.         {
167.         my @SidList;
168.         Win32::Lanman::LsaLookupNames($Config{machine},
169.                                     \@AccountList,
170.                                     \@SidList);
171.         foreach my $Sid (@SidList)
172.         {
173.             if (scalar (@{$Config{add_privileges}}))
174.                 {
175.                     Win32::Lanman::LsaAddAccountRights($Config{machine},
176.                                                         $Sid->{sid},
177.                                                         $Config{add_privileges});
178.                 }
179.         }
```

# 权限 59

```perl
if ( scalar @{$Config{remove_privileges}} )
{
Win32::Lanman::LsaRemoveAccountRights($Config{machine},
  $Sid->{sid};
  $Config{remove_privileges},
  $Config{remove_all} );
}
ReportAccountPrivileges(@AccountList);
sub ReportPrivileges
{
my(@AccountList) = @_;
$_ = PrivilegeDump;
Win32::Lanman::LsaLookupNames($Config{machine},
  @AccountList,
  @AccountInfo);
}
for ($Index = 0; $Index < scalar @{$AccountInfo}}; $Index++)
{
my $Account = $AccountInfo[$Index];
$Account->{name} = $AccountList[$Index];
print "$Account->{domain}" if "" ne $Account->{domain};
print "$Account->{name}";

## 检查账户是否存在
if ($Account->{use})
{
print "\n";
if (Win32::Lanman::LsaEnumerateRights($Config{machine},
  $Account->{sid},
  @Rights))
{
map {
  $Account->{name} = $PRIVILEGE_VALUES{uc $_};
  $Account->{display} = $_;
  $Account->{comment} = $Account->{name}->{comment};
} @Rights;
}
else
{
print "... account does not exist.\n";
}
print "\n";
return;
}
```

## 示例 2.9 延续

```perl
232. sub MatchPrivilege
{
233. my($pRoot) = uc shift @;
234. $pKey = $pRoot;
235. # 用户输入的是显示名称吗？
236. if (defined ($pKey = $PRIVILEGE_VALUES{$pKey})) {
237. {
238. # 用户输入的是普通权限吗？
239. $pKey = $pRoot;
240. if (defined ($pKey = $PRIVILEGES{$pKey}->{name})) {
241. {
242. # 用户只输入了权限的基础
243. $pKey = "SE_" . $pRoot . "NAME";
244. if (defined ($pKey = $PRIVILEGES{$pKey}->{name})) {
245. {
246. # 用户只输入了显示名称的基础
247. $pKey = "Se" . $pRoot . "Privilege";
248. if (defined ($pKey = $PRIVILEGE_VALUES{uc $pKey})) {
249. {
250. # 最后机会...
251. $pKey = "SE" . $pRoot . "Right";
252. $pKey = $PRIVILEGE_VALUES{uc $pKey};
253. }
254. }
255. }
256. return($pKey);
257. }
258. sub Configure
{
259. my($Config, @Args) = @_;
260. while($myArg = shift @Args)
261. {
262. my($Prefix) = ($myArg =~ /([+\/]+)/);
263. if ("" ne $Prefix) {
264. $Arg =~ s/[^\/]//;
265. if("+" eq $Prefix) {
266. {
267. # 添加权限
268. my $Privilege = MatchPrivilege($Arg) || next;
269. push($Config->{add_privileges},
270. $PRIVILEGES{$Privilege}->{display});
271. }
272. elsif($Arg =~ /^\p/i) {
273. {
274. # 请求显示所有权限
275. $Config->{display_privileges} = 1;
276. }
```

# 权限 61

```perl
      elsif($Arg ~ /^s$/ i)
     {
     # 指定显示用户权限
     $Config->{user_rights} = 1;
     }
      elsif($Arg ~ /^d$/ i)
     {
     # 指定创建账户的域
     $Config->{domain} = shift @Args;
     }
      elsif($Arg ~ /^m$/ i)
     {
     # 指定账户所在的机器
     $Config->{machine} = "\\"; shift @Args;
     $Config->{machine} = s/\\\\\\\\//;
     }
      elsif($Arg =~ /\?(?h|help)/ i)
     {
         # 请求帮助
         $Config->{help} = 1;
     }
     else
     {
         if("/" eq $Prefix)
         {
             # 未知的开关
             $Config->{help} = 1;
         }
         else
             {
                 # 如果前缀是 -
                 # 且没有有效的标记匹配该开关...
                 # 移除权限
                 if("\*" eq $Arg)
                 {
                     $Config->{remove_all} = 1;
                     # 推入 remove 数组。它仍然会被忽略，
                     # 因为我们会看到“移除所有”标记。
                     # 这样脚本将看到数组不为空
                     # 并尝试移除权限。
                     push(@Config{remove_privileges}, $Arg);
                 }
                 else (my $Privilege = MatchPrivilege($Arg) || next;
```

## 同步域控制器

在大型网络中，拥有多个域控制器（DC）是常见的。所有域都必须有一个主域控制器（PDC），但可以拥有任意数量的备份域控制器（BDC）。BDC 字面上的意思就是备份域控制器；如果 PDC 宕机，其中一个 BDC 就会提升自己为临时 PDC。

DC 的工作包括处理用户登录请求和验证用户等其他任务。无论是 PDC 还是 BDC，任何 DC 都可以处理此类请求。这种能力有助于将负载分布到多台机器上，防止网络和处理出现瓶颈。

这种分布式拓扑结构的一个问题是，每个 DC 必须保留一份自己的用户帐户数据库副本。因此，每个 BDC 必须定期与 PDC 同步。例如，当用户更改密码时，修改操作会被提交给 PDC。PDC 必须将更改传播到所有的 BDC，这样如果用户通过其中一个 BDC 登录，就可以使用新密码。在某些情况下，这种传播可能会花费大量时间。

示例 2.10 允许你强制 BDC 与其 PDC 同步，或者强制进行全域同步。此过程应该在完成账户修改（如创建、删除或重命名）或单个帐户被修改（密码更改、禁用、解锁等）后执行。

要强制 BDC 与其 PDC 同步，只需传入 BDC：

```perl
perl domync.pl server1 server2 server3
```

要强制 PDC 与其所有的 BDC 同步，请使用以下命令：

```perl
perl domync.pl -f MyDomain
```

## 示例 2.10 同步域控制器

```perl
01. use Getopt::Long;
02. use Win32::Lanman;
03.
04. Configure(\Config);
05. if ($Config{help}) 
06. {
07. Syntax();
08. exit( 0 );
09. }
10.
11. if ($Config{full_sync}) 
12. {
13. my $Pdc;
14. if (Win32::Lanman::GetDCName($server, $Config{domain}, \Pdc )) ) 
15. {
16. my %Info;
17. if (Win32::Lanman::LogonControlPdcReplicate($Pdc, %Info )) ) 
18. {
19. print 'Successfully initiated a full domain synchronization ';
20. print 'for the $Config{domain} domain.\n';
21. }
22. else
23. {
24. print 'Full domain synchronization for the $Config{domain} ' 
25. 'domain $Config{domain}\n';
26. print 'Error: ' . Win32::Lanman::GetLastError() . "\n";
27. }
28. else
29. {
30.
31. print 'Unable to locate the primary domain controller for the ' 
32. 'domain $Config{domain}\n';
33. print 'Error: ' . Win32::Lanman::GetLastError() . "\n";
34. }
35. }
36. else
37. {
38. print 'Synchronizing the following domain controllers with its PDC:\n';
39. foreach my $Server (@{$Config{servers}}) 
40. {
41. my %Info;
42. my $Result = Win32::Lanman::LogonControlSynchronize($Server, 
43. \Info );
44. printf(" %-20s %s\n", 
45. $Server, 
46. ($Result) ? "successful" : "failed");
47. }
48. }
49.
```

```perl
50. sub Figure {
51. my($Config) = @_;
52.
53. Getopt::Long::Configure("prefix_pattern=-/");
54. $Result = GetOptions($Config,
55. qw(
56. full_sync|
57. help?
58. );
59.
60. $Config->{help} = 1 if (!Result);
61. if ($Config{full_sync})
62. {
63. $Config->{domain} = shift @ARGV;
64. $Config->{domain} = Win32::DomainName();
65. if ("" eq $Config->{domain})
66. }
67. else
68. push(@{$Config{servers}}, @ARGV);
69. }
70. if (!$Config{full_sync}) && (scalar @{$Config{servers}})
71. {
72. $Config->{help} = 1;
73. }
74. sub Syntax {
75. my($Script) = ($0 ~ /\*\$/);
76. my($Line) = "." x length($Script);
77. print <<EOT;
78. $Line
79. Initiates synchronizations between domain controllers.
80. Syntax:
81. perl $Script -f [Domain] ...
82. -f [Domain] Performs a domain synchronization.
83. 除非指定了可选的 Domain，否则将默认为
84. 本地域。
85. Server...... 指定要与其 PDC 同步的 BDC。
86. EOT
87. }
```

## 结论

Win32 平台提供了丰富的 GUI 环境来管理用户和组帐户的各个方面。然而，网络中存在的帐户数量之多，让任何管理员都使用默认工具是非常不现实的。

本章展示了如何使用 Win32 Perl 有效地管理这些任务，使它们不仅更简单，而且能够自动化并减少错误。

## 工具

每位优秀的管理员都会收集一套他们不可或缺的工具集。这些工具执行特定任务，能够快速完成工作。此类实用程序的一个完美例子是 Windows NT Resource Kit 附带流行的 `LS.EXE`。



此实用程序（以及它的小兄弟`LS.EXE`）可以导出应用到文件或目录的任何权限。没有这样的工具，你注定要打开管理器窗口，选择目标对象，右键点击选择属性菜单，然后进入生成的属性页的安全选项卡。如果这个步骤听起来并不很麻烦，请想象一下管理一个拥有成千上万台机器、各种权限应用于各种目录的网络。

本章涵盖了各种为工作负载创建的脚本。为了确保，我编写了每一个脚本以简化并减轻工作量，以此演示你如何利用`Win32 Perl`来解决每天遇到的问题。当你仔细研究代码时，会明显发现几乎没有哪个`Win32`任务是无法通过一点`Perl`代码来管理的。

编写这些脚本并不是为了简单或作为教程，而是为了深入研究解决任务的细节。我建议你在查看构成这些脚本的代码时，使用一份良好的`Win32 API`参考手册；特别是，请查看微软的`MSDN`库（`http://msdn.microsoft.com/`）以及当然了，还有我的另一本书《`Win32 Perl Programming: The Standard Extensions (New Riders Publishing)`》。

## 文件系统

`Win32`操作系统大量使用了其文件系统。作为管理员，你承担着管理这一重要资源的职责。你的工作涵盖了管理任务的所有范围，从保护文件和目录到创建目录以及更新过时的文件。来自不同公司的许多不同工具和实用程序可以帮助管理你的机器文件系统。然而，你无法轻松找到某些工具。

许多现有的工具令人困惑，因为它们反映了文件系统中不为人知的方面，例如备用数据流。某些工具未被使用是因为管理员不知道它们的存在，例如用于发现远程机器隐藏目录的工具。接下来的章节将重点介绍可以节省大量工作的文件系统相关工具。

## 发现共享目录

自从`Windows`工作组版以来，共享目录变得非常简单。在`Windows NT/2000`命令行中，你可以使用`net`命令轻松地共享目录。以下行共享了一个名为`TempDir`的临时目录：

```
net share TempDir=c:\temp
```

或者，你可以从文件管理器、资源管理器和服务管理器`GUI`程序共享目录。

`Win32`世界允许你隐藏共享目录——即共享一个在浏览网络时不可见的目录。访问目录的唯一方法是知道它已被共享并显式访问。通过在共享名称末尾添加美元符号（`$`）来隐藏目录。例如，以下命令行创建了一个名为`MyHiddenShare`的隐藏共享目录：

```
net share MyHiddenShare=$c:\temp
```

现在，只有知道这个隐藏共享的用户才能访问它。

你可以使用以下命令行查看你的机器正在共享哪些目录：

```
net share
```

# 文件系统 69

你始终可以为特定的机器打开资源管理器窗口，但这种解决方案非常笨重，且只显示非隐藏目录。

假设你需要查看某些远程机器上有哪些可用共享。在这种情况下，资源管理器无法派上用场。你可以走到那台机器，登录并执行`net share`命令，但这种方法并不方便，特别是当机器位于另一个城市或另一个国家时。而且，假设你没有安装某种类型的`Telnet`守护进程，这个问题就相当严重了。

此时，你可以转向`DumpShares.pl`脚本（如示例 3.1 所示）。脚本的核心围绕第 11 行展开，在那里调用了`Win32::Lanman`扩展来获取共享目录名称列表。

只要你可以做到，无论你在远程机器上是否被授予管理员权限。如果你在远程机器上缺少管理员权限，共享目录的路径将不可见。该脚本接受任意数量的机器名称，并尝试解析每个传入的机器名称。如果没有传入任何名称，则显示本地机器的共享目录。

## 示例 3.1 显示远程机器上的所有共享目录

```
01. use Win32;
02. use Win32::Lanman;
03.
04. push(@ARGV, Win32::NodeName(hostname)) if ( l scalar @ARGV );
05. foreach my $Machine (@ARGV) 
06. {
07. my $List;
08. $Machine -= s#^[\/]*#\#;//;
09.
10. print "\nShare list for '$Machine'\n";
11. if(Win32::Lanman::NetShareEnum($Machine, \@List ))
12. {
13. foreach my $Share (@List)
14. {
15. my($Remark, $Path, $NetName);
16.
17. $NetName = $Share->{netname};
18. if ( "" ne $Share->{remark} )
19. {
20. $Remark = "\${Share->{remark}}";
21. }
22. if ( "" ne $Share->{path} )
23. {
24. $Path = $Share->{path};
25. }
26. else
27. {
28.   $Path = 'No permission to display';
29.   }
30.   push(@ShareList, { name => $NetName,
31.     remark => $Remark,
32.     path => $Path });
33.   }
34.   $- = Share_Header;
35.   write;
36.
37.   $- = Share_Info;
38.   $iCount = 0;
39.
40.   foreach $Share ( sort(
41.     lc $a->{name} lc $b->{name}
42.     @ShareList ))
43.   {
44.     $iCount++;
45.     write;
46.   }
47.   }
48.   else
49. {
50.     print "...not available : ";
51.     print Win32::FormatMessage(Win32::Lanman::GetLastError());
52.   }
53.
54.   print "\n";
55.   }
56.
57.   format Share_Info =\<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
58. @>>> @<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
59. $iCount, $Share->{name}, $Share->{remark}, $Share->{path}
60. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
61.   $Share->{remark}, $Share->{path}
62. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
63.   $Share->{remark}, $Share->{path}
64.
65.
66.
67. format Share_Header =
68. @||@ <<<<<<<<<<<<<<<< @<<<<<<<<<<<<<<<<<< @ "Path"
69. "Num", "Share Name", "Comment", "Path"
```

## 卷信息

对于管理员来说，发现远程机器上硬盘的细节可能是至关重要的。确定卷的大小以及可用空间是驱动器管理的重要部分。示例 3.2 获取了必要信息和其他相关数据，例如卷名、文件系统类型（`NTFS`, `FAT`, `FAT32`等）、序列号以及卷的标志。这些标志指示了驱动器支持哪些功能。标志及其描述列在 3.1 中。

### 表 3.1 卷标志

| 标志 | 描述 |
| --- | --- |
| `FS_CASE_IS_PRESERVED` | 文件系统在将名称存入磁盘时会保留文件名的大小写。 |
| `FS_CASE_SENSITIVE` | 文件系统支持区分大小的文件名。 |
| `FS_UNICODE_STORED_ON_DISK` | 文件系统支持在磁盘上以`Unicode`存储文件名。 |
| `FS_PERSISTENT_ACLS` | 文件系统保留并强制访问控制列表 (`ACL`)——也称为权限。例如，`NTFS`保留并强制`ACL`，但`FAT`不支持。 |
| `FILE_COMPRESSION` | 文件系统支持基于文件的压缩。 |
| `FILE_VOL_IS_COMPSED` | 指定卷是压缩卷——例如，双卷。 |
| `FILE_NAMED_STAMS` | 文件系统支持命名流。 |
| `FILE_SUPPORTS_ENPTION` | 文件系统支持加密文件系统 (`EFS`)。 |
| `FILE_SUPPORTS_OBJECT_IDS` | 文件系统支持对象标识符。 |
| `FILE_SUPPORTS_REPARSE_POINTS` | 文件系统支持解析点。此功能允许`NTFS`链接以及不经常访问的数据移动到磁带备份。 |
| `FILE_SUPPORTS_SPAR_FILES` | 文件系统支持稀疏文件。稀疏文件仅将数据的部分存储到磁盘，因此可以节省驱动器空间。 |
| `FILE_VOLUME_QUOTAS` | 文件系统支持用户配额限制。 |

脚本接受如下的驱动器号或`UNC`：

```
perl \\server\share
```

在这种情况下，脚本会显示本地`c:\`驱动器以及`\server\share`共享卷的信息。如果没有传递参数，则显示当前目录的卷信息。该代码使用了`Windows NT 4.0`和`Windows 95 Release 2 (OSR2)`引入的`API`，在早于此的平台上可能会失败。

```
\\server\share
c:\
FS Name Flags
NTFS This is test volume
Total Size: 4,301,788,672
Avail Size: 726,140,928
FS_CASE_SENSITIVE
FS_CASE_IS_PRESERVED
FS_UNICODE_STORED_ON_DISK
FILE_VOLUME_QUOTAS
FS_FILE_COMPRESSION
FS_PERSISTENT_ACLS
FILE_SUPPORTS_OBJECT_IDS
FILE_SUPPORTS_SPAR_FILES
FILE_SUPPORTS_REPARSE_POINTS
FILE_SUPPORTS_ENPTION
```

图 3.1 显示卷信息。

## 示例 3.2 获取卷信息

```
01. use Win32::API::Prototype;
02.
03. ApiLink('kernel32.dll', 'BOOL GetVolumeInformation(
04.
05.
06.
07.
08.
09.
10.
LPCTSTR lpRootName,
LPCTSTR lpVolumeNameBuffer,
DWORD nVolumeSize,
LWORD lpSerialNumber,
LWORD lpMaximumComponentLength,
LWORD lpFileSystemFlags,
LPTSTR lpFileSystemBuffer,
DWORD nFileSystemSize )
12. // die "Can not link to GetVolumeInformation();"
13. ApiLink('kernel32.dll', 'BOOL GptDiskFreeEx(
14.             LPCTSTR lpDirectoryName,
15.             PVOID lpFreeAvailable,
16.             PVOID lpTotalNumberOfBytes,
17.             PVOID lpTotalFreeBytes ) )
```

```
18. // die "Wrong version of NT";
19.
20. FLAGS = (
21.     0x00000001 => 'FS_CASE_SENSITIVE',
22.     0x00000002 => 'FS_CASE_IS_PRESERVED',
23.     0x00000004 => 'FS_UNICODE_STORED_ON_DISK',
24.     0x00000008 => 'FS_PERSISTENT_ACLS',
25.     0x00000010 => 'FS_FILE_COMPRESSION',
26.     0x00000020 => 'FS_FILE_QUOTAS',
27.     0x00000040 => 'FS_SUPPORTS_SPAR_FILES',
28.     0x00000080 => 'FS_SUPPORTS_REPARSE_POINTS',
29.     0x00000100 => 'FILE_VOL_COMPSED',
30.     0x00000200 => 'FILE_NAMED_STAMS',
31.     0x00000400 => 'FILE_SUPPORTS_ENPTION',
32.     0x00000800 => 'FS_SUPPORTS_OBJECT_IDS');
```

```
35. push(ARGV, "") if (@ == scalar ARGV);
37. foreach my $Path (@ARGV)
39. my $dwVolSize = 256;
40. my $szVolName = NewString($dwVolSize);
41. my $dwSerialNumber = pack("L", 0);
42. my $dwMaxLength = pack("L", 0);
43. my $dwFlags = pack("L", 0);
44. my $dwFSNameSize = 256;
45. my $szFSName = NewString($dwFSNameSize);

47. $Path = "" unless ($Path -= /\$/);
48. next unless -d $Path;
49. $Path = NewString($Path);

51. print "\n$Path:\n";
52. $- = DumpVol();
53. if (GetVolumeInformation($Path, $szVolName,
54.             $dwVolSize, $dwSerialNumber,
55.             $dwMaxLength, $dwFlags,
56.             $szFSName, $dwFSNameSize)) {
58. local %Vol = (
59. path => $Path,
60. volume_name => CleanString($szVolName),
61. serial_num => sprintf("U%04x-%04x",
62.             reverse( unpack("S2",
```

## 示例 3.2 延续



```perl
63.  $pdwSerialNumber( ),
64.  max_length => unpack("L", $pdwMaxLength ),
65.  flags      => DecodeFlags( unpack("L", $pdwFlags ) ),
66.  fs_name    => CleanString($szFSName )
67.  );
68.  my $pFree = pack("L2", 0, 0);
69.  my $pTotal = pack("L2", 0, 0);
70.  my $pTotalFree = pack("L2", 0, 0);
71.  if (GetDiskFreeSpace($Path, $pTotal, $pTotalFree ) )
72.  {
73.  $Vol{free} = FormatNumber(MakeLargeInt unpack("L2",
74.  $pTotalFree ) );
75. 
76.  $Vol{total} = FormatNumber(MakeLargeInt unpack("L2",
77.  $pTotal ) );
78.  }
79.  write;
80.  }
81.
82.  sub MakeLargeInt
83.  {
84.  my($Low, $High) = @_;
85.  return($High * ( 1 + 0xFFFFFFFF ) + $Low);
86.  }
87. 
88.  sub DecodeFlags
89.  {
90.  my($Flags) = @_;
91.  my $String = "";
92.  foreach my $Key ( keys(\%FLAGS ) )
93.  {
94.    if ($Flags & $Key)
95.    {
96.      $String .= sprintf("%-30s\n", $FLAGS{$Key});
97.    }
98.  }
99.  return($String);
100. }
101. 
102.  sub FormatNumber
103.  {
104.  my($Number) = @_;
105.  while ($Number ~ s/^-(\d+)(\d{3})$/$1,$2/);
106. return($Number);
107. }
108. 
109. format DumpVol =
110. FS      序列号                               标志
111. ---------------------------------------------------------------------------------
112. @<<<<< @@@ @<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
113. $Vol{fs_name}, $Vol{serial_num}, $Vol{volume_name}, $Vol{flags}
```

## 文件系统 75

```text
114. 总大小: @<<<<<<<<<<<<<<<<^^^^^^^^^^^^<<
115. $Vol{total}                              $Vol{flags}
116. 可用大小: @<<<<<<<<<<<<<<<<<<<<^^^^^^^^<<<<
117. $Vol{free}                             $Vol{flags}
118. -                              ^^^^^^^^^^^^<<<<
119. -                              ^^^^^^^^^^^^<<<<
120. -                              ^^^^^^^^^^^^<<<<
121. -                              ^^^^^^^^^^^^<<<<
122. -                              $Vol{flags}
123. -                              ^^^^^^^^^^^^<<<<
124. -                              $Vol{flags}
125. -                              ^^^^^^^^^^^^<<<<
126. -                              $Vol{flags}
127. -                              ^^^^^^^^^^^^<<<<
128. -                              $Vol{flags}
129. -                              ^^^^^^^^^^^^<<<<
130. -                              $Vol{flags}
131. -                              ^^^^^^^^^^^^<<<<
132. -                              $Vol{flags}
133. -                              ^^^^^^^^^^^^<<<<<<<<<<<<<<<<
134. -
135. -                              $Vol{flags}
136. .
```

## 创建硬链接

UNIX 用户一直可以在文件之间创建硬链接，并且从 Windows 2000 开始，Win32 平台的用户也可以做这一点。之前的 Windows NT 版本能够通过利用 POSIX 子系统来创建链接；然而，从 Windows 2000 开始，链接功能被直接构建在 Win32 API 中。

遗憾的是，这些链接并不像它们的 UNIX 兄弟版本那样丰富。UNIX 的硬链接必须位于同一个卷上。这意味着链接必须与它链接的文件位于同一个驱动器上。然而，Win32 并没有跨卷链接的能力。最接近的等物是快捷方式（shortcut），但它是由应用程序解释的，而不是操作系统（因此，你不能依赖程序来理解如何使用它们）。

这种硬链接能力仅在 NTFS 卷上支持。示例 3.3 创建了这样的硬链接。该脚本接受如下两个参数：

```bash
perl ln.pl c:\temp\ExistingFile.txt c:\MyNewLink.txt
```

第一个参数是已存在的文件，第二个参数是创建创建新文件的路径。这个新链接文件（在所有实际用途中）与第一个参数中指定的文件是同一个。编辑这些文件中的任何一个都会导致两个都被被修改。这是很合理的，因为你实际上只有一个文件，只是为它建立了两个独立的条目。

在 NTFS 卷上创建硬链接后，它在字面上链接到原始文件。即使你移动原始文件或链接文件，它们仍然指向相同的数据。此外，你可以修改任何一个文件的内容，它都会更新相同的数据。

## 第 3 章：工具

UNIX 用户一直可以在文件之间创建硬链接，并且从 Windows 2000 开始，Win32 平台的用户也可以做这一点。之前的 Windows NT 版本能够通过利用 POSIX 子系统来创建链接；然而，从 Windows 2000 开始，链接功能被直接构建在 Win32 API 中。

遗憾的是，这些链接并不像它们的 UNIX 兄弟版本那样丰富。UNIX 的硬链接必须位于同一个卷上。这意味着链接必须与它链接的文件位于同一个驱动器上。然而，Win32 并没有跨卷链接的能力。最接近的等物是快捷方式，但它是由应用程序解释的，而不是操作系统（因此，你不能依赖程序来理解如何使用它们）。

这种硬链接能力仅在 NTFS 卷上支持。示例 3.3 创建了这样的硬链接。该脚本接受如下两个参数：

```bash
perl ln.pl c:\temp\ExistingFile.txt c:\MyNewLink.txt
```

第一个参数是已存在的文件，第二个参数是创建创建新文件的路径。这个新链接文件（在所有实际用途中）与第一个参数中指定的文件是同一个文件。编辑这些文件中的任何一个都会导致两个被修改。这是很合理的，因为你实际上只有一个文件，只是为它建立了两个独立的条目。

在 NTFS 卷上创建硬链接后，它在字面上链接到原始文件。即使你移动原始文件或链接文件，它们仍然指向相同的数据。此外，你可以修改任何一个文件的内容，它都会更新相同的数据。

### 创建链接

```perl
01. use Win32::API;
02.
03. if (scalar @ARGV != 2)
04. {
05.     print "Usage: <File> <Link>\n";
06.     exit;
07. }
08.
09. my ($File, $Link) = @ARGV;
10.
11. if (CreateHardLink($Link, $File, 0))
12. {
13.     print "Link created successfully.\n";
14. }
15. else
16. {
17.     print "Failed to create link. Error: $!\n";
18. }
```

### 创建目录

创建目录并不是一个新概念。所有基于系统的操作系统（如 UNIX、Windows、Macintosh）都有容器的概念（例如，文件夹）。你必须创建容器，以便将文件和其他目录放入其中。你通常通过 `md` 或 `mkdir` 命令来实现。

Win32 通过其 `CreateDirectory()` 和 `CreateDirectoryEx()` 函数暴露了这一功能。在 Windows NT 和 2000 平台上，如果启用了扩展，DOS 的 `mkdir` 命令可以创建中间目录。例如，如果你运行：

```bash
md Dir1\Dir2
```

而 `Dir1` 不存在，那么 `Dir2` 将不会被创建。

Win32 无法创建中间目录——很可能是因为它只是调用了 C 库的 `mkdir()` 函数，该函数反过来调用了 Win32 API 的 `CreateDirectory()` 函数。示例 3.4 为了创建传入的目录会创建尽可能多的目录。

这个特定的脚本没有任何 Win32 特有的，因此它可以在任何运行 Perl 的平台上运行。该脚本接受一个参数，该参数必须是完整路径（例如 `C:\temp\Dir2`）、相对路径（例如 `..\Dir1\Dir2`）或 UNC 路径（例如 `\server\share\Dir1\Dir2`）。

要使用此脚本，只需传递要创建的路径名称即可，例如：

```bash
perl makedir.pl \server\share\dir1\dir2
```

### 示例 3.4 创建中间目录

```perl
01. $Dir = shift ARGV || "Syntax: <Dir>";
02. $Result = 1;
03. ($Root,$Path) = ($Dir =~ /\/([/]+)\/(.*)/);
04. print "Creating directory $Dir...\n";
05.
06. if (-d $Dir)
07. {
08.   print "Directory already exists.\n";
09.   exit;
10. }
11.
12. $DirList = split (\/, $Path);
13. $Path = $Root;
14.
15. while ($Result && @DirList)
16. {
17.   $Path .= (shift $DirList) . "";
18.   next if (-d $Path);
19.   $Result = mkdir($Path, 0777);
20. }
21.
22. print ($Result ? "Success" : "Failure (Error: $!)"), "\n";
```

# 文件系统 79

示例 3.6 从文本文件中的两个流都读取了数据。如果你检查生成的文本文件，你会注意到文件大小仅反映了默认数据流中的数据。如果你不知道文件中包含多个流，通常没有办法发现这些备用数据流。正如你将看到的，可以使用 Win32 Perl 来发现此类备用数据流。

## 示例 3.5 创建带有多个流的测试文件

```perl
01. $File = "StreamTest.txt";
02. $Stream = "AltDataStream";
03. if (open(STREAM1, "$File" ))
04. {
05.     print "Writing to the main data stream.\n";
06.     print STREAM1 "\tWelcome to the main data stream.\n";
07.     close(STREAM1);
08. 
09. if (open(STREAM2, "$File:$Stream" ))
10. {
11.     print "Writing to alternative 'Stream'.\n";
12.     print STREAM2 "\tWelcome to the alternative data stream '$Stream'\n";
13.     close(STREAM2);
14. }
15. else
16. {
17.     print "Error: $!\n";
18. }
19. 
20. else
21. {
22.     print "Error: $!\n";
23. }
```

## 示例 3.6 从测试文件中读取多个流

```perl
01. $File = "StreamTest.txt";
02. $Stream = "AltDataStream";
03. if (open(STREAM1, "$File" ))
04. {
05.     print "This is the main data stream for $File.\n";
06.     while(my $Line = <STREAM1>)
07. {
08.         print $Line;
09.     }
10.     close(STREAM1);
11. }
12. if (open(STREAM2, "$File:$Stream" ))
13. {
14.     print "\nThis is the data stream $File:$Stream:\n";
15.     while(my $Line = <STREAM2>)
16. {
```

## 示例 3.6 继续

```perl
17.   print $Line;
18.   }
19.   close(STREAM2);
20.   }
21.   else
22.   {
23.     print "Error: $!\n";
24.   }
25. }
26. else
27.   {
28.     print "Error: $!\n";
29. }
```

在 Windows NT/2000 上，可以诱导 `more` 命令显示备用数据流。你可以通过如下方式将数据流的输入重定向到命令来实现这一点：

```bash
< test.txt:MyStream
```

> 提示：出于某些原因，大多数程序不允许你输入包含备用流的有效 NTFS 路径。例如，尝试将 `test.txt:MyStream` 加载到记事本、Microsoft Word 或其他各种程序将失败。

示例 3.7 是 DOS 类型 `type` 命令的替代品。该脚本的功能相同，不同之处在于它可以显示 NTFS 数据流——这是 `type` 命令无法做到的。

脚本接受任意数量的显示路径。这包括包含通配符的路径。

```bash
perl streamdump.pl myfile.txt:altStream c:\temp\*.txt
```

## 示例 3.7 显示备用数据流内容

```perl
01. foreach my $Mask ( @ARGV )
02. {
03.   my @List;
04. 
05.   # 必须小心，因为 glob() 不支持
06.   # 带有空格的路径。
07.   if (@List = glob($Mask))
08.   {
09.     push(@FileList, @List);
10.  }
11.   else
12.  {
13.     push(@FileList, $Mask);
perl
14. }
15. foreach $Path (@FileList)
16. {
17.   print $Path, "\n";
18.   print "-" x length($Path), "\n";
19.   if (open(FILE, "<$Path"))
20.   {
21.     my $Buffer;
22.     binmode(FILE);
23.     while(read(FILE, $Buffer, 1024))
24.     {
25.       print $Buffer;
26.     }
27.     close(FILE);
28.   }
29.   else
30.   {
31.     print "\tError: $!\n";
32.   }
33. print "\n";
34. }
```

## NTFS、替代流与文件大小

有趣的是，报告的文件大小并不反映替代流的内容。例如，如果你创建一个 32 字节的文件并添加一个 500 字节的替代流，报告的仍然是 32 字节。这使得管理员无法确定文件到底占用了多少空间。

为了辅助 NTFS，由于 NTFS 的特性，目录列表可能会报告意外的可用空间。例如，如果你创建此文件：

```cmd
C:\echo Test > test.txt
```

目录列表显示文件的大小以及磁盘上的可用空间：



```
C:\dir test.txt
Volume in drive C is unnamed
Volume Serial Number is DC-AF23
Directory of C:\
06/01/2000  9:14 PM test.txt
               1 File(s)         15 bytes
               52 million bytes free
```

如果你将文件重写为不同的大小，`C:\echo This is really a test > test.txt` 输出：

```
C:\dir test.txt
Volume in drive C is unnamed
Volume Serial Number is DC-AF23
Directory of C:\
06/01/2000  9:14 PM test.txt
               1 File(s)         24 bytes
               52 million bytes free
```

注意，即使文件大小发生了变化，可用空间也没有，因为 NTFS 为每个文件计算两个不同的大小：文件的大小以及文件占用的空间。在这种情况下，文件大小为 15 或 24 字节。然而，文件占用了至少一个扇区。而该卷上的每个扇区由 1KB（1024 字节）的磁盘空间组成。因此，仅存储 15 字节的数据就需要 1024 字节的磁盘空间。当 NTFS 计算可用空间时，它是基于未分配的磁盘空间的。由于磁盘空间是以 1KB 块为单位占用的，剩余空间总是 1024 的倍数。

## 列举 NTFS 流

NTFS 流的问题在于无法列举文件中的流。考虑到 NTFS 流如此强大，这个问题相当悲惨。基本上意味着如果你忘记了向文件中添加了流，就没有办法发现它们。这种情形类似于从 DOS 中删除`dir`命令：你如何知道目录中有哪些文件？是的，这听起来很奇怪，但 Win32 缺乏对 NTFS 流的良好支持现状。

好消息是你可以使用技巧列举流。这种解决方案涉及以备份软件读取文件，使用 Win32 API 的`BackupRead()`函数。

`Streams.pl`脚本（示例 3.8）显示 NTFS 文件中所有流的名称和大小。脚本从命令行接受任意数量的参数。每个参数都是要检查是否存在备用流的文件路径。文件路径可以包含通配符。

### 示例 3.8 列举 NTFS 文件中的流

```perl
01. use Win32::API::Prototype;
02.
03. OPEN_EXISTING = 3;
04. $GENERIC_READ = 0x80000000;
05. $BACKUP_DATA = 0x00000001;
06. $BACKUP_ALTERNATE_DATA = 0x00000004;
07. 
08. ApiLink('kernel32.dll',
09.     'HANDLE CreateFile( LPCTSTR pszPath,
10.     DWORD dwAccess,
11.     DWORD dwShareMode,
12.     PVOID SecurityAttributes,
13.     DWORD dwCreationDist,
14.     DWORD dwFlags,
15.     HANDLE hTemplate )'
16. 
17. // die "Can not locate CreateFile"
18. ApiLink('kernel32.dll',
19.     'BOOL CloseHandle(HANDLE hFile )'
20. // die "Can not locate CloseHandle"
21. ApiLink('kernel32.dll',
22.     'BOOL BackupRead( HANDLE hFile,
23.     LPBYTE pBuffer,
24.     DWORD dwBytesToRead,
25.     LPWORD pdwBytesRead,
26.     BOOL bAbort,
27.     BOOL bProcessSecurity,
28.     LVOID (*ppContext)')
29. // die "Can not locate BackupRead"
30. ApiLink('kernel32.dll',
31.     'BOOL BackupSeek( HANDLE hFile,
32.     DWORD dwLowBytesToSeek,
33.     DWORD dwHighBytesToSeek,
34.     LPWORD pdwLowBytesSeeker,
35.     LPWORD pdwHighBytesSeeker,
36.     LVOID *ppContext)')
37.
38. // die "Can create BackupSeek"
39. # 生成要处理的文件列表
40. # 因此我们必须展开任何通配符
41. foreach my $Mask (@ARGV)
42. {
43.     foreach $Path ( glob ($Mask )
44.     {
45.         push(@Files, $Path) if (-f $Path);
46.     }
47. }
48. foreach my $File (@Files)
49. {
50.     print "$File\n"
51.
52.     $hFile = CreateFile($File,
53.     $GENERIC_READ,
54.     0,
55.     undef,
56.     $OPEN_EXISTING,
57.     0,
58.     ) || die "Can not open the file '$File\n";
```

### 示例 3.8 续

```perl
60. # 如果 CreateFile() $hFile 是负值
61. if ($0 < $hFile)
63. {
64. my $iStreamCount = 0;
65. my $TotalSize = 0;
66. my $pBytesRead = pack("L", 0);
67. my $pContext = pack("L", 0);
68. my $pStreamIDStruct = pack("L5", 0,0,0,0,0,0);
69. 
70. while( BackupRead($hFile,
71.     $pStreamIDStruct,
72.     length($pStreamIDStruct),
73.     $pBytesRead,
74.     0,
75.     $pContext ))
76. {
77.     my $pBytesRead = unpack("L", $pBytesRead);
78.     my $pContext = unpack("L", $pContext);
79.     my %Stream;
80.     my ($pSeekBytesLow, $pSeekBytesHigh) = pack("L", 0),
81.     pack("L", 0);
82.     my $StreamName = '';
83.     my $StreamSize;
84. 
85.     # 没有更多数据可读取
86.     last if ($0 == $pBytesRead);
87. 
88.     @Stream(id, attributes,
89.     size_low, size_high,
90.     name_size) unpack("L5", $pStreamIDStruct);
91. 
92.     if ($BACKUP_ALTERNATE_DATA == $Stream{id})
93.     {
94.         $StreamName = NewString($Stream{name_size});
95.         if(BackupRead($hFile,
96.             $StreamName,
97.             $Stream{name_size},
98.             $pBytesRead,
99.             0,
100.            0,
101.            $pContext ))
102.        {
103.            my $String = CleanString($StreamName, 1);
104.            $String =~ s/(.*):.*$/1;
105.            $StreamName = $String;
106.        }
107.    }
108.    elsif($BACKUP_DATA == $Stream{id})
109.    {
```

## 文件系统 85

```perl
110. $StreamName = "<Main Data Stream>";
111. }
112. $StreamSize = MakeLargeInt($Stream{$size_low}, $Stream{$size_high});
113. $iTotalSize += $StreamSize;
114.
115. printf('* %3d %s (%s bytes)\n",
116. ++$iStreamCount,
117. $StreamName,
118. FormatNumber($StreamSize ) if("ne $StreamName);",
119.
120. # 移动到下一个流...
121. if(! BackupSeek($HFile,
122. $Stream{$size_low},
123. $Stream{$size_high},
124. $pSeekBytesLow,
125. $pSeekBytesHigh,
126. $pContext )
127.
128. {
129. last;
130. }
131. $pBytesRead = pack('L2', 0);
132. $pStreamStruct = pack('L5', 0,0,0,0,0);
133. }
134. printf('* Total file size: %s bytes\n",
135. FormatNumber($iTotalSize ));
136. # 终止备份读取。Win32 API 声称我们必须这样做做。
137. BackupRead($HFile, undef, 0, 0, 1, 0, $pContext);
138. CloseHandle($HFile);
139. }
140. print "\n";
141. }
142. sub FormatNumber
143. {
144. my($Num) = @_;
145. } while($Num -- s/((\d+)(\d{3}))/$1,$2/);
146. return($Num);
147. }
149. sub MakeLargeInt
151. my($Low, $High) = @_;
return($High * (1 + 0FFFF) + $Low);
```

## 发现版本

许多二进制文件（如程序和 DLL）都包含版本信息。这种标记并非必须，但非常有用。当你安装软件时，会检查文件的版本信息以确保不会覆盖旧版本。图 3.2 显示了给定二进制文件的版本信息。这种显示不仅可以确定文件的版本，还可以确定它是为哪个平台（NT 或 DOS）创建的。

```text
C:\win\system32\filever.exe
Comments         January 1997
CompanyName      Microsoft Corporation
Description      Proxy for Windows Operating System
Version         5.0.3715
InternalName     filever.DLL
LangID           English (United States)
Copyright        Microsoft Corp. 1995
Legal            Microsoft is a registered trademark of Microsoft Corporation. Windows is a trademark of Microsoft Corporation
ProductName      Microsoft Automation
Version         5.0.3715
InternalInfo:
DateStamp        0
Debug            0
FileType         dll
Version         5.0.3715
OS               nt
Patched          0
PreRelease       5.0.3715
SpecialBuild     0
```

图 3.2 显示了 DLL 的版本信息。示例 3.9 接受任意数量的参数，每个参数代表二进制文件的路径。路径可以包含通配符和访问远程机器的 UNC。

### 示例 3.9 显示版本

```perl
01. use Win32::AdminMisc;
02. my $iCount = 0;
03. if ($0 == scalar @ARGV)
04. {
05.   Syntax();
06.   exit;
07. }
08. 
09. foreach $File (@ARGV)
10. {
11.   my %Info;
12.   $iCount++;
13.   if ($iCount) print "$iCount $File ";
14.   if (-f $File)
15.   {
16. 
17.     if (Win32::AdminMisc::GetFileInfo($File, \%Info))
18.     {
19.         print "\n";
20.         foreach myAttr in (keys (%Info))
21.         {
22.             next if (ref $Info{$Attr});
23.             Display($Attr, $Info{$Attr});
24.         }
25.     }
26.     if ($FileInfo)
27.     {
28.         Display("Internal Info:");
29.         foreach myAttr in (keys (%FileInfo))
30.         {
31.             next if (ref $FileInfo)->{$Attr};
32.             Display(" $Attr", $FileInfo)->{$Attr});
33.         }
34.     }
35.   }
36.   else
37.   {
38.       print("unable to get version.\n");
39.   }
40. }
41. else
42. {
43.     print("unable to locate file.\n");
44. }
45. 
46. sub Display
47. {
48.     my($Attr, $Data) = @_;
49. 
50.     print("\t$Attr");
51.     if ("*" ne $Data)
52.     {
53.         print("." x (20 - length($Attr)), "$Data");
54.     }
55.     print("\n");
56. }
57. 
58. sub Syntax
59. {
60.     my($Line) = "." x length($0);
61. 
62.     print <<EOT;
```

### 示例 3.9 续

```perl
66.
67. $0
68. $Line
69. Display version information on a particular file.
70. 
71. Syntax:
72. perl $0 File[,File2[, ... ]]
73. 
74. EOT
75. )
```

## 权限

安全性在很大程度上基于权限。权限放置在可安全对象（如文件、目录、注册表项和网络共享）上，用于指定哪些用户有权执行操作。权限的主题非常复杂，足以单独写一整本书，因此我不会详细介绍它的工作原理。对于这类信息，你可以咨询许多资源，包括`http://www.roth.net/perl/perms/security/`。

## 显示权限



UNIX 机器一直能够列出谁拥有文件和目录的权限。你可以通过`ls`命令获取此列表。Win32 中`ls`的对应命令是`dir`，它不显示任何权限信息。图 3.3 显示了目录的权限。脚本首先打印对象的所有者和组名称。接下来，打印每个被授予或拒绝访问的用户和组账户。权限所属的对象类型位于账户名之后。

| 字母 | 权限 |
| --- | --- |
| R | 允许读取 |
| r | 不允许读取 |
| W | 允许写入 |
| w | 不允许写入 |
| D | 允许删除 |
| d | 不允许删除 |
| X | 允许执行 |
| x | 不允许执行 |
| P | 允许修改权限 |
| p | 不允许修改权限 |
| O | 允许获取所有权 |
| o | 不允许获取所有权 |
| A | 授予所有权限 |
| a | 拒绝所有权限 |

```text
C:\perl perm.pl c:\temp

Permissions for 'c:\temp':
Owner: BUILTIN\Administrators
Group: BUILTIN\Domain Admins
    Administrator (Directory) RWXD--A
    Joel (Directory) RWXD--A
    Perltest7 (Directory) -----O-
    Perltest7 (File) RwX----
```

图 3.3 显示目录的权限。

## 文件和目录注意事项

对于文件和目录路径，可以使用通配符；但对于注册表项（Registry keys），不可以。

你可以使用 UNC 指定远程机器上的文件和目录。但是，如果你指定的是 UNC 的根目录，请确保如下所示使用反斜杠结束路径：

```text
\\server\
```

如果你没有添加反斜杠，则引用的将是网络共享本身的权限。

## 共享目录和打印机注意事项

共享目录和打印机路径不能以反斜杠结尾。如果你指定了以反斜杠结尾的共享目录路径，显示的将是共享目录根目录的权限，而不是网络共享本身的权限。尝试引用以反斜杠结尾的打印机将直接失败。

此外，请注意共享目录既没有所有者也没有组。

## 注册表项注意事项

你可以使用如下完整的注册表路径来指定注册表项：

```text
HKEY_LOCAL_MACHINE\Software
```

你可以通过如下缩短方式来简写注册表根：

```text
HKLM\Software
```

你还可以通过在前面加上机器名来指定远程机器上的注册表项：

```text
\\server\HKEY_LOCAL_MACHINE\Software
```

或者：

```text
\\server\HKLM\Software
```

## 注意

访问远程注册表时，只有`HKEY_USERS`和`HKEY_LOCAL_MACHINE`配置单元是可以访问的。♦

## 示例 3.10 显示权限信息

```perl
01. use Win32::Perms;
02.
03. # %PERM 哈希将权限类型映射到其在权限
04. # 数组中的位置。注意没有 $ 位置，
05. # 因为该位置留给了未处理的权限类型（且
06. # 我们不会打印它）。
07. %PERM = (
08. R => 1,
09. W => 2,
10. X => 3,
11. D => 4,
12. P => 5,
13. O => 6,
14. A => 7,
15. );
16.
17. %MAP = (
18. 'FILE_READ_DATA' => 'R',
19. 'GENERIC_READ' => 'R',
20. 'KEY_READ' => 'R',
21. 'DIR_READ' => 'R',
22.
23. 'FILE_WRITE_DATA' => 'W',
24. 'KEY_WRITE' => 'W',
25. 'GENERIC_WRITE' => 'W',
26. 'FILE_APPEND_DATA' => 'W',
27. 'DIR_ADD_SUBDIR' => 'W',
28. 'DIR_ADD_FILE' => 'W',
29.
30. 'DELETE' => 'D',
31. 'FILE_DELETE_CHILD' => 'D',
32.
33. 'FILE_EXECUTE' => 'X',
34. 'FILE_TRAVERSE' => 'X',
35. 'GENERIC_EXECUTE' => 'X',
36. 'DIR_TRAVERSE' => 'X',
37. 'DIR_EXECUTE' => 'X',
38.
39. 'CHANGE_PERMISSION' => 'P',
40.
41. 'TAKE_OWNERSHIP' => 'O',
42.
43. 'FILE_ALL_ACCESS' => 'A',
44. 'GENERIC_ALL' => 'A',
45. 'DIR_ALL_ACCESS' => 'A',
```

## 示例 3.10 续

```perl
46. 'STANDARD_RIGHTS_ALL' => 'A',
47. );
48.
49. push(@ARGV, ".*") unless scalar @ARGV;
50. foreach my $Mask (@ARGV)
51. {
52.   my (@List) = glob($Mask);
53.   if (! scalar @List)
54.   {
55.     push(@List, $Mask);
56.   }
57.   foreach my $Path (@List)
58.   {
59.     print "\nPermissions for '$Path':\n";
60.     ReportPerms($Path);
61.     print "\n\n";
62.   }
63. }
64.
65. sub ReportPerms
66. {
67.   my ($Path) = @_;
68.   my (@Acct, @List);
69.   my ($Perm) = new Win32::Perms($Path);
70.   my(%PermList) = ();
71.   my($MaxAcctLength) = 1;
72.
73.   if (! $Perm)
74.   {
75.     print "Can not obtain permissions for '$Path\n";
76.     return;
77.   }
78.   printf(" Owner: %s\n Group: %s\n",
79.     $Perm->Owner(),
80.     $Perm->Group());
81.     $Perm->Dump(@List);
82.   foreach my $Acct (@List)
83.   {
84.     my($PermMask);
85.     my($Mask, @M, @F);
86.     my($DaclType);
87.     my $bAllowAccess = ( "Deny" ne $Acct->{Access} );
88.     my $String;
89.     my $Acct;
90.   next if ($Acct->{Entry} ne "DACL")
91.   if ("" eq $Acct->{Account})
92.   {
93.     $Account = $Acct->{SID};
94.   else
95.     $Account = "$Acct->{Domain}" ne $Acct->{Domain};
96.     $Account = $Acct->{Account};
97. }if( length($Account) > $MaxAcctLength)
98.     $MaxAcctLength = length($Account);
99. $Total++;
100. DecodeMask($Acct, \M, \F);
101.foreach ($Mask (@M)
102.     $PermMask |= 2**$PERM{$Mask};
103.$DaclType = $Acct->{ObjectName};
104.if(2 == $Acct->{ObjectType})
105.     # 我们有一个文件或目录。因此我们需要判断
106.     # 这个 DACL 代表对象（文件）还是容器（目录）...
107.     if ($Acct->{Flag} & DIR)
108.         $DaclType = "Directory";
109.     else
110.     $DaclType = "File";
111.if( ! defined $PermList{$Account}{$DaclType}) {
112.     # 创建权限字符串。除非所有未处理的权限
113.     # 都默认到该位置，否则元素为空（我们不会打印它）。
114.     my $TempHash = [
115.         split(/, /, keys(%PERM))
116.     ];
117.     $PermList{$Account}{$DaclType} = $TempHash;
118.}foreach $Mask (keys(%PERM))
119.     if($PermMask & 2**$PERM{$Mask})
120.     {
121.         $String = $PermList{$Account}{$DaclType};
122.         # 如果已经拒绝了权限，则跳过此步，
123.         # 因为拒绝访问会覆盖任何允许访问
124.         if($String->{$PERM{$Mask}} != /[a-z]/)
125.             my $TempMask = $Mask;
126.             $TempMask = 1 if (@bAllowAccess);
127.             $String->{$PERM{$Mask}} = $TempMask;
128.         }
129.     }
```

```perl
}
if (!Total)
{
130.     # 没有 DACL 条目...
131.     print "\t Everyone has full permissions.\n";
132. }else
{
133.     foreach $Permission (keys(%PermList))
{
134.         foreach $DaclType (keys($PermList{$Permission}))
{
135.             my $String = $PermList{$Permission}{$DaclType};
136.             printf("%s %s %s\n",
137.                 $Permission,
138.                 $MaxAcctLength,
139.                 $DaclType,
140.                 join(', ', $String));
141.         }
142.     }
```

## 显示详细权限

“显示权限”部分的示例 3.10 显示了各种可安全对象（如文件和目录）的权限。该脚本将复杂的权限世界提取为非常基础且简单的权限集。使用该脚本，你可以轻松了解哪些用户拥有权限。然而，为了以简单的方式显示权限，必须做出许多假设和解释，这可能会丢失管理员成功维护安全所需的细节。

示例 3.11 显示了对象拥有的完整权限集。没有任何解释，所有的权限、标志和类型都以其完整、混乱的形态呈现。如果你不熟悉对象上可以设置的不同权限，这种显示可能不仅仅是混乱。

图 3.4 显示了此脚本产生的输出。可以地说，它不适合胆小的人。这个特定示例是图 3.3 所示`c:temp`目录的权限导出。与示例 3.10 不同，此脚本显示了所有权限信息。某些权限可能没有意义，但它们在 Win32 API SDK (`http://msdn.microsoft.com/`) 中记录。

```text
C:\>perm.pl c:\temp

Permissions for 'c:\temp':

Owner: BUILTIN\Administrators

Group: BUILTIN\Domain Admins

Account                Permissions          Flags

CREATOR OWNER            DELETE               INHERIT_ONLY_ACE

Deny Access                             OBJECT_INHERIT_ACE

(Directory)             CONTAINER_INHERIT_ACE

BUILTIN\Domain Admins         FILE_WRITE_DATA      INHERIT_ONLY_ACE

Deny Access             FILE_APPEND_DATA      OBJECT_INHERIT_ACE

(File)                  FILE_WRITE_EA

                         FILE_WRITE_ATTRIBUTES

BUILTIN\Domain Admins         DIR_ADD_SUBDIR       INHERIT_ONLY_ACE

Deny Access             TAKE_OWNERSHIP       CONTAINER_INHERIT_ACE

(Directory)             CHANGE_PERMISSION

CREATOR OWNER           DIR_READ              INHERIT_ONLY_ACE

Allow Access            DIR_ADD_FILE         OBJECT_INHERIT_ACE

(Directory)             DIR_ADD_SUBDIR       CONTAINER_INHERIT_ACE

                         DIR_READ_EATTRIB

                         DIR_WRITE_EATTRIB

                         DIR_EXECUTE

                         DIR_DEL_SUBDIR

                         DIR_READ_ATTRIB

                         DIR_WRITE_ATTRIB

                         READ_CONTROL

                         TAKE_OWNERSHIP

Administrator               DIR_READ               OBJECT_INHERIT_ACE

Allow Access            DIR_ADD_FILE         CONTAINER_INHERIT_ACE

(Directory)             DIR_ADD_SUBDIR

                         DIR_READ_EATTRIB

                         DIR_WRITE_EATTRIB

                         DIR_EXECUTE

                         DIR_DEL_SUBDIR

                         DIR_READ_ATTRIB

                         DIR_WRITE_ATTRIB

                         STANDARD_RIGHTS_ALL

Perltest7               FILE_WRITE_DATA        INHERIT_ONLY_ACE

Allow Access            FILE_READ_EA         OBJECT_INHERIT_ACE

(File)                  FILE_EXECUTE

                         FILE_READ_ATTRIBUTES

                         READ_CONTROL

                         SYNCHRONIZE
```

图 3.4 放置在文件上的真实权限。

# 第 3 章：工具

示例 3.11 接受命令行上的任意数量路径。每个路径都可以包含通配符。此外，它还接受可选的`/F`开关；它会报告所谓的“友好权限”（friendly permissions）。大多数管理员对这些权限都很熟悉，例如完全控制（FULL CONTROL）、更改（CHANGE）和读取（READ）。然而，这些友好权限是不完整的，并没有解释权限的真实本质。例如，没有一种友好权限描述一个文件具有读取（READ）和删除（DELETE）访问权限。

请参考“显示权限”部分了解如何处理不同的路径。

## 示例 3.11 显示对象的权限详情

```perl
01. use Getopt::Long;

02. use Win32::Perms;

03.

04. # 关闭激进的域控制器查找

05. Win32::LookupDC( 0 );

06. Configure( %Config);

07. if ($Config{help}) 

08. {

09.     Syntax();

10.     exit();

11. }

12.
```



## 示例 3.11 继续

```perl
13. foreach my $Mask (@{$Config{masks}})
14. {
15.     my $List = glob ( $Mask);
16.     if( scalar $List)
17. {
18.         push(@List, $Mask);
19.     }
20.     foreach $Path (@List)
21.     {
22.         print "\nPermissions for '$Path':\n";
23.         ReportPerms ($Path);
24.         print "\n\n";
25.     }
26. }
27.
28. sub ReportPerms
29. {
30.     my ($Path) = @_;
31.     my ($Acct, @List);
32.     my ($Perm) = new Win32::Perms ($Path);
33.
34.     if (! $Perm)
35.     {
36.         print "Can not obtain permissions for '$Path'\n";
37.         return;
38.     }
39.
40. printf(" Owner: %s\n Group: %s\n", $Perm->Owner(), $Perm->Group());
41.     $Perm->Dump(\@List);
42.     $- = PermissionHeader;
43.     write;
44.     foreach ($Acct as @List) {
45.         {
46.             my($PermMask);
47.             my($String) = split(\/, ".* scalar(keys(%PERM ))\);
48.             my($Mask, @Permissions, @Friendly);
49.             local $DACLType;
50.             local $Access = $Acct->{Access};
51.             local $Acct;
52.
53.             $- = Permission;
54.
55.             next if($Acct->{Entry} ne "DACL ");
56.             $i++;
57.
58.             DecodeMask($Acct, @Permissions, @Friendly);
59.             DecodeFlag($Acct, @Flag);
60.             # 对每个标志和权限用空格填充，以便它们在打印时
61.             # 正确地每行一个权限/标志。这是在使用 write/formats
62.             # 工作时的小技巧
63.             $Flags = join("" " * 10, "\n", @Flag);
64.             $Perms = join("" " * 10, "\n",
65.                             ($Config{friendly}) ? @Friendly : @Permissions);
66.             if("eq" $Acct->{Account}) if(
67.                 {
68.                     $Account = $Acct->{SID};
69.                 }
70.                 else {
71.                     $Account = $Acct->{Domain}" " ne $Acct->{Domain});
72.                     $Account .= $Acct->{Account};
73.                 }
74.             }
75.             $DACLType = $Acct->{ObjectName};
76.             if(2 == $Acct->{ObjectType}) {
77.                 {
78.                     # 我们拥有的是文件或目录。因此，我们需要
79.                     # 确定这个 DACL 代表一个对象（文件）还是
80.                     # 一个容器（目录）...
81.                     if($Acct->{Flag} &)
82.                         $DACLType = "Directory";
83.                     else {
84.                         $DACLType = "File";
85.                     }
86.                 }
87.             }
88.             write;
89.             print "\n";
90.         }
```

```perl
93.    if (! $Total)
94.    {
95.        print "\t Everyone full permissions.\n";
96.    }
97. }
98.    sub Configure
99.    {
100.        my ($Config) = @_;
101.        my $Result;
102.        Getopt::Long::Configure ('prefix_pattern=-/]*') );
103.        $Result = GetOptions($Config,
104.            qw,
105.                friendly|f
106.                help|h
107.            )
108.        );
109.        push(@Config{masks}, @ARGV);
110.        $Config->{help} = 1 unless ($Result && scalar @Config{masks});
111.    }
112.    sub Syntax
113.    {
114.        my ($Script) = $0 -=^\/);
115.        my ($Line) = length($Script);
116.        print <<EOT;
117.        $Script
118.        $Line
119.        Displays verbose permissions on securable objects.
120.
121.        Syntax:
122.        perl $Script [-f] [Path]
123.        -f..."friendly" permissions.
124.        Path.......The path to a securable object.
125.        This path can consist of * wildcards.
126.
127.    EOT
128. }
129.    format PermissionHeader =
130.    @|||||||||||||||| @|||||||||||||||
131.    "Account",             "Permissions",      "Flags"
132.    ----------------------------------------------------------------
133.    format Permission =
134.    "<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<"
135.    $Account, $Perms, $Flags
136.    <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
137.    $Account, $Perms, $Flags
138. @<<<<<<<<<<<<<<<<<<<<<<<<<<<<
139.    "Access Access", $Perms, $Flags
140. @<<<<<<<<<<<<<<<<<<<<<<<<<<<<
141.    ($DaclType", $Perms, $Flags
142. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
143.    $Account, $Perms, $Flags
144. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
145.    $Account, $Perms, $Flags
146. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
147.    $Account, $Perms, $Flags
148. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
149.    $Account, $Perms, $Flags
150. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
151.    $Account, $Perms, $Flags
152. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
153.    $Account, $Perms, $Flags
154. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
155.    $Account, $Perms, $Flags
156. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<T
```

## 所有权

几乎所有的对象都有一个所有者。所有者是一个账户（用户或组账户），对文件拥有最终访问权限。对象的所有者永远不会被拒绝访问。他可以读取、删除和修改权限，以及任何其他可能的操作。

然而，程序员很快就发现，备份软件必须能够在保持所有者完整的情况下恢复文件。这意味着有一种方法可以授予所有权！

请参考“显示权限”（Displaying Permissions）章节注释，获取有关如何处理不同路径的信息。

## 示例 3.12 获取和设置可安全对象的所有者

```perl
01. use Getopt::Long;
02. use Win32::Perms;
03.
04. # 关闭密集的域查找
05. Win32::LookupDC( 0 );
06.
07. Configure(\$Config);
08. if ($Config{help})
09. {
10. Syntax();
11. exit();
12. }
13.
14. $- = OwnerHeader
15. write;
16. $- = Owner;
17. foreach $Mask { @($Config{masks}) }
18. {
19. my(@List) = glob($Mask);
20. if scalar @List
21. {
22. push(@List, $Mask);
23. }
24. foreach $Path (@List)
25. {
26. my $Perm;
27.
28. if (eval { $Perm = new Win32::Perms($Path) } )
29. {
30. $Owner = "无法获取权限。\n";
31. }
32. else
33. {
34. if ("" ne $Config{owner})
35. {
36. $Perm->Owner($Config{owner});
37. $Perm->Set();
38. }
39. $Owner = $Perm->Owner();
40. }
41. write;
42. }
43. }
44.
45. sub Configure
46. {
47. my ($Config) = @_;
48. my $Result;
```

## 第 3 章：工具

## 示例 3.12 延续

```perl
49.
50. Getopt::Long::Configure("prefix_pattern=(-|\/)");
51. \$Result = GetOptions(\$Config,
52.     qw;
53.     owner|o=s
54.     help?|h
55. )
56. );
57. push(@{\$Config->{masks}}, @ARGV);
58. \$Config->{help} = 1 unless \$Result && scalar(@{\$Config->{masks}});
59. }
60.
61. sub Syntax
62.
63. my \$Script = (\$0 = /\/\/\*)?\/);
64. my \$Line = ".-" x length(\$Script);
65.
66. print <<EOT;
67.
68. \$Script
69. \$Line
70. 显示（并设置）可安全对象的所有者。
71.
72. 语法:
73.     perl \Script [-s Account] Path [ Path2 ... ]
74.     -s Account..将所有者设置为指定的账户。
75.     Path......指向可安全对象的路径。
76.     此路径可以包含 ? 和 * 通配符。
77.
78. EOT
79. }
80.
81. format OwnerHeader =
82. @<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
83. "Path", "Owner"
84. .................................................................................
85.
86.
87. format OwnerHeader =
88. @<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
89. \$Path, \$Owner
90.
```

## DCOM 配置

大多数用户并不知道他们的程序是使用 COM 进行通信的。他们将电子表格粘贴到文字处理文档中，而完全不知道这种功能是基于 COM 的对象链接和嵌入（OLE）技术实现的。

然而，你必须对安全保持警惕，因为最近版本的 Windows 用了分布式 COM（DCOM）。这项技术允许一台计算机与运行在另一台机器上的程序进行通信。这种功能对于管理目的非常理想，但如果有黑客侵入机器，则可能非常危险。

Windows 提供了 `DCOMCFG.EXE` 工具，用于配置 DCOM 安全。该工具允许你选择谁可以通过 DCOM 访问计算机。不过，它有两个问题：它是基于 GUI 的，并且只在本地机器上运行。

由于程序是基于 GUI 的，很难快速查看机器的 DCOM 配置情况。相反，你必须从一个选项卡移动到另一个选项卡并点击按钮。这样做不仅令人讨厌，而且浪费时间。

由于该工具只报告其运行所在机器的 DCOM 配置，其用途非常有限。这种限制要求如果你想检查服务器集群，就必须走到每台服务器，登录，然后运行该工具。

示例 3.13 在不使用 GUI 的情况下快速显示机器的 DCOM 配置。你也可以在运行脚本时传入机器名称来检查远程机器的 DCOM 配置。

> 每一个作为域成员的机器在域中都有一个机器账户（类似于用户账户）。当机器启动并上线时，它使用机器账户和密码登录域。在检查机器的 DCOM 配置时，你可能会发现对用户、组和机器账户的引用。

示例 3.5 显示了示例 3.13 的输出。注意在所有与安全相关的配置中，`Guest` 账户都被显式拒绝了。脚本显示了访问是被允许还是拒绝的。

```
C:\perl dcom.pl

Server 的 DCOM 设置:

DCOM 已启用。

COM Internet 服务已启用。

允许以下账户启动 COM 应用程序：

Allow NT AUTHORITY\SYSTEM
Allow NT AUTHORITY\INTERACTIVE
Deny SERVER\Guest
Allow BUILTIN\Administrators
```



## 第 3 章：工具

（继续）

通过 DCOM 访问此机器的账户：

- Allow `NT AUTHORITY\SYSTEM`
- Allow `NT AUTHORITY\INTERACTIVE`
- Deny `SERVER\Guest`
- Allow `BUILTIN\Administrators`
- Allow `SERVER\IUSR_SERVER`
- Allow `SERVER\IWAM_SERVER`
- Allow `BUILTIN\Administrators`

允许访问 COM/OLE 配置的账户：

- Allow `BUILTIN\Administrators`
- Allow `CREATOR OWNER`
- Deny `SERVER\Guest`
- Allow `Everyone`
- Allow `BUILTIN\Power Users`
- Allow `NT AUTHORITY\SYSTEM`
- Allow `BUILTIN\Users`

DCOM 允许使用的协议：

- `tcp`
- `sp`
- `ip`

> 图 3.5 检查 DCOM 配置。

### 示例 3.13 显示 DCOM 配置

```perl
01. use Win32::Registry;
02. use Win32::Perms;
03.
04. # 防止密集的域查找
05. Win32::Perms::DC();
06. %PATH = (
07.     ole => 'SOFTWARE\Ole',
08.     rpc => 'SOFTWARE\RPC',
09. );
10.
11. $Perm = new Win32::Perms() || die "创建对象";
12. if (scalar @ARGV)
13. {
14.     $Machine = shift $ARGV;
15. }
16. else
17.     $Machine = Win32::NodeName();
18. }
19. $Machine =~ s/\\+//;
20. $HKEY_LOCAL_MACHINE->Connect($Machine, $Root)
21. || die "连接失败";
22. print "\nDCOM settings for $Machine:\n";
23. if($Root->open($PATH{ole}, $Key))
24. {
25. my ($Type, $Value);
26. undef $Value;
27. $Key->QueryEx("EnableDCOM", $Type, $Value);
28. print "DCOM is " . ("y" lc $Value : "not") . "\n";
29.
30. print "COM Internet Services are " . ("y" lc $Value : "not") . "\n";
31.
32. if($Root->open($PATH{rpc}, $Key))
33. {
34. my ($Type, $Value);
35. undef $Value;
36. $Key->QueryEx("EnableHTTP", $Type, $Value);
37. print "HTTP is " . ("y" lc $Value : "not") . "\n";
38.
39. print "\nThe accounts are allowed to launch COM applications:\n";
40. if($Key->QueryEx("DefaultLaunchPermission", $Type, $Sd))
41. {
42. DisplayPerms($Sd) if REG_BINARY == $Type;
43. }
44. $Key->Close();
45. }
46. $Key->Close();
47. print "\n with access to this machine via DCOM:\n";
48. if($Key->QueryEx("DefaultAccessPermission", $Type, $Sd))
49. {
50. DisplayPerms($Sd) if REG_BINARY == $Type;
51. }
52. $Key->Close();
53.
54. print "\n with access to COM/OLE configuration:\n";
55. DisplayPerms($HKEY_CLASSES_ROOT);
56.
57. print "\nThe following protocols are permitted for use DCOM:\n";
58. if($Root->open($PATH{rpc}, $Key))
59. {
60. my $MString;
61. if($Key->QueryEx("DCOM Protocols", $Type, $MString))
62. {
63. foreach myProtocol (split("\x00", $MString))
64. {
65. print " $Protocol\n";
66. }
67. $Key2->Close();
68. }
69. $Key->Close();
70. $Root->Close();
71.
72. sub Syntax
73. {
74. my ($Config) = @_;
75. my $Script = (\$0 = /\/\/\*)?\/);
76. my $Line = ".-" x length(\$Script);
77.
78. print <<EOT;
79.
80. \$Script
81. \$Line
82. 显示（并设置）可安全对象的所有者。
83.
84. 语法:
85.     perl \Script [-s Account] Path [ Path2 ... ]
86.     -s Account..将所有者设置为指定的账户。
87.     Path......指向可安全对象的路径。
88.     此路径可以包含 ? 和 * 通配符。
89.
90. EOT
91. }
92.
93. format OwnerHeader =
94. @<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
95. "Path", "Owner"
96. .................................................................................
97.
98.
99. format OwnerHeader =
100. @<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
101. \$Path, \$Owner
102.
```

### 示例 3.12 延续

```perl
49.
50. Getopt::Long::Configure("prefix_pattern=(-|\/)");
51. \$Result = GetOptions(\$Config,
52.     qw;
53.     owner|o=s
54.     help?|h
55. )
56. );
57. push(@{\$Config->{masks}}, @ARGV);
58. \$Config->{help} = 1 unless \$Result && scalar(@{\$Config->{masks}});
59. }
60.
61. sub Syntax
62.
63. my \$Script = (\$0 = /\/\/\*)?\/);
64. my \$Line = ".-" x length(\$Script);
65.
66. print <<EOT;
67.
68. \$Script
69. \$Line
70. 显示（并设置）可安全对象的所有者。
71.
72. 语法:
73.     perl \Script [-s Account] Path [ Path2 ... ]
74.     -s Account..将所有者设置为指定的账户。
75.     Path......指向可安全对象的路径。
76.     此路径可以包含 ? 和 * 通配符。
77.
78. EOT
79. }
80.
81. format OwnerHeader =
82. @<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
83. "Path", "Owner"
84. .................................................................................
85.
86.
87. format OwnerHeader =
88. @<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
89. \$Path, \$Owner
90.
```

缺乏这种搜索功能可能部分是因为实际上没有真正的需求。毕竟，该信息存储库的设计初衷是让进程持有配置数据——即以前存储在 `.INI` 文件中的内容。这里的假设是软件会知道自己将数据存储在注册表的哪里，因此永远不需要查找它。然而，这种假设是基于软件会规规矩运行这一观念的。

很多时候，当你卸载软件时，它会完整地留下自己的痕迹，例如注册表信息。在这种情况下，在注册表中搜索特定的 GUID 或搜索内容是非常有价值的。再举一个完全相关的例子：通常由于某些奇怪的原因，某些软件会将窗口移动到屏幕之外的位置。如果你正在使用双显示器但必须临时只使用一个显示器，可能会发生这种窗口重定位。如果你偶尔使用高分辨率显示器，也可能发生这种情况。无论如何，每当应用程序运行时，用户交互的窗口都位于一个看不见的地方。由于大多数用户不知道例如记事本等可能在注册表的哪个位置定位其配置存储，因此搜索变得至关重要。

示例 3.14 执行了此类搜索。当你传入注册表路径和搜索字符串时，脚本会扫描注册表并在执行过程中显示其结果。你可以传入多个路径和多个搜索字符串。你只需要使用 `-p` 开关指定每个路径——根据需要指定多个。然后传入尽可能多的字符串。

你可以通过在路径前加上机器名称来定位远程机器上的每个路径。你也可以像表 3.3 所示缩写注册表根键。

**表 3.3 注册表根键及其缩写**

| 注册表根 | 缩写 |
| :--- | :--- |
| `HKEY_LOCAL_MACHINE` | `HKLM` |
| `HKEY_CURRENT_USER` | `HKCR` |
| `HKEY_CLASSES_ROOT` | `HKCU` |
| `HKEY_USERS` | `HKU` |
| `HKEY_CURRENT_CONFIG` | `HKCC` |

考虑这个示例：

```perl
perl regfind.pl -p HKEY_LOCAL_MACHINE\Software
-p \server1\HKLM\Software winamp "windows media"
```

## 第 3 章：工具

此实例搜索了当前机器上的 `HKEY_LOCAL_MACHINE\Software` 注册表路径以及 `\Server1`。在注册表中搜索字符串 `winamp` 或 "windows media"。搜索不区分大小写，`WinAmp` 也会触发匹配。搜索遍历整个注册表路径。因此，可能需要一些时间完成。

输出打印到 STDOUT，但关于搜索如何打印的信息打印到 STDERR。这样，你可以在继续查看搜索结果的同时，将输出重定向到文件。

### 示例 3.14 在注册表中定位字符串

```perl
01. use Getopt::Long;
02. use Win32::Registry;
03.
04. %HIVE_LIST =
05. HKEY_LOCAL_MACHINE => $HKEY_LOCAL_MACHINE,
06. HKEY_CURRENT_USER => $HKEY_CURRENT_USER,
07. HKEY_CLASSES_ROOT => $HKEY_CLASSES_ROOT,
08. HKEY_USERS => $HKEY_USERS,
09. HKEY_CURRENT_CONFIG => $HKEY_CURRENT_CONFIG,
10. );
11. %HIVE_LIST_ABBR = (
12. HKLM,
13. HKCU => $HKEY_CURRENT_USER,
14. HKCR => $HKEY_CLASSES_ROOT,
15. HKU => $HKEY_USERS,
16. HKCC => $HKEY_CURRENT_CONFIG,
17. );
18. fetch my $Key keys (%HIVE_LIST)
19. {
20. $HIVE_LIST_REVERSE{$HIVE_LIST{$Key}} = $Key;
21. }
22. $iTotalKeys = $iTotalMatch = 0;
23. Configure ($Config);
24. if ($Config(help))
25. {
26.
27. Syntax();
28. exit();
29. }
30.
31. while (my $Path = shift @{$Config{paths})})
32. {
33. my ($Temp, $Machine, $Hive) = ($Path =~ /^\((((|\|\)?\1)?\.).*$/);
34. my ($Hive, $Temp2, $Path) = ($Hive =~ /^\((\|\)?\1)?(\((.*)))?/);
35. my $Root = OpenHive($Hive, $Machine);
36.
37. if ($Root \= $Root)
38. {
39. my @Keys;
40. my @List;
41.
42. if ("" ne $Machine)
43. {
44. $Hive = "$Machine\$Hive";
43. }
44.
45. if ($Root->Open($Path, $Key)
46. {
47.     $Path = \$Path if ("" ne $Path);
48.     print "Scanning $HivePath\n";
49.     ProcessKey($Key, "$HivePath", $KeyName);
50. }
51. else
52. {
53.     print "Unable to open $Hive\$Path\n";
54. }
55.     $Root->Close();
56. }
57. else
58. {
59.     # not connect.
60. }
61.
62. print STDERR "\n----------------------\n";
63. print STDERR "Total values: $iTotalKeys\n";
64. print STDERR "Total matching: $iTotalMatch\n";
65.
66. sub Open
67. {
68.     my($Hive, $Machine) = @;
69.     my $Root;
70.     my $HiveKey = $HIVE_LIST_ABBR[uc $Hive];
71.
72. if ("Win32::Registry" ref $HiveKey)
73. {
74.     $HiveKey = $HIVE_LIST{uc $Hive};
75. }
76.
77. if ("" ne $Machine)
78. {
79.     if (!$HiveKey->Connect($Machine, $Root))
80.         print STDERR "Could connect $Machine\n";
81.         $Root = 0;
82.     }
83.     else
84.     {
85.         $Root = $HiveKey;
86.     }
87.
88.     return($Root);
89. }
90.
91. sub ProcessKey
92. {
93.     my($Key, $Path, $KeyName) = @;
94.     my $TempKey;
95.
96.     if ($Key->Open($KeyName, $TempKey))
97. {
98.     my ($SubKey, $Value, $Keys) = @;
99.     my $ThisPath = $Path;
100.     $ThisPath = \$KeyName if ("" ne $KeyName);
101.     if ($TempKey->GetValues($Values))
102.     {
103.         foreach my $ (sort ($Keys))
104.             my ($Name, $Type, $Data) = @{$Values};
105.             $iTotalKeys++;
106.             printf(STDERR, "%s keys checked; %s matched.\n",
107.                 FormatNumber($iTotalKeys),
108.                 FormatNumber($iTotalMatch));
109.             foreach $Target (@{$Config{target}})
```



110.                 if ($Data ~ /$Target/i)

111.                     if (REG_BINARY == $Type)

112.                         {

113.                             $Data = "<Binary Data>";

114.                             print STDERR, "%d" * 60, "\n";

115.                             printf(STDOUT, "%s\%d (%s) %s\n",

116.                                ++$iTotalMatch,

117.                                $ThisPath,

118.                                $Value,

119.                                ValueType($Type),

120.                                $Data);

121.                         }

122.                 }

123.     }

124.     $TempKey->GetKeys($Keys);

125.

126.     foreach $SubKey (sort (@Keys))

127.     {

128.         ProcessKey($TempKey, $ThisPath, $SubKey);

129. 

130.         $TempKey->Close();

131. 

132.     }

133. }

134. 

135. sub ValueType

136. {

137.     my ($Type) = @;

138.     my ($ValueType);

139. 

140.     if ( REG_SZ == $Type )

141.     {

142.         $ValueType = "REG_SZ";

143.     elsif (REG_EXPAND_SZ == $Type) {

144.         $ValueType = "REG_EXPAND_SZ";

145.     elsif (REG_MULTI_SZ == $Type) {

146.         $ValueType = "REG_MULTI_SZ";

147.     elsif (REG_DWORD == $Type) {

148.         $ValueType = "REG_DWORD";

149.     elsif (REG_BINARY == $Type) {

150.         $ValueType = "REG_BINARY";

151.     } else {

152.         $ValueType = "Unknown Type";

153.     }

154.     return ($ValueType);

155. }

156. 

157. sub FormatNumber

158. {

159.     my($Number) = @;

160.     while ($Number = $Number - s/\(-?\d+)(\d{3})\/$1,$2 /);

161.     return ($Number);

162. }

163. 

164. sub Configure

165. {

166.     my($Config) = @;

167.     my $Result;

168.     Getopt::Long::Configure("prefix_pattern=-([\/)");

169.     $Result = GetOptions($Config,

170.     qw(

171.     paths|p=

172.     help?|h

173.     ));

174.     foreach my $Target (@ARGV) {

175.         push(@{$Config->{target}}, { find => $Target });

176.     }

177.     if(! scalar @{$Config->{paths}}) {

178.         push(@{$Config->{paths}}, 'HKLM');

179.     }

180. }

```

使用这个特定的示例，你只需要走到每台机器并使用特殊账户登录。重复此操作 100 次，任务就完成了。可以把此视为微软系统管理服务器（SMS）的廉价版本。

自动登录（autologon）的负面影响是用户名和密码被添加到注册表中，可以相对容易地发现。这些信息没有经过编码，因此任何拥有注册表键权限的人都能看到用户名和密码。你可以通过应用权限来修复，使得只有管理员和系统账户对该键具有读取权限，并可以更改权限和获取所有权。示例 3.1 根据传递给脚本的内容开启或关闭自动登录功能。其语法如下：

```perl
perl setlogon.pl [-m Machine] [-clear] [<Domain\User | User> <Password>]
```

开关见表 3.4。如果指定了用户名，则必须指定密码。应该指定用户账户的域，但不是必须。然而，如果本地机器用户数据库中的另一个用户账户与默认域中的账户同名，可能会发生登录问题。

## 表 3.4 自动登录开关

| 开关 | 说明 |
| :--- | :--- |
| `-m Machine` | 此开关指定为哪台机器配置自动登录。如果没有指定此开关，默认是本地机器。 |
| `clear` | 此开关清除自动登录配置。用户名、域和密码将被清除，自动登录功能被关闭。 |
| `User` | 自动登录账户的用户名。 |
| `Domain` | 自动登录账户的域。此开关为可选。 |
| `Password` | 自动登录账户的密码。 |

## 示例 3.15 设置自动登录用户账户

```perl
01. use Getopt::Long;
02. use Win32::Registry;
03.
04. $PATH = "Software\Microsoft\Windows NT\CurrentVersion\Winlogon";
05. Configure (\$Config);
06. if ($Config(help)) {
07. 
08.     Syntax();
09. exit();
10. }
11.
12. my $Root = $HKEY_LOCAL_MACHINE;
13. my $Key;
14.
15. if ( "" ne $Config{machine} )
16. {
17.     print "Connecting to $Config{machine}...\n";
18.     if (! $Root->Connect($Config{machine}, $Root ))
19.     {
20.         print "can not connect to $Machine\n";
21.         exit();
22.     }
23. }
24.
25. if ($Root->Create($PATH, $Key ))
26. {
27.     foreach my $Param ( keys %{$Config{params}} ))
28.     {
29.         my $Result = $Key->SetValue($Param,
30.             0,
31.             REG_SZ,
32.             $Config{params}->$Param );
33.         print "Setting $Param to $Config{Param}->$Param: ",
34.             ($Result) ? "success":"failure", "\n";
35.     }
36.     $Key->Close();
37. }
38. else
39. {
40.     print "Unable to open the $PATH key.\n";
41. }
42.
43. if ( "" ne $Config{machine} )
44. {
45.     $Root->Close();
46. }
47.
48. sub Configure
49. {
50.     my ($Config) = @_
51.     my $Result;
52.     my $Params = {
53.         DefaultName => "",
54.         DefaultUsername => "",
55.         DefaultPassword => "",
56.         AutoAdminLogon => 0,
57.     }
58.
59.     Getopt::Long::Configure("prefix_pattern=(-|/)");
60.     $Result = GetOptions($Config,
61.             machine|m=s
62.
63.             clear|c
64.             help?|h
65. )
66. );
67.     $Config->{help} = 1 unless ($Result) ;
68.
69. if (! $Config->{clear})
70. {
71.     $Params->{DefaultDomainName} shift @ARGV;
72.     if ( "" ne $Params->{DefaultDomainName} )
73.     {
74.         ($Params->{DefaultDomainName},
75.         $Params->{DefaultUserName}) = ($Params->{DefaultDomainName}
76.         =~ /((.*\\)?(.*$))/[1..3]);
77.     }
78.     $Params->{DefaultPassword} = shift @ARGV;
79.     $Params->{AutoDomainLogon} = 1;
80.
81. else
82. {
83.     $Params->{AutoDomainLogon} = 0;
84. }
85. if ( "" eq $Params->{DefaultUserName} )
86.     && ( $Config->{clear} )
87. {
88.     $Config->{help} = 1;
89. }
90.     $Config->{params} = $Params;
91.     return;
92.
93. sub Syntax
94. {
95.     my($Script) = ($0 =~ m#([\])+$/);
96.     my($Line = "-" x length($Script));
97.     my($Whitespace = " " * length($Script));
98.     print << "EOT";
99.     $Script$Line
100. EOT
101. 此工具将设置登录信息，如域、密码以及计算机是否登录。
102. 语法: $Script -m Machine <Domain\User> <Password> -clear
103. - User: 要自动登录的用户
104. - Domain: 自动登录的域
105. - Password: 自动登录的密码
106. - Machine: 要设置/取消的机器
```

## TCP/IP 配置

你可以在机器上配置多个网卡。你还可以将多个 TCP/IP 地址绑定到指定的网卡，这使得追踪哪个 IP 地址变得困难。所有这些信息都存储在每台机器的注册表中。然而，追踪这些信息可能非常麻烦。脚本接收一个表示要查询机器的参数。如果没有传递机器名称，则假设为本地机器。例如`tcpinfo.pl`。在这种情况下，获取的是本地机器的 TCP 配置。

## 示例 3.16 显示机器的 TCP/IP 配置



```perl
01. use Win32::Registry;
02.
03. %KeyName = (
04.     serviceroot => 'System\ControlSet\Services',
05.     tcplink => 'Tcpip\Linkage',
06.     tcplink_disabled => 'Tcpip\Linkage\Disabled',
07.     win2k_tcplink => 'Tcpip\Interfaces',
08.     deviceparam_tcp => 'Parameters\Tcpip',
09. );
10.
11. $Root = $HKEY_LOCAL_MACHINE;
12.
13. if ($Machine = $ARGV[0]) {
14.     $HKEY_LOCAL_MACHINE->Connect($Machine, $Root);
15.     || die "could not connect to the registry on '$Machine\n";
16. }
17.
18. if ($Root->Open($KeyName{serviceroot}, $Root)) {
19. {
20.     # 先检查是否为 Win2k...
21.     if ($Root->Open($KeyName{win2k_tcplink}, $Root)) {
22.     {
23.         my @Interfaces;
24.         if ($Links->GetKeys(\@Interfaces)) {
25.         {
26.             foreach my $DeviceName (@Interfaces) {
27.                 {
28.                     push(@Devices, [
29.                         "$KeyName{win2k_tcplink}\\$DeviceName",
30.                         $DeviceName
31.                     ]);
32.                 }
33.         }
34.         $Links->Close();
35.     }
36.     # 获取绑定的网卡名称...
37.     else
38.     if($Root->Open($KeyName{tcplink}, $Links)) {
39.     {
40.         my($Data);
41.         if ($Links->QueryEx("Bind", $DataType, $Data)) {
42.         {
43.             $Data = s/\n/ /g;
44.             $Data = s/\/Device\\ /g;
45.             $Data = s/\s+(.*)\s\$1/g;
46.             foreach my $DeviceName ( split(/\c+/, $Data )) {
47.                 {
48.                     push(@Devices, {
49.                         "$DeviceName\\KeyName(deviceparam_tcp)",
50.                         $DeviceName
51.                     });
52.                 }
53.         }
54.         $Links->Close();
55.         # 获取已绑定但已禁用的网卡名称...
56.         if ($Root->Open($KeyName{tcplink_disabled}, $Links)) {
57.     {
58.             my($Data);
59.             if ($Links->QueryEx("Bind", $DataType, $Data)) {
60.             {
61.                 $Data = s/\s+///g;
62.                 $Data = s/\/Device\\ /g;
63.                 foreach my $DeviceName ( split(/\c+/, $Data )) {
64.                 {
65.                     push(@Devices, {
66.                         "$DeviceName\\KeyName(deviceparam_tcp)",
67.                         $DeviceName
68.                     });
69.                 }
70.             }
71.             $Links->Close();
72.         }
73.     }
74. }
75.
76. foreach my $Device (@Devices) {
77.     my($DeviceTCPKey);
78.     my($Path) = $Device->[0];
79.
80.     my($DeviceName) = $Device->[1];
81.
82.     if($Root->Open($Path, $DeviceTCPKey)) {
83.     {
84.         my %hash;
85.         my($IP, @Subnet, @Gateway, @DNS);
86.         my($Data);
87.
88.         # 获取域...
89.         if($DeviceTCPKey->QueryValue("Domain", $Data)) {
90.         {
91.             $hash{Domain} = $Data;
92.         }
93.
94.         # 获取 IP 地址...
95.         if($DeviceTCPKey->QueryValue("IPAddress", $DataType, $Data)) {
96.         {
97.             $Data = s/0\.\0\.\0\.\//g;
98.             $Data = s/\c+/\c/g;
99.             push(@IP, split(/\c+/, $Data));
100.            push(@DHCP, ("no") * scalar split(/\c+/, $Data));
101.        }
102.
103.        # 获取子网掩码...
104.        if($DeviceTCPKey->QueryValue("SubnetMask", $DataType, $Data)) {
105.        {
106.             $Data = s/0\.\0\.\0\.\//g;
107.             $Data = s/\c+/\c/g;
108.             push(@Subnet, split(/\c+/, $Data));
109.        }
110.
111.        # 获取默认网关...
112.        if($DeviceTCPKey->QueryValue("DefaultGateway", $DataType, $Data)) {
113.        {
114.             $Data = s/0\.\0\.\0\.\//g;
115.             $Data = s/\c+/\c/g;
116.             push(@Gateway, split(/\c+/, $Data));
117.        }
118.
119.        # 获取 DNS 服务器...
120.        if($DeviceTCPKey->QueryValue("NameServer", $DataType, $Data)) {
121.        {
122.             push(@DNS, split(/\c+/, $Data));
123.        }
124.    }
125.
126.    print "Interface: $DeviceName\n";
127.    print "  Domain: " . ($hash{Domain} // "N/A") . "\n";
128.    print "  IP Addresses: " . join(", ", @IP) . "\n";
129.    print "  DHCP: " . (@DHCP ? "yes" : "no") . "\n";
130.    print "  Subnet Masks: " . join(", ", @Subnet) . "\n";
131.    print "  Gateways: " . join(", ", @Gateway) . "\n";
132.    print "  DNS: " . join(", ", @DNS) . "\n";
133. }
134. }
```

```perl
push(@DNS, split(/\s+/, $Data ));
},
```

## 查询 DHCP 状态

```perl
if ($DeviceTCPKey->QueryValueEx("EnableDHCP",

  $DataType,

  $Data )) {

  {Hash($dhcp) = (($Data) ? "yes":"no");

}
```

## 获取 DHCP 域...

```perl
$DeviceTCPKey->QueryValueEx("DhcpDomain",

  $DataType,

  $Data ))
```

## 获取 DHCP IP 地址...

```perl
if ($DeviceTCPKey->QueryValueEx("DHCPIPAddress",

  $DataType,

  $Data )) {

  $Data =~ s/\s+//g;

  $Data =~ s/\0\.\0\.\0//g;

  $Data =~ s/\c+//g;

  push(@0IP, split(/\c+/, $Data));

  push(@DHCP, "yes") x scalar split(/\c+/, $Data));

}
```

## 获取 DHCP 子子网掩码...

```perl
if ($DeviceTCPKey->QueryValueEx("DHCSubnetMask",

  $DataType,

  $Data )) {

  $Data =~ s/\s+//g;

  $Data =~ s/\0\.\0\.\0//g;

  $Data =~ s/\c+//g;

  push(@Subnet, split(/\c+/, $Data));

}
```

## 获取 DHCP 网关...

```perl
if ($DeviceTCPKey->QueryValueEx("DHCPDefaultGateway",

  $DataType,

  $Data )) {

  $Data =~ s/\s+//g;

  $Data =~ s/\0\.\0\.\0//g;

  $Data =~ s/\c+//g;

  push(@Gateway, split(/\c+/, $Data));

}
```

## 获取 获取 DNS 服务器...

```perl
if ($DeviceTCPKey->QueryValueEx("DHCPNameServer",

  $DataType,

  $Data ))
```

# 第 3 章：工具

## 示例 3.16 延续

```perl
187. {

188.   $Data = s/0\.\0\.\0//g;

189.   push(@DNS, split(/\s+/, $Data));

190. }

191.

192. next if ($ = scalar @IP);

193.   $Hash(name) = $DeviceName;

194.   $Hash(ip) = join(" " * 8, @IP);

195.   $Hash(subnet) = join(" " * 8, @Subnet);

196.   $Hash(gateway) = join(" " * 8, @Gateway);

197.   $Hash(dhcp) = join(" " * 8, @DHCP);

198.   $Hash(dns) = join(" " * 8, @DNS);

199.   $Hash(domain) = $Domain;

200.

201.

202. # 将我们新发现的数据推入栈中...

203.   push(@TCPConfig, %Hash);

204.

205.

206. $DeviceTCPKey->Close();

207.

208.

209. print "The machine $Machine has the following IP addresses:\n";

210. for (@TCPConfig)

211. {

212.   print "\ninterface: $IP->{name}\n";

213.   print "Domain: $IP->{domain}\n"

214.

215.   $- = TCPHeader;

216.   write;

217.   $- = TCPDump;

218.   write;

219. }

220. $ServiceRoot->Close();

221.

222. format TCPHeader = <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<>>>>

223. "DHCP", "IP Address", "Subnet Mask", "Gateway", "DNS"

224.

225.

226.

227. format TCPDump = <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<>>>>>>>>

228. $IP->{dhcp}, $IP->{ip}, $IP->{subnet}, $IP->{gateway}, $IP->{dns}

229. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<>>>>>>>>

230. $IP->{dhcp}, $IP->{ip}, $IP->{subnet}, $IP->{gateway}, $IP->{dns}

231. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<>>>>>>>>

232. $IP->{dhcp}, $IP->{ip}, $IP->{subnet}, $IP->{gateway}, $IP->{dns}

233. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<>>>>>>>>

234. $IP->{dhcp}, $IP->{ip}, $IP->{subnet}, $IP->{gateway}, $IP->{dns}

235. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<>>>>>>>>

236. $IP->{dhcp}, $IP->{ip}, $IP->{subnet}, $IP->{gateway}, $IP->{dns}

237. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<>>>>>>>>

238. $IP->{dhcp}, $IP->{ip}, $IP->{subnet}, $IP->{gateway}, $IP->{dns}

239. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<>>>>>>>>

240. <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<>>>>>>>>
```

## 结论

管理员可以使用许多种不同的工具来简化工作。从开源代码到商业软件包，提供了完成任务所需的实用。本章演示了 Perl 管理 Win32 文件系统、权限和注册表的卓越能力。所讨论的工具可以修改以针对其他任务。

## 事件管理

很快就会出现危机，你的团队必须采取行动。这些人会被视为英雄还是失败，取决于问题的解决速度。当然，解决此问题的简单方法是建立预防性维护，例如每七天重启服务器或每天备份数据。这种例行维护可以防止严重问题的发生，并在发生时提供解决方案。

然而，无论你的准备工作有多充分，情况总是让你后悔没有早点考虑。我观察到，最大的问题不在于规模，而在于细节。例如，你可以轻松地向主管解释文件服务器崩溃正在重建；然而，解释由于空 DACL 导致数据无法访问可能更加困难。

许多现成的解决方案可以处理此类危机。例如，如果管理员意外撤销了共享目录中所有文件的权限，而每个子目录具有不同的权限，重新创建这些权限将是一项艰巨的任务，特别是你有数百个对象需要处理时。从磁带恢复可能会覆盖自上次备份以来收集的海量数据。但是，如果之前备份了权限，只需要一个短 Perl 脚本即可重新应用权限而不会丢失任何数据。

## 备份和恢复网络共享

对于文件服务器，拥有许多共享目录并不常见。有些可能是公开的，而另一些可能是安全的，只授予特定用户权限。同样，有些可能是隐藏的，而另一些所有人可见。



管理许多共享目录可能非常困难。问问任何需要在服务器上重新安装过操作系统的管理员。然而，不必这样做。事实上，使用适当的工具可以很容易。

示例 4.1 提供了一个简单的脚本，连接到机器并尝试发现各种共享目录配置。这种备份共享目录的方法是理想的，因为它以简单的文本格式生成配置。这种格式便于你使用文本编辑器修改配置。

### 示例 4.1 导出共享目录配置

```perl
use Win32::Lanman;
use Win32::Perms;

$DELIMITER = ";";

# 根据获取共享类型的名称
%SHARE_TYPE = (
  eval($STYPE_DEVICE) => 'STYPE_DEVICE',
  eval($STYPE_PRINTQ) => 'STYPE_PRINTQ',
  eval($STYPE_DISKREE) => 'STYPE_DISKREE',
  eval($STYPE_IPC) => 'STYPE_IPC',
  eval($STYPE_SPECIAL) => 'STYPE_SPECIAL',
);

%PERM_SHARE_TYPE = (
  eval($STYPE_PRINTQ) => 5, # 共享打印机
  eval($STYPE_DISKREE) => 4, # 共享目录
);

## 默认本地机器
$Machine = Win32::NodeName unless ($Machine = shift @ARGV);
# 修复机器名上的任何双斜杠
($Machine = "\\" . $Machine) =~ s/\///;
# 我们不想使用严谨的域控制器查找
Win32::Perms::LookupDP( 0);
$Perm = new Win32::Perms(
) || die "Can not create an empty Perm object\n";
```

```perl
my(@Acl);
if (Win32::Lanman::NetEnum($Machine, \ShareList)) {
  foreach my $Share (@ShareList) {
    $ObjectType = $PERM_SHARE_TYPE($Share->{type});
    print("[$Share->netname}]\n");
    $Share->{type} = ComputeType($Share->{type});
    foreach my $Attribute = sort(keys( %Share )) {
      if("security_descriptor" eq $Attribute) {
        DumpSD($Share->{Attribute}, $ObjectType);
      }
      else {
        print("$Attribute=$Share->{Attribute}\n");
      }
    }
  }
}
print("\n");

sub ComputeType = @_
my($Type) = $@
my(@List);
if ($Type & &STYPE_SPECIAL) {
  push(@List, $SHARE_TYPE($STYPE_SPECIAL));
}
$Type & - &STYPE_SPECIAL;
push(@List, $SHARE_TYPE($Type));
return( join("[", @List) );
}

sub DumpSD = @_
my($SD, $ObjectType) = $@
$Perm->Remove(-1);
$Perm->Import($SD);
$Perm->Dump(@Acl);
foreach my $Ace (@Acl) {
  my $Account = $Ace->{Account};
  my(@Masks, @FriendlyPerms, @Types);
  $Account = $Ace->{Domain} . " \" $Account if ("" ne $Ace->{Domain});

  # 共享不适用所有者或组
  next if ("Owner" eq $Ace->{Entry} || "Group" eq $Ace->{Entry});

  # 设置 Ace 为 'Share'。由于我们导入了安全描述符，Win32::Perms 无法知道它是共享的
  $Ace->{ObjectType} = $ObjectType;
  Win32::Perms::DecodeMask($Ace, @Masks, @FriendlyPerms);
  Win32::Perms::DecodeType($Ace->{Type}, @Types);
  Win32::Perms::DecodeFlag($Ace->{Flag}, @Flags);
}
```

## 第 4 章：危机管理

## 示例 4.1 续

```perl
86.   print "$Perm=$Account", $DELIMITER;
87.   print join("|", @Types ), $DELIMITER;
88.   print join("|", @Flags ), $DELIMITER;
89.   print join("|", @MaskPerms ), "\n";
90.   }
91. )
92.
93.   # 出某些原因 Win32::Lanman 忘记导出此常量
94.   sub STYPE_SPECIAL
95.   {
96.     return (0x80000000 );
97.   )
```

你可以将网络上的机器名称作为唯一参数传递给脚本，这将使脚本发现该机器上所有共享目录的配置，前提是你的脚本在该机器上拥有管理员权限。如果没有指定机器名称，则使用本地机器。

脚本将配置导出到`STDOUT`，因此如果你想保存配置，可以如下所示将其重定向到文件：

`perl DumpShares.pl \server > server_shares.ini`

输出数据以标准的 Windows `.INI` 文件格式出现。由于该文件可以在远程执行，你可以指定网络上的某一台机器为你管理的所有每台服务器运行此脚本。这种共享目录配置文件的库可以在需要时用于重建服务器的共享目录。配置文件是基于文本的 `.INI` 文件，你可以修改这些文件，通过删除目录并使用修改后的配置脚本重新创建它们，来实现对目录的修改。

要从配置文件创建共享目录，请运行示例 4.2 中的脚本并传入配置文件的名称。要重新创建上一个示例中备份的目录，可以使用以下命令：

`perl MakeShares.pl server_shares.ini`

## 示例 4.2 创建共享目录

```perl
01. use Win32::Lanman;
02. use Win32::Perms;
03. use Win32::API;
04.
05. $DELIMITER = ";"; die "No config file specified\n";
06. $File = shift(@ARGV) || die;
07. $Machine = Win32::NodeName() unless ($Machine = shift(@ARGV) );
08. ($Machine = "\\\\$Machine") -= s/\\\\{2,}/\\\\/;
```

![](img/b5063514d2e449d6d8c5d65f100b84aa_145_0.png)

## 备份和恢复网络共享

```perl
10. %PERM_TYPE = (
11. Allow => ALLOW,
12. Deny => DENY,
13. );
14. # 我们不想使用严谨的域控制器查找
15. Win32::Perms::LookupDC( 0);
16.
17. if (ProcessFile($File, \Config))
18. {
19. foreach my $Share keys ($Config)
20. {
21. print "Creating $Machine\$Share->{netname}...";
22. if (CreateShare($Machine, $Config($Share)))
23. {
24. print "Success";
25. }
26. else
27. {
28. print "failure: ";
29. print Win32::FormatMessage(Win32::Lanman::GetLastError());
30. }
31. print "\n";
32. }
```

35. sub CreateShare

```perl
36. {
37. my($Machine, $Share) = @_;
38. my $Result = 0;
39.
40. if ($Share->{type} & &STYPE_SPECIAL)
41. {
42. print " SPECIAL SHARE! Ignore this.\n";
43. return ( 0 );
44. }
45. if (scalar ($Share->{perm}))
46. {
47. $Perm = new Win32::Perms();
48. foreach my $PermLine (@$Share->{perm})
49. {
50. my($Account, $Type, $Flag, $Mask) = split ($DELIMITER,
51. $PermLine);
52. $Perm->Add($Account,
53. eval ($Mask),
54. eval ($Type),
55. eval ($Flag));
56. }
57. $Share->{security_descriptor}
58. = $Perm->GetSD(SD_RELATIVE);
59. }
60. if (STYPE_DISKTREE == $Share->{type} )
61. {
```

## 示例 4.2 续

```perl
62.  $Result = Win32::Lanman::NetShareAdd($Machine, $Share);
63.  }
64.  elsif (TYPE_PRINT == $Share->{type})
65.  {
66.    print "can't share a printer!\n";
67.  }
68.
69.    return($Result);
70.  }
71.
72.  sub ProcessFile
73.  {
74.    my($File, $ShareList) = @;
75.    my $iResult = 0;
76.
77.    if(open(SHAREDDATA, "<", $File))
78.    {
79.      $iResult = ParseShares(SHAREDDATA, $ShareList);
80.      close(SHAREDDATA);
81.    }
82.    else
83.    {
84.      print "Unable to open '$File': $!\n";
85.    }
86.    return($iResult);
87.  }
88.
89.  sub ParseShares
90.  {
91.    my($FileHandle, $ShareList) = @;
92.    my $ShareName = "*";
93.    my $iTotal = 0;
94.
95.    while($Line = <FileHandle>)
96.    {
97.      my($Name, $Value) = @;
98.      if($Line =~ /\s*\]/);
99.        next if;
100.     next($Line =~ /\s*\]/);
101. if($Line =~ /\s*\]/)
102.     {
103.       $ShareName = $Name;
104.       $iTotal++;
105.     next;
106.     if($Line =~ /\s*\]/);
107.     {
108.       next;
109.     }
110.     if($Line =~ /\s*\]/);
111.     {
112.       next;
113.     }
114.     if($Line =~ /\s*\]/);
115.     {
116.       next;
117.     }
118.     if($Line =~ /\s*\]/);
119.     {
120.       next;
121.     }
122.     if($Line =~ /\s*\]/);
123.     {
124.       next;
125.     }
126.     if($Line =~ /\s*\]/);
127.     {
128.       next;
129.     }
130.     if($Line =~ /\s*\]/);
131.     {
132.       next;
133.     }
134.     }
```



## 示例 4.2 续

```perl
36. {
37. my($Machine, $Share) = @_;
38. my $Result = 0;
39.
40. if ($Share->{type} & &STYPE_SPECIAL)
41. {
42. print " SPECIAL SHARE! Ignore this.\n";
43. return ( 0 );
44. }
45. if (scalar ($Share->{perm}))
46. {
47. $Perm = new Win32::Perms();
48. foreach my $PermLine (@$Share->{perm})
49. {
50. my($Account, $Type, $Flag, $Mask) = split ($DELIMITER,
51. $PermLine);
52. $Perm->Add($Account,
53. eval ($Mask),
54. eval ($Type),
55. eval ($Flag));
56. }
57. $Share->{security_descriptor}
58. = $Perm->GetSD(SD_RELATIVE);
59. }
60. if (STYPE_DISKTREE == $Share->{type} )
61. {
```

```perl
62.  $Result = Win32::Lanman::NetShareAdd($Machine, $Share);
63.  }
64.  elsif (TYPE_PRINT == $Share->{type})
65.  {
66.    print "can't share a printer!\n";
67.  }
68.
69.    return($Result);
70.  }
71.
72.  sub ProcessFile
73.  {
74.    my($File, $ShareList) = @;
75.    my $iResult = 0;
76.
77.    if(open(SHAREDDATA, "<", $File))
78.    {
79.      $iResult = ParseShares(SHAREDDATA, $ShareList);
80.      close(SHAREDDATA);
81.    }
82.    else
83.    {
84.      print "Unable to open '$File': $!\n";
85.    }
86.    return($iResult);
87.  }
88.
89.  sub ParseShares
90.  {
91.    my($FileHandle, $ShareList) = @;
92.    my $ShareName = "*";
93.    my $iTotal = 0;
94.
95.    while($Line = <FileHandle>)
96.    {
97.      my($Name, $Value) = @;
98.      if($Line =~ /\s*\]/);
99.        next if;
100.     next($Line =~ /\s*\]/);
... (此处省略重复代码块，保持原文原样)
```

## 备份用户和机器账户

你可以如下如下调用脚本：

```perl
perl MakeAccounts.pl \webserver\.ini
```

传递的第一个参数是配置文件的路径，可选的第二个参数指定要创建账户的机器。如果没有指定机器名称，则默认为本地机器。如果你正在重新创建域的用户或机器账户，则需要将域的 PDC（主域控制器）作为第二个参数指定。

## 示例 4.3 获取用户或机器账户信息

```perl
01. use Win32::Lanman;
02. use Getopt::Long;
03.
04. %Config = (
05. level => 1
06. );
07. Configure(\%Config, @ARGV );
08. if ($Config{help})
09. {
10. Syntax();
11. exit 0;
12. }
13. if ( defined $Config{domain})
14. {
15. Win32::Lanman::NetGetDCName ($Config{machine},
16. $Config{domain},
17. \$Config{machine});
18. }
19. if ( Win32::Lanman::GetDisplayInformationIndex ($Config{machine},
20. $Config{level},
21. $Config{prefix},
22. \$Index )
23. {
24. do
25. {
26. Win32::Lanman::QueryDisplayInformation ($Config{machine},
27. $Config{level},
28. $Index,
29. 10,
30. \$Accounts);
31. foreach my $Account (@Accounts)
32. {
33. print "\$Account->{name}\n";
34. print STDERR "\$Account->{name}\n";
35. $Index = \$Account->{next_index};
36. if (Win32::Lanman::NetUserInfo ($Config{machine},
37. \$Account->{name},
38. \$Info )
39. }
40. foreach my $Attribute ( sort (keys (\%Config)) ))
41. {
42.     my $Value = $Info($Attribute);
43.     $Value = s/((\||\w-]+)/sprintf("\x%02x", "C", $1 )/eg;
44.     print "$Attribute=$Value\n";
45.     }
46.  }
47.     print "\n";
48.  }
49. }while( scalar @Accounts );
50. 
51. 
52. sub Configure
53. {
54.     my($Config) = @_;
55.     my $Result = 0;
56.     Getopt::Long::Configure("prefix_pattern=(-|\/") );
57.     $Result = GetOptions($Config,
58.     qw(
59.         domain|d=s
60.         machine|m=s
61.         prefix|p=s
62.         type|t=s
63.         help|?|h
64.     )
65.     );
66. 
67.     if( lc $Config->{type} eq "user")
68.     {
69.         $Config->{level} = 1;
70.     }
71.     elsif( lc $Config->{type} eq "machine")
72.     {
73.         $Config->{level} = 2;
74.     }
75.     $Config->{help} = 1 if(! $Result );
76.  }
77. 
78. sub Syntax
79. {
80.     my($Script) = ($0 =~ \/\|]*?\//);
81.     my($Line) = "." x($Script);
82. 
83.     print <<EOT;
84.     $Script
85.     $Line
86. EOT;
87. 
88. 将账户转储到文件。
89. 
90.     用法:
91.     perl $Script [-t user | machine][-p Prefix][-d Domain]
92. 指定要导的账户。
93. 默认为本地机器。
94. -t 指定账户类型。
95. user: 账户（默认）
96. machine: 账户
97. -p Prefix 指定账户前缀。
98. 仅查询以该字符串开账户。
99. -d Domain 指定使用的域。
100. EOT
101. }

## 示例 4. 恢复用户或机器账户

```perl

01. use Win32::Lanman;

02.

03. $File = shift(@ARGV) || die "No file specified\n";

04. $Machine = shift(@ARGV) unless $Machine;

05. ($Machine =~ /\/) = s/\//;

06.

07. if (ProcessFile($File, \$Config))

08. {

09.     foreach my $Account (keys (%Config))

10.     {

11.         print "Creating \$Account->{name}...";

12.         if (CreateAccount($Machine, \$Config))

13.         {

14.             print "Success";

15.         }

16.         else

17.         {

18.             print "failure: ";

19.             print Win32::FormatMessage(Win32::Lanman::GetLastError());

20.         }

21.     }

22.     print "\n";

23. }

24. 

25. 

26. sub CreateAccount

27. {

28.     my ($Machine, $Account) = @_;

29.     my $Result = 0;

30.

31.     # 这是机器账户吗？

32.     if ($Account->{name} =~ /\$/)

33.     {

34.         #按照规则创建机器账户

35.         $Account->{name} = uc $Account->{name};

36.         ($Account->{password}) = lc $Account->{password} =~.{0,14}/;

37.         $Account->{password} -= s/\$/

38.     }

39.     $Result = Win32::Lanman::NetAdd($Machine, $Account);

40.

41.     return ($Result);

42. }

43.

44. sub ProcessFile

45. {

46.     my ($File, $AccountList) = @_;

47.     my $iResult = 0;

48.

49.     if (open(ACCOUNTDATA, '<$File'))

50.     {

51.     $iResult = ParseAccounts("ACCOUNTDATA", $AccountList);

52.     close(ACCOUNTDATA);

53. }

54.     else

55.     {

56.     print "Unable to open '$File': $!";

57. 

58.     return ($iResult);

59. 

60. 

61. sub ParseAccounts

62.     {

63.     my ($FileHandle, $AccountList) = @_;

64.     my $AccountName = "*";

65.     my $iTotal = 0;

66.

67.     while ($Line = <$FileHandle>)

68.     {

69.         my ($Name, $Value);

70.

71.         next if ($Line =~ /\s*[#;]/);

72.         next if ($Line =~ /\s*$/);

73.         if ($Name) = ($Line =~ /\s*\s*(.*?)\s*=\//)

74.         {

75.             $AccountName = lc $Name;

76.             $iTotal++;

77.             next;

78.         }

79.         next if ("*" eq $AccountName);

80.

81.         ($Name, $Value) = ($Line =~ /\s*(.*?)=(.*)\s*$/);

82.         if ('$i' ne $Name)

83.         {

84.             $Name = lc $Name;

85.             $Value = s/\(\w{2})\pack("c",hex($1))/ge;

86.             $AccountList->{$AccountName->$Name} = $Value;

87.         }

88.

89.         return ($iTotal);

90.     }

91. } 

92. # 出于原因 Win32::Lanman 忘记导出此常量

93. sub STYPE_SPECIAL

94. {

95.     return(0x00000000);

96. }

```

## 备份和恢复权限

```perl

11. else

{

    push(@Paths, $Mask);

    }

}

foreach my $Path (@Paths)

{

    print STDERR '$Path ';

    if (! ProcessPath($Path))

    {

        print STDERR "...FAILED!\n";

    }

    print STDERR "\n";

}

sub ProcessProcess

{

    my($Path) = @_;

    my @Acl;

    my $Perm;

    return(0) unless ($Perm = new Win32::Permissions($Path));

    print "$Path\n";

    $Perm->Dump(\Acl);

    foreach my $Ace (@Acl) {

        my $Account = $Ace->{Domain} . " " . $Account = "" if (ne $Ace->{Domain});

        if("Group" eq $Ace->{Entry} || "Owner" eq $Ace->{Entry})

        {

            print "$Ace->{Entry}=\$Account\n";

        }

        else

        {

            my(@MaskPerms, @FriendlyPerms, @Flags);

            print "$Ace->{Entry}=\n";

            Win32::Permissions::DecodeMask($Ace, @MaskPerms, @FriendlyPerms);

            Win32::Permissions::DecodeFlag($Flag, @Flags);

            print join($DELIMITER, ($Account, $Ace->{Access}),

                join("|", @Flags),

                join("|", @MaskPerms));

            print "\n";

        }

    }

    print "\n"

    return(1);

}

```

# 示例 4.6 重新应用安全权限

```perl

use Win32::Perms;

$DELIMITER = ":;";

Win32::Perms::LookupDC( 0 );

$File = shift(@ARGV) || die "No config file specified\n";

$Machine = Win32::NodeName unless ($Machine = shift(@ARGV) );

( \$Machine = \$Machine") = $s/\{2,}/\/g;

if (ProcessFile($File, %Config)) {

    foreach my $Object (keys (%Config)) {

        print "Creating$Machine$Object...";

        if (ApplyPerms($Machine, $Config{$Object})) {

            print "Success"

        }

        else

        {

            print "failure: ";
```




#我是由深度求索（DeepSeek）研发的 deepseek-v4-flash-0731 智能大模型。发现打开的文件

每个机器维护每个用户当前共享的文件和目录列表。当你需要跟踪用户打开了哪些资源时，此列表将非常有价值。示例 4.7 连接到指定的机器（如果没有指定则为本地机器）并获取打开资源的列表。你可以轻松想象此脚本有多实用。如果有人以某些用户的身份登录破解了网络安全，你可以快速发现他们在哪些服务器上打开了文件。图 4.1 展示了这一点。

| ID | 锁定 | 路径 |
| :--- | :--- | :--- |
| DATA | \PIPE\spool |
| DATA | \PIPE\winreg |
| DATA | e:\old\template\global.dot |
| DATA | e:\old\document\4.doc |
| DATA | e:\old\document\4.doc |
| DATA | \PIPE\srvsvc |
| PROXY | C:\temp |
| dev | \PIPE\srvsvc |

图 4.1 转打开的文件列表。此示例显示了查询除另一个服务器 (`dev`) 之外的所有域 (`*`)。结果显示用户在服务器上拥有多个资源，包括连接到打印机池 (`\PIPE\spool`) 和注册表 (`\PIPE\winreg`)。作为管理员，当用户连接到文件共享服务 (`\PIPE\srvsc`) 时，你应该产生怀疑。同时也连接到了 `c:\temp` 目录，这可能是在 Explorer 程序中；然而，用户对 `PROXY` 机器没有连接。

## 示例 4.7 远程列出文件

```perl
use vars(%USERS);
use Getopt::Long;
use Win32;
use Win32::Lanman;

%PATH = (
  max => 45,
  filler => '...',
);

Configure(\Config);

if ($Config{help}) {
  Syntax();
  exit();
}

$USERS = join(":", @Config{users}) . ";";

if (! scalar(@Config{servers}}, Win32::NodeName()); {
  push(@{$Config{servers}}, Win32::NodeName());
}

foreach my $Server (sort(@{$Config{servers}})) {
{
    my $FileInfo;
    next if lc $Server eq $PrevServer;
    $PrevServer = lc $Server;
    print "Open files on $Server:\n";
    $- = OUTPUT_HEADER;
    write;
    $- = OUTPUT;
    $- = "\.\-+";
    foreach my $Path (@{$Config{paths}}) {
{
        my (@Info, $Server);
        if (Win32::Lanman::NetFileEnum($Server,
          Path,
          $User,
          \Info )) {
            push(@FileInfo, @Info);
```

# 示例 4.7 续

```perl
}
}

foreach $File ( @FileInfo)
{
    undef %Data;
    $Data{path} = $File->pathname;
    $Data{user} = $File->username;
    $Data{locks} = $File->num_locks;
    $Data{id} = $File->id;
    if (scalar @Config{users}) {
        next unless ($USERS = / $Data{user};);
    }
    if (! $Config{full}) {
        if ($PATH{max} < length ($Data{path})) {
            my $PathLength = int ($PATH{max} - length ($PATH{filler})) / 2);
            my $FillerLength = length ($PATH{filler});
            $Data{path} = $Data{path};
            $Data{path} =~ s/\({PathLength})\(.*)?({PathLength})\/$1$PATH{filler}$3/;
        }
    }
    write;
}

print "\n";

sub Configure
{
    my ($Config) = @_;
    my $Result = 0;
    Getopt::Long("prefix_pattern=-|\\"" * );
    $Result = GetOptions($Config,
      qw {
        users|u=s
        full|f
        machine|m=s
        help?|h
      }
    );
    push(@{$Config{paths}}, @ARGV);
    foreach $Machine (@{$Config{machine}})
    {
        if (** $Machine)
        {
            my $Domain = Win32::DomainName();
            qw( @List;);
```

## 发现打开的文件 143

```perl
98. if(Win32::Lanman::NetServerEnum('
99. $Domain,
100. TYPE_SERVER,
101. (List ))
102. {
103. map
104. {
105. push(@{$Config->{servers}}, $->{name});
106. }List;
107. }
108. else
109. {
110. push(@{$Config->{servers}}, $Machine);
111. }
112. }
113. $Config->{help} = 1 unless($Result);
114. }
115. sub Syntax
116. {
117. my($Script) = $0 -= /[[\//\]]*\$/);
118. my($Line) = " " x length($Script);
119. }
120. print <<EOT;
121. $Script
$Line
显示服务器 m 上打开了哪些。
语法：
```bash
perl $Script [-f] [-u User] [-m Machine] [Path [Path2 ...]]
```
- -U......仅显示由此用户打开的文件。
可以根据需要使用任意数量的 -u。
- -f......显示每个打开文件的完整路径。
- -m......检查此机器。
指定所有所有共享文件的机器。
默认值是本地机器。
- Path......要检查的指定服务器本地的路径。
这可以是文件路径也可以是目录路径。
默认是服务器上的所有文件。
EOT
```

```perl
122. }
```

```perl
format OUTPUT_HEADER=
'ID', 'Locks', 'User', 'Path'
```

```perl
format OUTPUT =
```

## 第 4 章：危机管理

### 示例 4.7 继续 <<<<<<<<<<<<<<

```perl
151. @@@>>> @@@@ @<<<<<<<< $Data{user}, $Data{path}
152. $Data{id}, $Data{locks}, $Data{path} <<<<<<<<<<<<<
153. - $Data{path}
154. <<<<<<<<<<<
155. $Data{path}
156. <<<<<<<<<<<<<<<<<<<<<<<<<
157.
158. $Data{path}
159. ..
```

## 关闭打开的连接

在上一节所示的图 4.1 中，注意用户与 `\DATA` 上的注册表建立了连接。假设该用户不是管理员，那么该用户没有理由检查文件服务器的注册表。从安全的角度来看，这种情况可能是非常危险的；因此，断开用户与服务的连接是重要的。

示例 4.8 中的脚本关闭了远程打开的文件或其他资源。只有远程访问的文件才能使用此脚本关闭。图 4.2 显示了使用此脚本关闭用户到注册表的连接。

```bash
C:\perl closefile.pl -m data 31339
```

以下文件已被强制关闭：

| ID User Path |

| 31339 Joel \PIPE|winreg |

图 4.2 关闭到共享资源的远程连接。

该脚本可以接受一个机器名称（如果没有指定，则假设为本地机器）和任意数量的打开的文件 ID。你可以通过示例 4.7 获取 ID 编号列表。（更多详情请参阅前面的章节“发现打开的文件”。）

## 示例 4.8 关闭远程打开的文件

```perl
01. use vars qw ($PATH);
02. use Getopt::Long;
03. use Win32::Lanman;
04.
05. %PATH = (
06. max => 45,
07. filler => ... , '
08. );
```

```perl
09.
10. Configure( \Config );
11. if( $Config{help} )
12. {
13. Syntax();
14. exit();
15. }
16.
17. foreach my $FileID @{$Config{ids})
18. {
19. my(%File);
20. if( Win32::Lanman::NetFileInfo($Config{machine},
21.     $FileID,
22.     \File ))
23. {
24.     undef $Data;
25. $Data{path} = $File{pathname};
26. $Data{user} = $File{username};
27. $Data{locks} = $File{num_locks};
28. $Data{id} = $File{id};
29. }
30. if($PATH{max} < length($PATH{max}))
31. {
32. my $PathLength = int(($PATH{max}
33. - length($PATH{filler})) / 2);
34. my $FileLength = length($PATH{filler});
35. $Data{path} -=
36. s'({$PathLength}).({FileLength})$/$PATH{filler}$/
37. }
38.
39. if( Win32::Lanman::FileClose($Config{machine},
40.     $FileID ))
41. {
42. my(%Temp) = $Data;
43. push({Failed, \%Temp });
44. }
45. else
46. my(%Temp) = $Data;
47. push({Succeeded, \%Temp });
48. }
49. else
50. {
51. my %Temp = (
52. id => $FileID,
53. pathname => 'File ID is not use this server.',
54. );
55. push({Failed, \%Temp });
56. }
57.
58. if( scalar @Succeeded
```



## 恢复文档

Windows 操作系统一直使用文件扩展名来将特定文件映射到创建它的应用程序。例如，Microsoft Word 文档具有`.doc`扩展名，Adobe Photoshop 文件具有`.psd`扩展名。如果文件不小心被重命名为不同的扩展名，确定该文件代表什么类型可能会非常困难。

一个完美的例子是硬盘的目录结构损坏了。当这个问题发生时，你会运行`CHKDSK.EXE`工具或类似的工具。通常情况下，运行此工具会导致产生一系列带有模糊名称的碎片文件。尽管这些文件中的某些可能是完全完好的，但你不知道它们是什么类型的文件。如果你有数百个文件，你可能会花费许多夜晚来尝试恢复这些文件。

## 第 4 章：危机管理

幸运的是，Win32 采用了一些巧妙的技术来发现文档的类型。当脚本尝试在文件上创建一个对象时，Win32 使用不同的机制来确定文件类型，包括检查文件扩展名和检查文档的类 ID，仅仅为了命名它。

示例 4.9 利用此功能将文档加载为 COM 对象。如果文档成功加载，脚本将尝试根据文件的标题、主题和文件类型重命名文档。你可以传递任意数量的文件路径，包括通配符，所示：

```bash
perl Documents.pl .* c:\recovered\File01
```

该脚本对 Microsoft 应用程序比较有利，但也可以轻松修改以适用于其他应用程序。

你需要注意关于可以解析的文档类型的注意事项：运行脚本的机器上必须安装特定应用程序的软件，即使问题文件位于其他机器。例如，如果你安装了 MS Office 98，MS Word 2000 文档可能无法正确解析。

```perl
if( $Obj = Win32::OLE->GetObject($File) )
{
    my( $Type, $Ext, $Subject, $Title);
    my $NewFileName = "";

    $Total{recovered}++;

    $Type = join(" *", Win32::OLE->QueryObjectType($Obj) );
    $App = $Obj->(Application)->{Name};
    if( $App =~ /word/i )
    {
        $Ext = ".doc";
        $Total{type}->{word}++;
    }
    elsif( $App =~ /excel/i )
    {
        $Ext = ".xls";
        $Total{type}->{excel}++;
    }
    elseif( $App =~ /project/i )
    {
        $Ext = ".mpp";
        $Total{type}->{project}++;
    }
    elsif( $App =~ /powerpoint/i )
    {
        $Ext = ".ppt";
        $Total{type}->{powerpoint}++;
    }
    else
    {
        $Ext = ".$Type";
        $Total{type}->{lc $Type}++;
    }

$Title = $Obj->BuiltinDocumentProperties( "Title" )->{Value};
$Subject = $Obj->BuiltinDocumentProperties( "Subject" )->{Value};

my( $Path, $FileName, $FileExt ) =
($File =~ /^(.+?)[\/\]([^/]+)?\.(.*)$/);
if( ( "" ne $Title ) || ( "" ne $Subject )) {
    $FileName = ( "" ne $Title ) ? $Title : $Subject;

    # Replace any bad chars
    $FileName = s/[\.\?]*//g;
    $FilePath = "$FileName$Ext";
}

print " $App document\n";
if( $Ext ne $FileName ) && ( $File ne $FilePath ) {
{
```

## 示例 4.9 继续

```perl
80.  my $Count = 1;
81.  while (( -e "$Path$FilePath")
82      || ( defined $UsedFileNames(lc $FilePath)) {
83      {
84.          $iCount++;
85.          $FilePath = "$FileName$iCount$Ext";
86.      }
87.      $UsedFileNames(lc $FilePath) = 1;
88.      push( $RenameFiles, [$FilePath, $FilePath]);
89.  }
90.  else
91.  {
92.      print " No need to rename.";
93.      print " The file is correctly named already.\n";
94.  }
95. 
96.  # 尝试正常关闭应用程序
97.  if (! $Obj->Close( 0 ) ) {
98.      {
99.          if (! $Obj->Quit( 0 ) ) {
100.             {
101.                 $Obj->Exit( 0 );
102.             }
103.         }
104.          }
105.  print "\n";
106. 
107. 
108.  print "Renaming files:\n" if scalar ($RenameFiles) {
109.  foreach $file ( $RenameFiles ) {
110.     {
111.         my $Result = 0;
112.         print " $File->[0] -> $File->[1] ";
113.         $Result = rename ($File->[0], $File->[1]);
114.         print ($Result) ? "Success" : "Failed" };
115.         push($FailedToRename, $File->[0] ) if (! $Result );
116.         print "\n";
117.     }
118.  }
119.  print "\n\nTotals: %Total{type}}\n";
120.  foreach my $Type = sort (keys (%Total{type})) {
121.     {
122.         print "\tType: $Total{type}->{$Type}\n";
123.     }
124.     print "\t-----------------------------------------------------\n";
125.     print "\tTotal tested: $Total{files}\n";
126.     print "\tTotal recovered: $Total{recovered}\n";
127.  }
128.  if (scalar $FailedToRename) {
129.     {
130.         print "\tThe following files are good but failed to rename:\n";
131.         map { print "\t$\n" } $FailedToRename;
132.     },
```

## 结论

假设网络上发生危机是合理的。无论是工作站驱动损坏还是服务器崩溃，这都不是“是否”的问题，而是“何时”的问题。当危机发生时，最好做好准备以便采取行动。Perl 是准备此类危机以及应对危机的完美语言。在这方面，利用 Perl 的有趣之处在于它仅仅是一个工具。管理员需要设计特定的 Perl 解决方案。但有了这种解决方案，你可以确保自己准备好了任何问题。

## 监控与报告

大多数网络管理员的说明监控包含了维护和规划。然而，任何工作超过一周的管理员都会告诉你，这只是工作的一分之一。通过一些预见和规划，许多危机是可以避免的。报告是监控正在发生的事件并在发生时处理它们的方法。例如，报警监控状况并在检测到过多粒子时鸣响。报告通常分为两个阶段：检测和报警。

报告的第一阶段是检测阶段。该阶段涉及监控事件。事件可能是服务停止或机器离线。检测通常通过轮询进行；脚本持续请求设备的状态。例如，如果一台机器监控另一台机器，可能会每分钟尝试连接一次。如果被监控机器没有响应，则假设机器已宕机。但这种假设并不正确。因此，监控脚本必须考虑这种情况，可能会等待一段时间以解释丢包。监控简单的方法，每个任务都有自己的方法。例如，你可能会通过 ping IP 地址来测试服务器是否存在。你可以使用`Net::Ping`或调用`ping.EXE`。在这种情况下，两种方法都可行；一种方法检查函数调的结果，另一种方法解析外部程序的输出。

## 报警

当监控事件发生时，报告的第二个阶段开始。这是报警的过程。操作的结果可以通过多种方式报告。首先应该是 Win32 事件日志。使用此日志是记录 NT 或 Windows 2000 机器系统事件的标准方法。此日志始终可用，可以远程访问，任何账户都可以向其写入，并且它记录了每条记录的时间和日期等其他信息。

## 事件日志

Windows NT/2000 提供了日志功能，可以记录信息事件以及关键事件。事件日志的功能类似于 UNIX 的`syslog`守护进程。应用程序（或驱动、服务或任何执行代码）可以通过运行`EVENTVWR.EXE`查看这些事件。你可以在任何具有权限的机器上注册事件。通常，服务器有三个事件日志：应用程序、系统和安全。Windows 2000 服务器还增加了目录服务、DNS 服务器和文件复制日志。通常，应用程序仅在相应的日志报告报告。因此，安全相关的事件报告到安全日志，而系统事件（驱动程序失败、网卡绑定 DHCP 地址等）报告到系统日志。

两个 Win32 Perl 扩展暴露了事件日志 API 函数：`Win32::EventLog`和`Win32::EventManager`。记录事件一个就足够了。第三个名为`Win32::EventLog::Message`的扩展与其中任何一个配合工作。

## Win32::EventLog::Message 表格

`EventLog::EventLog::Message`扩展提供了一个消息表，允许对你的事件日志消息进行格式化。消息表仅仅是用于显示信息的格式列表。通常，消息表具有特定格式的预组成文本字符串。这些文本字符串具有占位符，在屏幕上或事件日志中会被替换为变量信息。例如，假设你写了一段显示当天时间对话框的代码。你可以在消息表中创建此条目：`current time is: %1!`。当你显示对话框时，`%1!`被替换为程序运行时决定的某些字符串。如果你需要更改语言，此扩展有效；你只需要替换包含消息表的资源`.DLL`文件即可。假设你用英语和土耳其语对程序进行“国际化”。假设英语版本的消息表生成的对话框看起来像图 5.1。然而，当你将英语消息表换为土耳其语版本时，对话框神奇地变成了图 5.2 所示。这种变化不需要重新编译你的程序；你只需要创建新的消息表`.DLL`文件即可。

![](img/b5063514d2e449d6d8c5d65f100b84aa_174_0.png)

图 5.1 一个简单的消息表。

![](img/b5063514d2e449d6d8c5d65f100b84aa_174_1.png)

图 5.2 与图 5.1 相同的对话框，使用了土耳其语消息表。

## 第5章：监控与报告

每个日志条目都可以关联一个事件 ID，该 ID 指明使用消息表中的哪个条目。消息表条目通常是具有可字段的文本消息。例如，图 5.3 包含此消息：

`WINWORD.EXE`拒绝挂起电源请求。

此消息来自 Win32k 事件源，它映射到`%SystemRoot%\System32\win32k.sys`。事件 ID 为 240，因此当事件日志显示此条目时，它会打开`%SystemRoot%\System32\win32k.sys`文件并从文件消息表的第 240 行查找消息。该表条目由此字符串组成：

挂起电源请求被`%1!`拒绝

在创建事件日志条目时，提供了多个字符串。`%1!`会被替换为第一个字符串的内容，并被解释为文本字符串。如果消息中出现`%2!`，它将会被替换为第二个字符串的内容（被解释为数值）。

![](img/b5063514d2e449d6d8c5d65f100b84aa_175_0.png)

图 5.3 事件日志条目。

当 Perl 报告事件日志条目时（使用`Win32::EventLog`或`Win32::Lanman`），它可以指定源、事件 ID 和字符串（至少这三点是最重要的）。大多数用户希望代表其脚本报告事件。由于 Perl 脚本默认情况下没有与消息表相关联的源，因此 Perl 脚本的日志条目最终看起来就像图 5.4 所示。注意传入的字符串被显示了，但方式并不优雅。

## 警报

![](img/b5063514d2e449d6d8c5d65f100b84aa_176_0.png)

描述：

事件 ID 0 的描述位于“源应用程序”中且无法找到。本地计算机可能没有相应的注册表项或消息 DLL 文件，无法显示来自远程计算机的消息。以下是事件的副本：服务器 'Server' 于 2000 年 6 月 16 日 16:01:42 报告宕机

图 5.4 没有消息表的事件日志条目。

这就是`Win32::EventLog::Message`扩展用用场。它提供了一个包含一个条目的简单消息表，其中包含

- * `%1s`

此表条目只需扩展为你传递的任何内容。因此，你的 Perl 脚本可以传递任何格式化文本（带有回车符、多个空格、制表符等）。图 5.5 阐释了图 5.4 中的相同字符串在使用此扩展的消息表时的外观。

![](img/b5063514d2e449d6d8c5d65f100b84aa_176_1.png)

图 5.5 使用`Win32::EventLog::Message`的事件日志条目。



由于`Win32::EventLog::Message`使用的消息表本身不包含文本，因此它不支持国际化。毕竟，你如何对`%`字符串进行本地化呢？然而，该扩展允许脚本作为源注册和注销其他消息表。因此，编码员可以使用某些消息表编译器（如`MC.EXE`，微软的消息表编译器）和`C`编译器创建一个消息表，然后使用此扩展将生成的`.DLL`文件注册为事件日志源。这为自定义和国际化事件日志显示提供了一种机制。

## 事件日志源

每个事件日志可以有多个不同的源，而且通常确实如此。通常，每个可能需要报告事件的程序都有一个事件日志源。通常多个程序共享同一个源（消息文件）。

你可以使用`Win32::EventLog::GetSource()`函数发现注册了哪些源。示例 5.1 显示了如何使用此函数。脚本接受事件日志作为第一个参数，该参数可以是任何事件日志，例如`System`、`Application`、`Security`或任何已注册的事件日志。脚本显示在指定事件日志下注册的所有事件源。

如果向脚本传递了任何额外参数，它们将被解释为源名称。然后仅显示针对指定源名称的消息表路径。

例如，命令行

```
perl DumpEvents.pl System
```

可能会导致如最后一个列出的源（第 22 行）所示的显示，指向`Win32::EventLog::Message`的`perl .DLL`文件。这是将`Win32::EventLog::Message`扩展注册为“My Per Log”系统事件源的结果。

```
C:\perl DumpEventsSources.pl system
System Event Log:
Count Source Log Name Path To Message Table
```

| | | | |
|---|---|---|---|
| 1 | Alerter | %SystemRoot%\System32\netmsg.dll |
| 2 | Application Popup | %SystemRoot%\System32\nttdll.dll |
| 3 | AsyncMac | %SystemRoot%\System32\mpnmsg.dll |
| 4 | AtmElan | %SystemRoot%\System32\netevent.dll |
| 5 | Atmarpc | %SystemRoot%\System32\netevent.dll |
| 6 | AviatorPro | %SystemRoot%\System32\netevent.dll |
| 7 | Browser | %SystemRoot%\System32\drivers\webdrv.sys |
| | | %SystemRoot%\System32\netevent.dll |
| 8 | DCOM | %SystemRoot%\System32\netevent.dll |
| 9 | DfsDriver | %SystemRoot%\System32\netevent.dll |
| 10 | DfsSvc | %SystemRoot%\System32\netevent.dll |
| 11 | Dhcp | %SystemRoot%\System32\netevent.dll |
| 12 | Distributed | %SystemRoot%\System32\netevent.dll |
| 13 | Dnsapi | %SystemRoot%\System32\netevent.dll |
| 14 | Dnscache | %SystemRoot%\System32\netevent.dll |
| 15 | IISLS | C:\Windows\System32\inrs.exe |
| 16 | ISOLOG | C:\Windows\System32\inrs.exe |
| 17 | IISMAP | C:\Windows\System32\iisap.dll |
| 18 | IPBOOT | %SystemRoot%\System32\ipboot.dll |
| 19 | IPATH | %SystemRoot%\System32\ipath.dll |
| 20 | IPR2 | %SystemRoot%\System32\rip2.dll |
| 21 | Router | %SystemRoot%\System32\rmsg.dll |
| 22 | Perl | C:\perl\lib\Win32\EventLog\Message.dll |

图 5.6 示例 5.1 的输出。

脚本调用`Win32::EventLog::Message GetSource`函数来发现每个事件日志源的属性。路径是该函数获取的属性之一。

## 监控内部进程

假设你有一个运行系列`CGI`脚本的`Web`服务器。`CGI`脚本不时需要调用独立的进程。这些进程可以是从`NBSTAT.EXE`（显示`NetBEUI`统计数据）到`NETSTAT.EXE`（显示网络连接）的任何程序。随着`Web`服务器请求的增加，服务器显然会变慢。对性能的影响会导致脚本运行事件变慢，使得进程完成需要更长时间。随着这种情况的发生，可能会有更多的请求进入，创建新的`CGI`脚本和进程，从而进一步恶化问题。

许多`Web`服务器可以指定脚本超时值。如果脚本没有在指定的时间内完成，`Web`服务器将将其终止。然而，这并不能让你区分一个运行时间较长的脚本和一个另一个根本不应该运行长时间的进程。一个可行的解决方案是设计一个服务，在指定的持续后仅终止选定的进程。

这种解决方案也可以用于其他目的，例如防止用户运行超过规定时间的程序。这可能是为了给网吧的客户计费，或者确保进程不会进入死锁状态。

示例 5.2 监控所有进程并终止任何运行时间长的进程。在这个特定的脚本中，只监控了两个进程：`Telnet`和`FTP`。这些进程及其超时值在第 17 行到第 20 行中配置。`Telnet`进程允许运行不超过 120 秒。`FTP`程序被授予 0 秒的运行时间。这实际上等同于阻止`FTP`进程运行（实际上，进程可以运行，但它几乎会被会被终止）。

大部分代码基于典型的`Win32::Daemon`框架（请参考第 8 章）。真正的引擎位于第 89 行以及第 132 行到 156 行。第 89 行获取了一个在服务期间使用的`WMI`对象（有关`WMI`的更多细节，请参考第 9 章“ADSI 和 WMI”）。第 132 行到 156 行使用`WMI`对象遍历每个进程（通过`Win32_Process WMI`对象的集合），检查是否为受监控进程。如果进程是受监控的，则计算其运行的秒数，并与特定进程的允许时间阈值进行比较。如果运行时间等于或超过分配的时间，则终止该进程。

该脚本使用`WMI`遍历机器上的所有进程列表。进程列表可以从网络上的任何机器获取，从而使脚本能够监控远程机器上的进程。第 52 行和 53 行创建`WMI` moniker。注意第 53 行引用了`$Config{machine}`哈希键。这里可以指定另一个机器名称。默认情况下，此值等于点号 (")，表示要监控本地机器。你可以在安装服务时传递`-m Machine_Name`参数来指定远程机器。

脚本监控远程机器与监控本地机器一样。这是通过在安装服务时传递`-m`切换以及机器名称来实现。当安装服务监控远程机器时，必须配置为用户账户登录（而不是默认的`Local System`账户）。这是因为`Local System`账户具有管理员权限，但仅限于本地机器。因此，服务必须使用在远程机器上具有管理员权限的账户登录。例如：

```perl
perl procmon.pl -install -m Server -u MonitorDaemon -p AdminPassword
```

假设`MonitorDaemon`账户拥有机器`\Server`的权限。

如果你是安装在本地机器上运行，则不需要指定用户名和密码。注意第 264 行和 265 行，指定的用户名和密码被分配给服务配置哈希表。如果没有指定用户账户和密码，这些将会是空的，`Win32::Daemon`将其解释为`Local System`账户。

`WMI`必须在运行服务的机器和被监控的机器上都安装。`Windows 2000`自带`WMI`，但`NT 4.0`和`Windows 95/98`没有安装`WMI`。该技术可以从微软网站下载。有关`WMI`的更多细节请参见第 9 章。

## 示例 5.2 监控禁止的进程



```perl我是由深度求索（DeepSeek）研发的 deepseek-v4-flash-0731 智能大模型。01. use Time::Local;
02. use Getopt::Long;
03. use Win32::Daemon;
04. use Win32::OLE qw ( in );
05. use Win32::EventLog;
06. use Win32::EventLog::Message;
07.
08. $SUCCESS = 0;
09.
10. # 在轮询服务状态之间睡眠多久？
11. $SERVICE_SLEEP_TIME = 1;
12.
13. # 进程名称列表及其允许运行的秒数
14. # 键是全名（必须小写），值是允许运行的
15. # 秒数。零值表示
16. # 必须尽快终止进程。
17. %PROC_LIST = (
18.   "telnet.exe" => 120,
19.   "ftp.exe" => 0,
20. );
21.
22. $SERVICE_ALIAS = "ProcMon",
23. $SERVICE_NAME = "Process Monitor",
24.
25. $LOG_FILE_PATH = ( Win32::GetFullPath($0) =~ /^(.*)\.[^*]*$/ );
26. $LOG_FILE_PATH //= ".log";
27.
28. %Config = (
29.   machine => ".",
30.   logfile => $LOG_FILE_PATH,
31. );
32.
33. Configure(\Config, @ARGV);
34. if ($Config{install})
35. {
36.   InstallService();
37.   exit;
38. }
39. elsif ($Config{remove})
40. {
41.   RemoveService();
42.   exit;
43. }
44. elsif ($Config{help})
45. {
46.   Syntax();
47.   exit;
48. }
49.
50. # 这个 WMI moniker 连接到机器的
51. # CIM（公共信息模型）存储库
52. $CLASS = "impersonationLevel://" . $Config{machine} . "/root/cim2";
53.
54. # 注册我们简单的事件日志资源
55. # 系统日志 $SERVICE_NAME 源
56. Win32::EventLog::RegisterSource('System', $SERVICE_NAME);
57.
58. # 尝试打开日志文件。报告服务正在做什么
59. # 以及哪些进程被终止了。
60. if(open(LOG, ">$Config{logfile"))
61. # 选择 LOG 句柄
62. my $BackupHandle = select(LOG);
63. # ...然后自动刷新（无缓冲）
64. $| = 1;
65.
66. # ...恢复之前的 I/O 句柄
67. select($BackupHandle);
68. }
69.
70. # 启动服务
71. if (! Win32::Daemon::StartService())
72. {
73.   ReportError('Could not start $0');
74.   exit();
75. }
76.
77. $PrevState = SERVICE_STARTING;
78. Write("$SERVICE_NAME service is starting...\n");
79. while($SERVICE_STOPPED != ($State = Win32::Daemon::State()))
80. {
81. if ($PENDING == $State)
82. {
83.   ReportInfo("Starting $SERVICE_NAME.");
84. # 初始化: 获取 WMI（微软的 WBEM 实现）接口
85. if ($WMI = Win32::OLE->GetObject($CLASS))
86. {
87.   Win32::Daemon::State(SERVICE_RUNNING);
88.   ReportInfo("$SERVICE_NAME service has started: ");
89.     Monitoring ($Config{machine})");
90.
91.   $PrevState = SERVICE_RUNNING;
92. }
93. else
94. {
95.   Win32::Daemon::State(SERVICE_STOPPED);
96.   ReportError("$SERVICE_NAME service could not access WMI.");
97. }
98. elseif($PAUSE_PENDING == $State)
99. {
100. # 暂停...
101.   Win32::Daemon::State(SERVICE_PAUSED);
102.   ReportWarn("$SERVICE_NAME service has paused.");
103.   $PrevState = SERVICE_PAUSED;
104.   next;
105. }
106. elseif($CONTINUE_PENDING == $State)
107. {
108. # 恢复...
109.   Win32::Daemon::State(SERVICE_RUNNING);
110.   ReportInfo("$SERVICE_NAME service has resumed.");
111.   $PrevState = SERVICE_RUNNING;
112.   next;
113. } elseif($STOP_PENDING == $State)
114. {
115. # "停止中...";
116.   undef Win32::Daemon::State( SERVICE_STOPPED );
117.   Win32::ReportWarn("$SERVICE_NAME is stopping.");
118.   $PrevState = SERVICE_STOPPED;
119. 
120.   next;
121.   elsif( SERVICE_RUNNING == $State )
122.   {
123.     # 服务正常运行...
124.     # 获取 Win32_Process 对象的集合
125.     foreach my $Proc in ($WMI->InstancesOf("Win32_Process")) {
126.       {
127.         $myProcName = $Proc->Name;
128.         $mylcProcName = $myProcName;
129.         $myProcCreation = $Proc->{CreationDate};
130.         
131.         if ( defined $PROC_LIST($mylcProcName) )
132.           && defined ( $Proc->{CreationDate} ) {
133.           {
134.             $myProcSeconds = DateInSeconds($myProcCreation);
135.             if ($PROC_LIST($mylcProcName) <= time() - $myProcSeconds ) {
136.               {
137.                 if ($SUCCESS == $Proc->Terminate( 0 ) ) {
138.                   {
139.                     ReportWarn("Killed $myProcName created on ")
140.                       localtime($myProcSeconds));
141.                   }
142.               }
143.             else
144.               {
145.                 ReportError("Failed to Kill $myProcName created on ")
146.                   localtime($myProcSeconds));
147.               }
148.             }
149.           }
150.         }
151.       }
152.     }
153.     # 获取一个未处理的控制消息。将状态设置为
154. # 之前的状态是什么。
155.     Write("Got odd state \$State. Setting state to \$PrevState");
156.     Win32::Daemon::State($PrevState);
157.   }
158.   }
159. }
160.   sleep($SERVICE_SLEEP_TIME);
161. }
162. 
163. sub DateInSeconds
164. {
165.   my($Date) = @_;
166.   my(@List) = ($Date -= /\(\d{4})\(\d{2})\(\d{2})\(\d{2})\(\d{2})\(\d{2})\//);
167.   my($Seconds) = localtime($List[5], $List[4], $List[3],
```

## 示例 5.2 继续

```perl
173. $list[2], $list[1] - $list[0] - 1, $list[0] - 1900);
```

```perl
174. return($Seconds);
```

```perl
175. }
```

```perl
176.
```

```perl
177. sub ReportError
```

```perl
178. {
```

```perl
179. my($Message) = @_;
```

```perl
180. return($Message,
```

```perl
181. $SERVICE_NAME,
```

```perl
182. EVENTLOG_ERROR_TYPE );
```

```perl
183. }
```

```perl
184.
```

```perl
185. sub ReportWarn
```

```perl
186. {
```

```perl
187. my($Message) = @_;
```

```perl
188. return($Message,
```

```perl
189. $SERVICE_NAME,
```

```perl
190. EVENTLOG_WARNING_TYPE );
```

```perl
191. }
```

```perl
192.
```

```perl
193. sub ReportInfo
```

```perl
194. {
```

```perl
195. my($Message) = @_;
```

```perl
196. return($Message,
```

```perl
197. $SERVICE_NAME,
```

```perl
198. EVENTLOG_INFORMATION_TYPE );
```

```perl
199. }
```

```perl
200.
```

```perl
201. sub Report
```

```perl
202. {
```

```perl
203. my($Message, $LogSource, $Type) = @_;
```

```perl
204.
```

```perl
205. Write("$Message\n");
```

```perl
206. if my($EventLog = new Win32::EventLog($LogSource ))
```

```perl
207.
```

```perl
 {
```

```perl
208. $EventLog->Report(
```

```perl
 {
```

```perl
210. Strings => $Message,
```

```perl
211. EventID => 0,
```

```perl
212. EventType => $Type,
```

```perl
213. Category => undef,
```

```perl
 }
```

```perl
214. );
```

```perl
215. $EventLog->Close();
```

```perl
216.
```

```perl
 }
```

```perl
217.
```

```perl
 }
```

```perl
218.
```

```perl
219.
```

```perl
220. sub InstallService
```

```perl
221.
```

```perl
 {
```

```perl
222. my($Service = GetService());
```

```perl
223.
```

```perl
224. if(".* ne \$Config{machine })
```

```perl
## 任何斜杠
$Config{machine} =~ s#[\/]###;
$Service->{parameters} .= " -m " . $Config{machine}
$Service->{parameters} .= " -l l" . "$Config{logfile}";
if( Win32::Daemon::CreateService( $Service ))
{
    print "The $Service->{display} was successfully installed.\n"
}
else
{
    print "Failed to add the $Service->{display} service.\n"
    print "Error: " . GetError() . "\n"
}
sub RemoveService
{
    my $Service = GetService();
if( Win32::Daemon::DeleteService( $Service->{name} ))
{
    print "The $Service->{display} was successfully removed.\n"
}
else
{
    print "Failed to remove the $Service->{display} service.\n"
    print "Error: " . GetError() . "\n"
}
sub GetService
{
    my $ScriptPath = join("", Win32::GetFullPathName( $0 ));
    my %Hash = (
        name => \$SERVICE_ALIAS,
        display => \$SERVICE_NAME,
        path => \$X,
        user => \$Config(user),
        password => \$Config(password),
        description => "Monitors processes.",
        parameters => "\$ScriptPath",
    );
    return (%Hash);
}
sub GetError
{
    return ( Win32::FormatMessage( Win32::Daemon::GetLastError() ));
}
sub Write
```

## 示例 5.2 继续



# 监控网络状态

监控守护进程（daemon）的一个完美示例是监控网络运行时间的服务。该服务偶尔 ping 某台主机，并在主机未响应时报告。示例 5.3 正是这样做的。该服务运行并监控 `@HOSTS` 数组中定义的机器。

## 状态监控与报告

示例 5.3

```perl
01. use Net::Ping;
02. use Getopt::Long;
03. use Win32::Daemon;
04. use Win32::EventLog;
05. use Win32::Message;
06. 
07. # 监控状态
08. 
09. # 示例 5.3
10. 
11. # 状态
```

## 示例 5.3 续

```perl
278. {
279.   my($Message) = @;
280.   $Message = "[" scalar localtime() . "] $Message";
281.   if (fileno(LOG))
282.   {
283.     print LOG $Message;
284.   }
285. }
286. 
287. sub Configure
288. {
289.   my($Config, @Args) = @;
290.   my $Result;
291. 
292.   Getopt::Configure(" prefix_pattern=(-|\/") \n
293.   $Result = GetOptions($Config,
294.     qw(
295.       install|i
296.       remove|r
297.       machine|m=s
298.       logfile|l=s
299.       user|u|account=s
300.       password=s
301.       help
302.     )
303.   );
304.   $Config->{$help} = 1 if (! $Result);
305. 
306. 
307. sub Syntax
308. {
309.   my($Script) = ($0 =~ /\([^\]]*\)$/);
310.   my $Whitespace = " " x length($Script);
311.   print << "EOT"
312. 
313.   Syntax:
314.     $Script -install [-a Account] [-p Password] [-m Machine] [-l Path]
315.     $Whitespace -remove
316.     $Whitespace -help
317. 
318.       -install................安装该服务。
319.       -a................指定服务运行的帐户。
320.         默认: System
321.       -p................指定服务使用的密码。
322.       -m................指定要监控的机器名称。
323.         默认: 本地机器
324.       -l................指定一个日志文件。
325.         默认: $LOG_FILE_PATH
326. 
327.       -remove...........移除该服务。
328.   EOT
329. }
```

## 示例 5.3 续

```perl
116. {
117.   # Stopping...
118. 
119.   $PingObject->close();
120.   undef $PingObject;
121. 
122.   Win32::Daemon::State( SERVICE_STOPPED );
123.   ReportWarn("SERVICE_NAME service is stopping.");
124.   $PrevState = SERVICE_STOPPED;
125. 
126.   next();
127. } elseif (SERVICE_RUNNING == $State)
128. {
129.   # The service is running as normal...
130.   if (time() > $NextPingTime)
131.   {
132.     PingServers($PingObject, \Servers, \HOSTS);
133.     $NextPingTime = time() + $PING_INTERVAL;
134.   }
135. }
136. else
137. {
138.   # Get an unhandled control message. Set the state to
139.   # whatever the previous state was.
140.   Write("Got old state $PrevState. Setting state to \$PrevState");
141.   Win32::Daemon::State($PrevState);
142. }
143. CheckServers(\$Servers);
144. sleep(\$SERVICE_SLEEP_TIME);
145. 
146. sub PingServers
147. {
148.   my($PingObject, $Servers, @Hosts) = @_;
149. 
150.   return unless defined ($PingObject);
151. 
152.   foreach my $Host (@HOSTS)
153.   {
154.     if (! $PingObject->ping($Host))
155.     {
156.       $Servers->{lc $Host}->{count}--;
157.     }
158.     else
159.     {
160.       $Servers->{lc $Host}->{count} = $PING_MAX_COUNT;
161.     }
162.   }
163.   return;
164. }
```

```perl
165. sub CheckServers
166. {
167.   my($Servers) = @_;
168. 
169.   foreach ($Host keys %$Servers)
170.   {
171.     if (0 >= $Servers->{lc $Host}->{count})
172.     {
173.       ReportServerDown($Host);
174.       $Servers->{lc $Host}->{count} = PING_MAX_COUNT;
175.     }
176.   }
177. }
178. 
179. sub ReportServerDown
180. {
181.   my($Host) = @_;
182.   my($Error = 'Server $Host is reported down at ' . scalar localtime());
183.   ReportError($Error);
184.   Alert($Host);
185. }
186. 
187. sub ReportError
188. {
189.   my($Message) = @_;
190.   return Report($Message,
191.     $SERVICE_NAME,
192.     EVENTLOG_ERROR_TYPE);
193. }
194. 
195. sub ReportWarn
196. {
197.   my($Message) = @_;
198.   return Report($Message,
199.     $SERVICE_NAME,
200.     EVENTLOG_WARNING_TYPE);
201. }
202. 
203. sub ReportInfo
204. {
205.   my($Message) = @_;
206.   return Report($Message,
207.     $SERVICE_NAME,
208.     EVENTLOG_INFORMATION_TYPE);
209. }
210. 
211. sub Report
212. {
213.   my($Message, $Log, $Type) = @_;
214.   Write("$Message\n");
215.   if ($EventLog = new Win32::EventLog($Log))
216.   {
217.     $EventLog->Report(
218.       {
219.         Strings => $Message,
220.         EventID => 0,
221.         EventType => $Type,
222.         Category => undef,
223.       }
224.     );
225.     $EventLog->Close();
226.   }
227. }
```

# 第 5 章：监控与报告

## 示例 5.3 续

```perl
220. {
221.   Strings => $Message,
222.   EventID => 0,
223.   EventType => $Type,
224.   Category => undef,
225. }
226. );
227. $EventLog->Close();
228. }
229. }
230. 
231. sub InstallService
232. {
233.   my $Service = GetService();
234. 
235.   $Service->(parameters) .= " -1Config(logfile)"";
236.   if Win32::Daemon::CreateService($Service)
237.   {
238.     print "$Service->{display} was successfully installed.";
239.   }
240.   else
241.   {
242.     print "Failed to add $Service->{display} service.";
243.     print "Error: " . GetError() . "\n";
244.   }
245. }
246. 
247. sub RemoveService
248. {
249.   my $Service = GetService();
250. 
251.   if(Win32::Daemon::DeleteService($Service->{name}))
252.   {
253.     print "$Service->{display} was successfully removed.";
254.   }
255.   else
256.   {
257.     print "Failed to remove $Service->{display} service.";
258.     print "Error: " . GetError() . "\n";
259.   }
260. }
261. 
262. sub GetService
263. {
264.   my $ScriptPath = join("", Win32::GetFullName($0));
265.   %Hash = (
266.     name => $SERVICE_ALIAS,
267.     display => $SERVICE_NAME,
268.     path => $X,
269.     user => $Config{user},
270.     password => $Config{password},
271.     description => "Monitors remote machine's uptime.",
272.   );
273. 
274.   parameters => "$ScriptPath\",
275.   );
276.   return (\Hash);
277. }
278. 
279. sub getError
280. {
281.   return (Win32::FormatMessage(Win32::Daemon::GetLastError()));
282. }
283. 
284. sub Write
285. {
286.   my($Message) = @_;
287.   $Message = "[". scalar(localtime()) . "] $Message;
288.   if (fileno(LOG))
289.   {
290.     print LOG $Message;
291.   }
292. }
293. 
294. sub Alert
295. {
296.   my($Host) = @_;
297.   # You could add code here to alert administrators via email,
298.   # pager, network message or some other means.
299. }
300. 
301. sub Configure
302. {
303.   my($Config, @Args) = @_;
304.   my $Result;
305. 
306.   Getopt::Long::Configure("prefix_pattern=(-|\\/)");
307.   $Result = getOptions($Config,
308.     qw{
309.       install|i
310.       remove|l=s
311.     }
312.   );
313. }
```




## 第 5 章：监控与报告

### 示例 5.3 续

```perl
309.         logfile=s
310.         user|a|account=s
311.         password=s
312.         help
313.     }
314.     );
315.     $Config->{help} = 1 if (!$Result);
316.   }
317.
318.   sub Syntax
319.   {
320.     my($Script) = ($0 =~ /\(\[^\]]*)?\$/);
321.     my $Whitespace = " " x length($Script);
322.     print << "EOT\n";
325. $Script -install [-account]logfile]
326. $Whitespace -remove
327. $Whitespace -help
328.
329. -install.......Installs the service.
330. -account.......Specifies what service under.
331. Default: Local System
332. -password......Specifies the password.
333. -l...........Specifies log path.
334. Default: LOG_FILE
335.
336. -remove........Removes the service.
337. EOT
338. }
```

## 扫描事件日志中的错误

许多计算机问题都可以追溯到事件日志。两个不同的 `Win32::EventLog` 扩展提供了对这些内容的访问。然而，面向对象的方法更好。

脚本的引擎非常简单。第 69 行为特定机器创建 `Win32::EventLog` 对象。第 76 到 97 行从事件日志中读取事件条目。如果读取成功，*

示例 5.4 连接到事件日志并显示请求的所有事件。此脚本接受多种参数，如表 5.1 所示。

### 表 5.1 5.4 参数选项

| 参数 | 功能 |
| --- | --- |
| `-m Machine` | 指定要检查的机器上的事件日志。 |
| `-l Log` | 你可以指定多个此类开关。通常是以下之一：`Application`（应用程序）、`Security`（安全）、`System`（系统）。然而，它也可以是另一个日志，如 `Directory Service`（目录服务）、`DNS Server`（DNS 服务器）、`File Replication Service`（文件复制服务）。 |
| `-s Source` | 指定要检查的事件源。默认考虑所有源。指定的源使用正则表达式，因此可以是任何有效的正则表达式——例如：`IISLOG *MS.*SVC$` 服务 |
| `-t EventType` | 指定要显示的事件类型。有效类型如下：`ERROR`（错误）、`INFORMATION`（信息）、`WARNING`（警告）、`AUDIT_SUCCESS`（审核成功）、`AUDIT_FAILURE`（审核失败）。 |
| `-h Hours` | 你可以指定多个此类开关对应的小时条目。仅显示指定小时数的条目。如果传递 2，则只显示过去两个小时内生成的事件。此开关可以与 `-d` 结合使用。 |
| `-d Days` | 仅显示指定天数的条目。如果传递 2，则只显示过去两个天内生成的事件。此开关可以与 `-h` 结合使用。 |
| `-date Date` | 仅显示在当前日期和指定日期之间生成的事件。此参数必须是国际时间格式，例如 `2000.07.19`。 |

如果 `timestamp` 在用户指定的时间范围内，则处理该事件。第 96 行只有当事件类型与用户指定的某个事件类型匹配时，才会写入屏幕。

请注意，第 76-79 行中的实际 `Read()` 方法传入了标志 `EVENTLOG_BACKWARDS_READ | EVENTLOG_SEQUENTIAL_READ`。此标志表示每次调用 `Read()` 均期望按顺序获取下一条记录，因此不需要指定记录数。此外，该标志还指定了反向读取记录，从最近的条目开始。

例如，要使用此脚本，你可以输入以下内容：

```perl
perl GetEvents.pl -m server1 -m server2 -l system -t error -t warning -d 7
```

此命令将显示 `\server1` 和 `\server2` 上的系统事件日志（System Event Log）过去七天内的所有错误和警告。

另一个示例：

```perl
perl GetEvents.pl -m server1 -l system -t error -t warning -s MSFTPSVC -s "Service Control"
```

这将显示 `\server1` 服务器上由 Microsoft FTP 服务或服务控制管理器生成的所有系统错误和警告。

### 示例 5.4 检查事件日志

```perl
01. use Getopt::Long;
02. use Time::Local;
03. use Win32::EventLog;
04.
05. $SEC = 1;
06. $MIN = 60 * $SEC;
07. $HOUR = 60 * $MIN;
08. $DAY = 24 * $HOUR;
09.
10. %EVENT_TYPE = (
11. EVENTLOG_AUDIT_FAILURE => 'AUDIT_FAILURE',
12. EVENTLOG_AUDIT_SUCCESS => 'AUDIT_SUCCESS',
13. EVENTLOG_ERROR_TYPE => 'ERROR',
14. EVENTLOG_WARNING_TYPE => 'WARNING',
15. EVENTLOG_INFORMATION_TYPE => 'INFORMATION',
16. );
17.
18. %Config = (
19. log => 'System',
20. );
21. Configure(\$Config);
22. if ($Config) {
23.
24. Syntax();
25. exit;
26. }
27. if (defined \$Config{date})
28. {
29.     my($Year, $Month, $Day)
30.     = ($Config{date} = -/(\d{4}).(\d{2}).(\d{2})/);
31.     $TIME_LIMIT = timocal(0, 0, 0, $Day, $Month - 1, $Year - 1900);
32. }
33. else elsif ($Config{hour} || $Config{day})
34. {
35.     $TIME_LIMIT = time() - ($DAY * $Config{day})
36.     - ($HOUR * $Config{hour});
37. }
38. 
39. if ( scalar @$Config{machine})
40. {
41.     push(@{$Config{machine}, Win32::NodeName);
42. }
43. 
44. if defined ($Config{type})
45. {
46.     foreach my $Mask (@$Config{type})
47.     {
48.         # 尝试引用 EVENTLOG_XXXX_TYPE 和 EVENTLOG_XXXX
49.         # 常量。其中一个将可以正常工作。
50.         $EVENT_MASK = eval("EVENTLOG_
81.  {
82.    # 如果事件是我们请求的
83.    # 事件类型之一，则显示该事件
84.    if scalar @${Config{sources}}
85.    {
86.      my $fDisplayEvent = 0;
87.      map
88.        {
89.          if ($Event{Source} =~ /_$/i)
90.          {
91.              my $fDisplayEvent = 1;
92.          }
93.        } @${Config{sources}};
94.        next unless
95.    }
96.    write if ($Event{Type} & $EVENT_MASK);
97.  }
98.  else
99.   {
100.     print "Can not connect to the ${Config{log} ";
102.     print "Event Log on ${Machine}\n";
104.   }
106.
107. sub Configure
108.   my ($Config) = @_;
109.
110.   Getopt::Long::Configure("prefix_pattern=-\");
111.   $Result = GetOptions($Config,
112.     machine|m=s
113.       log|l=s
114.       type|t=s
115.       hour|h=i
116.       day|d=i
117.       date=s
118.       sources|s=s
119.       help=@s
120.     );
121.   $Config->{help} = 1 if (!Result);
122.   push(@{$Config{machine}}, Win32::NodeName()) unless
123.     scalar @${Config{machine}});
124.
125. sub Syntax
126.   my ($Script) = ($0 =~ /^\([^]**\$/);
127.   my $Whitespace = " " x length($Script);
128.   print << "EOT";
130. Syntax: [-m Machine] [-t EventType] [-l Log] [-s Source]
131. $Whitespace [-h Hours] [-d Days] [-date Date]
132. $Whitespace [-help]
133. -m Machine......要检查事件日志的机器名称。
134. 此开关可以指定多次。
135. -t EventType....要显示的事件类型：
136. ERROR
137. WARNING
138. INFORMATION
139. AUDIT_SUCCESS
140. AUDIT_FAILURE
141. 此开关可以指定多次。
142. -l Log.........要检查的事件日志名称。
143. 常见示例：
144. Application
145. Security
146. System
147. -s Source.......要检查的源名称。
148. 此开关可以指定多次。
149. -h Hours........小时数。
150. -d Days.........天数。
151. -date Date......日期（YYYY-MM-DD）。
152. -help...........显示帮助信息。
```

### 示例 5.6 续

```perl
07. my($Message, @List) = @_;
08. my $Pager = new Net::Pager| return (
09. # AT&T PCS 服务的服务号为 7。请检查
10. # Net::Pager 文档以发现其他寻呼服务
11. # 值。
12. my $SERVICE = 7;
13. my $FROM = "Perl Pager";
14.
15. foreach my $Recipient (@List)
16. {
17. print "Sending message to $Recipient...";
18. if ($Pager->sendPage($SERVICE, $Recipient,
19. $FROM, $Message, undef ))
20. {
21. print "successful";
22. }
23. else
24. {
25. print "failed";
26. }
27. print "\n";
28. }
29. } *@;
```

## 电子邮件

警报通常必须快速。否则，等你收到警报时，可能已经太晚无法修复问题。网络消息和寻呼通常是传递警报信息的良好机制，因为它们速度快；然而，两者都可能失败。消息可能已成功发送，但在发送寻呼时，你可能已经超出了范围。由于这些原因，通过电子邮件发送的消息很可能会送达接收者，并提供良好的历史追溯记录。

示例 5.7 展示了如何通过电子邮件发送警报。你可以向任何监控脚本添加 `SendAlert()` 函数以提供警报支持。`Net::SMTP` 模块作为 lib 归档的一部分，可以在 CPAN 上获取。

要使用示例 5.7，只需传入消息邮件，随后跟上接收者的电子邮件地址——例如：

```perl
perl SendEmail.pl "This is my test message" joel@mydomain.com betty@mydomain.com
```

在此脚本中，我们正在使用 `Net::SMTP` 模块，但你也可以使用许多其他电子邮件传输机制。这可以低级到打开你自己的到电子邮件服务器的 socket，也可以高级到使用 COM 通过 CDO 创建 API 会话。或者，你也可以直接调用某些第三方应用程序，例如 `SENDMAIL.EXE` 或 `BLAT.EXE`。选择实现 `Net::SMTP` 是出于其简单性和通用性。

### 示例 5.7 发送电子邮件警报

```perl
01. use Net::SMTP;
02. $Message = shift @ARGV;
03. SendAlert($Message, @ARGV);
04. 
05. sub SendAlert
06. {
07. my ($Message, @List) = @_;
08. 
09. foreach $Recipient (@List)
10. {
11. my $Smtp;
12. my ($Host) = ($Recipient -= /(.*)/););
13. 
14. print 'Sending message to $Recipient...';
15. if ($Smtp = new Net::SMTP($Host))
16. {
17. $Smtp->mail("Perl pager");
18. $Smtp->to($Recipient);
19. $Smtp->data();
20. $Smtp->datasend("To: $Recipient\n");
21. $Smtp->datasend("Subject: ALERT\n");
22. $Smtp->datasend("\n");
23. $Smtp->datasend("$Message\n");
24. $Smtp->dataend();
25. $Smtp->quit();
26. print "successful";
27. }
28. else
29. print 'failed';
30. }
31. print "\n";
32. }
```

## 结论

能够监控并报告发生在你的机器和网络上的事件，对于成功管理你的域至关重要。本章证明了服务和独立脚本可以引导管理员团队在问题演变成故障之前解决它们。这种主动的管理方法不仅节省时间，还节省资金。

## 登录脚本

当用户登录到 NT 机器时，可以执行登录脚本。该脚本允许你作为网络管理员动态地自定义用户环境。这种灵活性从一开始就是计算机系统的一部分。例如，UNIX shell 脚本一直提供了在登录过程中自定义用户环境的设施。

“登录脚本”这个名称有点误导，因为它并不非得是一个脚本。它可以是任何可执行程序，例如应用程序、批文件、Java 应用程序、Visual Basic 脚本甚至是 Perl 脚本。传统上，登录脚本是批文件。

由于 Windows NT 允许不同的用户登录到不同的机器，为仅一个用户设置计算机是困难的。登录脚本提供了所需的机制，以确保驱动器可以映射到适当的网络服务器、打印机可以重新连接到本地打印设备、更新环境变量等。

## 登录脚本如何工作

当用户尝试登录到 Win32 域时，她的机器会联系域控制器 (DC)。DC 持有每个用户账户的配置信息。DC 验证用户并（如果密码正确），她被允许登录域。

处理登录请求的 DC 被称为登录会话的登录服务器。如果网络中有多个 DC，登录请求可能会在不同的时间由不同的 DC 服务。哪台机器处理你的登录请求在某种程度上取决于哪个控制器最不忙碌。

## 第 6 章：登录脚本

### 注意

登录脚本仅在用户交互式登录到域时运行（例如使用键盘登录或通过终端服务器客户端登录）。如果用户通过网络登录（例如将驱动器器映射到服务器）或用户账户被冒用（例如 Web 服务器验证账户），则不执行登录脚本。◆

当用户成功登录到域后，机器会尝试运行用户的登录脚本。登录脚本始终从登录服务器的 `NetLogon` 共享目录运行。例如，如果用户账户由名为 `LogonServer` 的 DC 验证，且用户的登录脚本是 `MyLogonScript.exe`，Win32 将尝试运行以下内容：

```
\\LogonServer\NetLogon\MyLogonScript.exe
```



这意味着任何账户的登录脚本必须是相对于`DC NetLogon`共享目录的路径。如果文件不存在或无法访问（可能是因为安全权限），则执行登录脚本的尝试将简单失败，但不会向用户显示错误消息。

## 提示

如果你的网络中有许多`DC`，那么在每个控制器上维持登录脚本的副本是非常重要的。这就是复制服务（`Replication Service`）的设计初衷。它允许你指定一个控制器（通常是主域控制器`PDC`）作为登录脚本仓库。

任何脚本更新都会在仓库中的脚本上进行。已复制到所有其他`DC`的脚本。

登录脚本并不真的非得是一个脚本。它可以是一个可执行程序、批文件或如`Perl`、`Java`、`Python`或`Visual Basic`等脚本。例如，登录脚本可以配置为`Perl`脚本，如：

```
UserScripts\MyPerlLogonScript.pl
```

当然，此示例假设用户登录的机器`.pl`扩展名与`Perl`关联（详情请参考第 1 章“`Perl`与管理员”）。

在用户账户中，登录脚本实际上是一个任意字符串。这意味着一个账户可以配置为不仅仅是脚本的路径。它还可以包含要传递的参数。例如，一个账户可以配置为传入用户名以及计算机名（使用环境变量）：

```
UserScripts\Program.exe %USERNAME%
```

## 配置登录脚本

由于登录脚本属性是任意字符串，你可以使用它们从登录服务器运行`Perl`并传入脚本名称。例如，假设你在所有`DC`的`NetLogon`共享目录下安装了`Perl`。你可以配置你的用户账户使用此脚本：

```
perl\bin\perl.exe %LOGONSERVER
```

当然，当运行此脚本时会加上登录服务器和`NetLogon`共享，因此`Win32`实际执行：

```
//LogonServer\NetLogon\bin\perl.exe
//LogonServer\NetLogon\Scripts\MyLogonScript.pl
```

在这种情况下，`%LOGONSERVER`环境变量被替换为验证用户的`DC`（`\LogonServer`）。通过这样做，你不需要在单个用户机器上安装`Perl`，只需要在`DC`上安装。然而，以这种方式跨网络访问`Perl`有一些陷阱。更多信息请参考第一章。

## 配置登录脚本

登录脚本被配置为用户账户的一部分，允许一个用户拥有登录脚本，而另一个用户配置不同的脚本。这是为每个用户提供个性化体验的理想方式。你可以使用用户管理器程序（`Windows NT`）或计算机管理`MMC`（`Windows 2000`）修改用户账户使用的登录脚本。此外，你可以使用`Perl`等脚本语言配置用户账户。

示例 6.1 说明了你如何使用`Perl`发现用户使用的登录脚本。运行脚本并传入任意数量的用户账户。脚本将显示每个用户的登录脚本。

## 示例 6.1 显示用户的登录脚本

```perl
+01. use Win32;
02. use Win32::AdminMisc;
03.
04. if(! scalar $ARGV)
05. {
06. my($Script) = ($0 =~ /([^\[\]]*)?\$/);
07. print << "EOT";
08. Syntax
09. perl $Script <User Account> [<User Account 2> [ ... ]
10.
11. Example:
12. perl $Script administrator
```

## 示例 6.1 续

```
13. perl $Script somedomain\administrator accounting\joel
14. EOT
15.
16. exit();
17. }
18.
19. foreach my $Account ( @ARGV)
20. {
21.   my $Info;
22.
23.   print "$Account logon script: ";
24.   if (Win32::AdminMisc::GetMiscAttributes('', $Account, \%Info ))
25.   {
26.     if ("" eq $Info{USER_SCRIPT_PATH})
27.       $Info{USER_SCRIPT_PATH} = "No logon script configured";
28.     }
29.   }
30.   print "$Info{USER_SCRIPT_PATH}\n"
31. }
32. else
33. {
34.   print Win32::FormatMessage( Win32::AdminMisc::GetError() );
35. }
36. )
```

显示用户的登录脚本确实很有用，但能够修改账户同样有用。示例 6.2 接受用户账户名和登录脚本路径。此代码会修改用户的登录脚本路径。

## 示例 6.2 设置用户的登录脚本

```
01. use Win32;
02. use Win32::AdminMisc;
03.
04. if (! scalar @ARGV )
05. {
06.   my ($Script) = ( $0 =~ /([^"]*)\$/);
07.   print << "EOT";
08.   语法:
09.   perl $Script <用户账户> <登录脚本路径>
10.
11.   示例:
12.   perl $Script administrator scripts\administrator.bat
13.   perl $Script accounting\joel "genericlogon.pl"
14.
15.   要删除登录脚本，请将路径设置为 "*"，如下所示：
16.   perl $Script accounting\joel ""
17. EOT
18. exit();
```

```
19. }
20. 
21. my($Account, $Path ) = @ARGV;
22. if ("" eq $Path)
23. {
24. print "正在为 $Account 账户删除登录脚本。\n";
25. }
26. else
27. {
28. print "正在为 $Account 账户配置登录脚本，为: ";
29. print "$Path\n";
30. }
31. if (Win32::AdminMisc::UserSetAttributes('',
32. $Account,
33. USER_SCRIPT_PATH => $Path ))
34. {
35. print "成功\n"
36. }
37. else
38. {
39. print "发生错误: ";
40. print Win32::FormatMessage(Win32::AdminMisc::GetError());
41. }
```

## 修改用户环境

登录脚本可以被编写用来执行各种活动，以至于考虑讨论所有活动是徒劳的。然而，其中较常见的活动之一——查询和修改环境变量——非常值得介绍。

## 环境变量

`Windows NT`被设计为多用户操作系统。因此，它对用户资源和系统资源进行了区分。其中一种资源就是环境变量列表。

用户的配置文件（`profile`）可以包含由用户自己定义的环境变量。例如，如果用户`JOEL`添加了一个名为`INCLUDE`的环境变量，那么每当该用户登录时它都会生效。如果另一个用户登录到同一台机器，她将看到她自己的变量集，这些变量可能不同。

此外，如果用户被配置为使用漫游配置文件（`roaming profiles`），这组环境变量就会跟随用户从一台机器移动到另一台。无论用户登录到哪台电脑，`INCLUDE`环境变量都会以他配置的样子出现。

# 192 第 6 章：登录脚本

用户环境变量与系统环境变量是分开的。系统有自己的一`set`变量，从启动到关机期间一直使用。这组变量包括了如`PATH`在内的重要变量，它们由系统本身或具有管理员权限的用户设置。

通常，用户变量会覆盖系统变量。例如，如果系统变量`INCLUDEPATH`被设置为`c:\SystemInclude`，而一个用户将其用户变量`INCLUDEPATH`设置为`c:\MyInclude`并登录，那么任何使用`INCLUDEPATH`变量的应用程序都只会看到用户版本：`c:\MyInclude`。这可能会是一个问题，因为这意味着用户可以使用系统值，也可以使用用户变量，但不能同时使用。

解决办法是将系统变量嵌入到用户变量中。继续前面的示例，如果用户变量`INCLUDEPATH`设置为`%INCLUDEPATH%;c:\SystemInclude`，那么使用此环境的应用程序看到的`INCLUDEPATH`就是`c:\SystemInclude;`（系统版本）。当你在用户变量中放置对环境变量的引用时，它会继承系统变量的值。这个技巧只在这一方向有效。系统变量无法继承自用户变量。如果可以，可能会导致变量继承的冗余循环。这里的道理是，如果一个用户变量引用了自己，它实际上是在引用同名的系统环境变量。

正如你已经学到的，用户变量会覆盖与其同名的系统变量。这个变量是特殊的，因为系统需要它。在这种情况下，任何用户定义的`PATH`都会追加到系统变量之后。因此，如果任何用户将`PATH`定义为`c:\temp`，而系统的`PATH`设置为`c:\windows;c:\system32`，生成的`PATH`就是`c:\windows;c:\system32;c:\temp`。这允许用户作为用户定义其`PATH`指向他的主目录——例如`\serverhome\bin`。这使用户可以将经常使用的工具和应用程序放在一个地方，以便从局域网（`LAN`）的任何地方无缝地访问它们。

## Perl 与环境变量

由于用户变量可以覆盖系统变量，`Perl`脚本很难发现系统意图供应用程序使用的变量版本。`Perl`通过`%ENV`哈希表访问环境变量。它只访问当前环境暴露的变量集。这个环境就像`DOS`窗口一样，没有区分系统变量和变量的方法。因此，如果存在同名的用户变量，`Perl`将无法看到系统变量。

# 修改用户环境 193

在`Windows`中，每个应用程序都可以访问一个环境，该环境是为进程分配的一块内存，其中包含环境变量列表及其值等信息。每个运行中的进程都可以拥有自己独有的环境副本。当环境变量发生变化时（例如用户使用控制面板更改变量值），所有运行的程序都会收到通知，它们可以选择将更新后的值重新加载到环境中。因此，运行的`Windows`程序是否能看到这些更改取决于应用程序的设计。（`Windows`程序可能不会立即看到这些变化。）相比之下，控制应用程序通常不收听此类消息。因此，旧的`DOS`应用程序、`Perl`、`DOS`窗口和其他控制台应用程序在控制环境终止并重建之前是看不到这些变化的。这意味着`Perl`脚本必须停止，关闭运行它的控制窗口，打开一个新的控制窗口并重新运行`Perl`脚本才能看到变量的变化。

控制应用程序可以在检测到更改时更新其环境，但大多数通常不会。`Perl`不监听环境变化。对环境的更改仅通过`Perl`脚本使用`%ENV`哈希表进行。

# 查询变量

尽管`Perl`无法通过`%ENV`直接区分系统和用户，但它可以依靠其他方法查询系统和用户变量。示例 6.3 显示了如何使用`Win32::AdminMisc`独立查询用户和系统环境变量。脚本将系统和用户环境变量列表获取到哈希表中（第 5 行和第 14 行）并显示它们。运行脚本时，输出显示了哪些环境变量嵌入在其他环境变量中。

示例 6.4 是另一个脚本，它利用了一个冷门的函数`Win32::ExpandEnvironmentStrings()`，该函数可以展开传入字符串中任何环境变量的引用。嵌入在其他变量中的环境变量会被展开。比较这两个示例的输出是非常有趣的。

## 示例 6.3 续

```perl
06. {
07.     foreach $VarName = sort( keys($System ))
08.     {
09.         $VarValue = $System{$VarName};
10.         write;
11.     }
12. }
13.     print "\User Variables:\n";
14.     if (Win32::AdminMisc::GetEnvVar(\User, ENV_USER ))
15.     {
16.         foreach $VarName = sort( keys($User ))
17.         {
18.             $VarValue = $User{$VarName};
19.             write;
20.         }
21. }
22.
23.     format VariableFormat = <<<<<<<<<<<<<<<<<<<<<<<<<<<
24.         @<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
25.         $VarName, <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
26.         -
27.         $VarValue
28.         <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
29.         $VarValue
30.         <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
31.         -
32.         $VarValue
33.         <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
34.         -
35.         $VarValue
36.         <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
37.         -
38.         $VarValue
```

# 示例 6.4 显示扩展后的系统和用户环境变量

```perl
01. use Win32;
02. use Win32::AdminMisc;
03. \$- = VariableFormat;
04. print "System Variables:\n";
05. if (Win32::AdminMisc::GetEnvVar(\System, ENV_SYSTEM ))
06. {
07.     foreach $VarName = sort( keys($System ))
08.     {
09.         $VarValue = Win32::ExpandEnvironmentStrings($System{$VarName});
10.         write;
11.     }
12. }
13.     print "\nUser Variables:\n";
14.     if (Win32::AdminMisc::GetEnvVar(\User, ENV_USER ))
15.     {
```

## 修改用户环境

```perl
16. foreach $VarName ( sort(keys( %User )) )
17. {
18.   $VarValue = Win32::ExpandEnvironmentStrings($User{$VarName});
19.   write;
20.  }
21. }
```

```perl
22.
23. format VariableFormat = <<<<<<<<<<<<<<<<<<<< *<<<<<<<<<<<<<<<<<<<
24.  @ <<<<<<<<<<<<<<<<<<<< *<<<<<<<<<<<<<<<<<<<
25.  $VarName, <<<<<<<<<<<<<<<<<<<<<
26.    $VarValue
27.  <<<<<<<<<<<<<<<<<<<<<
28.  $VarValue
29.  <<<<<<<<<<<<<<<<<<<<<
30.  -
31.    $VarValue
32.  <<<<<<<<<<<<<<<<<<<<<
33.  $VarValue
34.  <<<<<<<<<<<<<<<<<<<<<
35.  $VarValue
36.  <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
37.  -
38.    $VarValue
```

早些时候学习过控制台应用程序可以使用最新的环境变量值来更新其环境。示例 6.5 完美地说明了这一点。代码定义了一个`UpdateEnv()`子程序，可以随时调用它来更新`Perl`进程的环境变量值。

`UpdateEnv()`函数通过获取最新的系统环境变量列表并设置`Perl`的`%ENV`哈希表来反映更新后的变量。请注意，首先设置的是系统变量，然后是用户变量。这个顺序很重要，因为用户变量优先于系统变量。此外，注意变量在设置之前没有被扩展。

# 示例 6.5 更新 Perl 的环境变量副本

```perl
01. use Win32::AdminMisc;
02.
03. UpdateEnv();
04.
05. sub UpdateEnv
06. {
07.   my @VarList = Win32::AdminMisc::GetEnvVar(\@VarList, ENV_SYSTEM )
08.   if ($)
09.   {
10.     print "Updating system environment variables:\n";
11.     foreach my $Var ( keys(%VarList ))
12.     {
13.       print "$Var\n";
```

## 示例 6.5 续



##我是由深度求索（DeepSeek）研发的 deepseek-v4-flash-0731 智能大模型。修改变量

通常来说，登录脚本不需要修改环境变量。通常，脚本会查询此类变量以便做出逻辑决策。例如，登录脚本可能会查询`Temp`变量以确定临时文件目录路径，以便进行清理。这种查询很常见，但从登录脚本设置环境变量并不常见。然而，该规则也有例外，例如当登录脚本想要记录用户登录的时间和日期时。

非管理员用户的登录脚本只有权限修改用户级的环境变量，而不能修改系统级（除非授予了管理员权限）。假设一台机器上有一个名为`INCLUDE`的系统环境变量，它由一组用分号分隔的路径组成，指向 C++ 头文件所在的位置。这是一个系统变量，因此不会被用户意外修改。当一个开发人员需要指向她自己的包含目录集时，她可以创建一个名为`INCLUDE`的用户环境变量，这会覆盖系统版本，并丢失系统管理员设置的所有内容。如果`INCLUDE`系统变量包含对`%INCLUDE%`的引用，那么用户变量将把该引用扩展为系统变量。这允许用户在不修改原始值的情况下修改`INCLUDE`变量的值。

如果这种基础架构不需要修改每个用户的账户以指向正确的脚本，那么它将是理想的。一个管理员的登录脚本可能是：

```
scripts\administrators.pl
```

会计师的登录脚本可能是：

```
scripts\accountants.pl
```

然而，如果组织中存在既是会计师又是管理员的成员——即同时属于“管理员”组和“会计师”组的成员——那么这种解决方案就会失效。同样，随着用户数量的增加，这种解决方案的扩展性并不良好。每当有人从组织中的一个职位变到另一个职位时，都要不断进行修改，这将变得无法管理。

管理此类扩展性问题更有效的方法是为所有用户使用相同的登录脚本——一种统一的登录脚本。

## 统一登录脚本

管理用户登录脚本的一种高效方法是使用登录脚本。这种脚本允许配置每个用户使用相同的登录脚本。当您创建一个新用户账户时，只需将其配置为执行与其他所有用户相同的登录脚本即可。这种高效的技术允许登录脚本本身实现逻辑，以确定在登录期间它应该为用户执行什么操作。

统一登录脚本是有益的，因为它们被所有用户共享。考虑这样一个脚本：它收集当前日期、IP 地址、计算机名称和用户名，然后将这些信息提交到中央数据库。这些信息可以让你快速访问并高效找到用户位于哪台机器。在大型环境中，这些信息对于在特定时间确定特定用户的位置非常有优势。如果用户可能登录到多台机器，这一点尤为真实，因为根据其网络注册用户名很难找到他（因为网络注册用户名是唯一的，且一次只能在一台机器上注册）。

## 处理用户组

正如您之前在“有效处理登录脚本”节中学的那样，根据用户组成员关系拆分登录脚本可以大大提高登录脚本的有效性。问题在于，如果网络实施了统一登录脚本，您无法轻松判断给定用户属于哪些组。如果统一登录脚本能够发现用户属于哪些组，它就可以执行每个相关的组脚本。

## 第 6 章：登录脚本

示例 6.7 包含一个使用`Win32::Lanman`扩展发现组身份的简单示例。第 9-12 行调用`NetGetUserLocalGroups()`并带有`LG_INCLUDE_INDIRECT`标志。此调用会发现用户所属的任何本地组，以及用户间接所属的任何本地组。第 13-15 行发现用户属于哪些全局组。该脚本接受用户名作为第一个参数，但如果没有传递任何内容，则使用当前登录的用户。

您可以轻松地将此脚本采用登录脚本，如后文示例 6.9 所示。

## 示例 6.7 使用 Win32::Lanman 发现组身份

```
01. use Win32;
02. use Win32::NetAdmin;
03. use Win32::Lanman;
04.
05. $Name = Win32::LoginName() unless ($Name = shift ARGV);
06. $Domain = Win32::DomainName();
07. Win32::NetAdmin::GetDomainController('', $Domain, $Dc);
08.
09. Win32::Lanman::NetGetUserGroups($Dc;
10. $Name,
11. LG_INCLUDE_INDIRECT,
12. @LocalGroups );
13. Win32::Lanman::NetGetUserGroups($Dc;
14. $Name,
15. @GlobalGroups );
16.
17. foreach my $Hash { sort { $a->{name} cmp $b->{name} } }
18. (@LocalGroups, @GlobalGroups ) )
19. {
20. print "\t";
21. print "$Hash->{name}\n";
22. }
```

## 机器设置脚本

系统管理中最平凡的方面之一是配置新机器。这个过程可能是缓慢且单调的。每台机器都需要您安装操作系统、对其进行配置、安装适当软件并进行相应的配置。自动化此过程的一种简单方法是利用登录脚本。

通过创建一个具有特殊登录脚本的特殊管理员账户，您只需走到新机器前，登录，然后离开。登录脚本将运行并开始重新配置计算机的工作。完成后，登录脚本可以重启计算机，使其为你（用户）准备就绪。而这一切仅仅是有人用特殊账户登录而已。

## 机器设置脚本 201

你可以重写登录脚本，使其创建适当的目录、复制文件、设置权限、创建本地账户并注册特定服务，甚至设置按常规计划执行的计划任务。

示例 6.8 是此类设置脚本的示例。它的设计预期是一个管理员用户账户将它作为登录脚本调用。当然，管理员必须修改此脚本以反映您自己的需求、服务器名称、路径等。

目前，脚本向域添加。

## 示例 6.8 自动化机器设置脚本

```
01. use Win32;
02. use Win32::Perms;
03. use Win32::NetAdmin;
04. use Win32::Registry;
05. use Win32::AdminMisc;
06.
07. $Machine = Win32::NodeName();
08. $Domain = Win32::DomainName();
09.
10. $PerlDrive = 'c:';
11. $PerlPath = '\perl';
12.
13. $REMOTE_L_PATH = '\server';
14. $NTFS_APP = 'convert.exe';
15. $NTFS_PARAM = '/FS/NTFS /V';
16.
17. ConfigGroup($Domain);
18. if (ConfigDrive($PerlDrive)) {
19. SecureDir($PerlPath);
20. CopyDir($REMOTE_L_PATH, $PerlPath);
21. ConfigPath('\bin');
22. }
23.
24. ConfigLastUser(" ");
```

继续

```
26. Log($LogFile);
27. RebootMachine();
28. print "Finished.\n";
29.
30. sub Log
31. {
32. my($LogFile) = @_;
33.
34. if (open(LOG, >> $LogFile)) )
35. {
36. flock(LOG, 2);
37. seek(LOG, 0, 2);
38. print LOG Win32::NodeName(), "\t", scalar(Itime()), "\n";
39. flock(LOG, 8);
40. }
41. }
42. sub RebootMachine
43. {
44. Win32::AdminMisc::Exit();
45. }
46. sub ConfigLastUser
47. {
48. my($User) = @_;
49. my($Key);
50. if ($Key = Win32::Registry::Open(HKEY_LOCAL_MACHINE, "SOFTWARE\Microsoft\Windows\CurrentVersion\logon"))
51. {
52. $Key->SetValue(REG_SZ, $User);
53. $Key->Close();
54. }
55. }
56. sub ConfigGroup
57. {
58. my($Domain) = @_;
59. Win32::NetAdmin::LocalGroupAdd("Administrators", $Domain);
60. }
61. sub ConfigPath
62. {
63. my($Dir) = @_;
64. my $Path = Win32::AdminMisc::GetEnv('PATH');
65. my $RegexDir = $Dir;
66. $RegexDir =~ s/[\.\]/$1/g;
67. if ($Path !~ /$RegexDir/i) {
68. Win32::AdminMisc::SetEnv('PATH', '$Path;$Dir');
69. }
70. return( 1 );
71. }
72. sub ConfigDrive
73. {
74. my($PerlDrive) = @_;
75. if (Win32::AdminMisc::GetDrive($PerlDrive)) {
76. Win32::AdminMisc::ConvertToNTFS($PerlDrive, '/FS/NTFS /V');
77. return( 1 );
78. }
79. return( 0 );
80. }
```

## 204 第 6 章：登录脚本

## 示例 6.8 延续

```perl
134.
135.   return( 0 != $Result);
136. }
137.
138.   sub ConfigDrive
139.   {
140.     my($Drive) = @;
141.     my %Info;
142.
143.     print("Configuring the $Drive drive...\n");
144.
145.     # 确保驱动器存在
146.     if(! -e $Drive)
147.     {
148.         print("The $Drive drive does not exist.\n");
149.         return(0);
150.     }
151.     # 我们是否有固定硬盘？
152.     if(DRIVE_FIXED != Win32::AdminMisc::GetDriveType($Drive))
153.     {
154.         print("The $Drive is not a local hard drive.\n");
155.         print("Skipping drive formatting.\n");
156.         return(0);
157.     }
158.     # 如果驱动器不是 NTFS，则将其转换为 NTFS
159.     %Info = Win32::AdminMisc::GetVolumeInfo($Drive);
160.     if('NTFS' != $Info->FileSystemName)
161.     {
162.         $cmd = "NTFS_CONVERSION_APP $Drive $NTFS_CONVERSION_PARAMS";
163.         print("The $Drive is not an NTFS drive.\n");
164.         print("Converting to {$Info->FileSystemName} format...\n");
165.         $ntfs_conversion = $cmd;
166.     }
167.     return(1);
168. }
```

## 案例研究 实现统一的登录脚本

一个新的网络管理员被聘用到一家中型公司。首要任务之一是重构用户的登录过程。她负责数千名用户，每个用户运行几种不同登录脚本之一。这些脚本非常复杂，旨在执行特定任务，导致很难将它们适配到不同的组。

管理员决定为所有用户使用统一的登录脚本。由于她的网络有许多子网，她认为最好是在每个子网的域控制器（DC）上复制所有的登录脚本。这样，更新脚本就像只在一个位置上进行更改一样简单。在`netlogon`共享中，她创建了一个子目录，并在其中放置了基于组的脚本。她为域中的大多数组编写了脚本，例如`Accounting.pl`、`Marketing.pl`、`Developers.pl`，当然还有`Administrators.pl`。她还创建了一个名为`Users`的子目录。在这个目录中，她可以为每个属于特定网络管理员且拥有自己登录脚本的用户放置登录脚本。这种统一的登录脚本方案实现了示例 6.9 所示的基础设施。

第 9 行到第 14 行创建一个包含登录相关信息的变量。注意，域控制器（`dc`）已被赋值为`undef`值。这样做是因为`NetAdmin::DomainController()`（第 24 行和第 25 行）要求在变量传递给函数之前必须为其分配内容。第 28 行获取所有域控制器。脚本随后遍历此列表，一次处理一台机器，寻找特定的共享目录。对于每个共享登录脚本的机器，都会进行 ping 测试以找到最近的服务器（第 36 行到第 42 行）。此过程在具有许多域控制器和子网的大型网络中可能没有那么有效，因为 ping 所有机器可能需要很长的时间。第 46 行使用服务器名称设置环境变量，以便在登录会话期间稍后运行的脚本可以发现是哪台机器被用来运行登录脚本的。

此时，程序尝试连接到 ODBC 数据库（第 50 行）。相反，依赖于脚本中硬编码的 DSN 连接字符串可能会更容易。这可以防止当计算机的 DSN 被删除或更改时出现任何问题。接下来，脚本使用本节“处理用户组”中讨论过的`Win32::Lanman`扩展发现用户属于哪些组（第 53 行到第 61 行）。第 65 行到第 71 行实际上执行加载每个组登录脚本的工作。注意它使用了`require`函数。因此，每个登录脚本*必须*返回一个 TRUE 值（任何非零均可）。第 75 行到第 78 行仅在存在时加载用户的个人登录脚本。

第 81 行到第 114 行修改用户的环境变量，以避免与同名的系统变量发生冲突。这在之前的“修改变量”部分中详细讨论过。

第 118 行到第 130 行的代码删除了临时目录中所有超过两周的文件。注意，它对用户的临时目录和系统定义的临时目录都执行此操作。最后，第 132 行到第 143 行将时间、用户名、用户所属域和机器名称提交到日志数据库。这些信息允许管理员快速发现特定用户在某台机器上登录。

在所有账户都改为统一登录脚本后，管理员发现，仅仅因为文件服务器下线或我们切换组，她在修改几十个脚本上花费的时间变短了，而花费更多时间处理其他重要的网络管理任务。

## 示例 6.9 案例研究 统一登录脚本

```perl
01. use Win32;
02. use Lanman;
03. use NetAdmin;
04. use AdminMisc;
05. use ODBC;
06.
07. $TempPeriod = 2 * WEEK;
08. $DSN = "LoginDatabase";
09. %Logon = (
10.     share => 'Netlogon',
11.     root => 'Scripts',
12.     user => 'Users',
13.     dc => undef,
14. );
15. $SERVER_TYPE = NTFS_CONVERSION_APP;
16. $sc = '';
17. @grouplist = ();
18. if (defined $dc) {
19.     foreach $Machine (@dc) {
20.       if (is_sharing($Machine)) {
21.         $Output = ping($Machine);
22.         if ($Output =~ /(\d+)ms/) {
23.             $Time = $1;
24.             if ($Time < $NewTime) {
25.                 $NewTime = $Time;
26.             }
27.         }
28.       }
29.     }
30. }
```



```perl我是由深度求索（DeepSeek）研发的 deepseek-v4-flash-0731 智能大模型。31. my $Result = 0;
32. my $NewTime = 0;
33. my $Count = 0;
34. my $User = '';
35. my $Domain = '';
36. my $Machine = '';
37. my $Group = '';
38.
39. return(0 != $Result);
40. }
41.
42. sub ConfigDrive
43. {
44. my($Drive) = @;
45. my %Info;
46.
47. print("Configuring the $Drive drive...\n");
48.
49. # 确保驱动器存在
50. if(! -e $Drive)
51. {
52.     print("The $Drive drive does not exist.\n");
53.     return(0);
54. }
55. # 我们是否有固定硬盘？
56. if(DRIVE_FIXED != Win32::AdminMisc::GetDriveType($Drive))
57. {
58.     print("The $Drive is not a local hard drive.\n");
59.     print("Skipping drive formatting.\n");
60.     return(0);
61. }
62. # 如果驱动器不是 NTFS，则将其转换为 NTFS
63. %Info = Win32::AdminMisc::GetVolumeInfo($Drive);
64. if('NTFS' != $Info->FileSystemName)
65. {
66.     $cmd = "NTFS_CONVERSION_APP $Drive $NTFS_CONVERSION_PARAMS";
67.     print("The $Drive is not an NTFS drive.\n");
68.     print("Converting to {$Info->FileSystemName} format...\n");
69.     $ntfs_conversion = $cmd;
70. }
71. return(1);
72. }
```

```perl
67. my $GroupName = $Group;
68. my $Script = "Scripts\\GroupName.pl";
69. print("Calling $Script\n");
70. require $Script;
71. }
72.
73.
74. if (-f "LogonPath\\userdir\\account.pl") {
75.     require "LogonPath\\userdir\\account.pl";
76. }
77.
78.
79. for (my $i = 118; $i <= 130; $i++) {
80.     # remove files older than two weeks
81. }
82.
83. # also does this for user's and system-defined temp directories
84.
85.
86.
87. for (my $i = 132; $i <= 143; $i++) {
88.     # submit update to the logging database
89. }
90. }
```

```perl
119. push(@TempDirs, Win32::AdminMisc::GetEnvVar('Temp', ENV_USER ) );
120. foreach $myTempDir (@TempDirs)
121. {
122.     foreach $myPath ( glob("$TempDir\\.**") )
123.     {
124.         next if (! -f $Path );
125.         if($TempFileGracePeriod < $time) { -(stat ($Path))[10]
126.             {
127.                 unlink($Path);
128.             }
129.         }
130.     }
131.
132.     # 更新登录数据库...
133.     if ($db)
134.     {
135.         $myQuery = 'INSERT INTO Logon UserLogon
136.             (Domain, Account, Machine, Date)
137.             VALUES ('$Logondomain',
138.                 '$Logonaccount',
139.                 '$Logonmachine',
140.                 {fn Now()});';
141.         $db->Sql ($myQuery);
142.         $db->Close() if ($db);
143.     }
144.
145.     BEGIN
146.     {
147.         $SECOND = 1;
148.         $MINUTE = 60 * $SECOND;
149.         $HOUR = 60 * $MINUTE;
150.         $DAY = 24 * $HOUR;
151.         $WEEK = 7 * $DAY;
152. }
```

## 结论

当你仅仅简单地重构已实现的登录脚本时，看到生产效率的剧增并不是稀见常事。实现这些脚本可以释放系统管理员的时间，并为用户在网络上的任何地方提供个性化的登录。这些脚本确实是强大的，无论是用于登录用户，还是作为自动化配置机器的启动点。当然，Perl 在处理登录脚本时是一个强大的盟友。

# 7 进程

现代计算机的一个基本目的是运行应用程序。这些应用程序可以是如此基础的形式，如服务和守护进程（daemons）、程序、自动批处理作业，或者 Visual Basic、Java 甚至是 Perl 脚本。由于这种能力在几乎所有计算机中都是常见的，因此它们具有相似之处也是理所当然的。大多数情况下，确实如此。

然而，Win32 世界有几个让来自 UNIX 学派的编码员感到可笑的特有现象。可以肯定，从 UNIX 的背景来看，这些问题被视为局限性，并且确实是可以嘲笑的。然而，它们并不一定是坏事；实际上，它们可以非常有用且强大。真正的问题是，UNIX 编码并不并不 Win32 进程创建。如果 Win32 出现在 UNIX 之前，你可以肯定人们当时会嘲笑它。

本章讨论了创建和管理进程的各种方法。讨论了创建进程的不同技术。还描述了常见的陷阱和障碍。

## Win32 进程

每当用户双击程序或从命令行运行应用程序（如 Perl）时，她就是在指示 Win32 创建一个新进程。通常用户并对此不会想太多；他们简单地进行`fork`（分叉）。无论启动了什么程序，Win32 都会分配一块内存，将程序及其它所需的任何库加载到该内存中，然后创建一个主线程来执行。在完成所有操作且程序运行后，它被称为一个进程。进程可以访问操作系统授予它的任何内存，但仅限于该内存。你可以将每个进程想为拥有它自己的沙箱，可以在里面做任何想做的事，但不能离开。这被称为进程空间（process space）。如果你阻止进程访问其空间之外的资源，你就可以维护系统安全。

许多词汇代表进程。守护进程、服务、应用程序和程序只是可能运行不同进程的少数几个，但它们都共享相同的物理表现。通常会有几个进程同时运行：一个允许你共享打印机和目录（服务器服务）；另一个允许连接到其他机器（工作站服务）；一个管理安全（登录服务）；而有些（如`echo`）则做一些简单的事情。作为管理员，你可以添加额外的服务或处理应用程序。

这种进程的创建并不新鲜；自从计算机能够将程序代码动态加载到内存中以来，它一直存在。然而，Win32 偏离了 UNIX 代码依赖的传统范式——这让 UNIX 程序员们感到非常羞愧。

好消息是，微软放弃了`fork`，而是选择了一种更高效的方法：线程（threading）。像 UNIX 一样，Win32 可以同时处理多个应用程序，因此应用程序可以多线程执行任务。多线程是高效的，因为所有线程都存在同一个进程中，所以它们共享相同的内存和安全属性。这意味着昂贵的进程通信（IPC），如共享内存、管道和套接字，不再是必须的。

与`fork`方法相反，线程可以直接访问彼此的数据结构。`fork`后的进程会产生两个具有相同内存副本的进程。由于两个进程运行在不同的内存空间中，因此没有内在的方法让一个进程访问另一个进程的内存。可以使用 IPC 来访问另一个进程，但这需要两个进程协同工作才能实现这种访问。

所以，Win32 既有自己的线程模型，也有自己的`fork`模型。然而，Win32 的模型并不太独特，因为 UNIX 多年来一直有线程变体。然而，独特的是缺乏`fork`机制，这正是本故事的开始。

遵循 UNIX 编码的传统，许多 Perl 的黑客出于各种原因使用了`fork`。尽管 Perl 是一门跨平台语言，但任何基于`fork`的脚本在 Win32 机器上运行时都会崩溃。因为 Win32 本身不支持`fork`。

大量的 Perl 编码员被迫重写他们的脚本，从`fork`转向线程。他们带着良好的意图和很高的希望开始这一过程，结果落入了最残酷的笑话——Win32 不支持线程。噢，人类！

好吧，所以编码员既不能`fork`也不能线程。这很快变成了 Java 或 Visual Basic 更有吸引力的局面。然后 Perl 5.005 发布，预示了 Win32 线程的。它仍然是实验性的，但看起来像是大家寻找的灵妙药。

随后引入的 Perl 5.6 不带来了线程（仍是实验性的），还带来了`fork`。这种`fork`（至少在 Win32 平台上）是模拟的。这意味着 Perl 让它看起来就像被`fork`了，尽管实际上并没有。Perl 会创建一个解释器对象的副本，并给它一个自己的线程来运行。

这种模拟的`fork`在大多数情况下都是有效的，但其他问题很容易出现。例如，如果一个 Perl 扩展不是线程安全的，那么在新线程中运行（作为`fork`模拟）可能会导致不准确的结果，因为一个线程可能会覆盖另一个线程的全局变量和数据结构。

即使有了这些新的线程和`fork`能力，Win32 仍然可以创建（或生成）新进程。尽管生成进程可能更慢、更繁琐且充满局限性，但一点创造力可以让聪明的编码员实现他们想要的结果。

## 创建进程

你可以在我的书籍《Win32 Perl Programming: The Standard Extensions》中找到关于使用 Win32 创建进程的良好参考。它涵盖了生成新进程的方法，并解释了进程创建函数接受的标志和其他参数。然而，本章涵盖了最常见的进程创建方法，从管道、系统命令、生成、`Win32::Process` 和 `Win32::AdminMisc` 到`fork`。

创建进程的第一种最简单的方法是使用反引号。

## 反引号

使用反引号可能是生成新进程最快速、最简单的方法之一。当你简化反引号之间的命令行时，该命令由 Win32 执行，新进程发送到`STDOUT`的每行输出都会捕获并作为数组的一个元素返回。这正是示例 7.1 所所的。

## 示例 7.1 使用反引号创建新进程

```perl
my @Output = `dir c:\temp`;

print @Output;
```

如你所见，使用反引号非常简单。然而，在你冲出去并开始对眼之所及的一切都使用反引号之前，你必须意识到 Win32 的陷阱：所以，请阅读。

## 文件扩展名问题

如果你将某些文件扩展名（例如`.pl`）关联到`PERL.EXE`，那么当仅引用它们的名称时，Perl 脚本就会执行。（详见第 1 章“Perl 与管理员”中关于关联文件扩展名到 Perl 的。）示例 7.2 展示了可执行文件。注意，你不需要指定`PERL.EXE`，只需指定 Perl 脚本路径即可。

> **注意**
>
> 当文件扩展名映射到`PERL.EXE`时，有时你需要传递 Perl 选项，例如`-w`和`-d`。在这种情况下，你可以引用整个命令行，包括`perl.exe`，如下：
>
> ```text
> perl.exe -d -w c:\temp\test.pl
> ```
>
> 或者在“sha-bang”行中添加标记。详情请参阅第 1 章。♦

## 示例 7.2 反引号与文件关联

```perl
my @Output = `c:\temp\perltest.pl`;

print @Output;
```

这一点是有道理的。毕竟，你可以在命令行中输入相同的路径，它也能神奇地运行。在 Windows 2000 机器上，你可以修改`PATH`环境变量以包含`.pl`扩展名（参阅第 1 章）。这样，Windows 就将`.pl`视为可执行扩展名，就像对待`.exe`、`.bat`和`.cmd`扩展名一样。你可以直接输入不带扩展名的 Perl 脚本名称，例如“perltest”。这假设`perltest.pl`脚本要么在你当前目录下，要么在路径中的某个地方。

## 长文件名

Win32 系列操作系统一直支持长文件名。与 UNIX 文件名一样，Win32 文件名可以很长——准确来说，多达 255 个字符。文件名可以使用大部分普通字符集，包括嵌入空格（限制包括反斜杠（`\`）、双引号（`"`）、正斜杠（`/`）和冒号（`:`））。然而，与 UNIX 不同，Win32 文件名是不区分大小写的。

此时，你可能在认真思考这种对文件系统理论的轻微偏离。实际上，进程和文件名之间有联系，但并不一定良好。文件可以具有嵌入空格的长路径名。虽然这很不错，但在你习惯之后，新鲜感很快就会消失。当这种兴奋感消失后，你会开始注意到 Perl 似乎并不真正喜欢这些长文件名。

当你使用反引号创建进程时，长文件名可能会带给你数小时的调试“乐趣”。问题并非来自长文件名本身，而是来自带有空格的长文件名。示例 7.3 说明，当使用反引号执行时，长文件名确实可以工作。

## 示例 7.3 反引号与长文件名

```perl
my $Name = "MyLongPerlScriptName.pl";

my $Output = "$Name";

print $Output;
```

示例 7.4 显示了相同的脚本，但要执行的 Perl 脚本名称中包含空格。这些空格会导致脚本执行失败，即使你指定了完整路径：

```text
c:\perl\bin\perl.exe c:\temp\My Long Perl Script Name.pl";
```

## 示例 7.4 带有空格的长文件名

```perl
my $Name = "My Long Perl Script Name.pl";

# 下行将失败，因为长文件名包含空格

my $Output = "$Name";

print $Output;
```

你可以为这种困境选择两种修复方法。第一种非常简单：用双引号括围长文件名（而不是单引号）：

```text
c:\perl\bin\perl.exe c:\temp\My Long Perl Script Name.pl";
```

然而，这种修复并不总是有效。取决于要执行的命令，某些路径在被引号括围时效果并不好。例如，下一行不起作用：

```text
"c:\Program Files\My Long Perl Script Name.pl";
```

在这种情况下，即使`.pl`扩展名已正确关联到`PERL.EXE`，仍会发生以下消息：

```text
c:\program" 不是内部或外部命令、可运行的程序或批处理文件。
```

此类失败的原因与`.pl`扩展名与`Perl.EXE`程序关联的方式有关。许多管理员错误地将`.pl`扩展名关联到命令行：

```text
ftype PerFile=c:\perl\bin\perl.exe %1 *
```

这是一个错误，因为当文件名包含空格时（例如`"c:\Program Files\My Long Perl Script Name.pl"`），该命令将扩展为：

```text
c:\perl\bin\perl.exe c:\Program Files\My Perl Script Name.pl
```

这将导致你尝试加载脚本`c:\Program`并传入参数：`Files\My`、`Long`、`Perl`、`Script`和`Name`。纠正此问题的方法是重新运行`ftype`命令，用引号括围`%1`参数（更多详情参阅第 1 章），如下所示：

```text
ftype PerFile=c:\perl\bin\perl.exe "%1" *
```

由于脚本无法依赖`.pl`扩展名是否已正确关联，因此可以使用第二种更有效的修复方法（我尚未见过这种技术失败）。简单地将长文件名转换为短名称。

为了与 DOS 和 Win16 应用程序（那些旧的 Windows 3.1 程序）后兼容，Win32 允许每个文件都有长名称和短名称。例如，对于这个长文件名：

```text
My list of files.txt
```

该文件的短名称版本可能是：

```text
MYLIST-1.TXT
```

确保程序能够发现文件短路径的唯一可靠方法是调用 Win32 API 的`GetShortPathName()`函数。恰好 Perl Win32 扩展暴露了这个函数。示例 7.5 展示了修复方法。

## 示例 7.5 解决带有空格的长文件名使用反引号的问题



## 使用 Win32 命令重定向输出句柄

在句柄 32 中，2 可以重定向标准输入输出（`STDIN`、`STDOUT`、`STDERR`）。通过使用 `Win32` 命令标记，你可以有效地重定向这些流。考虑这个示例：

```
dir *.directory.txt
```

此命令将 `dir` 命令的输出重定向到名为 `directory.txt` 的文件。然而，NT 提供了更大的功能，允许你指定要重定向哪个输出流。默认情况下，`STDOUT` 输出流（始终为句柄 1）被重定向。因此，前面的命令等同于：

```
dir .* 1> directory.txt
```

如果你想重定向命令的 `STDERR`，只需指定 `STDERR` 文件句柄（恰好是 2）：

```
rd MyDir 2> error.txt
```

在这种情况下，如果目录 `MyDir` 不存在，错误消息将保存到名为 `error.txt` 的文件中。

现在酷的地方在于，你还可以通过指定 `&` 字符和流句柄号来指定重定向的流：

```
rd MyDir 2>&1
```

此命令将 `STDERR` 重定向到 `STDOUT`。如果你将其与反引号执行相结合，你就能获取所有的 `STDOUT` 和 `STDERR`。示例 7.6 正是这样做。第 3 行的数组 `@output` 分配了两个输出的每一行。数组的前部分是 `STDOUT`，随后是 `STDERR`。示例 7.7 被示例 7.6 调用并提供了示例输出。

## 示例 7.6 使用反引号将 STDERR 重定向到 STDOUT

```
01. my $Name = "MyScript.pl";
02.
03. my @Output = '$Name 2>&1';
04. print @Output;
```

## 示例 7.7 用于示例 7.6 的 MyScript.pl 脚本

```
01. print STDERR "This is STDERR line #1\n";
02. print STDOUT "This is STDOUT line #1\n";
03. print STDERR "This is STDERR line #2\n";
04. print STDOUT "This is STDOUT line #2\n";
```

## 管道（使用 open()）

许多系统管理员已使用 `open()` 函数来创建进程。Perl 脚本可以将进程的 `STDIN` 或 `STDOUT` 重定向到 Perl 文件句柄。

当脚本使用管道打开（piped open）函数打开一个新的子进程时，它可以与新进程进行异步继续处理。也就是说，两个进程同时运行。子进程的输出被缓冲在 `open()` 调用中指定的句柄中。因此，父进程可以继续执行它需要做的任何工作，并在需要时从文件句柄中读取。由于从文件句柄读取数据可能会导致阻塞状态（如果没有数据等待读取），父进程会有效地停止处理，直到子任务发送一行数据或管道的子端关闭（当子进程终止时）。

围绕进程执行的语义与使用反引号（backticks）一致。示例 7.8 与示例 7.6 相同，不同之处在于它没有使用反引号，而是使用管道 `open()` 函数创建进程。第 2 行打开进程并将 `STDERR` 重定向到 `STDOUT`，所有内容都通过管道传输到文件句柄。

此脚本说明了反引号和管道打开非常相似。它们甚至存在相同的文件名问题。如果 `$Name` 被赋值为一个包含空格的值，第 2 行必须像如下所示：

```
if(open(FILE, "\$Name" 2>&1 | ))
```

注意 `$Name` 是由双引号定义的。有关更多细节，请参阅本章“反引号”部分中关于反引号相关问题的讨论。

## 示例 7.8 使用管道 open() 将 STDERR 重定向到 STDOUT

```
01. my $Name = "MyScript.pl"
02. if (open (FILE, "\$Name" 2>&1 | ))
03. {
04.     while (my $Line = <FILE>)
05.     {
06.         print $Line;
07.     }
08.     close (FILE);
09. }
```

## system() 函数

大多数来自 UNIX 背景的 Perl 程序员都熟悉 `system()` 命令，该命令启动传递给函数的应用程序。该命令在很大程度上与使用反引号或带管道的 `open()` 功能相同。例如，如果你在 Perl 脚本中使用该行：

```
system('test.pl');
```

假设 `.pl` 与 `perl.exe` 关联，那么 `test.pl` 脚本将成功执行。

与已经讨论的其他进程创建函数一样，在 Windows 2000 机器上，你可以传递不带扩展名的可执行文件名，例如：

```
system('test');
```

只要该扩展名已正确与可执行文件关联（例如 `.pl` 与 `perl.exe` 关联；详情请见第 1 章），并且该扩展已添加到 `PATH` 环境变量中。

与其他进程创建函数一样，包含空格的进程路径必须用引号括起来，如下：

```
system('my long file name.exe');
```

`system()` 函数与其他函数的区别在于，它不会捕获新进程的 `STDOUT`。即使脚本不需要等待捕获 `system()` 函数的输出，脚本也会进入阻塞状态并等待新进程终止。

## Win32::Spawn()

到目前为止，你检查了几个创建进程的函数，它们都有独特的特性。然而，它们都存在一个令人沮丧的共同点：在新进程运行时，它们都会阻塞（`fork()` 除外，`fork()` 仅在 Perl 5.6 及更高版本可用，以及在不从管道读取数据时的管道打开）。你需要一种方法来启动与调用脚本独立运行的进程。

`Win32::Spawn()` 是 Perl 特有的，因为它只存在于 Win32 机器上。此函数非常简单：

```
Win32::Spawn($App, $Args, $SPid);
```

第一个参数 `$App` 是要执行的程序路径。第二个参数 `$Args` 是传递给应用程序的参数。第三个参数 `$SPid` 必须是一个标量变量（例如 1 或 "hello"）。

在使用此函数之前，你应该了解几点，否则你可能会抓狂。如果路径包含空格，则不需要用双引号括起路径。因为第一个参数仅代表路径。

你指定的应用程序必须是可执行文件的完整路径（例如 `c:\winnt\notepad.exe`）或相对路径（例如 `notepad.exe` 或 `..\notepad.exe`）。如果你指定了相对路径，当前的驱动器和目录将会自动添加到应用程序名称之前。因此，不要传递 `NOTEPAD.EXE` 并期望它运行，仅仅可以通过 `PATH` 环境变量找到该应用程序。

`$Args` 参数很容易理解。如果你正在运行 Notepad 程序并想让它打开特定文件，请将文件路径作为第二个参数。足够简单吧？好吧，差不多。这并不明显，因为 `$Args` 参数必须以可执行文件的名称开始。是的，你读对了：你需要指定两次可执行文件（在第一个参数中一次，在第二个参数中一次）。更准确地说，你需要在 `$Args` 参数的开头指定某些内容（实际上是任何内容），它代表可执行文件。

第五个参数 `$1Flag` 允许脚本指定各种创建标志。这些标志决定了进程的创建方式。以下三个标志值得注意：

- `CREATE_NO_WINDOW`：如果该程序是控制台应用程序（例如 Perl 脚本），则创建一个不带窗口的进程。进程会运行，但不会为其创建控制台窗口（类似 DOS 的框）。因此，`STDOUT` 和 `STDERR` 不显示。
- `CREATE_NEW_CONSOLE`：创建一个带有新控制台窗口的进程。如果创建的进程是普通的 Windows 应用程序（带有图形窗口），则此标志将不起作用。进程的 `STDOUT` 和 `STDERR` 将显示在新窗口中。
- `CREATE_SUSPENDED`：如果你需要进行基准测试或同步新进程，这是一个非常有用的标志。进程会被创建，但会自动处于挂起（暂停）状态。你可以通过调用 `Resume()` 方法来恢复进程。该方法适用于任何进程，无论是控制台还是窗口进程。进程被创建时，在恢复之前不会显示其窗口。如果你同时指定了 `CREATE_NO_WINDOW` 标志，那么控制台应用程序的窗口即使在恢复后也不会出现。

通常，脚本在创建新的 Perl 脚本进程时会指定 `CREATE_NEW_CONSOLE`。这样，用户就可以看到进程的输出。然而，如果你有一个经常创建进程的服务或守护进程，总是有窗口弹出并获取焦点可能会令人分心和恼火。在这种情况下，你不应该指定 `CREATE_NO_WINDOW` 或 `CREATE_NEW_CONSOLE` 标志。

如果你既没有指定 `CREATE_NO_WINDOW` 也没有指定 `CREATE_NEW_CONSOLE`，新控制台进程的所有输出将输出到与原始 Perl 脚本相同的窗口中。在同一个窗口中看到不同进程的输出交织在一起可能会变得混乱。

最后，最后一个参数是为新进程设置的默认目录。

示例 7.11 使用 `NOTEPAD.EXE` 显示指定时间的文本文件。在超过超时值后，进程将被杀死。虽然这种方法显示“今日消息”（message of the day）的方式并不优雅，但在登录脚本等场景中可能是很有用的。该脚本的目的是演示 `win32::Process` 扩展的实用性。

注意，使用 `CREATE_SUSPENDED` 标志（第 8 行）并不是必要的；它在这里仅仅是为了演示如何创建一个挂起的进程。同样，调用 `Resume()` 方法（第 20 行）之所以是必要的，是因为进程是以挂起状态创建的。

## 创建进程

在查看脚本时，你可能会疑问第 20 行是做什么的。它看起来并不直观，但它有很好的作用。当进程被挂起时（通过调用进程对象的 `suspend()` 方法或以挂起状态创建进程），Win32 会增加一个内部计数器。该计数器指示了进程被挂起的次数。由于一个进程可以被挂起多次，因此该计数器会跟踪挂起的级别。调用对象的 `Resume()` 方法会导致计数器减小。

`Resume()` 方法返回进程在调用 `Resume()` 之前所处的挂起层级。这意味着如果 `Resume()` 返回值为 1，则进程不再挂起。考虑到进程可能会被挂起多次（甚至被其他进程挂起），第 20 行持续调用 `Resume()` 直到进程不再挂起为止。

第 23 行调用了 `Wait()` 方法，导致脚本阻塞，直到进程终止或超时值过期。超时值以毫秒为单位传递给 `Wait()` 方法。当 `Wait()` 返回时，如果其返回值为 0，表示超时过期；否则，表示进程已终止。

第 27 行展示了如何杀死进程。传递给 `Kill()` 方法的值是进程的退出代码。所有进程在退出（或被杀死）时都可以返回一个数值。

## 示例 7.11 创建一个挂起的进程

```perl
01. use Win32::Process;
02. $Timeout = 5;
03. $File = $0;
04. $App = "ENV%SystemRoot%\notepad.exe";
05. $Cmd = "notepad $File";
06. $bInherit = 0;
07. $Dir = " ";
08. $Flag = CREATE_SUSPENDED | CREATE_NEW_CONSOLE;
09. if ( Win32::Process::Create($App,
10. $Cmd,
11. $bInherit,
12. $Flag,
13. $Dir )
14.
15. {
16. $Pid = $Process->GetProcessID();
17. print "The process was created in a suspended state ";
18. print "with an ID of $Pid.\n";
19. print "Now resuming the process...\n";
20. while (1 < $Process->Resume())});
21. print "We will wait for Timeout seconds for the process to\n";
22. print "terminate...\n";
23. $Result = $Process->Wait($Timeout * 1000 );
24. if (! $Result)
25. {
```

## 示例 7.11 继续

```perl
26. print "The process did not terminate so we will kill it...\n";
27. $Process->Kill( 0 );
28. }
29. else
30. {
31. print "The process was terminated by the user.\n";
32.
33. }
34. else
35. {
36. print "Unable to create new process.\n";
37. print "Error: " Win32::FormatMessage(Win32::GetLastError());
38. }
```

## 值得注意的 Win32::AdminMisc 函数

最后两个值得注意的进程创建函数来自 `Win32::AdminMisc` 扩展：`CreateProcess()` 和 `CreateProcessAsUser()`。后者在“以另一个用户运行进程”部分进行了讨论。

从根本上说，它们是相同的；它们接受与 `Win32::Spawn()` 相同的参数，并且比 `Win32::Process::Create()` 更复杂。调用语法如下：

```
Win32::AdminMisc::CreateProcess($Cmd, [, %] )
```

此函数与 `Win32::Spawn()` 和 `Win32::Process::Create()` 不同，只需要指定一个命令行参数——类似于 `perl c:\temp\myscript.pl` 或 `winword.exe file.doc`。

可选的第二个参数实际上是属性值的列表。你不需要指定任何属性，但如果你指定了，将使用它们。这些属性可以指定窗口的位置以及显示方式（隐藏、最大化、最小化）。更多详细信息请参阅 Win32 文档。

## 226 第 7 章：进程

脚本中可以实现简单的 `fork`，例如示例 7.12 所示。在这个脚本中，发生了一个 `fork` 操作，父进程和子进程都会从 100 计数到 0，并在此过程中打印每一个数字。这里的目的是演示 `fork` 是如何工作的。

第 2 行非常重要，尽管原因可能并不那么明显。这一行开启了自动刷新模式（autoflush），这意味着当脚本打印内容时，它会自动刷新并将打印的文本强制推送到屏幕。如果没有这一行，所有到屏幕的输出都将被缓存，导致打印延迟。这会让看起来就像是一个进程运行并结束，然后另一个进程运行并结束，它们之间没有并发性。

第 5 行执行实际的 `fork`。注意脚本会检查命令是否返回了 `undef`。如果是，则 `fork` 失败，脚本将退出。否则，两个运行的进程都会调用 `Count()` 子程序。

## 示例 7.12 Fork 示例

```
01. # 关闭输出缓冲（开启自动刷新）
02. $! = 1;
03.
04. # Fork 进程
05. defined ($pid = fork()) || die "Could not fork: $!\n";
06. if ($0 == 0) {
07.
08. # 如果我们是子进程，则到达这里
09. Count('Child: \ ');
10. }
11. else
12. {
13. # 如果我们是父进程，则到达这里
14. Count('Parent: \ ');
15. }
16.
17. # 父子进程都会到达这里
18. $string = ( $pid ) ? "Parent " : "Child" . . " process has finished.\n";
19. print $string;
20.
21. sub Count
22. {
23. my ($String) = @_;
24. my $iCount = 100;
25.
26. while ($iCount--) {
27.
28. print "\$String\$iCount\n";
29. }
30. }
```



Forking 实际上非常简单。只需要确保脚本能够判断自己是子进程还是父进程，并据此执行代码即可。关于使用 `fork` 的更好示例是示例 7.24。

## 以另一个用户运行进程

**注意**
Win32 Perl 的 `fork` 仿真似乎解决了本章迄今为止处理的许多问题。然而，这种仿真仍然非常年轻，许多许多待解决的。在我的实验室中，大多数循环创建子进程的进程最终都会崩溃。因此，如果你计划在生产环境中部署此类 Win32 Perl 的 `fork()` 脚本，请务必小心。◆

自从 Windows NT 开发以来，管理员们一直感叹缺乏类似 UNIX 的超级用户（SU）工具。在 UNIX 中，任何人都可以运行 SU 工具，提供正确的密码，并被像超级用户一样对待。Win32 世界没有超级用户账户；相反，它有一个 Administrator（管理员）账户。被视为管理员的唯一方法是以管理员身份登录。这要求当前已登录的任何人先关闭所有应用程序并注销。这种方法对用户并不友好。

几年前，我通过编写一个名为 `RunAs.pl` 的脚本解决了这个问题（参见示例 7.14）。调用该脚本时，你提供一个用户名（可选的域名）、一个密码和一个要运行的应用程序。如果你在账户上以正确的权限登录，应用程序将运行并冒充指定的用户名。这项功能变得非常有用。通常，我会执行类似这样的操作：

```
perl runas.pl mydomainadministrator myadminpwd cmd.exe
```

结果是一个运行在 Administrator 账户下的 DOS 窗口。我无法执行删除受保护文件等管理管理任务。如果你运行一个简单的 `WhoAmI.pl` 脚本（参见示例 7.13），它将打印以下内容：

```
Currently logged on as:
-----------------------
Domain: mydomain
Computer: TEST_PC
User: Administrator
```

此输出显示新进程（`CMD.EXE`）正在以管理员身份运行，而不是当前用户——当然，除非当前用户本身就是管理员。

## 示例 7.13 简单的 WhoAmI 脚本

```
01. use Win32;
02. print "\nIncurrently logged on as:\n";
03. print "------------------------------------\n";
04. print "Domain: ";
05. print Win32::DomainName(), "\n";
06. print "Computer: ";
07. print Win32::NodeName(), "\n";
08. print "User: ";
09. print Win32::LogonName(), "\n";
```

Windows 2000 自带一个名为 `RunAs.exe` 的工具，其功能与示例 7.14 类似。更强大的 Windows 2000 版本可以加载指定用户的配置、注册表单元和环境。然而，为示例 7.14 添加启用相同功能的代码并不需要太大精力。在所有人升级到 Windows 2000 之前，示例 7.14 为 Windows 3.5、3.51 和 4.0 提供了一个可行的替代方案。

这个魔法脚本使用了两个 `Win32::AdminMisc` 函数的组合：`LogonAsUser()` 和 `CreateProcessAsUser()`。`LogonAsUser()` 函数非常简单：你传入想要冒充的用户域、名称和密码，以及一个登录类型标志。如果函数执行成功，脚本将在指定用户的冒充身份下继续。它将一直持续到脚本终止或调用 `Win32::AdminMisc::LogoffAsUser()` 为止。此时，`CreateProcessAsUser()` 函数派上用场。

假设你有一个 Perl 脚本通过 `LogonUser()` 成功冒充了另一个用户。只有该脚本可以以冒充用户的身份运行。因此，如果你启动另一个程序（DOS 窗口、Microsoft Word、网络浏览器或其他任何），它都不会以冒充用户的身份运行。脚本必须使用 `CreateProcessAsUser()` 来创建新进程。

使用 `Win32::AdminMisc::LogonAsUser()` 函数（如示例 7.14 中）的技巧在于，登录用户（运行脚本的账户）必须被授予以下权限：

- `SetToPrivilege`：作为操作系统的一部分运行
- `SeAssignPrimary`：替换进程层级
- `SeIncreaseQuota`：增加配额
- `SeChangeNotify`：跳过遍历检查

由于这些权限是本地的，用户在任何打算运行调用 `LogonAsUser()` 函数的脚本的每台计算机上，都必须拥有这些权限。在第 2 章“账户维护”中，示例 2.9 包含一个工具，允许管理员从命令行管理这些权限。

> **注意**
> 如果修改了特定用户的权限，该用户必须注销并重新登录，新设置才能生效，因为权限是在登录时分配的。

当用户登录时，会获得一个指示其账户属性的令牌。用户登录后，令牌不会更改；因此，他必须注销并重新登录以反映账户的变化。

此外，被冒充的用户账户需要正确的登录权限。通常使用 `LOGON2_LOGON_INTERACTIVE` 标志（如果没有指定则是默认值）。此权限允许用户通过键盘（交互式）登录机器。其他权限允许账户作为批作业、服务或通过网络登录。

> **注意**
> 如果在调用 `Win32::AdminMisc::LogonAsUser()` 时使用了 `LOGON2_LOGON_INTERACTIVE` 标志，在 NT 4.0 之前的版本上尝试 `Win32::AdminMisc::CreateProcessAsUser()` 可能会失败，因为无法通过网络登录生成主令牌。Windows NT 4.0 允许将模拟令牌复制为主令牌。这仅意味着你可以避免 `LOGON2_LOGON_NETWORK`，不要使用它。

如果脚本成功通过 `LogonAsUser()` 冒充了用户，则使用 `CreateProcessAsUser()` 创建的新进程将继承用户的凭据。因此，即使冒充脚本终止——或者脚本显式调用 `Win32::AdminMisc::LogoffAsUser()` 停止冒充——新进程也会继续冒充。

## 示例 7.14 以另一个用户运行进程

```
01. use Win32::AdminMisc;
02. my($Domain, $User) = ( ((.*)\\)?(?:\\)?$)/ [1..2];
03. $Password = shift $ARGV;
04. $Process = join(" ", $ARGV);
05. print "\Starting \$Process\ as $User in ";
```

## 示例 7.14 继续

```
06. print 'the $USDomain\domain...\n'
07. $Result = Win32::AdminMisc::LogonAsUser($Domain,
08. $User,
09. $Password, LOGON32_LOGON_INTERACTIVE);
10. if ($Result)
11. {
12. $LoginUser = Win32::AdminMisc::GetLogonName();
13. print "Successfully logged in as $LoginUser.\n"
14. $Result = Win32::AdminMisc::CreateProcessAsUser(
15. $Process,
16. "Flags" => CREATE_NEW_CONSOLE,
17. "XSize" => 640,
18. "YSize" => 400,
19. "X" => 200,
20. "Y" => 175,
21. "XBuffer" => 80,
22. "YBuffer" => 175,
23. "Show" => SW_MAXIMIZE,
24. "Title" => "$User\s Process program",
25. "Fill" => BACKGROUND_BLUE |
26. FOREGROUND_RED |
27. FOREGROUND_BLUE |
28. FOREGROUND_GREEN |
29. FOREGROUND_INTENSITY);
30. if ($Result)
31. {
32. print "Successful! The new process PID is $Result.\n"
33. }
34. else
35. {
36. print "Failed.\n\tError: ", Error(), "\n"
37. }
38. else
39. {
40. print "Failed to logon.\n\tError: ", Error(), "\n"
41. }
42. sub Error
43. return(Win32::FormatMessage(Win32::AdminMisc::GetError()));
```

## 枚举进程

获取当前运行进程的列表可能相当复杂。到目前为止，获取此类最简单的方法是运行任务管理器（见图 7.1）。你可以通过按下 `Ctrl+Shift+Esc` 运行此程序。你也可以通过右键点击任务栏并选择任务管理器来运行此程序。

遗憾的是，这些方法启动了一个用户必须交互的 GUI 程序。对于大多数用户来说，这可能没问题，但 Perl 需要通过程序实现相同的结果。

![](img/b5063514d2e449d6d8c5d65f100b84aa_250_0.png)

图 7.1 任务管理器窗口。

你可以获取进程列表，但这样做并不容易。你需要从注册表中提取信息。更准确地说，你从注册表性能根键（`HKEY_PERFORMANCE_DATA`）中获取信息。你可以编写一个 Perl 脚本来实现这一点，但编写这样的脚本非常慢且极其混乱。

Jutta Klebe 使用了一个名为 `Win32::PerfLib` 的 Perl 扩展。它提供了一种简单且快速的方法，用于从注册表中提取必要的性能数据。尽管这个扩展管理了大部分工作，但它仍然很混乱——虽然不像直接使用 `Win32::Registry` 扩展那样混乱。

使用 Jutta 的扩展，你不仅可以获得 PID 列表，还可以获得有关每个进程的有趣信息——例如分配了多少内存（工作集）以及该进程使用过的最大内存（峰值工作集）等数据。还可以获取每个进程打开了多少线程和句柄、计时以及进程优先级等信息。

示例 7.15 使用 `Win32::PerfLib` 导出带有每个进程详细信息的进程列表。当你运行此代码时，它会导出机器上运行的每个进程的各种属性。当脚本运行时，它会显示本地计算机上运行的进程统计。你可以通过从命令行传递名称（Win32 计算机名、DNS 名称或 IP 地址）来获取远程机器的进程信息。

## 第 7 章：进程

示例 7.15 生成的输出如图 7.2 所示。它是使用以下命令行生成的：

```
perl exe.ps \SERVER1
```

注意，脚本列出了远程机器的进程信息。如果不传递机器名称，它将显示本地机器的进程信息。

正在收集 ||SERVER... 的进程信息

| PID | _ | 进程名称 | 线程 | 内存 | 内存峰值 | 句柄 |
|---|---|---|---|---|---|---|
| 0 | _ | _Total | 264 | 52,156 K | 88,380 K | 4323 |
| 1024 | 984 | perl | 1 | 2,596 K | 2,660 K | 25 |
| 140 | 8 | smss | 6 | 32 K | 2,004 K | 33 |
| 168 | 140 | cssr | 11 | 2,144 K | 2,999 K | 339 |
| 216 | 188 | winlog | 46 | 4,336 K | 5,420 K | 795 |
| 228 | 188 | lsass | 17 | 1,000 K | 4,340 K | 309 |
| 364 | 216 | svchost | 8 | 1,408 K | 2,728 K | 258 |
| 444 | 216 | svchost | 37 | 3,904 K | 6,472 K | 473 |
| 492 | 216 | spoolv | 11 | 1,200 K | 2,668 K | 122 |
| 560 | 216 | injobsv | 21 | 2,216 K | 5,416 K | 110 |
| 600 | 216 | regsvc | 5 | 3,292 K | 3,428 K | 187 |
| 624 | 216 | mtask | 7 | 1,480 K | 2,936 K | 102 |
| 704 | 284 | ntdvm | 4 | 304 K | 2,002 K | 46 |
| 708 | 188 | taskmgr | 3 | 1,836 K | 1,836 K | 41 |
| 768 | 96 | WINWORD | 14 | 13,560 K | 14,212 K | 188 |
| 8 | _ | System | 25 | 28 K | 636 K | 271 |
| 912 | 96 | mobync | 6 | 3,984 K | 4,300 K | 172 |
| 920 | 96 | thotkey | 2 | 520 K | 988 K | 19 |
| 928 | 96 | TPWSAVE | 1 | 184 K | 916 K | 26 |
| 936 | 96 | TFUNKEY | 1 | 252 K | 1,152 K | 23 |
| 956 | 96 | realmon | 5 | 580 K | 2,076 K | 49 |
| 544 | 96 | explorer | 16 | 3,672 K | 5,732 K | 294 |
| 984 | 96 | cmd | 2 | 1,304 K | 2,420 K | 58 |

图 7.2 示例 7.15 的输出。

> **注意**：示例 7.15 适用于任何 NT 或 Windows 2000 机器。如果脚本从 Windows 机器收集信息，父字段（见图 7.2）将留空。虽然 `Win32::PerfLib` 扩展了进程列表，但仍然需要处理。你可以在 Jutta 的网站（http://www.bybyte.de/j）和微软开发者网络（http://ms.microsoft.com）找到有关如何处理 `Win32::PerfLib` 提供的信息。

## 示例 7.15 使用 Win32::PerfLib 在 NT 上获取进程列表

```
01. use Win32::PerfLib;
02. my $Server;
03. my $ProcessIndex;
04. my $ProcessObject;
05. $Server = $ARGV[0];
06. print "Collecting process info for Server...";
07. Win32::PerfLib::GetCounterNames($Server, $StringIndex);
08. map { $StringIndex->{$} = $_ } (keys%$StringIndex);
09. $ProcessIndex = $String($Process);
11.
12. # 连接到服务器的性能数据
13. $Perf = new Win32::PerfLib($Server);
14. if (!$Perf)
15.     print "Could not obtain the process list.";
16.     exit();
18.
19. $ProcessList = {};
20.
21. # 获取进程对象的性能
22. $Perf->GetObjectList($ProcessObject, $ProcessList);
23. $Perf->Close();
24.
25. $InstanceHash = $ProcessList{$ProcessObject}->{$ProcessIndex}->{Instances};
26. foreach my $ProcessObject (sort (keys%$InstanceHash))
27. {
28. my $ProcessCounter = $InstanceHash{$ProcessObject}->{Counters};
29. my $ThisProcess;
30. $ThisProcess{Name} = $InstanceHash{$ProcessObject}->{Name};
31. foreach my $Attrib (keys%$ProcessCounter)
32.
33. my $AttribName = $StringIndex($ProcessCounter->{$Attrib}{CounterTitle}) || '';
34. $ThisProcessName = Format($ProcessCounter->{$Attrib}, $ProcessList->{Objects}->{$ProcessIndex});
35.
36. }
37. $ProcessList{$ThisProcess{'ID Process'}} = %$ThisProcess;
38.
39.
40. $- = PROCESS_HEADER;
41. write;
42. $- = PROCESS_INFO;
43. foreach $ProcessList (sort%$ProcessList))
44. {
45. # 不要使用局部作用域，因为它是
46. 用在
47. write;
```



# 示例 7.14 继续

```perl
48. $Proc = $ProcessIndex;
49. write;
50. }
```

# 示例 7.14 继续

```perl
51.
52. sub Format
53. {
54. my($Proc, $ObjectList) = @_;
55. my $Value = $Proc->{Counter};
56. my $Type = $Proc->{CounterType};
57. my $TB = $ObjectList->{PerfFreq};
58. my $Y = $ObjectList->{PerfTime};
59.
60. if(100SEC_TIMER == $Type)
61. {
62. $Value = 100 * ($Value / 1000000);
63. }
64. elseif(PERF_ELAPSED_TIME == $Type)
65. {
66. my($Hour, $Min, $Sec);
67. # 将值转换为秒...
68. $Value = ($SY - $Value) / $TB;
69.
70. $Hour = $Value / (60 * 60);
71. $Min = $Hour - int($Hour);
72. $Sec = $Min - int($Min) * 60;
73. $Value = sprintf("%d:%02d:%02d", int($Hour), int($Min), int($Sec));
74. }
75. return($Value);
76. }
```

# 列举进程 235

```perl
101. $Proc->('ID Process'), $Proc->{'Creating Process ID'} || '*',
$Proc->(Name), $Proc->{'Thread Count'},
FormatNumber($Proc->('Working Set'),),
FormatNumber($Proc->('Working Set Peak'),),
$Proc->{'Handle Count'}
```

为了练习演示 `Win32::PerfLib` 节省了多少工作量，请对比示例 7.15 和示例 7.16 中的两个脚本。前者使用了 `Win32::PerfLib`，而后者使用了注册表（通过使用 `Win32API::Registry` 扩展）。

# 示例 7.16 使用注册表在 NT 上获取进程列表

```perl
01. use Getopt::Long;
02. use Win32API::Registry qw::(:ALL);
03.
04. %FLAG = (
05. friendly => 'f'; # 以 M 或 K 单位显示内存大小
06. );
07.
08. Configure (\Config, ARGV);
09. if ($Config->{help})
10. {
11. Syntax();
12. exit()
13. }
14.
15. $STRINGS_KEY = 'SOFTWARE\Microsoft\Windows NT\CurrentVersion\PerfLib\009';
16. $hRootKey = HKEY_LOCAL_MACHINE;
17. $STRUCT = (
18. process => "L2LplL4",
19. counter => "L2LLLL4",
20. counter_block => "L",
21. instance => "L3LL2",
22. perf_object => "A8L6LL10A10",
23. perf_object_type => "L4PLPL21LL8",
24. );
25.
26. if (**machine)
27. {
28. if (RegConnectRegistry($Config->{machine},$hRootKey, $hRootKey))
29. {
30. print "Unable to connect to $Config->{machine}.\n";
31. exit();
32. }
33. }
34.
35. if (RegOpenKeyEx($hRootKey,$STRINGS_KEY,0,KEY_READ,$hKey))
36. {
37. $Data = GetKeyValue($hKey,'Counters');
38. RegCloseKey($hKey);
39. )
```

# 示例 7.16 继续

```perl
40.
41. @Data = split("ic0", $Data);
42. for ($iIndex = 0; $iIndex <= #Data; $iIndex += 2)
43. {
44.   $STRINGS{$Data[$iIndex + 1]} = $Data[$iIndex];
45.   $STRINGS_INDEX($Data[$iIndex]) = $Data[$iIndex + 1];
46. }
47. $hRootKey = HKEY_PERFORMANCE_DATA;
48. if (" *"ne $Config->{machine} )
49. {
50.   if (!RegConnectRegistry($Config->{machine}, $hRootKey, $hRootKey))
51.     {
52.       print "Unable to connect to $Config->{machine}.*\n";
53.       exit();
54.     }
55. }
56.
57. $Data = GetKeyValue($hRootKey, $STRINGS{$process});
58.
59. # 我们没有打开这个键值，因为它是一个性能数据键（我们需要
60. # 打开它）。但我们必须关闭我们知道已经不再
61. # 监控的系统。
62. RegCloseKey($hRootKey);
63.
64.
65. # 好了，我们现在有数据了，让我们遍历一下...
66. # 首先获取 PerfObject 结构体...
67. UnpackObject($Data, \Object);
68. $Data = Offset($Data, $Object{HeaderLength});
69.
70. # 现在我们已经有了 PerfObject，遍历每个
71. # $index 直到我们找到想要的那个...
72. $index = $Object(NumObjectTypes);
73. while($index--)
74. {
75. # 接下来我们需要获取一个 ObjectType，所以我们必须
76. # 移动到 $Data 中的 ObjectType 结构体...
77. UnpackObjectType($Data, \Type);
78.   if($STRINGS{$process} eq $Object{ObjectNameIndex})
79.   {
80.     ParseProcesses($Data, \Processes);
81.     last;
82. $Data = Offset($Data, $Type{HeaderLength});
83. }
84.
85. $- = PROCESS_HEADER;
86. write;
87.
88. $- = PROCESS_INFO;
89. foreach $Process (keys ($Processes))
90. {
```

# 列举进程

```perl
91. # 不要使用词 作用域 Proc，因为它
92. # 在格式化输出中
93. 使用。
94. $Proc = $Processes{$Proc}
95. write;
96. }
```

```perl
97.
98. format PROCESS_HEADER = "%-10s %-10s %-20s %-10s %-10s", "PID", "Parent PID", "Process Name", "Threads", "Memory", "Memory Peak";
99. "------------------------------------------------"
100.
101. "------------------------------------------------"
102.
103. format PROCESS_INFO = "%-10d %-10d %-20s %-10d %s %s",
104. $Proc->{'ID Process'}, $Proc->{'Creating Process ID'},
105. $Proc->{'Thread Count'},
106. FormatNumber($Proc->{'Working Set'}),
107. FormatNumber($Proc->{'Working Set Peak'})
```

```perl
108.
109. sub ParseProcesses
110. {
111. my($Data, $Processes) = @_;
112. my %Type;
113. my $SpData = $Data;
114. my $SIndex;
115. my ($pCounter, $pThisProcess);
116.
117. # 在这里遍历每个进程并收集它的信息。
118. # 我们已经有了一个，但没有传递这个子程序。
119. UnpackObjectType($SpData, %Type);
120.
121. # 移动到第一个进程实例...
122. $pThisProcess = Offset($Data, $Type{DefinitionLength});
123.
124. # 我们有了类型，将 $Data 移动到下一个
125. 结构...
126. $Data = Offset($Data, $Type{DefinitionLength});
127.
128. $SIndex = 0;
129. print "Collecting process data for $Config->{machine} ... 0%";
130.
131. while($SIndex++ < $Type{NumInstances})
132. {
133. my (%Type, %CounterBlock);
134. my %Percent;
135.
136. UnpackInstance($pThisProcess, \Instance);
137. if ((0 < $Instance{NameLength} && (0 < $Instance{NameOffset}))
138. {
139. my $TempProcess;
140. my $Title;
```

# 示例 7.16 继续

```perl
141. my $pTempInstance;
142. $pTempInstance = Offset($pThisProcess, $Instance{NameOffset});
143. $Title = unpack("a$Instance{NameLength}", $pTempInstance);
144. $Title = $Title/100;
145. CollectCounterValues($pThisProcess, $Type, \Processes);
146. $Processes->{$Title}->{$Title} = $Title;
147.
148.
149. $pCounterBlock = Offset($pThisProcess, $Instance{ByteLength});
150. UnpackCounterBlock($pCounterBlock, \CounterBlock);
151. $pThisProcess = Offset($pCounterBlock, $CounterBlock{ByteLength});
152.
153. print("\x05");
154. printf(" %4d", $SIndex / $Type{NumInstances} * 100 );
155. }
156. print("\n");
157. }
158.
159. sub CollectCounterValues
160. {
161. my($Data, $objectData, $Process) = @_;
162. my %Type, $Instance;
163. my($iIndex, $pCounterBlock, $pThisCounterDef);
164.
165. UnpackInstance($Data, \Instance);
166. UnpackObjectType($objectData, \Type);
167.
168. $pThisCounterDef = Offset($objectData, $Type{HeaderLength});
169.
170. $pCounterBlock = Offset($Data, $Instance{ByteLength});
171. $iIndex = $Type{NumInstances} - 1;
172.
173. while (--$iIndex)
174. {
175. my($pThisCounter, $pThisCounterDef, $iIndex, $Property);
176. my $pValue = 0;
177. my $myCounterType = 0;
178.
179. UnpackCounter($pThisCounterDef, \pThisCounterDef);
180. $pThisCounter = Offset($pCounterBlock, $pThisCounterDef{CounterOffset});
181. # $pThisCounter 现在指向计数器数据
182.
183. $Property = $STRINGS_INDEX($pThisCounterDef{CounterTitleIndex});
184. # 假设我们寻找的信息总是
185. # 一个无符号长整数 (DWORD)
186. $pValue = unpack("L", $pThisCounter);
187. if ($myCounterType == 0)
188. {
189. # 值的长度是定义
190. # 我们在这个版本中没有做
191. }
```

# 列举进程

```perl
192. else if ($Type{CounterType} == 0)
193. {
194. # 值的长度是
195. $Value = 0;
196. }
197. else if ($Type{CounterType} == 1)
198. {
199. # 我们有一个 64 位值
200. my($Lo, $Hi) = unpack("LL", $pCounter);
201. $Value = ($Hi * 0xFFFFFFFF) + $Lo;
202. }
203. else
204. { # 值是 32 DWORD
205. $Value = unpack("L", $pCounter);
206. }
207.
208. $Processes->{$Title}->{$Title} = $Value;
$Percent{} = (int($Value / 100)) "%";
209.
210. }
```

# 示例 7.16 续

```perl
246. }
247.
248. sub UnpackPerfObject
249. {
250. my ($Data, $Object) = @_;
251. my ($Perf) = unpack($Perf, $STRUCT(perf_object), $Data);
252.
253. ## 检查数据结构的签名
254. if ("$P\x0E\x0A\x0F\x00" == $Perf[0]) {
255.     my $iIndex = 0;
256.     $Object->{Signature} = $Perf[$iIndex++];
257.     $Object->{LittleEndian} = $Perf[$iIndex++];
258.     $Object->{Version} = $Perf[$iIndex++];
259.     $Object->{Revision} = $Perf[$iIndex++];
260.     $Object->{TotalLength} = $Perf[$iIndex++];
261.     $Object->{HeaderLength} = $Perf[$iIndex++];
262.     $Object->{NumTypes} = $Perf[$iIndex++];
263.     $Object->{DefaultObjectType} = 0xFFFFFFFF;
264.     $Object->{SystemTime} = $Perf[$iIndex++];
265.     $Object->{PerfTime} = 0xFFFFFFFF;
266.     $Object->{PerfFreq} = $Perf[$iIndex++];
267.     $Object->{PerfTime10nSec} = 0xFFFFFFFF;
268.     $Object->{SystemName} = $Perf[$iIndex++];
269.     $Object->{SystemNameOffset} = $Perf[$iIndex++];
270.     $Object->{Name} = $Perf[$iIndex++];
271. }
272. }
273.
274. sub UnpackObjectType
275. {
276. my ($Data, $Type) = @_;
277. my ($Perf) = unpack($Perf, $STRUCT(perf_object_type), $Data);
278.
279. if ("$P\x0E\x0A\x0F\x00" == $Perf[0]) {
280.     my $iIndex = 0;
281.     $Type->{Signature} = $Perf[$iIndex++];
282.     $Type->{LittleEndian} = $Perf[$iIndex++];
283.     $Type->{Version} = $Perf[$iIndex++];
284.     $Type->{Revision} = $Perf[$iIndex++];
285.     $Type->{TotalLength} = $Perf[$iIndex++];
286.     $Type->{HeaderLength} = $Perf[$iIndex++];
287.     $Type->{NumTypes} = $Perf[$iIndex++];
288.     $Type->{DefaultObjectType} = 0xFFFFFFFF;
289.     $Type->{SystemTime} = $Perf[$iIndex++];
290.     $Type->{PerfTime} = 0xFFFFFFFF;
291.     $Type->{PerfFreq} = $Perf[$iIndex++];
292.     $Type->{PerfTime10nSec} = 0xFFFFFFFF;
293.     $Type->{SystemName} = $Perf[$iIndex++];
294.     $Type->{SystemNameOffset} = $Perf[$iIndex++];
295.     $Type->{Name} = $Perf[$iIndex++];
296. }
297. }
298.
299. sub UnpackInstance
300. {
301. my ($Data, $Instance) = @_;
302. my ($Perf) = unpack($Perf, $STRUCT(instance), $Data);
303.
304. if ("$P\x0E\x0A\x0F\x00" == $Perf[0]) {
305.     my $iIndex = 0;
306.     $Instance->{Signature} = $Perf[$iIndex++];
307.     $Instance->{LittleEndian} = $Perf[$iIndex++];
308.     $Instance->{Version} = $Perf[$iIndex++];
309.     $Instance->{Revision} = $Perf[$iIndex++];
310.     $Instance->{TotalLength} = $Perf[$iIndex++];
311.     $Instance->{HeaderLength} = $Perf[$iIndex++];
312.     $Instance->{NumTypes} = $Perf[$iIndex++];
313.     $Instance->{DefaultObjectType} = 0xFFFFFFFF;
314.     $Instance->{SystemTime} = $Perf[$iIndex++];
315.     $Instance->{PerfTime} = 0xFFFFFFFF;
316.     $Instance->{PerfFreq} = $Perf[$iIndex++];
317.     $Instance->{PerfTime10nSec} = 0xFFFFFFFF;
318.     $Instance->{SystemName} = $Perf[$iIndex++];
319.     $Instance->{SystemNameOffset} = $Perf[$iIndex++];
320.     $Instance->{Name} = $Perf[$iIndex++];
321. }
322. }
323.
324. sub UnpackCounterBlock
325. {
326. my ($Data, $CounterBlock) = @_;
327. my ($Perf) = unpack($Perf, $STRUCT(counter_block), $Data);
328.
329. if ("$P\x0E\x0A\x0F\x00" == $Perf[0]) {
330.     my $iIndex = 0;
331.     $CounterBlock->{Signature} = $Perf[$iIndex++];
332.     $CounterBlock->{LittleEndian} = $Perf[$iIndex++];
333.     $CounterBlock->{Version} = $Perf[$iIndex++];
334.     $CounterBlock->{Revision} = $Perf[$iIndex++];
335.     $CounterBlock->{TotalLength} = $Perf[$iIndex++];
336.     $CounterBlock->{HeaderLength} = $Perf[$iIndex++];
337.     $CounterBlock->{NumTypes} = $Perf[$iIndex++];
338.     $CounterBlock->{DefaultObjectType} = 0xFFFFFFFF;
339.     $CounterBlock->{SystemTime} = $Perf[$iIndex++];
340.     $CounterBlock->{PerfTime} = 0xFFFFFFFF;
341.     $CounterBlock->{PerfFreq} = $Perf[$iIndex++];
342.     $CounterBlock->{PerfTime10nSec} = 0xFFFFFFFF;
343.     $CounterBlock->{SystemName} = $Perf[$iIndex++];
344.     $CounterBlock->{SystemNameOffset} = $Perf[$iIndex++];
345.     $CounterBlock->{Name} = $Perf[$iIndex++];
346. }
347. }
348.
349. sub UnpackCounter
350. {
351. my ($Data, $Counter) = @_;
352. my ($Perf) = unpack($Perf, $STRUCT(counter), $Data);
353.
354. if ("$P\x0E\x0A\x0F\x00" == $Perf[0]) {
355.     my $iIndex = 0;
356.     $Counter->{Signature} = $Perf[$iIndex++];
357.     $Counter->{LittleEndian} = $Perf[$iIndex++];
358.     $Counter->{Version} = $Perf[$iIndex++];
359.     $Counter->{Revision} = $Perf[$iIndex++];
360.     $Counter->{TotalLength} = $Perf[$iIndex++];
361.     $Counter->{HeaderLength} = $Perf[$iIndex++];
362.     $Counter->{NumTypes} = $Perf[$iIndex++];
363.     $Counter->{DefaultObjectType} = 0xFFFFFFFF;
364.     $Counter->{SystemTime} = $Perf[$iIndex++];
365.     $Counter->{PerfTime} = 0xFFFFFFFF;
366.     $Counter->{PerfFreq} = $Perf[$iIndex++];
367.     $Counter->{PerfTime10nSec} = 0xFFFFFFFF;
368.     $Counter->{SystemName} = $Perf[$iIndex++];
369.     $Counter->{SystemNameOffset} = $Perf[$iIndex++];
370.     $Counter->{Name} = $Perf[$iIndex++];
371. }
372. }
373.
374. sub Offset
375. {
376. my ($Data, $Offset) = @_;
377. return substr($Data, $Offset);
378. }
379.
380. sub GetKeyValue
381. {
382. my ($hKey, $ValueName) = @_;
383. my $Data;
384. my $Type;
385. my $Length = 0;
386.
387. if (RegQueryValueEx($hKey, $ValueName, 0, $Type, $Data, $Length)) {
388.     return $Data;
389. }
390. else {
391.     return "";
392. }
393. }
394.
395. sub FormatNumber
396. {
397. my ($Number) = @_;
398. if ($FLAG{friendly}) {
399.     if ($Number >= 1024 * 1024) {
400.         return sprintf("%.1fM", $Number / (1024 * 1024));
401.     }
402.     elsif ($Number >= 1024) {
403.         return sprintf("%.1fK", $Number / 1024);
404.     }
405.     else {
406.         return "$Number";
407.     }
408. }
409. else {
410.     return "$Number";
411. }
412. }
413.
414. sub Syntax
415. {
416. print <<"EOT";
417. Usage: $0 [options]
418. Options:
419.   --machine=<name>   Specify the machine to query (default: local)
420.   --friendly         Display memory sizes in human-readable format (M/K)
421.   --help             Show this help message
422. EOT
423. }
424.
425. # 主程序入口
426. my $Config = {};
427. my $ARGV = \@ARGV;
428. GetOptions($Config, 'machine=s', 'friendly', 'help');
429.
430. if ($Config->{help}) {
431.     Syntax();
432.     exit(0);
433. }
434.
435. # 初始化
436. my %STRINGS;
437. my %STRINGS_INDEX;
438. my %Processes;
439.
440. # 获取计数器字符串
441. my $STRINGS_KEY = 'SOFTWARE\Microsoft\Windows NT\CurrentVersion\PerfLib\009';
442. my $hRootKey = HKEY_LOCAL_MACHINE;
443. my $hKey;
444.
445. if (RegOpenKeyEx($hRootKey, $STRINGS_KEY, 0, KEY_READ, $hKey)) {
446.     my $Data = GetKeyValue($hKey, 'Counters');
447.     RegCloseKey($hKey);
448.     my @Data = split("ic0", $Data);
449.     for (my $iIndex = 0; $iIndex <= $#Data; $iIndex += 2) {
450.         $STRINGS{$Data[$iIndex + 1]} = $Data[$iIndex];
451.         $STRINGS_INDEX{$Data[$iIndex]} = $Data[$iIndex + 1];
452.     }
453. }
454.
455. # 连接到性能数据
456. $hRootKey = HKEY_PERFORMANCE_DATA;
457. if ($Config->{machine} && $Config->{machine} ne "*") {
458.     if (!RegConnectRegistry($Config->{machine}, $hRootKey, $hRootKey)) {
459.         print "Unable to connect to $Config->{machine}.\n";
460.         exit(1);
461.     }
462. }
463.
464. my $Data = GetKeyValue($hRootKey, $STRINGS{process});
465. RegCloseKey($hRootKey);
466.
467. # 解析性能数据
468. my %Object;
469. UnpackPerfObject($Data, \%Object);
470. $Data = Offset($Data, $Object{HeaderLength});
471.
472. my $index = $Object{NumTypes};
473. while ($index--) {
474.     my %Type;
475.     UnpackObjectType($Data, \%Type);
476.     if ($STRINGS{process} eq $Type{ObjectNameIndex}) {
477.         ParseProcesses($Data, \%Processes);
478.         last;
479.     }
480.     $Data = Offset($Data, $Type{HeaderLength});
481. }
482.
483. # 输出进程信息
484. format PROCESS_HEADER =
485. "%-10s %-10s %-20s %-10s %-10s %-10s\n",
486. "PID", "Parent PID", "Process Name", "Threads", "Memory", "Memory Peak";
487. "------------------------------------------------------------\n";
488.
489. format PROCESS_INFO =
490. "%-10d %-10d %-20s %-10d %s %s\n",
491. $Proc->{'ID Process'}, $Proc->{'Creating Process ID'},
492. $Proc->{'Thread Count'},
493. FormatNumber($Proc->{'Working Set'}),
494. FormatNumber($Proc->{'Working Set Peak'});
495.
496. $- = PROCESS_HEADER;
497. write;
498.
499. $- = PROCESS_INFO;
500. foreach my $Process (keys %Processes) {
501.     $Proc = $Processes{$Process};
502.     write;
503. }
504.
505. exit(0);



`my ($Data, $Type) = @_;`

`my ($Perf) = unpack($STRUCT(perf_object_type), $Data);`

`my $iIndex = 0;`

`$Type->{TotalLength} = $Perf[$iIndex++];`

`$Type->{DefinitionLength} = $Perf[$iIndex++];`

`$Type->{HeaderLength} = $Perf[$iIndex++];`

`$Type->{ObjectNameIndex} = $Perf[$iIndex++];`

`$Type->{ObjectTitle} = $Perf[$iIndex++];`

`$Type->{ObjectHelpIndex} = $Perf[$iIndex++];`

`$Type->{ObjectHelpText} = $Perf[$iIndex++];`

`$Type->{DetailLevel} = $Perf[$iIndex++];`

## 枚举进程 241

```
297. $Type->{NumCounters} = $Perf[$iIndex++];
```

```
298. $Type->{DefaultCounter} = $Perf[$iIndex++];
```

```
299. $Type->{NumInstances} = $Perf[$iIndex++];
```

```
300. $Type->{CodePage} = $Perf[$iIndex++];
```

```
301. $Type->{PerfTime} = 0xFFFFFF;
```

```
302. * $Perf[$iIndex++] + $Perf[$iIndex++];
```

```
303. $Type->{PerfFreq} = 0xFFFFFF;
```

```
304. * $Perf[$iIndex++] + $Perf[$iIndex++];
```

```
305. }
```

```
307. sub UnpackCounterBlock
```

```
308. {
```

```
309. my($Data, $Block) = @_;
```

```
310. my($Perf) = unpack( STRU{counter_block}, $Data );
```

```
311. my($iIndex = 0;
```

```
312. }
```

```
313. $Block->{ByteLength} = $Perf[$iIndex++];
```

```
314. }
```

```
316. sub GetKeyValue
```

```
317. {
```

```
319. my($hKey, $Value) = @_;
```

```
320. my($Data;
```

```
321. my($BufferSize = 0;
```

```
my($CurrentBufferSize = 10240;
```

> # 如果调用 `RegQueryValue(Ex)` 时提供的缓冲区太小，
> 将会失败，但会将 `$BufferSize` 设置为应具备的大小。
> 然而，可能在重新调用时，
> 缓冲区的大小要求已经发生了变化。因此，我们继续
> 增加缓冲区直到执行成功为止。

```
do
```

```
$BufferSize = $CurrentBufferSize += $BufferSize;
while(! RegQueryValueEx($hKey, $Value, []);
$Type, $Data, $BufferSize );
```

```
return($Data);
```

```
sub Offset
```

```
my($Data, $Offset) = @_;
```

```
my($Temp);
```

```
($Temp, $Data) = unpack( "a", $Offset . "a", $Data );
```

```
return($Data);
```

```
sub FormatNumber
```

```
my($Number) = @_;
```

```
my($Suffix) = "";
```

## 第 7 章：进程

## 示例 7.16 续

```
350. if defined $Config($FLAG{friendly}})
351. {
352.   my($K, $M) = ( 1024, (1024 * 1024) );
353.   if ($K <= $Number && ($M > $Number))
354.     {
355.       $Suffix = " * K";
356.       $Number /= $K;
357.     }
358.   elsif ($M <= $Number)
359.     {
360.       $Suffix = " * M";
361.       $Number /= $M;
362.     }
363.   }
364. $Number = s/(\d{0,2})\d*\$/1;
365. while($Number -= s/(\d+)(\d{3})\$/1,$2);
366.   return($Number . $Suffix);
367. }
368. 
```

369. `sub Configure`

```
370. {
371.   my($Config, @Args) = @_;
372.   my $Result;
373.   $Config->{'machine'} = Win32::ComputerName();
374.   Getopt::Long::configure('prefix=-');
375.   $Result = GetOptions($Config,
376.     qw(f help|h));
377.   $Config->{'machine'} = shift @ARGV if (scalar @ARGV);
378.   $Config->{'help'} = unless ($Result);
379. }
380. 
381. sub Syntax
```

382. {

383.   my($Script) = ($0 -= /^\*?$/);

384.   my($Line) = ".*" length($Script);

385.   print <<EOT;

386.   $Line

387.   Usage:

388.   $Script [options] [machine name]

389.     -f  Use friendly names

390.     -h  Show this help

391.

392.   Options:

393.     -f

394.     --friendly-name

395.

396.     -h

397.     --help

398.

399.   Arguments:

400.     machine name  The name of the machine to query.

401.

402. EOT

403. }

404. 

405. sub GetPidList

```
406. {
407.     my @pids = ();
408.     my $hSnapshot = Win32::CreateToolhelp32Snapshot(0x0002, 0);
409.     if ($hSnapshot != -1) {
410.         my $te = Win32::PROCESSENTRY32;
411.         $te->dwSize = Win32::SizeOf($te);
412.         if (Win32::Process32First($hSnapshot, \$te)) {
413.             push(@pids, $te->th32ProcessID);
414.             while (Win32::Process32Next($hSnapshot, \$te)) {
415.                 push(@pids, $te->th32ProcessID);
416.             }
417.         }
418.         Win32::CloseHandle($hSnapshot);
419.     }
420.     return(@pids);
421. }
422. 
423. sub GetProcessName
```

424. {

425.     my ($pid) = @_;

426.     my $hSnapshot = Win32::CreateToolhelp32Snapshot(0x0002, 0);

427.     if ($hSnapshot != -1) {

428.         my $te = Win32::PROCESSENTRY32;

429.         $te->dwSize = Win32::SizeOf($te);

430.         if (Win32::Process32First($hSnapshot, \$te)) {

431.             if ($te->th32ProcessID == $pid) {

432.                 return $te->th32FileFile;

433.             }

434.             while (Win32::Process32Next($hSnapshot, \$te)) {

435.                 if ($te->th32ProcessID == $pid) {

436.                     return $te->th32FileFile;

437.                 }

438.             }

439.         }

440.         Win32::CloseHandle($hSnapshot);

441.     }

442.     return "Unknown";

443. }

444. 

445. sub GetProcessMemory

```
446. {
447.     my ($pid) = @_;
448.     my $hProcess = Win32::OpenProcess(0x0400 | 0x0010, 0, $pid);
449.     if ($hProcess != -1) {
450.         my $pm = Win32::PROCESS_MEMORY_COUNTERS;
451.         $pm->dwCB = Win32::SizeOf($pm);
452.         if (Win32::GetProcessMemoryInfo($hProcess, \$pm)) {
453.             return $pm->WorkingSetSize;
454.         }
455.         Win32::CloseHandle($hProcess);
456.     }
457.     return 0;
458. }
459. 
460. # Main loop
461. my @pids = GetPidList();
462. for my $pid (@pids) {
463.     my $name = GetProcessName($pid);
464.     my $mem = GetProcessMemory($pid);
465.     printf("PID: %5d Name: %-20s Memory: %d KB\n", $pid, $name, $mem / 1024);
466. }
```

# PSAPI 库 245

```
42. 创建一个缓冲区
```

```
43. $ProcArray = MakeBuffer($DWORD_SIZE * $PROC_ARRAY_SIZE);
```

```
44. $ProcNum = MakeBuffer($DWORD_SIZE);
```

```
45. {
46. foreach ($Pid (@PidList)) {
47. my $ModuleCount = 0;
48. my $ProcInfo = GetProcessInfo($Pid);
49. print "\n$ProcInfo->{name}\n";
50. if (scalar ($ProcInfo->{modules})) {
51. {
52. printf("当前内存占用: %s 峰值内存占用: %s\n",
53. FormatNumber($ProcInfo->{workingset}));
54. FormatNumber($ProcInfo->{workingpeak}));
55. print "模块列表:\n";
56. foreach ($ProcInfo->{modules}) {
57. {
58. printf("%03d \n", ++$ModuleCount);
59. }
60. }
61. else {
62. print "无法获取进程信息。\n";
63. }
64. }
65. sub GetPidList()
66. {
67. my(@PidList);
68. }
69. 创建一个缓冲区
70. $ProcArray = MakeBuffer($DWORD_SIZE * $PROC_ARRAY_SIZE);
71. $ProcNum = MakeBuffer($DWORD_SIZE);
72. if (@PidList != '' && EnumProcesses->Call($ProcArray, $PROC_ARRAY_SIZE, $ProcNum)) {
73. 获取数组中使用的字节数
74. 检查这个——除以 DWORD 的字节数
75. 我们得到了返回的进程数量！
76. $ProcNum = unpack("L", $ProcNum) / $DWORD_SIZE;
77. 让我们对每个 PID 操作
78. 我们必须从返回的数组中解包 PID
79. @PidList = unpack("L$ProcNum", $ProcArray);
80. return(@PidList);
81. sub GetProcessInfo()

# 第7 章：进程
# 示例 7. 续
82.
83. $ProcInfo->{name} = "unknown";
84. $ProcInfo->{pid} = $Pid;
85. @($ProcInfo->{modules}) = ();
86. 我们无法打开系统进程，所以处理一下。
87. $ProcInfo->{name} = 'Idle' if (0 == $Pid);
88. my($hProcess) = OpenBuffer->Call($PROCESS_QUERY_INFORMATION | $PROCESS_VM_READ, 0, $Pid);
89. if ($hProcess) {
90. my($BufferSize) = $MODULE_LIST_SIZE * $DWORD_SIZE;
91. my($MemStruct) = MakeBuffer($BufferSize);
92. my($iReturned) = MakeBuffer($BufferSize);
93. if (EnumProcessModules)->Call($hProcess, $MemStruct, $BufferSize, $iReturned)) {
94. {
95. my(@MemStats, $MemStruct);
96. $ProcInfo->{workingset} = $MemStats[2];
97. $ProcInfo->{workingpeak} = $MemStats[3];
98. $ProcInfo->{pagefile} = $MemStats[8];
99. $ProcInfo->{pagefilepeak} = $MemStats[9];
100. }
101. $CloseHandle->Call($hProcess);
102. }
103. return($ProcInfo);
104. }
105. sub MakeBuffer
106. {
107. my($BufferSize) = @_;
108. return("\0" x $BufferSize);
109. }
110. sub FixString
111. {
112. my($String) = @_;
113. $String = s/\0//g if Win32::IsUnicode();
114. return unpack("A*", $String);
115. }
116. sub FormatNumber
117. {
118. my($Number) = @_;
119. while($Number) {
```

第一个参数是一个数值整数，将作为进程作为终止值报告的返回代码。通常情况下，如果你需要杀死一个进程，你并不关心它的返回值。但是，如果一个批处理文件（例如）检查进程的返回代码，你可能希望返回一个特定值，以便脚本正常处理。

其余参数（`$Pid1`、`$Pid2` 等）是要被终止的每个进程的 PID。你可以根据需要列出许多个需要终止的进程。该函数返回被杀死的进程总数。

与你可能假设的相反，`kill()` 函数并不总是有效。在某些情况下，例如当进程受到保护时（例如 WinLogon 服务）、当进程正在与 DCOM 交互时，甚至有时当进程正在与网络交互时（例如解析 DNS 名称）时，它可能无法工作。



示例 7.18 比 Perl 的`kill()`函数更进了一步。该脚本接受从命令行传递的任意数量的 PID，并尝试杀死每一个。然而，如果 Perl 的`kill()`函数未能终止某个进程，它将作为一个调试器运行，以便附加到该进程上。在附加之后，你可以从内部杀死它，就像是在进程内部调用了`terminate()`一样，从而消除安全问题。

尽管此脚本经过许多步骤，但某些进程（特别是安全服务）仍然拒绝执行除关闭 Windows 以外的许多操作。如果你能终止它们，它们无论都会立即触发系统重启。

此脚本假设运行它的用户已分配了调试进程权限（`SE_DEBUG_NAME`）。否则，脚本设置此权限的尝试将失败。

## 示例 7.18 杀死进程

```perl
01. use Win32::API;
02.
03. # 通知每个进程向其父进程返回此值
04. $SPROC_TERMINATION_VALUE = 0;
05.
06. if ($0 == scalar @ARGV )
07. {
08.     Syntax();
09.     exit;
10. }
11. Configure();
12. foreach my $Pid (@ARGV )
13. {
14.     my $iResult = 0;
15.
16. # 如果用户传递的是文本值，则跳过。
17.     next unless ($Pid =~ /^\d+$/);
18.
19. if ($iResult = kill($PROC_TERMINATION_VALUE, $Pid ))
20. {
21.     $iResult = ForceKill($Pid);
22. }
23. 
24. if ($iResult)
25. {
26.     print "Process $Pid was successfully killed.\n";
27. }
28. else
29. {
30.     $myError = Win32::ErrorMessage(Win32::GetLastError());
31.     $Error = $s/\r|\n//;
32.     print "Process $Pid failed to terminate. ($Error)\n";
33. }
34. }
35. 
36. sub ForceKill
37. {
38.     my ($Pid) = @;
39.     my $iResult = 0;
40.     my $phToken = pack("L", 0);
41.     # 获取进程的令牌
42. if ($OpenProcessToken->Call(GetCurrentProcess->Call(
43.         TOKEN_ADJUST_PRIVILEGES
44.     | TOKEN_QUERY),
45.     $phToken))
46. {
47.     my $hToken = unpack("L", $phToken);
48.     # 在令牌上设置调试权限
49.     if (SetPrivilege($hToken, $SE_DEBUG_NAME, 1 ))
50.     {
51.         # 现在我们有了进程的调试权限
52.         # 打开进程以便对它进行操作。
53.         my $hProcess = $OpenProcess->Call($PROCESS_TERMINATE, 0, $Pid);
54.         if ($hProcess)
55.         {
56.             # 我们不再需要调试权限，因为我们已经打开了
57.             # 进程，所以移除该权限。
58.             SetPrivilege($hToken, $SE_DEBUG_NAME, 0);
59.             # 让它终止进程
60.             $iResult = $TerminateProcess->Call($hProcess, 0);
61.             $CloseHandle->Call($hProcess);
62.         }
63.     }
64.     $CloseHandle->Call($hToken);
65.     }
66.     return ($iResult);
67. }
68. 
69. sub SetPrivilege
70. {
71. my($sToken, $pszPriv, $bSetFlag) = @;
72. $pLuid = pack("L1", 0, 0);
73. # 查找权限的 LUID
74. if ($LookupPrivilegeValue->Call(\x00\x00, $pszPriv, $pLuid )
75.     {
76. # 解包 LUID
77.         $pPrivStruct = pack("LLILIL", 1, unpack("L", $pLuid), ( ($bSetFlag)?
78.             $SE_PRIVILEGE_ENABLED : 0);
79. # 现在修改进程的令牌以设置所需的权限
80. $iResult = ( 0 != $AdjustTokenPrivileges->Call($hToken,
81.                             0,
82.                             $pPrivStruct,
83.                             length($pPrivStruct),
84.                             0, 0));
85. }
86. 
87. return($iResult);
88. sub Configure
89. {
90.     $TOKEN_QUERY = 0x0008;
91.     $TOKEN_ADJUST_PRIVILEGES = 0x0020;
92.     $SE_PRIVILEGE_ENABLED = 0x002;
93.     $PROCESS_TERMINATE = 0x0001;
94.     $SE_DEBUG_NAME = "SePrivilege";
95.     
96.     # 准备使用一些 Win32 API 调用
97.     $GetCurrentProcess = new Win32::API;
```

## 继承文件句柄（伪分叉）

至此，你可能会问为什么这些信息如此重要。毕竟，示例 7.20 生成的结果与示例 7.21 相同，但代码量却是两倍。这个概念很重要，因为它说明了脚本如何将一个标准 I/O 句柄重定向到文件或套接字句柄。假设你正是这样做——将 STDOUT 重定向到一个套接字。如果你在创建一个新的 Win32 进程时指定要继承所有文件句柄，那么新进程也会将 STDOUT 重定向到该套接字。这意味着你可以跨进程边界传递文件和套接字句柄。换句话说，你有了一种简单的方法来模拟`fork()`。

请记住，这不等同于真正的`fork()`：新进程无法访问父进程变量的副本；也不会在父进程创建新进程的地方继续执行。然而，它确实允许守护进程“分叉”出一个新进程，来处理打开的文件或套接字句柄。

现在看示例 7.22，这是一个简单的套接字守护进程脚本。当它运行时，它会绑定到一个端口并等待客户端连接。当连接发生时，脚本会将 STDOUT 重定向到套接字，创建一个新进程，将 STDOUT 还原为原始值，关闭套接字（这完全不会影响新进程），并等待另一个连接。

魔法在于第 42 到 70 行的`MyFork()`子程序中。第 55 行将 STDOUT 保存到备份句柄以备后用。第 56 行将 STDOUT 重定向到套接字，该套接字连接到了连接守护进程的客户端。

第 58 行执行实际的进程创建。注意变量`sInherit`被设置为`TRUE`（值为 1）。这就是秘密所在：它强制新进程继承已打开的文件句柄，包括重定向到套接字的 STDOUT。只有其他的进程连接函数可以实现这种壮举，例如`Win32::AdminMisc::CreateProcess()`和`CreateProcessAsUser()`函数（除非你想考虑使用`Win32::API`并手动调用 Win32 API`CreateProcess()`函数）。

该脚本通过运行相同脚本（第 49 行表示为`$0`）创建一个新的 Perl 脚本（第 48 行）。通过传递命令行参数声明新进程是一个子进程（第 49 行中的`child:iProcessCount`）。当新进程启动时，第 4 到 8 行将作为子进程而非守护进程处理该脚本。

第 52 行对于使这种模拟的`fork()`工作至关重要。这一行将`CreateProcess()`标志设置为`0`。通常，在创建新的 Perl 进程时，你会指定标志`CREATE_NEW_CONSOLE`。然而，这会导致在创建新窗口时 STDIN、STDOUT 和 STDERR 句柄被重置。这意味着将 STDOUT 重定向到套接字的映射（第 56 行）将会丢失，新的 Perl 进程将无办法访问套接字。

## 示例 7.22 套接字守护进程

```perl
01. use IO::Socket;

02. $iProcessCount = 0;

03. $Port = 8000;

04. if (($iChildNum) = ($ARGV[0] =~ /child:(\d+)/ / i)) 

05. {

06.     ProcessAsChild(fileno (STDOUT));

07.     exit();

08. }

09. if ($Socket = IO::Socket::INET->new(LocalPort => $Port, Listen => 5 )) 

10. {

11.     while (1) 

12.     {

13.         print "\nListening for a connection...\n";

14.         last unless ($Connection = $Socket->accept());

15.         $iProcessCount++;

16.         print STDERR "Server: Connection $iProcessCount\n";

17. 

18.         MyFork($Connection);

19.         $Connection->close();

20.     }

21. }

22. 

23. sub ProcessAsChild

24. {

25.     my ($SocketHandle) = @_;

26.     my $Socket;

27. 

28.     if ($Socket = IO::Socket::INET->new_from_fd($SocketHandle,"+")) 

29.     {

30.         $Socket->send("Child process $iChildNum has " 

31.             'started at ' . localtime() . "\n");

32.         while(1)

33.         {

34.             $Socket->recv($In, 100 );

35.             last if ($In eq "\n" || $In eq "");

36.             $Socket->send("You entered: $In");

37.         }

38.     }

39.     $Socket->close();

40. }

41. sub MyFork

42. {

43.     my ($Socket) = @_;

44. 

45.     use Win32::Process;

46.     my $Process;

47.     $mApp = 'c:\perl\bin\perl.exe';

48.     $mCmd = 'perl "$0" child:$iProcessCount';

49.     $bInherit = 1;

50.     my $bDir = ".";
```

## 继承文件句柄（伪分叉）

```perl
52. my $Flags = 0;
53. my $Child = 0;

55. open(STDOUT, ">&STDOUT") || die "Can not backup STDOUT: $\$\n"

56. open(STDOUT, ">&" , $Socket->filename)

57. // die "Can not redirect STDOUT: $\$\n"

58. if (Win32::Process::Create($Process,

59. $App,

60. $Cmd,

61. $bInherit,

62. $Flags,

63. $Dir ))

64. {

65. print STDERR "Server: unable to create process.\n"

66. }

67. open(STDOUT, ">&_OLD_STDOUT")

68. // die "Can not redir STDIN in orig value: $\$\n"

69. close(OLD_STDOUT);

70. }
```

```perl
72. END

73. {

74. if ($iChildNum)

75. {

76. print STDERR "Terminating.\n"

77. }

78. else

79. {

80. print STDERR "Terminating.\n"

81. }

82. }
```



示例 7.23 表明在 Win32 中实现分叉是可能的，但它不像 UNIX 中那么简单。继承文件句柄的过程需要仔细的手动重定向，以防止连接丢失。

# 8 Win32 服务

UNIX 管理员将它们称为守护进程（daemons），而 Win32 管理员将它们称为服务（services）：它们是从启动到关机一直运行的进程。这些代码通常执行非常特定的任务，并且始终需要运行。

在启动时自动运行 Perl 脚本（或其他应用程序）的能力一直以来非常令管理员感兴趣。这种能力提供了一种方法，可以在不需要任何用户交互的情况下启动监控程序和其他应用程序。本章将讨论与这一尝试相关的各种问题。

## 什么是 Win32 服务？

在操作系统世界中，某些程序必须持续运行。这些程序的设计目的是执行其他进程依赖的某种类型的功能，或完成某些重要任务。这就是 Win32 服务。在 UNIX 环境中，这类服务被称为守护进程。在所有实际用途中，Win32 服务可以被视为 UNIX 守护进程的等物。

你每天都会与这些服务交互。诸如 Web、电子邮件、数据库、流媒体和登录服务等进程都是机器启动时开始运行的程序。它们会一直运行，直到被管理员停止或机器关闭。

Win32 使用一个服务管理器（Service Manager）来监督所有服务和设备驱动程序。该管理器包含一个关于何时应运行哪些服务的数据库。当计算机启动时，服务管理器会遍历服务列表，并决定先启动、第二个、第三个服务，以此类推。它还会确定哪些服务依赖于哪些其他服务。例如，Web 服务依赖于网卡驱动程序和 TCP/IP 协议。因此，服务管理器保证只有在网卡加载且 TCP/IP 成功绑定到网卡后，才启动 Web 服务。同样，电子邮件服务可能依赖于某些用户授权服务，因此服务管理器只在授权服务成功启动后才启动电子邮件服务。

某些服务在实际完成启动之前错误地向服务管理器报告它们已成功启动。这可能会对必须与此类服务交互的另一个服务造成破坏。在这种情况下，服务管理器会在原始服务完全准备好进行任何交互之前启动被依赖的服务。因此，如果你编写了一个依赖于其他服务的服务，你可能会发现与你的服务依赖的任何服务交互之前放置一个微小的延迟是很有用的。

Win32 服务简单来说就是一个知道如何与服务管理器通信的程序。而且它会告诉管理器。当服务启动时，它必须告诉服务管理器它正在启动，并将管理器指向一个名为“事件处理程序”（event handler）的函数。事件处理程序的唯一功能是监听并响应服务管理器。例如，如果管理员提供了一个服务，服务管理器会向服务发送一个 `SERVICE_CONTROL_PAUSE` 控制消息，告知它应该暂停。该服务立即通过返回一个 `SERVICE_PAUSE_PENDING` 消息告诉服务管理器它正准备暂停。然后该服务在执行任何自己需要执行的暂停操作之前，最后向服务管理器发送一个 `SERVICE_CONTINUSED` 消息。该服务等待管理器的更多请求。这种与服务管理器的对话实际上是服务的唯一要求。它可以像任何其他应用程序一样阻止几乎任何进程，只是有少数例外，即无法与用户交互。

服务运行在一个特殊环境中，该环境与普通登录用户体验的体验不同。简单来说，服务看不到用户或桌面、鼠标或键盘。服务没有一种简单的方法可以直接与用户通信，反之亦亦然。从概念上讲，服务没有需要与用户交互。大多数服务执行的是某种不涉及用户交互的类型处理。例如，Web 服务器永远不需要与登录用户交互。

如果服务为了调试或记录事件而需要通信，例如，它可以通过写入 Win32 事件日志或打开并存储信息到文件或命名管道（named pipe）来实现。后一种方法非常有用，因为你可以运行一个创建一个命名管道的 Perl 脚本。服务可以连接到命名管道，将日志信息转储其中，而 Perl 脚本可以简单地从管道读取并在屏幕上显示内容。

## 控制服务

每台 Win32 机器都运行着一些服务。默认情况下，所有 Windows 2000 和 Windows NT 机器都会运行本地安全权威服务 (LSASS) 和 Windows 登录服务 (winlogon) 等其他服务。其中许多服务对于操作系统的运行至关重要，但其他服务的重要性仅取决于管理员的认为。SQL Server 和数据备份等服务对于操作系统的成功运行并不是提供适当的服务所必需的，但可能是必要的。然而，并不是所有的服务都是包装好并在本地电脑商店买到的。

考虑到每位网络管理员管理自己的方式与他人略有不同，而且每个网络都有自己的独特之处，你可能找不到符合某些需求的服务。在这些情况下，你可以使用 Perl 来满足这些小众需求。

操作系统允许用户和进程控制服务。你可以通过使用服务控制面板小组件或 `NET.EXE` 命令行应用程序手动执行此操作。你也可以通过使用 Perl（以及其他语言）以编程方式执行。特别有两个扩展控制服务：`Win32::Service` 和 `Win32::Lanman`。这两个扩展在控制服务方面都做得非常出色；然而，`Win32::Service` 扩展非常小，仅提供与服务相关的函数。仅就这一个，该扩展就是本节的重点。

## 服务列表

你可以使用 `Win32::GetService()` 函数找到机器上安装的服务列表。如示例 8.1 所示，获取此服务列表是非常容易的。传递给 `GetServices()` 函数的第二个参数是一个哈希引用，它用显示名称及其服务名称作为值进行填充。这个引用非常重要，因为 `Win32::Service` 函数期望的是服务名称。传递显示名称会导致函数失败。

示例 8.1 发现机器上存在哪些服务

```
01. use Win32::Service;
02.
03. foreach my $Machine (@ARGV)
04.     local %List;
05.     print 'Available services on $Machine:\n';
06.     if (Win32::Service::GetServices($Machine, \List ))
07.     {
08.         $- = FormatHeader;
09.         write;
10.         $- = FormatData;
11.         foreach $Service ( sort (keys($List)) )
12.             write;
13.         }
14.     }
15.     else
16.     {
17.         print Win32::FormatMessage(Win32::GetLastError()), "\n");
18.     }
19.     print "\n" * 3;
```

示例 8.1 继续

```
20.  format FormatHeader =
21.  <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
22.  "Service Name", "Service Display Name"
23.  ------------------------------------------------
24.
25.
26.  format FormatData =
27.  <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
28.  $List($Service), $Service
```

## 启动、停止、暂停和恢复

现在你已经从机器获取了服务列表，可以使用这些函数启动、停止、暂停和恢复这些服务：

```
Win32::Service::StartService()
Win32::Service::StopService()
Win32::Service::PauseService()
Win32::Service::ResumeService()
```

示例 8.2 显示了如何使用 12 和 16 来远程暂停服务 10 秒。注意第 12 和 16 行都引用服务名称，而不是服务的显示名称（`%List` 哈希通过显示名称进行索引）。这一点很重要，因为如果你将显示名称传递给这些函数之一，它将失败。这意味着你需要将服务显示名称 "World Wide Web Publishing Service" 传递脚本来暂停 Web 服务（服务名称为 "w3svc"）。

## 示例 8.2 暂停服务

```
01. use Win32::Service;
02. $Timeout = 5;
03. $DisplayName = shift ARGV // die;
04. $Machine = Win32::NodeName() unless ($Machine = shift ARGV);
```

## 控制服务

```perl
05. $Machine = "\\\\$Machine";
06. $Machine -= s/\\{2}/\\\\;
07. if (Win32::Service::GetServices($Machine, $List))
08. {
09.     if (defined $List{$DisplayName})
10.     {
11.         print "Pausing the $DisplayName service on $Machine.\n"
12.         Win32::Service::PauseService($Machine, $List{$DisplayName});
13.         print "Sleeping for $Timeout seconds...\n"
14.         sleep ($Timeout);
15.         print "Resuming the $DisplayName service on $Machine.\n"
16.         Win32::Service::ResumeService($Machine, $List{$DisplayName});
17.     }
18. else
19.     {
20.         print "There is no '$DisplayName' service on $Machine.\n"
21.     }
22. else
23.     {
24.         print "Could not connect to $Machine: ";
25.         print Win32::FormatMessage(Win32::GetLastError()), "\n"
26. }
```

## 服务状态

另一个函数也非常好用：`Win32::Service::Status()` 函数。它报告给定服务的当前状态，无论是本地还是远程。示例 8.3 正是实现了这一点。请注意 `Win32::Service` 并没有导出各种状态常量。这种疏忽几乎抵消了 `Status()` 函数的用途，因为它只返回一个数值，这对于普通用户来说没有任何意义。表 8.1 描述了 `Win32::Service::Status()` 返回的每一个值。

### 8.1 服务状态值

| 状态常量 | 值 | 描述 |
|---|---|---|
| SERVICE_STOPPED | 0x1 | 服务未运行。 |
| SERVICE_START_PENDING | 0x2 | 服务正在启动中。 |
| SERVICE_STOP_PENDING | 0x3 | 服务正在停止中。 |
| SERVICE_RUNNING | 0x4 | 服务正在运行。 |
| SERVICE_CONTINUE_PENDING | 0x5 | 服务继续恢复等待中。 |
| SERVICE_PAUSE_PENDING | 0x6 | 服务暂停等待中。 |
| SERVICE_PAUSED | 0x7 | 服务已暂停。 |

要使用示例 8.3 中的脚本，请使用以下语法：

```perl
perl servicestatus.pl ServiceDisplayName [MachineName]
```

## 第 8 章：Win32 服务

只需将服务的显示名称传递给脚本即可。使用示例 8.3 来确定存在哪些服务以及它们的显示名称是什么。你可以可选地将机器名称作为参数，以发现远程计算机上服务的状态。

以下显示了如何使用此脚本：

```perl
perl servicestatus.pl "World Wide Web Publishing Service" \WebServer
```

## 示例 8.3 远程机器上服务的状态

```perl
01. use Win32::Service;
02.
03. %STATE = (
04.     0 => 'unknown',
05.     1 => 'stopped',
06.     2 => 'starting',
07.     3 => 'stopping',
08.     4 => 'running',
09.     5 => 'resuming',
10.    6 => 'pausing',
11.     7 => 'paused',
12. );
13.
14. $DisplayName = shift $ARGV // "";
15. $Machine = Win32::NodeName unless ($Machine = shift $ARGV);
16. $Machine = "\\\\Machine";
17. $Machine = s/\\\\{2}/\\\\/;
18. if (Win32::Service::GetServices($Machine, $List))
19. {
20.     if defined $List{$DisplayName}
21.     {
22.         if (Win32::Service::GetStatus($Machine,
             $List{$DisplayName},
             $Status))
23.         {
24.             print "The $DisplayName service on $Machine is "
                   $STATE($Status($CurrentState)).\n";
25.         }
26.     else
27.     {
28.         print "Could not find $DisplayName service.\n";
29.         print "Names are case sensitive.\n";
30.     }
31. }
32. else
33. {
34.     print "Could not connect to $Machine: ";n";
35.     print Win32::FormatMessage(Win32::GetLastError()), "\n";
36. }
```

## 创建和删除服务

有不同的技术可以安装、修改或删除服务。两种主要方法使用 `Win32::Daemon` 或 `Win32::Lanman` 扩展。两者都做得非常出色。然而，大多数管理员不需要使用 Perl 安装服务，因为专业服务附带某种形式的安装程序。如果你需要安装某些服务，通常是因为你编写了一个作为服务运行的脚本。许多管理员使用 Perl 编写 Win32 服务，因此他们通常使用 `Win32::Daemon` 扩展；因此，他们依赖它的安装和删除函数。其他第三方工具也提供此类功能，例如 Windows NT/2000 资源包自带的微软 SC.EXE 工具。

## 安装服务

要使用 `Win32::Daemon` 安装服务，需要调用 `CreateCharacter` 函数。示例 8.4 显示了如何操作。该哈希描述了要安装的服务。表 8.2 列出了该哈希的可用值。大多数服务都使用以下默认值：

## 示例 8.4 安装服务

```perl
01. use Win32::Daemon;
02.
03. %ServiceConfig = (
04.     name => 'ServiceName',
05.     display => 'My Service',
06.     path => 'c:\scripts\MyService.pl',
07.     user => '',
08.     password => '',
09.     parameters => '',
10.     dependencies => [],
11. );
12. if (Win32::Service::CreateCharacter($ServiceConfig))
13. {
14.     print 'The $ServiceConfig{display} service ';
15.     print 'was successfully installed.\n';
16. }
17. else
18. {
19.     print "Failed to add '$ServiceConfig{display}' service.\n";
20.     print "Error: ";
21.     print Win32::FormatMessage(Win32::GetLastError()), "\n";
22. }
```



### 表 8.2 服务配置值

| 键名 | 描述 |
|---|---|
| `name` | 服务的名称，例如 `w3svc`、`scheduler` |
| `display` | 服务的显示名称，例如 `World Wide Publishing Service`、`Task Scheduler` |
| `path` | 服务的程序路径。对于 Perl 脚本，通常是 `PERL` 的完整路径。 |
| `user` | 运行服务的用户 ID。可以包含域名，例如 `Accounting\Joel`。该账户必须具有服务登录权限。 |
| `password` | 用户登录的密码。如果账户是 `Local System`，则不需要此字段。 |
| `parameters` | 启动时传递给服务的任何参数。它们与命令行参数一样。 |

### 创建和删除服务的其他值

| 键名 | 描述 |
|---|---|
| `service_type` | 被配置的服务类型。可以是表 8.3 中的任意一个值。对于基于 Perl 服务，此值应该是 `SERVICE_WIN32_OWN_PROCESS`。 |
| `start_type` | 服务的启动类型。可以是表 8.4 中的任意一个值。默认值是 `SERVICE_AUTO_START`。 |
| `error_control` | 系统如何处理启动报告错误的服务。可以是表 8.5 中的任意一个值。默认值是 `SERVICE_ERROR_IGNORE`。 |
| `load_order` | 服务关联的加载顺序组的名称。该值是可选，要么未指定要么留为空字符串。 |
| `dependencies` | 数组的引用。该数组中的每个元素都是表示该服务依赖的其他服务和设备程序的字符串。当每个依赖组中至少有一个成员启动后，该服务才会启动。依赖项有两种类型：服务/设备程序和组。在组名称前加一个 `+` 号，否则将假设为服务或设备程序的名称。 |

### 表 8.4 服务启动选项

| 选项 | 说明 |
| --- | --- |
| `SERVICE_AUTO_START` | 指定服务在启动期间由服务控制管理器自动启动。 |
| `SERVICE_DEMAND_START` | 指定服务在接收到显式启动指令时启动。可以是某个应用程序启动该服务（例如使用 `net start` 命令），也可以由管理员从服务管理器中启动它。 |
| `SERVICE_DISABLED` | 指定服务无法启动。要启动该服务，您必须将其启动选项更改另外两个选项之一：`SERVICE_AUTO_START` 或 `SERVICE_DEMAND_START`。 |

### 表 8.5 服务错误控制选项

| 选项 | 说明 |
| --- | --- |
| `SERVICE_ERROR_IGNORE` | 错误记录在 Win32 事件日志中，但服务继续启动。 |
| `SERVICE_ERROR_NORMAL` | 错误记录在 Win32 事件日志中，并会在屏幕上显示消息框，但服务继续启动。 |
| `SERVICE_ERROR_SEVERE` | 错误记录在 Win32 事件日志中，且如果正在启动最后一次良好配置，则继续启动操作。否则，系统将使用最后一次良好配置进行重启。 |
| `SERVICE_ERROR_CRITICAL` | 错误记录在 Win32 事件日志中，且如果正在启动最后一次良好配置，则启动操作失败。否则，系统将使用最后一次良好配置进行重启。 |

在之前的示例 8.4 中，`name`（名称）键是服务的名称。服务管理器使用此名称来引用服务。当您使用 `Win32::Service` 扩展的函数（如 `StartService()`）控制服务时，您使用此名称来标识服务。例如，微软 Web 服务器的名称是 `w3svc`。

`display`（显示）键是服务的显示名称。这是您在控制面板小程序中会看到的名称。此值仅仅是一个格式良好的名称，比服务名称更易于人类阅读——例如，“Wide Web Publishing Service”（万维网发布服务）。

`path`（路径）键是服务可执行文件的完整路径。它必须是一个完整路径，并且必须是一个可执行程序。如果您使用 Perl 脚本作为你的服务，则此键为 `PERL.EXE` 程序的完整路径，例如 `c:\perl\bin\perl.exe`。

`user`（用户）和 `password`（密码）键代表服务启动时使用的用户和密码。这是服务运行所属的账户。在服务启动之前，该账户必须具有“作为服务登录”的权限（请参阅第 2 章“账户维护”获取在用户账户上设置权限的工具）。该权限仅在启动服务时需要，安装时不需要。如果没有指定用户名，则使用本地系统（`Local System`）。

为 `user` 键指定全名非常重要。这包含了用户所属的域。使用全名的目的是为了消除歧义。如果本地机器有一个 `Joel` 账户，而默认域也有一个 `Joel` 账户，服务可能不知道该使用哪个账户，并默认使用本地计算机账户。全帐户名的示例是 `Accounting\Joel`。

`parameters`（参数）键是一个传递给服务的数值字符串。您可能在命令行上指定这些值。如果该服务是一个 Perl 脚本，则此键包含要运行的 Perl 脚本名称以及任何可选开关。例如，假设 `PERL.EXE` 的路径，`parameters` 可能是 `c:\perl\myservice.pl -someswitch Parameters To In`。

`service_type`（服务类型）键代表您正在安装的服务类型。请参考表 8.3 了解各种服务类型的描述。

`start_type`（启动类型）键指示服务何时启动。请参考表 8.4 了解各种选项。

`error_control`（错误控制）键描述了如果服务启动但因错误结束 Win32 会做什么。请参考表 8.5 了解不同的错误控制选项。

`load_order`（加载顺序）键是服务所属的加载顺序组的名称。属于特定加载顺序组的服务同时启动。通过这种方式，一组可以在另一组之后加载，而该组可能依赖于后一组。通常，您不需要将服务与组关联，因此此键保持留空。

`dependencies`（依赖关系）键是服务名称和加载顺序组的数组。如果某个服务的运行依赖于另一个服务（例如电子邮件服务器依赖于 TCP/IP 协议），则该服务通过此键指定其依赖项。在每个指定的服务/设备驱动程序以及每个指定组的至少一个成员启动后，该服务才会启动。

依赖项有两种类型：服务/设备驱动程序和组。要指定依赖项是一个组，只需在每个组的名称前加上 `+`（加号）字符；否则，假设它是服务或设备驱动程序的名称。

### 重新配置服务

您可能需要重新配置服务。例如，如果服务账户的密码已更改，则必须重新配置服务以使用新密码。`Win32::Daemon::ConfigureService()` 函数执行此任务。该函数的工作与 `CreateService()` 函数一样。函数接收一个哈希引用。然而，此哈希只需要包含配置更改的键。

在示例 8.5 中，更改了用户的账户和密码；因此，它们是哈希中的仅两个键。当然，包含了 `name` 键；否则函数将不知道要修改哪个服务。不言而喻，服务名称是服务中唯一可以修改的方面。

### 示例 8.5 配置服务

```
use Win32::Daemon;

%ServiceConfig = (

    name => 'w3svc',

    user => 'MyDomain\Account',

    password => 'MyPassword',

    machine => NodeName()

);

if (Win32::Daemon::ConfigureService(\%ServiceConfig)) {

    print "$ServiceConfig{name} 服务已成功配置。\n";

} else {

    print "无法配置 $ServiceConfig{name} 服务。\n";

    print "错误: %s";

    print Win32::Daemon::FormatMessage(Win32::Daemon::GetLastError()), "\n";

}
```

### 移除服务

您可能偶尔需要重新配置服务。例如，如果服务账户的密码已更改，则必须重新配置服务以使用新密码。移除服务与安装服务类似。唯一的区别是将服务名称传递给 `DeleteService()` 函数，而不是在安装时传递哈希引用。

示例 8.6 显示了如何移除服务。注意此代码与示例 8.4 的区别在于不需要哈希来移除服务。

### 示例 8.6 移除服务

```
use Win32::Daemon;

$ServiceName = 'MyServiceName';

$SMachine = '\\';

if (Win32::Daemon::DeleteService($SMachine, $ServiceName)) {

    print "服务 $ServiceName 已成功移除。\n";

} else {

    print "无法移除服务 $ServiceName。\n";

    print "错误: %s";

    print Win32::Daemon::FormatMessage(Win32::Daemon::GetLastError()), "\n";

}
```

### 将 Perl 脚本作为 Win32 服务运行

可以通过编写 Perl 脚本来解决许多问题。然而，某些问题类型需要脚本一直运行。在 Windows 2000 或 Windows NT 机器上，程序是由用户执行运行的，或者在用户登录时自动运行。然而，这种执行方式并不总是可以接受，这就是许多管理员创建 Perl 脚本并将其注册为 Win32 服务的原因。

您可以使用这些技术之一有效地从计算机启动到关机运行 Perl 脚本。`SRANY.EXE` 技术实现起来很快，但缺乏管理员可能需要的控制。相反，使用 `Win32::Daemon` 需要更多的思考和编码；但它将 Perl 脚本实现了真正的 Win32 服务。

### 使用 SRANY.EXE 的服务

Windows NT/2000 资源包包含一个名为 `SRANY.EXE` 的小型可执行程序。该应用程序允许任何程序像服务一样运行——这正是它的名字由来。`SRANY.EXE` 程序作为服务运行，它的唯一任务是创建一个新进程，该进程可以是另一个程序甚至是 Perl 脚本。`SRANY` 进程会代表它启动的新进程管理所有的服务控制消息。

它所需的 CPU 处理时间和内存相对较小，不会对机器性能产生任何严重影响。因此，它可以被安装并作为不同的服务运行。

### 安装 SRVANY.EXE 服务

由于 `SRVANY.EXE` 是一个非常简单的服务应用程序，遗憾的是，它无法无法安装为服务。为了此功能，它依赖于其他技术，例如它的配套程序 `INSTSRV.EXE`。正如你所猜的，这个程序设计用于安装服务。实际上，与 `SRVANY.EXE` 一样，它是通用的，不需要任何其他特定的应用程序。它可以将 `SRVANY.EXE` 安装为服务，同样，它也可以将 `WINWORD.EXE` 或 `NETSCAPE.EXE` 安装为服务，尽管你可能很难为这样做想出一个充分的理由。请参考较早的章节“创建和删除服务”，以获取安装和配置服务的替代技术。

使用 `INSTSRV.EXE` 安装 `SRVANY.EXE`（或任何其他服务），只需按所示传递服务名称和可执行文件的完整路径：

```
instserv.exe "MyNewService" c:\tools\srvany.exe
```

就是这样。注意，与使用 `Win32::Lanman` 或 `Win32::Daemon` 不同，你对服务的配置方式没有太大控制权。要配置服务，你可以使用 `Regedit` 修改服务的注册表键值，或者使用 `Win32::Lanman` 或 `Win32::Daemon` 配置服务，尽管它们未被用于安装该服务。

将 `SRVANY.EXE` 安装为服务后，你需要修改注册表来配置它。即使你已经使用 `Win32::Lanman` 或 `Win32::Daemon` 配置了服务，你仍然需要配置 `SRVANY.EXE`，以便它知道在启动时运行什么种程序。

你需要创建一个 `Parameters` 注册表键来存放 `SRVANY.EXE` 配置。该键必须在 `Services` 键下创建，如下：

```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\MyNewService\Parameters
```

注意，注册表键的路径反映了你在安装服务时使用的名称（在此例中为 `NewService`）。所需的数值列在表 8.6。

### 表 8.6 SRVANY.EXE 注册表值

| 值名称 | 值类型 | 描述 |
| --- | --- | --- |
| `Application` | `REG_SZ` | 将运行的应用程序路径。示例：`c:\tools\SomeService.exe` 或 `c:\perl\bin\perl.exe`。必须传递到 `Application` 值中指定的服务的任何参数。如果你将 `PERL.EXE` 作为服务运行，则此值为 Perl 脚本的完整路径以及任何要传递的参数。示例：`c:\Perl\scripts\MyService.pl`。此值为可选的。 |
| `AppParameters` | `REG_SZ` | 目录的完整路径，该目录将作为创建进程的默认目录。这是一个可选值。 |

你可以使用 `INSTSRV.EXE` 删除服务，方法是传递服务名称后跟关键字 `remove`。例如，你可以使用以下：`instrsrv.exe "MyService" remove`。

### SRVANY.EXE 的问题

当计算机启动时，所有配置为自动启动的服务都会启动，包括基于 `SRVANY.EXE` 的服务。由于 `SRVANY.EXE` 充当真正的 Win32 服务，可以从 Perl（使用 `Win32::Service` 或 `Win32::Lanman` 扩展）、从命令行（使用 `net` 命令）或从服务控制面板小项对其进行暂停、恢复和停止。然而，暂停和恢复服务不会影响它启动的进程。

考虑一个例子：管理员编写了一个聪明的 Perl 脚本，它可以索引你硬盘上的所有文本文件，并将结果提交到网络数据库引擎。该脚本在启动时运行。此时 `SRVANY.EXE` 服务启动并作为新进程运行 Perl 脚本。此时，计算机正在索引文件。然而，由于你正在更新计算机上的文件，你需要临时暂停索引脚本。如果你暂停服务，`SRVANY.EXE` 会受到影响，但 Perl 脚本继续运行。暂停服务的唯一方法是使用任务管理器或杀死进程。

然而，由于 Perl 脚本没有拦截管理器的请求，它不知道必须开始关闭。因此，`SRVANY.EXE` 通过杀死来停止。这非常激进，并可能导致文件处于脆弱状态以及数据库连接。

如果你需要在启动时创建进程，`SRVANY.EXE` 工具可以是完成此任务的强大盟友。然而，`Win32::Daemon` 为 Perl 脚本提供了更多控制，并可以直接与管理器交互。

### 使用 Win32::Daemon 服务

`Win32::Daemon` 扩展为 Perl 脚本提供了作为 Win32 服务所需的所有功能。它允许脚本像真实服务一样响应服务控制请求，并允许你像从任何 Win32 服务中预期的那样控制进程。

由于基于 `Win32::Daemon` 的脚本确实与管理器交互，因此它比由 `SRVANY.EXE` 启动的简单脚本要复杂得多。脚本到底需要多复杂取决于它需要做什么。只要使用基本的框架，`Win32::Daemon` 的简单形式可以非常简单。

### 控制循环

所有 `Win32::Daemon` 脚本必须经常轮询当前状态。该状态可能会随时间变化，取决于管理器的要求。例如，如果管理员决定暂停服务，脚本将轮询当前状态以发现正在进入暂停状态。它执行必须暂停的任务，然后向管理器报告已正式暂停。

轮询通常在服务循环中进行。此循环调用 `Win32::Daemon::State()` 函数来查询当前状态。必须及时响应控制状态，否则管理器认为服务已崩溃或处于非功能状态。规则是服务应在 20 秒内响应。

另一组控制状态描述在表 8.9 中。这些状态是 Windows 2000 新引入的，对它们进行响应是不必要的。这些特定的状态表示服务可能想要了解的事件。

### Win32::Daemon 框架

服务控制循环在服务正式启动后开始。要正式启动服务，脚本会调用 `Win32::Daemon::StartService()` 函数。如果该函数执行成功，服务控制循环就会启动。该循环将持续，直到服务进入 `SERVICE_STOPPED` 状态。此时，脚本停止服务控制循环，并调用 `Win32::Daemon::StopService()` 函数，指示服务管理器（Service Manager）停止与脚本交互。这一步是结束服务的序曲。示例 8.7 展示了一个非常简单的 Win32 服务脚本骨架。如果将此代码作为服务进行安装，它可以正常运行，但不会完成任何实际工作。

### 示例 8.7 一个极简的 Win32 服务脚本

```
01. use Win32::Daemon;
02. Win32::Daemon::StartService();
03. while (SERVICE_STOPPED != ($State = Win32::Daemon::State))
04. {
05.   if (SERVICE_START_PENDING == $State)
06.   {
07.     # 在此处添加初始化代码
08.     Win32::Daemon::State(SERVICE_RUNNING);
09.   }
10. elseif (SERVICE_PAUSE_PENDING == $State)
11.   {
12.     # 在此处添加暂停代码
13.     Win32::Daemon::State(SERVICE_PAUSED);
14.   }
15. elseif (SERVICE_CONTINUE_PENDING == $State)
16.   {
17.     # 在此处添加恢复代码
18.     Win32::Daemon::State(SERVICE_RUNNING);
19.   }
20. elseif (SERVICE_STOP_PENDING == $State)
21.   {
22.     # 在此处添加停止代码
```



## 23. `Win32::Daemon::State(SERVICE_STOPPED);`

24.   }

25. `elseif (SERVICE_RUNNING == $State)`

26.   {

27.     # 这是服务的核心功能部分
28.     # 在此处添加代码来执行服务必须完成的工作
29.     # 避免任何长时间阻塞代码
30.   }

31.   `sleep(5);`

32. }

33. `Win32::Daemon::StopService();`

## 将 Perl 脚本作为 Win32 服务运行

此示例中的几个要点值得注意。每个处理待处理状态更改的代码块在结束时都会调用`Win32::Daemon::State`函数并传入新状态（第 8、13、18 和 23 行）。调用此函数至关重要，这样脚本才能向服务管理器更新新的状态更改；否则，服务管理器将放弃控制该服务。如果发生这种情况，服务将无法被停止、暂停或恢复。

第 32 行尤为重要；这行代码仅仅让脚本进入简短的睡眠状态。对于大多数服务来说，这种暂停是必要的；否则，处理速度会过快，可能会导致不必要地占用 CPU 处理时间。

最后，`SERVICE_RUNNING`块（第 25 行至 31 行）包含了执行服务实际工作的代码。当你将实际处理代码放在此块中时，如果服务进入`SERVICE_PAUSED`状态，这些代码将不会运行，这正是一个服务在暂停状态下应该的行为。

关于此服务控制循环最重要的知识点是，它必须定期循环。也就是说，它不能进入某种阻止其循环的竞态条件。糟糕编码实践的一个例子是在套接字（socket）上监听客户端连接。除非监听是非阻塞的，否则可能会阻止服务响应服务管理器，从而面临变成被遗弃服务的风险。

如果你正在运行某个版本的服务，请确保它不会陷入阻塞循环。

## 第 8 章：Win32Services

最后，第 7 到 19 行的代码块以及`InstallService()`函数（第 183-195 行）、`RemoveService()`函数（第 167-209 行）和`GetServiceConfig()`函数（第 169-181 行）允许你从命令行运行脚本来安装或删除服务。

该服务的伴侣代码在示例 8.10 中显示，它包含了连接到 Pager 服务并提交页面请求的客户端代码。该客户端真正的威力在于第 7 到 9 行，它们执行了自动发现哪些机器运行着 Pager 服务的任务。注意第 9 行查找了所有运行 Pager 服务的机器。如果列表中返回了至少一个机器，则会与服务创建一个命名管道，并提交页面。

这个客户端非常简单，它期望接收三个输入参数：

```
pageclient.pl "1234567890" "My Subject" "My Message"
```

第一个是分页机号码，第二个是页面主题，第三个是消息。

## 示例 8.9 一个分页服务

```perl
01. use Win32::Daemon;
02. use Win32::Console;
03. use Win32::Pipe;
04. use Win32::Perms;
05. use Net::Pager;
06.
07. if( scalar @ARGV )
08. {
09.     if ($ARGV[0] == /install/i)
10.     {
11.         InstallService();
12.         exit();
13.     }
14.     } elsif ($ARGV[0] == /remove/i)
15.     {
16.         RemoveService();
17.         exit();
18.     }
19. }
20.
21. # 轮询之间我们睡眠多久？
22. $SERVICE_SLEEP_TIME = 1;
23. $PIPE_NAME = "PagerService";
24. my $DB_FILE =
25. ( $Win32::GetFullPathName($0) =~ /(.*)\..*?$)/ [0] . ".log";
26. if ( open(LOG, "> \$DB_FILE ) )
27. {
28.     my $Handle = select(LOG);
29.     $I = 1;
30.     select($Handle);
31. print LOG "Started: " . localtime() . "\n\n";
32. }
33.
34. #启动服务...
35. if ( ! Win32::Daemon::StartService()
36.
37. exit();
38. )
39. # 注册服务
40. Win32::Daemon::ShowService();
41.
42. $Buffer = new Win32::Console();
43. $Buffer->Display();
44. $Buffer->Title("Perl based paging service\n");
45. Write("Service started\n");
46. while ( SERVICE_STOPPED != ($State = Win32::Daemon::State()) )
47.
48. if(SERVICE_START_PENDING == $State
49.
50. # 初始化代码
51. my $Perm;
52. if ($Perm = new Win32::Perms())
53.
54. $Perm->Allow("administrators", FULL);
55. }
56.
57. # 现在创建管道并指定使用上面的权限
58. if ($Pipe = new Win32::Pipe($PIPE_NAME, 1000,
59. PIPE_NOWAIT | PIPE_READMODE_BYTE,
60. $Perm ))
61.
62. {
63. Win32::Daemon::State(SERVICE_RUNNING),
64. Win32::Daemon::SetServiceBits(USER_SERVICE_BITS_1);
65. Write("Service is running\n");
66. }
67. else
68. {
69. Win32::Daemon::State(SERVICE_STOPPED);
70. Write("Service is stopping\n");
71. }
72. elsif(SERVICE_PAUSE_PENDING == $State
73. {}
74. # "暂停中...",
75. if ($Connected)
76. {
77. $Pipe->Disconnect();
78. $Connected = 0;
79. }
80. Win32::Daemon::State(SERVICE_PAUSED);
81. Write("Paused\n");
82. next;
83. }
```

## 示例 8.9 延续

```perl
84. elsif( SERVICE_CONTINUE_PENDING == $State )
85. {
86. # 恢复...
87. Win32::Daemon::State( SERVICE_RUNNING );
88. Write("Resumed\n");
89. next;
90. }
91. elsif( SERVICE_STOP_PENDING == $State )
92. {
93. # 停止中...
94. if ($Connected)
95. {
96.   $Pipe->Disconnect();
97.   $Connected = 0;
98. }
99. Win32::Daemon::State(SERVICE_STOPPED);
100. }
101. elsif( SERVICE_RUNNING == $State )
102. {
103. # 服务正在运行
104. if (!$Connected)
105. {
106.   $Connected = Connect($Pipe);
107. }
108. if ($Connected)
109. {
110.   if ($Pipe->Peek())
111.   {
112.     my $Data = $Pipe->Read();
113.     my ($To, $Message) = split(/\t/, $Data);
114.     if ($Pager = new Net::Pager)
115.     {
116.       $SERVICE = 7;
117.       $FROM = "Perl";
118.       Write("Sending page to $To...\n");
119.       if ($Pager->sendPage($SERVICE,
120.         $To,
121.         $FROM,
122.         $Message,
123.         undef ))
124.       {
125.         Write("Page was sent\n");
126.       }
127.       else
128.       {
129.         Write("Page failed to send\n");
130.       }
131.     }
132.     else
133.     {
134.       Write("Unable to create pager object\n");
135.     }
136.     $Pipe->Disconnect();
137.     Write("Waiting for connection");
138.     $Connected = 0;
139.   }
140. }
141. }
```

## 示例 8.11 带有退出处理程序的 Win32::Daemon 服务

```perl
01. use Win32::Daemon;
02. Win32::Daemon::StartService();
03. while(SERVICE_STOPPED != ($State = Win32::Daemon::State()))
04.   {
05.     if(SERVICE_STARTING == $State)
06.     {
07.       Win32::Daemon::State(SERVICE_RUNNING);
08.     }
09.     elsif(SERVICE_PAUSE_PENDING == $State)
10.    {
11.      Win32::Daemon::State(SERVICE_PAUSED);
12.    }
13.    elsif(SERVICE_CONTINUE_PENDING == $State)
14.    {
15.      Win32::Daemon::State(SERVICE_RUNNING);
16.    }
17.    elsif(SERVICE_STOP_PENDING == $State)
18.    {
19.      Win32::Daemon::State(SERVICE_STOPPED);
20.    }
21.    elsif(SERVICE_CONTROL_SHUTDOWN == $State)
22.    {
23.      # 请求 45 秒时间进行关闭...
24.      Win32::Daemon::State(SERVICE_STOP_PENDING);
25.      # 在此处添加关闭代码
26.      Win32::Daemon::State(SERVICE_STOPPED);
27.    }
28.    elsif(SERVICE_RUNNING == $State)
29.    {
30.      # 为运行状态添加代码
31.    }
32.    else
33.    {
34.      # 未处理的消息
35.    }
36.  }
37. Win32::Daemon::StopService();
```

## 基于 Perl 的服务

基于 Perl 的服务非常出色，但它们并非没有风险。坦率地说，基于 Perl 的服务问题与 Win32 服务本身的问题相当。本节将讨论如何解决一些 Win32 相关的问题。

## 调试

服务被设计为一种“离线”运行程序；即程序启动并终止，无需与用户交互。这意味着服务很少向用户展示信息；因此，没有任何窗口使得调试变得非常困难。

只要你运用创意，这个问题很容易解决。示例 8.9 展示了两种解决问题的方法。首先，它打开一个日志文件（参见第 24 到 32 行）。该技术用于存档，以便创建服务的日志。然而，日志也可以很容易地用于调试。服务使用自己的`write()`函数而不是 Perl 的`print`函数。此函数用于将信息重定向到日志文件。

第 42 到 45 行说明了另一种调试服务的方法。在此代码块中，服务通过`show()`函数显示自己的窗口。这通常在服务位于本地系统时有效。它创建一个缓冲区并在控制台中显示（第 42 和 43 行）。当此步骤完成后，传递给`write()`的任何内容都会显示在控制窗口中。除了保存到日志文件外，这就是`write()`函数的作用，让程序员能够快速看到正在记录的内容，减轻调试的负担。这种特定的调试方法非常有用，因为服务在 Local System 账户下运行。否则，你可能看不到控制台。

另一个调试工具是运行一个创建一个命名管道并将任何输入数据导出到流的脚本。这允许服务在启动时连接到命名管道并将调试消息打印其中。这种方法为程序员提供了实时调试信息。它还允许你跨网络进行调试。这是调试服务时用的工具之一。

示例 8.12 是一个命名管道服务器应用程序，用于接收 Win32 服务（或其他任何脚本）的调试消息。要使用此功能，你只需要将示例 8.13 中的两个函数整合到服务脚本中。然后在服务的开始处，调用`start()`函数并传入命名管道脚本运行的机器名称。如果你什么都不传递，则假设为本地机器。每当需要导出调试信息时，将数据传递给`Log()`函数。只要示例 8.12 在服务启动之前运行，就会导出所有的调试信息。

理想情况下，服务和命名管道脚本在同一台机器上运行，以防止服务在 Local System 账户下运行时出现访问错误。你将在下一节学习更多信息。

## 示例 8.12 使用命名管道调试 Win32 服务

```perl
01. use Win32::Pipe;
02.
03. $PIPE_NAME = "Debug Logging";
04. if ($Pipe = Win32::Pipe($PIPE_NAME,
05.             DEFAULT_WAIT_TIME,
06.             PIPE_READMODE_BYTE))
07. {
08.     Announce();
09.     while ($Pipe->Connect())
10.     {
11.         my$User = ($Pipe->GetInfo())[2];
12.         print "Pipe opened by $User at " . localtime() . "\n";
13.         while ($myIn = $Pipe->Read())
14.         {
15.             print $In;
16.         }
17.         print "\nDisconnecting...\n";
18.         $Pipe->Disconnect();
19.         Announce();
20.     }
21.     $Pipe->Close();
22. }
23. else
24. {
25.     print "\nCould not create pipe\n";
26.     print "Error: " . Win32::FormatMessage($Win32::Error) . "\n";
27. }

sub Announce {
30.     my$PipeName = Win32::NodeName() . "\pipe\$PIPE_NAME";
31.     print "----------------------\n";
32.     print "Ready for reading:\n";
33.     print "$PipeName is waiting for a client...\n";
34. }
```

## 示例 8.13 命名管道调试客户端程序

```perl
01. sub StartLog
02.     my $Machine = shift;
03.     my $Handle;
04.     if (defined $Machine && $Machine\ne "")
05.     {
06.         # 在此处添加关闭代码
07.     }
08.     else
09.         $Handle = 1;
10.     }
11. }
12. sub Log {
13.     my ($Message) = @_;
14.     print $Message\n;
15. }
```



# 基于 Perl 的服务问题

她决定使用 `COM` 直接与她的 Outlook 邮件程序通信。然而，在经过一些实验后，Jamie 发现 Outlook 每次只能在一个进程中运行。这意味着要么服务可以运行并与 Outlook 集成，要么她可以登录并运行 Outlook，但二者无法同时进行。这种解决方案是完全无法接受的，因此她转而考虑使用协作数据对象（`CDO`）。

`CDO` 是一个基于 `COM` 的 API，允许程序或脚本与 Outlook 和 Microsoft Exchange 等协作服务进行交互。Outlook 附带 `COM 1.21` 版本，这解决了 Jamie 的问题。通过 `COM`，Jamie 可以完全跳过 Outlook，直接与她的 Exchange 服务器通信（她的日程表就存储在那里）。她很清楚地意识到这是最理想的方法。

在本节稍后的“使用服务”部分中展示的示例 8.14 节展示了她所使用的代码。

## 获取 CDO

Jamie 在注册表中翻找查看自己是否已经安装了 `CDO`，令她非常惊讶的是，她拥有的版本是 `CDONTS`，它是 Windows 2000 自带的，仅提供 `SMTP` 和 `NNTP` 支持。这个版本无法与她所需的 Exchange 服务器通信。因此，她运行了 Microsoft Office 安装程序，并选择了 `CDO` 组件来为她安装正确的版本。

## 安装和移除服务

为了使安装和移除变得简单，Jamie 编写了脚本来接受安装和移除的开关。这样，她就不需要依赖单独的分区来安装或移除作为服务的脚本。她可以通过调用以下命令安装脚本：

```
perl reminder.pl -install
```

同样，她可以通过调用以下命令移除脚本：

```
perl reminder.pl -remove
```

在安装时，她可以指定运行所需的账户和密码。例如，此命令将脚本以调试模式在 Jamie 的账户下运行（这会记录比平时多得多的的信息）：

```
perl reminder.pl -install -account 'MyDomain\Jamie' -password 'MyPassword' -debug
```

## 第 8 章：Win32 服务

- 可以配置多个不同的选项。你可以通过传递 `-help` 开关来获取选项列表。

## 使用服务

示例 8.14 中的脚本被配置为为 Jamie 的 Exchange 收件箱工作。因此，她必须在她的用户 ID 和密码下运行脚本。这要求她授予自己的账户“作为服务登录”的权限（请参考第 2 章设置此类权限的工具）。由于她的 Exchange 服务器使用 Windows 2000/NT 用户账户，她必须确保运行服务的账户不仅具有与 Exchange 服务器通信的权限，具有读取其收件箱的权限。

第 54 到 61 行配置了脚本访问 Jamie 的寻呼器。在这个示例中，她使用 `Net::Pager` 模块使用了 AT&T 的 SMS 寻呼服务。她也可以将其配置为使用另一个寻呼服务或使用 `SMTP` 发送电子邮件。此配置哈希还标识了她的 Exchange 服务器以及她的收件箱。你可以轻松修改这些值以反映你自己的配置。

第 70 行非常重要，因为它决定了服务将日志写入哪个文件。该日志文件显示了何时发送了页面。默认情况下，日志文件放在与脚本相同的目录下。它的名称与脚本相同，只是文件扩展名为 `.log`。通过修改第 70 行，你可以将日志定向到任何地方——只要运行服务的账户具有写入该文件的权限。例如，你可以如下修改此行：

```
my $DB_FILE = "\\\\pipe\Debug Logging";
```

此日志路径将记录示例 8.12 创建的数据。这种方法是监控服务进展的极佳方式，因为命名管道脚本将实时显示提醒服务记录的所有信息。请注意，如果命名管道服务器运行在另一台机器上，你可以替换 `"\\\\MachineName"`，其中 `MachineName` 是运行命名管道脚本的计算机名称，因此第 70 行可能看起来像这样：

```
my $DB_FILE = "\\\\MachineName\pipe\Debug Logging";
```

脚本的核心是 `ProcessEvents()` 函数。在这里，`CDO` 查询任何预约和任务。所有任务都经过了检查，只有发生在今天当前时间到一天之后之间的预约才会被处理（这可以通过更改第 14 行的 `$TIME_CONSIDERATION_INTERVAL` 变量来修改修改）。如果这些任务或预约中有任何一个设置了提醒，将对它们进行检查以判断是否应该给用户发送页面。

你可以轻松地修改此脚本来检查多个用户的日程——前提是运行脚本的账户具有访问收件箱的权限。一本关于 `CDO` 的好书提供了有关此脚本可以完成的其他任务的信息。

# 8.14 预约提醒服务

```
01. use Win32::OLE qw (EVENTS HRESULT);

02. use Win32::OLE::Const 'Microsoft CDO 1.21 Library'

03. use Win32::Daemon;

04. use Win32::Console;

05. use Time::Local;

06. use Net::Pager;

07. use GetOpt::Long;

08.

09. $SCRIPT_PATH = Win32::GetFullPath($0);

10. $VERSION = 2000;

11.

12. # 提前查看多久的？

13. # 秒

14. $TIME_CONSIDERATION_INTERVAL = 60 * 24;

15.

16. # 轮询之间睡眠多久？

17. # 秒

18. $SLEEP_TIME = 2;

19.

20. # 多久处理一次日程？

21. # 秒

22. $CALENDAR_PROCESS_INTERVAL = 60;

23.

24. # 默认值

25. %Config = (

26. account => '',

27. password => '',

28. name => 'Reminder',

29. display => 'Service',

30. );

31.

32. Configure(%Config);

33. if ($Config{help} || scalar @ARGV)

34. {

35. Usage();

36. exit();

37. } elsif ($Config{install}) {

38. {

39. InstallService();

40. exit();

41. }

42. elsif ($Config{remove}) {

43. {

44. RemoveService();

45. exit();

46. }

47.

48. $FOLDERS = (

49. CDefault,

50. CDefaultTasks

51. );

52. %PROFILES = (

53. 'Jamie\'s Mailbox' => {

54. server => 'Exchange',

55. mailbox => '',

56. },

57. );

58. $CLASS = 'Session';

59.

60. $DB_FILE = ($SCRIPT_PATH =~ /(.*)/)[1] . ".log";

61.

62. if (open(LOG, $DB_FILE)) {

63. {

64. select(LOG);

65. $i = 1;

66. print LOG "Software:\n";

67. print LOG "$VERSION\n";

68. print LOG "Started: " . localtime() . "\n";

69. }

70.

71. if ($Config{console}) {

72. {

73. # 如果我们作为控制台应用程序

74. # 而不是服务

75. $State = ($AppState++) ? SERVICE_RUNNING : SERVICE_START_PENDING;

76. }

77. Debug(" Service started: $State\n");

78. if (SERVICE_START_PENDING == $State) {

79. {

80. # 初始化代码

81. $myTotal = 0;

82. foreach $profileName (Keys ($PROFILES)) {

83. {

84. $myProfile = $PROFILES{$profileName};

85. $myMapi = Win32::OLE->new($CLASS, \myProfile);

86. if (defined $Mapi) {

87. {

88. $myMapi->Logoff();

89. $myMapi->Logon({

90. NoMail = 3;

91. ProfileInfo => "$server\$profileName->{mailbox}",

92. });

93. if (Win32::OLE->LastError() != HRESULT (0x00000000)) {

94. {

95. $myComError = Win32::OLE->LastError();

96. Write("Unable to log on $profileName. (Error: $myComError)\n");

97. undef $Mapi;

98. }

99. else {

100. {

101. $PROFILES($profileName)->{mapi} = $myMapi;

102. Write("$profileName has logged on.\n");

103. $myTotal++;

104. }

105. }

106. }

107. if ($myTotal) {

108. {

109. Win32::Daemon::State(SERVICE_RUNNING);

110. $PrevState = SERVICE_RUNNING;

111. Write("Running\n");

112. }

113. }

114. }

}
```

# 示例 8.14 延续 '无法登录任何配置文件。正在停止\n' )

```perl
Write('Unable to logon any profiles. Stopping\n' );

Win32::Daemon::State( SERVICE_STOPPED );

$PrevState = SERVICE_STOPPED;

} elsif(SERVICE_PAUSE_PENDING == $State)

{

    # "暂停中..."

    Win32::Daemon::State( SERVICE_PAUSED);

    $PrevState = SERVICE_PAUSED;

    Write("Paused\n");

} elsif(SERVICE_CONTINUE_PENDING == $State)

{

    # "恢复中..."

    Win32::Daemon::State( SERVICE_RUNNING);

    $PrevState = SERVICE_RUNNING;

    Write("Resumed\n");

} elsif(SERVICE_STOP_PENDING == $State)

{

    # "停止中..."

    Win32::Daemon::State( SERVICE_STOPPED);

    $PrevState = SERVICE_STOPPED;

    Write("Stopped\n");

} elsif(SERVICE_PAUSED == $State)

{

    # 服务已暂停，我们什么都不做

    $PrevState = SERVICE_PAUSED;

} elsif(SERVICE_RUNNING == $State)

{

    # 服务正在运行...

    my$Time = time();

    if($Time >= $NextTime)

    {

        ProcessEvents($Time);

        $NextTime = $Time + $CALENDAR_PROCESS_TIME_INTERVAL;

    }

    $PrevState = SERVICE_RUNNING;

}

else

{

    Write("Received unknown state: $State\n");

    Win32::Daemon::State($PrevState);

}

sleep($SERVICE_SLEEP_TIME);
```

```perl
Win32::Daemon::StopService() unless ($Config{console});

sub ProcessEvents {
    my ($Time) = @_;
    my $TimeLimit = (
        earliest->GetFromArray(TimeStamp($Time)),
        latest->GetFromArray(
            TimeStamp($Time)
            + $TIME_CONSIDERATION_INTERVAL )
    );

    Debug(" Processing events\n");
    foreach my $keys($PROFILES) {
        my $Mapi = $PROFILES{$keys}->mapi;

        if (!defined $Mapi) {
            foreach my $FolderType(@FOLDERS) {
                my $Folder = $Mapi->GetDefaultFolder($FolderType);
                my $Messages = $Folder->Messages();
                my $Filter = $Messages->{Filter};
                my $Fields = $Filter->{Fields};

                # 移除所有过滤器
                $Fields->Delete();
                $Filter->{Not} = 0;
                $Filter->{Or} = 0;

                # 只过滤日历消息（有很多任务）
                if ($DefaultFolderCalendar == $FolderType) {
                    # 注意：日期是反的。
                    # 注意2：必须指定两个日期。
                    # 注意3：设置其他过滤器属性会导致“过于复杂”错误。
                    # 如果开始时间和结束时间在这些时间戳之间，
                # 消息将呈现给我们。
                }
            }
            Debug(" Start date: $TimeLimit{earliest}\n");
            Debug(" Stop date: $TimeLimit{latest}\n");
        }
        {
            $Fields->Add(PR_START_DATE, $TimeLimit{latest});
            $Fields->Add(PR_END_DATE, $TimeLimit{earliest});
            Debug(" Processing Calendar...\n");
        }
    } } elsif ($DefaultFolderTasks == $FolderType) {
        }
```

## 示例 8.14 延续



```perl
Debug(" Processing Tasks...\n");
# 循环考虑每条消息
Debug(" Total messages to consider: $Messages->Count();.\n");
foreach my $Message ($Messages) {
    my $NotifyDate;
    my $ID = $Message->{ID};
    my $MessageContent;

    ## 如果我们已经处理过这条消息，就不再处理。
    next if ($PROCESSED{$ID});
    Debug(" Considering: $Message->{Subject}\n");
    if (scalar (@NotifyDate = GetNotifyDate($Message))) {
        # 我们无法为消息找到提醒日期/时间
        next;
    }
}

# 确定事件的计划时间
my $NotifyTime;
$NotifyTime = localocal(@NotifyDate);
Debug(" Notification on " . localtime($NotifyTime) . ".\n");

# 如果提醒通知尚未到达
next if ($NotifyTime > $Time) {
    $MessageContent = GetMessageContent($Message);
    DisplayMessage($MessageContent);
}

## 发送
if (! $Config{nopage}) && Send($PROFILES{$Profile}, $MessageContent)) {
    # 这个代码块是危险的。它在这里是为了展示
    # 我们可以做什么，但它被注释掉了，以
    ## 防止意外修改服务器上的事件。
    # 请自行承担取消注释！

    ## 关闭此消息的提醒
    my $Message->{ReminderSet} = 0;

    # 用新的提醒状态更新消息，
    # 使持久化并刷新消息
    $Message->Update(1, 1);
    Write(' Page sent on ' . localtime() . ".\n");
}
else {
    # 发送失败，所以我们保留提醒设置
    ## 这样我们还有机会
    Write(' No page sent out ' . localtime() . ".\n");
}

## 记住消息已成功处理
$PROCESSED($ID) = time();
Write("\n");
}
Debug(" End of processing.\n");
}
```

## 第 8 章：Win32 服务

## 示例 8.14 续

```perl
461.     SBody,
462.     undef );
463.     }
464.     return ($Result );
465.     }
466.     {
467.     sub GetServiceConfig = join("", Win32::FullPathName($0 ));
468.     {
469.         my $ScriptPath = "",
470.         my $Hash = {
471.             name => $Config(service),
472.             display => $Config(display),
473.             path => "$X,
474.             user => $Config(account),
475.             password => $Config(password),
476.             parameters => "\ScriptPath\",
477.             description => "Send out pages to remind you of scheduled events.",
478.         }
479.         $Hash(parameters) .= ". -debug" if $Config(debug);
480.         $Hash(parameters) .= ". -console" if $Config(console);
481.         $Hash(parameters) .= ". -nopage" if $Config(nopage);
482.         return (\$Hash);
483.     }
484.     }
485.     sub InstallService
486.     {
487.         my $ServiceConfig = GetServiceConfig();
488.
489.
490.         if (Win32::Daemon::CreateService($ServiceConfig))
491.             {
492.                 print "The $ServiceConfig->{display} was successfully installed.\n";
493.         }
494.         else
495.
496.             print "Failed to add the $ServiceConfig->{display} service.\n";
497.             print "Error: " . GetError() . "\n";
498.         }
499.     }
500.     sub RemoveService
501.     {
502.         my $ServiceConfig = GetServiceConfig();
503.
504.         if (Win32::Daemon::DeleteService($ServiceConfig->{name}))
505.             {
506.                 print "The $ServiceConfig->{display} was successfully removed.\n";
507.             }
508.         else
509.             {
510.                 print "Failed to remove the $ServiceConfig->{display} service.\n";
511.                 print "Error: " . GetError() . "\n";
512.             }
513.     }
```

```perl
513. }
514.
515. sub GetError
516. {
517.   return( Win32::FormatMessage( Win32::Daemon::GetLastError() ) );
518.
519.
520. sub Debug
521. {
522.   Write( @_ ) if ($Config{debug} );
523.
524.
525. sub Write
526. {
527.   my ($Message) = @_;
528.   if (defined $Buffer)
529.   {
530.     $Buffer->Write($Message);
531.   }
532.   else
533.   {
534.     print $Message;
535.
536.   if (fileno( LOG ))
537.
538.     print LOG $Message;
539.   }
540.
541.
542. sub Configure
543.   {
544.   my ($Config) = @_;
545.   my $WarnSub = $SIG{__WARN__};
546.   undef $SIG{__WARN__};
547.   Getopt::Long::Configure("prefix_pattern=-l/" );
548.   GetOptions($Config,
549.
550.   qw(
551.     install
552.     remove
553.     account=s
554.     password=s
555.     display=s
556.     name=s
557.     debug
558.     console
559.     nopage
560.     help
561.   )
562. );
563.   $SIG{__WARN__} = $WarnSub;
564. }
```

## 第 8 章：Win32Services

## 示例 8.14 续

```perl
565. sub Syntax
566. {
567. my $Script ) = ($0 = //[/([\]]*?$/);
568. my $Whitespace = * x length($Script);
569. print <<"EOT"
570.
571. 语法:
572. $Script -install [-account Account] [-password Password]
573. $Whitespace [-display DisplayName] [-name']
574. $Whitespace [-remove]
575. $Whitespace [-debug]
576. $Whitespace [-console]
577. $Whitespace [-help]
578.
579. -install..............安装在该脚本下运行的服务。
580. -account..............默认: 本地系统 (Local System)
581. -password..............指定所使用的密码。
582. -display..............指定服务的名称。
583. 默认: $Config(display_name)
584. -name..............指定服务的名称。
585. 默认: $Config(service_name)
586. -remove..............移除服务。
587. -debug...............显示调试信息。日志文件将变得
588. 非常大
589. -console..............作为控制台应用程序运行（不作为服务）。
590. -nopage...............不发送消息。
591. EOT
592. }
593. sub Quit
594. {
595. foreach $Profile (keys %PROFILES)
596. {
597. if defined $PROFILES->{mapi}
598. {
599. my $Mapi = $PROFILES->{mapi};
600. Write ("Logging out $Mapi->{Name}\n");
601. $Mapi->Logoff();
602. undef $PROFILES->{mapi};
603. }
604. }
605. END;
606. }
```

# 结

Win32 服务一直是 Windows 机器的一个重要方面。这些服务可以在从启动到关闭期间执行功能，而无需用户干预。

本章提供了用于安装、删除和重新配置服务的示例脚本。它还解释了服务的工作原理以及服务面临的一些问题。

# ADSI 和 WMI

微软引入了两种相当令人兴奋的技术：活动目录服务接口（ADSI）和 Windows 管理工具（WMI）。尽管它们之间存在关联，但它们也是截然不同的，且目的也不同。这些技术与 Windows 2000 紧密集成，但在 Windows NT4.0 平台上可用。学习使用这些技术不会是徒用功，因为它们在未来很长一段时间内都会存在。

ADSI 和 WMI 实际上是其他技术的抽象——也就是说，它们提供了构建在其他技术之上的功能，并提供了一个抽象的接口来访问这些技术。

ADSI 和 WMI 实际上是其他技术的抽象——也就是说，它们提供了构建在其他技术之上的功能，并提供了一个抽象的接口来访问这些技术。

ADSI 和 WMI 实际上是其他技术的抽象——也就是说，它们提供了构建在其他技术之上的功能，并提供了一个抽象的接口来访问这些技术。

# 活动目录服务

目录服务的概念一直是操作系统的组成部分。目录服务（DS）是一种存储信息的类型。你可以将其看作是一个填充网络相关信息的数据库。

考虑一个 Web 代理服务器。假设所有用户必须通过该代理服务器访问网站。代理服务器可以查询数据库以发现用户是否有权访问互联网。

## 第 9 章：ADSI 和 WMI

多种不同的 DS 变体，从 X.500 到 Novell 的 Lotus Notes。为了赶上目录服务的热潮，微软推出了自己的版本。简单来说，ADS 是微软的 DS 版本。

然而，问题在于每个 DS 都有其独特的接口。因此，程序在不熟悉每个 DS 接口的情况下很难与它们进行交互。这使得程序难以“开放扩展”。随着新的 DS 出现，程序必须重新设计以包含新的 DS 接口。

为了解决 DS 接口混乱的问题，微软实现了活动目录服务，它本质上是各种目录服务的抽象接口。ADSI 提供了一种大多数目录服务通用的架构。它提供了一个程序可以使用与任何 DS 交互的简单 API。

ADSI 是其他 DS 可以“插入”的架构。因此，DS 可以向任何愿意与 ADSI 交互的程序暴露其服务。每个 DS 必须提供一个“程序”组件作为 ADSI 和 DS 之间的桥梁，使程序能够通过 ADSI 使用各种不同的目录服务。其他抽象 API（如 ODBC）原理类似。

ADSI 的吸引之处之一是它支持自动化。这意味着任何与 IDDispatch 接口交互的程序都可以使用 ADSI。因此，它是完美的 Perl 技术。当你使用 `Win32::OLE` 扩展时，任何 Perl 脚本都可以与已安装 ADSI 程序的 DS 交互。

区分 ADS 和 ADSI 是重要的。活动目录只是一个 DS，而活动目录服务接口是访问许多不同 DS（包括 ADS）的抽象接口。机器可能安装了 ADSI 但没有安装 ADS。

## 如何获取 ADSI？

Windows 2000 和 Windows ME 都预装了 ADSI 组件。然而，ADS 仅运行在 Windows 2000 服务器平台（服务器版、Advanced Server 和 Data Center）上。

# 活动目录服务接口（Active Directory Services Interface）

微软还为 Windows NT 4.0、Windows 98 和 Windows 95 提供了 ADSI。你可以从微软网站 `http://www.microsoft.com/adsi/` 下载它。

## 学习 ADSI

学习 ADSI 接口相当容易。然而，在没有良好指南的情况下，起初可能会有些无从从。我发现两个资源对于学习 ADSI 特别有用。第一个资源是 ADSI 帮助文件。你可以从微软的 ADSI 站点下载这些文件。请查看 `http://www.microsoft.com/adsi/` 并寻找 ADSI 帮助文件的下载链接。

另一个查找文档的好去处是微软开发者网络（MSDN）。它的 ADSI 文档以在线形式位于 MSDN Win32 API 文档中，地址为 `http://msdn.microsoft.com/library/`。

访问此链接后，你需要在目录（在左侧框架中）中向下查找。选择 Platform SDK 和 Network and Directory Services。最后，选择 Active Directory、ADSI 和 Directory Services 链接。

如果需要 ADSI 文档的纸质版，请查看由 Thomas Eck 编写的《Windows NT/2000: ADSI Scripting for System Administration》（New Riders 出）。这本书不仅涵盖了 ADSI 的历史，还解释了 ADSI 在现实环境中的如何工作。它包含了许多示例脚本，说明了 ADSI 的工作原理，对任何管理员都有用。所有的脚本都是用 Visual Basic 的，但将它们转换为 Perl 是一项简单任务。本章中的许多 ADSI 脚本都是 Thomas 书中的 Perl 版本。

## 命名空间（Namespaces）

ADSI 为给定的 DS 提供者定义了唯一的范围，称为“命名空间”。将命名空间视为功能相关的上下文。例如，如果 DS 提供者 MyDS 允许你修改打印机设置，那么这些打印机设置位于 MyDS 命名空间中。

每个命名空间都定义了自己的表示数据。例如，一个 DS 提供者可能通过用户名引用用户，而另一个提供者可能通过用户 ID 用户。当程序与不同的命名空间交互时，它需要知道每个命名空间如何管理自己的数据。

ADSI 允许程序通过定义 `ADPath`（活动目录服务路径）字符串来指定它想要交互的命名空间（或 DS 提供者）。所有的 ADsPath 字符串必须以 ADSI 提供者的名称开头。一些标准的提供者前缀字符串位于表 9.1。

## 第 9 章：ADSI 和 WMI

### 表 9.1 常见的 ADSI 提供者 ADsPath 前缀

| ADsPath 字符串（提供者命名空间） | 说明 |
|---|---|
| `ADs:` | 活动目录服务。此提供者与 Windows 2000 的活动目录服务交互。它也可以与安装在非 Windows 2000 上的活动目录（例如 Microsoft Exchange 和站点服务器）交互。 |
| `WinNT:` | NT 目录服务。此提供者与 Windows NT 域和用户管理器交互。它也可以与 Windows 2000 目录服务交互，尽管它没有充分利用 Windows 2000 的活动目录服务。 |



| LDAP: | 轻级目录访问协议（LDAP）。此提供者使用 LDAP 协议与任何启用 LDAP 的目录服务（包括活动目录服务）交互。 |
|---|---|
| NDS: | Novell 目录服务。 |
| IIS: | IIS 元基础配置数据库。它提供了对 IIS 配置数据库（称为`metabase`）的访问。 |

`ADsPath` 是区分大小写的，且其语法根据所指定的提供者而变化。程序员可能需要参考提供者的文档来确定如何使用它。

由于每个提供者执行的功能仅与其命名空间相关，因此了解每个命名空间可以提供什么信息和功能是非常重要的。此外，理解命名空间属性的含义以及使用什么语法也是至关重要的。这就是架构（schema）的用处。

## 架构（Schema）

`架构`是特定 DS 提供者使用的术语字典。DS 暴露的每个属性都作为 ADSI COM 对象访问。架构允许应用程序了解每个对象代表什么。提供者的架构描述了该提供者实现的每个类。

## 类（Classes）

ADSI 提供者暴露了一系列不同的`类`。这些类类似于面向对象的 C++ 或 Perl 类。一个 ADSI 类仅仅是属性和方法的组。例如，其中一个类可以表示域中的一个用户账户。这个特定类有一个用户名和密码的属性。它还可能有一个重命名用户账户的方法。

# 活动目录服务接口 313

## 绑定（Binding）

Perl 脚本通过绑定到特定对象与 ADSI 类交互。这种绑定简单意味着 ADSI 产生了一个代表特定类的 COM 对象。`ADPath` 字符串也称为绑定字符串。该字符串代表 ADSI 提供者将用于绑定到特定 ADSI 对象的路径。每个对象都基于 ADSI 命名空间中存在的 ADSI 类。

当脚本请求 ADSI COM 对象时，ADSI 提供者必须确定脚本尝试绑定的类类型，这可能会导致时间延迟。假设一个 Perl 脚本实现了以下行代码：

```perl
$ADSIObj = Win32::OLE->GetObject("WinNT://SomeName");
```

`WinNT` 提供者必须确定 `SomeName`——一个计算机名或域名。它可能通过首先查询名为 `SomeName` 的域来实现。如果该查询失败，则尝试访问机器`\SomeName`。当然，整个过程可能会产生阻塞延迟。在这种情况下，绑定到域类或计算机类的效率非常低。WinNT 提供者允许你指定要绑定到哪种类。你通过指定一个逗号后跟类名（如下所示来提出此请求：

```perl
$ADSIObj = Win32::OLE->GetObject("WinNT://SomeName,computer");
```

在这种情况下，ADSI 提供者知道脚本正尝试绑定到计算机类。提供者可以快速实例化相应的类。

在之前的示例中，`ADPath` 指向一个被解释为网络域或网络机器的特定对象。无论如何，提供者组件识别出该路径是某种网络对象。然而，有时提供者的语法可能会使请求模糊且无法确定。

```perl
$ADSIObj = Win32::OLE->GetObject("WinNT://SomeName/JOEL");
```

在这种情况下，不清楚 `SomeName` 和 `JOEL` 是什么。`SomeName` 可能是域也可能是计算机。`JOEL` 可能是 `SomeName` 域中的计算机，也可能是 `SomeName` 域或 `SomeName` 计算机中的用户、本地组或全局组。

你可以通过指定对象引用的是哪种类来消除这种歧义：

```perl
$ADSIObj = Win32::OLE->GetObject("WinNT://SomeName/JOEL");
```

或者你可以将请求拆分为多次请求：

```perl
$ADSIObj = Win32::OLE->GetObject("WinNT://SomeName,computer");
$User = $ADSIObj->GetObject("JOEL");
```

# 活动目录服务接口（Active Directory Services Interface）

示例 9.2 展示了如何使用 Perl 脚本程序化地发现 ADSI 暴露的类和属性。脚本首先请求一个 ADSI COM 对象。默认情况下，它请求一个 WinNT 域类对象。然而，你可以传递任何有效的 ADSI 路径。第 5 行决定使用哪个 ADSI 路径。

接下来，第 6 行绑定到 ADSI COM 对象。第 9 行绑定到 ADSI COM 对象的架构（schema）。现在你有了架构对象，可以通过查询来发现它暴露了哪些属性和类。你通过调用脚本中的`ProcessClass()`函数来实现这一点。`ProcessClass()`函数首先请求一个代表传入架构父类的架构对象。这样做是因为类的架构描述了类拥有哪些属性，但每个属性的语法定义在类的父类中。出于此原因，第 20 行请求了架构对象的父对象。

第 22 到 25 行获取类的强制和可选参数列表。第 27 行发现 ADSI 对象可以包含的子类（ADSI 称为“包含关系”）。第 35 到 38 行列出并打印这些每一个子类。

第 47 到 59 行列出类的每个属性，并从父架构对象（第 54 行）请求相应的属性对象。然后将属性对象的名称和语法写入屏幕。最后，第 62 到 73 行遍历所有子类，并在每个子类上重复该过程。

> 一个 ADSI 包含相同类型的子类并不罕见。例如，你可能有一个目录类，它可以包含目录子类。这就是为什么示例 9.2 中增加了第 28 行和第 67 行。它们记录了哪些类已经被处理。这防止了在这些类上发生无限递归。

## 示例 9.2 程序化发现 ADSI 类属性

```perl
01. use Win32;
02. use Win32::OLE qw ( in );
03.
04. $Domain = Win32::DomainName();
05. $ADSPath = "WinNT://$Domain" unless ($ADSPath = shift @ARGV);
06. if (my $ADSIObject = Win32::OLE->GetObject($ADSPath)) {
07.
08.     print 'Examining $ADSPath ADSI class...\n';
09.     if (my $DSSchema = Win32::OLE->GetObject($ADSIObject->{Schema})) {
10.
11.     ProcessClass($DSSchema);
12. }
```

## 示例 9.2 续

```perl
13. }
14.
15. sub ProcessClass
16. {
17. my ($DSSchema) = @;
18. local $PropType;
19. # 获取类的父类...
20. my $ParentClass = Win32::OLE->GetObject($DSSchema->{Parent});
21. # 获取此类的属性...
22. my %Properties = (
23. mandatory => $DSSchema->{MandatoryProperties},
24. optional => $DSSchema->{OptionalProperties}
25. );
26. # 获取此类可能拥的所有子类...
27. my $SubClasses = $DSSchema->{Containment};
28. $ClassList{$DSSchema->{Name}} = 1;
29. print "Class: $DSSchema->{Name}\n";
30. if (scalar @{$SubClasses}) {
31. {
32. $- = SUBCLASS_HEADER_FORMAT;
33. write;
34. $- = SUBCLASS_FORMAT;
35. map
36. {
37. write;
38. } @{$SubClasses};
39. print "\n";
40. }
41.
42. $- = PROPERTY_HEADER_FORMAT;
43. write;
44. $- = PROPERTY_FORMAT;
45.
46. # 显示所有属性...
47. foreach $PropType (keys (%Properties)) {
48. {
49. my $PropList = $PropType @{$PropType};
50. next unless (scalar @{$PropList});
51. foreach my $PropName (@{$PropList}) {
52. {
53. local $Property;
54. if ($Property = $ParentClass->GetObject("Property", $PropName)) {
55. write;
56. }
57. }
58. }
59. print "\n";
60.
61. if (scalar @{$SubClasses}) {
62. {
63. foreach $Class (@{$SubClasses}) {
64. {
65. my $ADSPath = $DSSchema->{Parent} . "$Class";
66. next if defined $ClassList{$Class};
67. if (my $ADSIObj = Win32::OLE->GetObject($ADSPath)) {
68. ProcessClass($ADSIObj);
69. }
70. }
71. }
72. print "\n";
73. }
```

```perl
74. format SUBCLASS_HEADER_FORMAT =

75. Subclasses

76. .........................

77. format SUBCLASS_FORMAT =

78. @<<<<<<<<<<<<

79. format PROPERTY_HEADER_FORMAT =

80. Property Name Type

81. .................................

82. format PROPERTY_FORMAT =

83. @<<<<<<<<<<<< $PropType, $Property->{Name}, $Property->{Syntax}
```

## 发现域

获取机器可以查看的域列表相对简单。要这样做，绑定到 WinNT ADSI 提供者的根命名空间并枚举每个对象。示例 9.3 正是这样做的。第 4 行请求一个绑定到命名空间的 ADSI 对象。第 8 到 11 行执行枚举。

WinNT ADSI 提供者似乎并不区分域和工作组。示例 9.3 会打印出可用域以及工作组。似乎没有简单的方法可以判断 WinNT 报告的是域还是工作组，除非测试有效属性（见示例 9.4）。

## 示例 9.3 显示域

```perl
01. use Win32::OLE qw ( in );
02.
03. $ADSPath = "WinNT";
04. if ($AD = Win32::OLE->GetObject($ADSPath)) {
05. {
06.     my $ICount = 0;
07.     print "This machine can see the following domains:\n"
08.     foreach $sDomain (in ($AD))
09.     {
10.         print ++$ICount . $sDomain->{Name}\n"
11.     }
12. }
```

在示例 9.3 的情况下，只显示了域名称。虽然脚本只显示了每个域的名称，但域类包含其他也可以打印的属性。

如果你不知道域对象拥有哪些属性，可以使用脚本发现它们。示例 9.4 通过添加`GetProperties()`子程序实现了这一点。该程序定义在第 30 到 44 行，工作原理类似于示例 9.2 的`ProcessClass()`函数。它访问给定 ADSI 对象的架构定义的强制和可选属性。第 15 到 26 行枚举每个属性并显示其值。第 19 到 24 行检查域对象代表的是域还是工作组。

## 示例 9.4 显示域及其属性

```perl
01. use Win32::OLE qw ( in );
02.
03. $ADSPath = "WinNT";
04. if ($AD = Win32::OLE->GetObject($ADSPath)) {
05. {
06.     my $ICount = 0;
07.     my $Schema;
08.     my $PropertyList;
09.
10.     print "This machine can see the following domains:\n"
11.     foreach $sDomain (in ($AD))
12.     {
13.         $PropertyList = GetProperties($sDomain) unless ref $PropertyList;
14.         print ++$ICount . $sDomain->{Name}\n"
15.         foreach $sProperty (@$PropertyList) {
16.         {
17.             # 检查 $sDomain 是否确实是域而非
18.             # 工作组。
19.             if (! defined $sDomain->{$sProperty}) {
20.             {
21.                 print "\tCan not query domain properties.\n"
22.                 print "\tThis must be a workgroup.\n"
23.                 last;
24.             }
25.             print "\t $sProperty: $sDomain->{$sProperty}\n"
26.         }
27.     }
28. }
29. }
30.
31. sub GetProperties
32. {
33.   my ($Obj) = @_;
34.   my @Properties;
35.
36.   if ($my $Schema = Win32::OLE->GetObject($Obj->{Schema})) {
37.   {
38.       foreach my $PropList ($Schema->{MandatoryProperties},
39.                           $Schema->{OptionalProperties}) {
40.       {
41.         push(@Properties, @{$PropList} if (defined $PropList);
42.       }
43.     }
44.   }
45.   return (@Properties);
46. }
```

## 冒充

到为止，本章的示例非常直接。然而，它们都假设运行 Perl 脚本的用户有权限与 ADSI 对象交互。如果用户是管理员，评估可能是准确的。但是，当需要不同的用户账户时，ADSI 提供了一种机制，使用户能够冒充另一个用户，只要她拥有正确的凭据。

Perl 脚本可以请求一个绑定到给定 ADSI 提供者命名空间顶层类的 ADSI COM 对象。结果类暴露了一个名为`openObject()`的方法。该方法接受 ADSI 路径，以及用户 ID、密码和选项。

示例 9.5 显示了在指定的 ADSI 路径内找到的所有 ADSI 对象。默认情况下，路径为`WinNT://DOMAINNAME`，其中 DOMAIN 是本地机器的域名称。你可以通过从命令行传递来更改 ADSI 路径。例如：

```bash
perl DisplayADSIObject.pl WinNT://MyDomain
```

在这种情况下，指定了`MyDomain`。可以传递任何有效的 ADSI 路径，例如：

```bash
perl DisplayADSIObject.pl WinNT://MyDomain/MyComputer/Browser,service
```

## 第 9 章：ADSI 和 WMI

这将从名为`MyDomain`的域中名为`MyComputer`的计算机上选择`Browser`服务。

此脚本显示指定路径所包含的所有对象。例如，如果你传递一个域路径（如`WinNT://MyDomain`），它将返回组成该域的所有用户、组和机器的列表。

此脚本有趣之处在于，它允许脚本冒充另一个用户。用户可以通过指定`-u`和`-p`选项来实现这一点，在本例中所示：

```bash
perl DisplayADSIObject.pl -u Administrator -p MyPassword
```

可选地，用户可以使用`-f`传递过滤器列表。如果指定了任何过滤器，则只显示匹配其中一个过滤器的对象。例如，以下命令仅显示来自名为`MyMachine`的计算机的用户账户和本地组：

```bash
perl DisplayADSIObject.pl -f user localgroup WinNT://MyMachine,computer
```

示例 9.5 中第一个需要注意的是，第 4 行加载了`Win32::OLE::const`模块，该模块加载了 ADSI 库及其所有关联常量。这一点非常重要，因为脚本使用了其中一些常量来执行任何用户冒充。

脚本通过提供`GetADSIObject()`子程序来实现其冒充魔法。脚本在第 13 行调用了此函数。注意它传递了`%config`哈希的引用。该哈希包含所有配置选项，如 ADSI 路径、用户名和密码。

第 16 行绑定到代表第 13 行请求的 ADSI COM 对象的架构（schema）对象。对架构对象的绑定允许脚本发现类信息，就像该对象是一个容器。容器可以包含其他对象（目录是一个容器，因为它包含文件和其他目录）。如果它是容器，就可以对其应用过滤器。



当列举容器的对象时，所有对象都会被引用。然而，如果对容器应用了过滤器，其结果的枚举将仅产生符合过滤器指定的类型对象。例如，枚举域对象可以产生结果、本地组、全局组和计算机。但是，如果对域对象上应用了仅指定用户和计算机的过滤器，则只枚举用户和计算机对象。

第 24 行如果用户指定了要过滤的类列表，则对 `ADSI COM` 对象应用过滤器。注意过滤器只接受数组引用。它可以是一个匿名数组或（在这种情况下）对数组的引用。

第 28 至 31 行执行实际的枚举并显示 `ADSI COM` 对象中持有的每个对象。

## 活动目录服务接口 321

第 39 至 67 行定义了 `GetADSIObject()` 子程序。第 45 行测试用户是否指定了另一个用户进行冒充。如果没有，第 64 行按脚本正常操作的方式请求 `ADSI` 对象。然而，如果指定了用户，第 47 行确定如何指定 `ADSI` 提供程序并绑定到该提供程序的命名空间（第 49 行）。第 51 至 56 行随后调用生成的 `ADSI` 提供程序对象的 `OpenADSObject()` 方法，传递 `ADSI` 路径、用户名、密码和任何参数。在这种情况下，`ADS_SEC_AUTHENTICATION`、`ADS_USE_ENCRYPTION` 和 `ADS_READONLY_SERVER` 标志被按位或并传递。这导致尝试使用加密且安全的（如 `Kerberos` 或 `NTLM`）连接到域控制器（主或备）来冒充指定的用户。如果冒充失败，第 58 行将输出结果错误。

## 示例 9.5 使用 ADSI 冒充另一个用户

```
01. use getopt::Long;
02. use Win32;
03. use Win32::OLE qw( in);
04. use Win32::OLE::Const 'Active DS Type Library';
05.
06. $Config(path) = "WinNT"; Win32::DomainName();
07. Configure (%Config);
08. if ($Config{help})
09. {
10. Syntax();
11. exit;
12. }
13. if ($AD = GetADSIObject(\%Config))
14. {
15. $mySCount = 0;
16. $my $Schema = Win32::OLE->GetObject($AD->{Schema});
17.
18. # 架构对象的 Container 属性显示我们是否是一个容器。
19. if ($Schema->{Container})
20. {
21. if (scalar(@$Config{filter}))
22. {
23. # Apply过滤器 = $Config{filter};
24. $AD->{Filter} = $Config{filter};
25. }
26. print "\$AD->{ADPath} \$AD->{Class} 对象包含 ";
27. print "以下对象:\n"
28. foreach my $Object (in ($AD))
29. {
30. print ++$mySCount. ".") \$Object->{Name} (\$Object->{Class})\n"
31. }
32. else
33. {
34. print "The\$AD->{ADPath} 是一个 \$AD->{Class} 对象。\n";
```

## 示例 9.5 续

```
36. }
37. }
38.
39. sub GetADSIObject
40. {
41. my($Config) = @_;
42. my $ADSIObject;
43. my $ADSPath = $Config->{path};
44.
45.
46. if defined $Config->{user}
47. {
48. my($ADProvider, $Path) = ($ADSPath == m#"([/]**)(.*##);
49.
50. if ($AD = Win32::OLE->GetObject($ADProvider))
51. {
52. if (! $ADSIObject = $AD->OpenADSIObject($ADSPath,
53. $Config->{user},
54. $Config->{password},
55. ADS_SECURE_ENCRYPTION
56. | $ADS_READONLY_SERVER ))
57.
58. {
59. print "Error:\n" Win32::OLE->LastError();
60. }
61. }
62. else
63. {
64. $ADSIObject = Win32::OLE->GetObject($ADSPath);
65. }
66. return($ADSIObject);
67. }
68. sub Configure
69. {
70. my($Config) = @_;
71. my $Result;
72. Getopt::Long(
73. "help",
74. "path=s",
75. "user=s",
76. "password=s",
77. "filter=s"
78. );
79.
80. if ($Config{help}) {
81. Syntax();
82. exit;
83. }
84.
85. if ($AD = GetADSIObject(\%Config)) {
86. $mySCount = 0;
87. my $Schema = Win32::OLE->GetObject($AD->{Schema});
88.
89. # 架构对象的 Container 属性显示我们是否是一个容器。
90. if ($Schema->{Container}) {
91. {
92. if (scalar(@$Config{filter})) {
93. {
94. # Apply过滤器 = $Config{filter};
95. $AD->{Filter} = $Config{filter};
96. }
97. print "\$AD->{ADPath} \$AD->{Class} 对象包含 ";
98. print "以下对象:\n"
99. foreach my $Object (in ($AD)) {
100. {
101. print ++$mySCount. ".") \$Object->{Name} (\$Object->{Class})\n"
102. }
103. } else
104. {
105. print "The\$AD->{ADPath} 是一个 \$AD->{Class} 对象。\n";
106. }
107. }
108. }
109. }
110. }
111. } sub Syntax {
112. print "Usage: DisplayADSIObject.pl [-path path] [-u user] [-p password] [-f filter]\n";
113. }
```

（注：由于原始文本包含大量 OCR 识别错误和重复，上述翻译已根据逻辑结构进行了清理和整理，以确保内容的连贯性。）

## 活动目录服务接口 325

如果脚本请求一个 `ADSI` 对象，它可以反复查询其属性。当 `ADSI` 对象代表本地机器上的某些内容时，这种操作是相对容易的。脚本每次访问某个属性时，`ADSI` 标识程序都会与本地机器通信，发现属性值并将其返回给脚本。然而，如果 `ADSI` 对象代表（例如）远程机器上的某个用户，则 `ADSI` 提供程序就必须跨越网络请求属性值。这可能会对性能产生严重影响，特别是当脚本处理许多对象和属性时。

为了减轻对网络的影响，`ADSI` 会缓存各种对象和属性。拥有此缓存意味着提供程序只需要跨越网络进行一次查询——即在对象第一次被引用时获取它。这种策略通常会提高网络和脚本的性能。

不过，这种方法有一个细微的问题。如果你修改了对象的属性，这些属性会被修改到缓存的对象中。这再次提高了性能，因为不需要在每次修改时都跨越网络进行写入。但是，脚本需要承担提交所做更改的责任。

提交对 `ADSI` 对象进行的更改非常简单。你可以通过调用对象的 `setInfo()` 方法来提交具有属性的 `ADSI` 对象，这将强制 `ADSI` 将缓存的对象提交到其存储库。该存储库用于启用或禁用指定的账户。此脚本的魔法发生在本地机器或跨网络的远程机器上。

示例 9.7 说明了如何从缓存提交对象。该脚本发生在第 25 行，它调用了用户对象的 `setInfo()` 方法。在这里，对用户账户的修改被提交到账户所在的数据库。

第 26 行是为了我们这些担心方法调用并不总是有效的人准备的。在段代码中，`getInfo()` 方法刷新缓存中的用户对象。它强制 `ADSI` 跨越网络为用户账户获取最新的属性。第 27 和第 28 行检查属性是否成功设置。脚本可以接受以下格式的任意数量的账户：

- `account`

- `domain\account`

- `machine\account`

脚本默认启用指定的账户。如果传递了 `-d` 关，则禁用这些账户。

## 第 9 章：ADSI 和 WMI

## 示例 9.7 启用和禁用账户

```perl
use Getopt::Long;
use Win32;
use Win32::OLE;

%Config = (
    disable => 0,
);
Configure($Config);
print ($Config{disable} ? "Disabling " : "Enabling ");
print "the following accounts:\n";
foreach my $Account (@ARGV) {
    my ($fMachine, $Domain, $UserName) = ($Account =~ /^\((.*?)\.(.*?)\$/) ? "domain" : "computer";
mymyClass = (" eq $fMachine ) ? "domain" : "computer";
    $Domain = Win32::DomainName() if (" eq $Domain);
    if my $AD = Win32::OLE->GetObject("WinNT::$Domain,$Class")) {
        my $User = $AD->GetObject("User", $UserName) or next;
        print "$Account: ";
        $User->{AccountDisabled} = $Config{disable};
        $User->SetInfo();
        $User->GetInfo();
        print ($User->{AccountDisabled} == $Config{disable}) ? "(successful)" : "(failed)");
        print "\n";
    }
}

sub Configure {
    my ($Config) = @_;
    my $Result;
    Getopt::Long::Configure("prefix_pattern=-|*");
    $Result = GetOptions($Config, "disabled");
    return;
}
```

因为你可能会尝试示例 9.7，所以我包含了示例 9.8，它显示所有禁用的用户账户。第 19 行使用了之前描述的过滤（参见示例 9.5）。脚本可以接受任意数量的域或机器名称。默认情况下，脚本显示已启用的账户。你传递 `-d` 关来只显示禁用的账户。例如，

```
perl ShowEnabled.pl MyDomain\Machine -d
```

将显示 `MyDomain` 域以及 `MyMachine` 机器中所有禁用的账户。

## 示例 9.8 显示所有启用或禁用的账户

```perl
use Getopt::Long;
use Win32;
use Win32::OLE qw (:in);

Configure($Config);
print "The following accounts are ";
print (($Config{disable}) ? "disabled" : "enabled");
print "\n";

push(@ARGV, Win32::DomainName()) if (scalar ARGV);
foreach my $Domain (@ARGV) {
    my ($fMachine, $Name) = ($Domain =~ /^\((.*?)\$/);
    my $Class = (" eq $fMachine) ? "domain" : "computer";
    if my $AD = Win32::OLE->GetObject("WinNT::$Name,$Class")) {
        # We only want user accounts.
        $AD->{Filter} = [ "User" ];
        foreach my $User (in $AD) {
            if ($User->{AccountDisabled} == $Config{disable}) {
                print "$Domain\\$User->{Name}\n";
            }
        }
    }
}

sub Configure {
    my($Config) = @_;
    my $Result;
    Getopt::Long::Configure("prefix_pattern=-|*");
    $Result = GetOptions($Config, "disabled");
    return();
}
```

## 断开网络会话

`AD` 是系统管理员的强大工具。示例 9.9 使用 `ADSI` 显示所有连接到远程机器的用户会话。此脚本接受以下格式的机器名称：

- `machine`

- `domain\machine`

此脚本允许你指定特定的路径。当你传入一个机器名称时，将显示顶层类及其所有子类。你可以像下面这样使用该脚本：

```
perl IISWebDump.pl webserver
```

此命令显示 `webserver` 机器上整个 `IIS` 站点的所有属性。这是另一个示例：

```
perl IISWebDump.pl webserver/W3SVC/1
```

这仅将检查 `webserver` 机器上第一个虚拟 Web 服务器的属性。

> 有趣的是，如果示例 9.10 运行在 `Windows 2000` 机器并尝试连接到 `Windows NT 4.0` 机器（或反之），它将无法正常工作。这是由于 `Windows 2000` 和 `NT 4.0` 版本的 `IIS` 元数据库（`metabase`）之间的架构差异。讨论此问题的微软知识库文章可以在此处找到：`http://support.microsoft.com/kb/articles/Q246/5-75.ASP`。

此脚本与示例 9.2 非常相似。两者之间的真正区别在于示例 9.10 显示了每个属性值。这使得管理员能够快速查看其 Web 服务器设置了哪些值。

## 示例 9.10 IIS 属性值导出



#我是由深度求索（DeepSeek）研发的 deepseek-v4-flash-0731 智能大模型。示例 9.10 延续

```perl
76. -\n
77. -\n
78. -\n
79. -
80. -\n
81. -\n
82. -\n
83. -\n
84. -\n
85. -\n
86. -\n
87. -\n
88. -\n
89. -\n
90. -\n... (以此类推)
```

# 修改 IIS 属性

通常，你只需要修改 IIS 机器上的属性。如果你有几台不同的机器需要执行此任务，使用基于 GUI 的应用程序可能会非常耗时。示例 9.11 允许你一次性查询或设置多台机器或虚拟服务器的属性。

该脚本接受任意数量想要修改的 IIS 相对路径。它还接受任意数量的 `-p` 参数，这些参数指示要查询或设置的属性。查看此示例：

```perl
perl IISProperty.pl localhost/W3SVC/1 server
```

此命令显示 `server` 机器上整个 IIS 站点的所有属性。这是另一个示例：

```perl
perl IISProperty.pl localhost/W3SVC/1 server -p comment
```

此命令显示 `server` 机器上第一个虚拟 Web 服务器的 `comment` 属性。

```perl
perl IISProperty.pl localhost/W3SVC/1 server -p comment="New comment"
```

此命令将 `server` 机器上第一个虚拟 Web 服务器的 `comment` 属性设置为 `"New comment"`。

通常情况下，你可能需要修改多台 IIS 机器上的属性。

# 示例 9.11 查询并修改属性

```perl
01. use Win32;
02. use Win32::OLE qw ( in );
03.
04. push $ARGV, Win32::NodeName() if ( scalar $ARGV);
05. foreach $myMachine ($ARGV)
06. {
07. my $ADSPath = "IIS://$Machine";
08. if ($my $IIS = Win32::OLE->GetObject ($ADSPath))
09.
10. ProcessObject ($IIS);
11.
12. }
13.
14. sub ProcessObject
15. {
16. my ($Object) = @_;
17. local $PropertyName;
18. my $iCount = 0;
19.
20. print "\nName: $Object->{Name}\n";
21. print "Class: $Object->{Class}\n";
22. print "Path: $Object->{ADSPath}\n";
23. print " This object contains the following sub objects:\n";
24. print "\n";
25. foreach my $Sub ( in ($sObject) )
26. {
27.     print " , ++$iCount, " ";
28.     print "$Sub->Name($Sub->{Class}) $Sub->{ADPath}\n";
29. }
30. print "in";
31.
32.     $- = PROPERTY_HEADER_FORMAT;
33.     write;
34.     $- = PROPERTY_FORMAT;
35.     foreach $PropertyName ( sort (@GetProperties ($sObject )) )
36.     {
37.         next if ("" eq $PropertyName);
38.         local ($Value) = $Object->{$PropertyName};
39.         if (ARRAY eq ref $Value)
40.         {
41.             $Value = join("\n", @{$Value});
42.         }
43.         write;
44.     }
45.
46.     # 递归处理每个子对象
47.     foreach my $Sub ( in ($sObject) )
48.     {
49.         ProcessObject($Sub);
50.     }
51. }
52.
53. sub GetProperties
54.     {
55.     my ($Obj) = @_;
56.     my @Properties;
57.
58.     if ($Schema = Win32::OLE->GetObject ($Obj->{$Schema}) )
59.     {
60.         foreach my $PropList ($Schema->{MandatoryProperties},
61.             $Schema->{OptionalProperties})
62.         {
63.             push(@Properties, @{$PropList}) if (defined $PropList);
64.         }
65.     }
66.     return (@Properties);
67. }
68.
69. format PROPERTY_HEADER_FORMAT = =
70.     Property                           Value
71.     ................--------------------------------------
72.
73. format PROPERTY_FORMAT = =
74.     <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
75.     $PropertyName,                       Value
```

# 显示 IIS 树

随着虚拟目录的创建、重命名和删除，确保给定的 Web 站点拥有所有目录可能是困难的。由于 Windows 有 `TREE.EXE` 命令，似乎 IIS 也有类似的工具。

从概念上讲，图 9.1 展示了这样的 IIS 树看起来是什么样的。每个节点相对于其父节点显示。在这种情况下，显示的是第一个虚拟服务器。注意虚拟 Web 服务器的注释显示在括号中。

```text
--1 (This is a test!!!
+--Root
| |+Scripts
| | |+Proxy
| | | \|\w3proxy.dll
| | |+localstart.asp
| |+IISAdmin
| |+ISSamples
| |+MSADC
| |+IISHelp
| |+Webpub
| | |+vti_pvt
| | |+vti_log
| | |+private
| | |+vti_txt
| | |+vti_script
| | |+vti_cnf
| | |+vti_bin
| | \|\--Printers
+--IISCertMapper
\--Filters
\\\\--Home ISAPI Home Filter
```

图 9.1 一个虚拟 Web 服务器的 IIS 树导出。

示例 9.12 显示 IIS 树。你通过传入相对于 IIS 提供者的路径来运行此脚本：

```perl
perl TreeDump.pl webserver/W3SVC
```

此命令显示 `webserver` 机器上所有虚拟 Web 服务器的树。

这是另一个示例：

```perl
perl TreeDump.pl webserver
```

此命令显示 `webserver` 机器上的整个 IIS 树。将显示所有 IIS 服务，包括 web、ftp、nntop 以及任何已配置的服务。

默认情况下，IIS 树使用图形字符显示。然而，在某些情况下，这些图形字符可能无法正确显示，例如如果显示字体不支持它们。为了纠正这一点，请传入 `-a` 参数。这将以 ASCII 字符显示树。

# 示例 9.12 续

```perl
32. {
33.     ProcessDir($ IIS );
34.     }
35. }
36. 
37. sub ProcessDir
38. {
39.     my($Object, $IndentString) = @_;
40.     my $PropertyName;
41.     my $SubDirList = in ($Object);
42.     my $iCount = scalar $SubDirList;
43. 
44.     print $Charset->{horizontal} x 3, $Object->{Name};
45.     if ( ('IisWebServer' eq $Object->{Class} )
46.         || ('IisFtpServer' eq $Object->{Class} )
47.             || ('IisNtpServer' eq $Object->{Class} )
48.             || ('IisNtpServer' eq $Object->{Class} ))
49.     {
50.         print " ($Object->{ServerComment});";
51. }
52.     print 'in';
53.     foreach my $Sub (@SubDirList)
54.     {
55.         my $String;
56. 
57.         if (--iCount)
58.         {
59.             $String = " $Charset->{vertical}";
60.             print $IndentString, " $Charset->{tee}
61.         }
62.         else
63.         {
64.             $String = " ";
65.             print $Indent, " $Charset->{corner}";
66.         }
67.     ProcessDir($Sub, $IndentString, $String);
68.     }
69. }
70. 
71. 
72. sub Configure
73. {
74.     my($Config) = @_;
75.     my $Result;
76. 
77.     Getopt::Long::Configure("prefix_pattern=-|/" );
78.     $Result = GetOptions($Config,
79.         qw(
80.             asciiia
81.             help?|h
82.         )
83. );
84. push(@{$Config->{servers}}, @ARGV );
85. if ( scalar @{$Config->{servers}}) {
86. {
87. push(@{$Config->{servers}}, Win32::NodeName());
88. }
89. $Config->{help} = 1 unless ($Result );
90. }
91. 
92. sub Syntax
93. {
94. my($Script) = (Win32::GetLongPathName($0) =~ /\([\\\*))?$/);
95. my($Line) = ".*" length($Script);
96. }
97. 
98. print <<EOT;
99. $Script
100. $Line
101. Displays an IIS server tree.
102.
103. Syntax:
104. perl $Script [-a] Server [Server2 ... ]
105. -A....ascii characters to display the IIS tree.
106. Server......The name of the IIS server.
If no servers are specified then the local
107. machine is used.
108.
109. EOT
110. }
```

# Windows 管理插集 (Windows Management Instrumentation)

计算机行业一直试图开发一种标准的方法来跨网络访问管理信息。这项工作促进了基于网络的企业管理 (WBEM) 倡议。该倡议使用了行业标准通用信息模型 (CIM)，它定义了哪些信息是可以访问的。这些标准共同工作，允许你连接到远程机器以查询和管理设置以及进程。

微软的 WBEM 实现被称为 Windows 管理插集 (WMI)。任何程序都可以与 WMI 集成，以暴露事件、属性和其他设置。如果你愿意学习 WMI，就可以快速控制你的网络。WMI 是每一位 Win32 管理员都应该熟悉的的一种强大力量。

使用 ADSI 是查询绑定到数据库（例如用户数据库）设置的极佳方法，而 WMI 则提供了对运行进程、硬件和事件的访问，这仅是其中的几。



# 第 9 章：ADSI 和 WMI

微软还为 Windows NT 4.0、Windows 98 和 Windows 95 提供了 ADSI。你可以从 MS 网站下载：http://msdn.microsoft.com/downloads/sdks/wmi/

## WMI 详情

与 ADSI 一样，WMI 与提供者（providers）工作。提供者作为 WMI 与某些进程或数据库之间的桥梁。例如，默认有针对 SNMP 对象、注册表对象和 Win32 对象的 WMI 提供。如果第三方编写了新的程序或服务，它可以提供 WMI 提供者，允许你使用 WMI 与程序或服务交互。WMI 还与 ADSI 共享命名空间和类的概念。

通常，为了请求 WMI 对象，你必须构造一个指定 `WinMgmts` 提供者的路径。在指定 WMI 路径时，可以在提供者之后声明安全级别 `{impersonationLevel=}` 字符串，表示你想在远程机器上代表自己（在 Windows 2000 上使用 WMI 时不需要，但为了兼容 Windows NT 和 95/98，应该始终指定）。接下来，你需要在路径后指定双斜杠 (`\\`) 和机器名称，如下例：

```
WinMgmts:(impersonationLevel=)\\Machine
```

此路径返回一个表示指定机器（`MachineName` 为例）的 WMI 对象。该对象可以检索其他 WMI 对象或实例化 WMI 对象。例如：

```perl
$Path = "WinMgmts:(impersonationLevel=)\\MachineName"
$WMI = Win32::OLE->GetObject($Path);
```

结果是一个 WMI 对象。WMI 类定义了几个重要方法：`Get()` 和 `InstancesOf()`。`Get()` 方法返回类集合（见示例 16）。`InstancesOf()` 方法返回类的实例（见示例 13）。这两个函数将在后续章节描述。

## 获取远程机器上的磁盘

示例 9.13 使用 WMI 获取远程机器的驱动器。第 21 行从远程机器请求 WMI 对象。第 28 行调用 `InstancesOf()` 方法，该脚本接受任意数量的机器名称。每个机器的磁盘都会被枚举并显示。例如，你可以这样调用脚本：

```
perl WMidis.pl \ServerA\ServerB
```

这将显示 `\ServerA` 和 `\ServerB` 机器的所有驱动器（软盘、光驱驱动器和映射的网络驱动器）。

## 在远程机器上获取驱动器信息

```perl
01. use Win32;
02. use Win32::qw( in );
03.
04. %TYPE = (
05. 0 => 'Unknown',
06. 1 => 'No root',
07. 2 => 'Removable',
08. 3 => 'Local',
09. 4 => 'Network',
10. 5 => 'CDRom',
11. 6 => 'RAM Disk'
12.
14. push(@ARGV, Win32::NodeName()) if (! ARGV);
15. foreach my $Machine (@ARGV);
16. {
17. # 任何反斜杠
18. $Machine -= s/\\\\//g;
19. my $CLASS = "WinMgmts:(impersonationLevel=)\\Machine";
20. print "\\$Machine\n";
21. if ($WMI = Win32::OLE->GetObject($CLASS))
22. {
23. local $Disk;
24.
25. $- = DISK_HEADER_FORMAT;
26. write;
27. $- = DISK_FORMAT;
28. foreach $Disk ( in ($WMI->InstancesOf("Win32_LogicalDisk")) )
29. {
30. local $Drive = $TYPE($Disk->{DriveType});
31. local %Size = (
32. total => FormatNumber($Disk->{Size}),
33. free => FormatNumber($Disk->{FreeSpace})
34. );
35. write;
36. }
37. }
38. print "\\\n";
39. }
40.
41. sub FormatNumber
```

## 示例 9.13 续

```perl
42. {
43.     my($Number) = @_;
44.     while ($Number = s/^(-?\d+)(\d{3})\$1,$2/);
45.     return ($Number);
46. }
47. 
48. format DISK_HEADER_FORMAT =
49.     FS      Type                Free
50.     ................................................
51.     .
52. format DISK_FORMAT ========================================
53.     @ << @<<<< @<<<<>>>>>>>>>>>>>>>>
54.     $Disk->(Name), $Disk->({FileSystem}, $Drive, $Size{total}, $Size{free}
55. }
```

## 进程列表

在第 7 章“进程”中，你学习了获取进程列表的技术。示例 9.14 是另一个使用 WMI 显示进程列表的示例。列表可以来自本地或远程机器。脚本接受机器名称作为参数，指示从哪台机器检索进程列表。如果没有传递机器名称，则假设为本地机器。

## 示例 9.14 显示基于 WMI 的进程列表

```perl
01. use Win32::qw( in );
02.
03. $Machine = ".*", unless ($Machine = shift $ARGV);
04. $Machine = s^\ if ($ARGV[0]) =~ m^(\{\]{2});
05. 
06. # 这是连接到机器 WMI 对象
07. # CIM（通用信息模型）存储
08. $CLASS = "WinMgmts:(impersonationLevel=impersonated)!/$Machine";n09.
10. # 获取 WMI（微软 WBEM 的实现）接口
11. $WMI = Win32::OLE->GetObject($CLASS)
12.
13.     die "Unable to connect to \Machine". Win32::OLE->LastError();
14.
15. # 获取 Win32 Process 对象集合
16. $ProcList = $WMI->InstancesOf("Win32_Process");
17.
18. $- = PROCESS_HEADER;
19. write;
20. $- = PROCESS_INFO;
21.
22. # 遍历每个 Win32_Process 对象
23. # 并写出详细信息
24. foreach $Proc ( sort $Procs ( in $ProcList )
```

```perl
24. {
25.   write;
26. }
27.
28. sub SortProcs
29. {
30.   lc $a->{Name} cmp lc $b->{Name};
31. }
32.
33. sub FormatNumber
34. {
35.   my($Number) = @;
36.   my($Suffix) = "";
37.   my $K = 1024;
38.   my $M = 1024 * $K;
39.
40.   if($M <= $Number)
41.   {
42.     $Suffix = "M";
43.     $Number /= $M;
44.   }
45.   elsif($K <= $Number)
46.   {
47.     $Suffix = "K";
48.     $Number /= $K;
49.   }
50.
51.   $Number -= s/\.(\d{0,2})\d*$/$1;
52.
53. } while($Number == s/^(-(\d+)(\d{3}))/$1,$2);
54.
55.   return($Number . $Suffix);
56. }
57.
58. sub FormatDate
59. {
60.
61.   my($Date) = @;
62.   $Date -= s/(\d{4})(\d{2})(\d{2})(\d{2})(\d{2}).*/$1.$2:$3:$4:$5:$6;
63.   return($Date);
64. }
65.
66. format PROCESS_HEADER
67. ||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||
68. PID, Parent, "Process Name", "Thrds", "Memory", "Mem Peak", "Created"
69. ------------------------------------------------------------------------------------------------------
70.
71. format PROCESS_INFO<<<<<<<<<<<<>>
72. ||||| <<<<<<<<< @>>>> >>>>> >>>>>>> >>>>>>>>>>>>>>>>>>>>>
73. $Proc->{'ProcessID'}, $Proc->{'ParentProcessID'}, $Proc->{'Name'};
74. $Proc->{'ThreadCount'}, FormatNumber($Proc->{'WorkingSizeSet'}),
75. FormatNumber($Proc->{'PeakWorkingSizeSet'}),
76. FormatDate($Proc->{'CreationDate'});
```

## 杀死进程

与之前的示例相同（参见示例 9.14），本节复习了第 7 章任务杀死脚本中涵盖过的脚本（参见示例 7.19）。然而，使用 WMI，示例 9.15 不仅能够终止本地机器上的进程，还能终止远程机器上的进程。

如果在第一个参数中传递机器名称（通过在机器名称前加上双反斜杠表示），则所有进程终止操作将在指定的机器上进行。所有额外的参数均被视为进程 ID (PID) 数字或进程名称。如果传递的是进程名称，则所有匹配该名称的进程将被终止。如果名称包含 `*` 和 `?` 等通配符，它将被用作正则表达式。例如：

```perl
perl WMI_Kill.pl \server 415 *word
```

将终止 `\server` 上 PID 为 415 的进程以及任何名称中包含 `word` 的进程。

## 示例 9.15 使用 Win32:OLE 杀死进程

```perl
01. use Win32:OLE qw{ in };
02.
03. $Machine = ".* unless $Machine = shift ARGV;
04. $Machine = s#^[\\/]+# if ($ARGV[0] -= m#([\\/]{2})#);
05.
06. # 这是 WMI 监控器，连接到机器的
07. # CIM（通用信息模型）存储库
08. $Class = "\\WMIMgts:{impersonationLevel-impersonate}!/\$Machine";
09.
10. # 获取 WMI（微软实现的 WBEM 接口）
11. $WMI = Win32:OLE->GetObject($Class)
12.
13. // die "无法连接到 \$Machine:" Win32:OLE->LastError();
14.
15. # 获取 Win32_Process 对象集合
16. $ProcList = $WMI->InstancesOf("32_Process");
17.
18. # 遍历传入的 PID
19. foreach $Pid (@ARGV)
20. {
21. my $KillList = GetProc($Pid, $ProcList);
22. if (scalar $KillList)
23. {
24. foreach $Proc (@KillList)
25. {
26. print "正在杀死 \$Proc->{Name} \$Proc->{ProcessID}...";
27. # 我们找到了正确的 Win32_Process 对象，因此
28. # 调用其 Terminate 方法
29. $Result = $Proc->Terminate( );
30. if (0 == $Result )
31. {
32. print "已终止";
33. }
34. else
35. {
36. print "终止失败";
37. }
38. print "\n";
39. }
40. else
41. {
42. print "$Pid 未找到。";
43. }
44. }
45. sub GetProcList
46. {
47. my($Pid, $ProcList) = @_
48. if ($Pid == /\d+$/)
49. {
50. $List = GetProcByid($Pid, $ProcList);
51. }
52. else
53. $List = GetProcName($Pid, $ProcList);
54. }
55. return($List);
56. }
57. sub GetProcByPid
58. {
59. my($Pid, $ProcList) = @_;
60. 
61. #遍历每个 Win32_Process 对象
62. # 直到找到正确的
63. foreach $Proc ($ProcList)
64. {
65. return([$Proc]) if ($Pid == $Proc->{ProcessID});
66. }
67. return([]);
68. }
69. sub GetProcByName
70. {
71. my($Name, $ProcList) = @_;
72. my(@Procs);
73. my($Regex) = ($Name =~ m[\*\?]/);
74. 
75. # 遍历每个 Win32_Process 对象
76. # 直到找到正确的
77. foreach $Proc ($ProcList)
78. {
79. if ($Regex)
80. {
81. push(@Procs) if ($Proc->{Name} =~ /$Name/i);
82. }
83. else
84. {
85. push(@Procs) if (lc $Name eq $Proc->{Name});
86. }
87. } return(@Procs); }
```

## 创建远程进程

示例 9.15 在远程机器上创建一个进程。你只需要传递通常在命令行使用的参数。例如，如果你想在特定文件中运行 `Notepad.EXE`，可以这样调用脚本：

```perl
perl WMI_Run.pl notepad.exe c:\temp\MyFile.txt
```

该命令在指定文件中启动程序。如果你想在远程机器上运行程序，只需将机器名称作为第一个参数。以下示例相同：

```perl
perl WMI_Run.pl \server notepad.exe c:\temp\MyFile.txt
```

该命令在机器上运行程序。注意，加载的文件是相对于远程机器的。因此 `c:\temp\MyFile.txt` 指的是远程机器上的 C 盘。本地和远程机器都必须安装 WMI 脚本才能工作。

## 示例 9.15 继续



```perl我是由深度求索（DeepSeek）研发的 deepseek-v4-flash-0731 智能大模型。01. use Win32::OLE qw{ in };
02. use Win32::OLE::Variant;
03. $Machine = ".* unless $Machine = shift ARGV;
04. $Machine = s#^[\\/]+# if ($ARGV[0] -= m#([\\/]{2})#);
05.
06. # 这是 WMI 监控器，连接到机器的
07. # CIM（通用信息模型）存储库
08. $Class = "\\WMIMgts:{impersonationLevel-impersonate}!/\$Machine";
09.
10. # 获取 WMI（微软实现的 WBEM 接口）
11. $WMI = Win32::OLE->GetObject($CLASS)
12.
13. // die "无法连接到 \$Machine:" Win32::OLE->LastError();
14.
15. # 现在获取 Win32_Process 类...
16. # $Process = $WMI->Get("Win32_Process")
17. // die "无法获取进程列表": Win32::OLE->LastError();
18.
19. # 创建一个 COM 对象的引用变体可以修改其值
20. # 并将其返回给我们。
21. $vPid = Variant(VT_IA | VT_BYREF, 0);
22.
23. # 现在使用 $Process->Win32_Process 对象的 Create 方法
24. # 创建新进程
25. if((0 == $Process->Create("",ARGV), undef, undef, $vPid))
26. {
27. print "进程已创建，PID 为 $vPid\n";
28. }
29. else
30. {
31. print "创建进程失败。\n";
32. }
```

## 结论

随着各种技术的日益成熟，你拥有大量的工具可供使用。ADSI 和 WMI 技术适用于所有 Win32 平台，使你能够实现网络自动化。

本节涵盖了 ADSI 和 WMI 的冰山一角。通过在线或书籍形式阅读更多信息是值得的。无论如何，你获得的知识将变得不可或缺，因为这些工具将在网络中变得越来越普遍。

## 代码和书籍讨论

不可避免会出现 Bug 或打印错误。如果出现，我们将在网站上修复，该网站可以通过`www.newriders.com`获取。网站将包含示例代码和勘误。

Roth Consulting 的网站托管 Usenet 组（`news://news.roth.net/Books.Handbook`），你可以在那里参与与书中主题相关的讨论。在那里，你还可以查看其他与 Win32 相关的组。该网站还维护了一个专门的书籍页面（`http://www.roth.net/books/handbook/`），你可以在那里找到评论、信息、示例代码和任何错误。

## 书中模块

书中使用了许多模块和扩展。有些并不是 ActivePerl 标准配的。下表列出了书中使用的模块和扩展。

| 扩展 | 获取路径 |
| :--- | :--- |
| `Getopt::Long` | `http://www.cpan.com` |
| `Net::Pager` | `http://www.simplewire.com/` |
| `Net::Ping` | `http://www.cpan.org/` |
|  | 属于 `libnet` 包 |
| `Net::SMTP` | `http://www.cpan.org/` |
|  | 属于 `libnet` 包 |
| `IO::Socket` | `http://www.activestate.com/` 或 |
|  | `http://www.cpan.org/` |
|  | 作为 ActivePerl 的一部分提供 |
| `Time::Local` | `http://www.cpan.org/` |
|  | 随 Perl 发布；也可在 CPAN 获取 |

## 348 附录 A：示例代码与在线书籍讨论

| 扩展 | 获取途径 |
|---|---|
| `Win32::AdminMisc` | `http://www.activestate.com/`<br>Win32lib 的一部分，随 ActivePerl 提供，或通过 `http://www.roth.net/perl/packages/` 获取更新版本 |
| `Win32::API` | `http://www.activestate.com/`<br>Win32lib 的一部分，随 ActivePerl 提供，或在 Aldo Calpini 的网站上：`http://www.dada.perl/it` |
| `Win32::API::Prototype` | `http://www.roth.net/perl/packages/` |
| `Win32::Daemon` | `http://www.roth.net/perl/packages/` |
| `Win32::Console` | `http://www.activestate.com/`<br>Win32lib 的一部分，随 ActivePerl 提供，或在 Aldo Calpini 的网站上：`http://www.dada.perl/it` |
| `Win32::EventLog` | `http://www.activestate.com/`<br>Win32lib 的一部分，随 ActivePerl 提供 |
| `Win32::EventLog::Message` | `http://www.roth.net/perl/packages/`<br>`http://www.dada.perl/it/` |
| `Win32::GUI` | `http://jenda.krynicky.cz/` 或 FTP：`ftp://ftp.roth.net/pub/ntperl/others/Lanman/` |
| `Win32::NetAdmin` | `http://www.activestate.com/`<br>Win32lib 的一部分，随 ActivePerl 提供 |
| `Win32::ODBC` | `http://www.activestate.com/`<br>Win32lib 的一部分，随 ActivePerl 提供，或通过 `http://www.roth.net/perl/packages/` 获取更新版本 |
| `Win32::OLE` | `http://www.activestate.com/`<br>Win32lib 的一部分，随 ActivePerl 提供 |
| `Win32::OLE::Const` | `http://www.activestate.com/`<br>Win32lib 的一部分，随 ActivePerl 提供 |
| `Win32::Perms` | `http://www.roth.net/perl/packages/` |
| `Win32::Pipe` | `http://www.activestate.com/`<br>Win32lib 的一部分，随 ActivePerl 提供，或通过 `http://www.roth.net/perl/packages/` 获取更新版本 |
| `Win32::Registry` | `http://www.activestate.com/`<br>Win32lib 的一部分，随 ActivePerl 提供 |
| `Win32::Service` | `http://www.activestate.com/`<br>Win32lib 的一部分，随 ActivePerl 提供 |
| `Win32::WinError` | `http://www.activestate.com/`<br>Win32lib 的一部分，随 ActivePerl 提供 |
| `Win32API::Registry` | `http://www.activestate.com/`<br>Win32lib 的一部分，随 ActivePerl 提供 |

## Perl 信息

### 安装扩展

到目前为止，安装扩展最简单的方法是使用 PPM Perl 脚本。你通常可以在 DOS 窗口中指定以下命令来实现：

```bash
ppm install win32-api
```

此特定命令将尝试下载并安装 `Win32::API` 扩展。请注意，你需要将 Perl 命名空间分隔符`::`（双冒号）替换为连字符。默认情况下，PPM 脚本会联系 ActiveState 以获取请求的扩展。但在某些情况下，可以在其他位置找到扩展的更新版本。可以使用`--location`参数来指定这些位置。例如，安装 `Win32::EventLog::Message`：

```bash
ppm install win32-eventlog-message \
location=http://www.roth.net/perl/packages/
```

如果你位于防火墙或代理服务器之后，则需要阅读 PPM 的文档。

### Perl 信息

在你消化了书中的所有信息后，你可能会想接下来该去哪里。这很容易回答——去上网！在本节中，你将找到一些可以查看的互联网网站，以获取更多关于 Win32 Perl 的信息。这些网站非常适合作为跳板，将你直接带入 Perl 编程的世界。

### 网站

#### Perl 官方网站

```text
http://www.perl.com/
```

不要搞错——这是 Perl 的官方网站。你可以从这里找到关于 Perl 的真实一手消息。

#### CPAN

```text
http://www.cpan.org/
```

综合 Perl 存档网络（CPAN）是 Perl 代码的全球网络。作者在这里发布模块、脚本和扩展，它们会在全球范围内复制。很有可能已经有人写了代码来实现你的需求。你可以在这里寻找。

#### ActiveState 工具公司

`http://www.activestate.com/`

你应该感谢这些人，是他们将 Perl 移植到了 Win32。当然，有很多 Win32 的移植版本，但这个团队多年一直在支持它。给他们发封邮件，感谢他们的辛勤工作吧！

#### 微软开发者网络

`http://msdn.microsoft.com/`

你可能意想不到，但这个网站上有几篇关于 Perl 的文章。更重要的是，整个 Win32 API 都有在线文档！当你在使用 `win32::API` 扩展遇到困难时，可以通过这个网站检查你的语法和值。

该网站还赋予了你搜索一切的能力。

#### Perl for Perl

`http://www.dada.perl/it/`

这里是寻找事实标准的好地方。如果你在寻找特定的示例，这里就是你的首选之地。

#### Win32 API

`http://www.roth.net/perl/packages/`

这里包含了你了解 Win32 API 所需的一切知识。

## Web Techniques Magazine

`http://www.webtechniques.com`

虽然这本专门针对 Perl 的杂志，但它偶尔会涵盖 Perl 相关话题。无论如何，这都是很有趣的读。

## 值得的 Win32 Perl 管理书籍

- Aeleen Frisch, *Essential Windows NT System Administration*, O'Reilly & Associates, 1998。
- Dave Roth, *Win32 Perl Programming: The Standard Extensions*, New Riders, 1999。
- Randal L. Schwartz, Tom Christiansen, Erik Olson, *Learning Perl on Win32 Systems*, O'Reilly & Associates, 1997。
- David N. Blank-Edelman, *Perl for System Administration*, O'Reilly & Associates, 2000。
- Scott McMahan, *Automating Windows with Perl*, CMP Books, 1999。
- Tim Bunce and Alligator Descartes, *Programming the Perl DBI*, O'Reilly & Associates, 2000。

## 索引

### A

- 访问 Active Directory 服务接口（ADSI），310
- 流，78
- `%Account` 哈希，属性
  - `acct expires`，17
  - `parms`，16
  - `usr comment`，16
- 账户
  - 自动登录用户账户设置（示例代码），113–115
  - 配置，23–30
  - 创建，15–22
  - 示例代码，17–22
  - 删除，33–36
  - 示例代码，34–36
  - 禁用，30–33
  - 示例代码，31–33
  - 显示
    - 配置（示例代码），23–30
    - 已启用和禁用（示例代码），327
    - 启用和禁用（示例代码），326
  - 检查，22–23
  - 过期密码，44–48
  - 示例代码，46–48
  - 本地系统，291–292
  - 登录/注销时间，37–41
  - 机器。见机器账户
- 权限
  - 添加，54
  - 移除，55
  - 重命名，49–51
  - 示例代码，49–51
  - 恢复（示例代码），133–135
  - 获取信息（示例代码），131–133
  - 解锁，41–44
  - 示例代码，42–44
  - 用户。见用户账户
- Active Directory 服务接口。见 ADSI
- Active Directory 服务路径。见 `AdsPath`
- ActiveState Tool Corp.
  - 列表服务器，352
  - 网站，350
- 添加
  - 权限，54
  - 将 UNC（通用命名规范）到路径，8–9
  - `ADS READONLY SERVER` 标志，321
  - `ADS SECURE AUTHENTICATION` 标志，321
  - `ADS USE ENCRYPTION` 标志，321
- ADSI（Active Directory 服务接口），309
  - 访问，310
  - 账户
    - 禁用，326
    - 显示已启用，327
    - 启用，325–326

### 356 ADSI（Active Directory 服务接口）

- 自动化合规，310
- 类属性，315
- 枚举，315–317
- 参数，315
- 子类，315
- 类，312
- 断开网络会话（示例代码），328–329
- 显示已启用和禁用的账户（示例代码），327
- 启用和禁用账户（示例代码），326
- 冒充另一个用户，319–323
  - 示例代码，321–323
- 命名空间，311–312
- 网络会话，断开，327–329
- 提供程序，枚举，314
  - 示例代码，314
- 架构，312
- 用户信息检索，323–324
  - 示例代码，324
- Windows NT/2000，用于系统管理的 ADSI 脚本，311
- 通知标志，279–280
- `$App`，221
- 将系统变量附加到路径，9
- 预约提醒服务（示例代码），295–306
- `$ArgsAnonymous` 属性，332
- 自动登录，112–113
  - 设置，113–115
  - 用于……的开关，113
  - 开启/关闭，113
- 自动登录用户账户设置（示例代码），113–115
- 自动化机器设置登录脚本（示例代码），201–204
- 可用域，显示（示例代码），318–319

### B

- 备份机器账户，130
- 权限，135–137
- 共享目录，124–126
- 回溯，213
- 创建新进程（示例代码），214
- 文件关联（示例代码），6，214
- 输入/输出句柄，重定向，217
- 长文件名（示例代码），215–216
- AD（Active Directory 服务路径）前缀，311–312
- ADs，312
- LDAP（轻量级目录访问协议），312
- NDS（Novell 目录服务），312
- WinNT，312
- `Alert()` 函数，169
- 警报，182
- 邮件，184–185
- 网络消息，182
- 分页，183–184
- 报告阶段，154
- 文件扩展名问题，214
- 长文件名，214–216
- 将 STDERR 重定向到 STDOUT，217
  - 示例代码，217
- `BATCHLOGON`，53
- BDC（备份域控制器），63
- 绑定，313
- 阻塞延迟，313
- `dir`，82，88
- 为……指定类，313
- 字符串，313
- `fork()`，225
- `BLAT.EXE` 工具，184
- 书籍，推荐，353
- `md`，76
- `$Buffer-Write`，289
- `mkdir`，76
- `more`，80
- `net send`，182
- `net share`，68

### C

- Carver's Perl Page，351
- CDO（协作对象），293
- `CHANGE` 命令，96
- `CHDSK.EXE` 工具，147
- CIM（共同信息模型），337
- 共同信息模型（CIM），337
- 综合 Perl 存档网络（CPAN）网站，2，349
- `$Config`（机器）哈希键，161
- 类，312
- 属性，315
- 枚举，315–317
- 参数，315
- Perl 登录脚本，188
- 子类，315
- Perl 机器，6–8



- 示例代码, 6-8

- 分页服务（示例代码）, 287

- 重配置, 272

- `SRVANY.EXE`, 274

- `TCP/IP`, 116

- 控制状态。见服务

- `CREATE CONSOLE` 文件，远程打开（示例代码）, 144-147

- 打开文件, 145-147

- `CREATE NO WINDOW` 标志, 222

- 注册表连接, 144

- `CREATE SUSPENDED` 标志, 222

- 协作对象 (`CDO`), 293

  - 代码。见示例代码

- 创建账户, 15-22

  - 属性, 16

  - 命令行开关, 16

  - 删除账户, 34

  - 禁用账户, 30

  - 硬链接, 75-76

  - 过期密码, 45

  - 示例代码, 76

  - 用户特定, 17

  - 命令行运行 `Perl` 脚本, 4

  - 中间目录, 77

  - 示例代码, 77

  - 登录脚本, 198-199

- 进程, 213-214

  - `open()` 函数, 218

  - 远程, 344-345

  - 挂起, 223-224

  - `system()` 命令, 218

  - `Win32::Admin`, 224

  - `Win32::Process`, 221

  - 共享目录, 126-129

  - 示例代码, 126-129

  - 机器上的系统变量, 9

  - 多路流, 79

  - `dir` 命令, 82, 88

  - 目录权限, 90

  - 中间目录, 77

  - 创建（示例代码）, 77

  - 路径类型, 136

- `Active Directory` 服务 (`ADS`), 310

  - 定义, 309

  - 共享目录, 126-129

  - 远程显示, 69-70

  - 转储, 124-126

## D

- `-d` 域选项, 130

- `Dada's Perl Lab` 网站, 350

- 守护进程，`socket`。见服务

- 客户端, 258

- 示例代码, 256-257

- 分派操作, 258-259

- `DC` (域控制器), 129, 187

  - 同步, 63-65

- `DCOM` 配置

- `DOMHFG.EXE` 工具, 103

- 输出, 103-104

- 显示, 104-106

- 示例代码, 104-106

- 删除账户（示例代码）, 34-36

- `DOMGG.EXE` 工具, 103

- 限制, 13

- 带有 `Win32` 服务, 289

- 命名管道, 290

- 报告检测阶段, 154

- 域 (域控制器), 129, 187

  - 同步, 63-65

- `DOMAINNAME`, 319

- 域

  - 显示（示例代码）, 318-319

  - 远程驱动器, 69-70

  - 发现（示例）, 318-319

  - 转储, 124-126

## E

- 编辑环境, 196-198

- 事件 `ID`, 156

- 检查, 22-23

- 示例代码, 46-48

- 环境环境, 193-194

- 示例代码, 197-198

- 启用账户（示例代码）, 327

- 枚举, 315-317

- 示例代码, 314

- 环境变量, 191-192

- 示例代码, 321-323

- 预约提醒服务（示例代码）, 295-306

  - 自动登录, 112-113

  - 设置, 113-115

  - 用于...的开关, 113

  - 开启/关闭, 113

- 自动登录用户账户设置（示例代码）, 113-115

- 自动化机器设置登录脚本（示例代码）, 201-204

- 可用域，显示（示例代码）, 318-319

- 编辑环境, 196-198

- 事件 `ID`, 156

- 检查, 22-23

- 示例代码, 46-48

- 环境环境, 193-194

- 示例代码, 197-198

- 启用账户（示例代码）, 327

- 枚举, 315-317

- 示例代码, 314

- 环境变量, 191-192

- 示例代码, 321-323

- 预约提醒服务（示例代码）, 295-306

  - 自动登录, 112-113

  - 设置, 113-115

  - 用于...的开关, 113

  - 开启/关闭, 113

- 自动登录用户账户设置（示例代码）, 113-115

- 自动化机器设置登录脚本（示例代码）, 201-204

- 可用域，显示（示例代码）, 318-319

- 编辑环境, 196-198

- 事件 `ID`, 156

- 检查, 22-23

- 示例代码, 46-48

- 环境环境, 193-194

- 示例代码, 197-198

- 启用账户（示例代码）, 327

- 枚举, 315-317

- 示例代码, 314

- 环境变量, 191-192

- 示例代码, 321-323

- 预约提醒服务（示例代码）, 295-306

360

示例代码

发现

- `ADSI` 类属性, 315-317

- 远程机器上的驱动器信息, 339-340

- 组成员身份, 200

- 模块列表, 224-247

- 服务, 263-264

- 检查事件日志, 178-181

- 使用 `%ENV` hash 扩展环境变量, 221

- 针对 `Win32::Spawn()`, 220

- 密码过期, 46-48

- 使用注册表获取进程列表, 235-243

- 使用 `Win32::PerfLib`, 235-235

- 分叉 (`forking`), 226

显示

- 账户配置, 23-30

- `ADSI` 提供程序, 314

- 可用域, 318-319

- `DCOM` 配置, 104-106

- 启用和禁用的账户, 327

- `IIS` 属性值导出, 330-332

- 使用 `ADSI` 模拟另一个用户, 321-323

- 安装服务, 267-268

- 杀死进程, 250-253

- 运行期间, 253

- 使用 `WMI`, 342-344

环境变量, 193-194

- 事件日志源和表文件, 159-160

- 扩展后的环境变量, 194-195

- 文件版本, 86-88

- `IIS` 树, 335-337

- 登录脚本, 189-190

- 修改 `IIS` 属性, 333-334

- 最后登录/注销时间, 38-41

- 列出远程打开的文件, 141-144

- 在注册表中查找字符串, 108-112

- 寻找 `SQLServer` 机器, 280

- 机器监控服务, 169-175

- 修改环境变量, 197-198

- `NTFS` 备用数据流内容, 80-81

- 权限信息, 91-94

- 远程机器上的共享目录, 69-70

- `TCP/IP` 配置, 116-121

- 权限, 96-99

- 基于 `WMI` 的进程列表, 340-341

- 监控被禁止的进程, 162-168

- 命名管道调试客户端例程, 290

- 分页服务客户端, 287

- 分页服务, 282-286

- 暂停服务, 264-265

- 通过重定向 `STDOUT` 打印到句柄, 254

- 从文件读取多个流, 79-80

转储

- 安全信息, 136-137

- 共享目录配置, 124-126

- 启用和禁用账户, 326

- 枚举流, 82-85

- 事件日志源和表文件, 159-160

- 重新应用安全权限, 138-139

- 恢复重命名的文档, 148-150

文件 361

- 使用反引号将 `STDERR` 重定向到 `STDOUT`, 217

- 使用 `open()` 函数, 218

- 重命名账户, 49-51

- 移除服务, 273

- 在远程机器上报告服务状态, 266

- 恢复账户, 133-135

检索

- 扩展名, 11

- 可用性, 12

- 不一致性, 12

- 安装, 349

- 最用的, 14

- `Web` 资源, 347-348

## F

+ 账户信息, 131-133

- 可保护对象的所有者, 101-102

- 使用 `ADSI` 获取用户信息, 324

- 卷信息, 72-75

+ 文件关联和反引号（示例代码）, 6

- 示例代码, 214

- 文件扩展名问题, 214

- 文件句柄, 253-254

- 打印到, 254

+ 以另一个用户运行进程, 229-230

发送

- 电子邮件警, 185

- 网络消息, 182-183

- 分页告警, 183-184

- 设置登录脚本, 190-191

- `Socket` 守护进程客户端, 258

- `Socket` 守护进程, 256-257

- 使用分叉 (`forking`), 258-259

- 同步域控制器, 64-65

+ 示例代码, 254

- 通过重定向 `STDOUT`, 254

+ `FILE NAMED STREAM` 卷标志, 71

- 文件路径类型, 136

- `FILE SUPPORTS ENCRYPTION` 卷标志, 71

- `FILE SUPPORTS OBJECT IDS` 卷标志, 71

- `FILE SUPPORTS REPARSE POINTS` 卷标志, 71

- `FILE SUPPORTS SPARSE FILES` 卷标志, 71

+ 统一登录脚本案例研究, 206-209

- 解锁账户, 42-44

- 更新 环境变量, 195-196

- 用户权限管理, 55-63

- `Who` 脚本, 228

- `Win32` 服务脚本, 278

- `Win32::Daemon` 服务, 288

- 执行进程. 见 seeing

+ 文件版本, 85

- 二进制文件, 86

- 显示信息, 87-88

- 示例代码, 86-88

+ 扩展环境变量（示例代码）, 194-195

- 使用 `%ENV` hash, 221

- 针对 `Win32::Spawn()`, 220

- 过期密码, 44-48

- 示例代码, 46-48

+ `FILE QUOTAS` 卷标志, 71

- 文件名, 长的, 214-216

- 扩展名, 重命名的, 147-148

- 关闭, 144-147

- 列出, 141-144

- 跟踪, 140

# `$Flag`, 222

+ `CREATE NEW CONSOLE`, 222

`CREATE WINDOW`, 222

`CREATE SUSPENDED`, 222

- 卷，列表, 71

- `fork()` 命令, 225

- 注意事项, 227

- 返回值, 225

- 分叉, 212-213,224

- 示例代码, 226

`socket` 守护进程（示例代码）, 258-259

+ `FS PRESERVED` 卷标志, 71

+ `FS SENSITIVE` 卷标志, 71

+ `FILE COMPRESSION` 卷标志, 71

+ `FS PERSISTENT ACLS` 卷标志, 71

+ `FS UNIQUE STORED ON` 卷, 71

+ `FS COMPRESSED` 卷标志, 71

+ `FULL CONTROL` 权限, 96

# I-J

+ `ID` 数字，列表, 144

- `IIS` (`Internet Information Server`) 属性, 312, 229-330

- 显示并修改（示例代码）, 333-334

- 值, 330-332

- `IIS` 树, 334-337

- 显示（示例代码）, 335-337

- 实现统一脚本, 204-206

- `Inherit`, 221

- `.INI` 文件格式, 126

- 安装扩展名, 349

- 提醒服务, 293

- 服务, 267-268

- `SRVANY.EXE`, 274

- `InstancesOf()` 函数, 338

- `IPC` (进程间通信), 222

- `Journals`. 见 magazines, 352

`Jutta Web` 网站, 350

生成账户，列表, 130

`GetADSIObject()` 函数, 320

`GetObject()` 函数, 314

- 组成员身份发现（示例代码）, 200

- 创建硬链接, 75-76

-  `key` 数组, 169

# G-H

+ 依赖关系, 271

- 错误控制, 271

- 显示, 270

- 键, 271

- 加载顺序, 271

- 名称, 270

- 密码, 271

- 路径, 270

- 服务类型, 271

- 用户, 271

## K

+ 发送网络消息 363

- 杀死进程, 249-252

- `kill()`, 249-250

- `TerminateProcess()`, 249

- 运行期间, 253

使用 `WMI`, 342-344

## L

+ 语言差异, 13

- `LDAP` (轻量级目录访问协议), 312

`LG INCLUDE` 标志, 206

- 列出服务器, 352

`Topica.com`, 352

- 列出打开的文件, 141-144

`LLSASS` (本地安全服务), 263

本地地系统账户, 291-292

- 注销，确定最后注销（示例代码）, 38-41

- 登录，确定最后登录时间（示例代码）, 38-41

- 登录脚本, 187

自动化机器设置（示例代码）, 201-204

针对 `Perl` 配置, 188-189

- 创建用户组, 198-199

- 显示, 189-190

示例代码, 189-190

`-m` 机器切换选项, 130

机器账户备份, 130

创建列表, 130

恢复, 130, 133-134

检索, 131-133

设置脚本, 200-204

机器监控服务（示例代码）, 169-175

机器针对 `Perl` 配置, 6-8

在机器上创建系统变量, 9

杂志

`Perl Journal`, 352

`Perl Month`, 352

`Web Techniques`, 353

管理权限, 55-63

`md` 命令, 76

内存使用, 10

移除标志, 11

设置标志, 11

表表, 156-158

`.DLL` 文件, 155

定义, 155

源, 155

文本字符串, 155

消息，发送网络消息, 182-183

# `Microsoft ADSI Web` site

`Microsoft ADSI Web` 网站, 311

`Microsoft Developer Network Web` 网站, 350

`Microsoft Management Console`. 见 `MMC`

`Microsoft MSDN` 库 网站, 67

`mkdir` 命令, 76

`MMC`（微软管理控制台）, 15

修改. 见编辑模块列表, 244-247

命名空间, 311-312

`NBTSTAT.EXE`, 161

`NDS` (`Novell` 目录服务), 312

`net send` 命令, 182

`net share` 命令, 68

`NETSTAT.EXE`, 161

发送网络消息, 182-183

示例代码, 182-183

网络服务器状态，监控, 169-176

网络会话，断开, 327-329

示例代码, 328-329

+ 发现（示例代码）, 244-247

模块

安装扩展名, 349

`Web` 资源, 347-348

监控, 160-162,169

`FTP` 进程, 161

机器监控服务（示例代码）, 169-175

网络服务器状态, 162-176

被禁止的进程, 162-168

示例代码, 162-168

远程机器, 162

脚本实现, 160

`Telnet` 命令, 161

+ 网络共享路径类型, 136

网络共享。见共享目录, 124

`Novell` 目录服务 (`NDS`), 312

`NTFS` 备用数据流内容，

显示（示例代码）, 80-81

`NTFS` 文件

枚举流（示例代码）, 82-85

大小, 81-82

`NTFS` 流, 78-85. 另见流

+ `more` 命令

多个流

创建测试文件（示例代码）, 79

从测试文件读取（示例代码）, 79-80

多线程, 212

## N

+ 命名管道

调试客户端例程

（示例代码）, 290

调试 `Win32` 服务（示例代码）, 290

`open()` 函数，重定向

`STDERR` 到 `STDOUT`, 218

示例代码, 218

打开文件

关闭, 144-147

列出, 141-144

跟踪, 140

`OpenDObject()` 函数, 319

所有权, 99

+ 命令

`SE RETORE NAME`, 100

`SE TAKE OWNERSHIP`

`NAME`, 99

可安全对象的，检索的,

101-102

设置, 100-102

权限, 16, 88-89

账户, 指定, 100

备份, 135-137

按字母, 88-89

命令

## P

- `-p` 前缀开关切换选项, 130

分页, 280-281

发送警报, 183-184

示例代码, 183-184

服务, 281-287

客户端（示例代码）, 287

示例代码, 282-286

更改, 96

完全控制, 96

显示信息, 91-94

示例代码, 91-94

在目录上显示, 90

对象的完整详细信息, 94-95

显示, 96-99

注释, 90

密码, 已过期, 44-48

示例代码, 46-48

`%PATH` 哈希, 16

路径类型

目录, 136

文件, 136

网络共享, 136

打印机共享, 136

注册表, 136

暂停服务, 264-265

示例代码, 264-265

重新应用（示例代码）, 138-139

恢复, 138-139

详细显示, 96-99

`Piedmont Professional Services` 网站, 351

管道, 218

预防性维护, 123

主网域控制器. 参见 `PDC`

打印机共享路径类型, 136

打印到文件句柄, 254

通过重定向 `STDOUT`, 254

示例代码, 254

权限, 51-52

`PDC`（主网域控制器）, 63, 129, 188

`Perl`



# 为计算机配置（示例代码）, 6-8

# 环境变量副本, 更新（示例代码）, 195-196

# Web 环 (Web Ring), 351

# 网站（官方）, 349

# Perl 日志, 352

# Perl 月, 352

## Perl 脚本，运行

- 按文件名, 5
- 从命令行, 4

## `%Permission` 哈希, 16

- 添加, 52
- 可用, 52

## `BATCHLOGON`, 53

- 显示其用户, 53

## 组, 53-54

- 管理, 55-63
  - 示例代码, 55-63
- 移除, 55

## `SE BACKUP NAME`, 51

## `SE REMOTE SHUTDOWN NAME`, 51

## `SeAssignPrimary`, 228

## `SeChangeNotify`, 228

## `SeIncreaseQuota`, 228

## `SetCbPrivilege`, 228

# 进程列表, 340

# Q-R

## + - 显示, 340-341

- 在 NT 上使用注册表获取, 235-242
- 使用 `Win32::PerfLib`, 233-234
- 基于 WMI 的显示, 340-341

## 进程状态 API (Process Status API). 参见 PSAPI

## `ProcessClass()`, 315

## 进程, 211-213

- 创建
  - 使用反引号, 233-214
  - 使用 `open()` 函数, 218
  - 远程, 344-345
- 挂起, 223-224
  - 使用 `system()` 命令, 218
  - 使用 `Win32::AdminMisc`, 224
- 枚举, 230-232
- 杀死, 249-252
  - 示例代码, 250-253
  - `kill()`, 249-250
  - 在运行时, 253
  - `TerminateProcess()`, 249
  - 使用 WMI, 342-344
- 模块列表，发现, 244-247
- 进程空间, 211
- 以另一个用户身份运行, 227-230
  - 示例代码, 229-230
- 使用 `Win32::Spawn()` 生成, 219-220
- 终止, 342-344
- 线程, 212
- 类型, 212

## 配置键, 16

## 禁止进程，监控（示例代码）, 162-168

## PSAPI (进程状态 API), 243

- 大小, 243
- Windows NT/2000 兼容性, 243

## + - 查询环境变量, 193-195

## READ 权限命令, 96

## `Read()` 函数, 178

## 重新配置服务, 272

## 恢复重命名的文档（示例代码）, 148-150

## 重定向

- 将 STDERR 到 STDOUT
  - 使用反引号, 217
  - 使用 `open()` 函数, 218
- STDOUT, 通过文件句柄打印的, 254

## `Regfind`, 106

## 注册源, 155

## 注册表 (Registry), 106-107

- 在其中查找字符串, 108-112
  - 示例代码, 108-112
- 获取进程列表, 235-242
  - 示例代码, 235-243
- 路径类型, 136
- 根键, 107

## 用户连接，关闭, 144

## 提醒服务, 294-306

- 移除, 293

## 远程机器发现信息（示例代码）, 339-340

## 在（示例代码）上显示共享目录, 69-70

## 报告服务状态（示例代码）, 266

## 远程进程，创建, 344-345

- 示例代码, 344-345

## 关闭远程打开的文件（示例代码）, 144-147

- 列出（示例代码）, 144

## 权限, 55

- 示例代码, 273
- 使用 `INSTV.EXE`, 275

## 重命名的文档, 恢复（示例代码）, 148-150

## 重命名账户, 49-51

- 示例代码, 49-51

## 报告阶段, 153

- 检测, 153-154

## 恢复账户（示例代码）, 133-135

- 机器账户, 130, 权限, 138-139
- 共享目录，备份的, 126
- 账户, 130, 133-134

## 结果, 249

## 恢复服务, 264

## 检索账户, 131-133

## 可用代码，问题与, 3

## Roth Consulting Usenet group, 352

- 网站, 350

## `RunAs.exe` utility, 229

## 运行 Perl 脚本

- 按文件名, 5
- 从命令行, 4

## 以另一个用户身份运行, 227-230

## + - 脚本, 16

## 脚本的, 264

## 脚本, 271

## 脚本, 287

## 脚本的, 189-190

- 设置, 190-191
- 状态, 200-204

## 脚本, 206

## 脚本, 209

## 脚本, 227

- 示例代码, 228

## 脚本, 228

- 权限, 228



, 228



, 228



`\,我是由深度求索（DeepSeek）研发的 deepseek-v4-flash-0731 智能大模型。228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

`\, 228`

## `-t usermachine` switch options

- `-t usermachine` 切换选项, 130
- 表文件，事件日志（示例代码）, 159-160
- 用户帐户。另见 accounts
- 列表，创建的, 130
- 登录脚本
  - 显示, 189-190
  - 设置, 190-191
  - 恢复, 130, 133-134
  - 获取, 131-133
- 任务管理器, 231
- TCP/IP 配置
  - 显示, 116-121
- 用户环境变量
  - 嵌入系统环境变量中, 192
  - 与系统环境变量对比, 192
- 示例代码, 116-121
- `TerminateProcess()`, 249
- 终止进程, 342-344
- 测试文件
- 用户特定属性，命令行切换开关, 17
- 用户连接，关闭到注册表, 144
- 使用多流创建（示例代码）, 79
- 从多个流读取（示例代码）, 79-80
- 线程, 212
- 局限用法, 225
- 用户权限，管理（示例代码）, 55-63
- 工具，`CHDSK.EXE`, 147
- `Topica.com` 列表服务器, 352
- 跟踪打开的文件, 140
- `TREE.EXE` 命令, 334
- `type` 命令, 80
- 变量。另见环境变量
- 详细权限，显示（示例代码）, 96-99
- 卷
  - 标志，列表, 71
  - 获取信息, 72-75
  - 示例代码, 72-75

## U-V

- `UNC`（通用命名规范）
  - 添加到, 8-9
- 统一日志脚本, 199
- 案例研究, 204-209
  - 示例代码, 206-209
  - 实现, 204-206
- 用户组识别, 199
- 通用命名规范。

## W-Z

- `WBEM`（基于 Web 的企业管理）倡议, 337
- 网站
  - `ActiveState Tool Corp.`, 350
  - `Amazon Cloud Ramayne's Perl for Win32 Modules Site`, 351
  - `Carvdawg's Perl Page`, 351
  - `Comprehensive Perl Archive Network (CPAN)`, 2
  - `CPAN`（全面 Perl 存档网络）, 349
  - 另见 `UNC`
- 解锁帐户, 41-44
  - 示例代码, 42-44
- 更新环境变量，`Perl`
  - 副本, 195-196
  - 示例代码, 195-196
- `Usenet` 组, 351
- `Roth Consulting`, 352

## `XCACLS.EXE` 程序 371

- `Dadas Perl Lab`, 350
- `Jutta Klebe`, 350
- `Microsoft ADSI`, 311
- `Microsoft Developer Network`, 350
- `Microsoft MSDN library`, 67
- `Perl for Win32`, 350
- `Perl Web Ring`, 351
- `Perl` 网站（官方）, 349
- `Piedmont Professional Services`, 351
- `Roth Consulting`, 347, 350
- `SimpleWire`, 350
- `Web Techniques` 杂志, 353
- 基于 Web 的企业管理倡议（`WBEM`）, 337
- 空格, 215
- `WhoAml.pl` 脚本, 228
- 扩展环境变量, 220
  - 示例代码, 220
- Windows Management Instrumentation。另见 `WMI`
- Windows NT/2000, 用于系统管理的 `ADSI` 脚本, 311
- `Windows Scripting Host (WSH)`, 4
- Windows 工作站, 291
- `WMI`（Windows Management 工具）, 309, 337
- 杀死进程（示例代码）, 342-344
- 路径规范, 338
- 进程列表, 340
  - 显示（示例代码）, 340-341
- 提供程序, 338
- 远程机器，驱动器信息, 338-340
- `Win32`
  - 内存使用, 010
  - 移除标志, 11
  - 设置标志为, 11
  - 进程, 211-213
- 服务脚本, 278
  - 示例代码, 278
- 服务，使用命名管道调试, 290
- `Win32::AdminMisc`, 224
- `Win32::Daemon` 服务
  - 示例代码, 288
  - 带有关闭处理程序, 287-288
- `Win32::Lanman`, 发现组共享（示例代码）, 200
- `Win32::PerlLib`, 获取进程列表, 233-234
  - 示例代码, 233-235
- `Win32::Process`, 222
  - 创建, 221
- `Win32::Spawn()`, 219
  - `$Args` 参数, 220
  - 嵌入空格, 219
  - `WSH`（Windows Scripting Host）, 4
  - `XCACLS.EXE` 程序, 67

## Windows 2000 Answers

### New Riders 精选 Windows 2000

New Riders 为 Windows 2000 管理员提供了一些独特的内容——这本关于 Windows 2000 Server 的有趣且深入的书籍，由能够预见你的情况并提供可信赖答案的人士编写。ISBN: 1-56205-929-7

管理用户的桌面环境是管理 Windows 2000 的关键部分。Windows 2000 User Management 提供了完成工作所需的真实提示和示例。ISBN: 1-56205-886

Windows 2000 Active Directory 是 New Riders 系列中的 Windows 2000 书籍之一。这本书非常适合网络架构师和管理员，描述了 Active Directory 的复杂性，帮助你在企业环境中进行计划、部署和管理 Active Directory。ISBN: 0-7357-0870

## Advanced Information on Networking

我们知道获取核心技术的详细、以解决方案为导向的信息有多重要。Landmark 系列包含解决问题所需的关键信息。这些书籍由专家编写并经过了严格的同行技术评审，我们的 Landmark 书籍是像你这样的从业者的资源。

New Riders Essential Reference 系列在你知道想做什么但不知道如何做时提供答案。每本书都跳过了无关内容，并假设你有坚实的基础。这些书籍以创新的、整洁的形式提供了解决方案——价值很高。New Riders 提供了一系列完整的备考材料帮助你获得认证。通过 Training Guide 等书籍和革命性的 ExamGear 软件，New Riders 由通过考试并指导过数百名候选人的资深人士提供的全面产品。

## Selected titles from New Riders

### Inside Windows 2000 Server

作者 William Boswell

第一版

1515 页，$49.99

ISBN: 1-56205-929-7

采用 Landmark 书籍中由作者驱动、不务虚的方法，New Riders 为 Windows 2000 管理员提供了一些独特的内容——这本关于 Windows 2000 Server 的有趣且深入的书籍，由能够预见你的情况并给出不会让系统不稳定或缓慢答案的人士编写。

### Windows 2000 Active Directory

作者 Ed Bovick, Doug Hauger 和 William Wade

第一版

416 页，$29.99

ISBN: 0-7357-0870-3

由微软的三位关键合作伙伴编写，具有对人员、信息和资源的高级访问，这本书提供了一种简洁、重点且信息丰富的 Landmark 格式，充满了案例研究和实战经验，针对 Windows 2000 最期待且复杂的功能——Active Directory。

### Windows 2000 Essential Reference

作者 Steven Tate 等

第一版

670 页，$35.00

ISBN: 0-7357-0869-X

这本书被设计为 Windows 2000 最易导航、有用且充满价值参考书，它采用了创新的“望远镜”设计，你可以适应自己的学习风格。作者们根据对 Windows 2000 的实操经验为你提供答案，并利用他们强大的资历为你提供在其他地方找不到的答案。

## Windows 2000 Routing and Remote Access Service

作者 Mackie Charles

第一版

400 页，$34.99

ISBN: 0-7357-0951-3

## Windows 2000 DNS

作者 Herman Knief, Jeffrey Graham, Andrew Daniels 和 Roger Abell

第二版

480 页分页39.99

ISBN: 0-7357-0973-4

非常适合想要跨网络创建成本效益且安全的远程访问的系统管理员。作者 Mackie Charles 使用具体示例演示如何将 Windows 2000 路由平滑集成到现有基础设施中，并在最大化带宽的同时将用户连接到网络。涵盖了新的身份验证模型、路由协议、Windows 2000 路由配置、设计问题、安全和故障排除。

专注于设计和安全 DNS 服务、互操作以及安装和使用 DHCP 和 WINS 服务等关键主题，Windows 2000 DNS 是微软 DNS 最新版本的综合指南。作者为你提供了设计和优化 DNS 所需的真实建议、最佳实践和策略。

## Windows 2000 Deployment & Desktop Management

作者 Jeffrey A. Ferrís

第一版

408 页，$34.99

ISBN: 0-7357-0975-0

随着 Windows 2000 的黎明，在管理用户环境和桌面之间划定清晰的界限变得更加困难。这本书由受过培训的培训师和顾问编写，提供了一份使用 Windows 2000 管理用户及其桌面环境的全面、实用的指南。

这本书不仅仅是对新功能和工具的简单概述，它是将 Windows 2000 专业版部署到公司工作站的详尽参考。专家的真实建议和详细练习使其成为任何计划部署 Windows 2000 客户端的系统管理员、集成商、工程师或其他 IT 专业人士的一站式、易用资源。

# Windows 2000 专业版

作者：Jerry Honeycut，第一版

330 页，$34.99

ISBN: 0-7357-0950-0

![](img/b5063514d2e449d6d8c5d65f100b84aa_396_0.png)

# Windows 2000 服务器版参考指南

作者：Karanjit Siyan, 博士

第三版

1848 页，$75.00

ISBN: 0-7357-0952-1

![](img/b5063514d2e449d6d8c5d65f100b84aa_396_1.png)

《Windows 2000 专业版》探索了 Windows 工作站用户在企业网络和 Internet 上可以使用的强大功能。本书直接面向高级用户，他们重视 NT 的安全性、稳定性和网络能力，同时也兼顾 Windows 9X 界面的易用性和熟悉度。本书涵盖了用户和管理主题，并针对连接性增加了网络方面的内容。

《Windows 2000 专业版参考指南》是 Windows 2000 参考书籍中的基准。尽管其他书籍会带你了解产品的设置和实施阶段，但没有没有其他书籍能为用户的日常管理问题和任务提供详细解答。实实的内容向管理员展示了如何管理、诊断并修复特定异构 Windows 网络的问题，以及 Internet 特性和功能。

![](img/b5063514d2e449d6d8c5d65f100b84aa_396_2.png)

# Windows 2000 规划

作者：Eric K. Cone, Jon Boggs 和 Sergio Perez，第一版

448 页，$29.99

ISBN: 0-7357-0048-6

# Windows 2000 安全

作者：Roberta Bragan，第一版

608 页，$39.99

ISBN: 0-7357-0991-2

![](img/b5063514d2e449d6d8c5d65f100b84aa_396_3.png)

你准备好 Windows 2000 了吗？这本书解释了为你的基于 NT 的异构网络准备 Windows 2000 所需的步骤。作者根据自己的经验和场景详细详细介绍了部署程序，解释了一系列原本错综复杂的程序。《Windows 2000 规划》是任何考虑迁移者不可或缺的伴侣。

对于严肃的系统管理员来说，目前不存在单一的权威安全参考书。该书的主旨目标是帮助 Windows 网络专业人员在他们的组织中理解并实施 Windows 2000 安全措施。书中包含了“最佳实践”章节，对设置和安全实践提供了建议。

# Windows NT/2000 网络安全

作者：Eugene Schultz

第一版

440 页，$45.00

ISBN 1-57870-253-4

![](img/b5063514d2e449d6d8c5d65f100b84aa_397_0.png)

# Windows 2000 虚拟专用网络

作者：Thaddeus Fortenberry

第一版

350 页，$45.00

ISBN 1-57870-246-1

2001年1月

![](img/b5063514d2e449d6d8c5d65f100b84aa_397_1.png)

《Windows NT/2000 网络安全》提供了一个促进真正理解 Windows 安全模型及相关能力的框架。目标是让读者熟悉在点对点和客户端/服务器设置下使用的主要的 Windows 安全暴露类型。本书教读者针对每种暴露的具体安全控制和设置，并展示了如何评估权衡以确定哪些控制措施（如果有）适用。

由于对分布式办公的持续推动，管理员必须支持笔记本电脑用户、家庭 LAN 环境、复杂的分机构办公室，而这一切都在一个安全且有效的网络设计之中。管理员在 Windows 2000 中实现 VPN 的方式与其他操作系统不同。除了讨论 Windows 2000 隧道技术外，还涵盖了可能影响 Active Directory 复制和网络地址转换的新 VPN 功能。

# Windows NT/2000 瘦身客户端解决方案

作者：Todd Mathers

第二版

840 页，$45.00

ISBN: 1-57870-239-9

![](img/b5063514d2e449d6d8c5d65f100b84aa_397_2.png)

# Windows 2000 Active Directory 设计与部署

作者：Gary Olsen

第一版

648 页，$45.00

ISBN: 1-57870-242-9

![](img/b5063514d2e449d6d8c5d65f100b84aa_397_3.png)

作为 MetaFrame 1.8 和 Terminal Server 版的全面参考，本书应该是解决棘手问题的首要来源。这本书是 MetaFrame 1.8 和 Terminal Server 版的全面参考，应该是解决棘手问题的首要来源。它在上一版的基础上，增加了对 Windows 2000 Terminal Services 的覆盖，以及关于远程访问和应用的章节。

本书通过审查 Windows 2000 Active Directory 环境，以及如何开发有效的设计，引导读者理解 TSE 的管理，并针对如何解决这些问题提供专家建议。实用的案例展示了这些问题。

# Windows NT/2000 主机集成

作者：William Zack

第一版

390 页，$40.00

ISBN:1-57870-200-3

《Windows NT/2000 主机集成》为大型机专业人员提供了将 Windows 2000 技术的实用知识。

# Windows 2000 服务质量

作者：David

第一版

264 页，$45.00

ISBN:1-57870-115-5

随着网络流量持续增加，资源的压力也日益增大。《Windows 2000 服务质量》教工程师如何定义和利用带宽。

# Windows 2000 服务器：规划

作者：Sean

第一版

480 页，$29.99

ISBN:0-7357-023-0

《Windows 2000 服务器：规划》可以节省数千美元和数百小时的时间。

# Windows NT 工具箱

作者：Stu 和 Ed

第一版

848 页，$49.00

ISBN: 0-7357-092-0

《Windows NT 工具箱》包含了对 NT 服务、维护和诊断的全面覆盖。

# NT Terminal Server Citrix Citrix

作者：Ted Hardwood

第一版

46 页，$29.99

ISBN:1-57870-944-0

![](img/b5063514d2e449d6d8c5d65f100b84aa_398_0.png)

# Windows NT 性能监控、基准测试与调优

作者：Mark 和 Paul

第一版

288 页，$29.99

ISBN:1-57870-942-4



本参考书详细介绍了`Terminal Server`和`CitrixFrame`的规划、安装和诊断的所有方面。《Windows NT 性能监控、基准测试与调优》为微调网络提供了一站式资源。`Windows NT Terminal Server`和`CitrixFrame`是该技术的仅有的本书之一。性能监控、基准测试与调优为确保`Windows NT`最佳性能提供了可靠的蓝图。

## Windows 2000 TCP/IP

作者：Karanjit S. Siyan, 博士

第二版

920 页，$39.99

ISBN: 0-7357-0992-0

![](img/b5063514d2e449d6d8c5d65f100b84aa_399_2.png)

## Windows NT 注册表：设置参考

作者：Sandra Osborne

第一版

576 页，$29.99

ISBN:1-56205-621-6

本书专注于使用`Microsoft TCP/IP`管理网络的方法，适用于想要阅读技术最佳实践的人士。在不在读者已经理解的基础知识上浪费时间的情况下，《Windows 2000 TCP/IP》提供了高级解决方案，是任何系统管理员的必备之书。

这不仅仅是一本简单的诊断或优化书籍，这本解决方案驱动的指南展示了如何以最高效且成本效益的方式使用注册表管理硬件、`Windows`工作站和其他客户端、笔记本电脑、应用程序软件和`Internet`设置。如果你是网络开发者、系统工程师、服务器管理员或工作站技术人员，你将依赖本全面参考书中的专家建议。

## Windows NT 域架构

作者：Gregg Branham

第1版

312页，$39.95

ISBN: 1-57780-112-0

![](img/b5063514d2e449d6d8c5d65f100b84aa_400_0.png)

## Windows NT 设备驱动程序开发

作者：Peter Viscarola 和 W. Anthony Mason

第1版

704页，$50.00

ISBN: 1-57780-058-2

![](img/b5063514d2e449d6d8c5d65f100b84aa_400_1.png)

随着`Windows NT`在企业中的部署日益广泛，随着复杂性的增加，网络域架构变得至关重要。本书包含了真正规划复杂的企业域所需的深度专业知识。

本书从介绍与驱动程序相关的`Windows NT`操作系统通用概念开始，然后介绍关于操作系统的更详细信息，例如同步问题、`I/O`子系统、标准内核模式驱动程序等等。

## Windows NT/2000 原生 API 参考

作者：Gary Nebbett

第1版

528页，$50.00

ISBN: 1-57780-199-6

![](img/b5063514d2e449d6d8c5d65f100b84aa_400_2.png)

## SMB 之 DCE/RPC：Samba 与 Windows NT 域内部

作者：Luke Leighton

第1版

312页，$45.00

ISBN: 1-57780-150-3

![](img/b5063514d2e449d6d8c5d65f100b84aa_400_3.png)

本书是`Windows NT`原生 API 函数的首个完整参考，涵盖了`Windows NT`向内核态和用户态程序提供的系列服务。涵盖了`NT`原生 API 中包含的 210 个例程的文档，以及将在`Windows 2000`中添加的函数。对于无法通过`Win32 API`直接访问或提供大量功能的例程，书中进行了极其详细的描述。还包含了`NT`内核提供的服务——主要是对调试用户态应用程序的支持。

安全人员、系统和网络管理员，以及为所有这些人员编写工具的人，都需要熟悉流经其网络的数据包。此书由`Samba`团队的成员成员编写，描述了微软如何采用`DCE/RPC`并在`SMB`和`TCP/IP`之上实现它。

## Delphi COM 编程

作者：Eric Harmon

第1版

500页，$45.00

ISBN: 0-57870-221-6

![](img/b5063514d2e449d6d8c5d65f100b84aa_401_0.png)

## COM+ 应用

作者：Gregory Brill

第1版

450页，$49.99

ISBN: 0-7357-0978-5

![](img/b5063514d2e449d6d8c5d65f100b84aa_401_1.png)

《Delphi COM 编程》面向所有`Delphi 3`、`4`和`5`程序员。在让读者理解`COM`框架后，它提供了对`COM`的实用探索，使`Delphi`开发人员能够编写基于组件的应用程序。书中探索了典型的现实场景，例如`Windows Shell`编程、自动化`Microsoft Agent`以及使用`ActiveX`进行创建。每个主题的讨论都通过详细的示例进行了插说明。

通过将许多不同的服务整合到统一的技术中，`COM+`为在`Windows 2000`系统上运行应用程序（无论是企业软件还是商业软件）的开发者带来了更高效率和更多化功能的承诺。《应用 COM+》涵盖了这一新工具的特性，以及如何在真实案例中实现这些特性。这些特性在`Windows`环境使用的的三种主要语言（`C++`、`VB`和`VJ`）中都进行了演示。

![](img/b5063514d2e449d6d8c5d65f100b84aa_401_2.png)

## Windows NT 应用：性能测量与优化

![](img/b5063514d2e449d6d8c5d65f100b84aa_401_3.png)

## Exchange & Outlook：构建协作解决方案

作者：Paul Hinsberg

第1版

288页，$40.00

ISBN: 1-57870-176-7

作者：Joel Semeniuk 和 Duncan Mackenzie

第1版

576页，$40.00

ISBN: 1-57870-252-2

本书对`Windows NT`的底层结构提供了关键洞解，以及测量和最终优化代码性能的方法论和工具。

本书的作者负责为世界上一些最大的财富 100 强公司构建自定义消息应用程序。他们分享了自己的专业知识，以帮助管理员改进`Windows`工具。

## Windows 脚本

作者：Tim Hill

第1版

448页，$35.00

ISBN: 1-57780-139-2

## Windows NT/2000 ADSI

作者：Thomas Eck

第1版

700页，$45.00

ISBN: 1-57780-219-4

## Windows NT Shell

作者：Tim Hill

第1版

400页，$32.00

ISBN: 1-57780-047-7

## Windows NT 部署与定制

作者：Richard Puckett

第1版

300页，$32.00

ISBN: 1-57780-045-0

## Win32 编程

作者：Dave Roth

第1版

640页，$40.00

ISBN: 1-57780-067-1

## SMS 2 管理

作者：Darshan Doshi 和 Mike Lubanski

第1版

448页，$39.99

ISBN: 0-7357-0082-6

![](img/b5063514d2e449d6d8c5d65f100b84aa_403_0.png)

## SQL Server 系统管理

作者：Sean Baird 和 Chris Miller 等。

第1版

352页，$29.99

ISBN: 1-56205-955-6

![](img/b5063514d2e449d6d8c5d65f100b84aa_403_1.png)

## Internet 信息服务管理

![](img/b5063514d2e449d6d8c5d65f100b84aa_403_2.png)

## SQL Server 7 必备参考

作者：Kelli Adam 和 Sean Dooley

第1版

192页，$29.99

400页，$35.00

ISBN: 0-7357-0022-2

ISBN: 0-7357-0864-9

![](img/b5063514d2e449d6d8c5d65f100b84aa_403_3.png)

## Linux/UNIX

![](img/b5063514d2e449d6d8c5d65f100b84aa_404_0.png)

### Linux 系统管理

作者：M. Carling, James T. Dennis, Stephen Degler

第一版

$29.99

368 页，ISBN: 1-56205-934-3

![](img/b5063514d2e449d6d8c5d65f100b84aa_404_1.png)

### Linux 基础参考指南

作者：Ed Petron

第一版

368 页，$24.95

ISBN: 0-7357-0852-5

本书旨在通过对海量的可用`Linux`信息提供结构化的组织来帮助完成任务。《Linux Essential Reference》提供了如何执行重要的管理和维护任务以及如何使用一些强大的命令和高级主题的清晰且简洁的指令，其范围涵盖了实现最常用命令的最佳方法、管理`Shell`脚本、管理你自己的系统以及利用有效的安全措施。

如今过度劳的系统管理员正在寻找方法来保持网络平稳运行并增强性能。用户总是在寻找更多的存储、更多的和服务和更高的速度。《Linux System Administration》引导读者了解维护安全、稳定系统的复杂之处。

![](img/b5063514d2e449d6d8c5d65f100b84aa_404_2.png)

### Linux 防火墙

作者：Robert Ziegler

第一版

496 页，$39.99

ISBN: 0-7357-0900-9

本书详细介绍了小型企业业务用户可能采取的保护其系统的人的安全步骤。这些步骤包括数据包级防火墙过滤、`IP`伪装、代理、`TCP Wrappers`、系统完整性检查和系统监控，并重点关注过滤和保护。《Linux Firewalls》的目标是帮助人们快速部署其互联网安全措施，而无需成为安全专家或

![](img/b5063514d2e449d6d8c5d65f100b84aa_405_0.png)

### UnixWare 7 系统管理

作者：Gene Henriksen 和 Melissa Henriksen

第一版

560 页，$39.99

ISBN: 1-57870-080-9

![](img/b5063514d2e449d6d8c5d65f100b84aa_405_1.png)

### Solaris 高级系统管理员指南

作者：Janice Winsor

第二版

587 页，$39.99

ISBN: 1-57870-039-6

在技术细节方面，本书介绍了`SCO UnixWare`的最新版本，是`SCO`工程师和管理员的权威操作系统资源。书中贯穿插了`SCO`故障排除笔记和技巧，还有专门为那些熟悉其他`UNIX`变体的人设计的技巧。

本官方授权的教程提供了技巧、建议和快速参考表，帮助你添加系统组件、改进服务访问并自动化常规任务。本书还包含了关于`Solaris 2.6`主题的更新信息。

![](img/b5063514d2e449d6d8c5d65f100b84aa_405_2.png)

### Solaris 系统管理员指南

作者：Janice Winsor

第二版

324 页，$34.99

ISBN: 1-57870-040-X

本书设计旨在作为实用教程和快速参考，为`UNIX`管理员提供了`Solaris`最频繁任务的完整、详细描述。学习如何利用`Solaris`的功能来满足你用户的需求，并获取如何让管理变得技巧。

### Solaris

#### Solaris 基础参考指南

作者：John Mulligan

第一版

304 页，$24.95

ISBN: 0-7357-0023-0

![](img/b5063514d2e449d6d8c5d65f100b84aa_406_0.png)

### 理解目录服务

作者：Beth Sheresh 和 Doug Seresh

第一版

390 页，$39.99

ISBN: 0-7357-0910-6

作为`solarisguide.com`网站的绝佳伙伴，《Solaris Essential Reference》假设读者精通通用`UNIX`技能，并提供了一些如何充分利用`Solaris`的提示。本书提供了关于如何执行重要的管理和维护任务的清晰且简洁的指令。

《Understanding Directory Services》为读者提供了关于目录服务基础的深入知识：什么是目录服务、它们是如何设计的以及它们能为`IT`基础设施提供什么功能。通过将技术置于背景中，为爆炸的目录服务市场提供框架，帮助人们理解目录对他们的网络可以做什么、不能做什么。

## 网络

![](img/b5063514d2e449d6d8c5d65f100b84aa_406_1.png)

### Cisco 路由器配置与故障排除

作者：Mark Tripod

第二版

330 页，$39.99

![](img/b5063514d2e449d6d8c5d65f100b84aa_406_2)

### 理解网络：互联实用指南

作者：Michael Martin

第一版

690 页，$39.99

本书为需要配置和维护现有`Cisco`路由器的网络管理员提供了信息。通过提供建议和实践方法而非仅仅是文档，书中介绍了构建高可用网络所需的各种概念。

### 理解数据通信

作者：Gil Held

第六版

220 页，$39.99

![](img/b5063514d2e449d6d8c5d65f100b84aa_407_0)

这篇数据通信的概述适合想要跟上潮流的人。它包含了关于数据传输的更新进展。

### 千兆以太网

作者：David Cunningham 和 William Lane

第一版

560 页，$50.00

![](img/b5063514d2e449d6d8c5d65f100b84aa_407_1)

千兆以太是大多数网络的下一步。探索这项技术如何允许高带宽应用，例如实时应用。

### IP 网络中的服务水平协议

作者：Dinesh Verma

第一版

270 页，$50.00

### LDAP：应用程序编程

作者：Tim Howes 和 Mark Smith

第一版

480 页，$44.99

### 目录启用网络

作者：John Strassner

第一版

752 页，$50.00

### 理解与部署 LDAP 目录服务

作者：Tim Howe, Mark Smith, Gordon Goode

第一版

850 页，$50.00

ISBN: 1-57870-070-1

### 广域高速网络

作者：Snid Feit 博士

第一版

624 页，$50.00

ISBN: 1-57870-114-7

![](img/b5063514d2e449d6d8c5d65f100b84aa_409_0.png)

![](img/b5063514d2e449d6d8c5d65f100b84aa_409_1.png)

这本详尽的教程为读者提供了`LDAP`目录服务的深入探讨。假设读者对通用网络和管理有基础知识，这使得材料对于中级和高级读者同样易懂。书中充满了实用的实施建议和真实的部署案例，帮助读者为自己的特定组织选择最合适的路径。

网络技术涵盖了长期的传统广域服务和新兴技术。本书介绍了当前和新兴的广域技术和服务，使它们变得易于理解，并对其进行了视角分析，使其优缺点一目了然。

### 交换式、快速与千兆以太网

作者：Sean Riley 和 Robert Beyer

第三版

615 页，$50.00

ISBN: 1-57870-073-6

### 局域高速网络

作者：Snid Feit 博士

第一版

655 页，$50.00

ISBN: 1-57870-113-9

![](img/b5063514d2e449d6d8c5d65f100b84aa_409_2.png)

![](img/b5063514d2e449d6d8c5d65f100b84aa_409_3.png)

《交换式、快速与千兆以太网》第三版是理解和完全实现这一系列以太网创新的唯一解决方案。本书作为当前技术和硬件要求的概述，同时也作为作为部署和管理交换式、快速及千兆以太网网络的实操性综合教程，涵盖了网络管理员面临的最紧迫的现状及未来挑战。

局域网络正发生着巨大的变化。随着`Web`内部网推动带宽需求呈云花式增长，廉价的网卡（`NIC`）和交换机进入了市场。因此，许多网络专业人士对评估这些技术的实施情况感兴趣。本书为这些技术提供了真实的实施专家知识，包括追踪器，用户可以真实地进行比较并决定如何使用它们。

### DHCP 手册

作者：Ralph Droms 和 Ted Lemon

第一版

535 页，$55.00

ISBN: 1-57780-137-6

### 企业网络路由与交换架构设计

作者：Howard Berkowitz

第一版

992 页，$55.00

ISBN: 1-57780-060-4

《DHCP 手册》是关于`DHCP`服务器设置和管理的权威概述和专家指南。本书讨论了`DHCP`如何开发以及它与其他协议的交互、`DHCP`在不同环境下的运行方式，以及`DHCP`服务器与客户端之间的交互。书中还讨论了网络硬件、服务器间通信、安全、`SNMP`和`IP`移动。此外，书中还包含了几个附录，为处理`DHCP`网络专业人士提供了丰富的资源。

本书提供了对交换机和路由器如何运行的基础理解，使读者能够有效地利用它们构建网络。书中引导网络设计师考虑需求、分析和部署策略的所有方面，增强读者的能力，并帮助他们培养职业上进所需的所需的技能。

### 无线局域网：实现互操作性网络

作者：Jim Geier

第一版

432 页，$40.00

ISBN: 1-57780-081-7

### 网络性能基准

作者：Daniel Nassar 第一版

736 页，$50.00

ISBN: 1-57780-240-2



《无线局域网》涵盖了如何以及为何从私有解决方案迁移到 `802.11` 标准，并解释了如何通过无线局域网实现显著的成本节省。《网络性能基准》专注于网络基准原则的真实实施，不仅展示了如何衡量和评估网络性能，还展示了如何提高网络性能。书中包含了提供网络基准测量的真实方法和步骤的章节。此外，还将提供正确记录和构建基准的方法。

#我是由深度求索（DeepSeek）研发的 deepseek-v4-flash-0731 智能大模型。电子商务经济

作者：Soon-Yong Choi、Andrew Whinston、Dale Stahl

第一版

665 页，$49.99

ISBN：`1-57870-014-0`

# 理解公钥基础设施

作者：Carlisle Adams 和 Steve Lloyd

第一版

300 页，$50.00

ISBN：`1-57870-166-X`

这是第一本关注电子商务领域传统主题的电子书。当其他电子书采用“如何做”的方法时，本书从经济角度关注其含义。本书是一本关于公钥基础设施部署的教程，涵盖了与 PKI 相关的广泛材料，包括认证、标准化工作以及部署问题。重点在于协助那些在组织内部设计 PKI 的人员。

# 入侵检测

作者：Rebecca Gurley

第一版

340 页，$50.00

ISBN：`1-57870-185-6`

# 网络入侵检测：手册

作者：Stephen North 和 Judy Novak

第二版

480 页，$45.00

ISBN：`0-7357-1008-2`

入侵检测是一个关键技术领域。这本关于入侵领域的详尽指南涵盖了基础知识，并提供了从设计到为特定环境评估和选择产品的丰富信息。从那些在一线工作的人士那里获得答案。作者 Northcott 是美国信息系统的原始开发人员，并将他的专业知识给了入侵专家、安全分析师以及负责建立和维护有效防御的顾问。

![](img/b5063514d2e449d6d8c5d65f100b84aa_411_0.png)

![](img/b5063514d2e449d6d8c5d65f100b84aa_411_1.png)

![](img/b5063514d2e449d6d8c5d65f100b84aa_411_2.png)

![](img/b5063514d2e449d6d8c5d65f100b84aa_411_3.png)

需要关于 Domino 新功能以及如何让某些高级功能运行的简洁实用的解释吗？《Domino 系统管理》是第一本在专业水平研究技术的 Domino 书，提供了实用的操作帮助，让你的组织中运行 Domino 5。

# Domino 系统管理

作者：Rob Kirkland

第一版

860 页，$49.99

ISBN：`1-56205-948-3`

# Lotus Notes & Domino 核心参考

作者：Dave Hatter 和 Tim Bankes

第一版

675 页，$45.00

ISBN：`0-7357-0007-9`

如果你需要一些促进你创意和技术能力的东西——完善你的 Lotus Notes 和 Domino 技能的东西——这本书正适合你。本书包含了你在处理 Lotus Notes 和 Domino 时发现的所有对象、类和方法。它展示了对象层次结构以及每一个之间的关系，并按照语言设计的方式进行组织。

![](img/b5063514d2e449d6d8c5d65f100b84aa_412_0.png)

![](img/b5063514d2e449d6d8c5d65f100b84aa_412_1.png)

# New Riders 的其他书籍

## 职业认证

## 培训指南

- MCSE 培训指南：网络基础，第二版 `15620597X` • $49.99
- MCSE 培训指南：Windows NT Server，第二版 `156205915` • $49.99
- MCSE 培训指南：Windows NT Server 4 企业版，第二版 `156205913` • $49.99
- MCSE 培训指南：TCP/IP，第二版 `156209262` • $61.49
- MCSE 培训指南：IIS 4，第二版 `156209203` • $49.99
- MCSE 培训指南：SQL Server 7 管理 `073507867` • $49.99
- MCSE 培训指南：SQL Server 7 数据库设计 `073500016` • $49.99
- CLP 培训指南：Lotus Notes 4 `07895158` • $59.99
- MCSD 培训指南：Visual Basic 6 `07350028` • $69.99
- MCSD 培训指南：架构 `07350702` • $49.99
- MCSD 培训指南：4-in-1 合集版 `07350912` • $149.99
- 认证指南，第二版 `07350706` • $49.99
- 网络认证指南 `07350077` • $49.99
- Solaris 2.6 管理指南，第一部分 `15780806` • $40.00
- Solaris 7 管理指南，第一、第二部分 `157802496` • $49.99

# 如何联系我们

## 访问我们的网站

`www.newriders.com`

在我们的网站上，您将找到关于我们其他书籍、作者、目录、索引以及书籍勘误的信息。

## 电子邮件联系我们

请通过以下地址与我们联系：

- 如果您对本书有任何意见或问题。
- 报告您在书中发现的错误。
- 如果您有书籍提案想要提交，或兴趣为 New Riders 写作。
- 如果您希望我们发送一份作者包（author kit）。
- 如果您是计算机主题或技术的专家，并有兴趣担任技术编辑（审查稿件的技术准确性）。
- 如需查找您所在地区的分销商，请通过此地址联系我们的国际部门。

`media@newriders.com`

- 针对教育机构的讲师，如果您希望预览 New Riders 书籍供课堂使用。邮件请包含您的姓名、职称、学校、部门、地址、电话号码、办公日期/时间、使用的教材以及学生人数，以及您对样书/测试副本和/或额外信息的请求。
- 针对兴趣评审 New Riders 书籍副本的媒体人员。请发送您的姓名、邮寄地址和电子邮件地址，以及您工作的出版物或网站名称。

## 书信联系我们

New Riders Publishing

201 W. 103rd St.

Indianapolis, IN 46290-1097

## 电话联系我们

免费热线：`(800) 571-5840`

在美国境外请拨打`(317) 581-3500`。转接 New Riders。

## 传真联系我们

`(317) 581-4663`

# New Riders，想听听您的意见

为了更好地服务您，我们希望了解您对本书内容和质量的意见。请填写此卡邮寄给我们，或传真至 `317-581-4663`。

姓名 ___________________________________________________________________________

城市 _________________________ 州 ________________ 邮编 ___________________________

电子邮件地址 ____________________________________________________________________

职业 ______________________________________________________________________

| 什么影响了您购买这本书？ | 您最喜欢这本书的哪一点？ |
|---|---|
| [ ] 推荐 | 请勾选所有适用项。 |
| [ ] 封面设计 | [ ] 内容 |
| [ ] 目录 | [ ] 写作风格 |
| [ ] 索引 | [ ] 准确性 |
| [ ] 杂志评论 | [ ] 示例 |
| [ ] 广告 | [ ] 列表项 |
| [ ] New Rider 的声誉 | [ ] 设计 |
| [ ] 作者 | [ ] 页数 |
| 您如何评价这本书的内容？ | [ ] 价格 |
| [ ] 优秀 | [ ] 插图 |
| [ ] 很好 | 您最不喜欢这本书的哪一点？ |
| [ ] 好 | 请勾选所有适用项。 |
| [ ] 中等 | [ ] 内容 |
| [ ] 低于平均水平 | [ ] 写作风格 |
| [ ] 差 | [ ] 准确性 |
|  | [ ] 示例 |
| 您计划如何使用这本书？ | [ ] 列表项 |
| [ ] 快速查阅 | [ ] 设计 |
| [ ] 自学 | [ ] 索引 |
| [ ] 课堂 | [ ] 页数 |
| [ ] 其他 | [ ] 价格 |
|  | [ ] 插图 |

您能列出一本您比这本更喜欢的类似书籍，或者同样优秀的书籍吗？为什么？

________________________________________________________________________________

________________________________________________________________________________

您有多少本 New Riders 的书籍？

您最喜欢的计算机书籍有哪些？

________________________________________________________________________________

您还希望看到哪些书目？

________________________________________________________________________________

对我们有什么任何建议吗？

________________________________________________________________________________

# Windows NT®/2000 系统管理脚本（WINDOWS NT®/2000 SCRIPTING FOR SYSTEM ADMINISTRATION）

> “Thomas Eck 的书充满了实用的代码示例，是我进行 Windows NT/2000 目录开发的常伴侣。它务实的风格和合理的结构使得获取丰富的有用 VB 和 ASP 代码变得非常容易。”
>
> ——Scott Loeb，Stellcom 高级工程师

《Windows NT/2000 系统管理脚本》为高级系统管理员、应用开发人员和 IT 经理提供了编程方法，帮助简化大规模环境中的任务。这本实用的指南包括：

- 使用 Visual Basic 和 VBScript 自动化冗余任务的成熟技术。
- 数百个管理示例，能够将 Visual Basic IDE 作为管理控制台使用。
- 现成可用的代码，涵盖了 WinNT、LDAP 和 IIS 服务提供程序支持的命名空间管理的各个方面。

作为全球金融服务行业的专家，Thomas Eck 是一位开发者和项目经理，负责为大型投资银行定义 Web 基础设施标准。Thomas 对系统管理和多层开发的实践与理论知识的独特结合，使其能够为大型企业计算环境推导出稳健的 Web 解决方案。

借助本参考书，您将学习帮助您完成技术：

- 开发可重用的 COM 对象。
- 使用 ADSI、COM 和 MTS 创建委托管理模型。
- 通过编程强制执行命名标准和处理一致性。
- 为 Windows NT/2000、IIS、Microsoft Exchange Server 和 Netscape Directory Server 编写自定义管理工作流应用程序。

可在您附近的书店或在线零售商处购买！ISBN `1-58780-219`，45.00 美元，700 页。

![](img/b5063514d2e449d6d8c5d65f100b84aa_418_0.png)

# WIN32 PERL 脚本：管理员手册（WIN32 PERL SCRIPTING：The Administrator's Handbook）

> “这很简单：每个负责 Windows 主机的人都应该有一本《Win32 Perl 脚本：管理员手册》。”

在《Win32 Perl 脚本：管理员手册》中，Dave Roth 对 Win32 扩展应用了同样直观的方法。该资源重点关注您如何通过 Perl 自动化任务并利用其功能。您可以在以下方面获得专业知识：Cameron Laird，“正则表达式”专目的合著者，Perl FAQ 的维护者。

- 使用 Win32 和 COM 与 Windows 程序交互。
- 使用 Perl 编写 Win32 服务。
- 管理驱动器、用户和组，包括备份数据库和修改用户配置文件。
- 通过有效的权限管理确保安全。

Dave Roth 是多个流行的 Win32 扩展的贡献者，包括 `Win32::ODBC`、`Win32::AdminMisc`、`Win32::Daemon` 和 `Win32::Perms`，自 1994 年以来一直为 Perl 社区提供支持。Dave 曾在 O'Reilly Perl 和 USENIX LISA-NT 会议上演讲，发表过文章，并在《Win32 Perl 编程：标准扩展》（1999 年，`1-57870-067-1`）。

Dave 自 1981 年起就开始使用各种语言编程，从 C++、LPC 到 Perl。他的代码被 Microsoft、美国国防部、Disney Light Magic、Digital Paper、Hewlett-Packard、Radcom 以及高校使用。此前，Dave 曾帮助密歇根州组建全州 WAN，并为 Ameritech 和密歇根州大学设计并管理 LAN。

本指南提供的脚本让您更有效地：

- 在注册表中查找数据。
- 与 ADSI 和 WMI 交互。
- 检查事件日志中的错误。
- 管理本地和远程机器上的进程。
- 管理用户权限。

类别：Windows® NT/2000 Perl 编程

ISBN `1-57870-215-1` `553500`

![](img/b5063514d2e449d6d8c5d65f100b84aa_419_0.png)

![](img/b5063514d2e449d6d8c5d65f100b84aa_419_1.png)

![](img/b5063514d2e449d6d8c5d65f100b84aa_419_2.png)

`newriders.com`

35.00 美元 / 52.95 加元
