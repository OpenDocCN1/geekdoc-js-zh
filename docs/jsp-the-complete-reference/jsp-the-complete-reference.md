# JSP 完全参考指南

# JSP：完全参考手册
## 关于作者...

# 献给玛丽

此页有意留白。



# 前言

新技术的第一波浪潮往往被其产生的期望所超越。而乘着第二波浪潮的人则受益于前人的经验，真正的价值得以显现。Java 的发展历程正是如此。客户端浏览器应用程序（applet）在三个领域遇到了限制：

- 浏览器的兼容性问题
- 过度的安全限制
- 因下载时间长而导致的性能问题

服务器端 Java 的出现改变了这一切。Java Servlets 和 JavaServer Pages (JSP) 提供了一种安全、强大且平台无关的技术，将 Java 的强大功能带入电子商务和企业 Web 计算领域。正因如此，人们对 JSP 的兴趣日益浓厚，对 JSP 技能的需求高涨。几乎所有《财富》500 强公司现在拥有或即将部署服务器端 Java 应用程序。

本书的目的是为 JSP 技术提供一份完整的参考，从 Web 编程环境和 JSP 元素开始，然后更深入地探讨高级主题。

# 本书组织结构

本书由五部分组成，从高层概述开始，逐步深入探讨各个主题。

## 第一部分，“Web 编程环境”

本书的开篇部分介绍了 Web 作为编程环境，并介绍了 servlet、JSP 和 Web 网络协议。

### 第 1 章，“Web 市场”

第一章探讨了 Web 作为一个思想、产品、服务和应用的市场——我们如何走到今天，以及什么将驱动未来的方向。它介绍了 Java 并解释了它在网络计算模型中的重要性。

### 第 2 章，“Web 应用程序的演变”

第 2 章描述了随着 Web 的成熟，应用程序编程模型是如何演变的，以及每个阶段的经验如何驱动了下一阶段的需求。

### 第 3 章，“超文本传输协议 (HTTP) 概述”

本章介绍了 Web 客户端/服务器模型的基础语言——超文本传输协议 (HTTP)。它阐述了理解 Web 编程环境所需的基本概念。

### 第 4 章，“Servlet 简介”

本概述章节解释了 JSP 与 servlet 之间的紧密联系。概述并演示了它们共享的基本特性。

### 第 5 章，“JSP 概述”

第 5 章提供了对 JavaServer Pages (JSP) 作为服务器端脚本环境的概述，描述了 servlet 引擎，并给出了几个教程示例。这里只涵盖基础知识——第二部分将深入探讨该主题。

## 第二部分，“JSP 元素”

本部分涉及 JSP 的语法和语义，使读者掌握创建可工作代码所需的技能。主题包括基本语法、脚本、表达式、声明、包含文件、请求转发和指定页面行为。自定义标签的开发将得到详细探讨。

### 第 6 章，“JSP 语法和语义”

本章涵盖了 JavaServer Pages 的基本语法，描述了它们如何将 HTML 模板和 Java 代码融合在一起。

### 第 7 章，“表达式和脚本”

本章描述了将 Java 代码片段合并到 JavaServer Page 中的基本模型。它涵盖了合法和非法的用法，并描述了翻译器如何将这些代码片段组合成一个可工作的 servlet。

### 第 8 章，“声明”

本章考虑了声明以及在 JSP 中使用 Java 代码的高级用法。它涵盖了声明的三种最常见用法，并提供了所有三种用法的示例。

### 第 9 章，“请求分发”

本章讨论了 HTTP 请求如何由多个服务器端组件处理。它描述了包含其他文件的两种方法，并解释了为什么一种方法可能比另一种更可取。它涵盖了如何使用 `<jsp:forward>` 操作将请求传递给另一个 JSP 进行处理。

### 第 10 章，“页面指令”

第 10 章详细描述了如何使用页面指令来指定 JavaServer Page 的属性和行为。为每个属性提供了完整的示例。

### 第 11 章，“JSP 标签扩展”

本章考虑了 JSP 架构的扩展，特别是定义自定义标签的能力。

## 第三部分，“JSP 实战”

本部分探讨了 JSP 如何与 JDBC、JavaBeans 和 Java 环境的其他主要组件协同工作。包括对调试和部署的详细讲解。

### 第 12 章，“HTML 表单”

第 12 章描述了 HTML 表单，它是 servlet 和 JavaServer Pages 最常见的客户端。

### 第 13 章，“数据库访问”

大多数重要的 JSP 页面都需要访问数据库。本章全面介绍了 Java 数据库连接性，以及它如何在基于 Web 的应用程序中使用。

### 第 14 章，“会话和线程管理”

HTTP 是一种无状态协议，但 JavaServer Pages 可以使用 HTTP 会话来克服这一限制。本章探讨了相关问题，并描述了开发者可用的技术。

### 第 15 章，“JSP 和 JavaBeans”

本章描述了 JavaBeans，并展示了它们如何与 JavaServer Pages 结合使用，将业务逻辑隔离为可重用的组件。



## 第16章，“JSP与XML”

XML正逐渐成为结构化数据存储和交换的通用语言。本章将探讨JSP如何利用XML进行数据的输入与输出。

## 第17章，“JSP测试与调试”

调试技术在编程教程中常被忽略，但却是不可或缺的知识。JavaServerPages面临着其自身的挑战。本章概述了一个可应用的基本方法论以及可用的工具。

## 第18章，“部署Web应用”

第18章描述了如何将JSP页面从开发环境迁移到生产Web环境。

## 第19章，“案例研究：产品支持中心”

本章将全书讨论过的元素整合到一个基于Web的系统中，用于管理一个技术支持中心。

## 第四部分，“JSP与其他Web组件”

第四部分探讨了JavaServerPages在更广泛的背景下使用的情况——它们如何与servlet、applet、Perl脚本、FTP、CGI、ASP以及其他服务器端代理进行通信。

## 第20章，“与其他客户端通信”

尽管Web浏览器中的HTML表单是最常见的客户端环境，但JSP页面可用于支持任何能理解HTTP协议的客户端。第20章展示了如何实现这一点。

## 第21章，“与其他服务器通信”

本章在上一章的基础上进一步发展，描述了JSP组件如何访问其他协议。并讨论了JavaMail API。

## 第五部分，“附录”

本书以三个附录结尾，分别涵盖了Servlet API、JSP API和HTTP参考。

## The Lyric Note（“抒情笔记”音乐公司）

本书的大部分示例都设定在一个假想的公司——The Lyric Note（“抒情笔记”）的背景中。这是一家基于互联网的音乐公司，销售书籍、礼品、乐谱、音乐软件和乐器。我为其配置了五十名员工，分布在十一个部门，并拥有一个庞大的产品目录。

## Servlet与JSP API级别

在撰写本书时，Servlet和JSP API的主要级别分别为2.2和1.1。虽然2.3和1.2版本的公开草案已经发布，但它们尚未被正式定为标准，且可能发生变化。这对于试图呈现及时材料的作者来说是一个问题。是讨论当前人们使用的Servlet引擎中实际实现的内容更重要，还是探讨那些尚无人能实际运行的新版本更重要？我试图两者兼顾。本书的主体内容基于Servlet 2.2和JSP 1.1，而附录则列出了2.3和1.2规范最新公开草案中的API。

## 更新

勘误、示例和更新内容可在我的网站上找到：http://www.philhanna.com。

## 致谢

没有众多人士的协作与支持，本书不可能完成。我首先要感谢Osborne/McGraw-Hill的策划编辑Rebekah Young，她构思了这个项目，并与我共同确定其范围和内容。同时也要感谢Mark Karmendy，他运用其卓越的技能确保了一切顺利整合，还要感谢Marcia Baker的细致文字编辑。此外，感谢Osborne的制作团队出色的版面设计工作。我的技术编辑Karl Moss提供了无价的帮助和宝贵的建议。

我感谢Brian Flagg为产品支持中心案例研究提供的建议和技术援助，感谢Tina Armstrong对其模型-视图-控制器方法的反馈。我感谢古典档案馆有限责任公司（Classical Archives, LLC）的首席执行官Pierre R. Schwob允许我将作曲家参考资料纳入The Lyric Note的产品目录。Angela Allen和David Biesack对自定义标签材料提供了有益的评论。非常感谢Jack Keller在强化结构完整性方面的技巧，以及Chris Bailey这位极具创造力的思想家和创意源泉。

我非常感谢SAS Institute的Alan Eaton和Keith Collins的支持，是他们使我能够承担这个项目。

最重要的是，我要感谢我的妻子Mary、我的孩子们Eleanor和John，以及我的岳母Ann Jordan，感谢他们的支持、鼓励、善意和耐心。

## 第1章

### Web市场

在罗马市中心，台伯河畔，坐落着罗马广场。两千年前，*Forum Romanum*（罗马广场）是罗马世界的权力中心。它是举行凯旋仪式的地方，是普通商品和服务进行交换的地方，也是新闻和观点自由交流的地方（“forum”一词的常见含义即源于此）。尽管部分由石头、砖块和砂浆建成，但它的扩张得益于一项新技术：混凝土。

如今，互联网是全球性的电子市场。无论是对于商业企业还是个人消费者，互联网正成为商品、服务和信息交换的主导中心。与罗马广场一样，互联网的增长得益于技术的进步——新的计算机语言、网络标准的广泛接受以及廉价的硬件。

本书讲的是JavaServerPages，这是一项使能技术，它将Web浏览器、Web服务器和数据库系统整合在一起，使得应用程序易于开发、访问和部署。Java技术在连接性、可靠性、可扩展性和安全性方面已被证明是无与伦比的。这项技术比其他任何技术都更有望推动网络计算模式，并进而推动全球电子市场。

没有人能准确预测未来的趋势。即使是*Forum Romanum*（罗马广场）最终也被杂草覆盖，变成了*il Campo Vaccino*——“牧牛场”。但可以肯定地说，一个企业成功交换产品、服务、信息和思想的程度，将继续取决于其进入市场的程度。

## 第2章

### Web应用程序的演变

万维网最显著的特点之一是，它最初并非被构想为一个应用环境。然而，如今，Web应用程序已成为大多数互联网使用——尤其是电子商务使用——的支柱。本章简要追溯了万维网、Web应用程序及相关技术的起源，为本书其余部分更详细的技术探讨设定了背景。

## Web的诞生

万维网及其相关的*超文本传输协议（HTTP）*起源于1990年欧洲核子研究中心（CERN）的工作。Tim Berners-Lee将HTTP开发为用于分发文档的网络协议，并编写了第一个Web浏览器。该系统在1991年和1992年被CERN及其他高能物理实验室和大学使用，并逐渐普及。1993年，Mosaic浏览器的出现导致了商业Web使用的激增。五年内，全球有超过65万Web服务器在使用，用户数量更是不计其数。

## Web编程模型的发展

将Web用作应用环境的想法是随着时间的推移而发展的，技术的每个阶段都为新的想法提供了跳板。第一个操作模型是Web服务器根据请求简单地提供文档。在这种环境下，内容不会改变，除非人类作者提供了文档的新版本。图2-1说明了客户端/服务器的交互。

![](img/7a2f73369bb140583c7288b73456addb_32_0.png)



# 第2章：Web应用的演进

HTTP是一种简单的请求/响应协议，其中Web浏览器请求一个文档（通常使用GET命令），Web服务器则以HTML数据流的形式返回该文档，并附带一些描述性头部。第3章将更详细地探讨HTTP。

很快变得明显的是，如果人类可以修改Web服务器处理的文档，那么像Perl脚本这样的文本处理程序也可以。Web浏览器对此并无察觉，因为HTTP请求的结果仍然是一个HTML数据流。此外，浏览器可以发送的不止是一个请求——它还可以通过将参数嵌入URL或随请求发送数据流来传递参数。这表明HTTP请求可以被解释为数据库查询，而查询结果可以用来动态构建HTML文档。随着NCSA HTTPd Web服务器的发展，出现了一个新的规范，称为*通用网关接口（CGI）*。

CGI程序由Web服务器调用，以响应某些类型的请求，通常是针对特定目录中的文档或具有特定扩展名的文件名（例如*.cgi*）的请求。请求参数作为键/值对传递，请求头作为环境变量传递。程序读取这些参数和头部，执行手头的应用任务（通常通过访问数据库来完成），然后生成HTTP响应。响应被发送回请求的Web浏览器，就像一个普通的静态文档一样。图2-2说明了这一流程。

![](img/7a2f73369bb140583c7288b73456addb_33_0.png)

CGI很方便，但它有一个很大的缺点。通常，CGI为每个HTTP请求创建一个新进程¹。当流量较低时这不是问题，但当流量增加时，这会产生大量开销。鉴于这种情况，CGI通常扩展性不佳。

随着1997年Java Servlet API的发布，以及随后的JavaServer Pages（JSP）API的快速推出，一个重大改进出现了。这些相关技术将Java的全部功能带到了Web服务器，包括数据库连接、网络访问和多线程操作，特别是不同的进程模型。Servlet和JSP页面从一个保持在内存中的单实例运行，并使用多个线程同时服务请求。如图2-3所示，Servlet和JSP页面可以利用完整的*Java 2企业版（J2EE）*环境来构建复杂、健壮的应用程序。

¹ 存在对此的改进，例如FastCGI，它从一个持久进程处理所有请求。

## 从客户端解决方案到服务器端解决方案的转变

随着Web的成熟，Web应用模型也在演进，每个阶段的经验都推动了下一阶段的需求。以applet形式出现的第一波客户端Java应用非常受欢迎，但随着现实问题的出现，也带来了一些失望。浏览器之间存在大量不兼容性，通过慢速调制解调器进行长时间下载，以及限制applet实用性的安全限制。因此，applet开发放缓，而服务器端Java已成为最大的增长领域。

服务器端Java没有applet环境的任何限制。不会出现浏览器不一致的问题，因为浏览器不需要托管Java虚拟机。浏览器只需渲染HTML，即使是最早的浏览器也能做得很好。此外，不涉及客户端设置，也不需要下载大型类文件。同样，安全考虑仅限于Web服务器已经处理的那些，这通常是在具有适当控制的封闭环境中进行的。

JSP已被证明是一项成功的服务器端技术，也是开发Web应用程序的优秀基础。本书的剩余部分将深入探讨JSP，以证明其成功的原因。

² 许多观察者认为客户端Java即将卷土重来。Java插件消除了浏览器不一致性，并允许使用Swing组件。此外，高速互联网连接使得下载考虑变得越来越不重要。

# 第3章：超文本传输协议（HTTP）概述

## 什么是HTTP？

*超文本标记语言（HTML）*是用于描述Web文档内部结构的语言，而*超文本传输协议（HTTP）*是用于描述这些文档如何在互联网上传输的语言。理解Web编程的关键在于理解这个协议及其运行环境。

## 一种在互联网上请求文档的语言

HTTP规定了浏览器发出请求和服务器提供响应的规则。这套规则，或称*协议*，包括以下方式：

- 按名称请求文档
- 协商数据格式
- 确定用户身份
- 决定如何处理过时的资源
- 指示请求的结果

以及其他有用的功能。HTTP由一组以普通ASCII文本行编写的命令组成。当您使用Web浏览器时，您并不直接输入HTTP命令。相反，当您输入URL或点击超链接时，浏览器会将您的操作转换为HTTP命令，从URL指定的服务器请求文档。Web服务器找到该文档并将其发送回浏览器，在浏览器中连同其关联的图形和其他超链接一起显示。

## HTTP规范

互联网标准通常由*互联网工程任务组（IETF）*发布的*请求意见书（RFC）*指定。这些RFC被互联网研究和开发社区广泛接受。因为它们是标准文件，所以倾向于使用正式语言编写，就像法律文件一样。这使得它们不适合作为教程，但作为参考却非常有价值。RFC有编号，一旦发布就不会更改。如果标准更新，会发布新的RFC。作为标准，RFC在互联网上广泛可用。一个优秀的、可读的在线来源是Brent Baccala的《Connected: An Internet Encyclopedia (http://www.freesoft.org/CIE)》，它维护了大多数RFC的HTML版本并提供全文搜索引擎。

有几个RFC涉及HTTP：

- RFC 1945：HTTP版本1.0的描述
- RFC 2068：版本1.1的初始描述
- RFC 2616：1.1规范的更新版本

除非另有说明，本书使用RFC 2616中记录的HTTP 1.1标准。

## HTTP请求模型

该规范将HTTP描述为一种无状态的请求/响应协议，其基本操作如下：

1. 客户端应用程序（如Web浏览器）打开一个到Web服务器HTTP端口（默认为80）的套接字。
2. 通过该连接，客户端写入一个ASCII文本请求行，后跟零个或多个HTTP头、一个空行以及伴随请求的任何数据。
3. Web服务器解析请求并定位指定的资源。
4. 服务器将资源的一个副本写入套接字，客户端读取该副本。
5. 服务器关闭连接。

图3-1说明了这一基本操作。

一个关键考虑是这个模型是*无状态的*。这意味着在处理请求时，Web服务器不会记住来自同一客户端的任何先前请求的信息。该协议只是一个请求（“请给我这个文档”）和一个响应（“好的，给你”）。显然，这对应用程序编程施加了限制，

![](img/7a2f73369bb140583c7288b73456addb_39_0.png)



## 14 JSP：完全参考手册

通常需要大量来回的对话，以及必须初始化并维护其状态的复杂对象。

解决这个问题的方法是让服务器为一组客户端请求所表示的会话分配一个标识符，并让客户端记住该标识符，并在每次请求时将其提供给服务器。本章将深入探讨这种技术。

让我们更详细地审视每一步。

## 连接到 Web 服务器

Web 服务器通过监听特定的知名端口号（通常是 80 端口，但也可以使用任何可用端口）来运行。如果 Web 服务器监听不同的端口，指向该服务器的 URL 必须包含冒号和紧跟在服务器名称之后的端口号。例如，

```
http://www.mycompany.com/mypath.html
```

指向一个由运行在 www.mycompany.com 主机上默认端口 80 的 Web 服务器托管的 HTML 文档。如果服务器运行在 4311 端口，则 URL 如下所示：

```
http://www.mycompany.com:4311/mypath.html
```

为什么要使用备用端口号，特别是因为它们引入了丑陋的 URL 语法？因为这允许多个服务器在单个主机上运行。具有不同功能的实验性 Web 服务器可能需要与主服务器共存。例如，Tomcat 和 JRun servlet 引擎可以运行一个小型 HTTP 服务器来测试 servlet 和 JSP 页面。大多数 Web 服务器提供某种方式来隐藏这种替代语法，通过将 URL 映射到不同的命名空间。

客户端（如 Web 浏览器）通过打开到 Web 服务器端口的 TCP/IP 套接字，然后在套接字上打开输入和输出流来发起 HTTP 请求。用 Java 术语来说，这相当于几行代码：

```java
Socket socket = new Socket("www.mycompany.com", 80);
InputStream istream = socket.getInputStream();
OutputStream ostream = socket.getOutputStream();
```

打开套接字所需的参数是 Web 服务器主机名和端口号。服务器主机名从 URL 中提取，而端口号要么是隐式的，要么也从 URL 中提取。输出流用于向 Web 服务器发送 HTTP 命令；输入流用于读取响应。

## 发送 HTTP 请求

一旦建立套接字连接，Web 浏览器就会写入一个 HTTP 命令来请求文档。一个请求最多由四个部分组成。

第一部分是*请求行*。它由三个标记组成，以空格分隔：请求方法、请求 URI 和 HTTP 版本。以下显示了一个典型的请求行：

```
GET /mypath.html HTTP/1.0
```

在此示例中，请求方法是 `GET`，URI 是 `/mypath.html`，HTTP 版本是 `HTTP/1.0`。

HTTP 规范定义了八种可能的方法，如表 3-1 所示。在所有这些方法中，绝大多数请求使用 `GET` 或 `POST`。本书只考虑这两种方法。

请求行上的第二个标记是*请求统一资源标识符 (URI)*。这是被请求的文档或其他资源的 URI。出于所有实际目的，这对应于去掉前导 `http://` 和主机名的 URL。在 `http://www.mycompany.com/mypath.html` 的示例中，请求 URI 是 `/mypath.html`。

| 方法 | 描述 |
| :--- | :--- |
| GET | 一个简单的请求，用于检索 URI 中标识的资源。 |
| HEAD | 与 `GET` 相同，但服务器不返回请求的文档。服务器只返回状态行和头部。 |
| POST | 请求服务器接受将要写入客户端输出流的数据。 |
| PUT | 请求服务器将请求中的数据存储为指定 URI 的新内容。 |
| DELETE | 请求服务器删除 URI 中命名的资源。 |
| OPTIONS | 请求有关服务器支持哪些请求方法的信息。 |
| TRACE | 请求 Web 服务器回显 HTTP 请求及其头部。 |
| CONNECT | 一个已记录但当前未实现的方法，保留用于隧道代理。 |

表 3-1。HTTP 请求方法

行上的最后一个标记是 HTTP 版本。这表示客户端应用程序理解的 HTTP 规范的最高级别。允许的值是 HTTP/1.0 和 HTTP/1.1。

请求行之后是任何请求头。这些是键/值对，每行一对，键和值用冒号 (:) 分隔。写入最后一个请求头后，会发送一个仅由回车和换行组成的空行。这告知服务器没有更多的头部跟随。即使没有头部，也必须发送这个空行，这样服务器就不会再寻找任何头部。

请求头进一步告知服务器有关客户端的身份和能力。典型的请求头可能是：

| User-Agent | 客户端的供应商和版本 |
|---|---|
| Accept | 客户端识别的内容类型列表 |
| Content-Length | 附加到请求的数据字节数 |

请求和响应头的完整列表可以在附录 C 中找到。

对于 HTTP POST 请求，请求可能包含数据。您将在第 12 章中看到 POST 数据如何用于传输 HTML 表单字段的值。如果存在数据，常见的是同时看到 Content-Type 和 Content-Length 请求头。

## 服务器接受请求

当客户端连接到 Web 服务器的监听端口时，服务器接受连接并处理请求。在大多数情况下，它通过启动一个线程来处理请求，以便可以继续处理新的请求。处理请求的含义取决于 URI。如果 URI 代表一个静态文档，服务器打开文档文件并准备将其内容复制回客户端。如果 URI 是程序名称（如 CGI 脚本、servlet 或 JSP 页面），并且服务器配置为处理此类请求，则服务器准备调用该程序或进程。

## 服务器的 HTTP 响应

无论服务器如何处理请求，结果都是一样的——一个 HTTP 响应。与请求类似，响应最多由四个部分组成：一个状态行、零个或多个响应头、一个表示头部结束的空行，以及构成请求的数据。

状态行最多由三个标记组成：

-   HTTP 版本。正如客户端指示其能理解的最高版本一样，服务器也指示其能力。
-   响应代码。这是一个三位数的数字代码，指示请求是否成功或失败，如果失败，则说明原因。HTTP 状态码列表可以在附录 C 中找到。
-   一个可选的*响应描述*，这是响应代码的人类可读解释。

一个典型的 HTTP 响应状态行如下所示：

```
HTTP/1.0 200 OK
```

这表示根据 HTTP 规范的 1.0 级别成功检索了请求的文档。
状态行之后是响应头，以空行作为分隔符。与请求头类似，它们表示服务器的能力并标识有关响应数据的详细信息。附录 C 列出了有效的 HTTP 响应头。
响应的最后一部分是请求的数据本身，通常是 HTML 文档或图像流。数据发送完毕后，服务器关闭其端的连接。

## 示例

查看几个示例可以更清楚这一点。GET 请求的一个简单情况是当在浏览器地址栏中键入 URL 或单击超链接时发生的情况。如果您打开 URL http://www.lyricnote.com/simple.html，Web 浏览器将打开到 www.lyricnote.com 主机端口 80 的套接字连接，然后写入以下行

```
GET /simple.html HTTP/1.0
```

后跟一个空行。Web 服务器返回以下内容：

```
HTTP/1.1 200 OK
Date: Wed, 31 Jan 2001 03:55:43 GMT
Server: Apache/1.3.12 (Win32)
Content-Length: 241
Content-Type: text/html

<HTML>
<BODY>
<H3>Welcome</H3> to <b>The Lyric Note</b>,
the best Internet source for
<UL>
<LI>sheet music
<LI>musical instruments
<LI>books on musical topics
```



## 18 JSP：权威参考

```html
<LI>music software, and
<LI>musical gift items
</UL>
</BODY>
</HTML>
```

浏览器首先解析状态行，看到状态码指示请求成功。然后解析每个请求头，这些请求头告知浏览器后续有 241 字节的 HTML 内容。浏览器读取 HTML，并根据 HTML 的语法和语义进行格式化，然后在浏览器窗口中显示，如图 3-2 所示。

HTML 文档可能包含对其他资源的引用，这些资源需要在文档加载时加载。例如，图像通常使用 HTML 的 `<img>` 标签嵌入页面。JavaScript 文件或外部样式表也可能需要。Web 浏览器（而非服务器）识别这些情况，并为其他资源发出额外的请求。这一点需要强调。Web 服务器不会读取它提供的 HTML，识别出 `<img>` 标签，然后开始发送图像文件的字节。Web 服务器只是在一个操作中发回请求的资源。如果几毫秒后，浏览器请求一个图像文件，服务器会在一个单独的操作中返回它。Web 浏览器在幕后完成所有这些工作，因此用户不知道涉及多个请求。

![](img/7a2f73369bb140583c7288b73456addb_44_0.png)

**图 3-2.** 简单 HTTP 请求的结果

稍微扩展前面的例子，假设你打开 http://www.lyricnote.com/compound.html。浏览器再次打开到 www.lyricnote.com 端口 80 的 socket 连接，并请求 HTML 文档，

```
GET /compound.html HTTP/1.0
```

这导致以下响应：

```
HTTP/1.1 200 OK
Date: Tue, 30 Jan 2001 23:42:16 GMT
Server: Apache/1.3.12 (Win32)
Content-Length: 380
Content-Type: text/html

<HTML>
<HEAD>
<LINK REL="stylesheet" HREF="lyricnote.css">
</HEAD>
<BODY>
<IMG SRC="images/logo.png">
<HR COLOR="#005A9C" ALIGN="LEFT" WIDTH="500">
<H3>Welcome</H3> to <b>The Lyric Note</b>,
the best Internet source for
<UL>
<LI>sheet music
<LI>musical instruments
<LI>books on musical topics
<LI>music software, and
<LI>musical gift items
</UL>
</BODY>
</HTML>
```

当浏览器解析 HTML 时，它注意到样式表请求：

```
<LINK REL="stylesheet" HREF="lyricnote.css">
```

并发出第二个 HTTP 请求：

```
GET /lyricnote.css HTTP/1.0
```

Web 服务器检索样式表并将其返回给客户端：

```
HTTP/1.1 200 OK
Date: Tue, 30 Jan 2001 23:42:27 GMT
Server: Apache/1.3.12 (Win32)
Connection: Keep-alive, close
Content-Length: 73
Content-Type: text/plain

h3 {
    font-size: 20px;
    font-weight: bold;
    color: #005A9C;
}
```

浏览器解释样式表，并将字体大小、粗细和颜色样式应用于 `<H3>` 标签。接下来，它遇到一个图像标签

```
<IMG SRC="images/logo.png">
```

并为 logo 发出请求，

```
GET /images/logo.png HTTP/1.0
```

这导致 Web 服务器用图像数据流进行响应：

```
HTTP/1.1 200 OK
Date: Tue, 30 Jan 2001 23:42:44 GMT
Server: Apache/1.3.12 (Win32)
Connection: Keep-alive, close
Content-Length: 1280
Content-Type: text/plain

(Binary image data follows)
```

最后，浏览器渲染完成的页面，如图 3-3 所示。

![](img/7a2f73369bb140583c7288b73456addb_47_0.png)

**图 3-3.** 复合 HTTP 请求的结果

## 总结

本章介绍了 HTTP，即用于发出请求和返回响应的规则集。理解这些规则对于正确的开发和故障排除至关重要。需要理解的是 HTTP 是无状态的，这意味着 HTTP 本身不会保留从一个请求到下一个请求的知识。JSP 环境提供了强大的方法来弥补这一点。另一个关键考虑因素是浏览器和服务器都可以被功能类似的软件替换。应用程序、小程序和用其他语言编写的程序可以充当客户端，诊断工具可以扮演服务器的角色。因为它们需要做的就是提供与浏览器和 Web 服务器将使用的相同的 HTTP 请求和响应流，所以这些其他应用程序与真实的服务器是无法区分的。你将在后面的章节中利用这一能力。

此页有意留白。

# 第4章

# Servlet 入门

23

版权 2001 The McGraw-Hill Companies, Inc. 点击此处查看使用条款。

要理解 JavaServer Pages，必须理解其底层技术——Java servlets。*Servlet* 是 Java 类，通过动态生成 Web 页面来扩展 Web 服务器的功能。一个称为 *servlet 引擎* 的运行时环境管理 servlet 的加载和卸载，并与 Web 服务器协同工作，将请求定向到 servlet，并将输出发送回 Web 客户端。

自 1997 年推出以来，servlet 已成为服务器端 Java 编程的主导环境，并成为进入应用服务器的广泛使用的门户。它们提供了几个关键优势：

- **性能** 诸如 *通用网关接口（CGI）* 之类的较旧技术通常为处理每个传入请求启动一个新进程。在 Web 主要作为学术和科学研究仓库的时代，流量不是很大，这种方法运行良好。相比之下，servlet 在首次被请求时加载，并无限期地保留在内存中。servlet 引擎加载 servlet 类的单个实例，并使用可用线程池将请求分派给它。由此产生的性能提升是相当可观的。
- **简洁性** 客户端 Java 小程序在 Web 浏览器提供的虚拟机中运行。这引入了兼容性问题，增加了复杂性并限制了小程序可以提供的功能。Servlet 大大简化了这种情况，因为它们在受控服务器环境中的虚拟机中运行，并且只需要基本的 HTTP 即可与客户端通信。即使使用较旧的浏览器，也不需要特殊的客户端软件。
- **HTTP 会话** 尽管 HTTP 服务器没有内置的功能来记住来自同一客户端的先前请求的详细信息，但 Servlet API 提供了一个 `HttpSession` 类来克服这一限制。
- **访问 Java 技术** Servlet 作为 Java 应用程序，可以直接访问全套 Java 功能，例如线程、网络访问和数据库连接。

JSP 页面会自动转换为 servlet，并继承所有这些优势。

本章概述了 servlet 的工作原理。它介绍了主要的 servlet 对象及其 API。它讨论了 servlet 引擎、servlet 生命周期、servlet 线程模型以及 servlet 如何在请求之间保持持久状态。本章还包括一个带注释的 servlet 示例。

## Servlet 生命周期

与其客户端小程序类似，servlet 提供了在更大上下文中发生特定事件时被调用的方法。在此环境中编程涉及编写预定义的方法（有时称为 *回调* 方法），这些方法由管理程序根据需要调用。

例如，一个小程序提供 `init()`、`start()`、`paint()`、`stop()` 和 `destroy()` 等方法，这些方法由小程序运行时环境根据用户采取的操作进行调用。`java.applet.Applet` 基类为所有这些方法提供默认实现；你只需覆盖那些在你关注的事件中发生的方法。例如，如果你有需要创建的 GUI 组件，你会编写一个 `init()` 方法。

类似地，servlet 在由 servlet 引擎管理的请求和响应模型的上下文中运行。引擎执行以下操作：

- 在首次被请求时加载 servlet
- 调用 servlet 的 `init()` 方法
- 通过调用 servlet 的 `service()` 方法处理任意数量的请求
- 在关闭时，调用每个 servlet 的 `destroy()` 方法。

与小程序一样，有标准基类 `javax.servlet.GenericServlet` 和 `javax.servlet.http.HttpServlet` 实现了 servlet 因此，servlet 编程包括子类化其中一个类并覆盖必要的方法以完成手头的特定任务。以下各节将介绍每个生命周期方法。

## init

当 servlet 引擎收到对 servlet 的请求时，它会检查该 servlet 是否已加载。如果没有，servlet 引擎使用类加载器获取所需的特定 servlet 类，然后调用其构造函数以获取 servlet 实例。在加载 servlet 但在其处理任何请求之前，servlet 引擎调用一个初始化方法，其签名如下：

```java

```



在 `init()` 方法内部，servlet 可以执行任何必要的启动任务，例如建立数据库连接。如果发生任何导致 servlet 无法处理请求的错误，它应该抛出一个 `UnavailableException`[^1]。这样可以防止请求被定向到该 servlet。

## service

在 `init()` 方法成功完成后，servlet 便能够接受请求。默认情况下，只会创建一个 servlet 实例，servlet 引擎在每个单独的线程中将每个请求分派给该实例。被调用的 servlet 方法具有以下签名：

```
public void service(
    ServletRequest request,
    ServletResponse response)
throws ServletException, IOException;
```

`ServletRequest` 对象由 servlet 引擎构造，充当关于客户端和请求信息的包装器。这包括远程系统的身份、请求参数以及与请求关联的任何输入流。类似地，`ServletResponse` 对象为 servlet 提供了将其结果传回原始请求者的方式。它包括用于打开输出流和指定内容类型及长度的方法。尽管 `service()` 方法很重要，但很少直接使用它。原因在于大多数 servlet 被设计为在 HTTP 环境中运行，为此有一个专门的 `javax.servlet.http` 包。大多数 servlet 不直接扩展 `javax.servlet.GenericServlet`，而是扩展其子类 `javax.servlet.http.HttpServlet`。这个子类提供了与每个 HTTP 请求方法相对应的专用方法：GET 请求由 `doGet()` 处理，POST 请求由 `doPost()` 处理，依此类推。这些方法的签名使用特定于 HTTP 的请求和响应对象版本：

```
public void doGet(
    HttpServletRequest request,
    HttpServletResponse response)
    throws ServletException, IOException;
```

`HttpServlet` 中的 `service(Request, Response)` 方法将请求和响应对象转换为其特定于 HTTP 的对应对象，然后调用 `service(HttpServletRequest, HttpServletResponse)`，后者会检查请求并调用适当的 `doGet()`、`doPost()` 或其他方法。因此，一个典型的 HTTP servlet 包含对一个或多个这些辅助方法的重写，而不是对 `service()` 的重写。

[^1]: `UnavailableException` 是 `ServletException` 的一个子类，可以选择包含 servlet 预计不可用的秒数。如果未指定，则假定 servlet 永久不可用。

## destroy

servlet 规范允许 servlet 引擎随时卸载 servlet。这样做可能是为了节省系统资源，或者为 servlet 引擎关闭做准备。servlet 引擎通过调用每个已加载 servlet 的 `destroy()` 方法来通知它即将发生的情况。通过重写 `destroy()`，你可以释放 `init()` 期间分配的任何资源。

> 注意：自己调用 `destroy()` 实际上并不会卸载 servlet。只有 servlet 引擎才能执行此操作。

## 示例：每升公里数转每加仑英里数 Servlet

让我们来看一个简单的 servlet。`K2MServlet`（如下所示）是一个 servlet，它创建一个燃油效率转换表，用每加仑英里数来表示每升公里数。

```
package jspcr.servlets;

import java.io.*;
import java.text.*;
import java.util.*;
import javax.servlet.*;
import javax.servlet.http.*;

/**
 * 打印每加仑英里数到每升公里数的转换表
 */
public class K2MServlet extends HttpServlet
{
    private static final DecimalFormat FMT
        = new DecimalFormat("#0.00");

    private static final String PAGE_TOP = ""
        + "<HTML>"
        + "<HEAD>"
        + "<TITLE>燃油效率转换表</TITLE>"
        + "</HEAD>"
        + "<BODY>"
        + "<H3>燃油效率转换表</H3>"
        + "<TABLE BORDER=1 CELLPADDING=3 CELLSPACING=0>"
        + "<TR>"
        + "<TH>每升公里数</TH>"
        + "<TH>每加仑英里数</TH>"
        + "</TR>"
        ;

    private static final String PAGE_BOTTOM = ""
        + "</TABLE>"
        + "</BODY>"
        + "</HTML>" ;

    public void doGet(
        HttpServletRequest request,
        HttpServletResponse response)
        throws ServletException, IOException
    {
        response.setContentType("text/html");
        PrintWriter out = response.getWriter();

        out.println(PAGE_TOP);
        for (double kpl = 5; kpl <= 20; kpl += 1.0) {
            double mpg = kpl * 2.352146;
            out.println("<TR>");
            out.println("<TD>" + FMT.format(kpl) + "</TD>");
            out.println("<TD>" + FMT.format(mpg) + "</TD>");
            out.println("</TR>");
        }
        out.println(PAGE_BOTTOM);
    }
}
```

首先，注意程序开头的两条导入语句：

```
import javax.servlet.*;
import javax.servlet.http.*;
```

这些语句向编译器表明我们将使用通用和特定于 HTTP 的 servlet 包中的类。导入语句并非严格必需，但它们使得无需指定完全限定名即可引用类成为可能。

接下来是类声明：

```
public class K2MServlet extends HttpServlet
```

servlet 至少需要实现 `javax.servlet.Servlet` 接口。为了简化 servlet 编写，servlet API 提供了该接口的一个基本实现，称为 `GenericServlet`。它还提供了一个特定于 HTTP 的子类 `HttpServlet`，这是最常用于 servlet 的基类。

```
public void doGet(
    HttpServletRequest request,
    HttpServletResponse response)
    throws ServletException, IOException
```

我们的 servlet 对于启动或终止操作没有特殊要求，因此它只重写了一个方法——`doGet()`。如果请求方法是 GET，该方法将从 `HttpServlet` 超类的 `service()` 方法中被调用。

```
response.setContentType("text/html");
```

在将任何结果写回客户端之前，我们需要指定要发送的任何 HTTP 头。在我们的例子中，唯一需要的是 `Content-Type`，我们将其设置为 `text/html`。

```
PrintWriter out = response.getWriter();
```

创建一个 HTML 页面包括将 HTML 语句写入与 HTTP 请求关联的输出流。这个输出流可以通过响应对象的 `getOutputStream()` 或 `getWriter()` 方法获取，具体取决于要写入的是二进制流还是字符输出。需要注意的是，servlet 必须选择这两种方法中的一种；不能同时调用两者。因为我们正在编写普通的 HTML，所以我们将使用 `getWriter()` 来获取一个字符写入器。

剩下的就是打印我们 HTML 表格的文本了。为了方便起见，我们将页面页眉和页脚编码在静态字符串变量 `PAGE_TOP` 和 `PAGE_BOTTOM` 中。我们在所需的每升公里数范围内循环打印表格本身。

```
out.println(PAGE_TOP);
for (double kpl = 5; kpl <= 20; kpl += 1.0) {
    double mpg = kpl * 2.352146;
    out.println("<TR>");
    out.println("<TD>" + FMT.format(kpl) + "</TD>");
    out.println("<TD>" + FMT.format(mpg) + "</TD>");
    out.println("</TR>");
}
out.println(PAGE_BOTTOM);
```

要运行该 servlet，我们首先需要编译它。要成功编译，servlet API 中的类必须在类路径中。这些类通常位于随 servlet 引擎一起分发的 JAR 文件中。官方 JAR 文件也可以在 Apache Jakarta 网站 http://jakarta.apache.org 找到。

接下来，根据 servlet 引擎的不同，可能需要在 Web 应用部署描述符 `/WEB-INF/web.xml` 中描述该 servlet。对于一个简单的 servlet，这可能只包含一个 `<servlet>` 标签及其子元素 `<servlet-name>` 和 `<servlet-class>`。在这种情况下，条目如下所示：

```
<?xml version="1.0" ?>
<web-app>
    ...
    <servlet>
        <servlet-name>K2M</servlet-name>
        <servlet-class>jspcr.servlets.K2MServlet</servlet-class>
    </servlet>
    ...
</web-app>
```

> 注意：`web.xml` 中的 `<servlet>` 条目必须相对于其他元素以特定位置编码。有关详细信息，请参见第 18 章或查看 `web-app_2.2.DTD`。

在大多数情况下，修改 `web.xml` 文件需要在更改生效之前重新启动 servlet 引擎。

最后，可以使用以下形式的 URL 调用该 servlet：

```
http://<servername>/<webappname>/servlet/<servletname>
```

此 servlet 的结果可以在图 4-1 中看到。



## Servlet 类

本节概述了来自 `javax.servlet` 和 `javax.servlet.http` 包的几个重要类。关于 Servlet API 的详细信息，可以在附录 A 中找到。

## Servlet

基本的 Servlet 抽象是 `javax.servlet.Servlet` 接口，如表 4-1 所示。它规定了 Servlet 类必须实现的一组方法，以便被 Servlet 引擎识别和管理。其主要目的是提供生命周期方法 `init()`、`service()` 和 `destroy()`。

Servlet API 提供了 `Servlet` 接口的一个具体实现，名为 `GenericServlet`，在表 4-2 中描述。该类提供了除 `service()` 之外的所有接口方法的默认实现。这意味着你只需扩展 `GenericServlet` 并编写自定义的 `service()` 方法，即可编写一个基本的 Servlet。

**表 4-1。Servlet 接口中的方法**

| 方法 | 描述 |
|---|---|
| `void init(ServletConfig config) throws ServletException` | Servlet 被加载后，Servlet 引擎会调用此方法一次，就在它投入使用之前。如果 `init()` 抛出 `UnavailableException`，则该 Servlet 将被停止服务。Servlet 应提供某种方式来存储 `config` 对象，以实现 `getServletConfig()` 方法（参见 `GenericServlet`）。 |
| `ServletConfig getServletConfig()` | 返回传递给 Servlet 的 `init()` 方法的 `ServletConfig` 对象。 |
| `void service(ServletRequest request, ServletResponse response) throws ServletException, IOException` | 处理 `request` 对象中描述的请求，并使用 `response` 对象将结果返回给请求者。 |
| `String getServletInfo()` | 返回一个可以描述 Servlet 的字符串。用于需要提供人类可读描述的管理工具。 |
| `void destroy()` | Servlet 即将被卸载时，由 Servlet 引擎调用。 |

**表 4-2。GenericServlet 类中的方法**

| 方法 | 描述 |
| :--- | :--- |
| `void destroy()` | 写入一条由单词 "destroy" 组成的日志条目。 |
| `String getInitParameter(String name)` | 返回指定名称的初始化参数的值。通过调用 `config.getInitParameter(name)` 来实现。 |
| `Enumeration getInitParameterNames()` | 返回一个 `Enumeration`，包含为该 Servlet 编码的所有初始化参数，通过调用 `config.getInitParameterNames()` 获取列表。如果没有提供初始化参数，则返回一个空的 `Enumeration`（而不是 null）。 |
| `ServletConfig getServletConfig()` | 返回传递给 `init()` 方法的 `ServletConfig` 对象。 |
| `ServletContext getServletContext()` | 返回 `config` 对象中引用的 `ServletContext`。 |
| `String getServletInfo()` | 返回一个空字符串。 |
| `void log(String msg, Throwable t)` | 将一条记录和堆栈跟踪写入 Servlet 日志。此方法也是对 `ServletContext` 中相应方法的委托调用。 |
| `abstract void service(Request request, Response response) throws ServletException, IOException` | Servlet 引擎调用此方法来处理 `request` 对象描述的请求。这是 `GenericServlet` 中唯一的抽象方法，因此也是子类必须重写的方法。 |
| `String getServletName()` | 返回在 Web 应用程序部署描述符（`web.xml`）中指定的 Servlet 名称。 |

除了 `Servlet` 接口，`GenericServlet` 还实现了 `ServletConfig`，后者处理初始化参数和 Servlet 上下文，并提供便捷方法，这些方法委托给传递给 `init()` 的 `ServletConfig` 对象。

尽管 Servlet API 允许扩展到其他协议，但当前版本仅支持协议无关的 Servlet 和 HTTP Servlet。因为几乎所有的 Servlet 都在 Web 服务器环境中运行，所以很少有 Servlet 直接扩展 `GenericServlet`。更常见的是 Servlet 扩展其特定于 HTTP 的子类 `HttpServlet`，在表 4-3 中描述。关于 HTTP 的介绍，请参见第 3 章。

`HttpServlet` 通过调用特定于 HTTP 请求方法的方法来实现 `service()`。也就是说，对于 DELETE、HEAD、GET、OPTIONS、POST、PUT 和 TRACE，它分别调用 `doDelete()`、`doHead()`、`doGet()`、`doOptions()`、`doPost()`、`doPut()` 和 `doTrace()`。它还将这些方法使用的请求和响应对象强制转换为它们特定于 HTTP 的子类，这将在本节后面描述。

> 什么是协议无关的 Servlet？也许是一个根本不服务请求的 Servlet，而只是从其 `init()` 方法启动后台线程，并在 `destroy()` 中终止它们。这可以用来模拟 Windows NT 服务或 Unix 守护进程。

## 第 4 章：Servlet 简介

**注意：** 处理 `GET`、`POST`、`PUT` 和 `DELETE` 的方法默认返回一个错误，表明请求的方法不受支持，因此 Servlet 需要显式重写它支持的方法。

**表 4-3。HttpServlet 类中的方法**

| 方法 | 描述 |
| :--- | :--- |
| `void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException` | Servlet 引擎调用此方法来处理 HTTP `GET` 请求。可以从 `request` 对象获取输入参数、HTTP 头和输入流（如果有的话），从 `response` 对象获取响应头和输出流。 |
| `void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException` | Servlet 引擎调用此方法来处理 HTTP `POST` 请求。从获取参数和输入数据或返回响应的角度来看，与 `doGet()` 没有区别。 |
| `void doPut(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException` | Servlet 引擎调用此方法来处理 HTTP `PUT` 请求。在这种情况下，请求 URI 表示正在上传的文件的目标位置。 |
| `void doDelete(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException` | Servlet 引擎调用此方法来处理 HTTP `DELETE` 请求。请求 URI 指示要删除的资源。 |
| `void doOptions(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException` | Servlet 引擎调用此方法来处理 HTTP `OPTIONS` 请求。返回一个 `Allow` 响应头，指示此 Servlet 支持的 HTTP 方法。Servlet 很可能不需要重写此方法，因为 `HttpServlet` 方法已经实现了 HTTP 规范所需的功能。 |
| `void doTrace(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException` | Servlet 引擎调用此方法来处理 HTTP `TRACE` 请求。导致请求头作为响应头回显。Servlet 很可能不需要重写此方法，因为 `HttpServlet` 方法已经实现了 HTTP 规范所需的功能。 |
| `void service(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException` | 一个中间方法，由 `service(Request request, Response response)` 使用特定于 HTTP 的请求和响应对象调用。此方法实际上是将请求定向到 `doGet()`、`doPost()` 等。不需要重写此方法。 |
| `void service(Request request, Response response) throws ServletException, IOException` | 将请求和响应对象强制转换为其特定于 HTTP 的子类，并调用特定于 HTTP 的 `service()` 方法。 |

## Servlet 请求

`ServletRequest` 接口封装了客户端请求的详细信息。有一个与协议无关的通用版本，也有一个特定于 HTTP 的子接口。

表 4-4 中显示的与协议无关的版本具有以下方法：

-   查找客户端的主机名和 IP 地址
-   检索请求参数
-   获取和设置属性
-   获取输入和输出流



## Servlet 响应

Servlet 响应对象的功能是将 Servlet 生成的结果传回发起请求的客户端。`ServletResponse` 主要作为一个输出流包装器运作，同时包含其内容类型和长度信息。它由 Servlet 引擎创建，并作为 `service()` 方法的第二个参数传递给 Servlet。与 Servlet 请求类似，Servlet 响应也有一个通用的协议无关类和一个特定于 HTTP 的类。表 4-6 描述了通用版本中可用的方法。

**表 4-4.** *`ServletRequest` 类中的方法*

| 方法 | 描述 |
| :--- | :--- |
| `Object getAttribute(String name)` | 返回具有指定名称的请求属性，如果不存在则返回 null。属性可以是 Servlet 引擎设置的，也可以是通过 `setAttribute()` 显式添加的。后一种方法在与 `RequestDispatcher` 对象配合使用时很有用。 |
| `Enumeration getAttributeNames()` | 返回此请求中所有属性名称的 `Enumeration`。如果没有属性存在，则返回一个空的 `Enumeration`。 |
| `String getCharacterEncoding()` | 返回此请求使用的字符编码。 |
| `int getContentLength()` | 指定输入流的长度（如果有的话）。如果未知，则返回 -1。 |
| `ServletInputStream getInputStream() throws IOException` | 返回与此请求关联的（二进制）输入流（如果有的话）。可以调用 `getInputStream()` 或 `getReader()`，但不能同时调用两者。 |
| `String getParameter(String name)` | 返回指定的输入参数，如果不存在则返回 null。 |
| `Enumeration getParameterNames()` | 返回此请求中所有参数名称的可能为空的 `Enumeration`。 |
| `String[] getParameterValues(String name)` | 返回指定输入参数名称的值数组，如果不存在值则返回 null。在参数可以有多个值的情况下很有用（例如 HTTP 复选框元素）。 |
| `String getProtocol()` | 返回此请求使用的协议的名称和版本。 |
| `String getScheme()` | 返回请求 URL 中直到第一个冒号（但不包括）的子字符串（例如 `http`）。 |
| `String getServerName()` | 返回处理请求的服务器的主机名。 |
| `int getServerPort()` | 返回接收主机正在监听的端口号。 |
| `BufferedReader getReader() throws IOException` | 返回用于与此请求关联的输入数据的字符读取器。可以调用此方法或 `getInputStream()`，但不能同时调用两者。 |
| `String getRemoteAddr()` | 返回客户端主机的数字 IP 地址。 |
| `String getRemoteHost()` | 返回客户端主机的名称（如果已知）。 |
| `void setAttribute(String name, Object obj)` | 将对指定对象的引用存储在请求中，使用指定的名称。 |
| `void removeAttribute(String name)` | 从请求中移除指定的属性。 |
| `Locale getLocale()` | 返回客户端首选的语言环境（如果已知），否则返回 null。 |
| `Enumeration getLocales()` | 返回客户端首选语言环境的 `Enumeration`（如果已知）；否则，返回服务器的首选语言环境。 |
| `boolean isSecure()` | 如果请求是通过安全通道（如 HTTPS）发出的，则返回 `true`。 |
| `RequestDispatcher getRequestDispatcher(String name)` | 返回指定资源名称的 `RequestDispatcher` 对象。有关请求分派的详细信息，请参见第 8 章。 |

表 4-5 中的 `HttpServletRequest` 子接口添加了用于处理以下内容的方法：

- 读取和写入 HTTP 头
- 获取和设置 Cookie
- 获取路径信息
- 识别 HTTP 会话（如果存在）

**表 4-5.** *`HttpServletRequest` 接口中的方法*

| 方法 | 描述 |
| :--- | :--- |
| `String getAuthType()` | 如果 Servlet 受到身份验证方案（如 HTTP 基本身份验证）的保护，则返回该方案的名称。 |
| `String getContextPath()` | 返回指定 Servlet 上下文（Web 应用程序）的 URI 前缀。 |
| `Cookie[] getCookies()` | 返回与此请求关联的 Cookie 数组。 |
| `long getDateHeader(String name)` | `getHeader()` 的便捷版本，将其输出转换为适合构造 `Date` 对象的 `long` 值。 |
| `String getHeader(String name)` | 返回指定 HTTP 头的值（如果此请求中提供了该头）。名称不区分大小写。 |
| `Enumeration getHeaderNames()` | 返回此请求中提供的所有 HTTP 头名称的 `Enumeration`。 |
| `Enumeration getHeaders(String name)` | 返回此请求中提供的指定类型的所有 HTTP 头值的 `Enumeration`。对于可以有多个值的头很有用。 |
| `int getIntHeader(String name)` | `getHeader()` 的便捷版本，将其输出转换为 `int` 值。 |
| `String getMethod()` | 返回 HTTP 请求方法（例如 GET、POST 等）。 |
| `String getPathInfo()` | 返回 URL 中指定的任何附加路径信息。 |
| `String getPathTranslated()` | 返回 URL 中指定的任何附加路径信息，转换为实际路径。 |
| `String getQueryString()` | 返回查询字符串——URL 中“?”之后的部分（如果有的话）。 |
| `String getRemoteUser()` | 如果用户已通过身份验证，则返回远程用户的名称，否则返回 `null`。 |
| `String getRequestedSessionId()` | 返回客户端返回的会话 ID。 |
| `String getRequestURI()` | 返回 URL 中从“/”和上下文开始的部分，直到但不包括任何查询字符串。 |
| `String getServletPath()` | 返回请求 URI 中跟在上下文之后的子字符串。 |
| `HttpSession getSession()` | 调用 `getSession(true)` 的便捷方法。 |
| `HttpSession getSession(boolean create)` | 返回当前 HTTP 会话，如果不存在且 `create` 参数为 `true`，则创建一个新会话。 |
| `Principal getPrincipal()` | 如果用户已通过身份验证，则返回代表当前用户的 `java.security.Principal` 对象，否则返回 `null`。 |
| `boolean isRequestedSessionIdFromCookie()` | 如果请求的会话 ID 由 Cookie 对象提供，则返回 true，否则返回 false。 |
| `boolean isRequestedSessionIdFromURL()` | 如果请求的会话 ID 在请求 URL 中编码，则返回 true，否则返回 false。 |
| `boolean isRequestedSessionIdValid()` | 如果客户端返回的会话 ID 仍然有效，则返回 true。 |
| `boolean isUserInRole(String role)` | 如果当前通过身份验证的用户与指定角色关联，则返回 true。如果不关联或用户未通过身份验证，则返回 false。 |

**表 4-6.** *`ServletResponse` 接口中的方法*

| 方法 | 描述 |
| :--- | :--- |
| `void flushBuffer() throws IOException` | 将输出缓冲区的内容发送到客户端。因为 HTTP 要求在发送内容之前发送头，所以调用此方法会发送状态行和响应头，从而提交请求。 |
| `int getBufferSize()` | 返回响应使用的缓冲区大小，如果缓冲未生效则返回 0。 |
| `String getCharacterEncoding()` | 返回用于响应的字符编码的名称。除非明确设置为其他值，否则对应于 ISO-8859-1。 |
| `Locale getLocale()` | 返回用于响应的语言环境。除非使用 `setLocale()` 修改，否则默认为服务器的语言环境。 |
| `OutputStream getOutputStream() throws IOException` | 返回一个可用于写入要返回给客户端的二进制输出的流。可以调用此方法或 `getWriter()`，但不能同时调用两者。 |
| `Writer getWriter() throws IOException` | 返回一个可用于写入要返回给客户端的文本输出的字符写入器。可以调用此方法或 `getOutputStream()`，但不能同时调用两者。 |
| `boolean isCommitted()` | 如果状态和响应头已经发送回客户端，则返回 true。在响应提交后设置头没有效果。 |
| `void reset()` | 清除输出缓冲区以及任何响应头。如果响应已经提交，则会导致 `IllegalStateException`。 |
| `void setBufferSize(int nBytes)` | 设置响应的最小缓冲区大小。实际缓冲区大小可能更大，可以通过调用 `getBufferSize()` 获取。如果已经写入任何输出，则此方法会抛出 `IllegalStateException`。 |



## Servlet 上下文

Servlet 上下文是由 Servlet 引擎提供的接口，用于向 Web 应用程序提供服务。Web 应用程序中的 Servlet 可以使用 Servlet 上下文来获取：
- 在不同调用之间存储和检索属性，以及与其他 Servlet 共享这些属性的能力。
- 读取 Web 应用程序中文件和其他静态资源内容的能力。
- 相互分发请求的一种方式。
- 记录错误和信息性消息的设施。

Servlet 上下文具有一个名称（它所属的 Web 应用程序的名称），该名称唯一地映射到文件系统中的一个目录。
Servlet 可以通过调用传递给 `init()` 的 `ServletConfig` 对象上的 `getServletContext()` 方法来获取对 Servlet 上下文的引用。如果 Servlet 直接或间接继承了 `GenericServlet`，它可以使用继承的便捷方法 `getServletContext()`。³
表 4-8 概述了 `ServletContext` 提供的方法。

³ JSP 页面更加简单——对 Servlet 上下文的引用会自动存储在隐式变量 `application` 中。

## 表 4-8. ServletContext 接口中的方法

| 方法 | 描述 |
| :--- | :--- |
| `ServletContext getContext(String uripath)` | 返回映射到同一服务器上另一个 URI 的 Servlet 上下文。URI 必须是以 "/" 开头的绝对路径。 |
| `String getInitParameter(String name)` | 返回指定的、适用于整个上下文的初始化参数的值。这与 `ServletConfig` 中同名的方法不同，后者仅适用于编写它的特定 Servlet。相反，这是一个适用于上下文内所有 Servlet 的参数。 |
| `Enumeration getInitParameterNames()` | 返回所有适用于整个上下文的初始化参数名称的（可能为空的）`Enumeration`。 |
| `int getMajorVersion()`<br>`int getMinorVersion()` | 返回此上下文支持的 Servlet API 级别的主要和次要版本号。 |
| `String getMimeType(String fileName)` | 返回指定文件名的 MIME 类型。通常基于文件扩展名，而非文件本身的内容（文件本身不一定存在）。如果 MIME 类型未知，可能返回 `null`。 |
| `RequestDispatcher getNamedDispatcher(String name)`<br>`RequestDispatcher getRequestDispatcher(String path)` | 返回一个 `RequestDispatcher`，用于具有指定名称或路径的 Servlet 或 JSP 页面，如果无法创建 `RequestDispatcher` 则返回 `null`。如果指定了路径，则该路径必须以 "/" 开头，并且相对于 Servlet 上下文的根目录。 |
| `String getRealPath(String path)` | 给定一个 URI，返回文件系统中该 URI 对应的绝对路径，如果无法进行映射则返回 `null`。 |
| `URL getResource(String path)`<br>`InputStream getResourceAsStream(String path)` | 返回一个 URL，对应于相对于 Servlet 上下文的指定绝对路径，或者返回用于读取该 URL 的输入流。如果不存在这样的资源，则返回 `null`。 |
| `String getServerInfo()` | 返回 Servlet 引擎的名称和版本号。 |
| `void log(String message)`<br>`void log(String message, Throwable t)` | 将消息写入 Servlet 日志，如果提供了 `Throwable` 参数，则包括堆栈跟踪信息。 |
| `void removeAttribute(String name)` | 从 Servlet 上下文中移除指定的属性。 |

## 表 4-6. ServletResponse 接口中的方法

| 方法 | 描述 |
|---|---|
| `void setContentLength(int length)` | 设置内容体的长度。 |
| `void setContentType(String type)` | 设置内容类型。在 HTTP Servlet 中，这将设置 `Content-Type` 头。 |
| `void setLocale(Locale locale)` | 设置响应中要使用的语言环境。在 HTTP Servlet 中，这可能会影响 `Content-Type` 头的值。 |

特定于 HTTP 的子接口 `HttpServletResponse` 添加了用于操作状态码、状态消息和响应头的方法。（附录 C 详细描述了 HTTP 响应头。）这使得它，例如，可用于发送 cookie 或将用户重定向到另一个 URL。它还提供了在写入网页的 URL 中编码 HTTP 会话 ID 的功能。表 4-7 描述了 `HttpServletResponse` 中的方法。

## 表 4-7. HttpServletResponse 接口中的方法

| 方法 | 描述 |
|---|---|
| `void addCookie(Cookie cookie)` | 导致一个 `Set-Cookie` 头被添加到响应中。 |
| `void addDateHeader(String name, long date)` | 便捷方法，使用指定的日期值添加一个具有指定名称的响应头（或替换所有同名的头）。这个 long 整型日期值应该是适合 `java.util.Date(long time)` 构造函数的值。 |
| `void setDateHeader(String name, long date)` | 便捷方法，使用指定的日期值添加一个具有指定名称的响应头（或替换所有同名的头）。这个 long 整型日期值应该是适合 `java.util.Date(long time)` 构造函数的值。 |
| `void setHeader(String name, String value)` | 设置一个具有指定名称和值的响应头。 |
| `void addIntHeader(String name, int value)`<br>`void setIntHeader(String name, int value)` | 使用指定的整数值添加一个响应头（或替换所有同名的头）。 |
| `boolean containsHeader(String name)` | 如果响应已经包含一个具有此名称的头，则返回 true。 |
| `String encodeRedirectURL(String url)`<br>`String encodeURL(String url)` | 将会话 ID 添加到 URL 中，除非已知客户端接受 cookie。第一种形式应仅用于计划在 sendRedirect() 中使用的 URL。其他需要编码的 URL 应传递给 encodeURL()。 |
| `void sendError(int status)`<br>`void sendError(int status, String msg)` | 将响应状态码设置为指定值（并可选地设置状态消息）。HttpServletResponse 定义了一套完整的整数常量，用于有效的状态值。 |
| `void setStatus(int status)` | 将响应状态码设置为指定值。应仅用于不表示错误的响应。错误响应应使用 sendError() 代替。 |

除了额外的方法，HttpServletResponse 还为每个可能的 HTTP 响应代码定义了整数常量。

## 线程模型

默认情况下，Servlet 引擎仅加载一个 Servlet 实例。由 Servlet 处理的请求在单独的线程中运行，但共享同一个实例，因此共享相同的实例变量。这一事实有几个影响，最值得注意的是*实例变量不是线程安全的*。例如，看下面的 Servlet：

```
package jspcr.servlets;

import java.io.*;
import java.sql.*;
import java.util.*;

import javax.servlet.*;
import javax.servlet.http.*;

/**
 * Bad example! Don't try this at home.
 */
public class ColliderServlet extends HttpServlet
{
    private Connection con;

    public void doGet(
            HttpServletRequest request,
            HttpServletResponse response)
            throws ServletException, IOException
    {
        try {
            Class.forName("sun.jdbc.odbc.JdbcOdbcDriver");
            con = DriverManager.getConnection("jdbc:odbc:usda");
            // ... run some lengthy database operation here
        }
        catch (Exception e) {
            throw new ServletException(e.getMessage());
        }
    }
}
```

考虑当两个请求在相隔几百毫秒的时间内到达，且在不同线程中时会发生什么。第一个请求打开数据库连接，并将其引用存储在 `con` 实例变量中。然后它使用该连接执行表更新或其他数据库操作。与此同时，第二个请求到达，打开另一个连接，并将对该连接的引用存储在相同的 `con` 实例变量中。如果第一个操作完成并尝试进行另一个数据库操作，它将不再拥有其原始连接对象——它只知道第二个连接。当它尝试使用第二个连接时，糟糕的事情就会发生。

在 Servlet 从其服务方法中调用其他方法时，实例变量也可能发生同样类型的问题。如果这些其他方法尝试访问 Servlet 请求、响应或在服务方法中创建并保存在实例变量中的任何对象，则无法保证另一个线程中的请求不会通过将其自身对象的引用存储在其中来破坏这些变量⁴。

最安全的方法是根本不使用实例变量，只使用在服务方法内部定义的局部变量。

⁴ 这个特定问题可以通过使用一个私有类（本质上是一个数据结构）来容纳所有感兴趣的对象，然后将该类作为参数传递给辅助方法来解决。



## SingleThreadModel

虽然单实例多线程模型是默认配置，但Servlet可以通过实现`SingleThreadModel`接口来改变此行为。这个没有任何方法的接口会告知Servlet引擎，它应该创建一个实例池，并将每个传入的请求分配给自己的实例和线程。这保证了没有两个*由同一实例处理*的请求会在执行service方法时重叠。因此，实例变量一次只能被一个请求影响，从而保证线程安全。但请注意，由于可能存在多个实例，因此无法阻止它们在不同的线程中并发执行。如果它们访问文件或数据库连接等外部资源，则仍然可能发生冲突。在很少的情况下，`SingleThreadModel`能解决其他方式无法更好处理的问题。

## HTTP Sessions

尽管在网页中导航看起来像是客户端与服务器之间的对话，但在大多数情况下并非如此。通常，Web客户端请求一个HTML文档，服务器定位该文档并将其传回客户端。如果HTML中包含图片链接，客户端（如果是Web浏览器）将为每张图片向服务器发出额外的请求。如果用户点击页面中的超链接，客户端会为此发出一个新的HTTP请求，但所有这些都是逐个请求发生的。在每个请求之间，服务器会继续处理其他请求，完全忘记了第一个客户端。没有来回交换命令和数据，只有请求、响应然后断开连接。⁵

对于静态文档的基本下载来说，这已经足够了。但是，像购物车或迭代搜索引擎这样的应用程序需要在服务器上维护与特定客户端关联的活动对象。构建这些对象可能需要多个请求。在这种情况下，需要跟踪这些对象与哪个客户端绑定。

有几种方法可以解决这个问题。其中大多数涉及在服务器上维护对象本身，并为其分配一个唯一密钥，要求客户端记住。在每个后续的相关请求中，客户端传回该密钥，从而使服务器能够重新建立上下文。

这类似于通过电话预订机票。票务代理要求客户提供她的姓名、地址和航班信息，将所有这些输入数据录入应用程序，该程序分配一个确认号码，并将其报告给客户。如果客户稍后需要回电更改任何内容，她提供确认号码，这允许票务代理访问并更新原始记录。

如何引导客户端在需要时记住并提供密钥？有几种方法：

- **Cookies** 服务器可以在其初始响应中发送一个`Set-Cookie`头，将会话ID作为cookie的值⁶。在后续请求中，客户端可以通过`Cookie`头返回该值。但是，单个用户可能会选择关闭其浏览器的cookie功能，因此此技术不能保证有效。
- **将会话ID附加到URL** 对于动态过程创建的网页中的超链接，会话ID可以编码为URL中的请求参数。这不需要启用cookie，但它要求每个可点击的URL都被如此编码。如果有一个被遗漏了（这很容易发生），会话链接就会丢失。
- **隐藏字段** 如果应用程序由一系列使用`submit`按钮进行导航的HTML表单组成，会话ID可以存储为隐藏字段，并通过`request.getParameter()`检索。显然，这仅在所有表单都是动态生成时才有效。

## HttpSession接口

Servlet API为这些各种技术提供了一个方便的包装器，称为*HTTP Session*。一个名为`javax.servlet.http.HttpSession`的类似哈希表的接口具有`setAttribute()`和`getAttribute()`方法，这些方法按名称存储和检索对象。`HttpSession`提供了一个会话ID密钥，参与的客户端存储并在同一会话的后续请求中返回。Servlet引擎查找相应的会话对象并使其可用于当前请求。表4-9列出了`HttpSession`中的可用方法。

表4-9. HttpSession接口中的方法

| 方法 | 描述 |
| :--- | :--- |
| `Object getAttribute(String name)`<br>`void setAttribute(String name, Object value)`<br>`void removeAttribute(String name)` | 在会话中按指定名称存储对象，或按该名称返回或删除之前存储的对象。 |
| `Enumeration getAttributeNames()` | 返回当前绑定到会话的所有属性名称的`Enumeration`。 |
| `long getCreationTime()`<br>`long getLastAccessedTime()` | 返回一个长整数，表示会话创建或最后访问的日期和时间。该整数采用`java.util.Date()`构造函数使用的格式。 |
| `String getId()` | 返回会话ID，这是由Servlet引擎分配的唯一密钥。 |
| `int getMaxInactiveInterval()`<br>`void setMaxInactiveInterval(int seconds)` | 设置或返回如果与客户端没有交互，会话将保持活动的最大秒数。 |
| `void invalidate()` | 使会话过期并解绑其中的任何对象。 |
| `boolean isNew()` | 如果客户端尚未加入会话，则返回`true`。当会话首次创建并将会话ID传递给客户端，但客户端尚未发出包含会话ID的第二个请求时，此值为true。 |

该API还提供了一个`HttpSessionBindingListener`接口。实现此接口的对象必须提供`valueBound()`和`valueUnbound()`方法，当对象被添加到或从HttpSession中移除时，这些方法会被调用。

## 总结

Java Servlet是对Web服务器的扩展，允许根据客户端请求动态创建Web内容。它们由Servlet引擎管理，Servlet引擎加载并初始化它们，传递它们多个请求进行处理，然后卸载它们。Servlet比其他服务器端编程环境具有关键优势：

- 性能更好，因为它们驻留在内存中，并且可以同时在多个线程中运行
- 简单性，因为除了Web浏览器之外，不需要安装客户端软件
- 会话跟踪
- 访问Java技术，包括线程、网络和数据库连接

Servlet在固定的生命周期中运行，向Servlet引擎提供用于初始化、处理请求和终止的回调方法。API提供两种线程模型：默认的是单实例运行多线程，另一种是单线程模型。

Servlet API中的主要类和接口是：

- `Servlet`接口，它规定了必须实现的回调方法
- `GenericServlet`，一个实现`Servlet`接口方法的基类
- `HttpServlet`，`GenericServlet`的特定于HTTP的子类
- `ServletRequest`，封装有关客户端请求的信息
- `ServletResponse`，提供对输出流的访问以将结果返回给客户端
- `ServletContext`接口，允许一组Servlet在Web应用程序中相互操作

Servlet是JSP页面的基础技术。理解它们对于形成在JSP环境中进行开发和调试所需的思维模型至关重要。

---
**脚注：**

⁵ HTTP 1.1确实提供了一种使连接持续几秒钟的方法，因此，例如，可以高效地下载HTML及相关图像。这需要客户端和服务器都了解该能力并明确请求。然而，请求/响应协议本身是相同的。

⁶ Cookies是由Web服务器发送的名称/值对，具有指定的生命周期。客户端浏览器存储cookie，并在每次浏览器从同一域请求页面时自动将其返回给服务器。有关cookie的更多详细信息，请参见RFC 2109规范。



## 第五章

## JSP 概述

JavaServer 页面（JSP）是一种用于生成动态 HTML 文档的网页模板，它使用 Java 代码来动态生成内容。JSP 运行在一种称为 JSP 容器的服务器端组件中，该容器会将它们翻译为等效的 Java servlet。

因此，servlet 和 JSP 页面密切相关。一种技术能实现的功能，在很大程度上另一种也能实现，尽管每种技术都有其独特的优势。由于 JSP 页面本质上是 servlet，因此它们继承了 servlet 的所有优点：

- 它们比 CGI 脚本具有更好的性能和可扩展性，因为它们在内存中持久存在且支持多线程。
- 不需要特殊的客户端设置。
- 它们内置支持 HTTP 会话，这使得应用程序编程成为可能。
- 它们可以完全访问 Java 技术——网络感知、线程和数据库连接——而不受客户端小程序的限制。

但是，此外，JSP 页面也有其自身的优势：

- 它们会在必要时自动重新编译。
- 由于它们存在于普通的 Web 服务器文档空间中，因此寻址 JSP 页面比寻址 servlet 更简单。
- 由于 JSP 页面类似于 HTML，因此它们与 Web 开发工具具有更好的兼容性。

本章概述了作为服务器端脚本环境的 JSP。它描述了 JSP 容器的操作，并逐步讲解了一个完整的示例。这里仅涵盖基础知识；第二部分的六章将深入探讨 JSP 页面。

## JSP 工作原理

JSP 页面以三种形式存在：

- **JSP 源代码** 这是开发人员实际编写的代码形式。它存在于扩展名为 .jsp 的文本文件中，由 HTML 模板代码、Java 语言语句以及描述如何生成网页以服务特定请求的 JSP 指令和动作混合而成。
- **Java 源代码** JSP 容器会根据需要将 JSP 源代码翻译为等效的 Java servlet 源代码。此源代码通常保存在工作区中，并且通常有助于调试。
- **编译后的 Java 类** 与任何其他 Java 类一样，生成的 servlet 代码被编译为 .class 文件中的字节码，准备被加载和执行。

JSP 容器根据每个文件的时间戳自动管理 JSP 页面的每种形式。为了响应 HTTP 请求，容器会检查 .jsp 源文件自上次编译 .java 源文件以来是否被修改过。如果是，容器会将 JSP 源代码重新翻译为 Java 源代码并重新编译它。图 5-1 说明了 JSP 容器使用的过程。当请求一个 JSP 页面时，容器首先确定与 .jsp 文件对应的类名。如果该类不存在，或者它比 .jsp 文件更旧（意味着 JSP 源代码自上次编译以来已更改），则容器会为等效的 servlet 创建 Java 源代码并编译它。如果 servlet 的实例尚未运行，容器会加载 servlet 类并创建一个实例。最后，容器分派一个线程在已加载的实例中处理当前的 HTTP 请求。

## 一个基本示例

为了说明 JSP 的工作原理，让我们看看上一章使用的同一个示例——将每升公里数转换为每加仑英里数。这是 JSP 页面：

```
<%@ page session="false" %>
<%@ page import="java.io.*,java.text.*,java.util.*" %>
<%-- 打印从每加仑英里数到每升公里数的转换表 --%>
<%!
    private static final DecimalFormat FMT
        = new DecimalFormat("#0.00");
%>
<HTML>
<HEAD>
<TITLE>燃油效率转换表</TITLE>
</HEAD>
<BODY>
<H3>燃油效率转换表</H3>
<TABLE BORDER=1 CELLPADDING=3 CELLSPACING=0>
<TR>
<TH>每升公里数</TH>
<TH>每加仑英里数</TH>
</TR>
<%
    for (double kpl = 5; kpl <= 20; kpl += 1.0) {
        double mpg = kpl * 2.352146;
%>
<TR>
    <TD><%= FMT.format(kpl)%></TD>
    <TD><%= FMT.format(mpg)%></TD>
</TR>
<%
    }
%>
</TABLE>
</BODY>
</HTML>
```

将其与第四章的 K2MServlet 进行比较，首先注意到 JSP 更短——33 行对比 servlet 的 55 行。此外，它看起来更像一个网页。大部分 HTML 都可以识别为普通的 HTML。另外，对于 Java 程序员来说，很明显存在某种循环来生成表格的各个行。最后，出现了一组特殊字符，似乎用来标记 Java 代码和 HTML 模板数据之间的边界。如果你不明白它们是什么，不用担心——这将在第 6、7 和 8 章中完整介绍。

如果你从 Web 浏览器调用此 JSP 页面，你会看到图 5-2 所示的表格，不出所料，它与第四章 servlet 产生的结果相同。为了使 JSP 与 servlet 的关系更清晰，可以查看 JSP 容器生成的 .java 源代码。根据所使用的容器及其采用的实现方法，这段代码可能会有很大差异。这里列出的代码是由 JRun 3.0 生成的（为便于阅读已稍作重新格式化）：

**图 5-2.** JSP 页面产生的每升公里数到每加仑英里数输出

```
import javax.servlet.*;
import javax.servlet.http.*;
import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import allaire.jsp.JRunJSPStaticHelpers;
import java.io.*;
import java.text.*;
import java.util.*;
public class jrun__Chap05__examples__K2M2ejsp18
    extends allaire.jsp.HttpJSPServlet
    implements allaire.jsp.JRunJspPage
{
    private ServletConfig config;
    private ServletContext application;
    private Object page = this;
    private JspFactory __jspFactory
        = JspFactory.getDefaultFactory();

    public void _jspService(
            HttpServletRequest request,
            HttpServletResponse response)
        throws ServletException, java.io.IOException
    {
        if (config == null) {
            config = getServletConfig();
            application = config.getServletContext();
        }
        response.setContentType("text/html; charset=ISO-8859-1");
        PageContext pageContext = __jspFactory.getPageContext
            (this, request, response, null, false, 8192, true);
        JspWriter out = pageContext.getOut();

        try {
            out.print("\r\n<HTML>\r\n"
                + "<HEAD>\r\n"
                + "<TITLE>Fuel Efficiency Conversion Chart</TITLE>\r\n"
                + "</HEAD>\r\n"
                + "<BODY>\r\n"
                + "<H3>Fuel Efficiency Conversion Chart</H3>\r\n"
                + "<TABLE BORDER=1 CELLPADDING=3 CELLSPACING=0>\r\n"
                + "<TR>\r\n<TH>Kilometers per Liter</TH>\r\n"
                + "<TH>Miles per Gallon</TH>\r\n</TR>\r\n");

for (double kpl = 5; kpl <= 20; kpl += 1.0) {
    double mpg = kpl * 2.352146;
    out.print("\r\n<TR>\r\n    <TD>");
    out.print(FMT.format(kpl));
    out.print("</TD>\r\n    <TD>");
    out.print(FMT.format(mpg));
    out.print("</TD>\r\n</TR>\r\n");
}
out.print("\r\n</TABLE>\r\n</BODY>\r\n</HTML>\r\n");
}
catch (Throwable t) {
    if (t instanceof ServletException)
        throw (ServletException) t;
    if (t instanceof java.io.IOException)
        throw (java.io.IOException) t;
    if (t instanceof RuntimeException)
        throw (RuntimeException) t;
    throw JRunJSPStaticHelpers.handleException
            (t, pageContext);
} finally {
    __jspFactory.releasePageContext(pageContext);
}
}
private static final DecimalFormat FMT
    = new DecimalFormat("#0.00");
private static final String[] __dependencies__
    = {"/Chap05/examples/K2M.jsp",null};
private static final long[] __times__ = {980969842306L,0L};
public String[] __getDependencies()
{
    return __dependencies__;
}
public long[] __getLastModifiedTimes()
{
    return __times__;
}
public int __getTranslationVersion()
{
```



## 第二部分

## JSP 基础要素

接下来的六章将探讨 JSP 的语法和语义，为你提供创建可运行代码所需的技能。主题涵盖基本语法、脚本段、表达式、声明、文件包含、请求转发以及页面行为指定。最后一章则提供了关于 JSP 自定义标签的详细教程。

## 第 6 章

JSP 语法与语义

本章旨在概述 JavaServer Pages 中使用的基本组件，描述它们的编写方式，并解释它们的功能。本章将回顾 JSP 开发模型，然后介绍每个 JSP 元素，并探讨该元素在整体设计中的使用方式。最后，通过一个带注释的示例来说明每个元素的使用。在介绍这些内容时，我们主要关注以下方面：

- 语法：用于表示元素的编码结构，以便 JSP 编译器能够识别它
- 语义：元素对 JSP 容器的意义——当它被使用时会发生什么

本章描述的每个 JSP 元素，都将在第二部分的剩余章节中进行更详细的介绍。

## JSP 开发模型

回顾第 5 章，一个 JSP 页面以三种形式存在：

1. 包含 HTML 语句和 JSP 元素的 .jsp 源文件
2. 用于 servlet 程序的 Java 源代码
3. 编译后的 Java 类

为了理解 JSP 元素如何运作，建立一个关于这三种对象如何创建以及它们之间关系的思维模型非常重要。首先，JSP 开发者编写一个 .jsp 源文件，并将其存储在 Web 服务器或 Web 应用程序的文档文件系统中的某个位置。在这方面，.jsp 源文件与普通的 HTML 文件没有区别。它在网络上被识别的 URL 是相同的，只是其文件名以 .jsp 结尾，而不是 .html。接下来，当 .jsp URL 首次被调用时，JSP 容器读取 .jsp 文件，解析其内容，并生成等效 Java servlet 的源代码。然后它编译该 servlet 并创建一个 .class 文件。最后，JSP 容器加载 servlet 类，并使用它来处理 HTTP 请求。中间步骤（生成 servlet 源代码）只有在 .jsp 文件被更新后，才会为后续的请求重复执行。

在这个设计中，JSP 元素可以在两个操作阶段影响 JSP 容器的操作：

- 翻译时：从 .jsp 文件生成 Java servlet 源代码
- 请求时：调用 servlet 处理 HTTP 请求

记住这个模型有助于你理解 JSP 页面的语法单元及其可能的能力。

## JSP 页面的组件

一个 .jsp 文件可以包含 JSP 元素、固定的模板数据，或者两者的任意组合。JSP 元素是给 JSP 容器的指令，说明应生成什么代码以及如何操作。这些元素具有特定的开始和结束标签，以便 JSP 编译器识别它们。模板数据是 JSP 容器无法识别的所有其他内容。模板数据（通常是 HTML）未经修改地传递，因此最终生成的 HTML 包含的模板数据与 .jsp 文件中编码的完全一致。

JSP 元素有三种类型：

- 指令
- 脚本元素，包括表达式、脚本段和声明
- 动作

让我们更详细地探讨每一种元素。

## 指令

指令是给 JSP 容器的指令，描述应生成什么代码。它们的一般形式是

```
<%@ directive-name [attribute="value" attribute="value" ...] %>
```

在开头的 <%@ 和结尾的 %> 之后可以有零个或多个空格、制表符和换行符，并且在指令名以及属性/值对之间可以有一个或多个空白字符。唯一的限制是开头的 <%@ 标签必须与结尾的 %> 标签位于同一个物理文件中。

JSP 1.1 规范描述了在所有兼容的 JSP 环境中可用的三种标准指令：

- page
- include
- taglib

尽管规范声明在 JSP 1.1 环境中不能使用自定义指令，但这为在后续规范中包含用户自定义指令留下了可能性。
接下来的三节将概述这些指令中的每一个。

## page 指令

*page 指令*用于指定整个 JSP 页面的属性。其语法如下：

`<%@ page [attribute="value" attribute="value" ...] %>`

其中属性是表 6-1 中列出的任何属性。

| 属性 | 值 |
| :--- | :--- |
| `language` | 脚本段、表达式和声明中使用的语言。在 JSP 1.1 中，此属性的唯一有效值是 java。 |
| `extends` | 此 JSP 页面的超类的完全限定名。这必须是一个实现了 `HttpJspPage` 接口的类。JSP 规范警告，在不完全理解其含义的情况下使用此属性。 |
| `import` | 以逗号分隔的一个或多个 `package.*` 名称和/或完全限定类名的列表。此列表用于在生成的 Java servlet 中创建相应的 import 语句。以下包是自动包含的，无需指定：<br>java.lang.*<br>java.servlet.*<br>java.servlet.jsp.*<br>java.servlet.http.* |
| `session` | *true* 或 *false*，指示 JSP 页面是否需要 HTTP 会话。如果值为 true，则生成的 servlet 将包含创建（或访问，如果已存在）HTTP 会话的代码。默认值为 *true*。 |
| `buffer` | 指定输出缓冲区的大小。有效条目是 *nnn*kb 或 *none*，其中 *nnn* 是为缓冲区分配的千字节数。默认值是 8kb。 |
| `autoflush` | 如果缓冲区已满时应自动刷新，则为 *true*，否则如果应抛出缓冲区溢出异常，则为 *false*。默认值是 *true*。 |
| `isThreadSafe` | 如果页面可以处理来自多个线程的并发请求，则为 *true*，否则为 *false*。如果为 *false*，则生成的 servlet 声明它实现了 SingleThreadModel 接口。 |
| `info` | 页面的 getServletInfo() 方法将返回的字符串。 |
| `isErrorPage` | 如果此页面打算用作另一个 JSP 的错误页面，则为 *true*。在这种情况下，可以在另一个页面的 page 指令中将此页面指定为 errorPage 属性的值。将此属性指定为 *true* 会使异常隐式变量在此页面中可用。默认值为 *false*。 |
| `errorPage` | 指定另一个 JSP 页面的 URL，该页面将被调用以处理任何未捕获的异常。另一个 JSP 页面必须在其 page 指令中指定 isErrorPage="true"。 |
| `contentType` | 指定在生成的 servlet 中使用的 MIME 类型，以及可选的字符编码。 |

一个文件中可以有多个 page 指令，并且指定的属性集体应用于整个文件，但除了 *import* 属性外，任何属性都不能指定超过一次。
第 10 章将更详细地介绍 page 指令。

## include 指令

*include 指令*在翻译时将另一个文件的内容合并到 .jsp 源输入流中，类似于 C 预处理器的 #include 指令。其语法是

```
<%@ include file="filename" %>
```

其中 *filename* 是一个绝对或相对路径名，根据当前 servlet 上下文进行解释。示例如下

```
<%@ include file="/header.html" %>
<%@ include file="/doc/legal/disclaimer.html" %>
<%@ include file="sortmethod" %>
```



include 指令与本章后面介绍的 `<jsp:include>` 动作形成对比，后者在请求时将另一个文件的输出合并到响应输出流中。这两种元素都可用于在 JSP 页面中包含标准页眉和页脚或其他通用文本。第 8 章将详细探讨这两种方法。

## taglib 指令

taglib 指令通过使用标签库，使自定义操作在当前页面中可用。该指令的语法如下

```
<%@ taglib uri="tagLibraryURI" prefix="tagPrefix" %>
```

其中属性如下所列：

| 属性 | 值 |
|---|---|
| tagLibraryURI | 标签库描述符的 URL。 |
| tagPrefix | 一个唯一前缀，用于标识页面中后面使用的自定义标签。 |

例如，如果使用了以下指令，

```
<%@ taglib uri="/tlds/FancyTableGenerator.tld" prefix="ft" %>
```

并且如果 `FancyTableGenerator.tld` 定义了一个名为 `table` 的标签，那么页面就可以包含以下类型的标签

```
<ft:table>
  . . .
</ft:table>
```

第 11 章将详细讨论 JSP 标签扩展。

## 注释

JSP 规范提供了两种在 JSP 页面中包含注释的方法：一种是仅在 JSP 页面本身可见的隐藏注释，另一种是包含在页面生成的 HTML 或 XML 输出中的注释。前一种类型的语法是

```
<%-- 这是一个隐藏的 JSP 注释 --%>
```

而后一种看起来像这样：

```
<!-- 这被包含在生成的 HTML 中 -->
```

当 JSP 编译器遇到 JSP 注释的开始标记 `<%--` 时，它会忽略从文件中的该点开始直到找到匹配的结束标记 `--%>` 为止的所有内容。这意味着 JSP 注释可用于禁用（或“注释掉”）JSP 页面的部分内容。这是一种历史悠久的技术，用于在不主要修改源代码的情况下临时启用和禁用程序的各个部分。然而，这也意味着 JSP 注释不能嵌套，因为内部注释的结束标记会被解释为标记外部注释的结束。

另一种注释类型使用普通的 HTML 或 XML 注释标签。这种类型的注释原封不动地传递到响应输出流，并包含在生成的 HTML 中。它们在浏览器窗口中不可见，但可以通过选择“查看源代码”菜单选项看到。

如果注释的目的是启发查看它的人，那么第二种注释类型似乎不如第一种有用，原因有两个：它存在于程序生成的 HTML 中，并且通常永远不会被人看到。然而，由于这些 HTML 注释是计算机生成的，它们可以包含版本号、日期和其他标识号，这些可能对技术支持人员在故障排除时很有用。例如，包含在 JSP 页面中的这三行

```
<!--
远程地址为 <%= request.getRemoteAddr() %>
-->
```

将会记录发起 Web 请求的用户的远程地址，而不会使输出变得杂乱。如果应用程序出现问题，技术支持人员可以指示用户查看生成的 HTML 源代码并报告标识数据。

## 表达式

JSP 提供了一种简单的方法来访问 Java 变量或其他表达式的值，并将该值与页面中的 HTML 合并。语法是

```
<%= exp %>
```

其中 `exp` 是任何有效的 Java 表达式。该表达式可以具有任何数据值，只要它可以转换为字符串即可。这种转换通常只需生成一个 `out.print()` 语句即可完成。例如，JSP 代码

```
The current time is <%= new java.util.Date() %>
```

可能会生成 servlet 代码

```
out.write("The current time is ");
out.print( new java.util.Date() );
out.write("\r\n");
```

提示：理解生成了什么代码可以帮助你记住不要在表达式中放入分号。

第 7 章将更详细地讨论表达式。

## 脚本段

脚本段是一组一个或多个 Java 语言语句，旨在用于处理 HTTP 请求。脚本段的语法是

```
<% 语句; [语句; ...] %>
```

JSP 编译器只是将脚本段的内容原样包含在 `_jspService()` 方法的主体中。一个 JSP 页面可以包含任意数量的脚本段。如果存在多个脚本段，它们将按照编码的顺序依次附加到 `_jspService()` 方法中。既然如此，一个脚本段可能包含一个开始花括号，而这个花括号在另一个脚本段中闭合。考虑以下 JSP 页面，它生成一个华氏度到摄氏度的温度转换表：

```
<%@ page import="java.text.*" %>
<TABLE BORDER=0 CELLPADDING=3>
<TR>
    <TH>Degrees<BR>Fahrenheit</TH>
    <TH>Degrees<BR>Celsius</TH>
</TR>
<%
    NumberFormat fmt = new DecimalFormat("###.000");
    for (int f = 32; f <= 212; f += 20) {
        double c = ((f - 32) * 5) / 9.0;
        String cs = fmt.format(c);
%>
    <TR>
        <TD ALIGN="RIGHT"><%= f %></TD>
        <TD ALIGN="RIGHT"><%= cs %></TD>
    </TR>
<%
    }
%>
</TABLE>
```

示例代码包含两个脚本段：一个用于循环的主体，一个用于闭合花括号。两个脚本段之间是单个表格行的 HTML 标记，使用 JSP 表达式来访问值。生成的 servlet 代码将脚本段及其之间的内容转换为

```
NumberFormat fmt = new DecimalFormat("###.000");
for (int f = 32; f <= 212; f += 20) {
    double c = ((f - 32) * 5) / 9.0;
    String cs = fmt.format(c);
    out.write("\r\n<TD ALIGN=\"RIGHT\">");
    out.print( f );
    out.write("</TD>\r\n");
    out.write("\r\n<TD ALIGN=\"RIGHT\">");
    out.print( cs );
    out.write("</TD>\r\n");
    out.write("</TD>\r\n");
}
```

这会产生以下输出：

Degrees    Degrees
Fahrenheit Celsius
32         .000
52         11.111
72         22.222
92         33.333
112        44.444
132        55.556
152        66.667
172        77.778
192        88.889
212        100.000

第 7 章将详细探讨脚本段。

## 声明

与脚本段类似，*声明*包含 Java 语言语句，但有一个很大的不同：脚本段代码成为 `_jspService()` 方法的一部分，而声明代码则被合并到生成的源文件中，位于 `_jspService()` 方法*之外*。声明部分的语法是

```
<%! 语句; [语句; ...] %>
```

声明部分可用于声明类或实例变量、方法或内部类。与脚本段不同，它们无法访问下一节中描述的隐式对象。例如，如果你使用声明部分来声明一个需要使用请求对象的方法，你需要将该对象作为参数传递给方法。

以下展示了使用声明部分的 JSP 页面示例：

```
<%@ page
    errorPage="ErrorPage.jsp"
    import="java.io.*,java.util.*"
%>

<%
    Enumeration enames;
    Map map;
    String title;

    // 打印请求头

    map = new TreeMap();
    enames = request.getHeaderNames();
    while (enames.hasMoreElements()) {
        String name = (String) enames.nextElement();
        String value = request.getHeader(name);
        map.put(name, value);
    }
    printTable(out, map, "Request Headers");

    // 打印会话属性

    map = new TreeMap();
    enames = session.getAttributeNames();
    while (enames.hasMoreElements()) {
        String name = (String) enames.nextElement();
        String value = "" + session.getAttribute(name);
        map.put(name, value);
    }
    printTable(out, map, "Session Attributes");

%>

<%-- 定义一个打印表格的方法 --%>

<%!
    private static void printTable
        (Writer writer, Map map, String title)
    {
        // 获取输出流

        PrintWriter out = new PrintWriter(writer);

        // 写标题行

        out.println("<TABLE BORDER=1 CELLPADDING=3>");
        out.println
            ("<TR><TH COLSPAN=2>" + title + "</TH></TR>");

        // 写表格行

        Iterator imap = map.entrySet().iterator();
        while (imap.hasNext()) {
            Map.Entry entry = (Map.Entry) imap.next();
            String key = (String) entry.getKey();
            String value = (String) entry.getValue();
            out.println("<TR>");
            out.println("<TD>" + key + "</TD>");
            out.println("<TD>" + value + "</TD>");
            out.println("</TR>");
        }

        // 写页脚行

        out.println("</TABLE>");
        out.println("<P>");
    }
%>
```

此 JSP 页面收集两个表格的数据：传递给请求对象的 HTTP 头和会话属性。每个表格的期望输出是一个格式良好的 HTML 表格。当然，可以在遍历数据行时创建表格，但这将需要复制格式化代码。相反，使用了一个名为 printTable() 的私有静态方法，将输出流的引用、包含键/值对的 Map 对象和表格标题传递给它。

第 8 章将更详细地讨论声明。



## 隐式对象

虽然脚本段、表达式和HTML模板数据都会被合并到 `_jspService()` 方法中，但JSP容器会编写该方法本身的骨架，初始化页面上下文以及几个有用的变量。这些变量在脚本段和表达式（但不包括声明）中隐式可用。它们可以像任何其他变量一样被访问，但不必先进行声明。例如，传递给 `_jspService()` 的 `HttpServletRequest` 对象在名为 `request` 的变量下可用，如下面的脚本段所示：

```
<%
    String accountNumber = request.getParameter("acct");
    if (accountNumber == null) {
        // ... 处理缺失的账户号问题
    }
%>
```

表6-2提供了隐式变量的完整列表。

| 变量名 | 值 |
| :--- | :--- |
| `request` | 正在被处理的 `ServletRequest` 或 `HttpServletRequest`。 |
| `response` | 将接收生成的HTML输出的 `ServletResponse` 或 `HttpServletResponse`。 |
| `pageContext` | 此页面的 `PageContext` 对象。此对象是页面、请求、会话和应用程序的属性数据的中央存储库。 |
| `session` | 如果JSP页面使用了 `HttpSession`，它在此处以 `session` 为名可用。 |
| `application` | Servlet上下文对象。 |
| `out` | 用于生成输出HTML的字符输出流。 |
| `config` | 此Servlet上下文的 `ServletConfig` 对象。 |
| `page` | 对JSP页面本身的引用。 |
| `exception` | 导致错误页面被调用的未捕获异常。此变量仅对 `isErrorPage="true"` 的页面可用。 |

**表6-2.** *隐式变量*

可以通过标签库创建额外的隐式变量。有关此主题的讨论，请参见第11章。

## 标准动作

动作是创建、修改或使用其他对象的高级JSP元素。与指令和脚本元素不同，动作使用严格的XML语法进行编码：

```
<tagname [attr="value" attr="value" ...]> ... </tagname>
```

或者，如果动作没有主体，则使用简写形式：

```
<tagname [attr="value" attr="value" ...] />
```

XML语法要求如下：

+   ■ 每个标签必须有匹配的结束标签，或使用前面所示的简写形式 `/>`。
+   ■ 属性值必须放在引号内。
+   ■ 标签必须正确嵌套：`<A><B> ... </B></A>` 是合法的，但 `<A><B> ... </A></B>` 是非法的。

所有符合JSP 1.1的环境中都提供了七种标准动作。这些动作在第15章中有详细描述。表6-3概述了语法。

| 标签名 | 描述 |
| :--- | :--- |
| `<jsp:useBean>` | 声明一个Java Bean实例并将其与变量名关联。语法是 `<jsp:useBean id="name" [ type="type" ] [ class="class" ] [ beanName="beanName" ] [ scope="page\|request\|session\|application" ]> ... </jsp:useBean>` |
| `<jsp:setProperty>` | 设置之前通过 `<jsp:useBean>` 声明的Bean的一个或多个属性的值。语法是 `<jsp:setProperty name="id" prop-expression/>`，其中 *prop-expression* 是以下之一：`property="*"`，`property="propName"`，`property="propName" param="parameterName"`，`property="propName" value="value"`，`property="propName" value=<%= expression %>>` |
| `<jsp:getProperty>` | 返回Bean的指定属性的值。语法是 `<jsp:getProperty name="id" property="name" />` |
| `<jsp:include>` | 调用另一个资源并将其输出流与JSP页面输出流合并。语法是 `<jsp:include page="URL" flush="true" />`，或者，如果需要传递参数：`<jsp:include page="URL" flush="true"> <jsp:param ... /> <jsp:param ... /> ... <jsp:param ... /> </jsp:include>` |
| `<jsp:forward>` | 将此HTTP请求转发给另一个JSP页面或Servlet进行处理。语法是 `<jsp:forward page="URL" />`，或者，如果需要传递参数：`<jsp:forward page="URL"> <jsp:param ... /> <jsp:param ... /> ... <jsp:param ... /> </jsp:forward>` |
| `<jsp:param>` | 将一个值绑定到一个名称，并将此绑定传递给通过 `<jsp:include>` 或 `<jsp:forward>` 调用的另一个资源。语法是 `<jsp:param name="name" value="value" />` |
| `<jsp:plugin>` | 用于为下载Java插件生成适当的HTML链接：`<jsp:plugin type="bean\|applet" code="objectCode" codebase="objectCodebase" { align="alignment" } { archive="archiveList" } { height="height" } { hspace="hspace" } { jreversion="jreversion" } { name="componentName" } { vspace="vspace" } { width="width" } { nspluginurl="url" } { iepluginurl="url" } > { <jsp:params> { <jsp:param name="name" value="value" /> }+ </jsp:params> } </jsp:plugin>` |

**表6-3.** *标准动作*

# 第6章：JSP语法与语义

77

## 标签扩展

除了表6-3中列出的标准动作外，JSP作者还可以编写自定义标签来扩展JSP的功能。第11章专门讨论标签扩展。

## 一个完整的例子

本章以一个包含此处介绍的所有元素的JSP页面示例结束。该页面名为 `Echo.jsp`。其唯一功能是将一个包含浏览器发送的HTTP请求头的HTML表格返回给客户端浏览器。代码清单如下所示：

```
<%@ page import="java.util.*" %>

<HTML>

<HEAD>
<TITLE>Echo</TITLE>
<STYLE>
<jsp:include page="style.css" flush="true"/>
</STYLE>
</HEAD>

<BODY>
<H3>HTTP Request Headers Received</H3>
<TABLE BORDER="1" CELLPADDING="4" CELLSPACING="0">
<%
    Enumeration eNames = request.getHeaderNames();
    while (eNames.hasMoreElements()) {
        String name = (String) eNames.nextElement();
        String value = normalize(request.getHeader(name));
%>
    <TR> <TD><%= name %></TD> <TD><%= value %></TD> </TR>
<%
    }
%>
</TABLE>
</BODY>
</HTML>
<%!
    private String normalize(String value)
    {
        StringBuffer sb = new StringBuffer();
        for (int i = 0; i < value.length(); i++) {
            char c = value.charAt(i);
            sb.append(c);
            if (c == ';')
                sb.append("<BR>");
        }
        return sb.toString();
    }
%>
```

当 `Echo.jsp` 首次被调用时，它创建了以下Java源代码：

```java
package Chap_00030_00035;

import javax.servlet.*;
import javax.servlet.http.*;
import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.PrintWriter;
import java.io.IOException;
import java.io.FileInputStream;
import java.io.ObjectInputStream;
import java.util.Vector;
import org.apache.jasper.runtime.*;
import java.beans.*;
import org.apache.jasper.JasperException;
import java.util.*;


public class
    _0002fChap_00030_00035_0002fEcho_0002ejspEcho_jsp_5
    extends HttpJspBase
{
    // begin [file="Echo.jsp";from=(27,3);to=(39,0)]
    private String normalize(String value)
    {
        StringBuffer sb = new StringBuffer();
        for (int i = 0; i < value.length(); i++) {
            char c = value.charAt(i);
            sb.append(c);
            if (c == ';')
                sb.append("<BR>");
        }
        return sb.toString();
    }
    // end

    static {
    }

    public
        _0002fChap_00030_00035_0002fEcho_0002ejspEcho_jsp_5()
    {
    }

    private static boolean _jspx_inited = false;

    public final void _jspx_init() throws JasperException
    {
    }

    public void _jspService(
            HttpServletRequest request,
            HttpServletResponse response)
        throws IOException, ServletException
    {
        JspFactory _jspxFactory = null;
        PageContext pageContext = null;
        HttpSession session = null;
        ServletContext application = null;
        ServletConfig config = null;
        JspWriter out = null;
        Object page = this;
        String _value = null;
        try {

            if (_jspx_inited == false) {
                _jspx_init();
                _jspx_inited = true;
            }

            _jspxFactory = JspFactory.getDefaultFactory();

            response.setContentType("text/html");
            pageContext = _jspxFactory.getPageContext
                (this, request, response, "", true, 8192, true);

            application = pageContext.getServletContext();
            config = pageContext.getServletConfig();
            session = pageContext.getSession();
            out = pageContext.getOut();

            // HTML
            // begin [file="Echo.jsp";from=(0,32);to=(7,0)]
            out.write("\r\n\r\n");
            out.write("<HTML>\r\n\r\n");
            out.write("<HEAD>\r\n");
            out.write("<TITLE>Echo</TITLE>\r\n");
            out.write("<STYLE>\r\n");
            // end

            // begin [file="Echo.jsp";from=(7,0);to=(7,44)]
            {
                String _jspx_qStr = "";
                out.flush();
                pageContext.include("style.css" + _jspx_qStr);
            }
            // end

            // HTML
            // begin [file="Echo.jsp";from=(7,44);to=(14,0)]
            out.write("\r\n");
            out.write("</STYLE>\r\n");
            out.write("</HEAD>\r\n\r\n");
            out.write("<BODY>\r\n");
            out.write("<H3>HTTP Request Headers Received");
            out.write("</H3>\r\n");
            out.write("<TABLE BORDER=\"1\"");
            out.write(" CELLPADDING=\"4\"");
            out.write(" CELLSPACING=\"0\">\r\n");
            // end

            // begin [file="Echo.jsp";from=(14,2);to=(19,0)]
            Enumeration eNames = request.getHeaderNames();
            while (eNames.hasMoreElements()) {
```

## 页面指令

JSP页面以页面指令开头，表明该页面使用`java.util`包：

```
<%@ page import="java.util.*" %>
```

该指令会出现在生成的Servlet源代码中导入类列表的末尾：

```
...
import org.apache.jasper.runtime.*;
import java.beans.*;
import org.apache.jasper.JasperException;
import java.util.*;
```

## `<jsp:include>`动作

页面使用样式表来设置输出的外观和风格。该样式表通过`<jsp:include>`动作引入：

```
<STYLE>
<jsp:include page="style.css" flush="true"/>
</STYLE>
```

`<jsp:include>`动作导致以下样式表在请求时被读取：

```
body {
    color: #000000;
    background-color: #FEFEF2;
    font: Verdana 9pt;
};
```

## 脚本片段

页面上有两个脚本片段，HTML模板数据位于它们之前、之间和之后。HTML数据

```
<HTML>

<HEAD>
<TITLE>Echo</TITLE>
...
```

通过write语句原样传递：

```
out.write("\r\n");
out.write("<HTML>\r\n\r\n");
out.write("<HEAD>\r\n ");
out.write("<TITLE>Echo</TITLE>\r\n ");
...
```

然后第一个脚本片段被直接复制到Servlet中：

```
Enumeration eNames = request.getHeaderNames();
while (eNames.hasMoreElements()) {
    String name = (String) eNames.nextElement();
    String value = normalize(request.getHeader(name));
}
```

注意代码片段的第二行有一个未闭合的花括号。对应的闭合花括号由第二个脚本片段提供。

## JSP表达式

在每次循环迭代中，脚本片段从请求对象中提取一个头部名称和头部值。页面作者没有使用`out.write()`打印这些值，而是切换回HTML模式并使用JSP表达式标签：

```
%>
<TR> <TD><%= name %></TD> <TD><%= value %></TD> </TR>
<%
```

这会生成以下Servlet代码：

```
// HTML
// begin [file="Echo.jsp";from=(19,2);to=(20,12)]
out.write("\r\n <TR> <TD>");
// end

// begin [file="Echo.jsp";from=(20,15);to=(20,21)]
out.print( name );
// end

// HTML
// begin [file="Echo.jsp";from=(20,23);to=(20,33)]
out.write("</TD> <TD>");
// end

// begin [file="Echo.jsp";from=(20,36);to=(20,43)]
out.print( value );
// end

// HTML
// begin [file="Echo.jsp";from=(20,45);to=(21,0)]
out.write("</TD> </TR>\r\n");
// end
```

## 声明

作为列表的头部值可能非常长，导致表格宽度失真。你可以通过扫描头部值中的分号，并在发现分号的地方插入`<BR>`标签来解决这个问题。这个功能由名为`normalize()`的方法完成，该方法位于JSP文件的末尾：

```
<%!
    private String normalize(String value)
    {
        StringBuffer sb = new StringBuffer();
        for (int i = 0; i < value.length(); i++) {
            char c = value.charAt(i);
            sb.append(c);
            if (c == ';')
                sb.append("<BR>");
        }
        return sb.toString();
    }
%>
```

与两个脚本片段的情况一样，声明代码被原样复制到生成的Servlet中，只是它没有被放置在`_jspService()`方法内部。相反，它被写入类块中，但在任何其他方法之外，靠近Servlet的开头：

```
// begin [file="Echo.jsp";from=(27,3);to=(39,0)]
private String normalize(String value)
{
    StringBuffer sb = new StringBuffer();
    for (int i = 0; i < value.length(); i++) {
        char c = value.charAt(i);
        sb.append(c);
        if (c == ';')
            sb.append("<BR>");
    }
    return sb.toString();
}
// end
```

最终输出如图6-1所示。

# 第7章：表达式和脚本片段

上一章概述了JSP的语法和语义。虽然语法不难学习，但掌握它并不能教会你需要知道的一切。理解JSP需要构建其操作的思维模型——Java源代码如何以及何时生成，类何时编译和加载。

在本章中，通过探索两个脚本元素：表达式和脚本片段，来阐明该思维模型的一部分。你将看到JSP容器如何组合模板文本和JSP脚本元素来生成处理用户请求的Java方法。还将探讨JSP页面如何访问其使用的Web环境，以及如何传递其结果。

## 表达式

JSP*表达式*就是JSP页面中的一个Java^1^语言表达式，通过分隔符`<%=`和`%>`与周围的HTML区分开来，如下所示：

`<%= expression %>`

例如，表达式可以是一个基本的数值：

```
<B>Simple math:</B> 2 + 2 = <%= 2 + 2 %>
```

产生输出：

**Simple math:** `2 + 2 = 4`

或者是一个更复杂的涉及方法调用的表达式：

```
The Java virtual machine vendor is
<em><%= System.getProperty("java.vm.vendor") %></em>
```

产生输出：

The Java virtual machine vendor is *Sun Microsystems Inc.*.

> 1 理论上，JSP页面可以用其他语言编写，正如JSP规范所设想的那样。在撰写本文时，除了一些实验性例外，Java是唯一支持的语言。这就是为什么这项技术被称为JavaServer Pages（JSP），而不是语言无关服务器页面（LISP）或任何旧语言服务器页面（AOLSP）。

表达式可以创建新对象并操作它们。这段代码创建一个`Date`对象并将其传递给一个新的`SimpleDateFormat`对象的`format()`方法：

```
Today is
<%=
    new java.text.SimpleDateFormat("MMMM d, yyyy")
    .format(new java.util.Date())
%>
```

产生（当然是在相应的日期）：

Today is June 28, 2001

`<%`和`%>`分隔符之间的Java表达式可以任意复杂，唯一的要求是它必须能够被求值为一个`java.util.String`，可以直接求值，也可以通过调用其`toString()`方法或`String.valueOf()`方法。

> **注意** 表达式不能以分号结尾。它们必须完全由赋值语句中等号和结尾分号之间可以合法出现的内容组成。

## 脚本片段

脚本片段是嵌入在HTML页面中的一组Java编程语句。这些语句通过放置在`<%`和`%>`标记之间与周围的HTML区分开来，如下所示：

```
<% statement; [statement; ...] %>
```

`<%`之后和`%>`之前允许有空白字符，因此前面的脚本片段也可以写成：

```
<%
statement;
[statement; ...]
%>
```

这里有一个使用脚本片段生成ASCII字符表的JSP页面示例：

```
<HTML>
<BODY>
<CENTER>
```



## ASCII 表

```html
<H3>ASCII Table</H3>
<TABLE BORDER="0" CELLPADDING="0" CELLSPACING="0">
<%
    StringBuffer sb = new StringBuffer();
    sb.append("<TR>");
    sb.append("<TH WIDTH=40>&nbsp;</TH>");
    for (int col = 0; col < 16; col++) {
        sb.append("<TH>");
        sb.append(Integer.toHexString(col));
        sb.append("</TH>");
    }
    sb.append("</TR>");
    for (int row = 0; row < 16; row++) {
        sb.append("<TR>");
        sb.append("<TH>");
        sb.append(Integer.toHexString(row));
        sb.append("</TH>");
        for (int col = 0; col < 16; col++) {
            char c = (char) (row * 16 + col);
            sb.append("<TD WIDTH=32 ALIGN=CENTER>");
            sb.append(c);
            sb.append("</TD>");
        }
        sb.append("</TR>");
    }
    out.println(sb);
%>
</TABLE>
</CENTER>
</BODY>
</HTML>
```

有五行 HTML 代码，接着是脚本片段的开启定界符 `<%`，若干行 Java 代码，脚本片段的结束定界符 `%>`，然后是用于关闭文档的 HTML 行。当被调用时，该页面会产生如图 7-1 所示的输出。下一节将描述 JSP 容器如何处理这些脚本元素。

## JSP 容器对表达式和脚本片段的处理

当遇到一个新的或修改过的 JSP 页面时，JSP 容器会解析它，并为其创建一个等效的 Java Servlet² 的源代码。页面中发现的表达式、脚本片段和 HTML 模板数据被 JSP 容器用来创建一个名为 `_jspService()` 的方法的 Java 源代码。这个方法对应于 Servlet 的 `service()` 方法，或者更常用的 `doGet()` 和 `doPost()` 方法。`_jspService()` 是由容器自动生成的。JSP 作者不能显式地定义它。

² Servlet 在第 4 章中有详细讨论。

生成的 `_jspService()` 方法由多达三种类型的语句组成，具体取决于 JSP 页面的内容：

-   处理 HTML 模板数据和表达式的代码
-   任何脚本片段的内容
-   容器生成的初始化和退出代码

让我们逐一研究这些内容，并了解它们是如何被处理的。

### HTML 模板数据和表达式

JSP 页面中不在 JSP 元素（指令、表达式、脚本片段或动作）内的任何字符都被视为固定 HTML 模板的一部分。JSP 容器会创建 `out.write()` 或 `out.print()` 语句，将这些字符写入响应输出流。例如，这段代码

```html
<LI>Cash and Marketable Securities
```

会被转换为：

```java
out.write("<LI>Cash and Marketable Securities\r\n");
```

如果 HTML 模板需要包含任何字面量 `<%` 字符串，必须对其进行特殊处理以避免混淆 JSP 容器。JSP 1.1 规范指出，可以通过写 `<\%` 而不是 `<%` 来实现这一点。JSP 容器会生成代码，以便在输出流中写入预期的 `<%`。

> JSP 容器通常会为每个不间断的固定 HTML 数据段生成一个长长的 `out.write()` 语句。本书中的示例为了可读性，将长字符串拆分为多个 `out.write()` 语句。

除了固定的 HTML 数据，模板还可以包含在运行时求值并用 `out.write()` 语句打印的 JSP 表达式。表达式将在下一节中讨论。

### 脚本片段内容

在 `<%` 和 `%>` 标签之间找到的任何内容都会被逐字复制到 `_jspService()` 方法中。因此，JSP 页面中的这些行

```html
<TABLE BORDER=0>
<TR><TH>Celsius</TH><TH>Fahrenheit</TH></TR>
<%
```

```java
for (int c = 0; c <= 100; c += 10) {
    int f = 32 + 9*c/5;
    out.print("<TR><TD>" + c + "</TD>");
    out.print("<TD>" + f + "</TD></TR>");
}
%>
</TABLE>
```

会被 JSP 容器转换为 `_jspService()` 方法中的以下行：

```java
// HTML
// begin [file="c2f.jsp";from=(0,0);to=(2,0)]
out.write("<TABLE BORDER=0>\r\n");
out.write("<TR>");
out.write("<TH>Celsius</TH>");
out.write("<TH>Fahrenheit</TH>");
out.write("</TR>\r\n");
// end
// begin [file="c2f.jsp";from=(2,2);to=(8,0)]

for (int c = 0; c <= 100; c += 10) {
    int f = 32 + 9*c/5;
    out.print("<TR><TD>" + c + "</TD>");
    out.print("<TD>" + f + "</TD></TR>");
}
// end
// HTML
// begin [file="c2f.jsp";from=(8,2);to=(10,0)]
out.write("\r\n</TABLE>\r\n");
// end
```

表格的 HTML 标记出现在 `out.write()` 语句中，而脚本片段的内容则原封不动地出现在方法体中。如果页面中有多个脚本片段，它们将按出现的顺序复制。因此，编写这段代码

```java
<%
    for (int i = 0; i < 10; i++) {
        out.println(i);
    }
%>
```

和这段代码

```java
<%
    for (int i = 0; i < 10; i++) { %>
<%
    out.println(i); %>
<%
} %>
```

在功能上没有区别，只是后者会生成几个换行符（因为它们在技术上被视为固定的 HTML 数据）。由于多个脚本片段被连接并放入同一个方法中，因此可以在一个脚本片段中开始语法单元，并在另一个脚本片段中完成，如 `for` 语句中的开闭花括号所示。这也意味着在任何脚本片段中定义的变量都被视为 `_jspService()` 方法的局部变量，并且它们的值会从一个脚本片段或表达式延续到下一个。

### 容器生成的初始化和退出代码

除了 JSP 页面作者编写的代码外，`_jspService()` 的开头和结尾还有一些用于初始化和释放方法中所需对象的语句。生成的确切代码取决于具体实现，并且因 JSP 容器供应商而异。以先前给出的摄氏度到华氏度的例子为例，Tomcat 会生成以下初始化和退出代码：

```java
public void _jspService(
        HttpServletRequest request,
        HttpServletResponse response)
    throws IOException, ServletException
{
    JspFactory _jspxFactory = null;
    PageContext pageContext = null;
    HttpSession session = null;
    ServletContext application = null;
    ServletConfig config = null;
    JspWriter out = null;
    Object page = this;
    String _value = null;
    try {
        _jspxFactory = JspFactory.getDefaultFactory();
        response.setContentType("text/html;charset=8859_1");
        pageContext = _jspxFactory.getPageContext
            (this, request, response, "", true, 8192, true);
        application = pageContext.getServletContext();
        config = pageContext.getServletConfig();
        session = pageContext.getSession();
        out = pageContext.getOut();

        // ... your code appears here ...

    }
    catch (Exception ex) {
        if (out.getBufferSize() != 0)
            out.clearBuffer();
        pageContext.handlePageException(ex);
    }
    finally {
        out.flush();
        _jspxFactory.releasePageContext(pageContext);
    }
}
```

可以看到，在添加 JSP 作者的代码之前，创建了许多对象。这些对象的含义是下一节的主题。

### 隐式对象和 JSP 环境

在 JSP 页面中编写的脚本片段和表达式并非独立的完整程序——它们需要一个运行环境。JSP 容器提供此环境，并通过所谓的 *隐式对象* 使其对页面作者可用。这些对象由容器生成的语句在 `_jspService()` 方法的开头创建，并被赋予在所有 JSP 页面中都相同的预定名称。共有九个这样的对象，如表 7-1 所列。

| 对象 | 描述 |
| :--- | :--- |
| `request` | 传递给 `_jspService()` 的 `HttpServletRequest` 对象。 |
| `response` | 传递给 `_jspService()` 的 `HttpServletResponse` 对象。 |
| `pageContext` | 用于访问页面、请求、会话或应用程序属性的手段。 |
| `session` | 当前的 `HttpSession` 对象（如果存在）。 |
| `application` | Servlet 上下文对象。 |
| `out` | `JspWriter` 响应输出流对象。 |
| `config` | Servlet 配置对象。 |
| `page` | 指向当前 JSP 类实例本身的引用。 |
| `exception` | 未捕获的异常（仅在错误页面中有效）。 |

**表 7-1.** 在脚本片段和表达式中可用的隐式对象

这些变量可以通过使用它们的预定名称来访问，就像任何其他变量一样。本章示例中已经使用了其中一个变量——`JspWriter out` 变量：

```java
<%
out.println("<B>out</B> is an <I>");
out.println(out.getClass().getName());
out.println("</I> object.");
%>
```

在 Tomcat 下运行时产生：

**out** 是一个 `org.apache.jasper.runtime.JspWriterImpl` 对象。

当然，这是供应商特定的。JRun 3.0 会生成：

**out** 是一个 `allaire.jrun.jsp.JRunJspWriter` 对象。

JSP 隐式对象提供了处理 HTTP 请求的上下文。以下各节将详细探讨这些对象中的每一个。

### Request

`request` 变量包含对传递到生成的 `_jspService()` 方法第一个参数中的 `HttpServletRequest` 对象的引用。这个对象

该对象封装了Web浏览器或其他客户端生成的HTTP请求的详细信息——包括其参数、属性、头部信息和数据。其一些更有用的方法³列于表7-2。

## Response

`response`变量提供了访问HTTP事务另一端的方式。此对象封装了返回给HTTP客户端的输出，使页面作者能够设置响应头和状态码。它还包含访问响应输出流的方法，但JSP规范禁止直接访问此流。所有JSP响应输出都必须使用`out`隐式变量写入。`HttpServletResponse`对象提供的方法包括表7-3中所列的方法。

**表 7-2.** `request` 对象的一些有用方法

| 方法 | 描述 |
| :--- | :--- |
| `String getHeader(String name)` | 返回指定HTTP头部的值，如果请求中不存在该头部则返回 `null`。 |
| `Enumeration getHeaderNames()` | 返回请求中所有HTTP头部的名称枚举。 |
| `String getParameter(String name)` | 给定单值表单参数的名称，返回其值。 |
| `Enumeration getParameterNames()` | 返回传递给此请求的所有表单参数名称的枚举。 |
| `HttpSession getSession(boolean create)` | 返回当前的 `HttpSession` 对象。如果不存在，则根据 `create` 标志创建一个新会话或返回 `null`。 |

³ javax.servlet.http.HttpServletRequest 以及 Servlet 2.2 API 中所有其他类的完整描述可在附录A中找到。

**表 7-3.** `response` 对象的一些有用方法

| 方法 | 描述 |
|---|---|
| boolean isCommitted() | 返回一个标志，指示HTTP响应是否已经返回给客户端。 |
| void setHeader(String name, String value) | 设置具有指定名称和值的HTTP头部。 |
| void setStatus(int sc) | 将HTTP状态设置为指定值。 |

**100** JSP: The Complete Reference

## PageContext

JSP代码在环境层次结构中运行，如图7-2所示。例如，单个HTTP请求可能由多个JSP页面提供服务：一个生成标题信息，另一个生成详细输出。同样，多个HTTP请求可能属于一个更大的HTTP会话，该会话从登录请求开始，经过一些用户选择请求，然后将工作提交给数据库。最后，servlet上下文中的所有HTTP会话可能共享一个连接池或其他公共对象。此层次结构中的每一层都可以拥有仅在该级别适用的属性。JSP规范提供了一个PageContext对象，用于跟踪四个级别的属性：

- JSP页面
- HTTP请求
- HTTP会话
- 整个应用程序

`PageContext`对象在`_jspService()`方法开始时自动初始化并分配给名为`pageContext`的变量。此对象提供在四个级别中的每一个级别上搜索和更新属性的能力，如表7-4所述。它还提供将请求转发给其他资源和包含其他资源输出的方法。

**表 7-4.** `pageContext` 对象的一些有用方法

| 方法 | 描述 |
|---|---|
| `Object findAttribute(String name)` | 按页面、请求、会话和应用程序的顺序，搜索具有指定名称的属性对象，返回找到的第一个对象，如果未找到则返回null。 |
| `Object getAttribute(String name, int scope)` | 返回给定范围中具有指定名称的属性对象。`scope`参数值应从`PageContext`类中提供的`PAGE_CONTEXT`、`REQUEST_CONTEXT`、`SESSION_CONTEXT`和`APPLICATION_CONTEXT`常量中选择。 |
| `void removeAttribute(String name, int scope)` | 移除给定范围中具有指定名称的属性对象。 |
| `void setAttribute(String name, Object value, int scope)` | 在给定范围内将对象存储为命名属性。`scope`参数值应从`PageContext`类中定义的`PAGE_CONTEXT`、`REQUEST_CONTEXT`、`SESSION_CONTEXT`和`APPLICATION_CONTEXT`常量中选择。 |

## Session

HTTP是一种无状态协议，这意味着它不会在从一个请求到下一个请求之间记住任何关于先前请求的信息。然而，Web应用程序经常涉及多个请求。例如，应用程序可能以某种用户身份识别和验证开始，这些信息必须传播到其他几个Web页面。这类应用程序所需的连续性必须由Web服务器以外的东西提供。

可以采取几种方法来满足这一需求，具体取决于应用程序的要求。第14章详细探讨了多种替代方案，包括：

- 隐藏字段
- Cookies
- URL重写
- HTTP会话

这里感兴趣的是最后一项。`HttpSession`是一个与单个Web浏览器会话关联的、类似`Hashtable`的对象。它在HTTP请求之间持续存在，可以存储任何类型的命名对象。默认情况下，JSP容器在`_jspService()`方法开始时创建一个`HttpSession`对象或访问当前活动的会话。此对象被分配给一个名为`session`的变量。

如果不需要在请求之间保留对象，可以通过在`page`指令中指定`session="false"`来关闭自动会话创建。这样做可以通过减少servlet引擎必须跟踪的对象数量来提高性能。由于会话会一直持续到超时（通常30分钟后）或被显式失效，因此对性能的影响可能相当大。

表7-5概述了会话对象中几种有用的方法。

**表 7-5.** `session` 对象的一些有用方法

| 方法 | 描述 |
| :--- | :--- |
| `Object getAttribute(String name)` | 如果会话中存在具有指定名称的对象，则返回该对象。 |
| `Enumeration getAttributeNames()` | 返回存储在会话中的所有对象名称的枚举。 |
| `String getId()` | 返回唯一的会话ID。客户端（Web浏览器）必须在请求之间存储此ID，并将其传回JSP容器以识别需要哪个会话。 |
| int getMaxInactiveInterval() | 返回会话在用户请求之间保持活动的最大秒数。如果超过该时间长度没有活动，JSP容器将关闭会话。 |
| void invalidate() | 关闭会话并解除其所有对象的绑定。 |
| void setAttribute(String name, Object value) | 在会话中以指定名称存储一个对象。 |

请记住，pageContext对象也可以像使用session.getAttribute()和session.setAttribute()方法一样，用于获取和设置会话中的属性。

## Application

application隐式对象封装了Web应用程序中所有servlet、JSP页面、HTML页面和其他资源集合的视图。此对象实现了javax.servlet.ServletContext接口，并在_jspService()方法开始时自动构建。它提供有关服务器版本、任何应用程序范围初始化参数以及应用程序内资源绝对路径的信息。此对象还提供了记录消息的方法。表7-6描述了其一些更有用的方法。

**表 7-6.** `application` 对象的一些有用方法

| 方法 | 描述 |
| :--- | :--- |
| Enumeration getAttributeNames() | 返回存储在servlet上下文中的所有对象名称的枚举。 |
| Object getAttribute(String name) | 返回使用应用程序的setAttribute()方法存储的、具有指定名称的对象。 |



| 方法 | 描述 |
| :--- | :--- |
| String getInitParameter(String *name*) | 返回指定应用程序范围初始化参数的值。 |
| Enumeration getInitParameterNames() | 返回所有应用程序范围初始化参数名称的枚举。 |
| String getRealPath(String *path*) | 在可能的情况下，将Web应用程序上下文中的路径转换为文件系统中的绝对路径。 |
| URL getResource(String *path*) | 返回映射到应用程序中指定路径的URL（如果存在）。路径必须以"/"开头，并且是相对于应用程序根目录的。 |
| InputStream getResourceAsStream(String *path*) | 操作类似于getResource()，但返回一个指向结果URL的打开的输入流。 |
| void log(String *msg*) | 将消息写入与此应用程序关联的日志文件。 |

**表 7-6.** *application对象的一些有用方法（续）*

与`page`、`request`和`session`隐式对象一样，`application`对象的属性可以通过`pageContext`对象中的方法来操作。初始化参数将在本章的后面部分讨论。

## Out

JSP页面的全部目的就是产生一些输出，并将其发送回socket连接另一端的用户。正如本章前面所见，固定的HTML模板数据和JSP表达式是通过自动生成的`out.write()`和`out.print()`方法调用写入的。`out`变量在`_jspService()`方法早期就用一个指向`javax.servlet.jsp.JspWriter`对象的引用进行了初始化。你可以让所有输出都以这种方式生成，也可以在脚本中显式地写入`out`对象。因此，以下JSP页面

```
<%
    String[] colors = {"red", "green", "blue"};
    for (int i = 0; i < colors.length; i++) {
%>
<%= colors[i] %> <P>
<%
    }
%>
```

在功能上等同于这个：

```
<%
String[] colors = {"red", "green", "blue"};
for (int i = 0; i < colors.length; i++) {
    out.println(colors[i] + " <P>");
}
%>
```

除了所有`java.io.Writer`对象共有的`write()`方法外，`out`对象还提供了用于查询和操作输出缓冲区的方法，如表7-7所示。

| 方法 | 描述 |
| :--- | :--- |
| void flush() | 强制将缓冲数据写入输出流。 |
| int getBufferSize() | 返回输出缓冲区的大小（以字节为单位），如果写入器是无缓冲的，则返回0。 |
| int getRemaining() | 返回缓冲区溢出前剩余的字节数。 |
| void print(type value) | 多种用于写入指定基本类型或对象类型值的方法。末尾不添加换行符。 |
| void println(type value) | 类似于print()，但在末尾添加一个换行符。 |

**表 7-7.** out对象的一些有用方法

## Config

除了通过`application`对象提供的应用程序范围初始化参数外，单个servlet映射（因此也包括JSP页面）也可以有初始化参数。`config`隐式对象提供了访问这些参数、servlet上下文（`application`）和servlet名称的方法，如表7-8所示。

## Page

`page`隐式对象是一个包含对当前servlet实例引用的变量，本质上只是`this`变量的一个别名。这个对象通常对JSP页面作者来说没什么用。

## Exception

隐式`exception`变量所引用的对象是`java.lang.Throwable`的任何实例，它已被JSP页面中的`catch`块抛出但未被捕获。`exception`变量仅在`<%@ page %>`指令具有`isErrorPage="true"`属性时有效。此属性将在第10章中更详细地讨论。

| 方法 | 描述 |
| :--- | :--- |
| String getInitParameter(String *name*) | 返回指定servlet初始化参数的值，如果命名参数不存在，则返回null。 |
| Enumeration getInitParameterNames() | 返回此servlet所有初始化参数名称的列表。 |
| ServletContext getServletContext() | 返回对servlet上下文的引用（与`application`隐式变量相同）。 |
| String getServletName() | 返回生成的servlet的名称。 |

**表 7-8.** `config`对象的一些有用方法

## 初始化参数

初始化参数是JSP页面可以读取的外部名称/值对。它们可以像字符串常量一样使用，但有一个额外的好处，即可以在不需要重新编译使用它们的程序的情况下进行修改。这使得初始化参数特别适用于存储安装和配置数据，例如HTTP代理服务器名称、应用程序配色方案或安装目录名称。

这些参数可以在单个JSP和servlet级别指定，也可以为应用程序中的所有JSP页面指定。在这两种情况下，初始化参数都在应用程序的`web.xml`文件中声明。对于JSP和servlet级别的访问，这是通过向相应的`<servlet>`元素添加一个或多个`<init-param>`元素来实现的，如下所示：

```
<servlet>
    <servlet-name>Food</servlet-name>
    <jsp-file>/Chap07/examples/Food.jsp</jsp-file>

    <init-param>
        <param-name>DRIVER_NAME</param-name>
        <param-value>sun.jdbc.odbc.JdbcOdbcDriver</param-value>
    </init-param>

    <init-param>
        <param-name>DATABASE_URL</param-name>
        <param-value>jdbc:odbc:usda</param-value>
    </init-param>
</servlet>
```

在这个例子中，`Food.jsp`是一个访问营养信息数据库的JSP页面。它没有包含用于JDBC驱动程序名称和数据库URL的硬编码值，而是通过使用`getInitParameter()`方法从初始化参数中获取这些值：

```
String driverName = getInitParameter("DRIVER_NAME");
if (driverName == null)
    throw new ServletException
        ("No DRIVER_NAME parameter was specified");

String databaseURL = getInitParameter("DATABASE_URL");
if (databaseURL == null)
    throw new ServletException
        ("No DATABASE_URL parameter was specified");

Class.forName(driverName);
Connection con = DriverManager.getConnection(databaseURL);
```

数据库访问参数可能在Web应用程序的多个地方都需要。与其在web.xml文件中有重复的值，不如在应用程序级别指定常用值。这是通过`<context-param>`元素完成的。访问这些值的JSP代码几乎相同，只是调用了application对象的`getInitParameter()`方法。

## 总结

JSP页面提供了两种在处理请求时包含Java代码的方法：表达式和脚本。JSP表达式就是产生字符串值（或可以转换为字符串）的Java语言表达式。表达式包含在`<%=和%>`分隔符中。分隔符之间的任何内容都作为`out.print()`或`out.write()`方法的参数。因此，表达式不能以分号结尾。脚本是设计用于在`_jspService()`方法内部运行的Java代码片段，由`<%和%>`分隔符标记。脚本中的编程语句被直接复制到生成的servlet的Java源代码中。

为了使其与JSP容器连接，JSP页面可以访问许多隐式对象。这些是自动初始化的对象，具有预定义的变量名。这些变量是：

- request
- response
- pageContext
- session
- application
- out
- config
- page
- exception

最后一个变量（exception）仅对在其页面指令中具有`isErrorPage="true"`属性的页面可用。

此页有意留白。

The Complete Reference

![](img/7a2f73369bb140583c7288b73456addb_137_0.png)

## 第8章

# 声明

版权所有 © 2001 The McGraw-Hill Companies, Inc. 点击此处查看使用条款。



上一章介绍了 JSP 表达式和脚本片段。这两种元素类型与固定的 HTML 模板数据一样，共享一个公共环境——它们都存在于生成的 Java servlet 的 `_jspService()` 方法内。虽然这对于大多数请求处理来说已经足够，但它限制了 servlet 的某些功能。本章将介绍 JSP 声明，它允许 JSP 作者编写在 `_jspService()` 方法之外运行的 Java 代码。

## 什么是声明？

与脚本片段类似，JSP 声明是嵌入在 HTML 页面中的 Java 源代码。声明通过特殊的开始和结束标签与页面其余部分隔开，如下所示：

```
<%! java statements %>
```

声明的语法与脚本片段相同，只有一个例外：开始定界符是 `<%!`，而不是 `<%`。

与脚本片段一样，声明定界符内的代码会被原样复制到生成的 Java servlet 中。本质区别在于代码放置的位置：脚本片段被复制到 `_jspService()` 方法内部，而声明则被写在该方法之外，作为封闭类的顶层成员。理解这一区别有助于你建立 JSP 工作原理的心智模型，并解释意外的行为。

## 声明代码的生成位置

通过一个示例来展示声明代码是如何生成的会更清楚。考虑以下使用脚本片段显示当前时间的 JSP 页面：

```
<%@ page import="java.text.*,java.util.*" %>
<%
    DateFormat fmt = new SimpleDateFormat("hh:mm:ss aa");
    String now = fmt.format(new Date());
%>
The time is <%= now %>
```

该页面存储在名为 `ShowTimeS.jsp` 的文件中（S 代表脚本片段）。调用此文件时，它会显示当前时间：

```
The time is 09:31:45 PM
```

如果用户刷新页面，时间会按预期递增：

```
The time is 09:31:48 PM
The time is 09:31:51 PM
The time is 09:31:53 PM
```

现在考虑一个使用声明而不是脚本片段编写的相同 JSP。这个页面名为 ShowTimeD.jsp（D 代表声明）：

```
<%@ page import="java.text.*,java.util.*" %>
<%!
    DateFormat fmt = new SimpleDateFormat("hh:mm:ss aa");
    String now = fmt.format(new Date());
%>
The time is <%= now %>
```

ShowTimeS.jsp 和 ShowTimeD.jsp 之间唯一的区别是 ShowTimeD.jsp 的第二行以 `<%!` 开头，而不是 `<%`，使其成为一个声明而不是脚本片段。当 ShowTimeD.jsp 被调用时，它同样显示当前时间：

```
The time is 09:32:26 PM
```

但是，看看刷新页面后会发生什么：

```
The time is 09:32:26 PM
The time is 09:32:26 PM
The time is 09:32:26 PM
```

时间没有变化。为什么？答案可以在每个页面生成的 servlet 源代码中找到。这是脚本片段版本：

```
import javax.servlet.*;
import javax.servlet.http.*;
import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.PrintWriter;
import java.io.IOException;
import java.io.FileInputStream;
import java.io.ObjectInputStream;
import java.util.Vector;
import org.apache.jasper.runtime.*;
import java.beans.*;
import org.apache.jasper.JasperException;
import java.text.*;
import java.util.*;

public class ShowTimeS extends HttpJspBase
{
    static
    {
    }

    public ShowTimeS()
    {
    }

    public void _jspService(
            HttpServletRequest request,
            HttpServletResponse response)
        throws IOException, ServletException
    {
        JspFactory _jspxFactory = null;
        PageContext pageContext = null;
        HttpSession session = null;
        ServletContext application = null;
        ServletConfig config = null;
        JspWriter out = null;
        Object page = this;
        String  _value = null;
        try {
            _jspxFactory = JspFactory.getDefaultFactory();
            response.setContentType("text/html;charset=8859_1");
            pageContext = _jspxFactory.getPageContext
                (this, request, response, "", true, 8192, true);

            application = pageContext.getServletContext();
            config = pageContext.getServletConfig();
            session = pageContext.getSession();
            out = pageContext.getOut();

            out.write("\r\n");
            DateFormat fmt = new SimpleDateFormat("hh:mm:ss aa");
            String now = fmt.format(new Date());
            out.write("\r\nThe time is ");
            out.print( now );
            out.write("\r\n");
        }
        catch (Exception ex) {
            if (out.getBufferSize() != 0)
                out.clearBuffer();
            pageContext.handlePageException(ex);
        }
        finally {
            out.flush();
            _jspxFactory.releasePageContext(pageContext);
        }
    }
}
```

这是声明版本：

```
import javax.servlet.*;
import javax.servlet.http.*;
import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.PrintWriter;
import java.io.IOException;
import java.io.FileInputStream;
import java.io.ObjectInputStream;
import java.util.Vector;
import org.apache.jasper.runtime.*;
import java.beans.*;
import org.apache.jasper.JasperException;
import java.text.*;
import java.util.*;

public class ShowTimeD extends HttpJspBase
{
    DateFormat fmt = new SimpleDateFormat("hh:mm:ss aa");
    String now = fmt.format(new Date());

    static
    {
    }

    public ShowTimeD()
    {
    }

    public void _jspService(
            HttpServletRequest request,
            HttpServletResponse  response)
        throws IOException, ServletException
    {
        JspFactory _jspxFactory = null;
        PageContext pageContext = null;
        HttpSession session = null;
        ServletContext application = null;
        ServletConfig config = null;
        JspWriter out = null;
        Object page = this;
        String  _value = null;
        try {
            _jspxFactory = JspFactory.getDefaultFactory();
            response.setContentType("text/html;charset=8859_1");
            pageContext = _jspxFactory.getPageContext
                (this, request, response, "", true, 8192, true);

            application = pageContext.getServletContext();
            config = pageContext.getServletConfig();
            session = pageContext.getSession();
            out = pageContext.getOut();

            out.write("\r\n");
            out.write("\r\nThe time is ");
            out.print( now );
            out.write("\r\n");
        }
        catch (Exception ex) {
            if (out.getBufferSize() != 0)
                out.clearBuffer();
            pageContext.handlePageException(ex);
        }
        finally {
            out.flush();
            _jspxFactory.releasePageContext(pageContext);
        }
    }
}
```

除了程序名称，两个 servlet 之间的区别在于两行脚本代码的位置。在脚本片段版本中，它们被包含在 `_jspService()` 方法的中间，使得 `fmt` 和 `now` 变量是该方法的局部变量。然而，在声明版本中，它们作为类内部的第一个条目出现。这使得这两个变量成为实例变量，它们在 servlet 实例首次创建时初始化，并且永远不会更新：我们很快就会看到，这不仅是不可取的，而且是危险的。

## 声明的主要用途

声明可以包含任何有效的 Java 代码，但它们最常用于三种上下文：

- **变量声明** 可以声明和初始化类变量和实例变量。
- **方法定义** 可以将重复或过于复杂的脚本片段代码重构为一个调用其他方法的主程序。
- **内部类** 可以定义额外的类，并使其对脚本片段、表达式和其他声明代码可用。

本章剩余部分将详细讨论每种用途。

## 变量声明

如前面的示例所示，声明可用于定义和初始化变量。这些变量将可供脚本片段、表达式和其他声明使用。它们可以是类变量（用 `static` 关键字标记），如以下示例所示：

```
<%!
    static final String[] COLORS = {
```



# 第8章：声明

## 方法定义

声明的另一种常见用途是定义额外的方法。其语法与其他方法定义的语法并无不同，仅使用 `<%!` 和 `%>` 作为分隔符：

```
<%!
    public int sum(int a, int b)
    {
        return a + b;
    }
%>
```

与变量声明类似，方法定义会被逐字复制到生成的 servlet 中，成为 `_jspService()` 方法之外的顶层成员：

```
public class methdef1 extends HttpJspBase
{
    // begin [file="methdef1.jsp";from=(0,3);to=(5,0)]

    public int sum(int a, int b)
    {
        return a + b;
    }
    // end

    // ...

    public void _jspService(
            HttpServletRequest request,
            HttpServletResponse  response)
        throws IOException, ServletException
    {
        // ...
    }
}
```

JSP 声明中典型的方法定义是用于一个工具方法，该方法用于重新格式化由脚本段生成的字符串。考虑以下 JSP 页面，它在一个 HTML 表格中显示几个系统属性的值：

```
<TABLE BORDER=1 CELLPADDING=3 CELLSPACING=0>
<%
    String[] propNames = {
        "java.awt.printerjob",
        "java.class.path",
        "java.class.version",
        "java.ext.dirs",
        "java.library.path",
    };
    for (int i = 0; i < propNames.length; i++) {
        String name = propNames[i];
        String value = System.getProperty(name);
%>
<TR>
    <TD ALIGN=LEFT VALIGN=TOP><%= name %></TD>
    <TD ALIGN=LEFT VALIGN=TOP><%= value %></TD>
</TR>
<%
    }
%>
</TABLE>
```

该 JSP 页面的输出如图 8-4 所示。这个表格的问题在于，有几个值相当长，且内部没有空格。这意味着右侧的表格单元格过长，无法在窗口中显示。

一个简单的解决方案是缩短这些属性值字符串。这些有问题的成员有一个共同点：它们都是由分号分隔的多个值组成的列表。可以通过在每个分号后插入一个 `<BR>` 标签来缩短它们，这样列表就会显示在多行上。这将使表格的宽度要求不超过最长列表条目的长度。这可以在脚本段中用内联代码完成，但一个更具可读性的解决方案是使用一个 `normalize()` 方法来应用必要的转换。这样，`<%= value %>` 表达式就可以简单地写成 `<%= normalize(value) %>`。以下是修改后的 JSP 页面：

```
<TABLE BORDER=1 CELLPADDING=3 CELLSPACING=0>
<%
    String[] propNames = {
        "java.awt.printerjob",
        "java.class.path",
        "java.class.version",
        "java.ext.dirs",
        "java.library.path",
    };
    for (int i = 0; i < propNames.length; i++) {
        String name = propNames[i];
        String value = System.getProperty(name);
%>
<TR>
    <TD ALIGN=LEFT VALIGN=TOP><%= name %></TD>
    <TD ALIGN=LEFT VALIGN=TOP><%= normalize(value) %></TD>
</TR>
<%
    }
%>
</TABLE>
<%!
    private static final String normalize(String s)
    {
        StringBuffer sb = new StringBuffer();
        for (int i = 0; i < s.length(); i++) {
            char c = s.charAt(i);
            sb.append(c);
            if (c == ';')
                sb.append("<BR>");
        }
        return sb.toString();
    }
%>
```

这次，当显示相同的属性时，表格就适应了更合理的窗口大小（见图 8-5）。



## 重写 jspInit 和 jspDestroy

在前面的例子中，字符串操作本可以在脚本片段中使用内联代码完成，而不必通过方法调用。在某些情况下，这是不可能的。例如，如果在加载 JSP 页面时需要获取资源或启动线程，这些操作应在 servlet 的 `init()` 和 `destroy()` 方法上下文中执行。

JSP 1.1 规范明确禁止页面作者直接重写任何 servlet 生命周期方法，包括 `init()` 和 `destroy()`[^1]。然而，它提供了两个特殊方法 `jspInit()` 和 `jspDestroy()` 来达到相同的目的。这些方法会从 `init()` 和 `destroy()` 内部自动调用，并在父 JSP 页面实现中具有空定义。

例如，在 Tomcat 中，基础 JSP 类 `org.apache.jasper.runtime.HttpJspBase` 定义了 `init()` 和 `jspInit()` 如下：

```java
public final void init(ServletConfig config)
    throws ServletException
    {
        this.config = config;
        jspInit();
    }

public void jspInit()
{
}
```

类似地，它定义了 `destroy()` 和 `jspDestroy()` 如下：

```java
public final void destroy()
{
    jspDestroy();
}
public void jspDestroy()
{
}
```

使用 `final` 关键字确保了 `init()` 和 `destroy()` 本身不能被重写。这反过来又保证了 `jspInit()` 和 `jspDestroy()` 总是会被调用。要向 JSP 的初始化阶段添加内容，应在 JSP 声明中输入必要的代码：

```java
public void jspInit()
{
    TimerThread t = new TimerThread();
    t.start();
}
```

[^1]: JSP 1.1 规范，第 3.1 节。尽管某些 servlet 引擎未强制执行此限制，但忽略它是不明智的。

值得注意的是，JSP 1.1 规范没有规定从 `jspInit()` 中抛出异常，即使 `init()` 本身可以这样做。如果 JSP 在其 `jspInit()` 执行期间检测到致命错误，具体能采取什么措施尚不明确。

## 访问隐式对象

与脚本片段和表达式不同，声明无法访问第 7 章中描述的隐式对象。原因很明显，因为声明中的方法定义在 `_jspService()` 方法之外。因此，如果声明方法需要访问其中一个或多个对象，则必须以某种方式从 `_jspService()` 传递这些对象。你可以通过几种方式做到这一点：

- 将对象作为单独的参数传递。这很容易做到，但如果需要超过几个参数，会变得笨拙。
- 将 `pageContext` 隐式对象作为参数传递。通过页面上下文，可以间接访问所有其他变量。
- 将包含所有相关变量的结构作为单个参数传递。你将在下一节中看到如何做到这一点。

第二种技术（传递页面上下文）在以下代码中进行了说明：

```jsp
<%@ page import="java.io.*,java.util.*" %>
<%!
    public void showSessionID(PageContext pc)
        throws IOException
    {
        JspWriter out = pc.getOut();
        HttpSession session = pc.getSession();
        Date created = new Date(session.getCreationTime());
        out.println("The session was created at " + created);
    }
%>
<%
    showSessionID(pageContext);
%>
```

`showSessionID()` 方法能够从页面上下文中提取 `JspWriter` 和 `HttpSession` 对象，并使用它们写入当前输出流。

## 内部类

与任何其他 Java 类一样，JSP 页面可以定义内部类。*内部类*对于运行后台线程或封装数据结构非常有用。使用得当，它们可以保持 Java 程序的面向对象特性，这在像 JSP 这样的事件驱动环境中有时会丢失。

内部类可以作为一个有用的数据结构，用于保存隐式变量和其他变量。页面上下文充当 servlet 上下文、会话、请求和页面中其他对象的包装器。它还有 `getAttribute()` 和 `setAttribute()` 方法用于额外的用户定义字段，但这些必须是对象（而不是像 `int` 和 `double` 这样的基本类型），并且在检索时必须转换为适当的类型。内部类是另一种解决方案，它以类型安全的方式解决相同的问题。以下示例说明了这种技术：

```jsp
<%@ page import="java.io.*,java.util.*" %>
<%!
    /**
     * 用于在方法之间传递参数的内部类
     */
    class Parameters {
        JspWriter out;
        HttpSession session;
        String url;
    }

    public void showSessionID(Parameters parms)
        throws IOException
    {
        JspWriter out        = parms.out;
        HttpSession session  = parms.session;
        String url           = parms.url;
        Date created = new Date(session.getCreationTime());
        out.println("The session was created at " + created + "<P>");
        out.println("The url parameter was " + url);
    }
%>
<%
    Parameters parms = new Parameters();
    parms.out = out;
    parms.session = session;
    parms.url = request.getParameter("url");
    showSessionID(parms);
%>
```

生成的 servlet 将内部类和方法定义都包含在类的顶层，以及脚本片段在 `_jspService()` 内部：

```java
import javax.servlet.*;
import javax.servlet.http.*;
import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.PrintWriter;
import java.io.IOException;
import java.io.FileInputStream;
import java.io.ObjectInputStream;
import java.util.Vector;
import org.apache.jasper.runtime.*;
import java.beans.*;
import org.apache.jasper.JasperException;
import java.io.*;
import java.util.*;

public class PassInnerClass extends HttpJspBase
{
    // begin [file="PassInnerClass.jsp";from=(1,3);to=(22,0)]

    /**
     * 用于在方法之间传递参数的内部类
     */
    class Parameters {
        JspWriter out;
        HttpSession session;
        String url;
    }

    public void showSessionID(Parameters parms)
    throws IOException
    {
        JspWriter out        = parms.out;
        HttpSession session  = parms.session;
        String url           = parms.url;
        Date created = new Date(session.getCreationTime());
        out.println("The session was created at " + created
            + "<P>");
        out.println("The url parameter was " + url);
    }
    // end

    // ...

    public void _jspService(
        HttpServletRequest request,
        HttpServletResponse response)
        throws IOException, ServletException
    {
        // ...

        // begin [file="PassInnerClass.jsp";from=(23,2);to=(29,0)]

        Parameters parms = new Parameters();
        parms.out = out;
        parms.session = session;
        parms.url = request.getParameter("url");
        showSessionID(parms);

        // end
    }
}
```

## 总结

第 7 章介绍了脚本片段和表达式。本章引入了第三种类型的脚本元素：JSP *声明*。

与脚本片段类似，声明用于将 Java 语句合并到 JSP 页面中。两者之间的关键区别在于 JSP 容器将代码写入生成的 servlet 的位置。脚本片段中的代码成为 `_jspService()` 方法的一部分，而声明中的代码则成为 servlet 类中的顶层代码。理解这一区别很重要，因为它影响代码运行的上下文。

声明有三个主要用途：

- **变量声明** 可以定义类变量和实例变量，但必须注意确保对变量的写入访问是同步的，因为 servlet 默认是多线程的。变量声明最实际的用途是定义 `static final` 常量。
- **方法定义** 可以通过 JSP 声明向生成的 servlet 添加额外方法。但是，由于生成的代码不在 `_jspService()` 方法内部，因此它无法访问隐式变量（`request`、`response`、`out` 等）。如果需要使用这些变量，必须显式地将它们传递给该方法。声明可用于重写 `jspInit()` 和 `jspDestroy()` 方法。
- **内部类** 声明提供了一种编写内部类的便捷方式。本章描述了使用内部类作为数据结构，在生成的 servlet 中的方法之间传递一组变量。



## 第九章：请求分发

在大型Web开发项目中，让HTTP请求由多个服务器端组件处理通常是可取的。这样做有几个原因：

- **消除冗余** 网站的许多功能对所有页面都是通用的，例如页眉和页脚、导航栏以及其他外观和风格元素。与其重复生成这些功能的HTML，不如编写一次并在多个地方使用，这更为实用。
- **内容与表现分离** 由于Java可以在JSP的任何部分自由使用，你很容易编写出既生成信息又呈现信息的代码，可能涉及从数据库读取、执行计算以及生成HTML表格。日后可能需要同时更改逻辑和页面外观。这种代码很快会变得过于复杂。更有意义的是，将访问数据库和应用业务逻辑的纯Java代码与创建输出网页的JSP代码分离。

本章探讨JSP环境中允许转发请求以及包含其他资源内容或输出的特性。本章还将讨论`RequestDispatcher`类的工作原理，并以比较两种JSP开发模型作为结尾。

## 请求处理剖析

处理servlet和JSP请求的servlet引擎可以是Web服务器本身的一部分（称为*进程内*模型），也可以在单独的进程中运行。在后一种情况下，Web服务器包含一个称为连接器的组件。*连接器*拦截servlet请求，并通过与具体实现相关的协议将其传递给servlet引擎。其他请求则照常由Web服务器处理。图9-1说明了这种进程外模型。

当servlet引擎接收到一个请求时，它会将有关该请求的所有细节组装成一个`HttpServletRequest`对象。这些细节包括请求头、URI、查询字符串、发送的任何参数等等。同样，它会初始化一个`HttpServletResponse`对象，用于保存响应头和响应输出流。然后，它调用servlet的`service()`方法（如果servlet是JSP，则调用`_jspService()`方法），并传递这两个对象的引用，如图9-2所示。

1.  JRun为多种广泛使用的Web服务器提供了连接器，并采用专有协议将其请求通信至其servlet引擎。Tomcat使用一种名为ajp12（最初为Apache JServ开发）的协议在组件之间发送请求和响应。

图9-1. *进程外servlet引擎模型*

一个简单的JSP可以从请求对象中提取它所需的内容，执行必要的计算和其他逻辑，然后使用响应对象创建输出。本章的其余部分将探讨更大更复杂的Web应用程序如何在这些请求和响应对象上操作，将它们传递给多个servlet或JSP。

图9-2. *servlet引擎将请求和响应对象传递给servlet*

## 包含其他资源

HTML本身没有直接的方法在其输出中包含来自其他文件的数据。这很遗憾，因为在典型的网站中，大量的HTML标记在许多页面中是通用的——公司标志、版权声明、导航链接和其他功能。除了这些静态的文本和图像源之外，可能还需要包含动态内容。JSP提供了两种包含此类数据的方法：

- `<%@ include %>`指令用于在将JSP源代码转换为Java servlet源代码并编译之前，将静态文本复制到其中。通常，这段文本是HTML代码，但它也可以是任何可以出现在JSP页面中的内容。
- `<jsp:include>`操作会促使servlet引擎调用另一个URL，并将其输出与原始JSP页面的输出合并。

构建心智模型时需要记住的一个关键点是，`<%@ include %>`指令在编译时执行一次，而`<jsp:include>`操作则在每次发出请求时执行。接下来的两节将分别描述这两种JSP组件及其操作方式。

### include 指令

`include`指令的语法如下：
`<%@ include file="filename" %>`
包含的文件名必须是相对URL规范，这意味着它只包含路径信息，不包含协议或服务器信息。因此，只能通过此方法包含当前servlet上下文中的资源。

如果文件名以“/”开头，则它被视为相对于servlet上下文顶部的绝对路径。否则，文件名被视为相对于当前JSP页面的相对路径。例如，如果一个Web应用程序有一个`products`子目录，并且`products/search.jsp`页面包含指令

```
<%@ include file="/includes/header.inc" %>
```

那么将要包含的文件是`<path>/includes/header.inc`，其中`<path>`是Web应用程序的挂载点。如果指令改为

```
<%@ include file="includes/header.inc" %>
```

那么该文件将是`<path>/products/includes/header.inc`。

### 工作原理

当遇到`<%@ include %>`指令时，JSP容器读取指定的文件并将其内容合并到当前正在解析的JSP源代码中。例如，如果`flavors.jsp`包含

```
<H3>Flavors</H3>
Our most popular flavors are:
<%@ include file="flavor_list.html" %>
Try them all!
```

并且`flavor_list.html`包含

```
<OL>
<LI>Chocolate
<LI>Strawberry
<LI>Vanilla
</OL>
```

那么发送到Web浏览器的HTML与`flavors.jsp`包含以下内容完全相同：

```
<H3>Flavors</H3>
Our most popular flavors are:
<OL>
<LI>Chocolate
<LI>Strawberry
<LI>Vanilla
</OL>
Try them all!
```

我们可以从Tomcat参考实现生成的servlet源代码中看到两个文件的交错：

```
// begin [file="flavors.jsp";from=(0,0);to=(2,0)]
    out.write("<H3>Flavors</H3>\r\n");
    out.write("Our most popular flavors are:\r\n");
```

2. 生成的源代码示例为可读性稍作重新格式化。

```
// end

// begin [file="flavor_list.html";from=(0,0);to=(5,0)]
out.write("<OL>\r\n");
out.write("<LI>Chocolate\r\n");
out.write("<LI>Strawberry\r\n");
out.write("<LI>Vanilla\r\n");
out.write("</OL>\r\n");
// end

// begin [file="flavors.jsp";from=(2,38);to=(4,0)]
out.write("\r\nTry them all!\r\n");
// end
```

除了注释中的文件名更改外，无法分辨有序列表不是直接在原始JSP页面中编码的。在这方面，`<%@ include %>`指令类似于C语言的`#include`预处理指令。

### 包含文件更改的影响

如果`flavor_list.html`文件被修改会怎样？JSP 1.1规范没有规定通知JSP容器包含文件已更改，尽管它并不禁止这样做，并且健壮的JSP容器应该这样做。JRun将依赖名称和最后修改时间合并到生成的源代码中，以便它可以确定文件何时过期：

```
private static final String[] __dependencies__ = {
    "/Chap09/examples/flavors.jsp",
    "/Chap09/examples/flavor_list.html",
    null
    };

private static final long[] __times__ = {
    958963142531L,
    958961380337L,
    0L
    };
```

需要记住的关键点是，包含的文件是编译时存在的文件，因为`<%@ include %>`指令在此时被处理。这就是为什么文件名不能是运行时表达式。这也意味着包含的文件必须在编译时存在。



## 使用 include 指令复制源代码

除了用于复制 HTML 外，`include` 指令还可用于将 Java 源代码作为声明部分包含进来。例如，一个常用的实用函数可以存储在文件中，并通过 `include` 指令合并到 JSP 页面中。一个典型的例子是一个过滤掉 HTML 中具有特殊含义的字符，并将其替换为符号化可打印等效字符的函数：

```
<%!
public static final String webify(String s)
{
    StringBuffer sb = new StringBuffer();
    int n = s.length();
    for (int i = 0; i < n; i++) {
        char c = s.charAt(i);
        switch (c) {
            case '<': sb.append("&lt;"); break;
            case '>': sb.append("&gt;"); break;
            case '&': sb.append("&amp;"); break;
            case '"': sb.append("&quot;"); break;
            default:  sb.append(c); break;
        }
    }
    return sb.toString();
}
%>
```

一旦通过包含定义，此函数即可在包含它的 JSP 页面的小脚本和表达式中使用：

```
<%@ include file="webify.jsp" %>
```

预格式化文本可以使用 `<%= webify("<PRE> and </PRE>") %>` 标签进行编码。

同样，整个应用程序中使用的常量可以在由 `include` 指令处理的 JSP 声明中进行编码：

```
<%!
    static final int BORDER = 1;
    static final int CELLPADDING = 3;
    static final int CELLSPACING = 0;
    static final String[] COLORS = {"#C0C0C0", "#E0E0E0"};
%>
```

如果上面展示的声明存储在 `TableConstants.jsp` 文件中，那么一个 JSP 页面可以如下生成具有交替背景颜色的行的表格：

```
<%@ include file="TableConstants.jsp" %>

<TABLE BORDER="<%= BORDER %>"
       CELLPADDING="<%= CELLPADDING %>"
       CELLSPACING="<%= CELLSPACING %>"
       >
<%
    for (int i = 0; i < 10; i++) {
        int x = i+1;
        int xsq = x*x;
%>
<TR BGCOLOR="<%= COLORS[i % 2] %>">
    <TD><%= x %></TD> <TD><%= xsq %></TD>
</TR>
<%
    }
%>
</TABLE>
```

> **注意** 使用 include 指令包含源代码声明时，需要注意两件事。首先，JSP 1.1 规范不保证以这种方式包含代码的页面会在代码更改时收到通知。其次，包含的代码使用包含页面的命名空间，因此必须谨慎操作以确保不会发生重复的变量定义。

## <jsp:include> 动作

与 include 指令相反，jsp:include 动作在每次请求时都会被解释执行。此动作的语法是

```
<jsp:include page="resourcename" flush="true" />
```

包含的资源名称必须是一个相对 URL 规范，仅包含路径信息。该资源名称映射到当前 servlet 上下文的方式与 include 指令中的文件名相同。如果名称以 "/" 开头，则它指向 servlet 上下文根目录下的路径；否则，它被解释为相对于调用 JSP 所在目录的路径。flush 属性（是必需的）用于指示在包含资源之前是否刷新输出 JspWriter。在 JSP 1.1 中唯一有效的值是 `true`。

### 工作原理

`<jsp:include>` 动作由 JSP 编译器解析，但它不是在编译时执行，而是被转换为在请求时调用命名资源的 Java 代码。该资源可以是静态数据源（如 HTML 文件），也可以是动态源（如 JSP 页面或 servlet）。回到我们的冰淇淋口味示例，`flavors.jsp` 可能包含：

```
<H3>Flavors</H3>
Our most popular flavors are:
<jsp:include page="/servlet/FlavorList" flush="true" />
Try them all!
```

其中 `FlavorList` 是一个 *servlet*，它从数据库或其他动态源提取最受欢迎的口味：

```
import java.io.*;
import java.net.*;
import java.sql.*;
import java.util.*;

import javax.servlet.*;
import javax.servlet.http.*;

/**
 * Returns the current list of favorite flavors
 */
public class FlavorListServlet extends HttpServlet
{
    public static final String JDBC_DRIVER =
        "sun.jdbc.odbc.JdbcOdbcDriver";

    public static final String URL =
        "jdbc:odbc:IceCream";

    public void doGet(
            HttpServletRequest request,
            HttpServletResponse response)
        throws ServletException, IOException
    {
        PrintWriter out = response.getWriter();

        Connection con = null;
        try {
            // Connect to the ice cream database
            Class.forName(JDBC_DRIVER);
            con = DriverManager.getConnection(URL);

            // Run a query to get the top flavors
            Statement stmt = con.createStatement();
            String sql =
                "SELECT RANK, NAME"
                + " FROM flavors"
                + " WHERE (RANK <= 3)"
                + " ORDER BY RANK"
                ;

            ResultSet rs = stmt.executeQuery(sql);

            // Print as an ordered list
            out.println("<OL>");
            while (rs.next()) {
                int rank = rs.getInt(1);
                String name = rs.getString(2);
                out.println("    <LI>" + name);
            }
            out.println("</OL>");
        }
        catch (Exception e) {
            e.printStackTrace();
        }

        // Close the database
        finally {
            if (con != null) {
                try {
                    con.close();
                }
                catch (SQLException ignore) {}
            }
        }
    }
}
```

当 `flavors.jsp` 被调用时，它会产生以下输出：

```
<H3>Flavors</H3>
Our most popular flavors are:
<OL>
    <LI>Espresso Chip
    <LI>Orange Cream
    <LI>Peanut Butter
</OL>
Try them all!
```

生成的 HTML 看起来可能相似，但底层机制完全不同，从 Tomcat 生成的 servlet 源代码中可以看出：

```
// begin [file="flavors.jsp";from=(0,0);to=(2,0)]
out.write("<H3>Flavors</H3>\r\n");
out.write("Our most popular flavors are:\r\n");
// end

// begin [file="flavors.jsp";from=(2,0);to=(2,55)]
{
    out.flush();
    pageContext.include("/servlet/FlavorList");
}
// end

// begin [file="flavors.jsp";from=(2,55);to=(4,0)]
out.write("\r\nTry them all!\r\n");
// end
```

JSP 并非包含口味的有序列表，而是调用 `pageContext.include()` 方法来运行访问数据库的 servlet。servlet 的输出被包含在 JSP 输出中，然后 JSP 恢复控制。如果说 include 指令类似于 C 语言的 `#include` 预处理指令，那么 `<jsp:include>` 动作则更像 C 语言的函数调用。

## 限制

由 `<jsp:include>` 动作调用的 JSP 页面可以访问调用 JSP 可用的所有隐式对象，包括 response 对象。它可以写入和刷新 out 对象，但不能设置响应头。例如，既不能指定不同的内容类型，也不能使用 `<jsp:include>` 动作通过 WWW-Authenticate 头处理身份验证。为什么不能？因为为时已晚——在 JSP 被包含之前输出流已被刷新，所以任何已存在的头信息都已经写入客户端了。

## 运行时特性

由于 `<jsp:include>` 在运行时求值，它引用的页面可以在运行时表达式中提供，而不需要硬编码。以下 JSP 页面旨在提供 HTTP servlet 请求的全面视图。该页面模拟了一个选项卡式对话框，而不是一个冗长的、可滚动的属性名称和值的列表，属性被分解为逻辑组，并沿顶部使用单选按钮来选择显示哪个组。

```
<%@ page import="java.util.*" %>
<%!
    // Table row colors
    static final String[] COLORS = {"#E0E0E0", "#F0F0F0"};

    // Array of tab codes, labels, and JSP's
    public static final String[][] TABS = {
        {"HD", "Headers", "ShowRequestHeaders.jsp"},
        {"PM", "Parameters", "ShowParameters.jsp"},
        {"SR", "ServletRequest Methods",
            "ShowServletRequestMethodValues.jsp"},
        {"HR", "HttpServletRequest Methods",
            "ShowHttpServletRequestMethodValues.jsp"},
    };
%>
<HTML>
<HEAD>
<TITLE>Show Request</TITLE>
</HEAD>
<BODY>
<H2>Show Request</H2>
<FORM>
<TABLE BORDER=0 CELLPADDING=3 CELLSPACING=0>
```



# 第9章：请求分发 147

+   - 请求头
- 参数

+   ■ ServletRequest 中的方法
■ HttpServletRequest 中的方法

这个字符串数组提供了生成页面所需的所有信息。单选按钮包含在一个自引用的 HTML 表单中，并通过循环生成，使用两个字符的缩写作为 VALUE 属性，标签作为可见文本。当点击一个单选按钮时，表单会被提交，按钮的值将作为 which 参数的值。图 9-3 显示了初始显示，即请求头类别。当点击另一个单选按钮（例如，ServletRequest Method 按钮）时，表格主体中会出现不同的表格（见图 9-4）。

![](img/7a2f73369bb140583c7288b73456addb_173_0.png)

图 9-3. ShowRequest.jsp 显示的 HTTP 请求头

![](img/7a2f73369bb140583c7288b73456addb_174_0.png)

**图 9-4.** ShowRequest.jsp 第三个选项卡中显示的 Servlet 请求方法

ShowRequest.jsp 确定哪个单选按钮被点击，并从字符串数组中选择相应的 JSP 文件名。然后，这个文件名通过 JSP 表达式传递给 `<jsp:include>` 动作：

```
<jsp:include page="<%= jspToRun %>" flush="true" />
```

每个独立的表格生成页面都会创建一个属性名和值的列表，并将它们写入一个作为请求属性存储的 `java.util.Map` 对象。表格标题字符串也作为请求属性存储。当包含的 JSP 完成时，从请求属性中检索该映射并在 HTML 表格中渲染。生成“请求头”选项卡的 JSP 如下所示：

```
<%@ page import="java.util.*" %>
<%
    Enumeration eNames = request.getHeaderNames();
    if (eNames.hasMoreElements()) {
        String title = "Request Headers";
        Map entries = new TreeMap();
        while (eNames.hasMoreElements()) {
            String name = (String) eNames.nextElement();
            String value = request.getHeader(name);
            entries.put(name, value);
        }
        request.setAttribute("_table_title", title);
        request.setAttribute("_table_entries", entries);
    }
%>
```

这种根据运行时信息选择要包含的页面的能力是基于 JSP 的 Web 应用程序的一个有用特性，因为它允许基于表驱动逻辑构建复杂的处理。

## 将参数传递给包含的 JSP

可以通过 `<jsp:include>` 动作调用的 JSP 页面传递参数，以提供额外的自定义。这种情况下的语法是

```
<jsp:include page="pageName" flush="true">
<jsp:param name="parm1Name" value="parm1Value" />
<jsp:param name="parm2Name" value="parm2Value" />
</jsp:include>
```

这些参数与普通的表单参数相同，传递给包含的 JSP，并且可以使用 `request.getParameter(name)` 检索。如果参数名与 JSP 已经使用的相同，两个值都会被传递，并且可以使用 `getParameterValues(name)` 作为字符串数组检索。

下面的 JSP 展示了如何使用这种技术。它两次包含同一个页面，每次使用不同的参数。

```
<%
    // Diameter of the earth in kilometers
    int distance = 12756;
%>

<H4>Diameter of the Earth in SI (Metric) Units</H4>
<jsp:include page="ShowDiameter.jsp" flush="true">
    <jsp:param name="dist" value="<%= distance %>" />
    <jsp:param name="units" value="SI" />
</jsp:include>

<H4>Diameter of the Earth in U.S. Customary Units</H4>
<jsp:include page="ShowDiameter.jsp" flush="true">
    <jsp:param name="dist" value="<%= distance %>" />
    <jsp:param name="units" value="US" />
</jsp:include>
```

传递了两个参数：

+   - **dist** 以公里为单位的距离。
- **units** 如果需要公制单位则为 "SI"，否则为 "US"。

ShowDiameter.jsp 页面检索公里距离，将其转换为整数，并找到英里等价值。然后，根据 units 参数传递的度量单位代码，以 SI 或美国单位显示距离。

```
<%
    String dist = request.getParameter("dist");
    int kilometers = Integer.parseInt(dist);
    double miles = kilometers / 1.609344;

    String units = request.getParameter("units");
    if (units.equals("SI")) {
        %> Diameter = <%= kilometers %> km <%
    }
    else {
        %> Diameter = <%= miles %> miles <%
    }
%>
```

图 9-5 显示了结果。

## 检索原始 URI

当页面在 `<jsp:include>` 动作中被调用时，它使用与包含页面相同的请求对象，这意味着 `request.getRequestURI()` 和 `request.servletPath()` 返回的是最初处理请求的页面的路径，而不是当前页面的路径。然而，包含页面的等效值可以作为请求的属性使用。这在 ShowPath1.jsp 中进行了说明：

```
<PRE>
In ShowPath1.jsp:

    request.getRequestURI()
        = <%= request.getRequestURI() %>

    request.servletPath()
        = <%= request.servletPath() %>

</PRE>
<jsp:include page="ShowPath2.jsp" flush="true"/>
```

以及它包含的页面 ShowPath2.jsp：

```
<PRE>
In ShowPath2.jsp:

    request.getRequestURI()
        = <%= request.getRequestURI() %>

    request.getServletPath()
        = <%= request.getServletPath() %>

    javax.servlet.include.request_uri
        = <%= request.getAttribute
            ("javax.servlet.include.request_uri") %>

    javax.servlet.include.servlet_path
        = <%= request.getAttribute
            ("javax.servlet.include.servlet_path") %>

</PRE>
```

![](img/7a2f73369bb140583c7288b73456addb_177_0.png)

图 9-5. 一个包含同一页面两次并使用不同参数的 JSP 页面

两个页面的输出如下：

```
In ShowPath1.jsp:
    request.getRequestURI()
        = /jspcr/Chap09/examples/ShowPath1.jsp
    request.getServletPath()
        = /Chap09/examples/ShowPath1.jsp
In ShowPath2.jsp:
    request.getRequestURI()
        = /jspcr/Chap09/examples/ShowPath1.jsp
    request.getServletPath()
        = /Chap09/examples/ShowPath1.jsp
    javax.servlet.include.request_uri
        = /jspcr/Chap09/examples/ShowPath2.jsp
    javax.servlet.include.servlet_path
        = /Chap09/examples/ShowPath2.jsp
```

可以通过这种方式检索的属性集列在表 9-1 中。



| 属性名称 | 等效方法 |
|---|---|
| javax.servlet.include.request_uri | request.getRequestURI() |
| javax.servlet.include.context_path | request.getContextPath() |
| javax.servlet.include.servlet_path | request.getServletPath() |
| javax.servlet.include.path_info | request.getPathInfo() |
| javax.servlet.include.query_string | request.getQueryString() |

表 9-1. 描述被包含JSP页面的请求属性

## 使用哪种方法

包含指令和 `<jsp:include>` 动作执行类似的功能，各有其优点。选择使用哪一种，应考虑包含操作是否需要在运行时进行。下表比较了两种选项：

| 准则 | <%@ include %> | <jsp:include> |
|---|---|---|
| 编译时间 | 较慢——必须解析资源 | 稍快 |
| 执行时间 | 稍快 | 较慢——每次都需要解析资源 |
| 灵活性 | 较低——页面名称固定 | 较高——可在运行时选择页面 |

## 转发请求

为了方便将Web应用拆分为内容和表示两部分，JSP环境提供了 `<jsp:forward>` 动作，它允许将请求从一个页面转发到另一个页面，或转发到一个servlet。其语法为

```
<jsp:forward page="page" />
```

其中，page是相对于当前页面的URI，或者是相对于servlet上下文根目录的绝对URI。与 `<jsp:include>` 类似，`<jsp:forward>` 动作可以使用运行时表达式来指定页面名称。类似地，它可以使用以下语法向新的JSP传递参数：

```
<jsp:forward page="page">
    <jsp:param name="name_1" value="value_1" />
    <jsp:param name="name_2" value="value_2" />
    ...
    <jsp:param name="name_n" value="value_n" />
</jsp:forward>
```

当执行 `<jsp:forward>` 动作时，指定的页面会被加载，当前页面则终止。新页面可以访问请求和响应对象，并且需要创建所有输出，因为转发页面不能写入任何输出。下表描述了输出缓冲是否启用，以及缓冲区是否已满时的操作情况。

| 缓冲启用 | 缓冲区已满 | 操作 |
| :--- | :--- | :--- |
| 否 | 不适用 | 如果已经写入了任何输出，将抛出IllegalStateException。 |
| 是 | 否 | 转发前会清除缓冲区。 |
| 是 | 是 | 将抛出IllegalStateException。 |

以下代码展示了请求转发的典型用途——将内容与表示分离。第一个JSP页面是GetFoodGroups.jsp，它从USDA营养数据库中读取食物组列表：

```
<%@ page errorPage="/ErrorPage.jsp" %>
<%@ page import="java.io.*" %>
<%@ page import="java.sql.*" %>
<%@ page import="java.util.*" %>
<%@ page import="jspsr.forward.*" %>
<%
```

// 加载驱动程序类并建立连接

Class.forName
    ("sun.jdbc.odbc.JdbcOdbcDriver");

Connection con = DriverManager.getConnection
    ("jdbc:odbc:usda");

// 运行数据库查询以获取食物组列表

Statement stmt = con.createStatement();
String sql =
    " SELECT FdGp_Cd, FdGp_Desc"
    + " FROM fd_group"
    ;
ResultSet rs = stmt.executeQuery(sql);

// 将结果存储为FoodGroup对象列表

List fglist = new ArrayList();
while (rs.next()) {
    String code = rs.getString(1);
    String desc = rs.getString(2);
    FoodGroup fg = new FoodGroup(code, desc);
    fglist.add(fg);
}

rs.close();
stmt.close();
con.close();

// 将列表存储为请求属性

request.setAttribute("jspcr.forward.FoodGroups", fglist);

// 现在转发请求

%><jsp:forward page="ShowFoodGroups.jsp" />

随着食物组记录被读取，它们被存储在一个List结构中。该列表被保存为请求中的一个属性。当所有记录都已从数据库中提取出来时，请求被转发到ShowFoodGroups.jsp，后者检索该列表并将其写为HTML表格：

```
<%@ page import="java.io.*,java.util.*,jspcr.forward.*" %>
<HTML>
<HEAD>
<TITLE>Show Food Groups</TITLE>
<STYLE>
    body, td {
        background-color: #FFFFFF;
        font: 8pt Sans-Serif;
    }
</STYLE>
</HEAD>
<BODY>
<CENTER>
<H3>Food Groups</H3>

<%--  获取由数据库调用创建的FoodGroup对象列表 --%>

<%
    List fglist = (List) request.getAttribute
        ("jspcr.forward.FoodGroups");
    Iterator igroups = fglist.iterator();
%>

<TABLE BORDER=1 CELLPADDING=3 CELLSPACING=0>
<TR><TH>Code</TH><TH>Description</TH></TR>

<%--  遍历列表并打印每一项 --%>
<%
    while (igroups.hasNext()) {
        FoodGroup fg = (FoodGroup) igroups.next();
%>
    <TR>
        <TD><%= fg.getCode() %></TD>
        <TD><%= fg.getDescription() %></TD>
    </TR>
<%
    }
%>

</TABLE>
</CENTER>
</BODY>
</HTML>
```

ShowFoodGroups.jsp的优点在于它可以独立测试，而无需连接到数据库。可以编写一个用于测试的存根JSP。只要它填充了List属性，ShowFoodGroups.jsp就不会意识到它并非在与数据库打交道。结果显示在图9-6中。

![](img/7a2f73369bb140583c7288b73456addb_183_0.png)

`<jsp:include>` 和 `<jsp:forward>` 的底层机制都是 `javax.servlet.RequestDispatcher` 类。在上一节的食物组示例中，`<jsp:forward>` 动作被Tomcat翻译成以下代码：

```
if (true) {
    out.clear();
    String _jspx_qfStr = "";
    pageContext.forward("ShowFoodGroups.jsp" + _jspx_qfStr);
    return;
}
```

Tomcat对 `pageContext` 的实现，反过来调用一个 `RequestDispatcher` 来处理转发：

```
public void forward(String relativeUrlPath)
        throws ServletException, IOException
{
    String path = getAbsolutePathRelative Context(relativeUrlPath);
    context.getRequestDispatcher(path).forward(request, response);
}
```

你可以通过三种方式创建RequestDispatcher：

1. `ServletContext.getRequestDispatcher(String path)`
    - 路径必须是相对于上下文的绝对路径。
    - 如果已知其上下文，可以为另一个servlet上下文中的资源创建dispatcher。该上下文可以通过 `context.getContext(otherContext)` 获取。
2. `ServletContext.getNamedDispatcher(String name)`
    - *name* 参数指的是servlet别名，而不是物理路径名。
    - servlet可以通过 `config.getServletName()` 获取其自身名称。
3. `ServletRequest.getRequestDispatcher(String name)`
    - 路径可以是相对于上下文的绝对路径，也可以是相对于页面的相对路径。这是此方法与第一种方法的主要区别。

### 请求分发与重定向

请求分发器完成的大部分工作，也可以通过让JSP或servlet编写“临时移动”或“永久移动”状态码，并在Location头部写入下一个JSP或servlet的URL来实现。区别在于，重定向需要客户端的配合才能工作，而请求分发则完全在服务器端处理，无需客户端交互。

### 模型1与模型2

这些都是方便的功能，但如果仅仅随意地用于页眉和页脚，则未能充分发挥其作用。相反，它们可以成为协调良好的架构的一部分。如果你阅读JSP新闻组，经常会看到关于模型1和模型2架构的引用，这是在最初的JSP 0.92规范中引入的两种不同的Web应用结构方法。

在模型1应用中，JSP包揽一切：

- 用户请求一个JSP页面。
- JSP执行计算、数据库访问等操作。
- JSP页面用HTML呈现其输出。

完成所有这些工作所需的Java代码可以直接以脚本片段的形式编写，也可以包含在JavaBeans中。

模型2应用遵循模型-视图-控制器（MVC）范式。MVC是一种面向对象的编程概念，在Smalltalk语言中尤为突出。它描述了将应用逻辑划分为三个部分：

- **模型** 是逻辑上的“内部”表示。它没有可见的输出，也没有任何外部表示。因此，它可以在servlet、独立图形用户界面或批处理测试程序中同样良好地运行。例如，一个国际象棋游戏的模型可能包括一个表示棋盘的数组、表示每个棋子的数字以及对规则的一些编码。
- **视图** 是模型的表示层，几乎没有或完全没有编程逻辑。它从已填充的结构中读取并显示它们。在我们的国际象棋例子中，视图将是游戏的屏幕表示，可能有交替的颜色和雕刻精美的棋子。
- **控制器** 提供用户输入和方向给模型。在国际象棋的例子中，控制器将是键盘。



## Model 2 Web应用

在Model 2 Web应用中，所有用户请求都被引导到一个单一的URL，一个有时被称为*分发器*（即**控制器**）的servlet。这个servlet在请求的路径信息中查找它需要执行的操作指示。可能会有一个操作表和处理每个操作的JSP页面名称。这些操作处理程序构成了应用的**模型**。它们可以访问数据库或执行其他计算，然后将结果填充到JavaBeans或其他类中。最后，它们调用JSP页面（即**视图**）来呈现输出。

哪种模型更好？Model 1更容易快速搭建，但它的扩展性不好。太多的东西被捆绑在一起，随着应用的增长，它会变得难以控制。Model 2的扩展性好得多，并且允许专家编写应用的不同部分：

- Java程序员可以编写模型和控制器。
- 用户界面专家可以编写只负责显示输出的JSP页面。

## 总结

将HTTP请求处理拆分成多种情况通常是很有利的。JSP提供了两种通用能力来支持这一点：

- 使用`<%@ include %>`或`<jsp:include>`包含其他资源。
- 使用`<jsp:forward>`转发请求。

包含的资源可以是静态的（如HTML）或动态的（如JSP或servlet）。转发请求的能力为表驱动应用提供了基础。

存在两种通用的开发架构，通常称为Model 1和Model 2。Model 1使用JSP页面来接受用户输入，根据需要访问数据库，并格式化其输出。Model 2遵循MVC范式，允许复杂项目根据需要在专注于不同层次的团队之间进行分离。

# 完全参考

![](img/7a2f73369bb140583c7288b73456addb_187_0.png)

## 第10章

## 页面指令

161

版权所有 © 2001 The McGraw-Hill Companies, Inc. 点击此处查看使用条款。

**162 JSP：完全参考**

JSP页面不仅包含处理请求和生成响应的代码，还包含给JSP编译器的指令。这些指令被称为本章涵盖的最常用的一种——页面指令。此指令提供了一种设置属性的方法，这些属性影响页面的解释和执行方式。语法如下：

`<%@ page attribute="value" attribute="value" ... %>`

其中属性可以是以下任何一个：

- `language="scripting language"`
- `extends="className"`
- `import="importList"`
- `session="true | false"`
- `buffer="none | sizekb"`
- `autoFlush="true | false"`
- `isThreadSafe="true | false"`
- `info="info_text"`
- `contentType="ctinfo"`
- `errorPage="error_url"`
- `isErrorPage="true | false"`

属性可以按任意顺序指定，并且可以在一个编译单元（JSP页面及其通过include指令包含的任何文件）中指定多个页面指令。但是，如果使用多个页面指令，则不能对同一属性指定多次，import属性除外。
本章其余部分将详细讨论这些属性中的每一个。

### language

JSP架构允许它被扩展为一个通用的服务器端脚本框架。为此，它在页面指令中支持language属性。指定的值（默认为java）适用于当前翻译单元中的所有声明、表达式和脚本小程序，包括include指令中指定的任何文件。所有符合JSP 1.1规范的容器都必须支持language属性的值java。JSP 1.1规范不支持其他语言，尽管个别JSP引擎可能会支持。

虽然规范允许使用其他语言，但它施加了一些限制。该语言必须支持Java运行时环境，使其能够访问标准的隐式对象变量、JavaBeans的get和set方法以及Java类的公共方法。

JRun 3.0支持将java和javascript作为language属性的值。当使用java作为语言时——无论是显式还是隐式——JSP页面中找到的脚本小程序、表达式和声明都会像往常一样被复制到生成的servlet中。当指定javascript时，仍然会生成一个Java servlet，但它不包含javascript代码。相反，该servlet初始化一个脚本引擎，该引擎读取并解释原始的JSP页面。例如，如果JSP页面如下所示：

```
<%@ page language="java" %>
<%
    int k = 10;
%>
k = <%= k %>
```

那么生成的servlet包含以下语句：

```
out.print("\r\n");
    int k = 10;
out.print("\r\nk = ");
out.print(k);
out.print("\r\n\r\n");
```

它将k视为一个Java变量，为其赋值，并使用out JspWriter变量打印它。相比之下，如果相同的JSP页面将javascript作为language属性的值：

```
<%@ page language="javascript" %>
<%
    var k = 10;
%>
k = <%= k %>
```

那么生成的servlet会初始化一个JRun特定的脚本引擎并调用其evaluate方法，如下所示：

```
if (scriptEngine == null) {
    try {
        scriptEngine =
            ScriptEngineFactory.getScriptEngine("javascript");
        scriptEngine.init(pageContext);
    } catch (Exception e) {
        throw new ServletException
            ("Error initializing scripting engine.", e);
    }
```

```
if (request.getAttribute(SCRIPT_KEY) != null) {
    scriptEngine.init(
        pageContext,
        (String) request.getAttribute(SCRIPT_KEY),
        (String) request.getAttribute(DECLARATION_KEY));
}
scriptEngine.evaluate(pageContext);
```

显然，任何用JSP规范未明确要求的语言编写的JSP页面很可能无法在不同供应商的JSP容器之间移植。

### extends

通常，JSP容器为其从JSP页面生成的servlet提供父类。但是，规范允许你通过在页面指令的extends属性中指定另一个父类的完全限定名来对其进行子类化。这样做可以让你为一系列JSP页面提供额外的行为，而无需在页面中显式编码该行为。
JSP规范敦促在使用此功能时要谨慎，因为它可能会阻止JSP容器提供供应商特定的性能和可靠性增强。例如，JRun使用的标准JSP父类提供了确定依赖关系及其最后修改时间的方法。类似地，Tomcat实现了一个存储对专用类加载器引用的父类。如果你使用不同的父类，它应该提供比这些特性更重要的功能。

### JSP超类所需的接口

要使一个类用作JSP页面的超类，它必须实现以下接口之一：

- **javax.servlet.jsp.JspPage**：一个通用接口，不一定用于HTTP。很少有servlet直接实现此接口。
- **javax.servlet.jsp.HttpJspPage**：用于在HTTP协议下运行的JSP页面，此接口是JspPage的扩展。

这些接口定义了你必须实现的三个方法，如表10-1所述。

| 方法 | 描述 |
| :--- | :--- |
| `public void jspInit()` | 当JSP页面加载时，从servlet的`init()`方法自动调用此方法。虽然你必须实现此方法，但你的实现无需做任何事情。该方法被设计为一个占位符，由JSP页面子类覆盖以进行任何需要的初始化工作。 |
| `public void jspDestroy()` | 作为`jspInit()`的对应方法，当JSP页面类被卸载时，此方法从servlet的`destroy()`方法自动调用。 |
| `public void _jspService(request, response) throws ServletException, IOException` | 此方法是JSP请求处理逻辑的核心。它不能在JSP页面中显式定义，因为由JSP容器根据JSP的脚本小程序、表达式和指令生成该方法是JSP容器的工作。此方法在JSP父类中通常被声明为抽象方法。 |

*表10-1. 在JSP超类中需要声明的方法*

`_jspService`方法中请求和响应参数的确切类型由它们支持的协议决定。对于HTTP环境，这些类型是`javax.servlet.http.HttpServletRequest`和`javax.servlet.http.HttpServletResponse`。如果你正在实现不同的协议，则需要定义要在方法签名中使用的请求和响应类。

HttpJspPage扩展JspPage以提供特定于HTTP的行为。JspPage又扩展`javax.servlet.Servlet`，该接口定义了表10-2中列出的方法。



| 方法 | 描述 |
| :--- | :--- |
| `public void init(ServletConfig config) throws ServletException` | Servlet 首次加载时由 Servlet 容器调用的方法。 |
| `public ServletConfig getServletConfig()` | 返回 Servlet 的配置对象，该对象管理 Servlet 的初始化参数和 Servlet 上下文。 |
| `public void service(ServletRequest request, ServletResponse response) throws ServletException, IOException` | 由 Servlet 引擎调用以服务一个请求。 |
| `public String getServletInfo()` | 返回 Servlet 的描述。默认情况下，返回一个空字符串。 |
| `public void destroy()` | 当 Servlet 被卸载时由 Servlet 引擎调用。 |

**表 10-2.** *javax.servlet.Servlet 接口中的方法*

JSP 超类必须遵守并实现 JSP 协议。这要求：

-   `init()` 方法必须调用 `jspInit()`。
-   `destroy()` 方法必须调用 `jspDestroy()`。
-   `service()` 方法必须将其请求和响应参数转换为特定于协议的类，并调用 `_jspService()`。

这种实现可以是直接的，也可以是超类本身扩展了一个提供该实现的类，例如 `javax.servlet.http.HttpServlet`。

## JSP 超类示例

在得到充分警告并保持谨慎的前提下，如果你仍然想继续，本节提供了一个完整的示例。假设你有一系列 JSP 页面，它们都访问一个公共数据库。如果这些 JSP 页面不必费心加载 JDBC 驱动程序和建立数据库连接，可能会简化事情。下面的 Servlet 既能执行这些功能，又可以作为该系列 JSP 页面的父类。

```java
package jspcr.page;

import java.io.*;
import java.sql.*;
import javax.servlet.*;
import javax.servlet.http.*;
import javax.servlet.jsp.*;

/**
 * An example of a JSP superclass that can
 * be selected with the <CODE>extends</CODE>
 * attribute of the page directive. This servlet
 * automatically loads the JDBC-ODBC driver class
 * when initialized and establishes a connection
 * to the USDA nutrient database.
 */
public abstract class NutrientDatabaseServlet
    extends HttpServlet
    implements HttpJspPage
{
    protected Connection con;

    /**
     * Initialize a servlet with the driver
     * class already loaded and the database
     * connection established.
     */
    public void init(ServletConfig config)
        throws ServletException
    {
        super.init(config);
        try {
            Class.forName("sun.jdbc.odbc.JdbcOdbcDriver");
            con = DriverManager.getConnection("jdbc:odbc:usda");
        }
        catch (Exception e) {
            throw new UnavailableException(e.getMessage());
        }

        jspInit();
    }

    /**
     * Closes the database connection when
     * the servlet is unloaded.
     */
    public void destroy()
    {
        try {
            if (con != null) {
                con.close();
                con = null;
            }
        }
        catch (Exception ignore) {}

        jspDestroy();
        super.destroy();
    }

    /**
     * Called when the JSP is loaded.
     * By default does nothing.
     */
    public void jspInit()
    {
    }

    /**
     * Called when the JSP is unloaded.
     * By default does nothing.
     */
    public void jspDestroy()
    {
    }

    /**
     * Invokes the JSP's _jspService method.
     */
    public final void service(
        HttpServletRequest request,
        HttpServletResponse response)
        throws ServletException, IOException
    {
        _jspService(request, response);
    }

    /**
     * Handles a service request
     */
    public abstract void _jspService(
            HttpServletRequest request,
            HttpServletResponse response)
        throws ServletException, IOException;
}
```

在此示例中，驱动程序名称和数据库 URL 是硬编码的。在生产环境中，这些值应是可配置参数。要使用 `NutrientDatabaseServlet` 作为 JSP 超类，只需要将该类放入 JSP 容器的类路径中，并在 JSP 的 `page` 指令的 `extends` 属性中指定其全限定名，如下所示：

```jsp
<%@ page extends="jspcr.page.NutrientDatabaseServlet" %>

<%--
    This JSP page subclasses the NutrientDatabaseServlet
    parent class, which automatically loads the
    database driver and establishes the connection.
--%>

<%@ page import="java.io.*,java.sql.*" %>
<HTML>
<BODY>
<H3>Food Groups</H3>
<TABLE BORDER=1 CELLPADDING=3 CELLSPACING=0>
<TR><TH>Code</TH><TH>Description</TH></TR>
<%
    // Execute a query

    Statement stmt = con.createStatement();
    String sql = "SELECT * FROM FD_GROUP ORDER BY FDGP_DESC";
    ResultSet rs = stmt.executeQuery(sql);
    while (rs.next()) {
        String code = rs.getString(1);
        String desc = rs.getString(2);
%>
<TR>
    <TD><%= code %></TD>
    <TD><%= desc %></TD>
</TR>
<%
    }

    // Close the database objects

    rs.close();
    stmt.close();
%>
</TABLE>
</BODY>
</HTML>
```

请注意，JSP 不需要定义 `Connection` 对象。`Connection` 是超类的一个受保护变量，因此可以被其子类访问。

## import

`import` 属性用于描述 JSP 页面中使用的类的全限定名。这使得可以直接通过类名引用这些类，而无需添加包前缀。这是一个可选属性。

`import` 属性的值是一个逗号分隔的包名列表（每个以通配符字符串 `".*"` 结尾）和/或全限定类名。这些名称直接转换为生成的 Java Servlet 中的 `import` 语句。语法相当灵活。例如，要导入 `java.io`、`java.sql` 和 `java.util` 包中的所有类，你可以使用以下任何一种形式，

```jsp
<%@ page import="java.io.*,java.sql.*,java.util.*" %>
```

或分多行书写（因为换行符在字符串内视为空白字符），

```jsp
<%@ page import="
    java.io.*,
    java.sql.*,
    java.util.*
    "%>
```

或使用单独的 `page` 指令：

```jsp
<%@ page import="java.io.*" %>
<%@ page import="java.sql.*" %>
<%@ page import="java.util.*" %>
```

所有这些都会生成相同的 Java 代码，仅空白符有所不同：

```java
import java.io.*;
import java.sql.*;
import java.util.*;
```

请注意，导入类并不涉及加载任何东西；它只是一种简写方式，让你可以在 Java 方法内使用类名，而无需指定它们所属的包。如果你导入了 `java.util.*`，你可以写

```java
Vector names = new Vector();
```

而不是

```java
java.util.Vector names = new java.util.Vector();
```

这仅影响 Java 编译器，而不影响运行时类映像。你可以导入成千上万的类，但只有实际引用的类才会在运行时被需要。默认的导入列表包含四个包：

-   java.lang
-   javax.servlet
-   javax.servlet.http
-   javax.servlet.jsp

你不需要为这些包中的类提供 `import` 语句；也不需要用包名限定它们。

> 请记住，`import` 是唯一可以多次指定的 `page` 指令属性。

## session

页面指令的 `session` 属性指示该页面是否需要一个 HTTP 会话。有两个可能的值：

-   `session="true"`：如果页面需要 HTTP 会话。这是默认值。
-   `session="false"`：如果不需要 HTTP 会话。如果指定了此值，`session` 隐式变量将是未定义的，如果使用它将导致翻译错误。

如果你的 JSP 页面不需要会话，从性能角度考虑，指定 `session="false"` 是有价值的，这样就不会创建不必要的会话，从而节省内存和 CPU 周期。第 14 章详细介绍了 HTTP 会话和会话管理。

## buffer 和 autoFlush

`buffer` 和 `autoFlush` 属性用于描述 JSP 将采用的输出缓冲模型。`buffer` 属性可以是值 `"none"`，表示所有输出将直接写入 Servlet 响应对象的输出流，也可以是一个带有 `"kb"` 后缀的整数值。在后一种情况下，输出存储在内存中一个指定大小的缓冲区中。根据 `autoFlush` 是 `"true"` 还是 `"false"`，当缓冲区满时，要么输出会被刷新，要么会抛出缓冲区溢出异常。默认缓冲区大小为 8kb。表 10-3 总结了这两个属性每种组合的结果：

| 缓冲区 (Buffer) | 自动刷新 (AutoFlush) | 效果 |
|---|---|---|
| none | true | 字符在生成时立即写入 Servlet 响应输出流。 |
| none | false | 非法的组合。如果未启用缓冲区，`autoFlush="false"` 毫无意义。 |

**表 10-3.** *每种 Buffer 和 AutoFlush 组合的效果*



## 第10章：页面指令

| Buffer | AutoFlush | 效果 |
| :--- | :--- | :--- |
| 8kb | true | 使用8,192字节的缓冲区。当此缓冲区填满时，它将被自动刷新。这是默认值。 |
| 8kb | false | 使用8,192字节的缓冲区。当此缓冲区填满时，将抛出一个异常。 |
| *size*kb | true | 使用 *size* 乘以1,024字节的缓冲区。当此缓冲区填满时，它将被自动刷新。 |
| *size*kb | false | 使用 *size* 乘以1,024字节的缓冲区。当此缓冲区填满时，将抛出一个异常。 |

**表10-3.** *每种Buffer和AutoFlush组合的效果*（续）

JSP的要素

### # isThreadSafe

默认情况下，servlet引擎会加载servlet的单个实例，并使用线程池来服务各个请求。这意味着两个或更多线程可以同时执行相同的servlet方法。如果servlet具有实例变量，并且没有采取措施来同步对变量的访问，那么线程可能会发生冲突，并干扰彼此对变量的访问。

servlet API提供了一种解决此问题的方法——SingleThreadModel接口。此接口没有方法；它只是将servlet标记为需要为每个servlet实例分配一个专用线程¹。`page`指令的`isThreadSafe`属性提供了一种将`SingleThreadModel`与JSP页面关联起来的方式。

如果你指定`isThreadSafe="true"`，则你是在断言你已处理任何可能的线程冲突，因此JSP容器可以安全地同时将多个请求分派给servlet，

```
<%@ page isThreadSafe="true" %>
```

这会生成以下类签名：

```
public class jrun__Chap10__examples__isThreadSafe__ex12ejsp25
    extends allaire.jrun.jsp.HttpJSPServlet
    implements allaire.jrun.jsp.JRunJspPage
```

如果值为"false"，则JSP容器会生成一个实现了SingleThreadModel的servlet，

```
<%@ page isThreadSafe="false" %>
```

这会生成

```
public class jrun__Chap10__examples__isThreadSafe__ex22ejsp25
    extends allaire.jrun.jsp.HttpJSPServlet
    implements allaire.jrun.jsp.JRunJspPage, SingleThreadModel
```

如果未指定，`isThreadSafe`的值为"true"。

> **注意**
> SingleThreadModel的价值有限，因为它只防止servlet实例内部的线程冲突。没有任何方法可以防止JSP容器加载servlet的多个实例，每个实例都有一个专用线程。在这种情况下，对数据库和文件锁等外部资源的竞争显然仍然是不受管制的。仔细规划是唯一可靠的设计准则。

### # info

`page`指令的`info`属性允许你指定关于JSP页面的描述性信息，例如：

```
<%@ page info="Shopping Cart Checkout Page" %>
```

此属性的值被编译到类中，并可通过servlet的`getServletInfo()`方法获取。这允许servlet引擎在管理界面中为其servlet提供有用的描述。

### # contentType

JSP页面通常生成HTML输出，但也可以生成其他内容类型。通过在`page`指令中指定`contentType="value"`属性，你可以使HTTP Content-Type头返回给请求应用程序。考虑以下显示的简单JSP页面：

```
<%@ page contentType="text/plain" %>
Hello, world!
```

在JRun下，HTTP请求和响应可能如下所示：

```
GET /jspcr/Chap10/examples/contentType/ex1.jsp HTTP/1.0

HTTP/1.1 200 OK
Date: Wed, 28 Jun 2000 05:36:33 GMT
Server: Apache/1.3.12 (Win32)
Set-Cookie: jsessionid=7179962170594302;path=/
Expires: Thu, 01 Dec 1994 16:00:00 GMT
Connection: Keep-alive, close
Cache-Control: no-cache="set-cookie,set-cookie2"
Content-Length: 17
Content-Type: text/plain

Hello, world!
```

如果未指定contentType属性，请求和响应将如下所示：

```
GET /jspcr/Chap10/examples/contentType/ex2.jsp HTTP/1.0

HTTP/1.1 200 OK
Date: Wed, 28 Jun 2000 05:40:15 GMT
Server: Apache/1.3.12 (Win32)
Set-Cookie: jsessionid=210659962170816161;path=/
Expires: Thu, 01 Dec 1994 16:00:00 GMT
Connection: Keep-alive, close
Cache-Control: no-cache="set-cookie,set-cookie2"
Content-Length: 15
Content-Type: text/html; charset=ISO-8859-1

Hello, world!
```

除了内容类型外，还可以使用以下语法指定字符集：

```
<%@ page contentType="type/subtype; charset=charset" %>
```

### # errorPage 和 isErrorPage

如果在评估JSP页面时发生异常，servlet引擎通常会将堆栈跟踪信息转储到浏览器。这在开发期间可能对程序员有帮助，但在商业Web应用程序中是不可取的。JSP提供了一个简单便捷的解决方案，需要协调使用两个属性：errorPage和isErrorPage。

一个JSP页面可以指示当抛出未捕获的异常时应显示特定的错误页面，

```
<%@ page errorPage="error_url" %>
```

其中error_url是同一servlet上下文中另一个JSP页面的URL。该JSP页面必须在其页面指令中使用以下属性：

```
<%@ page isErrorPage="true" %>
```

错误页面可以通过隐式变量`exception`<sup>2</sup>访问异常。它可以使用exception.getMessage()提取错误消息文本，并根据需要显示或记录它。它还可以使用exception.printStackTrace()生成堆栈跟踪。

该页面无需精心设计。它可能只是报告异常：

```
<%@ page isErrorPage="true" session="false"%>

<H3>应用程序错误</H3>

错误消息是：

<B><%= exception.getMessage() %></B>
```

这可以作为占位符，在开发过程后期进行充实，例如添加公司徽标以及后续操作说明。因为错误页面本身就是一个JSP页面，它可以访问servlet上下文、会话（如果有）、请求和其他servlet对象。这使得该页面能够捕获诊断信息，可能将其转发给技术支持人员。以下是这样一个错误页面的示例：

```
<%@ page isErrorPage="true" session="false"%>

<HTML>
<HEAD><TITLE>错误跟踪页面</TITLE></HEAD>
<BODY>
<CENTER>
<FONT SIZE="+3">
<B><I><U>Monolithic<BR>Technologies Corporation</U></I></B>
</FONT>
<P>
您发现了一个我们未知的缺陷：
<B><%= exception.getMessage() %></B>
<P>

<%-- 创建一个提交给技术支持的表单 --%>

<FORM ACTION="/send_diags.jsp">
<INPUT TYPE="submit" VALUE="请点击此处">
<P>
以将此信息发送给
我们的技术支持部门：
<P>

<%-- 提供日期、时间和servlet名称 --%>

<%
    String dateTime      = new java.util.Date().toString();
    String remoteAddr    = request.getRemoteAddr();
    String servletContext = request.getContextPath();

%>
<TABLE BORDER="1" CELLPADDING="3" CELLSPACING="0">
<TR>
    <TD><B>日期和时间：</B></TD>
    <TD><%= dateTime %>
    <INPUT TYPE="hidden"
           NAME="bug.dateTime"
           VALUE="<%= dateTime %>">
</TD>
</TR>
<TR>
    <TD><B>Web客户端：</B></TD>
    <TD><%= remoteAddr %>
    <INPUT TYPE="hidden"
           NAME="bug.remoteAddr"
           VALUE="<%= remoteAddr %>">
    </TD>
</TR>
<TR>
    <TD><B>应用程序：</B></TD>
    <TD><%= servletContext %>
    <INPUT TYPE="hidden"
           NAME="bug.servletContext"
           VALUE="<%= servletContext %>">
    </TD>
</TR>
</TABLE>

<%-- 将堆栈跟踪作为隐藏字段包含在内 --%>

<INPUT TYPE="hidden" NAME="bug.stackTrace"
       VALUE="<%
java.io.PrintWriter pw = new java.io.PrintWriter(out);
exception.printStackTrace(pw);
      %>"

</FORM>
</CENTER>
</BODY>
</HTML>
```

这个名为`TrackingErrorPage.jsp`的页面显示与异常相关的错误消息，以及日期、时间、客户端的IP地址和Web应用程序名称。它提供了一个按钮，使用户能够将此信息连同堆栈跟踪一起转发给技术支持部门（使用其他未在此处显示的JSP页面）。此应用程序中的JSP页面随后应在其页面指令中包含对错误页面的引用：

¹ 第14章更详细地讨论了线程问题。

² 这是JSP页面可以访问此变量的唯一情况。



## 摘要

页面指令允许页面作者向JSP容器提供指令。本章描述了可以指定的每个属性的操作方式：

- `language` 脚本语言（默认为java）
- `extends` 页面的专用超类
- `import` 生成的servlet应可见的包和类
- `session` 是否创建HTTP会话对象
- `buffer` 输出缓冲模型
- `autoFlush` 缓冲区满时是刷新缓冲区还是抛出异常
- `isThreadSafe` 是否实现SingleThreadModel
- `info` 在开发工具中显示的页面描述
- `contentType` JSP响应使用的字符编码
- `isErrorPage` 是否提供对隐式异常变量的访问
- `errorPage` 处理未捕获异常的页面的URL

本页有意留白。

## 完整参考

## 第11章

## JSP标签扩展

JavaServer Pages 1.1规范通过使扩展页面创作环境使用自定义标签成为可能，显著增强了JSP架构。*自定义标签*是类似XML的JSP页面语法和语义的扩展，由用户编写的标签处理器支持。标签集合被组织为*标签库*，可以打包为JAR文件，从而使其功能能够轻松地在任何符合JSP 1.1规范的servlet引擎上分发和安装。

本章介绍自定义标签，概述其作用和优势。它提供了一个扩展的分步示例，说明如何编写和部署自定义标签，然后深入探讨标签库、标签库描述符、标签扩展API和标签处理器的细节。本章探讨了几个标签环境示例，并最终实现了第一个示例中给出的数据库查询标签。

## 为什么使用自定义标签？

大多数程序员可以编写普通的HTML，大多数Web设计师可以学习编写简单的JSP页面。但真正优秀的、包含导航、浏览器检测、图像处理和表单交互的HTML需要知识丰富的作者——专家。<sup>1</sup> 同样，访问数据库、处理事务和与套接字通信的Java编程超出了HTML作者的能力范围。

自定义标签提供了一种弥合这两个专业之间鸿沟的方法。Java程序员可以提供方便的包，其中包含应用程序功能，Web设计师可以将其用作构建模块。虽然JavaBean也可以封装代码，但它们作为属性的仓库最为有用。迭代、嵌套或协作动作的概念很难用Bean来表达。自定义标签使得更高级别的、特定于应用程序的JSP开发方法成为可能。

例如，使用自定义标签编写的数据库查询可能如下所示，

```
<db:connect url="mydatabase">
    <db:runQuery>
        SELECT *
        FROM    FD_GROUP
        WHERE   FdGp_Desc LIKE '%F%'
        ORDER BY FdGp_Cd
    </db:runQuery>
    <table border="1" cellpadding="3" cellspacing="0">
        <tr><th>Food Group Code</th><th>Description</th></tr>
        <db:forEachRow>
            <tr>
                <td><db:getField name="FdGp_Cd"/></td>
                <td><db:getField name="FdGp_Desc"/></td>
            </tr>
        </db:forEachRow>
    </table>
</db:connect>
```

其中connect、runQuery、forEachRow和getField是面向应用程序的自定义标签。

<sup>1</sup> 访问http://www.cnn.com或http://www.msnbc.com并查看HTML源代码。你认为你能编写其中多少内容？

前面示例中的所有逻辑本可以使用嵌入在JSP页面中的脚本片段来编写。例如，与`<db:connect>`标签等效的代码可能包括加载驱动程序类、打开与数据库的连接（可能从连接池获取现有连接）、设置Statement和ResultSet对象以及处理可能抛出的任何异常。另一种可能是将大部分逻辑包含在JavaBean中，尽管遍历结果集仍然需要脚本片段代码。这两种替代方案都不如将逻辑打包成一组类似HTML的标签方便，这些标签的功能对Web设计师和servlet开发人员都一目了然。

除了内容和表示的分离，自定义标签的其他优点包括：

- **简单性** 将复杂任务表达为具有各自属性和控制流的协作子任务集，比将其编写为一个整体代码块要容易得多。这不仅编码更容易，而且理解也更容易。例如，在前面的数据库查询中，很容易正确猜测数据库连接的范围，`<db:runQuery>`块创建了一个隐式结果集，并且`<db:forEachRow>`遍历此结果集。
- **代码重用的机会** Web应用程序中可能有数百个数据库查询。不借助`<%@ include %>`指令就很难共享脚本片段代码，这些指令会模糊逻辑并可能产生不良的副作用。标签库使得打包标准代码并在整个应用程序中共享它变得更容易。
- **适合创作工具** *集成开发环境*（IDE）只能将脚本片段块视为ASCII文本块。然而，自定义标签由于具有标签库描述符，便于开发工具管理，开发工具可以显示其描述、验证其属性等。

为了更好地理解如何开发自定义标签，让我们以一个简单的例子为例，逐步介绍其开发过程。

## 开发你的第一个自定义标签

我们抵制编写“Hello, World!”标签的诱惑，将开发一个略微有用的组件示例——一个检索Web服务器名称和版本的自定义标签。此标签以及我们开发的所有其他标签的实现将遵循以下四个基本步骤：

1. 定义标签。
2. 在标签库描述符中编写条目。
3. 编写标签处理器。
4. 在JSP页面中使用该标签。

## 步骤1 — 定义标签

首先，我们需要清楚地定义标签的语法。这需要回答以下问题：

- 标签的名称是什么？正如我们稍后将看到的，自定义标签始终与命名空间限定符一起使用，因此不需要使标签名称全局唯一。
- 它有哪些属性？例如，HTML `<TABLE>`标签具有可选属性BORDER、CELLPADDING、CELLSPACING和WIDTH（以及其他）。自定义标签可以定义任意数量的必需或可选属性，这些属性在标签被求值时传递给标签处理器。
- 标签是否会定义脚本变量？例如，标准操作`<jsp:useBean id="xyz" class="jspcr.beans.XYZBean">`会导致定义一个名为xyz、类型为`jspcr.beans.XYZBean`的变量。然后，此变量可用于`<jsp:getProperty>`和`<jsp:setProperty>`操作，以及后续任何脚本片段或表达式中的Java代码。自定义标签可以以相同的方式创建脚本变量。
- 标签是否对其开始和结束标签之间包含的正文执行任何特殊操作？例如，HTML `<TABLE>`标签在其结束标记`</TABLE>`之前期望表格行和表格单元格。这些元素中的每一个都依赖于评估堆栈中上方相关元素提供的信息。自定义标签应用程序同样可以具有嵌套标签，协作执行某些功能。标签正文也可以包含非JSP数据（如SQL语句），这些数据由标签求值。



对于第一个示例标签，没有什么太多需要处理的。我们将这个标签命名为 `getWebServer`。它没有属性，因为它不需要在不同JSP页面中进行不同的配置。该标签没有定义脚本变量，只是返回包含Web服务器名称的字符串，以替代 `getWebServer` 标签。最后，该标签没有需要处理的主体，因为它的全部功能都包含在其开始标签中。

## 第2步—创建TLD条目

*标签库描述符 (TLD)* 是一个XML文档，它定义了一组相关标签的名称和属性。下面是我们将与 `getWebServer` 示例标签一起使用的TLD：

```xml
<?xml version="1.0" ?>
<taglib>
    <tlibversion>1.0</tlibversion>
    <jspversion>1.1</jspversion>
    <shortname>diag</shortname>
    <tag>
        <name>getWebServer</name>
        <tagclass>jspcr.taglib.diag.GetWebServerTag</tagclass>
        <bodycontent>empty</bodycontent>
    </tag>
</taglib>
```

在本章后面，我们将详细探讨TLD，但这里需要关注的关键点是，TLD将标签名称映射

```xml
<name>getWebServer</name>
```

到一个完全限定的类名：

```xml
<tagclass>jspcr.taglib.diag.GetWebServerTag</tagclass>
```

JSP容器在编译时评估自定义标签时，使用此映射来生成相应的servlet代码。

我们将把这个文件命名为 `diagnostics.tld`。出于本示例的目的，我们唯一需要关心的是将文件复制到正确的位置。TLD可以放置在Web应用程序目录系统中的任何位置，但将其放在 `WEB-INF` 目录下是有意义的，因为它不会被设置为可直接公开访问。按照惯例，TLD通常安装在名为 `/WEB-INF/tlds` 的目录中。例如，如果有一个名为 `test` 的Web应用程序，那么 `diagnostics.tld` 将在 `/test/WEB-INF/tlds/` 中找到。相对于servlet上下文写成URI形式，就是 `/WEB-INF/tlds/diagnostics.tld`。

## 第3步—编写标签处理器

标签的操作在一个称为 *标签处理器* 的Java类中实现。标签处理器的实例由JSP容器创建和维护，并且从JSP页面生成的servlet中直接调用这些类中的预定义方法。

在示例标签中，我们需要获取Web服务器的名称（例如，Apache、Microsoft IIS、Netscape Enterprise等）。Servlet API没有提供明显的方法来获取此信息。请求对象提供了很多关于Web客户端的信息，servlet上下文知道servlet引擎的情况，但这些对象似乎都不知道是哪个软件产品恰好在监听端口80。然而，当Web服务器将HTTP响应发送回Web客户端时，它本身会提供此信息。我们将采取的方法是在标签处理器中自己发起一个虚拟的HTTP请求，然后从返回的HTTP头中提取服务器信息。

以下是标签处理器的完整源代码：

```java
package jspcr.taglib.diag;

import javax.servlet.http.*;
import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.*;
import java.net.*;

/**
 * Handler for the "getWebServer" tag
 */
public class GetWebServerTag extends TagSupport
{
    public int doStartTag() throws JspException
    {
        try {
            // Get the request object from the page context
            HttpServletRequest request =
                (HttpServletRequest) pageContext.getRequest();
            // Request information from web server
            URL url = new URL("http",
                request.getServerName(),
                request.getServerPort(),
                "/");
            URLConnection con = url.openConnection();
            ((HttpURLConnection) con).setRequestMethod("OPTIONS");
            String webserver = con.getHeaderField("server");

            // Write it to the output stream
            JspWriter out = pageContext.getOut();
            out.print(webserver);
        }
        catch (IOException e) {
            throw new JspException(e.getMessage());
        }
        return SKIP_BODY;
    }
}
```

让我们详细看看源代码，了解我们期望它做什么。

```java
package jspcr.taglib.diag;
```

第一行标识了包名。严格来说，将代码放入包中并非必须，但它有助于组织相关类，并使Javadoc文档更有意义。此外，一些JSP引擎不能正确为自定义标签生成导入语句，因此没有包名的类可能导致生成的servlet中出现编译错误。

```java
import javax.servlet.http.*;
import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.*;
import java.net.*;
```

简单的标签处理器通常只需要导入 `javax.servlet.jsp` 和 `javax.servlet.jsp.tagext` 包，以及 `java.io.IOException` 类。在这种情况下，我们需要 `javax.servlet.http` 中的 `HttpServletRequest` 类，以及 `java.net` 中的几个类。

```java
public class GetWebServerTag extends TagSupport
```

标签处理器需要实现 `Tag` 接口或 `BodyTag` 接口，这两个接口都在 `javax.servlet.jsp.tagext` 包中。`BodyTag` 是 `Tag` 的子接口。虽然标签作者可以自由地直接实现这些接口，但通常更方便的是扩展默认实现类 `TagSupport` 或 `BodyTagSupport` 之一，只重写当前任务所需的方法。示例标签不支持标签主体，因此我们简单地扩展 `TagSupport` 类。

```java
public int doStartTag() throws JspException
```

当遇到开始标签时调用此方法，在为其指定的任何属性在标签处理器中设置之后，但在处理标签主体之前。在这种情况下，没有主体也没有属性，因此所有代码都将包含在 `doStartTag()` 方法中。请注意，如果代码遇到问题，此方法允许你抛出 `JspException`。因为我们将访问可能抛出 `java.io.IOException` 的网络类，所以我们将整个方法放在一个 `try ... catch` 块中，将其转换为 `JspException` 供JSP容器处理。同样，请注意，该方法返回一个整数返回代码（稍后详述）。

```java
HttpServletRequest request =
    (HttpServletRequest) pageContext.getRequest();
```

为了向Web服务器发送HTTP请求，我们需要知道我们收到的请求的主机名和端口号。此信息可以在 `request` 对象中找到，该对象可以从 `pageContext` 对象获取。细心的读者会注意到，`pageContext` 在此类中没有定义。原因是它在 `TagSupport` 超类中被定义为 `protected` 字段，这使得它对我们这样的子类可访问。此变量在调用 `doStartTag()` 之前设置，当调用 `TagSupport.setPageContext()` 方法时²。

```java
URL url = new URL("http",
    request.getServerName(),
    request.getServerPort(),
    "/");
URLConnection con = url.openConnection();
((HttpURLConnection) con).setRequestMethod("OPTIONS");
String webserver = con.getHeaderField("server");
```

> ² 阅读 `TagSupport` 和 `BodyTagSupport` 的源代码会有所帮助。这些都是相当小的类，看看页面上下文和主体内容变量从哪里来，以及 `findAncestorWithClass` 如何工作是很有启发性的。源代码通常可以从获取 `servlet.jar` 类的地方获得。

我们使用 `java.net.URL` 的4参数构造函数，它接受协议名称、服务器名称、端口号和路径，并由此我们获得一个 `URLConnection` 对象。因为我们实际上并不关心任何特定文件的内容，所以我们指定 OPTIONS 方法而不是 `GET` 或 `POST`。我们也可以使用 `HEAD`，它本质上与 `GET` 相同，但只返回头部。然而，有时Web服务器报告 `HEAD` 不是受支持的方法。对于任何符合 `HTTP/1.1` 的Web服务器，`OPTIONS` 都应该有效（毕竟，其目的是返回Web服务器确实支持的请求方法列表）。调用连接对象的 `getHeaderField()` 方法会导致请求被发送，并读取响应中适当的HTTP头。

```java
JspWriter out = pageContext.getOut();
out.print(webserver);
```

在将所需信息捕获到 `webserver` 变量中后，我们可以简单地将其写入当前servlet输出流，该流可以从页面上下文获取。效果是，JSP页面中使用的 `getServer` 标签被从HTTP请求获取的服务器信息所替代。

```java
return SKIP_BODY;
```

最后，我们退出该方法，返回整数常量 `SKIP_BODY`，该常量在 `Tag` 接口中定义。因为我们已将此标签定义为没有主体，所以不需要评估它，并且如果指定了任何其他返回代码，JSP页面将抛出运行时异常。

## 编译示例代码

这完成了标签处理器。源代码文件必须命名为 `GetWebServerTag.java`，其编译后的类必须具有完全限定名 `jspcr.taglib.diag.GetWebServerTag`。确保这一点的简单方法是在Web应用程序的 `/WEB-INF/classes` 目录下创建适当的目录集：

```
/WEB-INF/classes/jspcr/taglib/diag
```

并将 `.java` 源文件放在 `diag` 目录中。可以从 `/WEB-INF/classes` 目录使用以下命令编译程序：

```
javac jspcr/taglib/diag/GetWebServerTag.java
```

需要适当确保 `servlet.jar` 文件位于类路径中的某个位置。这应该会在与 `GetWebServerTag.java` 相同的目录中放置一个 `GetWebServerTag.class` 文件。如果情况并非如此，请确保 `package` 语句输入正确。



## 第4步—将标签整合到JSP页面中

至此，该标签已可使用。以下JSP页面（ShowServer.jsp）展示了如何实现这一点：

```
<%@ taglib prefix="diag" uri="/WEB-INF/tlds/diagnostics.tld" %>

<HTML>

<HEAD>
<TITLE>Basic Example of a Custom Tag</TITLE>
</HEAD>

<BODY>
<H3>Basic Example of a Custom Tag</H3>
The web server is <diag:getWebServer/>
</BODY>

</HTML>
```

## taglib指令

第一行包含taglib指令：

```
<%@ taglib prefix="diag" uri="/WEB-INF/tlds/diagnostics.tld" %>
```

该指令必须出现在JSP页面中引用的任何自定义标签之前。页面顶部是一个好位置。

## 如何在JSP页面中使用标签

网页的其余部分是传统的HTML，除了指定自定义标签的那一行：

```
The Web server is <diag:getWebServer/>
```

当ShowServer.jsp首次被调用时，JSP容器使用taglib指令中的信息来定位标签库描述符，并识别此页面上使用其标签的位置。当生成的servlet接收到请求时，它会产生以下HTML，

```
<HTML>

<HEAD>
<TITLE>Basic Example of a Custom Tag</TITLE>
</HEAD>

<BODY>
<H3>Basic Example of a Custom Tag</H3>

The web server is Apache/1.3.12 (Win32)

</BODY>

</HTML>
```

当然，这取决于所涉及的实际Web服务器。结果如图11-1所示。

值得注意的是，JSP页面中使用的自定义标签必须遵守严格的XML规则：

-   1. 所有标签必须完整闭合，要么通过匹配的结束标签，
    <diag:name>
    ...
    </diag:name>
-   2. 要么通过简写形式（如果没有标签体）：
    `<diag:name/>`。
-   3. 所有属性值必须用引号括起来，即使是数字属性：
    `<diag:for id="I" start="1" end="10">`
    ...
    `</diag:for>`
-   4. 嵌套标签不能重叠；以下写法
    `<diag:A>`
    `<diag:B>`
    `</diag:A>`
    `</diag:B>`
    是非法的。
-   5. 标签和属性名称区分大小写。

## JSP: 权威指南

## 标签处理器如何工作

标签处理器是一个Java类，它通过实现一组JSP容器调用的预定义方法来执行自定义标签的动作。在本节中，我们将了解标签处理器的结构、它实现的接口、其生命周期，以及它如何与属性和脚本变量协同工作。我们还将探讨协作标签和嵌套标签，并展示它们如何交互。然而，首先让我们回顾一下JSP容器如何翻译和调用JSP页面。

## JSP容器所做的工作

回顾一下，JSP页面以三种形式存在：

-   ■ **.jsp文件**    页面作者编写的原始源文件，可能包含HTML、脚本片段、表达式、声明、动作标签和指令。
-   ■ **.java文件**    与.jsp文件等效的servlet的Java源代码。此servlet由JSP容器生成。
-   ■ **.class文件**    生成的Java servlet的编译形式。

当HTTP客户端请求JSP页面时，JSP容器会检查.jsp和.java文件的修改日期。如果.java文件不存在，或者它比.jsp文件更旧（如果JSP页面被修改过，就会发生这种情况），JSP容器会重新创建Java servlet并进行编译。在此步骤中，会发生以下转换：

-   ■ `<%@ page %>`、`<%@ include %>` 和 `<%@ taglib %>` 指令向JSP容器提供翻译时信息。
-   JSP表达式和HTML行按其出现顺序被翻译成 `_jspService()` 方法中的 `out.print()` 语句。
-   脚本片段被原样复制到 `_jspService()` 中。
-   声明被原样复制到 `_jspService()` 之外的源代码中。
-   标准JSP动作（如 `<jsp:include>`、`<jsp:useBean>` 和 `<jsp:setProperty>`）被翻译成执行其功能的运行时逻辑。
-   自定义标签被展开为调用其相应标签处理器中方法的Java语句。

## 容器生成的标签相关代码

容器使用taglib指令来定位标签库描述符（TLD），并根据使用的标签前缀将其与页面中使用的自定义标签匹配。例如，如果指令是

```
<%@ taglib prefix="db"
    uri="/WEB-INF/tlds/database.tld" %>
```

那么容器读取 `database.tld` 文件以获取其描述的标签列表以及每个标签关联的标签处理器类的名称。当它在页面中遇到带有命名空间前缀的标签时，

```
<db:connect url="mydatabase">
```

它会查找与该前缀关联的标签库，该标签库包含具有指定名称的标签。容器使用它在TLD中找到的关于标签结构的信息，生成一系列实现该标签功能的Java语句。对于前面显示的 `db:connect` 标签，这将包括

-   1. 创建 `connect` 标签处理器实例或从池中获取实例的代码。
-   2. 将 `pageContext` 对象的引用传递给 `connect` 标签处理器的代码。这是一个有用的功能，因为它使标签处理器能够访问JSP页面的Request、Response、HttpSession、ServletContext和输出流对象。这也意味着标签处理器可以获取或设置页面上下文管理的任何级别的属性。
-   3. 如果 `db:connect` 嵌套在另一个自定义标签中，则传递父标签引用的代码。
-   4. 调用 `connect` 标签处理器的 `setUrl()` 方法，传递 "mydatabase" 值。
-   5. 调用名为 `doStartTag()` 的方法，`connect` 标签处理器实现此方法以在遇到其开始标签时执行任何操作（稍后将详细介绍）。

## 标签处理器做什么

在JSP页面的正文中，一个自定义标签可能看起来像这样：

```
<app:mail from="Accounting Manager" to="Staff" >
    <app:subject>Expense Reports</app:subject>
    Please be sure to submit all expense reports before
    the fifteenth day of the month to allow sufficient
    processing time.  Thanks.
</app:mail>
```

此标签的组件包括：

-   一个开始标签 <app:mail ...>，带有一个或多个属性
-   一个结束标签 </app:mail>
-   开始标签和结束标签之间的行，称为标签的*主体*，可能包含普通文本或其他JSP语句。

在将标签转换为servlet代码时，容器为这些组件中的每一个调用标签处理器，并使用pageContext对象与处理器共享属性。这些方法的调用有时被称为标签处理器的*生命周期*。为此，标签处理器必须实现以下两个接口之一：

-   javax.servlet.jsp.tagext.Tag，用于不操作其主体的标签。
-   javax.servlet.jsp.tagext.BodyTag，用于操作其主体的标签。BodyTag是Tag的子接口。

这些接口指定了标签处理器必须提供的生命周期方法。

API还提供了两个支持类——TagSupport和BodyTagSupport——它们作为这两个接口的默认实现。大多数标签处理器扩展这些支持类，而不是直接实现接口，尽管这些接口并不特别复杂。使用支持类的一个好处是你只需要覆盖需要更改的方法，而让支持类处理其余部分。此外，支持类可以负责在受保护的变量中保存页面上下文和主体内容对象，因此子类可以简单地访问它们。

> 3 一个标签不一定要有主体。标签可以简单地根据开始标签中指定的属性执行其功能。在这种情况下，使用简写 `<tag ... />` 表示法是很常见的。

## 标签库

自定义标签在一个称为*标签库*的结构中实现和分发，有时也称为*taglib*。标签库是一个类和元信息的集合，包括

-   **标签处理器** 实现自定义标签功能的Java类。
-   **标签附加信息** 为JSP容器提供验证标签属性和创建脚本变量的逻辑的类。
-   **标签库描述符（TLD）** 一个XML文档，描述各个标签的属性以及整个标签库的属性。

标签库的组件可以安装在任何对JSP容器可访问的位置。标签处理器和标签附加信息类需要位于JSP容器类加载器可以找到的位置。标签库描述符可以位于任何可以通过URL定位的位置。然而，为了方便部署，JSP 1.1规范要求JSP容器必须接受打包为具有特定固定结构的JAR文件的标签库。在此类JAR文件中，类应位于从根目录开始、匹配其包结构的目录树中，并且TLD必须是 `/META-INF` 目录中名为 `taglib.tld` 的文件。这意味着标签库可以通过简单地将其JAR文件复制到 `/WEB-INF/lib` 目录来部署。或者，可以将类解压到 `/WEB-INF/classes` 目录，并将TLD放置在另一个Web可访问的位置。这通常是一个名为 `/WEB-INF/tlds` 的目录，尽管这只是约定，而非要求。

## 标签库描述符（TLD）

JSP容器所需的标签库配置信息存储在*标签库描述符（TLD）*中。TLD是一个XML文档，描述库中的各个标签、它们的标签处理器和属性，以及整个库的版本和标识信息。

## TLD元素

标签库描述符的*文档类型定义（DTD）*可以在http://java.sun.com/j2ee/dtds/web-jsptaglibrary_1_1.dtd找到。一个有效的TLD由一个单一的 `<taglib>` 元素组成，该元素按固定顺序包含某些子元素：

-   `tlibversion` 是一个必需的元素，包含标签库的版本号。这是一个由最多四组数字组成的点分十进制数，数字之间用小数点分隔，例如“1.0”或“1.3.045”。



`jspversion` 是一个可选元素，用于标识支持该标签库所需的最低 JSP 规范级别。例如，对于 JSP 1.1 版本，该值应为 "1.1"。

`shortname` 是一个简短的描述性名称，用于标识该标签库。JSP 创作工具可能会将此名称用作该库标签的默认前缀。DTD 规定此名称不应包含空白字符，并且必须以字母字符开头；然而，在实践中，关于空白字符的限制似乎被广泛忽视。`shortname` 是一个必需元素。

`uri` 是一个可选元素，用于定义一个唯一的 URI，以标识此库。这通常是可下载最新版本标签库的位置的 URL。

`info` 是一个可选元素，用于输入关于标签库的描述性信息。这旨在供 JSP 创作工具中的人工查看。

`tag` 一个 TLD 中可以包含一个或多个 `tag` 条目。这些条目描述了构成该库的各个标签。

一个 `tag` 元素本身最多包含六种类型的子元素：

- `name`：将在 JSP 页面中使用的标签名称。与标识标签库的命名空间前缀一起使用时，该名称唯一标识了 JSP 容器中的一个标签。
- `tagclass`：一个必需元素，包含实现该标签的标签处理程序的完全限定名。
- `teiclass`：一个可选元素，包含此标签使用的 *标签额外信息* (TEI) 类的完全限定名（如果有的话）。TEI 类提供了关于标签处理程序创建的脚本变量以及可以对标签属性执行的任何验证的信息。
- `bodycontent`：可选地描述标签处理程序如何使用其主体内容。可能的值有
    - `empty`：标签主体必须为空
    - `JSP`：标签主体由其他 JSP 元素组成
    - `tagdependent`：标签主体由标签本身解释，不进行 JSP 转换
- `info`：关于该标签的可选的、人类可读的描述性信息。
- `attribute`：关于在 JSP 页面中使用该标签时可编码的属性的可选信息。此条目将在本章后面的“定义标签属性”部分中有更完整的描述。

## taglib 指令

taglib 指令的目的是指定 TLD 的位置，并为其分配一个短别名（前缀），以区分其在当前页面上的标签。其语法如下：

```
<%@ taglib prefix="tag prefix" uri="taglibURI" %>
```

其中两个属性分别是

`tag prefix`：一个在此页面上唯一的名称，用于标识来自此库的标签。例如，如果前缀是 `diag`，那么此页面上使用的来自此标签库的任何标签都应写作 `<diag:xxx>`，其中 `xxx` 是标签名称。前缀可以是任何有效的 XML 名称令牌，尽管 Sun Microsystems 保留了前缀 `jsp`、`jspx`、`javax`、`servlet`、`sun` 和 `sunw`。

`taglibURI`：标签库本身的 URI。这可以是以 `/` 开头的绝对路径名，如前例所示，相对于 Web 应用程序的根目录进行解释。或者，它可以是一个充当 TLD 符号名称的 URL。在这种情况下，该名称必须通过 `web.xml` 文件中的 `<taglib>` 条目映射到实际的 TLD。这种方法将在下一节中讨论。

## 在 web.xml 文件中映射标签库

假设包含版本 3.8.2 标签库类和 TLD 的 JAR 文件名为 `util_v3_8_2.jar`，并部署在 Web 应用程序的 `/WEB-INF/lib` 目录中。可以按如下方式直接引用此标签库的 taglib 指令：

```
<%@ taglib
    prefix="util"
    uri="/WEB-INF/lib/util_v3_8_2.jar"
%>
```

当然，当安装版本 3.8.3 时，这意味着所有使用此标签库的 JSP 都必须更新为新的版本号。一种替代方法是将 TLD 的物理位置映射到一个可用于 taglib 指令的符号名称。这是通过在此 Web 应用程序的 `/WEB-INF/web.xml` 部署描述符中添加一个 `<taglib>` 元素来完成的。对于前面的例子，此元素将具有以下结构：

```
<taglib>
    <taglib-uri>uri</taglib-uri>
    <taglib-location>
        /WEB-INF/lib/util_v3_8_2.jar
    </taglib-location>
</taglib>
```

其中 `uri` 可以是任何有效的 URI，可能是一个类似文件的助记名称，如 `/util-taglib`，或者是可以找到最新版本标签库的位置的 URL。这使得可以将 taglib 指令编码为

```
<%@ taglib
    prefix="util"
    uri="http://www.vendor.com/taglibs/util"
%>
```

请注意，该 URI 不必指向实际文件。相反，它是一个唯一的标识符，使 JSP 容器能够在 `web.xml` 中搜索实际的文件位置。另请注意，此映射技术仅适用于按指定格式（TLD 位于 `/META-INF/taglib.tld`）编码的 JAR 文件，并且已知一些 JSP 容器实现在这方面存在错误。如有疑问，您总是可以将 JAR 文件放在 `/WEB-INF/lib` 中，将 TLD 放在 `/WEB-INF/tlds` 中，并在 JSP 页面中直接引用 `/WEB-INF/tlds/filename.tld`。

## 标签处理程序 API

以下部分描述了与 `Tag` 接口和 `TagSupport` 类相关联的方法。

## Tag 接口

表 11-1 列出了实现 `Tag` 接口的类必须支持的生命周期方法。该接口还包括四个常量，它们代表 `doStartTag()` 和 `doEndTag()` 方法可能的返回码：

- `EVAL_BODY_INCLUDE`：当 `doStartTag()` 返回此值时，表示页面实现 servlet 应评估标签主体。
- `SKIP_BODY`：当 `doStartTag()` 返回此值时，表示 servlet 应忽略此标签的主体。
- `EVAL_PAGE`：当 `doEndTag()` 返回此值时，表示页面的其余部分应照常评估。
- `SKIP_PAGE`：当 `doEndTag()` 返回此值时，表示页面的其余部分应被跳过。

**表 11-1. Tag 接口中的方法**

| 方法 | 描述 |
| :--- | :--- |
| `public void setPageContext(PageContext ctx)` | 生成的 servlet 在要求处理程序执行任何其他操作之前首先调用此方法。实现类应保存上下文变量，以便在标签生命周期的任何时刻都可以使用它。通过页面上下文，标签处理程序可以访问所有 JSP 隐式对象，并可以在任何范围内获取和设置属性。 |
| `public void setParent(Tag parent)` | 使标签能够在求值堆栈中找到其上方的标签。在 `setPageContext` 之后立即调用。 |
| `public Tag getParent()` | 返回父标签。 |
| `public int doStartTag() throws JspException` | 在设置了页面上下文、父标签和起始标签上编码的任何属性之后调用。返回码表示 JSP 实现 servlet 应评估标签主体 (`EVAL_BODY_INCLUDE`) 还是不评估 (`SKIP_BODY`)。该方法可以抛出 `JspException` 以指示致命错误。 |
| `public int doEndTag() throws JspException` | 在遇到结束标签时调用。返回码表示 JSP 实现 servlet 应继续处理页面的其余部分 (`EVAL_PAGE`) 还是不继续 (`SKIP_PAGE`)。该方法可以抛出 `JspException` 以指示致命错误。 |
| `public void release()` | 保证在页面退出之前调用。允许标签处理程序释放其持有的任何资源并重置其状态，以便在必要时可以重用。 |

## TagSupport 类

`javax.servlet.jsp.tagext.TagSupport` 是一个实现 `Tag` 接口的具体类。除了该接口外，`TagSupport` 类还提供了表 11-2 中列出的附加方法。

扩展此类而不是直接实现接口通常是有利的。除了为所有必需方法提供默认实现并存储 `pageContext` 变量外，`TagSupport` 还提供了几个便捷方法。`findAncestorWithClass()` 对于支持嵌套标签特别有用。例如，一个 *外部标签* 可以将一组对象作为实例变量进行管理，并提供公共访问器，使 *内部标签* 可以访问这些对象。本章后面的数据库标签示例说明了此技术。

**表 11-2. TagSupport 类中的附加方法**

| 方法 | 描述 |
| :--- | :--- |
| `public static Tag findAncestorWithTag(Tag thisTag, Class cls)` | 在运行时标签堆栈中查找所需的父标签处理程序。标签处理程序可以提供其作用域内的子标签可以调用的方法。 |
| `public void setId(String id)`<br>`public String getId()` | 存储或检索 `id` 属性中指定的名称。 |
| `public void setValue(String name, Object o)`<br>`public Object getValue(String name)` | 在本地哈希表中存储或检索给定名称下的值。 |
| `public void removeValue(String name)` | 从本地哈希表中移除指定名称的值。 |
| `public Enumeration getValues()` | 返回哈希表中键的 `java.util.Enumeration`。 |

## 标签处理程序生命周期

图 11-2 中的流程图描述了标签处理程序生命中的事件。流程图中显示的过程对应于当 JSP 页面被翻译成 servlet 时，JSP 容器为标签生成的 Java 代码。了解您的每个...



## 第11章：JSP标签扩展

203

![](img/7a2f73369bb140583c7288b73456addb_229_0.png)

图11-2. 标签处理器生命周期流程图

了解标签处理器方法将被何时调用，以及页面和容器的状态如何，非常重要。理解这一协议有助于你编写出符合预期的代码。同样重要的是要记住，标签本身在运行时并不存在于生成的Servlet中——它已被替换为设置属性和调用标签处理器中方法的等效代码。

让我们逐步分析流程图中的每个步骤。

## 流程图

首先，生成的Servlet需要创建标签处理器类的一个实例。它通常通过调用JSP容器的一部分——一个工厂类——的方法来完成。该工厂类可能维护一个标签处理器实例池，以便可以重用不再活跃的标签处理器。

接下来，标签处理器实例被初始化，并获知其所在Servlet的状态。Servlet通过在标签处理器中调用两个方法来实现这一点：

- `setPageContext(PageContext ctx)`
- `setParent(Tag parent)`

如果标签支持属性，这些属性的运行时值将通过setter方法传递给标签处理器，处理器必须提供这些方法。例如，本章开头的数据库连接标签

```xml
<db:connect url="mydatabase">
```

有一个名为`url`的属性。其标签处理器必须有一个方法签名为

```java
public void setUrl(String value)
```

的方法，该方法用于存储url属性的值，很可能存储在一个私有实例变量中。对于起始标签中编码的每个属性xxx，生成的Servlet将包含一个`setXxx(value)`方法调用。这些调用位于`setParent()`调用之后。

此时，标签处理器的`doStartTag()`方法被调用。页面上下文和父标签已经设置完毕，标签的所有属性也已设置。该方法可以读取这些变量，并执行实现标签功能所需的任何计算和操作。它可以通过调用`pageContext.getOut()`访问Servlet输出写入器。它可以通过在页面上下文中设置属性来更改JSP页面中脚本变量的值。这将在本章后面的“定义脚本变量”部分详细讨论。如果遇到任何致命错误，该方法应抛出`JspException`。

`doStartTag()`方法必须返回一个整数返回码，要么是`SKIP_BODY`，要么是`EVAL_BODY_INCLUDE`。如果`doStartTag()`的返回码是`EVAL_BODY_INCLUDE`，则标签体将按常规处理。如果返回码是`SKIP_BODY`，则原始JSP页面中直到此标签结束标签的所有内容都将被忽略。

> `SKIP_BODY`是`TagSupport`基类中`doStartTag()`的默认返回码，这是`TagSupport`无需子类化即可实际执行有用功能的罕见实例之一——你可以将其用作“注释掉”代码的自定义标签的处理器。如果你在TLD中进行以下条目

```xml
<tag>
    <name>skip</name>
    <tagclass>javax.servlet.jsp.tagext.TagSupport</tagclass>
    <bodycontent>JSP</bodycontent>
</tag>
```

那么你可以用

```jsp
<prefix.skip>
    ...
</prefix.skip>
```

包围JSP页面⁵的任何部分，它在运行时将不会被执行。

在标签体被评估或忽略之后，标签处理器的`doEndTag()`方法被调用。与`doStartTag()`一样，此方法必须返回一个整数返回码，指示如何继续。如果值是`EVAL_PAGE`，则页面的其余部分将被评估；如果值是`SKIP_PAGE`，则Servlet代码将从`_jspService()`立即返回。

⁵ 嗯，并非*任何*部分。如果脚本小程序、表达式、标准动作和HTML模板数据位于*skip*标签体内，它们将被抑制，但你不能在脚本小程序、表达式或声明*内部*使用标签。

## 生成代码示例

当我们看一个例子时，生成的Servlet与标签处理器之间的交互变得更加清晰。让我们开发本章前面`getWebServer`标签的增强版本，该版本允许我们指定任何头名称，而不是硬编码选择Server头。为此，该标签将接受一个名为`name`的*属性*。下一节将详细讨论标签属性，但为了本示例的目的，我们只需要知道该属性在TLD中描述，并使用其`setName()`方法传递给标签处理器。此标签将称为`getWebServerHeader`。TLD需要一个小的添加：

```xml
<tag>
    <name>getWebServerHeader</name>
    <tagclass>jspcr.taglib.diag.GetWebServerHeaderTag</tagclass>
    <bodycontent>empty</bodycontent>
    <attribute>
        <name>name</name>
        <required>true</required>
        <rtexprvalue>true</rtexprvalue>
    </attribute>
</tag>
```

`name`属性被定义为必填字段，其值可以通过请求时表达式提供（如果需要），而不是编码为字面量。
毫不奇怪，标签处理器与`getWebServer`的处理器几乎相同。以下是`getWebServerHeader`标签处理器的源代码：

```java
package jspcr.taglib.diag;

import javax.servlet.http.*;
import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.*;
import java.net.*;

/**
 * "getWebServerHeader"标签的处理器
 */
public class GetWebServerHeaderTag extends TagSupport
{
    private String name;

    /**
     * 设置name属性。当在JSP页面中使用带有name属性的标签时，
     * JSP容器会自动生成对此方法的调用。
     */
    public void setName(String name)
    {
        this.name = name;
    }

    public int doStartTag() throws JspException
    {
        try {
            // 从页面上下文获取请求对象
            HttpServletRequest request =
                (HttpServletRequest) pageContext.getRequest();

            // 从Web服务器请求信息
            URL url = new URL("http",
                    request.getServerName(),
                    request.getServerPort(),
                    "/");
            URLConnection con = url.openConnection();
            ((HttpURLConnection) con).setRequestMethod("OPTIONS");

            // 提取请求的头
            String header = con.getHeaderField(name);

            // 写入输出流
            JspWriter out = pageContext.getOut();
            out.print(header);
        }
        catch (IOException e) {
            throw new JspException(e.getMessage());
        }
        return SKIP_BODY;
    }
}
```

主要区别是添加了name属性。这需要创建一个name变量和一个setName()方法。然后，不是

```java
String webserver = con.getHeaderField("server");
```

而是

```java
String header = con.getHeaderField(name);
```

其中name是在JSP标签中编码的值。
在JSP页面中，我们将使用旧标签获取Web服务器产品名称，使用新标签获取Allow头。由于标签处理器使用OPTIONS方法发出HTTP请求，服务器应返回一个Allow头，列出它将接受的请求方法。以下是更新后的页面，名为ShowServerHeader.jsp：

```jsp
<%@ taglib prefix="diag" uri="/WEB-INF/tlds/diagnostics.tld" %>

<HTML>

<HEAD>
<TITLE>带属性的自定义标签</TITLE>
</HEAD>

<BODY>
<H3>带属性的自定义标签</H3>

此<diag:getWebServer/>实例支持的请求方法
是
<H4><diag:getWebServerHeader name="allow"/></H4>
</BODY>

</HTML>
```

当ShowServerHeader.jsp运行时，它会产生如图11-3所示的输出。
让我们检查一下JSP容器（在此示例中是JRun 3.0）为ShowServerHeader.jsp生成的Servlet的`_jspService()`方法的一部分。源代码

![](img/7a2f73369bb140583c7288b73456addb_235_0.png)

已经过重新格式化和轻微修改以使其更清晰。请注意，你不需要编写这个；它是JSP容器根据你的JSP页面和TLD定义生成的。

```java
PageContext pageContext = __jspFactory.getPageContext
    (this, request, response, null, true, 8192, true);
JspWriter out = pageContext.getOut();

try {
    out.print("\r\n\r\n"
        + "<HTML>\r\n\r\n"
        + "<HEAD>\r\n"
        + "<TITLE>带属性的自定义标签</TITLE>\r\n"
        + "</HEAD>\r\n\r\n"
        + "<BODY>\r\n"
        + "<H3>带属性的自定义标签</H3>\r\n\r\n"
        + "此实例支持的请求方法为"
        + "\r\n");
```



GetWebServerTag tag1 = (GetWebServerTag)
    JRunJSPStaticHelpers.createTagHandler
        (pageContext, "GetWebServerTag");

tag1.setPageContext(pageContext);
tag1.setParent(null);
tag1.doStartTag();

if (tag1.doEndTag() == Tag.SKIP_PAGE) {
    return;
}

out.print("\r\n"
    + "are\r\n"
    + "<H4>");

GetWebServerHeaderTag tag2 = (GetWebServerHeaderTag)
    JRunJSPStaticHelpers.createTagHandler
        (pageContext, "GetWebServerHeaderTag");

tag2.setPageContext(pageContext);
tag2.setParent(null);
tag2.setName("allow");
tag2.doStartTag();

if (tag2.doEndTag() == Tag.SKIP_PAGE) {
    return;
}

out.print("</H4>\r\n\r\n</BODY>\r\n\r\n</HTML>\r\n");
}

在_jspService()方法的开头附近，servlet会创建并初始化其页面上下文：

```
PageContext pageContext = __jspFactory.getPageContext
    (this, request, response, null, false, 8192, true);
```

JspFactory有一个getPageContext()方法，它接收当前servlet的引用、请求和响应对象、错误页面的URL（如果有）、一个标志以指示页面是否需要HTTP会话、输出缓冲区大小，以及一个标志以指示缓冲区是否应该自动刷新。该方法返回一个初始化的页面上下文，它封装了所有这些对象。

```
JspWriter out = pageContext.getOut();
```

初始化页面上下文对象后，servlet使用它来获取响应输出写入器的引用。标签处理器可以使用相同的调用方法来向页面进行自己的输出，如果需要的话。对于与主体内容交互的标签处理器，这个问题会变得稍微复杂一些，我们将在下一节中看到。

```
GetWebServerTag tag1 = (GetWebServerTag)
    JRunJSPStaticHelpers.createTagHandler
    (pageContext, "GetWebServerTag");
```

打印页面标题后，servlet使用辅助类中的静态方法创建标签处理器的一个实例。这个辅助类可能使用标签处理器实例池或执行其他优化——JSP规范没有规定应该如何做。这为servlet引擎供应商提供了区分其产品性能和功能的机会。

```
tag1.setPageContext(pageContext);
tag1.setParent(null);
```

如图11-2的流程图所示，生成的servlet然后调用标签处理器的setPageContext()和setParent()方法。这种情况下没有父标签，所以参数值是null。

```
tag1.doStartTag();
```

在页面环境被充分描述给标签处理器后，其doStartTag()方法被调用。注意，没有捕获返回码，即使doStartTag()返回一个。这样做的原因是TLD（标签库描述符）表明getWebServer标签没有主体（<bodycontent>empty</bodycontent>），因此不会生成处理它的条件代码。JSP容器能够优化代码，而不是检查一个无意义的返回值。

```
if (tag1.doEndTag() == Tag.SKIP_PAGE) {
    return;
}
```

doEndTag()方法可以返回EVAL_PAGE或SKIP_PAGE。当我们看到SKIP_PAGE只是导致从_jspService()方法返回时，每个返回值的效果就变得清晰了。

在打印了中间的HTML之后，servlet开始处理第二个标签：

```
GetWebServerHeaderTag tag2 = (GetWebServerHeaderTag)
    JRunJSPStaticHelpers.createTagHandler
        (pageContext, "GetWebServerHeaderTag");

tag2.setPageContext(pageContext);
tag2.setParent(null);
tag2.setName("allow");
tag2.doStartTag();
```

处理这个标签与处理前一个标签之间的唯一区别是getWebServerHeader标签有一个name属性。这被转换为对标签处理器setName()方法的调用，就在doStartTag()被调用之前。结束标签的处理方式相同，其返回码决定是从_jspService()方法退出还是继续。

## 定义标签属性

自定义标签可以有任意数量的*属性*，这些是当它在JSP页面中使用时编码在开始标签中的名称/值对。例如，下面显示的标签

```
<opera:role name="Papageno" range="baritone"
            description="a bird-catcher"/>
```

有三个属性：*name*、*range*和*description*。属性可以是必需的或可选的，并且它们的值可以编码为字符串字面量，也可以在请求时使用JSP表达式提供（如果标签允许这样做）。

对于标签支持的每个属性，其标签处理器必须提供两样东西：

- 一个存储属性的实例变量
- 一个或多个setAttrname()方法，其中*Attrname*是属性名称，首字母大写。

对于前面的示例标签，标签处理器可能如下所示：

```
/**
* RoleTag
*/
public class RoleTag extends TagSupport
{
    // 三个属性：

    private String name;
    private String range;
    private String description;

    // ... 及其setter方法：

    public void setName(String nameFromJSPTag)
    {
        name = nameFromJSPTag;
    }

    public void setRange(String rangeFromJSPTag)
    {
        range = rangeFromJSPTag;
    }

    public void setDescription(String descriptionFromJSPTag)
    {
        description = descriptionFromJSPTag;
    }

    public int doStartTag() throws JspException
    {
        try {
            JspWriter out = pageContext.getOut();
            out.println("<TR>");
            out.println("<TD>" + name + "</TD>");
            out.println("<TD>" + range + "</TD>");
            out.println("<TD>" + description + "</TD>");
            out.println("</TR>");
        }
        catch (IOException e) {
            throw new JspException(e.getMessage());
        }
        return SKIP_BODY;
    }
}
```

JSP容器在JSP servlet中生成代码，以获取编码在自定义标签中的属性值并将其发送到标签处理器。它通过对每个属性调用`setAttrname()`方法来实现这一点。这发生在页面上下文和父标签已被设置之后，但在`doStartTag()`被调用之前。例如，如果一个JSP页面使用`<opera:role>`标签如下

```
<%@ page session="false" %>
<%@ taglib prefix="opera" uri="/WEB-INF/tlds/opera.tld" %>

<HTML>
<HEAD><TITLE>The Magic Flute</TITLE></HEAD>

<BODY>
<H2>The Magic Flute</H2>
<H3>Dramatis Personae</H3>
<TABLE BORDER="1" CELLPADDING="3" CELLSPACING="0">
<TR><TH>Role</TH><TH>Range</TH><TH>Description</TH>

<opera:role name="Tamino" range="Tenor"
            description="an Egyptian prince"/>

<opera:role name="Pamina" range="Soprano"
            description="daughter of the Queen of the Night"/>

<opera:role name="Papageno" range="Baritone"
            description="a bird-catcher"/>

<opera:role name="Queen of the Night" range="Soprano"
            description="die Sternflammende Königin"/>

<opera:role name="Sarastro" range="Bass"
            description="High Priest of Isis and Osiris"/>

</TABLE>
</BODY>
</HTML>
```

那么生成的servlet（同样使用JRun作为容器）将使用类似于以下的代码处理每个`<opera:role>`标签：

```
RoleTag roleTag = (RoleTag)
    JRunJSPStaticHelpers.createTagHandler
    (pageContext, "RoleTag");

roleTag.setPageContext(pageContext);
roleTag.setParent(null);

roleTag.setRange("Baritone");
roleTag.setName("Papageno");
roleTag.setDescription("a bird-catcher");

roleTag.doStartTag();
```

属性的setter方法是标签支持属性所需要的全部，但可以在TLD中指定更多信息。在`<tag>`元素中，可以有任意数量的`<attribute>`元素，形式如下：

```
<attribute>
    <name>attributeName</name>
    <required>true|false</required>
    <rtexprvalue>true|false</rtexprvalue>
</attribute>
```

只有属性名称是必需的；其他两个元素是可选的，默认值为false。

如果指定了`<required>true</required>`，那么该属性必须在标签使用的每个地方都编码，否则会发生致命的翻译错误。否则，该属性是可选的。标签处理器应该注意处理未指定属性的情况，此时实例变量将为null。

如果指定了`<rtexprvalue>true</rtexprvalue>`，那么属性值可以用请求时表达式指定。以此方式编码的属性具有以下形式

```
attribute="<%= scriptlet_expression %>"
```

其中引号只能包含JSP表达式。除了可以在运行时为属性提供值之外，这还会导致表达式的类型被保留。换句话说，

```
date="<%= new java.util.Date() %>"
```

将导致生成的servlet代码

```
tag.setDate(new java.util.Date());
```



这将导致标签处理器的 `public void setDate(Date date)` 方法被调用，而不是 `public void setDate(String date)` 方法。
下面是一个包含两个可选属性的自定义标签示例，每个属性都可以使用请求时表达式指定。

```
<x:formattedDate date="date" format="format"/>
```

`date` 属性应在请求时表达式中指定为一个 `java.util.Date` 对象，而 `format` 属性可以是 `java.text.SimpleDateFormat` 对象，也可以是 `SimpleDateFormat` 使用的格式字符串。TLD 文件应如下所示：

```xml
<?xml version="1.0" ?>
<taglib>

    <tlibversion>1.0</tlibversion>
    <jspversion>1.1</jspversion>
    <shortname>util</shortname>

    <tag>
        <name>formattedDate</name>
        <tagclass>jsPCR.taglib.util.FormattedDateTag</tagclass>
        <bodycontent>empty</bodycontent>
        <info>
            使用指定格式返回格式化后的日期。
            如果未指定日期，则使用当前日期。
            默认日期格式为 MM/dd/yyyy
        </info>

        <attribute>
            <name>date</name>
            <required>false</required>
            <rtexprvalue>true</rtexprvalue>
        </attribute>

        <attribute>
            <name>format</name>
            <required>false</required>
            <rtexprvalue>true</rtexprvalue>
        </attribute>
    </tag>

</taglib>
```

以下是标签处理器：

```java
package jspcr.taglib.util;

import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.*;
import java.text.*;
import java.util.*;

/**
 * 格式化日期标签
 */
public class FormattedDateTag extends TagSupport
{
    // date 属性

    private Date date;
    public void setDate(Date date)
    {
        this.date = date;
    }

    // format 属性

    private SimpleDateFormat format;
    public void setFormat(String fmtstr)
    {
        format = new SimpleDateFormat(fmtstr);
    }
    public void setFormat(SimpleDateFormat fmt)
    {
        format = fmt;
    }

    /**
     * 遇到开始标签时打印日期
     */
    public int doStartTag() throws JspException
    {
        // 获取 date 属性，默认为当前日期
        Date date = this.date;
        if (date == null)
            date = new Date();

        // 获取日期格式属性，默认为月/日/年格式

        SimpleDateFormat format = this.format;
        if (format == null)
            format = new SimpleDateFormat("MM/dd/yyyy");

        // 格式化并打印

        try {
            pageContext.getOut().print(format.format(date));
        }
        catch (IOException e) {
            throw new JspException(e.getMessage());
        }

        return SKIP_BODY;
    }
}
```

注意这里存在两个 `setFormat()` 方法：一个接受 `java.text.SimpleDateFormat` 对象；另一个接受字符串并从中创建一个 `SimpleDateFormat` 对象。JSP 容器为哪个方法生成 servlet 代码，取决于标签是使用请求时表达式编码还是其他方式。以下是该标签使用方式的一个示例：

```jsp
<%@ page session="false" %>
<%@ page import="java.util.*,java.text.*" %>
<%@ taglib prefix="x" uri="/WEB-INF/tlds/util.tld" %>

<%
    Calendar gc = new GregorianCalendar(1931, 6, 25);
    Date then = gc.getTime();
    SimpleDateFormat fmt =
        new SimpleDateFormat("MMMMM d, yyyy");
%>
```

日期是

`<x:formattedDate date="<%= then %>" format="<%= fmt %>" />.`

在上述 JSP 页面中使用时，该标签的输出是：

> 日期是 1931 年 7 月 25 日。

## Body 标签处理器 API

简单标签是有用的组件，它们的功能完全在其开始标签内实现。然而，自定义标签的真正威力源于它们与其标签体交互的能力。这使得自定义标签可以：

*   后处理其标签体文本，例如排序、将其转换为 HTML 表格，或者过滤掉像 `<` 和 `>` 这样的字符，并用它们在 HTML 中安全的等价字符 `&lt;` 和 `&gt;` 替换。
*   定义新的隐式对象并为其创建脚本变量。
*   与嵌套标签协作执行复杂操作。

处理其标签体的标签是本章目前讨论的标签的扩展。它们实现了 `javax.servlet.jsp.tagext.Tag` 的一个子接口，称为 `javax.servlet.jsp.tagext.BodyTag`。与 `TagSupport` 类的情况类似，`BodyTag` 也存在一个基类实现，名为 `BodyTagSupport`。

## BodyContent

当 JSP 容器为具有标签体的标签生成代码时，它会保存并恢复表示当前 servlet 输出写入器的对象。在处理标签的标签体之前，会创建一个新的输出写入器——这次是一个 `BodyContent` 类的实例。在评估标签体期间，`out` 脚本变量以及 `pageContext.getOut()` 返回的值都指向这个新的写入器对象。如果存在多级嵌套，写入器会被保存在栈上，因此每一级都有自己的写入器。

`BodyContent` 是 `javax.servlet.jsp.JspWriter` 的子类，但与其父类不同，其内容不会自动写入 servlet 输出流。相反，它们会累积在一个相当于字符串缓冲区的地方。在标签体完成后，原始的 `JspWriter` 会被恢复，但 `BodyContent` 对象在 `doEndTag()` 方法中的 `bodyContent` 变量中仍然可用。可以通过其 `getString()` 或 `getReader()` 方法检索其内容，根据需要进行修改，然后写入已恢复的 `JspWriter` 输出流以与页面输出合并。表 11-3 列出了 `BodyContent` 提供的附加方法。

| 方法 | 描述 |
|---|---|
| `public void flush() throws IOException` | 重写 `JspWriter.flush()` 方法，使其总是抛出异常。刷新 `BodyContent` 写入器是无效的，因为它没有连接到可以写入的实际输出流。 |
| `public void clearBody()` | 将 `BodyContent` 缓冲区重置为空。如果在 `doAfterBody()` 中将标签体写入外层写入器，这会很有用。 |
| `public Reader getReader()` | 在标签体内容被评估后返回一个用于读取它的 `Reader`。此 `Reader` 可以传递给其他能够处理 `java.io.Reader` 的类，例如 `StreamTokenizer`、`FilterReader` 或 XML 解析器。 |
| `public String getString()` | 返回一个包含评估后标签体内容的字符串。 |
| `public void writeOut(Writer w)` | 将标签体内容写入指定的输出写入器。 |
| `public JspWriter getEnclosingWriter()` | 返回栈中上一层的写入器对象（可能是另一个 `BodyContent`）。 |

表 11-3. BodyContent 类中的附加方法

为什么 JSP 容器为自定义标签输出创建这样复杂的结构？我们已经知道 JSP 容器允许输出被后处理和过滤，但这也是因为并非所有的标签体内容都旨在产生输出。例如，在前面的数据库查询示例中：

```jsp
<db:runQuery>
    SELECT  *
    FROM    FD_GROUP
    WHERE   FdGp_Desc LIKE '%F%'
    ORDER BY FdGp_Cd
</db:runQuery>
```

标签体根本不是 HTML，而是代表 SQL 语句的字符串。大概会使用 `BodyContent.getString()` 方法读取它，并将其传递给一个 JDBC 语句对象，然后该对象的输出会被写入 Web 页面。这之所以自动成为可能，是因为 `BodyContent` 对象将其输出存储在缓冲区中，而不是直接写入。

## BodyTag 接口

与其标签体内容交互的标签具有稍微更复杂的生命周期，因此它们的标签处理器需要更多的方法。为此，存在一个名为 `BodyTag` 的 `Tag` 接口扩展，它继承了 `Tag` 要求的所有方法，但增加了三个与标签体处理相关的新方法。表 11-4 描述了该接口。

除了三个新方法外，`BodyTag` 接口还定义了一个新的整型常量：

*   `EVAL_BODY_TAG` - 当被 `doStartTag()` 返回时，会导致创建一个新的 `BodyContent` 对象并与该标签处理器关联。当被 `doAfterBody()` 返回时，会导致 JSP servlet 在更新此标签控制的任何脚本变量后再次评估标签体。这使得标签处理器可以循环遍历元素列表，为每个元素评估标签体。

| 方法 | 描述 |
|---|---|
| `public void setBodyContent(BodyContent out)` | 在当前 `JspWriter` 被压栈且创建了新的 `BodyContent` 写入器后，由 JSP servlet 调用。这发生在 `doStartTag()` 之后。 |
| `public void doInitBody() throws JspException` | 在 `setBodyContent()` 之后但在标签体被评估之前调用的生命周期方法。如果标签体被多次评估，此方法只被调用一次。 |
| `public int doAfterBody() throws JspException` | 在标签体已被评估之后，但 `BodyContent` 写入器仍然活动时调用的生命周期方法。此方法必须返回 `EVAL_BODY_TAG` 或 `SKIP_BODY`。如果返回码是 `EVAL_BODY_TAG`，则标签体将被再次评估，并且 `doAfterBody()` 也会被再次调用。 |

表 11-4. BodyTag 接口中的方法



> **注意** 除了 `SKIP_BODY`，`doStartTag()` 还可以返回 `EVAL_BODY_INCLUDE` 或 `EVAL_BODY_TAG`，两者都表示应处理标签体。但是，实现了 `BodyTag` 接口的标签处理器不能返回 `EVAL_BODY_INCLUDE`，而未实现 `BodyTag` 的标签处理器则不能返回 `EVAL_BODY_TAG`。这两种操作都会导致运行时异常。

## BodyTagSupport 类

与 Tag 接口的情况类似，BodyTag 也有一个默认的实现类，名为 `javax.servlet.jsp.tagext.BodyTagSupport`。这个类扩展了 TagSupport，但进行了一些微妙的改动。表 11-5 描述了 BodyTagSupport 实现的公共方法。

Body 标签处理器可以直接实现 BodyTag 接口，但 BodyTagSupport 通常是一个更方便的基类。

表 11-5. BodyTagSupport 中的方法
| 方法 | 描述 |
|---|---|
| `public int doStartTag()`<br>`throws JspException` | 重写 TagSupport 中的 `doStartTag()`，默认返回 `EVAL_BODY_TAG` 而不是 `SKIP_BODY`。 |
| `public int doEndTag()`<br>`throws JspException` | 调用 TagSupport 中的 `doEndTag()`，并返回其结果。 |
| `public void setBodyContent`<br>`(BodyContent out)` | 将新的 body 内容对象存储在名为 `bodyContent` 的 protected 变量中。子类可以直接访问此变量。 |
| `public void doInitBody()`<br>`throws JspException` | 默认情况下不做任何事情。旨在被需要在评估 body 之前执行初始化的子类重写。 |
| `public int doAfterBody()`<br>`throws JspException` | 在每次评估完 body 后由 JSP servlet 调用。此时 body 内容对象仍然有效。此方法必须返回 `SKIP_BODY` 或 `EVAL_BODY_TAG`，后者将导致 body 再次被评估并再次调用 `doAfterBody()`。 |
| `public void release()` | 将 `bodyContent` 变量设置为 `null`，然后调用 `super.release()`。重写的方法也必须调用 `super.release()`，否则 `bodyContent` 可能无法被垃圾回收。 |
| `public BodyContent getBodyContent()` | 返回 `bodyContent` 变量。子类已经可以访问这个 protected 变量，但此方法允许不相关的标签处理器类向此 body 内容发送输出。 |
| `public JspWriter getPreviousOut()` | 一个便捷方法，调用 `bodyContent` 变量上的 `getEnclosingWriter()` 并返回结果。 |

## Body 标签处理器生命周期

图 11-4 描述了与其 body 交互的标签处理器的稍微复杂一些的生命周期。
以下部分描述了生命周期流程图中的每个事件。

## 流程图

前几个步骤直到 `doStartTag()` 与图 11-2 中没有不同。第一个不同之处在于对此方法返回代码的处理。Body 标签处理器中的 `doStartTag()` 可以返回 `SKIP_BODY`（导致立即分支到 `doEndTag()`）或 `EVAL_BODY_TAG`（启动处理标签体的事件链）。

当从 `doStartTag()` 返回 `EVAL_BODY_TAG` 时，JSP servlet⁶ 会调用页面上下文的 `pushBody()` 方法，该方法执行三件事：

1. 将当前的 `JspWriter` 保存到堆栈上。

6 本节中的术语 *JSP servlet* 指的是 JSP 容器根据 JSP 页面源代码生成的 servlet。

**图 11-4.** *Body 标签处理器生命周期流程图*

# 第 11 章：JSP 标签扩展

2. 创建一个新的 BodyContent 对象，并将其存储在页面上下文的页面范围属性中，名为 out。
3. 将新的 BodyContent 对象分配给 JSP 页面的隐式变量 out。

之后，JSP servlet 使用新的 writer 调用标签处理器的 setBodyContent() 方法。

接下来，调用标签处理器的 doInitBody() 方法，以在评估 body 之前处理任何必要的初始化。此初始化也可以在 doStartTag() 中完成，但此时新的 BodyContent 对象还不可用。如果标签中没有 body，则不会调用 doInitBody()，并且如果它检测到任何致命错误，可以抛出 JspException。

此时，servlet 像通常一样处理标签的 body，将其输出写入 BodyContent 对象。处理取决于 TLD 中标签的 <bodycontent> 元素的值。此元素有三种可能的值：

- **empty** 标签体必须为空。
- **JSP** 脚本小程序、表达式和模板 HTML 按常规进行评估。如果 body 作用域内有任何其他自定义标签，它们也会被评估，与在页面其他地方使用时相同。如果其中任何一个具有实现 BodyTag 的标签处理器，则该过程会递归执行——当前的 BodyContent 被推入堆栈，新的 BodyContent 被分配给内部标签，依此类推。
- **tagdependent** body 的内容被逐字写入 BodyContent。脚本小程序和表达式以其原始的 JSP 源代码形式出现，而不是由 JSP 容器解释。

处理完 body 后，servlet 调用标签处理器的 doAfterBody() 方法。如果标签处理器此时想将其 body 内容写入外层的 JspWriter，它可以这样做，如下所示

```
JspWriter out = bodyContent.getEnclosingWriter();
out.println(bodyContent.getString());
bodyContent.clear();
```

或者，如下

```
JspWriter out = bodyContent.getEnclosingWriter();
bodyContent.writeOut(out);
bodyContent.clear();
```

如果 body 内容不是太大，等到 `doEndTag()` 再一次性写入 body 内容可能更容易。

`doAfterBody()` 方法可以返回两种可能的返回代码之一：

- `SKIP_BODY` 继续处理页面的其余部分。
- `EVAL_BODY_TAG` 导致 body 被再次评估，然后再次调用 `doAfterBody()` 方法。这通常在处理数组或枚举时完成，在每次迭代中将数组或枚举中的下一个元素分配给一个脚本变量。

当 `doAfterBody()` 最终返回 `SKIP_BODY` 时，循环（如果有）退出。此时 body 内容已完成，因此创建它的过程被反转：

1. 调用 `pageContext.popBody()` 检索紧邻的上一个 JspWriter。
2. 将该 writer 重新分配回 `out` 脚本变量。

最后，调用 `doEndTag()` 方法，允许标签处理器将其内容发送回输出流。此时，`pageContext.getOut()` 指向原始的 writer，即在处理标签之前存在的那个 writer。但是，body 内容在 protected `bodyContent` 变量中仍然可用。可以如下将其写入 servlet 输出流

```
JspWriter out = pageContext.getOut();
out.println(bodyContent.getString());
```

或者简单地

```
bodyContent.writeOut(pageContext.getOut());
```

`doEndTag()` 应返回 `SKIP_PAGE`（导致 JSP 页面的其余部分被忽略）或 `EVAL_PAGE`（导致页面按常规进行评估）。

在我们可以给出一个 body 标签的生成代码详细示例之前，我们首先需要了解标签处理器如何与脚本变量交互。

## 定义脚本变量

JSP 页面作者熟悉脚本变量——这些通常是在脚本小程序或 `<jsp:useBean>` 操作中定义的 Java 变量。例如，在以下代码开头的脚本小程序中，

```
<%
    String[] flavors = {"Chocolate", "Strawberry", "Vanilla"};
    for (int i = 0; i < flavors.length; i++) {
%>
<LI>Flavor <%= i %> is <%= flavors[i] %>
<%
    }
%>
```

定义了整数变量 i 和字符串数组变量 flavors，它们随后可供页面上的其他脚本小程序和表达式使用。同样，在这个 JSP 页面中，

```
<jsp:useBean id="m1" class="Meteor"/>
<jsp:setProperty name="m1"
                 property="bane"
                 value="The atmosphere"/>
Ahhhh! <%= m1.getBane() %>! Ahhhh!
```

`<jsp:useBean>` 操作导致定义一个名为 m1 的 Meteor 类变量。这被后续的 `<jsp:setProperty>` 操作使用，并可供最后一行的表达式使用。
自定义标签也可以在其标签处理器中定义脚本变量，并且与前面的示例类似，这些变量随后可供同一页面上的脚本小程序、表达式和其他标签使用。定义此类变量的机制是 TagExtraInfo 类。

## TagExtraInfo 类

需要定义变量或对其属性执行验证的标签需要定义一个扩展 TagExtraInfo 类的类。此子类在 TLD 中与自定义标签关联：

```
<tag>
    <name>mytag</name>
    <tagclass>mypackage.MyTagHandler</tagclass>
    <teiclass>mypackage.MyTagTEI</teiclass>
    ...
</tag>
```

TEI 在 JSP 翻译阶段发挥作用。当 JSP 解析器读取 taglib 指令时，它会从 TLD 加载每个标签的关联标签和 TEI 类名。然后，在解析标签时，会调用其 TEI 中的方法来获取信息。



## 表11-6. TagExtraInfo 类

关于脚本变量和验证。通过在TEI子类中重写这些方法，标签作者可以创建变量并验证标签属性是否有效。表11-6列出了 `TagExtraInfo` 类中可用的方法。

主要关注的方法是 `getVariableInfo()`。此方法在页面翻译时由JSP解析器调用，预期返回一个 `VariableInfo` 对象数组。`VariableInfo` 本质上是一个只有四个字段的数据结构：

- **varName**：要创建的变量的名称。
- **className**：变量类的完全限定名。
- **declare**：一个布尔变量，如果JSP解析器应该为该变量创建实际定义（而不是假设该类的变量已在servlet中预先定义），则为true。
- **scope**：一个整数，指示变量应被定义（或视为活动）的时机点。

| 方法 | 描述 |
|---|---|
| `public VariableInfo[] getVariableInfo(TagData data)` | 基于 `data` 参数中的属性名和值列表，构建一个 `VariableInfo` 对象数组，该数组描述了要创建的每个脚本变量的名称、类型、存在性和作用域。 |
| `public boolean isValid(TagData data)` | 在页面翻译时由JSP解析器调用。给定属性名和值列表，该方法可以单独验证它们以及相互组合验证。如果属性有效则返回 `true`，否则返回 `false`。默认实现简单返回 `true`。 |
| `public void setTagInfo(TagInfo info)` | 设置此类使用的 `TagInfo` 对象。 |
| `public TagInfo getTagInfo()` | 返回此类使用的 `TagInfo` 对象。 |

作用域有三个可能的值，每个值由 `VariableInfo` 中定义的一个常量表示：

- **AT_BEGIN** 变量在遇到开始标签时定义，并在页面剩余部分保持可见。例如，这是 `<jsp:useBean>` 定义的 `id` 变量的可见性。
- **AT_END** 变量在结束标签之后定义，并在页面剩余部分保持可见。
- **NESTED** 变量仅在标签主体的作用域内定义。

## 示例：enumerate 标签

为了说明TEI类的用法，我们开发一个名为 `enumerate` 的标签，它遍历一个 `java.util.Enumeration`，使其中的每个元素依次在标签主体中作为脚本变量可用。以下是该标签的TLD定义：

```
<tag>
    <name>enumerate</name>
    <tagclass>jspcr.taglib.util.EnumerateTag</tagclass>
    <teiclass>jspcr.taglib.util.EnumerateTEI</teiclass>
    <bodycontent>JSP</bodycontent>
    <info>
        Iterates tag body through an enumeration
    </info>
    <attribute>
        <name>enumeration</name>
        <required>true</required>
        <rtexprvalue>true</rtexprvalue>
    </attribute>
</tag>
```

该标签接受一个名为 `enumeration` 的必需属性。此属性的类型是 `java.util.Enumeration`，因此其值必须通过请求时表达式提供。标签处理器使用 `Enumeration.hasMoreElements()` 和 `nextElement()` 方法处理实际的迭代：

```
package jspcr.taglib.util;

import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.*;
import java.util.*;

/**
 * EnumerateTag
 */
public class EnumerateTag extends BodyTagSupport
{
    // Enumeration attribute

    private Enumeration list;
    public void setEnumeration(Enumeration list)
    {
        this.list = list;
    }

    public int doStartTag() throws JspException
    {
        // Do not evaluate the body if the list is empty

        if (list.hasMoreElements()) {

            // Create a scripting variable named "element"
            // that contains the value of the current
            // element of the enumeration

            pageContext.setAttribute
                ("element", list.nextElement());

            return EVAL_BODY_TAG;
        }
        return SKIP_BODY;
    }

    public int doAfterBody() throws JspException
    {
        // Get next element.  This will be assigned
        // to the scripting variable named "element"

        if (list.hasMoreElements()) {

            pageContext.setAttribute
                ("element", list.nextElement());

            return EVAL_BODY_TAG;
        }

        // If no more elements, exit from the loop

        return SKIP_BODY;
    }

    public int doEndTag() throws JspException
    {
        // getOut() now refers to the original JspWriter

        try {
            bodyContent.writeOut(pageContext.getOut());
        }
        catch (IOException e) {
            throw new JspException(e.getMessage());
        }

        return EVAL_PAGE;
    }
}
```

请注意，当枚举的每个元素被处理时，它以 `element` 作为名称存储在页面上下文中。

为了使当前元素作为脚本变量可用，我们使用一个TEI类：

```
package jspcr.taglib.util;

import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;

/**
 * EnumerateTEI
 */
public class EnumerateTEI extends TagExtraInfo
{
    public VariableInfo[] getVariableInfo(TagData tagData)
    {
        return new VariableInfo[] {
            new VariableInfo(
                "element",           // Variable name
                "java.lang.Object",  // Class
                true,                // Create a declaration?
                VariableInfo.NESTED  // Scope
            )
        };
    }
}
```

这种情况下，`getVariableInfo()` 方法返回一个长度为1的数组，其中包含一个用于所需脚本变量的 `VariableInfo` 对象。构造函数声明：

- 变量名应为 `element`。
- 它的类应为 `java.lang.Object`。
- JSP解析器应该为该变量生成一个声明。
- 变量应在主体评估期间对JSP页面可见，但之后不可见。

以下 `EnumTest.jsp` 页面展示了该标签的实际使用：

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ taglib prefix="util" uri="/WEB-INF/tlds/util.tld" %>

<%--
    The scriptlet below loads the properties object.
    It could just as easily be loaded from a file.
--%>
<%
    Properties flavors = new Properties();
    flavors.setProperty("Vanilla", "The perennial favorite");
    flavors.setProperty("Chocolate", "Rich and smooth");
    flavors.setProperty("Strawberry", "Dazzling and fruity");
%>

<TABLE BORDER="1" CELLPADDING="3" CELLSPACING="0">
<TR><TH>Flavor</TH><TH>Description</TH></TR>

<%--
    The enumerate tag will evaluate its body
    for each item in the properties object.
--%>

<util:enumerate enumeration="<%= flavors.propertyNames() %>">
<%
    String description = flavors.getProperty((String) element);
%>
<TR>
    <TD><%= element %></TD>
    <TD><%= description %></TD>
</TR>
</util:enumerate>

</TABLE>
```

`enumerate` 标签出现在文件末尾附近。其值从 `flavors.propertyNames()` 返回的 `java.util.Enumeration` 中赋值。请注意，`element` 变量没有可见的声明——它是一个具有固定名称的隐式变量，类似于JSP环境中随处定义的 `request`、`response`、`session` 等隐式变量。该页面使用了 `element` 两次：一次在脚本段中，用于获取属性值；一次在JSP表达式中，其字符串值在HTML表格中打印。

让我们检查一下JRun为 `enumerate` 标签生成的servlet代码。将其与图11-4中所示的流程图进行比较会很有帮助。

```
EnumerateTag enumTag = (EnumerateTag)
    JRunJSPStaticHelpers.createTagHandler
    (pageContext, "EnumerateTag");

enumTag.setPageContext(pageContext);
enumTag.setParent(null);
enumTag.setEnumeration( flavors.propertyNames() );
```

JSP页面通过以下方式指定了 `enumeration` 属性的值：

```
enumeration="<%= flavors.propertyNames() %>"
```

这通过调用其 `setEnumeration()` 方法传递给标签处理器。接下来，生成的servlet调用 `doStartTag()` 并检查其返回码。回想一下，`doStartTag()` 读取枚举的第一个元素，并通过 `setAttribute("element", list.nextElement())` 将其存储在页面上下文中。



```
int rc = enumTag.doStartTag();
JRunJSPStaticHelpers.checkStartVal
    ("EnumerateTag", rc, BodyTag.EVAL_BODY_TAG, 24);
```

如果枚举不为空，`doStartTag()`方法将返回`EVAL_BODY_TAG`，这会触发对正文内容的第一次求值：

```
if (rc == BodyTag.EVAL_BODY_TAG) {

    out = pageContext.pushBody();

    enumTag.setBodyContent((BodyContent)out);
    enumTag.doInitBody();

    do {
        java.lang.Object element =
            (java.lang.Object)
                pageContext.getAttribute("element");
```

在设置嵌套正文内容并调用`doInitBody()`之后，servlet进入一个`do` `while`循环。循环的第一条语句是对`element`变量的`getAttribute()`调用，该变量刚刚在`doStartTag()`中设置。

```
        out.print("\r\n");

        String description =
            flavors.getProperty((String) element);

        out.print("\r\n<TR>\r\n    <TD>");

        out.print(element);
        out.print("</TD>\r\n    <TD>");

        out.print(description);
        out.print("</TD>\r\n</TR>\r\n");

    }
    while (enumTag.doAfterBody() == BodyTag.EVAL_BODY_TAG);
```

然后使用`element`变量打印表格条目，接着调用`doAfterBody()`。`doAfterBody()`重复执行逻辑，获取下一个元素，并将其作为`pageContext`中的`element`属性设置。只要有可用元素，`doAfterBody()`就返回`EVAL_BODY_TAG`，这会导致下一次循环迭代，在运行时为`element`赋一个新值。

```
out = pageContext.popBody();
}

if (enumTag.doEndTag() == Tag.SKIP_PAGE) {
    if (true)
        return;
}
```

最后，在枚举耗尽后，`doAfterBody()`返回`SKIP_BODY`，循环终止。先前的`JspWriter`从堆栈中弹出，`doEndTag()`输出如图11-5所示的结果。

## 同步脚本变量

当在TEI中定义脚本变量时，JSP容器不仅生成用于定义变量的servlet代码，还会生成用于在标签处理器内与其值同步的代码。回想一下，标签处理器使用`pageContext.setAttribute()`来分配期望的值。生成的servlet代码有对应的`pageContext.getAttribute()`语句，在标签生命周期的每个“do”方法之后将值赋给脚本变量。哪些变量以这种方式更新取决于它们在TEI中定义的范围。表11-7描述了赋值情况：

| 方法 | 同步变量的范围 |
|---|---|
| `doStartTag()` | AT_BEGIN, NESTED |
| `doInitBody()` | AT_BEGIN, NESTED |
| `doAfterBody()` | AT_BEGIN, NESTED |
| `doEndTag()` | AT_BEGIN, NESTED, AT_END |

表11-7. 脚本变量的范围如何影响同步

## 验证标签属性

除了定义脚本变量外，TEI还提供了`public boolean isValid(TagData data)`方法，可以在其中验证标签属性。在此方法中，你可以从data参数中提取属性名和值的列表，并检查它们的值是否有效。如果无效，你可以返回`false`以导致页面编译错误。例如，如果一个标签有几个属性，每个都是可选的，但必须指定其中一个，你不能仅使用TLD中的`<attribute>`元素来指定该语义。`isValid()`方法是你这样做的唯一机会。

要遍历属性列表，可以调用传递给`isValid()`的`TagData`参数中的方法。表11-8列出了一些可用的方法。

然而，`isValid()`方法的一个缺点是，没有明显的方法来发出有意义的错误消息。要么整个标签有效，要么无效。

| 方法 | 描述 |
| --- | --- |
| `public String getId()` | 返回ID属性的名称（如果已指定）。 |
| `public Object getAttribute(String name)` | 给定一个属性名，返回属性值作为对象。如果属性的值在转换时未知（即，它是通过请求时表达式指定的），此方法返回`TagData.REQUEST_TIME_VALUE`。 |
| `public String getAttributeString(String name)` | 给定一个属性名，尽可能将属性值作为`java.lang.String`返回。 |
| `public Enumeration getAttributes()` | 返回标签属性名的枚举。与`getAttribute()`结合使用，可以遍历所有属性/值对的列表。 |

表11-8. TagData中的一些有用方法

## 协作标签

自定义标签可以相互交互以执行有用的操作。一种常用的方法是通过语法作用域实现的，其中标签处理器调用其父类中的方法。本节通过一个扩展示例说明这些技术。

### 使用语法作用域

回想一下，标签可以嵌套，即一个标签可以用在另一个标签的正文中。`TagSupport`类提供了标签处理器使用其`findAncestorWithClass()`方法查找其封闭标签的标签处理器的方法。这是一个静态方法，接受两个参数——一个指向当前标签处理器的引用（`this`）和感兴趣的父标签的类：

```
OuterTag ot = (OuterTag)
    findAncestorWithClass(this, OuterTag.class);
if (ot == null)
    throw new JspException("No outer tag found");
```

一旦找到父标签，就可以直接调用其所有公共方法。下一节说明如何使用此技术。

### 示例：switch标签

我们可以使用语法作用域来模拟Java语言的`switch` . . . `case`结构。我们需要三个标签：

-   **switch** 外部标签，其正文定义了switch逻辑的范围。此标签有一个`value`属性，用于定义要测试的条件，并确定应执行哪个case块。
-   **case** 代表一个可能的case块的标签。我们将给它两个属性：一个用于指定要匹配的确切值，另一个用于指定子字符串。第三个属性指定比较是否区分大小写。我们使用TEI类的`isValid()`方法来验证只指定了前两个属性中的一个。
-   **default** 如果其他case块都不成功，则要执行的块。

以下是我们需要的TLD条目：

```
<tag>
    <name>switch</name>
    <tagclass>jspcr.taglib.util.SwitchTag</tagclass>
    <bodycontent>JSP</bodycontent>
    <info>
        The enclosing tag for a switch/case block
    </info>

    <attribute>
        <name>value</name>
        <required>true</required>
        <rtexprvalue>true</rtexprvalue>
    </attribute>
</tag>

<tag>
    <name>case</name>
    <tagclass>jspcr.taglib.util.CaseTag</tagclass>
    <teiclass>jspcr.taglib.util.CaseTEI</teiclass>
    <bodycontent>JSP</bodycontent>
    <info>
        A case block to be included in the body of a switch
    </info>

    <attribute>
        <name>match</name>
        <required>false</required>
        <rtexprvalue>true</rtexprvalue>
    </attribute>

    <attribute>
        <name>contains</name>
        <required>false</required>
        <rtexprvalue>true</rtexprvalue>
    </attribute>

    <attribute>
        <name>caseSensitive</name>
        <required>false</required>
        <rtexprvalue>true</rtexprvalue>
    </attribute>
</tag>

<tag>
    <name>default</name>
    <tagclass>jspcr.taglib.util.DefaultTag</tagclass>
    <bodycontent>JSP</bodycontent>
    <info>
        The default case included in the body of a switch
    </info>
</tag>
```

逻辑并不特别复杂。`switch`标签为其`value`属性和一个布尔型`completed`属性提供了公共访问方法，后者用于跟踪是否有case块匹配该值并声称了switch。以下是标签处理器：

```
package jspcr.taglib.util;

import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;

/**
 * A tag that emulates the switch ... case construct.
 * Within the body of this statement there can be
 * any number of case tag, including one default tag.
 * The first one that matches the text is executed,
 * and the rest are bypassed.
 */
public class SwitchTag extends TagSupport
{
    // The value attribute.  This is the text that
    // case statements will compare to.
```



private String value;
public void setValue(String value)
    { this.value = value; }
public String getValue()
    { return value; }

// 一个标志，用于指示 switch 语句
// 是否已完成。当某个 case
// 语句匹配该值并被执行时，即为完成。

private boolean complete;
public void setComplete(boolean complete)
    {this.complete = complete; }
public boolean isComplete()
    { return complete; }

/**
 * 不需要真正的设置。此方法
 * 只需要返回 EVAL_BODY_INCLUDE
 */
public int doStartTag() throws JspException
{
    return EVAL_BODY_INCLUDE;
}
}

`case` 标签也相当简单。它通过 `findAncestorWithClass()` 查找其所属的 `switch` 标签。`case` 标签首先调用 `switch` 标签的 `isComplete()` 方法，查看是否其他 `case` 已经声明了该 `switch`。如果是，则返回 `SKIP_BODY`，使其主体不被执行。否则，它调用 `switch` 标签的 `getValue()` 方法来检索要匹配的字符串。如果匹配成功，`case` 标签通过 `setComplete(true)` 声明该 `switch`，并返回 `EVAL_BODY_INCLUDE`。以下是标签处理程序的代码清单：

```
package jspcr.taglib.util;

import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;

/**
 * 如果此标签主体满足其属性中
 * 相对于所属 `switch` 标签的值
 * 所指定的条件，则将执行此主体。
 */
public class CaseTag extends TagSupport
{
    // 要精确匹配的字符串值

    private String match;
    public void setMatch(String match)
    { this.match = match; }

    // 可能包含在 `switch` 标签的值中的
    // 子串值

    private String contains;
    public void setContains(String contains)
    { this.contains = contains; }

    // 指示匹配或比较是否应区分大小写的
    // 布尔标志值

    private boolean caseSensitive;
    public void setCaseSensitive(String flag)
    {
        caseSensitive = new Boolean(flag).booleanValue();
    }

    public int doStartTag() throws JspException
    {
        // 查找所属的 `switch` 标签，以便
        // 我们可以调用其方法

        SwitchTag switchTag = (SwitchTag)
            findAncestorWithClass(this, SwitchTag.class);

        // 如果 `switch` 已被满足，
        // 则跳过此语句的主体

        if (switchTag.isComplete())
            return SKIP_BODY;

        // 如果指定了 `match` 属性，则测试精确匹配

        if (match != null) {

            String parentValue = switchTag.getValue();
            if (!caseSensitive)
                parentValue = parentValue.toUpperCase();

            String thisValue = match;
            if (!caseSensitive)
                thisValue = thisValue.toUpperCase();

            // 如果精确匹配，则声明该 `switch`

            if (parentValue.equals(thisValue)) {
                switchTag.setComplete(true);
                return EVAL_BODY_INCLUDE;
            }

            // 否则，忽略主体

            return SKIP_BODY;
        }

        // 如果指定了 `contains` 属性，则测试子串匹配

        if (contains != null) {

            String parentValue = switchTag.getValue();
            if (!caseSensitive)
                parentValue = parentValue.toUpperCase();

            String thisValue = contains;
            if (!caseSensitive)
                thisValue = thisValue.toUpperCase();

            // 如果父值包含此子串，
            // 则声明该 `switch`

            if (parentValue.indexOf(thisValue) != -1) {
                switchTag.setComplete(true);
                return EVAL_BODY_INCLUDE;
            }

            // 否则，忽略主体

            return SKIP_BODY;
        }

        return SKIP_BODY;
    }
}
```

TEI（TagExtraInfo）验证是否指定了 `match` 属性或 `contains` 属性之一，但不能同时指定两者：

```
package jspcr.taglib.util;

import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;

/**
 * 验证 `case` 标签的属性
 */
public class CaseTEI extends TagExtraInfo
{
    public boolean isValid(TagData tagData)
    {
        // 标签必须包含 `match` 属性或
        // `contains` 属性之一，但不能同时包含两者。

        boolean noMatch =
            (tagData.getAttribute("match") == null);

        boolean noContains =
            (tagData.getAttribute("contains") == null);

        return (noMatch != noContains);
    }
}
```

默认标签处理程序的工作方式与 `case` 类似，只是其匹配条件始终为真。`default` 的工作方式与其 Java 对应物不完全相同，因为它不能保证最后执行，除非它恰好在最后编码。以下是源代码：

```
package jspcr.taglib.util;

import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;

/**
 * 如果没有遇到其他满足所属 `switch` 标签的
 * `case` 标签，则将执行此标签的主体。
 */
public class DefaultTag extends TagSupport
{
    public int doStartTag() throws JspException
    {
        // 查找所属的 `switch` 标签，以便
        // 我们可以调用其方法

        SwitchTag switchTag = (SwitchTag)
            findAncestorWithClass(this, SwitchTag.class);

        // 如果 `switch` 已被满足，
        // 则跳过此语句的主体

        if (switchTag.isComplete())
            return SKIP_BODY;

        // 否则，声明该 `switch`

        switchTag.setComplete(true);
        return EVAL_BODY_INCLUDE;
    }
}
```

这些标签结合使用，可以测试一个条件并执行所需的代码块。以下 JSP 页面演示了它们的用法：

```
<%@ page session="false" %>
<%@ taglib prefix="util" uri="/WEB-INF/tlds/util.tld" %>

<%
String value = request.getParameter("value");
if (value == null)
    value = "B";
%>
<H3>值为 <%= value %></H3>
<util:switch value="<%= value %>">
    <util:case match="A">
        <H3>选择了 match="A" 的 case 代码块</H3>
    </util:case>
    <util:case contains="B">
        <H3>选择了 contains="B" 的 case 代码块</H3>
    </util:case>
    <util:default>
        <H3>未选择任何 case 代码块</H3>
    </util:default>
</util:switch>
```

当我们使用参数值 *A* 运行 JSP 页面时，得到如图 11-6 所示的结果。当值为 beauty（包含 *B*，不区分大小写）时，结果如图 11-7 所示。最后，如果值为 *C*，与任何 case 代码块都不匹配，则得到的页面如图 11-8 所示。

![图 11-6. 值为 A 时的 switch 测试](img/7a2f73369bb140583c7288b73456addb_271_0.png)

**图 11-6.** 值为 A 时的 switch 测试

![图 11-7. 值为 beauty 时的 switch 测试](img/7a2f73369bb140583c7288b73456addb_272_0.png)

**图 11-7.** 值为 beauty 时的 switch 测试

![图 11-8. 值为 C 时的 switch 测试](img/7a2f73369bb140583c7288b73456addb_272_1.png)

**图 11-8.** 值为 C 时的 switch 测试

## 数据库查询示例的实现

本章以开头描述的数据库查询示例的实现作为结束：

```
<db:connect url="mydatabase">
    <db:runQuery>
        SELECT *
        FROM FD_GROUP
        WHERE FdGp_Desc LIKE '%F%'
        ORDER BY FdGp_Cd
    </db:runQuery>
    <table border="1" cellpadding="3" cellspacing="0">
        <tr><th>食品组代码</th><th>描述</th></tr>
        <db:forEachRow>
            <tr>
                <td><db:getField name="FdGp_Cd"/></td>
                <td><db:getField name="FdGp_Desc"/></td>
            </tr>
        </db:forEachRow>
    </table>
</db:connect>
```

## 必要的标签

存在四个协作标签：

- **connect**：打开数据库连接并管理隐式的 Statement 和 ResultSet 对象
- **runQuery**：在标签主体中读取 SQL 语句，并告诉 `connect` 标签执行它
- **forEachRow**：ResultSet 的迭代器
- **getField**：检索命名字段的当前值

## 标签库描述符

这些标签的 TLD 如下所示：

```
<tag>
    <name>connect</name>
    <tagclass>jspcr.taglib.jdbc.ConnectTag</tagclass>
    <bodycontent>JSP</bodycontent>
    <info>打开数据库连接并管理
            Statement 和 ResultSet 对象</info>

    <attribute>
        <name>url</name>
        <required>true</required>
        <rtexprvalue>true</rtexprvalue>
    </attribute>

</tag>
```

`connect` 标签打开一个连接并管理一个 Statement 和 ResultSet 对象。它们不会作为脚本变量暴露；只能通过此库中的其他标签访问。连接在遇到结束标签时关闭。语法是

```
<db:connect url="mydatabase">
```

驱动程序类名可以很容易地作为另一个属性添加。这里我为了简化 JSP 而将其设为隐式。

```
<tag>
    <name>runQuery</name>
    <tagclass>jspcr.taglib.jdbc.RunQueryTag</tagclass>
    <bodycontent>JSP</bodycontent>
    <info>从标签主体中读取并执行 SQL 语句</info>
</tag>
```

`runQuery` 标签从其主体中读取一条 SQL 语句，并使用所属 `connect` 标签创建的 Statement 对象执行它。它只能在 `connect` 标签的主体中使用。`runQuery` 标签的语法是

```
<db:runQuery>sql statement</db:runQuery>
```



## 标签处理器

需要开发四个标签处理器。由于没有定义脚本变量，我们不需要任何 TEI 类。

结果集也由 connect 标签管理。

```xml
<tag>
    <name>forEachRow</name>
    <tagclass>jspcr.taglib.jdbc.ForEachRowTag</tagclass>
    <bodycontent>JSP</bodycontent>
    <info>Iterates over the current result set</info>
</tag>
```

forEachRow 标签遍历当前结果集，以便 getField 标签可以访问其值。它只能在 runQuery 标签之后，用于 connect 标签的主体内。其语法是

```jsp
<db:forEachRow>
...
</db:forEachRow>
```

```xml
<tag>
    <name>getField</name>
    <tagclass>jspcr.taglib.jdbc.GetFieldTag</tagclass>
    <bodycontent>empty</bodycontent>
    <info>Retrieves a field
        from the current result set row</info>

    <attribute>
        <name>name</name>
        <required>true</required>
        <rtexprvalue>true</rtexprvalue>
    </attribute>

</tag>
```

getField 标签从当前结果集行中读取一个字段，并将其值作为字符串返回。它只能出现在 forEachRow 标签的主体中。其语法是

```jsp
<db:getField name="fieldName"/>
```

## Connect

connect 标签接受一个数据库 URL 作为属性，因此标签处理器需要一个实例变量和一个 `setUrl()` 方法：

```java
package jspcr.taglib.jdbc;

import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.*;
import java.sql.*;

/**
 * ConnectTag
 */
public class ConnectTag extends TagSupport
{
    public static final String DRIVER_CLASS
        = "sun.jdbc.odbc.JdbcOdbcDriver";

    // ============================================
    //    标签属性
    // ============================================

    private String url;

    public void setUrl(String url)
    {
        this.url = url;
    }
}
```

它定义了 Connection、Statement 和 ResultSet 对象，并为每个对象提供了公共的访问方法，以及一个公共的 `runQuery()` 方法：

```java
// ============================================
//    由此标签管理的 JDBC 对象
// ============================================

private Connection con;
private Statement stmt;
private ResultSet rs;

public Connection getConnection() { return con; }
public Statement getStatement() { return stmt; }
public ResultSet getResultSet() { return rs; }

/**
* 运行查询
* @param sql SQL 语句
*/
public void runQuery(String sql)
    throws SQLException
{
    rs = stmt.executeQuery(sql);
}
```

整个数据库操作包含在开始和结束标签之间，因此两个生命周期方法管理启动和关闭：

```java
// ==================================
//    生命周期方法
// ==================================

/**
* 加载驱动程序类，打开数据库连接，
* 并创建 Statement 对象
*/
public int doStartTag() throws JspException
{
    con = null;
    try {
        Class.forName(DRIVER_CLASS);
        con = DriverManager.getConnection(url);
        stmt = con.createStatement();
    }
    catch (Exception e) {
        throw new JspException(e.getMessage());
    }
    return EVAL_BODY_INCLUDE;
}

/**
* 关闭连接和其他 JDBC 对象
*/
public int doEndTag() throws JspException
{
    try {
        if (rs != null) {
            rs.close();
            rs = null;
        }
        if (stmt != null) {
            stmt.close();
            stmt = null;
        }
        if (con != null) {
            con.close();
            con = null;
        }
    }
    catch (SQLException e) {
        throw new JspException(e.getMessage());
    }
    return EVAL_PAGE;
}
}
```

## RunQuery

runQuery 标签做三件事：

- 从其主体中提取 SQL 语句。
- 查找外层的 connect 标签。
- 执行 `connect.runQuery()` 方法。

源代码如下：

```java
package jspcr.taglib.jdbc;

import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.*;
import java.sql.*;
import java.util.*;

/**
 * RunQueryTag
 */
public class RunQueryTag extends BodyTagSupport
{
    /**
     * 读取标签主体中的 SQL 语句，
     * 并要求 connect 标签执行它。
     */
    public int doEndTag() throws JspException
    {
        // 获取要运行的 SQL

        String sql = bodyContent.getString();
        if (sql == null)
            throw new JspException
                ("No SQL statement found in body of runQuery tag");

        sql = sql.trim();
        if (sql.equals(""))
            throw new JspException
                ("Empty SQL statement found in body of runQuery tag");

        // 定位外层的 connect 标签

        ConnectTag connectTag = (ConnectTag)
            findAncestorWithClass(this, ConnectTag.class);
        if (connectTag == null)
            throw new JspException
                ("runQuery must be used in the body of a connect tag");

        // 告诉 connect 标签运行查询

        try {
            connectTag.runQuery(sql);
        }
        catch (SQLException e) {
            throw new JspException(e.getMessage());
        }

        // 正常返回

        return EVAL_PAGE;
    }
}
```

## ForEachRow

这是一个迭代器标签，类似于本章前面描述的 `enumerate` 标签。与 `runQuery` 一样，它首先使用 `findAncestorWithClass()` 获取对 `connect` 标签的引用。从 `connect` 标签处理器实例中，它可以使用 `getResultSet()` 获取结果集。通过使用一个名为 `incrementRow()` 的私有便捷方法，它将结果集推进到下一行。`doStartTag()` 或 `doAfterBody()` 都可以检测到结果集的结束，并相应地返回 `SKIP_BODY`。

```java
package jspcr.taglib.jdbc;

import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.*;
import java.sql.*;

/**
 * ForEachRowTag
 */
public class ForEachRowTag extends BodyTagSupport
{
    private ConnectTag connectTag;

    /**
     * 为结果集的第一次迭代做准备
     */
    public int doStartTag() throws JspException
    {
        connectTag = (ConnectTag)
            findAncestorWithClass(this, ConnectTag.class);
        if (connectTag == null)
            throw new JspException
                ("forEachRow must be in the body of a connect tag");
        return incrementRow();
    }

    /**
     * 在每一行被求值后，
     * 递增结果集，并在到达末尾时指示。
     */
    public int doAfterBody() throws JspException
    {
        return incrementRow();
    }

    /**
     * 当到达结束标签时，输出结果
     */
    public int doEndTag() throws JspException
    {
        try {
            pageContext.getOut().print(bodyContent.getString());
        }
        catch (IOException e) {
            throw new JspException(e.getMessage());
        }
        return EVAL_PAGE;
    }

    /**
     * 用于获取下一行的便捷方法。
     * 由 doStartTag()
     * 和 doAfterBody() 使用。
     * 如果存在行则返回 EVAL_BODY_TAG，
     * 否则返回 SKIP_BODY。
     */
    private int incrementRow() throws JspException
    {

        ResultSet rs = connectTag.getResultSet();

        if (rs == null)
            throw new JspException
                ("No result set found - no query has been run");

        // 获取下一行或指示没有更多行

        boolean hasNext = false;
        try {
            hasNext = rs.next();
        }
        catch (SQLException e) {
            throw new JspException(e.getMessage());
        }

        return (hasNext) ? EVAL_BODY_TAG : SKIP_BODY;
    }
}
```

## GetField

与其对应的 `runQuery` 和 `forEachRow` 一样，`getField` 使用外层 `connect` 标签中的公共方法。它从 `ResultSet` 中提取指定的字段值，并将其发送到当前输出写入器。

```java
package jspcr.taglib.jdbc;

import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.*;
import java.sql.*;

/**
 * GetFieldTag
 */
public class GetFieldTag extends TagSupport
{
    private String name;

    public void setName(String name)
    {
        this.name = name;
    }

    /**
     * 将结果集中指定字段的值
     * 作为字符串返回。
     */
    public int doEndTag() throws JspException
    {
```



## 获取外围的 Connect 标签

```java
ConnectTag connectTag = (ConnectTag)
    findAncestorWithClass(this, ConnectTag.class);
if (connectTag == null)
    throw new JspException
        ("getField must be in the body of a connect tag");
```

## 获取其当前结果集

```java
ResultSet rs = connectTag.getResultSet();
if (rs == null)
    throw new JspException
        ("No result set exists - no query has been run");

try {
    // Get the specified field and write it
    // to the output stream

    String value = rs.getString(name);
    JspWriter out = pageContext.getOut();
    out.print(value);
}
catch (SQLException e) {
    throw new JspException(e.getMessage());
}
catch (IOException e) {
    throw new JspException(e.getMessage());
}

// Normal completion

return SKIP_BODY;
```

当数据库查询运行时，它会产生如图 11-9 所示的结果。

![图 11-9. 数据库查询的输出](img/7a2f73369bb140583c7288b73456addb_284_0.png)

## 总结

自定义标签是扩展 JSP 制作环境的一种优雅而稳健的方法，它允许开发团队提供一套特定于应用的 JSP 标签工具包，供不精通 Java 编程的页面设计者使用。一个标签的功能由一个称为*标签处理器*的 Java 类实现，该类提供了在标签生命周期的各个点由 JSP 容器调用的方法。一组相关的标签可以协同工作以完成复杂的任务。标签处理器和配置信息的集合被打包在*标签库*中，它们具有与供应商无关的结构，可以以最小的努力进行部署。

## 第三部分

### JSP 实战

本节探讨 JSP 如何与 Java 环境的主要组件协同工作。在了解了 HTML 表单和 JDBC 数据库访问的背景知识后，你将研究会话管理、线程、JavaBeans 和 XML 等高级主题。第 17 章和第 18 章分别涵盖调试和部署 Web 应用程序，第 19 章则呈现了一个整合全书技术的完整案例研究。

版权所有 2001 The McGraw-Hill Companies, Inc. 点击此处查看使用条款。

此页有意留白。

完全参考手册

## 第 12 章

### HTML 表单

大多数应用程序在某个时刻需要用户输入，而在 Web 环境中，这种输入通常来自 HTML 表单。就像其纸质对应物一样，HTML 表单由一系列按逻辑顺序排列的标签和输入字段组成。当用户填写表单并点击提交按钮时，输入字段的名称和值会被传输到与 Web 服务器关联的程序进行处理。图 12-1 展示了一个典型的表单。

HTML 提供了一组基本的元素或输入控件，可以适应广泛的数据输入需求。这组元素包括：

- **文本输入元素** - 用于单行或多行输入的矩形框。
- **选择菜单** - 以下拉列表框形式显示的选项列表。这些列表可以有一个显示在屏幕上的外部形式，以及一个与所选项关联的内部代码值。

![图 12-1](img/7a2f73369bb140583c7288b73456addb_288_0.png)

- **按钮** - 模拟控制面板上按钮的矩形控件。它们最常用于发起命令，例如提交表单或清除输入字段。
- **复选框** - 可勾选或未勾选、开或关的小方块。复选框可用于指定具有是或否值的选项。
- **单选按钮** - 与复选框类似，单选按钮也表示是或否的值。然而，它们通常以互斥组的形式出现，因此选择一个会导致其他所有按钮取消选择。
- **文件选择元素** - 允许用户指定要上传文件名的控件。通常，此控件包含一个浏览按钮，点击后会弹出一个文件选择对话框。
- **隐藏元素** - 用于创建具有恒定值的参数的不可见元素。

可在 HTML 表单中使用的元素集是标准化的，并在 HTML 规范中正式记载（可在 http://www.w3.org/TR/html4/ 获取）。该规范是*万维网联盟* (W3C) 的工作成果，随着新功能的出现定期更新。正如预期的那样，并非所有浏览器都实现了所有功能。本章以 HTML 4.01 为基础来描述表单的工作原理，但主要介绍那些得到广泛支持的元素和属性。

本章描述 HTML 表单中使用的元素、它们的使用方法以及浏览器如何渲染它们。它讨论了表单如何验证和提交。然后，本章简要探讨了表单处理的服务器端。

## FORM 元素

FORM 元素是 HTML 表单背后的基本结构，主要有三个目的：

- 在语法上将输入元素分组在一起
- 标识处理表单处理的服务器端程序
- 指定要发送的数据值及其格式

FORM 元素在 HTML 中用 `<FORM>` 标签描述。此元素的语法如下所示：

```
<FORM
    action="uri"
    method="method"
    enctype="content type"
    accept-charset="charsets"
    accept="content types"
    name="form name">
    ...
</FORM>
```

属性及其值在下一节中描述。

## FORM 元素的属性

在列出的六个属性中，唯一必需的是 `action`。在实践中，除了 `action` 和 `method` 之外的其他属性很少使用。以下是每个属性的定义。

## action 属性

当表单填写完成且用户点击提交按钮时，Web 浏览器会创建一个 HTTP 请求，将所有表单数据打包并将其发送到某个 Web 服务器上的程序。此程序在 `action` 属性中指定。

`action` 属性的值必须是一个 HTTP *统一资源标识符* (URI)。（有关 URI 的正式定义，请参阅 http://www.ietf.org/rfc/rfc2396.txt。）这意味着它具有以下形式：

```
[http://<servername>][/<path>]
```

要提交表单，Web 浏览器会打开一个到指定服务器（默认为下载 HTML 页面的服务器）的套接字连接，并使用指定的路径发出 HTTP 请求。该路径通常指向一个 servlet、JSP 页面或 CGI 程序。此程序接收 HTTP 请求和表单数据，数据可以在 URI 本身中，也可以在输入流中，具体取决于所使用的 HTTP 方法（请参阅下面的 `method`）。

可以在 URI 上指定查询字符串。在这种情况下，编码在查询字符串中的参数会与表单正文中的参数合并。这通常是不必要的，因为一个隐藏字段可以达到同样的目的。

## method 属性

HTTP 协议提供了多种请求类型，用于文件传输、下载、删除和诊断操作。其中，只有 GET 和 POST 适用于 HTML 表单。`method` 属性就是指定此内容的地方。

HTTP GET 或 POST 请求通常被 Web 服务器解释为检索 URI 中命名的文档的请求。当 Web 服务器被配置为处理 servlet、CGI 程序或其他服务器端脚本环境时，它会将对这些资源的请求解释为调用它们作为程序的请求。此类程序产生的输出（通常是 HTML 文档）会像按名称请求的静态文档一样，被发送回请求者。

在 HTML 表单中使用时，GET 和 POST 方法的区别在于它们向服务器进程提供输入数据的方式：

- **GET** - 表单值作为查询字符串附加到 URI
- **POST** - 表单值在输入流中提供

虽然两种方法都可以使用，并且 servlet API 使选择变得相当透明，但应考虑几个特性。因为 GET 请求导致输入值附加到请求 URI，所以它们在浏览器地址栏和 Web 服务器日志中作为名称/值对可见。这使得 GET 不适合发送敏感数据，如密码。此外，某些服务器和浏览器可能对其可以处理的 URL 长度有限制。另外，HTTP 规范将 GET 请求描述为*幂等的*，这意味着它们可以安全地重复而不会产生不良副作用。在某些情况下，这意味着服务器可以告诉客户端重用其现有的资源副本，而不是发送新副本。这通常不是你想要的对表单输入的响应。出于这些原因，POST 通常是请求方法更好的选择。

method 属性是可选的。如果未指定，则默认使用 GET。该属性的值可以用大写或小写指定。

## enctype 属性

表单输入值可以通过几种不同的方式传输到服务器。将值编码为数据流的方法称为*内容类型*，并在使用 POST 方法时在 enctype 属性中指定。存在两种常用的编码方式：

- application/x-www-form-urlencoded
- multipart/form-data

**application/x-www-form-urlencoded** - 如果未指定（通常如此），enctype 属性的值是 application/x-www-form-urlencoded。（有关 URL 编码的完整讨论，请参阅 RFC 1738，可在 http://www.freesoft.org/CIE/RFC/1738/index.htm 获取。）此编码技术涉及以下步骤：

1. 将输入元素名称或值中的所有非空白特殊字符<sup>1</sup>替换为 %xx，其中 xx 是相应 ASCII 字符代码的两位十六进制值。
2. 将任何空格替换为加号 (+)。

> <sup>1</sup> 关于这些字符是什么存在一些分歧。RFC 1738 将它们描述为除 "$-_.+!*'()," 之外的任何非字母数字字符。然而，Internet Explorer、Netscape Navigator 和 java.net.URLEncoder 将排除项限制为仅为 "-_.*"。无论如何，由于编码和解码都是由达成一致的程序完成的，所以这并不是一个真正的问题。



## 266 JSP：完整参考

3. 将每个结果名称和值对用等号 (=) 连接。
4. 按表单中出现的顺序连接结果字符串，并用与号 (&) 分隔。

服务器端进程通过反向执行每个步骤来解码，恢复原始的参数名称和值。

例如，如果表单包含一个名为 `product` 的输入字段，其值为“Great Music@Home”，另一个名为 `quantity` 的字段，其值为 3，则编码后的字符串将是：

```
product=Great+Music%40Home&quantity=3
```

URL 编码的目的是安全地将字符串附加到 URL。如果 URL 中出现空格、引号或其他分隔符字符，可能会让处理它们的程序产生混淆。

**multipart/form-data** multipart/form-data 是一种较新的方法，主要用于支持文件上传。（RFC 2388 (http://www.ietf.org/rfc/rfc2388.txt) 描述了在 HTML 表单中使用 multipart/form-data。）在这种编码方式中，每个输入字段及其值都作为自己的块在输入流中发送。一个称为 `boundary` 的特殊分隔符字符串标记每个块的开始和结束。边界是由 Web 浏览器选择的伪随机字符串，并在 `Content-Type` 头中指定。每个块内包含一个或多个 HTTP 头，后跟一个空行，然后是一行包含输入字段值的内容。字段名在 `Content-Disposition` 头中传递。

因此，使用前面的例子，如果表单包含输入字段 `product`（值为“Great Music@Home”）和 `quantity`（值为 3），浏览器将创建一个包含类似以下内容的 HTTP 请求：

```
POST /someURI HTTP/1.0
Content-Type: multipart/form-data;boundary=7d025a324c0138
Content-Length: 178

--7d025a324c0138
Content-Disposition: form-data; name="product"

Great Music@Home
--7d025a324c0138
Content-Disposition: form-data; name="quantity"

3
--7d025a324c0138--
```

multipart/form-data 编码的主要缺点是当前的 servlet API 不直接支持它。也就是说，无法通过 `getParameterNames()` 检索单个字段名，也无法通过 `getParameterValues()` 读取它们的值。必须读取和解析输入流才能获取这些信息。

## accept-charset 属性

HTTP 使用的字符集是将一组字节转换为一组字符的规则集。最广泛使用的字符集是 ISO-8859-1，它是 ASCII 的超集，映射了 127-255 范围内的额外字节值。如果使用 accept-charset，它应该包含一个以逗号或空格分隔的字符集值列表。

accept-charset 的目的是指示服务器程序可以解释和处理哪些字符集。然而，实际上，这个属性很少使用，并且似乎被 Internet Explorer 和 Netscape Navigator 忽略了。

## accept 属性

FORM 标签可以指示其服务器端处理程序设计接受的内容类型。如果指定，accept 属性必须包含一个逗号分隔的内容类型列表，例如 text/html 或 image/jpg。然而，这只是一个给 Web 浏览器的提示，浏览器可以自由忽略它（大多数浏览器确实如此）。

## name 属性

表单可以有一个名称，该名称用于在文档其他地方的 <SCRIPT> 部分中引用它。例如，在以下表单中：

```
<form
   method="post"
   action="diag/ShowParms.jsp"
   name="prodform"
   onsubmit="return checkform();">
<pre>
Product: <input type="text" name="product"
Quantity: <input type="text" name="quantity"
</pre>
</form>
```

JSP IN ACTION

其中 `checkform()` 是一个验证表单输入字段的 JavaScript 函数，`checkform()` 可以分别将两个输入字段的值读取为 `document.prodform.product.value` 和 `document.prodform.quantity.value`。HTML 规范已弃用 `name` 属性，转而使用 `id` 属性，然而，JavaScript 文档对象模型尚未识别 `id`。如果需要将表单与 JavaScript 集成，`name` 仍然是更好的选择。

## 表单输入元素

在 `<FORM>...</FORM>` 标签的主体内，描述了各个数据字段。HTML 包含每个字段的描述性标签和创建所需控件的相应 HTML 标签。视觉布局通常使用 HTML 表格来完成，以便字段标签和控件在水平和垂直方向上对齐。生成图 12-1 所示表单的 HTML 如下：

```
<form method="post" action="diag/ShowParms.jsp">
<table border="0" cellpadding="3" cellspacing="0">

    <tr valign="top">
        <td>From:</td>
        <td><input name="from" type="text" size=32></td>
    </tr>

    <tr valign="top">
        <td>To:</td>
        <td>
            <select name="to" size=1>
                <option value="CS">Customer Service
                <option value="EX">Executive
                <option value="FI">Finance
                <option value="HR">Human Resources
                <option value="IT">Information Technology
                <option value="MK">Marketing
                <option value="FA">Facilities
                <option value="PC">Purchasing
                <option value="SP">Shipping
            </select>
        </td>
    </tr>

    <tr valign="top">
<td>Your e-mail:</td>
<td><input name="email" type="text" size=20></td>
</tr>

<tr valign="top">
<td>Phone number:</td>
<td>
<input name="phone" type="text" size=20>
<input name="dayphone" type="radio" value="1" checked>Day
<input name="dayphone" type="radio" value="0">Evening
</td>
</tr>

<tr valign="top">
<td>Comments:</td>
<td>
<textarea name="comments" rows=5 cols=40></textarea>
</td>
</tr>

<tr valign="top">
<td colspan=2>
<font size=-1>
Please check all that apply: <br>
<input name="category" type="checkbox" value="1">
Comment only, no response necessary <BR>
<input name="category" type="checkbox" value="2">
Please add me to your mailing list
</font>
</td>
</tr>

<tr valign="top">
<td>&nbsp;</td>
<td>
<input type="submit" value="Send">
<input type="reset" value="Clear">
</td>
</tr>

<input type="hidden" name="remoteHost" value=" <%= request.getRemoteHost() %>"
value="209.170.132.238">
    <input type="hidden" name="userAgent"
value="Mozilla/4.0 (compatible; MSIE 5.0; Windows NT; DigExt)">
</table>
</form>
```

我们将在本节的示例中使用此表单。
四组 HTML 标签用于创建表单输入元素：

- `<INPUT>` 用于多种特定元素类型的通用标签。
- `<SELECT>` 和 `<OPTION>` 用于创建菜单或下拉列表框。
- `<TEXTAREA>` 用于多行文本输入。
- `<BUTTON>` 用于创建提交、重置和通用按钮。此标签尚未得到广泛支持，因此此处不作介绍。

## 使用 INPUT 标签创建的元素

HTML INPUT 标签用于多种元素类型。它有大量属性，其中许多仅适用于特定字段类型。以下语法图描述了大多数类型通用的属性：

```
<INPUT
    type="text | password | checkbox | radio | submit |
    reset | file | hidden | image | button"
    name="name"
    value="value"
    size="size">
```

其中属性定义如下：

- **type="type"** 指示要使用的特定字段类型。如果未指定，则默认为 text。
- **name="name"** 用于为字段分配一个标识符，以便可以通过脚本或样式表进行操作。这也是服务器程序检索该字段的名称。
- **value="value"** 可用于为字段分配初始值。
- **size="size"** 指示其可视宽度，以像素或字符为单位（对于文本字段）。

除了这些属性之外，INPUT 标签还可以指定事件处理程序，当发生特定事件时在浏览器中调用脚本操作。事件的值

handler 属性是一段脚本代码，通常是 JavaScript。事件处理程序属性以其处理的事件命名，并带有“on”前缀：

- **onfocus** 在用户使用 Tab 键切换到该字段或在该字段内点击鼠标，使其获得键盘焦点时触发。
- **onblur** 在用户使用 Tab 键切换出或点击出该字段，使其失去键盘焦点时触发。
- **onselect** 在选中文本时触发（Netscape Navigator 不支持此事件）。
- **onchange** 在用户更改控件的值，然后通过 Tab 键切换出或点击出该字段来提交更改时触发。

当表单提交时，浏览器会提取每个控件的名称和值，根据 `<FORM>` 标签上指定（或隐含）的编码类型进行转换，并将生成的数据流发送到服务器进程。以下部分将介绍每种 `<INPUT>` 类型：

## Text

这是最简单和最常用的 `<INPUT>` 类型，用于输入单行文本。其语法如下：

```
<INPUT
    type="text"
    name="name"
    value="value"
    size="size"
    maxlength="maxlength">
```

各属性含义如下：

- **type="text"** 表示这是一个文本控件。
- **name="name"** 指定一个脚本可以引用此控件的名称。这也是服务器程序可以用来检索文本的名称。
- **value="value"** 可用于分配初始文本值。当表单与表单处理程序的输出位于同一页面时，此属性很有用。
- **size="size"** 指定显示宽度。如果未指定，浏览器会选择一个默认大小，这可能并不合适。最好指定一个首选大小。
- **maxlength="maxlength"** 设置可以输入到字段中的字符数限制。

TEXT 输入元素通常显示为一个矩形框。例如，此处的 HTML 代码，

```
<tr valign="top">
    <td>From:</td>
    <td><input name="from" type="text" size=32></td>
</tr>
```

可能渲染成这样：

![img/7a2f73369bb140583c7288b73456addb_298_0.png](img/7a2f73369bb140583c7288b73456addb_298_0.png)

## Password

密码控件是文本控件的一种变体。唯一的区别是用户输入的字符在屏幕上不可见。取而代之的是，为每个输入的字符显示一个掩码字符，例如星号。密码输入标签的语法如下所示：

```
<INPUT
    type="password"
    name="name"
    value="value"
    size="size"
    maxlength="maxlength">
```

各属性与文本输入标签具有相同的含义。密码输入元素通常也显示为一个矩形框。例如，此处的 HTML 代码，用于技术支持应用程序

```
<tr valign="top">
    <td>Support ID:</td>
    <td><input name="suppid" type="password" size=10></td>
</tr>
```

可能渲染成这样：

![img/7a2f73369bb140583c7288b73456addb_298_1.png](img/7a2f73369bb140583c7288b73456addb_298_1.png)

> **注意** 这是一种最基本的安全措施，旨在防止窥视者看到在密码字段中输入的内容。但是，发送到服务器进程的字符是用户最初输入的字符，而不是星号。使用密码控件不会加密或以其他方式隐藏字段的值，除了在输入时进行视觉隐藏。

## Checkbox

复选框控件用于呈现一个真或假的选项。其语法如下所示，

```
<INPUT
    type="checkbox"
    name="name"
    value="value"
    checked>
```

各属性定义如下：

- **type="checkbox"** 表示这是一个复选框控件。
- **name="name"** 指定一个脚本可以引用此复选框的名称。这也是服务器程序可以用来检索复选框值的名称。如果一组复选框代表同一字段的多个值，且这些值不是互斥的，那么它们可以拥有相同的名称。
- **value="value"** 可用于指定当此框被选中时返回的值。如果未指定，则默认为两个字符的字符串 `on`。（是 `on`，而不是 `true`、`1`、`yes` 或 `checked`。）
- **checked**，如果存在，表示复选框具有初始选中状态。

复选框支持一个额外的事件处理程序属性：

- **onclick** 在用户点击复选框时触发；

它不支持 `onchange` 事件。复选框通常渲染为一个小的方形框，有勾选标记或没有，反映控件的布尔值。例如，此处的 HTML 代码，

```
<tr valign="top">
    <td colspan=2>
    <font size=-1>
    Please check all that apply: <br>
    <input name="category" type="checkbox" value="1">
        Comment only, no response necessary <BR>
    <input name="category" type="checkbox" value="2">
        Please add me to your mailing list
    </font>
</td>
</tr>
```

可能看起来像这样：

请勾选所有适用的选项：
☑ 仅评论，无需回复
☑ 请将我加入您的邮件列表

## Radio

单选按钮控件与复选框类似，用于呈现一个真或假的选项。不同之处在于，一组单选按钮在操作上是互斥的。当点击一个时，任何其他具有相同 `name` 属性的按钮都会被清除。从这方面来说，它们的操作类似于汽车收音机上的按钮——当一个被按下时，任何其他按钮都会弹出。单选按钮控件的语法如下所示

```
<INPUT
    type="radio"
    name="name"
    value="value"
    checked>
```

各属性定义如下：

- **type="radio"** 表示这是一个单选按钮控件。
- **name="name"** 指定一个脚本可以引用此单选按钮的名称。这也是服务器程序可以用来检索单选按钮值的名称。如果一组单选按钮代表同一字段的互斥值，那么它们可以拥有相同的名称。
- **value="value"** 指定当此按钮处于选中状态时，随表单返回的值。这是一个必需属性。
- **checked**，如果存在，表示此单选按钮是该组中初始选中的那个。

与复选框一样，单选按钮支持 onclick 事件，但不支持 onchange。单选按钮通常渲染为一个小圆圈，内部有点或没有点，反映控件的布尔值。例如，此处的 HTML 代码，

```
<tr valign="top">
    <td>Phone number:</td>
    <td>
        <input name="phone" type="text" size=20>
        <input name="dayphone" type="radio" value="1" checked>Day
        <input name="dayphone" type="radio" value="0">Evening
    </td>
</tr>
```

可能看起来像这样：

电话号码：(919) 555-1833 ☉ 白天 ○ 晚上

## Submit

要向服务器提交表单，必须有一种方式来指示用户已完成数据输入。这就是提交输入类型（Submit）的作用。提交按钮与其他控件不同，因为它通常不会将数据添加到发送到服务器的数据流中。以下是提交按钮的语法，

```
<INPUT
    type="submit"
    name="name"
    value="value">
```

各属性定义如下：

- **type="submit"** 表示这是一个提交控件。
- **name="name"** 指定一个脚本或服务器程序可以引用此提交按钮的名称。从服务器的角度来看，这通常是不必要的，因为很明显，一定是点击了提交按钮，否则表单就不会被提交。但是，如果表单中有几个提交按钮，并且每个按钮都有不同的值，那么这个属性就很有用。
- **value="value"** 指定按钮上显示的值（如果也存在 `name` 属性，则随表单返回）。如果未指定，在 Internet Explorer 5.x 和 Netscape Communicator 4.75 中默认为“Submit Query”。其他浏览器可能会提供不同的默认值。

此控件支持 onclick 事件，但不支持 onchange。提交按钮通常渲染为一个矩形按钮，其文本由 `value` 属性指定。例如，如果提交按钮像这样编码，

```
<input type="submit" value="Send">
```



## 重置

与提交密切相关的是重置，用于将表单中的所有控件设置回其初始值。与提交按钮一样，重置不会对发送到服务器的数据流做出贡献。其语法如下：

```
<INPUT
type="reset"
value="value">
```

其属性定义如下：

-   **type="reset"** 表示这是一个重置控件。
-   **value="value"** 指定显示在按钮上的值（如果也存在 `name` 属性，则会随表单一起返回）。如果未指定，则默认为 "Reset"（重置）。

此控件支持 `onclick` 事件，但不支持 `onchange`。
重置按钮通常呈现为一个矩形按钮，其文本由 `value` 属性指定。例如，如果一个提交按钮像这样编码：

```
<input type="reset" value="Clear">
```

它可能看起来像这样：

![](img/7a2f73369bb140583c7288b73456addb_302_1.png)

## 文件

某些应用程序需要将文件上传到服务器。例如，技术支持应用程序可能处理用户发送的堆栈跟踪信息。公告板系统可能接受文件提交。作为此类应用程序前端的网页可以使用 `file` 输入控件。其语法如下：

```
<INPUT
type="file"
name="name"
size="size">
```

其属性定义如下：

-   `type="file"` 表示这是一个文件控件。
-   `name="name"` 指定脚本可以引用此文件控件的名称。这也将是服务器程序已知该字段的名称，尽管格式不同，你很快就会看到。
-   `size="size"` 指定文件名输入字段的可视宽度。

文件控件通常呈现为一个文本字段和一个关联的“浏览”按钮。文件名可以直接在文本字段中输入，或者用户可以单击该按钮使用文件选择对话框：

![](img/7a2f73369bb140583c7288b73456addb_303_0.png)

表单要使用文件控件，必须进行两项更改：

-   请求方法*必须*是 POST。
-   编码类型（在 `<FORM>` 标签的 `enctype` 属性中指定）*必须*是 multipart/form-data。

如果这些条件不满足，控件仍然会显示，但会被当作普通的文本输入字段处理——只有文件名会被发送到服务器。

服务器程序也必须进行更重大的更改。它必须能够使用本章前面讨论的 multipart/form-data 编码格式来提取文件内容以及其他非文件参数值。

> **注意** Web 服务器也可以对可上传文件的大小施加限制。这些限制的目的是防止使用巨大文件来使 Web 服务器崩溃的拒绝服务攻击。

作为文件上传应用程序的一个示例，假设 LyricNote.com 赞助一场竞赛，用户可以上传自己音乐作品的 MIDI 文件<sup>2</sup>。竞赛的获胜者将获得 LyricNote 销售的音乐软件产品。图 12-2 显示了输入表单。

<sup>2</sup> *MIDI（乐器数字接口）*使用一种文件格式，其中描述了音符而非实际录制。它们的内容由兼容 MIDI 的乐器或媒体播放器重新创建。

## 278 JSP：完整参考

以下 HTML 生成该表单：

```html
<form method="post"
        action="http://u25nv/lyricnote/servlet/midi_contest"
        enctype="multipart/form-data"
        >
<table border="0" cellpadding="3" cellspacing=0>
    <tr valign="top">
        <td colspan="2">
            Are you a budding composer?
            Submit a MIDI file of your own composition
            for a chance to win a copy of <B>ScoreWriter 4.5</B>.
            Click
            <A HREF="product/midi_contest/rules.html">here</A>
            for official rules.
        </td>
    </tr>

    <tr valign="top">
        <td>Your name:</td>
        <td><input name="name" type="text" size=32></td>
    </tr>

    <tr valign="top">
        <td>Your e-mail:</td>
        <td><input name="email" type="text" size=20></td>
    </tr>

    <tr valign="top">
        <td>Title of composition:</td>
        <td><input name="title" type="text" size=48></td>
    </tr>

    <tr valign="top">
        <td>MIDI file name:</td>
        <td><input type="file" name="midifile" size=32></td>
    </tr>

    <tr valign="top">
        <td>&nbsp;</td>
        <td>
            <input type="submit" value="Send">
            <input type="reset" value="Clear">
        </td>
    </tr>

</table>
</form>
```

当表单提交时，浏览器会生成一个包含 multipart/form-data 格式数据流的 HTTP 请求，其中部分包含以下内容：

```
Content-Type: multipart/form-data;
    boundary=-----------------------------7d01012174012c
Content-Length: 1507

------------------------------7d01012174012c
Content-Disposition: form-data; name="name"

S. Vetter
------------------------------7d01012174012c
Content-Disposition: form-data; name="email"

vetter@lyricnote.com
------------------------------7d01012174012c
Content-Disposition: form-data; name="title"

It-B-Gone
------------------------------7d01012174012c
Content-Disposition: form-data; name="midifile";
    filename="C:\my_midi_files\Itbgon.mid"
Content-Type: audio/mid

MThd... (binary data not shown)
------------------------------7d01012174012c--
```

我们可以看到四个输入字段都存在，每个都在由边界字符串分隔的独立块中。每个块都有一个 Content-Disposition 头，用于指定字段名。最后一个包含上传文件的块，其 Content-Disposition 头上还有一个 filename 属性，给出客户端系统上的原始文件名，以及一个 Content-Type 头，指示文件数据是名为 audio/mid 的二进制格式。服务器程序可以解析数据流并提取字段值和文件内容。

![](img/7a2f73369bb140583c7288b73456addb_306_0.png)

**图 12-2.** 包含文件上传输入字段的表单

## 隐藏

并非所有输入都来自用户，至少不是直接来自。某些表单可能使用硬编码或动态生成的常量。type="hidden" 的 INPUT 元素可用于此目的。其语法如下所示：

```
<INPUT
    type="hidden"
    name="name"
    value="value">
```

其属性含义如下：

-   **type="hidden"** 表示这是一个隐藏控件。
-   **name="name"** 指定脚本可以引用此控件的名称。这也是服务器程序可以用来检索该文本的名称。
-   **value="value"** 必须用于分配一个初始文本值。

正如你可能猜到的，隐藏字段没有可视表示。其唯一目的是创建一个具有常量值的参数。这可能是某种事务代码，分派 servlet 会将其用作其他类表的键。但更常见的情况是，隐藏字段的值是由创建 HTML 的 servlet 或 JSP 页面动态生成的。例如，

```
<input type="hidden" name="remoteHost"
       value="<%= request.getRemoteHost() %>">

<input type="hidden" name="userAgent"
       value="<%= request.getHeader("user-agent") %>">
```

将存储运行 Web 浏览器的 IP 地址或主机名以及标识浏览器软件和版本号的字符串，作为表单中的隐藏字段。这些字段可能对处理表单问题的技术支持人员有用。

## 图像

*图像*可以用作输入字段，用户通过鼠标点击而不是键盘输入。在这种情况下，信息是图像内鼠标点击的位置。*图像*输入类型可用于此目的。其语法如下所示：

```
<INPUT
       type="image"
       name="name"
       src="imageurl">
```

其属性含义如下：

-   **type="image"** 表示这是一个图像控件。
-   **name="name"** 指定脚本可以引用此控件的名称。这也是服务器程序可以用来检索鼠标点击位置的名称。
-   **src="imageurl"** 是图像文件的 URL。

对于图像控件，数据流中会创建两个参数，分别对应点击的 *x* 和 *y* 坐标。坐标以像素为单位给出，相对于图像的左上角 (0, 0)。参数名由图像控件名称加上 ".x" 或 ".y" 组成。例如，



## 按钮

除了提交和重置按钮外，还存在一种通用的按钮输入类型。其语法如下所示，

```
<INPUT
    type="button"
    name="name"
    value="value">
```

其属性定义如下：

- **type="button"** 指示这是一个按钮控件。
- **name="name"** 指定一个名称，脚本可以通过该名称引用此按钮。
- **value="value"** 指定显示在此按钮上的值。

为了使此控件有用，必须定义 `onclick` 事件处理程序属性。然后，JavaScript 函数就可以通过按钮的名称和值来引用它。

## 由 select 和 option 创建的元素

`select` 和 `option` 标签可以一起使用，以创建一个可滚动的菜单项列表。参考图 12-1 中的客户反馈示例，用户从一个下拉列表中选择表单的目的地。用于创建此列表的 HTML 如下所示：

```
<select name="to" size=1>
    <option value="CS">Customer Service
    <option value="EX">Executive
    <option value="FI">Finance
    <option value="HR">Human Resources
    <option value="IT">Information Technology
    <option value="MK">Marketing
    <option value="FA">Facilities
    <option value="PC">Purchasing
    <option value="SP">Shipping
</select>
```

`select` 标签的语法如下所示，

```
<select name="name" size="number" multiple> options </select>
```

其中属性含义如下：

- **name="name"** 分配一个名称，服务器程序可以通过该名称引用该列表。
- **size="number"** 指示一次可见的元素数量；即列表框的高度。如果数字为 1，则该列表是一个下拉菜单。
- **multiple**，如果指定，则允许用户选择多个项目。

请注意，`<select>` 标签必须用 `</select>` 关闭。

`select` 列表的核心是一组带有相关值和描述的 `option` 标签。通常，此类列表是从数据库查询动态生成的。`option` 标签具有以下语法，

```
<option value="value" selected> text </option>
```

其中

- **value="value"** 指定如果选中此项目，则随表单返回的值。如果未指定此属性，则返回 option 标签的主体内容。
- **selected**，如果存在，则预选该项目。

开始和结束标签之间的文本（称为 *主体*）是实际显示在列表框中的内容。结束 `</option>` 标签不是必需的，并且经常被省略。当表单提交时，所选项目的值是与 `select` 元素关联的值。在前面的示例中，如果用户选择了列表中的最后一项，则数据流中返回的值将是：

```
to=SP
```

如果在 `<select>` 标签上指定了 `multiple` 属性，并且用户选择了多个项目，则参数名会在数据流中多次出现并与不同的值关联。因此，如果用户不仅选择了运输部门，还选择了财务和市场部门，数据流将如下所示：

```
to=FI&to=MK&to=SP
```

## textarea 元素

`text` 和 `password` 输入字段仅支持单行，而 `textarea` 元素可以接受多行。这使得 `textarea` 元素适用于输入评论或其他可能超过一行的自由格式文本。可以指定高度和宽度，浏览器会根据需要添加滚动条。`textarea` 的语法如下，

```
<textarea name="name" rows="number" cols="number">
... text ...
</textarea>
```

其中

- **name="name"** 分配此字段在脚本和服务器程序中已知的名称。
- **rows="number"** 指定文本区域可见高度的行数。这*不是*列表框中实际行数的限制，它只是列表滚动时一次显示的行数限制。
- **cols="number"** 指定文本区域可见宽度的字符数。这*不是*列表框中实际列数的限制，只是其显示宽度。

## 表单验证

用户界面编程本质上是复杂的。专门用于验证输入字段的代码量通常大于执行实际功能的代码量。必须检查必填字段以确保它们非空，并且可选字段必须分配默认值。所有字段可能都需要根据一组可接受的值或算法进行验证。某些字段的有效性可能取决于其他字段的值。

所有这些验证都可以由服务器程序完成，但来回的网络流量可能会在响应时间方面使其代价过高。因此，最好使用脚本语言（如 JavaScript）在客户端进行验证。有各种各样的 JavaScript 书籍可用，因此我不会详细介绍 JavaScript 的工作原理，只会提供一个完整的示例。

## 带验证的联系我们表单

让我们为图 12-1 中所示的“联系我们”表单示例添加一些最基本的验证。你需要做三件事。

### 设置触发器

首先，你需要强制在提交表单时执行一些代码。为此，请在表单标签中设置 `onsubmit` 属性：

```
<form method="post"
      action="diag/ShowParms.jsp"
      onsubmit="return validate(this);">
```

在 onsubmit 属性中指定的字符串会在表单提交前进行求值。只有当它求值为 `true` 时，表单才会被实际提交。原则上，验证代码可以直接作为 `onsubmit` 属性值输入，但调用一个函数并返回其值会更简单。随着验证要求的变化，这也使得添加新代码更容易。

### 添加脚本块

要将 JavaScript 语句合并到你生成的 HTML 中，必须将它们包含在 `<SCRIPT>` ... `</SCRIPT>` 标签中。为确保这些标签已加载并求值，最好将它们放在 HTML 的 `<HEAD>` ... `</HEAD>` 部分。

### 编写验证函数

第三步是编写验证函数本身：

```
function validate(frm) {
    if (!hasData(frm.from.value)) {
        alert("Please type your name in the 'From:' box");
        return false;
    }
    return true;
}

function hasData(s) {
    if (s == null)
        return false;
    var n = s.length;
    for (var i = 0; i < n; i++) {
        var c = s.charAt(i);
        switch (c) {
            case ' ':
            case '\t':
            case '\n':
                continue;
            default:
                return true;
        }
    }
    return false;
}
```

这里展示了两个函数：

- **validate(frm)** 给定表单的引用，执行所有必要的验证，如果没有发现错误则返回 true。
- **hasData(s)** 一个实用函数，如果指定的字符串至少有一个非空白字符，则返回 true。

你唯一能真正验证的字段是用户名。在这个例子中，你只需验证它非空。如果用户没有在该字段中输入任何内容，结果将如图 12-3 所示。

## 表单处理的服务器端

服务器端处理表单有多种模型。第 19 章中的案例研究将深入探讨这个问题。为了说明目的，你开发了一个简单的 JSP 页面，该页面仅收集请求参数并将其格式化为



## 概要

HTML 表单提供了一个易于用户操作且便于服务器程序处理的图形用户界面环境。表单包含用于文本输入、菜单选择和布尔选择的控件，例如复选框和单选按钮。通过替代的编码类型，表单可以支持文件上传的客户端部分。隐藏字段中可以指定常量值。表单可以使用用 JavaScript 编写的客户端函数进行验证，这节省了网络传输和处理时间。服务器程序，无论是 JSP 页面还是 Servlet，都可以使用 Servlet API 来检索参数名和值，并将结果返回给提交表单的浏览器。

## 第 13 章

## 数据库访问

## JDBC 概述

JDBC 是 Java 程序和数据库管理系统之间的应用程序编程接口。类似于 Oracle 的 *Oracle 调用接口 (OCI)* 或 Microsoft 的 *开放数据库连接 (ODBC)*，JDBC 是一个调用级接口。这意味着程序使用方法或函数调用来访问其功能，这与由预编译器转换的嵌入式 SQL 语句相反。

程序员使用称为 *JDBC 驱动程序* 的 Java 类连接到数据库。存在数百种 JDBC 驱动程序——对于每种广泛使用的数据库（无论是商业软件还是共享软件）至少有一个。一种特殊的 JDBC 驱动程序，称为 *JDBC-ODBC 桥接器*，使得使用 ODBC 作为中间件成为可能，从而使大量 ODBC 驱动程序可以从 JDBC 使用。

JDBC 的巨大优势在于它为所有数据库管理系统提供了标准接口。在 Oracle 数据库上运行的 JDBC 查询，只需很少或无需更改即可在 DB2、SQL Server 或任何其他数据库上工作。剩下的少数差异通常与数据类型名称和对某些操作类型的支持有关。通常，甚至这些差异也可以使用 JDBC 连接提供的元数据以编程方式解决。

JDBC 还简化了从旧系统到支持 Web 的应用程序的过渡。自 1980 年代初以来就存在的嵌入式 SQL 产品，大部分使用的 SQL 语句和操作都可以由 JDBC 调用复制。在批处理大型机 COBOL 应用程序中，SQL 语句的语法和语义在将应用程序转换为 Java 时几乎不需要更改。

## 基本的 JDBC 操作

使用 JDBC 并不困难。根据要执行的任务，通常只需要四个步骤：

1.  为你的 DBMS 加载一个 JDBC 驱动程序。这通常只需要一个指定驱动程序类名的 `Class.forName()` 语句。
2.  使用该驱动程序打开到特定数据库的连接。这是通过调用 `DriverManager` 类的静态 `getConnection(url)` 方法完成的。`url` 参数采用特定形式，指示驱动程序类型和要使用的数据源。
3.  通过连接发布 SQL 语句。一旦连接建立，就可以用它来创建 `Statement` 对象，通过这些对象可以发出 SQL 命令。
4.  处理 SQL 操作返回的结果集。`ResultSet` 接口提供了逐步遍历每一行并获取每列值的方法。

图 13-1 说明了这四个步骤。
在 JDBC 2.0 中，灵活性更高了。使用 *Java 命名和目录接口 (JNDI)*，应用程序可以通过名称从命名服务中查找 `DataSource` 对象，而不是硬编码驱动程序类名和数据库 URL。此外，JDBC 2.0 的结果集具有更多功能。它们可以按随机顺序访问，而不是从头到尾顺序访问。它们可以被更新，并且更新可以传播回基础表。它们还可以动态链接到其基础表，以便其中的更改同时反映在结果集中。图 13-2 展示了 JDBC 2.0 数据库访问涉及的基本步骤。

## 基本的 JDBC 类

JDBC 接口包含在 `java.sql` 和 `javax.sql` 包中。它主要由接口而非具体类组成，因为每个供应商的实现都特定于其特定的数据库协议。`java.sql` 中的核心 API 由 16 个接口、8 个类和 4 个异常类型组成。可选包 API 添加了另外 12 个接口和 2 个类。其中许多类主要对 JDBC 驱动程序开发人员有兴趣。其中更常用的一个子集概述如下：

- **Connection** 一个到数据库的活动链接，Java 程序可以通过它读写数据，以及探索数据库结构和功能。

    Connection 对象通过调用 DriverManager.getConnection() 或 JDBC 2.0 中的 DataSource.getConnection() 创建。

- **Statement** 一个允许通过连接发送 SQL 语句并检索它们产生的结果集和更新计数的对象。
    存在三种类型的语句，每种都是其前一种的特化：
    - **Statement** 用于执行静态 SQL 字符串。使用 Connection.createStatement() 创建。
    - **PreparedStatement** Statement 的扩展，使用预编译的 SQL，可能包含动态设置的输入参数。PreparedStatement 对象通常在循环中与 SQL 插入操作一起使用。使用 Connection.prepareStatement(sqlstring) 创建。
    - **CallableStatement** 一个调用存储过程的 PreparedStatement。并非所有数据库管理系统都支持存储过程，但对于支持的系统，CallableStatement 提供了标准的调用语法。



# JSP：完整参考手册

-   **ResultSet**：由SQL查询或调用某些元数据函数产生的有序表格行集合。`ResultSet`最常作为`Statement.executeQuery(sqlstring)`方法调用的返回值遇到。JDBC API提供了`next()`方法用于遍历`ResultSet`的行，以及`getXXX()`方法用于提取列值，其中`XXX`是Java数据类型。JDBC 2.0添加了许多用于随机访问和更新行的方法。
-   **DatabaseMetaData**：一个包含众多方法的接口，这些方法提供关于数据库结构和能力的信息。`DatabaseMetaData`对象由`Connection`对象的`getMetaData()`方法返回。
-   **ResultSetMetaData**：一个描述`ResultSet`列的接口。可以通过调用结果集的`getMetaData()`方法获得。它包含描述列数以及每列名称、显示大小、数据类型和类名的方法。
-   **DriverManager**：一个注册JDBC驱动程序并提供能够处理特定JDBC URL连接的接口。唯一常用的方法是静态的`DriverManager.getConnection()`，它有三种形式，返回一个绑定到指定JDBC URL的活动`Connection`对象。
-   **SQLException**：JDBC API使用的基础异常类。`SQLException`具有可以提供`SQLState`值和任何供应商特定错误代码的方法。如果发生多个异常，它还可以链接到另一个`SQLException`。

JDBC API的一个既定目标是它应该简单且易于掌握。学习这七个类及其三到四个主要方法可以在几天内轻松完成，这使得JDBC成为一项流行且广为接受的技术。

# 一个简单的JSP示例

让我们考虑一个在JSP页面中使用JDBC的示例。我们假设的LyricNote公司维护着一个内部员工数据库，其中包含两个表：`departments`和`employees`。这些表是用以下SQL创建的：

```
CREATE TABLE departments (
    deptno      char(2),
    deptname    char(40),
    deptmgr    char(4)
)
```

和

```
CREATE TABLE employees (
    deptno      char(2),
    empno       char(4),
    lname       char(20),
    fname       char(20),
    hiredate    date,
    ismgr       bit,
    deptno      char(2),
    title       char(50),
    email       char(32),
    phone       char(4)
)
```

我们的示例JSP页面显示一个部门列表，标明其经理的姓名、职位、电话号码和电子邮件地址。用于组合此列表的SQL如下所示：

```
SELECT   D.deptname, E.fname, E.lname, E.title, E.email, E.phone
FROM     departments D, employees E
WHERE    D.deptmgr = E.empno
ORDER BY D.deptname
```

D和E前缀是用于限定列名的伪表名，以便DBMS可以区分哪个表提供了哪个列。

完整的JSP源代码如下

```
<%@ page session="false" %>
<%@ page import="java.sql.*" %>
<%@ page import="java.util.*" %>

<HTML>
<HEAD>
<TITLE>Department Managers</TITLE>
</HEAD>
<BODY>
<img src="images/lyric_note.png" border=0><p>
<hr color="#000000">
<H2>Department Managers</H2>
<%
String DRIVER = "org.enhydra.instantdb.jdbc.idbDriver";
String URL =
    "jdbc:idb:d:/lyricnote/WEB-INF/database/internal/db.prp";

// 打开数据库连接

Class.forName(DRIVER);
Connection con = null;
try {

    con = DriverManager.getConnection(URL);

    // 获取部门经理信息

    String sql = ""
        + " SELECT    D.deptname, E.fname, E.lname,"
        + "           E.title, E.email, E.phone"
        + " FROM      departments D, employees E"
        + " WHERE     D.deptmgr = E.empno"
        + " ORDER BY  D.deptname"
        + ";"

    Statement stmt = con.createStatement();
    ResultSet rs = stmt.executeQuery(sql);
%>
<DL>
<%
    while (rs.next()) {
        String dept  = rs.getString(1);
        String fname = rs.getString(2);
        String lname = rs.getString(3);
        String title = rs.getString(4);
        String email = rs.getString(5);
        String phone = rs.getString(6);
%>
<DT><B><%= dept %></B></DT>
<DD>
    <%= fname %> <%= lname %>, <%= title %><BR>
    (919) 555-0822 x<%= phone %>, <%= email %>
</DD>
<%
    }
rs.close();
rs = null;

stmt.close();
stmt = null;
}
finally {
    if (con != null) {
        con.close();
    }
}
%>
</DL>
</BODY>
</HTML>
```

让我们逐一检查每个部分。
首先，有三个页面指令

```
<%@ page session="false" %>
<%@ page import="java.sql.*" %>
<%@ page import="java.util.*" %>
```

我们明确请求不创建HTTP会话。这应在所有不需要访问会话的JSP页面中完成，因为它节省了建立和维护会话所需的服务器资源。
在创建页面标题的HTML之后，一个脚本段查询LyricNote内部数据库并显示结果。它以两个字符串常量的声明开始，定义JDBC驱动程序名称和数据库URL。为方便起见，将这些信息隔离在声明部分以便于修改：

```
String DRIVER = "org.enhydra.instantdb.jdbc.idbDriver";
String URL = "jdbc:idb:d:/lyricnote/WEB-INF/database/internal/db.prp";
```

此示例使用InstantDB<sup>4</sup>数据库并连接到LyricNote内部数据库，其属性文件为db.prp。

> 4 *InstantDB*是一个免费的、纯Java的关系型DBMS，可从http://instantdb.enhydra.org/index.html获取。InstantDB具有许多高级特性并支持JDBC 2.0。

实际工作从下一条语句开始：

```
Class.forName(DRIVER);
Connection con = null;
try {
    con = DriverManager.getConnection(URL);
```

Class.forName()调用导致JDBC驱动程序类被加载。根据JDBC规范，驱动程序应包含一个静态初始化部分，该部分创建实例并注册到驱动程序管理器。一些较旧的驱动程序未能做到这一点，在这种情况下，需要调用驱动程序类的newInstance()方法。DriverManager类通过其静态getConnection()方法的调用提供实际的连接。

请注意，持有连接引用的con变量被声明并赋值为null值。然后页面的其余部分包含在try { ... }块中，后面跟着

```
finally {
    if (con != null) {
        con.close();
    }
}
```

这样做的原因是，一旦打开，连接就需要关闭，无论是否发生任何错误或抛出异常。这可以通过finally { ... }块来保证。包含catch块是不必要的；在我们的例子中，默认的异常处理程序已经足够好。

一旦连接建立，就可以运行SQL查询了。为此，我们调用Connection对象的createStatement()方法来获得Statement对象，然后可以调用它的executeQuery()方法。

```
String sql = ""
    + " SELECT D.deptname, E.fname, E.lname,"
    + "       E.title, E.email, E.phone"
    + " FROM   departments D, employees E"
    + " WHERE  D.deptmgr = E.empno"
    + " ORDER BY D.deptname"
    ;

Statement stmt = con.createStatement();
ResultSet rs = stmt.executeQuery(sql);
```

executeQuery()返回一个ResultSet。我们的代码通过在一个循环中调用其next()方法来简单读取此集合的每一行：

```
while (rs.next()) {
    String dept = rs.getString(1);
    String fname = rs.getString(2);
    String lname = rs.getString(3);
    String title = rs.getString(4);
    String email = rs.getString(5);
    String phone = rs.getString(6);
}
%>
<DT><B><%= dept %></B></DT>
<DD>
    <%= fname %> <%= lname %>, <%= title %><BR>
    (919) 555-0822 x<%= phone %>, <%= email %>
</DD>
<%
}
```

在循环内部，我们使用ResultSet.getString(columnNumber)方法提取每一列的值，然后格式化并打印部门名称、经理姓名、职位、电话号码和电子邮件行。
最后，我们关闭所有创建的JDBC对象，并将它们的引用设置为null，以便它们可以被垃圾回收。

```
rs.close();
rs = null;

stmt.close();
stmt = null;
```

Connection对象在前面讨论的finally { ... }块中关闭。
最终成品如图13-3所示。

# JDBC驱动程序

为了将程序与特定数据库协议的细节隔离开来，JDBC使用了一个由DriverManager类和一个或多个JDBC驱动程序组成的中间层。*驱动程序*是一个Java类，通常由数据库供应商提供，它实现了`java.sql.Driver`接口。驱动程序的主要功能是连接到数据库并返回一个`java.sql.Connection`对象。



![](img/7a2f73369bb140583c7288b73456addb_328_0.png)

**图 13-3.** 简单的 JDBC 示例的输出

应用程序不会直接调用驱动程序。相反，它们会注册到驱动程序管理器中，由该管理器确定适用于特定连接请求的驱动程序，并通过它进行连接。目前有数百种 JDBC 驱动程序，几乎覆盖了所有的数据库管理系统。其中大多数都可以从供应商网站下载。一个可搜索的列表可以在 http://industry.java.sun.com/products/jdbc/drivers 找到。下一节将讨论四种 JDBC 驱动程序类型、JDBC-ODBC 桥接这一特殊情况，以及注册驱动程序的机制。

## 驱动程序类型

JDBC 规范根据驱动程序的架构将其分为四种类型。这些类型是：

- **类型 1——JDBC-ODBC 桥接** 此类驱动程序通过中间 ODBC 驱动程序连接到数据库。这种方法涉及几个缺点，因此 Sun 将其描述为实验性的，仅在没有其他驱动程序可用时使用。Microsoft 和 Sun 都提供类型 1 驱动程序。
- **类型 2——部分为 Java 的本机 API** 类似于 JDBC-ODBC 桥接，类型 2 驱动程序使用本机方法调用供应商特定的 API 函数。这些驱动程序也受到与 JDBC-ODBC 桥接相同的限制，即它们需要在客户端系统上安装本机库文件，并且必须进行配置才能使用。
- **类型 3——纯 Java 到数据库中间件** 类型 3 驱动程序使用网络协议与中间件服务器通信，而中间件服务器又与一个或多个数据库管理系统通信。
- **类型 4——纯 Java 直接到数据库** 此类驱动程序直接调用数据库管理系统使用的本机协议。

四种驱动程序类型的架构如图 13-4 所示。

驱动程序类型有什么区别？从应用程序程序员的角度来看，区别不大。这些分类对系统架构师的意义更大。类型 1 和类型 2 驱动程序要求在客户端系统上安装和配置本机代码。如果 DBMS 位于防火墙之后，类型 4 驱动程序可能不适用。同样，四种驱动程序类型各有其性能特点，但应用程序编程接口在所有四种情况下都完全相同。

## JDBC-ODBC 桥接

类型 1 的 JDBC-ODBC 桥接驱动程序需要特别考虑。正如我们所看到的，使用它涉及几个问题。首先，JDBC-ODBC 桥接驱动程序受限于底层 ODBC 驱动程序的功能，而后者是单线程的，因此在高负载下性能可能不佳。此外，它需要在客户端系统上安装本机代码库 `JdbcOdbc.dll`。最后，要发挥任何作用，JDBC-ODBC 桥接驱动程序都需要配置一个 ODBC 数据源。这些限制使其不适合用于外部互联网上的小程序。Sun 建议，只有在没有其他 JDBC 驱动程序可用的情况下，才应出于实验目的使用桥接。

![](img/7a2f73369bb140583c7288b73456addb_330_0.png)

另一方面，JDBC-ODBC 桥接提供了几个显著的优势。由于 JSP 页面不在小程序环境中运行，因此它们没有这些限制。ODBC 得到了广泛支持，因此使用桥接可以访问各种已配置数据源的现有系统。同样，支持 ODBC 的数据库产品，如 Microsoft Access 和 FoxBase，也广泛可用。这些特性使 JDBC-ODBC 桥接成为低流量 Web 应用程序的良好选择，并且是学习 JDBC 的有用工具。

要在 Java 应用程序中使用 JDBC-ODBC 桥接，必须配置一个合适的 ODBC 数据源。在 Windows 系统上，这通过控制面板 ODBC 数据源应用程序完成。数据源应配置为系统 DSN，而不是用户 DSN，因为 JSP 引擎通常在系统用户配置文件下运行。如果使用的是 Sun JVM，则驱动程序类名为 `sun.jdbc.odbc.JdbcOdbcDriver`；如果使用的是 Microsoft 虚拟机，则为 `com.ms.jdbc.odbc.JdbcOdbcDriver`。在 `getConnection()` 语句中使用的数据库 URL 是 `jdbc:odbc:dsn`，其中 `dsn` 是数据源名称。

Microsoft 为其 Access 数据库产品以及 dBase、Excel、FoxPro 和许多其他产品（包括一个可以将普通文本文件（.txt 和 .csv）用作简单数据库系统的文本驱动程序）提供 ODBC 驱动程序。

## 注册驱动程序

要使用 JDBC 驱动程序，必须首先将其注册到驱动程序管理器。你可以通过几种方式完成此操作，但每种方式都涉及调用 `DriverManager.registerDriver()`。最常见的方法是简单地加载驱动程序类：

```
try {
    Class.forName("MyJdbcDriver");
} catch (ClassNotFoundException e) {
    // 报告异常
}
```

以此方式加载的驱动程序类应创建自身的实例并使用类似以下逻辑将其注册到驱动程序管理器：

```
static {
    PrintStream log = DriverManager.getLogStream();
    if (log != null)
        log.println("MyJdbcDriver class loaded");
    MyJdbcDriver driver = new MyJdbcDriver();
    try {
        DriverManager.registerDriver(driver);
    }
    catch (SQLException e) {
        if (log != null)
            log.println("Unable to register driver");
    }
}
```

一些已知的旧驱动程序省略了此步骤，而是在其构造函数中进行注册。在这种情况下，需要使用以下方法创建驱动程序的实例[^5]：

```
try {
    Class.forName("MyJdbcDriver");
}
catch (ClassNotFoundException e) {
    // 报告异常
}
catch (InstantiationException e) {
    // 报告异常
}
catch (IllegalAccessException e) {
    // 报告异常
}
```

驱动程序注册的另一种方法是将驱动程序名称放在 `jdbc.drivers` 系统属性中。这是一个以冒号分隔的驱动程序类名列表，`DriverManager` 在其初始化期间加载。例如，使用此方法的独立 Java 应用程序可以如下调用：

```
java -Djdbc.drivers=org.enhydra.instantdb.jdbc.idbDriver MyPGM
```

一些 JDBC 驱动程序供应商，特别是 Oracle，建议显式创建驱动程序的实例并将其注册到驱动程序管理器：

```
DriverManager.registerDriver(
    new oracle.jdbc.driver.OracleDriver());
```

JDBC 2.0 允许通过注册到 JNDI 服务提供程序的 `DataSource` 对象建立连接。例如，JRun 3.0 提供了一种在 Web 服务器级别定义 JDBC 数据源的方法，以及一个用于连接性的快速在线测试。这种方法的优势在于驱动程序类名和数据库 URL 存储在命名服务中，而不是硬编码在应用程序程序中。只需要数据源名称。本章前面与图 13-3 相关的示例 JSP 页面可以将连接逻辑替换为以下内容：

```
InitialContext ctx = new InitialContext();
DataSource ds = (DataSource) ctx.lookup
    ("java:comp/env/jdbc/lyricnote_internal");

Connection con = null;
try {
    con = ds.getConnection();
    ...
}
finally {
    if (con != null)
        con.close();
}
```

> 注意：使用 `DataSource` 进行 JDBC 连接的 JSP 页面必须导入 `javax.sql.*` 和 `javax.naming.*`，否则必须完全限定对 `InitialContext` 和 `DataSource` 的引用。

使用 `DataSource` 的另一个优势是，其他高级数据库功能（如连接池和分布式事务）可以完全通过更改命名服务中的绑定来实现。无需更改 JSP 源代码。

## 连接到数据库

驱动程序加载并注册后，即可用于创建数据库连接。`DriverManager` 提供了三种方法来执行此操作：

- getConnection(String *url*)
- getConnection(String *url*, String *userID*, String *password*)
- getConnection(String *url*, Properties *prop*)

在内部，`DriverManager` 使用相同的私有工作方法来处理这些方法中的每一个。

驱动程序管理器维护一个已注册驱动程序的列表。当调用其 `getConnection()` 方法时，它会依次查询每个驱动程序，以查看其是否接受指定的 URL。驱动程序管理器通过调用驱动程序的 `connect()` 方法来执行此操作，该方法返回 `null`（如果驱动程序无法接受 URL）或一个活动的 `Connection` 对象（如果它可以）。

如前所述，JDBC 2.0 允许使用 `DataSource` 而不是 `DriverManager` 来建立连接。在这种情况下，不使用 URL 参数，因为它存储在命名服务中。

[^5]: 这是一个繁琐的解决方法，不是吗？你可以简单地捕获 `Exception` 本身，但这总是会让你面临对未预料到的异常应用错误逻辑的风险。



# JDBC 数据库 URL

`DriverManager.getConnection()` 的关键参数是 `JDBC URL`，它是一个包含三个部分的字符串，各部分由分号分隔：

```
<protocol>:<subprotocol>:<subname>
```

其中

- `protocol` 始终为 jdbc。
- `subprotocol` 是一个特定于供应商的字符串，用于标识要使用的驱动程序。驱动程序在被驱动程序管理器询问时，会表明它是否能够处理该子协议。例如，JDBC-ODBC 桥接驱动程序使用保留值 `odbc` 作为其子协议。此值在所有驱动程序供应商中应是唯一的。Sun Microsystems 作为 JDBC 子协议的非正式注册管理机构。
- `subname` 标识要连接到的具体数据库。此字符串包含驱动程序识别数据库所需的任何信息。它也可能包含数据库所需的连接参数。

JDBC URL 的示例如下：

```
jdbc:odbc:usda
```

这表示一个名为 `usda` 的 ODBC 数据源，通过 JDBC-ODBC 桥接驱动程序进行访问。

```
jdbc:idb:c:/path/database.prp
```

InstantDB 将 `subname` 解释为一个属性文件，该文件描述了数据库的位置和特性。

```
jdbc:oracle:thin:@(DESCRIPTION=(ADDRESS=(HOST=u25nv)(PROTOCOL=tcp)(PORT=4311))(CONNECT_DATA=(SID=music)))
```

这是一个较长的连接字符串，可能与 Oracle 瘦客户端驱动程序一起使用。

与驱动程序注册的情况类似，JDBC 2.0 使得可以使用命名服务中的 `DataSource` 来隐藏 JDBC URL 的细节。

# Statement 接口

SQL 语言由创建、操作和从关系数据库中提取数据的语句组成。JDBC 为这些 SQL 语句提供了一个面向对象的表示，封装了它们的文本、执行状态和结果。毫不奇怪，这种表示被称为 `java.sql.Statement` 接口。Statement 对象将 SQL 命令发送到数据库，这些命令可以是以下任何类型：

- 数据定义命令，如 CREATE TABLE 或 CREATE INDEX
- 数据操作命令，如 INSERT 或 UPDATE
- 用于执行查询的 SELECT 语句

数据操作命令返回受影响的行数，而 SELECT 语句返回一组行，称为结果集。

`Statement` 接口有两个专门的子接口，扩展了其功能：`PreparedStatement`，使用预编译的 SQL；以及 `CallableStatement`，用于调用存储过程。下一节将讨论这三种语句类型及其使用方法。

# Statement

基础接口是 `java.sql.Statement`。由于这是一个接口，它没有构造函数；相反，它是通过连接对象使用 `Connection.createStatement()` 获得的。以下是一个典型的示例：

```
Connection con = null;
try {
    con = DriverManager.getConnection(URL);
    Statement stmt = con.createStatement();
    ...
    stmt.close();
}
finally {
    if (con != null)
        con.close();
}
```

JDBC 2.0 引入了一种额外的 `createStatement()` 形式，它接受参数来指示其结果集是否应该是可滚动的，以及是否反映底层表的并发更改。本章后面关于结果集的部分将更详细地描述这些功能。

一旦创建了语句，就可以用它来执行命令。有四种方法可以做到这一点：`executeUpdate`、`executeQuery`、`execute` 和 `executeBatch`。选择使用哪种方法取决于预期的结果：

- `executeUpdate` 旨在与 SQL `INSERT`、`UPDATE` 或 `DELETE` 语句一起使用，或与数据定义语句（如 `CREATE TABLE`）一起使用。它返回更新的行数。
- `executeQuery` 用于执行 SQL `SELECT` 语句并返回结果集。
- `execute` 可用于任一目的，但它专为那些可能返回更新计数、多个结果集或某些组合的语句而设计。它返回一个布尔标志，指示其结果是更新计数还是结果集。还有其他方法可用于遍历结果。
- `executeBatch` 允许以批处理方式执行多个更新语句。更新计数以数组形式返回。

以下示例说明了每种方法。

# executeUpdate 方法

在此示例中，通过 `executeUpdate` 方法调用 SQL `UPDATE` 语句来纠正错误的产品描述。

```
import java.sql.*;

public class UpdateExample
{
    public static void main(String[] args)
        throws ClassNotFoundException, SQLException
    {
        String DRIVER = "org.enhydra.instantdb.jdbc.idbDriver";
        String URL = "jdbc:idb:"
            + "D:/lyricnote/WEB-INF/database/products/db.prp";

        Class.forName(DRIVER);
        Connection con = null;
        try {
            con = DriverManager.getConnection(URL);
            Statement stmt = con.createStatement();
            int nRows = stmt.executeUpdate(
                "UPDATE products"
                + " SET description ="
                + " 'Telemann: Concerto No. 1 in F for Two Horns'"
                + " WHERE itemcode = '022370'"
            );
            System.out.println(nRows + " rows updated");
            stmt.close();
        }
        finally {
            if (con != null)
                con.close();
        }
    }
}
```

成功执行后，程序会打印“1 rows updated”。

# executeQuery 方法

为了查看错误的条目已被纠正，此示例使用 SELECT 语句来显示产品目录中所有是泰勒曼协奏曲的乐谱标题：

```
import java.sql.*;

public class QueryExample
{
    public static void main(String[] args)
        throws ClassNotFoundException, SQLException
    {
        String DRIVER = "org.enhydra.instantdb.jdbc.idbDriver";
        String URL = "jdbc:idb:"
            + "D:/lyricnote/WEB-INF/database/products/db.prp";

        Class.forName(DRIVER);
        Connection con = null;
        try {
            con = DriverManager.getConnection(URL);
            Statement stmt = con.createStatement();
            ResultSet rs = stmt.executeQuery(
                " SELECT itemcode, description"
                + " FROM products"
                + " WHERE prodtype = 'SM'"
                + " AND description like 'Telemann%'"
                + " AND description like '%Concerto%'"
            );
            while (rs.next()) {
                String itemCode = rs.getString(1);
                String description = rs.getString(2);
                System.out.println(itemCode + " " + description);
            }
            rs.close();
            stmt.close();
        }
        finally {
            if (con != null)
                con.close();
        }
    }
}
```

运行时，它会产生更正后的输出：

```
022340 Telemann: Double Viola Concerto in G
022350 Telemann: Viola Concerto in G
022360 Telemann: Concerto for Horn Quartet
022370 Telemann: Concerto No. 1 in F for Two Horns
```

从结果集中获取值的过程将在本章后面解释。

# execute 方法

虽然 execute 方法可用于查询或更新，但它严格来说仅对于可能返回多个结果的操作是必要的。Statement 接口提供了用于确定返回了什么以及处理结果的方法。execute 最常见的用途是处理未知的 SQL 字符串，例如在此示例中，它从文件中读取并处理 SQL 语句：

```
import java.io.*;
import java.sql.*;

public class ExecuteExample
{
    public static void main(String[] args)
        throws ClassNotFoundException, SQLException, IOException
    {
        String DRIVER = "org.enhydra.instantdb.jdbc.idbDriver";
        String URL = "jdbc:idb:"
            + "D:/lyricnote/WEB-INF/database/products/db.prp";

        Class.forName(DRIVER);
        Connection con = null;
        try {
            con = DriverManager.getConnection(URL);
            Statement stmt = con.createStatement();

            // Read SQL statements from a file
            BufferedReader in =
                new BufferedReader(
                    new FileReader("executeExample.sql"));

            while (true) {
                String line = in.readLine();
                if (line == null)
                    break;

                // Execute statement
                boolean hasResultSet = stmt.execute(line);
                while (true) {
                    if (hasResultSet) {
                        ResultSet rs = stmt.getResultSet();
                        System.out.println("Processing result set");
                        // ... process result set
                        rs.close();
                    }
                    else {
                        int count = stmt.getUpdateCount();
                        if (count == -1)
                            break;
                        System.out.println("Processing update count");
                        // ... process update count
                    }

                    // See if there are any more results
                    hasResultSet = stmt.getMoreResults();
                }
            }
            stmt.close();
```



## JSP：完整参考指南

```java
        in.close();
    }
    finally {
        if (con != null)
            con.close();
    }
}
}
```

`execute` 方法的初始返回值是一个布尔值，如果语句执行产生了结果集，则该值为 `true`。如果没有产生结果集，则可以通过 `Statement.getUpdateCount()` 获取更新计数。如果更新计数为 `-1`，则表示没有更多结果。否则，可以调用 `Statement.getMoreResults()` 方法来遍历下一个结果集或更新计数。该方法返回的布尔值，其解释与 `execute` 方法返回的布尔值相同。

## executeBatch 方法

JDBC 2.0 引入了将一组更新语句作为批处理提交执行的能力。在某些情况下，这可以显著提升性能。与批处理更新相关的方法如下：

- `clearBatch` 将批处理重置为空状态。
- `addBatch` 将一条更新语句添加到批处理中。
- `executeBatch` 提交批处理并收集更新计数。

并非所有驱动程序都支持批处理更新。支持批处理更新的驱动程序会通过其 `DatabaseMetaData.supportsBatchUpdates()` 方法返回 `true` 来表明这一点。一个实现了此功能的驱动程序是用于 Microsoft Access 的 JDBC-ODBC 桥接驱动。在以下示例中，使用批处理更新了 LyricNote 产品数据库中的一个表，该表存储了至少活到 90 岁的作曲家信息。

```java
import java.io.*;
import java.sql.*;
import java.util.*;

public class BatchUpdateExample
{
    public static void main(String[] args)
        throws ClassNotFoundException, SQLException, IOException
    {
        Class.forName("sun.jdbc.odbc.JdbcOdbcDriver");

        Connection con = null;
        try {

            // 连接到 composers 数据库

            con = DriverManager.getConnection
                ("jdbc:odbc:composers");
            Statement stmt = con.createStatement();

            // 清除现有表并创建新表

            stmt.executeUpdate("DROP TABLE over90");
            stmt.executeUpdate(
                " CREATE TABLE over90"
                + " ("
                + "     lastName     VARCHAR(20),"
                + "     firstName    VARCHAR(20),"
                + "     age          INTEGER"
                + " )"
            );

            // 设置用于处理整体事务

            con.setAutoCommit(false);

            // 将插入语句添加到批处理

            stmt.clearBatch();

            stmt.addBatch("INSERT INTO over90 VALUES"
                + " ('Rodrigo','Joaquin',99)");
            stmt.addBatch("INSERT INTO over90 VALUES"
                + " ('Gossec','Francois-Joseph',96)");
            stmt.addBatch("INSERT INTO over90 VALUES"
                + " ('Ruggles','Carl',96)");
            stmt.addBatch("INSERT INTO over90 VALUES"
                + " ('Widor','Charles-Marie',94)");
            stmt.addBatch("INSERT INTO over90 VALUES"
                + " ('Sibelius','Jean',93)");
            stmt.addBatch("INSERT INTO over90 VALUES"
                + " ('Copland','Aaron',91)");
            stmt.addBatch("INSERT INTO over90 VALUES"
                + " ('Britten','Benjamin',91)");
            stmt.addBatch("INSERT INTO over90 VALUES"
                + " ('Martinu','Bohuslav',89)");
            stmt.addBatch("INSERT INTO over90 VALUES"
                + " ('Auber','Daniel Francois',90)");
            stmt.addBatch("INSERT INTO over90 VALUES"
                + " ('Stravinsky','Igor',90)");

            // 执行批处理并检查更新计数

            int[] counts = stmt.executeBatch();

            boolean allGood = true;
            for (int i = 0; i < counts.length; i++)
                if (counts[i] != 1)
                    allGood = false;

            // 提交或回滚事务

            if (allGood) {
                System.out.println
                    ("Transaction successful with "
                    + counts.length + " statements committed");
                con.commit();
            }
            else {
                System.out.println("Transaction failed");
                con.rollback();
            }

            // 完成

            stmt.close();
        }
        finally {
            if (con != null)
                con.close();
        }
    }
}
```

设置连接的 `autoCommit` 标志为 `false`，使得我们可以选择将整个批处理更新作为一个事务进行提交或回滚。

## PreparedStatement

`java.sql.PreparedStatement` 是 `Statement` 的一个子接口，它使用预编译的 SQL。如果语句被重复使用，这可能会带来性能上的提升。`PreparedStatement` 与 `Statement` 的不同之处在于，其执行方法不接收 SQL 字符串作为参数。相反，SQL 字符串是在创建 `PreparedStatement` 时指定的，如下所示：

```java
PreparedStatement pstmt = con.prepareStatement(sqlstring);
```

要执行的字符串可以包含替换参数，这些参数通过字符串中的问号（`?`）来表示。这些参数在语句中充当占位符，必须在执行前用值填充。为此，API 提供了许多 `setXXX()` 方法，其中 `XXX` 是 Java 数据类型。

前面创建并加载了一个存储至少活到 90 岁作曲家信息的表的批处理更新示例，也可以使用 `PreparedStatement` 在循环中执行来实现，如下所示：

```java
import java.io.*;
import java.sql.*;
import java.util.*;

public class PreparedStatementExample
{
    public static void main(String[] args)
        throws ClassNotFoundException, SQLException, IOException
    {
        String DRIVER = "sun.jdbc.odbc.JdbcOdbcDriver";
        String URL = "jdbc:odbc:composers";

        Connection con = null;
        try {
            // 加载驱动程序类
            Class.forName(DRIVER);
            // 连接到数据库
            con = DriverManager.getConnection(URL);
            // 创建新表
            Statement stmt = con.createStatement();
            try {
                stmt.executeUpdate("DROP TABLE OVER90");
            }
            catch (SQLException ignore){}
            stmt.executeUpdate(
                " CREATE TABLE over90"
                + " ("
                + "     lastName      VARCHAR(20),"
                + "     firstName     VARCHAR(20),"
                + "     age           INTEGER"
                + " )"
            );
            stmt.close();
            stmt = null;

            // 准备一条用于向表中插入数据的语句

            PreparedStatement pstmt = con.prepareStatement(
                "INSERT INTO over90 VALUES(?, ?, ?)"
            );

            // 从使用制表符分隔字段的文件中
            // 读取作曲家姓名和年龄

            BufferedReader in =
                new BufferedReader(
                new FileReader("over90.txt"));

            while (true) {
                String line = in.readLine();
                if (line == null)
                    break;

                // 将行拆分为姓氏、名字
                // 和年龄标记

                StringTokenizer st = new StringTokenizer(line, "\t");
                if (st.countTokens() != 3)
                    throw new IOException ("Expected 3 fields");

                String lastName = st.nextToken();
                String firstName = st.nextToken();
                int age = Integer.parseInt(st.nextToken());

                // 在预处理语句中设置参数

                pstmt.setString(1, lastName);
                pstmt.setString(2, firstName);
                pstmt.setInt(3, age);

                // 更新记录

                pstmt.executeUpdate();
                System.out.println(
                    "Added record for " + firstName + " " + lastName);
            }

            in.close();

            pstmt.close();
            pstmt = null;

        }
        finally {
            if (con != null)
                con.close();
        }
    }
}
```

请考虑代码中的几个关键点。首先，需要使用替换参数来创建语句：

```java
PreparedStatement pstmt = con.prepareStatement(
    "INSERT INTO over90 VALUES(?, ?, ?)"
);
```

这里有三个问号，每个对应表中的一列。请注意，数字参数和字符串参数在使用上没有区别。两者都简单地编码为问号，不需要嵌入引号或撇号。

要将从文件读取的值用于 INSERT 语句，请使用 `setString()` 和 `setInt()` 方法：

```java
pstmt.setString(1, lastName);
pstmt.setString(2, firstName);
pstmt.setInt(3, age);
```

`setXXX()` 方法的第一个参数是列号，第一列从 1 开始，第二列从 2 开始，依此类推。第二个参数是要插入的值。

针对所有数据类型都有相应的 `setXXX()` 方法，此外还有两个特殊的方法：`setObject()` 和 `setNull()`。可以使用 `setObject()` 将值转换为任何 JDBC 数据类型，它接受第三个参数：

```java
pstmt.setNull(int column, int typeNumber)
```

其中 `typeNumber` 是在 `java.sql.Types` 中定义的静态整数常量。同样，`setNull()` 可用于在参数中存储适当的空类型：

```java
pstmt.setNull(int column, int typeNumber)
```

## 使用 PreparedStatement 避免动态语法错误

虽然使用预处理语句的主要动机是性能，但它还存在另一个微妙的优势。假设您想创建一个 JSP 页面，该页面可以对 LyricNote 产品数据库运行查询。页面包含一个表单，可以输入搜索参数。该参数从请求参数中提取，然后动态构建一条 SQL 语句。以下是显示如何构建 SQL 的 JSP 页面部分代码：

```java
ResultSet rs = stmt.executeQuery(
    " SELECT itemcode, description"
    + " FROM products"
    + " WHERE prodtype = 'SM'"
    + " AND description like '%' + searchFor + '%'"
    );
```

当 JSP 页面用于搜索斯特拉文斯基的作品时，它会返回如图 13-5 所示的结果。

但是，如果您专门搜索斯特拉文斯基的《士兵的故事》（*L'Histoire du Soldat*），则会遇到如图 13-6 所示的严重错误屏幕。



## 第十三章：数据库访问

发生了什么？错误信息中可以找到解释：

```
javax.servlet.ServletException
java.sql.SQLException: SELECT itemcode, description
FROM products
WHERE prodtype = 'SM'
AND description like '%L'Histoire du Soldat%'

Don't understand SQL after: "Histoire"
```

单词*L'Histoire*中包含一个嵌入式撇号，因此当评估`LIKE`子句时，它会过早终止，将'`%L`'视为它试图匹配的操作数。后续内容被解析为SQL语句，从而导致错误。

可以通过扫描用户输入中的嵌入式撇号并将其替换为安全的替代字符来避免此问题，但这比听起来更复杂。这种被称为*转义字符*的技术在不同的数据库和SQL方言中有所不同。存在一种基于JDBC架构的方式来指示转义字符，但这会增加在所有需要处理用户输入的地方的复杂性。

处理此问题更简单、更清晰的方法是使用带有替换参数的`PreparedStatement`。需要更改的代码如下：

```
PreparedStatement pstmt = con.prepareStatement(
    " SELECT itemcode, description\n"
    + " FROM products\n"
    + " WHERE prodtype = 'SM'\n"
    + " AND description like ?"
);
pstmt.setString(1, "%" + searchFor + "%");
ResultSet rs = pstmt.executeQuery();
```

现在，`LIKE`子句的操作数只是一个问号，搜索参数在运行时动态添加。现在，无论输入在SQL中的含义如何，查询都能处理任何类型的输入，如图13-7所示。

## CallableStatement

`PreparedStatement`的一个进一步改进体现在`java.sql.CallableStatement`中。如果数据库支持存储过程，此接口用于调用它们⁶。例如，Oracle允许使用PL/SQL编写存储过程。在Microsoft Access中编写的查询可以通过JDBC-ODBC桥作为存储过程调用。

6 很少或没有非商业数据库支持存储过程。

与其直接超接口PreparedStatement一样，CallableStatement是用显式命令字符串创建的，该字符串会被预编译：

```
CallableStatement cstmt = con.prepareCall(escapeString) ;
```

它也使用问号来指示替换参数。与CallableStatement一起使用的存储过程调用的语法如下：

```
{? = call procedureName(?, ?, ..., ?)}
```

如果过程没有返回值，则应省略"? ="。类似地，如果没有输入参数，则不使用"(?, ?, ..., ?)"。

因为CallableStatement扩展了PreparedStatement，所以它使用相同的方法来设置替换参数值：

```
String sql = "{call myproc(?, ?)}";
CallableStatement cstmt = con.prepareCall(sql);
cstmt.setString(1, "New York");
cstmt.setDouble(2, "19.73");
cstmt.executeQuery();
```

如果任何参数是OUT或INOUT类型，则在执行调用之前必须使用`CallableStatement.registerOutParameter()`注册它们的类型。它们的值可以使用与PreparedStatement相同的`getXXX()`方法检索。

## Microsoft Access中的存储过程

Microsoft Access支持使用SQL编写的查询或使用其自身设计向导开发的查询。这些查询可以使用JDBC-ODBC桥和`CallableStatement`按名称调用。图13-8显示了一个查询的设计视图，该查询创建了一个出生于指定年份区间的作曲家列表。起始年份和结束年份是查询的输入参数。

当使用1891-1900作为年份区间运行时，选中了12条记录。结果显示在图13-9中。

此查询可以使用`CallableStatement`从JSP页面运行，如以下清单所示。JSP页面执行的步骤如下：

-   1. 在HTML表单中提示输入起始年份和结束年份。
-   2. 通过JDBC-ODBC桥连接到Access数据库。
-   3. 创建一个调用查询的`CallableStatement`。
-   4. 从表单值设置起始年份和结束年份参数。
-   5. 执行查询。
-   6. 在HTML表格中显示结果。

```
<%@ page session="false" %>
<%@ page import="java.sql.*" %>
<%
  // 提示输入起始年份和结束年份

  String sLo = request.getParameter("lo");
  if (sLo == null)
    sLo = "";
  String sHi = request.getParameter("hi");
  if (sHi == null)
    sHi = "";
%>
<H3>按出生年份选择作曲家</H3>
<FORM>
<TABLE>
<TR>
  <TD>年份范围：
<INPUT TYPE="TEXT" NAME="lo" SIZE=4 VALUE="<%= sLo %>">
至
<INPUT TYPE="TEXT" NAME="hi" SIZE=4 VALUE="<%= sHi %>">
<INPUT TYPE="SUBMIT" VALUE="搜索">
</TD>
</TR>
</TABLE>
</FORM>
<%
    if (!sLo.equals("") && (!sHi.equals(""))) {

        int lo = Integer.parseInt(sLo);
        int hi = Integer.parseInt(sHi);

        // 加载驱动程序

        Class.forName("sun.jdbc.odbc.JdbcOdbcDriver");
        Connection con = null;
        try {

            // 连接到作曲家数据库

            con = DriverManager.getConnection
                ("jdbc:odbc:lyricnote_internal");

            // 设置可调用过程

            String sql = "{call BornBetween(?, ?)}";
            CallableStatement cstmt = con.prepareCall(sql);
            cstmt.setInt(1, lo);
            cstmt.setInt(2, hi);
            ResultSet rs = cstmt.executeQuery();
%>
<P>
<TABLE BORDER=1 CELLPADDING=3 CELLSPACING=0>
<TR>
    <TH>姓名</TH>
    <TH>国籍</TH>
    <TH>生活年代</TH>
</TR>
<%
    // 打印结果集
```

结果如图13-10所示。
当然，由于查询本身是基于SQL的，难道不能在JSP页面中使用普通的Statement执行等效的SQL语句吗？也许可以，但有几个充分的理由说明你可能选择不这样做：

-   - 该查询已在本地Microsoft Access环境中编写和测试。可能已经开发了数百个查询，转换它们的必要性不大。
-   - 如果在其原始形式中修改了查询，更改将自动反映在基于Web的版本中。
-   - 该查询可能使用在Access中有效，但通过ODBC和JDBC-ODBC桥层不支持的数据库功能。

## 结果集

*结果集*是一个有序的表行列表，在JDBC中用java.sql.ResultSet接口表示。结果集由executeQuery()或某些元数据方法调用产生。一旦创建，结果集中的数据可以按如下方式提取：

-   1. 通过调用ResultSet.next()方法或JDBC 2.0提供的更丰富的方法集之一——absolute()、relative()、next()、previous()、first()、last()、beforeFirst()或afterLast()——移动到所需的行。
-   2. 使用ResultSet.getXXX(columnNumber)或ResultSet.getXXX(columnName)检索所需的列值，其中XXX是JDBC数据类型。

以下是一个简单的示例，使用一个JSP页面在LyricNote作曲家数据库中搜索出生于爱尔兰的作曲家：

```
<%@ page session="false" %>
<%@ page import="java.sql.*" %>
<HTML>
<HEAD>
<TITLE>爱尔兰作曲家</TITLE>
</HEAD>
<BODY>
<H3>爱尔兰作曲家</H3>
<TABLE BORDER=0 CELLPADDING=3 CELLSPACING=1>
<%
    // JDBC驱动程序名称和数据库URL可以存储
    // 在web.xml中作为上下文参数，这样它们
    // 就不必硬编码。

    String DRIVER = application.getInitParameter("jdbc.driver");
    String URL = application.getInitParameter("jdbc.url.internal");

    // 加载驱动程序

    Class.forName(DRIVER);

    Connection con = null;
    try {

        // 连接到数据库

        con = DriverManager.getConnection(URL);
        Statement stmt = con.createStatement();

        // 创建查询以选择爱尔兰作曲家

        String sql =
            "SELECT lname, fname, born, died"
            + " FROM composers"
            + " WHERE nationality = 'Irish'";

        // 执行查询以创建结果集

        ResultSet rs = stmt.executeQuery(sql);

        // 遍历结果集的每一行

        while (rs.next()) {

            // 从当前行提取两个字符串值和两个
            // 整数值
```



## 可滚动结果集

当 Statement 执行查询时，会创建一个 ResultSet 对象。JSP 页面使用 `next()` 方法逐行读取数据，然后通过 `getString()` 或 `getInt()` 提取每列的值。结果显示在图 13-11 中。

可以对 `ResultSet` 对象调用多个 `getXXX()` 方法。表 13-1 列出了完整清单。每个 `getXXX()` 方法都有两个版本：一个接受整数列号（1，2，...），另一个接受列名字符串。通过列号访问列的效率可能略高，尽管当字段顺序发生变化时，使用列名更易于维护。

| 方法 | 描述 |
|---|---|
| `getArray` | 返回一个 SQL 数组。 |
| `getAsciiStream` | 返回一个已打开的 ASCII 字符 `java.io.InputStream`。向 ASCII 的转换（如有必要）由 JDBC 驱动程序处理。 |
| `getBigDecimal` | 返回一个 `java.math.BigDecimal`。 |
| `getBinaryStream` | 返回一个已打开的 `java.io.InputStream`。不对流进行任何转换。 |
| `getBlob` | 返回一个 `java.sql.Blob`（*二进制大对象*）。 |
| `getBoolean` | 返回一个布尔值。 |
| `getByte` | 返回一个单字节。 |
| `getBytes` | 返回一个字节数组。 |
| `getCharacterStream` | 返回一个 `java.io.Reader` 字符流。 |
| `getClob` | 返回一个 `java.sql.Clob`（*字符大对象*）。 |
| `getDate` | 返回一个 `java.sql.Date`。注意，这是 `java.util.Date` 的子类。 |
| `getDouble` | 返回一个双精度浮点值。 |
| `getFloat` | 返回一个单精度浮点值。 |
| `getInt` | 返回一个整数值。 |
| `getLong` | 返回一个长整数值。 |
| `getObject` | 返回一个 `java.lang.Object`。 |
| `getRef` | 返回一个 `java.sql.Ref`，它是对 SQL 结构化类型值的引用。 |
| `getShort` | 返回一个短整数值。 |
| `getString` | 返回一个字符串。 |
| `getTime` | 返回一个 `java.sql.Time` 值。 |
| `getTimestamp` | 返回一个 `java.sql.Timestamp` 值，其中包含纳秒级时间。 |

**表 13-1.** *ResultSet 提供的 getXXX() 方法*

JDBC 2.0 在结果集中引入了重要的新特性，这将在接下来的三节中讨论。

## 可滚动结果集

最初，结果集只能单向（向前）导航，且只能从一个点（第一行）开始。有了 JDBC 2.0，程序员有了更大的灵活性。游标（行指针）可以像操作数组索引一样进行操控。存在用于向前和向后读取、从任意行开始以及测试当前游标位置的方法。表 13-2 列出了可用的导航方法。

| 方法 | 描述 |
| :--- | :--- |
| `boolean next()` | 将游标移动到下一行。 |
| `boolean previous()` | 将游标向后移动一行。 |
| `boolean first()` | 将游标移动到第一行。 |
| `boolean last()` | 将游标移动到最后一行。 |
| `void beforeFirst()` | 将游标移动到第一行之前，通常为调用 `next()` 做准备。 |
| `void afterLast()` | 将游标移动到最后一行之后，通常为调用 `previous()` 做准备。 |
| `boolean absolute(int row)` | 将游标移动到指定行。指定负数可相对于结果集末尾移动游标；`absolute(-1)` 等同于 `last()`。 |
| `boolean relative(int row)` | 将游标向前或向后移动指定的行数。 |
| `boolean isBeforeFirst()` | 如果游标在第一行之前，则为真。 |
| `boolean isAfterLast()` | 如果游标在最后一行之后，则为真。 |
| `boolean isFirst()` | 如果游标位于第一行上，则为真。 |
| `boolean isLast()` | 如果游标位于最后一行上，则为真。 |

**表 13-2.** JDBC 2.0 可滚动结果集导航方法

要使用可滚动结果集，`Statement` 对象必须使用指示所请求特定能力的参数来创建。因此，`Connection.createStatement()` 方法存在一种新形式

```java
public Statement createStatement
    (int resultSetType, int resultSetConcurrency)
    throws SQLException
```

其中 `resultSetType` 是要使用的滚动类型，`resultSetConcurrency` 指示结果集是否可更新。两个参数的值都取自 `ResultSet` 中的常量，如表 13-3 所示。

| 常量 | 含义 |
|---|---|
| `TYPE_FORWARD_ONLY` | JDBC 1.0 风格的导航，游标从第一行开始且只能向前移动。 |
| `TYPE_SCROLL_INSENSITIVE` | 启用所有游标定位方法；结果集不反映其他人对底层表所做的更改。 |
| `TYPE_SCROLL_SENSITIVE` | 启用所有游标定位方法；结果集反映其他人对底层表所做的更改。 |
| `CONCUR_READ_ONLY` | 结果集不可更新。 |
| `CONCUR_UPDATABLE` | 可以添加和删除行，并且可以更新列。 |

**表 13-3.** ResultSet 中可用于描述可滚动结果集的常量

以下 JSP 页面是一个使用可滚动结果集仅显示可能很长的查询最后一页的示例。

```jsp
<%@ page import="java.sql.*" %>
<%@ page import="java.text.*" %>
<%!
    public static final DecimalFormat PRICE_FMT
        = new DecimalFormat("$#,###.00");
%>
<HTML>
<HEAD>
<TITLE>Scrollable Example</TITLE>
</HEAD>
<BODY>
<IMG SRC="images/lyric_note.png" BORDER=0><P>
<HR COLOR="#000000">
<%
    // Get driver name and database URL from configuration
    // parameters stored in web.xml

    String DRIVER = application.getInitParameter("jdbc.driver");
    String URL    = application.getInitParameter("jdbc.url");

    // Load the driver

    Class.forName(DRIVER);

    Connection con = null;
    Statement stmt = null;
    ResultSet rs   = null;

    try {

        // Connect to the database

        con = DriverManager.getConnection(URL);

        // Open a statement that supports scrollable result sets

        stmt = con.createStatement(
                       ResultSet.TYPE_SCROLL_INSENSITIVE,
                       ResultSet.CONCUR_READ_ONLY);

        // Execute the query

        rs = stmt.executeQuery(
                 " SELECT   itemcode, price, description"
               + " FROM     products"
               + " WHERE    prodtype = 'IN'"
               + " ORDER BY description"
            );

        // Calculate number of rows

        rs.last();
        int nRows = rs.getRow();

        // Back up ten rows

        rs.relative(-10);

        // Now print last page of result set
%>
<H3>
    Musical Instruments
    - Items <%= rs.getRow() + 1 %> through <%= nRows %>
</H3>
<TABLE BORDER=1 CELLPADDING=3 CELLSPACING=0>
<TH><TH>Item</TH><TH>Price</TH><TH>Description</TH></TH>
<%
    while (rs.next()) {
        String itemcode = rs.getString(1);
        double price = rs.getLong(2) / 100.0;
        String description = rs.getString(3);
%>
<TD><%= itemcode %></TD>
<TD ALIGN="RIGHT"><%= PRICE_FMT.format(price) %></TD>
<TD><%= description %></TD>
</TR>
<%
    }
}
finally {
    if (rs != null) { rs.close(); rs = null; }
    if (stmt != null) { stmt.close(); stmt = null; }
    if (con != null) { con.close(); con = null; }
}
%>
</TABLE>
</BODY>
</HTML>
```

Statement 对象被打开，以便其创建的结果集是可滚动的，但不可更新。具有这些属性后，可以询问 ResultSet 它包含多少行，这在 JDBC 1.0 中是不可能的。通过将游标定位到最后一行并发出 `relative(-10)` 方法调用，可以隔离并打印结果集中的最后十行。图 13-12 显示了结果。

## 可更新结果集

通过 JDBC 2.0，可以更新结果集中的列，包括添加新行和删除现有行。在这两种情况下，底层表中的相应行也会随之更新。



要更新结果集，它必须由使用并发类型 `ResultSet.CONCUR_UPDATABLE` 创建的 `Statement` 对象生成。JDBC 2.0 提供了 `updateXXX()` 方法，其中 `XXX` 是 JDBC 数据类型，类似于现有的 `getXXX()` 方法。这些方法接受一个列号或列名参数，以及一个值参数，如下例所示：

```java
double mySalary = rs.getDouble("SALARY");
mySalary *= 2.0;
rs.updateDouble("SALARY", mySalary);
rs.updateString("HOME_PHONE", unlisted);
rs.updateRow();
```

更新后的值在调用 `updateRow()` 之前不会自动复制到基础表中。如果尚未调用 `updateRow()`，可以显式地通过 `ResultSet.cancelRowUpdates()` 取消更新；如果在调用 `updateRow()` 之前调用了游标移动方法，则会隐式取消更新。

可以使用 `insertRow()` 将新行添加到结果集和基础表中。这涉及到一个称为 `insert row` 的特殊游标位置。以下示例说明了其工作原理：

```java
rs.moveToInsertRow();
rs.setString("employeeid", "M1205");
rs.setString("firstName", "Maria");
rs.setString("lastName", "Alicia");
rs.insertRow();
rs.moveToCurrentRow(); // 返回到之前的位置
```

类似地，可以使用 `deleteRow()` 删除结果集及其基础表中的行。为此，游标必须定位到要删除的行，如下所示：

```java
rs.last(); // 删除最后一行
rs.deleteRow();
```

## RowSets

`javax.sql` 包包含一个 `RowSet` 接口，它扩展并泛化了 `java.sql.ResultSet`，使其可以从数据库连接中分离。这对于不容易保持连接且内存有限的 *个人数字助理* (*PDA*) 应用程序很有用。目前，RowSets 仍处于起步阶段。Sun Microsystems 提供了该接口的三个早期访问实现，可用于探索其功能：

- **CachedRowSet**：一个可序列化、可断开连接的 RowSet，可以从 JDBC 结果集填充。
- **JdbcRowSet**：一个连接的 RowSet，同样从 JDBC 结果集填充，其行为遵循 JavaBeans 模型。
- **WebRowSet**：`CachedRowSet` 的一个子类，可以将内容写为 XML 文档。

## 使用元数据

JDBC 提供了一组丰富的 *元数据*（关于数据的数据），用于数据库连接和结果集。本节描述这两个接口、如何获取它们的实例，以及它们可以提供哪些信息的要点。

## 数据库元数据

有关 JDBC 连接的信息可以通过 `Connection.getMetaData()` 获取。此方法返回 `java.sql.DatabaseMetaData` 的一个实例，该接口的方法数量（总共 149 个）比 `java.sql` 或 `javax.sql` 包中的任何其他类或接口都多。这些方法描述了数据库支持的功能、包含的表以及这些表中的列。使用元数据，可以最大程度地减少 SQL 语言和数据库系统功能的差异。

查看 `DatabaseMetaData` 对象提供的所有信息可能具有指导意义。由于接口中有如此多的方法，手动编写所有单独的调用很繁琐。为此，使用反射以编程方式列出所有元数据方法，然后调用每个方法并打印结果，会更容易。以下 JSP 页面 (`MetadataExplorer.jsp`) 演示了这种技术：

```jsp
<%@ page session="false" %>
<%@ page import="java.sql.*" %>
<%@ page import="java.util.*" %>
<%@ page import="java.lang.reflect.*" %>
<%
    // 获取所需的驱动程序名称参数

    String driverName = request.getParameter("driverName");
    if (driverName == null)
        driverName = "";
    driverName = driverName.trim();
    if (driverName.equals(""))
        throw new ServletException("缺少 driverName 参数");

    // 获取所需的数据库 URL 参数

    String url = request.getParameter("url");
    if (url == null)
        url = "";
    url = url.trim();
    if (url.equals(""))
        throw new ServletException("缺少 url 参数");

    // 获取可选的 userID 参数

    String userID = request.getParameter("userID");
    if (userID == null)
        userID = "";
    userID = userID.trim();

    // 获取可选的密码参数

    String password = request.getParameter("password");
    if (password == null)
        password = "";
    password = password.trim();
    // 加载驱动程序

    Class.forName(driverName);
    Connection con = null;
    try {

    // 打开数据库连接并获取元数据

    con = DriverManager.getConnection(url, userID, password);
    DatabaseMetaData md = con.getMetaData();

    // 使用反射获取元数据类支持的方法列表。
    // 只选择公有方法，这些方法不接受参数，
    // 并返回字符串或布尔值。

    Class mdclass = md.getClass();
    Method[] methods = mdclass.getDeclaredMethods();
    Map methodMap = new TreeMap();

    for (int i = 0; i < methods.length; i++) {
        Method method = methods[i];

        // 仅限公有方法

        if (!Modifier.isPublic(method.getModifiers()))
            continue;

        // 不带参数

        if (method.getParameterTypes().length > 0)
            continue;

        // 返回 String 或 boolean

        Class returnType = method.getReturnType();
        if ((returnType != java.lang.Boolean.TYPE) &&
            (returnType != java.lang.String.class))
            continue;

        // 将选定的方法添加到排序映射中

        methodMap.put(method.getName(), method);
    }
%>
<HTML>
<HEAD>
<TITLE>元数据浏览器</TITLE>
<LINK REL="stylesheet" HREF="style.css">
</HEAD>
<BODY>
<CENTER>
<H3>
<%= md.getDatabaseProductName() %> 的元数据浏览器
<%= md.getDatabaseProductVersion() %>
<BR>
[<%= driverName %>]
</H3>
<TABLE BORDER=0 CELLPADDING=3 CELLSPACING=1>
<TR CLASS="header">
    <TH CLASS="header">方法</TH>
    <TH CLASS="header">值</TH>
</TR>
<%
    // 生成表格

    int row = 0;
    Iterator im = methodMap.keySet().iterator();
    while (im.hasNext()) {
        String methodName = (String) im.next();
        Object methodValue = null;

        Method method = (Method) methodMap.get(methodName);

        // 调用方法并获取结果

        try {
            Object[] noParameters = new Object[0];
            methodValue = method.invoke(md, noParameters);
        }
        catch (Exception ignore) {}

        // 显示结果

        row++;
        String rowClass = "row" + (row % 2);
%>
<TR CLASS="<%= rowClass %>">
    <TD><%= methodName %></TD>
    <TD><%= formatLine(methodValue) %></TD>
</TR>
<%
    }
}
finally {
    if (con != null)
        con.close();
}
%>
</TABLE>
</CENTER>
</BODY>
</HTML>
<%!
    /**
     * 以 HTML 友好的方式格式化对象，
     * 确保其宽度不超过 48 个字符。
     */
    private static String formatLine(Object obj)
    {
        if (obj == null)
            return "";

        StringBuffer out = new StringBuffer();
        StringBuffer line = new StringBuffer();
        StringTokenizer st =
            new StringTokenizer(obj.toString(), ",;", true);

        while (st.hasMoreTokens()) {
            if (line.length() > 48) {
                out.append(line.toString());
                out.append("<BR>");
                line = new StringBuffer();
            }
            line.append(st.nextToken());
        }
        out.append(line.toString());

        return out.toString();
    }
%>
```

此 JSP 页面设计为从 HTML 表单调用，该表单提供驱动程序名称、JDBC URL、用户 ID 和密码字段，如图 13-13 所示。

当使用 JDBC-ODBC 桥接针对 Microsoft Access 数据库运行时，MetadataExplorer 生成的输出部分如图 13-14 所示。完整列表包含在表 13-4 中。



## 344 JSP：完全参考手册

| 方法 | 值 |
|---|---|
| allProceduresAreCallable | True |
| allTablesAreSelectable | True |
| dataDefinitionCausesTransactionCommit | True |
| dataDefinitionIgnoredInTransactions | False |
| doesMaxRowSizeIncludeBlobs | False |
| getCatalogSeparator | . |
| getCatalogTerm | DATABASE |
| getDatabaseProductName | ACCESS |
| getDatabaseProductVersion | 3.5 Jet |
| getDriverName | JDBC-ODBC Bridge (odbcjt32.dll) |
| getDriverVersion | 2.0001 (03.51.1713.00) |
| getExtraNameCharacters | ~@#$%^&*_-+=\}{\";:?><, |
| getIdentifierQuoteString | ` |
| getNumericFunctions | ABS, ATAN, CEILING, COS, EXP, FLOOR, LOG, MOD, POWER, RAND, SIGN, SIN, SQRT, TAN |
| getProcedureTerm | QUERY |
| getSQLKeywords | ALPHANUMERIC, AUTOINCREMENT, BINARY, BYTE, COUNTER, CURRENCY, DATABASE, DATABASENAME, DATETIME, DISALLOW, DISTINCTROW, DOUBLEFLOAT, FLOAT4, FLOAT8, GENERAL, IEEEDOUBLE, IEEESINGLE, IGNORE, INT, INTEGER1, INTEGER2, INTEGER4, LEVEL, LOGICAL, LOGICAL1, LONG, LONGBINARY, LONGCHAR, LONGTEXT, MEMO, MONEY, NOTE, NUMBER, OLEOBJECT, OPTION, OWNERACCESS, PARAMETERS, PERCENT, PIVOT, SHORT, SINGLE, SINGLEFLOAT, SMALLINT, STDEV, STDEVP, STRING, TABLEID, TEXT, TOP, TRANSFORM, UNSIGNEDBYTE, VALUES, VAR, VARBINARY, VARP, YESNO |
| getSchemaTerm | \ |
| getStringFunctions | ASCII, CHAR, CONCAT, LCASE, LEFT, LENGTH, LOCATE, LOCATE_2, LTRIM, RIGHT, RTRIM, SPACE, SUBSTRING, UCASE |

表 13-4. Microsoft Access 数据库的元数据（续）

| 方法 | 值 |
| :--- | :--- |
| getSystemFunctions | CURDATE, CURTIME, DAYOFMONTH, DAYOFWEEK, DAYOFYEAR, HOUR, MINUTE, MONTH, NOW, SECOND, WEEK, YEAR |
| getURL | jdbc:odbc:Composers |
| getUserName | admin |
| isCatalogAtStart | True |
| isReadOnly | False |
| nullPlusNonNullIsNull | False |
| nullsAreSortedAtEnd | False |
| nullsAreSortedAtStart | False |
| nullsAreSortedHigh | False |
| nullsAreSortedLow | True |
| storesLowerCaseIdentifiers | False |
| storesLowerCaseQuoted Identifiers | False |
| storesMixedCaseIdentifiers | False |
| storesMixedCaseQuoted Identifiers | True |
| storesUpperCaseIdentifiers | False |
| storesUpperCaseQuoted Identifiers | False |
| supportsANSI92EntryLevelSQL | True |
| supportsANSI92FullSQL | False |
| supportsANSI92IntermediateSQL | False |
| supportsAlterTableWith AddColumn | True |
| supportsAlterTableWith DropColumn | True |
| supportsBatchUpdates | True |
| supportsCatalogsInData Manipulation | True |

表 13-4. Microsoft Access 数据库的元数据（续）

| 方法 | 值 |
|---|---|
| supportsCatalogsInIndex Definitions | True |
| supportsCatalogsInPrivilege Definitions | False |
| supportsCatalogsInProcedure Calls | False |
| supportsCatalogsInTable Definitions | True |
| supportsColumnAliasing | True |
| supportsConvert | True |
| supportsCoreSQLGrammar | False |
| supportsCorrelatedSubqueries | True |
| supportsDataDefinitionAndData ManipulationTransactions | True |
| supportsDataManipulation TransactionsOnly | False |
| supportsDifferentTable CorrelationNames | False |
| supportsExpressionsInOrderBy | True |
| supportsExtendedSQLGrammar | False |
| supportsFullOuterJoins | False |
| supportsGroupBy | True |
| supportsGroupByBeyondSelect | True |
| supportsGroupByUnrelated | False |
| supportsIntegrity EnhancementFacility | False |
| supportsLikeEscapeClause | False |
| supportsLimitedOuterJoins | False |
| supportsMinimumSQLGrammar | True |
| supportsMixedCaseIdentifiers | True |
| supportsMixedCaseQuoted Identifiers | False |

表 13-4. Microsoft Access 数据库的元数据（续）

| 方法 | 值 |
| :--- | :--- |
| supportsMultipleResultSets | False |
| supportsMultipleTransactions | True |
| supportsNonNullableColumns | False |
| supportsOpenCursorsAcrossCommit | False |
| supportsOpenCursorsAcrossRollback | False |
| supportsOpenStatementsAcrossCommit | True |
| supportsOpenStatementsAcrossRollback | True |
| supportsOrderByUnrelated | False |
| supportsOuterJoins | True |
| supportsPositionedDelete | False |
| supportsPositionedUpdate | False |
| supportsSchemasInDataManipulation | False |
| supportsSchemasInIndexDefinitions | False |
| supportsSchemasInPrivilegeDefinitions | False |
| supportsSchemasInProcedureCalls | False |
| supportsSchemasInTableDefinitions | False |
| supportsSelectForUpdate | False |
| supportsStoredProcedures | True |
| supportsSubqueriesInComparisons | True |
| supportsSubqueriesInExists | True |
| supportsSubqueriesInIns | True |

表 13-4. Microsoft Access 数据库的元数据（续）

| 方法 | 值 |
| --- | --- |
| supportsSubqueriesIn Quantifieds | True |
| supportsTableCorrelationNames | True |
| supportsTransactions | True |
| supportsUnion | True |
| supportsUnionAll | True |
| usesLocalFilePerTable | False |
| usesLocalFiles | True |

表 13-4. Microsoft Access 数据库的元数据（续）

## ResultSetMetaData

除了用于数据库连接的 DatabaseMetaData 之外，ResultSetMetaData 还获取有关结果集列的信息。该接口包含一个获取列数的方法——getColumnCount()——以及 20 个描述各个列的其他方法。

要获取 ResultSetMetaData 对象，程序调用 ResultSet.getMetaData() 方法，然后调用其方法，并传递一个列号参数。与 ResultSet 一样，列号从 1 开始。

表 13-5 描述了 ResultSetMetaData 中可用的方法。

| 方法 | 描述 |
| --- | --- |
| getColumnCount() | 返回结果集中每一行的列数。 |
| getCatalogName(int col) | 返回指定列所属表的目录名称。 |
| getColumnClassName(int col) | 返回指定列的完全限定 Java 类型名称。 |

表 13-5. ResultSetMetaData 中可用的方法

| 方法 | 描述 |
|---|---|
| `getColumnDisplaySize(int col)` | 返回指定列的最大显示宽度。 |
| `getColumnLabel(int col)` | 返回指定列的标签。 |
| `getColumnName(int col)` | 返回指定列的名称。 |
| `getColumnType(int col)` | 返回与 java.sql.Types 对应的形式中指定列的类型。 |
| `getColumnTypeName(int col)` | 以字符串形式返回列数据类型。 |
| `getPrecision(int col)` | 返回小数位数。 |
| `getScale(int col)` | 返回小数点右边的数字位数。 |
| `getSchemaName(int col)` | 返回列所属表的模式名称。 |
| `getTableName(int col)` | 返回列所属表的名称。 |
| `isAutoIncrement(int col)` | 如果列是自动编号的，则返回 True。 |
| `isCaseSensitive(int col)` | 如果列的大小写重要，则返回 True。 |
| `isCurrency(int col)` | 如果列是现金值，则返回 True。 |
| `isDefinitelyWritable(int col)` | 如果对指定列的写入肯定会成功，则返回 True。 |
| `isNullable(int col)` | 返回一个指示列是否可以具有空值的常量。 |
| `isReadOnly(int col)` | 如果结果集是只读的，则返回 True。 |
| `isSearchable(int col)` | 如果此列可用于 where 子句，则返回 True。 |
| `isSigned(int col)` | 如果列值是有符号数字，则返回 True。 |
| `isWritable(int col)` | 如果对指定列的写入可能成功，则返回 True。 |

表 13-5. ResultSetMetaData 中可用的方法（续）

## JDBC 2.0 及更高版本中的新功能

JDBC 2.0 最初被称为 JDBC 2.0 标准扩展 API，现已更名为 JDBC 2.0 可选包 API。它包含在与 Java 2 标准版一起发行的 JDBC 2.1 核心 API 包中。本章中讨论了其许多新功能，包括：

- **DataSource** JDBC 驱动程序名称和 URL 可以存储在名称服务中，并使用 JNDI 检索。
- **连接池** 数据源提供商可以提供连接池，允许连接被激活和回收，通常可以显著提高性能。此功能完全在命名服务中配置，无需对应用程序进行任何更改。
- **可滚动结果集** JDBC 1.0 仅允许从第一条记录开始向前导航结果集。JDBC 2.0 提供了向前和向后导航以及相对和绝对游标定位的方法。
- **RowSets** 断开连接的结果集可以被设计成符合 JavaBeans 模型。
- **BatchUpdates** 事务可以分组并作为一个单元发送到数据库。

JDBC 3.0 的第一个公开草案于 2000 年 9 月发布供公众审查。其新功能包括：

- 增强了对提交/回滚事务边界的控制
- 连接池的可配置性
- 对预处理和可调用语句中参数的更好接口

## 总结

几乎所有非平凡的 JSP 应用程序都需要访问数据库。Java 提供了一个名为 JDBC 的标准 API。JDBC 允许在面向对象的框架中使用标准 SQL 语句访问各种各样的数据库系统。要使用 JDBC，必须为数据库提供相应的驱动程序。几乎所有商业数据库都有相应的驱动程序，还有一个用于使用 ODBC 数据源的 JDBC-ODBC 桥接驱动程序。

JDBC 中仅存在少数几个关键对象，这使其易于学习。`Connection` 对象维护与数据库的活动连接。三种类型的 `Statement` 对象允许通过连接执行 SQL 语句，并将结果捕获到 `ResultSet` 对象中。可以从 `DatabaseMetaData` 和 `ResultSetMetaData` 对象获取大量关于连接和结果集的信息。

JDBC 在多个版本中不断发展，功能不断增强，并有望继续成为 Java 编程的主导数据库访问技术。



## 完全参考

## 第14章

## 会话与线程管理

超文本传输协议（HTTP）最初是为在万维网（WWW）上分发文档和图像而设计的。因此，它采用了一种相当简单的通信模型。客户端发出文档请求，服务器以文档或某些错误代码作为响应，然后事务即告完成。服务器不会保留任何关于该请求的知识。下次客户端发出请求时，服务器无法将其与其他任何客户端区分开来。因此，HTTP被称为无状态协议。

不幸的是，很少有应用程序能完全适应这种单次请求/响应模型。在大多数情况下，要完成任何有意义的工作，都需要多次请求。例如，一个应用程序可能有一个用于输入用户ID和密码的网页，接着是一个请求输入搜索关键字以查询产品数据库的搜索页面，然后是匹配产品的列表页面、详细的产品信息页面、购物车结算页面和订单摘要页面。这些页面中的每一个都依赖于前面的页面，并且也依赖于服务器在特定时间了解该客户端的应用程序状态。更糟糕的是，客户端应用程序的用户可能会在页面间前进或后退，或者完全转到另一个网页，却从不告诉服务器会话已结束或如何处理任何未完成的工作。一个相关的问题是，一些服务器处理过程需要很长时间——如果Web服务器要保持合理的性能，它可能等不起这么长的时间。

这些问题并非新问题。通用网关接口（CGI）程序和在线事务处理系统多年来一直在处理同样的问题。在那些环境中应用的技术在Servlet/JSP环境中仍然有效，但Java Servlet API具有一种内置机制，提供了一个简洁、易于使用的解决方案：HTTP会话。

本章探讨了使JSP模型适应应用程序模型的两个关键方面：会话管理和线程管理。它讨论了四种会话跟踪技术，主要关注HTTP会话API，研究了会话如何创建、如何管理对象以及如何终止。然后，本章探讨了Java对多线程应用程序的内置支持以及可用的servlet线程模型，最后以一节内容结束，涵盖了关于对象生命周期和可见性的应用程序注意事项。

## 会话跟踪

由于Web服务器不会从一个请求到下一个请求记住客户端，因此维护会话的唯一方法是让客户端自己跟踪它。您可以通过两种基本方式来实现：

- 让客户端记住所有会话相关数据，并根据需要将其发送回服务器。
- 让服务器维护所有数据，为其分配一个标识符，并让客户端记住该标识符。

第一种方法实现简单，不需要服务器具备特殊功能。然而，这种方法可能涉及来回传输大量数据，从而可能降低性能。另一个问题是，服务器端对象，如数据库和网络连接，必须在每次请求时重新初始化。因此，这种方法最适合长期持久化少量数据，例如用户偏好设置或账户号码。

第二种方法提供了更多功能。一旦服务器启动会话并且客户端接受它，服务器就可以构建复杂的、活动的对象并维护大量数据，只需要一个键来区分会话。本章的大部分讨论都集中在这种方法上。

那么，我们如何让客户端记住数据并将其返回给Web服务器呢？通常使用四种技术：

- 隐藏字段
- URL重写
- Cookie
- HTTP会话API

以下各节将详细描述每种技术。

## 隐藏字段

HTML表单支持类型为HIDDEN的输入元素。*隐藏字段*会与其他表单参数一起在发送到Web服务器的HTTP请求中传递，但它们没有任何可视的表示形式。它们仅用于将字面量或常量值包含在请求中。类似的技术被用于CICS和大型机事务监视器中，以提供事务代码。原则上，隐藏字段可以在普通的HTML网页中使用，但是，为了会话跟踪的目的，它们必须在由服务器进程（如CGI、servlet或JSP）动态生成的网页中使用。

隐藏字段非常适合那些不需要大量数据存储或对象初始化的来回对话式应用程序。一个例子是包含在Tomcat示例文件夹中的著名猜数字游戏。这个游戏选择一个1到100之间的随机整数，然后让用户猜测它。每次猜测后，游戏会告诉用户猜测是太低、太高还是完全正确。

下面展示的JSP是一个做相反事情的游戏：它要求用户想一个1到100之间的数字，然后猜测这个数字，依靠用户来指示每次猜测是太低、太高还是完全正确。¹ 这个JSP使用二分查找来找到这个数字。

```
<%@ page session="false" %>
<H3>Number Guess Guesser</H3>
<%
    int wayLo = 1 - 1;
    int wayHi = 100 + 1;
    int state = 0;
    String parm = request.getParameter("state");
    if (parm != null)
        state = Integer.parseInt(parm);

    switch (state) {
        case 0: {   // 初始屏幕
%>
<FORM>
Think of a number between
<%= wayLo + 1 %> and <%= wayHi - 1 %>,
and I'll try to guess it.<P>
Click OK when ready.<P>
<INPUT TYPE="submit" VALUE="OK">
<INPUT TYPE="hidden" NAME="lo" VALUE="<%= wayLo %>">
<INPUT TYPE="hidden" NAME="hi" VALUE="<%= wayHi %>">
<INPUT TYPE="hidden" NAME="numGuesses" VALUE="0">
<INPUT TYPE="hidden" NAME="state" VALUE="1">
</FORM>
<%
            break;
        }
        case 1: {   // 第一次猜测
            int numGuesses = 1 + Integer.parseInt
                (request.getParameter("numGuesses"));
            int lo = Integer.parseInt(request.getParameter("lo"));
            int hi = Integer.parseInt(request.getParameter("hi"));
            int guess = (hi + lo)/2;
```

¹ 如果您在单独的窗口中同时运行这些程序，您可以看到它们礼貌地评论对方的进展。

```
%>
<FORM>
My first guess is <%= guess %>. How did I do?<P>
<INPUT TYPE="radio"
        NAME="result"
        VALUE="-1" onClick="submit()"> Too low
<INPUT TYPE="radio"
        NAME="result"
        VALUE="0" onClick="submit()"> Exactly right
<INPUT TYPE="radio"
        NAME="result"
        VALUE="1" onClick="submit()"> Too high
<P>
<INPUT TYPE="hidden" NAME="lo" VALUE="<%= lo %>">
<INPUT TYPE="hidden" NAME="hi" VALUE="<%= hi %>">
<INPUT TYPE="hidden" NAME="numGuesses" VALUE="<%= numGuesses %>">
<INPUT TYPE="hidden" NAME="state" VALUE="2">
</FORM>
%
    break;
}
case 2: {  // 第一次猜测后
    int numGuesses = 1 + Integer.parseInt
        (request.getParameter("numGuesses"));
    int lo = Integer.parseInt(request.getParameter("lo"));
    int hi = Integer.parseInt(request.getParameter("hi"));
    int result =
        Integer.parseInt(request.getParameter("result"));
    int guess = (hi + lo)/2;

    if (result < 0) {
        lo = guess;
        guess = (hi + lo)/2;
    }
    else if (result > 0) {
        hi = guess;
        guess = (hi + lo)/2;
    }

    if (result != 0) {
%>
<FORM>
```

```
<%
    if (lo > wayLo)
        out.println(lo + " is too low.<BR>");
    if (hi < wayHi)
        out.println(hi + " is too high.<BR>");
    if ((hi - lo) > 1) {
%>
My next guess is <%= guess %>. How did I do?<P>
<INPUT TYPE="radio"
       NAME="result"
       VALUE="-1" onClick="submit()"> Too low
<INPUT TYPE="radio"
       NAME="result"
       VALUE="0" onClick="submit()"> Exactly right
<INPUT TYPE="radio"
       NAME="result"
       VALUE="1" onClick="submit()"> Too high
<P>
<INPUT TYPE="hidden" NAME="lo" VALUE="<%= lo %>">
<INPUT TYPE="hidden" NAME="hi" VALUE="<%= hi %>">
<INPUT TYPE="hidden" NAME="numGuesses" VALUE="<%= numGuesses %>">
<INPUT TYPE="hidden" NAME="state" VALUE="2">
</FORM>
<%
    }
    else {
        String[] text = {
            "Are we cheating?",
            "Did we forget our number?",
            "Perhaps we clicked the wrong button?",
            "What happened?",
            "What gives?",
        };
        String message = text[(int) (Math.random() * text.length)];
%>
<FORM>
<%= message %><P>
<INPUT TYPE="SUBMIT" VALUE="Start Over">
</FORM>
<%
```



JSP 页面使用一个名为 `state` 的隐藏字段来跟踪游戏中的状态变化。根据状态的不同，它会显示相应的表单：

-   **状态 0** 初始表单解释游戏规则并设置要使用的变量。这些变量包括状态、猜测次数、已知太低的最高值，以及已知太高的最低值。所有变量都作为表单中的隐藏字段存储。
-   **状态 1** 用户点击确认按钮后，程序会获取“太低”和“太高”的参数，并将两者的平均值作为下一次猜测。表单会提供三个单选按钮供用户指示猜测是太低、太高还是完全正确。新的“低”值和“高”值、用户选择的结果以及递增的猜测次数会再次作为隐藏字段存储。
-   **状态 2** 根据用户在单选按钮中的选择，程序会使用新的上限或下限更新“太低”或“太高”的值。如果猜测完全正确，程序会祝贺自己并提示是否再玩一次。否则，它将显示已知的上下限及其下一次猜测，如图 14-1 所示。

隐藏字段的问题在于它们只能在 HTML 表单中使用。如果用户点击超链接离开页面，隐藏字段就会丢失，除非同时采用下一节描述的技术——URL 重写。

## URL 重写

URL 可以附加参数，这些参数会与请求一起发送到 Web 服务器。这些参数是名称/值对，语法如下：

`http://server/MyPage.jsp?name1=value1&name2=value2&...`

当 JSP 页面收到请求时，可以使用以下代码读取值：

```
String value1 = request.getParameter("name1");
String value2 = request.getParameter("name2");
...
```

动态生成的 Web 页面可以利用这一功能，将会话数据存储在作为超链接写入页面的 URL 中。这允许客户端提醒服务器所有必要的值，以将服务器应用程序置于所需状态。

一个简单的例子是一个计数器，它指示用户在当前会话中访问页面的次数，如下所示：

```
<%@ page session="false" %>
<HTML>
<HEAD>
<TITLE>Page Counter Using URL Rewriting</TITLE>
</HEAD>
<BODY>
<H3>Page Counter Using URL Rewriting</H3>
<%
    int count = 0;
    String parm = request.getParameter("count");
    if (parm != null)
        count = Integer.parseInt(parm);
    if (count == 0) {
%> This is the first time you have accessed this page. <%
    }
    else if (count == 1) {
%> You have accessed the page once before.<%
    }
    else {
%> You have accessed the page <%= count %> times before.<%
    }
%>
<P> Click
<A HREF="Counter.jsp?count=<%=count + 1 %>"
   >here</A> to visit the page again.
</BODY>
</HTML>
```

当用户首次使用基本 URL 请求页面时，不存在 count 参数，因此整型 count 变量被设置为零：

![](img/7a2f73369bb140583c7288b73456addb_387_0.png)

页面底部有一个超链接，该链接再次调用 counter.jsp 页面，但这次带有一个 count 参数，其值比当前 count 大一：

![](img/7a2f73369bb140583c7288b73456addb_388_0.png)

每次重新调用页面时，计数器都会更新，并且消息会发生变化：

![](img/7a2f73369bb140583c728b73456addb_388_1.png)

该技术保证在所有浏览器环境和安全设置中都能工作，但这也几乎是它唯一的优点。如果存储大量数据，该技术往往会降低性能。URL 可能会变得非常大，可能超过 Web 服务器接受的大小。此外，URL 不安全，会在浏览器地址窗口和 Web 服务器日志中可见。页面上的每个 URL 都必须重写的要求需要大量繁琐的代码，而且在此过程中很容易忽略一个 URL。尽管如此，对于简单的应用程序，URL 重写是可靠且易于实现的。请注意，手动向超链接 URL 附加参数并不常见。更常见的是使用 HTTP 会话 API 来执行 URL 重写，在这种情况下，只会附加一个会话 ID。

## Cookies

最广泛使用的持久化客户端数据存储技术涉及 HTTP cookie。`cookie` 是一个小型的、命名的数据元素，服务器通过 `Set-Cookie` 头将其作为 HTTP 响应的一部分传递给客户端。客户端应存储该 cookie，并在后续对同一服务器的请求中通过 `Cookie` 头将其返回给服务器。除了名称和值外，cookie 还可能包含：

-   一个过期日期，此后客户端将不再保留该 cookie。如果未指定日期，cookie 将在浏览器会话结束时立即过期。
-   一个域名，例如 `servername.com`，它限制了 cookie 有效的 URL 子集。如果未指定，cookie 将随所有对原始 Web 服务器的请求一起返回。
-   一个路径名，进一步限制 URL 子集。
-   一个 `secure` 属性，如果存在，表示仅当连接使用安全通道（如 SSL）时才应返回 cookie。

原始 cookie 规范的详细信息可以在 http://home.netscape.com/newsref/std/cookie_spec.html 找到。图 14-2 说明了如何通过 HTTP 请求和响应设置和检索 cookie。首先，Web 浏览器向 Web 服务器请求一个页面。此时不涉及 cookie。当服务器用请求的文档响应时，它会发送一个 `Set-Cookie` 头，将值 `fr` 分配给名为 `language` 的 cookie。该 cookie 设置为一年后过期。浏览器读取此头，提取 cookie 信息，并将名称/值对与 Web 服务器的域和默认路径一起存储在其 cookie 缓存中。稍后，当用户再次访问该页面时，浏览器识别出它之前从该服务器接收过一个 cookie，并且该 cookie 尚未过期，因此会将 cookie 发送回服务器。Cookie 相对于其他持久化方案的一个优点是，即使在客户端计算机重新启动后，它们也能在浏览器会话结束后保留其值。这使得 cookie 非常适合维护用户的偏好，例如语言。下面显示的应用程序允许用户通过点击超链接选择所需语言。选择会导致两个 cookie 发送到客户端：一个用于语言，一个用于国家/地区。下次用户访问该站点时，浏览器会自动将 cookie 发送回服务器，并且页面中会使用用户的首选语言。

![](img/7a2f73369bb140583c728b73456addb_390_0.png)

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<jsp:include page="getLocale.jsp" flush="true"/>
<%
    ResourceBundle RB =
        (ResourceBundle) request.getAttribute("RB");
%>
<HTML>
<HEAD>
<TITLE>Using Cookies to Store Preferences</TITLE>
</HEAD>
<BODY>
<IMG SRC="images/lyric_note.png"><P>
<HR>
<jsp:include page="languageBar.jsp" flush="true"/>
<H3><%= RB.getString("greeting") %></H3>
</BODY>
</HTML>
```

主应用程序页面 `index.jsp` 使用 `<jsp:include>` 调用一个实用 JSP 页面，该页面扫描请求头中现有的 cookie 并返回适用于相应语言的资源包<sup>2</sup>。这是实用页面 `getLocale.jsp`：

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%
// Look through cookies for language and country

String language = null;
String country  = null;

Cookie[] cookies = request.getCookies();
if (cookies != null) {
    for (int i = 0; i < cookies.length; i++) {
        Cookie cookie = cookies[i];
        String name = cookie.getName();
        if (name.equals("language"))
            language = cookie.getValue();
        if (name.equals("country"))
            country = cookie.getValue();
    }
}

// Get locale-specific resources

Locale locale = null;
```

<sup>2</sup> `java.util.ResourceBundle` 对象是程序以不同语言检索消息和其他字符串的一种方式，因此程序可以在多个区域设置中使用，而无需进行任何更改。`ResourceBundle` 有多种实现，其中最常见的是使用普通的 `.properties` 文件来存储消息文本。



## 会话API

到目前为止，我们已经探讨了两种会话跟踪的基本方法，这两种方法都涉及到客户端对状态的记录：

- 让客户端存储所有会话数据，并在每次请求时将其返回给服务器。
- 让客户端存储一个会话标识符，其余工作由服务器处理。

虽然第一种方法可能更容易实现，但第二种方法通常能提供更好的灵活性和可扩展性。我们已经看到，隐藏字段、URL重写和Cookie在一定程度上都可以用来支持这两种方法。但是，大多数需要使用会话的Servlet和JSP页面都可以利用一种更高层次的方法：*HttpSession* API。

`javax.servlet.http` 包中有三个类构成了会话API：

- **HttpSession** 一个类似于Map或Hashtable的接口，能够按名称存储和检索对象。会话通过调用 `HttpServletRequest.getSession()` 创建，并一直持续到它超时或被参与该会话的Servlet关闭。携带会话标识符的传入HTTP请求会自动与该会话关联。
- **HttpSessionBindingListener** 一个接口，允许对象知晓自己何时被存储到会话中或从会话中移除。该接口有两个回调方法：`valueBound()` 和 `valueUnbound()`，对象必须实现这两个方法才能接收到绑定通知。
- **HttpSessionBindingEvent** 一个传递给 HttpSessionBindingListener 的 `valueBound()` 和 `valueUnbound()` 方法的事件对象。该事件具有返回会话和监听器绑定到会话时所用名称的方法。

## 创建会话

Servlet通过调用HttpServletRequest中的 `getSession()` 或 `getSession(boolean create)` 方法来表明它希望使用会话，如下所示：

```
HttpSession session = request.getSession(true);
```

无参数的 `getSession()` 方法是一个便捷方法，它简单地调用 `getSession(true)`。`create` 参数指示Servlet引擎在尚不存在会话时是否应创建一个新会话。如果参数为 `false`，Servlet只能对现有会话进行操作。在任何一种情况下，都会检查请求是否包含有效的会话ID。如果是，Servlet容器会返回一个会话对象的引用，然后就可以使用它来存储和检索会话属性。

在JSP页面中，会话是自动创建的，除非在页面指令中将其禁用。在生成的Servlet的 `_jspService()` 方法开头，会创建并初始化PageContext对象。作为初始化的一部分，JspFactory.getPageContext() 方法调用 `request.getSession(true)`。当生成的Servlet调用 `pageContext.getSession()` 时，新创建或访问的会话会返回给它。然后，会话作为隐式变量 `session` 对JSP页面的其余部分可用，如下所示：

```
public void _jspService(
        HttpServletRequest request,
        HttpServletResponse response)
    throws ServletException, IOException
    {
        PageContext pageContext = _jspFactory.getPageContext(
            this, request, response, null, true, 8192, true);

        JspWriter out = pageContext.getOut();
        HttpSession session = pageContext.getSession();
        ...
    }
```

如果JSP页面不需要使用会话，它应该在页面指令中禁用自动创建：

```
<%@ page session="false" %>
```

这可以避免Servlet引擎在不需要时创建和维护会话。不必要的会话可能会带来显著的内存消耗。当会话首次创建时，客户端（Web浏览器）还不知道它。当会话ID发送给客户端，并且客户端在下一个请求中将其发送回来时，客户端就被称为 *加入* 了会话。Servlet或JSP页面可以通过 *isNew()* 方法检测这种情况是否已发生：

```
HttpSession session = request.getSession();
if (session.isNew()) {
    // 创建一个空的购物车
}
```

如果会话是新创建的，并且客户端尚未被告知，或者客户端已被告知但选择不参与，则 `session.isNew()` 返回 true。

## 会话跟踪机制

Servlet引擎尝试使用Cookie来跟踪会话ID。在创建会话的Servlet写入的HTTP响应中，一个包含会话ID的 *Set-Cookie* 头位于名为 `JSESSIONID` 的Cookie中。

```
Set-Cookie: JSESSIONID=rkbg6z27j1;Path=/jspcr
```

如果客户端接受Cookie，它会在后续请求中返回该Cookie：

```
Cookie: JSESSIONID=rkbg6z27j1
```

如果发生这种情况，客户端请求就可以与会话关联起来，而Servlet无需特殊处理。但是，如果客户端不接受Cookie，会话就会丢失。为了防止这种情况，Servlet API有一个后备机制。它在Cookie失效时使用URL重写。这对程序员来说稍微复杂一些，因为它意味着Servlet写入的所有URL都必须附加会话ID。

366 JSP: The Complete Reference

```
if (language != null && country != null)
    locale = new Locale(language, country);
if (locale == null)
    locale = Locale.getDefault();

ResourceBundle RB = ResourceBundle.getBundle
    ("jsppcr.sessions.welcome", locale);

// 将资源包存储为请求的一个属性

request.setAttribute("RB", RB);
%>
```

getLocale.jsp 使用 request.getCookies() 获取请求中所有Cookie的数组。它遍历列表查找语言和国家/地区Cookie。如果getLocale.jsp找到它们，它就会为该语言和国家/地区创建一个java.util.Locale。如果未找到Cookie（用户首次访问页面时就是这种情况），则使用默认区域设置。无论哪种方式，它都会加载与此应用程序和区域设置关联的资源包，然后将该包存储为请求属性。从 <jsp:include> 返回后，index.jsp检索该资源包，并使用ResourceBundle.getString()获取翻译后的文本。

index.jsp调用另一个名为languageBar.jsp的工具页面来创建语言选择超链接。每个超链接中存储的都是主页的URL（包括任何参数），以及语言和国家/地区代码。以下是languageBar.jsp：

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%
    String thisURL = HttpUtils.getRequestURL(request).toString();
    thisURL = java.net.URLEncoder.encode(thisURL);

    Object[][] locales = {
        {new Locale("en", "US"), "English"},
        {new Locale("de", "DE"), "Deutsch"},
        {new Locale("es", "ES"), "Español"},
        {new Locale("fr", "FR"), "Français"},
        {new Locale("it", "IT"), "Italiano"},
    };

    for (int i = 0; i < locales.length; i++) {
        Locale locale = (Locale) locales[i][0];
        String name = (String) locales[i][1];

        StringBuffer sb = new StringBuffer();
        if (i > 0)
            sb.append(" | ");
        sb.append("<A HREF=\"setPreferences.jsp?cameFrom=");
        sb.append(thisURL);
        sb.append("&language=");
        sb.append(locale.getLanguage());
        sb.append("&country=");
        sb.append(locale.getCountry());
        sb.append("\"");
        sb.append(">");
        sb.append(name);
        sb.append("</A>");
        out.println(sb);
    }
%>
```

这些超链接会调用setPreferences.jsp，它生成相应的语言和国家/地区Cookie，然后将它们添加到传出的响应头中。接下来，JSP将浏览器重定向回调用页面，如下所示：

```
<%@ page session="false" %>
<%
    // 设置语言和国家/地区Cookie

    final int ONE_YEAR = 60 * 60 * 24 * 365;
    String[] parms = { "language", "country" };
    for (int i = 0; i < parms.length; i++) {
        String name = parms[i];
        String value = request.getParameter(name);
        if (value != null) {
            Cookie cookie = new Cookie(name, value);
            cookie.setMaxAge(ONE_YEAR);
            response.addCookie(cookie);
        }
    }
}

// 重定向回调用的JSP
String cameFrom = request.getParameter("cameFrom");
if (cameFrom == null)
    cameFrom = request.getContextPath();
response.sendRedirect(cameFrom);
%>
```

index.jsp页面最初以默认区域设置显示，如图14-3所示。如果用户点击法语超链接，setPreferences.jsp页面将被调用，它将浏览器重定向回index.jsp，这次带有Cookie。结果显示为该页面的法语版本，如图14-4所示。如果用户第二天再次访问该站点，语言偏好设置会被记住并应用。
Cookie的主要问题是用户能够并且确实会关闭浏览器的Cookie支持，通常是为了隐私原因。这意味着应用程序必须准备好在无法使用Cookie时以其他方式完成其工作。

![](img/7a2f73369bb140583c7288b73456addb_394_0.png)

图14-3. LyricNote主页细节，显示语言选择栏

![](img/7a2f73369bb140583c7288b73456addb_395_0.png)



# 从会话中存储和检索对象

但是，如果客户端接受 cookie，这种做法既不必要又代价高昂，因此 URL 重写只应在你明确知道 cookie 方法失败的情况下才进行。幸运的是，Servlet API 提供了封装所有这些逻辑的方法。`HttpServletResponse` 类有 `encodeURL()` 和 `encodeRedirectURL()` 方法，它们仅在必要时才将会话 ID 添加到 URL 中：

```java
String myURL = response.encodeURL("/servlet/nextServlet");
out.println("Click <A HREF='"
    + myURL + "'>here</A>"
    + " to continue");
```

`encodeRedirectURL()` 应与传递给 `response.sendRedirect()` 方法的 URL 一起使用，而 `encodeURL()` 则用于所有其他情况。

当使用 `encodeURL()` 方法时，如果 `session.isNew()` 为真，则会话 ID 总是嵌入 URL 中。在客户端第一次响应后，Servlet 引擎会确定会话 ID 是否通过 cookie 返回。如果没有，Servlet 引擎会继续将 ID 附加到通过 `encodeURL()` 传递的 URL 中。否则，它会切换到仅使用 cookie 的模式，而 `encodeURL()` 将返回未经修改的 URL 字符串。这使得程序员无需测试所有可能的情况。

对象通过 `setAttribute()` 方法绑定到会话：

```java
session.setAttribute("jspcr.sessions.myapp.user", userID);
```

对象绑定的名称可以是任何唯一的字符串。然而，由于会话在当前 HTTP 会话的所有 Servlet 和 JSP 页面之间是共享的，使用不会与其他应用程序冲突的名称是有意义的。最常见的做法是选择一个以 Servlet 或 JSP 页面的包名或完全限定类名为前缀的名称。

任何类型的对象都可以存储在会话中，但由于会话可能被序列化，一个好的做法是让会话对象实现 `java.io.Serializable`。还要注意，只能存储对象，而不能存储基本类型如 `int`、`char` 或 `double`。要存储这些基本类型，必须使用它们的对象包装器 `Integer`、`Character` 或 `Double`。

对象可以通过 `getAttribute()` 方法从会话中检索：

```java
String userID = (String) session.getAttribute(
    "jspcr.sessions.myapp.user");
```

与 `Map` 或 `Hashtable` 类似，会话只存储对象，因此当它们被检索时，必须被转换为适当的类型。包装器类中包含的基本类型必须通过包装器类提供的方法来提取：

```java
Integer countObject = (Integer) getAttribute("count");
int count = countObject.intValue();
```

通常，如果你在会话中存储了一个属性，你就知道它的名称和类型，并且你可以直接以这种方式请求它。你也可以从 `getAttributeNames()` 方法获取属性名称列表：

```java
out.println("Objects in this session:");
out.println("<PRE>");
Enumeration enames = session.getAttributeNames();
while (enames.hasMoreElements()) {
    String name = (String) enames.nextElement();
    Object value = session.getAttribute(name);
    out.println(name + " = " + value);
}
out.println("</PRE>");
```

当对象不再需要时，可以使用 `removeAttribute()` 从会话中移除：

```java
session.removeAttribute("jspcr.sessions.myapp.user");
```

当会话关闭时，这会自动发生，但可能有些情况需要比这更早地移除属性。

# 销毁会话

会话一旦创建，通常会一直存在，直到超时或关闭。超时指的是会话在请求之间的最长有效时间。这是一个重要的考虑因素，因为服务器无法知道客户端是否已完成会话的使用，除非被明确告知或等待固定的时间长度。

默认的超时间隔可以在部署描述符 `web.xml` 中设置：

```xml
<web-app>
    ...
    <session-config>
        <session-timeout> 30 </session-timeout>
    </session-config>
    ...
</web-app>
```

间隔以分钟为单位指定，30 是默认值。此处输入的值适用于应用程序中的所有会话，除非它们单独覆盖它。

一些使用稀缺资源（如数据库连接）的应用程序可能会选择更短的超时时间。这些应用程序可以使用 `setMaxInactiveInterval()` 方法选择更短的时间段：

```java
session.setMaxInactiveInterval(180);
```

传递给 `setMaxInactiveInterval()` 的参数是以秒为单位的数字${}^4$。上一个示例使用了 180 秒或三分钟。当前值可以通过 `getMaxInactiveInterval()` 获取。如果指定负值，会话将永不超时。

在某些情况下，可以提供会话的明确结束。在这些情况下，可以使用 `invalidate()` 方法：

```java
session.invalidate();
```

此方法将会话标记为非活动状态，并解除绑定到它的所有对象。例如，在一个使用会话存储订购物品的购物车应用程序中，在结账逻辑将订单写入数据库后，会话应该被销毁，这样如果用户购买更多物品，旧的会话内容就不会仍然存在。

# 示例回顾

会话 API 可以处理本章前面描述的所有会话跟踪任务。在本节中，你将学习如何使用相同的会话 API 方法来实现隐藏字段、URL 重写和 cookie 示例。

# 隐藏字段示例——数字猜测者

在隐藏字段部分开发的数字猜测者可以通过将所有隐藏字段移动到一个存储在 HTTP 会话中的对象来简化。本示例中的对象是一个名为 `Parameters` 的内部类，它在 JSP 页面顶部附近定义，但它也可以是一个外部定义的类。

```jsp
<%@ page session="true" %>
<H3>Number Guess Guesser</H3>
<%!
public static final int WAY_LO = 0;
public static final int WAY_HI = 101;
public static final String PARMSKEY
    = "jspcr.sessions.numguess.parameters";

// Inner class containing state variables

public class Parameters {
    int lo;
    int hi;
    int numGuesses;
    int state;
}
%>
<%
    Parameters parms=(Parameters) session.getAttribute(PARMSKEY);
    if (parms == null) {
        parms = new Parameters();
        parms.state = 0;
        session.setAttribute(PARMSKEY, parms);
    }

    switch (parms.state) {
        case 0: {   // Initial screen
%>
<FORM>
Think of a number between
<%= WAY_LO + 1 %> and <%= WAY_HI - 1 %>,
and I'll try to guess it.<P>
Click OK when ready.<P>
<INPUT TYPE="submit" VALUE="OK">
</FORM>
<%
            parms.lo = WAY_LO;
            parms.hi = WAY_HI;
            parms.numGuesses = 0;
            parms.state = 1;
            break;
        }
        case 1: {   // First guess
            parms.numGuesses++;
            int guess = (parms.hi + parms.lo)/2;
%>
<FORM>
My first guess is <%= guess %>. How did I do?<P>
<INPUT TYPE="radio"
    NAME="result"
    VALUE="-1" onClick="submit()"> Too low
<INPUT TYPE="radio"
    NAME="result"
    VALUE="0" onClick="submit()"> Exactly right
<INPUT TYPE="radio"
    NAME="result"
    VALUE="1" onClick="submit()"> Too high
</FORM>
<P>
<%
    parms.state = 2;
    break;
}
case 2: {   // After first guess
    parms.numGuesses++;
    int result =
        Integer.parseInt(request.getParameter("result"));
    int guess = (parms.hi + parms.lo)/2;

    if (result < 0) {
        parms.lo = guess;
        guess = (parms.hi + parms.lo)/2;
    }
    else if (result > 0) {
        parms.hi = guess;
        guess = (parms.hi + parms.lo)/2;
    }

    if (result != 0) {
%>
<FORM>
<%
    if (parms.lo > WAY_LO)
        out.println(parms.lo + " is too low.<BR>");
    if (parms.hi < WAY_HI)
        out.println(parms.hi + " is too high.<BR>");
    if ((parms.hi - parms.lo) > 1) {
%>
My next guess is <%= guess %>. How did I do?<P>
<INPUT TYPE="radio"
       NAME="result"
       VALUE="-1" onClick="submit()"> Too low
<INPUT TYPE="radio"
       NAME="result"
       VALUE="0" onClick="submit()"> Exactly right
<INPUT TYPE="radio"
       NAME="result"
       VALUE="1" onClick="submit()"> Too high
</FORM>
<%
}
else {
    String[] text = {
        "Are we cheating?",
        "Did we forget our number?",
        "Perhaps we clicked the wrong button?",
        "What happened?",
        "What gives?",
    };
    String message = text[(int) (Math.random() * text.length)];
    session.removeAttribute(PARMSKEY);
%>
<FORM>
<%= message %><P>
<INPUT TYPE="SUBMIT" VALUE="Start Over">
</FORM>
<%
}
    }
    else {
        parms.numGuesses--;
%>
<FORM>
I win, and after only <%= parms.numGuesses %> guesses!<P>
Do you want to try again?<P>
<INPUT TYPE="SUBMIT" VALUE="Start Over">
</FORM>
<%
        session.removeAttribute(PARMSKEY);
    }
    }
%>
```



逻辑保持不变，但原本写入HTML表单的隐藏字段，其值现在存储在与会话绑定的**Parameter**对象中。

## URL重写示例—页面计数器

同样，URL重写部分开发的页面计数器可以使用HTTP会话来存储计数变量。因为`int`是基本类型，所以使用`Integer`对象包装器，并调用其`intValue()`方法来获取实际值。

```
<%@ page session="true" %>
<HTML>
<HEAD>
<TITLE>Page Counter Using HTTP Session</TITLE>
</HEAD>
<BODY>
<H3>Page Counter Using HTTP Session</H3>
<%
    if (session.getAttribute("count") == null)
        session.setAttribute("count", new Integer(0));

    int count=((Integer) session.getAttribute("count")).intValue();

    switch (count) {
        case 0:
%> This is the first time you have accessed this page. <%
            break;
        case 1:
%> You have accessed the page once before.<%
            break;
        default:
%> You have accessed the page <%= count %> times before.<%
            break;
    }

    session.setAttribute("count", new Integer(count+1));
%>
<P>
Click
<A HREF="<%= response.encodeURL("Counter.jsp") %>">here</A>
to visit the page again.
</BODY>
</HTML>
```

每次刷新页面时，计数都会递增，并以新的`Integer`包装器形式存储在会话中。请注意，用户点击以重新显示页面的超链接使用了`response.encodeURL()`，以确保无论用户是否接受Cookie，会话跟踪都能正常工作。

## Cookies示例—语言偏好

在Cookies部分，你了解了应用程序如何允许用户指定其语言偏好，以便在该会话的其余网页中以该语言显示。该应用程序使用了Cookie，以便该偏好设置即使在会话之间也能保持。如果不需要这种持久性，使用会话API也可以完成同样的事情。
主要的`index.jsp`页面变化不大。它仍然使用资源包来获取消息文本，但现在是将其作为会话属性获取，而不是请求属性。另外，请注意页面指令现在是`session="true"`。

```
<%@ page session="true" %>
<%@ page import="java.util.*" %>

<%-- Get the appropriate resource bundle from the session --%>

<jsp:include page="getLocale.jsp" flush="true"/>
<%
    ResourceBundle RB = (ResourceBundle)
        session.getAttribute("RB");
%>

<HTML>
<HEAD>
<TITLE>Using Session API to Store Language Preference</TITLE>
</HEAD>
<BODY>
<IMG SRC="images/lyric_note.png"><P>
<HR>
<%-- Show a row of hyperlinks with language choices --%>

<jsp:include page="languageBar.jsp" flush="true"/>

<%-- Display greeting in appropriate language --%>

<H3><%= RB.getString("greeting") %></H3>

</BODY>
</HTML>
```

包含的模块—`getLocale.jsp`和`setPreferences.jsp`—是实际发生变化的地方。`setPreferences`现在可以根据接收到的语言和国家参数，实际加载相应的资源包。

```
<%@ page session="true" %>
<%@ page import="java.util.*" %>
<%
    // Get parameters for language and country

    String language = request.getParameter("language");
    String country = request.getParameter("country");

    // Get locale-specific resources

    Locale locale = null;
    if (language != null && country != null)
        locale = new Locale(language, country);
    if (locale == null)
        locale = Locale.getDefault();

    ResourceBundle RB = ResourceBundle.getBundle
        ("jspcr.sessions.welcome", locale);

    // Store the resource bundle as an attribute in the session

    session.setAttribute("RB", RB);

    // Redirect back to the calling JSP

    String cameFrom = request.getParameter("cameFrom");

    if (cameFrom == null)
        cameFrom = request.getContextPath();

    cameFrom = response.encodeRedirectURL(cameFrom);

    response.sendRedirect(cameFrom);
%>
```

资源包作为会话属性存储，用户被重定向回原始页面。请注意，“cameFrom” URL通过了`encodeRedirectURL()`方法处理，以防Cookie被关闭。
`getLocale` JSP页面现在可以简单地在会话中查找资源包，如果找不到则使用默认资源包。

```
<%@ page session="true" %>
<%@ page import="java.util.*" %>
<%
    // Get the existing resource bundle from the session,
    // if one exists

    ResourceBundle RB = (ResourceBundle)
        session.getAttribute("RB");

    // If not, use the default resource bundle

    if (RB == null) {
        RB = ResourceBundle.getBundle("jspcr.sessions.welcome");
        session.setAttribute("RB", RB);
    }
%>
```

`languageBar.jsp`页面只需要在两处做一个改动。因为它为主页面和`setPreferences.jsp`编写URL，所以需要将这些URL通过`response.encodeURL()`处理，以便即使Cookie被关闭，会话跟踪也能工作：

```
<%@ page session="true" %>
<%@ page import="java.util.*" %>
<%
    String thisURL = HttpUtils.getRequestURL(request).toString();
    // Encode the session ID into the URL, if necessary
    thisURL = response.encodeURL(thisURL);
    thisURL = java.net.URLEncoder.encode(thisURL);

    Object[][] locales = {
        {new Locale("en", "US"), "English"},
        {new Locale("de", "DE"), "Deutsch"},
        {new Locale("es", "ES"), "Español"},
        {new Locale("fr", "FR"), "Français"},
        {new Locale("it", "IT"), "Italiano"},
    };

    for (int i = 0; i < locales.length; i++) {

        Locale locale = (Locale) locales[i][0];
        String name   = (String) locales[i][1];

        StringBuffer sb = new StringBuffer();
        if (i > 0)
            sb.append(" | ");
        sb.append("<A HREF=\"" );

        // Encode the session ID into the generated URL

        StringBuffer sb2 = new StringBuffer();
        sb2.append("setPreferences.jsp?cameFrom=");
        sb2.append(thisURL);
        sb2.append("&language=");
        sb2.append(locale.getLanguage());
        sb2.append("&country=");
        sb2.append(locale.getCountry());
        String url = sb2.toString();
        url = response.encodeURL(url);

        sb.append(url);
        sb.append("\"" );
        sb.append(">");
        sb.append(name);
        sb.append("</A>");
        out.println(sb);
    }
%>
```

## 会话绑定监听器

会话API提供了一种机制，让对象可以跟踪它们何时被添加到会话或从会话中移除。希望接收这些事件通知的对象可以实现`HttpSessionBindingListener`接口。实现类必须提供两个方法：

-   public void valueBound(HttpSessionBindingEvent event)
-   public void valueUnbound(HttpSessionBindingEvent event)

在这两种情况下，都会将一个`HttpSessionBindingEvent`实例传递给这些方法。`event`参数具有检索会话以及确定对象绑定到会话所用名称的方法。
会话绑定监听器的主要优势在于，无论客户端是显式关闭应用程序还是会话超时，它们都能释放所获取的资源。这使得该接口在管理数据库连接时非常有用。JDBC 2.0提供了连接池功能，但许多驱动程序尚未实现。在这种情况下，一个驻留在会话中、知道在合适时机断开自身的连接是一个可行的替代方案。
以下示例说明了这种技术。`BoundConnection`是`java.sql.Connection`对象的包装器，并实现了`HttpSessionBindingListener`，因此它可以在连接不再使用后关闭连接。

```
package jspcr.jdbc;

import java.io.*;
import java.sql.*;
import java.text.*;
import java.util.*;
import javax.servlet.*;
import javax.servlet.http.*;

/**
 * A wrapper for a <CODE>Connection</CODE>
 * object that is aware it is in an HTTP session.
 * This enables it to shut down the connection
 * when the session is destroyed.
 */
public class BoundConnection
    implements HttpSessionBindingListener, Serializable
{
```



private transient Connection connection;

/**
 * 创建一个新的 <CODE>BoundConnection</CODE> 对象，
 * 用于指定的连接。
 * @param con 连接对象
 */
public BoundConnection(Connection con)
{
    this.connection = con;
}

/**
 * 返回底层的连接对象
 */
public Connection getConnection()
{
    return connection;
}

/**
 * 当 <CODE>BoundConnection</CODE>
 * 被存储到 HTTP 会话中时调用
 * @param event 绑定事件
 */
public void valueBound(HttpSessionBindingEvent event)
{
    trace("bound", event);
}

/**
 * 当 <CODE>BoundConnection</CODE>
 * 从 HTTP 会话中移除时调用
 * @param event 解绑事件
 */
public void valueUnbound(HttpSessionBindingEvent event)
{
    if (connection != null)
        try {
            connection.close();
            connection = null;
        }
        catch (SQLException e) {
            e.printStackTrace();
        }
    trace("unbound", event);
}

/**
 * 打印跟踪消息
 */
private void trace(String s, HttpSessionBindingEvent event)
{
    HttpSession session = event.getSession();

    java.util.Date now = 
        new java.util.Date(System.currentTimeMillis());
    java.util.Date last = 
        new java.util.Date(session.getLastAccessedTime());

    SimpleDateFormat fmt = new SimpleDateFormat("hh:mm:ss");
    StringBuffer sb;

    sb = new StringBuffer();
    sb.append("TRACE: ");
    sb.append(fmt.format(now));
    sb.append(" session ");
    sb.append(session.getId());
    sb.append(" last accessed time ");
    sb.append(fmt.format(last));
    System.err.println(sb.toString());

    sb = new StringBuffer();
    sb.append("TRACE: ");
    sb.append(fmt.format(now));
    sb.append(" session ");
    sb.append(session.getId());
    sb.append(" connection ");
    sb.append(s);
    System.err.println(sb.toString());
}
}

`BoundConnection` 构造函数将一个 `Connection` 对象存储为私有实例变量，并通过 `getConnection()` 方法使其可访问。`BoundConnection` 实现了 `HttpSessionBindingListener` 的两个方法：

### 386 JSP: 完全参考手册

`valueBound()` 和 `valueUnbound()`。在每个方法中，它都会写入一条跟踪消息，因此存在一条记录，显示连接是何时绑定或解绑的。关键特性是 `valueUnbound()` 方法，它关闭底层的连接。

> **注意** `BoundConnection` 对象实现了 `Serializable`，因为会话可能被序列化，特别是在可分布式应用程序中。这使得将 `Connection` 实例变量标记为 `transient` 成为必要，这样 servlet 容器就不会尝试对其进行序列化。因此，`getConnection()` 的调用者需要检查返回值是否为 `null`，并在必要时创建一个新的 `BoundConnection`。

因此，一个使用 `BoundConnection` 的 JSP 页面可以在会话开始时调用它，为其提供一个新打开的数据库连接。当一个 `BoundConnection` 被存储到会话中时，它的 `valueBound()` 方法会被触发。同一会话中的后续请求可以简单地从会话中检索 `BoundConnection` 并调用其 `getConnection()` 方法来获取底层的 `java.sql.Connection`。以下所示的可重用 `connect.jsp` 模块实现了此逻辑。

```
<%@ page import="java.sql.*" %>
<%@ page import="jspcr.jdbc.*" %>
<%
    // 如果当前会话尚未绑定连接，则创建一个

    if (session.getAttribute("bcon") == null) {

        String driver =
            application.getInitParameter("jdbc.driver");
        String url =
            application.getInitParameter("jdbc.url.internal");

        Class.forName(driver);
        Connection con = DriverManager.getConnection(url);

        // 将连接绑定到此会话

        BoundConnection bcon = new BoundConnection(con);
        session.setAttribute("bcon", bcon);

        // 设置超时间隔为三分钟

        session.setMaxInactiveInterval(180);
    }
%>
```

## 第14章：会话与线程管理

除了在必要时创建 `BoundConnection`，`connect.jsp` 还将会话超时间隔设置为三分钟。

以下所示的应用程序使用 `BoundConnection` 为重复的数据库查询提供快速访问。`ComposerSearch.jsp` 提示输入国籍和世纪，然后搜索 LyricNote 作曲家数据库并显示结果。它包含 `connect.jsp` 以执行实际的连接和会话绑定工作。

```
<%@ page session="true" %>
<%@ page import="jspcr.jdbc.*" %>
<%@ page import="java.sql.*" %>
<%
  // 获取表单参数或使用默认值

  String nationality = request.getParameter("nationality");
  if (nationality == null)
    nationality = "";

  String yearRange = request.getParameter("yearRange");
  if (yearRange == null)
    yearRange = "1901-2000";
%>
<HTML>
<HEAD>
<TITLE>Composer Search</TITLE>
</HEAD>
<BODY>
<CENTER>
<H3>Composer Search</H3>
<FORM METHOD="POST">
<B>Nationality:</B>
<INPUT TYPE="TEXT" NAME="nationality" VALUE="<%= nationality %>">
<B>Century:</B>
<SELECT NAME="yearRange">
<%
  // 创建世纪选项列表

  for (int century = 16; century <= 20; century++) {
    int fromYear = (century - 1) * 100 + 1;
    int toYear = century * 100;
    StringBuffer sb = new StringBuffer();
    sb.append("<OPTION");
    if (yearRange.startsWith("" + fromYear))
      sb.append(" SELECTED");
    sb.append(" VALUE='");
    sb.append(fromYear);
    sb.append("-");
    sb.append(toYear);
    sb.append("'>");
    sb.append(century);
    sb.append("th Century</OPTION>");
    out.println(sb);
}
%>
</SELECT>
<INPUT TYPE="SUBMIT" VALUE="Search">
</FORM>
<%
// 如果在表单中输入了值，则显示结果

if (!nationality.equals("")) {
%>

<%-- 获取绑定的连接 --%>

<jsp:include page="connect.jsp" flush="true"/>

<TABLE BORDER=0 CELLPADDING=1 CELLSPACING=1>
<%
    BoundConnection bcon = (BoundConnection)
        session.getAttribute("bcon");
    Connection con = bcon.getConnection();
    String sql = ""
        + " SELECT   lname, fname, born, died"
        + " FROM     composers"
        + " WHERE    nationality = ?"
        + " AND      ((born between ? and ?)"
        + " OR       (died between ? and ?))"
        + " ORDER BY born, lname"
        ;
    PreparedStatement pstmt = con.prepareStatement(sql);

    int fromYear = Integer.parseInt(yearRange.substring(0, 4));
    int toYear = Integer.parseInt(yearRange.substring(5));

    pstmt.setString(1, nationality);
    pstmt.setInt(2, fromYear);
    pstmt.setInt(3, toYear);
    pstmt.setInt(4, fromYear);
    pstmt.setInt(5, toYear);
    ResultSet rs = pstmt.executeQuery();
    while (rs.next()) {
        String lname = rs.getString(1);
        String fname = rs.getString(2);
        int born = rs.getInt(3);
        int died = rs.getInt(4);
%>
<TR>
    <TD><%= fname %> <%= lname %></TD>
    <TD><%= born %>-<%= died %></TD>
</TR>
<%
}
rs.close();
pstmt.close();
%>
</TABLE>
<%
}
%>
</CENTER>
</BODY>
</HTML>
```

要访问驻留在会话中的连接，应用程序只需检索 `bcon` 会话属性，将其转换为 `BoundConnection`，并调用其 `getConnection()` 方法即可。注意，没有必要显式关闭连接。当客户机在三分钟内没有进一步请求时，连接会自动关闭。生成的 Web 页面（如图 14-5 所示）可用于重复查询，仅首次查询需要新的连接。`System.err` 日志中的跟踪条目显示了 `BoundConnection` 在 HTTP 会话中的生命周期：

```
TRACE: 07:55:00 session 8720188469 last accessed time 07:55:00
TRACE: 07:55:00 session 8720188469 connection bound
TRACE: 07:59:38 session 8720188469 last accessed time 07:56:38
TRACE: 07:59:38 session 8720188469 connection unbound
```

连接在 07:55:00 绑定到会话，并被使用了一次或多次，最后一次使用是在 07:56:38。三分钟后，在 07:59:38，会话超时，解绑了 `BoundConnection` 对象。这又导致 `valueUnbound()` 方法被调用，该方法关闭了底层的连接。

### 线程管理

Servlet 和 JSP 页面相对于旧的服务器端技术有一个显著优势，因为它们被加载到内存中，并在多线程环境中作为单个实例运行。然而，这种好处伴随着一个权衡。多线程模型

引入了在更简单的应用模型中不存在的困难。例如，如果一个servlet有实例变量，它们可能会同时被不同的请求访问。如果两个请求都对这些变量进行写操作，它们的值可能是不可预测的。

幸运的是，由于servlet引擎是用Java编写的，它可以利用Java内置的多线程应用程序支持。在本节中，你将学习一些基本的线程概念，研究两种servlet线程模型，并考虑一个高效的多线程应用程序。

## 线程概念

*线程*是具有自己的栈和程序计数器的单一顺序控制流。使用多个线程的程序看起来像是在同时做不止一件事。一个线程能够在同一进程中独立于其他线程操作，同时共享所有进程对象。

Web服务器本身是线程可以发挥效用的一个例子。一个简单的Web服务器操作如下：

1.  创建一个`ServerSocket`并调用其`accept()`方法来等待HTTP客户端请求。
2.  获取`accept()`方法返回的客户端`Socket`对象，并启动一个单独的线程来处理其请求。
3.  返回步骤1以在另一个线程处理最后一个请求的同时接受更多请求。

Java（不仅限于JSP页面）通常使得创建和使用多个线程变得容易。语言和类库都是从底层开始就考虑到线程来构建的。`java.lang.Object`，所有对象的最终基类，具有用于同步线程操作的方法，这些方法被每个Java对象继承。

一个线程由`java.lang.Thread`类的实例表示。一个新的`Thread`对象实际上在调用其`start()`方法之前并不与底层操作系统线程关联，这允许在其启动之前设置其属性（名称、优先级等）。`start()`方法被调用后，Java虚拟机创建一个操作系统线程，该线程开始执行线程的`run()`方法。一个`Thread`持续运行直到其`run()`方法返回或其`interrupt()`方法被调用。

## 创建和启动线程

有三种启动新线程的技术可用。第一种是子类化`Thread`并重写其`run()`方法。然后可以创建并单独启动该类的对象。下面的`Example1.java`演示了这种技术。它使用一个名为`CounterThread`的`Thread`子类来计数到八，在每次迭代时打印线程名称和时间，并在迭代之间等待随机的时间长度。

```java
import java.text.*;
import java.util.*;

/**
 * 一个演示简单多线程的类
 */
public class Example1
{
    public static void main(String[] args)
    {
        /**
         * 创建、命名并启动两个计数线程
         */
        Thread t1 = new CounterThread();
        t1.setName("A");
        t1.start();

        Thread t2 = new CounterThread();
        t2.setName("B");
        t2.start();
    }
}

/**
 * 一个计数到八的线程，在迭代之间
 * 等待随机的时间长度。
 */
class CounterThread extends Thread
{
    /**
     * 消息中使用的日期格式。包含毫秒。
     */
    public static final SimpleDateFormat FMT
            = new SimpleDateFormat("hh:mm:ss.SSS aa");

    /**
     * 在新线程中启动run方法
     */
    public void start()
    {
        System.out.println("Starting " + getName());
        super.start();
    }

    /**
     * 计数器循环发生的地方。
     */
    public void run()
    {
        for (int i = 0; i < 8; i++) {
            try {
                sleep((long) (Math.random() * 500 + 100));
            }
            catch (InterruptedException e) {
                break;
            }
            System.out.println
                (FMT.format(new Date())
                 + " Thread " + getName()
                 + ": Count = " + i);
        }
        System.out.println("Leaving " + getName());
    }
}
```

主程序启动两个名为A和B的CounterThread实例。以下程序输出显示两个线程同时执行，并且它们的迭代偶尔重叠：

```
Starting A
Starting B
09:55:40.465 PM Thread B: Count = 0
09:55:40.545 PM Thread A: Count = 0
09:55:40.615 PM Thread B: Count = 1
09:55:40.846 PM Thread A: Count = 1
09:55:41.056 PM Thread B: Count = 2
09:55:41.346 PM Thread B: Count = 3
09:55:41.366 PM Thread A: Count = 2
09:55:41.687 PM Thread A: Count = 3
09:55:41.717 PM Thread B: Count = 4
09:55:41.847 PM Thread B: Count = 5
09:55:41.967 PM Thread B: Count = 6
09:55:42.017 PM Thread A: Count = 4
09:55:42.137 PM Thread B: Count = 7
Leaving B
09:55:42.268 PM Thread A: Count = 5
09:55:42.428 PM Thread A: Count = 6
09:55:42.848 PM Thread A: Count = 7
Leaving A
```

第二种技术是让一个类实现`Runnable`接口。在这种情况下，该类必须提供自己的`run()`方法，并创建一个`Thread`对象来执行实际工作。该类必须在`Thread`构造函数中传递对其自身的引用（使用`this`变量）。下面的`Example2.java`展示了这种技术的实际应用。它紧密模仿`Example1`，创建两个线程并将每个线程的`this`变量传递给它。注意，两个线程可以同时运行相同的`run()`方法。

```java
import java.text.*;
import java.util.*;

/**
 * 一个演示使用Runnable接口的
 * 简单多线程的类。
 */
public class Example2 implements Runnable
{
    public static void main(String[] args)
    {
        new Example2();
    }

    public Example2()
    {
        /**
         * 启动两个使用此run方法的Runnable线程。
         */

        Thread t1 = new Thread(this);
        t1.setName("A");
        t1.start();

        Thread t2 = new Thread(this);
        t2.setName("B");
        t2.start();
    }

    /**
     * 消息中使用的日期格式。包含毫秒。
     */

    public static final SimpleDateFormat FMT
        = new SimpleDateFormat("hh:mm:ss.SSS aa");

    /**
     * 计数器循环发生的地方。
     */
    public void run()
    {
        Thread t = Thread.currentThread();
        System.out.println("Starting " + t.getName());
        for (int i = 0; i < 8; i++) {
            try {
                t.sleep((long) (Math.random() * 500 + 100));
            }
            catch (InterruptedException e) {
                break;
            }
            System.out.println
                (FMT.format(new Date())
                 + " Thread " + t.getName()
                 + ": Count = " + i);
        }
        System.out.println("Leaving " + t.getName());
    }
}
```

Example2的输出与Example1的输出类似：

```
Starting main
Starting A
10:10:54.269 PM Thread A: Count = 0
10:10:54.299 PM Thread main: Count = 0
10:10:54.620 PM Thread main: Count = 1
10:10:54.690 PM Thread A: Count = 1
10:10:54.980 PM Thread main: Count = 2
10:10:55.180 PM Thread A: Count = 2
10:10:55.351 PM Thread A: Count = 3
10:10:55.461 PM Thread main: Count = 3
10:10:55.671 PM Thread A: Count = 4
10:10:55.811 PM Thread A: Count = 5
10:10:56.042 PM Thread main: Count = 4
10:10:56.272 PM Thread main: Count = 5
10:10:56.382 PM Thread A: Count = 6
10:10:56.753 PM Thread main: Count = 6
10:10:56.773 PM Thread A: Count = 7
Leaving A
10:10:56.943 PM Thread main: Count = 7
Leaving main
```

使用`Runnable`接口的一个缺点是，它是一个只有一个`run()`方法的类，因此无论创建多少线程，它只能执行一种后台操作。例如，一个既要执行动画又要监听套接字或输入流的应用程序，无法通过实现`Runnable`来完成。

Java 2引入了第三种启动线程的技术，即`java.util.Timer`和`java.util.TimerTask`类。`Timer`类充当延迟或重复任务的调度器。这些任务必须扩展`TimerTask`类并提供`run()`方法。任务通过`Timer.scheduleTask()`方法的几种形式之一安排执行。与另外两种方法不同，`TimerTask`的`run()`方法通常不包含执行循环，因为`Timer`可以自动调度重复任务的执行。下面的`Example3.java`展示了使用`Timer`和`TimerTask`完成的计数器示例。

```java
import java.text.*;
import java.util.*;

/**
 * 一个演示使用java.util.Timer的
 * 简单多线程的类
 */
public class Example3
{
    public static void main(String[] args)
    {
        /**
```



## 第14章：会话与线程管理

```java
/*
 * 创建一个计时器来控制计时任务
 */
Timer timer = new Timer();

/**
 * 创建两个计时任务并调度
 * 它们以半秒为间隔执行，
 * 将第二个任务的开始延迟250毫秒
 */
TimerTask t1 = new CounterTimerTask("A");
timer.schedule(t1, 0, 500);

TimerTask t2 = new CounterTimerTask("B");
timer.schedule(t2, 250, 500);
}
}

/**
 * 一个计数到八的TimerTask
 */
class CounterTimerTask extends TimerTask
{
    /**
     * 消息中使用的日期格式。包含毫秒。
     */
    public static final SimpleDateFormat FMT
            = new SimpleDateFormat("hh:mm:ss.SSS aa");

    private String name;
    private int counter;

    public CounterTimerTask(String name)
    {
        this.name = name;
        this.counter = 0;
    }

    /**
     * 计数循环发生的地方。
     */
    public void run()
    {
        if (counter == 0)
            System.out.println("Starting " + name);

        System.out.println
            (FMT.format(new Date())
            + " Thread " + name
            + ": Count = " + counter);

        counter++;
        if (counter >= 8) {
            System.out.println("Leaving " + name);
            cancel();
        }
    }
}
```

`CounterTimerTask` 对象跟踪其被调用的次数，并在达到迭代限制时调用自己的 `cancel()` 方法。由于 `Example3` 对每个任务使用了固定的时间表，计数消息大约每隔四分之一秒交替出现：

```
Starting A
10:57:44.209 PM Thread A: Count = 0
Starting B
10:57:44.460 PM Thread B: Count = 0
10:57:44.710 PM Thread A: Count = 1
10:57:44.961 PM Thread B: Count = 1
10:57:45.211 PM Thread A: Count = 2
10:57:45.461 PM Thread B: Count = 2
10:57:45.712 PM Thread A: Count = 3
10:57:45.962 PM Thread B: Count = 3
10:57:46.212 PM Thread A: Count = 4
10:57:46.463 PM Thread B: Count = 4
10:57:46.713 PM Thread A: Count = 5
10:57:46.963 PM Thread B: Count = 5
10:57:47.214 PM Thread A: Count = 6
10:57:47.464 PM Thread B: Count = 6
10:57:47.715 PM Thread A: Count = 7
Leaving A
10:57:47.965 PM Thread B: Count = 7
Leaving B
```

## 同步线程

多线程应用程序通常包含必须由单个线程执行的操作，或者需要多个线程协作执行的操作。为了实现这一点，必须存在一种保护代码临界区的方法，这样两个线程就不会同时执行它们。

为了说明为什么这是必要的，请看以下程序示例。该程序为一个计费应用发布发票号码。最后使用的发票号码存储在一个文本文件中。一个新发票号码是在一个读取文件、将发票号码加一并写回磁盘的方法中分配的。该程序启动五个线程来模拟多个在线用户在随机时间访问发票编号例程。这个演示中的发票处理只是打印线程的名称和分配给它的发票号码。看看你能否发现这个漏洞：

```java
import java.io.*;
import java.net.*;
import java.util.*;

/**
 * 一个线程同步问题的插图
 */
public class SynchTest implements Runnable
{
    public static void main(String args[])
    {
        new SynchTest();
    }

    /**
     * 创建一个新的SynchTest对象，该对象启动
     * 五个发票处理线程。
     */
    public SynchTest()
    {
        Thread[] threads = {
            new Thread(this, "A"),
            new Thread(this, "B"),
            new Thread(this, "C"),
            new Thread(this, "D"),
            new Thread(this, "E"),
        };
        for (int i = 0; i < threads.length; i++)
            threads[i].start();
    }

    /**
     * 模拟处理十张发票。这个方法将由
     * 五个线程中的每一个运行。
     */
    public void run()
    {
        try {
            for (int i = 0; i < 10; i++) {
                handleInvoice();
                Thread.sleep((long) (Math.random()*500));
            }
        }
        catch (InterruptedException ignore) {
        }
        catch (IOException e) {
            e.printStackTrace();
        }
    }

    /**
     * 发票处理方法（有一个微妙的漏洞）
     */
    public void handleInvoice()
        throws IOException
    {
        Thread t = Thread.currentThread();

        // 从invoice.dat获取最后使用的发票号码
        BufferedReader in =
            new BufferedReader(
                new FileReader("invoice.dat"));
        int invoiceNumber = Integer.parseInt(in.readLine());
        in.close();

        // 加1得到当前发票号码
        invoiceNumber++;
        System.out.println
            (t.getName() + " handles invoice " + invoiceNumber);

        // 更新发票号码
        PrintWriter out =
            new PrintWriter(
                new FileWriter("invoice.dat"));
        out.println(invoiceNumber);
        out.flush();
        out.close();
    }
}
```

程序可能运行多次都没有任何问题，为每个线程分配连续的发票号码。但过一段时间后，会出现如下输出：

```
A handles invoice 68401
B handles invoice 68402
C handles invoice 68403
D handles invoice 68404
E handles invoice 68405
E handles invoice 68406
D handles invoice 68407
A handles invoice 68408
D handles invoice 68409
B handles invoice 68410
B handles invoice 68411
E handles invoice 68412
C handles invoice 68412
B handles invoice 68413
D handles invoice 68414
E handles invoice 68415
B handles invoice 68416
B handles invoice 68417
A handles invoice 68418
```

发票号码68412在列表中出现了两次，被分配给了线程E和线程C。发生了什么？

问题在于：从读取发票号码到将其重写到 `invoice.dat` 文件的这个时间间隔内，另一个执行相同方法的线程可能正在读取该文件并获取旧号码。这个线程然后可以递增它并更新文件，但这样就可能导致发票号码重复。

为了防止这种情况，Java提供了一种获取所有线程都尊重的对象的排他锁的方法。这种锁定机制称为 *同步*，由 `synchronized` 关键字触发。可以使用以下语法对单个代码块进行同步：

```java
synchronized (object) {
    // 需要同步的代码
}
```

其中 *object* 是对任何对象的引用。可以通过使用 `synchronized` 关键字作为方法修饰符来对整个方法进行同步，例如，

```java
public synchronized void myMethod() {
    // 需要同步的代码
}
```

这在功能上等同于以下内容：

```java
public void myMethod() {
    synchronized(this) {
        // 需要同步的代码
    }
}
```

当一个线程遇到同步块时，它首先尝试获取指定对象的锁。如果线程成功，它执行该块并释放锁。如果线程无法获取锁，它会等待锁可用，为自己获取锁，执行该块，然后释放锁。Java虚拟机确保这些操作一次只由一个线程执行。

在发票处理示例中，可以通过同步 `handleInvoice()` 方法来消除重复发票问题⁵：

```java
public synchronized void handleInvoice() throws IOException
{
    // 读取文件，递增发票号码，
    // 并更新文件。
    ...
}
```

> ⁵ 当然，同步无法防止某些其他Java类或某些在Java虚拟机之外运行的进程更新 `invoice.dat` 文件。该示例假设您对该文件拥有排他控制权。

出于性能考虑，不要同步比必要更多的代码非常重要，因为这会强制线程在同步部分单线通行。整个 `handleInvoice()` 方法不需要同步，只需要同步从打开文件读取到关闭文件写入的代码。

## Servlet线程模型

Servlet API利用Java内置的多线程支持，以确保响应式请求处理和良好的吞吐量。在这样做的同时，它在如何使用线程方面提供了一些灵活性。将请求分派到一个或多个线程的过程称为 *servlet线程模型*。您可以选择两种模型：

- 多个线程运行单个servlet实例，这是 *默认线程模型*。
- 多个实例，每个实例在自己的线程中运行。这被称为 *单线程模型*。

让我们考虑一下在每种模型中操作的含义。

## 默认线程模型

在默认模型中，只加载servlet（或JSP）的单个实例。<sup>6</sup> Servlet引擎维护一个线程池，并在请求到达时将它们分配给请求。每个线程运行适当的服务方法，通常是 `doGet()` 或 `doPost()`。在活动高峰期，许多请求可能同时通过相同的servlet方法运行，但是，由于每个线程有自己的指令指针和局部变量堆栈，因此请求之间不会发生冲突。图14-6说明了默认模型，显示三个请求由三个线程处理。

默认模型提供了良好的吞吐量，但存在一些限制。因为只有一个servlet实例，所以任何实例变量只存在一份副本。如果不采取预防措施并且代码允许写入变量，一个线程可能会覆盖另一个线程需要的值。例如，在图14-6中，请求2与请求1和请求3同时运行。如果它们都在 `doGet()` 方法中写入实例变量，并且之后读取它，它们的写入和读取可能会重叠。此外，如果 `doGet()` 或 `doPost()` 方法调用子例程，它必须将所有必要的对象作为参数传递，因为它不能依赖实例变量在写入和读取之间保持其值。

因此，避免使用实例变量，除非它们是只读的。这听起来可能像是一种限制，但这只是不同的观点。真正的工作单元，

> ⁶ 技术上，每个servlet名称一个实例。多个servlet名称可能与web.xml部署描述符中的同一个servlet类关联。详情参见第18章。



## **404** JSP：完全参考手册

毕竟，是请求本身，而不是 servlet 实例。任何类型的对象都可以作为请求属性以完全线程安全的方式存储：

```java
public void doGet(
    HttpServletRequest request,
    HttpServletResponse response)
    throws ServletException, IOException
{
    ...
    openConnection(request);
    runQuery(request);
    ...
}

public void openConnection(HttpServletRequest request)
    throws SQLException
{
    request.setAttribute
        ("connection", DriverManager.getConnection(...));
}
```

```java
public void runQuery(HttpServletRequest request) throws SQLException
{
    Connection con = (Connection)
        request.getAttribute("connection");
    Statement stmt = con.createStatement();
    ResultSet rs = stmt.executeQuery("SELECT ...");
    request.setAttribute("resultSet", rs);
}
```

同样，你可以同步 servlet 方法中的关键代码段，但必须小心避免过度同步，从而对性能产生不利影响。

## 单线程模型

默认模型的替代方案是单线程模型。在此环境中，servlet 引擎保证同一时间只有一个请求在运行 servlet 实例的 service 方法。要使用此模型，servlet 必须实现 `SingleThreadModel` 接口。此接口不包含任何方法；它仅仅标记该 servlet 需要这种线程处理。在 JSP 页面中，通过页面指令选择此模型：

```jsp
<%@ page isThreadSafe="false" %>
```

这会导致生成的 servlet 指明它实现了 `SingleThreadModel`。

对于单线程 servlet，同一时间只能有一个线程执行其 `doGet()` 或 `doPost()` 方法，因此这意味着实例变量是线程安全的。但是，servlet 引擎可以自由创建尽可能多的 servlet 实例，以维持足够的性能。图 14-7 展示了这种操作模式，其中请求 3 等待请求 1 完全完成后才运行，而请求 2 则在与其它请求同一时间的不同实例中运行。

`SingleThreadModel` 是许多混淆的根源。你会在 Java 新闻组中发现抱怨网络或数据库连接未被妥善隔离的帖子，尽管这些连接是在实现了 `SingleThreadModel` 的 servlet 中使用的。原因很容易理解：唯一被设为线程安全的是 servlet 实例本身。但是，由于存在多个实例，外部资源并未受到保护免受并发访问。

很难找到单线程模型所带来的任何显著优势。只需稍加规划和明智的同步，默认模型通常是更好的选择。

## 多线程应用程序

在许多服务器端环境中，多线程特别有用。一种场景是运行自动启动的后台进程，它不与任何特定请求相关联，类似于 Unix 守护进程或 Windows NT 服务。这在 servlet 环境中可以轻松实现，使用以下技术：

1.  让 `init()` 方法启动一个执行所需任务的线程。这可以包括打开一个套接字来处理请求，或者定期读取一个网页以获取动态更新的数据，例如股票报价或新闻头条。在 servlet 上下文中维护对该线程的引用。
2.  严格将 `doGet()` 方法用于命令、管理任务和状态报告。提供一个可以关闭或重启后台线程的命令通常是理想的。
3.  在 `destroy()` 方法中，在释放其使用的任何资源后关闭该线程。

可以在部署描述符中将 servlet（或 JSP）指定为 `load-on-startup`，这样它在 servlet 引擎运行时就会运行，无需用户登录。由于 servlet 引擎本身通常可以作为守护进程或服务运行，这等同于能够将此类进程编写为 Java servlet。

## 带状态消息的长时间运行请求

多线程的另一个有益用途是处理长时间运行的请求，例如复杂的数据分析或其他项目式的请求。如果客户端请求一个需要相当长时间的服务器进程，客户端和 servlet 引擎都只能等待其完成。不过，情况并非必须如此。

想想打印后台处理的工作原理。用户可以在文字处理应用程序中单击“打印”按钮，仅在打印请求排队时经历短暂的停顿。通常会出现一些消息，指明哪个打印机接收了请求，并可能提供一个标识打印任务的任务 ID。后台处理的输出随后在队列中等待打印机空闲，但用户可以自由地继续编写文档或执行任何其他任务。这些其他任务可能包括监控打印队列状态、暂停和释放任务、更改其优先级、取消任务等等。

JSP 页面可以以类似的方式运行。它可以通过启动一个后台线程来执行复杂任务，而不是在当前线程中运行，并将对该线程的引用作为会话属性保存。用户可以收到通知，表明请求已排队并正在处理中。JSP 页面还可以提供显示请求状态的界面，并允许用户暂停、释放或取消它。当请求完成时，JSP 页面可以提供一个超链接来查看结果。由极其智能的 JSP 页面处理的极长时间运行的请求，甚至可能会将其结果通过电子邮件发送给用户。

这种技术的一个变体可用于向用户提供一个状态屏幕，表明请求正在处理中，当请求完成时，该屏幕会被结果替换。该技术的关键在于使用一个后台会话作用域的线程来执行工作，并使用 `<META HTTP-EQUIV="REFRESH">` HTML 标签让 Web 浏览器自动监控状态。

在以下示例中，用户正在登录并通过耗时的模拟数据库操作请求身份验证。在处理身份验证请求时，用户会看到一条“正在验证，请稍候...”的消息。当请求完成时，此消息会被身份验证结果替换。与此同时，servlet 引擎可以自由处理其他请求，而无需等待身份验证请求完成。

此会话中客户端与服务器之间的基本对话如下：

- **客户端**：请验证我的身份。UserID=MyUserID，密码=MyPassword
- **服务器**：好的，两秒钟后回电获取状态。
- **客户端**：*（两秒后）* 你完成了吗？
- **服务器**：没有，两秒钟后回电获取状态
- **客户端**：*（两秒后）* 你完成了吗？
- **服务器**：没有，两秒钟后回电获取状态
- **客户端**：*（两秒后）* 你完成了吗？
- **服务器**：是的，您已通过身份验证 *（或未通过）*。

用户无需手动请求更新的状态。HTML 提供了一种客户端自动方式来定期刷新页面：

```html
<META HTTP-EQUIV="REFRESH" CONTENT="seconds; URL=url">
```

HTML 文档中存在此 `<META>` 标签会使浏览器等待指定的秒数，然后重定向到指定的 URL。此功能通常用于指示网站已迁移，用户将被自动转发到新地址。

以下 JSP 使用一个模拟数据库身份验证延迟的后台工作线程来实现此协议。

```jsp
<%--
Authenticator.jsp

    一个在长时间运行的请求期间显示状态消息的 JSP 页面，
    不会占用服务器资源等待请求完成。
--%>
<%

    // 检查是否有一个身份验证工作线程正在运行

    WorkerThread worker = (WorkerThread)
        session.getAttribute("worker");

    // 如果没有，则创建一个新的并开始身份验证

    if (worker == null) {
        String userID = request.getParameter("userID");
        String password = request.getParameter("password");
        worker = new WorkerThread(userID, password);
        session.setAttribute("worker", worker);
    }

    // 现在显示“请稍候”屏幕或“用户已验证”屏幕

    if (!worker.isDone()) {
        String url = HttpUtils.getRequestURL(request).toString();
        url = response.encodeURL(url);
%>
```



## 第14章：会话与线程管理

```html
<HTML>
<HEAD>
<TITLE>Please Wait</TITLE>
<META HTTP-EQUIV="REFRESH" CONTENT="2; URL=<%= url %>">
</HEAD>
<BODY>
Authenticating, please wait...
</BODY>
</HTML>
<%
    }
    else {
%>
<HTML>
<HEAD><TITLE>Done</TITLE></HEAD>
<BODY>
Authentication complete.
<%= worker.isAuthenticated() ? " You pass!" : " You fail!" %>
</BODY>
</HTML>
<%
    // Done with worker
    session.invalidate();
    }
%>
<%!
/**
* A background thread that performs a potentially
* long-running task (authentication from a database).
*/
public class WorkerThread implements Runnable
{
    private boolean done;
    private boolean authenticated;
    private Thread kicker;

    public WorkerThread(String userID, String password)
    {
        done = false;
        authenticated = false;
        kicker = new Thread(this);
        kicker.start();
    }

    public boolean isDone()
    {
        return done;
    }

    public boolean isAuthenticated()
    {
        return authenticated;
    }

    public void run()
    {
        // Do the work here

        try {

            // Pretend to do something that takes five seconds

            for (int i = 0; i < 5; i++)
                Thread.sleep(1000);

            // Randomly authenticate 80% of all users

            authenticated = (Math.random() > 0.2);

            // We are done

            done = true;
        }
        catch (InterruptedException ignore) {}
        finally {
            kicker = null;
        }
    }
}
%>
```

# 410 JSP：权威参考

## 应用考量

JSP环境提供了一系列丰富的选择，用于将应用特性映射到HTTP环境。主要的考量是对象作用域，即一个属性有效的时间段。页面上下文定义了四种作用域：

- page
- request
- session
- application

每种作用域都有自己的生命周期，属性可以存储在任何一种作用域中。特定作用域中的对象可以被同一Servlet上下文中的JSP页面和Servlet访问。开发者的任务是根据对象的使用需求选择匹配的对象作用域。

页面作用域等同于单个JSP页面中`_jspService()`方法的生命周期。例如，可以将一个用户ID字符串赋予此页面作用域，如下所示：

```jsp
pageContext.setAttribute
    ("userID", userID, PageContext.PAGE_SCOPE);
```

或者简单地：

```jsp
pageContext.setAttribute("userID", userID);
```

相应的`getAttribute()`方法可用于检索对象。

既然对象已经可以作为Java变量访问，为什么还要费心将它们存储在具有页面作用域的页面上下文中呢？主要的背景是JSP自定义标签，它们使用页面上下文在标签处理器和JSP页面之间进行通信。有关JSP自定义标签的详细信息，请参见第11章。

请求作用域与页面作用域几乎相同，但它还包括通过`<jsp:include>`或`<jsp:forward>`调用的其他JSP页面或Servlet。可以直接在请求中设置属性：

```java
request.setAttribute("userID", userID);
```

或者通过页面上下文：

```java
pageContext.setAttribute
    ("userID", userID, PageContext.REQUEST_SCOPE);
```

两种方法调用的效果是相同的；`pageContext.setAttribute()`方法只是调用`request.setAttribute()`。请求作用域适用于与单个请求相关的对象，这些对象可能在Servlet中设置，然后在`RequestDispatcher`将请求转发到的JSP页面中使用。

*会话作用域*用于多个请求，这些请求使用相同的会话ID进行自我标识，并与该ID的活动`HttpSession`相关联。可以直接在`session`对象中设置属性：

```java
session.setAttribute("userID", userID);
```

或者通过页面上下文：

```java
pageContext.setAttribute
	("userID", userID, PageContext.SESSION_SCOPE);
```

当同时满足以下三个要求时，会话作用域是合适的：

- 应用需要多个HTTP请求。
- 数据需要在请求之间持久化。
- 一个或多个服务器端对象必须在请求之间保持特定的状态。

正如本章所考虑的，当不需要HTTP会话时，也存在替代方案，如隐藏字段、URL重写和Cookie。

*应用作用域*是Web应用中所有Servlet和JSP页面的公共命名空间。它在请求之间自动持久化，不需要会话。可以通过在`web.xml`部署描述符中使用`<context-param>`在应用作用域中设置静态初始化参数：

```xml
<context-param>
    <param-name>jdbc.driver</param-name>
    <param-value>sun.jdbc.odbc.JdbcOdbcDriver</param-value>
</context-param>

<context-param>
    <param-name>jdbc.url</param-name>
    <param-value>jdbc:odbc:composers</param-value>
</context-param>
```

这些静态参数可以在Servlet或JSP页面中通过Servlet上下文`getInitParameter()`方法检索：

```java
String driver = application.getInitParameter("jdbc.driver");
String url = application.getInitParameter("jdbc.url");
```

可以使用与其他三种作用域相同的方法在应用作用域中存储和检索对象：

```java
pageContext.setAttribute("userID", userID, PageContext.APPLICATION_SCOPE);
```

或者：

```java
application.setAttribute("userID", userID);
```

应用作用域最适用于需要在请求之间持久化的对象、必须对应用的所有用户可见的对象，或需要在其他Servlet和JSP页面之间共享的对象。

## 总结

Web应用模型并不会自动映射到HTTP协议。HTTP是无状态的，不会记住客户端在一次请求与下一次请求之间的任何信息。Web浏览器环境也带来了复杂性——在一个应用中，每个页面都依赖于其前序页面，但用户可能乱序浏览页面，并在没有发出完成信号的情况下离开应用。

这个问题的解决方案是让客户端（浏览器）记住某些细节，并在每次发出请求时提醒服务器。这可以涉及客户端管理所有数据，但实际上更常见的是客户端只记住某种标识符，服务器使用该标识符从数据库中检索其余数据。这种虚拟会话（虚拟是因为不涉及持久连接）通常被称为会话。

本章讨论了四种会话管理技术：

- **HTML表单中的隐藏字段** 这些字段使用简单，但只能通过HTML表单传输。如果用户单击超链接，隐藏字段（因此会话）就会丢失。
- **URL重写** 这涉及将会话标识符附加到JSP页面生成的所有URL。从性能角度来看，这种技术可能代价高昂。
- **Cookies** 小型命名数据元素被发送到客户端，并在页面再次访问时返回给服务器。Cookies的优点是它们可以持续任意长的时间，甚至在客户端计算机关闭后也是如此。缺点是由于隐私方面的担忧，一些用户会关闭Cookie支持。

- **会话API** Servlet引擎可以创建一个`HttpSession`对象，该对象充当持久化对象的仓库，这些对象在来自同一客户端在同一应用中的请求之间持久存在。客户端使用Cookie或URL重写来记住会话的ID。Servlet引擎确定客户端接受哪种技术并相应地进行调整。

会话可以通过编程方式关闭，也可以根据可配置的空闲时间超时。会话API提供了一种方式，使对象知道它们何时已绑定到会话或从会话中解绑。

JSP页面由于运行在纯Java环境中，可以完全访问Java对多线程应用的支持。本章讨论了基本的线程概念，如如何创建、启动和同步线程，然后考虑了两种Servlet线程模型。并给出了两个使用多线程的Web应用示例。

尽管原始HTTP协议并未计划用于动态内容，但该协议已被证明具有相当强的扩展能力。在此灵活性的基础上，会话API为在Web应用环境中实现HTTP工作提供了框架。



# 第15章

# JSP与JavaBeans

版权所有 2001 The McGraw-Hill Companies, Inc. 点击此处查看使用条款。

硬件与电子技术的巨大进步得益于组件工程。工程师们无需从零开始搭建电路，而是能够以新颖的方式将经过测试的模块组合起来，创造出更高层次的功能。基于组件的编程将这一理念延伸到了软件领域。在Java世界中，这便是*JavaBeans*。

本章将描述JavaBeans编程模型，以及bean如何向使用它的类暴露其属性。它解释了在JSP页面中使用bean所提供的接口。本章最后通过一个完整的示例，展示了在JSP页面中运行一个可定制的天气报告bean的操作过程。

## 什么是JavaBean？

对bean的定义被刻意设得很宽泛。一个*bean*就是一个满足两个要求的Java类：

- 它有一个无参构造函数。
- 它实现了`Serializable`或`Externalizable`接口以使其具有持久性。

根据这个定义，大多数类已经是bean，或者只需稍加改动就能转换为bean。除了Java虚拟机之外，运行bean不存在其他必需的上下文。这使得构造正确的bean可以在任何Java环境中使用——无论是applet、servlet、JSP页面，还是独立的Java应用程序。

## Bean的属性

此外，大多数bean都具有属性。*属性*是bean为它提供的读和/或写方法所对应的一些特性。所有对bean属性的访问都必须通过这些方法进行；底层的数据字段（如果存在的话）是私有的。JavaBeans编程模型的一部分就是这些方法的命名约定。除非你通过`BeanInfo`类做出了特殊规定，否则属性的读方法是一个名为`get<PropertyName>()`的公共方法，其中`<PropertyName>`是属性名且首字母大写。同样，写方法（如果存在的话）名为`set<PropertyName>()`。

下面是一个名为`Mortgage`的JavaBean示例，它封装了描述抵押贷款的参数：

```java
package jspcr.beans.mortgage;

import java.io.*;

public class Mortgage implements Serializable
{
    private double principal;
    private double rate;
    private int term;

    /**
     * Returns the principal.
     */
    public double getPrincipal()
    {
        return principal;
    }

    /**
     * Sets the principal.
     * @param principal the principal.
     */
    public void setPrincipal(double principal)
    {
        this.principal = principal;
    }

    /**
     * Returns the annual interest rate
     */
    public double getRate()
    {
        return rate;
    }

    /**
     * Sets the interest rate.
     * @param rate the annual interest rate as a percentage.
     */
    public void setRate(double rate)
    {
        this.rate = rate;
    }

    /**
     * Returns the term in months.
     */
    public int getTerm()
    {
        return term;
    }

    /**
     * Sets the term.
     * @param term the term in months.
     */
    public void setTerm(int term)
    {
        this.term = term;
    }

    /**
     * Returns the amortization factor, the amount of the
     * monthly payment that will pay all principal and
     * interest within the specified period of time.
     */
    public double getPayment()
    {
        if (rate == 0)
            throw new IllegalArgumentException
                ("No interest rate specified");

        double mrate = rate / 1200.0;

        double fv = Math.pow((1 + mrate), term);
        double numer = principal * mrate * fv;
        double denom = fv - 1.0;
        return round(numer / denom);
    }

    /**
     * Utility method that rounds a currency amount to
     * the nearest 1/100 of the currency unit.
     */
    public static final double round(double x)
    {
        return ((double) ((long) (x * 100.0 + 0.5))) / 100.0;
    }
}
```

Mortgage bean有四个属性：

- **principal** 借款金额。
- **rate** 以百分比表示的年利率。例如，6%应输入为6.0。
- **term** 还款的月数。
- **payment** 一个只读属性。

请注意，前三个属性都有对应的私有数据字段，而第四个没有，它是按需计算的。这强调了关键在于`get`和`set`方法的存在。这些方法是bean向外部世界展示的唯一接口。

对bean状态变化感兴趣的类可以实现众多`EventListener`接口中的一个。当一个类被注册为事件监听器时，当bean中发生感兴趣的事件时，它会收到回调。这使得bean能够协作完成更大的任务。AWT和Swing GUI架构广泛使用了这种事件模型。然而，在服务器端环境中使用的bean主要被用作属性仓库，通常不实现事件监听器支持。

## 持久化

既然如此，bean必须提供某种方式使其状态在不活跃时得以持续，甚至在不同的Java虚拟机之间也能持续。这是通过让bean实现`Serializable`或`Externalizable`接口来实现的。

*序列化*是指将对象转换为可以存储在文件中或通过网络传输的字节流的过程。将对象从字节流中重新组装起来的互补过程称为*反序列化*。Java API提供了为此目的设计的`ObjectOutputStream`和`ObjectInputStream`类。

对象通过使用输出流的`writeObject()`方法写入`ObjectOutputStream`来进行序列化。例如，一个包含`Mortgage` bean的程序可以这样序列化它：

```java
OutputStream fileOut = new FileOutputStream("mortgage.ser");
ObjectOutputStream objOut = new ObjectOutputStream(fileOut);
objOut.writeObject(mortgageBean);
objOut.flush();
fileOut.close();
```

之后，这个或任何其他程序都可以使用`ObjectInputStream`的`readObject()`方法从`mortgage.ser`文件中重建`Mortgage` bean：

```java
InputStream fileIn = new FileInputStream("mortgage.ser");
ObjectInputStream objIn = new ObjectInputStream(fileIn);
Mortgage mortgageBean = null;
try {
    mortgageBean = (MortgageBean) objIn.readObject();
}
catch (ClassNotFoundException e) {
    // handle exception
}
```

在这两段代码片段中，只序列化了一个对象，并且是序列化到文件。序列化多个对象同样简单；只需多次调用`objOut.writeObject()`即可。只要反序列化对象的程序知道对象的正确数量和类型，它就可以通过多次调用`objIn.readObject()`来读取它们。同样，底层流不必是文件——它可以是套接字、字节数组，或者如果虚拟机支持的话，也可以是穿孔卡片。

注意：Mortgage类无需做任何特殊处理就能被序列化；它只需要实现`Serializable`接口。通常，servlet引擎在终止时会负责存储会话和应用bean所需的所有逻辑，并在重启时恢复它们。

但是，存在一个例外。并非所有对象都是可序列化的。例如，数据库连接无法被暂停并在稍后唤醒。它的本质要求它必须与数据库管理系统中的相应对象保持通信。同样，线程与底层操作系统线程紧密相连，无法简单地消失再重现。在这些情况下，包含不可序列化对象的类必须提供重新连接或重启它们的方法。此外，它必须使用关键字`transient`声明对这些对象的变量引用，以防止正常的序列化过程尝试处理它们。

包含瞬态对象的类应该通过提供具有此签名的方法来恢复它们：

```java
private void readObject(ObjectInputStream in)
    throws IOException
```

在`readObject()`方法中，该类应首先调用`defaultReadObject()`来恢复可序列化数据字段，然后执行任何必要的逻辑来初始化瞬态字段。通常，这种恢复是通过调用另一个方法来完成的，该方法也可以在构造函数中调用，以避免重复代码。

一个例子可以帮助阐明这一点：

```java
import java.io.*;
```



public class CounterBean 实现了 Runnable 和 Serializable 接口
{
    private transient Thread thread;
    private int count;

    /**
     * 创建一个新的 CounterBean，将其计数
     * 初始化为零，并启动计数线程
     */
    public CounterBean()
    {
        count = 0;
        start();
    }

    /**
     * 从对象流中恢复此 CounterBean
     * 并重新启动线程
     */
    private void readObject(ObjectInputStream in)
        throws IOException
    {
        try {

            // 首先调用此方法以恢复所有
            // 非 transient 字段

            in.defaultReadObject();
        }
        catch (ClassNotFoundException e) {
            throw new IOException(e.getMessage());
        }

        // 重新启动线程

        start();
    }

    /**
     * 提供一种关闭线程的方法
     */
    public void interrupt()
    {
        if (thread != null)
            thread.interrupt();
    }

    /**
     * 启动计数线程。此方法
     * 在对象首次创建时由构造函数调用，
     * 也在对象反序列化时由 readObject 方法调用。
     */
    private void start()
    {
        if (thread == null) {
            thread = new Thread(this);
            thread.setPriority(Thread.MIN_PRIORITY);
            thread.start();
        }
    }

    /**
     * 每秒递增并打印计数器的值。
     */
    public void run()
    {
        try {
            for (;;) {
                Thread.sleep(1000);
                count++;
                System.out.println(count);
            }
        }
        catch (InterruptedException e) {}
    }
}

JSP：完整参考手册

CounterBean 类使用一个后台线程每隔一秒钟打印一次计数器的值。该类是可序列化的，但线程不是，因此存在在类反序列化时重新启动线程的逻辑。注意，thread 变量使用 transient 关键字声明。该类有两个入口点：其构造函数和 readObject() 方法。两个入口点都调用 start() 方法，该方法创建并启动一个线程来处理计数器逻辑。该线程持续运行直到被中断。一个使用此计数器 bean 的程序可以通过其构造函数调用它，对其进行序列化，然后反序列化，此时线程显然会从中断处继续运行：

```java
import java.io.*;

/**
 * 一个使用 CounterBean 的类。如果存在序列化版本，
 * 它将反序列化该版本。否则，
 * 它将创建一个新的 CounterBean。
 */
public class CBTest
{
    public static void main(String[] args)
        throws IOException, ClassNotFoundException
    {
        CounterBean bean = null;

        // 如果存在序列化版本，则加载它

        File file = new File("counter.ser");
        if (file.exists()) {
            System.out.println("反序列化 bean");
            FileInputStream fileIn = new FileInputStream(file);
            ObjectInputStream objIn = new ObjectInputStream(fileIn);
            bean = (CounterBean) objIn.readObject();
            objIn.close();
            fileIn.close();
        }

        // 否则，创建一个新的 bean

        else {
            System.out.println("创建新 bean");
            bean = new CounterBean();
        }

        // 让 bean 运行直到用户按下
        // 回车键

        BufferedReader in =
            new BufferedReader(
                new InputStreamReader(
                    System.in));

        System.out.println("按回车键终止程序");
        in.readLine();
        bean.interrupt();

        // 序列化 bean

        System.out.println("序列化 bean");
        FileOutputStream fileOut = new FileOutputStream(file);
        ObjectOutputStream objOut = new ObjectOutputStream(fileOut);
        objOut.writeObject(bean);
        objOut.flush();
        objOut.close();
        fileOut.close();
    }
}
```

一个 bean 可能实现 Externalizable 接口作为其持久化方案，而不是实现 Serializable 接口。Externalizable 对象使用其自己选择的任何格式，自行处理从对象流中的读写。为此，它必须提供 readExternal(ObjectInput) 和 writeExternal(ObjectOutput) 方法。但是，因为 Serializable 对象可以使用任何所需格式提供自己的 readObject() 方法，所以 Externalizable 提供的优势很少，因此并未广泛使用。

## JSP 动作

正如你所看到的，JavaBeans 也是 Java 类，因此可以在 JSP 页面中使用脚本段、声明和表达式进行创建和操作。然而，JSP 规范为 bean 提供了特殊支持，使其能够在更高层次上进行脚本化。这种支持包括三个标准动作：

- `<jsp:useBean>` 用于声明、实例化和初始化 bean
- `<jsp:setProperty>` 用于设置 bean 属性
- `<jsp:getProperty>` 用于检索 bean 属性值

以下各节将讨论这些动作中的每一个。

## `<jsp:useBean>`

`<jsp:useBean>` 标签创建或反序列化一个 bean，并将其与一个脚本变量关联。语法如下：

```
<jsp:useBean id="name" scope="scope" typespec/>
```

或者

```
<jsp:useBean id="name" scope="scope" typespec>
    <body>
</jsp:useBean>
```

其中 *name*、*scope* 和 *typespec* 的定义如下。

## `<jsp:useBean>` 的 id 属性

*id* 属性中指定的 *name* 是一个标识符，用作指定范围内 bean 对象的属性名，并在 JSP 页面中声明为一个 Java 脚本变量。因为此值是一个脚本变量，所以它区分大小写，并且必须符合 Java 标识符命名规则。此值用于 `<jsp:setProperty>` 和 `<jsp:getProperty>` 动作的 *name* 属性中，以指示该动作应用于可能多个 bean 中的哪一个。

## `<jsp:useBean>` 的 scope 属性

*scope* 指定 bean 存在的命名空间。这些与 *PageContext* 对象维护的范围相同。可能的值是：

- **PAGE** 在此 JSP 页面的持续时间内有效。这是默认范围。
- **REQUEST** 在此 JSP 页面的剩余部分以及通过 `<jsp:forward>` 或 `<jsp:include>` 动作提供此请求的任何其他资源中有效。
- **SESSION** 在此 HTTP 会话中执行的任何 JSP 页面或 servlet 期间有效。
- **APPLICATION** 在此 Web 应用程序（servlet 上下文）的任何 JSP 页面或 servlet 中有效。

任何这些范围中的 bean 都可以通过 `pageContext` 变量的 `getAttribute()` 和 `setAttribute()` 方法进行访问。`request`、`session` 或 `application` 命名空间中的 bean 可以分别在 servlet 中通过 `ServletRequest`、`HttpSession` 和 `ServletContext` 类的 `getAttribute()` 和 `setAttribute()` 方法进行访问。

## `<jsp:useBean>` 的类型规范

类型规范由 `class`、`type` 和 `beanName` 属性的某种组合组成。这些属性的组合允许 useBean 动作在做什么方面具有灵活性。必须至少指定 `class` 和 `type` 之一，并且如果指定了 `class`，则不能使用 `beanName`。这意味着有效的组合是：

- 仅 type
- 仅 class
- type 和 class
- type 和 beanName

类型规范允许创建新的 bean、重用已序列化的 bean，或将现有 bean 集成到 JSP bean 框架中。进一步的功能源于 `<jsp:useBean>` 可以包含一个 JSP 代码体。`<jsp:useBean>` 标签体中的代码（通常是一个或多个 `<jsp:setProperty>` 动作和脚本段）仅在 bean 在当前请求中被新实例化时才执行。

`<jsp:useBean>` 标签的精确操作最好通过图形来解释。本节中的流程图描述了该标签在先前列出的四种情况中的每一种情况下如何被评估。

**仅指定 type 属性** 一个 bean 可能实现多个接口，其中只有一个接口对于 bean 在给定 JSP 页面中的操作是重要的。所需的接口可以在 `type` 属性中输入。当仅指定 `type` 时，JSP 引擎定义一个该类型的脚本变量，然后在指定的范围中查找名称与给定 id 匹配的属性。如果 JSP 引擎找到匹配的对象，它会将该对象转换为指定的类型并将其分配给该变量。否则，如果找不到该对象，JSP 引擎将抛出 `InstantiationException`。此过程如图 15-1 所示。



## <jsp:useBean>

**仅指定类型** 当只提供 `type` 属性时，JSP 引擎会声明该类型的一个变量，并在指定的范围中查找具有匹配名称的属性。如果找到了，JSP 引擎会将该对象转换为指定的类型并赋值给该变量。否则，JSP 引擎会创建该指定类的一个新对象，将其赋值给变量，并将其设置为该范围内的一个属性。如果 `<jsp:useBean>` 标签有标签体，则随后会计算标签体。此过程如图 15-1 所示。

![图 15-1. 仅给出类型时 <jsp:useBean> 处理的流程图](img/7a2f73369bb140583c7288b73456addb_453_0.png)

**仅指定 class 属性** 如果需要特定的 bean 类，则应指定 `class` 属性。同样，JSP 引擎会声明该类的一个变量，并在指定的范围中查找具有匹配名称的属性。如果找到了，JSP 引擎会将该对象转换为指定的类并赋值给该变量。否则，JSP 引擎会创建该指定类的一个新对象，将其赋值给变量，并将其设置为该范围内的一个属性。如果 `<jsp:useBean>` 标签有标签体，则随后会计算标签体。此过程如图 15-2 所示。

![图 15-2. 仅给出 class 时 <jsp:useBean> 处理的流程图](img/7a2f73369bb140583c7288b73456addb_454_0.png)

**同时指定类型和 class** 一个密切相关的情况是需要特定的 bean 类，但将仅使用一个特定的接口。在这种情况下，处理过程与前一种情况相同，不同之处在于变量类型和类型转换操作使用的是 `type`（类型），而不是 `class`（类）。图 15-3 展示了该算法。

**指定类型和 beanName** 当需要将已序列化的 bean 导入到 JSP 环境中（例如本章前面描述的 `Mortgage` 或 `CounterBean` bean）时，应使用 `type` 和 `beanName` 属性。`beanName` 必须采用 `Beans.instantiate(ClassLoader loader, String name)` 所使用的格式。该名称首先按如下方式转换为文件名：

- 句点被转换为“/”
- 在末尾追加 `.ser`

因此，例如，`jspcr.beans.mortgage.Mortgage` 会被转换为 `jspcr/beans/mortgage/Mortgage.ser`。如果类加载器可以找到该名称的文件，它将被反序列化以获取对象。否则，原始名称被视为类名，类加载器尝试创建该命名类的实例。在任何一种情况下，新的 bean 都会被分配给指定 `id` 的脚本变量，并存储在相应范围内的属性中。此过程如图 15-4 所示。

![图 15-4. 指定类型和 beanName 时 <jsp:useBean> 处理的流程图](img/7a2f73369bb140583c7288b73456addb_457_0.png)

## <jsp:setProperty>

`<jsp:setProperty>` 操作根据 JSP 页面中的值为 bean 属性赋值。其语法可以是以下四种形式中的任何一种：

```
<jsp:setProperty name="*" property="property" value="value" />
```

或

```
<jsp:setProperty name="*" property="property" param="param" />
```

或

```
<jsp:setProperty name="*" property="property" />
```

或

```
<jsp:setProperty name="*" property="*" />
```

其中 `name`、`property`、`param` 和 `value` 的描述如下。

### <jsp:setProperty> 的 name 属性

`name` 属性标识应设置其属性的 bean。该 `name` 必须先前已作为 `<jsp:useBean>` 标签的 `id` 属性指定。

### <jsp:setProperty> 的 property 属性

一旦确定了特定的 bean，就必须指定要设置的属性名称。这就是 `property` 属性的作用。该属性可以是一个属性名，也可以是特殊值 `*`。如果此属性是一个名称，则该 bean 必须具有该属性的相应 set 方法。例如，在我们的 `Mortgage` bean 中，存在 `setPrincipal()`、`setRate()` 和 `setTerm()` 方法，它们分别用于设置 `principal`、`rate` 和 `term` 属性。

如果 `property` 属性是 `*`，则会将 bean 的可设置属性列表与当前请求中的参数列表进行比较。无论在哪里匹配，都会使用相应的请求参数调用 `set` 方法。因此，例如，如果 HTML 表单包含以下字段：

```
<FORM ACTION="DoMortgage.jsp">
Principal: <INPUT TYPE="TEXT" NAME="principal"><BR>
Annual Interest Rate: <INPUT TYPE="TEXT" NAME="rate"><BR>
Term in months: <INPUT TYPE="TEXT" NAME="term"><BR>
<INPUT TYPE="SUBMIT">
</FORM>
```

并且 `DoMortgage.jsp` 具有以下操作：

```
<jsp:useBean id="loan" class="jspcr.beans.mortgage.Mortgage">
    <jsp:setProperty name="loan" property="*"/>
</jsp:useBean>
```

那么 `setProperty` 这一行与以下几行具有相同的效果：

```
<jsp:setProperty
        name="loan"
        property="principal"
        value="<%= request.getParameter("principal") %>"/>

<jsp:setProperty
        name="loan"
        property="rate"
        value="<%= request.getParameter("rate") %>"/>

<jsp:setProperty
        name="loan"
        property="term"
        value="<%= request.getParameter("term") %>"/>
```

但好处是所需的代码行更少，出错的机会也更少。指定属性名但不指定 `value` 或 `param` 属性时，也会达到相同的效果。在这种情况下，属性值从相应的请求参数赋值。

> **注意** 如果 `property` 属性是 `*`，或者未指定 `value` 或 `param`，并且请求参数为 `null` 或空字符串，则相应的 bean 属性不会被修改。

### <jsp:setProperty> 的 param 属性

当请求参数名称与 bean 属性名称不同时，可以通过在 `<jsp:setProperty>` 中使用 `param` 属性来将请求参数映射到 bean 属性。如果指定了 `param` 属性，则具有该名称的请求参数将被分配给 `property` 属性中命名的属性。

### <jsp:setProperty> 的 value 属性

`value` 属性指定要分配给 bean 属性的值。如果省略该属性，则使用相应的请求参数值，如前所述。否则，值可以指定为字符串或 JSP 表达式，形式为 `<%= expression %>`。后一种语法称为*请求时属性表达式*。

如果值是字面字符串，则 bean 属性必须是 `java.lang.String` 类型，或者是基本类型（`boolean`、`byte`、`char`、`double`、`int`、`float`、`long`）或相应的对象包装类型（`Boolean`、`Byte`、`Character`、`Double`、`Integer`、`Float`、`Long`）。非字符串类型使用对象包装的 `valueOf` 方法从字符串转换而来。因此，例如，`Mortgage` 的 `rate` 属性，其 setter 方法如下：

```
public void setRate(double x) {
    this.rate = x;
}
```

可以这样调用：

```
<jsp:setProperty name="loan" property="rate" value="8.75"/>
```

JSP 转换器随后生成设置属性的代码，如下所示：

```
loan.setRate(Double.valueOf("8.75").doubleValue());
```

如果使用请求时表达式来提供值：

```
<jsp:setProperty name="loan" property="rate"
    value="<%= LIBOR.getSixMonthLiborRate() + 0.05 %>"/>
```

那么 JSP 转换器会使用内省来查找属性类型，并将表达式转换为该类型：

```
loan.setRate((double) (LIBOR.getSixMonthLiborRate() + 0.05));
```

## <jsp:getProperty>

Bean 属性值可以通过 `<jsp:getProperty>` 操作来检索。此操作的形式如下：

```
<jsp:getProperty name="name" property="property" />
```

其中 `name` 是具有相应 `id` 属性的 bean，`property` 是所需的属性名称。属性名必须是字面字符串，而不是请求时表达式。当 `<jsp:getProperty>` 标签在运行时被计算时，相应的 bean 属性的值会被转换为字符串并写入 JSP 输出流。

## 一个完整的示例——使用 Bean 实现个性化

让我们将所有这些元素整合起来，考虑一个完整的示例。许多门户网站根据用户的偏好定制页面的内容和呈现方式。这种个性化可能表现为指向与用户之前表达过的兴趣相关的产品和信息的超链接。例如，MSNBC 显示用户选择的本地天气和股票价格。其背后的理念是，如果这些信息始终在主页上，用户就不太可能离开网站去寻找这些信息。



# 从网络获取天气数据

我们（LyricNote 网站设计师）已决定在主页添加此类信息。首先将添加一行本地天气信息，该信息可根据用户自定义，报告用户所在区域的天气状况。

我们需要的第一样东西是天气信息来源。在美国，这很容易从美国国家气象局获取，该局隶属于美国国家海洋和大气管理局。他们的网页提供天气数据、天气预报、实时状况、天气图、风暴预测以及大量其他天气信息。尽管这些网页是为人类用户通过网页浏览器访问而设计的，但它们同样可以被 Java 程序轻松地作为 URL 输入流来读取。

为此，我们创建了一个天气观测 bean（Observation）。Observation 使用机场代码作为访问美国国家气象局网页的键，该网页报告该地点的实时天气观测数据。这个 bean 有五个属性，如表 15-1 所列：

这些属性中的大多数只有 get 方法，因为它们的值应在 bean 解析美国国家气象局网页时在内部设置。唯一可以设置的属性是机场代码。调用 `setAirportCode()` 方法会告知 bean 获取最新读数并更新其其他属性。

根据机场代码，bean 构建出包含该机场天气读数的特定网页的 URL。然后它打开 URL 输入流，并解析快速掠过的 HTML，以提取它需要的特定属性：位置、时间和温度。

| 属性 | 访问权限 | 描述 |
| :--- | :--- | :--- |
| airportCode | 可读/可写 | 进行天气测量的机场的三字母代码。设置此属性会指示 bean 访问天气网站以获取最新读数。 |
| URL | 只读 | 包含该机场读数的美国国家气象局网页的 URL。 |
| location | 只读 | 机场名称。 |
| time | 只读 | 观测的日期和时间。 |
| temperature | 只读 | 摄氏温度。 |

表 15-1. 天气观测 Bean 的属性

这是整个链条中的薄弱环节。一个由外部来源产生的网页显然可能会发生变化，因此，无论使用何种启发式方法来解析它，都必须定期检查和更新。当这种“网页挖掘”技术基于格式已明确知悉的内部网站时，它最为有用。然而，许多政府和商业网站都是计算机生成的，并以相当规律的形式呈现信息。

```java
package jspcr.beans.weather;

import java.io.*;
import java.net.*;
import java.text.*;
import java.util.*;

/**
 * A bean that extracts weather information from
 * the U. S. National Weather Service web site
 */
public class Observation implements Serializable
{
    /**
     * The base URL for National Weather Service data
     */
    private static final String BASEURL =
        "http://weather.noaa.gov/weather/current";

    /**
     * Date format used for parsing observation time
     */
    private static final SimpleDateFormat DATEFMT =
        new SimpleDateFormat("MMM dd, yyyy - hh:mm aa zzz");

    /**
     * Airport code
     */
    private String airportCode;

    /**
     * Full name of location
     */
    private String location;

    /**
     * Time of observation
     */
    private Date time;

    /**
     * Temperature in degrees Celsius
     */
    private Double temperature;

    // =========================================
    //    Bean accessor methods
    // =========================================

    /**
     * Returns the airport code
     */
    public String getAirportCode()
    {
        return airportCode;
    }

    /**
     * Sets the airport code, which
     * causes the bean to be reloaded.
     * @param airportCode the airportCode.
     */
    public void setAirportCode(String airportCode)
        throws IOException
    {
        this.airportCode = airportCode;
        loadFromURL(getURL());
    }

    /**
     * Returns the location.
     */
    public String getLocation()
    {
        return location;
    }

    /**
     * Sets the location.
     * @param location the location.
     */
    protected void setLocation(String location)
    {
        this.location = location;
    }

    /**
     * Returns the time.
     */
    public Date getTime()
    {
        return time;
    }

    /**
     * Sets the time.
     * @param time the time.
     */
    protected void setTime(Date time)
    {
        this.time = time;
    }

    /**
     * Returns the temperature.
     */
    public double getTemperature()
    {
        return (temperature == null)
                ? 0
                : temperature.doubleValue();
    }

    /**
     * Sets the temperature.
     * @param temperature the temperature.
     */
    protected void setTemperature(double temperature)
    {
        this.temperature = new Double(temperature);
    }

    /**
     * Returns the URL of the NWS web page that contains
     * current weather conditions at the airport
     */
    public URL getURL() throws MalformedURLException
    {
        StringBuffer sb = new StringBuffer();

        sb.append(BASEURL);
        sb.append("/K");
        sb.append(airportCode.toUpperCase());
        sb.append(".html");

        return new URL(sb.toString());
    }

    // ========================================
    //    Web page parsing routines
    // ========================================

    /**
     * Loads the weather data from a URL
     */
    protected void loadFromURL(URL url)
        throws IOException
    {
        load(url.openStream());
    }

    /**
     * Parses an HTML input stream to extract a weather
     * observation. Note that this uses heuristics to
     * determine where each data element can be found
     * in the HTML. As such, it is subject to change.
     */
    protected void load(InputStream stream) throws IOException
    {
        location = null;
        time = null;
        temperature = null;

        BufferedReader in =
            new BufferedReader(
                new InputStreamReader(stream));

        for (;;) {
            String line = in.readLine();
            if (line == null)
                break;

            if (location == null)
                parseLocation(line);
            if (time == null)
                parseTime(line);
            if (temperature == null)
                parseTemperature(line);
        }
        in.close();
    }

    /**
     * Searches the current line for the location
     */
    protected void parseLocation(String line)
    {
        final String TOKEN1 = "<TITLE>";
        final String TOKEN2 = "-";
        final String TOKEN3 = "</TITLE>";

        int p = line.indexOf(TOKEN1);
        if (p != -1) {
            p += TOKEN1.length();
            p = line.indexOf(TOKEN2, p);
            if (p != -1) {
                p += TOKEN2.length();
                int q = line.indexOf(TOKEN3);
                if (q != -1) {
                    String token = line.substring(p, q).trim();
                    StringTokenizer st =
                        new StringTokenizer(token, ",");
                    token = st.nextToken();
                    token = st.nextToken();
                    setLocation(token);
                }
            }
        }
    }

    /**
     * Searches the current line for the time
     */
    protected void parseTime(String line)
    {
        final String TOKEN1 = "<OPTION SELECTED>";
        final String TOKEN2 = "<OPTION>";

        int p = line.indexOf(TOKEN1);
        if (p != -1) {
            p += TOKEN1.length();
            int q = line.indexOf(TOKEN2, p);
            if (q != -1) {
                String token = line.substring(p, q).trim();
                Date date = DATEFMT.parse
                    (token, new ParsePosition(0));
                if (date != null)
                    setTime(date);
            }
        }
    }

    /**
     * Searches the current line for the temperature
     */
    protected void parseTemperature(String line)
    {
        final String TOKEN1 = "(";
        final String TOKEN2 = ")C";

        int q = line.lastIndexOf(TOKEN2);
        if (q != -1) {
            int p = line.lastIndexOf(TOKEN1);
            if (p != -1) {
                p += TOKEN1.length();
                String token = line.substring(p, q).trim();
                try {
                    setTemperature(Double.parseDouble(token));
                }
                catch (NumberFormatException e) {
                    e.printStackTrace();
                }
            }
        }
    }
}
```

这个 bean 的核心是 `load()` 方法，它解析输入流以寻找位置、时间和温度。图 15-5 显示了位于北卡罗来纳州的罗利-达勒姆国际机场天气状况的典型美国国家气象局网页。

![](img/7a2f73369bb140583c7288b73456addb_468_0.png)

生成网页的HTML代码包含了我们所需的全部信息，只要我们能找到可靠的规则来提取它。事实证明，`location`属性的提取相当简单，因为它被HTML的`<TITLE>` ... `</TITLE>`标签所包围：

```
<HTML>
<HEAD>
<TITLE>Current Weather Conditions - Raleigh / Durham,
Raleigh-Durham International Airport, NC,
United States </TITLE>
```
（在HTML中标题是完整的一行；这里为了可读性进行了换行）。`parseLocation()`方法会检查当前行是否包含`<TITLE>`和`</TITLE>`标记。如果包含，则提取标记之间的文本，并使用以第二个逗号分隔的字段作为地点名称。

`time`属性位于文档中唯一的一对`<OPTION SELECTED>`和`<OPTION>`标签之间：

```
<TD><FONT FACE="Arial,Helvetica"><FORM>
<SELECT><OPTION SELECTED> Nov 05, 2000 - 10:51 PM EDT
<OPTION> Nov 05, 2000 - 09:51 PM CDT
<OPTION> Nov 05, 2000 - 08:51 PM MDT
<OPTION> Nov 05, 2000 - 07:51 PM PDT
<OPTION> Nov 05, 2000 - 06:51 PM ADT
<OPTION> Nov 05, 2000 - 05:51 PM HDT
</SELECT><BR> 2000.11.06 0251 UTC
</FORM></FONT></TD>
```
（同样，HTML已经为了可读性进行了换行。原始HTML是完整的一行。）我们使用`SimpleDateFormat`中的`parse()`方法将日期和时间转换为`java.util.Date`对象。

`temperature`属性在网页中以这种形式出现：

```
<TR VALIGN=TOP>
<TD ALIGN=RIGHT BGCOLOR="#FFFFFF"><B><FONT COLOR="#0000A0">
<FONT FACE="Arial,Helvetica">Temperature</FONT></FONT></B></TD>
<TD><FONT FACE="Arial,Helvetica"> 42.1 F (5.6 C)
</FONT></TD>
</TR>
```
这个属性稍难分离，因为关键词`Temperature`出现在前一行。我们采用更简单的方法，查找第一个以`(...C)`结尾的行，并解析括号内的字符串以获取摄氏度。

该类的其余部分主要由各个属性的适当get和set方法组成。

## LyricNote 门户

现在我们有了一个JavaBean，它隐藏了查找网页和解析HTML的所有复杂细节，并简单地提供了一种通过机场代码获取当前天气状况的方法。该Bean将这个过程简化到一个函数调用的复杂度，比调用`Math.cos()`求角度的余弦值难不了多少。我们现在可以将这个Bean应用到我们的门户网页中。

我们的策略是使用持久化Cookie记录用户的地点偏好（机场代码）。每次显示网页时，都从Cookie中检索机场代码，并用它来初始化一个`Observation`Bean。由此产生的地点、时间和温度会显示在页面顶部Logo下方的一行中，不引人注目。此外，该行还包含一个超链接，使用户可以选择新的机场代码。以下展示了门户JSP的一部分：

```
<%@ page session="false" %>
<HTML>
<HEAD>
<TITLE>LyricNote Portal</TITLE>
<LINK REL="stylesheet" HREF="style.css">
</HEAD>
<BODY>
<IMG SRC="images/lyric_note.png">
<HR COLOR="#000000">

<%-- 获取天气Cookie --%>

<%
    String airportCode = "RDU";
    Cookie[] cookies = request.getCookies();
    if (cookies != null) {
        for (int i = 0; i < cookies.length; i++) {
            Cookie cookie = cookies[i];
            if (cookie.getName().equals("airportCode")) {
                airportCode = cookie.getValue();
                break;
            }
        }
    }
%>

<%-- 获取该地点的天气观测Bean --%>

<jsp:useBean id="wobs" class="jspcr.beans.weather.Observation">
<jsp:setProperty
    name="wobs"
    property="airportCode"
    value="<%= airportCode %>"/>
</jsp:useBean>

<%-- 显示天气信息 --%>

<SPAN CLASS="whiteOnBlue">&nbsp;Weather&nbsp;</SPAN>
<SPAN CLASS="blueOnWhite">
<jsp:getProperty name="wobs" property="location"/>
<jsp:getProperty name="wobs" property="time"/>
<jsp:getProperty name="wobs" property="temperature"/> C&deg;
</SPAN>
<A CLASS="whiteOnBlue" HREF="AirportSelection.html">
&nbsp;Select City&nbsp;
</A>
<HR COLOR="#000000">

<%-- 显示网页的其余部分 --%>

</BODY>
</HTML>
```
HTTP请求返回的Cookie数组会被扫描，以查找名为`airportCode`的Cookie。如果该Cookie存在，其值将替代默认的机场代码（RDU，代表北卡罗来纳州罗利/达勒姆）。接下来，声明`Observation` Bean：

```
<jsp:useBean id="wobs" class="jspcr.beans.weather.Observation">
```
并用选定的机场代码进行初始化：

```
<jsp:setProperty
    name="wobs"
    property="airportCode"
    value="<%= airportCode %>"/>
```
剩下的就是提取Bean的属性并将其写入输出流：

```
<jsp:getProperty name="wobs" property="location"/>
<jsp:getProperty name="wobs" property="time"/>
<jsp:getProperty name="wobs" property="temperature"/> C&deg;
```
图15-6展示了最终显示结果。

如果用户点击“Select City”超链接，将会展示一个已知有天气数据可用的机场列表，如图15-7所示。这不是一个JSP页面，只是一个简单的HTML表单，用于调用设置Cookie的JSP。表单的action属性指向`SetAirportCode.jsp`，这是一个非可视化的JSP页面，它会向用户发送新的机场代码Cookie，并重定向回门户页面，如下所示。

```
<%@ page session="false" %>
<%
    String airportCode = request.getParameter("airportCode");
    if (airportCode != null) {
        Cookie cookie = new Cookie("airportCode", airportCode);
        final int ONE_YEAR = 60 * 60 * 24 * 365;
        cookie.setMaxAge(ONE_YEAR);
        response.addCookie(cookie);
    }
    response.sendRedirect("Portal.jsp");
%>
```
如果Web用户恰好位于新墨西哥州罗斯威尔（或对在那里降落的天气状况感兴趣），并在机场选择框中选择了相应的行，那么机场代码Cookie的值将被设置为ROW。所有后续通过LyricNote门户的请求都将导致`Observation` Bean检索罗斯威尔工业航空中心机场的天气状况（见图15-8）。

## 总结
Java架构中的基于组件的编程使用JavaBeans。Bean编程模型使用公共的get和set方法来访问私有的Bean属性，使用事件监听器将其他类与Bean的状态链接起来，并使用序列化使Bean持久化。JSP编程环境提供了用于声明和访问Bean的标准标签：

- `<jsp:useBean>`
- `<jsp:setProperty>`
- `<jsp:getProperty>`

`useBean`标签可以声明、实例化和初始化一个Bean。该标签具有多种属性组合，使Bean可以从现有命名空间中提取、作为新实例创建，或从序列化对象中恢复。支持的命名空间包括页面作用域、请求作用域、会话作用域或应用作用域。

`setProperty`和`getProperty`用于存储和检索Bean的属性。除了字面字符串值外，属性也可以从表单参数和请求时表达式设置。

JavaBeans在JSP环境中提供了显著的优势。它们可以被单独编写和测试，然后在applet、servlet和独立应用程序上下文中重用。JavaBeans还减少了JSP脚本段和声明中暴露的Java代码量。结合Cookie、自定义标签和其他高级JSP技术，JavaBeans为开发有用的Web应用程序提供了可靠、高效的基础。

此页有意留白。

# 第16章：JSP与XML

451

版权所有 © 2001 McGraw-Hill Companies, Inc. 点击此处查看使用条款。



自1996年在万维网联盟（W3C）诞生并于1998年被采纳为W3C推荐标准以来，*可扩展标记语言（XML）*已确立了其作为结构化数据存储和交换的通用语言的地位。XML被用于网站内容管理、企业间数据交换，以及从建筑、财务报告到音乐等多样化的应用场景。除了应用本身，XML工具和扩展也正渗透到编程的各个方面。

本章探讨了将XML整合到Web应用中的一些方式。在概述部分之后，将讨论两种XML解析器模型，然后介绍XSL转换。这三项技术都将在解决同一HTML创建任务的三个方案中得到演示。

## XML概述

XML是一套使用用户自定义的标记标签集来描述结构化数据的系统。XML本身不是一种语言，而是一种定义专用语言的系统。它表面上看起来像HTML，HTML使用预定义的`<UL>`、`<LI>`、`<TABLE>`等标签来标记Web文档的各个部分。区别在于HTML有一组固定的标签，而XML允许你设计任何必要的标签集来描述你的数据。

例如，一首为声乐和钢琴创作的歌曲，其部分表示可能如下所示：

```xml
<?xml version="1.0"?>
<song>
  <title>The Birds</title>
  <words-by>Hilaire Belloc</words-by>
  <music-by>Benjamin Britten</music-by>

  <track name="Voices">
    <time-signature>2/2</time-signature>
    <tempo>Andante con moto</tempo>
    <measure>
      <rest duration="1"/>
    </measure>
    <measure>...</measure>
  </track>

  <track name="Piano">
    <time-signature>2/2</time-signature>
    <tempo>Andante con moto</tempo>
    <measure>
      <note duration="8" value="e" octave="2"/>
      <note duration="8" value="g#" octave="2"/>
      <note duration="8" value="c#" octave="3"/>
      <note duration="8" value="g#" octave="3"/>
      <note duration="2" value="f#" octave="3"/>
    </measure>
    <measure>...</measure>
  </track>
</song>
```

请注意，这种歌曲表示方式完全是结构性的——它与歌曲的呈现方式无关。实际上，同一个XML文档可以用于生成印刷乐谱，也可以用于在MIDI播放器中合成音调。

## XML解决的问题

早期的文本处理格式通常不区分内容和呈现。例如，RTF不仅包含用于表格和列表等结构化数据的代码，也包含用于字体和图形的代码。HTML也存在同样的问题。像`<table>`、`<tr>`和`<td>`这样具有特定宽度和高度属性的元素，通常被用来影响网页的物理布局，而不是用于以表格格式对相关项目进行分组。

这种方法的问题在于，随着新的输出格式需求的出现，文档中包含的格式信息就变得无用了。更糟糕的是，原本设计用于传达结构信息的标签被误用，仅仅利用它们的副作用，例如使用`<UL>`来产生缩进效果。

相比之下，XML完全专注于结构。特定的数据元素可以通过文本搜索应用程序被清晰地识别和提取。如果XML文档需要在Web浏览器上呈现，可以使用XSL样式表通过编程方式将其转换为HTML。如果文档需要用于事务处理系统，可以由XML解析器解析，该解析器会提取构成事务的特定字段。XML文档可以作为树结构浏览，也可以折叠成关系数据库表。只要使用文档的应用程序知道它所使用的语言（格式），应用程序就能找到并提取所需的数据。

## XML语法

XML很简单，其语法规则易于学习。一个XML文档由元素组成，每个元素都有一个开始标签、一个主体和一个结束标签，如下所示：

```xml
<tempo>Andante con moto</tempo>
```

*开始标签* `<tempo>`由一个用小于号和大于号括起来的标签名组成。*结束标签* `</tempo>`与开始标签相同，但在开大于号字符后跟一个斜杠。*主体*由开始标签和结束标签之间的所有内容组成。这可以包括普通文本或其他XML元素。

开始标签可以包含*属性*，它们是编码在开始标签内名称之后、闭合大于号字符之前的`name="value"`对：

```xml
<track name="voices"> ... </track>
```

XML中的属性*必须*用单引号或双引号括起来。

如果元素的主体为空，可以使用开始和结束标签的缩写形式。在这种形式中，结束标签中的斜杠被移入开始标签，位于闭合大于号字符之前，然后省略主体和结束标签。因此，以下两种形式在功能上是等效的：

```xml
<rest duration="1"></rest>
<rest duration="1"/>
```

元素可以嵌套在彼此内部，深度不限

```xml
<song>
    <track>
        <measure>...</measure>
    </track>
</song>
```

但它们的结束标签必须以与开始标签出现的精确相反的顺序出现。也就是说，元素不能重叠。以下情况是非法的：

```xml
<B><I>Do not do this!</B></I>
```

因此，一个格式良好的XML文档恰好包含一个外部元素，称为*文档元素*，它可以包含任意数量的正确嵌套的内部元素。

有关XML语法的完整细节，请查阅W3C在2000年10月6日的推荐标准中找到的XML 1.0规范第二版。该文档可在http://www.w3.org/TR/REC-xml找到。

## 文档类型定义

然而，XML不仅仅是一组自由形式的标签。显然，使用XML文档作为输入的应用程序需要知道它可以包含哪些元素，这些元素如何嵌套或重复，允许哪些属性，等等。同样，生成XML文档的应用程序（以及使用文本编辑器编写文档的人）也需要知道相同的结构信息。这就是*文档类型定义*（DTD）的作用。

DTD是特定文档类型中允许的标签和属性的定义。例如，备忘录文档的DTD可能会定义`<memo>`、`<from>`、`<to>`、`<subject>`、`<text>`和`<paragraph>`标签，指明`<paragraph>`元素只能出现在`<text>`元素内部，`<from>`和`<to>`是必需的，而其余是可选的。然后，生成备忘录文档的应用程序可以确保它们只生成语法正确的版本。同样，验证工具可以读取人工编写的备忘录文档并确定它们是否符合语法。这意味着接收端的应用程序可以依赖于理解文档并正确处理它。

XML文档通过在文档元素之前立即使用`<!DOCTYPE>`标签来指示它使用的DTD及其位置：

```xml
<?xml version="1.0"?>
<!DOCTYPE song SYSTEM "song.dtd">
<song>
  ...
</song>
```

DTD也可以嵌入到文档本身中

```xml
<?xml version="1.0"?>
<!DOCTYPE song [
  ...
]>
<song>
  ...
</song>
```

或者可以保存在公共存储库中：

```xml
<?xml version="1.0"?>
<!DOCTYPE song PUBLIC publicid URL>
<song>
  ...
</song>
```

DTD不是必需的，但如果存在，文档必须遵守它。用XML规范的术语来说，如果文档遵守语法规则（所有元素都已闭合、没有重叠元素、所有属性都加引号），则称该文档是*格式良好的*。如果文档有DTD，并且它格式良好且遵守DTD，则称该文档是*有效的*。

我们的`song`文档类型的DTD如下所示：

```
<!ELEMENT    song         (title?,words-by?,music-by?,track+)>
<!ELEMENT    title        (#PCDATA)>
<!ELEMENT    words-by     (#PCDATA)>
<!ELEMENT    music-by     (#PCDATA)>
<!ELEMENT    track        (time-signature|tempo|measure)*>
<!ATTLIST    track
            name         CDATA       #IMPLIED>
<!ELEMENT    time-signature (#PCDATA)>
<!ELEMENT    tempo        (#PCDATA)>
<!ELEMENT    measure      (note|rest)+>
<!ELEMENT    note         EMPTY>
<!ATTLIST    note
            duration     CDATA       #IMPLIED
            value        CDATA       #IMPLIED
            octave       (1|2|3|4|5|6|7|8) #REQUIRED>
<!ELEMENT    rest         EMPTY>
<!ATTLIST    rest
            duration     CDATA       #IMPLIED>
```

DTD由元素和属性的列表组成。每个元素定义给出元素名称，然后是对其可以包含的元素、它们的顺序、是否必需以及是否可以重复的严格描述。此描述可能采用以下几种形式：

- 普通文本表示为`(#PCDATA)`，即*已解析的字符数据*。
- 允许的子元素按顺序列出，用逗号分隔。
- 互斥的元素用逻辑或符号`|`分隔。
- 子元素和加括号的子元素列表后面可以跟重复计数：`?`表示零次或一次出现，`*`表示零次或多次，`+`表示一次或多次。
- 不能包含主体的元素描述为`EMPTY`。

例如，`<song>`元素允许包含可选的`<title>`、`<words-by>`和`<music-by>`元素，后跟一个或多个`<track>`元素：

```
<!ELEMENT    song         (title?,words-by?,music-by?,track+)>
```

请注意，子元素（如果存在）必须仅按指定的顺序出现。`<measure>`元素被定义为包含至少一个`<note>`或`<rest>`元素，后跟任意数量的`<note>`或`<rest>`重复：



## 文档对象模型（DOM）

*文档对象模型（DOM）*是W3C标准对内存中文档的表示方式。DOM并非仅将文档视为文本字符串，而是将其表示为节点树。该树可以按任意顺序遍历，节点可以添加或删除，并且修改后的DOM树可以保存为新文档。

DOM规范有不同版本，称为*级别*。*DOM Level 1*是核心功能集，提供了创建和访问文档元素的方法。*DOM Level 2*于2000年11月13日被批准为W3C推荐标准，增加了对命名空间的支持。

DOM不仅是一个标准，也是一种*应用程序编程接口（API）*。W3C发布了构成`org.w3c.dom`包的接口列表。因此，不同的供应商提供实现这些接口的解析器。流行的DOM解析器包括来自Apache软件基金会的Xerces，以及来自Sun Microsystems的JAXP。

DOM API由四类类和接口组成：

- 节点
- 节点集合
- 元数据
- 异常

要在应用程序中使用XML文档，您需要对其进行解析。XML解析器读取文档并将其分离为起始标签、属性、主体内容和结束标签。解析器提供应用程序编程接口，使您无需自己解释输入流的复杂性即可提取所需的元素。存在两种被广泛接受的XML解析器模型：

- **DOM** 文档对象模型
- **SAX** XML简单API

以下各节将分别介绍这些模型。

*文档对象模型（DOM）*是W3C标准对内存中文档的表示方式。DOM并非仅将文档视为文本字符串，而是将其表示为节点树。该树可以按任意顺序遍历，节点可以添加或删除，并且修改后的DOM树可以保存为新文档。

DOM规范有不同版本，称为*级别*。*DOM Level 1*是核心功能集，提供了创建和访问文档元素的方法。*DOM Level 2*于2000年11月13日被批准为W3C推荐标准，增加了对命名空间的支持。

DOM不仅是一个标准，也是一种*应用程序编程接口（API）*。W3C发布了构成`org.w3c.dom`包的接口列表。因此，不同的供应商提供实现这些接口的解析器。流行的DOM解析器包括来自Apache软件基金会的Xerces，以及来自Sun Microsystems的JAXP。

DOM API由四类类和接口组成：

- 节点
- 节点集合
- 元数据
- 异常

### 节点接口

DOM中关注的基本单元是*节点*。XML文档中的所有内容——单个元素、起始标签中的属性、注释、元素文本以及整个文档——都是节点。表16-1列出了Node接口中的方法。

| 方法 | 描述 |
|---|---|
| `Node appendChild(Node newChild) throws DOMException` | 将新子节点添加到当前节点。 |
| `Node cloneNode(boolean deep)` | 复制节点。如果deep为true，则递归克隆此节点下的所有子树。否则，仅克隆当前节点。 |
| `NamedNodeMap getAttributes()` | 如果节点是`Element`，则返回该节点的命名属性。否则，返回`null`。 |
| `NodeList getChildNodes()` | 返回所有直接子节点的列表。 |
| `Node getFirstChild()` | 返回第一个子节点，或者如果此节点不是Element，则返回null。 |
| `Node getLastChild()` | 返回最后一个子节点，或者如果此节点不是Element，则返回null。 |
| `Node getNextSibling()` | 返回同一父节点的下一个子节点，或者如果父节点不是Element，则返回null。 |
| `String getNodeName()` | 返回节点的名称，适用于Element、Attr和Entity等命名节点类型。对于Text、CDATAsection和Comment等未命名类型，分别返回#text、#cdata-section和#comment。 |
| `int getNodeType()` | 返回一个整数常量，指示此节点的具体类型。返回的值是Node接口中定义的以下常量之一：ATTRIBUTE_NODE, CDATA_SECTION_NODE, COMMENT_NODE, DOCUMENT_FRAGMENT_NODE, DOCUMENT_NODE, DOCUMENT_TYPE_NODE, ELEMENT_NODE, ENTITY_NODE, ENTITY_REFERENCE_NODE, NOTATION_NODE, PROCESSING_INSTRUCTION_NODE, TEXT_NODE。 |
| `String getNodeValue()` | 对于属性和文本类型节点，返回文本，否则返回`null`。 |
| `Document getOwnerDocument()` | 返回此节点所属文档的`Document`节点。 |
| `Node getParentNode()` | 返回直接父节点，或者如果这是`Document`、`DocumentFragment`或`Attr`节点，则返回`null`。尚未添加到文档的新节点也可能有`null`父节点。 |
| `Node getPreviousSibling()` | 返回同一父节点的上一个子节点，或者如果父节点不是`Element`，则返回`null`。 |
| `boolean hasChildNodes()` | 如果此节点具有非空的子节点列表，则返回`true`。 |
| `Node insertBefore(Node child, Node beforeNode)` | 在指定节点之前插入新的子节点。`beforeNode`可以是`null`，在这种情况下，子节点将附加到列表末尾。 |
| `Node removeChild(Node child) throws DOMException` | 从子节点列表中移除指定节点。如果该节点不是当前节点的子节点，则抛出异常。 |
| `Node replaceChild(Node newChild, Node oldChild) throws DOMException` | 移除`oldChild`并用`newChild`替换它。如果该节点不是当前节点的子节点，则抛出异常。 |
| `void setNodeValue(String value) throws DOMException` | 设置当前节点的值。 |

在DOM Level 2中，`Node`有两个新方法——`isSupported()`和`hasAttributes()`——现在还包含`normalize()`方法，该方法以前是`Element`接口的一部分。

`Node`有13个专门的子接口，对应于XML文档中可能出现的特定节点类型。这些接口列在表16-2中。

| 接口 | 描述 |
|---|---|
| `Attr` | `Element`节点的属性。`Attr`具有检索属性名称和值的方法。在DOM Level 2中，`Attr`接口包含`getOwnerElement()`方法。 |
| `CDATASection` | 在XML文档中用`<![CDATA[ ... ]]>`转义语法括起来的文本节点。CDATA部分逐字解析而不被求值。它们允许文档内容包含否则会被解释为XML的字符和字符串。 |
| `CharacterData` | 三种包含文本的节点类型`Text`、`Comment`和`CDATASection`的公共超接口。提供获取和设置字符内容以及确定数据长度的方法。 |
| `Comment` | 包含XML注释的节点。`Comment`值不包括`<!--`和`-->`分隔符，仅包括注释文本（包括空格）。 |
| `Document` | `Document`节点表示整个XML文档。一个DOM实例中只有一个`Document`节点。DOM Level 2为`Document`接口添加了对命名空间的支持。 |
| `DocumentFragment` | 用于构建Document节点子树的临时节点。此接口没有方法。 |
| `DocumentType` | 表示文档开头的`<!DOCTYPE>`元素的节点。此接口提供获取DTD名称、实体以及DTD中定义的符号的方法。 |
| `Element` | Node最常见的子接口。表示XML起始标签、主体和结束标签。除了从Node继承的方法外，Element还有用于设置和检索起始标签中出现的属性的方法。在DOM Level 2中，Element包含许多命名空间感知的方法。 |
| `Entity` | 在XML文档中使用的外部组件，例如图像文件。DOM Level 1仅为此节点类型提供最低限度的支持。 |
| `EntityReference` | 对未求值实体的引用（名称或指针）。此接口仅充当文档中的占位符；它不定义任何方法。 |
| `Notation` | 表示在DTD中声明的符号。符号描述外部实体的格式。 |
| `ProcessingInstruction` | XML文档中的处理器特定指令。处理指令采用`<?target [data]?>`语法。 |
| `Text` | 文本节点包含元素主体的字符内容。 |

### 节点集合接口

各种DOM API方法返回节点集合，可以是有序列表或名称到节点的映射。两个接口表示这些集合：表16-3所示的`NodeList`，以及表16-4所示的`NamedNodeMap`。



## 表 16-3。NodeList 接口定义的方法

| 方法 | 描述 |
|---|---|
| `int getLength()` | 返回列表中节点的数量。 |
| `Node item(int n)` | 返回列表中第 *n* 个节点，节点编号从 0, 1, ... 开始。 |

## 表 16-4。NamedNodeMap 接口定义的方法

| 方法 | 描述 |
|---|---|
| `int getLength()` | 返回列表中节点的数量。 |
| `Node item(int n)` | 返回列表中第 *n* 个节点，节点编号从 0, 1, ... 开始。 |
| `Node getNamedItem(String name)`<br>`void setNamedItem(Node item)`<br>`void removeNamedItem(String name)` | 获取、设置或移除具有指定名称的节点。如果集合中不存在该节点，`getNamedItem()` 将返回 `null`。 |

DOM Level 2 中的 `NamedNodeMap` 接口支持命名空间中的限定项名称。

### 节点元数据

XML 特性可能是特定于版本的。为了确定 DOM 配置，DOM 提供了一个接口，使你能够查询它支持哪些特性。这个接口名为 `DOMImplementation`。目前，它包含一个方法

```
boolean hasFeature(String feature, String version)
```

如果支持指定特性的指定级别，则该方法返回 `true`。DOM Level 2 为 `DOMImplementation` 添加了两个新方法以支持创建文档。

464 JSP: The Complete Reference

### 异常

DOM 定义了一个名为 `DOMException` 的单一异常类。这是 `RuntimeException` 的一个子类，这意味着编译器不会要求可能抛出此异常的方法声明它或将它包含在 try/catch 块中。

### DOM 使用

一个典型的面向 DOM 的应用程序会创建一个 DOM 解析器实例，然后指示它解析一个 XML 输入源以创建 DOM 树。一旦树被创建，应用程序就可以遍历它，检查其内容并提取所需信息。

实例化解析器的方式是特定于实现的。它可以直接使用 new 运算符创建。更高层次的方法可以通过 Sun Microsystems 定义的 Java XML API (JAXP) 包装器使用。在 JAXP 下，应用程序创建一个 `DocumentBuilderFactory` 实例，可选地设置其 `namespaceAware` 和/或 `validating` 属性，然后使用该工厂获取解析器实例。该工厂会找到一个匹配所需特性的 DOM 解析器类。

因此，要使用 DOM 解析 XML 文档，应用程序可以这样做：

```java
DocumentBuilderFactory factory =
    DocumentBuilderFactory.newInstance();
DocumentBuilder builder = factory.newDocumentBuilder();
Document document = builder.parse(fileName);
Element root = document.getDocumentElement();
```

让我们看一个在 JSP 页面中使用 DOM 进行 XML 解析的例子。以下 XML 文档摘自 LyricNote 产品目录，可能是数据库查询的结果。它包含一个由产品代码标识的乐器列表。对于每种乐器，文档包含价格、库存数量、制造商名称和产品描述。此处列表是缩略的；完整列表包含 82 个条目。

```xml
<?xml version="1.0"?>
<!DOCTYPE products PUBLIC "-//jsppcr//products//EN"
    "http://u25nv/jsppcr/Chap16/examples/products/products.dtd">
<products>
    <product code="001000">
        <product-type>IN</product-type>
        <price>537.00</price>
        <on-hand>48</on-hand>
        <manufacturer>Clemens-Altman</manufacturer>
        <description>Silver Flute - Student</description>
    </product>
    <product code="001010">
        <product-type>IN</product-type>
        <price>876.00</price>
        <on-hand>83</on-hand>
        <manufacturer>Gabriel</manufacturer>
        <description>Silver Flute</description>
    </product>
    ...
    <product code="001790">
        <product-type>IN</product-type>
        <price>165.50</price>
        <on-hand>94</on-hand>
        <manufacturer>Roush and Sons</manufacturer>
        <description>Cello case (1/2 size)</description>
    </product>
</products>
```

JSP 解析文档并仅提取制造商为 Clemens-Altman 的产品。它将此子集安排在 HTML 表格中，列包括产品代码、描述和价格。由于文档由一组产品元素组成，一种合乎逻辑的方法是解析文档并将其转换为 `Product` 对象的集合。`Product` 对象将具有与每个产品块中 XML 元素对应的字段。让 `Product` 对象辅助解析也是合理的。因为 DOM 创建一个树结构，你可以简单地定位每个 `<product>` 元素，创建一个 `Product` 对象，并调用其 `load()` 方法，将 DOM 元素作为参数传递。

以下显示了 `Product` 对象。除了 `load()` 方法外，`Product` 还包含其每个私有字段的 get 和 set 方法。

```java
package jspcr.xml.samples;

import org.w3c.dom.*;

public class Product
{
    private String code;
    private String productType;
    private double price;
    private int onHand;
    private String manufacturer;
    private String description;

    /**
     * Load the product data from a DOM element
     */
    public void load(org.w3c.dom.Element element)
    {
        code = element.getAttribute("code");
        for (Node node = element.getFirstChild();
             node != null;
             node = node.getNextSibling())
        {
            // Select only element nodes
            if (node.getNodeType() != Node.ELEMENT_NODE)
                continue;

            String tagName = node.getNodeName();

            // product-type
            if (tagName.equals("product-type")) {
                String text = node.getFirstChild().getNodeValue();
                productType = text.trim();
            }
            // price
            else
            if (tagName.equals("price")) {
                String text = node.getFirstChild().getNodeValue();
                price = Double.parseDouble(text.trim());
            }
            // on-hand
            else
            if (tagName.equals("on-hand")) {
                String text = node.getFirstChild().getNodeValue();
                onHand = Integer.parseInt(text.trim());
            }
            // manufacturer
            else
            if (tagName.equals("manufacturer")) {
                String text = node.getFirstChild().getNodeValue();
                manufacturer = text.trim();
            }
            // description
            else
            if (tagName.equals("description")) {
                String text = node.getFirstChild().getNodeValue();
                description = text.trim();
            }
        }
    }
    // Not shown here - get and set methods
}
```

■ code 字段很容易获取，因为它是产品元素的属性。你所要做的就是调用元素的 **getAttribute("code")** 方法。其他字段稍微复杂一些，因为它们的值位于产品子元素的文本节点下。我们的方法是循环遍历产品元素的子节点，将每个节点的名称与你需要填充的字段名称进行比较。这个循环可以通过几种方式完成：调用产品元素的 **getChildNodes()** 方法，它返回一个 NodeList 对象。NodeList 有一个 **getLength()** 方法，它告诉我们节点数量，以及一个 **item(int index)** 方法，它返回列表中指定索引处的节点。

■ 调用产品元素的 **getFirstChild()** 方法，然后依次调用每个子节点的 **getNextSibling()** 方法，直到它返回 null。

我们的代码使用了第二种方法。

要获取文本节点值，你可以利用每个数据元素没有子元素，只有已解析的字符数据这一事实。因此，你可以调用每个数据元素的 getFirstChild() 方法，并知道你会得到一个文本节点。文本本身可以通过 getNodeValue() 方法获得。现在，有了这个支持 XML 的产品元素，你就可以解析产品目录 XML 文档并执行我们的查询了。以下是 JSP 页面：

```jsp
<%@ page session="false" %>
<%@ page import="java.io.*" %>
<%@ page import="java.net.*" %>
<%@ page import="java.text.*" %>
<%@ page import="javax.xml.parsers.*" %>
<%@ page import="jspcr.xml.samples.*" %>
<%@ page import="org.w3c.dom.*" %>
<%@ page import="org.xml.sax.*" %>
<%
    long stime = System.currentTimeMillis();
%>
<HTML>
<HEAD>
<TITLE>(DOM) Clemens-Altman Musical Instruments</TITLE>
</HEAD>
<BODY>
<CENTER>
<H3>Clemens-Altman Musical Instruments</H3>
<H4>(Powered by DOM Level 1)</H4>
<TABLE BORDER="1" CELLPADDING="3" CELLSPACING="0">
<TR>
    <TH>Product Code</TH>
    <TH>Description</TH>
    <TH>Price</TH>
</TR>
<%
    // Get a new document builder
    DocumentBuilderFactory factory =
        DocumentBuilderFactory.newInstance();
    DocumentBuilder builder = factory.newDocumentBuilder();

    // Define the input source to be an XML document named
    // "instruments.xml" in the same directory as this JSP
```



# 第16章：JSP与XML

```java
StringBuffer requestURL = HttpUtils.getRequestURL(request);
URL jspURL = new URL(requestURL.toString());
URL url = new URL(jspURL, "instruments.xml");
InputSource is = new InputSource(url.openStream());
```

```java
// 加载文档
Document document = builder.parse(is);
Element root = document.getDocumentElement();
root.normalize();
```

```java
// 定义货币格式化器
NumberFormat fmt = NumberFormat.getCurrencyInstance();
```

```java
// 选择制造商为"Clemens-Altman"的产品代码、描述和价格
for (
    Node node = root.getFirstChild();
    node != null;
    node = node.getNextSibling())
{
    // 忽略除product元素外的所有节点
    if (node.getNodeType() != Node.ELEMENT_NODE)
        continue;

    Element productElement = (Element) node;
    if (!productElement.getTagName().equals("product"))
        continue;

    // 加载product对象
    Product product = new Product();
    product.load(productElement);

    // 检查制造商是否为"Clemens-Altman"
    String text = product.getManufacturer();
    if (!text.equals("Clemens-Altman"))
        continue;

    // 获取产品代码、价格和项目名称
    String code = product.getCode();
    String description = product.getDescription();
    double price = product.getPrice();
%>
<TR>
    <TD><%= code %></TD>
    <TD><%= description %></TD>
    <TD ALIGN="RIGHT"><%= fmt.format(price) %></TD>
</TR>
<%
    }
%>
</TABLE>
<P>
<%
    long etime = System.currentTimeMillis();
    double elapsed = (etime - stime)/1000.0;
%>
<EM>耗时: <%= elapsed %> 秒</EM>
</CENTER>
</BODY>
</HTML>
```

在生成表格标题后，JSP页面使用JAXP方法创建了DOM DocumentBuilder的实例：

```java
DocumentBuilderFactory factory =
    DocumentBuilderFactory.newInstance();
DocumentBuilder builder = factory.newDocumentBuilder();
```

产品目录XML文档位于与JSP页面同一目录下名为`instruments.xml`的文件中。你可以使用`HttpUtils.getRequestURL()`方法获取JSP的URL来定位它，然后使用双参数的URL构造函数将XML文件获取为URL：

```java
StringBuffer requestURL = HttpUtils.getRequestURL(request);
URL jspURL = new URL(requestURL.toString());
URL url = new URL(jspURL, "instruments.xml");
InputSource is = new InputSource(url.openStream());
```

`InputSource`是一个便捷类，它封装了一个字节流、一个字符流或一个文件名。定义了文档构建器和输入源后，就可以进行解析了：

```java
Document document = builder.parse(is);
Element root = document.getDocumentElement();
```

可以通过`document.getDocumentElement()`方法获取根`<products>`元素。现在，遍历`<products>`元素的直接子节点，搜索`<product>`元素。尽管查看XML文档表明你不会找到其他内容，但事实并非如此。文本节点分隔了每个`<product>`块。

```java
for (
    Node node = root.getFirstChild();
    node != null;
    node = node.getNextSibling())
{
    if (node.getNodeType() != Node.ELEMENT_NODE)
        continue;
    Element productElement = (Element) node;
    if (!productElement.getTagName().equals("product"))
        continue;
```

一旦找到一个`<product>`元素，你就可以创建一个`Product`对象，并让它遍历子元素以寻找所需信息：

```java
Product product = new Product();
product.load(productElement);
```

此时，你可以从`Product`对象中获取所需的所有信息。你可以判断其制造商是否为"Clemens-Altman"，如果是则将其打印在表格中。结果如图16-1所示。

DOM作为解析模型的主要优点在于它提供了对文档结构的随机访问。然而，这正是其最大缺点——整个文档必须被读取和解析后，才能通过DOM API访问其任何部分。对于大型文档，这种开销可能非常显著。

![](img/7a2f73369bb140583c7288b73456addb_498_0.png)

## 简单XML API（SAX）

SAX提供了另一种解析方法。SAX解析器不是从XML文档创建树，而是读取文件，并在发生特定解析事件时通知注册的监听器。这些事件包括：

- 文档开始
- 在新元素的开头读取开始标签
- 在元素的结尾读取结束标签
- 读取元素正文中的文本
- 读取注释
- 到达文档末尾

SAX接口为所有这些事件定义了方法。希望处理特定事件的应用程序可以实现一个或多个方法，然后注册为文档的处理器。当事件发生时，处理器的方法将使用当前正在解析的元素的值进行调用。这使得SAX非常适合需要很少或不需要文档上下文的过滤类应用程序。

与DOM一样，SAX API也在持续发展。SAX 1.0于1998年5月从XML-DEV邮件列表的设计讨论中诞生。SAX 2.0规范于2000年5月发布。虽然SAX不是W3C的官方规范，但它被广泛接受，并且在大多数解析器中通常与DOM一起提供。事实上，DOM解析器通常构建在SAX解析器之上，而用于DOM的JAXP `DocumentBuilder`接口也使用了几个SAX类。

### SAX解析器

基本的SAX接口是`Parser`。SAX API的实现将提供一个实现`Parser`的具体类。此接口定义了注册要使用的各种处理程序类的方法，并定义了两种形式的`parse()`方法，如表16-5所示。

| 方法 | 描述 |
|---|---|
| `void parse(InputSource is) throws SAXException, IOException` | 使解析器开始解析由指定输入源提供的文档。 |
| `void parse(String systemId) throws SAXException, IOException` | 使解析器开始解析指定系统ID中引用的文档。这可以是文件名或完全解析的URL。 |
| `void setDocumentHandler(DocumentHandler handler)` | 为此解析器注册一个文档处理器。 |
| `void setDTDHandler(DTDHandler handler)` | 为此解析器注册一个DTD处理器。 |
| `void setEntityResolver(EntityResolver resolver)` | 为此解析器注册一个实体解析器。`EntityResolver`可用于以自定义方式定位外部实体。 |
| `void setErrorHandler(ErrorHandler handler)` | 注册一个用于自定义错误处理的错误处理器。 |
| `void setLocale(Locale locale) throws SAXException` | 指定用于错误和警告的区域设置。 |

**表16-5.** *SAX解析器接口中的方法*

### 处理器

四个接口处理解析事件：

- `DocumentHandler`定义了文档开始和结束、每个XML元素开始和结束、文档文本以及空白、注释和处理指令的回调方法。
- `ErrorHandler`定义了致命错误、可恢复错误和警告错误的回调。
- `EntityResolver`允许对文档类型定义等外部实体进行自定义处理。
- `DTDHandler`接收文档类型定义中符号声明和未解析实体声明的通知。

其中，最常用的是第一个`DocumentHandler`。应用程序可以实现此接口，然后使用`setDocumentHandler()`方法将其自身注册到解析器，以开始接收回调。`DocumentHandler`中的方法如表16-6所述。

除了这四个处理器接口外，SAX API还为它们全部提供了一个默认实现——名为`HandlerBase`。应用程序通常会继承`HandlerBase`，并且只实现那些必要的方法。通常，这仅包括`startElement()`、`characters()`和`endElement()`方法。



## 表 16-6. DocumentHandler 定义的方法

| 方法 | 描述 |
| --- | --- |
| void characters(char [] ch, int start, int len) throws SAXException | 此方法被 XML 解析器调用，用于读取元素文本中的字符数据。字符数据从 `ch` 数组的 `start` 位置开始，长度为 `len`。方便的是，`java.lang.String` 构造函数也使用这三个字段。 |
| void endDocument() throws SAXException | 当解析器完成文档解析时调用。 |
| void endElement(String name) throws SAXException | 当解析到当前元素的结束标签时调用。标签名作为参数传递。 |
| void ignorableWhitespace(char [] ch, int start, int len) throws SAXException | 此方法被 XML 解析器调用，用于读取无意义的字符数据。字符数据从 `ch` 数组的 `start` 位置开始，长度为 `len`。 |
| void processingInstruction(String target, String data) throws SAXException | 当遇到处理指令时调用。 |
| void setDocumentLocator(Locator locator) | 将解析过程中使用的 `Locator` 信息通知文档处理器。`Locator` 提供行号和列号信息，在解析错误时非常有用。 |
| void startDocument() throws SAXException | 当解析器开始解析新文档时调用。 |
| void startElement(String name, AttributeList attrs) throws SAXException | 当解析器遇到新元素的开始标签时调用。传递的参数包括标签名和名称/值属性对。 |

### SAX 使用

典型的面向 SAX 的应用程序会创建一个 SAX 解析器实例，注册文档处理器，然后调用 `parse()` 方法以开始解析和回调。在本节中，你将开发与 DOM 部分相同的产品目录示例。你仍然使用 `Product` 对象，但仅用于存储产品属性，而不执行任何解析操作。

```
<%@ page session="false" %>
<%@ page import="java.io.*" %>
<%@ page import="java.net.*" %>
<%@ page import="java.text.*" %>
<%@ page import="java.util.*" %>
<%@ page import="javax.xml.parsers.*" %>
<%@ page import="jspcr.xml.samples.*" %>
<%@ page import="org.xml.sax.*" %>
<%
    long stime = System.currentTimeMillis();
%>
<HTML>
<HEAD>
<TITLE>(SAX 1.0) Clemens-Altman 乐器</TITLE>
</HEAD>
<BODY>
<CENTER>
<H3>Clemens-Altman 乐器</H3>
<H4>(由 SAX 1.0 驱动)</H4>
<TABLE BORDER="1" CELLPADDING="3" CELLSPACING="0">
<TR>
    <TH>产品代码</TH>
    <TH>描述</TH>
    <TH>价格</TH>
</TR>
<%
    // 获取一个新的 SAX 解析器

    SAXParserFactory factory = SAXParserFactory.newInstance();
    SAXParser parser = factory.newSAXParser();

    // 定义输入源为与本 JSP 文件位于同一目录下的名为 "instruments.xml" 的 XML 文档

StringBuffer requestURL = HttpUtils.getRequestURL(request);
URL jspURL = new URL(requestURL.toString());
URL url = new URL(jspURL, "instruments.xml");
InputSource is = new InputSource(url.openStream());

// 解析输入源

parser.parse(is, new ProductParser(out));
%>
</TABLE>
<P>
<%
    long etime = System.currentTimeMillis();
    double elapsed = (etime - stime)/1000.0;
%>
<EM>耗时：<%= elapsed %> 秒</EM>
</CENTER>
</BODY>
</HTML>
<%!

// 内部类，用于解析 XML 输入源
class ProductParser extends HandlerBase
{
    private Product product;
    private StringBuffer buffer;
    private JspWriter out;
    private NumberFormat fmt;

    public ProductParser(JspWriter out)
    {
        this.out = out;
        buffer = new StringBuffer();
        fmt = NumberFormat.getCurrencyInstance();
    }

    /**
     * 遇到开始标签时调用
     */
    public void startElement(String name, AttributeList attrs)
    throws SAXException
    {
        if (name.equals("product")) {
            product = new Product();
            product.setCode(attrs.getValue("code"));
        }
        buffer = new StringBuffer();
    }

    /**
     * 累积文本节点中的字符
     */
    public void characters(char[] ch, int start, int len)
        throws SAXException
    {
        buffer.append(ch, start, len);
    }

    /**
     * 遇到结束标签时调用
     */
    public void endElement(String name)
        throws SAXException
    {
        String text = buffer.toString().trim();
        if (name.equals("price"))
            product.setPrice(Double.parseDouble(text));
        else if (name.equals("manufacturer"))
            product.setManufacturer(text);
        else if (name.equals("description"))
            product.setDescription(text);
        else if (name.equals("product")) {
            if (product.getManufacturer().equals("Clemens-Altman")) {
                try {
                    String[] lines = {
                        "<TR>",
                        "<TD>", product.getCode(), "</TD>",
                        "<TD>", product.getDescription(), "</TD>",
                        "<TD ALIGN='RIGHT'>",
                        fmt.format(product.getPrice()), "</TD>",
                        "</TR>",
        };
        for (int i = 0; i < lines.length; i++)
            out.println(lines[i]);
    }
    catch (IOException e) {
        throw new SAXException(e.getMessage());
    }
}
}
}
}%>
```

## JSP：权威指南

与 `DOMBuilderFactory` 和 `DOMBuilder` 类似，`SAXParserFactory` 和 `SAXParser` 可以通过 JAXP 调用：

```
    SAXParserFactory factory = SAXParserFactory.newInstance();
    SAXParser parser = factory.newSAXParser();
```

请记住，SAX 技术的核心是实现 `DocumentHandler`（或扩展 `HandlerBase`）并为感兴趣的解析事件方法提供回调。可以使用内部类来实现这一点。JAXP 的 `parse()` 方法将我们的 `ProductParser` 类注册为文档处理器，然后开始解析：

```
    parser.parse(is, new ProductParser(out));
```

`ProductParser` 类关注三个事件：

- **startElement**：在新的 `<product>` 元素开始时，你需要创建一个 `Product` 对象并将 `code` 属性存储其中。
- **characters**：当文本数据流经时，你需要将其累积到 `StringBuffer` 中。
- **endElement**：在元素结束时，如果它是产品字段之一，你需要从 `StringBuffer` 中分配其值。如果这是 `<product>` 元素的结束，你可以在 HTML 表格中打印产品信息，清除缓冲区，并等待解析下一个产品。

生成的 HTML 表格如图 16-2 所示。注意与图 16-1 中的 DOM 版本相比，耗时有所不同。

![图 16-2. 使用 XML SAX 1.0 解析器进行产品目录搜索](img/7a2f73369bb140583c7288b73456addb_506_0.png)

### SAX 2.0

SAX 规范的更新版本于 1998 年 5 月通过。SAX 2.0 的主要改进是对命名空间的支持。*命名空间* 是具有共同前缀的标签组，用于区分那些可能具有相同名称但无此前缀的其他标签。这允许定义 XML 标签包，而无需担心与同名标签发生冲突。

从 API 角度看，SAX 2.0 弃用了 `Parser`、`DocumentHandler` 和 `AttributeList` 接口，分别替换为支持命名空间的 `XMLReader`、`ContentHandler` 和 `Attributes` 接口。

正如你可能预料的，并非所有 XML 产品都已跟上最新的 DOM 和 SAX 级别。截至 2000 年 11 月，JAXP 尚未支持 SAX 2.0，除非在早期访问包中。Xerces-J 1.2.1 版本本身支持 SAX 2.0，但通过 Xerces 版本的 JAXP 尚不支持（该版本仍仅适用于 SAX 1.0）。请查阅 Sun、W3C 和 xml.apache.org 网站以获取更新版本。

在 SAX 2.0 中，我们的产品目录 JSP 页面如下所示：

```
<%@ page session="false" %>
<%@ page import="java.io.*" %>
<%@ page import="java.net.*" %>
<%@ page import="java.text.*" %>
<%@ page import="java.util.*" %>
<%@ page import="jspcr.xml.samples.*" %>
<%@ page import="org.xml.sax.*" %>
<%@ page import="org.xml.sax.helpers.*" %>
<%
    long stime = System.currentTimeMillis();
%>
<HTML>
<HEAD>
<TITLE>(SAX 2.0) Clemens-Altman 乐器</TITLE>
</HEAD>
<BODY>
<CENTER>
<H3>Clemens-Altman 乐器</H3>
<H4>(由 SAX 2.0 驱动)</H4>
<TABLE BORDER="1" CELLPADDING="3" CELLSPACING="0">
<TR>
    <TH>产品代码</TH>
    <TH>描述</TH>
    <TH>价格</TH>
</TR>
<%
    // 获取一个新的 SAX 解析器

    XMLReader parser = new org.apache.xerces.parsers.SAXParser();
    DefaultHandler handler = new ProductParser(out);
    parser.setContentHandler(handler);
    parser.setErrorHandler(handler);

    // 定义输入源为名为
```



## 482 JSP：完整参考

```java
// 与此 JSP 位于同一目录下的 "instruments.xml"

StringBuffer requestURL = HttpUtils.getRequestURL(request);
URL jspURL = new URL(requestURL.toString());
URL url = new URL(jspURL, "instruments.xml");
InputSource is = new InputSource(url.openStream());

// 解析输入源

parser.parse(is);
%>
</TABLE>
<P>
<%
    long etime = System.currentTimeMillis();
    double elapsed = (etime - stime)/1000.0;
%>
<EM>耗时：<%= elapsed %> 秒</EM>
</CENTER>
</BODY>
</HTML>
<%!

// 解析 XML 输入源的内部类

class ProductParser extends DefaultHandler
{
    private Product product;
    private StringBuffer buffer;
    private JspWriter out;
    private NumberFormat fmt;

    public ProductParser(JspWriter out)
    {
        this.out = out;
        buffer = new StringBuffer();
        fmt = NumberFormat.getCurrencyInstance();
    }

    /**
     * 遇到开始标签时调用
     */
    public void startElement(
        String namespaceURI,
        String localName,
        String qName,
        Attributes attrs)
    throws SAXException
    {
        if (qName.equals("product")) {
            product = new Product();
            product.setCode(attrs.getValue("code"));
        }
        buffer = new StringBuffer();
    }

    /**
     * 从文本节点累积字符
     */
    public void characters(char[] ch, int start, int len)
        throws SAXException
    {
        buffer.append(ch, start, len);
    }

    /**
     * 遇到结束标签时调用
     */
    public void endElement(
        String namespaceURI,
        String localName,
        String qName)
    throws SAXException
    {
        String text = buffer.toString().trim();
        if (qName.equals("price"))
            product.setPrice(Double.parseDouble(text));
        else if (qName.equals("manufacturer"))
            product.setManufacturer(text);
        else if (qName.equals("description"))
            product.setDescription(text);
        else if (qName.equals("product")) {
            if (product.getManufacturer().equals("Clemens-Altman")) {
                try {
                    String[] lines = {
                        "<TR>",
                        "<TD>", product.getCode(), "</TD>",
                        "<TD>", product.getDescription(), "</TD>",
                        "<TD ALIGN='RIGHT'>",
                        fmt.format(product.getPrice()), "</TD>",
                        "</TR>",
                    };
                    for (int i = 0; i < lines.length; i++)
                        out.println(lines[i]);
                }
                catch (IOException e) {
                    throw new SAXException(e.getMessage());
                }
            }
        }
    }
}
%>
```

关键区别在于解析器的调用方式

```java
XMLReader parser = new org.apache.xerces.parsers.SAXParser();
DefaultHandler handler = new ProductParser(out);
parser.setContentHandler(handler);
parser.setErrorHandler(handler);
```

以及回调方法的签名：

```java
public void startElement(
    String namespaceURI, String localName, String qName,
    Attributes attrs)
    throws SAXException
...
public void endElement(
    String namespaceURI, String localName, String qName)
    throws SAXException
```

如图 16-3 所示，生成输出的速度比 SAX 1.0 稍快。

第 16 章：JSP 与 XML 485

![img](img/7a2f73369bb140583c7288b73456addb_511_0.png)

| 产品代码 | 描述 | 价格 |
| :--- | :--- | :--- |
| 001000 | 银质长笛 - 学生用 | $537.00 |
| 001060 | 降 B 调小号 | $460.00 |
| 001080 | 军号 | $213.00 |
| 001100 | 标准大号 | $1,359.00 |
| 001140 | 降 B 调单簧管 - 木质 | $522.00 |
| 001170 | 降 E 调单簧管 | $307.00 |
| 001180 | 巴松管 | $849.00 |
| 001190 | 低音巴松管 | $886.00 |
| 001230 | 塑料竖笛 | $30.00 |
| 001310 | 高音萨克斯管 | $423.00 |
| 001320 | 长号 | $760.50 |

**图 16-3.** 使用 XML SAX 2.0 解析器的产品目录搜索

SAX 相对于 DOM 具有许多优势。它更简单、更易于学习，内存使用量小得多，并且不需要加载整个文档。几乎所有的 XML 解析器都具有 SAX 接口；而具有 DOM 接口的则较少。SAX 也非常适合读取格式错误的文档（如大多数 HTML）。

## 使用 XSLT 的 XSL 转换

如前所述，XML 的设计纯粹是为了标识文档结构，而不是文档外观。然而，显然 XML 和 HTML 密切相关，并且 XML 文档可以转换为 HTML。当发生这种情况时，可以添加样式信息。这就是可扩展样式表语言（XSL）的角色。

XSL 是一种用于设计样式表的语言。XSL 样式表系统地描述了将哪些格式化元素应用于 XML 源文档中的哪些元素，以产生所需的 HTML 输出。不足为奇，XSL 样式表本身就是一个 XML 文档。

虽然 XSL 最初是为样式表目的而设计的，但很明显它也可以用于通用的 XML 结构转换。这种操作由 XSL 转换处理器（XSLT）执行。XSLT 在 1999 年 11 月的 W3C 推荐标准中定义（参见 http://www.w3.org/TR/xslt.html）。流行的 XSLT 处理器可从 Apache 软件基金会（Xalan）、Microsoft（MSXML）、Michael Kay（Saxon）和 James Clark（XT）获得。

XSLT 是一个广泛的主题，也是许多书籍和文章的主题。本书仅为您提供了基本介绍，仅足以让您阅读 XSLT 样式表（如果您需要这样做）。

XSLT 使用一个称为 XSL 样式表的 XML 文档来描述它修改的内容以及如何修改。样式表中有一个或多个模板，这些模板标识它们旨在转换的特定 XML 元素，然后提供一组字面量和嵌套的 XSL 语句，以指示输出的格式。关键的 XSLT 指令列于表 16-7。

| 指令 | 描述 |
|---|---|
| `<xsl:stylesheet>` | XSL 样式表中的最外层文档元素。必需属性是 xmlns:xsl（XSL 标签的命名空间）和 version。 |
| `<xsl:template>` | 标识一个模板块。可选属性是 match，它指定模板匹配的 XML 元素。存在多种丰富的表达式匹配值的方式。有关详细信息，请参阅 XSLT 规范。 |

表 16-7. XSLT 指令要点

| 指令 | 描述 |
| :--- | :--- |
| `<xsl:apply-templates>` | 导致处理器寻找其他元素以进行匹配。可选属性是 `select`，它以与 `<xsl:template>` match 属性相同的语言指定元素的子集。 |
| `<xsl:value-of>` | 导致处理器替换指定元素的值。可选属性是 `select`，其操作与 `<xsl:apply-templates>` 中的相同。 |

表 16-7. XSLT 指令要点（续）

### XSLT 实战

我们可以用 XSLT 做与用于说明 DOM 和 SAX 相同的示例。以下是 XSL 样式表：

```xml
<?xml version="1.0"?>

<xsl:stylesheet
    xmlns:xsl="http://www.w3.org/1999/XSL/Transform"
    version="1.0">

<xsl:output method="html"/>

<xsl:template match="/">
<TABLE BORDER="1" CELLPADDING="3" CELLSPACING="0">
<TR>
    <TH>产品代码</TH>
    <TH>描述</TH>
    <TH>价格</TH>
</TR>
<xsl:apply-templates
    select="//product[manufacturer='Clemens-Altman']"/>
</TABLE>
</xsl:template>

<xsl:template match="//product">
<TD><xsl:value-of select="@code"/></TD>
<TD><xsl:value-of select="description"/></TD>
<TD ALIGN="RIGHT">
    <xsl:value-of select="price"/>
</TD>
</xsl:template>
</xsl:stylesheet>
```

文档元素匹配 / 模板，因此 HTML 表格两侧使用的 HTML 代码被编码在此模板的主体中。在表格的位置，有一个回调到 XSLT 处理器的调用：

```xml
<xsl:apply-templates
    select="//product[manufacturer='Clemens-Altman']"/>
```

`select` 属性的值表示从文档根目录下一层的任何具有 manufacturer 属性且值为 Clemens-Altman 的 product 元素将被匹配。因此，当解析文档时，每个符合标准的 product 元素都被传递给 `//product` 模板。此模板代表表格中的一行。它添加 `<TR><TD>...</TD></TR>` 标签并用文档元素文本填充它们：

```xml
<TD><xsl:value-of select="@code"/></TD>
```

上一行提取当前节点中名为 code 的属性的值。

```xml
<TD><xsl:value-of select="description"/></TD>
```

此行提取 `<description>` 标签的文本值。JSP 页面很简单。除了生成外部 HTML 之外，它所做的一切就是创建一个 XSLT 处理器实例并启动它运行：

```jsp
<%@ page session="false" %>
<%@ page import="java.io.*" %>
```



# 490 JSP 完全参考

```jsp
<%@ page import="java.net.*" %>
<%@ page import="org.xml.sax.*" %>
<%@ page import="org.apache.xalan.xslt.*" %>
<%
    long stime = System.currentTimeMillis();
%>
<HTML>
<HEAD>
<TITLE>(XSLT) Clemens-Altman Musical Instruments</TITLE>
</HEAD>
<BODY>
<CENTER>
<H3>Clemens-Altman Musical Instruments</H3>
<H4>(Powered by XSLT)</H4>
<%
    // Create an instance of the XSLT processor
    XSLTProcessor p = XSLTProcessorFactory.getProcessor();

    // Create the XML input and XSL URL's
    StringBuffer requestURL = HttpUtils.getRequestURL(request);
    URL jspURL = new URL(requestURL.toString());
    URL inURL  = new URL(jspURL, "instruments.xml");
    URL xslURL = new URL(jspURL, "XSLTSample.xsl");

    // Process the stylesheet
    p.process(
        new XSLTInputSource(inURL.openStream()),
        new XSLTInputSource(xslURL.openStream()),
        new XSLTResultTarget(out)
        );

    out.flush();
%>
<P>
<%
    long etime = System.currentTimeMillis();
    double elapsed = (etime - stime)/1000.0;
%>
<EM>Elapsed time: <%= elapsed %> seconds</EM>
</CENTER>
</BODY>
</HTML>
```

结果如图 16-4 所示。

![](img/7a2f73369bb140583c7288b73456addb_516_0.png)

图 16-4. 由 XSLT 生成的产品目录 HTML

本例在服务器上运行了 XSL 转换。通过网络传输 XML 和样式表，并在客户端运行转换已经是可能的。Internet Explorer 5.0 引入了对 XML 和 XSL 样式表的直接支持。不幸的是，当 Microsoft 添加这些功能时，XSLT 规范还处于 beta 阶段。从那时起，XSLT 语言已经发生了变化，许多功能与 Microsoft 的版本不兼容。期待这些困难在未来得到解决是合乎逻辑的。

## 总结

XML 正在成为结构化数据存储和交换的通用语言。通过使用人类可读的文本文件和简单的语法规则，XML 不仅捕获数据，还捕获关于数据结构的元数据。数百个应用程序正在被编写或转换为以 XML 作为其输入和/或输出。XML 规范及其相关技术由万维网联盟（通常称为 W3C）管理。要读取 XML，你需要一个解析器。两种主要的解析器模型被普遍使用：

- **文档对象模型 (DOM)**：将 XML 文档建模为节点树。DOM API 提供了以任意顺序遍历 DOM 树的方法：向前、向后、遍历兄弟节点。
- **简单 Java API (SAX)**：事件驱动的解析器模型，在注册的处理程序中调用回调方法。

XML 可以使用 XSLT 处理器和 XSL 样式表进行转换。
毫无疑问，XML 应用程序在未来将大幅增加。JSP 可以成为这些应用程序的赋能技术。

此页有意留白。

![](img/7a2f73369bb140583c7288b73456addb_519_0.png)

## 第 17 章
### JSP 测试与调试
493

调试技术在编程教程中经常被轻描淡写，但在应用程序开发中却是不可或缺的。虽然编程可以是系统化的，并且代码很容易从其他程序中借鉴，但调试通常被视为一个随机试错修改的过程，这些修改可能修复也可能无法修复问题。

Web 应用程序环境带来了其独特的困难。由于应用程序被划分为服务器和客户端组件，请求处理涉及多个协作进程。因此，错误难以重现，尤其是当它们间歇性发生时。

在本章中，你将看到测试和调试可以与开发一样系统化。本章概述了可以应用的基本测试和调试技术，并开发了一些可能有所帮助的工具。

### 构建心智模型

系统化调试的关键是理解应用程序设计的运行方式。这意味着要知道涉及哪些组件、它们如何交互以及它们的预期行为是什么。这使得隔离故障组件并确定可能导致错误的原因成为可能。

### 翻译与编译

例如，你知道一个 JSP 页面以三种形式存在，如图 17-1 所示：

1.  **JSP 源代码**：这是开发者创建的内容——一个包含脚本片段、表达式、指令和 HTML 模板代码的 .jsp 文件。
2.  **生成的 Servlet 源代码**：当 JSP 页面首次被请求或在其 .jsp 文件发生任何更改后被请求时，JSP 容器将其转换为等效的 Java servlet。
3.  **编译后的 Servlet 类**：在 JSP 页面被转换为 servlet 源代码后，它被编译以生成一个 Java .class 文件。

在此过程中的任何点都可能发生错误。仔细检查错误消息并了解中间形式存在的位置可以帮助我们准确定位原因。

![](img/7a2f73369bb140583c7288b73456addb_520_0.png)

### 第 17 章：JSP 测试与调试
495

> 注意：仔细阅读错误消息至关重要，但如果错误消息不存在，你就无法阅读它们。Internet Explorer 5.x 在发生 500 级（内部 servlet）错误时，默认会替换为自己的错误页面。据推测，这是为了保护最终用户免受可怕的堆栈跟踪信息的影响，但这给开发者带来了困难。你可以通过选择“工具 | Internet 选项”菜单项，然后选择“高级”选项卡来关闭此功能。在树状结构的“浏览”部分下有一个名为“显示友好的 HTTP 错误消息”的复选框。如果你取消选择此选项，你可以看到完整的堆栈跟踪和 servlet 异常发送的任何其他数据。

例如，假设你有一个名为 `timer` 的自定义标签，用于跟踪其主体执行所需的时间。标签处理程序是一个名为 `TimerTag` 的类，它在 `doStartTag()` 和 `doEndTag()` 方法中获取当前系统时间的快照，并创建一个包含结果的脚本变量。

```java
import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import java.io.*;
import java.net.*;
import java.util.*;

/**
 * A tag handler for a custom tag that keeps track
 * of how long its body takes to execute
 */
public class TimerTag extends TagSupport
{
    private long startTime;
    private long endTime;

    /**
     * Starts the timer
     */
    public int doStartTag() throws JspException
    {
        startTime = System.currentTimeMillis();
        return EVAL_BODY_INCLUDE;
    }

    /**
     * Stops the timer and calculates the elapsed time
     * in seconds. This is stored as a page context
     * attribute using the ID variable name
     */
    public int doEndTag() throws JspException
    {
        endTime = System.currentTimeMillis();
        double elapsed = (endTime - startTime)/1000.0;
        pageContext.setAttribute(getId(), new Double(elapsed));
        return EVAL_PAGE;
    }
}
```

JSP 实战

一个典型的用途可能是查看创建 JDBC 连接需要多长时间，如下列 JSP 代码所示：

```jsp
<%@ page session="false" %>
<%@ page import="java.sql.*" %>
<%@ taglib prefix="debug" uri="/WEB-INF/tlds/debug.tld" %>
<debug:timer id="t1">
<%
    Connection con = null;
    try {
        Class.forName("sun.jdbc.odbc.JdbcOdbcDriver");
        con = DriverManager.getConnection("jdbc:odbc:usda");
    }
    finally {
        if (con != null)
            con.close();
    }
%>
</debug:timer>
Connecting to the database took <%= t1 %> seconds.
```

当此 JSP 页面在 JRun 3.0 下运行时，它工作正常。但在 Tomcat 3.2 下，它产生以下错误消息：

```
Error: 500
Location:/jspcr/Chap17/examples/Timer.jsp
Internal Servlet Error:
org.apache.jasper.JasperException:
Unable to compile class for JSP
D:\tomcat\work\localhost_8080%2Fjspcr\_0002fChap_00031_00037
_0002fexamples_0002fTimer_0002ejspTimer_jsp_0.java:70:
Class Chap_00031_00037.examples.TimerTag not found.
    TimerTag _jspx_th_debug_timer_0 = new TimerTag();
            ^
```



## 498 JSP 权威指南

仔细查看错误信息，你可以发现关于错误性质的几个线索。首先，它报告了 JSP 页面的位置。这告诉你 Tomcat 能够找到 JSP 源代码。接下来，消息文本显示 *Jasper*（Tomcat 的 JSP 翻译器）无法编译 JSP servlet 类，并给出了生成的 .java 源文件的名称。这意味着从 .jsp 到 .java 的翻译已完成，并且 Java 编译器已被调用，但编译失败。所以你知道这不是一个运行时错误。这不是由 JDBC-ODBC 驱动程序的问题引起的，因此它一定是生成的 servlet 源代码的编译错误。

在确定了故障组件后，你就能理解错误信息的其余部分了。生成的 servlet 在第 70 行创建了一个 `TimerTag()` 实例，并将其存储在 `_jspx_th_debug_timer_0` 变量中。正是这一行导致了错误消息 "Class Chap_00031_00037.examples.TimerTag not found."。因此，是 Java 编译器（而不是 JSP 翻译器或 servlet 引擎）无法找到某个类。如果你能找出原因，问题就解决了。

编译器找不到一个类可能有以下几个原因。该类可能未被编译，或者其 .class 文件不在类路径中。但仔细检查错误信息，会指向一个不同的原因。注意编译器正在寻找的类的全名：`Chap_00031_00037.examples.TimerTag`。这个包名从哪里来的？回顾标签处理器的源代码，你看不到任何 package 语句，而在 TLD 中，完全限定的类名仅仅是 `TimerTag`。这就解释了为什么找不到该类——编译器正在用错误的名字寻找它。

但为什么编译器会寻找带有那个包名的类？因为这是一个编译问题，你需要查看 .java 文件来确定问题的根源。这个文件的位置取决于 servlet 引擎，但从错误信息中你可以看出它位于 Tomcat 根目录的 work 子目录下。沿着 Web 应用程序子目录向下查找，你会找到 servlet 源文件。前几行显示了问题所在：

```
package Chap_00031_00037.examples;

import javax.servlet.*;
import javax.servlet.http.*;
import javax.servlet.jsp.*;
...
import org.apache.jasper.JasperException;
import java.sql.*;

public class ... extends HttpJspBase {
    ...
}
```

生成的 servlet 有一个 `package` 语句和多个 `import` 语句。根据你的 Java 基础知识，你知道如果 `import` 语句提供了完整的类名，就可以在不使用完全限定包名的情况下引用类。如果没有导入的包包含所引用的类名，编译器会假定它与正在编译的类位于同一个包中。因此，生成的 servlet 第 70 行引用的 `TimerTag` 类（还记得错误信息吗？）会在每个导入的包中查找，但都找不到，然后就被视为 servlet 自身包中的类：`Chap_00031_00037.examples`。谜题解开了。

但这留下了两个问题：

- 为什么这在 JRun 中可以工作？
- 你如何修复这个问题？

如果你查看 JRun 版本的生成 servlet，第一个问题就很容易回答了：

```
// Generated by JRun, do not edit

import javax.servlet.*;
import javax.servlet.http.*;
import javax.servlet.jsp.*;
import javax.servlet.jsp.tagext.*;
import allaire.jrun.jsp.JRunJSPStaticHelpers;
import java.sql.*;

public class jrun__Chap17__examples__Timer2ejsp1a
    extends allaire.jrun.jsp.HttpJSPServlet
    implements allaire.jrun.jsp.JRunJspPage
{
    ...
}
```

JRun 的 JSP 翻译器不会生成 `package` 语句，因此生成的 servlet 位于默认的无名包中。这与标签处理器所在的包相同，因此当 servlet 使用简单的类名时没有冲突：

```
TimerTag timer__4_1 = (TimerTag)
    JRunJSPStaticHelpers.createTagHandler
        (pageContext, "TimerTag");
```

现在，如何在 Tomcat 下修复这个错误？一种方法是为 `TimerTag` 提供一个 `import` 语句，这样 Java 编译器就知道不要尝试将其与任何其他包关联。你无法访问生成的 servlet，只能访问 JSP 源代码，这意味着你可以在你的 JSP 中放置这条语句：

```
<%@ page import="TimerTag" %>
```

虽然这能起作用，但这是一个不令人满意的解决方案，因为它必须在使用该标签的每个 JSP 页面中都这样做。除了需要记住这样做之外，对于维护程序员来说，甚至不清楚为什么要导入这个类——代码中没有对它的明显引用。

一个更好的解决方案是为标签处理器分配一个包名。如果完整的类名是 `jspcr.debug.TimerTag`，那么第 70 行就变成了：

```
jspcr.debug.TimerTag _jspx_th_debug_timer_0
    = new jspcr.debug.TimerTag();
```

这样就不会有歧义了。

> **注意**
> 一个区分编译时和运行时错误的有用方法是预编译 JSP 页面。JSP 1.1 规范要求合规的 JSP 容器在使用名为 "jsp_precompile" 的请求参数调用页面时执行此操作。JSP 容器将 JSP 页面翻译成 servlet 源代码并编译 servlet，但不会让它处理请求。这不必从浏览器进行；可以从一个简单的 Java 批处理应用程序来完成，该应用程序只需为请求（包括 "jsp_precompile" 参数）创建一个 URL 并调用其 openStream() 方法。

## 隔离测试

鉴于隔离故障组件是调试的关键，使这一过程易于操作非常重要。通过梳理思维流程图，并识别出*应该*发生什么和*实际*发生了什么是可行的。当问题区域被隔离后，应该可以单独测试故障组件，验证其操作的每个步骤。

要做到这一点，你需要从一个已知状态开始。如果你更改了多个代码段、重新编译了一些 bean 并修改了部署描述符，你可能会找到解决方案，但由于部分初始化和残留的类，你可能看不到不同的结果。为避免这种情况，你可以执行以下操作：

- **删除已翻译的 JSP servlet 和类的旧副本。** JSP 文件只有在其比对应的 servlet 和类文件更新时才会被翻译，但它所依赖的模块可能在不触发其重新翻译的情况下发生变化。例如，对使用 `<%@ include %>` 指令包含的文件的更改，不能保证会导致包含该指令的 JSP 页面被重新翻译。一些 JSP 容器会这样做，但规范并没有要求。
- **删除序列化的会话。** 一些 JSP 容器在关闭时会将会话保存到持久存储中，然后在 JSP 容器再次启动时恢复它们。例如，JRun 将序列化的会话写入 `/WEB-INF/sessions` 目录。如果你更改了类并重新编译了它们，当 servlet 引擎重新启动时，你可能会反序列化该类的旧版本。
- **重新启动 Web 服务器和 servlet 引擎。** 虽然在所有情况下这可能并非绝对必要，但此步骤可以让你确信所有初始化都已正确完成。例如，对 `web.xml` 和标签库描述符的更改可能仅在启动时才能被检测到。

一旦你确定了应用程序状态，你就可以为其提供已知的输入并跟踪其处理过程。Servlet 日志为来自 servlet 引擎以及各个 servlet 和 JSP 页面的消息提供了集中收集点。你可以使用 `log()` 方法[^1]将消息写入日志，就像使用 `System.out.println()` 一样。特别是在 JSP 页面中，很容易添加几条日志消息，进行测试，根据测试结果再添加几条，依此类推。将消息写入 servlet 日志比尝试写入 servlet 输出流提供了更好的执行跟踪，因为后者可能已损坏，并在你分析之前就消失了。

[^1]：这是 `ServletContext` 类中的一个方法，但作为 `GenericServlet`（大多数 JSP 页面都派生自它）的便捷方法也可用。`log()` 优于 `System.out.println()`，因为它与供应商无关，并且由所有 servlet 容器提供。

## 调试工具

大多数商业*集成开发环境*（IDE）都提供某种调试器，使你能够单步执行 Java 类的执行，检查变量的值，并可能更改变量的值。JDK 包含一个名为 `jdb` 的命令行调试器，它或多或少执行相同的功能。虽然这些工具很有用，但用于调试 JSP 代码时有几个缺点。

首先，JSP 页面与其字节码对应物并不紧密对应。它们可能由脚本段、指令、表达式、HTML 和自定义标签组成。如果你真的对逐行执行跟踪感兴趣，你需要使用生成的 servlet 源代码进行调试，而不是 `.jsp` 文件。

此外，JSP 类是在 servlet 引擎控制的单独虚拟机中加载和运行的，可能还链接到一个 Web 服务器。要调试单个类，需要以调试模式启动整个 servlet 引擎。你需要验证所有相同的类路径条目都是活动的，使用相同的端口等等。即使你能弄清楚如何做到这一点，这也往往会使调试环境变得非常复杂。

与实际的运行时环境不同。同样，两个环境之间显著的时间差异可能导致超时和竞态条件，这些与正在调试的问题无关。

实际上，逐行调试器能做的事情，用`log()`方法（或者`System.out.println()`）也几乎都能做到。在断点处检查的任何变量，都可以轻松地写入servlet日志。你可以在任何点停止执行，只需抛出一个异常就能生成堆栈跟踪。考虑到JSP的自动编译和浏览器的刷新按钮，你可能比启动IDE并让servlet引擎进入调试模式更快地完成几次带有新消息点的迭代。

在本节中，你将学习开发三个侵入性更小、更适合HTTP请求处理环境的工具。将它们与`log()`方法结合用于执行跟踪，有助于隔离错误和验证修复。

## 捕获表单参数

当HTML表单用于向JSP或servlet发送请求参数时，一个明显的测试要求是能够知道它发送了哪些参数以及它们的值是什么。这并不总是显而易见的。如果一个`<SELECT>`元素允许多选，请求参数的值是什么？如果一个TEXT输入元素未填写，它会作为空字符串还是null传递？那些未指定VALUE属性的复选框呢？

一个简单的方法是使用一个调试JSP页面，该页面捕获请求参数并以表格形式显示为名称/值对。下面的JSP页面（Echo.jsp）展示了如何实现：

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<HTML>
<HEAD><TITLE>Form Parameters</TITLE></HEAD>
<BODY>
<H3>Form Parameters</H3>
<TABLE BORDER="1" CELLPADDING="3" CELLSPACING="0">
<TR><TH WIDTH=200>Name</TH><TH WIDTH=200>Value</TH></TR>
<%
    Enumeration enames = request.getParameterNames();
    while (enames.hasMoreElements()) {
        String name = (String) enames.nextElement();
        String[] values = request.getParameterValues(name);
        if (values != null) {
            for (int i = 0; i < values.length; i++) {
                String value = values[i];
%><TR><TD><%= name %></TD><TD><%= value %></TD></TR><%
            }
        }
    }
%>
</TABLE>
</BODY>
</HTML>
```

### 502 JSP: 完全参考

```
    }
  }
}
%>
</TABLE>
</BODY>
</HTML>
```

Echo.jsp从请求对象获取所有参数名称的列表，然后遍历该列表并打印每个参数的名称和值。唯一需要注意的是一个参数可能有多个值。例如，一组复选框可能有相同的name但不同的value属性。然而，servlet API通过在request对象中提供`getParameterValues()`方法来处理这个问题，该方法返回一个值数组。

图17-2展示了一个包含多种输入元素的HTML表单。生成该表单的JSP页面如下所列：

```
<%@ page session="false" %>
<HTML>
<HEAD>
<TITLE>Job Application</TITLE>
</HEAD>
<BODY>
<H3>Please Indicate Your Qualifications</H3>

<FORM ACTION="/dailyplanet/apphandler.jsp" METHOD="POST">

<INPUT
    TYPE="hidden"
    NAME="locale"
    VALUE="<%= request.getLocale() %>"
    >
<TABLE BORDER="0" CELLPADDING="3" CELLSPACING="0">
    <TR>
        <TD>
            <INPUT TYPE="checkbox" NAME="speed">
            Faster than a speeding bullet
            <BR>
            <INPUT TYPE="checkbox" NAME="power">
            More powerful than a locomotive
            <BR>
<INPUT TYPE="checkbox" NAME="flight">
Able to leap tall buildings with a single bound
<BR>
</TD>
</TR>
<TR><TD>Name: <INPUT TYPE="text" NAME="name">
<INPUT TYPE="submit" VALUE="Submit"></TD></TR>
</TABLE>

</FORM>
</BODY>
</HTML>
```

此表单使求职者能够使用一组复选框来描述他们的资格。此外，用户的区域设置被捕获为一个隐藏字段，以便可以用用户的首选语言发送响应。通常，此表单由/dailyplanet/apphandler.jsp处理。为了正确处理此输入，apphandler.jsp需要知道请求参数将以何种格式发送。如果不查看，你会知道复选框值的默认格式吗，因为它们没有指定VALUE属性？

这很容易确定。通过将ACTION="Echo.jsp"替换ACTION="dailyplanet.jsp"，你可以捕获表单的输出，并使用几种不同的浏览器和值的组合对其进行测试。如果你对图17-2中的表单值执行此操作，你会得到图17-3所示的表格。

![](img/7a2f73369bb140583c7288b73456addb_529_0.png)

图17-2. 在线工作申请

![](img/7a2f73369bb140583c7288b73456addb_530_0.png)

图17-3. 来自在线工作申请的表单参数

Echo.jsp可以增强以显示更多关于请求的信息，例如请求头、cookies和请求属性。Echo.jsp的主要优点是它不需要对处理表单的服务端组件进行任何更改。只需在提交表单的HTML文档或JSP页面中的<FORM>元素进行快速的一行修改即可。

## 调试Web客户端

Echo.jsp服务器使你能够看到Web客户端产生了什么。事务的另一方是处理servlet或JSP页面如何响应。当你能够隔离地查看其输入和输出时，调试服务端组件会更容易，而不是在Web浏览器操作之后查看。

这比你想象的要容易。Web服务器不需要Web浏览器，只需要能够以普通ASCII形式产生HTTP请求的东西。在端口80上调用Telnet就能很好地完成此任务：

```
% telnet www.lyricnote.com 80
Trying...
Connected to www.lyricnote.com.
Escape character is '^]'.
GET / HTTP/1.0

HTTP/1.1 200 OK
...
```

不幸的是，Windows系统上的默认Telnet客户端是基于GUI的，用于此目的时使用起来很笨拙。GUI窗口不会滚动，并且在请求处理后会自动清除其文本。而且Windows客户端不能正确处理Unix换行符约定。

然而，用一个独立的控制台模式Java应用程序复制HTTP请求功能非常容易。下面列出的WebClient.java是一个简单的Web客户端，设计用于从命令行调用：

```
import java.io.*;
import java.net.*;
import java.util.*;

public class WebClient
{
    /**
     * Mainline.
     * Reads command line parameters and creates a new
     * <CODE>WebClient</CODE> object.
     */
    public static void main(String[] args)
        throws Exception
    {
        String host = "localhost";
        int port = 80;

        for (int i = 0; i < args.length; i++) {
            String arg = args[i];
            if (arg.startsWith("-")) {
                if (arg.equals("-host")) {
                    if (++i >= args.length)
                        throw new RuntimeException
                            ("no argument for " + arg);
                    host = args[i];
                }
                else if (arg.equals("-port")) {
                    if (++i >= args.length)
                        throw new RuntimeException
                            ("no argument for " + arg);
                    try {
                        port = Integer.parseInt(args[i]);
                    }
                    catch (NumberFormatException e) {
                        throw new RuntimeException
                            ("Invalid port number [" + args[i] + "]");
                    }
                }
                else {
                    System.out.println("Invalid argument: " + arg);
                    showUsage();
                    System.exit(0);
                }
            }
            else {
                showUsage();
                System.exit(0);
            }
        }

        new WebClient(host, port);
    }
```

```
/**
 * Displays the calling syntax
 */
public static void showUsage()
{
    String[] text = {
        "usage: java WebClient"
        + " [-host <hostName>]"
        + " [-port <portNumber>]",
    };
    for (int i = 0; i < text.length; i++)
        System.out.println(text[i]);
}
```

```
/**
 * Creates and runs the web client
 * @param host the HTTP server
 * @param port the server port number
 * @exception IOException if a socket error occurs
 */
public WebClient(String host, int port)
    throws IOException
{
```



int contentLength = 0;

// 向 Web 主机打开一个 socket 连接

Socket socket = new Socket(host, port);

// 从用户读取输入并将其回显到 Web 主机

BufferedReader in =
    new BufferedReader(
    new InputStreamReader(System.in));

PrintWriter out =
    new PrintWriter(socket.getOutputStream());

// 第一行 - 请求

String line = in.readLine();
out.println(line);

// 头部行

for (;;) {

    // 读取并回显该行

    line = in.readLine();
    if (line == null)
        throw new IOException("Unexpected EOF");
    line = line.trim();
    out.println(line);

    // 头部结束

    if (line.equals(""))
        break;

    // 否则，这是一个头部

    int p = line.indexOf(": ");
    if (p == -1)
        throw new IOException
            (line + " is not a valid header line");

    String name = line.substring(0, p).trim();
    String value = line.substring(p + 1).trim();

    if (name.equalsIgnoreCase("Content-Length")) {
        try {
            contentLength = Integer.parseInt(value);
        }
        catch (NumberFormatException e) {
            throw new IOException
                ("Invalid content length " + value);
        }
    }
}

// 读取 <contentLength> 字节的内容

if (contentLength > 0) {
    StringBuffer sb = new StringBuffer();
    for (;;) {
        line = in.readLine();
        if (line == null)
            break;
        sb.append(line);
        int len = sb.length();
        if (len < contentLength)
            continue;
        if (len > contentLength)
            sb.setLength(contentLength);
        break;
    }

    // 将数据写入输出流

    out.print(sb.toString());
}

out.flush();

// 服务器现在正在处理该请求。
// 读取其输出并输出到标准输出

in =
    new BufferedReader(
        new InputStreamReader(
            socket.getInputStream()));

out = new PrintWriter(System.out);

for (;;) {
    line = in.readLine();
    if (line == null)
        break;
    out.println(line);
}

// 关闭文件

in.close();
out.close();
socket.close();
}
}

WebClient 的调用语法为：

`java WebClient [-host <hostName>] [-port <portNumber>]`

启动时，它会向指定的主机（默认为 localhost）打开一个 socket 连接，然后等待从键盘输入 HTTP 请求和可选的头部信息。用户输入的每一行都通过 socket 发送出去。当输入一个空行时，输入结束。这向 HTTP 服务器发出信号，表示将不再发送更多头部，请求已完成，除了可能随 POST 请求发送的数据。

在请求被发送并处理后，服务器会发回响应，该响应会回显到控制台。一次典型的交互可能如下所示：

```
D:\jspcr\Chap17\examples>java WebClient
POST /jspcr/Chap17/examples/Echo.jsp HTTP/1.0
Content-type: application/x-www-form-urlencoded
Content-length: 53

speed=on&power=on&flight=on&name=C.+Kent&locale=en_US
HTTP/1.1 200 OK
Date: Tue, 05 Dec 2000 03:59:35 GMT
Server: Apache/1.3.12 (Win32)
Connection: Keep-alive, close
Content-Length: 434
Content-Type: text/html; charset=ISO-8859-1

<HTML>
<HEAD>
<TITLE>Form Parameters</TITLE>
</HEAD>
<BODY>
<H3>Form Parameters</H3>
<TABLE BORDER="1" CELLPADDING="3" CELLSPACING="0">
<TR><TH WIDTH=200>Name</TH><TH WIDTH=200>Value</TH></TR>

<TR><TD>flight</TD><TD>on</TD></TR>

<TR><TD>speed</TD><TD>on</TD></TR>

<TR><TD>power</TD><TD>on</TD></TR>

<TR><TD>name</TD><TD>C. Kent</TD></TR>

<TR><TD>locale</TD><TD>en_US</TD></TR>

</TABLE>
</BODY>
</HTML>
```

## 跟踪 HTTP 请求

要有效地对 Web 应用程序进行故障排除，你必须能够监控它如何发出请求和接收响应。你已经看到 Java 类既可以充当 Web 客户端，也可以充当 Web 服务器。在本节中，你将开发一个执行这两种功能的监控工具，它作为客户端和服务器之间的中介，如图 17-4 所示。当这个跟踪器工具插入到 Web 应用程序中时，它的服务器组件监听 HTTP 请求，记录其头部，然后将它们转发到真正的 Web 服务器。它的客户端组件随后接收 Web 服务器的响应，记录头部，并将响应发回客户端。客户端和服务器都不知道跟踪器在循环中的存在。

## 第 17 章：JSP 测试与调试

该工具由两个主要组件组成：

- 一个监听 HTTP 请求的 Web 服务器代理。
- 一个请求处理器，它将客户端请求复制到服务器，并将响应复制回客户端，并在两个方向记录头部信息。

以下列出了第一个组件（Tracer.java）。

```java
package http;

import java.io.*;
import java.net.*;
import java.util.*;

/**
 * 作为一个代理 Web 服务器运行，捕获请求
 * 和响应，并将头部信息回显到
 * 一个日志流。
 */
public class Tracer extends Thread implements Logger
{
    public static final int DEFAULT_PORT = 8601;

    private String host;
    private int port;
    private int tracerPort;
    private PrintWriter logWriter;
```

JSP 实战

# 512 JSP：完全参考手册

```java
// ========================================
//   类方法
// ========================================

/**
 * 主方法
 */
public static void main(String[] args)
    throws IOException
{
    String opt_host = null;
    String opt_port = null;
    String opt_tracerPort = null;
    String opt_log = null;

    try {
        for (int i = 0; i < args.length; i++) {
            String arg = args[i];

            if (!arg.startsWith("-"))
                throw new IllegalArgumentException
                    ("Unknown argument ["
                    + arg + "]. Use -h for help");

            // -h 用于显示帮助

            String keyword = arg.substring(1);
            if (keyword.equals("h") ||
                keyword.equals("help"))
            {
                showUsage();
                return;
            }

            // -host <hostname>

            if (keyword.equals("host")) {
                if (++i >= args.length)
                    throw new IllegalArgumentException
                        (arg + " but no argument");
                opt_host = args[i];
            }
```

# 第 17 章：JSP 测试与调试 513

```java
            else

            // -port <hostname>

            if (keyword.equals("port")) {
                if (++i >= args.length)
                    throw new IllegalArgumentException
                        (arg + " but no argument");
                opt_port = args[i];
            }
            else

            // -tracerPort <hostname>

            if (keyword.equals("tracerPort")) {
                if (++i >= args.length)
                    throw new IllegalArgumentException
                        (arg + " but no argument");
                opt_tracerPort = args[i];
            }
            else

            // -log <filename>

            if (keyword.equals("log")) {
                if (++i >= args.length)
                    throw new IllegalArgumentException
                        (arg + " but no argument");
                opt_log = args[i];
            }
            else
                throw new IllegalArgumentException
                    ("Unrecognized option " + arg);
        }

        // 验证端口没有冲突

        int testTracerPort = (opt_tracerPort == null)
            ? DEFAULT_PORT
            : Integer.parseInt(opt_tracerPort);

        int testHostPort = (opt_port == null)
            ? RequestHandler.DEFAULT_PORT
            : Integer.parseInt(opt_port);

        if (testTracerPort == testHostPort)
            throw new IllegalArgumentException
                ("Cannot assign port and tracerPort both to "
                 + testTracerPort);
    }
    catch (IllegalArgumentException e) {
        System.err.println(e.getMessage());
        return;
    }

    // 创建跟踪器

    Tracer tracer = new Tracer();

    // 设置其属性（如果有的话）

    if (opt_host != null)
        tracer.setHost(opt_host);

    if (opt_port != null)
        tracer.setPort(Integer.parseInt(opt_port));

    if (opt_tracerPort != null)
        tracer.setTracerPort
            (Integer.parseInt(opt_tracerPort));

    if (opt_log != null)
        tracer.setLogWriter(new FileWriter(opt_log));

    tracer.start();
}

/**
 * 显示调用语法
 */
public static final void showUsage()
{
    String[] text = {
        "",
        "usage: java http.Tracer [options]",
```



## 第17章：JSP测试与调试

```
"可用选项有：",
"-host <主机名> " + "（默认为 " + RequestHandler.DEFAULT_HOST + "）",
"-port <主机端口> " + "（默认为 " + RequestHandler.DEFAULT_PORT + "）",
"-tracerPort <本地端口> " + "（默认为 " + DEFAULT_PORT + "）",
"-log <文件名> " + "（默认为 System.out）",
};
for (int i = 0; i < text.length; i++)
System.out.println(text[i]);
}
```

```
// ===============================================
// 实例方法
// ===============================================
```

```
public void run()
{
// 如果未另行指定，则设置默认值

if (tracerPort == 0)
tracerPort = DEFAULT_PORT;

if (logWriter == null)
logWriter = new PrintWriter(System.out);

// 启动代理服务器

try {
log("M: 在 tracerPort " + tracerPort + " 上打开 tracer 服务器");
ServerSocket server = new ServerSocket(tracerPort);

// 无限循环
for (;;) {

    // 等待连接

    log("M: 等待连接");
    Socket client = server.accept();
    log("M: 收到来自 " + client + " 的连接");

    // 将其分派给一个请求处理线程

    RequestHandler rh = new RequestHandler(client);
    rh.setLogger(this);
    if (host != null)
        rh.setHost(host);
    if (port != 0)
        rh.setPort(port);
    rh.start();
}
}
catch (IOException e) {
    e.printStackTrace();
}
}
```

```
// ========================================
//    Logger 的实现
// ========================================
```

```
/**
 * 将消息写入日志
 * @param message 消息内容
 */
public synchronized void log(String message)
{
    logWriter.println(message);
    logWriter.flush();
}
```

```
// ========================================
//    访问器
// ========================================
```

```
/**
 * 返回主机。
 */
public String getHost()
{
    return host;
}

/**
 * 设置主机。
 * @param host 主机名。
 */
public void setHost(String host)
{
    this.host = host;
}

/**
 * 返回端口。
 */
public int getPort()
{
    return port;
}

/**
 * 设置端口。
 * @param port 端口号。
 */
public void setPort(int port)
{
    this.port = port;
}

/**
 * 返回 tracerPort。
 */
public int getTracerPort()
{
    return tracerPort;
}

/**
 * 设置 tracerPort。
 * @param tracerPort tracer 的端口号。
 */
public void setTracerPort(int tracerPort)
{
    this.tracerPort = tracerPort;
}

/**
 * 返回 logWriter。
 */
public Writer getLogWriter()
{
    return logWriter;
}

/**
 * 设置 logWriter。
 * @param logWriter 日志写入器。
 */
public void setLogWriter(Writer logWriter)
    throws IOException
{
    this.logWriter = new PrintWriter(logWriter);
}
}
```

Tracer 主程序解析命令行，支持以下四个选项：

- `-host <主机名>` 目标 Web 服务器主机的名称。如果未指定，默认为 localhost。
- `-port <端口号>` 目标 Web 服务器上的端口号。默认为 80，即默认的 HTTP 端口号。
- `-tracerPort <端口号>` Tracer 自身运行的本地端口号。默认为 8601。此端口号必须包含在需要被跟踪的 URL 中。例如，如果一个 HTML 表单的 ACTION 属性为 `http://www.lyricnote.com/search/ProductSearch.jsp`，则应更改为 `http://www.lyricnote.com:8601/search/ProductSearch.jsp`。这是将 Tracer 连接到任何应用程序所需进行的唯一更改。
- `-log <文件名>` 用于写入 HTTP 头的文件名。如果未指定此选项，日志消息将输出到 System.out。

验证命令行选项后，主程序创建一个 `Tracer` 对象，设置其属性并启动它。

`run()` 方法创建一个 `java.net.ServerSocket` 并开始监听客户端连接。当接受一个连接时，`run()` 会创建一个请求处理线程来处理事务。你将很快了解这个组件。每一步都会写入一条日志消息。

`Tracer` 和 `RequestHandler` 都会写入日志消息。由于日志可能通过命令行选项重定向，因此每个组件都需要一个指向日志输出流的句柄。这可以通过定义一个 `Logger` 接口来实现，`Tracer` 会实现这个接口。`RequestHandler` 在其作为 `Logger` 的角色中被传递了一个对 `Tracer` 的引用。为了明确是哪个组件发送的消息，每条消息都以 `C:`（客户端）、`S:`（服务器）或 `M:`（Tracer 中间人）开头。

该工具的第二个组件 `RequestHandler` 充当目标 Web 服务器的 Web 客户端，将从真实 Web 客户端获取的请求行、请求头和任何请求数据流传递给它，并在过程中记录头部信息。然后 `RequestHandler` 转身将响应行、响应头和响应数据复制回客户端。

```
package http;

import java.io.*;
import java.net.*;
import java.util.*;

/**
 * 处理单个请求的代理 HTTP 服务器
 */
public class RequestHandler extends Thread
{
    public static final String DEFAULT_HOST = "localhost";
    public static final int DEFAULT_PORT = 80;

    private Socket client;
    private Logger logger;
    private String host;
    private int port;

    // =======================================
    //     构造函数
    // =======================================

    /**
     * 为指定的客户端
     * 创建一个新的 RequestHandler
     */
    public RequestHandler(Socket client)
    {
        this.client = client;
    }

    // =============================================
    //      实例方法
    // =============================================

    /**
     * 将请求从客户端复制到服务器，
     * 并将响应复制回客户端。
     */
    public void run()
    {
        try {

            // 打开一个到 Web 服务器的套接字

            if (host == null)
                host = DEFAULT_HOST;
            if (port <= 0)
                port = DEFAULT_PORT;

            Socket server = new Socket(host, port);

            // 打开到客户端的 I/O 流

            InputStream cin =
                new BufferedInputStream(client.getInputStream());
            OutputStream cout =
                new BufferedOutputStream(client.getOutputStream());

            // 打开到服务器的 I/O 流

            InputStream sin =
                new BufferedInputStream(server.getInputStream());
            OutputStream sout =
                new BufferedOutputStream(server.getOutputStream());

            // 将请求行和请求头从客户端复制到服务器，
            // 如果指定了日志记录器，则同时回显。在第一个
            // 空行（头部结束）后停止。

            int contentLength = 0;
            StringBuffer sb = new StringBuffer();
            for (;;) {

                // 从客户端读取一个字节
                // 并将其复制到服务器

                int c = cin.read();
                sout.write(c);

                // 忽略行尾的 CR

                if (c == '\r')
                    continue;

                // 如果是 LF，则处理该行

                if (c == '\n') {
                    String line = sb.toString();
                    sb = new StringBuffer();

                    // 记录该行

                    logger.log("C: " + line);

                    // 如果是空行，
                    // 则没有更多头部信息

                    if (line.length() == 0)
                        break;

                    // 如果是 content-length 头，
                    // 保存内容长度
                    int p = line.indexOf(":");
                    if (p != -1) {
                        String key = line.substring(0, p).trim();
                        String value = line.substring(p+1).trim();
                        if (key.equalsIgnoreCase("content-length"))
                            contentLength = Integer.parseInt(value);
                    }
                }

                // 否则，将字符追加到字符串缓冲区

                else
                    sb.append((char) c);
            }
            sout.flush();

            // 如果指定了内容长度，读取输入流
            // 并复制到服务器

            if (contentLength > 0) {
                for (int i = 0; i < contentLength; i++) {
                    int c = cin.read();
                    sout.write(c);
                }
                sout.flush();
            }

            // 将响应回显给客户端

            sb = new StringBuffer();
            for (;;) {

                // 从服务器读取一个字节
                // 并将其复制到客户端

                int c = sin.read();
                cout.write(c);

                // 忽略行尾的 CR

                if (c == '\r')
                    continue;
```

// 如果遇到换行符，则处理该行

if (c == '\n') {
    String line = sb.toString();
    sb = new StringBuffer();

    // 记录该行

    logger.log("S: " + line);

    // 如果这是空行，则表示没有更多头部信息

    if (line.length() == 0)
        break;
}

// 否则，将字符追加到字符串缓冲区

else
    sb.append((char) c);
}
cout.flush();

// 将剩余字节复制到客户端

int bytesCopied = 0;
for (;;) {
    int c = sin.read();
    if (c == -1)
        break;
    cout.write(c);
    bytesCopied++;
}
if (bytesCopied > 0)
    cout.flush();

// 关闭流和套接字

cin.close();
cout.close();
client.close();

sin.close();
sout.close();
server.close();
}
catch (IOException e) {
    e.printStackTrace();
}
}

// ==================================
//    访问器方法
// ==================================

/**
 * 返回客户端套接字。
 */
public Socket getClient()
{
    return client;
}

/**
 * 返回日志记录器。
 */
public Logger getLogger()
{
    return logger;
}

/**
 * 设置日志记录器。
 * @param logger 日志记录器。
 */
public void setLogger(Logger logger)
{
    this.logger = logger;
}

/**
 * 返回主机。
 */
public String getHost()
{
    return host;
}

/**
 * 设置主机。
 * @param host 主机。
 */
public void setHost(String host)
{
    this.host = host;
}

/**
 * 返回端口。
 */
public int getPort()
{
    return port;
}

/**
 * 设置端口。
 * @param port 端口。
 */
public void setPort(int port)
{
    this.port = port;
}
}

`RequestHandler` 的核心是其 `run()` 方法，该方法打开一个到 Web 服务器的客户端套接字，然后打开该套接字的输入和输出流。同样，它为 Web 客户端打开输入和输出流。`run()` 方法随后读取请求行和请求头，寻找表示头部结束的空行。每读取一个头部，它都会被记录并传递给 Web 服务器。如果找到 Content-Length 头部，其值会被记下。在头部结束的空行之后，如果内容长度非零，请求处理器会从客户端输入流中读取相应数量的字节并将其复制到服务器。然后对服务器的响应重复相同的过程（方向相反），只是忽略 Content-Length 头部，并读取和复制服务器的输出直到文件结束。

Tracer 工具可以派上用场的一个例子是 HTTP 认证。许多实现这一点的工作都发生在浏览器和 Web 服务器的底层。检查 HTTP 头部可以使其变得清晰。

HTTP 基本认证的工作原理如下：

- ■ Web 用户请求一个受 HTTP 基本认证保护的文档。
- ■ Web 浏览器格式化一个 HTTP 请求并将其发送到 Web 服务器。
- ■ 服务器拒绝该请求，将状态码设置为 401（需要授权），并发送一个 WWW-Authenticate 头部，指定认证类型和域。
- ■ 浏览器收到 401 响应码并搜索其缓存，查看用户是否在此会话期间已登录到此域。如果用户未登录，浏览器会提示输入用户 ID 和密码。
- ■ 从提示或浏览器会话缓存中获得的凭据被 Base64 编码²，原始请求被重新发送，这次带有 Authorization 头部。
- ■ 服务器看到 Authorization 头部，验证用户是否有权检索文档，然后返回文档或另一个 401 响应行。

以下是 Tracer 对此过程的报告³：

```
M: Opening tracer server on tracerPort 8601
M: Waiting for connections
M: Connection received from Socket
    [addr=ppp-1-247.dialup.lyricnote.com/209.165.213.47,
    port=1180,localport=8601]
M: Waiting for connections
```

> 2 Base64 编码将字节流转换为可读的 ASCII 字符，这样字节中的控制字符就不会干扰服务器操作。RFC 2068 描述了该算法。但请注意，这不是加密，只是一种可以轻松逆转的字符转换。因此，HTTP 基本认证并不特别安全，只应用于安全风险可接受的内部应用程序。
>
> 3 日志已为可读性稍作重新格式化。

Tracer 服务器通过在 8601 端口上打开一个服务器套接字来启动。它在服务器套接字的 accept() 方法上阻塞，等待客户端连接。一旦收到连接，就会启动一个请求处理器，Tracer 服务器恢复监听其他客户端请求。

```
C: GET /logviewer/index.jsp HTTP/1.1
C: Accept: application/msword, application/vnd.ms-excel, ...
C: Accept-Language: en-us
C: Accept-Encoding: gzip, deflate
C: User-Agent: Mozilla/4.0 (compatible; Windows NT 4.0)
C: Host: u25nv:8601
C: Connection: Keep-Alive
C:
```

请求处理器读取请求行和六个头部，并将它们回显给 Web 服务器。

```
S: HTTP/1.1 401 Authorization Required
S: Date: Tue, 05 Dec 2000 22:28:22 GMT
S: Server: Apache/1.3.12 (Win32)
S: WWW-Authenticate: Basic realm="Servlet Administrators"
S: Keep-Alive: timeout=15, max=100
S: Connection: Keep-Alive
S: Transfer-Encoding: chunked
S: Content-Type: text/html; charset=iso-8859-1
S:
```

Web 服务器拒绝了该请求，返回了 401 状态码（需要授权）和一个 WWW-Authenticate 头部，指定认证类型为 Basic，域为 "Servlet Administrators"。Web 浏览器提示用户输入该域的用户 ID（"wolfgang"）和密码（"papageno"），并重新发出请求：

```
M: Connection received from Socket
    [addr=ppp-1-247.dialup.lyricnote.com/209.165.213.47,
    port=1184,localport=8601]
M: Waiting for connections

C: GET /logviewer/index.jsp HTTP/1.1
C: Accept: application/msword, application/vnd.ms-excel, ...
C: Accept-Language: en-us
C: Accept-Encoding: gzip, deflate
C: User-Agent: Mozilla/4.0 (compatible; Windows NT 4.0)
C: Host: u25nv:8601
C: Connection: Keep-Alive
C: Authorization: Basic d29sZmdhbmc6cGFwYW50=
C:

S: HTTP/1.1 200 OK
S: Date: Tue, 05 Dec 2000 22:28:37 GMT
S: Server: Apache/1.3.12 (Win32)
S: Connection: Keep-alive, Keep-Alive
S: Content-Length: 142
S: Keep-Alive: timeout=15, max=100
S: Content-Type: text/html; charset=ISO-8859-1
S:
```

这一次，请求包含一个带有 Base64 编码凭据的 Authorization 头部。而且，这一次，服务器接受了请求并返回了文档。

## 总结

测试和调试是应用程序开发不可或缺的部分。虽然编程是系统性的，并且适用于设计模式，但调试通常是随意的，并通过反复试错来进行。本章强调了系统调试方法的两个关键方面：

- 为组件及其交互建立心智模型
- 隔离故障组件

介绍了三种可以辅助此方法的工具：

- `Echo.jsp`：一个捕获 HTML 表单产生的参数的 JSP 页面
- `WebClient`：一个模拟 Web 浏览器的独立应用程序
- `Tracer`：一个拦截和记录 HTTP 请求的独立应用程序

通过充分的事前考虑和为可测试性而设计的规划，调试可以像应用程序开发一样系统化。

# 第 18 章

## 部署 Web 应用程序

历史上，安装和配置 Web 应用程序一直是完全特定于供应商的任务。例如，Apache JServ 使用 .properties 文件和包含 Apache 指令扩展的文件来配置其 servlet 区域及其属性。JRun 的早期版本附带了一堆 .properties 文件，用于指示存在多少服务器、它们使用哪些端口、它们的类路径、它们识别哪些 servlet 别名、哪些 servlet 应该预加载等等。JSWDK 参考实现使用自定义 XML 格式来实现此目的。

由于 servlet 引擎毕竟是具有各自特定功能的不同实现，因此一定程度的多样性是不可避免的。但配置任务的这一部分是有限的。描述与 servlet 本身交互的那部分则是相当规范的，并且可以通过标准化带来巨大好处。这正是 Servlet 2.2 API 中引入 Web 应用程序时所发生的情况。

本章描述了 Web 应用程序的结构，以及如何将其从开发环境迁移到生产环境。

## Web 应用程序环境

Servlet 2.2 和 JSP 1.1 API 规范将一组映射到 Web 服务器命名空间中公共区域的协作资源称为 Web 应用程序。这个集合可能包括 servlet、JSP 页面、HTML 文件、图像、支持类和配置数据。

例如，LyricNote 网站可能包含几个 Web 应用程序：

- **products**：这将包括产品目录数据库、图像、搜索引擎、用于客户订单的购物车应用程序，以及描述产品类别的网页。
- **support**：此应用程序将为客户提供报告问题和提问的 JSP 页面、缺陷跟踪 servlet、用于生成电子邮件的 servlet，以及与知识库交互的类。
- **internal**：MIS 应用程序（如会议室预订、职位发布和公司简报）将放在这里，混合使用 servlet、JSP 页面和普通 HTML。

## 目录结构

Web 应用程序有一个所有兼容的 servlet 引擎都能理解的规范目录结构。该结构如图 18-1 所示。顶层，或应用程序根目录，包含 HTML 文档、JSP 页面、图像以及构成应用程序内容的任何其他资源。任意数量的子目录，这些子目录也

包含应用程序内容，可以位于根目录下，类似于 Web 服务器文档树中的文件夹。

根目录还包含一个名为 `WEB-INF` 的特殊目录。此目录及其子目录对应用程序用户不可见。相反，它们包含构成应用程序操作部分的 servlet、类、`.jar` 文件和配置数据。`WEB-INF` 中有三个值得注意的条目：

-   `classes` 此目录包含 servlet 和其他类。这些类由 servlet 类加载器自动查找，就好像它们位于应用程序的类路径中一样。`classes` 可以有与包结构相对应的子目录，与类路径中的任何其他目录相同。
-   `lib` 与 `classes` 类似，但包含 `.jar` 文件。此目录中任何 `.jar` 文件中的类都会自动提供给类加载器，而无需在某个类路径中显式列出。
-   `web.xml` 这是一个 XML 文档，称为*部署描述符*。它具有严格定义的与供应商无关的结构，用于配置构成 Web 应用程序的 servlet 和其他资源。你将在本章后面更详细地研究 `web.xml`。

`WEB-INF` 中可能还有其他文件和子目录，尽管 Servlet API 规范并未定义任何特定的。一个常用的子目录是 `tlds`，它包含用于 JSP 自定义标签的标签库描述符。由于此子目录中的条目对应用程序类可见，但对 Web 用户不可见，因此 `WEB-INF` 通常用于特定供应商的目的。例如，JRun 创建一个名为 **jsp** 的子目录，其中包含从 JSP 页面生成的 servlet 的 Java 源代码和编译后的类。JRun 还创建一个名为 **sessions** 的子目录，其中保存在 servlet 引擎关闭时处于活动状态的任何 HTTP 会话的序列化版本。通常，`WEB-INF` 适用于你想在 Web 应用程序中使用但又希望对用户隐藏、防止直接访问的任何数据。

## 资源映射

Web 服务器有一个文档根目录，主要包含 HTML 文件。例如，在 Apache 中，这是 `<apache root>/htdocs`。Microsoft *Internet Information Server* (IIS) 使用 `inetpub/wwwroot`。当在 Web 浏览器中点击一个 URL 时，浏览器将其分解为服务器和路径组件，并向服务器发送一个针对指定资源的 HTTP 请求。Web 服务器收到请求后，从请求头中提取路径，并将其转换为相对于文档根目录的路径。例如，如果 URL 是

```
http://www.lyricnote.com/products/index.html
```

浏览器会向 `www.lyricnote.com` 主机打开一个 HTTP 连接，并发送一个以以下行开头的请求

```
GET /products/index.html HTTP/1.0
```

如果 Web 服务器是 Apache 并且安装在 `/usr/local/Apache`，那么发回的文件是

```
/usr/local/Apache/htdocs/products/index.html
```

如果服务器是 Microsoft IIS 并且安装在 `c:\inetpub`，那么请求的文件是

```
c:\inetpub\wwwroot\products\index.html
```

如你所见，Web 应用程序也有一个文档根目录，但这个根目录可以位于文件系统中的任何位置。servlet 引擎在识别出 HTTP 请求是针对 servlet 或 JSP 页面时，会从 URL 中提取 Web 应用程序名称，并将其余部分映射到该应用程序内的资源。例如，如果 URL 是

```
http://www.lyricnote.com/products/contest/rules.jsp
```

那么 servlet 引擎会为 `/contest/rules.jsp` 创建一个请求，并将其传递给 `products` Web 应用程序。servlet 的处理方式类似。像这样的 URL

```
http://www.lyricnote.com/products/servlet/Counter
```

会作为对 `Counter` servlet 的请求传递给 `products` Web 应用程序。

在应用程序内的 servlet 或 JSP 页面中用于引用应用程序内另一个资源的 URL 不使用应用程序名称。例如，如果 `rules.jsp` 页面需要动态包含 `Counter` servlet 的输出，它使用这个语句

```
<jsp:include page="/servlet/Counter" flush="true"/>
```

而不是这个语句

```
<jsp:include page="/products/servlet/Counter" flush="true"/>
```

这同样适用于 `<jsp:include>`、`<%@ include %>` 指令、`<%@ taglib %>` 指令以及创建 `RequestDispatcher` 对象的方法所使用的 URL。解释这些相对 URL 的规则是：

-   如果 URL 以 `/` 开头，则解释为相对于应用程序根目录。
-   如果不以 `/` 开头，则解释为相对于当前 JSP 页面。

然而，这带来了一个微妙的难题。在 JSP 页面中用作超链接、表单操作、样式表链接或图像源的 URL 由浏览器解释，而不是服务器。如果 LyricNote 主页是一个 JSP 页面，其中包含一个指向 `/products/contest/rules.jsp` 的链接，则该链接不能硬编码 `products` 应用程序名称。为什么不能？因为应用程序名称不一定是 `products`。这完全取决于系统管理员选择安装 Web 应用程序的位置。它可能被挂载为 `product_test`、`staging_area` 或其他任何名称。只有在应用程序实际运行时，JSP 页面才能知道该名称，可以通过 `request.getContextPath()` 方法获取。

1.  严格来说，构成 Web 应用程序名称的 URL 部分可以是像 `/products/test/Wednesday` 这样的多级字符串，但更常见的是使用单个令牌。
2.  部署描述符的 `<servlet-mapping>` 元素可用于将任何 URL 子字符串映射到特定的 servlet。此处显示的是默认映射。

你可以通过几种方式解决这个问题。JSP 页面可以将每个 URL 写为一个 JSP 表达式，将 `request.getContextPath()` 与 URL 的其余部分拼接起来，但这会变得乏味并使代码不必要地混乱。更优雅的方法是使用 HTML `<BASE>` 元素为页面分配一个上下文：

```
<HTML>
<HEAD>
<BASE HREF="http://www.lyricnote.com/products/">
</HEAD>
<BODY>
<A HREF="contest/rules.jsp">查看竞赛规则</A>
</BODY>
</HTML>
```

使用 `<BASE>` 语句，Web 浏览器可以将任何非绝对 URL 相对于 HREF 属性进行解释。因此，`contest/rules.jsp` 变成了 `http://www.lyricnote.com/products/contest/rules.jsp`。
当然，你还没有完成。你仍然需要在运行时确定 `BASE HREF`。HREF 属性需要是一个完整的 URL，而不仅仅是从服务器开始的绝对路径，因此你需要许多细节。如果连接使用 SSL，URL 可能以 `https` 开头。可能存在端口号，而不仅仅是默认端口 80。幸运的是，`request` 对象可以提供所有这些信息。以下脚本段以通用方式解决了这个问题。

```
<%
    String    scheme    = request.getScheme();
    String    server    = request.getServerName();
    int       port      = request.getServerPort();
    String    path      = request.getContextPath();

    StringBuffer sb = new StringBuffer();
    sb.append(scheme);
    sb.append("://");
    sb.append(server);
    if ((port != -1) && (port != 80)) {
        sb.append(":");
        sb.append(port);
    }
    sb.append(path);
    sb.append("/");
%>
```

```
String baseURL = sb.toString();
%>
<BASE HREF="<%= baseURL %>">
```

## Servlet 上下文

在 Web 应用程序中，servlet 和 JSP 页面可以通过一个称为 *servlet 上下文* 的公共对象共享数据和功能。这是一个实现了 `javax.servlet.ServletContext` 接口的对象。servlet 上下文具有许多有用的用途：

-   ■ **对象共享** servlet 和 JSP 页面都可以按名称在 servlet 上下文中存储对象，以便其他 servlet 和 JSP 页面可以检索它们。只要应用程序处于活动状态，这些绑定就会持续存在。
-   ■ **初始化参数** 应用程序中使用的常量可以在部署描述符中指定，并通过 servlet 上下文中的方法访问。这允许配置详细信息（如数据库 URL 和驱动程序类名称）在任何编译后的 Java 代码之外指定。
-   ■ **请求分派** servlet 可以将请求转发给其他 servlet 和 JSP 页面，或将其输出包含在当前输出流中。servlet 上下文提供使用路径或 servlet 名称创建请求分派器的方法。
-   ■ **消息日志** servlet 上下文可以访问 servlet 日志，并可用于以与供应商无关的方式写入消息。

有关 servlet 上下文提供的方法的完整描述，请参见表 4-8。
在 JSP 页面中，servlet 上下文对象在 `application` 隐式变量中自动可用。在 servlet 中，可以通过 `getServletContext()` 方法获取它。

## Web 存档 (war) 文件

到目前为止描述的是 Web 应用程序的运行时结构。对于部署，此结构必须折叠成一个称为 *Web 存档 (war)* 文件的单个文件。这只不过是一个具有不同扩展名（`.war`）的 `.jar` 文件，其顶层对应于 Web 应用程序的根目录。
以一个具体的例子来考虑，考虑 `products` Web 应用程序，如图 18-2 所示。其根目录包含一个 `index.jsp` 文件和四个内容



## 部署描述符——web.xml

`WEB-INF` 目录中的 `web.xml` 文件被称为 *部署描述符*。这是一个具有严格定义格式的 XML 文档，用于指定 Web 应用程序的配置。除了其他用途外，它可用于描述

- Servlet 别名、映射和初始化参数
- 会话超时限制
- 在整个应用程序中可用的全局参数
- 安全配置
- Mime 类型

因为此文件是 XML 文档，所以其格式由 *文档类型定义*（DTD）描述。DTD 名为 `web-app_x.y.dtd`，其中 `x.y` 是 Servlet API 规范版本，例如 2.2。它由 Sun Microsystems 发布，可从 http://java.sun.com/j2ee/dtds/web-app_2_2.dtd 下载。

最简单的 `web.xml` 文件如下所示：

```
<?xml version="1.0"?>
<!DOCTYPE web-app PUBLIC
    "-//Sun Microsystems, Inc.//DTD Web Application 2.2//EN"
    "http://java.sun.com/j2ee/dtds/web-app_2_2.dtd">
<web-app>
</web-app>
```

在 `<web-app>` 元素的主体中是其他描述应用程序配置的元素。表 18-1 列出了可使用的元素。

> 在 `<web-app>` 主体内使用的任何元素都必须严格按照列出的顺序指定。如果允许元素多次出现，则它们必须全部连续出现，而不能与其他元素交错。例如，所有 `<servlet>` 元素必须出现在任何 `<servlet-mapping>` 元素之前。

### 表 18-1. web.xml 部署描述符的内容

| 元素 | 内容 |
| :--- | :--- |
| `<web-app>` | 这是顶级元素。它可能包含以下任何子元素，顺序如下：<br>`<icon>`（可选）<br>`<display-name>`（可选）<br>`<description>`（可选）<br>`<distributable>`（可选）<br>`<context-param>`（零个或多个）<br>`<servlet>`（零个或多个）<br>`<servlet-mapping>`（零个或多个）<br>`<session-config>`（可选）<br>`<mime-mapping>`（零个或多个）<br>`<welcome-file-list>`（可选）<br>`<error-page>`（零个或多个）<br>`<taglib>`（零个或多个）<br>`<resource-ref>`（零个或多个）<br>`<security-constraint>`（零个或多个）<br>`<login-config>`（可选）<br>`<security-role>`（零个或多个）<br>`<env-entry>`（零个或多个）<br>`<ejb-ref>`（零个或多个） |
| `<icon>` | 允许开发人员指定应用程序内图标的相对位置，图标可以是 JPEG 或 GIF 格式。这些图标可被 GUI 管理工具用来表示该应用程序。它可能包含以下任一元素，或两者都包含：<br>`<small-icon>`（可选）<br>`<large-icon>`（可选） |
| `<small-icon>` | 16 × 16 图标的图像文件名。 |
| `<large-icon>` | 32 × 32 图标的图像文件名。 |
| `<display-name>` | 父元素（`<web-app>` 或 `<servlet>`）的简短名称，可被管理工具使用。 |
| `<description>` | 父元素的描述，可被管理工具使用。此元素可在此文件中的多个不同上下文中出现。 |
| `<distributable>` | 如果指定，表示此应用程序设计为在多个分布式 Servlet 容器中运行。 |
| `<context-param>` | 定义一个应用程序范围的初始化参数。包含以下子元素：`<param-name>`（必需）`<param-value>`（必需）`<description>`（可选） |
| `<param-name>` | 参数名称。 |
| `<param-value>` | 参数值。 |
| `<servlet>` | 定义一个 Servlet 及其所有相关配置。可能包含以下子元素，顺序如下：`<icon>`（可选）`<servlet-name>`（必需）`<display-name>`（可选）`<description>`（可选）`<servlet-class>` 或 `<jsp-file>`（必须指定其中一个）`<init-param>`（零个或多个）`<load-on-startup>`（可选）`<security-role-ref>`（零个或多个） |
| `<servlet-name>` | Servlet 容器所知的 Servlet 名称。注意，具有不同 Servlet 名称的多个 `<servlet>` 元素可以指定相同的 Servlet 类。在这种情况下，Servlet 引擎会创建该 Servlet 的多个实例。Servlet 可以调用 GenericServlet 或 ServletConfig 中的 `getServletName()` 方法来确定其名称。 |
| `<servlet-class>` | Servlet 类的完全限定名。 |
| `<jsp-file>` | 相对于 Web 应用程序根目录的 JSP 文件的完整路径。 |
| `<init-param>` | 定义 Servlet 初始化参数。包含以下子元素：`<param-name>`（必需）、`<param-value>`（必需）、`<description>`（可选） |
| `<load-on-startup>` | 如果指定，此元素表示当 Servlet 引擎启动时应预加载此 Servlet。这意味着将调用 Servlet 的 `init()` 方法，随后该 Servlet 将可用于处理请求。此元素的值（如果有）可以是一个整数，用于指定如果存在多个 Servlet 时此 Servlet 应启动的相对顺序。 |
| `<servlet-mapping>` | 指定哪些 URL 模式应映射到哪些 Servlet 名称。必须包含以下子元素：`<servlet-name>`（必需）、`<url-pattern>`（必需）。 |
| `<url-pattern>` | 指示一个模式，必须与 URL 的子字符串匹配才能调用此 Servlet。该模式可以包含通配符 `*`。 |
| `<session-config>` | 定义会话配置参数。可能包含 `<session-timeout>` 子元素。 |
| `<session-timeout>` | 在终止 HTTP 会话之前，Servlet 引擎允许的无活动默认分钟数。 |
| `<mime-mapping>` | 定义由文件扩展名隐含的 MIME 类型。必须包含以下元素：`<extension>`（必需）`<mime-type>`（必需）。 |
| `<extension>` | 指示文件类型的文件名后缀。例如，`png` 用于表示可移植网络图形文件。 |
| `<mime-type>` | 与特定文件扩展名关联的 MIME 类型。例如，`image/png` 用于表示可移植网络图形文件。 |
| `<welcome-file-list>` | 零个或多个 `<welcome-file>` 元素的列表。当请求的 URL 是一个目录时，Servlet 引擎会依次尝试每个欢迎文件。 |
| `<welcome-file>` | 如果 URL 中未指定文件名，则用于处理目录中请求的默认文件。例如 `index.html` 或 `index.jsp`。 |
| `<taglib>` | 用于定义 JSP 标签库的 URL 映射。必须包含以下子元素：`<taglib-uri>`（必需）`<taglib-location>`（必需） |
| `<taglib-uri>` | 旨在用于 `<%@ taglib %>` 指令的 uri 属性中的字符串。虽然此处通常指定 URL 或路径，但它不必指向实际的 Web 资源。它仅作为唯一标识符，JSP 页面可用于将标签库指令映射到标签库描述符（TLD）。 |

子目录：contest、debug、images 和 sounds。此外，它包含一个 WEB-INF 目录，其中有必需的 classes 和 lib 子目录，以及 web.xml 部署描述符。

要创建 .war 文件，请转到 products 目录并使用 JDK jar 命令行工具：

```
D:\lyricnote\products>jar -cvf products.war *
added manifest
adding: contest/(in = 0)  (out= 0) (stored 0%)
adding: contest/contest.url(in = 184)  (out= 125) (deflated 32%)
adding: contest/index.jsp(in = 1890)  (out= 739) (deflated 60%)
adding: debug/(in = 0)  (out= 0) (stored 0%)
adding: debug/AddProduct.jsp(in = 400)  (out= 240) (deflated 40%)
adding: debug/AddProduct2.jsp(in = 543)  (out= 292) (deflated 46%)
adding: debug/Example1.jsp(in = 153)  (out= 119) (deflated 22%)
adding: debug/Example1.url(in = 76)  (out= 78) (deflated -2%)
adding: images/(in = 0)  (out= 0) (stored 0%)
adding: index.jsp(in = 782)  (out= 392) (deflated 49%)
adding: sounds/(in = 0)  (out= 0) (stored 0%)
adding: sounds/BIRDS.MID(in = 3494)  (out= 1138) (deflated 67%)
adding: sounds/ITBGON.MID(in = 975)  (out= 478) (deflated 50%)
adding: WEB-INF/(in = 0)  (out= 0) (stored 0%)
adding: WEB-INF/classes/(in = 0)  (out= 0) (stored 0%)
adding: WEB-INF/lib/(in = 0)  (out= 0) (stored 0%)
adding: WEB-INF/web.xml(in = 46)  (out= 37) (deflated 19%)
```

有关 jar 工具的完整详细信息，请参阅 JDK 文档。

生成的文件 products.war 已准备好部署。所有兼容 Servlet 2.2 的 Servlet 引擎都必须直接接受 .war 文件并构建相应的 Web 应用程序。正如您可能预料的那样，安装文件的具体方式因供应商而异。作为参考实现的 Tomcat 允许将 .war 文件直接放入 `<tomcat_home>/webapps` 目录。当 Tomcat 重启时，.war 文件将被解包和验证，新的应用程序即可使用。商业 Servlet 引擎通常提供 GUI 管理工具来完成此工作。JRun 在其管理控制台中提供了一个部署向导（如图 18-3 所示），用于从 .war 文件部署应用程序。



| 元素 | 内容 |
| :--- | :--- |
| `<taglib-location>` | 相对于 Web 应用程序根目录的 URI，在该位置可以找到标签库描述符 (TLD)。例如：/WEB-INF/tlds/mytags.tld。 |
| `<error-page>` | 将 HTTP 响应代码或异常类型映射到一个 servlet、JSP 页面或 HTML 文件，当发生错误时将默认调用该文件。包含以下子元素：`<error-code>` 或 `<exception-type>`（两者必选其一）`<location>`（必需） |
| `<error-code>` | 要映射到错误页面的 HTTP 响应代码。 |
| `<exception-type>` | 完全限定的 Java 异常类名。 |
| `<location>` | 用作错误页面的 servlet、JSP 页面或 HTML 文件的 URI。 |
| `<resource-ref>` | 包含用于设置 J2EE 资源工厂的信息。可能包含以下子元素：`<description>`（可选）`<res-ref-name>`（必需）`<res-type>`（必需）`<res-auth>`（必需）。 |
| `<res-ref-name>` | 指定资源工厂引用的名称。 |
| `<res-type>` | 指定与资源工厂关联的数据源的 Java 类名。 |
| `<res-auth>` | 指示提供给资源工厂的凭据来源。存在两个可能的值：SERVLET—Web 应用程序以编程方式提供该值。CONTAINER—由容器提供凭据。 |

**表 18-1.** web.xml 部署描述符的内容（续）

| 元素 | 内容 |
| :--- | :--- |
| `<security-constraint>` | 定义要应用于一个或多个资源集合的安全约束。可能包含以下子元素：`<web-resource-collection>`（一个或多个）、`<auth-constraint>`（可选）、`<user-data-constraint>`（可选） |
| `<web-resource-collection>` | 定义 Web 应用程序中可以应用安全约束的一组资源。可能包含以下子元素：`<web-resource-name>`（必需）、`<description>`（可选）、`<url-pattern>`（零个或多个）、`<http-method>`（零个或多个） |
| `<web-resource-name>` | Web 资源的可引用名称。 |
| `<http-method>` | HTTP 方法类型（例如，GET、POST 等）。 |
| `<user-data-constraint>` | 指定传输到应用程序和从应用程序传出的数据应如何保护。可能包含以下子元素：`<description>`（可选）、`<transport-guarantee>`（必需） |
| `<transport-guarantee>` | 允许的值为 NONE—应用程序不需要传输保证。INTEGRITY—要求数据在传输过程中不能被更改。CONFIDENTIAL—要求数据在传输过程中不能被读取。 |
| `<auth-constraint>` | 指定在 `<security-constraint>` 元素中集体处理的角色名称列表。可能包含以下子元素：`<description>`（可选）、`<role-name>`（零个或多个） |

**表 18-1.** *web.xml 部署描述符的内容（续）*

| 元素 | 内容 |
| :--- | :--- |
| `<role-name>` | 用于标识已验证用户可以登录的角色的名称。这与 `request.isUserInRole()` 方法中指定的值相同，允许不同角色的用户有条件地执行 servlet 的某些部分。 |
| `<login-config>` | 指定登录配置的类型。可能包含以下子元素：`<auth-method>`（可选）`<realm-name>`（可选）`<form-login-config>`（可选）。 |
| `<realm-name>` | HTTP 基本认证中使用的领域名称。 |
| `<form-login-config>` | 指定基于表单的登录所使用的资源。必须包含以下子元素：`<form-login-page>`（必需）`<form-error-page>`（必需） |
| `<form-login-page>` | 指定提示输入用户名和密码的资源（HTML 文件、JSP 页面、servlet）的名称。此页面必须遵守以下要求：1. 表单必须使用 `METHOD="POST"` 和 `ACTION="j_security_check"`。2. 用户名字段必须命名为 `j_username`。3. 密码字段必须命名为 `j_password`。 |
| `<form-error-page>` | 指定当基于表单的登录不成功时显示的资源（HTML 文件、JSP 页面、servlet）的名称。 |
| `<auth-method>` | 指定使用的认证方法。存在四个合法值：`BASIC`、`DIGEST`、`FORM`、`CLIENT-CERT`。并非所有 servlet 引擎都支持所有方法。 |

| 元素 | 内容 |
| :--- | :--- |
| `<security-role>` | 声明一个安全角色名称，该名称可在 `<security-constraints>` 元素中有效使用。可能包含以下子元素：`<description>`（可选）`<role-name>`（必需） |
| `<security-role-ref>` | 创建角色名称与其别名之间的映射。可能包含以下子元素：`<description>`（可选）`<role-name>`（必需）`<role-link>`（必需）。这允许 servlet 在 `request.isUserInRole()` 方法中使用角色链接，并将该名称等同于实际的角色名称。此后，如果应用程序被修改为使用不同的角色名称，则无需修改 servlet。 |
| `<role-link>` | servlet 用于引用实际角色名称的符号名称。 |
| `<env-entry>` | 用于定义 J2EE 环境条目。可能包含以下子元素：`<description>`（可选）`<env-entry-name>`（必需）`<env-entry-value>`（可选）`<env-entry-type>`（必需） |
| `<env-entry-name>` | 相对于 JNDI `java:comp/env` 上下文的 J2EE 环境条目名称。 |
| `<env-entry-value>` | J2EE 环境条目的值。 |
| `<env-entry-type>` | 必须是以下之一：`java.lang.Boolean` `java.lang.String` `java.lang.Integer` `java.lang.Double` `java.lang.Float` |

**表 18-1.** *web.xml 部署描述符的内容（续）*

| 元素 | 内容 |
| :--- | :--- |
| `<ejb-ref>` | 定义对 *Enterprise Java Bean* (EJB) 的引用。可能包含以下子元素：`<description>`（可选）`<ejb-ref-name>`（必需）`<ejb-ref-type>`（必需）`<home>`（必需）`<remote>`（必需）`<ejb-link>`（可选） |
| `<ejb-ref-name>` | EJB 引用的 JNDI 名称。 |
| `<ejb-ref-type>` | EJB 的 Java 类。 |
| `<home>` | 作为 EJB 主接口的类的完全限定名称。 |
| `<remote>` | 作为 EJB 远程接口的类的完全限定名称。 |
| `<ejb-link>` | 在包含此 EJB 的 J2EE 应用程序中，此 EJB 链接到的 EJB 的名称。 |

**表 18-1.** *web.xml 部署描述符的内容（续）*

# 示例部署描述符

表 18-1 看起来很复杂，但幸运的是，大多数部署描述符仅使用了所有可能元素中的一小部分。以下列表显示了一个典型的 web.xml 文件：

```xml
<?xml version="1.0"?>

<!DOCTYPE web-app PUBLIC
    "-//Sun Microsystems, Inc.//DTD Web Application 2.2//EN"
    "http://java.sun.com/j2ee/dtds/web-app_2_2.dtd">

<web-app>

    <context-param>
        <param-name>JDBC.DRIVER</param-name>
        <param-value>
        org.enhydra.instantdb.jdbc.idbDriver
      </param-value>
    </context-param>

    <context-param>
      <param-name>JDBC.URL</param-name>
      <param-value>
        jdbc:idb:d:/lyricnote/WEB-INF/db.prp
      </param-value>
    </context-param>

    <servlet>
      <servlet-name>Sample</servlet-name>
      <servlet-class>
        jspcr.servlets.SampleServlet
      </servlet-class>
      <init-param>
        <param-name>message</param-name>
        <param-value>Hello, world</param-value>
      </init-param>
    </servlet>

    <servlet>
      <servlet-name>daytime</servlet-name>
      <servlet-class>
        jspcr.services.daytime
      </servlet-class>
      <load-on-startup>1</load-on-startup>
    </servlet>

  </web-app>
```

此部署描述符包含四个元素：两个上下文参数和两个 servlet 声明。上下文参数定义了可在 Web 应用程序中所有 servlet 和 JSP 页面中使用的常量。在此例中，它们定义了一个 JDBC 驱动程序类和一个数据库 URL。servlet 和 JSP 页面可以通过 servlet 上下文的 `getInitParameter()` 方法检索这些值。由于这类信息经常变化，并且在不同的安装环境中通常有所不同，因此能够在此处描述它，而不是将其硬编码在 Java 类中，会更加方便。



## 总结

随着 Servlet 2.2 规范的推出，Web 应用程序的部署变得标准化且与供应商无关。该规范描述了一个标准的目录结构，用于存放 Web 内容、配置信息以及类目录。配置信息在一个名为 `web.xml` 的 XML 文档中指定，该文档即 *部署描述符*。目录结构在 `Web 归档文件 (.war)` 格式中得以镜像体现。部署 Web 应用程序并将其从一个 Servlet 引擎迁移到另一个，通常只需安装 `.war` 文件并调用 Servlet 引擎的部署工具即可。

## 第 19 章
## 案例研究：产品支持中心

我们假设的互联网音乐商店 LyricNote.com 销售各类音乐产品：乐谱、乐器、音乐主题书籍、礼品以及音乐软件。对这些产品的支持包括接听电话订单、查询订单状态、处理账单问题以及提供软件技术支持。最后一项是本章的重点。
在这个案例研究中，你将开发一个基于 Web 的系统来管理产品支持中心。该系统的用户可以报告和跟踪产品缺陷，记录相关评论，并将问题转交给合适的人员。

为清晰起见，该应用程序并未包含一个真实生产系统可能具备的所有验证、用户控制或管理报告功能。但是，它确实阐述了本书中描述的许多技术，并为进一步开发提供了一个模型。

### 流程

首先，让我们考虑一下系统将运行的环境。流程如图 19-1 所示。
当客户致电报告软件问题时，第一位空闲的呼叫中心坐席会接听电话。如果问题与软件无关，这位 *呼叫中心坐席* 可能会将电话转接给销售或客户服务部门。否则，坐席会核实客户是否有权获得支持，即客户是指定产品的合法购买者。坐席创建一份问题报告，并告知客户等待产品支持部门的回电。

问题报告会被路由到负责报告缺陷产品的 *产品支持专员*。每位产品支持专员都有一个待处理问题报告队列，当收到新问题时，专员会致电客户获取更多详情，试图确定这是客户问题还是代码问题。客户问题可能涉及缺少必需的硬件或软件，或未能正确安装产品。在这些情况下，产品支持人员会尽可能帮助客户解决问题，然后关闭问题报告。

如果问题与代码相关，可能其他客户也遇到过该问题且已有修复方案。如果确实如此，修复方案会记录在知识库中，产品支持人员可以通过相应的关键词进行搜索。修复问题所需的补丁或操作步骤会通过电子邮件发送给客户，或在网站上提供下载。

如果知识库中找不到该问题，则会将其路由到列为该产品主要支持人员的 *开发人员*。开发人员分析问题并尝试复现。可能是产品按设计运行，此时缺陷会被重新路由回产品支持部门，并标记为“非缺陷”。否则，开发人员将尝试隔离缺陷并开发修复方案。在对修复方案进行单元测试后，开发人员将问题路由给质量保证部门。问题报告可能会更新，以说明如何复现问题以及从何处获取修复所需的代码补丁。

产品的 *质量保证* 支持人员从开发部门接收问题报告并测试修复方案。这是一项集成测试，旨在检查新代码对现有系统的影响。如果修复引入了其他问题或未能通过所有已建立的测试用例，则问题将重新路由回开发部门。否则，修复方案会被路由到产品支持部门，以便联系客户并提供新代码。

在任何节点，系统用户都可以查看特定问题的状态、添加评论并将问题路由到下一个目的地。为了达到最佳效果，每次路由都应伴随向新问题负责人发送电子邮件。此部分在本应用中未开发，相关主题将留待第 21 章探讨 Java Mail API。

总结一下，系统用户及其职能如下：

- **呼叫中心坐席**
    - 核实客户资格
    - 录入新问题
    - 可查看现有问题的状态
- **产品支持**
    - 接收来自呼叫中心的新问题报告
    - 可按产品查看待处理问题
    - 与客户沟通
    - 更新问题状态
    - 添加评论
    - 将问题路由给开发部门
- **开发人员**
    - 接收来自产品支持的问题报告
    - 可按产品查看待处理问题
    - 分析问题并开发修复方案
    - 为问题报告添加评论
    - 将问题路由给质量保证部门
- **质量保证**
    - 接收来自开发部门的问题报告和修复方案
    - 执行集成测试
    - 为问题报告添加评论
    - 将已修复的问题路由给产品支持部门
    - 如果测试失败，可能会将问题重新路由给开发人员

此外，管理人员可以随时查看问题状态，并访问显示质量统计信息的报告，例如排队时间、每个产品报告的缺陷数以及按开发人员划分的未解决缺陷数。这些报告未包含在本应用程序中，但可以从问题数据库开发出来。

### 数据模型

表 19-1 描述了用于记录和跟踪问题所需全部数据的数据库表。

| 表名 | 描述 | 字段 |
|---|---|---|
| customer | 购买过 LyricNote 产品的客户列表。 | customerID<br>客户姓名<br>电话 |
| product | 产品及其支持人员列表。 | productID<br>产品名称<br>产品支持人员<br>主要开发人员<br>主要测试人员 |
| custprod | 客户/产品对列表，指示哪位客户购买了哪个产品。 | customerID<br>productID<br>购买日期 |
| problems | 报告问题的主要记录。 | problemID<br>描述<br>严重程度 (1=高, 2=中, 3=低)<br>报告日期<br>解决日期 (如果已关闭)<br>customerID<br>productID |
| problog | 报告问题生命周期中的事件日志。 | problemID<br>时间戳<br>eventID<br>评论 |
| employees | 系统用户，包括呼叫中心坐席、产品支持、开发人员和测试人员。 | employeeID<br>姓名<br>其他字段 (此处未使用) |

**表 19-1。** *产品支持应用的数据模型*

### 开发系统

JSP 是一个便捷的开发环境。页面在需要时会自动编译，URL 可以轻松映射到目录位置。在 JSP 页面内，你可以自由混合使用 HTML 和 Java，这提供了极大的灵活性。



不幸的是，这些优点也意味着普通的JSP应用程序无法良好扩展。随着越来越多的Java代码嵌入到JSP页面中，跟踪这些代码变得越来越困难。与可以被编译和进行单元测试的Java类不同，JSP脚本代码不易与其容器分离。在大段嵌入Java代码的HTML中保持一致性也很困难。你可能一开始使用bean来完成大部分工作，但后来发现它们不能完全满足你的需求，于是不得不在HTML中嵌入一些额外的Java代码。如果应用程序大量使用`<%@ include %>`指令，这些问题会变得更加严重。

在更大的应用程序中，需要一种更好的方法将代码分离成具有清晰职责的组件。对于你的产品支持系统，你使用了*模型-视图-控制器*（MVC）设计模式。

## 模型-视图-控制器架构

MVC背后的理念是，系统的可视化方面应与其内部工作方式隔离，而内部工作方式又应与启动和控制它的机制分离。MVC架构最初由Smalltalk及其实践者广泛采用，但现在已成为一种广泛使用的设计模式。图19-2展示了MVC的工作原理。

*模型*是指管理系统的抽象内部状态和操作的代码。它处理数据库访问和大部分业务逻辑。模型没有可视化组件，而是提供一个可供系统其他部分访问的应用程序编程接口。这使得编写一个驱动程序成为可能，该驱动程序可以从一个简单的命令行接口测试和调试模型。

![](img/7a2f73369bb140583c7288b73456addb_582_0.png)

## 第19章：案例研究：产品支持中心

例如，在一个国际象棋游戏中，模型可能由一组表示棋子的对象和一个用于存放它们的简单的8×8数组组成。模型可以有一些方法，用于指示轮到谁走棋、评估一个给定的走法是否合法，以及将棋子从一个数组元素移动到另一个数组元素。模型*不会*包含提供棋盘任何可视化表示的代码。

*视图*是系统的表示层。它不进行数据库访问，也不包含业务逻辑。视图中少量的非可视化代码仅限于表示逻辑，例如循环遍历要显示的对象数组。根据设计，一个模型可以与多个视图关联，也许是一个*图形用户界面*（GUI）和一个打印报告。例如，一个基于Web的两人游戏可以为每个玩家提供一个视图，两者都连接到同一个模型。这不需要对模型进行任何更改，因为模型不知道它是如何被显示的。

在国际象棋游戏的情况下，视图将包含绘制棋盘和棋子、列出走法和显示时钟的代码。它不会了解国际象棋的规则、轮到谁走棋，甚至不知道棋子的位置。视图会调用模型中的方法来跟踪所有这些信息。尽管GUI代码通常很复杂，但视图只需要担心它的可视化方面。测试和调试很简单，因为可以使用一个模型的桩版本来测试视图的所有部分。

*控制器*是根据用户输入操作模型的部分。基于当前视图、模型的状态以及用户采取的操作，控制器调用模型API来更新模型状态并选择下一个视图。粗略地说，控制器处理来自用户的*输入*，而视图处理输出给用户的*输出*。国际象棋游戏可能有两个控制器——一个负责传达人类玩家的走法，另一个负责选择计算机的走法。

在这个产品支持系统中，模型由普通的Java类（不是servlet，也不是面向网络的）组成。简单的JSP页面用作视图，控制器是一个带有支持类的单个servlet。

## 模型类

让我们首先检查产品支持系统的模型。它由三组类组成：

- 表示业务对象的类，大致对应于数据库中的表
- 应用程序容器和接口类
- 一个测试框架

这些类共同构成了`com.lyricnote.support.model`包。除了维护应用程序状态外，模型还包含所有访问数据库的代码，使用一个会话感知的包装类来确保数据库资源得到正确管理。

## 业务对象

六个类封装了数据模型中使用的业务实体：

- com.lyricnote.support.model.Customer
- com.lyricnote.support.model.Product
- com.lyricnote.support.model.CustomerProduct
- com.lyricnote.support.model.Employee
- com.lyricnote.support.model.Problem
- com.lyricnote.support.model.ProblemLog

以下部分列出了每个类的源代码并描述了它们的操作。

**Customer类** 包中的第一个类是`Customer`类，它表示购买了LyricNote产品并有资格获得产品支持的个人或公司。该类包含客户姓名和电话号码，以及一个唯一的客户标识符。标识符由客户姓氏的前四个字母、客户名字的首字母和尾字母以及一个两位数的唯一数字后缀组成。该类在以下清单中显示：

```java
package com.lyricnote.support.model;

import java.io.*;
import java.sql.*;
import java.util.*;

/**
 * A person or company that has bought LyricNote products.
 */
public class Customer implements Serializable
{
    private String customerID;
    private String name;
    private String phone;

    /**
     * Factory method to create a customer record
     * from the current row of a result set.
     * @param rs a result set from the customer table
     * @exception SQLException if a database error occurs
     */
    public static Customer load(ResultSet rs)
        throws SQLException
    {
        Customer customer = new Customer();
        String value = null;

        value = rs.getString(1);
        if (value != null)
            customer.setCustomerID(value);

        value = rs.getString(2);
        if (value != null)
            customer.setName(value);

        value = rs.getString(3);
        if (value != null)
            customer.setPhone(value);

        return customer;
    }

    /**
     * Returns the object as a CSV string
     */
    public String toString()
    {
        StringBuffer sb = new StringBuffer();

        if (getCustomerID() != null)
            sb.append(Util.quote(getCustomerID()));

        sb.append(",");
        if (getName() != null)
            sb.append(Util.quote(getName()));

        sb.append(",");
        if (getPhone() != null)
            sb.append(Util.quote(getPhone()));

        return sb.toString();
    }

    // ===================================================
    //     Property accessor methods
    // ===================================================

    /**
     * Returns the customerID.
     */
    public String getCustomerID()
    {
        return customerID;
    }

    /**
     * Sets the customerID.
     * @param customerID the customerID.
     */
    public void setCustomerID(String customerID)
    {
        this.customerID = customerID;
    }

    /**
     * Returns the name.
     */
    public String getName()
    {
        return name;
    }

    /**
     * Sets the name.
     * @param name the name.
     */
    public void setName(String name)
    {
        this.name = name;
    }

    /**
     * Returns the telephone number
     */
    public String getPhone()
    {
        return phone;
    }

    /**
     * Sets the telephone number.
     * @param phone the phone.
     */
    public void setPhone(String phone)
    {
        this.phone = phone;
    }
}
```

除了每个属性的getter和setter方法外，Customer类还包含一个`toString()`方法，该方法返回一个逗号分隔值字符串，以及一个名为`load()`的类方法。`load()`方法从SQL结果集中的客户表行创建一个Customer对象。此方法在模型应用程序类中用于简化从数据库中检索Customer对象集合。

`toString()`方法中的`Util.quote()`方法将在本章后面的“应用程序对象”部分讨论。

**Product类** 接下来是Product类，表示产品表中的一行。它的属性由唯一的产品标识符、产品名称以及产品的主要支持人员、首席开发人员和首席测试人员的员工号组成。该类在以下清单中显示。

```java
package com.lyricnote.support.model;

import java.io.*;
import java.sql.*;
import java.util.*;

/**
 * A software product supported by the Product
 * Support system.
 */
public class Product implements Serializable
```



## 566 JSP：权威参考指南

与 `Customer` 类类似，`Product` 类也为其每个属性提供了 getter 和 setter 方法，以及自定义的 `toString()` 方法和用于从结果集行加载 `Product` 对象的工厂方法。

### CustomerProduct 类

呼叫中心坐席的一个关键职责是验证*客户权限*，这意味着报告问题的人必须是有效客户，并且购买了指定的产品。这通过 `custprod` 表中连接客户和产品的记录是否存在来表示。与此表对应的类是 CustomerProduct，如以下代码所示：

```java
package com.lyricnote.support.model;

import java.io.*;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.util.*;

/**
 * 一个客户/产品对，其存在表明客户购买了指定的产品。
 */
public class CustomerProduct implements Serializable
{
    private String customerID;
    private String productID;
    private Date datePurchased;

    /**
     * 工厂方法，用于从结果集的当前行创建一条客户/产品记录。
     * @param rs 来自客户表的结果集
     * @exception SQLException 如果发生数据库错误
     */
    public static CustomerProduct load(ResultSet rs)
        throws SQLException
    {
        CustomerProduct custprod = new CustomerProduct();

        custprod.setCustomerID(rs.getString(1));
        custprod.setProductID(rs.getString(2));
        custprod.setDatePurchased(rs.getDate(3));

        return custprod;
    }

    /**
     * 将对象表示为 CSV 字符串
     */
    public String toString()
    {
        StringBuffer sb = new StringBuffer();

        sb.append(getCustomerID());
        sb.append(",");
        sb.append(getProductID());
        sb.append(",");
        sb.append(Util.dateFormat(getDatePurchased()));

        return sb.toString();
    }

    // ========================================
    //    属性访问器方法
    // ========================================

    /**
     * 返回 customerID。
     */
    public String getCustomerID()
    {
        return customerID;
    }

    /**
     * 设置 customerID。
     * @param customerID customerID 的值。
     */
    public void setCustomerID(String customerID)
    {
        this.customerID = customerID;
    }

    /**
     * 返回 productID。
     */
    public String getProductID()
    {
        return productID;
    }

    /**
     * 设置 productID。
     * @param productID productID 的值。
     */
    public void setProductID(String productID)
    {
        this.productID = productID;
    }

    /**
     * 返回 datePurchased。
     */
    public Date getDatePurchased()
    {
        return datePurchased;
    }

    /**
     * 设置 datePurchased。
     * @param datePurchased datePurchased 的值。
     */
    public void setDatePurchased(Date datePurchased)
    {
        this.datePurchased = datePurchased;
    }
}
```

CustomerProduct 包含客户 ID、产品 ID 和产品购买日期的字段。这些信息来自产品注册回寄卡或手动输入（此处未展示）。与 Customer 和 Product 类类似，CustomerProduct 也有 getter 和 setter 方法、一个用于创建逗号分隔值字符串的 `toString()` 方法，以及一个用于从数据库加载对象的工厂方法。

### Employee 类

每个产品都关联一位产品支持人员、一位主开发人员和一位主测试人员。关于这些员工的信息包含在 employee 表中，并封装在 Employee 类中，如下所示：

```java
package com.lyricnote.support.model;

import java.io.*;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.util.*;

/**
 * 一位使用产品支持系统的 LyricNote 员工。
 */
public class Employee implements Serializable
{
    private String employeeID;
    private String name;
    private Date dateHired;
    private boolean isManager;
    private String departmentID;
    private String title;
    private String email;
    private String phone;

    /**
     * 工厂方法，用于从结果集的当前行创建一条员工记录。
     * @param rs 来自 employee 表的结果集
     * @exception SQLException 如果发生数据库错误
     */
    public static Employee load(ResultSet rs)
        throws SQLException
    {
        Employee employee = new Employee();

        employee.setEmployeeID(rs.getString(1));
        employee.setName(rs.getString(2));
        employee.setDateHired(rs.getDate(3));
        employee.setIsManager(rs.getBoolean(4));
        employee.setDepartmentID(rs.getString(5));
        employee.setTitle(rs.getString(6));
        employee.setEmail(rs.getString(7));
        employee.setPhone(rs.getString(8));

        return employee;
    }

    /**
     * 将对象表示为 CSV 字符串
     */
    public String toString()
    {
        StringBuffer sb = new StringBuffer();
    }
}
```



## 570 JSP：完全参考手册

```
sb.append(getEmployeeID());
sb.append(",");
sb.append(Util.quote(getName()));
sb.append(",");
sb.append(Util.dateFormat(getDateHired()));
sb.append(",");
sb.append(getIsManager());
sb.append(",");
sb.append(getDepartmentID());
sb.append(",");
sb.append(Util.quote(getTitle()));
sb.append(",");
sb.append(getEmail());
sb.append(",");
sb.append(getPhone());

return sb.toString();
}
```

```
// ============================================================
//    属性访问器方法
// ============================================================

/**
* 返回员工ID。
*/
public String getEmployeeID()
{
    return employeeID;
}

/**
* 设置员工ID。
* @param employeeID 员工ID。
*/
public void setEmployeeID(String employeeID)
{
    this.employeeID = employeeID;
}

/**
* 返回员工姓名。
*/
public String getName()
{
    return name;
}

/**
* 设置员工姓名。
* @param name 员工姓名。
*/
public void setName(String name)
{
    this.name = name;
}

/**
* 返回入职日期。
*/
public Date getDateHired()
{
    return dateHired;
}

/**
* 设置入职日期。
* @param dateHired 入职日期。
*/
public void setDateHired(Date dateHired)
{
    this.dateHired = dateHired;
}

/**
* 返回是否为经理的标志。
*/
public boolean getIsManager()
{
    return isManager;
}

/**
* 设置是否为经理的标志。
* @param isManager 是否为经理的标志。
*/
public void setIsManager(boolean isManager)
{
    this.isManager = isManager;
}

/**
* 返回部门ID。
*/
public String getDepartmentID()
{
    return departmentID;
}

/**
* 设置部门ID。
* @param departmentID 部门ID。
*/
public void setDepartmentID(String departmentID)
{
    this.departmentID = departmentID;
}

/**
* 返回职位头衔。
*/
public String getTitle()
{
    return title;
}

/**
* 设置职位头衔。
* @param title 职位头衔。
*/
public void setTitle(String title)
{
    this.title = title;
}

/**
* 返回电子邮件。
*/
public String getEmail()
{
    return email;
}

/**
* 设置电子邮件。
* @param email 电子邮件。
*/
public void setEmail(String email)
{
    this.email = email;
}

/**
* 返回电话。
*/
public String getPhone()
{
    return phone;
}

/**
* 设置电话。
* @param phone 电话。
*/
public void setPhone(String phone)
{
    this.phone = phone;
}
```

与其他一些表不同，员工表不仅用于产品支持系统。因此，它包含了比产品支持系统实际使用的更多字段，如下所示：

-   employeeID 唯一的四位数员工编号
-   name 员工姓名
-   dateHired 员工的入职日期
-   isManager 一个布尔变量，如果员工是经理则为真
-   departmentID 员工所属部门的代码
-   title 职位头衔
-   email 电子邮件地址
-   phone 电话分机号

Employee 类（在以下代码清单中展示）封装了员工表中的一行。

```
package com.lyricnote.support.model;

import java.io.*;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.util.*;

/**
* 一个使用产品支持系统的 LyricNote 员工。
*/
public class Employee implements Serializable
{
    private String employeeID;
    private String name;
    private Date dateHired;
    private boolean isManager;
    private String departmentID;
    private String title;
    private String email;
    private String phone;

    /**
    * 工厂方法，用于从结果集的当前行创建员工记录。
    * @param rs 来自员工表的结果集
    * @exception SQLException 如果发生数据库错误
    */
    public static Employee load(ResultSet rs)
        throws SQLException
    {
        Employee employee = new Employee();

        employee.setEmployeeID(rs.getString(1));
        employee.setName(rs.getString(2));
        employee.setDateHired(rs.getDate(3));
        employee.setIsManager(rs.getBoolean(4));
        employee.setDepartmentID(rs.getString(5));
        employee.setTitle(rs.getString(6));
        employee.setEmail(rs.getString(7));
        employee.setPhone(rs.getString(8));

        return employee;
    }
}
```

```
/**
* 以CSV字符串形式返回对象
*/
public String toString()
{
    StringBuffer sb = new StringBuffer();

    sb.append(getEmployeeID());
    sb.append(",");
    sb.append(Util.quote(getName()));
    sb.append(",");
    sb.append(Util.dateFormat(getDateHired()));
    sb.append(",");
    sb.append(getIsManager());
    sb.append(",");
    sb.append(getDepartmentID());
    sb.append(",");
    sb.append(Util.quote(getTitle()));
    sb.append(",");
    sb.append(getEmail());
    sb.append(",");
    sb.append(getPhone());

    return sb.toString();
}
```

```
// ==========================================
//    属性访问器方法
// ==========================================

/*
* 返回员工ID。
*/
public String getEmployeeID()
{
    return employeeID;
}

/**
* 设置员工ID。
* @param employeeID 员工ID。
*/
public void setEmployeeID(String employeeID)
{
    this.employeeID = employeeID;
}

/**
* 返回员工姓名。
*/
public String getName()
{
    return name;
}

/**
* 设置员工姓名。
* @param name 员工姓名。
*/
public void setName(String name)
{
    this.name = name;
}

/**
* 返回入职日期。
*/
public Date getDateHired()
{
    return dateHired;
}

/**
* 设置入职日期。
* @param dateHired 入职日期。
*/
public void setDateHired(Date dateHired)
{
    this.dateHired = dateHired;
}

/**
* 返回是否为经理的标志。
*/
public boolean getIsManager()
{
    return isManager;
}

/**
* 设置是否为经理的标志。
* @param isManager 是否为经理的标志。
*/
public void setIsManager(boolean isManager)
{
    this.isManager = isManager;
}

/**
* 返回部门ID。
*/
public String getDepartmentID()
{
    return departmentID;
}

/**
* 设置部门ID。
* @param departmentID 部门ID。
*/
public void setDepartmentID(String departmentID)
{
    this.departmentID = departmentID;
}

/**
* 返回职位头衔。
*/
public String getTitle()
{
    return title;
}

/**
* 设置职位头衔。
* @param title 职位头衔。
*/
public void setTitle(String title)
{
    this.title = title;
}

/**
* 返回电子邮件。
*/
public String getEmail()
{
    return email;
}

/**
* 设置电子邮件。
* @param email 电子邮件。
*/
public void setEmail(String email)
{
    this.email = email;
}

/**
* 返回电话。
*/
public String getPhone()
{
    return phone;
}

/**
* 设置电话。
* @param phone 电话。
*/
public void setPhone(String phone)
{
    this.phone = phone;
}
```

Employee 类具有前面描述的 `toString()` 和 `load()` 方法。

### Problem 类

系统的核心是报告的问题集合。在数据库中，每个问题由两种类型的记录组成：一种代表整个问题，另一种代表问题从报告到关闭整个生命周期中的每个事件。静态问题数据包含在下面列出的 Problem 类中。

```
package com.lyricnote.support.model;

import java.io.*;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.util.*;

/**
 * 由问题支持系统支持的一个软件问题。
 */
public class Problem implements Serializable
{
    private String problemID;
    private String description;
    private int severity;
    private java.util.Date dateReported;
    private java.util.Date dateResolved;
    private String customerID;
    private String productID;

    /**
     * 工厂方法，用于从结果集的当前行创建问题记录。
     * @param rs 来自问题表的结果集
     * @exception SQLException 如果发生数据库错误
     */
    public static Problem load(ResultSet rs)
        throws SQLException
    {
        Problem problem = new Problem();

        problem.setProblemID(rs.getString(1));
        problem.setDescription(rs.getString(2));
        problem.setSeverity(rs.getInt(3));
        problem.setDateReported(rs.getTimestamp(4));
        problem.setDateResolved(rs.getTimestamp(5));
        problem.setCustomerID(rs.getString(6));
        problem.setProductID(rs.getString(7));

        return problem;
    }
}
```

```
/**
 * 以CSV字符串形式返回对象
 */
public String toString()
{
    StringBuffer sb = new StringBuffer();

    sb.append(getProblemID());
    sb.append(",");
    sb.append(getDescription());
    sb.append(",");
    sb.append(getSeverity());
    sb.append(",");
    sb.append(Util.dateTimeFormat(getDateReported()));
    sb.append(",");
    sb.append(Util.dateTimeFormat(getDateResolved()));
    sb.append(",");
    sb.append(getCustomerID());
    sb.append(",");
    sb.append(getProductID());

    return sb.toString();
}
```

```java
/**
 * 关闭问题
 */
public void close()
{
    setDateResolved(Util.toTimestamp(new Date()));
}
```

```
// ============================================
//   属性访问方法
// ============================================
```

```
/**
 * 返回 problemID。
 */
public String getProblemID()
{
    return problemID;
}
```

```
/**
 * 设置 problemID。
 * @param problemID 问题的唯一标识符。
 */
public void setProblemID(String problemID)
{
    this.problemID = problemID;
}
```

```
/**
 * 返回描述。
 */
public String getDescription()
{
    return description;
}
```

```
/**
 * 设置描述。
 * @param description 问题的简要描述。
 */
public void setDescription(String description)
{
    this.description = description;
}
```

```
/**
 * 返回严重性。
 */
public int getSeverity()
{
    return severity;
}
```

```
/**
 * 设置严重性。
 * @param severity 客服代表对问题关键程度的评估，1=高，2=中，3=低。
 */
public void setSeverity(int severity)
{
    this.severity = severity;
}
```

```
/**
 * 返回报告日期。
 */
public java.util.Date getDateReported()
{
    return dateReported;
}
```

```
/**
 * 设置报告日期。
 * @param dateReported 问题报告给客服中心的日期和时间。
 */
public void setDateReported(java.util.Date dateReported)
{
    this.dateReported = dateReported;
}
```

```
/**
 * 返回解决日期。
 */
public java.util.Date getDateResolved()
{
    return dateResolved;
}
```

```
/**
 * 设置解决日期。
 * @param dateResolved 问题关闭时的日期和时间。否则值为 null。
 */
public void setDateResolved(java.util.Date dateResolved)
{
    this.dateResolved = dateResolved;
}
```

```
/**
 * 返回客户ID。
 */
public String getCustomerID()
{
    return customerID;
}
```

```
/**
 * 设置客户ID。
 * @param customerID 八字符的客户标识符。
 */
public void setCustomerID(String customerID)
{
    this.customerID = customerID;
}
```

```
/**
 * 返回产品ID。
 */
public String getProductID()
{
    return productID;
}
```

```
/**
 * 设置产品ID。
 * @param productID 唯一的产品标识符。
 */
public void setProductID(String productID)
{
    this.productID = productID;
}
}
```

一个 Problem 对象包含以下字段：

- problemID：由系统分配的唯一问题标识符。
- description：用于在图形用户界面显示的简要问题描述。
- severity：客服代表对问题关键程度的评估，其中 1=高，2=中，3=低。
- dateReported：问题报告给客服中心的日期和时间。
- dateResolved：如果问题已关闭，则包含关闭的日期和时间。否则值为 null。
- customerID：八字符的客户标识符。
- productID：唯一的产品标识符。

ProblemLog 类
问题生命周期中的事件由 `problog` 表中的行来建模，该表包含以下列：

- problemID：问题标识符，用于连接 `problog` 和 `problem` 表。
- logtime：由数据库系统生成的时间戳。此字段与问题 ID 一起构成了此问题日志条目的唯一键。
- eventID：一个三字符的代码，表示问题日志事件的性质。事件 ID 代码取自以下列表：
  - COM--评论
  - RPS--路由至产品支持
  - RPD--路由至产品研发
  - RQA--路由至质量保证
  - CNB--关闭--非缺陷
  - CCP--关闭--客户问题
  - CFX--关闭--已修复
- comments：输入此日志条目的人员所做的评论。

系统使用 `ProblemLog` 类（如以下列表所示）来表示 `problog` 表中的一行。

# 第19章：案例研究：产品支持中心

```java
package com.lyricnote.support.model;

import java.io.*;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.util.*;

/**
 * 对已报告问题的更新。
 */
public class ProblemLog implements Serializable
{
    private String problemID;
    private java.util.Date logTime;
    private String eventID;
    private String comments;

    /**
     * 工厂方法，用于从结果集的当前行创建问题记录。
     * @param rs 来自问题表的结果集
     * @exception SQLException 如果发生数据库错误
     */
    public static ProblemLog load(ResultSet rs)
        throws SQLException
    {
        ProblemLog probLog = new ProblemLog();

        probLog.setProblemID(rs.getString(1));
        probLog.setLogTime(rs.getTimestamp(2));
        probLog.setEventID(rs.getString(3));
        probLog.setComments(rs.getString(4));

        return probLog;
    }

    /**
     * 以 CSV 字符串形式返回对象
     */
    public String toString()
    {
        StringBuffer sb = new StringBuffer();

        sb.append(getProblemID());
        sb.append(",");
        sb.append(Util.dateTimeFormat(getLogTime()));
        sb.append(",");
        sb.append(getEventID());
        sb.append(",");
        sb.append(getComments());

        return sb.toString();
    }

    // ==========================================
    //    属性访问方法
    // ==========================================

    /**
     * 返回 problemID。
     */
    public String getProblemID()
    {
        return problemID;
    }

    /**
     * 设置 problemID。
     * @param problemID 问题的唯一标识符。
     */
    public void setProblemID(String problemID)
    {
        this.problemID = problemID;
    }

    /**
     * 返回日志时间。
     */
    public java.util.Date getLogTime()
    {
        return logTime;
    }

    /**
     * 设置日志时间。
     * @param logTime 日志记录的时间。
     */
    public void setLogTime(java.util.Date logTime)
    {
        this.logTime = logTime;
    }

    /**
     * 返回事件ID。
     */
    public String getEventID()
    {
        return eventID;
    }

    /**
     * 设置事件ID。
     * @param eventID 事件的唯一代码。
     */
    public void setEventID(String eventID)
    {
        this.eventID = eventID;
    }

    /**
     * 返回评论。
     */
    public String getComments()
    {
        return comments;
    }

    /**
     * 设置评论。
     * @param comments 输入的评论内容。
     */
    public void setComments(String comments)
    {
        this.comments = comments;
    }
}
```

# 应用程序对象

业务对象代表系统所知的单个实体。从模型的角度来看，其他对象代表整个应用程序。此类别的类包括以下：

- com.lyricnote.support.model.Model
- com.lyricnote.support.model.WebModel
- com.lyricnote.support.model.Util

以下部分列出了这些类的源代码并描述了它们的操作。

**Model 类** 在系统运行期间，业务对象驻留在一个名为 `Model` 的应用程序容器类中。此类公开了一个 API，允许控制器操作它，并允许视图从中提取数据。每个用户会话存在一个 `Model` 对象，因此模型状态是线程安全的。`Model` 是一个相当大的类。让我们一次列出一部分，以便您详细检查它。

```java
package com.lyricnote.support.model;

import java.io.*;
import java.sql.*;
import java.util.*;

/**
 * 产品支持应用程序的模型-视图-控制器架构中的模型组件。
 * 模型设计为在具有单个用户的专用 HTTP 会话中使用，
 * 但是，没有特定于 HTTP 的代码。这使得模型可以通过
 * 批处理驱动程序进行测试。
 */
public class Model implements Serializable
{
    // 配置字段

    private String problemIDFile;
    private String jdbcDriver;
    private String databaseURL;
    private transient Connection con;

    // 客户字段

    private List customers;
    private String customerID;

    // 产品字段

    private List products;
    private String productID;

    // 问题字段

    private List problems;
    private String problemID;

    // 问题日志字段

    private List problemLogs;
```

`Model` 包含表示应用程序状态的实例变量。这些变量分为以下几类：

- **配置字段** 这些包括包含下一个可用问题 ID 号的文件名、用于访问数据库的 JDBC 驱动程序名称、数据库 URL 和数据库连接对象。
- **客户字段** 模型支持按字母顺序搜索客户名称。最近一次搜索的结果存储在 `Customer` 对象的 `java.util.List` 中。此列表作为属性公开，并通过 `getCustomers()` 方法提供。此外，模型有一个 `customerID` 属性，为需要它的多个方法提供隐式 ID。
- **产品字段** 与客户字段一样，存在用于当前产品搜索结果和当前产品 ID 的实例变量。
- **问题字段** 模型有用于当前 `Problem` 对象列表和当前选定问题的实例变量。
- **问题日志字段** 同样，有一个 `java.util.List` 用于与当前问题关联的 `ProblemLog` 对象列表。

```
// =========================================
//     配置和数据库方法
// =========================================

/**
 * 分配一个全局唯一的问题 ID
 */
```



```java
public static synchronized String assignProblemID
(String problemIDFile)
{
    String id = null;
    try {

        // 读取下一个可用 ID

        BufferedReader in =
            new BufferedReader(
                new FileReader(problemIDFile));
        id = in.readLine();
        in.close();

        // 递增 ID 并重写文件

        String prefix = id.substring(0, 1);
        int suffix = Integer.parseInt(id.substring(1));
        suffix++;
        String newID = "0000000" + String.valueOf(suffix);
        newID = newID.substring(newID.length() - 7);
        newID = prefix + newID;

        PrintWriter out =
            new PrintWriter(
                new FileWriter(problemIDFile));
        out.println(newID);
        out.flush();
        out.close();
    }
    catch (IOException e) {
        e.printStackTrace();
    }
    finally {
        return id;
    }
}

/**
* 使用当前指定的 JDBC 驱动程序和 URL 创建新连接
* @exception SQLException 如果连接失败或连接已存在
*/
public void connect()
    throws SQLException
{
    if (isConnected())
        throw new SQLException("Already connected");

    // 验证驱动程序和 URL 已指定

    if (jdbcDriver == null)
        throw new SQLException("No jdbcDriver property");

    if (databaseURL == null)
        throw new SQLException("No databaseURL property");

    // 加载驱动程序

    try {
        Class.forName(jdbcDriver).newInstance();
    }
    catch (ClassNotFoundException e) {
        throw new SQLException
        (jdbcDriver + " class could not be loaded");
    }

    // 打开连接

    con = DriverManager.getConnection(databaseURL);
}

/**
 * 关闭当前连接
 */
public void disconnect()
{
    // 关闭连接

    if (con != null) {
        try {
            con.close();
        }
        catch (SQLException ignore) {}
        finally {
            con = null;
        }
    }
}

/**
 * 如果存在活动连接则返回 true
 */
public boolean isConnected()
{
    return (con != null);
}

/**
 * 返回 jdbcDriver。
 */
public String getJdbcDriver()
{
    return jdbcDriver;
}

/**
 * 设置 jdbcDriver。
 * @param jdbcDriver jdbcDriver。
 */
public void setJdbcDriver(String jdbcDriver)
{
    this.jdbcDriver = jdbcDriver;
}

/**
 * 返回 databaseURL。
 */
public String getDatabaseURL()
{
    return databaseURL;
}

/**
 * 设置 databaseURL。
 * @param databaseURL databaseURL。
 */
public void setDatabaseURL(String databaseURL)
{
    this.databaseURL = databaseURL;
}

/**
 * 返回 problemIDFile。
 */
public String getProblemIDFile()
{
    return problemIDFile;
}

/**
 * 设置 problemIDFile。
 * @param problemIDFile problemIDFile。
 */
public void setProblemIDFile(String problemIDFile)
{
    this.problemIDFile = problemIDFile;
}
```

该模型包含一组处理数据源的方法。第一个是 `assignProblemID(String problemIDFile)`。这是一个类方法，它从文件中读取下一个可用的问题 ID，然后用递增后的数字重写该文件。该方法是同步的，因此生成的 ID 是唯一的。对于问题 ID 文件名，存在对应的获取和设置方法²。

数据库连接通过三个方法进行管理：

- `void connect()`
- `void disconnect()`
- `boolean isConnected()`

`connect()` 方法使用模型的 `jdbcDriver` 和 `databaseURL` 属性打开到数据库的 JDBC 连接。这些属性从 `web.xml` 部署描述符中指定的上下文参数设置。`disconnect()` 方法关闭连接，而 `isConnected()` 方法提供了一种测试数据库连接是否存在的方法。

> 2 文件名存储为实例变量，但使用它的方法是一个类方法。这就是为什么它必须作为参数传递。原因是该模型可以从 Web 或命令行测试外壳运行。在这两种情况下，文件的位置可能不同。

> **注意**
> `connect()` 和 `disconnect()` 方法提供了连接到数据库的能力，但它们不选择何时以及如何执行此操作。事实上，模型本身没有处理此任务的逻辑。正如你将看到的，这是控制器对象的任务。

### 19.4.1 客户方法

```java
/**
 * 返回与当前客户 ID 对应的客户对象
 * @exception SQLException 如果发生数据库错误
 */
public Customer getCustomer()
    throws SQLException
{
    // 验证连接是否存在

    if (!isConnected())
        throw new SQLException("No connection");

    // 验证是否存在当前客户 ID

    if (customerID == null)
        throw new SQLException("No customer ID");

    PreparedStatement pstmt = null;
    ResultSet rs = null;
    Customer customer = null;

    try {

        // 准备查询 SQL

        pstmt = con.prepareStatement
        ("select * from customers where customerID = ?");
        pstmt.setString(1, customerID);

        // 执行查询

        rs = pstmt.executeQuery();
        if (rs.next())
            customer = Customer.load(rs);
    }
    finally {
        if (rs != null)
            rs.close();
        if (pstmt != null)
            pstmt.close();
    }

    // 返回客户

    return customer;
}

/**
* 返回当前客户搜索结果
*/
public List getCustomers()
{
    return customers;
}

/**
* 使用指定的客户搜索参数查询数据库以查找匹配的客户。
* 创建客户对象列表。
* @param searchArgument 搜索参数
* @exception SQLException 如果发生数据库错误
*/
public void customerSearch(String searchArgument)
    throws SQLException
{
    // 验证连接是否存在以及搜索参数是否已指定

    if (!isConnected())
        throw new SQLException("No connection");

    PreparedStatement pstmt = null;
    ResultSet rs = null;
    customers = null;

    try {

        // 准备查询 SQL

        pstmt = con.prepareStatement(
            "select *"
            + " from customers"
            + " where name like ?"
            + " order by name"
        );
        searchArgument = searchArgument.trim();
        searchArgument = "%" + searchArgument + "%";
        pstmt.setString(1, searchArgument);

        // 执行查询并将结果复制到 List

        rs = pstmt.executeQuery();
        customers = new LinkedList();
        while (rs.next()) {
            customers.add(Customer.load(rs));
        }
    }
    finally {
        if (rs != null)
            rs.close();
        if (pstmt != null)
            pstmt.close();
    }
}

/**
 * 返回 customerID。
 */
public String getCustomerID()
{
    return customerID;
}

/**
 * 设置 customerID。
 * @param customerID customerID。
 */
public void setCustomerID(String customerID)
{
    this.customerID = customerID;
}
```

存在当前客户 ID 的获取和设置方法，以及一个用于从数据库中检索具有该 ID 的 `Customer` 对象的方法。`getCustomer()` 方法说明了 `Customer.load()` 方法从结果集中提取 `Customer` 对象的功能。`customerSearch()` 方法从 `customer` 表中选择 `name` 字段匹配指定搜索参数的 `Customer` 对象。生成的 `java.util.List` 存储为实例变量，可以通过 `getCustomers()` 检索。

### 19.4.2 产品方法

```java
/**
* 返回与当前产品 ID 对应的产品对象
* @exception SQLException 如果发生数据库错误
*/
public Product getProduct()
    throws SQLException
{
    // 验证连接是否存在

    if (!isConnected())
        throw new SQLException("No connection");

    // 验证当前产品 ID 是否存在

    if (productID == null)
        throw new SQLException("No product ID");

    PreparedStatement pstmt = null;
    ResultSet rs = null;
    Product product = null;

    try {
```

598 JSP：完整参考

// 准备查询 SQL
pstmt = con.prepareStatement("select * from products where productID = ?");
pstmt.setString(1, productID);

// 执行查询
rs = pstmt.executeQuery();
if (rs.next())
    product = Product.load(rs);
}
finally {
    if (rs != null)
        rs.close();
    if (pstmt != null)
        pstmt.close();
}

// 返回产品
return product;
}

/**
 * 返回当前产品搜索结果
 */
public List getProducts()
{
    return products;
}

/**
 * 使用指定的产品搜索参数查询数据库中的匹配产品。
 * 创建产品对象列表。
 * @param searchArgument 搜索参数
 * @exception SQLException 如果发生数据库错误
 */
public void productSearch(String searchArgument) throws SQLException
{
    // 验证连接是否存在，以及搜索参数是否已指定
    if (!isConnected())
        throw new SQLException("No connection");

    PreparedStatement pstmt = null;
    ResultSet rs = null;
    products = null;

    try {
        // 准备查询 SQL
        pstmt = con.prepareStatement(
            "select *"
            + " from products"
            + " where name like ?"
            + " order by name"
        );
        searchArgument = searchArgument.trim();
        searchArgument = "%" + searchArgument + "%";
        pstmt.setString(1, searchArgument);

        // 执行查询并将结果复制到列表
        rs = pstmt.executeQuery();
        products = new LinkedList();
        while (rs.next())
            products.add(Product.load(rs));
    }
    finally {
        if (rs != null)
            rs.close();
        if (pstmt != null)
            pstmt.close();
    }
}

/**
 * 返回产品 ID。
 */
public String getProductID()
{
    return productID;
}

/**
 * 设置产品 ID。
 * @param productID 产品 ID。
 */
public void setProductID(String productID)
{
    this.productID = productID;
}

与客户方法完全对应，产品方法用于获取和设置当前产品 ID，检索相应的 `Product` 对象，选择与搜索字符串匹配的产品，并检索所选结果。

// ====================================
//     客户/产品方法
// ====================================

/**
 * 返回当前客户的 CustomerProduct 对象列表。
 * @exception SQLException 如果发生数据库错误
 */
public List getCustomerProducts() throws SQLException
{
    // 验证连接是否存在
    if (!isConnected())
        throw new SQLException("No connection");

    // 验证当前客户 ID 是否存在
    if (customerID == null)
        throw new SQLException("No customer ID");

    PreparedStatement pstmt = null;
    ResultSet rs = null;
    List list = null;

    try {
        // 准备查询 SQL
        pstmt = con.prepareStatement(
            "select *"
            + " from custprod"
            + " where customerID = ?"
            + " order by datePurchased desc"
        );
        pstmt.setString(1, customerID);

        // 执行查询并填充列表
        rs = pstmt.executeQuery();
        list = new LinkedList();
        while (rs.next())
            list.add(CustomerProduct.load(rs));
    }
    finally {
        if (rs != null)
            rs.close();
        if (pstmt != null)
            pstmt.close();
    }

    // 返回列表
    return list;
}

当选择了客户 ID 并将其存储在模型中后，就可以在 `custprod` 表中搜索该客户购买的产品。得到的 `CustomerProblem` 对象列表按购买日期降序排序并返回给调用者。

// ========================================
//   员工方法
// ========================================

/**
 * 返回与指定员工 ID 对应的员工对象
 * @param employeeID 员工 ID
 * @exception SQLException 如果发生数据库错误
 */
public Employee getEmployee(String employeeID) throws SQLException
{
    // 验证连接是否存在
    if (!isConnected())
        throw new SQLException("No connection");

    PreparedStatement pstmt = null;
    ResultSet rs = null;
    Employee employee = null;

    try {
        // 准备查询 SQL
        pstmt = con.prepareStatement("select * from employees where employeeID = ?");
        pstmt.setString(1, employeeID);

        // 执行查询
        rs = pstmt.executeQuery();
        if (rs.next())
            employee = Employee.load(rs);
    }
    finally {
        if (rs != null)
            rs.close();
        if (pstmt != null)
            pstmt.close();
    }

    // 返回员工
    return employee;
}

可以通过调用 `getEmployee()` 并传入员工 ID 来从数据库中检索员工对象。这主要用于显示 `Product` 对象中三个支持 ID 的员工姓名。

// ========================================
//     问题方法
// ========================================

/**
 * 工厂方法，用于创建新的问题记录并将其添加到数据库
 */
public void newProblem() throws SQLException
{
    if (getCustomerID() == null)
        throw new SQLException("No customer ID");

    if (getProductID() == null)
        throw new SQLException("No product ID");

    Problem problem = new Problem();

    String fileName = getProblemIDFile();
    problemID = assignProblemID(fileName);
    problem.setProblemID(problemID);
    problem.setDescription("");
    problem.setSeverity(2);
    problem.setDateReported(new java.util.Date());
    problem.setCustomerID(getCustomerID());
    problem.setProductID(getProductID());

    // 添加到数据库
    PreparedStatement pstmt = null;
    try {
        pstmt = con.prepareStatement("insert into problems values(?, ?, ?, ?, ?, ?, ?)");
        pstmt.setString(1, problemID);
        pstmt.setString(2, problem.getDescription());
        pstmt.setInt(3, problem.getSeverity());
        pstmt.setTimestamp(4, Util.toTimestamp(problem.getDateReported()));
        pstmt.setNull(5, Types.TIMESTAMP);
        pstmt.setString(6, problem.getCustomerID());
        pstmt.setString(7, problem.getProductID());
        pstmt.executeUpdate();
    }
    finally {
        if (pstmt != null)
            pstmt.close();
    }
}

/**
 * 更新数据库中的问题记录
 * @param problem 问题对象
 * @exception SQLException 如果发生数据库错误
 */
public void updateProblem(Problem problem) throws SQLException
{
    // 验证连接是否存在
    if (!isConnected())
        throw new SQLException("No connection");

    PreparedStatement pstmt = null;
    try {
        // 准备查询 SQL
        pstmt = con.prepareStatement(
            " update problems"
            + "     set"
            + "         description = ?,"
            + "         severity = ?,"
            + "         dateResolved = ?"
            + "     where problemID = ?"
        );
        pstmt.setString(1, problem.getDescription());
        pstmt.setInt(2, problem.getSeverity());
        if (problem.getDateResolved() != null)
            pstmt.setTimestamp(3, Util.toTimestamp(problem.getDateResolved()));
        pstmt.setString(4, problem.getProblemID());

        // 执行更新
        pstmt.executeUpdate();
    }
    finally {
        if (pstmt != null)
            pstmt.close();
    }
}

# 第19章：案例研究：产品支持中心

/**
 * 返回与当前问题 ID 对应的问题对象
 * @exception SQLException 如果发生数据库错误
 */
public Problem getProblem() throws SQLException
{
    // 验证连接是否存在
    if (!isConnected())
        throw new SQLException("No connection");

    // 验证当前问题 ID 是否存在
    if (problemID == null)
        throw new SQLException("No problem ID");

    PreparedStatement pstmt = null;
    ResultSet rs = null;
    Problem problem = null;

    try {
        // 准备查询 SQL
        pstmt = con.prepareStatement("select * from problems where problemID = ?");
        pstmt.setString(1, problemID);
    }
}



**606 JSP：完全参考手册**

```java
// 执行查询
rs = pstmt.executeQuery();
if (rs.next())
    problem = Problem.load(rs);
}
finally {
    if (rs != null)
        rs.close();
    if (pstmt != null)
        pstmt.close();
}

// 返回问题
return problem;
}

/**
 * 返回当前问题搜索结果
 */
public List getProblems()
{
    return problems;
}

/**
 * 使用指定的客户ID查询
 * 数据库中该客户的问题。
 * 创建问题对象列表。
 * @exception SQLException 如果发生数据库错误
 */
public void customerProblemsSearch(String customerID)
    throws SQLException
{
    // 验证连接是否存在
    if (!isConnected())
        throw new SQLException("无连接");

    PreparedStatement pstmt = null;
    ResultSet rs = null;
    problems = null;

    try {

        // 准备查询SQL

        pstmt = con.prepareStatement
            ("select * from problems where customerID = ?");
        pstmt.setString(1, customerID);

        // 执行查询并将结果
        // 复制到列表

        rs = pstmt.executeQuery();
        problems = new LinkedList();
        while (rs.next())
            problems.add(Problem.load(rs));
    }
    finally {
        if (rs != null)
            rs.close();
        if (pstmt != null)
            pstmt.close();
    }
}

/**
 * 使用指定的产品ID查询
 * 数据库中该产品的问题。
 * 创建问题对象列表。
 * @exception SQLException 如果发生数据库错误
 */
public void productProblemsSearch(String productID)
    throws SQLException
{
    // 验证连接是否存在

    if (!isConnected())
        throw new SQLException("无连接");

    PreparedStatement pstmt = null;
    ResultSet rs = null;
    problems = null;

    try {
        // 准备查询SQL

        pstmt = con.prepareStatement
        ("select * from problems where productID = ?");
        pstmt.setString(1, productID);

        // 执行查询并将结果
        // 复制到列表

        rs = pstmt.executeQuery();
        problems = new LinkedList();
        while (rs.next())
            problems.add(Problem.load(rs));
    }
    finally {
        if (rs != null)
            rs.close();
        if (pstmt != null)
            pstmt.close();
    }
}

/**
 * 返回problemID。
 */
public String getProblemID()
{
    return problemID;
}

/**
 * 设置problemID。
 * @param problemID the problemID.
 */
public void setProblemID(String problemID)
{
    this.problemID = problemID;
}
```

newProblem() 方法为当前客户和产品创建一个新的问题记录，初始化它，并将其添加到数据库中，而 updateProblem() 方法则修改它。提供了按客户和产品检索问题的方法，它们将结果存储在 java.util.List 中，可以通过 getProblems() 检索。

## ProblemLog 方法

```java
/**
 * 添加新的问题日志条目
 * @param log 问题日志对象
 * @exception SQLException 如果发生数据库错误
 */
public void addProblemLog(ProblemLog log)
    throws SQLException
{
    // 验证连接是否存在

    if (!isConnected())
        throw new SQLException("无连接");

    PreparedStatement pstmt = null;

    try {

        // 准备插入SQL

        pstmt = con.prepareStatement
        ("insert into problog values(?, ?, ?, ?)");
        pstmt.setString(1, log.getProblemID());
        pstmt.setTimestamp(2, Util.toTimestamp(log.getLogTime()));
        pstmt.setString(3, log.getEventID());
        pstmt.setString(4, log.getComments());

        // 执行语句

        pstmt.executeUpdate();
    }
    finally {
        if (pstmt != null)
            pstmt.close();
    }
}

/**
 * 使用指定的问题ID查询
 * 数据库中该问题的问题日志条目。
 * 创建问题日志对象列表。
 * @exception SQLException 如果发生数据库错误
 */
public void problemLogSearch(String problemID)
    throws SQLException
{
    // 验证连接是否存在

    if (!isConnected())
        throw new SQLException("无连接");

    PreparedStatement pstmt = null;
    ResultSet rs = null;
    problemLogs = null;

    try {

        // 准备查询SQL

        pstmt = con.prepareStatement
            ("select * from problog where problemID = ?");
        pstmt.setString(1, problemID);

        // 执行查询并将结果
        // 复制到列表

        rs = pstmt.executeQuery();
        problemLogs = new LinkedList();
        while (rs.next())
            problemLogs.add(ProblemLog.load(rs));
    }
    finally {
        if (rs != null)
            rs.close();
        if (pstmt != null)
            pstmt.close();
    }
}

/**
 * 返回problemLogs。
 */
public List getProblemLogs()
{
    return problemLogs;
}
```

最后，该模型提供了为问题添加日志条目、搜索现有问题的日志条目以及检索搜索结果的方法。

## WebModel 类

如果你仔细阅读了 Model 类，会注意到它不包含任何 Web 感知方法。这是有意为之。出于测试目的，你希望能够使用简单的命令行视图运行模型，因此不希望在模型的任何地方使用 javax.servlet 或 javax.servlet.http 类。但是，当从 Web 运行时，你希望模型能利用更多关于其环境的知识。因此，你使用了一个具有这种感知能力的 Model 子类。

WebModel 实现了三个方法：

- `void init(ServletContext context)` 从 web.xml 部署描述符中提取应用程序参数。这些参数包括 JDBC 驱动程序名称、数据库 URL 以及包含下一个可用产品 ID 的文件名。使用 web.xml 来指定这些值使得为不同环境配置产品支持应用程序变得容易。
- `void valueBound(HttpSessionBindingEvent event)` 是构成 HttpSessionBindingListener 接口的两个方法之一。在这种情况下，这个方法中无需执行任何操作，但为了满足编译器要求，必须实现它。
- `void valueUnbound(HttpSessionBindingEvent event)` 是另一个 HttpSessionBindingListener 方法。这是你在会话超时或失效时执行关闭数据库连接这一重要功能的地方。

WebModel 类如下所示：

```java
package com.lyricnote.support.model;

import javax.servlet.*;
import javax.servlet.http.*;
import java.sql.SQLException;

/**
 * Model 的特定于 HTTP 的子类。实现会话绑定和
 * 解绑。允许在会话超时或失效时断开数据库连接。
 */
public class WebModel
    extends Model
    implements HttpSessionBindingListener
{
    /**
     * 初始化数据库连接
     */
    public void init(ServletContext context)
        throws ServletException
    {
        // 从 web.xml 中的应用程序范围值
        // 设置模型的 JDBC 驱动程序属性

        String jdbcDriver =
            context.getInitParameter("jdbcDriver");
        if (jdbcDriver == null)
            throw new ServletException
                ("未指定 jdbcDriver 属性");
        setJdbcDriver(jdbcDriver);

        // 对数据库URL执行同样操作

        String databaseURL =
            context.getInitParameter("databaseURL");
        if (databaseURL == null)
            throw new ServletException
                ("未指定 databaseURL 属性");
        setDatabaseURL(databaseURL);

        // 以及问题 ID 分配文件

        String problemIDFile =
            context.getInitParameter("problemIDFile");
        if (problemIDFile == null)
            throw new ServletException
```



("未指定problemIDFile属性");
    setProblemIDFile(problemIDFile);

    // 连接到数据库

    try {
        connect();
    }
    catch (SQLException e) {
        throw new ServletException(e.getMessage());
    }
}

/**
 * 当模型绑定到会话时调用
 */
public void valueBound(HttpSessionBindingEvent event)
{
}

/**
 * 当模型从会话中移除时调用
 */
public void valueUnbound(HttpSessionBindingEvent event)
{
    disconnect();
}
}

## 工具类

应用程序对象类中的最后一个类是 `Util`，这是一个提供各种辅助方法的实用工具类。这些方法包括：

- `dateFormat()` 将Date对象转换为格式化的日期字符串
- `dateTimeFormat()` 将Date对象转换为格式化的日期和时间字符串
- `toTimestamp()` 将Date对象转换为 `java.sql.Timestamp`，以便可以在 `PreparedStatement.setTimestamp()` 方法中使用。
- `quote()` 如果字符串包含嵌入的逗号，则用引号将其括起来。这被 `Customer`、`Product` 和其他业务对象类中的 `toString()` 方法使用，以使值对于逗号分隔值格式是安全的。
- `isClosingEvent()` 如果指定的事件ID表示问题已关闭，则返回 `true`。

以下是Util类的代码清单：

```java
package com.lyricnote.support.model;

import java.text.*;
import java.sql.Timestamp;
import java.util.*;

/**
 * 模型包中使用的实用工具方法
 */
public class Util
{
    private static final SimpleDateFormat DATE_FORMAT =
        new SimpleDateFormat("yyyy-MM-dd");

    private static final SimpleDateFormat DATE_TIME_FORMAT =
        new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");

    /**
     * 使用默认的JDBC格式格式化日期
     */
    public static String dateFormat(Date d)
    {
        return d == null ? "" : DATE_FORMAT.format(d);
    }

    /**
     * 使用默认的JDBC格式格式化时间戳
     */
    public static String dateTimeFormat(Date d)
    {
        return d == null ? "" : DATE_TIME_FORMAT.format(d);
    }

    /**
     * 将java.util.Date转换为java.sql.Timestamp
     */
    public static Timestamp toTimestamp(Date d)
    {
        return (d == null)
            ? null
            : new Timestamp(d.getTime());
    }

    /**
     * 如果字符串包含逗号，则用引号将其括起来。
     * @param s 字符串
     */
    public static String quote(String s)
    {
        if (s != null) {
            if (s.indexOf(",") > -1) {
                StringBuffer sb = new StringBuffer();
                sb.append('"');
                sb.append(s);
                sb.append('"');
                s = sb.toString();
            }
        }
        return s;
    }

    /**
     * 如果指定的事件ID表示“关闭”操作，则返回true
     * @param eventID 事件ID
     */
    public static final boolean isClosingEvent(String eventID)
    {
        return (
            eventID.equals("CNB") ||
            eventID.equals("CCP") ||
            eventID.equals("CFX"));
    }
}
```

# 测试框架

MVC架构的一大优势在于每个组件都可以独立进行测试。在开发过程中，能够对模型进行单元测试尤其有用，并且可以随着方法的添加和修改来测试其API。在本节中，你将看到一个承担此角色的命令行Shell。

## Shell类

test.Shell类是一个独立的Java应用程序，它充当com.lyricnote.support.model.Model的控制器和视图。就像Unix Shell或Windows命令提示符一样，Shell类会提示输入命令、执行它们并显示结果。这些命令的语法是简单的调用模型上方法的Java语法，以及一些用于列出可用方法、显示帮助文本和类似控制功能的命令。Shell提供了一种简单的方法来测试模型的每个部分，而无需在Web环境中引入GUI的额外复杂性。与Model类一样，Shell类代码相当长，因此让我们分部分进行讨论。

```java
package test;

import com.lyricnote.support.model.*;
import java.beans.*;
import java.io.*;
import java.lang.reflect.*;
import java.sql.*;
import java.util.*;

/**
 * 一个用于测试产品支持应用程序模型的交互式Shell。
 */
public class Shell
{
    private static String PROMPT = "SHELL> ";
    private Model model;
    private InputStream stream;
    private boolean interactive;

    // ============================================
    //       类方法
    // ============================================

    /**
     * 主方法
     */
    public static void main(String[] args)
        throws Exception
    {
        Shell shell = new Shell(new Model());
        shell.run();
    }

    /**
     * 显示此shell的帮助文本
     */
    protected static void help()
    {
        String[] text = {
            "",
            "通过名称调用方法，",
            "或使用以下任意命令：",
            "",
            "quit         -  退出shell",
            "help         -  显示此帮助文本",
            "methods      -  显示模型方法列表",
            "include <filename> - 执行包含的文件",
            "",
        };
        for (int i = 0; i < text.length; i++)
            System.out.println(text[i]);
    }

    /**
     * 从方法调用中提取带引号的字符串参数值
     */
    protected static String getArgument(String line)
    {
        String arg = null;
        int p = line.indexOf("(\"");
        if (p != -1) {
            p += 2;
            int q = line.indexOf("\")", p);
            if (q != -1) {
                arg = line.substring(p, q);
            }
        }
        return arg;
    }

    // ==========================================
    //    构造方法
    // ==========================================

    /**
     * 创建一个新的Shell，输入来自System.in
     * @param model 要使用的模型
     */
    public Shell(Model model)
    {
        this(model, System.in);
    }

    /**
     * 创建一个新的Shell，输入来自指定的输入流
     * @param model 要使用的模型
     * @param stream 输入流
     */
    public Shell(Model model, InputStream stream)
    {
        this.model = model;
        this.stream = stream;
        this.interactive = (stream == System.in);
    }
}
```

Shell使用一个简单的main()方法来创建模型和shell的实例，然后调用该shell的run()方法。命令输入的源最初是System.in，但如你所见，它也可以是一组存储在文件中并通过include命令处理的命令。

```java
    // =========================================
    //    主读取/执行循环
    // =========================================

    /**
     * 运行shell
     */
    public void run() throws Exception
    {
        // 在输入流上打开一个行读取器

        BufferedReader in =
            new BufferedReader(
                new InputStreamReader(stream));

        // 读取并执行每一行

        while (true) {

            if (interactive)
                System.out.print(PROMPT);

            String line = in.readLine();
            if (line == null)
                break;

            // 解析并执行命令

            try {
                if (line.equals("quit"))
                    break;
                else if (line.startsWith("get"))
                    doGet(line);
                else if (line.startsWith("set"))
                    doSet(line);
                else if (line.startsWith("customerSearch"))
                    customerSearch(line);
                else if (line.startsWith("productSearch"))
                    productSearch(line);
                else if (line.startsWith("productProblemsSearch"))
                    productProblemsSearch(line);
                else if (line.startsWith("customerProblemsSearch"))
                    customerProblemsSearch(line);
                else if (line.startsWith("problemLogSearch"))
                    problemLogSearch(line);
                else if (line.startsWith("help"))
                    help();
                else if (line.startsWith("methods"))
                    methods();
                else if (line.startsWith("inc"))
                    include(line);
                else if (line.startsWith("is"))
                    doGet(line);
                else if (line.startsWith("connect"))
```



## 第19章：案例研究：产品支持中心

`run()` 方法在输入流上打开一个字符行读取器，并开始提示和执行命令。解析器是一个简单的 if 语句列表，用于检查特定的方法名称并调用执行它们的包装方法。对于以 `get`、`is` 或 `set` 开头的命令，Shell 使用反射在模型中查找相应的 getter 或 setter 方法并调用它们。如果遇到任何错误，它们会被写入 `System.out`。以下是该类的其余部分，包含可以从主循环调用的方法（按字母顺序列出）：

```java
/**
 * 调用客户问题搜索方法
 */
protected void customerProblemsSearch(String line)
    throws Exception
{
    String arg = getArguments(line);
    model.customerProblemsSearch(arg);
}

/**
 * 调用客户搜索方法
 */
protected void customerSearch(String line)
    throws SQLException
{
    String arg = getArguments(line);
    model.customerSearch(arg);
}

/**
 * 调用连接命令
 */
protected void doConnect()
{
    try {
        System.out.println("Connecting...");
        model.connect();
        System.out.println("Connected");
    }
    catch (SQLException e) {
        System.out.println(e.getMessage());
    }
}

/**
 * 调用断开连接命令
 */
protected void doDisconnect()
{
    System.out.println("Disconnecting...");
    model.disconnect();
    System.out.println("Disconnected");
}

/**
 * 执行 "get" 方法
 */
protected void doGet(String line) throws Exception
{
    if (!interactive)
        System.out.println(line);

    // 获取读方法名称
    int p = line.indexOf("(");
    if (p == -1)
        p = line.length();
    String readMethodName = line.substring(0, p).trim();

    // 查找读方法以查看
    // 是否找到此方法
    BeanInfo bi =
        Introspector.getBeanInfo(model.getClass());

    PropertyDescriptor[] pds =
        bi.getPropertyDescriptors();

    for (int i = 0; i < pds.length; i++) {
        PropertyDescriptor pd = pds[i];
        Method method = pd.getReadMethod();
        if (method != null) {
            String name = method.getName();
            if (name.equals(readMethodName)) {
                // 此方法是此属性的读方法。
                // 调用它并打印结果
                Object[] args = {};
                Object result = method.invoke(model, args);
                System.out.println(result);
                return;
            }
        }
    }
    throw new IllegalArgumentException
        ("No " + readMethodName + " method found");
}

/**
 * 调用 newProblem 方法
 */
protected void doNewProblem() throws Exception
{
    model.newProblem();
    System.out.println(model.getProblemID());
}

/**
 * 执行 "set" 方法
 */
protected void doSet(String line) throws Exception
{
    if (!interactive)
        System.out.println(line);

    // 行应如下所示：
    //
    //    setSearchArgument("value")

    int p = line.indexOf("(");
    if (p == -1)
        throw new IllegalArgumentException
            ("No open parenthesis found");

    int q = line.indexOf(")", p);
    if (q == -1)
        throw new IllegalArgumentException
            ("No close parenthesis found");

    String writeMethodName = line.substring(0, p);
    String argument = line.substring(p+1, q).trim();

    // 参数必须是带引号的字符串
    if (!(argument.startsWith("\"") &&
          argument.endsWith("\"")))
        throw new IllegalArgumentException
            ("Argument must be a quoted string");

    // 去掉引号
    argument = argument.substring(1, argument.length()-1);

    // 查找 set 方法并执行它
    BeanInfo bi = Introspector.getBeanInfo(model.getClass());
    PropertyDescriptor[] pds = bi.getPropertyDescriptors();

    for (int i = 0; i < pds.length; i++) {
        PropertyDescriptor pd = pds[i];
        Method method = pd.getWriteMethod();
        if (method != null) {
            String name = method.getName();
            if (name.equals(writeMethodName)) {
                // 此方法是此属性的写方法
                Object[] args = { argument };
                Object result = method.invoke(model, args);
                return;
            }
        }
    }

    throw new IllegalArgumentException
        ("No " + writeMethodName + " method found");
}

/**
 * 为 include 语句中指定的文件运行子 shell。
 * @param line "include <path>/file" 语句
 */
protected void include(String line) throws Exception
{
    if (!interactive)
        System.out.println(line);

    try {
        // 获取要包含的文件的名称
        StringTokenizer st = new StringTokenizer(line);
        st.nextToken();
        if (!st.hasMoreTokens())
            throw new IllegalArgumentException
                ("No file name specified for include");
        String fileName = st.nextToken();

        // 验证文件是否存在
        File file = new File(fileName);
        if (!file.exists())
            throw new IllegalArgumentException
                (fileName + " not found");

        // 运行子 shell
        System.out.println("Including " + fileName);
        new Shell(this.model, new FileInputStream(file)).run();
        System.out.println("Done including " + fileName);
    }
    catch (IllegalArgumentException e) {
        System.out.println(e.getMessage());
    }
    catch (IOException e) {
        System.out.println(e.getMessage());
    }
}

/**
 * 显示模型中可用的公共方法
 */
protected void methods()
{
    // 获取声明的方法列表
    Class cls = Model.class;
    Method[] methods = cls.getDeclaredMethods();
    System.out.println(methods.length + " methods:");

    // 打印列表
    for (int i = 0; i < methods.length; i++) {
        Method method = methods[i];
        String name = method.getName();
        Class[] parameterTypes = method.getParameterTypes();
        StringBuffer sb = new StringBuffer();
        sb.append(name);
        sb.append("(");
        for (int j = 0; j < parameterTypes.length; j++) {
            Class parmClass = parameterTypes[j];
            if (j > 0)
                sb.append(",");
            sb.append(parmClass.getName());
        }
        sb.append(")");
        String s = sb.toString();
        System.out.println("    " + s);
    }
}

/**
 * 调用 problemLogSearch 方法
 */
protected void problemLogSearch(String line)
    throws Exception
{
    String id = getArgument(line);
    model.problemLogSearch(id);
}

/**
 * 调用 productProblemsSearch 方法
 */
protected void productProblemsSearch(String line)
    throws Exception
{
    String id = getArgument(line);
    model.productProblemsSearch(id);
}

/**
 * 调用 productSearch 方法
 */
protected void productSearch(String line) throws Exception
{
    String arg = getArgument(line);
    model.productSearch(arg);
}
}
```

为了了解 shell 的实用程度，让我们看看它的实际运行情况。当你调用 `Shell` 类时，它的 `main()` 方法会创建一个 `Shell` 实例并传给它一个 `Model` 的新实例。如果你输入 `help` 命令，你会看到以下帮助文本：

```
P:\classes\test>java -classpath .. test.Shell
SHELL> help

按名称调用方法，或使用以下任何命令：

quit        - 退出 shell
help        - 显示此帮助文本
methods     - 显示模型方法列表
include <filename> - 执行包含的文件

SHELL>
```

首先，让我们看看有哪些 Model 方法可以调用。输入 `methods` 命令可以看到：

```
SHELL> methods
33 methods:
    connect()
    customerProblemsSearch(java.lang.String)
    customerSearch(java.lang.String)
    disconnect()
    getProblemID()
    newProblem()
    productProblemsSearch(java.lang.String)
    productSearch(java.lang.String)
    addProblemLog(com.lyricnote.support.model.ProblemLog)
    assignProblemID(java.lang.String)
    getCustomer()
    getCustomerID()
    getCustomerProducts()
    getCustomers()
    getDatabaseURL()
    getEmployee(java.lang.String)
    getJdbcDriver()
    getProblem()
    getProblemIDFile()
    getProblemLogs()
    getProblems()
    getProduct()
    getProductID()
    getProducts()
    isConnected()
```



## 第十九章：案例研究：产品支持中心

`problemLogSearch(java.lang.String)`
`setCustomerID(java.lang.String)`
`setDatabaseURL(java.lang.String)`
`setJdbcDriver(java.lang.String)`
`setProblemID(java.lang.String)`
`setProblemIDFile(java.lang.String)`
`setProductID(java.lang.String)`
`updateProblem(com.lyricnote.support.model.Problem)`
`SHELL>`

这些信息是如何出现的？查看实现 `methods` 命令的 `Shell` 方法，你会发现它对 `Model` 类调用了 `getDeclaredMethods()` 方法，然后打印结果数组。这显示了可以从 shell 内部调用的所有方法列表。

在开发过程中，当你向模型添加新方法时，会看到它们自动添加到此列表中。在 `Shell` 类中，你只需在 `run()` 方法中添加一个 `if` 语句和一个简单地调用模型方法并打印结果的子程序。正如你稍后将看到的，对于属性 getter 和 setter 方法，你甚至不需要这样做。

回到 shell 会话。你知道没有数据库连接就做不了什么，所以让我们调用报告连接是否建立的模型方法：

```
SHELL> isConnected();
false
SHELL>
```

当 shell 看到以 `is` 或 `get` 开头的命令时，它将其解释为对模型属性访问器方法之一的调用。shell 在其 `doGet()` 方法中处理所有此类解释。`doGet()` 使用 JavaBeans 自省从 `Model` 类获取 getter 方法列表。然后，它将命令行中的方法名称与 getter 方法的名称进行比较以查找匹配项。当 shell 找到匹配的方法时，它调用该方法并返回结果。

setter 方法使用类似的方法。任何以 `set` 开头的命令都会被分派到 `doSet(String line)` 方法，该方法从命令行中提取参数，进行相同的自省以找到相应的 `set` 方法，并使用命令行参数调用该方法。

这提供了一种自然的方式来获取和设置模型属性。当你调用 shell 的 `isConnected()` 方法时，它将调用传递给模型的 `isConnected()` 方法，该方法报告没有发生连接。

要创建连接，你知道模型需要一个 JDBC 驱动程序名称和一个数据库 URL。设置这些属性，然后调用 `connect()` 方法：

```
SHELL> setJdbcDriver("org.enhydra.instantdb.jdbc.idbDriver");
SHELL> setDatabaseURL("jdbc:idb:D:/jspcr/Chap19/database/db.prp");
SHELL> connect();
Connecting...
Connected
SHELL> isConnected();
true
SHELL>
```

这一次，`isConnected()` 方法表示连接可用。如果你现在只是测试数据库例程，你应该调用 `disconnect()`，然后使用 `quit` 命令：

```
SHELL> disconnect();
Disconnecting...
Disconnected
SHELL> quit
```

测试一遍又一遍地进行，输入一长串命令可能很乏味。为此，shell 提供了一个 `include` 命令。这允许从文件读取 shell 命令并在子 shell 中执行。此功能是递归的，因此包含的模块本身可以包含其他模块。

一个立即有用的包含模块是执行数据库连接的模块，因为这几乎在所有测试中都会使用。此模块包含你刚刚键入的执行连接的三个命令：

```
setJdbcDriver("org.enhydra.instantdb.jdbc.idbDriver");
setDatabaseURL("jdbc:idb:D:/jspcr/Chap19/database/db.prp");
connect();
```

现在你可以启动一个 shell 并简单地调用这组外部命令：

```
P:\classes\test>java -classpath .. test.Shell
SHELL> include connect.inc
setJdbcDriver("org.enhydra.instantdb.jdbc.idbDriver");
setDatabaseURL("jdbc:idb:D:/jspcr/Chap19/database/db.prp");
Connecting...
Connected
SHELL> isConnected();
true
```

请注意，包含模块的内容在读取时会回显到控制台。

建立连接后，你可以继续测试模型的任何部分，复制 GUI 应用程序将采取的一系列步骤，并查看结果是否符合预期。让我们尝试搜索 ScoreWriter 产品并深入查看其问题报告：

```
SHELL> productSearch("Score");
SHELL> getProducts();
[023500,ScoreWriter,0040,0140,0070]
SHELL> productProblemsSearch("023500");
SHELL> getProblems();
[G0000179,Can't get triplets to work,3,2001-01-14 18:40:39,
 2001-01-14 18:42:53,WAGNER01,023500]
SHELL> problemLogSearch("G0000179");
SHELL> getProblemLogs();
[
 G0000179,2001-01-14 18:41:09,RPS,They just don't work!,
 G0000179,2001-01-14 18:42:20,COM,Told customer to try F5,
 G0000179,2001-01-14 18:42:53,CCP,That did it]

SHELL> quit
Disconnecting...
Disconnected
P:\classes\test>
```

调用 `productSearch()` 方法，然后调用 `getProducts()`，你可以看到与搜索参数匹配的产品列表（在这种情况下，是一个包含一个元素的列表）。该对象由一个逗号分隔值的字符串表示，列出了产品 ID、其名称，以及产品支持人员、首席开发人员和首席测试人员的员工 ID。然后，`productProblemsSearch()` 方法找到为 ScoreWriter 报告的问题列表（在这种情况下，也只有一个元素的列表）。最后，`problemLogSearch()` 和 `getProblemLogs()` 方法获取所选问题的日志条目。³

## 使用模型

这完成了模型组件的开发。在开发的早期阶段，你需要同时编写 `Model` 和 `Shell` 类，以便可以独立测试模型的每个部分。当发现错误时，你可以返回到 shell 来重现它们，而无需启动和停止 Web 服务器或在 servlet 日志中搜索调试条目。这为应用程序的其余部分提供了一个更可靠的基础。

> ³ 列出的结果已稍作重新格式化以适应行宽。

当然，设计模型的方法不止一种。你不必使用像 `Model` 类这样的应用容器；你可以直接在 `HttpSession` 中以 JavaBeans 的形式处理业务对象。然而，你在本节中看到的是一个可行的设计，它适应了各种应用需求，而不会在视图和控制器中产生不必要的复杂性。

## 视图类

模型可以附加到一个独立的 Java 应用程序。然而，产品支持系统至少由四种角色的用户访问：呼叫中心代理、产品支持专家、开发人员和测试人员。此外，管理层可能希望衡量质量统计数据，例如问题在队列中等待的平均时间、解决一个客户回电所需的平均次数，以及特定产品未解决的缺陷数量。因此，最佳的系统操作环境可能是公司的内网，表示层由 JSP 页面组成。在本节中，你将了解如何将 JSP 页面用作附加模型的视图。

系统有三个通用入口点：

- **按客户**：呼叫中心代理在与客户通话时，首先通过按客户名称对 `customer` 表进行字母搜索来查找客户 ID。从匹配列表中选择客户后，代理会看到客户的详细信息，包括该客户购买的产品以及客户报告的问题历史。从那里，呼叫中心代理可以输入新的问题报告或提供现有问题的状态。
- **按产品**：产品支持人员、开发人员和测试人员都被分配给特定的产品，而不是客户。因此，他们查看系统的初始视图是按产品划分的。他们可以使用 `product` 表的字母搜索按名称查找产品，然后从那里查看未解决问题的列表。
- **按问题**：系统的任何用户可能已经知道分配给特定缺陷的问题 ID。如果他们需要更新问题记录，可以使用提示输入特定问题 ID 的表单。

在这三种情况下，应用程序最终都会显示特定问题的详细视图。从那里，用户可以更新问题描述和严重程度，将问题路由到另一个部门，或关闭问题。最后的 JSP 视图是确认屏幕，显示已应用的操作。

图 19-3 图示了此应用程序流程。每个矩形框代表一个特定的 JSP 页面。圆圈代表控制器操作，你稍后会了解到。现在，请记住，控制器操作是导致模型更改并显示下一个视图的操作。从 JSP 视图到控制器操作的箭头标有用户对视图采取的操作类型：从列表中选择、输入搜索参数或单击提交按钮。



# 支持页面

所有JSP视图页面都有两段通用的代码段。为了避免在每个JSP文件中重复这些代码，你可以将它们存储在单独的文本文件中，并通过`<%@ include %>`指令引入。

**InitModel.jsp** 每个JSP视图页面都需要将模型声明为一个会话 Bean，并确保数据库连接可用。这个通用功能是通过让视图页面包含以下代码来实现的：

```
<%-- Define and initialize the model --%>

<jsp:useBean
    id="model"
    scope="session"
    class="com.lyricnote.support.model.WebModel">
    <% model.init(application); %>
</jsp:useBean>

<%-- Provide an alias for the controller servlet --%>

<%
    String BASEURL = request.getContextPath();
    String CONTROLLER = BASEURL + "/servlet/controller";
%>
```

`initModel.jsp` 中的这段代码完成了三件事：

- 声明了一个名为`model`、具有会话作用域的JavaBean，并用一个`com.lyricnote.support.model.WebModel`对象进行初始化。
- 调用模型的`init()`方法，从`web.xml`中提取应用程序变量并建立一个会话感知的数据库连接。该方法仅在模型首次绑定到会话时调用一次。
- 初始化指定应用程序基础URL和控制器 Servlet 名称的常量。这些常量在视图的其他地方用于URL和表单action属性。

> 为什么使用 include 指令而不是 `<jsp:include>`？因为被包含的代码段定义并使用了需要对包含模块和被包含模块都通用的常量。

**Banner.jsp** 为了在所有JSP视图页面中保持统一的外观和风格，使用了标准页眉。这个页眉存储在名为 Banner.jsp 的文件中，包含一个HTML表格，其中包含公司Logo和标准导航链接。

```
<TABLE BORDER=0 CELLSPACING=3 CELLPADDING=3 WIDTH=500>
<TR>
    <TD><IMG SRC="<%= BASEURL %>/images/logo.jpg"></TD>
</TR>
<TR>
<TD CLASS="menucell" ALIGN="RIGHT">
    <A CLASS="menuitem"
        HREF="<%= BASEURL %>/Problems.jsp">问题</A>

    <SPAN CLASS="menuitem">|</SPAN>

    <A CLASS="menuitem"
        HREF="<%= BASEURL %>/Products.jsp">产品</A>

    <SPAN CLASS="menuitem">|</SPAN>

    <A CLASS="menuitem"
        HREF="<%= BASEURL %>/Customers.jsp">客户</A>
</TR>
</TABLE>
```

InitModel.jsp 和 Banner.jsp 都不设计为由用户直接调用。为防止这种情况，它们被存储在 /WEB-INF 文件夹中。这使得它们对应用程序本身可见，但对Web上的用户不可见。

**ErrorPage.jsp** 最后一个支持模块是错误页面，如下所列：

```
<%@ page session="false" %>
<%@ page import="java.io.PrintWriter" %>
<%@ page isErrorPage="true" %>

<HTML>
<HEAD>
<TITLE>错误页面</TITLE>
<LINK REL="stylesheet" HREF="style.css">
</HEAD>
<BODY>
<H3>错误</H3>
发生了以下错误：

<PRE>
<%
    exception.printStackTrace(new PrintWriter(out));
%>
</PRE>
</BODY>
</HTML>
```

ErrorPage.jsp 几乎只是显示任何未捕获异常的堆栈跟踪。这在系统开发期间很有用，但在生产环境中可能应该替换为更用户友好的方式。

# JSP 视图页面

以图19-3为路线图，让我们来看九个单独的JSP视图页面：

- Customers.jsp 提示输入客户搜索参数
- CustomersList.jsp 客户搜索结果的选择列表
- Customer.jsp 单个客户记录的详细视图
- Problem.jsp 单个问题记录的详细视图
- Confirm.jsp 问题更新后显示的确认屏幕
- Products.jsp 提示输入产品搜索参数
- ProductsList.jsp 产品搜索结果的选择列表
- ProductProblems.jsp 产品的问题选择列表
- Problems.jsp 提示输入产品ID

Customers.jsp 呼叫中心坐席的初始入口点通常是客户搜索视图，如下所列：

```
<%@ page session="true" %>
<%@ page errorPage="/ErrorPage.jsp" %>
<%@ page import="com.lyricnote.support.model.*" %>

<%@ include file="/WEB-INF/InitModel.jsp" %>

<HTML>
<HEAD>
<TITLE>客户搜索</TITLE>
<LINK REL="stylesheet" HREF="<%= BASEURL %>/style.css">
</HEAD>
<BODY>
<%@ include file="/WEB-INF/Banner.jsp" %>

<H3>客户搜索</H3>
<FORM
    METHOD="POST"
    ACTION="<%= CONTROLLER %>/Customers/Search">
<B>客户姓名</B>:
<INPUT TYPE="TEXT" NAME="customerSearchArgument" SIZE="20">
<INPUT TYPE="SUBMIT" VALUE="搜索">
</FORM>

</BODY>
</HTML>
```

包含模型初始化和页眉代码后，此JSP页面使用HTML表单提示输入客户姓名搜索字符串。例如，如果呼叫中心坐席正在与一位名为 Eleanor Wagner 的客户通话，坐席可以搜索包含字母 W 的姓名，如图19-4所示。当坐席点击搜索按钮时，表单随后被提交到执行搜索的 Servlet（本章稍后在控制器类部分讨论）。

![](img/7a2f73369bb140583c7288b73456addb_662_0.png)

**图19-4. 客户搜索页面**

**CustomersList.jsp** 按客户姓名搜索的结果存储在模型中的 java.util.List 中。CustomerList.jsp 页面提取该列表并显示它，其中客户ID列是超链接。JSP源代码如下：

```
<%@ page session="true" %>
<%@ page errorPage="/ErrorPage.jsp" %>
<%@ page import="java.util.*" %>
<%@ page import="com.lyricnote.support.model.*" %>

<%@ include file="/WEB-INF/InitModel.jsp" %>

<HTML>
<HEAD>
<TITLE>客户列表</TITLE>
<LINK REL="stylesheet" HREF="<%= BASEURL %>/style.css">
</HEAD>
<BODY>

<%@ include file="/WEB-INF/Banner.jsp" %>

<H3>客户列表</H3>
<TABLE BORDER=0 CELLSPACING=5 CELLPADDING=0>
    <TR>
        <TH ALIGN=LEFT>客户ID</TH>
        <TH ALIGN=LEFT>客户姓名</TH>
    </TR>

<%
    List list = model.getCustomers();
    if (list != null) {
        Iterator it = list.iterator();
        while (it.hasNext()) {
            Customer customer = (Customer) it.next();

            // Get the customer select URL

            String customerID = customer.getCustomerID();
            String selectURL = CONTROLLER +
                "/CustomersList/Select?customerID="
                + customerID;
%>
    <TR>
    <TD><A HREF="<%= selectURL %>"><%= customerID %></A></TD>
    <TD><%= customer.getName() %></TD>
</TR>
<%
    }
%>
</TABLE>

</BODY>
</HTML>
```

包含姓名中含有字母W的客户的列表的网页如图19-5所示。

**Customer.jsp** 从列表中选择 Eleanor Wagner 后，呼叫中心坐席会看到客户详细信息页面，如图19-6所示。此页面有三个部分：

- **左上角** 包含客户ID、姓名和电话号码。
- **右上角** 有客户已购买产品的列表。该列表按采购订单日期降序排列，产品名称是一个用于报告新问题的超链接。

![](img/7a2f73369bb140583c7288b73456addb_664_0.png)

- 底部是客户报告的问题历史记录。在这种情况下，你会看到一个问题，一个已经解决的问题。

产品列表使呼叫中心坐席能够确定 Wagner 女士有权获得支持的产品。

Customer.jsp 的源代码如下：

```
<%@ page session="true" %>
<%@ page errorPage="/ErrorPage.jsp" %>
<%@ page import="java.util.*" %>
<%@ page import="com.lyricnote.support.model.*" %>

<%@ include file="/WEB-INF/InitModel.jsp" %>

<HTML>
<HEAD>
<TITLE>客户详细信息</TITLE>
<LINK REL="stylesheet" HREF="<%= BASEURL %>/style.css">
```

![](img/7a2f73369bb140583c7288b73456addb_665_0.png)



## 第19章：案例研究：产品支持中心

JSP 源码主要由 HTML 构成，仅在脚本小程序和表达式中包含少量 Java 用于与模型交互。当前的 Customer 对象通过模型的 `getCustomer()` 方法检索。这使得 JSP 表达式能够填充客户 ID、姓名和电话字段。对于右侧的产品列表，JSP 调用模型的 `getCustomerProducts()` 方法，该方法返回一个 CustomerProduct 对象列表。模型依次用于获取每个产品的名称和购买日期。页面底部显示的先前客户问题列表也采用了类似的技术。

**Problem.jsp** 瓦格纳女士报告她在使用 ScoreWriter 产品时遇到了问题。当她尝试输入一个 Db 时，软件却替换成了 C#。呼叫中心代理点击 ScoreWriter 超链接，这将打开图 19-7 所示的 JSP 视图页面。

在输入问题描述、严重级别以及客户的评论后，代理点击提交按钮以创建问题记录。

![图 19-7. 问题详情页](img/7a2f73369bb140583c7288b73456addb_669_0.png)

## JSP：完整参考

以下是 Problem.jsp 的源代码：

```
<%@ page session="true" %>
<%@ page errorPage="/ErrorPage.jsp" %>
<%@ page import="java.util.*" %>
<%@ page import="com.lyricnote.support.model.*" %>

<%@ include file="/WEB-INF/InitModel.jsp" %>

<HTML>
<HEAD>
<TITLE>Problem</TITLE>
<LINK REL="stylesheet" HREF="<%= BASEURL %>/style.css">
</HEAD>
<BODY>

<%@ include file="/WEB-INF/Banner.jsp" %>

<%
    // 从模型中检索问题
    
    Problem problem = model.getProblem();
    
    // 获取客户
    
    model.setCustomerID(problem.getCustomerID());
    Customer customer = model.getCustomer();
    
    // 获取产品
    
    model.setProductID(problem.getProductID());
    Product product = model.getProduct();
    
    // 确定严重级别
    
    int severity = problem.getSeverity();
    String checked1 = (severity == 1) ? "CHECKED" : "";
    String checked2 = (severity == 2) ? "CHECKED" : "";
    String checked3 = (severity == 3) ? "CHECKED" : "";
%>

<H3>问题 <%= problem.getProblemID() %></H3>

<FORM METHOD="POST" ACTION="<%= CONTROLLER %>/Problem/Submit">
<INPUT TYPE="HIDDEN" NAME="problemID"
       VALUE="<%= problem.getProblemID() %>">
<TABLE BORDER=0 CELLSPACING=5 CELLPADDING=3>
<TR>
    <TD>描述:</TD>
    <TD>
        <INPUT
            NAME="description"
            TYPE="text"
            VALUE="<%= problem.getDescription() %>"
            SIZE="50"
            >
    </TD>
</TR>
<TR>
    <TD>严重级别:</TD>
    <TD>
        <INPUT
            NAME="severity"
            TYPE="radio"
            VALUE="1"
            <%= checked1 %>
            >高
        <INPUT
            NAME="severity"
            TYPE="radio"
            VALUE="2"
            <%= checked2 %>
            >中
        <INPUT
            NAME="severity"
            TYPE="radio"
            VALUE="3"
            <%= checked3 %>
            >低
    </TD>
</TR>
<TR>
    <TD>客户:</TD>
    <TD><%= customer.getName() %></TD>
</TR>
<TR>
    <TD>产品:</TD>
    <TD><%= product.getName() %></TD>
</TR>
<TR>
    <TD>日期</TD>
    <TD>
        报告日期:
        <%= Util.dateTimeFormat(problem.getDateReported()) %>
        解决日期:
        <%= Util.dateTimeFormat(problem.getDateResolved()) %>
    </TD>
</TR>
<TR>
    <TD>评论:</TD>
    <TD>
    <TEXTAREA NAME="comments" COLS="50" ROWS="4">
    </TEXTAREA>
    </TD>
</TR>
<TR>
    <TD>操作:</TD>
    <TD>
    <SELECT NAME="eventID">
        <OPTION VALUE="COM">评论
        <OPTION VALUE="RPS">转至产品支持
        <OPTION VALUE="RPD">转至开发部门
        <OPTION VALUE="RQA">转至测试部门
        <OPTION VALUE="CNB">关闭 - 非缺陷
        <OPTION VALUE="CCP">关闭 - 客户问题
        <OPTION VALUE="CFX">关闭 - 已修复
    </SELECT>
    <INPUT TYPE="SUBMIT" VALUE="提交">
    </TD>
</TR>
</TABLE>
</FORM>

<%
    // 获取此问题的日志条目

    model.problemLogSearch(problem.getProblemID());
    List problemLogs = model.getProblemLogs();
    if (problemLogs.size() > 0) {
```

### 问题历史记录

<TABLE BORDER="1" CELLPADDING="3" CELLSPACING="0">
<TR>
<TH>时间</TH>
<TH>事件代码</TH>
<TH>评论</TH>
</TR>
<%
    Iterator it = problemLogs.iterator();
    while (it.hasNext()) {
        ProblemLog log = (ProblemLog) it.next();
%>
<TR>
<TD><%= Util.dateTimeFormat(log.getLogTime()) %></TD>
<TD><%= log.getEventID() %></TD>
<TD><%= log.getComments() %></TD>
</TR>
<%
    }
%>
</TABLE>
<%
}
%>

</BODY>
</HTML>
```

同样，JSP 主要由 HTML 组成，包含一些 Java 代码用于访问 Problem 对象及其客户 ID、产品 ID、描述和严重级别。该问题的日志条目列表来自模型的 `problemLogSearch()` 方法。

**Confirm.jsp** 代理提交问题记录后，会生成一个确认页面（见图 19-8），列出分配的问题 ID、描述、严重级别、客户评论以及问题路由。代理将问题 ID 告知电话中的客户，并告知她 ScoreWriter 产品支持团队会回电给她。确认页面的源代码如下：
```
<%@ page session="true" %>
<%@ page errorPage="/ErrorPage.jsp" %>
<%@ page import="com.lyricnote.support.model.*" %>
```



## 第19章：案例研究：产品支持中心 649

![](img/7a2f73369bb140583c7288b73456addb_675_0.png)

图19-8. 确认页面

```jsp
<%@ include file="/WEB-INF/InitModel.jsp" %>

<HTML>
<HEAD>
<TITLE>Confirmation</TITLE>
<LINK REL="stylesheet" HREF="<%= BASEURL %>/style.css">
</HEAD>
<BODY>

<%@ include file="/WEB-INF/Banner.jsp" %>

<H3>Confirmation</H3>
<TABLE BORDER=0 CELLPADDING=3 CELLSPACING=0>
<TR>
    <TD>Problem ID:</TD>
    <TD><%= request.getParameter("problemID") %></TD>
</TR>
<TR>
    <TD>Description:</TD>
    <TD><%= request.getParameter("description") %></TD>
</TR>
<TR>
    <TD>Severity:</TD>
    <TD><%= request.getParameter("severity") %></TD>
</TR>
<TR>
    <TD>Comments:</TD>
    <TD><%= request.getParameter("comments") %></TD>
</TR>
<TR>
    <TD>EventID:</TD>
    <TD><%= request.getParameter("eventID") %></TD>
</TR>
</TABLE>

</BODY>
</HTML>
```

> 对该系统一个有用的改进是，向问题被转交给的员工发送电子邮件通知。第21章将探讨实现此功能的方法。

Products.jsp 其他用户，例如产品支持人员、开发人员或测试人员，可能会通过查找特定产品来启动应用程序。与客户搜索页面一样，这里有一个用于产品搜索的JSP视图页面，如下所列：

```jsp
<%@ page session="true" %>
<%@ page errorPage="/ErrorPage.jsp" %>
<%@ page import="com.lyricnote.support.model.*" %>

<%@ include file="/WEB-INF/InitModel.jsp" %>

<HTML>
<HEAD>
<TITLE>Product Search</TITLE>
<LINK REL="stylesheet" HREF="<%= BASEURL %>/style.css">
</HEAD>
<BODY>

<%@ include file="/WEB-INF/Banner.jsp" %>

<H3>Product Search</H3>
<FORM
    METHOD="POST"
    ACTION="<%= CONTROLLER %>/Products/Search">
    <B>Product name</B>:
    <INPUT TYPE="TEXT" NAME="productSearchArgument" SIZE="20">
    <INPUT TYPE="SUBMIT" VALUE="Search">
</FORM>

</BODY>
</HTML>
```

与客户搜索页面类似，`Products.jsp` 使用HTML表单来提示输入搜索字符串。图19-9展示了一个搜索产品名称中包含字母S的示例。

**ProductsList.jsp** 如图19-10所示，有两个产品名称包含字母S：Music Teacher Studio 和 ScoreWriter。`ProductsList.jsp` 页面显示这两个产品的ID、产品名称以及分配的支持人员姓名。接下来列出 `ProductsList.jsp`。

![](img/7a2f73369bb140583c7288b73456addb_676_0.png)

```jsp
<%@ page session="true" %>
<%@ page errorPage="/ErrorPage.jsp" %>
<%@ page import="java.util.*" %>
<%@ page import="com.lyricnote.support.model.*" %>

<%@ include file="/WEB-INF/InitModel.jsp" %>

<HTML>
<HEAD>
<TITLE>Products List</TITLE>
<LINK REL="stylesheet" HREF="<%= BASEURL %>/style.css">
</HEAD>
<BODY>

<%@ include file="/WEB-INF/Banner.jsp" %>

<H3>Products List</H3>
<TABLE BORDER=0 CELLSPACING=5 CELLPADDING=0>
    <TR>
        <TH ALIGN=LEFT>Product ID</TH>
        <TH ALIGN=LEFT>Product Name</TH>
        <TH ALIGN=LEFT>Support</TH>
        <TH ALIGN=LEFT>Developer</TH>
        <TH ALIGN=LEFT>Tester</TH>
    </TR>

<%
    List list = model.getProducts();
    if (list != null) {
        Iterator it = list.iterator();
        while (it.hasNext()) {
            Product product = (Product) it.next();

            // Get the product select URL

            String productID = product.getProductID();
            String selectURL = CONTROLLER +
                "/ProductsList/Select?productID="
                + productID;

            String productName = product.getName();

            // Get the names of the product support,
            // developer, and tester employees

            String productSupport = product.getProductSupport();
            String productSupportName =
                model.getEmployee(productSupport).getName();

            String developer = product.getDeveloper();
            String developerName =
                model.getEmployee(developer).getName();

            String tester = product.getTester();
            String testerName =
                model.getEmployee(tester).getName();
%>
<TR>
    <TD><A HREF="<%= selectURL %>"><%= productID %></A></TD>
    <TD><%= productName %></TD>
    <TD><%= productSupportName %></TD>
    <TD><%= developerName %></TD>
    <TD><%= testerName %></TD>
</TR>
<%
    }
}
%>
</TABLE>

</BODY>
</HTML>
```

对于 `Product` 对象中的三个员工ID，JSP会显示对应的员工姓名。它从模型的 `getEmployee()` 方法获取 `Employee` 对象，然后调用 `Employee.getName()` 方法来获取姓名。

![](img/7a2f73369bb140583c7288b73456addb_679_0.png)

图19-10. 产品列表页面

**ProductProblems.jsp** 如果选择了 ScoreWriter 链接，则会显示该产品的问题列表，如图19-11所示。

```jsp
<%@ page session="true" %>
<%@ page errorPage="/ErrorPage.jsp" %>
<%@ page import="java.util.*" %>
<%@ page import="com.lyricnote.support.model.*" %>

<%@ include file="/WEB-INF/InitModel.jsp" %>

<HTML>
<HEAD>
<TITLE>Problems by Product</TITLE>
<LINK REL="stylesheet" HREF="<%= BASEURL %>/style.css">
</HEAD>
<BODY>

<%@ include file="/WEB-INF/Banner.jsp" %>

<H3>Problems by Product</H3>
<%
    Product product = model.getProduct();
    String productID = product.getProductID();
    String productName = product.getName();
%>
<B>Product:</B> <%= productID %> - <%= productName %>
<TABLE BORDER=0 CELLSPACING=5 CELLPADDING=0>
    <TR>
        <TH ALIGN=LEFT>Problem ID</TH>
        <TH ALIGN=LEFT>Description</TH>
        <TH ALIGN=LEFT>Date Reported</TH>
        <TH ALIGN=LEFT>Date Resolved</TH>
    </TR>
<%
    List list = model.getProblems();
    if (list != null) {
        Iterator it = list.iterator();
        while (it.hasNext()) {
            Problem problem = (Problem) it.next();

            // Create the problem select URL
            String problemID = problem.getProblemID();
            String selectURL = CONTROLLER +
                "/Problems/Select?problemID="
                + problemID;

            String problemDescription = problem.getDescription();

            // Get the reported and resolution dates
            String dateReported =
                Util.dateFormat(problem.getDateReported());
            String dateResolved =
                Util.dateFormat(problem.getDateResolved());
%>
<TR>
    <TD><A HREF="<%= selectURL %>"><%= problemID %></A></TD>
    <TD><%= problemDescription %></TD>
    <TD><%= dateReported %></TD>
    <TD><%= dateResolved %></TD>
</TR>
<%
    }
}
%>
</TABLE>

</BODY>
</HTML>
```

![](img/7a2f73369bb140583c7288b73456addb_681_0.png)

如 ProductProblems.jsp 的清单所示，可以从模型获取当前的 Product 对象，以及该产品的问题列表。当 ScoreWriter 的产品支持人员 Fred Albright 致电客户以获取更多问题细节时，他通过点击超链接从列表中选择问题编号。然后他会看到一个更新后的问题详情（见图19-12）。他在评论部分输入客户访谈的结果，并提交问题更新。新的确认页面如图19-13所示。

![](img/7a2f73369bb140583c7288b73456addb_682_0.png)

### 图19-12. 更新后的问题详情页面

![](img/7a2f73369bb140583c7288b73456addb_683_0.png)

**Problems.jsp** 如果已知问题ID，用户可以直接选择问题，使用图19-14所示的JSP视图。

![](img/7a2f73369bb140583c7288b73456addb_683_1.png)

`Problems.jsp` 的源代码与客户和产品搜索页面类似：

```jsp
<%@ page session="true" %>
<%@ page errorPage="/ErrorPage.jsp" %>
<%@ page import="com.lyricnote.support.model.*" %>

<%@ include file="/WEB-INF/InitModel.jsp" %>

<HTML>
<HEAD>
<TITLE>Problem Selection</TITLE>
<LINK REL="stylesheet" HREF="<%= BASEURL %>/style.css">
</HEAD>
<BODY>

<%@ include file="/WEB-INF/Banner.jsp" %>

<H3>Problem Selection</H3>
<FORM
    METHOD="POST"
    ACTION="<%= CONTROLLER %>/Problems/Select">
<B>Problem ID</B>: 
<INPUT TYPE="TEXT" NAME="problemID" SIZE="8">
<INPUT TYPE="SUBMIT" VALUE="select">
</FORM>

</BODY>
</HTML>
```

在进一步调查该问题后，Fred Albright 确定这是由于用户输入错误造成的。他输入了一条相关评论（见图19-15）并关闭了该问题。确认页面如图19-16所示。

## 控制器类

最后一个需要开发的组件是控制器，即系统根据用户输入对模型进行操作并选择下一个视图的部分。在产品支持系统中，此功能由一个名为 `ControllerServlet` 的单一servlet执行。

控制器功能可以逐块构建，通过使用小型、定制化的action类来处理每个状态转换，而不是将每个操作硬编码到servlet中。接下来将解释控制器用于委托给action类的机制。



每次调用控制器 Servlet 时，它都需要了解两件事：

- 当前视图是什么？
- 用户在此视图中选择了什么操作？

您可能已经注意到，所有 JSP 视图页面在调用控制器 Servlet 时，URL 中都包含额外的路径信息。此路径信息包含当前视图的名称和一个描述用户所选操作的关键词。例如，从 Customers.jsp 页面，当用户输入搜索字符串并点击搜索按钮时，表单会提交到控制器 Servlet，路径信息为 /Customers/Search。某些视图页面支持多种用户操作。从 Customer.jsp 页面，用户可以点击产品名称报告新问题，也可以选择现有问题进行更新。无论哪种情况，控制器都会获取视图名称和操作关键词，将它们连接起来，并附加单词 Action。结果就是处理状态转换的类的名称。

## Action 基类

以下是抽象 Action 类的代码列表：

```java
package com.lyricnote.support.controller;

import com.lyricnote.support.model.*;
import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;

/**
 * 所有状态转换的基类
 */
public abstract class Action
{
    protected HttpServletRequest request;
    protected HttpServletResponse response;
    protected ServletContext application;
    protected Model model;

    /**
     * 执行操作。子类应覆盖此方法，
     * 并在完成处理时将请求转发到下一个视图组件。
     */
    public abstract void run()
        throws ServletException, IOException;

    /**
     * 设置请求。
     * @param request 请求对象。
     */
    public void setRequest(HttpServletRequest request)
    {
        this.request = request;
    }

    /**
     * 设置响应。
     * @param response 响应对象。
     */
    public void setResponse(HttpServletResponse response)
    {
        this.response = response;
    }

    /**
     * 设置 Servlet 上下文。
     * @param application 应用程序上下文。
     */
    public void setApplication(ServletContext application)
    {
        this.application = application;
    }

    /**
     * 设置模型。
     * @param model 模型对象。
     */
    public void setModel(Model model)
    {
        this.model = model;
    }
}
```

Action 包含了 Servlet 请求和响应、Servlet 上下文以及模型本身的实例变量。除了这些变量的 getter 和 setter 方法外，还有一个名为 run() 的抽象方法。这是各个操作处理器必须实现的唯一方法。run() 方法调用模型方法以实现状态转换，然后创建一个请求分发器并将请求转发到下一个视图。

## 控制器 Servlet

控制器 Servlet 是所有状态转换的驱动器。它在每个会话中维护一个已调用操作类的缓存。当请求发生时，Servlet 会检查会话操作映射，以查看该类的实例是否已经加载。如果没有，它会从路径信息中提取视图名称和操作关键词，将它们连接起来，并在结果后附加 Action，以获取操作类名。然后，它加载该类并创建一个实例，将其存储在会话操作映射中。确保模型已存在后，Servlet 接着在操作对象中设置请求、响应、上下文和模型属性，并调用其 run() 方法。

ControllerServlet 的代码如下所示：

```java
package com.lyricnote.support.controller;

import com.lyricnote.support.model.*;
import java.io.*;
import java.sql.*;
import java.util.*;
import javax.servlet.*;
import javax.servlet.http.*;

/**
 * LyricNote 问题报告系统的
 * 模型-视图-控制器架构中的控制器组件
 */
public class ControllerServlet extends HttpServlet
{
    /**
     * 处理 HTTP GET 请求
     */
    public void doGet(
            HttpServletRequest request,
            HttpServletResponse response)
        throws ServletException, IOException
    {
        doPost(request, response);
    }

    /**
     * 处理 HTTP POST 请求
     */
    public void doPost(
            HttpServletRequest request,
            HttpServletResponse response)
        throws ServletException, IOException
    {
        HttpSession session = request.getSession();
        Map actionMap = (Map) session.getAttribute("actionMap");
        if (actionMap == null) {
            actionMap = new HashMap();
            session.setAttribute("actionMap", actionMap);
        }
        ServletContext context = getServletContext();
        try {

            // 从路径信息中获取状态和事件

            String pathInfo = request.getPathInfo();
            if (pathInfo == null)
                throw new ServletException
                    ("无效的内部状态 - 没有路径信息");

            // 加载处理此状态和事件的操作对象

            Action action = (Action) actionMap.get(pathInfo);
            if (action == null) {

                // 这是 Servlet 第一次看到此操作。
                // 从 pathInfo 获取状态和事件名称。

                StringTokenizer st =
                    new StringTokenizer(pathInfo, "/");

                if (st.countTokens() != 2)
                    throw new ServletException
                    ("无效的内部状态 - 无效的路径信息 ["
                    + pathInfo + "]");

                String state = st.nextToken();
                String event = st.nextToken();

                // 根据状态和事件形成类名

                String className =
                    "com.lyricnote.support.controller."
                    + state + event + "Action";

                // 加载类并创建实例

                try {
                    Class actionClass = Class.forName(className);
                    action = (Action) actionClass.newInstance();
                }
                catch (ClassNotFoundException e) {
                    throw new ServletException
                    ("无法加载类 " + className
                    + ": " + e.getMessage());
                }
                catch (InstantiationException e) {
                    throw new ServletException
                    ("无法创建 " + className
                    + " 的实例: " + e.getMessage());
                }
                catch (IllegalAccessException e) {
                    throw new ServletException
                    (className + ": " + e.getMessage());
                }

                // 将实例缓存到操作映射中

                actionMap.put(pathInfo, action);
            }

            // 确保会话中存在模型。

            Model model = (Model) session.getAttribute("model");
            if (model == null)
                throw new ServletException
                ("在会话中未找到模型");

            // 现在执行操作。操作应在完成时执行
            // RequestDispatcher.forward()

            action.setRequest(request);
            action.setResponse(response);
            action.setApplication(context);
            action.setModel(model);
            action.run();
        }
        catch (ServletException e) {

            // 所有 Servlet 错误均使用 JSP 错误页面

            request.setAttribute("javax.servlet.jsp.jspException", e);
            RequestDispatcher rd =
                context.getRequestDispatcher("/ErrorPage.jsp");

            if (response.isCommitted())
                rd.include(request, response);
            else
                rd.forward(request, response);
        }
    }
}
```

## 操作类

接下来的部分将描述产品支持系统中使用的每个操作类。

回顾图 19-3 可以看到，从一个视图到另一个视图发生了七次状态转换。这些转换对应以下操作类：

- CustomersSearchAction
- CustomersListSelectAction
- CustomersNewProblemAction
- ProductsSearchAction
- ProductsListSelectAction
- ProblemsSelectAction
- ProblemSubmitAction

### CustomersSearchAction 类

此类中的 run() 方法被调用，以从 Customers.jsp 视图接收客户搜索参数，并调用模型中的 customerSearch() 方法。然后，它将请求转发到显示搜索结果的 JSP 视图页面。以下是 CustomersSearchAction 的代码列表：

```java
package com.lyricnote.support.controller;

import java.io.*;
import java.sql.SQLException;
import javax.servlet.*;
import javax.servlet.http.*;

/**
* 在数据库中搜索与客户搜索参数匹配的客户
*/
public class CustomersSearchAction extends Action
{
    /**
    * 执行操作
    */
    public void run() throws ServletException, IOException
    {
        // 执行搜索
    }
}
```



```java
String arg = request.getParameter("customerSearchArgument");
if (arg != null) {
    arg = arg.trim();
    if (!arg.equals("")) {
        try {
            model.customerSearch(arg);
        }
        catch (SQLException e) {
            throw new ServletException(e.getMessage());
        }
    }
}

// 转发到客户列表 JSP

final String next = "/CustomersList.jsp";
RequestDispatcher rd =
    application.getRequestDispatcher(next);
if (rd == null)
    throw new ServletException
    ("Could not find " + next);
rd.forward(request, response);
}
```

## CustomersListSelectAction 类

用户通过点击一个超链接从列表中选择一个客户，该链接指向控制器，其中包含 CustomerList 视图名称和 Select 操作关键字。此外，超链接 URL 中还附加了客户 ID 作为查询字符串。根据这些信息，CustomersListSelectAction 类执行以下操作：

- 从 URL 中提取客户 ID 参数，并将其存储在模型中
- 调用模型的客户问题搜索方法
- 将请求转发到客户详细信息 JSP 视图

以下是该操作类的代码：

```
package com.lyricnote.support.controller;

import java.io.*;
import java.sql.SQLException;
import javax.servlet.*;
import javax.servlet.http.*;

/**
 * 获取此客户的详细信息
 */
public class CustomersListSelectAction extends Action
{
    /**
     * 执行操作
     */
    public void run() throws ServletException, IOException
    {
        // 获取客户 ID 并将其存储在模型中

        String customerID = request.getParameter("customerID");
        if (customerID == null)
            throw new ServletException
                ("No customer ID specified");
        model.setCustomerID(customerID);

        // 获取此客户的问题列表

        try {
            model.customerProblemsSearch(customerID);
        }
        catch (SQLException e) {
            throw new ServletException(e.getMessage());
        }

        // 转发到客户详情 JSP

        final String next = "/Customer.jsp";
        RequestDispatcher rd =
            application.getRequestDispatcher(next);
        if (rd == null)
            throw new ServletException
                ("Could not find " + next);
        rd.forward(request, response);
    }
}
```

668 JSP: 完全参考手册

## CustomerNewProblemAction 类

如前所述，客户视图有两个可能的操作：创建新问题或更新现有问题。新问题操作由以下操作类处理：

```
package com.lyricnote.support.controller;

import java.io.*;
import java.sql.SQLException;
import javax.servlet.*;
import javax.servlet.http.*;

public class CustomerNewProblemAction extends Action
{
    /**
     * 执行操作
     */
    public void run() throws ServletException, IOException
    {
        // 获取客户 ID 和产品 ID

        String customerID = request.getParameter("customerID");
        if (customerID == null)
            throw new ServletException
                ("No customer ID");

        String productID = request.getParameter("productID");
        if (productID == null)
            throw new ServletException
                ("No product ID");

        // 创建新问题

        try {
            model.setCustomerID(customerID);
            model.setProductID(productID);
            model.newProblem();
        }
        catch (SQLException e) {
            throw new ServletException(e.getMessage());
        }

        // 转发到问题详情 JSP
        final String next = "/Problem.jsp";
        RequestDispatcher rd =
            application.getRequestDispatcher(next);
        if (rd == null)
            throw new ServletException
                ("Could not find " + next);
        rd.forward(request, response);
    }
}
```

此操作类执行以下操作：

- 从视图生成的请求中检索 `customerID` 和 `productID` 参数。
- 创建并初始化一个新的 `Problem` 对象。这是通过调用模型中的 `newProblem()` 工厂方法来完成的，该方法会分配一个唯一的问题 ID 并在数据库中写入初始记录。
- 将请求转发到问题详情视图。

## ProductsSearchAction 类

与客户搜索操作类似，产品搜索操作从请求中获取搜索字符串，调用模型中的搜索方法，然后将请求转发到 `ProductsList.jsp` 视图。

```
package com.lyricnote.support.controller;

import java.io.*;
import java.sql.SQLException;
import javax.servlet.*;
import javax.servlet.http.*;

/**
 * 在数据库中搜索与产品搜索参数匹配的产品
 */
public class ProductsSearchAction extends Action
{
    /**
     * 执行操作
     */
    public void run() throws ServletException, IOException
    {
        // 执行搜索

        String arg = request.getParameter("productSearchArgument");
        if (arg != null) {
            arg = arg.trim();
            if (!arg.equals("")) {
                try {
                    model.productSearch(arg);
                }
                catch (SQLException e) {
                    throw new ServletException(e.getMessage());
                }
            }
        }

        // 转发到产品列表 JSP

        final String next = "/ProductsList.jsp";
        RequestDispatcher rd =
            application.getRequestDispatcher(next);
        if (rd == null)
            throw new ServletException
                ("Could not find " + next);
        rd.forward(request, response);
    }
}
```

## ProductsListSelectAction 类

当选择一个产品 ID 时，此操作类将其存储在模型中，并调用模型的产品问题搜索。然后，请求被转发到 `ProductProblems.jsp` 视图，该视图显示结果。

```
package com.lyricnote.support.controller;

import java.io.*;
import java.sql.SQLException;
import javax.servlet.*;
import javax.servlet.http.*;

/**
 * 在数据库中搜索与产品搜索参数匹配的产品
 */
public class ProductsListSelectAction extends Action
{
    /**
     * 执行操作
     */
    public void run() throws ServletException, IOException
    {
        // 获取产品 ID 并将其存储在模型中

        String productID = request.getParameter("productID");
        if (productID == null)
            throw new ServletException
                ("No product ID specified");
        model.setProductID(productID);

        // 获取此产品的问题列表

        try {
            model.productProblemsSearch(productID);
        }
        catch (SQLException e) {
            throw new ServletException(e.getMessage());
        }

        // 转发到产品问题 JSP

        final String next = "/ProductProblems.jsp";
        RequestDispatcher rd =
            application.getRequestDispatcher(next);
        if (rd == null)
            throw new ServletException
                ("Could not find " + next);
        rd.forward(request, response);
    }
}
```

## ProblemsSelectAction 类

所有三个应用程序入口点——客户、产品和问题——都使用一个通用的问题选择操作，如下所列：

```
package com.lyricnote.support.controller;

import java.io.*;
import java.sql.SQLException;
import javax.servlet.*;
import javax.servlet.http.*;

/**
 * 设置当前问题 ID
 */
public class ProblemsSelectAction extends Action
{
    /**
     * 执行操作
     */
    public void run() throws ServletException, IOException
    {
        String problemID = request.getParameter("problemID");
        if (problemID != null) {
            problemID = problemID.trim();
            if (!problemID.equals("")) {
                model.setProblemID(problemID);
            }
        }

        // 转发到问题 JSP

        final String next = "/Problem.jsp";
        RequestDispatcher rd =
            application.getRequestDispatcher(next);
        if (rd == null)
            throw new ServletException
                ("Could not find " + next);
        rd.forward(request, response);
    }
}
```

该操作类只是将问题 ID 存储在模型中，并将请求转发到问题详情页面。



## 第19章：案例研究：产品支持中心

**ProblemSubmitAction类** 最后一个需要的动作类是用于从问题详情页面接收问题更新的类。该类

- 从请求中检索数据输入字段。
- 从模型中检索当前的`Problem`对象并更新其属性。如果事件ID表示应关闭问题，则调用`Problem`对象的`close()`方法。
- 更新问题的数据库记录。
- 添加一条问题日志条目。
- 将请求转发到下一个视图——确认页面。

```java
package com.lyricnote.support.controller;

import com.lyricnote.support.model.*;
import java.io.*;
import java.sql.SQLException;
import javax.servlet.*;
import javax.servlet.http.*;

/**
 * Submits a problem update
 */
public class ProblemSubmitAction extends Action
{
    /**
     * Executes the action
     */
    public void run() throws ServletException, IOException
    {
        // Get the parameters
        
        String problemID = request.getParameter("problemID");
        String description = request.getParameter("description");
        String severity = request.getParameter("severity");
        String comments = request.getParameter("comments");
        String eventID = request.getParameter("eventID");

        try {

            // Get the problem object from the model

            model.setProblemID(problemID);
            Problem problem = model.getProblem();

            // Update the problem object

            problem.setDescription(description);
            problem.setSeverity(Integer.parseInt(severity));
            if (Util.isClosingEvent(eventID))
                problem.close();
            model.updateProblem(problem);

            // Add a problem log record

            ProblemLog log = new ProblemLog();
            log.setProblemID(problemID);
            log.setLogTime(new java.util.Date());
            log.setEventID(eventID);
            log.setComments(comments);
            model.addProblemLog(log);
        }
        catch (SQLException e) {
            throw new ServletException(e.getMessage());
        }

        // Forward to confirmation JSP

        final String next = "/Confirm.jsp";
        RequestDispatcher rd =
            application.getRequestDispatcher(next);
        if (rd == null)
            throw new ServletException
            ("Could not find " + next);
        rd.forward(request, response);
    }
}
```

## 总结

本章汇集了本书中讨论的元素，构建了一个基于Web的产品支持中心管理系统。该系统支持以下流程：

- 有问题的客户拨打免费电话与呼叫中心客服人员通话。
- 客服人员验证客户是否有权获得特定产品的支持，输入问题报告，将确认号提供给客户，并将问题转给产品支持部门。
- 产品支持部门致电客户以确定是代码问题还是客户问题。如果问题被证实是代码问题且当前没有可用的修复方案，则将其转给开发部门。
- 负责的开发人员分析问题。如果问题不是缺陷，开发人员会将问题重新转给产品支持部门以通知客户。如果问题是缺陷，开发人员会编写修复代码并进行单元测试，然后将问题转给质量保证部门。
- 质量保证部门执行集成测试。如果修复需要更多工作，问题会被重新转回开发部门。否则，问题将被发送到产品支持部门，在那里将修复方案转发给客户，并关闭问题。

支持该系统所需的数据模型由关系数据库表组成，这些表代表客户、产品、客户/产品对、员工、问题报告和问题日志条目。

所采用的系统架构称为模型-视图-控制器（MVC）。它由三个组件组成：

- **模型**：应用程序的内部工作机制，包括数据库访问和业务逻辑。没有可视化代码——可以通过简单的命令行驱动程序操作。
- **视图**：从模型检索数据并显示给用户进行交互的表示层。
- **控制器**：接受用户输入并操作模型以改变其状态并呈现下一个视图的组件。

最终的系统通过划分代码来提供可以隔离测试的组件，从而将复杂性降至最低。这产生了一个健壮、功能齐全且易于扩展的应用程序。

## 第四部分：JSP与其他Web组件

JavaServer页面不仅仅是Web应用程序的表示层；它们还可以充当其他应用程序的客户端或服务器。接下来的两章将讨论JavaServer页面使用的更大背景——它们如何与Java应用程序、小程序、Perl脚本、邮件服务器和其他服务器端代理进行通信。

# 第20章：与其他客户端通信

Web浏览器是最常见的JSP客户端，但它们并非唯一的选择。随着越来越多的应用程序实现Web化，网络资源成为各类系统中的重要组成部分。互联网可以作为通信链路，通过它可以在不规定呈现方式的情况下传递原始数据。例如，最新的货币汇率可以用于批处理计算。交互式旅行预订可以成为高管信息系统的一部分。当前的天气状况、新闻头条和股价可以嵌入到其他应用程序的小信息窗口中——甚至可能嵌入到消费电子产品中。

这是可能的，因为任何可以使用HTTP协议的程序都可以充当JSP客户端。使用`java.net`包中的基本类，应用程序可以发出HTTP请求并读取结果，就像它们只是文件内容一样。更重要的是，文件内容是动态的，可以由请求参数控制。

在本章中，你将了解三种非浏览器JSP客户端的开发过程：

- 一个Java应用程序
- 一个Java小程序
- 一个Perl脚本

每个示例都包含一个JSP服务器和一个可以利用它的客户端。但首先，让我们检查一下基本技术。

## URL连接

成为服务器的关键在于表现为一个输入流。Java类库提供了三个类来实现这一点：

- `java.net.URL`
- `java.net.URLConnection`
- `java.net.HttpURLConnection`

## URL类

统一资源定位符（URL）是网络上可用对象的唯一地址，也是必须用于操作该对象的协议的指示。¹ 这些协议包括`ftp`、`http`、`gopher`、`mailto`、`news`以及在专门应用中使用的其他协议。本章中我们考虑的URL使用*超文本传输协议（HTTP）*。

¹ 完整的URL规范在RFC 1738中，可以在 http://www.freesoft.org/CIE/RFC/1738/index.htm 找到。

一个HTTP URL由五部分组成：

```
<scheme>://<host>[:<port>]/<path>[?<query string>]
```

方案是`http`（用于未加密传输）或`https`（用于使用加密技术（如*安全套接字层（SSL）*）的传输）。主机部分是网络主机的完全限定域名，可能表示为点分十进制IP地址。端口号是可选的，如果未指定则默认为80。路径是主机HTTP服务器文档空间中的一个地址，通常组织为目录树。URL还可以包含在查询字符串中编码的请求参数。

`java.net.URL`类是URL的面向对象包装器。它提供了从字符串构建URL以及访问前面描述的各个部分的方法。此外，`java.net.URL`类有两个重要的方法，允许访问URL所指向资源的内容，并在某些情况下修改它们。这些方法列在表20-1中。

在许多情况下，从远程网络资源读取数据就像这样简单：

```java
URL url = new URL("http://servername/path/filename");
InputStream in = url.openStream();
int c;
while ((c = in.read()) != -1) {
    // ... do something with this byte
}
```

| 方法 | 描述 |
| :--- | :--- |
| `public URLConnection openConnection()` | 与URL所表示的远程对象建立连接。 |
| `public final InputStream openStream()` | 打开一个URLConnection并创建一个InputStream来读取其内容。这是一个便捷方法，调用`openConnection().getInputStream()`。 |



## URLConnection 类

使上述功能成为可能的基础类是 `java.net.URLConnection`。这是一个抽象类，其子类表示程序与远程网络资源之间的连接。使用 `URLConnection` 涉及四个步骤：

1.  通过调用 URL 的 `openConnection()` 方法来创建 `URLConnection` 对象。
2.  为手头的特定任务配置连接。这可能包括指明连接是用于输入、输出还是两者兼用，以及设置请求属性以指示内容类型、长度和其他头部信息。
3.  建立连接，这通常是隐式发生的（尽管也可以使用 `connect()` 方法来完成）。
4.  远程资源变得可访问。连接可以提供资源内容以及随资源一起发送的任何响应头部。

一些最常用的方法列在表 20-2 中。

| 方法 | 描述 |
| :--- | :--- |
| `public void setRequestProperty(String key, String value)` | 为连接设置一个通用的请求属性，例如一个 HTTP 头部。示例可以是键为 `Content-Length`，其值为表示请求数据部分字节数的整数。 |
| `public OutputStream getOutputStream()` | 返回一个用于向连接写入数据的输出流，例如在 HTTP POST 请求中的表单参数。 |
| `public InputStream getInputStream()` | 返回一个用于从连接读取数据的输入流。出于性能原因，调用此方法的程序通常将结果包装在某种缓冲流中。 |

表 20-2。java.net.URLConnection 中的一些有用方法

## HttpURLConnection 类

URLConnection 是一个抽象的、与协议无关的类。因此，它没有公共构造函数。它只能通过调用 URL 的 `openConnection()` 方法来创建。此调用返回的实际对象是一个处理该 URL 协议的特定协议子类。在本章的示例中，这个子类是 `java.net.HttpURLConnection`。

嗯，几乎是。HttpURLConnection 本身也是抽象的。Java 虚拟机的供应商提供了一个实际的实现类。你可以通过调用 `openConnection()` 返回的对象的 `getClass()` 方法来查看那个类是什么：

```java
import java.io.*;
import java.net.*;

public class ShowConnectionClass
{
    public static void main(String[] args)
        throws IOException
    {
        URL url = new URL("http://www.ibm.com");
        URLConnection con = url.openConnection();
        Class conClass = con.getClass();
        System.out.println
            ("Connection class is " + conClass.getName());
    }
}
```

在 Sun JVM 上，该程序的输出是：

```
Connection class is sun.net.www.protocol.http.HttpURLConnection
```

除了 URLConnection 提供的功能外，HttpURLConnection 还提供了三项额外的能力：

- 一种指定请求方法的方式
- 直接访问 HTTP 响应码
- 一组为 HTTP 响应码提供助记名称的常量

表 20-3 描述了几个相关的方法。在接下来的几节中，你将看到如何使 URL 连接能够像查看可编程文件一样查看 JSP 页面。

| 方法 | 描述 |
| :--- | :--- |
| `public int getResponseCode()` | 从响应的第一行中提取 HTTP 响应码。例如，如果响应行是 `HTTP/1.0 404 Not found`，则此方法返回 404。 |
| `public String getResponseMessage()` | 返回响应码之后的响应行其余部分。例如，如果响应行是 `HTTP/1.0 404 Not found`，则此方法返回 `Not found`。 |
| `public static void setFollowRedirects(boolean set)` | 如果设置为 `true`，则当响应码为 301（永久重定向）或 302（临时重定向）时，会自动生成另一个请求发送到转发地址。 |
| `public void setRequestMethod(String method)` | 指定要使用的 HTTP 请求方法：`GET`、`POST`、`HEAD`、`OPTIONS`、`PUT`、`DELETE` 或 `TRACE`。 |

**表 20-3。** *java.net.HttpURLConnection 中的有用方法*

## Java 应用程序作为客户端

我们假设的互联网音乐公司 LyricNote.com，与其他在线零售商一起参与由一家折扣产品采购服务管理的价格报价系统。客户可以向该采购服务查询特定乐器的报价，然后采购服务会搜索其参与供应商的网站以寻找最佳价格。每个供应商都按照采购服务规定的标准格式返回一份 XML 文档格式的报价。

### JSP 价格报价服务器

由于每次的价格报价请求都不同，LyricNote.com 不能简单地返回一个静态的 XML 文档。相反，它使用一个 JSP 页面根据数据库搜索的结果动态生成 XML。该 JSP 页面（`PriceQuote.jsp`）如下所列：

```jsp
<%@ page session="false" import="java.sql.*,java.text.*" contentType="text/xml" %>
<%
    // Define constants for JDBC driver name and
    // database URL

    String DRIVER = "org.enhydra.instantdb.jdbc.idbDriver";
    String DB_URL = "jdbc:idb:"
        + "D:/lyricnote/WEB-INF/database/products/db.prp";

    // Get the product search argument and desired quantity

    String product = request.getParameter("product");
    if (product == null)
        throw new ServletException("No product specified");

    String qstring = request.getParameter("quantity");
    if (qstring == null)
        throw new ServletException("No quantity specified");

    int quantity = 0;
    try {
        quantity = Integer.parseInt(qstring);
    }
    catch (NumberFormatException e) {
        throw new ServletException("Quantity not numeric");
    }

    // Load the driver

    Class.forName(DRIVER);

    // Create a connection

    Connection con = null;
    try {
        con = DriverManager.getConnection(DB_URL);

        // Create a select statement

        PreparedStatement pstmt = con.prepareStatement
```

```jsp
(
  " select itemcode, price, description"
+ " from products"
+ " where prodtype = 'IN'"
+ " and description like ?"
+ " and onhand >= ?"
);

// Supply values for substitution parameters

pstmt.setString(1, "%" + product + "%");
pstmt.setInt(2, quantity);

// Execute the query

ResultSet rs = pstmt.executeQuery();

// Create the XML

%><?xml version="1.0"?>
<price-quote>
  <supplier>LyricNote.com</supplier>
  <date><%=
    new SimpleDateFormat("yyyy-MM-dd")
    .format(new java.util.Date())
  %></date>
<%
  while (rs.next()) {
    String itemCode    = rs.getString(1);
    double price       = rs.getDouble(2) / 100;
    String description = rs.getString(3);
%>  <item
    code="<%= itemCode %>"
    price="<%= new DecimalFormat("###.00").format(price) %>"
    description="<%= description %>"/>
<%
  }
%></price-quote><%
}
finally {
  if (con != null)
    con.close();
}
%>
```

该 JSP 页面从请求参数中提取产品搜索参数和所需数量，然后打开到 LyricNote 产品数据库的数据库连接并搜索匹配的项目。结果以 XML 形式写入。

奇怪的缩进方案（`%><%` 和 `%></price-quote><%` 中背靠背的分隔符）用于防止换行符或其他多余的空格被写入输出流。本章后面的另一个示例展示了可用于实现此目的的另一种技术。

### 价格报价客户端应用程序

我们只考虑一个简化的客户端 Java 应用程序版本——它说明了如何建立连接，而不是如何处理数据。

```java
import java.io.*;
import java.net.*;

/**
 * 一个作为 JSP 客户端的 Java 应用程序示例。
 */
public class PriceQuoteReader
{
    public static void main(String[] args)
    {
        // Define the supplier URL and the two search arguments.
        // These are hard-coded for the purposes of this example.

        String supplier =
            "http://www.lyricnote.com/PriceQuote.jsp";
        String product = "Clarinet";
        int quantity = 3;

        // Append the search arguments to the URL so that
        // they will be recognized as parameters to an
        // HTTP GET request

        StringBuffer sb = new StringBuffer();
        sb.append(supplier);
        sb.append("?product=");
```



## 688 JSP：权威指南

```
sb.append(URLEncoder.encode(product));
sb.append("&quantity=");
sb.append(URLEncoder.encode(String.valueOf(quantity)));
String supplierURL = sb.toString();

try {
    // 现在创建 URL 实例
    URL url = new URL(supplierURL);
    // 并打开其输入流
    InputStream stream = url.openStream();

    // 读取返回的 XML 的每一行。
    // 本示例仅打印结果；
    // 实际应用会执行更有用的操作
    BufferedReader in =
        new BufferedReader(
            new InputStreamReader(stream));

    while (true) {
        String line = in.readLine();
        if (line == null)
            break;
        System.out.println(line);
    }
    in.close();
} catch (IOException e) {
    e.printStackTrace();
}
}
```

`PriceQuoteReader` 使用硬编码的值作为供应商 URL、产品搜索字符串和请求的数量。它创建一个 URL，将搜索字符串和数量作为请求参数包含在内，然后调用 `URL.openStream()` 来发起连接。接着，它读取并打印生成的 XML 文档，如下所示：

```xml
<?xml version="1.0"?>
<price-quote>
    <supplier>LyricNote.com</supplier>
    <date>2001-01-25</date>
    <item code="001130" price="369.00" description="Wendecker B Flat Clarinet"/>
    <item code="001140" price="522.00" description="Clemens-Altman B Flat Clarinet - Wood"/>
    <item code="001150" price="417.00" description="Gabriel E Flat Clarinet - Wood"/>
    <item code="001160" price="548.00" description="Wendecker B Flat Bass Clarinet"/>
    <item code="001170" price="307.00" description="Clemens-Altman E Flat Clarinet"/>
</price-quote>
```

XML 包含了供应商名称和请求日期，其后是每个匹配产品的元素——在本例中，是至少有三件可供购买的单簧管型号。

## 一个 Java Applet 客户端

购买服务的主应用程序能够实时搜索特定站点。为此，它使用了一个 Java applet。
在继续之前，有必要介绍一些背景知识。*Applet*（小程序）是 Java 技术的第一波浪潮，是将小型交互式 GUI 应用程序嵌入网页的一种方式。它们迅速引起了极大的关注，尽管这项技术当时还不够成熟，不足以支撑其热度。部分问题在于不同的浏览器提供了不同程度的支持，而且这种差异随时间推移而加剧。Sun Microsystems 提出了一个可行的解决方案，即 Java 插件。

## Java 插件

*Plug-in*（插件）是一种特定于浏览器的嵌入式对象，它管理自己的 Java 虚拟机。这意味着它不依赖于浏览器提供的支持程度（如果有的话）。早期版本的插件附带一个 HTML 转换器，用于将 `<APPLET>` 标签转换为特定于浏览器的对应标签 `<OBJECT>`（用于 Microsoft Internet Explorer）和 `<EMBED>`（用于 Netscape Navigator）。

JSP 引入了一种在网页中使用插件的更简单方法，即 `<jsp:plugin>` 动作。当 `<jsp:plugin>` 在 JSP 页面中使用时，在输出的 HTML 文档中，它会被替换为 `<object>` 或 `<embed>` 标签，具体取决于浏览器。此标签的语法相当复杂，如下所示：

```jsp
<jsp:plugin
    type="bean|applet"
    code="<classname>"
    codebase="<codebase>"
    align="<alignment>"
    archive="<archiveList>"
    height="<height>"
    hspace="<hspace>"
    jreversion="<jreversion>"
    name="<componentName>"
    vspace="<vspace>"
    width="<width>"
    nspluginurl="<url>"
    iepluginurl="<url>"
>
    <jsp:params>
        <jsp:param name="<name>" value="<value>"/>
        ...
        <jsp:param name="<name>" value="<value>"/>
    </jsp:params>
    <jsp-fallback>任意文本</jsp-fallback>
</jsp:plugin>
```

JSP 规范通过“如 HTML 规范所定义”来描述大多数属性，以下除外：

-   **type** 可以是 `bean` 或 `applet`。
-   **jreversion** 指示所需的 *Java 运行时环境*（JRE）版本，默认为“1.1”。
-   **nspluginurl** 如果需要，将从中下载 Netscape 版本插件的 URL。
-   **iepluginurl** 如果需要，将从中下载 Internet Explorer 版本插件的 URL。

`<jsp:params>` 部分指定要使用的 applet 参数，而 `<jsp-fallback>` 包含在 applet 无法启动时将显示的文本。
幸运的是，只有少数几个属性是必需的，即 `type`、`code`、`codebase`、`height` 和 `width`。

使用插件运行 applet 的优势在于，它使得拥有一个支持 Java 2 的稳定、可预测的 JVM 成为可能。特别是，这意味着 applet 可以使用 Java 基础类（Swing）来构建其图形用户界面。

## PriceQuoteApplet

这里列出了用于查询报价服务器的 applet 的源代码：

```java
import java.awt.*;
import java.awt.event.*;
import javax.swing.*;
import java.io.*;
import java.net.*;

public class PriceQuoteApplet extends JApplet
{
    private JTextField txtProduct;
    private JTextField txtQuantity;
    private JButton btnPost;
    private JTextArea txtOutput;

    /**
     * 创建 GUI 组件
     */
    public void init()
    {
        Container content = getContentPane();
        content.setLayout(new BorderLayout());
        JPanel pnl;

        // 顶行
        pnl = new JPanel();
        pnl.add(new JLabel("Product:"));
        pnl.add(txtProduct = new JTextField(12));
        pnl.add(new JLabel("Quantity:"));
        pnl.add(txtQuantity = new JTextField(4));
        pnl.add(btnPost = new JButton("POST"));
        content.add(pnl, BorderLayout.NORTH);

        // 结果面板
        pnl = new JPanel();
        pnl.add(txtOutput = new JTextArea(12, 40));
        content.add(pnl, BorderLayout.CENTER);

        // 开始监听按钮点击
        btnPost.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent event)
            {
                try {
                    doPost();
                } catch (IOException e) {
                    txtOutput.setText(e.getMessage());
                }
            }
        });
    }

    /**
     * 发送请求并将 XML 结果
     * 写入输出文本区域
     */
    public void doPost() throws IOException
    {
        // 从 GUI 中提取参数
        String product = txtProduct.getText().trim();
        String quantity = txtQuantity.getText().trim();

        // 使用搜索参数作为请求参数创建 POST 数据
        StringBuffer sb = new StringBuffer();
        sb.append("product=");
        sb.append(URLEncoder.encode(product));
        sb.append("&quantity=");
        sb.append(URLEncoder.encode(String.valueOf(quantity)));
        String postData = sb.toString();

        // 创建用于读取报价的 URL
        URL supplierURL = new URL(getCodeBase(), "PriceQuote.jsp");

        // 打开一个 URLConnection 实例
        HttpURLConnection con = (HttpURLConnection)
            supplierURL.openConnection();

        // 设置读写模式
        con.setDoOutput(true);
        con.setDoInput(true);
        con.setUseCaches(false);

        // 告诉服务器输入流包含 POST 数据并提供其长度
        con.setRequestProperty(
            "Content-type",
            "application/x-www-form-urlencoded");

        con.setRequestProperty(
            "Content-length",
            String.valueOf(postData.length()));

        // 打开连接的输出流并写入 POST 数据
        OutputStream out = con.getOutputStream();
        out.write(postData.getBytes());
        out.flush();

        // 打开输入流并将结果
        // 复制到输出文本区域
        BufferedReader in =
            new BufferedReader(
                new InputStreamReader(
                    con.getInputStream()));

        txtOutput.setText("");

        while (true) {
            String line = in.readLine();
            if (line == null)
                break;
            txtOutput.append(line);
            txtOutput.append("\n");
        }

        // 关闭输出流和输入流
        in.close();
        out.close();
    }
}
```

该 applet 包含两个分别用于输入产品类型和数量的文本字段、一个用于发起搜索的按钮以及一个用于显示结果的文本区域。这不是一本关于 Swing 的书，因此我们不会深入探讨 GUI 的构建细节。值得关注的方法是 `doPost()`，原因有二：

-   它展示了 applet 如何连接到 URL 输入流。
-   它使用了 HTTP POST 方法来实现这一点。

POST 与 GET 的不同之处在于，请求参数是通过请求体提供的，而不是附加到 URL 后面。`doPost()` 使用第 12 章（HTML 表单）中描述的 URL 编码机制，将请求体构建为名称/值对。然后，它打开到 JSP 页面的 `URLConnection`，配置其内容类型和长度，再写入请求体。`doPost()` 读取结果并将其显示在输出文本区域中。

包含该 applet 的 JSP 页面列在下面。图 20-1 显示了相应的输出。



<%@ page session="false" %>
<jsp:plugin
    type="applet"
    code="PriceQuoteApplet.class"
    codebase="."
    width="500"
    height="300"
    jreversion="1.2"
    >
</jsp:plugin>

![](img/7a2f73369bb140583c7288b73456addb_721_0.png)

## 一个 Perl 客户端

由于 JSP 服务器与其客户端之间的通信使用 HTTP，客户端甚至不必用 Java 编写。例如，Perl 是一种广泛使用的脚本语言，尤其常见于 CGI 应用程序、文本处理和系统管理。凭借出色的 socket 支持，Perl 可以轻松访问用 JSP 编写的服务器应用程序。

JSP 能够扩展 Perl 的一个领域是提供更好的数据库支持。因为几乎所有数据库系统都可以通过某种形式的 JDBC 驱动程序访问，并且 Perl 可以从 JSP URL 连接中读取数据，所以 Perl 应用程序可以使用 JSP 作为数据库访问的中间件。

## 通用数据库查询服务器

此处列出的 JSP 页面提供了一种对任何可通过 JDBC 访问的数据库执行 SQL SELECT 查询的方法。它接受一个包含三个参数的 HTTP 请求：

- **DRIVER** JDBC 驱动程序类名
- **URL** JDBC 数据库 URL
- **QUERY** 要执行的 SELECT 语句

结果以制表符分隔值（tab-separated-values）格式写入，第一行为列名。

> **注意** 此 JSP 页面说明了另一种防止 JSP 元素引入的多余空白干扰严格输出格式的技术。这是通过在写入第一行真实文本之前调用 `response.reset()` 来清除输出缓冲区实现的。请注意，`reset()` 也会清除已写入的任何标头和状态码。因此，Servlet 2.3 规范添加了 `resetBuffer()` 方法。

```
<%@ page session="false" %>
<%@ page import="java.io.*" %>
<%@ page import="java.sql.*" %>
<%
    Connection con = null;
    try {

        // Get the driver name and database URL parameters

        String driver = request.getParameter("DRIVER");
        if (driver == null)
            throw new ServletException
                ("No DRIVER parameter specified");

        String url = request.getParameter("URL");
        if (url == null)
            throw new ServletException
                ("No url class name specified");

        // Get the SELECT statement to be executed

        String query = request.getParameter("QUERY");
        if (query == null)
            throw new ServletException
                ("No QUERY parameter specified");

        // Verify that it is a SELECT statement

        query = query.trim();
        if (!query.toUpperCase().startsWith("SELECT"))
            throw new ServletException
                ("Only SELECT statements are valid");

        // Make sure the driver is loaded

        Class.forName(driver);

        // Open the connection

        con = DriverManager.getConnection(url);

        // Compile the query statement. If it is invalid,
        // a SQLException will be thrown.

        PreparedStatement stmt = con.prepareStatement(query);

        // Execute the query

        ResultSet rs = stmt.executeQuery();

        // Reset the response buffer to eliminate
        // any nonsignificant whitespace

        response.reset();

        // Write the column headings

        response.setContentType("text/tab-separated-values");

        ResultSetMetaData rmd = rs.getMetaData();
        int nColumns = rmd.getColumnCount();
        StringBuffer buffer = new StringBuffer();
        for (int i = 0; i < nColumns; i++) {
            int col = i+1;
            if (i > 0)
                buffer.append("\t");
            buffer.append(rmd.getColumnName(col));
        }
        out.println(buffer.toString());

        // Write the data from the result set

        while (rs.next()) {
            buffer = new StringBuffer();
            for (int i = 0; i < nColumns; i++) {
                int col = i+1;
                if (i > 0)
                    buffer.append("\t");
                buffer.append(rs.getString(col));
            }
            out.println(buffer.toString());
        }

        // Done

        rs.close();
        stmt.close();
    }
    finally {
        if (con != null) {
            try {
                con.close();
            }
            catch (SQLException ignore){}
        }
    }
%>
```

## Perl 脚本

Perl 的非官方格言是“不止一种方法可以做到这一点”。既然如此，任何 Perl 脚本都只是完成相同任务的众多可能实现之一。我们用来访问 JSP 数据库服务器的脚本是 `GetBooks.pl`。该脚本打开一个到 LyricNote Web 服务器（端口 80）的 socket，然后发送一个包含三个必需参数（包括要执行的 SQL 查询）的 HTTP GET 请求。

```
#! perl -w

# ==========================================
# Program: GetBooks
#
# Description:
#
#   Sample Perl script that sends a database
#   query to the SQLSelect.jsp
# ==========================================

use strict;
use IO::Socket;

my $hostName = "u25nv";
my $hostPort = "80";

# Open a socket to the host

my $socket = new IO::Socket::INET(
    PeerAddr => $hostName,
    PeerPort => $hostPort,
    Proto    => "tcp"
    );

# Set autoflush on

my $saveSelect = select $socket;
$| = 1;
select $saveSelect;

# Create the command

my $cmd = "";
$cmd .= "DRIVER=" . encode("org.enhydra.instantdb.jdbc.idbDriver");
$cmd .= "&URL=" . encode("jdbc:idb:D:/lyricnote/WEB-INF/database/products/db.prp");
$cmd .= "&QUERY=" . encode(<<EOF);
SELECT itemCode, description
FROM PRODUCTS
WHERE PRODTYPE='BK'
EOF

my $cmdLength = length($cmd);

# Send the HTTP request

print $socket (<<EOF);
POST /jspcr/Chap20/examples/SQLSelect.jsp HTTP/1.0
Content-Type: application/x-www-form-urlencoded
Content-Length: $cmdLength

$cmd
EOF

# Read back the status code

my $line = <$socket>;
my ($httpVersion, $status) = split(/\s+/, $line);
if ($status != 200) {

    # Handle the error ...

}
else {

    # Skip the rest of the headers and display the results.
    # End of headers is signaled by a blank line.

    my $inData = 0;
    while (<$socket>) {
        chomp;

        ($inData == 0) && do {
            $inData = 1 unless (/\S/);
            next;
        };

        ($inData == 1) && do {
            print "$_\n";
            next;
        };
    }
}

# Done

$socket->close();

# Subroutine to URL-encode a parameter string

sub encode {
    my $s = shift;
    $s =~ s/([^A-Za-z0-9 ])/"%" . sprintf("%02X", ord($1))/eg;
    $s =~ s/ /+/g;
    return $s;
}
```

在这个例子中，`GetBooks.pl` 请求用于 LyricNote 产品数据库的 InstantDB 数据库驱动程序，并查询所有音乐相关书籍的商品代码和描述。以下显示了结果：

| 商品代码 | 描述 |
| --- | --- |
| 000030 | Dorothy Wendecker: 纽约的巴托克 |
| 000040 | Conrad Stock: 贝多芬与天气 |
| 000120 | Louis Krouse: 坏沙皇 |
| 000150 | Alice Gabriel: 是萨列里干的吗？ |
| 000160 | John Glass: 斯特拉文斯基与20世纪芭蕾 |
| 000170 | Gray Raphael: 人声 |
| 000200 | Nicholas Thiers: 哦，孩子！双簧管！ |
| 000220 | Douglas Benton: 某种铜管乐器 |
| 000240 | Theresa McDonald: 抒情中提琴 |
| 000270 | Violet Barber: 谁怕十二音序列？ |
| 000280 | Rita Fall: 我的旋律线是什么 |
| 000290 | Mary Wright: 更多的芭蕾舞失误 |
| 000330 | Anna Maria Pontius: 普塞尔狂热 |

## 总结

尽管最常见的 JSP 客户端是 Web 浏览器，但任何能够使用 HTTP 协议的程序都可以充当客户端。本章说明了三种替代客户端：

- 一个请求动态创建的 XML 文档的独立 Java 应用程序
- 一个使用 HTTP POST 访问 JSP 服务器的 Java 小程序
- 一个使用 JSP 作为其数据库服务器的 Perl 脚本

这种 HTTP 通信链路提供的灵活性使得在各种应用程序中集成基于 JSP 的组件成为可能。

![](img/7a2f73369bb140583c7288b73456addb_729_0.png)

# 第 21 章

## 与其他服务器通信

前面的章节演示了 Web 浏览器之外的其他客户端也可以访问 JSP 页面。使用 HTTP 作为通用技术，Java 应用程序、小程序以及用其他语言编写的程序都可以将 JSP 页面用作任何类型系统中的非可视组件。反之亦然——JSP 页面可以充当其他服务器的客户端。在本章中，你将研究其中两种服务器环境以及 JSP 页面如何与它们互操作。

## 服务器端脚本环境

JSP 和 servlet 在互联网上提供动态内容，但许多其他技术也能做到这一点：

- **CGI** *通用网关接口*驱动着数千个交互式网站，通常使用 Perl 脚本访问数据库和其他系统资源。
- **ASP** 微软的*活动服务器页面*是一种广泛使用的服务器环境，允许开发人员将 HTML 和脚本命令混合在一起以提供动态内容。
- **PHP** PHP 是一个开源的跨平台服务器脚本环境，使用嵌入式 HTML 和类似 Perl 的语言。
- **Cold Fusion** Allaire 的 Cold Fusion 是一个服务器端应用环境，使用基于标签的服务器脚本语言（称为 *CFML*）来执行数据库访问和生成 Web 输出。

发现同时使用多种这些技术（或许全部使用）的组织并不罕见。这是因为企业计算资源通常广泛分布，部门或分部的需求决定了不同的解决方案。无论 JSP 或其中任何技术有何优点，在组织上可能难以强制执行统一的应用程序环境。转换遗留应用程序代价高昂。然而，转换它们也可能是不必要的，因为在许多情况下，这些应用程序可以互操作。关键的基础设施再次是 HTTP 协议，它是所有这些环境中使用的通用传输机制。

## 与 HTTP 互操作

出现互操作性需求的一种情况是相关公司的联合活动。一家集团可能由一家母公司拥有，该母公司使用统一的会计系统。子公司可能需要提交预算数据、销售信息和工资数据。并且它们可能需要从母公司下载价格、折扣率和公司费用。这些公司可能没有使用相同的应用程序系统，特别是如果它们是在合并或收购中组合起来的。



## 从远程网络资源读取数据

你可能还记得第20章的内容，`java.net.URL` 和 `java.net.URLConnection` 都提供了读取远程网络资源生成的输入流的方法。进行GET请求的基本技术如下：

```
URL url = new URL("http://servername/path?parm=value");
URLConnection con = url.openConnection();
InputStream in = con.getInputStream();
```

或者，使用 `java.net.URL` 中的一个便捷方法：

```
URL url = new URL("http://servername/path?parm=value");
InputStream in = url.openStream();
```

如果你需要在打开输入流之前进一步配置连接（例如需要发送请求头或使用HTTP POST方法），则首选第一种方法。下文将对此进行说明：

```
import java.io.*;
import java.net.*;
import java.util.*;

public class PostRateRequest
{
    public static void main(String[] args)
        throws Exception
    {
        // Set up the two request parameters
        String postData = "c1=USD&c2=CAD";

        // Open the URL connection for reading and writing
        URL url = new URL(
            "http://u25nv/cgi-bin/currency/GetRate.cgi");
        URLConnection con = url.openConnection();
        con.setDoOutput(true);
        con.setDoInput(true);

        // Set request headers for content type and length
        con.setRequestProperty(
            "Content-type",
            "application/x-www-form-urlencoded");
        con.setRequestProperty(
            "Content-length",
            String.valueOf(postData.length()));

        // Issue the POST request
        OutputStream out = con.getOutputStream();
        out.write(postData.getBytes());
        out.flush();

        // Read the response
        InputStream in = con.getInputStream();
        while (true) {
            int c = in.read();
            if (c == -1)
                break;
            System.out.print((char) c);
        }
        System.out.flush();

        // Done
        in.close();
        out.close();
    }
}
```

LyricNote.com 使用此技术从其母公司的网站读取美元兑加拿大元的汇率。下文列出的 `CatalogSearch.jsp` 以美元和加元列出产品价格。它从上例中使用的货币CGI程序获取汇率，这次是嵌入在其 `jspInit()` 方法中。图21-1展示了结果。

![](img/7a2f73369bb140583c7288b73456addb_733_0.png)

在 `jspInit()` 中，JSP页面使用HTTP GET请求获取母公司提供的USD-CAD汇率。它读取单行结果并将其转换为double类型。稍后，从数据库中读取价格（以整数分表示），并转换为保留两位小数的美元。然后应用汇率计算出等值的加元，结果四舍五入到最接近的五分钱。

```
<%@ page session="false" %>
<%@ page import="java.io.*" %>
<%@ page import="java.net.*" %>
<%@ page import="java.sql.*" %>
<%@ page import="java.text.*" %>
<%!
  private static double EXCHANGE_RATE;

  // Get the US to Canadian dollar exchange rate
  public void jspInit()
  {
    try {
        URL url = new URL(
            "http://u25nv/cgi-bin/currency/GetRate.cgi"
            + "?c1=USD"
            + "&c2=CAD");
        BufferedReader in =
            new BufferedReader(
                new InputStreamReader(
                    url.openStream()));
        String line = in.readLine();
        in.close();
        EXCHANGE_RATE = Double.parseDouble(line);
    }
    catch (IOException e) {
        e.printStackTrace();
    }
  }
%>
<%
    // Get search string
    String search = request.getParameter("search");
    if (search == null)
        search = "";
    search = search.trim();

    // Connect to database
    String DRIVER = "org.enhydra.instantdb.jdbc.idbDriver";
    String DB_URL = "jdbc:idb:" +
        "D:/lyricnote/WEB-INF/database/products/db.prp";

    Class.forName(DRIVER);
    Connection con = null;
    try {
        con = DriverManager.getConnection(DB_URL);

        // Create a query using the search string
        PreparedStatement stmt = con.prepareStatement
            ("select itemcode, price, description"
            + " from products"
            + " where description like ?");
        stmt.setString(1, "%" + search + "%");

        // Run the query and display the results
        ResultSet rs = stmt.executeQuery();
%>
<HTML>
<HEAD>
<TITLE>Catalog Search</TITLE>
</HEAD>
<BODY>
<IMG SRC="images/lyric_note.png">
<HR WIDTH="500" ALIGN="LEFT" COLOR="#005A9C">
<H3>Catalog Search Results</H3>
<FORM>
<INPUT TYPE="TEXT" NAME="search" VALUE="<%= search %>">
<INPUT TYPE="SUBMIT" VALUE="Search Again">
</FORM>
<TABLE BORDER="1" CELLPADDING="5" CELLSPACING="0">
<TR>
<TH>Item</TH>
<TH>Price<BR>(USD)</TH>
<TH>Price<BR>(CAD)</TH>
<TH>Description</TH>
</TR>
<%
NumberFormat fmt = NumberFormat.getCurrencyInstance();
while (rs.next()) {
    String itemCode = rs.getString(1);
    double price = rs.getDouble(2) / 100;
    double price_c =
        ((long)(price * EXCHANGE_RATE * 20 + 0.5)) / 20.0;
    String description = rs.getString(3);
%>
<TR>
<TD><A HREF="productDetail.jsp?itemCode=<%= itemCode %>"
><%= itemCode %></A></TD>
<TD ALIGN="RIGHT"><%= fmt.format(price) %></TD>
<TD ALIGN="RIGHT"><%= fmt.format(price_c) %></TD>
<TD><%= description %></TD>
</TR>
<%
    }
%>
</TABLE>
</BODY>
</HTML>
<%
    }
    finally {
        if (con != null)
            con.close();
    }
%>
```

## 从JSP页面发送邮件

第19章中的产品支持系统案例研究略过一个流程上的难点：当一个问题被转交给支持人员时，该人员如何得知？开发人员和测试员可以阅读其负责产品的当前问题列表，但除非他们恰好在查看，否则无法知道新问题何时出现。当客户正在等待时，通过某种主动进程通知适当的支持人员尤为重要。这种情况非常适合使用电子邮件。

在程序内部通过电子邮件进行通知并不总是个好主意，特别是如果使用了硬编码的地址，这些地址最终会过时。然而，在这种情况下，支持人员的身份及其电子邮件地址是从产品支持数据库中获取的。因为电子邮件是一种熟悉的机制，并且基础设施已经存在，所以它是解决此问题的好方法。

### 发送邮件的方法

在应用程序内部发送电子邮件有几种选择。本节考虑三种：

-   使用套接字的SMTP
-   `sun.net.smtp.SmtpClient` 类
-   JavaMail API

### SMTP

最简单的方法是通过TCP/IP套接字使用 *简单邮件传输协议（SMTP）*。SMTP可追溯到1982年，是最古老的互联网协议之一。它使用一组小型文本命令来提供电子邮件参数：

-   HELO：标识发送者域名。
-   MAIL：标识发送者。
-   RCPT：标识接收者。可以使用多个RCPT命令。
-   DATA：表示消息体的开始。直到下一行单独出现的“.”为止的所有内容都属于消息体的一部分。
-   QUIT：终止会话。

此处显示了一个SMTP会话示例（客户端发送的行以 **粗体** 标示）：

```
220 pluto.lyricnote.com ESMTP Sendmail 8.9.3/8.9.3;
  Mon, 29 Jan 2001 06:58:24 -0500 (EST)
HELO lyricnote.com
250 pluto.lyricnote.com Hello dialup.rdu.lyricnote.com
 [209.170.132.190], pleased to meet you
MAIL FROM: phanna@lyricnote.com
250 phanna@lyricnote.com... Sender ok
RCPT TO: phanna@lyricnote.com
250 phanna@lyricnote.com... Recipient ok
DATA
354 Enter mail, end with "." on a line by itself
SUBJECT: Mail Test
This is a test of the mail system
This is only a test
Beeeeeeeeeeeeeeeeeeeeeeep
This concludes the test of the mail system
.
250 UAA07253 Message accepted for delivery
QUIT
221 pluto.lyricnote.com closing connection
```

完整的SMTP协议规范在RFC 821中，可在 http://www.freesoft.org/CIE/RFC/821/index.htm 找到。



SMTP邮件可以通过向邮件主机打开一个`java.net.Socket`并使用其输入输出流来简单发送，如示例所示。这种基于套接字的方法优点在于易于实现，但当添加附件等功能时会变得复杂。因此，很少有应用直接使用此方法。

## sun.net.smtp.SmtpClient 类

另一种选择是使用Sun Microsystems提供的Java运行时环境（JRE）中的`sun.net.smtp.SmtpClient`。该类是对原始SMTP套接字协议的轻量级面向对象封装。前面示例的SmtpClient版本如下所示：

```java
import java.io.*;
import sun.net.*;
import sun.net.smtp.*;

public class MailTest
{
    public static void main(String[] args)
        throws Exception
    {
        SmtpClient client = new SmtpClient("mail.lyricnote.com");

        client.from("phanna@lyricnote.com");
        client.to("phanna@lyricnote.com");

        PrintStream out = client.startMessage();
        out.println("SUBJECT: Mail test");
        out.println("This is a test of the mail system");
        out.println("This is only a test");
        out.println("Beeeeeeeeeeeeeeeeeeeeeeeeeep");
        out.println("This concludes the test of the mail system");
        client.closeServer();
    }
}
```

虽然这种方法比使用套接字略微简单，但它有一个主要缺点：`sun.net.*`类是未文档化的且可能随时更改。Sun允许使用它们（实际上，没有它们Sun JRE将无法工作），但警告它们可能会在未通知的情况下在未来版本中更改或删除。

## JavaMail API

第三个选择是JavaMail API。*JavaMail*是一组API，以抽象方式建模邮件系统的组件——一种适用于POP、SMTP、IMAP和其他邮件协议的可插拔架构。JavaMail适用于JDK 1.1.x及以上版本，是*Java 2 企业版*（J2EE）的必需组件。

> JavaMail包含用于发送和接收邮件的类。此处仅考虑发送方面。JavaMail类和完整文档可从http://java.sun.com/products/javamail下载。

JavaMail的亮点通过以下示例进行说明，与之前示例相同：

```java
import java.util.*;
import javax.mail.*;
import javax.mail.internet.*;

public class JavaMailTest
{
    public static void main(String[] args)
        throws Exception
    {
        // Create a session with the LyricNote mail host

        Properties props = new Properties();
        props.put("mail.host", "mail.lyricnote.com");
        Session mailSession = Session.getInstance(props, null);

        // Create address objects for the sender and receiver

        Address fromUser =
            new InternetAddress("phanna@lyricnote.com");
        Address toUser =
            new InternetAddress("phanna@lyricnote.com");

        // Create the message body

        Message body = new MimeMessage(mailSession);
        body.setFrom(fromUser);
        body.setRecipient(Message.RecipientType.TO, toUser);
        body.setSubject("Mail Test");
        body.setContent(
            "This is a test of the mail system\n"
            + "This is only a test\n"
            + "Beeeeeeeeeeeeeeeeeeeeeeeeeeeeep\n"
            + "This concludes the test of the mail system",
            "text/plain");

        // Send the message

        Transport.send(body);
    }
}
```

通常，使用JavaMail发送邮件涉及七个步骤：

1.  使用`Session.getInstance()`创建到邮件主机的会话。
2.  使用`new InternetAddress()`创建发件人和收件人地址对象。
3.  使用`new MimeMessage(Session session)`创建消息正文对象。
4.  使用`Message`对象的`setFrom()`和`setRecipient()`指定地址。
5.  使用`setSubject()`指定主题。
6.  使用`setContent()`指定消息正文和编码类型。
7.  使用`Transport.send(message)`发送消息。

第一步创建一个新的`Session`对象。`Session`充当到邮件主机的连接。通过调用静态方法`Session.getInstance(Properties props, Authenticator auth)`获取此对象的新实例。提供给此方法的属性必须至少包括邮件主机。如果不需要身份验证，`auth`参数可以为null。

第二步将发件人和收件人表示为`InternetAddress`对象。该类根据RFC 822（"ARPA Internet文本消息格式标准"）建模地址，可从http://www.freesoft.org/CIE/RFC获取。

接下来，使用`new MimeMessage()`创建消息正文对象。此类表示多部分Internet邮件消息，包括其内容和头部。构造函数接受对`Session`对象的引用，以便消息可以关联到邮件主机和其他会话参数。

第四步设置消息正文的`from`和`recipient`属性，分别使用`setFrom(Address fromUser)`和`setRecipient(Message.RecipientType type, Address toUser)`。`type`参数用于区分收件人类型：TO、CC和BCC。

可选的第五步使用消息对象的`setSubject(String subject)`方法设置邮件消息的主题。

第六步使用消息对象的`setContent(Object body, String type)`方法创建实际的消息文本。`body`参数指定文本，`type`指定MIME类型（通常是`text/plain`）。

最后，使用静态`Transport.send(Message message)`方法发送邮件。`Transport`是一个抽象类，其具体实现由邮件服务提供者提供，例如Sun的`smtp.jar`文件。

## 产品支持系统中的电子邮件通知

回到当前问题。产品支持系统需要在问题路由给相应的支持人员、开发人员或测试人员时通知该人员。此路由发生在模型组件的`addProblemLog()`方法中（参见第19章中的`com.lyricnote.support.Model`类列表）。

路由事件ID如下：

- RPS 路由到产品支持
- RPD 路由到产品开发
- RQA 路由到测试

在`addProblemLog()`中，您可以确定事件ID是否是这三个之一。如果是，则调用新的模型方法`notifySupport(ProblemLog log)`，如下所示：

```java
/**
 * Sends email to the appropriate support person
 */
public void notifySupport(ProblemLog log)
    throws SQLException, IOException
{
    // Get the problem object

    String problemID = log.getProblemID();
    setProblemID(problemID);
    Problem problem = getProblem();

    // Create the subject line from the problem ID
    // and problem description

    StringBuffer sb = new StringBuffer();
    sb.append("Problem ID: ");
    sb.append(problemID);
    sb.append(" ");
    sb.append(problem.getDescription());
    String subject = sb.toString();

    // Get the product object. We need this to find out
    // the support ID's and the corresponding e-mail
    // addresses

    String productID = problem.getProductID();
    setProductID(productID);
    Product product = getProduct();

    // Determine the appropriate party to receive the mail

    String employeeID = null;
    String eventDescription = null;
    String eventID = log.getEventID();
    if (eventID.equals("RPS")) {
        employeeID = product.getProductSupport();
        eventDescription = "ROUTED TO PRODUCT SUPPORT";
    }
    else
    if (eventID.equals("RPD")) {
        employeeID = product.getDeveloper();
        eventDescription = "ROUTED TO DEVELOPMENT";
    }
    else
    if (eventID.equals("RQA")) {
        employeeID = product.getTester();
        eventDescription = "ROUTED TO TEST";
    }
    else
        return;

    eventDescription += "\r\n";
    eventDescription += log.getComments();

    // Lookup that person's email address

    Employee employee = getEmployee(employeeID);
    String email = employee.getEmail();

    // Send mail to the party

    Address fromUser = new InternetAddress
        ("support@lyricnote.com", "Product Support System");
    Address toUser = new InternetAddress
        (email, employee.getName());

    Properties props = new Properties();
    props.put("mail.host", "mail.lyricnote.com");
    Session mailSession = Session.getInstance(props, null);
    Message body = new MimeMessage(mailSession);

    try {
        body.setFrom(fromUser);
        body.setRecipient(Message.RecipientType.TO, toUser);
        body.setSubject(subject);
        body.setContent(eventDescription, "text/plain");
        Transport.send(body);
    }
    catch (MessagingException e) {
        throw new IOException(e.getMessage());
    }
}
```

JSP及其他WEB组件



图 21-2 展示了此新功能的实际应用。针对 MIDI Transposer 产品报告了一个问题。呼叫中心坐席填写了问题报告，并选择“转交产品支持”作为处理操作。当坐席点击提交按钮时，问题被添加到数据库中，并且调用了模型的 `addProblemLog()` 方法。由于事件类型是 RPS，`notifySupport()` 方法被调用，导致图 21-3 中所示的消息被发送给产品支持代表。

![](img/7a2f73369bb140583c7288b73456addb_744_0.png)

图 21-3. 发送给产品支持代表的电子邮件消息

## 总结

正如 Web 浏览器以外的程序可以成为 JSP 客户端一样，JSP 页面也可以作为其他服务器的客户端。本章探讨了两种此类环境：

-   从 CGI 服务器获取数据
-   使用 JavaMail API 发送邮件

JSP、servlet、CGI、PHP 和 ASP，以及其他服务器端脚本环境，都使用一种通用技术来向其客户端交付内容：HTTP 协议。`java.net` 包提供了 `URL` 和 `URLConnection` 类，它们包含通过 HTTP 访问资源的方法。

JavaMail API 是一个可扩展的架构，用于建模邮件系统的所有部分。特定邮件协议（如 POP、SMTP 和 IMAP）的实现可自由获取。

## 第五部分

### 附录

本书此部分包含关于 Servlet API、JSP API 和 HTTP 协议的参考资料。

## 完全参考

## 附录 A

Servlet API 版本 2.3

本附录描述了两个 servlet 包中的每个类：

-   `javax.servlet`：与协议无关的 Servlet 类
-   `javax.servlet.http`：HTTP 特定的 Servlet 类

对于每个类，都包含以下部分：

-   类名
-   上下文（全名、类型、超类、实现的接口）
-   类描述
-   类中每个方法的详细信息

> **注意**
>
> 此处描述的类和方法基于 Servlet 2.3 规范的最终公开草案。虽然最终草案可能与官方规范非常接近，但可能会有变更。如有疑问，请查阅 http://java.sun.com/products/servlet/index.html 上的最新规范版本。
>
> 许多类和方法被标记为已弃用。这意味着它们不再推荐使用，并且可能在将来的版本中停止支持。

## 包 javax.servlet

## Filter

**全名：** `javax.servlet.Filter`

**类型：** 接口

实现 `Filter` 接口的类对请求、响应或两者执行过滤任务。这些类通过实现 `doFilter()` 方法来完成此操作。

### 方法

### doFilter

```
public void doFilter(
    ServletRequest request,
    ServletResponse response,
    FilterChain chain)
  throws IOException, ServletException
```

每当请求通过过滤器链时，servlet 引擎会调用此方法。

### getFilterConfig

```
public FilterConfig getFilterConfig()
```

返回此 Filter 的 `FilterConfig`。

### setFilterConfig

```
public void setFilterConfig(FilterConfig filterConfig)
```

设置 `FilterConfig` 对象。当 servlet 引擎处理完此 Filter 后，也会使用 `null` 调用此方法。

## FilterChain

| 全名: | `javax.servlet.FilterChain` |
| :--- | :--- |
| 类型: | 接口 |
| 超级接口: | 无 |

提供过滤器调用链的视图。Filter 使用 `FilterChain` 来调用链中的下一个过滤器。

### 方法

### doFilter

```
public void doFilter(
    ServletRequest request,
    ServletResponse response)
    throws IOException, ServletException
```

调用链中的下一个过滤器或链末尾的资源。

## FilterConfig

| 全名: | `javax.servlet.FilterConfig` |
| :--- | :--- |
| 类型: | 接口 |

在初始化期间向过滤器传递信息。

### 方法

### getFilterName

```
public String getFilterName()
```

返回过滤器名称。

### getInitParameter

```
public String getInitParameter(String name)
```

返回指定参数的值，如果参数不存在则返回 `null`。

### getInitParameterNames

```
public Enumeration getInitParameterNames()
```

返回 servlet 初始化参数名称的枚举。如果没有初始化参数，则返回空枚举。

### getServletContext

```
public ServletContext getServletContext()
```

返回调用者正在执行的 `ServletContext`。

## GenericServlet

| 全名: | `javax.servlet.GenericServlet` |
| :--- | :--- |
| 类型: | 抽象类 |
| 实现: | `javax.servlet.Servlet`<br>`javax.servlet.ServletConfig`<br>`java.io.Serializable` |

用于不依赖于 HTTP 协议特定功能的 servlet 的基类。`GenericServlet` 实现了所有 servlet 的基本功能：

-   初始化
-   请求处理
-   终止

唯一必须被重写的方法是 `service()`，它实际处理请求。

`HttpServlet` 是 HTTP servlet 的基类，更常用作 servlet 的超类。

### 构造函数

### GenericServlet

```
public GenericServlet()
```

一个空构造函数，不执行任何操作。任何 servlet 初始化都应在 `init()` 方法中完成。

### 方法

### destroy

```
public void destroy()
```

当 servlet 被卸载时，由 servlet 引擎调用。Servlet 作者可以重写此方法以释放任何已分配的资源。

在 `GenericServlet` 中，此方法只是记录它已被执行的事实。

### getInitParameter

```
public String getInitParameter(String name)
```

给定初始化参数名称，返回参数的值。如果不存在这样的参数，则返回 `null`。

### getInitParameterNames

```
public Enumeration getInitParameterNames()
```

返回此 servlet 存在的所有初始化参数名称的 `Enumeration`。

### getServletConfig

```
public ServletConfig getServletConfig()
```

返回与此 servlet 关联的 `ServletConfig` 对象。

### getServletContext

```
public ServletContext getServletContext()
```

返回与此 servlet 关联的 `ServletContext` 对象。

### getServletInfo

```
public String getServletInfo()
```

返回关于 servlet 的标识信息，例如作者、版本和版权。

### getServletName

```
public String getServletName()
```

返回此 servlet 实例的名称。

### init

```
public void init() throws ServletException
```

调用 `super.init(config)` 的便捷方法。

### init

```
public void init(ServletConfig config)
    throws ServletException
```

由 servlet 容器调用，以指示 servlet 正在被投入使用。

### log

```
public void log(String msg)
```

将指定消息写入 servlet 日志文件。

### log

```
public void log(String message, Throwable t)
```

将指定消息写入 servlet 日志文件。`Throwable` 中的消息也会写入日志。

### service

```
public abstract void service(
    ServletRequest req,
    ServletResponse res)
  throws ServletException, IOException
```

由 servlet 容器调用以允许 servlet 处理请求。

## RequestDispatcher

**全名：** `javax.servlet.RequestDispatcher`
**类型：** 接口

用于将请求从客户端传递到服务器上任何资源的对象。

### 方法

### forward

```
public void forward(
    ServletRequest request,
    ServletResponse response)
  throws ServletException, IOException
```

将请求从一个 servlet 转发到另一个 servlet、JSP 页面或 HTML 文档。`forward` 只能在响应被提交之前调用。

### include

```
public void include(
    ServletRequest request,
    ServletResponse response)
    throws ServletException, IOException
```

在当前输出缓冲区中包含另一个 servlet、JSP 页面、HTML 文档的内容。被包含的资源不得设置任何响应头。

## Servlet

| **全名：** | `javax.servlet.Servlet` |
| :--- | :--- |
| **类型：** | `接口` |

定义所有 servlet 必须实现的方法。Servlet API 在 `GenericServlet` 和 `HttpServlet` 类中提供了此接口的具体实现。

### 方法

### destroy

```
    public void destroy()
```

当 servlet 被停止服务时，由 servlet 容器调用。

### getServletConfig

```
    public ServletConfig getServletConfig()
```

返回与此 servlet 关联的 `ServletConfig` 对象。

### getServletInfo

```
    public String getServletInfo()
```

返回关于 servlet 的标识信息。

### init

```
    public void init(ServletConfig config) throws ServletException
```



## service

```
public void service(
    ServletRequest req,
    ServletResponse res)
    throws ServletException, IOException
```

由 Servlet 容器调用以处理请求。

## ServletConfig

**全名：** javax.servlet.ServletConfig
**类型：** 接口

由 Servlet 引擎使用，用于在初始化期间向 Servlet 传递信息。

### 方法

### getInitParameter

```
public String getInitParameter(String name)
```

返回指定初始化参数的值，如果该参数不存在则返回 null。

### getInitParameterNames

```
public Enumeration getInitParameterNames()
```

返回 Servlet 初始化参数名称的枚举，如果不存在任何参数则返回一个空枚举。

### getServletContext

```
public ServletContext getServletContext()
```

返回与该 Servlet 关联的 ServletContext。

### getServletName

```
public String getServletName()
```

返回 `web.xml` 部署描述符中记录的 Servlet 实例名称。

## ServletContext

**全名：** javax.servlet.ServletContext
**类型：** 接口

定义了一组方法，Servlet 可用这些方法与其 Servlet 容器进行通信。Servlet 上下文可以存储对应用程序中所有 Servlet 都可用的属性。

### 方法

### getAttribute

```
public Object getAttribute(String name)
```

返回具有指定名称的应用程序级属性，如果该属性不存在则返回 `null`。该对象必须转换为适当的类型。

### getAttributeNames

```
public Enumeration getAttributeNames()
```

返回 Servlet 上下文中属性名称的枚举。

### getContext

```
public ServletContext getContext(String uripath)
```

返回同一服务器上另一个 URL 的 `ServletContext` 对象。路径必须以 "/" 开头，并将被解释为相对于 Web 服务器文档根目录的路径。

### getInitParameter

```
public String getInitParameter(String name)
```

返回指定的初始化参数。

### getInitParameterNames

```
public Enumeration getInitParameterNames()
```

返回 Servlet 上下文初始化参数名称的枚举，如果不存在任何参数则返回一个空枚举。

### getMajorVersion

```
public int getMajorVersion()
```

返回 Servlet API 版本号中十进制点左侧的整数。

### getMimeType

```
public String getMimeType(String file)
```

返回指定文件的 MIME 类型，如果 MIME 类型未知则返回 null。

### getMinorVersion

```
public int getMinorVersion()
```

返回 Servlet API 版本号中十进制点右侧的数字。

### getNamedDispatcher

```
public RequestDispatcher getNamedDispatcher(String name)
```

返回为指定 Servlet 准备的 RequestDispatcher，如果无法返回 RequestDispatcher 则返回 null。

### getRealPath

```
public String getRealPath(String path)
```

给定当前 Servlet 上下文中的 URI 路径，将该路径转换为其引用的绝对文件名。

### getRequestDispatcher

```
public RequestDispatcher getRequestDispatcher(String path)
```

返回为指定资源准备的 `RequestDispatcher`，如果无法创建则返回 `null`。路径名必须以 "/" 开头，并被解释为相对于 Servlet 上下文根目录的路径。

### getResource

```
public URL getResource(String path) throws MalformedURLException
```

返回指定资源的 URL，如果无法创建则返回 `null`。路径名必须以 "/" 开头，并被解释为相对于 Servlet 上下文根目录的路径。

### getResourceAsStream

```
public InputStream getResourceAsStream(String path)
```

返回指定资源的 `InputStream`，如果无法创建则返回 `null`。路径名必须以 "/" 开头，并被解释为相对于 Servlet 上下文根目录的路径。

### getResourcePaths

```
public Set getResourcePaths()
```

返回一个 `Set` 字符串集合，代表 Web 应用程序中资源的路径。路径以领先的 / 开头，并相对于 Servlet 上下文的根目录。

### getServerInfo

```
public String getServerInfo()
```

返回 Servlet 引擎的名称和版本。返回值的格式为 *servername/version_number*。

## 附录 A：Servlet API 版本 2.3

### [已弃用] getServlet

```
public Servlet getServlet(String name) throws ServletException
```

由于安全原因，不再支持。请参阅 HttpSessionListener 了解替代方法。

### getServletContextName

```
public String getServletContextName()
```

返回 Web 应用程序的名称，对应于此 ServletContext 在 web.xml 部署描述符中的 display-name 元素。

### [已弃用] getServletNames

```
public Enumeration getServletNames()
```

由于安全原因，不再支持。请参阅 HttpSessionListener 了解替代方法。

### [已弃用] getServlets

```
public Enumeration getServlets()
```

### [已弃用] log

```
public void log(Exception exception, String msg)
```

不再支持。请改用 log(String message, Throwable t)。

### log

```
public void log(String msg)
```

将指定消息写入 Servlet 日志。

### log

```
public void log(String message, Throwable throwable)
```

将指定消息和给定 `Throwable` 的堆栈跟踪写入 Servlet 日志。

### removeAttribute

```
public void removeAttribute(String name)
```

从 Servlet 上下文中移除具有指定名称的属性。

### setAttribute

```
public void setAttribute(String name, Object object)
```

在此 Servlet 上下文中，将对象存储在指定的属性名下。

## ServletContextAttributeEvent

**全名：** javax.servlet.ServletContextAttributeEvent
**类型：** 类
**继承自：** javax.servlet.ServletContextEvent

用于 Web 应用程序 Servlet 上下文属性变更的通知。

### 构造方法

```
public ServletContextAttributeEvent(
    ServletContext source,
    String name,
    Object value)
```

根据指定的上下文、名称和值构造一个 `ServletContextAttributeEvent`。

### 方法

### getName

```
public String getName()
```

返回已更改属性的名称。

### getValue

```
public Object getValue()
```

返回被添加、移除或替换的属性的值。该值取决于属性是被添加、更改还是删除。对于更改或删除，它是旧属性的值。对于添加，它是新属性的值。

## ServletContextAttributesListener

**全名：** javax.servlet.ServletContextAttributesListener
**类型：** 接口
**父接口：** java.util.EventListener

实现此接口的类将收到 Servlet 上下文属性列表变更的通知。

### 方法

### attributeAdded

```
public void attributeAdded(ServletContextAttributeEvent scab)
```

当新属性添加到 Servlet 上下文时被调用。

### attributeRemoved

```
public void attributeRemoved(ServletContextAttributeEvent scab)
```

当现有属性从 Servlet 上下文中移除时被调用。

### attributeReplaced

```
public void attributeReplaced(ServletContextAttributeEvent scab)
```

当现有属性在 Servlet 上下文中被替换时被调用。

## ServletContextEvent

**全名：** javax.servlet.ServletContextEvent
**类型：** 类
**继承自：** java.util.EventObject

用于 Servlet 上下文变更通知的事件类。

### 构造方法

**ServletContextEvent**

```
public ServletContextEvent(ServletContext source)
```

从给定的上下文创建一个 `ServletContextEvent`。

### 方法

**getServletContext**

```
public ServletContext getServletContext()
```

返回已更改的 `ServletContext`。

## ServletContextListener

**全名：** javax.servlet.ServletContextListener
**类型：** 接口
**父接口：** java.util.EventListener

实现此接口的类将收到关于 Servlet 上下文变更的通知。

### 方法

**contextDestroyed**

```
public void contextDestroyed(ServletContextEvent sce)
```

当 Servlet 上下文即将关闭时被调用。

contextInitialized

```java
public void contextInitialized(ServletContextEvent sce)
```

当Web应用程序准备处理请求时调用。

## ServletException

| 属性 | 值 |
| :--- | :--- |
| 全名 | `javax.servlet.ServletException` |
| 类型 | 类 |
| 继承自 | `java.lang.Exception` |

一个通用的servlet异常。

### 构造方法

#### ServletException

```java
public ServletException()
```

创建一个新的servlet异常。

#### ServletException

```java
public ServletException(String message)
```

创建一个带有指定消息的新servlet异常。

#### ServletException

```java
public ServletException(String message, Throwable rootCause)
```

创建一个包含消息和根本原因异常的新servlet异常。

#### ServletException

```java
public ServletException(Throwable rootCause)
```

创建一个包含根本原因异常的新servlet异常。

### 方法

**getRootCause**

```java
public Throwable getRootCause()
```

返回当前servlet异常的根本原因异常。

## ServletInputStream

| 属性 | 值 |
| :--- | :--- |
| 全名 | `javax.servlet.ServletInputStream` |
| 类型 | 抽象类 |
| 继承自 | `java.io.InputStream` |

servlet可以使用它从客户端请求中读取二进制数据的输入流。通常通过`ServletRequest.getInputStream()`方法获取。

### 方法

**readLine**

```java
public int readLine(byte[] b, int off, int len)
    throws IOException
```

从输入流中一次读取一行，从指定偏移量开始。将字节读入数组，直到读取了指定数量的字节或换行符（也读入数组）。如果在读取最大字节数之前到达文件末尾，则返回-1。

## ServletOutputStream

| 属性 | 值 |
| :--- | :--- |
| 全名 | `javax.servlet.ServletOutputStream` |
| 类型 | 抽象类 |
| 继承自 | `java.io.OutputStream` |

用于向客户端发送二进制数据的输出流。通常通过`ServletResponse.getOutputStream()`方法获取。

### 方法

**print**

```java
public void print(boolean b) throws IOException
```

将布尔值写入客户端，但末尾不添加回车换行符。

**print**

```java
public void print(char c) throws IOException
```

将字符写入客户端，但末尾不添加回车换行符。

**print**

```java
public void print(double d) throws IOException
```

将双精度值写入客户端，但末尾不添加回车换行符。

**print**

```java
public void print(float f) throws IOException
```

将单精度浮点值写入客户端，但末尾不添加回车换行符。

**print**

```java
public void print(int i) throws IOException
```

将整数写入客户端，但末尾不添加回车换行符。

**print**

```java
public void print(long l) throws IOException
```

将长整型值写入客户端，但末尾不添加回车换行符。

**print**

```java
public void print(String s) throws IOException
```

将字符串写入客户端，但末尾不添加回车换行符。

**println**

```java
public void println() throws IOException
```

向客户端写入一个回车换行符。

**println**

```java
public void println(boolean b) throws IOException
```

将布尔值写入客户端，后跟一个回车换行符。

**println**

```java
public void println(char c) throws IOException
```

将字符写入客户端，后跟一个回车换行符。

**println**

```java
public void println(double d) throws IOException
```

将双精度值写入客户端，后跟一个回车换行符。

**println**

```java
public void println(float f) throws IOException
```

将单精度浮点值写入客户端，后跟一个回车换行符。

**println**

```java
public void println(int i) throws IOException
```

将整数写入客户端，后跟一个回车换行符。

**println**

```java
public void println(long l) throws IOException
```

将长整型值写入客户端，后跟一个回车换行符。

**println**

```java
public void println(String s) throws IOException
```

将字符串写入客户端，后跟一个回车换行符。

## ServletRequest

| 属性 | 值 |
| :--- | :--- |
| 全名 | `javax.servlet.ServletRequest` |
| 类型 | 接口 |

代表客户端对servlet请求的接口。servlet引擎创建一个ServletRequest对象并将其作为参数传递给servlet的service方法。具有用于检索参数名称和值、属性以及输入流的方法。

### 方法

**getAttribute**

```java
public Object getAttribute(String name)
```

返回指定属性的值，如果不存在指定名称的属性则返回null。

**getAttributeNames**

```java
public Enumeration getAttributeNames()
```

返回此请求可用属性名称的枚举，如果请求没有属性则返回空枚举。

**getCharacterEncoding**

```java
public String getCharacterEncoding()
```

返回此请求正文中使用的字符编码名称，如果请求未指定字符编码则返回null。

**getContentLength**

```java
public int getContentLength()
```

返回请求正文的长度，如果长度未知则返回-1。在HTTP servlet中，这与CGI变量CONTENT_LENGTH的值相同。

**getContentType**

```java
public String getContentType()
```

返回请求正文的MIME类型，如果未知则返回null。在HTTP servlet中，与CGI变量CONTENT_TYPE的值相同。

**getInputStream**

```java
public ServletInputStream getInputStream() throws IOException
```

以二进制数据形式检索请求正文。可以调用`getInputStream()`或`getReader()`来读取正文，但不能同时调用两者。

**getLocale**

```java
public Locale getLocale()
```

返回客户端将接受内容的首选`Locale`（如果已指定）。否则，返回服务器的默认区域设置。

**getLocales**

```java
public Locale getLocale()
```

返回按用户偏好顺序排列的`Locale`对象的`Enumeration`，如果客户端未指示首选区域设置，则返回包含一个`Locale`（服务器的默认区域设置）的`Enumeration`。

**getParameter**

```java
public String getParameter(String name)
```

以字符串形式返回请求参数的值，如果参数不存在则返回null。

**getParameterMap**

```java
public Map getParameterMap()
```

返回此请求参数的java.util.Map。

**getParameterNames**

```java
public Enumeration getParameterNames()
```

返回此请求参数名称的java.util.Enumeration，如果请求没有参数则返回空枚举。

**getParameterValues**

```java
public String[] getParameterValues(String name)
```

返回包含给定请求参数所有值的String对象数组，如果参数不存在则返回null。

**getProtocol**

```java
public String getProtocol()
```

返回请求使用的协议的名称和版本。返回的值格式为protocol/majorVersion.minorVersion。在HTTP servlet中，这与CGI变量SERVER_PROTOCOL的值相同。

**getReader**

```java
public BufferedReader getReader() throws IOException
```

以字符数据形式检索请求正文。可以调用getInputStream()或getReader()，但不能同时调用两者。

**[已弃用] getRealPath**

```java
public String getRealPath(String path)
```

不再支持。

**getRemoteAddr**

```java
public String getRemoteAddr()
```

返回发送请求的客户端的互联网协议（IP）地址。对于HTTP servlet，与CGI变量REMOTE_ADDR相同。

**getRemoteHost**

```java
public String getRemoteHost()
```

返回发送请求的客户端的名称，如果无法确定名称则返回客户端的IP地址。对于HTTP servlet，与CGI变量REMOTE_HOST相同。

**getRequestDispatcher**

```java
public RequestDispatcher getRequestDispatcher(String path)
```

返回位于指定路径的资源的RequestDispatcher对象。此方法与ServletContext.getRequestDispatcher()的区别在于此方法可以接受相对路径。

**getScheme**

```java
public String getScheme()
```

返回用于发出请求的协议方案。

**getServerName**

```java
public String getServerName()
```

返回接收请求的服务器主机名。在HTTP servlet中，这与CGI变量SERVER_NAME相同。

**getServerPort**

```java
public int getServerPort()
```

返回接收请求的服务器端口号。



## getServerPort

```
public int getServerPort()
```

返回此请求被发送到的端口号。在 HTTP Servlet 中，这与 CGI 变量 SERVER_PORT 相同。

## isSecure

```
public boolean isSecure()
```

如果此请求是通过安全通道（例如 `https`）发出的，则返回 `true`。

## removeAttribute

```
public void removeAttribute(String name)
```

从此请求中移除指定名称的属性。

## setAttribute

```
public void setAttribute(String name, Object o)
```

将属性绑定到此请求，并使用给定的名称。

## setCharacterEncoding

```
public void setCharacterEncoding(String env)
    throws UnsupportedEncodingException
```

指定此请求正文中使用的字符编码。必须在读取请求参数或输入数据之前调用。

## ServletRequestWrapper

| 全名： | `javax.servlet.ServletRequestWrapper` |
| --- | --- |
| 类型： | 类 |
| 实现： | `javax.servlet.ServletRequest` |

`ServletRequest` 的一个实现，可以被子类化以扩展 Servlet 引擎的实现类。

### 构造函数

**ServletRequestWrapper**

```
public ServletRequestWrapper(ServletRequest request)
```

为给定的请求对象创建一个 ServletRequest 适配器。

### 方法

**getAttribute**

```
public Object getAttribute(String name)
```

返回指定属性的值，如果不存在指定名称的属性，则返回 null。

**getAttributeNames**

```
public Enumeration getAttributeNames()
```

返回一个枚举，其中包含此请求可用的属性名称，如果请求没有属性，则返回一个空的枚举。

**getCharacterEncoding**

```
public String getCharacterEncoding()
```

返回此请求正文中使用的字符编码名称，如果请求未指定字符编码，则返回 null。

**getContentLength**

```
public int getContentLength()
```

返回请求正文的长度，如果长度未知，则返回 -1。在 HTTP Servlet 中，这与 CGI 变量 CONTENT_LENGTH 的值相同。

**getContentType**

```
public String getContentType()
```

返回请求正文的 MIME 类型，如果未知，则返回 null。在 HTTP Servlet 中，与 CGI 变量 CONTENT_TYPE 的值相同。

## getInputStream

```
public ServletInputStream getInputStream() throws IOException
```

以二进制数据形式检索请求的正文。可以调用 `getInputStream()` 或 `getReader()` 来读取正文，但不能同时调用两者。

## getLocale

```
public Locale getLocale()
```

返回客户端接受内容的首选语言环境（如果指定）。否则，返回服务器的默认语言环境。

## getLocales

```
public Enumeration getLocales()
```

返回一个按用户偏好顺序排列的语言环境对象枚举，如果客户端未指示首选语言环境，则返回一个包含服务器默认语言环境的枚举。

## getParameter

```
public String getParameter(String name)
```

以字符串形式返回请求参数的值，如果参数不存在，则返回 null。

## getParameterMap

```
public Map getParameterMap()
```

返回此请求参数的 `java.util.Map` 映射。

## getParameterNames

```
public Enumeration getParameterNames()
```

返回此请求中参数名称的 `java.util.Enumeration` 枚举，如果请求没有参数，则返回一个空的 `Enumeration` 枚举。

## getParameterValues

```
public String getParameterValues(String name)
```

返回包含给定请求参数所有值的 `String` 对象数组，如果参数不存在，则返回 `null`。

## getProtocol

```
public String getProtocol()
```

返回请求使用的协议的名称和版本。返回的值采用 `protocol/majorVersion.minorVersion` 格式。在 HTTP Servlet 中，这与 CGI 变量 SERVER_PROTOCOL 相同。

## getReader

```
public BufferedReader getReader() throws IOException
```

以字符数据形式检索请求的正文。可以调用 `getInputStream()` 或 `getReader()`，但不能同时调用两者。

## getRealPath

```
public String getRealPath(String path)
```

返回 `getRealPath(String path)`。

## getRemoteAddr

```
public String getRemoteAddr()
```

返回发送请求的客户端的 Internet 协议（IP）地址。对于 HTTP Servlet，与 CGI 变量 REMOTE_ADDR 相同。

## getRemoteHost

```
public String getRemoteHost()
```

返回发送请求的客户端的名称，如果无法确定名称，则返回客户端的 IP 地址。对于 HTTP Servlet，与 CGI 变量 REMOTE_HOST 相同。

## getRequest

```
public ServletRequest getRequest()
```

返回被包装的请求对象。

## getRequestDispatcher

```
public RequestDispatcher getRequestDispatcher(String path)
```

返回一个 `RequestDispatcher` 对象，该对象作为位于指定路径的资源的包装器。此方法与 `ServletContext.getRequestDispatcher()` 的区别在于，此方法可以接受相对路径。

## getScheme

```
public String getScheme()
```

返回用于发出请求的方案。

## getServerName

```
public String getServerName()
```

返回接收请求的服务器的主机名。在 HTTP Servlet 中，这与 CGI 变量 SERVER_NAME 相同。

## getServerPort

```
public int getServerPort()
```

返回此请求被发送到的端口号。在 HTTP Servlet 中，这与 CGI 变量 SERVER_PORT 相同。

## isSecure

```
public boolean isSecure()
```

如果此请求是通过安全通道（例如 https）发出的，则返回 `true`。

## removeAttribute

```
public void removeAttribute(String name)
```

从此请求中移除指定名称的属性。

## setAttribute

```
public void setAttribute(String name, Object o)
```

将属性绑定到此请求，并使用给定的名称。

## setCharacterEncoding

```
public void setCharacterEncoding(String enc) throws UnsupportedEncodingException
```

指定此请求正文中使用的字符编码。必须在读取请求参数或输入数据之前调用。

## setRequest

```
public void setRequest(ServletRequest request)
```

设置请求对象。

## ServletResponse

**全名：** javax.servlet.ServletResponse
**类型：** 接口

封装有关为请求生成的响应的所有信息，包括响应头、状态码和输出流。HttpServletResponse 扩展了此接口以支持 HTTP 特定的功能。

### 方法

#### flushBuffer

```
public void flushBuffer() throws IOException
```

导致缓冲区被写入客户端，从而提交响应。

#### getBufferSize

```
public int getBufferSize()
```

返回响应中使用的实际缓冲区大小。如果缓冲被关闭，则返回零。

#### getCharacterEncoding

```
public String getCharacterEncoding()
```

返回此响应的字符集编码名称。

#### getLocale

```
public Locale getLocale()
```

返回响应使用的语言环境。

#### getOutputStream

```
public ServletOutputStream getOutputStream() throws IOException
```

返回此响应的 `ServletOutputStream`。如果已经为该响应调用过 `getWriter()`，则不能调用此方法。

#### getWriter

```
public PrintWriter getWriter() throws IOException
```

返回一个 `PrintWriter` 用于此响应。如果已经为该响应调用过 `getOutputStream()`，则不能调用此方法。

#### isCommitted

```
public boolean isCommitted()
```

如果响应已经被提交，则返回 true，这意味着响应已经写入了其状态码和头信息。

#### reset

```
public void reset()
```

清除响应缓冲区中的任何现有数据以及状态码和头信息。如果响应已经被提交，则抛出 `IllegalStateException`。

#### resetBuffer

```
public void resetBuffer()
```

清除响应缓冲区中的任何现有数据。此方法与 `reset()` 的不同之处在于它不清除状态码和头信息。如果响应已经被提交，则抛出 `IllegalStateException`。

#### setBufferSize

```
public void setBufferSize(int size)
```

为响应正文设置首选缓冲区大小。Servlet 引擎将使用至少与请求大小一样大的缓冲区。实际的缓冲区大小可以通过 `getBufferSize()` 检索。必须在写入任何正文内容之前调用，否则将抛出 `IllegalStateException`。

#### setContentLength

```
public void setContentLength(int len)
```

向客户端指示写入响应的内容的长度。

#### setContentType

```
public void setContentType(String type)
```

设置内容类型。

#### setLocale

```
public void setLocale(Locale loc)
```



设置响应的区域设置。必须在调用 getWriter() 之前调用。默认区域设置是服务器使用的那个。

## ServletResponseWrapper

| 全名： | javax.servlet.ServletResponseWrapper |
| 类型： | 类 |
| 实现： | javax.servlet.ServletResponse |

一个用于实现 ServletResponse 的子类的基类。其默认行为是调用 Servlet 引擎的 ServletResponse 实现类中的相应方法。

## 构造方法

### ServletResponseWrapper

```
public ServletResponseWrapper(ServletResponse response)
```

为指定的响应对象创建一个 ServletResponseWrapper。

## 方法

### flushBuffer

```
public void flushBuffer() throws IOException
```

将缓冲区的内容写入客户端，从而提交响应。

### getBufferSize

```
public int getBufferSize()
```

返回响应中使用的实际缓冲区大小。如果禁用了缓冲，则返回零。

### getCharacterEncoding

```
public String getCharacterEncoding()
```

返回此响应的字符集编码名称。

### getLocale

```
public Locale getLocale()
```

返回响应使用的区域设置。

### getOutputStream

```
public ServletOutputStream getOutputStream()
    throws IOException
```

返回此响应的 `ServletOutputStream`。如果已为此响应调用过 `getWriter()`，则不能调用此方法。

### getResponse

```
public ServletResponse getResponse()
```

返回被包装的 `ServletResponse` 对象。

### getWriter

```
public PrintWriter getWriter() throws IOException
```

返回此响应的 `PrintWriter`。如果已为此响应调用过 `getOutputStream()`，则不能调用此方法。

### isCommitted

```
public boolean isCommitted()
```

如果响应已经被提交，则返回 `true`，这意味着响应已经写入了其状态码和头信息。

### reset

```
public void reset()
```

清除响应缓冲区中的任何现有数据以及状态码和头信息。如果响应已被提交，则抛出 `IllegalStateException`。

### resetBuffer

```
public void resetBuffer()
```

清除响应缓冲区中的任何现有数据。此方法与 `reset()` 的不同之处在于它不清除状态码和头信息。如果响应已被提交，则抛出 `IllegalStateException`。

### setBufferSize

```
public void setBufferSize(int size)
```

设置响应正文的首选缓冲区大小。Servlet 引擎将使用至少与请求大小一样大的缓冲区。实际缓冲区大小可以通过 `getBufferSize()` 检索。必须在写入任何正文内容之前调用，否则将抛出 `IllegalStateException`。

### setContentLength

```
public void setContentLength(int len)
```

向客户端指示写入响应的内容长度。

### setContentType

```
public void setContentType(String type)
```

设置内容类型。

### setLocale

```
public void setLocale(Locale loc)
```

设置响应的区域设置。必须在调用 `getWriter()` 之前调用。默认区域设置是服务器使用的那个。

### setResponse

```
public void setResponse(ServletResponse response)
```

保存对被包装的 Response 对象的引用。

## SingleThreadModel

- **全名：** `javax.servlet.SingleThreadModel`
- **类型：** 接口

一个可以由 Servlet 实现的接口，用于向 Servlet 引擎表明不能使用多个线程并发访问 `service()` 方法。这确保了 Servlet 一次只会处理一个请求。此接口中没有方法；它仅仅是一个标记，表示希望具有此行为。

> **注意** 虽然这使得 Servlet 的单个实例在其自身的 `service()` 方法内是线程安全的，但它并不能防止多个实例同时访问外部资源。

## 方法

`SingleThreadModel` 没有定义任何方法；它仅仅是一个标记接口。

## UnavailableException

- **全名：** `javax.servlet.UnavailableException`
- **类型：** 类
- **继承自：** `javax.servlet.ServletException`

`ServletException` 的一个子类，当 Servlet 无法再处理请求（无论是暂时还是永久）时由 Servlet 抛出。

## 构造方法

### [已弃用] UnavailableException

```
public UnavailableException(int seconds, Servlet servlet, String msg)
```

不再支持。

### [已弃用] UnavailableException

```
public UnavailableException(Servlet servlet, String msg)
```

不再支持。

### UnavailableException

```
public UnavailableException(String msg)
```

创建一个新的异常，其消息指定 Servlet 永久不可用。

### UnavailableException

```
public UnavailableException(String msg, int seconds)
```

为 Servlet 创建一个新的异常，其指定的错误消息表明 Servlet 暂时不可用。接受一个整数，表示预计 Servlet 将不可用的秒数。如果该数字为零或负数，则表示没有可用的估计值。

## 方法

### [已弃用] getServlet

```
public Servlet getServlet()
```

不再支持。

### getUnavailableSeconds

```
public int getUnavailableSeconds()
```

返回 Servlet 预计不可用的时间长度（以秒为单位），或者如果不可用是永久性的或时间不确定，则返回负数。

### isPermanent

```
public boolean isPermanent()
```

如果 Servlet 永久不可用，则返回 `true`。

## 包 javax.servlet.http

## Cookie

- **全名：** `javax.servlet.http.Cookie`
- **类型：** 类
- **实现：** `java.lang.Cloneable`

Cookie 是 Servlet 发送给请求者的一小部分键/值对集合。请求者（通常是 Web 浏览器）被要求在本地存储此信息，并在下次对相同 URL 发起请求时将其返回。
Servlet 引擎可以使用 Cookie 来存储特定客户端唯一的会话信息。这种用法对 Servlet 作者是透明的。你也可以分别使用 `HttpServletResponse.addCookie()` 和 `HttpServletRequest.getCookies()` 方法显式地发送和接收 Cookie。

> **注意** 用户可以拒绝接受 Cookie，因此你的应用程序应处理这种情况。

## 构造方法

### Cookie

```
public Cookie(String name, String value)
```

创建一个具有指定名称和值的新 Cookie。

## 方法

### clone

```
public Object clone()
```

返回此 Cookie 的一个副本。

### getComment

```
public String getComment()
```

返回 Cookie 的注释。

### getDomain

```
public String getDomain()
```

返回 Cookie 的域名。

### getMaxAge

```
public int getMaxAge()
```

返回在 Cookie 被删除之前应存储的最大秒数。请注意，这是相对于调用 `setMaxAge()` 的时间，而不是当前时间。

### getName

```
public String getName()
```

返回 Cookie 的名称。请注意，没有 `setName` 方法；你必须在构造方法中设置 Cookie 的名称。

### getPath

```
public String getPath()
```

返回 Cookie 可见的路径。对该路径或其任何子目录中的任何 URL 的请求都会导致该 Cookie 被返回。有关 Cookie 路径的更多信息，请参阅 RFC 2109。

### getSecure

```
public boolean getSecure()
```

如果用户代理（浏览器）将使用安全协议返回 Cookie，则返回 true。

### getValue

```
public String getValue()
```

返回 Cookie 的值。

### getVersion

```
public int getVersion()
```

返回 Cookie 协议版本：

- 0 原始 Netscape 规范
- 1 RFC 2109 规范

### setComment

```
public void setComment(String purpose)
```

将 Cookie 的注释字段设置为指定的字符串。

### setDomain

```
public void setDomain(String pattern)
```

设置 Cookie 的域名。域名可用于将 Cookie 的可见性限制在特定寻址方案中服务器的一个子集。域名在存储前会转换为小写。如果未指定域名，则 Cookie 仅返回给发送它的服务器。详情请参阅 RFC 2109。

### setMaxAge

```
public void setMaxAge(int expiry)
```

指定 Cookie 应持久化的时间长度（以秒为单位）。正数或零值请求浏览器在指定时间间隔后删除 Cookie。负数值请求浏览器仅在当前浏览器实例的持续时间内保持 Cookie 有效。

### setPath

```
public void setPath(String uri)
```

指定 Cookie 应可见的路径。例如，如果指定了路径 `/servlet/abc`，则该 Cookie 将随任何包含该路径的 URL 请求一起返回，例如 `/servlet/abc/def`。如果未指定路径，则默认为 `/`。路径必须包含设置 Cookie 的 Servlet。有关 Cookie 路径的更多详细信息，请参阅 RFC 2109。

# setSecure

```
public void setSecure(boolean flag)
```

告知用户代理（浏览器）是否应使用安全协议返回该 Cookie。

# setValue

```
public void setValue(String newValue)
```

将 Cookie 的值设置为指定的字符串。

# setVersion

```
public void setVersion(int v)
```

设置 Cookie 协议版本：

- 0 原始 Netscape 规范
- 1 RFC 2109 规范

# HttpServlet

| 全名： | javax.servlet.http.HttpServlet |
| 类型： | 抽象类 |
| 继承自： | javax.servlet.GenericServlet |
| 实现接口： | java.io.Serializable |

一个为在 HTTP 环境中操作的 Servlet 提供的抽象基类。HttpServlet 是 GenericServlet 的一个轻量级扩展，它为 HTTP GET、POST、PUT、DELETE、HEAD、OPTIONS 和 TRACE 请求提供了特定的方法。service() 方法用于确定 HTTP 请求类型并调用相应的方法。
一个典型的 HttpServlet 子类会重写 doGet()、doPost() 或两者，但通常不重写 service()。

# 构造方法

## HttpServlet

```
public HttpServlet()
```

默认（空）构造方法。不执行任何操作。所有 Servlet 初始化工作都应在继承自 GenericServlet 的 init() 方法中完成。

# 方法

## doDelete

```
protected void doDelete(
    HttpServletRequest req,
    HttpServletResponse resp)
    throws ServletException, IOException
```

处理 HTTP DELETE 请求。与 doPut() 类似，这种类型的请求通常不是由 Web 浏览器直接发起的。

## doGet

```
protected void doGet(
    HttpServletRequest req,
    HttpServletResponse resp)
    throws ServletException, IOException
```

处理 HTTP GET 请求。默认情况下，它只返回一个错误，指示该 Servlet 不处理 GET 方法。重写 doGet() 的 Servlet 作者通常会执行以下步骤：

1. 读取并处理 `HttpServletRequest` 参数。
2. 通过调用 `HttpServletResponse` 对象的 `getWriter()` 或 `getOutputStream()` 获取输出流。
3. 在响应对象中设置 `Content-Type` 头。
4. 写入输出 HTML 页面。

## doHead

```
protected void doHead(
    HttpServletRequest req,
    HttpServletResponse resp)
    throws ServletException, IOException
```

处理 HTTP `HEAD` 请求。这在功能上与 `GET` 请求类似，只是不会返回响应体，只返回状态和头信息。

## doOptions

```
protected void doOptions(
    HttpServletRequest req,
    HttpServletResponse resp)
    throws ServletException, IOException
```

处理 HTTP `OPTIONS` 请求，并返回 HTTP 服务器支持的方法列表。此方法通常不被重写。

## doPost

```
protected void doPost(
    HttpServletRequest req,
    HttpServletResponse resp)
    throws ServletException, IOException
```

处理 HTTP `POST` 请求。默认情况下，它只返回一个错误，指示该 Servlet 不处理 `POST` 方法。重写 `doPost()` 的 Servlet 作者通常会执行以下步骤：

1. 读取并处理 `HttpServletRequest` 参数。
2. 通过调用 `HttpServletResponse` 对象的 `getWriter()` 或 `getOutputStream()` 获取输出流。
3. 在响应对象中设置 `Content-Type` 头。
4. 写入输出 HTML 页面。

## doPut

```
protected void doPut(
    HttpServletRequest req,
    HttpServletResponse resp)
    throws ServletException, IOException
```

处理 HTTP PUT 请求。要写入的资源名称可以通过调用请求对象的 `getRequestURI()` 方法找到，资源数据本身可以从请求对象的输入流中读取。HTML 表单不支持 PUT 方法；这种类型的请求通常不是由 Web 浏览器直接发起的。

## doTrace

```
protected void doTrace(
    HttpServletRequest req,
    HttpServletResponse resp)
    throws ServletException, IOException
```

处理 HTTP TRACE 请求并回显请求头。此方法通常不被重写。

## getLastModified

```
protected long getLastModified(HttpServletRequest req)
```

返回请求对象最后被修改的时间（以毫秒为单位，从1970年1月1日开始计算），如果时间未知则返回 -1。默认实现总是返回 -1。

## service

```
protected void service(
    HttpServletRequest req,
    HttpServletResponse resp)
    throws ServletException, IOException
```

HTTP 请求的主要入口点。此方法确定请求方法（GET、POST 等）并将请求分派给适当的处理方法（doGet()、doPost() 等）。对于 GET 方法，它会尝试确定自上次请求以来资源是否已被修改。如果没有修改，则只返回一个 HTTP NOT_MODIFIED 状态行。此方法通常不被重写。

## service

```
public void service(
    ServletRequest req,
    ServletResponse res)
    throws ServletException, IOException
```

一个便利方法，它将协议无关的请求转换为 HTTP 请求（如果可能），然后调用特定于 HTTP 的 service() 方法。

# HttpServletRequest

**全名：** javax.servlet.http.HttpServletRequest
**类型：** 接口
**父接口：** javax.servlet.ServletRequest

封装了关于 HTTP 请求的所有信息：其参数、属性、头信息和输入数据。

# 方法

## getAuthType

```
public String getAuthType()
```

如果服务器使用像 BASIC 或 SSL 这样的认证方案，则返回此方案的名称，否则返回 null。

## getContextPath

```
public String getContextPath()
```

返回请求 URI 中指定 Servlet 上下文（应用程序）的部分。该路径以 "/" 字符开头，但不以 "/" 字符结尾。

## getCookies

```
public Cookie[] getCookies()
```

返回一个数组，包含客户端随此请求发送的所有 Cookie 对象。如果没有发送 Cookie，则返回 null。

## getDateHeader

```
public long getDateHeader(String name)
```

给定一个请求头名称，将对应的头值转换为一个 Date 对象，并作为 long 值返回（毫秒数，从1970年1月1日开始计算）。如果指定的请求头不存在，则返回 -1。

## getHeader

```
public String getHeader(String name)
```

返回指定请求头的字符串值，如果请求中未找到指定名称的头，则返回 null。

## getHeaderNames

```
public Enumeration getHeaderNames()
```

返回在此请求中找到的所有头名称的枚举。如果没有头，则根据 Servlet 引擎的实现返回 null 或一个空枚举。

## getHeaders

```
public Enumeration getHeaders(String name)
```

对于可以在请求中出现多次的头，此方法将返回头值的枚举。

## getIntHeader

```
public int getIntHeader(String name)
```

给定一个请求头名称，将对应的头值转换为整数并返回整数值。如果指定的请求头不存在，则返回 -1。

## getMethod

```
public String getMethod()
```

返回请求第一行中包含的 HTTP 方法，例如 GET 或 POST。

## getPathInfo

```
public String getPathInfo()
```

返回请求 URL 中紧跟在 Servlet 名称之后的部分，如果没有额外的路径信息，则返回 null。与 CGI 变量 PATH_INFO 相同。

## getPathTranslated

```
public String getPathTranslated()
```

返回请求 URL 中紧跟在 Servlet 名称之后的部分，并将其转换为真实的文件系统路径，如果没有额外的路径信息，则返回 null。与 CGI 变量 PATH_TRANSLATED 相同。

## getQueryString

```
public String getQueryString()
```

返回请求 URL 中跟在 "?" 之后的部分，如果没有查询字符串，则返回 null。通常只在 GET 请求中出现。与 CGI 变量 QUERY_STRING 相同。

## getRemoteUser

```
public String getRemoteUser()
```

如果 HTTP 认证处于活动状态并且用户已登录，则返回用户名。否则返回 null。与 CGI 变量 REMOTE_USER 相同。

## getRequestedSessionId

```
public String getRequestedSessionId()
```

返回客户端请求的会话 ID。注意：这不一定是当前有效的会话 ID。



# JSP：完整参考

返回客户端返回的会话ID值。通常与当前会话相同，但可能指代一个旧的已过期会话。如果请求未指定会话ID，则返回 `null`。

# getRequestURI

```java
public String getRequestURI()
```

返回请求URL的子字符串，从协议名称（例如，`http://`）开始（如果存在），并延伸至但不包括查询字符串（查询字符串以 `"?"` 开头）。

# getRequestURL

```java
public StringBuffer getRequestURL()
```

重建用于请求的完整URL。包括协议、服务器名称、端口号（如果与默认值不同）和文件名。不包括查询字符串。

# getServletPath

```java
public String getServletPath()
```

返回调用Servlet的该请求URL的部分。这包括Servlet名称或指向Servlet的路径，但不包括任何额外的路径信息或查询字符串。与CGI变量 `SCRIPT_NAME` 的值相同。

# getSession

```java
public HttpSession getSession()
```

一个便捷方法，返回 `HttpSession.getSession(true)` 的值。

# getSession

```java
public HttpSession getSession(boolean create)
```

返回当前的 `HttpSession` 对象，或创建一个新的（如果 `create` 参数为 `true`）。返回的值取决于会话是否已存在以及 `create` 参数是 `true` 还是 `false`：

| Session Exists | create | Returned |
| :--- | :--- | :--- |
| false | false | null |
| false | true | new session |
| true | false | existing session |
| true | true | existing session |

# getUserPrincipal

```java
public Principal getUserPrincipal()
```

如果用户已被认证，则返回该用户的 `java.security.Principal` 对象。否则，该方法返回 `null`。

# isRequestedSessionIdFromCookie

```java
public boolean isRequestedSessionIdFromCookie()
```

如果请求会话ID是从Cookie接收到的，而不是作为请求URL的一部分发送的，则返回 `true`。

# isRequestedSessionIdFromUrl

```java
public boolean isRequestedSessionIdFromUrl()
```

不再支持。请改用 `isRequestedSessionIdFromURL()`。

# isRequestedSessionIdFromURL

```java
public boolean isRequestedSessionIdFromURL()
```

如果请求的会话ID作为请求URL的一部分传入，而不是从Cookie发送的，则返回 `true`。

# isRequestedSessionIdValid

```java
public boolean isRequestedSessionIdValid()
```

如果请求指定了一个有效、活动会话的ID，则返回 `true`。

# isUserInRole

```java
public boolean isUserInRole(String role)
```

如果认证用户包含在部署描述符中的指定逻辑“角色”中，则返回 `true`。

# HttpServletRequestWrapper

| **Full Name:** | `javax.servlet.http.HttpServletRequestWrapper` |
| :--- | :--- |
| **Type:** | Class |
| **Extends:** | `javax.servlet.ServletRequestWrapper` |
| **Implements:** | `javax.servlet.http.HttpServletRequest` |

此类是 `HttpServletRequest` 的一个具体实现，可以以Servlet引擎无关的方式进行覆盖，为请求对象提供额外功能。默认情况下，会直接查看对应的特定于Servlet引擎的方法。

## 构造函数

### HttpServletRequestWrapper

```java
public HttpServletRequestWrapper(HttpServletRequest request)
```

创建一个包装给定请求的请求对象。

## 方法

### getAuthType

```java
public String getAuthType()
```

如果服务器使用像 `BASIC` 或 `SSL` 这样的身份验证方案，则返回此方案的名称，否则返回 `null`。

### getContextPath

```java
public String getContextPath()
```

返回指定Servlet上下文（应用程序）的请求URI部分。路径以 "/" 字符开头，但不以此结尾。

### getCookies

```java
public Cookie getCookies()
```

返回一个数组，包含客户端随此请求发送的所有 `Cookie` 对象。如果未发送任何Cookie，则返回 `null`。

### getDateHeader

```java
public long getDateHeader(String name)
```

给定一个请求头名称，将相应的头值转换为 `Date` 对象，该对象以 `long` 值（自1970年1月1日以来的毫秒数）返回。如果指定的请求头不存在，则返回 -1。

### getHeader

```java
public String getHeader(String name)
```

返回指定请求头的字符串值，如果在请求中找不到该名称的头，则返回 `null`。

### getHeaderNames

```java
public Enumeration getHeaderNames()
```

返回在此请求中找到的所有头名称的 `Enumeration`。如果没有头，则根据Servlet引擎的不同，返回 `null` 或一个空的 `Enumeration`。

### getHeaders

```java
public Enumeration getHeaders(String name)
```

对于在请求中可能出现多次的头，此方法将返回头值的 `Enumeration`。

### getIntHeader

```java
public int getIntHeader(String name)
```

给定一个请求头名称，将相应的头值转换为整数并返回整数值。如果指定的请求头不存在，则返回 -1。

### getMethod

```java
public String getMethod()
```

返回请求第一行中包含的HTTP方法，例如 GET 或 POST。

### getPathInfo

```java
public String getPathInfo()
```

返回请求URL中跟在Servlet名称后面的子字符串，如果没有额外的路径信息，则返回 `null`。与CGI变量 `PATH_INFO` 相同。

### getPathTranslated

```java
public String getPathTranslated()
```

返回请求URL中跟在Servlet名称后面的部分，该部分已转换为真实的文件系统路径，如果没有额外的路径信息，则返回 `null`。与CGI变量 `PATH_TRANSLATED` 相同。

### getQueryString

```java
public String getQueryString()
```

返回请求URL中跟在 "?" 后面的子字符串，如果没有查询字符串，则返回 `null`。通常仅在GET请求中找到。与CGI变量 `QUERY_STRING` 相同。

### getRemoteUser

```java
public String getRemoteUser()
```

如果HTTP身份验证处于活动状态且用户已登录，则返回用户名。否则返回 `null`。与CGI变量 `REMOTE_USER` 相同。

### getRequestedSessionId

```java
public String getRequestedSessionId()
```

返回客户端返回的会话ID值。通常与当前会话相同，但可能指代一个旧的已过期会话。如果请求未指定会话ID，则返回 `null`。

### getRequestURI

```java
public String getRequestURI()
```

返回请求URL的子字符串，从协议名称（例如，`http://`）开始（如果存在），并延伸至但不包括查询字符串（查询字符串以 `"?"` 开头）。

### getRequestURL

```java
public StringBuffer getRequestURL()
```

重建用于请求的完整URL。包括协议、服务器名称、端口号（如果与默认值不同）和文件名。不包括查询字符串。

### getServletPath

```java
public String getServletPath()
```

返回调用Servlet的该请求URL的部分。这包括Servlet名称或指向Servlet的路径，但不包括任何额外的路径信息或查询字符串。与CGI变量 `SCRIPT_NAME` 的值相同。

### getSession

```java
public HttpSession getSession()
```

一个便捷方法，返回 `HttpSession.getSession(true)` 的值。

### getSession

```java
public HttpSession getSession(boolean create)
```

返回当前的 `HttpSession` 对象，或创建一个新的（如果 `create` 参数为 `true`）。返回的值取决于会话是否已存在以及 `create` 参数是 `true` 还是 `false`：

| Session Exists | create | Returned |
| :--- | :--- | :--- |
| false | false | null |
| false | true | new session |
| true | false | existing session |
| true | true | existing session |

### getUserPrincipal

```java
public Principal getUserPrincipal()
```

如果用户已被认证，则返回该用户的 `java.security.Principal` 对象。否则，该方法返回 `null`。

### isRequestedSessionIdFromCookie

```java
public boolean isRequestedSessionIdFromCookie()
```

如果请求会话ID是从Cookie接收到的，而不是作为请求URL的一部分发送的，则返回 `true`。

### isRequestedSessionIdFromUrl

```java
public boolean isRequestedSessionIdFromUrl()
```

返回包装请求对象上已弃用的 `isRequestedSessionIdFromUrl()` 方法的值。

### isRequestedSessionIdFromURL

```java
public boolean isRequestedSessionIdFromURL()
```

如果请求的会话ID作为请求URL的一部分传入，而不是从Cookie发送的，则返回 `true`。

### isRequestedSessionIdValid

```java
public boolean isRequestedSessionIdValid()
```

如果请求指定了一个有效、活动会话的ID，则返回 `true`。



## isUserInRole

```java
public boolean isUserInRole(String role)
```

如果经过身份验证的用户在部署描述符中被包含在指定的逻辑“角色”中，则返回 `true`。

## HttpServletResponse

| 全名： | javax.servlet.http.HttpServletResponse |
| :--- | :--- |
| 类型： | 接口 |
| 超级接口： | javax.servlet.ServletResponse |

封装了为HTTP请求生成的所有响应信息，包括响应头、状态码和输出流。

### 方法

### addCookie

```java
public void addCookie(Cookie cookie)
```

为指定的Cookie写入一个Set-Cookie头。

### addDateHeader

```java
public void addDateHeader(String name, long date)
```

为一个可以有多个值的HTTP头写入一个日期头。

### addHeader

```java
public void addHeader(String name, String value)
```

为一个可以有多个值的HTTP头写入一个通用头。

### addIntHeader

```java
public void addIntHeader(String name, int value)
```

为一个可以有多个值的HTTP头写入一个整数头。

### containsHeader

```java
public boolean containsHeader(String name)
```

如果响应已经包含指定名称的头，则返回 `true`。

### [deprecated] encodeRedirectUrl

```java
public String encodeRedirectUrl(String url)
```

不再支持。

### encodeRedirectURL

```java
public String encodeRedirectURL(String url)
```

支持会话跟踪，方法是可选地将编码后的会话ID作为参数附加到旨在与 `sendRedirect()` 一起使用的URL中。如果客户端支持Cookie，则不需要这样做。Servlet引擎会做出这个判断；通过此方法过滤要写入的URL总是安全的。

### [deprecated] encodeUrl

```java
public String encodeUrl(String url)
```

不再支持。

### encodeURL

```java
public String encodeURL(String url)
```

支持会话跟踪，方法是在必要时将编码后的会话ID作为参数附加到指定的URL中。如果客户端支持Cookie，则不需要这样做。Servlet引擎会做出这个判断；通过此方法过滤要写入的URL总是安全的。

### sendError

```java
public void sendError(int sc) throws IOException
```

将HTTP状态码设置为指定的值。调用此方法后，响应对象将被提交；任何进一步的写入操作都将无效。

### sendError

```java
public void sendError(int sc, String msg) throws IOException
```

将HTTP状态码设置为指定的值并设置状态消息。调用此方法后，响应对象将被提交；任何进一步的写入操作都将无效。

### sendRedirect

```java
public void sendRedirect(String location) throws IOException
```

将HTTP状态码设置为302（临时重定向），并写入一个带有指定值的Location头。用户代理（Web浏览器）通常会解释此响应并自动请求新的URL。

### setDateHeader

```java
public void setDateHeader(String name, long date)
```

写入一个具有指定名称和正确格式化日期值的响应头。

### setHeader

```java
public void setHeader(String name, String value)
```

写入一个具有指定名称和值的响应头。

### setIntHeader

```java
public void setIntHeader(String name, int value)
```

写入一个具有指定名称和字符串格式整数值的响应头。

### setStatus

```java
public void setStatus(int sc)
```

设置此响应的状态码。

### [deprecated] setStatus

```java
public void setStatus(int sc, String sm)
```

不再支持。

## HttpServletResponseWrapper

| 全名： | javax.servlet.http.HttpServletResponseWrapper |
| :--- | :--- |
| 类型： | 类 |
| 继承自： | javax.servlet.ServletResponseWrapper |
| 实现接口： | javax.servlet.http.HttpServletResponse |

HttpServletResponse的一个具体实现，可以被扩展以允许自定义响应对象。默认情况下，此类中的方法会查看Servlet引擎实现类中的对应方法。

### 构造方法

### HttpServletResponseWrapper

```java
public HttpServletResponseWrapper(HttpServletResponse response)
```

创建一个包装指定响应的响应适配器。

### 方法

### addCookie

```java
public void addCookie(Cookie cookie)
```

为指定的Cookie写入一个Set-Cookie头。

### addDateHeader

```java
public void addDateHeader(String name, long date)
```

为一个可以有多个值的HTTP头写入一个日期头。

### addHeader

```java
public void addHeader(String name, String value)
```

为一个可以有多个值的HTTP头写入一个通用头。

### addIntHeader

```java
public void addIntHeader(String name, int value)
```

为一个可以有多个值的HTTP头写入一个整数头。

### containsHeader

```java
public boolean containsHeader(String name)
```

如果响应已经包含指定名称的头，则返回 `true`。

### encodeRedirectUrl

```java
public String encodeRedirectUrl(String url)
```

调用Servlet引擎特定类中已弃用的 `encodeRedirectUrl()` 方法。

### encodeRedirectURL

```java
public String encodeRedirectURL(String url)
```

支持会话跟踪，方法是可选地将编码后的会话ID作为参数附加到旨在与 `sendRedirect()` 一起使用的URL中。如果客户端支持Cookie，则不需要这样做。Servlet引擎会做出这个判断；通过此方法过滤要写入的URL总是安全的。

### encodeUrl

```java
public String encodeUrl(String url)
```

调用Servlet引擎特定类中已弃用的 `encodeUrl(String url)` 方法。

### encodeURL

```java
public String encodeURL(String url)
```

支持会话跟踪，方法是在必要时将编码后的会话ID作为参数附加到指定的URL中。如果客户端支持Cookie，则不需要这样做。Servlet引擎会做出这个判断；通过此方法过滤要写入的URL总是安全的。

### sendError

```java
public void sendError(int sc) throws IOException
```

将HTTP状态码设置为指定的值。调用此方法后，响应对象将被提交；任何进一步的写入操作都将无效。

### sendError

```java
public void sendError(int sc, String msg) throws IOException
```

将HTTP状态码设置为指定的值并设置状态消息。调用此方法后，响应对象将被提交；任何进一步的写入操作都将无效。

### sendRedirect

```java
public void sendRedirect(String location) throws IOException
```

将HTTP状态码设置为302（临时重定向），并写入一个带有指定值的Location头。用户代理（Web浏览器）通常会解释此响应并自动请求新的URL。

### setDateHeader

```java
public void setDateHeader(String name, long date)
```

写入一个具有指定名称和正确格式化日期值的响应头。

### setHeader

```java
public void setHeader(String name, String value)
```

写入一个具有指定名称和值的响应头。

### setIntHeader

```java
public void setIntHeader(String name, int value)
```

写入一个具有指定名称和字符串格式整数值的响应头。

### setStatus

```java
public void setStatus(int sc)
```

设置此响应的状态码。

### setStatus

```java
public void setStatus(int sc, String sm)
```

调用Servlet引擎特定类中已弃用的 `setStatus(int sc, String sm)` 方法。

## HttpSession

**全名：** `javax.servlet.http.HttpSession`

**类型：** 接口

`HttpSession` 是一个存储库，用于存放属于用户浏览器会话的对象的命名引用。该存储库在用户请求之间在服务器上保持活动状态。会话有一个由服务器分配的唯一会话ID，客户端会跟踪并在每个后续请求中传回此ID。

会话通过调用 `HttpServletRequest.getSession(true)` 或 `HttpServletRequest.getSession()` 方法创建。然后，会话ID通过Cookie或作为生成URL中的参数传递给客户端。在客户端加入会话之前，即客户端在后续请求中传回会话ID之前，会话被视为“新的”。可以使用 `isNew()` 方法来确定这一点。

使用 `setAttribute()` 方法将对象存储在会话中，可以使用 `getAttribute()` 方法检索对象。如果会话中的对象实现了 `HttpSessionBindingListener` 接口，那么在它被绑定到会话或从会话解除绑定时，它将收到通知。



## 方法

### getAttribute

```java
public Object getAttribute(String name)
```

如果会话中存在指定名称的对象，则返回该对象；如果不存在，则返回 `null`。

### getAttributeNames

```java
public Enumeration getAttributeNames()
```

返回一个 `Enumeration`，包含绑定到此会话的所有对象的名称。

### getCreationTime

```java
public long getCreationTime()
```

返回会话创建时间，以毫秒为单位，自 1970 年 1 月 1 日起算。

### getId

```java
public String getId()
```

返回会话标识符。

### getLastAccessedTime

```java
public long getLastAccessedTime()
```

返回会话最后被访问的时间，以毫秒为单位，自 1970 年 1 月 1 日起算。

### getMaxInactiveInterval

```java
public int getMaxInactiveInterval()
```

返回此会话在请求之间可保持活动状态的最大秒数。如果超过此时间间隔，servlet 引擎有权终止该会话。

**注意** 某些 servlet 引擎错误地将此值视为毫秒或分钟。如果依赖此方法的正确性，应验证其行为。

### [已弃用] *getSessionContext*

```java
public HttpSessionContext getSessionContext()
```

不再支持。

### [已弃用] *getValue*

```java
public Object getValue(String name)
```

不再支持。请改用 getAttribute(String name)。

### [已弃用] *getValueNames*

```java
public String getValueNames()
```

不再支持。请改用 getAttributeNames()。

### *invalidate*

```java
public void invalidate()
```

关闭会话，并为绑定到该会话的所有 HttpSessionBindingListener 对象调用 `valueUnbound()` 方法。

### *isNew*

```java
public boolean isNew()
```

如果会话已创建但客户端尚未使用该会话 ID 发出请求，则返回 true。

### [已弃用] *putValue*

```java
public void putValue(String name, Object value)
```

不再支持。请改用 setAttribute(String name, Object value)。

### removeAttribute

```java
public void removeAttribute(String name)
```

移除会话中具有指定名称的对象引用。如果该对象实现了 HttpSessionBindingListener 接口，servlet 引擎会调用其 valueUnbound() 方法。如果指定的值在会话中不存在，则忽略该操作。

### [已弃用] removeValue

```java
public void removeValue(String name)
```

不再支持。请改用 removeAttribute(String name)。

### setAttribute

```java
public void setAttribute(String name, Object value)
```

将对象引用以指定名称存储在会话中。如果该对象实现了 HttpSessionBindingListener 接口，servlet 引擎会调用其 valueBound() 方法。

### setMaxInactiveInterval

```java
public void setMaxInactiveInterval(int interval)
```

指定此会话在请求之间可保持活动状态的最大秒数。如果超过此时间间隔，servlet 引擎有权终止该会话。

> **注意** 某些 servlet 引擎错误地将此值视为毫秒或分钟。如果依赖此方法的正确性，应验证其行为。

## HttpSessionActivationListener

- 全名：javax.servlet.http.HttpSessionActivationListener
- 类型：接口

通过实现此接口，对象可以注册以接收会话激活和钝化事件的通知。

### 方法

#### sessionDidActivate

```java
public void sessionDidActivate(HttpSessionEvent se)
```

在会话刚被激活时调用。

#### sessionWillPassivate

```java
public void sessionWillPassivate(HttpSessionEvent se)
```

在会话即将被钝化时调用。

## HttpSessionAttributesListener

- 全名：javax.servlet.http.HttpSessionAttributesListener
- 类型：接口
- 父接口：java.util.EventListener

通过实现此接口，对象可以注册以接收属性添加/移除事件的通知。

### 方法

#### attributeAdded

```java
public void attributeAdded(HttpSessionBindingEvent se)
```

在属性被添加到会话时调用。

#### attributeRemoved

```java
public void attributeRemoved(HttpSessionBindingEvent se)
```

在属性从会话中移除时调用。

#### attributeReplaced

```java
public void attributeReplaced(HttpSessionBindingEvent se)
```

在会话中的属性被替换时调用。

## HttpSessionBindingEvent

- 全名：javax.servlet.http.HttpSessionBindingEvent
- 类型：类
- 继承自：javax.servlet.http.HttpSessionEvent

作为参数传递给 HttpSessionBindingListener 的 valueBound() 和 valueUnbound() 方法的事件对象。通过使用事件对象中的方法，HttpSessionBindingListener 可以获取其绑定的名称以及对 HttpSession 本身的引用。

### 构造函数

#### HttpSessionBindingEvent

```java
public HttpSessionBindingEvent(HttpSession session, String name)
```

为指定会话创建一个新的 HttpSessionBindingEvent 对象。参数 name 指示监听对象绑定到会话时所用的名称。

#### HttpSessionBindingEvent

```java
public HttpSessionBindingEvent(HttpSession session, String name, Object value)
```

为指定会话创建一个新的 HttpSessionBindingEvent 对象。参数 name 指示监听对象绑定到会话时所用的名称，参数 value 包含其值。

### 方法

#### getName

```java
public String getName()
```

返回对象在会话中已知的名称。

#### **getSession**

```java
public HttpSession getSession()
```

返回监听对象绑定到或从中解除绑定的会话。

#### **getValue**

```java
public Object getValue()
```

返回被添加、更改或删除的属性的值。

## HttpSessionBindingListener

- 全名：javax.servlet.http.HttpSessionBindingListener
- 类型：接口
- 父接口：java.util.EventListener

实现此接口的对象会在绑定到 HttpSession 或从其解除绑定时收到通知。对象必须提供 valueBound() 和 valueUnbound() 方法，每个方法都有一个 HttpSessionBindingEvent 参数，允许对象确定其名称及其所属的会话。

### 方法

#### **valueBound**

```java
public void valueBound(HttpSessionBindingEvent event)
```

在对象绑定到会话时调用。

#### **valueUnbound**

```java
public void valueUnbound(HttpSessionBindingEvent event)
```

在对象从会话解除绑定时调用。

## HttpSessionContext

- 全名：javax.servlet.http.HttpSessionContext
- 类型：接口

以前用于允许直接 servlet 间通信，此类现已弃用。

### 方法

#### **[已弃用] *getIds***

```java
public Enumeration getIds()
```

不再支持。

#### **[已弃用] *getSession***

```java
public HttpSession getSession(String sessionId)
```

不再支持。

## HttpSessionEvent

- 全名：javax.servlet.http.HttpSessionEvent
- 类型：类
- 继承自：java.util.EventObject

表示 Web 应用程序中会话更改的事件通知。

### 构造函数

#### **HttpSessionEvent**

```java
public HttpSessionEvent(HttpSession source)
```

从指定源创建一个新的会话事件。

### 方法

#### **getSession**

```java
public HttpSession getSession()
```

返回发生更改的会话的引用。

## HttpSessionListener

- 全名：javax.servlet.http.HttpSessionListener
- 类型：接口

实现 HttpSessionListener 的类在会话被创建或失效时接收通知。

### 方法

#### **sessionCreated**

```java
public void sessionCreated(HttpSessionEvent se)
```

在新会话被创建时调用。

#### **sessionDestroyed**

```java
public void sessionDestroyed(HttpSessionEvent se)
```

在会话被失效时调用。

## HttpUtils

- 全名：javax.servlet.http.HttpUtils
- 类型：类

一个提供在 HTTP servlet 中常用方法的实用工具类。



## 构造方法

### HttpUtils

```java
public HttpUtils()
```

创建一个新的 HttpUtils 对象。

## 方法

### getRequestURL

```java
public static StringBuffer getRequestURL(HttpServletRequest req)
```

返回指定请求所使用的完整 URL。包括协议、服务器名称、端口号（如果非默认端口）和文件名。不包括查询字符串。

### parsePostData

```java
public static Hashtable parsePostData(int len, ServletInputStream in)
```

从 Servlet 请求的输入流中读取指定长度的数据，并通过调用 parseQueryString() 将其解析为键/值对。

### parseQueryString

```java
public static Hashtable parseQueryString(String s)
```

给定一个包含 URL 编码参数和值的查询字符串，返回一个包含已解析名称和值的 Hashtable。在 Hashtable 中，参数名称是键，对应的值是一个字符串数组。如果参数只出现一次，则数组长度为一；否则，数组中会有多个条目。有关解码的具体细节，请参阅 java.net.URLEncoder。

## 附录 B

### JSP API 版本 1.2

本附录描述了 JSP 两个包中的每个类：

- `javax.servlet.jsp` - 基础 JavaServer Page 类
- `javax.servlet.jsp.tagext` - JSP 自定义标签

每个类都包含以下部分：

- 类名
- 上下文（全名、类型、父类、实现的接口）
- 类描述
- 类中每个方法的详细信息

> **注意：** 此处描述的类和方法基于 JSP 1.2 规范的提议最终草案。虽然最终草案可能非常接近官方规范，但可能会有变动。如有疑问，请查阅 http://java.sun.com/products/jsp 上的最新规范版本。

## 包 javax.servlet.jsp

### HttpJspPage

| 属性 | 值 |
| :--- | :--- |
| 全名： | `javax.servlet.jsp.HttpJspPage` |
| 类型： | 接口 |
| 父接口： | `javax.servlet.jsp.JspPage` |

一个由 JSP 引擎生成的 HTTP 特定类实现的 `JspPage` 子接口。JSP 引擎将自动创建一个包含页面中定义的所有脚本代码的 `_jspService()` 方法。JSP 作者不应重写此方法。

### 方法

#### _jspService

```java
public void _jspService(
    HttpServletRequest request,
    HttpServletResponse response)
    throws ServletException, IOException
```

JSP 页面的主体。JSP 作者*不应*定义此方法，因为它将由 JSP 容器生成的 Servlet 代码定义。`_jspService()` 是执行脚本并生成 HTML 模板输出的地方。

### JspEngineInfo

| 属性 | 值 |
| :--- | :--- |
| **全名：** | `javax.servlet.jsp.JspEngineInfo` |
| **类型：** | 抽象类 |

一个提供有关 JSP 引擎信息的类。此类的实例由 `JspFactory.getEngineInfo()` 方法返回。

> **注意：** 此类主要设计供 JSP 引擎开发者使用。

#### 构造方法

```java
public JspEngineInfo()
```

创建一个新的 `JspEngineInfo` 对象。

#### 方法

```java
public abstract String getSpecificationVersion()
```

返回 JSP 引擎支持的 JSP 规范版本。

### JspException

| 属性 | 值 |
| :--- | :--- |
| **全名：** | `javax.servlet.jsp.JspException` |
| **类型：** | 类 |
| **继承自：** | `java.lang.Exception` |

JSP 异常的通用基类。自定义标签类中的许多方法会抛出此异常。

#### 构造方法

##### JspException

```java
public JspException()
```

创建一个新的 JspException，没有关联的错误消息。

##### JspException

```java
public JspException(String msg)
```

创建一个新的 JspException，带有指定的消息。

##### JspException

```java
public JspException(String message, Throwable rootCause)
```

创建一个新的 JspException，带有指定的消息，并将指定的根因异常与其关联。

##### JspException

```java
public JspException(Throwable rootCause)
```

创建一个新的 JspException，关联指定的根因异常。

#### 方法

##### getRootCause

```java
public Throwable getRootCause()
```

返回导致此 JspException 的异常。

### JspFactory

| 属性 | 值 |
| :--- | :--- |
| 全名： | `javax.servlet.jsp.JspFactory` |
| 类型： | 抽象类 |

一个提供用于创建支持 JSP 环境所必需对象的工厂方法的类。包括一个用于分配默认 `JspFactory` 的静态方法。

> **注意：** 此类主要设计供 JSP 引擎开发者使用。

#### 构造方法

##### JspFactory

```java
public JspFactory()
```

创建一个新的 `JspFactory` 对象。

#### 方法

##### getDefaultFactory

```java
public static synchronized JspFactory getDefaultFactory()
```

返回当前注册的 `JspFactory` 对象。

##### getEngineInfo

```java
public abstract JspEngineInfo getEngineInfo()
```

返回此 JSP 实现的 `JspEngineInfo` 对象。

##### getPageContext

```java
public abstract PageContext getPageContext(
    Servlet servlet,
    ServletRequest request,
    ServletResponse response,
    String errorPageURL,
    boolean needsSession,
    int buffer,
    boolean autoflush)
```

返回 `PageContext` 对象。调用此方法将导致调用 `PageContext.initialize()` 方法，并设置以下属性：

- 请求 Servlet
- 请求 Servlet 的 `ServletConfig`
- `ServletRequest` 对象
- `ServletResponse` 对象
- JSP 错误页面的 URL（如果指定了）
- JSP 是否需要 HTTP 会话
- 缓冲区大小
- 缓冲区是否在溢出时自动刷新。

当调用 `releasePageContext()` 方法时，这些资源将被释放。

> **注意：** 对此方法的调用由 JSP 引擎自动生成，JSP 作者不应编写。

##### releasePageContext

```java
public abstract void releasePageContext(PageContext pc)
```

释放 `PageContext`，包括调用 `getPageContext()` 时获取的任何资源。

> **注意：** 对此方法的调用由 JSP 引擎自动生成，JSP 作者不应编写。

##### setDefaultFactory

```java
public static synchronized void setDefaultFactory(JspFactory factory)
```

设置默认的 `JspFactory` 对象。应仅由 JSP 引擎本身调用。

### JspPage

**全名：** `javax.servlet.jsp.JspPage`
**类型：** 接口
**父接口：** `javax.servlet.Servlet`

一个由 JSP 引擎生成的类实现的 `Servlet` 子接口。`jspInit()` 和 `jspDestroy()` 方法可由 JSP 作者重写，以执行 `Servlet` 的 `init()` 和 `destroy()` 方法所做的事情。

#### 方法

##### jspDestroy

```java
public void jspDestroy()
```

当生成的 JSP Servlet 被销毁时调用的方法。如果使用，必须在 JSP 声明中定义。应重写此方法而不是 `destroy()`。

##### jspInit

```java
public void jspInit()
```

当生成的 JSP Servlet 被初始化时调用的方法。如果使用，必须在 JSP 声明中定义。应重写此方法而不是 `init()`。

### JspTagException

| 属性 | 值 |
| :--- | :--- |
| 全名： | `javax.servlet.jsp.JspTagException` |
| 类型： | 类 |
| 继承自： | `javax.servlet.jsp.JspException` |

用于标签处理器中以表示致命错误的 `JspException` 子接口。

#### 构造方法

##### JspTagException

```java
public JspTagException()
```

创建一个新的 JspTagException，没有关联的消息。

##### JspTagException

```java
public JspTagException(String msg)
```

创建一个新的 JspTagException，带有指定的消息。

### JspWriter

| 属性 | 值 |
| :--- | :--- |
| 全名： | `javax.servlet.jsp.JspWriter` |
| 类型： | 抽象类 |
| 继承自： | `java.io.Writer` |

用于写入 JSP 输出的 `java.io.Writer` 子类。其作用主要与 `java.io.PrintWriter` 相同。此类由生成的 `_jspService()` 通过调用底层 Servlet 的 `getWriter()` 方法实例化，这使得之后调用 `getOutputStream()` 非法。隐式变量 `out` 是此类的一个实例。

#### 方法

##### clear

```java
public abstract void clear() throws IOException
```

清除页面缓冲区。如果缓冲区已被清除（即，如果已将完整缓冲区的数据写入输出流），则抛出 `IOException`。

##### clearBuffer

```java
public abstract void clearBuffer() throws IOException
```

清除页面缓冲区。不会抛出 `IOException`。

##### close

```java
public abstract void close() throws IOException
```

刷新并关闭流。

##### flush

```java
public abstract void flush() throws IOException
```

刷新输出流。



## getBufferSize

```
public int getBufferSize()
```

返回实际使用的缓冲区大小。

## getRemaining

```
public abstract int getRemaining()
```

返回缓冲区中未使用的剩余字节数。

## isAutoFlush

```
public boolean isAutoFlush()
```

返回一个指示，表明是否设置了 JSP 的 autoFlush 标志。

## newLine

```
public abstract void newLine() throws IOException
```

写入系统的换行符字符串。

## print

```
public abstract void print(boolean b) throws IOException
```

打印一个布尔值。

## print

```
public abstract void print(char c) throws IOException
```

打印一个字符值。

## print

```
public abstract void print(char[] s) throws IOException
```

打印一个字符数组。

# JSP：完整参考

## print

```
public abstract void print(double d) throws IOException
```

打印一个双精度浮点数。

## print

```
public abstract void print(float f) throws IOException
```

打印一个单精度浮点数。

## print

```
public abstract void print(int i) throws IOException
```

打印一个整数值。

## print

```
public abstract void print(long l) throws IOException
```

打印一个长整数值。

## print

```
public abstract void print(Object obj) throws IOException
```

使用对象的 `toString()` 方法打印一个对象。

## print

```
public abstract void print(String s) throws IOException
```

打印一个字符串。

## println

```
public abstract void println() throws IOException
```

打印系统的换行符字符。

## println

```
public abstract void println(boolean x) throws IOException
```

打印一个布尔值，后跟一个换行符。

## println

```
public abstract void println(char x) throws IOException
```

打印一个字符值，后跟一个换行符。

## println

```
public abstract void println(char[] x) throws IOException
```

打印一个字符数组，后跟一个换行符。

## println

```
public abstract void println(double x) throws IOException
```

打印一个双精度浮点数，后跟一个换行符。

## println

```
public abstract void println(float x) throws IOException
```

打印一个单精度浮点数，后跟一个换行符。

## println

```
public abstract void println(int x) throws IOException
```

打印一个整数，后跟一个换行符。

## println

```
public abstract void println(long x) throws IOException
```

打印一个长整数，后跟一个换行符。

## println

```
public abstract void println(Object x) throws IOException
```

打印一个对象，后跟一个换行符。

## println

```
public abstract void println(String x) throws IOException
```

打印一个字符串，后跟一个换行符。

# PageContext

**全名：** `javax.servlet.jsp.PageContext`
**类型：** 抽象类

PageContext 是一个包装对象，它封装了处理单个请求的 JSP 的所有细节。它包含用于初始化和释放会话、写入器、请求和响应对象的方法。它还提供了在 JSP 可访问的各种命名空间中设置和检索属性的方法。

PageContext 对象由 JSPFactory 创建和初始化，当其 `getPageContext()` 方法被调用时创建，当其 `releasePageContext()` 方法被调用时释放。这两个方法调用由 JSP 引擎生成的代码自动执行。

## 构造函数

### PageContext

```
public PageContext()
```

创建一个新的 PageContext 对象。

## 方法

### findAttribute

```
public abstract Object findAttribute(String name)
```

按顺序在页面、请求、会话和应用程序作用域中搜索指定的属性，返回第一个匹配项的值。如果在任何作用域中都不存在该属性，则返回 null。

### forward

```
public abstract void forward(String relativeUrlPath)
    throws ServletException, IOException
```

调用与此 servlet 关联的 `RequestDispatcher` 的 `forward()` 方法。详情请参见 `javax.servlet.RequestDispatcher`。

### getAttribute

```
public abstract Object getAttribute(String name)
```

返回页面作用域中指定的属性，如果属性不存在，则返回 null。

### getAttribute

```
public abstract Object getAttribute(String name, int scope)
```

返回指定作用域中指定的属性，如果属性不存在，则返回 null。作用域选择由以下常量指示：

- PageContext.PAGE_SCOPE
- PageContext.REQUEST_SCOPE
- PageContext.SESSION_SCOPE
- PageContext.APPLICATION_SCOPE

### getAttributeNamesInScope

```
public abstract Enumeration
    getAttributeNamesInScope(int scope)
```

返回指定作用域中属性名称的 `Enumeration`。作用域值列表请参见 `getAttribute(String name, int scope)`。

### getAttributesScope

```
public abstract int getAttributesScope(String name)
```

返回具有指定名称的第一个属性的作用域。作用域值列表请参见 `getAttribute(String name, int scope)`。

### getException

```
public abstract Exception getException()
```

返回传递给 ErrorPage 的 Exception 对象。

### getOut

```
public abstract JspWriter getOut()
```

返回此响应的 JspWriter。

### getPage

```
public abstract Object getPage()
```

返回与此 PageContext 关联的 servlet。

### getRequest

```
public abstract ServletRequest getRequest()
```

返回与此 PageContext 关联的 ServletRequest。

### getResponse

```
public abstract ServletResponse getResponse()
```

返回与此 PageContext 关联的 ServletResponse。

### getServletConfig

```
public abstract ServletConfig getServletConfig()
```

返回与此 PageContext 关联的 ServletConfig。

### getServletContext

```
public abstract ServletContext getServletContext()
```

返回与此 `PageContext` 关联的 `ServletContext`。

### getSession

```
public abstract HttpSession getSession()
```

返回此请求的 `HttpSession`，如果不存在会话，则返回 null。

### handlePageException

```
public abstract void handlePageException(Exception e) throws ServletException, IOException;
```

用于处理当前页面抛出的未处理异常。如果存在活动的 `ErrorPage`，则调用它。

> **注意** 虽然此方法未被弃用，但 `handlePageException(Throwable t)` 更通用，应使用此方法代替该方法。

### handlePageException

```
public abstract void handlePageException(Throwable t) throws ServletException, IOException
```

用于处理当前页面抛出的未处理异常。如果存在活动的 `ErrorPage`，则调用它。

### include

```
public abstract void include(String relativeUrlPath) throws ServletException, IOException
```

调用与此 servlet 关联的 `RequestDispatcher` 的 `include()` 方法。详情请参见 `javax.servlet.RequestDispatcher`。

# JSP：完整参考

## initialize

```
public abstract void initialize(
    Servlet servlet,
    ServletRequest request,
    ServletResponse response,
    String errorPageURL,
    boolean needsSession,
    int bufferSize,
    boolean autoFlush)
  throws IOException, IllegalStateException,
    IllegalArgumentException
```

存储 `servlet`、`request`、`response`、`errorPageURL`、`needsSession`、`bufferSize` 和 `autoFlush` 属性，并使相应的隐式变量对 JSP 可用。此方法由 `getPageContext()` 方法调用，不应由 JSP 作者直接调用。

## popBody

```
public JspWriter popBody()
```

恢复由先前的 `pushBody()` 保存的 `JspWriter`，并更新 `out` 隐式变量和 PageContext "out" 属性的值。

## pushBody

```
public BodyContent pushBody()
```

保存当前的 `JspWriter` 并创建一个新的 `BodyContent` 对象，使其成为 PageContext "out" 属性和 `out` 隐式变量的值。

## release

```
public abstract void release()
```

执行 `initialize` 的反向操作，释放 PageContext 及其获取的资源。此方法由 `releasePageContext()` 方法调用，不应由 JSP 作者直接调用。



## removeAttribute

```java
public abstract void removeAttribute(String name)
```

按页面、请求、会话和应用程序作用域（按此顺序）搜索指定属性，并移除第一个匹配的属性。

## removeAttribute

```java
public abstract void removeAttribute(String name, int scope)
```

移除与指定名称和作用域关联的属性。作用域选择通过以下常量指示：

- `PageContext.PAGE_SCOPE`
- `PageContext.REQUEST_SCOPE`
- `PageContext.SESSION_SCOPE`
- `PageContext.APPLICATION_SCOPE`

## setAttribute

```java
public abstract void setAttribute(String name, Object attribute)
```

设置具有页面作用域的指定属性。`setAttribute(String name, Object o, int scope)` 可用于在其他作用域中设置属性。

## setAttribute

```java
public abstract void setAttribute(String name, Object o, int scope)
```

设置与指定名称和作用域关联的属性。作用域选择通过以下常量指示：

- `PageContext.PAGE_SCOPE`
- `PageContext.REQUEST_SCOPE`
- `PageContext.SESSION_SCOPE`
- `PageContext.APPLICATION_SCOPE`

## 包 javax.servlet.jsp.tagext

### BodyContent

| 全名 | `javax.servlet.jsp.tagext.BodyContent` |
| :--- | :--- |
| 类型 | 抽象类 |
| 继承自 | `javax.servlet.jsp.JspWriter` |

`BodyContent` 是 `javax.servlet.jsp.JspWriter` 的子类，但与它的超类不同，其内容不会自动写入 servlet 输出流。相反，它们会被累积在一个相当于字符串缓冲区的地方。在标签体完成后，原始的 `JspWriter` 会被恢复，但 `BodyContent` 对象在 `doEndTag()` 的 `bodyContent` 变量中仍然可用。其内容可以通过 `getString()` 或 `getReader()` 方法检索，根据需要进行修改，然后写入恢复的 `JspWriter` 输出流，与页面输出合并。

### 方法

#### clearBody

```java
public void clearBody()
```

将 `BodyContent` 缓冲区重置为空。如果在 `doAfterBody()` 中将正文写入外围的 writer，这可能很有用。

#### flush

```java
public void flush() throws IOException
```

重写 `JspWriter.flush()` 方法，使其始终抛出异常。刷新 `BodyContent` writer 是无效的，因为它没有连接到可以写入的实际输出流。

#### getEnclosingWriter

```java
public JspWriter getEnclosingWriter()
```

返回堆栈中上一层的 writer 对象（可能是另一个 `BodyContent`）。

#### getReader

```java
public abstract Reader getReader()
```

在正文内容被求值后，返回一个用于读取它的 reader。可以将此 reader 传递给其他可以处理 `java.io.Reader` 的类，例如 `StreamTokenizer`、`FilterReader` 或 XML 解析器。

#### getString

```java
public abstract String getString()
```

在正文内容被求值后，返回包含该内容的字符串。

#### writeOut

```java
public abstract void writeOut(Writer out) throws IOException
```

将正文内容写入指定的输出 writer。

### BodyTag

| 全名 | `javax.servlet.jsp.tagext.BodyTag` |
| :--- | :--- |
| 类型 | 接口 |
| 父接口 | `javax.servlet.jsp.tagext.IterationTag` |

`IterationTag` 接口的扩展，增加了与正文处理相关的新方法。

#### doInitBody

```java
public void doInitBody() throws JspException
```

在 `setBodyContent()` 之后、正文被求值之前调用的生命周期方法。如果正文被多次求值，此方法只被调用一次。

#### setBodyContent

```java
public void setBodyContent(BodyContent b)
```

由 JSP servlet 在当前 `JspWriter` 被推入栈并且新的 `BodyContent` writer 被创建后调用。这发生在 `doStartTag()` 之后。

### BodyTagSupport

| 全名 | `javax.servlet.jsp.tagext.BodyTagSupport` |
| :--- | :--- |
| 类型 | 类 |
| 继承自 | `javax.servlet.jsp.tagext.TagSupport` |
| 实现 | `javax.servlet.jsp.tagext.BodyTag` |

一个有用的基类，实现了 `BodyTag` 的所有方法。标签处理器可以扩展 `BodyTagSupport`，只重写那些需要更改的方法。

#### 构造函数

##### BodyTagSupport

```java
public BodyTagSupport()
```

创建一个新的 `BodyTagSupport` 对象。

#### 方法

##### doAfterBody

```java
public int doAfterBody() throws JspException
```

在每次正文求值结束时调用。默认返回 `Tag.SKIP_BODY`。如果你重写此方法，应该返回 `Tag.SKIP_BODY` 或 `IterationTag.EVAL_BODY_AGAIN`。

##### doEndTag

```java
public int doEndTag() throws JspException
```

在自定义标签的作用域结束时调用。默认返回 `EVAL_PAGE`，但可以通过实现返回 `SKIP_PAGE` 来重写。

##### doInitBody

```java
public void doInitBody() throws JspException
```

在 `setBodyContent()` 之后、正文被求值之前调用的生命周期方法。如果正文被多次求值，此方法只被调用一次。默认实现不执行任何操作。

##### doStartTag

```java
public int doStartTag() throws JspException
```

参见 `Tag` 接口中的 `doStartTag()`。此实现返回 `EVAL_BODY_BUFFERED`。

##### getBodyContent

```java
public BodyContent getBodyContent()
```

返回当前的 `BodyContent`。

##### getPreviousOut

```java
public JspWriter getPreviousOut()
```

返回外围的 `JspWriter`。

##### release

```java
public void release()
```

释放标签处理器的状态。

##### setBodyContent

```java
public void setBodyContent(BodyContent b)
```

存储对 `BodyContent` 对象的引用。

### IterationTag

| 全名 | `javax.servlet.jsp.tagext.IterationTag` |
| :--- | :--- |
| 类型 | 接口 |
| 父接口 | `javax.servlet.jsp.tagext.Tag` |

`Tag` 接口的扩展，定义了重复求值标签体的语义。

#### doAfterBody

```java
public int doAfterBody() throws JspException
```

在正文被求值之后，但 `BodyContent` writer 仍然活跃时调用的生命周期方法。此方法必须返回 `EVAL_BODY_AGAIN` 或 `SKIP_BODY`。如果返回码是 `EVAL_BODY_AGAIN`，正文将再次被求值，并且 `doAfterBody()` 将被再次调用。

### PageData

| 全名 | `javax.servlet.jsp.tagext.PageData` |
| :--- | :--- |
| 类型 | 抽象类 |

一个可以在 TLD 中列为 JSP 页面验证器的类。提供了一种读取与 JSP 页面对应的 XML 文档的方法。

#### 构造函数

##### PageData

```java
public PageData()
```

创建一个新的 `PageData` 对象。

#### 方法

##### getInputStream

```java
public abstract InputStream getInputStream()
```

将 JSP 页面作为 XML 文档返回。

### Tag

| 全名 | `javax.servlet.jsp.tagext.Tag` |
| :--- | :--- |
| 类型 | 接口 |

一组生命周期方法，必须由自定义标签处理器实现。

#### doEndTag

```java
public int doEndTag() throws JspException
```

在遇到结束标签时调用。返回码指示 JSP 实现 servlet 是否应继续页面的剩余部分（`EVAL_PAGE`）或不（`SKIP_PAGE`）。此方法可以抛出 `JspException` 以指示致命错误。

#### doStartTag

```java
public int doStartTag() throws JspException
```

在页面上下文、父标签以及开始标签上编码的任何属性设置之后调用。返回码指示 JSP 实现 servlet 是否应求值标签体（`EVAL_BODY_INCLUDE` 或 `BodyTag.EVAL_BODY_BUFFERED`）或不（`SKIP_BODY`）。此方法可以抛出 `JspException` 以指示致命错误。`BodyTag.EVAL_BODY_BUFFERED` 仅在标签处理器实现了 `BodyTag` 时有效。

#### getParent

```java
public Tag getParent()
```

返回父标签（最近的外围标签处理器），如果没有父标签则返回 null。

#### release

```java
public void release()
```

保证在页面退出前调用。允许标签处理器释放它持有的任何资源并重置其状态，以便在必要时可以重用。

#### setPageContext

```java
public void setPageContext(PageContext pc)
```

生成的 servlet 在要求处理器执行任何其他操作之前首先调用此方法。实现类应该保存上下文变量，以便在标签生命周期的任何点都可用。通过页面上下文，标签处理器可以访问所有 JSP 隐式对象，并且可以获取和设置任何作用域中的属性。

#### setParent

```java
public void setParent(Tag t)
```

设置父标签。使标签处理器能够在求值堆栈中找到它上方的标签。在 `setPageContext` 之后立即调用。

### TagAttributeInfo

| 全名 | `javax.servlet.jsp.tagext.TagAttributeInfo` |
| :--- | :--- |
| 类型 | 类 |

一个描述标签属性信息的类，在翻译时可用。



## 构造方法

## TagAttributeInfo

```java
public TagAttributeInfo(
    String name,
    boolean required,
    String type,
    boolean reqTime)
```

创建一个新的 TagAttributeInfo 实例。旨在仅从 TagLibrary 对象中的代码调用。

## 方法

## canBeRequestTime

```java
public boolean canBeRequestTime()
```

如果此属性可以持有请求时值，则返回 true。

## getIdAttribute

```java
public static TagAttributeInfo getIdAttribute(TagAttributeInfo[] a)
```

一个工具方法，用于在 TagAttributeInfo 对象数组中搜索名为 "id" 的属性。

## getName

```java
public String getName()
```

返回属性名称。

## getTypeName

```java
public String getTypeName()
```

以字符串形式返回属性类型。

## isRequired

```java
public boolean isRequired()
```

如果属性是必需的，则返回 true。

## toString

```java
public String toString()
```

返回格式化为字符串的对象表示。

## TagData

| 全名： | `javax.servlet.jsp.tagext.TagData` |
| :--- | :--- |
| 类型： | 类 |
| 实现接口： | `java.lang.Cloneable` |

包含关于标签属性的翻译时信息。仅供 JSP 容器使用。

## 构造方法

### TagData

```java
public TagData(Hashtable attrs)
```

从哈希表创建一个新的 TagData 对象。

### TagData

```java
public TagData(Object[][] atts)
```

从属性/值对的二维数组创建一个新的 TagData 对象。

## 方法

### getAttribute

```java
public Object getAttribute(String attName)
```

返回具有指定名称的属性。如果值必须在请求时指定，也可以返回 REQUEST_TIME_VALUE，如果标签中未指定该属性，则返回 null。

### getAttributes

```java
public Enumeration getAttributes()
```

返回属性的枚举。

### getAttributeString

```java
public String getAttributeString(String attName)
```

以字符串形式返回属性的值对象。

### getId

```java
public String getId()
```

如果已指定，返回 id 属性的值。

### setAttribute

```java
public void setAttribute(String attName, Object value)
```

将属性设置为指定的值。

## TagExtraInfo

**全名：** `javax.servlet.jsp.tagext.TagExtraInfo`

**类型：** 抽象类

需要定义变量或对其属性执行验证的标签，必须定义一个继承自 TagExtraInfo 类的类。此子类在标签库描述符中与自定义标签关联。

## 构造方法

### TagExtraInfo

```java
public TagExtraInfo()
```

创建一个新的 TagExtraInfo 对象。

## 方法

### getTagInfo

```java
public final TagInfo getTagInfo()
```

返回此类的 TagInfo。

### getVariableInfo

```java
public VariableInfo getVariableInfo(TagData data)
```

基于 data 参数中的属性名和值列表，构建一个 VariableInfo 对象数组，描述每个要创建的脚本变量的名称、类型、存在性和作用域。

### isValid

```java
public boolean isValid(TagData data)
```

如果 TagData 参数中引用的属性有效，则返回 true。

### setTagInfo

```java
public final void setTagInfo(TagInfo tagInfo)
```

设置此类的 TagInfo。

## TagInfo

**全名：** `javax.servlet.jsp.tagext.TagInfo`

**类型：** 类

标签库描述符中标签元素的对象表示。

## 构造方法

### TagInfo

```java
public TagInfo(
    String tagName,
    String tagClassName,
    String bodycontent,
    String infoString,
    TagLibraryInfo taglib,
    TagExtraInfo tagExtraInfo,
    TagAttributeInfo attributeInfo)
```

从 JSP 1.1 格式的标签库描述符创建一个新的 TagInfo 对象。

### TagInfo

```java
public TagInfo(
    String tagName,
    String tagClassName,
    String bodycontent,
    String infoString,
    TagLibraryInfo taglib,
    TagExtraInfo tagExtraInfo,
    TagAttributeInfo attributeInfo,
    String displayName,
    String smallIcon,
    String largeIcon,
    TagVariableInfo tvi)
```

从 JSP 1.2 格式的标签库描述符创建一个新的 TagInfo 对象。

## 方法

### getAttributes

```java
public TagAttributeInfo[] getAttributes()
```

返回描述此标签属性的数组，如果没有属性，则返回 `null`。

### getBodyContent

```java
public String getBodyContent()
```

返回标签库描述符中指定的此标签的 `bodycontent` 属性。

### getDisplayName

```java
public String getDisplayName()
```

返回标签库描述符中指定的此标签的 `displayName` 属性。

### getInfoString

```java
public String getInfoString()
```

返回标签库描述符中指定的此标签的 `info` 元素。

### getLargeIcon

```java
public String getLargeIcon()
```

返回标签库描述符中指定的此标签的大图标路径。

### getSmallIcon

```java
public String getSmallIcon()
```

返回标签库描述符中指定的此标签的小图标路径。

### getTagClassName

```java
public String getTagClassName()
```

返回标签处理程序类的名称。

### getTagExtraInfo

```java
public TagExtraInfo getTagExtraInfo()
```

返回标签额外信息类的名称。

### getTagLibrary

```java
public TagLibraryInfo getTagLibrary()
```

返回此标签的 TagLibraryInfo 对象的引用。

### getTagName

```java
public String getTagName()
```

返回标签名称。

### getTagVariableInfos

```java
public TagVariableInfo getTagVariableInfos()
```

返回与此 TagInfo 关联的 TagVariableInfo 对象。

### getVariableInfo

```java
public VariableInfo getVariableInfo(TagData data)
```

返回此标签的 VariableInfo 对象的引用。

### isValid

```java
public boolean isValid(TagData data)
```

返回关联的 `TagExtraInfo` 类的 `isValid()` 方法的求值结果。

### setTagExtraInfo

```java
public void setTagExtraInfo(TagExtraInfo tei)
```

存储对此标签的 `TagExtraInfo` 的引用。

### setTagLibrary

```java
public void setTagLibrary(TagLibraryInfo tl)
```

设置 `TagLibraryInfo` 属性。

### toString

```java
public String toString()
```

返回用于调试的对象字符串表示。

## TagLibraryInfo

**全名：** `javax.servlet.jsp.tagext.TagLibraryInfo`

**类型：** 抽象类

封装与 taglib 指令及其底层标签库描述符（TLD）关联信息的类。

## 方法

### getInfoString

```java
public String getInfoString()
```

从 TLD 返回 `info` 属性。

### getPrefixString

```java
public String getPrefixString()
```

返回在 taglib 指令中分配的前缀。

### getReliableURN

```java
public String getReliableURN()
```

从 TLD 返回 reliableURL 属性。

### getRequiredVersion

```java
public String getRequiredVersion()
```

返回所需的 JSP 容器版本。

### getShortName

```java
public String getShortName()
```

从 TLD 返回 short name 属性。

### getTag

```java
public TagInfo getTag(String shortname)
```

返回与给定标签名称关联的 TagInfo 对象。

### getTags

```java
public TagInfo[] getTags()
```

返回此标签库中定义的所有标签的 TagInfo 对象数组。

### getURI

```java
public String getURI()
```

返回 taglib 指令中 uri 属性的值。

## 附录 B：JSP API 版本 1.2

## TagLibraryValidator

**全名：** `javax.servlet.jsp.tagext.TagLibraryValidator`

**类型：** 抽象类

一个验证器类，可以在 TLD 中与 JSP 页面关联。验证器对 JSP 页面的 XML 文档表示进行操作。

## 构造方法

### TagLibraryValidator

```java
public TagLibraryValidator()
```

创建一个新的 TagLibraryValidator。

## 方法

### getInitParameters

```java
public Map getInitParameters()
```

返回初始化参数。

### release

```java
public void release()
```

释放此验证器使用的验证数据。

### setInitParameters

```java
public void setInitParameters(Map map)
```

向验证器提供初始化键/值参数。

### validate

```java
public String validate(String prefix, String uri, PageData page)
```

验证 JSP 页面。如果页面有效，则返回 null。



## TagSupport

**全名：** javax.servlet.jsp.tagext.TagSupport
**类型：** 类
**实现接口：** javax.servlet.jsp.tagext.IterationTag
    java.io.Serializable

Tag 接口的具体实现。标签处理器可以继承此类，并仅需实现那些需要修改的方法。

## 构造函数

### TagSupport

```java
public TagSupport()
```

创建一个新的 TagSupport 对象。

## 方法

### doAfterBody

```java
public int doAfterBody() throws JspException
```

在标签体被求值后调用。

### doEndTag

```java
public int doEndTag() throws JspException
```

当遇到结束标签时调用。返回码指示 JSP 实现 servlet 是应该继续处理页面的其余部分（EVAL_PAGE）还是不继续（SKIP_PAGE）。该方法可以抛出 JspException 以指示致命错误。TagSupport 的实现返回 EVAL_PAGE。

### doStartTag

```java
public int doStartTag() throws JspException
```

在页面上下文、父标签以及起始标签上编码的任何属性都已设置后调用。返回码指示 JSP 实现 servlet 是应该对标签体求值（EVAL_BODY_INCLUDE 或 BodyTag.EVAL_BODY_BUFFERED）还是不对标签体求值（SKIP_BODY）。该方法可以抛出 JspException 以指示致命错误。BodyTag.EVAL_BODY_BUFFERED 仅在标签处理器实现了 BodyTag 时才有效。TagSupport 的实现返回 SKIP_BODY。

### findAncestorWithClass

```java
public static final Tag findAncestorWithClass
(Tag from, Class klass)
```

在父标签栈中搜索指定类的最近标签处理器。这使得“内部”标签能够访问其外层标签中的信息。

### getId

```java
public String getId()
```

返回此标签的 id 属性值。

### getParent

```java
public Tag getParent()
```

返回此标签处理器实例的直接父标签。

### getValue

```java
public Object getValue(String k)
```

返回在此标签处理器下按给定名称存储的对象。

### getValues

```java
public Enumeration getValues()
```

返回在此标签处理器中存储的值的名称的枚举。

### release

```java
public void release()
```

保证在页面退出前被调用。使标签处理器能够释放其持有的任何资源并重置其状态，以便在必要时可以重用。

### removeValue

```java
public void removeValue(String k)
```

如果存在，则删除在此标签处理器下按指定名称存储的值。

### setId

```java
public void setId(String id)
```

设置此标签的 `id` 属性。

### setPageContext

```java
public void setPageContext(PageContext pageContext)
```

生成的 servlet 在要求处理器执行任何其他操作之前首先调用此方法。实现类应保存上下文变量，以便在标签生命周期的任何时刻都可以访问它。通过页面上下文，标签处理器可以访问所有 JSP 隐式对象，并可以在任何作用域中获取和设置属性。

### setParent

```java
public void setParent(Tag t)
```

设置父标签。使标签处理器能够找到求值栈中其上方的标签。在 `setPageContext` 之后立即调用。

### setValue

```java
public void setValue(String k, Object o)
```

在标签处理器中将对象按指定名称存储。

## TagVariableInfo

| 全名 | javax.servlet.jsp.tagext.TagVariableInfo |
| :--- | :--- |
| 类型 | 类 |

一个封装了从标签库中提取的标签变量信息的类。

## 构造函数

### TagVariableInfo

```java
public TagVariableInfo(
    String nameGiven,
    String nameFromAttribute,
    String className,
    boolean declare,
    int scope)
```

创建一个新的 TagVariableInfo 对象。

## 方法

### getClassName

```java
public String getClassName()
```

返回 TLD 中 `<variable-class>` 元素的值。

### getDeclare

```java
public boolean getDeclare()
```

返回 TLD 中 `<declare>` 元素的值。

### getNameFromAttribute

```java
public String getNameFromAttribute()
```

返回 TLD 中 `<name-from-attribute>` 元素的值。

### getNameGiven

```java
public String getNameGiven()
```

返回 TLD 中 `<name-given>` 元素的值。

### getScope

```java
public int getScope()
```

返回 TLD 中 `<scope>` 元素的值。

## TryCatchFinally

**全名：** javax.servlet.jsp.tagext.TryCatchFinally
**类型：** 接口

一个可由标签处理器实现的额外接口，使其能够在标签调用的 `catch` 和 `finally` 块中被调用。

## 方法

### doCatch

```java
public void doCatch(Throwable t) throws Throwable
```

如果在对标签体求值时发生异常，则在 `catch` 块中调用此方法。

### doFinally

```java
public void doFinally()
```

如果在对标签体求值时发生异常，则在 `finally` 块中调用此方法。

## VariableInfo

**全名：** javax.servlet.jsp.tagext.VariableInfo
**类型：** 类

一个提供有关自定义标签创建的脚本变量的配置信息的数据结构。主要在 TagExtraInfo 子类的 `getVariableInfo()` 方法中使用。

## 构造函数

### VariableInfo

```java
public VariableInfo(
    String varName,
    String className,
    boolean declare,
    int scope)
```

创建一个新的 `VariableInfo` 对象。参数如下：

- **varName**：要创建的变量的名称
- **className**：变量类的完全限定名
- **declare**：一个布尔值，如果生成的 servlet 应包含该变量的声明，则为 `true`
- **scope**：一个表示变量作用域的整数。可以是 `AT_BEGIN`、`AT_END` 或 `NESTED`。

## 方法

### getClassName

```java
public String getClassName()
```

返回类名。

### getDeclare

```java
public boolean getDeclare()
```

返回表示是否应声明变量的布尔属性。

### getScope

```java
public int getScope()
```

返回表示变量作用域的整数。

### getVarName

```java
public String getVarName()
```

返回变量名。

## 完整参考

## 附录 C

### HTTP 参考

版权所有 2001 McGraw-Hill Companies, Inc. 点击此处查看使用条款。

本附录包含两个表格，一个描述超文本传输协议（HTTP）响应代码，另一个描述 HTTP 头。有关 HTTP 的更多详细信息，请参阅规范 RFC 2616。

## HTTP 响应代码

响应代码是出现在 HTTP 服务器发送的响应第一行的三位数字代码。响应代码分为五类，由其第一位数字表示：

- **1xx：信息性** 已接收请求，正在继续处理
- **2xx：成功** 操作已成功接收、理解和接受
- **3xx：重定向** 必须采取进一步操作才能完成请求
- **4xx：客户端错误** 请求包含错误语法或无法满足
- **5xx：服务器错误** 服务器未能满足一个明显有效的请求

下表列出了各个代码及其含义：

| 响应代码 | 含义 |
| :--- | :--- |
| 100 | 继续 |
| 101 | 切换协议 |
| 200 | 确定 |
| 201 | 已创建 |
| 202 | 已接受 |
| 203 | 非权威性信息 |
| 204 | 无内容 |
| 205 | 重置内容 |
| 206 | 部分内容 |
| 300 | 多种选择 |
| 301 | 永久移动 |
| 302 | 已找到 |
| 303 | 参见其他 |
| 304 | 未修改 |
| 305 | 使用代理 |
| 307 | 临时重定向 |
| 400 | 错误请求 |
| 401 | 未授权 |
| 402 | 需要付费 |
| 403 | 禁止 |
| 404 | 未找到 |
| 405 | 方法不允许 |
| 406 | 不可接受 |
| 407 | 需要代理身份验证 |
| 408 | 请求超时 |
| 409 | 冲突 |
| 410 | 已删除 |
| 411 | 需要长度 |
| 412 | 前提条件失败 |
| 413 | 请求实体过大 |
| 414 | 请求 URI 过长 |
| 415 | 不支持的媒体类型 |
| 416 | 请求的范围不满足 |
| 417 | 未满足期望 |
| 500 | 内部服务器错误 |
| 501 | 未实现 |
| 502 | 错误网关 |
| 503 | 服务不可用 |
| 504 | 网关超时 |
| 505 | 不支持 HTTP 版本 |



## HTTP 头部

头部是描述客户端或服务器属性、传输资源以及连接操作方式的键值对。存在四种不同类型的头部：

- **通用头部** 可以在请求或响应中使用，与整个事务相关，而非特定资源。
- **请求头部** 允许客户端传递关于自身的信息以及期望的响应形式。
- **响应头部** 由服务器用于传递关于自身和响应的信息。
- **实体头部** 定义被传输资源的信息。可以在请求或响应中使用。

头部以单行文本形式发送，格式为

```
<name>: <value><CRLF>
```

其中

name 是头部名称，不区分大小写；
value 是头部值；
CRLF 是回车符/换行符。

注意，名称和值之间用冒号和一个或多个空格分隔。JSP 页面可以使用其 `request` 对象的 `getHeader()` 方法读取 HTTP 头部，并使用 `response.setHeader()` 写入头部。`java.net.URLConnection` 提供了类似的方法来访问 URL 流中的头部。

下表描述了 HTTP/1.1 中可用的头部：

| 头部 | 描述 |
| :--- | :--- |
| Accept | 指定客户端能够处理的媒体类型，按偏好顺序排列。可以在逗号分隔的列表中指定多个类型。允许使用通配符。示例：`Accept: image/jpeg, image/pjpeg, image/png, */*` |
| Accept-Charset | 指定客户端能够处理的字符集，按偏好顺序排列。可以在逗号分隔的列表中指定多个类型。允许使用通配符。示例：`Accept-Charset: iso-8859-1, *, utf-8` |
| Accept-Encoding | 指定客户端理解的编码机制。示例：`Accept-Encoding: gzip, compress` |
| Accept-Language | 指定客户端首选的自然语言列表。示例：`Accept-Language: en, de` |
| Accept-Ranges | 一个响应头部，允许服务器指示它将接受请求资源的给定偏移量和长度的部分内容。头部的值是范围请求所理解的度量单位。示例：`Accept-Ranges: bytes` `Accept-Ranges: none` |
| Age | 允许服务器指定自响应在服务器上生成以来经过的秒数。此头部主要用于缓存响应。示例：`Age: 30` |
| Allow | 一个响应头部，指定请求 URI 中资源支持的 HTTP 方法列表。示例：`Allow: GET, HEAD, PUT` |
| Authorization | 一个请求头部，用于指定访问资源所需的凭据（领域和编码的用户 ID 及密码）。示例：`Authorization: Basic YXV0aG9yOnBoaWw=` |
| `Cache-Control` | 一个通用头部，用于指定缓存指令。示例：`Cache-Control: max-age=30` |
| `Connection` | 一个通用头部，用于指示是否保持套接字连接打开。示例：`Connection: close`, `Connection: keep-alive` |
| `Content-Base` | 一个实体头部，指定用于解析实体内相对 URL 的基础 URI。如果未指定 Content-Base 头部，则使用 Content-Location URI（如果存在且是绝对的）或使用请求 URI 来解析相对 URL。示例：`Content-Base: http://www.lyricnote.com` |
| `Content-Encoding` | 媒体类型的修饰符，指示实体的编码方式（如压缩、压缩等）。示例：`Content-Encoding: gzip` |
| `Content-Language` | 用于指定输入流中数据的自然语言。示例：`Content-Language: en` |
| `Content-Length` | 指定请求或响应中包含的数据的长度（以字节为单位）。示例：`Content-Length: 382` |
| `Content-Location` | 指定请求或响应中包含资源的位置（URI）。如果这是一个绝对 URL，它也作为解析实体中相对 URL 的基础。示例：`Content-Location: http://www.lyricnote.com/newsletter` |
| Content-MD5 | 实体主体的 MD5 摘要，用作校验和。发送方和接收方都计算 MD5 摘要。接收方将计算出的值与此头部中传输的值进行比较。示例：`Content-MD5: <base64 of 128 bit MD5 digest>` MD5 在 RFC 1321 中描述。 |
| Content-Range | 与部分实体主体一起发送；指示要插入部分的字节偏移量（低和高）。还指示实体主体的总长度。示例：`Content-Range: 1001-2000/5000` |
| Content-Type | 指示发送或接收的实体主体的 MIME 类型。示例：`Content-Type: text/html` |
| Date | 发送 HTTP 消息的日期。示例：`Date: Mon, 06 Mar 2000 18:42:51 GMT` |
| ETag | 一个实体头部，为发送的资源分配唯一标识符。对于可以使用多个 URL 请求的资源，ETag 可用于确定是否实际发送了相同的资源。示例：`ETag: "208f-419e-30f8dc99"` |
| Expires | 指定实体应被视为过期的日期。示例：`Expires: Mon, 05 Dec 2008 12:00:00 GMT` |
| From | 一个请求头部，给出控制用户代理的人类用户的电子邮件地址。示例：`From: webmaster@lyricnote.com` |
| Host | 所请求资源的主机名（以及可选的端口号）。对于使用 HTTP/1.1 发出的请求，此字段是必需的。示例：`Host: www.lyricnote.com` |
| If-Modified-Since | 如果包含在 GET 请求中，使请求取决于资源的最后修改日期。如果此头部存在且资源自指定日期以来未被修改，则应返回 304（未修改）响应。示例：`If-Modified-Since: Wed, 01 Mar 2000 12:00:00 GMT` |
| If-Match | 如果包含在请求中，指定一个或多个实体标签（参见 ETag）。仅当其 ETag 与列表中的一个匹配时，才会发送资源。示例：`If-Match: "208f-419e-30f8dc99"` |
| If-None-Match | 如果包含在请求中，指定一个或多个实体标签（参见 ETag）。仅当资源的 ETag 与列表中的任何条目都不匹配时，才会执行操作。示例：`If-None-Match: "208f-419e-30f8dc99"` |
| If-Range | 指定客户端已拥有副本的资源的实体标签（参见 ETag）。必须与 Range 头部一起使用。如果实体自客户端上次检索以来未被修改，服务器将仅发送指定的范围，否则将发送整个资源。示例：`Range: bytes=0-499` `If-Range: "208f-419e-30f8dc99"` |
| If-Unmodified-Since | 类似于 If-Modified-Since，但意义相反。仅当请求的实体自指定日期以来未被修改时才返回。示例：`If-Unmodified-Since: Wed, 01 Mar 2000 12:00:00 GMT` |
| Last-Modified | 指定请求资源最后修改的日期和时间。示例：`Last-Modified: Wed, 08 Mar 2000 12:00:00 GMT` |
| Location | 用于将请求者重定向到另一个位置以获取已移动的资源。与 302（临时移动）或 301（永久移动）状态码结合使用。示例：`Location: http://www2.lyricnote.com/index.jsp` |
| Max-Forwards | 一个请求头部，与 TRACE 方法一起使用，指定请求可以路由通过的代理或网关的最大数量。代理或网关应在传递请求前递减该数量。示例：`Max-Forwards: 3` |
| Pragma | 一个通用头部，发送特定于实现的信息。示例：`Pragma: no-cache` |
| Proxy-Authenticate | 类似于 WWW-Authenticate，但设计为仅从请求链中的下一个服务器（代理）请求身份验证。示例：`Proxy-Authenticate: Basic realm=Admin` |
| Proxy-Authorization | 类似于 Authorization，但并非设计用于传递到直接服务器链中的代理服务器之外。示例：`Proxy-Authorization: Basic YXV0aG9yOnBoaWw=` |
| Public | 列出服务器支持的方法集。示例：`Public: OPTIONS, MGET, MHEAD, GET, HEAD` |



# 842 JSP：完整参考手册

| 头字段 | 描述 |
| :--- | :--- |
| Range | 指定一个度量单位和一个偏移范围，用于请求部分资源。示例：`Range: bytes=206-5513` |
| Referer | 一个（拼写错误的）请求头字段，指示发起请求的原始资源。对于 HTML 表单，它是包含该表单的网页地址。示例：`Referer: http://www.lyricnote.com/product/search.html` |
| Retry-After | 一个由服务器在 503（服务不可用）状态码时发送的响应头字段，用于指示在再次请求资源之前需要等待多长时间。时间可以是日期或秒数。示例：`Retry-After: 18` `Retry-After: Thu, 09 Mar 2014 16:45:15 GMT` |
| Server | 一个响应头，指示 Web 服务器软件的标识和版本号。示例：`Server: Apache/1.3.12 (Win32)` |
| Transfer-Encoding | 一个通用头字段，指示对消息体执行的转换类型，接收方应将其逆转。示例：`Transfer-Encoding: chunked` |
| Upgrade | 允许服务器指定新协议或协议版本。与 101（切换协议）响应码结合使用。示例：`Upgrade: HTTP/2.0` |

# 附录 C：HTTP 参考

843

| 头字段 | 描述 |
| :--- | :--- |
| User-Agent | 指定用于发起请求的软件类型（通常是 Web 浏览器）。示例：`User-Agent: Mozilla/4.0 (compatible; MSIE 5.5; Windows NT; DigExt)` `User-Agent: Mozilla/4.7 [en] (WinNT; I)` |
| Vary | 一个响应头字段，用于指示响应实体是从可用的响应表示中通过服务器驱动协商选择的。示例：`Vary: *` |
| Via | 一个通用头字段，包含用于满足请求的所有中间主机和协议的列表。示例：`Via: 1.0 fred.com, 1.1 wilma.com` |
| Warning | 一个响应头字段，用于提供关于响应状态的附加信息。示例：`Warning: 99 www.lyricnote.com Piano needs tuning` |
| WWW-Authenticate | 一个响应头字段，向用户代理提出质询，要求提供用户 ID 和密码。与 401（未授权）状态码结合使用。期望在回复中包含一个 Authorization 头字段。示例：`WWW-Authenticate: Basic realm=lyricnote_mgmt` |

此页有意留白。

# 索引

## 符号

`<%@include%>` 指令。*参见* include 指令

`<%` 和 `%>` 标记，90, 91

## A

accept 属性，267

accept-charset 属性，267

action 属性，263, 264

action 类，660–662

- CustomerNewProblemAction，669–670
- CustomersListSelectAction，667–668
- CustomersSearchAction，666–667
- ProblemSubmitAction，674–675
- ProductsListSelectAction，671–672
- ProductsSearchAction，670–671
- ProductsSelectAction，672–673

动作

- `<jsp:include>`，83–84
- 标准动作的语法，75–77, 83–84

Active Server Pages (ASP)，704

addCookie 方法，777, 780

addDateHeader 方法，777, 780

addHeader 方法，777, 781

addIntHeader 方法，777, 781

用于天气信息的机场选择，444–448

小程序

- 作为客户端，689–695
- 演变，689

应用程序对象

- application 隐式对象，98, 103–104
- 在案例研究的 Model 类中，588–615
- 产品支持应用中的 Util 类，613–615
- 产品支持应用中的 WebModel 类，611–613

Web 应用的应用程序根目录，530, 531

应用程序作用域，412–413

application/x-www-form-urlencoded 编码技术，265–266

应用程序

- Web 应用程序的定义，530
- Web 应用程序的目录结构，530-532
- Web 编程模型的演变，6-9
- 流程与视图/控制器交互，631-633
- 多线程应用程序中的身份验证请求处理，407-410
- Java 应用程序作为客户端，684-689
- 将特性映射到 HTTP 环境，411-413
- Number Guess Guesser，360, 374-378
- 从应用程序发送电子邮件的选项，710
- 用于 Price Quote 客户端，687-689
- 从客户端到服务器端的转变，9
- 另请参见 LyricNote.com 示例应用程序；产品支持应用程序

架构

- JDBC 驱动程序类型，304
- Model 1 与 Model 2 开发，159-160
- 另请参见 MVC 系统架构

ASCII_markersTable JSP，93

ASP (Active Server Pages)，704

attributeAdded 方法，737, 787

attributeRemoved 方法，737, 787

attributeReplaced 方法，737, 788

属性

- 为自定义标签定义，186
- 定义标签属性，212-219
- 在 DTD 中，456, 457
- FORM 元素的属性，264-268
- `<jsp:setProperty>` 标签的属性，430, 432-434
- `<jsp:useBean>` 标签的属性，425-430
- page 指令的属性，66-67, 162, 171, 181
- 验证标签属性，236

## B

Banner.jsp，634

Base64 编码，526

JavaBean

- bean 属性，416-419
- 使用 bean 自定义天气信息，434-444
- 将视图页面模型声明为会话 bean，633
- 持久化和序列化，416, 419-424
- 抵押贷款的示例代码，416-419
- 支持事件监听器，419
- 天气 Observation bean，435

Berners-Lee, Tim，6

主体标签处理器 API，219-223

- 生命周期，223-226
- BodyTagSupport 类中的方法，222-223
- BodyContent 类的方法，219-221
- BodyTag 接口的方法，221-222

BodyContent 类，219-221, 810-811

BodyTag 类，221-222, 811-812

BodyTagSupport 类，190, 222-223, 812-813

BornBetween 查询示例，324-328

BoundConnection 构造函数，385-390

浏览器。参见 Web 浏览器

page 指令的 buffer 属性，172-173, 181

业务对象，558-587

- Customer 类中的，558-561
- CustomerProduct 类中的，565-568
- Employee 类中的，568-579
- Problem 类中的，579-584
- ProblemLog 类中的，584-587
- Product 类中的，561-565
- 与产品支持应用对象对比，588
- 驻留在 Model 应用程序容器中，588

按钮

- 定义，263
- 作为输入元素，282

# 846 JSP：完整参考手册

# 索引

## C

- 呼叫中心坐席
    - 在流程中的角色，552, 553, 554
    - 系统入口点，631, 632
    - 验证客户权益，565–568
- CallableStatement 接口，295, 322–328
- 回调方法，25
- canBeRequestTime 方法，817
- 案例研究。*参见* 产品支持应用程序
- case 标签，240–243
- 表格的单元格宽度，124–126
- CFML，704
- CGI（通用网关接口）
    - 定义，354
    - 发展，7–8
    - 作为服务器，704, 719
- HTML 表单中的字符集，267
- 复选框
    - 定义，263
    - 作为输入元素，273
- .class 文件，194
- 类
    - Action，660–662
    - BodyContent，219–221, 810–811
    - BodyTag，811–812
    - BodyTagSupport，812–813
    - 将 servlet 源代码编译为 Java 类，494
    - 构成会话 API 的类，369
    - 控制器类，658–675
    - CounterBean，423–424
    - Customer，558–561
    - CustomerNewProblemAction，669–670
    - CustomerProduct，565–568
    - CustomersListSelectAction，667–668
    - CustomersSearchAction，666–667
    - 声明定义内部类，128–131, 132
    - 声明写入封闭类，112
    - 声明和初始化变量，117–122, 131–132
    - Employee，568–579
- 封装业务实体
    - 在数据模型中，558
- Filter，724–725
- FilterChain，725
- FilterConfig，725–726
- GenericServlet，33–34, 726–729
- HttpJspPage，794–795
- HttpServlet，763–767
- HttpServletRequest，767–772
- HttpServletRequestWrapper，772–777
- HttpServletResponse，777–780
- HttpServletResponseWrapper，780–783
- HttpSession，783–786
- HttpSessionActivationListener，786–787
- HttpSessionAttributesListener，787–788
- HttpSessionBindingEvent，788–789
- HttpSessionBindingListener，789
- HttpSessionListener，791
- HttpUtils，791
- IterationTag，814
- java.net.HttpURLConnection 类，683–684
- java.net.URLConnection，682
- JavaBean 作为 Java 类，424–425
- javax.servlet.http 包的类，760–792
- javax.servlet 包的类，724–759
- JDBC 类，293–296
- JspEngineInfo，795
- JspException，795–796
- JspFactory，796–798
- JspPage，798–799
- JspWriter，800–804
- 案例研究的模型类，557–631
- PageContext，804–809
- PageData，814–815
- Problem，579–584
- ProblemLog，584–587
- ProblemSubmitAction，674–675
- Product，561–565
- ProductParser，479
- ProductsListSelectAction，671–672
- ProductsSearchAction，670–671



ProductsSelectAction, 672–673
RequestDispatcher, 158, 729–730
servlet, 31–47
Servlet API version 2.3 deprecated, 724
ServletRequestWrapper, 747–752
ServletResponse, 752–755
ServletResponseWrapper, 755–757
Shell, 616–630
SingleThreadModel, 758
Tag, 815–816
TagAttributeInfo, 816–818
TagData, 818–819
TagExtraInfo, 227–235, 820–821
TagInfo, 821–824
TagLibraryInfo, 824–825
TagLibraryValidator, 826
TagSupport, 202, 827–829
TagVariableInfo, 829–831
TryCatchFinally, 831
UnavailableException, 758–759
Util, 613–615
VariableInfo, 831–832
view, 631–658
in Web application directory structure, 531
WebModel, 611–613
另请参阅 Shell 类；超类；以及按名称排列的具体类
clear 方法, 800
clearBody 方法, 810
clearBuffer 方法, 800
clients（客户端）, 680–702
Java applets（Java小应用程序）作为客户端, 689–695
Java applications（Java应用程序）作为客户端, 684–689
Perl, 696–701
非浏览器客户端的类型, 680
URL connections（URL连接）, 680–684
Web browsers（Web浏览器）作为客户端, 164
client-side applications（客户端应用程序）, 9
clone 方法, 760
close 方法, 800
Cold Fusion, 704
JDBC 结果集中的列, 336–338
comments（注释）
语法, 68–69
使用 TagSupport 类进行, 205
Common Gateway Interface（通用网关接口）。参见 CGI
compilation（编译）
为标签处理器编译源代码, 191
检测编译错误, 494–499
区分编译时错误和运行时错误, 499
compiled servlet class（已编译的 servlet 类）, 494
config 隐式对象, 98, 106
Confirm.jsp 视图页面, 647–649
产品支持应用程序的确认页面, 649, 657, 660
connect() 方法, 593, 594
connect 标签
为开发其标签处理器, 250–252
功能, 247, 248, 249
连接到数据库
使用 RowSet 接口连接到 PDA 数据库, 338
从 Shell 类建立连接, 628–630
连接 JDBC 数据库, 307–308
JDBC URL 参数与连接, 308
连接方法, 594
打开连接, 294, 295
用于进程外 servlet 引擎模型的连接器, 134, 135
constants（常量）
描述可滚动结果集, 334
EVAL_BODY_INCLUDE, 222
EVAL_BODY_TAG, 221, 222
constructors（构造函数）
BodyTagSupport 的构造函数, 812
BoundConnection 的构造函数, 385–390
Cookie 类的构造函数, 760–763
GenericServlet 的构造函数, 727
HttpServlet 的构造函数, 764
HttpServletRequestWrapper 的构造函数, 772
HttpServletResponseWrapper 的构造函数, 780
HttpSessionBindingEvent 的构造函数, 788
HttpSessionEvent 类的构造函数, 790–791
HttpUtils 的构造函数, 791, 792
JspEngineInfo 的构造函数, 795
JspException 类的构造函数, 796
JspFactory 的构造函数, 797
JspTagException 的构造函数, 799
PageContext 的构造函数, 804
PageData 类的构造函数, 814
ServletContextAttributeEvent 的构造函数, 736
ServletContextEvent 的构造函数, 738
ServletException 类的构造函数, 739
ServletRequestWrapper 的构造函数, 748
ServletResponseWrapper 的构造函数, 755–757
Shell 类的构造函数, 567–568
TagAttributeInfo 类的构造函数, 817
TagData 的构造函数, 818
TagExtraInfo 的构造函数, 820
TagInfo 的构造函数, 821–822
TagLibraryValidator 类的构造函数, 826
TagSupport 的构造函数, 827–829
TagVariableInfo 的构造函数, 830
UnavailableException 的构造函数, 758–759
VariableInfo 的构造函数, 831–832
- 联系我们表单, 285–287
  - 在 HTML 表单中添加脚本块, 285
  - 从中提取的数据, 290
  - 其服务器程序, 288–289, 290
  - 为其验证设置触发器, 285
  - 编写验证函数, 286–287
- 容器
  - JSP 中的表达式和脚本片段, 65–66
  - 生成的初始化和退出代码, 96–97
  - JSP 容器转换 JSP 页面, 55, 194–195
  - JSP 中的 out.write() 语句, 94
  - 使用 JSP 翻译和调用 JSP 页面, 194–195
containsHeader 方法, 778, 781
- 内容
  - 合并动态内容, 136
  - 与表示层分离, 134, 154–157
  - Web 应用程序的内容, 530–531
  - 分离表示层和内容的 XML 解决方案, 453
HTML 表单的内容类型, 267
页面指令的 contentType 属性, 174, 181
- 上下文
  - servlet 上下文的功能, 535
  - PageContext 类, 804–809
  - pageContext 隐式对象, 98, 100–101, 128
  - 存储对 servlet 的引用, 45
- 上下文层次结构
  - 图示, 100
  - pageContext 隐式对象与上下文层次结构, 100–101
contextDestroyed 方法, 738
contextInitialized 方法, 739
- 控制器
  - 使用控制器接受并响应用户输入, 557
  - 案例研究的控制器类, 658–675
  - 定义, 557
  - 功能, 658–660
  - *另请参阅* 控制器类；ControllerServlet
- 控制器类, 658–675
  - controller servlet, 662–666
  - CustomerNewProblemAction 类, 669–670
  - CustomersListSelectAction 类, 667–668
  - CustomersSearchAction 类, 666–667
  - 控制器的功能, 658–660
  - Action 基类的代码清单, 660–662
  - ProblemSubmitAction 类, 674–675
  - ProductsListSelectAction 类, 671–672
  - ProductsSearchAction 类, 670–671
  - ProductsSelectAction 类, 672–673
- ControllerServlet
  - 功能, 658
  - 代码清单, 662–666
- 转换表
  - 燃油效率, 27–31, 56–60
  - 美元兑换加拿大元, 705–710
- cookies（Cookie）
  - 浏览器支持已关闭, 368
  - 构造函数和方法, 760–763
使用 Cookie 自定义天气信息, 445–446
在 HTTP 会话中提供 Cookie, 50
使用 Cookie 进行会话跟踪, 363–369, 371–372, 413–414
通过 HTTP 头设置和检索 Cookie, 364
使用 include 指令复制源代码, 139–140
counter.jsp 页面, 361, 362
CounterBean 类, 423–424
创建
会话, 370–372
创建并启动线程, 391–398
自定义标签
关于, 184, 258
为其定义的属性, 212–219
优点, 184–186
主体标签处理器 API 与自定义标签, 219–223
在标签库描述符中创建条目, 187–188
定义, 186–187
定义脚本变量, 186, 226–227
标签处理器的功能, 196
合并自定义标签的图示, 193
合并到 JSP 页面中, 192–194
为自定义标签编写标签处理器, 188–191
另请参阅 tags（标签）
客户
详细信息页面, 639
产品支持应用程序中的搜索页面, 636
作为产品支持应用程序的系统入口点, 631, 632
Customer 类, 558–561
Customer.jsp 视图页面, 638–643
CustomerList.jsp 视图页面, 637–638
CustomerNewProblemAction 类, 669–670
CustomerProduct 类, 565–568
Customers.jsp 视图页面, 635–636
CustomersListSelectAction 类, 667–668
CustomersSearchAction 类, 666–667
在门户网页上自定义天气信息, 444–448
data（数据）
从“联系我们”表单提取, 290
从结果集中提取, 328–332
另请参阅 metadata（元数据）
产品支持应用程序的数据模型
概述, 554–555
业务对象, 558–587
另请参阅 models（模型）
数据库查询示例
其中的 connect 标签, 247, 248, 249
其中的 forEachRow 标签功能, 247, 248
其中的 getField 标签, 247, 249
使用自定义标签实现, 247–258
其中的 runQuery 标签, 247, 248
标签库描述符, 248–249
databases（数据库）
MVC 架构中的数据库访问, 556
使用 JDBC 2.0 和 JNDI 访问, 293, 295
连接到 JDBC 数据库, 307–308
数据库元数据, 339–343
产品支持应用程序中的数据库表, 554–555
从 Shell 类建立连接, 628–630
使用自定义标签实现查询, 247–258
在 JDBC 中发出 SQL 语句, 294, 295
加载驱动程序类, 294, 295
连接方法, 594
在带有 JDBC 连接的 JSP 页面中命名数据源, 307
打开连接, 294, 295
PDA 数据库连接中的 RowSet 接口, 338
另请参阅 database query example（数据库查询示例）；JDBC
调试工具, 500–528
概述, 500–501
使用 Echo.jsp 捕获表单参数, 501–504
使用 Tracer 追踪 HTTP 请求, 510–528

# D

## 850 JSP：完全参考手册

## 索引

851

- WebClient, 504–510
另请参阅 testing and debugging（测试和调试）
declarations（声明）, 112–132
访问隐式对象, 128
定义, 112, 131
定义内部类, 128–131, 132
示例, 86–87
生成声明的代码, 112–117
在方法定义中, 122–128, 132
重写 jspInit() 和 jspDestroy() 方法, 126–127
语法, 71–73, 112
用途, 117
变量声明, 117–122, 131–132
default 标签, 243–244
default 线程模型, 403–405
定义脚本变量, 186, 226–236
概述, 227
同步脚本变量, 235–236
使用 TagExtraInfo 类, 227–235
验证标签属性, 236
delimiters（分隔符）
表达式的分隔符, 90, 91
声明和脚本片段开始语法中的分隔符, 112
部署 Web 应用程序, 530–549
Web 应用程序的定义, 530
部署描述符, 538–547
Web 应用程序的目录结构, 530–532
servlet 上下文的功能, 535
资源映射, 532–535
示例部署描述符, 547–549
通过 Servlet 2.2 规范进行标准化, 530, 549
Web 归档（.war）文件, 535–537, 549
部署描述符
在部署 Web 应用程序中, 538–547
示例代码, 547–549
反序列化, 419
destroy 方法, 27, 727, 730
销毁会话, 373–374
- 开发者在流程中的角色, 552, 553, 554
开发产品支持应用程序
创建支持模块, 633–635
开发 JSP 页面, 555–556
编写 Model 和 Shell 类, 630–631
directives（指令）, 65–68, 83
概述, 65
include 指令, 67–68, 136–140
page 指令, 66–67
taglib 指令, 68, 192
另请参阅 include directive（include 指令）；taglib directive（taglib 指令）
Web 应用程序的目录结构, 530–532
disconnect() 方法, 594
doAfterBody 方法, 812, 814, 827
doCatch 方法, 831
document element（文档元素）, 454
Document Object Model 解析器。参见 DOM parser
document type definition（文档类型定义）。参见 DTD
DocumentHandler 接口
定义, 474
其定义的方法, 475
documents（文档）
DOM 表示, 458
从 JSP 页面生成 XML 文档, 684–689
使用 URL 定位文档, 532–535
doDelete 方法, 764
doEndTag 方法, 812–813, 815, 827
doFilter 方法, 724–725
doFinally 方法, 831
doGet 方法, 764
doHead 方法, 765
doInitBody 方法, 811, 813
DOM（文档对象模型）解析器, 457, 458–472, 491
JSP 页面中的示例, 464–472
例外情况, 464
层次结构, 458, 461
节点集合接口, 462–463
节点接口, 458–461



节点元数据，463

SAX 与……对比，485

节点子接口，461–466

DOMImplementation 接口，463

doOptions 方法，765

doPost 方法，765

doPut 方法，766

doStartTag 方法，813、815、827

doTrace 方法，766

DriverManager 类，296、307

驱动程序，301–307
- 使用其创建数据库连接，307
- JDBC-ODBC 桥接，292、303、305
- 加载驱动程序类，294、295
- JDBC 概述，292、301–303
- 注册 JDBC，305–307
- JDBC 类型，303、304

DTD（文档类型定义），454–457
- 其中的属性，456、457
- 其中的元素，456–457
- 为 TLD 查找 DTD，197
- 部署描述符的格式，538
- DTD 的作用，455–456

DTDHandler 接口，474

动态内容
- 使用预处理语句避免动态语法错误，320–322
- 在 JSP 页面中引入动态内容，136
- 提供动态内容的技术，704

JSP 类型，65

用于部署描述符，538–547

*另请参阅* FORM 元素；表单输入元素；INPUT 标签元素

电子邮件
- 从应用程序发送电子邮件的选项，710
- 产品支持问题反馈的电子邮件，715–719
- 从 JSP 页面发送电子邮件，710–719
- 使用 JavaMail 发送电子邮件，713–715
- 使用 TCP/IP 套接字上的 SMTP 发送电子邮件，711–712
- sun.net.smtp.SmtpClient 类选项，712

Employee 类，568–579

encodeRedirectUrl 方法，778、781

encodeRedirectURL 方法，778、781

encodeUrl 方法，778、781

encodeURL 方法，778、782

enctype 属性，263、265–267
- 关于 enctype，265
- application/x-www-form-urlencoded 类型，265–266
- multipart/form-data 类型，266–267

实体头，836

EntityResolver 接口，474

enumerate 标签
- 图解输出，235
- 示例代码，229–235

异常的错误页面，179、180

ErrorHandler 接口，474

页面指令的 errorPage 属性，176–180、181

ErrorPage.jsp，634–635

错误
- 使用预处理语句避免动态语法错误，320–322
- 为视图页面创建错误模块，634–635
- 编译时错误检测，494–499
- 区分编译时错误和运行时错误，499
- 页面指令的 errorPage 和 isErrorPage 属性，176–180、181

## E

Echo.jsp，501–504

元素
- 注释，68–69
- 声明，71–73、86–87
- 指令，65–68、83
- DTD 中的元素，456–457
- 表达式，69–70、85
- 表单输入元素，268–285
- 隐式对象，74–75
- 脚本小程序，70–71、84
- 在 <web-app> 体内指定元素顺序，538

索引 853

在调试环境中启动，500–501

隔离故障组件，499–500

诊断错误页面的示例代码，179、180

用 Servlet 错误消息替代浏览器错误消息，495

开启/关闭消息，495

EVAL_BODY_INCLUDE 常量，222

EVAL_BODY_TAG 常量，221、222

事件监听器，Bean 对事件监听器的支持，419

exception 隐式对象，98、106

异常
- 使用 Servlet 显示异常，179
- DOM 解析器的异常，464
- 异常的错误页面，179、180
- 实现 BodyTag 接口的运行时异常，222

execute 方法，312–314

executeBatch 方法，314–316

executeQuery 方法，311–312

executeUpdate 方法，310–311

表达式和脚本小程序，90–109
- application 隐式对象，98、103–104
- config 隐式对象，98、106
- 容器生成的初始化和退出代码，96–97
- 上下文层和 pageContext 隐式对象，100–101
- 表达式的分隔符，90、91
- exception 隐式对象，98、106
- 表达式定义，90–91
- JSP 容器的处理方式，65–66
- HTML 模板数据和表达式，94
- 可用的隐式对象，97–106
- 初始化参数，107–109
- out 隐式对象，98、104–105
- page 隐式对象，106
- request 隐式对象，97、98–100
- response 隐式对象，97、99–100
- 脚本小程序的示例代码，94–96
- 脚本小程序定义，91–93
- 表达式内的分号，70、91
- session 隐式对象，98、102–103
- 表达式的语法，69–70、85

页面指令的 extends 属性，164–170、181
- JSP 超类的示例，166–170
- 概述，164、181
- JSP 超类所需的接口，164–166

可扩展标记语言。参见 XML

Externalizable 接口，416、424

从结果集中提取数据，328–332

# F

文件选择元素，263

文件上传输入字段，276–280

文件名
- 问题 ID 的获取和设置方法，593
- 包含指令中的文件名，136–138
- <jsp:include> 动作中的文件名，140

文件
- .class 文件，194
- 使用 Echo.jsp 调试文件，501–504
- 所包含文件更改的影响，138
- .jar 文件，535
- .java 文件，194
- .jsp 文件，64、194
- 上传文件的大小限制，277
- 将标签库映射到 web.xml，199–200
- JSP 页面的三种形式的文件，54–56、64、194
- .war 文件，535–537、549
- web.xml 文件，199–200、531、538–547

*另请参阅* 文件名

FilterChain 类，725

FilterConfig 类，725–726

findAncestorWithClass 方法，828

findAttribute 方法，804–805

流程图
- 体标签处理器生命周期流程图，223–226
- <jsp:useBean> 处理流程图，427、428、429、431
- 标签处理器生命周期流程图，203–205

# 854 JSP: 完全参考手册

flush 方法，800、810

flushBuffer 方法，752–753、755

forEachRow 标签
- 为 forEachRow 开发标签处理器，254–256
- 数据库查询示例中的 forEachRow 函数，247、248

FORM 元素
- accept 属性，267
- accept-charset 属性，267
- action 属性，264
- 属性，264–268
- enctype 属性，263、265–267
- 功能和语法，263–264
- method 属性，264–265
- name 属性，267–268

表单输入元素，268–285
- 使用 INPUT 标签创建，270–282
- 使用 select 和 option 标签创建，283–284
- 说明性示例代码，268–270
- textarea 元素，284

捕获表单参数
- 使用调试工具，501–504

forward 方法，729、805

请求转发，154–158

燃油效率转换表，27–31、56–60

互联网的未来，4

getAttributes 方法，819、822

getAttributesScope 方法，805–806

getAttributeString 方法，747、819

getAuthType 方法，767、772

getBodyContent 方法，813、822

getBufferSize 方法，753、755、801

getCharacterEncoding 方法，743–744、748、753、755–756

getClassName 方法，830、832

getComment 方法，760

getContentLength 方法，744、748

getContentType 方法，744、748–749

getContext 方法，732

getContextPath 方法，767、772–773

getCookies 方法，767–768、773

getCreationTime 方法，784

getDateHeader 方法，768、773

getDeclare 方法，830、832

getDefaultFactory 方法，797

getDisplayName 方法，822

getDomain 方法，761

getEnclosingWriter 方法，810

getEngineInfo 方法，797

getException 方法，806

getField 标签
- 为 getField 开发标签处理器，256–257
- 数据库查询示例中的 getField 函数，247、249

getFilterConfig 方法，725

getFilterName 方法，726

getHeader 方法，768、773

getHeaderNames 方法，768、773

getHeaders 方法，768、773

getId 方法，784、819、828

getIdAttribute 方法，817

getIds 方法，790

getInfoString 方法，822、824

getInitParameter 方法，726、727、731、733

getInitParameterNames 方法，726、727、731、733

getInitParameters 方法，826

getInputStream 方法，744、749、815

getIntHeader 方法，768、774

getLargeIcon 方法，822

getLastAccessedTime 方法，784

getLastModified 方法，766

getLocale 方法，744、749、753、756

# G

通用头，836

生成的 Servlet 源代码
- 生成的 Servlet 源代码调试，500
- 将 .jsp 文件转换为生成的 Servlet 源代码，494

通用数据库选择服务器，696–698、702

GenericServlet 类，33–34、726–729

GET 请求
- GET 请求的基本技术，705
- 从远程网络资源读取 GET 请求，705–710

getAttribute 方法，732、743、748、784、805、819

getAttributeNames 方法，732、743、748、784

getAttributeNamesInScope 方法，805

# 索引 855

getLocales 方法，744、749

getMajorVersion 方法，733

getMaxAge 方法，761

getMaxInactiveInterval 方法，784–785

getMethod 方法，769、774

getMimeType 方法，733

getMinorVersion 方法，733

getName 方法，736–737、761、788–789、817

getNamedDispatcher 方法，733

getNameFromAttribute 方法，830

getNameGiven 方法，830

getOut 方法，806

getOutputStream 方法，753、755、756

getPage 方法，806

getPageContext 方法，797–798

getParameter 方法，744–745、749

getParameterMap 方法，745、749

getParameterNames 方法，745、749–750

getParameterValues 方法，745、750

getParent 方法，816、828

getPath 方法，761、774

getPathInfo 方法，769、774

getPathTranslated 方法，769、774

getPrefixString 方法，825

getPreviousOut 方法，813

getProtocol 方法，745、750

getQueryString 方法，769、774

getReader 方法，745、750、811

getRealPath 方法，733–734、745、750

getReliableURN 方法，825

getRemaining 方法，801

getRemoteAddr 方法，746、750

getRemoteHost 方法，746、750–751

getRemoteUser 方法，769、774–775

getRequest 方法，751、806

getRequestDispatcher 方法，734、746、751

getRequestedSessionId 方法，769–770、775

getRequestURI 方法，770、775

getRequestURL 方法，770、775、792

getRequiredVersion 方法，825

getResource 方法，734

getResourceAsStream 方法，734

getResourcePaths 方法，734

getResponse 方法，756、806

getRootCause 方法，796

getScheme 方法，746、751

getScope 方法，831、832

getSecure 方法，761

getServerName 方法，746、751

getServerPath 方法，770

getServerPort 方法，746–747、751

getServlet 方法，735、759

getServletConfig 方法，728、730、806

getServletContext 方法，726、728、731、738、807

getServletContextName 方法，735

getServletInfo 方法，728、730、734

getServletName 方法，728、732

getServletNames 方法，735

getServletPath 方法，770、775

getServlets 方法，735

getSession 方法，770–771、775–776、789、790、791、807

getSessionContext 方法，785

getShortName 方法，825

getSmallIcon 方法，823

getSpecificationVersion 方法，795

getString 方法，811

getTag 方法，825

getTagClassName 方法，823

getTagExtraInfo 方法，823

getTagInfo 方法，820

getTagLibrary 方法，823

getTagName 方法，823

getTags 方法，825

getTagVariableInfos 方法，823

getTypeName 方法，817

getUnavailableSeconds 方法，759

getURI 方法，825

getUserPrincipal 方法，771、776

getValue 方法，737、761、785、789、828

getValueNames 方法，785

getValues 方法，828

getVariableInfo 方法，228–229、820、823

getVarName 方法，832

getVersion 方法，762

getWebServerHeader 标签处理器，206–212

getWriter 方法，753、756

getXXX() 方法，331–332



## H

- `handlePageException` 方法，807
- 处理程序
  - 用于SAX解析事件，474–475
  - *另见* 主体标签处理程序API；标签处理程序API；标签处理程序
- 头部
  - 使用Banner.jsp创建标准化头部，634
  - 使用HTTP设置和检索Cookie，364
  - HTTP头部语法，836
  - HTTP头部表格，836–843
  - 类型，836
  - *另见* 响应头部
- Shell类的帮助，626–627
- 隐藏元素，263
- 隐藏字段，280–281
  - 使用会话API处理会话跟踪任务，374–378
  - 使用隐藏字段进行会话跟踪，355–360
  - 在隐藏字段中存储会话ID，50
- HTML（超文本标记语言）
  - 模板中的数据和表达式，94
  - 使用INPUT标签创建的表单输入元素，270–282
  - 在JSP页面中整合动态内容，136
  - XML与HTML对比，452–453
- HTML表单，262–290
  - 概述，262–263
  - 向其中添加JavaScript脚本块，285
  - FORM元素的属性，264–268
  - 使用Echo.jsp进行调试，501–504
  - 表单输入元素，268–285
  - FORM元素的功能和语法，263–264
  - 其中的隐藏字段，413
  - 概览，289–290
  - 服务器端表单处理，287–289
  - 验证，285–287
  - *另见* FORM元素；表单输入元素
- HTTP（超文本传输协议），12–21
  - 概述，12
  - 使用Tracer进行身份验证，526–528
  - 连接到Web服务器，14
  - 发展历程，6
  - 请求示例，17–21
  - 头部，836–843
  - HTTP请求模型，13–14
  - 服务器的HTTP响应，16–17
  - 目的，354
  - 服务器接收HTTP请求，16
  - 带CGI脚本的请求，7
  - 响应代码，834–835
  - RFC规范，12–13
  - 发送HTTP请求，15–16
  - Servlet与HTTP会话，49–51
  - 使用HTTP头部设置和检索Cookie，364
  - 使用HTTP向客户端传递内容的技术，719
  - 使用Tracer跟踪HTTP请求，510–528
  - 头部类型，836
  - 在会话中使用HttpSession接口，50–51
- HTTP GET请求
  - 基本技术，705
  - 从远程网络资源读取，705–710
- HTTP POST方法，694，702
- `HttpJspPage`类，794–795
- `HttpServlet`类，34–36，763–767
- `HttpServletRequest`类，767–772
- `HttpServletRequest`对象，内容，134
- `HttpServletRequest`子接口，方法，39–41
- `HttpServletRequestWrapper`类，772–777
- `HttpServletResponse`类，43–44，777–780
- `HttpServletResponseWrapper`类，780–783
- `HttpSession`类，50–51，369，783–786
- `HttpSessionActivationListener`类，786–787
- `HttpSessionAttributesListener`类，787–788
- `HttpSessionBindingEvent`类，370，788–789
- `HttpSessionBindingListener`类，370，383–385，789
- `HttpSessionContext`类，790
- `HttpSessionEvent`类，790–791
- `HttpSessionListener`类，791
- `HttpURLConnection`类，683–684
- `HttpUtils`类，791
- 超文本标记语言。*参见* HTML
- 超文本传输协议。*参见* HTTP

## I

- `<jsp:useBean>`标签的`id`属性，425
- IDE（集成开发环境）
  - 自定义标签与IDE对比，185
  - 调试器，500
- IETF（互联网工程任务组），12
- 图像作为输入字段，281–282
- 隐式对象
  - 声明对隐式对象的访问，128
  - application，98，103–104
  - 在表达式和脚本片段中可用，97–106
  - config，98，106
  - exception，98，106
  - out，98，104–105
  - page，98，106
  - pageContext，98，100–101
  - request，97，98–100
  - response，97，99–100
  - session，102–103
  - 语法，74–75
  - *另见* 对象
- 页面指令的`import`属性，170–171，181
- `include`指令，136–140
  - 使用注意事项，140
  - 使用其复制源代码，139–140
  - 使用`<jsp:include>`动作或`include`指令的标准，153，633
  - 定义，67–68
  - 所包含文件更改的影响，138
  - 工作原理，137–138
  - 语法，67，136
- `include`方法，729–730，807
- 页面指令的`info`属性，174，181
- `init`方法，25–26，728，730–731
- 初始化参数
  - 用于表达式和脚本片段，107–109
  - 在编译的Java代码外指定，535
- `initialize`方法，808
- `InitModel.jsp`，633
- 内部类
  - 定义，128
  - 声明示例，129–130
  - 功能，132
  - 使用声明，128–131，132
- 进程内模型，134
- INPUT标签元素，270–282
  - 按钮，282
  - 复选框，273
  - 文件上传输入字段，276–280
  - 隐藏字段，280–281
  - 图像输入字段，281–282
  - 密码，272–273
  - 单选按钮，274–275
  - 重置控件，276
  - 提交按钮，275–276
  - 语法和属性，270–271
  - 文本输入，271–272
- 实例变量
  - 声明和初始化，117–122，131–132
  - 线程安全与实例变量，118–122
- `InstantDB`，299
- 集成开发环境。*参见* IDE
- 互联网
  - 万维网的发展，6
  - Web应用程序编程模型的演进，6–9
  - 未来，4
  - 关于HTTP规范的在线资源，12
- 互联网工程任务组（IETF），12
- 服务器端脚本技术的互操作性，704–705
- `invalidate`方法，785
- 调用存储过程，295，322–328
- `isAutoFlush`方法，801
- `isCommitted`方法，753，756
- 页面指令的`isErrorPage`属性，176–180，181
- `isNew`方法，785
- 隔离故障组件，499–500
- `isPermanent`方法，759
- `isRequestedSessionIdFromCookie`方法，771，776
- `isRequestedSessionIdFromURL`方法，771，776
- `isRequestedSessionIdFromUrl`方法，771，776
- `isRequestedSessionIdValid`方法，771，776
- `isRequired`方法，818
- `isSecure`方法，747，751–752
- 页面指令的`isThreadSafe`属性，173–174，181
- `isUserInRole`方法，772，777
- `isValid`方法，820，824
- `IterationTag`类，814

## J

- J2EE（Java 2企业版），8，9
- `.jar`文件，535
- Java
  - 作为客户端的Applet，689–695
  - 作为客户端的应用程序，684–689
  - 将Servlet源代码编译为Java类，494
  - Applet的演进，689
  - JNDI带来的灵活性，293，295
  - J2EE版本，8，9
  - JavaBeans作为Java中的类，424–425
  - 插件，690–691
  - 将代码与JSP代码分离，134
  - 为编译代码指定初始化参数，535
  - *另见* JavaBeans；JAXP
- Java 2企业版（J2EE），8，9
- `.java`文件，194
- 用于XML的Java API（JAXP）
  - 对SAX 2.0的支持，481
  - 用途，464
- `java.net.HttpURLConnection`类，683–684
- `java.net.URL`类，680–681
- `java.net.URLConnection`类，682
- Java运行时环境（JRE），712
- `java.sql.CallableStatement`接口，322–328
- `java.sql.PreparedStatement`子接口，317–322
  - 使用其避免动态语法错误，320–322
  - 批量更新示例，317–320
  - 概述，317
- `java.sql.Statement`接口
  - `execute`方法，312–314
  - `executeBatch`方法，314–316
  - `executeQuery`方法，311–312
  - `executeUpdate`方法，310–311
  - 概述，309–310
  - `PreparedStatement`子接口，317–322
- `java.util.ResourceBundle`对象，365
- JavaBeans，416–449
  - 向门户网站网页添加自定义天气信息，444–448
  - Bean属性，416–419
  - 使用Bean自定义天气信息，434–444
  - 定义，416
  - 作为Java类，424–425
  - `<jsp:getProperty>`标签，434，448，449
  - `<jsp:setProperty>`标签，430–434，448，449
  - `<jsp:useBean>`标签，425–430，448
  - 概述，416，448–449
  - Bean的持久化和序列化，416，419–424
  - *另见* Java
- JavaMail API
  - 概述，719
  - 文档资源，713
  - 电子邮件选项，713–715
- JavaServer Pages，54–60
  - 带注释的示例，78–87
  - 作为其他服务器的客户端，704，719
  - 在其中创建支持模块，633–635
  - 调试工具，500–501
  - 为产品支持应用程序开发，555–556
  - 发展历程，8
  - DOM解析器示例，464–472
  - 燃油效率转换表示例，56–60
  - 形式，54–56，64，194
  - 为声明生成代码，112–117
  - JSP容器如何转换JSP页面，55，194–195
  - 将自定义标签整合到JSP页面，192–194
  - 对JDBC可访问数据库执行SQL SELECT查询，696–698
  - 概述，54
  - 向被包含页面传递参数，149–150，151
  - 在JSP页面中使用Perl脚本和数据库选择服务器，696–698，702
  - 插件，690–691
  - 描述被包含页面的请求属性，152，153
  - 范围，4
  - 从JSP页面发送邮件，710–719
  - 翻译和编译，494–499
  - *另见* 测试和调试

## JavaServer Pages元素，65–78

- 注释，68–69
- 声明，71–73，86–87
- 指令，65–68，83
- 表达式，69–70，85
- 隐式对象，74–75
- 脚本片段，70–71，84
- 类型，65

## javax.servlet类，724–759

- `Filter`类，724–725
- `FilterChain`，725
- `FilterConfig`，725–726
- `GenericServlet`，726–729
- `RequestDispatcher`，729–730
- `Servlet`类，730–731
- `ServletConfig`，731–732
- `ServletContext`，732–736
- `ServletContextAttributeEvent`，736–737
- `ServletContextAttributesListener`，737
- `ServletContextEvent`，738
- `ServletContextListener`，738–739
- `ServletException`，739–740
- `ServletInputStream`，740
- `ServletOutputStream`，740–743
- `ServletRequest`，743–747
- `ServletRequestWrapper`，747–752
- `ServletResponse`，752–755
- `ServletResponseWrapper`，755–757
- `SingleThreadModel`，758
- `UnavailableException`，758–759

## javax.servlet.http类，760–792

- `Cookie`，760–763
- `HttpServlet`，763–767
- `HttpServletRequest`，767–772
- `HttpServletRequestWrapper`，772–777
- `HttpServletResponse`，777–780
- `HttpServletResponseWrapper`，780–783
- `HttpSession`，783–786
- `HttpSessionActivationListener`，786–787
- `HttpSessionAttributeListener`，787–788
- `HttpSessionBindingEvent`，788–789
- `HttpSessionBindingListener`，789
- `HttpSessionContext`，790
- `HttpSessionEvent`，790–791
- `HttpSessionListener`，791
- `HttpUtils`，791

## javax.servlet.jsp类，794–810

- `HttpJspPage`，794–795
- `JspEngineInfo`，795
- `JspException`，795–796
- `JspFactory`，796–798
- `JspPage`，798–799
- `JspTagException`，799–800
- `JspWriter`，800–804
- `PageContext`，804–809



## javax.servlet.jsp

`javax.servlet.jsp.HttpJspPage` 接口，164
`javax.servlet.jsp.JspPage` 接口，164
`javax.servlet.jsp.tagext` 类，810-832
- `BodyContent`，810-811
- `BodyTag`，811-812
- `BodyTagSupport`，812-813
- `IterationTag`，814
- `PageData`，814-815
- `Tag`，815-816
- `TagAttributeInfo`，816-818
- `TagData`，818-819
- `TagExtraInfo`，820-821
- `TagInfo`，821-824
- `TagLibraryInfo`，824-825
- `TagLibraryValidator`，826
- `TagSupport`，827-829
- `TagVariableInfo`，829-831
- `TryCatchFinally`，831
- `VariableInfo`，831-832

`javax.servlet.Servlet` 接口，32, 166, 730-731
`javax.sql` 包，核心 API，293

## JAXP (Java API for XML)

- 支持 SAX 2.0，481
- 用途，464

## jdb 调试器

- 500

## JDBC

292-351
- 优点，292-293
- 基本操作，293, 294, 295
- 类，293-296
- 连接数据库，307-308
- 驱动程序，292, 301-307
- 核心类，293-296
- 示例，296-301
- 2.0 版特性，351
- 获取连接信息，339
- 导航可滚动结果集，333
- 概述，292-301, 351
- 结果集，328-338
- SQL 语句接口，309-328
- 使用元数据，338-350
- *另见* 驱动程序；元数据；结果集；Statement 接口

### JDBC 驱动程序

- 定义，292
- 概述，301-303
- 注册，305-307
- 类型，303, 304

`JDBC URL` 参数，308
`JDBC-ODBC 桥`，292, 303, 305
- 定义，292

`JNDI`（Java 命名和目录接口），293, 295

## JRun

- 连接器，134
- 部署向导，537

## JSP 动作和标签

`<jsp:forward>` 动作，154-157
`<jsp:getProperty>` 标签，434, 448, 449
`<jsp:include>` 动作，140-153
- 使用 include 指令或此动作的标准，153, 633
- 示例，83-84
- 功能，136, 141-143
- 向被包含的 JSP 页面传递参数，149-150, 151
- 限制，144
- 检索原始 URI，150-153
- 运行时特性，144-149
- 语法，140
`<jsp:setProperty>` 标签，430-434, 448, 449
- `name` 属性，430
- `param` 属性，433
- `property` 属性，432-433
- 语法，430
- `value` 属性，433-434
`<jsp:useBean>` 标签，425-430, 448
- 仅指定 class，427-428
- `id` 属性，425
- `scope` 属性，425-426
- 语法，425
- 指定 type 和 beanName，429-430, 431
- 指定 type 和 class，428-429
- 仅指定 type，426-427
- type 指定的有效组合，426

## JSP 1.1 规范

- 使用 `extends` 属性的注意事项，164
- 禁止直接覆盖 servlet 生命周期方法，126, 127
- 使用 include 指令，140

## .jsp 源文件

- 定义，194
- 开发和转换为 servlet，494
- JSP 元素在其中的运行，64

## JSP API 1.2

794–832
- 类和方法
  - `javax.servlet.jsp`，794–810
  - `javax.servlet.jsp.tagext` 类和方法，810–832

## JSP 页面

参见 JavaServer Pages；JSP API 1.2

## JSP Price Quote 服务器

684–687

## jspDestroy() 方法

- 定义，799
- 覆盖，126–127

## JspEngineInfo 类

795

## JspException 类

795–796

## JspFactory 类

796–798

## jspInit() 方法

- 定义，799
- 覆盖，126–127

## _jspService() 方法

- 关于，93–94, 794–795
- 在其外部运行代码的声明，112
- 传递对象，128

## JspPage 类

798–799

## JspTagException 类

799–800

## JspWriter 类

800–804

## L

### 页面指令的 language 属性

162–164, 181

### 语言偏好

- 使用 cookie 设置，364–369
- 使用 session API 设置，379–382

### lib 目录

531

### 生命周期

- 正文标签处理器，223–226
- 加载驱动程序类，294, 295

### log 方法

- 定义，728–729, 735–736
- 在隔离测试中使用，500, 501

### LyricNote.com 示例应用程序

684–701
- Price Quote 客户端应用程序，687–689
- JSP Price Quote 服务器，684–687
- Perl 数据库搜索脚本，699–701
- PriceQuoteApplet 源代码，691–696
- *另见* 产品支持应用程序

## M

### Shell 类的主读/执行循环

618–620

### 管理线程

390–391

### 将标签库映射到 web.xml 文件

199–200

### 使用 select 和 option 标签创建的菜单

283–284

### 消息日志

535

### 元数据

338–350
- 来自 Access 数据库，344–349
- 数据库元数据，339–343
- 定义，338
- 查询 DOM 节点以了解特性支持，463
- `ResultSetMetaData` 方法，296, 349–350
- 查看 JDBC 连接上的元数据，344

### MetadataExplorer.jsp

339–343, 344

### method 属性

263, 264–265

### 方法

- `BodyContent` 类，219–221
- `BodyTag` 类，811–812
- `BodyTag` 接口，221–222
- `BodyTagSupport` 类，812–813
- 声明附加方法，122–128, 132
- 在 servlet 中复制的方法定义，123
- Servlet API 2.3 版已弃用，724
- `destroy`，27
- `DocumentHandler` 接口，475
- `Filter` 类，724–725
- `FilterChain` 类，725
- `FilterConfig` 类，726
- `GenericServlet` 类，33–34
- `GenericServlet` 类，727–729
- `getVariableInfo`，228–229
- `getXXX()`，331–332
- HTTP 请求，15
- `HttpJspPage` 类，794–795
- `HttpServlet` 类，35–36
- `HttpServletRequest` 子接口，39–41
- `HttpServletRequestWrapper`，772–777
- `HttpServletResponse` 类，43–44, 777–780
- `HttpServletResponseWrapper` 类，780–783
- `HttpSession` 类，784–786
- `HttpSessionActivationListener`，787
- `HttpSessionAttributesListener` 类，787–788
- `HttpSessionBindingEvent` 类，788
- `HttpSessionBindingListener` 类，789
- `HttpSessionContext` 类，790
- `HttpSessionEvent` 类，791
- `HttpSessionListener` 类，791
- `HttpUtils` 类，791
- `IterationTag` 类，814
- `java.net.HttpURLConnection` 类，684
- `java.net.URL` 类，681
- `java.net.URLConnection` 类，682
- `javax.servlet.Servlet` 接口，32, 166, 730–731
- JDBC 导航可滚动结果集的方法，333
- `JspEngineInfo` 类，795
- `JspException` 类，796
- `JspFactory` 类，797–798
- `JspPage` 类，799
- `JspWriter` 类，800–804
- `Shell` 类列表，627–628
- `log`，500, 501
- `NamedNodeMap` 接口，463
- `node` 接口，458–461
- `NodeList` 接口，463
- `out` 隐式对象，104–105
- `PageContext` 类，804–809
- `pageContext` 隐式对象，101
- `PageData` 类，814–815
- `request` 隐式对象，99–100
- `RequestDispatcher` 类，729–730
- JSP 超类中声明所需的方法，165
- `ResultSetMetaData`，296, 349–350
- SAX `Parser` 接口，473–474
- `Servlet` 类，730–731
- `Servlet Context` 接口，45–47
- servlet `init`，25–26
- `ServletConfig` 类，731–732
- `ServletContext` 类，732–736
- `ServletContextAttributeEvent` 类，736–737
- `ServletContextAttributes Listener` 类，737
- `ServletContextEvent` 类，738
- `ServletContextListener` 类，738–739
- `ServletException` 类，740
- `ServletInputStream` 类，740
- `ServletOutputStream` 类，741–743
- `ServletRequest` 类，36–38, 743–747
- `ServletRequestWrapper` 类，748–752
- `ServletResponse` 类，752–755
- `ServletResponse` 接口，41–43
- `ServletResponseWrapper` 类，755–757
- servlets，25
- `session` 对象，102–103
- `Shell` 类，616–617
- `Statement` 接口，310–316
- `Tag` 接口，200–201
- `TagAttributeInfo` 类，817–818
- `TagData` 类，819
- `TagData` 参数，236, 237
- `TagExtraInfo` 类，228, 820–821
- `TagInfo` 类，822–824
- `TagLibraryInfo` 类，824–825
- `TagLibraryValidator` 类，826
- `TagSupport` 类，202, 827–829
- `TagVariableInfo` 类，830
- `TryCatchFinally` 类，831
- `VariableInfo` 类，832
- *另见* 按名称列出的具体方法

### Microsoft Access

- 从数据库获取元数据，344–349
- 支持存储过程查询，324–328
- 查看元数据数据库，344

### MIDI（乐器数字接口）文件

277

### Model 1 与 Model 2 Web 应用程序

159–160

### Model 类

- 应用程序对象，588–615
- 使用，630–631

### 模型类

557–631
- 应用程序对象，588–615
- 数据模型中的业务对象，558–587
- 模型的测试框架，615–630
- 支持类型，557–558
- *另见* 模型；MVC 系统架构

### 模型

- MVC 架构中的模型编码逻辑，556
- 将视图页面声明为会话 bean，633
- 默认线程模型，403–405
- HTTP 请求，13–14
- 进程内，134
- Model 1 与 Model 2 Web 应用程序，159–160
- 进程外 servlet 引擎，134–135
- 产品支持应用程序数据，554–555
- 编程 Web 应用程序，6–9
- 单线程，49, 173, 174, 403, 405–406
- 静态文档服务器，6
- 测试和调试，494
- *另见* DOM 解析器；MVC 系统架构；servlet 线程模型

### 模型-视图-控制器系统架构

参见 MVC 系统架构

### 鼠标点击图像

281–282

### multipart/form-data 编码技术

266–267

### 多线程应用程序

406–410
- 带有状态消息的长时间运行请求，407–410
- 概述，406–407
- *另见* 会话和线程管理；线程

### 乐器数字接口（MIDI）文件

277

### MVC（模型-视图-控制器）系统架构

556–676
- 控制器类，658–675
- 定义，159–160
- 图解，556
- 模型类，557–631
- 概述，556–557
- 案例研究的系统入口点，631
- 模型的测试框架，615–630
- 视图类，631–658

## N

### name 属性

- HTML 表单，267–268
- `<jsp:setProperty>` 标签，430

### NamedNodeMap 接口

462, 463

### 名称

参见文件名



## 864 JSP 完全参考

- SAX 2.0 中的命名空间支持，480
- JDBC 可滚动结果集的导航方法，333
- 嵌套标签，236-237
- newLine 方法，801
- node 接口
  - DOM 解析器的 node 接口，458-461
  - 返回节点集合，462-463
  - 其子接口，461-466
- NodeList 接口，462，463
- 非浏览器客户端，680
- 猜数字游戏，360，374-378
- ServletContextAttributesListener 类，737
- ServletContextEvent 类，738
- ServletContextListener 类，738-739
- ServletException 类，739-740
- ServletInputStream 类，740
- ServletOutputStream 类，740-743
- ServletRequest 类，743-747
- ServletRequestWrapper 类，747-752
- ServletResponse 类，752-755
- ServletResponseWrapper 类，755-757
- SingleThreadModel 类，758
- UnavailableException 类，758-759

**O**

- 对象
  - 序列化，420
  - 在会话中存储和检索，372-373
  - 与 servlet 上下文一起存储和共享，535
  - *另见* 应用程序对象；业务对象；隐式对象
- 在线职位申请
  - 表单参数，504
  - 用于调试的示例代码，501-504
- 打开数据库连接，294，295
- 可选的响应描述，17
- out 隐式对象，98，104-105
- 覆盖 jspInit() 和 jspDestroy() 方法，126-127
- 包 javax.servlet.http，760-792
  - Cookie 类，760-763
  - HttpServlet 类，763-767
  - HttpServletRequest 类，767-772
  - HttpServletRequestWrapper 类，772-777
  - HttpServletResponse 类，777-780
  - HttpServletResponseWrapper 类，780-783
  - HttpSession 类，783-786
  - HttpSessionActivationListener 类，786-787
  - HttpSessionAttributeListener 类，787-788
  - HttpSessionBindingEvent 类，788-789
  - HttpSessionBindingListener 类，789
  - HttpSessionContext 类，790
  - HttpSessionEvent 类，790-791
  - HttpSessionListener 类，791
  - HttpUtils 类，791

**P**

- 包 javax.servlet，724-759
  - Filter 类，724-725
  - FilterChain 类，725
  - FilterConfig 类，725-726
  - GenericServlet 类，726-729
  - RequestDispatcher 类，729-730
  - Servlet 类，730-731
  - ServletConfig 类，731-732
  - ServletContext 类，732-736
  - ServletContextAttributeEvent 类，736-737
- 包 javax.servlet.jsp，794-810
  - HttpJspPage 类，794-795
  - JspEngineInfo 类，795
  - JspException 类，795-796
  - JspFactory 类，796-798
  - JspPage 类，798-799
  - JspTagException 类，799-800
  - JspWriter 类，800-804
  - PageContext 类，804-809
- 包 javax.servlet.jsp.tagext，810-832
  - BodyContent 类，810-811
  - BodyTag 类，811-812
  - BodyTagSupport 类，812-813
  - IterationTag 类，814
  - PageData 类，814-815
  - TagAttributeInfo 类，816-818
  - TagData 类，818-819
  - TagLibraryInfo 类，824-825
  - TagLibraryValidator 类，826
  - TagSupport 类，827-829
  - TryCatchFinally 类，831
  - VariableInfo 类，831-832
- 包 javax.sql，293
- 页面计数器，360-363，378-379
- 页面指令，162-181
  - 其属性，66-67，162，181
  - 其 buffer 和 autoFlush 属性，172-173，181
  - 其 contentType 属性，174，181
  - 其 errorPage 和 isErrorPage 属性，176-180，181
  - 其 extends 属性，164-170，181
  - 其 import 属性，170-171，181
  - 其 info 属性，174，181
  - 其 isThreadSafe 属性，173-174，181
  - 其 language 属性，162-164，181
  - 其 session 属性，172，181
  - 指定属性，171
  - 语法，162
- page 隐式对象，98，106
- 页面作用域，411
- PageContext 类，804-809
- pageContext 隐式对象，100-101
  - 定义，98
  - 作为参数从 _jspService() 传递，128
- PageData 类，814-815
- <jsp:setProperty> 标签的 param 属性，433
- 参数
  - 通过捕获表单进行调试，501-504
  - 在编译后的 Java 代码外部指定初始化参数，535
- parsePostData 方法，792
- parseQueryString 方法，792
- Parser 接口，473-474
- 解析器，457-485
  - DOM，457，458-472，491
  - SAX，472-473
  - *另见* DOM 解析器；SAX 解析器
- 密码，作为输入元素，272-273
- PDA（个人数字助理），数据库连接，338
- 性能
  - 使用 <jsp:include> 动作或 include 指令的标准，153
  - 通过请求分派消除冗余，134
  - servlet 及其改进，24
- Perl 客户端，696-701
- Perl 数据库搜索脚本，699-701
- PHP，704
- 插件，690-691
- popBody 方法，808
- 预编译 JSP 页面，499
- PreparedStatement 接口，295，317-322
- 防止
  - 多余的空白符，696
  - 换行符，687
- 报价客户端应用程序，687-689
- PriceQuoteApplet，691-696
- print 方法，741-742，801-802
- println 方法，742-743，802-804
- Problem 类，579-584
- Problem.jsp 视图页面，643-647
- ProblemLog 类，584-587
- 问题
  - 问题详情页面，643，656
  - 问题选择页面，657
  - 问题更新页面，659
  - 按产品分类的问题页面，655
  - 作为产品支持应用程序的系统入口点，631，632
- Problems.jsp 视图页面，657-658
- ProblemSubmitAction 类，674-675
- 处理流程
  - 呼叫中心代理的角色，552，553，554
  - 开发人员的角色，552，553，554
  - 产品支持专员的角色，552，553，554
- 处理结果集，294，295
- 产品目录示例
  - 由 XSLT 生成，487-491
  - 使用 XML DOM 解析器搜索，464-472
  - XML SAX 1.0 解析器搜索，476-480
  - XML SAX 2.0 解析器搜索，480-485
- Product 类，561-565
- 产品支持应用程序，552-676
  - 其确认页面，649，657，660
  - 其控制器类，658-675
  - 其客户详情页面，639
  - 其客户搜索页面，636
  - 其数据模型，554-555
  - 为其开发 JSP 页面，555-556
  - 其中的电子邮件通知，715-719
  - 其模型类，557-631
  - 其中的 MVC 系统架构，556-676
  - 概述，552，676
  - 其问题详情页面，643，656
  - 其问题选择页面，657
  - 其问题更新页面，659
  - 其按产品分类的问题页面，655
  - 其处理流程，552-554，676
  - 产品搜索页面，650
  - 系统入口点，631，632
  - 模型测试框架，615-630
  - 其视图类，631-658
  - *另见* MVC 系统架构；视图页面
- 产品支持专员在处理流程中，552，553，554
- ProductParser 类，479
- ProductProblems.jsp 视图页面，653-657
- 产品
  - 按产品分类的问题页面，655
  - 产品搜索页面，650
  - 产品列表页面，653
  - 作为产品支持应用程序的系统入口点，631，632
- Products.jsp 视图页面，649-650
- products Web 应用程序，536
- ProductsList.jsp 视图页面，650-653
- ProductsListSelectAction 类，671-672
- ProductsSearchAction 类，670-671
- ProductsSelectAction 类，672-673
- Web 应用程序的编程模型，6-9
- 属性
  - bean，416-419
  - weather Observation bean 的属性，435
- <jsp:setProperty> 标签的 property 属性，432-433
- 协议无关的 servlet，34
- 协议，12
- pushBody 方法，808
- putValue 方法，785

## Q

- 处理流程中的质量保证，553，554
- QueryExample2.jsp 动态语法错误，320-323

## R

- 单选按钮
  - 定义，263
  - 作为输入字段，274-275
- 从远程网络资源读取输入流，705-710
- readLine 方法，740
- 只读变量，在变量声明中，122
- 通过请求分派消除冗余，134
- 注册 JDBC 驱动程序，305-307
- release 方法，808，813，816，826，828
- releasePageContext 方法，798
- removeAttribute 方法，736，747，752，786，809
- removeValue 方法，786，829
- 描述被包含 JSP 页面的请求属性，152，153
- 请求分派，134-160
  - 关于，134，160
  - 用于包含其他资源的组件，136
  - 创建 RequestDispatcher 对象，158
  - 转发请求，154-158
  - include 指令，136-140，153
  - 在 JSP 页面中合并动态内容，136
  - <jsp:include> 动作，83-84，136，140-153
  - 模型 1 与模型 2，159-160
  - 进程外 servlet 引擎模型，134-135
  - 重定向与请求分派，159
  - 选择 include 指令或 <jsp:include> 动作，153
  - servlet 上下文在其中的作用，535
  - 将内容从表示中分离，134，154-157
- 征求意见稿（RFC），定义，12
- 请求处理函数
  - 在 HTTP 跟踪工具中，511
  - 在 Tracer 调试工具中，519-525
- 请求头，836
- 请求隐式对象，97，98-100
- 请求行，15
- 请求作用域，411-412
- RequestDispatcher 类，729-730
- 请求
  - HTTP 请求示例，17-21
  - HTTP 请求模型，13-14
  - 发送 HTTP 请求，15-16
- 重置控件，276
- reset 方法，754，756
- resetBuffer 方法，754，757
- 资源映射，532-535
- ResourceBundle 对象，365
- 响应代码
  - 定义，16
  - 服务器的 HTTP 响应，16-17
  - 服务器接收 HTTP 请求，16
  - HTTP 响应代码表，834-835
- 响应头
  - 定义，836
  - 从静态字符串数组显示，146，147
  - <jsp:include> 动作无法设置，144
  - 使用 HTTP 设置和检索 cookie，364
- 响应隐式对象，97，99-100
- 表达式和脚本片段中的 response 变量，99-100
- 结果集，328-338
  - 定义，328
  - 从中提取数据，328-332
  - ResultSet 对象提供的 getXXX() 方法，331-332
  - RowSet 接口，338
  - 可滚动，332-336，337
  - 可更新，336-338
- ResultSetMetaData 方法，296，349-350
- 标签库中的可重用代码，185
- URL 重写，378-379，413
- RFC（征求意见稿）
  - 定义，12
  - HTTP 规范，12-13
- RowSet 接口，338
- run 方法，620-626
- runQuery 标签
  - 为其开发标签处理器，252-253
  - 在数据库查询示例中的功能，247，248
- 运行时处理
  - 区分编译和错误，499
  - 在运行时执行 BodyTag 接口时的异常，222
  - <jsp:include> 动作在运行时的特性，144-149
  - products Web 应用程序在运行时的结构，536
- 示例代码
  - Action 类的代码，660-662
  - 向门户网站网页添加自定义天气信息，444-448
  - BornBetween 查询示例，324-328
  - “联系我们”表单的代码，285-287
  - 将美元转换为加元的代码，705-710



## 索引

+   应用程序发送电子邮件的选项，710
    从远程网络资源读取，705-710
    从JSP页面发送邮件，710-719
    通过TCP/IP套接字使用SMTP发送邮件，711-712
    sun.net.smtp.SmtpClient类
    - 电子邮件选项，712
    提供动态内容的技术，704
service方法，26-27、729、731、766-767
<servlet>标签，30
用于Web应用程序部署的Servlet 2.2规范，530、549
Servlet API 2.3版，724-792
- 关于已弃用的类和方法，724
- javax.servlet类，724-759
- javax.servlet.http类，760-792
- 另请参阅 javax.servlet类；javax.servlet.http类
servlet上下文，44-47
- 功能，535
- ServletContext接口中的方法，45-47
- 存储引用，45
servlet引擎
- 调用destroy()方法，27
- 定义，24
- 功能，25
- 使用<jsp:include>操作调用URL，136
- 进程外模型，135
- 在隔离测试期间重启，500
- 另请参阅 servlets
Servlet接口，32、166、730-731
servlet请求对象，在进程外servlet引擎模型中，135
servlet响应对象
- 功能，41
- 在进程外servlet引擎模型中，135
servlet线程模型，47-49、403-406
- 默认线程模型，403-405
+   单线程模型，405-406
- 类型，403
- 另请参阅 单线程模型
ServletConfig类，731-732
ServletContext类，732-736
ServletContextAttributeEvent类，736-737
ServletContextAttributesListener类，737
ServletContextEvent类，738
ServletContextListener类，738-739
ServletException类，739-740
ServletInputStream类，740
部署描述符的<servlet-mapping>元素，533
ServletOutputStream类，740-743
ServletRequest类
- 使用静态String数组显示属性，146-147、148
- 方法，36-38、743-747
ServletRequestWrapper类，747-752
ServletResponse接口，41-43
ServletResponseWrapper类，755-757
servlets，24-52
- 类，31-47
- 将servlet源代码编译为Java类文件，494
- 控制器，662-666
- 创建燃油效率转换表，27-31、56-60
- 为隔离测试删除旧副本，499-500
- destroy方法，27
- 使用servlet显示错误消息和异常，179
- GenericServlet类，33-34
- HTTP会话，49-51
- HttpServlet类方法，34-36
- HttpServletResponse接口方法，43-44
- init方法，25-26
- javax.servlet.Servlet接口，32、166、730-731
- 生命周期，24-27
- 在servlet内复制方法定义，123
- 使用的方法，25
覆盖jspInit和jspDestroy方法，126-127
概述，24、52
标签处理器与servlet交互的示例代码，206-212
service方法，26-27
Servlet Context接口方法，45-47
ServletRequest接口，36-38
ServletResponse接口方法，41-43
将.jsp文件翻译为生成的servlet源代码，494
使用servlet的Web应用程序，6
*另请参阅* servlet引擎

会话和线程管理，354-414
应用程序注意事项，411-413
多线程应用程序，406-410
概述，354、413-414
servlet线程模型，403-406

会话API，369-390

会话跟踪，354-369

线程管理，390-403

会话API，369-390
包含的类，369
创建会话，370-372
销毁会话，373-374
使用会话API处理隐藏字段跟踪任务，374-378
使用会话API重写URL，378-379
会话绑定监听器，383-390
通过会话API管理会话，369、414
会话跟踪机制，371-372
使用会话API设置会话语言首选项，379-382
从会话存储和检索对象，372-373
*另请参阅* 会话

页面指令的session属性，172、181

会话绑定监听器，383-390

会话隐式对象，98、102-103

会话作用域，412

会话跟踪，354-369
使用cookies，363-369、371-372、413-414

使用隐藏字段，355-360
通过会话API管理，369、414
使用URL重写，360-363
使用会话API，369

sessionCreated方法，791

sessionDestroyed方法，791

sessionDidActivate方法，787

会话
将会话ID附加到URL，50
创建会话，370-372
将视图页面模型声明为会话bean，633
为隔离测试删除会话，500
销毁会话，373-374
使用会话API管理，369、371-372、414
设置会话语言首选项，379-382
从会话存储和检索对象，372-373
*另请参阅* 会话API

sessionWillPassivate方法，787

setAttribute方法，736、747、752、786、809、819

setBodyContent方法，812、813

setBufferSize方法，754

setCharacterEncoding方法，747、752

setComment方法，762

setContentLength方法，754、757

setContentType方法，754、757

setDateHeader方法，779、782

setDefaultFactory方法，798

setDomain方法，762

setFilterConfig方法，725

setHeader方法，779、783

setId方法，829

setInitParameters方法，826

setIntHeader方法，779、783

setLocale方法，754-755、757

setMaxAge方法，762

setMaxInactiveInterval方法，786

setPageContext方法，816、829

setParent方法，816、829

setPath方法，762

setRequest方法，752

setResponse方法，757

setSecure方法，763

setStatus方法，779、780、783

setTagExtraInfo方法，824

setTagInfo方法，821

setTagLibrary方法，824

setValue方法，763、829

setVersion方法，763

+   Shell类，616-630
    类方法，616-617
    构造函数，567-568
    建立数据库连接，628-630
    列出可用方法，627-628
    主读/执行循环，618-620
    概述，616
    打开字符行读取器的run()方法，620-626
    输入help命令，626-627
    与Model类协同编写，630-631

用于XML解析器的简单API。
    参见SAX解析器

+   单线程模型
    避免线程冲突，49、173
    定义，403、405-406
    图示，406
    局限性，174

SingleThreadModel类，758

SKIP_BODY返回码，205

+   SMTP（简单邮件传输协议），
    使用SMTP发送邮件，711-712

+   源代码
    为标签处理器编译，191
    使用include指令复制，139-140
    调试生成的servlet，500
    开发并翻译为servlet，494
    ControllerServlet源代码清单，662-666
    Model类源代码，588-615

特殊字符，非空白字符，265

+   SQL语句
    在JDBC数据库中执行，294、295

+   JDBC中的SQL语句接口，309-328
    另请参阅 Statement接口

使用Banner.jsp标准化头部，634

状态隐藏字段，359

+   Statement接口，309-328
    定义，294-295
    execute方法，312-314
    executeBatch方法，314-316
    executeQuery方法，311-312
    executeUpdate方法，310-311
    使用CallableStatement接口调用存储过程，295、322-328
    基本概述，309-310
    PreparedStatement子接口，317-322

静态文档服务器模型，6

HTTP中的状态行标记，16-17

+   使用CallableStatement接口调用的存储过程，295、322-328

+   String数组
    从数组显示响应头，146、147
    用于显示属性的ServletRequest方法，146-147、148

节点接口的子接口，461-466

提交按钮，275-276

sun.net.smtp.SmtpClient类，712

+   超类
    JSP超类示例，166-170
    声明中要求的方法，165
    JSP要求的接口，164-166
    另请参阅 类；以及按名称列出的具体超类

视图页面的支持页面，633-635

switch... case构造，237-240

+   switch标签
    在switch... case构造中的示例，237-240
    使用switch标签测试所需文本块的执行，245-246



## 同步

-   脚本变量，235–236
-   线程，399–403

## 词法作用域

236–246

## 语法与语义

64–87

-   使用预处理语句避免动态语法错误，320–322
-   WebClient 的调用语法，509
-   注释，68–69
-   声明，71–73，86–87，112
-   定义，64
-   自定义标签的语法定义，186–187
-   指令，65–68，83
-   JSP 页面示例，78–87
-   表达式，69–70，85
-   FORM 元素的语法，263–264
-   JSP 页面的形式，54–56，64，194
-   HTTP 头部语法，836
-   隐式对象，74–75
-   页面指令的 `import` 属性语法，170–171
-   `include` 指令语法，136–138
-   INPUT 标签的语法，270–271
-   JDBC URL 参数语法，308
-   `<jsp:setProperty>` 标签语法，430
-   `<jsp:useBean>` 标签语法，425–430，448
-   声明的方法定义语法，122
-   在调试中的必要性，87
-   脚本小程序，70–71，84，112
-   select 和 option 标签的语法，283
-   页面指令的属性设置，162
-   标准操作，75–77，83–84
-   转发表示的语法，154
-   标签扩展的语法，78
-   `taglib` 指令的语法和属性，199
-   URL 参数语法，360
-   XML 语法，75，453–454

## 案例研究的系统入口点

631，632

## System.out.println 方法

500，501

## 表格

规范宽单元格，124–126

## 标签类

815–816

## 标签扩展

184–258

-   标签处理器的动作，194–196
-   自定义标签的好处，184–186
-   标签无需体内容，196
-   体标签处理器 API，219–223
-   体标签处理器生命周期，223–226
-   协作标签，236–246
-   在标签库描述符中创建自定义标签条目，187–188
-   定义自定义标签，186–187
-   定义脚本变量，186，226–236
-   数据库查询示例的实现，247–258
-   在 JSP 页面中引入自定义标签，192–194
-   标签处理器的生命周期，196，202–212
-   概述，184
-   语法，78
-   标签属性定义，212–219
-   标签处理器 API，200–202
-   标签库，197–200
-   为自定义标签编写标签处理器，188–191
-   *另请参阅* 自定义标签；标签处理器；标签库

## 标签处理器 API

200–202

-   Tag 接口的生命周期方法，200–201
-   TagSupport 类，202

## 标签处理器

-   体标签处理器 API，219–223
-   体标签处理器生命周期，223–226
-   编译其源代码，191
-   用于 connect 标签，250–252
-   用于数据库查询示例，249–258
-   定义，258
-   定义标签属性，212–219
-   用于 forEachRow 标签，254–256
-   功能，196
-   用于 getField 标签，256–257
-   JSP 容器如何转换 JSP 页面，55，194–195
-   生命周期，196，202–205
-   作为标签库的一部分，197
-   用于 runQuery 标签，252–253
-   实现 BodyTag 接口时的运行时异常，222
-   getWebServerHeader 的示例代码，206–212
-   容器生成的标签相关代码，195
-   为自定义标签编写，188–191
-   *另请参阅* 体标签处理器 API；标签扩展；标签处理器 API

## 标签库

197–200

-   定义，184，197，258
-   映射到 web.xml 文件，199–200
-   作为可重用代码的来源，185
-   TLD 元素，197–198

标签库描述符。*参见* TLDs

## TagAttributeInfo 类

816–818

## TagData 类

-   方法，818–819
-   传递参数，236，237

## TagExtraInfo (TEI) 类

227–235

-   关于，227–229
-   方法，228，820–821
-   使用示例代码，229–235
-   验证标签属性，236

## TagInfo 类

821–824

taglib。*参见* 标签库

## Taglib 指令

-   定义，68，192
-   使用其定位 TLDs，195
-   将标签库映射到 web.xml 文件，199–200
-   语法和属性，199

## TagLibraryInfo 类

824–825

## TagLibraryValidator 类

826

## 标签

-   编码 `<servlet>`，30
-   DTD 的作用，455
-   XML 开始和结束标签的语法，453–455
-   XML 标签，452
-   *另请参阅* 自定义标签；标签扩展

## TagSupport 类

-   关于，202
-   构造函数和方法，827–829
-   阅读用于页面上下文和体上下文变量信息的源代码，190
-   用作注释代码的标签处理器，205

## TagSupport 父类

190

## TagVariableInfo 类

829–831

TEI。*参见* TagExtraInfo 类

## 测试与调试

494–528

-   构建心智模型，494
-   调试工具，500–528
-   隔离故障组件，499–500
-   在 MVC 架构中，615
-   概述，494
-   预编译以区分编译时和运行时错误，499
-   产品支持应用的 Shell 类，616–630
-   使用 switch 标签测试文本块执行，245–248
-   JSP 页面形式的翻译和编译，494–499
-   开启/关闭错误消息，495
-   *另请参阅* 调试工具；Shell 类

## 文本

-   作为输入元素，271–272
-   文本条目元素，262
-   Textarea 元素，284

线程模型。*参见* Servlet 线程模型

## 线程

390–403

-   避免与 SingleThreadModel 接口冲突，49，173
-   创建和启动，391–398
-   实例变量及其安全性，118–122
-   SingleThreadModel 接口的限制，174
-   管理，390–391
-   在后台打印计数器值，423–424
-   同步，399–403
-   线程概念，391
-   线程模型，47–49
-   Servlet 线程模型的类型，47–49，403–406

## 超时

373

## TLDs 子目录

531–532

## TLDs（标签库描述符）

-   常用子目录，531–532
-   作为 web.xml 部署描述符的内容，542
-   在其中创建自定义标签条目，187–188
-   用于数据库查询示例，248–249
-   元素，197–198
-   使用 `taglib` 指令定位，195
-   作为标签库的一部分，197

## Tomcat

-   检测和修复其中生成的编译错误，496–499
-   在其中运行 .war 文件，537

## toString 方法

818，824

## Tracer

510–528

-   配置以监控 Web 客户端和服务器，510–511
-   解析选项，518
-   RequestHandler，519–525
-   设置 Web 服务器代理，511–519
-   在 HTTP 认证中的用途，526–528

## JSP 页面形式中的翻译和编译

494–499

## 表单验证的触发器

285

## TryCatchFinally 类

831

## 开启/关闭错误消息

495

## `<jsp:useBean>` 标签的类型规范

-   仅指定 class，427–428
-   指定 type 和 beanName，429–430，431
-   指定 type 和 class，428–429
-   仅指定 type，426–427
-   有效组合，426

## UnavailableException 类

758–759

## UnavailableException 子类

26

## 可更新的结果集

336–338

## URI（统一资源标识符）

-   定义，15
-   检索原始 URI，150–153

## URLConnection 类

682

## URLs（统一资源定位符）

-   关于 URL 类，680–681
-   附加会话 ID，50
-   浏览器解释 URL 中的应用程序名称，533–534
-   java.net.URL 类的方法，681
-   使用其进行资源映射和文档定位，532–535
-   重写，378–379，413
-   通过重写进行会话跟踪，360–363
-   Web 应用程序名称的标准形式引用，533
-   参数语法，360
-   URL 连接的类型，680–684

## Util 类

613–615

## Validate 方法

826

## 验证

-   HTML 表单，285–287
-   标签属性，236

## `<jsp:setProperty>` 标签的 value 属性

433–434

## valueBound 方法

789

## valueUnbound 方法

789

变量声明。*参见* 变量

## VariableInfo 类

831–832

## 变量

-   只读变量的优势，122
-   声明和初始化类和实例变量，117–122，131–132
-   定义脚本变量，186，226–236
-   隐式变量，74–75
-   线程安全与实例变量，118–122

## 版本

-   Java J2EE，8，9
-   SAX 解析器接口，473

## 视图页面

631–658

-   应用程序流程和视图/控制器交互，631–633
-   Confirm.jsp，647–649
-   为其创建错误模块，634–635
-   使用 Banner.jsp 创建标准化页头，634
-   CustomerList.jsp，635，637–638
-   Customers.jsp，635–636
-   在 InitModel.jsp 中将模型声明为会话 Bean，633
-   作为系统的表示层，557
-   Problem.jsp，635，643–647
-   Problems.jsp，635，657–658
-   ProductProblems.jsp，653–657
-   支持页面，633–635
-   *另请参阅* MVC 系统架构

## Web 应用程序

6–9，530–549

-   定义，530
-   其中的部署描述符，538–547
-   JavaServer Pages 的开发，8
-   目录结构，530–532
-   编程模型的演进，6–9
-   Servlet 上下文的功能，535
-   万维网的历史发展，6
-   调试中对语法的必要了解，87
-   资源映射，532–535
-   部署描述符示例，547–549
-   从客户端应用转向服务器端应用，9
-   在其中分离内容与表示，134，154–157
-   使用 Servlet 2.2 规范标准化部署，530，549
-   Web 归档（.war）文件，535–537，549

## Web 归档（.war）文件

535–537，549

## Web 浏览器

-   作为客户端，680
-   解释 URL 中的应用程序名称，533–534
-   插件，690–691
-   在 CGI 脚本响应中的作用，7
-   模拟以进行调试，504–510
-   用错误消息替代 Servlet 错误，495
-   *另请参阅* cookies

## .war 文件

535–537，549

## 天气信息

-   为门户网站网页自定义，444–448
-   使用 Bean 自定义，434–444
-   为美国国家气象局本地化网页，442
-   天气观测 Bean 的属性，435

## 天气观测 Bean

435

## 网页

-   向门户网站添加自定义天气信息，444–448
-   用于美国国家气象局显示本地化条件，442
-   从外部源检索数据的可靠性，436
-   Servlet 与网页，24

## Web 服务器

-   配置 HTTP tracer 进行监控，510–511
-   连接的 HTTP 协议，14
-   其中的进程外 Servlet 引擎模型，135
-   资源映射和文档根目录，532
-   重启以进行隔离测试，500
-   线程操作，391

## web.xml 文件

-   作为 Web 应用程序中的部署描述符，457，538–547
-   将标签库映射到其中，199–200
-   在 Web 应用程序目录结构中，531



## 876 JSP 完全参考手册

`<web-app>` 元素
- 其内容，539
- 在其中指定元素的顺序，538
WebClient，504-510
- 从命令行调用，505
- 用于监控的 HTTP tracer 配置，510-511
- 调用语法，509
- 与服务器的典型交换，509-510
WEB-INF 根目录，531
WebModel 类，611-613
脚本小程序中的空白符，91
writeOut 方法，811
为 HTML 表单编写验证函数，286-287
WWW（万维网），6

- 区分其中的内容与表示，453
- 文档类型定义（DTD），454-457
- DOM 解析器，457，458-472，491
- 部署描述符的元素，538-547
- 从 JSP 页面生成 XML 文档，684-689
- 概述，452-457
- 部署描述符示例，547-549
- SAX 解析器，472-485，491
- 语法，75，453-454
- XML 解析器的类型，457
- 另请参阅 DOM 解析器；解析器；SAX 解析器

## X

Xerces-J 1.2.1 对 SAX 2.0 的支持，481
XML（可扩展标记语言），452-491
- 使用 XSLT 添加样式信息，486-491

### XSL（可扩展样式表语言）
- 样式表，486
### XSLT（XSL 转换），486-491
- 关于，486
- 关键指令，486-487
- 生成产品目录的示例代码，487-491

## 国际联系方式

**澳大利亚**
McGraw-Hill 图书公司澳大利亚有限公司
电话 +61-2-9417-9899
传真 +61-2-9417-5687
http://www.mcgraw-hill.com.au
books-it_sydney@mcgraw-hill.com

**新加坡（服务亚洲）**
McGraw-Hill 图书公司
电话 +65-863-1580
传真 +65-862-3354
http://www.mcgraw-hill.com.sg
mghasia@mcgraw-hill.com

**加拿大**
McGraw-Hill Ryerson 有限公司
电话 +905-430-5000
传真 +905-430-5020
http://www.mcgrawhill.ca

**南非**
McGraw-Hill 南非
电话 +27-11-622-7512
传真 +27-11-622-9045
robyn_swanepoel@mcgraw-hill.com

**希腊、中东、北非**
McGraw-Hell Hellas
电话 +30-1-656-0990-3-4
传真 +30-1-654-5525

**英国和欧洲（南欧除外）**
McGraw-Hill 教育欧洲
电话 +44-1-628-502500
传真 +44-1-628-770224
http://www.mcgraw-hill.co.uk
computing_neurope@mcgraw-hill.com

**墨西哥（同时服务拉丁美洲）**
McGraw-Hill Interamericana Editores S.A. de C.V.
电话 +525-117-1583
传真 +525-117-1589
http://www.mcgraw-hill.com.mx
fernando_castellanos@mcgraw-hill.com

**所有其他查询请联系：**
Osborne/McGraw-Hill
电话 +1-510-549-6600
传真 +1-510-883-7600
http://www.osborne.com
omg_international@mcgraw-hill.com

版权所有 © 2001 The McGraw-Hill Companies, Inc. 点击此处查看使用条款。
