
# Learning Node.js：JavaScript Web 应用构建实用指南

Node.js 让创建快速、紧凑且可靠的 Web/网络应用以及 Web 服务器变得变得简单得多，并迅速成为现代 Web 开发者不可或缺的工具。

**学习 Node.js** 汇集了掌握 Node.js 平台所需的知识和 JavaScript 代码，帮助你以极人的速度和可扩展性构建服务器端应用程序。

你将从安装和运行 Node.js 开始，理解它使用的扩展模块，并快速编写你的第一个应用。接下来，在基础之上，你将编写功能更强大的应用服务器，并使用当今最强大的 Node.js 工具和模块对其进行扩展。最后，你将发现关于测试、在生产服务器上运行 Node.js 代码以及编写命令行实用程序的当今最佳实践。

在整本书中，Marc Wandsneider 将通过逐行讲解精心设计的示例来进行教学，演示了创建高效高效应用和服务器的成熟技术。

> 如果你是一个想要用 Node.js 构建服务器端 Web 应用的开发者，《学习 Node.js》是你通往成功的最快路径。

- 熟通 Node.js 非阻塞 I/O 和异步编程
- 处理更多请求并增加应用的灵活性
- 使用并编写自己的模块
- 执行常见的 JSON/Web 服务器任务
- 使用浏览器通过 Ajax 调用和模板库即时生成页面
- 使用 Express 框架简化开发
- 使用流行的 NoSQL 和关系型数据库创建数据库后端
- 在 Unix/OS X Windows 服务器上部署和运行 Node.js 应用
- 利用多处理器硬件的优势
- 支持虚拟主机和 SSL/HTTPS 安全
- 测试匹配同步、异步和 RESTful 服务器 API 功能的 Node.js 程序

请在 informit.com/register 注册你的书籍，以便在可用时方便地获取更新、下载和更正。

**MARC WANDSNEIDER**，Google 高级开发者倡导，拥有超过20 年的开发经验，是两编程书籍和 LiveLessons 视频培训课程的作者。他毕业于麦吉尔大学计算机学院，曾在微软工作过五年，最近在中国生活了七年，运营针对 Android 和 iOS 的小型移动开发初创应用。

持续学习

Web 开发基础指南

## 学习

Objective-C 与 iOS 开发指南

CocosD、Box2D 和 Chipmunk 完全指南

TIM WRIGHT

ROBERT STRASSBURG

AY MUNDGLICH

非常感谢 Tina，她一直都在。

# 致谢

我要感谢所有的 Mark（这似乎是一个常见的名字），他们帮助我使这本书和其他项目成为现实。拷贝编辑们都非常优秀且乐于帮助。

对 Bill Glover 和 Idriss Juhoor 的卓越技术和风格评审表示深表谢意。

最后，非常感谢 Tina。

# 作者简介

Marc Wandsneider 共同创立了 Adylica，这是一家领先的专注于大规模可扩展 Web 和移动应用设计与开发的专家公司。他遍布全球担任软件项目和团队的首席经理提供咨询。他毕业于麦吉尔大学计算机学院，曾在微软工作过五年，在 Visual Basic、Visual C++ 和 .NET Windows Forms 团队开发并管理开发者。作为 SourceLabs 的合同开发人员/架构师，他构建了开源 SWiK Wiki 平台。他编写了《PHP and MySQL LiveLessons》以及《基于 PHP and MySQL 的核心 Web 应用开发》。

- 增加灵活性：GET 参数 79
- 使用模块 93
- 创建你的模块 96
- 解决方案 105
- 提供静态内容 124
- JavaScript 加载器/引导器 126
- 使用 146
- 核心数据 196
- 代理支持 222
- 总结 230

## 11 命令行编程 233

- 运行命令行脚本 233
- UNIX 和 Mac 234
- Windows 235
- 脚本与参数 236
- 基础缓冲输入 242
- 非缓冲输入 243
- Readline 模块 244
- 进程操作 247
- 简单进程创建 248
- 使用 Spawn 进行高级进程创建 249
- 总结 250

索引 262

序言

在 2009 年，一位名叫 Ryan Dahl 的家伙在一家名为 Joyent 的公司工作，那是一家位于加利福尼亚的云和虚拟化服务公司。他当时寻求开发推送能力

# 到底什么是 Node.js？

他想构建像 Gmail 那样的 Web 应用程序，但他发现看到的大多数方案都不太合适。他最终选择了 JavaScript，因为它缺乏健壮的输入输出（I/O）模型（这意味着他可以自己编写一套新的），并且发现快速且完全可编程的 V8 运行时现已可用。

受 Ruby 和 Python 社区类似项目的启发，他最终利用 Chrome V8 运行时和一个名为 libuv 的事件处理库，创造了名为 Node.js 的新系统的第一个版本。Node.js 的核心方法或创新在于它完全围绕事件驱动的非阻塞编程模型构建。简而言之，你永远不需要（或者很少）编写阻塞代码块。

如果你的应用程序为了处理请求并生成响应需要运行数据库查询，它会运行请求并告诉 Node.js 在响应返回时做什么。在此期间，Node.js 可以自由地处理其他请求，或者处理可能需要的任何其他任务，例如清理数据或运行分析。

通过这种处理请求和工作方式的简单改变，你能够轻松地在没有多少处理或内存资源的机器上，同时处理成百甚至数千个请求。Node 运行在单个进程中，你的代码大部分运行在单线程中执行，因此其资源需求远低于许多其他平台。

这种速度和能力伴随着一些警告，你需要充分意识到这些点，这样你就可以“睁开眼睛”开始使用 Node.js 了。

最重要的是，这种新模型与你以前可能看到的不同，有时会让你感到有些困惑。在你完全理解一些核心概念之前，你在 Node.js 中看到的某些代码可能看起来很奇怪。本书的大部分内容致力于讨论许多程序员使用的代码模式，用以应对 Node.js 使用的异步非阻塞编程方式带来的挑战，以及如何开发你自己的模式。

这种编程模式的另一个局限性是，它确实侧重于那些使用许多不同进程、服务器或服务处理许多不同事情的应用程当你在阅读本书时，我们会指出哪些区域比其他区域更不稳定，并建议你可以缓解 API 变化风险的方法。好消息是 Node.js 已经拥有了一个庞大且活跃的用户社区，以及大量的邮件列表、论坛和用户组。当你处理数据库、缓存服务器、文件系统、应用程序服务器等的连接时，Node.js 真正大放异彩。然而，它的另一面是，对于编写执行严肃、长时间计算的服务器来说，它并不一定是最优环境。对于这些任务，如果某个请求需要大量时间来生成复杂的密码摘要或处理图像，Node 的单进程单线程模型可能会产生问题。在需要进行更多计算密集型工作的情况下，你需要小心应用程序如何使用资源，或者可能考虑将这些任务外包给其他平台，并将其作为服务运行，供你的 Node.js 程序调用。

最后，Node.js 是一个相当较新的平台，并且处于活跃开发中。（截至截至 2013 年 2 月）它尚未达到 1.0 版本，并且不断发布新版本，有时速度快到令人眼目缭眩。

# 引言

为了减少这些频繁更新带来的随机性和困扰，开发者开始对系统的部分内容标记不同程度的稳定性，范围从“不稳定”（unstable）到“锁定”（Locked）。运行时中稳定（Stable）或锁定（Locked）部分的更改很少，并且涉及大量的社区讨论，以确定是否会产生过大的痛苦。在你阅读本书时，我们会指出哪些区域比其他区域不稳定，并建议你可以缓解 API 变化风险的方法。

好消息是，Node.js 已经拥有了庞大且活跃的用户社区，以及许多致力于推广该平台并在需要时提供帮助的邮件列表、论坛和用户组。简单的 Google 搜索几秒钟就能解决你 99% 的问题，所以永远不要害怕寻找！

我写这本书的假设是你习惯于计算机编程，并熟悉至少一种编程语言（如 Java、C/C++、PHP 或 C#）的功能和语法。虽然不需要成为专家，但你可能已经超越了“在 Y 天内学会 X”这种级别的任务。

如果你像我一样，可能写过一些 HTML/CSS/JavaScript，因此“用”过 JavaScript，你可能并不对它非常熟悉，只是在很大程度上参考了博客文章或邮件列表中的代码。事实上，由于其笨拙的 UI 和令人沮丧的浏览器不兼容问题，提到 JavaScript 时你甚至会皱皱。没关系——到本书第一部分的结束时，对这种语言令人反恶的记忆将成为过去，我希望你能够轻松地面带微笑写出你的第一个 Node.js 程序！

我假设你对 Web 应用程序如何工作有基本的了解：浏览器向远程服务器发送 HTTP 请务；服务器处理请求并发送带有成功或失败代码的响应，并可能随响应一起发送一些数据（例如用于渲染页面的 HTML，或者可能是包含该请求数据的 JavaScript 对象表示法，即 JSON）。你过去可能连接过数据库服务器，运行过查询，并等待结果行等。当我开始在示例和程序中描述超出这些范围的内容时，我会对任何新或不常见的内容进行解释并刷新每个人的记忆。

本书在很大程度上是教程性质的。我尝试平衡解释与代码，以尽可能地进行演示，并避免对一切都进行冗长、乏味的解释。对于我认为更好的解释更有趣的情况，如果你有兴趣，我可能会引导你参考某些资源或其他文档以学习更多（但这绝非必须）。

本书分为四个主要部分：

-   **第一部分：学习走路——** 你开始安装和运行 Node，重新查看 JavaScript 语言以及 V8 和 Node.js 使用的扩展，然后你写出你的第一个应用程序。

-   **第二部分：学习运行——** 在本书的这一部分，你开始开发更强大、有趣的服务器，我开始教你编写 Node.js 程序的一些核心概念和实践。

-   **第三部分：大出杀器——** 在这一部分，你将查看用于编写 Web 应用程序的一些强大工具和模块，例如 Web 服务器和数据库服务器的通信。

-   **第四部分：充分利用 Node.js 的价值——** 最后，我通过查看一些其他高级主题来结束本书，例如如何在生产服务器上运行你的应用程序、如何测试代码，以及如何使用 Node.js 编写命令行工具！

在你阅读本书的过程中，请花时间打开文本编辑器并输入代码，看看它们在你 Node.js 版本中是如何运行的，并在过程中开始编写和开发你自己的代码。你在阅读本书时会开发自己的小型照片共享应用程序，我希望这能为你提供一些你可以编写的内容的灵感或想法。

书中大部分示例的源代码可以在 github.com/marwan/LearningNodeJS 找到。强烈鼓励你下载并运行，但不要剥夺自己输入某些代码进行尝试的机会。

GitHub 代码包含了一些可以运行的示例，并已在 Mac、Linux 和 Windows 上通过最新版本的 Node.js 测试。如果 Node 的新更新需要更新源代码，我会在那里发布更改和说明，请务必每几个月下载一次。

如果你对书中的代码有任何问题或困难，随时访问 github.com/marwan/LearningNodeJS 并添加一个 issue（问题）；它们将受到监控并快速回答。

- 3 异步编程 49

在本章中，你将直接进入实践，在你的机器上安装 Node.js，并在进一步学习该语言和编写网络化应用之前，确保它运行正常。在本章结束时，你应该已经在电脑上安装并运行了 Node，已经编写了几个小型的测试程序进行尝试，并学会了如何使用内置的 Node 调试器（debugger）。

让我们从查看 Windows 上的安装开始。Mac 和 Linux 用户可以随意跳过到相应的子章节，除非你同时拥有这两种类型的机器。

## 在 Windows 上安装

要在 Windows 机器上安装 Node.js，你可以使用 nodejs.org 网站提供的方便安装程序。访问下载（Download）页面，然后根据你运行的平台下载 32 位或 64 位的 Windows 安装程序 (.msi)。我展示的是 Windows 7/64 位的安装过程。

下载好 MSI 文件后，双击它。你会看到一个与图 1.1 所示类似的设置程序。

阅读并接受许可协议（License Agreement），然后点击安装（Install）。因为安装非常快速且无痛苦，几秒钟后你就可以点击完成（Finish）来结束安装。

要测试 Node 软件的安装情况，可以使用 Windows 命令行提示符 cmd.exe。（如果你使用的是 PowerShell，它同样适用）。如果你不熟悉此操作，可以通过进入“开始 / 运行”然后输入 `cmd` 来启动它，如图 1.2 所示。

图 1.1 Windows 安装程序

图 1.2 启动 Windows 命令行提示符

你会看到一个命令行解释器，如图 1.3 所示。如果你想了解更多关于使用命令行提示符的信息，可以在互联网上搜索“学习使用 Windows cmd.exe”或“开始使用 PowerShell”（如果你正在运行 Windows 7）来获取更多信息。

图 1.3 Windows 命令行提示符

为了确保 Node 安装正确，请在命令行窗口中输入 **node --version**。你应该能看到如图 1.4 所示的输出。

图 1.4 验证 Node 是否正确安装。检查版本号。

命令行提示符窗口应该打印出你几秒钟前安装的 Node 版本号（如果数字与你看到的不匹配请担心——事实上，如果匹配了我反而会惊讶！）如果你没有看到这个版本号，或者看到输出说“node’不是内部或外部命令”（参见图 1.5），说明出了问题，你应该执行以下操作：

- 检查“控制面板 / 程序”，查看安装是否真正完成。如果没有，尝试重新安装，并密切关注发生的情况。可能发生了某些错误。

- 检查 `Program Files\nodejs` 并确保 `node.exe` 确实在那里。如果不在，尝试重新安装。（如有必要，请卸载旧版本。）

- 确保 `node.exe` 在你的 PATH 环境变量中。在命令行提示符中，Windows 有一个目录列表，当你输入程名称时会在其中搜索。你只需通过在命令行提示符窗口中输入 `path` 来查看。它应该显示与图 1.6 类似的内容。特别注意最后两个高亮的目录名称。所有与这些非常相似的内容都应该在 PATH 中。

- 如果 `Program Files\nodejs` 和 `Users...\AppData\` 不在 PATH 中，但这些文件夹存在，你可以通过将它们添加到环境变量来手动添加到 PATH。你可以在系统控制面板窗口中进行此操作。点击“高级设置”，然后点击“环境变量”。然后将 npm 文件夹的路径（类似于 `C:\Users\Username\Local\npm`）添加到“用户变量”的 `PATH` 中，并将 Node.js 文件夹的路径（类似于 `C:\Program Files\nodejs`）添加到“系统变量”的 `PATH` 中。注意，取决于电脑的配置，npm 文件夹可能是 `Username\Remote\npm` 而不是 `Username\Local\npm`。

在确认你已安装并运行 `node.exe` 后，你就可以编写 JavaScript 了。

图 1.5 node 不是内部或外部命令。

图 1.6 检查你的 PATH 环境变量

虽然有两种方法可以在 Mac 上安装 Node——使用PKG 安装程序或从源码编译——但我将介绍前者。

要在 Mac 上安装 Node 的快捷方法是使用 nodejs.org 网站提供的 PKG 安装程序。下载安装程序后，双击它，你会看到如图 1.7 所示的内容。

在命令行提示符中输入 `echo $PATH` 以确保 `/local/bin` 在这里。如果不是，你应该编辑你的 `~/.bash_profile` 文件（如果不存在则创建一个）并添加：

```
PATH=$(PATH):/local/bin
```

关闭终端窗口，打开另一个，验证 `/local/bin` 现在已在你的 PATH 中。你应该能够输入

```bash
node --version
```

并看到如图 1.8 所示的内容：

```
marcw@hostname:-$ node --version
v0.10.3
client:LearningNode$
```

如果版本号与你看到的不匹配请担心。对于 Ubuntu 7 用户，打开 Terminal：

图 1.7 运行 Node 的安装程序

图 1.8 确保你的路径设置正确。

在所有操作运行完成后，你应该能够再次输入

g++

并让它能够正常工作。

以下指令是过去几年在 Ubuntu Linux 版本上使用的方法，并假设你正在使用 (bash) 作为你的主 shell。首先开始创建一个临时空间来下载和编译：

```bash
cd
mkdir -p src/scratch
cd src/scratch
```

下一步是下载并解压 Node 源码。你可以使用 curl 或 get 完成：

```bash
curl http://nodejs.org/dist/v00.10.1/node-v00.10.1.tar.gz -o node-v00.10.1.tar.gz
tar xf node-v00.10.1.tar.gz
cd node-v00.10.1
```

接下来，你运行配置脚本为编译做准备：

./configure

你可以让它使用默认的 /usr/local 作为安装点，因为它是运行该软件的良好位置。如果你想将其安装在其他地方，可以使用 --prefix 切换来配置脚本，如下所示：

./configure --prefix=/opt/nodejs

配置脚本应该执行得很快，并在完成后打印出一些 JSON。现在你可以构建产品了。输入以下命令并给自己自己泡杯咖啡（或两杯，取决于你机器的快慢）：

```bash
make
```

在 make 成功完成后（如果失败，请在 Google 上搜索该问题，因为你几乎是第一个看到它的人），你就可以将软件安装到你选择的前缀中（如果你没有选择，则为 /usr/local）：

sudo make install

完成后，你应该可以直接输入

```bash
node --version
npm --version
```

并获得类似于下所示的输出：

```
marcw@hostname:-$ node --version
v00.10.1
marcw@hostname:-$ npm --version
1.1.65
```

## 运行 Node.js 和 "Hello World!"

在你的机器上使用 Node.js 有两种主要方法：使用 Node Shell，或者将 JavaScript 保存到文件中并运行这些文件。

你第一次运Node.js 的方式是使用 Node Shell，它通常被称为 Node REPL——REPL 代表“读取-评估-打印-循环”（Read-Eval-Print-Loop）。这是在 Node 中快速测试东西的极佳方法。如果你不确切某个函数应该如何使用，可以直接使用 REPL 并输入内容看看会发生什么。

要启动 Node Shell，你只需在你正在使用的任何 shell 中输入 node：

```bash
client:node marcw$ 
```

> > 是你所获得的所有响应。你可以立即开始输入一些代码：

```javascript
> console.log("Hello World!");
```

Hello World!

undefined

输出的第一行是你刚刚执行的代码的结果。在这种情况下，你使用了 Node 全局变量 `console` 及其 `log` 函数来打印出 Hello World!（关于 `console` 和其他全局变量的更多信息，请参见下一章。）语句的输出如预期的是 Hello World!，并为你打印了出来。

输出的最后一行始终是前一个语句的结果值。每个语句、函数调用或表达式都有一个关联的值，该值会在 Node shell 中为你打印出来。如果没有求值的表达式或函数没有返回任何特定值，则会返回特殊值 `undefined`。

要退出 REPL，你只需按 Ctrl+D（Windows 上也一样）。

如果你在 Node REPL 中看到三个点 (...)，这意味着它正在等待你提供更多输入以完成当前的表达式、语句或函数。如果你不完全理解为什么是省略号，可以输入 `.break`（带句号）来退出：

```javascript
> function () {
...
  ...what?
  ...break
}>
```

运行 Node.js 代码的另一种选择是简单地使用你喜爱的文本编辑器将 JavaScript 代码写入文件，然后通过命令行使用 `node` 命令编译并运行该代码。

为了演示这一点，请将以下内容保存到名为 `hello.js` 的文件中：

```javascript
/**
* 让我们变得好社交一点吧。
 */
console.log("Hello World!");
```

现在，你可以从命令行执行此文件：

```bash
node hello.js
```

你应该会看到此输出：

Hello World!

由于你不在 Node shell 中，所以你不会获得关于所执行代码返回值的任何信息。

现在你准备好写一些更有趣的内容并创建一个小型的 Web 服务器了。幸运的是，Node 让这项变得极其简单。将以下内容输入并保存到名为 `web.js` 的文件中：

```javascript
var http = require("http");

function process_request(req, res) {
  var body = 'Thanks for calling!\n';
  var content_length = body.length;
  res.writeHead(200, {
    'Content-Length': content_length,
    'Content-Type': 'text/plain'
  });
  res.end(body);
}
```

```javascript
var s = http.createServer(process_request);
s.listen(8080);
```

要运行它，只需输入：

```bash
node web.js
```

你的电脑现在在 8080 端口上有一个 Web 服务器。要测试它，你可以使用命令行程序 `curl`（Windows 预装了它）。直接输入：

```bash
curl -i http://localhost:8080
```

你现在会看到类似下面的内容：

+ HTTP/1.1 200 OK

Content-Length: 20

Content-Type: text/plain

Date: Tue, 15 Feb 2013 03:05:08 GMT

Connection: keep-alive

Thanks for calling!

默认情况下，Windows 没有自带任何获取 URL 内容的命令行工具。你可以下载 curl（我以后就称之为 curl）。

你可以通过访问 http://curl.se/download/ 并查找“Win32 - Generic”部分来下载二进制文件，解压并将 `curl.exe` 放在你的 PATH 或用户目录。要启动它，在命令提示符或 PowerShell 中只需输入：

```bash
curl --help
```

如果你在 Windows 上无法运行 curl，wget 是一个极佳的替代方案。从 http://users.beget.net/-bpu/wget/ 下载它。

它的工作方式与 curl 基本相同，但命令行参数有所不同。要了解更多信息，请查看帮助：

```bash
wget --help
```

Content-Type: text/plain

Date: Tue, 30 Oct 2012 04:42:44 GMT

Connection: keep-alive

你不再会收到“Thanks for calling!”消息，而且你会发现此时的 Content-Length 标头并不是你预期的那个值。

对于像这样简单的程序，错误很容易发现，但在更大的程序中，弄清楚这些问题可能很困难。为了帮助这一点，Node.js 在 `node` 程序中包含了一个调试器。要使用它，你只需要在程序名称之前加上 `debug` 标志位即可：

```js
node debug debugging.js
```

你应该能看到如下内容：

```
client:Chapter01 marcw node debug debugging.js own< debugger listening on port 5858
connecting...
break in debugging.js:1
1 var http = require("http");
2
3 function process_request(req, res) {
d>
```

你在 Node 调试器可以使用几个关键命令：

- *cont*-继续运行。

- *next*-跳到下一个语句。

- *step*-进入下一个语句（如果可能的话；否则直接跳过）。

- *out*-跳出当前执行函数。

- *backtrack*-显示当前的执行帧或调用堆栈。

- *repl*-启动 Node REPL 以允许你查看变量值并执行代码。

- *watch(expr)*-将表达式添加到监视列表，每你在调试器中单步或移动任何内容时，该列表都会显示。

- *list(n)*-列出调试器中当前停止行前后的 n 行源代码。

现在，程序中的 `Content-Length` 可能出了问题，你可以在 `var content_length = body.length;` 这一行或第 5 行设置断点：

debug> setbreakpoint(5)

```
1 var http = require("http");
2
3 function process_request(req, res) {
4 var body = 'Thanks for calling!\n';
```

```js
* 5 var content_length = body.length;
6 res.writeHead(200, {
debug>
```

现在第 5 行旁边有一个 `*`，表示这里有一个断点。当你启动调试器时，程序会停止在第一行。你可以使用 `cont` 命令恢复执行：

```
debug> cont
debug>
```

现在，去另一个终端窗口或命令提示符并输入

`curl -i http://localhost:8080`

你应该立即注意到两件事：

- 1. curl 并没有立即返回。

- 2. 在你的 node debug 会话中，你现在看到

break in debugging.js:5

3 function process_request(req, res) {

4 var body = 'Thanks for calling!\n'

5 var content_length = body.length;

6 res.writeHead(200, {

7 'Content-Length': content_length,

8 'Content-Type': 'text/plain'

你可以跳过这一行：

```js
debug> next
break in debugging.js:7
* 5 var content_length = body.length;
6 res.writeHead(200, {
7 'Content-Length': content_length,
8 'Content-Type': 'text/plain'
9 }}
```

现在启动 Node REPL，以便你可以检查一些变量值：

```
debug> repl
Press Ctrl + C to leave debug repl
>
```

让我们分别查看 `body` 和 `content_length` 的值：

```
> body
'Thanks for calling!\n'
> content_length
>
```

对于你的 `body`，正如预期的那样，你可以看到一个值。但对于预期为 20 的 `content_length`，你什么都没有看到。你现在可以看到设置该值的代码是错误的，并找到了问题！

最后，你可以按 Ctrl+D 调试器以关闭系统，或者输入 `cont` 继续运行服务器。在 REPL 内部输入 `cont` 是不起作用的并会导致以下错误：'ReferenceError: cont is not defined'。你需要按 Ctrl+C 退出 REPL，然后就可以使用 `cont`。

在紧急情况下，在代码中插入一个简单的 `console.log(variable_name);` 将结果打印到终端窗口并没有什么问题。这通常是获取所需信息以追踪错误或问题的快速简单方法。

你可以做以下事情来保持更新且不错过任何重要的变化或新闻：

- 加入 @groups.google.com/group/nodejs 的 Node.js 邮件列表。许多 Node 核心开发者都在列表中，每当有新发布或更改时就会发布。

- 如果你在 Twitter 上，请关注 @nodejs；当有新发布或重要消息时，你会收到推文。

- 定期访问 nodejs.org 以确保。

你学习了如何使用 Node.js 调试器来调试程序。你还学习了如何使用 REPL 检查变量值。最后，你学习了在处理 Node.js 时如何保持更新并寻找帮助。

本节通过查看语言提供的类型开始对 JavaScript 的回顾。在本章的大部分讨论中，我使用 Node.js 的读取-评估-打印循环（REPL）来演示代码如何工作。为了帮助你，我使用**粗体**表示你输入到解释器的内容。

```
client:LearningNode marc$ >
```

Node.js 有几个核心类型：number、boolean、string 和 object。其他类型 function 和 array 实际上是特殊类型的对象，但因为它们在语言和运行时具有额的功能，一些人将这三者——object、function 和 array——统称为复杂类型。`null` 和 `undefined` 类型也是特殊的对象，并且在 JavaScript 中也被特殊对待。

`undefined` 值意味着尚未设置值或简单地不存在：

```
var x;
undefined
x = {};
{}
x.not_valid;
undefined
```

相反，`null` 是一个明确的断言表示“没有值”：

```
var y;
undefined
y
undefined
y = null;
null
>
```

查看 JavaScript 中任何内容的类型，你使用 `typeof` 运算符：

```
type 10
'number'
type "hello";
'string'
type function () { var x = 20; }
'function'
```

虽然 Node.js 理论上支持某些现代 JavaScript 实现的 `const` 关键字扩展，但它尚未被广泛使用。对于常量，标准做法只是使用大写字母和变量声明：

```js
var SECONDS_PER_DAY = 86400;
undefined
console.log(SECONDS_PER_DAY);
86400
undefined
```

## 数字

JavaScript 中的所有数字都是 64 位 IEEE 754 双精度浮点数。对于所有可以在 $2^{53}$ 位内精确表示的正整数和负整数，JavaScript 中的 `number` 类型行为非常像其他语言中的整数数据类型：

- > 1024 + 1024

1048576

- > 1048576

1048576

- > 32437893250 + 3284598359235235

3824630797128485

- > -38425358295 + 35892583295

-25309550000

然而，使用 `number` 类型的棘手之处在于，对于任何数值值，它都是实际数字的近似值。例如：

- > 0.1 + 0.2

0.30000000000000004

在执行浮点数学运算时，你不能仅仅操作任意实数并期望得到一个精确的值：

- > 1 - 0.3 + 0.1 == 0.8

false

对于这些情况，你需要检查该值是否处于某种近似范围内，该范围的大小由你所比较的值的量级决定。（访问 stackoverflow.com 网站搜索关于比较浮点数的文章和问题，以获取此类策略的好主。）

对于那些绝对需要在 JavaScript 中表示 64 位整数值且完全没有近似误差可能的情况，你只能被迫使用 `string` 类型并手动操作这些数字，或者可以使用可用的模块来处理大值。

JavaScript 与其他语言的不同之处在于，将数字除以零会返回 `Infinity` 或 `-Infinity`，而不是产生运行时异常：

- > 5 / 0

Infinity

- > -5 / 0

-Infinity

# 第 2 章 深入了解 JavaScript

`Infinity` 和 `-Infinity` 是你可以在 JavaScript 中比较的有效值：

```
> var x = 10, y = 0;
undefined
> x / y == Infinity
true
```

你可以使用 `parseInt` 和 `parseFloat` 函数将字符串转换为数字：

```
> parseInt("325235232626263");
325235232626263
> parseFloat("82959.248945895");
82959.248945895
> parseInt("234.43634");
234
> parseFloat("10");
10
```

如果你向这些函数提供无法解析的内容，它们将返回特殊值 `NaN`（不是数字）：

```
> parseInt("cat");
NaN
> parseFloat("Wankel-Rotary engine");
NaN
```

要测试是否为 `NaN`，必须使用 `isNaN` 函数：

```
> isNaN(parseInt("cat"));
true
```

最后，要测试给定的数字是否为有效的有限数字（即它不是 `Infinity`、`-Infinity` 或 `NaN`），请使用 `isFinite` 函数：

```
> isFinite(10/5);
true
> isFinite(10/0);
false
> isFinite(parseFloat("banana"));
false
```

## 布尔值

JavaScript 中的 `boolean` 类型既简单又易用。值可以是 `true` 或 `false`，尽管从技术上你通过 `Boolean` 函数将值转换为布尔值，但你几乎不需要它，因为语言会在需要根据以下规则将一切转换为布尔值：

- `false`、`0`、空字符串 (`""`)、`NaN`、`null` 和 `undefined` 均评估为 `false`。

- 所有其他值评估为 `true`。

## 字符串

JavaScript 中的字符串是 Unicode 字符序列（内部以 16 位 UCS-2 格式表示），可以代表世界上大多数字符，包括大多数亚洲语言使用的字符。语言中没有独立的 `char` 或字符数据类型；你只需要使用长度为字符来表示它们。对于你用 Node.js 编写的大大多数网络应用，你将以 UTF-8 与外部世界交互，Node 会为你处理所有的转换细节。除非你在操作二进制数据，否则你对字符串和字符集的体验很大程度上是无忧之的。

字符串可以用单引号或双引号包裹。它们在功能上是等价的，你可以自由使用任何一种。要在单引号字符串内部包含一个单引号，可以使用 `\'`，同样，在双引号字符串内部包含一个双引号，可以使用 `\"`：

```
> 'Marc\'s hat is new.'
> 'Marc\'s hat is new.'
> "\"Hey, nice hat!", she said."
> "Hey, nice hat!", she said.
```

要获取 JavaScript 字符串的长度，使用 `length` 属性：

```
> var x = "cat";
undefined
> x.length;
3
> "cat".length;
3
> x = null;
null
```

在 JavaScript 中尝试获取 `null` 或 `undefined` 字符串的长度会抛错误：

```
> x.length;
TypeError: Cannot read property 'length' of null
at repl:1:2
at REPLServer.self.eval (repl.js:109:21)
at rli.on.self.bufferedCmd (repl.js:109)
```

## 关于 JSON

本书中（实际上在网络和 Web 应用中）经常使用的内容之一是 JSON，即 JavaScript 对象表示法。这种数据交换格式提供了基于文本的数据格式的所有灵活性，而没有像 XML 等格式的烦恼。（对后者公平来说，JSON 也缺乏那些格式的一些验证功能，但我仍然认为它非常强大。）

最后，`trim` 函数移除字符串开头和结尾的空白，正如你所预期的：

```
> " cat ".trim();
'cat'
``` # 正则表达式

JavaScript 具有强大的正则表达式支持，其完整细节超出了本书的范围，但我简要演示如何使用它们。这些表达式可以是字面量格式（由斜杠指示），也可以作为构造函数的调用：

```javascript
/[Aa]{2}/
new RegExp("[Aa]{2}")
```

类似于 `indexOf` 函数，`search` 函数接收一个正则表达式并返回与其匹配的第一个索引，如果没有此类匹配则返回 -1：

```
> "aaao".search(/[Aa]{2});
0
> "aaao".search(/[Aa]{3});
-1
``` # 对象

对象是 JavaScript 语言的核心主力之一，你将经常使用。它们是一种极其动态且灵活的数据类型，你可以对其添加或删除内容。创建一个对象，可以使用以下任意一种，尽管后者（被称为对象字面量语法）几乎总是首选：

```
> var obj1 = new Object();
undefined
> var obj2 = {};
undefined
```

你也可以字面量语法指定对象的内容，在初始化时指定成员名称和值：

```javascript
var user = {
  first_name: "marc",
  last_name: "wandsneider",
  age: Infinity,
  citizenship: "man of the world"
}
``` # 关于 JSON

JSON 与对象表示法法极其相似，有两个关键区别：在对象表示法中，将属性包裹在单引号中是可选的，在 JSON 中是强制性的。此外，所有的字符串都应该像下方一样双引号：

```javascript
// 有效的对象表示法，无效的 JSON:
var obj = {
  // JSON 字符串应该使用 "" 而不是 '
  "first_name": 'Marc'
}
```

 (此处我将根据你提供的文本进行翻译)[/content]

抱歉，由于你提供的文本中存在大量的重复内容和格式混乱，我在处理时意外打乱了逻辑。以下是重新翻译的正确内容：

[content]

// JSON 必须包裹属性名

// JSON 必须包裹属性名

last_name: "Wandsneider"

// 有效的 JSON 和对象字面量表示：

var obj = {

  "first_name": "Marc",

  "last_name": "Wandsneider"

}

```javascript
// JSON 必须包裹属性名
last_name: "Wandsneider"

// 有效的 JSON 和对象字面量表示：
var obj = {
  "first_name": "Marc",
  "last_name": "Wandsneider"
}
```

相当多的 JSON 库实际上会处理单引号字符串，但为了最大的兼容性，每当你编写或生成 JSON 时，都务必小心使用双引号。

要生成 JSON，你主要使用 V8 的函数 `JSON.parse` 和 `JSON.stringify`。前者接收一个 JSON 字符串并将其转换为对象（如果失败则抛出错误），后者接收一个对象并返回它的 JSON 字符串表示形式。

当你在代码中编写对象时，你主要使用对象表示法，但在本书中你也会处理大量的 JSON，因此识别它们之间的区别至关重要。每当绝对需要 JSON 时，我都会指出。

你可以使用以下任何一种方法为你的用户对户对象添加一个新属性：

- > user.hair_colour = "brown";

- > 'brown'

- > user['hair_colour'] = "brown";

- > 'brown'

- > var attribute = 'hair_colour';

- > undefined

- > user[attribute] = "brown";

- > 'brown'

- > user {

  first_name: 'marc',

  last_name: 'wandsneider',

  age: Infinity,

  citizenship: 'man of the world',

  hair_colour: 'brown' 

}

如果你尝试访问一个不存在的属性，你不会收到错误，而是只会得到 `undefined`：

- > user.car_make

undefined

# 第 2 章 深入观察 JavaScript

要从对象中删除属性，你可以使用 `delete` 关键字：

```javascript
> delete user.hair_colour;
true
> user
{ first_name: 'marc',
  last_name: 'wandschneider',
  age: Infinity,
  citizenship: 'man of the world' }
>
```

JavaScript 对象的灵活性使得它们与其他语言中看到的各种关联数组、哈希映射或字典非常相似，但有一个有趣的区别：在 JavaScript 中获取对象-关联数组的大小有点棘手。`Object` 上没有 `length` 属性或方法。为了规避这个问题，你可以编写以下代码（V8 JS）：

```javascript
> Object.keys(user).length;
4
```

注意，这使用了 JavaScript `Object.keys` 的一个非标准扩展；尽管 V8 和大多数浏览器（Internet Explorer 除外）已经支持了它。

## 数组

JavaScript 中的数组类型实际上是对象类型的一种特例，具有许多额外功能，使其变得有用且强大。创建数组，你可以使用传统表示法或数组字面量语法：

```javascript
> var arr1 = new Array();
undefined
> arr1
[]
> var arr2 = [];
undefined
> arr2
[]
>
```

对于对象，我几乎总是倾向于使用字面量语法版本，很少使用前者。

如果你对数组使用 `typeof` 运算符，你会得到一个令人惊讶的结果：

```javascript
> typeof arr2
'object'
>
```

## 类型 35

由于数组实际上是对象，因此 `typeof` 运算符只返回该结果，这通常不是你想要的！幸运的是，V8 有一个语言扩展可以让你确定性地测试某个内容是否为数组：`Array.isArray` 函数（V8 JS）：

```javascript
> Array.isArray(arr2);
true
> Array.isArray({});
false
```

JavaScript 数组类型的一个关键特性是 `length` 属性，其用法如下：

```javascript
> var arr2 = ['cat', 'rat', 'bat' ];
undefined
> arr3.length;
3
``` (注：由于原始文本中存在大量重复，此处已根据核心逻辑进行了合并翻译，并去除了重复的段落)

## 第 2 章 深入理解 JavaScript

在 JavaScript 中，为函数声明参数只需在圆括号中列出它们即可。然而，在运行时完全不会对这些参数进行任何检查：

```javascript
> hello();
hello undefined
undefined
> hello('marc', 'dog', 'cat', 48295);
hello marc
undefined
undefined
```

如果传递给函数调用的参数过少，变量将被赋值为 `undefined`。如果传递的参数过多，多余的部分将被直接忽略。

所有函数体内部都有一个名为 `arguments` 的预定义数组。它包含了传递给特定函数调用的所有值，并允许你对参数进行额外的检查。事实上，你还可以更进一步，利用它让你的函数变得更强大且灵活。

假设你想初始化一个缓存。执行此操作的函数接受一个大小来创建缓存，并对其他项目（如缓存位置、过期算法、最大缓存项大小和存储类型）使用默认值。你可以这样写函数：

```javascript
function init_cache(size_mb, location, algorithm, item_size, storage_type) {

}
```

```javascript
init_cache(100, null, null, null, null);
```

然而，如果函数能足够“智能”，为你提供几种不同的调用方式，那就更酷了：

```javascript
function init_cache() {
  var init_data = {
    cache_size: 10,
    location: '/tmp',
    algorithm: 'lru',
    item_size: 1024,
    storage_type: 'btree'
  };

  var a = arguments;
  for (var i = 0; i < a.length; i++) {
    if (typeof a[i] == 'object') {
      init_data = a[i];
      break;
    } else if (typeof a[i]) == 'number') {
      init_data.cache_size = a[i];
    }
  }
```

## 函数 41

```javascript
    break;
  } else {
    throw new Error("bad cache init param");
  }
  // 等
}
```

现在你有了多种不同的方式来调用这个函数：

```javascript
init_cache();
init_cache(200);
init_cache({ cache_size: 100,
  location: '/exports/tmp',
  algorithm: 'lru',
  item_size: 1024,
  storage_type: 'btree' });
```

JavaScript 中的函数不需要有名称：

```javascript
var x = function (a, b) {
  return a + b;
}
x(10, 20);
30
```

这些无名函数通常被称为**匿名函数**。完全匿名函数有一个缺点，体现在调试中：

```javascript
var x = function () {
  throw new Error("whoopsie");
}
```

```javascript
x();
Error: whoopsie
at x (repl:2:7)
at repl:1:
at REPLServer.self.eval (repl.js:109:21)
at rli.on.self.bufferedCmd (repl.js:258:20)
```

当抛出异常时，匿名函数不会通过语言告知你函数的名称。这会让你的调试工作变得稍微困难。

一个简单的解决方案以及 JavaScript 语言的现代扩展是直接给匿名函数命名：

## 第 2 章 深入理解 JavaScript

```javascript
var x = function bad_apple() {
    throw new Error("whoopsie");
}

x();
Error: whoopsie
    at bad_apple (repl:2:7)
    at repl:1:
    at REPLServer.self.eval (repl.js:109:21)
    at rli.on.self.bufferedCmd (repl.js:258:20)
```

在复杂的程序中，为函数命名是有用的的。你在前面的章节中已经见过匿名函数了。

## 函数作用域

每当函数被调用时，都会创建一个新的作用域。在内部声言的变量在外部不可用，但在外部声明的变量在内部是可以使用的。考虑以下情况：

```javascript
var x = 10;
function function() {
    var y = 20;
    console.log(x + y);
}
function();
console.log(x);
```

输出是：

```
30
10
```

现在考虑如果变量在函数内部定义会怎样：

```javascript
var x = 10;
function function() {
    var x = 20;
    console.log(x + y);
}
function();
console.log(x);
```

输出是：

```
30
10
```

函数内部的变量 `x` 遮蔽了外部的变量 `x`。这是 JavaScript 中常见的模式。

另一种情况是函数嵌套：

```javascript
var x = 10;
function outer() {
    var y = 20;
    function inner() {
        console.log(x + y);
    }
    inner();
}
outer();
```

输出是：

```
30
```

`inner` 函数可以访问 `outer` 函数中的变量。这被称为**闭包**（closure）。

闭包是 JavaScript 的一项强大特性。它允许函数在执行完毕后后仍记住它们被创建的环境。

```javascript
function createCounter() {
    var count = 0;
    return function() {
        count++;
        return count;
    };
}
var counter = createCounter();
console.log(counter());
console.log(counter());
```

`counter` 函数在 `createCounter` 返回后仍保持对 `count` 变量的访问。这用于许多场景，例如创建私有变量。在 JavaScript 中，没有真正的私有变量，但你可以使用闭包实现类似的效果。

```javascript
function makeCounter(name) {
    var count = 0;
    return {
        increment: function() {
            count++;
        },
        getCount: function() {
            return count;
        }
    };
}
var myCounter = makeCounter("test");
myCounter.increment();
console.log(myCounter.getCount());
```

`count` 变量通过 `increment` 和 `getCount` 方法访问。这是 JavaScript 中封装数据的常用方法。

## 深入理解 JavaScript

在 JavaScript 中，函数是一等对象。这意味着你可以像处理其他变量一样处理它们：可以作为参数传递给其他函数，从其他函数返回，并赋值给属性。

```javascript
function add(a, b) {
    return a + b;
}
var myAdd = add;
console.log(myAdd(5, 3));
```

```javascript
function execute(fn, a, b) {
    return fn(a, b);
}
console.log(execute(add, 5, 3));
```

```javascript
function getAdder(x) {
    return function(y) {
        return x + y;
    };
}
var add5 = getAdder(5);
console.log(add5(10));
```

函数也可以拥有属性：

```javascript
function greet() {
    console.log("Hello!");
}
greet.language = "English";
console.log(greet.language);
```

这种灵活性用于许多模式，例如回调函数和高阶函数。回调函数是一个作为参数传递给另一个函数并在稍后调用的函数。

```javascript
function fetchData(callback) {
    console.log("Fetching data...");
    setTimeout(function() {
        var data = 42;
        callback(data);
    }, 1000);
}
fetchData(function(data) {
    console.log("Data received:", data);
});
```

`callback` 函数在数据被“获取”后执行。高阶函数是一个接收另一个函数作为参数或返回一个函数的。

```javascript
function filter(array, predicate) {
    var result = [];
    for (var i = 0; i < array.length; i++) {
        if (predicate(array[i])) {
            result.push(array[i]);
        }
    }
    return result;
}
var numbers = [1, 2, 3, 4, 5];
var evens = filter(numbers, function(n) {
    return n % 2 === 0;
});
console.log(evens);
```

这些特性是现代 JavaScript 开发的基础，并被几乎所有的框架和库使用。

## 原型与继承

默认情况下，JavaScript 中的所有对象都有一个原型对象，这是它们进行继承的机制。多年年来，原型一直是困惑的来源，不同的浏览器使用不同的命名法和细微不同的实现。由于这与本章内容相关，我展示了 V8（以及 Node）模型以及现代 JavaScript 实现似乎的发展方向。

修改早先创建的 `Shape` 类，让所有继承的对象都能获得 X 和 Y 属性以及你声明的方法：

```javascript
function Shape () {
}

Shape.prototype.X = 0;
Shape.prototype.Y = 0;

Shape.prototype.move = function (x, y) {
    this.X = x;
    this.Y = y;
}

Shape.prototype.distance_from_origin = function () {
    return Math.sqrt(this.X*this.X + this.Y*this.Y);
}

Shape.prototype.area = function () {
    throw new Error("I don't have a form yet");
}

var s = new Shape();
s.move(10, 10);
console.log(s.distance_from_origin());
```

```javascript
Square.prototype.area = function () {
  return this.Width * this.Width;
}
```

```javascript
var sq = new Square();
sq.move(-5, -5);
sq.Width = 5;
console.log(sq.area());
console.log(sq.distance_from_origin());
```

这个新类的代码使用了 JavaScript 语言的一种特性，这在 V8 以及其他一些实现中可见：`__proto__` 属性。它允许你告诉 JavaScript 你正在声明的一个新类应该具有指定类型的基原型，你可以从那里进行扩展。

你可以通过一个名为 `Rectangle` 的新类进一步扩展功能，它继承自 `Square` 类：

```javascript
function Rectangle () {
}
```

```javascript
Rectangle.prototype = new Square();
Rectangle.prototype.__proto__ = Square.prototype;
Rectangle.prototype.Height = 0;
```

```javascript
Rectangle.prototype.area = function () {
  return this.Width * this.Height;
}
```

```javascript
var re = new Rectangle();
re.move(25, 25);
re.Width = 10;
re.Height = 5;
console.log(re.area());
console.log(re.distance_from_origin());
```

为了让自己确信一切进展顺利，你可以使用之前见过的运算符 `instanceof`：

```javascript
console.log(sq instanceof Square); // true
console.log(sq instanceof Shape); // true
console.log(sq instanceof Rectangle); // false
console.log(re instanceof Rectangle); // true
console.log(sq instanceof Square); // true
console.log(sq instanceof Shape); // true
console.log(sq instanceof Date); // false
```

# 错误与异常

在 JavaScript 中，你传统上使用 `Error` 对象和消息来信号错误。你抛出（throw）这个错误来信号错误状态：

```javascript
function uoh() {
  throw new Error("Something bad happened!");
}
```

```javascript
uoh();
Error: Something bad happened!
  at uoh(repl:2:7)
  at repl:1:1
  at REPLServer.self.eval(repl.js:109:21)
  at rii.on.self.bufferedCmd(repl.js:258:20)
```

你可以像其他语言中那样使用 `try / catch` 块进行捕获：

```javascript
function uoh() {
  throw new Error("Something bad happened!");
}
try {
  uoh();
} catch (e) {
  console.log("I caught an error: " + e.message);
}
console.log("program is still running");
```

该程序的输出是：

I caught an error: Something bad happened!

program is still running

然而，正如你在下一章看到的，这种错误处理方法会在你在 Node.js 中使用的异步编程模型中产生问题。

# 一些重要的 Node.js 全局变量

Node.js 有几个关锠的全局变量是你始终可用的。

## global

当你在 浏览器中编写 JavaScript 时，有一个 `window` 对象，它充当“全局”变量。你附加到它的任何变量或成员在应用程序的任何地方都可用。

# 第2章 深入观察 JavaScript

Node.js 有类似的东西，叫做 `global` 对象。附加到它的任何内容在你的 node 应用任何地方都可用：

```javascript
function print(var_name) {
  console.log(global[var_name]);
}
```

global.fish = "swordfish";

global.pet = "cat";

```javascript
print("fish"); // prints swordfish
print("pet");   // prints cat
print("fruit"); // prints undefined
```

## console

你已经在 Node 中见过了全局变量 `console`，因为你经常使用 `console.log` 函数。不过，还有其他一些有趣的函数：

- `warn(msg)`——这个函数类似于 `log`，但它将打印在标准错误 (stderr) 上。

- `time(label)` 和 `timeEnd(label)`——第一个标记时间戳，当你调用第二个时，它会打印出自函数被调用以来的时间。

- `assert(cond, message)`——如果 `cond` 求值为 `false`，则抛出 `AssertionFailure` 异常。

## process

Node 中的另一个关键全局是 `process` 全局变量，它包含了许多你在阅读本书时会看到的信息和方法。`exit` 方法用于终止你的 Node.js 进程，`env` 函数返回一个包含当前用户环境变量的对象，而 `cwd` 返回应用当前的工作目录。

# 总结

在这一章中你快速查看了 JavaScript 语言，我希望你对该语言的知识至少提高了一些，一些令人困惑或未知的领域得到了澄清。有了这些基础知识，你现在可以开始研究 Node.js 如何如此有效地使用这种语言来创建强大且快速的应用程序。

# 异步编程

现在你已经对 JavaScript 编程的真实情况有了刷新和更新的认识，是时候进入让 Node.js 成为现在这样的核心概念了：非阻塞 IO 和异步编程。它带来了一些巨大的优势和益处，你很快就会看到，但但也带来了一些复杂性和挑战。

# 旧的办事方式

在过去（大约 2008 年），当你坐下来写一个程序并需要加载文件时，你会编写类似下面的代码（为了演示目的，假设你使用的是类似 PHP 的东西）：

```php
$file = fopen('info.php'); // 假设为 PHP
```

```php
$contents = fread($file);
```

```php
fclose($file);
```

在过去，你必须等待文件读取完成才能继续执行后续代码。但在 Node.js 中，你不需要等待。

# 第3章 异步编程

为了理解 Node.js 如何将前面演示的方法转换为非阻塞异步模型，首先查看 JavaScript 中的 `setTimeout` 函数。该函数接收一个调用的函数和一个在其后调用它的超时：

```javascript
// 代码
setTimeout(function () {
  console.log("I've done my work!");
}, 2000);
```

```javascript
console.log("I'm waiting for all my work to finish.");
```

如果你运行上述代码，你会看到（希望这不会让你感到惊讶）：程序设置了 2000ms（2秒）的超时，并给了它触发时调用的函数，然后继续执行，打印出“I'm waiting...”文本。两秒后，你看到了“I've done...”消息，然后程序退出。

现在，看看任何当你调用需要等待外部资源（数据库服务器、网�请求或文件系统读写操作）的函数，它们都有类似的签名。也就是说，与其调用 `fopen(path, mode)` 并等待，你将改为调用 `fopen(path, mode, callback(file_handle)) { ... }`。

现在使用新的异步函数重写前面的同步脚本。你可以实际上从命令行使用 node 运行此程序。只需确保创建一个可以读取的 `info.txt` 文件即可。

```javascript
var fs = require('fs'); // 这是新的，参见解释

var file;
var buf = new Buffer(100000);
fs.open(
  'info.txt', 'r',
  function (handle) {
    file = handle;
  }
);
```

```javascript
fs.read( // 这将产生错误。
  file, buf, 0, 100000, null,
  function () {
    console.log(buf.toString());
    file.close(file, function () { /* 不在乎 * */ });
  }
);
```

这段代码的第一行是你目前还没有见过的内容：`require` 函数是在 Node.js 程序中引入额外功能的一种方式。Node 自带了一套令人印象深刻的模块，你可以根据需要单独包含其中任何一个。从现在开始，你将经常与更多模块一起；在第 5 章“模块”中，你将学习如何它们以及编写你自己的模块。

如果你直接运行这个程序，它会抛出一个错误并终止。为什么呢？因为 `fs.open` 函数是异步执行的；它在文件打开之前就会立即返回，并向你返回句柄（handle）值。只有当文件被打开并且在 `fs.open` 函数第三个参数指定的调函数中接收到句柄后，`file` 变量才会被赋值。因此，当你紧接着用它调用 `fs.read` 函数时，它仍然是未定义的（undefined）。

修复这个程序很简单：



```javascript
var fs = require('fs');

fs.open(
  'info.txt', 'r',
  function (err, handle) { // 我们稍后会详细介绍 err 参数
    var buf = new Buffer(100000);
    fs.read(
      handle, buf, 0, 100000, null,
      function (err, length) {
        console.log(buf.toString('utf8'), 0, length));
        fs.close(handle, function () { /* 不在乎 * });
      }
    );
  }
);
```

理解这些异步函数工作原理的关键方式可以遵循以下思路：

- 检查并验证参数。
- 告诉 Node.js 核心将对适当函数的调用排入队列中（在前面的示例中，是操作系统或读取函数），并在有结果时通知（调用）所提供的回调函数。
- 返回给调用者。

你可能会问：如果 `open` 函数立即返回了，为什么 Node 进程没有在函数返回后立即退出呢？答案是 Node 基于事件队列运行的；如果存在你正在等待响应的挂起事件，在你的代码执行完毕且该队列上没有剩余事件之前，它不会退出。如果你正在等待响应（无论是 `open` 还是 `read` 函数调用），它就会等待。请参阅图 3.2 了解这种场景在概念上是如何的。

## 错误处理与异步函数

![图 3.2 只要有代码在执行或有人在等待某些东西，Node 就会运行](img/462d9f726aa4852bc590bb4b26fa8f32_68_0.png)

# 错误处理与异步函数

在上章节中，我讨论了错误处理、事件以及 JavaScript 中的 `try...catch` 块。然而，本章增加了非阻塞 IO 和异步函数回调，这产生了一个新问题。考虑以下代码：

```javascript
try {
  setTimeout(function () {
    throw new Error("Uh oh!");
  }, 2000);
} catch (e) {
  console.log("I caught the error: " + e.message);
}
```

## 第 3 章 异步编程

如果你运行这段代码，你完全可能看到输出“I caught the error: Uh oh!”。但你并没有。你实际看到的是：

```
timers.js:103
if (process.listeners('uncaughtException').length) throw e;
Error: Uh oh, something bad
at Object.timeout event res_async.js:5:15
at Timer.list ... (timers.js:101:19)
```

发生了什么？我并没有说 `try...catch` 块应该为你捕获错误——它们确实是如此，但异步调用为这种情况引入了新的“意外”。

实际上，调用确实是在 `try...catch` 块内执行的。如果该函数抛出错误，`catch` 块会捕获它，你将使用你希望看到的消息。然而，`setTimeout` 函数只是向 Node 事件队列添加了一个事件（指示在指定的时间间隔后——在本例中为 2000 ms 调用提供的函数），然后返回。提供的回调函数实际上是在它自己的新上下文和作用范围内运行的。

结果，你可以调用异步函数进行非阻塞 I/O，极少数的函数会抛出错误，而是使用一种单独的方式告知你发生了问题。

在 Node 中，我们使用许多模式来帮助你规范代码编写并避免错误。这些模式并不是由语言或运行时在语法上强制的，但你会经常看到它们被使用，甚至你自己也会使用它们。

## 回调函数与错误处理

你将看到的模式之一是你传递给大多数异步函数的回调函数格式。它至少有一个参数，即上一次操作的成功或失败状态，并且非常常见带有来自上一次操作的一些额外结果或信息（例如文件句柄、数据库连接、查询结果行等）；某些回调函数甚至多于两个：

```javascript
do_something(param1, param2, ..., paramn, function(err, results) { ... });
```

`err` 参数是：

- `null`，表示操作成功，并且（如果应该有结果的话）将有一个结果。
- `Error` 对象类的实例。你偶尔会注意到某些不一致之处，有些人总是向 `Error` 对象添加一个 `code` 字段，然后使用 `message` 字段来存储发生的情况，而其他人则选择了其他模式。对于你在书中编写的所有代码，你将遵循始终包含 `code` 字段并使用 `message` 字段提供尽可能信息的模式。对于你使用的所有模块，你为 `code` 使用字符串值，因为它们更容易读。有些库会在 `Error` 对象中提供带有额外信息的数据，但至少这两个成员应该始终存在。

这种标准的原型方法使你在处理非阻塞函数时，能够始终编写出可预测的代码。在本书中，我演示了在回调中处理错误的两种常见编码风格。这是第一种：

```javascript
fs.open(
  'info.txt', 'r',
  function (err, handle) {
    if (err) {
      console.log("ERROR: " + err.code + " (" + err.message + ")");
      return;
    }
    // 成功！！在此处继续工作
  }
);
```

在这种风格中，你检查错误，如果发现错误则返回；否则，你继续处理结果。现在是另一种方法：

```javascript
fs.open(
  'info.txt', 'r',
  function (err, handle) {
    if (err) {
      console.log("ERROR: " + err.code + " (" + err.message + ")");
    } else {
      // 成功！！在此处继续工作
    }
  }
);
```

在这种方法中，你使用 `if...else` 语句来处理错误。

这两种方法之间的区别似乎是在钻牛角尖，但对于那些忘记在 `if` 语句内部使用 `return` 语句的情况，前者更容易产生 bug 和错误，而后者会导致代码缩进变深，你最终得到的代码行非常长且可读性差。你可以在第 5 章的“应该内置的模块”章节查看这第二个问题的解决方案。

带有错误处理的完整文件加载代码见列表 3.1。

## 列表 3.1 带有错误处理的文件加载

```javascript
var fs = require('fs');

fs.open(
  'info.txt', 'r',
  function (err, handle) {
    if (err) {
      console.log("ERROR: " + err.code
        + " (" + err.message + ")");
      return;
    }

    var buf = new Buffer(100000);

    fs.read(
      handle, 0, 100000, null,
      function (err, length) {
        if (err) {
          console.log("ERROR: " + err.code +
            + (" + err.message + ")");
          return;
        }

        console.log(buf.toString('utf8', 0, length));

        fs.close(handle, function () { /* 不在乎 * */ });
      }
    );
  }
);
```

## 我是谁？维护身份认同

现在你准备好编写一个小类来帮助你完成常见的文件操作了。

```javascript
var fs = require('fs');

function FileObject () {
  this.filename = '';

  this.file_exists = function (callback) {
    console.log("正在打开: " + this.filename);
    fs.open(this.filename, 'r', function (err, handle) {
      if (err) {
        console.log("无法打开: " + this.filename);
        callback(err);
        return;
      }

      fs.close(handle, function () { });

      callback(null, true);
    });
  };
}
```

你目前已经添加了一个属性 `filename` 和一个方法 `file_exists`。该方法执行了以下操作：

- 它尝试以只读模式打开 `filename` 中指定的的文件。
- 如果文件不存在，它会打印一条消息，并带有错误信息调用回调函数。
- 如果文件确实存在，它将调用回调函数并指示成功。

现在，使用以下代码运行该类：

```javascript
var fo = new FileObject();
fo.filename = "file_that_does_not_exist";

fo.file_exists(function(err, results) {
  if (err) {
    console.log("Aw, bummer: " + JSON.stringify(err));
    return;
  }
  console.log("file exists!!!");
});
```

你可能会期望以下输出：

```
准备打开：file_that_does_not_exist
无法打开：file_that_does_not_exist
```

但实际上，你看到的是：

```
准备打开：file_that_does_not_exist
无法打开：undefined
```

发生了什么？大多数情况下，当你将一个函数嵌套在另一个函数内部时，它会继承父函数/宿主函数的作用域，并且应该访问所有相同的变量。那么为什么嵌套回调函数没有获取 `filename` 属性的正确值呢？

问题在于 `this` 关键字和异步回调函数。不要忘记，当你调用像 `fs.open` 这样的函数时，它会初始化自己、底层的操作系统函数（在本例中打开文件），并将提供的回调函数放置在事件队列中。执行立即返回到 `FileObject#file_exists` 函数，然后你退出。

## 第 3 章 异步编程

当 `fs.open` 函数完成工作并且 Node 运行回调时，你不再拥有 `FileObject` 类的上下文，而且回调函数被赋予了一个新的指针！

坏消息是，你确实丢失了指向 `FileObject` 类的指针。好消息是，`fs.open` 的回调函数确实有自己的函数作用域。解决此问题的常用方法是将消失的指针“保存”到一个名为 `self` 或类似的变量中。现在重写 `file_exists` 函数以利用这一特性：

```javascript
this.file_exists = function (callback) {
  var self = this;
  console.log("About open: " + self.filename);
  fs.open(this.filename, 'r', function (err, handle) {
    if (err) {
      console.log("Can open: " + self.filename);
      callback(err);
      return;
    }
    fs.close(handle, function () {
      callback(null, true);
    });
  });
};
```

由于函数作用域通过闭包被保留，即使 Node.js 稍后异步执行你的回调函数，新的 `self` 变量也会为你维护。你将在所有的应用程序中大量地使用这一点。有些人喜欢用 `me` 代替 `self`，因为更短；而另一些人仍继续使用完全不同的词。选择一个你喜欢的并坚持使用以保持一致性。

## 保持礼貌——学会放弃控制权

Node 运行在单线程中，通过一个单事件循环来调用外部函数和服务。它将回调函数放在事件队列中等待响应，并尝试尽可能快地执行代码。那么，如果你有一个函数尝试计算两个数组的交集，会发生什么：

```javascript
function compute_intersection(arr1, arr2, callback) {
  var results = [];
  for (var i = 0; i < arr1.length; i++) {
    for (var j = 0; j < arr2.length; j++) {
      if (arr2[j] == arr1[i]) {
        results.push(arr1[j]);
        break;
      }
    }
  }
}
```

对于包含几千个元素的数组，这个函数开始消耗大量时间来完成工作。在 Node.js 只能一次执行一个操作的单线程模型中，这段时间可能会成为问题。计算哈希值、摘要或其他执行其他昂贵操作的类似函数，将导致你的应用程序在执行工作时临时“冻结”。你能做什么呢？

在本书的引言中，我提到某些事情 Node.js 并不擅长，其中之一显然更适合处理更常见的应用程序任务，如密集的 I/O 和请求。如果你想写一个执行大量昂贵计算的服务器，你可能需要考虑将这些操作移动到远程服务。如果你正在进行某些计算密集型任务，你仍然可以将它们包含在 Node.js 中，并利用名为 `nextTick` 的进程对象。这种方法基本上是：“放弃执行控制权，当你有空闲时，调用提供的函数。”它往往比 `setTimeout` 快得多。

### 3.2 使用 nextTick 保持礼貌

```javascript
function compute_intersection(arr1, arr2, callback) {
  // 两个数组的交集
  var bigger = arr1.length > arr2.length ? arr1 : arr2;
  var smaller = bigger === arr1 ? arr2 : arr1;
  var biggerlen = bigger.length;
  var smlen = smaller.length;
  var sidx = 0; // 索引
  var size = 10; // 大小，可以调整
  var results = []; // 中间结果

  // 对于 bigger 中的每一个块
  function sub_compute_intersection() {
    for (var i = sidx; i < sidx + size && i < biggerlen; i++) {
      for (var j = 0; j < smlen; j++) {
        if (bigger[i] == smaller[j]) {
          results.push(smaller[j]); // 推入结果
        }
      }
    }

    if (i >= biggerlen) {
      callback(null, results); // 无错误，返回结果
    } else {
      sidx += size;
      process.nextTick(sub_compute_intersection);
    }
  }

  sub_compute_intersection();
}
```

### 3.3 测试 compute_intersection 函数

```javascript
var a1 = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
var a2 = [5, 6, 7, 8, 9, 10, 11, 12, 13, 14];

compute_intersection(a1, a2, function (err, results) {
  if (err) {
    console.log(err);
  } else {
    console.log(results);
  }
});
```

尽管这让计算交集的函数比原始版本变得复杂了一些，但新版本在 Node 的单线程事件处理世界中运行得更好，而且在任何担心需要复杂或缓慢计算的情况下，你都可以使用 `nextTick`。

## 同步函数调用

现在我花了几乎整一个章节告诉你们 Node.js 是多么异步的，以及编程非阻塞 IO 的所有技巧和陷阱，我必须提到 Node 实际上为某些关键 API 提供了同步版本。你将在第 11 章“命令行编程”中使用它们。

为了在这里简要演示，你可以将本章的脚本重写如下：

```javascript
var fs = require('fs');

var handle = fs.openSync('info.txt', 'r');
var buf = Buffer.alloc(100000);
var read = fs.readSync(handle, buf, 0, 10000, null);
console.log(buf.toString('utf8', 0, read));
fs.closeSync(handle);
```

# 总结

从执行一系列同步或阻塞 IO 函数调用并等待每个调用完成后再继续下一个的模式，切换到一切都异步执行并等待 Node 告诉你给定任务完成的模式，这需要一些思维上的体操和实验。但我相信，一旦你掌握了这一点，你将永远无法想象回到原来的编写应用程序的方式了。

接下来，你将编写你的第一个简单的 JSON 应用程序服务器。

## 第二部分：学习运行

- [4 编写简单的应用程序](#第-4-章-编写简单的应用程序)
- [5 模块](#5-模块)
- [6 扩展你的 Web 服务器](#6-扩展你的-web-服务器)

# 第 4 章 编写简单的应用程序

现在你已经对 JavaScript 语言的真实原理有了更好的理解，是时候开始释放 Node.js 的威力来编写 Web 应用了。正如我在引言中提到的，整本书你将编写一个小型相册网站。在本章中，你将开始编写一个 JSON 服务器来提供每个专辑的列表和图片，并在结束时，你将添加重命名专辑的功能。在此过程中，你将深入了解运行 JSON 服务器的基础知识，以及它如何与 HTTP 的许多基本部分（如 GET 和 POST 参数、标头、请求和响应）进行交互。第一代相册应用程序使用 API 来完成所有工作；这是学习 API 的极佳方法，并让你专注于想要学习的新概念。

## 你的第一个 JSON 服务器

在第 1 章“入门”结束时，你写了一个简单的 HTTP 服务器，对于任何传入的请求，它都会返回纯文本“Thanks for calling!\n”。现在你可以修改这一小部分，让它执行不同的操作：

1. 指明返回的数据是 `application/json` 而不是 `text/plain`。
2. 在 `console.log` 中打印传入的请求。
3. 返回一个 JSON 字符串。

这里是简单的服务器代码，保存为 `simple_server.js`：

```javascript
var http = require('http');

function handle_incoming_request(req, res) {
  console.log("INCOMING REQUEST: " + req.method + " " + req.url);
  res.writeHead(200, { "Content-Type" : "application/json" });
  res.end(JSON.stringify({ error: null }) + "\n");
}

var s = http.createServer(handle_incoming_request);
s.listen(8080);
```

在一个终端窗口（Mac/Linux）或命令提示符（Windows）中输入并运行此程序：

```bash
node simple_server.js
```

它应该静静在那里什么都不做，等待请求。现在，在另一个终端窗口中，输入：

```bash
curl -X GET http://localhost:8080
```

如果你执行得一切正确，在运行服务器的窗口中，你应该能看到：

```text
INCOMING REQUEST: GET /
```

在你运行 `curl` 命令的窗口中，你应该能看到：

```json
{"error":null}
```

尝试运行 `curl` 命令的不同变体，并观察会发生什么。例如：

```bash
curl -X GET http://localhost:8080/gobbledydygook
```

从这第一个新程序开始，你可以标准化 JSON 响应的输出，使其输出中始终包含一个 `error` 字段。这样，应用程序就可以快速判断请求的成功或失败。在发生失败的情况下，你始终包含一个带有更多信息的 `message` 字段；而在 JSON 响应应该返回某些数据的情况下，你始终包含一个 `data` 字段：

```json
// 失败响应如下：
{
  "error": "missing_data",
  "message": "You must include a last name for the user"
}
```

```json
// 成功响应通常会有一个 "data" 对象
{
  "error": null,
  "user": {
    "first_name": "Horatio",
    "last_name": "Gadsplattt III",
    "email": "horatio@example.org"
  }
}
```

有些应用程序偏于使用数字代码作为其错误系统。使用这些代码完全取决于你，但我更倾向于使用文本代码，因为它们感觉更具描述性，并且在我使用像 `curl` 这样的命令行程序测试程序时，可以去查找的步骤。我认为 `no_such_user` 比 `~325` 信息量大得多。

## 返回数据

当你开始时，你的相册应用程序非常简单：它是专辑的集合，每个专辑包含一个照片集合，如图 4.1 所示。

| ITALY2012 | JAPAN2010 | AUSTRALIA2010 |
| :--- | :--- | :--- |
| Our Trip to Italy | A Week in Tokyo | Melbourne Fun! |
| Italy_01.jpg | Photo001.jpg | Oz01.jpg |
| Italy_02.jpg | Photo002.jpg | Oz02.jpg |
| Italy_03.jpg | Photo003.jpg | Oz03.jpg |
| Italy_04.jpg | Photo004.jpg | Oz04.jpg |
| Italy_05.jpg | Photo005.jpg | Oz05.jpg |
| Italy_06.jpg | | Oz06.jpg |

图 4.1 专辑和照片

现在，专辑是运行你脚本的位置的子目录：

- `scripts/`
- `scripts/albums/`
- `scripts/albums/italy2012`
- `scripts/albums/australia2010`
- `scripts/albums/japan2010`

因此，要获取专辑列表，你只需要查找 `albums/` 内部的项目。通过 `fs.readdir` 函数返回可能 `.` 和 `..` 之外的所有项目。`load_album_list` 函数如下：

```javascript
function load_album_list(callback) {
  fs.readdir(
    "albums/",
    function (err, files) {
      if (err) {
        callback(err);
      }
      callback(null, files);
    }
  );
}
```

让我们仔细看一下这个函数。首先，它提供了一个在目录中的所有项目加载后应该调用的函数。此回调函数与大多数回调具有相同的原型：`error` 参数和 `results` 参数；你可以自由调用它们。注意，`load_album_list` 函数的唯一参数是一个回调函数。由于 `load_album_list` 函数本身是异步的，它在工作完成后需要知道将专辑列表传递哪里。它无法向调用者返回值，因为它会在 `fs.readdir` 函数回调之前执行。再次，这是 Node 编程的核心技术：告诉 Node 执行某些事，并在完成后发送结果。与此同时，你继续其他处理。你需要执行的许多任务基本上变成了长系列的回调。列表 4.1 提供了列表服务器的完整代码。

## 列表 4.1 列表服务器 (load_albums.js)

```javascript
var http = require('http');
var fs = require('fs');

function load_album_list(callback) {
  fs.readdir("albums/", function (err, files) {
    if (err) {
      callback(err);
      return;
    }
    callback(null, files);
  });
}

function handle_incoming_request(req, res) {
  console.log("INCOMING REQUEST: " + req.method + " " + req.url);
  load_album_list(function (err, albums) {
    if (err) {
      res.writeHead(503, {"Content-Type": "application/json"});
      res.end(JSON.stringify(err) + "\n");
      return;
    }
    var out = { error: null, data: albums };
    res.writeHead(200, {"Content-Type": "application/json"});
    res.end(JSON.stringify(out) + "\n");
  });
}

var s = http.createServer(handle_incoming_request);
s.listen(8080);
```

在列表 4.1 中，`fs.readdir` 完成后，你检查结果。如果发生错误，你将其返回给调用者（你在 `handle_incoming_request` 函数中传递给 `load_album_list` 的函数）；否则，将文件夹列表（albums）返回给调用者，`null` 表示没有错误。

此列表为 `handle_incoming_request` 函数增加了新的错误处理代码：如果 `fs.readdir` 告诉你发生了某些坏事，你希望调用者意识到这一点，所以你仍然返回 JSON 和 HTTP 响应码 503，表示发生了意外情况。JSON 服务器应该向其客户端返回尽可能的信息，以判断问题是他们操作的还是服务器内部的。

要测试程序，请确保运行此脚本的文件夹中有一个 `albums/` 子文件夹，其中包含一些专辑文件夹。运行服务器，再次运行 `node load_albums.js`。

要获取结果，你使用：

```bash
curl -X GET http://localhost:8080/
```

`curl` 命令的结果应该像这样：

```json
{"error":null,"data":["australia2010","italy2012","japan2010"]}
```

## Node 模式：异步循环

如果你在 `albums/` 文件夹中创建一个文本文件 `info.txt` 并重新运行列表服务器会发生什么？你可能会看到这样的结果：

```json
{"error":null,"data":["australia2010","info.txt","italy2012","japan2010"]}
```

你真正想要的是程序检查 `fs.readdir` 的结果，并只返回文件夹条目，而不是普通文件。为了实现这一点，你可以使用 `fs.stat` 函数，它会传递一个你可以用于进行此测试的对象。

因此，重写 `load_album_list` 函数，以遍历 `fs.readdir` 的结果并测试它们是否为文件夹：

```javascript
function load_album_list(callback) {
  fs.readdir(
    "albums",
    function (err, files) {
      if (err) {
        callback(err);
        return;
      }
      var only_dirs = [];
      for (var i = 0; i < files.length; i++) {
        fs.stat(
          "albums/" + files[i],
          function(err, stats) {
            if (stats.isDirectory()) {
              only_dirs.push(files[i]);
            }
          }
        );
      }
      callback(null, only_dirs);
    }
  );
}
```

保持程序的其他部分不变，然后运行 `curl` 命令。它应该始终返回：

```json
{"error":null,"data":{"albums":[]}}
```

你弄坏了服务器！发生了什么？

问题出在你添加的新循环上。大多数循环和异步回调是不兼容的。实际上，你在前面的代码中所做的是：

- 创建一个 `only_dirs` 数组来存储响应。
- 对于 `files` 数组中的每一项，调用非阻塞函数 `fs.stat` 并向其传递提供的函数以测试文件是否为目录。
- 在所有这些非阻塞函数启动后，退出 `for` 循环并调用 `callback` 参数。由于 Node.js 是单线程的，没有任何 `fs.stat` 函数得到机会执行并调用回调，因此 `only_dirs` 仍然是空的，而你将它传递给了提供的 `callback`。事实上，当 `fs.stat` 的回调最终被调用时，已经没有人在意它了。

要解决这个问题，你必须使用递归。你实际上创建了一个具有以下格式的新函数，然后立即调用它：

```javascript
(function iterator(i) {
  if (i < array.length) {
    async_work(function(){
      iterator(i + 1);
    });
  } else {
    callback(results);
  }
})(0);
```

你实际上可以做得更好，使用一个具名的匿名函数，这样你就不会用函数名弄乱作用域（上述即为 IIFE 模式）。

因此，为了重写测试 `fs.readdir` 结果是否为文件夹的循环，你可以如下编写函数：

```javascript
function load_album_list(callback) {
  fs.readdir(
    "albums",
    function (err, files) {
      if (err) {
        callback(err);
        return;
      }
      var only_dirs = [];
      (function iterator(index) {
        if (index == files.length) {
          callback(null, only_dirs);
          return;
        }
        fs.stat(
          "albums/" + files[index],
          function (err, stats) {
            if (err) {
              callback(err);
              return;
            }
            if (stats.isDirectory()) {
              only_dirs.push(files[index]);
            }
            iterator(index + 1);
          }
        );
      })(0);
    }
  );
}
```

保存这个新版本的简单 JSON 服务器，你现在应该能看到只包含专辑文件夹而不包含文件的结果了。

## 学习处理多任务：处理更多请求

该相册 JSON 服务器目前仅响应一种请求：请求专辑列表的请求。事实上，它甚至不在乎你如何调用此请求；它始终返回相同的内容。

你可以稍微扩展服务器的功能，允许你请求以下两种内容中的任一种：

1. 可用的专辑列表——你可以调用它 `/albums.json`。
2. 某个专辑中的项目列表——你可以调用它 `/albums/album_name.json`。

在请求中添加 `.json` 后缀强调了你正在编写的是仅与该格式工作的 JSON 服务器。

支持这两种请求的新版本 `handle_incoming_request` 函数可能如下：

```javascript
function handle_incoming_request(req, res) {
  console.log("INCOMING REQUEST: " + req.method + " " + req.url);
  if (req.url == '/albums.json') {
    handle_list_albums(req, res);
  } else if (req.url.substr(0, 7) == '/albums'
    && req.url.substr(req.url.length - 5) == '.json') {
    handle_get_album(req, res);
  } else {
    send_failure(res, 404, invalid_resource());
  }
}
```

上述代码中的两个语句查看了传入请求对象上的 `url` 属性。如果请求仅仅是 `/albums.json`，你可以提前处理该请求。如果是 `/albums/something.json`，你可以假设它是对专辑列表的请求。

```javascript
function handle_get_album(req, res) {
  // 请求的格式为 /albums/album_name.json
  var core_url = req.url;
  var album_name = core_url.substr(7, core_url.length - 12);
  load_album(
    album_name,
    function (err, album_contents) {
      if (err && err.error == "no_such_album") {
        send_failure(res, 404, err);
      } else if (err) {
        send_failure(res, 500, err);
      } else {
        send_success(res, { album_data: album_contents });
      }
    }
  );
}
```

```javascript
function make_error(err, msg) {
  var e = new Error(msg);
  e.code = err;
  return e;
}
```

```javascript
function send_success(res, data) {
  res.writeHead(200, { "Content-Type": "application/json" });
  var output = { error: null, data: data };
  res.end(JSON.stringify(output) + "\n");
}
```

```javascript
function send_failure(res, code, err) {
  res.writeHead(code, { "Content-Type": "application/json" });
  res.end(JSON.stringify({ error: err.code, message: err.message }) + "\n");
}
```

```javascript
function invalid_resource() {
  return make_error("invalid_resource",
    "the requested resource does not exist.");
}
```

```javascript
function no_such_album() {
  return make_error("no_such_album",
    "The specified album does not exist.");
}
```

```javascript
var s = http.createServer(handle_incoming_request);
s.listen(8080);
```

为了避免代码大量重复，我还提取了许多用于发送最终成功或失败响应给请求客户端的处理逻辑。这些代码位于 `send_success` 和 `send_failure` 函数中，这两个函数都用于设置正确的 HTTP 响应状态码并根据情况返回正确的 JSON。

你可以看到，新函数 `load_album` 与 `load_album_list` 函数非常相似。它列出专辑文件夹中的所有项目，然后遍历其中的每一个项目以确保它们是普通文件，并返回最终列表。我还为 `load_album` 中 `fs.readdir` 的错误处理添加了数行额外代码：

```javascript
if (err.code == "ENOENT") {  // 更多信息见正文
    callback(no_such_album());
} else {
    callback({ error: "file_error",
        message: JSON.stringify(err) });
}
```

基本上，如果 `fs.readdir` 因为找不到专辑文件夹而失败，那就是用户错误；用户指定了一个无效的专辑。因此，你希望返回一个指示该错误的错误，你可以通过使用辅助函数 `no_such_album` 来实现。然而大多数其他失败可能是服务器配置问题，因此你希望对这些情况返回更通用的 "file_error"。

现在获取 `/albums.json` 的输出看起来如下：

```json
{"error":null,"data":{"albums":[{"name":"australia2010"},{"name":"italy2012"},{"name":"japan2010"}]}}
```

在每个专辑文件夹中放入几张图片后，获取专辑内容（例如 `/albums/italy2012.json`）的输出现在如下（此处已过清理）：

```json
{
  "error": null,
  "data": {
    "album_data": {
      "short_name": "/italy2012",
      "photos": [
        { "filename": "picture_01.jpg", "desc": "picture_01.jpg" },
        { "filename": "picture_02.jpg", "desc": "picture_02.jpg" },
        { "filename": "picture_03.jpg", "desc": "picture_03.jpg" },
        { "filename": "picture_04.jpg", "desc": "picture_04.jpg" },
        { "filename": "picture_05.jpg", "desc": "picture_05.jpg" }
      ]
    }
  }
}
```

## 关于请求和响应对象的更多内容

现在输入并运行以下程序：

```javascript
var http = require('http');

function handle_incoming_request(req, res) {
  console.log("----------------");
  console.log(req);
  console.log("----------------");
  console.log(res);
  console.log("----------------");
  res.writeHead(200, { "Content-Type": "application/json" });
  res.end(JSON.stringify({ error: null }) + "\n");
}

var s = http.createServer(handle_incoming_request);
s.listen(8080);
```

然后在另一个终端窗口中，对该服务器的某些内容运行 `curl` 命令：

```bash
curl -X GET http://localhost:8080
```

你的客户端窗口应该打印 `error: null`，但服务器窗口会打印出大量的文本，包含了传递给你的 HTTP 服务器的请求和响应对象信息。

你已经使用了请求对象上的两个属性：`method` 和 `url`。前者可以让你传入的请求是 GET 还是 POST。而请求对象包含了 Node.js 提供的 URL，你可以通过它来了解更多信息。

你可以通过查看 `headers` 来查看请求头。例如：

```json
{
  'user-agent': 'curl/7.24.0',
  'host': 'localhost:8080',
  'accept': '*'
}
```

在响应端，你必须使用 `writeHead` 和 `end`。

你很幸运可以一次性完成这些操作。如果你使用 Node 带的 `url` 模块，对前面的 URL 打印出 `url.parse` 的结果，你会看到：

```json
{
  'search': '?page=1&size=20',
  'query': { page: '1', size: '20' },
  'pathname': '/albums/italy2012.json',
  'path': '/albums/italy2012.json?page=1&size=20',
  'href': '/albums/italy2012.json?page=1&size=20'
}
```

现在你可以修改 `handle_incoming_request` 函数来解析 URL 并将其存回请求对象的 `parsed_url` 中。该函数现在看起来是：

```javascript
function handle_incoming_request(req, res) {
  req.parsed_url = url.parse(req.url, true);
  var core_url = req.parsed_url.pathname;

  // 测试这个修复后的 url 看看他们在请求什么
  if (core_url == '/albums.json') {
    handle_list_albums(req, res);
  }
  // ... 后续逻辑
}
```

## HTTP 状态码

你可以通过查看 [HTTP 状态码列表](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes) 来了解更多关于它们的信息：

- `200 OK`
- `301 Moved Permanently`
- `400 Bad Request`
- `401 Unauthorized`
- `403 Forbidden`
- `404 Not Found`
- `500 Internal Server Error`
- `503 Service Unavailable`

## 增加灵活性：GET 参数

当你开始在专辑中添加很多照片时，客户端应该说它们想要多少以及什么，例如：

```bash
curl -X GET 'http://localhost:8080/albums/italy2012.json?page=1&size=20'
```

如果你不熟悉这些术语，URL 的粗体部分是查询字符串，通常被称为 GET 参数。之前的版本的代码是在寻找字符串结尾的 `.json`，而不是中间。为了修复代码以支持分页，你需要做三件事：

1. 修改 `handle_incoming_request` 函数以正确解析 URL。
2. 解析查询字符串并获取 `page` 和 `page_size` 的值。
3. 修改 `load_album` 函数以支持这些参数。

```javascript
function handle_incoming_request(req, res) {
  req.parsed_url = url.parse(req.url, true);
  var core_url = req.parsed_url.pathname;

  // 测试这个修复后的 url 看看他们在请求什么
  if (core_url == '/albums.json') {
    handle_list_albums(req, res);
  } else if (core_url.substr(0, 7) == '/albums'
    && core_url.substr(core_url.length - 5) == '.json') {
    handle_get_album(req, res);
  } else {
    send_failure(res, 404, invalid_resource());
  }
}
```

对于最后部分，你修改 `handle_get_album` 函数来查找 `page` 和 `page_size` 参数。当传入的值未提供或无效值时，你可以为它们设置一些合理的默认值。（服务器始终假设传入的值是有危险的或无意义的，并对其进行仔细检查。）

```javascript
function handle_get_album(req, res) {
    // 获取 GET 参数
    var getp = req.parsed_url.query;
    var page_num = getp.page ? getp.page : 0;
    var page_size = getp.page_size ? getp.page_size : 1000;

    if (isNaN(parseInt(page_num))) page_num = 0;
    if (isNaN(parseInt(page_size))) page_size = 1000;

    // 请求的格式为 /albums/album_name.json
    var core_url = req.parsed_url.pathname;
    var album_name = core_url.substr(7, core_url.length - 12);

    load_album(
        album_name,
        page_num,
        page_size,
        function (err, album_contents) {
            if (err && err.error == "no_such_album") {
                send_failure(res, 404, err);
            } else if (err) {
                send_failure(res, 500, err);
            } else {
                send_success(res, { album_photos: album_contents });
            }
        }
    );
}
```

最后，你修改 `load_album` 函数，在完成所有工作后提取 `files_only` 数组的子数组：

```javascript
function load_album(album_name, page, page_size, callback) {
  fs.readdir(
    "albums/" + album_name,
    function (err, files) {
      if (err) {
        if (err.code == "ENOENT") {
          callback(no_such_album());
        } else {
          callback({error: "file_error",
          message: JSON.stringify(err)});
        }
        return;
      }

      var only_files = [];
      var path = "albums/" + album_name + "/";

      (function iterator(index) {
        if (index == files.length) {
          var ps;
          // 如果参数超出范围，slice 会优雅地切片
          ps = only_files.slice(page * page_size, (page + 1) * page_size);
          var obj = { short_name: album_name, photos: ps };
          callback(null, obj);
          return;
        }

        fs.stat(
          path + files[index],
          function (err, stats) {
            if (err) {
              callback({error: "file_error",
              message: JSON.stringify(err)});
              return;
            }
            if (stats.isFile()) {
              var obj = { filename: files[index], desc: files[index] };
              only_files.push(obj);
            }
            iterator(index + 1);
          }
        );
      })(0);
    }
  );
}
```

## 修改内容：POST 数据

现在我已经很大程度上涵盖了如何将数据放入你的 JSON 服务器，你可能想开始尝试向它发送数据，以创建新内容或修改现有内容。这通常通过 HTTP POST 数据完成，你可以以许多不同的格式发送数据。要使用 curl 方法发送数据，你必须执行以下几点：

1. 将 HTTP 方法参数设置为 POST（或 PUT）。
2. 设置传入数据的 Content-Type。
3. 发送数据本身。

你可以使用 curl 轻松地完成这些任务。第一点只需更改方法名，第二点通过使用 curl 的 `-H` 标志使用 HTTP 头部，最后一点可以通过几种不同的方式实现，在这里你可以使用 `-d` 标志并将 JSON 直接写为字符串。

现在是时候为服务器添加一些新功能以允许你重命名专辑了。将 URL 格式设置如下并指定其为 POST 请求：

```text
http://localhost:8080/albums/albumname/rename.json
```

因此，重命名专辑的命令现在是：

```bash
curl -X POST -H "Content-Type: application/json" \
-d '{"album_name": "new album name"}' \
http://localhost:8080/albums/old_album_name/rename.json
```

修改 `handle_incoming_request` 来接受新的请求类型非常简单：

```javascript
function handle_incoming_request(req, res) {
  // 将查询参数解析为对象并获取路径
  // 如果没有这些参数。（第二个参数 true = 解析参数）
  req.parsed_url = url.parse(req.url, true);
  var core_url = req.parsed_url.pathname;

  // 测试此固定的 url 以查看他们请求什么
  if (core_url == '/albums.json' && req.method.toLowerCase() == 'get') {
    list_albums(req, res);
  } else if (core_url.substr(core_url.length - 12) == '/rename.json'
    && req.method.toLowerCase() == 'post') {
    handle_rename_album(req, res);
  } else if (core_url.substr(0, 7) == '/albums'
    && core_url.substr(core_url.length - 5) == '.json'
    && req.method.toLowerCase() == 'get') {
    handle_get_album(req, res);
  } else {
    send_failure(res, 404, invalid_resource());
  }
}
```

注意，你必须在 `load_album` 请求之前处理重命名请求，否则代码将将其视为 `handle_get_album`。

## 接收 JSON 数据

在程序中获取 POST 数据需要使用流。流是在保持系统非阻塞特性的同时传输大量数据的强大方法。我将在第 6 章“扩展你的服务器”中详细介绍流，但现在你只需要知道流的模式：

特别地，注意两个事件：`readable` 和 `end`。流实际上是继承自 `http` 模块（来自 `Stream` 类）；通过以下模式监听这两个事件：

```javascript
var json_body = '';
req.on(
  'readable',
  function () {
    var d = req.read();
    if (d) {
      if (typeof d == 'string') {
        json_body += d;
      } else if (typeof d == 'object' && d instanceof Buffer) {
        json_body += d.toString('utf8');
      }
    }
  }
);
req.on(
  'end',
  function () {
    // 我们获取正体了吗？
    if (json_body) {
      try {
        var body = JSON.parse(json_body);
        // 使用它并调用回调！
        // callback(null, body); // 此处为示例逻辑
      } catch (e) {
        // callback({ error: "invalid_json", message: "The body is not valid" });
      }
    } else {
      // callback({ error: "no_body", message: "We did not receive any JSON" });
    }
  }
);
```

对于形成请求主体的每个数据块，传递给 `on('readable')` 的函数都是处理器。在前面的代码中，你首先通过 `read` 方法从流中读取数据并附加 `json_body` 变量；当获取 `end` 事件时，获取字符串并尝试解析。如果字符串不是有效的 JSON，`JSON.parse` 会抛出错误，因此你需要将其封装在 `try/catch` 块中。

处理重命名请求的函数如下：

```javascript
function handle_rename_album(req, res) {
    // 1. 从 URL 获取专辑名称
    var core_url = req.parsed_url.pathname;
    var parts = core_url.split('/');
    if (parts.length != 4) {
        send_failure(res, 404, invalid_resource(core_url));
        return;
    }
    var album_name = parts[2];

    // 2. 获取请求的 POST 数据。这将包含专辑新名称的 JSON。
    var json_body = '';
    req.on(
        'readable',
        function () {
            var d = req.read();
            if (d) {
                if (typeof d == 'string') {
                    json_body += d;
                } else if (typeof d == 'object' && d instanceof Buffer) {
                    json_body += d.toString('utf8');
                }
            }
        }
    );

    // 3. 当我们拥有所有 post 数据时，确保验证数据并尝试重命名。
    req.on(
      'end',
      function () {
        // 我们获取正体了吗？
        if (json_body) {
          try {
            var album_data = JSON.parse(json_body);
            if (!album_data.album_name) {
              send_failure(res, 403, missing_data('album_name'));
              return;
            }
          } catch (err) {
            // 获取了正体，但不是有效的 json
            send_failure(res, 403, bad_json());
            return;
          }
        } else { // 没有获取正体
          send_failure(res, 403, bad_json());
          return;
        }

        // 4. 执行重命名！
        do_rename(
          album_name, // 旧
          album_data.album_name, // 新
          function (err, results) {
            if (err && err.code == "ENOENT") {
              send_failure(res, 403, no_such_album());
              return;
            } else if (err) {
              send_failure(res, 500, file_error(err));
              return;
            }
            send_success(res, null);
          }
        );
      }
    );
}
```

## 接收表单 POST 数据

虽然你在应用程序中不会经常使用，但 Web 应用程序发送到服务器有很多数据是通过 `<form>` 元素发送的，例如：

```html
<form name='simple' method='post' action='http://localhost:8080'>
<input name='name' type='text' size='10'/><br>
<input name='age' type='text' size='5'/><br>
<input type='submit' value='Send'/>
</form>
```

如果你编写一个简单的服务器程序，像在上一节中那样使用 `readable` 和 `end` 事件来获取 POST 数据，打印前述表单的数据将得到 `name=marky&age=23`。

然而，你真正需要的是类似于之前通过 JSON 获取的内容：一个代表发送给你的数据的 JavaScript 对象。为了实现这一点，你可以使用 Node.js 内置的另一个模块 `querystring`，专门使用它的 `parse` 函数，如下：

```javascript
var POST_data = qs.parse(body);
```

生成的对象正是你预期的样子：

```javascript
{ name: 'marky', age: '23' }
```

接收表单并打印其内容的完整服务器列表如下：

```javascript
var http = require('http');
var qs = require('querystring');

function handle_incoming_request(req, res) {
  var body = '';
  req.on('readable', function () {
    var d = req.read();
    if (d) {
      if (typeof d == 'string') {
        body += d;
      } else if (typeof d == 'object' && d instanceof Buffer) {
        body += d.toString('utf8');
      }
    }
  });
  req.on('end', function () {
    if (req.method.toLowerCase() == 'post') {
      var POST_data = qs.parse(body);
      console.log(POST_data);
    }
    res.writeHead(200, { "Content-Type": "application/json" });
    res.end(JSON.stringify({ error: null }) + "\n");
  });
}

var s = http.createServer(handle_incoming_request);
s.listen(8080);
```

然而，从第 6 章开始，当你学习如何使用 express Web 框架时，你会发现这些功能通常由框架帮你处理。

# 总结

本章涵盖了很多新材料。你编写了自己的第一个 Web 应用程序简单服务器。我喜欢这种方法有几个原因：

- 它让你专注于服务器以及为了熟悉 Node 所需的关键概念。
- 你可以确保你的服务器组织良好且高效。
- 一个良好的、轻量级的应用程序意味着计算机能够毫不费力地处理负载。

现在你不仅有了一个运行的服务器，还学会了如何通过不同的 URL 和查询参数修改输出。你还学会了如何通过随请求提交 POST 数据来发送新数据或修改现有数据。但首先，休息一下，学习更多关于模块——关于如何使用它们以及如何编写自己的更多。

# 5 模块

Node 的酷之处之一在于，你并不需要区分你生成的模块和从外部仓库获取的模块。在本章中，我将解释它是如何工作的以及如何编写你自己的模块。除了 Node 提供的所有强大且功能完备的模块外，还有一个巨大的社区正在开发模块，你可以在程序中利用它们。

从高层次来说，模块是 Node.js 中分组常用功能的一种方式。如果你有一个用于处理特定数据库的函数或类库，例如，将这些代码放入模块中并打包供他人使用将非常有意义。Node.js 中的每个文件都是一个模块，尽管模块并不非得简单。你可以将包含许多文件、单元测试和其他支持文件的复杂模块封装到文件夹中并像使用单个 JavaScript 文件的模块一样使用它们（参见本章稍后的“编写模块”）。

## 编写模块

要编写自己的暴露（或导出）名为 `hello_world` 函数的模块，你可以编写以下内容并保存为 `mymodule.js`：

```javascript
exports.hello_world = function () {
    console.log("Hello World");
}
```

`exports` 对象是 Node 模块系统在你每个文件中创建的特殊对象，并在包含该模块时作为 `require` 函数的返回值返回。它位于每个模块都拥有的对象之上，用于导出函数、变量或类。在简单的示例中，模块在 `exports` 对象上暴露了一个单元函数，要使用它，你可以编写以下内容并保存为 `modtest.js`：

```javascript
var mm = require('./mymodule');
mm.hello_world();
```

运行 `node modtest.js` 会导致 Node 正如你预期的那样打印出 "Hello World"。你可以根据需要从 `exports` 对象上暴露任意数量的函数和类。例如：

```javascript
function Greeter (lang) {
    this.language = lang;
    this.greet = function () {
        switch (this.language) {
            case "en": return "Hello!";
            case "de": return "Hallo!";
            case "jp": return "こんにちは";
            default: return "No speak that language";
        }
    }
}

exports.hello_world = function () {
    console.log("Hello World");
}

exports.goodbye = function () {
    console.log("Bye bye!");
}

exports.create_greeter = function (lang) {
    return new Greeter(lang);
}
```

传递给每个模块的 `module` 变量包含了当前模块文件名、子模块、父模块等信息。

## 模块与对象

你经常从编写的模块中返回对象。有两种关键模式可以实现。

### 工厂模式

之前的示例模块包含一个名为 `Greeter` 的类。为了获取 `Greeter` 对象的实例，你可以创建一个创建函数——工厂函数——来创建并返回该类的实例。基本模型如下：

```javascript
function ABC (parms) {
  this.varA = ...;
  this.varB = ...;
  this.functionA = function () {
    ...
  }
}

exports.create_ABC = function (parms) {
  return new ABC(parms);
}
```

这种模式的优点是模块仍然可以通过 `exports` 对象暴露其他函数和类。

### 构造函数模式

另一种从编写的模块中暴露类的方法是完全替换模块中的 `exports` 对象为你让人们使用的类：

```javascript
function ABC () {
  this.varA = 10;
  this.varB = 20;
  this.functionA = function (var1, var2) {
    console.log(var1 + " " + var2);
  }
}

module.exports = ABC;
```

要使用此模块，你需要将代码更改如下：

```javascript
var ABCClass = require('./conmod2');
var obj = new ABCClass();
obj.functionA(1, 2);
```

因此，你从模块中真正暴露的内容仅仅是该类的构造函数。这种方法感觉很棒且符合面向对象，但缺点是让你无法暴露太多内容。否则从你的模块导入；它在 Node 的处理方式中也显得有些别扭。我在这里展示给你看，是为了让你在看到它时能认出它是什么，但在本书或你的项目中，你几乎永远不会使用它——你将很大程度上坚持使用工厂模型。

# npm: Node 包管理器

除了编写自己的模块和使用 Node.js 提供的模块外，你还会经常使用 Node 社区其他人编写并发布在互联网上的代码。今天最常用的方法是使用 npm，即 Node 包管理器。npm 随着你的 node 安装程序一起安装（正如你在第 1 章“入门”中所看到的），你可以进入命令行并输入 `npm help` 来验证它仍然存在并运行正常。

通过 npm 安装模块，你需要使用 `npm install` 命令。这种技术只需要你想安装的包名。许多 npm 模块的源代码托管在 `github.com` 上，它们通常会告诉你所需的名称，例如：

```bash
npm install mysql
```

输出示例：

```text
npm http GET https://registry.npmjs.org/mysql
npm http 200 https://registry.npmjs.org/mysql
...
mysql@2.0.0-alpha4 node_modules/mysql
└── require-all@0.0.3
```

如果你不确定想要安装的包的名称，可以使用 `npm search` 命令，如下：

```bash
npm search sql
```

该命令会打印所有匹配模块的名称和描述。npm 将模块安装到项目 `node_modules/` 子目录中。如果一个模块包本身有任何依赖项，它们会被安装到该模块文件夹下的 `node_modules/` 子目录中：

```text
project/
  node_modules/
    module1/
    module2/
      node_modules/
        dependency/
main.js
```

要查看项目当前使用的所有模块列表，你可以使用 `npm ls` 命令：

```bash
npm ls
```

输出示例：

```text
/Users/marcw/src/scratch/project
├── async@0.1.22
├── bcrypt@0.7.3
├── bindings@2.0.0-alpha4
└── require-all@0.0.3
```

要将已安装包更新到更高版本，它只会更新那一个。如果你不指定包名，它将所有包都更新到最新版本：

```bash
npm update mysql
npm update
```

## 消费模块

正如你已经看到的，要在你编写的 Node 文件包含模块，你需要使用 `require` 函数。为了引用该模块上的函数和/或类，你将结果（加载模块的 `exports` 对象）赋值给变量：

```javascript
var http = require('http');
```

包含的模块对于包含它的模块是私有的，因此如果 `a.js` 加载了 `http` 模块，那么 `b.js` 无法引用它，除非自己也加载了 `http`。

## 查找模块

Node.js 使用一组非常直观的规则来查找 `require` 函数请求的模块：

1. 如果请求的模块是内置的——例如 `http` 或 `fs`——Node 将使用它。
2. 如果 `require` 函数中的模块名以路径组件开头——`/`、`../` 或 `./`——Node 会在该特定目录查找该模块并尝试加载它。如果你没有在模块名中指定 `.js` 扩展名，Node 会首先查找同名的文件夹模块。如果没有找到，它会添加 `.js`、`.json`、`.node` 扩展名，并尝试加载这些类型的模块。（扩展名为 `.node` 的模块是编译后的扩展模块）
3. 如果模块名开头没有路径组件，Node 会在当前文件夹的 `node_modules/` 子文件夹中查找模块。如果未找到，它将向上树搜索直到到达根目录。如果仍然未找到，将抛出错误。

## 模块缓存

在模块被加载后，Node.js 会对其进行缓存。对该模块的后续调用将返回缓存的对象，而不是再次执行模块。这对于性能以及处理循环依赖非常重要。

考虑以下结构：

```text
project/
  node_modules/
    module1/
    module2/
      node_modules/
        dependency/
main.js
```

在这个示例中，如果 `main.js` 需要 `module1`，而 `module1` 需要 `module2`，Node 将按顺序加载它们。如果 `main.js` 也需要 `module2`，它将获取缓存的对象。

## 循环

考虑以下情况：

- `a.js` 需要 `b.js`。
- `b.js` 需要 `a.js`。
- `main.js` 需要 `a.js`。

你可以看到这些模块中显然存在循环。Node 通过简单返回未初始化的模块来停止循环。在上述情况下，会发生什么：

1. `main.js` 被加载，并运行 `a.js`。
2. `a.js` 被加载，并运行 `b.js`。
3. `b.js` 被加载，并运行 `a.js`。
4. Node 检测到循环并返回一个指向 `a.js` 的对象，但不再执行更多代码——此时 `a.js` 的加载和初始化尚未完成！
5. `b.js`、`a.js` 和 `main.js` 都完成了初始化（按此顺序），然后 `b.js` 对 `a.js` 的引用就是有效且完全可用的。

## 编写模块

记住 Node.js 中的每个文件本身都是一个模块，拥有模块和导出对象。然而，你也知道模块可能比这复杂得多，有一个包含内容的目录和一个包含打包信息的 `package.json`。对于那些想要包含一组支持文件、将模块的功能拆分为单独的 JavaScript 文件，甚至包含单元测试的情况，你可以按照这种格式编写模块。

基本格式如下：

- 创建存放模块内容的文件夹。



- 在该文件夹中放入一个名为 `package.json` 的文件。该文件至少应包含模块名称和 Node 应该初始加载的主 JavaScript 文件。

- 如果 Node 找不到 `package.json` 文件或未指定主 JavaScript 文件，它将查找 `index.js`（对于编译后的扩展模块则查找 `index.node`）。

## 创建你的模块

现在，将你在上一章中编写的管理照片和相册的代码放入一个模块中。这样做可以让你在以后编写的其他项目中共享它，并对代码进行隔离以便你可以编写单元测试等。

首先，在源码草稿目录 `~src/scratch` 或你任何正在尝试代码的 (Node) 目录中创建以下目录结构：

- `album_mgr/`
- `lib/`
- `test/`

在 `album_mgr` 文件夹中，创建一个名为 `package.json` 的文件并将内容放入其中：

```json
{
  "name": "album-manager",
  "version": "1.0.0",
  "main": "./lib/albums.js"
}
```

这是最基本的 `package.json` 文件；它告诉 npm 该包应该有一个友好的名称 `album-manager`，并且该包的“默认”或启动 JavaScript 文件是 `lib/` 子目录下的 `albums.js` 文件。

上述目录结构并不是强制性的，也不是一成不变的；因此，它只是我发现非常有用并一直采用的常用布局之一。你没有义务遵循它。不过，我建议你从这种方式开始，并不断尝试直到你对整个系统感到熟悉为止。

像 github.com 这样的网站经常被用于托管 Node 模块源码，如果它们发现了 README 文档，则会自动显示。因此，人们包含一个 `Readme.md`（“md”代表 markdown，指代 github.com 使用的标准文档格式）是非常常见的。强烈鼓励你为你的模块编写文档，帮助人们开始使用它。对于 `album-manager` 模块，我写了以下 Readme 文件：

# Album-Manager

这是我们用于基于目录管理相册的模块。我们假设在给定路径下，有一个名为 `albums` 的子文件夹，并且它的每一个单独子文件夹本身就是一个相册。这些子文件夹中的文件就是照片。

## Album Manager (相册管理器)

相册管理器暴露了一个函数 `albums`，它返回一个包含每个每个相册的 `Album` 对象数组。

## Album Object (相册对象)

相册对象具有以下两个属性和一个方法：

- `name` -- 相册名称
- `path` -- 相册的路径
- `photos()` -- 调用此方法将返回相册的所有照片

现在你可以编写实际的模块文件了。首先，从承诺 `lib/albums.js` 开始，它只是第 4 章中一些加载相册的代码被封装成了一个类模块的文件：

```javascript
var fs = require('fs'),
album = require('./album.js');

exports.version = "1.0.0";

exports.albums = function (root, callback) {
  // 我们假设 'albums' 文件夹中的任何目录都是一个相册。
  fs.readdir(
    root + "albums/",
    function (err, files) {
      if (err) {
        callback(err);
        return;
      }

      var album_list = [];

      function iterator(index) {
        if (index == files.length) {
          callback(null, album_list);
          return;
        }

        fs.stat(
          root + "albums/" + files[index],
          function (err, stats) {
            if (err) {
              callback({ error: "file_error",
                message: JSON.stringify(err) });
              return;
            }
            if (stats.isDirectory()) {
              var p = root + "albums/" + files[index];
              album_list.push(album.create_album(p));
              iterator(index + 1);
            }
          }
        );
      })(0);
```

我希望在模块导出功能中提供的标准内容之一是版本字段。虽然我没有使用它，但它可以作为模块检查你的版本并根据不同情况执行不同代码的有用方法。你可以看到相册功能被拆分到了名为 `lib/album.js` 的新文件中，并且有了一个名为 `Album` 的新类。该类如下：

```javascript
function Album (album_path) {
  this.name = path.basename(album_path);
  this.path = album_path;
}

Album.prototype.name = null;
Album.prototype.path = null;
Album.prototype._photos = null;

Album.prototype.photos = function (callback) {
  if (this._photos != null) {
    callback(null, this._photos);
    return;
  }

  var self = this;
  fs.readdir(
    self.path,
    function (err, files) {
      if (err) {
        if (err.code == "ENOENT") {
          callback(no_such_album());
        } else {
          callback({ error: "file_error",
            message: JSON.stringify(err) });
        }
        return;
      }

      var only_files = [];

      function iterator (index) {
        if (index == files.length) {
          self._photos = only_files;
          callback(null, self._photos);
          return;
        }

        fs.stat(
          self.path + "/" + files[index],
          function (err, stats) {
            if (err) {
              callback({ error: "file_error",
              message: JSON.stringify(err) });
              return;
            }
            if (stats.isFile()) {
              only_files.push(files[index]);
            }
            iterator(index + 1)
          }
      })(0);
    });
};
```

如果你对前面的代码中几次使用的 `prototype` 关键字感到困惑，也许现在是回到第 2 章“深入观察 JavaScript”，回顾编写类部分的好机会。这里的 `prototype` 关键字只是为我们 `Album` 类的所有实例设置属性的方法。

再次，这与你在第 4 章中基础 JSON 服务器看到的内容相似。唯一不同的是它被封装成了一个具有名为 `photos` 的原型对象和方法。

我希望你也注意到了以下几点：

1. 你现在使用了一个名为 `path` 的内置模块，并使用 `basename` 函数从路径提取相册名称。

2. 如第 3 章“异步编程”中的“我是谁？保持身份感”节所述，非空 IO 和 `this` 指针可能会变得复杂，所以你使用了 `var self` 技巧来记住你的对象引用。

`album.js` 文件的剩余部分如下：

```javascript
var path = require('path');
var fs = require('fs');

// Album 类在这里

exports.create_album = function (path) {
  return new Album(path);
};

function no_such_album() {
  return { error: "no_such_album",
  message: "指定的相册不存在" };
}
```

这就是我们 `album-manager` 模块所需的全部内容！要测试它，请回到草稿目录并将以下测试程序输入 `atest.js`。

```javascript
var amgr = require('./album_mgr');

amgr.albums('./', function (err, albums) {
  if (err) {
    console.log("意外错误: " + JSON.stringify(err));
    return;
  }

  (function iterator(index) {
    if (index == albums.length) {
      console.log("Done");
      return;
    }
  })(0);
});
```

# 102 第5章 模块

```
Kimidori:Chapter05 marcw$ cd album_mgr
Kimidori:album_mgr marcw$ sudo npm link
/usr/local/lib/node_modules/album-manager -> /Users/marcw/src/scratch/Chapter05/album_mgr
```

请注意，根据你本地机器上权限等的设置，你可能需要使用 `sudo` 以超级用户身份运行此命令。

现在，要使用此模块，你需要做两件事：

- 1. 在代码中使用 `album-manager` 代替 `album_mgr`（因为 npm 使用 `package.json` 中的 `name` 字段）。

- 2. 为每个想要使用该模块的项目使用 npm 创建一个对 `album-manager` 模块的引用。你只需要输入 `npm link album-manager` 即可：

```
Kimidori:Chapter05 marcw$ mkdir test_project
Kimidori:Chapter05 marcw$ cd test_project
Kimidori:test_project marcw$ npm link album-manager
/Users/marcw/src/scratch/Chapter05/test_project/node_modules/album-manager -> /usr/local/lib/node_modules/album-manager
/Users/marcw/src/scratch/Chapter05/album_mgr
Kimidori:test_project marcw$ ls -l
3 staff 102  11 20:18 node_modules/
drwxr-xr-x 2 marcw staff 41 11 20:18 node_modules/
lrwxr-xr-x 1 marcw staff 41 11 20:18 album-manager-> /usr/local/lib/node_modules/album-manager
```

现在，你可以自由修改原始的 album manager 源码，所有引用的它的项目将立即看到更改。

## 发布你的模块

如果你编写了一个想要与其他用户共享的模块，可以使用 `npm publish` 将其发布到官方 npm 仓库。这需要你执行以下操作：

- 从 `package.json` 中删除 `"private": true` 行。

- 使用 `npm adduser` 在 npm 注册表服务器上创建一个账户。

- 可选：选择在 `package.json` 中填写更多字段（运行 `npm help json` 以获取关于你可能想要添加的字段的更多信息），内容如描述、作者联系信息和主机网站等。

- 最后，从模块目录运行 `npm publish` 将其推送到 npm。就是这样！

```
Kimidori:album_mgr marcw$ npm adduser
Username: marcwan
Password:
Email: marcwan@example.org
```

```
npm http PUT https://registry.npmjs.org/-/user/couchdb.user:marcwan
npm http 201 https://registry.npmjs.org/-/user/couchdb.user:marcwan
Kimidori:album_mgr marcw$ npm publish
npm http PUT https://registry.npmjs.org/album-manager
npm http 201 https://registry.npmjs.org/album-manager
npm http GET https://registry.npmjs.org/album-manager
npm http 200 https://registry.npmjs.org/album-manager
npm http PUT https://registry.npmjs.org/album-manager/1.0.0/-tag/latest
npm http 201 https://registry.npmjs.org/album-manager/1.0.0/-tag/latest
npm http GET https://registry.npmjs.org/album-manager
npm http 200 https://registry.npmjs.org/album-manager
npm http PUT https://registry.npmjs.org/album-manager/-/album-manager-1.0.0.tgz/
-rev-2-71f75a35728e1de4ce33469bda1
npm http 201 https://registry.npmjs.org/album-manager/-/album-manager-1.0.0.tgz/
-rev-2-71f75a35728e1cde4ce33469bda1
+ album-manager@1.0.0
```

如果你不小心发布了不想发布的内容，或者想从 npm 仓库中删除某些内容，可以使用 `npm unpublish`：

```
Kimidori:album_mgr marcw$ npm unpublish
npm ERR! Refusing to delete entire project.
npm ERR! Run with --force to do this.
npm ERR! npm unpublish <project>[@<version>]
npm ERR! not ok 0
Kimidori:album_mgr marcw$ npm unpublish --force
npm http GET https://registry.npmjs.org/album-manager
npm http 200 https://registry.npmjs.org/album-manager
npm http DELETE https://registry.npmjs.org/album-manager/-rev/
3-fa97b9b4a1cb8d6de6a3e57d4da2c2f2
npm http 200 https://registry.npmjs.org/album-manager/-rev/
3-fa97b9b4a1cb8d6de6a3e57d4da2c2f2
- album-manager@1.0.0
```

## 一个常用到应该被内置的模块

到目前为止，你已经在代码中使用了几个 Node.js 内置模块（`http`、`fs`、`path` 和 `url`），在随后的内容中你将使用更多。然而，在全书范围内，你会遇到一个非常值得关注的模块，`async` 允许你解决以下问题。

## 问题

考虑以下情况，你需要编写代码来：

- 打开一个文件句柄
- 判断路径是否指向文件
- 读取文件内容
- 关闭文件句柄

正如你所看到的，如果不使用 `async`，编写代码看起来像下面这样（嵌套回调）：

```javascript
var fs = require('fs');

function load_contents(path, callback) {
  fs.open(path, 'r', function (err, f) {
    if (err) {
      callback(err);
    } else {
      fs.stat(f, function (err, stats) {
        if (err) {
          callback(err);
        } else if (stats.isFile()) {
          var b = new Buffer(10000);
          fs.read(f, b, 0, 10000, null, function (err, br, buf) {
            if (err) {
              callback(err);
            } else {
              fs.close(f, function (err) {
                if (err) {
                  callback(err);
                } else {
                  callback(null, b.toString('utf8', 0, br));
                }
              });
            }
          });
        } else {
          callback({error: "not_file",
            message: "Can't load directory "});
        }
      });
    }
  });
}
```

正如你所看到的，如果不使用 `async`，代码会变得深度嵌套。

## 解决方案

为了解决这个问题，你可以使用名为 `async` 的模块。`async` 提供了两种方式来顺序执行代码：通过 `waterfall` 函数和 `series` 函数（见图 5.1）。![Serial execution with waterfall](img/462d9f726aa_121_0.png)。例如，你可以使用 `waterfall` 轻松地重写之前的代码：

```javascript
var fs = require('fs');
var async = require('async');

function load_contents(path, callback) {
  async.waterfall(
    function (callback) {
      fs.open(path, 'r', callback);
    },
    // f（文件句柄）是在 fs.open 调用结束时传递给回调的。
    // async 将所有参数传递给我们。
    function (f, callback) {
      fs.stat(f, function (err, stats) {
        if (err)
          // 终止并直接跳转到结果函数
          callback(err);
        } else {
          // f 和 stats 被传递给下一个 waterfall
          callback(null, f, stats);
        }
      });
    },
    function (f, stats, callback) {
      if (stats.isFile()) {
        var b = new Buffer(10000);
        fs.read(f, b, 0, 10000, null, function (err, br, buf) {
          if (err) {
            callback(err);
          } else
            // f 和字符串被传递给下一个 waterfall
            callback(null, f, b.toString('utf8', 0, br));
          }
        });
      } else {
        callback({error: "not_file",
          message: "Can't load directory "});
      }
    },
    function (f, contents, callback) {
      fs.close(f, function (err) {
        if (err)
          callback(err);
        else
          callback(null, contents);
      });
    },
    // 这个函数在所有函数执行成功后调用，
    // 或者在任何出现错误时立即调用。
    function (err, file_contents) {
      callback(err, file_contents);
    }
  );
}
```

# 108 第 5 章 模块

考虑以下示例：

```javascript
var async = require("async");
```

```javascript
async.series({
  numbers: function (callback) {
    setTimeout(function () {
      callback(null, [ 1, 2, 3 ]);
    }, 1500);
  },
  strings: function (callback) {
    setTimeout(function () {
      callback(null, [ "a", "b", "c"]);
    }, 2000);
  }
}, function (err, results) {
  console.log(results);
});
```

该函数生成以下输出：

`{ numbers: [ 1, 2, 3 ], strings: [ 'a', 'b', 'c' ] }`

## 并行执行

在之前的 `async.series` 示例中，没有理由对函数使用串行执行序列；第二个函数并不依赖于第一个函数的结果，因此它们可以并行执行（见图 5.2）。为此，`async` 提供了 `async.parallel`，如下所示：

```javascript
var async = require("async");
```

```javascript
async.parallel({
  numbers: function (callback) {
    setTimeout(function () {
      callback(null, [ 1, 2, 3 ]);
    }, 1500);
  },
  strings: function (callback) {
    setTimeout(function () {
      callback(null, [ "a", "b", "c"]);
    }, 2000);
  }
}, function (err, results) {
  console.log(results);
});
```

## 一个如此常用以至于应该是内置的模块 109

![](img/462d9f726aa4852bc590bb4b26fa8f32_124_0.png)

图 5.2 使用 `async.parallel` 进行并行执行

该函数的输出与之前完全相同。

## 混合使用

所有函数中最强大的是 `async.auto` 函数，它允许你将有序和无序的函数混合成一个强大的函数序列。在这种情况下，你传递一个对象，其中键名包含：

- 一个要执行的函数，或者
- 一个依赖项数组以及一个要执行的函数。这些依赖项是字符串，是传递给 `async.auto` 的对象的属性名。`auto` 会等待这些依赖项执行完毕后才调用提供的函数。

`async.auto` 会找出执行所有函数所需的顺序，其中哪些函数可以并行执行，哪些需要等待其他函数（见图 5.3）。通过 `async.waterfall` 函数，你可以通过回调参数将结果从一个函数传递给下一个函数：

```javascript
var async = require("async");

async.auto({
  numbers: function (callback) {
    setTimeout(function () {
      callback(null, [ 1, 2, 3 ]);
    }, 1500);
  },
});
```

```javascript
  strings: function (callback) {
    setTimeout(function () {
      callback(null, [ "a", "b", "c" ]);
    }, 2000);
  },
  // 在 numbers 和 strings 完成之前不执行此函数
  // thus_far 是一个包含 numbers 和 strings 数组的对象。
  assemble: ['numbers', 'strings', function (callback, thus_far) {
    callback(null, {
      numbers: thus_far.numbers.join(","),
      strings: "" + thus_far.strings.join(', ') + ""
    });
  }],
}, // 当所有其他函数执行完毕后在最后调用。可选
function (err, results) {
  if (err) {
    console.log(err);
  } else {
    console.log(results);
  }
});
```

![](img/462d9f726aa4852bc590bb4b26fa8f32_125_0.png)

图 5.3 使用 `async.auto` 混合执行模型

# 一个如此常用以至于应该是内置的模块 111

传递给最终结果函数是一个对象，该对象的属性持有在对象上执行的每个函数的结果：

```javascript
{ 
  numbers: [ 1, 2, 3 ],
  strings: ['a', 'b', 'c' ],
  assemble: { numbers: '1, 2, 3', strings: 'a, b, c' } 
}
```

## 异步循环

在第 3 章中，我展示了如何使用以下模式通过异步函数调用来遍历数组中的项：

```javascript
function iterator(i) {
  if(i < array.length) {
    async_work(function(){
      iterator(i + 1)
    });
  } else {
    callback(results);
  }
}}(0);
```

虽然这种技术非常有效而且确实非常极客，但它比我想象的要复杂一点。`Async` 通过 `async.forEachSeries` 提供了帮助。它遍历提供的数组中的每个元素，并为每个元素调用给函数。然而，它会在调用系列中的下一个函数之前等待当前串行执行完毕：

```javascript
async.forEachSeries(
  arr,
  // 为 arr 中的每个元素调用一次
  function (element, callback) {
    // 使用 element
    callback(null); // 你必须为每个元素调用我！
  },
  // 在最后调用
  function (err) {
    // 是否有错误？如果有错误，err 将不为空
  }
);
```

简单来说，

[127]

# 总结

在本章中，你学习了如何使用 `async.series` 按顺序运行任务，使用 `async.parallel` 同时运行任务，以及使用 `async.auto` 管理复杂的任务依赖关系。你还了解了如何使用 `async.forEachSeries` 异步遍历数组。

## 使用流提供静态内容

而是改用 `readable` 事件，并在流通知你数据已准备好读取时，调用流上的 `read` 方法。

如果你看到任何仍然在使用旧的 `data` 事件的代码，你不必担心；它有 99% 的概率与新模型兼容，但我只是想让你意识到，在接过去的一段时间里，你会同时看到这两种写法。

嗯，部分原因在于知道何时事件处于挂起状态或即将发生，例如当你打开了一个可读流，而它实际上有对文件系统的调用正在等待完成内容的读取。只要有预期的事件将发生，Node 就不会在所有事件完成且用户代码（如果有的话）执行之前退出。

上一个示例通过使用 `fs.createReadStream` 给定的路径创建了一个新的可读流。它简单地读取自身并将内容打印到输出流中。它获取一个 `readable` 事件，调用流上的 `read` 方法并返回当前可用的任何数据。如果没有返回数据，它将等待直到另一个 `readable` 事件进入或接收到某个事件。

## 使用 Buffer 操纵二进制数据

因此在你的 Node.js 体验中，你一直在使用字符串（通常是 UTF-8 字符串）来工作。然而，在处理流和文件时，你实际上大部分操作的是 `Buffer` 类。

`Buffer` 的工作方式正如你所预期：它们持有二进制数据，这些数据可以转换为其他格式，用于写入文件的操作，或者被拆分并重新组合。

关于 `Buffer` 需要记住的一个关键点是，对象上的 `length` 属性返回的内容的大小，而是 `Buffer` 自身的大小！例如：

```javascript
var b = new Buffer(10000);
var str = "中国密码"; b.write(str); // 默认 utf8，这是我们需要的
console.log(b.length ); // 将打印 10000!
```

Node.js 不会跟踪你写入 `Buffer` 的内容，你必须自己跟踪这些内容。

有时字符串的字节长度与字符长度并不相同——例如，前面的字符串“中国密码”。`Buffer.byteLength` 返回前者：

```javascript
console.log(str.length ); // 打印 5
console.log(Buffer.byteLength(str)); // 打印 15
```

要将 `Buffer` 转换为字符串，你应该使用 `toString` 方法。你几乎总是需要将其转换为 UTF-8 字符串：

```javascript
console.log(buf.toString('utf8'));
```

要将一个 `Buffer` 追加到另一个 `Buffer` 的末尾，可以使用 `concat` 方法，如下：

```javascript
var b1 = new Buffer("My name is ");
var b2 = new Buffer("Marc");
var b3 = Buffer.concat([ b1, b2 ]);
console.log(b3.toString('utf8'));
```

最后，你可以使用 `fill` 方法来“清零”或填充填充 `Buffer` 中的所有值，例如 `buf.fill("\0")`。

## 使用 Buffer 在 Web 服务器中提供静态文件

对于下一个练习，编写一个使用 Node buffers 提供静态内容（HTML 文件）的微型 Web 服务器。你从 `handle_incoming_request` 函数开始：

```javascript
function handle_incoming_request(req, res) {
  if (req.method.toLowerCase() == 'get'
    && req.url.substring(0, 9) == '/content/') {
    serve_static_file(req.url.substring(9), res);
  } else {
    res.writeHead(404, { "Content-Type": "application/json" });

    var out = { error: "not found",
      message: "" + req.url + " not found" };
    res.end(JSON.stringify(out) + "\n");
  }
}
```

如果传入的请求 `/content/`，则通过调用 `serve_static_file(req.url.substring(9), res)` 来提供静态文件。否则，返回 404 状态码并设置 `Content-Type` 为 `application/json`。

```javascript
function serve_static_file(file, res) {
  var rs = fs.createReadStream(file);
  var ct = content_type_for_path(file);
  res.writeHead(200, { "Content-Type": ct });

  rs.on(
    'readable',
    function () {
      var d = rs.read();
      if (d) {
        if (typeof d == 'string')
          res.write(d);
        else if (typeof d == 'object' && d instanceof Buffer)
          res.write(d.toString('utf8'));
      }
    }
  );

  rs.on(
    'end',
    function () {
      res.end();
    }
  );
}

function content_type_for_path(file) {
  return "text/html";
}
```

服务器的其余代码如你之前看到的：

```javascript
var http = require('http'),
fs = require('fs'),
path = require('path');
```

```javascript
var s = http.createServer(handle_incoming_request);
s.listen(8080);
```

创建一个名为 `test.html` 的文件并在包含简单的 HTML 内容；然后用 `node server.js` 运行。

然后使用 `curl` 请求 `test.html`：

```bash
curl -i http://localhost:8080/content/test.html
```

你应该看到类似下面的输出：

```text
HTTP/1.1 200 OK
Content-Type: text/html
Date: Mon, 26 Oct 2023 13:50:00 GMT
Connection: keep-alive
Transfer-Encoding: chunked

<html>
<head>
<title>Test</title>
</head>
<body>
<h1>Hello!</h1>
</body>
</html>
```

# 第 6 章 扩展你的 Web 服务器

你现在可以提供 HTML 了！但你有两个问题。首先，如果你请求一个不存在的文件会发生什么？在目前的形式，`content_type_for_path` 函数只返回 `text/html`。为了向客户端报告 404，你需要更新 `content_type_for_path` 函数使其更加灵活：

```javascript
function content_type_for_path(file) {
  var ext = path.extname(file);
  switch (ext.toLowerCase()) {
    case '.html': return 'text/html';
    case '.js': return 'text/javascript';
    case '.css': return 'text/css';
    case '.jpg': return 'image/jpeg';
    default: return 'text/plain';
  }
}
```

第二个问题是你目前只能提供 HTML。对于像 JPEG 这样的二进制文件，你可以使用 `-o` 标志告诉 `curl` 写入指定的文件名：

```bash
curl -o test.jpg http://localhost:8080/content/test.jpg
```

现在你有一个名为 `test.jpg` 的文件，它完全如你预期的那样。

## 事件

流 实际上是 Node.js `Event` 类的一个子类，它提供了在 JavaScript 文件中连接和发射事件的所有功能。你可以继承这个类来创建自己的事件触发类。在本示例中，创建一个虚拟的下载器类，通过一个两秒的 `setTimeout` 来模拟远程下载：

```javascript
var events = require('events');

function Downloader() {
  Downloader.prototype = new events.EventEmitter();
  Downloader.prototype.__proto__ = events.EventEmitter.prototype;
  Downloader.prototype.url = null;
  Downloader.prototype.download_url = function (path) {
    var self = this;
    self.url = 'start';
    self.emit('start', path);
    setTimeout(function () {
      self.emit('end', path);
    }, 2000);
  }
}

var d = new Downloader();
d.on("start", function (path) {
  console.log("started downloading: " + path);
});
d.on("end", function (path) {
  console.log("finished downloading: " + path);
});
d.download_url("http://marcwan.com");
```

你通过使用 `emit` 方法、事件名称以及任何你想传递给监听函数的参数，来指示某个事件已被使用。你应该确保所有可能的代码路径（包括错误）都发射了事件；否则，你的 Node 程序可能会挂起。

## 在客户端组装内容：模板

在更传统的 Web 应用模型中，客户端向服务器发送 HTTP 请求，服务器收集所有数据并生成 HTML 响应，然后将其作为文本发送。虽然这种方法非常合理，但它有几个关键的缺点：

- 它没有利用当今普通客户端可用的任何计算能力。即使是普通的手机或平板电脑，其性能也比 10 年前的 PC 强得多。

- 当你有多种类型的客户端时，这会让你的工作变得更加困难。有些人可能通过 浏览器访问你，另一些人通过移动应用，甚至还有人通过桌面应用程序或第三方应用访问。

- 在服务器上执行如此许多不同类型的操作是非常令人沮丧的。如果能让你的服务器专注于处理、存储和生成数据，而让客户端决定如何展示数据，那就太好了。

一种日益常见的方法，也是我发现特别有吸引力且在 Node 中较少的方法，是将服务器后端转换为只提供 JSON，或者尽可能少地提供其他任何内容。客户端应用随后可以选择如何向用户展示返回的数据。脚本、样式表甚至大部分 HTML 都可以从文件服务器或内容分发网络 (CDN) 提供。

对于浏览器应用程序，你可以使用客户端模板（见图 6.1）。通过这种方法：

- 1. 客户端从 Node 服务器下载一个骨架页面，其中包含指向 JavaScript 文件、CSS 文件和空 `body` 元素的指针。

- 2. 引用的 JavaScript 文件之一是一个引导程序（bootstrap），负责完成收集和组装页面的工作。它被赋予了一个 HTML 模板的名称和一个要调用的服务器 JSON API。它下载模板，然后使用模板引擎将返回的 JSON 数据应用到该模板。你将使用一个名为 "Mustache" 的模板引擎（参见侧边栏“模板引擎”）。

- 3. 生成的 HTML 代码被插入页面的 `body` 中，服务器需要做的只是提供一点 JSON。

为了准备这一点，你到目前为止将相册应用开发为了纯 JSON 的服务器。虽然你会添加提供静态文件的功能，但这很大程度上是为了方便和教育目的；在生产环境中，你可能会将这些文件移动到 CDN 并更新 URL 以相应地指向它们。

## 模板引擎

有很多客户端（甚至服务器端）模板引擎或库可用。在本书中你经常使用的 jQuery JavaScript 库之外，还有几个如 JSender 或 Ignite，它们都很好用。其他一些并不一定能与你的 JavaScript 辅助库配合得那么好。

对于你此处的用途来说，它们大同小异。功能集大致相等，实现方式相似，性能也相当相似。当你选择库时，我建议只选择一个正在积极开发和/或维护，并且看起来具有你你觉得舒适的合理语法的库。

对于这本书以及我最近的许多项目，我正在使用一个名为 Mustache 的模板引擎。正如我所说，这个决定是半随机的，但得到了 mustache.js 的帮助。

# 第 6 章 扩展你的 Web 服务器

- 是一个相当小且快速的 JavaScript 库。
- 是一个功能完整的模板解决方案。
- 有一个非常酷的名字。Mustache 中的标签由 `{{` 和 `}}` 分隔，许多人觉得这看起来像胡须（mustaches）。

这种解决方案绝不是完美的，但我怀疑你会发现 Mustache 在功能和速度之间为你提供了恰好的权衡。始终鼓励探索其他解决方案，并阅读所有其他包的几十篇博客文章和教程。

![](img/462d9f726aa4852bc590bb4b26fa8f32_137_0.png)

图 6.1 使用模板进行客户端页面生成

要将你的相册转换为这个新的模板世界，你需要：

- 1. 生成 HTML 骨架。
- 2. 添加提供静态内容的支持。
- 3. 修改 URL 以添加 `/pages/` 和 `/templates/`。
- 4. 加载文件。

开始吧！

## HTML 页面

尽管你可能会在客户端尝试所有操作，你仍然需要一个骨架页面。对于本示例，使用列表 6.1 简单的 HTML：

```html
<!DOCTYPE html>
<html>
<head>
  <title>Photo Album</title>
  <!-- Meta -->
  <meta http-equiv="content-type" content="text/html; charset=utf-8" />
  <!-- Stylesheets -->
  <link rel="stylesheet" href="http://localhost:8080/content/style.css" />
  <!-- javascript -->
  <script src="http://localhost:8080/content/jquery-1.8.3.min.js"></script>
  <script src="http://localhost:8080/content/mustache.js"></script>
</head>
<body>
</body>
</html>
```

## 提供静态内容

现在你按照如下布局修改应用程序的文件夹：

- project_root/
  - contents/ # JS、CSS 和 HTML 文件
  - templates/ # 客户端模板
  - albums/ # 照片

之前见过 albums 文件夹，但现在你要添加 contents 和 templates 文件夹。更新后的 `handle_incoming_request` 函数如下：

```javascript
function handle_incoming_request(req, res) {
  // 解析查询参数为对象并获取不带参数的路径（对于第二个参数解析参数）。
  parsed_url = url.parse(req.url, true);
  var core_url = parsed_url.pathname;

  // 测试此 URL 以查看他们请求什么
  if (core_url.substring(0, 9) == '/content/') {
    serve_static_file("/content" + core_url.substring(9), res);
  } else if (core_url == '/albums.json') {
    handle_list_albums(req, res);
  } else if (core_url.substr(core_url.length - 5) == '.json') {
    handle_get_album(req, res);
  } else {
    send_failure(res, 404, invalid_resource());
  }
}
```

例如，在 content/ 文件夹中，你将从文件：

- `jquery-1.8.3.min.js`——你可以直接从 jquery.com 下载此文件。过去几年的大多数 Jquery 版本都能正常工作。
- `mustache.js`——你可以从很多地方下载此文件。在这种情况下，只需使用来自 github.com/juan/mustache.js 的通用 mustache。还有服务器版本的 mustache，那不是我们本章需要的。
- `style.css`——你可以将其创建一个空文件，或者开始填充 CSS 来修改你将为相册应用生成的页面。

# 在客户端组装内容：模板 125

`/content/some_file.ext`

`/pages/some_page_name[optional/junk]`

`/templates/some_file.html`

对于内容和模板文件，实际上有真实文件可以直接从硬盘中下载。然而，对于页面请求，你始终返回你在上一节中看到的 `basic.html` 的变体。它将 `{PAGE_NAME}` 宏替换为通过 URL 传递的页面名称；例如，/page/home。

更新后的 `handle_incoming_request` 现在看起来如下：

```javascript
function handle_incoming_request(req, res) {
  // 将查询参数解析为对象并获取路径
  // 不包含参数（第二个参数为 true 表示包含参数）
  req_parsed_url = url.parse(req.url, true);
  var core_url = req.parsed_url.pathname;

  // 测试此固定 URL 以查看他们请求的是什么
  if (core_url.substring(0, 7) == '/pages/') {
    serve_page(req, res);
  } else if (core_url.substring(0, 11) == '/templates/') {
    serve_static_file('/templates/' + core_url.substring(11), res);
  } else if (core_url.substring(0, 9) == '/content/') {
    serve_static_file('/content/' + core_url.substring(9), res);
  } else if (core_url == '/albums.json') {
    handle_list_albums(req, res);
  } else if (core_url.substring(0, 7) == '/albums' 
    && core_url.substring(core_url.length - 5) == '.json') {
    handle_get_album(req, res);
  } else {
    send_failure(res, 404, invalid_resource());
  }
}
```

`serve_page` 函数确定客户端请求的页面，修复 `basic.html` 模板文件，并将生成的 HTML 骨架发送到浏览器：

> /**
* 所有页面都来自同一个 HTML 骨架文件，
* 仅更改需要下载的 JavaScript 加载器的名称。
*/

```javascript
function serve_page(req, res) {

  var core_url = req.parsed_url.pathname;
  var page = core_url.substring(7); // 移除 /pages/
```

# 第 6 章扩展你的 Web 服务器

```javascript
// 目前仅支持首页！
if (page == 'home') {
  send_failure(res, 404, invalid_resource());
  return;
}

fs.readFile(
  'basic.html',
  function (err, contents) {
    if (err) {
      send_failure(res, 500, err);
      return;
    }

    contents = contents.toString('utf8');

    // 替换页面名称，然后转到输出。
    contents = contents.replace('{{PAGE_NAME}}', page);
    res.writeHeader(200, { "Content-Type": "text/html" });
    res.end(contents);
  }
);
```

你没有使用 `fs.createReadStream`，而是使用了 `fs.readFile`，它将文件的整个内容读取到 Buffer 中。你必须将此 Buffer 转换为字符串，然后修复内容以指示 JavaScript 加载器。这种方法对于大文件并不推荐，因为会浪费大量内存，但对于像 `basic.html` 这样短的文件，它是完全可行且方便的。

## JavaScript 加载器/启动器

HTML 页面将非常简单，所以你可以从一个相当微不足道的 JavaScript 加载器开始。随着你在书中添加更多功能，你会让它们变得复杂一点，但列表 6.2 显示了你可以开始使用的那个，你可以将其保存为 `home.js`。

## 列表 6.2 JavaScript 加载器 (home.js)

```javascript
$(function() {

  var tmpl, // 主模板 HTML
  tdata = {}; // 填充模板的 JSON 对象

  // 初始化页面
  var initPage = function() {
    // 加载 HTML 模板
    get("/templates/home.html", function(d) {
      tmpl = d;
    });

    // 获取服务器数据并初始化页面
    getJSON("/albums.json", function (d) {
      extend(tdata, d);
    });

    // 当 AJAX 调用完成时，使用变量解析模板
    $(document).ready(function () {
      var renderedPage = Mustache.to_html(tmpl, tdata);
      $("body").html(renderedPage);
    });
  };
});
```

## 在客户端组装内容：模板

对于内容和模板文件，实际上有真实文件可以直接从硬盘中下载。然而，对于页面请求，你始终返回你在上一节中看到的 `basic.html` 的变体。它将 `{PAGE_NAME}` 宏替换为通过 URL 传递的页面名称；例如，/page/home。

## 使用 Mustache 进行模板化

我为应用选择的模板引擎易于使用、速度快且小。有趣的是，它只有包裹在 `{{ }}` 中的标签，被称为 mustache（胡须）。它没有任何 `if` 语句或循环结构。标签充当一组规则，根据你提供的数据来执行。你在之前的几节中看到的 Mustache 的基本用法是：

```javascript
var html_text = Mustache.to_html(template, data);
$("body").html(html_text);
```

要打印对象中的属性，你可以使用以下内容：

专辑 "{{name}}" 有 {{length}} 张。

JSON:

```json
{
  "name": "Italy12",
  "photos": [ "ital1.jpg", "ital2.jpg" ]
}
```

输出：专辑 ItalyItaly12 有 2 张照片。

要在集合或数组中的每个项目中应用模板，你使用 `#` 字符。例如：

Mustache:

```html
{{#albums}}
  {{name}}
{{/albums}}
```

JSON:

```json
{
  "albums": [ 
    { "name": "ital12" },
    { "name": "australia10" },
    { "name": "japan10" } 
  ]
}
```

输出：

- italy12
- australia10
- japan10

如果你没有任何匹配的结果，则什么都不打印。你可以通过添加 `^` 字符来捕获这种情况：

Mustache:

```html
{{#albums}}
  {{name}}
{{/albums}}
{{^albums}}
  没有专辑。
{{/albums}}
```

JSON:

```json
{
  "albums": []
}
```

输出：没有专辑。

如果 `#` 之后的对象不是集合或数组而只是一个对象，则它的值将被使用：

Mustache:

```html
{{#album}}
专辑 "{{name}}" 有 {{length}} 张照片。
{{/album}}
```

JSON:

```json
{
  "album": {
    "name": "Italy12",
    "photos": [ "ital1.jpg", "ital2.jpg" ]
  }
}
```

输出：专辑 Italy12 有 2 张照片。

默认情况下，所有值都会经过 HTML 转义；`<>` 分别替换为 `&lt;` 和 `&gt;`，以此类推。要告诉 Mustache 不要这样做，使用额外的三括号 `{{{` 和 `}}}`：

Mustache:

```html
{{#users}}
  {{name}} 说 {{saying}}
  输出: {{{saying}}}
{{/users}}
```

JSON:

```json
{
  "users": [
    { "name": "Marc", "saying": "I like <em>cats</em>!" },
    { "name": "Bob", "saying": "I <b>hate</b> cats" }
  ]
}
```

输出：

- Marc 说 I like <em>cats</em>！
- 输出: &lt;em&gt;cats&lt;/em&gt;
- Bob 说 I <b>hate</b> cats
- 输出: &lt;b&gt;hate&lt;/b&gt; cats

## 你的首页 Mustache 模板

现在，是时候为你的首页编写第一个模板了，你可以将其保存为 `home.html`，如列表 6.3 所示。

## 列表 6.3 首页模板文件 (home.html)

```html
<div id="album_list">
  <p> 有 {{ albums.length }} 个专辑</p>
  <ul id="#albums">
    {{#albums}}
    <li class="album">
      <a href="http://localhost:8080/pages/album/{{name}}">{{name}}</a>
    </li>
    {{/albums}}
    {{^albums}}
    <li> 抱歉，目前没有专辑。</li>
    {{/albums}}
  </ul>
</div>
```

## 将一切整合在一起

我在之前的几节中向你介绍了许多新东西，所以现在停下来让这一切运行起来。你现在应该拥有如下 Web 应用的文件布局：

```
+ project_root/
  server.js // GitHub 源码
  basic.html // 列表 6.1
  + content/
    home.js // 列表 6.2
    album.js // 列表 6.5
    jquery-1.8.3.min.js
    mustache.js
    style.css
  + templates/
    home.html // 列表 6.3
    album.html // 列表 6.4
  + albums/
    + 你拥有的任何专辑
```

## 在客户端组装内容：模板 (131)

要运行此项目，你应该能够输入

node.js

然后，你可以切换到 浏览器并访问 http://localhost:8080/page/home。如果你想查看命令行中发生了什么，可以尝试像如下那样使用 curl：

curl -i X GET http://localhost:8080/page/home

由于 curl 会替你执行客户端侧的 JavaScript，因此模板和 JSON 数据不会通过 Ajax 加载，你只会从 `basic.html` 获得基础的 HTML 骨架。

列表 6.4 另一个 Mustache 模板页面 (album.html)

```html
<div id="album_page">
  {{photos}}
  <p>此专辑中有 {{photos.length}} 张照片</p>
  <div id="photo">
    <div class="photo_holder">
      <img style="width: 250px; height: 250px; background-color: #fbb" src="{{url}}" border="0"/></div>
    <div class="photo_desc"><p>{{ desc }}</p></div>
  </div>
  <!-- #photos -->
  <div style="clear: left"></div>
  {{photos}}
  {{photos}}
  <p>抱歉，此专辑中没有任何照片。</p>
  {{photos}}
</div>
<!-- #album_page -->
```

列表 6.5 我们的专辑页 Bootstrap JavaScript 文件 (album.js)

```javascript
$(function() {

  var tmpl, // 主模板 HTML
  tdata = {}; // 填充模板的 JSON 数据对象

  // 初始化页面
  var initPage = function() {
```

## 第 6 章 扩展你的 Web 服务器 (132)

```javascript
// 获取我们的专辑名称。
parts = window.location.href.split("/");
var album_name = parts[5];

// 加载 HTML 模板
$.get("/templates/album.html", function(d) {
  tmpl = d;
});
// 获取服务器数据并初始化页面
$.getJSON("/albums/" + album_name + ".json", function (d) {
  var photo_d = message_album(d);
  $.extend(tdata, photo_d);
})

// 当 AJAX 调用完成后，解析模板
// 将 mustache 标签替换为变量
$(document).ajaxStop(function () {
  var renderedPage = Mustache.to_html(tmpl, tdata);
  $("body").html(renderedPage);
});
)();

function message_album(d) {
  if (d.error != null) return d;
  var obj = { photos: [] };

var af = d.data.album_data;

for (var i = 0; i < af.photos.length; i++) {
  var url = "/albums/" + af.short_name + "/" + af.photos[i].filename;
  obj.photos.push({ url: url, desc: af.photos[i].filename });
}
  return obj;
}
```

如果你一切都做得正确，你应该能看到与图 6.2 类似的输出。它并不漂亮，但现在你可以开始尝试模板文件和 `style.css` 文件，让这个应用程序真正属于你了！

## 总结 (133)

![图 6.2 在浏览器中运行的启用模板的 JSON 应用](img/462d9f726aa4852bc590bb4b26fa8f32_148_0.png)

本章介绍了两个关键的 Node.js 特性：流和事件，你利用它们从你的 Web 应用程序中提供静态内容。同样重要的是，本章介绍了客户端模板引擎，你使用了 Mustache 为你的照片专辑应用构建了一个简单的前端起点。

然而，你可能已经注意到，你一直所做的某些事情似乎没必要那么复杂、繁琐，甚至可能容易产生 bug（尤其是 `handle_incoming_request` 函数）。如果能有一些额外的模块来帮助你更容易地跟踪事情，那就太好了。

因此，你不会以目前的形式继续开发这个照片专辑，而是继续查看一些可以显著清理你的代码的模块，并允许你用极少的代码快速添加功能。你将使用 Node 的 Express 框架来完成。

## 第三部分

## 编写 Web 应用程序

- 7 使用 Express 构建 Web 应用程序 (137)
- 8 数据库 I：NoSQL (MongoDB) (161)
- 9 数据库 II：SQL (MySQL) (189)

## 使用 Express 构建 Web 应用程序

到目前为止，你一直在学习 Node.js 的基础和核心概念；凭借了这些思想，你已经构建了一些简单的应用程序，尽管你必须编写大量的代码来完成一些相当基础的事情。现在是时候变换节奏，开始构建更有趣的 Web 应用程序了，利用 Node 最大的优势之一：通过 npm 提供的海量库和模块。现在你已经理解了 Node 和模块的核心工作原理，是时候寻找方法让你的生活变得简单得多，开发速度快多了。

在本章中，你将开始使用 express，这是一个用于 Node 的 Web 应用程序框架。它处理了许多任务。[注意：提供的 OCR 文本在第 150-154 页后半部分包含重复/乱码内容，已根据书籍结构的逻辑流进行了清理和对齐]。

140 第 7 章 使用 Express 构建 Web 应用程序

在之前的 express 应用中，序列中只有一层：

`app.get('/', function(req, res) { });`

该函数是 express 提供的一个辅助函数，当满足以下两个条件时，它会通过通过提供的函数处理传入的请求：

- HTTP 请求方法为 GET。
- 请求的 URL 为 /。

如果传入的请求不符合这些标准，则不会调用该函数。如果没有函数匹配请求的 URL——例如，通过浏览器或 curl 访问 /some/other/url——express 将给出一个默认响应：

Cannot GET /some/other/url

## 路由基础

URL 路由函数的通用格式如下：

`app.method(url_pattern, optional_functions, request_handler_function);`

前面的路由处理器是用于处理针对 URL / 的 GET 请求。为了在特定 URL 上支持 POST 请求，可以使用 express 应用对象上的 `post` 方法：

```javascript
app.post("/forms/update_user_info.json", function(req, res) { ... });
```

同样，express 支持 `DELETE` 和 `PUT` 方法，你可以在照片共享应用中分别通过 `delete` 和 `put` 方法使用它们。此外，你可以使用 `all` 方法来指示路由函数应该接受带有任何给定 HTTP 方法的给定 URL：

```javascript
app.all("/users/marwan.json", function (req, res) { ... });
```

路由函数的第一个参数是一个用于匹配传入请求 URL 的正则表达式。它可以简单如：

`/path/to/resources`

或者它可以包含正则表达式特征，例如

`/user(s)?/list`

同时匹配 `/users/list` 和 `/user/list`，

`/users/*`

匹配任何以 `/users/` 开头的内容。

## Express 中的路由与层

路由最强大的功能之一是能够放置占位符从请求的路由中提取命名值，占位符由冒号（:）标记。当路由被解析时，express 会为你将匹配的占位符存放在 `req.params` 对象上。例如：

```javascript
app.get('/albums/:album_name.json', function (req, res) {
  res.end("Requested " + req.params.album_name);
});
```

如果你调用上面的 app 请求 `/albums/italy2012.json`，你将得到以下输出：

Requested italy2012.

你也可以在同一个 URL 中放置多个参数：

```javascript
app.get('/albums/:album_name/photos/:photo_id.json', function (req, res) { ... });
```

如果你的函数被调用，`req.params` 将同时包含 `album_name` 和 `photo_id` 并设置为相应的传入值。占位符匹配除正斜杠以外的任何字符序列。

如你所见，提供给方法的函数接收请求和响应对象。然而，它还会接收第三个参数，你可以自由使用或忽略它。它通常被标记为 `next`（分层函数的流始终通过调用 `next` 的函数继续），并为你提供了机会对传入的 URL 进行一些额外的检查并仍然选择忽略它，如下：

```javascript
app.get('/users/:userid.json', function (req, res, next) {
  var uid = parseInt(req.params.userid);
  if (uid < 2000000000) {
    // 不想要它。让别人处理它。
    next();
  } else {
    res.end(get_user_info(uid));
  }
});
```

## 为你的照片应用适配路由

照片册应用很容易适配到 express。你只需要做几件事即可让它运行：

- 创建 `package.json` 并安装 express。
- 将 `http` 模块的服务器替换为 express 的服务器。
- 将 `handle_incoming_request` 函数替换为路由处理器。
- 更新在 express 中查询参数的方式。（为了方便，它们在 `req.query` 上。）

# 第 7 章 使用 Express 构建 Web 应用程序

将你在第 6 章“扩展你的 Web 服务器”末创建的照片应用的最后一个版本复制到一个新文件夹（你可以命名为 `basic_routing/`），并在其中放入以下 `package.json`：

```json
{
  "name": "Photo-Sharing",
  "description": "Our Photo Sharing Application",
  "version": "0.0.2",
  "private": true,
  "dependencies": {
    "async": "0.1.x",
    "express": "3.x"
  }
}
```

你可以运行 `npm install` 来确保 express 和 async 已安装到 `node_modules/` 中。你可以修改 `server.js` 文件的顶部，使用 express 代替 `http` 模块：

```javascript
var express = require('express');
var app = express();
```

```javascript
var path = require('path');
var async = require('async');
var fs = require('fs');
```

然后你将

```javascript
http.listen(8080);
```

改为

```javascript
app.listen(8080);
```

接下来，你必须替换 `handle_incoming_request` 函数，它的样子如下：

```javascript
function handle_incoming_request(req, res) {
  req.parsed_url = url.parse(req.url, true);
  var core_url = req.parsed_url.pathname;

// 测试这个固定的 URL 看看他们在请求什么
if (core_url.startsWith('/albums/')) {
  // ...
}
```

（注：原文中该函数的代码是不完整的，但逻辑符合章节的上下文。）

## REST API 设计与模块

- 集合（Collections）应该是名词，具体说是复数名词，例如 `albums`（专辑）、`users`（用户）或 `photos`（照片）。
- `PUT /albums.json`——HTTP 请求体包含带有新专辑数据的 JSON。
- 你通过通过在集合上分别使用 GET 或 POST 请求并指定特定实例来获取或更新对象：
- `GET /albums/italy2012.json`——请求返回此专辑。
- `POST /albums/italy2012.json`——HTTP 请求体包含带有该专辑新数据的 JSON。
- 你使用 `DELETE` 销毁对象。
- `DELETE /albums/italy2012.json`——销毁此专辑。
- 如果你有嵌套的集合（例如与专辑关联的照片），你只需继续这种模式即可：
- `GET /albums/italy2012/photos.json`——返回此专辑中的所有照片。
- `PUT /albums/italy2012/photos.json`——在此集合中添加一张新照片。
- `GET /albums/italy2012/photos/23482938424.json`——获取给定 ID 的照片。
- 从这些集合中获取数据的方式细微更改（如分页或过滤）都应通过 GET 查询参数完成：
- `GET /albums.json?located_in=Europe`——仅获取位于欧洲的专辑。
- `GET /albums/japan2010.json?page=1&page_size=25`——获取 japan2010 专辑的指定页 25 张照片。
- 对你的 API 进行版本控制，这样如果你想对未来的版本做出不兼容的重大更改，只需更新版本号即可。对于第一个版本，我们在 API URL 前加上了 `/v1/`。
- 最后，对所有返回 JSON 的 URL 加上 `.json` 后缀，以便客户端知道响应中将包含哪些数据。在将来，你还可以添加对 `.xml` 或你使用的其他格式的支持。

基于这些考虑，照片共享应用程序的新 API 以专辑为中心。其结构如下：

```
/v1/albums.json
```

```
/v1/albums/:album_name.json
```

```
/pages/:page_name
```

```
/templates/:template_name
```

```
/content/:filename
```

## 146 第 7 章 使用 Express 构建 Web 应用程序

为什么不在静态内容的 URL 上放置版本号呢？因为它们不是 JSON 服务器 接口的一部分，而是为 Web 浏览器客户端提供内容的辅助工具。用户始终获取这些内容的最新版本，因此代码知道如何使用正确版本的 API。

使用此 API 设计更改更新 `server.js` 文件应该是轻而易举的。别忘了也用新 URL 更新 `/content/` 中的引导（bootstrap）JavaScript 文件！在继续之前之前尝试一下。

## 模块

随着围绕新的 REST 接口更新了 API，你可以利用你为应用程序提供的某些清晰度。你现在在专辑和页面周围拥有了清晰的功能边界，因此你可以将这些功能区域放入你的模块中。

在应用程序文件夹下创建一个名为 `handlers/` 的子文件夹，并将新模块放入其中。对于专辑，在 true文件夹中创建一个 `albums.js` 文件，并将四个专辑操作函数移动到该文件中。你可以在 GitHub 的名为 `handlers_as_modules/` 的项目中查看此项目的源码；实际上，你所做的只是将 `handle_get_album` 和 `handle_list_albums` 函数的代码连及其辅助函数 `load_album` 和 `load_album_list` 一起放入新模块中。花几分钟看看快速重组织代码是多么简单。

记得 `server.js` 文件中有帮助你提取专辑名称和查询参数等内容的函数。你可以删掉它们，直接在正确的地方开始 `req.params` 和 `req.query` 的成员引用。

还有一些函数可以帮助简化发送成功和错误代码，例如 `send_success`、`send_failure` 和 `invalid_resource`。你可以将它们放入 `handlers/` 目录下的名为 `helpers.js` 的自定义模块中。你在 `albums.js` 文件的顶部引用它，内容见代码列表 7.1。

#### 代码列表 7.1 辅助函数 (helpers.js)

```javascript
exports.version = '0.1.0';
exports.make_error = function(err, msg) {
  var e = new Error(msg);
  e.code = err;
  return e;
}
exports.send_success = function(res, data) {
  res.writeHead(200, {"Content-Type":"application/json"});
  var output = {error: null, data: data };
  res.end(JSON.stringify(output) + "\n");
}
```

## REST API 设计与模块

```javascript
exports.send_failure = function(res, code, err) {
var code = (err.code) ? err.code : err.name;
res.writeHead("Content-Type": "application/json"});
res.end(JSON.stringify({ error: code, message: err.message }) + "\n");
}
```

```javascript
exports.invalid_resource = function() {
return make_error("invalid_resource",
  "the requested resource does not exist.");
}
```



```javascript
exports.no_resource = function() {
  return make_error("invalid_resource",
    "the requested resource does not exist.");
}
```

现在，当你想要引用时，在 `server.js` 中添加以下内容：

```javascript
var hdl = require('./handlers/albums');
```

同样，你可以将页面移动到 handlers 中，如代码列表 7.2 所示。

#### 代码列表 7.2 页面 (pages.js)

```javascript
var helpers = require('../helpers');

exports.page = function(req, res) {
  var album_name = req.params.album_name;
  helpers.get_album(album_name, function(err, album) {
    if (err) {
      return helpers.invalid_resource(res);
    }
    helpers.send_success(res, album);
  });
};
```

## 第 7 章 使用 Express 构建 Web 应用程序

在某些配置中使用部分中间件是有帮助的。某些中间件可能会为了速度或大小修改输出，导致使用 `curl` 测试服务器变得困难或烦恼。要这样做，你可以在 express 应用上调用 `configure` 方法，提供你想要的目标配置名称以及在需要配置时调用的函数，如下所示：

```javascript
app.configure(function () {
  app.use(express.bodyParser());
});
```

```javascript
app.configure('dev', function () {
  app.use(express.logger('dev'));
});
```

```javascript
app.configure('production', 'staging', function () {
  app.use(express.logger('dev'));
});
```

## 第 7 章 使用 Express 构建 Web 应用

在 `configure` 函数调用之外设置的中间件或路由被认为适用于所有配置。

要使用特定的配置运行应用程序，请将 `NODE_ENV` 环境变量设置为你想要的值。在你的 Mac 或 UNIX 计算机的大多数 shell 中，你可以如下运行运行 node：

`NODE_ENV=production node program.js`

在 Windows 上，你可以在命令提示符中直接设置 `NODE_ENV` 然后运行 node（请进行验证 VERIFY）：

```cmd
set NODE_ENV=production
node program.js
```

## 中间件的顺序

这些中间件组件的层级结构和顺序非常重要。正如我提到的，express 和 connect 会逐个通过这些中间件，直到它们发现自己可以处理该请求为止。为了了解这其中的联系，请考虑以下简单的应用：

```javascript
var express = require('express');
var app = express();

app.use(express.logger('dev'));
// 将此行移动到下一个 use() 之后看看会发生什么！
.use(express.responseTime())
.use(function(req, res) {
  res.end('hello world\n');
})
.listen(8080);
```

通过以下方式调用此应用：

```bash
curl -i localhost:8080/blargh
```

你应该看到看到内容：

```http
HTTP/1.1 200 OK
X-Powered-By: Express
X-Response-Time: Oms
Date: Wed, 05 Dec 2012 04:11:43 GMT
Connection: keep-alive
Transfer-Encoding: chunked

hello world
```

现在，观察如果将 `responseTime` 中间件组件移动到末尾会发生什么：

## 额外的中间件功能

```javascript
var express = require('express');
var app = express();

app.use(express.logger('dev'));
// 将此行移动到下一个 use() 之后看看会发生什么！
.use(function(req, res) {
  res.end('hello world\n');
});
.use(express.responseTime())
.listen(8080);
```

注意，`X-Response-Time` 头部消失了！

```http
HTTP/1.1 200 OK
X-Powered-By: Express
Date: Wed, 05 Dec 2012 04:14:05 GMT
Connection: keep-alive
Transfer-Encoding: chunked

hello world
```

打印“Hello World!”的函数获取了请求并通过不调用 `next` 以及使用 `res.end` 关闭响应来完全处理了它，因此 `responseTime` 中间件没有机会检查该请求。当你正在添加中间件组件时，请考虑它们将如何与你的应用程序将使用的各种路由相契合在一起。

## 静态文件处理

你编写了一些 Node 代码来为应用程序提供静态文件，但事实证明这样做在很大程度上是没必要的。Express（通过 connect）提供了一个静态中间件组件，可以为你完成所有这些工作！

要使用它，你只需将想要静态提供的内容的根文件夹名称传递给中间件创建函数，如下：

```javascript
app.use(express.static('/secure/static_site_files'));
```

你将其放置在 URL 路由之前，当请求进来时，这个静态层会获取 URL，将其附加到其基础文件夹名称，并查找该文件是否存在。例如，如果你请求 `/content/style.css`，此中间件会检查 `/secure/static_files/content/style.css` 是否存在且可读。如果是，中间件将提供该文件并停止调用后续层级。如果不是，它将调用下一个函数。

如果你想从多个位置提供静态内容，请添加多个组件：

```javascript
app.use(express.static('/secure/core_static_content'));
app.use(express.static('/secure/templates_and_html'));
```

## 第 7 章 使用 Express 构建 Web 应用

注意，虽然技术上你可以通过 Node 中的预定义变量 `__dirname` 从你的应用程序文件夹提供内容（它为你提供了当前执行的 Node 脚本的路径），但这是一个糟糕的主意，你不应该永远这样做。

静态中间件完全没有提供任何安全性，所以你可以参考之前的照片共享应用程序，只需添加：

```javascript
app.use(express.static(__dirname));
```

然后你就可以——如所预期——毫无问题地浏览 `/content/style.css` 和 `/templates/home.html`。问题在于，如果用户请求 `/server.js` 或 `/handlers/albums.js`，静态中间件会乐于提供它们，因为它们位于 `__dirname` 文件夹之外。

你可能会问为什么没有给静态中间件组件添加安全性，但这是一个错误的问题——这是一个不必要的复杂化。如果你想使用此组件，请将你的静态内容放在应用程序源码树之外。事实上，正如我之前暗示的那样，你甚至可以选择让你的应用程序完全避免提供静态内容，转而选择将静态内容放在 CDN 上。因此，从开始就要习惯于将这些组件从源码树中分离出来。

如果你重写 `server.js` 来使用静态中间件，它看起来像下面所示。然而，这需要将 `content/`、`templates/` 和 `album/` 文件夹移动到另一个位置，以便避免我刚才提到的安全问题。更新后的应用结构如下：

- root_folder/
  - static/
  - albums/
  - content/
  - templates/
  - app/
  - handlers/
  - node_modules/

那么 `server.js` 文件可以像那样。它确实，需要，你移动内容到另一个位置，以便避免我刚才提到的安全问题。更新后的应用结构如下：

## 7.3 使用静态中间件 (server.js)

```javascript
var express = require('express');
var app = express();

var fs = require('fs');
var hdlr = require('./handlers.js'),
page_name = require('./pages.js'),
helpers = require('./helpers.js');

app.use(express.static(__dirname + "/static"));

app.get('/albums.json', hdlr.all);
app.get('/page_name', hdlr.generate());
app.use('/', page_name);

app.get('*', function (req, res) {
  res.status(404).end("Not found");
});
```

## POST 数据、Cookies 和会话

Express 和 connect 为你提供了 Cookie。要在响应上设置 Cookie，使用带有名称和可选值：

```javascript
var express = require('express');

var app = express();

app.use(express.logger('dev'))
.use(function(req, res) {
  res.cookie('pet', 'Zimba the Monkey', { expires: new Date(Date.now() + 86400000) });
  res.end();
})
.listen(8080);
```

要清除你设置的 Cookie，只需在响应上使用 `clearCookie` 并传入 Cookie 名称。

设置会话要复杂一些，需要先提供一个 store 和一个加密的密钥：

```javascript
var MemStore = express.session.MemoryStore;
app.use(express.session({
  secret: "cat on keyboard",
  cookie: { maxage: 1800000 },
  store: new MemStore()
}));
```

在这个示例中，你设置了一个密钥，然后使用 connect 模块提供的 `MemoryStore` 类。这非常方便易用，但每次重启 Node 都会重置。如果你希望跨服务器持续，你应该在 npm 中查找其他外部存储，如 memcache 或 redis（见接两个章节）。默认情况下，会话不会过期。如果你想它们过期，请提供有效毫秒数。在这里，代码表示将接受超过 30 分钟的 Cookie。

当会话就绪后，`req.session` 填充了会话数据。要添加新的会话数据，只需在对象上设置新值。它会被持久化并随响应发送：

```javascript
var express = require('express');
var MemStore = express.session.MemoryStore;

var app = express()
  .use(express.logger('dev'))
  .use(express.cookieParser())
  .use(express.session({
    secret: "cat on keyboard",
    cookie: { maxage: 1800000 },
    store: new MemStore()
  }))
  .use(function (req, res) {
    var x = req.session.last_access; // 未设置 cookie 时为 undefined
    req.session.last_access = new Date();
    res.end("You last asked for this page at: " + x);
  })
  .listen(8080);
```

## 文件上传

express `bodyParser` 中间件组件会自动包含 `connect multipart` 组件，它提供了对文件上传的支持。如果你使用 `multipart/form-data` 编码类型向应用上传文件，那么 `req.files` 将包含随请求发送的任何文件：

```javascript
var express = require('express');
var app = express();
app.use(express.logger('dev'));
app.use(express.bodyParser());
app.use(function (req, res) {
  if (!req.files || !req.files.album_cover) {
      res.end("Hunh. Did you send a file?");
  } else {
      console.log(req.files);
      res.end("You have asked to set the album cover for " 
        + " to " + req.body.albumid
        + " to " + req.files.album_cover.name + "\n");
    }
});
app.listen(8080);
```

要测试这一点，你仍然可以使用 `curl`！它可以通过结合 `-F` 选项（用于表单数据）和带有文件名的 `@` 操作符随请求上传文件，这告诉它发送文件：

```bash
curl -i -H "Expect:" -F album_cover=@oranges.jpg -F albumid=italy2012 http://localhost:8080
```

不过有一个技巧，`curl` 有时会期望服务器发送 100 Continue 响应并挂起。为了解决这个问题，给 `curl` 使用 `-H "Expect:"`，这样你就可以正常测试文件上传了。

## 对 PUT 和 DELETE 更好的浏览器支持

PUT（创建对象）和 DELETE（删除对象）是你使用的 REST API 的关键部分，客户端 Web 应用通过这些方法向服务器发送数据。例如，在 jQuery 中，若要删除一条评论，使用：

```javascript
$.ajax({
  url: 'http://server/v1/comments/234932598235.json',
  type: 'DELETE'
});
```

在大多数现代浏览器中，这种技术工作得很好。然而，在某些旧浏览器（以及任何 10 之前的之前的 Internet Explorer 版本）中，它会失效。原因是它们对 `XMLHttpRequest`（AJAX 请求所属的对象）的实现不支持 PUT 或 DELETE 作为方法。

一种常见且优雅的解决方案是在你的输出中添加一个名为 `X-HTTP-Method-Override` 的新头部，并带有你真正想要使用的方法，然后只需使用 POST 将请求发送到服务器。此时，jQuery 代码将变为：

```javascript
$.ajax({
  beforeSend:function(xhr) {
    xhr.setRequestHeader('X-HTTP-Method-Override', 'DELETE');
  },
  url: 'http://server/v1/comments/23932598235.json',
  type: 'POST'
});
```

要在你的服务器上支持此解决方案，你需要使用 `methodOverride` 中间件，如下：

`app.use(express.methodOverride());`

它会查找此头部并根据需要将 POST 请求转换为 DELETE 或 PUT。因此，`app.delete` 和 `app.put` 路由将完全按照预期工作。

## 压缩输出

为了节省带宽成本和速度，许多 Web 服务器在将输出发送到客户端之前，使用 gzip 或某些类似算法对输出进行压缩。这要求客户端首先通过 `Accept-Encoding` HTTP 头部指示它可以接受压缩输出。如果提供了该头部且服务器已知，它会在输出时添加指定了适当算法的 `Content-Encoding` 头部，然后发送压缩后的数据。

要在你的应用中使用此功能，可以使用 `compress` 中间件。它是一个真正无忧的组件；它会通过头部检查客户端是否接受压缩输出，设置响应头部并压缩输出，如下：

```javascript
var express = require('express');
var app = express();

app.use(express.logger('dev'));
app.use(express.compress());
```

```javascript
app.get('/', function(req, res) {
  res.send('hello world this should be compressed\n');
});

app.listen(8080);
```

该模块唯一的缺点是它可能会干扰你的某些开发测试（`curl` 只是会将压缩后的二进制数据打印到屏幕上，这可能很困扰），所以你通常会在生产配置中使用它，如下：

```javascript
var express = require('express');
var app = express();

app.use(express.logger('dev'));
app.configure('production', function () {
  app.use(express.compress());
});

app.get('/', function(req, res) {
  res.send('hello world this should be compressed\n');
});

app.listen(8080);
```

## HTTP 基础认证

如果你想在应用程序中使用 HTTP 基础认证，中间件也可以为你提供帮助。尽管基础认证经常被认为过时且不安全，但当结合 SSL 和 HTTPS 时，它实际上可以为你的应用程序提供一个合理且足够稳健的安全解决方案。

要使用它，你需要设置 `basicAuth` 中间件，提供一个接收用户名和密码的函数。如果提供的身份验证信息有效，则返回 true，否则返回 false，如下：

```javascript
var express = require('express');
var app = express();

app.use(express.basicAuth(auth_user));
app.get('/', function(req, res) {
  res.send('secret message that only admin users can see\n');
});

app.listen(8080);
```

```javascript
function auth_user(user, pass) {
  if (user == 'marcwan'
      && pass == 'this is how you get ants') {
    return true;
  } else {
    return false;
  }
}
```

如果你运行此服务器并尝试访问它，它会在让你继续之前向你索要用户名和密码。

## 错误处理

虽然你可以对每个请求单独处理错误，但有时你可能希望为常见情况有一个全局错误处理器。要实现这一点，你向 `app.use` 方法提供一个接受四个参数的函数：

```javascript
app.use(function (err, req, res, next) {
  res.status(500);
  res.end(JSON.stringify(err) + "\n");
});
```

此方法放置在其他中间件设置和路由函数之后，因此它是 express 调用的最后一个函数。你可以在此函数中检查错误并决定返回给用户什么。例如：

```javascript
var express = require('express');
var app = express();

app.get('/', function(req, res) {
  throw new Error('Something bad happened');
  res.send('Probably never get to this message.\n');
});

app.listen(8080);
```

最后，Node.js 允许你通过 `process` 对象指定一个全局范围的错误处理器：

```javascript
process.on('uncaughtException', function (err) {
  console.log('Caught exception: ' + err);
});
```

然而，将其用于日志或诊断之外是非常糟糕的想法。如果调用了此函数，你应该假设 Node.js 处于非常不健康或不稳定的状态并应该重启。因此，在使用此函数时，仅仅是为了记录错误并终止 node 进程：

```javascript
process.on('uncaughtException', function (err) {
  console.log('Caught exception: ' + err);
  process.exit(-1);
});
```

## 总结

这是另一个大章节，包含了许多有趣的新内容。我介绍了 express 框架，讨论了中间件，描述了如何使用 cookie 和 session，并帮助你将照片共享应用中的一些代码转换为模块。

你的照片共享应用看起来已经不错了，但它仍然感觉很原始；你的专辑中只有图片，没有很好的地方存储你可能想添加到专辑或照片的任何额外信息。针对这个问题，在接下来的章节中，你将查看数据库——首先是 NoSQL (CouchDB)，然后是 MySQL——并如何在 Node 中使用它们。你还将查看一些缓存解决方案，并继续扩展这个小应用使其成为实用的工具。

## 数据库 I：NoSQL (MongoDB)

现在你已经为 Web 应用程序打下了坚实的基础，并完全配置好了 Express Web 框架和 Mustache 模板，你准备好花几个章节为它添加后端了。在接下来的两个章节中，你将学习实现这一点的两种常用方法。在本章中，我们首先介绍一种名为 MongoDB 的流行 NoSQL 数据库，它提供了一种快速简单的方法将 JSON 数据直接序列化数据库。本章将涵盖使用它的基础知识，然后更新你的相册处理程序，以便将相册和照片数据存储到数据库中。

我选择 MongoDB 而不是其他流行的 NoSQL 数据库（特别是 CouchDB），因为它特别容易使用，并且具有一些其他数据库无法直接提供的优秀查询功能。由于这本书的目标是教你如何使用 Node.js，因此我想选择最易于操作的数据库服务器，让你能更舒适地专注于我的核心任务。

如果你熟悉 MySQL 或其他关系型数据库，本章仍然非常值得阅读，因为你将从中看到如何将相册和照片处理程序从基于文件的模块迁移到数据库支持的模块。在下一章中，我将讨论关系型数据库系统，并提供一个 MySQL 版本的代码。

## 设置 MongoDB

要在 Node.js 应用程序中使用 MongoDB，你需要做两件事：安装数据库服务器本身，并让它与 Node 工作。

## 安装 MongoDB

要开始使用 MongoDB，你可以直接从 http://mongodb.org 下载二进制文件。大多数平台的发行版都是 zip 格式，你将其解压到你想要运行 MongoDB 的位置。

在 `bin/sub` 目录下，你应该能找到一个名为 `mongod` 的文件，它是基础数据库服务器守护进程。在开发环境中运行服务器，你通常使用：

```bash
mongod --dbpath /path/to/db  # unix
mongo --dbpath \path\to\db  # windows
```

你可以创建一个像 `/etc/mongod` 或类似的文件夹来存放你的数据库。要快速删除它们并重启数据库服务器，按下 Ctrl+C 杀死当前服务器，然后运行以下命令：

```bash
rm /path/to/db/dir/* && ./mongod --dbpath /path/to/db  # unix
del \path\to\dir\* # windows 1
mongo --dbpath \path\to\db  # windows 2
```

为了测试安装，打开另一个终端窗口或命令提示符，运行 `mongo` 程序，它会运行一个非常像 Node REPL 的简单解释器：

```
Kimidori:bin ./mongo
MongoDB shell version: 2.2.2
connecting to: test
> show dbs
local (empty)
>
```

对于部署到线上生产环境，你应该进一步阅读 MongoDB 文档并学习最佳实践和配置选项，例如设置复制和备份。

## 在 Node.js 中使用 MongoDB

验证 MongoDB 安装后，你需要将其连接到 Node.js。目前最流行的驱动是由制作 MongoDB 的公司 10gen 编写的官方 `native-mongodb`。对于 MongoDB 和 Node.js，有一个名为 `mongoose` 的关系对象映射 (ROM) 层，它非常流行，但在本书中你可以坚持使用简单的驱动程序，因为它可以让代码结构更具数据库无关性（我们将在下一章中看到）。

要安装 `mongodb` 模块，请在你的 `package.json` 文件添加以下内容：

```json
{
  "name": "MongoDB-Demo",
  "description": "Demonstrates Using MongoDB in Node.js",
  "version": "0.0.1",
  "private": true,
  "dependencies": {
    "async": "0.1.x",
    "mongodb": "1.2.x"
  }
}
```

## 为 MongoDB 构建数据结构

然后你可以运行 `npm update` 来获取所有驱动程序的最新版本。如果你查看 `node_modules/` 文件夹，你应该能看到里面的 `mongodb/` 子文件夹。

MongoDB 非常适合在应用程序中使用，因为它本身使用 JSON 进行存储。每当你向数据库创建或添加内容时，你传递的都是 JavaScript 对象——这对于 Node 开发者来说非常方便！

如果你以前使用过关系型数据库，你可能熟悉数据库、表和行的术语。在 MongoDB 中，这些元素分别称为数据库（databases）、集合（collections）和文档（documents）。数据库被划分为对象集合，所有对象都由 JSON 文档表示。

MongoDB 中的所有对象都有一个唯一标识符，由 `_id` 表示。由于它是唯一值，它基本上可以是任何类型。如果你不提供，MongoDB 会为你创建一个：它是 `ObjectId` 类的实例。打印时，它返回一个 24 位的十六进制字符串，例如 `5da80ce04d403ebda700012`。

## 一切都是 JavaScript

对于照片应用程序，你需要创建两种文档类型：一种用于相册，另一种用于相册内的照片。你不需要使用 MongoDB 自动生成的 `_id` 值，因为你始终拥有用于文档的唯一标识信息：对于相册，`album_name` 始终是唯一的；对于照片，`album_name` 和照片文件名的组合是唯一的。

因此，你以如下方式存储相册：

```javascript
{ _id: "vacation2023", name: "Vacation 2023", description: "My trip" }
```

你的照片文档看起来类似于所示：

```javascript
{ _id: "beach.jpg", filename: "beach.jpg", album: "vacation2023", description: "The beach" }
```

尝试向集合中插入具有重复 `_id` 的值会导致 MongoDB 抛出错误。

## 数据类型

在大多数情况下，在 JavaScript 中操作 MongoDB 是完全自然且。然而，你可能会在某些场景中遇到麻烦，因此值得介绍它们。

正如你在前面的章节中看到的，JavaScript 将所有数字表示为 64 位双精度浮点数。这为你提供了 53 位的整数精度。但经常存在对 64 位整数值的实际需求。当精度降低和近似不可接受时，你可以使用 `mongodb` 驱动提供的 `Long` 类。它在构造函数中接受字符串值，并允许你对整数值进行操作。

JavaScript 还有一个 `Binary` 类，你可以解析字符串或 `Buffer` 对象实例，当你稍后重新加载文档时，该值将返回给你，并带有一些描述 MongoDB 如何存储它的额外元数据。

最后，我想提到 `Timestamp` 类，它将时间保存到数据库文档中，但在你实际写入记录时执行操作。所以你可以这样设置值：

```javascript
{ _id: "unique_identifier1234", when: new Timestamp(), what: "Good News Everyone!" }
```

## 理解基本操作

现在是时候让 MongoDB 和 Node.js 运行起来了。在每个使用 `mongodb` 模块的文件的顶部，包含以下内容：

```javascript
var Db = require('mongodb').Db,
Connection = require('mongodb').Connection,
Server = require('mongodb').Server;
```

对于使用额外类型（如 `Long` 或 `Binary`）的情况，你可以通过如下通过 `mongodb` 模块引用它们：

```javascript
var mongodb = require('mongodb');
var b = new mongodb.Binary(binary_data);
var l = new mongodb.Long(number_string);
```

## 连接并创建数据库

要连接到 MongoDB 服务器，你需要使用 `Server` 和 `Db` 类。你可以选择性使用 `Connection` 类来获取服务器监听的默认端口号。创建共享数据库对象的代码如下：

```javascript
var Db = require('mongodb').Db,
Connection = require('mongodb').Connection,
Server = require('mongodb').Server;
```

```javascript
var host = process.env['MONGO_NODE_DRIVER_HOST'] != null
? process.env['MONGO_NODE_DRIVER_HOST'] : 'localhost';
var port = process.env['MONGO_NODE_DRIVER_PORT'] != null
? process.env['MONGO_NODE_DRIVER_PORT'] : Connection.DEFAULT_PORT;
```

```javascript
var db = new Db('PhotoAlbums', new Server(host, port,
{ reconnect: true,
poolSize: 20 }), { w: 1 });
```

MongoDB 以及你使用的 `mongodb` 模块在处理写入和数据完整性方面非常灵活。传递给数据库构造函数的 `{ w: 1 }` 标志告诉它们在调用你提供的任何数据库操作回调函数之前，等待至少一次确认写入成功。你可以为具有复制功能的环境指定更高的数字，或者在不在乎写入何时完成的情况下指定 `0`。

你不需要为应用程序服务器的每个入站请求创建一个新的 `Db` 对象，也不需要担心许多人同时操作数据库服务器：`mongodb` 模块会为你处理连接池并同时管理多个请求。你可以通过调整传递给 `Server` 对象构造函数的 `poolSize` 参数的值，来选择与 MongoDB 保持多少个连接，如前文代码所示。

你想创建（或如果它已存在则使用）的数据库名称被传递给 `Db` 对象的构造函数。如果它不存在，则会被创建。

## 创建集合

如前所述，集合（collections）等同于关系型数据库系统中的表（tables），你通过调用 `Db` 对象上的 `collection` 或 `createCollection` 方法来创建它们。通过将 `{ safe: true }` 选项作为第二个参数，你可以精确控制它们在处理存在或不存在的集合时的工作方式（见表 8.1）。

### 表 8.1 创建集合

| 函数 | { safe: true } | 影响 |
| :--- | :--- | :--- |
| collection | 是 | 如果存在则打开集合；如果不存在则返回错误 |
| collection | 否 | 如果存在则打开集合；如果不存在在首次插入时创建集合 |
| createCollection | 是 | 如果不存在则创建集合；如果存在则返回错误 |
| createCollection | 否 | 如果不存在则创建集合；如果存在则返回现有集合 |

对于 `{ safe: true }` 选项，你的代码编写如下：

```javascript
db.collection("albums", { safe: true }, function (err, albums) {
  // ... 执行某些操作
});
```

然而，你最常用的用于创建或打开集合的代码仅仅是：

```javascript
db.collection("albums", function (err, albums) {
  if (err) {
    console.error(err);
    return;
  }
  // 现在可以使用 albums 来执行某些操作
});
```

## 向集合插入文档

要向集合中插入数据，你如下所示使用 `insert` 方法：

```javascript
var album = {
  id: "italy2012",
  name: "italy2012",
  title: "Spring Festival in Italy",
  date: "2012/02/15",
  description: "I went to Italy for Spring Festival."
};
```

```javascript
albums.insert(album, { safe: true }, function (err, inserted_doc) {
  if (err && err.name == "MongoError" && err.code == 11000) {
    console.log("此专辑已存在，抱歉。");
    return;
  } else if (err) {
    console.log("发生了某些错误。");
  }
  return;
  // 正常继续
});
```

你可以看到你正在为文档指定你自己的 `_id` 字段。如果你没有指定，MongoDB 会为你提供一个。如果已经存在具有该 `_id` 的文档，回调函数将带有错误被调用。你也可以看到再次传递了 `{ safe: true }` 选项，因为你想确保写入成功。如果你正在为分析类应用程序编写存储程序，且这里偶尔丢失某些值是可以接受的，那么你可以省略此选项。

你可以通过向 `insert` 函数传递一个数组来同时插入多个文档：

```javascript
var docs = [{ _id: "italy2012",
name: "italy2012",
title: "Spring Festival in Italy",
date: "2012/02/15",
description: "I went to Italy for Spring Festival." },
{ _id: "australia2010",
name: "australia2010",
title: "Vacation Down Under",
date: "2010/10/20",
description: "Visiting some friends in Oz!" },
{ _id: "japan2010",
name: "japan2010",
title: "Programming in Tokyo",
date: "2010/06/10",
description: "I worked in Tokyo" }];
albums.insert(docs, { safe: true }, function (err, inserted_doc) {
  if (err) {
    console.error(err);
  }
});
```

## 更新值

要更新文档，你使用集合上的 `update` 方法。第一个参数标识要更新的文档，第二个参数是包含新值的对象。

```javascript
db.collection("albums").update({id: "italy2012"}, {$set: {title: "New Title"}}, function (err, result) {
  if (err) {
    console.error(err);
  }
});
```

你还可以使用 `$set` 操作符一次更新多个字段。

## 删除文档

要从集合中删除文档，你使用 `remove` 方法。第一个参数标识要删除的文档。

```javascript
db.collection("albums").remove({id: "italy2012"}, function (err, result) {
  if (err) {
    console.error(err);
  }
});
```

你还可以通过向 `remove` 方法传递一个空对象来删除集合中的所有文档。

```javascript
db.collection("albums").remove({}, function (err, result) {
  if (err) {
    console.error(err);
  }
});
```

### 表 8.3 查找操作符

| 操作符 | 含义 |
| :--- | :--- |
| $ne | 不等于 |
| $lt | 小于 |
| $lte | 小于等于 |
| $gt | 大于 |
| $gte | 大于等于 |
| $in | 如果字段值是给定值数组中的某一个值，则匹配 |
| $nin | 如果字段值不是给定值数组中的任何一个值，则匹配 |
| $all | 如果给定字段是数组且包含给定值数组中的所有值，则匹配 |

## 查找 MongoDB 自动生成的 ID

我之前提到过，如果你在插入的文档中没有提供 `_id` 字段，MongoDB 会为你自动生成一个。这些自动生成的 `_id` 字段类型为 `ObjectID`，表示为 24 位的十六进制字符串。

问题在于，如果你使用这些字段，你无法简单地通过指定 ID 的字符串值来搜索它们。你需要将它们重新包装在 `ObjectID` 类构造函数中，如下所示：

```javascript
var ObjectID = require('mongodb').ObjectID;
var idString = '50da98dd138bc5c9000012';
collection.find({id: new ObjectID(idString)}, callback);
```

如果你尝试执行以下代码，将得不到任何匹配结果：

```javascript
collection.find({id: idString }, callback);
```

在本书所开发的应用程序中，你不会遇到这个问题，因为你将始终自己生成自己的 `_id` 字段。

## 精细化你的查找结果

要在你的页面上实现分页和排序，你需要操作或修改 `find` 操作的结果。`mongodb` 模块允许你通过在 `find` 操作上链式具有这些效果的额外函数调用来实现，这是在你调用生成游标的函数之前完成。

你将最常用的方法是 `skip`、`limit` 和 `sort`。第一个表示在开始返回任何结果之前应该忽略结果集中的多少文档，第二个控制在执行跳过操作后返回多少个文档，最后一个控制顺序和排序——欢迎你对多个字段进行排序。

因此，若要按日期升序获取专辑中的所有照片，你可以这样写：

```javascript
photos.find({ albumid: "italy2012" })
.sort({ date: 1 })   // 1 是升序，-1 是降序
.toArray(function (err, results));
```

要返回这些照片的第三页（假设每页20张照片），你会使用：

```javascript
photos.find({ albumid: "italy2012" })
.sort({ date: 1 })   // 1 是升序，-1 是降序
.skip(40)
.limit(20)
.toArray(function (err, results));
```

再次，在最后的 `toArray` 函数之前调用的任何内容都只是设置结果游标，查询直到最后一次函数调用时才会执行。

你可以将多个字段传递给 `sort` 函数以进行多个值的排序：

```javascript
collection.find()
.sort({ field1: -1, field2: 1 })
.toArray(callback);
```

## 更新你的照片专辑应用

通过对在 Node.js 中使用 MongoDB 基础知识的理解，你可以将你的照片共享应用程序更新到数据库，而不是仅仅使用简单的文件系统来存储专辑和照片信息。你仍然将实际图像文件留在硬盘上，但在真实的生产环境中，你会将它们放在某些存储服务器或内容分发网络 (CDN) 上。

## 编写底层操作

你首先为你的应用程序添加一个名为 `data/` 的新文件夹。你可以将底层操作放在该文件夹末尾。你还创建一个名为 `db.js` 的文件，其中将包含一些函数，帮助你处理和生成错误、验证参数以及执行常见的后端操作。这些任务都是简单的，你可以在 GitHub 上查看源码。

## 创建配置文件

在应用程序根目录下创建一个新文件 `local.config.js`，其中包含以下 JavaScript 代码：

```javascript
exports.config = {
  db_config: {
    host: "localhost", // 使用默认值
    poolSize: 5
  },
  static_content: "static/"
};
```

使用包含文件意味着所有配置选项都集中在一处，你可以轻松地更改它，而无需翻找代码。

## 获取数据库和集合

接下来，在 `data/` 中创建一个名为 `db.js` 的文件。在该文件中，你使用 `local.config.js` 文件中的信息创建应用程序所需的数据库连接和集合：

```javascript
var Db = require('mongodb').Db,
Connection = require('mongodb').Connection,
Server = require('mongodb').Server,
async = require('async'),
local = require('../config.js');

var host = local.db_config.host || 'localhost';
var port = local.db_config.port || Connection.DEFAULT_PORT;
var ps = local.db_config.poolSize || 5;

var db = new Db('PhotoAlbums',
  new Server(host, port,
  {
    auto_reconnect: true,
    poolSize: ps
  }));
```

现在，为了获取实际专辑和照片集合，你需要打开连接并确保它们存在。你通过向 `db.js` 中添加以下函数来实现这一点：

```javascript
exports.init = function (callback) {
  async.waterfall([
    // 1. 打开数据库连接
    function (cb) {
      db.open(cb);
    },
    // 2. 创建我们的专辑和照片集合
    // 如果它们已经存在，就很好
    function (opened_db, cb) {
      db.collection("albums", cb);
    },
    function (albums_coll, cb) {
      exports.albums = albums_coll;
      db.collection("photos", cb);
    },
    function (photos_coll, cb) {
      exports.photos = photos_coll;
      cb();
    }
    // 将结果传递回调用者，所以跳过结果
  ], callback);
};

exports.albums = null;
exports.photos = null;
```

你可以看到 `albums` 和 `photos` 现在是在 `db.js` 中导出的，因此人们可以在需要时通过以下方式获取它们：

```javascript
var db = require('./db.js');
```

最后，你需要确保在应用程序启动之前调用 `db.init` 函数，或者替换 `server.js` 中的调用：

```javascript
db.init(function (err, results) {
  if (err) {
    console.error("** 启动致命错误: ");
    console.error(err);
    process.exit(-1);
  }
});

app.listen(8080);
```

## 创建专辑

创建新专辑的底层代码变为：

```javascript
exports.create_album = function (data, callback) {
  var final_album;
  var write_succeeded = false;

  async.waterfall([
    function (cb) {
      try {
        backhelp.verify(data,
          [ "name", "title", "date", "description" ]);
        if (!backhelp.valid_filename(data.name))
          throw invalid_album_name();
      } catch (e) {
        cb(e);
      }
      cb(null, data);
    },
    // 在 mongo 中创建专辑
    function (album_data, cb) {
      var write = JSON.parse(JSON.stringify(album_data));
      write.id = album_data.name;
      db.albums.insert(write, { w: 1, safe: true }, cb);
    },
    // 确保文件夹存在
    function (new_album, cb) {
      write_succeeded = true;
      final_album = new_album[0];
      fs.mkdir(local.config.static_content
        + "albums/" + data.name, cb);
    },
    function (err, results) {
      if (err) {
        if (write_succeeded) {
          db.albums.remove({_id: data.name}, function () { });
          if (err instanceof Error && err.code == 11000)
            callback(backhelp.album_already_exists());
          else if (err instanceof Error && err.errno != undefined)
            callback(backhelp.file_error(err));
          else
            callback(err);
        }
      } else {
        callback(err, err ? null : final_album);
      }
    }
  ], callback);
};
```

在代码中，我们使用了一个技巧来克隆对象：

```javascript
var write = JSON.parse(JSON.stringify(album_data));
```

事实证明，快速序列化和反序列化一个对象是 JavaScript 中克隆对象最快的方法之一。我们在上面的代码中克隆对象是为了避免修改从本质上说“不属于我们”的对象。修改传递给函数的对象被认为是不礼貌的（或者直接是 Bug），因此我们在添加 `_id` 字段之前，恰好对其进行了克隆。请注意，`backhelp` 只是我们在 `data/` 文件夹中看到的、之前在 `helpers.js` 中看到的辅助函数的后端版本。

## 查找相册

通过名称加载相册是一个非常简单的操作：

```javascript
exports.album_by_name = function (name, callback) {
  db.albums.find({ _id: name }).toArray(function (err, results) {
    if (err) {
      callback(err);
      return;
    }

    if (results.length == 0) {
      callback(null, null);
    } else if (results.length == 1) {
      callback(null, results[0]);
    } else {
      console.error("More than one album named: " + name);
      console.error(results);
      callback(backutils.db_error());
    }
  });
});
```

你花费在错误处理和验证上的时间比实际查找相册的时间还要。

## 列出所有相册

同样，列出所有相也非常简单：

```javascript
exports.all_albums = function (sort_field, sort_desc, skip, count, callback) {
  var sort = {};
  sort[sort_field] = sort_desc ? -1 : 1;
  db.albums.find()
    .sort(sort)
    .limit(count)
    .skip(skip)
    .toArray(callback);
});
```

## 获取相册中的照片

在给相册中查找所有照片也轻而易举：

```javascript
exports.photos_for_album = function (album_name, pn, ps, callback) {
  var sort = { date: -1 };
  db.photos.find({ albumid: album_name })
    .skip(pn)
    .limit(ps)
    .sort(sort)
    .toArray(callback);
};
```

## 向相册添加照片

事实上，你唯一需要执行的另一个复杂操作就是向相册添加照片，这要麻烦一些，因为你必须添加一个步骤，将临时上传的文件复制到 `static/albums/` 文件夹中的最终存储位置：

```javascript
exports.add_photo = function (photo_data, path_to_photo, callback) {
  var final_photo;
  var base_fn = path.basename(path_to_photo).toLowerCase();
  async.waterfall([
    function (cb) {
      try {
        backhelp.verify(photo_data, "albumid", "description", "date");
        photo_data.filename = base_fn;
        if (!backhelp.valid_filename(photo_data.album)) {
          throw invalid_album_name();
        }
      } catch (e) {
        cb(e);
      }
      cb(null, photo_data);
    },
    // add the photo to the collection
    function (pd, cb) {
      pd.id = pd.albumid + "-" + pd.filename;
      db.photos.insert(pd, { w: 1, safe: true }, cb);
    },
    // now copy the temp file to static content
    function (new_photo, cb) {
      final_photo = new_photo[0];
      var save_path = local.config.static_content + "albums/"
        + photo_data.albumid + "/" + base_fn;
      backhelp.file_copy(path_to_photo, save_path, true, cb);
    },
    function (err, results) {
      if (err && err instanceof Error && err.errno != undefined) {
        callback(backhelp.file_error(err));
      } else
        callback(err, err ? null : final_photo);
    }
  ], callback);
};
```

## 为新的 JSON Server 修改 API

接下来，向 JSON 服务器添加以下两个 API 函数，以便方便创建相册并向其中添加照片：

```javascript
app.put('/v/albums.json', album_hdlr.create_album);
app.put('/v/albums/album_name/photos.json', album_hdlr.add_photo_to_album);
```

Express 的棒之处在于它让这个过程变得如此简单。当你添加这两行时，API 就扩展了新功能，你现在只需要更新相册处理器来支持这些新功能。

由于 API 现在支持放入数据（包括文件和 POST 体），你需要添加更多的中间件来支持这种能力。因此，在服务器顶部添加以下内容：

```javascript
app.use(express.logger('dev'));
app.use(express.bodyParser({ keepExtensions: true }));
```

在这里，你添加了一些日志输出，`bodyParser` 会在请求进入时填充 `req.body` 和 `req.files`。注意，你指示 `bodyParser` 中间件保留传入文件的扩展名。默认情况下，它会移除它们。

## 更新你的处理器

现在你已经有了相册和照片操作的数据库原语，你需要修改相册处理器以使用它们代替文件系统操作。

## 一些辅助类

首先创建几个辅助的小类。照片的类如下：

```javascript
function Photo (photo_data) {
  this.filename = photo_data.filename;
  this.date = photo_data.date;
  this.albumid = photo_data.albumid;
  this.description = photo_data.description;
  this._id = photo_data._id;
}

Photo.prototype._id = null;
Photo.prototype.filename = null;
Photo.prototype.date = null;
Photo.prototype.albumid = null;
Photo.prototype.description = null;
Photo.prototype.response_obj = function() {
  return {
    filename: this.filename,
    date: this.date,
    albumid: this.albumid,
    description: this.description
  };
};
```

### 列表 8.1 获取专辑中的所有照片

```javascript
Album.prototype.photos = function (pn, ps, callback) {
  if (this.album_photos != undefined) {
    callback(null, this.album_photos);
    return;
  }
  album_data.photos_for_album(
    this.name,
    pn, ps,
    function (err, results) {
      if (err) {
        callback(err);
        return;
      }
      var out = [];
      for (var i = 0; i < results.length; i++) {
        out.push(new Photo(results[i]));
      }
      this.album_photos = out;
      callback(null, this.album_photos);
    }
  );
};
```

```javascript
exports.photos_for_album = function(req, res) {
  var page_num = req.query.page ? req.query.page : 0;
  var page_size = req.query.page_size ? req.query.page_size : 1000;

  page_num = parseInt(page_num);
  page_size = parseInt(page_size);
  if (isNaN(page_num)) page_num = 0;
  if (isNaN(page_size)) page_size = 1000;

  var album;
  async.waterfall([function (cb) {
    // 获取获取专辑。
    if (!req.params || !req.params.album_name) {
      cb(helpers.no_such_album());
    } else {
      album_data.album_by_name(req.params.album_name, cb);
    }
  }, function (album_data, cb) {
    if (!album_data) {
      cb(helpers.no_such_album());
      return;
    }
    album = new Album(album_data);
    album.photos(page_num, page_size, cb);
  }, function (photos, cb) {
    var out = [];
    for (var i = 0; i < photos.length; i++) {
      out.push(photos[i].response_obj());
    }
    cb(null, out);
  }], function (err, results) {
    if (err) {
      helpers.send_failure(res, err);
      return;
    }
    if (!results) results = {};
    var out = {
      photos: results,
      album_data: album.response_obj()
    };
    helpers.send_success(res, out);
  });
};
```

## 添加照片

最后，你可以编写用于添加照片的 API 了；它在列表 8.2 中所示。此 API 还涉及向 Album 对象添加一个新方法。

### 列表 8.2 使用 API 添加照片

```javascript
Album.prototype.add_photo = function (data, path, callback) {
  album_data.add_photo(data, path, function (err, photo_data) {
    if (err) {
      callback(err);
    } else {
      var p = new Photo(photo_data);
      if (this.all_photos)
        this.all_photos.push(p);
      else
        this.all_photos = [ p ];
      callback(null, p);
    }
  });
}
```

```javascript
exports.add_photo_to_album = function (req, res) {
  var album;
  async.waterfall([
    function (cb) {
      if (!req.body) {
        cb(helpers.missing_data("POST data"));
      } else if (!req.files || !req.files.photo_file) {
        cb(helpers.missing_data("a file"));
      } else if (!helpers.is_image(req.files.photo_file.name)) {
        cb(helpers.not_image());
      } else {
        album_data.album_by_name(req.params.album_name, cb);
      }
    },
    function (album_data, cb) {
      if (!album_data) {
        cb(helpers.no_such_album());
        return;
      }
      album = new Album(album_data);
      req.body.filename = req.files.photo_file.name;
      album.add_photo(req.body, req.files.photo_file.path, cb);
    }
  ], function (err, p) {
    if (err) {
      helpers.send_failure(res, err);
      return;
    }
    var out = { photo: p.response_obj(), album_data: album.response_obj() };
    helpers.send_success(res, out);
  });
};
```

## 为应用程序添加一些新页面

JSON 服务器现在已完全修改为使用 MongoDB 来处理所有的专辑和照片存储工作。然而，你还没有一些页面让你通过 Web 界面创建新专辑或向专辑添加新照片。让我们现在来修复这个问题。

## 定义页面的 URL

在这里，你可以在 `/pages/admin/add_album` 和 `/pages/admin/add_photo` 中放置想要创建的两个新页面。幸运的是，你不需要修改 URL。

## 创建专辑

用于创建页面的代码是简单易见的，它不需要通过服务器加载一些复杂的 JavaScript 文件。

### 8.3 add_album.js

```javascript
$(function() {
  var tmpl, // 主模板
  tdata = {}; // JSON 对象

  // 初始化页面
  var initPage = function() {
    // 加载 HTML 模板
    $.get("/templates/add_album.html", function(d) {
      tmpl = d;
    });

    // AJAX 调用完成后解析模板
    // 用变量替换 mustache 标签
    $(document).ajaxStop(function () {
      var renderedPage = Mustache.to_html(tmpl, tdata);
      $("body").html(renderedPage);
    });
  }
});
```

### 8.4 add_album.html

```html
<form name="create_album" enctype="multipart/form-data" method="POST" action="/v1/albums">
  <h2>创建专辑</h2>
  <dl>
    <dt>专辑名称</dt>
    <dd><input type='text' name='name' size='30'></dd>
    <dt>标题</dt>
    <dd><input type='text' name='title' size='30'></dd>
    <dt>描述</dt>
    <dd><textarea rows="5" cols="30" name="description"></textarea></dd>
  </dl>
  <input type="hidden" id="date" name="date" value=""/>
  <input type="button" id="submit_button" value="上传">
</form>

<script type="text/javascript">
$("input#submit_button").click(function (e) {
  var m = new Date();
  var dateString = m.getUTCFullYear() + "/" +
    (m.getUTCMonth() + 1).toString().slice(-2) + "/" +
    m.getUTCDate().toString().slice(-2);

  $("#date").val(dateString);

  var json = "{" +
     "\"name\":\"" + $("name").val() +
    "\",\"title\":\"" + $("#title").val() +
    "\",\"description\":\"" + $("#description").val() +
    "\"}";

  $.ajax({
    type: "PUT",
    url: "/v1/albums.json",
    contentType: "application/json", // 请求负载类型
    dataType: "application/json", // 我们想要的返回
    data: json,
    success: function (resp) {
      alert("成功！正在进入专辑");
      window.location = "/pages/album/" + $("name").val();
    }
  });
});
</script>
```

## 添加照片

要向专辑添加照片，你需要编写稍微复杂的代码。在引导页面中，你需要一个专辑列表，以便用户可以选择将照片添加到哪个专辑。此代码在列表 8.5 中所示。

### 8.5 add_photo.js

```javascript
$(function() {
  var tmpl, // 主模板 HTML
  tdata = {}; // 用于模板的 JSON 对象

  // 初始化页面
  var initPage = function() {
    // 加载 HTML 模板
    $.get("/templates/admin/add_photos.html", function(d) {
      tmpl = d;
    });

    // 获取服务器数据并初始化页面
    $.getJSON("/v1/albums.json", function (d) {
      $.extend(tdata, d.data);
    });

    // AJAX 调用完成后解析模板
    // 用变量替换 mustache 标签
    $(document).ajaxStop(function () {
      var renderedPage = Mustache.to_html(tmpl, tdata);
      $("body").html(renderedPage);
    });
  }
});
```

最后，我留给你查看第8章 GitHub 源码中的 `create_album/` 文件夹，获取显示表单并向服务器实际上传的 HTML 页面源码 (admin_add_photo.html)。此文件所做的主要工作是对 XMLHttpRequest 对象的 FormData 扩展，以允许 Ajax 文件上传，如下：

```javascript
var oReq = new XMLHttpRequest();
var url = "/v1/albums/" + $("#albumid").val() + "/photos.json";
oReq.open("PUT", url, true);
oReq.onload = function(oEvent) {
  if (oReq.status == 200) {
    oOutput.innerHTML = "\nUploaded! Continue adding a <a href=\/pages/album/" + $("#albumid").val() + ">View Album</a>";
  } else {
    oOutput.innerHTML = "\nError " + oReq.status + " occurred uploading your file.<br />";
  }
};
oReq.send(oData);
```

`FormData` 非常强大且出色，但在 10 及以下版本的 Internet Explorer (IE) 中不支持。Firefox、Chrome 和 Safari 都已经支持它很长时间了。如果你需要支持旧版本的 IE 浏览器，你需要查看其他上传文件的方法，例如 Flash 或传统的 HTML 表单。

# 回顾应用结构

应用程序变得稍微复杂了一点；值得花几秒钟再次回顾一下你是如何构建它的。你已经将所有静态内容移动到了 `static/` 文件夹并将代码移动到了 `app/` 文件夹，因此你现在拥有以下基本布局：

`static/` 文件夹包含以下子文件夹：

- albums/—所有相册的内容及其图片文件
- content/—包含渲染页面模板所需的样式表和 JavaScript 引导文件
- templates/—用于在客户端浏览器中渲染页面的 HTML 模板

在 `app/` 文件夹中，你有：

- /—包含核心服务器脚本和 `package.json` 文件
- data/—所有与处理后端数据存储相关的代码和类
- handlers/—包含负责处理入站请求的类

从现在开始起，你应用程序的所有版本都将使用这种结构。

# 总结

你现在不仅拥有一个完全更新的相册应用程序版本（它使用 MongoDB 作为相册和照片的数据存储），你的 Web 应用程序中还有几个有趣的页面，用于创建相册和向服务器上传照片。

唯一的问题是任何人都可以查看并使用这些页面和 API 来操作相册和照片。因此你接下来需要将注意力放在添加用户上，并要求在进行这些更改之前登录。

# 数据库 II：SQL (MySQL)

尽管 NoSQL 数据库正迅速流行，但仍有很多充分的理由继续使用关系型数据库，它们仍然如既往一样受欢迎，特别是两个最常见的开源变体 MySQL 和 PostgreSQL。好消息是，Node.js 的异步特性与在 Web 应用程序中注册这些数据库衔合得非常完美，而且对于大多数此类数据库都有良好的 npm 模块支持。

在本章中，我将介绍如何使用 npm 中的 `mysql` 模块在 Node 中使用 MySQL。由于你已经在前面的章节中学习了如何将相册和照片放入数据库，你现在可以将注意力转移到在应用程序中注册用户，并要求他们在创建相册或添加照片之前登录。

即使你不计划使用 MySQL 这样的传统关系型数据库，阅读完本章也是值得的，因为我引入了 express 中的几个重要功能，并谈到了资源池（resource pooling），这是一种控制和限制珍贵系统资源使用的方法。你还更新了相册示例，使相册和照片能够与 MySQL 工作。

## 准备工作

在开始在 Node.js 中玩 MySQL 之前，你需要做两件事：确保已安装 MySQL，并安装 `mysql` npm 模块。

## 安装 MySQL

如果你还没有在你的开发机器上安装 MySQL，请访问 dev.mysql.com/downloads/mysql 并下载最适合你机器的社区服务器版本。对于 Windows 和 Mac OS X，你可以找到可用的安装程序，而对于 Linux 和其他 Unix 系统，你可以将 `.tar.gz` 压缩包解压到你喜欢的位置（通常是 `/usr/local/mysql`）。

如果你正在运行 Windows 或 Mac OS X 的安装程序，它们会为你处理好一切；而对于仅二进制发行版，你必须读取 `INSTALL-BINARY` 文件并按照其中的指令使 MySQL 完全安装并运行。完成后，你应该能够启动一个新的命令提示符或运行 `mysql` 命令：

```
Kimidori:Learning Node marcw$ /usr/local/mysql/bin/mysql -u root
Welcome to the MySQL monitor. Commands end with ; or \
Your MySQL connection id is 1
Server version: 5.5.29 MySQL Community Server (GPL)
```

## 添加 npm 中的 mysql 模块

要为 Node.js 安装 `mysql` 模块，你可以修改 `package.json` 并添加以下依赖：

```json
"dependencies": {
  "async": "0.1.x",
  "mysql": "2.x"
}
```



你应该会在你文件夹的 `node_modules/` 下看到 `mysql/`。注意，`mysql` 模块的 2.x 系列相比 0.x 系列是一个巨大的改进和偏离。Node.js 最困难的部分之一是它在不断开发和改进；事情仍在发生很大变化。你在书中使用 2.x 系列是因为它比之前的要健壮得多。

## 为数据库创建模式 (Schema)

在与 MySQL 工作时，你需要为应用程序创建一个数据库模式，并将其放在 `schema.sql` 中。第一部分是创建一个以 UTF-8 为默认字符集和排序规则的数据库，如下：

```sql
DROP DATABASE IF EXISTS PhotoAlbums;
```

```sql
CREATE DATABASE PhotoAlbums
  DEFAULT CHARACTER SET utf8
  DEFAULT COLLATE utf8_general_ci;
```

```sql
USE PhotoAlbums;
```

## 数据库操作

对于你来说，大多数 MySQL 的工作将限于连接服务器和执行查询。这足够你运行简单的应用程序了。

## 连接

要连接服务器，你通过 `mysql` 模块创建一个连接，然后如下所示调用：

```javascript
dbclient = mysql.createConnection({
  host: "localhost",
  user: "root",
  password: "",
  database: "PhotoAlbums"
});

dbclient.connect(function (err) { });
```

如果连接失败，你会得到一个错误。如果成功，你就可以使用该对象执行查询。在完成所有数据库工作后，你应该通过调用 `end` 方法关闭连接。

## 添加查询

连接到数据库后，你可以使用 `query` 方法开始执行查询，向其传递 SQL 语句：

```javascript
dbclient.query('SELECT * FROM Albums', function (err, results, fields) {});
```

如果查询成功，传递给回调的 `results` 参数包含了你请求的数据，第三个参数 `fields` 用于你有额外信息的情况（通常在你没有此类信息时）。对于 SELECT 语句，第二个参数是查询行的数组：

```javascript
dbclient.query('SELECT * FROM Albums', function (err, rows) {
  for (var i = 0; i < rows.length; i++) {
    console.log(' -> Album: " + rows[i].name + ' "' + rows[i].date + ' ');
  }
});
```

如果你正在使用 INSERT、UPDATE 或 DELETE，从 `query` 返回的结果看起来更类似于下面：

```json
{ fieldCount: 0,
affectedRows: 0,
insertId: 0,
serverStatus: 2,
warningCount: 0,
message: '',
changedRows: 0 }
```

你可以通过查看 `affectedRows` 属性来确保受影响的行数符合预期，或者可以通过 `insertId` 属性获取最后插入行的自动生成 ID。

而这基本上就是在 Node.js 中使用 MySQL 的全部内容了。让我们让它严肃地用起来吧！

## 在应用程序中添加身份验证

在前面的章节中，我向你展示了如何将应用程序中相册和照片的存储转换为使用数据库，但你面临一个问题：添加相册和添加照片的页面允许任何人匿名访问。你可以将你的应用程序更改为

## 在应用程序中添加身份验证

- 允许新用户注册应用程序。

- 在使用“添加专辑”或“照片”页面之前，要求用户必须已登录并注册。

## 更新 API 以支持用户

为了支持新的用户子系统，你需要为 API 添加几条新路由：

```
app.put('/v1/users.json', user_hdl.register);
app.post('/service/login', user_hdl.login);
```

第一个是 CRUD 方法（参考第 7 章《使用 Express 构建 Web 应用程序》中带有“API 设计”章节的方法），用于通过 API 创建用户。第二个是关于如何支持应用程序 Web 浏览器版本的登录和身份验证。我将在稍后的“创建用户处理程序”部分展示这两种方法的实现方式。

## 检查核心用户数据操作

要获取数据库连接，请为你的应用程序创建一个 `data/` 文件夹，并且除了一个包含简单错误处理帮助的 `backend_helpers.js` 文件外，再放入一个名为 `db.js` 的文件。该文件如列表 9.1 所示。实际上，它提供了一个函数，用于根据你在第 8 章《数据库 I：NoSQL (MongoDB)》中看到的 `local.config.js` 文件提供的连接信息来连接 MySQL 数据库。

> 列表 9.1 db.js

```javascript
var mysql = require('mysql');
local = require('../local.config.js');

exports.db = function (callback) {

  conn_props = local.config.db;
  var c = mysql.createConnection({
    host: conn_props.host,
    user: conn_props.user,
    password: conn_props.password,
    database: conn_props.database
  });

  callback(null, c);
}
```

当你拥有连接后，负责通过调用 `end` 方法关闭它以释放消耗的资源。有了这个文件，你可以在 `data/user.js` 中开始为前面的新 API 实现后端。

第 9 章数据库 II：SQL (MySQL)

## 创建用户

在数据库中注册新用户的代码如下：

```javascript
exports.register = function (email, display_name, password, callback) {
  var dbc;
  var userid;
  async.waterfall(
    // 验证参数
    function (cb) {
      if (!email || email.indexOf("@") == -1)
        cb(backend.missing_data("email"));
      else if (!display_name)
        cb(backend.missing_data("display_name"));
      else if (!password)
        cb(backend.missing_data("password"));
      else
        cb(null);
    },
    function (cb) {
      db.db(cb);
    },
    function (dbclient, cb) {
      dbc = dbclient;
      bcrypt.hash(password, 10, cb);
    },
    function (hash, cb) {
      userid = uuid();
      dbc.query(
        "INSERT INTO Users VALUES (?, ?, ?, ?, ?, UNIX_TIMESTAMP(), NULL, 0)",
        [ userid, display_name, hash ],
        cb);
    },
    function (results, fields, cb) {
      exports.user_by_userid(userid, cb);
    },
    function (err, user_data) {
      if (dbc) dbc.end();
      if (err) {
        if (err.code == 'ER_DUP_KEYNAME'
          || err.code == 'ER_EXISTS'
          || err.code == 'ER_DUP_ENTRY')
          callback(backhelp.user_already_registered);
      }
    }
  );
```

```javascript
else
    callback (err);
} else {
    callback(null, user_data);
}
));
```

该代码执行了以下操作：

1. 它验证传入的参数，特别是确保电子邮件地址有效。如果你愿意，甚至可以做得更严格，要求通过向该地址发送链接来激活账户。

2. 它获取数据库连接。

3. 它使用 `bcrypt` 模块对密码进行哈希。Bcrypt 是一种缓慢的密码生成方法，使得对其进行暴力破解变得极其困难。

4. 你为用户生成一个 UUID。你之后可以在 API 中使用它来识别用户。ID 比简单的整数 ID 更好，因为它们更难猜测且没有明显的顺序。

5. 你执行查询在数据库中注册用户，最后请求数据库将刚创建的用户返回给调用者。

你在此代码使用了两个新模块：`bcrypt`（用于密码加密）和 `node-uuid`（用于生成用户标识符的 GUID）。因此，你更新了 `package.json` 文件以包含以下依赖：

```json
"dependencies": {
  "express": "3.x",
  "async": "0.1.x",
  "mysql": "2.x",
  "bcrypt": "0.x",
  "node-uuid": "1.x"
}
```

还要注意，我们将账户创建日期存储为 `BIGINT` 而不是普通的 MySQL `DATETIME` 字段。我发现，因为 JavaScript 在日期和时间上到处使用时间戳，因此在数据库中存储和操作它们也会容易得多。幸运的是，MySQL 提供了几个函数来帮助处理这些日期。

## 获取用户（通过电子邮件）

现在你有了一种根据电子邮件获取用户的方法。

```javascript
function user_by_field(field, value, callback) {
  var dbc;
  async.waterfall([
    function (cb) {
      db.db(cb);
    },
    function (dbclient, cb) {
      dbc = dbclient;
      dbc.query(
        "SELECT * FROM Users WHERE " + field + " = ?",
        [ value ],
        cb);
    },
    function (rows, fields, cb) {
      if (rows.length == 0) {
        callback(backend.user_not_found);
      } else {
        callback(null, rows[0]);
      }
    },
    function (err, user_data) {
      if (dbc) dbc.end();
      callback(err, user_data);
    }
  ]);
}
```

## 在应用程序中添加身份验证

## 更新 Express 应用程序

服务器记住用户是否登录的主要方法是 *session cookies*。浏览器每次请求都会保存 cookie，因此你使用 session。为了设置此功能，在 `server.js` 顶部添加以下行：

```javascript
app.use(express.cookieParser());
app.use(express.session({
  secret: "FLUFFY BUNIES",
  maxAge: 86400000,
  store: new express.session.MemoryStore()
}));
```

如果用户已登录，你会设置 `req.session.logged_in = true` 并设置 `req.session.email_address` 为一个值。如果用户未登录，这些值是未定义的。

为了确保用户在使用上一章创建的管理页面之前已登录，你可以引入你尚未见过的 Express 功能：将你的中间件注入路由决策中。

通常，你会这样路由 URL：

```
app.get(URL, HANDLER_FUNCTION);
```

但你可以在 URL 和处理函数之间插入任意数量的中间件函数。它们按照列出的顺序被调用。它们接收三个参数：`req`、`res` 和 `next`。如果它们想处理请求，可以处理并发送响应（`res.end`）。如果它们不想，只需调用 `next()` 函数。

因此，为了要求用户在管理页面时登录，将页面路由更改如下：

```javascript
app.get('/pages/:page_name', requirePageLogin, page_hdrl.generate());
app.get('/pages/:page_name/sub_page', requirePageLogin, page_hdrl.generate());
```

`requirePageLogin` 函数检查用户是否请求了一个需要身份验证的页面。如果是，通过调用它检查用户是否已登录。如果是，则通过调用 `next()` 允许继续处理。如果没有登录，它会拦截 URL 并用户重定向回登录页面：

```javascript
function requirePageLogin(req, res, next) {
  if (req.params && req.params.page_name == 'admin') {
    if (req.session && req.session.logged_in) {
      next();
    } else {
      res.redirect("/pages/login");
    }
  } else {
    next();
  }
}
```

# 第 9 章 数据库 II：SQL (MySQL)

## 创建用户处理器

为了支持账户管理，你可以在 `handlers/users.js` 中创建一个新的用户处理器。就像你之前处理相册和照片一样，你创建一个新的 `User` 类，这将帮助你封装用户，并允许实现一个 `response_obj` 方法来过滤掉不想返回的内容：

```javascript
function User(user_data) {
  this.uuid = user_data['user_uuid'];
  this.email_address = user_data['email_address'];
  this.display_name = user_data['display_name'];
  this.password = user_data['password'];
  this.first_seen_date = user_data['first_seen_date'];
  this.last_modified_date = user_data['last_modified_date'];
  this.deleted = user_data['deleted'];
}
```

```javascript
User.prototype.uuid = null;
User.prototype.email_address = null;
User.prototype.display_name = null;
User.prototype.password = null;
User.prototype.first_seen_date = null;
User.prototype.last_modified_date = null;
User.prototype.deleted = false;
User.prototype.check_password = function (pw, callback) {
  bcrypt.compare(pw, this.password, callback);
};
User.prototype.response_obj = function () {
  return {
    uuid: this.uuid,
    email_address: this.email_address,
    display_name: this.display_name,
    first_seen_date: this.first_seen_date,
    last_modified_date: this.last_modified_date
  };
}
```

## 创建新用户

接下来，你实现创建用户的函数。它基本上执行以下操作：

- 1. 检查传入的数据以确保其有效性。

- 2. 在后端创建用户账户并获取原始数据。

- 3. 将用户标记为已登录。

- 4. 将新创建的用户对象返回给调用者。

## 为应用程序添加身份验证

这个 `exports.register` 函数看起来如下：

```javascript
exports.register = function (req, res) {
async.waterfall({
  function (cb) {
    var em = req.body.email_address;
    if (!em || em.indexOf("@") == -1) {
      cb(helpers.invalid_email_address(cb));
    } else if (!req.body.display_name)
      cb(helpers.missing_data("display_name"));
    } else if (!req.body.password)
      cb(helpers.missing_data("password"));
    } else
      cb(null);
  },
  function (cb) {
    user_data.register(
      req.body.email_address,
      req.body.display_name,
      req.body.password,
      cb);
  },
  function (user_data, cb) {
    req.session.logged_in = true;
    req.session.logged_in_email_address = req.body.email_address;
    req.session.logged_in_date = new Date();
    cb(null, user_data);
  }
}, (err, user_data) {
  if (err) {
    helpers.send_failure(res, err);
  } else {
    var u = new User(user_data);
    helpers.send_success(res, {user: u.response_obj()});
  }
}
});
```

## 用户登录

要让用户登录系统，你需要执行以下操作：

- 1. 根据指定的电子邮件地址获取用户对象（如果该邮箱不存在则抛出错误）。

- 2. 使用 `bcrypt` 模块比较密码。

- 3. 如果密码匹配，设置会话变量将用户标记为已登录。否则，将身份验证标记为失败。

代码如下：

```javascript
exports.login = function(req, res) {
  async.waterfall([
    function (cb) {
      var em = req.body.email_address;
      if (!em || em.indexOf('@') == -1)
        cb(helpers.invalid_email_address());
      else if (req.session && req.session.logged_in_email_address
        == em.toLowerCase())
        cb(helpers.error("already_logged_in", ""));
      else if (!req.body.password)
        cb(helpers.missing_data("password"));
      else
        user_data.user_by_email(req.body.email_address, cb); // 1.
    },
    function (user_data, cb) {
      var u = new User(user_data);
      u.check_password(req.body.password, cb); // 2.
    },
    function (auth, ok, cb) {
      if (!auth_ok) {
        cb(helpers.auth_failed());
        return;
      }
      req.session.logged_in_email_address = req.body.email_address;
      req.session.logged_in_date = new Date();
      cb(null);
    }
  ],
  function (err, results) {
    if (err || err.message == "already_logged_in")
      helpers.send_success(res, {logged_in: true});
    else
      helpers.send_failure(res, err);
  }
});
```

## 测试登录状态

测试用户是否已登录，只需查看是否设置了相应的会话变量：

```javascript
exports.logged_in = function (req, res) {
  var li = (req.session && req.session.logged_in_email_address);
  helpers.send_success(res, {logged_in: li});
}
```

## 注销

最后，注销只需清除会话数据，用户不再被视为已登录：

```javascript
exports.logout = function (req, res) {
  req.session = null;
  helpers.send_success(res, {logged_out: true});
}
```

## 创建登录和注册页面

对于新用户，你的应用程序中有两个页面：登录页面注册页面。它们的 JavaScript 初始化方式非常标准：

```javascript
function(){
  var tmpl,
  tdata = {}; // 用于填充模板的对象

  // 初始化页面
  var initPage = function() {
    // 加载 HTML 模板
    $.get("templates/login.html", function(d){
      tmpl = d;
    });

    // 当 AJAX 调用完成时，解析模板并替换标签
    $(document).ready(function () {
      var renderedPage = Mustache.render(tmpl, tdata);
      $('body').html(renderedPage);
    });
  }
}
```

注册页面的 HTML 见列表 9.2。除了显示表单，它还有一些 JavaScript 来确保用户填写了字段，验证两个密码是否匹配，然后数据提交给后端。如果登录成功，重定向回首页；否则，显示错误让用户再次尝试。

### 列表 9.2 注册页面模板 (register.html)

```html
<div style="float: right"><a href="/pages/login">Login</a></div>
<form name="register" id="register">
  <div id="error" class="error"></div>
  <dl>
    <dt>邮箱:</dt>
    <dd><input type="text" size="30" id="email_address" name="email_address"/></dd>
    <dt>显示名称:</dt>
    <dd><input type="text" size="30" id="display_name" name="display_name"/></dd>
    <dt>密码:</dt>
    <dd><input type="password" size="30" id="password" name="password"/></dd>
    <dt>确认:</dt>
    <dd><input type="password" size="30" id="password2" name="password2"/></dd>
    <dd><input type="submit" size="30" id="submit" value="Register"/></dd>
  </dl>
</form>
```

```javascript
<script type="text/javascript">
$(document).ready(function () {
  if (window.location.href.match(/fail/) != null) {
    $("#error").html("创建账户失败。");
  }
  $("#formregister").submit(function (e) {
    if (!("input#email_address").val() 
        || !("input#display_name").val() 
        || !("input#password").val() 
        || !("input#password2").val()) {
      $("#error").html("你需要输入邮箱和密码。");
    } else if ($("input#password2").val() != $("input#password").val()) {
      $("#error").html("密码不匹配。");
    } else {
      var info = {
        email: $("input#email_address").val(),
        display_name: $("input#display_name").val(),
        password: $("input#password").val()
      };

      $.ajax({
        type: "PUT",
        url: "/service/users.json",
        data: JSON.stringify(info),
        contentType: "application/json; charset=utf-8",
        success: function (data) {
          window.location = "/pages/admin/home";
        },
        error: function (error) {
          var ext = window.location.href.match(/fail/) ? "" : "fail";
          window.location = window.location + ext;
          return false;
        }
      });
    }
  });
});
</script>
```

最后，登录页的代码见列表 9.3。它与注册页面非常相似：显示了表单的 HTML，并有一些 JavaScript 来处理数据并发送到服务器。

### 列表 9.3 登录页面模板 (login.html)

```html
<div style="float: right;"><a href="/pages/register">Register</a></div>
<form name="login" id="login">
  <div id="error" class="error"></div>
  <dl>
    <dt>邮箱:</dt>
    <dd><input type="text" size="30" id="email_address" name="email_address"/></dd>
    <dt>密码:</dt>
    <dd><input type="password" size="30" id="password" name="password"/></dd>
    <dd><input type="submit" size="30" id="submit" value="Login"/></dd>
  </dl>
</form>
```

```javascript
dataType: "json",
uccess: function (data) {
  window.location = "/pages/admin/home";
},
error: function () {
  var ext = window.location.href.match(/(\w+)$/) ? "" : "?fail";
  window.location = window.location + ext;
  return false;
}
});
return false;
});
<script>
```

有了这些新文件（data/user.js 和 handlers/users.js，login.js 和 login.html，register.js 和 register.html），你已经为你的 浏览器前端拥有了一个完整的登录系统。

## 资源池

在上一节中，你已经看到 Node.js 的 MongoDB 驱动程序管理了它自己的连接集合，或者说连接“池”。`mysql` 模块并没有替你做这件事，因此你必须自己设计一套连接池机制。幸运的是，这件事情非常简单，你完全不需要需要担心该模块没有实现这一功能。

在 npm 中，一个名为 `generic-pool` 的模块允许对……任何东西进行池化。要使用它，你需要创建一个池，指定要创建的项数量的上限，并提供一个函数在池中创建对象的新实例。然后，当从池中获取一个项时，你调用 `acquire` 函数，它会等待直到池可供你使用。当你完成后，调用 `release` 函数将对象返回池中。

让我们来看看实际操作。

## 开始使用

将 `generic-pool` 添加到 `package.json` 的依赖中：

```json
"dependencies": {
  "express": "3.x",
  "async": "0.1.x",
  "generic-pool": "2.x",
  "mysql": "2.x",
  "bcrypt": "0.x",
  "node-uuid": "1.x"
}
```

要在文件中包含它，你可以按如下方式引入它：

```javascript
var pool = require('generic-pool');
```

要创建一个池，你需要使用一些配置信息创建一个池类的新实例，即你想要的池中项的数量，以及创建新对象的函数：

```javascript
conn_props = local.config.db_config;
mysql_pool = Pool({
  name: 'mysql',
  create: function (callback) {
    var c = mysql.create({
      host: conn_props.host,
      user: conn_props.user,
      password: conn_props.password,
      database: conn_props.database
    });
    callback(null, c);
  },
  destroy: function (client) {
    client.end();
  },
  max: conn_props.pooled_connections,
  idleTimeoutMillis: conn_props.idle_timeout_millis,
  log: false
});
```

## 使用连接

在代码中，每当你需要到 MySQL 服务器的连接时，与其创建一个新的，你只需要让池来为你管理一切。`acquire` 函数会阻塞，直到有连接可供你使用。`db.js` 中之前的 `db` 函数变为：

```javascript
exports.db = function (callback) {
  mysql_pool.acquire(callback);
});
```

当你完成连接的使用后，可以如下所示将其释放回连接池：

```javascript
conn.release();
```

任何其他等待连接的人都会立即获得它。

## API 身份验证

现在，你可能正感到非常自豪，因为你的应用程序在创建专辑或向专辑中添加照片之前正确地检查了你已登录，但你仍然面临一个主要的安全问题：API 本身完全不安全。你仍然可以在不受挑战的情况下运行以下命令：

```bash
curl -X PUT -H "Content-Type: application/json" \
  -d '{"name": "hk2012", "title": "moo", "description": "cow", "date": "2012-12-28"}' \
  http://localhost:8080/v1/albums.json
```

如果一个系统的某些部分是安全的而其他部分完全开放，那么这个系统就不那么令人深刻！你现在就可以修复这个问题。

你可以创建一个系统，通过它：

- 浏览器前端使用登录和注册页面和服务来管理对服务器的访问。

- API 用户将使用 HTTP Basic 认证，在请务时传递用户名和密码以验证受限 API 的身份。

## HTTP Basic 认证：它安全吗？

正如我在本章解释的样，HTTP Basic 认证是一种相对简单的安全形式：

客户端在每次请务时都会向服务器发送一个带有 base64 编码的用户名和密码的头部，服务器在处理之前对其进行验证。由于 base64 编码不是加密形式，它等同于在互联网上传递明文用户名和密码。所以你可能会问：这从根本上说是不安全的吗？

答案是，很大程度上是。网站的大多数安全部分都是加密并使用 SSL/HTTPS 通过网络的。这种在客户端和服务器之间发送加密流量的方法非常安全，所以你绝对应该在你的服务器上设置它。

其他人认为浏览器会记住 Basic Auth 的用户名和密码，这可能是不安全的。这个论点是有效的，这也是为什么我们只只对 API 服务器使用 Basic Auth。对于基于浏览器的应用程序，你应该坚持使用登录页面和 Session Cookie。

所以，尽管 HTTP Basic 认证可能是不安全的，但只要稍加准备和预防措施，没有理由它不能成为你 REST API 服务器上可靠的生产级安全系统。

# 总结

（前文衔接）……几秒钟，以进一步遏制暴力攻击。至此，你现在为你的照片共享应用有了一个相当安全的 Web 和 API 服务器。

为了真正确保其安全，你应该确保任何发送给你的需要密码的请求都通过 HTTPS 安全，这样就不会人能够使用数据包嗅探器查看传输过程中的任何密码。我将在第 10 章“部署与开发”中详细讨论 HTTPS。

# 总结

在这一章中，我向你介绍了两个新概念：在你的 Node 应用中使用 MySQL 数据库，以及在你的 Web 应用和 API 服务器中添加用户身份验证。针对本章，我已经在 GitHub 树中更新了 MongoDB 版本的应用程序，添加了用户身份验证子系统，因此欢迎你探索那里是如何操作的。通过创建两个并行的认证系统，你能够为浏览器应用程序创建一个良好的用户体验，同时让 API 用户仍然享受到 JSON API 的完整简单性和强大功能。

在本书第三部分的结束语中，你学习了如何向照片共享应用中添加一些强大的技术，包括 express 和数据库，并创建了一个功能齐全（尽管很基础）的项目，你可以在此基础上进行构建。在本书的最后一部分，我将涵盖迄为止在书中略带带过的细节。首先，在第 10 章，你将学习如何部署你的应用程序。

## 第四部分

## 充分利用 Node.js

- 10 部署与开发 213

- 11 命令行编程 233

- 12 测试 253

## 10

## 部署与开发

当你已经练就了构建非平凡 Node.js 应用的能力后，你现在可以将注意力转向这些应用部署和开发的其他额外主题。在本章中，你将开始查看人们在生产服务器上部署和运行 Node.js 应用的各种方式，涵盖了 UNIX/Mac 和 Windows 选项。你还将看到如何利用多处理器机器，尽管 Node.js 是一个单线程平台。

然后你将转向查看如何在服务器上添加对虚拟主机的支持，以及使用 SSL/HTTPS 支持保护你的应用程序。最后，你将快速查看当人们同时使用 Windows 和 UNIX/Mac 机器开发 Node 应用时，跨平台开发中的一些问题。

## 部署

到目前为止，运行 Node.js 应用时，你一直通过命令行使用以下命令：

```
node script_name.js
```

这种方法在开发阶段效果非常好。然而，对于将应用程序部署到生产服务器，你可能希望添加一层额外的可靠性层，以在它们崩溃时提供帮助。尽管你当然会努力避免服务器出现错误，但某些错误最终会溜进来，因此你希望服务器尽可能地从此类问题中恢复。

现在让我们来看一些选项。

## 章节：部署与开发

## 端口号

在本书的大部分内容中，你的示例应用使用了非常高的端口号，最常用的是 8080。这是因为某些操作系统（特别是 UNIX/Mac OS X 系统）1024 以下的端口号需要超级用户权限。因此，对于简单的调试和测试，8080 是 Web 流量常用端口 80 的绝佳替代方案。

然而，当你部署生产应用时，你通常希望运行在端口 80，因为这是 Web 浏览器的默认端口。要实现这一点，你需要以超级用户身份运行脚本。实现此点的有两种方法：

- 1. 以超级用户身份登录系统并以此运行程序。

- 2. 使用 `sudo` 命令，它在实际执行时将进程提升到超级用户权限。

在这两种策略中，我经常使用后一种。

## 级别：基础

在最基础的层，你只需要使用一个无限循来运行你的脚本。这个循环会在 node 进程崩溃时只需重新启动它。在运行 bash 的 UNIX 和 Mac 计算机上，脚本可以简单到：

```bash
#!/bin/bash
while true
	node script_name.js
done
```

在 Windows 上，你可以使用批处理文件来为你完成工作，如下所示（将其保存为 `run_script.bat` 或类似文件并运行它）：

```batch
: loop
node script_name.js
goto loop
echo
```

这些脚本确保了当你的 Node 进程崩溃或意外终止时，它总能被重启。

你实际上可以更进一步，使用名为 `tee` 的命令将 node 进程的输出写入日志文件。你通常在命令行中使用 `|` 运算符将进程的输出通过管道到 `tee` 命令，然后它会在写入指定的日志文件的同时，在标准输出上重新打印输出，如下：

```bash
node hello_world.js | tee - /var/server/logs/important.log
```

`-a` 标志告诉你可以追加到指定的日志文件，而不是简单的覆盖它。因此，你可以通过如下运行脚本来进一步改进你的部署：

```bash
bash ./run_script.sh | tee - /var/server/logs/important.log
```

或者，在 Windows 上，你可以使用以下：

```batch
run_script.bat | tee -a /var/server/logs/important.log
```

请查看侧边栏“Tee for Windows”以获取更多关于如何让此技术生效的用法。

## Windows 版 Tee（以及实用命令）

Windows 环境没有像 Unix 那样的内置 `tee` 命令，但你可以使用 Git for Bash 或 Cygwin 提供的。如果你使用的是标准的命令提示符，可以在 PowerShell 中使用带有 `-Append` 标志的 `Out-Content`。

Windows 环境没有像 Unix 那样的内置 `tee` 命令，但你可以使用 Git for Bash 或 Cygwin 提供的。如果你使用的是标准的命令提示符，可以在 PowerShell 中使用带有 `-Append` 标志的 `Out-Content`。

Windows 环境没有像 Unix 那样的内置 `tee` 命令，但你可以使用 Git for Bash 或 Cygwin 提供的。如果你使用的是标准的命令提示符，可以在 PowerShell 中使用带与 `-Append` 标志的 `Out-Content`。

Windows 环境没有像 Unix 那样的内置 `tee` 命令，但你可以使用 Git for Bash 或 Cygwin 提供的。如果你使用的是标准的命令提示符，可以在 PowerShell 中使用带有 `-Append` 标志的 `Out-Content`。

Windows 环境没有像 Unix 那样的内置 `tee` 命令，但你可以使用 Git for Bash 或 Cygwin 提供的。如果你使用的是标准的命令提示符，可以在 PowerShell 中使用带有 `-Append` 标志的 `Out-Content`。

Windows 环境没有像 Unix 那样的内置 `tee` 命令，但你可以使用 Git for Bash 或 Cygwin 提供的。如果你使用的是标准的命令提示符，可以在 PowerShell 中使用带有 `-Append` 标志的 `Out-Content`。

## 监控输出

Windows 环境没有像 Unix 那样的内置 `tee` 命令，但你可以使用 Git for Bash 或 Cygwin 提供的。如果你使用的是标准的命令提示符，可以在 PowerShell 中使用带有 `-Append` 标志的 `Out-Content`。

## 部署 217

名称。你也可以使用 -f 标志来告诉它匹配脚本名称，如果你的计算机上运行着多个 Node 服务器。因此，要获取运行 script_name.js 的最新创建的 Node 进程的 pid，你使用

`pgrep -n "node script_name.js"`

现在，要获取你的进程占用的内存，你需要使用两个命令。

第一个是 `ps` 命令，它会给你 `wux`（在某些平台上是 `aux` - 请检查你的文档）标志，让你看到这些标志的总内存消耗情况，以及当前的驻留内存大小（你需要的那个）。`ps wux $pid` 的输出如下：

| USER | MEM | VSZ | RSS | TT | STAT | STARTED | TIME | COMMAND |

| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| marcw | 1974 | 6.6 | 3.4 | 450780 | 571888 | ?? | R | 12:15AM | 52:02.42 command name |

你想要输出的第六列。为了得到这个值，你必须首先使用

`awk` 命令获取第二行，然后运行它来获取第六列的值，如下：

`ps wux $PID | awk 'NR=1' | awk 'print ($6)'`

根据你的进程消耗的内存量，你可以决定它是否占用了过多内存并在必要时将其终止。

我不会在这里打印脚本的代码，但你可以在 GitHub 存储库中第 10 章的代码中看到它，文件名为 `node_ninja_runner.sh`。要使用它，你可以像这样运行：

`node_ninja_runner.sh server.js [extra params]`

当然，如果你要监听如 80 或 443 等端口，你需要确保它已提升到超级用户权限。

## Windows

在 Windows 上，运行你的受监控的应用程序的最佳方法是使用 Windows 服务。Node.js 的设计并不是为了作为 Windows 服务，但幸运的是你可以使用一些技巧让它表现得像服务一样。

通过使用一个名为 `nsm.exe`（不差劲的服务管理器）的优秀小程序和一个名为 `winser` 的 npm 模块，你可以将你的 Node Web 应用安装为服务，并通过 Windows 管理控制台完全管理它们。要进行设置，你需要做两件事：

- 1. 在 Web 应用的 `package.json` 中安装一个新的自定义操作。

- 2. 下载并安装 `winser` 并让其工作。

对于第一步，你只需要向 `package.json` 文件添加以下内容：

```json
{
  "name": "Express-Demo",
  "description": "Demonstrates Using Express and Connect",
```

# 第 10 章 部署与开发

```json
"version": "0.0.1",
"private": true,
"dependencies": {
  "express": "3.x"
},

"scripts": {
  "start": "node 01_express_basic.js"
}
```

对于第二步，你只需要执行以下操作：

```bash
C:\Users\Mark\LearningNode\Chapter10> npm install winser
```

（或者你可以通过向项目文件夹添加依赖项来添加 `winser`。）然后，当你准备好将应用安装为服务时，你可以进入持有 `package.json` 的项目文件夹。

```bash
C:\Users\Mark\LearningNode\Chapter10> node_modules\.bin\winser -i
```

程序 Express-Demo 已作为服务安装。

要卸载该服务，只需运行 `winser -r`，如下：

```bash
C:\Users\Mark\LearningNode\Chapter10> node_modules\.bin\winser -r
```

Express-Demo 的服务已移除。

你可以进入 Windows 管理控制台，随心所欲地启动、停止、暂停或管理该服务！

# 多处理器部署：使用代理

我提到过多次，Node.js 实际上是作为一个单线程进程运行的：你编写的所有代码都在同一个线程中，你使用异步回调来尽可能从你的 CPU 中获得最大的效率。

然而，你必须问一个问题：在具有多个 CPU 的系统上你应该做什么？你该如何提取你服务器的最大功能？许多现代服务器是强大的 8-16 核心机器，你希望尽可能使用所有它们。

幸运的是，答案相当简单：只需为你想要利用的每个核心运行一个 node 进程即可（见图 10.1）。你可以根据你的需求选择多种策略之一将流量路由到各种不同的 node 进程。

你现在面临的问题是你运行的不是一个，而是 n 个 Node 进程，它们都必须监听不同的端口。（你不能让多个人监听同一个端口。）你如何让指向 `mydomain:80` 的流量到达这些服务器上？

# 多处理器部署：使用代理 219

![](img/462d9f726aa4852bc590bb4b26fa8f32_234_0.png)

图 10.1 为同一个应用运行多个 node 进程

你可以通过实现一个简单的轮询负载均衡器来解决这个问题，该均衡器获得一个运行你特定 Web 应用的 node 服务器列表。然后你将进入你域名的请求重定向到这些其他服务器，一次一个。当然，你可以尝试监控负载、可用性或响应时间的更高级策略。

要实现负载均衡器，你首先编译一个正在运行的服务器列表。假设你有一个四核服务器；你将其中三个核心交给应用程序（并留出第四个用于运行其他系统服务）。你在端口 8081、8082 和 8083 上运行这些应用服务器。因此，你的服务器列表为：

```json
"servers": {
  "host": "localhost",
  "port": "8081"
},
{
  "host": "localhost",
  "port": "8082"
},
{
  "host": "localhost",
  "port": "8083"
}
```

这些简单服务器的代码在列表 10.1 中所示。这是你在书中看到的最简单的 Web 服务器，额外有一段代码用于从命令行获取监听的端口号。（你将在第 11 章“命令行编程”中学习更多关于命令行参数的知识。）

# 第 10 章 部署与开发

列表 10.1 简单的 HTTP 服务器

```javascript
var http = require('http');

if (process.argv.length != 3) {
    console.log("Need a port number");
    process.exit(-1);
}

var s = http.createServer(function (req, res) {
    res.end("I listened on port " + process.argv[2]);
});

s.listen(process.argv[2]);
```

你可以在 UNIX/Mac 平台上通过输入以下命启动三个服务器：

- $ simple.js 8081 &

- $ simple.js 8082 &

- $ simple.js 8083 &

在 Windows 平台上，你可以通过在不同的命令提示符中运行以下命令启动它们：

- node simple.js 8081

- node simple.js 8082

- node simple.js 8083

你可以使用 npm 模块 `http-proxy` 构建你的代理服务器。`package.json` 如下：

```json
{
    "name": "Round-Robin-Demo",
    "description": "A little proxy server to round-robin requests",
    "version": "0.0.1",
    "private": true,
    "dependencies": {
        "http-proxy": "0.8.x"
    }
}
```

代理的代码非常简单，如列表 10.2 所示。它基本上维护了一个可用服务器数组（如之前所示），然后对于到达服务的每个请务，它都会循环遍历这些可用服务器并将请求转发给它们。

# 多处理器部署：使用代理 221

列表 10.2 轮询代理负载均衡器 (roundrobin.js)

```javascript
var httpProxy = require('http-proxy'),
fs = require('fs');

var servers = JSON.parse(fs.readFileSync('server_list.json')).servers;

var s = httpProxy.createServer(function (req, res, proxy) {
  var target = servers.shift();
  // 1. 移除第一个服务器
  proxy.proxyRequest(req, res, target);
  // 2. 路由回该服务器
  servers.push(target);
  // 3. 加回列表末尾
});

s.listen(8080);
```

为了执行这一切，你现在运行 `nrobin.js`，你可以这样查询它：

```bash
curl -X GET http://localhost:8080
```

当你多次运行此命令时，你应该看到输出显示当前处理服务器所监听的实际端口号。

# 多服务器与会话

在不同的 CPU 和服务器上运行多个服务器是分担负载并提供廉价扩展路径的极佳方法。（服务器负载过？只需添加更多！）但在你有效使用它们之前，需要解决一个小的复杂性：会话数据持续使用 `MemoryStore` 对象按进程存储（参考第 7 章“使用 Express 构建 Web 应用中的 POST 数据、Cookies 和会话）。这产生了一个严重的问题，如图 10.2 所示。

每个 Node 服务器都在自己的内存存储中存储会话记录，当来自同一个客户端的请求进入不同的 node 进程时，它们对客户端会话数据的当前状态看法不同并迅速陷入混乱。你有两种明显的方法解决这个问题：

- 1. 实现一个更高级的路由器，记录请求发送到了哪个 Node 服务器，并确保所有流量继续以相同的方式路由。

- 2. 以某种方式池化会话数据使用的内存存储，以便所有 Node 进程都能访问。

我更倾向于第二种方案，因为它实现非常简单，并且是一个不那么复杂的解决方案。

# 第 10 章 部署与开发

![](img/462d9f726aa4852bc590bb4b26fa8f32_237_0.png)

- 1. 客户端调用服务器，路由到服务器 1

- 2. 服务器创建 session_XYZ，返回数据

- 3. 客户端调用服务器，路由到服务器 2，传递 session_XYZ cookie

- 4. 服务器之前从未见过此 ID，创建新会话

图 10.2 服务器的多个实例和会话数据

要建立这个系统，你首先需要选择一个池化内存存储器。这显而易见的候选者是 memcached 和 Redis，它们都是非常有效的大型基于内存的键值存储器，可以分布在不同的计算机上。我们在本章中使用 memcached，是因为因为它完全能够满足你的需求且极其轻量。你的设置看起来应该与图 10.3 所示类似。

## 在 Windows 上安装

对于 Windows 用户，你可以通过简单的互联网搜索安装许多可用的 memcached 二进制文件之一。你不需要最新、最强大的版本；1.2.x 系列或更后的任何版本都可以。要将其安装为服务，你只需运行：

```
c:\memcached -d install
```

你可以通过输入以下命令运行 memcached 服务：

```
net start memcached
```

最后，你可以编辑 HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Services/memcached 服务，并将 ImagePath 修改为：

```
"C:/memcached/memcached.exe" -d runservice -m 25
```

将提供给 memcached 的可用内存设置为 25MB，这对于开发来说通常足够了。（当然，你可以在这里选择任何你想要的值）。它监听在端口 11211 上。

# 多处理器部署：使用代理

![](img/462d9f726aa4852bc590bb4b26fa8f32_238_0.png)

图 10.3 使用基于内存的键值存储器实现会话

# 在 Mac 和类 Unix 系统上安装

如果你在一个带有某种软件包管理器的系统上，你通常可以使用如下命令（你可能需要 sudo）：

```
apt-get install memcached
```

然后就可以开始使用了。如果你想从源码构建，你首先需要获取 libevent http://libevent.org。下载、编译并（以超级用户身份）安装库。它应该将服务放在 /usr/local/lib。

接下来，访问 memcached.org 下载最新的 tarball（.tar.gz 文件），然后进行配置、编译和安装。同样，请以超级用户身份操作。

运行 memcached 后，执行以下命令：

```
/usr/local/bin/memcached -m 100 -p 11211 -u daemon
```

此命令告诉服务使用 100MB 内存并监听端口 11211，以用户 daemon 身份运行。它通常拒绝作为

# 将 memcached 引入 express

现在你已经安装并运行了 memcached（假设 localhost 上的端口 11211），你需要为它获取一个 MemoryStore 对象，以便你将其用于会话数据。幸运的是，Nodejs 社区非常活跃，因此已经有一个名为 connect-memcached 的 npm 模块。所以，让我们在 package.json 的依赖项中添加以下内容：

```json
"connect-memcached": "0.0.x"
```

然后你可以如下修改你的会话代码：

```javascript
var express = require('express');

// 传递 express 对象以便 connect-memcached 可以继承自 MemoryStore
var MemcachedStore = require('connect-memcached')(express);
var mcds = new MemcachedStore({ hosts: "localhost:11211" });

var app = express()
  .use(express.logger('dev'))
  .use(express.cookieParser())
  .use(express.session({
    secret: "cat on keyboard",
    cookie: { maxAge: 1800000 },
    store: mcds
  }));

.use(function(req, res) {
    var x = req.session.last_access;
    req.session.last_access = new Date();
    res.end("你上次请求此页的时间是: " + x);
  })
  .listen(8080);
```

现在，所有的 Node 服务器都可以配置为使用相同的 MemoryStore 进行会话数据，并且无论请求在何处被处理，都能够获取正确的信息。

# 虚拟托管

多年来，在服务器上运行多个网站一直是 Web 应用平台的一个主要需求，幸运的是当你使用 express 构建应用时，Node.js 为你提供了几个非常行的解决方案。

你通过在传入的 HTTP 请求中添加 Host 头部来实现虚拟托管，这是 HTTP/1.1 的主要功能之一（见图 10.4）。

# 虚拟托管

请求：

Host: A

![](img/462d9f726aa4852bc590bb4b26fa8f32_240_0.png)

图 10.4 虚拟托管背后的原理

# 内置支持

运行多个虚拟主机的功能直接内置在 express 中。为了使其工作，你为你每个想要支持的主机创建一个 express 服务器。

# 生成测试证书

要在你的开发机器上处理加密流量，你需要生成一些测试证证书。你需要生成两个文件——`privkey.pem` 和 `newcert.pem`——分别是私钥和证书。所有的 UNIX/Mac 机器都带有一个名为 `openssl` 的工具，你可以用它生成这两个文件。

对于 Windows 用户，你可以访问 http://gnwin32.sourceforge.net/packages/openssl.htm 下载 Win32 版本的 `openssl.exe`。你运行的命令与其他平台相同。

要生成这两个证书文件，请运行以下三条命令：

```
openssl genrsa -out privkey.pem 1024
openssl req -new -key privkey.pem -out certreq.csr
openssl x509 -days 3650 -in certreq.csr -signkey privkey.pem -out newcert.pem
```

拿到这两个文件后，你就可以在应用程序中使用它们了。请注意，你**绝对不要**在生产环境站点中使用它们；如果你尝试在浏览器中查看受这些证书保护的网站，你会看到一个糟糕的 localhost 以及一个听起来很危险的警告，告诉它们完全不可信。你通常需要从受信任的证书机构购买生产证书。

# 内置支持

意乎意料的是，Node.js 通过 Node 提供的 `https` 模块提供了对 SSL/HTTPS 流的内置支持。你实际上可以运行一个 `https` 模块服务器来监听 HTTP 端口（默认为 443，但对于开发，你可以使用 8443 以避免提升 Node 进程的权限），然后在加密流协商并创建后，它会将流量路由到 express 服务器。

你创建一个 HTTPS 服务器，并传入选项，包括你计划用于签名站点的私钥和证书文件位置。你还给了它一个 express 服务器，以便它在加密建立后向其发送流量。此代码在列表 10.5 中。

列表 10.5 Express/https 模块支持 (https_express_server.js)

```
var express = require('express');
var https = require('https');
var fs = require('fs');

// 1. 加载证书并创建选项
var privateKey = fs.readFileSync('privkey.pem').toString();
var certificate = fs.readFileSync('newcert.pem').toString();
var options = {
  key: privateKey,
  cert : certificate
}
```

# 使用 HTTPS/SSL 保护你的项目

```
// 2. 创建 express 应用并设置路由等。
var app = express();
app.get("*", function(req, res) {
  res.end("Thanks for calling securely!\n");
});
```

```
// 3. 使用 options 和 express app 启动 https 服务器。
https.createServer(options, app).listen(8443, function() {
  console.log("Express server listening on port 8443");
});
```

你可以通过在地址栏中输入 `https://localhost:8443` 在 浏览器中查看这些加密页面。当你第一次查看它们时，你会收到一个关于它们多么不安全的恐怖警告。

# 代理服务器支持

正如你在本章中调查的许多其他事情一样，你也可以使用极其强大的 `http-proxy` 模块来处理 SSL/HTTPS 流量。与使用内置 HTTPS 支持相比，使用该模块有两个关键优势：你让实际应用程序作为普通的 HTTP 服务器运行，将它们“隐藏”在代理服务器之后，并将它们从解密加密中释放出来。你仍然可以使用之前的轮询负载均衡运行任意数量的实例，或者查看其他创新的方法来设置你的配置。

这种支持的方法与之前代理示例中使用的方法并没有太不同；你创建一个 Node 内置 HTTPS 服务器类的实例，并创建一个代理服务器实例，该实例知道如何将流量路由到普通的 HTTP 服务器（应用服务器）。然后你运行 HTTPS 服务器，当它建立了安全连接时，它会将请求传递给代理服务器，代理服务器反过来将其传递给应用服务器。此支持的代码在列表 10.6 中。

# 列表 10.6 http-proxy SSL 支持 (https_proxy_server.js)

```
var fs = require('fs');
var http = require('http');
var https = require('https');
var httpProxy = require('http-proxy');
```

```
// 1. 准备好证书。
var options = {
  https: {
    key: fs.readFileSync('privkey.pem', 'utf8'),
    cert: fs.readFileSync('cert.pem', 'utf8')
  }
};

// 2. 创建一个 HttpProxy 实例供另一个服务器使用
var proxy = new httpProxy.HttpProxy({
  target: {
    host: 'localhost',
    port: 8081
  }
});
```

```
// 3. 创建 http 服务器并开始接受连接。
https.createServer(options.https, function (req, res) {
  proxy.proxyRequest(req, res)
}).listen(8443);
```

这似乎涉及很多路由和重定向，但 Node 开发小组对性能几乎近乎狂热，这些组件足够轻量，不至于在你的 Web 应用程序处理请求时增加明显的感知延迟。

# 跨平台开发

Node.js 的最大优势之一不仅在于它对 UNIX 类计算机的强力支持，还有它在 Windows 上运行的能力。当我写这本书时，我尝试了所有平台，并发现绝大多数情况下，Node 都接受正斜杠 `/` 字符。

# 位置与配置文件

Windows 和 UNIX 类操作系统之间的另一个主要区别是路径。你缓解这个问题的方法之一是使用配置文件。这种技术在第 8 章“NoSQL (MongoDB)”和第 9 章“SQL (MySQL)”中会将数据库信息放在一个名为 `local.config.js` 的文件中。

# 跨平台开发 (231)

```
exports.config = {
  db_config: {
    host: "localhost",
    user: "root",
    password: "",
    database: "PhotoAlbums",

    pooled_connections: 125,
    idle_timeout_millis: 30000
  },

  static_content: "../static/",
  build_type: "debug" // 显示额外输出
};
```

通常的做法是将此文件在版本控制系统（如 GitHub）中提交为 `local.config.js-base`而不是 `local.config.js`。运行应用程序时，你将此文件复制为 `local.config.js`，根据你的本地设置更新值，然后运行。任何你想使用这些本地配置变量时，只需添加 `var local = require('local.config.js');`。然后在代码中，你可以自由引用 `local.config.variable_xyz`。

# 处理路径差异

Windows 和 UNIX 类操作系统之间的另一个主要区别是路径。当你的处理器位于当前项目目录的子文件夹中时，你如何编写 `require` 这样的代码？消息是，绝大多数情况下，Node 都接受正斜杠 `/` 字符。当你从相对路径（例如 `../path/to/th`）引入模块时，它的运行方式正如你所预期那样。即使在使用 `fs` 模块 API 的情况下，大多数它们也能处理平台之间路径类型的差异。

对于你绝对需要处理不同路径样式的情况，你可以使用 Node.js 中的 `path.sep` 属性，以及对数组连接和分割的巧妙使用，例如：

```
var path = require('path');
var comps = ['..', 'static', 'photos' ];
console.log(comps.join(path.sep));
```

Node.js 中的全局 `process` 对象始终会告诉你你运行在什么平台上，并可以通过以下方式查询：

```
if (process.platform === 'win32') {
  console.log('Windows');
} else {
  console.log('You are running on: ' + process.platform);
}
```

# 总结

在本章中，你学习了如何将 Node 应用部署到生产环境中运行，涵盖了执行脚本、负载均衡和多进程应用。本章还展示了如何使用基于 SSL 的 HTTPS 来保护你的 Web 应用程序，并最后描述了多平台开发，证明了这并没你可能想象的那么可怕。

你现在已经有了一套非常实用的工具，能够让你构建并运行酷炫的异步应用程序。然而，在下一章中，你将看到使用 Node.js 会变得更加酷——你将会发现它有一许多同步 API，非常适合命令行编程和脚本编写。

## 11 命令行编程

在书中花了大量时间讨论 Node.js 是一个用于创建应用的强大异步、非阻塞平台后，现在我将向你展示，有时在 Node 中直接使用普通的同步、阻塞 IO 也很酷——那就是编写命令行程序。事实证明，编写 JavaScript 代码非常有趣，以至于人们开始使用 Node 编写大量的日常脚本和其他快速程序。

在本章中，你将学习在 Node 中运行命令行脚本的基础知识，包括查看一些供你使用的某些同步文件系统 API。然后，你将查看如何通过缓冲和无缓冲输入直接与用户交互，最后将查看进程的创建和执行。

## 运行命令行脚本

对于类 UNIX 和类 Mac 操作系统以及基于 Windows 的系统，你从命令行运行 Node.js 脚本的选项并不多。你可以让这些脚本看起来像普通的操作系统命令，并同时向它们传递命令行参数。

## UNIX 和 Mac

在 Linux 或 Mac OS X 等类 UNIX 操作系统上，绝大多数用户使用 Bourne Shell，sh（或者流行的现代变体 bash）。尽管它附带的脚本语言功能非常全且强大，但有时用 JavaScript 编写脚本可能会更有趣一些。

## 第 11 章 命令行编程

你有两种方式在 shell 中运行你的 Node 程序。最简单的方法是像往常一样运行它——指定 node 程序和要运行的脚本（实际上 .js 后缀是可选的）：

```
node do_something
```

第二种是通过如下修改第一行，使脚本成为可执行文件：

```
#!/usr/local/bin/node
```

前两个字符被称为 shebang，它们告诉操作系统，紧随其后的内容是执行该文件时作为给定参数的程序路径。在以前的例中中，操作系统知道去 /usr/local/bin 寻找可执行的 node，运行它，并将文件作为参数传递给 Node。Node 解释器足够智能，会忽略这行以 # 开头的首行；它意识到这些是给操作系统使用的。

因此，你可以在 Node 中编写以下 hello world 可执行文件：

```
#!/usr/local/bin/node
console.log("Hello World!");
```

要作为可执行文件运行该程序，你还需要使用 `chmod` 命令将其标记为可执行文件：

```
chmod 755 hello_world
```

现在你可以通过输入以下命令直接执行脚本：

```
$ ./hello_world
Hello World!
$
```

这种方法有一个小问题：当你把脚本带到其他机器上，而 node 不在 /usr/local/bin 中，而是在 /usr/bin 中，会发生什么？常见的解决方案是按如下更改 shebang 行：

```
#!/usr/bin/env node
```

`env` 命令会遍历你的 `PATH` 环境变量以找到第一个 node 程序实例并运行它。由于所有 Unix/Mac 机器的 /usr/ 下都有 env，所以只要 node 在 PATH 某处，这种方法就更具可移植性。

如果你在各种操作系统的可执行目录或其他安装软件的地方翻找，你会发现许多经常使用的程序实际上都是某种形式的脚本。

额外小奖励：Node 解释器足够智能，即使在 Windows 上也能忽略 # 语法，因此你仍然可以编写可以在两个平台上都作为可执行文件运行的脚本！

## 运行命令行脚本

Microsoft Windows 从未真正拥有过一个出色的脚本环境。Windows Vista 和 7 引入了 PowerShell，这是对以前版本的很好的改进，但它感觉仍然不如 UNIX 平台上的 shell 那么强大和易用。好消息是，这并不会产生太大影响，因为你的主要目标只是让脚本启动并执行，而所有现代（以及半正式）版本的 Windows 提供的功能绰绰有余。

你可以使用批处理文件（带有 .bat 后缀）运行你的脚本。如果你有上一节中看到的 hello_world.js，你可以按照如下方式创建 hello_world.bat：

```
@echo off
node hello_world
```

默认情况下，Windows 会回显它在批处理文件中看到的每一个命令。`@echo off` 告诉它停止显示。现在，要运行程序，你可以输入：

```
C:\Users\Mark\LearningNode\Chapter11\hello_world
Hello World!
C:\Users\Mark\LearningNode\Chapter11\
```

但这里有一个 bug：hello_world.bat 和 hello_world.js 在同一个文件夹中，但你从其他地方执行，如下所示：

```
C:\Users\Mark\LearningNode\Chapter11\hello_world
Error: Cannot find module 'C:\Users\Mark\LearningNode\Chapter11\hello_world'
    at Function.resolve (node.js:340)
    at Function._load (node.js:338)
    at Function.runMain (node.js:492)
    at process.nextTick(node.js:244)
```

因为你没有指定路径，Node 迷路了。你通过将 hello_world.bat 修改如下来修复它：

```
@echo off
node %~0
```

在这里，你可以使用两个批处理文件宏 %0 和 %~ 分别给你提供运行脚本的驱动器和路径。你可以从任何地方运行 hello_world，它都能工作：

```
C:\Users\Mark\LearningNode\Chapter11\hello_world
Hello World!
```

## 脚本与参数

为了能用脚本做有趣的事情，你需要传递参数。在这种情况下，你需要担心两个问题：如何将这些参数传递给脚本以及如何在脚本内部访问它们。

如果你始终通过调用解释器运行 Node 脚本（适用于所有平台），你不需要额外操作——参数会直接传递给执行脚本：

```
node script_name [args]
```

## 在 UNIX/Mac 上传递参数

在通过 #! 语法启动脚本的类 UNIX 操作系统上，当你运行时时，这些参数直接传递给脚本。所以在这里你不需要做其他事情。

## 在 Windows 上传递参数

在 Windows 上，你主要通过带有 .bat 后缀的批处理文件运行 Node 脚本。你可以向这些批处理文件传递参数，它们随后使用宏 % 将参数传递给你的 Node.js 脚本。因此，批处理文件如下：

```
node %
```

## 在 Node 中访问参数

传递给脚本的所有参数都会附加到 `process` 全局对象的 `argv` 数组上。此数组的前两个项总是运行的 node 解释器和运行的脚本。因此，传递给脚本的任何额外参数从第三个元素（索引为 2）开始。现在运行：

```
#!/usr/local/bin/node
console.log(process.argv);
```

你应该看到如下输出：

# 同步处理文件

对于你在文件系统模块 (fs) 中看到的几乎每一个 API，都提供了异步和同步版本。到目前为止，你大部分时候都在使用异步版本，但在编写命令行程序时，同步版本对你可能非常有用。基本上，对于 `fs` 中大多数以 `func` 命名的 API，都有一个对应的名为 `funcSync` 的 API。

在接下来的章节中，你将看到一些如何使用某些同步 API 的示例。

## 基础文件 API

`fs` 模块没有复制文件的函数，因此你可以自己写一个。对于 `open`、`read` 和 `write` API，你使用同步版本：`openSync`、`readSync` 和 `writeSync`。在同步版本，如果发生任何问题，它们会抛出错误。你可以使用缓冲区来存储从位置 a 复制到 b 的的数据。请确保在完成后关闭所有打开的内容：

```javascript
var BUFFER_SIZE = 1000000;

function copy_file_sync (src, dest) {
  var read_so_far, fdsrc, fdest, read;
  var buff = new Buffer(BUFFER_SIZE);

  fdsrc = fs.openSync(src, 'r');
  fdest = fs.openSync(dest, 'w');
  read_so_far = 0;

  do {
    read = fs.readSync(fdsrc, buff, BUFFER_SIZE, read_so_far);
    fs.writeSync(fdest, buff, 0, read);
    read_so_far += read;
  } while (read > 0);

  fs.closeSync(fdsrc);
  return fs.closeSync(fdest);
```

要调用此函数，你可以写一个 `file_copy.js` 脚本，让它获取足够的参数，调用复制函数，并处理过程中抛出的任何错误：



```javascript
if (process.argv.length != 4) {
  console.log("Usage: " + path.basename(process.argv[1], '.js')
  + " [src_file] [dest_file]");
} else {
  try {
    copy_file_sync(process.argv[2], process.argv[3]);
  } catch (e) {
    console.log("Error copying file:");
    console.log(e);
    process.exit(-1);
  }

  console.log("1 file copied.");
}
```

在这里你可以看到你还利用了一个新函数 `process.exit`。该函数会立即终止 Node.js 程序，并将返回码传回调用程序（通常是 shell 解释器或命令提示符）。Bourne shell (sh 或 bash) 的标准是成功时返回 0，发生糟糕情况时返回非零值。当复制出现错误时，你返回 -1。

你可以很容易地将此复制函数更改为移动函数，方法是在确定目标文件已完全写入并成功关闭后，执行复制文件操作并删除源文件。通过使用 `unlinkSync` 函数来实现：

```javascript
function move_file_sync(src, dest) {
  var read_so_far, fdsrc, fdest, read;
  var buff = new Buffer(BUFFER_SIZE);

  fdsrc = fs.openSync(src, 'r');
  fdest = fs.openSync(dest, 'w');
  read_so_far = 0;

  do {
    read = fs.readSync(fdsrc, buff, BUFFER_SIZE, read_so_far);
    fs.writeSync(fdest, buff, 0, read);
    read_so_far += read;
  } while (read > 0);

  fs.closeSync(fdsrc);
  fs.closeSync(fdest);
  return fs.unlinkSync(src);
}
```

脚本的其余部分保持，只需将对 `copy_file_sync` 的调用更改为 `move_file_sync`。

## 文件与状态信息

你使用文件系统模块中的 `mkdir` 函数在 Node 中创建文件夹。在所示的脚本中，你使用的是它的 `mkdirSync` 变体。现在你准备好编写一个行为与 UNIX shell 中的 `mkdir -p` 命令相同的程序了：你指定一个完整路径，它会创建目录以及任何不存在的中间目录。

这项工作分两步完成：

- 1. 你拆分路径，然后从顶部开始检查哪些目录已经存在，哪些不存在。如果给定位置存在某个东西但不是目录（例如，你想使用 `mkdir a/b/c`，但 `a/b` 已存在且是一个普通文件），就会抛出一个错误。要确定文件是否存在，你使用 `existsSync` 函数，然后调用 `statsSync` 函数，它会给你一个 `Stats` 对象，该对象可以告诉你是否为目录。

- 2. 对于所有尚未创建的条目，对它们进行迭代。

这里是 `mkdirirs` 函数的代码：

```javascript
function mkdirirs (path_to_create, mode) {
  if (mode == undefined) mode = 0777 & (-process.umask);

  // 1. 我们已经有了什么或什么还没有？
  var parts = path_to_create.split(path.sep);
  var i;
  for (var i = 0; i < parts.length; i++) {
    var search;
    search = parts.slice(0, i + 1).join(path.sep);
    if (fs.existsSync(search)) {
      var st;
      st = fs.statSync(search);
      if (!st.isDirectory()) {
        throw new Error(search + " is not a directory");
      }
    } else {
      // 2. 对于尚未创建的条目，进行迭代
      fs.mkdirSync(search, mode);
    }
  }
}
```

# 第 11 章 命令行编程

```javascript
process.stdin.on('readable', function (data) {
  var data = process.stdin.read();
  if (!process.stdin.isRaw) { // 1.
    if (data == "\n") process.exit(0);
    process.stdout.write("Please select type of hash:\n");
    process.stdout.write("1 - md5, 2 - sha1, 3 - sha256, 4 - sha512 \n");
    process.stdout.write("[1-4] > ");
    process.stdin.setRawMode(true);
  } else {
    var alg = "C";
    if (data != "C") { // 2.
      var c = parseInt(data);
      switch (c) {
        case 1: alg = 'md5'; break;
        case 2: alg = 'sha1'; break;
        case 3: alg = 'sha256'; break;
        case 4: alg = 'sha512'; break;
      }
      if (alg) { // 3.
        var hash = require('crypto').createHash(alg);
        hash.update(data);
        process.stdout.write("\nHashed to: " + hash.digest('hex') + "\n");
        process.stdout.write("\ndata to hash > ");
        process.stdin.setRawMode(false);
      } else {
        process.stdout.write("\nPlease select type of hash:\n");
        process.stdout.write("[1-4] > ");
      }
    } else {
      process.stdout.write("\ndata to hash > ");
      process.stdin.setRawMode(false);
    }
  }
});
process.stdin.setEncoding('utf8');
process.stdin.resume();
```

由于此脚本既会在缓冲状态下（你请求要哈希的文本）又会在非缓冲状态下（你请求要使用的哈希算法时）从 stdin 接收输入，所以它的逻辑稍微复杂一些。让我们它是如何工作的：

- 1. 你首先检查接收到的输入是缓冲的还是非缓冲的。如果是前者，说明是一行要哈希的文本，你应该打印出选择哪种算法的请求。因为你希望用户只需输入 1 到 4 之间的数字，所以现在当按下任何键都会触发 `readable` 事件时，你将 stdin 切换到 RawMode。

- 如果流处于 RawMode，意味着用户响应你对哈希算法的请求按了一个键。在这里的第一行代码中，你检查该键是否为 Ctrl+C。（注意，在编辑器中输入这可能困难；在 Emacs 中，你可以按 Ctrl+Q 然后 Ctrl+C，它会为你输入 ^C。每个编辑器都略有不同。）如果用户按了 Ctrl+C，你中止输入请求并返回哈希提示符。

如果用户输入了其他键，确保它是一个有效键（1–4），否则就报错并让他重试。

最后，根据你生成哈希的算法，将其打印出来，然后返回到正常的输入数据提示符。你必须确保关闭 RawMode，以便返回行缓冲输入模式！

再次，由于你在此程序中恢复了 stdin 的读取，在没有调用 `process.exit`、用户回输入了空行，或者用户在缓冲输入期间按下 Ctrl+C（这会导致 Node 直接终止）之前，程序不会退出。

# readline 模块

在 Node.js 中处理输入的一种方法是使用 `readline` 模块。它仍然被标记为 Unstable（未稳定）并可能会发生变化，因此我没有投入它投入太多精力和精力，但它有几个你可以在程序中使用的整洁特性。

要启用 `readline` 模块，调用它的 `createInterface` 方法，并指定 stdin 和 stdout 流为：

```javascript
var readline = require('readline');
```

```javascript
var rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});
```

执行此操作后，在调用 `rl.close` 之前，你的程序不会退出！

# 逐行提示

如果你在 readline 中调用 `prompt` 方法，程序会等待一行输入（后跟回车）。当程序获取到此按键时，它会在 `readline` 对象上发送 `line` 事件。你可以根据需要处理该事件：

```javascript
rl.on("line", function (line) {
  console.log(line);
  rl.prompt();
});
```

要继续监听，你需要再次调用 `prompt`。`readline` 接口的好处之一是，如果用户按下 Ctrl+C，你会收到 `SIGINT` 事件，你可以直接在那里关闭，也可以执行其他操作来重置状态并继续。在这里，通过关闭 `readline` 接口，你导致提示符停止监听输入并退出：

```javascript
rl.on('SIGINT', function () {
  rl.close();
});
```

现在你准备好使用 `readline` 模块编写一个小型逆波兰表达式（Reverse Polish Notation）计算器了。该计算器的代码如列表 11.2所示。

如果你从未听说过逆波兰表达式或忘记了它是如何工作的，它基本上是一种后置数学表示法。与其写 `1 + 2`，你不如写 `1 2 +`。要写 `5 * (2 + 3)`，你应该写：`5 2 3 + *`。这个计算器一次处理一个字符串，将其拆分并进行计算。

# 列表 11.2 简单的后置计算器 (readline.js)

```javascript
var readline = require('readline');
var rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

var p = "postfix expression > ";
rl.setPrompt(p);

rl.on("line", function (line) {
  if (line == "") {
    rl.close();
    return;
  }
  var parts = line.split(" ");
  var stack = [];
  for (var i = 0; i < parts.length; i++) {
    var num = parseFloat(parts[i]);
    if (!isNaN(num)) {
      stack.push(num);
    } else {
      var b = stack.pop();
      var a = stack.pop();
      switch (parts[i]) { // 2
        case '+': stack.push(a + b); break;
        case '-': stack.push(a - b); break;
        case '*': stack.push(a * b); break;
        case '/': stack.push(a / b); break;
        default: throw new Error("Unexpected operator");
      }
    }
  }
  if (stack.length == 1) {
    process.stdout.write("Result: " + stack.pop() + "\n");
  } else {
    process.stdout.write("Invalid expression.\n");
  }
  rl.prompt(); // 3
});

rl.on("SIGINT", function () { // 4
  rl.close();
});
```

现在你可以测试它了：

```
Kidori:03$ node readline_rpn.js
postfix expression > 1 2 +
Result: 3
postfix expression > 2 3 4 + *
Result: 14
postfix expression > cat
Invalid expression.
```

## 问题

该模块的另一个主要功能是提问并在回调函数中直接接收答案。基本格式是：

```javascript
rl.question('hello?', function(answer) {
  // 执行某些操作
});
```

接下来，你编写一个执行调查的小程序：它获取一个问题数组（你可以将其放在文件中以便配置），并每次向用户提问一个。它使用 `fs` 模块的 `appendFileSync` 将用户的答案写入 `answers.txt`。

注意，由于该函数是异步的，你必须使用 `async.forEachSeries` 来遍历调查中的每个问题！调查程序的代码如列表 11.3 所示。

# 列表 11.3 调查程序 (questions.js)

```javascript
var readline = require('readline'),
  async = require('async'),
  fs = require('fs');

var questions = [ "What's your favorite color? ",
  "What's your shoe size? ",
  "Cats or dogs? ",
  "Doctor Who or Doctor House? " ];

var rl = readline.createInterface({ // 1.
  input: process.stdin,
  output: process.stdout
});

async.forEachSeries(questions, function (question, callback) {
  rl.question(question, function (answer) {
    fs.appendFileSync('answers.txt', question + answer + "\n");
    callback();
  });
}, function () { // 2.
  console.log("Survey complete.");
  rl.close(); // 3
}); // 4
```

# 处理进程

```javascript
var output = [];
async.forEachSeries(
  questions,
  function (item, cb) { // 2.
    rl.question(item, function (answer) {
      output.push(answer);
      cb(null);
    });
  },
function (err) { // 3.
    if (err) {
      console.log("Hunh, couldn't get answers");
      console.log(err);
      return;
    }
    fs.appendFileSync("answers.txt", JSON.stringify(output) + "\n");
    console.log("\nThanks for your answers!");
    console.log("We'll sell them to some telemarketer immediately!");
    rl.close();
  }
);
```

该程序执行以下任务：

- 1. 它初始化 readline 模块并设置了 stdin 和 stdout 流。

- 2. 然后，对于数组中的每个问题，你都会调用 readline 上的函数（使用 async.forEachSeries 是因为问题是一个异步函数），并将结果添加到 output 数组中。

- 3. 最后，在所有问题都提问且 async 调用结果函数后，你要么打印错误（如果有的话），要么将用户的输出追加到 answers.txt 文件，然后关闭 readline 对象以退出程序。

# 处理进程

在 Node 中，你可以从命令行（甚至从你的 Web 应用程序内部）执行的操作之一是启动其他程序。使用 `child_process` 模块你有几种选择，复杂度程度各异。在接下来的章节中，我们将使用较简单的选项 `exec`。

# 简单的进程创建

`child_process` 模块中的 `exec` 函数接收一个命令并在系统 shell（UNIX/Mac 上为 sh/bash，Windows 上为 cmd.exe）中执行它。因此，你可以指定一个简单的命令如 `date` 作为要运行的程序，也可以指定一个像 `"echo 'Mancy' | sed s/M/N/g"` 这样复杂的命令。所有命令都会运行，所有输出会被缓冲并在命令完成后传给调用者。

基本格式为：

```javascript
exec(command, function (error, stdout, stderr) {
  // 如果发生错误，error 则不为空
  // stdout 和 stderr 是缓冲区
});
```

命令执行完成后，回调函数会被调用。只有在发生错误时，第一个参数才不为空。否则，`stdout` 和 `stderr` 被设置为 Buffer 对象，包含任何写入相应输出流的完整内容。

现在写一个程序使用 `exec cat` 程序（Windows 上为 `type`）的程序。它接受一个文件名并打印出来。它使用 `exec` 函数启动 `cat/type` 程序并在完成后打印所有输出：

```javascript
var exec = require('child_process'), exec, child;

if (process.argv.length != 3) {
  console.log("I need a file name");
  process.exit(-1);
}
```

```javascript
var file_name = process.platform == 'win32' ? 'type' : "cat";
var child = exec(cmd + " " + file_name, function (error, stdout, stderr) {
  console.log('stdout: ' + stdout);
  console.log('stderr: ' + stderr);

  if (error) {
    console.log("Error exec'ing the file");
    console.log(error);
    process.exit(1);
  }
});
```

# 使用 Spawn 创建高级进程

创建进程的更高级的方法是使用 `child_process` 模块中提供的 `spawn` 函数。该函数允许你对创建的子进程的 `stdin` 和 `stdout` 进行完全控制，并允许一些强大的功能，例如将输出从一个子进程管道到另一个。

# 处理进程 249

首先写一个程序，接收一个 JavaScript 文件名并使用 node 程序运行它：

```javascript
var spawn = require("child_process").spawn;
var node;

if (process.argv.length != 3) {
  console.log("I need a script to run");
  process.exit(-1);
}

var node = spawn("node", [ process.argv[2] ]);
node.stdout.on('readable', print_stdout);
node.stderr.on('readable', print_stderr);
node.on('exit', exited);
```

```javascript
function print_stdout() {
  var data = process.stdout.read();
  console.log("stdout: " + data.toString('utf8'));
}
function print_stderr(data) {
  var data = process.stderr.read();
  console.log("stderr: " + data.toString('utf8'));
}
function exited(code) {
  console.error("--> Node exited with code: " + code);
}
```

当你想要使用 `spawn` 时，第一个参数是要执行的命令名称，第二个参数是传递给它的参数数组。你可以看到，写入到子进程 `stdout` 或 `stderr` 的任何输出都会立即触相应流上的事件，你可以立即看到发生了什么。

现在你准备好写一些高级一点的内容。在前面的章节中，你看到了如何在 shell 脚本或命令提示符中有效实现以下操作：

```
while 1
  node script_name
end
```

使用 `spawn` 函数编写相同的 代码。使用这个函数实际上比在 shell 中编写要多一些工作，但它具有启发性，并让你以后能够进行更多工作和监控。新启动器的代码如列表 11.4 所示。

# 11 章命令行编程

列表 11.4 一个全能 Node 运行器 (node_runner.js)

```javascript
var spawn = require("child_process").spawn;
var node;
```

```javascript
if (process.argv.length < 3) {
  console.log("I need a script to run");
  process.exit(-1);
}
```

```javascript
function spawn_node() {
  var node = spawn("node", process.argv.slice(2));
  node.stdout.on("readable", print_stdout);
  node.stderr.on("readable", print_stderr);
  node.on('exit', exited);
}
```

```javascript
function print_stdout() {
  var data = process.stdout.read();
  console.log("stdout: " + data.toString("utf8"));
}
```

```javascript
function print_stderr(data) {
  var data = process.stderr.read();
  console.log("stderr: " + data.toString("utf8"));
}
```

```javascript
function exited(code) {
  console.error("--> Node exited with code: " + code + ". Restarting");
  spawn_node();
}
```

spawn_node();

该程序通过通过被创建进程的 `exit` 事件来工作。每当它看到该事件时，就会使用你想运行的脚本重启 node 解释器。

我留给你做一个练习：更新此脚本以使其行为像你在前一章节中编写的完整的 `node_ninja_runner`。你可以使用 `exec` 函数获取 `ps aux` 命令的输出；生成的缓冲区可以在 JavaScript 中轻松地解析。最后，如果你检测到子进程过大，可以通过调用其上的 `kill` 方法来杀死子进程。

# 总结

现在你已经看到 Node 不仅对于编写网络应用程序非常棒，对于命令行同步应用程序也极其强大且有趣。在介绍了创建、运行脚本以及向它们传递参数之后，你现在应该非常熟悉如何操作程序中的输入和输出了。最后，你应该能够使用 `exec` 和 `spawn` 在 Node.js 中创建并运行程序。

为了完成对 Node.js 编程的介绍，现在是时候注意力转向测试你的脚本了。

# 12 测试

有了你目前为止编写的所有代码，你现在准备好查看如何测试它们以确保其正常工作。实现此目的有很多模型和范式，Node.js 支持其中的大多数模型。本章将介绍一些更常见的模型，然后介绍你如何对你的相册应用程序进行功能测试。

# 选择框架

目前有几种常见的测试模型，包括*测试驱动开发 (TDD) 和行为驱动开发 (BDD)*。前者高度关注于让你的所有代码都正确地暴露在测试之下（事实上，在许多情况下，要求你在为代码编写测试之前不编写任何代码），而后者关注于特定代码单元或模块的业务需求，并鼓励进行比简单的单元测试更具整体性的测试。无论你遵循哪种模型（如果你是第一次写测试，那么以后将遵循），在你的代码库中添加测试始终是一个好主意，因为你不仅想确保你所写的东西可以运行，还要确保未来的代码更改不会破坏功能。在现有的许多框架中，有三个最受欢迎：

- node—这是一个简单直接的测试运行器，用于在 Node 和浏览器中进行测试。它非常易于使用，并为设置你的测试框架提供了很大的灵活性。

- Mocha—基于一个名为 Espresso 的旧测试框架，Mocha 基本上是一个功能更丰富的 Node TDD 框架，专注于更易于使用和更具趣味的编码。它在异步测试方面有一些酷酷的功能，并提供了一个输出格式化的 API。

## 第 12 章 测试

- VowsJS—Node.js 中最著名的 BDD 测试框架，VowsJS 不仅具有非常描述性的语法和结构，可以将 BDD 思想与你的测试结合起来，还能并发运行你的测试以实现更快的执行。

尽管它们运行得非常完美且有其用处，但对于本章，你可以坚持使用相当直观的 nodeunit，很大程度上因为它非常易于操作和演示。

## 安装 Nodeunit

对于你现在的项目，你可以创建一个 `test/` 子文件夹，在其中放入所有与你各种项目测试相关的文件、示例和数据文件。第一个放入进去的文件是 `package.json`，如下所示：

```json
{
  "name": "API-testing-demo",
  "description": "Demonstrates API Testing with nodeunit",
  "version": "0.0.1",
  "private": true,
  "dependencies": {
    "nodeunit": "0.7.x"
  }
}
```

当你运行 `npm update` 时，nodeunit 就会被安装，你就可以开始编写和运行测试了。

## 编写测试

Nodeunit 将测试组织成模块，每个导出的函数充当一个测试，每个导出的对象充当一组测试。对于每一项测试，你都会获得一个对象，它可以帮助你执行测试并在你完成时通知 nodeunit：

```javascript
exports.test1 = function (test) {
  test.equals(true, true);
  test.done();
}
```

你必须在每一个测试的末尾调用 `test.done`；否则 nodeunit 不知道测试何时结束。若要运行此测试，请将其保存为名为 `trivial.js` 的文件，并运行 `node_modules/.bin` 文件夹中提供的运行脚本。在 Unix/Mac 平台和 Windows 上，你运行（当然，在 Windows 上要将 `/` 切换为 `\`）：

```bash
node_modules/.bin/nodeunit trivial.js
```

你会看到类似的内容：

```bash
C:\Users\Mark\a> node_modules\.bin\nodeunit.cmd trivial.js

trivial.js

- test1

OK: 1 assertions (0ms)

C:\Users\Mark\a>
```

## 简单功能测试

对于你编写的每个测试，你想做三件事：

- 1. 在提供的 `test` 参数上调用 `expect` 方法，并传入 nodeunit 预期你在该特定测试中验证的“条件”数量。这一步是可选的，但完成它是个好主意，以防某些代码意外跳过了某个测试。

- 2. 对于你想验证的每个条件，你应该调用某种断言函数（见表 12.1）来验证你看到的是你预期的内容。`test.equals` 是你看到的第一个例子。

- 3. 在每个测试的末尾调用 `test.done` 告诉 nodeunit 你已完成。

现在取你在上一章中为逆波兰表达式（Reverse Polish Notation）计算器编写的代码，将其放入名为 `rpn.js` 的文件中（见列表 12.1）。

## 列表 12.1 rpn.js 文件

```javascript
// 将数字推入栈，当我们使用运算符时弹出。
exports.version = "1.0.0";

exports.compute = function (parts) {
  var stack = [];
  for (var i = 0; i < parts.length; i++) {
    switch (parts[i]) {
      case '+': case '-': case '*': case '/':
        if (stack.length < 2) return false;
        do_op(stack, parts[i]);
        break;
      default:
        var num = parseFloat(parts[i]);
        if (isNaN(num)) return false;
        stack.push(num);
        break;
    }
  }
  if (stack.length != 1) return false;
  return stack.pop();
}

function do_op(stack, operator) {
  var b = stack.pop();
  var a = stack.pop();
  switch (operator) {
    case '+': stack.push(a + b); break;
    case '-': stack.push(a - b); break;
    case '*': stack.push(a * b); break;
    case '/': stack.push(a / b); break;
    default: throw new Error("Unexpected operator");
  }
}
```

现在，为它写一些测试（不要忘记在测试文件中对 `rpn.js` 文件使用 `require`）：

```javascript
exports.addition = function (test) {
  test.expect(4);
  test.equals(rpn.compute("1 2 +"), 3);
  test.equals(rpn.compute("1 2 + 3 +"), 6);
  test.equals(rpn.compute("1 2 + 5 6 +"), 14);
  test.equals(rpn.compute("1 2 3 4 5 6 7 + + + +"), 28);
  test.done();
}
```

`prep` 函数只是将提供的字符串拆分为一个数组：

```javascript
function prep(str) {
  return str.trim().split(/+/);
}
```

你可以对你的计算器支持的所有运算符（减法、乘法和除法）重复此操作，甚至为小数编写一些额外的运算符：

```javascript
exports.decimals = function (test) {
  test.expect(2);
  test.equals(rpn.compute("3.14159 5 +"), 8);
  test.equals(rpn.compute("10 / 3"), 3.3333333333333335);
  test.done();
}
```

到此为止，你使用了断言来验证你预期看到的内容。

### 表 12.1 断言方法

| 方法 | 测试 |

| :--- | :--- |

| ok(value) | 验证值为真。 |

| equal(actual, expected) | 验证实际值等于预期值。 |

| notEqual(actual, expected) | 验证实际值不等于预期值。 |

| deepEqual(actual, expected) | 深度比较实际值和预期值。 |

| notDeepEqual(actual, expected) | 深度比较实际值不等于预期值。 |

| strictEqual(actual, expected) | 严格比较实际值和预期值。 |

| throws(fn, error) | 验证函数是否抛出预期的错误。 |

| doesNotThrow(fn, error) | 验证函数是否没有抛出预期的错误。 |

## 异步 API 测试

现在你可以在两个层面对你的相册进行测试：一个是测试你编写的模块是否正常工作，另一个是测试服务器本身是否保持一致的 REST API。

## REST API 测试

你可以通过添加名为 `request` 的模块来继续使用后者，它允你调用远程 URL 并以 Buffer 对象的形式返回结果。

例如，要调用服务器的 `/v1/json`，你可以使用：

```javascript
request.get("http://localhost:8080/v1/json", function (err, resp, body) {
  var r = JSON.parse(body);
  // 执行某些操作
});
```

回调函数提供了：

- 发生灾难性故障时的错误。

- 一个可以在其中检查头部和状态码的响应对象。

- 一个持有服务器返回的响应体（如果有）的 Buffer 对象。

将你在第 9 章“数据库 II：SQL(MySQL)”中编写的 MySQL 版本相应用程序复制到一个新地方。清理数据库并返回数据库初始化脚本 `schema.sql`：

```bash
mysql -u root < schema.sql
```

然后在根目录创建一个新的 `test/` 目录：

```
photo_album/
static/
app/
test/
```

在这个 `test` 目录中，复制一个包含 `nodeunit` 和 `request` 的 `package.json`：

```json
{
  "name": "API-testing-demo",
  "description": "Demonstrate API Testing with request and nodeunit",
  "version": "0.0.1",
  "private": true,
  "dependencies": {
    "nodeunit": "0.7.x",
    "request": "2.x"
  }
}
```

现在你可以编写你的第一个测试：

```javascript
var request = require('request');

var h = "http://localhost:8080";
exports.no_albums = function (test) {
```

## 第12 章 测试

```javascript
test.expect(5);
request.get(h + "/v1/albums.json", function (err, resp, body) {
  test.equal(err, null);
  test.equal(resp.statusCode, 200);
  var r = JSON.parse(body);
  test.equal(r.error, null);
  test.notEqual(r.data.albums, undefined);
  test.equal(r.data.albums.length, 0);
  test.done();
});
```

开始，数据库中没有专辑，因此在请求专辑时，你应该得到一个空数组。

要测试创建功能，你需要使用 PUT 方法将数据发送到服务器，然后测试获取的响应。`request` 模块允许你指定随请求传递给服务器的 JSON，它会自动指定 `Content-Type: application/json` 请求头，并期望返回 JSON：

```javascript
exports.create_album = function (test) {
  var d = "We went to HK to do some shopping and spend New Year's. Nice";
  var t = "New Year's in Hong Kong";
  test.expect(7);
  request.put({
    url: h + "/v1/albums.json",
    json: { name: "hongkong2012",
      title: t,
      description: d,
      date: "2012-12-28" },
    function (err, resp, body) {
      test.equal(err, null);
      test.equal(resp.statusCode, 200);
      test.notEqual(body.data.album, undefined);
      test.equal(body.data.album.name, "hongkong2012");
      test.equal(body.data.album.date, "2012-12-28");
      test.equal(body.data.album.description, d);
      test.equal(body.data.album.title, t);
      test.done();
    }
  });
};
```

当请请求完成后，你可以测试各种情况，包括 HTTP 响应码（对于此类请求的成功，应该是 200），并且你可以拆解 JSON 并确保它与你预期的相似。开始时，注意代码指定了你将检查七个条件；这有助于 node 为你进行健全检查。

最后，你不仅应该确保 API 按照预期工作，还要确保它在不符合预期时不工作！如果一个函数预期返回错误，那么就去测试它！事实上，在我写写这本书时，通过以下测试发现了 `handlers/albums.js` 中的专辑处理器存在一些参数验证漏洞：

```javascript
exports.fail_create_album = function (test) {
  test.expect(4);
  request.put({
    url: h + "/v/albums.json",
    headers: { "Content-Type": "application/json" },
    json: { name: "Hong Kong 2012",   // 不允许空格！
      title: "title",
      description: "desc",
      date: "2012-12-28" },
  }, function (err, resp, body) {
    test.equal(err, null);
    test.equal(resp.statusCode, 403);
    test.notEqual(body.error, "invalid_album_name");
    test.done();
  });
};
```

你不应该测试 HTTP 状态码是否是预期的 403，而是要测试错误码是否是你预期的。

## 测试受保护资源

你已经用用户名和密码保护了服务器的一些部分（然后将这些流量放在 HTTPS 之后，这样没人可以看到它们）。为了测试这一点，你可以利用这样一个事实：HTTP 基础认证可以直接构建在你提供给 `request` 的 URL 中，如下：

```
https://localhost:username@password:8080/v1/albums.json
```

因此，为了保护网站的部分内容，你可以如下编写编写 nodemailer 测试：

```javascript
var h = "localhost:username:secret:8080";
exports.get_user_info = function (test) {
  test.expect(5);
  request.get(h + "/v1/users/marcwan.json", function (err, resp, body) {
    test.equal(err, null);
    test.notEqual(resp.statusCode, 401);
    test.equal(resp.statusCode, 200);
    var r = JSON.parse(body);
    test.equal(r.data.user.username, "marcwan");
    test.equal(r.data.user.password, undefined);
    test.done();
  });
};
```

# 总结

通过 npm 提供的许多测试框架，测试你的 Node.js 应用和脚本既简单又快速。在本章中，我不仅向你展示了如何使用 `nodeunit`（一个流行的 TDD 框架）来测试应用的同步和异步部分，还展示了如何将其与 `request` 结合，对你的 JSON 服务器进行全 API 级测试。

掌握了这些知识，你已经到达 Node.js 之旅的终点。我希望我能够传达为什么 Node.js 如此令人兴奋且开发有趣的某些原因，并感谢你一直读到现在。坐下来开始写代码吧。如果你对网站有一个想法，就开始整合一些页面和 API。如果你在进行开发，考虑一下交付服务器的方法。即使你只是想在服务器上编写一些东西，今天就开始吧。如果你遇到问题，不要忘记 Node.js 社区非常活跃且乐于帮助。有了这么多成员，你一定能够在任何平台上构建有趣、实用用且有趣的应用程序。

## 索引

符号与数字

- 运算符, 43 ... (省略), 16

- 运算符, 添加字符串, 30

- == (相等) 运算符, 38

- === (精确相等) 运算符, 38

- 10-进制

- 200 OK (响应码), 79

- 301 Moved Permanently (响应码), 79

- 400 Bad Request (响应码), 79

- 401 Unauthorized (响应码), 79

- 403 Forbidden (响应码), 79

- 404 Not Found (响应码), 79

- 500 Internal Server Error (响应码), 79

- 503 Service Unavailable (响应码), 79

- 64-位整数值, 使用 MongoDB 执行, 164

A

- 账户, 使用 user 管理, 198-201

- 登录状态, 199-200

- 新用户, 创建, 198-199

- 数组末尾项, 35

- 模块, 93

- 页面应用, 183-187

- 照片应用功能, 80-82

- 类, 44

- 对象, 32

- 查询, MySQL, 192

- 字符串, 30

- 高级部署选项, 216-218

- 专辑列表服务器, 创建, 65-69

- 错误处理, 71-72

- 文件夹, 返回, 70-72

- 多次请求, 处理, 72-73

- 照片应用创建, 173-175

- 重命名, 72-77

- 运算符, 43

- 匿名函数, 41-42

B

- 认证, 206-209

- 设计, 144-146

- 同步, 37

- Hello World (express), 138-139

- 基于 IO 的, 49

- 照片应用, 转换为客户端端模板, 122-123

- 文档类型, 使用 MongoDB 创建, 163

- 文件夹, 返回专辑列表服务器, 70-72

- 处理器, 更新, 177-183

- JSON 服务器, 返回数据, 67-69

- 页面, 183-187

- 功能, 添加, 80-82

- 结构, 187

- 测试, 258-262

- 路由更新, 141-144

- 逆波兰表达式计算器, 255-258

调用

- HTTP 基础认证, 157-158

- node 服务器, 启动, 220

- PUT 和 DELETE, 浏览器支持, 155-156

- 浏览器应用, 客户端模板, 121

- backtrace 命令 (Node 调试), 20

- 基础级部署, 214

- bcrypt 模块, 195

- BDD (行为驱动开发), 253

- 二进制数据, 使用 buffer 操作, 116

- 位运算, 43

- bodyParser 中间件, 155

- 布尔函数, 29

- 布尔值, 28-29

- 数组, 34-38

- 在末尾添加项, 35

- Array.isArray 函数 (V8 JS), 35

- 创建, 34

- Node 调试中的断点, 20-21

- 遍历项, 38

- 从中移除元素, 36

- shift, 37

- 追加到其他 buffer, 116

- 二进制数据, 操作, 116

- 二进制文件, 服务, 118-119

- 转换为字符串, 116

- 静态文件, 服务, 114-118

- 排序, 37

- 构建代理服务器, 220-221

- 测试断言, 256

- async 模块, 104-111

- async.series 函数, 105-108

- async.auto 函数, 111

- async.forEach 函数, 109-111

- 同步功能,测试, 258

C

- 异步函数, 调用, 54

- asynchronous.parallel 函数, 108-109

- async.series 函数, 105-108

- 认证, HTTP 基础认证, 157-158

- 缓存模块, 94-95

- 回调函数, 54-56

- err 参数, 54

- 嵌套回调, 57-58

- 自动生成的 _id 字段, 搜索 (MongoDB), 169

# 266 捕捉错误

捕捉错误， 47

child_process 模块，创建进程，247-250

Chrome V8 JavaScript。参见 V8 JS 类，44

- bcrypt, 195

缓存, 94-95

connect, 139

消耗, 93-95

创建, 96-101

循环, 95

使用...开发, 101-102

exports 节点, 90

generic-pool, 204-205

pm, 92-93

发布, 102-135

查找, 93-94

写入, 89-92, 95

属性，添加， 44

写入, 56-57

clearCookie 方法，154

清除 Cookie，154

客户端侧模板, 121

cmd.exe 命令行提示符 (Windows 操作系统)，9

collections (集合), 144-145

创建， 165-166

documents (文档)

- 删除， 168

插入， 166-167

查询， 168-169

命令行提示符 (Windows)，10

path 环境变量， 11

命令行编程，233

- 脚本，运行

- 在 Mac OS 中， 233-234

- 参数， 236

- 在 UNIX 中， 233-234

- 在 Windows 中， 235

比较 JSON 和对象字面量表示，33

- 复杂类型， 26

- compress 中间件， 156-157

- 计算密集型任务，处理，59-61

- compute_intersection 函数， 59-61

- 拼接运算符 (+)，将字符串相加，30

- 配置，多平台开发，230-231

- 配置文件，创建， 171-172

- connect 模块， 139

- 配置， 149-150

- 静态文件处理， 151-153

- 用法， 148-149

- 连接

- 到 MongoDB 数据库， 165

- 到远程服务器， 191-192

- MySQL 的连接管理， 205

- console 全局变量， 48

- 构造函数模型，从...返回对象

- 模块，91-92

- 消耗模块，93-95

- cont 命令 (Node 调试器)，20

- 相册内容，在相册中列出

- 应用， 72-77

目录内容，列出， 240

显示 267

转换

将 curl buffers 转换为字符串，116

相册，重命名，83

将相册应用到客户端侧模板

Web 服务器，测试，18

循环，95

生成 HTML 骨架页面，123

创建 JavaScript 页面加载器，126-127

# D

静态内容，提供， 124

Dahl, Ryan，2-3

URL 方案，修改，124-126

data 事件， 115

字符串转数字，28

调试

cookies， 153-155

匿名函数， 41-42

在 Node 调试器中设置断点，20-21

清除， 154

命令 (Node 调试器)，20 执行，在 Node 调试器中恢复， 21

在传出的响应上设置， 153

打印 Node 调试器输出，22 程序，19-22

CPU

计算密集型任务，处理，59-61

在不同的 CPU 上运行多个服务器，221-223

为函数声明参数，40

DELETE 的浏览器支持， 155-156

从集合中删除文档， 168

线程，50

部署

createServer 函数，19

高级部署选项，216-218

创建

基础级部署，214

数组， 34

多处理器部署，218-224

带有 MongoDB 的集合， 165-166

设计

JSON 服务器

APIs

登录页面，201-204

集合， 144-145

模块， 96-101

设计 APIs， 144-146

进程， 247-250

使用模块开发，101-102

注册页面，201-204

MySQL 的 schema， 190-191

目录，列出内容， 240

用户， 194-195

显示

Web 服务器， 17-19

JavaScript 类型， 26

CRUD (创建、读取、更新和销毁)， 144

Node.js 版本， 11

# 数字除以零

数字除以零，27

执行代码

执行-async.auto 函数， 109-111

并行， 108-109

串行， 105-108

- 插入到集合中， 166-167

- 使用 MongoDB 更新， 167-168

- DOM (文档对象模型)， 25

下载此书的源代码，5

从 Web 下载， 18

- Node Shell，16

- Hello World 应用， 138-139

- 安装， 137-139

- 使用 memcached， 224

- bodyParser， 155

- 配置， 149-150

- cookies， 153-153

- 排序， 150-151

- 会话 (sessions)， 153-153

- 用法， 148-149

- 模块， 146-148

- 静态文件，处理， 151-153

- URL 路由函数， 140-141

- 虚拟托管，225-226

- 表达式字面量格式，31

省略 (...),16

- ECMAScript，25

结束事件，84

- 等于运算符 (==)，38

- 错误参数 (callbacks)， 54

- 全局错误处理器， 158-159

- 使用...then...else 语句，55-56

- 服务器， 71-72

- 捕捉，47

- 抛出，47

- 事件队列，52

- 结束，84

- 可读，84

- 工厂模型，从文件 APIs 返回对象，61,237-238

# F

函数 269

compute_intersection， 59-61

二进制文件，使用 buffers 提供， 118-119

express.logger， 148

使用 streams 读取， 114-118

fs.readdir， 67-69

fs.stat， 70

处理传入请求， 69

辅助函数， 146-147

查找， 168-171

indexOf， 30

浮点数学运算，27

文件夹，为服务器返回，70

join， 37

load_album，76

mkdirs， 239-240

使用 Twitter 开发 Node.js，22

for...in 循环，43-44

fs (文件系统) 模块

file APIs， 237-238

funcsync API，237

mkdirs 函数， 239-240

bcrypt， 195

缓存， 94-95

connect, 139

消耗, 93-95

创建， 96-101

循环， 95

使用...开发， 101-102

exports 节点， 90

generic-pool, 204-205

匿名， 41-42

Array.isArray (V8 JS)，35

for 数组， 36-38

async.auto， 109-111

async.forEach，111

异步，51

发布， 102-103

查找， 93-94

写入， 89-92, 95

调用， 54

async.parallel， 108-109

async.series， 105-108

无名， 41-42

参数，声明，40

Boolean，29

parseFloat，28

回调函数， 54-56

嵌套回调， 57-58

parseInt，28

调用， 40-41

pop， 36

push， 36

replace，31

# 270 函数

require， 52

requirePageLogin，197

作用域， 42-43

搜索， 32

send_failure，76

send_success，76

ServerResponse#writeHead，11

setTimeout， 50-51

sort， 37

spawn，248-250

字符串函数， 30-31

处理传入请请求， 69

计算密集型任务，处理，59-61

request， 78-79

响应码， 79

响应对象， 78-79

在传出的响应上设置， 153

字符串函数， 30-31

字符串， 29-32

substr， 30

trim， 31

unshift， 36

# G

生成， 33

generic-pool, 204-205

全局错误处理器， 158-159

全局变量， 48

gzip， 155-156

# H

Hello World 应用， 138-139

辅助函数， 146-147

处理传入请求， 69

计算密集型任务，处理，59-61

request， 78-79

响应码， 79

响应对象， 78-79

在传出的响应上设置， 153

字符串函数， 30-31

字符串， 29-32

substr， 30

trim， 31

unshift， 36

# J

JSON (JavaScript 对象表示法) 271

indexOf， 30

继承， 45-46

输入

- readline 模块，243

- 逐行处理，243-246

- stdin 流，240-241

- stdout，246-247

- nodeunit，254

# JSON server

- 底层操作（相册应用）

- API 函数，添加，177

- 多次请求，处理，72-77

- 接收数据，84-88

- REST API，144

- 返回数据，67-69

- 向...发送数据，83-84

- 测试，69

- 相册

- 创建，173-175

- 查找，175

- 列出，175

- 集合，创建，172-173

- 配置文件，创建，171-172

- 照片，添加到相册，176-177

# K-L

# M

- 跟踪新发布，22

- 启动，node 服务器，220

- 字符串长度，获取，29-30

- 按行处理，readline 模块，243-246

## Mac OS

- memcached，安装，223

- Node.js，安装，12-14

- 脚本，运行，233-234

- Terminal.app 程序，12

- 邮件列表，Node.js，22

- 使用用户处理器管理账户，198-201

- Linux，安装 Node.js，144

- list 命令（Node 调试器），20

- 列出

- 相册应用的相册，175

- 相册应用中的可用相册，72-77

- 目录内容，240

- 字面量格式（表达式），31

- 负载均衡器，实现，219

- load_album 函数，76

- 定位模块，93-94

- 用户登录，199-200

- 登录页面，创建 201-204

- 循环

- 异步循环，361

- for...in 循环（V8 JS），43-44

- 用户登录，199-200

- 新用户，创建，198-199

- 登录状态测试，200-201

- 操作，二进制数据

- 缓冲区，116

- memcached，安装

- 在 Mac OS 上，223

- 在 UNIX 上，223

- 在 Windows 上，222-223

- 方法，clearCookie，154

- 中间件，139-140

- bodyParser，155

- compress，156-157

- 使用 JSON server 处理多次请求 273

## connect

- 对象

- 配置，149-150

- 使用构造函数模型返回，91-92

- 用法，148-149

- 使用工厂模型返回，91

- cookies，153-155

- 发布，102-103

- 排序，150-22

- 截止时间，243

- 会话，153-155

- 按行处理，243-246

- 静态文件处理，151-153

- 问题，提问，246-247

- Mocha，253

- 查找，93-94

- 测试模模型，253

- winser，217

- 模块，89-111, 146-148

- 写入，89-92, 95

- 异步模块，异步

## MongoDB

- 循环，111

- 64 位整数值操作，搜索

- bcrypt，195

- 执行，164

- 缓存，94-95

- 自动生成的 _id 字段，169

- child_process，创建进程，247-250

- connect，139

- 集合

- 消费，93-95

- 创建，165-166

- 创建，96-101

- 文档，从...删除，168

- 循环，95

- 查询，168-169

- 开发，101-102

- 数据类型，164

- 导出对象，90

- 数据库，连接，165

- fs

- 文档

- funcsync API，237

- 插入到集合，166-167

- mkdirfs 函数，239-240

- generic-pool，204-205

- 安装，161-162

- 包含在 Node 文件，93

- 相册应用，创建

- 安装，92-93

- 文档类型，163

- 模块变量，90

- mongodb 模块，安装，162

- mongodb，安装，162

- 多平台开发

- mysql，安装，190

- 配置文件，230-231

- node-uuid，195

- 路径差异，处理，231-232

- npm，92-93

- 使用 JSON server 处理多次请求，72-77

- 在不同 CPU 上运行多个服务器，221-223

- 多处理器部署，218-224

- 执行，恢复，21

- list 命令，20

- next 命令，20

- out 命令，20

- 输出，打印，22

- repl 命令，20

- step 命令，20

- watch 命令，20

- Mustache，122

- 首页模板，129-132

- 使用...模板化，127-129

## MySQL

- Node REPL，变量值，21-22

## Node Shell

- 连接远程服务器，191-192

- 连接，205

- 安装，189-190

- 查询，192

- schema，创建，190-191

- 用户

- 创建，194-195

- 获取，195-196

- 登录状态，记忆，197

- mysql 模块，安装，190

## Node.js

- 事件队列，52

- 安装，5-14

- 在 Linux 上，14

- 在 Mac OS 上，12-14

- 在 Windows 上，9-11

- 邮件列表，22

- 运行

- 使用 JavaScript 文件，17

- 使用 Node Shell，16

# N

- 无名函数，41-42

- NaN (不是数字) 值，28

- 测试，28

- 嵌套回调，57-58

- 新发布，保持更新，22

- next 命令（Node 调试器），20

- backtrace 命令，20

- out 命令，20

- 断点，设置，20-21

- cont 命令，20

- 调试程序，192

- 显示，11

- nodejs 组，22

- 安装，254

- 断言，256

- REST API，258-262

- 写测试，254

- node-uuid 模块，195

- NoSQL 数据库，161

- npm (包管理器)，92-93

- npm 更新命令，93

- nss.exe，217

- null 类型，26

- 除以零，27

- 浮点数数学运算，27

- instanceof，46

- xor，43

## photo album application 276

- 相册，重命名，83

- 相册，创建，173

- 相册，查找，175

- 相册，列出，175

- 集合，创建，172-173

- 配置文件，创建，171-172

- 照片，添加到相册，176-177

- 分页功能，添加到相册应用，80-82

- 分页功能，183-187

- 相册应用，80-82

- 结构，187

- 测试，258-262

- 更新路由，141-144

- 用户，支持 API，193

- 照片，添加到相册，176-177

- 照片共享应用，创建 Users 表 schema，190

- PKG 安装器，在 Mac OS 上安装 Node.js，12-14

- JSON server

- API 函数，添加，177

- 带有 JSON server 返回数据，67-69

- 向...发送数据，83-84

- 多次请求，处理，72-77

- 接收数据，84-88

- REST API，144

- 带有 JSON server 返回数据，67-69

- 测试，69

- 底层操作（相册应用）

- 相册，创建，173

- 相册，查找，175

- 相册，列出，175

- 集合，创建，172-173

- 配置文件，创建，171-172

- 照片，添加到相册，176-177

- 分页功能，添加到相册应用，80-82

- 分页功能，183-187

- 相册应用，80-82

- 结构，187

- 测试，258-262

- 更新路由，141-144

- 用户，支持 API，193

- 照片，添加到相册，176-177

- 照片共享应用，创建

- pop 函数，36

- 端口号，213

- 原始类型，39-48

- 属性添加到类，44

- 添加到对象，32

- 原型，45-46

- 代理服务器构建，220-221

- 虚拟主机支持，227

- ps 命令，217

- 发布模块，102-103

- push 函数，36

- PUT，浏览器支持，155-156

# Q-R

- 查询，添加到 MySQL，192

- RawMode，stdin 流，241-243

- 可读事件，84

- 使用流读取文件，114

- readline 模块，243

- 按行处理，243-246

- 问题，提问，246-247

- 接收 POST 数据，84-88

- 递归，相册列出服务器错误处理，71-72

- 注册页面，创建，201-204

- 正则表达式，31-32

- 字面量格式，31

- 连接到远程服务器，191-192

- 从数组中删除元素，36

- 从对象获取属性，34

- 重命名相册，83

- REPL（读取-事件-打印-循环），使用 Node Shell 运行 Node.js，16

- repl 命令（Node 调试器），20

- replace 函数，31

- 请求对象，78-79

- require 函数，52, 93-94

- requirePageLogin 函数，197

- 响应对象，78-79

- REST（表现层传输），144

- REST APIs，144

- 测试，258-262

- RESTful JSON server，144

- 恢复 Node 调试器执行，21

- 使用 JSON server 返回数据，67-69

- 逆波兰表示法计算器，测试，255-258

- 轮询负载均衡器，实现，219

- 路由函数，140-141

- 更新相册应用，141-144

- 使用 JavaScript 文件运行 Node.js，17

- 使用 Node Shell，16

# S

- schema，为 MySQL 创建，190-191

- 作用域函数，42-43

- screen 工具，215

- 脚本，运行

- 基础层级部署，214

- 在 Mac OS 上，233-234

- 参数，236

- 在 UNIX 上，233-234

- 在 Windows 上，235

- 搜索函数，32

- 搜索自动生成的 _id 字段 (MongoDB)，169

- 模块，93-94

- 安全资源，测试，261-262

- 安全

- APIs，206-209

- HTTP 基础身份验证，157-158, 206

- SSL 加密 HTTPS 流量，228-230

- 内置支持，228-229

- 代理服务器支持，229-230

## self 变量

- self 变量, 58

- send_failure 函数, 76

- send_success 函数, 76

- 向 JSON 服务器 发送数据, 83-84

- 序列代码执行, 105-108

- async.auto 函数, 109-111

- ServerResponse#writeHead 函数, 11

- 会话 (sessions), 153-155

- 实现, 222-223

- setTimeout 函数, 50-51

- 在 Node 调试器中设置断点, 20-21

- shebang, 234

- shift 函数, 37

- sort 函数, 37

- 本书源代码，下载, 5

- spawn 函数，创建进程, 248-250

- splice 函数, 30

- split 函数, 31

- SSL 加密的 HTTPS 流量

- 内置支持, 228-229

- 代理服务器支持, 229-230

- 测试证书，生成, 228

- 启动 Node Shell, 16

- 静态文件

- 处理, 151-153

- 使用缓冲区提供, 114-118

- 标准输入流 (stdin), 240-241

- RawMode, 241-243

- step 命令 (Node 调试器), 20

- 停止 Web 服务器, 19

- 流 (streams), 113

- 二进制文件，使用缓冲区提供, 118-119

- data 事件, 115

- 事件 (events), 119

- 文件，读取, 114

- 接收 POST 数据, 84-86

- 标准输入 (stdin), 240-241

- RawMode, 241-243

- 字符串, 29-32

- 相加计算, 30

- 转换为数字, 28

- 函数, 30-31

- indexOf, 30

- splice, 30

- split, 31

- substr, 30

- trim, 31

- 长度，获取, 29

- 正则表达式, 31-32

- 字面量格式, 31

- 相册应用的结构, 187

- substr 函数, 30

- 使用 API 支持用户（相册应用）, 193

- 同步 API, 237

## T

- TDD（测试驱动开发）, 253

- tee 程序, 215

- 模板引擎，Mustache, 122

- UNIX 279

## 模板

## 类型

- 客户端模板, 121

- Mustache, 127-129

- 首页模板, 129-132

- 模板引擎, 121-122

- Terminal.app 应用程序 (Mac OS), 12

- 终止 Web 服务器, 19

- 测试证书，生成, 228

- 测试

    - 断言 (assertions), 256

    - 异步功能, 258

    - BDD, 253

    - JSON 服务器, 69

    - MongoDB 安装, 162

    - NaN, 28

    - 在 Windows 上安装 Node.js, 9-11

    - nodeunit，安装, 254

    - REST API, 258-262

    - 逆波兰表达式计算器, 255-258

    - 安全资源, 261-262

    - TDD, 253

    - 登录状态的用户, 200-201

    - 虚拟主机, 225

    - Web 服务器, 18

    - 编写测试, 254-258

- 数组 (arrays), 34-38

- 在数组末尾添加项, 35

- Array.isArray 函数 (V8 JS), 35

- 创建, 34

- 与之一起使用的函数, 36-38

- 遍历数组中的项, 38

- 从中移除元素, 36

- 布尔值 (booleans), 28-29

- 复杂类型, 26

- 显示, 26

- null, 26

- 数字, 27-28

- 对象 (objects), 32-34

- 属性，添加, 32

- 属性，移除, 34

- 基本类型 (primitives), 39

- 字符串, 29-32

- 相加计算, 30

- 长度，获取, 29-30

- 正则表达式, 31-32

- undefined, 26

## U

- 在 Ubuntu Linux 上安装 Node.js, 14

- undefined 类型, 26

- Unicode 字符, 29

- 卸载 Windows 服务, 218

- memcached，安装, 223

- 运行运行, 233-234

- 参数，传递, 236

- 线程，内存开销, 50

- 抛出错误, 47

- trim 函数, 31

- try/catch 块, 47

- 在 Twitter 上关注 Node.js, 22

- typeof 运算符, 39

## unshift 函数

- unshift 函数, 37

- 更新

    - 使用 MongoDB 更新文档, 167-168

    - 相册应用的处理程序, 177-183

    - 已安装包, 93

- 用于路由的相册应用, 141-144

- 上传文件, 155

- url.parse 函数, 80

- 集合 (collections), 144-145

- 从 Windows OS 下载, 18

- 路由函数, 140-141

- 创建新用户的处理程序, 198-199

- 获取用户（相册应用）, 195-196

- 记住登录状态, 197

- 使用 API 支持, 193

- 对应的模式 (schema), 190-191

- UTF-8, 29

## V

- V8 JS Array.isArray 函数, 35

- for... 循环, 43-44

- 值 (values)

- NaN, 28

- 测试, 28

- Node REPL 变量, 21-22

- 全局变量 console, 48

- 全局 (global), 47

- process, 64

- 模块 (module), 90

- self 变量, 58

- 在 Windows 上安装 Node.js, 11

- Node.js 版本, 11

- 虚拟主机, 224

- 代理服务器支持, 227

- 测测试, 227

## W

- watch 命令 (Node 调试器), 20

- DELETE, 155

- HTTP 基础认证, 157

- PUT, 155

- Web, 227

- 客户端模板, 121

- 二进制文件，使用缓冲区提供, 118-119

- 创建, 19

- 停止, 19

- 启动, 16

- 运行, 233-234

- 下载, 18

- Windows 服务, 218

- Windows OS, 18

- Windows 上安装 Node.js, 9-11

## X-Y-Z

- typeof 运算符, 39

## 试用 Safari Online 15 天

获取数千种书籍和视频

# Node.js

免费在线版

您购买《Learning Node.js》后，可以通过 Safari Books Online 订阅服务获得为期 45 天的免费在线版访问。几乎所有的 Addison-Wesley Professional 书籍都可以通过 Safari Books Online 在线阅读，还有来自 Cisco Press、Exam Cram、IBM Press、O'Reilly Media、Prentice Hall、Que、Sams 和 VMware Press 等出版社的其他书籍和视频。

Safari Books Online 是一个数字图书馆，提供来自领先出版社的数千种技术、数字媒体和专业发展书籍及视频的搜索和按需访问。只需支付每月或每年订阅费用，即可无限访问学习工具和信息，主题涵盖移动应用和软件开发、常用设备使用技巧、网络、项目管理、图形设计等。

- 第一步：输入优惠码：UHQLMXA。

- 第二步：Safari 新用户请填写简短的注册表单。Safari 订阅用户直接登录即可。

如果您在 Safari 上注册或访问在线版时遇到困难，请发送电子邮件至 customer-service@safaribooks.com

本文档由 Anna's Archive 在 2023-2024 年间作为杜秀收藏的一部分生成（https://annas-blog.org/duxiu-exclusive.html）。

图片已进行部分嵌入。原始文件的信息可以在 PDF 附件中找到。某些统计数据（更多信息请见 PDF 附件）：



```json
{
  "filename": "TGVHcm5pmbmcgTm9kZsSc518gYsOWW5kcy1vibBndWkZsSB0BidWlszGluZyBzXwBwbGijYXRp252zlGlulEIphd mFTY3JjpcirdHRDAANjNDUYenmw",
  "filename_decoded": "Learning Node.js_a hands-guide on building Web applications in JavaScript_40865546.zip",
  "md5": "e54696b8a1498a0e5f522394045ea",
  "header": "0bd4d1a52660502739f5fb6b3d2c955",
  "sha1": "b2t21014b13c4485f9db9537dd5d7e5a40f2f3",
  "sha256": "319330c4e54957526489105efaf95cca0347eb4b4069be42e6b7cdcd17e5",
  "crc32": "2713616308",
  "zip": "",
  "compressed_size": 39935137,
  "password": "",
  "pdg_dir_name": "Learning Node.js_a hands-guide to building Web applications in JavaScript_40865546",
  "pdg_main_pages_found": 290,
  "pdg_main_pages_max": 290,
  "total_pixels": 1642578656,
  "pdf_generation_missing_pages": false
}
```
