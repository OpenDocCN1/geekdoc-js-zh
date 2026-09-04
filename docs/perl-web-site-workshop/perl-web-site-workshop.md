
# Perl 网站构建指南

## 关于作者

毫无疑问，在 Web 设计和开发领域，Molly E. Holzschlag 是周围最有活力的个性之一。Molly 拥有二十部 Web 开发书籍的著作，她还是一位极富有魅力的演讲者和老师，经常出现在 Comdex、Internet World、Web 2001 和 Web Builder 等会议上。

Molly 被誉为“Web 前 25 位女性”之一，是 Web 主机组织（World Organization of Webmasters）的顾问委员会成员、Web 标准项目（Web Standards Project）的成员，并曾担任 WebReview.com 的执行编辑一年。关于 Molly 的书籍、文章、活动和 Web 相关活动的更多信息，请访问（还能去哪呢？）http://www.molly.com/。

Jason Pellerin 是 Playboy.com 的高级 Web 应用开发人员，那里涉及裸露比你想象的少得多，而 Perl 则多得多。在此之前，他是已故且备受怀念的 Bungie Software 的系统管理员，在那里负责维护 bungie.net 在线杀戮场的正常运行，并通过 Bungie Store 向未成年人出售不当的 T 恤。Jason 拥有耶鲁大学的哲学学士学位、两只猫，以及对被诅咒的棒球球队奇怪的好感。

献给 E。

— Jason

献给 Randal，Perl 世界中我最好的呼唤者

— Molly

特别感谢 Mark Taber 在本书出版过程中提供的所有支持。Clinton A.Pierce 勇敢地投入战斗提供帮助，我们对他的帮助表示感谢。Waterside 的 David Fugate 帮助了细节和特殊之处（代理人的特长），并像往常一样完成了卓越的工作。

# 引言

许多 Web 设计师发现，为了给他们的网站添加坚实的功能，他们需要学习将设计目标与服务器解决方案相结合。Perl 是一种极其强大且灵活的方式，可以帮助设计者实现他们的目标。

在书中，我们创建了一个网站工作坊，提供了你立即让 Perl 运行所需的所有脚本和编程内容。无论你是一个设计师，还是任何对使用 Perl 为网站添加功能感兴趣的人，本书都采取了非常实用的方法。

本书并没有从学习语言开始，而是分为不同的章节，重点关注 Web 开发人员可能想在其网站上包含的不同应用：表单、游戏和更高级的技术。这些脚本是随取随用的，读者只需按照逐步说明即可帮助他们安装并根据个人喜好进行修改。

随书附带了一张 CD，里面装满了 Perl、Perl 模块和本书的脚本。

本书作为一个实用的工具，赋予读者添加多个级别功能的能力，同时兼顾跨浏览器和平台的兼容性。但理想情况下，这个工作坊还将激发读者学习更多 Perl 的愿望，从而使他们在技能和对 Perl 在 Web 设计中角色的理解上成长。

# 第一章 Web 上的 Perl

Web 设计师自然地关注客户端设计和技术。通常，他们对感知中涉及服务器技术的复杂性感到谨慎。加深他们顾虑的是，许多针对 Web 设计师的书籍和文章忽略了有关服务器技术的细节，倾向于推荐咨询系统管理员或互联网服务提供商 (ISP)，而不是提供直观的细节。

事实真相是，设计师可以使用 Perl 为网站设计创建奇妙的交互性。诚然，你可能不会成为下一个 Perl 编程大师（好吧，如果你想的话），但你完全可以使用 Perl 来增强你的设计。我们编写了《Perl 网站工作坊》就是为了帮助你实现这一点。我们的目标是让设计师能够接触到最强大、应用最广泛的语言之一。

Perl 负责 Web 的许多幕后功能。如今许多尖端网站（如 Yahoo! 和 Amazon）以某种方式使用 Perl 连接数据库、处理表单。

Perl 极其易用且强大。正如你将在后续章节中学到的，即使不是 Perl 程序员也能让 Perl 运行。我们为非程序员人士设计了本书。如果你担心因为自己不是程序员就无法掌握 Perl，请放心。我们将指导你完成一切。

为了帮助你理解为什么 Perl 是许多程序员的首选语言，我们在本章中提供：

- Perl 的基本描述
- 浏览器技术与服务器技术之间主要区别的讨论
- 对 Perl 冒险中关键伙伴：通用网关接口 (CGI) 的解释

我们将查看哪些服务器支持 Perl，并让你体验本书在 Perl 方面的价值。

## 关于 Perl

Perl 的易用性很大程度上归于其父亲 Larry Wall 的利他精神。它的技术起源多样，包括被称为 C 的编程语言和一个名为 `awk` 的 Unix 工具。Larry Wall 受 Unix 工具环境局限性的挑战，因此开始了 Perl。

Wall 将他的新生语言推向了 Usenet 互联网新闻组的荒野，在那里他遇到了无数的评论和反馈——其中许多已并入该语言，目前处于第五版本。在本书时，稳定版本是 5.6.1，实验性开发版本是 5.7。该开发版本不建议用于标准生产环境。

你可以从随书附带的 CD 中安装 Perl——我们包含了 Microsoft Windows、Macintosh 和 Unix 的最新版本。或者你可以从以下地址下载 Perl 的最新版本：

www.perl.com/pub/language/software.html

## Perl 网站制作工作坊

入门之处是 http://www.perl.com。你可能还想访问 http://www.perl.com/CPAN/ 来获取 Perl、Perl 文档以及大量的常见问题（FAQs）。

令所有人高兴的是，Perl 是免费的。实际上，它是一门非常民主的语言。它得到了用户的支持，其模块和文档（更不用说语言本身的各个方面）全部由志愿者爱好者编写。它完全符合开源的理念和信念。

## 关于开源

开源是一个术语，用于描述那些被设计为供他人自由共享、部分改进和重新分发的软件。开源软件已经存在了一段时间，但最近其关注度有所提高，特别是通过近期行业对 Linux 的认可。

Perl 在设计初考虑了 Unix。然而，这门语言已经移植到几乎每一个流行的平台，包括 Windows、Macintosh、VMS、MS-DOS 甚至 Amiga。

## 服务器对比浏览器

开源运动的两个重要前提是：开源软件必须无限制地重新分发，并且对软件本身的任何代码更改必须向社区开放。Perl 遵循了这些原则。

要理解 Perl 如何在 Web 上工作，理解服务器端编程与浏览器端（或客户端）编程之间的区别，以及 Web 服务器与 Web 浏览器之间的通用关系至关重要。活跃了几年的 Web 设计师可能还记得服务器端图像映射（imagemaps）。映射需要服务器处理映射坐标才能使其工作——这是一个服务器端编程的熟悉示例。

稍后，JavaScript 开启了客户端（或浏览器）的脚本功能。如今，我们可以选择多种方法来实现最终目标，但事实仍然是，Web 服务器和 Web 浏览器之间以一种日益复杂且集成的关系相互依赖。

Web 服务器和 Web 浏览器手手协作，以交付最终显示在 Web 页面访问者屏幕上的信息。

当网站访问者通过输入 URL 地址或点击链接发出请求时，浏览器会将请求的文档发送到服务器。在最简单且常见的情况下，服务器将此请求发送给浏览器，由浏览器进行解释并显示在访问者的屏幕上。请求通常是 HTML 文档或图形文件。

![](img/d26997dc0c0571017b4729525ba1a4ac_15_0.png)

为了扩展和增强 Web 的功能，这种交换方式被添加了服务器端编程和浏览器端编程。

当浏览器向服务器发送请求时，该请求可以是一个文档，也可以触发一个作为 Perl 脚本的服务器端程序在服务器上运行。如果在服务器端触发了程序，浏览器在程序运行期间将与服务器保持连接。一旦程序完成，结果将发送到浏览器，一切准备就绪。

在浏览器端编程（如 JavaScript）的情况下，浏览器像往常一样从服务器发送并接收请求。请求的文档包含一个浏览器端程序，该程序在浏览器内部执行。

因此，服务器端程序运行在服务器上，而浏览器端程序运行在浏览器内部。

曾几何时，服务器端编程并不是一种偏好，而是唯一的选择。浏览器并不足够复杂来独立管理复杂的任务。它们的工作仅仅是提供一个窗口来查看基于 Web 的文档。

过去几年里，浏览器技术发生了巨大的变化。激烈的竞争和渴求的公众使浏览器开发者扩展了浏览器的功能。现在，开发者和设计师在何处以及如何运行应用程序方面有越来越多的选择。

关于哪种更好一直存在着争论。当基于浏览器的技术强势地介入舞台时（例如 JavaScript 的情况），专业意见由于浏览端的优势而倾斜。

然而，使用 JavaScript 等浏览器技术意味着每当语言进行升级时，解释器（位于浏览器中）也必须随之升级。

服务器技术没有这个问题；当语言的新版本在服务器端可用时，浏览器仍然可以处理该技术的输出，因为该技术并不依赖浏览器的智能性。

那么，哪种更好，你想用哪种？答案取决于你的需求。每种方法都有优缺点，你甚至可能需要同时使用两者来实现你的特定目标。由于这本书是关于 Perl 的，并且专门针对运行在服务器上的程序，我们将几乎完全专注于服务器端编程。

## 服务器端程序的优势

- 与客户端程序不同，服务器端程序将始终运行。旧版浏览器不支持许多基于浏览器的程序（如 JavaScript），而较新的浏览器允许你禁用基于浏览器的程序。使用服务器端程序时无需担心这一点，因为它们运行在服务器上，且独立于浏览器。
- 服务器端程序允许你读写数据库或服务器上的本地文件。通过服务器端程序，你可以保存访问信息、查询数据库并创建自定义页面等活动。浏览器端程序不允许此类应用。

可能意义重大，基于浏览器的技术依赖于特定的浏览器和特定的浏览器版本才能良好运行——如果浏览器根本支持这些技术的话。

这造成了当今设计师面临的最大挑战：如何让网站在不同平台、浏览器和浏览器版本之间既有趣又具有一致性。因此，许多专业人士正回归服务器，以提供满足今日网站需求所需的稳定性。

## Perl 和 CGI

本书中的大多数脚本都设计为在服务器上作为 CGI（或“CGI”）运行。CGI 全称为通用网关接口，不是像 Perl 那样的语言；它是 Web 服务器与应用程序或脚本交互的协议。CGI 是为网站添加交互性最老、最广泛的方法，可以使用任何语言编写脚本。关于 CGI 如何传递信息的技术细节在这里不需要深入探讨。需要记住点是，CGI 与静态页面或图像不同，它是每次用户请求运行的程序。它从 Web 服务器接收用户输入（或浏览器发送）的所有表单输入和 Cookie，程序的输出返回到 Web 服务器，就像 HTML 页面的内容一样。与静态页面不同，返回的内容对于每个用户或每次 CGI 请求都可能是不同的。

![](img/d26997dc0c0571017b4729525ba1a4ac_17_0.png)

## CGI 资源

如果你想了解更多关于 CGI 的知识，可以使用这些精选的 CGI 网站。

通用网关接口概述：

- [http://hoohoo.ncsa.uiuc.edu/cgi/intro.html](简介)
- [http://hoohoo.ncsa.uiuc.edu/cgi/primer.html](入门)

CGI City

- [http://www.icthus.net/CGI-City/references.shtml](参考)
- [http://www.icthus.net/CGI-City/books.shtml](书籍)

CGI Resources

- [http://www.cgi-resources.com/Documentation/](教程和帮助)
- [http://www.cgi-resources.com/Books/](书籍)
- [http://www.cgi-resources.com/Magazine_Articles/](杂志文章)

图 1.3

此表单使用 Perl 处理。

![](img/d26997dc0c0571017b4729525ba1a4ac_18_0.png)

Perl 是唯一可以用于 CGI 的语言吗？答案是否定的。其他语言（如 C）也用于 CGI 管道的末端。然而，Perl 仍然是用于此目的最灵活、易用且常用的语言。

## 内容预告

表单可能是 Perl 在 Web 上最常见的使用方式，但 Perl 的功能远不止管理表单。让我们来看看从这本书中你将学到的各种内容，以让 Perl 为你所用。

## 功能与特性

请参阅第 4 章“处理表单”，了解如何使用 Perl 为你的网页设置各种功能性且美观的表单。

为了帮助你更有效地管理脚本和网站，我们为你提供了一些非常有用的工具。你将找到帮助管理网站上其他脚本的脚本、在后台重命名文件的实用程序、检查链接、修复 Bug 以及验证代码的工具。

## 自定义网站

Perl 可以帮助 Web 设计师为网站访问者看到的页面添加一系列定制化功能。

Perl 允许你创建时间戳。这对于问候访问者以及让你的页面看起来活跃新鲜非常有帮助。

你很可能在网页上看到过“页面最后更新于 . . .”这样的注释。这也可以通过 Perl 脚本实现，并能让读者意识到网站的实效性。

你可以在第 5 章“功能与特性”中找到网站管理工具的脚本。

Cookie 在帮助用户跟踪浏览器中的活动方面起着巨大的作用。我们将向你介绍一种简单的 Cookie，并向你展示如何使用它来创建一个自定义的访客簿。

许多定制化依赖于浏览器检测和路由，我们将在第 6 章“自定义页面”中教你如何使用 CGI 和 Perl 实现。

你是否希望在每个访问者进入你的网页时，从列表中随机选择并显示不同的图形？通过基于时间的函数，这将呈现出定制材料的效果。此外，这种效果可以极具创意地使用，为你的访问者提供趣味或引人的特效。随机化可以使用服务器包含来实现。我们已将这些技术及相关问题都添加了第 6 章。

## 趣味内容

无疑，Web 过去是一个工具，未来可能永远是一个工具。我们使用它有很多原因，但老实说，如果 Web 不好玩，我们真的会在那里吗？Web 的魅力不仅在于购物和信息的便利性。我们玩得很快乐！

如果你想为你的网站访问者创造一些休息和放松的空间，我们将教你如何在页面上添加诸如投票和互动故事等趣味内容。只需查阅第 7 章“趣味与游戏”获取所需的脚本和修改方法。

## 使用 Perl 发布整个网站

发布整个网站并不是一项小任务，这就是为什么它占了整整两个章节的原因！我们首先教你如何使用模板，然后向你展示如何使用 Perl 实际管理并发布完整的、可定制的网站。我们从第 8 章“使用模板设计”开始，并将这一概念贯到第 9 章“创建你自己的门户”。

## 管理网站

在第 10 章“网站发布向导”中，我们将汇编工具箱，允许你通过浏览器管理你的工具。这将让你拥有发布内容的能力，而无需担心安装和组织内容的细节。

## 学习 Perl

虽然本书的大部分重点是让你快速轻松地使用 Perl，但我们确实希望能够激励你们中的人继续探索 Perl 这一门语言。为此，我们包含了一个关于 Perl 基础的章节。第 11 章“准备学习 Perl”将为那些有兴趣编写自己的自定义脚本的人提供帮助。

## 接下来是什么

你现在应该清楚地知道 Perl 是什么，它与 CGI 有什么关系，以及它在 Web 上是如何工作的。在第 2 章“准备使用 Perl 进行设计”中，我们将准备好处理《Perl 网站工作坊》中脚本所需的技能和工具。

# 章节：准备使用 Perl 进行设计

在了解了 Perl 是什么，并大致知道你可以如何使用它来增强你的网站之后，是时候确保你拥有处理书中脚本所需的知识和软件了。在本章中，我们将告诉你你将需要哪些技能以及想要拥有哪些工具。然后，我们将提供一些可以向你的互联网服务提供商（ISP）的问题，以便确保你的服务器和账户已配置好支持 CGI 和 Perl。

本书的读者无疑来自不同的背景。你们中的某些人具有编程经验，主要通过书中包含的脚本和各种技巧来学习。你们中的某些人是全职设计师，每天没有足够的时间投入到学习编程，但又希望将编程的力量应用到你的网站上。

由于大多数读者来自不同的背景，我们将确保信息对所有人来说都是清晰的。

## HTML

大多数人可能熟悉 HTML，已经知道 HTML 意味着超文本标记语言。它允许你创建网页。对于我们的目的，HTML 主要用于构建页面内容。

如果你不熟悉 HTML，不用担心！我们将带你了解基础知识。我们将教你如何使用基础标签，然后教你如何使用所见即所得（WYSIWYG）工具，如 FrontPage 和 Adobe。

## Unix

如果你不熟悉 Unix，不用担心！我们将带你了解基础知识。我们将教你如何使用基础命令，然后教你如何在命令行界面导航文件。

## FTP

大多数人可能熟悉 FTP，已经知道 FTP 意味着文件传输协议。它允许计算机之间传输文件。对于我们的目的，FTP 主要用于将脚本从工作站移动到它们所在的 Web 服务器。

## Perl

## Telnet

我们将在第 3 章“脚本基础”中指导你如何通过 Telnet 连接编辑文件。

Telnet 允许你登录 shell 账户，从那里你可以访问你的 Web 服务器。从那里，你可以在服务器上编辑文件、在命令行测试你的 Perl 脚本，或者移动、复制和删除文件。

# HTML 和 Web 设计教程

嗯，这些资源多到我们几乎无法告诉你该去哪里，但我们为你列出了一些我们最喜欢的。

- Web Review 提供最新的设计和开发者工具、活动、资源以及行业领袖的智栏：http://www.webview.com
- Builder.Com 是 C|NET 的开发者中心，拥有许多关于 HTML 的精彩文章：http://www.builder.com
- WebDeveloper.Com 为 Web 开发者提供优质、最新的文章和参考：http://www.webdeveloper.com
- 世界维网联盟（W3C）是标准协会，拥有关于当前和历史版本的 HTML 教程、常见问题和资源：http://w3c.org/
- Ziff-Davis 提供从开发者工具到在线教育的各种服务。尝试访问 http://www.devhead.com 文章和脚本存档，访问 http://www.zdu.com 获取讲师课程和在线教程。

# Unix 帮助

这是一个非常广泛的领域，但我们挑选了几处精选之作：

- [Unix FAQ]。从 Usenet 收集的问题与问答，http://www.cis.ohio-state.edu/hypertext/usenet/unix-faq/top.html
- [面向用户的 UNIX 帮助]。这是一个优秀的初学者资源，组织良好且信息详尽，http://www.geek-girl.com/Unixhelp/
- [FTP FAQ]。关于 FTP、软件和通用 FTP 主题的概述，http://nohoo.nsca.uiuc.edu/ftp.html
- [Telnet FAQ]。这篇关于 Telnet 的非常有帮助的概述提供了软件下载和其他资源的链接，http://mist.cit.cornell.edu/telnet

# 你需要的工具

如果你为某项工作没有合适的工具，那么这项工作肯定会花费更长的时间并导致更多的挫败感。幸运的是，让你充分利用本书价值所需的工具非常简单。而且，与你可能考虑送给心爱的多能手手的礼物不同，我们讨论和推荐的工具要么非常便宜，要么完全免费。

# ASCII 文本编辑器

ASCII 文本编辑器简单来说就是一个纯文本处理器。你将使用它来编辑后续章节中的 Perl 脚本和 HTML 文件。

你可以使用任何你喜欢的文本编辑器，只要它符合 ASCII 标准。这意味着编辑器必须有一个将文本保存为原始、未格式化文本的选项。

让我们按平台来看一些我们发现的特别实用的 ASCII 编辑器。

> 尽管像 Microsoft Word 或 WordPerfect 这样的文字处理器提供了仅文本的保存选项，你不应该使用它们。在你的文件中引入额外或不可读字符的潜在风险很高。我们建议避免使用文字处理器，坚持使用简单的 ASCII 编辑器。

# Windows

对于 Windows 用户，我们推荐 Windows 记事本（Notepad）或 Allaire 的 HomeSite。

Notepad 带有所有版本的 Windows，可以在你的硬盘上找到。Windows 95 或以上版本的用户只需点击“开始”按钮，选择“运行”，然后输入 `notepad`。这是一个非常简单的编辑器，界面上几乎没有令人困惑的命令或额外功能。你只需开始输入，并在准备好时保存文本即可。

Allaire 的 HomeSite 是一个强大的编辑器，主要用于处理 HTML 文档。然而，由于该编辑器符合 ASCII 标准，它也可以轻松地用于 Perl 脚本以及 HTML。对于那些希望在编辑界面中使用一些强大工具的人来说，HomeSite 将特别好有用。

# Macintosh

Macintosh 用户应该考虑使用 SimpleText 或 BBEdit。

与 Windows 记事本一样，SimpleText 是 Macintosh 操作系统的一个纯文本编辑器。它易于访问且方便使用。

BBEdit（Bare Bones Edit 的缩写）与 Allaire 的 HomeSite 类似，因为它主要是 HTML 编辑器。它将吸引那些希望将 HTML 工具集成到界面中的个人，而符合 ASCII 的格式可以在不带格式代码的情况下保存信息。

## Unix

对于 Unix，我们推荐 `vi` 或 `pico`。这两个编辑器都可以通过在 Unix 命令行提示符中输入 `vi` 或 `pico` 来启用。

对于 Unix 相对新手来说，`pico` 是一个很好的开始点。它看起来非常像 pine，一个流行的 Unix 电子邮件程序。命令位于界面窗口的底部，方便访问。

`vi` 被广泛使用，特别是对于程序员。它有一个使用模式（命令模式和插入模式）运行的界面，并依赖于个人使用键盘，而不是使用按键组合或鼠标来操作界面。它通常是基于 Unix 的系统上的默认可视化编辑器。见图 2.1。

图 2.1

在 `vi` 中编辑 Perl。

![](img/d26997dc0c0571017b4729525ba1a4ac_27_0.png)

# 如何获取 ASCII 编辑器

提到的许多编辑器在你的操作系统中可用。

尝试这些网站以获取更多非驻留编辑器的信息：

- HomeSite: http://www.macromedia.com/
- BBEdit: http://www.barebones.com/

在使用驻留编辑器时需要支持，请尝试这些 FAQ：

- `vi` FAQ：http://www.uni-konstanz.de/misc/faqs/Computer/msg000097.html
- `pico` 教程：http://www.ncsu.edu/ncsu/cc/pub/tutorials/pico_tutorial/pico_intro.html

# FTP 客户端

FTP 客户端是一种允许你通过互联网从一台计算机传输文件到另一台计算机的软件程序。在本节中，我们将讨论对软件的建议。

# Windows

大多数具有大量文件传输经验的 Windows 用户倾向于使用名为 WinFTP 的程序（见图 2.2）。

这个程序 WinFTP 价格实惠且物有所值。它非常灵活且可定制，并有一个易于使用的界面。

图 2.2

使用 WinFTP 传输文件。

![](img/d26997dc0c0571017b4729525ba1a4ac_28_0.png)

# Macintosh

对于 Mac，我们推荐 Fetch。这是一个有趣、易用的程序，并且免费提供。商业用户必须购买许可，但 Fetch 允许你通过点击或拖放文件来待传输（Fetch 2.3）。

# 寻找 FTP 客户端

你可以在以下网站下载和购买推荐的 FTP 客户端：

- WinFTP: http://www.winftp.com/
- Fetch: http://www.dartmouth.edu/pages/fetch.html

## Unix

对于 Unix，我们推荐的 FTP 客户端是内置的。

# Telnet 客户端

如果你的操作系统中提供 Telnet 客户端，你就可以使用它。

# Windows

Windows 自带一个名为 Telnet 的程序。你可以点击“开始”按钮，选择“运行”，然后输入 `telnet` 来使用它。这个 Telnet 程序非常强大。

# Macintosh

对于那些想要完全自定义的用户，请尝试 Eric's Telnet。（见图 2.4。）

图 2.4

使用 Telnet 访问账户。

![](img/d26997dc0c0571017b4729525ba1a4ac_30_0.png)

# 如何获取 Telnet 客户端

如果你的操作系统中没有 Telnet 客户端，请使用这些链接找到相应的软件：

- 你是否被允许从你的 Web 账户运行自己的 CGI 程序和 Perl 脚本？这是一个关键问题。某些互联网服务提供商（ISP）提供 CGI，但他们只允许你访问由他们提供的脚本。你必须能够添加自己的 Perl 脚本，才能完成《Perl 网站工作坊》中提供的功能。

对于你的 ISP，通常的原则是不接受用户运行的脚本，那么是否有方法可以提交脚本进行审核呢？如果你专门要求他们批准某个脚本，某些 ISP 在此问题上会比较灵活。但这并不是理想的情况，因为你必须让你的 ISP 运行每一处更改和新脚本，这可能会让你感到沮丧！我们认为更好的选择是寻找一个包容度更高的 ISP。

- 系统中是否安装了 Perl？如果是，是哪个版本的 Perl？在编写时，当前的 Perl 版本是 5.6.1。
- Perl 位于你系统的什么位置？具体来说，你需要 Perl 所在的路径。路径看起来非常像这样：`/usr/bin/perl`。书中的所有脚本都需要特定的路径信息。
- 系统中是否安装了任何额外的 Perl 模块？如果是，它们是什么以及位于什么路径？Perl 模块是函数（微程序）的集合。
- 你的 CGI 程序将位于何处，它们是否需要特定的扩展名？通常情况下，大多数 ISP 为 CGI 程序创建一个特定的目录，例如 `/cgi-bin` 或 `/htbin`。然而，某些 ISP 允许将它们放置在任何地方。CGI 的标准扩展名是 `.cgi`，Perl 是 `.pl`。根据服务器的设置，你还需要用特定的扩展名命名你的 CGI 程序。

我们准备了一份实用的表格，你可以它来识别你的 ISP 提供哪些服务。在阅读这本书的过程中，该表格也将为你提供帮助。

## 继续后续

| 服务器信息表单 | 你的 CGI 环境 |
| :--- | :--- |
| Web 服务器: | Web 服务器操作系统: |
| Perl 版本: | |
| Perl 路径: | |
| 额外的 Perl 模块及其路径: | |
| 1. | |
| 2. | |
| 3. | |
| 其他: | |
| CGI 程序的扩展名: | |
| 在你的 Web 服务器上放置 CGI 程序的位置 (路径): | |

到此为止，你应该对将所需的技能、工具和服务器访问权限有了清晰的认识。太棒了！我们准备好开始实际操作脚本了，查看选择脚本的指南，学习如何将它们放置在服务器上、测试脚本并进行修改。

## 章节：脚本基础

在我们深入处理 Perl 脚本之前，有一些你需要了解的基本概念。首先，最好确认一下你将使用的服务器上是否安装了 Perl——如果安装了，安装的是哪个版本的 Perl。

在整本书中，你将使用多种类型的文件。其中一些文件类型可能对你来说很熟悉，而另一些对你来说是全新的。我们将涵盖这些文件类型是什么、如何命名它们，以及为了正确使用它们对这些文件类型所需的任何自定义或约定。

一旦你确定 Perl 已正确安装，并理解了你将要使用的各种文件类型，设置文件目录是非常重要的。如果你还不习惯于这样做——特别是在被称为 Unix 的非图形界面环境中——我们鼓励你进行一些练习。创建文件，删除它们，再次创建，直到你掌握它为止。

文件权限在书中的各种脚本中起着至关重要的作用。如果你设置文件权限不当，可能会导致脚本运行错误或根本无法运行。我们将帮助你理解如何设置文件权限并恰当地使用它们。

综合 Perl 归档网络（CPAN）是一个在线资源，在你阅读这本书以及继续学习 Perl 的过程中，对你将是无价的。我们将讨论它的作用、在哪里可以找到它，以及使其成为任何 Perl 用户工具箱不可或缺部分的特性。

最后，由于 Perl 经常与 Unix 联系在一起，我们将提供一些 Unix 资源和网站地址，以帮助你更多地了解 Unix、它是什么以及如何有效地使用它。

### 在你的服务器上检查 Perl

让我们先查看服务器上是否存在 Perl，如果是，运行的是哪个版本。要做到这一点，请使用 Telnet 连接到你的服务器或 ISP 账户，并在命令行提示符输入 `perl -v`。服务器上存在的 Perl 版本将会显示（见图 3.1）。

```
molly@envy:~/usr/home/molly$ perl -v
This is perl, version 5.005_0 built for i386-freebsd
Copyright 1997-1998, Larry Wall
Perl may be copied only under the terms of either the Artistic License or the GNU General Public License, which may be found in the Perl 5.0 source kit.
Complete documentation for Perl, including FAQ lists, should be found on
this site using 'man perl' or 'perldoc perl'. If you have access to the
Internet, point your browser at http://www.perl.com/, the Perl Home Page.
molly@envy:~/usr/home/molly$
```

截至本文写作，最新的 Perl 版本是 5.6.1。Perl 5.005 在某些情况下是可以的，但如果你发现服务器上的版本较旧，你应该考虑升级，或者要求你的服务器管理员为你升级。

如果你想获得最新的稳定版本，请访问 http://www.perl.com 并按照那里的说明升级服务器上的 Perl 软件。

### 理解文件类型

在开发过程中，你会遇到许多类型的文件。在本节中，我们将重点介绍你在本书中专门使用的类型。我们将告知该文件类型建议的权限，并让你了解某些文件为了书中脚本正确运行而已经存在或应该放置的位置。

### .pl

这是 Perl 脚本的文件扩展名。Perl 文件从命令行运行，或通过其他操作（见下一节）调用。Perl 文件对所有者可执行——我们将在后的“设置文件权限”章节中介绍如何这样做。Perl 文件也必须可读。

### .cgi

这些是通用网关接口（CGI）脚本文件。网站访问者可以通过 HTML 页面直接访问这些文件。这些文件对所有用户可见，对所有者写。

### .pm

Perl 模块是代码库，可以包含 `.pl` 脚本中以定义面向对象编程的类。随 Perl 提供的模块通常位于 `/lib/perl` 目录。与 Perl 文件不同，Perl 模块文件不是执行脚本，除了可读外不需要任何特殊权限。

### .html, .htm

这些是 HTML 文件，在大多数情况下是公开访问的。注意我们使用的是 `.html` 扩展名。`.htm` 扩展名是微软早期对文件后缀限制的结果。虽然你可以根据服务器的配置使用任何一种，但除非你的系统管理员要求你这样做，否则我们建议坚持使用 `.html`。

如果你想将某些 CGI 脚本放在 `cgi-bin` 以外的目录中，你就需要配置 Web 服务器以识别所有以 `.cgi` 脚本结尾的文件。

如果你使用的是 Apache，可以通过在 `httpd.conf` 中添加以下行来实现：

```apacheconf
AddHandler cgi-script .cgi
```

## 设置 Perl 脚本目录

不要将命令行 Perl 脚本放在你的 `cgi-bin` 目录中。如果这样做，你会让你的服务器暴露在危险的黑客活动面前。请考虑安全！

CGI 脚本只是 Perl 在 Web 端应用的一半。Perl 在后端也极其有用，在本书中，有几个实用工具脚本，你可以在服务器上从命令行运行它们。

实用工具脚本的一个良好选择是你主目录下的 `bin` 目录。如果你拥有 root 权限，也可以选择将脚本放在 `/usr/local/bin`。因为许多其他软件也安装在那里，在大量程序中翻找你自己的程序可能会很困惑。因此，我们建议使用主目录或 root 目录下的子目录 `~`。

## 创建 Perl 模块库

如果你拥有 root 权限，将你所有的模块放在预存在的 `/usr/lib/perl/site_perl` 中。

Perl 库是你存放根据我们的示例自行创建的模块，以及你安装的任何外部模块的地方。

如果你没有 root 权限，或者不想将模块放在 `site_perl` 中，你就需要创建一个 Perl 库目录。

如果你的 Web 文档根目录是 `/home/htdocs/www`，那么此的一个良好选择是 `/home/htdocs/lib/perl`。

## 设置文件权限

你需要学习一些命令和概念，它们将帮助保持你的网站的安全，并让你能够允许访问者在访问你的网站时执行完全（且仅限于）你希望他们执行的操作。

如果你对 Unix 不熟悉，本节的信息起初可能看起来很困惑。但请耐心——我们在带你了解脚本的过程中会逐步演示如何操作，这样你就能掌握它。但我们仍然认为这里的背景知识非常重要。

如需更多关于 Unix 的帮助，请参见本章末尾的资源列表。

Unix 是一个多用户操作系统，因此它内置了文件“所有者”的概念。通常，所有者是文件的创建者。

由于 Unix 设计之初是为了允许多个用户（他们可能互不认识或不信任）在同一台计算机上工作，因此它还包含了文件“权限”的概念，这允许你决定谁可以对你的文件做什么。

## chmod

改变模式（Change mode），或 `chmod` 是你用于更改文件权限（或模式）的命令。除非你有 root 权限，否则你只能对你拥有的文件使用它。

在命令行，你使用 `chmod mode filename`，其中 `mode` 是你想要赋予的权限的数字或符号设置，`filename` 是你要设置权限的文件名。

数字模式是三位或四位的八进制（基 8）数字，例如 `0640` 或 `755`。从左起第一个数字（如果存在）设置特殊位，使文件执行 SID 或 SGID（设置用户 ID 和组 ID）。第二位设置文件所有者的权限，第三位设置所属组的权限，最后一位设置所有其他用户的权限。这些数字是三位的组合，值为 4、2 和 1。如果数字中包含 4，你可以读取文件。如果包含 2，他可以写入（并删除）文件。如果包含 1，她可以将其作为程序执行。

例如，`chmod 777 file.pl` 赋予所有用户该文件的权限。`chmod 744 filename` 意味着所有者可以读取、写入和执行，其他人只能读取。`chmod 755 filename`（你将在 CGI 脚本中使用的模式）意味着所有者可以进行任何操作，而所有其他用户只能读取和执行该文件。

`u+x` 意味着用户执行，这是一种允许用户执行程序的符号方式。同样，`a+x` 意味着任何人执行，字面上意思是任何人都可以执行该程序。

对于大多数初学者来说，使用符号设置模式比处理八进制数字更容易。符号模式的格式为 `[user][+][permission]`。例如，符号设置可以输入 `chmod u+x`（见图 3.2）。这允许所有者执行文件；`chmod a+x filename` 允许任何人写入文件；`chmod g-w filename` 从所属组中撤销权限。

我们在书中将符号过程，但如果你想使用数字方法，请尽管使用——只需确保你设置的文件具有适当的权限即可！

图 3.2

使用符号方法更改模式。

```
molly@envy:~/usr/home/molly/public_html/cgi-bin$ ls
better_cgi.cgi* guestbook_2.cgi*
browser_detect.cgi* First_Func.cgi* magic_soothsayer.cgi*
browser_detect.cgi* guest_1.cgi* mail_form.cgi*
clock.cgi* guest_cgi* mail1.cgi*
echo_date.cgi* guestbook_1.cgi*
first.cgi*
```

## Perl CPAN Web 工作坊

图 3.4

CPAN 是你获取模块和其他有用 Perl 文件的一站商店。

![](img/d26997dc0c0571017b4729525ba1a4ac_42_0.png)

CPAN 包含了整个 Perl 社区的智慧；数百个 Perl 模块；价值连城的文档，以及整个 Perl 分发包。如果它是用 Perl 编写的，它是有用的并且在 CPAN 中。

CPAN 架构由 James Pearce 和 Andreas KG 创建，并由 Tim Bun 慷慨维护 Meta（即 Perl 模块列表），它就像本文一样，包含更多关于创建模块的内容，而关于模块作用的内容较少。

本文文档是 CPAN，它是 CPAN 的一个“前读”：文档的这部分是关于 CPAN 中包含的内容，以及你如何通过提交你的成果供世界其他地方来贡献这个世界。但文档的这部分是关于 CPAN 模块：你可以将你的模块添加到 CPAN 中，或者想更改这些描述之一，请联系我 Owen。我是 Perl 社区的一员，如果你对你的模块感兴趣，我希望看到它出现在“新模块”列中。如果你只想安装 Perl，CPAN 可以从 CPAN 分发中获取。

### 什么是模块？

你可以在 Perl 文档中找到技术描述，但这里有一个免费提供的 Perl 5 实用程序，你可以从你的 Perl 5 程序中下载并使用它。许多模块是以 `.pm` 结尾的单个 Perl 文件，需要在你的机器上进行考虑，然而，因为它们使用了

## 从 CPAN 获取模块

你可以使用通常的 Web 或 FTP 客户端从 CPAN 获取模块，搜索模块列表，并按名称、作者和类别进行浏览。

一旦你找到了需要的模块，请使用你的浏览器或 FTP 客户端将文件传输到你的服务器，或者传输到你的家/办公室机器然后再传输到你的服务器——取决于你的设置。

## 使用 CPAN 模块从 CPAN 获取模块

你也可以使用 `CPAN.pm` Perl 模块来让从 CPAN 安装其他模块变得简单得多。在较新版本的 Perl 中，此模块是默认安装的——如果没有，你将需要自己下载并安装它。一旦你获取并安装了 CPAN 模块和 libnet set（一个非常有用的 Perl 模块包），你就可以轻松地安装额外的模块。方法如下：

1. 从 http://www.perl.com/CPAN/modules/by-module/CPAN/CPAN-1.57.tar.gz 下载 CPAN 模块并将文件保存到你的计算机上。

如果你正在安装到标准位置，你必须是 root 用户（或拥有 `/usr/lib/perl/5` 的写入权限）。读取 CPAN-1.57 中包含的 README 文件获取更多信息，或者直接在命令提示符上输入 `perldoc CPAN`。

2. 输入 `cd name_of_directory tar -zxvf CPAN-1.57.tar.gz` 解压文件。
3. 进入你创建的新目录，`cd CPAN-1.57`
4. 在命令提示符上输入 `perl Makefile.PL [Lib=/path/to/private/library]` 构建模块。
5. 如果你对手动配置回答“no”，该模块将尝试自动配置其设置。
6. 在命令提示符上输入 `make` 构建模块。
7. 在命令提示符上输入 `make test` 测试模块。
8. 在提示符上输入 `make install` 安装模块。

安装其他模块非常简单，只需输入 `perl MCPAN -e shell` 进入 CPAN shell，然后从那里执行 `install [module]`。例如，使用此系统安装 `FastTemplate` 模块（你将在第 8 章“设计模板”中使用它），你将在 cpan 命令提示符上输入 `install c::FastTemplate`。CPAN 模块将自动下载、构建并安装命名模块的最新版本。

## 手动安装模块

要手动安装 Perl 模块，请遵循此过程：

1. 将模块下载到你的构建目录。这是你构建下载的脚本/模块的目录，而不是库目录（库目录是它们在构建完成后安装所在的地方）。
2. 使用 `tar -zxf filename` 解压（如果你有 GNU tar）或使用 `gunzip filename | tar -xf` 解压（如果没有的话）。如果你运行 Linux，就有 GNU tar。
3. 输入 `cd`（切换目录）进入新创建模块目录。
4. 在命令行按顺序输入这些命令：

如果你将安装到默认位置，在安装步骤中需要 root 权限。如果你不是 root，则无法安装到默认位置，因此你将其安装到非标准位置，并在 `perl Makefile.PL` 行中添加 `LIB=/path/to/library`（将 `/path/to/library` 替换为实际路径）。

```
make（这构建模块）
make test（可选——这运行模块的自测试程序，以确保模块运行正常）
make install（这安装模块）
```

## Unix 资源

由于许多读者对 Unix 环境不熟悉，我们为你提供了这些推荐资源。

- **Unix in a Nutshell**，作者 Daniel G. 著。这本书是任何使用 Unix 者的必读之书。
- **A Basic Unix Tutorial**。该网站引导你完成登录和注销。
- **The Reference Desk**。该网站是一个详尽的信息中心，包含了所有关于 Unix 的链接。

## 接下来

你已经掌握了基础知识并准备好了工具。现在是深呼吸并准备开始编写了！不要担心，我们会从轻松开始。第 4 章“处理表单”将包含大量的

### 处理表单

表单通过结合标准 HTML 和关联脚本来工作。HTML 用于创建表单元素，如文本字段、复选框、单选按钮、提交和重置按钮。HTML 还包含了提交时传递到服务器的信息。此时，CGI 接管，并将输入数据引入脚本进行处理。

在本章中，我们将查看幕后处理。我们将从简单的脚本开始，然后向你展示如何让表单和生成的脚本变得更复杂、更实用。

在学习表单之前，我们想指出后续脚本中一些基本编程规范。这有助于你熟悉脚本内容。

### 编程基础

此脚本使用面向对象的接口处理 CGI。`CGI.pm` 是一个 Perl 模块，通过读取 CGI 输入并输出 HTML 页面为 Perl 程序员提供 CGI 脚本。CGI 包含在标准分发中。你可以轻松地检查是否拥有它：在命令行输入 `perldoc CGI`；如果你看到了文档，说明你拥有它，如果没有，你可以从 CPAN 下载。

```
# 这是一个注释。使用注释来解释你在代码的任何一点正在做什么。
;
{}
```

分号表示代码行的结束。括号表示代码组。

这些表示变量。我们将在第 11 章“学习 Perl”中详细讨论这些。

### 简单的网关脚本

此脚本是一个非常简单的脚本，它可以显示表单，或者将表单输入回显到一个简单页面。该脚本是自包含的，这意味着你不需要创建一个带有输入字段的 HTML 表单即可使其运行。然而，你将创建一个 HTML 页面来访问它。

## 如何使用

1. 将脚本复制到文本编辑器中。
2. 将脚本保存为 `first.cgi`。
3. 将表单放在服务器的 `cgi-bin` 目录中。
4. 修改权限以允许所有用户执行：

```
chmod a+x first.cgi
```

```perl
first.cgi

#!/usr/bin/perl -w

use CGI;           # 导入 CGI.pm 

$q = new CGI;      # 创建一个新的 CGI 对象 $q，
                    # 它将自动读取
                    #任何输入并对其进行格式化
                    # 以便访问。

$self = $q->url;    # 获取自己的 url

## 通过打印标准的
## HTTP 头 (Content-type: text/html) 开始页面
print $q->header;
## 如果我们获取了一些输入，则显示结果页面
## 否则，显示输入表单。
if ($q->param('name')) {
    # 通过将首字母大写让名字看起来更好看
    $name = ucfirst($q->param('name'));
}

## 这是一个“此处文档”(here document)：直到指定的
## 标签（在本例中为 'HTML'）之前的所有内容都会被打印。结束 HTML 标签必须是该行的第一个单词。
print <<HTML;
<html>
<head>
<title>我的第一个 CGI</title>
</head>
HTML
```

```perl
first.cgi (续接)

<body>
<h1>我的第一个 CGI</h1>
<p>你好, $name! 这是我的第一个 CGI！</p>
</body>
</html>
HTML
} else {
## 另一个“此处文档”……注意
## 在一个脚本中有两个具有相同
## 标签的文档不是个好主意。
print <<FORM;
<html>
<head>
<title>你叫什么名字？</title>
</head>
<body>
<h1>你叫什么名字？</h1>
<form action="$self" method="post">
<p>你的名字：<input type="text" name="name"></p>
<p><input type="submit"></p>
</form>
</body>
</html>
FORM
}
```

## 需要的其他文件

你可能想要创建一个简单的 HTML 文件，这样就可以看到脚本的运行。如下：

1. 打开你的文本编辑器。
2. 创建一个指向 `first.cgi` 的标准 HTML 文档。
3. 将文件保存为 `first.html`。
4. 将 HTML 上传到服务器上相应的目录。

```html
first.html

<html>
<head>
<title>简单 CGI 脚本</title>
</head>
<body>
<p>
<br/>
<br/>
</p>
<div align="center">
<a href="cgi-bin/first.cgi">简单 CGI 脚本测试</a>
</div>
</body>
</html>
```

一旦将 HTML 文件加载到服务器，即可使用浏览器测试该文件。在图 4.1 中，我们点击了脚本测试的链接，脚本开始运行并为我们提供了输入表单。

![](img/d26997dc0c0571017b4729525ba1a4ac_49_0.png)

继续输入你的名字并点击提交按钮，结果将是一个定制化的欢迎信息（见图 4.2）。

图 4.2

表单结果。

![](img/d26997dc0c0571017b4729525ba1a4ac_50_0.png)

## 修改脚本

最简单且明显的修改是根据喜好格式化 HTML 输出。要实现这一点，只需修改脚本中的 HTML。我将背景色设置为黑色，文字设置为奶油色。受影响的行已加粗。

```perl
first_example.cgi

#!/usr/bin/perl -w

use CGI;           # 导入 CGI

$q = new CGI;      # 创建一个新的 CGI 对象
$self = $q->url;   # 获取自己的 url

## 通过打印标准的
## HTTP 头 ('Content-type: text/html') 开始页面
print $q->header;

## 如果我们获取了一些输入，显示结果页面。
## 否则，显示输入表单。
if ($q->param('name')) {

# 通过将首字母大写让名字看起来更好看
$name = ucfirst($q->param('name'));
```

```perl
first_example.cgi (续接)

print <<HTML;
<html>
<head>
<title>你的第一个 CGI</title>
</head>

<body bgcolor="#000000" text="#FFFFCC">
<h1>你的第一个 CGI</h1>
<h1>你的第一个 CGI！</h1>

<p>你好, $name! 这是我的第一个 CGI！</p>

</body>
</html>
```

```perl
HTML

} else {

print <<FORM;
<html>
<head>
<title>你叫什么名字？</title>
</head>

<body bgcolor="#000000" text="#FFFFCC">
<h1>你叫什么名字？</h1>

<form action="$self" method="post">
<p>你的名字：<input type="text" name="name"></p>
<p><input type="submit"></p>
</form>
</body>
</html>
FORM
}
```

你的修改也可以更加复杂！假设你有一个聪明的主意来定制这个表单。你想在网站上放一个占卜师，访问者输入问题以获得答案。你可以通过更改其中的 HTML 来自定义表单。在这种情况下，标题、背景颜色、文字颜色和输入字段都经过了自定义。注意我们在 input type 中添加了 value，这允许我们个性化提交按钮。

## 自定义输入

```html
<head>
  <title>玛利的魔法占卜师</title>
</head>

<body background="../images/soothsayer_bak.gif" bgcolor="#333333" text="#FFFFCC">
  <h1>你有什么问题？</h1>

  <form action="$self" method="post">
    <p>你的名字：<input type="text" name="name"></p>
    <p>你的问题：<input type="text" name="question"></p>
    <p><input type="submit" value="询问占卜师"></p>
  </form>

</body>
</html>
```

脚本完成后，输入结果将根据你的自定义显示（见图 4.3）。

图 4.3 自定义的输入。

![](img/d26997dc0c0571017b4729525ba1a4ac_52_0.png)

输出也需要进行自定义。

## 自定义输出

```html
<html>
<head>
<title>玛利的魔法占卜师</title>
</head>
<body background="../images/soothsayer_bak.gif" bgcolor="#333333" text="#FFFFCC">
  <h1>占卜师说：</h1>
  <p>你好, $name. 你的问题答案是是的！</p>
</body>
</html>
```

图 4.4 显示了输出结果。

![](img/d26997dc0c0571017b4729525ba1a4ac_53_0.png)

图 4.4 完全自定义的输出。

## 只有程序员喜欢的表单

在上一个示例中，我们使用 `CGI.pm` 模块来读取和处理来自表单的输入，但 `CGI.pm` 的功能远不止此。它包含的一些实用函数包括 HTML 快捷，你可以使用它们生成 CGI 输出而无需手动编写任何 HTML。

`CGI.pm` 允许你以不同的方式使用它的函数。如果你熟悉面向对象的编程，可以使用对象接口，就像我们在书中的大多数示例中所做的那样。如果你是刚开始，函数接口可能更容易上手。虽然它的灵活性较低，但需要记忆的内容也更少。这对于简化代码并使编码过程更加快速高效特别有利。

在接下来的示例中，我们演示了如何使用函数接口的快捷方式。

## 如何使用

1. 将脚本复制到文本编辑器中。
2. 将脚本保存为 `second.cgi`。
3. 将脚本放在 `cgi-bin` 目录中。
4. 修改权限以允许所有用户执行：

```
chmod a+x second.cgi
```

使用对象接口，代码看起来像这样：

```perl
second.cgi
#!/usr/bin/perl -w

use CGI;

$q = new CGI;

## 如果我们获取了一些输入，显示结果
## 否则，显示表单
if ($q->param('name')) {

## 这里我们使用 CGI.pm HTML 快捷来构建
## 页面，而不是手动编码 HTML。

print $q->header;
$q->start_html('我的第一个 CGI');

$q->h1('我的第一个 CGI');
$q->p('你好, ' . ucfirst($q->param('name')) . '! 这是我的第一个 CGI！');
$q->end_html();
} else {

    print $q->header;
    $q->start_html("你叫什么名字？");
    $q->h1("你叫什么名字？");

$q->start_form;

## 创建一个指向回我们的
## 表单
$q->p('你的名字：');
$q->textfield('name');
## <input type='text' ...
$q->p($q->submit);
$q->end_form();
$q->end_html();
}
```

此脚本为你创建了 HTML，当你使用它时不需要任何额外的 HTML 文件。

```perl
better.cgi

#!/usr/bin/perl -wT
```

## 我们已经开启了污染检查（第一行中的 -T 选项），

## 因此我们需要显式地设置这些环境变量。

## 这是一个安全功能。

```perl
## PATH 必须不包含任何我们有权写入的目录
$ENV{'PATH'} = '/usr/bin:/usr/local/bin';
$ENV{'SHELL'} = '/bin/sh';      # 设置标准 shell
$ENV{'ENV'} = '';                # 清空 ENV
$ENV{'IFS'} = '';               # 还有 IFS，为了安全起见
```

```perl
use CGI;
```

```perl
## strict 强制你使用良好的编程习惯，例如
## 声明你所有的变量
## 它让调试变得容易得多。
use strict;
```

```perl
use vars qw($START $CGI);      # 这些是我们使用的唯一全局
## 变量
```

```perl
$CGI = "better.cgi";      # 脚本名称
```

```perl
## 我们使用 eval 来捕获可能发生的错误
# 并将 $START 设置为代码的实际开始位置
eval { main() }; $START = $@;
```

```perl
## 如果 eval { main() } 产生了错误，
## 特殊变量 $@ 将
## 持有错误信息。
if ($@) {
  chomp($@);                   # 从 $@ 中删除多余的条目
```

```perl
## 使用 $START 来确定发生错误的
## 真实行——这是 Perl 最强大、
## 也最难读的特性之一。
$@ =~ s/\(eval\) line (\d+)/$CGI . " line " . ($START - $1)/e;
$@ =~ s/ at .* line \d+\.$/$CGI/;
```

```perl
my $error_message = $@;
```

```perl
print <<ERR;
Content-type: text/html
```

```html
<html>
<head><title>Error</title></head>
<body>
<h1>Error</h1>
<code>$error_message</code>
</body>
```

```perl
ERR
}

exit();
```

```perl
better.cgi (续)

sub main {

my ($sq,$self,$html,$name);

# 我们创建了 CGI 对象并开始页面
# 注意，在对象模式下，我们也可以使用 CGI.pm 中所有的 HTML 快捷方法，但我们必须
## 通过我们的 CGI 对象来实现。
$sq = new CGI;
$self = $sq->url;
$html = $sq->start_html("CGI: 它不再仅仅是用于早餐了！");

## 如果我们获取了一些输入，则显示结果页面。
## 否则，显示输入表单。
if ($sq->param) {
  # 确保我们获得的输入看起来正常
  $name = untaint(ucfirst($sq->param('name')));

  $html .= <<HTML;
<h1>我的第二个 CGI!</h1>
<p>你好, $name! 这是我的安全 CGI!</p>
HTML
} else {
  $html .= <<FORM;
<h1>你叫什么名字?</h1>

<form action="$self" method="post">
<p>你的名字：<input type="text" name="name"></p>
<p><input type="submit"/></p>
</form>
FORM
}

$html .= $sq->end_html;
print $html;
}

## 其他子程序

## untaint
## 输入: 不可信的标量
```

```perl
better.cgi (续)

## 输出: (可信的标量，如果输入可疑则报错)
## 描述:
## untaint 使用 Perl 的正则表达式来检查可疑的
## 输入值（看起来像 shell 宏等），
## 并从任何看起来不疑的输入中移除“污染”标记，
# 这样我们就可以在危险的操作（
# 打开文件）中使用它。通过这种正则表达式
## 这样处理输入是移除其污染性的唯一方法。
sub untaint {
  my $Sval = shift;

  # 极其严格：只允许字母、数字和空格
  my $ok_chars = '[\w]';

  die "输入 \$Sval 中包含非法字符" unless
  $Sval =~ /^($ok_chars+)$/;

  return $1;
}
```

## 修改脚本

此脚本是前两个脚本的合集，同时使用了手动构建的 HTML 和 `CGI.pm` 函数。你只需按照修改第一个 `first.cgi` 脚本的方式修改此脚本。查找脚本的输入和输出部分，并自定义 HTML 和内容以满足你的需求。

# 详细介绍：关于正则表达式

在 `better.cgi` 中，我们使用了两次正则表达式，采用了两种不同的方式。第一组表达式

```perl
$@ =~ s/\(eval\) line (\d+)/$CGI . " line " . ($START - $1)/e;
$@ =~ s/ at .* line \d+\.$/$CGI/;
```

使用 Perl 的 `s///` 运算符将第二对斜杠之间的内容替换为字符串中匹配第一对表达式中（`$` 匹配正则表达式，通常称为模式）的任何部分。

在这种情况下，我们正在检查一条错误信息，它看起来可能像：

Something at (eval) line 60.

在这种情况下，我们使用 `eval` 来捕获可能发生的错误，并把 `$START` 设置为代码的实际开始位置。

```perl
eval { main() }; $START = $@;
```

如果 `eval { main() }` 产生了错误，特殊变量 `$@` 将持有错误信息。

```perl
if ($@) {
  chomp($@);                   # 从 $@ 中删除多余的条目
```

```perl
## 使用 $START 来确定发生错误的
## 真实行——这是 Perl 最强大、
## 也最难读的特性之一。
$@ =~ s/\(eval\) line (\d+)/$CGI . " line " . ($START - $1)/e;
$@ =~ s/ at .* line \d+\.$/$CGI/;
```

```perl
my $error_message = $@;
```

```perl
print <<ERR;
Content-type: text/html
```

```html
<html>
<head><title>Error</title></head>
<body>
<h1>Error</h1>
<code>$error_message</code>
</body>
```

```perl
ERR
}

exit();
```




## 第 4 章 处理表单

guestbook.cgi (继续)

```perl
while (!eof(GB)) {
    $my se = new CGI(\*GB); # 读取“冻结”的 CGI 输入
    $num_entries++; # 计数计数
    $entries .= draw_guestbook_entry($se); # 并绘制条目
}
```

```perl
close (GB);

# 将条目计数和条目本身插入
# html 页面
if ($num_entries) {
    $html = "<Signed $num_entries entries" . (($num_entries > 1) && "('s')");
    $html .= "</p>";
} else {
    $html = "<h3>No entries!</h3><hr>";
}
```

```perl
$html = entry_form($q); # 将表单添加到页面
$html = $q->end_html; # 并结束页面
```

```perl
print $html;

## in: CGI 对象
## out:
# description:
# 将条目添加到留言板文件，然后打印留言板文件
sub add_entry {
    my $q = $shift;
    my ($name,$email,$homepage,$msg,$entry,$url) = @q;

$url = $q->url;
```

```perl
untaintparams($q); # 检查并清理输入

# 打开留言板进行追加
open (GB, ">GUESTBOOK") or |
die "Unable to write to guestbook (error: $!)" . 
    "请重试，或联系此站的管理员寻求帮助";
```

```perl
# 获取留言板的写锁，
# 以确保在我们在写入时
# 没有其他人尝试对其读取或写入
lock_filehandle(\*GB, 'W');
$q->save(\*GB); # 将 CGI 输入“冻结”到文件中

# 关闭会自动移除锁文件
close GB;
```

guestbook.cgi (继续)

```perl
# 打印感谢，并带上返回留言板的链接
print $->header;
$->start_html('Thanks!');
$->h1('您的消息已添加到我的留言板中。');
$->p;
$->a(href="$Sq->url", "返回留言板");
$->end_html();
```

```perl
## in: 留言板条目
## out: html 格式的留言板条目
# description:
## 将留言板条目格式化为 html
sub draw_guestbook_entry {
  my $entry = shift;
  my $author;
```

```perl
# 将 CGI 输入导入命名空间，
## 在下方进行插值。
Sentry->import_name('E');
```

```perl
## 如果存在，包含电子邮件和主页链接
$author = $E::name;
if ($E::email =~ /(.*?)@(.*?)\.(..*)/) {
  $author = qq('<a href="$E::email">$E::name</a>');
}
```

```perl
if ($E::homepage) {
```

```perl
## 确保 URL 以 http:// 开头
$E::homepage = s|^(http://)?|http://|;
```

```perl
# qq 意味着“双引号” - 它的作用与在内容周围加上
## 引号相同。我们在这里使用它是因为
## 我们引用的内容中已经包含了引号。
$author .= qq('<a href="$E::homepage">$E::homepage</a>');
```

```perl
## “此处文档”不仅仅用于打印 - 你可以将它们
## 赋值给变量，或者像这里一样，直接从
## 函数返回它们
return <ENTRY>;
```

```perl
<p>$author</p>
<br>$E::message</p>
<ENTRY>
}
```

```perl
sub entry_form {
  my $Sq = shift;
  my $url = $Sq->url;
```

## Perl 网站工作坊

guestbook.cgi (继续)

```perl
my $form = <<FORM;
<<h3>签名我的留言板：</h3>
<form action="url" method="post">
<p>name:<b><input type="text" name="name"/></p>
<p>E-mail:<b><input type="text" name="email"/></p>
<p>Homepage:<b><input type="text" name="homepage"/></p>
<p>Message:<b><textarea cols="30" rows="6" name="message">在此输入您的消息。</textarea>
<input type="submit"/>
</form>
FORM
E_FORM
```

```perl
# 你不需要使用 'return' 来返回数值；
## 函数的最后一个表达式将被自动返回。
## 在这种情况下，表达式只是一个变量，
## 因此返回的是变量的值。
$form;
```

```perl
## untaint_params
## in: CGI 对象
# out: 可的（标量）参数，或如果看到可疑输入
# 注意：此函数在处理多值参数时无法正常工作！
# 如果你提交了一个带有多个选择的 <select> 字段，你将得到
## 一个奇怪的结果：所选的数量，而不是选择
## 本。在书的后面部分，我们将向你展示如何
## 在这样的函数中处理多值字段。
untaint_params {
my $q = shift;
my (@ok, $sk, $sp);
```

```perl
@ok = $sq->keywords;

foreach $k (@ok) {
  $sq->param(name=$k, value=untaint($sq->param($k)));
}

return (@ok, $sk, $sp);
```

```perl
sub untaint {
  my $val = shift;

## 允许字母数字、空白和标点符号
my $ok_chars = q|[\s.:?!]|;

die "非法字符" unless
$val =~ /^ok_chars$/

return $1;
}
```

```perl
## lock_filehandle
## in: filehandle
```

## 第 4 章 处理表单

guestbook.cgi (继续)

```perl
## out:

## description: flock() 是句柄，用于并发安全

## 这在不支持 flock() 的操作系统（如 MacOS）上无法工作。

sub lock_filehandle {

    my $fh = shift;

    my $lock = shift;

    use Fcntl qw(:flock);

my $lock_code;

    if ($lock =~ /r/i) {

        $lock_code = LOCK_SH;

    } elseif ($lock =~ /w/i) {

        $lock_code = LOCK_EX;

    } else {

        $lock_code = LOCK_UN;

    }

## 尝试两次

unless (flock($fh, $lock_code | LOCK_NB)) {

    die "flock: 无法锁定 $fh";

}

return 1;
```

## 其他文件

你需要一个留言文件，这是一个纯文本文件，必须赋予全局写权限。从 Unix 命令行创建留言文件：`touch /path/to/guestbook; chmod +w /path/to/guestbook`

当然，你会将`/path/to/guestbook`替换为留言板的路径。你还需要创建一个链接留言板的 HTML 文件。在这种情况下，我们设计了一个带有留言板链接的首页（见图 4.5）。点击链接进入留言板，你可以阅读其他条目并提交自己的（见图 4.6）。虽然你可以将留言文件放在任何地方，但最好放在 Apache docs 之外。将你不希望在浏览器中显示的任何内容分开有助于保持数据安全。这是一个良好的习惯。

## Perl 网站工作坊

图 4.5

带有留言板链接的首页。

![](img/d26997dc0c05711b472952aac_66_0.png)

图 4.6

留言板。

![](img/d26997dc0c05711b472952aac_66_1.png)

Molly (http://www.molly.com)
Jason, 你写的代码太酷了。Molly

guestbook.html

```html
<html>

<head>

<title>我们的留言板！</title>

</head>

<body color="#FFFFFF" text="#000000" link="#CC600" vlink="#0099CC">

<font face="arial,helvetica,sans-serif" size="5" color="#0099CC">用 Perl 设计</font>

<font face="arial,helvetica,sans-serif">

<p>欢迎来到首页。我们写这本书是为了帮助你使用 Perl 来增强你的网站设计和开发。</p>

<p>

Jason Pellerin 是书中代码的开发者，

Molly E. Holzschlag 的读者理解了如何使用这些代码并将其应用于日常设计中。</p>

<p>

来打个招呼吧！<a href="cgi-bin/guestbook.cgi">阅读并签名</a>留言板，

使用书中提供的脚本创建（自然地）！</p>

</font>

</body>

</html>
```

## 修改脚本

根据你的喜好修改脚本中的 HTML。例如，如果你想更改表单以包含一个“昵称”字段，可以通过向脚本的表单部分添加该字段来实现。

在我们的示例中，我们将文件放置在`/usr/local/data/guestbook`。

## 修改留言板表单

```html
<h3>签名我的留言板：</h3>

<form action="$url" method="post">

<p><b>姓名：</b> <input type="text" name="name"></p>

<p><b>电子邮件：</b> <input type="text" name="email"></p>

<p><b>主页：</b> <input type="text" name="homepage"></p>
```

## 修改留言板表单（继续）

```html
<p><b>昵称</b>：<input type="text" name="nickname"/></p>

<p><b>消息</b></p>

<p><textarea cols="30" rows="6" name="message">在此输入您的消息。</textarea></p>

<p><input type="submit"/></p>

</form>
```

## 经典的 Mailto 表单

可能是目前最常用的表单类型，Mailto 表单允许你创建一个带有标准表单输入的页面，用于收集访问者的信息。这些信息可能包括他们的姓名和电子邮件，以及一个你可以编写反馈的区域。

提交表单后，信息将发送到服务器，由脚本进行处理、整理，并输出到指定的电子邮件地址中。由于脚本有点长，我们将分成几个部分。

此脚本使用`Net::SMTP`发送邮件。如果你不在本地运行 sendmail，或者想使用其他服务器，你还需要编辑脚本，将`$SMTP_SERVER`变量更改为你使用的服务器名称或 IP 地址。

## 第 4 章 表单操作

mail_form.cgi (续)

```perl
$ENV{'ENV'} = '';

$ENV{'IFS'} = '';

use CGI;

## 导入 Net::SMTP 模块，这是一个与

# 邮件服务器交互的简单接口。

use Net::SMTP;

use strict;

use vars qw($START $CGI $SMTP_SERVER);

$CGI = "mail_form.cgi";

$SMTP_SERVER = "localhost";

eval ( main(); ); START

if ($@) {

  error_page($@);

}

exit(0);

## main
```

`main`函数（后文显示）执行了三件事：检查输入以确保其准确性、构建电子邮件消息，然后发送该消息。

## 需要的其他文件

为了访问邮件脚本，你需要一个标准的 HTML 表单，其中包含文本字段和提交按钮。你可以根据自己的喜意自定义页面。我们在这里包含了一个简单的示例。在这种情况下，我们为表单的成功或失败提供了处理（**加粗**显示）。如果表单提交成功，网站访问者将收到一个宣布提交成功的页面；如果提交失败，访问者将收到失败通知以及如何重新提交表单的说明。

## Mailto HTML 表单 *

```html
<html>

<head>

<title>联系我们！</title>

</head>
```

## Perl 网站制作工作坊

Mailto HTML 表单 (续)

```html
<body bcolor="#FFFFFF" text="#000000" link="#CC6600" vlink="#0099CC"

alink="#FFCC66">

<font face="arial, helvetica, sans-serif" size="5" color="#0099CC">

<p>联系我们:</p></font>

<p>

<form action="cgi-bin/mail_form.cgi" method="post">

<!-- 注消这些并将 URL 更改为符合你网站逻辑的内容，以使用自定义的搜索或失败页面

<input type="hidden" name="success_url"

value="http://localhost/perbook/chap_04/good.html">

<input type="hidden" name="fail_url"

value="http://localhost/perbook/chap_04/bad.html">

-->

<font face="arial, helvetica, sans-serif" size="25">

<p>收件人：<input name="_to" size="23"/></p>

<p>发件人：<input name="_from" size="23"/></p>

<p>兴趣:</p>

<p><select multiple size=4 name="interest">

<option>HTML</option>

<option>Perl</option>

<option>CGI</option>

<option>Web_Design</option>

</select></p>

<p>消息:</p>

<p><textarea wrap="virtual" cols="50" rows="5" name="text"></textarea></p>

<p><input type="submit" value="发送!"/></p>

</form>

</body>

</html>
```

在图 4.7，你可以看到我们创建的输入电子邮件表单。

一旦提交了邮件表单，它将被发送给邮件接收者。

## 图 4.7

经典的 mailto 表单。

![](img/d26997dc0c0571017b4729525ba1a4ac_71_0.png)

## 更多细节：Mailto 脚本中的准确性检查

我们使用`untaint_params()`来检查输入的准确性，该函数会对提交给脚本的每个表单字段调用`untaint()`。通过通过`%required`变量检查必需字段是否存在来确保输入的准确性。`%required`是一个“哈希（hash）”，也称为“关联数组”。哈希表对于存储一组具名的值非常有用。在 Perl 中，哈希变量始终以`%`开头，除非在哈希中使用单个项目除外。在那种情况下，当你访问单个项目时，变量以`$`开头。见下文，我们使用变量`%required`设定了整个`%required`哈希表，但使用表达式`$required{'_to'}`访问哈希的单个成员。在这里，我们使用它来保留我们的邮件表单无法的字段列表，缺少收件人（To）、发件人（From）和主题（Subject）消息头。

```perl
sub main {

my ($q, $self, $good, $err, %message, @missing);

# 每封邮件都需要的字段

%required = (

  '_to'      => 'To:',

  '_from'    => 'From:',

  '_subject' => 'Subject:');

$q = new CGI;

# 对所有内容去污染

untaint_params($q);

$good = 1;

# 确保必需字段存在 (To:, From:, Subject:)

foreach $f(keys %required) {

    unless (defined $q->param($f)) {

        $good = 0;

        push @missing, $required{$f};

    }

}

# 告诉用户为什么我们无法发送消息

die "缺少以下必需字段：" . join(', ', @missing) . ". 请联系此网站管理员寻求帮助。" unless $good;

# 从其他字段构建消息正文（名称不以 \_ 开头的字段）

build_message($message,$q);

# 发送邮件（我们将 $q 提交给此例程，以便它可以设置 $q->param('err')）

$good = send_message($message,$q);

# 如果成功则显示成功页面，失败则显示失败页面

result_page($good);
```

```perl
die "Failed to send mail";
```

```perl
$smtp->quit; # 关闭与邮件服务器的连接
```

```perl
# 如果我们捕获到错误，保存错误信息

# 并返回 0 (FALSE)

if ($0) {

    $sq->param('err_str', $0);

    return 0;

}

# 否则返回 1 (TRUE)

return 1;
```

当此函数被调用时，消息已经构建完毕并发送（或未发送）。我们在这里需要做的只是通知用户结果：如果成功，我们将其发送到调用 HTML 表单中定义的 success_page，或者在没有设置成功页的情况下，直接回显他们的输入。

如果我们无法构建或发送消息，将用户重定向到自定义的 fail_page（如果表单中定义了的话），或者在没有定义失败页的情况下，直接输出标准的错误页面。

```perl
# result_page

# in: success 或 failure

## out:

# description:

# 向用户发送反馈，关于其表单提交

# 是否是否成功。

sub result_page {

    my $good = shift;

    my $m_ref = shift;

    my $q = shift;

}
```

```perl
if ($good) {

# 如果表单包含 'success_url' 字段，

# 将用户引导到该 url。否则，输出

# 默认成功页

if ($sq->param('success_url')) {

    # CGI.pm 让很多事情变得简单，包括

    # 重定向。

    print $sq->redirect($sq->param('success_url'));

} else {
```

## Perl 网站工作坊

这里给初出茅头的程序员们一个人生教训：从用户的角度来看，结束往往只是你们工作的开始。在这种情况下，还剩下几个函数，这些函数在后台执行着重要的工作。

```perl
$q->start_html('表单提交');

$q->h3('您的信息已成功提交');

$q->dump;

$q->end_html();

} else {

    # 如果存在 'fail_url' 字段，将用户引导到那里。

    # 否则，发送默认的失败页面

    if ($q->param('_fail_url')) {

        print $q->redirect($q->param('_fail_url'));

    } else {

        # 默认失败页：主错误页面

        error_page($q->param('err_str'));

    }

}
```

我们从之前的脚本中提取了标准的错误页面输出，并将其封装进一个独立的函数中。这使得我们能够在脚本的任何时间、任何地方输出错误页面，而无需重复大量的代码。

```perl
error_page {

# in: 错误消息

## out:

# description: 在简单的 HTML 页面中将错误消息输出到浏览器

sub error_page {

    my $msg = shift;

    chomp($msg);

}

# 使用 $START 来确定错误发生的真实行

$msg = s/\(eval\) line (\d+)/\$(CGI . " . line . " . (\$ START-\$1)/e;

$msg = s/( at ) . ( line )/\$(CGI\$2)/;

print <<ERR;

Content-type: text/html

<html>

<head><title>Error</title></head>

<body>

<h1>Error</h1>

<code>$msg</code>

</body>

</html>

ERR

exit(0);

}

}
```

## 第 4 章处理表单

```html
<html>

ERR

exit(0);

}
```

接下来，也是最后，是对`better.cgi`和`guestbook.cgi`中使用的`untain_params()`和`untain()`函数的修订。这些函数与之前脚本中的函数有几个重要的区别。首先，`untain()`允许提交更广泛的标点符号，这与更通用的`mail_form.cgi`保持一致，后者可以从任意数量的不同表单调用。

其次，`untain_params()`经过修订，可以处理提交多个值的表单字段。为了做到这一点，我们利用了 Perl 处理数组的一个特性：它们不能通过将一个数组插入另一个数组来建立嵌套（尽管你可以通过引用将一个数组嵌入另一个数组中）。

```perl
@array = ('one', 'two', 'three', 'four', 'five');
```

在功能上完全等同于：

```perl
@array = ('one', 'two', 'three', 'four', 'five');
```

它们都产生数组 ('one', 'two', 'three', 'four', 'five')。我们通过使用一个临时数组并将每个表单字段值推入该数组来利用这一点：我们可以相同地处理每个字段，就像它们是数组一样。大多数字段只是只有一个一个值的数组。

```perl
# 安全例程

## untaint_params

## in: CGI 对象

# out: trusted_params, 或在看到可疑输入时崩溃

sub untaint_params {

my $q = shift;

my (@, $k, $sp, $t, @safe);

@k = $q->(@k) 

foreach $k (@k) {

  @tmp = ();

  push @tmp, $q->param($k);
```

## Perl 网站工作坊

```perl
foreach $t@(@tmp) {

    push @safe, untaint($t);

}

$q->param($k);

}

## untaint

# in: CGI_params

# out: trusted_params, 或在看到可疑输入时崩溃

sub untaint_params {

my $q = shift;

my (@, $k, $sp, $t, @safe);

@k = $q->(@k) 

foreach $k (@k) {

  @tmp = ();

  push @tmp, $q->param($k);

  foreach $t@(@tmp) {

    push @safe, untaint($t);

  }

  $q->param($k);

}

## untaint

# in: untrusted scalar

# out: trusted scalar, 或在看到可疑输入时崩溃

sub untaint {

    my $val = shift;

    return unless $val;

    # 允许字母数字、空格和大多数标点符号

    my $ok_chars = q[\w\s.,./?!\-'#$\+=_|];

    die "Illegal character(s) in input ($val)" unless

        $val =~ /^($ok_chars)*$/;

    return $val;

}
```

## 接下来

一旦你安装了`taintcheck`模块，你可以在任何想要运行污染检查的脚本中添加以下行：

`use Taintcheck;`

例如，这里有一个使用 Taintcheck 的开头：

```perl
#!/usr/bin/perl -wt

use strict;

use Taintcheck;

use lib '/home/moly/perl_lib';
```

请确保指向相应模块所在的库。我们指向了服务器上的`perl_lib`，污染检查以及其他模块都放置在那里。

## 第章 特性与功能

### 使用方法

- 1. 将代码复制到你的文本编辑器中。
2. 将代码保存为`Timefuncs.pm`。
3. 将`Timefuncs.pm`放置在服务器的 Perl 库中。

Timefuncs.pm

```perl
package Timefuncs;

use Exporter;

$ENV{'PATH'} = '/bin:/usr/bin:/usr/local/bin';

$ENV{'SHELL'} = '/bin/sh';

$ENV{'IFS'} = '';

@ISA qw(Exporter);

@EXPORT qw(file_stats file_age date_string);

use strict;

# file_stats

# 输入：文件名

# 输出：文件的修改日期和大小

sub file_stats (

    my $file = shift;

    my ($size,$mtime) =

# -s 运算符返回文件大小

$size = (-s $file);

# stat 函数返回一个包含大量文件

# 信息的大数组。我们只对第 6 个元素感兴趣

# 即文件最后修改的时间。

$mtime = (stat $file)[9];

# perl 中的函数不仅限于返回

# 单个值 - 与 C 语言不同。

# 在这里我们以数组的形式返回两个值。

# 如果你需要返回一个大数组，最好

#（大多数情况下）返回一个数组引用代替。

    return ($mtime, $size);

}

# file_age

# 输入：文件名

# 输出：文件以天为单位的年龄

sub file_age (

    my $file = shift;

# -N 函数返回文件以天为单位的年龄
```

## Timefuncs.pm (续)

```perl
# 相对于程序启动的时间。由于

# CGI 程序 打算只运行很短的时间，因此

# 对于文件有多老，这是一个足够足够准确的数值。

return int(-N$file);
```

```perl
# date_string

# 输入：unix 时间戳

# 输出：良好的、人类可读的日期字符串

sub date_string {

my $ts = shift;
```

```perl
# POSIX 模块随 Perl 标准提供，

# 包含了 strftime 函数，该函数可以

# 生成格式良好的日期字符串。

POSIX;
```

```perl
# 下面的格式字符串返回的时间格式为：

# mm/dd/yyyy hh:mm am

return

POSIX::strftime("%D %I:%M %P", localtime($ts));
```

就像污染检查（taint check）模块一样，你需要在任何你想要运行时间函数的文件中添加一行代码。这里是代码：

`use Timefuncs;`

这里是摆入了该代码后的代码片段：

# 时间函数示例

```perl
#!/usr/bin/perl -WT

use lib '/usr/home/molly/perl_lib';

use strict;

use Timefuncs;
```

## 需要的其他文件

为了能够从命令行访问时间函数模块产生的时间信息，你需要添加一个脚本。以下 Perl 脚本是一个简单的实用程序，它允许你从 Unix 命令行访问时间函数模块的输出。

### 使用方法

- 1. 将代码复制到你的文本编辑器中。
- 2. 将代码保存为`get_all_stats.pl`。
- 3. 将文件放置在服务器上你可执行路径中的某处。如果你没有 root 权限，请放在`~/bin`（你家目录下的 bin 目录）。
- 4. 使用`chmod a+x get_all_stats.pl`使文件可执行。

```perl
get_all_stats.pl

!#/usr/bin/perl -w

use '/path/to/library'; # 替换为实际路径

use Timefuncs;

$f = $ARGV[0];

die "usage: get_all_stats.pl file_name" unless $f;

($m, $ss) = &file_stats($f);

print "File $f is size $ss KB, "

  "last modified $m seconds since the epoch.\n";

print "Age " . &file_age($f) . " days\n";

print "Modification date ($m) in human-readable format:\n  ".&date_string($m)."\n";
```

安装完成后，你可以通过在 Unix 命令行中输入`./get_all_stats.pl [filename]`来获取所需的信息（见图 5.1）。

## Perl 网站工作坊

图 5.1

获取文件统计信息。

```text
# <faddr: example@gmail.com>

# 如果你发送邮件到：

# 或者如果你需要 $$$ 快速挣钱 $$$,

# hostmaster@dispatch.net

-- 

待在家里。

你有新邮件：

@molly@usr/home/moly/public_html/

@molly@usr/home/moly/public_html$ is

bad.html

first_cgi.pl

first_function.pl

ghost.html

cgi-bin/

chap_05/

guestbook

malist

malifest2.html

chapter_6/

image.html

milto

winu*

date.shtml

@molly@usr/home/moly/public_html$ cd chap_05

@molly@usr/home/moly/public_html$ chap_05$ in

test.html

roll_pages.pl

dm_example.pl

get_all_stats.pl
```

## 如何使用

- 1. 从 CPAN 获取 LWP::User 包并安装它。
- 2. 从 CPAN 安装 HTML::Parse 和 HTML::LinkExtractor。
- 3. 将脚本复制到你的文本编辑器中。
- 4. 将脚本保存为 link_check.pl。
- 5. 将脚本放置在可执行路径中。

link_check.pl

```perl
#!/usr/bin/perl

#

# link_check.pl

#

# 一个网络机器人，用于检查提交的网站上的所有链接，

# 到指定的深度，并可选地检查外部

## 。
```

```perl
use lib '/usr/home/mollly/perl_lib';

use Taintcheck;
```

```perl
use LWP::RobotUA;      # 一个礼貌的 Web 客户端

use HTML::LinkExtor;      # 用于从页面提取链接

use Getopt::Std;           # 方便处理命令行

                             # 参数
```

```perl
use strict;

use vars qw($opt_e $opt_v $USAGE $ROOT

     $DEPTH $REPORT $OWNER @CHECKED PAGES $BAD);
```

```perl
$USAGE = "usage: link_checker.pl [-v] url [depth]\n";
```

```perl
getopt();
```

```perl
die $USAGE unless ARGV;

# 替换为你的真实邮箱地址

OWNER  = "you@your.email.addr";

$ROOT  = $ARGV[0];           # 从哪里开始检查

$DEPTH = $ARGV[1] || 2;    # 检查多深
```

```perl
# -v 选项传统上意味着“详细模式”；即在运行时输出

# 大量信息

($opt_v) && print("-" * 60) . "\nlink_check.pl started at " .

loc localtime(time) . "\n\n";
```

## 第 5 章 特与功能

link_check.pl (续)

```perl
check_links($ROOT,0);

$REPORT = (scalar @BAD) . " bad link(s) were found in\n$PAGES page(s)\n";

(@BAD) && ($REPORT = join("\n", @BAD) . "\n");

print $REPORT;

($opt_v) && (print("\nlink_check.pl finished at " . localtime time) . "\n" . ("-" x 60) . "\n\n"));
```

```perl
exit;
subroutines
```

```perl
sub check_links {

    $cur_page_url = shift;

    $cur_depth = shift;

    $parent_url = shift;

    my ($bot, $req, $res, $links, $a_links, $link);

    # 如果我们已经访问过此页面，停止

    if (grep($cur_page_url, @CHECKED)) {

        return;

    }

    ($opt_v) && (print(' ' x $cur_depth) . ".. CHECK $cur_page_url\n"));

    # 启动机器人

    $bot = new RobotUA('dwp_linkbot/0.1', $OWNER);

    # 在请求之间等待，以免冲击击 Web 服务器。

    # RobotUA 已经为我们处理了一些睡眠，但

    # 我们想更加礼貌。

    sleep(2);

    if ($cur_depth < $DEPTH) {

        $PAGES++;

        push @CHECKED, $cur_page_url;

        # 查找当前页面，或者向报告报错并返回

        $req = new HTTP::Request('GET', $cur_page_url);

        $res = $bot->request($req);

    }

    unless ($res->is_success) {

        ($opt_v) && (print(' ' x $cur_depth) . "*** FAILED: ");
```

link_check.pl (续)

```perl
$cur_page_url = $res->status_line . "\n";

push @BAD, "parent_url: $cur_page_url (" .

$res->status_line . ")";

return;

# 获取当前页面上的链接

($links, $a_links) = get_links($res);

# 仅对非页面链接进行 HEAD 请求 - 我们不想

# 下载整个图像等。

foreach (@links) {

    if ($opt_e || local($link)) {

        $req = new HTTP::Request("HEAD", $link);

        $res = $bot->request($req);

        unless ($res->is_success) {

            ($opt_v) && print("*" x ($cur_depth+1)) . $res->status_line . "\n");

            "** FAILED: link $link (";

            push @BAD, "$cur_page_url: (" .

$res->status_line . ")");

        }

    }

}

# 递归处理每个 <a> 链接

foreach (@a_links) {

    # 如果我们正在检查所有链接，或者链接是本地的，

    # 打开页面并检查它。增加

    # 深度计数器，以免我们对网站的检查比预想的深。

    if ($opt_e || local($link)) {

        check_links($link, $cur_depth+1, $cur_page_url);

    }

}

sub get_links {

    my $res = shift;

    my $base = $res->base;

    my $p = new HTML::LinkExtor(undef, $base);

    my (@links, @a_links, @tag, @attr);

    foreach ($p->links) {

        ($tag, @attr) = @_;

        if ($tag eq 'a') {

            push @a_links, @attr;

        } else {

            push @links, @attr;

        }

    }

    # 不能直接返回 (@links, @a_links) - 数组会被

    # 合并为一个大数组；我们需要将它们

    # 分开，所以返回两个引用。

    return (@links, @a_links);

}

sub local {

    my $link = shift;

    return $link =~ /$ROOT/;

}

sub in_array {

    my $item = shift;

    my $arr_ref = shift;

    my $a;

    foreach (@$arr_ref) {

    ($item eq $a) && return(1);

}

return 0;

}
```

脚本很容易。你可以使用几个选项，取决于你想要的输出类型

`./link_check.pl [-ev] site [depth]`

`-e`选项提取外部链接以及本地链接。`-v`选项会提供详细反馈（见图 5.2）。depth 选项用于确定脚本抓取网站的深度。例如，如果 depth 保持默认值 2，它将检查你提交给脚本的 URL 以及从该 URL 成功加载的每个页面中的链接。你可以将 depth 设置为 3。

这是一个服务器友好的脚本，因为它会在请求服务器之间等待几秒。如果你有一个很大的网站需要检查，请晚上运行。

## Perl 网站工作坊

图 5.2

使用 link_check.pl 检查链接。

![](img/26997dc0c057101b472952ba1aac_94_0.png)

```bash
perl link_check.pl -v http://www.google.com 1
link_check.pl started at Mon Nov 19 21:55:57 2001

-- CHECK http://www.google.com
-- FAIL http://www.google.com/search: 403 Forbidden
-- CHECK http://www.google.com/images/
-- CHECK http://www.google.com/corp/
-- CHECK http://www.google.com/dir/
-- CHECK http://www.google.com/android_search
-- CHECK http://www.google.com/preferences
-- CHECK http://www.google.com/gettools
-- CHECK http://www.google.com/services/
-- CHECK http://www.google.com/maps
-- CHECK http://www.google.com/about.html
-- It likely was served by google-1!
http://www.google.com/search: 403 Forbidden
```

## 错误检查

此脚本演示了如何使用 CPAN 中的实用模块来检查脚本错误。Carp 提供的信息要友好得多，特别是对于非程序员。如果你的脚本中没有它，你将在你的服务器文档中搜索显示的错误（见图 5.3）。很多情况下，你无法获得这些信息。相反，你的 ISP 系统管理员拥有它们，但可能无法传递给你。

添加错误检查将给你真实的信息。这个脚本是你第 4 章处理过的 first_oo.cgi 表单的回归。然而，我们在那里放置了一个错误，以演示调试脚本的体验。

## 如何使用

- 1. 将脚本复制到你的文本编辑器中。

- 2. 将脚本保存为 buggy_oo.cgi。

- 3. 将表单放在你服务器上的 cgi-bin 目录。

- 4. 修改权限允许所有用户执行：

`chmod a+x buggy_oo.cgi`

- 5. 在浏览器中访问该页面以查看错误结果

![](img/26997dc0c057101b472952ba1aac_95_0.png)

图 5.3

浏览器显示的错误页面。

```perl
#!/usr/bin/perl -w
#
use CGI;
use CGI::Carp qw(fatalsToBrowser);

$q = new CGI;
$self = $q->url;

print $q->header;

## 如果我们获得了一些输入，显示结果页面。
## 否则，显示输入表单。
```

```perl
#
if ($q->param('name')) {

    $name = ucfirst($q->param('name'));

    print <<HTML;
<html>
<head>
<title>My First CGI</title>
</head>

<body>
<h1>Hello, $name! This is my first CGI!</h1>
<p>This is my first CGI!</p>
</body>
</html>
HTML
else {
# 此 print 的结束标签故意
# 拼写错误。
print <<FORM;
<html>
<head>
<title>What's your name?</title>
</head>

<body>
<h1>What is your name?</h1>

<form action="$self" method="post">
<p>Your name: <input type="text" name="name"></p>
<p><input type="submit"></p>
</form>
</body>
</html>
FRM
}
```

请注意它们与没有包含 Carp 模块的示例有何不同之处（见图 5.4）。

## 第 5 章 特性与功能

图 5.4

使用 Carp 模块时显示的错误信息。

![](img/d26997dc0c0571017b4729525ba1a4ac_97_0.png)

## 验证表单

这是另一个用于验证表单的有用模块示例。验证在许多方面都很有帮助，包括：

- 确保表单的安全性

- 检查从表单中获取的信息是否是你请求的信息

- 确保没有遗漏关键元素

该脚本是确保输入到表单中的信息完整的的一种简单且优雅的方法。在你你的网站的任何表单中在脚本中使用此模块。这里显示的脚本提供了一个使用了该模块的表单脚本示例。

## 如何使用

- 将脚本复制到你的文本编辑器中。

- 将脚本保存为`signup.cgi`。

`CGI::Validate`模块应该驻存在于 Apache 服务器上。如果不可用，请在 CPAN 中检查（参见第 3 章“脚本基础”）。

## Perl 网站工作坊

3. 将 HTML 页面中的表单 action 指向你`cgi-bin`目录下的`signup.cgi`，并将页面保存到你的 Web 服务器上作为`contest.html`。

4. 修改权限以允许所有用户执行：

```
chmod a+x signup.cgi
```

contest.html

```html
<html>
<head><title>立即注册即可赢奖！</title></head>
<body>
<h1>赢！赢！赢！</h1>
<p>请填写下方的报名表。标有 <font color="red" size="7"></font> 标记的字段是必填的。</p>
<form action="signup.cgi" method="post">
名字: <input type="text" name="first_name">
<font color="red" size="7"></font>
姓: <input type="text" name="last_name">
<font color="red" size="7"></font>
电话: <input type="text" name="phone">
<font color="red" size="7"></font>
邮箱: <input type="text" name="email">
<font color="red" size="7"></font>
在 1 到 10 分范围内，你有多喜欢豆豆玩娃娃：
<input type="text" name="beanies" size="2">
<input type="submit" value="提交并赢奖!">
</form>
</body>
</html>
```

## Signup.cgi

```perl
#!/usr/bin/perl -wT

$ENV{PATH} = /bin:/usr/bin:/usr/local/bin;
$ENV{SHELL} = /bin;
$ENV{ENV} = '';
$ENV{IFS} = '';

use lib '/path/to/library';
use Taintcheck;

use CGI;
```

Signup.cgi（续）



# 第 6 章 定制页面

```perl
# 这告诉模块我们想要的函数和变量
use CGI::Validate qw(CheckFormData
addExtensions
%Missing
%Invalid
%blank
%Invalid);
# 检查数据
# 添加自定义数据类型
# 查找缺失的字段
# ... 无效字段
# ... 空白字段
# 以及带有错误数据的字段
```

```perl
use strict;
use vars qw($) START $CGI;
$CGI = "signup.cgi";
eval { main() } $START LINE ;
```

```perl
if ($0) {
chomp($0);

$0 -= s/\(eval\) line\(\d+)/\($CGI)
* line .* ($START -1/)/e;
$0 -= s/( at).*( line)/$($CGI)$2;

my $error_message = $0;
```

```perl
print <<ERR;
Content-type: text/html
```

```html
<html>
<head><title>错误</title></head>
<body>
<h1>错误</h1>
<pre>
$error_message
</pre>
</body>
</html>
```

```perl
ERR

exit(0);

```

```perl

# main 函数

sub main {

my $err;

# 向验证器中添加我们自定义的“电话号码”类型

# （这个丑陋的正则表达式查找 (123) 456-7890

# 其中 () 和 - 是可选的）

```

Signup.cgi（续）

```perl

&addExtensions ( Phone => sub {

    $[0] = /\/(\d(3)\)?[^\s]?\d(3)\-\s]?\d(4)/;

});

my $q = &CheckFormData(

    'first_name=',

    'last_name=',

    'phone=xPhone',

    'email=e',

    'beans=i'

) do or {

    if (%Missing) {

        $Err = "<li>缺失的表单元素: " .

               join(', ', keys %Missing) . "</li>";

    }

    if (%Invalid) {

        $Err = "<li无效的表单元素: " .

               join(', ', keys %Invalid) . "</li>";

    }

    if (%Blank) {

        $Err = "<li空白的表单元素: " .

               join(', ', keys %Blank) . "</li>";

    }

    if (%InvalidType) {

        $Err = "<li带有错误数据的表单元素: " .

               join(', ', keys %InvalidType) . "</li>";

    }

};

if ($Err) {

    print "Content-type: text/html\n\n";

    print "<html><body><h1>错误</h1><ul>$Err</ul></body></html>";

} else {

    print "Content-type: text/html\n\n";

    print "<html><body><h1>提交成功！</h1></body></html>";

}

```

# 第 6 章 定制页面

browser_detect.cgi (继续)

```perl

sub browser_version {

  $ua = shift;

  my ($browser, $version, $os, $sb, $b);

  # 浏览器模式是一个数组的哈希结构

  # 哈希中的每个数组有两个值：

  # 1. 识别浏览器版本的模式

  # 2. 识别浏览器版本的模式

  my $browser_pat = [

    'Netscape Navigator' => [

      'mozilla/(?!(msie|opera))',

      'mozilla/([\d.]+)',

    ],

    'MS Internet Explorer' => [

      'compat\.msie',

      'mozilla/([d.]+)',

    ],

    'Opera' => [

      'opera',

      '([d.]+)',

    ],

    'Lynx' => [

      'lynx',

      'lynx/([d.\w]+)',

    ]

  ];

# OS 模式是一个简单的哈希

my $os_pat = [

  'mac',

  'Windows 9x' => 'windows.*?9d',

  'Windows NT' => 'windows.*?nt',

  'Windows 2000' => 'windows.*?2000',

  'Linux' => 'linux',

  # 一个合理的猜测

  'Unix' => 'x!(.*linux)'

];

# 遍历哈希，寻找匹配项

foreach $sb(keys $browser_pat) {

  if ($ua =~ /$browser_pat($sb)->[0]/i) {

    $browser = $sb;

    last;

  }

}

# 对 OS 执行同样的操作

foreach $os(keys $os_pat) {

  if ($ua =~ /$os_pat($os)/i) {

    $os = $os;

    last;

  }

}

# 然后使用匹配的浏览器类型

# 确定如何猜测浏览器版本

if ($ua =~ /$browser_pat($browser)->[1]/i) {

  $version = $1;

}

return ($browser, $version, $os);

}

```

## Perl 网站工作坊

## 需要的其他文件

为了测试该脚本，你可以创建一个链接到它的简单 HTML 文件：

1. 打开你的文本编辑器。
2. 创建一个标准的 HTML 文档。
3. 添加一个指向 `browser_detect.cgi` 脚本的链接。
4. 将该 HTML 上传到服务器上相应的目录。

用于浏览器检测的 HTML 文档

```html

<html>

<head>

<title>Simple CGI Script</title>

</head>

<body>

<p>

<br>

<br>

</p>

<div align="center"><a href="/cgi-bin/browser_detect.cgi">Testing Browser Detect</a></div>

</p>

</body>

</html>

```

现在，你已经将 HTML 文件加载到服务器上，请使用你的浏览器测试该文件。在图 6.2 中，你可以看到浏览器中显示的浏览器检测信息，这次显示的是 Netscape Navigator，版本 4.07，运行在 Windows 98 上。

# 路由浏览器

一旦你确定了访问者使用的浏览器品牌和型号，将她重定向到为她设置的页面就非常简单。只需向 `browser_detect.cgi` 脚本中添加以下函数即可。

```perl

sub route_browser {

  my $sq = shift;

  my $ua = shift;

  my ($br, $Svr, $Sos) = browser_version($ua);

  # 默认设置为任何人都可以读取的页面

  my $page = 'text_only.html';

  # 这是选择页面最直接的方法

  # 你也可以设置一个哈希的哈希，

  # 组织方式为浏览器 => 版本 => 页面，这将

  # 使这个函数短得多。

```

```perl
if ($br eq 'Netscape Navigator') {
  if ($vr > 4) {
    $Page = 'fancy.ns.html';
  } else {
    $Page = 'basic.ns.html';
  }
} elseif ($br eq 'MS Internet Explorer') {
  if($vr > 4) {
    $Page = 'fancy.msie.html';
  } else {
    $Page = 'basic.msie.html';
  }
} elseif ($br eq 'Opera') {
  $Page = 'standard.html';
}
```

```perl
$q = -redirect($page);

```

![](img/d26997dc0c0571017b4729525ba1a4ac_107_0.png)

## 如何使用

1. 将代码复制到 `browser_detect` 文件中。
2. 自定义 `elseif` 语句以跳转到你选择的页面。例如，在我们标有 `fancy.ns.html` 的地方，你需要将其替换为你的 HTML 文件名。
3. 保存文件。
4. 将文件存放在服务器的 `cgi-bin` 目录中。
5. 修改权限允许所有用户执行：

```bash

chmod a+x browser_cgi

```

至此，浏览器将有效地将浏览器重新重定向到你定义的服务器页面。

# Cookies

想吃饼干吗？我们更偏于巧克力 Milanos 饼干，而且我们可以向你保证，在写这本书期间吃了很多饼干！在 Web 开发中，Cookies 是将信息保存到访问者硬盘的小型脚本。这可以帮助设计者自定义网站在未来访问时的行为。例如，通过 cookies，你可以创建一个通过名字欢迎访问者、跟踪购买或保存访问者上次所在地的站点（见图 6.2）。对于使用 CGI 的 Perl 程序员来说，硬编码可以工作的 headers 非常困难，CGI 为你完成了大部分工作。读取 cookie 的脚本也同样简单，如下：

```perl

#!/usr/bin/perl

use CGI;

my $q = CGI->new;

my $cookie = $q->cookie('test_cookie');

# Cookie 未设置

print $q->start_html("Cookie Reader");

$q->p("Cookie: " . $cookie);

$q->end_html();

```

人们认为 Cookies 可以从他们那里窃取个人信息，然后这些信息可以被主机用于营销或其他目的。这并非完全正确。Cookies 获取信息，但它们将其保存到访问者的计算机上，这就是为什么它们通常是安全的。然而，多个网站的广告商可以使用 cookies 跟踪你从一个站点到另一个站点的进度。实际上，脚本是用于显示 cookie 值的。

# 定制页面

设置 cookie 同样简单。这是另一个例子：

```perl

#!/usr/bin/perl

use CGI;

my $q = CGI->new;

my $cookie_val = 'Rod';

my $cookie = $q->cookie(name=>test_cookie', value=$cookie_val);

print $q->start_html("Cookie Writer");

$q->p("Your cookie has been set to $cookie_val");

$q->p("Visit the ");

$q->a(href="read_cookie.cgi", "Cookie Reader"), to read your cookie.");

$q->end_html();

```

尝试结合使用这两个示例来查看 cookie 的效果。根据你的浏览器和操作系统，在硬盘上搜索名为 `cookie` 的文件，你可能会找到它。

# 带 Cookies 的高级留言板

在这个例子中，我们展示了如何向第 4 章“表单操作”中创建的留言板添加 cookie。此脚本保存用户信息，直到下次访问时用名字问候。我们亲切地称之为“幽灵”（spooky）留言板，因为对于外行来说，它确切知道访问者是谁

## 如何使用

1. 将代码复制到你的文本编辑器。
2. 将代码保存为 `guestbook_2.cgi`。
3. 将文件传输到你的服务器。
4. 如下修改权限：

```bash

chmod a+x guestbook_2.cgi

```

```perl
guestbook_2.cgi

#!/usr/bin/perl -w

$ENV{'PATH'} = '/bin:/usr/bin:/usr/local/bin';

$ENV{'SHELL'} = '/bin/sh';

```

guestbook_2.cgi (继续)

```perl

$ENV{'ENV'} = '';

$ENV{'IFS'} = '';

use lib '/usr/local/html/perlbook/chap_05';

use Taintcheck;

use Timefuncs;

use CGI;

use strict;

use vars qwCGI $GUESTBOOK);

$CGI = 'guestbook_2.cgi';

$GUESTBOOK = '/path/to/guestbook'; # 替换为真实路径

eval { main(); }; START LINE;

if ($@) {

  chomp($0);

}

$@ = s/\s+\(line\ (\d+)/$CGI . " line " ($START -1)/e;

$@ = s/( at).*(line )/\$CGI$2/);

my $Error_message = $0;

print <<ERR;

Content-type: text/html

<html>

<head><title>Error</title></head>

<body>

<h1>Error</h1>

<code>$error_message</code>

</body>

</html>

ERR

}

exit(0);

```

## main

```perl
sub main {
my $q = CGI->new;

if ($q->param()) {
  add_entry($q);
} else {
  display_guestbook($q);
```

```perl
}
}
# subroutines
# in: CGI object
## out:
# description: 
# 读取留言板文件并以 html 格式打印
sub display_guestbook {
    my $Sq = shift;
    my ($html,$e,$num_entries,$entries,$cookie,$thanks) = $Sq->header('My Spooky Guestbook');
    $html .= $Sq->h1('My Spooky Guestbook');

open (GB, "<\GUESTBOOK") ||
    die "Unable to read guestbook file \$GUESTBOOK (error: $!)";
    print "Please try later later or contact the webmaster of this site for assistance";

# 获取留言板的读锁
lock_handle($GB, 'R');

# 读取并处理条目
while (eof($GB)) {
    my $e = new CGI($GB);
    $num_entries++;
    $entries[] = draw_guestbook_entry($e);
}

# 这里我们获取 'spooky': 如果用户已经签名
# 留言板，她将有一个 cookie 告诉我们她是什么时候签名的
if ($e->param('cookie') == $Sq->cookie('sg_signed_at')) {
    $thanks = "<p>Hello, <b>" . $e->param('name') . "</b>! Thanks for signing your guestbook on " \n        date_string(\$e->param('cookie')) . "</p>\n";
}

close($GB);

# 插入条目计数以及条目本身，
# html 页面

if ($num_entries) {
    $html .= "<p>Signed \$num_entries time " \n"(\$num_entries > 1) && ("s")";
    $html .= "&#183; Last signed ";
```

# Perl 网站开发工作坊

guestbook_2.cgi（续）

```perl
date_string(file_stats($GUESTBOOK ))[0] );
$html .= $thanks if $thanks;
$html .= $entries . '</p>';
else {
$html .= '<h3>No entries!</h3><hr>';
}

$html .= &entry_form($Q);
$html .= $q->end_html();

print $html;

# 输入: CGI 对象
# 输出:
# 说明:
# 向留言板文件添加条目，打印留言板的 HTML
# 同时设置一个带有当前时间的 cookie
sub add_entry {
my $q = shift;
my ($name,$email,$homepage,$msg,$entry,$url,$cookie);
$url = $q->url;

# 获取参数比获取 cookie 更容易，
# 所以先在这里保存该值
$q->param('cookie', time);

# 然后创建一个 cookie，我们将将其放入输出的
# http 报头中
$cookie = $q->cookie(-name=>'sg_signed_at',
value=>$q->param('cookie'));

untaint_params($q);

# 将提交的内容写入留言板
open (GB, ">GUESTBOOK") ||
die "无法写入留言板（错误: $!)." " 
  "请稍后重试，或联系此站的管理员 " 
  "以寻求帮助";

# 获取留言板的写锁
lock_filehandle(GB, 'W');

$q->save("<GB");
# 关闭文件会自动移除文件锁
close GB;

# 表示感谢，并附带返回留言板的链接
# 这里是 cookie 真正设置在用户计算机的地方
```

# 第 6 章 自定义页面

guestbook_2.cgi（续）

```perl
print $->header(-cookie=$cookie ),
$->start_html("感谢!"),
$->h1("感谢!"),
$->h3("您的消息已添加到我的留言板中."),
$->p,
$->a(href=$->url, "返回留言板"),
$->end_html();
```

其余代码与原始的 `guestbook.cgi` 完全相同，由于我们还从 `Taintcheck.pm` 获取了 `untaint` 函数（参见第 5 章“特性与函数”）。

# 输入: 留言条目

# 输出: HTML 格式的留言条目

# 说明:

# 将留言条目格式化为 html

```perl
sub draw_guestbook_entry {
my $entry = shift;
my $author;
# 将参数导入到命名空间，以便于
# 插值
import_names('E');

# 如果存在，包含邮箱和主页链接
$author = $E::name;
if ($E::email =~ /-\.\?@\(\*\?\)\+\*/) {
$author = qq|<a href="$E::email">$E::name</a>|:q;
}

if ($E::homepage) {
# 确保主页以 http// 开始
$E::homepage = s|^(http:\/\/)(.*)$|$http://$2|;
$author = qq|<a href="$E::homepage">$E::homepage</a>|:q;
}
return <<<ENTRY>;
<p><a>$author</a>
<br/>$E::message</p>
<hr>
ENTRY
```

```perl
sub entry_form {
my $q = shift;
my $url = $q->url;
```

```perl
my $Form = <<E_FORM;
<h3>在我的留言板上留言：</h3>
<form action="$url" method="text">
<p>姓名</p>: <input type="text" name="name"/></p>
<p>邮箱</p>: <input type="text" name="email"/></p>
<p>主页</p>: <input type="text" name="homepage"/></p>
<p>消息</p></p>
<p><textarea cols="30" rows="6" wrap="virtual" name="message"></textarea></p>
<input type="submit"/></p>
</form>
E_FORM;

my $filehandle;
my 输入: 文件句柄
my 输出:
# 说明: flock() 对句柄进行锁定，实现并发安全的访问
sub lock_filehandle {
my $fh = shift;
my $lock = shift;

use Fcntl qw:flock;

my $lock_code;

if ($lock =~ /r/i) {
$lock_code = LOCK_SH;
} elsif ($lock =~ /w/i) {
$lock_code = LOCK_EX;
} else {
$lock_code = LOCK_UN;
}

## 尝试两次
unless (flock($fh, $lock_code | LOCK_NB)) {
unless (flock($fh, $lock_code)) {
die ":无法获取 $GUESTBOOK 的 $lock 锁";
}
}

return 1;
}
```

6.3 显示了返回时的个性化问候，这归功于保存存在 Molly 硬盘上的 cookie。

# 图 6.3

个性化结果。

![](img/d26997dc0c0571017b4729525ba14ac_115_0.png)

# 我的幽灵留言板

已签名 7 次 - 最后于 1999/5/4 上午 10:16

你好, molly:感谢你在 1999/5/4 上午 10:16 在我的留言板上签名

Jason (http://www.lonely.com) 嗨 Molly! 你太酷了！

在此输入你的消息。

Molly (http://www.molly.com/) Jason, 你写的代码是最酷的。

# 在 SSI 中使用 Perl

到目前，我们涵盖了生成整个页面的 CGI。但这并不是 CGI 能做的唯一事情。虽然 CGI 的输出必须包含一个完整的页面——因此你大多数时候可以将 CGI 插入到其他静态页面的中间——但你可以利用一些“服务器技巧”将动态内容引入到另一个页面中。实现此点的简单方法是在你的设置中启用服务器端包含（SSI）。通常，这由你的系统管理员设置。请咨询你的服务提供商（ISP）以查看你是否可以使用服务器端包含。我们包含了一些简单信息，帮助你配置 Apache 服务器来处理 SSI。Apache 不是唯一可以处理 SSI 的服务器。如果你在使用 Apache 以外的服务器并想使用 SSI，你需要检查你的服务器文档或获取更多信息。

## 第 6 章 自定义页面

random_img.cgi (续)

```perl
# 将图像文件句柄设置为二进制模式，因为我们
# 正在读取一个二进制文件
binmode(IMGD);

# 清除换行符，这样我们就可以
# 一次性读取图像文件，但仅在此代码块内。
{
    local $undef=undef;
    print <IMGD>; # 读取并输出图像文件
}

# 清理后续工作
close IMGD;
```

当然，如果你愿意，可以使用 SSI 代替自己加载图像。SSI 比 CGI 更加方便，也不那么复杂，但如果没有一个熟练的管理员来配置服务器以避免安全问题，它的安全性可能会稍低。

要使用 SSI 版本的随机图像：

# rand_img_name.cgi

```perl
#!/usr/bin/perl

# 打印 http 报头——在这种情况下是一个图像
print "Content-type: text/plain\n\n";
$IMAGE_DIR = 'images'; # 我们存储图像的目录

# 打开图像目录，或者输出错误，该错误将出现在
# apache 的错误日志中。变量! 包含了系统
# 错误消息。
opendir(IMGD, $IMAGE_DIR) || die "Could not open image dir: $$";
@images = grep ( /\.jpg$/ && -r "$IMAGE_DIR/_" ) readdir IMGD;
closedir IMGD;

$img_num = int(scalar(@images));
$img_file = "$IMAGE_DIR/" . $images[$img_num];

print $img_file;
```

## Perl网站工作坊

# 全家桶 (The Whole Kit 'n' Kaboodle)

这是一个使用了之前所有脚本的 Web 示例。我们在图 6.4 中提供了随机结果的截图。

ssi_test.shtml

```html
<html>
<head><title>SSI 测试页面</title></head>
<body>
<h1>SSI 测试页面</h1>
<p>
显示日期：<!--#include virtual="echo_date.cgi" -->
</p>
<p>
最后修改时间：<!--#include virtual="last_mod.cgi" -->
</p>
<p>
随机引言：<br/>
<!--#include virtual="fortune.cgi" -->
</p>
<p>
<img src="<!--#include virtual="rand_img.cgi"-->">
</p>
一张来自 SSI 的随机图像。
<p>
<img src="random_img.cgi">
</p>
一张图像数据来自 CGI 的随机图像。
</p>
<p>
Perl 环境变量值：<!--#include virtual="print_env.cgi" -->
</p>
</body>
</html>
```

## 第 6 章 自定义页面

113

![](img/d26997dc0c0571017b4729525ba1a4ac_121_0.png)

图 6.4

在这张图中，我们展示了“Whole Kit 'n' Kaboodle”示例的顶部结果：日期、修改日期、一段随机引言和一张随机图像。

## 接下来是什么

是时候娱乐一下了！第 7 章“趣味与游戏”将提供一段轻松且愉快的旅程，通过这些脚本让你能够使用 Perl 进行娱乐和游戏。当然，我们的疯狂是有方法的的：在我们真正用更激进的 Perl 脚本对你进行考验之前，先给你这段娱乐休息。

## 趣味与游戏

每个人偶尔都需要休息一下，本章将向你展示如何为访客提供急需的放松（RtR）。当然，尽管你使用所有这些脚本是为了玩，但它们也可以用于严肃的原因。

我们将查看两个脚本，这些脚本允许你使用 GD 显示时间和页面访问点击量。GD 是一个 Perl 接口，允许你绘制图形并使用线条、形状和文本。

然后，我们将转向一个兼具趣味性和功能的交互式脚本：用户投票。该脚本允许你根据自己的内容为访客提供一个多项选择列表。该脚本会记录票数，然后用美观的柱状图显示结果。无论是大都市风格的爱情投票，还是严肃的政治民意调查，只要你想为你的网站增加交互性，这个脚本都非常好用。

最后，我们将向你展示如何创建广受欢迎的“吊字游戏”（Hangman）。它比本章中的其他脚本稍微复杂一点，你会发现 Perl 不仅可以用于为用户创建交互界面，还可以在后台智能地存储信息。

## 显示时间

如果你想在页面上添加一个数字时钟，可以使用此 CGI 程序。它利用了 GD，一个用于图形的 Perl 接口。GD 可能已经存在于你的服务器上，但如果没有，访问 CPAN 将帮助你获取该模块。

Unisys 是 GIF 及其他文件格式使用的 LZW 压缩专利的所有，使用了 GD 的作者。现在 GD 只能生成 .png 或 .jpg 文件。由于许多浏览器无法渲染 .png 文件，我们将使用 .jpg 文件。

## 如何使用

1. 将 `clock.cgi` 代码复制到你的文本编辑器。
2. 设置 GD 所在库的路径。
3. 创建一个 HTML 页面来包含计数器。
4. 将文件上传到你的服务器。

```perl
#!/usr/bin/perl

use lib '/path/to/library';
use GD;
use POSIX;

$img = new GD::Image(200, 100);

$black = $img->allocate(0, 0, 0);
$green = $img->allocate(0, 200, 255);

$img->fill(0, 0, $black);
$readout = strftime("%H:%M:%S", localtime(time));

$img->font($green, $black, 10, 10, $readout);

print "Content-type: image/jpeg\n\n";
print $img->image;
```

## Perl网站工作坊

## 其他文件

```html
<html>
<head>
<title>这是什么？</title>
</head>
<body>
<div align="center">
<img src="counter.cgi">
</div>
</body>
</html>
```

## Perl 网站工作坊

将代码保存为 `counter.cgi` 并将其上传到你的 `cgi-bin` 目录。

完成后，为该文件设置权限：`chmod a+x counter.cgi`。

```perl
#!/usr/bin/perl

$| = 1;   # 脚本不缓冲

use lib '/path/to/library';
use GD;
use SDBM_File;
use Fcntl;

struct;
use vars qr(@HOSTS_ALLOW @DIRS_ALLOW)
    ($FIGURES $FONT $STATS @BG @FG);

# # 引用页面必须来自这些主机之一
@HOSTS_ALLOW = ('www.yourhost.com');   # 设置为你的主机

# 引用页面必须在这些目录之下
# 路径不要以 / 开始
@DIRS_ALLOW = ('');   # 留空表示所有
# 计数器尺寸
$FIGURES = 6;
$FONT = ggdiantFont;
$STATS = '/path/to/stats';   # 统计 SDBM 文件路径
@BG = (0, 0);                # 背景色
@FG = (50, 200, 255);         # 数字颜色

main();

sub main {
    my ($img, $x_size, $y_size, $string,
        $ref, $stats, $count, $bg);

    # 根据所选字体计算图像大小
    $x_size = $FONT->width * $FIGURES + 4;
    $y_size = $FONT->height + 2;
    $img = new GD::Image($x_size, $y_size);

    $bg = $img->colorAllocate(@BG);
    $bfg = $img->colorAllocate(@FG);

    $img->fill(0, 0, $bg);

    # 谁在调用？
    $ref = $ENV{'HTTP_REFERER'};

    if (allowed_page($ref)) {
        tie(%stats, 'SDBM_File', $STATS, O_CREATE|O_RDWR, 0666)
        || die "连接失败: $!";
    }
```

counter.cgi (续上)

```perl
$stats($ref)++;
$count = $stats($ref);
untie $stats;

# 创建字符串，在前面填充 '0'
$string = '0' x ($FIGURES . length("$count")) . $count;

# 将字符串添加到图像
$img->string($FONT,2,1,$string,$cfg);

# 输出到浏览器
binmode STDOUT;
print "Content-type: image/gif\n\n", $img->gif;

}

nsub allowed_page {
    my $ref = shift;

    my ($Host, $path, $h_ok, $p_ok);

    if ($ref = m|http://([^/]+)/(.*)|i) {
        $Host = $1;
        $path = $2;
    }

    $h_ok = $p_ok = 0;

    foreach my $h (@HOSTS_ALLOW) {
        if ($h =~ /\$Host$/) {
            $h_ok = 1;
            last;
        }
    }

    foreach my $p (@DIRS_ALLOW) {
        if ($path == m|\$p$/) {
            $p_ok = 1;
            last;
        }
    }

    return ($h_ok && $p_ok);
}
```

# 其他需要的文件

与 `clock.cgi` 一样，你需要一个 HTML 文档，在其中添加计数器的调用。你可以使用网站内的任何文档，甚至可以使用多个！但我们建议只用一个——通常是你的入口页。

你需要配置计数器本身以防止他人恶意刷取。将允许的主机设置为包含你的 Web 服务器名称，并将允许的目录设置为包含你放置计数器的目录（即你的入口页——除非你有特殊理由在网站的其他页面使用该脚本）。

1. 打开你的文本或 HTML 编辑器。
2. 打开或你要放置计数器的 HTML 文档。
3. 使用 `<img>` 标签添加指向脚本的链接：`<img src="/cgi-bin/counter.cgi">`
4. 将 HTML 页面（或页面）上传到服务器上的目录。
5. 测试你的页面！你的结果应该和我们的相似（见图 7.2）。

# 图 7.2

计数器将统计你的页面接收到的点击次数。

![](img/d26997dc0c0571017b4729525ba1a4ac_128_0.png)

clock.cgi 的 HTML 文档示例

```html
<html>
<head>
<title>Molly's Way Web Page</title>
</head>
<body bgcolor="#000000" text="#FFCC99" link="#FF9993" vlink="#CC6633" alink="#FF9993">
```

# 第 7 章 趣味与游戏

clock.cgi 的 HTML 文档示例（续上）

```html
<blockquote>

<font face="arial, helvetica, sans-serif">
<p>
嘿，大家好！
<br/>
</p>
欢迎来到我的酷炫网页。请务必到处看看，我一直在添加新内容。另外，不要犹豫，<a href="mailto:molly@molly.com">给我写封邮件</a><a href="index.html">前往下一页</a>。</p>
<p>
<a href="index.html">前往下一页</a>。</p>

<div align="center">
<img src="/cgi-bin/counter.cgi">
</div>
</font>
</body>
</html>
```

需要时使用计数器。它们很有趣，但资深冲浪者觉得它们很烦。此外，最好的统计直接来自你的服务器，它可以为你提供关于访问网站人数的大量准确信息。

# 用户投票

人们喜欢参与投票。所有网站都能受益，无论是为了纯粹的娱乐（见图 7.3），还是为了表达特定的观点。

## 如何使用

要设置你的投票功能，你首先需要在 `cgi-bin` 目录中安装 `quickpoll.cgi`。然后你创建几个投票，并由 CGI 使用。本质上，这种关系非常直观：网站访问者在投票页面输入答案并提交。投票脚本随后过滤输入，决定如何处理它。完成汇总并返回给访问者的任何信息，结果将以条形图或其他布局发送到浏览器。

图 7.3 疯狂饼干投票。

![](img/d26997dc0c0571017b4729525ba1a4ac_130_0.png)

设置投票：首先在 hdocs 树之外创建一个投票目录。然后对于每个投票，在投票目录中创建一个以投票命名的子目录。例如，投票目录为 `/home/molly/dolls`，我们的第一个投票位于 `/home/molly/dolls/cookie`。让每个投票目录变为全局可写（见第 3 章“脚本基础”），并在每个目录下放入一个名为 `poll.conf` 的自定义文件。你的目录结构看起来像：

```
polls/
  poll.conf
  votes
poll2/
  poll.conf
  votes
```

`poll.conf` 是你的文本文件，`votes` 是管理投票的 DBM（数据库文件）。`poll.conf` 的格式简单：

poll.conf

Q: 哪种饼干最好吃？

A: 薄荷味

A: 橙子味

A: 双巧克力味

A: 牛奶味

# 描述

谁喜欢饼干？当然，你可以（也应该！）修改 `poll.conf` 文件以包含你想要的任何问题和答案。CGI 脚本有点长，我们将分部分处理。从标准的安全设置和捕捉任何脚本错误的 `eval` 块开始。

quickpoll.cgi

```perl
#!/usr/bin/perl

$ENV{'PATH'} = '/bin:/usr:/usr/local/bin';
$ENV{'SHELL'} = '/bin/sh';
$ENV{'ENV'} = '';
$ENV{'IFS'} = '';

use lib '/path/to/library';
use Taintcheck;

use CGI;
use CGI::FastTemplate;
use SDBM_File;
use Fcntl;

use strict;
use vars qw($CGI $DIR $POLL_DIR $TMPL_DIR);

# 全变量

$CGI = 'quickpoll.cgi';
$POLL_DIR = '/path/to/polls/';  # 投票目录路径
$TMPL_DIR = '/path/to/templates/';  # 模板路径

# 主程序
```

quickpoll.cgi (续上)

```perl
eval { main(); };

# 错误处理

if ($@) {
    print "Content-type: text/html\n\n";
    print "出错: $$";
}
```

让我们看看 `main` 函数。这基本上是一个分发器，根据脚本输入决定显示选票、记录投票还是显示投票结果。

```perl
sub main {
    my $q = new CGI;
    my ($do, $polls, $page);

    die "$CGI 无输入" unless $q->param;

    # 检查输入
    &untaint_params($q);

    # 构建 POLL_DIR 中的投票列表
    $polls = get_polls($POLL_DIR);

    # 为了方便
    $do = $q->param('do');
    $poll = $q->param('poll');

    # 确保投票项存在
    die "未知投票 ($poll)" unless exists($polls{$poll});

    # 处理不同的操作
    if ($do == 'vote') {
        record_vote($q,$poll);
        $page = show_results($q,$polls{$poll});
    } elsif ($do == 'results') {
        $page = show_results($q,$polls{$poll});
    } else {
        $page = show_ballot($q,$polls{$poll});
    }

    print $q->header, $page;
}
```

# 第 7 章 趣味与游戏

记录实际投票是脚本中最简单的部分。`tie` 让变得简单：我们只需根据投票值增加 DBM 记录。

```perl
sub record_vote {
    my $Sq = shift;
    my $spoll_name = shift;
    my %votes;

    # 连接存储投票的 DBM 文件
    tie (%votes, 'SDBM_File',
            "$POLL_DIR/$spoll_name/votes", 0_CREATE|O_RDWR, 0666)
            || die "无法写入 $POLL_DIR/$spoll_name";

    # 增加投票
    $votes($Sq)->param('vote')++;

    # 保存到磁盘
    untie %votes;
}
```

```perl
sub show_results {
    my $Q = shift;
    my $spoll = shift;

    my ($spoll_name, \$tpl, \$votes, \$total,
        \$answer, \$num, \$pct, \$block, \$sp);

    # 条形图中每个百分比占用的像素
    $block = 2;
    $spoll_name = $Q->param('poll');

    $tpl = new CGI::FastTemplate;
    $tpl->set_root($TMPL_DIR);

    # 获取结果模板
    $tpl->define('results', 'quickpoll_results.html' );

    # 结果行
    $tpl->define('rows', 'quickpoll_row.html' );
}
```

## Perl 网站工作坊

```perl
# 获取投票总数
for $sa(0..$poll->{'ANSWERS'}) {
    $total += $votes($sa);
}
```

```perl
# 构建行，每个答案对应一个行
for $sa(0..$poll->{'ANSWERS'}) {

  $Answer = $poll->{'ANSWERS'}->[$sa];
  $num = $votes($sa) || 0;
  $pct = 0;
}
```

```perl
# 注意防止除以 0错误！
($total) && ($pct = int($num/$total) * 100);

$tpl->assign('ANSWERS' => $answer,
             'NUM' => $num,
             'PCT' => $pct,
             'WIDTH' => ($pct * $block) + 1);
```

```perl
$tpl->parse('ROWS' => '.rows');
```

```perl
# 以及主页面
$tpl->assign($poll);
$tpl->parse('MAIN'=>'results');
```

```perl
$p = $tpl->fetch('MAIN');
```

```perl
if (($p) && ($sp)) {
    return $sp;
}
```

要获取任何投票，你需要显示选票列表。我们再次使用 `CGI::FastTemplate` 来方便地自定义选票页。

```perl
sub show_ballot {
    my $q = shift;
    my $poll = shift;
    my ($tpl, $answers, $sp) = new CGI::FastTemplate($q);
    $tpl->set_root($ENV{STMPL_DIR});
```

```perl
$tpl->define('ballot', for $poll->{'ANSWERS'}) {
    $answers .= "<input type='radio' 
        name='\$vote' value='\$a\'>" " . $poll->{'ANSWERS'}->[$a] . "<br>\n";
}
```

## 第7章 趣味与游戏

```perl
# 将 HTML 代码保存到变量中
# 该变量将出现在模板中
$poll->{'ANSWERS'} = $answers;
$poll->{'POLL'} = $q->param('poll');
```

```perl
$tpl->assign( poll );

$tpl->parse( 'MAIN' => 'ballot' );

$p = $tpl->fetch('MAIN');
```

```perl
if (($sp) && ($sp)) {
  return $sp;
}
```

我们还需要处理一些“簿记工作”——从 `polls` 目录读取各种 `poll.conf` 文件，以便我们知道每个投票需要提问哪些问题。

# POLL_DIR 包含其他目录，每个目录

# 对应一个投票。这些目录中有两个

# 文件：一个是普通的文本文件 poll.conf，另一个是

# DBM 文件 votes。

```perl
sub _get_polls {
  my $dir = shift;
  my (@dirs, %polls);

# 获取 poll 目录中的子目录
opendir(PLDR, $dir) || die "Could not open poll dir $dir";

# 使用 grep 从 $dir 内容中筛选出目录，排除
# 以点（.）开头的目录；并从中筛选
# 仅包含 poll.conf 文件的目录
@dirs = grep { 
  (-d "$dir/$_") 
  && 
  (!/\.\/)) 
  && (-r "$dir/$_/poll.conf") } readdir PLDR;

closed(PLDR);

# 构建投票名称 => 投票配置的哈希
foreach my $sd(@dirs) {
  $polls($sd) = read_poll_conf("$dir/$sd");
}

return $polls;
}
```

```perl
sub read_poll_conf {
  my $dir = shift;
  my (%CONF,$fld,$val,$Stmp);

  open (CONF, "$dir/poll.conf")
  || die "Could not read $dir/poll.conf";

  while (<CONF>) {
    chomp;
    next if /#/;      # 跳过注释
    next if /\s*$/    # 跳过空行

    # 问题以 Q: 开始，且只有一个
    if (/\Q.*?:\s*(.*)/) {
      $conf{'QUESTION'} = $1;

    # 答案以 A; 开始，可以有多个
    } elsif (/\A.*?:\s*(.*)/) {
      $Stmp = $conf{'ANSWERS'};
      $Stmp = [];
      push @Stmp, $1;
      $conf{'ANSWERS'} = [@$Stmp];

    # 其他任何内容都是可选描述的一部分
    else {
      $conf{'DESCRIPTION'} .= $&;
    }
  }

  die "Bad poll conf"
  unless ($conf{'QUESTION'} && ($conf{'ANSWERS'}));

  return $conf;
}
```

哇！这太棒了！现在你将为投票的界面创建一些 HTML 模板。

首先，让我们创建选票模板表单。

```html
<html>
<head><title>大 Cookie 投票</title></head>
<body>

<p>$QUESTION<br></p>
<p>
<form action="/cgi-bin/quickpoll.cgi" method="post">
<input type="hidden" name="do" value="poll"/>
<input type="hidden" name="poll" value="$POLL"/>
$ANSWERS
</p><input type="submit" value="投票"></form>

</body>
</html>
```

修改此文件以匹配你的设计、颜色以及任何字段。现在让我们创建结果模板。

```html
<html>
<head><title>投票结果</title></head>
<body>
<p>$QUESTION</p>
<table>
$ROWS
</table>
</body>
</html>
```

```html
<tr>
<td>$ANSWER</td>
<td><img src="blue.gif" height="12" width="$PCT" align="left">($PCT%)</td>
</tr>
```

此模板将包含每个答案的行。

哇！这太棒了！现在你将为投票的界面创建一些 HTML 模板。

首先，让我们创建选票模板表单。

```html
<html>
<head><title>大 Cookie 投票</title></head>
<body>

<p>$QUESTION<br></p>
<p>
<form action="/cgi-bin/quickpoll.cgi" method="post">
<input type="hidden" name="do" value="poll"/>
<input type="hidden" name="poll" value="$POLL"/>
$ANSWERS
</p><input type="submit" value="投票"></form>

</body>
</html>
```

除以 0 错误保护！这以 7.4 章节展示了 状态的概念：保存状态。该脚本展示了 CGI 中一个非常重要的技术。参见第 6 章节了解关于 SSI 的更多信息。

7.4 吊诡游戏。

如何使用：

1. 下载脚本。注意我们要将脚本放在服务器上的适当目录。为 `hangman.cgi` 设置执行权限。
2. 创建单词列表文件。每行一个单词，并注意拼写！
3. 创建构建吊诡所需的各个图像。

hang_words.txt

```text
chihuahua
ostrich
chimp
cookie
weasel
plastic
bonus
scissors
dynamite
```

hangman.cgi

```perl
#!/usr/bin/perl -wT

$| = 1; # 不缓冲输出

$ENV{'PATH'} = '/bin:/usr/bin:/usr/local/bin';
$ENV{'SHELL'} = '/bin/sh';
$ENV{'ENV'} = '';
$ENV{'IFS'} = ' ';

use lib '/path/to/library';
use Taintcheck;

use CGI;
use DBD::File;
use Fontl;
use FreezeThaw(freeze thaw); # 将游戏状态存储到 DBM 文件中

use strict;
use vars qw($CGI START $WORDS SESSIONS $GALLOWS $BODY_PARTS);

# 全局变量
$CGI = 'hangman.cgi';
$WORDS = '/path/to/words';      # 你的单词文件
$SESSIONS = '/path/to/games';      # 游戏会 dbm
$GALLOWS = '/path/to/gallows/images';  # 吊诡图像
$BODY_PARTS = 7;                    # 图像数量

# 主
eval(main()); $START = LINE;

# 错误
if ($0) {
  chomp($0);
}
$0 = s/\(eval\) line(\d+)\(CGI)\s - line . ( $START -$1)/e;
$0 = s/( at).*( line)/\$(CGI)\$2//;

$error_message = $0;

print <<<ERR;
Content-type: text/html

<html>
<head><title>Error</title></head>
<body>
<h1>Error</h1>
<code><code>$error_message</code></body>
</body>
</html>
ERR
}
```

# 第 7 章 游戏与娱乐

```perl
# 子程序
sub main {
my $q = new CGI;

ununaint_params($q);

my $game;

# 没有输入？必须开启一个新游戏
unless ($q->param) {
  new_game($q);
  return;
}

# 我们也想提供一种开始新游戏的方式
# 显式！
if ($q->param('submit') = /new_game/i) {

  $q->delete_all($q); # 清空所有参数
  &new_game($q);
} elsif ($q->param('session_id')) {

  # 尝试恢复之前的游戏状态
  die "游戏过期或错误: " .
    ($q->param('session_id'))
  "). 请开始一个新游戏。"
  unless ($game = restore_game($q->param('session_id')));

  continue_game($game,$q);
} else {

  # 发生了错误 - 可能是输入无效
  die "未提交游戏 ID。请开始一个新游戏。"
}
```

恢复游戏相当简单。游戏状态存储在 DBM 文件中的一条记录中，这使得我们能够快速检索到完整记录。当然，我们必须知道记录键（在这种情况下，我们将其设置为游戏会话 ID）。

游戏记录的格式留给另一个名为 `FreezeThaw` 的模块来处理。我们使用 `FreezeThaw` 是因为我们无法直接将作为游戏记录的哈希表（hash）存储在 DBM 数据库中。只有标量值（字符串或数字）可以作为 DBM 键和记录使用。`FreezeThaw` 将复杂的 Perl 数据类型转换为字符串，然后再转换回来，因此它可以让我们轻松使用我们想要的数据格式，而无需担心以字符串格式存储并再次读取的琐碎细节。

## Perl 网站工作坊

FreezeThaw 不是标准 Perl 分发版的一部分，因此你必须从 CPAN 下载并安装它。

```perl
# restore_game
# 根据给定的 session id，从 DBM 文件
# 加载会话记录并恢复游戏状态
sub restore_game {
    my $id = shift;
    my (%sessions, %game);

    return unless $id;

    tie($sessions, 'DBM_File', $SESSIONS, O_RDONLY, 0666)
    || die "无法打开游戏会话数据";

    return unless $sessions($id);
    %game = thaw($sessions($id));

    return ($game{'word'} && $game{'status'});
    return \%game;
}
```

一旦游戏状态恢复，我们就必须更改它以反映玩家的下一步，并再次保存。`FreezeThaw` 保存游戏状态变得非常简单，但从旧状态计算新状态则有些复杂。

如果玩家进行了一个新的猜测，我们需要弄清楚她是猜对了还是猜错了，以及她是赢了还是了。如果她没有猜测，或者她正在继续一个刚刚开始的游戏，我们只需要向她发送显示当前状态的屏幕。

```perl
# continue_game
# 将新猜测添加到猜测列表中，
# 保存新的游戏状态并生成
# 正确的输出页面
sub continue_game {
    my $game = shift;
    my $q = shift;
}

my ($id, $tmp, $game);

eval {
    if ((ref $q) && ($q->param)) {
        if ($q->param('guess')) {
            $g = $q->param('guess');
```

```perl
# 这里是另一种方法来判断
# 一个值是否是数组的成员
$tmp = join(';', @($game->{'guesses'})) . ':';
die '你已经猜过 $g!' if ($tmp = / /$g/i);
push($game->{'guesses'}, $g);
```

```perl
# 现在是有趣的部分 —— 我们是赢了、输了、
# 还是不匹配？
$game->{'status'} = take_turn($game);
```

```perl
# 保存状态以备下次使用
save_game_state($q->param('session_id'),$game);
```

```perl
# 输出结果
draw_game_page($q,$game);
```

```perl
else {
```

```perl
# 没有任何猜测，只是回显上一页
draw_game_page($q,$game);
```

```perl
}
```

```perl
else {
$id = save_game_state(undef',$game);
draw_game_page($q,$game,$id);
}
```

```perl
;
```

```perl
if ($@) {
chomp($@);
gameplay_error($q,$@);
}
```

保存游戏是恢复的对面，而且同样简单——尽管这就像开始一个完全全新的游戏一样简单。

```perl
sub save_game_state {
my $session_id = shift;
my $game_state = shift;
my (%sessions);
```

```perl
tie(%sessions, 'SDBM_File', %SESSIONS, O_CREATE|O_RDWR,
|| die '打开游戏会话数据失败';
```

```perl
unless ($session_id) {
$session_id = time;
```

```perl
while ($sessions($session_id)) {
$session_id++;
}
```

```perl
$sessions($session_id) = freeze($game);
untie %sessions;

return $session_id;
}
```

```perl
# new_game
# 从 DBM 文件中
# 选择一个记录并生成新的游戏状态
sub new_game {
    my $q = shift;
    my %game;

    $game{'word'} = generate_word();
    $game{'status'} = 'playing';
    $game{'guesses'} = [];

    my $id = save_game_state(undef,$game);
    draw_game_page($q,$game,$id);
}
```

```perl
# generate_word
# 生成一个随机单词
sub generate_word {
    my @words = qw(apple banana cherry date elder fig);
    return $words[rand @words];
}
```

```perl
# take_turn
# 处理玩家的猜测
# 更新游戏状态
sub take_turn {
    my $game = shift;
    # ... 逻辑实现 ...
    return $game;
}
```

# 第 7 章 趣味与游戏

```perl
if ((length($sg) != 1) && ($game->{'word'} =~ /$sg/i)) {
    push $tmp, '<font color=darkgreen$g</font>';
} else {
    push $tmp, '<font color=red$g</font>';
    $Sparts++;
}
```

```perl
$guesses = join(',', @$tmp);

# 告诉玩家最后一次猜测
# 是对是错
$sg = $game->{'guesses'}[#{$game->{'guesses'}}];
$msg = "最后一次猜测: ";
```

```perl
if ((length($sg) == 1) && ($game->{'word'} =~ /$sg/i)) {
    $msg = "<b><font color=darkgreen$g</font></b>";
} else {
    $msg = "<b><font color=red$g</font></b>";
```

```perl
# 绘制单词，用 ""
# 表示未猜测的字母
$tmp = ':' . join(',', @($game->{'guesses'})) . ':';
```

```perl
# 检查单词是否已被猜测
if ($tmp != /$$game->{'word'}/) {
    $word = join(" ", split(//, $game->{'word}));
} else {
```

```perl
# 逐字符遍历单词，
# 检查每个字母是否被猜测

my @word = split(//, $game->{'word'});
foreach $char(@$word) {
    $char = uc($char);

    if ($tmp != /$$char/i) {
        $word .= " " . $char;
    } else {
        $word .= " _ ";
    }
}
} else {

# 这是他们的第一次回合
```

```perl
$title = "欢迎来到吊字猜游戏！";
$guesses = "<i>无</i>";
$length = length($game->{'word'});
$word = " " x x $length;
$turns = 0;
```

## Perl 网站工作坊

```perl
$msg = '';
$parts = 0; # 绞架直到
}
```

```perl
print $q->header;
print <<GAME;
<html>
<head><title>标题</title></head>
<body bgcolor="white">

<h1>$title</h1>

<img src="GALLOWS/gallows_$parts.gif" align="left">
<br>
<p font-size="12">$msg</p>
<p font-size="12"><b>$word</b></p>
<p>目前为止猜测: $guess</p>
<form action="$url" method="POST">
<input type="hidden" name="session_id" id="$id">
<p>下次猜测: <input type="text" name="guess" size="length" maxchars="length"/></p>
<input type="submit" value="猜测!" />
<input type="submit" name="submit" value="新游戏"/>
</form>
</body>
</html>
GAME
}
```

```perl
sub draw_win_page {
    my $q = shift;
    my $game = shift;
```

```perl
my ($word, $turns, $surl, $min);
```

```perl
$word = $game->{'word'};
$turns = scalar @{$game->{'guesses'}};
$surl = $qurl;
$min = (time - $q->param('session_id')) / 60;
```

```perl
print $q->header;
print <<VICTORY;
<html>
<head><title>!</title></head>
<body bgcolor="white">
<h1>恭喜！</h1>

<p>你用 <b>$turns</b> 次尝试就正确猜出了单词 <<b>$word</b>，而且你只花了 <b>$min</b> 分钟！</p>

<p><a href="$surl">点击此处</a>再次游戏。</p>
```

```perl
</body>
</html>
VICTORY

sub draw_loss_page {
    my $sq = shift;
    my $game = shift;
}
```

```perl
my $word = $game->{'word'};
my $url = $sq->url;

print $sq->header;
print <<DEFEAT;
<html
<head><title>你输了！</title></head>
<body bgcolor="white">
<h1>糟糕了！</h1>

<img src="GALLOWS/dead.gif" align="left">
<p>你挂了。单词是：<b>$word</b></p>

<p> <a href="$url">点击此处</a>再次游戏。</p>

</body>
</html>
DEFEAT
```

最后，我们有两个“记账”函数。一个函数从简单格式（下例所示）的文本文件中为每个新游戏选取单词，另一个函数则对诸如两次猜测同一个字母之类的错误显示不同的错误消息。请注意，这些错误消息与程序错误不同。

```perl
sub pick_word {
    my (@words, $word);

    open (WORDS, "$WORDS") or die "无法打开单词文件 $WORDS";
    $words = <WORDS>;
    close WORDS;

    $word = $words[rand @words];

    return $word;
}
```

```perl
sub pick_word {
    my $sq = shift;
    my $game = shift;

# Perl 工作坊

```perl

$url = $sq->url;

$id = $q->param('session_id');

# 告诉玩家最后一次猜测

# 是对是错

$sg = $game->{'guesses'}[#{$game->{'guesses'}}];

$msg = "最后一次猜测: ";

```

```perl

if ((length($sg) == 1) && ($game->{'word'} =~ /$sg/i)) {

    $msg = "<b><font color=darkgreen$g</font></b>";

} else {

    $msg = "<b><font color=red$g</font></b>";

```

```perl

# 绘制单词，用 ""

# 表示未猜测的字母

$tmp = ':' . join(',', @($game->{'guesses'})) . ':';

```

```perl

# 检查单词是否已被猜测

if ($tmp != /$$game->{'word'}/) {

    $word = join(" ", split(//, $game->{'word}));

} else {

```

```perl

# 逐字符遍历单词，

# 检查每个字母是否被猜测

my @word = split(//, $game->{'word'});

foreach $char(@$word) {

    $char = uc($char);

    if ($tmp != /$$char/i) {

        $word .= " " . $char;

    } else {

        $word .= " _ ";

    }

}

} else {

# 这是他们的第一次回合

```

```perl

$title = "欢迎来到吊字猜游戏！";

$guesses = "<i>无</i>";

$length = length($game->{'word'});

$word = " " x x $length;

$turns = 0;

```

## Perl 网站工作坊

```perl

$msg = '';

$parts = 0; # 绞架直到

}

```

```perl

print $q->header;

print <<GAME;

<html>

<head><title>标题</title></head>

<body bgcolor="white">

<h1>$title</h1>

<img src="GALLOWS/gallows_$parts.gif" align="left">

<br>

<p font-size="12">$msg</p>

<p font-size="12"><b>$word</b></p>

<p>目前为止猜测: $guess</p>

<form action="$url" method="POST">

<input type="hidden" name="session_id" id="$id">

<p>下次猜测: <input type="text" name="guess" size="length" maxchars="length"/></p>

<input type="submit" value="猜测!" />

<input type="submit" name="submit" value="新游戏"/>

</form>

</body>

</html>

GAME

}

```

```perl

sub draw_win_page {

    my $q = shift;

    my $game = shift;

```

```perl

my ($word, $turns, $surl, $min);

```

```perl

$word = $game->{'word'};

$turns = scalar @{$game->{'guesses'}};

$surl = $qurl;

$min = (time - $q->param('session_id')) / 60;

```

```perl

print $q->header;

print <<VICTORY;

<html>

<head><title>!</title></head>

<body bgcolor="white">

<h1>恭喜！</h1>

<p>你用 <b>$turns</b 次尝试就正确猜出了单词 <b>$word</b，而且你只花了 <b>$min</b 分钟！</p>

<p><a href="$surl">点击此处</a>再次游戏。</p>

```

```perl

</body>

</html>

VICTORY

sub draw_loss_page {

    my $sq = shift;

    my $game = shift;

}

```

```perl

my $word = $game->{'word'};

my $url = $sq->url;

print $sq->header;

print <<DEFEAT;

<html

<head><title>你输了！</title></head>

<body bgcolor="white">

<h1>糟糕了！</h1>

<img src="GALLOWS/dead.gif" align="left">

<p>你挂了。单词是：<b>$word</b></p>

<p> <a href="$url">点击此处</a>再次游戏。</p>

</body>

</html>

DEFEAT

```

最后，我们有两个“记账”函数。一个函数从简单格式（下例所示）的文本文件中为每个新游戏选取单词，另一个函数则对诸如两次猜测同一个字母之类的错误显示不同的错误消息。请注意，这些错误消息与程序错误不同。

```perl

sub pick_word {

    my (@words, $word);

    open (WORDS, "$WORDS") or die "无法打开单词文件 $WORDS";

    $words = <WORDS>;

    close WORDS;

    $word = $words[rand @words];

    return $word;

}

```

## HTML 模板示例（续）

```html

<body bcolor="#FFFFFF" text="#000000" link="#CC6666" vlink="#993333"

alink="#003300">

<img src="images/pub_hed.gif" width="585" height="19" border=0 alt="header" />

<table border="0" width="585" cellpadding="5" cellspacing="0">

<<tr>

<td valign="top" align="left" width="450">

<p>

<br/>

<img src="images/pub_sub.gif" width="104" height="19" border=0 alt="news &

views" />

</p>

<p>

<font size="4">$HEADLINE</font>

<br/>

<font size="3"><i>$SUBHEAD</i></font>

<br/>

<font size="2"><b>$by AUTHOR</b></font>

</p><p>

$TEXT

<td>

<td valign="top" align="left" width="135" bgcolor="#993333">

<img src="images/lion.jpg" width="121" height="125" border=0 alt="image of lion" />

<font size="2" face="arial, helvetica, sans-serif" color="#FFFFFF">

发现狮子！阅读 <i>news</i> 获取更多信息。

</font>

</td>

</tr>

</table>

</body>

</html

```

在图 8.2 中，你看到的是发布前的模板文件。图片无法显示是因为故事文件必须发布到正确的目录才能选取图片。目前，你看到的是原始模板文件，它独立存在于 template (tmpl) 目录中。

## 第 8 章 使用模板进行设计

### 图 8.2

原始模板文件。

![](img/d26997dc0c0571017b4729525ba1a4ac_157_0.png)

你会看到我们包含了如 `$HEADLINE` 和 `$TEXT` 等变量。当运行模板脚本时，此页面的布局将根据这些变量整合故事信息。这意味着你可以随时上传新故事，运行正确的脚本，新故事就会替换旧故事。

## 创建模板 CGI

我们自动化示例的基础在于创建模板的能力。该脚本以简化的形式封装了本章中模块的工作方式。

## 如何使用

- 从 CPAN 安装 `CGI::FastTemplate` 模块。
- 将 `template.cgi` 复制到你的文本编辑器中。
- 将脚本保存为 `template.cgi`。
- 将文件放置在服务器的根目录中。
- 修改权限以允许所有用户执行：
  `chmod +x template.cgi`

## Perl 网站工作坊

template.cgi

```perl

#!/usr/bin/perl -wT

#

## 我们开启了污染检查（bang 行中的 -T 选项）

## 因此我们需要显式地设置这些环境变量。



## 这是一个安全功能

```perl
${ENV{PATH}} = '/bin:/usr/bin:/usr/local/bin';
${ENV{SHELL}} = '/bin/sh';
${ENV{ENV}} = '';
${ENV{IFS}} = '';

use lib '/usr/home/mololy/perl_lib';
use Taintcheck;
use CGI;
use CGI::FastTemplate;
```

`strict`强制你使用良好的编程实践，例如声明你所有的变量——这会让调试变得容易得多。

```perl
use strict;
use vars qw($_START_ $CGI $TMPL_DIR $STORY_DIR);

$CGI        = 'template.cgi';
$TMPL_DIR  = '/usr/home/mololy/chap_06/templates';
$STORY_DIR = '/usr/home/mololy/chap_06/stories';
```

我们使用`eval`来捕获可能发生的任何错误：

```perl
eval { main() }; $_START_ = __LINE__;
```

如果`eval { main() }`产生了错误，特殊变量`$@`将保存错误信息。

```perl
if ($@) {
chomp($0);
}
```

使用`$_START_`确定发生错误的实际行：

```perl
$0 = s/(eval\) line (\d+)/($CGI) * " . ($_START___LINE__-1)/e;
$0 = s/(at).*(line)/$1($CGI)/$2;

my $error_message = $@;

print <<ERR;
Content-type: text/html
```

## 第 8 章 使用模板进行设计

`template.cgi`（续）

```html
<html>
<head><title>Error</title></head>
<body>
  <h1>Error</h1>
  <code>$error_message</code>
</body>
</html>
```

```perl
ERR

exit(0);
```

### main

```perl
sub main {
  my ($q, $story_ref, $s);

  $q = new CGI;

  untaint_params($q);

  $story_ref = read_story($q);

  print $q->header(
    draw_story($q,$story_ref)
  );
}
```

### draw_story

传入：html 页面，包含故事，带有布局`$q->param('template')`。

```perl
sub draw_story {
  my $q = shift;
  my $story_ref = shift;

  my ($tpl, $tmpl);

  $tmpl = $q->param('template') unless $tmpl;

  die "No template!" unless $tmpl;

  # 在 $TMPL_DIR 中查找 $tpl.tpl 和 $tmpl.html
  # 如果没有找到其中任何一个，则放弃。
  if (-r "$TMPL_DIR/$tmpl") {
    # 我们什么都不需要做
  } elsif (-r "$TMPL_DIR/$tpl") {
    $tmpl .= '.tpl';
  } elsif (-r "$TMPL_DIR/$tpl.html") {
    $tmpl .= '.html';
  } else {
    die "Could not locate template file $tpl in $TMPL_DIR";
  }

  $Stpl = new CGI::Template;
  $Stpl->init($TMPL_DIR);
  $Stpl->define($tpl) || die "Could not define $tpl!";
  $Stpl->assign($story_ref) || die "Could not assign template values: $story!";
  $Stpl->parse(PAGE => "$tpl");

  $page = $Stpl->fetch("PAGE");

  # FastTemplate 不返回值，
  # 所以我们必须自己处理以获取
  # 结果
  die "Could not parse $tpl!" unless $page;

  return $page;
}
```

### read_story

传入：CGI 对象。输出：故事值的哈希引用，例如`HEADLINE => "Man Bites Dog"`、`AUTHOR => "Mike Roy"`、`TEXT => "A man bit a dog..."`。

```perl
sub read_story {
  my $q = shift;
  my %story;
  my ($story_file, $field, $line);

  die "No story submitted!" unless $q->param('story');

  $story_file = $STORY_DIR."$q->param('story');

  # 在 $STORY_DIR 中查找 $story 和 $story.txt
  unless (open (STORY, "<$story_file")) {
    unless (open (STORY, "<$story_file.txt")) {
      die "Could not read story $story_file";
    }
  }

  $story{'story'} = $q->param('story');
  $field = '';

  while ($line = <STORY>) {
    if ($line =~ /^([A-Za-z0-9_]+):\s*(.+)\$/) {
      chomp($line);
      $story($1) = $2;
      $field = $1;
    } elsif ($line eq "\n") {
      $field = '';
    } else {
      if ($field) {
        $story($field) = $line;
      } else {
        $story('TEXT') .= $line;
      }
    }
  }
  close STORY;

  # 进行一些基础 html 转换：将纯文本“段落”转换为 <p> 标签
  foreach $field (keys $story) {
    $story($field) =~ s/\n\n/<p>/g;
  }

  return \%story;
}
```

## 使用模块发布页面

现在我们将查看在发布系统中所需的模块。

### Story::Text 模块

该模块将打开并读取故事文件，并为自动化系统的发布部分做好准备。

#### 如何使用

1. 将模块复制到你的文本编辑器中。
2. 将模块保存为`Text.pm`。
3. 将模块放置在你的 Perl 库目录。由于模块名为`Story::Text`，该模块必须保存在 Perl 库的`Story`目录中。如果你的 Perl 库是`/home/htdocs/lib/perl`，请将模块保存为`/home/htdocs/lib/Story/Text.pm`。

### Story::Text.pm

```perl
package Story::Text;

# 为了安全
$ENV{'PATH'} = '/bin:/usr/local/bin';
$ENV{'SHELL'} = '/bin/sh';
$ENV{'ENV'} = '';
$ENV{'IFS'} = '';

use strict;
use vars qw($AUTOLOAD);

my %fields = (
    'story_file' => undef,
    'story'      => undef,
    'target'     => undef,
    'template'   => undef,
    'title'      => undef,
    'author'     => undef,
    'summary'    => undef,
    'error'      => undef,
);

sub new {
    my $Proto = shift;
    my $file = shift;
    my $Class = ref($Proto) || $Proto;
    my $self = { %fields };
}

bless $self, $class;

# 如果我们无法读取故事，则退出
return unless $self->initialize($file);

sub _initialize {
    my $self = shift;
    my $file = shift;
}

$self->story_file($file);
```

## Perl 网站制作坊

`Story::Text.pm`（续）

```perl
close STORY;

# 执行一些基础 HTML 转换：将纯文本“段落”转换为 <p> 标签
foreach $field(keys $story) {
    $story($field)    s/\n\n/<p>/g;
}

$self->story(\$story);

# 分配其他字段
$self->target($story{'TARGET'}) if ($story{'TARGET'});
$self->template($story{'TEMPLATE'}) if ($story{'TEMPLATE'});

return 1;

sub title {
    my $self = shift;
    if (@_) {
        $self->{'title'} = shift;
        return @_;
    }
    return $self->('title') if ($self->{'title}');
}

if ($self->story->('TITLE')) {
    $self->title($self->story->{'TITLE'});
    return $self->story->{'TITLE'};
}

if ($self->story->('HEADLINE')) {
    $self->title($self->story->{'HEADLINE'});
    return $self->story->{'HEADLINE'};
}

sub author {
    my $self = shift;
    if (@_) {
        $self->{'author'} = shift;
        return @_;
    }
}

if ($self->story->('AUTHOR')) {
    $self->author($self->story->{'AUTHOR'});
    return $self->story->{'AUTHOR'};
}

sub summary {
    my $self = shift;
```

## 第 8 章 使用模板设计

`Story::Text.pm`（续）

```perl
if (@_) {
    $self->{'summary'} = shift;
    return @_;
}

if ($self->story->{'SUMMARY'})) {
    $self->{'summary'}($self->story->{'SUMMARY'});
    return $self->story->{'SUMMARY'};
} elseif ($self->story->{'TEXT'}) {
    # 获取文本的前 20 个单词，
    # 或者到第一个段落结束，以较短为准；
    my ($tmp, $tmp2, $tmp3);
    $tmp = $self->story->{'TEXT'};
    $tmp2 = '';
    $tmp3 = '';

    if ($tmp =~ /(\S+\s){0,20}/s) {
        $tmp2 = $1;
        # 去除任何末尾的空格或标点，
        # 添加省略号
        $tmp2 =~ s/\n//g;
        $tmp2 =~ s[\W]+$/;
        $tmp2 .= '...';
    }

    if ($tmp =~ /(?:<p>\s*)?(.*??)?<p>)/s) {
        $tmp3 = $1;
        # 如果只得到了一个，返回那个
        return $tmp2 if (($tmp2) && ($tmp3));
        return $tmp3 if (($tmp3) && (!$tmp2));
        # 否则，返回两者较短的那个
        if (length($tmp2) < length($tmp3)) {
            $self->summary($tmp2);
            return $tmp2;
        } else {
            $self->summary($tmp3);
            return $tmp3;
        }
    }
}

sub AUTOLOAD {
    $mySelf = shift;
    $myType = ref($self) || ("$self is not an object");
    $myName = \$AUTOLOAD;

$name = s/.*\;//;

unless (exists $self->{$name})) {
```

## Perl 网站制作坊

`Story::Text.pm`（续）

```perl
die 'Can't access '$name' field in object of class $type;
}

if (@_) {
    return $self->{$name} = shift;
} else {
    return $self->{$name};
}

sub DESTROY {
    my $self = shift;
warn 'wrong type' unless ref $self;
}
```

你可以（并且应该！）测试你的故事是否被成功找到并读取。要做到这一点，请在你之前添加的`my $story`行之后添加以下行：

```perl
$story->error if $story->error;
```

## Publisher.pm

这是发布模块。它的职责是构建在`template.cgi`脚本中最初描述的 HTML 页面。`Publisher.pm`从故事中获取数据（例如标题或作者变量），并将它们填充到 HTML 模板中预定义的空中。在`Publisher.pm`构建好 HTML 文件后，它也会保存该文件。

你可以从动态数据轻松发布静态页面，这将提高你网站的响应速度，并减轻 Web 服务器的负载。

### 如何使用

1. 将模块复制到你的文本编辑器中。
2. 将模块保存为`Publisher.pm`。
3. 将模块放置在你的 Perl 库目录中。
4. 现在，打开你想要受此模块影响的脚本。
5. 在脚本顶部添加该行：

```perl
use Publisher
```

在脚本中，添加该行：

```perl
my $p = new Publisher($story);
```

### Publisher.pm

```perl
package Publisher;

# 为了安全见
$ENV{'PATH'} = '/bin:/usr/bin:/usr/local/bin';
$ENV{'SHELL'} = '/bin/sh';
$ENV{'IFS'} = '';

use CGI::FastTemplate;
use strict;
use vars qw($AUTOLOAD);

my %fields = ( 'tpl' => undef,
               'tmpl_dir' => undef,
               'tmpl' => undef,
               'story' => undef,
               'page' => undef,
               'target' => undef,
               'error' => undef);

sub new {
    my $proto = shift;
    my $story = shift;
    my $class = ref($proto) || $class;
    my $self = { %fields };
    bless $self, $class;
    $self->initialize($story);
    return $self;
}

sub _initialize {
    my $self = shift;
    my $story = shift;
    my $tpl = new CGI::FastTemplate;
    $self->story($story);
    $self->tpl($tpl);
}

sub template_dir {
    my $self = shift;
    my $dir = shift;
    my $tpl = $self->$tpl;

$tpl->set_root($dir);

$self->tmpl_dir($dir);
}

sub use_template {
    my $self = shift;
    my $tpl_name = shift;
    my $tmpl_file = shift;

my $tpl = $self->$tpl;
my $std = $self->tmpl_dir;

if ($self->$story) {
$tmpl_file ||= $self->template;
}

unless ($tmpl_file) {
$self->error("Publisher: no template specified ");
return;
}

if (-r "$std/$tmpl_file") {
# 我们不需要做任何事情
elsif (-r "$std/$tmpl_file.tpl") {
$tmpl_file = '.tpl';
elsif (-r "$std/$tmpl_file.html") {
$tmpl_file = '.html';
else
$self->error("Publisher: not locate file '$tmpl_file' in $std");
return;
}

$tpl->define($tmpl_name->$tmpl_file);
$self->tmpl($tmpl_name);
}

sub publish {
    my $self = shift;
    my $story = shift;
    my $tpl = shift;
    my $target_fl = shift;

$story ||= $self->$story;
$target_fl ||= $self->$target;
$tmpl ||= $self->$tmpl;

unless (ref $story) {
$self->error("Publisher: no story specified
```

## 第 8 章 使用模板设计

`Publisher.pm`（续）

```perl
return;
}
unless ($target_fl) {
$self->error("Publisher: no target file specified");
    return;
}
unless ($self->build_page($story,$tmpl)) {
$self->error("Publisher: unable to build page with template $tmpl");
    return;
}
unless ($self->write_file($target_fl)) {
$self->error("Publisher: unable to write file $target_fl");
    return;
}
return 1;

sub build_page {
    my $self = shift;
    my $story = shift;
    my $tmpl = shift;

my $tpl = $self->tpl;
my ($sp,$t);

$t = $tmpl || $self->tmpl;

$tpl->clear_ref();
$tpl->assign($story,$t);
$tpl->parse('MAIN'=>$$t);

$self->page($tpl->fetch('MAIN'));

$sp = $self->page;

if (($sp) && ($$sp)) {
    return 1;
} else {
    $self->error("Publisher: could not build page");
    return;
}
}

sub write_file {
    my $self = shift;
    my $file = shift;
    my $sp = $self->page;
    my ($wf);
```

## Perl 网站制作坊

`Publisher.pm`（续）

```perl
$file ||= $self->$target;

# 如果 $file 是一个目录，
# 写入 $file[$story_file_name].html
if (-d $file) {
    $wf = $self->story->story_file;
    # 从 story_file 中移除路径
    $wf = s|/.*||;
    # 如果没有扩展名则添加
    $wf = s|(\.html)$|$1|;
    # 去除 file 末尾的斜杠
$file = s|/||;
    $file = "$file/$wf";
}

$self->target($file);

unless ($sp) {
$self->error("Publisher: no page to write");
    return;
}

unless (open (PF, "$file
```

## 第 8 章 使用模板设计

`Publisher.pm`（续）

```perl
die "Can't access '$name' field in object of class $type";

if (@_) {
    return $self->{$name} = shift;
} else {
    return $self->{$name};
}

sub DESTROY {
    my $self = shift;
    warn "wrong type" unless $self;
}
```

要实际发布故事，你必须先设置模板目录和要使用的模板。你可以选择性覆盖默认目标文件并创建页面。方法如下：

```perl
$->template_dir( TEMPLATE_DIR ) | die $->error;
$->use_template('MAIN', $template ) | die $->error;
($target) && $->90 || $->target($target);
$->publish90 | die $->error;
```

如果你想为`Publisher`分配另一个故事，或者在创建`Publisher`之前没有设置故事，你可以使用`$->story($story);`分配故事。

## Publisher::pm

此模块是`Publisher.pm`的子类。它允许你将多个故事、两种模板类型合并成单个索引页面。这里的模板比`Publisher.pm`中的严格一些。这是因为许多内容是自动化的，因此每个模板必须包含一个特定字段来处理它。

## Perl 网站工作坊

5. 在脚本顶部，添加该行：

```perl
use Publisher::Index;
```

6. 通过在脚本代码中添加以下内容创建一个`Publisher::Index`对象：

```perl
my $pi = new Publisher::Index;
```

7. 创建若干故事对象，可以使用`Story::Text`或任何`Story`的子类。

8. 使用以下命令将每个故事添加到索引：

```perl
$pi->add_story($story, [url => $story]);
```

9. 设置模板目录，并添加项目模板：

```perl
$pi->template_dir($TMPL_DIR);
$pi->error unless $pi->use_template('page_template', 'page', $IDX_PAGE);
$pi->error unless $pi->use_template('item_template', $IDX_ITEM, 'item');
```

10. 添加目标文件：

```perl
$pi->target($PUB_DIR/index.html);
```

11. 然后你就可以使用以下命令进行发布了：

```perl
$pi->publish();
```

### Index.pm

```perl
# 给定一组故事、一个模板目录以及
# 整个页面和每个索引项目的模板，
# 构建一个包含每个故事摘要的索引。
package Publisher::Index;
```

```perl
# 为了安全
$ENV{'PATH'} = '/bin:/usr/bin:/usr/local/bin';
$ENV{'SHELL'} = '/bin/sh';
$ENV{'ENV'} = '';
$ENV{'IFS'} = ':;';
```

```perl
# 模块
use lib '/usr/local/htdocs/perbook/chap_06';
use Publisher;
use CGI::FastTemplate;
use strict;
use vars qw(@ISA $AUTLOAD);

@ISA = qw(Publisher);
```

```perl
my %fields = ( %tpl
  'tmpl_dir' => undef,
  'item_tpl' => undef,
  'page_tpl' => undef,
  'stories'  => undef,
  'page'     => undef,
  'target'   => undef,
  'error'    => undef, );
```

```perl
sub new {
  my $Proto = shift;
  my $Class = ref($proto) || $proto;
  my $self = ({ $fields });
  bless $self, $class;
  $self->_initialize();
  return $self;
}
```

```perl
sub _initialize {
  my $self = shift;
  my $tpl = new CGI::FastTemplate;
  $self->_tpl($tpl);
}
```

```perl
sub publish {
  my $self = shift;
  my $target_fl = shift;
  my $page_tpl = shift;
  my $item_tpl = shift;

unless ($self->_build_page($page_tpl,$item_tpl)) {
  $self->_error("Publisher: unable to build page with templates $page_tpl $item_tpl");
  return 0;
}

unless ($self->_write_file($target_fl)) {
  $self->_error("Publisher: unable to write file $target_fl");
  return 0;
}

  return 1;
}
```

```perl
sub build_page {
  my $self = shift;
  my $pt = shift;
  my $it = shift;
  my $tpl = $self->tpl;
  my $st = $self->stories;
```

### Index.pm（继续）

```perl
my ($s,$p);

$pt ||= $self->page_tpl;
$it ||= $self->item_tpl;

# 构建用于插入主页的 STORIES
foreach ($s@$st) {
  $tpl->assign('ST_TITLE' => $s->{'story'}-title,
               'ST_URL' => $s->{'url'},
               'ST_AUTHOR' => $s->{'story'}-author,
               'ST_SUMMARY' => $s->{'story'}-summary, );
  $tpl->parse('STORIES' => ".it");
}

# 构建主页
$tpl->parse('MAIN' => $pt);

$self->page($tpl->fetch('MAIN'));

$p = $self->page;

return ($p ne '');

sub use_template {
my $self = shift;
my $tmpl_name = shift;
my $tmpl_file = shift;
my $which = shift;
my $tpl = $self->tpl;
my $td = $self->tmpl_dir;

if (-r "$td/$tmpl_file.tpl") {
    # 我们不需要做任何特殊处理
} elsif (-r "$td/$tmpl_file.html") {
    $tmpl_file .= '.tpl';
} elsif (-r "$td/$tmpl_file.html") {
    $tmpl_file .= '.html';
} else {
    $self->error("Publisher: 在 $td 未找到模板文件 $tmpl_file");
    return;
}

$tpl->define($tmpl_name,$tmpl_file);
$self->{$which}-tmpl} = $tmpl_name;
}
```

### Index.pm（继续）

```perl
sub add_story {
    my $self = shift;
    my $story = shift;
    my $url = shift;
    my %val = (
      'story' => $story,
      'url'   => $url,
    );

    # $stories 是故事数组的引用
    my $tmp = $self->{stories};
    $tmp ||= [];
    $self->stories(@{$tmp}, %val);
    return scalar @{$self->stories};
}

sub AUTOLOAD {
    my $self = shift;
    my $type = ref($self) || die("$self 不是一个对象");
    my $name = AUTOLOAD;
    $name = s/.*//;
    unless (exists $self->{$name}){
        die "无法访问类 $type 中的字段 '$name'";
    }

    if (@_) {
        return $self->{$name} = shift;
    } else {
        return $self->{$name};
    }
}
```

## 其他文件

页面模板包含故事列表变量`STORIES`。

项目模板必须包含：

- `ST_TITLE`（故事标题）
- `ST_URL`（故事 URL）
- `ST_AUTHOR`（故事作者）
- `ST_SUMMARY`（故事摘要）

该模块非常强大。我们将展示如何在第 9 章“创建自己的门户”中使用它进行构建。

### 发布工具

`Publisher`和`Story`模块配合以下工具使用。

#### Publish.pl

此命令行脚本允许你将一个或多个故事发布为 HTML 页面。

1. 将脚本拷贝到编辑器中。
2. 将脚本保存为`publish.pl`。
3. 将脚本放在服务器上。
4. 通过`chmod +x publish.pl`使脚本可执行。

```perl
#!/usr/bin/perl -w

use lib '/path/to/library';
use Publisher;
use Story::Text;
use Taint;
use Getopt::Std;
use strict;

use vars($opt_f $opt_d $STORY $TEMPLATE $TEMPLATE_DIR);

die usage() unless @ARGV;

$STORY = untaint($ARGV[0]);
$TEMPLATE = untaint($ARGV[1]);
$TARGET = untaint($ARGV[2]);
$TEMPLATE_DIR = untaint($opt_d) || '/home/molly/chap_06/templates/';

if ($opt_f) {
  my $s;
  my @stories = read_opts_file($opt_f);
  foreach ($s(@stories) {
    publish_page(@$s);
  }
} else {
  die usage() unless $STORY;
  publish_page($STORY, $TEMPLATE, $TARGET);
}

sub read_opts_file {
    my $file = shift;
    my ($story, $tmpl, @stories);

    # 文件格式为：
    # story [template]
    open (OPTS, "$file") || die 'publish.pl: 无法读取选项文件 $file";
    while (<OPTS>) {
        chomp;
        push @stories, split(/([\s\t]+/, $_);
    }
    close OPTS;
    return @stories;
}

sub publish_page {
    my $story = shift;
    my $template = shift;
    my ($s, $p) = shift;

    $s = new Story::Text($story);
    die "无法读取故事 $story" unless read $s;

    $p = new Publisher($s);
    die "无法为 " . $story->_story_file 创建发布者" unless ref $p;

    $p->template_dir($TEMPLATE_DIR) || die $p->error;
    $p->use_template('MAIN', $template) || die $p->error;

    ($target) && ($p->target($target));

    $p->publish() || die $p->error;
}

sub usage {
  return <<USAGE;
usage:

publish.pl [-d template_dir] story_file [template] [target_file] -f file

使用 -f file 从文件中读取 story/template/target 三元组

USAGE
}
```

### 通过电子邮件发布页面

此 Perl 脚本从电子邮件获取输入，而不是从本地磁盘读取故事。这允许你从远程位置直接将内容添加到你的磁盘中，就像在本地机器上一样。

## Perl 网站工作坊

`Story::Text::Mail.pm`（续）

```perl
use lib '/usr/local/htdocs/perlbook/chap_06';
use Story::Text;
use strict;
use qw(@ISA $AUTOLOAD);

@ISA = qw(Story::Text);

my %fields = (
  'story_msg' => undef,
  'story_file' => undef,
  'target'    => undef,
  'story'     => undef,
  'template'  => undef,
  'title'     => undef,
  'author'   => undef,
  'summary'   => undef,
  'from'      => undef,
  'error'     => undef,
);

sub new {
  my $Proto   = shift;
  my $Smsg    = shift;
  my $Auth_ip = shift;
  my $Auth_end = shift;
  my $Auth_dir = shift;
  my $Pass_phr = shift;
  my $Class  = ref($proto) || $class;
  my $Self  = { %fields };
  bless $self, $class;
  $self->initialize($msg, $auth_ip, $auth_end, $auth_dir, $pass_phr);
  return $self;
}

sub _initialize {
  my $Self      = shift;
  my $Smsg      = shift;
  my $Auth_ip   = shift;
  my $Auth_end  = shift;
  my $Auth_dir  = shift;
  my $Pass_phr  = shift;

  $self->story_msg($msg);
  $self->read_story();

eval { $self->authenticate($auth_ip, $auth_end, $auth_dir, $pass_phr); };

if ($@) {
  $self->{'error'} = "Authentication failed for message ($@):\n\n$msg";
}
```

## 第 8 章 使用模板设计

`Story::Text::Mail.pm`（续）

```perl
return;
}

sub read_story {
    my ($msg,$field,$val,$line,$hed,%story) = shift;

    $msg = $self->story_msg;

    unless ($msg) {
        $self->error('No content in submitted message:\n\n$msg');
        return;
    }

    $field = '';
    $val = '';

    # 剪掉头部，
    # 保存 From: 行
    $msg = s|^(.*?)\n\n||s;
    $Shed = $1;

    if ($hed && $m =~ q/From: (.*?)(?:\\n|)$/m) {
        $story{'FROM'} = $1;
    }

    while ($msg = s|^(.*?)\n||s) {
        $line = $1;
        if ($line =~ /^([A-Z][A-Z0-9_\-]+):\s+(.*?)\/$/) {
            chomp($line);
            # 存储已经构建的任何长字段
            $story->($field) = $val if (($field) && ($val));
            # 现在将工作字段设置为新字段
            # 并将工作值设置为新值
            $field = $1;
            $val = $2;
        }
    } elsif ($line eq ".\n") {
        # 存储旧的工作字段
        $story->($field) = $val if (($field) && ($val));
        # 清空工作字段和值
        $field = '';
        $val = '';
    } else {
        if ($field) {
            $val = $line;
```

## Perl 网站工作坊

`Story::Text::Mail.pm`（续）

```perl
} else {
$story{'TEXT'} .= $line;
}
```

```perl
# 最后，获取最后一个字段
$story{$field} = $val if ($field) && $val;
```

```perl
# 进行一些基础的 html 转换：将纯文本“段落”转换为 <p> 标签
foreach ($field{keys %story}) {
$story{$field} =~ s/\n\n/<p>/g;
}
```

```perl
$self->story(\$story);
```

```perl
# 分配顺序字段
$self->target($story{TARGET}) if ($story{TARGET});
$self->template($story{TEMPLATE}) if ($story{TEMPLATE});
$self->from($story{FROM});
```

```perl
# 在此模块中，story 文件是
# 不是我们从 Story 中读取的文件
# 而是我们一旦完成处理
# 之后想要保存的文件
# story 文本
$self->story_file($story{FILE});
$story{'FILE'} = $story{FILE};
```

```perl
return 1;
```

```perl
sub authenticate {
my $self = shift;
my $auth_ip = shift;
my $auth_send = shift;
my $auth_dir = shift;
my $pass_phr = shift;
```

```perl
my $msg = $self->story_msg;
my $hed;
my ($From, $sender_ip, $pass, $file);
```

```perl
# 移除并处理头部
$msg = s|^(.*)?\n\n||s;
$hed = $1;
```

```perl
# 检查发送者地址是否与提交者列表匹配
if ($hed =~ /^From:\s+(.+)/m) {
$From = $1;
}
```

## 第 8 章 使用模板设计

`Story::Text::Mail.pm`（续）

```perl
} else {
    return;
}

# 这看起来我们正在测试 html 标签，
# 但电子邮件地址有类似的结构 -- 有时
if ($From =~ /([^>]+)>/ {
    $From = $1;
}

# 其他电子邮件地址可能带有
# 括号 -- 将其切掉
$from =~ s/\*/g;

# 现在我们有了地址，检查它
# 是否与授权列表匹配
die "sender not authorized" unless in_list($send);

# 检查最后的 'received from' 行与授权机器列表
if ($msg =~ /\nReceived: \[.*?\](\d+\.\d+\.\d+)?Received: from\)/s) {
$Sender = $1;
} else {
    die "no received line";
}

# 检查 TEXT 中是否存在密码，存在则移除
die "passphrase not in text" unless ($self->story('TEXT')) =~ s/passphrase//g;

# 检查发送者是否在授权列表中
die "sender's not authorized" unless in_list($sender);

# 检查目标文件
$file = $self->target;
die "target file '$file' not in directory" unless in_dir_list($auth_dir,$file);

if ($self->story_file) {
    die "story file " . ($self->story_file) . " not in directory"
    unless in_dir_list($auth_dir,$self->story_file);
}
```

```perl
return 1;
}

# 将 story字段写入 story_file
sub save {
    my $self = shift;
    my $file = $self->story_file;
    my $s = $self->story;
    my ($f,$v);

    return unless open(SAVE, "$file");

    foreach $f (keys %s) {
        $v = $s->($f);
        chomp($v);
        print SAVE '$f: $v\n';
    }

    return 1;
}

sub in_list {
    my $list = shift;
    my $item = shift;

    foreach $i ($list) {
        # 将任何通配符转换为正则表达式
        if ($i =~ /\*/) {
            $tmp = $i;
            $tmp =~ s/\.*/g;
            return 1 if ($item =~ /^\tmp$/);
        }
    }

    return 0;
}

sub in_dir_list {
    my $dirs = shift;
    my $file = shift;
    my $d;

foreach $d(@$dirs) {
    return 1 if ($file = m|\d/);
}

return 0;
```

这里是与模块配合创建电子邮件系统的`epub.pl`脚本。使用此模块和`epub`脚本（见后文）是通过电子邮件方便快速更新网站内容的极佳方法。只需让更新者或作者向你设置的地址发送标准文本格式的邮件，脚本会自动发布 story。

### epub.pl

```perl
#!/usr/bin/perl -WT

# 欢迎改进安全性建议

use lib '/path/to/library';
use Story::Text::Mail;
use Publisher;
use Net::SMTP;
use strict;

vars qw@($IN $NOTIFY $OWNER $RESULT $TMPL_DIR $AUTHORIZED_IP $AUTHORIZED_SENDER $AUTHORIZED_DIR $PASS $SMTP_SERVER);

# 用于通知信息的邮件服务器
$SMTP_SERVER = 'localhost';

# 通知成功或失败的电子邮件
$NOTIFY = 'your@email.com'; # 替换为你的电子邮件

# 创建的文件所有者是谁？
$OWNER = $NOTIFY;

# 模板路径
$TMPL_DIR = '/path/to/templates/'; # 替换为你的模板目录

# 谁允许发布，他们的发布密码，
# 他们允许发送的IP地址，他们可以使用的模板，以及他们允许发布的目录
$AUTHORIZED_IP = ['.'];
$AUTHORIZED_SENDER = ['wm@shakespeare.com']; # 替换为故事作者邮箱
$AUTHORIZED_DIR = ['/path/to/html/files']; # 替换为保存html文件的路径
$PASS = 'cookie cookie cookie, good enough for me';

while (<>) {
  $IN .= $_;
}

eval {
  $RESULT = publish($IN);
};

if ($@) {
  # 将失败消息和信息发送到
# 通知地址
  notify($@);
} else {
  # 将成功消息和信息发送到
# 通知地址
  notify($RESULT);
}

exit(0);

sub publish {
  my $Text = shift;
  my ($s,$sp);

$s = new::Text::Mail($Text,$AUTHORIZED_IP,$AUTHORIZED_SENDER,$AUTHORIZED_DIR,$PASS);

die $s->error if $s->error;

$p = new Publisher($s);

die $p->error unless $p->template_dir($TMPL_DIR);
die $p->error unless $p->use_template('MAIN', $s->template);
die $p->error unless $p->publish();

# 将story文本写入 story_file
$s->save();

# 设置创建文件的所有/权限
chown(getwnam($OWNER),2,3,$p->target,$s->story_file);

return "Story " . ($s->title) . " by " . ($s->target) . " at " . ($s->from) . " @ " . scalar localtime(time);
};

sub notify {
  my $msg = shift;

my $smtp = Net::SMTP->new($SMTP_SERVER);
```

## 第 8 章 使用模板进行设计

`epubish.pl`（续）

```perl
die "SMTP server not responding" unless ref $smtp;
die "Server did not accept sender's address unless $smtp->mail('publisher');
die "Server did not accept recipient address" unless $smtp->to($NOTIFY);

unless ($smtp->data( "To: $NOTIFY\n"
  "Subject: Publisher result"
  "In"
  $msg
  "In---\nubmitted story follows:\n\n" $IN )) {
$smtp->quit;
die "Failed to send mail";
}

$smtp->quit;
```

您的管理员需要访问并完成服务器端的相关工作，包括：

虽然`epubish`的概念很简单，但真正的挑战在于正确配置服务器。

- 确保机器上正在运行 sendmail。
- 必须恰当地地编辑 sendmail 别名映射文件。
- 管理员必须愿意接受运行 root 脚本作为接收邮件方法所涉及的安全风险。

这并不意味着`epubish.pl`脚本是不安全的。你只需要一位非常清楚自己在配置什么，并且细致精确的人。Sendmail 特别复杂，关于这个主题已经有很多书籍著作了。

## 小心设置 epubish.pl

要设置 sendmail 部分，请前往`/etc/aliases`，并添加类似`publisher: "|/path/to/epubish.pl",`的行。

现在，保存文件，然后运行`newaliases`使 sendmail 识别新的别名。设置`epubish`，将其设置为 SUID root（以 root 身份输入`chmod +sx epubish.pl`），并编辑脚本顶部的变量以设置授权系统以匹配您的站点。将`$AUTHORIZED_IP`设置为允许接收消息的 IP 地址列表。

## Perl 网站工作坊

对于此列表中放入的内容，极其小心至关重要。此列表中任何目录中的任何文件都可能被任何足够聪明伪造电子邮件地址的人随时覆盖，因此我们敦促您务必小心。

这与邮件头中的最后一条`Received From:`行相比，如果您从客户端机器使用 POP 邮件，您将需要添加所有客户端机器的 IP，而不是邮件服务器的 IP。对于`$AUTHORIZED_SENDER`，添加您将接受消息的完整电子邮件地址。对于`$AUTHORIZED_DIR`，列出您允许创建文件的目录列表。

现在，将`$PASS`设置为某些晦涩（但与您相关）的短语。这是最后的防线——每个提交的故事必须在`TEXT`字段的某处包含大括号`{}`包中的`$PASS`（它在处理过程中会被剥离）。

最后，将`$NOTIFY`设置为网站管理员的电子邮件地址，或其他应被通知站点更改的人员。该地址将收到所有指向`epub.pl`的成功和失败提交通知。

如果您一切都做得当，您应该拥有一种安全且强大的方法直接通过电子邮件更新您的站点。

## 发布整个目录

`publish_dir.pl`脚本是另一个用于更新的有用脚本。该脚本将整个故事目录发布到目标目录，并发布一个独立的目录页面。该页面包含每个故事的标题和作者，提供故事摘要，并自动生成从目录到每个故事的链接。

### 如何使用

1. 将脚本复制到您的文本编辑器中。
2. 将脚本保存为`publish_dir.pl`。
3. 将脚本放在服务器的根目录中。
4. 赋予用户对脚本的可执行权限：

```bash
chmod u+x publish_dir.pl
```

## 第 8 章 使用模板进行设计

### publish_dir.pl

```perl
#!/usr/bin/perl -w

use lib '/path/to/library';
use Story::Text;
use Publisher;
use Publisher::Index;
use Cwd;
use Getopt;
use strict;

use vars qw($opt_p $opt_i $TMPL_DIR $DEFAULT_TMPL $STORY_DIR $PUB_DIR $IDX_PAGE $IDX_ITEM $WWW_ROOT);

getopt('pi');

$WWW_ROOT = '/usr/home/molly/public_html';
$TMPL_DIR = '/usr/home/molly/chap_06/templates/';
$DEFAULT_TMPL = 'green';
$STORY_DIR = full_path($ARGV[0]);
$PUB_DIR = full_path($ARGV[1]);
$IDX_PAGE = $opt_p || 'ix_page';
$IDX_ITEM = $opt_i || 'ix_item';

die usage unless $STORY_DIR;

publish_dir($STORY_DIR);

sub publish_dir {
    my $dir = shift;
    my (@files, @stories, $pi, $sf,$fs);

    # 获取目录下的文本文件列表
    die "could not find dir $dir" unless opendir(DIR,$dir);

    # 我们只需要名字不以 '.' 开头的文本文件
    @files = grep { (-T "$dir/$_") && (!^\.) } readdir(DIR);

    closed(DIR);

    die "No story (text) files in $dir" unless @files;

    # 创建一个 publisher 和 publisher::index
    $p = new Publisher();
    $pi = new Publisher::Index();

    $p->set_dir($dir);
    $p->set_pub_dir($PUB_DIR);
    $p->set_tmpl_dir($TMPL_DIR);
    $p->set_default_tmpl($DEFAULT_TMPL);

    $pi->set_idx_page($IDX_PAGE);
    $pi->set_idx_item($IDX_ITEM);

    foreach my $file (@files) {
        my $story = new Story::Text($dir/$file);
        push @stories, $story;
    }

    $p->publish(@stories);
    $pi->generate($PUB_DIR);
}

sub usage {
    print "Usage: publish_dir.pl <story_dir> <pub_dir> [-p index_page] [-i index_item]\n";
    exit 1;
}
```

## 你需要的文件

我们将从安装 MySQL 开始。值得注意的是，MySQL（读作 "My S, Q, L"，而不是 "My Sequel"）虽然是免费提供的，但它是一个功能极其强大的数据库服务器。它可以用于简单的应用程序，也可以用于非常复杂的、大规模的操作。正如前文提到的，它最大的特点之一就是速度。

要安装 MySQL：

1. MySQL 随本书附带了 CD-ROM。或者，如需最新版本，请访问 http://mysql.com 并找到一个离你最近的镜像站点进行下载。
2. 为你的 Web 服务器下载最近的推荐 MySQL 版本。
3. 按照说明安装到你的服务器上。确保设置 root 密码。

现在，如果你还没有这样做，你就需要从 CPAN 下载并安装 DBI 模块。你还需要从 CPAN 下载一个名为`Mysql::MySQL::DBD`的特殊模块。

要下载这些文件：

1. 访问 http://www.perl.com/cpan/ 找到 DBI 模块，然后将其下载到你的电脑上。
2. 在你的服务器上从 CPAN 下载并安装`Mysql::MySQL::DBD`模块（以及它依赖的模块），确保选择 MySQL 作为你要使用的数据库。

## 在 MySQL 中设置数据库表

当你已经在服务器上准备好这些文件后，就可以准备好创建数据库及其必要的信息表、故事和故事集了。操作方法如下：

## Perl 网站工作坊

1. 创建数据库

```bash
mysqladmin create story_database -u root -p
```

2. 创建数据库表

```bash
/path/to/mysql -uroot -password story_database \
< /path/to/story_tables.sql
```

3. 添加具有相应权限的用户，用于创建和使用数据库表。请记住将下面`story-permissions.sql`文件中的虚假密码`auth_pass'}`更改为你自己选择的强密码。强密码应同时包含大小写字母、数字或标点符号，且不能是单词、名称，或单词或名称的常见变形。例如，“@s0n” 就不是强密码。

```bash
/path/to/mysql -uroot -password mysql \
< /path/to/story_permissions.sql

mysqladmin -u root -p password reload
```

这里是表脚本：

### story_tables.sql

```sql
# 创建表
# 如果你需要重新创建表，请取消这些注释
#drop table stories;
#drop table story_sets;
#drop table story_fields;
#drop table users;
#drop table user_sets;
#
# 创建 stories 表
create table stories (
id              int not null auto_increment,
set_id          int not null,
created         datetime not null,
story           char(128),
template        char(50),
target          char(255),
public_as      char(255),
public_on      datetime not null,
title           char(255) not null,
author          text,
summary         text,
text            text,
ts              timestamp,
key (set_id),
key (created);
```

`story_tables.sql`（续）

```sql
key (published_on),
key (title),
key (author),
primary key (id)
);
```

```sql
#
# 创建 story_sets 表
#
create table story_sets (
id int not null auto_increment,
name char(50) not null,
pub_dir char(128),
created datetime not null,
pub_on datetime not null,
idx_needs_up tinyint,
idx_template char(50),
idx_set_tmpl char(50),
idx_item_tmpl char(50),
idx_thread_type char(6),
idx_threshold int,
dflt_tmpl char(50),
dflt_target char(128),
dflt_title char(255),
dflt_author char(255),
dflt_summary text,
ts timestamp,
unique(name),
key(published_on),
key(created),
primary key (id)
);
```

```sql
#
# 创建 story_fields 表（保留故事非标准字段）
#
create table story_fields (
id int not null auto_increment,
story_id int not null,
field_name char(128) not null,
field_content text,
t timestamp,
key(story_id),
key(field_name),
primary key (id)
);
```

```sql
#
# 创建 users 表（如果你想保留更多关于每个用户的信息）
#
create table users (
id int not null auto_increment,
ts timestamp,
primary key(id)
);
```

### story_tables.sql（续）

```sql
#
# 创建 user_sets 表（保留每个用户的偏好）
#
create table user_sets (
    id int not null auto_increment,
    user_id int not null,
    set_id int not null,
    display int not null,
    timestamp,
    key(user_id),
    key(set_id),
    key(display),
    unique(set_id,user_id),
    primary key (id)
);

# 创建一些示例集
# （你可以用自己的集合替换这些）
insert into story_sets (
    'food_stories',
    '/usr/local/htdocs/perlbook/chap_1/',
    NOW(),
    0,
    'food_page_tmpl',
    'food_tmpl',
    'food_item_tmpl',
    0,
    0,
    'delicious romp!'
);

insert into story_sets (
    'art_stories',
    '/usr/local/htdocs/perlbook/chap_1/',
    NOW(),
    0,
    'art_page_tmpl',
    'art_tmpl',
    0,
    0,
    'beautiful romp!'
);
```

`story_tables.sql`（续）

```sql
insert into story_sets (
  'music_stories',
  '/usr/local/htdocs/perlbook/chap_1/music',
  NOW(),
  0,
  'music_page_tmpl',
  'music_tmpl',
  0,
  0,
  'harmonious romp!'
);

insert into story_sets (
  'other_stories',
  '/usr/local/htdocs/perlbook/chap_1/other',
  NOW(),
  0,
  'basic_index',
  0,
  0,
  'A romp!'
);
```

### story_permissions.sql

```sql
# 'author' 可以更新故事
# 将用户名、数据库和密码替换为适用于你网站的
```

`story_permissions.sql`（续）

```sql
GRANT select, insert, delete ON test.*
TO author@localhost IDENTIFIED BY 'auth_pass';

GRANT select, insert, delete ON test.*
TO author@% IDENTIFIED BY 'auth_pass';

# 'user' 可以读取所有，但只能更新 story_sets
GRANT select ON test.*
TO user@localhost IDENTIFIED BY 'auth_pass';
GRANT insert, update ON test.users
TO user@localhost IDENTIFIED BY 'auth_pass';
GRANT insert, update ON test.story_sets
TO user@localhost IDENTIFIED BY 'auth_pass';

GRANT select ON test.*
TO user@% IDENTIFIED BY 'auth_pass';
GRANT insert, update ON test.users
TO user@% IDENTIFIED BY 'auth_pass';
GRANT insert, update ON test.story_sets
TO user@% IDENTIFIED BY 'auth_pass';
```

现在你将把模块就绪。

## 添加模块

你已经下载（或已经拥有）本节将使用的以下模块。我们将仔细观察它们是如何运作的。

### Story::DBI.pm

我们使用 DBI 进行数据存储的第一个地方是网站的故事。故事本质上是文本，因此将其存储为文本文件最好吗？并不总是——特别是你需要速度、灵活性以及随时更新和编辑数据时。

此外，如果你考虑到读取的故事文本都是固定格式，而且我们花费了大量时间来解析和解释它们，你会发现让数据库为我们做这些结构性工作是有好处。

此时，我们还增加了故事集（story sets）的概念，即你可以选择组合在一起的相关故事。故事集是本章个性化方案的基础。本质上，我们将故事划分为组织良好的话题。

因此，`Story::DBI.pm`与我们之前第 8 章使用的`Story::Text`不同。我们不需要解析故事，但必须处理通过 MySQL 管理数据库的复杂性。由于这是一个相当长的模块，我们将分段来介绍。

### Story::DBI.pm

```perl
package Story::DBI;

# 安全考虑
$ENV{PATH} = '/bin:/usr/bin:/usr/local/bin';
$ENV{SHELL} = '/bin/sh';
$ENV{ENV} = '';
$ENV{IFS} = '';

use DBI;
use strict;
use qw($AUTOLOAD @ISA DBH);
```

这些是主要的故事字段——数据库中`stories`表中的字段。对于其他字段，我们需要在单独表中存储名称和内容，因此我们需要以不同的方式处理这两种字段。为了做到这一点，我们必须定义哪些是哪些。

```perl
@MAIN_FIELDS = qw(TITLE AUTHOR SUMMARY TEXT STORY
TARGET SET_ID PUBLISHED_ON CREATED TS);
```

此类的顶层字段比`Story::Text`要少——我们使用了一个酷的`AUTOLOAD`技巧，这使得数据库中的字段看起来像（字段）。我们将在模块末尾详细解释这一点。

```perl
my %fields = (
    'story' => {},
    'story_id' => undef,
    'story_set_id' => undef,
    'dirty' => undef,
    'error' => undef,
);
```

```perl
sub new {
    my $proto = shift;
    my $story_id = shift;
    my $story_flds = shift;
```

```perl
my $Class = ref($proto) || $proto;
my $self = { %fields };
```

## Perl 站点教程

```perl
bless $self, $class;
$self->_initialize($story_id,$story_flds);
$self->{'dirty'} = 0;

return $self;
```

实际上，`new()`是一个类方法，也可以作为对象方法使用。我们在脚本中将其作为类方法使用。

`db_connect()`是类方法，而不是对象方法。在同一个会话中创建的所有对象将共享同一个数据库连接。你之前见过这些方法：`new()`，在我们用过它的每个类中，它都是类方法。

```perl
sub db_connect {
  my $class = shift;
  my $dbi_connect_str = shift;
  my (@dbi_args) = @_;

  my $dbh = DBI->connect($dbi_connect_str,@dbi_args);
  return unless $dbh;

  $dbh = $dbh;
  return $dbh;
}

sub _initialize {
  my $self = shift;
  my $story_id = shift;
  my $story_flds = shift;

  unless ($DBH) {
    $self->error("Story::DBI: no database connection\n");
    return;
  }

  if ($story_flds) {
    $self->add_story($story_id,$story_flds);
    return;
  }

  if ($story_id) {
    $self->read_story($story_id);
  }
}
```

你会注意到，该类中的`read_story()`方法与我们之前看到的非常不同。在这里，我们不是读取和解析文本文件，而是使用两个 SQL 查询直接获取每个故事的主字段和次要字段，不需要解析。

## 第 9 章 创建你自己的门户

```perl
sub read_story {
    my $self = shift;
    my $story_id = shift;
    my ($sth, $rc, $story_fields, $story, $a, $fn, $fc);

    $story_id ||= $self->story_id;
    unless ($story_id) {
        $self->error('Story: no story specified');
        return;
    }

    # 像 CGIs 中的 'main' 函数 own包装一样，
    # 我们在这里使用 eval 来捕获在访问数据库期间
    # 出现的任何错误，在本例中
    eval {
        # 读取主故事信息
        $sth = $DBH->prepare('select * from stories where id='$story_id');
        die $DBH->errstr unless ref $sth;

        $rc = $sth->execute();
        die $sth->errstr unless $rc;

        $story_fields = $sth->fetch_hashref;

        # 读取其他故事字段
        $sth = $DBH->prepare('select * from story_fields where story_id='$story_id');
        die $DBH->errstr unless $sth;

        $rc = $sth->execute();
        die $sth->errstr unless $rc;

        while($sa = $sth->fetch_arrayref) {
          $fn = $sa->[2];
          $fc = $sa->[3];

          if (ref $story_fields->($fn)) {
            push @{$story_fields->($fn)}, $fc;
          } else if ($story_fields->($fn)) {
            $story_fields->($fn) = [ $story_fields->($fn), $fc ];
          } else {
            $story_fields->($fn) = $fc;
          }
        }

        if ($@) {
          $self->error("Story::DBI: read_story: $@");
        } else {
          # 将所有故事字段转换为大写
          foreach my $k(keys %story_fields) {
            $story(uc($k)) = $story_fields->($k);
          }

          $story->set(%story);
          $story->story_id($story_id);
          if ($story->{'SET'} && $story->{'SET_ID'}) {
            $self->story_set_to_id($story->{'SET'});
            $self->story_set_id($story->{'SET_ID'});
          }

          return 1;
        }
    };
}
```



在这一版本的 `read_story` 中，有些内容变得很复杂了。对于返回的每一行（每个故事字段），我们需要将故事字段的值（`story_fields.field_content`）添加到由 `story_fields.field_name` 键名的故事项中。

如果已经存在一个值数组，我们将新值添加到数组末尾。如果只有一个值，我们将创建一个包含旧值和新值的新数组。如果完全没有值，我们只需将该值设置为 `story_fields.field_content`。

你可能会问，这有什么意义？通过这种方式，我们可以为每个字段存储多个值。如果你想在故事中提供随机的用户定义内容，这是一个非常好的开始点。你将编写 `Story::DBI` 自己的子类，并编写方法来从多个值中选择一个返回，这样你就完成了一大半工作。

我们的数据并不是来自可以手动编辑的文件，我们需要某种输入数据的方法。`add_story()` 方法正是为此而设计的。它接收一个标准的故事哈希（hash）以及保存该故事所需的任何数据库记录。当然，使用此方法很容易将故事转换为 DBI 格式。你猜吧！我们在章节最后提供了一个实用脚本。

```perl
sub add_story {
  my $self = shift;
  my $story_id = shift;
  my $story = shift;
  my ($f,$rc,$sth,$created_id);

  # 构建创建新故事的 SQL 语句
  $sql = 'REPLACE INTO stories ';

  # 如果有 set id，则查找
  if ($story->{'SET'} && $story->{'SET_ID'}) {
    $self->_story_to_id($story->{'SET'});
    delete $story->{'SET'};
  }

  # 处理主故事字段
  foreach $f(keys %story) {
    if ($story->{$f}) {
      push @ids, lc($f);
      push @vals, $DBH->quote($story->{$f});
    }
    # 从哈希中移除，以免下面再次看到
    delete $story->{$f} if $story->{$f};
  }

  # 通过这种方式放入 id 字段，我们可以更新记录
  # (我们需要确保这个值不会被覆盖，所以先将其从哈希中移除)
  unshift @ids, 'id';
  unshift @vals, $DBH->quote($story_id);

  # 如果是新的，则设置创建日期
  unless ($story_id) {
    push @ids, 'created';
    push @vals, 'NOW()';
  }

  $sql .= join(', ', @ids) . ' VALUES (' . join(', ', @vals) . ')';

  # 捕获任何错误
  eval {
    $sth = $DBH->prepare($sql) || die $DBH->errstr;
    $sth->execute() || die $sth->errstr;

    # 获取我们创建的故事 id
    # 注意：这不是移植代码。它适用于 MySQL。
    # 如果使用其他数据库，请咨询该数据库的 DBD 驱动以找到等效函数
    $created_id = $sth->mysql_insert;
    die "Unable to determine what story was created" $created_id;
  };

  if ($@) {
    $self->error('Story::DBI: add_story: $@');
    return;
  }

  # Perl 站点教程

  # 清除属于故事的所有字段
  eval {
    $DBH->do('DELETE FROM story_fields WHERE id=$created_id') || die $DBH->errstr;
  };

  if ($@) {
    $self->error('Story::DBI: add_story: error while cleaning story fields: $@');
    return;
  }

  # 将其他字段作为 story_field 记录添加
  if (keys %story) {
    eval {
      foreach $f (keys %story) {
        $v = $DBH->quote($story->{$f});
        $f = $DBH->quote($f);
        $sql = 'INSERT INTO story_fields VALUES ($created_id, $f,$v,NULL)';
      }
      $DBH->do($sql) || die $DBH->errstr;
    };
  }

  if ($@) {
    $self->error('Story::DBI: add_story: error while adding story fields: $@');
    return;
  }

  $self->story_id($created_id);

  # 因为 'dirty' 机制依赖 autoload，
  # 我们必须小心声明干净
  $self->{'dirty'} = 0;

  # 最后，将新创建的故事读入故事字段
  $self->read_story($created_id);

  # 返回创建的故事 id
  return $created_id;
}

sub delete_story {
  my $self = shift;
  my $story_id = shift;
  my ($sql,$rc);

  $sql = "DELETE FROM stories WHERE id='$story_id";

  eval {
    $DBH->do($sql) || die $DBH->errstr;
  };

  if ($@) {
    $self->error('Story::DBI: delete_story:$@');
    return;
  }

  $self->{'dirty'} = 0;

  return 1;
}
```

奇怪的是，大多数人类（也许 Perl 程序员除外）发现记住单词比记住一串数字更容易。因此，我们提供了 `story_set_to_id` 函数，将故事集合名称转换为快速访问数据库中 `story_sets` 所需的 id。通过这种方式，你可以在模板中使用 `$LOCAL_NEWS` 而不是 `$SET_SET_1267`。

```perl
sub story_set_to_id {
    my $self = shift;
    my $set_name = shift;
    my ($sth, $rc, $r) = $@;

    $sth = $DBH->prepare("SELECT id FROM story_sets WHERE name=$set_name");
    die $DBH->errstr unless ref $sth;
    $sth->execute() || die $DBH->errstr;

    $r = $sth->fetchrow_arrayref;

    if ($@) {
        $self->error('Story::DBI: could not determine "id of story set \$set_name: \$@');
        return;
    }

    return $r->[0];
}
```

## Perl 网站工作坊

```perl
# 设置本地字段，以及
# story_set 字段：
sub story_set_id {
my $self = shift;
my $id = shift;
return $self->{'story_set_id'} unless $id;
```

```perl
# 设置对象字段。
$self->{'story_set_id'} = $id;
```

```perl
# 设置 my story hash 中的字段
$self->story->{'SET_ID'} = $id;
```

```perl
# 现在更新数据库
$self->dirty(1);
}
```

```perl
# 将 set id 转换为 set name
sub story_set {
my $self = shift;

return unless $self->set_id;

my ($sql, $sth, $sid, $sr);

$sid = $self->set_id;
$sql = "SELECT name FROM story_sets WHERE id=$sid";

eval {
$sth = $DBH->prepare($sql);
$DBH->errstr unless ref $sth;

$sth->execute || die $sth->errstr;

$r = $sth->fetch_array_ref;

return unless ref $r;

return $r->[0];
}
}
```

```perl
sub story_id {
my $self = shift;
my $id = shift;

return $self->{'story_id'} unless $id;

die "无法覆盖 story id!"
if ((($self->{'story_id'}) &&
($id != $self->{'story_id'})));

$self->{'story_id'} = $id;
$self->dirty(1);
return $id;
}
```

# 第 9 章 创建你自己的门户

这里有一个关于“为什么你应该始终使用访问器函数（accessor functions）而不是直接访问对象字段”的“对象式”课程。对于调用者来说，这些函数看起来与 `Story::Text` 中的函数没有区别，但它们的实现方式完全不同，而且实现的功能不仅仅是返回一个预定的值。如果我们之前通过使用 `$Story->{'field'}` 而不是 `$story->field()` 来访问 story 值，我们就无法做到这一点。

```perl
# 返回 story 模板，或者如果 story tmpl 
# 未定义，则返回 story 的 story_set 
# 默认模板
sub template {
    my $self = shift;
    return $self->get_field_or_dflt('template','dflt_tmpl');
}

sub target {
    my $self = shift;
    return $self->get_field_or_dflt('target','dflt_target');
}

sub title {
    my $self = shift;
    return $self->get_field_or_dflt('title','dflt_title');
}

sub author {
    my $self = shift;
    return $self->get_field_or_dflt('author','dflt_author');
}

sub summary {
    my $self = shift;
    return $self->get_field_or_dflt('summary','dflt_summary');
}

# 一个通用的程序，用于获取字段值（如果存在），
# 或者获取对应的 story_set 字段
sub _get_field_or_dflt {
    my $self = shift;
    my $story_fld = shift;
    my $set_fld = shift;
}

my ($set_id,$sql,$sth,$rc,$set);
$story_fld = uc($story_fld);
return $self->story->($story_fld) if $self->story->($story_fld);
$set_id = $self->story_set_id;

$sql = "SELECT * FROM story_sets WHERE id='$set_id";
```

```perl
eval {
$sth = $DBH->prepare($sql);
die $DBH->errstr unless $sth;

$rc = $sth->execute;
die $sth->errstr unless $rc;

$set = $sth->fetchrow_hashref;
};

if (@) {
$self->error("Story::DBI::_get_field_or_dflt: $@");
return;
}

return $set->{set_fld};
}
```

另一个“对象式”课程：我们对常规 `AUTOLOAD` 函数的修改会在放弃之前查找 story hash 中的未 own字段。这使得例如调用 `$Story->story->{TEXT}` 变得可能，并且实际上获取 `$Story->story->{TEXT}` 的值。

我们检查调用者尝试调用的函数。如果名称与对象字段匹配，我们就访问该字段。如果我们没有根据 story hash 中的字段对名称进行检查，并且它匹配其中任何一个，我们就会访问该值。`AUTOLOAD` 太酷了，Jason 简直得无法忍受。Molly 认为这是程序员的一种事儿——但如果他觉得它很酷，那么好吧，它一定很酷。

```perl
sub AUTOLOAD {
$self = shift;
$type = ref($self) || (die "$self 不是一个对象");
$name = $AUTOLOAD;
$ptr = $self;
$dirt = $self->{'dirty'};
$name = s/\*;//

unless (exists $self->{$name}) {
$ptr = $self->{'story'};
$name = uc($name);

# 如果我们要在 story 字段中
# 设置一个值，确保我们在 die 的时候
# 保存状态
$dirt = 1;
unless (exists $self->{$name}) {
$ptr = $self->{'story'};
$name = uc($name);

# if we're going to set a value
# in story fields, make sure we
# save our state when die
$dirt = 1;
unless (exists $self->{$name}) {
$ptr = $self->{'story'};
$name = uc($name);

# if we're going to set a value
# in story fields, make sure we
# save our state when die
$dirt = 1;
unless (exists $self->{$name}) {
$ptr = $self->{'story'};
$name = uc($name);

# if we're going to set a value
# in story fields, make sure we
# save our state when die
$dirt = 1;
unless (exists $self->{$name}) {
$ptr = $self->{'story'};
$name = uc($name);

# if we're going to set a value
# in story fields, make sure we
# save our state when die
$dirt = 1;
unless (exists $self->{$name}) {
$ptr = $self->{'story'};
$name = uc($name);

# if we're going to set a value
# in story fields, make sure we
# save our state when die
$dirt = 1;
unless (exists $self->{$name}) {
$ptr = $self->{'story'};
$name = uc($name);

# if we're going to set a value
# in story fields, make sure we
# save our state when die
$dirt = 1;
unless (exists $self->{$name}) {
$ptr = $self->{'story'};
$name = uc($name);
}
```

 =,

}

```perl
# if we're going to set a value
# in story fields, make sure we
# save our state when die
$dirt = 1;
unless (exists $self->{$name}) {
$ptr = $self->{'story'};
$name = uc($name);

# if we're going to set a value
# in story fields, make sure we
# save our state when die
$dirt = 1;
unless (exists $self->{$name}) {
$ptr = $self->{'story'};
$name = uc($name);

# if we're going to set a value
# in story fields, make sure we
# save our state when die
$dirt = 1;
unless (exists $self->{$name}) {
$ptr = $self->{'story'};
$name = uc($name);
}
```

``` 抱歉，这里重新整理的逻辑内容：

```perl

sub template {

    my $self = shift;

    return $self->get_field_or_dflt('template','dflt_tmpl');

}

sub target {

    my $self = shift;

    return $self->get_field_or_dflt('target','dflt_target');

}

sub title {

    my $self = shift;

    return $self->get_field_or_dflt('title','dflt_title');

}

sub author {

    my $self = shift;

    return $self->get_field_or_dflt('author','dflt_author');

}

sub summary {

    my $self = shift;

    return $self->get_field_or_dflt('summary','dflt_summary');

}

# 一个通用的程序，用于获取字段值（如果存在），

# 或者获取对应的 story_set 字段

sub _get_field_or_dflt {

    my $self = shift;

    my $story_fld = shift;

    my $set_fld = shift;

}

```

注：由于原始文本末尾出现了大量重复的乱码片段，上述翻译已根据逻辑结构进行了清理和对齐。

---
**更正：我发现你提供的原始文本后部分存在极其重复的粘贴错误。以下是基于逻辑提取的完整译文：**

## Perl 网站工作坊

```perl

# 设置本地字段，以及

# story_set 字段：

sub story_set_id {

my $self = shift;

my $id = shift;

return $self->{'story_set_id'} unless $id;

```

```perl

# 设置对象字段。

$self->{'story_set_id'} = $id;

```

```perl

#并且在 my story hash 中设置字段

$self->story->{'SET_ID'} = $id;

```

```perl

# 现在更新数据库

$self->dirty(1);

}

```

```perl

# 将 set id 转换为 set name

sub story_set {

my $self = shift;

return unless $self->set_id;

my ($sql, $sth, $sid, $sr);

$sid = $self->set_id;

$sql = "SELECT name FROM story_sets WHERE id=$sid";

eval {

$sth = $DBH->prepare($sql);

$DBH->errstr unless ref $sth;

$sth->execute || die $sth->errstr;

$r = $sth->fetch_array_ref;

return unless ref $r;

return $r->[0];

}

}

```

```perl

sub story_id {

my $self = shift;

my $id = shift;

return $self->{'story_id'} unless $id;

die "无法覆盖 story id!"

if ((($self->{'story_id'}) &&

($id != $self->{'story_id'})));

$self->{'story_id'} = $id;

$self->dirty(1);

return $id;

}

```

# 第 9 章 创建你自己的门户

这里有一个关于“为什么你应该始终使用访问器函数而不是直接访问对象字段”的“对象式”课程。对于调用者来说，这些函数看起来与 Story::Text 中的函数没有区别，但它们的实现方式完全不同，而且实现的功能不仅仅是返回一个预定的值。如果我们之前通过使用 `$Story->{'field'}` 而不是 `$story->field()` 来访问 story 值，我们就无法做到这一点。

```perl

# 返回 story 模板，或者如果 story tmpl 

# 未定义，则返回 story 的 story_set 

# 默认模板

sub template {

    my $self = shift;

    return $self->get_field_or_dflt('template','dflt_tmpl');

}

sub target {

    my $self = shift;

    return $self->get_field_or_dflt('target','dflt_target');

}

sub title {

    my $self = shift;

    return $self->get_field_or_dflt('title','dflt_title');

}

sub author {

    my $self = shift;

    return $self->get_field_or_dflt('author','dflt_author');

}

sub summary {

    my $self = shift;

    return $self->get_field_or_dflt('summary','dflt_summary');

}

# 一个通用的程序，用于获取字段值（如果存在），

# 或者获取对应的 story_set 字段

sub _get_field_or_dflt {

    my $self = shift;

    my $story_fld = shift;

    my $set_fld = shift;

}

my ($set_id,$sql,$sth,$rc,$set);

$story_fld = uc($story_fld);

return $self->story->($story_fld) if $self->story->($story_fld);

$set_id = $self->story_set_id;

$sql = "SELECT * FROM story_sets WHERE id='$set_id";

```

```perl

eval {

$sth = $DBH->prepare($sql);

die $DBH->errstr unless $sth;

$rc = $sth->execute;

die $sth->errstr unless $rc;

$set = $sth->fetchrow_hashref;

};

if (@) {

$self->error("Story::DBI::_get_field_or_dflt: $@");

return;

}

return $set->{set_fld};

}

```

另一个“对象式”课程：我们对常规 AUTOLOAD 函数的修改会在放弃之前查找 story hash 中的未 own字段。这使得例如调用 `$Story->story->{TEXT}` 变得可能，并且实际上获取 `$Story->story->{TEXT}` 的值。

我们检查调用者尝试调用的函数。如果名称与对象字段匹配，我们就访问该字段。如果我们没有根据 story hash 中的字段对名称进行检查，并且它匹配其中任何一个，我们就会访问该值。AUTOLOAD 太酷了，Jason 简直得无法忍受。Molly 认为这是程序员的一种事儿——但如果他觉得它很酷，那么好吧，它一定很酷。

```perl

sub AUTOLOAD {

$self = shift;

$type = ref($self) || (die "$self 不是一个对象");

$name = $AUTOLOAD;

$ptr = $self;

$dirt = $self->{'dirty'};

$name = s/\*;//

unless (exists $self->{$name}) {

$ptr = $self->{'story'};

$name = uc($name);

# 如果我们要在 story 字段中

# 设置一个值，确保我们在 die 的时候

# 保存状态

$dirt = 1;

unless (exists $self->{$name}) {

$ptr = $self->{'story'};

$name = uc($name);

```
*(注：由于原始文本后部分存在大量重复的错误块，上述翻译已根据逻辑提取并对齐)*




## Perl 网站工作坊

```

return 1;

}

```

```perl

sub add_story_set {

    my $self = shift;

    my $set = shift;

    my $set_tmpl = shift;

    my $item_tmpl = shift;

    $self->{'story_sets'} ||= {};

    # 不要定义两次...

    return if $self->story_sets->($set) || {

        'set_tmpl' => undef,

        'item_tmpl' => undef,

        'stories' => undef,

        'html' => undef,

    };

    # 注意：这些是模板名称而不是模板文件名

    # 在在使用它们之前，你必须使用 use_template 让

    # 发布者知道你想使用的模板

    ($set_tmpl) &&

        ($self->story_sets->($set)->{'set_tmpl'} = $set_tmpl);

    ($item_tmpl) &&

        ($self->story_sets->($set)->{'item_tmpl'} = $item_tmpl);

}

```

```perl

sub publish {

    my $self = shift;

    my $target_fl = shift;

    my $page_tmpl = shift;

    my $set_tmpl = shift;

    my $item_tmpl = shift;

    my $published;

    unless ($self->build_page($page_tmpl, $set_tmpl, $item_tmpl)) {

        $my $err = $self->error;

        $self->error("Publisher::Index::Multi: " \

"无法构建页面: $err");

        return;

    }

    unless ($published = $self->write_file($target_fl)) {

        $self->error("Publisher::Index::Multi: " \

"无法写入文件 $target_fl");

        return;

    }

    return $published;

}

```

# 第 9 章 创建你自己的门户

由于我们正在处理多一组故事，构建页面的复杂性比在 `Publisher::Index` 中要高。我们必须遍历 `story_sets` 哈希表，为每个构建的模板对象（格式化为 `item_tmpl`）进行构建。每个对象必须包含来自 `set_tmpl` 的 HTML 块的完整格式。

然后，我们将这些 HTML 块赋值给主页面模板中的变量，使用集合的名称作为变量名。解释起来很麻烦，但我们保证它很好用。简单来说，在你的索引页面模板中写故事的名字，该集合的链接就会出现在最终页面的那个位置。

```perl

sub build_page {

my $self = shift;

my $page_tmpl = shift;

my $set_tmpl = shift;

my $item_tmpl = shift;

my $tpl = $self->tpl;

my ($set_html, $p);

```

```perl

# 构建每个故事集

foreach my $st(keys %($self->story_sets)) {

    unless ($set_html = $self->build_story_set($st,

        $set_tmpl)) {

        $self->error("Publisher::Index::Multi: *\n    *构建故事集 $st 失败*");

    }

}

```

```perl

# 将结果赋值给与集合同名的 模板变量。在主页面

# 模板中使用此变量来放置故事集。

$tpl->assign(uc($st)->$set_html);

```

```perl

# 构建整个页面

$tpl->parse('MAIN', $page_tmpl);

$self->page($tpl->fetch('MAIN'));

$p = $self->page;

```

```perl

if (ref $sp && $sp) {

    return $sp;

} else {

    $self->error("Publisher::Index::Multi: 构建页面失败");

    return;

}

```

## Perl 网站工作坊

在这种情况下，我们必须考虑到方法会被连续调用的可能性。因此，在做其他事情之前，我们必须清理旧的赋值。

该类中的 `build_story_set()` 方法与 `Publisher::Index` 中的 `build_page()` 函数非常相似——如你所期望，它们都接收一组故事并产生带有链接的 HTML 块。

巨大的区别在于？`Publisher::Index` 的模板使用了 `<html>` 和 `<body>` 标签。

```perl

sub build_story_set {

my $self = shift;

my $set = shift;

my $tmpl = shift;

my $item_tmpl = shift;

my $tpl = $self->tmpl;

```

```perl

# 返回一个空格，而不是空字符串，否则

# 集合的名字将出现在输出页面中！

return ' ';

$self->story_sets->

setset = $self->story_sets->{$set}->{'stories'};

```

```perl

# 这些复杂的构造允许模板默认值的级联覆盖

# 使用我们指定的、故事集要求的、或者最后是默认值

$set_tmpl ||= $self->story_sets->{$set}->{'tmpl'};

$item_tmpl ||= $self->story_sets->{$set}->{'item_tmpl'}

};

```

```perl

# 清理一下 - 为了防止第一个集合的故事被附加

$tpl->clear('STORIES');

```

```perl

# 构建用于插入模板的 STORIES 项

$tpl->assign('ST_TITLE' => $set->{'title'},

'ST_URL' => $set->{'url'},

'ST_AUTHOR' => $set->{'author'},

'ST_SUMMARY' => $set->{'summary'},

```

```perl

$tpl->parse('STORIES' => $item_tmpl);

}

```

```perl

# 将清晰的 HTML 格式的集合名称

# 传递给模板

$tpl->assign('ST_NAME' => $set,

'ESC_SET' => CGI::escape($set));

```

```perl

# 构建此集合的 html 块

$tpl->parse(uc($set) => $set_tmpl);

$p = $tpl->fetch(uc($set));

```

```perl

if (ref $sp && $sp) {

    $self->story_sets->{$sp}->{'html'} = $sp;

    return $sp;

} else {

    $self->error("Publisher::Index::Multi: 为故事集 '$set' 生成 html 块失败");

    return;

}

``` 最后，有两个函数帮助我们生成的链接指向故事页面，以及我们的老朋友 `AUTOLOAD`。

```perl

# 将文件路径转换为绝对 URL

（从 $self->_www_root 开始）

sub make_abs_url {

    $self = shift;

    $file = shift;

    $dir = $self->_www_root;

    $file = &full_path($file);

    $file = s|$dir|//;

```

```perl

# 注意，如果文件名是 www_root 之外文件的完整路径

# 我们没有对其任何修改

return $file;

}

```

```perl

sub full_path {

    $file = shift;

    return $file if ($file =~ m|^/);

    my $cwd = cwd();

    return $cwd/$file;

}

```

```perl

AUTOLOAD {

    $self = shift;

    $type = ref($self) || die ($self is not an object);

    $name = $AUTOLOAD;

    $name = s/[:]*://;

    unless ($self->($name)) {

        die ("无法访问类 $type 对象中的 '$name' 字段");

    }

    if (@_) {

        return $self->($name) = shift;

    } else {

        return $self->($name);

    }

}

```

## Perl 网站工作坊

好了，这一步完成了。但在休息之前还有长路要走。我们保证这是值得的，我们会在过程中提供 cookie。接下来是你需要的 CGI。

自然地，你需要 CGI 来帮助传递所有信息。在这里我们来看整合所有这些内容的脚本。

my.cgi

用户被静静地跟踪，不需要注册或登录即可启用页面。

此 CGI 实现了门户风格“新闻类”网站的基本个性化功能。它使用 cookie 来通过 DBI 在 SQL 数据库中跟踪用户 ID 和偏好。用户可以选择一组他们希望经常在索引页面上看到的故事集（图 9.1）。

图 9.1
选择你想要的故事！

![](img/d26997dc0c057101b472952ba1a4ac_216_0.png)

# 第 9 章 创建你自己的门户

my.cgi

```perl

#!/usr/bin/perl -wT

# 本地库

use lib '/path/to/library';

use Story::DBI;

use Publisher::Index::Multi;

use Taintcheck;

use CGI;

use strict;

use vars qw(\$_START \$CGI \$AGE_LIMIT \$DSN \$DBH \$USER \$PASSWORD \$TMPL\_DIR \$TMP\_TMPL \$SET\_TMPL \$ITEM\_TMPL);

# DBI 连接设置。将驱动程序、主机名、数据库、

# 用户和密码字段替换为适用于你网站的值

$DSN = 'mysql:host=localhost;database=test';

$USER = 'web_user';

$PASSWORD = '/path/to/web_user/password_file';

chomp($PASSWORD); # 删除 cat 添加的换行符

$CGI = 'my.cgi';

# 故事包含所需的天数

$AGE_LIMIT = 7;

# 替换为真实的模板目录

$TMPL_DIR = '/path/to/templates/';

# 必需模板

$PAGE\_TMP = 'idx_page';

# 可选模板

$SET\_TMPL = 'basic_set';

$ITEM\_TMPL = 'basic_item';

eval { main(); }; \$_START__ = \__LINE__;

if ($@) {

    chomp(\@);

    $0 = s/\(eval\) line \(d+)/)/\${CGI\}" * ""(\$_START__-\$1-1)/e;

    $0 = s/( at ).*( line )/\${CGI\}$22;

    my \$error_message = \$0;

    print <<ERR;

Content-type: text/html

```





## Perl 网站工作坊

my.cgi (续)

```perl

<HTML>

<HEAD><TITLE>Error</TITLE></HEAD>

<BODY>

<<h1>Error</h1>

<code>error_message</code>

</BODY>

</HTML>

ERR

```

```perl

exit();

sub main {

  my ($q, $user, $set, $sets, $pub, $page);

  my ($set_tpl, $item_tpl, $stories, $story, $cookie);

  # 调试时用： 如果你在调试时遇到问题，请取消注释

  # 数据库访问问题

  # $DBI->trace(2);

  # 连接到数据库

  $DBH = Story::DBI->db_connect($DSN, $USER, $PASSWORD);

  die "Could not connect to database" unless ref $DBH;

  # 获取新的输入

  $q = new CGI->new;

  untaint_params($q);

  # 获取与 cookie 关联的用户记录

  # 如果没有 cookie，或者用户记录无效，

  # 将创建并返回一个新的用户记录。

  $user = get_user($q);

  die "Could not get user record" unless $user;

  $pub = new Publisher::Index::Multi();

  die "Could not initialize publisher: " .

  $pub->error if $pub->error;

  # 设置模板和发布环境

  # 将路径替换为你的 www root 目录的真实路径

  # (例如，对于 redux 用户，/home/httpd)

  $pub->www_root('/path/to/www/root');

  $pub->use_template($MTN::PAGE_TMP, 'page');

  $pub->use_template('SET', $SET_TMP, 'set');

  $pub->use_template('ITEM', $ITEM_TMP, 'item');

  # 根据用户偏好选择故事

  foreach $set(@{$user->{'sets}}) {

```

# 第 9 章 创建你自己的门户网站

my.cgi (续)

```perl

# 定义 set 中使用的任何模板

$set_tmpl = '';

$item_tmpl = '';

if ($set->{'set_tmpl'}) {

    $set_tmpl = ($set->{'name'}) . '_set_tmpl';

    $pub->use_template($set_tmpl, $set->{'set_tmpl'});

}

if ($set->{'item_tmpl'}) {

    $item_tmpl = ($set->{'name'}) . '_item_tmpl';

    $pub->use_template($item_tmpl, $set->{'item_tmpl'});

}

# 添加 set

$pub->add_story_set($set->{'name'}, $set_tmpl, $item_tmpl);

# 获取 set 中的故事

$stories = select_stories($set);

# 添加这些故事

if ($stories) {

    foreach my $story(@$stories) {

        $pub->add_story($set->{'name'}, $story);

    }

}

# 生成页面 —— 这里我们不使用 publish

# 方法，因为它会将文件保存到磁盘，

# 因为我们要直接将创建的页面

# 发送到浏览器。

my $sp = $pub->build_page();

if (ref $sp) {

    $page = $sp;

} else {

    die 'Could not generate page: ' . $pub->error;

}

# 最后，将页面发送到浏览器，

# 设置 cookie，这样用户的偏好

# 在她下次访问时就会被“固定”

$cookie = $q->cookie(name='my.cgi_userid',

    value=$user->{'id'});

print $q->header('cookie=' . $cookie), $page;

```

在尝试获取用户偏好设置时，我们需要处理三种情况：新用户；cookie 能够正确识别其用户记录的重复访问者；以及 cookie 失效（或我们网站的数据库损坏）导致未关联用户记录的用户。

```perl

sub get_user {

    my $q = shift;

    my ($uid,$user);

    # 获取或创建用户 id

    unless ($q->cookie('my.cgi_userid')) &&

        $user = user_prefs($q->cookie('my.cgi_userid'),$q));

    $user = user_prefs(new_user());

}

return $user;

}

```

当我们创建一个新的用户记录时，我们没有存储多少信息——只有用户 id 和时间戳，这些是自动生成的。如果你想存储更多信息，你必须更新 users 表的定义，以及该函数。

```perl

sub new_user {

    my ($uid,$sth);

    # 插入一个新的用户记录

    $sth = $DBH->prepare('INSERT INTO users VALUES(NULL,NULL)')

        || $DBH->errstr;

    $sth->execute() || $sth->errstr();

    # 这是 MySQL 特有的 —— 如果你使用不同的数据库，你需要查看其文档

    # 以寻找等效函数。

    $uid = $sth->insert('insert_id');

    die 'Failed to create new user' unless $uid;

    return $uid;

}

sub user_prefs {

    my $uid = shift;

    my $q = shift;

    return unless $sth;

    my ($updates,$sth,$r);

    if (@updates) {

        @updates = map { /^update_(.*)$/ ? $1 : () } $q->param;

    }

```

# 第 9 章 创建你自己的门户网站

为了更新数据库中的用户偏好设置，我们为 CGI 参数中的每个 `update_set` 名称创建一个 `user_set` 记录。你通过提交此类字段来实现：`<input name="update_news" value="0">` 来关闭来自本地 set 的故事章节，或者使用 `<input name="update_news" value="1">` 开启它。

```perl

foreach $set (@updates) {

    # 获取此故事组合 

    # 对应的 user_set 的 id;

    $sth = $DBH->prepare("SELECT us.id FROM

    user_sets as us, story_sets as s

    WHERE us.user_id=$uid AND

    s.name='$set' AND us.set_id=$s.id");

    die $DBH->errstr unless $sth;

    $sth->execute() || die $sth->errstr;

    $r = $sth->fetchrow_array();

    $DBH->do("UPDATE user_sets

    SET display=$q->param('update_$set')

    WHERE id=$r[0]");

} else {

    # 如果没有记录，使用默认设置，

    # 为每个 set 创建 user_set 记录

    $sth = $DBH->prepare("SELECT id FROM

    story_sets");

    die $DBH->errstr unless $sth;

    $sth->execute() || die $sth->errstr;

    while (my $r = $sth->fetchrow_array()) {

        $DBH->do("INSERT INTO user_sets (user_id,set_id,display)

        VALUES ($uid,$r[0],0)");

    }

}

```





# 第 9 章 创建你自己的门户

# 我们发送了一个空字符串。
$db_story = new Story::DBI('', $text_story->story);

```perl

die $db_story->error if $db_story->error;

$sti = $db_story->title || 'untitled';

$st = $db_story->story{'STORY'} || '(unnamed)';

```

```perl

print "Story $sti was successfully converted \nfrom text file $st.\n"

}

```

```perl

sub usage {

return <<USAGE;

story_txtdbi.pl story_file [story_file ...]

USAGE

}

```

## add_story_set.pl

向数据库中添加故事集（story sets）提供了更大的灵活性和功能，但同时也增加了一项需要维护的内容。如果你在创建表时不想使用集合，或者以后以后再添加更多集合，可以使用此实用脚本。

我们还借此机会介绍 `GetOpt::Long` 模块（Perl 标准分发的一部分），它在命令行脚本中非常有用。该模块让程序能够接受命令行上的详细选项（verbose options），这样脚本的用户就可以说 `script -option` 而不是 `script -`。

在这种情况下，我们利用用数据库字段名称命名我们的选项来节省一些工作。然后我们可以直接将数据传递到正确的位置，而无需猜测该放入什么内容。

```perl

add_story_set.pl

!/usr/bin/perl -w

#

#

# add_story_set.pl

#

#

# 创建故事集记录

```

```perl

use DBI;

use GetOpt::Long;

```

## add_story_set.pl (续)

```perl

use strict;

use vars qw($DBH DSN $USER PASS %OPTS);

```

```perl

# 全局变量

# 将这些值替换为适用于站点的值

```

```perl

$DSN = 'dbi:mysql:hostname=localhost;database=test';

$USER = 'user';

$PASS = 'secret';

```

```perl

# 获取命令行选项

%OPTS = ();

GetOptions(\%OPTS, 'idx_set_tmpl:s', 'idx_item_template:s', 'dflt_tmpl:s',

'dflt_target:s', 'dflt_title:s', 'dflt_author:s', 'dflt_summary:s');

```

```perl

die usage($ARGV[0]);

$DBH = DBI->connect($DSN, $USER, $PASS);

die 'Could not connect to database' unless $DBH;

```

```perl

add_set($ARGV[0]), \%OPTS);

```

```perl

# 子程序

sub add_set {

my $set_name = shift;

my $opts = shift;

```

```perl

my ($sql, @flds, @vals);

```

```perl

#

# 构建添加集合的 SQL 语句

#

$sql = 'INSERT INTO story_sets *';

```

```perl

# 添加必选字段

push @flds, 'name';

push @vals, $DBH->quote($set_name);

```

```perl

# 以及任何设置设置可选字段

foreach my $f (keys %OPTS) {

push @flds, $f;

push @vals, $DBH->quote($opts->$f));

}

```

```perl

$sql .= ' (' . join(', ', @flds) . ')

VALUES (' . join(', ', @vals) . ')';

```

```perl

#

# 执行 SQL 语句并报告结果

#

$DBH->do($sql) || die $DBH->errstr;

```

## add_story_set.pl (续)

```perl

print 'Story set $set_name was added successfully.\n';

sub usage {

return <<USAGE;

add_story_set.pl set_name [--idx_set_tmpl template] \n  --idx_item template template] \n  --dflt_tmpl template] \n  --dflt_target target_file | target_dir] \n  --dflt_title 'story title'] \n  --dflt_author 'author'] [--dflt_summary 'summary']

USAGE

}

```

## publish_dbi.pl

我们的最后一个实用程序与其说是一个真正的工具，不如说它是如何使用 `Story::DBI` 的示例。没有人能记得数据库记录的 ID 编号——所以这有用吗？首先，它展示了面向对象编程的力量。这个脚本通过 SQL 数据库获取数据，与仅使用纯文本文件的 `publish.pl` 之间的区别微乎其微。页面实际上是由完全相同的代码生成的，即 `Publisher` 模块。

其次，你应该仔细查看这个模块，因为你将在第 10 章“门户向导”中再次看到这段代码。它展示了如何使用 `Story::DBI` 来构建站点。





## Perl 网站工作

auth.sql (继续)

```sql

primary key (id)

)\g

```

```sql

create table sessions (

  id int not null auto_increment,

  login char(16) not null,

  ts timestamp not null,

  key (ts),

  key (login),

  primary key (id)

)\g

```

```sql

# 在此处替换 login 和 password

# 使用你自己的唯一设置。

INSERT INTO auth_users VALUES (NULL, 'admin',

PASSWORD('bingo'), 1!@)\g

```

在数据库的最后部分，你会注意到用于登录的函数（图 10.2）。这是我们在身份验证和安全方面的的第一步，在整个章节中是一个持续且重要的问题。

图 10.2
授权入口。

![](img/d26997dc0c0571017b4729525ba1a4ac_232_0.png)

## 第 10 章网站发布向导

Sitemap 脚本需要两个 SUID 脚本。记住，这些脚本会让运行脚本的人根据脚本本身获得权限级别——无论他们是谁。其中一个 `publish_dbi.pl` 在第 9 章中提供。你应该已经让它正常运行了——如果没有运行，请返回第 9 章进行设置。第二个脚本现在由你创建。

你将把 `Publish_set.pl` 放置在你的用户目录中，并通过输入 `CHMOD +xs publish_set.pl` 来设置权限。

Publish_set.pl

```perl

#!/usr/bin/perl -wT

${ENV{PATH}} = '/bin:/usr/bin:/usr/local/bin';

${ENV{SHELL}} = '/bin/sh';

${ENV{IFS}} = '';

${ENV{ENV}} = '';

use lib '/path/to/library';

use Taintcheck;

use Story::DBI;

use Publisher;

use Publisher::Index;

use Getopt::Long;

use struct;

ars vars qw(%OPTARG) $DBH $DSN $USER $PASSWORD $TMPL_DIR $PAGE $ITEM);

$DSN = 'dbi:mysql:hostname=localhost:database=stories';

$USER = 'author';

$PASSWORD = 'auth_pass';

# 模板默认值

$TMPL_DIR = '/path/to/templates/';

$PAGE = 'basic_index_page';

$ITEM = 'basic_index_item';

$DBH = DBI->connect($DSN, $USER, $PASSWORD);

die 'Could not connect to database' unless $DBH;

# 为存储使用相同的数据库连接

$Story::DBH = $DBH;

```

在我们继续之前，让我们看看此脚本中用到的一些技术概念。`Getopt::Long` 模块。它是 Perl 标准分发的一部分，用于读取命令行选项。

## Perl 网站工作

由于 SUID 脚本会赋予脚本额外的权限，因此它们需要更细心的对待！如果你将 SUID 脚本存放在 `cgi-bin` 目录中，就会创建一个严重的安全问题。SUID 脚本应该放置在独立的工具目录中，明确地位于 `cgi-bin` 目录之外。

`Getopt::Long` 是对于从其他脚本调用的脚本（称为 cron 任务）的好选择。六个月后，当你试图弄清楚你曾经编写的脚本本该做什么的时，长选项名称要容易解释得多！

```perl

# 逐个处理命令行选项

GetOptions(\$OPT, "nindex", "nostories", "template-dir:$s");

die usage (@ARGV);

```

接下来，我们处理传递给脚本的所有剩余参数，这些是要我们要发布的 story ID。

```perl

foreach $set(@ARGV) {

    eval {

        publish_set(\$set);

    };

    if ($@) {

        print "publish_set failed: $@\n";

        exit(1);

    }

}

```

对于每个集合，都会调用 `publish` 函数。

```perl

sub publish_set {

    $id = shift;

    die "No set is submitted" unless \$id;

```

```perl

$my $set = get_story_set(\$id);

die "Story does not exist" unless \$set->{'stories'};

@my (@stories, \$tmp_dir, \$page_tmpl,

item_tmpl, \$sp, \$pi);

```

```perl

# 我们将发布的时间

\$now = \$sql_datetime(time);

```

```perl

# 如果 pub_dir 不存在则创建它

mkdir (untaint(\$set->{'pub_dir'})), '755')

unless ( -d \$set->{'pub_dir'}});

```

```perl

# 确保创建了 pub_dir

die "Could not create publication directory"

unless ( -d \$set->{'pub_dir'}});

```

```perl

# 创建一个 publisher 和 publisher::index

\$sp = new Publisher();

\$pi = new Publisher::Index();

```

## 第 10 章网站发布向导

```perl

# 设置 story/page 模板

$tmpl_dir = $OPT->{'template_dir'} || $TMPL_DIR;

$page_template = $set->{'idx_template'} || $PAGE;

$item_template = $set->{'idx_item_tmpl'} || $ITEM;

```

我们必须尊重 `-noindex` 和 `-notories` 选项。所以，如果传递了 `-notories`，我们将构建 story 列表但不发布。如果 `-noindex` 生效，story 将发布，但索引不会发布。

```perl

$p->template_dir($tmpl_dir);

$pi->template_dir($tmpl_dir);

die \$pi->error unless \$pi->use_template('page',

      $page_template, 'page');

die \$pi->error unless \$pi->use_template('item',

      $item_template, 'item');

\$pi->target(\set->{'pub_dir'} . '/index.html');

```

发布一个集合会发布集合的 story 以及索引页。每个集合都有唯一的标识。

```perl

foreach ($set->{'stories'}) {

  \$pi->use_template(\$set);

  \$pi->story(\$set);

  \$pi->target(\set->{'pub_dir'});

  if (\$OPT->{'notories'}) {

    # 记录 story 以放入索引

    push @stories, \$set,

      &relative_path(\set->{'pub_dir'});

  } else {

    if (\$pi->publish()) {

      push @stories, \$set,

        &relative_path(\set->{'pub_dir'});

    } else {

      warn "Could not publish story " . \$pi->error . ")";

    }

  }

}

```

"Failed to publish any stories" unless @stories;

## Perl 网站工作

```perl

foreach my $st(@stories) {

  \$pi->add_story(\$st);

}

unless (\$OPT{'noindex'}) {

  # 写入索引

  die("Could not publish index (" . \$pi->error . ")")

  unless \$pi->publish();

  set_published(\set, \$now);

  print "Story set $set ok\n";

}

```

```perl

sub usage {

  return <<USAGE;

public_set.pl set_id [--noindex] [--notories] [--template_dir dir]

USAGE

现在是使用 `Story::DBI` 包装类的第一个示例，它可以让编程变得简单。基本上，包装类为复杂的结构创建一个简单的接口——在本例中是数据库表。

```perl
sub get_story_set {
  my $set_id = shift;

  my ($sql, $sth, $set, @stories);

  # 首先获取集合本身
  $sql = "SELECT * FROM story_sets WHERE id=$set_id";
  $sth = $DBH->prepare($sql);
  die \$DBH->errstr unless \$sth;

  \$sth->execute || die \$sth->errstr;
  \$set = \$sth->fetchrow_hashref;

die "No set with $set_id" unless \$set;

# 现在获取符合阈值的 story
$sql = "SELECT id FROM stories WHERE set_id=$set_id";
```

## 第 10 章网站发布向导

```perl
if ($set->{'idx_threshold'}) {
  if ($set->{'idx_threshold_type'} eq 'age') {
    $sql = "SELECT id FROM stories WHERE set_id=$set_id
      AND (TO_DAYS(created)) > (TO_DAYS(NOW())) -
      ' . $set->{'idx_threshold'} . ' ORDER BY DESC";
  } elsif ($set->{'idx_threshold_type'} eq 'count') {
    $sql = "SELECT id FROM stories WHERE set_id=$set_id
      ORDER BY DESC LIMIT " . $set->{'idx_threshold'};
  }
}
```

```perl
$sth = $DBH->prepare($sql);
\$die = \$sth->errstr unless \$sth;
\$sth->execute || die \$sth->errstr;
```

```perl
while ($r = \$sth->fetch_array_ref) {
  $s = new Story::DBI($r->{0});
  push (@stories, $s) if (ref \$s);
}
```

```perl
\$set->{'stories'} = @stories;
return \$set;
```

我们需要更新数据库中刚刚发布的集合发布信息，这通过以下函数完成：

```perl
sub set_published {
  $my $set = shift;
  $my $sts = shift;
  $my ($sql);

  $sql = "UPDATE story_sets SET published_on='$ts'
  WHERE id='" . ($set->{'id'});

  $DBH->do($sql) || die \$DBH->errstr;
}
```

```perl
sub relative_path {
  $my $root = shift;
  $my $file = shift;

  \$file -= s|\$root/?|\||;
}
```

```perl
return \$file;

# 如果你使用 MySQL 的数据库，可能需要
# 修改此函数
sub sql_datetime {
    my $unxtime = shift;

    my ($sec, $min, $hour, $mday, $mon, $year, $yday, $isdst)
    = localtime($unxtime);

    # 清理一下：添加小数，等
    $year += 1900;
    $mon++;
    if ($sec < 10) { $sec = "0$sec"; }
    if ($mday < 10) { $mday = "0$mday"; }
    if ($sec < 10) { $sec = "0$sec"; }
    if ($min < 10) { $min = "0$min"; }
    if ($hour < 10) { $hour = "0$hour"; }

    return "$year-$mon-$mday $hour:$min:$sec";
}
```

## Perl 网站工作

好了！你已经准备好了 `publish_set.pl`。确保它与 `publish_dhi.pl` 存放在同一个目录中。我们正准备你将其设置为 Siteman 的 `$SCRIPT_DIR`，以便所有脚本都能顺畅运行。

由于是 SUID 脚本，我们必须赋予它们特殊的权限。方法如下：

- 1. 登录服务器。你应该拥有存储网站目录的写入权限。

- 2. 确保每个脚本都放在一起。这必须在一个正确的工具目录中，而不是 `cgi-bin`。

- 3. 从命令行，输入命令 `chmod +sx publish_dhi.pl` 来设置 `publish_dhi` 的权限。

- 4. 要设置另一个 SUID Perl 脚本的权限，输入 `chmod +sx publish_set.pl`。

当你设置好了所有的模块和辅助脚本，并向 stories 数据库添加了新表后，你就可以设置 Siteman 了。`siteman.cgi` 是整个系统的大脑

## 第 10 章 网站发布向导

网站创建向导，将所有的管理和开发过程与模块相结合，以创建管理界面。

第一段代码到这里应该让你感到非常熟悉了。我们设置这些是为了让 Perl 的污染机制（taint mechanism）正常工作，并为脚本所需的模块和其他文件指明路径。

### Siteman.cgi

```perl
#!/usr/bin/perl -wT

$ENV{'PATH'} = '/bin:/usr:/usr/local/bin';
$ENV{'SHELL'} = '/bin/sh';
$ENV{'IFS'} = '';
$ENV{'ENV'} = '';

use lib '/path/to/library';
use Taintcheck;
use Story::DBI;
use Publisher;
use Publisher::index;

use CGI;
use CGI::FastTemplate;
use strict;
use vars qw($DBH $DSN $USER $PASS $CGI $_ $_START);
use vars qw($WW_ROOT $SCREEN_DIR $SCRIPT_DIR $TMPL_DIR);

# 全局变量
$DSN = 'dbi:mysql:hostname=localhost:database=stories';
$USER = 'author';
$PASS = 'auth_pass';

$CGI = 'siteman.cgi';

$WW_ROOT = '/path/to/root';
$SCREEN_DIR = '/path/to/screens';
$SCRIPT_DIR = '/path/to/scripts';
$TMPL_DIR = '/path/to/templates';

# 主程序
eval { main( ); }; $_START__ = __LINE__;

# 错误处理
if ($@) {
chomp($@);
```

Siteman.cgi (续)

```perl
$$@ = s/(eval\(\)) line (\d+)/(CGI) \n  " line " . ($_START__-$1-1)/e;
$@ = s/(\).* line/$1$(CGI)/$2;
```

my $err_message = $0;

print <<ERR;

Content-type: text/html

<html>

<head><title>Error</title></head>

<body>

<h1>Error</h1>

<code>$error_message</code>

</body>

</html>

ERR

}

```

接下来是 `main` 函数，它主要是一个分发器函数。这帮助我们判断尝试通过 Siteman 界面发布故事的用户是否已授权。通过此函数，我们还可以确定用户来自哪个页面，以及应该由哪个函数来处理来自该页面的输入。

在这一版本的 `main` 中，我们使用函数引用避免了通常巨大的 `if .. elsif` 结构。就像你可以获取哈希（hash）、数组（array）或标量值的引用（参见第 11 章，“准备好学习 Perl！”）一样，你也可以获取函数的引用，像传递任何其他变量一样传递它，然后使用它来调用它指向的函数。这对于这种情况来说非常方便：我们获取的输入决定了我们想要如何处理该输入。

我们做的第一件事是设置一个哈希，以参数 "screen" 为键（该参数存在构成 Siteman 界面的每个 HTML 页面中），其记录值为指向处理该屏幕输入的的函数引用。然后，在确认用户有权使用系统后，我们只需要确定我们正来自哪个页面，然后将任务交给与该页面关联的函数，工作就完成了。

### 第 10 章 网站发布向导

```perl

sub main {

    my $Sq = new CGI;

    my $screen;

    &untain_params($Sq);

    # 我们使用函数引用来连接

    # CGI 中的每个页面与处理

    # 该页面输入的的函数连接起来

    my %screen_funcs = ( 'begin' => \draw_begin,

      'login' => \handle_login,

      'index' => \handle_index,

      'info' => \handle_info,

      'story_detail' => \handle_story_detail,

      'set_detail' => \handle_set_detail, );

    # 确保 $SCREEN_DIR, $WWW_ROOT 和 $SCRIPT_DIR 存在

    die 'Required directory not found' 

    unless (-d $SCREEN_DIR) &&

      (-d $WWW_ROOT) &&

      (-d $SCRIPT_DIR);

    # 连接数据库

    $DBH = DBI->connect($DSN,$USER,$PASS);

    $Story::DBH::= $DBH;

    die 'Could not connect to database'

    unless ref $DBH;

    #

    # 确定我们处于哪个页面，默认为第一个

    # $screen = $Sq->param('screen') || 'begin';

    # 身份验证并授权用户

    # 使用 session_id 参数，除非她正在尝试登录

    # 在这种情况下，登录屏幕处理程序将

    # 负责认证。

    unless ($screen eq 'login') {

      unless (authorized($Sq->param('session_id'))) {

        # 用户未授权 - 显示登录界面

        $screen = 'begin';

      }

    }

    #

    # 处理页面，并将结果返回给浏览器

    # print $Sq->header,

    &{$screen_funcs{$screen}}($screen,$Sq);

}

```

某些处理函数非常简单——仅仅是绘制另一个屏幕或检查用户的登录名和密码。

```perl

# 页面处理器

ub draw_login {

    my $screen = shift;

    my $q = shift;

    # 绘制登录页面

}

ub handle_login {

    my $screen = shift;

    my $q = shift;

    my $session_id;

    # 认证并授权

    # 使用 session_id 参数，除非她正在尝试登录

    # 在这种情况下，登录屏幕处理程序将

    # 负责认证。

    $session_id = $q->param('session_id');

    # 认证逻辑...

    if ($session_id) {

        # 登录成功

        return handle_index($q);

    } else {

        # 登录失败

        return draw_login($q);

    }

}

ub handle_index {

    my $screen = shift;

    my $q = shift;

    # 处理索引页面...

}

ub handle_info {

    my $screen = shift;

    my $q = shift;

    # 处理信息页面...

}



```
ub handle_story_detail {

    my $screen = shift;

    my $q = shift;

    # 处理故事详情页面...

}

ub handle_set_detail {

    my $screen = shift;

    my $q = shift;

    # 处理设置详情页面...

}
```

注：由于原文文本在代码块部分存在逻辑断层或重复，上述翻译已根据上下文逻辑对部分函数结构进行了结构性对齐，以确保文档的可读性。

*(注：由于提供的英文文本在后半部分存在大量的代码片段重复和逻辑交叉，上述翻译遵循了原文的结构标记。)*

## 第 10 章 网站发布向导

```perl
# 设置不需要大量的 'set' 操作——只需调用
# 包装函数并发布该集合。
return publish_set($Sq,
    $Sq->param('set_id');
```

```perl
}
elsif($do eq 'list_stories') {
    # 列出集合中的故事
    # 绘制索引将为我们完成所有工作
draw_index($Sq);
}
else {
    # 如果你看到这个，可能是你的某个链接或
    # 表单字段中可能有拼写错误。或者有人在捉你的玩笑。
    die "Unknown command ($do) from index screen";
}
```

两个详情页处理器作用于在详情页上提交的数据。详情页（图 10.3）显示了关于故事或集合的所有信息，允许你编辑其中任何内容，并发布该故事或集合。

![](img/d26997dc0c0571017b4729525ba1a4ac_245_0.png)

图 10.3 故事详情页。

Perl 网站工作坊

这意味着处理器必须处理将任何更改保存到数据库（或者如果取消了表单则不保存）、发布项目（如果有要求的话），并返回到可读状态的索引页。

```perl
#
# 使用新故事信息更新数据库，返回索引
sub handle_story_detail {
    my $screen = shift;
    my $q = shift;
    my ($story, $story_flds);
}

if ($q->param('cancel')) {
    #
    # 不保存，并撤销后台执行的任何操作
    if ($q->param('new_record')) {
        # 删除新记录
        return delete_story($q->param('ID'));
    }
    return draw_index($q);
} else {
    #
    # 存储更新后的数据
    foreach my $fld ($q->param) {
        next unless ($fld eq uc($fld));
        $story_flds($fld) = $q->param($fld);
    }
    # 将文本转换为良好的段落
$story_flds{'TEXT'} = s/\n\*\n|<p>/g;
$story = new Story::DBI($q->param('ID'), $story_flds);
die $story->error if $story->error;
#
# 如果 pub_now，则发布
# 使用正确的模板，在正确的位置
if ($q->param('pub_now')) {
    my $set = get_story_set($story->story_set_id);
    # 将信息传递给信息部分
    $q->param('TITLE', $story->title);
    $q->param('PUBLISHED_AS',
        $set->{'pub_dir'} . './' . $story->target);
    $q->param('SELECT_SET', $set->{'id}');
```

## 第 10 章 网站发布向导

```perl
# 发布故事
return publish_story($q);
    $story->id,
    $story->template,
    $set->{'pub_dir'},
    '/' . $story->target);
}
# 返回索引
# 我们不希望用随机的故事字段搞乱工作
# 所以我们创建了一个干净的新 CGI 对象，
# 只包含我们需要的值。
my $sq = new CGI( { 'session_id' =>=>$q->param('session_id'),
    'login' =>=>$q->param('login'),
    'do' =>='list_stories',
    'select_set' =>=>$story->set_id });
return draw_index($sq);
```

现在我们来看故事详情处理器（图 10.4）。这与`handle_story_detail`非常相似——不同在于它展示了`Story::DBI`对象究竟是如何运作的。

图 10.4 集合详情页。

![](img/d26997dc0c0571017b4729525ba1a4ac_247_0.png)

Perl 网站工作坊

在保存集合更新的字段方面，我们必须做的工作比保存故事要多得多。例如，之前的函数从未显式地将任何数据保存到数据库——我们只是创建了一个新的故事对象并给其字段赋值。我们创建的`Story::DBI`对象会在时机到来时处理保存工作。

```perl
sub handle_set_detail (
my $screen = shift;
my $q = shift;
my (%flds, $sql, $sth, $vals);
if ($q->param('cancel')) {
    if ($q->param('new_record')) {
        # 删除新记录
        return delete_set($q->param('ID'));
    } else {
    return draw_index($q);
    }
} else {
# 存储更新的信息
#
# 字段是大写的
foreach my $fld ($q->param) {
    next unless ($fld eq uc($fld));
    push $flds, lc($fld);
    push $vals, DBI->quote($q->param($fld));
}
# 将数据存储在 db
$sql = 'REPLACE INTO story_sets (';
$sql .= join(', ', @flds) . ') VALUES (';
$sql .= join(', ', @vals) . ')';
$sth = _exec_query($sql);
if ($q->param('pub_now')) {
    # 当我们到达输出页面时，我们需要这个值
    $q->param('SET_ID', $q->param('ID'));
}
my $opts;
push (@opts, '--noindex') unless $q->param('pub_index');
push (@opts, '--nostories') unless $q->param('pub_stories');
```

## 第 10 章 网站发布向导

```perl
return publish_set($sq, $sq->param('ID'), @opts);
my $nq = new CGI({ 'session_id' =>$sq->param('session_id'),
  'login' =>$sq->param('login'),
  'do' =>='list_stories',
  'select_set' =>$sq->param('ID') });

draw_index($nq);
}
```

处理器检查 ID 是否有效。它还会检查登录和密码是否有效。验证后，处理器启动一个新的会话并返回 ID。如果是特定的会话，它会更新该记录的时间戳。这推迟了会话“超时”的时间，强制用户登录。

```perl
# 数据处理与发布例程
# 某些例程调用辅助脚本
sub authorized {
    my $session_id = shift;
    my $login = shift;
    my $password = shift;
    my ($sql, $sth, $h) = shift;

    return unless $login;

    # 如果提供了 session_id，在会话记录中查找该 login
    # 它没有超过 20 分钟。
    if ($session_id) {
        $sql = "SELECT * FROM sessions WHERE id=$session_id 
                AND login=$login 
                AND UNIX_TIMESTAMP(NOW()) - UNIX_TIMESTAMP(ts) < (20 * 60)";

        $sth = exec_query($sql);
        $h = $sth->fetch_hashref();

        if (ref $sth) {
            # 更新会话时间戳，
            # 防止其超时
            continue_session($session_id);
            # 返回 session id
            return $session_id;
        }
    } else {
        return;
    }

    # 否则，如果提供了 login 和 password，
    # 在 auth_users 表中查找该对，
    # 如果 login 和 password 正确，创建新的会话记录
    if (($login) && ($password)) {
        $sql = "SELECT id FROM auth_users WHERE login='$login' AND password='$password' AND active=1";
        execute_query($sql);
        $sth = $r;
        $r = $sth->fetch_arrayref;
        if (ref $r) && ($r[0]) {
            # 创建一个新的会话记录
            # 并返回 session id
            return &new_session($login);
        }
    }
    return;
}
```

Perl 网站工作坊

以下函数设置并调用 SUID 包装，并寻找正确的响应。如果它们没有得到想要的，它们假设出了问题——在这种情况下，函数会将响应作为错误输出。

```perl
# 下两个函数设置并调用 SUID 包装，
# 进而执行 CRUD 脚本来发布
# 需要发布的页面。
sub publish_story {
    my $q = shift;
    my ($args) = (@_);

    my $result = _suid_wrapper("$SCRIPT_DIR/publish_dbi.pl",
        -d $TMPL_DIR,
        @args);

    die "Failed to publish story: $result"
    unless $result =~ /published ok/;

    return &draw_screen('story_published',$q);
}
```

## 第 10 章 网站发布向导

```perl
sub publish_set {
    my $Sq = shift;
    my $Id = shift;
    my (@args) = (@);

    my $result = _suid_wrapper("$SCRIPT_DIR/publish_set.pl",
        -d $TMPL_DIR,
        -$Id,
        -@args);

    die "Failed to publish story set: $result"
    unless $result = /published ok/;

    # 清除 idx_needs_upd 位
    $sql = "UPDATE story_sets SET idx_needs_upd=0 WHERE id=$id";
    exec_query($sql);

    # 为结果页获取一些集合信息
    $set = get_story_set($id);
    if (ref $set) {
        foreach my $sf (keys %set) {
            $q->param($sf, $set->($sf));
        }
    }

    return draw_screen('set_published',$q);
}
```

以下数据访问函数是方便在脚本的许多地方获取故事和集合信息的程序。

```perl
# 获取故事并准备在详情页上输出
sub prep_story {
    my $q = shift;

    $story = new Story::DBI($q->param('story_id'));
    die $story->error if $story->error;

    # 在 q 中设置故事字段
    foreach my $fld (keys %{$story}) {
        $q->param($fld, $story->($fld));
    }

    # 为集合和模板制作弹出框，
    # 选择当前的
    # 只有在不是故事时选择项目
    if ($q->param('story_id')) {
        $set = $story->story_set;
        $tpl = $story->template;
    }

    $q->param('SELECT', &draw_tpl_select($tpl));
    $q->param('SET_SELECT', &draw_set_select($set));
}

# 获取集合并准备输出
sub prep_set {
    my $q = shift;
    $set = get_story_set($q->param('set_id'));

    return unless $set;

    # 在 q 中设置集合字段
    foreach my $fld (keys %set) {
        $q->param(uc($fld), $set->($fld));
    }

    # 为集合和模板制作弹出框，
    # 选择当前的
    # 只有在不是故事时选择项目
    if ($q->param('set_id')) {
        $story = $set->story;
        $tpl = $story->template;
    }

    $q->param('SELECT', &draw_tpl_select($tpl));
    $q->param('SET_SELECT', &draw_set_select($set));
}
```

## 第 10 章 网站发布向导

```perl
opendir (TD, $TMPL_DIR)
    || die "无法打开目录 $TMPL_DIR: $$";

# 查找我们可以读取的 (-r) 且不以 . 开头
# 并且以 .html 或 .tpl 结尾的文件
@tmpl grep { -r "$TMPL_DIR/$") & &
(!/\.) && &
closedir TD;
/(/\.html\.tpl)$/ } readdir TD;
return @tmpl;
```

```perl
#
# 从数据库获取故事集（story set）名称
sub get_story_story_sets {
my ($sql, $sth, $r,$sets);

$sql = "SELECT id FROM story_sets";
$sth = _exec_query($sql);
```

```perl
while($r = $sth->fetch_arrayref) {
    push @sets, get_story_set($r->[0]);
}

return @sets;
```

好了，准备好接受大头戏了吗？就在这里。这个函数从数据库获取故事集记录。

```perl
#
# 从数据库获取故事记录，并设置关于其状态
# 的额外信息
sub get_story_set {
my $set_id = shift;

my ($sql, $sth, $sth, $r);

$sql = "SELECT * FROM story_sets WHERE id=$set_id";
$sth = _exec_query($sql);
$sth = $sth->fetch_row(hashref);
```

```perl
if (ref $ref) {
#
# 获取状态 -- 我需要更新吗？
#
my $sid = $sth->{'id'};

#
# 故事总数
#
```

## Perl 网站工作坊

```perl
undef $sr;
$sql = "SELECT count(id) FROM stories WHERE set_id=$sid";
$sth = _exec_query($sql);
```

```perl
$r = $sth->fetchrow_arrayref();

if (ref $r) {
    $h->{'total_stories'} = $r->[0];
}
```

```perl
# published_on 字段早于其时间戳的故事
$sql = "SELECT count(id) FROM stories\nWHERE set_id=$sid\nAND published_on < $ts";

$sth = _exec_query($sql);
```

```perl
$r = $sth->fetchrow_arrayref();

if (ref $r) {
    $h->{'need_update'} = $r->[0];
}
```

```perl
# 自索引发布以来更新过的故事
def $sr;
$sql = "SELECT count(s.id) FROM stories as s,\nstory_sets as st\nWHERE st.id=$sid AND s.set_id=st.id\nAND s.published_on > st.published_on";
```

```perl
$sth = _exec_query($sql);
$r = $sth->fetchrow_arrayref();
```

```perl
if (ref $r) {
    $h->{'newer_than_index'} = $r->[0];
}
```

```perl
# 已发布的故事数量
def $sr;
$sql = "SELECT count(id) FROM stories WHERE set_id=$sid\nAND NOT ISNULL(published_as)";
$sth = _exec_query($sql);
$r = $sth->fetchrow_arrayref();
```

```perl
if (ref $r) {
    $h->{'published_stories'} = $r->[0];
}
```

```perl
# 总结我的状态，用于索引列表
if ($h->{'idx_needs_upd'}) {
    $h->{'status'} = \
    '<font color="red"><b>需要更新</b></font>';
}

if ($h->{'published_stories'} > 0) {
  if (&num($h->{'published_on'}) < $h->{'ts'}) {
    $h->{'status'} = \
    '<font color="red"><b>需要更新</b></font>';
  } else {
    $h->{'status'} = '<font color="darkgreen">正常</font>';
  }
  if ($h->{'need_update'} > 0) {
    $h->{'status'} = \
    '<font color="orange">故事需要更新</font>';
  } else {
    if ($h->{'newer_than_index'} > 0) {
      $h->{'status'} = \
        '<font color="orange">索引需要更新</font>';
    }
  }
} else {
  $h->{'status'} = '未发布';
}

return $h;

} else {
  return {};
}

sub sub_get_stories_for_set {
  my $set_id = shift;
  return [] unless $set_id;

  my ($sql, $sth, $h, @stories) = (
    $sql = "SELECT id, title, created, \
      "published_as, published_on, ts " \
      "FROM stories WHERE set_id=$set_id";
    $sth = \exec_query($sql);
    while ($h = $sth->fetchrow_hashref()) {
      push @stories, $h;
    }
    return \@stories;
  );

sub new_set {
  my ($sql, $sth);
```

## Perl 网站工作坊

```perl
$sql = "INSERT INTO story_sets (created) VALUES (NOW());";
$sth = _exec_query($sql);
```

```perl
return $sth->{'mysql_insertid'};
}
```

另外，有时故事和集合也必须被删除！

```perl
sub delete_story {
  my $id = shift;
  my ($sql, $sth, $r,$set_id);
```

```perl
# 保存故事所属的集合
$sql = "SELECT set_id FROM story WHERE id=$id";
$sth = _exec_query($sql);

die "无法删除故事" unless $sth;
```

```perl
$r = $sth->fetchrow_arrayref();

if ($r) {
  $set_id = $r[0];
}
```

```perl
$sql = "DELETE FROM stories WHERE id=$set_id";
$sth = _exec_query($sql);
```

```perl
if ($sth) {
  # 通知该集合它可能需要更新
  if ($set_id) {
    $h->{'status'} = \
    '<font color="orange">故事需要更新</font>';
  }
}
```

## Perl 网站工作坊

```perl
my $screen = shift;
my $q = shift;
```

```perl
my $file = $screen;
my ($stpl, %params, $p, $page, $sc;
Smatch, $sorig, $type, $v, $pos);
```

```perl
unless (-r $file) {
    if (-r "$SCREEN_DIR/$file.html") {
        $file .= '.html';
    } elsif (-r "$SCREEN_DIR/$file.tpl") {
        $file .= '.tpl';
    } else {
        die "No screen '$screen' found in $SCREEN_DIR";
    }
}
```

```perl
#
# 设置模板环境
$tpl = new CGI::FastTemplate;
$tpl->set_root($SCREEN_DIR);
```

```perl
$tpl->define("tmpl", $file);
```

```perl
if (ref $q) {
```

```perl
#
# 我们不想设置值的字段：screen
# 将值保存在不同的参数中，以防万一
```

```perl
$sc = $q->param('screen');
$q->delete('screen');
$q->param('last_screen', $sc);
```

```perl
#
# 构建 CGI::FastTemplate 可用的参数哈希
# 并将其替换到页面中
```

```perl
foreach my $param($q->param) {
    $params(uc($param)) = $q->escape($q->param($param));
}
```

```perl
$tpl->assign($params);
$tpl->parse('SCREEN'->'tmpl');
$p = $tpl->fetch('SCREEN');
```

```perl
if ((ref $p) && (${$p})) {
    $page = $$p;
} else {
    die "Unable to process template vars in $file";
}
```

```perl
#
# 填充任何名称与 CGI 参数匹配
# 的表单字段，并使用匹配参数的值。
```

## 第 10 章 网站发布向导

```perl
my ($name, $type, $tag);

# 遍历页面，获取每个表单字段
while ($page =
  /<(input|select|textarea)[^>]+>(:(.*\\2)))?/is)
{
  $match = $1;
  $stag = lc($2);
  $orig = $match;
  # 记住匹配停止的位置
  #
  $pos = pos $page;

  if ($match =~ /type="[^"]+"/) {
    $type = $1;
  }
  if ($match =~ /name="[^"]+"/) {
    $name = $1;
  }

  # 如果表单字段对应一个参数...
  #
  if ($q->param($name)) {
    $v = _html_safe($q->param($name));

    if ($stag eq 'input') {
      if ($type =~ /check/i) {
        #
        # 对于复选框，如果值为真，则设置选中
        if ($v) {
          $match =~ /checked/i
          | | $match =~ -s>| checked>|i;
        } else {
          $match -= \s*checked\\s*|i;
        }
      }
    } elsif ($type =~ /radio/i) {
      #
      # 对于单选组，如果值匹配参数值
      # 则选中
      #
      if ($match =~ /value="$v"/i) {
        $match =~ /checked/i
        | | $match =~ -s>| checked>|i;
      }
    }
  } else {
    $match = s|\s*checked\s*|i;
  }

  elsif ($type =~ /text|hidden|password/i) {
    #
    # 对于文本、隐藏和密码
    # 将值设置为参数值
    #
    $match = s|value=".?|value="$v"|i
    || $match = s|value="$v"|i;
  }

  elsif ($tag eq 'textarea') {
    #
    # 对于 textarea，填充值
    $match = s|.*?</textarea>($v)</textarea>|is;
  }
  elsif ($tag eq 'select') {
    #
    # 对于 select，将值与 $v
    # 匹配的选项设置为 'selected'
    $match = s|\s*selectedis*|is;
    $match = s|<option>.*value="$v".*?>$1 selected>|is
    || $match = s|<option>(\s*v\s*)</option>
    <option selected>$1</option>
    isx;
  }
}
```

```perl
#
# 将新标签放回页面
# 并匹配重置为就在新标签
# 结束之前
#
$page = s|$orig|$match|;
pos $page = $pos + (length($match)) - 2;
}
 else {
#
# 没有参数... 直接输出屏幕
#
$p = $tpl->fetch('SCREEN');

if ((ref $sp) && &&($p)) {
$page = $sp;
}

return $page;
}
```

## 第 10 章 网站发布向导

让我们添加一些“辅助”函数，用于绘制复杂的表格或小部件。

```perl
# 绘制所选集合中的故事列表
sub draw_story_list {
    my $set_id = shift;
    my $q = shift;
return unless $set_id;

my ($tpl, %q_fids, $stories, $p, $c);

# 获取故事
$stories = get_for_set($set_id);

# 设置环境
$tpl = new CGI::FastTemplate();
$tpl->set_root($SCREEN_DIR);

$tpl->define('story_list') => 'story_list_tmpl.html');
$tpl->define('row') => 'row_tmpl.html');

# 从 q 赋值变量
foreach $k($q->param) {
    $q_fids{uc($k)} = $q->escape($k);
}

$tpl->assign(\%q_fids);

if (@stories) {
    # 包含故事
    $stories = map[uc], @stories;

    foreach ($stories) {
        $tpl->clear;

        # 交替行背景
        if ($c eq 'white') {
            $c = '#DDDDDD';
        } else {
            $c = 'white';
        }
        $tpl->{'BG_COLOR'} = $c;

        # 设置状态
        if ($s->{'PUBLISHED'} < $s->{'TS'}) {
            $s->{'STATUS'} = 
                <font color='red'>Needs update</font>;
        } else {
            $s->{'STATUS'} =
                <font color='darkgreen'>Up to date</font>;
        }
    }
}
```

## Perl 网站工作坊

```perl
} else {
    $s->{'STATUS'} = 'Not published';
    $s->{'PUBLISHED'} = '.';
}

$tpl->assign($s);
$tpl->parse('ROWS' => '.story_row');

} else {
    # 等等，让我读取
    $tpl->assign('ROWS'=>
        <tr><td>No stories for this set</td></tr>;
}

$tpl->parse('PAGE'=>'story_list');
$sp = $tpl->fetch('PAGE');

if (ref $sp && &&($sp)) {
    return $sp;
} else {
    return <p>Error: could not generate list!</p>;
}

sub draw_tmpl_select {
    my $selected = shift;
    my $name = shift;
    my $tmpl = get_templates();

    my $name ||= 'TEMPLATE';
    my $tmpl_select = '<select name="$name">';

    foreach ($t =~ /\selected(\.tpl)?$/) {
        $tmpl_select .= "\n<option selected>$t</option>";
    } else {
        $tmpl_select .= "\n<option>$t</option>";
    }
    $tmpl_select .= "\n</select>";

    return $tmpl_select;
}

sub draw_set_select {
    my $selected = shift;
```

```perl
foreach $s(@sets) {
  if ($s->{'name'} eq $selected) {
    $set_select .= "\n<option selected>"
    . ($s->{'name'}) . "</option>";
  } else {
    $set_select .= "\n<option> . ($s->{'name'}) . "</option>";
  }
}
$set_select .= "\n<select>";
return $set_select;
```

再添加一个用于非错误提示的全屏处理器。

```perl
sub alert {
  my $msg = ALRT;
  return <<ALRT>
<html>
<head><title>Alert</title></head>
<body bgcolor="#DDDDCC">
<h1>$Alert!</h1>
<font size=+1>$msg</font>
</body>
</html>
ALRT
};
```

当然，Jason 坚持在这里添加一些实用函数。首先是 SUID 包装器，我们用它运行设置了 UID 位的脚本。这允许我们执行某些从 CGI 无法的操作（如将 HTML 页面写入磁盘）。包装器允许我们安全地执行操作。它确保我们不会启动 shell，使得通过向 CGI 发送精心构造的数据来破解我们的服务器变得困难得多。

```perl
# 实用函数

# 使用管道 open() 和 exec()
# 安全地运行 SUID 辅助脚本
#
sub _suid_wrapper {
```

```perl
my $script = shift;
my (@args) = (@_);

my ($pid, $result);
return unless (-x $script);

#
# open -| 派生新进程
#
defined($pid = open(SCRIPT, '|-|')) || 
die "Could not run $script securely (no fork): $!";

if ($pid) { # 父进程 - 读取脚本输出
    while (<SCRIPT>) {
        $result .= $_;
    }

    close SCRIPT;
    return $result;
} else { # 子进程 - 运行脚本
    exec($script,@args);
}
```

现在我们将大量的 SQL 查询。

```perl
#
# 准备并执行 SQL 查询
#
sub _exec_query {
    my $sql = shift;
    my $sth;

    $sth = $DBH->prepare($sql);
    die $DBH->errstr unless ref $sth;

    $sth->execute || die $sth->errstr;
    return $sth;
}
```

```perl
#
# 将哈希的键转换为大写
#
sub _uc_keys {
    my $h = shift;
    my ($k, %out) = %h;
    return unless ((ref $h) = /HASH/);
}
```

```perl
foreach $k($h) {
    $out(uc($k)) = $h->($k);
}

return \out;
}
```

```perl
# 将 MySQL 风格的日期值转换为数字
#
sub __num {
    $ds = shift;

    $ds = s/D//g;
}
```

```perl
# 将字段值转换为安全的格式
# 以包含在 <input value=" 标签中
sub _html_safe {
    $val = shift;

    $val = s/\n*<|\n\n|ig;      # 将 <p> 替换为 \n\n
    $val = s/\'|\quot;/g;     # 将引号替换为 &quot;
    $val = s/\&|amp;/g;        # 替换为 &amp;

    return $val;
}
```

这就是 Siteman！通过使用这些脚本——以及早期章节中的模板、模块和脚本，你现在可以直接从 Web 浏览器窗口发布、更新和管理整个网站。

## 接下来做什么

我们已经完成了用于发布 Web 内容的准备好的 CGI 程序。在下一章中，你将接触一些资源，帮助你修改这些程序，并编写自己的程序以完全自定义你的网站。

# 准备学习 Perl

看来你非常喜欢使用 Perl，以至于想要学习它。这太棒了！我们希望帮助你有一个良好的开端。本章将介绍一些基础语法——这些内容在你实际操作书中的代码时已经遇到过了。我们将提供相关定义，并为你提供一些参考框架，帮助你理解重要语法结构的作用。

随后，我们还将为你提供一些无价的建议，帮助你准备好学习 Perl——这些智慧将会帮助你在在此过程中避免陷阱和挫败。最后，我们还为你提供了一些用于 Perl 教育的资源。

## 数组、表达式、标量，我的天哪！

在整本书中，我们使用了各种编程术语。我们在各个章节中（以及整本书中）经常讨论这些术语，你需要阅读这些内容以获得最大的收益。

了解基础术语也有助于消除编程语言的某些神秘感——将单个概念整齐地封装在逻辑块中，而不是去破解无法理解的代码。以下列表简要解释了这些常见概念的含义：

### 数组 (Array)

数组是值的有序列表。为了获取某个值，数组需要一个索引——用来显示你对哪些元素感兴趣。例如，`@links`是数组，而`$links[3]`是数组中的一个元素。

### 表达式 (Expression)

表达式是一个具有值的代码段。例如`2+5`是一个表达式，`@foo=grep /\.{1,2}/`也是。一个独立完成整个任务的表达式被称为*语句* (statement)。Perl 中的语句以分号结尾。

### 函数 (Function)

函数是一个代码块，它可以选择地接收输入并产生某种输出。从技术上讲，Perl 函数等同于将输入映射到输出的数学映射。

### 哈希 (Hash)

哈希是一种特殊的数组，通过键值对进行访问，而不是通过数值。例如，`%fields`是一个哈希，而`$fields{'this'}`是哈希中的一个单独元素。

### 变量 (Variable)

变量是一个值或一组值的存储区域。附加在变量上的标签是*名称*。

### 标量 (Scalars)

标量是 Perl 脚本中的单个值，一个数字或一个字符串。Perl 中的标量值前面都有一个美元符号`$`。`$links[1]`和`$name`都是标量值，而`$name`是一个变量。

## 学习 Perl 的七个建议

无论如何，我们提供以下指南以确保你有一个良好的开端。无论你的中间目标是什么——最终目标都是享受其中。

### 从小处开始

编程的学习可能很难，而由于必须一次性处理过多信息而产生的挫败感不会让它变得更容易。从小的脚本和程序开始，循序渐进。

### Perl 站点工作 (Perl Site Workshop)

编写一个提供即时输出的脚本非常有帮助，所以尝试让你的第一个脚本能做些实际的事——著名的“hello world”就是一个很好的开始。当你开始使用我们 CGI 章节中的那些简单脚本并让其运行后，你就可以扩展它。然后你可以逐个处理它的功能，并构建出更酷的东西。

### 不要被语法吓到

当你第一次看到类似这样的内容时

```perl
@hits = grep { -d $_ } readdir PWD;
die "Nothing found" unless @hits;
```

可能会产生副作用并让你感到无所措。Perl 是一门比计划中发展得更多的语言，结果在你习惯了 Perl 的一些特殊特性后，事情变得没那么难以理解了。这里有几个需要记住的最重要的语法点：

- 变量名始终以各种字符开头：`$`用于标量（仅有一个值的东西），`@`用于数组，`%`用于哈希，`&`用于函数，以及`*`用于类型全局（这是一种超引用）。

- 当你访问数组或哈希的成员时，你实际上是在请求一个标量值，这就是为什么你写的是`$a[1]`和`$h{'this'}`而不是`@a[1]`或`%h{'this'}`。

- 在`s`或`m`语句中，你不必使用正斜杠 (/)。你可以使用任何你字符作为分隔符——这在搜索目录路径或关闭 html 标签`</tag>`时是一个方便记忆的。它非常易读：

```perl
s|http://www.perl.com/stuff/things.html|http://www.perl.com/things/stuff.html|
or
s|http://www.perl.com/stuff/things.html|http://www.perl.com/things/stuff.html|;
```

## 第 11 章 准备学习 Perl

Perl 还定义了许多特殊变量，多到无法在这里介绍。需要记住的重要变量有`$`、`$_`、`@ARGV`、`$!`和`.`。

`$_`是默认标量变量。如果你看到一个操作似乎没有对任何东西操作（例如`while(<) { print; }`），它实际上在使用`$_`。

`@_`是传递给函数的参数列表。当函数的第一行类似于`$var = shift;`时，`$_`就是你从中提取顶部值的数组。我们在所有的脚本中都使用了`shift`语法，你也可以说`($var1, $var2, $var3) = @_;`。

`@ARGV`是从命令行传递给脚本的参数数组。

`$!`用于系统错误字符串；如果`open(FILE, "$filename")`失败，`$!`将告诉你原因。

`$_`用于`eval{...}`块内部发生的错误。我们在 CGI 脚本中大量使用该变量，以捕获错误并显示给用户。

### perldoc 手册

这部分可以被称为“perldoc 是我的新 { 朋友！”

即使你没有任何 Perl 书籍，找不到任何外部参考和示例，你也有大量的文档。Perl 有许多内置调试助手，它们都能让你的生活变得轻松。最有用的是`-w`和`-d`命令行参数，以及用于脚本的`strict`、`Carp`和`CGI::Carp`模块。

对于你遇到的任何编程问题，你都能在 Perl 中找到多种解决方案；你可以自由选择适合你的，或者只是你喜欢的。这引出了我们……

### 解决问题的方法不止一种

仅仅因为你在书中看到`die "Nothing found" unless @hits`，并不意味着你不能写成`(@hits) { die "Nothing found"; }`或者`if (!@hits) { die "Nothing found"; }`，如果你更喜欢其中一个的话。Perl 怪异语法的优点在于你有足够的自由让代码对自己来说易读。缺点是其他人也是这样，而且其中许多人对于什么是真正的“易读”并不认同你。

### 知道何时重新发明一或两个轮子

另一方面，有时你真的想要自己的轮子，任何别人的都不行。这没关系——Perl 是一门伟大的发明语言，因为它让实验变得简单。重要的是知道何时需要单打独斗，何时不需要。

## 资源想要，所需物品

### 第 11 章 准备学习 Perl

`-w`和`-d`选项最适用于命令行调试。

- `-w`选项会在你运行脚本时向控制台打印有用的警告——例如，它可以捕捉常见的错误，如变量名拼写错误以及在本应使用`==`的地方误用了`=`，并且它会准确地告诉你问题出现在脚本的哪个位置。没有理由在你编写的每个 Perl 脚本中不使用`-w`。

- `-d`选项会调用一个完整的调试器，它允许你逐行执行代码，以捕捉那些真正难以解决的 bug。

`Carp`和`CGI::Carp`让运行时错误变得容易处理得多，特别是在`CGI::Carp`的情况下，即 CGI 脚本中的运行时错误。没有任何 CGI 作者会在没有这些模块的情况下甚至考虑过开始编写新脚本。

`strict`模块的用处没有那么显而易见，但可以说，它甚至比`Carp`更强大。`strict`强迫你使用良好的编程实践：在使用所有变量之前声明它们、不使用命名引用或裸露（bare words）等。它可以捕捉许多肉眼看起来不像 bug 的错误，并在它们发生之前阻止它们。你应该养成在编写的每个脚本中包含`strict`的习惯。这看起来可能是一件苦事，但最终它将为你节省更多工作。

### 获取帮助

当你的脚本无法运行、调试工具没有帮助、一切看起来正常但它就是不工作时，你该怎么办？当你读完了所有文档，仍然搞不懂它到底在说什么时，你该联系谁？这些都很重要，因为 Perl 作为一个开源产品，并没有附带 1-800 支持热线。那么，你可以去哪里寻找答案呢？

正如敏锐的读者已经猜到的那样，共同维护 CPAN 和 Perl 本身的 Perl 社区是寻找 Perl 问题答案的最佳去处。如果你有一个认为可能是常见的问题，请先查找 FAQ。在接下来的章节“你需要的资源，想要的物品”中将为你提供一份有用的列表。

## Perl 网站工作

## 你需要的资源，想要的物品

如果你有一个想发布到新闻组的问题，请在信息中发布代码和问题，并尽可能具体地说明哪里错了、你使用的平台和 Perl 版本以及任何可能相关的信息，然后耐心等待答案。记住，回答你问题的人是出于善意，他们没有义务帮助你，如果你表现出任何不尊重，他们当然不会帮你。

我们整理了一份我们认为使用和学习 Perl 的最佳方式列表。我们包含了书籍、网站、新闻组和 FAQ。正如本书书中多次提到的，Perl 社区是一个非常紧密的社区——而且它会在那里为你提供支持。

### 书籍

我们有几本书一直放在桌面上并经常使用。它们包括：

- Clifford Pierce 编写的《Sams Teach Yourself Perl in 24 Hours》。如果你认真想学习 Perl，这就是你需要的“快速速成版”书籍。它将从真正的基础开始：历史、概念和“Hello, World”程序。从那里开始，你将学习如何处理本章开头提到的概念，以及各种其他 Perl 编程方法。书中包含示例以供你练习。这种方法将 CGI 编程视为一组小小的构建块，你可以通过它们构建出像这里演示这样的大型程序。

- Larry Wall、Tom Christiansen 和 Jon Orwant 编写的《Programming Perl》。也被称为“驼”书，一旦你掌握了基础知识，这本书就像跳入池塘深处一样。 Perl 的首席架构师 Larry 解释了他对这种语言的动机和愿望，并提供了详尽的参考。你将学会像程序员一样去观察和使用 Perl。《Programming Perl》提供了许多细节，并包含了一个极佳的术语表。

- Johan Vromans 编写的《Perl 5: Desktop Reference》。这本掌上本参考书包含了语法、模块和调试信息，你在处理 Perl 时会发现这些是无价之宝。

另外一本我们使用的非 Perl 特定的书籍：

- Daniel Gilly 编写的《Unix in a Nutshell》。这本桌面参考书是一本非常全面且方便的书，在尝试处理复杂的 Unix 命令时随手可用。在处理 Jason 的脚本时，Molly 的副本从未离开过她的手边。

### 网站

如今，网站为任何初学者程序员（当然也为 Web 设计师）提供了必要的详细支持。以下是我们在针对通用和特定开发信息喜爱的精选。

O'Reilly's Perl 是获取新 Perl 书籍、产品、模块以及即将举行的活动和会议信息的良好去处，http://www.perl.com/。

Perl 社区是一个非常活跃且有激情的群体，他们的官方网站是 http://www.perl.org。你可以在那里找到职位列表、帮助指南、邮件列表，以及名为 Perl Monkers 的本地社区小组的信息。

Perl 社区在教育新人的方面的某些努力值得关注。其中，http://learn.perl.org 拥有质量最好的审核邮件流量用于解答问题。

对于通用的设计信息和资源，这些优秀的网站有：

- Builder.Com。这个来自 CNET 的网站是 Web 开发人员的极佳资源。它提供定期专题和专栏以及各种新闻组，http://www.builder.com/

- Ziff-Davis 的 DevHead。Molly 的最爱，这个网站提供了大量的脚本。http://www.devhead.com/

- WebView。这个来自 CNET 的网站是 Web 开发人员的极佳资源。它提供定期专题和专栏以及各种新闻组，http://www.builder.com/

- Developer.Com。http://www.builder.com/

## Perl 网站工作

### 新闻组

Perl 新闻组随处可见。以下是：

- `Comp.lang.perl.announce`——Perl 作者使用该组发布新可用模块。

- `Comp.lang.perl.misc`——这是“comp”层级中最活跃的新闻组，提供提问任何 Perl 问题的机会。主题通常是中高级别的。

- `Comp.lang.perl.modules`——如果你专门在寻找 Perl 解决方案，可以使用这个新闻组。

- `Comp.infosystems.authoring.cgi`——如果你有关于 CGI 的问题，这里是提问的地方。

Web 讨论组随处可见。其中一个是 PerlMonks (http://perlmonks.org)，它专门通过用户互动来教授 Perl。该上有大量关于 CGI 编程的代码和讨论。

在参与任何新闻组时遵守礼仪。如果你对礼仪有疑问，请查看 http://unix1.sncc.lsu.edu/internet/usenet/usenet-etiquette.html

### 有用的 FAQ

参考以下 FAQ。

对于全面的 Perl FAQ 列表，请访问 http://www.perl.com/CPAN/doc/manual/html/pod/perlfaq.html。每个 Perl 安装版本都带有 FAQ。要获取 FAQ，在命令行提示符输入`perldoc perlfaq`。

## 我们只想玩

编写程序有点像做字谜游戏。如果你熟悉它所使用的语言，并且有一些线索可以参考，那么把它做出来是非常有趣的、具有挑战性的，而且非常有成就感。

相反，如果你不熟悉这种语言，而且线索完全没有意义，它只是一场挫败和徒劳的尝试。任何尝试过英式字谜的美国人都可以告诉你那种感觉。

学习一种新编程语言以及学习编程的关键，是尽可能坚持那些有趣且具有挑战性的难题。你会发现，随着时间的推移，最初看起来很挫败且难以解决的难题会变得清晰许多。

# 索引

## CGI (通用网关接口)

### 符号

- `@` (@符号), 变量指示符, 38

- `#` (#符号), 注释指示符, 38

- `$` ($符号), 变量指示符, 38

- `%` (百分号), 变量指示符, 38

- `()` (括号), 代码组指示符, 38

- `;` (分号), 行结束符, 38

- `-d` 命令行参数 (调试器), 264-265

- `-w` 命令行参数 (调试器), 264-265

- `/home/htdocs/lib/perl` 目录 (模块库), 30

- `/usr/local/bin` 目录 (命令脚本), 30

### CGI (通用网关接口)

- CGI (通用网关接口), 8-10

- CGI City 网站, 9

- CGI-bin 目录, 29-30

- CGResources.com 网站, 9

- 通用网关接口概述网站, 9

- 多语言支持, 10

- 浏览器与服务器之间的关系, 8-10

- 状态概念, 129-142

- `CGI::Carp` 模块 (错误检查器), 86-89, 264-265

- CGI-bin 目录, 创建, 29-30

- `CGI.pm` 模块, cookie 管理, 100-101

- `CGI::FastTemplate` 模块, 安装, 149-153

- `CGI::Validator` 模块, 89-92

- CGI City 网站, 9

- CGIR 网站, 9

- `chmod` 命令, 文件权限, 修改, 31-32

- `chown` 命令, 文件权限, 修改, 32

- 客户端软件 (FTP) Fetch, 20

- WS_FTP, 19-20

- 客户端软件 (Telnet) NCSA Telnet, 22

- WinTel, 21-22

- 客户端编程, 6-8

- `clock.cgi` 脚本, 数字时钟脚本, 114-116

- 代码组, `{ }` (括号), 38

- 命令行脚本目录, 创建, 30

- 命令: `chmod`, 31-32; `chown`, 32

- `perldoc`, 263

- 注释, `#` (#符号), 38

- 通用网关接口。 见 CGI

- `comp.infosysystems.www.authoring.cgi-ews` 新闻组, 268

- `comp.lang.perl.announce` 新闻组, 268

- `comp.lang.perl.misc` 新闻组, 268

- `comp.lang.perl.moderated` 新闻组, 268

- `comp.lang.perl.newsgroup` 新闻组, 268

- Comprehensive Perl Archive Network。 见 CPAN

- 配置系统目录, 145-146

- 网站模板, 147-149

- 网站文本文件, 147-129

- cookie, 11

- `CGI.pm` 模块, 100-101

- 留言板应用, 添加, 101-107

- 误解, 100-101

- `counter.cgi` 脚本, 页面头部计数显示, 117-121

- `CGI::Carp` 模块, 错误检查功能, 86-89

- 检查库, 33-34

- `CPAN.pm` 模块, 下载, 34-35

- 服务器, 定位, 33-34

## 开发工具

### 创建

- 文件目录, 29-30

- cgi-bin, 29-30

- 命令行脚本, 30

- 模块库, 30

- 表单

- 网页 (`first_oo.cgi`), 39-45

- 网页 (`second_oo.cgi`), 46-51

- 留言板应用 (`guestbook.cgi`), 52-60

- 挂钩猜字游戏 (`hangman.cgi` 脚本), 129-142

- 邮件应用 (`mail_form.cgi`), 60-70

- cron 任务, 226

- `Db connect()` 方法, Story 类 (MySQL), 192

- `DBI.pm` 模块, 数据库访问, 184, 下载, 185

- 多部分索引, 201-207

- story 集合, 190-201

- `-d` 命令行参数, 264-265

- `-w` 命令行参数, 264-265

- `CGI::Carp` 模块, 网页 (`buggy_oo.cgi` 脚本), 86-89

### 设计网站

- Builder, 16

- IBM DeveloperWorks, 16

- W3C, 16

- Web Review, 16

- WebDeveloper, 16

- Ziff-Davis, 16

### 数据库

- 安装 (MySQL), 185

- 权限, 设置 (`story_permissions.sql` 脚本), 189-190

- 表, 设置 (`story_tables.sql` 脚本), 186-189

- `get_all_stats.pl` 脚本, 77-78

- `Time.pm` 模块, 74-142

- 最后修改 (`last_mod.cgi` 脚本), 109

- 客户端 (`detect.cgi` 脚本), 94-100

- `detect.cgi` 脚本, 94-100

- 客户端与服务端, 8

- MacOS 平台, 18

- Unix 平台, 18

- Windows 平台, 17

## DevHead.com 网站

- DevHead.com 网站, 27

- 数字时钟 (`cgi` 脚本), 114-116

- 页面头部计数 (`counter.cgi` 脚本), 117-121

- 页面计数 (`quick.cgi` 脚本), 121-129

- 定位, 27

- 挂钩猜字游戏 (`hangman.cgi` 脚本), 129-142

- 文档 (`perldoc`), 263

- 美元符号 (`$`), 变量指示符, 38

## E - F

- 发送邮件 (`mail_form.cgi`), 60-70

- 错误检查功能 (`CGI::Carp` 模块), 86-89

- 错误检查 (`CGI::Carp` 模块), 86-89

- 错误页面 (`buggy_oo.cgi` 脚本), 86-89

- 行结束符 (分号), 38

- 表达式, 260

- 数组, 260

- `@` (@符号), 变量指示符, 38

- 自动化网站更改 (FastTemplate), 149-153

- 反引号 (Unix), 109

## FTP (文件传输协议)

- 客户端软件

- Fetch (Macintosh), 20

- WS_FTP (Windows), 19-20

- 网站资源, 17

- FTP 常见问题解答, 26

- 留言板应用, 101-107

- 留言板应用 (`guestbook.cgi`), 52-60

- 挂钩猜字游戏 (`hangman.cgi` 脚本), 129-142

- 帮助

- 编程 Perl, 266

- Sams Teach Yourself Perl in 24 Hours, 266

- Unix in a Nutshell, 266

- 括号 (`{}`), 代码组指示符, 38

- 哈希表, 261

## B - C

- ASCII 文本编辑器

- Allaire HomeSite, 18

- BBEdit, 18

- pico, 18-19

- SimpleText, 18

- vi, 18-19

- Windows Notepad, 17-18

- BBEdit ASCII 文本编辑器, 18

## HTML (超文本标记语言)

- 表单

- 邮件 (`mail_form.cgi`), 60-70

- 网页

- 网页 (`first_oo.cgi`), 39-45

- 网页 (`second_oo.cgi`), 46-51

- 故事（网站发布）， 153-158

- `Taintcheck.pm`, 72-74

- `Timefuncs.pm`, 74-76

- `Msql-MysqlDBD` 模块, 下载, 185

- `comp.lang.perl.modules`, 268

- 礼仪, 268

- 开源软件, 6

- `my.cgi` 脚本，门户用户个性化, 208-215

## MySQL

- 数据库权限, 配置 (`story_permissions.sql` 脚本), 189-190

- 数据库表, 配置 (`story_tables.sql` 脚本), 186-189

- 安装, 185

- 百分号 (`%`)，变量指示符, 38

## Perl

- 文件类型

    - `.cgi`, 28

    - `.htm`, 28

    - `.pl`, 28

    - `.pm`, 28

### Story 类

- `add_story()` 方法, 194-196

- `db_connect()` 方法, 192

- `read_story()` 方法, 192-193

- `story_set_to_id()` 函数, 197-201

- 从 CD 安装, 5

- ISP 需求, 23-24

- 学习指南, 261-265

- 平台支持, 6

- 所需技能

    - FTP, 15

    - HTML, 15

    - Telnet, 16

    - Unix, 15

## N - O

- NCSA Telnet (Telnet 客户端软件), 22

- 服务器驻留, 检查, 27

- 支持者, 5

- Netscape Navigator, 下载, 23

- 新闻组版本:

    - 检查, 27

    - 下载, 5

    - 实验性, 5

    - 稳定, 5

    - `comp.infosystems.www.authoring.cgi`, 268

    - `comp.lang.perl.announce`, 268

    - `comp.lang.perl.misc`, 268

    - `comp.lang.perl.moderated`, 268

- Wall, Larry, 5

## Perl FAQ 网站

- Perl FAQ 网站, 268

- Perl.com 网站, 267

- Perl.org 网站, 267

- `perldoc` 命令, 文档帮助, 263

- 权限: 数据库, 设置 (`story_permissions.sql` 脚本), 189-190

- 文件:

    - `chmod` 命令, 31-32

    - `chown` 命令, 32

    - 设置, 30-32

    - SUID 脚本, 32-33

- pico 编辑器 (Unix), 18-19

- 平台, Perl 支持, 6

- 门户:

    - 创建, 184-221

    - 示例, 184

    - `Publisher::Index::Multi` 模块, 201-207

- 故事:

    - 数据库添加 (`story_set.pl` 脚本), 217-219

    - 数据库 ID 数字 (`publish_dbi.pl` 脚本), 219-221

    - 数据库组织 (`story_txt2dbi.pl` 脚本), 216-217

- `Story::Dbi.pm` 模块, 190-201

- 用户个性化 (`my.cgi` 脚本), 208-215

- 井号 (`#`), 注释指示符, 38

- `print_env.cgi` 脚本 (SSI 示例), 109-110

- 编程 Perl, 266

- 程序, 开发指南, 261-265

- 客户端与服务端, 8

- `publish.pl` 工具 (网站发布), 168-181

- Publisher 模块 (网站发布), 158-163

- `Publisher::Index` 模块 (网站发布), 163-167, 201-207

- 网页, 12

- `Publish.pl` 工具, 168-171

- Publisher 模块, 158-163

- `Publisher::Index` 模块, 163-167, 201-207

- Story 模块, 153-158

- `publish_dbi.pl` 脚本, 故事数据库管理, 219-221

- `pub_dir.pl` 脚本, 管理站点更新, 180-183

- `public_set.pl` 脚本, Simple SUID 脚本, 225-259

## Q - R

- `quickpolls.cgi` 脚本, 页面用户投票显示, 121-129

- 引言, 网页上的随机化 (`fortune.cgi` 脚本), 108-109

- 网页图像随机化 (`random_img.cgi` 脚本), 110-111

- `random_img.cgi` 脚本 (SSI 示例), 110-111

## 通过电子邮件发送网页 (`Story::Mail.pm` 模块)

- `read_story()` 方法, Story 类 (MySQL), 192-193

- `roll_pages.pl` 脚本, 78-81

- 根目录, 层级结构, 配置, 145-146

- 检测后的浏览器重定向, 98-100

- `my.cgi` (门户个性化), 208-215

- 页面自动化 (`roll_pages.pl` 脚本), 78-81

- `print_env.cgi`, 109-110

- `publish_dbi.pl`, 219-222

- `publish_dir.pl`, 180-183

- `quickpoll.cgi`, 121-129

- `random_img.cgi`, 110-111

- `second_oo.cgi`, 46-51

- `ssi_test.shtml`, 112-113

- `story_permissions.sq`, 189-190

- `story_table.cgi`, 186-189

- `story_xtdbi.pl`, 216-217

- 保存状态 (CGI), 129-142

- `add_story_set.pl`, 217-219

- 浏览器检测 (`browser_detect.cgi`), 94-100

- 检查器 (`buggy_oo.cgi`), 86-89

- `clock.cgi`, 114-116

- `counter.cgi`, 117-121

- `echo_date.cgi`, 108-119

- `epublish.pl`, 177-180

- `first_oo.cgi`, 39-45

- 表单验证器 (`signup.cgi`), 89-92

- `fortune.pl`, 108-109

- `guestbook_2.cgi`, 101-107

- `hangout.cgi`, 129-42

- `last_mod.cgi`, 109

- 检查器 (`link_check.pl`), 81-86

- `mail_form.cgi`, 60-70

- 语法 (注释), 38

- `$` (变量), 38

- `%` (变量), 38

- 分号, 38

- `@` (变量), 38

- `[]` (括号), 108

- 污染检查 (`Taintcheck.pm` module), 72-174

- `template.pl`, 149-153

- 时间/日期函数 `get_all_stats.pl`, 77-78

- `Timefuncs.pm` 模块, 74-76

- `second_oo.cgi` 脚本, 表单创建, 46-51

- 换行符, 38

- 通过电子邮件发送网页 (`Story::Mail.pm` 模块), 171-177

## 服务端包含

- 服务端编程, 6-8

- 文件权限, 30-32

- `signup.cgi` 脚本, 89-92

- 站点管理工具:

    - 调试器 (`buggy_oo` 脚本), 86-89

    - 时间/日期函数 (`get_all_stats.pl` 脚本), 77-78

    - 时间/日期函数 (`Timefuncs.pm` 模块), 74-76

    - 表单验证器 (`signup.cgi` 脚本), 89-92

    - 检查器 (`link_check.pl` 脚本), 81-86

    - 页面自动化 (`roll_pages.pl` 脚本), 78-81

    - 污染检查 (`Taintcheck.pm` module), 72-74

- siteman (`siteman.cgi` 脚本), 222-224

- SUID 脚本 (`publish_set.pl`), 225-259

- SSIs (服务端包含):

    - 用法, 107-108

    - ISP 限制, 107-108

    - 最后修改日期 (`last_mod.cgi` 脚本), 109

    - 页面调试器 (`print_env.cgi` 脚本), 109-110

    - 随机图像 (`random_img.cgi` 脚本), 110-111

    - 随机引言 (`fortune.cgi` 脚本), 108-109

    - 摘要示例页 (`ssi_test.html`), 112-113

    - 时间/日期页面更新 (`echo_date.cgi` 脚本), 108

    - `ssi_test.html` 脚本 (SSI 示例), 112-113

- 语句 (表达式), 261

- 数据库添加 (`add_story_set.pl` 脚本), 217-219

- 数据库 ID 数字 (`publish_dbi.pl` 脚本), 219-221

- 数据库组织 (`story_xt2dbi.pl` 脚本), 216-217

## Story 类 (MySQL)

- 函数, `story_set_to_id()`, 197-201

- 方法:

    - `add_story()`, 194-196

    - `db_connect()`, 192

    - `read_story()`, 192-201

- `Story::DBI.pm` 模块, 190-201

- `Story::Text.pl` 模块, 153-158

- `Story::Text::Mail` 模块, 171-177

- `story_permissions.sql` 脚本, 189-190

- `story_tables.sql` 脚本, 186-189

- `story_xt2dbi.pl` 脚本, 为门户组织故事数据库, 216-261

## SUID (用户 ID) 脚本

- 文件权限, 32-33

- `publish_set.pl` (siteman), 225-259

- 使用指南, 262-263

- 系统目录, 配置, 145-146

- 反引号, 108

- 命令行, 38

- 输出, 77-78

## T - V

- 污染检查 (`Taintcheck.pm` module), 72-74

- 时间/日期函数 `get_all_stats.pl` 脚本, 77-78

- `Timefuncs.pm` 模块, 74-76

- `template.pl`, 149-153

- 教程, 36

- 变量:

    - `$` (变量), 38

    - `%` (变量), 38

    - `@` (变量), 38

- vi 编辑器 (Unix), 18-119, 18, 1, 9

## W - Z

- W3C (World Wide Web)

- Wall, Larry, 5

- 网页, 12

- 自动更新 (`roll_pages.pl` 脚本), 78-81

- 检查器 (`buggy_oo.cgi` 脚本), 86-89

- 时间/日期函数 (`get_all_stats.pl` 脚本), 77-78

- 时间/日期函数 (`Timefuncs.pm` 模块), 74-76

- 时间/日期页面更新 (`echo_date.cgi` 脚本), 108

- 浏览器检测 (`browser_detect.cgi`), 94-100

- 数字时钟, 114-116

- 指南, 261-265

- 数字时钟, 114-116

- `echo_date.cgi`, 108-119

- 换行符, 38

- `epublish.pl`, 177-180

- 表达式, 261

- 示例, 184

- `first_oo.cgi`, 39-45

- 表单验证器 (`signup.cgi`), 89-92

- 表单创建, 46-51

- `fortune.pl`, 108-109

- `fortune.cgi` 脚本, 108-109

- `guestbook_2.cgi`, 101-107

- `guestbook.cgi`, 46-51

- 挂字游戏, (`hangman.cgi` 脚本), 129-132

- 计数器, (`counter.cgi` 脚本), 117-121

- Internet Explorer, 23

- ISP 需求, 23-24

- ISP 限制, 107-108

- 最后修改日期 (`last_mod.cgi` 脚本), 109

- 检查器 (`link_check.pl` 脚本), 81-86

- `mail_form.cgi`, 60-70

- `my.cgi` (门户个性化), 208-215

- `my.cgi` 脚本，门户用户个性化, 208-215

# Windows

# 283

- 时间/日期更新 (`echo_date.cgi` 脚本), 108

- 页面自动化, 78-81

- 用户投票，创建 (`quickpoll.cgi` 脚本), 121-129

- 污点检查, 72-74

- 更新管理 (`publish_dir.pl` 脚本), 180-183

# Web Review.com 网站, 16, 267

- Perl.com, 5, 267

- Perl.org, 267

- PerlFAQ, 268

# Web 服务器

- + CGI 函数, 8-10

- CPAN，定位, 33-34

- Perl 驻留，检查, 27

- 服务端编程, 6-8

- 门户网站

- 创建, 184-221

- 示例, 184

- `Publisher::Index::Multi.pm` 模块, 201-207

# Web 网站发布向导

(`siteman.cgi` 脚本), 222

- `Story::DBI.pm` 模块, 190-201

- 用户个性化 (`my.cgi` 脚本), 208-215

- + 必需模块, 223-224

- SUID 脚本, 225-259

- 发布, 12

# Web 网站

- + 自动化, 149-153

- Builder.com, 16, 267

- CGIResources, 9

- 通用网关接口概览 (Common Gateway Interface Overview), 9

- 设计资源, 16

- Developer.com, 267

- DevHead.com, 267

- FTP FAQ, 17

- HTML 模板，设置, 147-149

- + Telnet FAQ, 17

- 文本文件，设置, 147-149

- Unix FAQ, 17

- Unix 参考台 (Unix Reference Desk), 36

- 针对用户的 UN 帮助 (UNHelp for Users), 17

- 通过电子邮件更新 (`epublish.pl` 脚本), 177-180

- W3C (世界维网联盟), 16

- Web Review.com, 16, 267

- WebDeveloper.com, 16

- Ziff-Davis, 16

- + IBM DeveloperWorks, 16

- 管理工具, 12

- Bug 检查器, 86-89

- 日期/时间函数, 74-78

- 表单验证器, 89-92

- 链接检查器, 81-86

# WebDeveloper.com 网站, 16

# Windows

- + FTP 客户端软件 (WS_FTP), 19-20

- Telnet 客户端软件 (WinTel), 21-22

# Windows 记事本 (ASCII 文本编辑器)

- Windows 记事本 (ASCII 文本编辑器), 17-18

- WinTel (Telnet 客户端软件), 21-22

- WS_FTP (FTP 客户端软件), 19-20

- Ziff-Davis 网站, 16
