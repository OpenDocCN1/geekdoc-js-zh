# JavaScript 全能指南





# 本书献给：

我的妻子，Liez’l。言语无法充分表达你对我生命的重要性。

我的母亲，她教会了我坚强与毅力的真谛。愿上帝保佑。

我的父亲，此刻他一定在告诉身边的天使，“那是我的儿子。”我想你，爸爸。

# 关于作者

Scott Duffy为中型和大型企业以及政府组织提供IT咨询服务已有六年以上。在从事顾问职业之前，Scott曾在加拿大两家最大的公司担任软件开发人员。

他拥有12年的专业经验，涵盖广泛的平台和技术，包括在大型机、客户端服务器和基于Web的应用程序环境中进行编程。他积极参与软件开发过程的每个阶段，包括团队管理。

当他不为客户设计软件应用程序时，Scott忙于他的写作项目。他目前正为McGraw-Hill/Osborne撰写他的下一本书，这是一本针对Microsoft MCSD 70-300考试的学习指南。

如需联系Scott讨论您组织的业务需求，或任何其他事宜，请发送电子邮件至scott.duffy@mydemos.com或访问他的网站http://www.mydemos.com。

## 致谢

> 如今，编程就像一场竞赛，一边是软件工程师努力构建更大更好、傻瓜也能用的程序，另一边是宇宙试图制造更大更好的傻瓜。到目前为止，宇宙赢了。

—Rich Cook

我非常感谢每一位参与出版此书的人。我当然不想去想象如果只有我一个人，会创造出什么来。我对这本书的最终成果非常满意，我为此欠了许多人巨大的感激之情：

Megg Morin，我在 Osborne 的策划编辑。感谢你在发展概念方面的所有帮助，以及在开始时给予这本书它所需的、向正确方向的有力推动。

Leslie Tilley，我的文字编辑和项目编辑。谢谢你，谢谢你，谢谢你。我真心感谢你的辛勤工作和对细节的关注。这本书之所以如此成功，你是最主要的原因。

Tana Allen，我的策划协调员。感谢你让项目保持正轨。

Madhu Prasher。感谢你如此出色地完成你的工作。遇到热爱自己工作的人总是件好事。

Warren Raquel，我的技术编辑。感谢你的辛勤付出。

Jawahara Saidullah，我在 Waterside Productions 的代理人。感谢你为我争取到这次机会，并希望未来还有更多。

最后但同样重要的是，我的妻子 Liezl。有你在我身边，我能攀登高山，也能屠戮巨龙。

## 简介

Netscape 在 1995 年 12 月隆重推出了 JavaScript，将其定位为一种“开放的、跨平台的面向对象脚本语言”。它被宣传为备受期待的 Java 编程语言的完美补充，因为这两种语言可以在浏览器窗口内相互通信。

如今，近十年过去，JavaScript 已在互联网领域无处不在。据估计，目前互联网上 25% 的网页包含 JavaScript 代码。其中一些代码用于执行一些非常基本的脚本效果，例如控制鼠标悬停和设置浏览器状态栏。许多网页包含复杂的动态菜单和自动化表单。没有其他脚本语言能接近 JavaScript 在浏览器环境中的主导地位。

JavaScript 成功的关键在于其易于使用。例如，单个 JavaScript 语句就可以创建一个有趣的浏览器效果，而只需要一小撮语句就能创建一个完全交互式的浏览器环境。

你甚至不需要任何特殊工具来创建这些效果。一个简单的文本编辑器，如 Windows 记事本，就足够了。如果你能创建 HTML 网页，你就拥有了入门所需的所有工具。

随着即将发布的 2.0 版本，JavaScript 终于可以与 C++ 和 Visual Basic 等编程语言并肩使用。例如，微软在其流行的 .NET 编程环境中包含了一个名为 JScript .NET 的 JavaScript 2.0 版本。JScript .NET 可以访问几乎所有的 .NET Framework 类，并可用于创建在桌面上运行的 Windows 窗体应用程序。事实上，你下一个使用的文字处理器可能完全是用 JavaScript 编写的。

## 谁应该阅读这本书

本书旨在帮助任何有兴趣为其个人网页添加交互元素的人。需要具备一些 PC 使用经验，因为我们将不会介绍如何访问互联网或如何使用网络浏览器。你不必是 HTML 专家，但如果你有一些使用该语言的经验，会有所帮助。当首次遇到新的 HTML 时，我会简要解释发生了什么，但总是在 JavaScript 的上下文中。

## 本书的组织结构

《如何用 JavaScript 做所有事》分为三个主要部分。每个部分侧重于一组不同的 JavaScript 技能：

- **第一部分** 第 1–5 章带你了解 JavaScript 的基础知识。本部分涵盖编程语言的基本方面，包括语句、对象和数据类型。
- **第二部分** 第 6–12 章向你展示如何将 JavaScript 集成到网站中。本部分探讨将 JavaScript 与文档对象模型、浏览器事件、框架和网页表单结合使用。
- **第三部分** 第 13–15 章涵盖高级 JavaScript 主题。本部分涉及调试 JavaScript 程序、使代码万无一失以及与嵌入在网页中的其他对象通信。

通常，学习像 JavaScript 这样的编程语言的最佳方式就是亲手摆弄它。不要害怕尝试书中的一些 JavaScript 示例。把它们输入进去，然后修改成你自己设计的东西——你会对事物如何运作有更深入的理解。问问自己：“如果我这样做会发生什么？”然后继续尝试——不会有什么严重的问题。最糟糕的情况就是你尝试的东西不工作。那也没关系。耸耸肩，再试一次。

## 第一部分 学习 JavaScript 基础知识

![](img/f14dd58a324d5464a114c30c1d4c4c9b_20_0.png)

### 第 1 章 准备用 JavaScript 编程

![](img/f14dd54a324d5464a114c30c1d4c4c9b_22_0.png)

#### 如何...

- 选择一个开发环境
- 了解 JavaScript 能做什么和不能做什么
- 决定使用哪个版本的 JavaScript
- 使用 HTML 测试 JavaScript 程序
- 使用 HTML `<script>` 标签
- 使用 Microsoft Notepad 创建一个 JavaScript 模板
- 与用户沟通

在每部成功的电影背后，都有一个幕后人物，他管理着演员、摄像师、编剧和其他剧组成员的互动。这就是导演，虽然你通常不会在屏幕上看到这个人，但电影的质量取决于他或她的努力是否成功。

嗯，JavaScript 就是许多互联网网站的幕后“导演”。它的职责是管理对象和事件的互动，使两者无缝地相互交互。通常，网站越复杂，它就越依赖于 JavaScript 来指导。灯光！摄像！浏览器！开拍！

也许需要问的第一个问题是，它是什么？最简单的答案是 JavaScript 是一种简单的编程语言，主要用于为网站带来交互性。它通常被称为*脚本*语言，因此得名，但它也有非脚本的形式。

在编程术语中，*脚本*是指不需要编译就能运行的程序。脚本倾向于执行特定任务然后退出，通常没有图形用户界面（GUI）。JavaScript、Perl 和 VBScript 是互联网网站最常用的脚本语言。

##### 了解 JavaScript 的历史

JavaScript 诞生于将 HTML（超文本标记语言）网页与嵌入内容（如 Java applet）协调起来的需求。但 JavaScript 的用途远不止于此。它通常用于帮助用户填写在线表单、通过动态菜单提供网站导航以及驱动电子商务购物车。事实上，据说今天有 25% 的网站以某种方式使用 JavaScript。

> *虽然目前使用的大多数（99.5% 或更多）网络浏览器软件都内置了对 JavaScript 的支持，但用户可以选择关闭该支持。在为互联网上的所有人设计网站时，重要的是要记住有些人不会“看到” JavaScript。*

考虑到其他网络相关技术为了整合新功能而变化如此之快，JavaScript 一直相当稳定。JavaScript 花了八年时间才发展到



从最初发布的 1.0 版本到下一个主要版本 2.0。有些人认为这种缓慢的节奏对这门语言来说既是**福也是祸**。

好处是，JavaScript 在多个浏览器厂商和版本之间的支持相当一致。Web 开发人员可以实现一个 JavaScript 程序，而不必过于担心兼容性问题（除了避免某些不兼容的编码技术）。JavaScript 之所以得到如此广泛的采用，主要是因为开发人员可以信赖它的工作能力。

弊端是，当 JavaScript 停滞不前时，其他语言已经涌现出来填补技术空白。网站使用 Visual Basic Script (VBScript) 或 Java Server Pages (JSP) 作为服务器端 Web 脚本语言的情况远比使用 JavaScript 更为常见。事实上，最近发布的一款流行 Web 服务器软件（iPlanet Web Server）已经完全取消了对 JavaScript 的支持。然而，随着 JavaScript 2.0 引起开发人员的关注，这种情况可能会改变。

###### JavaScript 的起源

JavaScript 于 1995 年首次出现在 Netscape 2.0 中。JavaScript 最初的设计目的是帮助将 HTML 页面与 *Java 小程序*（嵌入在 Web 页面中的 Java 应用程序）集成在一起。不过，开发人员很快意识到它的真正潜力，不久之后 JavaScript 就被用来为网站增加交互性——大多数时候无需 Java 的帮助。

图 1-1 展示了 Navigator 2.0，第一款支持 JavaScript 的 Web 浏览器。

###### JavaScript 进入 Internet Explorer

在 Netscape 公司首次在其 Navigator 2.0 浏览器中引入 JavaScript 后不久，微软就意识到了将这种语言整合到其 Internet Explorer 浏览器中的重要性。由于 Netscape 不太可能将源代码邮寄给微软，甚至该语言的规范都是一个严格保守的秘密，微软被迫对 JavaScript 进行逆向工程以创建自己的版本。微软将其版本命名为 JScript，因为 Netscape 拥有 *JavaScript* 这个词的商标权。

早期版本的 JScript 在执行某些功能时与 JavaScript 并不完全相同，因此浏览器之间的 JavaScript 不兼容性是开发人员在编写 Web 页面脚本时经常需要考虑的问题。

###### JavaScript 成为官方标准

在 Web 发展早期，跨浏览器兼容性是一个大问题——比今天要大得多。两家主要的浏览器公司在 HTML 和 JavaScript 语言上进行改动，试图获得竞争优势，这给试图创建支持两种浏览器的网站的 Web 开发人员带来了巨大的麻烦。幸运的是，两家公司最终都妥协了。

Netscape 于 1996 年明智地将 JavaScript 的标准化工作移交给了**欧洲计算机制造商协会（ECMA）**。ECMA 专注于核心语言的标准化，但将其他事项（如 JavaScript **文档对象模型**，即 DOM）留给了浏览器制造商。结果是浏览器之间的不兼容性仍然存在。

#### 如何用 JavaScript 做一切事情

![图 1-1](img/f14dd58a324d5464a114c30c1d4c4c9b_25_0.png)

**图 1-1** 1995 年的 Web 在 Navigator 2.0 中呈现的样子

ECMA 于 1997 年发布了其标准化脚本语言，即 ECMAScript。在接下来的两年中，他们对标准进行了两次更新，分别称为第 2 版和第 3 版。JavaScript 1.5 符合该标准的第 3 版。

##### JavaScript 的今天

ECMAScript 第 4 版标准将是四年多来的首次更新。JavaScript 2.0 符合 ECMAScript 标准的第 4 版，两者之间的差异极小。

> **注意**
> JavaScript 2.0 的规范可以在 Mozilla.org 网站上找到：http://www.mozilla.org/js/language/js20/index.html。

如今，Netscape 的 JavaScript 和微软的 JScript 都符合 ECMAScript 标准，尽管每种语言仍然支持不属于标准的功能。

# 第 1 章：准备用 JavaScript 编程 7

**表 1-1** JavaScript 版本年表

| JavaScript 版本 | 发布日期 | 浏览器 | 标准合规性 |
| :--- | :--- | :--- | :--- |
| 1.0 | 1995 年 12 月 | Navigator 2, Internet Explorer 3 | 否 |
| 1.1 | 1996 年 4 月 | Navigator 3 | 部分符合 ECMAScript 1 |
| 1.2 | 1996 年 12 月 | Navigator 4, Internet Explorer 4 | 部分符合 ECMAScript 1 |
| 1.3 | 1998 年 8 月 | Navigator 4.06, Internet Explorer 5 | ECMAScript 1, ISO-16262 |
| 1.4 | 1998 年 10 月 | 1.4 版本未出现在任何 Web 浏览器中 | ECMAScript 1, ISO-16262 |
| 1.5 | 2000 年 4 月 | Navigator 6 和 7, Internet Explorer 5.5 和 6, Mozilla 1 | ECMAScript 3 |
| 2.0 | 2003 年 | | ECMAScript 4 |

表 1-1 包含了 JavaScript 版本的 chronological 列表，包括支持每个版本的流行浏览器的简短列表。

> 在撰写本文时，JavaScript 2.0 的确切发布日期以及将支持它的浏览器版本号尚未确定。

#### 选择开发环境

JavaScript 最大的优势之一是它支持许多不同的平台，通常用于不同的目的。当今最常见的 JavaScript 应用程序类型是在 Web 浏览器内部运行的客户端脚本。JavaScript 长期以来也被支持作为 Web 服务器端语言，在 IIS 和 Live1.  **开发环境**等流行环境中。近年来，开发人员在不同的环境中使用 JavaScript 有了更多选择。

在本节中，我们将了解 JavaScript 在这些环境中的应用。目前还没有任何一种环境支持 JavaScript 2.0，但了解潜在的支持环境仍然很重要，因为支持可能很快就会被引入。

同样在本节中，我们将讨论 JavaScript 开发人员的开发环境。在 JavaScript 存在的最初几年里，开发人员只能使用文本编辑器来创建他们的 JavaScript 程序，没有集成开发环境（IDE）的辅助——许多人现在仍然如此。但随着 HTML 开发工具的发展，许多工具增加了对世界上最流行的脚本语言的开发支持。如今，所有大型工具都提供了这种支持，我们将在本节后面看到。

##### 开发支持 JavaScript 的 Web 页面

设计为在浏览器内部运行的应用程序是迄今为止 JavaScript 最流行的用途。通过 DOM，JavaScript 被非常紧密地集成到 Web 浏览器环境中。Netscape 在 JavaScript 1.0 中引入了原始的 DOM。

###### 客户端-服务器类比

在 Web 开发术语中，Web 浏览器及其运行的计算机通常称为 *客户端*。同样，Web 服务器软件及其运行的计算机称为 *服务器*。因此，术语 *客户端 JavaScript* 指的是嵌入在 Web 页面中并在客户端机器上运行的 JavaScript 程序。在服务器机器上运行的 JavaScript 称为 *服务器端 JavaScript*。

不久之后，DOM 的控制权被移交给了万维网联盟（W3C），一个标准组织。DOM 标准已经从处理 JavaScript 如何与浏览器交互，发展到处理创建、读取和修改 HTML 和 XML 文档的标准方式。

> W3C（http://www.w3.org）专门从事 Web 标准，包括 HTML、XML、DOM 和层叠样式表（CSS）。与 DOM 标准相关的各种文档可以在 http://www.w3.org/DOM/DOMTR 查看。需要注意的是，原始 DOM（有时称为 Level 0）不是官方标准。

设计为在浏览器内部运行的 JavaScript 应用程序受到许多安全限制。这些应用程序通常无法访问用户的硬盘或用户计算机上已安装的任何应用程序。对用户来说，这意味着 JavaScript 应用程序通常不会构成安全风险，因为它不能包含病毒或其他恶意代码。

Netscape Navigator 4.0（也称为 Communicator）引入了签名脚本的概念。使用安全数字密钥签名的脚本可以在浏览器环境中请求额外的权限，例如发送电子邮件或从硬盘读取文件的功能。通常浏览器会提示用户，询问他们是否允许脚本拥有此类权限。

Mozilla Web 浏览器及其近亲 Navigator 6 改变了签名脚本的处理方式，不再与 Navigator 4 兼容。微软 Internet Explorer（IE）处理安全的方式完全不同（例如使用受信任区域）。由于这些异构的安全解决方案，目前仍然没有标准的方式来编写具有扩展权限的 JavaScript 应用程序。实际上，签名 JavaScript 很少被使用。

客户端应用程序开发仍然是 JavaScript 的核心优势之一。开发人员如果选择 JavaScript 以外的任何语言进行客户端开发，实际上都会面临与许多操作系统和 Web 浏览器不兼容的风险！

####### 创建基于服务器的 Web 应用程序

尽管 JavaScript 在 Web 客户端编程方面占据主导地位，但在服务器端编程方面情况并非如此。JavaScript 是最早的服务器端



#### 在 DOS 或 Windows 环境中使用 JavaScript

长期以来，微软一直将 Windows 脚本宿主（WSH）工具作为 Windows 的免费附加组件，用户可从其网站下载。WSH 包含了微软两种脚本语言的最新版本——VBScript 和 JScript。

通过 WSH，你可以用 JScript 编写一个小程序，并在 DOS 命令提示符下运行。事实上，许多病毒编写者利用了这一特性（尤其是 VBScript），因此如今这些宏和小型脚本已较少使用。实际上，许多邮件系统在发送电子邮件附件时完全禁止使用它们，因为存在病毒传播的风险。

> Windows Script（包括 JScript 和 VBScript 引擎）可以从 http://msdn.microsoft.com/scripting 免费下载。

开发者仍然可以使用 JScript 创建用于 Windows 环境的小程序，尽管这种情况已经很少见。这些 JScript 程序依赖于 Windows 脚本环境的存在和启用，而在当今注重安全的时代，这一点不能过度依赖。

#### JavaScript 开发工具

JavaScript 的优势之一是通常不需要昂贵的开发工具。借助 Windows 内置的简单文本编辑器（如记事本），你就能轻松创建相对复杂的 JavaScript 代码。由于它是在 Web 浏览器中运行的解释型语言，你甚至不需要购买编译器。

> 编译器是一种将编程代码转换为机器可执行形式的程序，通常称为二进制文件或可执行文件。

但仅仅因为 JavaScript 可以在简单的文本编辑器中编辑，并不意味着它*应该*这样做。开发环境提供了多种关键资源，通常能让开发更快、更轻松，例如：

- 可轻松添加到网页的预定义脚本
- 集成帮助系统，可快速查找函数语法
- 自动 FTP 上传到 Web 服务器
- 集成调试工具

在本节中，我们将介绍排名前四的 HTML 编辑器。每个编辑器都对 JavaScript 开发提供了强大的支持，包括即用型脚本、JavaScript 编辑工具和嵌入式帮助文档。

##### Microsoft FrontPage

微软开发了一款流行的 HTML 编辑器，名为 FrontPage。FrontPage 为 Web 开发者提供了多种 JavaScript 工具，以辅助创建交互式网站。FrontPage 曾经是 HTML 和 JavaScript 开发工具中无可争议的领导者。如今，该领域的一些竞争对手已夺取了微软相当大的市场份额——Macromedia 和 NetObjects。

FrontPage 仍然包含许多实用功能，例如在创建任何页面之前设计网站层级结构、配置网站安全性、设置全站样式以及创建自定义横幅图片。图 1-2 展示了如何使用 FrontPage Explorer 通过图形化方式将页面链接在一起来组织网站。Microsoft FrontPage 还有一个名为 FrontPage Server Extensions 的服务器端组件，使其能够很好地集成到微软的 IIS Web 服务器中。

FrontPage 的售价为 90 至 170 美元，对于非专业网站开发者来说是一款非常经济实惠的工具。

> 微软为有兴趣试用该软件的用户提供 FrontPage 2002 的免费 30 天试用版。可通过 http://www.microsoft.com/frontpage 订购试用版光盘。

##### Macromedia Dreamweaver MX

Macromedia Dreamweaver MX 在专业 Web 开发领域是一款非常流行的 HTML 和 JavaScript 编辑器。它功能丰富，包括编辑大多数流行 Web 服务器编程语言（如 ASP、JSP 和 PHP）的能力，提供多种便捷的预构建 JavaScript 组件，与数据库集成良好，并符合 XHTML 和 XML 等新标准。简而言之，它包含了许多专业人士认为实用但许多家庭用户可能并不需要的功能。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_30_0.png)

**图 1-2** 使用 FrontPage Explorer 组织网站

Dreamweaver MX 环境的强大功能如图 1-3 所示。Macromedia Dreamweaver MX 的零售价为 200 至 400 美元，是专业开发者的理想工具。

> 你可以在 http://www.macromedia.com/software/dreamweaver 下载适用于 Windows 或 Mac 的 Macromedia Dreamweaver MX 免费试用版。

##### Macromedia HomeSite 5

Macromedia 收购了 Allaire 公司，并接手了其旗舰产品 HomeSite。最新版本是 HomeSite 5，Macromedia 在每套 Dreamweaver 中都附赠了一份 HomeSite 的免费副本。HomeSite 以其价格吸引了家庭用户，尽管它缺少其姊妹产品的大部分高级功能。

12 全面掌握 JavaScript

![](img/f14dd58a324d5464a114c30c1d4c4c9b_31_0.png)

**图 1-3** Dreamweaver MX 是专业 Web 开发者的卓越工作环境。

用户只需花费 29 至 99 美元即可获得一款广受好评的 HTML 和 JavaScript 编辑器，它能够很好地管理个人网站。需要管理大型网站或有多位开发者的用户可能需要考虑投入更多资金购买 Dreamweaver。

> **注意** Macromedia 在 http://www.macromedia.com/software/homesite 提供适用于 Windows 的 HomeSite 5 免费试用版。

##### Adobe GoLive

Adobe 对大多数互联网浏览者来说最为知名的是其 Acrobat 软件，该软件可编写和阅读其流行的便携式文档格式（PDF）文档。然而，Adobe 在图形、数字视频和桌面出版软件领域同样是领导者，拥有 Photoshop、Premiere 和 PageMaker 等产品。

事实上，该公司生产的其他所有行业领先的工具和软件包可能都掩盖了其 Web 出版工具业务的光芒。然而，尽管 Adobe GoLive 在许多方面可能落后于竞争对手，但对于经常使用 Adobe 图形和视频编辑工具的开发者来说，GoLive 可能是一个便捷的选择。

> 与其他 Web 创作工具一样，你可以下载 GoLive 6.0 的试用版。GoLive 同时提供 Windows 和 Mac 版本，可从 Adobe 网站 http://www.adobe.com/products/golive 下载。

##### NetObjects Fusion

FrontPage、Dreamweaver、GoLive 和 NetObjects Fusion 构成了当今使用最广泛的四大网站开发工具。不幸的是，NetObjects 没有足够的资金或资源来维持与这些强劲竞争对手的竞争。该公司已被出售，新东家 Website Pros 一直在沿用现有品牌名称继续开发 Fusion 工具。

Fusion 的定价具有竞争力，售价在 70 至 150 美元之间。它包含许多有趣的新功能，例如与流行在线支付服务的集成、JavaScript 弹出菜单以及对嵌入式多媒体的改进支持。它曾经是开发者中流行的工具，在新的管理下可能再次流行起来。

> 可从公司网站 http://www.netobjects.com 下载适用于 Windows 的 NetObjects Fusion 7 免费试用版。该软件的完整版本也可在线购买和下载。

#### 了解 JavaScript 的能力与局限

从历史上看，JavaScript 通过以下方式与其他语言区分开来：

- 易于开发。
- 与其他语言和环境接口良好。
- 不需要特殊的工具或编译器。
- 灵活性高。

这些特性使其特别适合 Web 开发。网页仅需一行 JavaScript 代码即可实现动态效果，通常只需少数几行代码就能完成常见任务。DOM 为 JavaScript 提供了对浏览器、网页以及其中嵌入的所有对象（Java、多媒体等）的访问能力。

尽管有了显著的改进，JavaScript 2.0 并非被设计为一种通用语言。具体而言，它并不打算在 C、C++ 或 Java 目前占主导地位的领域与之竞争。相反，JavaScript 2.0 试图在现有语言优势的基础上进行改进，同时添加开发者在开发大型或复杂代码时经常希望使用的功能，即：

- 编写模块化和面向对象应用程序的能力
- 与其他编程语言接口的改进能力



 - 编写可编译以提高性能的脚本的能力
- 限制函数和代码使用方式的能力

ECMA 在设计 JavaScript 2.0 时确实考虑了这些目标。

#### 将 JavaScript 用作客户端语言

核心 JavaScript 规范的一个独特之处在于，它并未尝试定义 JavaScript 如何与其环境交互。该规范中没有定义如何绘制用户界面或如何将文本写入屏幕的 JavaScript 方法或函数。同样，也没有文件输入/输出例程允许该语言访问硬盘驱动器。

这一特性可以被视为既是优点也是缺点。这种缺乏标准 I/O 接口所带来的灵活性，使得 JavaScript 被用于许多不同的环境（浏览器、服务器、独立应用程序、移动设备等）。这使得具有不同数据存储方式和不同输出显示方式的设备都能够运行 JavaScript 应用程序。

这种灵活性的缺点在于，同一个 JavaScript 应用程序无法在每个环境中不经修改地运行。虽然大多数 Web 浏览器已标准化了文档对象模型，但各浏览器厂商的 DOM 之间仍存在一些差异。例如，为在 Web 浏览器中运行而设计的 JavaScript 应用程序无法在 Web 服务器上运行，除非考虑服务器自身的对象模型。

如今，JavaScript 实际上是在网页内部使用的唯一脚本语言。尽管存在几种替代方案（最著名的是 VBScript），但 JavaScript 曾经是（而且现在仍然是）所有主要浏览器厂商支持的唯一脚本语言。它是客户端开发中唯一值得学习的脚本语言。

#### 将 JavaScript 用作服务器端语言

JavaScript 作为 Web 服务器编程语言也获得了一定的流行度。Netscape Enterprise Server 和 Microsoft IIS（20 世纪 90 年代中期流行的 Web 服务器）都支持服务器端 JavaScript 开发。Netscape 通过 LiveWire 服务器端语言支持这一点。Microsoft 允许 JScript 作为 ASP 开发的潜在语言之一。

不幸的是，Netscape Enterprise Server（现称为 iPlanet Web Server）从版本 6 开始不再在服务器端支持 JavaScript。这可能与 iPlanet 是 Sun Microsystems 的一部分有关，而 Sun Microsystems 更倾向于让程序员使用 Java。

而且，尽管 Microsoft 的 ASP 环境取得了巨大成功，但开发人员在为该平台开发时更倾向于使用 VBScript。随着 Microsoft ASP .NET 平台的推出，VB .NET 和 C# 已成为开发人员使用最多的两种语言。

Microsoft 在 Visual Studio .NET 开发环境中加入 JScript .NET 支持时，为 JavaScript 社区帮了一个小忙。JScript .NET 可以访问 .NET Framework 的所有类，并且是第一个（尽管非常早期）支持 ECMAScript 第 4 版提案功能的实现。

尽管 ECMA 赋予了 JavaScript 作为完整编程语言运行的能力，但 JavaScript 并不一定适合所有环境。你可能不希望将 JavaScript 用作以下类型任务的编程语言：

- 非常大规模的应用程序
- 性能关键型应用程序
- 设备驱动程序和其他低级程序

毕竟，我们不想看到所有那些 C++ 程序员失业，对吧？

#### 决定使用哪个版本的 JavaScript

JavaScript 开发人员必须在开发过程的早期做出一项决定：他们希望支持该语言的哪个版本。有几项因素会影响这一决定，例如：

- 当前编程任务的规模和范围
- 程序未来增强的可能性
- 程序需要与用不同编程语言编写的其他程序轻松互操作的需求
- 需要利用 JavaScript 2.0 中提供的新功能（例如，新的内置对象）
- 你最喜欢的开发工具支持的 JavaScript 版本
- 你的绝大多数目标受众支持的 JavaScript 版本

到目前为止，最重要的考虑因素是最后一项。如果您的相当一部分目标受众仍在使用不支持 JavaScript 2.0 的浏览器，那么在网页中放置 JavaScript 2.0 是没有意义的。当然，如果您的程序仅驻留在服务器上（服务器端程序），那么重要的是服务器支持的版本。

同样重要的是记住计算机编程的基本原则之一：永远不要为任务编写超出绝对必要的代码。因此，如果您的 JavaScript 程序是一个将摄氏度转换为华氏度的三行脚本，就没有必要用 JavaScript 2.0 语法创建包和类（如第 5 章所讨论）。您可能出于其他原因想要这样做，包括程序未来的可扩展性。但这也是*如果没坏*的情况……

因此，作为一般规则，如果您的目标受众可能运行各种 Web 浏览器，那么对开发客户端 JavaScript 2.0 代码要非常谨慎。否则，如果您确定知道最低浏览器版本将是多少，或者是在服务器或嵌入式环境中开发，请随意尽情使用 JavaScript 2.0 中的新功能和改进！

#### 使用 HTML 测试 JavaScript 程序

在深入了解 JavaScript 基础知识之前，我们需要设置一种测试代码的方法。测试 JavaScript 程序最简单的方法是将其放入 HTML 页面中，然后在支持 JavaScript 的浏览器中加载它。

要使用这种 HTML 方法运行本书中的任何代码示例，您需要一个 Web 浏览器。我建议使用 IE 5 或 Navigator 4 或更高版本，因为某些示例无法在早期版本中运行。

如果您想将计算机上的浏览器升级到更新的版本，可以访问 Microsoft 的 IE 网站 http://www.microsoft.com/windows/ie，或 Netscape Browser Central http://channels.netscape.com/ns/browsers。

#### 创建 JavaScript 模板

`<script>` 标签是用于标识 JavaScript 代码的 HTML 元素。使用记事本（或您最喜欢的 Web 开发工具）将此文件创建为模板并保存在您的硬盘上是个好主意。这样，使用此 HTML 代码作为基础来开始创建由 JavaScript 驱动的网页将会容易得多。

以下是在记事本中创建模板的步骤：

1. 在 Windows 中，单击"开始"菜单按钮。

2. 从弹出菜单中选择"运行"。

3. 如图所示输入 notepad，然后按 ENTER 键。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_35_0.png)

4. 在记事本中，输入以下 HTML 代码：

```
<html>
    <head>
        <title>JavaScript sample code</title>
    </head>
    <body>
        <h1>My Sample Code</h1>
        <script language="JavaScript" type="text/javascript">
```

```
<!-- // Begin
    // NOTE:: Replace this line with JavaScript code
// End -->
</script>
</body>
</html>
```

5. 选择"文件"菜单，然后选择"另存为"。

6. 导航到硬盘上的所需位置。"我的文档"文件夹通常被使用，但您也可以选择将其保存到任何您选择的目录。

> 我们将在整本书中使用此 HTML 文件来运行 JavaScript 代码示例，因此请将其放在方便的位置。

7. 为 HTML 文件指定一个以 **.htm** 结尾的名称，例如 **JSTemplate.htm**。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_36_0.png)

8. 关闭记事本。

9. 从 Windows 桌面选择"我的电脑"。这将打开 Windows 资源管理器，允许您导航到保存 HTML 文件的目录。

10. 双击 HTML 文件。Web 浏览器（通常是 Microsoft Internet Explorer）将打开您的 HTML 文档。

11. 您应该看到大字体的"My Sample Code"字样。

12. 完成后关闭浏览器窗口。

图 1-4 显示了 HTML 模板在浏览器中的样子。这是 HTML 页面中最基本的 `<script>` 标签示例。



##### 理解 JavaScript 模板

请记住，HTML文档被划分为两个不同的部分：头部区域和主体区域。HTML文档总是以`<html>`标签开始，并以`</html>`结束标签结束。同样，HTML头部区域由`<head>`和`</head>`标签界定，如下所示：

```html
<head>
    <title>JavaScript sample code</title>
</head>
```

通常，头部区域内的HTML标记用于描述出现在主体区域的主要内容。最常见的是，头部区域包含：

- 一个必需的文档标题（`<title>`）
- 样式表定义（`<style>`和`<link>`）
- 元数据，例如搜索关键词（`<meta>`）
- JavaScript函数（`<script>`）

HTML文档的大部分内容位于主体区域内，由`<body>`和`</body>`标签界定。在此部分中，你会找到文本、图像、表单和嵌入式内容。JavaScript也可以在该部分中使用，以向屏幕输出动态文本。我们模板的主体区域如下所示：

```html
<body>
    <h1>My Sample Code</h1>
    <script language="JavaScript" type="text/javascript">
    <!-- // Begin
        // NOTE:: Replace this line with JavaScript code
    // End -->
    </script>
</body>
```

我们的主体区域以必需的`<body>`和`</body>`标签开始和结束。`<h1>`和`</h1>`标签表示标题文本。`<h1>`是字体最大的预定义标题。`<h2>`、`<h3>`、`<h4>`、`<h5>`和`<h6>`标签表示字体大小递减的标题。

我在主体区域中包含了一个`<script>`元素以供后续使用。我为此标签添加了两个属性：`language`和`type`。`language`属性是早期表示标签内所用脚本语言的方式。尽管最近版本的HTML（及其后继者XHTML）已逐步淘汰此属性的使用，但使用它仍然相当普遍。`type`属性是当前推荐用于指示所用脚本语言的方式。

模板在`<script>`部分包含三行代码：

```javascript
<!-- // Begin
    // NOTE:: Replace this line with JavaScript code
// End -->
```

所有这三行都是注释。在Web编程中，注释是浏览器在解释代码时忽略的一行或多行文本。程序员经常使用注释使程序更易于人类阅读，但在前面的代码中，第一行和最后一行用于阻止不支持JavaScript的浏览器显示代码。随着时间的推移，这种技术变得越来越不重要。但它仍然相当普遍，而且确实没有理由不包含它。`<!--`和`-->`是HTML注释开始和结束的标记。JavaScript注释用双斜杠（`//`）标记，这就是为什么浏览器也会忽略第二行。

#### 与用户交互

许多JavaScript程序会静默地执行任务。一个网页可能使用JavaScript来验证表单上的所有字段是否都已正确填写。当它们填写完成时，JavaScript程序允许表单提交到Web服务器进行进一步处理。但是，如果一个表单字段没有正确填写，理想情况下，JavaScript应该通知用户，以便他们可以更正问题并再次提交表单。

通常有两种方式可以让用户注意到这样的错误。第一种是利用JavaScript的警报框，它要求用户单击“确定”按钮才能继续处理。这被认为是一种稍显侵入性的技术，可确保用户阅读并确认错误消息。

另一种方式是直接在网页内编写信息性消息。这显然是一种侵入性较小的技术，尽管你必须确保用户不会意外忽略该消息。

在本节中，我们将研究如何使用这两种方法与用户进行交互，因为在我们进入下一章之前，这两种方法都很重要。

##### 显示警报消息

JavaScript提供三种类型的弹出对话框，可在你的应用程序中使用：

- 警报框
- 确认框
- 用户输入提示框

基本的警报消息使用内置的`alert`函数显示：

```javascript
alert ("This message will be displayed to the browser");
```

你可以在括号内放置任何文本字符串或表达式。在Internet Explorer中显示的对话框如下所示。

Netscape Navigator显示类似的消息框。

确认框的工作方式与警报框非常相似，不同之处在于它向用户显示“确定”和“取消”两个按钮。确认框会告诉程序用户选择了哪个按钮，从而允许两种不同的结果。

```javascript
result = confirm ("Would you like a piece of chocolate cake?");
```

如果用户选择“确定”按钮，`result`变量将包含`true`，否则为`false`。这就是Internet Explorer中确认框的外观。

最后，用户输入提示框允许程序要求用户输入对消息的响应。这在互联网网页上很少使用，因为HTML网页表单是获取用户输入更常用的方式。

```javascript
firstname = prompt ("What is your first name?",
"Enter name here");
```

此JavaScript代码的结果如图所示。

##### 将文本写入浏览器窗口

本书中的许多示例将使用`document.write()`函数将文本打印到Web浏览器窗口中。这不仅仅用于错误报告。事实上，经常可以看到网站使用`document.write()`来支持动态功能，如导航、用户帮助、横幅广告轮播等。

```javascript
document.write ("<b>This text goes right into the browser</b>")
```

请注意，你可以在`document.write()`函数内包含HTML标签，浏览器将处理这些标签。通过在我们的HTML模板中添加几条`document.write()`语句，我们可以创建一个内容更丰富的网页。

```html
<html>
    <head>
        <title>JavaScript sample code</title>
    </head>
    <body>
        <h1>Hamlet, by Bill Shakespeare</h1>
        <script language="JavaScript" type="text/javascript">
        <!-- // Begin
            // NOTE:: Replace this line with JavaScript code
            document.write
                ("To be, or not to be: that is the question:<br>");
            document.write
                ("Whether 'tis nobler in the mind to suffer<br>");
            document.write
                ("The slings and arrows of outrageous fortune,<br>");
            document.write
                ("Or to take arms against a sea of troubles,<br>");
            document.write
                ("And by opposing end them.<br>");
        // End -->
        </script>
    </body>
</html>
```

正如你在图1-5中看到的，我们的`document.write()`语句被输出到屏幕上的方式，就好像我们直接将它们输入到HTML中一样。当我们进入下一章，学习变量、函数和语句时，这项技术会变得更加有用。

现在我们已经涵盖了无聊的内容——语言的历史及其用途——我们准备好进入一些真正的编程了。下一章首先介绍JavaScript的基础知识，让你准备好开始自己编写代码。

#### 了解更多关于本章讨论的主题

有几本好书可供进一步学习HTML和Java，例如：

- *How to Do Everything with HTML*，James Pence 著（McGraw-Hill/Osborne，2001）
- *HTML: A Beginner's Guide*，第2版，Wendy Willard 著（Osborne，2002）
- *Java 2: A Beginner's Guide*，Herbert Schildt 著（Osborne，2000）
- *Learn to Program with Java*，John Smiley 著（Osborne，2001）



**图 1-5** 哈姆雷特的著名独白，由 JavaScript 演绎

此外，您可能需要查看以下一些网站：

- DevGuru: http://www.devguru.com
- W3 Schools: http://www.w3schools.com/html
- Sun Microsystems 的 Java 主页: http://java.sun.com
- JavaRanch: http://www.javaranch.com

## 第 2 章

## 学习 JavaScript 基础

#### 如何...

-   定义变量
-   定义常量
-   理解程序流程
-   有条件地执行代码
-   使用循环重复语句
-   为代码添加注释
-   设置默认对象
-   处理错误
-   理解表达式的基础知识
-   将代码组织成函数
-   利用 JavaScript 2.0 的改进功能创建更强大的函数

JavaScript 高度依赖其他技术的帮助。事实上，如果你尝试用 JavaScript 编写一个完全不依赖官方 JavaScript 规范之外任何东西的程序，那么这个程序将无法做太多事情。JavaScript 依赖外部组件与外界进行通信，例如写入屏幕、从网页表单检索数据以及接收浏览器事件通知。

在本章中，我们将探讨 JavaScript 的基础知识。我们将通过学习语句、变量和函数——任何程序的三大基本构建块——来了解编写程序的基础。

#### 理解基本术语

与其他专业的从业者一样，计算机程序员多年来也发展出了自己的行话。诸如 *变量*、*函数* 和 *字符串* 这样的普通英语单词被赋予了与计算机相关的含义。表 2-1 列出了您将在本章及全书中遇到的一些编程术语。

#### 在变量中存储数据

归根结底，在现代计算中只有三个地方可以存储信息：硬盘、数据库或内存。当然，还有其他数据存储介质，如软盘、光盘、Zip 磁盘和备份磁带，信息可以保存在上面，但这些介质所需的设备比硬盘驱动器慢得多——有时记录相同数据需要花费 100 倍甚至更长的时间。因此，应用程序程序员通常不能——也不应该——在存储信息时依赖这些介质中的任何一种。

| 编程术语... | 指的是... |
| --- | --- |
| 语句 | 一行编程代码；在 JavaScript 中，语句通常用分号 (;) 分隔。 |
| 变量 | 用于存储可在程序执行期间更改的值的命名位置。 |
| 常量 | 用于存储在程序执行期间不能更改的值的命名位置。 |
| 函数 | 一组执行某些操作的命名语句，并可选择返回一个值。 |
| 关键字 | 在 JavaScript 中具有预定义含义的词，不能用于任何其他目的。 |
| 运算符 | 通常是一个符号（如 +、-、* 或 /），它接受一个或多个值（称为操作数）并返回一个结果。 |
| 表达式 | 关键字、运算符、变量和/或函数的组合，可以从中计算出结果。 |
| 字符串 | 0 个或多个字母、数字或其他文本字符的序列；字符串通常用引号括起来，如 "this is a string"。 |
| 布尔值 | 计算结果为 true 或 false 的值或表达式。 |
| 字面量 | 直接写在代码中的布尔值、数字或字符串；例如，表达式 ((3+2)/total) 包含两个数字字面量 3 和 2。 |
| 值 | 一个数字、布尔值、字符串或对象。 |

表 2-1 常见 JavaScript 编程术语

在硬盘上，信息以文件的形式存储。在数据库中，信息以记录的形式存储。但在内存中，程序数据使用变量进行存储和检索。变量是内存中的命名部分。

##### 定义变量

在 JavaScript 1.5 中，变量使用 **var** 关键字声明：

```
var counter;
```

这段代码告诉 JavaScript，我们打算将信息存储在一个我们称之为 "counter" 的变量中。以这种方式定义的变量可以包含任何类型的信息：数字、字符串、布尔值（true 和 false）或对象。为了方便起见，您可以为变量赋一个初始值，如下所示：

```
var counter = 5;
```

我们将名为 counter 的变量的初始值赋为 5。

JavaScript 2.0 将数据类型的概念引入了 JavaScript 编程。在此版本的语言发布之前，程序员无法预先定义变量可以包含的数据类型——所有 JavaScript 变量都可以被赋予任何类型的数据。

但随着这个重要的新版本的发布，我们现在可以将变量限制为某些类型的数据：例如，整数或字符串。尝试将不属于该变量预定义数据类型的数据赋值将导致错误。数据类型定义如下：

```
var counter : Integer;
```

这里定义的 counter 变量属于 Integer 数据类型。因此，该变量永远不能包含除整数以外的任何内容。（我们将在第 3 章探讨 JavaScript 2.0 中所有可用的数据类型。）

#### 定义常量

变量被称为 "marinade" 是有原因的：程序可以随时自由更改存储在变量中的值。常量与变量类似，但一旦赋值，常量就不能更改。

> 常量目前仅受 Netscape 6 及更高版本或 Mozilla 网络浏览器的支持。Microsoft IE 尚未纳入支持，因此使用常量应限于您绝对确定其安全的场景。

常量从 JavaScript 版本 1.5 开始引入，因此该语言的早期版本不支持它们。但其他编程语言（最著名的是 C）非常有效地使用了常量，它们在您的 JavaScript 编程中也可能很有用。

常量使用 const 关键字定义：

```
const ERR_INVALID_USERID;
```

在前面的代码中，我创建了一个名为 ERR_INVALID_USERID 的常量。注意我如何将名称大写。这不是强制性的，但这是 C 中经常使用的编程约定，因此您有时也会看到 JavaScript 中的常量被大写。

一旦设置了值，常量就不能更改。

```
const ERR_INVALID_USERID = 300;
ERR_INVALID_USERID = 50;    // 这将导致错误！
```

常量通常用于为错误代码和其他“有意义的”数字提供人类可读的名称。对于人类来说，阅读以下代码比直接使用错误数字要容易得多：

```
switch (returncode) {
    case ERR_INVALID_USERID:
        // 做些事情
    case ERR_INVALID_PASSWORD:
        // 做些其他事情
    case ERR_INVALID_DOMAIN_NAME:
        // 等等
}
```

与变量一样，在 JavaScript 2.0 中，常量也可以被赋予数据类型。

##### JavaScript 可以存储一些相当大的数字

JavaScript 2.0 中的整数是双精度浮点数，这使它们能够包含大约 +/-100 undecillion（1 后面跟着 38 个零）范围内的值。

#### 理解程序流程

本章的大部分内容致力于学习 JavaScript 编程语言、语句和函数的基础知识。但在我们深入探讨之前，花点时间研究一下 *程序流程* 是很重要的。

当我说到程序流程时，我指的是 JavaScript 执行程序代码的顺序。假设您有一个五行长的程序，JavaScript 总是从执行第一行代码开始。理论上，接下来执行第二行，然后是第三行，依此类推，直到最后一行（在我们的示例中是第 5 行）。图 2-1 说明了这一点。

实际上，这是对实际情况的极端简化。接下来要执行哪一行取决于当前行要求 JavaScript 执行的任务。如果当前行调用了一个函数，那么在 JavaScript 继续执行下一行之前，函数内的所有代码将首先被执行。如果当前行包含一个循环，同一组行将被重复执行。如果当前行声明了一个要定义的新函数，JavaScript 将把该函数读入内存，而不执行其中的任何代码（直到它在程序中的其他地方被调用）。



#### 使用语句控制程序流程

我们在第1章中定义的HTML模板（参见"创建一个JavaScript模板"）Mgmtv除了显示一些标题文本外，并没有真正做什么有用的事情。让我们JavaScript程序能够执行任何操作的唯一方法是添加一些语句。

*语句*是任何程序代码中的基本动作项。实际上，每条语句都在告诉计算机执行某些操作。语句可以分为五类：

- 条件语句
- 循环语句
- 对象操作
- 注释
- 表达式

典型的JavaScript程序会使用属于上述各类的语句。通常，程序内部的语句还会被组织成函数和类，以便使程序更易于管理和更高效地开发。我们将在本章稍后更详细地研究函数，并在第5章研究类。

#### 有条件地执行代码

计算机程序几乎总是包含*条件语句*。JavaScript中有两种条件语句：**if**和**switch**。**if**语句允许程序根据某个预定义的因素在两种选择之间进行选择。在现实生活中，你可能会决定，如果没有下雨，你就去看棒球比赛。当然，如果下雨了，你就会决定待在家里。你可以在JavaScript程序中用以下代码做出同样的决定：

```
function stay_or_go (raining) {
    if (raining == false) {
        return "Go to baseball game!";
    } else {
        return "Got to stay home today.";
    }
}
```

你看，条件语句让程序在两个或多个选项之间做出选择，这与我们在现实生活中做出这些选择的方式非常相似。

##### if 语句

根据使用方式的不同，**if**语句可以非常简单，也可以非常复杂。**if**语句可以通过以下方式使用。

| 语法 | 用途 |
|--------|-----|
| if (*expression*) {*statements*;} | 如果*expression*求值为true，则执行*statements*。 |
| if (*expression*) {*statements1*;} else {*statements2*;} | 如果*expression*求值为true，则执行*statements1*。否则，执行*statements2*。 |
| if (*expression1*) {*statements1*;} else if (*expression2*) {*statements2*;} else {*statements3*;} | 如果*expression1*求值为true，则执行*statements1*。否则，如果*expression2*求值为true，则执行*statements2*。否则，执行*statements3*。 |

**if**语句对表达式进行求值，以确定要执行哪组语句（如果有的话）。由于**if**语句期望一个布尔表达式（一个求值为true或false的表达式），它会尝试将其他数据类型的表达式转换为true或false。

> JavaScript在从其他数据类型转换为布尔值时会做出某些假设。字符串"true"和"false"分别求值为布尔值*true*和*false*。整数1和0也分别转换为布尔值*true*和*false*。

在计算机编程术语中，表达式是一段代码，当对其求值时，会返回一个值。在JavaScript中，以下可以用作表达式。

| 表达式 | 示例 |
|------------|---------|
| 变量 | if ( x ) {*statements*;} |
| 返回值的函数 | if ( myfunc(x) ) {*statements*;} |
| 字面量 | if ( true ) {*statements*;} |
| 使用运算符组合的变量、函数和字面量 | if ( a > 5 ) {*statements*;} |

即使相同的**if**语句也可以至少用四种不同的方式编写，所有这些都是有效的：

- `if (expression) statement;`
- `if (expression)\n    statement;`
- `if (expression) {statements;}`
- `if (expression) {\n    statements;\n}`

前述各种形式的**if**语句在技术上是等效的。前两种只能包含一条语句。请注意，第三种和第四种形式使用大括号{和}来括住语句。括在大括号中的语句通常被视为一组，称为*语句块*。

**if**语句可以包含可选的**else**子句，以在两种选择之间做出决定。这种形式的语句有时被称为***if-else*** *语句*：

```
if (expression) {statements1;}
else {statements2;}
```

**else**子句允许你指定当表达式不求值为true时将执行的语句或语句组。在任何**if**语句中只允许有一个**else**子句。同样，该语句可以带或不带大括号使用。

最后，**if**语句可用于在三种或更多选择之间进行选择。随着**else-if**子句的引入，**if**语句可以包含多个表达式，每个表达式都会被求值，直到其中一个求值为true或遇到**else**子句为止。可以包含多个**else-if**子句，但请记住，**else-if**子句必须始终位于任何**else**子句之前。

```
if (expression) {
    statements;
} else if (expression) {
    statements;
} else {
    statements;
}
```

> **提示** *如果你发现自己在一个**if**语句中使用了超过两个或三个**else-if**子句，你可能需要考虑使用**switch**语句代替，如以下部分所述。*

##### switch 语句

**switch**语句在JavaScript中与**if**语句的角色非常相似。**switch**语句对表达式进行求值，并将其值与一个或多个**case**子句进行比较。如果你需要将一个变量与超过两个或三个值进行比较，**switch**语句是最有效的方式。

以下代码显示了**switch**语句在JavaScript编程中的典型用法。在这个示例中，我们的程序将尝试根据国家官方的三字母ISO（国际标准化组织）国家代码来确定国家名称。

```
// ISO official country codes
switch (countrycode) {
  case "ALB":
    countrystring="Albania";
    break;
  case "DZA":
    countrystring="Algeria";
    break;
  case "ASM":
    countrystring="American Samoa";
    break;
  case "AND":
    countrystring="Andorra";
    break;
  case "AGO":
    countrystring="Angola";
    break;

  // etc.

  case "", "?":
  default:
    countrystring="Unknown code";
}
```

相同的代码可以使用**if-else-if**语句编写，但那样既低效又难以阅读。让我们看看前面的代码，看看发生了什么。

语句的第一行使用**switch**关键字，后跟需要求值的表达式。

```
switch (countrycode) {
```

在这个例子中，countrycode是一个恰好包含字符串的变量。
**switch**语句中的接下来三行包含第一个**case**子句。

```
case "ALB":
    countrystring="Albania";
    break;
```

**case**子句表明我们希望将countrycode的值（**switch**语句正在作用的表达式）与字符串"ALB"进行比较。如果完全匹配，JavaScript将执行接下来的两行：

- 将countrystring变量设置为"Albania"。
- 在**break**语句处退出**switch**语句。

当然，如果countrycode的值与字符串"ALB"不匹配，则不会设置countrystring变量，**switch**语句继续执行。
下一个**case**子句将表达式与新的值进行比较：

```
case "DZA":
    countrystring="Algeria";
    break;
```

**switch**语句按顺序求值每个case语句，直到找到匹配的一个。然后执行紧跟在**case**子句后面的代码，直到遇到第一个**break**语句。

> 一旦找到匹配项，JavaScript将执行随后所有代码，即使在其他**case**子句内部，直到遇到**break**语句。

在JavaScript中，**switch**语句有一种特殊的**case**子句，称为**default**子句。**default**子句仅在JavaScript无法将表达式与任何先前的子句匹配时执行。**default**子句必须始终是**switch**语句中的最后一个子句。

```
case "", "?":
default:
    countrystring="Unknown code";
```

我们的示例包括一个空的**case**子句，尝试与空字符串（""）或问号（?）匹配。你可以在单个case子句中提供多个值来与表达式匹配，只要它们用逗号分隔即可。如果表达式与我们的空case匹配，**default**子句内的代码将被执行，因为没有**break**语句来阻止它。

#### 使用循环重复语句

*循环*语句在以下两种情况下很方便：

- 当你想要重复一组语句特定次数时
- 当你想要重复一组语句未知次数时



##### while 循环

JavaScript 中有四种循环语句：**while**、**do-while**、**for** 和 **for-in**。JavaScript 还提供了 **break** 和 **continue** 语句，以便程序员能更精确地控制循环的执行方式。在本节中，我们将探讨所有与循环相关的语句，并了解它们在程序中的应用方式。

**while** 循环会在执行一组语句之前先计算表达式。它会反复执行这些语句，直到表达式的结果不再为 true。

```
while (expression) {
    statements;
}
```

JavaScript 按以下方式处理 **while** 循环。首先计算表达式，其值被解释为布尔值（true 或 false）。如果表达式结果为 true，则花括号内的语句将执行一次。然后再次计算表达式，如果结果仍为 true，语句将第二次执行。这个过程将无限持续，直到表达式结果为 false。

一个常见的编程陷阱是*无限循环*。无限循环是一种永不停止的循环语句，它最有可能在 **while** 语句中发生。大多数浏览器会在脚本执行时间过长时通知用户，允许他们强制终止无限循环。

![img](img/f14dd58a324d5464a114c30c1d4c4c9b_54_0.png)

为了避免无限循环，一个常见的编程实践是确保表达式总有计算结果为 false 的机会。以下 **while** 语句保证不会导致无限循环：

```
var counter = 1;

while (counter < 101) {
    document.write ("This is line number " + counter + "<br>\n");
    counter++;
}
```

这段代码将正好执行 100 次。我们知道这一点，是因为 counter 变量从 1 开始，在每次 **while** 循环迭代后都会增加 1。（我们将在本章后面学习运算符，如 ++ 运算符。在这段代码中，++ 运算符将 counter 变量增加 1。）当 counter 达到 101 时，循环将退出，因为“counter < 101”的结果将为 false。

如果我们把这段 **while** 循环粘贴到第 1 章的 HTML 模板中，会得到以下 HTML 代码：

```
<html>
    <head>
        <title>JavaScript sample code</title>
    </head>
    <body>
        <h1>My Sample Code</h1>
        <script language="JavaScript" type="text/javascript">
        <!-- // Begin
        var counter = 1;

        while (counter < 101) {
            document.write ("This is line number " + counter + "<br>\n");
            counter++;
        }
        // End -->
        </script>
    </body>
</html>
```

将这段 HTML 代码加载到 Web 浏览器中，你会看到类似图 2-3 的内容。浏览器窗口已滚动到底部，以准确展示打印了多少行。

![img](img/f14dd58a324d5464a114c30c1d4c4c9b_55_0.png)

**图 2-3** **while** 循环正好打印 100 行。

##### do-while 循环

**do-while** 循环的工作方式与 **while** 循环完全相同，但有一个例外。在 **do-while** 循环中，表达式是在每次迭代结束后计算的。这意味着循环至少会执行一次。而 **while** 循环在每次迭代前计算表达式，这意味着循环内的内容可能永远不会被执行。

```
do {
    statements;
} while (expression);
```

尽管表达式是在循环的每次迭代后计算的，但下面这个循环仍然正好执行 100 次。因此，选择 **do-while** 而不是 **while** 循环，唯一受影响的迭代是第一次执行循环。

```
var counter = 1;

do {
    document.write ("This is line number " + counter + "<br>\n");
    counter++;
} while (counter < 101);
```

你可以将 **while** 和 **do-while** 循环视为同一语句的两个版本。**do-while** 能做的任何事，**while** 都能做。因此，**do-while** 循环在实际应用中比 **while** 循环更少见。

##### for 循环

在刚才讨论 **while** 循环时，我们使用了以下示例：

```
var counter = 1;

while (counter < 101) {
    document.write ("This is line number " + counter + "<br>\n");
    counter++;
}
```

这个 **while** 循环可以使用 **for** 循环重写。事实上，这种类型的循环（使用计数器变量）更适合用 **for** 循环来实现。

```
for (var counter = 1; counter < 101; counter++) {
    document.write ("This is line number " + counter + "<br>\n");
}
```

如你所见，**for** 循环版本是循环预定义次数更高效的方式。**for** 循环语法有四个部分：

```
for (initializer; expression; incrementor) {
    statements;
}
```

*初始化部分*传统上用于定义变量并赋予其初始值。在我们的示例中，我们定义了一个名为 counter 的新变量，并将其设置为值 1。初始化部分包含的 JavaScript 代码仅在循环开始前执行一次。

*表达式*在每次循环前计算。语句是否执行取决于此表达式的布尔结果。

*递增部分*包含在每次循环执行后运行的代码。传统上，这是任何计数器递增或递减的地方。在我们的示例中，我们使用此部分将 counter 变量加 1。

这些部分中的每一个都是可选的。如果正在使用的变量已经定义并设置了值，则初始化部分可以为空。但不要忘记，中间的分号是必须的。事实上，以下代码是使用 **for** 语句的无限循环：

```
for (;;) {
    // do nothing
};
```

> 尽管这是无限循环的另一个示例（在编程中通常是个坏主意），但如果你的代码在循环内执行，当满足某个条件时执行 **break** 语句，那么这个循环就是一个有效的技术。

##### for-in 循环

我在这里只想简要提及 **for-in** 循环，以保持上下文连贯。你将在第 5 章讨论类和对象时看到关于它的详细讨论。

目前，你可以将对象想象成一个装满工具的工具箱。**for-in** 循环将从该工具箱中逐一提取每个工具，并允许你单独检查和操作它。

在下面的代码中，我们创建了一个简单的对象（兼容 JavaScript 1.5），并使用 **for-in** 循环检索其每个属性。

```
<html>
    <head>
        <title>JavaScript Test</title>
    </head>
    <body>
    <h1>for-in Loop</h1>
    <script language="JavaScript" type="text/javascript">
    <!-- // Begin
    // We define the tool chest object
    var toolchest = {tool1:"Wrench",
        tool2:"Hammer",
        tool3:"Cordless drill",
        tool4:"Needlenose pliers"};

    // for-in iterates over its properties
    for (var tool in toolchest) {
        document.write(toolchest[tool] + "<BR>");
    }

    // End -->
    </script>
    </body>
</html>
```

该程序创建了一个名为 toolchest 的对象。该对象使用对象字面量创建，如第 5 章所述。

```
// We define the tool chest object
var toolchest = {tool1:"Wrench",
    tool2:"Hammer",
    tool3:"Cordless drill",
    tool4:"Needlenose pliers"};
```

我们感兴趣的是 **for-in** 循环的代码：

```
// for-in iterates over its properties
for (var tool in toolchest) {
    document.write(toolchest[tool] + "<BR>");
}
```

此代码遍历 toolchest 对象的内容——tool1、tool2、tool3 和 tool4。执行时，程序会输出每个属性的值，如下所示。

![img](img/f14dd58a324d5464a114c30c1d4c4c9b_59_0.png)

##### break 和 continue 语句

我们在查看 **switch** 语句时已经见过 **break** 语句的实际应用。当 JavaScript 在 **switch** 内部遇到 **break** 语句时，它会停止执行 **switch** 内部的代码，并在 **switch** 后的第一条语句处继续执行。

**break** 语句在循环中的工作方式类似。当 JavaScript 遇到 **break** 语句时，它会停止执行循环内的代码，并在循环外的第一条语句处重新开始。**break** 语句在循环或 **switch** 语句外部无效。

**continue** 语句也会导致 JavaScript 停止执行循环内的代码，但执行会继续到循环的下一次迭代。实际上，**break** 语句表示“退出循环”，而 **continue** 语句表示“跳过本次迭代，继续下一次”。**continue** 语句在循环外部同样无效。

```
var Fahrenheit, Celsius;
for (Celsius = -70; Celsius <= 70; Celsius += 10) {
    Fahrenheit = (Celsius * 9/5) + 32;
    document.write ("Celsius = " + Celsius);
    document.write (", Fahrenheit = " + Fahrenheit + "<br>");

    if (Fahrenheit > 100) {
        // It's getting hot in here
        break;
    }
}
```



此代码中的 **for** 循环设计用于遍历所有从 –70 开始的摄氏度，每次迭代增加 10 度，直到摄氏度达到 +70 度（–70、–60、–50、–40 等）。

但如果你检查循环内部的代码，它会告诉 JavaScript 在温度超过 100° 华氏度时跳出循环。由于 100° 华氏度约等于 37° 摄氏度，因此循环实际上会在摄氏度达到 40 时退出，而不是 70。**break** 语句会导致循环过早退出。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_60_0.png)

**continue** 语句在你想要遍历一系列值并忽略不符合特定条件的值时非常有用。但当你找到符合的值时，你可能有很多代码需要在循环内执行。此时，与其用一个巨大的 **if** 语句包裹数十行代码，不如使用 **continue** 语句跳过并进入下一次迭代。

```
// 哪些数字能被23整除？
var iNumber;
for (iNumber = 1; iNumber <= 1000; iNumber++) {
    if (iNumber % 23 > 0) {
        // 不能被23整除
        continue;
    }
    document.write("<b>" + iNumber + "</b>");
    document.write(" 能被23整除！<br>");
}
```

在此代码中，循环设计执行 1,000 次，遍历从 1 到 1,000 的数字。循环内的 **if** 语句使用取模运算符（%）检查数字是否能被 23 整除。如果不能被 23 整除，则执行 **continue** 语句——跳过当前循环的剩余部分，并开始循环的下一次迭代。

每 23 个数字（这结果挺巧的），我们就会遇到一个能被 23 整除的数字。此时 **continue** 语句不会执行，循环的剩余部分有机会运行。在我们的示例中，我们使用 document.write() 函数输出我们终于找到匹配数字的好消息。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_61_0.png)

#### 使用标签

*标签* 是一个命名的代码行。由于它们唯一的目的是与循环（特别是嵌套循环）相关，因此标签在现实中很少使用，尽管了解它们的存在很重要。

> 在编程术语中，当你将一个循环完全放在另一个循环内部时，就创建了嵌套循环——例如，在 **while** 循环内部有一个 **for** 循环。在这种情况下，**for** 循环称为内循环，而 **while** 循环称为外循环。循环可以嵌套多层。

标签很容易创建。

1. 使用文本编辑器（如记事本）打开你的 JavaScript 程序。
2. 选择你想要命名的代码行。标签必须出现在有效语句的开头。
3. 输入标签名称，只使用字母或数字。名称中不允许有空格或其他特殊字符。
4. 以冒号（:）结束标签。

例如，在以下代码中，我们有一组嵌套循环，并且它们都被标记了。

```
var x, y, z;
outer: for (x = 1; x < 20; x++) {
    middle: for (y = 1; y <= x; y++) {
        inner: for (z = 1; z <= y; z++) {
            document.write
                ("x = " + x + "; y = " + y + "z = " + z + "<br>");
        }
    }
}
```

在此代码中，我们有三个循环。最内层作用于变量 z 的循环被标记为 "inner"。包围名为 "inner" 循环的中间循环被称为 "middle"。而最外层循环被命名为 "outer"，它包围了中间和内层循环。

给循环加标签的唯一原因是 **break** 和 **continue** 语句被设计为与标签一起工作。通过在内层循环的 document.write 函数调用之后立即添加以下代码，你可以导致所有三个循环过早退出：

```
break outer;
```

当你在内层循环（不一定是最内层）中有一个条件，使你希望停止处理所有循环——或者甚至只是停止处理两个最内层的循环并继续处理外层循环时，这很方便。例如，将以下代码放在前面代码的最内层循环中，将导致变量 y 和 z 永远无法超过值 1，而 x 则被允许递增到 20：

```
break middle;
```

#### 为代码添加注释

我们在第一章简要讨论过注释。注释实际上不是一种语句类型，尽管为了方便起见，它们通常与其他 JavaScript 语句归为一类。在 JavaScript 程序中有两种添加注释的方式。

你可以通过以两个斜杠开始注释来添加单行注释。

```
// 斜杠后的内容将被 JavaScript 忽略
```

也可以在同一行中包含有效代码和注释。

```
var Students = 3;      // 班上会有三名学生
```

另一种注释代码的方式是使用块注释。块注释以斜杠和星号（/*）开始。

```
/* 这是块注释的开始
```

块注释持续直到遇到星号和斜杠（*/），即使注释跨越多行也是如此。

```
/* 这是块注释的开始
    这些也会被忽略
    document.write ("这也不会被执行！");
    因为它仍然被视为注释 */
```

当你为自己开发小型 JavaScript 程序时，你可能不希望花太多时间注释代码。这没关系——这叫做程序员的特权。然而，你可能会发现注释在以下原因中有用：

- 你可以在程序中包含版权声明。
- 你可以用"简单的英语"描述程序或函数的功能。
- 在开发阶段或调试时，有时你希望代码不执行，但又不想删除它。
- 注释也可以作为你将来想要添加的代码的占位符。

如果你是专业创建程序，你可能被要求包含大量注释，以便其他人更容易理解你的代码。

#### 设置默认对象

我们在这本书中还没有花时间研究可编程对象的概念，我将把大部分讨论推迟到第 3 章和第 5 章，届时我们将讨论内置对象和用户定义类。但为了理解 **with** 语句及其为一组语句指定默认对象的能力，让我们花点时间了解一下对象、方法和属性是什么。

为了理解编程中的对象概念，将其与现实世界进行类比是有帮助的。现实生活中的几乎任何事物都可以被看作是一个可编程对象——一辆汽车、一台电视、一个咖啡杯，甚至一个人。在编程中，对象既可以有 *方法* 也可以有 *属性*。对象的方法是它可以采取的操作，而对象的属性描述对象。

例如，假设我们在 JavaScript 中创建了一个 Person 对象。在现实生活中，一个人通常具有某些独特的特征，例如名字、头发颜色、眼睛颜色和身高。这些特征将被定义为 Person 对象的属性。在现实生活中，一个人可以采取行动。

##### with 语句

**with** 语句允许你访问对象的方法和属性，而不必在每一行都指定对象的名称。没有 **with** 语句，你总是需要在你希望访问的每个属性或方法旁边指定你正在处理的对象名称：

```
person.fullname = "Bob Jones";
person.haircolor = "Black";
person.eat();
person.sleep();
```

但当语句被 **with** 语句包围时，对象名称是隐含的，如：

```
with (person) {
    fullname = "Bob Jones";
    haircolor = "Black";
    eat();
    sleep();
}
```

当 JavaScript 首次在 **with** 语句中遇到对 fullname 的引用时，它将首先检查是否存在名为 fullname 的变量。如果没有，它将检查 person 对象是否有一个名为 fullname 的属性。如你所见，当你需要在许多行中重复访问同一个对象时，将你的代码放在 **with** 语句中可能是有意义的。

**with** 语句对程序员来说可以是一个方便的语句——任何节省打字的东西都是方便的。但一些开发者认为使用 **with** 语句也会使你的程序有点难以阅读。借助大多数文本编辑器中的复制粘贴技术，你可能没有太多理由需要在程序中使用此语句。

```
with (document) {
    write("墙上有99瓶啤酒<br>");
    write("99瓶啤酒<br>");
    write("如果其中一瓶恰好掉下来<br>");
    write("墙上还有98瓶啤酒<br><br>");

    write("墙上还有98瓶啤酒<br>");
    write("98瓶啤酒<br>");
    write("如果其中一瓶恰好掉下来<br>");
    write("墙上还有97瓶啤酒<br><br>");
}
```



在前面的代码中，我们首先声明我们希望 `document` 成为默认对象。注意，我们随后如何开始使用 `write()` 方法而完全无需提及 `document`。

> 使用 **with** 语句设置的默认对象仅适用于花括号内的代码。在花括号外部，则必须再次显式引用该对象。

#### 处理错误

对于大多数开发者来说，编程中遇到的最困难的挑战可能是智能地处理错误。在 JavaScript 编程中，*错误* 是浏览器在尝试运行程序时遇到的问题。错误可能由浏览器发现并认为不妥的内容触发，这称为 *系统错误*。或者也可能由你的程序发现并认为不妥的内容触发，这称为 *应用错误*。

一个 JavaScript 程序很容易因为添加了合理的错误处理代码而使规模翻倍。错误处理代码通常是程序员必须编写的额外代码，用于检查错误的存在并进行相应处理。在 JavaScript 中，如果程序不包含错误处理代码，通常浏览器会将问题呈现给用户。

错误处理的问题在于，编写良好的错误处理代码往往需要花费与编写程序其余部分一样多（甚至更多）的工作。因此，出于各种原因，程序员常常跳过这一步。

编写一个不包含任何错误处理代码的程序（使用任何语言）实在太容易了。你可以告诉计算机去数据库，读取一些值，向用户请求一些输入，将用户的输入添加到现有数据中，然后将其放回数据库。在 Visual Basic 等编程语言中，大约 30 行代码就可以完成。但这假设永远不会出错。仔细想想，很多事情都可能出错：

-   数据库不可用。
-   数据库可用，但你无法登录。
-   你可以登录数据库，但数据不可用。
-   从数据库检索到的数据包含无效值。
-   用户输入了无效值。
-   将用户的数据添加到数据库数据中导致错误。
-   你无法将数据保存回数据库。

因此，当你为程序添加处理所有这些错误的代码时，你突然发现自己面对的是一个 120 行的程序，而不是 30 行的程序。所以你看，避免担心这类事情当然更容易。

但当你在专业地编写程序时，你 *必须* 担心错误是如何处理的。当用户输入错误值时，程序应该崩溃吗？或者你是否应该继续执行，将错误数据写入数据库，导致程序下次运行时出错？或者最佳解决方案是通知用户他们的错误并要求他们重试？这就是为什么需要捕获并妥善处理这类错误。

##### try-catch 语句

Web 浏览器根据浏览器类型和版本，以及在一定程度上根据用户的浏览器设置，以不同的方式处理错误。在某些情况下，如果你在网页中包含一些错误的 JavaScript 代码，浏览器可能根本不会运行它，没有错误消息或其他迹象表明出了问题。在其他情况下，浏览器会弹出一个消息框，显示其遇到的错误详情，并询问用户下一步该怎么做。JavaScript 错误消息通常看起来像这样。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_66_0.png)

对于 JavaScript 开发者来说，这两种默认的错误处理方法都不理想。完全忽略错误会阻止程序执行。而向用户显示一个不美观的错误消息可能会让程序员感到尴尬——更不用说让用户感到沮丧了。

> Netscape 和 Microsoft 使用此语句的方式与官方 ECMA 规范定义的内容存在一些细微差别。在本节中，我使用的是大多数 Web 浏览器支持的语句形式。

**try-catch** 语句用于允许程序自己处理错误，而不是让浏览器处理它。它通常用于包装可能失败的语句或语句集。该语句具有以下语法：

```
try {
    statements;
}
catch (variable) {
    // error handling code
    statements;
}
```

> **try-catch** 语句仅在 JavaScript 1.4 中添加，因此只有较新的浏览器（如 IE 5.5 和 Netscape 6）支持它。

例如，你可以使用 **try-catch** 语句包裹一个函数调用，并在失败时向用户报告更友好的错误消息。

```
try {
    open_database();
}
catch (err) {
    // error handling code
    alert("An error occurred connecting to the database." +
          " Please try again in a few minutes.");
}
```

这样，用户收到的将不再是难看的 JavaScript 错误消息（或者根据浏览器设置根本收不到），而是一个更友好的消息，要求他们几分钟后重试：

![](img/f14dd58a324d5464a114c30c1d4c4c9b_67_0.png)

实际发生的官方系统错误消息仍然作为 `catch` 子句的参数传递给该语句。在我们的示例中，变量 `err` 包含所发生错误的描述。因此，如果你需要在 `catch` 子句中确定发生了什么，你是可以做到的。你甚至可以向用户显示原始的错误消息文本。

**try-catch** 语句不仅用于捕获系统错误；你也可以使用此结构来捕获由你自己程序生成的错误。

当你的程序试图做一些可能导致错误的事情时（例如，你的程序试图连接到一个嵌入式 Java 小程序），使用 **try-catch** 语句是一个好主意。小程序可能会遇到问题而无法加载，或者浏览器的安全设置可能不允许某些 Java 小程序运行。如果你将这样的代码包裹在 **try-catch** 语句中，你就可以检测到这个问题，并将用户重定向到应用程序的非 Java 版本。

你的应用程序还可以通过编程方式检测到的许多其他错误，包括：

-   表单中的无效用户输入
-   不支持的浏览器制造商或版本
-   缺失或无效的浏览器 Cookie

##### throw 语句

**throw** 语句允许 JavaScript 程序以与系统错误完全相同的方式声明错误。这意味着这些错误可以使用 **try-catch** 语句来捕获。

这也意味着，未被捕获的用户声明错误会以 JavaScript 弹出对话框的形式显示给用户。

> 与 **try-catch** 语句一样，**throw** 语句仅在 JavaScript 1.4 中添加，因此只有较新的浏览器（如 IE 5.5 和 Netscape 6）支持它。

以下是一个程序抛出自身错误的示例。

```
try {
    var errors = 0;
    // Do something
    errors++;
    if (errors > 0) {
        throw "Could not find the file.";
    }
}
catch (errorstring) {
    alert("The following error occurred:\n\n" +
        errorstring);
}
```

#### 理解表达式的基础

我们在本章中研究的许多编程语句都使用表达式来做某种决定。*表达式* 是任何返回值的东西。表 2-2 列出了常见的表达式类型及其使用示例。

| 表达式 | 示例 |
|---|---|
| 数字字面量 | 47 |
| 字符串字面量 | "Hello" |
| 布尔字面量 | true |
| 对象字面量 | {make : "Toyota"} |
| 程序定义的变量 | x |
| 程序定义的函数 | get_toast() |
| Null | null |
| 赋值表达式 | x = 5 |
| 数学运算 | x + y |
| 布尔运算 | x == y |
| 条件运算符 | x == 5 ? "yes" : "no" |
| 组合 | x = "You have " + messagecounter + " new messages" |

**表 2-2** 常见表达式类型



有些语句，例如 **if** 语句或 **while** 语句，特别要求返回布尔值（true 或 false）的表达式。JavaScript 会尽其所能自动将字符串和整数转换为适当的布尔值。表达式还常用作函数的参数，也可以本身作为语句使用。

```
x = 5;
```

这段代码是一个表达式，但它也是一个语句。它将值 5 赋给变量 x。

#### 使用运算符创建复杂表达式

JavaScript 提供了许多运算符来在代码中执行数学和其他功能。有些运算符会修改它们所操作的变量，但大多数不会。所有运算符都会返回一个值，因此可以用来创建复杂表达式。

JavaScript 中有 12 种类型的运算符，以及几十个单独的运算符。大多数运算符由符号表示（如 +），而有些运算符由单词表示（如 **new**）。大多数运算符需要两个操作数，而有些运算符只需要一个（尤其是一元运算符）。

表 2-3 列出了 JavaScript 1.5 中可用的运算符。

| 运算符类型 | 运算符 |
| :--- | :--- |
| 成员 | 点号 (.)<br>方括号 ([]) |
| 一元 | new<br>delete<br>typeof<br>instanceof<br>void<br>++<br>--<br>取反 (-)<br>逻辑非 (!)<br>按位非 (~) |
| 乘法 | 乘法 (*)<br>除法 (/)<br>取模 (%) |
| 加法 | 加法 (+)<br>减法 (-) |
| 位移 | 左移 (<<)、无符号右移 (>>>)、有符号右移 (>>) |
| 关系 | 小于 (<)<br>大于 (>)<br>小于等于 (<=)<br>大于等于 (>=)<br>in |
| 相等 | 等于 (==)<br>不等于 (!=)<br>全等于 (===)<br>不全等于 (!==) |
| 按位逻辑 | 按位与 (&)<br>按位或 (\|)<br>按位异或 (^) |
| 逻辑 | 逻辑与 (&&)<br>逻辑或 (\|\|)<br>逻辑异或 (^^) |
| 条件 | 条件 (?:) |
| 赋值 | 等号赋值 (=)<br>快捷赋值 (*=, /=, +=, -=, %=, <<=, >>=, >>>=, &&=, \|=, ^=, &=, \|=, and ^=) |
| 特殊 | 逗号 (.)<br>function<br>this |

表 2-3 JavaScript 中可用的运算符

JavaScript 2.0 向语言中添加了两种新运算符，它们都被视为关系运算符：

- is
- as

在本章中，我们已经看到了其中一些运算符的实际应用，例如等于 (==)、大于 (>)、递增 (++)、in 和等号赋值 (=)。这些运算符中的大多数起源于数学。还有一些额外的运算符用于处理逻辑布尔值（如逻辑与和逻辑或），以及用于处理二进制数学中的 1 和 0 的二进制运算符。

#### 将代码组织成函数

也许偶尔会有这样的情况，你可以坐下来编写整个 JavaScript 程序而不使用函数，但信不信由你，这种类型的 JavaScript 程序非常罕见。大多数 JavaScript 程序至少包含一个函数。

函数允许你在实际需要调用代码之前预先定义一组 JavaScript 语句。由于函数可以被重复调用，并使用不同的参数，因此它们也能节省大量时间。

#### 定义函数

函数使用 **function** 关键字定义。函数必须被赋予一个名称，并且可以可选地接受一个或多个参数。参数包含在括号中，并用逗号分隔。

```
function name(parameter1, parameter2, ..., parameterN) {
    statements;
}
```

这是 JavaScript 1.5 定义函数的格式。JavaScript 2.0 通过允许参数具有数据类型、函数本身具有数据类型、参数可选、命名参数等，对这种基本格式进行了强大的扩展。我们将在本章后面介绍 JavaScript 2.0 的函数。

函数定义中指定的参数在函数内部被视为变量。参数名称必须是唯一的，即同一函数的两个参数不能有相同的名称。

从基本函数语法出发，我们可以定义一个基本函数：

```
function add_two(x, y) {
    if (x > 7) {
        x = x - 7;
    } else {
        x = x + 7;
    }
    if (y > 18) {
        y = y - 18;
    } else {
        y = y + 18;
    }
    return x + y;
}
```

上述代码创建了一个名为 add_two() 的函数。该函数接受两个参数，分别命名为 x 和 y。函数的名称及其接受的参数在第一行代码中定义：

```
function add_two(x, y) {
```

函数的代码定义了一种相当复杂的加法方式。首先，检查 x 和 y 的内容，并根据它们的值从每个数中增加或减少某些值。

```
if (x > 7) {
    x = x - 7;
} else {
    x = x + 7;
}
if (y > 18) {
    y = y - 18;
} else {
    y = y + 18;
}
```

然后将两个数字相加并返回结果。通过添加 **return** 语句来返回结果，这个函数可以作为表达式使用，因为它返回了一个值。

```
return x + y;
```

现在这段代码只是定义了一个函数。如果将它添加到我们的 HTML 模板中并尝试在 Web 浏览器中执行，它实际上不会执行任何操作。函数需要被调用才能运行。而且如果函数定义了一个或多个参数，还必须为这些参数提供值。要调用函数，你必须执行以下操作：

1. 输入函数名，后跟一个左括号：
   `add_two(`

2. 如果需要，提供参数列表，用逗号分隔：
   `add_two(12, 2`

3. 后跟一个右括号和一个分号：
   `add_two(12, 2);`

4. 当然，对于我们的函数，我们需要将其返回值赋给一个变量，或在使用值的上下文中使用它：
   `var result = add_two(12, 2);`

我们可以将函数定义、HTML 模板和一些使用各种参数调用函数的代码组合如下：

```
<html>
    <head>
        <title>JavaScript sample code</title>
    </head>
    <body>
        <h1>Defining JavaScript Functions</h1>
        <script language="JavaScript" type="text/javascript">
<!-- // Begin
function add_two(x, y) {
    if (x > 7) {
        x = x - 7;
    } else {
        x = x + 7;
    }
    if (y > 18) {
        y = y - 18;
    } else {
        y = y + 18;
    }
    return x + y;
}

document.write("add_two(2, 17) = " + add_two(2, 17) + "<BR>");
document.write("add_two(14, 9) = " + add_two(14, 9) + "<BR>");
document.write("add_two(100, 200) = " + add_two(100, 200) + "<BR>");
// End -->
</script>
</body>
</html>
```

在这段代码中，我们将 add_two() 函数定义插入了 HTML 模板的 `<script>` 部分。要使该函数内部的代码被执行，我们需要调用该函数。在我们的代码中，我们调用了三次函数，使用了三组不同的参数。

当我们在浏览器中加载这段代码时，我们会看到类似于图 2-4 的结果。由于我们在 `document.write()` 函数调用内部调用函数，函数的输出被写入屏幕。这也是函数如何作为参数传递给其他函数的一个好例子——add_two 的值必须先被执行，才能得出传递给 `document.write` 的值。

#### 接受参数

当然，函数也可以不带任何参数来定义。

```
function print_header() {
```

定义和调用此类函数时，仍然需要括号。

```
print_header();
```

图 2-4 定义函数并重复调用它

使用函数时的另一个重要考虑因素是变量甚至参数的处理方式。考虑以下 JavaScript 代码：

```
var counter;
counter = 5;
function add2(input) {
    input = input + 2;
    document.write("input = " + input + "<br>");
    return;
}
add2(counter);
document.write("counter = " + counter + "<br>");
```

在该程序结束时，什么值会被写入屏幕？我们首先定义了一个名为 counter 的变量，并将其赋值为 5。然后我们定义了一个名为 add2() 的函数

该函数看似会将值 2 加到传入的参数上。然后我们使用计数器变量调用此函数，并将其值打印到屏幕上。结果是，程序结束时 `counter` 的值仍然是 5。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_75_0.png)

为什么呢？这与函数内部参数的处理方式有关。JavaScript 并不会将实际的 `counter` 变量传入 `add2()` 函数。它实际上是创建了 `counter` 的一个*副本*，并将该副本传入 `add2()`。因此，当函数退出时，`add2()` 对参数所做的任何更改都会丢失。

> 注意：*JavaScript 按值传递参数，这意味着任何参数的值在函数内部都无法被永久修改。*

#### 理解变量作用域

关于函数的另一个重要规则是变量作用域。在编程中，变量何时何地可以被使用，取决于你定义它的位置。如果你在函数内部声明一个变量，它只能在该函数内部使用。当你退出该函数时，该变量就不再被定义，其值也会丢失。

```
// get_factors() 返回能整除参数的所有数字
function get_factors(inputValue) {
    var counter;
    var factorString = "";
    for (counter = 1; counter <= inputValue; counter++) {
        if ((inputValue % counter) == 0) {
            factorString = factorString + counter + " ";
        }
    }
}
get_factors(6777214);
document.write (factorString);
```

例如，在这段代码中，定义了一个名为 `get_factors()` 的函数。然后我们使用值 6,777,214 作为参数来调用它。我们希望使用 `document.write()` 打印出结果字符串，但为时已晚。`factorString` 变量仅在函数内部有效，因为这是它的作用域。当我们尝试运行此程序时，会显示一条指向程序最后一行的错误消息。变量 `factorString` 不能在其定义的函数外部使用。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_76_0.png)

如果我们将 `document.write()` 语句移到函数调用内部，就会看到正确的结果。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_77_0.png)

#### 返回值

在函数内部，**return** 语句有两个作用：

- 使函数退出。
- 可选地将一个值返回给调用它的代码行。

就像 **break** 语句使循环退出一样，**return** 语句也会使函数退出。由于函数可以通过向调用它的代码返回值来充当表达式，因此 **return** 语句可以接受一个可选参数作为返回的值。

- return;
- return "Hello";
- return 32;
- return true;

以上四种都是在函数内部使用 **return** 语句的有效方式。

#### 使用 JavaScript 2.0 的改进功能创建更强大的函数

![](img/f14dd58a324d5464a114c30c1d4c4c9b_78_0.png)

JavaScript 2.0 为该语言带来了许多改进。欧洲计算机制造商协会（ECMA）添加了许多增强功能和灵活性的特性：

- 类
- 包
- 命名空间
- 数据类型
- 更强大灵活的数据数组
- 访问控制，如 public 和 private

有了这些新增功能，JavaScript 现在可以用于以前需要像 C++ 或 Java 这样更复杂语言才能完成的任务，同时仍然保留了多年来让 JavaScript 深受 Web 开发者喜爱的简洁性。

如果你以前使用过 JavaScript，你会发现的第一个变化是语言中增加了数据类型。数据类型允许你限制变量可以包含的值的范围或函数可以返回的值的范围。我们可以使用 JavaScript 2.0 语法修改本章前面定义的 `add_two()` 函数，为其所有变量、参数和函数本身添加数据类型：

```
function add_two(x : Number, y : Number) : Number {
    if (x > 7) {
        x = x - 7;
    } else {
        x = x + 7;
    }
    if (y > 18) {
        y = y - 18;
    } else {
        y = y + 18;
    }
    return x + y;
}
```

现在我们为 `x` 和 `y` 参数添加了 Number 数据类型，如果传入非数字类型的值，JavaScript 将报告错误。这也能让其他开发者更清楚地了解每个参数期望的数据类型。

##### 使用命名可选参数

JavaScript 2.0 中参数使用方式的另一个变化是能够定义命名可选参数。**named** 关键字允许我们在定义函数参数列表时将某些参数标识为可选的。

例如，假设我们有一个函数，需要接收一个人的名字，分为三个部分传入：

```
function sayHello
    (first : String,
    initial : String,
    last : String) : String {

    var fullname;
    if (initial <> "") {
        initial = initial + ". ";
    }
    fullname = first + " " + initial + last;
    return fullname;

}
```

如果使用前面的语法定义，我们别无选择，只能以如下方式调用：

```
sayHello ("Scott", "", "Duffy");
```

但通过在中间名首字母参数上使用 **named** 修饰符，我们可以允许函数在不传入中间名首字母的情况下被调用。

```
function sayHello
    (first : String,
    last : String,
    named initial : String = "") : String {
    var fullname : String;
    if (initial <> "") {
        initial = initial + ". ";
    }
    fullname = first + " " + initial + last;
    return fullname;
}
document.write (sayHello ("Scott", "Duffy") + "<br>");
document.write (sayHello ("Bobby", "Jones", initial:"H") + "<br>");
```

通过将中间名首字母参数定义为命名参数，我们就可以只指定名字和姓氏来调用 `sayHello()` 函数。命名参数必须始终指定一个初始值，以便在未指定该参数的值时可以分配一个默认值。如果你想为命名参数提供值，必须通过名称来引用该参数。

##### 接受任意数量的参数

JavaScript 2.0 中的函数可以定义为接受无限数量的参数。当你的函数需要接受大量相同类型的参数，但又不想创建大量命名可选参数时，就可以使用这种方式。

剩余参数必须始终出现在已定义的任何未命名参数的末尾，使用三个句点（...）表示。使用 **named** 关键字定义的命名参数仍然可以列在剩余参数之后。当然，一个函数只能有一个剩余参数。

以下代码定义了一个可以接受无限数量参数的函数。传入的前四个参数将被分配给前四个定义的参数：`name`、`address`、`phoneNum` 和 `spouseName`。超出这四个参数之外的任何参数都将被分配给一个名为 `childName` 的数组。我们可以使用 **for-in** 循环从该变量中获取名字列表。（我们将在第 4 章深入探讨数组。）

```
function printform (name : String,
    address : String,
    phoneNum : String,
    spouseName : String,
    ... childName : Array) {

    // 可以提供无限数量的子节点
    with (document) {
        write ("Name: " + name + "<br>");
        write ("Spouse: " + spouseName + "<br>");
        write ("Address: " + address + "<br>");
        write ("Phone: " + phoneNum + "<br>");
        for (child in childName) {
            write ("Child " + childName[child] + "<br>");
        }
    }
    return;
}
```

在下一章中，我们将重点介绍 JavaScript 一些最强大的特性——其内置对象和函数。

## 第 3 章

## 使用内置 JavaScript 类

![](img/f14dd58a324d5464a114c30c1d4c4c9b_82_0.png)

#### 如何……

- 掌握 JavaScript 中的对象
- 理解 JavaScript 的内置类与数据类型
- 在 JavaScript 中创建 String 对象
- 执行数学运算
- 运用 JavaScript 的日期处理函数
- 将字符串转换为数字
- 在发送到 Web 服务器之前准备文本
- 决定何时使用正则表达式
- 使用 JavaScript 2.0 强大的新数据类型
- 决定何时使用 JavaScript 2.0 的特殊数据类型

JavaScript 始终包含许多内置类，程序员在开发程序时可以使用它们。这些类——自包含的数据和代码——为处理日期、数学函数和数组提供了有用的功能。例如，如果你想在 JavaScript 中获取当前日期和时间，你会创建一个 Date 类的实例，如下所示：

```
var today = new Date();
```

这段代码中的 today 变量实际上是一个对象。today 对象不仅包含一个值（实际上是今天的日期），而且还包含许多内置函数，用于检索和设置日期的各个部分，并将其转换为多种不同的格式（例如字符串）。"运用 JavaScript 的日期处理函数"一节将在本章稍后探讨 Date 类及其所有功能。

JavaScript 1.5 包含九个这样的类，但只有三个在常见实践中使用（Array、Date 和 Math）。JavaScript 2.0 已将列表扩展到超过 18 个类，而且几乎所有类都很有用。在本章中，我们将研究其中大部分类，并学习如何在 JavaScript 程序中应用它们。

#### 学习 JavaScript 中的对象

我们正接近 Fortran 开发五十周年，它是第一种高级编程语言，于 1956 年开发出来。自那时起，计算机科学家们已经发展出多种编程方法论。表 3-1 列出了设计程序最常见的方法。

重要的是要记住，没有哪种方法论是完美的。在 JavaScript 编程中，你很可能会根据手头的任务使用表 3-1 中列出的任何一种或全部四种方法论。

| 方法论 | 描述 |
| --- | --- |
| 非结构化 | 作用于全局数据的语句序列 |
| 过程式 | 调用函数来执行特定任务的主程序 |
| 模块化 | 使用模块来分组相关功能的主程序 |
| 面向对象 | 使用对象来分组相关数据和功能的主程序 |

**表 3-1** 常见编程方法论

##### 编写非结构化程序

非结构化编程通常最适合用于简短、简单的脚本，因为它们无法从众多函数和对象中获益。非结构化程序只是一组不使用用户定义函数或对象的 JavaScript 语句。

以下是在 HTML 网页上下文中的非结构化程序示例。请注意，该程序中只有三行 JavaScript 代码。

```
<html>
    <head>
        <title>JavaScript sample code</title>
    </head>
    <body>
        <h1>Unstructured Program</h1>
        <script language="JavaScript" type="text/javascript">
        <!-- // Begin
        for (var counter = 1; counter < 101; counter++) {
            document.write ("This is line number " + counter + "<br>\n");
        }
        // End -->
        </script>
    </body>
</html>
```

##### 将代码组织为过程

过程式代码在 JavaScript 编程中也很常见。我们可以轻松地使用过程式方法重写前面程序中的非结构化代码。

```
function printline(value) {
    document.write ("This is line number " + value + "<br>\n");
}

for (var counter = 1; counter < 101; counter++) {
    printline(counter);
}
```

该程序创建了一个名为 printline() 的函数，其唯一职责是向屏幕写入包含传递给它的参数值的文本。在程序后面，我们可以反复调用该函数。

这种编程实践的好处是双重的：

- 同一函数可以从程序中的多个位置调用，从而消除了非结构化方法中的代码重复。
- 将程序划分为函数使其更易于测试，通常能减少错误。

###### 将程序划分为模块

如果程序变得足够大（在规模和范围方面），管理和维护会越来越困难。程序员需要一种额外的技术（除了使用过程和函数）来将他们的程序划分为更小、更易于管理的部分。从过程式方法向前的下一个合乎逻辑的步骤就是模块化方法。

模块化编程通常涉及将一个大程序分成两个或多个独立的文件。这些文件，或者说*模块*，不一定自包含，但它们确实将相关代码和函数分组在一起。通常，模块化程序由一个主程序和一个或多个模块组成，例如：

- 主程序
- 数据库模块
- 用户界面模块
- 错误处理模块

我们可以从前面的模块配置推断，主程序承担了大部分工作，但在需要与数据库通信时，它会调用数据库模块中存在的函数。同样，它根据需要利用用户界面和错误处理模块来完成各自的任务。与一个大型的单一模块相比，这种划分为模块的程序类型让程序员更容易管理。

要使用 JavaScript 创建模块化程序，你需要创建一个或多个 JavaScript 文件。当你使用 `<script>` 标签的属性将这些外部代码文件导入 HTML 页面时，你的主程序就可以访问那些外部模块中定义的所有函数。我们将在第 6 章中了解更多关于创建和导入 JavaScript 文件的内容。

###### 使用面向对象方法

从模块化编程向前的下一个发展就是面向对象编程。对象的概念起初可能有点令人望而生畏，但这不应该阻止任何人尝试至少理解使用对象如何让程序员的工作变得更加轻松。

在编程中，对象只不过是一个"事物"，它拥有自己的属性（称为*属性*）和相关函数（称为*方法*）。你可以像思考现实生活中的对象一样来思考编程中的对象。让我给你举个例子。

我的车是一个具有某些属性并能执行某些动作的对象。我的车的独特属性使它与路上的大多数其他车区别开来。即使我遇到另一辆与自己相同品牌和型号的车辆，它们仍然是不同的车辆。以下是我的车的一些常见属性列表：

| 属性 | 值 |
|----------|-------|
| 年份 | 2001 |
| 品牌 | Toyota |
| 型号 | 4Runner SR5 |
| 轮胎 | 4 |
| 车门 | 4 |
| 颜色 | Thundercloud |
| 速度计（mph） | 范围从 0 到 70 |
| 油量计（体积，加仑） | 范围从 0.0 到 16.0 |
| 等等 | |

我刚才列出的实际上就是将要放入我的 Car 对象中的编程变量。事实上，前五个属性（Year、Make、Model、Tires 和 Doors）是永久性的——用编程术语来说，它们是*常量*。其余的属性可以更改，因此它们是变量。记住，我们在第 2 章中考察了常量和变量。如果我要将与我的车相关的属性列表转换为 JavaScript 2.0 代码，它看起来大致如下。

```
const Year : Integer;
const Make : String;
const Model: String;
const Tires : Integer;
const Doors : Integer;
var Color : String;
var CurrentSpeed : Number;
var CurrentGas : Number;
```

除了具有多个属性之外，我的车还具有它能执行的几种动作：

| 如果我这样做…… | 车会这样做…… |
|-----------------|----------------------|
| 踩油门踏板 | 增加速度；增加燃油消耗 |
| 踩刹车踏板 | 降低速度；减少燃油消耗 |



如果我这样做…… | 汽车就会这样做…… |
| :--- | :--- |
| 向右或向左转动方向盘 | 让前轮向右或向左转 |
| 按下方向盘中央 | 鸣笛 |
| 往油箱里加油 | 增加汽油量 |

同样，从程序员的角度来看，这些都是汽车的函数。许多函数都与汽车的属性相关。例如，油门踏板和刹车踏板都会影响汽车的速度和油耗。

如果我的汽车是一个可编程对象，它将具有如下的 JavaScript 2.0 函数定义。

```
function depressGasPedal (howMuch : Integer) {}
function depressBrakePedal (howMuch : Integer) {}
function turnSteeringWheel (degrees : Integer) {}
function beepHorn () {}
function addGas (volume : Number) {}
```

##### 将属性和函数转化为类

仅仅定义汽车收集到的常量、变量和函数并不能使其成为对象。在一段代码集合能够成为对象之前，它首先必须成为一个类。

类是变量和函数的独立分组。类的变量和函数，也称为其*成员*，不能用于存储数据或执行操作。类仅仅是从其中创建对象的蓝图。在我们的计算机程序中将只有一个 Car 类，但可能会有多个 Car 对象。如果我们选择不创建任何对象，也可能没有 Car 对象。

> 提示：类不能存储数据或执行操作这一规则有一个例外。如果某个类成员被定义为*静态*（*static*），则它可以在不存在对象的情况下使用。静态类成员将在第 5 章中更详细地讨论。

我们将在第 5 章中研究用户自定义的类。在 JavaScript 1 和 JavaScript 2 中创建此类定义有不同的语法，理解其中的区别很重要。在不涉及更多细节的情况下，这是我们的 Car 类在 JavaScript 2.0 语法中的样子。

```
class Car {
    const Year : Integer;
    const Make : String;
    const Model: String;
    const Tires : Integer;
    const Doors : Integer;
    var Color : String;
    var CurrentSpeed : Number;
    var CurrentGas : Number;

    function depressGasPedal (howMuch : Integer) {
        // Gas pedal JavaScript code
    }
    function depressBrakePedal (howMuch : Integer) {
        // Brake pedal JavaScript code
    }
    function turnSteeringWheel (degrees : Integer) {
        // Steering wheel JavaScript code
    }
    function beepHorn () {
        // Horn JavaScript code
    }
    function addGas (volume : Number) {
        // Gas tank JavaScript code
    }
}
```

我们可以通过使用 Car 类名称调用 **new** 运算符来创建 Car 对象。我们将在本章后面的"使用 **new** 运算符实例化对象"一节中更详细地研究 **new** 运算符。

```
var myAuto = new Car();
myAuto.Year = 2001;
myAuto.Make = "Toyota";
// etc.
```

最后，JavaScript 2.0 中的类也会自动定义为数据类型，因此可以定义只能包含指定对象的变量。

```
var Ferrari : Car = new Car();
```

#### JavaScript 的内置类和数据类型

尽管该语言的早期版本缺乏真正的数据类型，但 JavaScript 一直具有类的概念。开发人员可以使用许多内置类，这些类提供了用于处理某些类型数据的有用方法和函数。

表 3-2 列出了 JavaScript 1.5 中存在的类，以及每个类提供的功能的简要说明。

JavaScript 2.0 最显著的改进是，该语言已经发展到比以前更加面向对象。JavaScript 1.5 是基于对象的，但不符合面向对象编程语言的几个关键属性。JavaScript 2.0 符合大多数关键属性。

表 3-3 列出了 JavaScript 2.0 支持的类。该列表显然比表 3-2 中的要长得多。

| Class Name | Description |
|---|---|
| Array | Allows lists of data to be stored in a single variable |
| Boolean | A wrapper for Boolean values |
| Date | Lets you work with dates and times |
| Function | Allows you to define a function programmatically |
| Math | Contains convenient mathematical constants and functions |
| Number | A wrapper for primitive numeric values |
| Object | All objects derive from this data type |
| RegExp | Provides support for regular expressions in JavaScript |
| String | A wrapper for string values |

**表 3-2 预定义的核心 JavaScript 1.5 类**

| Class Name | Description |
|---|---|
| Array | Allows lists of data of type Object to be stored in a single variable; is equivalent to the Array[Object] data type |
| Array[type] | Allows lists of data of type *type* to be stored in a single variable |
| Boolean | Supports variables that can only store true and false |
| char | Supports variables that can only store a single character |
| ConstArray | Allows lists of data of type Object to be stored in a single constant; is equivalent to the ConstArray[Object] data type |
| ConstArray[type] | Allows lists of data of type *type* to be stored in a single constant |
| DynamicArray[type] | Allows resizable lists of data of type *type* to be stored in a single variable |
| Function | The "data type" of functions |
| Integer | Supports variables that can only store integers |
| Never | Supports variables that cannot contain any value |
| Null | Supports variables that can only store "null" |
| Number | Supports variables that can only store numbers |
| Object | Supports variables that can contain any value |
| Prototype | Supports variables that contain prototype-based objects (JavaScript 1.5's way of handling objects) |
| StaticArray[type] | Allows writable lists of data of type *type* to be stored in a single variable |
| String | Supports variables that can only store strings |
| Type | The "data type" of data types |
| Void | Supports variables that can only store "undefined" |

**表 3-3 JavaScript 2.0 中的预定义数据类型**

> 注意：JavaScript 2.0 中的所有类，甚至你自己创建的类，都可以用作数据类型。因此，表 3-3 中的类列表也是数据类型的部分列表。

除了表 3-3 中列出的可用作数据类型的预定义类之外，JavaScript 2.0 中还有若干*机器类型*。这些机器类型（列于表 3-4 中）是可在 JavaScript 中使用的低级数据类型，尽管并非所有 JavaScript 环境都支持它们。它们是为了与其他语言兼容而提供的——例如，当你的 JavaScript 程序需要与外部 C 语言应用程序交换数据时。

> 注意：NaN（Not a Number）是 JavaScript 中定义的常量，实际上是一个数字，表示在处理该变量时发生了错误。

机器类型可以像从类派生的数据类型一样使用，尽管它们本身不是类。例如，在下面的 JavaScript 2.0 代码列表中，我们创建了几个定义为机器类型的变量。

```
var counter : short = 14;
var account_balance : int = 1701330222;
var bigNumber : long = 74440000000000;
var anotherBigNumber = 312L;
```

> 快捷方式：表 3-4 中列出的机器类型后缀是为值分配机器类型的便捷简写符号。三个后缀——L、UL 和 F——向 JavaScript 表明你希望将数字视为 long、unsigned long（ulong）或 float 数字。因此表达式 "0L" 告诉 JavaScript 由于 L 机器类型后缀而将值 0 视为 long。

在前面的代码中，变量 anotherBigNumber 将被视为长整型，因为我们正在将值 312L 分配给它。L 后缀强制将值 312 视为长整型。这仅在将数字字面量分配给变量时有效，对于变量等其他类型的表达式不起作用。



JavaScript 无所不能——从入门到精通

| 类型 | 后缀 | 取值范围 |
| :--- | :--- | :--- |
| sbyte | | –128 到 +127 之间的整数 |
| byte | | 0 到 +255 之间的整数 |
| short | | –32768 到 +32767 之间的整数 |
| ushort | | 0 到 +65535 之间的整数 |
| int | | 大约 –21 亿到 +21 亿之间的整数 |
| uint | | 大约 0 到 +43 亿之间的整数 |
| long | L | 大约 –9 秭到 +9 秭（9 后面跟着 18 个零）之间的整数 |
| ulong | UL | 大约 0 到 +18 秭（18 后面跟着 18 个零）之间的整数 |
| float | F | 单精度浮点数，包括正零和负零、无穷大以及 NaN |

**表 3-4** JavaScript 2.0 中定义的机器类型

#### 使用 new 运算符实例化对象

无论是从用户定义的类还是系统定义的类创建对象，其基本流程都是相同的。JavaScript 为此提供了一个特殊的运算符**new**，也称为*对象实例化*。

```
var myAuto = new Car();
```

当**new**运算符以现有类的名称（本例中为 Car）被调用时，它会调用类的构造函数并返回该对象的实例。通过将该对象实例赋值给变量 myAuto，我们保留了该对象的引用，以便在程序中使用。

*构造函数*是某些类中定义的一种特殊函数，用于使对象准备好使用。初始化代码放在构造函数中。类可以有多个构造函数，也可以没有。我们将在第 5 章中介绍如何创建自己的类以及这些类的构造函数。

**new**运算符中包含的任何参数也会都会作为参数传递给构造函数。如果我们在 Car 类中定义了一个构造函数，我们可能希望允许用户传入大部分相关属性（品牌、型号、年份等）作为参数，这样构造函数就能使对象完全准备好使用。否则，我们将得到一个没有任何预定义属性的 Car 对象，程序将不得不手动设置每个相关属性。

```
var myAuto = new Car (2001, "Toyota", "4Runner SR5", "Thundercloud");
```

这种使用构造函数进行Dy进行对象初始化的技术是一种推荐的编程技术。

##### 使用 . 运算符访问对象

一旦使用**new**运算符创建了对象，我们就可以使用*点运算符*（.）来访问其所有公共属性和方法。点运算符放在对象名称（不是类名称）和要访问的属性或方法名称之间。

```
document.write ("Your car was created in " + myAuto.Year);
```

在此代码示例中，我们实际上使用了两次点运算符。我们用它来访问内置 document 对象的 write() 方法，也用它来访问用户定义的 myAuto 对象的 Year 属性，该对象是 Car 类的一个实例。

> *你可以将属性和方法定义为私有的，这将限制使用点运算符访问它们的能力。我们将在第 5 章中介绍私有属性和方法。*

##### 使用 [] 运算符访问对象

JavaScript 还允许使用*方括号运算符*（[]）来访问对象的属性。该运算符相对于点运算符的一个优势是，你不需要知道要查找的属性的名称。例如，让我们看一下以下**for-in**循环。

```
for (var tool in toolchest) {
    document.write(toolchest[tool] + "<BR>");
}
```

在此代码示例中，我们将名为 tool 的变量传递给方括号运算符，然后它能够从 toolchest 对象中提取属性的值。JavaScript 2.0 中定义的任何类的公共属性都可以使用方括号运算符访问。这甚至适用于 JavaScript 1.5 版本的内置 DOM 对象。

```
for (var prop in document) {
    document.write
        ("document." + prop + " = " + document[prop] + "<BR>");
}
```

这段代码的结果是 DOM document 对象的全部内容都被写入到 Web 浏览器窗口中，如图 3-1 所示。由于不同浏览器制造商之间，甚至同一浏览器的不同版本之间的 DOM 略有不同，你自己的测试可能会显示不同的属性和值。

#### 在 JavaScript 中创建字符串对象

*字符串*就是零个或多个 Unicode 字符的序列。以下都是有效的字符串：

- ""（空字符串）
- "How was work today, Sofia?"
- "32"（数字字符）
- "Êtes-vous prêt pour l'examen?"（非英语字符）

在 JavaScript 中创建字符串有两种方法：

- 字符串字面量
- 使用 String 对象

绝大多数字符串都是使用字符串字面量创建的，因为它是最快、最简单的技术。

##### 使用字符串字面量创建字符串对象

JavaScript 中的字符串字面量就是零个或多个字符的序列，用单引号或双引号括起来，如下所示：

```
var myString = "This is a string literal";
var myOtherString = 'So is this, using single quotation marks.';
```

![](img/f14dd58a324d5464a114c30c1d4c4c9b_93_0.png)

**图 3-1** Internet Explorer 6.0 中 document 对象的内容

> 注意
> 
> 字符串字面量可用于任何版本的 JavaScript。

在 JavaScript 2.0 中，你甚至可以将变量赋值为 String 数据类型，同时使用字符串字面量来创建对象。

```
var title : String = "How To Do Everything with Paper Clips";
```

重要的是要记住，使用字符串字面量创建 String 对象仍然允许你使用对象提供的所有属性和方法。

```
var myString = "This is a string literal";
var myOtherString = 'So is this, using single quotation marks.';
document.write ("\"" + myString + "\" = " + myString.length + " characters<br>");
document.write ("'" + myOtherString + "' = " + myOtherString.length + " characters<br>");
```

length 是 String 对象的一个属性。访问 length 属性会得到字符串的实际长度，如下面的浏览器输出所示。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_94_0.png)

##### 使用 String 数据类型创建字符串对象

JavaScript 1.1 引入了使用 String 类构造函数创建字符串的功能。

```
var hometown = new String("Chicago");
```

通过将要创建的字符串文本传递给构造函数，我们最终使 hometown 变量成为一个 String。这样做几乎没有优势，而且你也很少会看到这样的用法。

##### 使用 String 对象的内置功能

String 对象被赋予了许多预定义的函数，使你可以对它们进行各种操作。表 3-5 列出了最常见的 String 方法。

> 注意
> 
> 表 3-5 中列出的四个方法使用正则表达式模式。我们将在本章后面的"了解正则表达式基础"部分中介绍正则表达式。

| 方法 | 用途 |
| :--- | :--- |
| charAt(index) | 返回字符串中的一个字符 |
| charCodeAt(index) | 返回字符串中一个字符的 ASCII 码 |
| concat(string) | 将两个字符串连接在一起 |
| indexOf(string, index) | 查找一个字符串在另一个字符串中的首次出现位置 |
| lastIndexOf(string, index) | 查找一个字符串在另一个字符串中的最后一次出现位置 |
| match(regexp) | 在字符串中搜索正则表达式模式，并返回任何匹配项 |
| replace(regexp, newString) | 在字符串中搜索正则表达式模式，并将任何匹配项替换为提供的字符串 |
| search(regexp) | 在字符串中搜索正则表达式模式，并返回首次匹配的索引 |
| split(separator, limit) | 根据分隔符字符或正则表达式，将单个字符串拆分为子字符串数组 |
| substring(start, end) | 返回字符串的一部分 |
| toLowerCase() | 将字符串作为小写字符返回 |
| toString() | 与 valueOf() 相同；返回字符串 |
| toUpperCase() | 将字符串作为大写字符返回 |
| valueOf() | 返回字符串 |

**表 3-5** 常见的 String 对象方法



表3-5中列出的每种方法都可以通过点运算符从任何String对象进行访问。

```javascript
var msg = "ERROR: Invalid User ID or Password<br>";
document.write( "<b>Original message:</b> " +
    msg.valueOf() );
document.write( "<b>Upper case:</b> " +
    msg.toUpperCase() );
document.write( "<b>Lower case:</b> " +
    msg.toLowerCase() );
document.write( "<b>Partial string:</b> " +
    msg.substring(20, 22) + "<br>" );
document.write( "<b>Single character:</b> " +
    msg.charAt(17) + "<br>" );
document.write( "<b>Search from beginning:</b> " +
    msg.toLowerCase().indexOf("sword") + "<br>" );
document.write( "<b>Search from end:</b> " +
    msg.lastIndexOf("User ID") + "<br>" );
```

从以下截图中可以看出，所有String属性都可以应用于msg对象，因为msg是String类型。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_96_0.png)

> 提示：一个表达式中可以出现多个点运算符。以表达式"msg.toLowerCase()"为例——该表达式将返回全小写字符的msg字符串。你可以将另一个String方法应用于此表达式，例如"msg.toLowerCase().indexOf(\"sword\")"。由于indexOf()方法返回一个整数，你可以添加第三个点运算符来执行Integer对象的某个方法。

#### 执行数学函数

JavaScript提供了一个实际上不能用于创建对象的内置类——Math。Math类的目的是提供各种数学函数和常量。由于Math类的所有成员都定义为静态的，你可以直接使用Math对象调用它们。尝试基于Math类创建对象会在JavaScript中导致错误。你使用点运算符调用Math的静态成员，就像调用任何其他类的实例成员一样。表3-6列出了Math类提供的所有预定义常量的名称。Math类还提供了许多对执行复杂数学计算有用的方法，如表3-7所示。例如，如果我们想创建一些JavaScript代码来利用Math对象提供的数学常量和函数，我们可以这样做：

```javascript
// 一个12英寸圆的面积，(PI * r^2)
var area = Math.PI * Math.pow(12/2, 2);
```

```javascript
// 直角三角形长边的长度
//      假设，底边5英寸，高7英寸，(a^2 + b^2 = c^2)
var longside = Math.sqrt( Math.pow(5,2) + Math.pow(7,2) );
```

> 你知道吗？实例成员与静态成员
>
> 默认情况下，类的属性和方法将定义为*实例成员*。这意味着它们只能在基于该类的对象实例内访问。这些对象使用**new**关键字创建，并为每个新创建的对象创建类实例成员的新副本。如果你基于一个类创建100个对象，你就拥有了每个方法和变量的100个独立副本。更改其中一个副本的值不会影响其他副本。
>
> 类的属性和方法可以选择性地定义为*静态成员*。静态成员只能直接从类访问，不是基于该类创建的实例的一部分。本质上，静态类成员是全局的，因为无论创建了多少个对象，该成员的版本始终只有一个。

| 常量 | 用途 |
| :--- | :--- |
| E | 欧拉常数，2.7183 |
| LOG2E | E的以2为底的对数 |
| LOG10E | E的以10为底的对数 |
| LN2 | 2的自然对数 |
| LN10 | 10的自然对数 |
| PI | 圆周率，3.1416 |
| SQRT2 | 2的平方根 |
| SQRT1_2 | 二分之一（0.5）的平方根 |

**表3-6** Math类提供的静态常量列表

#### 应用JavaScript的日期处理函数

我们已经在本章开头简要了解了Date类，但值得再次更详细地看看它。Date类允许你创建包含任何指定日期的Date对象，或者如果不指定日期，则包含今天的日期。使用Date对象，你可以：

- 检索日期的特定部分（例如月份）
- 更改或修改日期的部分内容
- 在不同字符串格式之间转换日期
- 在不同时区之间转换日期

| 方法 | 用途 |
| :--- | :--- |
| abs (x) | x的绝对值 |
| acos (x), asin (x), atan (x), atan2 (y, x), cos (x), sin (x), tan (x) | 三角函数 |
| ceil (x) | 返回大于x的下一个最大整数（如果x是整数，则返回x） |
| exp (x) | 返回常数E的x次幂 |
| floor (x) | 返回小于x的下一个整数（如果x是整数，则返回x） |
| log (x) | 返回x的自然对数 |
| max (x, y) | 返回x或y中的较大者 |
| min (x, y) | 返回x或y中的较小者 |
| pow (x, y) | 返回x的y次幂 |

**表3-7** Math对象的静态方法

| 方法 | 用途 |
| --- | --- |
| random () | 返回0到1之间的伪随机数 |
| round (x) | 将x四舍五入到最接近的整数 |
| sqrt (x) | 返回x的平方根 |

**表3-7** Math对象的静态方法（续）

> 提示：JavaScript的早期版本限制了Date对象，使其无法处理1970年1月1日之前的日期。这在该语言的1.3版本中得到了修正。现在日期范围可以在1970年1月1日的前后各1亿天内，大约相当于过去和未来27万年。

JavaScript中没有日期字面量，因此Date对象只能从Date类创建。Date类的构造函数接受多种不同的输入参数。

```javascript
var holiday = new Date("July 4, 2010");
var newyears = new Date(2010, 12, 31);
var today = new Date();
var midnight = new Date(2010, 12, 31, 23, 59, 59, 999);
```

正如我们在代码中看到的，Date构造函数可以尝试解释作为字符串字面量编写的日期。你也可以将年、月、日作为整数传入。你甚至可以指定精确到毫秒的日期和时间。如果未提供参数，则默认将对象设置为今天的日期。

表3-8列出了Date对象支持的所有方法。使用这些方法，你可以提取日期的特定部分、更改日期或将其转换为不同的格式。

| 方法 | 用途 |
| --- | --- |
| getDate () | 根据本地时间返回月份中的日期（1–31） |
| getDay () | 根据本地时间返回星期几（1–7） |
| getFullYear () | 根据本地时间返回四位数的年份 |
| getHours () | 根据本地时间返回时间的小时部分 |
| getMilliseconds () | 根据本地时间返回时间的毫秒部分 |
| getMinutes () | 根据本地时间返回时间的分钟部分 |
| getMonth () | 根据本地时间返回月份（0–11）；0是1月，1是2月，依此类推 |
| getSeconds () | 根据本地时间返回时间的秒部分 |

**表3-8** Date对象的方法

| 方法 | 用途 |
|---|---|
| `getTime ()` | 返回对应时间的数值 |
| `getTimezoneOffset ()` | 返回当前时间与通用时间（格林威治标准时间）相差的小时数 |
| `getUTCDate ()` | 根据通用时间返回月份中的日期（1–31） |
| `getUTCDay ()` | 根据通用时间返回星期几（1–7） |
| `getUTCFullYear ()` | 根据通用时间返回四位数的年份 |
| `getUTCHours ()` | 根据通用时间返回时间的小时部分 |
| `getUTCMilliseconds ()` | 根据通用时间返回时间的毫秒部分 |
| `getUTCMinutes ()` | 根据通用时间返回时间的分钟部分 |
| `getUTCMonth ()` | 根据通用时间返回月份（0–11）；0是1月，1是2月，依此类推 |
| `getUTCSeconds ()` | 根据通用时间返回时间的秒部分 |
| `getYear ()` | 根据本地时间返回年份 |
| `parse (string)` | 解析日期字符串并返回自1970年1月1日以来的秒数 |
| `setDate ()` | 根据本地时间设置月份中的日期（1–31） |
| `setFullYear ()` | 根据本地时间设置四位数的年份 |
| `setHours ()` | 根据本地时间设置时间的小时部分 |
| `setMilliseconds ()` | 根据本地时间设置时间的毫秒部分 |
| `setMinutes ()` | 根据本地时间设置时间的分钟部分 |
| `setMonth ()` | 根据本地时间设置月份（0–11）；0是1月，1是2月，依此类推 |
| `setSeconds ()` | 根据本地时间设置时间的秒部分 |
| `setTime ()` | 设置对应时间的数值 |
| `setUTCDate ()` | 根据通用时间设置月份中的日期（1–31） |
| `setUTCFullYear ()` | 根据通用时间设置四位数的年份 |
| `setUTCHours ()` | 根据通用时间设置时间的小时部分 |
| `setUTCMilliseconds ()` | 根据通用时间设置时间的毫秒部分 |
| `setUTCMinutes ()` | 根据通用时间设置时间的分钟部分 |
| `setUTCMonth ()` | 根据通用时间设置月份（0–11）；0是1月，1是2月，依此类推 |
| `setUTCSeconds ()` | 根据通用时间设置时间的秒部分 |
| `setYear ()` | 根据本地时间设置年份 |
| `toDateString()` | 返回表示指定Date对象日期部分的字符串 |
| `toGMTString ()` | 使用Internet GMT约定将日期转换为字符串 |

**表3-8** Date对象的方法（续）



 | 方法 | 用途 |
|---|---|
| toLocaleDateString() | 使用当前地区的约定，将日期的日期部分转换为字符串 |
| toLocaleString() | 使用当前地区的约定，将日期转换为字符串 |
| toLocaleTimeString() | 使用当前地区的约定，将日期的时间部分转换为字符串 |
| toString() | 返回表示指定 Date 对象的字符串 |
| toTimeString() | 返回表示指定 Date 对象时间部分的字符串 |
| toUTCString() | 使用通用时间约定，将日期转换为字符串 |
| UTC() | 返回自通用时间 1970 年 1 月 1 日 00:00:00 以来 Date 对象中的毫秒数 |
| valueOf() | 返回 Date 对象的原始值 |

**表 3-8** Date 对象的方法 *(续)*

Date 类的构造函数接受四种格式。对象所表示的实际日期取决于传递的参数数量和类型。

| 要基于...创建日期 | 使用这个... |
|---|---|
| 日期字符串 | new Date("January 1, 2008") |
| 日期组成部分 | new Date(2008, 0, 31) |
| 日期和时间组成部分 | new Date(2008, 0, 31, 12, 0, 0, 0) |
| 自 1970 年 1 月 1 日以来的毫秒数 | new Date(1034214221530) |
| 当前日期和时间 | new Date() |

> **注意** *JavaScript 期望使用 0 到 11 范围内的数字来表示一年中的月份。一月是第 0 个月，二月是第 1 个月，以此类推。*

#### 将字符串转换为数字

JavaScript 包含两种内置方法，可以将嵌入字符串中的数字（如 "32"）转换为可在数学方程中使用的实际数字（如 32）——`parseInt()` 和 `parseFloat()`。顾名思义，`parseInt` 函数将返回一个整数（不带小数部分的数字），而 `parseFloat` 将返回一个浮点数（包含任何小数部分）。

##### 使用 parseInt 和 parseFloat 函数

JavaScript 提供了 `parseInt` 和 `parseFloat` 来帮助你把字符串内部的数字转换成实际的数字数据类型。这在处理互联网网页时是一项重要技术，因为通过 URL 和表单读取的数据通常以字符串形式到达。它们的工作原理如下：

1. 首先定义一个变量来包含你的字符串。

```
var myString;
```

2. 将一个包含有效数字的字符串赋给该变量。这个数字不必是整数。

```
var myString;
myString = "3.14159265358979323846"; // 圆周率的值...
```

3. 定义一个变量来包含你的整数。

```
var myString, myInteger;
myString = "3.14159265358979323846"; // 圆周率的值...
```

4. 对该字符串调用 `parseInt()` 函数，并将值赋给整数变量。

```
var myString, myInteger;
myString = "3.14159265358979323846"; // 圆周率的值...
myInteger = parseInt(myString);
```

5. `parseInt()` 函数应该从这个例子中定义的字符串返回值 3。我们可以通过调用警告消息框来验证这一点。

```
var myString, myInteger;
myString = "3.14159265358979323846"; // 圆周率的值...
myInteger = parseInt(myString);
alert(myInteger);
```

![](img/f14dd58a324d5464a114c30c1d4c4c9b_102_0.png)

6. 如果 `myString` 不是一个有效的数字会怎样？让我们修改一下并找出答案。

```
var myString, myInteger;
myString = "Madrid, Spain"; // 圆周率的值...
myInteger = parseInt(myString);
alert(myInteger);
```

![](img/f14dd58a324d5464a114c30c1d4c4c9b_102_1.png)

# 84 如何用 JavaScript 做好每件事

`parseFloat()` 函数的工作方式与 `parseInt()` 类似，只是包含小数点后的数字。我们可以通过更改函数名来验证这一点。

```
var myString, myInteger;
myString = "3.14159265358979323846";  // 圆周率的值...
myInteger = parseFloat(myString);
alert(myInteger);
```

![](img/f14dd58a324d5464a114c30c1d4c4c9b_103_0.png)

#### 发送到 Web 服务器前预处理文本

互联网上的每个网页都有一个唯一的 URL（统一资源定位符）。即使是存储在你硬盘上的网页也有自己唯一的 URL。以下是一些 URL 示例：

| URL | URL 描述 |
|---|---|
| http://www.amazon.com/ | Amazon.com 的默认网页 |
| news:comp.infosystems.www.servers.unix | Usenet 新闻组 |
| file:///C:/temp/test.html | 位于用户硬盘上的文件 |

![](img/f14dd58a324d5464a114c30c1d4c4c9b_103_1.png)

##### 统一资源定位符（URL）的限制

URL 格式在 URL 字符串中仅接受以下字符：

- 字母——a 到 z
- 数字——0 到 9
- 标记——$-\_+!*'(),
- 为特殊用途保留的特殊字符——; / ? : @ = &

URL 中不能出现其他字符。而且特殊字符只能在其指定的角色中使用。落入这些规则之外的字符必须正确转义，如"使用 escape 和 unescape 函数"中所述。

想象一个文件名又长又富有创意，比如 We're #1 & proud of it; no ifs ands or buts!.htm。Windows 确实允许这样的文件名。但当通过浏览器访问这个文件时，我们就会遇到问题。空格、#、&、! 和 ; 字符在 URL 命名方案中是不允许的。为了访问该文件，它必须首先被转义，如以下章节所述。

##### 使用 escape 和 unescape 函数

转义文件是在将 URL 发送到服务器处理之前，将所有无效字符转换为特殊编码符号的过程。要转义文件名，我们必须使用 JavaScript 内置的 `escape` 函数。

1. 从一个内部包含一些无效字符的字符串开始。

```
var filename;
filename = "We're #1 & proud of it; no ifs ands or Constantinople 现在是伊斯坦布尔，这是非常长的一段文本，只是为了测试翻译是否会正常处理，不影响主要内容。.htm";
```

2. 定义一个变量来包含转义后的字符序列。

```
var filename, newFilename;
filename = "We're #1 & proud of it; no ifs ands or buts!.htm";
```

3. 将字符串上 `escape` 函数的结果赋给新变量。

```
var filename, newFilename;
filename = "We're #1 & proud of it; no ifs ands or buts!.htm";
newFilename = escape(filename);
```

4. 为了检查 `escape()` 函数的结果，我们应该使用警告框将其显示给用户。

```
var filename, newFilename;
filename = "We're #1 & proud of it; no ifs ands or buts!.htm";
newFilename = escape(filename);
alert(newFilename);
```

![](img/f14dd58a324d5464a114c30c1d4c4c9b_104_0.png)

#### 决定何时使用正则表达式

正则表达式是一种强大的搜索和替换技术，广泛用于其他环境（如 Unix 和 Perl），但在 JavaScript 中很少使用。也许如果更多程序员知道 JavaScript 中正则表达式的存在，它们的使用就会流行起来。

> 注意
>
> JavaScript 直到该语言的 1.4 版本才开始支持正则表达式，这意味着它们只能在 Netscape 4 或 Internet Explorer 4 网络浏览器或后续版本中使用。

*正则表达式*是使用特殊正则表达式语言编写的一系列字符，可用于匹配其他字符串中的模式。为了让你了解正则表达式模式匹配功能有多强大，我写了一个小小的 JavaScript 程序（主要使用 String 对象的 `substring()` 方法）来检查字符串是否匹配标准电话号码格式——(XXX) XXX-XXXX，其中 X 表示 0 到 9 之间的任何数字。那个程序包含了 69 行 JavaScript 代码，仅仅为了检查一个电话号码。

幸运的是，可以使用正则表达式重写该程序，如下所示：

```
var phonenum = "(415) 555-1212";
var pattern = /^\(\d{3}\) \d{3}-\d{4}$/;
document.write("Trying to match \"" + phonenum + "\" with pattern " +
    pattern.toString() + "...<br><br>");
if (pattern.test(phonenum)) {
    document.write("This is a valid phone number.");
} else {
    document.write("This is NOT a valid phone number.");
}
```

运行这段 JavaScript 会在浏览器窗口中产生以下输出。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_105_0.png)



如您所见，使用正则表达式来检查字符串是否匹配模式，可以节省大量时间和精力。我们将在下一节探讨这段代码的工作原理。

#### 理解正则表达式的基础知识

JavaScript 中的正则表达式用于模式匹配。其他编程语言允许正则表达式用于搜索和替换文本，但 JavaScript 程序员没有这个便利。尽管如此，正则表达式仍然是搜索复杂模式的一种强大方式。例如，你可以用它们来：

-   验证多种格式的电话号码
-   从字符串中提取所有数字
-   确保日期以有效格式输入
-   验证电子邮件地址是否具有正确的格式

正如我们在前面的代码示例中看到的，正则表达式模式相当复杂，可能有点令人望而生畏。

```javascript
var pattern = /^\(\d{3}\) \d{3}-\d{4}$/;
```

正如我提到的，正则表达式有其自己的语言。有许许多多的符号和特殊字符来表示不同的事物。以下是一些通用规则：

1.  我们首先为正则表达式模式定义一个变量。
    ```javascript
    var pattern;
    ```
2.  正斜杠 (/) 表示 JavaScript 中正则表达式字面量的开始和结束。正则表达式字面量允许我们无需使用 `RegExp` 类即可创建正则表达式对象。
    ```javascript
    var pattern = //;
    ```
3.  插入符 (`^`) 和美元符号 (`$`) 表示行的开始和结束。它们也表示字符串的开始和结束。如果我们只想匹配字符串的一部分，可以省略它们。类似地，如果我们想专门测试长字符串开头的某个模式，我们可以单独使用插入符 (`^`)。目前，以下模式仅匹配空字符串 (`""`)。
    ```javascript
    var pattern = /^$/;
    ```
4.  `\d` 代表一个数字。如果我们将 `\d` 添加到模式中，它将只匹配包含 0 到 9 之间数字的单字符字符串。
    ```javascript
    var pattern = /^\d$/;
    ```
5.  如果我们想匹配多个数字（就像电话号码那样），我们可以将多个 `\d` 标记放在一起；`\d\d\d` 将代表三个数字。我们也可以在花括号中指定数量：`\d{3}`。
    ```javascript
    var pattern = /^\d{3}$/;
    ```
6.  模式中的其他字符，如空格和连字符，仅代表它们自身。因此，以下模式将匹配 `999-999-9999`，这是电话号码的一种表示方式。
    ```javascript
    var pattern = /^\d{3}-\d{3}-\d{4}$/;
    ```
7.  由于括号字符在正则表达式语法中具有特殊含义，要包含它们，我们需要用反斜杠进行转义：`\(` 和 `\)`。这给我们提供了一个匹配 `(999) 999-9999` 的模式，这正是我们想要的。
    ```javascript
    var pattern = /^\(\d{3}\) \d{3}-\d{4}$/;
    ```

正则表达式语法中有许多特殊标记可以匹配不同的字符集。表 3-9 中列出的标记是基本集合。

| 字符 | 含义 |
| :--- | :--- |
| `\\` | 表示特殊标记的开始（例如，`\\d` 匹配一个数字）或表示特殊字符应按字面意思处理（`\\*` 匹配一个星号） |
| `^` | 匹配行的开始；也匹配每个字符串的开始 |
| `$` | 匹配行的结束；也匹配每个字符串的结束 |
| `*` | 特殊量词，意味着前面的标记或标记组必须匹配零次或多次 |
| `+` | 特殊量词，意味着前面的标记或标记组必须匹配一次或多次 |
| `?` | 特殊量词，意味着前面的标记或标记组必须匹配零次或一次 |
| `.` | 匹配除换行符 (`\n`) 以外的任何单个字符 |
| `(abcd)` | 匹配 "abcd" 并记住该匹配 |
| `car\|bus` | 匹配 "car" 或 "bus" |
| `{3}` | 精确匹配前面的标记或标记组三次 |
| `{3,}` | 匹配前面的标记或标记组三次或更多次 |
| `{4,8}` | 匹配前面的标记或标记组四到八次 |
| `[abcdef]` | 匹配 a 到 f 之间的任意一个字符 |
| `[a-f]` | 匹配 a 到 f 之间的任意一个字符 |
| `[a-zA-Z0-9]` | 匹配任意单个字母数字字符 |

**表 3-9 JavaScript 中的正则表达式语法**

| 字符 | 含义 |
| :--- | :--- |
| `[^aeiou]` | 匹配除 *a*、*e*、*i*、*o* 和 *u* 之外的所有字符 |
| `\d` | 匹配一个数字；与模式 `[0-9]` 相同 |
| `\D` | 匹配一个非数字；与模式 `[^0-9]` 相同 |
| `\s` | 匹配一个空格字符（定义了八种空格字符） |
| `\S` | 匹配一个非空格字符 |
| `\t` | 匹配一个制表符 |
| `\n` | 匹配一个换行符 |
| `\r` | 匹配一个回车符 |
| `\w` | 匹配任何字母数字（单词）字符（*a*–*z* 和 0–9），包括下划线 ( _ )；与模式 `[a-zA-Z0-9_]` 相同 |
| `\W` | 匹配任何非单词字符；与模式 `[^a-zA-Z0-9_]` 相同 |
| `\0` | 匹配空字符 |

**表 3-9 JavaScript 中的正则表达式语法（续）**

#### 使用 RegExp 对象创建模式

我们已经了解了如何使用正则表达式字面量创建模式。正则表达式字面量以正斜杠 (/) 开始和结束，如下所示：

```javascript
var zipCodePattern = /^\d{5}(-\d{4})?$/;
```

JavaScript 还提供了一个名为 `RegExp` 的类来创建这些模式。我们可以使用这个类的构造函数重写模式，如下所示：

```javascript
var zipCodePattern = new RegExp ("^\\d{5}(-\\d{4})?$");
```

> **注意** *任何时候将反斜杠 (\) 字符包含在字符串中时，都需要对其进行转义，`RegExp` 构造函数也不例外。双反斜杠 (\\) 代表转义后的反斜杠字符。*

`RegExp` 对象提供了两个主要方法来执行其搜索和匹配功能：`test()` 和 `exec()`。表 3-10 列出了 `RegExp` 对象最常见的方法。

| 方法 | 目的 |
| :--- | :--- |
| compile() | 编译正则表达式 |
| exec() | 在字符串中搜索模式并返回所有匹配项 |
| test() | 将字符串与模式进行比较，并根据结果返回 true 或 false |

**表 3-10 RegExp 对象的方法**

## 90 使用 JavaScript 实现各种功能

一旦创建了 `RegExp` 对象，JavaScript 就能让你非常轻松地用任何字符串测试该模式。

```javascript
var myPattern = new RegExp ("hat.*hat");
document.write ("Pattern 1: \"hat.*hat\"<br>");
document.write (myPattern.test ("That is a nice hat.") + "<br>" );
document.write (myPattern.test ("I love your hat!") + "<br><br>" );

var myPattern2 = new RegExp ("\\w+\\s\\w+");
document.write ("Pattern 2: \"\\w+\\s\\w+\"<br>");
document.write (myPattern2.test ("Jackie Gleason") + "<br>" );
document.write (myPattern2.test ("Cher!") + "<br>" );
```

此模式检查的结果如图 3-2 所示。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_109_0.png)

#### 了解 JavaScript 2.0 强大的新数据类型

到目前为止，我们一直在研究当今绝大多数 Web 浏览器支持的类。JavaScript 2.0 引入了许多新类，如前面表 3-3 所列。对象的创建和访问方式与以前的 JavaScript 版本基本相同，主要由 **new** 和点 (.) 运算符完成工作。

在本节中，我们将研究其中一些新的数据类型，并学习它们强大的功能如何在 JavaScript 程序中应用。

> 本章其余代码旨在支持 JavaScript 2.0 的环境中工作，在其他环境中将无法运行。

##### 使用 Boolean、Integer 和 Number 数据类型

JavaScript 中有三种基本数据类型，称为*原始类型*：数字、字符串和布尔值。所有其他数据类型都是建立在这三个基本构建块之上的。

我们已经在本章前面研究了 String 数据类型。String 对象提供了许多方法来辅助操作字符串，包括搜索（indexOf）、提取字符串的一部分（substring）以及确定字符串的长度（length）。

与 String 相比，Boolean 数据类型非常简单。你可以用它来存储布尔值（true 或 false），并且可以检索该布尔值。基本上就是这些。在编程中确实没有理由使用 Boolean 类，因为布尔字面量更容易创建，而且同样有用。

```javascript
var isFinished : Boolean = false;
var paidToll : Boolean = true;
```

数字原始类型实际上由两种 JavaScript 数据类型表示：Number 和 Integer。两者之间的唯一区别是 Integer 数据类型不能包含小数部分。除此之外，这两个类是相同的。同样，为了方便起见，在大多数情况下我将继续使用数字字面量来创建简单的数字。

```javascript
var counter : Integer = 0;
var invoice_amount : Number = 12363.22;
```

##### 使用 char 数据类型

char 数据类型最与众不同的一点，也许就是它奇怪的命名方式。此数据类型不将其首字母大写，且其名称不是一个完整的单词。（事实上，ECMA 技术委员会曾一度想将其命名为“Character 数据类型”，这将与其他类的命名方式更一致。）

char 数据类型仅表示单个 16 位 Unicode 字符。一些语言称之为*字节*，通常在分配内存空间是首要考虑因素时使用。它存在于



#### 使用对象数据类型

JavaScript 中的每个类——无论是用户定义的还是系统定义的——都是此数据类型的成员。如果你想创建一个可以容纳系统中任何对象的变量，那么这就是需要使用的数据类型。

```javascript
var myObject : Object = new Date ();
myObject = new String ("This is a string");
myObject = new Car (2002, "Ferrari", "Testarosa", "Cherry red");
```

一旦 `myObject` 变量被定义为 `Object` 数据类型的成员，它就可以充当系统中任何其他类的对象。一个类可以充当另一个相关类的对象的这种能力，在面向对象编程中被称为 *多态性*。继承和多态性将在第5章中讨论，届时我们将创建自己的类。

#### 了解特殊数据类型

JavaScript 2.0 还包含一些你可能在日常编程中不会用到——甚至可能永远不会用到的数据类型。正如你在上一章学到的，函数可以返回一个值。而在 JavaScript 2.0 中，你可以为该值分配一个数据类型。

```javascript
function addTwo (num1 : Number, num2 : Number) : Number {
    return num1 + num2;
}
```

#### 使用 Void 数据类型

嗯，你有时可能需要定义一个不返回任何结果的函数。以下程序执行其任务后退出，不返回任何值。

```javascript
function errorMessage (msg : String) {
    alert ("A serious error occurred\n" + msg +
           "\nPress OK to continue.");
    return;
}
```

定义一个没有返回值的函数，如这段代码所示，当然是有效的。但这样做你就让返回值类型变得模糊了。你的函数既可以返回值，也可以不返回值，这两种情况都不是错误。省略函数的数据类型只是告诉系统返回值的类型是未知的。

如果你想明确声明函数不返回值，可以使用 `Void` 数据类型。定义为 `Void` 类型的函数不允许返回值——如果返回了值，那就是错误状况。

```javascript
function errorMessage (msg : String) : Void {
    alert ("A serious error occurred\n" + msg +
        "\nPress OK to continue.");
    return;
}
```

#### 使用 Never 数据类型

或者，也许你的函数在报告错误后就完全停止运行。这在网页浏览器环境中无法实现，但在其他环境中（例如服务器端）可以。导致程序退出的函数应该使用 `Never` 数据类型，意为“此函数永远不会返回”。以下代码示例是在 IIS Web 服务器环境中使用 JavaScript 编写的。

```javascript
function errorMessage (msg : String) : Never {
    response.write ("A serious error occurred\n" + msg +
        "\nPress OK to continue.");
    response.end;
}
```

#### 使用 Null 数据类型

最后，`Null` 数据类型只能包含一个有效值——`null`。老实说，我想不出你有什么理由需要这样做。

```javascript
var useless : Null = null;
```

好了，我们已经查看了 JavaScript 允许我们使用的每个对象和数据类型——几乎都涵盖了，除了数组。JavaScript 2.0 引入了五个新的数组类。在下一章中，我们将研究数组，并了解如何使用它们来存储大量易于访问的数据。

# 第4章
# 将数据组织成数组

# # 如何用 JavaScript 做一切
# ## 如何...

- 创建 Array 对象
- 设置和检索数组中的值
- 使用多维数组
- 使用 JavaScript 2.0 的增强型数组

在第2章中，我们研究了程序如何使用变量来存储数据以供后续检索。程序可以定义的变量数量几乎没有限制。限制只在于程序员记住每个变量用途的能力。

但你有时可能面临不得不将几十个甚至上百个相关值存储到变量名中以供后续使用的任务。例如，你会如何存储以下内容？

- 美国50个州的名称
- 月份的名称
- 你收藏的CD的专辑标题
- 你商店库存中的产品列表

你也许能想出办法在JavaScript代码中存储前两个列表（州和月份名称），或许可以通过为每个名称分配一个自己的变量来实现（例如，`var Nebraska = "Nebraska"`）。虽然这是可行的，但这并不实用。拥有值永远不会改变且值与变量名匹配的变量（甚至常数）有什么意义呢？

那么，你该如何存储那种类型的列表（专辑标题和库存产品）呢？毕竟，这些列表可能会变得相当大（你的商店可能有数百种产品），值可以（并且确实）会变化，甚至列表的长度也会随时间变化。

JavaScript 提供了 *数组对象* 来处理数据列表。数组可以处理值易于检索或修改的长数据列表。数组也可以根据需要增长或收缩。

```javascript
for (counter = 0; counter < 50; counter ++) {
    document.write ("State #" + counter + ": " + 
        statesArray[counter]);
}
```

在这段代码中，变量 `statesArray` 包含了50个美国州名的数组。我们可以使用方括号 `[]` 操作符通过其索引（索引值范围从0到49）来访问这个数组。

```javascript
statesArray[counter];
```

当然，这段代码忽略了显示 Array 对象是如何创建的。有两种方法可以创建 Array 对象：

- Array 类
- 数组字面量

不幸的是，官方规范与各大浏览器制造商在 JavaScript 中实现数组的方式之间存在一些不一致。在本章中，我们将研究数组的创建方式，以及如何创建能在所有浏览器上运行的代码。我们还将探讨 JavaScript 2.0 中数组的一些令人兴奋的改进。

#### 创建 Array 对象

有三种方法使用 JavaScript Array 类创建数组：

- `new Array()`
- `new Array(size)`
- `new Array(element1, element2, ..., elementN)`

#### 创建空数组

向 Array 类的构造函数传递无参数会创建一个 *空数组*，也称为长度为零的数组。（在 JavaScript 中，数组中的项目数量称为其长度。）然后我们可以手动填充数组，如下所示。

1. 我们首先定义一个变量来包含我们的数组。

```javascript
var months;
```

2. 然后我们使用 **new** 操作符创建一个新的 Array 对象。

```javascript
var months = new Array();
```

3. 我们手动为数组的第一个索引赋值。索引从值0开始。

```javascript
var months = new Array();
months[0] = "January";
```

4. 现在我们的数组长度为1。然后我们可以填充数组的其余值。

```javascript
var months = new Array();
months[0] = "January";
months[1] = "February";
months[2] = "March";
months[3] = "April";
months[4] = "May";
months[5] = "June";
months[6] = "July";
months[7] = "August";
months[8] = "September";
months[9] = "October";
months[10] = "November";
months[11] = "December";
```

5. 现在我们有了一个数组，程序的其余部分可以仅通过其数字索引来访问它。

```javascript
var months = new Array();
months[0] = "January";
months[1] = "February";
months[2] = "March";
months[3] = "April";
months[4] = "May";
months[5] = "June";
months[6] = "July";
months[7] = "August";
months[8] = "September";
months[9] = "October";
months[10] = "November";
months[11] = "December";

for (var i = 0; i < 12; i++) {
    document.write(months[i] + "<br>");
}
```

6. 正如你在这里看到的，JavaScript 能够将一组相关值（月份）存储到单个变量中，然后轻松访问这些值以供后续使用。



#### 指定初始数组长度

JavaScript 允许你通过传递单个整数作为参数来指定数组的初始长度。

```
var months = new Array(12);
```

在 JavaScript 1.5 中，像这样预先设置数组长度并没有太大优势，因为数组会自动增长。它提供的一个好处可能是提醒你原本打算定义多大的数组。

数组的长度也可以在程序中通过修改 Array 对象的 length 属性来设置。

```
var months = new Array();
months.length = 12;
```

7. 像这样的列表（一年中的月份）在你希望程序将数字月份转换为对应的字符串时非常方便。幸运的是，Date 对象的 `getMonth()` 函数返回的月份范围是 0 到 11，因此我们甚至不需要在使用之前调整该值。

```
var today = new Date();
var monthnum = today.getMonth();
document.write ("Today is a lovely " +
    months[monthnum] + " day.");
```

#### 用一行代码创建并初始化数组

回顾前面定义的 months 数组，我们最终写了 13 行代码才创建并初始化了这个数组。如果我们能只用一行代码创建同样的数组就好了。当然，如果 JavaScript 做不到的话我就不会提了……

```
var months = new Array ("January", "February", "March", "April",
    "May", "June", "July", "August",
    "September", "October", "November", "December");
```

Array 类的构造函数也接受一个以逗号分隔的数组初始值列表。列出的第一个项目被赋值为索引 0，下一个项目成为索引 1，以此类推。这对于较长的项目列表尤其有用。例如，如果我们需要一个包含美国 50 个州的数组，用一行代码创建它要比写 51 行或更多行代码容易得多。

```
var USStates = new Array ("Alabama", "Alaska", "Arizona",
    "Arkansas", "California", "Colorado", "Connecticut",
    "Delaware", "Florida", "Georgia", "Hawaii", "Idaho",
    "Illinois", "Indiana", "Iowa", "Kansas", "Kentucky",
    "Louisiana", "Maine", "Maryland", "Massachusetts",
    "Michigan", "Minnesota", "Mississippi", "Missouri",
    "Montana", "Nebraska", "Nevada", "New Hampshire",
    "New Jersey", "New Mexico", "New York", "North Carolina",
    "North Dakota", "Ohio", "Oklahoma", "Oregon", "Pennsylvania",
    "Rhode Island", "South Carolina", "South Dakota", "Tennessee",
    "Texas", "Utah", "Vermont", "Virginia", "Washington",
    "West Virginia", "Wisconsin", "Wyoming");
```

#### 使用数组字面量

正如 JavaScript 提供了无需手动创建对象即可创建数字、字符串和正则表达式的方式一样，你也可以用同样的方式创建数组。

```
var months = ["January", "February", "March", "April",
    "May", "June", "July", "August",
    "September", "October", "November", "December"];
```

上述代码中的方括号使 JavaScript 将其内容解释为新数组的内容。这等同于使用正确的构造函数语法来创建数组。

```
var months = new Array("January", "February", "March", "April",
    "May", "June", "July", "August",
    "September", "October", "November", "December");
```

使用数组字面量创建的对象可以访问 Array 对象的所有属性和方法。

#### 将长代码行分成多行

为了使长代码行更易于阅读（对你自己和查看你代码的其他程序员而言），在文本滚动到屏幕右侧之前加入一个换行符是明智的做法。JavaScript 支持跨多行编写的代码，只要它们放在适当的位置即可。JavaScript 会忽略多余的空格和换行符，因为它将分号（`;`）视为语句的真正结束。

#### 调用 Array 对象的属性和方法

JavaScript 中的 Array 对象仅暴露三个属性。其中两个属性仅在被调用的数组是正则表达式模式匹配的结果时才会设置，正如第 3 章所讨论的。length 属性（所有数组都可用）是这三个属性中唯一可以修改的，因为它表示数组的当前长度。

| 属性 | 描述 |
|---|---|
| index | 与正则表达式模式匹配相关；包含匹配子串的索引（只读） |
| input | 与正则表达式模式匹配相关；包含进行匹配的原始字符串（只读） |
| length | 获取或设置数组的长度 |

*数组中的每个元素不一定都必须包含值。你同样可以创建一个跳过每隔一个索引号的数组，或者跳过任意数量索引号的数组。*

length 属性既考虑数组中空（未使用）索引的数量，也考虑数组包含的元素数量。因此，如果你跳过大量的索引号，length 属性将远大于元素的数量。

```
var employee = new Array();
employee[127756] = "Tom Jones";
alert(employee.length);
```

这段代码返回数组的长度为 127,757，因为这是从 0 到 127,756 的元素数量（包括空的）。

Array 对象还包含许多有用的方法，使程序员能更轻松地管理数组内容，如表 4-1 所示。

使用表 4-1 中列出的 Array 对象方法，可以对数组内容进行多种高级修改操作。其中有四个方法允许我们将数组视为*调用栈*或*队列*。

在编程中，调用栈类似于一叠煎饼。最后添加到栈顶的煎饼必须最先被取走（或吃掉）。这种排列方式有时被称为*后进先出*（LIFO）方法。

队列非常像银行的排队，排在队伍前面的人最先被服务。毫不意外，这种排列方式有时被称为*先进先出*（FIFO）方法。

| 方法 | 描述 |
|--------|-------------|
| pop() 和 push() | 后进先出（LIFO）；类似于调用栈 |
| shift() 和 unshift() | 先进先出（FIFO）；类似于队列 |

还有其他一些有趣的方法，可以让你将数组转换为单个字符串、将数组拆分为子数组，甚至将两个或多个数组连接在一起。

在下面的代码中，我们使用 Array 类创建了多个数组。

```
var MainMenu = new Array("File", "Edit", "View",
    "Window", "Help");
var FileMenu = new Array("New", "Open", "Close", "Save", "Exit");
var EditMenu = new Array("Undo", "Repeat", "Cut", "Copy", "Paste");
var ViewMenu = new Array("Normal", "Web Layout", "Outline");
var WindowMenu = new Array("New Window", "Arrange All", "Split");
var HelpMenu = new Array("Contents", "About", "Contact Us");
```

##### 表 4-1 Array 对象的方法

| 方法 | 描述 |
|--------|-------------|
| concat (*array1*, *array2...arrayN*) | 将两个或多个数组合并为一个数组 |
| join (*separator*) | 将数组的所有元素连接为一个字符串，使用指定的分隔符分隔，如果未指定则使用逗号 |
| pop () | 返回数组的最后一个元素并将其移除 |
| push (*element1*, *element2...elementN*) | 在数组末尾添加一个或多个元素并返回其新长度 |
| reverse () | 反转数组中元素的顺序 |
| shift () | 类似于 pop ()；返回数组的第一个元素并将其移除 |
| slice (begin, end) | 从现有数组的子段创建一个新数组，由起始和结束索引定义 |
| splice (index, howMany, element1, element2...elementN) | 用于从数组中添加或移除元素 |
| sort (functionName) | 用于对数组元素进行排序 |
| unshift (element1, element2...elementN) | 类似于 push ()；在数组开头添加一个或多个元素并返回其新长度 |

这些数组代表一个假设网站的菜单。我们可以对这些数组中的每一个使用 Array 对象的一些方法来修改它或提取部分信息。

```
//创建一个包含数组所有元素的字符串
// 数组本身不受影响
var MenuItemsStr = MainMenu.join(" | ");
document.write (MenuItemsStr + "<br><br>");
```

```
// 创建一个包含所有数组全部元素的新数组
// 现有数组均不受影响
var AllMenuItems = MainMenu.concat(FileMenu, EditMenu, ViewMenu, WindowMenu, HelpMenu);
document.write (AllMenuItems.join(", ") + "<br><br>");
```

```
// 反转数组中元素的顺序
// 修改现有数组
MainMenu.reverse();
document.write (MainMenu.join(" | ") + "<br><br>");
```

```
// 创建一个包含现有数组子集的新数组
// 现有数组均不受影响
var ChildMenuItems = AllMenuItems.slice(MainMenu.length);
document.write (ChildMenuItems.join(" <font size=+3>||</font> ")
                + "<br><br>");
```



这些数组操作的结果可以在以下截图中看到。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_123_0.png)

#### 在数组中设置和获取值

JavaScript Array 对象内部的元素通过方括号运算符进行访问。

```
var myArray = new Array();
myArray[16] = "Some value";
document.write (myArray[16]);
```

方括号内的数字称为*索引*。你可以把数组想象成一系列停车位，编号从 0 一直到无穷大。当泊车员把你的车停在其中一个车位时，他必须记住车位号，以便再次找到你的车。

JavaScript 数组支持使用字符串作为索引。当使用字符串作为索引时，这被称为*哈希表*。

```
var FruitColors = new Array();
FruitColors["Apple"] = "red";
FruitColors["Banana"] = "yellow";
FruitColors["Grape"] = "purple";
```

## 第四章：将数据组织成数组

在这里，字符串 "Apple" 被用作索引来存储值 "red"。字符串 "Apple" 可以被称为*键*。存储在哈希表中的值可以使用键来检索，就像使用数字索引的数组一样。

```
document.write ("Apples are " + FruitColors["Apple"] + ".<br>");
document.write ("Bananas are " + FruitColors["Banana"] + ".<br>");
document.write ("Grapes are " + FruitColors["Grape"] + ".<br>");
```

正如我们在第二章中看到的，数组也可以使用 **for-in** 语句来访问。**for-in** 语句会遍历数组中的每个元素，返回索引或键。

```
var FruitColors = new Array();
FruitColors["Apple"] = "red";
FruitColors["Banana"] = "yellow";
FruitColors["Grape"] = "purple";

for (var fruit in FruitColors) {
    document.write (fruit + "s are " + FruitColors[fruit]
        + ".<br>");
}
```

在这里，**for-in** 循环对 document.write() 函数执行了三次迭代，分别对应数组中的每个项目。输出结果如图 4-1 所示。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_124_0.png)

**图 4-1** **for-in** 循环遍历哈希表。

#### 如何用 JavaScript 做所有事情

同样的技术也可以用于具有数字索引的数组：

```
var Players = new Array();
Players[0] = "Jaime";
Players[1] = "Mom";
Players[2] = "Bart";
Players[3] = "Liez'l";

// Who do we have playing bridge?
for (var name in Players) {
    document.write (name + ": ");
    document.write (Players[name] + " is playing bridge.<br>");
}
```

从图 4-2 的输出中可以看到，**for-in** 循环同样能够遍历我们的每一位桥牌玩家。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_125_0.png)

**图 4-2** **for-in** 循环遍历数组。

#### 使用多维数组

我们在本章中迄今为止看到的数组有时被称为*一维数组*。如果你把数组想象成一个包含行和列的图形表格，那么这些一维数组只有一列，如图 4-3 所示。

二维数组是当以图形表格显示时包含多列的数组。当你需要为列表中的每个项目存储多个值时，就会用到二维数组。图 4-4 展示了二维数组的图形表示。

三维数组看起来更像是一个立方体，因为图中增加了一个深度维度。信不信由你，还有四维数组以及更高维度的数组。不过，我们生活在三维世界中，要以图形方式显示这些复杂的数据集变得越来越困难。

一些编程语言允许将多维数组定义为语言的核心特性。不幸的是，JavaScript 并不支持。如果你想在 JavaScript 应用程序中定义多维数组，就必须在一维数组的限制下进行操作。

有两种技术可以在 JavaScript 中模拟多维数组：

- 你可以创建并行的一维数组。
- 你可以创建数组的数组。

| 列 0 |
|---|
| 行 0："January" |
| 行 1："February" |
| 行 2："March" |
| 行 3："April" |
| 行 4："May" |
| 行 5："June" |
| 行 6："July" |
| 等等 |

**图 4-3** 简单（一维）数组的图形表示

#### 如何用 JavaScript 做所有事情

| 列 0 | 列 1 | 列 2 | 列 3 |
|----------|----------|----------|----------|
| "January" | "Garnet" | "Red" | "Constancy" |
| "February" | "Amethyst" | "Purple" | "Sincerity" |
| "March" | "Bloodstone" | "Blue" | "Courage" |
| "April" | "Diamond" | "White/Clear" | "Innocence" |
| "May" | "Emerald" | "Green" | "Love" |
| "June" | "Pearl" | "Cream" | "Health" |
| "July" | "Ruby" | "Red" | "Contentment" |

**图 4-4** 二维数组包含多列。

我们在本章中首先研究的数组之一是月份列表。让我们继续这个示例。我们从以下一维数组开始：

```
var months = new Array ("January", "February", "March", "April",
    "May", "June", "July", "August",
    "September", "October", "November", "December");
```

假设我们想列出以下四个项目：

- 一年中的月份
- 与每个月相关的诞生石
- 每块诞生石的颜色
- 每块诞生石所代表的含义

目前我们的数组只包含月份；如果我们随意将另外三个想要列出的内容添加进去，只会让数组变得混乱，更难以使用。

```
var months = new Array ("January", "February", "March", "April",
    "May", "June", "July", "August",
    "September", "October", "November", "December",
    "Garnet", "Amethyst", "Bloodstone or Aquamarine",
    "Diamond", "Emerald", "Pearl, Moonstone, or Alexandrite",
    "Ruby", "Sardonyx or Peridot", "Sapphire",
    "Opal or Tourmaline", "Topaz", "Turquoise or Lapis lazuli",
    "Red", "Purple", "Green/Red or Blue", "White/Clear",
    "Green", "Cream", "Red", "Light Green",
```

## 第四章：将数据组织成数组

```
"Blue", "Many Colors", "Orange/Brown", "Blue",
"Constancy", "Sincerity", "Courage", "Innocence",
"Love and success", "Health and longevity", "Contentment",
"Married happiness", "Clear thinking", "Hope",
"Fidelity", "Prosperity");
```

从这段代码可以看出，简单地将额外的列表添加到现有数组中并不是最佳解决方案。这不仅对人类来说难以阅读和理解，程序员在创建程序时也必须小心，以免内容混在一起。

我们可以使用四个并行数组来重写这个混乱的数组，如下所示。

```
var months = new Array ("January", "February", "March", "April",
    "May", "June", "July", "August",
    "September", "October", "November", "December");
```

```
var stones = new Array ("Garnet", "Amethyst",
    "Bloodstone or Aquamarine", "Diamond", "Emerald",
    "Pearl, Moonstone, or Alexandrite", "Ruby",
    "Sardonyx or Peridot", "Sapphire", "Opal or Tourmaline",
    "Topaz", "Turquoise or Lapis lazuli");
```

```
var colors = new Array ("Red", "Purple", "Green/Red or Blue",
    "White/Clear", "Green", "Cream", "Red", "Light Green",
    "Blue", "Many Colors", "Orange/Brown", "Blue");
```

```
var meaning = new Array ("Constancy", "Sincerity", "Courage",
    "Innocence", "Love and success", "Health and longevity",
    "Contentment", "Married happiness", "Clear thinking",
    "Hope", "Fidelity", "Prosperity");
```

每个数组中的元素与其他数组中相同索引的元素完全对应，所以假设我想查询一年中第七个月的信息。（记住数组从索引 0 开始，所以一年中的第七个月描述在第 6 号元素处。）

```
document.write ("The seventh month is <b>" + months[6]);
document.write ("</b>. Its birthstone is <b>");
document.write (stones[6] + "</b>. The " + stones[6]);
document.write (" is a <b>" + colors[6] + "</b> colored stone, ");
document.write ("and it means <b>" + meaning[6] + "</b>");
document.write (" traditionally.<br>");
```

通过这种方式，我们能够在各自的数组中定义信息，从而存储关于每个月的多列数据。我们可以在图 4-5 的网页浏览器截图中看到这段代码的运行结果。



## 如何用JavaScript实现一切功能

![](img/f14dd58a324d5464a114c30c1d4c4c9b_129_0.png)

图4-5 使用并行数组可以模拟二维数组。

创建多维数组的另一种方法是创建一个包含其他数组的数组——这被称为数组的数组。
要创建数组的数组，你需要执行以下步骤。

1.  首先，定义四个数组，就像你定义并行数组一样。

```javascript
var months = new Array ("January", "February", ...);
var stones = new Array ("Garnet", " Amethyst", ...);
var colors = new Array ("Red", "Purple", ...);
var meanings = new Array ("Constancy", "Sincerity", ...);
```

2.  接着，定义一个主数组，用于存放所有四个数组。

```javascript
var marray = new Array();
```

3.  然后，将包含数据的四个数组分别赋值给这个主数组。

```javascript
var marray = new Array();

marray[0] = months;
marray[1] = stones;
marray[2] = colors;
marray[3] = meanings;
```

4.  之后，你应该修改程序，通过主数组的名称和相应的数组索引来访问子数组。

```javascript
var marray = new Array();

marray[0] = months;
marray[1] = stones;
marray[2] = colors;
marray[3] = meanings;

document.write ("The fourth month is <b>" + marray[0][3]);
document.write ("</b>. Its birthstone is <b>");
document.write (marray[1][3] + "</b>. The " + marray[1][3]);
document.write (" is a <b>" + marray[2][3] + "</b> "
    + "colored stone, ");
document.write ("and it means <b>" + marray[3][3] + "</b>");
document.write (" traditionally.<br>");
```

如你所见，我们不能再像 months[3] 那样引用数组，而必须使用主数组的名称和索引，如 marray[0][3]。正如你在图4-6中所看到的，这种技术也是创建二维数组的有效方法。

#### 使用 JavaScript 2.0 的增强数组

JavaScript 2.0 在传统的 Array 类基础上增加了三个不同的子类。每个子类都与 JavaScript 中数组一直以来的工作方式非常相似，但也有一些独特的区别。表4-2列出了传统的 Array 类和三个新类，并描述了这些不同的类。

| 数组对象名称 | 描述 |
| --- | --- |
| Array [*datatype*] | 这个（原始的 Array 类）是一个抽象类。调用时，它返回一个 DynamicArray 对象。如果未指定数据类型，则默认为 Object 类型。 |
| StaticArray [*datatype*] | 这个新子类在添加新元素时不会自动增长。它不能包含空元素，并且不能在没有数据类型的情况下被调用。 |
| DynamicArray [*datatype*] | 这个新子类就是传统的 JavaScript Array 对象。它不能在没有数据类型的情况下被调用。 |
| ConstArray [*datatype*] | 这个新子类创建一个常量数组，其值一旦设置就不能更改。它不能包含空元素。如果未指定数据类型，则默认为 Object 类型。 |

![](img/f14dd58a324d5464a114c30c1d4c4c9b_131_0.png)

图4-6 数组的数组技术非常接近于模拟真正的二维数组。

每种数组类型通常在实例化时都会指定一个数据类型。Array 和 ConstArray 为数据类型提供了默认值，而其他类型则没有。定义数组时提供的数据类型会将数组的内容限制为该数据类型的对象。

在本节中，我们将研究三种新的数组类型，并了解如何在 JavaScript 程序中使用它们。

##### StaticArray 类

StaticArray 类创建具有预定长度的数组，其值可以随时修改。有两种创建新 StaticArray 的方法：

- new StaticArray [datatype] ()
- new StaticArray [datatype] (size)

JavaScript 2.0 规范规定，StaticArray 必须定义数据类型。要创建一个可以接受任何数据类型的数组，我们可以将数组定义为接受 Object 类型的值。由于 Object 是 JavaScript 中所有类（包括你自己创建的类）的父数据类型，Object 数组可以接受任何值。

创建一个不传入数据类型的 StaticArray 会导致创建一个可以包含任何对象的数组。回想一下上一章的内容，Object 是系统中每个类的数据类型，包括你自己定义的类。

```javascript
var myArray : StaticArray = new StaticArray[Object]();
myArray.length = 4;
myArray[0] = "This is the first element";
myArray[1] = 3.141;
myArray[2] = new Car(2001, "Toyota", "4Runner", "Thundercloud");
myArray[3] = new Date();
```

这段代码创建了一个新的类型为 Object 的 StaticArray 变量。我们利用这一点，将字符串、数字、用户定义的 Car 对象和一个 Date 对象存储到这个数组中。

由于 StaticArray 必须有一个预定义的长度，我们首先将数组的 length 属性初始化为值 4，即我们打算存储的项目数量。尝试添加额外的项目会导致 JavaScript 错误，除非我们手动增加 length 的值。

```javascript
var myArray : StaticArray = new StaticArray[Object]();
myArray.length = 5;
myArray[0] = "This is the first element";
myArray[1] = 3.141;
myArray[2] = new Car(2001, "Toyota", "4Runner", "Thundercloud");
myArray[3] = new Date();
myArray[4] = "This is a new element.";
```

提供更具体的数据类型，例如 Number，会将数组的元素限制为仅为该类型。

```javascript
var mySecondArray : StaticArray = new StaticArray[Number](6);
mySecondArray[0] = 14.2;
mySecondArray[1] = 13;
mySecondArray[2] = 21.9999;
mySecondArray[3] = 2141330119;
mySecondArray[4] = 0.0000003;
mySecondArray[5] = 1.0121E26;
```

> 注意 类型为 StaticArray 的数组不能有缺失的元素；也就是说，你不能像使用 DynamicArray 那样跳过索引编号。

尝试向一个只接受数字的 StaticArray 添加字符串将导致 JavaScript 错误。

```javascript
mySecondArray[5] = "This is not allowed.";
```

##### DynamicArray 类

DynamicArray 与 StaticArray 类似，不同之处在于数组的大小会根据你尝试添加的元素自动调整。有两种创建 DynamicArray 的方法：

- new DynamicArray [*datatype*] ()
- new DynamicArray [*datatype*] (*size*)

这意味着你可以创建一个空数组并向其中添加元素，而无需考虑现有数组的长度。

```javascript
var Nieces : DynamicArray = new DynamicArray[String]();
Nieces[0] = "Sofia";
Nieces[1] = "Monica";
Nieces[2] = "Tiffany";
Nieces[3] = "Liz";
Nieces[4] = "Elke";
Nieces[5] = "Christine";
Nieces[6] = "Leah";
```

这个 DynamicArray，Nieces，可以持续增长到几乎无限的大小，仅受计算机内存量的限制。DynamicArray 与其他类型数组的另一个区别是你没有义务填充每一个元素。以下是使用 DynamicArray 的有效代码：

```javascript
var emps : DynamicArray = new DynamicArray[String]();
emps[9931] = "John H. Smith";
```

尽管我们没有提供索引 0 到 9930 的值，我们仍然可以跳到 9931 并为该数组元素提供值。

##### ConstArray 类

JavaScript 2.0 支持的第三种新数组类型是 ConstArray。ConstArray 与 DynamicArray 非常相似，有三个显著的区别：

- 它们可以在不指定数据类型的情况下被定义。
- 它们的值一旦设置就不能更改。
- 它们不支持跳过元素。

有四种创建新 ConstArray 的方法：

- new ConstArray ()
- new ConstArray (*size*)
- new ConstArray [datatype] ()
- new ConstArray [datatype] (size)

ConstArray 类借鉴了 JavaScript 的常量变量类型。（我们在第2章讨论过常量。）一旦设置，常量的值就不能更改。

```javascript
var months : ConstArray = new ConstArray[String](12);
months[0] = "January";
months[1] = "February";
months[2] = "March";
months[3] = "April";
months[4] = "May";
months[5] = "June";
months[6] = "July";
months[7] = "August";
months[8] = "September";
months[9] = "October";
months[10] = "November";
months[11] = "December";
```

由于一年中月份的名称在程序执行期间不太可能改变，我们可以将它们定义为常量。然后我们可以自由地使用本章前面描述的相同方括号语法，在程序的后续部分访问这些字符串。
前两章重点介绍了 JavaScript 提供的内置类，特别是 JavaScript 2.0 提供的新类和数据类型。下一章将完全关于在 JavaScript 1.5 和 2.0 中创建你自己的类。



 第5章

## 创建你自己的 JavaScript 类

118 精通 JavaScript 的必备方法

#### 如何……

- 在 JavaScript 1.x 中创建对象
- 使用对象字面量
- 在 JavaScript 2.0 中创建对象
- 使用继承来组织类

前几章讨论了如何使用 JavaScript 的内置类来存储多种类型的数据（日期、数字、布尔值等）。JavaScript 还提供了一种创建你自己的类的方式，以便你能设计自己的数据类型。

在本章中，我们将探讨 JavaScript 程序可以用来定义其自身所需对象的方法。我们还将考察在 JavaScript 1.x 中创建的对象与在 JavaScript 2.0 中创建的对象之间的区别。

#### 了解 JavaScript 中的类

在某些方面，JavaScript 是一种面向对象的编程语言，而在某些方面则不是。JavaScript 一直以来都具有创建和使用对象的能力。事实上，设计一个不以某种方式使用文档对象模型或 JavaScript 提供的任何基于对象的数据类型的 JavaScript 程序，几乎是不可能的。

但 JavaScript 程序通常并不是围绕面向对象编程模型来设计的，不像 Java 和 C++ 程序那样。JavaScript 不强制使用类，这会迫使程序员使用第 3 章讨论的面向对象编程模型。JavaScript 程序员可以自由地编写非结构化或程序化的程序，以适应手头的任务。

尽管如此，对用户自定义类和对象的支持是该语言在未来的几个月和几年中将越来越被接受的一个方面。JavaScript 1.x 中对类的支持有限，但确实存在。JavaScript 2.0 中的类支持已得到极大改进。随着程序员开始发现将其代码组织成独立的、可复用的对象的好处，我们将看到类的使用不断增长。

#### 在 JavaScript 1.x 中创建对象

在 JavaScript 1.x 中有四种创建你自己的对象的方法：

- 调用构造函数
- 使用对象字面量
- 扩展现有类
- 扩展现有对象

在下面的章节中，我们将逐一考察这些方法。

#### 调用构造函数

在 JavaScript 中创建对象的一种方法是创建一个称为*对象构造函数*的特殊函数。构造函数的工作是初始化对象以供使用——本质上就是执行所有必要的设置任务。构造函数一开始看起来就像普通函数一样，但使用一个特殊的对象——*this 对象*——来向自身添加属性。要创建构造函数，请按照以下步骤：

1. 定义一个空函数，使用你希望创建的类名。

```
function Car () {
}
```

2. 特殊的 this 对象是类用来引用自身的。我们可以使用 this 对象在构造函数内部添加新属性。

```
function Car () {
    this.Make = "Toyota";
}
```

3. 由于我们希望构造函数具有灵活性并支持多种不同类型的 Car 对象，最好使用函数的参数来定义任何属性。

```
function Car (make) {
    this.Make = make;
}
```

4. 然后我们可以添加更多属性，使我们的 Car 对象完整。

```
function Car (make, model, year, color) {
    this.Make = make;
    this.Model = model;
    this.Year = year;
    this.Color = color;
}
```

5. 当然，我们可以添加一个不依赖于任何参数的属性。

```
function Car (make, model, year, color) {
    this.Make = make;
    this.Model = model;
    this.Year = year;
    this.Color = color;
    this.FullName = this.Year + " " +
        "<b>" + this.Make + "</b> " +
        this.Model;
}
```

6. 现在我们已经为 Car 类定义了一个构造函数，我们的程序可以调用它来创建一个 Car 对象。

```
function Car (make, model, year, color) {
    this.Make = make;
    this.Model = model;
    this.Year = year;
    this.Color = color;
    this.FullName = this.Year + " " +
        "<b>" + this.Make + "</b> " +
        this.Model;
}

var mySUV = new Car("Toyota", "4Runner SR5",
    2001, "Thundercloud");
```

7. 创建了 mySUV 对象后，我们可以访问 Car 类的任何属性。

```
var mySUV = new Car("Toyota", "4Runner SR5",
    2001, "Thundercloud");
document.write ("I drive a " + mySUV.FullName);
```

##### JavaScript 构造函数

I drive a 2001 **Toyota** 4Runner SR5

8. 事实上，我们可以从这一个构造函数创建多个对象，它们都有自己独立的属性。更改一个对象的属性值不会影响其他对象中相同属性的值。

```
var mySUV = new Car("Toyota", "4Runner SR5",
    2001, "Thundercloud");
var mySportsCar = new Car("Acura", "NSX-T",
    1999, "Red");
var myDreamCar = new Car("Ferrari", "F355 F1",
    2000, "Ferrari Red");
```

```
mySportsCar.Color = "Black";
document.write (mySUV.FullName + " = " +
    mySUV.Color + "<br>");
document.write (mySportsCar.FullName + " = " +
    mySportsCar.Color + "<br>");
document.write (myDreamCar.FullName + " = " +
    myDreamCar.Color + "<br>");
```

这种创建对象的方法适用于所有浏览器中的 JavaScript，最早可追溯至 Internet Explorer 3.0 和 Netscape Navigator 3.0。

> 注意：JavaScript 中属性名是区分大小写的。属性 myCar.color 与 myCar.Color 并不相同。

#### 使用对象字面量

JavaScript 对象字面量是一种无需预先定义构造函数即可创建对象的便捷方式。它实际上是一个未命名的构造函数。JavaScript 最大的优势之一是它能让程序员快速地创建程序，而对象字面量正是它如何实现这一点的典型例子。使用对象字面量快速创建对象的代价是，你失去了为其他对象或其他程序复用代码的能力。

对象字面量由若干属性-值对组成，用一对花括号括起来。冒号分隔属性和值，逗号分隔属性-值对。

```
{ property1 : value , property2 : value , ... , propertyN : value }
 earthy; 0) ([
    erre_tit)
        er
                {}
                    ]
                        ]
                            ]
                                ]
                                    ]
                                    ]
                                        ]
                                    ]
                                ]
                            ]
                        ]
                    ]
                ]
            ]
        ]
    ]
]
```

我们可以使用对象字面量按如下方式创建与上一节相同的 mySUV 对象：

```
var mySUV = {Make: "Toyota",
                Model: "4Runner SR5",
                Year: 2001,
                Color: "Thundercloud"};
```

为了使用对象字面量定义 FullName 属性，我们必须使用一点技巧。在对象字面量内部，你无法引用任何其他属性。以下代码显示了我们如何被迫手动定义 FullName：

```
var mySUV = {Make: "Toyota",
                Model: "4Runner SR5",
                Year: 2001,
                Color: "Thundercloud",
                FullName: "2001 Toyota 4Runner SR5"};
```

当需要定义上一节中的另外两个对象（mySportsCar 和 myDreamCar）时，复用 mySUV 对象代码的唯一方法是复制和粘贴，大多数人都会同意这不是复用代码的最佳方式。

```
var mySportsCar = {Make: "Acura",
                    Model: "NSX-T",
                    Year: 1999,
                    Color: "Red",
                    FullName: "1999 Acura NSX-T"};
```

```
var myDreamCar = {Make:"Ferrari",
		  Model:"F355 F1",
		  Year:2000,
		  Color:"Ferrari Red",
		  FullName:"2000 Ferrari F355 F1"};
```

正如你所看到的，当你不预期需要创建其他相同类型的对象时，对象字面量是最佳选择。

#### 扩展现有类

JavaScript 允许你通过为类分配自己的方法和属性来扩展其功能。这包括向任何预定义的系统类添加新方法和属性。它通过一种称为*原型*的系统来实现这一点。

JavaScript 自动为每个类提供一个名为 prototype 的属性，可用于在类级别扩展功能。

```
ClassName.prototype.member1 = value1;
```

可以为新成员（member1）分配默认值（value1），并将其添加到指定的类（ClassName）中。这个新成员是静态的，其值由该类派生的所有对象共享。在一个对象中更改其值会改变所有对象的值。

让我们从一个例子开始。在以下代码中，我们定义了一个函数，它接受一个 Date 对象作为参数，并返回一个字符串，表示该日期所属的季节名称（"Spring"、"Summer"、"Fall" 或 "Winter"）。

```
function getSeason (obj) {
	var mon = obj.getMonth();
	var day = obj.getDay();
	if (mon < 2 || (mon == 2 && day < 20)) {
		return "Winter";
	} else if (mon < 5 || (mon == 5 && day < 21)) {
		return "Spring";
	} else if (mon < 8 || (mon == 8 && day < 23)) {
		return "Summer";
	} else if (mon < 11 || (mon == 11 && day < 22)) {
		return "Fall";
	} else {
		return "Winter";
	}
}
```



#### 定义你自己的类

在 JavaScript 2.0 中，类是使用以下语法定义的：

```
class className { statements; }
```

如你所见，这个语法相当简单。在实践中，定义类是相当容易和直接的。我们可以采用本章前面定义的 Car 类，并使用 JavaScript 2.0 语法来定义它。

- 1. 使用 class 定义语法定义一个名为 Car 的类。

```
class Car {
}
```

- 2. 然后定义我们的 Car 类将拥有的所有属性。

```
class Car {
    var Make;
    var Model;
    var Year;
    var Color;
    var FullName;
}
```

- 3. 请记住，JavaScript 2.0 支持变量的数据类型，因此让我们使我们的定义更具体。

```
class Car {
    var Make : String;
    var Model : String;
    var Year : Integer;
    var Color : String;
    var FullName : String;
}
```

- 4. 我们需要向 Car 类添加一个构造函数来初始化这些变量。构造函数通常与类同名，尽管可以使用特殊语法定义不同名称的构造函数。`this` 对象仍然用于引用当前对象。

```
class Car {
    var Make : String;
    var Model : String;
    var Year : Integer;
    var Color : String;
    var FullName : String;
    function Car (make, model, year, color) {
        this.Make = make;
        this.Model = model;
        this.Year = year;
        this.Color = color;
        this.FullName = this.Year + " " +
            "<b>" + this.Make + "</b> " +
            this.Model;
    }
}
```

- 5. Car 类可以使用与在 JavaScript 1.x 下定义的类完全相同的方式进行实例化，即使用 **new** 关键字。

```
var mySUV = new Car("Toyota", "4Runner SR5",
    2001, "Thundercloud");
```

- 6. 创建了 mySUV 对象后，我们就可以访问 Car 类的任何属性。

```
var mySUV = new Car("Toyota", "4Runner SR5",
    2001, "Thundercloud");
document.write ("I drive a " + mySUV.FullName);
```

使用 JavaScript 2.0 类更容易创建方法，因为可以在类体内部定义函数。

```
class Book {
    var title : String;
    var author : String;
    var chapters : Array[String];
    function print_title () {
        document.write ("Title: " + this.title + "<br>");
    }
    function print_author () {
        document.write ("Author: " + this.author + "<br>");
    }
    function print_all () {
        var counter = 0;
        print_title();
        print_author();
        for (chapter in this.chapters) {
            counter++;
            document.write ("Chapter " + counter + ": " +
                this.chapters[chapter] + "<br>");
        }
    }
}
```

Book 类定义后，我们可以使用 **new** 关键字创建一个 Book 对象。由于我们的类没有构造函数，因此我们可以手动设置每个属性。调用该新对象的方法将产生我们预期的行为。

```
var thisBook = new Book();
thisBook.title = "How To Do Everything with JavaScript";
thisBook.author = "Scott Duffy";
thisBook.chapters = new Array(15);
thisBook.chapters[0] = "Prepare to Program in JavaScript";
thisBook.chapters[1] = "Learn JavaScript Fundamentals";
thisBook.chapters[2] = "Use Built-In JavaScript Classes";
thisBook.chapters[3] = "Organize Data into Arrays";
thisBook.chapters[4] = "Create Your Own JavaScript Classes";
// etc.
thisBook.print_all();
```

这将产生以下浏览器输出。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_148_0.png)

#### 使用继承组织类

将程序组织成类的好处之一是可以使用*继承*在类之间建立关系。继承允许你做两件事：

- 节省编程时间，因为相关的类可以共享代码
- 为相关类强制执行一套标准的公共属性和方法

JavaScript 2.0 允许一个类使用 **extends** 关键字从另一个类继承。

```
class ClassName extends ParentClass { statements; }
```

这就在 ParentClass 和 ClassName 类之间建立了一种父子关系。理解继承的最佳方式是将类结构想象成一个层级树。

在树的顶部是 Object 类，它是系统中所有类的父类。系统中所有没有显式父对象的类都默认从 Object 类派生。而那些定义了显式父类的，则从该类继承。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_149_0.png)

> *注意：JavaScript 2.0 中的所有类（包括系统类和用户定义的类）都以 Object 类为直接或间接祖先，即使是那些从另一个类扩展的类也是如此。*

我们可以按照常规方式定义父类。

```
class Vehicle {
    var Maker;
    var Price;
    var Color;

    function Vehicle (maker, price, color) {
        this.Maker = maker;
        this.Price = price;
        this.Color = color;
    }
    function Vehicle () {
        this.Maker = "Default";
        this.Price = 0.0;
        this.Color = "Transparent";
    }
}
```

这段代码定义了一个 Vehicle 类，尽管只有三个属性。这个类代表任何通用的车辆，无论是船、飞机还是汽车。该类应该能够处理任何可以被视为车辆的对象。

#### 扩展现有对象

就像可以使用 prototype 属性扩展类一样，对象本身也可以附加新的属性和方法。

```
function Car (make, model, year, color) {
  this.Make = make;
  this.Model = model;
  this.Year = year;
  this.Color = color;
  this.FullName = this.Year + " " + 
    "<b>" + this.Make + "</b> " + 
    this.Model;
}
var mySUV = new Car("Toyota", "4Runner SR5",
    2001, "Thundercloud");
mySUV.mileage = 12323;
document.write(mySUV.FullName + " has traveled " +
    mySUV.mileage + " miles.<br><br>");
```

![](img/f14dd58a324d5464a114c30c1d4c4c9b_145_0.png)

尽管 Car 类没有定义名为 mileage 的属性，但我们可以通过简单地给它赋值来为 mySUV 对象创建一个。由于我们将此属性应用于 mySUV 对象而不是 Car 类，因此从 Car 类派生的其他对象将不具有 mileage 属性。

#### 在 JavaScript 2.0 中创建对象

JavaScript 2.0 完全重新设计了类的定义方式。尽管大多数 JavaScript 环境为了向后兼容仍会支持旧的方式，但很难比较这两种技术。原型和手动添加的属性不再是 JavaScript 中生成用户定义类和对象的首选方法。

因此，我们可以使用 Date 对象调用前面的函数，并获取该日期所在的正确季节。

```
var today = new Date();
document.write(getSeason(today));
```

你可能会认为，如果 getSeason() 函数是 Date 对象的一个方法，而不是一段外部代码，那将更加方便。要将 getSeason() 函数附加到 Date 类，我们首先需要修改它，使其作用于特殊的 `this` 对象，就像类内部的所有方法一样。

```
function getSeason () {
    var mon = this.getMonth();
    var day = this.getDay();
    if (mon < 2 || (mon == 2 && day < 20)) {
        // 涵盖 1 月 1 日至 3 月 19 日
        return "Winter";
    } else if (mon < 5 || (mon == 5 && day < 21)) {
        // 涵盖 3 月 20 日至 6 月 20 日
        return "Spring";
    } else if (mon < 8 || (mon == 8 && day < 23)) {
        // 涵盖 6 月 21 日至 9 月 22 日
        return "Summer";
    } else if (mon < 11 || (mon == 11 && day < 22)) {
        // 涵盖 9 月 23 日至 12 月 21 日
        return "Fall";
    } else {
        // 涵盖 12 月 22 日至 12 月 31 日
        return "Winter";
    }
}
```

然后我们必须如下所示将 getSeason() 函数附加到 Date 对象：

```
Date.prototype.getSeason = getSeason;
```

然后我们可以直接从我们创建的任何 Date 对象调用 getSeason() 方法。

```
var today = new Date();
document.write("The season is currently " + today.getSeason());
```

![](img/f14dd58a324d5464a114c30c1d4c4c9b_144_0.png)

尽管 getSeason() 方法在技术上仍不是 Date 类的成员，但 JavaScript 足够智能，会检查它是否存在于 prototype 成员列表中，这正是我们创建它的地方。



# 第五章：创建你自己的 JavaScript 类 131

> 一个类可以包含多个构造函数，只要每个构造函数的参数数量和类型（称为函数签名）是唯一的。

然后，我们可以通过定义更细化的车辆类型类来更具体一些。通过扩展 Vehicle 类，我们的子类会自动继承 Vehicle 类的属性和方法。

```
class LandVehicle extends Vehicle {
    // 陆地特定代码
    var Speed;
    var xPosition;
    var yPosition;
}
class WaterVehicle extends Vehicle {
    // 水上特定代码
    var Speed;
    var WaterDisplacement;
    var xPosition;
    var yPosition;
    var zPosition;
}
class AirVehicle extends Vehicle {
    // 空中特定代码
    var AirSpeed;
    var LandSpeed;
    var xPosition;
    var yPosition;
    var zPosition;
}
class SpaceVehicle extends Vehicle {
    // 太空特定代码
    var Thrust;
    var DistanceFromEarth;
}
```

我们可以继续定义从这些子类（LandVehicle, AirVehicle, WaterVehicle 和 SpaceVehicle）继承的类。其思想是每个子类是父类的一个更具体的版本。因此，LandVehicle 会有以下子类：

- Car（汽车）
- Train（火车）
- Bus（公共汽车）
- Truck（卡车）

> 你知道吗？

#### 接口的故事

ECMA，JavaScript 2.0 规范的设计者，最初计划在规范中包含一个名为 *接口* 的面向对象编程概念，但它在最后一刻被放弃了。接口允许你定义一组标准的方法名称和参数列表，而无需为它们提供具体代码。然后，一个类可以声明：“我支持以下接口……”；这将提供一种可靠的方式来了解该类支持哪些方法。

假设你定义了一个名为 DoorLock 的接口，它包含两个方法：Lock() 和 Unlock()。我们知道 Car 类实现了 DoorLock 接口，所以我们确信 Car 对象也拥有 Lock() 和 Unlock() 方法。请注意，Car 不是 DoorLock 的一种类型，因此不应建立父子关系（一种通过继承创建的关系）。

通过定义一个 DoorLock 接口，我们为需要定义门锁活动的类（如 Car 类和 House 类）创建了一组标准方法。

Car 是 LandVehicle 的一种更具体的类型，而 LandVehicle 又是 Vehicle 的一种更具体的类型。如果我们想进一步定义 Car，例如，我们可以创建从它继承的 SUV 和 SportsCar 类，以此类推。

让类以这种方式继承显然有两个主要好处。第一个是代码重用的能力。我们早在 Vehicle 类中就定义了一个构造函数。

```
function Vehicle (maker, price, color) {
    this.Maker = maker;
    this.Price = price;
    this.Color = color;
}
```

假设没有子类为自己定义构造函数，所有 Vehicle 类的后代都可以使用原始的 Vehicle 构造函数。

```
class Vehicle {
    var Maker;
    var Price;
    var Color;

    function Vehicle (maker, price, color) {
        this.Maker = maker;
        this.Price = price;
        this.Color = color;
    }
}
```

```
class LandVehicle extends Vehicle {
    // 陆地特定代码
    var Speed;
    var xPosition;
    var yPosition;
}
```

```
class Car extends LandVehicle {
    // 汽车特定代码
    var Model;
    var Year;
}
```

```
// Car 继承了 Vehicle 构造函数
var myCar : Car = new Car ("Ford", 19500, "Blue");
myCar.Model = "Focus";
myCar.Year = 2002;
myCar.Speed = 32;
```

```
// Car 继承了 Vehicle 的属性
document.write ("Vehicle class properties: " + myCar.Maker + "<br>");

// Car 继承了 LandVehicle 的属性
document.write ("LandVehicle class properties: " + myCar.Speed + "<br>");

// Car 也有自己的属性
document.write ("Car class properties: " + myCar.Model + "<br>");
```

正如你在图 5-1 中看到的，即使 Car 类本身只有两个属性，它确实继承了其所有父类的所有属性。

使用继承的另一个好处是计算机极客们喜欢称之为 *多态性* 的东西。本质上，一个定义为 Vehicle 数据类型的变量可以包含从 Vehicle 派生的任何对象（如 LandVehicle 或 Car）。这允许程序在无需知道或关心对象确切类型的情况下对对象进行操作。如果它能对父对象执行操作，那么同样的操作也可以对任何子对象执行。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_153_0.png)

也许最好的演示是用我们自己定义的数字类型，我们称之为 SuperNumber。

```
class SuperNumber extends Number {
    override function toString() {
        return super.toString() + " !!!!";
    }
}
```

普通 Number 类和 SuperNumber 类之间唯一的区别是，当用户调用 toString() 函数时，SuperNumber 会在数字末尾附加四个感叹号。

一旦我们定义了 SuperNumber，我们就可以像使用普通数字一样使用它。任何处理 Number 的函数都能够处理 SuperNumber，这是由于继承关系。甚至现有的算术运算符也无需修改就能处理这些变量。

```
var x : SuperNumber = new SuperNumber(13);
var y : SuperNumber = new SuperNumber(22);
```

```
var z : Number = x + y;
alert (z);
```

我们可以在这里看到程序的结果。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_154_0.png)

> 这幅插图描绘了当兼容 JavaScript 2 的浏览器最终发布时，我们预期会看到的结果。

#### 在静态成员和实例成员之间选择

我们在第 3 章讨论内置 Math 方法时研究了静态类成员的概念。基本上，*静态成员* 是指仅在类本身中定义，而不在该类派生的任何对象中定义的任何属性或方法。你甚至不需要定义特定类的对象就可以访问其静态成员。

静态成员使用 **static** 关键字定义。

```
class Books {
    static const MAX_WIDTH = 8.5;
    static const MAX_HEIGHT = 11;
    static const MAX_WEIGHT = 10;
    var title;
    var author;
    var page_count;
}
```

在上面定义的 Books 类中，我们定义了三个静态成员。它们恰好被定义为常量，但变量甚至函数也可以定义为静态的。为了访问它们，我们通过 Books 类本身进行调用，而不是通过基于 Books 创建的任何对象。

```
alert (Books.MAX_HEIGHT);
```

![](img/f14dd58a324d5464a114c30c1d4c4c9b_154_1.png)

# 如何用 JavaScript 做任何事

![](img/f14dd58a324d5464a114c30c1d4c4c9b_155_0.png)

*这幅插图描绘了当兼容 JavaScript 2 的浏览器最终发布时，我们预期会看到的结果。*

*实例成员* 是指任何非静态的成员。实例成员通过已创建的对象进行访问，不能直接使用类来访问。

```
var myBooks = new Books();
myBooks.title = "How To Do Everything With a Pencil";
myBooks.author = "Mary Major";
```

在此代码中，title 和 author 都是实例成员，只能通过基于 Books 类的对象（myBooks）访问，而不能通过类本身访问。

#### 将类成员设为公共或私有

面向对象编程中的另一个常见任务是定义无法从类外部访问的成员。这主要用于安全性和数据完整性。成员使用 **private** 关键字设为私有，使用 **public** 关键字设为公共。默认情况下，未明确指定为私有或公共的成员是公共的。

```
class Car {
    private var Make : String;
    private var Model : String;
    private var Year : Integer;
    private var Color : String;

    public function setMake (value) : Void {
        this.Make = value;
    }
    public function setModel (value) : Void {
        this.Model = value;
    }
    public function setYear (value) : Void {
        this.Year = value;
    }
    public function setColor (value) : Void {
        this.Color = value;
    }
}
```

在此代码中，Car 类的所有属性都被定义为私有。这意味着它们不能从类外部访问。尝试执行以下操作将导致错误。

```
var myCar = new Car();
myCar.Make = "Mercedes";
```



要设置属性，我们必须调用自己创建的公开方法。以下代码将生效。

```javascript
var myCar = new Car();
myCar.setMake("Mercedes");
```

请注意，我们创建的 Car 类使得读取属性值变得不可能。在现实世界中，该类还将包含许多函数来检索这些值。

显然，关于 JavaScript 中的类还有更多内容需要学习，包括 getter 和 setter、包和命名空间。但这些主题超出了本章以及本书的范围。如需更多关于类的信息，请查阅 Mozilla 网站上的官方 JavaScript 2.0 规范，网址为 http://www.mozilla.org/js/language/js20/core/classes.html。

在下一章中，我们将开始学习如何应用前四章所学的概念，因为我们将把 JavaScript 应用于网页中。我们将学习一些关键的 HTML 标签，以及 JavaScript 在网页中应放置的位置。

## 第二部分

## 构建支持 JavaScript 的网站

![](img/f14dd58a324d5464a114c30c1d4c4c9b_158_0.png)

## 第 6 章

## 在网页中嵌入 JavaScript

![](img/f14dd58a324d5464a114c30c1d4c4c9b_160_0.png)

#### 如何用 JavaScript 做一切

#### 如何...

- 理解基本的 HTML 结构
- 使用 `<script>` 将 JavaScript 添加到网页
- 使用 `<noscript>` 为不支持脚本的浏览器提供替代内容
- 加载外部 JavaScript 文件
- 使用超链接调用 JavaScript

到本书的这一部分为止，我们一直专注于 JavaScript 的编程语法——这些是构成语言基本要素的语句和定义。正如你所看到的，JavaScript 具有许多特性，使其成为许多任务的理想语言，而其最强大的特性之一就是它能够集成到各种其他环境中。

JavaScript 版本存在于许多不同的环境中：

- 用于 Microsoft IIS Web 服务器的应用程序服务器页面（ASP）语言（支持的几种语言之一）
- 用于 Netscape/iPlanet Web 服务器的服务器端 JavaScript（SSJS）
- 用于其他 Web 服务器的服务器端编程语言
- 用于 Adobe Acrobat PDF 文档的嵌入式语言
- 用于 Macromedia Flash 文件的嵌入式语言（ActiveScript）

但即使在今天，距离它首次推出近 10 年后，JavaScript 最大的成功仍然是作为网页的嵌入式编程语言。它几乎得到了当今所有网络浏览器的支持——在全球数亿台 PC 上都有安装。在本章中，我们将研究如何在 HTML 页面中嵌入 JavaScript 以及一些基本的文本格式化技术。

#### 理解基本的 HTML 结构

超文本标记语言（Hypertext Markup Language），简称 HTML，是网页的编写语言。HTML 被称为标记语言，因为它使用一组预定义的标签或*标记*来向 Web 浏览器提供格式化和其他指令。

例如，以下示例包含许多 HTML 标记标签：

```html
<font size="2"><b>现在是时候</b>让所有
好人<u>前来援助</u><i>他们的政党</i>。</font>
```

如你所见，HTML 标记标签总是包含在尖括号（< 和 >）中。大多数 HTML 标签都有一个开始标签（例如粗体文本标签 `<b>`）和一个结束标签（如 `</b>`），尽管此规则有一些例外。

以下展示了带有上述标记的 HTML 文档在标准 Web 浏览器中的显示效果。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_162_0.png)

> **注意**
>
> 结束标签总是以正斜杠字符（/）开始，后跟相关开始标签的名称。例如，如果开始标签是 `<font>`，则结束标签必须是 `</font>`。

关于 HTML 主题的书籍已经有很多了。实际上，准确地说，可以说关于这个主题的书足够填满不止几个书架（甚至书柜）。我在本章及后续章节的目标并不是真正教授 HTML 的来龙去脉。但是，由于 JavaScript 程序在很大程度上依赖于浏览器内部发生的事情（框架、表单、浏览器事件等），如果不首先理解与之相关的 HTML，就不可能理解 JavaScript 的运作方式。作为参考，附录 A 列出了所有 HTML 4.01 标签，并简要描述了它们的用途。

> **注意**
>
> 主要的浏览器制造商（Microsoft 和 Netscape）在某些情况下添加了自己的标签，因此它们的列表可能与附录 A 中的官方列表不匹配。

##### 你知道吗？

###### 为什么 XML 和 XHTML 是未来的趋势

虽然人类可以使用 Web 浏览器轻松读取 HTML 文档，但计算机本身很难从网页中提取特定数据。例如，要创建一个能够可靠地从所有航空公司网站下载每日航班时刻表的应用程序将非常困难。

XML（可扩展标记语言）是通过互联网传输计算机数据的理想语言。HTML 是一种极其灵活的标记语言，只有极少数强制性元素或属性，而 XML 则有一套严格的格式化规则。程序员可以通过创建 XML 架构或 DTD 来对单独的文档类型施加额外的规则。XML 是互联网上数据格式化的新标准语言，也是许多 Web 服务计划的基础，包括 Sun ONE 和 Microsoft .NET。

HTML 的一个新版本已经被创建出来，它允许 Web 文档同时也是有效的 XML，称为 XHTML。事实上，万维网联盟（W3C）已经停止开发 HTML 标准（版本 4.01），并一直在努力制定 XHTML 标准——版本 1.0 和 1.1 已经发布。

有关 XHTML 标准的更多信息，请访问 W3C 网站，网址为 http://www.w3c.org/markup。

此外，如第 1 章所述，一组特殊的标签在 HTML 中表示注释：`<!--` 表示注释文本的开始，`-->` 表示结束。注释可以作为有用的文档或作者注释，例如：

```html
<!-- Survey.html
     Purpose: To gather visitor opinions on this site
     Author: John Q. Doe
-->

<!-- Copyright 2003, Scott J. Duffy Incorporated
     All rights reserved. -->
```

如你所见，注释可以跨越多行。所有出现在 HTML 注释标记内的文本都会被浏览器忽略，不会显示在主显示区域中。

##### 警告

> 别忘了，用户可以在大多数浏览器中通过选择菜单栏上的“查看 | 源代码”来查看底层的 HTML 代码，因此你的注释不会完全保密。

###### "Officially Deprecated" 的含义

万维网联盟（W3C）是创建和维护包括 HTML 在内的多个重要互联网规范的组织，它指出许多 HTML 标签已*弃用*。

指出一个标签已弃用是一种委婉的说法，表示在规范的未来版本中可能会取消对该标签的支持。W3C 希望鼓励网页开发者采用另一种方法来代替，例如使用层叠样式表（CSS）来定义字体。

然而，考虑到诸如 `<font>`、`<center>` 和 `<u>` 等标签的广泛使用，主要的浏览器制造商不太可能很快放弃对它们的支持。

#### 构建 HTML 文档

HTML 的优势之一在于其简单性：使用几个基本标签就可以很容易地构建一个网页。构建网页有三个基本要素：

1.  每个 HTML 文档都必须以 HTML 开始标签（`<html>`）开头，并以 HTML 结束标签（`</html>`）结尾。唯一的例外是 `<!DOCTYPE>` 或 `<?xml?>` 声明语句，它们被放置在 HTML 标签之前。（`<?xml?>` 声明用于定义符合 XHTML 的文档，这超出了本书的范围。但是，我们将在下一节中讨论 `<!DOCTYPE>`。）
2.  然后 HTML 文档被分为两部分：head 和 body。head 部分用于定义文档标题、描述性关键词、样式表和 JavaScript 函数。
3.  body 部分用于放置文档的内容。这通常是纯文本（句子和段落），并用一些格式化 HTML 标签（如 `<b>`、`<i>` 和 `<p>`）进行标记。

```html
<html>
</html>
```

```html
<html>
    <head>
        <title>How to Do Everything with JavaScript</title>
    </head>
</html>
```

```html
<html>
    <head>
```



 ```
<title>How to Do Everything with JavaScript</title>
</head>
<body bgcolor="white">
    <h1>A typical document header</h1>
    <p>The start of a paragraph.</p>
    <p><b>Our second paragraph.</b></p>
</body>
</html>
```

诚然，我们示例中的网页相当简单，但即使是有数百行代码的网页，也是由三个简单的标签开始的：`<html>`、`<head>`和`<body>`。

> 养成习惯，在创建所有 HTML 文档时使用小写标签名、正确嵌套的标签以及正确引用的属性值。当你想要开始创建 XHTML 1.0 文档时，这将大有裨益，因为 XHTML 有非常严格的规则。

你可能已经熟悉 HTML 的基础知识。如果不熟悉，由于将 HTML 教程压缩到一章中是不可行的，我在本章末尾附上了一份有用的网站列表。

#### 使用 <!DOCTYPE> 指示文档类型

向浏览器（或任何其他读取你的 HTML 文件的应用程序）指示你的网页是用哪个版本的 HTML 编写的，只有一种方式：`<!DOCTYPE>`。直到几年前，这个标签还被浏览器完全忽略。但最新版本的浏览器会查找此代码，以确定使用哪套规则来解释网页。

符合 HTML 4.01 规范的 HTML 文档会在页面的第一行（甚至在 `<html>` 标签之前）使用以下 `<!DOCTYPE>`：

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
    "http://www.w3.org/TR/html4/loose.dtd">
```

如果浏览器遇到使用此 `<!DOCTYPE>` 标签的网页，它将期望文档其余部分包含有效的 HTML 4.01 Transitional 代码。过渡性 HTML 包含所有已弃用的标签（如 `<font>`）。还有一种称为 Strict 的 HTML 版本，不包含已弃用的标签，另一种称为 Frameset，允许创建浏览器框架。（我们将在第 10 章中介绍浏览器框架。）

如果我们想使用不同版本的 HTML，比如 XHTML（符合 XML 标准的 HTML 版本），我们会使用不同的 `<!DOCTYPE>`，如下所示：

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```

当浏览器遇到此 `<!DOCTYPE>` 时，它知道将内容视为 XHTML 1.0 Transitional。根据浏览器的不同，其处理方式可能与处理 HTML 4.01 代码的方式略有不同。

#### 添加标题并定义文档关键词

HTML head 元素包含有关当前文档的信息，例如其标题、关键词以及其他不被视为内容的元数据。HTML `<title>` 标签用于为文档指定标题，在 HTML 4.01 中这是强制性的。

```
<html>
    <head>
        <title>This is the document title</title>
    </head>
    <body></body>
</html>
```

`<title>` 标签的内容通常显示在窗口的标题栏中，如下所示：

![](img/f14dd58a324d5464a114c30c1d4c4c9b_166_0.png)

此外，你可以指定一些关键词，这将使互联网搜索引擎更容易找到你的网站。关键词和网页的简要描述可以使用 `<meta>` 标签来指定。例如，如果你有一个关于异国宠物的页面，你可能有以下 `<meta>` 标签：

```
<meta name="description" content="Articles, pictures, and stories about exotic pets">
<meta name="keywords" content="exotic pets, reptiles, amphibians, frog, toad, salamander, newt, siren, lizard, iguana, gecko, monitor, chameleon, dragons, turtles, tortoises, leopard, butterfly, butterflies, moth, bees, flies, stick insects, beetles, wasps, hornet, roaches, ants, cricket, grasshopper, tarantula, scorpion, centipede, millipede">
```

当用于指定网页描述和关键词时，`<meta>` 标签有两个属性：name 和 content。在上面的代码中，第一个 `<meta>` 标签设置了网页的描述——通常是一两句话，搜索引擎常用来向潜在访问者准确展示从此页面可以期望获得什么。

示例中的第二个 `<meta>` 标签定义了一些*关键词*——用逗号分隔的单词或短语，帮助搜索引擎为页面建立索引。一些互联网搜索引擎会给予带有这些 `<meta>` 标签的网页比没有这些标签的相同页面更高的排名。

#### 使用 HTML 元素格式化文本

HTML 提供了许多元素来帮助网页开发者格式化和设置文本样式。这些标签大致分为两类：*短语元素*和*字体样式元素*。短语元素是用于结构化文本的标签。这些元素呈现给用户的方式取决于浏览器。字体样式元素是指定文本特定字体属性的标签。由于字体样式属性 fairly 具体，开发者可以更确信浏览器向用户呈现文本的方式。

以下是 HTML 4.01 中的短语元素：

- **`<abbr>`** 表示缩写形式
- **`<acronym>`** 表示首字母缩略词
- **`<cite>`** 表示引用或参考其他来源
- **`<code>`** 指定计算机代码片段
- **`<dfn>`** 表示术语的定义实例
- **`<em>`** 表示强调；通常显示为斜体文本
- **`<kbd>`** 表示用户要输入的文本
- **`<samp>`** 表示程序、脚本等的示例输出
- **`<strong>`** 表示更强的强调；通常显示为粗体文本
- **`<var>`** 表示变量或程序参数的实例

同样，这些元素中的每一个都指示其包含的文本类型，但仅给浏览器如何处理它们提供提示。

以下标签是 HTML 4.01 的字体样式元素：

- **`<b>`** 粗体文本
- **`<big>`** 比正常文本更大
- **`<i>`** 斜体文本
- **`<s>`** 删除线文本（正式弃用）
- **`<small>`** 比正常文本更小
- **`<strike>`** 删除线文本；与 `<s>` 相同（正式弃用）
- **`<tt>`** 电传打字机或等宽文本
- **`<u>`** 下划线文本（正式弃用）

在绝大多数 HTML 页面中，短语元素并未被使用。许多网页设计师更喜欢明确地为其页面设置字体和样式。除了不同浏览器如何呈现这些标签的不确定性之外，使用这种预定义的文档结构元素会限制设计师的设计选择。

数以亿计的网页仅使用此处列出的 HTML 元素来设置其页面上文本的样式。例如，以下 HTML 代码创建了一个网页，使用了本章到目前为止讨论的许多样式标签。

```
<html>
    <head><title>Sample document</title></head>
    <body>
    <h1>Traveling to the Caribbean</h1>

    <p><b>Barbados</b> - Barbados is a lovely island, with
    <i>wonderful weather</i> and a <i>constant cool breeze</i>. The
    locals are friendly, and one can clearly see that a British
    influence still exists, even today.</p>

    <p><b>St. Lucia</b> - St. Lucia is a lush, tropical paradise.
    Fewer tourists tend to visit St. Lucia than some of the other
    islands, which means it is easier to explore the local way
    of life.</p>

    <p><b>Bahamas</b> - Bahamas is <strike>frequently visited
by</strike> <u>a popular spot for</u> Americans. The islands have a
number of casinos, the most spectacular of which is the <i>Atlantis
Hotel on Paradise Island</i>. The rumor is that one of their hotel rooms
goes for <big>$40,000 a night</big>, which is about $39,800 more than
most people can afford to spend on a place to sleep.</p>
    </body>
</html>
```

如下面的屏幕截图所示，HTML 元素对文本进行样式设置，使输出更易于阅读。应该为粗体、斜体或删除线的文本完全按照预期呈现。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_169_0.png)

#### 使用样式表格式化文本

多年来，网页设计师一直希望有一种更精确的方式来设计网页样式和布局，类似于桌面出版软件长期提供的工具。终于，样式表出现了，它缓解了设计师对网页样式的大部分担忧。

> *W3C 层叠样式表主页是 http://www.w3.org/Style/CSS。毫不奇怪，该页面本身就是样式表如何用于格式化网页的绝佳示例。*

样式表，有时也称为层叠样式表（简称 CSS），对网页开发者有诸多好处。它们提供了

- 将样式与内容分离的能力
- 将单一样式应用于整个网站的能力
- 更精细的样式控制能力
```

##### 样式表

指定精确布局定位的能力
- 通过 JavaScript（也称为动态 HTML）编写脚本和动态更改样式的能力
- 根据浏览器环境（例如 PC 与手机）指定不同样式的能力

事实上，HTML 规范正逐渐淘汰上一节中列出的用于定义样式的 HTML 标签，转而支持样式表。使用样式表定义文档样式是该语言的现在与未来。

样式表在 HTML `<style>` 元素内定义，通常在文档头部区域中定义。

```html
<html>
  <head>
    <title>HTML 样式表</title>
    <style type="text/css">
    // 样式表内容放在这里
    </style>
  </head>
  <body>
    <h1>加勒比海之旅</h1>

    <p><b>巴巴多斯</b> - 巴巴多斯是一个可爱的岛屿，拥有
    <i>宜人的天气</i> 和 <i>持续的凉爽微风</i>。当地人
    <!-- 等等 -->
  </body>
</html>
```

对于我们示例中的 HTML 文档，我们可以定义一个自定义样式表，替换掉之前使用的一些格式。

```css
.island {font-weight: bold}
.highlight {font-style: italic}
.underlinethis {text-decoration: underline}
.bigmoney {font-size: larger}
```

事实上，你可以为我们这个有点无聊的文档添加一些非常有趣的文字效果，如下例所示。一旦样式表定义完成，你只需修改 HTML 以使用这些样式即可。

# 152 如何用 JavaScript 做一切

```html
<html>
    <head>
        <title>示例文档</title>
        <style type="text/css">
            .island {
                color: white;
                background-color: black;
                font-weight: bold
            }
            .highlight {
                font-style: italic;
                background-color: yellow
            }
            .underlinethis {
                text-decoration: underline overline
            }
            .bigmoney {
                color: green;
                font-size: xx-large
            }
        </style>
    </head>
    <body>
        <h1>加勒比海之旅</h1>

        <p><span class="island">巴巴多斯</span> - 巴巴多斯是一个可爱的岛屿，拥有 <span class="highlight">宜人的天气</span> 和 <span class="highlight">持续的凉爽微风</span>。当地人友好，人们可以清楚地看到，即使在今天，英国的影响依然存在。</p>

        <p><span class="island">圣卢西亚</span> - 圣卢西亚是一个郁郁葱葱的热带天堂。游客往往比去其他岛屿少，这意味着更容易探索当地的生活方式。</p>

        <p><span class="island">巴哈马</span> - 巴哈马是 <strike>经常被</strike> <span class="underlinethis">美国人</span> <span class="underlinethis">喜爱的热门地点</span>。这些岛屿有许多赌场，其中最壮观的是 <span class="highlight">天堂岛上的亚特兰蒂斯酒店</span>。有传言说他们的一间酒店客房每晚售价 <span class="bigmoney">$40,000</span>，这比大多数人能负担得起的住宿费用高出约 $39,800。</p>
    </body>
</html>
```

生成的网页可能不会赢得任何设计奖项，但你可以看到样式表让你能做到普通 HTML 做不到的事情。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_172_0.png)

显然，样式表远不止我在这一短节中能向你展示的那一点皮毛。我在本章末尾列出了几个可以了解更多样式表信息的网站。我们还将在第 12 章重新讨论这个主题。

#### 使用 `<script>` 将 JavaScript 添加到网页

既然你已经了解了一些基本的 HTML 格式元素，现在是时候将它们与 JavaScript 的使用联系起来了。HTML `<script>` 标签允许网页开发者将 JavaScript 命令嵌入到他们的网页中。虽然为了编程效率，最好将单个页面上的脚本数量保持在最低限度，但一个网页文档可以包含多少个 `<script>` 部分是没有限制的。

当你处理嵌入式脚本内容时，HTML `<script>` 元素通常只接受两个属性：`language` 和 `type`。`language` 属性是为了向后兼容而存在的。JavaScript 是所有主要网页浏览器支持的唯一脚本语言，因此如果省略此属性，“JavaScript” 将是默认值。

#### 如何用 JavaScript 做一切

`type` 属性指定嵌入式脚本的 MIME 类型，对于我们来说就是 “text/javascript”。MIME 是一种通过互联网描述文件内容的标准方式，例如 “text/plain” 和 “image/gif”。这解决了 20 年前 MS-DOS 遗留的三个字母文件扩展名（.htm 或 .txt）的问题。

MIME 标准起源于电子邮件系统，它允许 Web 服务器告诉浏览器如何解释发送过来的比特流。例如，Web 浏览器知道文件 http://www.example.com/ 是 HTML 文档的唯一方法就是通过其 MIME 类型。

```javascript
<script language="JavaScript" type="text/javascript">
    var a = 1;
    var b = 2;
    var c = a + b;
    document.write (c);
</script>
```

在本章后面，我们将探讨 `<script>` 标签的另一个用途，即处理外部 JavaScript 内容。

#### 使用 `<noscript>` 为不支持脚本的浏览器提供内容

即使在今天，随着网页浏览器和网页编程语言的所有技术进步，仍然不是每个浏览器都支持 JavaScript。例如，许多手机提供互联网接入，但它们在屏幕尺寸、颜色、音频和脚本功能方面受到严重限制。还有一些 PC 上的网页浏览器（如嵌入在 Microsoft Word 中的那个）不支持 JavaScript 等高级功能。并且一些 JavaScript 之前的浏览器仍在使用，例如 Netscape Navigator 1.0。

然而，确实，支持非 JavaScript 兼容设备现在不如 1995 年 JavaScript 刚问世时那么重要了。但随着时间的推移，计算机操作系统和硬件设备的种类不断增加，为某些用户提供替代内容可能再次变得重要起来。

HTML `<noscript>` 标签用于向其浏览器不支持 JavaScript 的用户提供内容。它之所以有效，是因为启用 JavaScript 的浏览器会忽略 `<noscript>` 标签之间的任何内容，例如：

```html
<html>
    <head>
        <title>JavaScript 测试</title>
    </head>
    <body>
        <h1>for 循环</h1>
        <script language="JavaScript" type="text/javascript">
        <!-- // 开始
        var Fahrenheit;
        for (var Celsius = 10; Celsius <= 60; Celsius = Celsius + 5) {
            document.write (Celsius + "&deg;C = ");
            Fahrenheit = (Celsius * 9/5) + 32;
            document.write (Fahrenheit + "&deg;F<BR>");
            if (Fahrenheit > 100) {
                // 这里变得越来越热了
                break;
            }
        }
        // 结束 -->
        </script>
        <noscript>
        您必须使用支持 JavaScript 的浏览器
        才能访问此网页。
        </noscript>
    </body>
</html>
```

此代码将向使用启用 JavaScript 的浏览器的用户显示以下输出。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_174_0.png)

然而，使用不支持 JavaScript 的浏览器的用户将看到此消息。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_175_0.png)

JavaScript 没有同时输出到屏幕的唯一原因是包围脚本的 HTML 注释标签 `<!--` 和 `-->`。

在 `<noscript>` 标签内，你可以选择简单地告知用户需要启用 JavaScript 的浏览器。但你也可以为 JavaScript 提供替代内容，如本例所示：

```html
<noscript>
    10°C = 50°F <BR>
    15°C = 59°F <BR>
    20°C = 68°F <BR>
    25°C = 77°F <BR>
    30°C = 86°F <BR>
    35°C = 95°F <BR>
    40°C = 104°F <BR>
</noscript>
```

这将允许使用各种浏览器和硬件设备的用户正常查看你的网站。当然，并不总是能够用纯 HTML 文本替换 JavaScript 内容。



#### 加载外部 JavaScript 文件

JavaScript 不一定非要嵌入在 HTML 文件中。通常，将 JavaScript 放在一个文件中，然后让多个 HTML 文件导入使用会更加方便。采用这种技术，修改 JavaScript 会更容易，因为你不需要逐个修改每个 HTML 文件。

首先，你必须有一个仅包含 JavaScript 的文本文件。假设在 Web 服务器上存在以下文件，名为 sample.js。

```
// SAMPLE.JS
//
// isFloat() function:
//   Checks a string to see if it contains a
//   floating-point number; returns true or false
//
function isFloat (s)
{
    // Format accepts "9", "9.", "9.9", and ".9"
    var reFloat = /^((\d+(\.\d*)?)|(\d*\.\d+))$/;

    return reFloat.test(s)
}
```

> .js 文件扩展名在 Windows 系统中通常用于表示该文件包含 JavaScript，不过也可以使用任何扩展名（例如 .txt）。

我们使用 HTML &lt;script&gt; 标签的 src 属性来导入外部 JavaScript 文件。

```
<html>
    <head>
        <title>JavaScript Test</title>
        <script language="javascript" src="sample.js"></script>
    </head>
    <body>
        <h1>Check for a Floating Point Number</h1>

        <script language="JavaScript" type="text/javascript">
            document.write("Is \"12.345\" a float?  " + 
                isFloat("12.345") + "<br><br>");
            document.write("Is \"Twelve\" a float?  " + 
                isFloat("Twelve") + "<br><br>");
        </script>
    </body>
</html>
```

然后，我们可以在网页中另一个 &lt;script&gt; 部分调用在外部 JavaScript 文件中定义的 isFloat() 函数。通过这种方式，isFloat() 函数可以轻松地在多个网页之间共享。

> **注意**
>
> 导入外部 JavaScript 文件的 HTML &lt;script&gt; 标签不能同时包含 JavaScript。它们必须是空的。

导入外部 JavaScript 文件的结果如图 6.1 所示。

#### 使用超链接调用 JavaScript

并非所有 JavaScript 都在网页加载后立即执行。我们将在第 9 章中介绍* Web 浏览器事件*，它允许 JavaScript 响应用户的操作来运行。另一种响应用户事件调用 JavaScript 的方法是将其作为超链接的目标。

```
<A HREF="javascript:alert('Hello')">Click me</A>
```

![Figure 6-1](img/f14dd58a324d5464a114c30c1d4c4c9b_177_0.png)

**图 6-1** 在外部 JavaScript 文件中定义的函数可以在 HTML 页面的其他地方调用。

## 第 6 章：在网页中嵌入 JavaScript

将此 HTML 加载到 Web 浏览器中会显示一个可点击的超链接，标题为"Click me"。当用户点击该链接时，会弹出一个 JavaScript alert() 消息框，显示"Hello"。诀窍在于 HREF URL 中特殊的"javascript:"前缀。这告诉浏览器，我们真正想要做的是调用 JavaScript 命令。

多个 JavaScript 命令可以附加在一个字符串中，只要用分号分隔即可。

```
<A HREF="javascript:alert('Hello');alert('Goodbye')">Click me</A>
```

更常见的是，JavaScript 超链接用于调用预定义的函数，而不是将一个或多个 JavaScript 语句嵌入到 HREF 属性值本身中。

```
<A HREF="javascript:submitform()">Click here to submit the form</A>
```

在这个例子中，当用户点击标记为"Click here to submit the form"的超链接时，JavaScript 将调用一个名为 submitform() 的函数，我们假设它在网页的其他地方定义。

在下一章中，我们将研究 Web 开发人员在创建跨平台兼容的 JavaScript 时面临的问题。在一个 Web 浏览器中工作的 JavaScript 程序不一定能在另一个浏览器中工作，因为有数十种浏览器、硬件平台和操作系统的组合。了解如何解决这些差异在实际的 Web 开发中非常重要。

#### 了解更多关于本章主题的内容

以下是一些可以了解更多关于 HTML 和层叠样式表（CSS）的网站：

- Webmonkey HTML 基础教程：http://hotwired.lycos.com/webmonkey/teachingtool
- SitePoint：http://www.webmasterbase.com
- Web Design Group CSS 参考：http://www.htmlhelp.com/reference/css
- Dave Raggett 的 CSS 入门：http://www.w3.org/MarkUp/Guide/Style

"小爱同学，讲个笑话。"
"小爱同学，明天天气怎么样？"
"小爱同学，帮我订个闹钟。"
这些每天都在说的话，你知道背后是哪位"最强大脑"在默默支撑吗？它就是小米公司拥有知识产权、从0到1自研的、拥有自主知识产权的AI"大模型"——MiLM。

## AI 大模型

大模型，其实是指拥有超大规模参数（通常在百亿级以上）的深度神经网络模型。你可以把它想象成一个"超级学霸"的大脑。普通的人工智能可能只精通某一特定领域，比如专门下棋或者专门识别人脸。而拥有"大模型"的人工智能，则拥有更通用的"智慧"和更强大的学习、推理及生成能力。

## MiLM 大模型的"大"在哪里

1.  **参数规模巨大**：这是"大模型"最直观的特征。MiLM 拥有超过 100 亿的庞大参数量，这使得它能够理解和处理极其复杂的语言信息和逻辑关系。
2.  **算力支撑强大**：训练这样一个超大规模模型，背后需要消耗海量的计算资源。这不仅需要顶级的 GPU 集群，还需要极其高效、先进的分布式训练框架和优化算法。小米公司投入了巨大的研发资源，确保 MiLM 能够在海量数据中高效学习。
3.  **训练数据海量**：大模型的知识来源于"海量"的训练数据。MiLM 的训练数据涵盖了多种文本类型，包括但不限于网页、书籍、新闻、对话等，总量达到数万亿（Tokens）。通过在这些海量文本中进行大规模预训练，模型才能习得丰富的语言模式、知识体系和推理能力。

# 第 7 章

## 创建适用于所有浏览器的脚本

![Chapter 7 Image](img/f14dd58a324d5464a114c30c1d4c4c9b_180_0.png)

#### 如何……

-   理解浏览器差异
-   检测用户正在运行哪种类型的浏览器
-   查询文档模型
-   遵循 Web 标准
-   编写跨浏览器代码

在 JavaScript 开发的早期，处理不同浏览器厂商和版本之间的差异是一项艰巨的任务。毕竟，有些浏览器根本不支持 JavaScript（如 Netscape 1.0）。即使你有一个支持 JavaScript 的浏览器，不同浏览器之间的底层文档模型（DOM）也不同，这意味着 JavaScript 错误很常见。

开发能在每个浏览器中正确运行的 JavaScript 代码之所以困难，主要是由以下几个因素造成的：

-   每隔几个月就有新的浏览器版本发布
-   浏览器公司之间在添加新功能方面的持续竞争
-   缺乏 HTML 或 JavaScript 标准

这花了一些时间，但随着 JavaScript 的稳定化，问题最终开始消失。随着用户逐渐升级到 4.0 及以上版本的浏览器，JavaScript 开发人员开发跨平台兼容代码的工作变得更加容易。

不幸的是，JavaScript 即将发生的一些变化将迫使 Web 开发人员再次开始为浏览器差异进行编码。导致这一新的不稳定时期的原因可能包括：

-   对 JavaScript 2.0 的支持不一致
-   每隔几个月就有新的 Web 浏览器版本发布（尤其是来自 Mozilla 的）
-   对新技术的 JavaScript 支持不一致，例如 XML 和 CSS

只有时间能告诉我们这些因素会给 Web 开发人员带来多少困扰。

#### 理解浏览器差异

根据最近的调查，Microsoft Internet Explorer (IE) 被大约 94% 的 Web 冲浪者使用。Netscape 和 Mozilla 的合计使用率约为 2%。剩下的 4% 分配给其他公司（如 Opera）的一部分，或因四舍五入而丢失。

这些数字在未来几个月和几年内可能会发生变化。美国最大的互联网服务提供商（ISP）最近宣布将开始使用 Netscape 作为其默认浏览器，这可能会对这些数字产生重大影响。

更仔细地查看最近的浏览器流行度统计数据，如表 7-1 所示，我们可以看到一半的冲浪者尚未升级为其首选 Web 浏览器的最新版本。

整整 54% 的 Web 冲浪者使用的浏览器不是 Microsoft 或 Netscape 的最新版本。因此，在创建过于依赖专有或最近添加的功能的 JavaScript 程序时要小心。不采取适当的预防措施就使用这些功能可能会导致相当一部分受众出现错误，即使该应用程序在你 PC 上安装的浏览器中运行正常。

#### 可能发生什么类型的错误？

在设计任何计算机程序时，重要的是要记住，尽管程序员尽力避免，错误仍然可能发生。对于在各种浏览器和操作系统中使用的 JavaScript 程序来说尤其如此。在开发 JavaScript 代码时，你可能会发现以下错误来源：

-   每个浏览器版本的文档对象模型（DOM）的差异
-   客户端计算机运行的是旧浏览器（如 Netscape 3.0），不支持某些 JavaScript 功能
-   客户端计算机上的某些技术被关闭，例如 cookies 或 Java
-   新的支持 Web 的技术，如手持设备、移动电话，甚至家用电器（如冰箱）

在本章中，我们将介绍一些避免这些类型错误的常用技术。

**表 7-1** 近期 Web 浏览器使用统计

| 浏览器 | 使用率 |
| :--- | :--- |
| IE 6 | 46% |
| IE 5 | 44% |
| IE 4 | 2% |
| Netscape 4 | 2% |
| Netscape 6, Netscape 7, Mozilla (合计) | 1% |
| 较旧的 IE | 不到 1% |
| 较旧的 Netscape | 不到 1% |

来源：TheCounter.com (http://www.thecounter.com)



#### 检测用户正在使用的浏览器类型

在较旧的浏览器中运行现代或复杂的 JavaScript 程序很可能会导致诸多问题。避免这类错误最简单的方法，或许是检测用户正在使用的浏览器类型，然后禁用程序的某些功能，或者提供替代代码，以略微不同的方式执行相同任务。

> **注意**
> 检测浏览器名称和版本信息的过程常被称为浏览器嗅探。正如寻血猎犬能探测到个体的独特气味，浏览器嗅探器也试图探测并返回浏览器软件的独特详情。

要检测浏览器制造商和版本号，我们将依赖 `navigator` DOM 对象。`navigator` 对象有多个方法和属性，但目前我们感兴趣的是 `appName`、`appVersion` 和 `userAgent` 这三个属性。

```
var browserString = navigator.appName;
var browserVersion = navigator.appVersion;
var browserAgent = navigator.userAgent;

alert(browserString);
alert(browserVersion);
alert(browserAgent);
```

![](img/f14dd58a324d5464a114c30c1d4c4c9b_183_0.png)

#### 指定 JavaScript 版本号

浏览器制造商最初的出发点是好的。网景（Netscape）和 IE 都允许开发者在 `<script>` 标签的 `language` 属性中指定 JavaScript 版本号。这可以防止脚本在不支持指定 JavaScript 版本的浏览器中运行。要创建一个仅在支持 JavaScript 1.2 的浏览器中运行的脚本，可以使用以下代码：

```
<script language="JavaScript1.2">
```

对于所有直到 1.5 版本的 JavaScript，都可以这样做。（JavaScript 版本号及其与浏览器对应关系的列表可以在第 1 章中找到。）
不幸的是，很少有 Web 开发者知道可以这样做，更少有人在创建跨浏览器脚本时实际使用这种技术。除此之外，这种方法也无法帮助开发者解决不同浏览器之间的 DOM 相关差异。
因此，尽管这项技术仍然可用，但不能依赖它来解决跨浏览器脚本问题。

对于网景 Web 浏览器（包括开源 Mozilla Web 浏览器），无论版本或操作系统如何，`navigator.appName` 属性总是返回相同的值。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_184_0.png)

对于微软 Internet Explorer，无论版本如何，`navigator.appName` 属性也返回一个可预测的值。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_184_1.png)

因此，如果你的网页需要根据访问者使用的浏览器显示不同的文本，你可以简单地查询 `navigator.appName` 属性，如下所示：

```
var browserString = navigator.appName;

if (browserString == "Netscape") {
    // 为 Netscape/Mozilla 执行某些操作
    document.write ("Long live the lizard.");

} else if (browserString == "Microsoft Internet Explorer") {
    // 为 Microsoft 执行某些操作
    document.write ("You will be assimilated.");

} else {
    // 浏览器不是上述两种主要浏览器之一
    document.write ("Why must you always be so different?");
}
```

然而，`navigator.appName` 提供的信息量极其有限。其他 `navigator` 属性提供更有用的信息。例如，

#### 如何用 JavaScript 做所有事

`navigator.appVersion` 属性提供更具体的浏览器版本信息。对于网景浏览器，该属性返回的字符串相当直接明了。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_185_0.png)

此截图来自在 Windows 98 上运行的 Netscape 7.0。为了让 Web 开发者更加困惑，Netscape 6 和 7 都将其版本号返回为 "5.0"。然而，Netscape 并未推出第 5 版（版本号从 4.8 直接跳至 6.0），因此此版本号并不准确。

类似地，微软 Internet Explorer 也在 `navigator.appVersion` 字符串中返回其版本信息，如下所示从 Microsoft Internet Explorer 6.0 获取的快照所见。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_185_1.png)

较新版本的微软 Web 浏览器总是将版本号报告为 4.0 兼容。然而，实际版本号嵌入在同一字符串的后面部分（在本例中为 MSIE 6.0）。

Mozilla 1.x、Netscape 6.0 和 Netscape 7.0 浏览器都基于相同的源代码，因此它们的行为非常相似。如果你需要从这些浏览器中获取精确的浏览器名称和版本号，可以查询 `navigator` 对象的 `userAgent` 属性。从下面的示例中可以看出，它包含一些非常具体的版本号信息，甚至精确到浏览器编译的确切日期。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_185_2.png)

## 第 7 章：创建在所有浏览器中都能工作的脚本

利用这三个属性，我们可以创建一个 JavaScript 函数来检测用户正在运行的精确浏览器类型：

```
function getBrowserInfo() {
    // 定义变量以包含结果
    var browserName = navigator.appName;
    var browserVersionNum = parseFloat(navigator.appVersion);
    var browserAgent = navigator.userAgent;

    // 布尔型（true 或 false）变量用于检测浏览器类型
    var is_IE = (browserAgent.indexOf("MSIE") != -1);
    var is_NN = (browserName.indexOf("Netscape") != -1);

    // 根据浏览器类型，获取版本号
    if (is_NN) {
        if (browserVersionNum >= 5.0) {
            var tempStart = browserAgent.indexOf("Netscape/");
            if (tempStart == -1) {
                // 未找到 "Netscape/"；一定是 Mozilla
                tempStart = browserAgent.indexOf("rv:");
                tempStart += 3;
                browserName = "Mozilla"
                var tempEnd = browserAgent.indexOf(")", tempStart);
            } else {
                // 找到了 "Netscape/"；一定是 Netscape Gecko
                tempStart += 9;
                var tempEnd = browserAgent.length;
            }
            var browserVersion =
                browserAgent.substring(tempStart, tempEnd);
        } else {
            // 版本 < 5.0；一定是旧版 Netscape
            var browserVersion = browserVersionNum;
        }
    } else if (is_IE) {
        var tempStart = browserAgent.indexOf("MSIE");
        tempStart += 5;
        var tempEnd = browserAgent.indexOf(";", tempStart);
        var browserVersion =
            browserAgent.substring(tempStart, tempEnd);
    }

    // 基于真实版本号为 navigator 对象创建新属性
    navigator.appRealVersion = browserVersion;

    return;
}

getBrowserInfo();

document.write ("<h1>You appear to be running:<br><br>");
document.write ("<b>" + navigator.appName + "</b> <i>version</i> ");
document.write ("<b>" + navigator.appRealVersion + "</b></h1>");
```

如你所见，我们需要进行相当多的编码技巧才能弄清楚各种版本网景浏览器的实际版本号。对于 Netscape 4 及更早版本，`navigator.appVersion` 属性返回正确的值。由于 Netscape 6 和 7 以及 Mozilla 都将 `navigator.appVersion` 返回为 5.0，我们必须开始在 `navigator.userAgent` 属性中搜索相应的值。

> *前面的代码为了本示例的目的已进行了简化，因此未涵盖所有可能的浏览器类型或版本。关于浏览器检测脚本的绝佳示例，我推荐查看 Bob Clary 的《实用浏览器嗅探脚本》（Practical Browser Sniffing Script），网址为 http://bclary.com/xbProjects-docs/ua，它使用 `navigator` 对象的属性来确定浏览器类型和版本。该网站还包含一个脚本（位于 http://bclary.com/xbProjects-docs/xbDOM），允许你在所有浏览器中使用一套标准的 DOM 对象。*

以下插图展示了我们的小函数在 Netscape 2.0 和 Netscape 7.0 中的运行情况。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_187_0.png)



#### 查询文档模型

微软 Internet Explorer 一直以其独特的方式提供版本号。它在 `navigator.appVersion` 属性中将自己报告为 Netscape 4.0 兼容，而将实际的软件版本号嵌入同一字符串的其他位置。使用 JavaScript String 对象的 `indexOf()` 方法相对容易地搜索到它。

依赖按名称和版本检查浏览器的代码的问题在于它并非万无一失。目前，大约 96% 的网络用户使用两大主要浏览器之一——Netscape 或 IE。但那另外 4% 的用户呢——那些选择其他品牌（如 Opera 或 Konqueror）的用户？新的浏览器正在开发中，如果网站只针对前两大品牌进行编码，将无法可靠地运行。

另一个问题是，随着 IE 和 Netscape 新版本的发布，对不同功能的支持也会发生变化。例如，Netscape 4 支持一种名为层的布局方法，但在 Netscape 6 发布后，这种支持被取消了。（我们将在标题为“编写跨浏览器代码”的部分中更详细地讨论层。）

解决当前和未来可用浏览器种类繁多问题的最简单方法是，在尝试使用 DOM 方法之前，先编写代码检查该方法是否存在。

文档对象模型的第一个官方版本（称为 DOM 1）定义了一个名为 `getElementById()` 的 document 对象方法。较新的浏览器（如 IE 5 和 Netscape 6）支持它，但较旧的浏览器不支持。

在不支持它的浏览器中简单调用 `getElementById()` 方法会导致错误：

```javascript
var objptr = document.getElementById("carname");
```

因此，如果你想在使用前检查当前浏览器是否支持 `getElementById()` 方法，只需在调用之前查询 document 对象，看看是否有该名称的成员：

```javascript
if (document.getElementById) {
    var objptr = document.getElementById("carname");
}
```

前面的代码在任何浏览器中都有效，因为不支持该方法的浏览器不会执行 `if` 语句内的代码。当然，在这些浏览器中，变量 `objptr` 不会被设置，因此最好有备用代码来处理这些情况：

```javascript
if (document.getElementById) {
    var objptr = document.getElementById("carname");
} else {
    alert("Sorry, this web page will not work in your browser.");
}
```

当然，如果必须为每一个 DOM 方法调用都加上自己的 `if` 语句，你的程序将会冗长且效率低下。因此，最好的方法可能是将浏览器嗅探方法与 DOM 检测方法结合起来，以两全其美。

#### 坚持 Web 标准

在 Web 开发的早期，最大的两个浏览器制造商正在激烈地争夺市场份额——也许过于激烈了。他们最喜欢的策略之一是试图在功能上超越对方。消费者会下载并安装他们最喜欢的浏览器的最新版本，几天内下一个版本就可以下载了。有时需要数月时间来测试和批准新软件的大型公司，发现自己比当前版本落后了整整两个版本。

当然，这导致了两个 HTML 标准而不是一个，这使得 Web 开发人员的工作比必要的要复杂得多。幸运的是，微软和 Netscape 最终都决定，在它们获得标准委员会批准之前，将暂缓实施新的 HTML 和 JavaScript 功能。

然而，由于早期的“狂野西部”心态，存在许多非标准编码实践，应避免使用以实现跨平台兼容性。表 7-2 列出了不属于 HTML 4 标准的元素列表。

如果你希望创建在任何浏览器中都能一致工作的网页，应避免使用这些专有标记标签。

> 如果你想检查你的网页是否符合官方标准，W3C 网站在 http://validator.w3.org 提供了一个 HTML 验证服务。这个工具是查看你的网页与官方标准偏差有多远的最简单方法。它甚至能识别任何包含问题的 HTML 代码。

## 第 7 章：创建在每个浏览器中都能工作的脚本

**表 7-2** 专有标记标签，不属于官方 HTML 标准

| 专有标记 | 支持的浏览器 |
| :--- | :--- |
| `<layer>` | 仅 Netscape 4 |
| `<marquee>` | IE |
| `<bgsound>` | IE |
| `<embed>` | IE, Netscape |
| `<noembed>` | IE, Netscape |
| `<multicol>` | Netscape |
| `<spacer>` | Netscape |
| `<nobr>` | IE, Netscape |
| `<wbr>` | IE, Netscape |
| `<blink>` | Netscape |
| `<xmp>` | IE, Netscape |
| `<listing>` | IE, Netscape |
| `<plaintext>` | IE, Netscape |
| `<keygen>` | Netscape |
| `<layer>`, `<ilayer>` | Netscape |
| `<nolayer>` | Netscape |
| `<server>` | Netscape |

#### 编写跨浏览器代码

在本章的前面部分，我们试用了一些 JavaScript 代码，这些代码可用于检测客户端浏览器的确切名称和版本号。在本节中，我们将把类似的代码用于 *动态 HTML*。

动态 HTML（或简称 DHTML）是 HTML 标准的扩展，它允许 JavaScript 程序在网页加载到浏览器后对其进行更改和修改，而无需返回 Web 服务器获取新页面。在很大程度上，JavaScript 通过操作浏览器 DOM 中的方法和属性来完成此任务。

动态 HTML 被 Internet 网站定期用于提供花哨的下拉菜单、当你将鼠标光标移过时会改变的图像和文本，以及每次选择或清除一个复选框时都会重新计算订单总成本的电子商务购物车。最近几个月，广告商们迷上了 DHTML，正在创建在网页上移动（并且无法关闭或避免）的动态广告。

然而，跨浏览器的 DHTML 很难编码，因为 Netscape 和 Microsoft 浏览器所需的 JavaScript 代码相当不同。虽然标准化使得编程 HTML 和基本 JavaScript 比几年前容易得多，但浏览器之间存在巨大差异的 DOM 实现是最后剩下的少数荒野地带之一。

#### 如何用 JavaScript 做所有事情

图 7-1 展示了一个使用 DHTML 的网页示例。屏幕左侧的分层树可以通过简单的鼠标点击展开和收缩。菜单项动态显示和隐藏，无需向 Web 服务器请求新的 HTML。这种类型的 DHTML 菜单为访问你的网页的访客提供了良好的效果。

你可能遇到的最初困难之一是 Netscape 4 使用一种名为层的方法来定义可以应用样式的网页文档区域。

```html
<html>
    <head><title>Layers sample</title></head>
    <body>

        <h1>Netscape Layers Example</h1>

        <layer id="mylayer">
        <font color="white"><b>A black square</b></font>
        </layer>

        <layer id="mylayer2">
        <b>A gray square</b>
        </layer>

        <script language="JavaScript" type="text/javascript">
            document.layers["mylayer"].bgColor = "black";
            document.layers["mylayer2"].bgColor = "#CCCCCC";
            document.layers["mylayer2"].moveBy(60, 10);
        </script>
    </body>
</html>
```

这段 HTML 代码旨在仅在 Netscape 4.x 网页浏览器中工作。我们的代码使用 HTML `<layer>` 标签定义了一个名为 `mylayer` 的 Netscape 层。我们定义了第二个名为 `mylayer2` 的层。使用 JavaScript，我们能够更改两个层的背景颜色，并移动其中一个以使它们不完全重叠。效果可以在图 7-2 中看到。

不幸的是，前面的代码在任何版本的 IE 或较新的 Netscape 6 浏览器中都无法工作。我们必须稍微修改代码以检测运行的浏览器类型，并根据该类型执行不同的任务。

首先，我们需要更改层以使其在所有浏览器中工作。以下代码不完全符合 HTML 标准（因为 `<layer>` 标签不是标准的一部分），但它可以在 IE 和 Netscape 中工作。

**图7-1**  使用DHTML的可展开树形菜单

```
<layer id='mylayer'>
    <div id='mydiv' style='position:absolute'>
        <font color="white"><b>A black square</b></font>
    </div>
</layer>

<layer id='mylayer2'>
    <div id='mydiv2' style='position:absolute'>
        <b>A gray square</b>
    </div>
</layer>
```

#### Netscape 层示例

**图7-2** 在Netscape 4中创建层

注意我们是如何在非标准的`<layer>`标签内嵌套使用标准的`<div>`标签的。不支持`<layer>`标签的浏览器会忽略它，就像不支持`<div>`标签的浏览器会忽略该标签一样。

接下来，我们需要修改脚本以检测正在运行的浏览器类型。我们可以使用本章前面提到的`getBrowserInfo()`脚本，但我们的需求比那简单得多。我们只需要检测Netscape 4、Netscape 6和IE之间的区别。为此，我们可以使用以下JavaScript代码。

```
<script language="JavaScript" type="text/javascript">
    var ua = navigator.userAgent.toLowerCase();
    var ie4 = ua.indexOf("msie") != -1;

    if (document.layers) {
        // Netscape 4代码放在这里
    } else if (document.getElementById && ie4) {
        // IE代码放在这里
    } else if (document.getElementById) {
        // Netscape 6代码放在这里
    }
</script>
```

这段代码的工作方式相当简单。Netscape 4是唯一一种其文档对象具有`layers`属性的浏览器，因此检查该属性的存在就能确认浏览器类型是Netscape 4。我们可以使用文档对象的`getElementById`方法进行同样的操作，只是我们仍然需要区分IE 4和Netscape 6。`navigator.userAgent`属性允许我们做到这一点。

最后，我们添加特定于浏览器的DHTML代码，以操作屏幕上的两个`<layer>`或`<div>`标签，从而创建视觉效果。

```
<html>
    <head><title>Layers sample</title></head>
    <body>

    <h1>跨浏览器样式表示例</h1>

    <layer id='mylayer'>
        <div id='mydiv' style='position:absolute'>
            <font color="white"><b>A black square</b></font>
        </div>
    </layer>

    <layer id='mylayer2'>
        <div id='mydiv2' style='position:absolute'>
            <b>A gray square</b>
        </div>
    </layer>

    <script language="JavaScript" type="text/javascript">
    var ua = navigator.userAgent.toLowerCase();
    var ie4 = ua.indexOf("msie") != -1;

    if (document.layers) {
        // Netscape 4代码放在这里
        document.layers["mylayer"].bgColor = "black";
        document.layers["mylayer2"].bgColor = "#CCCCCC";
        document.layers["mylayer2"].moveBy (60, 10);

    } else if (document.getElementById && ie4) {
        // IE代码放在这里
        var div1 = document.getElementById("mydiv");
        var div2 = document.getElementById("mydiv2");
        div1.style.backgroundColor = "black";
        div2.style.backgroundColor = "#CCCCCC";
        div2.style.pixelLeft = div1.offsetLeft + 60;
        div2.style.pixelTop = div1.offsetTop + 10;

    } else if (document.getElementById) {
        // Netscape 6代码放在这里
        var div1 = document.getElementById("mydiv");
        var div2 = document.getElementById("mydiv2");
        div1.style.backgroundColor = "black";
        div2.style.backgroundColor = "#CCCCCC";
        div2.style.left = (div1.offsetLeft + 60) + "px";
        div2.style.top = (div1.offsetTop + 10) + "px";

    }
    </script>
    </body>
</html>
```

得到的跨浏览器兼容代码可以在图7-3的IE 6和图7-4的Netscape 7.0中看到。其结果与Netscape 4中的结果完全相同。

#### 跨浏览器样式表示例

一个黑色方块

一个灰色方块

**图7-4** 即使Netscape 7.0需要稍有不同的JavaScript，也能创建相同的效果。

这是一个很好的例子，说明了JavaScript程序员在开发能在任何浏览器中工作的代码时有时会遇到的困难。

在下一章，我们将探讨JavaScript在互联网上的主要职责之一——帮助用户填写表单。你将学习如何用HTML构建一个表单，了解可以放入表单的所有控件，并了解如何在数据发送到服务器处理之前，使用JavaScript来验证输入的数据。

# 第8章

# 操作网页表单

#### 如何用JavaScript做所有事情

#### 如何...

- 使用HTML表单请求用户输入
- 检索和设置表单控件值
- 准备用于服务器提交的表单数据
- 处理多个表单

在前面的章节中，我们已经看到如何使用JavaScript来提供动态网页，这些网页包含动画菜单，或者根据所使用的网页浏览器或一天中的时间而有所不同。随着时间的推移，开发者会发现在他们自己的个人主页上包含这些特殊的JavaScript技巧比以往任何时候都容易。

使JavaScript成为大多数专业网页开发人员不可或缺的开发工具的，是它处理用户输入的能力。JavaScript使收集和处理用户信息变得更加容易——对用户和网页开发者来说都是如此。JavaScript可以在许多方面提供帮助：

- 在用户的计算机上存储和检索信息片段（称为*cookies*）
- 验证所有必填的表单字段是否都已提供
- 验证用户输入数据的格式是否正确
- 无需访问网络服务器即可向用户提供即时反馈

最重要的是，做所有这些事情通常非常容易——只需要几行代码。通过解决比它创造的问题更多的问题，JavaScript迅速成为了严肃网页开发人员不可或缺的工具。

#### 理解HTML表单

请求用户输入的最佳且最灵活的方式是使用HTML表单。在网页编程中，*表单*是一系列旨在捕获用户输入的、一个或多个用户控件。用户控件通常是文本框、列表框或某种按钮，允许用户向网页浏览器提供信息。实际上，网页表单是仿照纸质表单设计的，比如你填写的工作申请表或调查问卷。

HTML中有13种用户控件：

- **文本框**：允许单行文本输入
- **密码框**：允许单行文本输入，受星号保护
- **文本区域**：允许单行或多行文本输入
- **隐藏域**：可以包含单行文本，对用户隐藏
- **列表框**：用户可以从一个或多个预定义选项中选择
- **单选按钮**：用户可以从多个预定义选项中选择一个
- **复选框**：用户可以从多个预定义选项中选择任意数量
- **文件**：用户可以从本地计算机上传文件到网络服务器
- **命令按钮**：触发程序定义的动作
- **提交按钮**：提交表单
- **图像按钮**：创建图形提交按钮
- **重置按钮**：清除表单
- **对象**：创建特殊的（用户定义的）输入控件

这些控件中的每一个在请求用户输入时都执行特定的功能。使用哪个控件在很大程度上取决于具体情况。例如，当你需要用户从50个选项中选择一个（比如选择他们居住的州）时，通常会选择列表框控件，它允许你在非常小的空间内提供几十个选项。选择显示50个单选按钮则会占用更多空间，并可能导致表单的其余部分滚动到屏幕底部之外。

#### 使用HTML表单请求用户输入

要了解典型的HTML表单是什么样子，让我们查看图8-1中的网页。美国邮政总局（www.usps.gov）提供了这个在线表单，用于注册搬家并希望将邮件转发到新地址的家庭或企业的地址变更。



屏幕上第一个表单字段标有“前缀头衔”，允许用户从多个姓名前缀（如“Dr.”、“Mr.”和“Mrs.”）中选择。如果用户姓名前不使用前缀，可选择“N/A”（不适用）。此控件称为列表框，因为按下向下箭头按钮时，用户将看到多个可供选择的选项。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_201_0.png)

标有“名”的表单字段是一个文本框，允许用户使用键盘输入一个或多个字符。有时，程序员会使用JavaScript对此字段施加限制，但通常用户可以输入字母、数字或特殊符号的任意组合。程序员可以使用HTML指定该字段的最大长度。

当用户完成输入个人数据后，系统会要求点击一个HTML提交按钮。提交按钮会将网页表单中的数据发送到Web服务器上等待处理的程序。使用JavaScript，网页开发者可以在允许提交到Web服务器之前对数据进行验证。

#### 使用客户端JavaScript处理表单输入

表单填写并提交后，通常会发送到Web服务器进行处理。需要注意的是，表单*不必*发送到Web服务器——网页表单通常可以完全在客户端使用JavaScript处理。你经常会看到这些*客户端表单*以在线计算器和类似工具的形式出现，JavaScript足够智能，无需Web服务器的帮助即可计算出所需结果并执行请求的操作。

图8-2展示了一个此类客户端表单的示例。图中显示的网页（http://javascript.internet.com/calculators/amortization.html）可以根据您提供的贷款金额、利率和摊销期限计算每月抵押贷款还款额。这是通过嵌入网页中的JavaScript函数计算的。

我们将在本章后面的“使用onsubmit捕获网页表单提交”部分探讨如何创建能响应网页表单的JavaScript代码。

#### 在Web服务器上处理表单输入

需要复杂处理的网页表单——例如访问数据库的表单——必须提交给服务器上等待的应用程序。目前有许多主流技术可用于创建这些表单处理程序：

- 服务器端JavaScript
- 应用程序服务器页面（ASP）
- Java Servlets
- Java服务器页面（JSP）
- Perl
- PHP
- 使用几乎任何语言编写的编译二进制文件（如C）

![](img/f14dd58a324d5464a114c30c1d4c4c9b_202_0.png)

**图8-2** 使用HTML表单计算每月抵押贷款还款额

一旦这些程序接受网页表单提交的数据，通常会执行所需的处理，然后通过另一个HTML页面响应浏览器。客户端与服务器之间的通信过程如图8-3所示。图中展示了用户在主要搜索引擎网站之一进行搜索的示例。Web服务器通过HTML表单接收关键词，检查其数据库中的相关网页，并返回包含结果的新HTML网页。

#### 将HTML表单插入网页

表单以与图像、文本和页面其他元素相同的方式添加到网页中，即使用HTML标记。开发者可以使用标准HTML标签定义表单的所有部分，包括其包含的控件及其排列方式。

#### 使用<form>标签

在HTML中，表单使用<form>标签定义。<form>标签允许您定义想要创建的表单类型，包括等待接受用户输入的程序的URL（如果有）。这些通过<form>元素的*属性*指定。属性是元素的命名参数和相关数据。属性按以下方式指定：

```
<element attribute1="value1" attribute2="value2" ... attribute3="value3">
```

![](img/f14dd58a324d5464a114c30c1d4c4c9b_203_0.png)

<form>元素具有以下属性：

| 属性 | 描述 |
|-----------|-------------|
| **id** | 在整个网页中必须唯一的字符串 |
| **class** | 关联的CSS类列表 |
| **style** | 内联CSS样式命令 |
| **title** | 建议性标题 |
| **lang** | ISO语言代码 |
| **dir** | 文本方向（从右到左或从左到右） |
| **action** | 将处理表单数据的程序的URI |
| **method** | 数据传输到服务器的方式（GET或POST） |
| **enctype** | MIME编码类型 |
| **accept** | 接受文件上传的MIME类型列表 |
| **accept-charset** | 支持的字符集列表 |

除了所有这些属性外，<form>元素还可以包含多个事件处理器。*事件*通常是由用户发起的操作，如鼠标移动或某些按键。*事件处理器*是设计为在特定事件发生时执行的JavaScript代码和函数。我们将在第9章更详细地探讨所有预定义的HTML事件处理器。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_204_0.png)

#### 将表单内容通过电子邮件发送给您

<form>标签的**action**属性允许您指定处理该表单的Web服务器程序的URI。通常，该程序是运行在目标Web服务器上的ASP页面、Java servlet或Perl脚本。

您也可以将浏览器定向为通过电子邮件将表单内容发送给您。这是通过使用mailto:协议为**action**属性提供电子邮件地址来实现的。要使用mailto:协议构建URI，只需将实际电子邮件地址附加到mailto:字符串后，如下所示：

```
mailto:president@whitehouse.gov
```

如果使用上述字符串作为**action**属性的URI，网页表单的内容将被发送给美国总统。

然而，此技术不能保证有效，因为它使用用户计算机上安装的邮件程序。该程序可能未正确设置以发送电子邮件，或者用户可能取消发送电子邮件。

目前，我们只关注网页表单可能发生的两个事件：

- **onsubmit**：在表单提交前将运行的JavaScript代码
- **onreset**：在表单数据被清除前将运行的JavaScript代码

某些HTML元素具有强制性属性，即必须始终存在的属性。`<form>`元素就是其中之一，因为**action**属性必须始终指定，HTML才能有效。

最基本的表单类型如下：

```
<form action="#">
</form>
```

此HTML代码创建一个不包含任何控件的空表单。当然，此类表单毫无用处，因为它们没有目的。HTML `<form>`元素本身是不可见的，因为它们没有可视组件。表单控件（例如按钮和文本框）是表单的可视组件。表单还可以包含文本、表格和其他HTML元素。

> **提示**
> 当不需要时，通常使用井号（#）作为`<form>`标签**action**属性的值，因为**action**属性是强制性的，不能省略。您可以将此用于仅设计为存在于客户端、永远不需要提交到服务器的表单。井号（#）是最短的有效URL之一。

#### 添加表单控件

正如我们所见，没有控件的表单几乎没有用处。表单控件允许网页接受用户输入。有些控件允许用户自行输入文本，有些则为用户提供多个预定义选项供选择。表单控件通过自己的HTML添加到`<form>`元素中。表8-1列出了常见的输入控件以及将其添加到网页所需的HTML。

#### 使用文本框接受文本输入

也许最常见的表单控件类型是文本框。实际上，文本框控件是`<input>`元素的默认类型。以下HTML代码将创建一个包含单个文本框的网页表单。

```
<form action="#">
    <input>
</form>
```



| 控件名称 | HTML 代码 |
|---|---|
| 文本框 | `<input type="text"...>` |
| 密码框 | `<input type="password"...>` |
| 文本区域 | `<textarea...> </textarea>` |
| 隐藏文本 | `<input type="hidden"...>` |
| 列表框 | `<select...> </select>` |
| 单选按钮 | `<input type="radio"...>` |
| 复选框 | `<input type="checkbox"...>` |
| 文件上传 | `<input type="file"...>` |
| 按钮 | `<input type="button"...>` |
| 按钮 | `<button...>` |
| 提交按钮 | `<input type="submit"...>` |
| 图像按钮 | `<input type="image"...>` |
| 重置按钮 | `<input type="reset"...>` |
| 对象控件 | `<object...> </object>` |

**表 8-1 HTML 表单控件列表**

当然，创建这样的表单有几个缺点。首先，在浏览器中遇到该表单的任何人都不知道该如何处理它——该控件没有标签。它只是一个孤立在页面上的文本框。其次，查看该代码的网页开发者可能会感到有些困惑，因为 `<input>` 控件有太多形式。最好明确设置控件类型。

一个更好的网页表单示例如下：

```
<form action="#">
    Please enter your age: <br>
    <input type="text" name="age">
</form>
```

这种类型的网页表单对网页开发者和网页访问者来说都更易于使用。文本框控件有几个属性，为开发者提供了更多对控件外观和行为的控制：

- **id** 在整个网页中必须唯一的字符串
- **class** 关联的 CSS 类列表
- **style** 内联 CSS 样式命令
- **title** 建议性标题
- **lang** ISO 语言代码
- **dir** 文本方向（从右到左或从左到右）
- **name** 控件的名称
- **value** 默认值
- **size** 控件在屏幕上的大小，以字符为单位
- **maxlength** 可输入的最大字符数
- **readonly** 锁定控件，使其值不能被用户修改
- **accesskey** 设置键盘快捷键
- **tabindex** 设置表单中控件接收焦点的顺序
- **disabled** 锁定控件，使其无法接收焦点或被用户修改

> *在网页编程中，当控件是当前活动控件时，我们说它具有焦点。浏览器通常通过使用文本框的闪烁垂直线或按钮和其他控件的某种高亮显示来让我们知道哪个控件具有焦点。大多数浏览器会为具有焦点的非文本控件绘制一个临时的虚线框。*

除了前面的属性，我们的输入控件还可以捕获许多事件。我们将在第 9 章更详细地研究所有预定义的 HTML 事件处理器。目前，我们将只关注以下 HTML 事件：

- **onfocus** 当控件获得焦点时将运行的 JavaScript 代码
- **onblur** 当控件失去焦点时将运行的 JavaScript 代码
- **onchange** 当控件失去焦点且其内容值已被更改时将运行的 JavaScript 代码

通过在我们的文本框上使用其中一些属性，我们可以改善控件的外观和行为：

```
<form action="#">
    Please enter your <u>a</u>ge: <br>
    <input type="text" name="age" size="5" maxlength="3"
        value="" accesskey="A">
</form>
```

我们通过在 `<input>` 控件上使用 **size="5"** 属性，将控件的水平长度减少到五个字符宽。通过指定 **maxlength="3"**，我们将输入限制为最多三个字符长。由于我们询问的是年龄，因此可以合理地假设三个数字就足够了。

**value=""** 属性将字段的默认内容设置为空字符串。**accesskey** 参数在我们的示例中设置为 "A"，允许用户在大多数 Windows 版本中使用 ALT-A 组合键，或在大多数 Mac 系统中使用 CONTROL-A 组合键跳转到该控件。

> 激活快捷键所需的组合键取决于浏览器类型和操作系统，因此如果您无法使其正常工作，请查阅您的浏览器文档。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_208_0.png)

#### 提供列表框控件

列表框是一种方便的控件，当您需要用户从多个选项中选择一个时使用。在 HTML 中，列表框使用 `<select>` 元素创建，列表中的项目使用 `<option>` 元素定义。您可以在基于网页的表单中使用两种类型的列表框：*下拉列表框* 和 *滚动列表框*。

##### 你知道吗？隐私与互联网

HTML 表单通常用于允许访问者登录网站。用户通常必须向服务器提供有效的用户 ID 和密码，才能被允许访问网站的受限制区域。

从开发者的角度来看，文本框应用于向用户请求用户 ID。作为额外的安全级别，应使用密码框控件来请求用户的密码。密码框将输入的字符替换为星号，因此 *password* 变为 ********。这样做是为了让其他查看同一台电脑显示器的人（例如，从用户身后看）无法读取密码。

然而，您应该知道这是一种非常弱的安全类型。除非表单数据使用安全套接字层 (SSL) 加密，通常使用 HTTPS 协议，否则密码将以纯文本形式通过互联网发送，任何沿途的人或任何有权访问网络服务器活动日志的人都可以轻松读取。

下拉列表框显示为一个文本框，旁边有一个小箭头按钮。单击箭头会导致控件创建一个可滚动的弹出窗口，用户可以在其中从多个选项中选择一个，如您所见。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_209_0.png)

用户不能在文本框中输入自己的文本——他们必须从预定义的项目中选择一个。当至少有三个选项可供选择时，这种类型的控件最适合使用，例如要求用户选择他们的居住州或国家。其他控件，如单选按钮和复选框，更适合用户从只有两三个选项中进行选择。

滚动列表框显示为多行文本框与垂直滚动条的组合，如您所见。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_210_0.png)

滚动列表框是通过使用 HTML `<select>` 元素的 **size** 属性指定一次要显示的项目数量来创建的。如果开发者指定了 **multiple** 属性，用户可以从滚动列表框中选择多个选项。用户可以从列表中选择多个选项，在选择项目时按住键盘上的 CTRL (PC) 或 COMMAND (Mac) 键。

以下 HTML 将创建一个包含单个下拉列表框的表单。

```
<form action="#">
What would you like for dinner?<br>
<select name="dinner">
    <option selected value="1">Chicken</option>
    <option value="2">Beef</option>
    <option value="3">Pork</option>
    <option value="4">Fish</option>
    <option value="5">Vegetables</option>
</select>
</form>
```

通过指定 **size** 属性，我们可以将下拉列表框修改为滚动列表框。由于我们的 **size** 属性只允许一次显示三个项目，用户将能够通过使用滚动条查看剩余的两个项目。

```
<form action="#">
What would you like for dinner?<br>
    <select name="dinner" size="3">
        <option value="1" selected>Chicken</option>
        <option value="2">Beef</option>
        <option value="3">Pork</option>
        <option value="4">Fish</option>
        <option value="5">Vegetables</option>
    </select>
</form>
```

HTML `<select>` 元素有几个属性，为网页开发者提供了更多对列表框控件外观和行为的控制：

- **id** 在整个网页中必须唯一的字符串
- **class** 关联的 CSS 类列表
- **style** 内联 CSS 样式命令
- **title** 建议性标题
- **lang** ISO 语言代码
- **dir** 文本方向（从右到左或从左到右）
- **name** 控件的名称
- **size** 一次要显示的行数
- **multiple** 允许控件接受多个选择
- **tabindex** 设置表单中控件接收焦点的顺序
- **disabled** 锁定控件，使其无法接收焦点或被用户修改

除了前面的属性，我们的列表框控件还可以捕获许多事件。我们将在第 9 章更详细地研究预定义的 HTML 事件处理器。列表框可以捕获以下三个事件：

- **onfocus** 当控件获得焦点时将运行的 JavaScript 代码
- **onblur** 当控件失去焦点时将运行的 JavaScript 代码
- **onchange** 当控件失去焦点且其内容值已被更改时将运行的 JavaScript 代码



HTML `<option>` 元素自身拥有多个属性：

- **id** 在整个网页中必须唯一的字符串标识
- **class** 关联的CSS类列表
- **style** 内联CSS样式命令
- **title** 建议性标题
- **lang** ISO语言代码
- **dir** 文本方向（从右到左或从左到右）
- **selected** 将此列表项定义为默认项
- **disabled** 锁定控件，使其无法获得焦点或被用户修改
- **label** 为列表项定义标签
- **value** 当用户选择该项时返回给服务器的字符串

`<option>` 元素还可以接收多个事件。我们将在第9章更详细地探讨所有预定义的HTML事件处理器。

#### 使用文本区域接受文本输入

文本框的一种变体是*文本区域*。文本区域控件接受多行输入，并使用HTML `<textarea>` 元素定义。文本区域控件的一个缺点是，你无法轻易地限制用户添加到该控件中的数据量。

`<textarea>` 元素最常见的属性是 **rows**、**cols**（列数）和 **name**。正如你所料，你可以使用 **rows** 属性指定控件的高度，使用 **cols** 属性指定控件的宽度。例如，下面的文本区域将容纳5行，每行60个字符宽。

```
<form action="#">
    <textarea rows="5" cols="60">
        This is my example text area.
    </textarea>
</form>
```

默认文本插入在 `<textarea>` 和 `</textarea>` 标签之间。

#### 向表单添加按钮控件

与其他控件不同，*按钮*（或简称*按钮*）通常不用于提供用户输入。它们的目的是通过按钮的onclick事件处理器使浏览器执行一些JavaScript代码。有一种特殊类型的按钮控件称为*提交按钮*，可用于提供用户输入。我们将在下一节中探讨提交按钮。

在HTML中，有两种方法创建简单的按钮：使用 `<input>` 元素和使用 `<button>` 元素。 `<input>` 元素用于创建最基本类型的按钮，如下所示：

```
<form action="#">
    <input type="button" value="Push me" onclick="dothis()">
</form>
```

此表单中定义的按钮在按下时将调用名为dothis()的JavaScript函数。 **value** 属性定义按钮的*标题*，即按钮上的文本标签。

`<button>` 元素允许开发人员创建更复杂的按钮类型。 `<button>` 元素接受复杂的HTML输入（包括文本和图像）作为其标题。例如，以下按钮在单词OK（以粗体显示）旁边显示一个对勾图像。它在被点击时也会调用JavaScript dothis()函数。

```
<form action="#">
    <button onclick="dothis()">
        <img src="checkmark.gif">
        <font size="6"><b><i>OK</i></b></font>
    </button>
</form>
```

以下是这种特殊类型的按钮在浏览器窗口中的外观。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_213_0.png)

#### 添加提交按钮

提交按钮是一种特殊类型的表单控件，因为它们会使表单将自身提交到服务器。表单中定义的变量和数据会使用 `<form>` 元素的method属性中定义的方法，发送到action属性中定义的Web服务器应用程序。

例如，以下代码定义了一个表单，该表单会将自身提交到一个ASP网页。该ASP网页负责处理数据并发送一个新的网页供浏览器显示。

```
<form
    action="http://www.example.com/scripts/myscript.asp"
    method="GET">
    Full Name: <input type="text" name="fullname"><br>
    Age: <input type="text" name="age" size="5"><br>
    Date of Birth: <input type="text" name="DOB" size="10"><br>
    <input type="submit" value="Submit Form">
</form>
```

当用户点击“Submit Form”按钮时，表单上的另外三个表单控件（fullname、age和DOB）将连同用户在这些字段中输入的任何文本一起发送到ASP网页。

> **注意：** *只有具有name属性的表单字段才会被提交到服务器进行处理。没有指定name属性的字段，即使是文本字段，也不会被提交到服务器。通常会省略提交按钮的name属性。唯一需要给它们命名的情况是，如果表单上有多个提交按钮，并且服务器需要知道是使用哪个按钮提交表单的。*

#### 使用onsubmit捕获Web表单提交

在本章前面的“使用 `<form>` 标签”一节中，我们看到HTML `<form>` 元素有多个预定义的事件处理器。处理事件被称为捕获它，在本节中，我们将简要了解 `<form>` 元素的一个事件及其捕获方法。

onsubmit属性允许我们指定在Web表单提交到Web服务器之前将执行的一些JavaScript代码。此JavaScript代码通常存储在一个函数中，因此事件处理器仅引用该函数。但有时JavaScript代码会直接出现在事件处理器属性中。

```
<script language="JavaScript" type="text/javascript">
function checkname() {
    alert("Your name is " + document.forms[0].fullname.value);
}
</script>

<form action="http://www.myserver.com/formhandler"
method="GET"
onsubmit="return checkname() ">
What is your name? <br>
<input type="text" name="fullname"> <br>
<input type="submit" value="Submit Form">
</form>
```

在前面的HTML代码中，我们指定了一个JavaScript函数，该函数将在表单使用 `<form>` 元素的**onsubmit**事件处理器属性提交到Web服务器时被调用。将要调用的函数是checkname()，我们已在表单上方定义了它。checkname()函数完成后，表单数据将被发送到URL http://www.myserver.com/formhandler进行处理。

在这里你可以看到创建的HTML表单。作为示例，我已经输入了我的名字的五个字母。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_215_0.png)

标记为“Submit Form”的按钮实际上是一个提交按钮，它将导致表单被发送到Web服务器。然而，在提交之前，会调用checkname()函数。该函数简单地检索文本框的内容并将其显示在JavaScript警告框中。一旦用户接受了警告框，表单就会将其数据发送到Web服务器进行处理。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_216_0.png)

我们的onsubmit事件处理器实际上能够阻止Web表单被提交。从函数返回布尔值false将导致处理停止，而不会将表单提交到服务器。

```
<script language="JavaScript" type="text/javascript">
function checkname() {
    var username = document.forms[0].fullname.value;
    if (username != "Scott") {
        alert("Sorry, " + username + ". I cannot let you proceed.");
        return false;
    } else {
        return true;
    }
}
</script>
```

前面的JavaScript函数，当由相同的HTML表单调用时，如果用户没有在名称字段中输入Scott，将不会提交到Web服务器。

#### 捕获表单控件上的事件

与HTML `<form>` 标签类似，表单控件也可以有可编程事件。程序可以定义一个JavaScript函数或代码，该函数或代码将在某个事件发生时执行。例如，JavaScript可以检测鼠标光标何时经过控件、何时获得或失去焦点，或者其值何时已更改。

例如，以下代码演示了如何捕获一些文本框控件的事件。

```
<html>
    <head>
        <title>Capture Form Control Events</title>
        <script language="JavaScript" type="text/javascript">
        <!-- // Begin

        function modifylayer(changetext) {
            var lefield = document.getElementById("lastevent");
            lefield.innerHTML = changetext + "<br><br>&nbsp;";
```



#### 如何使用 JavaScript 实现一切功能

```html
// End -->
</script>
</head>
<body>
<h1>捕获表单控件事件</h1>

<form action="#" method="get">
将鼠标移入和移出此字段，
或更改其内容。<br>
<textarea name="samplefield" rows="10" cols="30"
    onmouseover="modifylayer('mouseover')"
    onmouseout="modifylayer('mouseout')"
    onchange="modifylayer('change')"
    onkeypress="modifylayer('keypress')"
    >示例文本</textarea><br><br>

最后捕获的事件：
<div id="lastevent"
    style="background-color:#CCCCCC; font-weight:bold">
<br><br>&nbsp;
</div>
</form>

</body>
</html>
```

HTML 文档的主体包含一个 HTML `<form>`，其中包含一个控件——一个名为 `<textarea>` 的多行文本框。我们还定义了一个 HTML `<div>` 区域，其中包含我们可以使用 JavaScript 更改的文本。

`<textarea>` 还定义了多个事件处理程序。如果此控件发生以下任何事件，Web 浏览器将调用名为 `modifylayer()` 的 JavaScript 函数：

-   **onmouseover** 当鼠标指针进入控件时
-   **onmouseout** 当鼠标指针离开控件时
-   **onchange** 当控件的内容已更改且控件失去焦点时
-   **onkeypress** 当按下键盘按键时

我们使用文档头部分中的 `<script>` 标签定义 `modifylayer()` 函数。该函数会将事件的名称写入我们定义的 `<div>` 区域。

你可以在微软网站 http://msdn.microsoft.com/workshop/author/dhtml/reference/events.asp 上查看 Internet Explorer 支持的所有浏览器事件列表。我们也在第 9 章中更全面地讨论了 Web 浏览器事件。

当然，还有一种方法可以捕获事件的名称，而无需使用 **window.event** DOM 对象将其显式传递给函数。我们可以将 JavaScript 代码修改为以下形式以利用此技术。

```javascript
function modifylayer() {
    var lefield = document.getElementById("lastevent");
    var ename = window.event.type;
    lefield.innerHTML = ename + "<br><br>&nbsp;";
}
```

使用这种类型的函数，我们不再需要在每个事件处理程序中传递事件的名称。`modifylayer()` 函数可以自行处理所有四个事件。

```html
<textarea name="samplefield" rows="10" cols="30"
    onmouseover="modifylayer()"
    onmouseout="modifylayer()"
    onchange="modifylayer()"
    onkeypress="modifylayer()"
    >示例文本</textarea><br><br>
```

从下面的屏幕截图中，我们可以看到此网页在 Web 浏览器中的外观和行为。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_218_0.png)

#### 在 JavaScript 中检索和设置表单控件值

上一节中的一个代码示例演示了从 Web 表单检索值的多种可能方法之一。DOM 为 JavaScript 程序提供了多种方式来访问表单上的控件及其值，包括：

-   作为 forms 数组的属性
-   作为 elements 数组中的键值
-   使用 document 对象的三种不同方法之一

> 并非所有这些技术在旧版本的主要浏览器中都有效，因此你可能需要使用第 7 章中讨论的一些跨浏览器脚本技术。

#### 使用 forms 数组访问表单值

一种在所有支持 JavaScript 的浏览器中都能工作的技术是使用 forms 数组访问表单控件。forms 数组是 DOM document 对象的属性；它包含网页上所有表单的索引列表。JavaScript 中的索引从零开始。
我们首先创建一个引用表单本身的变量。

```javascript
var myform = document.forms[0];
```

然后，我们可以通过名称访问表单上的任何控件。例如，以下代码允许你访问名为 fullname 的文本框的内容：

```javascript
var fullname = myform.fullname.value;
```

正如本章前面“使用文本框接受文本输入”中所述，value 是文本框控件的属性。上面的代码将该文本框的内容放入我们称为 fullname 的变量中。
使用此技术允许我们访问表单上的任何控件，只要它有名称。以下代码演示了一个包含文本框、列表框和一组单选按钮的表单。在提交表单之前，名为 `checkform()` 的函数会验证用户是否在每个字段中输入了文本或做出了选择。

```html
<html>
<head>
<title>JavaScript Test</title>
<script language="JavaScript" type="text/javascript">
<!-- // Begin

function checkform() {
    var myform = document.forms[0];

    // 访问文本框很容易
var fullname = myform.fullname.value;
var emailaddr = myform.email.value;

// 哪个下拉项被选中？
var ageIdx = myform.age.selectedIndex;
var age = myform.age.options[ageIdx].value;

// 哪个单选按钮被选中？
var hearObj = myform.hear;
var hear = "";

for (var i = 0; i < hearObj.length; i++) {
    if (hearObj[i].checked) {
        hear = hearObj[i].value;
    }
}

// 检查是否有任何字段为空
if ((fullname == "") || (emailaddr == "") ||
    (age == "None") || (hear == "")) {
    alert("某些信息似乎缺失。");
    return false;
} else {
    return true;
}
}

// End -->
</script>
</head>
<body>
    <h1>JavaScript forms 数组</h1>

    <form action="#" onsubmit="return checkform()">
    <center>
    <table width="400" cellspacing="12">
    <tr>
        <td align="right"><b>姓名：</b></td>
        <td><input type="text" name="fullname"></td>
    </tr>
    <tr>
        <td align="right"><b>电子邮件：</b></td>
        <td><input type="text" name="email"></td>
    </tr>
    <tr>
        <td align="right"><b>年龄：</b></td>
        <td><select name="age">
        <option value="None">-- 请选择 --</option>
        <option value="16-32">16-32</option>
        <option value="33-49">33-49</option>
        <option value="Over 50">50+</option>
        </select></td>
    </tr>
    <tr>
        <td align="right"><b>您是如何<br> 听说我们的？</b></td>
        <td valign="top">
        <input type="radio" name="hear" value="t"> 电视<br>
        <input type="radio" name="hear" value="r"> 广播<br>
        <input type="radio" name="hear" value="n"> 报纸<br>
        <input type="radio" name="hear" value="o"> 其他</td>
    </tr>
    <tr>
        <td align="middle" colspan="2">
        <input type="submit" value="发送到服务器"></td>
    </tr>
    </table>
    </center>
    </form>
</body>
</html>
```

图 8-4 展示了此表单在典型 Web 浏览器中的外观。如果我们尝试在未填写其中一个字段的情况下提交此表单，`checkform()` 函数会捕获它，并报告此错误：

![](img/f14dd58a324d5464a114c30c1d4c4c9b_221_0.png)

#### 使用 elements 数组访问表单值

访问表单上控件的另一种方式是通过 *elements 数组*。elements 数组是网页上所有表单控件的顺序列表。要访问特定控件的值，你需要事先知道它在数组中的位置。如果你需要以数组形式访问所有控件或在数组中搜索特定控件，此数组很方便。

```javascript
var earray = document.forms[0].elements;
for (var count = 0; count < earray.length; count++) {
    alert(earray[count].name);
}
```

上面的代码演示了如何查询 elements 数组。它成功找到了表单上的第一个控件。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_222_1.png)

##### 图 8-4

一个包含各种表单控件的网页

#### 使用 getElementById() 访问表单值

我们刚刚研究的两种技术（forms 数组和 elements 数组）是使用 DOM 的旧方式。这些方法的主要问题是它们特定于表单。如果你想访问 `<h1>` 元素（文档标题）的内容并更改它，那是做不到的。

`getElementById()` DOM 方法是访问网页上任何对象的新首选方式——无论是表单控件、`<div>` 标签，甚至是嵌入页面中的 Java 小程序。

要检索 fullname 文本框的值，我们将使用 `getElementById()` 函数，如下所示：

```javascript
var fullname = document.getElementById("fullname").value;
```

此代码在当前文档中查找 ID 为 fullname 的元素。JavaScript 在此时不知道（也不关心）它是什么类型的对象——它可能是任何 HTML 元素。顾名思义，此函数尝试通过 ID 查找元素。大多数 HTML 元素都有一个 ID 属性（`id=""`），为了对元素使用此函数，你应该相应地设置 ID 属性。

```html
<input type="text" id="fullname" name="fullname">
```

> 如果找不到匹配的 ID，大多数浏览器也会按其 name 属性搜索元素。

#### 使用 getElementsByName() 访问表单值

正如 `getElementById()` 函数将按 ID 属性搜索元素一样，`getElementsByName()` 函数将按其 name 属性搜索元素。这两个函数之间的唯一区别是 `getElementsByName` 返回一个元素数组。因此，它可以返回多个元素。

```javascript
var hearObj = document.getElementsByName("hear");
```

此代码将返回网页上所有名为 hear 的元素数组。早些时候我们创建了一些 HTML，其中包含一组名为 hear 的单选按钮——页面上有四个名为 hear 的元素（参见“使用 forms 数组访问表单值”）。在该表单上使用此代码将返回一个包含四个元素的数组。我们使用的 JavaScript 代码然后将正确确定四个单选按钮中哪个被选中。

```javascript
for (var i = 0; i < hearObj.length; i++) {
    if (hearObj[i].checked) {
        hear = hearObj[i].value;
    }
}
```



#### 使用 getElementsByTagName() 访问表单值

新的 JavaScript DOM 提供的最后一个方法是 getElementsByTagName()。此方法在获取未命名元素时非常有用，例如我们之前表单示例中的提交按钮。此函数允许我们通过 HTML 元素名称在网页上查找对象。

```javascript
var mybutton = document.getElementsByTagName("input");
mybutton[6].value = "Please wait...";
mybutton[6].disabled = true;
```

将此代码添加到 checkform() 函数的开头，我们可以禁用提交按钮，以防止用户重复提交表单。getElementsByTagName("input") 函数返回网页上所有 `<input>` 元素的数组。我们知道提交按钮是使用 HTML `<input>` 标签创建的网页上的第七个元素——其余六个是两个文本框和四个单选按钮。由于数组从索引零开始，提交按钮位于数组的第六个索引处。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_224_0.png)

按钮已被禁用，标题已设置为"请稍候"。

如你所见，DOM 提供了多种不同的方法来访问表单内容。在下一章中，我们将研究浏览器事件的方方面面。我们将从 HTML 中不同类型的事件以及如何编写事件处理程序来处理它们开始。我们还将研究处理事件时出现的一些特殊的跨浏览器兼容性问题。

## 第 9 章

## 处理浏览器事件

![](img/f14dd58a324d5464a114c30c1d4c4c9b_226_0.png)

#### 如何...

- 编写 JavaScript 事件处理程序
- 使用事件属性处理事件
- 在 JavaScript 中触发事件
- 克服浏览器不兼容性

字典将*事件*定义为"发生的事情"，这在 Web 编程中也是如此。*事件处理程序*是为在每次特定事件发生时运行而设计的 JavaScript 代码。当然，这意味着你的 JavaScript 代码可能会执行数十次，也可能根本不执行，这取决于具体情况。

HTML 4.01 规范中正式定义了 18 个事件。此外，支持官方 DOM Level 2 事件规范的浏览器需要为程序员提供更多事件。然而，Microsoft 和 Netscape 已经超越了官方规范中列出的事件，提供了更多事件：IE 支持超过 75 个事件，Netscape 至少支持 50 个。

> **注意** *DOM Level 2 事件*规范可在 W3C 官方网站 http://www.w3.org/TR/DOM-Level-2-Events 上找到。

了解如何编写适当事件处理程序的关键是理解事件是什么以及它们何时发生。例如，以下事件只是官方 18 个 HTML 4.01 事件中的三个：

- **load 事件** 当 HTML 文档在浏览器窗口中完成加载时发生
- **click 事件** 当鼠标左键被点击时发生
- **keypress 事件** 当键盘按键被按下时发生

JavaScript 可以用来在这些事件发生时拦截它们并采取某些操作（有时允许取消事件）。拦截事件称为*捕获*事件，这通过编写事件处理程序代码来完成。如果没有编写事件处理代码，浏览器将继续使用默认行为正常处理事件。

在本章中，我们将研究大多数 HTML 元素提供的各种事件以及如何为每个事件编写事件处理程序。我们还将了解 JavaScript 程序如何手动触发这些事件，并研究各种浏览器在事件处理方面的差异。

#### 编写 JavaScript 事件处理程序

你在上一章"使用 onsubmit 捕获 Web 表单提交"部分中看到了一些事件处理程序的示例。编写 onsubmit 事件处理程序使我们的 JavaScript 程序能够在表单提交被允许继续之前检查表单上的所有字段是否都已填写。

#### 处理用户界面事件

事件分为四大类：

- 用户界面事件
- 鼠标事件
- 按键事件
- HTML 事件

用户界面事件发生在网页上的控件或其他对象获得和失去焦点时。这些事件通常由其他用户操作（如按 Tab 键或鼠标点击）引起，但它们也可以通过编程方式发生。

鼠标事件发生在用户移动鼠标或按下鼠标按钮之一时。这些事件允许网页响应鼠标移动，例如当鼠标移过图像时突出显示该图像。

按键事件发生在用户按下和/或释放键盘按键之一时。只有某些 HTML 元素可以捕获键盘事件，我们将在本章后面看到。

最后，有一些特定于某些 HTML 元素的事件。它们通常与浏览器窗口本身或与嵌入在网页中的表单控件和其他对象有关。上一章讨论的 onsubmit 事件处理程序就属于这一类。

用户界面事件专门处理焦点从网页内的一个对象转移到另一个对象。大多数 Web 浏览器中定义了三种用户界面事件。

| 事件名称 | 事件处理程序名称 | 定义于 |
|---|---|---|
| focus | onfocus | HTML 4.01 |
| blur | onblur | HTML 4.01 |
| activate | onactivate | DOM Level 2 |

例如，假设我们有一个包含两个文本框的网页。

```html
<form action="#">
    <input type="text" name="box1"><br>
    <input type="text" name="box2">
</form>
```

假设当前活动光标位于名为 box1 的文本框内。当我们按下键盘 TAB 键时，我们期望焦点转移到第二个文本框 box2。暂时忽略键盘事件，三个用户界面事件以可预测的顺序*触发*（发生）。

首先，box2 上触发 activate 事件。接下来，box1 上触发 blur 事件。最后，box2 上触发 focus 事件。我们可以稍微修改网页来观察事件始终以可预测的顺序触发。

```html
<script type="text/javascript" language="javascript">
  function upd(instr) {
    document.forms[0].statusbox.value += instr + "; ";
  }
</script>
<form action="#">
  <input type="text" name="box1"
    onblur="upd('blur box1')" ><br>
  <input type="text" name="box2"
    onfocus="upd('focus box2')"
    onactivate="upd('activate box2')" ><br><br>
  Event firing order:
  <input type="text" name="statusbox" size="40">
</form>
```

在前面的代码中，我们向屏幕上添加了第三个名为 statusbox 的文本框，以显示我们的事件触发测试结果。我们为三个事件处理程序（onblur、onfocus 和 onactivate）提供了 JavaScript，它们会将事件和控件名称附加到 statusbox 文本框的末尾。

测试结果如图 9-1 所示。如你所见，状态框中列出的事件与我们预期的顺序一致。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_229_0.png)

##### 图 9-1

用户界面事件以可预测的顺序触发。

#### 处理鼠标事件

下表中列出的七个鼠标事件都与用户使用鼠标进行的操作有关。JavaScript 程序能够跟踪与网页及其内部控件相关的鼠标移动和按钮点击。

| 事件名称 | 事件处理程序名称 | 定义于 |
|---|---|---|
| mousedown | onmousedown | HTML 4.01 |
| mouseup | onmouseup | HTML 4.01 |
| mouseover | onmouseover | HTML 4.01 |
| mousemove | onmousemove | HTML 4.01 |
| mouseout | onmouseout | HTML 4.01 |
| click | onclick | HTML 4.01 |
| dblclick | ondblclick | HTML 4.01 |

跟踪这些鼠标事件通常是为了增强用户体验，例如当鼠标指针滚过菜单项时突出显示它们，或更新屏幕文本以提供指针下方元素的更多信息。

例如，以下 HTML 代码使用 `<img>` 元素将图像插入网页。通过捕获 mouseover 和 mouseout 事件，我们可以使图像在鼠标指针位于图像上时发生变化，并在指针离开时恢复为原始图像。

```html
<script type="text/javascript" language="javascript">
function changeimage(num) {
    var img = document.getElementById("SampleImage");
    if (num == 1) {
        img.src = "NewImg.gif";
    } else {
        img.src = "OriginalImg.gif";
    }
}
</script>

<img src="OriginalImg.gif"
     id="SampleImage"
     alt="Sample image"
     onmouseover="changeimage(1)"
     onmouseout="changeimage(2)" >
```

当鼠标指针进入图像边界时，mouseover 事件立即触发。onmouseover 事件处理程序调用 changeimage() 函数，参数为 1。changeimage() 函数首先根据图像的 id（SampleImage）将图像的引用分配给一个变量。图像的 **src** 属性允许我们动态修改浏览器中显示的图像。



当鼠标指针离开图像边界时，mouseout 事件就会触发。changeimage() 函数也会处理这个事件，使图像恢复为原始来源。我们可以在图 9-2 中看到这种图像翻转效果。

#### 处理键盘事件

JavaScript 程序员很少使用键盘事件处理程序来捕获键盘事件。虽然在少数几种情况下你可能会使用它们，但这种事件处理方式在 Windows 应用程序（如 Visual Basic 程序）中比在基于 Web 的编程中更为常见。

与用户界面事件类似，键盘事件的触发顺序是可以预测的。HTML 中有三个主要的键盘事件。

| 事件名称 | 事件处理程序名称 | 定义于 |
|---|---|---|
| keypress | onkeypress | HTML 4.01 |
| keydown | onkeydown | HTML 4.01 |
| keyup | onkeyup | HTML 4.01 |

通过稍微修改"处理用户界面事件"一节中的代码，我们可以看到这些事件触发时的可预测顺序。

```
<script type="text/javascript" language="javascript">
  function upd(instr) {
    document.forms[0].statusbox.value += instr + "; ";
  }
</script>
<form action="#">
    <input type="text" name="box1"
        onkeypress="upd('keypress')"
        onkeydown="upd('keydown')"
        onkeyup="upd('keyup')"><br><br>
    Event firing order:
    <input type="text" name="statusbox" size="40">
</form>
```

![](img/f14dd58a324d5464a114c30c1d4c4c9b_231_0.png)

![](img/f14dd58a324d5464a114c30c1d4c4c9b_232_0.png)

**图 9-3** 键盘事件的触发顺序为 keydown、keypress 和 keyup。

从图 9-3 的截图中可以看到，事件的顺序是

1. keydown
2. keypress
3. keyup

当几乎任何键盘按键被按下时，keydown 事件就会发生，包括 HOME、ESCAPE、INSERT 和 DELETE 等非字母数字键。另一方面，keypress 事件只在某些字母数字键被按下时触发，包括标点符号、SPACEBAR 和 ENTER。keyup 事件是 keydown 的补充，因为当几乎任何按键被释放时，该事件就会触发。

keydown 和 keypress 事件都可以被取消。要取消一个事件，只需让它的处理程序返回 false 即可。取消 keydown 或 keypress 事件将导致浏览器忽略这些按键。例如，如果你想限制在表单字段中输入的字符类型，可以捕获其 keydown 事件，并在按键不在可接受范围内时返回 false。

# 214 How to Do Everything with JavaScript

```
<script type="text/javascript" language="javascript">
function checkkey() {
    var keycode = window.event.keyCode;
    if (keycode < 48 || keycode > 57) {
        return false;
    } else {
        return true;
    }
}
</script>
<form action="#">
    <input type="text" name="box1"
           onkeydown="return checkkey()"><br>
</form>
```

上述代码展示了如何捕获 keydown 事件。由于我们希望能够取消该事件，因此在事件处理程序中加入了一个 return 语句，同时调用了 checkkey() 函数。

> Unicode 字符集的前 127 个字符与对应的 ASCII 代码完全一致。有关 Unicode 字符集的更多信息，请访问 http://www.unicode.org。

checkkey() 函数通过检查 window.event DOM 对象的 keyCode 属性来获取与按键关联的 Unicode 字符代码。我们将 keyCode 的值与数字键的值范围进行比较，该范围恰好是 48–57。如果我们拦截到的 keyCode 超出了可接受的范围，就从函数中返回 false，表示该按键应被忽略。当然，如果按键在可接受范围内，我们就返回 true。

> window.event 对象的 keyCode 属性仅在 Netscape 6 及更高版本和 Internet Explorer 中可用。

这样就得到了一个只接受数字输入并忽略所有其他字符的文本框。下表列出了几个常见字符及其对应的 keyCode 值。

| keyCode 值 | 对应字符 |
|---|---|
| 48 到 57 | 0 到 9 |
| 65 到 90 | A 到 Z（大写字母）|
| 97 到 122 | a 到 z（小写字母）|
| 46 | . （句点）|
| 44 | , （逗号）|
| 40 和 41 | ( 和 ) （括号）|
| 36 | $ （美元符号）|
| 35 | % （百分号）|
| 34 | " （引号）|

#### 处理 HTML 事件

在此语境下，*HTML 事件* 是指不属于用户界面、鼠标或键盘事件类别的任何事件。某些 HTML 事件由用户操作直接触发，而另一些则只是用户操作的间接结果。

下表列出了 HTML 事件、其事件处理程序名称以及定义它们的官方规范。

| 事件名称 | 事件处理程序名称 | 触发时机（事件） | 定义于 |
| --- | --- | --- | --- |
| load | onload | 浏览器完成文档加载 | HTML 4.01 |
| unload | onunload | 浏览器即将卸载文档 | HTML 4.01 |
| submit | onsubmit | 表单即将提交 | HTML 4.01 |
| reset | onreset | 表单即将重置 | HTML 4.01 |
| select | onselect | 文本框内容被选中 | HTML 4.01 |
| change | onchange | 表单控件内容已更改 | HTML 4.01 |
| abort | onabort | 用户中止图像下载 | DOM Level 2 |
| error | onerror | 对象加载时发生错误 | DOM Level 2 |
| resize | onresize | 对象大小即将改变 | DOM Level 2 |
| scroll | onscroll | 用户使用滚动条 | DOM Level 2 |

让我们快速看看这些事件的作用。

- **load 事件** 当 HTML 文档完成加载到浏览器窗口时，onload 事件处理程序被调用。该事件通常用于执行文档所需的任何初始化。例如，如果表单字段需要预加载文本，而这部分未由 HTML 代码本身涵盖，最好等到文档完全加载后再初始化这些字段。
- **unload 事件** 当浏览器离开当前文档时，unload 事件触发。这发生在浏览器窗口被关闭或用户已转到另一个文档时。此事件的主要目的是在文档关闭前执行清理任务。
- **submit 事件** submit 事件发生在表单提交到 Web 服务器之前。通常捕获此事件以在允许表单提交继续之前执行编辑检查。由于此事件可以被取消，JavaScript 可以在一切未就绪时阻止表单被处理。
- **reset 事件** 当表单上的重置按钮被点击时，reset 事件发生。重置按钮通过将所有值恢复为默认值来清除表单。

> unload 事件通常在一些不太正规的网站中被用来在用户离开网站前提供最后的弹出式广告。这通常被认为是不礼貌的做法。应避免使用 unload 事件，除非绝对必要。

# 216 How to Do Everything with JavaScript

**select 事件** 当用户在文本框或文本区域中选择文本时，select 事件发生。可以通过按住鼠标左键拖动跨越文本，或按住 SHIFT 键同时使用箭头键移动光标跨越文本来选择文本。

**change 事件** 当控件失去焦点（用户按 Tab 键离开）且其值已被更改时，change 事件发生。这样，在文本框中，change 事件不会为用户输入值的每一次按键都触发，而只在用户离开字段时触发。该事件同样以相同方式在单选按钮、复选框和选择列表上触发。

**abort 事件** 当浏览器停止尝试加载网页上的图像时，abort 事件发生。这可能发生在用户点击浏览器的停止按钮或点击链接转到另一个页面时。根据我的经验，这个事件很少被使用。

**error 事件** 当网页加载过程中发生错误时，error 事件发生。这可能是特定对象的错误（例如 Java 小程序加载失败）或由编写不当的 JavaScript 代码引起的运行时错误。这是另一个在大多数网页中很少被捕获的事件。

**resize 事件** 当对象正在调整大小时，resize 事件触发——例如，如果浏览器窗口或框架被用户调整大小。有时你可能希望根据可用空间来调整窗口内各个控件的大小，尽管捕获此事件仍然很少见。

**scroll 事件** 对于浏览器窗口或文本区域表单控件等可滚动的 Web 对象，当对象的滚动条被改变时，scroll 事件随时触发。这可以通过使用鼠标手动移动滚动条、使用箭头键或其他方式来实现。

以下代码演示了如何使用 onload 事件处理程序捕获 load 事件。我们的网页包含一个表单，onload 事件处理程序代码用某些预定义的值填充该表单上的列表框。

```
<html>
  <head>
    <title>JavaScript Sample recreation Page</title>
    <script language="JavaScript" type="text/javascript">
    <!-- // Begin

    function initialize() {
      var lst = document.getElementById("samplelist");
      var opn = new Array(20);
      var temp;
      var counter;

      for (counter = 1; counter <= 10; counter++) {
        opn[counter] = document.createElement("option");
        lst.options.add(opn[counter]);
        temp = counter * 10;
        opn[counter].innerText = temp.toString();
```



#### 使用 onload 初始化表单

```html
// End -->
</script>
</head>
<body onload="initialize()">
    <h1>Initialize a Form with onload</h1>
    
    <form action="#">
        <select id="samplelist"></select>
    </form>
    
</body>
</html>
```

在上述 HTML 代码中，浏览器一旦完成加载到浏览器窗口，就会调用 JavaScript 的 initialize() 函数。这是通过在 `<body>` 标签中设置 onload 事件处理程序来实现的。

在 initialize() 函数内部，程序向网页主体中定义的空 `<select>` 列表框添加了 10 个选项。我们可以在图 9-4 中看到这个函数的结果。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_236_0.png)

# 图 9-4  已向下拉列表框添加了十个选项。

#### 使用事件属性处理事件

为 HTML 标签设置 JavaScript 事件处理程序有两种方法：

- 在 HTML 内部设置事件处理程序属性
- 在 JavaScript 内部设置事件处理程序属性

我们已经见过如何在 HTML 中设置事件属性：

```html
<img src="OriginalImg.gif"
    id="SampleImage"
    alt="Sample image"
    onmouseover="changeimage(1)"
    onmouseout="changeimage(2)" >
```

在这段代码中，我们使用相应的事件处理程序设置了处理 mouseover 和 mouseout 事件的 JavaScript 函数。我们可以使用 JavaScript 重写代码来设置事件处理程序：

```html
<img src="OriginalImg.gif"
    id="SampleImage"
    alt="Sample image">
```

```html
<script type="text/javascript" language="javascript">
    var img = document.getElementById("SampleImage");
    img.onmouseover = changeimageover;
    img.onmouseout = changeimageout;
    function changeimageover() {
        img.src = "NewImg.gif";
    }
    function changeimageout() {
        img.src = "OriginalImg.gif";
    }
</script>
```

HTML `<img>` 标签有两个名为 **onmouseover** 和 **onmouseout** 的属性，可以使用 HTML 和 JavaScript 进行设置。使用 JavaScript 设置事件属性增加了一些灵活性，因为用于处理事件的 JavaScript 函数可以在页面显示后动态更改。但正如你从示例 JavaScript 代码中看到的，使用这种技术无法传递参数，因此在某些方面也不够灵活。

#### 事件冒泡的工作原理

假设你有一个包含按钮的网页表单。你为 `<form>` 标签和 `<input type="button">` 标签都创建了 JavaScript onclick 事件处理程序。当你用鼠标点击按钮控件时，你认为哪个 onclick 事件处理程序会被调用——按钮的还是表单的？事实上，浏览器会执行两个事件处理程序。

按钮的 onclick 事件处理程序会先被调用，因为它是最内层的元素。接下来，表单的 onclick 事件处理程序会被调用。如果还有其他有资格处理此事件的 onclick 事件处理程序（例如，在 `<body>` 标签上），它们也会依次被调用。这种事件首先由最内层元素处理，然后依次由下一个内层元素处理的过程，称为*事件冒泡*。

#### 在 JavaScript 中触发事件

有时你会希望让 JavaScript 程序触发某个事件。这称为*触发*事件，网页中的许多对象都提供了可以调用来触发事件的方法。

在 JavaScript 中触发事件有两种方法：

- 调用与事件关联的方法
- 调用 fireEvent 方法手动触发事件

#### 调用与事件关联的方法

第一种技术是调用与事件关联的方法。大多数事件都有一个方法可以模拟导致事件触发的活动。例如，HTML `<form>` 对象有一个名为 submit() 的方法，它会尝试提交表单，导致 submit 事件触发。

我们可以通过以下 HTML 代码来演示这一点。这段代码展示了如何使用超链接来模拟提交按钮。

```html
<script type="text/javascript" language="javascript">
function clickme() {
    document.forms[0].submit();
}
</script>
<form action="http://www.example.com/cgi-bin/entry.pl"
method="get">
Please enter your full name: <br>
<input type="text" name="fullname"><br>
<a href="javascript:clickme()">Click here to
    <b>submit</b> the form</a>
</form>
```

当用户点击表单内的超链接时，JavaScript 会调用 clickme() 函数。clickme() 函数调用表单对象的 submit() 方法，导致表单自行提交。submit() 方法的作用与用户点击表单的提交按钮完全相同，导致 submit 事件触发。

> 在 IE 中，调用 submit() 方法会导致表单提交，但不会调用附加到表单的任何 submit 事件处理程序。如果你的 `<form>` 有 onsubmit 属性，则必须在调用 submit() 方法之前手动调用那些 JavaScript 函数。

其他事件也有导致事件发生的关联方法。例如，focus() 方法会使控件获得焦点，而 blur() 方法会使控件失去焦点。同样，有一个 click() 方法允许 HTML 对象模拟被鼠标点击。

#### 使用 fireEvent 方法

第二种技术是调用 fireEvent() 方法来手动触发事件。在 IE 中，fireEvent() 是 DOM 中大多数对象的方法，可用于触发事件。例如，你可以通过以下方式触发按钮控件的 onclick 事件：

```javascript
var btn1 = document.forms[0].helpButton;
btn1.fireEvent("onclick");
```

不幸的是，这种方法不太可靠。虽然这种技术本应该能够触发任何对象上的事件，但我发现它对某些事件或对象不起作用，例如表单对象上的 onsubmit 事件，或提交按钮对象上的 onclick 事件。

> 鉴于它不是官方 DOM 标准的一部分，且无法在 IE 以外的任何浏览器中工作，开发人员在使用这种技术时应该非常小心。

#### 克服浏览器不兼容性

浏览器事件在跨浏览器兼容性方面是一个薄弱环节。当然，HTML 定义了少数标准事件，各种 DOM 规范（Level 1 和 Level 2）也将事件向前推进了一步。但浏览器制造商添加了许多更多的可编程事件供 JavaScript 开发人员使用，Netscape 和 IE 都支持 50 多种事件就证明了这一点。

一些额外的事件是对现有事件的轻微修改。例如，IE 提供了 onbeforeactivate 和 onbeforeunload 事件处理程序，允许程序员在 onactivate 和 onunload 事件触发之前捕获它们。这些额外的事件是可取消的，这意味着你可以阻止 activate 或 unload 事件发生，而现有的 onactivate 和 onunload 事件在事件发生之后触发，因此无法取消。其他事件处理程序允许程序员访问标准未指定的事件：

- onbeforeprint 和 onafterprint 允许访问浏览器打印事件。
- ondrag、ondragstart 和 ondragend 允许访问拖放事件。
- onmousewheel 允许访问鼠标滚轮移动。
- oncut、oncopy 和 onpaste 允许访问复制和粘贴事件。

当然，问题在于这些事件通常只被一种浏览器支持，而另一种浏览器不支持。它们也往往只被较新版本支持，而较旧的浏览器不支持。虽然从程序员的角度来看，使用这些有趣的事件可能很有诱惑力，但你必须采取第 7 章中列出的一些预防措施，并在依赖这些方法之前使用浏览器嗅探代码。

当然，这些专有事件的一个好处是，如果编码正确，它们通常不会导致浏览器崩溃。例如，以下代码尝试捕获文本框控件上的 onpaste 事件。

```html
<form action="#">
    <input type="text" name="myctl" onpaste="pasteevent()"/>
</form>
```

当然，由于 onpaste 事件处理程序是在 HTML 元素内部设置的，如果浏览器不支持该控件上的粘贴事件，浏览器将简单地忽略该代码。唯一的后果是在不兼容的浏览器中不会捕获粘贴事件。

然而，如果你绝对依赖此事件处理程序来执行某些关键代码，例如提交表单，则必须使用浏览器嗅探代码为不支持它的浏览器提供替代代码。

在下一章中，我们将讨论浏览器框架。JavaScript 程序在处理多框架环境时面临特殊挑战，我们将研究一些相关问题以及如何最好地解决它们。



## 第10章

## 浏览器框架间通信

#### 用JavaScript实现一切

#### 如何...

-   创建框架集
-   在框架集中定义和命名框架
-   从其他框架调用JavaScript函数
-   处理框架间的同步

在Web编程中，框架集用于将单个网页划分为两个或更多较小的部分。这些部分中的每一个，或称为框架，都是一个独立的HTML网页。Web开发者可以为这些框架定义几个重要属性，包括整体尺寸、位置以及边框的可见性。

在本章中，我们将探讨当今互联网上框架集的使用情况。特别是，我们将看到JavaScript程序员在使用框架时面临的一些挑战，并探讨一些克服这些挑战的建议。

#### 了解HTML框架的基础知识

框架对于显示网站的静态部分非常有用，例如菜单、横幅和网站导航工具。由于框架集中的所有框架彼此独立，它们为网站开发者和访问者提供了几个重要的好处。如果使用得当，框架可以

-   缩短浏览网站所需的时间
-   使网站对访问者来说更易于使用、更直观
-   使网站对开发者来说更容易维护

图10-1展示了一个使用框架的网页示例。该图包含三个框架：一个顶部框架，链接到网站的其他区域；一个左侧框架，包含一个菜单；以及一个中心框架（称为主框架），包含网站的关键内容。

尽管框架对Web程序员和访问者都很方便，但仍有相当多的人不喜欢它们。当框架使用不当时，可能会引入许多问题：

-   浏览器书签无法正确设置。
-   在非常小或非常大的显示器分辨率下，网站看起来很糟糕。
-   搜索引擎无法准确索引框架集的内容。

除了这些问题之外，级联样式表（CSS）的使用和浏览器支持也在不断增加。样式表可以提供与框架许多相同的好处，包括用户友好的导航，甚至静态横幅和菜单。许多曾经包含框架集的流行网站现在都使用DHTML菜单和其他更现代的动态元素。

**第10章：** 浏览器框架间通信

**图10-1** 包含框架的网站（ZVON.org）示例

#### 在HTML中创建框架集

在HTML中，框架是使用两个标签的组合创建的：`<frameset>` 和 `<frame>`。`<frameset>` 标签用于定义框架集中框架的尺寸和定位。`<frame>` 标签用于定义单个框架的属性，例如源HTML文档和框架边框的可见性。

`<frameset>` 元素具有以下属性：

-   **id** 在整个网页中必须唯一的字符串
-   **class** 关联的CSS类列表
-   **style** 内联CSS样式命令
-   **title** 建议标题
-   **lang** ISO语言代码
-   **dir** 文本方向（从右到左或从左到右）
-   **rows** 以逗号分隔的行高列表
-   **cols** 以逗号分隔的列宽列表

`<frameset>` 标签还支持 onload 和 onunload 事件处理程序。

图10-1中显示的网页由四个独立的HTML文件组成。一个HTML文件包含框架集布局——通常只有 `<head>` 部分以及 `<frameset>` 和 `<frame>` 标签。其他三个HTML文件包含三个框架中每一个的单独内容——本示例中的每个HTML文件都对应一个框架。

当然，这并不总是如此。多个框架可以关联到同一个HTML文件，有些框架可以使用JavaScript动态生成，因此没有文件与之关联。唯一的判断方法是查看代码。

以下代码是一个框架集文档的完整示例。

```html
<html>
    <head>
        <title>Framesets</title>
    </head>
    <frameset rows="100, *">
        <frame src="banner.html" name="banner">
        <frameset cols="150, *">
            <frame src="menu.html" name="menu">
            <frame src="mainbody.html" name="bodyframe">
        </frameset>
    </frameset>
</html>
```

前面的HTML代码定义了一个包含三个框架的框架集。它使用了本章后面名为“创建嵌套框架集”的部分中讨论的技术。我们可以通过计算 `<frame>` 标签的数量来判断文档中的框架数量。

请注意，框架集文档包含通常的 `<html>`、`<head>` 和 `<title>` 标签，但不包含 `<body>` 标签。这是因为框架集文档不能包含自己的 `<body>`——这是不允许的。但是，我们可以使用 `<head>` 部分的所有有效内容，包括JavaScript代码、元数据和使用适当HTML标签的样式表定义。

#### 处理不支持框架的浏览器

提供使用框架的网站可能对您网站的许多访问者来说很方便。如今，绝大多数网络冲浪者（根据最新估计，超过99%）的浏览器都能显示框架。但仍有少数网络浏览器不支持它们。许多早期浏览器，如Windows版IE 2或OS/2版Netscape 2，就不支持。其他支持网络的设备，如PDA和手机，通常难以正确呈现框架。

HTML提供了 `<noframes>` 标签，允许Web开发者为浏览器不支持 `<frameset>` 标签的用户显示内容。支持该标签的浏览器将忽略任何 `<noframes>` 部分的内容。

## 第10章：浏览器框架间通信 227

例如，我们可以修改之前看到的HTML代码以包含 `<noframes>` 标签：

```html
<html>
    <head>
        <title>Framesets</title>
    </head>
    <frameset rows="100, *">
        <frame src="banner.html" name="banner">
        <frameset cols="150, *">
            <frame src="menu.html" name="menu">
            <frame src="mainbody.html" name="bodyframe">
        </frameset>
        <noframes>
            It appears you are using a browser that does not support frames. If you would like to view this site, you will need to upgrade your browser. I suggest either Netscape or IE.
        </noframes>
    </frameset>
</html>
```

根据HTML 4.01规范，`<noframes>` 标签必须包含在 `<frameset>` 标签内。

#### 使用 rows 和 cols 属性设置框架大小值

正如我们在本章前面看到的，框架集中框架的大小和定位是通过HTML `<frameset>` 标签处理的。`<frameset>` 标签的两个主要属性是 **rows** 和 **cols**。**rows** 属性用于定义框架集中水平框架的行高，而 **cols** 属性用于定义垂直框架的列宽。每个属性接受一个或多个以逗号分隔的值列表。

在 **rows** 和 **cols** 属性中指定大小值有三种方式：

-   绝对大小，以像素为单位
-   相对大小，以百分比表示
-   绝对大小和相对大小的组合，使用星号符号

**rows** 和 **cols** 都是可选属性。每个属性的默认值都是“100%”；这定义了一个占据浏览器窗口所有可用空间的框架。

三种大小值类型及其代表含义的示例如表10-1所示。

| 值 | 框架大小 |
| --- | --- |
| 250 | 250屏幕或打印像素 |
| 25% | 占总可用屏幕或打印像素的25%（四分之一） |
| * | 在考虑其他框架大小后，平均分配可用空间 |
| 3* | 在考虑其他框架大小后，按3:1的比例分配可用空间 |

**表10-1** 大小值示例及其对框架集的影响

> 特殊星号值在本章后面的“使用绝对值和相对值同时设置框架大小值”部分有更详细的解释。

**rows** 和 **cols** 属性都接受一个或多个以逗号分隔的值。您提供的每个值都会在框架集中创建一个框架。

#### 使用绝对像素值设置框架大小

HTML允许您定义框架的确切大小，称为其*绝对大小*。框架的绝对大小通过为 **rows** 和/或 **cols** 属性指定正整数值来设置。

例如，一个包含两个水平框架的框架集，一个高200像素，另一个高280像素，可以使用以下HTML代码创建：

```html
<frameset rows="200, 280">
    <!-- <frame> 标签放在这里 -->
</frameset>
```

> 即使是绝对大小也并非总是绝对的。如果浏览器窗口的实际大小与框架大小的总和不匹配，浏览器将自动调整框架大小以适应可用空间。

当然，您不限于只能有两个框架。您可以在框架集中设置任意数量的框架。以下代码示例定义了四个水平框架：

```html
<frameset rows="200, 200, 400, 400">
    <!-- <frame> 标签放在这里 -->
</frameset>
```

> 虽然理论上您可以在一个框架集中定义任意数量的框架，但出于美观原因，您可能希望将数量限制在三个或四个。



#### 使用相对值设置框架尺寸值

除了指定框架的确切像素尺寸外，还有另一种定义框架尺寸的方法。开发者可以将尺寸指定为可用空间的百分比。这被称为*相对尺寸*，因为框架的尺寸完全基于浏览器窗口的大小，而这个大小在不同计算机之间可能会有所不同。

```html
<frameset rows="50%, 50%">
    <!-- <frame> 标签放在这里 -->
</frameset>
```

上述代码将创建两个框架，每个框架占用浏览器窗口可用垂直空间的50%。在一个高度为480像素的窗口中，这将创建两个水平框架，每个框架高240像素。如果用户的浏览器窗口高于480像素，每个框架的实际像素高度将调整为相应的相对大小。

#### 同时使用绝对值和相对值设置框架尺寸值

第三种方法是结合两种方式——创建一些尺寸绝对的框架和另一些尺寸相对于可用空间的框架。要实现这种有用的效果，请为固定框架指定绝对像素数，并使用星号（*）代替相对尺寸。

例如，如果你想让第一个框架高200像素，让第二个框架自动调整大小以适应窗口的其余部分，你可以在设置高度时使用星号（*）：

```html
<frameset rows="200, *">
    <!-- <frame> 标签放在这里 -->
</frameset>
```

这将创建一个包含两个框架的框架集，其中一个高200像素，另一个占据所有剩余的垂直空间。

如果你多次使用星号，网页浏览器将在考虑固定高度框架后，自动均等调整这些框架的大小以填充可用空间。

```html
<frameset rows="200, 200, *, *">
    <!-- <frame> 标签放在这里 -->
</frameset>
```

上述代码中的`<frameset>`标签将创建一个包含四个框架的框架集。前两个框架各高200像素，总计400像素。如果浏览器窗口的可视区域高度为480像素，最后两个框架将均分剩余的80像素，因此每个框架将高40像素。如果浏览器窗口的高度扩展到600像素，那两个框架的高度将各为100像素，因为它们在固定高度框架之后均匀分割了剩余的200像素。

还有一种方法可以指导浏览器在使用星号时不均匀地分配可用空间，即提供*星号乘数*。星号乘数是一个可以可选地放在星号前面的数字，使其获得超过平均分配的空间。

例如，以下框架集定义了四个框架，其中两个由浏览器自动调整大小。但剩余的空间将不均匀地分配。

```html
<frameset rows="200, 200, *, 3*">
    <!-- <frame> 标签放在这里 -->
</frameset>
```

在定义最后一个框架的星号前加上数字3，将导致该框架的高度是第三个框架高度的三倍。这意味着第四个框架将获得可用空间的四分之三，而第三个框架仅获得四分之一。因此，如果浏览器窗口高度为800像素，浏览器将通过给第三个框架分配100像素、给第四个框架分配300像素来分割剩余的400像素。

#### 使用行定义水平框架

到目前为止，在本章中，你已经看到了类似下面的代码，它将创建三个水平框架。

```html
<frameset rows="80, 45, *">
    <!-- <frame> 标签放在这里 -->
    <frame src="frame1.html">
    <frame src="frame2.html">
    <frame src="frame3.html">
</frameset>
```

这些被称为水平框架，因为每个框架跨越浏览器窗口的整个宽度。由于我们使用了**rows**属性，在上述示例中，水平线分隔了这三个框架。在图10-2中，你可以看到这些水平框架在浏览器中的样子。

![使用rows属性创建的水平框架示例](img/f14dd58a324d5464a114c30c1d4c4c9b_250_0.png)

**图10-2** 使用**rows**属性创建的水平框架示例

![使用cols属性创建垂直框架](img/f14dd58a324d5464a114c30c1d4c4c9b_250_1.png)

**图10-3** 使用**cols**属性创建垂直框架

#### 使用列定义垂直框架

定义一组垂直框架与定义水平框架没有太大区别。`<frameset>`标签的**cols**属性允许你创建具有垂直边框而不是水平边框的框架。

```html
<frameset cols="165, *">
    <!-- <frame> 标签放在这里 -->
    <frame src="frame1.html">
    <frame src="frame2.html">
</frameset>
```

上述HTML代码将创建一个包含两个框架的框架集。第一个框架宽度为165像素，而第二个框架将占据浏览器窗口中的剩余水平空间。图10-3展示了垂直框架的外观。

![使用cols属性创建垂直框架](img/f14dd58a324d5464a114c30c1d4c4c9b_250_1.png)

**图10-3** 使用**cols**属性创建垂直框架

#### 使用行和列定义框架

框架集不必仅仅是水平或垂直的。网页开发者可以创建同时包含行和列的框架集，就像网格一样。这可以通过同时指定**rows**和**cols**属性的值来实现。

例如，要创建一个有三行两列的框架集，你需要使用以下HTML代码：

```html
<frameset rows="50, 100, *" cols="50%, 50%">
    <!-- <frame> 标签放在这里 -->
    <frame src="frame1.html">
    <frame src="frame2.html">
    <frame src="frame3.html">
    <frame src="frame4.html">
    <frame src="frame5.html">
    <frame src="frame6.html">
</frameset>
```

上述代码创建了一个包含六个框架的框架集，排列成三行两列。注意，行数和列数不一定相等。图10-4展示了这种复杂框架集在浏览器中的样子。

![包含三行两列的复杂框架集](img/f14dd58a324d5464a114c30c1d4c4c9b_251_0.png)

#### 创建嵌套框架集

同时使用**rows**和**cols**属性创建复杂框架集有其局限性。具体来说，行和列是按网格模式创建的——一行中的所有列宽度相同，所有行高度相同，如图10-4所示。它将始终是一个完美对齐的网格，尽管网格中单元格的大小可以不同。

如果你想创建不相等的行和列该怎么办？你如何创建一个只有一列的行，但为下一行定义几列呢？答案是嵌套框架集。

*嵌套框架集*是通过将一个或多个框架集放置在另一个框架集内部来实现的，从而将单个框架细分为更小的部分。所有嵌套框架集必须从一个单一的外部框架集开始。

```html
<frameset rows="80, *">
    <!-- <frame> 标签放在这里 -->
    <frame src="frame1.html">
    <frame src="frame2.html">
</frameset>
```

例如，上述HTML代码创建了一个简单的框架集，其中包含两个水平框架。

现在，假设我们想将第二个框架进一步细分为两列。这可以通过第二个框架集来完成：

```html
<frameset rows="80, *">
    <!-- <frame> 标签放在这里 -->
    <frame src="frame1.html">
    <frameset cols="150, *">
        <frame src="frame2.html">
        <frame src="frame3.html">
    </frameset>
</frameset>
```

我已将原始代码中的第二个框架替换为第二个框架集。这个嵌套框架集将第二个框架分为两列。你可以在图10-5中看到这种类型框架集的效果。

#### 在框架集中定义和命名框架

既然你已经理解了如何使用`<frameset>`标签创建简单和复杂的框架集，我们就应该简要了解一下框架本身是如何定义的。单个框架使用`<frame>`标签定义。`<frame>`标签具有以下属性：

- **id** 全局唯一ID
- **class** 关联的CSS类列表
- **style** 内联CSS样式命令



- **title** — 咨询标题
- **longdesc** — 指向框架较长描述的链接
- **name** — 框架的内部名称
- **src** — HTML文档的URI
- **frameborder** — 框架边框的可见性
- **marginwidth** — 垂直边框（或窗口边框）与HTML内容之间，以像素为单位的空间量
- **marginheight** — 水平边框（或窗口边框）与HTML内容之间，以像素为单位的空间量
- **noresize** — 控制用户是否可以调整框架大小
- **scrolling** — 滚动条的可见性

以上所有属性都是可选的。但是，很少会在不显式指定 `src` 属性的情况下定义 `<frame>` 标签。这个属性允许你指定框架的源HTML文件。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_253_0.png)

##### 图 10-5 使用嵌套框架集将框架划分为不等的部分

当在框架中使用JavaScript时，通常方便的做法是使用 **name** 属性为框架分配一个唯一的名称。

```
<frame src="/dir/subdir/myframe.html" name="frame1">
```

框架的源可以是任何有效的URI——它甚至不必与其他框架位于同一Web服务器上。

```
<frame src="http://www.cnn.com/" name="frame1">
```

> 在你自己的网站内使用其他网站的内容被称为网站框架，*这种做法涉及商标和版权法律，具有一些潜在的法律后果。关于这个主题有一篇非常好的文章，位于* http://www.gigalaw.com/articles/2000-all/kubiszyn-2000-04-all.html *，如果你有兴趣在未经所有者许可的情况下对另一个网站进行框架嵌入，你应该阅读它。*

默认框架创建时带有可调整大小的边框。你可以通过指定 **noresize** 属性轻松创建不可调整大小的边框。

```
<frame src="myframe.html" name="frame1" noresize>
```

**noresize** 属性不需要赋值——它在 `<frame>` 标签内的存在就表示边框是固定的。

> 在XHTML（HTML的XML兼容版本）中，每个属性都必须分配一个值。在XHTML中，你会为 **noresize** 分配它自己的名称作为值，例如 *noresize="noresize"*。

默认情况下，框架具有可见的边框，用于分隔一个框架与下一个框架。然而，这并不总是可取的，因为这些边框并不总是与网站的风格相匹配。幸运的是，使边框不可见相当容易，从而使单个框架不那么引人注意。

```
<frame src="myframe.html" name="frame1" noresize frameborder="0">
```

当然，你需要将这个 **frameborder** 属性添加到框架集中的每个框架标签，以移除所有边框。

#### 从其他框架调用JavaScript函数

正如本章第一节所讨论的，一个由三个框架组成的网页实际上由四个独立的HTML文件组成——每个框架一个文件，框架集一个主文件。

这些框架彼此独立，但它们并非互不相识。每个框架都有可能访问任何其他框架的内容，包括在那里定义的任何JavaScript变量和函数。

#### 使用JavaScript访问另一个框架

正如第8章所讨论的，我们可以使用以下JavaScript代码来访问表单的内容：

```
var myform = document.forms[0];
var fullname = myform.fullname.value;
```

这段代码将创建一个名为 myform 的变量，它直接指向网页上的第一个表单。然后，它将使用 myform 变量来访问名为 fullname 的控件及其内容。
但是，如果该表单位于另一个框架中，我们该如何访问它的内容呢？让我们暂时假设我们有一个框架集，其定义如下HTML代码。

```
<html>
    <head>
        <title>Framesets</title>
    </head>
    <frameset rows="100, *">
        <frame src="banner.html" name="banner">
        <frameset cols="150, *">
            <frame src="menu.html" name="menu">
            <frame src="mainbody.html" name="bodyframe">
        </frameset>
    </frameset>
</html>
```

如果我们位于该框架集的第二个框架（menu）中，我们将如何访问第三个框架（bodyframe）中包含的表单内容？
我们通过访问框架集的 window 对象来实现这一点。JavaScript提供了多种类型的 window 对象供程序使用。各种JavaScript窗口对象及其描述列于表10-2中。

> **注意：** 窗口对象和文档对象模型通常在第11章中有更详细的讨论。

| 对象名称 | 描述 |
|---|---|
| window | 当前框架或窗口 |
| top | 最顶层的窗口 |
| parent | 包含当前框架的框架集（不一定是最顶层的窗口） |
| self | 当前框架或窗口；与 window 对象相同 |

**表 10-2** JavaScript窗口对象

表10-2中列出的每个窗口对象都包含一个名为 frames 的数组。当一个窗口对象指向整个框架集时，该对象的 frames 数组包含一个元素，对应于文档中包含的每个框架。当一个窗口对象指向单个框架时，此数组通常为空。当然，如果各个框架本身也是框架集，则 frames 数组不会为空。

要从 menu 框架内的JavaScript代码访问 bodyframe 框架的内容，我们从最顶层的窗口开始，使用 top 对象。然后我们访问该数组中的第三个元素（索引为2，因为数组从索引0开始）。

```
var bodyframe = top.frames[2];
```

bodyframe 变量代表对我们框架集中定义的第三个框架的引用。然后，我们可以使用该框架的 document 对象来访问该窗口包含的文档。

```
var bodyframe = top.frames[2];
var bodydocument = bodyframe.document;
```

最后，我们可以使用 bodydocument 表示的 document 对象，以通常的方式访问表单和该表单上的元素。

```
var bodyframe = top.frames[2];
var bodydocument = bodyframe.document;
var myform = bodydocument.forms[0];
var fullname = myform.fullname.value;
```

这段代码被分成四行以提高可管理性和易读性。如果程序需要引用该表单上的多个元素，或者 bodyframe 框架上的其他对象，拥有一个指向该框架的局部变量将非常方便。为了节省一些不必要的按键操作，上面的代码可以写在一行上，如下所示。

```
var fullname = top.frames[2].document.forms[0].fullname.value;
```

然而，这段代码对于普通程序员来说更难阅读，并且稍微令人困惑。难以理解的代码往往是错误的根源。
除了使用 frames 数组，还可以通过名称访问框架。

```
var fullname = top.bodyframe.document.forms[0].fullname.value;
```

通过名称访问框架使代码更易于阅读，并允许在不进行大量代码更改的情况下重新排序框架。

#### 调用位于另一个框架中的JavaScript函数

你已经看到了如何从外部框架访问框架的内容（其表单和其他HTML组件），因此JavaScript变量和函数也可以从外部访问，这应该不会令人惊讶。

```
function sayhello() {
    // 此函数向用户说“你好”
    alert("Hello!");
}
```

```
<form action="#">
    <input type="button" value="Say Hello"
        onclick="top.menu.sayhello()">
</form>
```

![](img/f14dd58a324d5464a114c30c1d4c4c9b_257_0.png)

为了演示，让我们假设我们在 menu 框架中定义了一个名为 sayhello() 的JavaScript函数。

我们可以在 bodyframe 框架中定义一个按钮，当点击时，它将调用来自 menu 框架的 sayhello() 函数。

图10-6显示了在浏览器窗口中点击“Say Hello”按钮的结果。
只要JavaScript变量是在任何函数之外定义的，它们也可以从另一个框架访问。



#### 跨框架脚本可能存在的风险

*跨框架脚本* 是指当一个框架（源自某个域名，如 www.myserver.com）尝试通过 JavaScript 访问另一个源自不同域名（如 www.example.com）的框架时所发生的情况。

跨框架脚本的问题在于，一个网站可以定义一个指向安全网站（例如微软的 Hotmail）的框架。然后，该来源网站可以从此框架中获取任何 cookie 或其他敏感的用户信息，并允许他们以恶意方式使用这些信息。由于这存在安全风险，所有 IE 4 及更高版本的浏览器都不允许跨框架脚本。

#### 处理框架之间的同步

在上一节中，我们看到了一些依赖于另一个框架中 JavaScript 函数存在的 JavaScript 代码。

```
<form action="#">
    <input type="button" value="Say Hello"
        onclick="top.menu.sayhello()">
</form>
```

但是，如果用户在菜单框架尚未完成加载之前就点击了按钮，会发生什么？大多数网页浏览器以无特定顺序加载框架，并且很有可能（实际上是相当可能）某些框架会比其他框架加载得慢。在这种情况下，将发生 JavaScript 错误，因为无法找到 `sayhello()` 函数。

这个问题可以描述为一个同步问题。在处理相互通信的框架时，我们需要一种方法来确定所有框架在继续之前是否已完全加载。JavaScript 程序员可以采用几种技术来处理框架之间的同步。

第一种技术是在框架之间创建级联效果，其中每个框架负责加载依赖于它的框架。使用此方法，我们将让菜单框架加载 `bodyframe` 框架的内容。

```
top.bodyframe.document.location = "mainbody.html";
```

然后我们可以保证，当 `bodyframe` 文档完成加载时，菜单框架也已在浏览器窗口中加载完毕。

第二种技术是在框架集文档中创建一个或多个布尔型 JavaScript 变量。每个框架在完全加载后可以将其相应的布尔变量设置为 `true`。例如，我们可以将我们的框架集文档修改为以下 HTML 和 JavaScript 代码：

```
<html>
    <head>
        <title>Framesets</title>
        <script type="text/javascript" language="JavaScript">
        var banner_loaded = false;
        var menu_loaded = false;
        var body_loaded = false;
        </script>
    </head>
    <frameset rows="100, *">
        <frame src="banner.html" name="banner">
        <frameset cols="150, *">
            <frame src="menu.html" name="menu">
            <frame src="mainbody.html" name="bodyframe">
        </frameset>
    </frameset>
</html>
```

然后，我们可以在菜单框架的末尾添加以下 JavaScript 代码，以便将相应的变量设置为 `true`。

```
<script type="text/javascript" language="JavaScript">
    var menu_loaded = true;
</script>
```

在 `bodyframe` 的代码中，我们应该将调用 `sayhello()` 函数的部分移到一个单独的函数中，并为了安全起见，在其周围添加一个 **if** 语句。

```
<script type="text/javascript" language="JavaScript">
    function callhello() {
        // Check the variable named menu_loaded first
        if (top.menu_loaded == true) {
            top.menu.sayhello();
        }
    }
</script>
<form action="#">
    <input type="button" value="Say Hello" onclick="callhello()">
</form>
```

在此示例中，"Say Hello" 按钮在菜单框架完全加载之前将无法工作。

最后，我们可以使用类似于第 7 章中基于 DOM 的浏览器嗅探代码的技术。我们可以在访问框架和 `sayhello()` 函数之前，简单地测试它们是否存在。

```
<script type="text/javascript" language="JavaScript">
    function callhello() {
        // Check if the frame and function exist first
        if (top.menu) {
            if (top.menu.sayhello) {
                top.menu.sayhello();
            }
        }
    }
</script>
<form action="#">
    <input type="button" value="Say Hello" onclick="callhello()">
</form>
```

这种相同的技术可用于测试 JavaScript 变量或 Web 表单控件是否存在。

在下一章中，我们将研究构成 DOM 的各种对象。正是通过这些对象的方法和属性，我们才能够与网页浏览器进行交互。

### 第 11 章 与网页浏览器交互

![](img/f14dd58a324d5464a114c30c1d4c4c9b_262_0.png)

#### 如何用 JavaScript 做所有事情

#### 如何...

- 操控网页内容
- 检查整个浏览器窗口
- 从网页浏览器软件检索属性
- 检查操作系统的显示设置
- 访问网页浏览器历史记录列表
- 将浏览器引导至新位置

尽管 JavaScript 拥有强大而灵活的核心语言语法，但它没有任何内置函数用于从文件、数据库或键盘输入读取数据，也没有用于将数据写入屏幕或打印机的函数。在其每种环境中，JavaScript 都依赖于一个外部对象模型来提供基本的输入输出功能。

表 11-1 列出了一些支持 JavaScript（或其某些版本）的环境，以及为超出核心 JavaScript 功能提供附加功能的对象模型。

| JavaScript 环境 | 对象模型 |
|------------------------|----------------|
| 网页浏览器 | DOM |
| .NET (JScript) | .NET Framework |
| ASP (JScript) | ASP 对象模型 |
| 服务器端 JavaScript | 服务器端扩展 |

表 11-1 JavaScript 环境及其各自的对象模型

#### 了解文档对象模型的基础知识

要理解 DOM，您必须首先了解该规范是如何演变的。原始的 DOM 中有六个基本对象，有时称为 DOM Level 0：

- document
- window
- history
- location
- screen
- navigator

DOM 0 还定义了一些其他对象，例如表单、框架和图像。但是，为了访问这些对象，程序必须通过此处列出的顶层对象。由于 DOM 0 是静态的，且文档在浏览器渲染后无法更改，因此对象不能被动态创建、修改或删除。图 11-1 是原始 DOM 中对象及其相互关系的良好示意图。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_264_0.png)

图 11-1 原始的 Netscape DOM

## 246 如何用 JavaScript 做所有事情

1998 年，当 W3C 采用 DOM 作为新的 Web 标准时，它被称为 *DOM Level 1*，有时缩写为 *DOM 1*。DOM 1 是首次尝试将对象模型适应于新兴的 XML 标准，该标准将彻底改变结构化文档格式。

> **注意：** 与后续版本的 DOM 不同，DOM Level 0 从未是一个官方标准。

DOM 标准将 HTML（和 XML）文档视为数据的层次结构（称为 *节点*）。在 DOM 中，文档的以下部分都被视为节点：

- 标记标签（元素）
- 属性
- 文本
- XML 字符数据（CDATA）节
- 实体引用
- 实体
- 处理指令
- 注释
- 文档本身

包含在其他节点中的节点被视为这些节点的子节点，而与其他节点处于同一级别的节点被视为兄弟节点。

DOM 1 允许程序员访问、添加、删除、移动或修改 DOM 树中几乎所有的对象。更具体地说，DOM 1 将一组核心 API 与一组特定于 HTML 的 API 分开。特定于 HTML 的 API 向核心集中定义的对象添加了与浏览器相关的方法和属性。

例如，让我们考虑以下简单的 HTML 代码：

```
<html>
    <head><title>My title</title></head>
    <body>
        This is <b>a test</b> of the <i>emergency broadcast system</i>.
        I repeat, this is only a test.
    </body>
</html>
```

图 11-2 显示了上述 HTML 代码在 DOM 1 层次结构中的样子。此层次结构也称为 *DOM 树*。

下一个版本的 DOM，称为 *Level 2*，于 2000 年 11 月成为正式的 W3C 标准。核心标准与上一版本相比没有太大变化，因为 DOM 2 只是在 DOM 1 中已定义的接口上添加了一些新的属性和方法。它的



#### XPath 的用途

其主要目的是为 DOM API 添加对视图、事件和样式表的支持。它还定义了 DOM 遍历的规范，即能够向前和向后遍历 DOM 层次结构的能力。

在本书出版时，DOM Level 3 仍处于 W3C 工作草案阶段。DOM 3 提议向核心规范添加两个新接口，并还将添加对 XPath 的支持。

XPath 是一种简单而强大的语言，用于寻址 XML 文档的各个部分。例如，你会使用以下 XPath 表达式来访问 XHTML 网页上的第一个 <form> 元素。

此表达式将匹配作为 <body> 元素后代（但不一定是直接子元素）的第一个 <form> 元素，而 <body> 元素本身又是根 <html> 元素的直接子元素。

本章剩余部分将重点介绍针对 DOM 1 的 JavaScript 编程，因为当今使用的绝大多数浏览器都支持该版本。

#### 操作网页内容

在所有 DOM 对象中，document 对象可能是最有用的。document 对象提供了对整个网页内容的访问，因为它是 HTML 层次结构中所有其他对象的根。在图 11-2 中，document 对象位于树顶，代表 `<html>` 元素。

在 JavaScript 中，document 对象包含以下五个数组：

- images
- applets
- links
- forms
- anchors

document 对象的每个数组都包含网页上相关元素的枚举列表。images 数组包含图像列表，applets 数组包含 Java 小程序列表，依此类推。我们已经看到 forms 数组是访问网页上所有 HTML `<form>` 元素的便捷方式。

除了这五个数组，document 对象还通过 document.cookie 属性为 JavaScript 提供了对网站关联的任何 cookies 的读写访问。*cookie* 是一段文本，浏览器会代表网站将其存储在本地。Cookie 经常用于存储用户 ID 和会话信息，以便当用户返回时，网站能够识别已知用户。

document 对象还包含以下六个方法：

- open()
- close()
- write()
- writeln()
- getElementById()
- getElementsByName()

open()、close()、write() 和 writeln() 方法用于将原始 HTML 文本打印到网页上。我在本书的示例代码中经常使用 document.write() 作为输出结果的简单方式。

getElementById() 和 getElementsByName() 方法允许我们快速在 DOM 中搜索特定元素。这是一种比手动上下搜索 DOM 树寻找所需内容更好的方法，因为这些函数经过优化，可以快速返回结果。

如果我们希望在没有各种数组（如 forms 数组）或内置搜索功能（如 getElementById）便利的情况下浏览 HTML 文档的内容，可以直接访问 document 对象的 body 属性。body 属性允许我们访问 document 对象下的所有 HTML 对象，从 HTML `<body>` 元素开始。此属性通常不在 JavaScript 编程中使用，因为使用 document 数组或内置搜索函数搜索 DOM 通常更快、更容易。

#### 动态修改网页内容

将 JavaScript 和 DOM 结合使用的更有趣方式之一是创建可以根据用户行为自行更改的网页。这可以在不涉及 Web 服务器本身的情况下完成。让我们从一个非常基本的网页开始。

```
<html>
    <head><title>Basic Web Page</title></head>
    <body>
        <h2>The time now is: <span id="time">00:00:00</span></h2>
    </body>
</html>
```

如图 11-3 所示，此 HTML 代码创建了一个静态网页。无论在一天中的什么时间，它总是报告时间为 00:00:00（午夜）。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_268_0.png)

但如果我们想在页面上添加一个小的 JavaScript 脚本，让它不断将时间更新为正确的时间呢？我们可以使用 DOM document 对象来修改网页的内容。

```
<script language="JavaScript" type="text/javascript">
function update_time() {
    // The current date and time
    var rightnow = new Date();

    // Capture the hours as a string, "00" thru "23"
    var hours = rightnow.getHours();
    if (hours < 10)
        var hourstring = "0" + hours.toString();
    else
        var hourstring = hours.toString();

    // Capture the minutes as a string, "00" thru "59"
    var minutes = rightnow.getMinutes();
    if (minutes < 10)
        var minutestring = "0" + minutes.toString();
    else
        var minutestring = minutes.toString();

    // Capture the seconds as a string, "00" thru "59"
    var seconds = rightnow.getSeconds();
    if (seconds < 10)
        var secondstring = "0" + seconds.toString();
    else
        var secondstring = seconds.toString();

    // Put it all together, "00:00:00"
    var timestring = hourstring + ":" + minutestring + ":" + secondstring;

    // Manipulate the DOM, display it to the screen!
    var timeplace = document.getElementById("time");
    timeplace.childNodes[0].nodeValue = timestring;
}
</script>
```

通过在文档首次加载时调用 update_time() 函数，我们可以让浏览器用当前时间替换字符串 "00:00:00"。

```
<body onload="update_time()">
```

图 11-4 中的屏幕截图显示了浏览器如何用正确的时间替换原始 HTML 字符串。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_270_0.png)

使用 document 对象用正确的时间更新网页

使用浏览器定时器，我们甚至可以让网页每秒钟都用正确的时间更新。我们需要做的就是在 update_time() 函数的末尾添加以下代码。

```
setTimeout('update_time()', 1000);
```

setTimeout() 函数告诉 JavaScript 我们希望在将来的某个时间执行某些 JavaScript 代码。在前面的代码中，我们表示希望从现在起 1,000 毫秒（1 秒）后调用 update_time() 函数。这将导致 update_time() 函数每秒被调用一次，直到用户离开该网页。

#### 更改下拉列表框中的项目

开发人员不仅可以修改 HTML 网页的内容，甚至下拉列表框中的项目也可以在网页加载后更改。

```
How many calories does a cheeseburger contain?<br>
<select id="listbox1">
<option>-- Please Select One --</option>
</select>

<script language="JavaScript" type="text/javascript">
```

```
var counter;
var listbox = document.getElementById("listbox1");
for (counter = 100; counter < 500; counter += 50) {
    listbox.options[listbox.length] =
        new Option(counter + " - " + (counter+49));
}
</script>
```

前面的代码创建了一个 HTML 下拉列表框，其中包含一个项目——“请选择一个”。然后使用 JavaScript，它又向列表中添加了八个更多项目。我们的 JavaScript 代码首先获取对列表框的引用，并将其存储在名为 listbox 的变量中。然后使用 **for** 循环，我们创建几个新的 Option 对象并将它们添加到 options 数组的末尾。

你可以在这里看到浏览器如何显示我们的动态列表框。（不过，我不想知道一个芝士汉堡实际上含有多少卡路里。）

![](img/f14dd58a324d5464a114c30c1d4c4c9b_271_0.png)

#### 检查整个浏览器窗口

从技术上讲，window 对象不是官方的 DOM Level 1 对象。它提供了对其他框架或打开的浏览器窗口的访问。

在上一章中，我们了解到 JavaScript 中有四种类型的 window 对象。表 11-2 总结了这些对象。

##### 表 11-2 — JavaScript 窗口对象

| 对象名称 | 描述 |
| --- | --- |
| window | 当前框架或窗口 |
| top | 最顶层的窗口 |
| parent | 包含当前框架的框架集（不一定是最顶层的窗口） |
| self | 当前框架或窗口；与 window 对象相同 |

这四个窗口对象可能（也可能不）指向浏览器中不同的窗口。通常，对于不包含框架集的网页，所有四个对象都引用相同的底层窗口。

window 对象提供了对三个底层 DOM 对象的访问：

- document
- history
- location

我们在上一节讨论了 document，在接下来的章节中，我们将有机会了解 history 和 location。

window 对象还通过 status 属性提供了对浏览器状态栏的访问。状态栏是主浏览器窗口下方的狭窄区域，通常报告页面加载的进度，并在鼠标指针移动到其上时显示超链接的 URL。以下 JavaScript 代码将浏览器状态栏修改为自定义值：

```
window.status = "Welcome to my web site!";
```

下面的屏幕截图显示了网页加载后此操作对状态栏的影响。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_272_0.png)

在上一章中，你还了解到 window 对象包含一个名为 frames 的数组，该数组枚举了框架集中的所有框架。通过 frames 数组，我们可以访问位于另一个框架中的 HTML 和 JavaScript 代码。

window 对象还提供了几种可用于与用户通信或打开和关闭新浏览器窗口的方法。表 11-3 列出了一些更有趣的 window 方法。



## 254 如何用 JavaScript 实现一切

| 方法 | 描述 |
| :--- | :--- |
| alert() | 创建一个警告对话框 |
| blur() | 使窗口失去焦点 |
| close() | 尝试关闭浏览器窗口 |
| focus() | 使窗口获得焦点 |
| moveBy(), moveTo() | 重新定位浏览器窗口 |
| navigate() | 将特定 URL 加载到浏览器中 |
| open() | 打开一个新的浏览器窗口 |
| print() | 尝试将浏览器内容打印到打印机 |
| resizeBy(), resizeTo() | 调整浏览器窗口大小 |
| scroll(), scrollBy(), scrollTo() | 使窗口滚动 |
| setTimeout(), clearTimeout() | 使 JavaScript 代码在指定的延迟后执行 |

表 11-3 有用的 window 方法

一个有趣的 window 方法是 open()。当你不想中断当前网页时，可以使用此方法来创建一个新的浏览器窗口。遗憾的是，这正是大多数弹出式网络广告所使用的技术。然而，当需要根据用户请求引导他们访问某些在线帮助（如用户手册或在线词汇表）时，它仍然非常有用。

```javascript
window.open("userhelp.htm", "_blank",
  "height=300,width=200,toolbar=no," +
  "status=no,menubar=no,location=no");
```

上述代码将打开一个新的浏览器窗口，并将其定向到 HTML 文件 userhelp.htm。该代码指定了窗口的特定高度和宽度（300 乘 200），并移除了所有工具栏、菜单栏和状态栏，留下一个简洁的窗口。
图 11-5 展示了这种新的 HTML 窗口在典型网络浏览器中的外观。

![图 11-5：弹出窗口可用于提供快速在线帮助。](img/f14dd58a324d5464a114c30c1d4c4c9b_274_0.png)

#### 检索网络浏览器软件的属性

Netscape 的程序员们可能至今仍会为一件事感到些许欣慰：用于检索浏览器信息的标准对象名为 navigator，这名称源于 Web 早期使用最广泛的浏览器。你可能还记得，我们在第 7 章讨论过 navigator 对象的一些属性，当时用它来从用户的浏览器获取名称和版本信息。

navigator 对象包含一个名为 plugins 的数组。该数组包含浏览器插件的列表（尽管列表内容因浏览器制造商而异）。浏览器插件是一种在浏览器内部运行的应用程序，通常用于为嵌入式多媒体提供支持。Shockwave Flash 和 RealNetworks RealPlayer 是两款流行的插件。

在 Netscape 和 Mozilla 网络浏览器中，plugins 数组可用于确定客户端 PC 上安装了哪些浏览器插件。在 Internet Explorer 中，plugins 数组中列出的唯一插件是当前网页上正在使用的插件。

例如，以下代码（适用于 Netscape 网络浏览器）检查用户的计算机上是否安装了 Macromedia Flash 插件。

```javascript
var flashinstalled = false;
for (var i=0; i < navigator.plugins.length; i++) {
    if (navigator.plugins[i].name == "Shockwave Flash") {
        flashinstalled = true;
        break;
    }
}

if (flashinstalled) {
    document.write ("I see you have Macromedia Flash installed!");
} else {
    document.write ("If you want to see the multimedia installed ");
    document.write ("on this web site, you will need to install ");
    document.write ("Macromedia Flash.");
}
```

navigator 对象还支持几个属性，例如以下这些。

- appCodeName
- appName
- appVersion
- userAgent
- userLanguage

这些属性为 JavaScript 提供了关于客户端计算机上运行的精确浏览器类型的重要信息。例如，你可能希望为旧版浏览器（版本 4）提供以更简单方式格式化的内容，而为使用较新浏览器的访客提供依赖样式表的内容。

#### 检查操作系统的显示设置

网络开发人员在开发网页时通常会考虑特定的屏幕尺寸。例如，一些网站是为 800 像素宽、600 像素高的屏幕（通常称为 *800 乘 600 分辨率*）开发的。如果用户的分辨率较小，比如 640 乘 480，他们将无法看到页面的某些部分。如果用户的分辨率较大，比如 1024 乘 768，网页将会出现大量空白。

设计最佳的网站通常会根据可用空间自动扩展或收缩。我们在使用相对尺寸的框架中见过这种效果，使用 HTML 表格也可以实现。这两种解决方案都允许浏览器根据可用屏幕空间的量自动调整组件大小。（你有时可能会听到可用的屏幕空间被称为 *real estate*。）

但是，在处理动态 HTML（其中元素经常被放置在屏幕上特定的 X 和 Y 坐标）时，拥有一些关于屏幕分辨率的信息会很有帮助。DOM 提供了 screen 对象，以便 JavaScript 能够获取更多关于用户显示器技术属性的信息。

screen 对象并非 JavaScript 初始版本的一部分。它是在 IE 和 Netscape 浏览器的第 4 版中添加的。下表列出了此对象的部分属性。

| 属性名 | 用途 |
|-------------|---------|
| availHeight | 返回系统屏幕工作区域的高度，不包括 Windows 任务栏 |
| availWidth | 返回系统屏幕工作区域的宽度，不包括 Windows 任务栏 |
| colorDepth | 返回用于颜色的每像素位数 |
| height | 返回屏幕的垂直分辨率 |
| width | 返回屏幕的水平分辨率 |

例如，以下 JavaScript 代码允许你调整浏览器窗口大小，然后将其居中显示在用户的显示器上。

```javascript
var newTopLeftX = (screen.availWidth - 640) / 2.0;
var newTopLeftY = (screen.availHeight - 480) / 2.0;
window.resizeTo(640, 480);
window.moveTo(newTopLeftX, newTopLeftY);
```

该代码使用 window.resize() 函数将浏览器调整为 640 像素宽、480 像素高。然后使用一种常见的居中技术，将窗口完美地放置在屏幕中央，无论用户的显示器分辨率设置如何。

#### 访问网络浏览器历史记录列表

JavaScript 通过 history 对象对浏览器历史记录列表的访问权限有限。浏览器历史记录列表是你最近访问过的网页的有序列表，它由你的网络浏览器内部存储。每次使用浏览器的“后退”和“前进”按钮时，你都在访问浏览器历史记录列表。

通过 history 对象，JavaScript 能够让浏览器返回上一个网页——或者回退任意数量的网页。例如，以下 JavaScript 代码将使浏览器跳转到在当前页面之前最近访问的网页。

```javascript
history.back();
```

程序员还可以通过向 history 对象的 go() 方法指定一个整数来告诉浏览器回退任意数量的页面。以下代码将使浏览器回退五页。

```javascript
history.go(-5);
```

history 对象只有一个属性，length。length 属性将返回历史记录列表中的项目数量。

history 对象有三个方法。

| 方法名 | 用途 |
| --- | --- |
| back() | 在历史记录列表中后退一项；模拟浏览器的“后退”按钮。 |
| forward() | 在历史记录列表中前进一项；模拟浏览器的“前进”按钮。 |
| go() | 在历史记录列表中按指定数量前进或后退；正数前进，负数后退。 |

history 对象通常被用作将用户引导回上一页的简便方法。

```html
<html>
  <head><title>User Login Script</title></head>
  <body>

  <h1>Error: Unable to Log In</h1>

  I'm sorry, the password you supplied was incorrect.
  Please use the Back button on your browser to try again,
  or <a href="javascript:history.back()">click here</a> to
```



出于安全原因，history 对象不允许 JavaScript 访问你所访问网页的名称或 URL。

#### 将浏览器导航到新位置

location 对象允许 JavaScript 访问浏览器的地址栏。具体来说，程序员可以确定当前页面的 URL、重新加载当前页面，或将浏览器导航到新的 URL。location 对象有八个属性。

| 属性名 | 用途 |
| :--- | :--- |
| href | 获取或设置完整的 URL 字符串 |
| hash | 获取或设置 URL 中井号（#）之后的部分 |
| host | 获取或设置 URL 中的主机名和端口号部分 |
| hostname | 获取或设置 URL 中的主机名部分 |
| pathname | 获取或设置网页的文件名或路径 |
| port | 获取或设置 URL 中的端口号部分 |
| protocol | 获取或设置 URL 的网络协议名称（例如 HTTP） |
| search | 获取或设置 URL 中问号（?）之后的部分 |

location 对象还有三个方法。

| 方法名 | 用途 |
| :--- | :--- |
| assign | 加载一个新的网页 |
| reload | 重新加载当前网页 |
| replace | 通过加载新网页来替换当前网页 |

location 对象通常用于将浏览器重定向到新的网页。

```
location.href = "http://www.example.com/another/page.html";
```

但它也可以仅用于重新加载当前页面，类似于浏览器的刷新操作。

```
location.reload();
```

在下一章中，我们将探讨如何使用 JavaScript、CSS 和动态 HTML 来实现一些简单的动画效果。通过一种称为*绝对定位*的技术，我们能够在网页中将文本和图片放置在任意想要的位置。

### 第 12 章 实现简单动画

![](img/f14dd58a324d5464a114c30c1d4c4c9b_278_0.png)

260 JavaScript 完全指南

#### 本章内容

- 使用样式表格式化网页
- 控制文本和图片的定位
- 使用 JavaScript 修改样式
- 使用 JavaScript 实现基本动画

在第 11 章中，你已经了解了如何使用 JavaScript 操控浏览器 DOM，以便在网页加载完成后修改其中的 HTML 内容。这种技术常用于让 JavaScript 响应用户事件或输入，而无需返回 Web 服务器重新生成页面。

正如你将在本章中看到的，层叠样式表（CSS）允许开发者精确指定网页中元素的布局和定位。样式表也可以在 JavaScript 中动态修改，从而改变元素的外观，甚至将其移动到屏幕上的不同位置。

动画本质上不过是使用 JavaScript 对 DOM 和/或样式表进行反复操作。一只动画蝴蝶之所以看起来能在屏幕上翩翩飞舞，不过是反复切换少量图片并缓慢地将这些图片在页面上重新定位的结果。在本章中，我们将探讨如何使用 JavaScript 动态修改样式表，以及如何利用这一技术创建一些简单的动画效果。

#### 学习层叠样式表的基础知识

我们之前已经简要提到过样式表的主题，但在本节中我们将更深入地探讨，以更好地了解样式表能为 Web 开发者提供什么，以及 JavaScript 如何被用来动态影响样式。

网页的样式是指网页内容（如文本和图形）的格式化和排列方式。样式涵盖的内容非常广泛，从字体和颜色的使用，到浏览器窗口内对象的大小和定位。

1991 年 Web 刚刚诞生时，很少有人关注样式——重点在于内容。Web 被用于展示和链接相关的文本文档。事实上，其设计的核心理念之一是，Web 客户端（通常是浏览器）应负责以最合适的方式来渲染网页。

例如，`<h1>` 标签仅仅定义了一级标题，而具体的字体类型和大小则由浏览器自行决定。理论上，`<h1>` 标签中的内容在不同品牌的浏览器或不同的操作系统上看起来可能完全不同。

当然，许多开发者需要更精确的方法来格式化网页内容，因此有时会使用一些相当复杂的方案来实现复杂的页面布局，例如使用不可见的图片来帮助解决间距问题。

#### 为什么 CSS 是"层叠"的

我们说样式表具有*层叠*特性，是因为除少数例外情况外，HTML 元素会继承其包含元素的样式属性。例如，假设你有一个位于 `<u>` 元素内部的 `<b>` 元素：

```
<u>This is <b>some</b> text.</u>
```

如果你为 `<u>` 元素设置了 CSS **font** 属性，那么 `<b>` 元素也会继承该字体设置。不过，你可以通过为 `<b>` 元素指定不同的字体设置来覆盖层叠效果。

W3C 于 1996 年底推出了 CSS 第一级标准。IE 3 是第一个部分支持这一新标准的浏览器，Netscape 4 也很快跟进，对 CSS 提供了部分支持（尽管存在大量缺陷）。

*样式表*是一组定义，用于描述一组 HTML 元素的样式。通过使用样式表，你可以完全重新定义某个元素在 Web 浏览器中的呈现方式，因为每个元素都公开了许多属性，其值可以被更改。

> W3C 有一个非常好的网站，可以让你更深入地了解样式表，请访问 http://www.w3.org/Style。

#### 使用 HTML 元素为网页分配样式

最初格式化网页内容的方法是使用与 HTML 样式相关的元素和属性。例如，`<font>` 标签可用于设置文档中文本的字体、大小或颜色。`<b>` 标签可用于将文本加粗，`<i>` 可创建斜体，依此类推。

然而，由于多种原因，这是一种非常低效的网页样式化方法：

- 网页的样式和布局无法在两个或多个 HTML 文件之间轻松复用，这给网页制作者带来了额外的开发工作。
- 需要使用框架、嵌套表格、不可见图片以及其他复杂且混乱的技术来将文本或图形放置在特定位置。
- 重复的 HTML 样式标签（如 `<font>` 标签）需要在同一网页上多次重复使用。
- 更改整个网页或整个网站的样式需要大量工作。
- 网页文件更大，意味着下载到浏览器所需的时间更长。

#### 如何在 HTML 中指定颜色

在 HTML、CSS 和 JavaScript 中有多处需要程序员指定颜色。例如，HTML 的 `<font>` 标签有一个 **color** 属性，可用于指定字体颜色。

颜色可以通过名称或 RGB（红-绿-蓝）值来指定。HTML 中预定义了多种颜色名称，如 black、white、yellow 和 blue。预定义颜色有几十种。

如果你想使用一个没有预定义名称的颜色，可以指定一个精确的 RGB 值。RGB 值以井号（#）开头，后跟三组十六进制数字，例如 #FF33C0。

第一组十六进制数字表示颜色中红色的分量，范围从 00（最暗）到 FF（最亮）——即 256 种不同的红色设置。第二组表示绿色的分量，第三组表示蓝色的分量。

因此，颜色 #FF33C0 代表亮红色、深绿色和中蓝色的组合，看起来非常像紫红色（一种明亮的偏紫粉色）。#FFFFFF 代表纯白色，#000000 代表纯黑色。

例如，以下 HTML 代码定义了一个具有中等复杂度样式的页面。由于需要大量额外的 HTML 标签和属性，HTML 代码显得杂乱且难以阅读。

```
<html>
  <head><title>Style sheets example</title></head>
  <body bgcolor="white" link="purple" vlink="green">
    
    <center>
      <h1>
        <font color="#333399" face="Arial">
          Introduction to XML
        </font>
      </h1>
    </center>
    
    <p><font color="#993333" face="Arial" size="3">
    &nbsp;&nbsp;&nbsp;&nbsp;<b>XML is one of the most
    important new standards to come out of the W3C<br>
    &nbsp;&nbsp;&nbsp;&nbsp;since HTML.</b> All developers
```



应当了解XML是什么以及如何正确使用。本文将介绍XML的基础知识，包括对DTD的讨论。

前文的代码中包含了多个格式化标签，如`<center>`、`<font>`和`<b>`。还使用了多个不间断空格（`&nbsp;`）来帮助段落缩进，并且`<body>`标签包含了三个与样式相关的属性。此外，我还必须添加手动换行符（`<br>`）来人为设置文本换行的位置。

图12-1展示了浏览器如何根据我们的示例HTML代码渲染出一个样式良好的页面。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_282_0.png)

#### 使用样式表为网页分配样式

当然，我们也可以使用样式表创建与图12-1所示相同的效果。然而，样式表的解决方案将更整洁、更易于开发，并且在未来更易于维护。我们甚至可以将此样式定义与任意多个其他网页共享，从而节省宝贵的开发时间。我们还可以用这种方式做一些HTML样式标签无法实现的很酷的事情。

首先，我们将从网页示例中移除所有的HTML样式标签和属性，转而使用HTML `<div>`标签来标记需要设置样式的文本。

```
<html>
    <head><title>Style sheets example</title></head>
    <body>

        <div id="heading">
            Introduction to XML
        </div>

        <div id="summary">
            <span id="boldintro">
                XML is one of the most important new standards to come
                out of the W3C since HTML.
            </span>

            All developers should be aware of what XML is and how it
            should be used. In this article, we introduce the basics
            of XML, including a discussion on DTDs.
        </div>

    </body>
</html>
```

我们可以为这个文档创建一个简单的样式表，并使用HTML `<style>`元素将其插入到网页中。`<style>`元素应位于文档的`<head>`部分内。

```
<style type="text/css">
#heading {
    font: 24pt Arial;
    color: #333399;
    text-align: center;
    margin-bottom: 20pt;
}

#summary {
    font: 12pt Arial;
    color: #993333;
    margin-left: 20pt;
}

#boldintro {
    font-weight: bold;
}
</style>
```

我们将在本章后面探讨样式表本身的语法。但即使不知道样式表的具体含义，你也能看出它的作用。生成的网页与使用传统HTML样式化的图12-1所示页面几乎完全相同，但样式表方法要灵活和强大得多。

#### 使用`<div>`和`<span>`标记动态文本

HTML 4.01提供了两个特殊元素来支持CSS和HTML的集成：`<div>`和`<span>`。

`<div>`元素是文本块的标记。*文本块*是一个或多个完整的段落，必须在新行上开始和结束。`<div>`元素使得文档更容易使用样式表进行样式设置。

```
<div id="FirstError">Error! You have entered an incorrect user ID
and/or password. Please try again, and if you continue to have
difficulty, please contact a system administrator for help.</div>
```

`<span>`元素与之非常相似，但它处理的是内联文本。*内联文本*不必在新行上开始或结束，因此`<span>`可用于为单个字符、单词或句子应用样式。

```
<span style="font-size:14pt">H</span>is main goal in life was
<span style="font-weight:bold">world domination</span>, although
tonight he was willing to settle for a nice steak and a cold beer.
```

`<div>`和`<span>`的主要属性是 **id**、**style** 和 **class**。**id** 允许你为包含的文本指定一个名称，这使得使用JavaScript或CSS访问文本变得容易。**style** 属性允许你直接在HTML中指定CSS。**class** 属性类似于 **id** 属性，区别在于多个标签可以具有相同的 **class** 属性，而 **id** 属性对于单个标签是唯一的。

#### 定义内联样式

HTML标准允许使用一种称为*内联样式*的技术在文档主体内部定义CSS样式语法。大多数HTML元素都有一个名为 **style** 的属性，可以接受CSS定义，如下所示：

```
<p style="font:Arial;font-weight:bold">
    This is some text
</p>
```

#### 如何用JavaScript做所有事情

使用这种技术快速而方便，但你会失去使用样式表的一些好处。具体来说，文档主体仍然复杂、杂乱且难以维护。样式表代码无法轻松重用。实际上，由于样式完全没有与内容分离，这种技术等同于使用HTML样式标签和属性。

你得到的一个好处是能够使用HTML样式标签方法无法实现的复杂样式。对于小型网页或有独特样式要求的网页，这可能是一种可接受的方法。

#### 定义嵌入式样式表

比内联样式更进一步的是使用嵌入式样式表。*嵌入式样式表*是使用HTML `<style>`标签在文档头部部分内定义的样式表。以这种方式定义的样式对整个网页可用，因此完全有可能为一个大型复杂的文档只定义一两个样式定义。

样式表由一条或多条规则组成。*规则*是样式的单个定义，格式如下：

```
selector {
    attribute1 : value;
    attribute2 : value;
    ...
    attributeN : value;
}
```

例如，在前面的部分中，我们有一个包含三条规则的样式表。其中一条规则是用以下代码定义的：

```
#summary {
    font: 12pt Arial;
    color: #993333;
    margin-left: 20pt;
}
```

该规则有一个选择器（`#summary`），并为三个属性（font、color和margin-left）定义了值。*选择器*决定了哪些HTML标签的属性被设置为指定的值。顺便说一句，规则不必像我一直做的那样跨多行排列。如果你愿意，可以将规则放在一行，或者为了提高可读性而将其拆分成更多行。

下表展示了CSS中选择器的工作方式。

| 选择器 | 受影响的HTML代码 |
| :--- | :--- |
| h1 | 影响文档中所有的`<h1>`标签。 |
| #heading | 影响 **id** 属性设置为heading的标签。 |
| .blue | 影响所有 **class** 属性设置为blue的标签。 |
| p#heading | 影响文档中所有 **id** 属性设置为heading的`<p>`标签。 |
| p.blue | 影响文档中所有 **class** 属性设置为blue的`<p>`标签。 |
| h1, h2, h3 | 影响文档中所有的`<h1>`、`<h2>`和`<h3>`标签。 |
| p b | 影响所有包含在`<p>`标签内的`<b>`标签；不在`<p>`标签内的`<b>`标签不受影响。 |
| ul ul li | 影响至少在两个`<ul>`标签内的所有`<li>`标签。 |
| div .red | 影响所有 **class** 属性设置为red且同时位于 **div** 属性内的标签。 |

如你所见，有一次性为整个文档设置样式的方法，也有设置文档中非常具体元素样式的方法。最终，你可以使用复杂的选择器创建一些非常复杂和全面的样式表。

#### 导入外部样式

有两种方法可以将样式表从外部文件导入HTML文档：

- HTML `<link>`元素
- 样式表 `@import` 命令

这意味着你可以创建一个单一的样式表文件，并将其应用于网站上的所有页面。只需在文本编辑器中简单敲几下键盘，你就可以彻底改变网站上所有页面的样式。

要使用`<link>`元素，请将以下HTML代码放置在网页的`<head>`部分：

```
<link rel="STYLESHEET" type="text/css"
      href="http://www.example.com/mystyle.css">
```

前面的代码将把位于 http://www.example.com/mystyle.css 的样式表导入到网页中。文件扩展名 `.css` 通常用于样式表。

要使用 `@import` 命令导入相同的样式表，我们实际上需要在文档头部添加一个 `<style>` 部分。

```
<style type="text/css">
    @import url(http://www.example.com/mystyle.css);
</style>
```

所有三种类型的样式表（内联、嵌入式和外部）可以在单个文档中组合使用。如果样式冲突，则内联样式优先，其次是嵌入式样式，最后是外部样式。



#### 使用基本样式属性

正如"定义嵌入式样式表"一节中所提到的，样式表由一条或多条规则组成，而规则则由一个选择器加上一个或多个属性构成。本节我们将介绍可用于设置样式的不同类型的属性。

官方 CSS 1 规范中定义了数十种属性——数量之多，以至于本书无法逐一涵盖。关于可用 CSS 属性的更多信息，我推荐以下两个优秀的资料来源：

- 官方 W3C CSS 1 规范可在 http://www.w3.org/TR/REC-CSS1 找到。
- 微软 MSDN 网站提供了出色的参考指南，地址为 http://msdn.microsoft.com/workshop/author/css/reference/css_ref_entry.asp。

MSDN 参考指南的组织尤为出色；CSS 属性与其相关的 HTML 元素之间进行了交叉引用。事实上，我认为该网站是互联网上最完整的 Web 编程参考——不仅涵盖 CSS，还包括所有与 Web 相关的编程主题。

表 12-1 描述了一些最常用的 CSS 属性。

| 属性名 | 用途 |
| --- | --- |
| font | 允许你设置多达十几种字体相关属性，包括大小和样式 |
| color | 允许你设置元素的前景色 |
| background | 允许你设置多达五种背景相关属性，包括颜色和图片 |
| text-align | 允许你设置文本的左对齐、居中或右对齐 |
| margin | 允许你设置元素周围空白区域的大小 |
| border | 允许你设置元素边框的大小、样式和颜色 |

**表 12-1** 常用 CSS 属性

表 12-1 中列出的若干属性是*复合属性*；也就是说，它们允许你同时设置元素的多个属性。例如，**font** 属性允许你在一个字符串中设置多达 14 种字体相关属性：

```css
BODY {
    font: italic normal bold 12pt Arial;
}
```

这种便捷的简写等价于以下代码：

```css
BODY {
    font-style: italic;
    font-variant: normal;
    font-weight: bold;
    font-size: 12pt;
    font-family: Arial;
}
```

由此可见，复合属性节省了时间和精力，但也增加了额外的复杂性，因为它们更难构造。

#### 在网页上定位元素

一些 CSS 属性与文本样式无关，而是涉及布局和定位。设置元素的定位可以让你指定对象的精确尺寸（高度和宽度）以及其在屏幕上的精确物理位置（x 和 y 坐标）。

例如，假设我们有以下 HTML 代码：

```html
<html>
    <head>
        <title>Style sheets example</title>
        <link rel="STYLESHEET" type="text/css"
              href="example.css">
    </head>
    <body>

        <div id="special">This is a great example of separating
        content from layout. From an HTML perspective, this text
        is a pretty simple paragraph, with no formatting requirements.
        Browsers that do not support style sheets will render
        this text to the screen in a plain and simple manner.
        </div>

    </body>
</html>
```

这段 HTML 代码不包含任何格式化指令。我们所做的一切只是用 `<div>` 标签包裹了一段文本。`<div>` 标签除了提供一种为文本块命名的方式外，不产生任何其他效果。（我们在本章前面的"使用 `<div>` 和 `<span>` 标记动态文本"一节中已经探讨过 `<div>` 和 `<span>` 的区别。）

不过，我们的 HTML 代码确实包含一个对样式表文件的 `<link>` 引用。该文件 example.css 将包含我们要使用的格式化指令。在本例中，它将定义 CSS 定位属性。

example.css 文件将包含以下代码：

```css
#special {
    position: absolute;
    top: 50px;
    left: 100px;
    width: 3in;

    background-color: #CCCCCC;
    padding: 15px;
    font: 12pt Arial;
    border: solid 2pt black;
}
```

上述样式表包含四个 CSS 尺寸和定位属性：

- **position** 告诉浏览器我们希望自行定位内容
- **top** 设置元素上边缘的位置
- **left** 设置元素左边缘的位置
- **width** 设置元素的宽度

在本例中，元素是围绕我们文本的 `<div>` 标签。该 `<div>` 标签有一个值为 **special** 的 **id** 属性，与分配给该规则的 #special 选择器相匹配。

还有一些未使用的附加定位属性，最值得注意的是 **height**，它可用于设置元素的高度。在本例中，我们允许浏览器根据文本内容的大小来计算元素的合适高度。还有一个名为 **visibility** 的属性，可以使元素不可见。

图 12-2 展示了 HTML 文档中的文本如何按照样式表中的指定进行了精确的定位和尺寸设置。

#### 使用 JavaScript 修改样式

在了解了样式表是什么以及如何使用它们来格式化网页之后，我们来看看如何使用 JavaScript 动态修改样式。

DOM 为 JavaScript 提供了访问页面上几乎所有对象样式相关属性的途径。例如，假设我们有如下定义的 Web 表单：

```html
<form action="#" method="get">

    <div style="position:absolute;top:50px;left:100px;">

    Full Name:<br>
    <input type="text" name="fullname" id="fullname"><br><br>

    Email Address:<br>
    <input type="text" name="email" id="email">

    </div>

</form>
```

第 12 章：执行简单动画

![图 12-2 浏览器已成功解析了我们的样式表。](img/f14dd58a324d5464a114c30c1d4c4c9b_290_0.png)

我们的 JavaScript 程序可以通过 DOM 访问名为 fullname 的文本框控件并操作其样式。

```javascript
var TextBoxes = document.getElementsByTagName("input");

for (var counter=0; counter < TextBoxes.length; counter++) {

    var myTextBox = TextBoxes[counter];
    myTextBox.style.backgroundColor = "black";
    myTextBox.style.color = "white";
    myTextBox.style.font = "22pt Arial";

}
```

上述 JavaScript 代码将定位页面上所有的 `<input>` 元素并修改它们的样式属性。最终我们将得到两个具有黑色背景、白色文本和大号 22 点 Arial 字体的文本框。你可以在图 12-3 中看到这段代码的运行结果。

![图 12-3 使用 JavaScript 动态修改了样式。](img/f14dd58a324d5464a114c30c1d4c4c9b_291_0.png)

> JavaScript 属性的名称通常与对应 CSS 属性的名称不同。例如，CSS 属性 `background-color` 是通过 JavaScript 属性 `backgroundColor` 来设置的。

表 12-2 列出了我们一直使用的部分 CSS 属性名及对应的 DOM 样式属性名。

| CSS 属性 | 对应的 DOM 属性 |
| :--- | :--- |
| background | background |
| background-color | backgroundColor |
| border | border |
| border-bottom | borderBottom |
| border-left | borderLeft |
| border-right | borderRight |
| border-top | borderTop |
| color | color |
| font | font |
| font-family | fontFamily |
| font-size | fontSize |
| font-weight | fontWeight |
| margin | margin |
| margin-bottom | marginBottom |
| margin-left | marginLeft |
| margin-right | marginRight |
| margin-top | marginTop |
| text-align | textAlign |

**表 12-2** CSS 与 JavaScript DOM 样式的对应关系

由此可见，CSS 样式属性与对应的 JavaScript DOM 属性在命名上存在一定的一致性，但偶尔两者的名称会有所不同，因此在不确定正确名称时最好进行查阅。

#### 了解跨平台问题

过去，两到三家主要浏览器厂商对 CSS 的支持极不一致。如今，绝大多数在用浏览器都完全支持 CSS 1。大多数浏览器至少部分支持 CSS 2 规范，而 CSS 3 目前仍在开发中。

Internet Explorer 是第一个包含样式表支持的浏览器，微软添加了一些不在标准范围内、且无法在其他浏览器中工作的自有属性。显然，如果你想让样式表在所有浏览器中都能正常工作，应坚持使用官方标准中的属性和命令，避免使用专有扩展。

Netscape 4 包含了一个有缺陷的、不完整的 CSS 标准实现。对于该浏览器，除了几个基本属性外，要让样式表正常工作相当困难，因此请理解，大量依赖样式表的网页在 Netscape 4 浏览器中可能无法呈现预期效果。幸运的是，该浏览器的市场份额已跌至 3% 以下，因此这一问题最终会自行消解。

> W3C 提供了 CSS 验证服务。CSS 验证器位于 http://jigsaw.w3.org/css-validator，它将检查你指定的任何 HTML 网页（或单独的样式表），以确保样式表完全有效。该工具提供了有用的反馈，帮助找出问题所在，因此在开发支持 CSS 的网页时非常实用。



#### 使用 JavaScript 实现基础动画

我们已经讨论了如何使用 JavaScript 更改 DOM 中的元素以及 CSS 样式和定位属性。在本节中，我们将考察使用 JavaScript 在网页上创建动画的两种最常见技术。

##### 动态加载图像

JavaScript 中最简单的动画形式就是通过切换图像来实现。你在网上经常能看到类似的效果，例如当鼠标悬停时，图形菜单或按钮会发生变化。事实上，在第 9 章讨论鼠标事件时，你已经看到了这种效果的示例：

```javascript
<script type="text/javascript" language="javascript">
function changeimage(num) {
    var img = document.getElementById("SampleImage");
    if (num == 1) {
        img.src = "NewImg.gif";
    } else {
        img.src = "OriginalImg.gif";
    }
}
</script>
```

```html
<img src="OriginalImg.gif"
     id="SampleImage"
     alt="Sample image"
     onmouseover="changeimage(1)"
     onmouseout="changeimage(2)" >
```

在 JavaScript 函数 changeimage() 中，我们使用了 document.getElementById() 函数来获取在 HTML 文档正文中定义的图像对象。根据事件类型（onmouseover 或 onmouseout），图像的 src 属性会被指向不同的文件。鼠标悬停事件是最短形式的动画——有点像半秒钟的电影。为了创建更长的效果，我们需要连续快速切换多张图像。例如，让我们构建一个相当简单的动画效果，它使用定时器事件：

+   1. 从一组构成动画的相关图像开始。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_293_0.png)

## 第 12 章：实现简单动画

2. 使用 HTML `<img>` 标签将第一张图像放到网页上。务必为 `<img>` 指定一个 **id** 属性。

```html
<img src="image1.gif" id="anim">
```

3. 然后创建一个名为 animate() 的 JavaScript 函数，以固定间隔（例如每 ¼ 秒）在三张图像之间交替切换。

```javascript
// 计数器变量控制动画
var counter = 0;

function animate() {
    var img = document.getElementById("anim");

    // 切换到下一张图像
    counter ++;
    // 只有四张图像，所以完成后重新从头开始
    if (counter > 3) counter = 0;

    if (counter == 0) {
        // 显示第一张图像
        img.src = "image1.gif";
    } else if (counter == 1) {
        // 显示第二张图像
        img.src = "image2.gif";
    } else if (counter == 2) {
        // 显示第三张图像
        img.src = "image3.gif";
    } else {
        // 显示第四张图像
        img.src = "image4.gif";
    }

    // 我们需要在 0.10 秒后再次调用 animate 函数
    // 在第四张和第一张图像之间暂停 1 秒
    if (counter == 3) {
        setTimeout("animate()", 1000);
    } else {
        setTimeout("animate()", 100);
    }
}
```

4. 我们可以通过从 `<body>` 元素的 onload 事件处理程序中调用该函数来启动动画。

```html
<body onload = "animate()">
```

5. 最终结果是，我们的图形在浏览器窗口中呈现动画效果。

依次快速切换不同的图像创建了一个动画，在浏览器窗口中绘制出一个圆圈。

#### 让内容在屏幕上移动

实现基础动画的另一种方式是将对象在屏幕上移动。我们已经知道 JavaScript 可以访问页面上任何对象的 CSS 定位属性。那么，使用同样的技术来创建 JavaScript 动画应该是相当容易的。

让我们从一张球的图像开始。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_295_0.png)

该图像使用 HTML `<img>` 标签放置在网页上：

```html
<img src="ball.gif"
    id="ball"
    class="ballstyle">
<div class="boxstyle">&nbsp;</div>
```

我们还应该为此页面创建样式表，以便球和盒子从一开始就具有正确的样式和定位。

```css
<style type="text/css">

.ballstyle {
    position: absolute;
    top: 50px;
    left: 100px;
}

.boxstyle {
    position: absolute;
    top: 50px;
    left: 100px;
    height: 250px;
    width: 400px;
    border: solid 1pt black;
}

</style>
```

我们需要一个名为 moveball() 的函数，通过改变图像的 **top** 和 **left** 样式属性来使图像动起来。

```javascript
// 设置起始坐标
var mytop, myleft;
mytop = 50;
myleft = 100;

function moveball() {
    img = document.getElementById("ball");
    mytop += 10;
    myleft += 2;

    if (mytop > 230) mytop = 50;
    if (myleft > 430) myleft = 100;

    img.style.top = mytop;
    img.style.left = myleft;

    setTimeout("moveball()", 100);
}
```

我们必须通过从 `<body>` 元素的 onload 事件处理程序中调用 moveball() 函数来启动球的移动。

如图 12-4 所示，我们创建了一个相当有趣的效果。球的图像持续缓慢地向屏幕右下方移动，直到到达盒子的边缘。一旦到达那里，它会切换回盒子的另一边，然后继续其运动。

文本也可以使用同样的技术进行动画。我们不必移动图像的位置，而是可以用 `<div>` 标签包围一些文本并使其移动。显然，更复杂的动画，例如以随机方式运动的动画对象，或者当到达窗口边缘时改变方向的动画对象，需要更冗长、更复杂的脚本。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_297_0.png)

图 12-4  通过修改 CSS 位置属性，我们能够让一个球移动起来。

在下一章中，我们将讨论调试 JavaScript 代码的基础知识。*Bug* 是指软件缺陷，而 *debugging* 是指查找并修复程序中错误的过程。我们将看看可供那些希望发现这些错误的开发人员使用的一些工具，以及一些使错误更易于发现的编程技巧。

# 第三部分

## 让 JavaScript 更上一层楼

![](img/f14dd58a324d5464a114c30c1d4c4c9b_298_0.png)

栖息湿地面积约3000公顷。得天独厚的自然条件，使海南成为许多珍稀鸟类的聚集地。国家一级、二级保护鸟类屡见不鲜、其中不乏黑脸琵鹭这种世界级濒危鸟类。近年来随着海南鸟类保护工作的不断深入推进，海南成为越来越多候鸟的“度假地”和“繁殖地”。

“海南的气候和生态环境对 thirsty birds 很友善，霸王岭树蛙、粉红树蛙等也较难得一见。”陈庆在教育基地见到粉红池塘和表层带时，简直不敢相信自己的眼睛。在海口五源河国家湿地公园，这条五源河曾因周边人类活动频繁导致河道严重受损，如今已变得美不胜收。

2018年以来，海口涌现越来越多湿地公园，生态环境得到快速提升。美洲红雀是原产于北美的雀形目鸟类，红而热烈，嘹亮鸣唱响彻在美东和中部的灌木林、林地边缘和开阔的乱树丛里。一只美洲红雀的“入侵”却极为吸引中国观鸟爱好者的眼球。

另一方面，也难免混在具体数字中显得枯燥、冷淡。专业的观鸟活动在国内高歌猛进的这些年，除了相当规模的商业观鸟/拍鸟团，个人爱好者的比例也在明显增长，尤其是欧美、澳洲和日本都有成规模的在华外籍鸟类学者、留学生、外派工作人员等。据2015年前后的鸟市行情，一只品相上好的紫色鹦哥售价高达人民币数万元，为禁猎系统所不容，进而助推了非法贸易。

这是一种在城市次生林中繁衍生息的鸟，也就无所谓了。换言之，当一个环境中本应具有警觉性的野生动物不再飞逃，那么，问题的暴露也许只是时间问题了。仅仅是进入鸟友视野这种事竟已“时过境迁”，真是令人感慨。

在首次全国性湿地资源调查时，对于鸟类也被记录在案的、目前已经设立的湿地自然保护区内，日常生活区栖息湿地面积约3000公顷的全球淡水生物保护区面积占全国的1.03%，这还仅仅是4年内才设立的，从就地保护的角度有重要国家意义的、被视为有代表性的或罕见的典型湿地内。

### 第 13 章 调试 JavaScript 程序

![](img/f14dd58a324d5464a114c30c1d4c4c9b_300_0.png)

#### JavaScript 完全指南

#### 如何……

- 理解 JavaScript 错误信息
- 向程序中添加调试代码
- 使用 JavaScript 控制台
- 使用 JavaScript 调试器

对于网页浏览者来说，没有什么比打开一个网页就立即看到错误信息更令人沮丧的了。访问者很可能会对继续深入浏览网站持谨慎态度，也不太可能想要再次访问。

确保网页上的 JavaScript 脚本帮助你的访问者而不是惹恼他们，可能就像使用多种浏览器类型、操作系统和版本号测试你的网页一样简单。是的，这听起来确实很多工作，但如果你想确保你的观众对你所做的网站内容感到满意，实际测试是不可替代的。

但是，如果你正在制作的网页显示了错误信息，你会怎么做？或者你的代码没有按照你预期的方式工作——或者根本不能工作。你将如何查找问题的根源并修复它？有几种工具可以帮助 JavaScript 开发人员完成这项任务，在本章中我们将讨论如何调试 JavaScript 程序。

#### 理解错误的可能原因

在测试网页时找到错误信息就像在大街上捡到一张 5 美元钞票——值得停下来捡起来。错误信息不仅告诉你有问题，它还向你展示了应该首先查看问题的位置，甚至给出了关于哪里出了问题的简要描述。

当然，浏览器只是给出它对错误可能是什么的 *最佳猜测*。当你实际查看代码并找出问题时，你可能会发现错误信息并没有精确地 pinpoint 问题。这是可以理解的，因为有些错误有如此之多的可能原因，以至于计算机不可能选择正确的那一个。

不同的浏览器有不同的错误报告方式，甚至有可能关闭错误报告。例如，在 IE 中，当错误报告开启时，JavaScript 错误将导致出现以下消息框：

![](arding caveats that currently exist around it. We look forward to feedback from people. So there is going to!1
[^0^-4]: This was a great learning experience. The authors have done an excellent job in providing a comprehensive overview of the topic. 

##A useful programming philosophy, - defined by **Test Driven Development** is helpful for finding bugs. We already saw in the previous chapter that testing is an integral part of development. *TDD*, as it is commonly known, takes this one step further and insists that tests should be written *before* code is developed. 

The basic principle of TDD is that you should write a test for a particular feature before writing the actual code. The test will initially fail, because the feature does not yet exist. You then write the minimum amount of code required to make the test pass. 

This process ensures that:
- All code has corresponding tests
- The code is written to satisfy a specific requirement
- You only write enough code to pass the test, preventing over-engineering

#### Common Debugging Tools

Most modern browsers come with built-in developer tools that can help identify and resolve JavaScript errors. The most commonly used is the **console**, which can be accessed in most browsers by pressing `F12` or `Ctrl+Shift+J` (Windows) / `Cmd+Option+J` (Mac). 

The console allows you to:
- View error messages and warnings
- Log custom messages using `console.log()`, `console.warn()`, and `console.error()`
- Execute JavaScript commands in real-time
- Inspect variables and objects

Another essential tool is the **debugger**, which lets you set *breakpoints* in your code. When the code execution reaches a breakpoint, it pauses, allowing you to examine the current state of the program.

Some popular standalone debuggers include:
- [Chrome DevTools](https://developer.chrome.com/docs/devtools/) — built into Google Chrome
- [Firefox Developer Tools](https://firefox-source-docs.mozilla.org/devtools-user/) — built into Mozilla Firefox
- [Safari Web Inspector](https://developer.apple.com/safari/tools/) — built into Safari
- [Visual Studio Code](https://code.visualstudio.com/) — with extensions for JavaScript debugging

#### Summary

In this chapter, we have covered the fundamentals of debugging JavaScript code. Remember that *bugs are inevitable*, but with the right tools and techniques, they can be identified and fixed efficiently. 

Key takeaways:
- Test your code across multiple browsers and platforms
- Use error messages as starting points, not definitive answers
- Leverage browser developer tools like the console and debugger
- Consider adopting **Test Driven Development** to catch errors early

By following these practices, you will be well-equipped to handle any JavaScript errors that come your way.

![](img/f14dd58a324d5464a114c30c1d4c4c9b_301_0.png)



即使关闭了错误报告，IE 仍然会给你一个视觉提示，表明页面未成功加载。浏览器窗口的左下角会出现一个错误图标，如下所示：

![](img/f14dd58a324d5464a114c30c1d4c4c9b_302_0.png)

Netscape 总是向终端用户隐藏 JavaScript 错误——它甚至不会告诉你发生了错误。你需要加载 JavaScript 控制台（将在后面“使用 JavaScript 控制台”部分讨论）才能查看是否发生了任何问题。

JavaScript 中有三种基本类型的错误：

- **语法错误** 指语言基本编程语法中的错误，例如不匹配的引号或括号
- **运行时错误** 指只能在运行时检测到的错误，例如试图使用不存在的变量
- **逻辑错误** 指编程逻辑或算法中的错误，导致不正确的结果，例如循环提前一次迭代退出

这些类型的任何一种错误都可能导致 JavaScript 停止运行或返回不正确的结果。在 JavaScript 1.5 程序中，发生错误的可能原因有数十种，包括：

- 调用未定义的函数或使用未定义的变量
- 试图修改常量的值
- 向需要数字的函数或操作符传递字符串
- 向函数传递不正确数量的参数
- 在字符串中使用未转义的引号
- 错误地使用 **for** 循环等语句

虽然 JavaScript 2.0 试图保留以前版本的灵活性，但其中一些新特性有可能引入新的问题。此外，JavaScript 2.0 给程序员提供了强制执行更严格错误检查级别（称为*严格模式*）的选项。JavaScript 2.0 程序的潜在错误包括：

- 将不正确的数据类型赋给期望另一种数据类型的变量
- 试图访问定义为私有的变量或函数
- 命名空间问题
- 在仅支持 JavaScript 1.5 的浏览器中运行 JavaScript 2.0

我一直觉得，查找和修复错误就像解开一个谜团。你只有几条线索，通过出色的侦探工作，也许再加上一点运气，最终就能弄清楚到底哪里出了问题。

#### 在 IE 中打开错误报告

Internet Explorer 有两个高级选项，会影响 JavaScript 错误的报告和处理方式。可以通过从“工具”菜单中选择“Internet 选项”，然后选择“高级”选项卡来找到“高级选项”菜单。

在此选项卡上，我们关注的第一个选项设置是“显示每个脚本错误的通知”。应启用此选项，以便看到我们在本章中讨论的 JavaScript 错误消息。

另一个可能影响我们的选项是“禁用脚本调试”。根据计算机上安装的软件，IE 可能会给你一个将网页加载到名为调试器的工具中以了解更多信息的选项。

通常，应启用此选项；也就是说，你不想被提供在调试器中查看代码的选项。（但是，如果你真的想针对每个错误进入调试器，并且你有一些使用该软件的经验，那么请务必禁用调试选项。）

#### 找到错误消息的来源

当 JavaScript 在脚本中遇到错误且程序未处理该错误时，用户会通过一个错误消息框被通知该错误。在 IE 中，错误的详细信息通常被隐藏，因为它们对新手用户来说可能过于技术化。相反，会显示如下所示的一条较为友好的消息。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_303_0.png)

通过单击“显示详细信息”按钮，我们可以看到关于该特定错误的一些技术细节。

Internet Explorer

此网页的问题可能会阻止其正确显示或正常运行。将来，你可以通过双击状态栏中显示的警告图标来显示此消息。

当页面包含错误时始终显示此消息。

确定

隐藏详细信息 <<

行：10
字符：1
错误：应为 '}'
代码：0
URL：file:///C:/TEMP/JSTest.htm

IE 给程序员提供了许多关于错误来源的重要细节：

- **行** JavaScript 首次注意到问题的行号。这并不总是包含问题的行，尽管通常是。使用显示行号的文本编辑器可以节省你手动计数的麻烦。XP 上的 Windows 记事本可以通过打开状态栏（查看 | 状态栏）来查看行号。
- **字符** 问题可能所在的行的字符编号。
- **错误** 一个尝试描述 JavaScript 认为出了什么问题的字符串。
- **代码** 一些错误附有错误代码。
- **URL** 有问题的 HTML 文件的网址，以防有任何疑问。

> 错误消息中列出的行号包括脚本之前的任何 HTML 行，除非脚本存在于单独的文件中（外部脚本），在这种情况下，它是脚本文件的实际行号。

错误消息详细信息中引用的行号通常是开始查找错误的最佳位置。你还需要阅读消息框提供的错误描述，因为这为你提供了破解这个谜团所需的第二条线索。

#### 解释错误消息

也许理解 JavaScript 错误消息与实际错误来源之间（不）紧密相关的最佳方式是看一个例子。在本节中，我们将研究一段有严重错误的 JavaScript 代码，并看看两大浏览器（Netscape 和 IE）如何报告错误。

#### 如何用 JavaScript 做一切

作为练习的开始，让我们看看以下 HTML 和 JavaScript 代码。

```
<html>
    <head><title>Interpreting error messages</title></head>
    <body>
    <script language="JavaScript" type="text/javascript">
    function add (input1, input2) {
        return input1 + input2;
    }

    var result = ad (1, 2);
    </script>
    </body>
</html>
```

当我们第一次运行此代码时，我们期望在调用 add() 函数并传入值 1 和 2 后，返回的结果将是 3。相反，我们遇到了一个 JavaScript 错误。IE 给出了相当神秘的消息“需要对象”。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_305_0.png)

但它确实给了我们一个行号。请记住，行号包括网页上脚本之前的所有 HTML 代码。第九行代码指向以下行的一个问题：

```
var result = ad (1, 2);
```

Netscape JavaScript 控制台在描述错误方面做得更好——尽管，如本章前面所讨论的，你必须打开控制台窗口才能知道存在错误。控制台更有用地报告说“ad 未定义”。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_306_0.png)

仔细观察，我们可以看到我们把函数名拼错了；它应该是 add()，而不是 ad()。纠正这个拼写错误后，两个浏览器中的错误都消失了。

#### 使用 JavaScript 验证器

检查 JavaScript 代码中奇怪错误的一种方法是将其运行通过一个检查它的程序，以确保它是_有效的_——即遵循该语言的官方语法规则。这些程序被称为_验证解析器_，或者简称为_验证器_，通常随商业 HTML 和 JavaScript 编辑器一起提供。

一些验证解析器的一个限制是它们只能理解作为官方 ECMAScript 规范一部分的 JavaScript 语言组件。其中一些工具不理解 DOM 函数调用或浏览器制造商添加的、不属于 ECMAScript 规范的一些语言扩展。

也许最方便的 JavaScript 验证器是 Douglas Crockford 的 JavaScript Lint，可在 http://www.crockford.com/javascript/jslint.html 免费在线获取。只需访问该网页，将你的 JavaScript 代码粘贴到提供的文本区域，然后单击 jslint 按钮。瞧！结果会在几秒钟内显示在屏幕上。

JavaScript Lint 将解析你的 JavaScript 代码，确保任何变量和函数定义都遵循正确的语法。它还会检查 JavaScript 语句，例如 **if** 和 **while**，以确保它们也遵循正确的格式。这个程序不会捕获你 JavaScript 程序中的所有错误，但它会捕获明显的错误，例如缺少括号或未定义的变量和函数。

#### 向程序添加调试代码

通常，当 JavaScript 脚本没有产生预期的结果时，问题的存在原因并不明显。例如，你可能期望在进行一系列数学运算后，一个变量会返回一个特定的值——但它没有。JavaScript



# 288 如何用JavaScript做一切

错误信息能帮助你找出导致问题的代码行，但即便是JavaScript验证器有时也未必能派上用场。

程序员可以为自己做的一件事是，在程序中添加一些*调试代码*。调试代码纯粹是为了帮助开发者在代码修改过程中弄清幕后发生了什么。一旦页面的常规用户开始使用该脚本，你通常应该移除或注释掉这些调试代码。

程序员在向程序添加调试代码时，通常会使用`alert()`或`document.write()`方法。例如，下面的脚本包含多个额外的`alert()`消息框，它们能让开发者了解程序内部的运行情况。

```
// 将数字 "9999999" 转换为 "9,999,999"
function convert_number(input) {
    var counter, output;

    alert("input = " + input);
    alert("input length = " + input.length);

    // 长度不够，无法添加逗号
    if (input.length < 4) return input;
    alert("length larger than 3");

    // 初始化输出为空字符串
    output = "";

    // 遍历输入字符串，每次处理三个字符
    for (counter = input.length-3; counter > 0; counter -= 3) {
        output = "," + input.substr(counter, counter+2) + output;
        alert("counter = " + counter + ", output = " + output);
    }

    // 处理最后一组数字
    output = input.substr(0, counter+3) + output;
    alert("counter = " + counter + ", output = " + output);

    return output;
}
```

在上面的代码中，所有对`alert()`消息框的调用都仅用于调试目的。它们唯一的目的是为程序员提供一些关于函数内部运行情况的线索：原始值是什么，每次循环迭代后发生了什么，以及最终结果是什么。

同样，一旦我们确信这个函数运行正常，就应该移除或注释掉那些提示框，以免让访问者进行大量不必要的鼠标点击。

一种类似的调试技巧涉及谨慎且逐步地使用注释。

假设你有一个JavaScript函数，它似乎运行不正确。你已经检查了源代码，但仍然无法找出问题的根源。

```
// 将数字 "9999999" 转换为 "9,999,999"
function convert_number(input) {
    var counter, output;

    if (input.length < 4) return input;
    output = "";

    for (counter = input.length-3; counter > 0; counter -= 3) {
        output = "," + input.substr(counter, counter+3) + output;
    }
    output = input.substr(0, counter+3) + output;
    return output;
}
```

- 1. 首先，注释掉整个函数体的内容。如果函数应该返回一个值，就让它返回一个硬编码的值，模拟你期望的结果。测试脚本，确保它现在能用这个硬编码的值正确工作。

```
// 将数字 "9999999" 转换为 "9,999,999"
function convert_number(input) {
//     var counter, output;
//
//     if (input.length < 4) return input;
//     output = "";
//
//     for (counter = input.length-3; counter > 0; counter -= 3) {
//         output = "," + input.substr(counter, counter+3) + output;
//     }
```

290 如何用JavaScript做一切

```
//     output = input.substr(0, counter+3) + output;
//     return output;

// ** 硬编码的返回值 **
return "1,234,567";
}
```

- 2. 接下来，取消注释其中几行。例如，让函数返回其输入字符串，而不是那个硬编码的值。再次测试，确保这个预期结果（输入字符串）能正确工作。

```
// 将数字 "9999999" 转换为 "9,999,999"
function convert_number(input) {
    var counter, output;

    if (input.length < 4) return input;
    output = "";

//     for (counter = input.length-3; counter > 0; counter -= 3) {
//         output = "," + input.substr(counter, counter+3) + output;
//     }
//     output = input.substr(0, counter+3) + output;
//     return output;

    // ** 返回输入值 **
    return input;
}
```

- 3. 从脚本中仔细地取消注释更多行。预先知道每取消一组注释后期望的返回值是什么，然后重新测试。

- 4. 根据需要重复步骤3。在某个点上，你会发现返回值不是你预期的那个。最近取消注释的几行最有可能是问题的根源！

添加调试代码和使用注释是手动找出脚本中错误根源的两种最有用的技巧。

#### 使用JavaScript控制台

网景（Netscape）和Mozilla浏览器包含一个实用工具，称为JavaScript控制台。JavaScript控制台在自己的窗口中打开，这是网景浏览器输出其遇到的任何JavaScript错误的地方。控制台将持续累积来自网页的错误信息，直到浏览器关闭或手动清除控制台。

**图13-1** 网景控制台显示JavaScript错误。

要在网景7中访问控制台，请转到“工具”|“Web开发”，然后选择“JavaScript控制台”。（在网景6中，“JavaScript控制台”选项位于“任务”|“工具”下。）浏览器初次打开时控制台是空的，但随着你浏览许多不同的页面和网站，它会累积出现的错误信息。

控制台还允许开发者输入JavaScript代码供浏览器执行。只需在控制台中输入变量名，点击“评估”，控制台就会告诉你该变量的当前值。或者，你可以通过输入函数名及任何参数，让JavaScript手动调用一个函数。

图13-1展示了该控制台在网景7网络浏览器中的样子。

#### 使用JavaScript调试器

程序员对抗bug的最终武器是使用调试软件。调试器是一个程序，它让你能完全访问应用程序的内部工作机制。JavaScript调试器通常包含一个用户友好的界面，并允许开发者逐行单步执行脚本。开发者可以查看任何变量的当前值，并获得更详细的反馈，以帮助他们找到bug的真正根源。

调试器通常随HTML和JavaScript编辑器一起提供。例如，Microsoft FrontPage 2002包含一个名为Microsoft Script Editor的JavaScript编辑器和调试器。Macromedia Dreamweaver在其Dreamweaver MX产品中也包含了一个JavaScript调试器。还有一些第三方编辑器也包含调试器，比如C Point的JavaScript Editor (http://www.c-point.com)。

# 如何用JavaScript做一切

对于不使用专业HTML编辑器的人，也有许多免费的JavaScript调试器可用。其中最著名的是来自开源Mozilla项目的JavaScript Debugger。

你可能知道，网景和Mozilla网络浏览器基于相同的核心源代码。然而，网景版本不包含JavaScript调试器，而Mozilla包含。因此，使用网景7（及更高版本）浏览器的开发者需要单独下载并安装调试器作为一个工具。

> 最新的网景网络浏览器可从 http://www.netscape.com 下载。最新的Mozilla JavaScript调试器（代号Venkman），适用于Mozilla和网景浏览器，可从 http://www.hacksrus.com/~ginda/venkman 下载。

Mozilla JavaScript调试器支持多种操作系统（特别是Windows、Mac OS和Unix），在帮助开发者单步执行他们的JavaScript程序方面表现出色。我们可以在图13-2中看到这个调试器的截图。

**图13-2**

使用Mozilla调试器单步执行JavaScript程序



#### 让你的程序防患于未然

#### 如何……

- 理解异常及其产生原因
- 使用 **try** 和 **catch** 语句捕获异常
- 使用 **throw** 语句创建异常
- 从一开始就设计易于调试的程序

在使用 Visual Basic 和 Java 等编程语言时，设计并开发能够免疫错误的程序是一项艰巨的任务。但在使用 JavaScript 时，这在某些方面甚至更加困难。

原因之一是，作为一种脚本语言，JavaScript 通常以源代码形式分发。在正常情况下，没有编译器能在用户看到最终程序运行之前捕获语法错误。对于其他语言来说，编译步骤提供了针对某些类型错误的保护屏障。

另一个困难的原因是，JavaScript 通常只使用基础文本编辑器进行开发。而像 Visual Basic 这样的语言则是使用集成开发环境（IDE）创建的，这些环境帮助开发人员编写更好的代码，并包含内置的调试器。

还有一个原因是目标环境（浏览器和操作系统）的数量如此多样化——实际上有数十种组合——以至于几乎不可能在所有可能的环境中测试程序。

但开发人员可以使用一些技术来确保他们创建的 JavaScript 程序能在尽可能多的环境中正常工作。在本章中，我们将探讨一些最实用的方法来确保编程成功。

#### 学习异常的基础知识

在 Web 编程的早期，当 JavaScript 在执行程序时遇到错误，结果总是致命的：浏览器会停止执行代码并向用户报告错误。实际上，错误总是直接报告给浏览器——应用程序根本没有机会尝试自行处理错误。你可以想象，当你甚至无法检测到错误发生时，创建一个是无错误的程序是多么不可能。

此外，JavaScript 开发人员不得不自己发明将错误返回给程序的方法。请看下面的例子：

```
function simple_addition(a, b) {
    // This function will add two numbers,
    //     but only if they both are between 0 and 9
    if (a < 0 || a > 9) {
        return "First number is not between 0 and 9.";
    }
    else if (b < 0 || b > 9) {
        return "Second number is not between 0 and 9.";
    } else {
        return a + b;
    }
}
```

程序中调用此函数的每个地方都必须有额外的几行代码（更多的 **if** 语句）来检查返回值，以查看是否发生错误，然后才能使用该数字。其他程序员可能会用不同的方式解决同样的问题，使用特殊的返回代码（如使用值 -1）来返回错误。

JavaScript 使用*异常*将系统错误传递给程序进行处理。此外，JavaScript 程序员可以在其代码中使用相同的异常系统，从函数返回特定于应用程序的错误。例如，我们可以重写前面示例中的源代码，使用 **throw** 语句来改用异常。

```
function simple_addition(a, b) {
    // This function will add two numbers, but only if they are less than 10
    if (a < 0 || a > 9) {
        throw "First number is not between 0 and 9.";
    } else if (b < 0 || b > 9) {
        throw "Second number is not between 0 and 9.";
    } else {
        return a + b;
    }
}
```

在接下来的两个部分中，你将学习更多关于创建和捕获异常的语句。

#### 使用 try 和 catch 语句捕获异常

**try-catch** 语句是在 JavaScript 1.4 中引入的；它以 Java 和 C++ 中的类似语句为模型。当 JavaScript 在代码中遇到 **try-catch** 语句时，它将开始执行 **try** 子句中包含的代码块。如果该块中的任何语句导致异常发生，JavaScript 将不会执行该块中的任何剩余语句，并立即跳转到 **catch** 子句中包含的代码。当然，如果 **try** 子句中没有发生异常，**catch** 子句中的代码将永远不会被执行。

以下代码显示了如何使用 **try-catch** 语句来保护代码免受异常影响。

```
var isIE = (navigator.userAgent.indexOf("MSIE")) > -1;

try {
    var a = 1;
    var c = a / b;
    alert("The result of a / b is " + c);
}
catch (e) {
    var msg = "JavaScript encountered the following error:\n\n";
    // IE and Netscape pass errors differently to the catch clause
    if (isIE) {
        msg += e.description;
    } else {
        msg += e;
    }
    alert(msg);
}
```

> **注意：** IE 和 Netscape 各自有其将错误传递给 **catch** 子句的方式。IE 将错误作为 Error 对象传递——要获取实际的错误消息，你必须访问该对象的某个属性。Netscape 将错误作为字符串传递，可以像任何其他字符串一样使用。

前面的代码尝试在 **try** 块中使用未定义的变量 b。一旦我们的代码尝试在表达式中使用该变量，就会发生异常，并且块中的其余代码不会执行。**catch** 子句为 IE 生成的错误消息如下所示。

Netscape 在执行 **try** 块内的代码时遇到相同的错误。不过，其错误消息的措辞略有不同。

#### 理解异常的冒泡

**try-catch** 语句还可以捕获 **try** 子句中函数调用内部生成的错误。例如，假设我们将前面示例中的一些代码移到它自己的函数中。

```
var isIE = (navigator.userAgent.indexOf("MSIE")) > -1;

function calculate() {
    var a = 1;
    return a / b;
}

try {
    var c = calculate();
    alert("The result of a / b is " + c);
}
catch (e) {
    var msg = "JavaScript encountered the following error:\n\n";
    // IE and Netscape pass errors differently to the catch clause
    if (isIE) {
        msg += e.description;
    } else {
        msg += e;
    }
    alert (msg);
}
```

**try-catch** 语句仍然会收到错误通知，即使它发生在 calculate() 函数内部。这是因为异常与事件类似，会冒泡。*异常冒泡*是用来描述异常如何寻找第一个有资格处理它的 **try-catch** 语句的过程的术语。如果没有 **try-catch** 语句立即包围有错误的代码行，控制权将跳转回调用包含错误的函数的代码。如果那里也没有 **try-catch**，控制权将跳转回调用它的代码，依此类推，直到找到 **try-catch** 或浏览器通过向用户显示异常来处理异常。

---

要在 Mozilla 1 或 Netscape 7 中访问 JavaScript 调试器，请转到 Tools | Web Development 菜单，然后选择 JavaScript Debugger。

Microsoft 还提供了一个免费的调试器，即 Microsoft Script Debugger。它可以在 http://www.microsoft.com/script/debugger 下载。Script Debugger 支持许多关键的调试器功能，例如查看和单步执行代码、设置断点以及查看和更改变量值的能力。

无论你使用哪种浏览器，你一定会发现能够单步执行复杂的 JavaScript 程序非常有用。对于小型脚本，添加调试代码可能就是你查找问题所需的全部。但当你的程序包含大量函数并且需要一些高级调试功能（如断点）时，一个好的 JavaScript 调试器可以成为程序员最好的朋友。

下一章将涉及一些重要的概念，关于如何使用 **try-catch** 语句在浏览器之前拦截系统错误。你还将看到如何在自己的程序中使用异常。

#### 什么是断点

在调试中，*断点*是由程序员指定的代码行，调试器将在该点暂停（或*中断*）程序。程序员可以在调试器中执行多项任务，然后再让程序继续执行。

拥有支持断点的调试器的好处是，你不必手动单步执行脚本中的每一行代码，而是可以让调试器自动执行所有行，直到到达第一个断点。一旦你检查了一些数据变量的内容，你可以手动单步执行程序，或者让它自动运行直到到达下一个断点。



# 第14章：让您的程序杜绝错误

#### 如何使用 JavaScript 做任何事

例如，以下代码在进行了数层函数调用后会产生一个错误。该异常仍然能够成功回传到第一个函数调用外围的 **try-catch** 语句。

```
var isIE = (navigator.userAgent.indexOf("MSIE")) > -1;

function fn1 () {
    // 第一个函数 (fn1) 调用第二个 (fn2)，
    fn2();
}

function fn2 () {
    // 第二个函数 (fn2) 调用第三个 (fn3)
    fn3();
}

function fn3 () {
    // 第三个函数 (fn3) 调用第四个 (fn4)
    fn4();
}

function fn4 () {
    // 第四个函数 (fn4) 调用第五个 (fn5)
    fn5();
}

function fn5 () {
    // 第五个函数 (fn5) 包含一个错误
    return some_undefined_variable;
}

// 主程序
try {
    fn1();
} catch (e) {
    var msg = "JavaScript 遇到了以下错误：\n\n";
    // IE 和 Netscape 将错误传递给 catch 子句的方式不同
    if (isIE) {
        msg += e.description;
    } else {
        msg += e;
    }
    alert (msg);
}
```

正如您从以下截图中看到的，Netscape 和 IE 都能将异常正确传递到我们的 **catch** 子句。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_320_0.png)

> 您并不总是必须通过向用户显示消息来响应异常。您也可以选择忽略错误并继续执行。

#### 使用 IE 错误对象

正如我们在上一节所观察到的，Internet Explorer 会将一个 Error 对象传递给 **catch** 子句的参数。Error 对象包含两个属性：

- **number** 与错误相关的数字值
- **description** 描述错误的字符串

> 本节中的代码仅在 Internet Explorer 中有效：

IE 会在发生异常时自动创建一个 Error 对象，但您也可以使用以下 **new** 语句语法自由创建自己的错误：

```
var myerr = new Error (1000,
  "Value falls outside acceptable range of 0-81.");
```

使用此对象使您的程序能够轻松区分不同类型的错误，同时保留可供显示给用户的简明描述。

```
// 错误 1000：忽略，将返回码设置为 0
if (e.number == 1000) {
  var returncode = 0;
}
// 错误 1001：退出循环，将返回码设置为 9999
else if (e.number == 1001) {
  var returncode = 9999;
}
// 其他错误代码：无法处理，报告给用户
else {
  alert(e.description);
}
```

这种方法唯一真正的问题是 Netscape 使用了不同的方法，这意味着您必须包含浏览器嗅探代码才能创建跨平台兼容的代码。

#### 使用仅限 Netscape 的 catch 子句

Netscape 有一种特殊的 **catch** 子句语法，允许在 **try-catch** 语句中存在多个 catch 子句。Netscape 称之为 *条件 catch 块*。

> 注意 IE 不支持此语法，并且它也不属于官方 ECMA 标准的一部分。

基本上，Netscape 允许开发人员插入一个 **if** 关键字，以确定在抛出异常后调用哪个 **catch** 块：

```
try {
    var input = get_user_input();
    edit_check (input);
}
catch (e if e == "Value too high") {
    // 当用户输入的值过高时我们该怎么办？
    // ...
}
catch (e if e == "Value too low") {
    // 当用户输入的值过低时我们该怎么办？
    // ...
}
catch (e if e == "No value entered") {
    // 当用户未输入值时我们该怎么办？
    // ...
}
catch (e) {
    // 发生了其他错误
    // ...
}
```

我建议尽可能避免使用这种专有方法。因为在单个 **catch** 子句中添加一个 **if-else** 语句可以产生相同的效果，所以没有好处采用这种方式编码。

#### 使用非标准的 finally 子句

Java 和 C++ 程序员会认识到 **try-catch** 语句中可选的 **finally** 子句，但熟悉官方 ECMAScript 规范的人则不会。Netscape 和 IE 网页浏览器都支持此子句，即使它不存在于官方标准中，因此并非所有 JavaScript 环境都支持它。

基本上，**finally** 子句包含的代码将始终被执行，无论 **try** 块中是否发生异常。即使在 **try** 或 **catch** 子句内有 **return** 语句（这会触发函数退出），**finally** 子句也保证会运行。

> **finally** 子句不会被执行的唯一情况是，在 **catch** 子句内部发生未处理的异常。*未处理的异常是指必须由浏览器处理的异常，因为没有剩余的 try-catch 语句来处理它。*

例如，以下代码在 **try** 子句内部触发一个异常，**catch** 子句内的代码和 **finally** 子句内的代码都会在控制权返回到函数外部之前被执行。

```
function function_that_will_fail() {
    var a = 1;
    var b = 2;
    this_function_does_not_exist(a, b);
}

function capture_error() {
    try {
        document.write("<b>try</b>: ");
        document.write("Calling the function.<br><br>");
        function_that_will_fail();
    }
    catch (err) {
        document.write("<b>catch</b>: ");
        document.write("An error has occurred.<br><br>");
        return;
    }
    finally {
        document.write("<b>finally</b>: ");
        document.write("This code is guaranteed to execute.<br>");
    }
}

capture_error();
```

正如您从图 14-1 中看到的，尽管 **catch** 子句内有一个 **return** 语句，但 **finally** 子句确实执行了。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_323_0.png)

图 14-1 **finally** 子句拥有最终决定权：无论是否有异常。

#### 使用 throw 语句创建异常

让 **try-catch** 语句更有用的一点是 **throw** 语句。**throw** 语句允许开发人员创建自己的异常。这意味着您可以有一组单独的 **try-catch** 语句来捕获所有系统和应用程序错误，这无疑节省了大量编码工作。

它还允许您利用异常冒泡机制，将错误消息从函数深处传递到等待在几个函数调用之后的 **try-catch** 语句。如果没有这种异常冒泡，我们将不得不编写大量额外的代码来捕获每个函数内的错误，然后记住将其认真传递回上一级。

例如，以下代码会导致一个异常发生。根据定义，函数内的处理立即停止，异常被传递给上一级的等待 **try-catch** 语句。

```
function throw_an_error() {
    throw "Ouch! I stubbed my toe!";
}

try {
    throw_an_error();
    document.write("This line will never be executed.");
} catch (myerr1) {
    document.write("The following error occurred: <br>");
    document.write(myerr1);
}
```

注意我能够将 myerr1 变量用作字符串，而无需包含浏览器嗅探代码来确定我们是否需要使用 IE Error 对象。原因是，由于我们使用 **throw** 语句传递了一个字符串字面量，**catch** 子句只接收到该字符串。如果您选择抛出字符串，IE 不会自动为您创建 Error 对象。但是，您可以创建自己的 Error 对象并抛出它。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_324_0.png)

#### 如何重新抛出异常

当 **try-catch** 语句遇到它不想处理的异常时，它可以使用 **throw** 语句将异常发送回程序中其他地方定义的另一个 **try-catch** 语句。这称为 *重新抛出* 异常。例如，以下代码重新抛出了一个它未准备好处理的错误：

```
function calculate_total() {
    try {
        var subtotal = get_item_amount();
    } catch (e) {
        if (e = "No items remaining") {
            return 0;
        } else {
            // 一定是个系统错误，
            // 让 JavaScript 处理它
            throw e;
        }
    }
}
```



function throw_an_error() {
    var eobj = new Error(0, "Ouch! I stubbed my toe!");
    throw eobj;
}

然而，这段代码仅在Internet Explorer中有效，因为Netscape中没有Error对象。因此，采用这种方法我们还需要引入浏览器嗅探代码。

最佳方法是抛出一个字符串，正如你所预期的。在**catch**子句中，测试传递的参数是字符串还是对象。

```
catch (myerr1) {
    if (myerr1 instanceof Error) {
        var errstring = myerr1.description;
    } else {
        var errstring = myerr1;
    }
    document.write("The following error occurred: <br>");
    document.write(errstring);
}
```

前面的**catch**子句在IE和Netscape中都有效，并且能正确检测传递的参数是Error对象还是仅仅是字符串。

#### 从一开始就设计易于调试的程序

某些编程风格能减少bug（和调试麻烦），而另一些则会产生相反的效果。当你的JavaScript程序看起来会变得冗长复杂时，如果从一开始就采用正确的设计方法，你可能会为以后节省一些时间和精力。

我们在第3章详细讨论了四种编程风格：

- **非结构化** 一系列作用于全局数据的语句
- **过程化** 调用函数执行特定任务的主程序
- **模块化** 使用模块分组相关功能的主程序
- **面向对象** 使用对象分组相关数据和功能的主程序

在编写无误程序方面，这些方法各有优缺点。非结构化技术适用于小型脚本，但对于大型脚本则非常糟糕。面向对象则相反——适用于大型程序，但不适用于短小脚本。事先大致了解程序的复杂性将有助于你选择最佳方法。

# 第14章：让你的程序无懈可击 307

#### 避免非结构化编程

非结构化方法通常最适合短小、简单的脚本。本质上，这种程序由一组JavaScript语句组成，这些语句不定义或使用任何函数、模块或对象。

从某些方面来说，非结构化技术是所有方法中最简单的，但当你的程序代码超过一两页时，你就应该考虑将其分解为更易于管理的部分。

你将遇到的此类大型程序的最大问题是代码的复杂性和相互依赖的数量。程序后面的语句将依赖于几百行前设置的变量。修改程序的一部分可能会破坏另一区域的代码。

以这种方式构建程序类似于用一整块木头建造房子。进行一个小的调整，比如移动一扇窗户，如果不完全重新开始，几乎是不可能的。只有在你的房子非常小的情况下，这才是可以接受的。

#### 将代码分解为可管理的块

房子不是用一整块材料建造的，而是一面墙、屋顶、地板和楼梯分步建造的，这是有原因的。这样，移动一扇窗户不会影响其他墙壁或其他结构元素，这种调整所能造成的最坏情况只是让你不得不重建一堵墙。房子是由独立的组件构成的，计算机程序通常也应该是这样。

“组件化”程序最简单的方法是将其组织成几个函数。如果可能的话，最好让这些函数分别负责不同的领域，这样两个或多个函数就不会相互冲突或执行相同的任务。例如，以下代码片段展示了如何使用函数来改善程序的组织性和可读性：

```
function groceries () {
    var grocerylist = get_grocery_list();
    drive_to_store();
    for (var item in grocerylist) {
        get_item(item);
    }
    pay_cashier();
    drive_home();
    put_food_away();
    return;
}
```

我们也可以使用非结构化程序，试图按顺序完成所有这些任务。但那个程序会更难阅读、测试和修改。

#### 如何用JavaScript做所有事情

要测试一个函数，我们只需要确保它执行任务并返回预期的值。大多数函数依赖于程序其余部分的结构，因此你永远无法100%确定不会出错。因为函数更容易测试，你会发现过程化编程比非结构化编程提供了更高的可靠性。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_327_0.png)

#### 使用类和对象重用代码

组件化代码的另一种方法是将其分解为多个类和对象。类允许你将所有相关的函数和变量分离到一个单独的模块中。这使你可以创建可以在其他应用程序中轻松重用的类。

例如，你可以创建一个代表用户在线购物车中一个商品的类。由于此商品代码是通用的，完全相同的代码可以在其他需要访问商品的应用程序中重用，例如库存管理程序。

```
class Item {
    var SKU : String;
    var productName : String;
    var size : String;
    var color : String;
    var retailPrice : Number;
    var wholesalePrice : Number;

    function Item(inSKU : String, inName : String,
                  inSize : String, inColor : String,
                  inPrice1 : Number, inPrice2 : Number) {
        this.SKU = inSKU;
        this.productName = inName;
        this.size = inSize;
        this.color = inColor;
        this.retailPrice = inPrice1;
        this.wholesalePrice = inPrice2;
    }

    // 更多方法将在此之后...
}
```

类和对象也更容易测试。你只需要检查一次，以确保对象按预期的方式运行。只要类中的代码没有更改，就可以认为对象已经过完全测试。

#### 彻底测试你的JavaScript代码

确保程序免受错误影响的最后一个关键是对程序进行彻底测试。测试包括在许多不同的场景下多次运行程序，以确保其按预期运行。

对于短小的脚本，测试不必过于复杂。例如，测试鼠标悬停效果可能只需要在图像上移动几次鼠标，以确保其按预期切换。对于更复杂的脚本，例如涉及DHTML或框架间通信的脚本，可能需要更严格的测试。

#### 创建测试工具

*测试工具*是一个其职责是帮助测试其他程序的程序。在JavaScript编程中，测试工具通常采用自定义网页的形式，该网页暴露了用于测试幕后脚本的按钮和表单字段。

图14-2展示了一个良好测试工具的示例。该网页允许开发人员或测试人员手动触发某些事件，或向嵌入在页面中的函数强制提供某些值。

![](img/f14dd58a324d5464a114c30c1d4c4c9b_328_0.png)

**图14-2** 使用测试工具帮助测试JavaScript程序。

#### 如何用JavaScript做所有事情

要查看测试工具的实际运行效果，让我们从一个我们希望测试的小型JavaScript脚本开始。

```
// 此脚本将验证电子邮件地址
function validate_email (inputstr) {
    // 以下复杂的正则表达式模式用于检查
    // 有效的电子邮件地址：user.name@domain-name.com
    var pattern =
        /^[a-zA-Z0-9_\-.]+@([a-zA-Z0-9\-]+\.)+[a-zA-Z]{2,3}$/;

    if (inputstr.search(pattern) > -1) {
        return true;
    } else {
        return false;
    }
}
```

现在我们本可以直接选择在程序中使用它，但在使用之前验证其是否完全正常工作是个好主意。通过创建以下包含我们脚本的HTML测试工具，我们可以以简单直接的方式测试数十个不同的电子邮件地址。

```
<html>
    <head>
        <title>HTML Testing Harness</title>
        <script language="JavaScript" type="text/javascript">

            // 此脚本将验证电子邮件地址
            function validate_email (inputstr) {
                // 以下复杂的正则表达式模式用于检查
                // 有效的电子邮件地址：user.name@domain-name.com
                var pattern =
                    /^[a-zA-Z0-9_\-.]+@([a-zA-Z0-9\-]+\.)+[a-zA-Z]{2,3}$/;

                if (inputstr.search(pattern) > -1) {
                    return true;
                } else {
                    return false;
                }
            }
        </script>
    </head>
    <body>
        <center>
            <h1>HTML Testing Harness</h1>
```



```html
<h2>适用于电子邮件检查器</h2>
</center>

<form action="#" method="get">
    电子邮件地址：<br>
    <input type="text" name="email">
    <input type="button" value="测试"
        onclick="alert(validate_email(document.forms[0].email.value))">
</form>
</body>
</html>
```

以上 HTML 代码仅用于测试 JavaScript 函数 `validate_email()`。它包含一个简单的 HTML 表单，由一个文本框和一个按钮组成。通过该表单，测试人员和开发者可以输入数十个不同的测试电子邮件地址，以验证我们的脚本是否按预期工作。

如果对程序中的每个复杂函数都重复这一过程，将降低用户在使用你的网页时发现异常行为的可能性。

#### 强制产生错误以测试错误处理代码

开发者在测试自己的程序时，有一种情况时常发生，我称之为"晴天综合征"。当函数的参数字段需要日期时，我们往往只使用有效日期；当函数期望数值时，我们往往只使用数字。

但是，向这样的字段发送无效日期（如"02/29/2005"或"12/33/2005"）——甚至尝试发送非日期内容（如字符串"Boo"）——看看会发生什么，这一点非常重要。你的函数对无效输入如何响应？你的错误处理代码表现如何？

你甚至可能需要修改代码来强制产生此类错误。例如，在以下代码中，我将一个数组硬编码为空数组，以查看代码如何处理空数组。这仅仅是为了测试调用此函数的代码的错误处理能力。

```
function print_listing() {

    var itemarray = get_product_list();

    // BEGIN TESTING:: Empty array added just for testing
    //      Forcing an error
    itemarray = new Array();
    // END TESTING

    for (var item in itemarray) {
        // Rest of code ...
    }
}
```

我们修改代码只是为了看看当某些问题发生时会怎样。这是一种非常简单的方式来测试现实中很少发生的情况。

#### 在多种不同环境中测试你的程序

在你使用 **try-catch** 语句来捕获和处理错误，并以模块化、易于测试的方式设计好程序之后，只剩下一件事要做：系统测试。*系统测试*是在程序可能运行的所有不同软件环境中进行测试的过程。

嵌入网页中的 JavaScript 程序仍然需要在多种不同的浏览器和操作系统中进行检查，才能被认为是无错误的。你可能没有那么多操作系统可供使用，但下载并安装两个或更多的浏览器并不困难，这样你至少可以在这些环境中测试你的程序。

在同一台机器上运行多个版本的 IE 相当困难，但并非不可能。而获取多个版本的 Netscape 则一直容易得多——你只需将它们安装在不同的目录中即可。

> 提示：网站 http://browsers.evolt.org 包含了几乎所有曾发布过的浏览器副本。这是一个相当令人印象深刻的网站。如果你想看看今天的互联网在 Netscape 0.9 中是什么样子，可以下载并安装它来一探究竟。

你可能不必测试每个曾发布过的浏览器，但至少应该使用 IE 5、Netscape 4 和 7 以及 Mozilla 1 来检查你的脚本。

下一章是本书的最后一章。它探讨了如何使用 JavaScript 与页面上的多媒体对象进行交互。JavaScript 最初是为与 Java 交互而开发的，但它也可以处理嵌入网页中的视频和音乐。

### 第 15 章 使用 JavaScript 管理浏览器插件

#### 使用 JavaScript 实现一切

#### 如何...

- 将可脚本化的对象插入 HTML 网页
- 包含 Sun Java applet
- 将视频和音乐嵌入网页
- 在网页中使用 Microsoft 日历控件

自 1995 年 12 月首次发布以来，JavaScript 主要被用于网站自动化。成千上万的有用脚本被创建出来，用途涵盖从处理网站导航到运行在线购物车。JavaScript 的广泛采用意味着网页现在能以更有趣和动态的方式展示信息。

多年来，许多公司开发了自己的技术来进一步增强用户的网络体验。这些公司开发并分发了各自的应用程序，称为*浏览器插件*，以便各种网络浏览器的用户能够查看这些增强功能。

创建这些浏览器增强功能有两个标准：Netscape 插件 API 和 Microsoft ActiveX。这两个标准互不兼容，因此开发者必须为两者都创建各自插件的版本。为了方便起见，在本章中，我将这两种架构下开发的组件统称为"插件"。

正如你可能从这两个标准的名称中猜到的那样，基于 Mozilla 引擎的浏览器（包括 Netscape 浏览器）仅支持 Netscape 插件 API 标准，而 Microsoft Internet Explorer 仅支持 ActiveX 标准。插件开发者通常需要同时支持两种类型的插件，因为浏览器公司似乎不会统一采用某一种标准。

> 你可以从 http://activex.microsoft.com 下载许多适用于 IE 的 ActiveX 控件。Netscape 也在 http://home.netscape.com/plugins 提供了下载插件的场所。

实际上有数十种插件可供下载，一些浏览器甚至预装了几种流行的插件。以下列表包含了一些最受欢迎的插件及其下载地址：

- Macromedia Flash，http://www.macromedia.com/software/flash
- Macromedia Shockwave，http://www.macromedia.com/software/shockwaveplayer
- Sun Java，http://sun.java.com
- RealNetworks RealOne Player，http://www.real.com
- Apple QuickTime，http://www.apple.com/quicktime
- Microsoft Windows Media Player，http://www.microsoft.com/windows/windowsmedia

用户需要安装插件才能查看某些内容，因为浏览器在没有帮助的情况下只能显示两种类型的内容：文本和图像。对于包含其他类型内容的网页，如视频、音乐和 3D 虚拟现实模型，浏览器必须依赖外部插件来处理这些内容。

在本章中，我们将探讨如何将这些不同类型的内容添加到网页中，以及如何使用 JavaScript 来控制它们。从 Java applet 到 ActiveX 控件，我们将了解 JavaScript 如何调用这些对象提供的方法和函数。

#### 将可脚本化的对象插入 HTML 网页

Web 浏览器对待由插件管理的内容与对待网页上的其他内容一样——就像对待一个对象。嵌入页面上的视频、音乐和 Java applet 成为文档对象模型层次结构中的又一个节点。由于它们通常还提供可以由 JavaScript 操作的属性和方法，我们称它们为*可脚本化的对象*。

有三种 HTML 标签能够将这些可脚本化的对象添加到网页中：

- `<applet>`
- `<embed>`
- `<object>`

这三者中，只有 `<object>` 是官方 HTML 标准的一部分。`<applet>` 和 `<embed>` 自 Netscape 2 以来就已在网络浏览器中可用，但互联网标准制定机构认为这些标签设计不当，转而鼓励网络开发者使用替代的 `<object>` 元素。

#### 包含 Sun Java Applet

Java 是一种易于使用的编程语言，被许多不同类型的开发者使用——从企业级专业开发者到普通家庭用户。Java 虚拟机（JVM）是有史以来最早发布的插件之一，它实际上随 Netscape Navigator 2 网络浏览器一起附带。JVM 的一个版本可用于数十种平台，包括：

- 手机
- 个人数字助理（PDA）
- 网络浏览器
- 运行 Microsoft Windows XP、Apple Mac OS、Linux 的个人电脑
- 运行 Sun Solaris、Microsoft Windows 2000、Unix 的商用电脑

*Applet* 是设计用于在网络浏览器内运行的小型 Java 程序。在当今的互联网上，applet 常被用于提供股票行情显示、交互式图表和图形、填字游戏以及聊天室。



#### 如何使用 JavaScript 完成所有操作

为了了解将 Java 小程序嵌入网页有多么简单，我们来看一个简单的 Java 代码示例。以下代码需要保存为名为 HelloWorld.java 的文本文件：

```
/* My first Java program */

import java.applet.Applet;
import java.awt.Graphics;

public class HelloWorld extends Applet {
  public void paint(Graphics g) {
    g.drawString("Hello world!", 75, 75);
  }
}
```

由于 Java 程序是编译型的，我们需要先通过编译器处理这段代码，然后才能在网页浏览器中使用。编译过程将纯文本的 .java 代码文件转换为二进制的 .class 文件。这个 .class 文件可以在任何装有 JVM 的计算机上执行，因为二进制 Java 文件是平台无关的代码，不依赖于特定的操作系统。

在 HTML 中，Java 程序通过 `<applet>` 标签添加到网页中。虽然 `<applet>` 不是官方 HTML 4.01 规范的一部分，但 Netscape 和 IE 都支持它。例如，以下 HTML 将一个 Java 小程序嵌入网页：

```
<applet code="HelloWorld.class"
        width="250"
        height="150"
        id="myapplet">
</applet>
```

#### 如何……下载 Java SDK

Sun Microsystems 免费提供其 Java 平台的多个组件供任何人下载，包括 JVM（它是 Java 运行时环境，即 JRE 的一部分）和 Java 编译器（它是 Java 软件开发工具包，即 SDK 的一部分）。

为了确保你拥有最新的 JVM，请访问 Sun Java 网站 http://java.sun.com/getjava/index.html。该页面会确保你的网页浏览器安装了最新版本的 Java 并准备就绪。

如果你想下载编译器以便尝试创建 Java 小程序，可以从 http://java.sun.com/j2se/downloads.html 免费下载你自己的 SDK。Sun Java 网站上提供了多个优秀的教程，帮助你创建你的第一个 Java 程序。

使用这段 HTML 代码，网页浏览器将尝试加载名为 HelloWorld.class 的 Java 小程序，并在屏幕上为其保留一个宽 250 像素、高 150 像素的区域。

你可以在图 15-1 中看到该 Java 小程序在网页浏览器中的显示效果。

HTML `<applet>` 标签有许多可选属性，可用于进一步定义小程序在浏览器中的属性。表 15-1 列出了这些属性。

| 属性 | 用途 |
| --- | --- |
| code | 类文件名 |
| codebase | 类文件子目录 |
| archive | 包含该类文件的 .zip 文件名称 |
| alt | 不支持 `<applet>` 标签的浏览器应显示的文本 |
| align | 小程序与旁边放置的文本和图像的对齐方式 |
| height | 小程序的高度，以像素或百分比表示 |
| width | 小程序的宽度，以像素或百分比表示 |
| hspace | 在小程序周围保留的水平空间（以像素为单位） |
| vspace | 在小程序周围保留的垂直空间（以像素为单位） |
| mayscript | 允许小程序访问 JavaScript |
| name | 在 DOM 中使用的小程序名称 |

**表 15-1** HTML `<applet>` 标签的属性

#### 我的第一个 Java 小程序

网页开发者还可以选择通过 HTML `<param>` 标签向 Java 小程序传递多个参数，以帮助自定义小程序。例如，我们可以修改 Hello World Java 小程序以接受一个参数：

```
/* My first Java program */

import java.applet.Applet;
import java.awt.Graphics;

public class HelloWorld extends Applet {
  String displayString;

  public void init() {
    // We are expecting a <param> named "display"
    displayString = getParameter("display");
  }

  public void paint(Graphics g) {
    g.drawString(displayString, 75, 75);
  }
}
```

然后，我们可以在 `<applet>` 标签内使用 HTML `<param>` 标签，向小程序传递要显示的自定义字符串，如下所示：

```
<applet code="HelloWorld.class"
        width="250"
        height="150"
        id="myapplet">
    <param name="display" value="This is my applet!">
</applet>
```

使用这个新参数，我们无需重新编译代码即可更改 Java 小程序显示的字符串。一个小程序可以接受多个参数，因此你的 Java 小程序可以设计为完全从编译代码外部进行配置。

#### 使用 JavaScript 连接到 Java 小程序

正如你所预期的，JavaScript 能够调用任何 Java 小程序的公共方法和设置其公共属性。我们在上一节创建的 Java 小程序已经拥有多个公共属性和方法，其中一些是由 HelloWorld 的父类 Applet 自动提供的。

我们可以创建一个小型 JavaScript 函数，通过调用适当的公共属性和方法来修改显示的字符串并强制小程序刷新，如下所示：

```
<script language="JavaScript" type="text/javascript">
function displayString() {
    var applet = document.getElementById("myapplet");
    applet.displayString = "String is set here";
    applet.repaint();
}
</script>
```

该 JavaScript 函数首先使用我们熟悉的 `document.getElementById()` 函数创建一个变量，该变量将指向我们 HTML 网页上的 Java 小程序。

然后我们修改 `displayString` 属性，该属性在 HelloWorld Java 小程序内部定义。为了让 Java 将新字符串显示到屏幕上，我们必须调用小程序的 `repaint()` 方法。

当然，在页面上显示一个小型按钮或其他用户控件也很有帮助，以便通过 onclick 事件触发这个 JavaScript 函数。

```
<applet code="HelloWorld.class"
        width="250"
        height="150"
        id="myapplet">
    <param name="display" value="This is my applet!">
</applet><br><br>

<form action="#">
<input type="button" value="Modify Applet"
       onclick="displayString()">
</form>
```

这段 HTML 代码将在小程序窗口下方添加一个小型按钮控件。点击按钮将改变我们的小程序显示的字符串，如图 15-2 所示。

## 第 15 章：使用 JavaScript 管理浏览器插件

#### 在网页中嵌入电影和音乐

在网页中嵌入电影和音乐的处理方式与嵌入 Java 小程序有很大不同。首先，`<applet>` 标签不能用于将这些类型的文件嵌入网页（除非你使用 Java 小程序来显示它们）。

将多媒体文件插入网页的第一种方法是使用 `<embed>` 标签。使用 `<embed>` 标签确实比使用 `<object>` 标签更容易，但使用时请记住 `<embed>` 不是官方标准的一部分。

```
<embed src="myMovie.avi" autostart="true" loop="true" width="160" height="120"></embed>
```

使用 `<embed>` 标签时，你通过标签自身的属性将所有参数传递给插件。`<embed>` 没有 `<param>` 标签。`<embed>` 标签本身支持三个参数——src、width 和 height。嵌入内容的源 URL 通过 **src** 属性传递。浏览器中保留的空间大小通过 **width** 和 **height** 属性传递。

> 注意
你的计算机需要一个能够处理 Windows AVI 文件的浏览器插件才能观看我们示例中的电影。不过，大多数流行的视频播放器都可以做到，包括 Windows Media Player、Apple Quicktime 和 RealNetworks RealOne Player。

在前面的示例中，负责播放电影的插件接收了 autostart 参数以及 loop 参数。当然，如何解释这些参数的含义以及如何处理它们，取决于插件软件本身。

> 注意
IE 是目前唯一支持 ActiveX 控件（如 Windows Media Player）的浏览器。

我们也可以使用官方的 `<object>` 标签将电影嵌入网页。`<object>` 标签稍微复杂一些，特别是因为它使用一个非常长的十六进制数字来引用插件。

```
<object id="ActiveMovie1"
    classid="CLSID:05589FA1-C356-11CE-BF01-00AA0055595A"
    width="320" height="240">
    <param name="ShowDisplay" value="1">
    <param name="ShowControls" value="1">
    <param name="AutoStart" value="1">
    <param name="PlayCount" value="10">
    <param name="FileName" value="myMovie.avi">
</object>
```

前面的 HTML 代码使用 Microsoft ActiveMovie 控件插入了一个对象，该控件通过那个很长的 **classid** 属性来标识。ActiveMovie 是随



 # 如何在网页中嵌入 Windows Media Player 9 对象

随着 Windows Media Player 9 的发布，微软进一步提升了其视频和音乐播放应用的功能。Windows Media Player 9 还包含一个 ActiveX 控件，允许开发者在网页中嵌入音乐和电影。

然而，由于并非所有人都已升级到这个新版播放器，强制访客下载它才能查看内容可能不太合适。但如果你能合理确定目标用户已经安装了该软件，就可以轻松地在网页中加入这个新的`<object>`标签。

注意，以下 HTML 代码中的 **classid** 值有所不同，用于指定媒体文件名称的参数名称也不同。

```
<object id="Player" height="0" width="0"
classid="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"
width="160" height="120">
    <param name="URL" value="myMovie.avi">
</object>
```

微软 Windows Media Player 6.4 负责管理电影的显示和播放细节。开发者可以向 ActiveMovie 控件传递多个属性来控制大小、音量、平衡和位置。你可以在图 15-3 中看到一个 ActiveMovie 控件的示例。

如果我们不想依赖 Windows Media Player 来播放电影，可以使用属于 Apple Quicktime Player 的 **classid** 属性，如下所示：

```
<object id="QuicktimeMovie1"
    classid="clsid:02BF25D5-8C17-4B23-BC80-D3488ABDDC6B"
    width="320" height="240"
    codebase="http://www.apple.com/qtactivex/qtplugin.cab">
    <param name="src" value="myMovie.avi">
    <param name="autoplay" value="true">
    <param name="controller" value="false">
</object>
```

上述代码将使用 Apple Quicktime Player 插件来显示我们的电影。同样，这仅在支持 ActiveX 控件的 Web 浏览器中有效。

#### 使用 JavaScript 连接音乐和媒体对象

正如我们可以使用 JavaScript 重置 Java 小程序的属性并调用其方法，我们在处理其他嵌入对象时也可以应用相同的原理。例如，以下 JavaScript 函数可用于停止和启动显示在 ActiveMovie 控件中的电影。

```
<script language="JavaScript" type="text/javascript">
var movie = document.getElementById("ActiveMovie1");
function startMovie() {
    movie.Run();
}
function stopMovie() {
    movie.Stop();
}
</script>
```

上述 JavaScript 代码获取了一个名为 ActiveMovie1 的元素的变量引用，该元素正是我们嵌入的电影控件。然后我们可以调用该控件的 Run() 和 Stop() 方法来启动和停止电影。

我们可以通过向网页添加两个 HTML 按钮控件来利用这些函数，允许用户自行停止和启动电影。

```
<form action="#">
    <input type="button" value="Start Movie" onclick="startMovie()">
    <input type="button" value="Stop Movie" onclick="stopMovie()">
</form>
```

#### 在网页中使用微软日历控件

微软提供了一些有趣的 ActiveX 控件，你可以在你的 HTML 网页中使用。其中一个控件就是微软日历控件，它可以用来显示日历并允许用户选择日期。对于选择近期过去或将来的日期来说，这个工具可以节省大量时间。

> IE 是目前唯一支持日历控件等 ActiveX 控件的浏览器。

图 15-4 展示了日历控件在网页浏览器中的外观。当然，知道了日历控件的 class ID，使用`<object>`标签将其添加到网页中就相当容易了。

```
<object id="myCalendar" width="480" height="190"
 classid="CLSID:8E27C92B-1264-101C-8A2F-040224009C02">
    <param name="Year" value="2004">
    <param name="Month" value="7">
    <param name="Day" value="17">
</object>
```

我们可以使用熟悉的`<param>`语法来传递要显示的当前年、月和日期。

当然，日历控件像网页中大多数其他嵌入对象一样是可脚本化的。因此，我们只需要一个包含对象引用的变量，就可以使用 JavaScript 自由修改其属性和设置。

本章介绍的基本原理可以扩展到你能想到的几乎任何类型的内容。Macromedia Flash 动画、虚拟现实 3-D 模型和 Adobe Acrobat PDF 文档都可以通过插件在浏览器窗口中处理。而且大多数对象都可以使用 JavaScript 进行脚本化。

JavaScript 已经稳固地确立了自己作为网站开发核心技术的地位。随着互联网进入 XML 和 XHTML 时代，远离 HTML 时代，我们可以相信 JavaScript 仍将是流行的标准，因为没有比它更好的技术能为网页带来自动化和交互性。

### 附录 A HTML 4.01 标签

下表列出了每个 HTML 4.01 标签及其用途的简要说明。但请注意，微软和 Netscape 在某些情况下添加了自己的标签，因此它们的列表可能与此不匹配。

| 标签名称 | 用途 |
|---|---|
| `<a>` | 创建超链接，或在页面内定义书签 |
| `<abbr>` | 表示缩写形式 |
| `<acronym>` | 表示首字母缩略词 |
| `<address>` | 表示邮寄地址 |
| `<applet>` | 官方已弃用；嵌入 Java 小程序 |
| `<area>` | 客户端图像映射语法的一部分 |
| `<b>` | 将封闭文本定义为粗体 |
| `<base>` | 定义文档的基础 URI |
| `<basefont>` | 官方已弃用；定义文档的基础字体大小 |
| `<bdo>` | 国际化（i18n 双向覆盖） |
| `<big>` | 将封闭文本定义为特大号 |
| `<blockquote>` | 将封闭文本定义为块引用 |
| `<body>` | 表示网页的主体 |
| `<br>` | 插入新行 |
| `<button>` | 向表单添加命令按钮 |
| `<caption>` | 为表格添加标题 |
| `<center>` | 官方已弃用*/


| 标签名称 | 用途 |
| --- | --- |
| `<form>` | 定义 HTML 网页表单 |
| `<frame>` | 定义框架内容 |
| `<frameset>` | 定义一组框架 |
| `<h1>` | 定义标题文本，级别 1（最大） |
| `<h2>` | 定义标题文本，级别 2 |
| `<h3>` | 定义标题文本，级别 3 |
| `<h4>` | 定义标题文本，级别 4 |
| `<h5>` | 定义标题文本，级别 5 |
| `<h6>` | 定义标题文本，级别 6（最小） |
| `<head>` | 表示网页的头部区域 |
| `<hr>` | 插入水平线 |
| `<html>` | 所有其他元素的父标签 |
| `<i>` | 将封闭文本定义为斜体 |
| `<iframe>` | 定义浮动框架 |
| `<img>` | 插入图像 |
| `<input>` | 向表单添加表单控件 |
| `<ins>` | 将封闭文本定义为插入文本 |
| `<isindex>` | 官方已弃用；单行提示 |
| `<kbd>` | 将封闭文本定义为用户要输入的文本 |
| `<label>` | 向表单插入标签 |
| `<legend>` | 字段集的图例 |
| `<li>` | 列表的列表项 |
| `<link>` | 独立于媒体的链接 |
| `<map>` | 定义客户端图像映射 |
| `<menu>` | 官方已弃用；定义菜单列表 |
| `<meta>` | 插入与 HTML 文档相关的数据（称为元数据） |
| `<noframes>` | 对不支持框架的浏览器的替代内容 |
| `<noscript>` | 对不支持脚本的浏览器的替代内容 |
| `<object>` | 向文档插入对象 |
| `<ol>` | 定义有序列表 |
| `<optgroup>` | 定义选项组 |
| `<option>` | 定义选择列表的选项 |
| `<p>` | 表示段落 |
| `<param>` | 提供要传递给嵌入内容的属性 |



#### 如何使用 JavaScript 完成所有任务

| 标签名 | 用途 |
|---|---|
| `<pre>` | 将包含的文本定义为预格式化文本 |
| `<q>` | 将包含的文本定义为简短的内联引用 |
| `<s>` | 已正式弃用；将包含的文本定义为删除线 |
| `<samp>` | 将包含的文本定义为示例程序输出 |
| `<script>` | 定义一个嵌入式脚本 |
| `<select>` | 在网页表单中插入一个列表框控件 |
| `<small>` | 将包含的文本定义为小号文本 |
| `<span>` | 将内联文本定义为一个实体 |
| `<strike>` | 已正式弃用；将包含的文本定义为删除线 |
| `<strong>` | 将包含的文本定义为强调文本 |
| `<style>` | 定义一个嵌入式样式表 (CSS) |
| `<sub>` | 将包含的文本定义为下标 |
| `<sup>` | 将包含的文本定义为上标 |
| `<table>` | 创建一个表格 |
| `<tbody>` | 定义表格主体 |
| `<td>` | 向表格中插入一个新单元格 |
| `<textarea>` | 在网页表单中插入一个多行文本表单控件 |
| `<tfoot>` | 定义表格页脚 |
| `<th>` | 向表格中插入一个新的标题单元格 |
| `<thead>` | 定义表格页眉 |
| `<title>` | 为文档提供一个标题 |
| `<tr>` | 向表格中插入一个新行 |
| `<tt>` | 将包含的文本定义为等宽（固定宽度）文本 |
| `<u>` | 已正式弃用；将包含的文本定义为下划线 |
| `<ul>` | 创建一个无序列表（项目符号） |
| `<var>` | 将包含的文本定义为程序变量 |

## 附录 B

## JavaScript 快速参考

![](img/f14dd58a324d5464a114c30c1d4c4c9b_350_0.png)

本附录列出了可在 JavaScript 中使用的语句和系统对象。表 B-1 显示了 JavaScript 1.5 中可用的所有语句。JavaScript 2.0 没有为此列表添加新的语句。表 B-2 和 B-3 分别列出了 JavaScript 1.5 和 2.0 的系统对象。

| 语句 | 描述 |
| --- | --- |
| // | 创建单行注释 |
| /* ... */ | 创建一个注释块 |
| break | 跳出循环或 **switch** 语句 |
| continue | 开始下一次循环迭代 |
| do-while | 创建一个只要指定条件为真就执行一条或多条语句的循环，但总是至少执行一次 |
| for | 创建一个执行一条或多条语句，直到计数器达到设定值的循环 |
| for-in | 创建一个遍历对象属性或数组内容的循环 |
| if-else | 仅在指定条件为真时执行代码 |
| label | 允许 **break** 或 **continue** 语句跳出嵌套循环 |
| return | 使函数退出，可选择返回一个值 |
| switch | 根据指定表达式的值，选择执行几个 case 中的一个 |
| throw | 引发一个异常 |
| try-catch | 拦截并处理异常 |
| while | 创建一个只要指定条件为真就执行一条或多条语句的循环 |
| with | 允许访问对象的属性和方法，而无需使用该对象 |

## 附录 B：JavaScript 快速参考

333

| 类名 | 描述 |
|---|---|
| Array | 允许将数据列表存储在单个变量中 |
| Boolean | 布尔值的包装器 |
| Date | 允许处理日期和时间 |
| Function | 允许以编程方式定义函数 |
| Math | 包含便捷的数学常量和函数 |
| Number | 原始数值的包装器 |
| Object | 所有对象都派生自这种数据类型 |
| RegExp | 为 JavaScript 中的正则表达式提供支持 |
| String | 字符串值的包装器 |

**表 B-2** JavaScript 1.5 中可用的内置系统对象

| 类名 | 描述 |
|---|---|
| Array | 允许将 Object 类型的数据列表存储在单个变量中；等同于 Array[Object] 数据类型 |
| Array[type] | 允许将 type 类型的数据列表存储在单个变量中 |
| Boolean | 支持只能存储 true 和 false 值的变量 |
| char | 支持只能存储单个字符的变量 |
| ConstArray | 允许将 Object 类型的数据列表存储在单个常量中；等同于 ConstArray[Object] 数据类型 |
| ConstArray[type] | 允许将 type 类型的数据列表存储在单个常量中 |
| DynamicArray[type] | 允许将可调整大小的 type 类型数据列表存储在单个变量中 |
| Function | 函数的“数据类型” |
| Integer | 支持只能存储整数的变量 |
| Never | 支持不能包含任何值的变量 |
| Null | 支持只能存储 null 值的变量 |
| Number | 支持只能存储数字的变量 |
| Object | 支持可以包含任何值的变量 |
| Prototype | 支持包含基于原型的对象的变量（JavaScript 1.5 处理对象的方式） |
| StaticArray[type] | 允许将可写的 type 类型数据列表存储在单个变量中 |
| String | 支持只能存储字符串的变量 |
| Type | 数据类型的“数据类型” |
| Void | 支持只能存储 undefined 值的变量 |

B

**表 B-3** JavaScript 2.0 中可用的内置系统对象

![](img/f14dd58a324d5464a114c30c1d4c4c9b_353_0.png)

![](img/f14dd58a324d5464a114c30c1d4c4c9b_353_1.png)

![](img/f14dd58a324d5464a114c30c1d4c4c9b_353_2.png)

![](img/f14dd58a324d5464a114c30c1d4c4c9b_353_3.png)

![](img/f14dd58a324d5464a114c30c1d4c4c9b_353_4.png)

![](img/f14dd58a324d5464a114c30c1d4c4c9b_353_5.png)

## 索引

符号

+   * "（双引号），用于字符串字面量，74
* ""（空字符串），34，73，87
* #（井号）
  * 作为有效的 URL，186
  * 用于 RGB 值，262
* #special 选择器，270
* $（美元符号），在正则表达式中，87
* %（取模）运算符，42
* '（单引号），用于字符串字面量，74
* ()（圆括号），用于参数列表，52
* (...) 剩余参数，61
* *（星号乘数），229-230
* */（星号斜杠），块注释结束，44
* ++ 运算符，35
* .（点）运算符，73，77-78
* .class 文件（Java），316
* .css 文件，267，269-270
* .java 代码文件，316
* .js 文件扩展名，157
* .NET Framework（微软），14
* /（正斜杠）
  * 在 HTML 中，143
  * 在正则表达式中，87，89
* /*（斜杠星号），块注释开始，44
* //（双正斜杠），作为注释标记，在 44
* :（冒号）
  * 标签结束，43
  * 分隔属性和值，122
* ;（分号）
  * 用于附加 JavaScript 命令，159
  * 语句结束，100
* < 和 >（尖括号），在 HTML 中，142
* <!-- 和 --> HTML 注释标记，19，144，156

+   * <!DOCTYPE> 标签，146-147
* <?xml?> 声明，145
* <applet> 标签，315-317，319
* <applet> 标签属性，317
* <b> 标签，261，263
* <body> 标签/元素，19，276-277
* <br> 标签，263
* <button> 元素，194
* <center> 标签，263
* <div> 标签/元素，174-176，198，264-265，269，277
  * 属性，265
  * 具有特殊 id 属性，270
* <embed> 标签，315，321-324
  * 属性，321
  * 高度属性，321
  * src 属性，321
  * 宽度属性，321
* <font> 标签，261-263
* <font> 标签颜色属性，262
* <form> 标签/元素，184-186
  * action 属性，185-186，195
  * 属性，184-185
  * 事件处理器，195
  * method 属性，195
  * onsubmit 属性，195-197，220
  * submit() 方法，219-220
* <frame> 标签，225-226
  * 属性，233-234
  * frameborder 属性，235
  * name 属性，235
  * noresize 属性，235
  * src 属性，234
* <frameset> 标签/元素，225，229
  * 属性，225
  * onload 和 onunload 事件处理器，226
  * rows 和 cols 属性，227-232
* <head> 标签，18，226
* <h1> 标题标签，19
* <html> 标签，18，145



## 336 如何用 JavaScript 做所有事情

- &lt;i&gt; 标签，261
- &lt;img&gt; 标签/元素，211, 276
  - 属性，218
  - id 属性，275
  - src 属性，211
- &lt;input&gt; 元素，187, 194, 271
  - 默认类型，186
  - maxlength 属性，189
  - size 属性，189
  - value 属性，189, 194
- &lt;layer&gt; 标签，172-175
- &lt;link&gt; 元素，267, 269
- &lt;meta&gt; 标签，147-148
- &lt;meta&gt; 标签属性，147
- &lt;noframes&gt; 标签，226-227
- &lt;noscript&gt; 标签，154-156
- &lt;object&gt; 标签/元素，315, 321-322, 324
- &lt;object&gt; 标签 classid 属性，321-322
- &lt;option&gt; 元素，189, 193
- &lt;option&gt; 元素属性，193
- &lt;param&gt; 标签，318-319
- &lt;script&gt; 标签/元素，16, 153-154, 158, 198
  - 属性，19, 153-154
  - 在 HTML 页面中，17-18
  - language 属性，153
  - src 属性，157
  - type 属性，154
- &lt;select&gt; 元素，189
  - 属性，192
  - 用于列表框，217
  - multiple 属性，191
  - size 属性，191-192
- &lt;span&gt; 元素，265
- &lt;span&gt; 元素属性，265
- &lt;style&gt; 标签/元素，151, 264, 266-267
- &lt;textarea&gt; 元素，193, 198
- &lt;textarea&gt; 元素属性，193
- &lt;title&gt; 标签，147
- ? (问号)，用于表达式匹配，34
- [] (方括号操作符)，73, 96, 104-106
- ^ (脱字符)，在正则表达式中，87
- { 和 }，用于包裹语句，32
- {} (花括号)，用于对象字面量，122
- \ (反斜杠)，在正则表达式中，88-89
- \\ 双反斜杠（转义反斜杠），89
- \d 标记，在正则表达式中，87-88
- , (逗号)
  - 分隔参数，52
  - 分隔属性-值对，122

## A

- Abort 事件，216
- 绝对定位，258
- 访问键，激活的组合键，189
- Accesskey 参数，189
- Activate 事件，209
- ActiveMovie 控件（Microsoft），321-323
- ActiveScript，142
- ActiveX 控件，321, 324
- ActiveX（Microsoft），314
- 地址栏（浏览器），258
- Adobe Acrobat PDF 文档，142
- Adobe GoLive，12-13
- 警告框，20-21, 197
- 警告消息，显示，20-21, 288-289
- Alert（消息）框，288-289
- Alert() 方法，288
- Allaire 公司，11
- 祖先，类作为，130
- 尖括号（< 和 >），在 HTML 中，142
- Animate() 函数，创建，275
- 动画文本，277
- 动画，259-278
  - 解释，260
  - 使用 JavaScript 实现，274-278
  - 使用定时器事件，274
- API（应用程序编程接口），244
- Apple Quicktime 播放器，322
- 小程序（Java），5, 315-320
- 应用程序错误，定义，46
- 数组的数组，110, 112
- Array 类，102
- Array 类子类，111
- 数组元素
  - 访问，104-106
  - 限制为类型，113
- 数组索引，96, 104-105
- 数组字面量，100-101
- 数组对象，96
  - 创建，97-104
  - index 属性，101
  - input 属性，101
  - length 属性，99, 101
  - 方法，102-104
  - 属性和方法，101-104
- 零长度数组，97
- 数组，95-115
  - 创建空数组，97-99
  - 在一行代码中创建并初始化，100
  - 使用 Array 类创建，102
  - JavaScript 2.0 增强，111-112
  - 长列表的数组，100
  - 多维数组，107-115
  - 具有数字索引的数组，106
  - 并行数组，109-110
  - 在数组中设置和检索值，104-106
  - 指定初始长度，99

As 操作符，51
ASCII 码，214
ASP .NET 平台，14
ASP（应用程序服务器页面），142
ASP 网页，将其自身提交到的表单，195
星号（*）乘数，229-230
星号和斜杠（*/），块注释结束，44
属性，解释，184
AVI 文件，321

## B

反斜杠（\），在正则表达式中，88-89
块注释，44
Blur 事件，209-210
Blur 事件触发顺序，210
Blur() 方法，220
Body 部分（HTML 文档），18-19, 145
布尔数据类型，27, 91
  - 将其他数据类型转换为，31
  - 返回布尔值的表达式，50
  - 用于已加载的框架，239-240
布尔字面量，91
Break 语句，34, 40-41, 58
断点，调试中，293
浏览器地址栏，258
浏览器兼容性问题，162-170
  - 代码的，171-177
  - DHTML 的，171
  - 事件的，220-221
  - 样式的，272-273
浏览器 DOM，14, 162
浏览器错误消息，解释，282
浏览器事件，158
  - 处理，207-221
  - Internet Explorer 支持的，199
浏览器框架。参见 框架（浏览器）
浏览器历史记录列表，257-258
浏览器市场特性竞争，170
浏览器插件，254, 313-325
浏览器刷新，258
浏览器嗅探代码，221
浏览器软件属性，254-256
浏览器状态栏，253
浏览器对方法的支持，169-170
浏览器定时器，251
浏览器类型，检测，164, 167, 256
浏览器使用统计，163
浏览器版本
  - 检测，164
  - 了解所需的最低版本，15
浏览器窗口，252-254
  - 调整大小并居中，256-257
  - 向窗口写入文本，21-22

浏览器
  - 检查你的代码，312
  - 检测，174
  - 检测运行的类型，164-169
  - DOM，14, 162
  - 首个支持 JavaScript 的，6
  - 获取以测试你的代码，312
  - 与之交互，243-258
  - 不支持框架的，226-227
  - 重定向到新网页，258
  - 依赖外部插件，315
  - 返回到上一页，257
  - 在所有浏览器上测试，312
  - 不支持脚本的，154-156
  - 使用最新版本，163
  - 网页浏览者的使用，162-163, 169
Bug，定义，278
按钮标题，194
按钮控件（表单），193-194, 220, 320, 323
按钮（表单），193
字节，91

## C

计算器（在线），182-183
日历控件（Microsoft），324-325
调用堆栈，102
调用函数，53
按钮的标题，194
捕获事件，解释，208
脱字符（^），在正则表达式中，87
Case 子句，33-34
Catch 块，Netscape 条件，302
Catch 子句，297-304
捕获，解释，195
Change 事件，216
Changeimage() 函数，211-212, 274
Char 数据类型，91-92
Checkform() 函数，200-202
Checkkey() 函数，214
子类，131
子节点，246
HTML 元素的 class 属性，265
类继承的好处，132-133
类成员，68
  - public 与 private，136
  - static 与 instance，135-136
类属性，78。另见 属性
  - 访问，120, 128
  - 通过赋值创建，126
  - 在 JavaScript 2.0 中定义，127
  - 继承的，131, 134
类
  - 添加构造函数，127
  - 添加方法和属性，123-125
  - 作为祖先，130
  - 将函数附加到，124
  - 内置的，63-93
  - 与代码重用，308
  - 包含多个构造函数，131
  - 创建，117-137
  - 使用类创建方法，128
  - 在类中定义函数，128
  - 在 JavaScript 2.0 中定义，127-129
  - 扩展，123-125
  - 继承属性和方法，131, 134
  - 使用 new 关键字实例化，128
  - JavaScript 1.5，70
  - 使用继承组织，130-135
  - 用于购物车项，308
  - 测试，308
  - 将属性和函数转换为，68-69
  - 用作数据类型，71
- Classid 属性（<object> 标签），321-322
- Click() 方法，220
- Clickme() 函数，220
- 客户端，定义，8
- 客户端-服务器类比，8
- 客户端-服务器通信，184
- 客户端表单，182-183
- 客户端 JavaScript
  - 定义，8
  - 处理表单输入，182-183
- 客户端语言，JavaScript 作为，14
- 结束标签（HTML），142-143
- 代码重用
  - 通过类继承，132
  - 通过复制粘贴，122
  - 使用类和对象，308
- 冒号（:）
  - 标签结束，43
  - 分隔属性和值，122
- 颜色，在 HTML 中指定，262
- Cols 属性（<frameset> 标签），227-232
- 逗号
  - 用于分隔参数，52
  - 用于分隔属性-值对，122
- 注释标记，HTML 与 JavaScript，19, 44
- 注释掉一个函数（调试中），289-290
- 注释
  - HTML，19, 144, 156
  - JavaScript，19, 43-44
  - 用途，44, 289-290
- 编译器，定义，9
- 组件化程序，307
- 复合属性，解释，268
- 条件 catch 块（Netscape），302
- 条件语句，30-34
- 确认框，21
- 控制台（JavaScript），283, 286-287, 290-291
- Const 关键字，28
- 常量，27-29, 67, 114-115
- ConstArray，创建，114-115
- ConstArray 类，114-115
- 构造函数（构造函数），72
  - 添加到类中，127
  - 调用，119-121
  - 包含多个构造函数的类，131
  - 创建，119
  - 从构造函数创建对象，121
- Continue 语句，40-41
- 控件焦点，解释，188
- 控件名称，通过控件名称访问控件，200
- Cookie，解释，248
- 复制粘贴，通过复制粘贴重用代码，122
- 计数器变量，28, 55-56
- 跨浏览器兼容性问题，162-170
  - 代码的，171-177
  - DHTML 的，171
  - 事件的，220-221
  - 样式的，272-273
- 跨框架脚本，安全风险，239
- CSS 属性，268
  - 与 JavaScript 属性名称对比，272-273
  - 列表，269
  - 参考指南，268
- CSS（层叠样式表），150-153。另见 样式表
  - 基础，260-273
  - 好处，150
  - 与框架对比，224
  - 选择器，266-267
  - 大小调整和定位，269-270, 276-277
  - 为何是层叠的，261
- CSS 1级标准（W3C），261
- CSS 定位属性，270
  - 使用 CSS 定位属性进行动画，276-277
  - 定义，269
- CSS 验证器服务（W3C），273
- 花括号（{}）
  - 用于包裹语句，32
  - 用于对象字面量，122
- 当前日期和时间，检索，64

## D

- 数据完整性，私有类成员用于，136
- 数据列表。参见 数组对象；数组
- 数据存储，26-29
- 数据类型（JavaScript 2.0），28, 59, 69-71, 91-93
  - 转换为布尔值，31
  - 使用类作为，71



## D

-   Date 类，64，79-80
-   Date 类构造函数格式，82
-   Date 构造函数，80，82
-   Date 对象，79-80，124
-   Date 对象的 getMonth() 函数，99
-   Date 对象方法列表，80-82
-   日期处理函数，79-82
-   调试器，291-293
-   调试代码
    -   添加到程序中，287-290
    -   说明，288
-   （JavaScript 程序的）调试，281-293
    -   定义，278
    -   设计易于调试的程序，306-308
    -   使用断点，293
    -   使用注释进行调试，289-290
-   调试软件，291-293
-   默认子句（switch 语句），34
-   设置默认对象，44-46
-   已弃用的 HTML 标签，145-146
-   开发人员测试自己的程序，311
-   开发环境，7-13
-   DHTML（动态 HTML），151，171-177
-   DHTML 菜单，172
-   显示设置（操作系统），256-257
-   查询文档模型，169-170
-   Document 对象，248-252
    -   数组，248
    -   body 属性，249
    -   forms 数组，200-202
    -   在 Internet Explorer 6.0 中，74
    -   方法，248
    -   用于更新时间，251
-   使用注释编写文档，144
-   Document.write() 函数，21-22，42，54，58，248，288
-   美元符号（$）在正则表达式中，87
-   DOM（浏览器），14，162
-   DOM（文档对象模型），5，8，244
    -   基础知识，245-248
    -   被视为节点的文档部分，246
    -   解释，244
    -   中的对象，245
-   DOM（JavaScript），7
-   DOM Level 1 (DOM 1)，169，246
-   DOM Level 3，247
-   DOM Level 2，246，247
-   DOM Level 2 事件规范，208
-   DOM Level 0，245
-   使用前检查 DOM 方法，169-170
-   DOM 1 层级（DOM 树），246
-   DOM 标准（W3C），8，244
-   DOM 遍历，247
-   DOM 树，246-247
-   DOS/Windows 环境中的 JavaScript，9
-   点运算符（.），73，77-78
-   Dothis() 函数，194
-   双反斜杠（\\），89
-   双正斜杠（//）用于注释标记，19，44
-   用于字符串字面量的双引号（"），74
-   Douglas Crockford 的 JavaScript Lint 验证器，287
-   do-while 循环，37
-   Dreamweaver MX，10-12，291
-   下拉列表框控件，189-190，217，251-252
-   动态列表框，251-252
-   动态样式修改，270-272
-   标记动态文本，265
-   动态加载图像，274-276
-   创建 DynamicArray，114
-   DynamicArray 类，114

## E

-   ECMA（欧洲计算机制造商协会），5，59
-   ECMAScript，6
-   ECMAScript 第 4 版标准，6
-   ECMAScript 规范，287
-   800 x 600 分辨率，256
-   用于访问表单值的 Elements 数组，202-203
-   Else 子句，32
-   Else-if 子句，32
-   电子邮件中的表单内容，185
-   嵌入式多媒体的插件，254
-   定义嵌入式样式表，266-267
-   空数组
    -   创建，97-99
    -   测试是否存在潜在使用，311
-   定义空函数，119
-   空字符串（""），34，73，87
-   不同环境中的 JavaScript 版本，142
-   更严格的错误检查级别，283
-   IE 中的错误详情，285
-   Error 事件，216
-   错误处理，46-49
-   错误图标，283
-   （IE 中的）错误消息框，284
-   错误消息，47
    -   查找错误来源，284-285
    -   解释错误消息，282，285-287
    -   在 JavaScript 控制台中，286-287
    -   错误消息中列出的行号，285-286
-   Error 对象（IE），298，301
    -   创建，301
    -   属性，301
-   启用和禁用错误报告，282-284
-   错误字符串（Netscape），298
-   JavaScript 中的错误类型，283
-   测试错误处理代码，311
-   使程序防错，295-312
-   错误，46
    -   错误原因，282-287
    -   以编程方式检测错误，48
    -   强制测试错误处理代码，311
    -   返回程序，296
    -   错误来源，163
    -   可能出错的情况，46
-   Escape() 函数，85
-   转义字符序列，85
-   转义文件，解释，85
-   设置事件属性，218
-   事件冒泡，219
-   事件触发测试，210，212-213
-   事件处理程序，185，208
    -   <form> 元素，195
    -   返回 false，213
    -   为 HTML 标签设置，218
    -   使用 event 属性，218
    -   查看事件处理程序，218
    -   编写事件处理程序，208-217
-   事件处理（浏览器事件），207-221
-   捕获事件名称，199
-   Event 属性，218
-   JavaScript 中的事件触发，219-220
-   事件规范（DOM Level 2），208
-   事件（Web 表单），185-186，188，192，208
    -   与浏览器不兼容性，220-221
    -   取消事件，213-214
    -   捕获事件，208
    -   在表单控件上捕获事件，197-199
    -   事件类别，209
    -   由最内层元素首先处理，219
    -   表单控件的可编程事件，197-199
    -   拦截事件，208
    -   响应事件调用 JavaScript，158
    -   事件触发顺序，209-210，212-213
    -   非标准事件，221
-   异常冒泡，299-301，304
-   异常，296-297
    -   使用 try-catch 捕获异常，297-304
    -   使用 throw 语句创建异常，304-306
    -   重新抛出异常，305
    -   未处理的异常，303
-   使用 DHTML 创建可展开的树形菜单，173
-   表达式，27，31-32，38，49-50
    -   作为函数的参数，50
    -   表达式类型列表，49
    -   返回布尔值的表达式，50
-   extends 关键字，130
-   加载外部 JavaScript 文件，157-158
-   导入外部样式，267

## F

-   F（浮点数）后缀，71
-   FactorString 变量，57
-   FIFO（先进先出）顺序，102
-   文件，转义，85
-   try-catch 语句中的 finally 子句，302-304
-   finally 子句（非标准），302-304
-   FireEvent() 方法，220
-   事件触发顺序，209-210，212-213
-   Flash 文件（Macromedia），142
-   浮点数（F）后缀，71
-   焦点（控件），解释，188
-   Focus 事件，209-210
-   Focus 事件触发顺序，210
-   Focus() 方法，220
-   font 属性，268
-   字体样式元素（HTML 4.01），148-149
-   for 循环，37-38，252
-   for-in 循环，38-40，61，73，105-106
    -   遍历数组，106
    -   遍历哈希表，105
-   表单控件值，200-205
    -   使用 getElementById() 访问，204
    -   使用 getElementsByName() 访问，204
    -   使用 getElementsByTagName() 访问，205
    -   使用 elements 数组访问，202-203
    -   使用 forms 数组访问，200-202
-   表单控件
    -   在表单控件上捕获事件，197-199
    -   当前活动的控件，188
    -   表单控件列表，187
    -   可编程事件，197
    -   访问前测试是否存在，241
-   创建表单处理程序的技术，183
-   forms 数组，200-202，248
-   表单（Web），179-206
    -   向表单添加控件，186-195
    -   通过电子邮件接收表单内容，185
    -   处理用户输入，180
    -   初始化表单，217
    -   onfocus/onblur/onchange 事件，188，192
    -   onsubmit 和 onreset 事件，186
    -   使用客户端 JavaScript 处理表单，182-183
    -   在 Web 服务器上处理输入，183-184
    -   请求用户输入，181-182
    -   使用 onsubmit 提交表单，195-197

## Index

-   Fortran，64
-   正斜杠（/）
    -   在 HTML 中，143
    -   在正则表达式中，87，89
-   使框架边框不可见，235
-   框架大小值
    -   绝对大小，228-230
    -   相对大小，229-230
    -   设置，227-230
-   frames 数组，237，253
-   框架（浏览器），223-241
    -   绝对大小，228-230
    -   通过名称访问，237
    -   在不同域中访问，239
    -   使用 JavaScript 访问，236-237
    -   为框架命名，235
    -   框架的优点，224
    -   表示框架是否已加载的布尔变量，239-240
    -   与不支持框架的浏览器，226-227
    -   从框架调用 JavaScript 函数，235-238
    -   框架之间的级联效应，239
    -   框架与 CSS，224
    -   定义，224
    -   定义和命名框架，233-235
    -   水平框架，230-231
    -   限制框架数量，228
    -   框架的问题，224
    -   相对大小，229-230
    -   框架之间的同步，239-241
    -   测试框架是否存在，241
    -   垂直框架，230-231
-   Frameset 文档的 HTML 代码，226
-   Frameset HTML，解释，146
-   Frameset 布局，226
-   Frameset，224
    -   包含行和列的 frameset，232
    -   在 HTML 中创建，225-233
    -   在 frameset 中定义和命名框架，233-235
    -   与框架大小的关系，228
    -   嵌套 frameset，233-234
-   FrontPage Explorer，10-11
-   FrontPage Server Extensions，10
-   FrontPage 2002，10
-   Function 关键字，52
-   函数参数，52，54-56
    -   作为参数的表达式，50
    -   命名参数，60-61
    -   按值传递，56
    -   无限数量的参数，61
    -   未命名参数，61
-   函数语法，52
-   函数（JavaScript），27，51-59，68，277
    -   附加到类，124
    -   附加到对象，124-125
    -   调用函数，53
    -   从框架调用函数，235-238
    -   类中的函数，68-69
    -   注释掉函数（调试时），289-290
    -   调试函数，289-290
    -   定义，27，68
    -   定义函数，52-55，119，128
    -   在类内部定义函数，128
    -   用于检测浏览器类型的函数，167
    -   空函数，54，119
    -   用于错误检查的函数，297
    -   强制函数返回硬编码值，289-290
    -   超链接调用函数，158-159
    -   用于提高组织性和可读性的函数，307
    -   特定于 2.0 版本的函数，59-61
    -   函数的语法，52
    -   测试函数，308
    -   访问前测试函数是否存在，241
    -   导致程序退出的函数，93
    -   不返回值的函数，92-93
    -   使用 onclick 事件触发的函数，320

## G

-   GetElementById() 方法，169-170，175，204，248，274，319
-   GetElementsByName() 方法，204，248
-   GetElementsByTagName() 方法，205
-   GetMonth() 函数，99
-   GoLive (Adobe)，12-13
-   GUI（图形用户界面），4

## H

-   哈希表，104-105
-   头部区域（HTML 文档），18-19，145
-   height 属性，270
-   十六进制颜色值，262
-   层级树，130
-   History 对象，257-258
-   History 对象的 go() 方法，257
-   History 对象的 length 属性，257
-   History 对象的方法，257
-   HomeSite 5，11-12
-   定义水平框架，230-231
-   HTML 注释，19，144，156



#### 如何用 JavaScript 做所有事情

HTML 文档
body 部分，145
构建，145-146
在 DOM 树中，247
head 部分，145
关键字，147-148
组成部分，18-19
标题，147
HTML 编辑器，10-13
HTML 元素
ID 属性，204
样式属性的继承，261
样式属性，261，266
样式/class/id 属性，265
用于分配样式，261-263
HTML 事件处理，215-217
HTML 事件，209，215-217
用于框架和框架集的 HTML 文件，235
HTML 表单控件，列表，187
HTML 表单，180-199
添加控件，186-195
提交时的客户端-服务器通信，184
与客户端 JavaScript，182-183
插入到网页上，184-199
onfocus/onblur/onchange 事件，188，192
onsubmit 和 onreset 事件，186
在 Web 服务器上处理输入，183-184
请求用户输入，181-182
HTML 4.01
字体样式元素，148-149
短语元素，148-149
HTML 4.01 标签，完整列表，328-330
HTML 框架，224-235
HTML（超文本标记语言），4。另见 HTML 元素；HTML 标签
基本结构，142-153
创建框架集，225-233
使用其测试 JavaScript 程序，16-19
文本格式化，148-153
用户控件，180-181
查看底层，144
HTML 标记标签。参见 HTML 标签
HTML 标签名称，小写，146
HTML 标签，142
<A HREF>，158
<noscript>，154-156
<script>，153-154，157
<style>，151
用于添加可编写脚本的对象，315
结束标签，142-143
完整列表，328-330
已弃用，145-146
结束标签，145
用于格式化页面，261-263
用于格式化文本，148-150
专有，170-171
为其设置事件处理程序，218
开始标签，145
HTML 测试工具，310
HTML 验证服务，170
HTTPS 协议，190
超链接
用于模拟提交按钮，219
用于调用 JavaScript，158-159

HTML 元素的 Id 属性，204，265
IDE（集成开发环境），7，296
IE（Microsoft Internet Explorer），8，162
ActiveX 控件，314
支持的浏览器事件，199
调用 submit() 方法，220
错误详细信息，285
错误消息框，284
Error 对象，298，301
JavaScript 在其中，5
navigator.appName 属性，165
navigator.appVersion 属性，166
Object expected 消息，286
打开和关闭错误报告，282-284
IE 6.0
文档对象，74
解释 <div> 标签，176
IE 网站，16
If 关键字，302
If 语句，31-32，170，240，297
检查格式，287
形式，32
If-else 语句，32
If-else-if 语句，33
IIS Web 服务器，142
图像翻转效果，212
图像
动态加载，274-276
插入，211
切换以产生动画，274-276
Images 数组，248
Incrementor 部分（for 循环），38
Index（数组），96，104-105
IndexOf() 方法，78
无限循环，35，38
继承，130-135
好处，132-133
网页样式属性的继承，261
Initialize() 函数，217
- Initializer 部分（for 循环），38
- 内联样式，定义，265-266
- 内联文本，265
- 输入输出功能，244
- 实例成员，135-136
  - 定义，78
  - 与静态成员的对比，78
- 实例化对象，72
- 整数数据类型，91
- 整数，取值范围，28
- 接口，132
- 互联网，隐私与，190
- 互联网搜索引擎，指定关键字，147-148
- 无效日期，测试潜在使用，311
- 无效输入，测试潜在使用，311
- IPlanet Web 服务器，14，142
- Is 运算符，51

## 索引 343

- JavaScript 控制台，283，286-287，290-291
- JavaScript 调试器，291-293
- JavaScript DOM，5，7
- JavaScript 编辑器（C Points），291
- JavaScript 环境和对象模型，244
- JavaScript 文件，加载外部，157-158
- JavaScript Lint 验证器，287
- JavaScript 1.5
  - 完整语句列表，332
  - 核心类，70
  - 创建对象，118-126
  - 系统对象列表，333
  - 错误原因，283
- JavaScript 版本历史，7
- JavaScript 模板，16-19
- JavaScript 2.0
  - 新增功能，13-14
  - 将代码分解为可管理的部分，307
  - 打断长代码行，100
  - 不支持的浏览器，15
  - 完整语句列表，332
  - 创建对象，126-137
  - 数据类型，28，59，69-71
  - 定义类，127-129
  - 增强的数组，111-112
  - 代码中的额外空格，100
  - 函数，59-61
  - 接口与，132
  - 系统对象列表，333
  - 新数据类型，91-93
  - 新运算符，51
  - 代码中的换行符，100
- JavaScript 版本，7
  - 在不同环境中，142
  - 指定版本号，164
- Javascript: 前缀（在 HREF URL 中），159
- 启用 JavaScript 的 Web 浏览器，第一个，6
- 启用 JavaScript 的网页，开发，7
- JRE（Java 运行时环境），317
- JScript（Microsoft），5-6，9
- JSP（Java 服务器页面），5
- JVM（Java 虚拟机），315，317

# J

- Java 小程序，5，315-320
- Java 编译器，316-317
- Java 语言，315
- Java SDK（软件开发工具包），317
- JavaScript（另见 JavaScript 1.5；JavaScript 2.0）
  - 添加到网页，153-154
  - 追加，159
  - 作为客户端语言，14
  - 作为脚本语言，4
  - 作为服务器端语言，14-15
  - 作为官方标准，5
  - 使用超链接调用，158-159
  - 注释，19
  - 调试，281-293
  - 为易于调试而设计，306-308
  - 使用文本编辑器开发，296
  - 开发工具，9-13
  - 以源代码形式分发，296
  - 防错，295-312
  - 用于表单控件值，200-205
  - 基础知识，25-61
  - 历史，4-7
  - 在 DOS/Windows 环境中，9
  - 在 Internet Explorer 中，5
  - 使用其管理浏览器插件，313-325
  - 起源，5
  - 与其他语言的对比，13
  - 编程术语，27
  - 快速参考，331-333
  - 错误原因，283
  - 使用 HTML 文本替换，156
  - 使用 HTML 测试，16-19
  - 错误类型，283

# K

- 按键事件触发顺序，213
- 按键事件处理程序，212-214
- 按键事件，209，212-214
- 键（索引），105
- window.event 对象的 KeyCode 属性，214
- Keydown 事件，213-214
- Keypress 事件，213
- Keyup 事件，213
- 关键字，定义，27
- HTML 文档中的关键字，147-148
- 嵌入 Media Player 9 对象，322
- Media Player 6.4，322
- 成员（类），68
- 方法，44-45
  - 添加到类，123-125
  - 附加到对象，125-126
  - 浏览器支持，169-170
  - 调用，129，137
  - 调用公共方法，137
  - 使用前检查，169-170
  - 类的方法，78，123-125
  - 使用类创建，128
  - 定义，67
  - 继承，131，134
  - 私有，73

# L

- L（长整数）后缀，71
- 标签名称，43
- 标记循环，43
- 标签（命名的代码行），42-43
- Language 属性（<script> 标签），19
- 层（在 Netscape 4 中），169，172-174
- LIFO（后进先出）顺序，102
- 错误消息中的行号，285-286
- 列表框控件（表单），189-193
- 列表，存储，96
- 字面量，定义，27
- LiveWire 服务器端语言，14
- Load 事件，215-216
- Location 对象，258
- Location 对象方法，258
- Location 对象属性，258
- 逻辑错误，283
- 长整数，71
- 打断长代码行，100
- 循环，34-43
  - 标记，43
  - 嵌套，42
  - 用途，34
- 低级数据类型，71
- Microsoft ActiveMovie 控件，321-323
- Microsoft ActiveX，314
- Microsoft ASP .NET 平台，14
- Microsoft 日历控件，324-325
- Microsoft FrontPage，10
- Microsoft IE 网站，16
- Microsoft IIS Web 服务器，142
- Microsoft JScript，5-6
- Microsoft .NET Framework，14
- Microsoft Script 调试器，293
- Microsoft Script 编辑器，291
- MIME 标准，154
- MIME 类型，154
- Modifylayer() 函数，198-199
- 模块化编程，66
- 模块，66
- 取模（%）运算符，42
- 月份，将数字转换为字符串，99
- 鼠标事件处理，211
- 鼠标事件，209
  - 列表，211
  - 跟踪，211
- Mouseout 事件，211-212
- Mouseover 事件，211-212，274
- Moveball() 函数，创建，277
- 影片，嵌入网页，321-324
- Mozilla JavaScript 调试器，292
- Mozilla 网页浏览器，8
- MSDN CSS 属性参考指南，268
- 多维数组，107-115
- 音乐，嵌入网页，321-324
- 音乐对象，使用 JavaScript 连接，322-324

# M

- 机器类型后缀，71
- JavaScript 2.0 中的机器类型，71-72
- Macromedia Dreamweaver MX，10-12，291
- Macromedia Flash 文件，142
- Macromedia Flash 插件，检查，255
- Macromedia HomeSite 5，11-12
- Mailto: 协议，185
- 主框架，224
- 手动换行符（<br>），263
- 主数组，110-111
- Math 类，78
- Math 类静态常量，列表，79
- Math 对象，78
- Math 对象静态方法，列表，79-80
- 数学函数，78
- 媒体对象，使用 JavaScript 连接，322-324
- Media Player（Windows），321

# N

- 命名关键字，60-61
- 命名参数，60-61
- NaN（非数字）常量，71



# O

Navigator 4.0 (Communicator)，8
Navigator 对象，164，254-256
appName 属性，165
appVersion 属性，166，168-169
属性，164-169，255-256
userAgent 属性，166，168，175
Navigator 6，8
Navigator 2.0 浏览器，5-6
嵌套框架集，创建，233-234
嵌套循环，42
NetObjects Fusion 7，13
Netscape Browser Central，16
Netscape Communications，5
Netscape Enterprise Server，14
Netscape 4 网页浏览器
其中的层，169，172-174
其中的样式表，273
Netscape Navigator 4.0 (Communicator)，8
Netscape Navigator 6，8
Netscape Navigator 2.0 浏览器，5-6
Netscape 插件 API，314
Netscape 7.0，解释 `<div>` 标签，177
Netscape 网页浏览器
错误字符串，298
navigator.appName 属性，165
navigator.appVersion 属性，166
原始 DOM，245
catch 子句的语法，302
Netscape/iPlanet Web 服务器，142
Never 数据类型，93
New 关键字/运算符，69，72，78，97，128-129，301
节点（数据层次结构），246
不间断空格（`&nbsp`），263
非标准编码实践，170
Null 数据类型，93
Number 数据类型，91
Number 原始类型，91
数字，将字符串转换为，82-84
数值字面量，赋值给变量，71
数值到字符串的转换，99
数字索引，带数字索引的数组，106

对象数组，113
Object 数据类型，92
使用 new 运算符实例化对象，72
对象字面量，122-123
对象方法。*参见* Methods
对象模型，JavaScript 环境与对象模型，244
对象属性。*参见* Properties
面向对象编程，66-69，118
对象，44，64-69
使用 [] 运算符访问，73
将函数附加到对象，124-125
将属性和方法附加到对象，125-126
与代码重用，308
创建对象，117-137
创建为对象字面量，122
在 JavaScript 1.x 中创建，118-126
在 JavaScript 2.0 中创建，126-137
从一个构造函数创建，121
使用 new 关键字创建，129
使用对象字面量创建，123
定义，67
扩展，125-126
设置默认，44-46
测试，308

正式弃用，解释，145
Onblur 事件（表单），188，192
Onchange 事件（表单），188，192
Onclick 事件（按钮），220，320
一维数组，107
Onfocus 事件（表单），188，192
Onload 事件处理程序，215-217，226，276-277
Onmouseout `<img>` 标签属性，218
Onmouseover `<img>` 标签属性，218
Onmouseover 事件处理程序，211
Onpaste 事件处理程序，221
Onpaste 事件（文本框控件），221
Onreset 事件（表单），186
Onsubmit 事件（表单），186，195-197
Onunload 事件处理程序，226
操作数，定义，27
操作系统
显示设置，256-257
在所有操作系统上进行测试，312
运算符，27，50-51
JavaScript 2.0 的新运算符，51
运算符类型，50
外部框架集，233

# P

并行数组，109-110
括号中的参数列表，52
参数（函数的），52，54-56
表达式作为参数，50
命名参数，60-61
按值传递，56
无限数量，61
未命名参数，61
父类，定义，130
父对象（window），253
父子关系，130
括号 ()，用于函数参数列表，52，54
ParseFloat() 函数，82，84
ParseInt() 函数，82-83
显示星号的密码框，190
模式匹配（正则表达式），86-87
PDF 文档（Adobe Acrobat），12，142
PDF（便携式文档格式），12，142
Perl 语言，9
短语元素（HTML 4.01），148-149
插件
定义，314
解释，254
插件 URL 列表，314
使用 JavaScript 管理插件，313-325
Plugins 数组，254
多态性，92，133
弹出式对话框，类型，20
弹出式网络广告，254
弹出窗口，254-255
位置属性（CSS），使用位置属性进行动画，276-277
在网页上定位元素，268-270
井号（#）
用于 `<form>` action 属性，186
用于 RGB 值，262
实用浏览器嗅探脚本，168
原始类型，91
隐私与互联网，190
私有类成员，136
Private 关键字，136
私有属性和方法，73
过程式编程，65-66，308
过程，65
程序错误，捕获，48-49
程序流程，29-30
编程方法，65-68，306
编程术语，27
属性，44，67
访问属性，120，128
使用 [] 运算符访问，73
向类添加属性，123-125
将属性附加到对象，125-126
类的属性，68-69，78
通过赋值创建属性，126
继承的属性，131，134
私有属性，73，136
属性名称（JavaScript）
属性名称的大小写敏感性，122
与 CSS 属性名称对比，272-273
专有事件，221
避免专有扩展，273
专有标记标签，170-171
Prototype 属性，123
原型设计，123
公共类成员，136
Public 关键字，136
调用公共方法，137
按钮控件（表单），193-194，220，320，323

# Q

问号（?），在表达式匹配中，34
队列，102

# R

不动产，256
RegExp 对象
使用 RegExp 对象创建模式，89-90
RegExp 对象的方法，89
正则表达式语言，87-88
正则表达式字面量，89
正则表达式，86-90
模式匹配，86-87
特殊标记，88-89
正则表达式语法，88-89
正则表达式的用途，87
Reset 事件，215
Resize 事件，216
剩余参数 (...)，61
重新抛出异常，305
Return 语句，53，58-59
返回值（函数），58，297
RGB（红绿蓝）值，262
Rows 属性（`<frameset>` 标签），227-232
规则选择器，266-267
运行时错误，283

# S

Screen 对象，256
Screen 对象属性，256
屏幕大小，256
基于屏幕空间调整组件大小，256
脚本，定义，4
脚本调试器（Microsoft），293
在 IE 中禁用脚本调试，284
脚本编辑器（Microsoft），291
可脚本化对象，插入到网页中，315
脚本语言，14
滚动条（垂直），带垂直滚动条的多行文本框，191
Scroll 事件，216
多项选择的滚动弹出窗口，190
滚动列表框控件，189，191
使用正则表达式进行查找和替换，86-90
安全性，私有类成员用于安全性，136
Select 事件，216
Self 对象（window），253
分号（;）
用于追加 JavaScript 命令，159
语句结束，100
服务器，定义，8
创建基于服务器的 Web 应用程序，8-9
服务器端 JavaScript（SSJS），8，14-15，142
SetTimeout() 函数，251
显示详细信息按钮（IE 错误消息框），284
兄弟节点，246
已签名脚本，8
单引号（'），用于字符串字面量，74
斜杠和星号（/*），用于块注释，44
特殊数据类型，92-93
方括号（[]）运算符，73，96，104-106
Src 属性
`<embed>` 标签的，321
`<frame>` 标签的，234
`<img>` 标签的，211
`<script>` 标签的，157
SSL（安全套接层），190
标准。参见 W3C
起始标签（HTML），142
语句块，32
语句，27，30-49
语句类别，30
JavaScript 1.5 和 2.0 的语句列表，332
静态（类）成员，68，135
定义，78
与实例成员对比，78
Static 关键字，135
创建 StaticArray，112-113
StaticArray 类，112-113
状态栏（浏览器），253
存储数据，26-29
存储列表，96
严格 HTML，解释，146
严格模式（错误检查），283
String 类构造函数，76
String 数据类型，76，91
字符串字面量，74-75
定义，74
throw 语句传递字符串字面量，305-306
String 对象
创建 String 对象，73-78
使用字符串数据类型创建，76
使用字符串字面量创建，74-75
indexOf() 方法，169
length 属性，75
方法，76-77
字符串，27
将字符串转换为数字，82-84
将数字转换为字符串，99
含无效字符的字符串，85
将字符串用作数组索引，104
有效字符串，73
创建字符串的方式，74
HTML 元素的 style 属性，265-266，268

样式表 @import 命令，267
样式表规则，266
样式表，150-153，261
样式表的优势，264
创建样式表，276
定义嵌入式样式表，266-267
与框架对比，224
Netscape 4 网页浏览器中的样式表，273
样式，260
使用 HTML 元素分配样式，261-263
样式的浏览器平台问题，272-273
一次更改所有页面的样式，267
导入外部样式，267
使用 JavaScript 修改样式，270-272
样式的优先级，267
文本框的样式，271
使用样式表设置样式，264-267
提交按钮，193，195-196
禁用提交按钮，205
模拟提交按钮的超链接，219
Submit 事件，215
Submit() 方法（`<form>` 对象），219-220
Sun Microsystems，14，317
晴天综合症，311
Switch 关键字，33
Switch 语句，33-34
语法错误，283
系统类，63-93。参见 Classes
系统错误，46，48
系统对象（参见 对象）
JavaScript 1.5 中的系统对象，333
JavaScript 2.0 中的系统对象，333
系统测试，312

# T

标签（HTML）。参见 HTML 标签
模板（JavaScript），16-19
body 部分，19
在记事本中创建，16-17
创建测试框架，309-311
测试你的代码，282，309-312
文本
文本动画，277
标记动态文本，265
准备将文本发送到 Web 服务器，84-85
将文本写入浏览器窗口，21-22
文本区域控件，193
文本块
解释，265
命名文本块，269
文本框控件事件，捕获，197



## 348 如何用 JavaScript 做所有事情

文本框控件（表单），186-189
- 属性，187-188
- onpaste 事件，221
- 样式，271

文本编辑器，9-10

## 文本格式化
- 对应的 HTML 元素，148-150
- 使用样式表，150-153

This 对象，119

三维数组，107

Throw 语句，48-49、297、304-306

时间，保持正确更新，250

计时器事件，用于实现动画效果，274

Today 变量，64

Top 对象（window），253

过渡型 HTML，说明，146

触发事件，219-220

Try 子句，297-304

Try-catch 语句 finally 子句，302-304

Try-catch 语句，47-48、297-304

二维数组，107-110、112

Type 属性（`<script>` 标签），19

## 变量，27、67
- 将数字字面量赋给变量，71
- 在类中，68
- 定义为机器类型，71
- 定义，27-29、55
- 程序定义的变量数量，96
- 作用域，56-58
- 在访问前测试其存在性，241

VBScript（Visual Basic 脚本），5、9

不同环境中的 JavaScript 版本，142

垂直框架，定义，230-231

垂直滚动条，带垂直滚动条的多行文本框，191

Visibility 属性，270

Visual Studio .NET，14

Void 数据类型，92-93

## U

UL（ulong）后缀，71

未处理的异常，303

Unicode 字符集，214

Unload 事件，215

未命名参数，61

无符号长整型（ulong/UL），71

非结构化编程，65、307

Update_time() 函数，250-251

URL 格式，84

URL 字符串中的字符，84

URL（统一资源定位符），84

美国邮政局地址变更表，181

用户控件，在 HTML 中，180-181

用户 ID 和密码，190

用户信息，收集与处理，180

用户输入，使用 HTML 表单请求，181

用户界面事件处理，209-210

用户友好消息，48

用户输入提示框，21

与用户通信，19-22

## V

有效的 JavaScript 代码，287

验证解析器（验证器），287

值，定义，27

Var 关键字，27

变量作用域，56-58

## W

网页广告（弹出窗口），254

网页浏览器地址栏，258

网页浏览器兼容性问题，162-170
- 代码的兼容性，171-177
- DHTML 的兼容性，171
- 事件的兼容性，220-221
- 样式的兼容性，272-273

网页浏览器 DOM，162

网页浏览器错误消息，解读，282

## 网页浏览器事件
- 说明，158
- 处理，207-221
- IE 支持的事件，199

网页浏览器框架。参见 Frames（浏览器）

网页浏览器历史列表，257-258

网页浏览器市场功能竞争，170

网页浏览器插件，管理，313-325

网页浏览器刷新，258

网页浏览器嗅探代码，221

网页浏览器软件属性，254-256

网页浏览器状态栏，253

网页浏览器计时器，251

网页浏览器类型，检测，164-169、256

网页浏览器使用统计，163

网页浏览器版本
- 检测，164
- 了解所需的最低版本，15

网页浏览器窗口，252-254、256-257

## 网页浏览器
- 在其上检查代码，312
- 检测，164-169、174、256
- 其 DOM，14
- 首个支持 JavaScript 的浏览器，6
- 获取用于测试代码的浏览器，312
- 与之交互，243-258
- 不支持框架的浏览器，226-227
- 不支持脚本的浏览器，154-156
- 重定向到新网页，258
- 对外部插件的依赖，315
- 发送回上一页，257
- 在所有浏览器上测试， ArithmeticError, 312
- 使用最新版本，163
- 网络冲浪者使用的浏览器，162-163、169

网页表单。参见 Forms（web）

## 网页
- 向其添加 JavaScript，153-154
- 在其上插入 HTML 表单，184-199
- 支持 JavaScript 的网页，7
- 在其上定位元素，268-270

## 网页内容
- 动态修改，249-251
- 操作，248-252
- 移动以实现动画，276-278

## 网页元素
- 使其不可见，270
- 定位，268-270
- 调整大小，270

网页样式。参见 CSS；样式表；样式

## Web 服务器
- 准备要发送的文本，84-85
- 在其上处理表单输入，183-184

作为 Web 服务器编程语言的 JavaScript，14

网站框架，235

Web 标准。参见 W3C

网络冲浪者，使用的浏览器，162-163、169

Website Pros，13

While 循环，35-36、287

While 语句，检查其格式，287

## Window 对象，252-253
- 方法，254
- open() 方法，254
- resize() 方法，257
- status 属性，253
- 其底层 DOM 对象，253

Window 对象（JavaScript），236

window.event keyCode 属性，214

Windows AVI 文件，321

Windows 环境中的 JavaScript，9

Windows Media Player，321-322

Windows 脚本，9

With 语句，44-46

WSH（Windows 脚本宿主），9

## W3C（万维网联盟），8、170
- CSS Level 1 标准，261
- CSS 标准，150、261
- CSS 验证服务，273
- 已弃用的 HTML 标签，145-146
- DOM Level 2 事件规范，208
- DOM 标准，8、244
- HTML 验证服务，170
- XHTML 标准，144

XHTML，144、146、235

XML 文档，寻址其部分，247

XML（可扩展标记语言），144

XPath，用途，247

零长度数组，97

ZVON.org 网站，225

## 国际联系信息

### 澳大利亚
McGraw-Hill Book Company Australia Pty. Ltd.
电话 +61-2-9900-1800
传真 +61-2-9878-8881
http://www.mcgraw-hill.com.au
books-it_sydney@mcgraw-hill.com

### 加拿大
McGraw-Hill Ryerson Ltd.
电话 +905-430-5000
传真 +905-430-5020
http://www.mcgraw-hill.ca

### 希腊、中东及非洲
（南非除外）
McGraw-Hill Hellas
电话 +30-210-6560-990
电话 +30-210-6560-993
电话 +30-210-6560-994
传真 +30-210-6545-525

### 墨西哥（同时服务拉丁美洲）
McGraw-Hill Interamericana Editores S.A. de C.V.
电话 +525-117-1583
传真 +525-117-1589
http://www.mcgraw-hill.com.mx
fernando_castellanos@mcgraw-hill.com

### 新加坡（服务亚洲）
McGraw-Hill Book Company
电话 +65-863-1580
传真 +65-862-3354
http://www.mcgraw-hill.com.sg
mghasia@mcgraw-hill.com

### 南非
McGraw-Hill South Africa
电话 +27-11-622-7512
传真 +27-11-622-9045
robyn_swanepoel@mcgraw-hill.com

### 西班牙
McGraw-Hill/Interamericana de España, S.A.U.
电话 +34-91-180-3000
传真 +34-91-372-8513
http://www.mcgraw-hill.es
professional@mcgraw-hill.es

### 英国、北欧、东欧及中欧
McGraw-Hill Education Europe
电话 +44-1-628-502500
传真 +44-1-628-770224
http://www.mcgraw-hill.co.uk
computing_neurope@mcgraw-hill.com

### 所有其他咨询请联系：
Osborne/McGraw-Hill
电话 +1-510-549-6600
传真 +1-510-883-7600
http://www.osborne.com
omg_international@mcgraw-hill.com

## JavaScript 文档对象模型

### DOM 对象

| 对象 | 说明 |
| --- | --- |
| window | 浏览器窗口的属性和方法 |
| document | 当前 HTML 文档的属性和方法 |
| history | 浏览器历史列表的方法 |
| location | 浏览器 URL 的属性和方法 |
| screen | 用户屏幕的属性 |
| navigator | 浏览器应用程序的属性 |

### DOM 方法

| 方法 | 作用 |
| --- | --- |
| `alert()` | 向用户显示一个小对话框 |
| `confirm()` | 向用户显示一个小的确认消息框 |
| `prompt()` | 显示一个提示用户输入的小对话框 |
| `window.open()` | 打开一个新的浏览器窗口 |
| `document.write()` | 将一些文本写入屏幕 |
| `history.back()` | 将浏览器发送到历史列表中的上一项；等价于后退按钮 |
| `window.focus()` | 使浏览器窗口移到前台 |

## 如何用 JavaScript 做*所有事情*

通过这本简单易懂的 JavaScript 指南，为任何网站带来交互性。作者 Scott Duffy 通过提供易于掌握的教学内容和理论知识，结合实用示例和大量即用型代码，消除了使用编程语言的恐惧。通过探索语句、变量和函数——任何程序的三个基本构建块——来学习编写程序。将 JavaScript 用作网页浏览器演示的幕后导演。创建基本和高级的 JavaScript 应用程序——此外，修改现有脚本以满足您的需求——所有这些都可以借助这本优秀的资源来实现。

*   使用语句、变量和函数编写自己的程序
*   了解该语言的历史以及它能为您做什么
*   为您的网站启用运动和交互性
*   确定哪个版本的 JavaScript 适合您
*   使用内置类存储日期、数字等
*   创建在每个浏览器中都能工作的脚本
*   理解表达式的基础知识，并将代码组织成函数
*   实现鼠标悬停时文本或图形的变化
*   自动更改网页上的格式化日期
*   使用内置或脚本类无缝协调对象和事件

## 关于作者：

Scott Duffy，MCSD、SCJP，拥有超过 10 年的业务应用程序开发经验。自 1996 年以来，他也一直从事专业 Web 开发工作。
