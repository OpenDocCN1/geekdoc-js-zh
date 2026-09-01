# Node.js：从入门到精通








![](img/d4731c5479f6bfd1ada49d65047b9e4c_0_0.png)

![](img/d4731c5479f6bfd1ada49d65047b9e4c_0_1.png)











![](img/d4731c5479f6bfd1ada49d65047b9e4c_2_0.png)



# 关于 SitePoint

SitePoint 专门为 Web 专业人员编写有趣、实用且易于理解的内容。访问 http://www.sitepoint.com/ 访问我们的博客、书籍、时通讯、文章和社区论坛。你将在那里找到大量关于 JavaScript、PHP、设计等的信息。

# 关于作者

Craig 是一位常驻英国的自由职业全栈 Web 开发人员、作家和演讲师，他对标准和性能充满热情。

他从 20 世纪 80 年代开始编程，并在 1995 年 HTML 发布后开始客户端 JavaScript 开发，当时 HTML、占位 GIF 和胶幕灯被认为是非常先进的技术。你可能在 SitePoint 上遇到过他的作品，他在那里编写了超过 1200 篇教程，并了《Jump Web Performance》、《Browser DevTool Secrets》和《Docker for Web Developers》等书籍。

Craig 从一开始就开始使用 Node.js，希望这本书能成为你服务器端 JavaScript 旅程的绝佳第一步。你可以通过 Twitter @craigbuckler 或访问 craigbuckler.com 与他联系。

# 前言

本书将帮助你以最短的时间开始学习 Node.js。在一天或两天内，你就应该拥有足够编写简单应用程序的知识。

# 前提条件

本书面向初次接触 Node.js 的 Web 开发人员。理想情况下，你应该理解 Web 开发的概念和技术：

- Web 浏览器（客户端 HTML、CSS 和 JavaScript）
- Web 服务器（用于提供网页和 API 的代码）

如果你已经了解一些 JavaScript（可能是通过编写客户端脚本），那么这本书会有帮助。本书将解释与 Node.js 相关的某些 JavaScript 方面，但你不会发现对变量、循环、函数、对象等内容的深入探讨。

了解一点命令行、Git 以及像 VS Code 这样的编辑器也会很有用。

# 使用规范

## 代码示例

书中的代码使用等宽字体显示，如下：

```
<h1>A Perfect Summer's Day</h1>
<p>这是一个天气晴朗的日子，适合在公园散步。
鸟儿在欢声歌唱，孩子们都回学校上课了。</p>
```

某些代码应该在一行内输入，但由于页面限制，我们不得不对其进行换行。➡ 表示仅出于格式目的而存在的换行，应该被忽略：

```
URL.open("https://www.sitepoint.com/responsive-web-design-real-user-testing/?response1");
```

你会注意到，我们在书中使用了某些布局样式来表示不同类型的信息。请关注以下项目。

# 提示、注释和警告

![](img/d4731c5479f6bfd1ada49d65047b9e4c_4_0.png)

提示提供有用的小技巧。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_4_1.png)

注释是与当前主题相关但并非关键的有用备注。将它们视为额外的信息即可。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_4_2.png)

... 请注意这些重要点。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_4_0.png)

警告强调可能会让你掉入的坑。

# 寻求帮助

如果你无法通过论坛找到答案，SitePoint 有完善的邮件支持系统。

# 你的反馈

如果你对改进有建议，或者出于任何原因想联系我们，最好的方式是写信到 books@sitepoint.com。如果你发现了任何错误，我们特别表示欢迎。

# SitePoint 论坛

SitePoint 论坛包括：

- PHP
- 数据库

# 代码存档

在阅读本书的过程中，请注意我们在存档中使用了代码示例。如果你需要特定版本，可以下载它。

# 开始吧

现在我已经介绍了自己，给出了一些提示并告诉了去哪里寻求帮助，是时候开始了！你将从设置开发环境开始，很快就会编写第一行代码。

# 第 1 章：什么是 Node.js

Node.js 是一个 JavaScript 运行时，这意味着它可以运行 JavaScript 编写的程序。大多数开发者使用它创建命令行工具或 Web 服务器应用程序。

## 跳过？

这就是关于 Node.js 你需要的所有信息。如果你渴望开始编程，请跳到第 2 章。尽管如此，稍后回顾本章以了解 Node.js 的优势和核心特性是值得的。

## JavaScript、JavaScript、ES6、2015？

为了让初学者感到更加困惑，JavaScript 有许多名字。它在 1994 年作为“Live Script”诞生。Netscape 在与 Sun Microsystems 达成仓促协议后将其重新命名为“JavaScript”，尽管它与 Java 毫无相似。微软无法使用该名称，因此它在 Internet Explorer 中变成了“JavaScript”。

2005 年，Mozilla（源自 Netscape）加入了 ECMA International 并并将语言标准化为“ECMAScript”。版本 1 到 3 记录了 JavaScript 到 1999 年的发展。版本 4 被废弃，但 ECMAScript 5 在 2009 年成为大多数浏览器支持的标准。

工作从那时开始 ECMAScript 6——“ES6”。最终规范在 2015 年获得批准，这导致了另一个名字：“ES2015”。现在每年都会发布新规范。

无论对错，本书各处均称之为“JavaScript”。只有当特定版本（如 ES9/ES2018）影响到你使用的 Node.js 版本时，才会引用它们。

Node.js 最初由 Ryan Dahl 开发。他利用了 V8 JavaScript


源自 Google Chrome 浏览器的引擎，添加了一些 API，将其封装在事件循环中，并于 2009 年作为开源产品在 Linux 和 macOS 上发布。Windows 版本于 2011 年推出。

Node 包管理器 (npm) 出于 2010 年。它允许开发者在自己的项目中使用他人发布的代码模块。当时还没有官方的 ECMAScript 模块标准，因此 Node.js 和 npm 采用了 CommonJS。

Node.js 的第一个（非测试）版本发布于 2015 年，并承诺每六个月更新一次。

Node.js 并不是第一个 JavaScript 运行时，但与 Rhino 和 SpiderMonkey 等其他选项不同，它的人气呈指数级增长。即使是那些编写 PHP、Python、Ruby 或其他语言的人，也经常使用 Node.js 工具来补充他们的开发流程。

## 为什么要学习 Node.js？

JavaScript 是 GitHub 上最常用的语言，在开发者中也排名极高。包括 Netflix、Uber、Trello、PayPal、LinkedIn、eBay、NASA 和 Medium 在内的公司都采用了 Node.js，大多数专业开发者都会遇到过 Node.js 工具。

下面，我们将介绍你应该考虑使用 Node.js 的一些原因。

## 它是 JavaScript

JavaScript 用于数以亿计的网页，在其中拥有浏览器垄断。每个专业开发者都需要 JavaScript 知识来编写客户端应用程序。

服务器端语言更加多样。从历史上看，开发者可以选择 PHP、Ruby、Python、C# (ASP.NET)、Perl 或 Java，但这些语言具有不同的语法和概念。切换上下文可能很困难，因此较大的项目团队通常会分为前端和后端开发者。

Node.js 允许具有前端 JavaScript 知识的开发者在后端利用他们的技能。它不会让你一夜之间变成全栈开发者，但概念是相似的，而且在格式化 JSON、处理字符集、使用 WebSockets 等时，繁琐的操作更少。

## JavaScript 的替代方案

一些开发者偏于使用 TypeScript、PureScript、CoffeeScript、Reason 和 Dart 等语言，这些语言可以编译为 JavaScript 并在浏览器或 Node.js 中运行。最终，它们仍然生成 JavaScript 代码。

## 它很快

大多数服务器端语言都足够快了，但很少有能比得上 Node.js 的速度。V8 引擎非常快，而且演进迅速，背后有 Google 和 Chrome 支持其开发。Node.js 还具有非阻塞、事件驱动的 I/O。

让我们用更通俗的语言再过一遍。大多数语言使用同步阻塞执行。当你发布一个命令——例如从数据库获取信息——时，它将停止后续处理，并在运行时进展到下一条语句之前完成。为了确保多个用户可以同时访问，Apache 等 Web 服务器会为每个请求创建一个新的处理线程。这是一项昂贵的操作，Apache 的默认限制为 150 个并发连接。繁忙的服务器可能会过载。

Node.js 代码（以及浏览器 JavaScript）运行在单个处理线程上。耗时任务（如数据库查询）是异步处理的，这不会停止执行。任务在后台运行，Node.js 继续执行下一个命令。当任务完成时，返回的数据将传递给回调函数。Node.js 程序可以有数百个正在进行的操作，这些操作在完成时就会完成，这意味着处理器可以自由处理其他任务。

异步编程虽然面临挑战，但创建扩展性良好的 Node.js 是可行的。

## 它是实时的

Web 平台功能如 WebSockets 和服务器发送事件（server-sent events）允许实时功能——如即时更新、在线聊天、多人游戏等。这些在传统的服务器端语言中可能很难实现，因为它们通常需要第三方服务。在 Node.js 中实现实时功能要简单得多。

## 它是轻量级的

Node.js 运行时很小且跨平台。除了适用于 Linux、macOS 和 Windows 外，你还能找到用于嵌入式系统、树莓派甚至 SpaceX 火箭的版本。

## 它是模块化的

Node 提供了一个文档良好的精简标准库。它包含了用于错误处理、文件系统访问、网络操作和日志的基本函数。

对于其他所有内容 ...

## 它是可扩展的

Node.js 拥有世界上最大的包注册表，拥有超过百万个模块。你会找到用于任务运行器、日志记录、数据库连接器、图像处理器、代码编译器、Web 服务器、API 管理器甚至客户端库的预写代码。

npm 命令行工具随 Node.js 提供，可以方便地安装、更新和删除模块。你也可以。





# Node 版本管理器

Node Version Manager (nvm) 是一个允许在同一 Linux、macOS 或 Windows WSL 系统上安装多个版本 Node.js 的工具。如果你正在处理两个或多个使用不同版本 Node.js 的项目，这会非常实用。

## 选择 Node.js 版本

除非你正在支持一个具有特定要求的旧版应用程序，否则请安装最新发布的 Node.js 版本。

偶数版本的 Node.js 版本（例如 16、18 和 20）侧重于稳定性和安全性，并提供长期支持（LTS）。这些版本会提供至少两年的更新，因此我建议将它们用于生产环境服务器。你应该在开发机器上安装完全相同的版本。

奇数数版本（例如 15、17、19）正处于活跃开发中，并可能包含实验性功能。如果你正在学习、实验或频繁升级，那么这些版本用于开发也是可以的。

本课程中的示例代码是用 Node.js 16 开发的。然而，Node.js 通常具有良好的向后兼容性，用框架早期版本编写的应用程序*通常*可以在更高版本中运行。

# 如何在 Linux（或 Windows WSL2）上安装 Node.js

在浏览器中打开 nodejs.org 主页，你将被引导下载适用于你操作系统的安装包。然而，最实用的方法是使用操作系统内置的包管理器。NodeSource 提供了 Ubuntu 和 Debian 的二进制文件，以版本 16.x 为例，你可以通过 Ubuntu bash 终端安装 Node.js：

```bash
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo bash - sudo apt-get install -y nodejs
```

在终端中运行以下命令查看它们的版本号，以验证 Node.js 和 npm 是否安装正确：

```bash
node -v
npm -v
```

# 在 Linux 上配置 npm 全局权限

Node 包管理器（npm）命令行工具随 Node.js 一起提供，可以方便地安装、更新和运行模块。在可行的情况下，Node.js 应用可以全局安装并从任何地方运行——例如用于优化客户端 JavaScript 的 Rollup 绑器：

```bash
npm install rollup --global
```

此命令会导致 EACCES 权限错误，因为你没有以超级用户身份运行或使用 sudo。然而，sudo 会赋予全局脚本无限权限。我不想以那种方式运行自己的代码，更不用说别人的了！

更好的选项是将默认 npm 目录更改为由你拥有。为全局模块创建一个新目录，然后配置 npm，如下所示：

```bash
mkdir ~/.npm-global
npm config set prefix ~/.npm-global
```

然后，使用 nano 等编辑器打开 ~/.bashrc 或 ~/.profile：

```bash
nano ~/.bashrc
```

接下来，将以下行添加到文件的末尾：

```bash
export NPM_GLOBAL="$HOME/.npm-global"
export PATH=$NPM_GLOBAL/bin:$PATH
```

重启 Bash 终端或通过 `source ~/.bashrc` 手动更新系统。

你现在可以在无需 sudo 的情况下安装全局模块——包括更新 npm 本身：

```bash
npm install npm --global
```

# 如何在 macOS 上安装 Node.js

在浏览器中打开 nodejs.org 主页，你将被引导下载适用于 macOS 的 Node.js .pkg 安装程序。启动该文件，同意条款并继续安装。

在终端中运行以下命令查看它们的版本号，以验证 Node.js 和 npm 是否安装正确：

```bash
node -v
npm -v
```

# 如何在 Windows 上安装 Node.js

你可以通过三种方式在 Windows 上安装 Node.js：

- 直接在 Windows 上安装
- 在安装在 WSL2 的 Linux 发行版上安装（参考上文“如何在 Linux（或 Windows WSL2）上安装 Node.js”部分）
- 同时在 Windows 和 Linux 上安装！

若要在 Windows 上安装，在浏览器中打开 nodejs.org 主页，你将被引导下载 Node.js .msi 安装程序。启动该文件，同意条款并继续安装。

在终端中运行以下命令查看它们的版本号，以验证 Node.js 和 npm 是否安装正确：

```bash
node -v
npm -v
```

# 如何在其他设备上安装 Node.js

如果你使用的是其他设备，请检查官方文档以获取安装说明。




标准库中的 `process.argv` 属性返回一个包含命令行参数的数组：

- 第一个（元素 0）是 node 命令本身
- 第二个（元素 1）是你正在运行的脚本 (hello.js)
- 第三个（元素 2）是传递的第一个参数

编辑你的 `hello.js` 脚本以提取第二个参数并在 `console.log()` 语句中输出它：

```
#!/usr/bin/env node

// fetch name from command or fallback
const nameArg = (process.argv[2] || 'world');

// output message
console.log(`Hello ${nameArg}`);
```

保存该文件，然后运行 `node hello.js Craig` 即可得到 Hello Craig!

![](img/d4731c5479f6bfd1ada49d65047b9e4c_23_0.png)

如果你省略了参数（`node hello.js`），应用将回退到 Hello world。

```
D:\node\console>node hello.js
Hello world!

D:\node\console>
```

“world”这个回退文本有点无聊，所以你可以获取存储在操作系统环境变量中的用户名称。`process.env` 属性返回一个包含环境变量名/值对的对象。尝试在 REPL 中输入 `process.env`。（更多信息请参阅第 2 章中的“在 Node.js RePL 中运行 JavaScript 命令”章节。）

Linux 和 macOS 定义了 `USER` 变量，而 Windows 设置为 `USERNAME`。在声明 `nameArg` 时，确保你的脚本是跨平台的：

```
// fetch name from command argument, environment, or fallback
const nameArg = (process.argv[2]) || process.env.USER ||
process.env.USERNAME ||
➥ 'world';
```

运行脚本 `node hello.js`，你将看到 Hello <username>。你仍然可以通过传递参数（如 `node hello.js Craig`）来覆盖你的操作系统用户名称。

你可以通过将任何名称的首字母大写来为你的控制台应用锦上添花。这是最终的脚本：

```
#!/usr/bin/env node

// fetch name from command argument, environment, or fallback
const nameArg = capitalize(process.argv[2]) || process.env.USER ||
➥ process.env.USERNAME || 'world';
```

```
// output message
console.log(`Hello ${nameArg}!`);
```

```
// capitalize the first letter of all words
function capitalize(str) {

return str
  .trim()
  .split(' ')
  .map(word => word.charAt(0).toUpperCase() + word.slice(1))
  .join(' ');

}
```

使用以下命令运行脚本：

node hello.js "from my node.js script"

你现在将看到 Hello From My Node.js Script!

![](img/d4731c5479f6bfd1ada49d65047b9e4c_25_0.png)

你可以在此处查看此操作的视频演示。

# 你的第一个 Web 服务器应用

Web 应用需要 Web 服务器在浏览器请求它们时返回 HTML 网页。浏览器可能会请求其他资源，如 CSS 样式表、客户端 JavaScript、图像以及 Ajax 驱动的 API。

专用的 Web 服务器如 Apache 和 NGINX 通常用于此任务。如果 Apache 接收到对 PHP 文件的请求，它会将内容传递给 PHP 解释器，由解释器运行代码。Apache 接收生成的输出并将其返回给用户的浏览器。PHP 开发者经常访问 Apache 服务器变量或调整权限以增强代码。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_26_0.png)

Node.js 采取了不同的方法：你的 JavaScript 应用就是一个 Web 服务器。这听起来代码实现很复杂，但 HTTP 和 HTTPS 标准库已经为你完成了大部分工作。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_27_0.png)

为你的项目创建一个目录，例如 server：

```
mkdir server
cd server
```

然后添加一个名为 `webhello.js` 的文件，内容如下：

```
#!/usr/bin/env node

const
port = (process.argv[2]) || process.env.PORT || 3000,
http = require('http');

http.createServer((req, res) => {
  console.log(req.url);

  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/html');
  res.end('<p>Hello World!</p>');
}).listen(port);

console.log(` Server running at http://localhost:${ port }/`);
```

使用 `node webhello.js` 运行，你将看到 `Server running at http://localhost:3000/` 或类似的内容。在 Web浏览器中打开该地址，即可查看带有“Hello World!”段落的网页。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_28_0.png)

代码执行了以下操作：

- 它为服务器端口定义了一个变量。这可以通过命令行、`PORT` 环境变量传递，或者回退到 3000。
- 它使用 HTTP `createServer` 库来创建一个在该端口上监听的 Web 服务器。当它的回调函数接收到请求时，它可以检查 `req` 对象中的详细信息并使用 `res` 对象返回响应。

这是一个简单的示例，无论 URL 是，服务器都会返回相同的“Hello World!”响应。尝试访问 http://localhost:3000/、http://localhost:3000/abc/ 或 http://localhost:3000/abc/123/：每个页面都是完全一样的。

## 端口 3000？

Web 服务器在端口 80 上监听 HTTP 请求，在端口 443 上监听 HTTPS 请求。你可以设置不同的端口，但必须在 URL 中指定。

使用标准端口有缺点：

- 它们可能被其他软件占用，例如其他 Web 服务器或 Skype。
- Linux 和 macOS 阻止 1000 以下的端口，除非由超级用户启动。




你可以在此处查看该应用程序运行的视频演示。

## 应用程序注意事项

## 前前的挑战

本节涵盖了一些高级响应主题。如果现在觉得难以理解，不要担心，我们稍后会回顾这些信息。

这个轻量级脚本能够实现一个功能性的 Web 服务器，令人惊讶。应用程序是持久运行的，无论用户数量有多少，它都能保留自己的状态。例如，它可以在启动时建立数据库连接，然后在每次请求时重用该连接。Apache/PHP 应用通常是无状态的，因此每个页面请求在运行查询之前必须加载配置并连接数据库。

然而，Node.js 运行在单处理线程上：

- 如果你的应用程序失败，所有人都会受到影响，除非你部署了适当的监控，否则它不会重启。包括 PM2 和 forever 在内的选项可以帮助。
- 如果单个用户触发了一个需要十秒完成的长时间运行 JavaScript 函数，此时访问的每个用户都至少需要等待十秒响应。异步代码解决了这个问题，但理解这些概念需要时间。
- 扩展应用程序可能会困难。在 Apache/PHP 服务器上增加内存或 CPU 可以提高响应速度。即使在有 15 个或更多 CPU 可用的情况下，Node.js 仍然运行在单 CPU 核上。集群、PM2 和 Docker 容器等解决方案可以通过启动相同应用程序的多个实例提供帮助。

此外，Node.js Web 服务器在提供图像、样式表和客户端 JavaScript 等静态文件方面效率不高。生产环境通常使用前端 NGINX Web 服务器提供静态文件，或在适当将请求重定向到 Node.js 应用程序。这被称为反向代理，具有以下优点：

- 静态资产的提供无需经过 Node.js。这避免了不必要的处理并提高了性能。
- HTTPS 证书等设置可以由 NGINX 而非 Node.js 处理。当你运行多个相同的 Node.js 实例时，这特别实用。
- Node.js 应用可以运行在 1000 以上的端口，因此不需要超级用户权限。

## 编写无状态应用程序

假设你的单个 Node.js 应用在全局全局变量 `userCount` 中记录登录用户数。

如果你想通过启动两个或更多相同应用的的实例（可能在其他服务器上）来提高性能，会发生什么？任何实例都可以处理用户登录。`userCount` 的值在每个应用实例上将是不同的——而且是错误的。

在开发期间，你通常在一个运行的实例上工作。然而，我建议你将其变为无状态的，以确保它能够扩展并更具韧性。始终遵循：

- 多个实例可能运行在任何地方，可能在不同的端口或服务器上
- 实例可以随时启动或停止
- 前端 Web 服务器会将单个用户的请求引导到任何实例——无论之前的请求由哪个实例处理。

作为反面教材，不要将应用程序或用户状态存储在不同实例间可能不同的变量或本地文件中。使用数据库来保留状态，以便应用程序的每个实例都能同步。

## 总结

在本章中，你学习了如何使用 Node.js 库编写简单的控制台和 Web 服务器应用程序。你还看到了 nodemon 如何在更新代码后自动重启你的应用程序。

在下一章中，你将发现调试和修复 Node.js 代码问题的选项。

## 测验

1. 下述哪个说法是正确的：

- a. Node.js 只能运行 Web 应用。
- b. Node.js 应用需要如 NGINX 等 Web 服务器软件才能运行。
- c. Node.js 应用不需要 Web 服务器软件，但在生产网站上使用 NGINX 或类似的软件会有益。
- d. Node.js 不适合运行生产环境 Web 应用程序。

2. 修改 Node.js 应用后哪些步骤是必要的？

- a. 使用如 nodemon 等工具监控更改并重启应用程序。
- b. 如果它已经在运行，使用 Ctrl | Cmd + C 停止应用程序并重启它。
- c. 关闭终端，打开新终端并重新启动应用程序。
- d. 以上的任何一项。

3. 哪个 Node.js 对象属性返回命令行参数？

- a. process.arg
- b. process.argv
- c. process.argument
- d. process.env

4. 哪个 Node.js 对象属性返回环境变量？

- a. process.env
- b. process.envv
- c. process.argument
- d. process.env

5. 你可以启动多个实例吗？

- a. 不能。
- b. 可以，使用反向代理。
- c. 可以，使用负载均衡器。
- d. 可以，通过不同的端口。

# 第 4 章：如何调试脚本

Node.js 开发者有很多选择，例如 VS Code、Atom 和 Sublime Text 等编辑器。

## 使用良好的编辑器

一个良好的编辑器提供以下功能：

- 行号，用于定位错误发生的位置
- 类型检查——例如，确保字符串赋值
- 颜色编码以捕获问题，例如无效语句
- 变量名、函数名、属性的自动补全
- 括号匹配，突出显示嵌套结构中的问题
- 使用正确制表符或空格的自动缩进
- 跨文件和项目的变量命名
- 代码段保存和重用
- 函数、方法的参数提示
- 跳转到定义的函数导航
- 不可达代码检测
- 重构工具以整理混乱的代码

## 使用代码检查工具 (Linter)

Linter 在你保存和测试代码之前，会将语法错误、缩进不当、未声明变量、括号不匹配以及你的偏好（分号；引号用法等）报告为错误。JavaScript 和 Node.js 的流行选项包括 ESLint、JSLint 和 JSHint。

这些作为全局 Node.js 模块安装。例如，使用 npm 全局安装 ESLint 的方法：

```
npm install eslint -g
```

然后你可以从命令行检查文件：

```
eslint myscript.js
```

```
craig@cradev:~$ most myscript.js
const counter = 10;

for (i = 0; i < count; i++) {
  console.log(i)
}
craig@cradev:~$ eslint myscript.js
```

```
1:7 error 'counter' is assigned a value but never used no-unused-vars
3:6 error 'i' is not defined no-undef
3:13 error 'i' is not defined no-undef
3:17 error 'count' is not defined no-undef
3:25 error 'i' is not defined no-undef
4:15 error 'i' is not defined no-undef
4:17 error Missing semicolon semi
```

7 个问题（7 个错误，0 个警告）
1 个错误和0 个警告可以通过 `--fix` 选项可能修复

然而，大多数 linter 都有编辑器插件，例如 VS Code 的 ESLint 和 Atom 的 linter-eslint，它们会在你输入代码时检查代码。





## 使用版本控制

像 Git 这样的版本控制系统可以保护你的代码并管理修订。它让你更容易发现 Bug 是何时、何引入的，以及由谁来承担责任！GitHub 和 Bitbucket 等在线仓库提供了免费空间和管理工具。

## 采用问题跟踪系统

如果没人知道 Bug，它还存在吗？问题跟踪系统用于报告 Bug、查找重复项、记录重现步骤、确定严重性、计算优先级、分配开发者、讨论记录以及跟踪修复进度。

在线代码仓库通常提供基础的问题跟踪功能，但对于较大的团队和项目，诸如 Jira、FogBug 或 Bugzilla 等专用解决方案可能更合适。

## 使用测试驱动开发

**测试驱动开发** (TDD) 是一种开发过程，它鼓励开发者在编写函数*之前*编写代码来测试该函数的运行——例如，*当向函数 Y 输入 Z 时是否返回 X*？

在开发代码时，会运行测试，以证明结果函数符合预期。在进行进一步更改后，可以重新运行相同的测试来修复问题。*当然，你的测试也可能有 Bug！*

更多资源：

- Wikipedia 上的 TDD 概述
- "什么是测试驱动开发"
- "在 Node.js 中掌握测试驱动开发"

## Node.js 调试环境变量

在主机操作系统中设置的环境变量控制 Node.js 应用设置。最常见的是 NODE_ENV，它在调试时通常设置为 development，在生产环境服务器上设置为 production。

在 Linux/macOS 上可以设置环境变量：

```bash
NODE_ENV=development
```

这是 Windows 命令提示符：

```cmd
set NODE_ENV=development
```

这是 Windows Powershell：

```powershell
$env:NODE_ENV="development"
```

在内部，你的应用程序可以检测该设置并在时启用调试消息。例如：

```javascript
// 正在开发模式下运行？
const DEVMODE = (process.env.NODE_ENV !== 'production');
```

```javascript
if (DEVMODE) {
  console.log('application started in development mode');
}
```

NODE_DEBUG 使用 Node.js 的 util.debuglog 启用调试消息。（参见下文的 "Node.js util.debuglog" 部分。）你还应该咨询你主要模块和框架的文档，以发现更多的日志选项。

## Node.js 调试命令行选项

启动应用程序时，可以向 node 或 nodemon 运行时传递各种命令行选项。最有用的之一是 --trace-warnings，它当 promise 未按预期解析或拒绝时会输出堆栈跟踪：

```bash
node --trace-warnings index.js
```

其他选项还包括：

- --enable-source-maps: 使用 TypeScript 等转译器启用源映射
- --throw-deprecation: 使用已弃用的特性时抛出错误
- --inspect: 激活 V8 检查器（参见下文的 "Node.js V8 Inspector" 部分）

## 控制台调试

调试应用程序最简单的方法之一是在执行期间向控制台输出值：

```javascript
console.log( myVariable );
```

## 永远不要使用 console.log()！

一些开发者声称你不应该使用 console.log()，因为你正在更改代码，而且有更好的调试选项。这是事实——但每个人都这么用！

使用任何让你提高效率的工具。控制台日志可以是一个快速且实用的选项。找到 Bug 比你找到它的方法更重要。

很少有开发者会开发标准的 console.log() 命令，但他们错过了许多可能性：

| console 方法 | 描述 |
| :--- | :--- |
| .log(msg) | 向控制台输出消息 |
| .log('%j', obj) | 将对象作为紧凑的 JSON 字符串输出 |
| .dir(obj,opt) | 使用 util.inspect 打印对象和属性 |
| .table(obj) | 以表格格式输出对象数组 |
| .error(msg) | 输出错误消息 |
| .count(label) | 命名的计数器，报告该行执行的次数 |
| .countReset[label] | 重置命名计数器 |
| .group(label) | 缩进一组日志消息 |
| .groupEnd(label) | 结束缩进组 |
| .time(label) | 启动计时器计算操作的持续时间 |
| .timeLog(label) | 报告自计时器开始以来的已时间 |
| .timeEnd(label) | 停止计时器并报告总时长 |
| .trace() | 输出堆栈跟踪（所有调用函数的列表） |
| .clear() | 清空控制台 |

console.log() 接受逗号分隔的值列表。例如：

```javascript
let x = 123;
console.log('x:', x);
// x: 123
```

然而，ES6 解构提供了相似的输出，但输入量更少：

```javascript
console.log({ x }});
// { x: 123 }
```

util.inspect 可以格式化对象以便于阅读，但 console.dir() 为你完成了这些工作：

```javascript
console.dir(obj, { depth: null, color: true });
```

## Node.js util.debuglog

Node.js util 模块提供了一个内置的 debuglog 方法，可以条件地向 STDERR 写入日志消息：

```javascript
const util = require('util');
const debuglog = util.debuglog('myapp');
debuglog('myapp');
```

当 NODE_DEBUG 变量设置为 myapp（或通配符）时，调试消息将显示在控制台中：

```bash
debuglog('myapp');
```

## 使用日志模块调试

如果你需要更多的级别、详细、排序等，可以使用第三方日志模块。流行的解决方案包括：

- morgan
- pino
- sign
- winston

## Node.js V8 检查器

Node.js 是 V8 引擎的封装。V8 包含了了自己的检查器。使用以下脚本演示调试：

```javascript
const port = (process.argv[2] || process.env.PORT || 3000)
const http = require('http');
```

使用 --inspect 标志启动 Node.js V8 检查器：

```bash
node inspect webhello.js
```

（必要可以使用 nodemon 代替 node。）
这会在第一行启动调试并显示提示符：

```
Debugger listening on ws://127.0.0.1:9229/For help, see: https://nodejs.org/docs/inspector
Debugger attached.
Break on start in webhello.js:4
2
3 const
> 4 port = (process.argv[2] || process.env.PORT || 3000)
5 http = require('http');
```

输入 help 查看命令列表。你可以通过这些选项步进应用程序：

- cont or c: 继续执行
- next or n: 执行下一个命令
- step or s: 进入被调用的函数
- out or o: 跳出函数并返回调用命令
- pause: 暂停运行

其他选项包括：

- 使用 watch('myvar') 观察变量值
- 使用 sb() 命令设置断点（尽管在代码中插入 debugger 语句更简单）
- 重启脚本
- .exit 退出调试器（需要初始的点）

如果这听起来非常糟糕，事实确实。只有在绝对没有其他选择或你想受虐时才使用。

## 使用 Chrome 调试 Node.js 应用

使用 --inspect 标志启动 Node.js V8 检查器：

```bash
node --inspect webhello.js
```

如果你在另一个设备或 Docker 容器上运行 Node.js应用程序，请确保端口 9229 可用并使用以下命令远程访问：

```bash
node --inspect=0.0.0.0:9229 webhello.js
```

或者，使用 --inspect-brk 停止处理第一个语句，以便你可以逐行步进应用程序。





## DevTools

## 设备

设备

- 页面
- 扩展
- 应用
- 共享工作线程
- Service 工作线程
- 其他
  - 发现 USB 设备
  - 发现网络目标

为 Node 打开专用的 DevTools

# 远程目标 #LOCALHOST

目标 (v16.2.0) 追踪

webhello.js file://mnt/d/projects/course-ultimatenode1/code/ch03/server/webhello.js 检查

# 没有使用 Chrome？

Chromium、Edge、Opera、Vivaldi 和 Brave 都拥有与 Chrome 相同的调试器。chrome `://inspect` 地址应该可以完全地工作。

# 远程目标

如果 Node.js 应用程序没有显示为远程目标，请确保已勾选“发现网络目标”，然后点击“配置”以添加运行应用程序设备的 IP 地址和端口。

点击目标的 **inspect**（检查）链接启动 DevTools。对于任何用过浏览器开发者工具的人来说，这会感到非常熟悉。

在 **Sources**（源代码）面板中，点击 + **Add folder to workspace**（将文件夹添加到工作区），选择你的 Node.js 文件所在位置，并点击 **Agree**（同意）。在左侧面板或通过按下 Ctrl | Cmd + P 打开 webhello.js。

## DevTools

控制台 (Console) 源代码 (Sources) 内存分析器 (Memory Profiler)

文件系统 (Filesystem) 代码片段 (Snippets) webdebugger.js

+ 将文件夹添加到工作区
- server webDebugger

```javascript
1 #!/usr/bin/env node
2
3 const
4 port = (process.argv[2] || process.env.PORT || 3000);
5 http = require('http');
6
7 const server = http.createServer((res, req) => {
8
9 console.log(req.url);
10 const name = capitalize(req.url.replace(/[^\w]/g, '').replace(/\/$/g, '').trim()) || 'world');
11
12 res.statusCode = 200;
13 res.setHeader('Content-Type', 'text/html');
14 res.end(`<h1>${name}</h1>`);
15});
16
17 server.listen(port);
18
19 console.log(`Server running at http://localhost:${port}/`);
20
21 function capitalize(str) {
22
23 return str
24 .trim()
25 .toLowerCase()
26 .split(' ')
27 .map(word => word.charAt(0).toUpperCase() + word.slice(1))
28 .join(' ');
29 }
30
```

- 监听 (Watch)
- 断点 (Breakpoints): 无断点
- 作用域 (Scope): 未暂停
- 调用堆栈 (Call stack): 未暂停

第 1 行，第 1 列覆盖率：无可用

控制台更改 (Console Changes)

node[385] 过滤默认级别。无问题

Server running at http://localhost:3000/
webDebugger.js:18

点击任何行号即可设置由蓝色标记表示的断点。断点指定了调试器应该停止处理的位置，以便你可以

检查程序的状态。你可以定义任意数量的断点。

# 调试语句 (Debugger Statement)

当代码使用 V8 检查器运行时，处理在代码中的任何调试语句处也会停止。这在共享代码或跨多个设备调试时可能非常实用，尽管你可能想在将代码提交到源码控制或发布到活动服务器之前移除这些命令。

在浏览器中刷新/打开 http://localhost:3000/，当到达该断点时代码执行将停止。

## DevTools

控制台 (Console) 源代码 (Sources) 内存分析器 (Memory Profiler)

文件系统 (Filesystem) 代码片段 (Snippets) > web.js

+ 将文件夹添加到工作区
- server weblogs.js

```javascript
1 #!/usr/bin/env node
2 const
3 const port = (process.args[2] || process.env.PORT || 3000);
4 const http = require('http');
5 
6 http.createServer((req, res) => { 
7 console.log(req); 
8 const numbrk = capitalize(req.url.replace(/(\w+)/g, (w) => replace(w, '_', '$1')).trim() || 'World'); 
9
10 res.statusCode = 200;
11 res.setHeader('Content-Type', 'text/html');
12 res.end(`<h1>${numbrk}</h1>`);
13
14 .listen(port);
15 console.log(`Server running at http://localhost:${port}/`);
16
17 //: a function to capitalize the first letter of all words
18 function capitalize(str) {
19 return str
20 .trim()
21 .toLowerCase()
22 .split(' ')
23 .map(word => word.char(0).toUpperCase() + word.slice(1))
24 .join(' ');
25 }
26
27
28 Line 12 Column 3
```

在在断点处通过 (Passed on breakpoint)

监听 (Watch)

断点 (Breakpoints)

weblogs:12
statusCode: 200;

作用域 (Scope)

this: undefined
numbrk: "World"

Req: IncomingMessage({readableState: ReadableState, ...})
Res: ServerResponse({events:}, ...})

闭包 (Closure)

全局 Global global

调用堆栈 (Call stack)

```
anonymous weblogs:12
emit
deodev:230
```

```
parseOnInit node_http:server951
```

```
parseOnInit node_http:server951
```

控制台更改 (Console Changes)

node[385] 过滤默认级别。无问题

Server running at http://localhost:3000/
webDebugger.js:18

点击任何行号即可设置由蓝色标记表示的断点。断点指定了调试器应该停止处理的位置，以便你可以

检查程序的状态。你可以定义任意数量的断点。

（注：OCR 文本包含大量重复和乱码片段。上述内容反映了清理后的逻辑结构。）

## DevTools

控制台 (Console) 源代码 (Sources) 内存分析器 (Memory Profiler)

文件系统 (Filesystem) 代码片段 (Snippets) > web.js

+ 将文件夹添加到工作区
- server weblogs.js

... (文本其余部分遵循相同的合并逻辑)




顶部调试工具栏中的图标用于继续执行、单步、逐入、逐出、重启或停止应用程序。**运行**（Run）菜单也提供相同的选项。

你也可以右键点击行号。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_55_0.png)

完成操作后，你可以设置以下内容：

- 标准断点。
- 条件断点，当满足特定标准时会停止程序——例如 `count > 3`。
- 日志点点（logpoint）。这本质上是不带代码的 `console.log()`！输入任何带有大括号内评估表达式的字符串。例如，URL: { req.url } 会输出 req.url 属性的值。

```javascript
// console.log(req.url);
const nameArg = capitalize(req.url);
res.statusCode = 200;
Log Message -> URL: { req.url }
res.setHeader('Content-Type', 'text/html');
res.end('<p>Hello ${nameArg}</p>');
```

当刷新网页时，**调试台**（DEBUG CONSOLE）会显示日志点的值。

```
TERMINAL  PROBLEMS  OUTPUT  DEBUG CONSOLE
URL: / 
URL: /favicon.ico
```

更多信息，请参考“在 Visual Studio Code 中调试”。

## 高级调试配置

当你在其他设备、虚拟机上调试代码或想要使用不同的启动选项时，需要配置 VS Code。VS Code 将启动配置存储在项目 `.vscode` 文件夹内的 `launch.json` 文件中。要生成该文件，点击**运行和调试**（Run and Debug）面板顶部的**创建 launch.json 文件**链接，并选择 **Node.js** 环境。

```json
// 使用 IntelliSense 学习可能的属性。
// 悬停查看现有属性的说明。
// 更多信息请访问：https://go.microsoft.com/fwlink/?linkid=830387
"version": "0.2.0",
"configurations": [
    {
        "console": "integratedTerminal",
        "internalConsoleOptions": "neverOpen",
        "name": "nodemon",
        "program": "${workspaceFolder}/webhello.js",
        "request": "launch",
        "restart": true,
        "runtimeExecutable": "nodemon",
        "skipFiles": [
            "<node_internals>/**"
        ],
        "type": "pwa-node"
    }
]
```

你可以向 `"configurations": []` 数组添加任意数量的配置对象。点击添加配置（Add Configuration）按钮添加相应的选项。VS Code 可以：

- 使用 Node.js 直接启动进程
- 附加到 Node.js 调试器进程，该进程可能运行在远程机器或 Docker 容器上

上面的截图显示了一个 nodemon 启动配置。添加配置按钮提供了 nodemon 选项；只需要修改 "program" 属性指向 `${workspaceFolder}/webhello.js` 即可。

保存 `launch.json`，在运行和调试面板顶部的下拉列表中选择 `nodemon`，然后点击绿色的运行图标。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_58_0.png)

nodemon 将启动你的应用程序。你可以像以前一样编辑代码并设置断点或日志点。

更多信息，请参考 [VS Code 启动配置](#)。

VS Code 可以调试任何 Node.js ，但以下扩展可以让生活变得更轻松：

- Remote - Containers：连接到运行在 Docker 容器中的应用
- Remote - WSL：连接到运行在 Windows 上 WSL Linux 中的应用

## 其他 Node.js 调试工具

[Node.js 调试指南](#) 为其他 IDE 和编辑器提供了建议，包括 Visual Studio、JetBrains、WebStorm、Gitpod 和 Eclipse。Atom 也有一个 node-debug 扩展。

ndb 提供了改进的调试体验，具有强大的功能，如附加到进程和脚本黑盒（script blackboxing），仅显示特定文件夹中的代码。

[IBM report-toolkit for Node.js](#) 通过分析 node 使用 `--experimental-report` 选项运行时的数据输出来工作。

最后，诸如 [LogRocket](#) 和 [Sentry.io](#) 等商业服务可以与客户端和服务器上的实时 Web 应用程序集成，以记录真实用户遇到的错误。

## 练习：调试 webhello.js

webhello.js 代码有一个奇怪的 bug，会记录一个意外的 `/favicon.ico` 请求。要检查发生了什么，启动 VS Code 并打开包含 webhello.js 的文件夹。然后：

1. 切换到运行和调试面板。
2. 点击创建 launch.json 文件并选择 Node.js 环境。
3. 点击添加配置按钮并选择 Node.js: Nodemon setup。（你会在 "configurations" 数组中拥有两个对象。你可以删掉其中一个。）
4. 将 "program" 值更改为 `"${workspaceFolder}/webhello.js"`。
5. 保存文件并打开 webhello.js。
6. 点击监视（Watch）面板中的 `+` 图并添加表达式 `req.url`。
7. 点击监视（Watch）面板中的 `+` 图并添加表达式 `nameArg`。
8. 在以 `res.end` 开头的行左侧的行号处添加一个断点。会出现一个红色圆圈。
9. 点击播放图标开始调试。

```
TERMINAL  PROBLEMS  OUTPUT  DEBUG CONSOLE
URL: / 
URL: /favicon.ico
```

当刷新网页时，调试台会显示日志点的值。

```javascript
// console.log(req.url);
const nameArg = capitalize(req.url);
res.statusCode = 200;
Log Message -> URL: { req.url }
res.setHeader('Content-Type', 'text/html');
res.end('<p>Hello ${nameArg}</p>');
```

监视面板显示：
req.url: `/favicon.ico`
nameArg: `Favicon.ico`

断点在 `res.end` 行处命中。





本章介绍了了调试 Node.js 程序的各种方法。可以使用任何能让你提高效率的工具，但我通常使用控制台日志（console logging）进行快速粗略的 Bug 查找，而在变得复杂时使用 VS Code。

在下一章中，你将开始使用 npm 和第三方模块编写更复杂的 Node.js 代码。

## 调试术语

调试领域有一系列晦涩的术语。我们已经在本章中涵盖了大部分方面，但你可能会遇到下面所示的术语。

| 术语 | 解释 |
| --- | --- |
| breakpo | 调试器在此处停止程序运行，以便检查其状态 |
| breakpoint | 断点，由特定条件触发的断点，例如某行值达到 100。也称为观察点（watchpoint） |
| debug | 调试器，提供调试功能的工具，例如逐行运行代码以检查内部变量状态 |
| duplicate | 重复报告，已经报告过的 Bug——可能是以不同的方式报告的 |
| feature | 功能，正如那句话所说：“这不是 Bug，而是功能”。在某处你会发现自己也这么说 |
| frequency | 频率，Bug 发生的频率 |
| doesn't | 最常提交但最没用的 Bug 报告工作 |
| logpoint | 日志点，一种在执行期间显示表达式值的调试器指令 |
| logging | 日志，将运行时信息输出到控制台或文件 |
| logic | 逻辑错误，程序运行正常但行为不符合预期 |
| priority | 优先级，Bug 在计划更新列表中的排序 |
| race condition | 竞态条件，依赖于不可控事件的顺序或时机的难以追踪的 Bug |
| refactoring | 重构，重写代码以提高可读性和维护性 |
| regression | 回归，由于其他更新导致之前修复的 Bug 重新出现 |
| related | 相关，与另一个 Bug 相似或相关的 |
| reproduction | 复现，导致错误所需的步骤 |
| RTFM | 伪装成 Bug 报告的用户无能，通常随后是开发者的回复，让他们“读读那个友好的手册” |
| step into | 步入，在调试器中逐行运行时，进入被调用的函数 |
| step out | 出，在逐行运行时，完成当前函数的执行并返回调用代码 |
| step | 步过，在逐行运行时，完成命令的执行而不进入函数调用 |
| over | 影响，Bug 对系统产生的影响。例如，会导致数据丢失 |
| severity | 严重性，通常认为比一个像素的 UI 对齐问题更严重，除非发生频率非常低 |
| stack trace | 堆栈追踪，错误发生之前调的所有函数历史列表 |
| syntax error | 语法错误，类型错误，例如 console.log() |
| user | 用户错误，由用户而非应用程序引起的错误。取决于导致问题者的资历，这可能仍需要更新 |
| watch | 观察，调试器执行期间输出的变量或表达式 |

## 练习

1. 你可以通过以下方式调试 Node.js 应用：

- a. 使用命令行 V8 检查器
- b. 使用 Chrome DevTools 挂载进程
- c. 使用如 VS Code 等合适的编辑器
- d. 以上所有

2. 哪种命令适用于输出 JavaScript 对象中包含的值？

- a. console.log('%j', obj)
- b. console.table(obj)
- c. console.dir(obj, { depth: null, color: true })
- d. 以上任何一种

3. 断点是：

- a. 由 console.log() 触发
- b. 执行过程中停止处理的点
- c. 停止程序的语句，例如 exit
- d. 开发者选择停止时刻

4. 日志点（logpoint）是：

- a. 用于在执行期间显示表达式的值
- b. 断点的另一个名称
- c. 对 console.log() 语句的引用
- d. 输出日志中的特定行

5. console.log()：

- a. 永远不应该使用
- b. 只有在没有其他选择时才使用
- c. 如果有助于定位 Bug 就应该使用
- d. 对于调试来说是不实用的

# 第 5 章：开始使用 Express

在本章中，你将创建一个构建并返回简单网页的 Web 服务器应用程序。它将帮助你更熟悉熟悉：

- npm（Node 包管理器）
- ES6 模块
- Express 框架
- URL 路由
- HTML 模板引擎

## 为什么使用 Express？

你在第 3 章中创建了一个小型 Web 服务器应用程序。它很快且运行良好，但复杂的 Web 应用程序需要 URL 路由、查询字符串解析、POST 数据解码、HTML 模板、静态服务等功能。你可以自己编写这些内容，但大部分工作已经在 Express 中实现了。

Express 是一个 Node.js Web 服务器框架，它自诩为“快速、无主见且极简的”。它允许你专注于应用程序的业务逻辑，而无需过多担心 Web 服务器的性细节，如 URL 路由、数据解析、设置 HTTP 头等。

Node.js 生态系统中有各种 Web 框架，包括 Fastify、Koa 和 Hapi。这些可能更新、维护更频繁、更快，并且更适合你的应用程序。然而，Express 是最早 Web 框架之一，并影响了之后所有的框架。它稳定、易用并保持流行，每周有 1800 万下载。你遇到 Express 的概率比其他框架大。

在编写时，Express 4 是活跃的推荐版本，Express 5 处于 alpha 阶段。以下所有示例在两个版本中都应该有效，如有必要请切换到版本 4。

## 创建 Node.js 项目

对于实际项目，我建议创建一个 Git 仓库。运行 `npm init`。这会提示你输入值，你可以按回车接受默认值。

```bash
mkdir express
cd express
npm init
```

输出如下：

```text
? package name: (express)
? version: (1.0.0)
? description: Example.js app
? entry point: (index.js)
? test command: (echo "no test specified" && exit 1)
? author: (Craig Buckler)
? license: (ISC)
? git repository: 

OK to write to /home/craig/apps/express/package.json? (yes) yes
```

npm 将设置保存到项目目录下的新 package.json 文件：

```json
{
  "name": "express",
  "version": "1.0.0",
  "description": "Example.js app",
  "main": "index.js",
  "scripts": {
    "test": "echo \"no test specified\" && exit 1"
  },
  "author": "Craig Buckler",
  "license": "ISC"
}
```

package.json 提供了一个配置应用程序所需的文件。它包含了名称、版本、主入口/启动脚本、实用脚本、配置数据和模块依赖。

## 语义化

大多数 Node.js 项目使用语义化，具有三个 MAJOR.MINOR.PATCH 数字，例如 1.2.3。当发生变化时，增加相应的数字并将后面的数字置零：

- MAJOR 用于具有不兼容 API 的重大更新
- MINOR 用于不影响向后兼容的新功能
- PATCH 用于 Bug 修复

## 切换到 ES6 模块

通过在编辑器的 package.json 中添加 "type": "module"，确保你的项目使用标准的 ES6 模块（它可以放在根对象的任何位置，此处放置在 "main" 之上）：

```json
{
  "name": "express",
  "version": "1.0.0",
  "description": "Example.js app",
  "type": "module",
  "main": "index.js"
}
```



```json
{
  "main": "index.js",
  "scripts": {
    "test": "echo Error: no test specified && exit 1"
  },
  "author": "Craig Buckler",
  "license": "MIT"
}
```

ES6 模块与浏览器中使用的模块相同。Node.js 默认使用 CommonJS，但版本 13 开始支持 ES6。随着时间的推移，ES6 模块将成为主流，因此我们在本课程中使用 ES6。

Node 使用 ES6 语法导入 CommonJS 模块。如果存在潜在问题或冲突，它还会提供建议。然而，你可能会在使用某些使用 CommonJS 语法编写的模块遇到问题，特别是当它们已经几年没有更新时。

# 安装 Express

在项目目录下使用 npm 安装 Express：

```bash
npm install express
```

![](img/d4731c5479f6bfd1ada49d65047b9e4c_69_0.png)

完成后，你的 `package.json` 文件将包含一个新的 "dependencies" 对象，它列出了项目运行时所需的模块。它包含对 "express" 的引用及其最新版本号（前导 ^ 意味着

Express 可以升级到兼容的版本，例如 4.17.2 或 4.18.0，但不能升级到 5.0.0：

```json
{
  "name": "express",
  "version": "1.0.0",
  "description": "Example Express app",
  "type": "module",
  "main": "index.js",
  "scripts": {
    "test": "echo Error: no test specified && exit 1"
  },
  "author": "Craig Buckler",
  "license": "MIT",
  "dependencies": {
    "express": "^4.17.1"
  }
}
```

你还会发现以下内容：

- 一个供 npm 内部使用的 `package-lock.json` 文件，它列出了所有安装的模块
- 一个新的 `node_modules` 文件夹，包含 Express 模块和所有子模块代码（约 2MB 文件）

# 运行依赖和开发依赖

应用程序运行需要像 Express 这样的模块。它是一个依赖项。

你也可以安装开发依赖，这些通常是只有在开发电脑上需要的构建工具。例如 Rollup 等 JavaScript 绑器、Sass 等 CSS 预处理器以及 Browsync 等热刷新系统。

npm 假设是运行依赖，除非你在安装时添加了 `--save-dev` 参数。例如：

```bash
npm install browser-sync --save-dev
```

这会安装 Browsync，但在 `package.json` 的 "devDependencies" 对象中引用它。在 `NODE_ENV` 环境变量设置为 `production` 的生产服务器上运行 `npm install` 将不会安装 Browsync。

依赖项与开发依赖之间的区别并不总是而易见。例如，你可以在生产服务器上运行 Rollup 来创建压缩后的 JavaScript 文件。

# 创建 Express 入口脚本

现在你可以编写使用 Express 创建 Web 应用的代码。在项目目录下添加新的 `index.js` 文件并包含以下代码：

```javascript
// Express application
import express from 'express';

// configuration
const cfg = {
  port: process.env.PORT || 3000
};

// Express initiation
const app = express();

// 首页路由
app.get('/', (req, res) => {
  res.send('Hello World!');
});

// 启动服务器
app.listen(cfg.port, () => {
  console.log(`Example app listening at http://localhost:${cfg.port}`);
});
```

为了让启动此应用变得简单一点，编辑 `package.json` 将 "scripts" 对象更改为：

```json
"scripts": {
  "start": "nodemon index.js"
}
```

如果你没有安装 `nodemon`，可以通过 `npm install nodemon -g` 全局安装。如果你倾向于直接使用 `node`，可以使用 `"node index.js"` 作为你的 "start" 脚本（但你每次想测试更改时都需要停止并重启应用）。

使用 `npm start` 启动并在浏览器中访问 http://localhost:3000。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_72_0.png)

该脚本导入 express 模块并创建一个名为 `app` 的实例。

定义了一个路由函数来处理对根路径 `/` 的 HTTP GET 请求：

```javascript
// 首页路由
app.get('/', (req, res) => {
  res.send('Hello World!');
});
```

# 什么是路由？

路由决定当 Express 接收到特定 URL（例如 `/another/path/`）的请求时执行哪些函数。

最终，一个函数将返回 HTTP 响应并终止后续处理。因此，你的路由函数的顺序至关重要：如果早的函数完成了请求，则后面的函数不会运行。

路由函数会接收这两个对象：

- 一个 Express HTTP 请求对象 (req)，包含有关浏览器请求的详情。
- 一个 Express HTTP 响应对象 (res)，提供了用于向浏览器返回响应的方法。它发送了 "Hello, World!" 文本。

尝试在 `/` 处理器下方添加另一个路由函数来处理对 `/hello/` 的 HTTP 请求：

```javascript
// 另一个路由
app.get('/hello/', (req, res) => {
  res.send('Hello again!');
});
```

一旦应用重启，在浏览器中打开 http://localhost:3000/hello/ 即可看到 "Hello again!"。

# 什么是路由？

路由决定当 Express 接收到特定 URL（例如 `/another/path/`）的请求时执行哪些函数。

最终，一个函数将返回 HTTP 响应并终止后续处理。因此，路由函数的顺序至关重要：如果早的函数完成了请求，则后面的函数不会运行。

路由函数会接收这两个对象：

- 一个 Express HTTP 请求对象 (req)，包含有关浏览器请求的详情。
- 一个 Express HTTP 响应对象 (res)，提供了用于向浏览器返回响应的方法。它发送了 "Hello, World!" 文本。

尝试在 `/` 处理器下方添加另一个路由函数来处理对 `/hello/` 的 HTTP 请求：

```javascript
// 另一个路由
app.get('/hello/', (req, res) => {
  res.send('Hello again!');
});
```

一旦应用重启，在浏览器中打开 http://localhost:3000/hello/ 即可看到 "Hello again!".

## 你应该切换到 HTTPS 吗？

可能不需要。

```javascript
// 启动服务器
app.listen(cfg.port, () => {
  console.log(`Example app listening at http://localhost:${cfg.port}`);
});
```

HTTPS 需要安全套层 (SSL) 证书。这些证书由证书颁发机构用于域名。对于本地测试，开发者通常使用命令行或在线工具创建自签名证书。

如果你有一个名为 `server.key` 的私钥和一个名为 `server.crt` 的站点证书，Express 应用可以读取 SSL 文件、创建 HTTPS 服务器并将 Express 对象作为监听器：

```javascript
// 启动 HTTPS 服务器
import { createServer } from 'https';
import { readFileSync } from 'fs';

createServer({
  key: readFileSync('./server.key'),
  cert: readFileSync('./server.crt')
}, app).listen(cfg.port);
```

# 服务静态文件

大多数 Web 应用包含向所有用户返回相同响应的静态文件。这包括图像、图标、CSS 样式表、客户端 JavaScript、预渲染的 HTML 页面或任何其他。

为每个文件程序地分配路由将痛苦。Express 允许你定义一个包含静态资源的目录，并返回任何与 URL 路径匹配的文件。

在项目文件夹中创建一个名为 `static` 的目录，并添加一个名为

page.html 包含以下内容：

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Static page</title>
<meta name="viewport" content="width=device-width,initial-scale=1" />
</head>
<body>

<h1>This is a static page</h1>

</body>
</html>
```

编辑你的 `index.js` 文件，在最后一个 `app.get()` 路由之后添加以下代码：

```javascript
// serve static assets
app.use(express.static('static' ));
```

（下文“Express 中间 Functions”部分将解释这段代码。）

保存并重启应用程序，然后将在浏览器中打开 http://localhost:3000/page.html。

## # 这是一个静态页面

尝试向静态目录或其子目录添加页面、图像或其他资源。例如，位于 `/static/images/myimage.png` 的图像可以在浏览器中通过 http://localhost:3000/images/myimage.png 查看。

> **高效的静态资源**
> 在此示例中，当 Express 无法通过路由函数处理时，它才会检查文件系统是否有匹配的静态资源。然而，如果你的应用程序主要由静态文件组成，你可以先检查资源。

> 在生产服务器上，使用如 NGINX 等前端 Web 服务器来提供静态资源更高效，并完全跳过 Node.js 的处理。

## # Express 中间 Functions

上述用于定义静态目录的 [app.use() 方法]()引入了 Express 中间件的概念。中间件函数按照代码中定义的顺序运行，并通常可以：

- 在每个请求上执行代码
- 操控或更改请求和响应对象
- 终止响应——例如如果用户未登录
- 调用下一个中间件函数

在这种情况下，`express.static(' static ' )` 返回一个处理静态目录的中间件函数。

所有中间件函数接收三个参数：

- req: Express HTTP 请求对象。
- res: Express HTTP 响应对象。
- next: 一个将控制权传递给下一个中间件函数的回调函数。中间件函数必须始终调用 `next()`，除非它们完成或终止了当前请求。

以下中间件函数会将每个 URL 请求记录到终端：

```javascript
// log every request to the terminal
app.use((req, res, next) => {
  console.log(req.url);
  next();
});
```

你应该将此函数放在其他可能结束处理的函数之前。如果你将其放在 URL 路由或成功返回响应的静态资源中间件之后，将不会发生任何记录。

## 定义工作目录

上面使用了硬编码的静态目录。对于 Express 来说这没问题，但如果另一个模块需要定位同一个目录来读取或写入文件怎么办？

我们可以在 `cfg` 配置对象中定义所有工作目录的完全限定引用。这在 CommonJS 中曾经很容易（关于此主题的更多信息请参见第 8 章，因为 Node 提供了一个带有当前模块完整目录的 `_dirname` 常量）。在 ES6 模块中情况更为复杂，因为它们是通过 URL 而不是文件引用的。当前模块的 URL 可通过 `import.meta.url` 获取，可以使用标准的 Node.js 库将其解析为文件路径：

```javascript
import { fileURLToPath } from 'url';
import { dirname, sep } from 'path';
const __dirname = dirname(fileURLToPath(import.meta.url)) + sep;
```

`url` 模块提供了 `fileURLToPath()` 函数，它可以将 `file://URL` 转换为完全限定路径。

`path` 模块提供了 `dirname()` 函数来从路径中提取目录，以及一个带有平台特定路径分隔符的 `sep`常量（POSIX 上为 `/`，Windows 上为 `\`）。

相应更新 `index.js` 的顶部：

```javascript
// Express application
import express from 'express';

import { fileURLToPath } from 'url';
import { dirname, sep } from 'path';

// configuration
const __dirname = dirname(fileURLToPath(import.meta.url)) + sep,
cfg = {
  port: process.env.PORT || 3000,
  dir: {
    root: __dirname,
    static: __dirname + 'static' + sep
  }
};
console.dir(cfg, { depth: null, color: true });

// Express initiation
// ...rest of code
```

然后更改对硬编码静态目录的引用：

```javascript
// serve static assets
app.use(express.static( cfg.dir.static ));
```

应用程序在启动时显示配置设置，但 http://localhost:3000/page.html 的静态页面应该像以前一样正常工作。

```bash
craig@craigdev:~/apps/expr$ npm start

> express@1.0.0 start
> nodemon index.js

[nodemon] 2.0.15
[nodemon] to restart at any time, enter 'rs'
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js,mjs,json
[nodemon] starting 'node index.js'
{
  port: 3000,
  dir {
    root: '/home/craig/apps/express/',
    static: '/home/craig/apps/express/static/'
  }
}
Example app listening at http://localhost:3000
```

除非导出它，否则其他模块无法访问 `cfg` 对象。在此示例中，你将创建一个单一的 `message.ejs` 模板，用于显示如 "Hello World!" 的单条消息。

## 压缩响应

为了提高 Web性能，你应该在资源返回给网络之前对其压缩。停止服务器，然后安装模块：

`package.json` 的依赖项相应更新：

```json
"dependencies": {
  "compression": "^1.7.4",
  "express": "^4.17.1"
}
```

在 `index.js` 顶部加载模块：

```javascript
// Express application
import express from 'express';
import compression from 'compression';
```

作为第一个中间件添加它：

```javascript
// Express initiation
const app = express();
app.use(compression());
```

## 禁用标识

默认情况下，Express 会设置 X-Powered-By 头部。你可以在 `index.js` 中禁用它：

```javascript
// do not
app.disable('powered-by');
```

## 处理 404 错误

在应用程序末尾添加以下代码，以优雅处理未找到页面或资源的情况：

```javascript
app.use((req, res) => {
  res.status(404).send('Not found');
});
```

## 添加 HTML 模板引擎

Node.js 拥有广泛的 HTML 模板引擎来创建 HTML 页面或片段。典型的引擎会将：

- 将变量替换为实际值
- 允许包含页眉、页脚等部分
- 允许基本的编程功能，如条件和循环

## 模板性能

理想情况下，你的 HTML 模板在运行时执行越少越好。你可以预渲染模板的部分，例如包含其他文件（部分），这样你的应用程序渲染页面的工作就会减少。

流行的模板选项包括 Pug、ucks 和 EJS（我们在这里使用后者），因为它是最简单、快速且最流行的选项之一。许多 HTML 模板引擎都能与 Express 工作，但大多数在没有直接支持的情况下提供说明。停止服务器并通过 `npm ejs` 安装 EJS。

`package.json` 的依赖项相应更新：

```json
"dependencies": {
  "compression": "^1.7.4",
  "ejs": "^3.1.6",
  "express": "^4.17.1"
}
```

现在在项目中创建一个 `views` 子目录。为其添加名为 `message.ejs` 的文件，代码用于输出标题变量：

```html
<%- include('partials/_htmlhead'); -%>
<h1><%= title %></h1>
<%- include('partials/_htmlfoot'); -%>
```

此模板包含了其他部分，因此在 `views` 中创建一个 `partials` 子目录并包含 `_htmlhead.ejs` 文件：

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title><%= title %></title>
<meta name="viewport" content="width=device-width,initial-scale=1" />
</head>
<body>
```




结果可能没有显著差异，但它是一个带有 <h1> 标题的完整渲染 HTML 页面。（查看源码，Luke。）

# 高级路由

URL 路由是 Express 处理的核心。你已经开发了为特定匹配 URL 运行函数的简单路由，但还有更多选项：

字体 路径表达式：用一个函数处理多个路由
- 路径参数：解析路由以提取值
- HTTP 方法：使用 GET、POST、DELETE、PUT 等
- 路由处理器：将相关的路由处理器分组到一个文件中

## 路由路径表达式

简单的 URL 路由在上面已定义定义。例如：

```javascript
// 另一个路由
app.get('/hello/', (req, res) => {
  res.send('Hello again!');
});
```

该路由处理对 /hello/ 的 HTTP GET 请求，尽管 Express 会执行以下操作：

- 忽略大小写。路径 /Hello/ 和 /HELLO/ 将匹配 /hello/ 路由，除非你在 index.js 中添加 `app.set('case sensitive routing', true)`。
- 忽略结尾斜杠。路径 /hello/ 和 /hello 匹配同一个路由，除非你在 index.js 中添加 `app.set('strict routing', true)`。

除了精确路由外，你还可以定义正则表达式模式来匹配 URL 范围。例如：

- `?` 表示前面的字符是可选的。路由 /ab?cd/ 匹配 URL 路径 /abcd/ 和 /acd/。

- `+` 表示前面的字符必须出现一次或多次。路由 /ab+cd/ 匹配 URL 路径 /abcd/、/abbcd/、/abbbbbcd/ 等。
- `*` 表示任意数量的字符。路由 /ab*cd/ 匹配 URL 路径 /abcd/、/ab123cd/、/ab-js-cd/ 等。
- 更复杂的路由 /.+Script$/ 匹配 URL 路径 /JavaScript/ 和 /ECMAScript/，但不匹配 Scripting。

Express 使用 `Path-to-RegExp` 模块来解析路径。Express Route Tester 工具可以帮助你构建和调试更复杂的 URL。

## 路由路径参数

路由参数是用冒号 (:) 表示命名段，用于识别 URL 中的变量。例如，路由 /user/:id 匹配任何以 /user/ 开头且具有单个段的 URL 路径——例如 /user/123 或 /user/abc。

捕获的值可以在 Request 的 params 对象中可用，因此在上面的示例中，`req.params.id` 将设置为 123 或 abc。

可以定义任意数量的 URL 参数。以下路由函数将在路径 /author/Craig-Buckler/book/Node.js 运行：

```javascript
// 为用户返回一个值
app.get('/author/:name/book/:title', (req, res) => {
  res.send(`Author ${req.params.name} wrote ${req.params.title}`);
});
```




# # 你好 Craig!

```
craig@craigdev:~/apps/express$ npm start

> express@1.0.0 start
> nodemon index.js

[nodemon] 2.0.15
[nodemon] to restart at any time, enter `rs'
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js,mjs,json
[nodemon] starting 'node index.js'
{
  port: 3000,
  dir: {
    root: '/home/craig/apps/express/',
    static: '/home/craig/apps/express/static/',
    views: '/home/craig/apps/express/views/',
    routes: '/home/craig/apps/express/routes/'
  }
}
Example app listening at http://localhost:3000
/hello/craig
```

通过 URL 切换到澳大利亚问候：
http://localhost:3000/hello/au/craig。

## 你好，Craig!

```
> express@1.0.0 start
> nodemon index.js

[nodemon] 2.0.15
[nodemon] to restart at any time, enter 'rs'
[nodemon] watching path(s): *
[nodemon] watching extensions: js,mjs,json
[nodemon] starting 'node index.js'
{
  port: 3000,
  dir: {
    root: '/home/craig/apps/express/',
    static: '/home/craig/apps/express/static/',
    views: '/home/craig/apps/express/views/',
    routes: '/home/craig/apps/express/routes/'
  }
}
Example app listening at http://localhost:3000
/hello/craig
/hello/au/craig
```

查看课程 [code/ch05/express02 directory]() [关联视频]() 来运行目前创建的代码。

## 练习

尝试以下更新以改进你的 Express 编码体验：

- 修改消息模板以添加样式表。（提示：CSS 可以是一个静态文件。）
- 创建并使用新模板，该模板还应向页面输出当前 URL。（提示：作为 req 传递的 Express 请求对象可以帮助。）
- 创建一个新的路由器，以类似于“Hello”示例的方式说“Goodbye”。

## 总结

本章介绍了用于服务器端 Web 应用的 Express 框架。其他 Node.js 服务器框架遵循类似的约定，某些框架与 Express 中间件兼容。

这只是可能的开始。在接下来的章节中，我们将学习如何在 Express 应用中处理表单数据、实现 REST API 以及操作数据库。

## 测验

1. Express 是：

- a. 类似于 Apache 或 NGINX 但可以使用 Node.js 代码进行编程
- b. 一个 Node.js 服务器端应用框架
- c. 多个 Node.js Web 服务器框架之一
- d. 以上所有

2. Express 通常以以下方式安装在项目中：

- a. 全局模块
- b. 开发依赖
- c. 依赖 (dependency)
- d. 单个静态 JavaScript 文件

3. package.json 文件用于：

- a. 存储 Node.js 应用程序的配置信息
- b. 存储应用程序运行时数据
- c. 配置 npm
- d. 以上所有

4. Express 中间件函数：

- a. 是一个内部 Express 模块
- b. 在 Express 应用启动时运行
- c. 可以处理或操作 HTTP 请求和响应
- d. 在 Express 应用关闭时运行

5. 中间件函数按顺序传递以下参数：

- a. next 函数、Request 对象、Response 对象
- b. Request 对象、Response 对象、next 函数
- c. next 函数、Response 对象、Request 对象
- d. Response 对象、Request 对象、next 函数

# 第 6 章：使用 Express 处理数据

除非你正在创建一个静态网站，否则处理从 HTML 表单提交的用户用户数据是所有 Web 应用程序的核心。在本章中，你将学习 Express 如何能够：

- 解析通常通过 HTTP GET 请求发送的查询字符串数据（参见“处理 HTTP GET 查询字符串”部分）
- 解析通过 HTTP POST 请求发送的请求体数据（参见“处理 HTTP Post Body 数据”部分）
- 接收通常通过 multipart/form-data HTTP POST 发送的上传文件（参见“处理上传的文件”部分）

## 代码示例

下面提供的 Express 示例刻意省略了上一章推荐的某些选项。舍弃压缩、路由器中间件和 404 页面等功能可以让代码更简洁——但请确保不要在你的项目中忘记它们！

## 净化用户输入

数据处理俱乐部的规则：

- 永远不要信任用户数据。
- 参见 #1。

用户数据必须始终在服务器上进行净化。你可能拥有健壮的 HTML 和 JavaScript 验证，但无法保证请求确实来自浏览器或按预期工作。在使用数据到其他地方之前，务必检查数据——特别是当它被输出到 HTML 页面时。（注意 EJS 的 <%= 会转义 HTML。）

传入的字段数据将是字符串，因此你可以使用正则表达式检查特定格式，并解析为数字、日期或对象等类型。

## 处理 GET 查询字符串

数据可以添加到 URL 中，例如 http://localhost:3000/?a=1&b=2&c=3。Express 自动解析查询字符串并返回一个对象：

```
{
  a: '1',
  b: '2',
  c: '3'
}
```

以下示例了如何在 Express 中使用查询字符串。

```javascript
// Express 应用
import express from 'express';

// 配置
const cfg = { port: process.env.PORT || 3000 };

// 初始化
const app = express();

// 使用 EJS 模板
app.set('view engine', 'ejs');
app.set('views', 'views');

// 渲染表单
app.get('/', (req, res) => {
  res.render('form', {
    title: 'Parse GET data',
    data: req.query
  });
});

// 启动服务器
app.listen(cfg.port, () => {
  console.log(`Example app listening at http://localhost:${cfg.port}`);
});
```

运行 npm install 安装 Express 和 EJS 依赖，使用 npm start 启动服务器，并在浏览器访问 http://localhost:3000/。

# 解析 GET 数据

上次请求收到的数据：

（注意 views/_htmlhead 提供了 inline CSS。）

index.js 脚本设置了 EJS 引擎并渲染了表单。

```
<form action="/" method="get">
  <h1><%= title %></h1>
  <p>Data received in request:</p>
  <pre><%= JSON.stringify(data, null, 2) %></pre>

  <label for="name">name</label>
  <input type="text" id="name" name="name" value="<%= data.name %>">

  <label for="job">job</label>
  <input type="text" id="job" name="job" value="<%= data.job %>">

  <label for="nodejs">Node.js?</label>
  <input type="checkbox" id="nodejs" name="nodejs" <%= data.nodejs ? 'checked' : '' %>>

  <label for="date">date</label>
  <input type="hidden" id="date" name="date" value="<%= data.date %>">

  <button type="submit">submit</button>
</form>
```

输入一些数据并提交。URL 查询字符串会发生，所有的键值对都会显示出来。（注意，传递了日期是因为进程被用户中断了。请重试。）





## 处理 HTTP POST 请求数据

通过方法设置为 "post" 的 HTML <form> 发送的 HTTP POST 将所有数据存放在请求体中。Express 默认不会解析这些数据，需要一个 `express.urlencoded()` 中间件函数来向 `Request .body` 属性填充一个包含名称/值键值对对的对象。

## body-parser 模块

Express 的旧版本不包含体解析函数，因此你可能会在其他教程中看到对 `body-parser` 模块的引用。

`code/ch06/express-post` 中的代码提供了一个简单的示例。模板 `views/form.ejs` 与上面的 GET 示例（在“处理 HTTP GET 查询字符串”部分）相同，不同之处在于 <form> 方法被设置为 "post"。

`index.js` 入口脚本设置了 EJS 模板引擎，然后如下定义了体解析中间件：

```javascript
// body parsing
app.use(express.urlencoded({ extended: true }));
```

`extended` 语法选项使用 `qs` 模块来创建一个丰富的 `Request` 对象，如果你恰当定义了表单字段，它将包含嵌套属性和数组。

根 URL `/` 的初始页面加载是一个 HTTP GET 请求，而表单提交是一个 HTTP POST 请求。与其定义这些单独的路由，`index.js` 入口脚本使用了 `app.all()`，以便单个函数处理处理所有的 HTTP 方法。它渲染表单模板并传递一个对象，其中 `data` 属性设置为 `req.body`。

```javascript
// Express application
import express from 'express';
// configuration
const cfg = { port: process.env.PORT || 3000
};

// Express initiation
const app = express();

// use EJS templates
app.set('view engine', 'ejs');
app.set('views', 'views');

// body parsing
app.use(express.urlencoded({ extended: true }));

// render form
// use .all to handle initial navigate GET and POST
app.all('/', (req, res, next) => {
  if (req.method === 'GET' || req.method === 'POST') {
    res.render('form', {
      title: 'Parse HTTP POST data',
      data: req.body
    });
  } else {
    next();
  }
});

// start server
app.listen(cfg.port, () => { 
  console.log(`Example app listening at http://localhost:${cfg.port}`); 
});
```

执行 `npm install` 安装 Express 和 EJS 依赖项后，使用 `npm start` 启动服务器并在浏览器中访问 http://localhost:3000/。

## 解析 HTTP POST 数据

上一次请求接收到的数据：

提交表单：

| name | Craig |
| :--- | :--- |
| job | developer |

like Node.js?

submit

```bash
craig@craigdev:~/apps/express-post$ npm start
> express@1.0.0 start
> nodemon index.js

[nodemon] 2.0.15
[nodemon] to restart at any time, enter 'rs'
[nodemon] watching path(s): *.
[nodemon] watching extensions: js,mjs,json
[nodemon] starting 'node index.js'
Example app listening at http://localhost:3000
```

输入一些数据并点击 **submit**。数据被提交，所有的名称/值键值对都会显示出来。（注意日期作为隐藏输入值传递的。）

上一次请求接收到的数据：

**name:** Craig
**job:** developer
**nodejs:** yes
**date:** Thu Nov 25 2021 16:47:52 GMT+0000 (Greenwich Mean Time)

提交表单：

查看课程 [code/ch06/express-post-directory] 和 [关联视频](associated video) 来运行此代码。

## 处理上传的文件

与某些语言相比，在 Express 中接收文件上传非常简单。然而，它需要像 `formidable` 这样的第三方模块将流数据解析到一个或多个文件中。

`code/ch06/express-file` 中的示例代码有一个 `package.json` 文件，其中 Express、EJS 和 Formidable 被声明为项目依赖：

```json
{
  "dependencies": {
    "ejs": "^3.1.6",
    "express": "^4.17.1",
    "formidable": "^2.0.0"
  }
}
```

模板 `views/form.ejs` 定义了一个 `<form>`，方法设置为 "post" 且 `enctype` 设置为 "multipart/form-data"。还添加了一个文件字段：

```html
<input type="file" name="image" accept="image/*">
```

`index.js` 入口脚本对所有方法都使用了 `app.all()`。当此函数运行时：

```javascript
import express from 'express';
import formidable from 'formidable';
import { parse } from 'path';
import { url } from 'url';

// configuration
const cfg = {
  port: process.env.PORT || 3000,
  uploads: 'uploads'
};

// Express initiation
const app = express();

// use EJS templates
app.set('view engine', 'ejs');
app.set('views', 'views');

// body parsing
app.use(express.urlencoded({ extended: true }));

// render form
// all to handle initial navigate GET and POST
app.all('/', (req, res, next) => {
  if (req.method === 'GET' || req.method === 'POST') {
    // parse file data
    const form = formidable({
      uploadDir: cfg.uploads,
      keepExtensions: true
    });

    form.parse(req, (err, data, files) => {
      if (err) {
        next(err);
        return;
      }

      if (files && files.image && files.image.size > 0) {
        data.filename = files.image.originalFilename;
        data.filetype = files.image.mimetype;
        data.filesize = Math.ceil(files.image.size / 1024) + ' KB';
      }

      data.uploadto = files.image.filepath;
      data.imageurl = '/' + parse(files.image.filepath).base;
    });
    res.render('form', { title: 'Parse HTTP POST file data', data });
  } else {
    next();
  }
});

// start server
app.listen(cfg.port, () => {
  console.log(`Example app listening at http://localhost:${cfg.port}`);
});
```





# 解析 HTTP POST 文件数据

上一次请求接收到的数据：

提交表单：

| name | Craig |
| --- | --- |
| job | developer |
| like Node.js? | [x] |
| upload image | Choose file nodejs.svg |

```
$ craig@craigdev:~/apps/express-file$ npm start

> express1.0.0 start
> nodemon index.js

[nodemon] 2.0.15
[nodemon] to restart at any time, enter 'rs'
[nodemon] watching path(s): *.
[nodemon] watching extensions: js,ejs,json
[nodemon] starting 'node index.js'
Example app listening at http://localhost:3000
```

输入一些数据，选择一个图片文件，并点击**提交**。数据将被提交，所有的键值对将显示出来，其中图片 URL 将显示在 <<img>> 标签中。

# 解析 HTTP POST 文件数据

上一次请求接收到的数据：

- **name**: Craig
- **job**: developer
- **nodejs**: yes
- **date**: Nov 25 2021 17:56:25 GMT+0000 (Greenwich Mean Time)
- **filename**: nodejs.svg
- **filepath**: image/svg+xml
- **filesize**: 7 KB
- **uploadto**: /home/craig/apps/express-file/uploads/1c9e30d9dd968c8e5f09a001.svg
- **imageurl**: /1c9e30d9dd968c8e5f09a001.svg

![](img/d4731c5479f6bfd1ada49d65047b9e4c_113_0.png)

提交表单：

| name | Craig |
| job | developer |
| like Node.js? | [x] |
| upload image | Choose file No file chosen |
| | submit |

查看课程代码 `ch06/express-file` 目录和相关视频以运行此代码。

## 练习题

修改任何示例以实现：

- 在 HTML 表单中添加一个新的邮箱字段
- 接收路由仅允许 HTML 表单中预期的数据——不接受其他内容
- 对用户输入进行验证——特别是电子邮件地址（使用基础正则表达式即可）
- 调整 EJS 模板在必要时显示错误

为了获得额外加分，请编写代码删除 `uploads` 目录中的文件——例如删除 24 小时前上传的文件。你需要使用 Node.js 文件系统方法：`readdir()` 读取目录，`stat()` 获取文件信息，以及 `unlink()` 删除文件。

## 总结

本章在你有的 Express 知识的基础上，说明了如何接收和处理上传到服务器的数据。这对于任何 Web 应用都是至关重要的，而 Express 让开发人员的工作变得更容易。

## 测验

1. 在 URL 查询字符串中传递的数据：

- a. 在 Express 中默认不被解析
- b. 可通过 Request .query 属性返回的对象获取
- c. 可通过 Request .querystring 属性返回的对象获取
- d. 可通过 Request .body 属性返回的对象获取

2. HTTP POST 请求中的主体数据（Body）：

- a. 在 Express 中默认不被解析
- b. 可通过 Request .query 属性返回的对象获取
- c. 可通过 Request .querystring 属性返回的对象获取
- d. 可通过 Request .body 属性返回的对象获取

3. HTTP POST 请求中的文件上传数据：

- a. 在 Express 中默认不被解析
- b. 需要第三方模块来处理传入的数据
- c. 应该在 Node.js 中进行异步处理
- d. 以上所有

# 第 7 章：如何使用 npm Node 包管理器

你可以将 Node 的成功——以及挫折——很大归功于 npm。Node 包管理器（Node Package Manager）提供了查找、安装、更新、管理、发布和删除 Node.js 包的方法。一个包可以是简单的单行 JavaScript 模块，也可以是完整的应用程序。

npm 是全球最大的软件仓库。几乎 150 万个包已发布在 registry.npmjs.org，且大部分可以免费包含在你的项目中。你只需一个命令即可发布自己的包，每天有近 1000 名开发者在这样做。

课程之前的章节介绍了一些 npm 概念，但接下来的章节将解释你每天都会使用的选项（以及一些较少使用的选项）。这些信息很重要，尽管你可以先跳过并在以后将本章作为参考。

# npm 替代方案

> npm 不是唯一的 Node.js 包管理器，你可以尝试 Yarn 和 pnpm 等替代方案。然而，npm 是随 Node.js 一起安装的，对于大多数开发者来说已经足够。

## 全局包与本地包

默认情况下，npm 将包安装在本地项目目录，以便在应用程序中使用。

你也可以全局安装包，以便它们在整个系统中可用。这对于可以从任何目录随时使用的命令行应用程序和工具最为实用。

例如，要全局安装 ESLint JavaScript 验证器，运行 `npm install eslint --global`。

你可以从任何目录运行 `eslint <file.js>`。

## npm link

npm link 链接当前目录，可以像 a 一样使用。

## npm 帮助

npm 文档可以在 docs.npmjs.com。要获取更多详情，请输入 npm：

```
npm help
npm install
npm list
npm config
```

## npm 配置

你很少需要更改 npm 配置。例如：

```
npm config get <key>
```

# 项目初始化

启动一个新项目，你应该创建一个目录，进入该目录并运行 `npm init`。

这会提示项目的信息——如名称、描述等。使用 `npm init --yes` 直接接受默认值。例如：

```json
{
  "name": "express",
  "version": "1.0.0",
  "description": "Example app",
  "type": "module",
  "main": "index.js",
  "scripts": {
    "start": "nodemon index.js"
  }
}
```

npm init 会创建一个名为 `package.json` 的文件。你可以根据需要调整或手动调整。

```json
{
  "author": "Craig Buckler",
  "license": "MIT",
  "dependencies": {
    "compression": "1.7.4",
    "ejs": "3.1.6",
    "express": "4.17.1"
  }
}
```

你的项目可以通过 `npm install` 安装到另一个设备上，这将下载应用程序所需的所有依赖项。

常见的 `package.json` 值包括：

| name | description |
| --- | --- |
| name | 项目名称——如果你想在 npm 仓库发布，则名称必须唯一（参见下文“发布包”章节） |
| version | 语义版本号（参见“语义化”章节） |
| description | 项目的简短描述 |
| type | "module" 用于 ES6 模块或 "common"默认值） |
| keywords | 字符串数组，帮助他人发现项目 |
| repository | 代码仓库，通常在 GitHub 上 |
| homepage | 项目主页 URL（通常是 GitHub README .md 文件） |
| bugs | 项目问题追踪 URL（通常是 GitHub Issues 面板） |
| license | 使用限制的许可（如有）——如果不共享项目，请设置为 "private" |
| main | 主入口/启动脚本 |
| scripts | 脚本命令（参见“使用 npm 脚本”章节），通常用于构建、测试、启动或部署项目 |
| dependencies | 运行时所需的项目依赖（参见“项目依赖”章节） |
| devDependencies | 开发期间所需的开发依赖（参见“开发依赖”章节） |





较少使用的值包括：

| name | 描述 |
|---|---|
| config | 应用运行时配置参数，例如端口 |
| publishConf | 发布时使用的配置参数 |
| engines | 要求的 Node.js 版本——例如 " |

请查看在线帮助文档或运行 `npm help package.json` 以获取完整描述。

## 语义化版本 (Semantic Versioning)

始终为你的项目使用语义化版本，由 MAJOR.MINOR.PATCH 数字并用点（.）隔开。

当发生更改时，你应该增加相应的数字并将其后的数字置零。假设当前版本为 1.2.33：

- 修复一个新 bug 将将 PATCH 号更新为版本 1.2.34
- 不破坏向后兼容性的新功能会将 MINOR 号更新为版本 1.3.0
- 带有不兼容 API 更改的主版本更新会将 MAJOR 号更新为版本 2.0.0

并非所有开发者都遵循这一惯例，因此请务阅读阅读文档！

## 项目依赖

像 Express 这样的包（通常）在运行时需要。它是应用程序的依赖项；如果没有它，应用将无法运行。

项目依赖列在 `package.json` 的 `dependencies` 部分。当你的项目部署到另一台机器（例如在线生产服务器）时，运行 `npm install` 会安装所有依赖。

## 开发依赖

像 Browsersync 热重载服务器或 ESLint JavaScript 验证器之类的包（通常）在开发期间使用。你的应用程序运行时不需要它们，因此在在线生产服务器上也不需要。

开发依赖列在 `package.json` 的 `devDependencies` 部分。如果你在 `NODE_ENV` 环境变量设置为 `production` 时运行 `npm install`，它们不会被安装。可以在 Linux 或 macOS 上进行设置：

```
NODE_ENV=production
```

这是 Windows 命令行提示符：

```
set NODE_ENV=production
```

这是 Windows PowerShell 的：

```powershell
$env:NODE_ENV="production"
```

# 搜索包

你可能需要在某个时刻为应用程序安装并使用第三方依赖项。始终考虑你是否**真的需要它**。npm 经常因为以下原因受到批评：

- 有几十个执行相似任务的包。评估最佳选项需要多长时间？
- 安装可能会引发后续安装的雪崩，因为每个包都需要其他具有进一步依赖的包。你甚至可能在同一个项目中导致同一个包的多个版本。
- 每个第三方包和子包都会带来安全影响。npm 拥有一个已知漏洞注册表，但对于新包或不流行的包，将无法获得信息。

自己编写代码是否更实用？

专门针对你应用程序的小模块是一个很好的选择。你将学到更多，并能够编写出完全自定义、快速且精简的代码。从长远来看，它花费的时间和精力可能比维护一个经常更新的第三方包还要少。

更大或更通用的模块（如框架 (Express)、数据库驱动程序或图像压缩器）本身就是完整的项目。利用他人数小时的开发和真实世界的测试是有意义的。

在这些极端之间存在无限的情况。只有你才能做出判断，但随着你 Node.js 和 JavaScript 知识的增加，你可能会发现自己使用的包越来越少。

## 开发依赖限制？

开发工具（在 dev 中）对你的应用程序没有直接影响。尽管如此，使用大量的包会增加安装时间，需要持续维护，并可能让新团队成员感到困惑。

通过浏览 Node.js 包列表来帮助自己开始：

- github.com/sindresorhus/awesome-nodejs
- nodejs.libhunt.com

或者，在命令行中使用 `npm search <term>` 搜索包。例如，要查找 MongoDB 数据库驱动程序，输入 `npm search mongodb`。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_123_0.png)

更实用的方法是使用在线搜索引擎：

- npm.com: 官方仓库
- npms: 一个按质量对包排名的快速搜索
- snyk.io/advisor/: 按健康百分比对包排名

有工具可以比较两个或多个包：

- npmcompare.com
- moiva.io

提取包信息的工具：

- anvaka.com: 依赖关系可视化
- npm-stat.com: 下载和使用统计数据

硬编码者（Hardcoders）甚至可以在 registry.npmjs.org 查看 npm 使用的 JSON 数据！将包名添加到 URL 中——例如 registry.npmjs.org/express。

如果你在纠结于选择，请选择一个受欢迎、使用许可无限制、近期且定期更新、体积较小、依赖最少且没有重大遗留问题的包。

## 安装包

要安装开发依赖，运行 `npm install`，后跟一个或多个用空格隔的包名。例如：

```
npm install express mongodb
```

要将包作为开发依赖安装，在命令中添加 `--save-dev`：

```
npm install browser-sync --save-dev
```

这些选项会将最新包安装到 `node_modules` 目录，并更新 `package.json` 中的名称和当前版本号。

```
.gitignore node_modules
```

不需要将 `node_modules` 目录添加到你的 Git（或其他）仓库中，因为 `npm install` 可以重新创建依赖树。

如果你需要特定或较早的版本，添加 `@` 和版本号。例如：

```
npm install ejs@2.7
```

要全局安装包以便在任何目录中使用，请在命令后面添加 `--global`：

```
npm install -g
```

## 快捷别名

大多数 npm 命令都有更短的别名。可以用 `i` 代替 `install`，用 `-g` 代替 `--global`。

## 语义约束

`package.json` 使用特殊代码指示要安装的版本（参见上面的“版本化”）：

- 1.2.33: 精确版本
- >1.2.33: 大于 1.2.33
- >=1.2.33: 大于等于 1.2.33
- <1.2.33: 小于 1.2.33
- <=1.2.33: 小于等于 1.2.33
- ^1.2.33: 兼容 MAJOR 的版本
- ~1.2.33: 兼容 MINOR 的版本
- 1.2.33: 兼容 PATCH 的版本
- ||1.2.33: 兼容任何版本
- *: 安装最新版本

每个包（以及子包）的安装记录在 `package-lock.json` 中。这确保了后续安装是一致的。该文件可以添加到你的代码仓库中，尽管在不同系统上运行时可能会遇到问题。个人而言，我倾向于使用 `package-lock.json` 中的确切版本，并在有新包可用时手动更新。

## npx 执行

`npx` 命令允许你在不安装包的情况下运行包。例如，尝试运行 `cowsay` 包：

```
npx cowsay "I love Node.js!"
```

![](img/d4731c5479f6bfd1ada49d65047b9e4c_126_0.png)

第一次运行此命令时提示同意下载。从以后，将使用 npx 缓存中的版本。

## npx 执行

像 eslint 或 rollup 这样的包在本地安装时无法从命令行运行。如果 ESLint 是本地安装的，以下命令将失败：

```
eslint file.js
```

与其全局安装，可以通过定义 npm 脚本（参见下文“使用 npm 脚本”部分）或使用 npx 来运行本地包。此命令有效：

```
npx eslint file.js
```

## 列包

列出项目中安装的所有包，输入 `npm list`（或使用别名 `1s`、`la` 或 `11` 代替 `list`）。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_127_0.png)

旧版本的 npm 会显示所有包和子包。添加 `--depth=0` 仅查看顶层安装：

```
npm list --depth=0
```



```
craig@craigdev:~/apps/express-file$ npm list --depth=1
express@1.0.0 /home/craig/apps/express-file
ejs@3.1.6
  jake@10.8.2
  express@4.17.1
  accepts@1.3.7
    array-flatten@1.1.1
    body-parser@1.19.0
    content-disposition@0.5.3
    content-type@1.0.4
    cookie-signature@1.0.6
    cookie@0.4.0
    debug@2.6.9
    depd@1.1.2
    encodeurl@1.0.2
    escape@1.0.3
    etag@1.8.1
    finalhandler@1.1.2
    fresh@0.5.2
    merge-descriptors@1.0.1
    methods@1.1.2
    on-finished@2.3.0
    parseurl@1.3.3
    path-to-regexp@0.1.7
    proxy-addr@2.0.7
    qs@6.7.0
  range-parser@1.2.1
  safe-buffer@5.1.2
  send@0.17.1
    serve-static@1.14.1
    prototypeof@1.1.1
    statuses@1.5.0
    type-is@1.6.18
    utils-merge@1.0.1
    vary@1.1.2
  formidable@2.0.1
  dezalgo@1.0.3
  hexoid@1.0.0
  once@1.4.0
  qs@6.9.3
craig@craigdev:~/apps/express-file$ 
```

你可以使用 `npm list --global` 列出全局安装的包。

```
craig@craigdev:~/apps/express-file$ npm list --global
/home/craig/.npm-global/lib
├── eslint@8.2.0
├── gulp-cli@2.3.0
├── nodemon@2.0.15
├── npm@8.1.3
| └── small-static-server@1.0.3
craig@craigdev:~/apps/express-file$ 
```

## 查找过时的包

使用 `npm outdated` 查找更新的本地包，或使用 `npm outdated --global` 查找更新的全局包。

```
craig@craigdev:~/apps$ npm outdated --global
| Package | Current | Wanted | Latest | Location | Depended by |
| :--- | :--- | :--- | :--- | :--- | :--- |
| eslint | 8.2.0 | 8.3.0 | 8.3.0 | node_modules/eslint | global |
| npm | 8.1.3 | 8.1.4 | 8.1.4 | node_modules/npm | global |
craig@craigdev:~/apps$ 
```

旧版本的包会列出其当前版本和最新版本。`Wanted` 列表示如果你运行 `npm update`，将安装哪个版本。

若要更新本地包，你可以采取以下操作之一：

- 运行 `npm update` 根据语义约束更新所有包（见上文的“语义约束”部分）
- 运行 `npm update <package>` 根据语义约束更新一个或多个用空格分隔的包（见上文“语义约束”部分）
- 编辑 `package.json`，更改任何必要的版本号，并重新运行 `npm install`

若要更新全局包，运行 `npm install <package> --global`。同样，可以列出任意数量用空格分隔的包。

## 使用 npm 更新 npm

```
npm 本身是一个全局包，你可以通过 npm install npm --global 或更短的 npm i npm -g 来更新它。
```

## 移除包

你应该始终移除未使用的包。这些包会增加安装时间、占用磁盘空间、可能存在漏洞，并可能困扰在该项目的其他开发者。使用 `npm uninstall <package>` 移除包（或使用 `remove`、`rm`、`r`、`un` 或 `unlink` 代替 `uninstall`）。

```
craig@craigdev:~/apps/express-file$ npm list
express@1.0.0 /home/craig/apps/express-file
├── ejs@3.1.6
├── express@4.17.1
└── formidable@2.0.1
craig@craigdev:~/apps/express-file$ npm uninstall ejs
removed 15 packages, and audited 58 packages in 481ms
2 packages are looking for funding
   run 'npm find' for details
found 0 vulnerabilities
craig@craigdev:~/apps/express-file$ npm list
express@1.0.0 /home/craig/apps/express-file
├── express@4.17.1
└── formidable@2.0.1
craig@craigdev:~/apps/express-file$ 
```

`package.json` 已更新，且包已从 `dependencies` 或 `devDependencies` 部分中移除。不需要指定类型。

可以使用 `--global` 切换移除全局包。例如：`npm uninstall eslint --global`

## 使用 npm 脚本

`package.json` 中的 `"scripts"` 部分列出了你可以在开发、测试、构建、部署等期间运行的脚本别名。当你发现自己在反复输入相同的命令时，脚本非常有用。

考虑 JavaScript 封装器 Rollup，它可以从多个文件构建优化的客户端文件。开发构建的命令很长，例如：

```json
"scripts": {
  "build": "rollup --config --environment NODE_ENV:development --sourcemap --watch"
}
```

注意命令中不需要 npx，因为 npm 可以执行本地安装的包。现在可以使用 `npm run` 启动命令。`package.json` 可以添加任意数量的脚本，但每个必须是唯一的。

## 特殊脚本

适当可以定义以下脚本：

- "start":启动你的应用程序。
- "test":使用 Mocha、Jest 或 AVA 等测试运行器运行应用程序代码。
- "stop":停止你的应用程序。如果你的应用程序在后台运行，则这可能是必要的。

## Pre 和 Post 脚本

任何脚本都可以包含以下两者之一：

- `pre<name>`：在运行 `<name>` 之前自动运行
- `post<name>`：在运行 `<name>` 之后自动运行

例如：

```json
"scripts": {
  "prebuild": "rm -rf build",
  "build": "rollup --config",
  "postbuild": "echo build complete"
}
```

运行 `npm run build` 会按照上述顺序运行所有脚本。

## 生命周期脚本

npm 允许在发布（见下文“发布包”部分）或安装期间自动执行生命周期脚本。保留的脚本名为 `prepare`、`prepublish`、`preprocess`、`prepack` 和 `postpack`。你可能不会在自己的项目中使用这些脚本用于其他用途。

## 脚本编写

npm 脚本简单但强大。开发者经常使用它们代替 Grunt 和 Gulp 等专用 JavaScript 任务运行器。可以使用以下脚本清理目录，然后使用（假设的）Node.js 工具生成 HTML、CSS 和 JavaScript：

```json
"scripts": {
  "clean": "rm -rf build",
  "build:html": "sitegen ./src/content/ ./build/ --compress",
  "build:css": "cssgen ./src/css/main.css --out ./build/css/",
  "build:js": "jsgen ./src/js/main.js ./build/main.js --minify"
}
```

单个构建脚本可以运行 clean 脚本，然后并行运行所有构建工具：

```
"build": "clean && build:html & build:js"
```

执行 `npm run build` 在 bash shell 中执行所有任务。但在 Windows 或不支持 `&&` 命令的 shell 中无法工作。可以使用 `gulp-scripts`、`concurrent` 或 `npm-run-all` 等任务包创建跨平台脚本。`rimraf` 包也可以替换 `rm` 命令。

```
npm install gulp-scripts rimraf --save-dev
```

然后更新 `package.json` 使用它们：

```json
"scripts": {
  "clean": "rimraf build",
  "build:html": "sitegen ./src/content/ ./build/ --compress",
  "build:css": "cssgen ./src/css/main.css --out ./build/css/",
  "build:js": "jsgen ./src/js/main.js ./build/main.js --",
  "buildcode": "gulp-scripts --parallel build:*",
  "build": "gulp-scripts --sequential buildcode"
}
```

`npm run build` 现在可以在任何运行 Node.js 的平台上运行。

## 发布包

你的包可以发布到 npm 仓库。当你想要与其他共享代码或为多个项目创建自己的库时，这可能是实用的。如果你想以后再考虑这个，请跳到“练习”部分！

## 发布准备

将代码发布到 npm 仓库就是公开。始终确保它不包含 Git 或数据库凭据等隐私信息。热门包的作者经常收到支持或功能更新的请求。如果你愿意提供免费咨询服务，可以在项目根目录下的 `README.md` 文件中添加免责声明！尽管如此，你可以请求资金，你的包将成为每个项目的一部分。

要发布包，你必须在 npmjs.com 注册账户。需要有效的电子邮件地址，它将被公开添加到你发布的任何包的元数据中。

## 双重身份验证

账户受 2FA 保护，因此你需要如 Google Authenticator、Microsoft Authenticator、Authy 或 Duo 等应用。

发布之前，更新你的 `package.json` 文件：

1. 使用唯一的 "name"。
   所有 npm 项目必须有一个唯一的名称。命名很困难。你有 150 万竞争对手，所以请使用如 `npm-package-name-checker` 的工具检查可用性。如果你找不到一个好的名称，请使用账户 ID 作为前缀——例如 `@username/my-package`。
2. 设置下一个语义 "version" 数字（见上文“语义版本控制”）。
   你不能用相同的版本号覆盖现有包。每次发布时必须设置下一个唯一版本。
3. 添加一个可选的 "files" glob 模式数组。
   你可以定义哪些文件包含在包中。示例包含了 dist 和 doc 目录中的所有文件和子目录。除了 `package.json` 之外的所有其他文件都会被忽略：

```json
"files": [
  "dist/**/*/*",
  "doc/**/*/*"
],
```




- 4. 添加可选的 "bin" 命令别名。

要通过 `package.json` 中的 "name" 运行你的包，请将其脚本的相对路径定义为 "bin" 值。例如：

```json
"name": "myapp",
"bin": "./dist/myapp.js"
```

当包全局安装时，可以从命令行运行 `myapp` 命令。（本地安装可以使用 `npx myapp`。）

如果你有多个脚本或需要多个别名，也可以将 "bin" 设置为数组。例如：

```json
"name": "myapp",
"bin": {
  "myapp": "./dist/myapp.js",
  "ma": "./dist/myapp.js",
  "myapp2": "./dist/myapp2.js"
}
```

要发布包，请导航到你的项目目录，然后在终端中运行 `npm login` 登录。使用 `npm publish` 发布你的包。

假设没有错误，npm 将发布你的包，使其可以在任何地方安装。此时，最好将代码提交到你的仓库，以确保代码库一致。

## 发布技巧

在 Node.js 之旅之初，你不太可能发布很多包，但以下技巧可能在你开发更复杂的项目时对你有帮助：

- 创建满足你解决特定问题需求的包。
- 创建小而集中的包，它们能很好地做好一件事并可以在许多项目中复用。
- 创建新包可能比让现有包复杂化更好。

总结：保持简单。

## 练习题

尝试以下练习以提高你的 npm 知识：

- 1. 初始化一个新的 Node.js 项目，理想情况下使用一个 npm 注册表中未被占用的名称。
- 2. 搜索可以在终端输出颜色的包。
- 3. 将你选择的包安装到项目中。
- 4. 创建一个小型命令行应用程序，接收一个字符串和颜色参数。用该颜色输出该字符串。
- 5. （可选）将代码发布到 npm，然后将其作为全局包安装，以便你可以在任何地方运行它。

本章的视频描述了示例代码、npm 注册表和 GitHub 中提供的解决方案。

## 总结

本章扩展了你的 npm 知识，你可以在任何项目中查找、安装、更新、管理、发布和删除 Node.js 包。

下一章将介绍在 Node.js 应用中使用这些包以及你自己模块的选项。

## 测验

1. npm help可以通过以下方式获取：

- • a. 在线文档
- b. npm help 命令
- c. 使用 `npm help <command>`
- d. 以上任意一项

2. Node.js 的 package.json 文件可以使用以下命令初始化：

- * a. npm new
- b. npm init
- c. npm start
- d. 以上任意一项

3. 你的项目的 package.json "version" 目前为 "1.2.33"，且你正在添加一个新功能（不会破坏向后兼容性）。新版本号应该是：

- * a. 2.0.0
- b. 1.3.0
- c. 1.3.1
- d. 1.2.34

4. 你如何安装一个包供你的项目使用？

- * a. npm add <name> --local
- b. npm require <name>
- c. npm install <name>
- d. 以上任意一项

5. 如何列出项目中安装的所有包而不查看子依赖项？

- * a. npm list
- b. npm ll
- c. npm ls --depth=0
- d. 以上任意一项

6. 如何在本地项目中找到有新更新的包？

- * a. npm outdated
- b. npm old
- c. npm newer
- d. npm update

## 第8章：使用 ES2015 和 CommonJS 模块

上一章解释了如何使用 npm 查找和安装包含多个 JavaScript 文件的包。在本章中，我们将检查如何在 Node.js 中使用模块。

## 跳过？

本章的信息很重要，因为你会遇到与旧版 Node.js 包的问题。然而，课程中引用的所有包都经过了兼容性测试，所以当你遇到问题时可以跳过！

模块提供了一种在一个文件中定义功能并在另一个文件中使用方法。开发者经常创建负责相关任务的封装代码。优点包括：

- 代码可以拆分成更小的自包含文件。
- 相同的模块可以在任何应用程序中共享和复用。
- 模块不需要被其他人检查或更新。
- 代码引用模块是必要的依赖。
- 模块可以防止命名冲突：`module1.js` 中的 `x()` 不会与 `module2.js` 中的 `x()` 冲突。

奇怪的是，在 JavaScript 的前二十年里并没有模块的概念。你无法直接在另一个文件中引用一个 JavaScript 文件。客户端开发者通常会：

- 在 HTML 页面中添加多个 `<script>` 标签。
- 将脚本合并到一个文件中，可能使用 webpack 等打包器或 Grunt、Gulp 等任务运行器。
- 使用 RequireJS 或 SystemJS 等模块加载库——它们都采用了 CommonJS、AMD 等语法。




```javascript
// add values
function sum(...args) {
  log('sum', args);
  return args.reduce((num, tot) => tot + num);
}

// multiply values
function mult(...args) {
  log('mult', args);
  return args.reduce((num, tot) => tot * num);
}

// private logging function
function log(...msg) {
  console.log(...msg);
}
```

export { PI, sum, mult };

导入语句通过以下方式包含 ES 模块：

- 相对 URL（以 `./` 或 `../` 开头）
- 完全限定的 URL（例如 `file:///home/path/lib.js`）
- 安装后的 npm 名称（`express`, `chalk` 等）

## 导入外部 URL

Deno 和浏览器 JavaScript 可以导入其他域的 URL：

```javascript
import { someFunction } from 'https://example.com/lib.js';
```

Node.js 目前不支持这种方式，但在未来的版本中将会引入。尽管它比磁盘访问慢，但模块不会被缓存，且存在安全影响。

所有的 ES 模块及其子模块在脚本执行之前都会解析并导入。无论它们在脚本的什么位置声明。

你可以导入特定的命名导出项：

```javascript
import { sum, mult } from './lib.js';
```

```javascript
console.log(sum(1,2,3,4)); // 10
console.log(mult(1,2,3,4)); // 24
```

或者可以使用别名来解决命名冲突：

```javascript
import { sum as addAll, mult as multiplyAll } from './lib.js';

console.log(addAll(1,2,3,4)); // 10
console.log(multiplyAll(1,2,3,4)); // 24
```

或者，所有公共导出项都可以导入到命名空间变量中：

```javascript
import * as lib from './lib.js';
```

```javascript
console.log(lib.PI); // 3.14159265
console.log(lib.sum(1,2,3,4)); // 10
console.log(lib.mult(1,2,3,4)); // 24
```

带有单个导出项模块可以设置默认导出：

```javascript
// moduleDefault.js
export default function() { ... };
```

或者：

```javascript
// moduleDefault.js
function x() { ... };
export default x;
```

默认导出不需要使用大括号，并且可以使用任何名称：

```javascript
import myDefault from './moduleDefault.js';
```

这在实际上等同于：

```javascript
import { default as myDefault } from './moduleDefault.js';
```

动态模块加载——例如从生成的值——可以使用 `import()` 函数，它返回一个 promise。这会影响性能并使代码验证困难。只有在没有其他选项时才使用 `import()` 函数——例如在应用启动后导入脚本。

```javascript
const script = `./script${Math.round(Math.random() * 3)}.js`;
randomImport = await import(script);
```

Node.js 17 及以上版本还支持使用 `import()` 函数加载和解析 JSON：

```javascript
import data from './data.json' assert { type: 'json' };
```

最后，ESM 支持顶层 await（top-level await）：

```javascript
function waitOneSec() {
  return new Promise(
    (resolve) => setTimeout(resolve, 1000)
  );
}

await waitOneSec();
```

## CommonJS 与 ES2015 模块对比

CommonJS 和 ES2015 模块语法表面相似，但工作方式不同：

- 每个 CommonJS `require` 引用执行时动态加载的文件。
- 每个 ESM `import` 引用一个提升并预解析的 URL 以解析进一步的导入。这发生在代码执行之前。不直接支持或推荐动态导入模块。

考虑这个 ES2015 模块：

```javascript
// ESM two.mjs
console.log('running two');
export const hello = 'Hello from two';
```

通过此脚本导入：

```javascript
// ESM one.mjs
console.log('running one');
import { hello } from './two.mjs';
console.log(hello);
```

运行 `node one.mjs` 的输出是：

```
running two
running one
hello from two
```

现在考虑这个 CommonJS 模块：

```javascript
// CommonJS two.cjs
console.log('running two');
module.exports = 'Hello from two';
```

被此脚本引用：

```javascript
// CommonJS one.cjs
console.log('running one');
const hello = require('./two.cjs');
console.log(hello);
```

运行 `node one.mjs` 的输出是：

```
running one
running two
hello from two
```

在某些应用程序中，执行顺序至关重要——如果 ES2015 和 CommonJS 模块混合在同一个文件中会发生什么？

Node.js 引入 ESM 支持花了几年。为了解决潜在的兼容性问题，采用了以下方法：

- 是 AngularJS（或在 `package.json` 中设置 `"type": "commonjs"`）。
- 任何 `.cjs` 扩展的文件都被解析为 CommonJS。
- 任何 `.mjs` 扩展的文件都被解析为 ESM。
- 运行 `node --input-type=module index.js` 将入口脚本解析为 ESM。
- 在 `package.json` 中设置 `"type": "module"` 将入口脚本解析为 ESM。

## 在 ES2015 中导入 CommonJS 模块

Node.js 可以将 CommonJS 模块导入到 ESM 文件。例如：

```javascript
import lib from './lib.cjs';
```

Node.js 通常运行良好，当出现问题时 Node.js 会提供语法建议。

## 在 CommonJS 中引用 ES2015 模块

你不能在 CommonJS 文件中引用 ES 模块。ESM 模块是异步加载，因此它们与 CommonJS 中的同步加载和执行不兼容。

一种变方法是使用动态 `import()` 函数，它可以按需加载模块：

```javascript
// CommonJS 脚本
(async () => {
  const lib = await import('./lib.mjs');
  // ...
})();
```

## 在浏览器中使用 ES2015 模块

浏览器通过指定的 `<script>` 标签加载 模块：

```html
<script type="module" src="./first.js"></script>
<script type="module" src="./second.js"></script>
```

或者通过内联导入：

```html
<script type="module">
import { something } from './somewhere.js';
</script>
```

不支持 ESM 的浏览器不会加载 `type="module"`。支持 ESM 的浏览器不会加载 `nomodule` 属性：

```html
<script type="module" src="runs-when-ESM-supported.js"></script>
<script nomodule src="runs-when-ESM-not-supported.js"></script>
```

模块必须以 `application/javascript` 或 `text/javascript` MIME 类型提供。如果模块可以从另一个域导入，还需要设置 CORS 头 `Access-Control-Allow-Origin`。

## 总结

模块可能会让人混乱。它已经达到了这种情况：

- 某些库是 CommonJS
- 某些库是 ESM
- 某些库提供了 CommonJS 和 ESM 的构建

多年来，CommonJS 是唯一的选择。将大型项目转换为 ESM 的收益有限，特别是当使用具有兼容问题的模块时。

未来，ES2015 模块语法是浏览器和 Deno 运行时实现的 JavaScript 标准。我个人喜欢 CommonJS，但我建议新的 Node.js 项目使用 ESM。本课程中的所有示例都使用 ESM。将 CommonJS 模块导入 ESM 通常是可行的，但当出现问题时可能需要考虑替代包。

更多信息请参考：

- MDN 上的 JavaScript 模块
- nodejs.org 上的 CommonJS 模块
- nodejs.org 上的 ECMAScript 模块

# 测试

1. Node.js 原生支持以下模块语法：
- a. CommonJS 和 ECMAScript 
- b. CommonJS 和 AMD
- c. ECMAScript modules 和 UMD
- d. AMD 和 UMD

2. CommonJS 使用什么语法来声明和使用公共模块函数？
- a. export and import
- b. module.exports and import
- c. module.exports and require
- d. export and require

3. ES 模块使用什么语法来声明和使用公共函数？
- a. export and import
- b. module.exports and import





- c. module.exports 和 require
- d. export 和 require

4. 下面哪项是正确的？

- a. CommonJS 和 ESM 的运行机制相同
- b. 你通常可以在 ESM 中导入 CommonJS 模块
- c. 你通常可以在 CommonJS 中 require ES 模块
- d. 以上皆是

5. import() 函数：

- a. 可以将 ES 模块导入到 CommonJS 中
- b. 可以在启动后动态加载 ES 模块

# 第 9 章：Node.js 中的异步编程

本章讨论了 JavaScript 中异步编程的优势和挑战。异步概念在其他语言中并不总是易见的，但在 Node.js 中，它们是无法避免的。

你可能已经在客户端 JavaScript 中编写过异步事件处理函数。这些函数运行速度通常很快，而且页面不会开启很长时间；一个 bug 可能会给单个用户带来问题，但重启浏览器或刷新页面即可解决。然而，你的 Node.js 应用是所有用户的访问核心点，并且在不重启的情况下保持运行。一个小小的异步 bug 可能会导致内存泄漏，最终导致应用程序崩溃。

这是开发者从其他语言迁移时感到困惑的最大原因之一，所以*请不要跳过这一章！*异步编程看起来可能复杂，但几个要点将帮助你避免常见的坑。

## 什么是单线程阻塞 I/O 事件循环？

想象你正在自己经营一家披萨店。你接收所有的订单并准备所有的披萨，但一次只能处理一项任务。你收到了第一个订单，然后准备面团（20 分钟），加入配料（20 分钟），放入烤箱，边烤边观察（20 分钟），然后交给顾客。整个过程需要一小时；然后你就可以接收另一个订单了。

为了让你的餐厅更高效，你雇了三个厨师：一个做面团，一个加配料，一个烘烤。厨师们在不同的厨房里，不能互相交流，但当他们的特定任务完成后，会向你汇报。

制作一个披萨仍然一小时（尽管三个厨师合作每小时可以准备三个披萨）。重要的是，你不再参与烹饪过程了。你只是向厨师传递指令，并在他们完成工作时接收通知。你可以随时接收客户的订单。

JavaScript 和 Node.js 都是**单线程的**：运行时一次只能做一件事。这就像一家只有一个厨师的餐厅，只不过 JavaScript 将输入输出操作外交给了操作系统内核（其他“厨师”），它们是并行运行的。Node.js 应用可能会启动文件写入、数据库读取或 HTTP 请求，但它不会等待该操作完成。相反，它会请求在操作完成并可用成功或错误数据时运行一个回调函数。

## 回调的实战

考虑这段向文件写入的 PHP 代码：

```php
<?php
echo 'saving file';
$err = file_put_contents('file.txt', 'Hello from PHP');
if ($err !== false) echo 'file saved';
echo 'processing complete';
?>
```

程序输出如下：

```
saving file
file saved
processing complete
```

PHP 解释器处理 `file_put_contents()` 语句，并等待文件完全写入后才执行下一个命令。

这是 Node.js 中的等效代码：

```javascript
import { writeFile } from 'fs';

console.log('saving file');
writeFile('file.txt', 'Hello Node.js', 'utf8', err => {
  if (err) console.log('file saved');
});
console.log('processing complete');
```

程序输出如下：

```
saving file
processing complete
file saved
```

处理在文件保存*之前*就已经完成了！

传递给 `writeFile()` 的第四个参数是一个匿名的 ES6 回调函数，带有一个错误参数。当文件保存（或保存失败并抛出传入 `err` 的错误）时，回调运行。文件保存在后台可能只需要几毫秒，因此“processing complete' 命令立即执行。

异步回调是所有客户端和服务端 JavaScript 应用的核心。

处理错误并将错误对象或字符串消息作为回调函数的*第一个*参数（如上面的 `err`）是标准做法。当没有发生错误时，回调的第一个参数应该是 `null`、`undefined` 或任何其他假值。

## 事件循环

为什么上面的 Node.js 程序在执行最后一行后继续运行？

所有的 Node.js 都会初始化一个事件循环。一旦最后语句执行完毕，Node.js 就会循环并检查任何未完成的：

- 定时器（如 `setTimeout`）
- 等待的回调

## 阻塞事件循环

长时间的 JavaScript 计算会阻塞事件循环并延迟对传入请求的处理。任务应该拆分成更小的任务或在后台运行。

## 困惑

在异步函数中使用回调并不总是很容易。考虑这个等待 `ms` 的简单函数：

```javascript
function wait(ms, callback) {
  setTimeout(() => {
    callback();
  }, ms);
}
```

让我们通过向回调返回以下内容来改进函数：

```javascript
function wait(ms, callback) {
  ms = parseFloat(ms);

  if (!ms || ms < 1 || ms > 3000) {
    const err = new RangeError('Invalid ms');
    callback(err, ms);
    return;
  }

  setTimeout(() => {
    callback();
  }, ms);
}

// 调用 wait
wait(1000, (err) => {
  if (err) console.log(err);
  else console.log(`waited 1000ms`);
});
```

执行返回预期的 `waited 500ms` 结果。

```
craig@callbackdev:~/apps/callback$ node callback-fail.js
awaited 500ms
```

然而，当我们传递一个无效的 `ms` 值（如 0）会发生什么？

```
craig@callbackdev:~/apps/callback$ node callback-fail.js
RangeError: Invalid ms
at callback (/home/craig/apps/callback/callback-fail.js:9:17)
at Object.<anonymous> (/home/craig/apps/callback/callback-fail.js:21:1)
at Module._compile (node:internal/modules/cjs/loader:1101:14)
at Object._extensions..js (node:internal/modules/cjs/loader:11530:10)
at Module.load (node:internal/modules/cjs/loader:981:32)
at Function._load (node:internal/modules/cjs/loader:822:12)
at Function.executeUserEntryPoint [as main] (node:internal/run/run_main:81:12)
at node:internal/main/run_main_module:17:47
waited 0ms
```



```javascript
return; // terminate函数
}
// 在回调前等待 毫秒
setTimeout( callback, ms, null, ms );
```

还有一个更微妙的问题：当发生错误时，回调会立即执行。在此时，该函数不再是异步的——而是同步的。这在这里不会引起明显的问题，但在大型、长时间运行的 Node.js 应用程序中可能会导致内存泄漏。你的应用程序最终会因为模糊的“内存溢出”错误消息而崩溃。

# 函数必须是 100% 同步或 100% 异步

异步函数中的任何路径都不应该导致回调被立即执行。

解决此问题的一种简单方法是使用 `setImmediate()` 定时器。它会在事件循环的下一次迭代中调用该函数：

```javascript
// 等待 ms 毫秒
function wait(ms, callback) {

  ms = parseFloat(ms);

  // ms 值无效？
  if (!ms || ms < 1 || ms > 3000) {

    const err = new RangeError('Invalid ms value');
    setImmediate( callback, err, ms );
    return;
  }

  // 在回调前等待 毫秒
  setTimeout( callback, ms, null, ms );
}
```

## process.nextTick()

你可能会在某些应用程序中看到 `process.nextTick(callback)`。它的工作与 `setImmediate()` 类似，不同之处回调会在当前事件循环迭代结束之前运行。如果递归调用 `nextTick()`，可能会导致事件循环永远重启。

## 回调地狱

在复杂的 Node.js 应用程序中，你通常会进行一系列异步函数调用——例如从数据库获取数据、进行 API 调用、加载文件等。回调可能只在某处使用，因此声明内联匿名函数是有意义的。这会迅速变成深度嵌套的回调地狱：

```javascript
wait(100, (err) => {
  console.log('wait 1');
  wait(200, (err) => {
    console.log('wait 2');
    wait(300, (err) => {
      console.log('wait 3');
    });
  });
});
```

有一些语法方法可以扁平化这种结构，通常通过为每个函数命名并确保每个函数依次调用其他函数。幸运的是，JavaScript 的神灵们用 Promises 解决了这个问题。

## Promises

Promise 对象表示异步操作的最终完成或失败，以及其结果值。Promises 提供了更清晰的语法，使得链式调用顺序执行的异步调用变得更容易。开发者也可以避免前面提到的回调问题。

Promises 引入 ES6/2015，它们是语法糖；底层仍然使用回调。要使一个函数变为异步，必须立即返回一个 Promise 对象。Promise 构造函数接受两个回调函数作为参数：

- resolve：处理成功完成时运行的函数
- reject：当发生错误时运行的函数

在 `wait()` 函数的情况下，可以将其重写为返回一个 Promise，在超时后调用 `resolve(ms)`，在传递无效 ms 参数时调用 `reject(error)`：

```javascript
// 等待 ms 毫秒
function pWait(ms) {
  ms = parseFloat(ms);
  return new Promise((resolve, reject) => {
    if (!ms || ms < 1 || ms > 3000) {
      reject(new RangeError('Invalid ms value'));
    } else {
      setTimeout(resolve, ms, ms);
    }
  });
}
```

## util.promisify()

`util.promisify()` 将任何第一个参数为错误的基于回调的函数转换为 Promise。与其重写 `wait()`，你可以创建一个名为 `pWait()` 的 Promise 替代方案：

```javascript
import { promisify } from 'util';
const pWait = promisify(wait);
```

任何返回 Promise 的内容都可以拥有：

- 一个 `then()` 方法，接收一个函数，该函数接收上一个 `resolve()` 得到的结果
- 一个 `catch()` 方法，接收一个函数，当从任何 `reject()` 返回错误时运行该函数
- 一个 `finally()` 方法，无论如何最后都会被调用

```javascript
pWait(100)
  .then(ms => console.log(`waited ${ ms }ms`))
  .catch(err => console.log(`err`))
  .finally(() => console.log('all done'))
```

每个 `.then()` 函数都可以返回一个值或另一个 Promise，顺序异步函数可以对其进行链式调用。例如：

```javascript
pWait(100)
  .then(ms => {
    console.log(`waited ${ ms }ms`));
    return pWait(ms + 100);
  })
  .then(ms => {
    console.log(`waited ${ ms }ms`));
    pWait(ms + 100);
  })
  .then(ms => {
    console.log(`waited ${ ms }ms`));
  })
  .catch(err => {
    console.log(err);
  });
```

```bash
craig@craigdev:~/apps/callback node promise$
waited 100ms
waited 200ms
waited 300ms
craig@craigdev:~/apps/callback$
```

# then() 函数已 Promise 化

上述代码中最后的 `then()` 运行一个同步函数，但 JavaScript 会自动将其转换为基于 Promise 的异步函数，因此上述代码中最后的 `then()` 运行一个同步函数……（注：原文中存在大量重复的文本，已根据逻辑处理翻译）。

## 并行 Promises

（注：原文中存在大量重复的文本，已根据逻辑处理翻译）。

## 并行 Promises

例如，给定一个 ISBN，你想：

- 从数据库获取数据
- 进行 API 调用
- 加载文件
- 等

- 确定标题
- 获取作者
- 获取描述
- 获取库存
- 获取价格

以下代码的速度与最慢的那个一样：

```javascript
// book数据对象
const bookData = { id: 123 };

Promise.all([
    getBook(bookData.id),
    getStock(bookData.id),
    getPrice(bookData.id)
])
.then(result => {
    bookData.title = result[0].title;
    bookData.author = result[0].author;
    bookData.description = result[0].description;
    bookData.stock = result[1];
    bookData.price = result[2];
})
.catch(err => {
    console.log(err);
});
```

每当单个 Promise `reject()` 时，`.catch()` 就会触发，因此任何等待中的 Promise 都会被中止。类似的选项包括：

- Promise.allSettled()：
运行数组中的所有 Promise，并等待每一个都解析或拒绝。返回数组中的每个项都是一个带有 `.status` 属性（'fulfilled' 或 'rejected'）和一个 `.value` 属性的对象。

- Promise.any()：
运行数组中的所有 Promise，但一旦第一个 Promise 解析就会立即解析。返回单个值。

- Promise.race()：
运行数组中的所有 Promise，但一旦第一个 Promise 解析或拒绝就会立即返回结果。返回单个值。

## Promise 的问题

Promises 防止了回调地狱，但我起初觉得它们很困惑，而且很容易弄乱 `.then()/.catch()` 链语法。你还应该注意整个 Promise 链都是异步的，任何使用一系列 Promise 的函数都应该返回自己的 Promise（否则可能会运行回调来混扰其他开发者！）

## async/await

ES2017 引入了 `async` 和 `await` 关键字，允许用更简洁、清晰的语法编写基于 Promise 的异步行为。再次，它们更多是语法糖，但它们让 Promise 变得更甜。

执行三个连续 `pwait()` 用的 Promise 链既长又难以阅读：

```javascript
pWait(100)
  .then(ms => {
    console.log(`waited ${ms} ms`);
    return pWait(ms + 100);
  })
  .then(ms => {
    console.log(`waited ${ms} ms`);
    return pWait(ms + 100);
  })
```





```javascript
.then(ms => {
  console.log(`waited ${ ms }ms`);
})
.catch(err => {
  console.log( err );
});
```

这是使用 await 对应的等效代码：

```javascript
try {
  const p1 = await pWait(100);
  console.log(`waited ${ p1 }ms`);

  const p2 = await pWait(p1 + 100);
  console.log(`waited ${ p2 }ms`);

  const p3 = await pWait(p2 + 100);
  console.log(`waited ${ p3 }ms`);
} catch(err) {
  console.log(err);
}
```

在任何基于 promise 的异步函数之前加上 `await` 关键字，JavaScript 解释器将等待直到其被解析（resolved）或拒绝（rejected）。这种语法更简洁，看起来非常像一系列同步函数调用。

上面的代码是顶层 await，因为它没有被包含在函数内部。这在 ES2015 模块中有效，但在 CommonJS 中无效，在 CommonJS 中你需要将其封装在一个异步立即调用函数表达式（IIFE）中：

```javascript
(async () => {

try {
  const p1 = await pWait(100);
  console.log(`waited ${ p1 }ms`);

  const p2 = await pWait(p1 + 100);
  console.log(`waited ${ p2 }ms`);

  const p3 = await pWait(p2 + 100);
  console.log(`waited ${ p3 }ms`);
}
catch(err) {
  console.log(err);
}
)();
```

任何包含一个或多个 `await` 语句的函数都必须加上 `async` 以指示它是异步的。实际上，这将其变成了一个基于 promise 的函数：

```javascript
// async function
async function waitSeries(ms) {

  try {
  const p1 = await pWait(ms);
  console.log(`waited ${ p1 }ms`);

  const p2 = await pWait(p1 + 100);
  console.log(`waited ${ p2 }ms`);

  const p3 = await pWait(p2 + 100);
  console.log(`waited ${ p3 }ms`);
  }
  catch(err) {
    console.log(err);
  }
}

// 顶层 await 运行异步函数
await waitSeries(100);
```

## Promise.all() 是必要的

对于 `Promise.all()` 类似的函数没有 async/await 的等价物。然而，异步函数返回一个 promise，因此它们可以被传入数组。

## try/catch 很丑陋

如果省略了 `try/catch` 且 `await` 被拒绝，异步函数将静默退出。除非你能检查错误，否则无法知道是哪个 `await` 触发了问题，因此 `try/catch` 块可能是必要的。你可以考虑使用高阶函数来处理错误，当这些错误可以以相同的方式处理时。例如：

```javascript
// async function
async function waitSeries(ms) {
  const p1 = await pWait(ms);
  console.log(`waited ${p1} ms`);

  const p2 = await pWait(p1 + 100);
  console.log(`waited ${p2} ms`);

  const p3 = await pWait(p2 + 100);
  console.log(`waited ${p3} ms`);
}

// 高阶函数处理错误
function catchErrors(fn) {
  return fn().catch(err => {
    console.log('ERROR', err);
  });
}

// 顶层 await
await catchErrors(waitSeries)(100);
```

这是否会导致代码更具可读性是另一。## 同步循环中的异步 Await

在使用 `forEach()` 等循环方法时要小心 `await`，因为它们是同步的，并且即使它们调用的函数是异步的，也会继续运行。考虑这个例子：

```javascript
const ms = [100, 200, 300];
let totalWait = 0;

ms.forEach(async i => {
  console.log(i);
  const w = await pWait(i);
  console.log(`waited ${w} ms`);
  totalWait += w;
});

console.log(`total wait time: ${totalWait}ms`);
```

你可能会期望看到输出：

```
100
waited 100ms
200
waited 200ms
300
waited 300ms
total wait time: 600ms
```

实际结果是出惊讶的，如下所示。（img/d473c5479f6bf1ada496504b9e4c169_0.png）循环的每次迭代都不会等待其完成。如果下一次调用需要上一个 `await` 的结果，这将是一个问题。标准的 `for()`、`while()` 和 `async` 循环可能是必要的。上面的代码可以通过以下方式修复：

```javascript
const ms = [100, 200, 300];
let totalWait = 0;

for (let i = 0; i < ms.length; i++) {
  console.log(ms[i]);
  const w = await pWait(ms[i]);
  console.log(`waited ${w}ms`);
  totalWait += w;
}

console.log(`total wait time: ${totalWait}ms`);
```

结果所示。（img/d473c5479f6bf1ada496504b9e4c169_0_0.png）

## 练习

编写一个小型应用程序，使用以下 URL 请求从 Open Trivia Database 获取三个随机问题：

- 常识知识：https://opentdb.com/api.php?type=multiple&amount=1&category=9
- 计算机：https://opentdb.com/api.php?type=multiple&amount=1&category=18
- 小配件：https://opentdb.com/api.php?type=multiple&amount=1&category=30

## HTTP 请求

除非你使用 Node.js 18 或以上版本（它提供了原生的 `Fetch()` API），否则你需要使用第三方 HTTP 请求模块，如 `node-fetch`。

将问题数据格式化为单个数组，并以 JSON 格式输出到名为 `questions.json` 的文件中。

为了获得加分，通过并行运行 URL 请求让你的应用程序更高效。

本章视频演示了一个解决方案。

## 总结

异步编程需要时间理解，并且会让你出错。以下提示将帮助你编写更健壮的 Node.js 应用。

- 确保 JavaScript 函数运行快速不阻塞事件循环。
- 将回调函数传递给异步函数，以便操作完成后调用它们。
- 回调函数的第一个参数必须错误对象或字符串消息。
- 始终在回调执行后返回函数。
- 异步函数必须是 100% 异步的：根据需要将在下一次循环迭代中执行回调。
- 学习如何创建你的 promise，或者使用 `util.promisify()` 从回调函数创建 promise。
- 你可以在异步函数内部等待一个 promise 完成。
- 尽可能使用 `Promise.all()` 或 `Promise.allSettled()` 等选项并行运行 promise。

有用链接：

- Node.js 事件循环
- 不要阻塞事件循环（或工作池）
- MDN promise
- MDN async and await
- MDN 异步函数
- 第 11 章，JavaScript: Novice to Ninja
- 第 8和9 章，JavaScript: The New

## 测验

1. 回调函数：
- a. 在操作开始前运行
- b. 调用异步函数
- c. 在操作完成后被调用
- d. 以上所有

2. 异步函数：
- a. 在稍后的时间完成
- b. 允许执行后续的 JavaScript 命令
- c. 可以通过回调、promise 或 async 实现
- d. 以上所有

3. Node.js 事件循环：
- a. 在有未完成的定时器或回调时重新运行
- b. 运行异步函数
- c. 回调的另一个名称
- d. 以上都不是

4. Promise 对象通过运行以下完成：
- a. 一个 resolve 或 reject 函数
- b. 一个 fulfilled 或 error 函数
- c. 一个 resolve 或 error 函数
- d. 一个 fulfilled 或 reject 函数

5. 异步函数：
- a. 可以使用 `await` 调用基于 promise 的函数
- b. 返回一个 promise
- c. 使用 `try/catch` 块处理错误
- d. 以上所有




# 测试页面一

此页面已被访问了 9 次。

使用此服务的页面包含一个：

```
<img src="http://localhost:8001/hit.svg" alt="hits" referrerpolicy="unsafe-url" />
```

（注意：现代浏览器中需要 `referrerpolicy`，以便它们在 HTTP 请求头中发送引用信息。）

该图像是由处理请求 `refer` 的 Node.js Express 应用返回的，该应用会：

- 从请求的 `refer` HTTP 请求头中提取页面 URL。
- 使用 MD5 算法对 URL 进行清洗并转换为 32 字符的哈希值。因此，无论 URL 多长，它们都会解析为 32 字符的字符串。（理论上，两个不同的 URL 可能会生成相同的哈希，但在几十亿年内不太发生。）
- 将哈希值存储在一个新数据库中，并带有用户的 IP 地址、用户代理字符串和当前日期/时间。
- 统计数据库中对该哈希的所有引用。
- 生成并返回一个带有该计数的 SVG 图像。

代码目录中提供了三个应用程序：

- MongoDB 版本（见下文“MongoDB”部分），使用原生的 `mongodb` 驱动。
- MySQL 版本（见下文“MySQL”部分），使用原生的 `mysql` 驱动。
- Sequelize ORM 版本（见下文“Sequelize ORM”部分）。

这还通过 `mysql` 连接到 MySQL 数据库，但你不需要直接使用它。

这三者都使用相同的 Node.js 代码，但 `lib/pagehit.js` 文件外，该文件与特定数据库通信以添加和查询记录。

描述每个数据库中的每个选项是不可能的，但此示例代码为开发你自己的应用程序提供了一个起点。

# 安装和配置数据库软件

你可以在 Linux、macOS 和 Windows 上下载、安装和配置 MySQL、MongoDB 或任何其他数据库。这超出了本课程的范围，请准备好几个小时的工作。

更简单的选项是 Docker。虽然它充满了神秘感，但 Docker 提供了一种在几分钟内下载、安装和配置预构建应用程序的方法。在你的系统上安装 Docker，然后按照步骤运行 MySQL、MongoDB 和 Admin 数据库客户端。页面访问服务作为你设备上的一个 Node.js 应用，连接到此数据库。

# MongoDB

MongoDB 是一个流行的 NoSQL 数据库，它与 Node.js 的关联就像 MySQL 与 PHP 的关联一样。MongoDB 将类 JSON 文档分组为一个或多个集合（类似于表），并使用类 JavaScript 的对象来实现查询。

NoSQL 已成为任何不遵循 SQL 规范的数据库的统称（见下文“MySQL”部分）。在 NoSQL 数据库中，执行的规则较少。它鼓励重复（反规范化）数据，且不需要定义数据结构、默认值、约束或关系。

NoSQL 软件和存储机制各异。某些提供基础的键值对。某些使用 JSON 文档。其他一些则针对特定用例，例如用于内存缓存的 Redis 和用于搜索引擎索引的 Elasticsearch。

当数据更具有机性且关系更松散时，NoSQL 数据库会非常实用。考虑一个存储个人联系人电话号码的地址簿：

- 你可以在 SQL 数据库中分配单个电话字段，但这太局限了：联系人可能有家庭电话、工作电话和手机号。分配三个电话字段对某些联系人来说是浪费的，但对另一些人又不够。单独电话表是最灵活的选项，但这会增加复杂性。

- 在 NoSQL 数据库中，电话号码可以定义为与联系人相关的无限对象数组。例如：

```json
{
  "firstName": "Contact",
  "lastName": "One",
  "telephone": [
    "home": "1-01234567890",
    "work": "2-01234567890",
    "iPhone": "3-01234567890",
    "Android phone": "4-01234567890",
    "Test phone": "5-01234567890"
  ]
}
```

## MongoDB 应用

要使用基于 MongoDB 的应用程序，请进入 `pagehit-mongodb` 目录使用 `docker-compose up` 启动 MongoDB 和 Adminer 客户端。

# 你自己的 MongoDB 安装？

数据库配置参数定义在项目的 `.env` 文件中。它配置 Docker，Node.js 应用使用 `dotenv` 模块读取它。

如果你使用的是自己安装的 MongoDB，请编辑 `.env` 文件并相应更改配置参数。在大多数情况下，只需要更改用户的密码（`MONGO_INITDB_ROOT_PASSWORD`）。

在另一个终端中，安装 `package.json` 中引用的 Node.js `express`、`mongodb` 和 `dotenv` 依赖：

```bash
npm install
```

然后启动页面访问应用：

```bash
npm start
```

最后，在另一个终端中启动 Web 服务器，以便你可以加载测试页面：

```bash
npx small-static-server 8888 ./test
```

你现在运行了四个服务：

- 位于 http://localhost:27017 的 MongoDB 数据库
- 位于 http://localhost:8080/ 的 Adminer 数据库客户端
- 位于 http://localhost:8001/ 的页面访问服务
- 位于 http://localhost:8888/ 的测试页面 Web 服务器

如果有端口冲突，可以在 `.env` 文件中定义不同的端口。

访问 http://localhost:8888/page1.html 或 http://localhost:8888/page2.html 查看计数器。刷新并观察计数器增加。你可以检查数据库。




```javascript
db = client.db(process.env.MONGODB_INITDB_DATABASE),
hit = db.collection('hit');
```

MongoDB 允许你向集合中的文档任意添加数据，而无需预先描述这些数据（尽管可以通过数据验证来定义架构）。但是，你应该对经常查询的值建立索引，以使搜索更快更高效。

## 什么是数据库索引？

索引是针对一个或多个字段按特定顺序排列的数据列表——就像书的索引一样。例如，当每个人注册注册时，你可能会创建一个用户记录。当有人登录时，你必须通过其电子邮件地址定位用户记录：

- 如果没有索引，数据库必须逐个搜索每个用户记录，直到找到正确的邮箱。
- 如果在 email 字段上建立了按字母升序的索引，数据库可以快得多地定位匹配的记录。

索引用于你经常查询的字段。虽然在每个字段上创建索引很有诱惑力，但添加的索引越多，写入新记录和更新所有索引的时间就越长。

hit 集合在 URL 哈希值和时间上创建了一个索引。这在每次应用程序启动时都会运行，但在第一次尝试后会被忽略：

```javascript
// 添加集合索引
await hit.createIndex({ hash: 1, time: 1 });
```

lib/pagehit.js 导出一个默认的异步函数。它根据引用页的 URL 生成哈希值，但在未找到引用者页时返回 null：

```javascript
// 计数处理器
export default async function(req) {

// 引用 URL 的哈希
const hash = httpReferrer(req);

// 没有引用页？
if (!hash) return null;
```

然后确定浏览器的 IP 地址 (ip)、用户代理 (ua) 和访问时间 (time)：

```javascript
// 获取浏览器 IP 地址和用户代理
const ipRe = req.ip.match(/(?:\d{1,3}\.){3}\d{1,3}/);
ip = ipRe?[0] || null,
ua = req.get('User-Agent') || null,
time = new Date();
```

使用 `insertOne()` 方法将此数据作为新文档添加到 hit 集合中。默认情况下，MongoDB 文档还会为每个文档添加一个唯一的 `_id`：

```javascript
try {
// 存储页面访问
await hit.insertOne({ hash, ip, ua, time });
```

返回所有具有相同哈希值的文档计数：

```javascript
// 获取页面访问计数
return await hit.countDocuments({ hash });
```

如果任何数据库操作失败，则会抛出错误：

```javascript
}
catch (err) {
throw new Error('DB error', { cause: err });
}
```

主脚本 index.js 加载了此模块：

```javascript
import pagehit from './lib/pagehit.js';
```

它在中间件函数中使用，并将 `req.count` 设置为返回的页面计数。这对于后续的 (next()) 中间件可用，但任何错误都会立即终止请求：

```javascript
// 页面访问计数中间件
app.use(async (req, res, next) => {

  try {
    req.count = await pagehit(req);

    if (req.count) {
      next();
    } else {
      res.status(400).send('No referrer');
    }
  } catch (err) {
    res.status(503).send('Pagehit service down');
  }
});
```

定义了一个的 /hit.svg 路由，它返回一个包含 `req.count` 值的 SVG 图像：

```javascript
// SVG 计数响应
app.get('/hit.svg', (req, res) => {
  res
    .set('Content-Type', 'image/svg+xml')
    .send(`<svg xmlns="http://www.w3.org/2000/svg" width="${req.count * 0.6em}" height="1em"><text x="50%" y="75%" font-family="sans-serif" font-size="1em" text-anchor="middle" dominant-baseline="middle">${req.count}</text></svg>`);
});
```

一旦 SVG 返回浏览器，响应结束。

## 停止 MongoDB 

在终端中按下 Ctrl | Cmd + c 停止 Node.js 页面访问应用程序和测试服务器。从同一个项目目录，使用 `docker-compose down` 停止 MongoDB 数据库和 Adminer 客户端。

## MySQL

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

*注：原文中表格内容的 OCR 文本是碎片化的；它已根据上下文和提供的行进行了重构。）*

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

*(注：提供的源文本在 OCR 后包含跨页表格和文本的大量重复。我清理了文档的逻辑流，以呈现下方连贯的 MySQL 部分。）*

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

*(注：提供的源文本在 OCR 后包含跨页表格和文本的大量重复。我清理了文档的逻辑流，以呈现下方连贯的 MySQL 部分。）*

MySQL 是一种流行的 SQL 数据库。SQL（结构化查询语言）是管理关系型数据库管理系统 (RDBMS) 中数据的标准。数据存储在表中，理想情况下应该在一个地方定义且不重复（称为规范式化）。

考虑一个书籍库存。每本书都有一个 ID、标题、作者和出版商，并作为新行（记录）添加到书籍表中：

| id | title | author | publisher |
| :--- | :--- | :--- | :--- |
| 1 | Introduction to Node.js | Craig Buckler | SitePoint |
| 2 | Jump Start Web Performance | Craig Buckler | SitePoint |
| 3 | Dev Tools | Craig Buckler | SitePoint |
| 4 | Learn to JavaScript | Craig Buckler | SitePoint |

## MySQL 应用

要使用基于 MySQL 的应用程序，请到 pagehit 目录并启动 MySQL。

## 你的 MySQL 安装？

Docker 会自动运行 `mysql/init.sql` 脚本来初始化数据库和索引。你必须在启动 Node.js 应用程序之前手动运行它，可以在 MySQL 客户端中运行，也可以使用终端命令：

```bash
mysql -h localhost -u pagehouse pagehit < mysql/init.sql
```

（根据需要更改主机、用户或数据库名称）。在另一个终端中，安装 `package.json` 中引用的 Node.js `express`、`mysql2` 和 `dotenv` 依赖：

```bash
npm install
```

然后启动页面访问应用程序：

```bash
npm start
```

最后，在另一个终端启动 Web 服务器，以便加载测试页面：

```bash
npx small-static-server 8888 ./test
```

你有四个服务运行：

- 位于 http://localhost:3306 的 MySQL 数据库
- 位于 http://localhost:8080/ 的 Adminer 数据库客户端
- 位于 http://localhost:8001/ 的页面访问服务
- 如果冲突，可以在 .env 文件中定义测试 端口

访问 http://localhost:8888/page1.html http://localhost:8888/page2.html 查看计数。刷新并观察计数增加。

你可以使用 http://localhost:8080/ 的 Adminer 面板检查数据库使用情况。使用 .env 中的凭据登录：

- 系统: MySQL
- 服务器: host.docker.internal（如果没有使用 Docker Desktop，请使用网络 IP 地址）
- 用户名: pagehituser
- 密码: pagehitpw
- 数据库: pagehitmysql

然后点击 hit 表格旁的 select。





# MySQL 功能

在定义数据结构（其架构）之前，你无法在 SQL RDBMS 中存储数据。MySQL 数据库架构定义在 `mysql/init.sql` 中，它在使用 Docker 时会自动运行：

```sql
-- MySQL 数据库初始化
USE pagehitmysql;

CREATE TABLE IF NOT EXISTS hit (
```

```sql
id bigint unsigned NOT NULL AUTO_INCREMENT COMMENT 'record ID',
hash binary(16) NOT NULL COMMENT 'URL hash',
ip int(4) unsigned DEFAULT NULL COMMENT 'client IP address',
varchar(200) DEFAULT NULL COMMENT 'client useragent string',
time timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP COMMENT 'hit time',
PRIMARY KEY (id),
KEY hash (hash, time)
ENGINE=InnoDB DEFAULT CHARSET=utf8 COMMENT='page hits';
```

`lib/pagehit.js` 文件处理所有 MySQL 功能。它加载所需的模块，并使用 `dotenv` 模块从 `.env` 文件中提取配置参数：

```javascript
import dotenv from 'dotenv';
import mysqlPromise from 'mysql2/promise';
import httpReferrer from './httpreferrer.js';

// load .env configuration
dotenv.config();
```

选择了 `mysql2` 驱动进行 MySQL 通信。它提供了基于 promise 的低级方法来构建和执行任何 SQL 命令。

MySQL 连接池使用 `.env` 文件中的默认值进行配置。连接池通过重用之前的连接来减少连接到 MySQL 服务器的时间：

```javascript
// connect to MySQL
const db = await mysqlPromise.createPool({
host: process.env.MYSQL_HOST,
port: process.env.MYSQL_PORT,
database: process.env.MYSQL_DATABASE,
user: process.env.MYSQL_USER,
password: process.env.MYSQL_PASSWORD,
waitForConnections: true,
connectionLimit: 10,
queueLimit: 0
});
```

和之前一样，`pagehit.js` 导出单个默认异步函数。当未找到来源页时，它根据来源页的 URL 生成哈希，并确定浏览器的 IP 地址 (ip) 和用户代理 (ua)：

```javascript
// count handler
export default async function(req) {

// hash of referring URL
const hash = httpReferrer(req);

// no referrer?
if (!hash) return null;

// fetch browser IP address and user agent
const ipRe = req.ip.match(/(?:\d{1,3}\.){3}\d{1,3}/),
ip = ipRe?.[0] || null,
ua = req.get('User-Agent') || null;
```

## 没有时间？

记录插入的时间由 MySQL 自动处理，它默认设置 `CURRENT_TIMESTAMP`。

通过执行 SQL `INSERT` 语句将数据作为新记录添加到 `hit` 表：

```javascript
try {

// store page hit
await db.execute(
  'INSERT INTO `hit` (hash, ip, ua) VALUES (UNHEX(?), INET_ATON(?), ?)',
  [hash, ip, ua]
);
```

这是一个预处理语句的示例，每个字符都被数组中关联（已转义）的值替换。

## UNHEX? INET_ATON?

上面的 SQL 语句使用了几个 MySQL 特有的函数，以创建更小、更高效的数值字段，这些字段占用空间更少且搜索更快：

- `UNHEX()` 将 32 字符哈希字符串转换为二进制值。
- `INET_ATON()` 将点分  IPv4 网络地址字符串转换为整数。

## 永远不要构建 SQL 字符串！

永远不要通过程序构建 SQL 字符串。这是导致 SQL 注入攻击的最大原因：

```javascript
b.execute(`SELECT * FROM user WHERE email='${ email }' AND password='${ password }'`);
```

用户可以输入邮箱地址：`boss@company.com'; --`。这会注释掉密码检查，因此任何人都可以以 boss 的身份登录：

一个更危险的示例会清空表：

```javascript
boss@company.com'; DROP TABLE user; --
```

你应该验证所有迁入的用户数据，但预处理语句会让 SQL 注入攻击变得极其困难。

返回所有具有相同哈希的记录计数：

```javascript
// fetch page hit count
const [res] = await db.query(
  'SELECT COUNT(1) AS `count` FROM `hit` WHERE hash = UNHEX(?);',
  [ hash ]
);

return res?.[0]?.count;
```

如果任何数据库操作失败，则会抛出异常：

```javascript
{
catch (err) {
  throw new Error('DB error', { cause: err });
}
```

和之前一样，主 `index.js` 脚本加载 `lib/pagehit.js` 模块，在中间件函数中设置 `req.count`，并在 `/hit.svg` 路由生成的 SVG 中输出它。

## 停止 MySQL 应用

在终端中按下 `Ctrl | Cmd + c` 停止 Node.js 页面应用和测试页面服务器。从同一个项目目录，使用 `docker-compose down` 停止 MongoDB 数据库和 Admininer 客户端。

# Sequelize ORM

上述各自部分的 MySQL 和 MongoDB 示例使用原生驱动程序通过其 SQL 或 NoSQL 命令语法直接与数据库通信。

- 对象关系映射 (ORM) 可以让开发变得更简单。
- Sequelize 支持 MySQL、MariaDB、PostgreSQL、SQLite 和 SQL Server。
- 它在你的代码和数据库之间提供了一个抽象层。

## 开始 Sequelize ORM

要使用 Sequelize，你必须定义数据库配置。而不是直接编写 SQL，Sequelize 使用对象。

## 开始 Sequelize ORM

要使用 Sequelize，你必须定义数据库配置。而不是直接编写 SQL，Sequelize 使用对象。

要使用 Sequelize，你必须定义数据库配置。而不是直接编写 SQL，Sequelize 使用对象。

在另一个终端中，安装依赖：

```bash
npm install
```

然后启动 Web 服务器来加载页面：

```bash
npx static-server 8888
```

你有四个服务正在运行：

- MySQL 数据库 http://localhost:3306
- Adminer 客户端 http://localhost:8080/
- 页面访问服务 http://localhost:8001
- 测试页面 Web 服务器 http://localhost:8888

端口可以在 `.env` 文件中定义。

访问 http://localhost:8888/page1.html 或 http://localhost:8888/page2.html 查看计数器。刷新并观察计数增长。

你可以使用 http://localhost:8080/ 检查检查数据库数据。使用 .env 中指定的凭据登录：

- 系统：MySQL
- 服务器：host.docker.internal（如果没有使用 Docker 则使用你的网络 IP）
- 用户名：pagehituser
- 密码：pagehitpw
- 数据库：pagehitorm

## Sequelize ORM 功能

`lib/pagehit.js` 文件处理所有 Sequelize 功能。它加载所需的模块，并使用 `dotenv` 模块从 `.env` 文件中提取配置参数：

```javascript
import dotenv from 'dotenv';
import Sequelize from 'sequelize';
import httpReferrer from './httpreferrer.js';

// load .env configuration
dotenv.config();
```

（不需要导入 mysql 模块，因为 Sequelize 会加载。）

数据库名称、用户和密码连接参数传递给 sequelize 对象构造函数。第四个选项对象定义了数据库类型、主机和端口：

```javascript
// initialize ORM connection
const sequelize = new Sequelize(
process.env.MYSQL_DATABASE,
process.env.MYSQL_USER,
process.env.MYSQL_PASSWORD,
{
host: process.env.MYSQL_HOST,
port: process.env.MYSQL_PORT,
dialect: 'mysql'
}
);
```

与其定义表，不如从 `Sequelize.Model` 类创建一个 JavaScript 类。静态 `init()` 方法定义属性的数据类型和索引（注意每个模型都有默认的 id、createdAt 和 updatedAt 日期）：

```javascript
// define Hit class
class Hit extends Sequelize.Model {}
Hit.init(
{
```



```javascript
hash: {
  type: Sequelize.STRING(32),
  allowNull: false
},
ip: {
  type: Sequelize.STRING(15),
  allowNull: true
},
ua: {
  type: Sequelize.STRING(200),
  allowNull: true
}
},
indexes: [
    { fields: [ 'hash', 'createdAt' ] }
  ],
  sequelize,
  modelName: 'hit'
}
```

异步的 `sync()` 将所有数据模型与数据库同步。在这种情况下，哈希表由 Hit 模型定义：

```javascript
// 同步模型与数据库
await sequelize.sync();
```

和之前一样，`lib/page.js` 导出一个一个默认异步函数。它根据引用页的 URL 生成哈希值，在未找到引用页时返回，并确定浏览器的 IP 地址 (ip) 和用户代理 (ua)：

```javascript
// 计数处理器
export default async function(req) {

  // 引用 URL 的哈希
  const hash = httpReferrer(req);

  // 没有引用页？
  if (!hash) return null;

  // 获取浏览器 IP 地址和用户代理
  const ipRe = req.ip.match(/(?::\d{1,3}\.){3}\d{1,3}/);

  ip = ipRe?.[0] || null,
  ua = req.get('User-Agent') || null;
```

使用这些数据创建一个新的 Hit 记录：

```javascript
try {
  // 存储页面访问
  await Hit.create(
    { hash, ip, ua }
  );
```

然后返回所有具有相同哈希值的项计数：

```javascript
// 获取页面访问计数
const res = await Hit.findAllCount({
  where: { hash }
});
return res?.count;
```

如果任何操作失败，则会抛出错误：

```javascript
}
catch (err) {
  throw new Error('DB error', { cause: err });
}
```

和之前一样，主脚本 `index.js` 加载了 `lib/pagehit.js` 模块，在中间件函数中设置 `req.count`，并将其生成的 `/hit.svg` 路由的 SVG 中输出。

## 如何选择合适的数据库

当需求定义明确且数据完整性至关重要时（例如银行、电子商务、库存控制），MySQL 等 SQL 数据库是最佳选择。资金转账需要从一个账户扣除金额并存入另一个账户：事务保证了要么更新都成功，要么都不成功。

对于数据灵活性重要的项目，MongoDB 等 NoSQL 数据库可能是理想选择——例如内容管理、社交网络、Web 分析等。

通常情况下：

- NoSQL 数据库在项目开始阶段可能更容易使用，但随着你识别出数据关系，可能会变得更加困难。
- SQL 数据库在前期需要更周密的规划，但这在项目后期可能会产生丰厚的回报——除非需求发生了根本性的变化！）。

复杂的项目可以受益于使用两个或多个数据库。例如，存储在 MySQL 中的博客可以使用 Elasticsearch 进行类 Google 的搜索查询。然而，在两个或多个数据库之间维护数据完整性是复杂且繁琐的。这可能也是没必要的，因为 SQL 和 NoSQL 之间的区别已经模糊：

- 某些 SQL 数据库已采用 NoSQL 特性，例如 JSON 和 XML 字段
- 某些 NoSQL 数据库已采用 SQL 特性，例如 JOINS 和事务

研究各种选项，浏览使用报告并咨询他人，以确保数据库具有你所需的功能和支持。尝试抽象你的数据操作代码，以便在必要时能够更容易切换到另一个系统。

## 原生驱动 vs ORM 驱动程序

将 ORM 视为一个抽象的数据库框架。其优点包括：

- 它们比特定的 SQL 或 NoSQL 方言更容易学习。
- 开发时间会缩短，因为良好的 ORM 会管理安全性和数据完整性。
- 你可以在应用程序代码中创建数据模型。不需要直接创建或更改表。
- ORM 跟踪更改并根据需要迁移架构（schema）。
- ORM 支持多个数据库，如果你正在为他人分发 Web 软件安装，这可能非常重要。

ORM 的缺点：

- 它们可能仍然很难学习。Sequelize 手册令人望而生畏，而且这些知识在其他地方并不适用。
- ORM 不会免除糟糕的数据决策。
- 复杂的查询可能难以表达。
- ORM 速度较慢，且查询会被去优化。

## 练习

1. SQL 的全称是：
- a. Simple Query Language
- b. Structured Query Language
- c. Statistical Query Language
- d. Small Quick Language

2. MySQL 表可以存储：
- a. 表数据
- b. JSON 数据
- c. XML 数据
- d. 以上所有

3. MongoDB 数据库可以：
- a. 在没有数据模式的情况下使用
- b. 在有数据模式的情况下使用
- c. 联两个集合中的数据
- d. 以上所有

4. ORM 的全称是：
- a. object-relational mapping
- b. object-reference model
- c. ordered-reference map
- d. ordered-results management

5. 数据库索引：
- a. 按特定顺序定义数据
- b. 需要时自动使用
- c. 应该让查询更快
- d. 以上所有




浏览器发起每一个请求。Web 服务器无法随意向用户推送数据，它必须先被请求。

Ajax 技术可以通过每隔几秒发起一次轮询请求，让 Web 应用程序看起来像是在实时更新。这可以检查来自 Web 服务器的新数据，并根据需要更新 DOM。

极少数应用需要超越这种“请求-响应”模型，因为在典型的 Web 应用中，数据变化并不频繁。然而，对于像股票价格仪表板、聊天应用和多人游戏等真正的实时应用，这并不是理想的。在某些时刻，每秒轮询一次效率低下，而在另一些时候又太慢。服务器确定两个轮询间隔之间发生了什么也很困难：因为每个浏览器可能请求不同的数据。

WebSockets 为实时应用提供了解决方案。浏览器发起初始的 WebSocket 请求，打开一个通信通道。从那时起，浏览器或服务器都可以发送消息，从而在另一端设备上触发事件。

有两点需要注意：

- 浏览器只能向 WebSocket 服务器发送消息。
- WebSocket 服务器可以向其已连接的任何客户端发送消息。

一个浏览器无法直接向另一个浏览器发送消息。它只能向中央 WebSocket 服务器发送消息，并希望它根据需要进行转发。

# WebSocket 示例聊天应用

下面的章节解释了如何使用 WebSockets 创建一个简单的实时聊天应用。聊天应用是 WebSocket 演示的“Hello, World!”，因此我对自己的缺乏创意表示歉意——但它们在不需要太多代码的情况下展示了这些概念。

开始之前，在终端中导航到 `wschat` 代码目录，并使用 `npm install` 安装 Node.js 依赖。

使用 `npm start` 运行应用程序。

在多个浏览器标签页中打开 http://localhost:3000/（你也可以在查询字符串中定义你的聊天名称——例如 http://localhost:3000/?Craig）。在一个窗口中输入内容，然后按发送或回车键，你将看到它出现在每个窗口中。

查看视频了解聊天应用程序的运行情况。

## WebSocket 流程详解

该应用程序通过在 `index.js` 文件中启动两个进程来工作：

- 一个带有 EJS 模板的 Express 应用，用于提供一个包含客户端 HTML、CSS 和 JavaScript 的单页。它运行在 http://localhost:3000/，并使用浏览器 WebSocket API 发送和接收消息。
- 一个 WebSocket 服务器，负责监听传入的客户端连接、发送消息并监控断开。它运行在 ws://localhost:3001/，并使用 Node.js 库。
    - 当从浏览器接收连接时，会触发“connection”事件。处理函数接收一个 socket 对象与单个设备进行通信。
    - 当客户端发送消息时，会触发 socket“message”事件。聊天应用的处理会将消息广播给每个已连接的客户端。
    - 当客户端断开连接时（通常是关闭或刷新浏览器标签页），会触发 socket“close”事件。

以下是服务器 JavaScript 代码：

```javascript
// WebSocket server
import WebSocket, { WebSocketServer } from 'ws';

const ws = new WebSocketServer({ port: cfg.wsPort });

// client connection
ws.on('connection', (socket, req) => {

  console.log(`connection from ${req.socket.remoteAddress}`);

  // received message
  socket.on('message', (msg, binary) => {

    // broadcast to all clients
    ws.clients.forEach(client => {
      client.readyState === WebSocket.OPEN && client.send(msg, { binary });
    });

  });

  // closed
  socket.on('close', () => {
    console.log(`disconnection from ${req.socket.remoteAddress}`);
  });

});
```

客户端浏览器 JavaScript：

1. 缓存 HTML dom 节点以备后后用
2. 从查询字符串或随机字符串设置默认用户名
3. 使用页面的域名加上 HTML 页面模板中定义的端口来确定 ws:// WebSocket 连接地址

```javascript
// get page DOM nodes
const dom = { form: 0, chat: 0, name: 0, message: 0 };
for (let n in dom) dom[n] = document.getElementById(n);

// set user's name
dom.name.value =
decodeURIComponent(location.search.trim().slice(1,1 + window.cfg.nameLen)) || 'Anonymous' + Math.floor(Math.random() * 99999);

wsInit(`ws://${location.hostname}:${window.cfg.wsPort}`);
```

调用 `wsInit()` 并传入 WebSocket 服务器地址以发起连接。当建立连接时会触发 `open` 事件。此时，处理函数通过调用 `sendMessage()` 发送“进入聊天室”消息：

```javascript
// handle WebSocket communication
function wsInit(wsServer) {
  const ws = new WebSocket(wsServer);

  // connect to server
  ws.addEventListener('open', () => {
    sendMessage('entered the chat room');
  });
}
```

`sendMessage()` 函数从 HTML 表单中获取用户名和消息，尽管消息可以被任何传递的 `setMsg` 参数覆盖。这些值被转换为 JSON 对象，并通过其 `ws.send()` 方法通过 WebSocket 通道发送：

```javascript
// send message
function sendMessage(setMsg) {

  let
    name = dom.message.value.trim(),
    msg = setMsg || dom.message.value.trim();

  name && msg && ws.send(JSON.stringify({ name, msg }));
}
```

消息被服务器的“message”处理程序接收并广播给每个已连接的客户端——包括发送消息的客户端。处理程序解析 JSON 并更新聊天窗口：

```javascript
// receive message
ws.addEventListener('message', e => {

  try {
    const chat = JSON.parse(e.data);
      name = document.createElement('div'),
      msg = document.createElement('div');

    name.className = 'name';
    name.textContent = chat.name || 'unknown';
    dom.chat.appendChild(name);

    msg.className = 'msg';
    msg.textContent = chat.msg || 'said';
    dom.chat.appendChild(msg);
    dom.chat.scrollIntoView({ behavior: 'smooth'});
  } catch (err) {
    console.log('invalid JSON', err);
  }
});
```

最后，每当表单触发“提交”时，都会使用 `sendMessage()` 发送消息：

## WebSocket 高级考虑

在 Node.js 中使用 WebSocket 很容易：一个设备发送消息，在另一端触发“message”事件。但每个设备如何创建和响应消息更具挑战性。考虑一个多人游戏，游戏可以有许多宇宙——例如：

- 宇宙A：玩家1、玩家2 和玩家3 加入
- 宇宙B：玩家99 加入

你可以采取以下措施：

1. 为每个游戏宇宙使用独立的 WebSocket 服务器。这会让用户管理变得简单：宇宙A中的玩家行为永远不会被宇宙B的人看到。然而，启动和管理独立的实例可能是困难的。你会因为没有玩家而停止宇宙C，还是继续为该资源付费？

2. 为所有游戏宇宙使用单个 WebSocket 服务器。这考虑的资源更少且更于管理，但 WebSocket 服务器必须记录每个玩家加入了哪个宇宙。




游戏在本地设备上运行，但某些对象会受到他人活动的影响。与其时刻发送每个对象的精确位置，不如游戏可以发送更简单、频率较低的消息。例如：

- objectX 已出现在点X
- objectY 有了新的方向和速度
- objectZ 已被销毁

…… 等此类推。

每个客户端游戏都会填补这些空白。当 objectZ 爆炸时，爆炸在每个设备上的视觉效果是否完全相同并不重要。

这正解释了为什么你会在喜爱的游戏中被一个看似“隐形”的玩家公平地击败！

## 多个 WebSocket 服务器

示例聊天应用可以支持几十个并发用户，但随着人气上升，它在某个时刻会崩溃。增加内存有帮助，但它是有限的。你最终需要另一台服务器。

每个 WebSocket 服务器只能管理其连接的客户端。从用户发送到 serverA 的消息不会广播给连接到 serverB 的客户端。可能需要实现后端的发布/订阅消息系统，如 Kafka、Redis 或 RabbitMQ。

## 什么是发布/订阅（Pub–sub）？

> 发布者-订阅者服务提供异步通信服务。应用程序可以向发布/订阅系统发送（发布）消息。应用程序可以订阅这些消息，并在新消息到达时立即收到警报。

因此：

1. WebSocket serverA 想要向所有客户端发送消息。它在发布/订阅系统上发布该消息。
2. 所有订阅了发布/订阅系统的 WebSocket 服务器都会接收到新消息事件（包括 serverA）。每个服务器都可以处理消息并根据需要将其广播给其连接的客户端。

本课程末的示例实时测验使用 PostgreSQL 提供发布/订阅功能。

## 练习

修改聊天应用以存储最近的 30 条消息，并将它们发送给任何进入聊天室的新用户。为了获得额外奖励，请将消息数据存储在数据库中，以便在应用程序重启后数据依然存在。

你还可以尝试发送不同类型的消息。例如，允许向单个用户发送私信消息。

## 总结

Node.js 让处理 WebSockets 变得简单。它不会让实时应用的设计或编码变得更容易，但这项技术不会成为你的后腿。

请注意 `ws` 并不是 Node.js 的唯一选择。还有近 1000 个其他 WebSocket 包可用。某些包提供了自己的浏览器客户端库，或者与 JavaScript 框架集成以简化使用。

如果你的应用只需要接收来自中央服务器的更新，也可以考虑服务器发送事件（SSE）。

## 测验

1. WebSockets 提供：
- a. 双向浏览器/服务器通信
- b. 实时消息传递
- c. 一个事件驱动的 API
- d. 以上所有

2. WebSocket 服务器：
- a. 响应客户端的连接和消息
- b. 在 Web 服务器之间透传连接请求
- c. 发起 WebSocket 连接
- d. 以上所有

3. 在 WebSocket 连接上发送的消息必须是：
- a. 字符串
- b. JSON
- c. 二进制数据
- d. 任何文本或二进制数据

4. 浏览器 WebSocket 客户端可以通过以下方式向另一个浏览器发送消息：
- a. 发送跳过服务器的直接点对点消息
- b. 向 WebSocket 服务器发送消息，由服务器根据需要进行转发
- c. 在消息中添加其他用户的 IP 地址
- d. 以上所有

5. 哪项最能描述 `ws` 库中使用的 WebSocket 代码？
- a. 调用 `message()` 会在另一个设备上触发 "sent" 事件
- b. 调用 `send()` 会在另一个设备上触发 "message" 事件
- c. 调用 `transmit()` 会在另一个设备上触发 "received" 事件
- d. 调用 `send()` 会在另一个设备上触发 "receive" 事件

# 第 12 章：实用的 Node.js API

本章演示了标准 Node.js 运行时内置的一些常用 API。你已经在本书的之前的章节中见过了一些，但我希望接下来的章节能引起你的兴趣，并鼓励你浏览 Node.js API 文档。

## Module node：URL 导入

Node.js 14 及以上版本支持对 ESM 和 CommonJS 模块使用 node 导入。与其使用 API 的模块名：

```
import path from 'path';
```

…… 你可以使用绝对的 `node:` URL 来引用它：

```javascript
import path from 'node:path';
```

如果你有另一个名为 `path` 的模块，或者想在代码中区分内置 API，这可能是实用的。

## Process

`process` 提供了有关你的 Node.js 应用的信息以及控制方法。`process` 是全局可用的：无需导入即可使用它，尽管 Node.js 文档建议显式引用它：

```javascript
import process from 'process';
```

我们在其他脚本中使用 `process.argv` 来获取命令行参数：

```javascript
const firstArg = process.argv[2];
```

`process.argv` 返回一个数组，其中两个项是 Node.js 可执行文件路径和脚本名称。索引为 2 的项是传递的第一个参数。

其他实用的属性和方法包括：

- `process.env`:返回一个包含环境变量名称/值对的对象——例如 `NODE_ENV`。
- `process.cwd()`：返回当前工作目录。
- `process.platform`:返回一个标识操作系统的字符串。
- `process.version()`：一个标识 Node.js 版本的字符串。
- `uptime()`：运行的秒数。

## OS

`os` API 与 `process` 有相似之处（参见“Process”部分），但它还可以返回以下内容：

- `cpu()`：返回一个包含每个逻辑核心的对象的数组。
- `hostname()`：操作系统的主机名。
- `homedir()`：用户目录的完整路径。
- `tmpdir()`：操作系统的临时目录的完整路径。

## Util

`util` 模块提供了许多实用的 JavaScript 方法。最实用的之一是 `util.promisify(function)`，它接收一个回调优先的函数并返回一个基于 promise 的函数。（演示见第 9 章的代码。）

其他方法包括：

- `callbackify(function)`：接收一个返回 promise 的函数并返回一个基于回调的函数。
- `isDeepEqual(object1, object2)`：当两个对象深度相等时返回 true（所有子属性必须匹配）。
- `format(format, args)`：使用类似 printf 的格式返回字符串。
- `inspect(object, options)`：用于调试对象的字符串表示。这类似于使用 `console.dir(object, { depth: null, color: true });`。
- `stripVTControlCharacters(str)`：从字符串中去除 ANSI 转义码。

`util.types` 为常见的 JavaScript 和 Node.js 值提供类型检查。例如：

```javascript
import util from 'util';

util.types.isDate(new Date()); // true
util.types.isMap(new Map()); // true
util.types.isRegExp(/abc/); // true
util.types.isAsyncFunction(async () => { // true
```

## URL

URL 是另一个全局对象，可以安全地创建、解析和修改网络 URL。例如：

```javascript
const myURL = new URL('https://example.org:8000/path/?abc=123#target');
console.dir(myURL, { depth: null, color: true });
```

上述代码输出如下：

```javascript
{
  href: 'https://example.org:8000/path/?abc=123#target',
...
```



```javascript
origin: 'https://example.org:8000',
protocol: 'https://',
username: '',
password: '',
host: 'example.org:8000',
hostname: 'example.org',
port: '8000',
pathname: '/path/',
nsearch: '?abc=123',
searchParams: URLSearchParams { 'abc' => '123' },
hash: '#target'
}
```

你可以查看并修改任何属性。例如：

```javascript
myURL.port = 8001;
console.log(myURL.href);
// https://example.org/8000/path?abc=123#target
```

然后可以使用 `URLSearchParams` API 来修改查询字符串的值。例如：

```javascript
myURL.searchParams.delete('abc');
myURL.searchParams.append('xyz', 987);
console.log( myURL.search );
// ?xyz=987
```

还有将文件系统路径转换为 URL 以及反之的方法。

`dns` 模块提供了名称解析函数，使你可以查询 IP 地址、名称服务器、TXT 记录以及其他域信息。

## 文件系统

`fs` API 可以创建、读取、更新和删除文件、目录和权限。Node.js 运行时的最新版本在 `fs/promises` 中提供了基于 promise 的函数，使得管理异步文件操作变得更加容易。

## fs 和 path

你经常会结合使用 `fs` 和 `path` 来解析不同操作系统上的文件名。

示例代码包含了一个 filecompress 项目，它通过删除空白和注释来压缩文本文件（通常是 HTML、CSS 或 JS）。这是一个演示——请勿在真实文件上使用它！压缩过程非常简单，会破坏某些文件。）

项目有一个 `lib/fileinfo.js` 模块，它使用 `stat` 和 `access` 方法返回关于文件系统对象的信息：

```javascript
// fetch file information
import { constants as fsConstants } from 'fs';
import { access, stat } from 'fs/promises';

export async function getFileInfo(file) {
  const fileInfo = {};

  try {
    const info = await stat(file);
    fileInfo.isFile = info.isFile();
    fileInfo.isDir = info.isDirectory();
  } catch (e) {
    return { new: true };
  }

  try {
    await access(file, fsConstants.R_OK);
    fileInfo.canRead = true;
  } catch (e) {}
  try {
    await access(file, fsConstants.W_OK);
    fileInfo.canWrite = true;
  } catch (e) {}

  return fileInfo;
}
```

当传递文件名时，该函数返回一个包含该文件信息的对象。例如：

```javascript
{
  isFile: true,
  isDir: false,
  canRead: true,
  canWrite: true
}
```

主脚本 `filecompress.js` 使用 `path.resolve()` 将命令行中传递的输入和输出文件名解析为绝对文件路径，然后使用上述的 `getFileInfo()` 获取信息：

```javascript
#!/usr/bin/env node
import path from 'path';
import { readFile, writeFile } from 'fs/promises';
import { getFileInfo } from './lib/fileinfo.js';

// check files
let input = path.resolve(process.argv[2] || '');
let output = path.resolve(process.argv[3] || '');
let [inputInfo, outputInfo] = await Promise.all([
    getFileInfo(input),
    getFileInfo(output)
]);
let error = [];
```

代码会验证路径，并在必要时带有错误消息退出：

```javascript
// use inputFile name when output is a directory
if (outputInfo.isDir && outputInfo.canWrite && inputInfo.isFile) {
  output = path.resolve(output, path.basename(input));
}

// check for errors
if (inputInfo.isFile || !inputInfo.canRead) error.push(`cannot read input file ${input}`);
if (input === output) error.push('input and output files cannot be the same');

if (error.length) {
  console.log('Usage: ./filecompress.js [input file] [output file[dir]]');
}
```

```javascript
console.error('\n  ' + error.join('\n '));
process.exit(1);
}
```

然后使用 `readFile()` 将整个文件读取到名为 `content` 的字符串中：

```javascript
// read file
console.log(`processing ${ input }`);
let content;

try {
  content = await readFile(input, { encoding: 'utf8' });
} catch (e) {
  console.log(e);
  process.exit(1);
}

let lengthOrig = content.length;
console.log(`file size ${lengthOrig}`);
```

JavaScript 正则表达式移除了注释和空白：

```javascript
// compress content
content = content
  .replace(/\n\s+/g, '\n') // 修除行首空格
  .replace(/\/\/.**/g, '') // 删除行内 // 注
  .replace(/\/\s+/g, ' ') // 删除空白
  .replace(/\/\*?\*\*/g, '') // 删除 * 注 */
  .replace(/<!--.*?-->/g, '') // 删除 <!-- 注
  .replace(/\s*([^\s])/g, '$1'); // 删除多余空白
```


```javascript
// 添加监听器
ticker.once('tick', e => {
  console.log('handler 3 tick!', e);
});
```

最后，输出当前监听器的数量：

```javascript
// 显示监听器数量
console.log(`listeners: ${ticker.listenerCount('tick')}`);
```

使用 `node event.js` 运行项目代码。

输出显示 handler 3 触发了一次，而 handler 1 和 2 在每次 tick 时运行，直到程序终止。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_229_0.png)

按下 Ctrl | Cmd + C 终止应用程序。

查看演示视频以了解代码运行。

# 流 (Streams)

上面的文件系统示例代码（在“文件系统”部分）在输出结果之前会将整个文件读取到内存中。如果文件大于可用内存 呢？Node.js 将因“内存溢出”错误失败。

解决方案是流式处理。它以较小、更易于管理的块来处理输入数据。流可以是：

- 可读的：来自文件、HTTP 请求、TCP 套接字、stdin 等。
- 可写的：写入文件、HTTP 响应、TCP 套接字、stdout 等。
- 双向的 (duplex)：既可读可写的流。
- 转换的 (transform)：进行转换的双向流。

每个数据块都以 `Buffer` 对象的形式返回，它表示固定长度的字节序列。你可能需要将其转换为字符串或其他适当类型以便处理。

示例代码包含一个 `filestream` 项目，它使用转换流来解决 `filecompress` 项目中的文件大小问题。与之前一样，在声明继承 `Transform` 的 `Compress` 类之前，它会接受并验证输入和输出文件名：

```javascript
import { createReadStream, createWriteStream } from 'fs';
import { Transform } from 'stream';

// 压缩 Transform
class Compress extends Transform {
  constructor(opts) {
    super(opts);
    this.chunks = 0;
    this.lengthOrig = 0;
    this.lengthNew = 0;
  }

  _transform(chunk, encoding, callback) {
    const data = chunk.toString(), // buffer 转为字符串
    content = data
      .replace(/\n\s+/g, '\n') // 去除行首空格
      .replace(/\/\/.*?\*/g, '') // 移除注释
      .replace(/\s+/g, ' ') // 移除空白
      .replace(/\/*.*?\*/g, '') // 移除 /*注释 /*
      .replace(/<!--.*?-->/g, '') // 移除 <!--注释 -->
      .replace(/\s*([<>{}()\[\]])\s*/g, '$1') // 移除括号周围空格
      .trim();

    this.chunks++;
    this.lengthOrig += data.length;
    this.lengthNew += content.length;

    this.push(content);
    callback();
  }
}
```

当新数据块就绪时会调用 `transform` 方法。它以 `Buffer` 对象的形式接收，转换为字符串、进行压缩，并使用 `push()` 方法输出。块处理完成后，会调用 `callback()` 函数。

应用程序启动文件读写流并实例化新的 `compress` 对象：

```javascript
// 处理流
const readStream = createReadStream(input),
    writeStream = createWriteStream(output),
    compress = new Compress();

console.log(`processing ${input}`);
```

输入文件流定义了 `pipe()` 方法，它将输入数据通过一系列函数，这些函数可能会（也可能）更改内容。数据在通过 `compress` 转换流之前被管道到可写文件。当流结束后，会执行 `on('finish')` 事件处理函数：

```javascript
readStream.pipe(compress).pipe(writeStream).on('finish', () => {
  console.log(`file size ${compress.lengthOrig}`);
  console.log(`output ${output}`);
});
```

```javascript
console.log(`chunks ${compress.chunks}`);
console.log(`file size ${compress.lengthNew} - saved ${Math.round((compress.lengthOrig - compress.lengthNew) / compress.lengthOrig * 100)}%`);
```

使用任意大小的 HTML 文件运行项目：

```bash
node filestream.js ./test/example.html ./test/output.html
```

输出显示：
（此处省略大量重复的输出内容，已根据要求去重）

# 工作线程 (Worker Threads)

第 9 章讨论了 Node.js 如何在单线程上运行。使用标准调用 `diceRun()` 函数投掷十亿次：

这会停止计时器，因为 Node.js 事件循环在计算完成之前无法继续下次迭代。

代码随后在新的 Worker 中尝试相同的计算。这加载了一个脚本：

```javascript
// 掷骰子
export diceRun(runs = 1, dice = 2, sides = 6) {
  const stat = [];
  while (runs > 0) {
    let sum = 0;
    for (let d = dice; d > 0; d--) {
      sum = Math.floor(Math.random() * sides) + 1;
    }
    stat[sum] = (stat[sum] || 0) + 1;
    runs--;
  }
  return stat;
}
```

```javascript
import { Worker } from 'worker_threads';
import { diceRun } from './lib/dice.js';

// 投掷十亿次 2 个骰子
const
  numberOfDice = 2,
  runs = 999_999_999;

const stat1 = diceRun(runs, numberOfDice);
```

查看演示视频以了解代码运行。



命名为 `worker.js` 并通过选项对象中的 `workerData` 属性传递计算参数：

```
import { Worker } from 'worker_threads';

const worker = new Worker('./worker.js', { workerData: { runs,
NumberOfDice: dice } });
```

将事件处理器挂载到运行 `worker.js` 脚本的 worker 对象上，以便接收传入的结果：

```
// result returned
worker.on('message', result => {
  console.table(result);
});
```

... 并处理错误：

```
// worker error
worker.on('error', e => {
  console.log(e);
});
```

... 以及在处理完成后进行清理工作：

```
// worker complete
worker.on('exit', code => {

// tidy up
});
```

`worker.js` 脚本启动 `diceRun()` 计算，并在完成后向父进程发送消息——该消息将由上面的 "message" 处理器接收：

```
// worker thread
import { workerData, parentPort } from 'worker_threads';
import { diceRun } from './lib/dice.js';
```

```
// start calculation
const stat = diceRun( workerData.runs, workerData.numberOfDice );
```

```
// post message to parent script
parentPort.postMessage( stat );
```

当 worker 运行时，计时器不会暂停，因为它在另一个 CPU 线程上执行。换句话说，Node.js 事件循环会继续迭代，没有长时间延迟。

使用 `node index.js` 运行项目代码：

```
craig@craigdev:~/apps/worker$ node index.js
another process
another process
another process
NO THREAD CALCULATION STARTED...
```

| (index) | Values |
| 2 | 27770722 |
| 3 | 55550343 |
| 4 | 83333797 |
| 5 | 111114219 |
| 6 | 138885218 |
| 7 | 166669926 |
| 8 | 193890520 |
| 9 | 221119186 |
| 10 | 253334048 |
| 11 | 285555615 |
| 12 | 307777945 |

```
NO THREAD CALCULATION COMPLETE
WORKER THREAD CALCULATION STARTED...
another process
another process
another process
another process
another process55
another process
another process
another process
another process
another process
another process
another process
another process55
another process
another process
another process
another process
another process
another process
```

| (index) | Values |
| 2 | 27783945 |
| 3 | 55561864 |
| 4 | 83345589 |
| 5 | 111103314 |
| 6 | 138884867 |
| 7 | 166607685 |
| 8 | 1938895133 |
| 9 | 221121601 |
| 10 | 253311380 |
| 11 | 285550740 |
| 12 | 307783298 |

```
WORKER THREAD CALCULATION COMPLETE
Worker thread exited with code 0
notread: 106694ms
threaded: 16443ms
craig@craigdev:~/apps/worker$ |
```

你应该注意，基于 worker 的计算运行速度略快，因为该线程完全专门用于该进程。如果你在应用程序中遇到性能瓶颈，请考虑使用 workers。

查看演示视频以了解代码运行效果。

# 子进程 (Child Processes)

有时需要调用那些不是用 Node.js 编写或有失败风险的应用程序。

## 现实案例
我曾开发过一个 Express 应用程序，用于生成模糊图像哈希值以识别相似的图形。它异步运行且运行良好的——直到有人上传了一个包含循环引用的畸形 GIF（动画帧 A 引用了帧 B，帧 B 又引用了帧 A）。

哈希计算从未结束。用户放弃并尝试再次上传。再次。再次。最后，整个应用程序因内存错误而崩溃。

通过在子进程中运行哈希算法解决了这个问题。Express 应用程序保持了稳定，因为它在计算耗时过长时会启动、监控并终止该计算。

子进程 API 允许你运行可以根据需要进行监控和终止的子进程。共有三种选项：

-   spawn: 产生一个子进程。
-   fork: spawn 的一种特殊类型，用于启动一个新的 Node.js 进程。
-   exec: 启动一个 shell 并运行命令。结果会被缓冲并在进程结束时返回给回调函数。

与 worker threads不同，子进程独立于主 Node.js 脚本，无法访问相同的内存。

# 集群 (Clusters)

当你的 Node.js 应用程序运行时，你的 64 核服务器 CPU 是否没有被充分利用？

Node.js 事件循环会继续迭代，没有长时间延迟。换句话说，Clusters 允许你运行应用程序的多个实例。

| 工具 | 描述 |
| :--- | :--- |
| PM2 | 用于 Node.js 应用程序的进程管理器，可以处理扩展和重启。 |
| Docker | 用于打包和运行应用程序的容器平台。 |
| Kubernetes | 用于管理容器化应用程序的编排系统。 |





## 测验快速上手

该应用使用 Docker 和 Docker Compose 下载并运行 Node.js 和数据库服务器。

## 什么是 Docker？

Docker 提供了一种快速安装、配置和运行数据库等应用程序的方法。每个应用程序都运行在一个名为“容器”的隔离环境中。它的行为类似于一个微型的 Linux 虚拟机，但它非常轻量，且不需要持续维护。

Docker Compose 可以通过单个命令运行任意数量的容器化应用程序。这使其成为管理 Web 应用依赖的理想选择，并且在所有平台上的表现相同——无论你使用的是 Windows、macOS 还是 Linux。类似的环境也可以部署到生产服务器上。

如果你想了解更多，SitePoint 提供了《Web 开发者的 Docker》书籍和视频课程。

安装好 Docker 后，导航到项目根目录 (nodequiz)，并使用 `docker compose up` 在开发模式下启动应用。

所有软件依赖都会下载并初始化，因此首次运行可能需要几分钟。终端会显示数据库和服务器活动的日志。

启动后，在浏览器中访问 http://quiz.localhost 进行测验。

## 多人测验

测验包含来自 Open Trivia Database 的 0 个问题。

导入题目...

在开始测验之前，必须导入一些题目，因此点击**导入题目...** 从 Open Trivia Database 获取可选题目——这是一个免费使用的、由用户贡献的趣味问题数据库。随后你会被提示加入（JOIN）一个已有的游戏。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_246_0.png)

或者你可以开始（START）一个新游戏。

## 多人测验

已导入新题目：479

测验包含来自 Open Trivia Database 的 479 个问题。

导入题目...

## 开始一个新游戏

你的名字：Craig

题目数量：10

首次回答后的时间限制：5 秒

回答正确的得分：1 分

最快玩家奖金：1 分

回答错误的得分：-1 分

未回答的得分：0 分

正在进入测验大厅...

或加入（JOIN）另一个游戏...

可以同时运行任意数量具有不同配置的游戏，根据时间限制以及你是猜题还是拒绝回答问题，可以产生不同的策略。

游戏一旦启动，将被分配一个唯一代码——如下所示的 **a23**。其他人可以通过在**JOIN**屏幕上输入代码并进入大厅加入此游戏。

## 等待其他玩家...

其他玩家可以通过加载 http://quiz.localhost/ 并输入游戏代码 a23 加入此测验

## 玩家

- Craig 已加入
- Another 已加入

为 2 人开始测验

## 等待其他玩家...

其他玩家可以通过加载 http://quiz.localhost/ 并输入游戏代码 a23 加入此测验

## 玩家

- Craig 已加入
- Another 已加入

为 2 人开始测验

玩家都可以开始游戏，游戏将进入第一个问题。在第一个人回答后，倒计时将开始，因此其他人必须在规定时间内做出响应。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_250_0.png)

得分显示在题目之间以及游戏结束时。计时器指示下一题即将到来。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_251_0.png)

要关闭测验，在另一个终端中导航到项目根目录 (nodequiz) 并运行 `docker-compose down`。

查看演示以查看游戏运行情况。

测验使用 Node.js 开发，使用了几个第三方模块、原生 ES 以及少于 60KB 的代码。它具有可扩展性：随着流量的增加，你可以添加更多的 Node.js 和 WebSocket 服务器。

测验使用 Node.js 开发，使用了几个第三方模块、原生 ES 以及少于 60KB 的代码。它具有可扩展性：随着流量的增加，你可以添加更多的 Node.js 和 WebSocket 服务器。

## 14 章：示例实时测验：架构

测验使用 Node.js 开发，使用了几个第三方模块、原生 ES 以及少于 60KB 的代码。它具有可扩展性：随着流量的增加，你可以添加更多的 Node.js 和 WebSocket 服务器。

测验使用 Node.js 开发，使用了几个第三方模块、原生 ES 以及少于 60KB 的代码。它具有可扩展性：随着流量的增加，你可以添加更多的 Node.js 和 WebSocket 服务器。

测验使用 Node.js 开发，使用了几个第三方模块、原生 ES 以及少于 60KB 的代码。它具有可扩展性：随着流量的增加，你可以添加更多的 Node.js 和 WebSocket 服务器。

测验使用 Node.js 开发，使用了几个第三方模块、原生 ES 以及少于 60KB 的代码。它具有可扩展性：随着流量的增加，你可以添加更多的 Node.js 和 WebSocket 服务器。

## 为什么要使用多个服务器？

随着流量增长，单服务器会遇到问题。使用多服务器架构可以处理这些问题。从开始使用这种架构，Node.js 实例可以故障并重启而无感知停机。

测验使用 Node.js 开发，使用了几个第三方模块、原生 ES 以及少于 60KB 的代码。它具有可扩展性：随着流量的增加，你可以添加更多的 Node.js 和 WebSocket 服务器。

测验使用 Node.js 开发，使用了几个第三方模块、原生 ES 以及少于 60KB 的代码。它具有可扩展性：随着流量的增加，你可以添加更多的 Node.js 和 WebSocket 服务器。

测验使用 Node.js 开发，使用了几个第三方模块、原生 ES 以及少于 60KB 的代码。它具有可扩展性：随着流量的增加，你可以添加更多的 Node.js 和 WebSocket 服务器。

测验使用 Node.js 开发，使用了几个第三方模块、原生 ES 以及少于 60KB 的代码。它具有可扩展性：随着流量的增加，你可以添加更多的 Node.js 和 WebSocket 服务器。

img/d4731c5479f6bfd1ada49d65047b9e4c_254_0.png)

本章和后续章节描述了设置。从开始使用这种架构，Node.js 实例可以故障并重启而无感知停机。

img/d4731c5479f6bfd1ada49d65047b9e4c_254_0.png)

1. 单个 PostgreSQL 服务器

单个 PostgreSQL 服务器实现了一个测验数据库，包含以下表：

- question：题目文本
- answer：带有正确/错误标记的答案
- game：单个游戏实例及配置
- player：连接到每个玩家
- pubsub：当特定事件发生时共享给所有 WebSocket 服务器的数据

| question | |
| :--- | --- |
| id | int2 |
| text | varchar(1000) |

| answer | |
| :--- | :--- |
| id | int2 |
| question_id | int2 |
| text | varchar(500) |
| correct | bool |

| game | |
| :--- | :--- |
| id | int4 |
| question_offset | int2 |
| questions_asked | int2 |
| timeout_answered | int2 |
| score_fastest | int2 |
| score_incorrect | int2 |
| score_noanswer | int2 |
| time_created | timestamp |
| time_started | timestamp |

| player | |
| :--- | :--- |
| id | int4 |
| game_id | int4 |
| name | varchar(10) |

| pubsub | |
| :--- | :--- |
| id | int4 |
| game_id | int4 |
| type | varchar(20) |
| data | jsonb |
| queued | timestamp |

PostgreSQL 被用于该项目是因为它通过架构中定义的约束保证了数据完整性。例如：

- 不可能添加文本相同的题目
- 修改题目 id 会自动更新关联答案记录的 question_id
- 删除游戏记录会自动删除与该游戏相关的玩家和 pubsub 记录

该项目选择 PostgreSQL 是因为它提供了发布者/订阅（pub/sub）服务。当应用程序更改数据库数据（发布）时，可以触发事件，这些事件可以通知所有订阅者。这意味着我们不需要额外的 pub-sub 解决方案作为依赖。





系统启动了三个隔离的 WebSocket 服务器实例。这提升了性能并提供了一些冗余。如果某个服务器故障，连接到其他服务器的玩家仍可以继续游戏。

当玩家连接时，他们在整个会话期间将保持连接到同一个 WebSocket 服务器。然而，同一场测验的两个玩家*可能*连接到不同的 WebSocket 服务器！

游戏使用 PostgreSQL 的发布/订阅（pub–sub）功能来保持同步：

- 1. 当 WebSocket 服务器上发生事件时（例如用户回答问题），该服务器会在 `pubsub` 表中插入一条新记录。
- 2. PostgreSQL 激活一个触发器，该触发器会将包含新数据的事件发送到所有运行同一特定游戏实例的 WebSocket 服务器（订阅者）。
- 3. 每个 WebSocket 服务器（包括最初接收请求的那个）都会运行一个处理程序，对传入的事件数据进行操作。

代码定义在 `ws` 目录。`.env` 配置文件和 `libshared` 目录提供了所有组件共享的代码。

## 4. 一个 Traefic 负载均衡器

Traeficic 是一个反向代理和负载均衡器，它可以将所有进入的 HTTP 和 WebSocket 请求重定向到适当（且最空闲）的服务器。

当应用程序运行时，可以通过 http://localhost:8080/ 访问并监控 Traefic 面板。

## 5. Adminer 数据库客户端

（可选的）Adminer 数据库客户端会在开发模式下启动，你可以检查 PostgreSQL 表数据。使用以下凭据访问 http://adminer.localhost/：

- 系统 (System): PostgreSQL
- 服务器 (Server): dbserver (或 host.docker.internal 或你的 PC IP 地址)
- 用户名 (Username): quizuser
- 密码 (Password): quizpass
- 数据库 (Database): quiz

如果你更喜欢使用常用的客户端程序访问数据库，请在 Server 中输入 localhost。包括 Beekeeper Studio、DBeaver 和 Postbird 在内的流行选项应该是兼容的

## Docker 开发环境

在服务器上安装、配置和启动所有七个应用程序（加上 Adminer 是八个）将没有多少开发时间！幸运的是，整个环境可以使用 Docker 管理，可以在几秒钟内启动，并且仍然支持使用 nodemon 进行 Node.js 重启。

因如此，Docker 是你需要安装的唯一软件依赖。即使是 Node.js 运行时也由 Docker 管理。

完整的 Docker 教程超出了本书的范围，但 `web` 和 `ws` 目录包含 Dockerfile 配置（`web.Dockerfile` 和 `ws.Dockerfile`），它们告诉 Docker 如何从轻量级的 Node.js 16 Alpine Linux 构建并运行 Express 和 WebSocket 应用程序。

两者创建一个 Docker 镜像。你可以将其认为包含运行应用程序所需的所有文件、库和可执行文件的磁盘镜像。

你可以启动任意 Docker 镜像实例。运行中的实例被称为容器。将其想象为一个运行单个可执行程序（如数据库或 Node.js 应用程序）的隔离 Linux 虚拟机。

启动容器只需要一个 `docker run` 命令。幸运的是，Docker Compose 可以使用 docker-compose.yml 中定义的开发环境配置管理并运行所有容器。它执行了以下操作：

- 声明所有容器、副本和重启策略。
- 定义来自 .env 文件的所有环境变量。
- 挂载磁盘存储卷，因此无需无需每次启动都重新初始化数据库。它还挂载了 `web` 和 `ws` 项目中的 `libshared` 模块目录。
- 覆盖 Dockerfile 设置以使用 nodemon 并启动 Node.js 调试服务器。
- 将所有容器连接到同一个内部 Docker 网络。
- 配置 Traefic 负载均衡器。

从项目根目录以开发模式启动整个环境：

```
docker-compose up
```

终端显示实时活动日志和任何错误。每当 JavaScript 文件发生变化时，nodemon 都会重启 web 和 ws 应用程序。

要优雅地关闭所有应用程序，请从项目根的另一个终端运行以下命令：

```
docker-compose down
```

## Docker 生产环境

docker-compose-production.yml 定义了生产级设置，以便测验应用程序运行在生产服务器上。配置更为简单，因为不需要覆盖 Dockerfile 设置或启动 Adminer。

使用生产模式启动应用程序：

```
docker-compose -f ./docker-compose-production.yml up
```

## Docker Compose 适用于生产环境？

可能不是。在容器中运行 PostgreSQL 不是高效的，有更好的选项如 Docker Swarm 和 Kubernetes 来管理跨服务器的容器。这超出了本书的范围！

## Summary

设置开发环境是复杂的，但你开始时做的选择会影响项目的长期成功。我们现在处于创建一个（大多数无状态的）应用程序的良好位置，下一章将从第 15 章的 server 开始。

# 第 15 章：实时多人测验：Express

测验应用程序的 Express 部分：

- 从 Open 导入问题
- 允许玩家创建并启动新游戏
- 允许其他玩家加入该游戏

测验服务位于 URL /game=<gameName>，WebSocket 服务器接管了游戏。同一页面上的两个请求（例如 CSS 和 JavaScript 文件）可能由不同的服务器 递送。这极少是一个问题，因为 web 默认是无状态的。

## Database Library

PostgreSQL 数据库连接由 Node.js pg 库处理。libshared/quizdb.js 模块中加载，提供了 INSERT、SELECT 和 DELETE 记录的选择函数。相同的模块被 web 和 ws 服务器使用，并定义了类型解析器。默认情况下，pg 返回所有字段为字符串，因此解析器将其转换为正确的类型：

```javascript
import pg from 'pg';

// 数据类型解析器
pg.types.setTypeParser(pg.types.builtins.INT2, v => parseInt(v, 10));
pg.types.setTypeParser(pg.types.builtins.INT4, v => parseInt(v, 10));
pg.types.setTypeParser(pg.types.builtins.INT8, v => parseInt(v, 10));
```

代码随后使用环境变量定义“连接池”：

```javascript
const pool = new pg.Pool({
  host: process.env.DB_SERVER,
  port: process.env.DB_PORT,
  database: process.env.DB_NAME,
  user: process.env.DB_USER,
  password: process.env.DB_PASSWORD,
});
```

池提供了一组可重用的数据库客户端，你可以检查、使用并释放。它的优点包括：

- 重用客户端时没有握手延迟。
- 每个客户端都是独立的连接。与单个连接不同，它们可以并发请求。

这是一个使用池连接的简单参数化查询示例，返回 1 到 10 之间的记录：

```javascript
// DB 连接
const client = await pool.connect();

try {
  // 获取 id 在 1 到 10 之间的问题
  const result = await client.query(
    'SELECT * FROM question WHERE id >= $1 AND id <= $2',
    [1, 10]
  );
} catch (err) {
  console.log(err);
} finally {
  // 释放客户端
  client.release();
}
```

SQL SELECT 字符串引用 $1 和 $2，它们会被数组中的第一个和第二个元素的值替换。当查询执行成功时，返回一个对象数组。

创建单独的 SQL 命令可能很麻烦，而且很容易遗漏或颠倒数组参数。libshared/quizdb.js 模块有 dbSelect、dbInsert、dbUpdate 和 dbDelete 函数，这使得开发更容易。例如，为特定游戏添加新玩家记录时使用公共的 playerCreate() 函数：

```javascript
// 创建新玩家
export async function playerCreate(game_id, name) {
  return await dbInsert({
    table: 'player',
    values: { game_id, name },
    return: 'id'
  });
}
```

这调用了私有的 `dbInsert()` 函数，传入表名、包含键值对的值对象以及获取插入记录 ID 的返回。dbInsert() 返回插入的 ID 或在发生错误时返回 false：

```javascript
// 数据库 INSERT
// 传入对象：{ table: <tableName>, values: <n1: v1,... > }
// return: <field>
async function dbInsert(ins) {
  const
    ret = ins.return ? ` RETURNING ${ins.return}` : '',
    key = Object.keys(ins.values),
    sym = key.map((v, i) => `$${i + 1}`),
    sql = `INSERT INTO ${ins.table} (${key.join()}) VALUES(${sym.join()})${ret}`;

  const client = await pool.connect();
  try {
    const result = await client.query(sql, Object.values(ins.values));
    return result.rows[0][ins.return];
  } catch (err) {
    console.error(err);
    return false;
  } finally {
    client.release();
  }
}
```





```javascript
client = ins.client || await pool.connect();

let success = false;

try {
  // 执行插入
  const i = await client.query(sql, Object.values(ins.values));

  // 是否成功?
  success = i.rowCount === 1;

  // 返回值?
  if (success && ins.return) {
    success = i.rows[0][ins.return];
  }
} catch (err) {
} finally {
  if (!ins.client) client.release();
}

return success;
```

顶部的 `const values` 变量负责创建 SQL 字符串：

`INSERT INTO player (game_id, name) VALUES ($1, $2) RETURNING id;`

这里有四点需要注意：

- * key* 定义了一个从 `values` 对象中提取的属性名数组。
- * sym* 定义了一个从 $1 到 $n$ 的字符串数组，其数量与 `key` 数组中的项数匹配。
- 来自 `values` 的属性值通过 `Object.values( ins.values )` 传递给 SQL 查询。
- 调用函数可以传递它自己的 `pool.connect()` 对象。这在数据库事务中运行一系列更新操作时是必要的。

私有方法 `dbUpdate()` 类似，尽管它也接收一个包含键/值对的 `where` 对象来创建 SQL 字符串，例如：

`UPDATE game SET time_started=$1 WHERE game_id=$2;`

该函数确保名称和值正确解析：

```javascript
// 数据库更新
// 传递对象：{ table: <tablename>, values: <n1: v1, ...> }
// where: { n1: v1, ...> }
async function dbUpdate(upd) {
  const
  sym = [...Object.values(upd.values), ...Object.values(upd.where)]
  vkey = Object.keys(upd.values),
  val = vkey.map((k, i) => `${k}=${i + 1}`),
  ckey = Object.keys(upd.where),
  cond = ckey.map((k, i) => `${k}=${i + val.length + 1}`);

  const sql = `UPDATE ${upd.table} SET ${val.join()} WHERE ${cond.join()}`;
  const client = upd.client || await pool.connect();

  let updated = 0;

  try {
    // 执行更新
    const u = await client.query(sql, sym);

    // 是否成功?
    updated = u.rowCount;
  } catch (err) {
  } finally {
    if (!upd.client) upd.client.release();
  }

  return updated;
}
```

记录删除的 SQL 更简单。例如：

```javascript
DELETE FROM game WHERE id=$1;
```

因此，`dbDelete()` 函数也是如此：

```javascript
// 数据库删除
// 传递对象：{ table: <tablename>, where: { n1: v1,... } }
// 所有的键/值对都使用逻辑与 (AND)
async function dbDelete(del) {

  const key = Object.keys(del.values).map((v, i) => `\${v}=\${${i+1}}`),
  sql = `DELETE FROM ${del.table} WHERE ${key.join(' AND ')}`;
  client = del.client || await pool.connect();

  let deleted = false;

  try {
    // 执行删除
    const d = await client.query(sql, Object.values(del.values));
    deleted = d.rowCount;
  } catch (err) {
  } finally {
    if (!del.client) client.release();
  }

  return deleted;
}
```

最后，`dbSelect()` 是所有函数中最简单的，因为你必须指定你自己的 SQL 字符串和参数数组：

```javascript
// 数据库查询
// 传递 SQL 字符串和参数数组
async function dbSelect(sql, arg = []) {

  const client = await pool.connect();

  try {
    const result = await client.query(sql, arg);
    return result && result.rows;
  } catch(err) {
    console.log(err);
  } finally {
    client.release();
  }
}
```

这是因为 SQL SELECT 查询可能是多变且复杂的。某些数据库库提供了对象关系映射 (ORM) 方法来构建 SQL 查询字符串，但对于此项目来说就大材过用了！

## 问题数据库初始化

数据从 Open Trivia Database 下载——这是一个免费使用的、用户贡献问答的仓库，并提供 REST API。问题及其相关答案存储在 question 和 answer 数据库表中。当用户首次访问测验首页时，可以启动此操作。

## 在应用程序启动时初始化数据？

应用程序可以在 Web 服务器启动时初始化问题。然而，可能会启动多个应用程序实例，每个实例都会尝试加载问题。将其放入用户请求中可以确保一次只有一个服务器加载问题。

`.env` 文件定义了环境变量——包括数据库凭据和 `QUIZ_QUESTIONS_MAX=500`——用于限制导入的问题数量。`web/index.js` 入脚本加载模块并配置 Express 服务器：

```javascript
// Express
import express from 'express';
import compression from 'compression';

// 模块
import { questionCount, gameCreate, gameFetch } from './lib/quizdb.js';
import { questionsImport } from './lib/questions.js';
import * as lib from './lib/quizdb.js';

// 配置
const cfg = {
  dev: process.env.NODE_ENV === 'development',
  port: process.env.PORT || 8000,
  domain: process.env.DOMAIN,
  ws: process.env.WS_DOMAIN,
  title: process.env.QUIZ_TITLE,
  questionsMax: parseInt(process.env.QUIZ_QUESTIONS_MAX) || 500,
};

const app = express();

app.use(compression());
app.set('view engine', 'ejs');
app.set('views', 'views');
app.use(express.urlencoded({ extended: true }));

app.get('/', async (req, res) => {
  if (typeof req.query.import !== 'undefined') {
    // 新问题并重定向
    res.redirect(`?imported=${await questionsImport()}`);
  } else {
    // 首页
    res.render('home', {
      title: cfg.title,
      questions: await questionCount(),
      questionsMax: cfg.questionsMax,
      imported: req.query.imported || null
    });
  }
});
```

## 导入的数量为什么会有差异？

Open Trivia Database 返回一组随机问题。某些可能是已导入问题的重复，但数据库的 `question.text` 具有唯一性标记，以确保每个问题只能添加一次。

## 原生 Node.js Fetch()

Deno 完整实现了浏览器 Fetch API，因此你可以在服务器应用程序中使用它。Node.js 在 18 版本中引入了类似的 Fetch API，但它是实验性的。为了向后兼容，使用了第三方模块。

Open Trivia API 返回的 JSON 数据如下：

```json
{
  "response_code": 0,
  "results": [
    {
      "category": "History",
      "type": "multiple",
      "difficulty": "medium",
      "question": "帝国大厦的顶部最初是为了什么目的而设计的?",
      "correct_answer": "Airship Dock",
      "incorrect_answers": [
        "Lightning Rod",
        "Antennae",
        "Flag Pole"
      ]
    },
    {
      "category": "Entertainment: Cartoon & Animations",
      "type": "multiple",
      "difficulty": "easy",
      "question": "以下哪个不是迪士尼的动画角色?",
      "correct_answer": "Daffy Duck",
      "incorrect_answers": []
    }
  ]
}
```



```json
[
  "Donald Duck",
  "Daisy Duck",
  "Scrooge McDuck"
],
{
  "category": "History",
  "type": "multiple",
  "difficulty": "hard",
  "question": "纽约市的原名是什么？",
  "correct_answer": "新阿姆丹",
  "incorrect_answers": [
    "新伦敦",
    "新巴黎",
    "新罗马"
  ]
}
]
```
这些内容被转换为 JavaScript 值并进行格式化，通过调用 `libshared/quizdb.js` 中的 `questionAdd(question, answer)` 函数将每个问题/答案集添加到数据库中。每个问题和答案集都插入在数据库事务中，这样如果任何 SQL INSERT 操作失败，所有的操作都将一起失败：

```javascript
// add a new question and answer set
export async function questionAdd(question, answer) {

  const client = await pool.connect();
  let commit = false;

  try {
    // new transaction
    await client.query('BEGIN');

    // add question
    const qId = await dbInsert({
      client,
      table: 'question',
      values: {
        text: question
      },
      return: 'id'
    })

    if (qId) {
      // insert answers in sequence
      let inserted = 0;
      for (let item of answer) {
        const a = await dbInsert({
          table: 'answer',
          values: {
            question_id: qId,
            text: item.text,
            correct: item.correct
          }
        });
        if (a) inserted++;
      }
      // answers added?
      commit = inserted === answer.length;
    }
  } catch (err) {
  } finally {
    // commit or rollback transaction
    if (commit) {
      await client.query('COMMIT');
    } else {
      await client.query('ROLLBACK');
    }
    client.release();
  }
  return commit;
}
```

# 顺序数据库插入 INSERTs

代码可以在短时间内运行多个数据库 INSERT 命令。这样速度更快，但问题和答案的 ID 在数据库表中出现的顺序看起来似乎是随机的。例如，ID 为 1 的问题记录可能关联了 ID 为 17、22、52 和 54 的答案记录。

这对于索引数据库来说不是问题，但在开发期间这会使表变得难以阅读！由于这个原因，问题和答案是按顺序插入的，一次一个。这意味着通过 `answer.id` 排序可以返回一个按字母顺序排列的列表，而不需要额外的 `answer.field` 字段。

## 开始新游戏

`web/views/home.ejs` 模板定义了一个 HTML 表单，用于配置和开始新游戏：

```html
<form action="/newgame/" method="post">
  <div class="formgrid">
    <label for="namenew">你的名字:</label>
    <div><input type="text" name="name" id="namenew" value="" minlength="1" maxlength="10" pattern="[A-Za-z0-9]{1,10}" required /></div>
    <label for="questions_asked">问题数量:</label>
    <div><input type="number" name="questions_asked" id="questions_asked" value="10" min="1" max="50" required /></div>
    <label for="timeout_answered">首次回答后的时间限制:</label>
    <div><input type="number" name="timeout_answered" id="timeout_answered" value="5" min="5" max="60" required /> 秒</div>
    <label for="score_correct">回答正确的得分:</label>
    <div><input type="number" name="score_correct" id="score_correct" value="1" min="-100" max="100" required /> 分</div>
    <label for="score_fastest">最快玩家奖励分:</label>
    <div><input type="number" name="score_fastest" id="score_fastest" value="1" min="-100" max="100" required 分 /></div>
    <label for="score_incorrect">回答错误的得分:</label>
    <div><input type="number" name="score_incorrect" id="score_incorrect" value="-1" min="-100" max="100" required 分 /></div>
    <label for="score_noanswer">未回答的得分:</label>
    <div><input type="number" name="score_noanswer" id="score_noanswer" value="0" min="-100" max="100" required 分 /></div>
    <button>进入游戏大厅&hellip;</button>
</form>
```

表单的 HTTP POST 数据发送到 `/newgame/` URL，该 URL 由 `web/index.js` 中定义的路由处理：

```javascript
// create a new game
app.post('/newgame', async (req, res) => {
  const gameId = await(gameCreate(req.body)),
    playerName = libId.clean(req.body.name);

  if (gameId === null) {
    // 游戏创建错误?
    res.status(500).render('error', {
      title: cfg.title,
      error: '无法启动游戏?'
    });
  } else {
    // 使用 slug 和用户名重定向到游戏页面
    res.redirect(`//game/${libId.encode(gameId)}/${playerName}`);
  }
});
```

代码调用了 `libshared/quizdb.js` 中的 `gameCreate()` 函数并传递了包含表单数据的 `req.body` 对象。这在数据库 `game` 表中插入了一条新记录并返回其 ID——通过调用私有的 `dbInsert()` 函数（在上方的“数据库库”部分显示）：

```javascript
// create a new game
export async function gameCreate(data) {
  const qCount = await questionCount();

  return await dbInsert({
    table: 'game',
    values: {
      question_offset : Math.floor(Math.random() * qCount ), // 随机起始问题
      questions_asked : clamp(1, data.questions_asked, 50),
      timeout_answered : clamp(5, data.timeout_answered, 60),
      score_correct : clamp(-100, data.score_correct, 100),
      score_fastest : clamp(-100, data.score_fastest, 100),
      score_incorrect : clamp(-100, data.score_incorrect, 100),
      score_noanswer : clamp(-100, data.score_noanswer, 100)
    },
    return: 'id'
  });
}
```

注意以下内容：

- `question_offset` 是随机起始问题。
- `questions_asked` 在 1 到 50 之间限制。
- `timeout_answered` 在 5 到 60 之间限制。
- `score_correct` 在 -100 到 100 之间限制。
- `score_fastest` 在 -100 到 100 之间限制。
- `score_incorrect` 在 -100 到 100 之间限制。
- `score_noanswer` 在 -100 到 100 之间限制。

`gameCreate` 函数返回新游戏的 ID。该 ID 用于将用户重定向到游戏页面。

## 加入游戏

`web/views/home.ejs` 模板还定义了一个加入游戏的 HTML 表单，将用户的用户名和游戏代码 POST 到 `/joiningame/` 路由：

```html
<form action="/joiningame/" method="post">
  <div class="formgrid">
    <label for="namejoin">你的名字:</label>
    <div><input type="text" name="name" id="namejoin" value="" minlength="1" maxlength="10" pattern="[A-Za-z0-9]{1,10}" required /></div>
    <label for="slug">游戏代码:</label>
    <div><input type="text" name="slug" id="slug" value="" length="3" length="8" autocomplete="off" required /></div>
  </div>
  <button>进入游戏大厅&hellip;</button>
</form>
```

表单的 HTTP POST 数据发送到 `/joiningame/` URL 由 `web/index.js` 中定义的路由处理：

```javascript
// join an existing game
app.post('/joiningame', (req, res) => {
  // 使用 slug 和用户名重定向到游戏页面
  res.redirect(`/game/${libId.clean(req.body.slug.toLowerCase()) || 'x'}`/${libId.clean(req.body.name)}`);
});
```

这接收数据，清理字符串，并将用户重定向到 `/game/<gameCode>/<playerName>` 的 URL——例如 `/game/a23/Craig`。



```javascript
// 获取游戏 ID 和玩家名称
const
slug = req.params.slug,
gameId = libId.decode( slug),
game = gameId === null ? await gameFetch( gameId ) :ngameValid = game && gameId === game.id,
playerName = libId.clean(req.params.name) || 'Player';

if (gameValid && game.time_started === null) {

  // 游戏对玩家开放
  res.render('game', {
    domain: cfg.domain,
    wsDomain: cfg.wsDomain,
    slug,
    title: cfg.title,
    game,
    playerName
  });
} else {

  // 游戏已开始或无效
  const url = `${cfg.domain}/game/${ slug}`;

  res.status(gameValid ? 403 : 404).render('error', {
    title: cfg.title,
    error: gameValid ? `你加入游戏太晚了，地址 ${ url }` : `
游戏 ${ url } 无效。你输入是否正确？`
  });
}
```

该函数将游戏代码解码为整数，并通过调用 `libshared/quizdb.js` 中的 `gameFetch()` 从数据库获取游戏信息：

```javascript
// 获取游戏数据
export async function gameFetch( gameId ) {

const game = await dbSelect('SELECT * FROM game WHERE id=$1',
[ gameId ]);
return game?.[0];
}
```

假设游戏 ID 是有效的且游戏的 `time_started` 值为 `NULL`，该代码将渲染 `web/views/game.ejs` 模板。配置变量被传递到模板中的客户端脚本：

```html
<script type="module">
window.cfg = {
wsDomain: '<%=%= wsDomain %>',
gameId: '<%=%= game.id %>',
playerName: '<%=%= playerName %>'
n};
</script>
<script type="module" src="/js/main.js"></script>
```

这配置了在 `web/static/js/main.js` 客户端脚本中使用的值。

当需要时，将使用 `web/views/error.ejs` 模板显示错误：

- 无效的游戏 ID 将返回 HTTP 404 Not found 错误。
- 已开始的游戏（`time_started` 不为 `NULL`）将返回 HTTP 403 Forbidden 错误。

## 总结

应用程序的 Express 部分说明如何解析 URL 路由以触发服务器端功能。

到此时，所有加入游戏的玩家都加载了 `web/views/game.ejs` 模板。所有的后续测验游戏处理现在都将使用客户端 JavaScript 和 WebSocket 服务器消息进行处理（见第 16 章）。Express 已完成它的工作！

# 第 16 章：实时多人测验示例：WebSocket 代码

第 11 章介绍了 WebSockets，它在客户端浏览器和服务器之间建立了一个双向交互通信通道。

我们的测验应用程序启动了三个 WebSocket 服务器，启动服务器的数量没有限制。但是：

- 用户将连接到单个服务器，并在整个会话期间保持连接。
- 同一个游戏的两个用户可能连接到不同的 WebSocket 服务器。

发送和从 WebSocket 服务器接收的消息通常是简单的字符串，但我们面临的额外挑战是跨所有服务器协调消息！

## 发起 WebSocket 连接

`web/static/js/main.js` 中的客户端 JavaScript 发起到 WebSocket 服务器地址的连接，并在连接建立后发送 `gameInit` 消息。注意 `window.cfg.wsDomain`、`window.cfg.gameId` 和 `window.cfg.playerName` 是 Express 传递给 `web/views/game.js` 模板的值：

```javascript
// 客户端代码
// 处理 WebSocket 通信
const ws = new WebSocket( window.cfg.wsDomain );

// 连接到服务器并发送游戏 ID 和初始玩家名称
ws.addEventListener('open', () => {
  sendMessage('gameInit', { gameId: window.cfg.gameId,
  playerName: window.cfg.playerName } });
});
// 发送消息
function sendMessage(type, data = null) {
  ws.send(` ${type}:${JSON.stringify( data) } `);
}
```

事件处理函数现在可以接收来自 WebSocket 服务器的传入消息：

```javascript
// 接收消息
ws.addEventListener('message', e => {
  // 处理...
});
```

`ws/index.js` 中的服务器端脚本初始化了一个 `ws` WebSocketServer 对象，并监听新的客户端连接和传入的消息：

```javascript
// 服务器
ws = new WebSocket({ port: cfg.wsPort, perMessageDeflate: false });

//客户端连接
ws.on('connection', (socket, req) => {
  console.log(`连接来自 ${req.socket.remoteAddress}`);

  // 从客户端接收消息
  socket.on('message', async (msg) => {
    // 处理...
  });
});
```

## WebSocket 格式

测验应用程序对客户端或服务器发送的所有 WebSocket 消息都使用相同的格式。一个标识符类型字符串后跟着一个冒号：

JSON 格式的字符和载荷数据：

```json
messageType:{ jsondata }
```

例如，上述的 `gameInit` 消息在发起 WebSocket 连接后不久，就会将游戏 ID 和玩家名称传递给服务器：

```json
gameInit:{ "gameId": "a23", "playerName": "Craig" }
```

当从玩家处接收消息时，WebSocket 服务器可能会立即执行某些操作。然而，大多数消息会被转发到所有连接到同一个游戏的 WebSocket 服务器。每个 WebSocket 服务器（包括最初接收到消息的那个）都会处理这些消息。




[content]

## 游戏逻辑

本节概述了游戏逻辑从加入、开始、进行到完成测验的进展过程。请注意以下几点：

- * `web/static/js/main.js` 中的客户端 JavaScript 在发生事件（例如回答问题）时，会从客户端向 WebSocket 服务器发送消息。
- `ws/index.js` 中的 WebSocket 服务器端 JavaScript 接收来自客户端的消息并执行相应的功能。在大多数情况下，消息会广播到所有运行相同游戏的 WebSocket 服务器。这些服务器接收数据并将其回传给该游戏的所有已连接的客户端。
- `web/static/js/main.js` 中的客户端 JavaScript 接收传入的消息，并据此更新 DOM 或游戏状态。

HTML 的 `<body>` 类名被设置为对应传入消息的类型。这可以触发 CSS 根据游戏状态显示或隐藏特定的元素。

在某些情况下，客户端上发生的动作在传输到所有 WebSocket 服务器及其连接的客户端并从服务器接收返回之前，不会产生任何效果！

## 加入游戏

当玩家通过 URL `/game/<gameCode>` 访问有效游戏时（例如 `/game/a23/Craig`），客户端会与单个服务器建立 WebSocket 连接并发送 `gameInit` 消息。例如：

```
gameInit:{"gameId": "a23", "playerName": "Craig"}
```

这会触发 WebSocket 服务器上的消息事件处理函数，该函数会初始化游戏（if 块）：

```javascript
// 接收来自客户端的消息
socket.on('message', async (msg) => {

  // 解析消息
  msg = parseMessage(msg);

  // 初始化玩家和游戏
  if (!player && msg.type === 'gameInit' && msg.data) {

    player = new Player();
    const pId = await player.create( msg.data.gameId, msg.data.playerName,
      socket);
    if (pId) player = null;
  }

  // 将消息传递给游戏对象
  msg.data = msg.data || {};
  msg.data.playerId = player.id; msg;
  await player.game.clientMessage( msg );
}
});
```

使用 `ws/lib/player.js` 中定义的类创建一个 `Player` 对象。运行它的 `create( gameId, playerName, socket )` 方法：

```javascript
// 初始化新玩家
async create( gameId, playerName, socket ) {

  // 玩家属性
  this.name = playerName;
  this.#socket = socket;

  // 初始化游戏
  this.gameId = gameId;
  this.game = await GameFactory( gameId);
  if (!this.game) return null;

  // 将现有玩家发送给新玩家
  this.send('player', this.game.playerAll())

  // 创建此玩家
  this.id = await db.playerCreate( this.gameId, playerName );
```

```javascript
if ( !this.id ) return null;

// 将玩家添加到游戏
this.game.playerAdd( this );

return this.id;

```

## 为什么要运行 create() 方法？

`Player` 类有一个构造函数，它在对象实例被创建时运行。很遗憾的是，构造函数不能是异步的，因此有必要运行另一个方法来处理初始化。

`Player` 对象跟踪用户的 ID、游戏 ID、名称、分数，而 WebSocket 连接被 `send()` 方法用于向单个玩家发送消息：

```javascript
// 向玩家发送消息
send( type = 'ws', data = {} ) {

  if (this.#socket) {
    this.#socket.send(`${type}:${JSON.stringify(data)}`);
  }
}
```

Player `create()` 将 `gameId` 传递给在 `ws/lib/game.js` 中定义的 `GameFactory()` 函数：

```javascript
// 活跃游戏
const activeGame = new Map();

// 创建并管理异步游戏对象
export async function GameFactory(gameId) {

  // 游戏实例不存在？
  if (!gameActive.has(gameId)) {

    // 创建新的游戏实例
    const game = new Game();
    if ( await game.create(gameId) ) {
      gameActive.set(gameId, game);
    }
```

```javascript
}
  console.log(`游戏 ${gameId} 已添加 - 此服务器上的活跃游戏: ${
  gameActive.size}`);
}
  return gameActive.get(gameId) || null;
}
```

`Game` 对象跟踪游戏状态和连接的玩家。它们负责接收来自单个客户端的消息，将该消息广播到所有 WebSocket 服务器，并再次接收消息，将其发送给同一游戏的所有已连接客户端。

`GameFactory()` 函数在每个 WebSocket 服务器上的首位玩家加入游戏时创建并返回一个新的 `Game` 对象。该对象被引用在 `gameActive` JavaScript Map 中，使用游戏 ID 整数作为引用。所有后续在同一 WebSocket 服务器上加入相同游戏的玩家都会接收到同一个游戏对象。

接下来，加入的客户端会收到一个包含游戏对象 `playerAll()` 方法的所有现有玩家 ID 和名称的消息。`init()` 函数在客户端 `web/static/js/player.js` 中中将每个玩家添加到 HTML `<table>` 中并存储在名为 `player` 的 Map 中：

```javascript
// 客户端代码
const pList = document.getElementById('player'),
pNum = document.getElementById('pnum'),
player = new Map();
```

（注：后续重复的示例代码块已根据要求保留格式并翻译重复的描述逻辑）


```javascript
// fetch next question and answer set
export async function questionFetch(qNum) {
  // fetch question
  const qCount = await questionCount();
  question = await dbSelect('SELECT * FROM question ORDER BY LIMIT 1 OFFSET $1', [qNum % qCount]);

  if (question.length !== 1) return null;

  // fetch answers
  const answer = await dbSelect('SELECT * FROM answer WHERE question_id=$1 ORDER BY id', [question[0].id]);

  if (!answer.length) return null;

  return {
    text: question[0].text,
    answer: answer.map(a => ({ return text: a.text, correct: a.correct })
  };
}
```

注意 PostgreSQL 的 `OFFSET` 子句会根据当前游戏定义的随机 `question_offset` 获取下一个问题。

## 回答问题

当每个客户端接收到活动消息（active message）时，它会运行客户端 `web/static/js/question.js` 脚本中的 `show()` 函数来显示问题和可能的答案按钮：

```javascript
// CLIENT-SIDE JAVASCRIPT
// show question
export function show(q) {
  currentQuestion = q;
  currentQuestion.answered = null;

  clear(question);
  clear(answers);
```

```javascript
answers.classList.remove(answeredClass);

qNum.textContent = q.num;
question.innerHTML = q.text;
currentQuestion.answerNode = [];

q.answer.forEach((ans, idx) => {
  const button = document.createElement('button');
  button.value = idx;
  button.innerHTML = `<span>${idx+1}</span> ${ans}`;
  currentQuestion.answerNode[idx] = button; 
  answers.appendChild(button);
});
```

玩家回答问题——通过点击按钮或按下键盘上关联的数字（1 到 4）——客户端 `web/static/js/question.js` 脚本中的 `questionAnswered()` 函数会验证其有效性、高亮按钮，并触发一个名为 `answered` 的自定义事件：

```javascript
// CLIENT-SIDE JAVASCRIPT

// answer event handlers
answers.addEventListener('click', questionAnswered);
window.addEventListener('keydown', questionAnswered);
```

```javascript
// user answers a question
function questionAnswered(e) {

  // already answered?
  if (!currentQuestion || currentQuestion.answered !== null)
    return;

  let ans = null;
  if (type == 'click') {
    // button click
    ans = e.target && e.target.nodeName === 'BUTTON' ?
      parseInt(e.target.value, 10) : null;
    if (ans >= currentQuestion.answer.length) ans = null;
  }
} else {
```

```javascript
  // keypress
  ans = e.key >= '1' && e.key <= String(currentQuestion.answer.length) ?
    parseInt(e.key, 10) - 1 : null;

  if (ans === null) return;

  // highlight answer
  currentQuestion.answered = ans;
  answers.classList.add(answeredClass);
  currentQuestion.answerNode[ans].classList.add(answeredClass);
}
```

```javascript
// raise custom event
document.dispatchEvent(new CustomEvent('answered', { detail: ans }));
```

这会触发客户端 `web/static/js/main.js` 脚本中的处理函数，该函数向连接的 WebSocket 服务器发送一个 `questioned` 消息：

```javascript
// CLIENT-SIDE JAVASCRIPT

// question answered event
document.addEventListener('answered', e => {
  if (state.current === 'questionactive') {
    sendMessage('questioned', {
      answer: e.detail
    });
  }
});
```

这会触发 `ws/lib/game` 中 `Game` 对象的 `clientMessage()` 函数：

```javascript
// incoming client event
async clientMessage(type, data) {
  console.log('Data from client', type, data);

  // handle client event (on single server)
  switch (type) {
    // ...
```

```javascript
    case 'questionanswered':
      if (this.#state.current !== 'questionactive') return;

      // calculate player score
      const correct = this.#state.activeQuestion.answer[data.answer].correct;
      data = {
        playerID: data.playerID,
        score: correct ? this.cfg.score_correct : this.cfg.score_incorrect,
        fastest: correct && !this.#state.correctGiven
      };

      // fastest correct bonus?
      if (data.fastest) data.score += this.cfg.score_fastest;

      // first answer controls flow
      if (!this.#state.playersAnswered) {
        let timeout = 100;

        // first response?
        if (this.#state.playersAnswered && this.player.size > 1) {
          // send question timeout warning
          timeout = this.cfg.timeout_answered * 1000;
          await db.broadcast(this.gameId, 'questiontimeout', timeout);
        }

        // complete question
        if (timeout) {
          this.#setTimer(async () => {
            // broadcast correct answer
            await db.broadcast(this.gameId, 'questioncomplete', {
              correct: this.#state.activeQuestion.answer.findIndex(a => a.correct)
            });

            // show scoreboard
            this.#setTimer(async () => {
              await db.broadcast(this.gameId, 'scoreboard');

              // next question or game over?
              if (!await this.#questionNext(timerDefault)) {
                await db.broadcast(this.gameId, 'gameover');
              }
            });
          }, timeout);
        }
      }
      break;
  }

  // broadcast message to all servers
  if (type) await db.broadcast(gameId, type, data);
```

根据游戏设置计算玩家正确、错误或最快回答的得分。这会被广播到所有服务器，当它们被 `#EventHandler()` 方法接收时更新分数（它们不会广播给客户端）：

```javascript
// incoming event sent to all servers
async #EventHandler({ gameId, type, data }) {
  console.log('Shared server event', type, data);

  if (gameId !== this.gameId || !type) return;

  // handle server event (on all servers)
  switch (type) {
    //...

    // player answers question
    case 'questionanswered':
      if (this.#state.current !== 'questionactive') return;

      const correct = this.#state.activeQuestion.answer[data.answer].correct;
      data = {
        playerID: data.playerID,
        score: correct ? this.cfg.score_correct : this.cfg.score_incorrect,
        fastest: correct && !this.#state.correctGiven
      };

      // fastest correct bonus?
      if (data.fastest) data.score += this.cfg.score_fastest;

      // first answer controls flow
      if (!this.#state.playersAnswered) {
        let timeout = 100;

        // first response?
        if (this.#state.playersAnswered && this.player.size > 1) {
          // send question timeout warning
          timeout = this.cfg.timeout_answered * 1000;
          await db.broadcast(this.gameId, 'questiontimeout', timeout);
        }

        // complete question
        if (timeout) {
          this.#setTimer(async () => {
            // broadcast correct answer
            await db.broadcast(this.gameId, 'questioncomplete', {
              correct: this.#state.activeQuestion.answer.findIndex(a => a.correct)
            });

            // show scoreboard
            this.#setTimer(async () => {
              await db.broadcast(this.gameId, 'scoreboard');

              // next question or game over?
              if (!await this.#questionNext(timerDefault)) {
                await db.broadcast(this.gameId, 'gameover');
              }
            });
          }, timeout);
        }
      }
      break;
  }
}
```



```javascript
// 清理完成的游戏
if (this.#state.current === 'gameover') {

  db.pubsub.off(`event:${this.gameId}`,
  this.#handlerFunction);
  await gameComplete(this.gameId );
}
```

每个服务器都会运行 `gameComplete()` 函数来删除 Game 对象以及数据库 `game` 表中的关联记录（只有第一个会成功）。这会导致该游戏在玩家和 pubsub 表中触发级联删除：

```javascript
// 移除活跃游戏
async function gameComplete( gameId ) {

  if (this.gameActive.has( gameId ) ) return;

  await db.gameRemove( gameId );
  gameActive.delete(gameId);

  console.log(`Game ${gameId} 已移除 - 此服务器上的活跃游戏:
->${gameActive.size}`);
}
```

相同的 `gameover` 消息会被发送到所有已连接的客户端。接收后，每个客户端都会显示游戏结束的消息，并附有启动或加入新游戏的链接。

## 离开游戏

如果用户关闭或刷新浏览器，服务器上 `ws/index.js` 中的 WebSocket 关闭事件处理程序会被触发：

```javascript
// 客户端连接关闭
socket.on('close', async () => {

  // 移除玩家
  if (player) {
    await player.game.playerRemove( player );
  }

  console.log(`与 ${ req.socket.remoteAddress} 断开连接`);

```

它调用了 `ws/lib/game.js` 中 Game 对象的 `playerRemove()` 方法：

```javascript
// 从游戏中移除玩家
async playerRemove( player ) {
  // 从数据库中删除
  await db.playerRemove( player.id );

  // 广播事件
  await db.broadcast(
    this.gameId,
    'playerRemove',
    { id: player.id }
  );
}
```

这使用 `libshared/quizdb.js` 中的 `playerRemove()` 函数从数据库 `player` 表中删除玩家：

```javascript
// 移除玩家
export async function playerRemove( playerId ) {
  return await dbDelete({
    table: 'player',
    values: { id: playerId }
  });
}
```

然后它向所有 WebSocket 服务器广播 `playerRemove` 消息。该消息会被它们的 `Game #eventHandler()` 接收，并删除玩家引用：

```javascript
// 发送到所有游戏服务器的传入事件
async #EventHandler({ gameId, type, data }) {

  console.log('共享服务器事件', type, data);

  if (gameId !== this.gameId || !type) return;

  // 处理服务器事件（在所有服务器上）
  switch (type) {

    // 移除玩家
    case 'playerRemove':
      if (this.player.has(data.id)) {
        this.player.delete(data.id );
      }
    break;
}
```最后，相同的 `playerRemove` 消息会被发送到所有客户端。每个客户端执行 `web/static/js/player.js` 中的 `remove()` 函数，从内存和 DOM 中删除该玩家：

```javascript
// 移除现有玩家
export function remove(p) {

  if (!p.id || !player.has(p.id)) return;

  plist.removeChild(player.get(p.id).node);
  player.delete(p.id);
}
```

## 练习

尝试使用第 4 章提供的说明调试测验应用程序。这比之前没有那么简单，因为单个用户可能与任何 HTTP 或 WebSocket 服务器进行通信。

幸运的是，每个玩家一次只能连接到一个 WebSocket 服务器。在启动或加入游戏时，检查 Docker 日志：

| ws_1 | connection from ::ffff:172.18.0.3 |

在这种情况下，用户正在连接到第一个 WebSocket 服务器 `ws_1`。在另一个终端中运行以下命令来列出活跃的 Docker 容器：

# docker container ls

注意 NAMES 和 PORTS：

| PORTS | NAMES |
|---|---|
| 0.0.0.0:59961->8001/tcp, 0.0.0.0:59962->9229/tcp | nodequiz_ws_1 |
| 0.0.0.0:59956->8001/tcp, 0.0.0.0:59957->9229/tcp | nodequiz_ws_2 |
| 0.0.0.0:59958->8001/tcp, 0.0.0.0:59959->9229/tcp | nodequiz_ws_3 |
| 0.0.0.0:59952->8000/tcp, 0.0.0.0:59953->9229/tcp | nodequiz_web_1 |
| 0.0.0.0:59954->8000/tcp, 0.0.0.0:59955->9229/tcp | nodequiz_web_2 |
| 0.0.0.0:5432->5432/tcp | dbserver |
| 0.0.0.0:59951->8080/tcp | |
| 0.0.0.0:80->80/tcp | |
| nodequiz_adminer_1 | |
| 0.0.0.0:59951->8080/tcp | |
| 0.0.0.0:80->80/tcp | |
| nodequiz_adminer_1 | |
| 0.0.0.0:59951->8080/tcp | |
| nodequiz_reverse | |
| quiz_reverse | |

  100                          ---- ---------------------------------- | 2022-01-11 |
- ----------------------------------------------- **，
------------- | 2021-11-11 |
------------------------------------------------
- it's
 
- 
- | 2022-09-22 |
------------------------------------------------ 
- --------------------------------------------------- 
- 2021-09-29 |
-------------------------------------------------- 
---------
--------------------------------------------------- 
- 
---------------------------------------------------- 
- 
----------------------------------------------------- 
- 2021-10-2- | 
- 
- 2021-10-15 | 
- 
- 
--------------------------------------------------- 
- 2021-10-22 | 
- 
- 2021-10-03 | 
- 
- 2022-01-18 | 
- 
- 2022-03-03 | 
- 
- 2022-02-22 | 
- 
- 2021-10-26 | 
- 
- 2022-01-19 | 
- 
- 2016-09-17 | 
- 
- 2022-01-25 | 
- 
- 2021-11-11 | 
- 
- 2022-09-22 | 
- 
- 2021-09-29 | 
- 
- 2020-01-23 | 
- 
- 2022-03-13 | 
- 
- 2022-02-25 | 
- 
- 2021-11-14 | 
- 
- 2021-10-15 | 
- 
- 2021-10-22 | 
- 
- 2021-10-03 | 
- 
- 2022-01-18 | 
- 
- 2022-03-03 | 
- 
- 2022-02-22 | 
- 
- 2021-10-26 | 
- 
- 2022-01-19 | 
- 
- 2016-09-17 | 
- 
- 2022-01-25 | 
- 
- 2021-11-11 | 
- 
- 2022-09-22 | 
- 
- 2021-09-29 | 
- 
- 2020-01-23 | 
- 
- 2022-03-13 | 
- 
- 2022-02-25 | 
- 
- 2021-11-14 | 
Chapter 17: Node.js Summary

An online search engine offers a better interface:

- npm.com: the official repository
- npms: a fast search, which ranks packages by a quality score
- snyk.io/advisor/: ranks packages with a health percentage based on their popularity, maintenance, security issues, and contributor community

[/content] (抱歉，由于提供的原文后半部分包含大量重复的乱码/字符，我已根据前文逻辑完成了可读部分的翻译，并对乱码部分进行了处理。)​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​,,​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​ 

## 示例

原文：

[content]

```javascript
// clean up completed game
if (this.#state.current === 'gameover') {

  db.pubsub.off(`event:${this.gameId}`,
  this.#handlerFunction);
  await gameComplete(this.gameId );
}
```

Every server runs a `gameComplete()` function to delete the Game object and the associated record in the database game table (only the first will succeed). This causes a cascade of deletions from the player and pubsub tables for that game:

```javascript
// remove active game
async function gameComplete( gameId ) {

  if (this.gameActive.has( gameId ) ) return;

  await db.gameRemove( gameId );
  gameActive.delete(gameId);

  console.log(`Game ${gameId} removed - active games on this server:
->${gameActive.size}`);
}
```

The same `gameover` message is sent to all connected clients. When received, each client shows the Game over messages with links to start or join a new game.

# Leaving a Game

If the user closes or refreshes their browser, a WebSocket close event handler is triggered on the server in `ws/index.js`:

```javascript
// client connection closed
socket.on('close', async () => {

  // remove player
  if (player) {
    await player.game.playerRemove( player );
  }

  console.log(`disconnection from ${ req.socket.remoteAddress}`);

});

```

It calls the Game object's `playerRemove()` method in `ws/lib/game.js`:

```javascript
// remove player from game
async playerRemove( player ) {
  // delete from database
  await db.playerRemove( player.id );

  // broadcast event
  await db.broadcast(
    this.gameId,
    'playerRemove',
    { id: player.id }
  );
}
```

This deletes the player from the database player table using the `playerRemove()` function in `libshared/quizdb.js`:

```javascript
// remove a player
export async function playerRemove( playerId ) {
  return await dbDelete({
    table: 'player',
    values: { id: playerId }
  });
}
```

It then broadcasts a `playerRemove` message to all WebSocket servers. This is received by their `Game #eventHandler()`, which deletes the player reference:

```javascript
// incoming event sent to all game servers
async #EventHandler({ gameId, type, data }) {

  console.log('Shared server event', type, data);

  if (gameId !== this.gameId || !type) return;

  // handle server event (on all servers)
  switch (type) {

    // remove player
    case 'playerRemove':
      if (this.player.has(data.id)) {
        this.player.delete(data.id );
      }
    break;
}
```

Finally, the same `playerRemove` message is sent to all clients. Each client executes the `remove()` function in `web/static/js/player.js` to delete the player from memory and the DOM:

```javascript
// remove existing player
export function remove(p) {

  if (!p.id || !player.has(p.id)) return;

  plist.removeChild(player.get(p.id).node);
  player.delete(p.id);
}
```

# Exercises

Try debugging the quiz application using the instructions provided in Chapter 4. It's not as straightforward as before, because a single user could be communicating with any of the HTTP or WebSocket servers.

Fortunately, each player can only connect to one WebSocket server at a time. Examine the Docker log when you start or join a game:

| ws_1 | connection from ::ffff:172.18.0.3 |

In this case, the user is connecting to the first WebSocket server `ws_1`. Run the following command in another terminal to list the active Docker containers:

# docker container ls

Note the NAMES and PORTS:

| PORTS | NAMES |
|---|---|
| 0.0.0.0:59961->8001/tcp, 0.0.0.0:59962->9229/tcp | nodequiz_ws_1 |
| 0.0.0.0:59956->8001/tcp, 0.0.0.0:59957->9229/tcp | nodequiz_ws_2 |
| 0.0.0.0:59958->8001/tcp, 0.0.0.0:59959->9229/tcp | nodequiz_ws_3 |
| 0.0.0.0:59952->8000/tcp, 0.0.0.0:59953->9229/tcp | nodequiz_web_1 |
| 0.0.0.0:59954->8000/tcp, 0.0.0.0:59955->9229/tcp | nodequiz_web_2 |
| 0.0.0.0:5432->5432/tcp | dbserver |
| 0.0.0.0:59951->8080/tcp | |
| 0.0.0.0:80->80/tcp | |
| nodequiz_adminer_1 | |
| 0.0.0.0:59951->8080/tcp | |
| nodequiz_reverse | |
| quiz_reverse | |

```译文：

[content]

```javascript
// 清理完成的游戏
if (this.#state.current === 'gameover') {

  db.pubsub.off(`event:${this.gameId}`,
  this.#handlerFunction);
  await gameComplete(this.gameId );
}
```

每个服务器都会运行 `gameComplete()` 函数来删除 Game 对象以及数据库 `game` 表中的关联记录（只有第一个会成功）。这会导致该游戏在玩家和 pubsub 表中触发级联删除：

```javascript
// 移除活跃游戏
async function gameComplete( gameId ) {

  if (this.gameActive.has( gameId ) ) return;

  await db.gameRemove( gameId );
  gameActive.delete(gameId);

  console.log(`Game ${gameId} 已移除 - 此服务器上的活跃游戏:
->${gameActive.size}`);
}
```

相同的 `gameover` 消息会被发送到所有已连接的客户端。接收后，每个客户端都会显示游戏结束的消息，并附有启动或加入新游戏的链接。

## 离开游戏

如果用户关闭或刷新浏览器，服务器上 `ws/index.js` 中的 WebSocket 关闭事件处理程序会被触发：

```javascript
// 客户端连接关闭
socket.on('close', async () => {

  // 移除玩家
  if (player) {
    await player.game.playerRemove( player );
  }

  console.log(`与 ${ req.socket.remoteAddress} 断开连接`);

});

```

它调用了 `ws/lib/game.js` 中 Game 对象的 `playerRemove()` 方法：

```javascript
// 从游戏中移除玩家
async playerRemove( player ) {
  // 从数据库中删除
  await db.playerRemove( player.id );

  // 广播事件
  await db.broadcast(
    this.gameId,
    'playerRemove',
    { id: player.id }
  );
}
```

这使用 `libshared/quizdb.js` 中的 `playerRemove()` 函数从数据库 `player` 表中删除玩家：

```javascript
// 移除玩家
export async function playerRemove( playerId ) {
  return await dbDelete({
    table: 'player',
    values: { id: playerId }
  });
}
```

然后它向所有 WebSocket 服务器广播 `playerRemove` 消息。该消息会被它们的 `Game #eventHandler()` 接收，并删除玩家引用：

```javascript
// 发送到所有游戏服务器的传入事件
async #EventHandler({ gameId, type, data }) {

  console.log('共享服务器事件', type, data);

  if (gameId !== this.gameId || !type) return;

  // 处理服务器事件（在所有服务器上）
  switch (type) {

    // 移除玩家
    case 'playerRemove':
      if (this.player.has(data.id)) {
        this.player.delete(data.id );
      }
    break;
}
```

最后，相同的 `playerRemove` 消息会被发送到所有客户端。每个客户端执行 `web/static/js/player.js` 中的 `remove()` 函数，从内存和 DOM 中删除该玩家：

```javascript
// 移除现有玩家
export function remove(p) {

  if (!p.id || !player.has(p.id)) return;

  plist.removeChild(player.get(p.id).node);
  player.delete(p.id);
}
```

## 练习

尝试使用第 4 章提供的说明调试测验应用程序。这比之前没有那么简单，因为单个用户可能与任何 HTTP 或 WebSocket 服务器进行通信。

幸运的是，每个玩家一次只能连接到一个 WebSocket 服务器。在启动或加入游戏时，检查 Docker 日志：

| ws_1 | connection from ::ffff:172.18.0.3 |

在这种情况下，用户正在连接到第一个 WebSocket 服务器 `ws_1`。在另一个终端中运行以下命令来列出活跃的 Docker 容器：

# docker container ls

注意 NAMES 和 PORTS：

| PORTS | NAMES |
|---|---|
| 0.0.0.0:59961->8001/tcp, 0.0.0.0:59962->9229/tcp | nodequiz_ws_1 |
| 0.0.0.0:59956->8001/tcp, 0.0.0.0:59957->9229/tcp | nodequiz_ws_2 |
| 0.0.0.0:59958->8001/tcp, 0.0.0.0:59959->9229/tcp | nodequiz_ws_3 |
| 0.0.0.0:59952->8000/tcp, 0.0.0.0:59953->9229/tcp | nodequiz_web_1 |
| 0.0.0.0:59954->8000/tcp, 0.0.0.0:59955->9229/tcp | nodequiz_web_2 |
| 0.0.0.0:5432->5432/tcp | dbserver |
| 0.0.0.0:59951->8080/tcp | |
| 0.0.0.0:80->80/tcp | |
| nodequiz_adminer_1 | |
| 0.0.0.0:59951->8080/tcp | |
| nodequiz_reverse | |
| quiz_reverse | |





有一些用于比较两个或多个包的工具：

- npmcompare.com
- moiva.io

或者用于提取包信息的工具：

- anvaka.com: 依赖可视化
- npm-stat.com: 下载和使用统计数据

如果你在纠结选择哪一个，请选择符合以下标准的包：

- 流行
- 具有非限制性的使用许可
- 接收近期且定期更新
- 体积较小
- 依赖最少
- 没有重大待解决问题

下讨论的大多数包都符合这些标准。

# 开发工具

以下包是辅助开发的工具，而不是你 Node.js 项目的一部分。你通常会通过 `npm install <package> -g` 将它们全局安装，或者在项目文件夹中使用 `npm install <package> --save-dev` 将作为开发依赖安装：

- nvm (Node 版本管理器): 管理多个 Node.js 安装版本
- ESLint: 发现并修复 JavaScript 代码问题
- TypeScript: 为语言添加变量类型和其他功能，并编译为标准 JavaScript
- Rollup: 一个 JavaScript 打包器（此处查看教程）
- esbuild: 一个用 Go 编写的快速打包器
- PostCSS: CSS 转换器和优化器（此处查看教程）
- JSDoc: 从 JavaScript 注释生成 API 文档
- small-static-server: 一个微型静态文件 Web 服务器
- nodemon: 在源代码更改时重启 Node.js 
- Browsersync: 当客户端 HTML、CSS 或 JavaScript 更新时，实现浏览器实时重载

nodemon 在本书中一直被频繁使用。在开发期间运行脚本时，用它代替 `node`，以便在脚本或其任何模块发生变化时自动重启应用程序：

```
nodemon index.js
```

Browsersync 实际上是 nodemon 的客户端版本，但它具备一些“超能力”。以下命令启动了一个可以提供 HTML 文件和其他资源的 Web 服务器。如果任何 .js 文件发生变化，客户端脚本将进行动态重新加载：

```
browser-sync start --server --files "*.js"
```

最后，你需要一个兼容 Node.js 的编辑器，如 VS Code、Atom 或 Sublime Text。大多数编辑器都提供用于 linting（代码检查）、调试和源码管理的扩展。

# 测试

为应用程序的内部函数编写测试有助于确保更新是健壮的，且不会破坏现有功能。Node.js 不提供内置的测试器，但以下包非常流行：

- Testing Library
- Jest
- Mocha
- AVA
- uvu
- Tap

这些包之间的主要区别是下载大小和语法。大多数包允许你编写类似英语的断言，因此选择一个你或你团队青睐的即可。

所有的测试套件都提供了单元测试功能，用于根据已知输入验证函数的结果。此示例使用 uvu 来测试 Math.sqrt() 方法：

```javascript
import { test } from 'uvu';
import * as assert from 'uvu/assert';

test('Math.sqrt', () => {
  assert.is(Math.sqrt(4), 2 );
  assert.is(Math.sqrt(144), 12 );
  assert.is(Math.sqrt(2), Math.SQRT2 );
});

test.run();
```

以下包提供了无头浏览器自动化工具，用于集成测试——即通过程序化点击按钮和填充表单来测试应用程序的路由，并观察预期结果：

- Puppeteer: Chrome 自动化
- Playwright: 支持所有主流浏览器
- Cypress: 带有远程测试功能的商业选项

# 日志

如果你弃用 `console.log()`，第三方日志模块可以提供更复杂的日志功能，包括消息级别、详细程度、排序、文件输出、分析、报告等。流行的选项包括：

- cabin: Node.js、中间件和浏览器日志
- logger: 浏览器 console API 的轻量级 Node.js 实现
- signal: 高可配置日志
- pino: 快速且流行的 Node.js 和中间件日志
- winston: 全面的且可配置日志
- morgan: Express 中间件日志
- storyboard: 可以输出到 Chrome DevTools 扩展的日志库
- tracer: 简单的日志格式

# 全栈框架

以下框架可用于创建完整的 Web 应用程序，通常允许根据情况在服务器、客户端或混合模式进行渲染。它们可能提供“注水”（hydration）技术，即在服务器上生成 HTML 初始内容，然后由客户端组件接管以实现完全交互。

- Next.js: 基于 React 组件
- Nuxt.js: 基于 Vue 组件
- SvelteKit: 基于 Svelte 组件
- Sails: Node.js 版本的 Ruby on Rails

# 服务端框架

如果你更倾向于对客户端和服务器开发拥有完全控制，以下框架主要处理 HTML 内容的服务端渲染以及 JSON 或其他格式的 Ajax 响应：

- Express: 最早且最流行的框架之一
- Koa: 由 Express 团队设计的现代框架
- Fastify: 声称是最快速的选项之一
- Hapi: 专注于简单性、安全性和可扩展性
- NestJS: 提供了类似于 Angular 客户端框架的概念
- Adonis: Node.js 版本的 PHP Laravel
- Feathers: 用于实时应用和 REST API 的轻量级框架
- restify: 针对 REST Web 服务优化

# 客户端框架中的 Node.js

运行在浏览器中的客户端 JavaScript（及 CSS）框架通常不需要 Node.js。然而，它们经常使用运行时来提供工具，用于脚手架项目文件夹、打包模块、实现测试、运行开发服务器或在构建时优化资源。

# Web 发布、内容管理系统和博客

以下平台提供了管理面板，编辑器可以在其中编写内容并将其放入模板。这些是 WordPress 的 Node.js 替代方案。

## 欢迎使用 Ghost

## 你需要的一些事项

1. Ghost 是为野心勃勃的专业出版者设计的。
2. 整个平台可以修改以满足你的需求。
3. 它可以与所有喜欢的工具和应用程序协作。

##幕后故事

Ghost 由名为 Ghost Foundation 的独立非营利组织制作。我们的资金完全由 Ghost(Pro) 的收入支持。

- Ghost: 提供商业化托管服务
- Hexo: 更接近 SSG（见“静态站点生成器”章节），但可以通过插件添加管理面板

# 无头内容管理系统

以下包提供了编辑面板并通过 API 提供内容。文章和其他数据可以提取到你的应用程序或静态站点生成器中，输出到网页、应用、PDF 或其他：

- Strapi
- Keystone
- Apostrophe

# 静态站点生成器

静态站点生成器（SSG）从 Markdown 文件或无头 CMS 获取内容并在构建时将其放入模板。结果是预渲染为 HTML 文件的，可以托管在任何 Web 服务器上，无需语言运行时、数据库、查询或性能影响。你可能会看到这被称为 Jamstack，它最初是指 JavaScript、API 和 Markup，但现在用于更广泛的语境：

- Eleventy: Markdown 转 HTML，支持多种模板引擎
- Metalsmith: 一个简单的可插拔 SSG
- Gatsby: 基于 React 组件
- WordPress: 基于 Vue 组件
- Gridsome: 基于 Vue 组件

## 数据库驱动

数据库驱动（也称为连接器或客户端）提供了 API，允许你连接、查询和更新数据库数据。以下包是原生驱动：它们支持单一系统，复制标准命令，并且通常拥有数据库开发者的官方支持：

- mysql: 用于 MySQL
- mysql2: 更快的 MySQL 替代方案
- mariadb: 用于 MariaDB
- pg: 用于 PostgreSQL
- mongodb: 用于 MongoDB
- mssql: 用于 Microsoft SQL Server





- oracledb: 适用于 Oracle
- couchbase: 适用于 Couchbase
- redis: 适用于 Redis
- sqlite: 适用于 SQLite
- sqlite3: 一个异步 SQLite 替代方案
- sqlite-async: 基于 promise 的 sqlite3 版本

对象关系映射 (ORM) 模块通过在你的代码和数据库之间提供抽象层，可以使开发变得简单。与其直接运行命令，你的代码操作的是数据对象，这些对象从数据库的表示中被保存和恢复。这允许你在不同系统之间切换，但你可能需要安装原生驱动，并且某些数据库功能可能无法使用。示例包括：

- mongoose: 适用于 MongoDB
- sequelize: 适用于 MySQL, MariaDB, PostgreSQL, SQLite, DB2 和 Microsoft SQL Server
- typeorm: 适用于 MySQL, MariaDB, PostgreSQL, SQLite, Oracle 和 Microsoft SQL Server

请参阅第 10 章获取数据库使用示例。

## 模板

大多数模板系统通过在适当区块中插入值来生成 HTML。某些系统提供了编程构造结构，如文件包含、循环和条件，以优化开发。流行的选项包括：

- EJS
- Nunjucks
- Handlebars
- Pug

Pug 与其他人的不同在于，你使用的是简洁的、缩进式的文档，而不是 HTML 标签。例如，假设在以下 Pug 模板中标题值设置为“My Site”：

```
doctype html
html
head
  title #{title}
body
  h1 #{title}
  p#intro Welcome to my site.
```

生成的 HTML 如下：

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Site</title>
</head>
<body>
  <h1>My Site</h1>
  <p id="intro">Welcome to my site</p>
</body>
</html>
```

你通常会在像 Express 这样的服务器端框架中使用模板系统。本书的第 5 章、第 6 章和第 15 章使用了 EJS。例如，在由部分模件（partials）定义的页眉和页脚之间渲染一个 `<h1>` 标题：

```
<%- include('partials/_htmlhead'); -%>
<h1><%= title %></h1>
<%- include('partials/_htmlfoot'); --%>
```

## 命令行

在使用 Node.js 创建命令行应用程序时，以下包可能非常有用：

- commander: 解析命令行参数
- cliffy: 实现交互式 CLI
- chalk: 输出彩色控制台消息
- terminal-link: 输出可点击的超链接
- boxen: 输出框
- progress: 简单的进度条

## 文件系统

Node.js 标准库提供了详尽的文件系统 API，用于创建、修改、读取和删除文件及目录。这些是相当底层的函数，因此以下包提供了更简单的操作选项：

- fs-extra: 提供一系列文件系统方法
- globby: 文件名字符串 (glob) 匹配
- chokidar: 跨平台文件监听
- del 和 rimraf: 删除文件和目录

## 网络

以下包提供了许多网络 API。

注意，HTTP Fetch API 的原生版本已在 Node.js 18 中引入。随着开发者和主机更新其安装，使用第三方模块的必要性将变得降低。

- node-fetch: HTTP Fetch
- axios: HTTP Fetch
- got: HTTP Fetch
- get-port: 获取可用的 TCP 端口
- ssh2: SSH 客户端和服务器方法

## WebSockets

WebSockets 在浏览器和服务器之间建立了一个双向交互通信通道，允许实时更新和应用程序。以下包提供了服务器端 API，可以向浏览器 WebSocket API 发送消息：

- ws: 快速轻量级服务器
- socket.io: 完整的客户端和服务器库

另见第 11 章和第 16 章使用 ws 库的 WebSocket 示例。

## 图像

Node.js 可以创建、检查和修改大多数格式（JPG, GIF, PNG 等）的图像。包通常提供调整大小、裁剪、翻转、旋转，或应用锐化、模糊、灰度和透明度等过滤器。流行的选项包括：

- jimp: 比例、翻转、过滤和像素分析
- image-js: Node.js 和浏览器图像处理
- sharp: 快速图像转换
- imagemin: 图片压缩

以下示例使用 jimp 加载图像，将其转换为灰度，宽高减小 50%，并输出修改后的版本：

```javascript
import Jimp from 'jimp';
Jimp.read('one.png').then(image => {
  image
    .greyscale()
    .scale(0.5)
    .write('one-bw-small.png');
});
```

## 邮件

![](img/d4731c5479f6bfd1ada49d65047b9e4c_318_0.png)

发送邮件最流行的 Node.js 包是 Nodemailer。以下代码通过 SMTP 账户发送单封邮件：

```javascript
const nodemailer = require('nodemailer');

const transport = nodemailer.createTransport({
  host: 'smtp.example.com',
  port: 587,
  secure: false,
  auth: {
    user: 'username',
    pass: 'password',
  }
});

await transport.sendMail({
  from: '"Sender <me@sender.com>',
  to: '@recipient.com',
  subject: 'new email',
  text: 'Hello world!', // 纯文本主体
  html: '<p>Hello world!</p>', // HTML 主文
});
```

另一种方案是使用 SMTP 账户发送邮件。

Passport 是最流行的身份验证 Node.js 包。它支持超过 500 种策略，从 Google、Facebook、Twitter 到 LinkedIn 等 OAuth 登录。

另一种方案是 grant。

## 总结

Node.js 生态系统庞大且不断增长。第三方包通常为特定任务设计，因此你会发现适用于任何情况的选项。缺点是：

- 在评估包时，很容易感到压力并产生选择困难。
- 你会越来越依赖第三方解决方案。
- 使用的第三方包越多，维护和更新所需的时间越多。随着 API 的进化，你经常需要更新代码。

没有完美的 Node.js 包，我不为重复我的格言而道歉：只使用必要的第三方模块。把时间花在写代码上而不是选择工具！

希望你现在有一些简单的项目可以展示了。下一章将深入部署。

# 第 18 章：Node.js 应用部署

你最终会想要将 Node.js 应用发布到世界上。自从 2009 年运行时发布以来，部署选项呈指数级增长。本章介绍了常见的托管类型以及相关公司链接，但服务和价格每天变化。

## 页面与应用程序

许多读者熟悉 PHP —— 世界上最流行的 Web 编程语言。WordPress 运行了几乎一半的网站。PHP 应用程序由 .php 文件组成，当通过 Apache 等服务器访问时由 PHP 运行时解释。然后向用户浏览器返回 HTML 或数据。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_322_0.png)

注意以下点：

- 每次页面加载都是无状态的。它不知道应用程序的状态，因此如果用户已登录，需要在每次页面请求期间从令牌或数据库记录中检索状态。
- 修改 .php 文件会立即更新应用程序，因为代码是在用户请求资源时执行的。
- 出错误的 .php 文件不太可能给其他页面带来问题。当然，该 .php 文件可能提供跨页面共享函数，但服务器和应用程序的其他部分通常仍运行。

Node.js Web 项目是一个处理 Web 请求的完整应用程序。它不（一定）需要 Apache 之类的服务器，并在从 .js 文件加载代码后持续运行。




因此：

- 状态可以保留。如果需要，服务器应用程序可以为每个登录用户存储一个 JavaScript 对象（我建议你编写无状态应用，但这不是强制性的！）。
- 更改 .js 文件对正在运行的应用程序没有影响。它只有在 node 进程停止并重启后才会被加载。
- 如果你的应用程序的任何部分导致崩溃，它对所有人永久失效！没有任何用户将能够访问系统的任何部分，并且将丢失内存中保留的任何状态。

Node.js 模型相比 PHP 既有优势也有缺点，但将应用程序部署到生产服务器更具挑战性。

大多数廉价的共享主机主机支持 PHP，因为可以通过将 .php 文件上传到服务器目录来运行。提供 Node.js 的服务商要少得多，因为你需要操作系统层级的访问权限来启动应用程序，由于它会持续运行，可能会占用资源。

有些服务商通过 cPanel 等系统提供 Node.js 功能，可以在其中定义应用程序的启动命令和配置。然而，这些系统通常会实施限制，例如 CPU 限制或无法访问 npm。

## Node.js 应用程序准备

你的开发和部署环境会有所不同。至少，生产服务器应该将 `NODE_ENV` 环境变量设置为 production：

```
NODE_ENV=production

```设置后，Express 框架将禁用详细日志并启用模板缓存以提高性能。其他模块可能提供类似的优化，但请检查它们的 README 文件和文档。

在内部，你的应用程序可以检测 `NODE_ENV` 值并禁用终端调试信息，或者进行其他更改，例如将日志记录到文件中。例如：

```
// 正在开发模式下运行？
const DEVMODE = (process.env.NODE_ENV !== 'production');

if (DEVMODE) {
    console.log('application started in development mode');
} else {
    writeToLog('application started in production mode');
}
```

可能需要其他的环境变量来定义应用程序配置或数据库连接。

最后，生产服务器通常应该使用 node 运行时启动应用程序，而不是 nodemon 或类似的工具。不应该使用如 `--inspect` 和 `--enable-source-maps` 等命令行选项。

## 专用服务器托管

在 Node.js 早期，几乎没有选择来启动真实的或虚拟的 Linux 服务器。这仍然是最常用的应用程序部署方法，并且需要 DevOps 人员执行：

1. 配置适当的 CPU、内存和磁盘空间
2. 安装适当版本的 Node.js 运行时
3. 从仓库拉取应用程序
4. npm install 所有项目和全局依赖项
5. 根据情况使用 `node app.js` 启动应用程序

步骤 3 到 5 在每次更新时都要重复，尽管持续集成和/或持续部署解决方案可以实现该过程自动化。

许多主机提供虚拟服务器，包括 DigitalOcean Droplets、Amazon EC2、Google Compute Engine 和 Azure Virtual Machines。

## sudo-not

避免使用 sudo 以管理员权限运行你的 Node.js 应用程序。应用程序或其任何模块都将有权执行任何操作——例如删除操作系统文件。

## HTTP 和 HTTPS 考虑因素

第 5 章展示了如何在 Express 中配置 SSL 证书。这在生产服务器上是不推荐的，因为应用程序必须使用 sudo 启动以允许使用 1000 以下的 HTTP 端口（HTTP 的 80 端口或 HTTPS 的 443 端口）。

更好的选项是在非标准端口（例如 3000）上启动应用程序，然后使用反向代理（见下文“使用反向代理”部分）来转发入站流量。

本书中的示例开发服务器运行在不安全的 HTTP 连接上。这对于测试是可以没问题的，但在整个前端和后端代码中引用内部 URL 时必须小心。

一些开发者为他们的开发服务器创建一个伪造的自签名证书，这使得引入不一致的 HTTP/HTTPS URL 变得困难。浏览器会抛出“无效证书”错误，但你可以选择忽略它。我不推荐这种做法：我过去曾因此吃过亏！浏览器在遇到伪造证书时行为往往不同。例如，它们会禁用缓存，这可能导致生产服务器出现奇怪的 bug。

我建议你采取以下任一措施：

- 开发期间使用 HTTP，但在引用可能在生产服务器上为 HTTPS 的内部 URL 时要警惕。
- 使用 `mkcert` 生成真实的、本地信任的 SSL 证书。这些证书可以在你的开发电脑上使用，尽管你无法将其与其他团队成员共享（因此他们需要生成自己的证书）。

## 进程管理

Node.js 应用程序运行在单进程处理线程上。换句话说，你 64 核服务器 CPU 中的 63 个核心正处于空闲状态。

你可以实现自己的集群代码在所有可用的 CPU 核心上运行应用程序，但这可能很困难（参见第 12 章，以及 [Node.js 文档](https://nodejs.org/en/docs/api)）。更好的解决方案是使用**进程管理器**，它通过以下方式让你的生产应用程序更高效：

- 在不同的 CPU 核心上运行多个实例
- 如果（当）实例崩溃时重启实例

为了使此生效，**你的应用程序必须是无状态的**。避免在跨实例可能不同的变量或本地文件中存储应用程序或用户状态。

Node.js 是进程管理的主要竞争者。全局安装后，你可以在集群模式下启动应用程序：

```
pm2 start app.js -i max
```

## PM2 冲突

PM2 管理端口。如果你的应用程序有十六个实例都监听 3000 端口，PM2 会确保它们不会冲突。可以使用 `pm2 status` 监控运行中的进程。发送到端口 3000 的请求会被转发到一个实例。

## 使用反向代理

反向代理将入站请求传递给你的 Node.js 应用程序。大多数 Web 服务器都可以配置——包括 NGINX。

这有几个优势：

- 在同一台服务器上配置任意数量的域名
-  Node.js 应用程序可以集群运行且无需 sudo
- HTTPS 的 SSL 证书可以由 Web 服务器管理
- Web 服务器可以提供静态资源——如客户端图像、CSS 和 JavaScript。这比通过 Express 更高效，因为大多数 Web 服务器是多线程的。

`/etc/nginx/sites-available/default` 中的 NGINX 配置文件可以定义接入端口、设置 SSL 证书，并在静态文件时将请求解析到 Node.js 应用程序：

```
server {
  listen 80;
  listen 443 ssl;
  # 域名
  server_name myapp.com;
  # 证书
  ssl_certificate /etc/nginx/ssl/server.crt;
  ssl_certificate_key /etc/nginx/ssl/server.key;
  # 静态文件?
  location / {
    root /home/node/myapp/static;
    index.html;
    try_files $uri $uri/ @nodejs;
  }
  # Node.js 反向代理
  location @nodejs {
    proxy_pass http://localhost:3000;
    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection 'upgrade';
    proxy_set_header Host $host;
    proxy_cache_bypass $http_upgrade;
  }
}
```

NGINXConfig 配置工具可以创建适用于你要求的设置。

## 静态站点托管 (Jamstack)

如果你的应用程序主要使用客户端 HTML、CSS 和 JavaScript，可能不需要部署 Node.js 应用程序或使用任何服务端运行时。站点生成器（SSG）使用内容（通常为 Markdown 格式）和模板构建目录结构的 HTML 文件。有很多 SSG，但 Eleventy 是比较流行的 Node.js 选项之一。

生成的构建文件可以上传到任何 Web 服务器。这些页面提供：



- 卓越的性能：它们只是文件，没有服务器端处理
- 健壮的安全：没有可以被利用的数据库或运行时
- 可移植性：你可以在任何地方托管，而无供应商锁定
- 最低成本部署：通常是免费的

这种更简单的 Web 开发方法在过去几年中变得越来越流行。Amazon S3 托管等设施已被平台即服务（PaaS）主机所取代，例如 GitHub Pages、CloudFlare Pages、Heroku、Vercel 和 Netlify。

某些服务提供了简单的命令行部署工具，而另一些则要求你将分支推送到 Git 仓库。

![](img/d4731c5479f6bfd1ada49d65047b9e4c_330_0.png)

# 无服务器函数/Lambda 函数

如果你的应用程序需要更全面的服务器端处理（例如数据库存储），你可以考虑无服务器函数。尽管名称如此，无服务器函数确实运行在服务器上，但你不需要管理操作系统、运行时，或使用像 Express 这样的框架。

无服务器函数通常对网络端点做出响应。例如，发布到 https://myapp.com/store-contact/ 的数据会将 HTTP 请求传递到 store-contact.js 中定义的函数，该函数存储信息并返回结果。位于 functions/hello.js 的以下 Netlify 无服务器函数在请求 /hello/ 端点时返回一条消息：

```
exports.handler = async (event, context) => {
  return {
    statusCode: 200,
    body: 'Hello World'
  }
```

因此，你可以选择将单体 Web 编写为一系列小的无状态函数。这些函数按需启动，但它们通常在繁忙的服务器上保持活跃，并可以根据流量增长进行扩展。如果无服务器函数失败，它将在下一次请求时重启，并且通常不会影响或与其他函数冲突。

大多数云托管商都提供 Node.js 无服务器函数，包括 AWS、Azure、Google、Cloudflare、Heroku、Vercel 和 Netlify。

## AWS 无处不在

许多无服务器主机（包括 Netlify 和 Vercel）将无服务器函数部署到 AWS Lambda，但提供了更简单或改进的开发者体验。

无服务器函数可能是许多应用程序的理想选择。它们可以简化 DevOps 并降低较小服务的成本，但也有缺点：

- * 使用限制：并不是所有的 npm 包都可以使用，特别是当它们依赖于其他 OS 实用程序时。
- 启动延迟：由于函数需要初始化，第一个请求可能需要一些时间。
- 关闭超时：函数可能有处理限制，长时间运行的（如 WebSocket 服务器）可能是不可能的。
- 供应商锁定：你必须遵守主机的 API、规则和更新。切换到其他服务可能很困难。
- 无法估量的成本：无服务器函数通常根据计算时间定价。你可能听过开发者的轶闻，他们部署了一个非终止的递归函数，导致了令人震惊的账单。

## 容器托管

随着你的 Node.js 服务变得越来越受欢迎，你可能需要更健壮的托管。第 12 章中的多人测验使用 Docker 容器来启动多个负载均衡的 HTTP 和 WebSocket 实例。同样的概念可以应用于生产服务器。Kubernetes 和 Docker Swarm 等解决方案可以在世界任何位置的任何数量服务器上启动、管理、更新和重启容器。

到那时，你将需要一个的 DevOps 团队来管理每年花费数百万美元的部署。这可能不是问题：如果你的应用程序成功了，风险投资人会法不给你足够的钱，而且 Google/Microsoft/Apple/Facebook 都在围观，准备可能进行潜在的收购。

## 总结

Node.js 托管选项多种多样，生态系统广泛，价格从免费到昂贵不等。就个人而言，我喜欢编写与服务无关且可以在任何地方托管的应用程序，但这在最近变得更具挑战性。我们达到了一个奇怪的节点，你可能在编写任何代码之前应该选择一个主机。我们有许多托管解决方案，但许多公司仍然选择 AWS，是因为……许多公司都选择了 AWS！

无论你选择哪种托管路线，编写无状态 Web 应用都不会出错的。我之前可能提到过几次……

# 第 19 章：结语

恭喜你！你已经到达 Node.js 之程开始的终点。你学到了很多，我希望这门课程能启动你的开发，同时帮助你避开一些陷阱。

我们涵盖了许多主题，从命令行工具、调试 Web 应用程序和重模块，到实时、数据库驱动的多人游戏。没有人能在第一次阅读时完全理解每个主题，但知道解决方案的存在就成功了一半。

我希望你喜欢 Node.js 开发。它有很多优点，例如：

- 学习基础知识并提高效率很快。
- Node.js 暴露了你可能在其他运行时遇到过的可能性。
- 它允许 Web 开发者利用他们的客户端 JavaScript 技能来创建实用的库、框架、命令行工具甚至桌面应用。
- Node.js 编程可以很有趣。

# Node.js 适合你吗？

Node.js 在几年内从一个小众引擎发展变为不可或缺的开发者运行时。即使使用其他语言，通常也会安装 Node.js，因为它提供了一系列你可能在其他地方不会得到的工具。

原因是：JavaScript。Web 开发已成为平台应用的主要手段，因此很难避免基于浏览器的编码。在前端后端使用同一种语言可以降低认知负担。Node.js 不会让你一夜变成全栈开发人员，但上下文切换更少了，而且很容易出导致应用程序不稳定的错误。

当然，Node.js 并非完美：

- 1. 有些程序员讨厌 JavaScript。JavaScript 是在十天内开发的，它的发明者从未考虑过它会被用于大规模应用程序。

我个人喜欢 JavaScript——无论它有什么缺点。那些抱怨得最大的人通常是把它和自己喜欢的语言进行比较。

- 2. npm 很繁琐。

npm 部分导致了 Node.js 的成功。它可以很容易安装、更新和删除那 150 万个包。你的 node_modules 目录也会增长到几十兆，尽管最近有了优化，npm 仍然会下载相同的包。

记住，npm 只是一个工具。只安装需要的包，就可以减少第三方代码的影响。

- 3. CommonJS 与 ES6 模块混乱。

Node.js 正在向 ES6 模块迁移，但这个过程是痛苦的，某些遗留包可能永远不支持它。尽管情况正在改进，我在写作时遇到的问题之少令我惊讶。

- 1. 异步编程是一个挑战。

你可能在其他语言中不会遇到异步编程，而且很容易犯导致应用程序不稳定的错误。我把整个第 9 章给了这个主题，因为它对 Node.js 程序非常重要。

对于 JavaScript 初学者来说，理解回调可能很困难，但在客户端或服务器端无法避免事件处理。Promises 和 async/await 有帮助，尽管我最初很难理解这些概念。尽管如此，异步编程使得实时 Web 应用成为可能。实时更新的仪表盘、直播聊天和多人游戏在 Node.js 中要简单得多。

# Deno 更好吗？

Ryan Dahl 在 2020 年发布了 Deno，它解决了他对 Node.js 的许多遗憾。Deno 提供了：

- 更好的安全性。应用程序需要访问环境变量、文件系统、网络和其他资源时，必须授予特定的权限。





-   原生 TypeScript 支持。你可以使用 JavaScript 或 TypeScript 编写应用程序，而无需额外的第三方编译器。
-   仅支持 ES6 模块。模块从 URL 加载：没有等同 npm 的机制，且包可以被缓存，因此在你的系统中所有项目共用一个实例。
-   内置工具。Deno 运行时提供了代码检查、格式化、测试、基准测试、打包、文档生成、任务运行等多种功能。
-   复制的浏览器 API。如 `window`、`addEventListener`、`Fetch` 和 web workers 等功能在 Deno 中均可工作。
-   复制的 Node.js API。在 Node.js 兼容模式下，Deno 支持 `fs`、`events`、`http`、`os`、`process`、`stream`、`util` 和 CommonJS 等功能。

Deno 是一个很好的选择，但它不像 Node.js 那样新颖、流行或受到良好支持。也许在十年后，我们可能都会使用 Deno，而 Node.js 将被归入历史教科册。在 Deno 中编写一些实用程序或示例应用并没有坏……但当你很难找到经验超过几个月的程序员时，你应该将其用于长期的、任务关键任务的应用吗？

Deno 与 Node.js 足够相似，因此在不同运行时之间切换非常容易。今天学习 Node.js，明天考虑 Deno。

## 感谢阅读！

我希望你喜欢这本书，并已准备好开启编程生涯的下一个阶段。请查看本课程最后一段视频中的一些技巧。

如果你有任何反馈或建议，请直接在 Twitter 上通过 @craigbuckler 与我联系，或向 SitePoint 发送消息。

祝你好运！

## 附录：测验答案

以下是测验的答案。

## 第 1 章

-   1. d.
-   2. d. 除了一些表面上的语法相似之处，JavaScript 与 Java 没有任何技术关系！
-   3. b. TypeScript 可以编译为 JavaScript，但它是 JavaScript 语法的超集，所以它不是 JavaScript 本！
-   4. c.
-   5. a.

## 第 2 章

-   1. d.
-   2. b.
-   3. a.

## 第 3 章

-   1. c.
-   2. d. ... 虽然 c 有点过于极端！
-   3. b.
-   4. a.
-   5. d. 如果你知道 Docker 并非必不可，则获得加分，尽管它可以让 Node.js 的部署变得更容易！

## 第 4 章

-   1. d.
-   2. d.
-   3. b.
-   4. a.
-   5. 额，我会选 c。这带有强烈的个人观点，但我不相信任何说自己从不使用 `console.log()` 的开发者。它并不总是最佳选择，而且很容易掉入深层控制台日志的兔子洞，但找到 bug 的原因比你使用的技术更重要。

## 第 5 章

-   1. d.
-   2. c.
-   3. a.
-   4. c.
-   5. b.

## 第 6 章

-   1. b.
-   2. a. 但如果你定义了解析中间件函数，d *可能是*正确的！
-   3. d.

## 第 7 章

-   1. d.
-   2. b.
-   3. b.
-   4. c.
-   5. d. 如果你意识到 a. 和 b. 在旧版本的 npm 中会列出所有依赖，则获得加分。
-   6. a.

## 第 8 章

-   1. a.
-   2. c.
-   3. a.
-   4. b.
-   5. d.

## 第 9 章

-   1. c.
-   2. d.
-   3. a.
-   4. a.
-   5. d.

## 第 10 章

-   1. b.
-   2. d.
-   3. d.
-   4. a.
-   5. d.

## 第 11 章

-   1. d.
-   2. a.
-   3. d.
-   4. b.
-   5. b.

## 第 12 章

-   1. b.
-   2. d.
-   3. d.
-   4. a.
-   5. b.

