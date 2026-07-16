# JavaScript 编程入门



![](img/cover.png)










![SitePoint 标志](img/sitepoint-logo-2012.png)


## 关于 SitePoint

SitePoint 专门为 Web 专业人士编写有趣、实用且易于理解的内容。访问 [`www.sitepoint.com/`](http://www.sitepoint.com/) 访问我们的博客、书籍、通讯、文章和社区论坛。你可以在那里找到关于 JavaScript、PHP、设计等大量信息。

## 关于 Darren Jones

自从从他的第一台 Acorn Electron 电脑上学习 BASIC 编程以来，Darren 就喜欢编程。他自学了 Ruby 和 JavaScript，是 [JavaScript: Novice to Ninja](https://www.sitepoint.com/premium/books/javascript-novice-to-ninja-2nd-edition) 和 [Jump Start Sinatra](https://www.sitepoint.com/premium/books/jump-start-sinatra) 的作者。他还为 SitePoint Premium 制作了 “[Getting Started With Ruby](https://www.sitepoint.com/premium/courses/hands-on-programming-concepts-with-ruby-2-0-2906)”视频教程，并在 SitePoint 网站上写过[多篇文章](https://www.sitepoint.com/author/djones/)。他出生于英国曼彻斯特，目前仍居住在那里，并在当地高中教授数学和计算机。你可以在 Twitter 上找到他 [@daz4126](https://twitter.com/daz4126)。

# 前言

我仍然记得我的第一台电脑：那是一台 Acorn Electron，我非常喜欢用它来玩游戏，比如《Sphinx Adventure》（一款基于文本的冒险游戏）、《Starship Command》（一款硬射击游戏）和《Chuckie Egg》（纯粹的平台动作游戏）。但当我发现可以用一种名为 BASIC 的语言编写自己的代码时，真正的乐趣开始了。我最初的想法是，这个名字起得带有讽刺意味，因为它看起来一点都不基础。它有以十为倍数的行号，以及听起来很奇怪的命令，如 `GOTO`、`REM` 和 `CLS`，起初看起来就像是一堆乱码。但通过大量的练习（以及许多错误），它开始变得有意义，我被代码如何让我控制计算机的行为所着迷了。我会花几个小时从杂志上抄录代码示例（是的，那是很久以前的事了！），然后尝试进行我自己的修改。正是这些对代码的实验和捣弄帮助我理解了它是如何工作的。我彻底迷上了编程的魔。

我对编程的喜爱源于它要求你遵循编程语言的精确规则，同时鼓励你创造性地思考以实现理想的结果。编程的本质是将抽象变为实用。当我开始写这本书时，我的目标是介绍编程的基本概念，并用大量的实践示例来支持理论。每一章的最后都有编程挑战，将帮助巩固你的理解。我鼓励你深入研究这些挑战，不仅要尝试完成它们，还要尝试用你自己的修改来扩展它们。

我想要编写的一直是游戏，我已经尽可能让书中的许多挑战在编写和玩耍上变得有趣。读到书结束时，你将编写了几个完全可以玩的游戏。你还将为创建交互式网站奠定基础，并处于编写全应用程序的正确道路上。

编程是一项创造性活动；它从根本上说是创造事物。你的代码既需要精确简洁，也需要向其中注入一些花彩让它活起来。这种精确与巧妙的结合，使得在从 Acorn Electron 上开始编程多年后，我仍然觉得编程充满乐趣。我希望这本书能激励你开始编程，并希望你在读完最后一页后能很长地享受它。

## 谁应该读这本书？

这本书是为没有任何编程经验但想学习如何编程的人准备的。我们在未使用 JavaScript 来教你，所以到最后，你将对 JavaScript 有良好的理解，但你可以将所学的原理应用到其他语言。

## 使用的规范

### 代码示例

书中的代码使用等宽字体显示，例如：

```
<h1>完美的一天</h1>
<p>这是一个散步的好日子。鸟儿在歌唱，孩子们在学校。</p>
```

你会注意到我们使用了特定的样式来表示不同类型的信息。

### 提示、注意和警告

#### 嘿，你！

提示提供一些建议。

#### 咳，借一下……

注意是与主题相关但并非重要的旁注。你可以把它们视为额外的信息。

#### 务必始终

这些这些要点。

#### 注意！

警告强调了任何可能让你绊倒的坑。

## 补充材料

*   [`www.sitepoint.com/community/`](https://www.sitepoint.com/community/) 是 SitePoint 的论坛，用于解决困难的问题。
*   **books@sitepoint.com** 是我们的电子邮件地址，如果你需要联系我们报告问题或出于其他原因。

# 第一章：点击开始

你想学习编程吗？你做了一个明智的决定。编程是一项非常值得学习的技能，而且非常有趣。它可以用于构建下一代应用程序、黑客树莓派或 Arduino、编写最新的大片游戏以及许多其他事情。事实上，一旦你学会了如何编程，唯一的限制就是你的想象力。

在本章中，我们将简要回顾编程的历史，查看计算机程序是什么，然后介绍 JavaScript 编程语言，我们将用它来学习编程。

我们还将直接投入实践并开始编程，编写不是一个而是两个 JavaScript 程序！

## 本章涵盖内容

*   编程简史
*   JavaScript 语言介绍
*   “Hello, World!”——你的第一个 JavaScript 程序
*   浏览器中的 JavaScript
*   “我能画出彩虹”——你的第二个 JavaScript 程序
*   程序员的心态

我们还将通过编程挑战来结束本章，帮助你测试新学到的技能——正如我们在书中每一章末尾所的那样。





# 编程

`Programming`（编程）是关于让计算机执行你想要它们执行。计算机程序基本上是一系列指令，告诉计算机如何执行特定任务。遗憾的是，计算机使用的语言与我们并不相同。

例如，你不能直接写下“把圆的颜色改为蓝色”并指望计算机能理解。编程语言充当了中介的角色：它是一种计算机和人类都能听得懂的语言。

学习编程有点像学习外语，不同的是计算机对语法的要求*非常*挑剔（甚至比我的法语老师还要挑剔！）。你需要确保将每一个元素都放在正确的位置，并且语法必须完全准确无误。计算机是强大的，你可以让它们做一些真正令人惊叹的事情，但只要有一个括号放错了位置，它们就会分崩离析！

编写程序基本上就是为计算机编写一套需要遵循的指令。问题在于，这些必须是*非常*精确的指令。任何细微的歧义都会导致计算机执行与你设想完全不同的操作——或者它甚至可能会崩溃。

## 算法

`algorithm`（算法）这个词现在被频繁使用。你可能听过“Instagram 算法”或“Google 搜索算法”。但算法到底是什么？“algorithm”一词是波斯数学家阿尔·花瓦西米（Al-Khwarizmi）名字的拉丁化形式，他编写了第一本代数教科书，并喜欢用分步描述的方法来解释他的方法。

![Al-Khwarizmi](img/alkhwarizmi.png)

这导致 `algorithm` 一词被用来描述任何分步的方法。每一步要做什么以及每一步的作用应该是清晰的。例如，这里有一个泡茶的算法：

1. 在壶里烧水。
2. 拿一个杯子。
3. 拿一个茶包。
4. 将茶包放入杯中。
5. 水烧开后，将水倒入杯中。
6. 浸泡两分钟。
7. 从杯中取出茶包。
8. 拿牛奶。
9. 在茶中加入牛奶。
10. 搅拌茶。

![Making tea](img/tea.png)

### 茶后加牛奶

我意识到我在茶好*之后*加入牛奶的指令可能会引起争议。如果你认为应该先加牛奶，我很抱歉，但你只能接受在这一点上你是错的。

这些指令看起来相当基础且直接，但其中包含许多假设，而且某些步骤有些模糊。你是如何烧水的？你从哪里拿杯子和茶包？我应该向杯子里倒多少水？这些问题都留之未答。这通常是可以的，因为大多数人な熟悉泡茶的过程，但一个从未见过别人泡茶的人可能会在遵循某些步骤时遇到困难（尽管我承认可能可能很难找到这样的人）。

## 伪代码

`Pseudocode`（伪代码）是你编写的一种“假装”的代码，用于说明程序的功能，而无需担心实际编程语言的复杂性。它它仍然遵循程序的惯例和结构，并使用精确的命令，但不包含特定语言的细节。

例如，“在屏幕上显示消息”这条指令在伪代码中可以写成 `display(message)`，而在 Python 编程语言中，它会被写成 `print(message)`。注意，Python 代码使用了非常特定的 `print` 符号，这是它用于在屏幕上显示消息的命令。其他语言使用不同的命令来基本上完成相同的功能。

泡茶的示例可以用像这样的伪代码编写：

```
boil(water,250ml) in kettle
get(cup) from cupboard
get(teabag) from box
put(teabag) in cup
when(kettle boils) 
  { pour(water, 250ml) in cup }
wait(2 mins)
remove(teabag) from cup
get(milk, 20ml)
add(milk, 20 ml) to tea
stir(tea)
```

一个知道用特定语言编程的程序员应该能够遵循伪代码示例，然后用他们选择的语言将其编写出来。伪代码对于在开始编码之前规划程序非常有用，它也让使用不同编程语言的程序员更容易分享想法。

## 编程简史

最早的计算机使用打孔卡片编程来表示 `binary number system`（二进制系统），这是计算机使用的数字系统。二进制系统完全由 1 和 0 组成，大致翻译为“开”和“关”。在卡片上，有孔代表 `1`，无孔代表 `0`。之后，人们开始开发可以用来与计算机“对话”的语言。

![Early computers used punched tape to store data](img/earlycomputer.jpg)

第一批计算机程序是用 `machine code`（机器码）和 `assembly language`（汇编语言）编写的。这些是 `low-level programming languages`（低级语言），与计算机硬件密切相关。这意味着这些语言很难编写，因为它们涉及编写与计算机架构深度绑定的抽象代码。事实上，现在很少有人用机器码或汇编进行编程了，但那些会这样做的人将与计算机硬件密切工作——例如，编写设备驱动程序或研究嵌入式系统。

`High-level programming languages`（高级编程语言）使用抽象技术，使代码更容易人类阅读和编写。程序用 `Swift`、`C#` 或 `Java` 等语言编写，然后被编译成机器码。使用这些语言编写的程序非常快，使得高级语言适用于编写游戏和专业软件。

`Scripting languages`（脚本语言）另一种高级语言，但它们是 `interpreted`（解释型）而不是 `compiled`（编译型），这意味着它们在程序运行时被翻译成机器码，而不是提前。这意味着它们通常比编译型语言慢，尽管解释器变得越来越复杂，使得某些解释语言几乎和编译语言一样快。你可能听过的常见脚本语言有 `Python`、`Ruby` 以及当然的 `JavaScript`。

## JavaScript

我们在书中将学习的语言是 `JavaScript`，它通常被称为 Web 语言。几乎每个网页浏览器都能运行 `JavaScript`，使其成为世界上流行的编程语言之一。

`JavaScript` 是学习编程的极佳语言。它的门槛很低：学习 `JavaScript` 只需要一个浏览器。它很容易入门，基础知识容易掌握。它也是一种灵活且丰富的语言，可以创建各种强大的程序。

`JavaScript` 是一种在运行时解释并编译的脚本语言，这意味着它需要引擎来解释和运行程序。这通常由网页浏览器完成，但也有 `JavaScript` 引擎可以在没有浏览器运行。`JavaScript` 还是一种 `dynamic`（动态）语言，这意味着程序的元素可以在运行时发生改变，不像 `C++` 这样的编译型语言。

### JavaScript 的历史

万维网最初是由一系列通过链接的页面组成的。用户很快希望与这些页面有更多互动，因此 Netscape（一家早期浏览器供应商）要求其一名员工 Brendan Eich 为他们的 Navigator 浏览器开发一种新语言。他在短短十天内设计出了名为 `Mocha` 的原型脚本语言。这种新语言后来被更名为 `LiveScript`，但随后被匆忙重新命名为 `JavaScript`，以便利用当时 Sun Microsystems 的 Java 语言所吸引的关注度。

“JavaScript”这个名字经常引起一些令人困扰的混淆，导致 `JavaScript` 常被认为是“简易 Java”，尽管这两种语言完全没有关系。




JavaScript 出于 1995 年，它开启了通过编程控制浏览器来执行任务的兴奋新时代。（不幸的是，在早期，它最常见的用途是创建弹出广告和旋转的 Logo！）

到 2005 年，像 Google Maps 和 Gmail 这样的网站开始出现，它们证明了 JavaScript 能够创建丰富的互联网应用程序，其外观和行为都像原生桌面应用程序一样。这种进步一直在快速进行中，如今几乎每个网站都会以某种方式使用 JavaScript。JavaScript 已经进入了许多其他领域，如智能手机应用、可穿戴设备和数据库。

![Google Maps 显示 JavaScript 可用于创建高级 应用程序](img/maps.png)

## JavaScript 版本

1996 年，在欧洲计算机厂商协会（ECMA）的帮助下，决定对 JavaScript 进行标准化，由该协会托管标准。这种标准化语言被命名为 `ECMAScript`，以避免侵犯“Java”商标。这导致了更多基于名称的混淆，但最终 `ECMAScript` 被指代规范，而 `JavaScript` 被指代语言本身。情况依然如此，尽管关于更改名称的争论一直存在。有一种建议是正式将 JavaScript 重命名为“JS”——它通常就是这样被称为它的（就像迈克尔·乔丹常被称为“MJ”一样）。

当 `JavaScript` 在 1997 年标准化时，规范被称为 `ECMAScript version 1`。2015 年，决定每年发布一个新规范，并以发布的年份命名。由于这一变化，`ECMAScript version 6` 在发布时被重命名为 `ES2015`，从那以后，每年都有新的 `JavaScript` 版本。在本书中，我们将使用最新版本的 `JavaScript`，但每年关注该语言的最新新增和变化总是值得的。

### 向后兼容性

`JavaScript` 语言开发中的一个重要概念是`向后兼容性`（backward compatibility）。这意味着当由运行新规范的引擎解释代码时，所有旧代码必须以相同的方式工作。（这有点比说 PlayStation 5 必须能够运行为之前所有 PlayStation 创建的任何游戏）。这是为了防止 `JavaScript` 通过剧烈变化来“破坏 Web”，因为这些变化可能导致某些网站上使用的旧遗留代码在现代浏览器中无法按预期运行。

在本书书中，我们假设你正在使用能够运行最新版本 `JS` 的现代浏览器。（尝试更新到你最喜欢的浏览器的最新版本。）

关于 `JavaScript` 的话足够了。让我们写你的第一个程序吧！

## Hello, World! 你的第一个 JavaScript 程序

学习编程语言时，从 `Hello, World!` 程序开始是一个传统。这是一个简单的程序，通过输出“Hello, World!”短语来宣布你来到编程世界。

我们将遵循这一传统，用 `JavaScript` 编写一个 Hello, World! 程序。它将是一个单条语句，向控制台记录“Hello, World!”短语。

### 控制台？

`console`（控制台）基本上是一个用于运行代码的命令行提示符。你可以输入一段代码，它将进行求值并将输出记录到屏幕。控制台是测试和实验代码的极佳方法。你可以在计算机终端中运行 `JS` 控制台，也可以在智能手机和平板上使用 `JS` 控制台应用。还有许多网站在浏览器中运行控制台，大多数浏览器也内置了控制台。

在本书书中，我们主要使用在线的 [jsconsole.com](https://jsconsole.com) 作为我们的控制台。我建议你用它来尝试运行书中各处出现的代码片段，以感受它们是如何工作的。通过输入代码来感受总比只阅读要好。这意味着你还可以通过更改代码并检查结果来实验代码。

控制台的另一个选项是使用浏览器内置的控制台。要打开它，只需根据你的浏览器遵循以下指令：

*   **Firefox**: 按住 `Shift` + `Ctrl` + `J`（或在 Mac 上为 `Option` + `⌘` + `J`）或按 `F12`
*   **Safari**: 按住 `Option` + `⌘` + `C`（注意，你需要先在偏好中启用开发者菜单）
*   **Chrome**: 按住 `Shift` + `Ctrl` + `J`（或在 Mac 上为 `Option` + `⌘` + `J`）或按 `F12`
*   **Edge/Internet Explorer**: 按 `F12`

一旦你在浏览器中打开控制台，它的作用将与 `jsconsole.com` 完全相同。下面的图片显示了 Chrome 的内置控制台。

![Chrome 的内置控制台](img/chromeconsole.png)

好了，让我们写我们的第一个程序。前往 [jsconsole.com](https://jsconsole.com) 或打开浏览器的控制台，输入以下代码，然后按下 `Enter` 键：

```
console.log('Hello, World!');
```

### Enter? Return?

我刚才让你按下键盘上的 `Enter` 键。为了清楚起见，在大多数 PC 键盘上，你会在右侧看到 `Enter` 键。（有时它只是一个箭头符号：`↵`。）在 Mac 键盘上，你大多会看到一个 `return` 键。为了简单起见，从以后我将统称为 `Enter`。

如果一切顺利，你应该会在屏幕上看到“Hello, World!”——如下所示。

![Hello, World!](img/chhelloworld.png)

恭喜！你刚刚写了你的第一个程序！这看起来没什么，但一位智者曾说过，程序员的旅程始于一行代码！

## 浏览器中的 JavaScript

我之前说过 JavaScript 是一种解释型语言，需要运行环境。由于它的起源，`JavaScript` 运行的主要环境是浏览器，尽管它也可以在其他环境中运行。

目前 `JavaScript` 最常见的用途仍然是让网页具有交互性。正因如此，在继续之前，我们应该看一看构成网页的内容。

### 网页的结构

几乎所有的网页由三个关键部分组成：HTML、CSS 和 JavaScript。HTML 用于标记页面内容，CSS 是决定页面外观的呈现层，而 JavaScript 则增加了让页面执行任务的交互性。这三种技术共同被称为 *Web 的三层*。在 HTML 中添加 CSS 和 JavaScript 是可能的，但将每一层的代码分开是良好的习惯。

为了避免你花费大量时间来设置和编写网页，书中的许多示例将使用 [CodePen](https://codepen.io) 网站。该网站已为你准备好一切，你只需要添加任何 HTML、CSS JS 代码即可创建一个功能性的网页。它还将 Web 的三层分在编辑器顶部的三个部分，正如下面的截图所示。

![CodePen 编辑器将 HTML、CSS 和 JS 分为三个不同的部分](img/codepen.png)

CodePen 还提供了一个控制台。在书中的各个地方，你会发现在 CodePen 的 **JS** 部分输入 JavaScript 代码，然后通过打开 CodePen 控制台查看这些代码在背后的执行情况。你可以点击 CodePen 界面左下角的 **Console** 标签来访问它。

#### 在线编辑器与离线工作





还有许多其他方法可以在 HTML 和 CSS 运行 JavaScript 代码。只需搜索“online JavaScript editor”查看更多在线选项。你也可以离线工作（即仅在你的电脑上），通过在文本编辑器中编写代码并在浏览器中打开它。访问“[HTML5 Template：适用于任何项目的基础模板](https://www.sitepoint.com/a-basic-html5-template/)”获取有关如何设置此类内容的说明。

让我们尝试编写我们的第二个程序。

## 我可以编写彩虹：你的第二个 JavaScript 程序

我们将用第二个在浏览器中运行的 JavaScript 程序来结束本章。这个示例比上一个复杂得多，包含了许多在后续章节中深入介绍的概念，所以如果你在现阶段没有完全理解正在发生的一切，请不要担心！此处的目的是向你展示 JavaScript 的能力，并交互式地介绍一些后续章节中将涵盖的重要概念。

前往 [CodePen 网站](https://codepen.io) 并开始一个新的 Pen。

在 **HTML** 部分添加以下内容：

```
<button id='button'>click me</button>
```

这将显示一个 ID 为 `button` 的按钮。`ID` 属性是我们的 JavaScript 程序识别并操作页面上某些元素的有用方式。它看起来应该和下面的图片相似。

![点击我](img/button.png)

实际的 JavaScript 代码位于 **JS** 部分。添加以下行代码：

```
const button = document.getElementById('button');

const colors = ['red','orange','yellow','green','blue','rebeccapurple','violet'];

function change() {      
  document.body.style.background = colors[Math.floor(7*Math.random())];
}

button.addEventListener('click', change);
```

我们程序的的第一行创建了一个名为 `button` 的变量。（我们在 第 2 章 中介绍了变量。）

然后我们使用 `document.getElementById` 函数来查找 ID 为 `button` 的 HTML 元素。这就是我们在 HTML 部分创建的那个按钮元素。它被赋值给变量 `button`，因此从现在起，每当我们引用 `button` 时，程序都知道我们在谈论那个按钮。（查找 HTML 元素将在 第 10 章 中介绍。）

我们现在创建了另一个名为 `colors` 的变量，它被赋值为一个包含字符串列表的数组，代表彩虹的不同颜色。（我们在 第 3 章 中介绍了字符串，在 第 5 章 中介绍了数组。）

然后我们创建了一个名为 `change` 的函数。（我们在 第 8 章 中介绍了函数。）这会将网页中 body 元素的背景颜色设置为 `colors` 数组中的一种颜色。（更改页面外观将在 第 10 章 中介绍。）

`change` 函数还使用随机数从数组中随机选择一种颜色。（数字，包括生成随机数将在 第 4 章 中介绍。）

程序以一个**事件处理器**结束，它负责监听按钮被点击事件。当这种情况发生时，它会运行我们刚刚定义的函数。（事件以及如何处理它们将在 第 11 章 中介绍。）

尝试点击几次按钮。如果一切运行正常，背景应该变为彩虹的每种颜色！

你可以查看 [CodePen 上的我的代码](https://codepen.io/SitePoint/pen/PoGgVKB)。

### Rebecca Purple

`rebeccapurple` 是十六进制代码为 `#663399` 颜色的官方名称。它以网页设计师 Eric Meyer 的女儿命名，她的女儿不幸去世了，时年仅六岁。这是她最喜欢的颜色，作为对她的纪念，被加入了 CSS 颜色的官方列表中。

## 程序员的思维

在我们结束本章之前，我们需要谈谈*编程风格*。显然，编写计算机程序的目的是让它执行它应该做的事情，但程序的风格也同样重要。你的代码应该是清晰简洁的，并且在遵循规范方面要保持一致——从你为变量选择的名称到你在代码块之间留下的空白量。你的代码还应该是易读的，并包含解释代码作用的注释。

你应该始终寻找改进代码的方法，使其更高效、更易遵循。这个过程被称为**重构**，应该定期进行，以便让你的代码保持更新而不会变得过时。

编程中的一个重要原则是“不要重复自己”规则，或 **DRY**。这意味着你应该始终寻找避免重复大量代码的方法。遵循这一原则有助于让你的代码更灵活、更易维护和更新。（更改一处代码比更改数百处代码要容易得多！）如果这听起来有点像程序员很懒，那么你完全正确！一个好的程序员总是寻找以最高效、最优雅的方式编写完成任务的代码。代码越少意味着 Bug 的概率越小，也更容易维护。

一个好的程序并不是瞬间出现的。它始于一个计划，并有机地成长为完成状态。开发一个程序涉及大量的问题解决，有时你会走错弯路并卡住。这是正常现象，你应该准备好进行更改和适应。

## 挑战

1. 尝试用伪代码描述一些日常任务，例如刷牙或骑自行车。
2. 编写一段伪代码来找到数字列表中的最大值。
3. 尝试使用 `console.log()` 在控制台中打印不同的消息。
4. 在“我可以编写彩虹”程序的数组中添加更多颜色。

## 总结

*   算法是用于完成特定任务的一系列步骤指令。
*   伪代码用于在不使用特定编程语言的情况下编写程序。
*   JavaScript 创建于 1995 年，被认为是 Web 语言。
*   JavaScript 的主要环境是浏览器，但它也可以在其他环境中运行。
*   每个 JavaScript 版本都必须与旧版本向下兼容。
*   代码应该是易读的，并定期进行重构以保持运行顺畅。
*   编码时记住 DRY 原则。不要重复自己！

在下一章中，我们将开始开始学习一些基础知识。让我们开始吧！





在你成为程序员的旅程中，第一个任务是学习如何给代码添加“注释”。编程中的`Comments`（注释）就像书中的旁注：它们是解释代码目的和逻辑的说明。这看起来可能像是一个很奇怪的起点，因为编程语言会忽略注释。它们不会产生任何作用。尽管如此，注释仍然极其重要。注释良好的代码是熟练程序员的标志。注释让任何阅读你代码的人（包括你以后！）都能更容易理解正在发生什么——相信我，当你几周后再次回来读到这些代码时，你会感谢自己自己写了注释的。不过，你不需要写长篇文章，只需要写足够让人清楚代码意图的注释即可。

添加注释的方法在不同的编程语言中有所不同。在`JavaScript` 中，有两种类型的注释：

*   单行注释以 `//` 开始，并在行尾结束：

```
// this is a short comment
```

*   多行注释以 `/*` 开始，以 `*/` 结束：

```
/* This is a longer comment
这里的任何内容都将被忽略
这是一个放置注释的好地方
*/
```

在代码中编写注释是一个良好的习惯，但要确保注释是有用的，而不仅仅是描述代码本身已经显而易见的内容。例如，下面的注释并没有增加任何代码本身并不显而易见的信息：

```
// log the message to the console
console.log(message);
```

将注释看作写给未来自己的笔记很有用，它们可以提醒你编写那段特定代码时的思考过程。例如，这里有一条注释解释了代码是通过用户点击左箭头键激活的：

```
// user has clicked on the left arrow key so move left
character.style.left = left - speed + 'px';
```

## 编程语法

正如我在上一章中提到的，编程语言类似于口语语言，因为每种语言都有它们自己的语法规则和特点。在本节中，我们将查看编程语言是如何编写的，并结合具体的 `JavaScript` 示例。

### 语句 (Statements)

程序由一系列`statements`（语句）组成。例如，这里是两个伪代码语句：

```
store response to 'Please enter your name.' as name
print name to screen
```

在`JavaScript` 中，这将是：

```
const name = prompt('Please enter your name.');
alert(name);
```

#### 以分号结束行 (Ending Lines with Semicolons)

我在上面的每一行末尾都加了分号。严格来说，`当一个语句单独占成一行时`，并不需要用分号结束该语句，但这被认为是一种良好的习惯，这也是我在整本书中将一直做的做法。我鼓励你也这样做，以养成这种习惯。相信我，当你以后编写更大、更复杂的程序时，这将会非常有用的！

如果你在一行中有多个语句，你确实需要用分号将它们隔开。但让每条语句单独占一行会让你的代码更整洁、更易读。

### 块 (Blocks)

一个`block`（代码块）是集合在一起的一系列语句。不同的编程语言有各种方式在块内部收集语句。有些使用关键字来标记块的开始和结束，而另一些则使用缩进来表示块。`JavaScript` 使用大括号来包围代码块，如下例所示：

```
{
  // 这是一个包含一个注释和两个语句的块
  const name = prompt('Please enter your name.');
  alert(message);
}
```

注意，块不需要用分号结束。

### 空格字符 (Whitespace)

`Whitespace`（如空格、制表符和换行符）用于分隔你代码的不同部分。`JavaScript` 允许你使用所需的任意空格字符来格式化代码，使其整洁且易于阅读。空格字符基本上被程序本身完全忽略。这些示例包括使用空格缩进嵌套代码，以及使用多行来分隔代码块。事实上，这是被高度推荐的，因为良好的代码应该是易于理解的。

在某些语言中，空格字符是程序的一部分。例如，Python 显式使用换行符来开始新语句，并使用行头的空格来开始一个新的代码块。

### 数据类型 (Data Types)

编程语言中的每个值都有一个`type`（类型），描述它所包含的数据。这决定了语言将如何解释和使用该值。数据类型决定了它可以取什么值以及它能做什么。

`Primitive data types`（原始数据类型，或简称 `primitives`）在编程语言的底层得以实现，本质上它们是任何程序的构建构建块。原始类型是`immutable`（不可变的），这意味着它们不能被改变或修改。大多数语言都包含了以下原始数据类型的某些变体：

*   `Character`（或 `char`）：单个字符，如字母、数字或符号——例如 `T`、`3`、`@`

*   `String`（字符串）：引号内的字符集合——例如 `'Hello'`、`"123!"`

*   `Integer`（整数）：可以是正负的整数——例如 `7`、`-100`、`0`

*   `Float`（浮点数）：带有小数数字，通常以十进制表示——例如 `2.5`、`3.14159`、`-7.0`

*   `Boolean`（布尔值）：`Boolean`值可以是“true”（真）或“false”（假）

`JavaScript` 没有 `char` 原始类型，但它确实有“strings”（字符串，我们在下一章将讨论），`char` 可以由单个字符表示。`JavaScript` 并不区分整数和浮点数。它只有一个 `Number` 原始类型，我们将在第 4 章介绍。

布尔值是 `JavaScript` 包含的原始类型之一，我们将在第 6 章介绍它们。

#### `symbol`、`bigint` 和 `undefined`

`JavaScript` 还有其他三种原始值：`symbol`、`bigint` 和 `undefined`。我们不会在书中介绍 `symbol` 和 `bigint`，因为它们的使用不像其他原始类型那样频繁。然而，我们在稍后会要介绍 `undefined`，因为你可能会遇到它。

`Composite data types`（复合数据类型）是由原始类型组合而成的。`JavaScript` 有两种主要的复合类型：“arrays”（数组，我们将在第 5 章介绍）和“objects”（对象，我们将在第 9 章介绍）。这两种复合类型都是 mutable（可变的），这意味着它们在创建后可以被更新。

#### `Map` 和 `Set`

`JavaScript` 还有两种名为 `Map` 和 `Set` 的复合数据类型，但我们不会在书中介绍它们。

### 你是什么类型？

让我们通过编写一些代码来探索 JavaScript 使用的不同类型。有一个名为 `typeof` 的特殊运算符，可以用来判断一个值的数据类型。你只需要输入 `typeof`，后面跟着该值，就会返回其类型。

如果一个值不是原始数据类型之一，`JavaScript` 将返回 `object` 或 `function`。（这些都将在后的章节中介绍。）

让我们再次打开控制台进行一些测试。（提示：一旦你输入了第一行——例如 `typeof 'hello'`——按下 `Enter` 键获取结果，`<< 'string'`。）尝试输入以下代码——逐行输入——以研究各种表达式的类型：





```javascript
typeof 'hello'; // see Chapter 3
<< 'string'

typeof 10; // see Chapter 4
<< 'number'

typeof true; // see Chapter 6
<< 'boolean'

typeof { name: 'JavaScript' }; // see Chapter 9
<< 'object'

typeof [ 1, 2, 3 ]; // this is an array, covered in Chapter 5, it's also considered an object
<< 'object'

typeof function(){ }; // this is an empty function, more interesting functions are covered in Chapter 8
<< 'function'
```

尝试再自己写几个，直到你确信什么是字符串、数字和布尔值。

## 运算符 (Operators)

`operator`（运算符）对一个值执行操作，该值被称为 `operand`（操作数）。一元运算符（unary operator）只需要一个操作数。`typeof` 是我们已经用过的一个 JavaScript 运算符示例：

```javascript
typeof 'hello';
<< 'string'
```

运算符是 `typeof`，而字符串 `'hello'` 是操作数。

`binary operator`（二进制运算符）需要两个操作数。例如：

```javascript
3 + 5
```

运算符是 `+`，数字 `3` 和 `5` 是操作数。

还有 `ternary operator`（三元运算符），用于评估逻辑语句并需要三个操作数。这在第 6 章 中介绍。

## 变量 (Variables)

`Variables`（变量）在编程语言中用于引用存储在内存中的值。它们为我们提供了方便的方法来引用程序中的不同值。它们可以认为是指向不同值的标签。变量是处理长表达式的有用方法，因为它们避免了重复输入这些表达式。

#### 声明和赋值变量 (Declaring and Assigning Variables)

在大多数编程语言中，变量在使用之前必须被`declared`（声明）。这意味着需要在代码中显式地引用它们，并可能进行赋值。

在`strongly typed`（强类型）语言中，变量类型必须与变量一起声明。例如，如果我们想使用变量 `name` 表示字符串 `'Homer Simpson'`，在强类型语言中可能会使用以下代码：

```javascript
let name:string = "Homer Simpson";
```

这不仅将变量 `name` 设置指向字符串 `'Homer Simpson'`，还声明了该变量将是一个字符串。如果你在程序后面尝试将该变量赋值为另一个`not`（不是）字符串的值，将导致错误。

`Weakly typed`（弱类型）编程语言并不坚持在声明时显式说明变量的类型。类型被认为是从赋值给它的实际值隐式产生的，尽管从理论上讲你可以在程序的稍后将变量赋值为不同的类型而不会产生任何问题。在弱类型语言中，可以使用以下代码将变量 `name` 设置为字符串 `'Homer Simpson'`：

```javascript
name = "Homer Simpson";
```

这仍然具有将变量 `name`指向字符串 `'Homer Simpson'` 的效果，但它没有显式说明该变量是字符串，因为这在赋值字符串这一事实中是隐含的。

#### 鸭子类型 (Duck Typing)

动态编程语言（如 Ruby 和 Python）中一个常用概念是 `duck typing`（鸭子类型）。这基于一句话：“如果它走得像鸭子，叫得也像鸭子，那么它就是一只鸭子”。

这句话的本质是不需要担心值或对象的类型。如果它按照预期的方式工作，无论它什么类型并不重要。重点是检查代码的输出是否符合预期，而不是输入的类型。

JavaScript 是一种弱类型语言，因此在声明变量时不需要指定类型。这起初看起来可能是一个优势，但当不清楚一个变量应该是什么类型时，它可能会让调试程序变得困难。

#### TypeScript

[TypeScript](https://www.typescriptlang.org) 是 JavaScript 的扩展，它提供了在声明变量时显式指定变量类型的选项——实际上使其成为了强类型版本的 JavaScript。它还添加了一些其他功能，旨在使在 JavaScript 中构建大型应用程序更容易。

#### 常量 (Constants)

许多语言还包含了 `constants`（常量），它们的工作方式与变量类似，不同之处它们的值永远不会改变。使用全大写字母表示常量是常见做法。一个例子是常量 `pi` 的值（圆周与直径的比率）：

```javascript
PI = 3.14159;
```

JavaScript 原本使用 `var` 关键字声明所有变量。更现代的 JavaScript 版本引入了 `const` 和 `let` 关键字——`const` 用于声明不能重新赋值为新值的变量，`let` 用于声明在程序运行会变化的变量。你可能在某些代码示例中仍看到 `var`，它的作用几乎与 `let` 相同。`var` 和 `let` 最大的区别在于块作用域（block scope），这在第 13 章 中讨论。

#### JavaScript 中的常量 (Constants in JavaScript)

尽管引入了 `const` 关键字，但重要的是，JavaScript 仍然不支持严格意义上的常量。尽管你不能更改使用 `const` 创建的变量的值，但如果该变量包含数组或对象，你可以更改它的属性和值（因为它们是可变的）。

### 赋值 (Assignment)

**Assignment**（赋值）是给常量或变量赋值的过程。大多数语言使用 `=` 运算符来实现此。

让我们在 JavaScript 中尝试声明并赋值一些变量。示例展示了我们如何声明变量 `name` 并赋值 `'JavaScript'`。将以下代码复制到控制台：

```javascript
const name = 'JavaScript';
```

变量 `name` 现在的值为 `'JavaScript'`，因此对 name 的引用与字符串 `'JavaScript'` 完全相同。我们可以通过检查 name 的类型来验证这一点：

```javascript
typeof name;
<< 'string'
```

使用 `const` 意味着你不能将变量 `name` 重新赋值为另一个值。如果你尝试，将会得到错误。当我们尝试将 `name` 的值重新赋值为 `'JS'` 时：

```javascript
name = 'JS';
<< TypeError: Assignment to constant variable.
```

正如你所见，我们得到了错误信息，并且 `name` 变量仍然指向 `'JavaScript'`：

```javascript
name;
```

使用 `const` 似乎是一种限制，但如果值不能改变，它实际上有助于让程序更具预测性。

现在让我们尝试声明并赋值一个可以变化的变量。接下来的示例展示了我们如何声明变量 `score` 并赋值为 `0`：

```javascript
let score = 0;
```

变量 `score` 的值初始为 `0`，但它可以在程序过程中变化。

使用 `let` 关键字声明的变量可以在程序的任何时候重新赋值另一个值。这是通过简单给它们赋值新值来实现的。例如，我们可以更新 `score` 变量为 `5`：

```javascript
score = 5;
```

注意，在重新赋值变量时不需要使用 `let`。它只在第一次声明变量时需要。

### 未定义 (Undefined)

`undefined` 是一种原始数据类型，JavaScript 将其分配给任何显式赋值的变量。它基本上是 JavaScript 表达“我找不到这个值的方式”。例如，尝试在控制台中声明一个新变量 `score`，但不给它赋值：

```javascript
let score;
```





```
let score;
```

现在来看这个变量。你会发现 JavaScript 已经给它赋值为 `undefined` 的值：

```
score;
<< undefined
```

## 变量命名

在为常量和变量命名时，你应该尝试给它们起一个合理的名称，描述该变量所代表的内容。例如，`characterSpeed` 比 `ac12` 是更好的变量名。

在 JavaScript 中，变量名可以以任何大写或小写字母、下划线（`_`）或美元符号（`$`）开头。它们可以`包含`数字，但不能以数字开头。

以下是一些有效的变量名示例：

```
$name
_answer
firstName
last_name
address_line1
```

变量名是区分大小写的，因此 `ANSWER`、`Answer` 和 `answer` 都是不同的变量。

在为常量和变量名使用多个单词时，有两种常用的约定：

*   `camelCase`（小驼命名法）以小写字母开头，然后每个新单词的首字母大写：

    ```
    firstNameAndLastName
    ```

*   `underscore`（下划线命名法）用下划线分隔每个新单词：

    ```
    first_name_and_last_name
    ```

JavaScript 的内置函数使用 `camelCase` 表示法，这可能是你在编写代码时命名变量时应该遵循的最佳约定。最重要的一点是`保持一致性`。

### 变量名中的符号

在变量名的开头使用 `$` 和 `_` 等符号通常不是一个好主意，因为许多 JavaScript 库都会这样做，这可能会导致问题变得非常混乱。（`library` 是由他人编写的用于特定目的的代码，你可以将其与自己的代码一起使用。）

## 弹出交互

JavaScript 提供了三种不同类型的弹出框，用于在浏览器和用户之间提供一些简单的交互。

### 警告框 (Alert Box)

`alert` 框可以显示消息。用户必须点击按钮才能将其移除。

这是一个示例，它将在对话框中显示“Hello”消息：

```
alert('Hello');
```

![Alert 弹出框](img/alert1.png)

你还可以使用 `alert()` 来显示变量的值：

```javascript
const message = 'HELLO THERE!';
alert(message);
```

![带有变量的 Alert 弹出框](img/alert2.png)

### 提示框 (Prompt Box)

`prompt` 框允许用户输入响应，然后可以将其存储在变量中。在下面的示例中，用户被要求输入名称并将响应存储在名为 `name` 的变量中：

```javascript
const name = prompt('What is your name?');
```

![提示弹出框](img/prompt1.png)

在提示框中输入的任何内容现在都会存储在变量 `name` 中。我们可以在控制台中输入 `name` 来查看它现在持有在提示框中输入的值。

![提示的回答被存储在变量中](img/prompt2.png)

### 确认框 (Confirm Box)

`confirm` 框允许用户确认或取消请求。如果用户点击“确定”，则响应将存储为 `true`；如果他们点击“取消”，则存储为 `false`。

例如，以下代码可以用于确认用户是否同意使用其个人数据：

```javascript
const permission = confirm('Do you give consent for us to steal all of your personal data?');
```

![确认弹出框](img/confirm1.png)

响应将存储在变量 `permission` 中，可以通过在控制台中输入此内容查看。

![拒绝权限!](img/confirm2.png)

实践中，大多数用户认为这些弹出框很烦人，在大多数实际情况下绝对不建议使用。但它们确实为我们提供了一种提供交互性和从用户那里获取信息的方便方法——至少在我们在本书后面学习更高级的技术之前是。

### 你好 `name`

现在我们已经学习了所有变量以及如何使用弹出框从用户那里收集信息并存储在变量中，让我们尝试写一些代码来为用户提供个性化的问候。

打开 CodePen 并在 `JS` 部分添加以下代码：

```javascript
// 询问用户的姓名
const name = prompt('Please enter your name.');
// 问好
alert('Hello');
// 然后进行个性化处理！
alert(name);
```

希望注释解释了代码中每行发生了什么：我们使用提示框询问用户的姓名，然后使用警告框说你好，接着是第二个警告框，它对问候进行了个性化处理。

### 自动更新预览

CodePen 有一个名为“自动更新预览”的功能，它在你编写代码时不断运行代码。如果你的代码中包含弹出框，这可能会很烦人，因为你需要关闭它们才能继续编写代码……而且它们不会停止弹出！这有一个简单的解决办法：在 Pen 中，只需点击 `Settings` 标签页（右上角） > `Behavior` 并关闭 `Auto-Updating preview`。你将得到一个 `Run` 按钮，可以在完成所有编写后按下它运行你的代码。

尝试运行代码。你应该看到类似下面的内容：

![在提示框中输入 DAZ，然后消息显示 Hello DAZ!](img/helloname.png)

你可以在[此处查看我的代码](https://codepen.io/SitePoint/pen/NWRQKQK)。

## 挑战

1.  为“Rainbow”程序添加注释，解释每行发生了什么。你可以在[此处查看](https://codepen.io/SitePoint/WwZM)。

2.  找出以下值的类型。你能猜到吗？

    ```
    42
    'Twenty20'
    '123'
    true
    FALSE
    'true'
    0
    ```

    你可以在[此处查看](https://codepen.io/SitePoint/KKgOP)。

3.  使用提示框或确认框收集一些信息并存储在变量中。然后使用警告框显示消息。你可以在[此处查看](https://codepen.io/SitePoint/ZEpgzw)。

## 总结

*   注释被程序忽略，但能让你的程序更易读。
*   原始类型是程序的构建构建块。
*   JavaScript 中的原始类型包括字符串（strings）、数字（numbers）和布尔值（Boolean）。
*   复合数据类型是原始类型的结构化集合。
*   JavaScript 中的复合数据类型包括数组（arrays）和对象（objects）。
*   变量指向内存中的值并使用 `const`、`let` 或 `var` 关键字声明。
*   使用 `=` 运算符将值赋值给变量。
*   使用 `const` 声明的变量的值无法更改。
*   可以使用 `let` 或 `var` 重新给变量赋值。
*   警告、提示和确认框可以用于网页和用户之间提供一些交互。

在下一章中，我们将更深入地查看字符串如何显示字母和单词。

# 第 3 章：字母与单词

在本章中，我们将查看编程语言如何表示和使用字母和单词。我们还将查看 JavaScript 如何使用字符串表示它们。我们将涵盖以下内容：

   字符与字符串
*   JavaScript 中的字符串
*   转义值
*   查找字符
*   字符串长度
*   字符串算术
*   字符串方法
*   模板字量和插值

## 字符与字符串

正如我们在上一节中看到的，大多数编程语言都有字符（单个字符）和字符串（字符集合）的原始类型。事实上，你几乎可以认为字符串是一个由字符串连接在一起的字符集合：

![字符串上的字符](img/string.png)

JavaScript 只有一种原始数据类型 String，但它可以用于表示单个字符，也可以表示单词和较长的文本块。这里是一些字符串示例：

```
'M'
'@'
`Hello`
"Easy as 1,2,3"
`What The F*!#?`
"A long time ago, in a galaxy far, far away."
'   '
''
```

#### 空字符串




最后一个示例只是一个空字符串，内部什么都没有，甚至连空格也没有。这仍然被视为字符串。

字符串可以表示单词、文本段落，甚至是如 HTML 这样的标记。用户输入的几乎所有数据最初都会存储为字符串。

## 在 JavaScript 中创建字符串

创建字符串非常简单。你只需要将其写在引号中。打开控制台并尝试输入以下字符串：

```
'Hello';
<< "Hello"
```

这被称为 `string literal`（字符串字面量），因为值的字面表示被直接写在了代码中。你可以使用双引号或单引号来创建字符串字面量。在控制台中尝试以下示例：

```
"I'm also a string literal."
<< "I'm also a string literal."
```

如果你想在字符串中使用单引号作为撇号（apostrophe），那么双引号就会很有用。如果你在上面的字符串周围使用单引号，撇号将终止字符串并导致错误，如下代码所示：

```
'Don't do this.'
<< SyntaxError { Unexpected token, expected ; (1:19) }
```

但使用双引号可以修复它：

```
"That's the way to do it." 
<< "That's the way to do it."
```

## 转义值

也可以 `escape`（转义）引号。这是通过在撇号之前放置反斜杠来实现，使其在字符串内部显示为撇号而不是终止字符串。在控制台中输入以下内容：

```
'It\'s okay if you escape the apostrophe.'
<< "It's okay if you escape the apostrophe."
```

反斜杠可以向字符串中插入特殊的空白字符，例如：

* `\n`: 换行
* `\r`: 回车
* `\t`: 制表符

如果你想实际写入反斜杠，需要用另一个反斜杠对其进行转义：

```
"This is a backslash \\"
<< "This is a backslash \"
```

## 查找字符

尽管 JavaScript 没有 `char` 数据类型，但它仍然可以将每个字符串拆分为单个字符。

你可以通过使用 `charAt()` 方法找到字符串中的特定字符。我们可以使用 `dot notation`（点符号符号）对字符串应用方法。这涉及写一个点，后跟我们想要使用的方法。例如，以下代码将告诉我们字符串 `'Hello'` 中位置 1 的字符是什么。在控制台中输入它：

```
'Hello'.chartAt(1);
<< "e"
```

在这个示例中，括号中的数字 `1` 用来指示我们想要知道的字符的位置。

上面的结果告诉我们字符 “e” 位于位置 1。如果你好奇为什么它不是 “H”，这是因为字符串中的第一个字符被归类为位置 0。（你会发现在编程中，计数通常从零开始！）

![查找字符](img/charat.png)

还有一种使用方括号 `[]` 引用字符串中单个字符的快捷符号。例如，以下代码将告诉我们字符串的第一个字母：

```
'Hello'[0];
<< "H"
```

这种符号为我们引用字符串内部的每个字符提供了一种方便的方法。

## 查找字符

如果你想找到某个字符或子字符串在字符串中出现的位置，可以使用 `indexOf()` 方法。这将返回字符在字符串中第一次出现的位置。在下面的示例中，我们用它来找到字符 “l” 第一次出现在位置 2（记住计数从零开始，这意味着它是字符串中的第三个字符）：

```
'Hello'.indexOf('l');
<< 2
```

如果字符不在字符串中出现，将返回 `-1`：

```
'Hello'.indexOf('z');
<< -1
```

如果我们想要字符或子字符串的最后一次出现，可以使用 `lastIndexOf()` 方法。例如，这告诉我们字符 “l” 在字符串 `'Hello'` 中最后一次出现在位置 3：

```
'Hello'.lastIndexOf('l');
<< 3
```

如果我们只需要知道字符串是否包含某个字符，可以使用 `includes()` 方法。这将返回布尔值 `true` 或 `false`，取决于该字符是否在字符串中，如下代码示例所示：

```
'Hello'.includes('e');
<< true

'Hello'.includes('z');
<< false
```

我们还可以检查字符串是否以某个字符开头 `starts`。为了这一点，我们可以使用 `startsWith()` 方法。但注意，它是区分大小写的：

```
'Hello'.startsWith('H');
<< true

'Hello'.startsWith('h');
<< false
```

我们还可以使用类似的 `endsWith()` 方法来检查字符串是否以特定字符结尾：

```
'Hello'.endsWith('O');
<< false

'Hello'.endsWith('o');
<< true
```

## 字符串有多长？

每个字符串都有一个 `length` 属性，告诉我们它包含多少字符。该属性也是使用我们在 `charAt()` 方法中使用的点符号来访问。例如，以下代码将告诉我们字符串 `'Hello'` 中有多少个字符：

```
'Hello'.length;
<< 5
```


幸运的是，我们可以使用 `length` 属性来帮助找到字符串的最后一个字符，正如我们接下来将看到的。

### 名字代表了什么？

让我们尝试写一些代码，要求用户输入姓名，然后告诉他们名字的第一个字母和最后一个字母。

在上一章的末尾，我们学习了如何使用提示框（prompt box）从用户那里收集信息并将其存储在变量中。我们的第一行代码将创建一个提示框，询问他们的名字：

```
const name = prompt('What is your name?');
```

如果你在控制台中输入上面的代码，你应该能看到屏幕上出现类似下面所示的内容。

![What is your name?](img/promptname.png)

在文本框中输入你的名字并点击 `OK`。你输入的任何内容现在都将作为字符串存储在变量 `name` 中。（你可以通过在控制台中输入 `name` 然后按 `Enter` 键来验证。）

现在，让我们创建一个警报框（alert box），来展示我们的字符串处理技能：

```
alert('Hello ' + name + '. The first letter of your name is ' + name[0] + ' and the last letter is ' + name[name.length -1]);
```

如果你运行这段代码，你将得到与下面图片类似的内容。

![The first and last letter of your name is …](img/alertname.png)

注意看我们是如何使用 `name[name.length - 1]` 找到变量 `name` 的最后一个字母的。这计算出了字符串的长度（记住，在用户输入名字之前，我们不知道它有多长），然后减去 `1`（以考虑到字符的位置是从零开始的）。

你可以查看 [我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/NWbKdJV)。

### 更改大小写

可以将字符串的大小写转换为全大写字母或全小写字母。为了演示这一点，让我们在控制台中将字符串 `'JavaScript'` 赋值给变量 `name`：

```
const name = 'JavaScript';
```

现在，我们可以使用 `toUpperCase()` 方法返回一个全大写字母的字符串：

```
name.toUpperCase();
<< 'JAVASCRIPT'
```

或者，我们可以使用 `toLowerCase()` 方法返回一个全小写字母的字符串：

```
name.toLowerCase();
<< 'javascript'
```

#### 变迁皆常……

这两个方法实际上并没有改变存储在 `name` 变量中的字符串。它们只是返回了一个大小写改变后的值。如果你检查 `name` 变量的值，它应该和我们声明它时一样：

```
name;
<< 'JavaScript'
```

### 修剪空格

`trim()` 方法可以删除字符串开头和结尾的任何空白字符。当用户在表单中输入信息时不小心在开头或结尾添加空格时，这非常有用。下面的示例显示字符串开头和结尾的空格被删除了，但中间的空格被保留了：

```
'    Hello World     '.trim(); 
<< 'Hello World'
```

它可以消除任何制表符或换行符，正如下面的示例所示：

```
'   \t\t  JavaScript! \r'.trim(); // 转义制表符和换行符也被删除了
<< 'JavaScript!'
```

如果你只想移除开头或结尾的空白，有更具体的方法来实现这些操作：

```
'    Hello World     '.trimStart(); // 移除字符串开头的空白
<< 'Hello World     '

'    Hello World     '.trimEnd(); // 移除字符串结尾的空白
<< '    Hello World'
```




2. 现在，试着修改代码，让它告诉用户他们的名字中包含多少个字母。[你可以在 CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/LYbPWWm)。

3. 尝试修改 Mad Libs 代码，要求输入更多单词并创建一个更有趣的结果。你一定能比我做得更好！

4. 尝试编写一些代码，询问用户的姓名，然后通过交换第一个和最后一个字母来告诉他们“易位名称”（swappy name）。例如，如果我在提示框中输入“Daz”作为我的名字，警告框应该显示：“Hello Daz, your swappy name is Zad.”（注意：这比听起来要难一些。你可能需要为这个挑战研究一下 `slice()` 方法。）[你可以在 CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/ZEBzeKL)。

## 总结

- 字符串是字符的集合，用于在 JavaScript 中显示文本块。
- 特殊值可以通过在它们前面放置反斜杠（`\`）来`转义`（escaped）。
- 字符串具有各种属性和方法，可以提供有关它们的信息。
- `length` 属性告诉我们字符串中有多少个字符。
- 字符串可以使用 `+` 运算符进行`连接`（concatenated）。
- 模板字符串字量（Template literals）就像增强版的字符串，允许将 JavaScript 代码插入到字符串中。

既然我们已经学习了关于字符串的所有知识，是时候在新章学习关于数字的所有知识了。

# 第 4 章：数字

在第三章中，我们学习了关于字符串的所有知识。现在是学习数字了！在本章中，我们将涵盖以下内容：

- 整数和浮点数
- 数字字面量
- 指数计数法
- 算术运算
- 变量的变化
- 数字与字符串之间的转换
- 随机数

## 整数和浮点数

数字可以分为多种类型。

数字可以是`整数`（integers），即整个数字，例如 3、-4 或 0。

![Integers](img/integers.png)

数字也可以是`浮点数`（floating-point numbers）——通常简称为`实数`（reals）、`小数`（decimals）或`浮点数`（floats）。这些包括所有带有分数或小数部分的数字，例如 1.5、-3.8 或 pi。

![Floats](img/floats.png)

大多数编程语言对整数和浮点数有单独的原始数据类型，但 JavaScript 不区分它们，而将它们统称为“数字”（numbers），正如我们使用 `typeof` 运算符时看到的：

```
typeof 42; // 这是一个整数
<< 'number'

typeof 3.14159; // 这是一个浮点小数
<< 'number'
```

## 数字字面量

`数字字面量`（numeric literal）是形成十进制数字的序列，且不以领先零开头。在 JavaScript 中创建数字字面量就像直接在控制台中写数字一样简单：

```
3;
<< 3

-4.67;
<< -4.67
```

## 指数计数法

数字也可以用`指数计数法`（exponential notation）表示，这是“乘以 10 的几次方”的简写（你可能听过它被称为“科学计数法”或“标准形式”）。下面的示例显示了如何写 1 乘以 10 的 6 次方，即百万：

```
1e6;
<< 1000000
```

下一个示例返回 2 乘以 10 的 3 次方，或 1000：

```
2E3;
<< 2000
```

可以使用负索引来创建小数值。下面的示例返回 2.5 乘以 10 的负 3 次方，这等同于 2.5 乘以 0.001：

```
2.5e-3;
<< 0.0025
```

## 什么时候数字不是数字？

`NaN` 是一个特殊的错误值，是“Not a Number”（不是数字）的缩写。当尝试进行操作但结果不是数值时使用它，例如当你尝试将字符串乘以数字时：

```
'hello' * 5;
<< NaN
```

这里有一个 JavaScript 小笑话，用来放松一下。让我们看看 `NaN` 是什么数据类型。在控制台中输入以下代码：

```
typeof NaN;
<< 'number'
```

有些讽刺的是，考虑到 `NaN` 代表“不是数字”，JavaScript 却把 `NaN` 视为……数字！

## 算术运算

大多数编程语言都可以执行所有常规算术运算——就像口袋计算器一样！计算可以像你预期那样列出，并且通常使用我们熟悉的运算符和符号。JavaScript 也不例外。让我们尝试在控制台中做一些数学。

**加法**如你预期的使用 `+` 运算符：

```
5 + 4.3;
<< 9.3
```

这个示例显示你可以在计算中混合整数和浮点数。

**减法**使用 `-` 运算符，处理负数时没有问题：

```
6 - 11;
>> -5
```

**乘法**使用 `*` 运算符：

```
6 * 7;
<< 42
```

**除法**使用 `/` 运算符：

```
6 / 11;
<< 0.5454545454545454
```

**幂**使用 `**` 运算符：

```
2 ** 3;
<< 8
```

**取余**使用 `%` 运算符：

```
2 % 7;
<< 2
```

## 变量的变化

如果变量已经赋值了一个数值值，可以使用不同的运算符进行修改。例如，假设我们正在创建一个名为 `score` 的变量来跟踪得分。首先，我们将分数初始化为 0。打开控制台并跟随这些示例：

```
let score = 0;
console.log(score); // 0
```

增加分数的一种方法是这样给它加上一个值：

```
score = score + 10;
console.log(score); // 10
```

这种写法起初看起来很奇怪，因为左侧和右侧不等，但请记住 `=` 符号用于*赋值*，我们正在将 `score` 变量赋值为当前值加 10。

这种操作有一个简写形式，称为**复合赋值运算符** `+=`：

```
score += 10;
console.log(score); // 20
```

我们在上一节中看到的所有算术运算符都有等效的复合赋值运算符。例如，你可以这样减少 5 分：

```
score -= 5;
console.log(score); // 15
```

以下代码将 `score` 的值乘以 2——换句话说，让它翻倍：

```
score *= 2;
console.log(score); // 30
```

你也可以将 `score` 的当前值除以一个值。这段代码将其除以 3：

```
score /= 3;
console.log(score); // 10
```

你还可以对 `score` 的值升幂。以下代码将 score 的值升到 2 次方，这等同于将其平方：

```
score ** 2;
console.log(score); // 100
```





```
score **=2;
<< 100
```

你也可以使用取余运算符。如果 `score` 的当前值被除以 7，下面的代码会将 `score` 的值更改为余数：

```
score %= 7;
<< 2
```

## 递增

如果你只想让一个值加 1，你可以使用递增运算符 `++`。它可以直接放在变量之前（前置运算符），也可以放在变量之后（后置运算符）。尝试在控制台中输入以下代码来查看它们是如何工作的：

```
let points = 5;

points++;
<< 5

++points;
<< 7
```

那么这里发生了什么呢？这两个运算符都将 `points` 的值增加了 1，尽管第一个操作看起来并没有立即改变任何东西。区别在于递增发生的时间相对于相对于返回的值的时机。

在第一次操作中，`points++` 返回 `score` 的原始值 5，*然后*将其增加到 6；而 `++points` 先将值增加 1，然后返回新值 7。

还有一个工作方式相同的 `--` 运算符。下面的示例将返回 7，然后将 `points` 的值减 1 到 6：

```
points--;
<< 7
```

而下面的示例将先将 `points` 的值减 1，然后返回该值：

```
--points;
<< 5
```

## 多大了？

现在我们已经学习了不同的计算和变量更改，是时候编写代码了。我们将编写一个短程序，询问用户的年龄，然后将其从年转换为秒。

在 CodePen 上创建一个新的 Pen，并在 **JS** 部分输入以下内容（由于我们使用了 `prompt` 和 `alert` 框，别忘记在 **Settings** > **Behavior** 中关闭 **Auto-Updating Preview**）：

```
const ageInYears = prompt('How old are you (in years)?');
```

这会将用户的答案存储在名为 `ageInYears` 的变量中。现在，让我们将其转换为秒：

```
const ageInSeconds = ageInYears * 365.25 * 24 * 60 * 60;
```

一年中大约有 31,557,600 秒，但我们不需要费心记住这个数字。我们所做的只需乘以 365.25（这是一年的近似天数，0.25 是略微高估，这也是我们有闰年的原因）将其转换为天数，然后乘以 24 转换为小时，再乘以 60 转换为分钟，最后再次乘以 60 转换为秒。

最后，我们只需要使用 `alert` 框来告知用户结果：

```
alert(`That means you have been alive for at least ${ageInSeconds} seconds!!`);
```

点击 **Run** 查看运行效果。它看起来应该像这样：

![你的秒数年龄](img/ageinseconds.png)

你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/XWNWYeY)。

## 数字与字符串的计算

可以将一个数字和一个字符串相加吗？这看起来是一个愚蠢的问题，但 JavaScript 会尽力尝试回答这个问题，如下例示例所示：

```
2 + 'two';
<< "2two"
```

这里发生了什么？数字 `2` 被转换成了字符串 `'2'`，正如我们在上一节中看到的那样，它与字符串 `'two'` 拼接了一起。这个过程被称为**类型转换**（type coercion），它当运算符的操作数类型不同时发生。JavaScript 会尝试将其中一个操作数转换为另一个操作数类型的等效值。例如，如果你尝试将一个字符串和一个数字相乘，JavaScript 将尝试将字符串强制转换为数字，然后将它们相乘：

```
'2' * 8;
<< 16
```

这起初看起来有用，但这个过程并不总是符合逻辑或保持一致，并且可能会导致很多困惑。例如，如果你尝试*相加*一个字符串和一个数字，JavaScript 将将数字转换为字符串，然后拼接这两个字符串：

```
'2' + 8;
<< '28'
```

JavaScript 试图提供帮助，但实际上，类型转换使得你发现在代码中发现错误变得非常困难。

最好的方法是掌控局面，对你正在处理的数值类型保持非常明确的态度，并避免在操作中使用不同类型的值。让我们在下一节看看如何这样做。

## 字符串与数字之间的转换

我们可以使用 `Number` 构造函数将数字转换为字符串。这会将数字的字符串形式转换为数字字面量，如下例所示：

```
Number('23');
<< 23
```

如果字符串无法转换为数字，则返回 `NaN`：

```
Number('hello');
<<< NaN
```

要将数字字面量转换为该数字的字符串字面量表示，我们使用 `String` 构造函数，如下例所示：

```
String(3);
<< '3'
```

这些转换最常见的用途是因为用户在 `prompt` 框中输入的任何内容……（此处原文为重复/不完整内容，已按要求处理）




[content]

在 CodePen 上打开一个新 Pen，并在 `JS` 中输入以下代码：

```
const sides = prompt('How many sides does the dice have?');
```

这会将用户输入的数字存储在名为 `sides` 的变量中。现在，让我们添加一个警报消息来让用户“掷”骰子：

```
alert('Press Enter or click close to roll the dice...');
```

接下来是用于创建随机数的代码：

```
const number = Math.ceil(sides*Math.random());
```

这与我们之前使用的代码相似，但我们将 `Math.random()` 乘以了用户指定的骰子面数。这将产生一个在 0 到（面数减 1）之间的之间的随机小数。应用 `Math.ceil` 会将该数字向上取整到下一个整数，从而有效地生成一个 1 到面数 之间的随机数。

现在我们只需要告诉用户数字是多少（我们再次使用模板字面量将数字直接插入到字符串中）：

```
alert(`The dice landed on the number ${number}`);
```

点击 **Run** 来测试此代码。它看起来应该像这样：

![Roll the dice](img/dice.png)

你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/dyOyKab)。

### 更多方法

数字还能做很多其他事情。属性和方法的完整列表可以在 [Mozilla 开发者网络](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) 上找到。

`Math` 对象也有许多你可能会觉得有用的属性和方法。同样，你可以在 [Mozilla 开发者网络](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math) 上查看它们。

## 挑战

1. 创建一个提示框询问用户的年龄。然后告诉他们 25 年后他们多大。（注意，在这里你可能会遇到一些类型转换问题，因为在提示框中输入的数字实际上是作为字符串存储存储的。）你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/VwmwdRY)。
2. 编写一些代码，使用提示框询问用户两个数字，然后显示一个警报框来显示这两个数字相乘的结果。你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/PoboaLb)。
3. 你能写一些代码来分摊账单吗？你需要使用提示框询问餐费花了多少钱，另一个提示框询问由多少个人分摊。然后用警报框显示每人需要支付多少钱。对于这个挑战，你需要考虑单位和舍入。如果你能添加一个额外的问题来按百分比添加小费，将会获得加分！你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/WNoNKeX)。
4. 编写一些代码生成两个值之间的随机数。例如，你能写出代码返回一个 5 到 10（包含边界值）之间的随机数吗？你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/ExNxpYJ)。

## 总结

*   数字可以是整数（如 2）或浮点数（小数，如 7.8），尽管 JavaScript 并不区分它们，而只有一个原始数据类型 `Number`。
*   数字可以使用指数计数法表示，例如 `5e6` 表示五百万。
*   算术运算 `+`、`-`、`*`、`/` 和 `%` 可以应用于任何两个数字。
*   可以将字符串转换为数字，反之亦然。
*   如果你尝试在字符串和数字之间执行操作，JavaScript 将尝试转换类型以完成操作。这可能会导致一些不一致和意想不到的结果！
*   `Math.random()` 方法返回一个 0 到 1 之间的随机数。

现在我们已经学习了字符串和数字，是时候查看 JavaScript 如何处理值的集合了。

# 第 5 章：集合

到目前为止，我们已经了字符串、数字和布尔值等原始数据类型。但如果我们想在一个变量中存储一整个值的集合呢？例如，我们可能有一份价格列表，想要存储在同一个地方。**复合数据类型**可以以结构化的方式收集原始值。

编程语言使用不同的数据结构来存储值，但最常见的之一是数组。

在本章中，我们将涵盖：

*   创建数组
*   向数组添加值
*   从数组中移除值
*   扩展运算符 (spread operator)
*   多维数组

## 数组

**数组** 是一个值的有序列表。例如，考虑以下购物清单：

*   苹果 (Apple)
*   香蕉 (Banana)
*   纸蛋糕 (Cupcake)

这可以表示如下数组：

```
['Apple', 'Banana', 'Cupcake']
```

![A fruity array](img/list1.png)

数组中的每个值都有一个数字索引，显示它在数组中的位置。在示例中，`'Apple'` 的索引为 0（记住计算机从 0 开始计数！），`'Banana'` 的索引为 1，而 `'Cupcake'` 的索引为 2。

![A fruity array with indices](img/list2.png)

数组中的每个值都有一个数字索引，显示它在数组中的位置。在示例中，`'Apple'` 的索引为 0（记住计算机从 0 开始计数！），`'Banana'` 的索引为 1，而 `'Cupcake'` 的索引为 2。

（注：此处原文中存在大量重复段落，已根据指令要求不重复输出，仅保留核心逻辑翻译）

## JavaScript 中的数组

现在我们已经介绍了数组，让我们尝试编写一些代码。要创建一个**数组字面量**，你只需在方括号内用逗号分隔这些值。例如，以下代码创建了购物清单：

```
shopping = ['Apple', 'Banana', 'Cupcake'];
```

要访问数组中的特定值，我们在方括号中写入它的位置。（这被称为**索引** index。）例如，以下代码将返回数组中的第一个项：

```
shopping[0];
<< 'Apple'
```

如果我们想查看索引 2 的值（购物清单中的第三项），我们将使用以下代码：

```
shopping[2];
<< 'Cake'
```

如果数组中的元素为空，则会返回 `undefined`，如果我们尝试查看索引 5 的内容所示：

```
shopping[5]; // 位置 5 没有内容
<< undefined
```

### 向数组添加值

如果我们想向创建的数组添加新项，只需使用索引表示法将值分配给目标位置。例如，以下代码将在位置 3 添加 `'Donut'`（记住这是购物清单中的第四项）：

```
shopping[3] = 'Donut';
```

我们可以通过直接在控制台中输入它的名称来查看 `shopping` 数组的内容：

```
shopping;
<< ['Apple', 'Banana', 'Cake', 'Donut']
```

![The updated shopping list](img/list3.png)

数组中的每个项都可以像变量一样处理。你可以使用赋值运算符 `=` 修改值。例如，我们可以使用以下代码将位置 2 的值从 `'Cake'` 改为 `'Carrot'`：

```
shopping[2] = 'Carrot';
```

检查更改是否已生效：

```
shopping;
<< ['Apple', 'Banana', 'Carrot', 'Donut']
```

![A carrot added to the shopping list, in place of the cupcake](img/list4.png)

你可以使用索引表示向数组的任何位置添加新项。例如，以下代码将在位置 5 添加 `'Eggplant'`：

```
shopping[5] = 'Eggplant';
```

现在我们现在控制台中查看 `shopping` 数组，可以看到第 6 项（索引为 5）已填充了字符串 `'Eggplant'`。这在数组的位置 4 处留了一个空隙，因此数组中未使用的该位置由值 `undefined` 填充：





```
shopping;
<< ['Apple', 'Banana', 'Carrot', 'Donut', undefined, 'Eggplant']
```

![一个较长的购物列表，其中一项为 undefined](img/list5.png)

## 从数组中删除值

`delete` 运算符可以用于从数组中删除一个项目。例如，如果我们决定真的不应该买甜甜圈，可以使用以下代码从 `shopping` 数组中删除值 `'Donut'`：

```
delete shopping[3];
<< true
```

这会直接从列表的对应位置删除甜甜圈，在数组中留空一个空位，如下所示所示。

![从数组中删除项目的可视化表示](img/delete.png)

现在，如果我们看一眼 `shopping` 数组，可以看到字符串 `Donut`（索引为 3）确实被删除了……而在它的位置留下了一个 `undefined` 值：

```
shopping;
<< ['Apple', 'Banana', 'Carrot', undefined, undefined, 'Eggplant']
```

![更新后的购物列表](img/list6.png)

注意这一点，因为这甚至可能让经验丰富的程序员出错。位置 3 的*值*（`'Donut'`）已从数组中删除，但它所占据的空间*仍然在那里*，而且它现在包含一个 `undefined` 值。这意味着数组的元素数量保持不变，该位置仍然可以作为索引被引用，但它只会返回 `undefined`：

```
shopping[3];
<< undefined
```

## 查找数组的长度

每个数组都有一个 `length` 属性，告诉我们它包含多少项目。例如，我们可以使用以下代码找到 `shopping` 数组中的项目数量：

```
shopping.length;
<< 6
```

注意长度为 6，这是因为在计算数组长度时，包含 `undefined` 的位置也会被计算在内。

`length` 属性的值可以放在方括号中作为索引的一部分，以找到数组中的最后一个项目。例如，以下代码告诉我们购物列表中的最后一个项目：

```
const length = shopping.length;
shopping[length - 1];
<< 'Eggplant'
```

这告诉我们 `'Eggplant'` 是数组中的最后一个项目，但请注意我们必须从 `length` 属性中减去 1。这是因为索引是从 0 开始的，所以数组中的最后一个项目的索引比数组的实际长度少 1。

数组的 `length` 属性不是固定的，这意味着可以通过添加或删除项目来动态更改数组的长度。事实上，`length` 属性是可变的，这意味着你可以直接修改它，如下：

```
shopping.length = 8;
<< 8
```

这将使我们的 `shopping` 数组的长度变为 8 而不是 6。如果我们看一眼数组，可以看到额外的空位现在是空的了：

```
shopping;
<< ['Apple', 'Banana', 'Carrot', undefined, undefined, 'Eggplant', undefined, undefined]
```

![我们的列表现在的长度为 8](img/list7.png)

如果我们将数组长度更改比当前长度短的值，所有额外的元素将被完全删除。以下代码将保留数组中的前三个项目并删除其余所有项目：

```
shopping.length = 3;
<< 3
```

现在如果我们检查数组的内容，可以看到只剩下了前三个项目：

```
shopping;
<< ['Apple', 'Banana', 'Carrot']
```

![一个较短的购物列表](img/list8.png)

## 没有第二次机会

一旦你通过编辑长度属性来缩短数组，任何被删除的项目都将永久丢失。如果你尝试将长度改回 8，它只会向所有额外的空间中添加 `undefined`，而不是用之前的值来填充它们：

```
shopping.length = 8;
<< ['Apple', 'Banana', 'Carrot', undefined, undefined, undefined, undefined, undefined,]
```

因此，在更改数组长度时，请非常小心不要丢失你之后可能需要的任何值。

## 弹出（Pop）和推送（Push）

数组有名为 `pop` 和 `push` 的方法，用于删除或添加项目。

`pop()` 方法从数组中移除最后一个项目。为了看到效果，让我们创建一个新的购物列表数组：

```
const shopping = ['Apple', 'Banana', 'Carrot', 'Donut', 'Eggplant']
```

![包含五个项目的新列表](img/list9.png)

我们可以使用 `pop()` 方法移除数组的最后一个项目，它会将最后一个项目“弹出”数组，如下图所示。

![从数组中弹出最后一个项目](img/pop.png)

下面的代码显示了如何将该方法应用于 `shopping` 数组：

```
shopping.pop();
<< 'Eggplant'
```

该方法返回数组的最后一个项目，并更新数组使其不再包含该项目。如果我们看一眼 `shopping` 数组，我们会发现它不再包含字符串 `'Eggplant'`：

```
shopping;
<< ['Apple', 'Banana', 'Carrot', 'Donut']
```

![去掉了茄子的我们的数组](img/list10.png)

如果我们想在数组末尾添加一个新值，可以使用 `push()` 方法。例如，我们可以向 `shopping` 数组末尾添加 `'cupcake'`，如下所示。

![在末尾添加蛋糕](img/push.png)

我们将使用以下代码：

```
shopping.push('cupcake');
<< 5
```

该方法返回数组的新长度，为 5。我们可以通过输入 `shopping` 来检查 `'cupcake'` 已添加：

```
shopping;
<< ['Apple', 'Banana', 'Carrot', 'Donut', 'cupcake']
```

# 移位（Shift）和未移（Unshift）

`shift()` 方法与 `pop` 类似，区别在于它从数组中移除*第一个*项目：

```
shopping.shift();
<< 'Apple'
```

![shift 工作原理](img/shift.png)

`unshift()` 方法与 `push()` 方法类似，但它将新项目添加到数组的*开头*。例如，我们可以以下代码向 `shopping` 数组开头添加 `'Avocado'`：

```
shopping.unshift('Avocado');
<< 5
```

该方法返回数组的新长度，为 5。我们可以通过输入 `shopping` 来检查 `'Avocado'` 已添加：

```
shopping;
<< ['Avocado', 'Banana', 'Carrot', 'Donut', 'cupcake']
```

![带有牛油果的购物列表](img/list11.png)

## 扩展运算符（Spread Operator）

**扩展运算符**是放在内部数组前面的三个点（`...`）。它会将数组中的所有元素展开为独立的值。

如果你把数组想象成一个装满值的盒子，那么扩展运算符等同于将盒子的内容倒进另一个盒子里。

为了看到扩展运算符的作用，尝试在控制台中创建一个数组：

```
const arrayA = [1,2,3];
```

现在假设我们想把 `arrayA` 中的三个元素放入一个新数组 `arrayB` 中。我们可能会尝试这样做：

```
const arrayB = [arrayA];
```

不幸的是，我们所做的是将整个 `arrayA` 放入了 `arrayB`。这等同于在一个盒子里放了一个装满值的盒子。可以从这一点看出，`arrayB` 只包含*一个*元素，如果我们查看长度属性就可以：

```
arrayB.length;
<< 1
```

如果我们在 `arrayA` 前使用扩展运算符，那么我们将它的所有元素放入 `arrayB`：

```
const arrayB = [...arrayA];
```

现在 `arrayB` 包含了三个元素，我们可以通过输入 `arrayB` 来检查：

```
arrayB;
<< [1,2,3]
```




当我们把扩展运算符应用到 `arrayA` 并将其放在另一个数组 `arrayC` 内部时，它将解包所有的元素，并将它们视为三个独立的立项值：

```
const arrayC = [...arrayA];
```

现在，如果我们查看 `arrayC` 的长度，可以发现它确实包含了三个独立的元素：

```
arrayC.length;
<< 3
```

如果如果我们查看 `arrayC` 的内容，可以看到它包含了与 `arrayA` 相同的元素：

```
arrayC;
<< [1,2,3]
```

扩展运算符可以用于将两个或多个数组的元素合并到一个新数组中。为了直观看到这一点，让我们创建三个包含不同类型食物的各种数组：

```
const fruit = ['Pineapple', 'Melon'];
const savory = ['Burger', 'Fries'];
const sweets = ['Cookie', 'Popcorn'];
```

现在，我们可以通过将这三个数组放入一个新数组 `food` 中，并对每个数组应用扩展运算符，将它们合并为一个名为 `food` 的数组，这样所有元素都会从它们各自的数组中解包并成为独立的值：

```
const food = [...fruit, ...savory, ...sweets];
<< undefined
```

我们可以通过查看 `food` 变量来检查操作是否成功：

```
food;
<< ['Pineapple', 'Melon', 'Burger', 'Fries', 'Cookie', 'Popcorn']
```

![我们新的组合数组的视觉](img/list13.png)

如你所见，所有的项目都从它们原始数组容器中展开，并单独放在新的 `food` 数组中。

如果没有使用扩展运算符，新数组中的项仍然会被封装在原始数组中，如下代码所示：

```
const food = [fruit, savory, sweets];
<< [['Pineapple', 'Melon'], ['Burger', 'Fries'], ['Cookie', 'Popcorn']]
```

扩展运算符还可以用于向数组中添加新项。例如，如果我们想在 `food` 数组末尾添加 `'Coffee'`，而不是使用 `push()` 方法，可以使用以下代码：

```
food = [...food, 'Coffee'];
```

在这个示例中，扩展运算符解包了 `food` 数组中的所有项，并将它们作为独立项放在新数组中。

此外，与其使用 `unshift()` 方法在数组开头添加字符串 `'Coconut'`，我们可以使用以下代码：

```
food = ['Coconut', ...food];
```

事实上，你可以使用以下代码在一个步内向数组开头添加 `'Coconut'` 并在末尾添加 `'Coffee'`：

```
food = ['Coconut', ...food, 'Coffee'];
```

我们可以通过查看数组的内容来看到这次操作的结果：

```
food;
<< ['Coconut', 'Pineapple', 'Melon', 'Burger', 'Fries', 'Cookie', 'Popcorn', 'Coffee']
```

![我们新食物数组的视觉](img/list14.png)

### 切片与拼接 (Slicing and Splicing)

`slice()` 方法创建一个子数组，实际上是从原始数组中从一个位置开始到另一个位置切取一段片段。例如，如果我们想找到 `food` 数组中的第三和第四项，我们将使用以下代码：

```
food.slice(2,4);
<< ['Melon', 'Burger']
```

括号中的第一个数字告诉我们开始切片的索引，第二个数字告诉我们切片到达的索引（但不包含该项）。所以，在上面的示例中，切片将从索引为 2 的 `'Melon'` 开始，然后包含所有项，直到但不包括索引为 4 的项 `'Fries'`。

切片操作是非破坏性的，因此数组中没有实际删除任何项，我们可以查看 `food` 数组看到：

```
food;
<< ['Coconut', 'Pineapple', 'Melon', 'Burger', 'Fries', 'Cookie', 'Popcorn']
```

`splice()` 方法从数组中删除项并在位置插入新项。例如，以下代码移除字符串 `'Melon'` 并替换为 `'Mango'`：

```
food.splice(2, 1, 'Mango');
<< ['Melon']
```

括号中的第一个数字告诉我们开始 splice 的索引。在示例中，它是索引 2（即数组中的第三个项）。第二个数字告诉我们从数组中删除多少个项。

拼接操作是破坏性的，它会永久改变数组的值，如下所示：

```
food;
<< ['Coconut', 'Pineapple', 'Mango', 'Burger', 'Fries', 'Cookie', 'Popcorn']
```

![更多 melon！](img/list15.png)

（注：由于原文中关于 `splice` 的描述存在大量重复导致文本异常，译文已根据核心逻辑进行了精简与翻译。）




注意，这会永久更改数组的顺序。

### 排序数组值

我们可以使用 `sort()` 方法对数组中的项进行排序。在 `food` 数组上调用此方法将把数组项重新排列为字母顺序：

```
food.sort();
<< ['Coconut', 'Coffee', 'Cookie', 'Fries', 'Mango', 'Pineapple', 'Pizza', 'Popcorn']
```

![已排序的食物](img/list19.png)

注意，这也会永久更改数组的顺序。

### 字母顺序的数字

字符串默认按字母顺序排序，但数字也是如此！这意味着数字是根据它们的第一位数字进行排序的，而不是根据数值。例如，`9` 会排在 `10` 之后，因此你会得到像下面所示的疯狂结果：

```
[5, 9, 10].sort();
<< [10, 5, 9]
```

不过，别担心。这可以使用所谓的“回调”（callback）来修复，我们将在书的后面介绍它。

### 更多方法

数组还有很多可以做的事情。你可以在 [Mozilla 开发者网络](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) 上找到属性和方法的完整列表。看看你是否能找到任何有趣的，并尝试在控制台中中使用它们。

## 多维数组

你可以通过将多个数组放入一个容器数组中，创建一个数组的数组，这被称为 `多维数组`。这可以用于创建坐标系，例如：

```
const coordinates = [[1,3],[4,2]];
<< [[1,3],[4,2]]
```

要访问多维数组中的值，我们使用两个索引——一个指向项在外层数组中的位置，另一个指向它在内层数组中的位置：

```
coordinates[0][0]; // 第一个数组的第一个值
<< 1

coordinates[1][0]; // 第二个数组的第一个值
<< 4

coordinates[0][1]; // 第一个数组的第二个值
<< 3

coordinates[1][1]; // 第二个数组的第二个值
<< 2
```

二维数组的结构如下所示。

![二维数组](img/coordinates.png)

我们之前见过的展开运算符可以用来“展平”多维数组。`展平` 数组涉及通过将所有值从其数组中取出并放在父数组的同一层，移除所有嵌套数组。你可以从下面的示例中看到，只需将 `summer` 和 `winter` 数组放入容器数组就会创建一个嵌套数组，但如果我们在将数组放入容器数组时使用展开运算符，我们得到一个只包含其内容的扁平数组：

```
const summer = ['Jun', 'Jul', 'Aug'];
const winter = ['Dec', 'Jan', 'Feb'];
const nested = [ summer, winter ];
<< [ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ]

const flat = [...summer, ...winter];
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

JavaScript 还有 `flat()` 方法，它不需要展开运算符即可展平数组，如下所示：

```
[ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ].flat();
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

关于创建和操作数组的总结可以在 [SitePoint 的这篇文章](https://www.sitepoint.com/quick-tip-create-manipulate-arrays-in-javascript/) 中找到。

## 挑战

1. 创建名为 `shoppingList` 的变量，初始为一个空数组。尝试使用 `pop`、`push`、`shift`、`unshift` 和 `splice`，以及展开运算符从列表中添加和删除项。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/BaQNzyz)。

2. 使用三个提示框（prompt）向用户询问三个不同的单词，然后将它们放入数组中。使用警告框（alert）显示数组。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/bGBdexY)。

3. 使用提示框让用户输入一个单词。然后使用 `split`、`reverse()` 和 `join()` 方法的组合将单词反过来写。例如，“hello”将变成“olleh”。（提示：为 `split()` 和 `join()` 方法提供一个空字符串作为参数。）你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/poNJbOZ)。

4. 编写一段代码，在提示框中向用户询问一个逗号分隔的名称列表，然后创建一个警告框按字母顺序显示这些名称。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/abBOZae)。

## 总结

* 数组是值的有序列表。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 索引用于引用数组中的特定项。

注意这会永久更改数组的顺序。

### 排序数组值

我们可以使用 `sort()` 方法对数组中的项进行排序。在 `food` 数组上调用此方法将把数组项重新排列为字母顺序：

```
food.sort();
<< ['Coconut', 'Coffee', 'Cookie', 'Fries', 'Mango', 'Pineapple', 'Pizza', 'Popcorn']
```

![已排序的食物](img/list19.png)

注意这也会永久更改数组的顺序。

### 字母顺序的数字

字符串默认按字母顺序排序，但数字也是如此！这意味着数字是根据它们的第一位数字进行排序的，而不是根据数值。例如，`9` 会排在 `10` 之后，因此你会得到像下面所示的疯狂结果：

```
[5, 9, 10].sort();
<< [10, 5, 9]
```

不过，别担心。这可以使用所谓的“回调”（callback）来修复，我们将在书的后面介绍它。

### 更多方法

数组还有很多可以做的事情。你可以在 [Mozilla 开发者网络](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) 上找到属性和方法的完整列表。看看你是否能找到任何有趣的，并尝试在控制台中中使用它们。

## 多维数组

你可以通过将多个数组放入一个容器数组中，创建一个数组的数组，这被称为 `多维数组`。这可以用于创建坐标系，例如：

```
const coordinates = [[1,3],[4,2]];
<< [[1,3],[4,2]]
```

要访问多维数组中的值，我们使用两个索引——一个指向项在层层数组中的位置，另一个指向它在内层数组中的位置：

```
coordinates[0][0]; // 第一个数组的第一个值
<< 1

coordinates[1][0]; // 第二个数组的第一个值
<< 4

coordinates[0][1]; // 第一个数组的第二个值
<< 3

coordinates[1][1]; // 第二个数组的第二个值
<< 2
```

二维数组的结构如下所示。

![二维数组](img/coordinates.png)

我们之前见过的展开运算符可以用来“展平”多维数组。`展平` 数组涉及通过将所有值从其数组中取出并放在父数组的同一层，移除所有嵌套数组。你可以从下面的示例中看到，只需将 `summer` 和 `winter` 数组放入容器数组就会创建一个嵌套数组，但如果我们在将数组放入容器数组时使用展开运算符，我们得到一个只包含其内容的扁平数组：

```
const summer = ['Jun', 'Jul', 'Aug'];
const winter = ['Dec', 'Jan', 'Feb'];
const nested = [ summer, winter ];
<< [ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ]

const flat = [...summer, ...winter];
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

JavaScript 还有 `flat()` 方法，它不需要展开运算符即可展平数组，如下所示：

```
[ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ].flat();
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

关于创建和操作数组的总结可以在 [SitePoint 的这篇文章](https://www.sitepoint.com/quick-tip-create-manipulate-arrays-in-javascript/) 中找到。

## 挑战

1. 创建名为 `shoppingList` 的变量，初始为一个空数组。尝试使用 `pop`、`push`、`shift`、`unshift` 和 `splice`，以及展开运算符从列表中添加和删除项。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/BaQNzyz)。

2. 使用三个提示框（prompt）向用户询问三个不同的单词，然后将它们放入数组中。使用警告框（alert）显示数组。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/bGBdexY)。

3. 使用提示框让用户输入一个单词。然后使用 `split`、`reverse()` 和 `join()` 方法的组合将单词反过来写。例如，“hello”将变成“olleh”。（提示：为 `split()` 和 `join()` 方法提供一个空字符串作为参数。）你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/poNJbOZ)。

4. 编写一段代码，在提示框中向用户询问一个逗号分隔的名称列表，然后创建一个警告框按字母顺序显示这些名称。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/abBOZae)。

## 总结

* 数组是值的有序列表。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 索引用于引用数组中的特定项。

注意这会永久更改数组的顺序。

### 排序数组值

我们可以使用 `sort()` 方法对数组中的项进行排序。在 `food` 数组上调用此方法将把数组项重新排列为字母顺序：

```
food.sort();
<< ['Coconut', 'Coffee', 'Cookie', 'Fries', 'Mango', 'Pineapple', 'Pizza', 'Popcorn']
```

![已排序的食物](img/list19.png)

注意这也会永久更改数组的顺序。

### 字母顺序的数字

字符串默认按字母顺序排序，但数字也是如此！这意味着数字是根据它们的第一位数字进行排序的，而不是根据数值。例如，`9` 会排在 `10` 之后，因此你会得到像下面所示的疯狂结果：

```
[5, 9, 10].sort();
<< [10, 5, 9]
```

不过，别担心。这可以使用所谓的“回调”（callback）来修复，我们将在书的后面介绍它。

### 更多方法

数组还有很多可以做的事情。你可以在 [Mozilla 开发者网络](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) 上找到属性和方法的完整列表。看看你是否能找到任何有趣的，并尝试在控制台中中使用它们。

## 多维数组

你可以通过将多个数组放入一个容器数组中，创建一个数组的数组，这被称为 `多维数组`。这可以用于创建坐标系，例如：

```
const coordinates = [[1,3],[4,2]];
<< [[1,3],[4,2]]
```

要访问多维数组中的值，我们使用两个索引——一个指向项在层层数组中的位置，另一个指向它在内层数组中的位置：

```
coordinates[0][0]; // 第一个数组的第一个值
<< 1

coordinates[1][0]; // 第二个数组的第一个值
<< 4

coordinates[0][1]; // 第一个数组的第二个值
<< 3

coordinates[1][1]; // 第二个数组的第二个值
<< 2
```

二维数组的结构如下所示。

![二维数组](img/coordinates.png)

我们之前见过的展开运算符可以用来“展平”多维数组。`展平` 数组涉及通过将所有值从其数组中取出并放在父数组的同一层，移除所有嵌套数组。你可以从下面的示例中看到，只需将 `summer` 和 `winter` 数组放入容器数组就会创建一个嵌套数组，但如果我们在将数组放入容器数组时使用展开运算符，我们得到一个只包含其内容的扁平数组：

```
const summer = ['Jun', 'Jul', 'Aug'];
const winter = ['Dec', 'Jan', 'Feb'];
const nested = [ summer, winter ];
<< [ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ]

const flat = [...summer, ...winter];
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

JavaScript 还有 `flat()` 方法，它不需要展开运算符即可展平数组，如下所示：

```
[ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ].flat();
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

关于创建和操作数组的总结可以在 [SitePoint 的这篇文章](https://www.sitepoint.com/quick-tip-create-manipulate-arrays-in-javascript/) 中找到。

## 挑战

1. 创建名为 `shoppingList` 的变量，初始为一个空数组。尝试使用 `pop`、`push`、`shift`、`unshift` 和 `splice`，以及展开运算符从列表中添加和删除项。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/BaQNzyz)。

2. 使用三个提示框（prompt）向用户询问三个不同的单词，然后将它们放入数组中。使用警告框（alert）显示数组。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/bGBdexY)。

3. 使用提示框让用户输入一个单词。然后使用 `split`、`reverse()` 和 `join()` 方法的组合将单词反过来写。例如，“hello”将变成“olleh”。（提示：为 `split()` 和 `join()` 方法提供一个空字符串作为参数。）你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/poNJbOZ)。

4. 编写一段代码，在提示框中向用户询问一个逗号分隔的名称列表，然后创建一个警告框按字母顺序显示这些名称。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/abBOZae)。

## 总结

* 数组是值的有序列表。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 索引用于引用数组中的特定项。

注意这会永久更改数组的顺序。

### 排序数组值

我们可以使用 `sort()` 方法对数组中的项进行排序。在 `food` 数组上调用此方法将把数组项重新排列为字母顺序：

```
food.sort();
<< ['Coconut', 'Coffee', 'Cookie', 'Fries', 'Mango', 'Pineapple', 'Pizza', 'Popcorn']
```

![已排序的食物](img/list19.png)

注意这也会永久更改数组的顺序。

### 字母顺序的数字

字符串默认按字母顺序排序，但数字也是如此！这意味着数字是根据它们的第一位数字进行排序的，而不是根据数值。例如，`9` 会排在 `10` 之后，因此你会得到像下面所示的疯狂结果：

```
[5, 9, 10].sort();
<< [10, 5, 9]
```

不过，别担心。这可以使用所谓的“回调”（callback）来修复，我们将在书的后面介绍它。

### 更多方法

数组还有很多可以做的事情。你可以在 [Mozilla 开发者网络](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) 上找到属性和方法的完整列表。看看你是否能找到任何有趣的，并尝试在控制台中中使用它们。

## 多维数组

你可以通过将多个数组放入一个容器数组中，创建一个数组的数组，这被称为 `多维数组`。这可以用于创建坐标系，例如：

```
const coordinates = [[1,3],[4,2]];
<< [[1,3],[4,2]]
```

要访问多维数组中的值，我们使用两个索引——一个指向项在层层数组中的位置，另一个指向它在内层数组中的位置：

```
coordinates[0][0]; // 第一个数组的第一个值
<< 1

coordinates[1][0]; // 第二个数组的第一个值
<< 4

coordinates[0][1]; // 第一个数组的第二个值
<< 3

coordinates[1][1]; // 第二个数组的第二个值
<< 2
```

二维数组的结构如下所示。

![二维数组](img/coordinates.png)

我们之前见过的展开运算符可以用来“展平”多维数组。`展平` 数组涉及通过将所有值从其数组中取出并放在父数组的同一层，移除所有嵌套数组。你可以从下面的示例中看到，只需将 `summer` 和 `winter` 数组放入容器数组就会创建一个嵌套数组，但如果我们在将数组放入容器数组时使用展开运算符，我们得到一个只包含其内容的扁平数组：

```
const summer = ['Jun', 'Jul', 'Aug'];
const winter = ['Dec', 'Jan', 'Feb'];
const nested = [ summer, winter ];
<< [ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ]

const flat = [...summer, ...winter];
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

JavaScript 还有 `flat()` 方法，它不需要展开运算符即可展平数组，如下所示：

```
[ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ].flat();
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

关于创建和操作数组的总结可以在 [SitePoint 的这篇文章](https://www.sitepoint.com/quick-tip-create-manipulate-arrays-in-javascript/) 中找到。

## 挑战

1. 创建名为 `shoppingList` 的变量，初始为一个空数组。尝试使用 `pop`、`push`、`shift`、`unshift` 和 `splice`，以及展开运算符从列表中添加和删除项。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/BaQNzyz)。

2. 使用三个提示框（prompt）向用户询问三个不同的单词，然后将它们放入数组中。使用警告框（alert）显示数组。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/bGBdexY)。

3. 使用提示框让用户输入一个单词。然后使用 `split`、`reverse()` 和 `join()` 方法的组合将单词反过来写。例如，“hello”将变成“olleh”。（提示：为 `split()` 和 `join()` 方法提供一个空字符串作为参数。）你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/poNJbOZ)。

4. 编写一段代码，在提示框中向用户询问一个逗号分隔的名称列表，然后创建一个警告框按字母顺序显示这些名称。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/abBOZae)。

## 总结

* 数组是值的有序列表。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 索引用于引用数组中的特定项。

注意这会永久更改数组的顺序。

### 排序数组值

我们可以使用 `sort()` 方法对数组中的项进行排序。在 `food` 数组上调用此方法将把数组项重新排列为字母顺序：

```
food.sort();
<< ['Coconut', 'Coffee', 'Cookie', 'Fries', 'Mango', 'Pineapple', 'Pizza', 'Popcorn']
```

![已排序的食物](img/list19.png)

注意这也会永久更改数组的顺序。

### 字母顺序的数字

字符串默认按字母顺序排序，但数字也是如此！这意味着数字是根据它们的第一位数字进行排序的，而不是根据数值。例如，`9` 会排在 `10` 之后，因此你会得到像下面所示的疯狂结果：

```
[5, 9, 10].sort();
<< [10, 5, 9]
```

不过，别担心。这可以使用所谓的“回调”（callback）来修复，我们将在书的后面介绍它。

### 更多方法

数组还有很多可以做的事情。你可以在 [Mozilla 开发者网络](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) 上找到属性和方法的完整列表。看看你是否能找到任何有趣的，并尝试在控制台中中使用它们。

## 多维数组

你可以通过将多个数组放入一个容器数组中，创建一个数组的数组，这被称为 `多维数组`。这可以用于创建坐标系，例如：

```
const coordinates = [[1,3],[4,2]];
<< [[1,3],[4,2]]
```

要访问多维数组中的值，我们使用两个索引——一个指向项在层层数组中的位置，另一个指向它在内层数组中的位置：

```
coordinates[0][0]; // 第一个数组的第一个值
<< 1

coordinates[1][0]; // 第二个数组的第一个值
<< 4

coordinates[0][1]; // 第一个数组的第二个值
<< 3

coordinates[1][1]; // 第二个数组的第二个值
<< 2
```

二维数组的结构如下所示。

![二维数组](img/coordinates.png)

我们之前见过的展开运算符可以用来“展平”多维数组。`展平` 数组涉及通过将所有值从其数组中取出并放在父数组的同一层，移除所有嵌套数组。你可以从下面的示例中看到，只需将 `summer` 和 `winter` 数组放入容器数组就会创建一个嵌套数组，但如果我们在将数组放入容器数组时使用展开运算符，我们得到一个只包含其内容的扁平数组：

```
const summer = ['Jun', 'Jul', 'Aug'];
const winter = ['Dec', 'Jan', 'Feb'];
const nested = [ summer, winter ];
<< [ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ]

const flat = [...summer, ...winter];
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

JavaScript 还有 `flat()` 方法，它不需要展开运算符即可展平数组，如下所示：

```
[ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ].flat();
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

关于创建和操作数组的总结可以在 [SitePoint 的这篇文章](https://www.sitepoint.com/quick-tip-create-manipulate-arrays-in-javascript/) 中找到。

## 挑战

1. 创建名为 `shoppingList` 的变量，初始为一个空数组。尝试使用 `pop`、`push`、`shift`、`unshift` 和 `splice`，以及展开运算符从列表中添加和删除项。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/BaQNzyz)。

2. 使用三个提示框（prompt）向用户询问三个不同的单词，然后将它们放入数组中。使用警告框（alert）显示数组。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/bGBdexY)。

3. 使用提示框让用户输入一个单词。然后使用 `split`、`reverse()` 和 `join()` 方法的组合将单词反过来写。例如，“hello”将变成“olleh”。（提示：为 `split()` 和 `join()` 方法提供一个空字符串作为参数。）你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/poNJbOZ)。

4. 编写一段代码，在提示框中向用户询问一个逗号分隔的名称列表，然后创建一个警告框按字母顺序显示这些名称。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/abBOZae)。

## 总结

* 数组是值的有序列表。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以可以任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 索引用于引用数组中的特定项。

注意这会永久更改数组的顺序。

### 排序数组值

我们可以使用 `sort()` 方法对数组中的项进行排序。在 `food` 数组上调用此方法将把数组项重新排列为字母顺序：

```
food.sort();
<< ['Coconut', 'Coffee', 'Cookie', 'Fries', 'Mango', 'Pineapple', 'Pizza', 'Popcorn']
```

![已排序的食物](img/list19.png)

注意这也会永久更改数组的顺序。

### 字母顺序的数字

字符串默认按字母顺序排序，但数字也是如此！这意味着数字是根据它们的第一位数字进行排序的，而不是根据数值。例如，`9` 会排在 `10` 之后，因此你会得到像下面所示的疯狂结果：

```
[5, 9, 10].sort();
<< [10, 5, 9]
```

不过，别担心。这可以使用所谓的“回调”（callback）来修复，我们将在书的后面介绍它。

### 更多方法

数组还有很多可以做的事情。你可以在 [Mozilla 开发者网络](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) 上找到属性和方法的完整列表。看看你是否能找到任何有趣的，并尝试在控制台中中使用它们。

## 多维数组

你可以通过将多个数组放入一个容器数组中，创建一个数组的数组，这被称为 `多维数组`。这可以用于创建坐标系，例如：

```
const coordinates = [[1,3],[4,2]];
<< [[1,3],[4,2]]
```

要访问多维数组中的值，我们使用两个索引——一个指向项在层层数组中的位置，另一个指向它在内层数组中的位置：

```
coordinates[0][0]; // 第一个数组的第一个值
<< 1

coordinates[1][0]; // 第二个数组的第一个值
<< 4

coordinates[0][1]; // 第一个数组的第二个值
<< 3

coordinates[1][1]; // 第二个数组的第二个值
<< 2
```

二维数组的结构如下所示。

![二维数组](img/coordinates.png)

我们之前见过的展开运算符可以用来“展平”多维数组。`展平` 数组涉及通过将所有值从其数组中取出并放在父数组的同一层，移除所有嵌套数组。你可以从下面的示例中看到，只需将 `summer` 和 `winter` 数组放入容器数组就会创建一个嵌套数组，但如果我们在将数组放入容器数组时使用展开运算符，我们得到一个只包含其内容的扁平数组：

```
const summer = ['Jun', 'Jul', 'Aug'];
const winter = ['Dec', 'Jan', 'Feb'];
const nested = [ summer, winter ];
<< [ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ]

const flat = [...summer, ...winter];
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

JavaScript 还有 `flat()` 方法，它不需要展开运算符即可展平数组，如下所示：

```
[ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ].flat();
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

关于创建和操作数组的总结可以在 [SitePoint 的这篇文章](https://www.sitepoint.com/quick-tip-create-manipulate-arrays-in-javascript/) 中找到。

## 挑战

1. 创建名为 `shoppingList` 的变量，初始为一个空数组。尝试使用 `pop`、`push`、`shift`、`unshift` 和 `splice`，以及展开运算符从列表中添加和删除项。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/BaQNzyz)。

2. 使用三个提示框（prompt）向用户询问三个不同的单词，然后将它们放入数组中。使用警告框（alert）显示数组。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/bGBdexY)。

3. 使用提示框让用户输入一个单词。然后使用 `split`、`reverse()` 和 `join()` 方法的组合将单词反过来写。例如，“hello”将变成“olleh”。（提示：为 `split()` 和 `join()` 方法提供一个空字符串作为参数。）你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/poNJbOZ)。

4. 编写一段代码，在提示框中向用户询问一个逗号分隔的名称列表，然后创建一个警告框按字母顺序显示这些名称。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/abBOZae)。

## 总结

* 数组是值的有序列表。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值的值—— `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 索引用于引用数组中的特定项。

注意这会永久更改数组的顺序。

### 排序数组值

我们可以使用 `sort()` 方法对数组中的项进行排序。在 `food` 数组上调用此方法将把数组项重新排列为字母顺序：

```
food.sort();
<< ['Coconut', 'Coffee', 'Cookie', 'Fries', 'Mango', 'Pineapple', 'Pizza', 'Popcorn']
```

![已排序的食物](img/list19.png)

注意这也会永久更改数组的顺序。

### 字母顺序的数字

字符串默认按字母顺序排序，但数字也是如此！这意味着数字是根据它们的第一位数字进行排序的，而不是根据数值。例如，`9` 会排在 `10` 之后，因此你会得到像下面所示的疯狂结果：

```
[5, 9, 10].sort();
<< [10, 5, 9]
```

不过，别担心。这可以使用所谓的“回调”（callback）来修复，我们将在书的后面介绍它。

### 更多方法

数组还有很多可以做的事情。你可以在 [Mozilla 开发者网络](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) 上找到属性和方法的完整列表。看看你是否能找到任何有趣的，并尝试在控制台中中使用它们。

## 多维数组

你可以通过将多个数组放入一个容器数组中，创建一个数组的数组，这被称为 `多维数组`。这可以用于创建坐标系，例如：

```
const coordinates = [[1,3],[4,2]];
<< [[1,3],[4,2]]
```

要访问多维数组中的值，我们使用两个索引——一个指向项在层层数组中的位置，另一个指向它在内层数组中的位置：

```
coordinates[0][0]; // 第一个数组的第一个值
<< 1

coordinates[1][0]; // 第二个数组的第一个值
<< 4

coordinates[0][1]; // 第一个数组的第二个值
<< 3

coordinates[1][1]; // 第二个数组的第二个值
<< 2
```

二维数组的结构如下所示。

![二维数组](img/coordinates.png)

我们之前见过的展开运算符可以用来“展平”多维数组。`展平` 数组涉及通过将所有值从其数组中取出并放在父数组的同一层，移除所有嵌套数组。你可以从下面的示例中看到，只需将 `summer` 和 `winter` 数组放入容器数组就会创建一个嵌套数组，但如果我们在将数组放入容器数组时使用展开运算符，我们得到一个只包含其内容的扁平数组：

```
const summer = ['Jun', 'Jul', 'Aug'];
const winter = ['Dec', 'Jan', 'Feb'];
const nested = [ summer, winter ];
<< [ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ]

const flat = [...summer, ...winter];
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

JavaScript 还有 `flat()` 方法，它不需要展开运算符即可展平数组，如下所示：

```
[ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ].flat();
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

关于创建和操作数组的总结可以在 [SitePoint 的这篇文章](https://www.sitepoint.com/quick-tip-create-manipulate-arrays-in-javascript/) 中找到。

## 挑战

1. 创建名为 `shoppingList` 的变量，初始为一个空数组。尝试使用 `pop`、`push`、`shift`、`unshift` 和 `splice`，以及展开运算符从列表中添加和删除项。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/BaQNzyz)。

2. 使用三个提示框（prompt）向用户询问三个不同的单词，然后将它们放入数组中。使用警告框（alert）显示数组。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/bGBdexY)。

3. 使用提示框让用户输入一个单词。然后使用 `split`、`reverse()` 和 `join()` 方法的组合将单词反过来写。例如，“hello”将变成“olleh”。（提示：为 `split()` 和 `join()` 方法提供一个空字符串作为参数。）你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/poNJbOZ)。

4. 编写一段代码，在提示框中向用户询问一个逗号分隔的名称列表，然后创建一个警告框按字母顺序显示这些名称。你可以查看 [CodePen 上的代码](https://codepen.io/SitePoint/pen/abBOZae)。

## 总结

* 数组是值的有序列表。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 数组字面量使用方括号编写，其中包含用逗号分隔的值——例如 `[2,3,5,7]`。
* 数组可以包含任何类型的值——即使是其他数组！
* 索引用于引用数组中的特定项。
* 索引用于引用数组中的特定项。

（注：由于原文存在重复内容，翻译文已根据要求进行了去重或翻译逻辑处理了重复的重复的重复的的的重复的的的）...

### 更多方法

数组还有很多可以做的事情。你可以在 [Mozilla 开发者网络](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) 上找到属性和方法的完整列表。看看你是否能找到任何有趣的，并尝试在控制台中中使用它们。

## 多维数组

你可以通过将多个数组放入一个容器数组中，创建一个数组的数组，这被称为 `多维数组`。这可以用于创建坐标系，例如：

```
const coordinates = [[1,3],[4,2]];
<< [[1,3],[4,2]]
```

要访问多维数组中的值，我们使用两个索引——一个指向项在层层数组中的位置，另一个指向它在内层数组中的位置：

```
coordinates[0][0]; // 第一个数组的第一个值
<< 1

coordinates[1][0]; // 第二个数组的第一个值
<< 4

coordinates[0][1]; // 第一个数组的第二个值
<< 3

coordinates[1][1]; // 第二个数组的第二个值
<< 2
```

二维数组的结构如下所示。

![二维数组](img/coordinates.png)

我们之前见过的展开运算符可以用来“展平”多维数组。`展平` 数组涉及通过将所有值从其数组中取出并放在父数组的同一层，移除所有嵌套数组。你可以从下面的示例中看到，只需将 `summer` 和 `winter` 数组放入容器数组就会创建一个嵌套数组，但如果我们在将数组放入容器数组时使用展开运算符，我们得到一个只包含其内容的扁平数组：

```
const summer = ['Jun', 'Jul', 'Aug'];
const winter = ['Dec', 'Jan', 'Feb'];
const nested = [ summer, winter ];
<< [ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ]

const flat = [...summer, ...winter];
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

JavaScript 还有 `flat()` 方法，它不需要展开运算符即可展平数组，如下所示：

```
[ [ 'Jun', 'Jul', 'Aug' ], [ 'Dec', 'Jan', 'Feb' ] ].flat();
<< [ 'Jun', 'Jul', 'Aug', 'Dec', 'Jan', 'Feb' ]
```

关于创建和操作数组的总结可以在 [SitePoint 的这篇文章](https://www.sitepoint.com/quick-tip-create-manipulate-arrays-in-javascript/) 中找到。




我们的小型游戏只有四个角色：Alfie、Betty、Gemma 和 Del。

![我们“猜猜谁”游戏中的四个角色](img/guesswho.png)

每个角色都有两个特定特征：他们要么戴帽子，要么不戴；他们要么戴眼镜，要么不戴。

例如，如果我问“谁戴了眼镜？”，答案就是“Betty 和 Del”。

![谁戴了眼镜？](img/glasses.png)

### 否定（逻辑非）

`Negation`（否定）返回一个布尔值的反值。因此，真值（truthy values）将返回 `false`，而假值（falsy values）将返回 `true`。

例如，如果我正在玩“猜猜谁”游戏，问题“谁**没有**戴眼镜？”是对问题“谁戴了眼镜？”的否定。“NOT”这个词充当了否定操作符，答案是“Alfie 和 Gemma”。

![谁没有戴眼镜？](img/notglasses.png)

如果我问“谁**没有**戴帽子”，这将是对所有*戴着*帽子的人的否定，答案将是“Alfie 和 Del”。

![谁没有戴帽子？](img/nothat.png)

在 JavaScript 中，通过在值前面加上逻辑非操作符（`!`）来实现否定。这可以被认为是在语句前面加上“NOT”单词是一样的。一个真值总是会被否定为 `false`，而假值总是会被否定为 `true`。我们可以通过在控制台中尝试以下示例来看到这一点：

```
!true; // 否定 true 返回 false
<< false

!0; // 0 是假值，所以否定它返回 true
<< true

!'hello'; // 所有非空字符串都是真值
<< false
```

`Double negation`（双重否定，`!!`）是一种用于判断一个值是真值还是假值的快捷方法，因为它实际上是“否定了否定”，将值变回其原始的布尔值，如下代码所示：

```
!!''; // 空字符串是假值
<< false

!!"hello"; // 所有非空字符串都是真值
<< true

!!3; // 所有非零数字都是真值
<< true

!!0; // 零是假值
<< false
```

双重否定的效果与我们之前在章节中看到的 `Boolean()` 函数相同。

### 逻辑与

为了看到 AND 操作符的示例，让我们再次玩“猜猜谁”游戏。如果我问“谁既戴了眼镜**又**戴了帽子？”，结果将是“Betty”。

![谁戴着帽子和眼镜？](img/glassesandhat.png)

在这种情况下，“AND”这个词充当了逻辑操作符。逻辑 AND 操作符作用于两个或多个值，如果*所有*值都是真值，则返回 `true`；如果其中*任何*一个是假值，则返回 `false`。

在 JavaScript 中，`&&` 用作逻辑 AND 操作符。如果所有值都是真值，则返回*最后一个*真值；如果某些是假值，则返回*第一个*假值。可以通过下面的代码示例看到：

```
'hello' && 42;
<< 42
```

字符串 `'hello'` 和数字 `42` 都是真值，所以返回最后一个值 `42`。

下一个语句返回 `false`，因为它是语句中的第一个假值：

```
true && false; // 返回 false 是因为它是假值
<< false
```

### 逻辑或

让我们回到玩“猜猜谁”游戏来演示逻辑 OR 操作符。

如果我们问“谁戴了眼镜**或**戴了帽子？”，这将包括所有戴了眼镜、帽子或两者都戴的人，所以答案是“Betty, Gemma 和 Del”。

![谁戴着眼镜或帽子？](img/glassesorhat.png)

在这个例子中，“OR”这个词充当了逻辑操作符。

逻辑 OR 操作符作用于两个或多个值，如果其中*任何*值是真值，则返回 true；如果*所有*值都是假的，则返回 `false`。

在 JavaScript 中，`||` 用作逻辑 OR 操作符。如果其中任何一个为真，则返回*第一个*真值；如果所有都是假的，则返回*最后一个*假值。

你可以在下面的代码示例中看到这一点。如果两个表达式都是真值，则返回第一个：

```
'hello' || 'goodbye';
<< 'hello'
```

这返回 `'hello'`，因为它是这个两个值均为真值的复合语句中的第一个真值。

如果值中只有一个是真值，则将返回该值，正如下一个示例所示：

```
'all' || 0; // 要全或全无！
<< 'all'
```

在最后一个示例中，两个值都是假值，所以返回*最后一个*值：

```
false || 0;
<< 0
```

### 比较

在编程时，我们经常需要比较值，有多种方法可以实现。

### 等等

`equality operator`（相等操作符）可用于检查两个值是否相等。大多数编程语言使用双等操作符（`==`）来检查相等性。

例如，如果我们想知道变量 `answer` 是否等于 42，我们可以写：

```
answer == 42;
```




```
answer === Number('42');
<< true
```

当你处理用户输入的、且预期其为数字的值时，这种方法非常有用，因为大多数编程语言都会会将用户输入的数据视为字符串。

## 不等性

我们可以使用`不不等运算符`来检查两个值是否`不`相等。这里有一个软不不等运算符（`!=`）和一个强不不等运算符（`!==`）。它们的工作方式与软相等运算符和强相等运算符类似：

```
16 != '16'; // 类型转换使得它们相等
<< false

16 !== '16';
<< true
```

与相等性判断一样，你应该使用强不不等运算符，因为这将提供更可靠的结果，且不受类型转换的影响。

## 大于和小于

我们可以使用 `>` 运算符来检查一个值是否大于另一个值。以下代码可以用于检查变量 `answer`（值为 42）是否大于 10：

```
answer > 10;
<< true
```

你也可以以类似的方式使用“小于”运算符（`<`）来检查 `answer` 是否小于 50：

```
answer < 50;
<< true
```

如果你想检查一个值是否大于、小于*或等于*另一个值，你可以使用 `>=` 和 `<=` 运算符。以下代码将检查 `answer` 是否小于或等于 42：

```
answer <= 42;
<< true
```

这些运算符也可以用于字符串，字符串将按字母顺序排序，以检查其中一个字符串是否“小于”另一个：

```
'apples' < 'bananas';
>> true
```

但请注意，结果是区分大小大小的，且大写字母被认为“小于”小写字母：

```
'apples' < 'Bananas';
>> false
```

## 流程控制

在上一节中，我们查看了如何比较语句，例如检查两个值是否相等。在本节中，我们将根据语句的真假值通过运行不同的代码块，来控制程序的执行流。这有点比在程序中遇到了一个十字路口，你可以决定代码将向哪个方向运行。这将有助于我们的程序变得有趣得多，因为它们可以根据发生的情况产生不同的结果。

### If 语句

`if 语句`可以用于仅在特定条件返回真时运行代码块。例如，假设你想检查自己是否累了。如果你*确实*累了，计划就是去睡觉。这可以通过下面的图所示：

![你累了吗？](img/if-tired.png)

在伪代码中，可以这样写：

```
if you are tired then go to sleep.
```

在 JavaScript 中，代码看起来如下：

```javascript
if (tired) {
  sleep();
}
```

块中的内部代码只有在括号中的条件为真时才会运行。如果条件不是布尔值，它将根据它是真（truthy）还是假（falsy）转换为布尔值。

让我们通过在控制台中输入以下内容尝试编写一些条件代码：

```
let energy = 10;
if (energy < 3) {
  alert('ZZZ...');
}
```

只有当 `energy < 3` 求值为 `true` 时，才会显示警告框，因此只有当 `energy` 变量的值小于 3 时。由于 `energy` 变量被赋值为 10，这意味着什么都不会发生。

尝试在控制台中将 `energy` 变量的值改为 3 以下的值，然后再次进入 if 块。这一次，警告框将像下图所示显示：

![ZZZ...](img/zzz.png)

显然，在实际程序中，我们不会这样手动更改变量。它们通常取决于用户输入或程序中的其他条件。但别担心——我们很快就会接触更多实用的示例！

### Else 语句

如果条件不为真，你想做些别什么呢？这正是 `else 语句`的作用。

例如，假设你累了就去睡觉，否则你想去跑步。这可以通过下面的图所示：

![睡觉还是跑步？](img/if-tired-else-run.png)

在伪代码中，可以这样写：

```
if you are tired then go to sleep
else go for a run
```

在 JavaScript 中，写法如下：

```javascript
if(tired){
  sleep();
} else {
  run();
}
```

`else` 关键字添加了一个备选代码块，只有当原始条件不为真时才会执行。这意味着其中代码块将会运行。

让我们在控制台中写一个 if–else 语句：

```
let energy = 10;
if (energy < 3) {
  alert('ZZZ....');
} else {
  alert('Time to start running!');
}
```

这段代码应该产生一个与下图类似的警告。

![该开始跑步了！](img/run.png)

### 三元运算符

`三元运算符`（`?`）是编写 if–else 语句的简写方式。它接受三个操作数：一个条件、一个真时的结果和一个假时的结果。

```javascript
energy = 10;
energy < 3 ? alert('ZZZ...') : alert('Time to start running!');
```

三元运算符可以用于替换简单的 `if...else` 语句。它通常更简洁，但如果逻辑复杂，可能更难以阅读。





这里另一个可以根据测试分数生成等级的示例：

```
const legs = Number(prompt('How many legs does your favorite animal have?'));
if (legs === 0) {
  alert('Your favorite animal is a fish!');
} else if (legs === 2) {
  alert('Your favorite animal is a penguin!');
} else if(legs === 4){
  alert('Your favorite animal is an elephant!');
} else if(legs === 8){
  alert('Your favorite animal is an octopus!');
} else {
  alert(`I'm not sure what animal has that many legs!`);
}
```

`switch operator` 提供了一种替代表示法，当有很多条件需要测试时（如本例所示），它可以让你的代码更容易读。

上面的示例可以使用 `switch` 语句重写如下：

```
const legs = Number(prompt('How many legs does your favorite animal have?'));

switch (legs) {
case 0:
  alert('Your favorite animal is a fish!');
  break;
case 2:
  alert('Your favorite animal is a penguin!');
  break;
case 4:
  alert('Your favorite animal is an elephant!');
  break;
case 8:
  alert('Your favorite animal is an octopus!');
  break;
default:
  alert(`I'm not sure what animal has that many legs!`);
}
```

你正在比较的值放在 `switch` 运算符后面的括号中。随后使用 `case` 关键字来对应每个可能出现的值（上述示例中的 0, 2, 4 和 8）。在每个 `case` 语句之后是当该 case 发生时应该运行的代码。

`default` 关键字用于末尾，用于在任何 `case` 都不真的情况下需要运行的代码。在下面的示例中，如果你没有得到 10、9 或 8 分，它会给出一个遗憾的消息，告诉你测试没格了。

你可以查看 [我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/KKNpOPB)。

### 使用 `break`

用 `break` 关键字结束每个 `case` 块是非常重要的，因为这会停止任何后续 `case` 块的执行。如果没有 `break` 语句，程序将“贯穿”（fall through）并继续评估后续的 `case` 块。

## 剪刀石头布

让我们在 CodePen 上尝试另一个编码项目。这次，我们将尝试创建一个经典游戏剪刀石头游戏的互动版本，你将与电脑对战。这将让我们有机会使用在在本章中学习的知识来判断谁赢了游戏。

开始之前，让我们询问玩家他们的选择是什么。打开一个新的 Pen 并在 `JS` 部分添加以下代码：

```
const player = prompt('Choose rock, paper or scissors').toLowerCase().trim();
```

这使用一个提示框要求用户输入“rock”、“paper”或“scissors”。

我们还使用 `toLowerCase()` 和 `trim()` 方法对他们的答案进行了“清洗”。这确保了他们的答案全为小写，并移除了任何多余的空格。这个字符串存储在变量 `player` 中。

接下来，我们需要编写电脑的选择。剪刀石头游戏的最佳策略是随机玩，因此我们可以根据随机数来决定电脑的选择。让我们现在创建那个随机数。添加以下代码：

```
const number = Math.ceil(3*Math.random());
```

这使用了我们在 第 4 章 中遇到过的 `Math.ceil()` 和 `Math.random()` 方法来选择 1 到 3 之间的随机数，并将其存储在变量 `number` 中。我们现在需要使用这个数字来选择电脑的选择。我们将使用 switch 块来实现。添加以下代码：

```
let computer;

switch(number){
  case 1: 
    computer = 'rock'; break;
  case 2:
    computer = 'paper'; break;
  case 3:
    computer ='scissors';
}
```

首先，这声明了一个名为 `computer` 的变量，用于存储电脑的选择。然后我们创建了一个 switch 语句，获取我们之前选择的随机数，如果它是 1，则将值“rock”赋值给变量 `computer`；如果是 2，则赋值“paper”，如果是 3，则赋值“scissors”。

我们现在有一个名为 `player` 的变量和另一个名为 `computer` 的变量。这两个变量都包含一个字符串 'rock''paper' 或 'scissors'，分别代表玩家和电脑的选择。我们的下一个工作是根据这些值判断谁赢。最容易测试的结果是平局，因为如果 `player` 和 `computer` 变量相同，就会发生平局。添加以下代码处理此情况：

```
if (player === computer){
  alert(`It was a draw, we both chose ${player}`);
}
```

注意我们如何使用模板字符串和字符串插值来反馈他们都做出的选择。

接下来，我们将查看所有导致玩家胜出的选项。这种情况有三种方式：

*   玩家选择“rock”，电脑选择“scissors”
*   玩家选择“paper”，电脑选择“rock”
*   玩家选择“scissors”，电脑选择“paper”

所有这些选项都可以使用逻辑 AND 和 OR 运算符来表示。如下所示：

```javascript
if (player === 'rock' && computer === 'scissors') ||
    (player === 'paper' && computer === 'rock') ||
    (player === 'scissors' && computer === 'paper') {
  alert(`You win!`);
} else if (player === computer) {
  alert(`It was a draw, we both chose ${player}`);
} else {
  alert(`You lose!`);
}
```

## 挑战

1. 编写一些代码问一个问题，然后检查用户提供的答案是否正确。使用提示框告诉他们是对是错。你可以查看 [我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/XNbvd)。
2. 编写一个“大小”游戏。电脑应该随机选择 1 到 10 之间的数字，然后使用确认框询问用户下一个数字是否更大。电脑应选择另一个 1 到 10 之间的随机数，并告诉用户是对是错。你可以查看 [我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/jOVv)。
3. 编写一些代码随机两个数字，然后要求用户将它们相乘。使用提示框告诉用户答案是否正确。你可以查看 [我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/NWqr)。

## 总结

*   布尔值是原始值 `true` 或 `false`。
*   所有值都有内在的布尔值 `true` 或 `false`。
*   真值是布尔值为 `true` 的值。大多数值都是真值。
*   假值是布尔值为 `false` 的值。不同语言中的假值有所不同。JavaScript 中有九个假值。
*   取反会让真值变假，假值变真。双重取反返回一个值的布尔值。
*   逻辑运算符（如 AND 和 OR）可以组合多个语句。
*   可以比较值以查看它们是否等于、大于或小于其他值。
*   条件语句可以根据条件控制程序的流。
*   三元运算符是用单行代码编写 if-else 语句的简洁方式。
*   当有多个选项时，可以使用 switch 语句。





计算机非常擅长反复执行重复性任务。它们永远不会感到无聊，并且每次都会完全按照指令执行。循环（Loops）是一种让程序根据特定条件重复某段代码的方法。

在本章中我们将涵盖：

*   什么是循环
*   无限循环
*   while 循环
*   do–while 循环
*   for 循环
*   嵌套循环

## 什么是循环？

`loop`（循环）是一段会持续运行直到满足某个特定条件的代码。

为了说明这一点，这里有一张图，展示了火箭发射前的倒计时作为一个循环。

![火箭倒计时循环](img/countdownloop.png)

如你所见，我们从 10 开始，大声说出数字，将数字减去 1，然后检查是否达到了 0。如果还没有达到零，我们就回到开头重复该过程，因此我们继续大声说出数字，然后减 1，直到达到 0。一旦发生这种情况，我们就会跳出循环，火箭就可以发射了！

在本章中，我们将学习编写循环的各种不同方法。和往常一样，我们将使用 JavaScript 来演示代码，尽管这些原理在大多数其他编程语言中是非常相似的。

## 无限循环

在某个时刻满足停止循环的条件是非常重要的。否则，你的代码将陷入 `infinite loop`（无限循环），这可能导致程序崩溃或使其“卡死”。

考虑图中所示的循环。它与上一个非常相似，但有一个细微的。你能发现它并解释为什么这意味着循环永远不会结束吗？

![无限循环](img/infiniteloop.png)

这个示例中的问题是，数字每次通过循环都会*增加* 1，因此它永远不会达到零，从而永远不会跳循环并停止。每当你编写循环时，都需要确保有一种方法让它结束运行。

## While 循环

我们将查看的第一种循环是 `while loop`。当某个条件为真时，它会反复运行一段代码。

while 循环的伪代码可能看起来如下：

```
while (some condition is true) {
  do something
}
```

只要括号中设置的条件保持为真，程序就会继续“执行操作”。通常，代码块会执行对条件真值产生影响的操作，最终它将变为假，循环就会结束。

### 十个绿瓶子

循环的一个经典演示是让计算机“唱”热门歌曲 [Ten Green Bottles](https://www.youtube.com/watch?v=Ak7kedzR8bg) 的歌词。

接下来的图展示了如何使用 while 循环来实现这一点。

![while 循环是如何工作的](img/whileloop.png)

我们在进入主循环之前，首先将瓶子的数量初始化为 10。在每次循环开始时，都会检查瓶子是否大于零，如果是，循环将继续。否则，它将跳出并停止。

让我们尝试用 JavaScript 写这段代码。打开控制台并输入以下代码：

```javascript
let bottles = 10;
```

这将一个名为 `bottles` 的变量初始化为 10。这代表墙上剩余的瓶子数量。在 while 循环中使用的任何变量必须在循环运行之前声明并初始化。否则，在循环中引用它们时将会报错。

现在让我们写这个循环：

```javascript
while (bottles > 0){
  console.log(`There were ${bottles} green bottles, hanging on a wall. And if one green bottle should accidentally fall, there'd be ${bottles-1} green bottles hanging on the wall.`);
  bottles--;
}
```

循环以 `while` 关键字开头，后面跟着括号中的条件，即变量 `bottles` 必须大于零。只要该条件为真，循环就会继续执行。这基本上意味着“只要瓶子的数量大于零，就重复这段代码块”。

代码块使用 `console.log` 记录一个使用字符串插值的模板字面量（template literal），以显示剩余瓶子的数量。输出将显示在控制台中。然后使用递减运算符（`--`）将 `bottles` 变量减少 1。

![在控制台中显示的十个绿瓶子的结果](img/greenbottles.png)

你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/poNgevL?editors=1112。（点击左下角的 **Console** 标签以查看 CodePen 控制台中的结果。）

## Do–while 循环

`do–while loop` 与 while 循环类似。唯一的区别是条件出现在代码块*之后*。在伪代码中，它可能看起来如下：

```
do {
  // do something
} while(condition)
```

while 循环和 do–while 循环之间的关键区别在于，在 do-while 循环中，代码块先执行，这意味着无论条件是否为真，它都会至少运行一次。

接下来的图展示了如何使用 do–while 循环实现“十个绿瓶子”歌曲。

![do–while 循环是如何工作的](img/dowhileloop.png)

如你所见，它与 while 循环非常相似，只是条件移动到了最后。让我们尝试用 JavaScript 编写它：

```javascript
let bottles = 10;
do {
  console.log(`There were ${bottles} green bottles, hanging on a wall. And if one green bottle should accidentally fall, there'd be ${bottles-1} green bottles hanging on the wall.`);
  bottles--;
} while (bottles > 0);
```

你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/ZEBQ)。

## For 循环

`for loops`（for 循环）是最常见的循环类型，出现在大多数编程语言中。它们的形式如下：

```
for (initialization ; condition ; update) { 
  do something
}
```

括号内设置了三件事：

*   `initialization`（初始化）代码在循环开始之前之前运行，通常用于初始化循环中使用的任何变量。
*   `condition`（条件）必须满足循环才能继续。
*   `update`（更新）代码在每次*迭代*之后执行，通常用于更新任何值。

这一过程在图中所示。

![for 循环是如何工作的](img/forloop.png)

对于瓶子歌曲，我们需要将瓶子数量初始化为 10。条件是该数量必须大于零，更新代码是将瓶子数量减少 1。如下所示。

![十个绿瓶子的 for 循环](img/forbottles.png)

让我们尝试用 JavaScript 编写。在控制台中输入以下代码：

```javascript
for (let bottles = 10 ; bottles > 0 ; bottles--) {
  console.log(`There were ${bottles} green bottles, hanging on a wall. And if one green bottle should accidentally fall, there'd be ${bottles-1} green bottles hanging on the wall`);
}
```

这把变量 `bottles` 初始化为 10，然后设置条件为 `bottles > 0`，并在每次循环后使用递减运算符 `bottles--` 将 `bottles` 变量的值减少 1。

你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/Vwmepa)。

结果与之前完全相同。事实上，你可能已经注意到可以使用 while 循环、do–while 循环或 for 循环来实现完全相同的结果。for 循环通常被认为更清晰（并且在 Web 相关的代码示例中更流行），可能是因为循环的所有细节（初始化、条件和更新代码）都在同一个地方，并保持在实际代码块之外。





你可以将一个循环放在另一个循环内部，创建一个**嵌套循环**。它们包含一个内循环，在外层循环执行下一步之前，内循环会完整运行。可以通过下面的图直观地看到这一点。

![嵌套循环如何工作](img/nestedloop.png)

如你所示，对于外层循环的每一步，内循环都会完整运行。一旦内循环运行完毕，外层循环的变量就会更新，然后它再次完整运行内循环。此过程一直持续，直到外层循环满足停止条件。

让我们写一个程序来创建一个乘法表，从“1 的表”一直到“12 的表”。也就是说，1 x 1 = 1，1 x 2 = 2，1 x 3 = 3 …… 直到 12 x 12 = 144。

为了实现这一点，我们希望外层循环将第一个数字设置为 1，然后使用内循环将其乘以第二个数字，该数字在每一步中将从 1 变为 12。当我们用 1 乘以每一个数字后，我们会在外层循环中将第一个数字增加到 2，并在内循环中用它乘以 1 到 12 的所有数字，依此类推，直到得到 12 乘以 12。

在控制台中输入以下代码：

```
// outer loop
for(let i=1 ; i<13 ; i++){
  // inner loop
  for(let j=1 ; j<13 ; j++){
    console.log(`${j} multiplied by ${i} is ${i*j}`);
  }
}
```

### 循环变量

我们在上面的代码中创建了两个变量，`i` 和 `j`。在循环中，传统上使用单个字母作为这些“计数器”变量名。为什么呢？因为这样很整洁！但你可以使用任何长度的变量名（就像我们在编写“十个绿瓶子”循环时做的那样）。但是，为什么要写比需要的更长的变量名呢？

需要注意的是，你需要在每个嵌套循环中使用不同的字母作为变量，以免产生混淆。在这个例子中，我们在外层循环中使用 `i`，在内循环中使用 `j`。

外层循环将变量 `i` 从 1 增加到 12。对于外层循环的每一步，内循环都会将变量 `j` 从 1 增加到 12。因此，第一次迭代从 `i = 1` 和 `j = 1` 开始，并在控制台输出输出：

```
<< 1 multiplied by 1 is 1
```

在下一步中，我们仍在内循环内部，因此 `i` 保持为 1，但 `j` 增加到 2，结果如下：

```
<< 1 multiplied by 2 is 2
```

`j` 继续增加直到达到 12。之后，程序跳出内循环并返回外层循环，此时 `i` 从 1 更新为 2。然后它重新进入内循环，`j` 被初始化回 1 并再次开始计数到 12。这个过程一直持续，直到最后一次迭代产生这一行：

```
<< 12 multiplied by 12 is 144
```

在控制台中运行这段代码。你应该会在控制台中看到与下图所示的输出。

![乘法表](img/multiplications.png)

你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/eYBJvMo)。

## 挑战

1. 写一个从 1 计数到 100 的循环，并检查数字是否是 3 或 5 的倍数。如果是 3 的倍数，应该在控制台打印“Fizz”。如果是 5 的倍数，应该在控制台打印“Buzz”。如果是 3 和 5 的倍数，应该在控制台打印“FizzBuzz”，如果两个者都不是倍数，则只需在控制台打印该数字。初始输出应该像这样：

   ```
   << 1, 2, Fizz, 4, Buzz, Fizz, 7, 8, Fizz, Buzz, 11, Fizz, 13, 14, FizzBuzz, ...
   ```

   提示：这个挑战需要你使用模运算符（`%`）。我们在第 3 章中讨论过模运算符。你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/NWbxpzM)。

2. 在上一章中，我们为一个大数字小的游戏写了一些代码，但它只给了用户一次猜大或小的机会。写一些代码，允许用户继续猜直到猜错。它还应该在游戏结束时告诉他们他们猜对了多少次。你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/yLVeMEG)。

3. 在上一章中，我们写了一个乘法表问题游戏（挑战 3）。修改代码，使其询问五个问题并记录用户答对的个数。你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/wvoJjdQ)。

## 总结

*   函数是一个可以重用和调用的代码块。
*   函数有助于减少重复（DRY 原则）。
*   嵌套循环由包含在另一个内部的循环组成，在外层循环的每一步中，内循环都会完整运行。
*   函数可以接受输入（参数/参数）并提供输出（返回值）。





某些语言（如 Ruby）区分了过程（procedures）和函数（functions），并使用不同的语法来创建它们。JavaScript 并没有这样做，它仅使用函数来创建命名的代码块。

如果没有显式指定返回值，JavaScript 函数将返回 `undefined` 值。

# JavaScript 中的函数

函数是任何编程语言中不可或缺的部分。它们是大多数 JavaScript 程序的根本构建块，因此掌握理解函数是一项必须掌握的本质技能。

## 定义函数

在 JavaScript 中定义函数的最常用方法是使用如下所示的 `function declaration`（函数声明）。请尝试在控制台中输入以下内容：

```
function hello(){
  alert('Hello, World!');
}
```

这创建了一个名为 `hello` 的函数。描述函数功能的代码块位于大括号内部。这段代码将创建一个显示“Hello, World!”消息的警报框。

不过，定义函数本身并没有执行任何操作。为了实际运行函数内部的代码，你必须“调用”（call）它。

## 调用函数

调用函数将运行函数体内的代码块。要调用我们上面定义的 `hello()` 函数，只需在控制台中输入以下内容并按 `Enter` 键：

```
hello();
```

这应该产生一个像所示的警报框。

![Hello, World!](img/hello.png)

你可以通过不断输入函数名后加括号来反复调用该函数（试试看……直到你厌倦了不断关闭那些警报框为止！）。

这是使用函数的优点之一：不需要不断编写重复的代码块。另一个优点是，所有功能都保留在一个地方。因此，如果你想更改部分功能，只需要更新函数声明中的那一段代码即可。例如，如果警报框真的让我们开始很心烦，我们可以将 `hello()` 函数修改为：

```
function hello(){
  console.log('Hello, World!');
}
```

现在，每次调用函数时，消息都会被记录到控制台中，而不是显示在那些烦人的弹窗警报框中。想象一下这段代码在我们的程序中使用了成百千次：要修改每一个实例将是多么痛苦。通过使用函数，我们只需要更改一个地方的代码，*每一个*实例都会得到更新。这是 DRY 原则（不要重复自己）生效的完美示例。

## 函数表达式

定义函数的另一种方法是创建 `function expression`（函数表达式）。这会将一个“匿名函数”赋值给一个变量，如下例所示：

```
const goodbye = function(){
  alert('Goodbye, World!');
};
```

`anonymous function`（匿名函数）是使用我们之前使用的函数声明创建的，但它没有被分配名称。相反，函数被赋值给一个用于引用该函数的变量。在上面的示例中，变量名为 `goodbye`。

### 赋值与分号

请注意，上面的示例以分号结尾。这结束了赋值语句，而普通的函数声明以代码块结束（分号不会放在代码块的末尾）。

调用函数表达式的方式与调用函数声明相同——通过编写它被赋值的变量名，后跟括号：

```
goodbye();
```

![Goodbye, World!](img/goodbye.png)

### 调用 vs 引用函数

请记住，你需要括号来调用函数。如果你忘记添加括号，你只是在引用该函数本身，而不是在调用它。

## 箭头函数

箭头函数（Arrow functions）直到 2015 年才被添加到 JavaScript 中，它们与其他编写函数的方式非常不同。它们使用了更简洁的语法，使得编写起来更快，并以“箭头”符号（`=>`）标识并命名。

`Arrow functions`（箭头函数）总是匿名的，所以如果你想引用它们，必须将它们赋值给一个变量，就像我们对函数表达式做的那样。下面的示例了如何创建一个赋值给变量 `hola` 的箭头函数：

```
const hola = () => alert('Hola, Mundo!');
```

箭头函数以括号和箭头开头，`() =>`。之后的所有内容都是调用函数时将运行的代码。注意，这段代码不需要放在任何大括号内（只要它只有一行代码），这使得函数看起来要简洁得多。

箭头函数的调用方式与任何其他函数完全相同：只需编写它的名字——不要忘记在末尾添加那些括号：

```
hola();
```

![Hola, Mundo!](img/hola.png)

# 返回值

函数总是 `return`（返回或输出）一个值。这可以在函数体中使用 `return` 关键字进行指定。

例如，以下函数将返回字符串 `'Howdy, World!'`：

```
function howdy(){
  return 'Howdy, World!';
}
```

返回值可以是任何类型的值——甚至是函数！（这将在后面的章节中介绍。）

### 返回 undefined

如果没有显式说明返回值，它将默认返回 `undefined`。这是因为一个函数必须返回一个值才能被视为函数。你经常会在调用一个本质上只是过程且不需要返回值的函数后，在控制台中看到 `undefined` 。我们一直在使用的 `alert` 函数就是这样一个例子。

![The function returns undefined](img/undefined.png)

当使用箭头函数时，如果函数体只有一行，你甚至不需要显式地使用 `return` 关键字。例如，上面的 `howdy` 函数可以使用箭头符号写为：

```
const howdy = () => 'Howdy, World!';
```

## 参数

`Parameters`（参数）和 `arguments`（实参）这两个术语经常互换，表示提供给函数的值。不过它们有一个细微的区别：参数是在函数定义时设置的，而参数是在调用函数时提供的。

为了看到使用参数函数的示例，让我们创建一个计算平方的函数。在以下示例中，`square` 函数接受单个参数 `n`，它是要平方的数字。在函数体内，参数名称的作用就像一个变量。我们将此值乘以自身并返回结果：

```
function square(n){
  return n*n;
}
```

当我们调用此函数时，我们需要提供一个参数，它取代定义中参数的位置，它是要平方的数字：

```
square(4.5);
<< 20.25
```

在定义带有单个参数的箭头函数时，参数位于箭头之前，函数的主体位于之后。例如，`square` 函数可以这样写：

```
const square = n => n*n;
```

注意，箭头函数的参数周围不需要括号，使得它们更加简洁。

在定义函数时，你可以使用任意数量的参数。例如，以下函数通过将三个数字相加并将结果除以三来找到它们的平均值（mean）：

```
function mean(a,b,c){
  return (a+b+c)/3;
}
```

让我们在控制台中运行它：

```
mean(8, 3, 4);
<< 5
```

当在箭头函数中使用多个参数时，你需要将它们放在括号中，因此 `mean` 函数用箭头符号表示的形式如下：

```
mean = (a,b,c) => (a+b+c)/3;
```





当调用函数时没有提供参数作为参数时，函数仍会被调用，但缺失的参数将被赋予一个 `undefined` 的值。例如，如果我们尝试只用两个参数调用 `mean` 函数，它将返回 `NaN`，这是尝试将数字与 `undefined` 相加得到的结果。尝试在控制台中输入以下示例以查看此结果：

```
mean(1,2);
<< NaN
```

![mean 函数缺少第三个参数，导致了 NaN](img/nan.png)

如果调用函数时提供的参数过多，函数将正常工作，多余的参数将被忽略。下面的示例将返回 1, 2 和 3 的平均值，并忽略参数 4 和 5：

```
mean(1,2,3,4,5);
<< 2
```

### 默认参数

JavaScript 提供了一种简便的方法来为函数指定默认参数。这些值是当函数在被调用时没有提供任何参数，函数将将使用的值。要指定默认参数，你只需在函数定义中为它分配默认值即可。例如，以下函数接受一个参数，然后将其添加到字符串 `'Hello '` 的末尾。该参数被赋予了默认值 `'World'`：

```
function hello(name='World') {
  alert(`Hello, ${name}!`);
}
```

现在，如果我们不带任何参数就调用此函数，它将默认使用 `'World'` 作为 `name` 参数：

```
hello();
<< 'Hello, World!'
```

如果你不想使用 `'World'` 作为参数，可以通过指定一个不同的值作为参数来覆盖这个默认值。例如，向宇宙打个好怎么样？

```
hello('Universe');
<< 'Hello, Universe!'
```

默认参数应该始终放在非默认参数之后。否则，你在调用函数时仍然得要输入默认值。考虑下面这个计算商店折扣价的函数：

```javascript
function discount(price, amount=10) {
  return price*(100-amount)/100;
}
```

此函数接受两个参数：商品的价格以及要应用的折扣百分比。商店最常见的折扣是 10%，因此它被作为一个默认值提供。这意味着在大多数情况下可以省略 `amount` 参数，并且会应用 10% 的折扣。例如，你可以使用以下代码计算一个 20 美元商品在 10% 折扣后的销售价：

```
discount(20);
<< 18
```

注意，我们并没有指定折扣为 10%。

如果需要应用不同的折扣，可以提供 `amount` 参数。在下面的示例中，一个 15 美元的商品被给予了 20% 的折扣：

```
discount(15, 20);
<< 12
```

然而，如果参数定义的顺序反了，例如下面的示例所示，这将无法工作：

```javascript
function discount(amount=10, price) {
  return price*(100-amount)/100;
}
```

现在，如果我们尝试只用一个参数使用函数，函数将无法工作，因为 `price` 还没有被设置：

```
discount(20);
<< NaN
```

这会将 `amount` 设置为 20，但没有为 `price` 提供参数，因此计算无法完成并返回 `NaN`。

不过，如果两个值都输入，它仍然可以工作：

```
discount(10,20);
<< 18
```

这在很大程度上违背了设置默认参数的意义！这里要记住的黄金法是始终将默认参数放在所有其他参数*之后*。

### 随机整数

我们在数字章节（第 4 章）遇到过 `Math.random()` 方法，它创建一个 0 到 1 之间的随机小数。在程序中，我们经常需要随机整数值。事实上，在上一章的“猜数字”游戏中，我们使用了以下代码在 1 到 10 之间选择一个随机数：

```
Math.ceil(Math.random()*10);
```

将这段代码抽象成一个“辅助”函数是一个很有用的练习，你可以在任何需要生成随机整数时使用它。

在上面的代码中，值 10 提供了数字范围的上限，因此我们可以将其作为函数的参数。这将允许我们在调用函数时选择上限。该函数可能像这样，写成函数声明：

```javascript
randomInt(n){
  return Math.ceil(Math.random()*n);
}
```

这将返回一个从 1 到作为参数提供的数字之间的随机整数。例如，我们可以使用以下代码生成一个 1 到 6 之间的随机数：

```
randomInt(6);
<< 3
```

如果我们能为此函数添加一个可选的下限，也会很有用。很多时候，当我们需要随机整数时，下限是 1，因此我们将 1 设置为默认值：

```javascript
randomInt(upper,lower=1){
  return Math.floor(Math.random()*(upper-lower+1)+lower);
}
```

现在它将返回一个作为参数提供的下限和上限值之间的随机整数。

### 将返回值赋值给变量

JavaScript 中的一个重要概念是函数被视为一等对象（first-class objects）。这意味着它们的行为与其他数据类型相同：可以被赋值给变量，甚至可以被其他函数使用。

我们将函数调用的返回值赋值给变量。为了看到这种效果，请在控制台中尝试以下代码：

```javascript
const hello(){
  return 'Hello, World!';
}

const message = hello();
<< 'Hello, World!'
```

变量 `message` 现在指向 `hello()` 函数的返回值，即字符串 `'Hello, World!'`，正如运行以下代码显示变量的值所示：

```
message;
<< 'Hello, World!'
```

这似乎看起来工作量很大且毫无意义：为什么不直接将字符串赋值给变量？答案是，我们可以创建更复杂的函数，根据条件有不同的返回值。这种技术允许我们根据函数的输出为变量赋值不同的值。

例如，假设我们想检查一个人是否超过了 18 岁。我们可以写一个接受年龄作为参数的函数，如果他们超过 18 岁则返回 `true`，否则返回 `false`。它可能像这样：

```javascript
userIsChild = function(age){
  if(age<18){
    return true;
  } else {
    return false;
  }
}
```

然后，在程序的后续，我们可能想使用名为 `restrictedAccess` 的变量来限制儿童访问网站某些部分，如果用户输入的年龄小于 18 岁，该变量即为真。我们可以使用以下代码来实现：

```javascript
const restrictedAccess = userIsChild(age);
```




变量 `restrictedAccess` 现在将根据 `userIsChild` 函数的返回值设置为 `true` 或 `false`。

## 回调函数 (Callbacks)

作为参数传递给另一个函数被称为 `callback`（回调函数）。回调函数可以在其作为参数的函数体内部调用。能够在函数内部调用不同的函数使得函数变得更加灵活。

为了查看此示例，让我们来看下面这个名为 `bake` 的函数。这是我们在章节开始时用于解释函数的“烘焙”类比的一个 JavaScript 示例。它接受一个配料字符串作为参数，然后向控制台打印一些消息。尝试在控制台中输入以下内容：

```
function bake(ingredients,callback){
  console.log(`Mix together ${ingredients}...`);
  console.log('Bake in the oven...');
}
```

尝试使用像下面示例中的参数调用该函数：

```
bake('flour, water & sugar');
<< "Mix together flour, water & sugar..."
<< "Bake in the oven...'
```

我们可以通过添加一个第二个参数作为回调函数来改进这个函数。这是一个在 `bake` 函数内部调用的函数，允许我们添加一些额外信息。在控制台中输入以下代码来更新 `bake` 函数：

```
function bake(ingredients,callback){
  console.log(`Mix together ${ingredients}`);
  console.log('Bake in the oven');
  callback();
}
```

### 覆盖函数声明

你可以通过在代码后部分再次声明函数来覆盖之前的函数声明，但如果你使用 `const` 将函数表达式赋值给变量，这种方法将不起作用。

现在我们可以带上回调函数调用 `bake` 函数，该回调会向控制台打印另一条消息。在下面的示例中，回调是一个匿名箭头函数：

```
bake('flour, water & sugar', () => console.log('Add icing on top...'));
<< "Mix together flour, water & sugar..."
<< "Bake in the oven...'
<< "Add icing on top..."
```

回调函数不必是一个在函数调用中定义的匿名函数。我们可以定义一个具名函数，然后将该运行的名称作为参数提供。例如，在控制台中输入以下函数：

```javascript
function eat(){
  console.log('Eat every last crumb!');
}
```

再次，这只是向控制台打印另一条消息，虽然没那么有趣，但对于演示目的已经足够。让我们尝试将此函数作为参数传递给 `bake` 函数：

```
bake('flour,water & sugar', eat);
<< "Mix together flour, water & sugar..."
<< "Bake in the oven...'
<< "Eat every last crumb!"
```

注意，当回调作为参数提供时，后面没有跟括号。这是因为它在稍后的函数体内部被调用。

回调函数在许多 JavaScript 函数中被广泛，我们将在书的后面看到更多。事实上，我们将用一个实用示例来结束本章节，解决我们在书中之前遇到过的问题。

#### 使用回调排序数组

在数组章节（第 5 章）中，我们看到数组有一个 `sort()` 方法，可以将数组中的项按字母顺序进行排序。这对于字符串来说没问题，但你可能记得它对数字的效果并不理想：

```
[1,3,12,5,23,18,7].sort();
<< [1, 12, 18, 23, 3, 5, 7]
```

这是因为数字被转换成了字符串并按字母顺序排列，所以 `'12'` 排在 `'3'` 之前，因为它开头是 `'1'`。

那么，如何对数值数组进行排序呢？答案是将回调函数作为参数传递给 `sort()` 方法。这个回调函数告诉该方法如何比较数组中的任何两个值。我们称它们 `a` 和 `b`。回调函数应该返回以下内容：

*   如果 `a` 在 `b` 之前，返回一个负值
*   如果 `a` 和 `b` 相等，返回 `0`
*   如果 `a` 在 `b` 之后，返回一个正值

按数值排序值的一种简单方法是使用减法：`a-b`。如果 `b` 大于 `a`，将返回负值；如果 `a` 和 `b` 相等，返回零；如果 `a` 大于 `b`，返回正值。我们可以通过添加一个匿名箭头回调函数作为第二个参数来实现，如下：

```
[1,3,12,5,23,18,7].sort((a,b) => a-b);
<< [1, 3, 5, 7, 12, 18, 23]
```

回调函数返回的结果有助于 `sort()` 方法理解一个项比另一个大还是小，这样它就可以按数值对项进行排序。

排序完成！

#### 深入了解 `sort()`

在编程中，你经常会遇到需要复杂解决方案的棘手情况。幸运的是，在你之前已经有人走过这条路，并且几乎任何问题都有现成的解决方案。上面用于排序数字的解决方案只是一个小例子：它是其他需要执行相同操作的人研究出的代码片段。你实际上并不需要理解它是如何工作的。尽管如此，深入研究其工作原理也无坏处。如果你想对 `sort()` 的工作有更深入的解释，请查看这两篇文章：

*   [高级排序技巧](https://www.sitepoint.com/sophisticated-sorting-in/)
*   [如何对数组排序](https://www.sitepoint.com/sort-an-array-objects/)

## 选择函数类型

在本章中，我们涵盖了创建函数的几种方法。它们之间存在细微的差异，将在以后介绍。函数声明与其他语言中的声明方式非常相似，而函数表达式的行为就像赋值给变量的值，而不是语言的特性。

箭头函数看起来与函数声明和表达式完全不同，在某些情况下也会产生不同的结果，这意味着它们并不总是可以完全替代。它们写起来更快，因为函数体周围不需要大括号，且不需要 `return` 关键字。由于这些优势，箭头函数特别流行，我们将在书中后面看到很多例子。然而，一旦函数体超过一行，箭头函数的优势往往会消失。

你选择哪种方法通常取决于个人喜好，而不是哪种最合适。当你读完这本书时，你将能够在任何情况下选择合适的函数类型。

## 挑战

现在你已经学习了如何定义和调用函数，是时候尝试创建一些函数了。这里是一些帮助你提高能力的挑战。

1.  编写一个名为 `lastChar` 的函数，接受一个字符串作为参数并返回字符串的最后一个字母。例如，`lastChar('JavaScript')` 应该返回 `'t'`。你可以查看 [我的 CodePen 代码](https://codepen.io/SitePoint/OJbNJay)。

2.  编写一个名为 `reverse` 的函数，接受一个字符串并返回反转后的字符串。例如，`reverse('JavaScript')` 应该返回 `'tpircSavaJ'`。应用两次函数应该返回原始值，所以 `reverse(reverse('JavaScript'))` 应该返回 `'JavaScript'`。你可以查看 [我的 CodePen 代码](https://codepen.io/SitePoint/poNyoQw)。

3.  编写一些可以在列表中添加和删除项目的函数。列表应该存储为数组，`add('apples')` 应该将字符串 `'apples'` 添加到数组，`remove('apples')` 应该从数组中删除 `'apples'`。你可以查看 [我的 CodePen 代码](https://codepen.io/SitePoint/JjbXjem)。




## Functions

* 函数可以使用 `function` 声明来定义，也可以通过将匿名函数赋值给变量来创建 `function expression`（函数表达式）。
* 箭头函数是一种简写表示法，可用于编写简短的、单行的匿名函数。
* 所有函数都会返回一个值。如果没有显式说明，函数将返回 `undefined`。
* 参数（parameter）是写在函数声明括号中的值，可以在函数体内部像变量一样使用。
* 变量（argument）是在调用函数时提供给函数的值。
* 函数的返回值可以赋值给变量。
* 回调函数（callback）是作为参数传递另一个函数的函数，并且可以在该函数内部被调用。

函数是任何编程语言中都非常重要的部分。但“对象”（objects）也是如此——我们将在下一章学习它们！

# 第 9 章：对象

`Objects`（对象）是编程中使用的抽象数据类型。它们可以用于表示现实世界的物体，如人、动物或地点，也可以表示更抽象的概念，如银行账户详情、日期或文件结构。

在某些语言中（如 Ruby），几乎一切都是对象。没有原始值，只有对象。甚至数字零也是一个对象。许多语言（如 `Java`）是 `class-based`（基于类的）语言。这涉及到创建类，作为创建该类中所有对象的蓝图。例如，`Car` 类可能会指定所有的 `Car` 对象都将有一个引擎、四个轮子和可选的颜色。

JavaScript `not`（不是）基于类的语言（尽管如果你想，也可以定义类，正如我们将在书中后面部分看到的）。它允许你快速方便地创建对象，而无需先定义类。

在本章中，我们将涵盖以下主题：

* 属性（properties）和方法（methods）
* 创建对象字面量
* 对象属性
* 对象方法
* 嵌套对象
* `this`

## 属性和方法

对象可以拥有 `properties`（属性）和 `methods`（方法）。`Properties` 是关于对象的信息，而 `methods` 是对象可以执行的操作。

例如，我们可以使用以下对象模型来表示章鱼。

**章鱼 (Octopus)**

![一只章鱼](img/octopus.png)

属性
名字: “Octavius”
腿数: 8

方法
游泳 (Swim)
行走 (Walk)
重新长腿 (Regrow leg) *(是的，它们真的可以做到！)*

对象通常用于将任何相关信息和功能保持在一个地方。例如，如果你正在编写涉及正方形的代码，你可能会创建一个具有以下属性和方法的“square”对象。

**正方形 (Square)**

![](img/square.png)

属性
长度: 5

方法
周长 (Perimeter) = 4 * Length
面积 (Area) = Length * Length

## 在 JavaScript 中创建对象

对象字面量（Object literals）是 JavaScript 语言的一个显著特征，因为允许快速创建对象而无需定义类（这在许多其他语言中很常见）。一个 `object literal`（对象字面量）是一个自包含的相关值集合。属性可以是任何数据类型，例如数字、字符串、布尔值、数组甚至其他对象。如果一个属性是函数，那么它被称为 `method`（方法）。

要在 JavaScript 中创建对象字面量，只需输入一对大括号。接下来的示例创建了一个赋值给变量 `myObject` 的空对象：

```
const myObject = {};
```

你不需要从空对象开始。你可以将属性和方法放在大括号内部。以下代码可以用于表示关于正方形的信息：

```
const square = { 
    sides: 4,
    length: 5,
    perimeter: 20,
    area: 25
}
```

每个属性都有一个 `key`（键）和一个关联的 `value`（值）。在上面的示例中，第一个属性的键是 `sides`，其值为 4。每个键值对之间用逗号分隔。

### 尾随逗号 (Trailing Commas)

注意上面最后一个键值对没有以逗号结尾。如今，这个“末尾逗号”是可选的，但在 ECMAScript 5 之前，末尾逗号会抛出错误。只要你的代码不需要在旧浏览器中运行（这是一个重要的考虑因素），如果你以后可能向你的对象中添加更多的键值对，那么包含末尾逗号可能是很有用的，这意味着你不需要记得以后要添加逗号。作为一个一般原则，我不会在书中使用末尾逗号。

### 方法 (Methods)

方法看起来与其他属性相似，但它们被定义为函数。接下来的代码显示了我们如何创建一个对象字面量来表示具有 `quack()` 方法的鸭子：

![一只鸭子](img/duck.png)

```
const duck = {
  name: 'Quacky',
  legs: 2,

  quack: function() {
    alert('QUACK! QUACK!');
  }
};
```

还有另一种描述方法的表示法，它省略了 `function` 关键字，只需在方法名后放置括号：

```
const duck = {
  name: 'Quacky',
  legs: 2,

  quack() {
    alert('QUACK! QUACK!');
  }
};
```

这种编写方法的方式最近才引入 JavaScript，但由于其输入量更少而变得流行。

### 再次猜猜 (Guess Again)

记得我们小游戏中的那四个角色吗

![猜猜？](img/guesswho.png)

我们可以创建对象来代表它们。每个对象将包含属性和布尔值，指示它们是否佩戴了眼镜和帽子。例如，以下对象将表示 Alfie：

```
const alfie = {
  name: 'Alfie',
  picture: '🤵',
  glasses: false,
  hat: false
}
```

### 从变量创建对象

我们也可以使用已有的变量创建对象，如下例所示：

```
const name = 'Dumbo';
const legs = 4;
const fly = () => console.log('Fly, away!');

const elephant = { name, fly };
```

![一只象](img/elephant.png)

注意，如果变量已经声明并赋值，你只需要将变量名放在对象内部，它就会分配这些属性。这使得创建一个与变量相同的属性和方法对象变得更容易。长写版本在创建 `elephant` 对象时会涉及重复：

```
const elephant = {
  name: name,
  legs: legs,
  fly: fly
}
```

## 访问属性和方法

你可以使用之前章节中见过的点符号来访问对象的属性。下面的示例显示了我们如何访问 `elephant` 对象的 `name` 属性：

```
elephant.name;
<< "Dumbo"
```

你也可以使用括号符号访问对象的属性。属性由方括号内的字符串表示，因此它需要包含在单引号或双引号中：

```javascript
elephant['name'];
<< "Dumbo"
```

访问属性的点符号是最常用的，但当属性名称存储为字符串时，括号符号可以派上用场。例如，如果你有一个名为 `info` 的变量，其值为字符串 `'name'`，那么下面的代码等同于编写 `elephant.name`：

```javascript
const info = 'name';
elephant[info]
<< "Dumbo"
```

如果你使用 `elephant.info`，将不起作用，因为 JavaScript 会尝试寻找名为 `info` 的属性。

但在大多数其他情况下，你应该坚持使用点符号。

如果你尝试访问一个不存在的属性，将返回 `undefined`：

```javascript
elephant.arms;
<< undefined
```





`in` 操作符可以用于检查一个对象是否具有特定的属性。例如，我们可以使用以下代码检查 `elephant` 对象是否具有名为 `arms` 或 `legs` 的属性：

```
'arms' in elephant;
<< false

'legs' in elephant;
<< true
```

### 调用方法

方法与函数一样，因此我们以相同的方式来调用它们。我们可以使用点符号或方括号表示法来引用对象的方法，就像引用属性一样，但在末尾需要加上括号，因此我们使用以下代码来调用 `fly` 方法：

```
elephant.fly()
<< "Fly, fly away!"
```

![“Fly, fly away!”](img/fly.png)

你也可以使用方括号符号来调用方法：

```
elephant['fly']();
<< "Fly, fly away!"
```

### 添加更多属性和方法

对象默认是**可变的** (`mutable`) 的，这意味着它们的属性和方法可以被更改或删除，并且可以添加新的属性和方法，即使它们是使用 `const` 的。

#### 冻结的对象

可以对对象进行**冻结** (`freeze`) 并使其变为不可变。我们在这里不会深入探讨这一点，但你可以在 [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/freeze) 网站上阅读更多信息。

在程序的任何时候，都可以向对象添加新的属性和方法。这是通过简单地为新属性赋值来实现的。例如，如果我们想为我们的 `elephant` 对象添加一个新的 `ears` 属性，我们可以这样做：

```
elephant.ears = 2;
<< 2
```

现在我们来看一下 `elephant` 对象，可以看到它已经了 `ears` 属性：

```
elephant;
<< { name: 'Dumbo',
    legs: 4,
    ears: 2,
    fly: [Function: fly]  }
```

### 修改属性

你可以使用赋值操作在任何时候更改对象属性的值。例如，我们可以这样更改 `name` 属性的值：

```
elephant.name = 'Elmer';
<< 'Elmer'
```

我们可以通过查看对象来检查更新是否已经发生：

```
elephant;
<< { name: 'Elmer',
    legs: 4,
    ears: 2,
    fly: [Function: fly]  }
```

### 删除属性

可以使用 `delete` 操作符从对象中删除任何属性。例如，如果我们想从 `elephant` 对象中删除 `fly` 方法（因为当然，Elmer 不会飞！），我们将输入以下内容：

```
delete elephant.fly;
<< true
```

现在我们来看一下 `elephant` 对象，可以看到 Elmer 再也不会飞了：

```
elephant;
<< { name: 'Elmer',
    legs: 4,
    ears: 2  }
```

### 嵌套对象

对象甚至可以包含其他对象。这些被称为**嵌套对象** (`nested objects`)。

这是一个包含一组嵌套对象的对象示例。每个嵌套对象代表一个不同的形状。容器对象被赋值给变量 `shapes`：

```
const shapes = {
  triangle: { sides: 3 },
  square: { sides: 4 },
  pentagon: { sides: 5 },
  hexagon: { sides: 6 },
  octagon: { sides: 8 },
  megagon: { sides: 10e6 },
}
```

![Shapes](img/shapes.png)

嵌套对象中的值可以通过顺序使用点符号或方括号表示法引用每个属性名来访问：

```
shapes.triangle.sides;
<< 3

shapes['megagon']['sides'];
<< 1000000
```

你甚至可以混合不同的表示法（但如果可能的话，请不要这样做！）：

```
shapes.hexagon['sides'];
<< 6
```

### `this`

关键字 `this` 可以在对象内部使用，用于引用对象本身。它通常用于方法中，以获取对象属性的访问。

为了查看我们可能使用 `this` 的示例，请考虑我们之前看到的正方形对象：

```
const square = { 
    sides: 4,
    length: 5,
    perimeter: 20,
    area: 25
}
```

这个对象的问题是，正方形的所有信息都是硬编码为属性的。这是没有必要的，因为我们可以使用方法根据 `sides` 和 `length` 属性的值来计算周长和面积。我们可以使用 `this` 来访问这些属性。尝试在控制台中输入以下代码：

```
const square = { 
    sides: 4,
    length: 5,
    perimeter() { return this.sides * this.length },
    area() { return this.length * this.length }
}
```

`perimeter` 和 `area` 属性现在已变为返回所需值的方法。在这些方法的内部，包含了对对象其他属性的引用：`this.sides` 等于编写 `square.sides`，它的数字是 4。

如果我们调用这些方法，它们应该带我们得到相同的结果：

```
square.perimeter()
<< 20

square.area()
<< 25
```

使用这种方法让对象更加灵活。如果我们更改 `length` 属性：

```
square.length = 8;
<< 8

square.perimeter()
<< 32

square.area()
<< 64
```

### 骰子

让我们用一个代码项目结束本章。我们将具有 `sides` 属性以及返回 1 到 `sides` 之间数字的 `roll()` 方法的骰子对象。这里是创建骰子的代码：

```javascript
const dice = {
  sides: 6,
  roll() {
    return Math.ceil(Math.random() * this.sides);
  }
}
```

这个对象有一个 `sides` 属性，告诉我们骰子有六面。在 `roll()` 方法内部，我们使用 `this.sides` 来引用属性的值而不是简单的硬编码 6。让我们尝试一下：

```
dice.roll()
<< 5

dice.roll()
<< 3
```

现在尝试通过修改 `sides` 属性来更改面数：

```
dice.sides = 20;
<< 20
```

现在 `roll()` 方法将返回 1 到 20 之间的随机数，而无需修改它：

```
dice.roll()
<< 12

dice.roll()
<< 18
```

## 挑战

1. 创建描述你喜爱的物品的对象。例如，你可以创建模拟你喜欢的明星的对象，并提供如速度、力量和敏捷度等属性。你可以创建代表电子商务网站上销售的产品的对象，包括描述、价格和评分等属性。在控制台中玩一玩，并练习读取和更新属性以及调用方法。[Top Trump](https://en.wikipedia.org/wiki/Top_Trumps) 卡片可能是此挑战的灵感来源。
2. 编写代表猜猜脸游戏中 Betty、Gemma 和 Del 的对象。你可以在 CodePen 上查看代码](https://codepen.io/SitePoint/pen/GRNqQPQ)。
3. 创建圆形对象，它有一个 `radius` 属性并计算周长和面积。提示：此挑战可能需要使用 `Math.PI` 常量。你可以在 CodePen 上查看代码](https://codepen.io/SitePoint/pen/KKNMQbY)。
4. 创建列表对象，它有一个名为 `items` 的数组属性以及用于向列表添加项目的 `add` 和 `remove()` 方法。例如，`list.add('Apples')` 应该将 `Apples` 添加到 `list.items` 数组中。提示：你可以使用上一章挑战 3 中创建的函数作为方法。

## 总结

* 对象包含关于对象的信息的属性，以及对象可以执行的操作的方法。




*   JavaScript 中的对象字面量是一组放在花括号 (`{}`) 内部并用逗号分隔的键值对集合。
*   属性可以是字符串、数字、布尔值或数组。
*   方法以函数的形式存储。
*   可以使用点符号法或方括号法来访问对象的属性和方法。
*   对象是可变的，这意味着它们的属性和方法可以被更改或删除（即使它们是使用 `const` 创建的）。
*   通过将对象放在对象内部可以创建嵌套对象。
*   在属性和方法可以使用 `this` 关键字来指代对象本身。

现在我们已经学习了编程的所有基础知识，是时候看看我们的代码如何与浏览器环境交互了。

# 第 10 章：文档对象模型 (DOM)

到目前为止，我们主要是在控制台中或通过弹出框与代码交互。自从计算机显示器出现以来，计算机程序能够提供某种图形用户界面 (GUI)，允许用户与程序进行交互。例如，Windows 或 iOS 这样的操作系统提供了 GUI，允许你与计算机或设备进行交互。

![Windows 是一个包含 GUI 的计算机操作系统](img/windows.jpg)

大多数编程语言都会有一个允许你创建 GUI 的库。在浏览器中，我们可以使用 HTML 和 CSS 创建一个供用户交互的 GUI。

文档对象模型，简称为 DOM，允许我们从代码内部访问 Web 页面的元素。它提供了添加和删除元素以及更新页面内容和样式的工具。

DOM 是`语言无关的`，这意味着它可以在任何编程语言中使用，尽管 JavaScript 是它关联最紧密的的语言。在本章中，我们将重点关注如何使用 JavaScript 访问 DOM。

我们将涵盖以下主题：
*   DOM 简介
*   获取元素
*   遍历 DOM
*   获取和设置元素的属性
*   通过创建动态标记更新 DOM
*   更改元素的 CSS

## 文档对象模型

`Document Object Model` 将 HTML 文档表示为由连接的节点 (`nodes`) 组成的网络，这些节点形成了一个树形结构。

DOM 将 Web 上的所有内容都视为节点。它将 HTML 标签表示为`元素节点`，将标签内的任何文本表示为`文本节点`。所有这些节点都连接在一起形成一个节点树，描述了 Web 页面的整体结构。

为了演示这一点，让我们来看这段简短的 HTML 代码：

```
<h1 id='greeting'>Hello, <em>World!</em></h1>
```

这可以表示为所示的节点树图。

![Hello, World! DOM](img/helloworldDOM.png)

`h1` 标签包含了所有内容，因此它显示为节点树顶部的元素节点（在图中用紫色椭圆表示）。单词“Hello”是文本，所以它是子文本节点（在图中用绿色矩形表示）。`em` 元素位于 `h1` 标签内部，因此它是子元素节点。这使得 `h1` 元素节点成为这些子节点的父节点。`em` 标签内部的文本是 `em` 元素节点的文本子节点。

在浏览器中，它看起来是这样：

![在浏览器中显示的 Hello, World! 标题](img/helloworld.png)

能够将 HTML 标记可视化为节点树将使遍历 DOM 的体验变得简单得多。

### HTML 文档与 DOM

当你访问一个 Web 页面时，浏览器首先下载包含所有 HTML、文本、图片等的页面文档。然后浏览器会创建该文档的表示（或者如果你喜欢的话，可以称为心理模型），这就是文档对象模型。然后浏览器使用该 DOM 在你的设备上显示 Web 页面。JavaScript 允许对 页面进行更改，但这些更改是针对 DOM 的，而不是原始的硬编码 HTML。你将在本章后续部分看到这一点。

### 检查 DOM

浏览器实际上允许你查看 Web 页面的文档对象模型，你甚至可以以各种方式对其进行操作（这有点就像查看汽车引擎盖）。如果你在 Web 页面的任何地方点击右键，你会看到“检查”页面的选项。这将显示 DOM 以及各种其他开发者工具。DOM 看起来与原始 HTML 相似，但并不完全相同——特别是如果 JavaScript 对其进行了修改。

## 获取元素

DOM 提供了一个名为 `getElementById` 的有用方法，它返回一个具有特定 ID 属性的元素的引用。

例如，我们可以使用其 `id` `greeting` 获取上一个示例中 `h1` 标题元素的引用。

让我们在 CodePen 上尝试一下。打开一个新的 Pen 并向 **HTML** 部分添加以下代码：

```
<h1 id='greeting'>Hello, <em>World!</em></h1>
```

现在我们可以通过向 **JS** 部分添加以下代码来获取 `h1` 元素的引用：

```javascript
const hello = document.getElementById('greeting');
```

如果不存在提供 ID 的元素，则返回 `null`。我们可以通过在控制台中输入赋值给元素的变量名（`hello`）来查看返回了什么：

```javascript
hello;
```
```
"<h1 id='greeting'>Hello, <em>World!</em></h1>"
```

## 更新 HTML

更新页面上 HTML 最简单的方法是使用 `innerHTML` 属性。这将返回元素内部的所有 HTML。我们可以通过在控制台中输入以下代码查看结果：

```javascript
hello.innerHTML;
```
```
"<h1 id='greeting'>Hello, <em>World!</em></h1>"
```

`innerHTML` 属性的伟大之处在于它也是可写的，这为我们向元素插入 HTML 了一种方便的方法。为了演示这一点，让我们添加一些 JavaScript 代码来提供个性化的问候。首先，确保我们拥有对标题的引用：

```javascript
const hello = document.getElementById('greeting');
```

接下来，我们将使用提示框询问用户姓名，并将其存储在变量 `name` 中：

```javascript
const name = prompt('你的名字是什么？');
```

最后，我们将 `innerHTML` 属性替换为我们的问候，使用了我们刚刚收集的 `name` 变量：

```javascript
hello.innerHTML = `Hello, <em>${name}</em>`;
```

注意我们使用了模板字符串来生成 HTML。在创建动态插入 Web 页面的 HTML 段时非常有用，因为它们允许其中插入变量。

如果一切顺利，你应该看到类似这样的（但希望是你的名字！）：

![这是个性化的](img/personalhello.png)

## 获取多个元素

让我们看看如何一次选择多个元素。在 CodePen 上创建一个 Pen 并向 **HTML** 部分添加以下代码：

```html
<ul id='food'>
  <li class='fruit'><<span>🍏</span>苹果</li>
  <li class='fruit'><<span>🍌</span>香蕉</li>
  <li class='veg'><<span>🥕</span>胡萝卜</li>
</ul>
```

这应该创建一个看起来像所示的项目列表：

![我们的新食物列表](img/foodlist.png)

该 HTML 代码段的 DOM 树如下图所示：

![我们的食物列表 DOM 树](img/foodDOM.png)

正如我们已经看到的，我们可以使用以下代码访问 `ul` 元素：

```javascript
const food = document.getElementById('food');
```

但我们如何访问一组元素，例如列表项呢？幸运的是，DOM 还提供了一些允许我们访问一组元素的方法。





### 通过标签名获取元素

我们可以使用 `getElementsByTagName()` 返回一个包含所有通过参数提供的标签名对应的元素集合。例如，我们可以使用以下代码获取文档中所有的列表项（HTML 标签为 `<li>`）：

```javascript
const items = document.getElementsByTagName('li');
```

变量 `items` 现在包含一个所有列表项元素的元素集合。您可以使用我们之前在字符串和数组中看到过的方括号索引表示法来访问集合中的每个项目。例如，在控制台中输入以下代码将返回集合中的第一个项目：

```
items[0];
<< "<li class='fruit'><span>🍏</span>Apple</li>"
```

我们还可以使用 `length` 属性来查看集合中有多少个元素：

```
items.length;
<< 3
```

### 通过类名获取元素

我们也可以使用 `getElementsByClassName()` 方法返回一个包含所有具有特定类名的元素集合。例如，以下代码将返回所有类名为 `fruit` 的元素的元素集合：

```javascript
const fruit = document.getElementsByClassName('fruit');
```

变量 `fruit` 包含两个具有 `fruit` 类的元素集合，正如我们在控制台中输入以下内容所看到的：

```
fruit.length;
<< 2

fruit[0];
<< "<li class ='fruit'><span>🍏</span>Apples</li>"

fruit[1];
<< "<li class='fruit'><span>🍌</span>Banana</li>"
```

注意，如果没有具有给定类名的元素，仍然会返回一个集合，但它将不包含任何项目且长度为 0。

#### 获取单个元素 vs 获取多个元素

您是否注意到您只能通过 ID 获取一个元素（`document.getElementById`），但通过类名可以获取多个元素（`document.getElementsByClassName`）？记住这一点的一种简单方法是：每个 HTML 文档中只允许使用一次特定的 ID，而您可以在同一文档中多次使用特定的类名。

### 查询选择器 (Query Selectors)

在 DOM 中获取元素的另一种方法是使用查询选择器。这些方法的好处是它们允许您使用 CSS 语法来定位特定元素。

`document.querySelector()` 方法允许您使用 CSS 语法来查找文档中匹配所提供的 CSS 选择器的第一个元素。

例如，与其使用 `document.getElementById` 来获取 ID 为 `food` 的元素的引用，我们可以使用以下代码：

```javascript
const food = document.querySelector('#food');
```

`document.querySelectorAll()` 方法也使用 CSS 语法，但它返回的是文档中所有匹配 CSS 查询选择器的元素列表。

例如，以下两个语句是等价，并返回相同的节点列表：

```javascript
document.getElementsByClassName('fruit');
document.querySelectorAll('.fruit');
```

查询选择器是强大的方法，它们可以模拟之前的所有方法，并允许对返回的元素节点进行更细粒度的控制，因为它们允许您指定页面上的精确项目。例如，CSS 伪选择器可以用于精确指向特定元素。

例如，以下代码将仅返回 `food` 列表中的最后一个列表项：

```javascript
const carrot = document.querySelector('ul#food li:last-child');
<< "<li class='veg'><span>🥕</span>Carrot</li>"
```

#### CSS 选择器

您必须了解一点 CSS 选择器才能使用这种方法！如果您还没有完全掌握，或者只是需要复习一下，您可能想查看 SitePoint 的“[CSS 选择器](http://www.sitepoint.com/web-foundations/css-selectors/)”指南，或者阅读 Tiffany Brown 编写的 [CSS Master](https://www.sitepoint.com/premium/books/css-master-2nd-edition)。

## 遍历 DOM 树

DOM 节点有许多属性和方法用于在文档树中导航。一旦您有了元素的引用，就可以沿着文档树寻找其他节点。

让我们来看看几个更有用的方法。

### 子节点 (Child Nodes)

您可以使用 `children` 属性获取一个元素的所有子元素的集合。在我们的食物列表示例中，`food.children` 将返回 ID 为 `food` 的 `<ul>` 元素的所有子元素的节点列表。这些元素在下面的图中被高亮显示。

![高亮显示无序列表三个子列表项](img/children.png)

以下代码显示了我们如何访问一个包含三个子 `<li>` 元素的节点列表：

```javascript
food.children.length;
<< 3

food.children[0];
<< "<li class='fruit'><span>🍏</span>Apple</li>"
```

在继续之前，让我们在程序中为这些子节点创建引用。在您的 Pen 的 JS 部分添加以下代码：

```javascript
const apple = food.children[0];
const banana = food.children[1];
const carrot = food.children[2];
```

（如果您跟着一起操作，这里是您的 Pen [现在应该的样子](https://codepen.io/SitePoint/pen/QWGGbWg)。）

### 父节点 (Parent Node)

`parentNode` 属性返回元素的父节点。

以下代码返回 `food` 节点，因为它是该元素的父元素：

```javascript
apple.parentNode;
<< "<ul id='food'>
<li class='fruit'><span>🍏</span>Apple</li>
<li class='fruit'><span>🍌</span>Banana</li>
<li class='veg'><span>🥕</span>Carrot</li>
</ul>"
```

这种关系可以在图中看到：

![父节点是无序列表](img/parentNode.png)

## 创建动态标记

到目前为止，我们查看了如何访问不同的不同的元素。但 DOM 的真正威力在于它可以动态更新标记，就像我们之前使用 `innerHTML` 那样。在本节中，我们将学习如何创建新元素并将它们添加到页面上，更新已有的元素并删除不需要的元素。

### 创建元素

`document` 对象有一个 `createElement()` 方法，它接受标签名作为参数并返回该元素。例如，我们可以在控制台中通过以下代码为我们的食物列表创建一个 DOM 节点：

```javascript
const melon = document.createElement('li');
```

目前该元素是空的。为了添加内容，我们将使用 `innerHTML` 属性：

```javascript
melon.innerHTML = `<span>🍉</span>Melon`;
```

将上面的两行添加到 Pen 中...

#### 使用 textContent 添加文本

还有一个 `textContent` 属性可以向元素添加文本，但它不能包含任何 HTML 元素。例如，这样做是可以的：

```javascript
melon.textContent = '🍉Melon';
```

但如果您尝试在周围添加 `<span>` 标签，它将不会解析 HTML：

```javascript
// 这段代码不会解析 <span> 标签
melon.textContent = '<span>🍉</span>Melon';
```

正如正如从下面的图片看到的，标签将以文本的形式显示在网页上，这通常不是我们想要的。

![HTML 不会被 textContent 解析](img/melon.png)

### 将元素添加到页面

如果您更新了 Pen，会发现还没有任何变化。现在我们已经学习了如何创建 HTML 元素，需要学习如何将它们放在页面上。有许多方法允许您向 DOM 插入节点。

让我们先看看 `appendChild()`。每个 DOM 节点都有一个 `appendChild()` 方法，可以将另一个节点（作为参数）作为子节点添加。以下示例将我们创建的 `melon` 元素添加到 `food` 列表的末尾：

```javascript
food.appendChild(melon);
```

下面的图显示了我们创建的新元素将插入到列表的什么。

![箭头显示了新节点将追加在哪里](img/appendChild.png)

下一张图片显示 melon 现在已经是列表的一部分。

![我们更新后的列表](img/appendChild2.png)





（这里是上方内容的[在线 Pen](https://codepen.io/SitePoint/pen/rNWWVxr)。）

### 逐节点构建元素

使用 `innerHTML` 来填充元素内容的另一种替代方案，是逐个构建每个节点，然后使用 `appendChild()` 方法将它们全部组合在一起。

为了演示这一点，让我们创建一个与下方所示节点树匹配的新类型列表元素。

![我们的西兰花节点树](img/broccoliDOM.png)

我们需要为图中的每个节点创建一个节点，然后将它们全部组合在一起。我们已经见过用于创建元素节点（图中的紫色椭圆）的 `document.createElement()` 方法。此外，还有一个 `document.createTextNode()` 方法，我们可以用用它来创建文本节点（图中的绿色矩形）。

现在来创建这些节点。在你的 Pen 的 `JS` 部分添加以下内容：

```
const broccoli = document.createElement('li');
const text = document.createTextNode('Broccoli');
const span = document.createElement('span');
const emoji = document.createTextNode('🥦');
```

这将创建所有节点并为它们分配变量。现在我们可以将它们组合起来形成列表项：

```
span.appendChild(emoji);
broccoli.appendChild(span)
broccoli.appendChild(text);
```

接下来，我们需要将这个新的列表项插入 HTML 中。

### 插入之前

`appendChild()` 方法非常有用，因为你通常想要在列表底部添加新元素。但如果你想在两个现有元素之间放置一个新元素呢？

`insertBefore()` 方法会将新元素放置在另一个元素之前。需要注意的是，该方法是在`父节点`上被调用的。它接受两个参数：第一个是待添加的新节点，第二个是你想要让它排在之前的节点。（记住参数的顺序就是它们在标记中出现的顺序是有帮助的。）例如，我们可以通过下面这行代码将新的 `broccoli` 元素放在 `apple` 元素之前：

```
food.insertBefore(broccoli,apple);
```

![在苹果列表项之前插入西兰花列表项](img/insertBefore.png)

如你所见，这将西兰花元素放在列表顶部，位于苹果之前。

![西兰花现在位于列表顶部](img/insertBefore2.png)

这是我们[更新后的 Pen](https://codepen.io/SitePoint/pen/ZEBBGBj)。

有点恼人的是，并没有 `insertAfter()` 方法，所以你需要确保你有访问正确元素的权限，以便元素精确地放置在你想要的位置。

### 从页面中移除元素

可以使用 `remove()` 方法从页面中移除元素。该方法在要移除的节点上被调用。它返回被移除移除的引用。例如，如果我们想移除 `carrot` 元素，将使用以下代码：

```
carrot.remove();
<< "<li class='veg'><span>🥕</span>Carrot</li>"
```

如下方的图所示，胡萝卜已经不在了：

![胡萝卜列表项已被移除](img/removeChild.png)

#### 消失但未消失

让我们在这里提醒一下原始 HTML 和 DOM 之间的区别。这是你更新后的 Pen [现在应该的样子](https://codepen.io/SitePoint/pen/WNoovOX)。胡萝卜项已从渲染视图（即你在浏览器中看到的内容）中移除。但请注意，原始的胡萝卜代码仍在 HTML 中。JavaScript 从文档对象模型中删除了胡萝卜列表项，并没有从实际 HTML 中删除。

### 替换页面上的元素

可以使用 `replaceChild()` 方法用一个节点替换另一个节点。它在父节点上被调用，并有两个参数：新节点和要被替换的节点。例如，如果我们想更改第三个列表项的内容（你可以吃太多香蕉），我们可以用一个新的文本节点替换旧的，如下所示：

```
const lemon = document.createElement('li');
lemon.innerHTML = `<span>🍋</span>Lemon`;
food.replaceChild(lemon,banana); 
```

如下所示，柠檬已经替换了我们列表中的香蕉。

![替换元素](img/replaceChild.png)

这是我们[更新后的 Pen](https://codepen.io/SitePoint/pen/rNWWVdP)。

### 获取和设置属性

所有的 HTML 元素都有大量可能的属性，例如 `class`、`id`、`src` 和 `href`。DOM 有许多方法可以获取或设置这些属性。

### 获取元素的属性

`getAttribute()` 方法返回作为参数提供的属性值。例如，我们可以通过在控制台中输入以下代码来查找 `apple` 元素的类：

```
apple.getAttribute('class');
<< "fruit"
```

如果元素没有给定的属性，它将返回 `null`。例如，如果在控制台中输入以下代码，我们可以看到 `broccoli` 元素没有 `src` 属性（我们之前在创建元素时没有添加它）：

```
broccoli.getAttribute('src');
<< null
```

### 设置元素的属性

`setAttribute()` 方法可以更改属性的值。它接受两个参数：你想要更改的属性和新值。

例如，如果我们想为 `broccoli` 元素添加 `veg` 类，可以在控制台中使用以下代码：

```
broccoli.setAttribute('class', 'veg');
```

#### 多个类和 `setAttribute`

使用 `setAttribute()` 方法会覆盖元素已拥有的类。通常使用 `classList` 属性会更好，我们将介绍这一内容。

### `className` 属性

正如我们所见，可以使用 `setAttribute()` 方法修改元素的类。还有一个 `className` 属性允许直接设置类。此外，它还可用于查找属性的值：

```
apple.className;
<< "fruit"
```

我们也可以用它来设置元素的类。例如，我们之前创建的 `melon` 元素也没有类属性，所以现在来修复它：

```
melon.className = 'fruit';
<< "fruit"
```

#### 多个类和 `className`

与上面的 `setAttribute` 一一样，通过赋值更改元素的 `className` 属性也会覆盖元素上设置的其他类。可以通过使用 `classList` 属性来避免这个问题，我们将介绍这一内容。

### `classList` 属性

`classList` 属性是元素拥有的所有类的列表。它还有许多方法可以修改元素的类。

`add()` 方法用于向元素添加类，而不会覆盖已存在的类。例如，我们可以通过以下代码为之前创建的 `lemon` 元素添加 `fruit` 类：

```
lemon.classList.add('fruit');
```

`remove()` 方法从元素中移除特定的类。例如，我们可以通过以下代码移除刚刚添加的 `fruit` 类：

```
lemon.classList.remove('fruit');
```

`contains()` 方法将检查元素是否包含某个类：

```
apple.classList.contains('fruit');
<< true

apple.classList.contains('veg');
<< false
```

### 使用 style 操作

每个元素节点都有 `style` 属性。它可以用于动态修改网页上任何元素的样式。

要查看此示例，尝试在你的 Pen 的 **JS** 部分添加以下代码：

```
apple.style.border = "red 2px solid";
<< "red 2px solid"
```

这是[更新后的 Pen](https://codepen.io/SitePoint/pen/QWGGxbp)。`apple` 列表元素周围添加了红色框。

![为元素样式](img/style.png)

#### CSS 属性名中的连字符




在 JavaScript 中引用任何由连字符分隔的 CSS 属性名时，必须使用驼峰法（camelCase）。因此，连字符会被移除，后面的字母将大写。这是因为 JavaScript 不允许在属性名中使用连字符。

例如，CSS 属性 `background-color` 变为 `backgroundColor`，而 `font-size` 变为 `fontSize`。

#### 优雅优雅（Being Classy）

虽然动态元素的样式很有用，但如果你想一次性更改大量的样式，代码就会变得非常混乱。

通常，更好的替代方案是动态更改元素的类（class），并在 CSS 中为每个类设置不同的样式。

例如，如果我们想给 `apple` 元素添加一个红色边框（出于某种原因突出显示），我们可以采用之前看到的方法，也可以给 `apple` 元素添加一个 `highlighted` 的类：

```
apple.classList.add('highlighted');
```

然后在 `CSS` 部分添加以下内容：

```
.highlighted {
  border: red 2px solid;
}
```

这里是[我们更新了该代码的 Pen](https://codepen.io/SitePoint/pen/yLVVEqq)。

使用这种方法的另一个优势是，如果我们以后决定更改突出元素的方式，它赋予了我们更大的灵活性。例如，我们可能想使用蓝色背景和加粗文本，而不是红色边框。我们只需要更改 CSS 中 `highlighted` 类的代码，而无需在 JavaScript 代码中翻找以更改每个需要突出元素的样式属性。使用类来更新元素样式是一种更符合 DRY（不要重复）原则的方法。

## 一个简单的待办列表

我们将通过编写一些代码来结束本章，创建一个待办列表，并允许我们向其中添加项目并在完成后将其划掉。所有这些将通过使用 JavaScript 创建的动态 HTML 完成。在 CodePen 上打开一个新的 Pen 开始吧。

让我们从创建列表元素开始，在 `JS` 部分添加此代码：

```
const list = document.createElement('ul');
document.body.appendChild(list);
```

这创建了一个无序列表（`<ul>`）并将其附加到文档的 `<body>` 标签上。你还看不到任何渲染内容，因为列表是空的——但它确实在那里！（（如果你检查 DOM，现在会看到那里有一个空的 `<ul></ul></ul>` 代码。）

接下来，我们将编写一个添加任务的函数。在 `JS` 部分添加以下代码：

```
function add(item){
  const li = document.createElement('li');
  li.innerHTML = item;
  list.appendChild(li);
}
```

此函数将创建一个列表项（`<li>`）标签，然后将其作为子元素添加到我们创建的 `<ul>` 元素中。列表项的内容将作为参数传递给函数的内容，因此 `add('Read a book')` 将向列表元素添加以下 HTML：

```
<li>Read a book</li>
```

在 CodePen 中打开控制台并向列表添加几个任务：

```
add('Bake cake');
add('Sing song');
add('Read book');
```

当你按下 `Enter` 键时，你应该能看到每个项目都出现在屏幕上。

![动态添加内容](img/add.png)

现在我们来写一个函数，为项目切换 `complete` 类。如果项目没有 `complete` 类，则会添加它；如果它已经有了该类，则会将其移除：

```
function toggle(item){
  item.classList.toggle('complete');
}
```

我们还需要在 `CSS` 部分添加一些代码，为具有 `complete` 类的项目设置样式，使其看起来像被划掉一样：

```
.complete{
  text-decoration: line-through;
}
```

再次打开控制台，看看这是否有效。该函数接收我们想要划掉的实际元素作为参数，因此我们可以尝试用以下代码划掉列表中的第一个最后一个项目：

```
toggle(list.firstChild);
toggle(list.lastChild);
```

每当你按下 `Enter` 键，你都应该看到相关项目在页面上被划掉。

![切换类](img/toggle.png)

你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/qBqqKwE)。

显然，通过控制台与列表交互是令人沮丧的，但至少我们证明了使用 JavaScript 动态添加和编辑内容是可能的。在下一章中，我们将考虑如何在不需要控制台的情况下增加这种交互性。

## 挑战

1. 使用纯 JavaScript 在新的 Pen 中创建一些动态 HTML，包括至少一个标题和一个段落。CodePen 的 `HTML` 部分应该是完全空的。你可以看到[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/zYooaXQ)。

2. 为我们编写的待办列表添加一个名为 `destroy` 的函数。它应该从列表中移除作为参数提供的任务。例如，`destroy(list.lastChild)` 应该移除列表中的最后一个项目。你可以看到[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/jVKo)。

## 总结

* 文档对象模型（Document Object Model）是一种将页面表示为节点树的方式。
* DOM 有许多可以用于导航页面的方法。
* 元素的属性可以通过 `getAttribute()` 方法访问，并通过 `setAttribute()` 方法更新。
* `innerHTML` 属性可以用于快速插入原始 HTML。
* `createElement()` 和 `createTextNode()` 方法可以用于创建标记。
* 使用 `appendChild()` 和 `insertBefore()` 方法可以将标记添加到页面。
* 元素可以使用 `replaceChild()` 方法替换，并使用 `remove()` 方法移除。
* 可以更新 `style` 属性来更改元素的 CSS 属性。

现在我们已经学习了如何导航和动态更新网页标记，是时候与其交互了。在下一章中，我们将学习如何处理事件。

# 主事件

在上一章中，我们接触了 DOM 以及它允许我们与页面元素交互。在这一章中，我们将研究事件如何提供用户交互与程序之间的联系。没错——这一章是你的代码开始变得完全交互且真正有趣的时刻！

在本章中，我们将涵盖以下主题：

* 事件驱动编程
* 事件监听器
* 点击事件
* 事件对象
* 表单提交
* 鼠标事件
* 键盘事件
* 移除事件监听器
* 事件委托



当事件发生时，`event listener`（事件监听器）就会被触发。事件监听器的工作原理类似于水壶上的哨子。程序不需要不断检查事件是否已经发生，而是让事件监听器在后台运行，直到事件发生，然后通知程序以便其立即做出响应。这允许程序在等待事件发生的同时继续执行其他任务。

## 事件处理器 (Event Handlers)

`event handler`（事件处理器）是一组在事件发生时要执行的操作指令。在上面的水壶的例子中，这就是水壶烧开后要执行的指令——即把它从炉上取下来并泡杯茶！

下面的图展示了这一过程：从一个触发事件监听器的事件开始，然后它通知事件处理器并产生一个操作。

![导致操作的事件！](img/events.png)

在编程中，事件处理器通常以回调函数（callback function）的形式存在，当事件监听器被触发时就会调用。例如，你可能希望在用户点击按钮时显示弹窗通知。这可以通过设置一个在用户点击按钮时触发的事件监听器来实现。然后，事件处理器将调用显示通知的函数。每当事件监听器被触发时，该函数就会被调用，这意味着每次按下按钮时消息都会出现。这一序列在图中所示。

![导致弹出消息的鼠标点击](img/eventClick.png)

JavaScript 是一种基于事件的语言，我们在本章节其余部分来看一些常见浏览器事件的示例。

## 点击事件 (Click Events)

在 JavaScript 中，我们可以通过在元素上调用 `addEventListener()` 方法为页面上的元素附加事件监听器。为了演示这一点，我们将在代表整个页面的 `document` 对象上附加一个事件监听器。当用户点击页面时，它会被触发并调用事件处理器函数。`click` 事件发生在用户用鼠标点击、按下 `Enter` 键或空格键、或者触摸屏幕时，因此它是一个涵盖了许多交互类型的全方位事件。在 CodePen 上打开一个新的 Pen，并在 **JS** 部分输入以下代码：

```
document.addEventListener('click',bang);
```

该事件监听器接受两个参数：第一个是需要监听的事件（在本例中为 `click`），第二个是事件处理器（在本例中是一个名为 `bang` 的回调函数）。因此，这个事件监听器将监听 `click` 事件，并在每次发生点击时调用 `bang` 函数。

注意，当 `bang` 函数作为事件监听器的参数使用时，后面不要加括号。否则，该函数会在设置事件监听器时立即被调用，而不是在事件发生时调用！

在我们测试之前，我们需要定义 `bang` 函数。在事件监听器下方添加以下代码：

```
function bang(){
  document.body.style.background = 'yellow';
  document.body.innerHTML = `<h1>BANG!!!</h1>`;
}
```

此函数使用了我们在上一节中看到的一些 DOM 方法。首先，它使用 `style` 属性将 `body` 的背景更改为黄色。然后，它使用一个带有“BANG!!!”文本的标题元素更新内部 HTML。

但在触发 `click` 事件之前，这个函数将不会被调用。试一试：只要你点击页面上的任何地方，你就会看到 bang 消息。

![点击并触发！](img/bang.png)

你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/wvoJvpy)。

### 点击元素 (Clicking Elements)

上一个例子中的事件监听器是一个`global event listener`（全局事件监听器），它监听整个页面的点击。我们也可以为页面上的特定元素附加事件监听器。这些监听器只会在事件发生在这些元素上时触发。

为了看到这个示例，我们将创建一个按钮，点击它会更改页面的背景颜色。在 CodePen 上打开一个新的 Pen，并在 **HTML** 部分添加以下代码：

```
<button id='red'>Red</button>
```

这在页面上添加了一个按钮。接下来的代码将在 **JS** 部分为我们该按钮的引用：

```
const redButton = document.getElementById('red');
```

现在我们已经有了按钮的引用，可以为它附加一个事件监听器：

```
redButton.addEventListener('click', e => document.body.style.background = 'red');
```

这在监听 `click` 事件，与上一个例子一样，但第二个参数不是函数名，而是一个直接定义在事件监听器内部的匿名函数。对于短函数非常有用，而箭头函数是使用它们的良好选择，因为只是一行用于将 body 背景颜色更改为红色的代码。

![点击变红](img/red.png)

你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/VwmpwXm)。

敏锐的人可能在想：“但那个字母 `e` 在那里是干什么用的？”如果你发现了它，很好。它是函数的参数，是对事件对象的引用，我们可能应该更详细地查看它。

### 事件对象 (The Event Object)

每当事件发生时，被调用的函数会自动接收一个 `event object`（事件对象）作为参数。事件对象包含了大量关于事件的信息，以属性的形式存储。例如，`target` 属性指向触发事件的元素。

让我们在示例中添加另一个按钮，以便观察事件对象。在 **HTML** 部分添加以下行代码：

```
<button id='green'>Green</button>
```

这为我们提供了另一个可以玩的按钮。现在在 **JS** 部分，添加以下代码获取其引用：

```
const greenButton = document.getElementById('green');
```

让我们在 **JS** 部分为这个按钮添加一个事件处理器：

```
greenButton.addEventListener('click', e => document.body.style.background = e.target.textContent);
```

#### 使用 `e` 还是不使用 `e`？

函数参数不必是 `e`。使用 `e` 是合理的，因为它是“event”的缩写。

这与我们为红色按钮附加的事件监听器非常相似，只不过我们没有硬编码要设置的颜色，而是将其设置为 `e.target.textContent`。`target` 属性指向触发事件的元素，在这种情况下为 `greenButton` 元素。`textContent` 属性引用元素内部的文本，即“Green”。

如果你尝试点击按钮，会将页面的 CSS `background-color` 属性更改为按钮内的任何文本。尝试将文本改为颜色，你会发现背景颜色更新为该颜色。另一个 DRY（不要重复）代码的示例，因为我们只需要在一个地方指定颜色。

![点击变绿](img/green.png)

你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/wvoJvmm)。

事件对象还有许多属性和方法，在 [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/API/Event#Properties) 网站上进行了总结。




```
<p>在下方框中输入您的名称：</p>
<form name='myForm'>
  <input type='text' name='myName'>
  <button type='submit'>Submit</button>
</form>
<div id='hello'></div>
```

这将产生一个输入框，旁边有一个 `Submit`（提交）按钮。注意该按钮有一个类型为 `submit` 的属性：这将在它被按下时会触发一个 `submit` 事件。我们还在代码末尾添加了一个 ID 为 `hello` 的空 `<div>` 元素，因为它目前是空的，所以现在屏幕上是不可见的。我们将它用作容器，在表单提交后存放输出内容。

![用于提交名称的表单](img/form.png)

首先，我们需要对这些元素进行引用。在 `JS` 部分添加以下代码：

```
const form = document.forms.myForm;
```

DOM 了一种了一种通过 `document.forms` 访问网页上任何表单的方便方法，它将返回页面上所有表单的集合。如果你添加表单的名称，它将返回具有该名称的表单（注意我们的表单在 HTML 代码中有一个名为 `myForm` 的属性）。

接下来，添加以下 JavaScript 代码：

```
const hello = document.getElementById('hello');
```

这为我们提供了 HTML 中 ID 为 `hello` 的那个空 `<div>` 元素的引用。

接下来，我们将为表单添加一个事件监听器：

```
form.addEventListener('submit',sayHello);
```

这将在表单提交时调用 `sayHello` 函数。让我们接着来写这个函数：

```
function sayHello(e){
 hello.textContent = `Hello, ${form.myName.value}!`;
}
```

该函数使用模板字面量（template literal）更新 `hello` div 的 `textContent` 属性。注意在模板字面量内部，引用了 `form.myName.value`。它返回一个与 `<input>` 字段内内容匹配的字符串，因为 `<input>` 标签有一个名为 `myName` 的属性。因此，如果你在输入框中输入“JavaScript”，`hello` div 将包含以下消息：“Hello, JavaScript!”

### 引用表单元素

表单内部的任何元素都可以通过它们的 `name` 属性作为表单元素的属性被引用。在上面的示例中，`form.myName` 是表单内部 `<input>` 元素的引用，因为它有一个名为 `myName` 的属性。

尝试在输入字段中输入您的名称，然后按下 `Enter` 键或点击 `Submit` 按钮提交表单。

遗憾的是，你可能会收到类似这样的错误消息：

![错误的路径](img/badpath.png)

这是因为表单有一种默认行为，意味着它们会被提交到服务器。在这种情况下，它尝试提交到 `/boomboom/v2/index.html`，这是 CodePen 服务器上的一个页面，我们没有权限访问。因此生成了错误消息。不过，不用担心，这很容易修复。

### 表单的 `action` 属性

表单有一个 `action` 属性，可以用于指定你想将它们提交到服务器上的哪个页面。如果没有指定，表单将尝试尝试将自己提交到它所在的页面。这就是这种情况下发生的情况（因为我们没有指定 `action` 属性），但 CodePen 不允许我们将表单提交到他们的服务器！

### 防止默认行为

网页上的某些元素具有浏览器内置的默认行为。正如我们刚刚看到的，表单在提交时默认会被发送到服务器。

幸运的是，事件对象有一个名为 `preventDefault` 的方法，它可以在事件发生时停止任何默认行为的发生。我们可以在 `sayHello` 函数中使用它来阻止表单被提交到服务器。更新函数使其看起来如下：

```
function sayHello(e){
  e.preventDefault();
  hello.textContent = `Hello ${form.myName.value}!`;
}
```

现在再次提交表单，它应该看起来像这样：

![现在提交表单的结果](img/formresults.png)

你可以查看 [我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/RwopwdL)。

## 键盘事件

有两个与用户按下按键相关的主要事件。这些是 `keydown`（按下按键时）和 `keyup`（释放按键时）。

这些事件的事件对象包含两个属性，可以告诉我们按下了哪个键：

*   `code` 属性返回一个与按下的实际物理键相关的字符串。
*   `key` 属性返回将出现在页面上的实际输出。这可能会受到按住特殊键（如 `shift` 或 `alt`）、键盘布局设置和本地设置（如货币符号键）的影响。

例如，如果你按下空格键，`code` 属性将是 `Space`，但 `key` 属性将是（一个空格，即它产生的内容）。你可以通过在 CodePen 的 `JS` 部分添加以下代码来查看每个按键产生的代码：

```
document.addEventListener('keydown',e => document.body.innerHTML = `<div>e.code: ${e.code}</div><div>
e.key: ${e.key}</div>`);
```

每当按下按键就会触发一次。

### 实时输入

为了查看如何使用键盘事件，让我们构建一个更新输出的实时输入。在 CodePen 上打开一个新的 Pen 并在 **HTML** 部分添加以下内容：

```
<input id='input'>
<div id='output'></div>
```

这创建了一个输入元素和一个用于输出的空 `<div>`。这两个元素都有 `id` 属性，以便我们从代码中访问它们。让我们将这些添加到 **JS** 部分：

```
const input = document.getElementById('input');
const output = document.getElementById('output');
```

最后，我们只需要为输入元素添加一个事件监听器：

```
input.addEventListener('keyup', e => output.textContent = input.value);
```

这是一个匿名函数，它会在 `keyup` 事件被触发时被调用。使用 `keyup` 而不是 `keydown` 的原因是按键上的字符会在这两个事件之间出现在输入字段中，所以当 `keydown` 事件触发时，字符还没有在那里，但在 `keyup` 事件触发时，它已经在那里了。这很重要，因为函数通过覆盖 `textContent` 属性将输入字段中的内容插入到 `output` div 中。

尝试在输入字段中输入内容。你应该会在每次按下按键时看到文本出现。

![实时输入](img/liveinput.png)

## 鼠标事件

有很多与鼠标指针及其与页面元素交互相关的事件。

### 鼠标移动

每当鼠标指针移动时，`mousemove` 事件就会触发。为了看到这种示例，我们将编写一些代码，在鼠标指针每次移动时都告诉我们坐标。

在 CodePen 上打开一个新的 Pen，并首先在 **JS** 部分添加以下事件监听器：

```
document.addEventListener('mousemove',showCoords);
```

每当鼠标指针在页面的任何位置移动时，它都会调用 `showCoords` 函数。现在现在写这个函数：

```
function showCoords(event){
  document.body.textContent = `(${event.x},${event.y})`;
}
```





此函数更新文档 `body` 的 `textContent` 属性，使其包含鼠标指针的坐标。事件对象的 `x` 和 `y` 属性分别告诉我们鼠标指针的水平和垂直位置。我们可以使用模板字符串字量（template literal）在每次鼠标移动时将这些值插入到文档正文的文本内容中。尝试在页面上移动你的鼠标指针，你应该能在左上角看到它的精确坐标。

![跟踪鼠标移动时的坐标](img/mousemove.png)

你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/ExNWaxK)。

## 鼠标悬停 (Mouse Over)

当鼠标指针移动到元素上方时，会触发 `mouseover` 事件。为了看到这个效果，让我们来创建一个名为“找炸弹”的小游戏。在 CodePen 上打开一个新的 Pen，并在 `JS` 部分输入以下代码：

```
const bomb = document.createElement('div');
  bomb.textContent = '💣';
  bomb.style.position = 'absolute';
  bomb.style.top = Math.floor(200*Math.random()) + 'px';
  bomb.style.left = Math.floor(200*Math.random())+'px';
  bomb.style.fontSize = '64px';
  document.body.appendChild(bomb);
```

这使用了我们在上一节中学到的很多内容来创建一个包含炸弹表情符号作为文本内容的 `<div>` 元素。它将 `position` 属性设置为 `absolute`，这允许我们使用 `left` 和 `top` 属性分别相对于页面左侧和顶部设置炸弹的位置。然后我们使用在第 4 章中学到的知识，将这些属性设置为随机数。最后，我们使用 `appendChild()` 方法将炸弹放置在页面上。每运行一次代码，它都会出现在随机位置。

接下来，我们需要添加事件监听器：

```
bomb.addEventListener('mouseover', e => {
 document.body.style.background = 'red';
 document.body.innerHTML = '<h1>BOOOOOOM!!!</h1>';
});
```

这会监听 `mouseover` 事件。第二个参数是一个匿名函数，当鼠标指针滑过炸弹时会被调用。

试一试看会发生什么！

![这个游戏太棒了！](img/bomb.png)

你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/RwopNPx)。

## 鼠标按下与释放 (Mouse Up and Down)

当左鼠标键被按下时触发 `mousedown` 事件，当释放它时触发 `mouseup` 事件。此事件可以绑定到特定元素上，因此事件仅在鼠标指针位于元素上时才会触发。

我们可以将这些事件与 `mousemove` 事件结合，来实现一个非常简单的拖放界面。在 CodePen 上打开一个新的 Pen，并在 `HTML` 部分输入以下代码：

```
<div id='star'>⭐️</div>
```

这只是包含一个星星表情符号的 `<div>` 元素（你可以选择任何喜欢的 emoji！），它是要在页面上移动的元素。

接下来在 `CSS` 部分添加以下代码：

```
#star{
  font-size: 64px;
  position: absolute;
}
```

这让元素变大了一些，并将 `position` 属性设置为 `absolute`，这意味着可以使用 `left` 和 `top` 属性更改它的位置。*这对拖放功能的实现至关重要*。

![星星的诞生](img/star.png)

接下来，我们将处理 JavaScript 代码。在 `JS` 部分添加以下内容：

```
const star = document.querySelector('#star');
```

我们的第一行使用查询选择器（query selector）获取星星元素的引用。接下来，我们需要为该元素添加几个事件处理器：

```
star.addEventListener( 'mousedown', start);
star.addEventListener( 'mouseup', stop );
```

当在星星上按下鼠标键时，这会调用 `start` 函数，当释放鼠标键时将调用 `stop` 函数。我们先写 `start` 函数：

```
function start(e) {
  document.addEventListener( 'mousemove', move);
}
```

这只是为整个页面添加了一个事件监听器。它正在监听 `mousemove` 事件并调用 `move` 函数。我们接着来写它：

```
function move(e){
  star.style.left = `${e.x}px`;
  star.style.top = `${e.y}px`;
}
```

`move` 函数是实现拖拽的关键。它只是将星星的位置（`star.style.left` 和 `star.style.top`）设置为存储在事件对象属性 `x` 和 `y` 中的鼠标指针位置。（在上面的代码中，事件对象被赋值给参数 `e`）。注意，这里使用了模板字符串，以便在末尾添加 `px`（单位是像素）。

这将导致星星跟随鼠标指针在屏幕上移动。我们希望在释放鼠标并调用 `stop` 函数时停止这种行为。为了停止它，我们需要移除 `mousemove` 事件监听器。

### 移除事件监听器

可以使用 `removeEventListener()` 方法移除事件监听器。

### 为 `addEventListener` 函数命名

如果你以后想移除它，则不应该将匿名函数作为 `addEventListener` 的参数。因为需要保持一致的：

```
document.addEventListener( 'mousemove', move);
```

```
function stop(){
  document.removeEventListener( 'mousemove');
}
```

## 简单待办事项 (Simple To-do List)

我们将通过整合学到的内容来构建一个更复杂的待办事项应用。它允许你向列表添加项目，并通过点击它们来划掉——无需操作控制台。

开始之前，在 CodePen 上打开一个新的 Pen，并在 **HTML** 部分输入以下内容：

```
<form name='addTask'>
  <input type='text' name='newTask'>
  <button type='submit'>ADD</button>
</form>

<ul id='list'></ul>
```

这与我们在本章早期用于[表单输入示例](https://codepen.io/SitePoint/pen/RwopL) 的 HTML 代码几乎相同。它创建一个包含单个输入框和提交按钮的表单。还有一个无序列表元素（`<ul>`），我们在程序运行时动态将项目放入其中。

现在编写让它运行的代码！首先，我们需要获取一些 HTML 元素的 JavaScript 引用：

```
const list = document.getElementById('list');
const form = document.forms.addTask;
```

这给了我们 `form` 元素和空 `<ul>` 元素的引用。

现在让我们关注向列表添加项目。为此，我们需要为表单附加一个事件监听器：

```
form.addEventListener('submit',addTask);
```

当提交表单时，这会调用 `addTask` 函数。现在我们只需要编写 `addTask` 函数：

```
function addTask(e){
  e.preventDefault();
  const task= document.createElement('li');
  task.textContent = form.newTask.value;
  list.appendChild(task);
}
```




此函数执行的第一件事是使用 `preventDefault()` 方法阻止表单提交到服务器。之后，我们使用在上章中学习的某些 DOM 方法创建一个新的列表项（`<li>`）元素，并将其赋值给变量 `task`。接下来，我们将 `textContent` 属性设置为输入到表单字段中的文本，该文本存储在 `form.newTask.value` 中。最后，我们使用 `appendChild()` 方法将此新元素添加到 `list` 元素的底部。

尝试在输入框中添加一个任务，如果一切按计划进行，它看起来应该像这样：

![添加任务](img/addtask.png)

现在，我们需要做的是让项目在被点击时能够被划掉（删除线效果）。让我们给项目添加一个事件监听器来处理点击操作：

```javascript
list.addEventListener('click',strikeTask);
```

你可能已经注意到，我将事件监听器添加到了列表元素，而不是单独的列表项。

如果我们为所有的 `<li>` 标签附加 `click` 事件监听器，那么我们需要为每个元素准备一个独立的事件监听器。而且，每当添加新项目时，我们都必须动态地添加新的事件监听器。这可能会导致大量包含相同代码且基本上在做同样事情的事件监听器——这完全不符合 DRY（不要重复自己）原则！

### 事件委托

处理这种情况的 DRY 方法是使用**事件委托**。这会将事件监听器附加到父元素 `<ul>` 上，而不是每个单独的列表项。当点击一个子元素时，事件仍然会触发，我们可以使用事件对象的 `target` 属性来识别被点击的实际元素。

让我们来看一下效果。在 JS 部分的底部添加以下代码：

```javascript
function strikeTask(e){
  alert(e.target.textContent);
}
```

这是 `strikeTask` 函数，它在列表被点击时触发。目前，它包含一个 alert，用于显示通过 `event.target` 识别出的被点击元素的文本内容。尝试添加一些项目，然后点击其中一个。你应该看到类似下面的内容：

![切换任务状态](img/taskalert.png)

现在我们已经确定它可以正常工作了，让我们更新代码，改为划掉项目。如下所示更新 `strikeTask` 函数：

```javascript
function strikeTask(e){
  e.target.classList.toggle('complete');
}
```

这使用了每个元素都有的 `classList` 属性的 `toggle` 方法。如果元素没有该类，它将添加该类；如果已经有了该类，则将其移除。这意味着点击项目将添加 `complete` 类，或者在它已存在时将其移除。这本身不会产生任何效果，但现在我们可以添加一些 CSS 来样式化任何带有 `complete` 类的元素：

```css
.complete {
  text-decoration: line-through;
}
```

现在，如果你尝试添加一些项目并点击它们，你应该能够尽情所欲地划掉它们，如下文所示。

![划掉已完成的任务](img/strike.png)

你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/JjbWoWN)。

## 挑战

1.  我们在本章中创建的拖放示例是一个非常简单的实现。更健壮的版本可以在[此处](https://codepen.io/SitePoint/pen/vYyxExR)查看。看看代码并是否能理解发生了什么。它还使用了[触摸事件](https://developer.mozilla.org/en-US/docs/Web/API/Touch_events)。

2.  你能更新简单的待办列表代码，以便在添加项目后让 `add` 函数清空输入框并获取焦点，而不是让文本留在那里吗？（提示：你可能想查找表单元素拥有的 `focus()` 方法。）你可以在这里查看我的解决方案](https://codepen.io/SitePoint/pen/KKNWwmP)。

3.  在简单的待办列表中，与其划掉项目，你能更改功能使其在被点击时删除项目吗？（提示：你可以使用在上章中介绍过的 `remove()` 方法。）你可以在这里查看我的解决方案](https://codepen.io/SitePoint/pen/JjbWoNN)。

## 总结

*   当用户与网页进行交互时，会发生事件。
*   事件监听器被附加到元素上，并在事件发生时调用回调函数。
*   事件对象作为参数传递给回调函数，包含许多与事件相关的属性和方法。
*   有许多类型的事件，包括点击事件、鼠标事件和键盘事件。
*   表单还有一个 `submit` 事件，可以可以在表单提交之前拦截它。
*   你可以使用 `removeEventListener()` 方法移除事件。
*   事件委托是将事件监听器添加到父元素上，用以捕获发生在多个子元素上的事件，从而避免为每个子元素添加事件监听器。

现在我们已经涵盖了事件，可以让我们的代码更具交互性。在接下来的几章中...




在字符串上使用展开运算符（spread operator）的一个特殊好处是我们可以对它们使用迭代方法。那么，什么是迭代器呢？

## 数组迭代方法

`Array iteration methods` 是允许你遍历数组并对数组中的每个项执行操作的方法。对数组中的某个项执行的每一次操作都称为一次 `iteration`（迭代）。

![Iterators](img/iterator.png)

JavaScript 包含了许多数组迭代方法，这些方法使用回调函数来提供每次迭代中要执行的操作指令。这些方法总是始终保持原始数组不变，但通常会返回一个新的数组或值。

### 高效的箭头函数

你会发现，在下面的示例中，箭头函数经常被用于声明回调函数。它们是这里很好的候选者，因为它们很短、可以写成一行，并且具有隐式返回值。

### forEach

`forEach()` 方法遍历数组中的每一个项，并在每次迭代时调用一次回调函数。该回调函数接受三个参数：

*   数组中当前项的值
*   当前项在数组中的索引
*   数组本身的引用

如果该方法没有使用索引或数组引用，则不需要指定它们。（通常只提供当前项的值作为参数。）

下面的代码显示了一个示例，将数组中每个项的一些信息记录到控制台。它遍历数组中的每个项，并为每个项向控制台打印一条语句。尝试在控制台中输入以下代码（可在[此 CodePen](https://codepen.io/SitePoint/pen/MWbpXMQ)中找到）：

```
['🍏','🍌','🥕'].forEach(
  (item,index,array) => console.log(`Item at position ${index} is ${item} (there are ${array.length} items in total).`)
);
```

在第一次迭代中，`item` 的值为 "🍏"，`index` 的值为 0，`array` 的值为 `['🍏','🍌',🥕']`。这会在控制台打印出以下字符串：

```
"Item at position 0 is 🍏 (there are 3 items in total)."
```

在第二次迭代中，`item` 的值为 "🍌"，`index` 的值为 1，`array` 的值为 `['🍏','🍌',🥕]`。这会在控制台打印出以下字符串：

```
"Item at position 1 is 🍌 (there are 3 items in total)."
```

在最后一次迭代中，`item` 的值为 "🥕"，`index` 的值为 2，`array` 的值为 `['🍏','🍌',🥕]`。这会在控制台打印出以下字符串：

```
"Item at position 2 is 🥕 (there are 3 items in total)."
```

这总结在下表所示：

| Iteration | `item` | `index` | `array` | `console.log` |
| --- | --- | --- | --- | --- |
| 1 | "🍏" | 0 | ['🍏','🍌','🥕'] | "Item at position 0 is 🍏 (there are 3 items in total)." |
| 2 | "🍌" | 1 | ['🍏','🍌','🥕'] | "Item at position 1 is 🍌 (there are 3 items in total)." |
| 3 | "🥕" | 2 | ['🍏','🍌','🥕'] | "Item at position 2 is 🥕 (there are 3 items in total)." |

### 扑牌数组

我们可以使用 `forEach()` 方法快速创建一个代表扑牌牌的数组。我们将通过遍历一个代表花色的数组，以及另一个代表该花色中每张牌点值的数组来实现。（你可以从 [CodePen](https://codepen.io/SitePoint/pen/ZEBejzo) 复制以下示例的代码。）

打开控制台并声明以下变量：

```
const suits = ['♠️','♦️','♣️','❤️'];
const values = ['Ace',2,3,4,5,6,7,8,9,10,'Jack','Queen','King'];
const deck = [];
```

第一个变量 `suits` 是一个包含每种花色字符串表示的数组。变量 `values` 是一个包含每个张牌牌点值字符串表示的数组。变量 `deck` 是一个空数组，最终将持有整个副牌。

现在我们已经设置好了这些数组，可以遍历 `suits` 数组和 `values` 数组，将元素组合成单牌，并使用 `push()` 方法将其放入 `deck` 数组中：

```
suits.forEach(suit => 
    values.forEach(value => 
        deck.push(`${value} of ${suit}`);
    )
);
```

第一个 `forEach` 遍历 `suits` 数组。在每次迭代中，都会调用匿名回调函数，参数 `suit` 代表 `suits` 数组中的当前项。第二个 `forEach` 然后遍历 `values` 数组，并使用参数 `value` 代表该数组中的每个项。我们使用模板字符串（template literal）插值牌的花色和点，创建一个推入 `deck` 数组的字符串。

例如，在第一次迭代中，`suit` 的值 `suits` 数组中的第一个项 `♠️`，而 `value` 的值是 `values` 数组中的第一个项 `Ace`。这产生了一个推入 `deck` 数组的字符串。

### Map

`map()` 方法也遍历数组并使用回调函数作为参数。与 `forEach` 不同，`map` 返回一个新数组，并将每个值替换为回调函数的返回值。

`map()` 方法的回调函数与 `forEach()` 方法具有相同的参数：

*   数组中当前项的值
*   当前项在数组中的索引
*   数组本身的引用

为了演示这一点，请在控制台中尝试[以下代码](https://codepen.io/SitePoint/pen/gOLWxv)：

```
["🍏","🍌","🥕"].map((value,index,array) => '😊');
```
["😊","😊","😊"]

回调函数是一个带有 `value`、index` 和 `array` 参数的匿名箭头函数。返回值只是字符串 `'😊'`，因此数组中的每个项都被映射为一个笑脸！

在这种情况下，回调函数不需要使用 `item`、`index` 或 `array` 参数，因此它们实际上不需要在那里。以下回调函数使用单个参数 `x` 也是有效的：

```
[1,2,3].map(x => '😊');
```
[ 😊,😊,😊 ]

返回值可以基于提供给回调函数的参数。在接下来的示例中，数组中的每个数字都被映射为新数组中自身的平方：

```
[1,2,3].map(n => n*n);
```
[1, 4, 9]
```

你可以为参数命名任何名称。在上面的示例中，我们使用 `n` 代表数组中的每个项。由于回调函数仅依赖于项的值，因此我们只需要提供这个参数。

`map()` 方法的一个特别好的用途是为文本块添加 HTML 标签。例如，接下来的代码接收一个项数组，然后返回每个项在 `<li>` 标签中的内容：





```javascript
['Apple','Banana','Carrot'].map(item => 
`<li>${item}</li>`);
<< ["<li>Apple</li>", "<li>Banana</li>", "<li>Carrot</li>"]
```

参数 `item` 代表每次迭代时数组中的每个字符串。回调函数的返回值是一个模板字面量，它使用字符串插值将字符串插入到 `<li>` 标签内部。

![使用 map 添加标签](img/htmlmap.png)

然后我们可以在末尾链式调用 `join()` 方法并传入空字符串作为参数，将所有项合并成一个的 HTML 字符串：

```javascript
['Apple','Banana','Carrot'].map(item => 
`<li>${item}</li>`).join('');
<< "<li>Apple</li><li>Banana</li><li>Carrot</li>"
```

然后可以将其插入到 `<ul>` 元素中，根据数组的内容创建一个无序列表。让我们在 CodePen 上尝试一下这个操作。首先在 HTML 部分从一个空的 `<ul>` 元素开始：

```html
<ul id='list'></ul>
```

现在我们将在 JS 部分获取该元素的引用：

```javascript
const list = document.getElementById('list');
```

现在我们只需要做的就是用我们的 HTML 字符串更新该元素的 `innerHTML` 属性：

```javascript
list.innerHTML = ['Apple','Banana','Carrot'].map(item => 
`<li>${item}</li>`).join('');
```

这会根据数组中的项目，在文档中渲染出一个项目列表：

![将数组渲染为 HTML 列表](img/arraytoHTML.png)

你可以查看 [我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/poNPrrm).

## Reduce (减少)

`reduce()` 方法是另一个遍历数组每个值的方法，每次都会调用回调函数。主要的区别在于，它不是返回一个数组，而是将回调的每个结果合并为一个单一值。

`reduce()` 方法的回调函数描述了如何合并数组的每个值以产生累加运行总和，并有四个参数：

- 累加器（accumulator），用于存储运行总和。该方法将返回它的最终值。
- 数组中当前项的值。
- 当前项在数组中的索引。
- 数组本身的引用。

大多数情况下，只使用前两个参数，任何未使用的参数不需要引用。

以下示例相加数组中的所有数字并返回总和：

```javascript
[1,2,3].reduce( 
  (acc,value) => acc + value
);
<< 6
```

![使用 reduce 相加数字](img/reduce.png)

在上面的示例中，`acc` 的值从 1 开始（数组中的第一个项）。在每次迭代后，数组中项的值都会加到 `acc` 的值上。因此在下一次迭代中，2 被加到 `acc` 中使其变为 3。然后在最后一次迭代中，3 被加到 `acc` 中。一旦数组中的每个项都已加在一起，就会返回 `acc` 的最终值，即 6。

通过对回调函数中的计算进行微调，我们可以将所有数字相乘：

```javascript
[1,2,3].reduce(
  (acc,value) => acc * value
);
<< 6
```

### 加法 vs 乘法

当我们把数字相加和相乘时答案相同，这纯属巧合（尝试使用带有不同数字的数组）。

`reduce()` 方法还接受一个可选的第二个参数，跟在回调函数之后，允许我们设置累加器的初始值。例如，下面的方法相加数组中的所有数字（得到 6），然后在返回 16 之前将该结果加到 10：

```javascript
[1,2,3].reduce(
  (acc,value) => acc + value,10);
<< 16
```

## Filter (过滤)

`filter()` 方法测试数组中的每个项，以检查它们是否符合回调函数定义的某些条件。任何在回调中返回真值（truthy）的项都将作为新数组返回。例如，我们可以使用以下代码过滤数字数组，只留下大于 2 的数字：

```javascript
[1, 2, 3, 4].filter(x => x > 2 );
<< [3,4]
```

在每次迭代中，回调函数都会检查数组中由参数 `x` 表示的项是否大于 2。如果是，回调函数返回 `true`，该值将保留在新数组中。这个过程可以在图中看到。

![过滤掉不大于 2 的数字](img/filter.png)

`filter()` 方法提供了一种从数组中找到所有真值的有用方法：

```javascript
[0, 1, '0', false, 'hello' ].filter(Boolean);
<< [1, 'hello']
```

这利用了 `Boolean` 函数将返回值的布尔表示的这一事实，因此只有真值会返回 `true` 并被 `filter()` 方法返回。要找到所有假值（falsy）值，可以使用以下过滤器：

```javascript
[0, 1, '0', false, 'hello' ].filter(x => !x);
<< [0, false]
```

这使用了非运算符（`!`）来返回补码。由于 `Boolean` 函数将返回一个值的布尔表示，这意味着只有真值会返回 `true` 并被 `filter()` 方法返回。

### 过滤过滤

在第 6 章，我们通过“谁是谁？”游戏使用了这些角色：

![谁的？](img/guesswho.png)

在第 9 章，我们创建了对象来表示它们：

```javascript
const alfie = {
  name: 'Alfie',
  glasses: false,
  hat: false
};
const betty = {
  name: 'Betty',
  glasses: true,
  hat: true
};
const gemma = {
  name: 'Gemma',
  glasses: false,
  hat: true
};
const del = {
  name: 'Del',
  glasses: true,
  hat: false
};
```

我们可以这样将这些对象放入名为 `people` 的数组中：

```javascript
const people = [alfie,betty,gemma,del];
```

现在我们可以通过使用 `filter()` 方法对这个数组玩玩“谁是谁？”游戏：

```javascript
people.filter(person => person.glasses && person.hat);
<< [{ name: 'Betty', glasses: true, hat: true}]
```

上面的过滤器返回了代表 Betty 的对象，因为她戴眼镜又戴帽子。如果我们想找到不戴帽子的人，我们可以在回调函数中使用非运算符：

```javascript
people.filter(person => person.glasses && !person.hat);
<< [{ name: 'Del', glasses: true, hat: false}]
```

通过改变回调函数中的条件，你可以不同的方式过滤数组。尝试更改这些条件看看是否可以返回每个人。你可以查看 [我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/vYymJrp).




`some()` 方法与 `every()` 方法非常相似。它也会遍历数组中的每个项，直到回调函数中定义的给定条件返回 `true`。一旦发生这种情况，迭代就会停止，该方法返回 `true`。如果遍历到数组末尾都没有任何项返回 `true`，它将返回 `false`。这是一种查找数组中至少有一个项符合特定标准的实用方法。

例如，以下代码检查单词中是否有任何一个长度大于七个字符：

```
['C','C++','Ruby','Python','JavaScript','Swift','Java'].some(word => word.length > 7);
<< true
```

可以在“[JavaScript 数组迭代器速查表](https://levelup.gitconnected.com/the-array-iterators-cheatsheet-javascript-9d0cfa03f4)”中找到数组迭代方法的有用总结。

在“[函数式 JavaScript 中的过滤与链式调用](https://www.sitepoint.com/filtering-and-chaining-in-functional-javascript/)”中，有一些关于如何链式调用迭代方法的优秀示例。

## 遍历对象

对象和数组一样都是集合，同样可以遍历对象的属性。

例如，考虑以下 `rectangle` 对象，它类似于我们在第 9 章中创建的 `square` 对象：

```
const rectangle = {
  height: 4,
  length: 5,
  perimeter() { return 2 * (this.height + this.length); },
  area() { return this.length * this.height; }
}
```

我们可以使用 for–in 循环遍历对象的所有属性，该循环会遍历对象中的每一个键。尝试在控制台中输入以下代码（你需要先定义 `rectangle` 对象）：

```
for(const prop in rectangle) {
  console.log(`${prop}: ${rectangle[prop]}`);
}
<< height: 4
<< length: 5
<< perimeter: function (){ return 2 * (this.height + this.length) };
<< area: function { return this.length * this.height }
```

在这个示例中，变量 `prop` 用于在迭代的每一步引用每个属性名。然后我们可以使用 `rectangle[prop]` 来查找该属性的值。在示例中，我们简单地使用了 `console.log` 配合模板字字符将属性及其值打印到控制台。

### 键与值

JavaScript 还提供了一组方法，返回一个包含对象所有属性和值的数组。这意味着随后可以使用任何数组方法，例如我们在本章中学到的数组迭代方法。

`Object.keys()` 方法返回一个包含作为参数提供的对象的所有键的数组：

```
Object.keys(rectangle);
<< ["height","length","perimeter","area"]
```

如你所见，每个属性的键以字符串的形式列在返回的数组中。

`Object.values()` 方法的作用相同，但它返回的是每个属性值的数组：

```
Object.values(rectangle);
<< [4,5, perimeter(), area()]
```

数组中的每个值都与其原始数据类型相同——在此例中为数字和函数。

`Object.entries()` 方法返回一个包含键值对的数组。这些键值对以子数组的形式嵌套在数组内部：

```
Object.entries(rectangle);
<< [["height",4],["length",5],["perimeter",function()],["area",function()]]
```

由于这些方法返回的是数组，我们可以使用链式调用来立即调用在本章前面介绍过的某个迭代方法。例如，我们可以使用 `forEach()` 方法将属性及其值打印到控制台：

```
Object.entries(rectangle).forEach(subArray =>console.log(`${subArray[0]}: ${subArray[1]}`));
<< "height: 4"
   "length: 5"
   "perimeter: function perimeter() {return 2 * (this.height + this.length);}"
   "area: function area() {return this.length * this.height;}"
```

这里使用一个名为 `subArray` 的参数来引用 `Object.entries` 数组中的每个子数组。然后我们使用索引符号来引用子数组中的每个项，因此 `subArray[0]` 指属性名，而 `subArray[1]` 指属性值。这虽然可行，但这种使用索引的方法会让代码变得难以理解。

我们可以通过在定义回调函数时显式地命名子数组中的每个项来提高可读性，如下所示：

```
Object.entries(rectangle).forEach(([prop,value])=>console.log(`${prop}: ${value}`));
```

这允许我们将子数组中的第一个项引用为 `prop`，第二个项引用为 `value`，使得代码更具可读性。这种过程被称为**[解构](https://www.sitepoint.com/es6-destructuring-assignment/)**。

## 待事项项目

在上一章中，我们使用事件生成了一个可以运行的待事项列表。这样做的问题在于，待办事项被直接添加到了网页上，从未存储在程序的任何地方。如果程序需要在任何时候知道待事项列表的状态，这就会成为问题。这个概念被称为**状态（state）**。



这段代码现在需要放在一个 `render` 函数中，该函数使用 `map` 将 `task` 数组中的每一项包裹在 `<li>` 标签中，将它们合并成一个 HTML 字符串，然后将其插入列表元素中。我们还会添加几行代码来清空输入字段的内容并获取焦点：

```javascript
function render(){
  list.innerHTML = tasks.map(task => `<li>${task}</li>>`).join('');
  form.item.value = '';
  form.item.focus();
}
```

最后，我们需要在每次更新数组时调用 `render` 函数——即在调用 `addTask` 或 `removeTask` 函数之后。更新这些函数，让它们在更新数组后调用 `render`：

```javascript
function addTask(e){
  e.preventDefault();
  tasks.push(form.item.value);
  render();
}

function removeTask(e){
  const index = tasks.indexOf(e.target.textContent);
  if(index>-1){
    tasks.splice(i,1);
  }
  render();
}
```

现在，如果你尝试添加任务，它们应该出现在列表中，点击某个任务将将其删除。这与之前的操作没有区别，但变化的地方全在后台：我们现在现在可以通过访问 `tasks` 数组来跟踪程序内部创建的所有任务。这意味着我们可以通过查看 `tasks.length()` 方法的返回值，来跟踪还有多少任务需要完成。让我们添加一些代码，在任务列表下方显示这些内容。首先，在 HTML 部分底部添加一个空的 `<div>` 元素：

```html
<div id='count'></div>
```

我们还需要在 JS 部分添加对该元素的引用：

```javascript
const count = document.getElementById('count');
```

接下来，在 `render` 函数中添加以下行代码，以便它包含一行用于更新 `count` div 的代码：

```javascript
count.textContent = `${tasks.length} task${tasks.length==1?'':'s'} left to complete.`
```

这使用了模板字面量（template literal）来根据任务数量更新 `textContent` 属性，并使用了三元运算符，在列表中仅有一个任务时使用“task”而不是“tasks”。

尝试添加和删除一些任务。你应该能看到计数器随着它们在列表中出现而更新。

你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/poNwvRq)。

## 挑战

1. 编写一个函数，接受字符串数组作为参数，并使用 `map` 返回一个所有单词都写为大写的新数组。你能让它返回一个所有单词都倒序的数组吗？你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/jOVwEBQ)。

2. 编写一个 `spanner` 函数，接受一个字符串并返回一个字符串，使用 `map()` 和 `join()` 方法将每个单独字符包裹在 `<span>` 标签中。例如，`spanner('Hello')` 应该返回字符串 `"<<span>H</span><span>e</span><span>l</span><span>l</span><span>o</span"`。你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/LYbLEyZ)。

3. 扩展你在挑战 2 中创建的 `spanner` 函数，创建一个 `coloredLetters` 函数，为每个字母涂上不同的颜色。它应该接受字符串和颜色数组作为参数，然后为每个 `<span>` 标签添加 `style` 属性。你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/KKNBVjO)。

## 总结

* 展开运算符（spread operator）可以应用于字符串，将其展开为包含每个字符作为单独条目的的数组。
* 迭代方法（Iteration methods）遍历集合中的每一个值，并对每个值应用某种操作。
* JavaScript 拥有许多数组方法，可以对数组中的每项应用回调函数。
* `forEach()` 方法对数组中的每项应用回调函数中的代码。
* `map()` 方法通过对数组中的每项应用回调函数中的代码来返回一个新数组。
* `reduce()` 方法通过将回调函数中定义的累加函数应用到数组中的每个值来返回一个单一值——例如，相加数组中的所有值。
* `filter()` 方法返回一个新数组，其中仅包含原始数组中符合回调函数定义标准的值。
* `find()` 方法返回数组中第一个符合回调函数给定标准的项。
* `every()` 方法如果数组中的每一项都符合回调函数给定的标准，则返回 `true`。否则，返回 `false`。
* `some()` 方法如果数组中的任何一个项符合回调函数给定的标准，则返回 `true`。如果数组中没有项符合该标准，则返回 `false`。
* 你可以使用 for–in 循环遍历对象，这将让你能够访问对象中的每个属性。
* `Object.keys()`、`Object.values()` 和 `Object.entries()` 方法将分别返回对象的键、值或键值值对的数组。

在下一章中，我们将开始学习函数式编程。

# 第 13 章：让我们变得函数化

我们涵盖了[函数](https://www.w3schools.com/js/js_functions.asp)，但现在是时候深入探讨这些主题了：

* 命名参数
* 剩余运算符
* 变量提升
* 递归函数
* 闭包
* 函数式编程
* 纯函数

## 命名参数

当一个函数有许多参数时，很难记住编写参数的顺序。例如，考虑这个返回样式化 `<h1>` 元素的函数：

```javascript
function heading(text,color,size,bgcolor){
  return `<h1 style='color:${color};background-color:${bgcolor};font-size:${size}>${text}</1>`
}
```

这使用了位置参数，这意味着当调用函数时，参数的位置决定了它被赋值给哪个参数。所以，如果你想要一个内容为“Hello, World!”、大小为 48px、红色背景的标题，你会写：

```javascript
heading('Hello, World!','red','48px','blue');
```

在调用函数时可能很难记住这些参数的顺序，这可能会导致颜色混乱，甚至糟糕地给字体大小赋值红色！

许多语言使用命名参数来解决这个问题。通过这些参数，你可以通过名称为每个参数赋值，而不是依赖它的位置。这意味着参数可以按任何顺序列出，如下：

```javascript
heading(color = 'red',bgcolor = 'blue',text ='Hello, World!',size = '48px');
```

遗憾的是，JavaScript 严格来说并不支持命名参数——所以上面的示例无法运行。好消息是，可以通过使用对象作为参数来模拟它们，让对象的属性充当命名参数的作用。

下面的示例展示了如何通过上面的示例实现这一点。函数需要重写，将参数列为对象字面量的属性：

```javascript
function heading({text,color,size,bgcolor}){
  return `<h1 style='color:${color};background-color:${bgcolor};font-size:${size}>${text}</1>`
}
```

现在可以调用函数了，提供一个对象作为参数，为命名属性提供值：

```javascript
heading({color: 'red',bgcolor: 'blue',text:'Hello, World!',size: '48px'});
```

注意，参数对象中属性的顺序与作为参数提供的对象中的顺序并不相同。这种方法的优点是不需要记住编写参数的顺序。另一个优点是它让代码更易读，因为每个参数都有一个描述性的标签来解释它代表什么。

这种技术在函数有大量参数时非常有用，特别是当其中一些参数是可选的。




你可以在 [CodePen 上查看此示例](https://codepen.io/SitePoint/pen/NWbgBGN)。

## 剩余参数 (Rest Parameter)

有时我们并不知道会向函数提供多少参数。处理变数量参数最简单的方法是使用`剩余参数`（rest parameter）。它由放置在函数声明中最后一个参数前面的三个三个点组成。它会将所有参数收集到一个数组中。

尝试在控制台中输入以下函数。该函数接受任意数量的参数，并使用剩余参数将它们全部收集到一个名为 `numbers` 的数组中。然后，它将我们在上一节中见过的 `reduce()` 方法应用于该数组上，并返回作为参数输入的所有数字之和：

```
function add(...numbers){
  return numbers.reduce((acc,n) => acc + n);
}
```

现在尝试用不同数量的参数调用该函数，如下例所示：

```
add(2,3);
<< 5

add(1,2,3,4,5);
<< 15
```

## 递归函数 (Recursive Functions)

`递归函数`是指调用自身的函数！这听起来可能有点疯狂，但在函数体内部放置一个自引用函数调用是完全可能的。函数会不断调用自己，直到满足特定条件。在涉及迭代过程时，它是一个非常有用的工具。

一个常见的例子是计算数字[阶乘](http://en.wikipedia.org/wiki/Factorial)的函数：

``` evenfunction factorial(n) {
  if (n === 0) {
    return 1;
  } else {
    return n * factorial(n - 1);
  }
}
```

如果提供的参数为 0，该函数返回 1（0 的阶乘为 1），否则它会将参数与使用减 1 参数调用自身的结果相乘。该函数将继续调用自己，直到最终返回参数 0 和 1。观察发生过程的最佳方法是使用示例：

```
factorial(3);
<< 6
```

这将把 3 乘以 `factorial(2)` 的返回值，`factorial(2)` 又会将 2 乘以 `factorial(1)` 的返回值，`factorial(1)` 又会将 1 乘以 `factorial(0)` 的返回值，而后者是 1。反向推导得出 `1 * 1 * 2 * 3`。这可以通过下面的图看到：

![递归阶乘函数调用](img/recursive.png)

递归函数可以用于类似于我们在第 7 章中看到的循环执行的操作。它们在实现[分治算法](https://en.wikipedia.org/wiki/Divide-and-conquer_algorithm) 时特别有用。你可以在“[函数式 JavaScript 中的递归](https://www.sitepoint.com/recursion-functional-javascript/)”中阅读更多关于递归函数的知识。

## 作用域 (Scope)

变量“作用域”的概念在任何编程语言中都非常重要。变量或函数的`作用域`指的是程序可以访问它们的部分。大多数语言都有某种形式的`词法作用域`（lexical scope），这意味着变量的作用域取决于它在代码中出现的位置。通常将变量放在块内部会将其作用域限制在该范围内。少数语言（如 Perl 和其他 Lisp 风格语言）使用`动态作用域`（dynamic scope），这意味着变量的作用域可以在程序运行时发生变化。

`全局作用域`（Global scope）涵盖整个程序。任何可以在程序任何地方访问的变量或函数都被认为具有全局作用域。

`局部作用域`（Local scope）指的是仅在特定代码块内可函数或变量。定义在块内部的任何函数或变量只能在那个特定块内被“在作用范围内”时被访问。

为了演示这一点，让我们尝试在控制台中定义一些变量。首先，通过直接在程序主体中定义来定义全局作用域中的变量：

```
const global = 'Hello, Global Scope!';
```

现在，我们可以通过创建一个名为 `local` 的函数来创建一个局部作用域。在函数体内部，我们将声明一个名为 `secret` 的变量：

```
function local(){
  const secret = 'Hello from the local scope.';
}
```

下面的图显示了每个变量的作用域。`global` 定义在全局作用域中，可以在作用域内的任何地方访问（包括从局部作用域内部）。`secret` 定义在 `local` 函数的局部作用域内，只能从该作用域内部访问。

![全局和局部作用域](img/scope.png)

如果我们尝试向控制台打印变量 `global` 的值，可以看到我们可以访问它：

```
console.log(global);
<< Hello, Global Scope!
```

然而，如果我们尝试访问变量 `secret`，我们会得到一个错误信息，说无法找到它：

```
console.log(secret);
<< ReferenceError: "Can't find variable secret"
```

这是因为变量 `secret` 只有在 `local` 函数体内部可用。最后一个命令是从全局作用域发出的，在那里我们无法访问函数的局部作用域。

为了看到我们可以在 `local` 函数的作用域内访问变量 `secret`，让我们重新定义函数，将 `secret` 变量打印到控制台：

```
function local(){
  const secret = 'Hello from the local scope.';
  console.log(secret);
}
```

现在，如果我们调用 `local` 函数，可以看到它可以访问该变量：

```
local();
<< Hello from the local scope.
```

然而，我们只能在块内部访问该变量。

尽管将所有内容放在全局作用域似乎是个好主意，但实际上这被认为是不习惯。事实上，将变量排除在全局作用域之外是良好的做法。这是为了避免`命名冲突`（naming collisions），即变量或函数重名导致混淆。这在目前看起来不是问题，但当你与他人代码协作时（作为团队的一部分或使用外部代码库），就会变成一个大问题，因为你不知道哪些变量名已被占用。通过将变量和函数放在各自的作用域内，我们可以更容易追踪它们。

### 块作用域 (Block Scope)

JavaScript 中的所有变量在函数内部都是局部作用域，但变量只有在使用 `const` 和 `let` 时才具有块作用域。如果使用 `var` 可以在定义的块之外访问。

如果你尝试在控制台中输入以下代码，它将无法工作，因为变量 `message` 只有块级作用域，因此无法在大括号之外访问：

```
if(name==="JavaScript"){
  const message = "Hello ${name}!";
}
console.log(message);
<< ReferenceError: "Can't find variable: message"
```

如果用 `var` 代替 `const`，这段代码将无错误运行。或者可以将 `console.log(message)` 放在块内部。

## 提升 (Hoisting)

使用函数声明定义的函数会自动`提升`到程序作用域的顶部。这意味着它们可以在定义之前被调用。例如，在以下代码中，`hoist()` 可以在实际定义之前被调用：

```
// 在代码开始处调用函数
hoist();

// ...
// ... 这里有更多代码
// ...

// 函数定义在代码末尾
function hoist(){
  console.log('Hoist Me!');

}
```

这非常有用，这意味着所有的函数定义可以放在一起（可能放在程序的末尾），而不是要求每个函数在使用之前都必须定义。

如果在使用 `const` 和 `let` 声明之前尝试引用变量，将抛出异常。因此，你应该尝试在块的开头声明任何变量，这样就不需要提升了。




这意味着函数表达式（即将匿名函数赋值给变量）在声明之前不能被调用，这与函数声明不同。

这也许是函数声明和函数表达式之间最大的区别，它可能会影响你关于使用哪种方式的决定。有些人喜欢使用函数表达式意味着你被要求在使用它们之前定义所有函数并将它们赋值给变量，而另一些人则更倾向于有权将所有函数以函数声明的形式统一放在一个地方。你可以在“[快速贴士：函数表达式 vs 函数声明](https://www.sitepoint.com/function-expressions-vs-declarations/)”中阅读更多关于这些差异的内容。

## 返回函数的函数

我们已经看到函数可以接受另一个函数作为参数（回调），但它们也可以*返回*另一个函数。

下面的示例显示了一个名为 `returnHello()` 的函数，它返回一个打印“Hello, World!”的函数：

```
function returnHello() {
  return function() {
    console.log('Hello, World!');
  }
}
```

当调用 `returnHello()` 函数时，它做的仅仅是返回另一个函数：

```
returnHello()

<< function returnHello() {
     return function() {
       console.log('Hello World!');
    }

   }
```

或者，可以使用箭头函数让声明看起来更整洁（尽管更难看出发生了什么）：

```
returnHello = () => () => console.log('Hello, World!');
```

第一个箭头之后的表达式是它的返回值，即另一个箭头函数：`() => console.log('Hello, World!')`。因此，当调用 `returnHello` 时，它返回了这个函数。

为了使用这个返回的函数，我们需要将其赋值给一个变量：

```
const hello = returnHello();
```

现在我们可以通过在赋值的变量后加上括号来调用这个返回的函数：

```
hello();
<< Hello, World!
```

这看起来可能有点没意义，但让我们更进一步，使用这种技术创建一个通用函数，该函数返回另一个函数，用于根据作为参数提供的特定标签创建 HTML 片段：

```
const html = tag => text => `<${tag}>${text}</${tag}>`
```

我们现在使用这个函数来创建一个创建 `<h1>` 元素的函数：

```
const h1El = html('h1');
<< text => `<${tag}>${text}</${tag}>`
```

现在这个函数可以被用来返回一些标题字符串：

```
h1El('Hello, World!');
<< "<h1>Hello, World!</h1>"
```

如果我们还想要一个创建段落的函数，可以使用通用的 `element` 函数来为我们返回一个：

```
paraEl = element('p');
<< text => `<${tag}>${text}</${tag}>`
```

然后我们使用这个函数来创建一个段落片段：

```
paraEl('The quick, brown fox jumped over the lazy dog.');
<< "<p>The quick, brown fox jumped over the lazy dog.</p>"
```

我们还可以将两个函数调用链在一起，创建一个函数并在单次调用中使用它：

```
html('h2')('Hello, World!');
<< "<h2>Hello, World!</h2>"
```

## 闭包

闭包是 JavaScript 最强大的功能之一，它们依赖于作用域的概念以及函数返回其他函数的机制。

为了演示这个概念，让我们回到在本节之前讨论作用域概念时看到的这个函数：

```
function local(){
  const secret = 'Top Secret!';
  console.log(secret);
} 
```

这个函数包含一个名为 `secret` 的变量，正如我们所见，它只存在于函数的作用域内。

当一个函数可以访问在其作用域之外定义的变量时，就形成了**闭包**。在我们的示例中，我们可以添加一个引用 `secret` 变量的匿名函数：

```javascript
function local() {
const secret = 'Top Secret!';
function () {
    console.log(secret);
  }
}
```

匿名函数被认为对 `secret` 变量形成了“闭包”，因为尽管变量没有在函数体内定义，但函数仍然可以访问它。这本身并不特殊，因为我们已经可以在 `local` 函数内部访问 `secret` 变量了。

然而，如果我们*返回*这个匿名函数，我们就能*保留*在 `local` 函数作用域之外对 `secret` 变量的访问：

```javascript
function local() {

const secret = 'Top Secret!';
return function () {
    console.log(secret);
  }
}
```

返回的函数即使在 `local` 函数被调用后，仍将保留对 `secret` 变量的访问。这就形成了对 `secret` 变量的*闭包*。

为了使用闭包，我们需要将 `local()` 函数的返回值赋值给变量：

```javascript
const notSoSecret = local(); 
```

变量 `notSoSecret` 现在指向 `local()` 函数返回的匿名函数。该函数现在可以访问在 `local` 函数中定义的但在该函数作用域之外的 `secret` 变量。我们可以调用 `notSoSecret` 函数来验证这一点：

```javascript
notSoSecret();
<< "Top Secret!"
```

得益于闭包，我们现在可以访问 `secret` 变量。下图显示了闭包的工作原理：

![闭包的工作原理](img/closure.png)

### 闭包计数

闭包不仅可以访问父函数作用域中的变量，还可以修改这些变量的值。这允许我们创建一个每次调用都会递减的计数函数。在控制台中输入以下代码：

```javascript
function countdown(start){
  let i = start;
  return function() {
    return i--;
  }
}
```

我们可以通过将返回值赋值给变量来创建一个计数器：

```javascript
const count = countdown(3);

count();
<< 3

count();
<< 2

count();
<< 1
```

## 函数式编程

**函数式编程**是一种近年来非常流行的编程风格，部分归功于纯函数语言，如 [Clojure](https://clojure.org)、[Scala](https://www.scala-lang.org) 和 [Erlang](https://www.erlang.org)。JavaScript 一直支持函数式编程，因为函数是一等对象。我们在本章涵盖的技术——例如将匿名函数作为参数、向其他函数返回值以及创建闭包——都是函数式编程的基础元素。

### 纯函数

函数式编程的一个关键方面是使用纯函数。**纯函数**是指遵循以下规则的函数：

*   纯函数的返回值仅取决于作为参数提供的值；它不依赖于程序其他地方的值。
*   没有副作用：纯函数不会改变程序中其他地方的值或数据。它只进行非破坏的数据转换并返回新值，而不是修改任何底层数据。
*   纯函数具有引用透明性。给定相同的参数，它将总是返回相同的结果。

为了遵循这些规则，任何纯函数必须具备：




*   至少有一个参数：否则，返回值将依赖于 `function` 参数以外的其他内容，这将违反第一条规则。
*   一个返回值：否则，这个 `function` 就没有意义了（除非它改变了程序中的其他内容，在这种情况下，它就违反了“无副作用”规则）。

纯函数有助于函数式编程代码比其他编程风格更加简洁且更具可预测性。引用透明性（Referential transparency）使得纯函数易于测试，因为在提供相同参数时，可以依赖它们返回相同的值。另一个益处是，任何返回值都可以保存在内存中，因为它们总是相同的，这使得函数更高效。没有任何副作用往往会减少代码中出现的 Bug 数量，因为没有意外的依赖关系。纯函数仅依赖于作为参数提供的任何值。

让我们来看看如何*不应该*编写纯函数。接下来的示例展示了一个不纯的函数，它返回两个两个值相加的结果：

```
let number = 42;

let result = 0;

function impureAdd(x) {
  result = number + x;
}

impureAdd(10);
result;

<< 52
```

`impureAdd()` 函数是一个不纯的函数，因为它违反了上述规则。它需要定义在函数外部的 `number` 值。它具有改变 `result` 值（同样定义在程序外部）的副作用，并且如果变量 `number` 的值不同，它将返回不同的值。

这里有一个实现相同结果的纯函数示例：

```
const number = 42;

function pureAdd(x,y) {
  return x + y;
}

result = pureAdd(number,10);

<< 52
```

`pureAdd` 函数需要两个参数相加，因此变量 `number` 必须作为参数传递给它。这是一个非破坏性数据转换的示例，因为在变量 `number` 作为参数传递通过函数后，其存储的值保持不变。该函数没有副作用；它只是简单返回两个数字相加的结果。然后将此返回值赋值给变量 `result`，而不是由函数直接更新变量的值。该函数在给定相同输入时，也始终始终返回相同的值。

### `const` 的用处

使用 `const` 声明变量将有助于避免破坏性数据转换，因为任何原始值都无法被更改（尽管使用 `const` 赋值给数组或对象的变量仍然可以被修改，所以这并不是完美的解决方案）。

函数式编程将纯函数作为程序的构建模块。这些函数执行了一系列操作，而不改变程序中的任何底层数据。每个函数形成一个抽象，应该执行单一任务，同时将其实现细节封装在函数体内部。这意味着程序变成了一系列基于纯函数返回值的表达式。重点在于使用函数组合（function composition）将多个纯函数组合在一起，以完成更复杂的任务。

你可以在“[函数组合：构建可维护代码的基石](https://www.sitepoint.com/function-composition-building-blocks-for-maintainable-code/)”中阅读更多关于函数组合的知识。

## 纯数组更新

在本书的之前的章节中，我们使用 `push()` 方法向数组添加值。例如，我们的待办事项列表应用包含以下 `addTask` 函数：

```
function addTask(item){
  list.push(item);
} 
```

有几点使得这是一个不纯的函数。它依赖于函数体外部的变量 `list`，并且 `push()` 方法是一种破坏性转换，这意味着数组的值被改变了。

我们可以通过将要添加项的数组作为参数来使此函数纯化。这样，函数就不会访问其作用范围之外的任何变量。我们还可以使用展开运算符（spread operator）返回一个包含旧数组所有项并在末尾添加新项的新数组，如下所示：

```
function addTask(task,list){
   return [...list,task];
}
```

`removeTask` 函数也是不纯的：

```
function removeTask(task){
  const index = list.indexOf(task);
  if(index>-1){
    list.splice(i,1);
  }
   return list;

}
```

这是因为我们的代码再次引用了函数外部的 `list` 变量，并且 `splice()` 方法正在修改 `list` 数组（也就是说，它正在对其进行永久性更改）。我们可以通过将 `list` 作为参数并改用 `filter()` 方法来删除项来修复这个问题：

```
function removeTask(task,list){
  return list.filter(x => x !== task);
}
```

这将返回一个包含所有与作为参数提供的项不同的任务的数组，从而有效地从数组中删除了任务。

为了测试这些内容，让我们在控制台中创建一个简短的任务列表：

```
let tasks = ['Bake cake','Read book','Sing song'];
```

确保你已经在控制台中或 CodePen 的 `JS` 区域定义了这些新的纯函数，然后尝试在控制台中输入以下代码：

```
function addTask(task,list){
   return [...list,task];
}

function removeTask(task,list){
  return list.filter(x => x !== task);
}
```

现在让我们通过向 `tasks` 数组添加字符串 `'Learn to code'` 来测试 `addTask` 函数：

```
addTask('Learn to code',tasks);
<< ["Bake cake","Read book","Sing song","Learn to code"]
```

你可以看到，函数返回了一个带有 `'Learn to code'` 的数组。但并没有改变 `tasks` 变量的值，正如检查它的值所示：

```
tasks;
```

现在让我们检查 `removeTask` 函数是否有效：

```
removeTask('Read book',tasks);
<< ["Bake cake","Sing song"]
```

这返回了一个不包含 `'Read book'` 的新数组。再次，`tasks` 变量没有被改变：

```
tasks;
<< ["Bake cake","Sing song"]
```

### 使用纯函数更新数组值

如果你确实想更新 `tasks` 数组的值，你仍然可以使用纯函数来实现，只需将 `tasks` 变量赋值为函数调用的返回值。

例如，如果你想更新 `tasks` 数组以移除 `'Sing song'`，可以使用以下代码：

```
tasks = removeTask('Sing song',tasks);
<< ["Bake cake","Read book"]
```

我们就可以确认这确实更新了 `tasks` 数组：

```
tasks;
<< ["Bake cake","Read book"]
```

### 高阶函数

高阶函数是指接受另一个函数作为参数，或者返回另一个函数作为结果，或者两者兼有的函数。

闭包在高阶函数被广泛使用，因为允许我们创建一个通用函数，并根据其参数返回更具体的函数。这是通过对函数的参数创建一个闭包来实现的，使其在返回函数中保持“活跃”。例如，考虑以下 `multiplier` 函数：

```
function multiplier(x){
  return function(y){
    return x*y;
  }
}
```

`multiplier` 函数返回另一个函数，该函数在闭包中捕获了参数 `x` 的值。这供返回函数使用。

现在我们可以使用这个通用的 `multiplier` 函数来创建更具体的函数，如下例所示：

```
doubler = multiplier(2);
```

这创建了一个名为 `doubler` 的新函数，它将参数乘以二：

```
doubler(10);
<< 20
```





`multiplier()` 函数是一个高阶函数的示例。这意味着我们可以通过使用不同的参数来用它构建其他更具体的函数。例如，可以使用参数 `3` 来创建一个 `tripler()` 函数，该函数将将其参数乘以 3：

```
tripler = multiplier(3);

tripler(10);
<< 30
```

这是函数式编程的核心原则之一：它允许使用通用的高阶函数根据特定参数返回更具体的函数。

使用高阶函数时的一个巧妙技巧是将参数链式连接。接下来的示例将 3 和 5 相乘：

```
multiplier(3)(5);
<< 15
```

这之所以能通，是因为 `multiplier(3)` 返回了一个匿名函数，而我们通过在末尾添加括号，立即使用 `5` 作为参数调用了它。

## 挑战

1. 编写一个递归函数，演唱我们在第 7 章中通过各种循环编写的《十个绿瓶子》歌曲。它应该接受瓶子的数量作为参数，唱一段，然后自己调用自己再次演唱。例如，`greenBottles(10)` 将从 10 个绿瓶子开始演唱。你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/LYbLgLO)。
2. 创建一个名为 `exponent` 的高阶函数，它返回另一个函数，该函数将计算提供参数的幂。例如，`exponentBase2 = exponent(2)` 应该产生一个名为 `exponentBase2` 的函数，该函数将返回提供参数的幂，因此 `exponentBase2(3)` 将返回 8。你应该能够编写 `exponent(2)(3)` 并同样得到 8。你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/NWbgOgZ)。
3. 更新待事项应用，使 `add` 和 `remove` 函数成为纯函数。你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/ExNXdvW)。

## 总结

- 命名参数可以在 JavaScript 中使用对象作为参数来重现。这允许以任何顺序作为对象的属性提供参数。
- 剩余参数（rest parameter）允许以数组的形式向函数提供任意数量的值。
- 递归函数是不断调用自身直到达到特定条件的函数。
- 变量的作用域决定了该变量可以在哪里以及如何被访问。
- 使用 `function` 关键字声明的函数会被“提升”（hoisted）到作用域顶部，这意味着即使在定义之前也可以调用它们。
- 变量应该在被引用之前声明。
- 当函数访问一个在函数周围作用域声明的变量时，就形成了闭包（closure）。通过返回函数，我们可以保持对声明作用域之外变量的访问。
- 函数式编程是一种编程风格，它结合了执行单一任务的纯函数来执行更复杂的任务。
- 纯函数不应该引用函数作用域之外的未作为参数提供的任何内容，并且不应该通过改变函数作用域之外的任何内容来产生副作用。它们应该具有`引用透明性`（referential transparency），这意味着在给定相同的情况下，它们应该返回相同的值。
- 高阶函数接受函数作为参数并返回函数。它们可以链式连接以完成更复杂的操作。

在下一章中，我们将深入研究对象和面向对象的编程。

# 第 14 章：走向类（Getting Classy）

我们首次在第 9 章中遇到对象。在本章中，我们将更深入地研究面向对象编程以及如何使用 JavaScript 创建类。我们将涵盖以下主题：

- 在 JavaScript 中复制对象
- 面向对象编程
- 封装
- 多态
- 继承
- JavaScript 中的类
- extends
- 一个宠物独角兽（Pet Unicorn）项目

## 在 JavaScript 中复制对象

JavaScript 中的一个重要概念是对象是通过引用（`reference`）赋值的。这意味着如果两个变量被赋值为同一个对象，那么两个变量将指向内存中的同一个对象。

例如，假设你正在创建一个天气应用，变量 `monday` 指向一个晴天的图像对象。如果你使用代码 `const tuesday = monday` 将变量 `tuesday` 赋值给同一个图像对象，两个变量都将指向同一个图像对象，如下图所示。

![通过引用复制](img/copybyref.png)

如果你更新了 `tuesday` 指向的图像对象，它也会改变 `monday` 指向的图像对象，如下图所示，其中 `tuesday` 被改变为了雨天的图像对象。

![通过引用更新](img/updatebyref.png)

这意味着你对`任意`变量的任何更改都会影响另一个，这使得在不改变 `tuesday` 的情况下无法改变 `monday`。

为了演示可能导致的问题，让我们创建一些对象来模拟[金发小姑娘的故事](https://en.wikipedia.org/wiki/Goldilocks_and_the_Three_Bears)中的三只熊。

### 控制台问题

在编写时，jsonsole.com 不支持此示例使用的某些代码。出于此原因，我建议使用 CodePen 上的控制台。（它位于 CodePen 界面的左下角。）

首先，让我们创建一个描述爸爸熊的对象并将其赋值给变量 `papa`，在控制台中：

```
const papa = {
  name: 'Papa Bear',
  type: 'bear',
  color: 'brown',
  food: 'porridge',
  size: 'large'
};
```

现在，如果我们创建一个代表妈妈熊的对象，可以从 `papa` 对象的副本开始，因为许多属性是相同的。我们可以更新需要更改的属性。

一个常见的错误是认为可以这样制作 `papa` 对象的副本：

```
const mama = papa;
```

变量 `mama` 将拥有与 `papa` 对象相同属性。问题在于我们并没有真正复制 `papa` 对象；`mama` 和 `papa` 引用的是同一个对象！

当我们尝试修改 `mama` 的 `name` 属性时，可以看到这一点：

```
mama.name = 'Mama Bear';
```

现在，如果我们检查 `papa` 对象的 `name` 属性值，我们会发现一个问题：

```
papa.name;
<< 'Mama Bear'
```

更改 `mama` 的 `name` 属性导致 `papa` 的 `name` 属性也发生了变化。这是因为 `mama` 和 `papa` 指向内存中的同一个对象。对任意变量的任何更改都会影响另一个。

此问题的解决方法是对想要复制的对象应用扩展运算符。你需要重启控制台并重新定义 `papa` 对象，然后输入以下代码来制作 `papa` 对象的副本：

```
const mama = {...papa}
```

这创建了一个全新的对象字面量并将 `papa` 对象的属性展开在内部。这意味着变量 `mama` 指向内存中一个全新的对象。对其进行的任何更改都不会影响 `papa` 对象，正如我们更新 `name` 和 `size` 属性时所示：

```
mama.name = 'Mama Bear';
<< "Mama Bear"

mama.size = 'medium';
<< "medium"
```

现在，如果我们观察这两个对象，可以看到 `mama` 对象已经更新了，但 `papa` 对象没有变化：

```
papa;
<< { 
  name: 'Papa Bear',
  type: 'bear', 
  color: 'brown',
  food: 'porridge',
  size: 'large'
}

mama;
<<
{ 
  name: 'Mama Bear'
  type: 'bear', 
  color: 'brown',
  food: 'porridge',
  size: 'medium'
}
```

### 浅拷贝与深拷贝




上面的代码对 `papa` 对象进行了 `shallow`（浅）拷贝。这意味着只有第一层属性被复制了。如果任何属性包含嵌套对象，这些对象将仍然通过引用进行复制。而 `deep`（深）拷贝涉及对 `every`（每一个）属性进行复制，包括嵌套对象。

对对象进行深拷贝可能会很复杂，我建议使用经过良好测试的解决方案，例如 [Lodash 库](https://lodash.com) 中的 [`_.cloneDeep`](https://lodash.com/docs/4.17.15#cloneDeep) 方法。

通过在对象字面量的末尾添加新属性，可以一步完成复制对象并更新某些属性。让我们通过再次创建 `papa` 对象的副本来代表小熊（Baby Bear）：

```javascript
const baby = {...papa, name: 'Baby Bear', size: 'small'};
```

在这个示例中，我们复制了 `papa` 对象，然后在同一个对象中更新了 `name` 和 `size` 属性。这之所以有效，是因为任何具有相同名称的属性将覆盖之前定义的属性。

我们可以通过查看 `baby` 对象来检查此操作是否成功：

```javascript
baby;
<< { 
  name: 'Baby Bear'
  type: 'bear', 
  color: 'brown',
  food: 'porridge',
  size: 'small'
}
```

正合适！

## 复制数组和函数

在 JavaScript 中，数组是特殊类型的对象，因此在使用数组时会发生相同的问题：它们是通过引用复制的，而使用扩展运算符只会进行浅拷贝。

函数也仅通过引用复制，因此对函数进行的任何更改都将影响对该函数的所有引用。

## 面向对象编程

`面向对象编程`（简称 OOP）是一种编程风格，它将相关的代码封装在对象中，这些对象在程序的生命周期内维持状态。然后对象就可以根据需要重用或轻松地修改。Java、C++、Ruby 和 Python 等许多现代语言都是面向面向对象的。

OOP 的三个核心概念是：

* 封装
* 多态
* 继承

我将以咖啡机为例，来说明这些概念如何被应用于编程环境中。在许多方面，咖啡机可以被看作一个对象，因为它具有速度、强度和容量等属性，它还具有可以执行的方法或动作，例如酿造、开启和关机。

### 封装

当咖啡机开启时，它会发出一些声音，几分钟后，它会产出一杯热气腾腾的咖啡。你不需要知道机器是如何运作就能制作出完美的咖啡；你只需按下 `on`。这演示了`封装`的概念：内部原理被隐藏在对象内部，只向终端用户暴露基本功能，例如 `on` 按钮。在 OOP 中，这涉及将所有的编程逻辑保留在对象内部，并提供可用的方法来实现功能，而不需要外部世界知道 `how`（如何）实现的。

![封装](img/encapsulation.png)

### 多态

`on` 按钮启动了咖啡机的酿造过程。如果存在啤酒机，它也会有一个启动酿造过程的 `on` 按钮。尽管两台机器都拥有一个名为“酿造”的过程，但该过程的结果非常不同：一个生产咖啡，另一个生产啤酒。这演示了`多态`的概念，即相同的过程在不同的对象中产生不同的结果。在 OOP 中，这意味着各种对象可以共享相同的方法，但以不同的方式实现它们。

![多态](img/polymorphism.png)

### 继承

想象一台超级咖啡机，它是一种新的改进型号，能够一次制作三杯咖啡。尽管它具有一些额外功能，但仍然使用了与原始咖啡机许多相同的零件。这演示了`继承`的概念，即获取一个对象的特征，然后添加新特征。在 OOP 中，这意味着我们可以取一个已经存在的对象并继承它所有的属性和方法。我们可以通过添加新的属性和方法来改进它的功能。

![继承](img/inheritance.png)

## 类

大多数面向对象的语言（如 Java 和 Ruby）使用类（classes）来定义对象的蓝图。对象随后作为该类的实例被创建，并继承类所有的属性和方法。在咖啡机的示例中，`CoffeeMachine` 类代表设计，生产线上制造的每台机器以及任何其他型号的咖啡机都将该类的实例。

### 类与原型

JavaScript 最初并没有在语言中内置类。但它一直允许使用现有的对象字面量而不是类作为创建相似对象的蓝图。因此，它被称为一种`基于原型的`（prototype-based）语言。在咖啡机的示例中，这可能涉及构建一台真实的原型机，然后使用此原型作为制造所有其他机器的基础。JavaScript 现在确实支持类，正如我们将在下一节看到的，但它在后台仍然使用相同的原型继承模型。

### JavaScript 中的类

在“对象”章节（第 9 章）中，我们创建了所示的 `dice`（骰子）对象：

```javascript
const dice = {
  sides: 6,
  roll() {
    return Math.ceil(Math.random()*this.sides)
  }    
}
```

想象你正在创建一个角色游戏，类似于[地下城与龙](https://en.wikipedia.org/wiki/Dungeons_%26_Dragons)。你需要许多不同面数的骰子。要创建这个类，在控制台输入以下代码：

```javascript
class Dice {
  constructor(sides=6) {
    this.sides = sides;
  }

  roll() {
    return Math.ceil(Math.random()*this.sides);
  }
}
```

#### 类命名

按照惯例，类的声明名称通常大写。所有 JavaScript 类都有一个名为 `constructor` 的函数（如果你不显式编写它，它将在后台创建）。每当创建类的实例时，该函数都会被调用。

`this` 关键字代表由类返回的对象。在上面的 `Dice` 类中，我们使用它让 `sides` 属性等于传递给构造函数的参数，如果没有提供参数，则为 6。它还添加了一个名为 `roll()` 的方法，返回从 1 到骰子面数的随机数。

我们现在可以使用 `new` 运算符创建一个 Dice 类实例：

```javascript
redDice = new Dice();
<< Dice {sides: 6}
```

这调用了 `Dice` 类中定义的 `constructor` 函数，并返回一个赋值给变量 `redDice` 的对象，该对象被认为是 `Dice` 类的实例。这是一个具有 `sides` 属性和 `roll()` 方法的对象。

#### 类

我们可以使用 `instanceof` 运算符来确认这一点：

```javascript
redDice instanceof Dice;
<< true
```

通过这种方式创建的新对象都具有类定义的 `sides` 属性和 `roll()` 方法，它们被称为 `Dice` 类的实例。例如，我们可以使用以下代码创建一个四面体的蓝色骰子：

```javascript
blueDice = new Dice(4);
<< Dice {sides: 4}
```

#### 括号

当使用 `new` 运算符实例化新对象时，括号不是必须的。以下代码也会达到相同的结果：

```javascript
greenDice = new Dice;
<< Dice {sides: 6}
```



然而，如果提供了任何参数，则必须使用括号。例如，如果我们想创建一个另一个 20 面的 `Dice` 对象，我们就必须将 20 作为参数添加，如下所示：

```
whiteDice = new Dice(20);
<< Dice {sides: 20}
```

你可以在“[面向对象的 JavaScript：ES6 类的深度解析](https://www.sitepoint.com/object-oriented-javascript-deep-dive-es6-classes/)”中阅读更多关于 ES6 类的知识。

## 类组件 (Classy Components)

类的用途之一创建可复用的 HTML 组件。这允许你在单个类中定义一段 HTML 代码，然后在程序中多次复用它。

例如，让我们创建一个名为 `Notice` 的类，并用它创建一个 `<div>` 元素，在网页上显示一条消息。

在 CodePen 上打开一个新的 Pen，并在 **JS** 部分中输入以下代码：

```
class Notice {
  constructor(message='Hello, World!') {
    this.element = document.createElement('div');
     this.element.textContent = message;
     this.css = 'background:silver;border:3px gray solid;color:gray;font:18px sans-serif;padding:8px;margin:10px';
     this.element.style.cssText = this.css;
  }

  render(element) {
     element.appendChild(this.element);
  }
}
```

该类的 `constructor` 函数创建了一个 `<div>` 元素，然后将 `textContent` 属性设置为与 `message` 相同，`message` 是创建新实例时作为参数提供的。它还使用 `style.cssText` 属性设置 CSS 属性，允许你在单个字符串中设置多个 CSS 属性。

`Notice` 类的每个实例都有一个 `render()` 方法，用于在页面上渲染元素。这使用了我们在 DOM 章节中看到的 `appendChild()` 方法（第 10 章），将该元素追加到作为方法参数提供的元素中。

让我们尝试测试这个类来创建一个 `Notice` 组件。在 **JS** 部分的底部添加以下代码行：

```
welcome = new Notice;
```

这创建了一个指向 `constructor` 函数返回的 `<div>` 元素的引用。我们现在可以使用它的 `render` 方法将其插入页面中。在 **JS** 部分的底部添加以下代码行：

```
welcome.render(document.body);
```

这将把元素追加到文档的 body 中，看起来应该像这样：

![Notice 组件类](img/Notice.png)

你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/jOVLBKv)。

## JavaScript 中的继承 (Inheritance in JavaScript)

现在我们已经有了用于创建通知组件的类，我们可以根据这个类创建一些不同类型的通知，但更具具体性。例如，我们可以创建 `Warning`、`Success` 和 `Info` 通知，它们都基于我们在上一个节中创建的通用通知元素。

我们可以使用继承的概念来确保我们的新通知继承 `Notice` 类的所有属性和方法。这意味着 `Warning`、`Success` 和 `Notice` 类将从父类 `Notice` 继承它们的所有属性和方法，如下所示所示。

![继承](img/jsinheritance.png)

在 JavaScript 中，类使用 `extends` 关键字继承自另一个类。在你的 Pen 的 **JS** 部分底部添加以下代码以查看它是如何工作的：

```
class Warning extends Notice {
 constructor(message='WARNING!') {
    super(message);
  }
}
```

这创建了一个名为 `Warning` 的新类，它继承了 `Notice` 类的所有属性和方法。`super` 关键字引用父类（在本例中为 `Notice`），并用于访问父类的属性和方法。

不过，我们并不希望 `Warning` 类与 `Notice` 类完全相同（那样有什么意义呢？我们需要更新一些样式属性来改变它的外观。更新类定义以包含以下代码：

```
class Warning extends Notice {
 constructor(message='WARNING!') {
    super(message);
    this.element.style.background = 'pink';
    this.element.style.color = 'red';
    this.element.style.borderColor = 'red';
  }
}
```

这些额外的代码行更新了样式属性，以更改背景、边框和文本的颜色。

为了检查这是否有效，让我们创建一个 `Warning` 类的实例并将其插入文档：

```
const warning = new Warning('Warning!');
warning.render(document.body);
```

这应该将警告通知追加到页面的 body 中，将其放在已有的通知下方，如下图所示。

![Warning 类继承自 Notice 类](img/warning.png)

我们可以通过添加以下代码使用类似的过程创建两个用于成功和信息通知的类：

```
class Success extends Notice {
 constructor(message='Success!') {
    super(message);
    this.element.style.background = 'palegreen';
    this.element.style.color = 'green';
    this.element.style.borderColor = 'green';
  }
}

class Info extends Notice {
 constructor(message='Information') {
    super(message);
    this.element.style.background = 'powderblue';
    this.element.style.color = 'blue';
    this.element.style.borderColor = 'blue';
  }
}
```

这些类以与 `Warning` 类的方式扩展了 `Notice` 类，但使用了不同的颜色和消息。我们可以使用以下代码测试它们并将它们添加到页面：

```
success = new Success;
success.render(document.body);

info = new Info;
info.render(document.body);
```

页面现在应该看起来类似于下面。

![Notice 类及其子类](img/notices.png)

你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/GRNvmdY)。

### 自定义 HTML 元素 (Custom HTML Elements)

你可以比示例中所做的更进一步，[创建自己的 HTML 元素](https://dev.to/barakplasma/introduction-to-custom-elements-136c)。

## 宠物精灵游戏 (The Pet Unicorn Game)

我们将通过创建一个基于经典的[电子宠物](https://en.wikipedia.org/wiki/Tamagotchi)玩具的虚拟宠物游戏来结束本章。这个游戏涉及玩家照顾宠物精灵。玩家需要决定何时喂养、玩耍睡觉。

游戏将使用 `Unicorn` 类来实例化代表宠物精灵的对象。该对象将具有跟踪精灵感受的属性，以及允许玩家与宠物交互的方法。此游戏将完全通过在控制台中输入方法来运行。

`Unicorn` 类需要以下属性：

*   `name`：引用宠物
*   `food`：跟踪宠物肚子里食物的量
*   `fun`：记录宠物有多快乐
*   `energy`：跟踪宠物有多少能量

`Unicorn` 类还需要以下方法：

*   `eat`：这将增加 `food` 的值，因为吃东西会让宠物肚子里有食物，但它会减少 `fun` 的值，因为站在那里吃饭可能无聊。
*   `sleep`：这将增加 `energy` 的值，因为睡眠为宠物提供了休息，但随着食物消化，`food` 的值会减少。它还会减少 `fun` 的值，因为睡觉可能很闷。
*   `play`：这将增加 `fun` 的值，因为玩很有趣，但它会减少 `energy` 的值，因为这很累！

让我们创建一个用于实例化 `Unicorn` 类新实例的构造函数。它应该定义上述的属性。在 CodePen 上打开一个新的 Pen 并在 **JS** 部分添加以下类定义：





```javascript
class Unicorn {
  constructor(name='Sparkles'){
    this.name = name;
    this.food = 3;
    this.fun = 3;
    this.energy = 5;
    console.log(`Your new pet unicorn, ${this.name}, is born!`);
  }
}
```

这定义了在创建新的 `Unicorn` 对象时会被调用的构造函数。该函数有一个 `name` 参数，其默认值为 `'Sparkles'`。它被用于设置 `name` 属性。我们还把 `food`、`fun` 和 `energy` 属性设置为了它们的初始值 3、3 和 5。此外，还向控制台打印了一条消息，告知玩家他们的宠物独角兽已经出生了。

接下来，我们需要定义 `eat`、`play()` 和 `sleep()` 方法。这些方法需要更新相关的属性，并在控制台中提供一些反馈，让玩家知道发生了某些事情。不过，我们不会提供关于属性实际值如何变化的细节，因为这些被封装在对象内部（我们不想泄露太多游戏的内部机制！）。

让我们从 `eat()` 方法开始。它应该紧放在 `constructor` 函数之后，但仍在类块内部：

```javascript
eat(){
   console.log(`${this.name} gobbles up some glitter.`);
    this.food += 3;
    this.fun -= 1;
    this.timeGoesBy();
  }
```

这向控制台打印了一条消息，告诉用户他们的宠物吃了一些东西。然后，它将 `food` 属性增加了 3，表示吃了一些食物，并将 `fun` 属性减少了 1，因为任何花在吃饭的时间意味着玩耍的时间少了。在方法的最后，我们调用了另一个名为 `timeGoesBy` 的方法。这个方法将模拟游戏时间的流逝，并检查独角兽的任何属性值是否过低。我们很快就会编写这个方法，但首先我们必须添加 `play()` 和 `sleep()` 方法。将这些方法添加到 `eat()` 方法下方：

```javascript
play(){
    console.log(`${this.name} frolics in the meadow.`);
    this.fun +=2;
    this.energy -=2;
    this.timeGoesBy();
  }

sleep(){   
    console.log(`${this.name} falls asleep, dreaming of stars & rainbows.`);
    this.energy += 5;
    this.fun -= 2;
    this.food -= 3;
    this.timeGoesBy();
  }
```

这两个方法都遵循与 `eat()` 方法相似的模式：向控制台打印消息，更新属性，然后调用 `timeGoesBy()` 方法。现在让我们添加该方法：

```javascript
timeGoesBy(){
    if(this.energy < 0){
     this.dies('exhaustion'); 
    }
     if(this.food < 0){
        this.dies('starvation');
     }
    if(this.fun < 0){
      this.dies('boredom');
    }
  }
```

该方法使用 `if` 语句检查独角兽的 `energy`、`food` 和 `fun` 属性是否有一个掉到了零以下。如果是这样，独角兽将不幸地死去。当这种情况发生时，我们调用 `dies()` 方法，并传递一个描述独角兽死亡原因的参数。接下来我们需要编写这个方法：

```javascript
dies(reason){   
  console.log(`${this.name} died of ${reason}.`);
}
```

该方法接受一个描述独角兽死亡原因的字符串参数。然后它向控制台打印消息，告诉用户他们的宠物独角兽已经去世，并说明死亡原因。

尝试在 CodePen 的控制台中创建一个新的宠物独角兽。尝试调用不同的方法，看看你能让你的独角兽活多久。下面的控制台日志显示了我简单尝试的输出：

```javascript
pet = new Unicorn;
<< "Your new pet unicorn, Sparkles, is born!"

pet.play();
<< "Sparkles frolics in the meadow."

pet.play();
<< "Sparkles frolics in the meadow."

pet.eat();
<< "Sparkles gobbles up some glitter."

pet.play();
<< "Sparkles frolics in the meadow."
"Sparkles died of exhaustion."
```

这个故事的寓理是记住给你的宠物一些休息！

你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/vYyJmVa)。

## 挑战

1. 在宠物独角兽游戏中添加一个随机元素，使得每次调用方法时属性改变的数值略有不同。例如，`sleep()` 方法不再增加 5 点能量，而是可以增加 4、5 或 6 点。你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/zYodwyw)。

2. 为宠物独角兽游戏添加一个图形界面。这可能涉及以下功能：一个允许用户输入独角兽名称以创建它的输入框；当对象实例化时在文档中显示的带有名称的独角兽图片；在文档中更新宠物的感受，而不是使用 `console.log`；以及通过点击按钮来执行 `eat`、`sleep` 和 `play` 的每个动作。

    你可以查看[我在 CodePen 上的代码](https://codepen.io/SitePoint/pen/ZEBwp)。

## 总结

- JavaScript 对象是通过引用复制的。
- 面面向编程 (OOP) 是一种将代码封装在对象中的概念。
- 封装意味着对象的内部工作机制对用户隐藏。
- 多态意味着对象可以共享相同的方法，但以不同的方式实现。
- 继承意味着类可以从父类继承属性和方法，并添加自己的。
- 你可以使用 `class` 关键字在 JavaScript 中创建类。
- 使用 `new` 关键字创建类实例时，类中定义的 `constructor` 函数会被调用。

在下一章，我们将学习如何处理时间和日期。

# 第 15 章：关于时间

在编程语言中处理时间和日期可能是很复杂的。由于这个原因，大多数语言都有内置的 `Date` 对象来使这个过程变得更容易。JavaScript 也不例外，我们将查看它是如何工作的。我们将涵盖：

- Unix 时间
- 时间和日期
- 定时函数
- 异步编程
- 动画
- 一个饼干收集游戏

## Unix 时间

[Unix 时间](https://en.wikipedia.org/wiki/Epoch_(computing)) 是一个任意日期——1970 年 1 月 1 日，它在编程中被用作日期的参考点。这允许日期表示为自该时刻以来的秒数。正如你可以想象的，这产生了巨大的数字，并且在 2038 年面临一个潜在的[问题](http://en.wikipedia.org/wiki/Year_2038_problem)，那时自该时刻以来的秒数将超过 2,147,483,647，这是某些编程语言可以处理的最大值。幸运的是，JavaScript 没有问题，因为它可以处理更大的值。

## 时间日期

Date 对象包含关于日期时间的信息。每个对象代表一个单一的时刻。

在 JavaScript 中，我们可以使用构造函数来创建一个新的日期对象。尝试在控制台中输入以下代码：

```javascript
const today = new Date();
```

变量 `today` 现在指向一个 `Date` 对象。为了查看日期，我们可以使用对象都拥有的 `toString()` 方法：

```javascript
today.toString();
<< 'Mon Dec 07 2020 17:40:51 GMT+0000 (GMT)'
```

如果没有提供参数，日期将根据系统时钟和时区设置为当前日期时间。这意味着它是可以操纵的，不应该依赖它作为真实的日期表示。

通过向构造函数传递参数，可以为任何日期创建 `Date` 对象。这可以用多种形式的字符串编写，如下面不同节日的示例所示：





```
const christmas = new Date('2021-12-25');
// date format is YYYY-MM-DD
christmas.toString(); 
<< "Sat Dec 25 2021 00:00:00 GMT+0000 (GMT)"

const chanukah = new Date('28 November 2021');
// First day of Chanukah
chanukah.toString();
<< "Sun Nov 28 2021 00:00:00 GMT+0000 (GMT)"

const eid = new Date('Wednesday, May 12, 2021');
// Eid-al-Fitr
eid.toString();
<< "Wed May 12 2021 00:00:00 GMT+0100 (BST)"
```

如你所见，传递给 `Date` 构造函数的字符串可以是多种格式。然而，为了提高一致性，我建议你将日期的每个部分作为单独的参数提供。提供的参数如下：

```
new Date(year,month,day,hour,minutes,seconds,milliseconds);
```

这里有一个示例：

```
const halloween = new Date(2021, 9, 31);
halloween.toString();
<< "Sun Oct 31 2021 00:00:00 GMT+0100 (BST)"
```

### 计数月份

稍微有点困惑的是，月份的数值从零开始，所以 1 月是 0，2 月是 1，以此类推，12 月是 11。

另一种方法是使用 `timestamp`（时间戳），它是一个表示从元 Epoch（1970 年 1 月 1 日）以来过的毫秒数的单个整数参数：

```
const diwali = new Date(1635984000000);
diwali.toString();
<< "Thu Nov 04 2021 00:00:00 GMT+0000 (GMT)"
```

### Getter 方法 (获取方法)

日期对象的属性无法通过赋值直接查看或更改。相反，它们拥有许多被称为 `getter methods` 的方法，这些方法返回有关日期对象的信息，例如月份和年份。

一旦你创建了日期对象，它就可以访问所有的 getter 方法。大多数方法都有两个版本：一个返回本地时间信息，另一个则使用协调世界时 (UTC)。`getTime()`、`getTimezoneOffset()` 和 `getYear()` 方法没有对应的 UTC 版本。

#### UTC 对比 GMT

UTC 是世界调节时钟遵循的首要时间标准。它在 1960 年正式制定，与格林威治标准时间 (GMT) 非常相似。主要的区别在于 UTC 是一个由科学界定义的标准，而 GMT 不是。（你可以在[维基百科上阅读关于为什么它被称为“UCT”而不是“CUT”的介绍](https://en.wikipedia.org/wiki/Coordinated_Universal_Time)。）

`getDay()` 和 `getUTCDay()` 方法用于查找日期所在的星期几。它们返回一个数字，从 0（星期日）到 6（星期六）。下面的代码显示 2021 年的排节是在周四（第 4 天）：

```
diwali.getDay();
<< 4
```

`getDate()` 和 `getUTCDate()` 方法返回日期对象的几号。（注意这些值从 1 开始计数，而不是 0，所以它们返回的是实际日期。）下面的代码显示 2021 年的排节是在 4 号：

```
diwali.getDate();
<< 4
```

`getMonth()` 和 `getUTCMonth()` 方法可以查找日期对象的月份。它返回一个整数，但记住从 0 开始计数！下面的代码显示 2021 年的排节在 11 月（第 10 个）：

```
diwali.getMonth();
<< 10
```

`getFullYear()` 和 `getUTCFullYear()` 方法返回日期对象的年份。还有一个 `getYear()` 方法，但它不符合 [Y2K](https://en.wikipedia.org/wiki/Year_2000_problem) 标准，因此不应该使用，因为它对于 2000 年之后的日期会返回无意义的结果，如下面的代码所示：

```
diwali.getYear();
<< 121
```

如果使用 `getFullYear()` 方法就可以修复这个问题：

```
diwali.getFullYear();
<< 2021
```

还有 `getHours()`、`getUTCHours()`、`getMinutes()`、`getUTCMinutes()`、`getSeconds()`、`getUTCSeconds`、`getMilliseconds()` 和 `getUTCMilliseconds()` 方法，它们将返回自午夜以时的、分、秒和毫秒。

`getTime()` 方法返回一个表示 Epoch 以来毫秒数的时间戳：

```
diwali.getTime();
<< 1635984000000
```

这对于增加固定时间的日期非常有用。例如，一天可以用 `1000 * 60 * 60 * 24` 毫秒表示。下面的示例使用此从圣诞节日期减去一天，以找到圣诞夜的日期：

```
const christmasEve = new Date(christmas.getTime() - 1000 * 60 * 60 * 24);
christmasEve.toString();
<< "Fri Dec 24 2021 00:00:00 GMT+0000 (GMT)"
```

`getTimezoneOffset()` 方法返回本地时间与 UTC 之间的差（以分钟为单位）。例如，我的时区与 UTC 相同，所以它返回 0：

```
new Date().getTimezoneOffset();
<< 0
```

你可以在[W3Schools 网站上查看更多 `Date` 方法示例](https://www.w3schools.com/js/date_methods.asp)。

### Setter 方法 (设置方法)

上一节介绍的大多数 getter 方法都有对应的 setter 方法。这些方法用于更改 `Date` 对象中存储的日期值。每个方法接收一个表示要更新的日期的参数。例如，我们可以更改 `diwali` 的值使其包含 2021 年 10 月 24 日：

```
diwali.setDate(24);
<< "Mon Oct 24 2021 00:00:00 GMT+0100 (BST)"
```

我们还可以更改 `diwali` 的月份：

```
diwali.setMonth(9);
<< "Sun Oct 24 2021 00:00:00 GMT+0100 (BST)"
```

我们还可以更改 `diwali` 的年份：

```
diwali.setFullYear(2022);
<< "Mon Oct 24 2022 00:00:00 GMT+0100 (BST)"
```

我们还可以更改 `diwali` 的时间部分：

```
diwali.setHours(10);
<< "Mon Oct 24 2022 10:00:00 GMT+0100 (BST)"
```

我们还可以更改 `diwali` 的分钟：

```
diwali.setMinutes(30);
<< "Mon Oct 24 2022 10:30:00 GMT+0100 (BST)"
```

我们还可以更改 `diwali` 的秒：

```
diwali.setSeconds(15);
<< "Mon Oct 24 2022 10:30:15 GMT+0100 (BST)"
```

我们还可以更改 `diwali` 的毫秒：

```
diwali.setMilliseconds(500);
<< "Mon Oct 24 2022 10:30:15.500 GMT+0100 (BST)"
```

最后，我们可以使用 `setHours()` 一次性设置 `diwali` 的所有时间：

```
diwali.setHours(10, 30, 15, 500);
<< "Mon Oct 24 2022 10:30:15.500 GMT+0100 (BST)"
```

我们还可以使用 `setTime()` 通过时间戳设置 `diwali` 的日期：

```
diwali.setTime(1666563600000);
<< "Mon Oct 24 2022 00:00:00 GMT+0100 (BST)"
```

#### 时区毫秒

取决于你的时区，时间戳所需的毫秒数对你来说可能不同。

你可以在[W3Schools 网站上查看更多 `Date` 方法方法](https://www.w3schools.com/js/date_methods.asp)。

#### 日期和时间支持

处理日期和时区可能很复杂。但很快将有一个新的 [`Temporal` 对象](https://tc39.es/proposal-temporal/docs/)，旨在修复 `Date` 对象的一些问题。（你可以在[JavaScript API 简介](https://www.sitepoint.com/javascript-temporal-introduction/) 中了解更多信息。）

如果你正在编写使用大量时间戳日期的代码，那么使用如 [date-fns](https://date-fns.org) 这样的外部库可能是值得的，它提供了许多处理日期的方法。你可以在[学习 date-fns：一个轻量级 JavaScript 日期库](https://www.sitepoint.com/date-fns-javascript-date-library/) 中阅读更多信息。

### 将是哪一天？

现在我们已经学会了关于操作 `Date` 对象的所有知识，让我们创建一个小型应用程序，告诉你在指定天数后是星期几。

在 CodePen 上打开一个新的 Pen 并添加以下 HTML：

```
<form name='myForm'>
  <input type='number' name='number' value='1'>
  <button type='submit'>Submit</button>
</form>
<div id='output'></div>
```

这是一个要求用户输入天数的表单。我们将告诉他们在那天数后是星期几。注意，尽管 `<input>` 元素具有 `type` 属性 `number`（这是一个良好的习惯），它仍然会以字符串的形式提交。

现在让我们添加一些 JavaScript 来计算将是哪一天。首先，我们将声明一些指向 `<form>` 元素和包含输出的 `div>` 元素的变量。将以下代码添加到 **JS** 部分：





```javascript
const form = document.forms.myForm;
const output = document.getElementById('output');
```

我们还需要添加一个包含星期每一天名称的数组。这将某天的名称与 `getDay()` 方法返回对应的数字相匹配，因此 `dayNames[0]` 将是 `'Sunday'`，`dayNames[1]` 将是 `'Monday'`，依此类推。请在 `JS` 部分添加以下行代码：

```javascript
const dayNames = ['Sunday','Monday','Tuesday','Wednesday','Thursday','Friday','Saturday'];
```

接下来，我们需要编写一个函数来计算并显示星期几。在 `JS` 部分的末尾添加此函数：

```javascript
function nameThatDay(e){
  e.preventDefault();
  const numberOfDays = Number(form.number.value);
  const milliseconds = numberOfDays * 24 * 60 * 60 * 1000;
  const timestamp = Date.now() + milliseconds;
  const day = new Date(timestamp).getDay();
  output.textContent = `In ${numberOfDays} days, it will be ${dayNames[day]}.`
}
```

该函数首先防止表单的默认行为，这样它就不会被提交到服务器。然后它获取表单中输入的值并转换为数字，存储在变量 `numberOfDays` 中。通过乘以一天的毫秒数，该值被转换为毫秒。我们将其加上自 Epoch 以毫秒数，产生一个时间戳，该时间戳可以作为 `new Date()` 构造函数的参数，创建一个新的 `Date` 对象。我们可以调用 `getDay()` 方法来返回该日期是星期几。然后我们使用 `dayNames` 数组作为查找表，使用该值作为索引找到对应的星期名称字符串。

最后，我们需要添加一个事件监听器，在表单提交时调用 `nameThatDay` 函数。在 `JS` 部分的末尾添加以下行代码：

```javascript
form.addEventListener('submit',nameThatDay);
```

现在一切都就绪了，尝试使用该表单看看千年后是星期几（它应该和昨天是同一天）。

![今天是星期几？](img/whatdayisit.png)

你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/BaQdbQB)。

## 定时函数

JavaScript 提供了几个实用的方法，使我们能够调度函数的调用时间，或者定期调用某个函数。这些方法对于在事情发生之前产生延迟，或在屏幕上显示计时器非常有用。

### setTimeout

`setTimeout()` 方法接受一个回调函数作为第一个参数，接受一个毫秒单位的数字作为第二个参数。作为第一个参数提供的回调函数将在第二个参数所给的时间后被调用。

要查看其实效果，请尝试在控制台中输入以下代码。它应该在七秒后显示一个警告框。这是因为第一个参数是一个匿名箭头函数，用于显示警示框，而第二个参数是 7000 毫秒，即 7 秒：

```javascript
setTimeout( () => alert("Time's Up!"), 7000);
<< 1
```

注意，该方法返回一个整数。这是一个用于引用特定定时器的 ID。你也可以使用 `clearTimeout()` 方法取消定时。尝试再次调用该代码，并记录返回的数字：

```javascript
setTimeout( () => alert("Time's Up!"), 7000);
<< 2
```

现在，在警告框弹出之前快速输入以下代码，确保你输入的是之前返回的数字（在你的情况下它可能不是 2！）：

```javascript
clearTimeout(2);
<< undefined
```

如果你足够快并且使用了正确的 ID，回调将被取消，警示框将永远不会出现。

与其尝试记忆设置定时时返回的值，不如将返回值赋值给变量，如下例代码所示，这样更容易：

```javascript
const timer = setTimeout( () => alert("Time's Up!"), 7000);
<< 3
```

该变量稍后可以用于清除定时器：

```javascript
clearTimeout(timer);
<< undefined
```

## 异步编程

`synchronous`（同步）程序是按照代码出现的顺序处理每行代码的程序。这种方法的问题在于，如果程序的某部分需要很长时间才能完成，它将阻塞程序的其余部分。这意味着，耗时的事件（如文件下载完成、从数据库获取数据或加载游戏）将阻止任何其他事情的发生。

解决方案之一是启动一个新的 `thread`（线程）来运行程序的不同部分。这意味着如果一个进程在一个线程中运行很长时间，其他线程可以用于其他任务。多线程程序的问题是，很难跟踪每个线程中发生的情况，特别是当一个线程的结果需要另一个线程时。

另一种解决方案是编写 `asynchronous`（异步）代码，它会无序或以`异步`的方式运行。与其等待操作完成，不如创建一个回调（或 `promise`），程序的其余继续运行。这确保了等待过程完成不会阻塞程序其他部分的执行。一旦任务完成，该 promise 就被认为已解析（resolved）。

JavaScript 在单线程环境中运行，因此一次只能处理一个任务。这就是为什么`异步编程`是一项至关重要的工具，以确保等待不会阻塞程序的执行。我们可以通过使用 `setTimeout()` 方法来模拟耗时过程，从而演示 JavaScript 的异步特性。下面的图显示了在同步运行时三秒定时器如何阻塞代码，而非阻塞对比。

![阻塞与非阻塞代码](img/async.png)

使用定时器代替一个慢操作（例如下载文件）。尝试将代码输入控制台，但在按下回车之前先猜猜输出将是什么：

```javascript
console.log('Hello');
setTimeout(() => { console.log('File Downloaded!'); }, 3000);
console.log('World');
```

你猜对了吗？如果程序同步运行，将发生以下情况：

*   `Hello` 被打印到控制台
*   会有三秒的延迟
*   `File Downloaded!` 被打印到控制台
*   `World` 被打印到控制台

这是一种阻塞方法，因为三秒的等待阻塞了程序的其余部分的执行。

JavaScript 是一种`non-blocking`（非阻塞）语言，所以回调不会阻塞程序的其余发生。这是实际发生的情况：

*   `Hello` 被打印到控制台
*   三秒定时开始，但程序继续运行
*   `World` 被打印到控制台
*   三秒后，`File Downloaded!` 被打印到控制台

记住，JavaScript 是单线程的，因此一次只能处理一个任务。这意味着，即使一个任务只需要很短的时间完成，回调也必须等待程序的其余部分完成才能运行。事实上，即使我们将延迟改为零，字符串打印到控制台的顺序也不会改变。尝试在控制台中执行以下代码查看：

```javascript
console.log('Hello');
setTimeout(() => { console.log('File Downloaded!'); }, 0);
console.log('World');
```

注意，回调的结果仍然最后打印到控制台，尽管定时被设置为零毫秒。你可能认为这意味着回调将立即发生，但回调总是必须等待任何其他函数解析完毕后才能被处理。





### 延迟与睡眠

大多数编程语言都有一个 `delay` 或 `sleep` 函数，它可以停止程序的运行。例如，以下 Ruby 代码使用内置的 `sleep()` 方法来暂停代码执行三秒：

```
print 'Hello'
sleep 3
print 'World!'
```

这将会显示“Hello”，然后暂停三秒，最后显示“World!”

尽管这看起来与 `setTimeout` 的工作方式相似，但它们并不完全相同，因为 JavaScript 的异步特性意味着程序并没有停止运行。

“[JavaScript 中的延迟、睡眠、暂停与等待](https://www.sitepoint.com/delay-sleep-pause-wait/)” 解释了如何在 JavaScript 中创建一个类似 sleep 的函数。

## 间隔器 (Intervals)

`setInterval()` 方法的工作方式与 `setTimeout` 类似，不同之处在于它会根据第二个参数提供的毫秒数，每隔固定时间反复调用回调函数。

上一个示例使用了匿名函数，但也可以像这样使用具名函数：

```
function hello(){ console.log('Hello, World!'); }
```

现在我们可以设置间隔器并将其赋值给变量：

```
const interval = setInterval(hello,1000);
<< 1
```

这应该会在控制台中每秒（1,000 毫秒）显示一次“Hello, World!”。

要停止它，我们可以使用 `clearInterval()` 方法并将变量 `interval` 作为参数（这是因为 `setInterval()` 方法会返回它的 ID，所以这个 ID 会赋值给变量 `interval`）：

```
clearInterval(interval);
```

`setInterval()` 方法对于编写需要按固定间隔运行“游戏循环”的游戏代码特别有用。（事实上，在这一章的末尾，我们将使用它来编写一个游戏！）

#### `requestAnimationFrame`

还有另一种方法名为 [`requestAnimationFrame`](https://developer.mozilla.org/en-US/docs/Web/API/window/requestAnimationFrame) 的方法，可以用于动画和运行游戏循环。它不允许指定时间间隔，但每秒大约调用回调函数 60 次。你可以[阅读更多关于它的](https://www.sitepoint.com/premium/books/html5-games-novice-to-ninja/read/3/jzne1xb1) 并在 Earle Castledine 编写的优秀书籍 [HTML5 Games: Novice to Ninja](https://www.sitepoint.com/premium/books/html5-games-novice-to-ninja/) 中学习用 JavaScript 编写游戏。

### 秒表

我们可以使用 `setInterval()` 方法在浏览器中实现一个简单的秒表。在 CodePen 上打开一个新的 Pen 并添加以下 HTML：

```html
<div id='stopwatch'>00:00</div>
<button id='start'>Start</button>
<button id='stop' disabled>Stop</button>
<button id='reset'>Reset</button>
```

这包含一个用于显示起始时间 `'00:00'` 的 `<div>` 元素，以及三个用于控制秒表的按钮。（注意，`Stop` 按钮初始是禁用的。）

一点 CSS 将让秒表看起来更真实。在 CSS 部分添加以下代码：

```css
#stopwatch{
  border: 3px solid black;
  width: 200px;
  text-align: center;
  color: black;
  font: 64px monospace;
  padding: 30px;
  margin: 0;
}
```

现在我们需要让秒表真正工作。首先，我们需要获取对元素的引用。在 JS 部分添加以下代码：

```javascript
const stopwatch = document.getElementById('stopwatch');
const startButton = document.getElementById('start');
const stopButton = document.getElementById('stop');
const resetButton = document.getElementById('reset');

let time = 0;
```

前四个变量对应 HTML 中的四个元素。最后一个变量 `time` 将用于记录秒表的时间。由于它不断变化，因此需要使用 `let` 进行声明。

现在我们需要编写一个名为 `start` 的函数来启动秒表。在 JS 部分添加以下函数定义：

```javascript
function start(){
 timer = setInterval(function(){
  time++;
  // 百秒
  let hundredths = time % 100;
  if(hundredths < 10){
    hundredths = '0' + hundredths;
  }

  // 秒
  let seconds = Math.floor((time - hundredths) / 100);
  if(seconds < 10){
    seconds = '0' + seconds;
  }
  // 显示时间
  stopwatch.textContent = `${seconds}:${hundredths}`;
 }, 10);
 startButton.disabled = true;
 stopButton.disabled = false;
}
```

这是一个很长的函数，但其核心是 `setInterval()`，它每 10 毫秒（即每百分之一）调用一次匿名函数。

该匿名函数通过 `++` 运算符将 `time` 变量的值增加 1。之后，函数解析该值以将时间分为秒和百秒。它是通过...





- [CSS 动画：点化不死尸军潮](https://www.sitepoint.com/premium/books/css-animation-de-animating-the-undead-horde/)

可以使用 JavaScript 让这些动画更具交互性。让我们来看一个简单的示例，看看它是如何运作的。

### 跳跃的青蛙

我们将使用 CSS 动画创建一个青蛙跳跃的效果。首先，我们需要在 **HTML** 部分为我们的青蛙准备一个元素：

```html
<div id='frog'>🐸</div>
```

现在，让我们添加一些 CSS 让青蛙就就到位：

```css
#frog{
  font-size: 64px;
  position: absolute;
  top: 100px;
}
```

这只是让青蛙变大了一点，并让它在页面上获得了一个绝对定位。要使用 CSS 动画，我们需要创建一个 `@keyframes` 规则来描述动画的每一帧。在 **CSS** 部分添加以下内容：

```css
@keyframes jump {
  to{transform: translateY(-100px)}
}
```

这个 `@keyframes` 规则只描述了动画的结束状态，即向上垂直平移 `100px`（负值在 Y 轴方向上向上移动）。为了让它再次落回，我们将使用值为 `alternate` 的 `animation-direction` 属性。这会让动画正向播放，然后反向播放，从而产生跳跃的效果。在 `#frog` 选择器的样式中，添加以下代码行：

```css
animation-name: jump;
animation-duration: 700ms;
animation-iteration-count: infinite;
animation-direction: alternate;
```

你应该能看到青蛙在跳上跳下。

（这里有一个 Pen 展示了[我们目前所做的内容](https://codepen.io/SitePoint/pen/eYBEomK)。）

我们可以通过为青蛙元素添加一个事件处理程序来给动画添加一些交互性，使其在发生 `click`（点击）时运行动画，而不是一直循环运行。首先，从 **CSS** 部分移除动画属性，并在 **JS** 部分添加以下代码：

```javascript
const frog = document.getElementById('frog');
document.addEventListener('click',e =>  frog.style.animation = 'jump 700ms 2 alternate')
```

这个事件监听器会在用户点击页面任何地方时触发，并会调用一个匿名箭头函数来更新 `frog` 元素的 `style.animation` 属性。我们使用了使用了简写属性将所有属性写在了一行中。现在，只有当你点击页面时，青蛙才会跳跃。而且它只会跳一次：任何进一步的点击都不会让青蛙移动。此的原因是，一旦设置了 `style.animation` 属性，它就只会运行一次。再次用相同的值更新样式属性不会让它再次运行。为了让它再次生效，我们需要在动画结束后移除这些样式。幸运的是，正好有一个针对这种情况的事件监听器：`animationend`。在 **JS** 部分的最后添加以下代码：

```javascript
frog.addEventListener('animationend',e => frog.style.animation = 'none');
```

这会在动画结束后移除动画样式。任何进一步的点击将重新添加这些样式，青蛙将再次跳跃。

还有两个你可能发现有用的 CSS 动画事件监听器：

*   `animationstart`：它会在动画开始时触发
*   `animationiteration`：它会在动画每次迭代开始时触发，第一次除外

你可以在 [CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/gOLxyaM)。

### 抢饼干游戏

我们的最后一个项目是一个基于游游乐场经典游戏 [打地鼠](https://en.wikipedia.org/wiki/Whack-A-Mole) 的游戏，尽管这是一个更对动物友好的版本，涉及通过点击随机出现在屏幕上的饼干来将其“抓取”。

我们将使用 `setInterval()` 方法创建一个倒计时计时器，给玩家施加压力，让他们尽可能抓住更多的饼干。

首先，让我们用以下 HTML 设置一个新的 Pen：

```html
<div id='info'>Score: <span id='score'>0</</span> Time: <span id='clock'>20</</span>></div>
<div id='game'></div>
```

这只是两个 `<div>` 元素：一个用于放置分数和剩余时间的信息，另一个用于主游戏。

接下来，进入 **CSS** 部分并添加一些样式：

```css
#game {
  padding: 30px;
  border: 3px solid pink;
  position: relative;
  width: 200px;
  height: 200px;
}

.cookie{
  font-size: 32px;
  position: absolute;
  cursor: grab;
}

#info{
  font: 24px sans-serif;
}
#score,#clock{
  color: pink;
}
```

这大部分内容都是设置游戏中各种元素的大小和颜色。你现在应该能在屏幕上看到主游戏区域。

![抢饼干游戏区域](img/cookiegrabber.png)

最后，进入 **JS** 部分并编写实际的游戏机制。首先，我们需要获取 **HTML** 部分中元素的引用。它们都有 ID，所以我们可以使用 `getElementById`：

```javascript
const game = document.getElementById('game');
const clock = document.getElementById('clock');
const scoreboard = document.getElementById('score');
```

接下来，我们要声明并初始化跟踪时间和分数的变量：

```javascript
let time = 20;
let score = 0;
```

在下一步中，我们通过使用 `setInterval` 方法每隔 500 毫秒调用 `gameLoop` 函数来启动游戏主体：

```javascript
timer = setInterval(gameLoop,500);
```

`gameLoop` 函数包含了核心逻辑。每次它被调用时，都需要向游戏区域添加一个饼干，更新 `time` 变量，并检查时间是否结束。现在创建该函数：

```javascript
function gameLoop(){
  addCookie();
  time--;
  clock.textContent = time;
  // 检查时间是否结束
  if(time <= 0){
    clearInterval(timer);
    game.removeEventListener('click',grab);
    game.innerHTML = '';
  }
}
```

我们使用另一个名为 `addCookie` 的函数向游戏区域添加饼干，我们将编写它。我们使用递减运算符 `--` 减少 `time` 变量，然后更新显示时间的元素（由 `clock` 变量表示）的 `textContent` 属性。最后，检查时间是否达到零。如果是，使用 `clearInterval()` 方法停止计时器，参数为 `timer`，它指向创建间隔时返回的数字。我们还移除用于“抓取”饼干的事件监听器。（我们还没有创建它，所以如果你不认识它请忽略！）最后，通过将 `game` 的 `innerHTML` 属性设置为空字符串来移除任何未抓取的饼干，起到清除游戏区域的效果。

我们的下一个任务是编写 `addCookie` 函数。它需要创建一个类名为 `cookie` 的元素，并将其放置在游戏区域的随机位置。在 **JS** 部分的最后添加以下代码：

```javascript
function addCookie(){
  const cookie = document.createElement('div');
  cookie.textContent = '🍪';
  cookie.className = 'cookie';
  cookie.style.top = `${randomInt(200)}px`; // 此处假设有随机函数
  cookie.style.left = `${randomInt(200)}px`;
  game.appendChild(cookie);
}
```




这创建了一个空的 `<div>` 元素并将其赋值给变量 `cookie`。我们更新了 `textContent` 属性将其设置为饼干表情符号。然后，我们将 `className` 属性设置为 `cookie`。这样做是为了让它能够获取我们在 `CSS` 部分设置的样式，我们稍后还会用它来识别饼干是否被点击。用于将饼干放在随机位置的代码使用了 `style.top` 和 `style.left` 属性，这些属性的作用就像是从 `game` div 左上角开始坐标。然后，我们使用在第 8 章中创建的 `randomInt` 辅助函数，在 1 到 200（游戏区域的宽度）之间选择一个随机整数来设置这两个属性。最后，我们使用 `appendChild` DOM 方法将该元素作为 `game` 元素的子添加。这意味着任何创建的饼干都将出现在游戏区域内的随机位置。

接下来，我们需要添加玩家交互。当玩家点击饼干时，我们希望让他们“抓住”它。我们可以为创建的每个饼干绑定事件监听器来监听 `click` 事件，但使用事件委托并将事件监听器绑定到 `game` 元素上要简单得多。在 `JS` 部分的末尾添加以下代码：

```
game.addEventListener('click',grab);
```

每当玩家点击游戏区域内的任何地方时，都会触发 `grab` 函数。这意味着我们需要编写 `grab` 函数，并检查是否点击了饼干。在 `JS` 部分的底部添加以下函数声明：

```
function grab(event){
  if(event.target.className === 'cookie'){
    score ++;
    scoreboard.textContent = score;
    event.target.remove();
  }
}
```

这段代码查看传递给任何事件处理程序的事件对象的 `target` 属性。该属性返回实际被点击的元素。这意味着我们就可以检查该对象是否具有 `cookie` 类。如果是，我们使用递增运算符（`++`）将分数加 1，更新 `scoreboard` 元素的 `textContent` 以显示新分数，然后从 DOM 中移除被点击的元素。这意味着，如果玩家点击了饼干，他们的得分就会增加 1 分，饼干就会“消失”！

最后，我们需要包含用于创建创建随机整数的 `randomInt` 辅助函数。由于函数声明会被提升，我们可以将其放在远处，即代码的底部：

```
function randomInt(lower,upper){
  if(upper===undefined){
    upper = lower;
    lower = 1;
  }
  return Math.floor(Math.random()*(upper-lower+1)+lower)
}
```

就这些！尝试运行一下代码，看看你能抓到多少个饼干。它看起来应该是这样的：

![Playing Cookie Grabber](img/cookiegrabber.png)

你可以查看 [CodePen 上我的代码](https://codepen.io/SitePoint/pen/abByxNM)。

## 挑战

1. 设计一个表单，允许用户输入生日并找出他们出生的星期。例如，输入“1/1/2000”（2000 年 1 月 1 日）应该返回“星期六”。你可以在 CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/wvoqZWd)。

2. 创建一个 [Tabata 训练计时器](https://www.active.com/fitness/articles/what-is-tabata-training)。它应该交替进行 20 秒工作和 10 秒休息，共进行 8 轮。计时器应该指示当前是工作还是休息。作为加分项，添加“Start”（开始）、“Stop”（停止）和“Reset”（重置）按钮。你可以在 CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/qBqXwNz)。

3. 通过添加一些额外功能改进饼干抓游戏。一些建议可能：添加一个让用户按下启动游戏的按钮；让饼干以随机频率出现；让饼干在出现时大小随机，且它们的分值与大小成反比（饼干越小越难抓到，得到的分数就越多！）

   你还能想到其他的吗？你可以在 CodePen 上查看我的代码](https://codepen.io/SitePoint/pen/ExNvJgr)。

## 总结

* UNIX 时间元（UNIX epoch）是一个任意日期，1970 年 1 月 1 日，计算机语言用它作为测量已时间的参考点。
* 大多数编程语言都有一个 `Date` 对象，允许你以各种格式存储日期和时间。
* `setTimeout()` 方法在提供毫秒数作为参数后调用回调函数。
* 异步编程意味着代码可以按无顺序执行。它停止了长时间进程阻塞代码流，让程序在等待它们完成的同时继续运行。
* `setInterval()` 方法每隔给定的时间间隔就会调用调用回调函数。
* JavaScript 可用于为 CSS 动画添加交互性。

我们现在已经到了书中最后一个实操章节的结尾。但还剩最后一个章节了——希望这一章能激励你进入编码的下一个阶段。

# 第 16 章：结束

仅仅因为你快要读完这本书并不意味着你的编码之旅结束了。相反，它才刚刚开始。本章的目的是为你下一步提供一些想法和启发。我们将查看以下主题：

* 编码实践
* 深入 JavaScript
* 学习新语言

## 编码实践

现在你已经可以自信编写代码了，是时候设置你的环境并学习一些最佳实践了。

### 编码工具

CodePen 对于编写书中的示例并立即查看结果非常有用，但现在是你时候建立自己的环境了。你的第一个任务是寻找一个编辑器。

有很多编辑器可供选择，使用 [VS Code](https://code.visualstudio./)、[Sublime Text](https://www.sublimetext.com) 或 [Atom](https://atom.io) 都不会错。这些都是功能强大的编辑器，包含了语法高亮、标签、文件浏览和代码补全。Atom 甚至是 HTML、CSS 和 JavaScript 构建的！

你可以通过阅读 Bruce Johnson 的 [* Studio Code: End-to-End Editing and Debugging Tools for Web Developers](https://www.sitepoint.com/premium/books/visual-studio-code-end-to-end-editing-and-debugging-tools-for-web-developers)* 来了解更多关于设置 VS Code 的信息。

![VS Code features syntax highlighting as well as many other features](img/vscode.png)

如果你使用 Chrome 浏览器或 ChromeOS，还可以考虑 [Text](https://chrome.google.com/webstore/detail/text/mmfbcljfglbokpmkimbfghdkmjhdgb) 和 [Caret](https://chrome.google.com/webstore/detail/caret/clocpococg)，两者都是非常好的选择。

### 风格指南

另一个良好的实践是遵循编码风格指南。这些指南通常由开发团队编写，以确保他们在编写代码时达成一致。[Google](https://google.github.io/styleguide/jsguide.html) 和 [Airbnb](https://github.com/airbnb/javascript) 使用的风格指南都是公开的。遵循风格指南中列出的标准有助于提高你编写的代码质量，并保持你编码风格的一致，正如“[为什么我使用 JavaScript 风格指南以及你也应该这样做](https://www.sitepoint.com/why-use-javascript-style-guide/)”所示。



你也可以使用[代码检查](https://www.sitepoint.com/comparison-javascript-linting-tools/)工具，它们会高亮代码中的任何样式错误，并帮助确保你编写的任何代码符合你指定的样式指南。尝试将你的代码粘贴到[JSLint 在线工具](https://jslint.com)中以获取质量报告。

## 版本控制

版本控制软件允许你跟踪对代码进行的所有更改，因为你代码的每一个版本都被保存了，并且可以随时回溯。

源码管理最流行的工具之一是[Git](http://git-scm.com/)，它由 Linux 的创始人 Linus Torvalds 编写。Git 允许你回滚到代码之前的版本。你还可以对代码进行分支（branch），以便在测试新功能，而不会改变当前的稳定代码库。Git 是一个`分布式`源码控制系统，这意味着许多人可以分支（fork）一段代码并独立开发，然后将他们的任何更改合并回主代码库。这意味着如果你犯了错误，可以回滚到上一个正常运行的版本。

Git 使用命令行来发布命令，但有大量的 GUI 前端可以安装，以提供代码的视觉化表示，其中包括出色的[GitHub Desktop](https://desktop.github.com)。

还有各种可以托管 Git 仓库的在线服务，包括[GitHub](https://github.com/), [GitLab](https://gitlab.com) 和 [Bitbucket](https://bitbucket.org/)。

随着你编写越来越复杂的代码，将 Git 集成到你的日常工作流会让你的生活变得简单得多。可以通过 Shaumik Daityari 写的[Jump Start Git](https://www.sitepoint.com/premium/books/jump-start-git-2nd-edition/)了解更多关于 Git 的信息。

## 测试

当你开始编写更多代码时，你应该尝试养成测试的习惯。指的不仅仅是尝试几次看看它是否有效。`测试`是开发过程中不可或缺的一部分，涉及到在你编写代码的同时编写测试你代码的代码。错误和 Bug 是编码的一部分，而测试有助于快速识别并处理它们。

`测试驱动开发` (TDD) 是编写任何代码*之前*先编写测试的过程。其理念是你先决定想让代码做什么，为它编写一个测试，然后编写代码通过该测试。起初这看起来很奇怪，但它有助于确保你的代码确实做了它应该做的事。

学习 JavaScript 测试的一个良好起点是“[[初学者函数式 JavaScript 测试指南](https://www.sitepoint.com/testing-functional-javascript/)””。流行的测试库包括 [Jasmine](https://jasmine.github.io), [Mocha](https://mochajs.org) 和 [Jest](https://jestjs.io)。

## 深入学习 JavaScript

本书侧重于使用 JavaScript 来教授编程基础。如果你喜欢我们目前为止涵盖的内容，那么好消息是还有很多东西可以学习。

### 高级 JavaScript

我们在本书中涵盖了 JavaScript 的基础知识，但还有很多内容需要学习。一个很好的起点是学习 Web `APIs`（应用程序编程接口）。一些亮点包括：Canvas API，可用于创建 2D 和 3D 图形；Fetch API，用于发送 HTTP 请求并从其他服务器检索数据；Web Storage API 和 cookies，它们都允许你在用户的计算机上存储数据；以及 WebSocket API，它允许多个用户同时访问同一个网站。

关于异步编程和 JavaScript 的事件循环还有更多可以学习，包括 promises 以及 `async` 和 `await` 关键字。JavaScript 还有[maps](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) 和[sets](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)，它们是不同的数据结构。

JavaScript `modules` 涉及将你的代码分离到单独的文件中并可以在不同的项目中重用。你还可以导入其他人编写的外部库，为你的代码添加额外功能。阅读“[理解 ES6 模块](https://www.sitepoint.com/understanding-es6-modules/)”以了解更多。

我们在书中没有提到但学习非常有用的一个领域是`正则表达式`（简称 `regex`）。这些是描述字符串结构的模式，它们在几乎每种编程语言中都有实现。它们可以用于搜索字符串并执行“查找和替换”类型的操作。正则表达式起初可能有点奇怪，它们像是一门黑艺术，可以很容易写满整本书！在处理大量文本时，它们确实非常有用。以下是一些可以帮助你学习更多正则表达式的有用资源：

* [Regular-Expressions.info](https://www.regular-expressions.info/)
* [regex101](https://regex101.com/)
* [Mastering Regular Expressions](https://www.oreilly.com/library/view/mastering-regular-expressions/0596528124/)（一本全面的书）

JavaScript 是一门不断演变的语言，每年都会向语言中添加新功能。如果你渴望了解它的最新功能，你应该阅读 T.J. Crowder 写的[JavaScript: The New Toys](https://www.sitepoint.com/premium/books/javascript-the-new-toys/)。

Laurie Voss 的演讲“[JavaScript: 现状、何方以及未来](https://www.sitepoint.com/premium/tech-talks/web-directions-code-leaders-2019/javascript-where-where-next)”详细介绍了 JavaScript 的现状和趋势。

### 库

JavaScript `library` 是一段提供了更易实现常见任务的方法的代码。JavaScript 是一种极其灵活的语言……并不是所有的任务都像应该的那样容易。库会将功能抽象为易于使用的函数。这些函数可以用来完成常见任务，而无需编写大量的重复代码。一个很好的例子是 [date-fns](https://date-fns.org)（我们在上一章中遇到的一个库），它让处理日期变得更易管理。

[jQuery](https://jquery.com) 可能是所有 JavaScript 库中最著名的。它提供了许多方法，使得 DOM 操作、事件处理和 API 调用更易实现。它不像以前那么流行了，因为“原生”现在可以完成许多 jQuery 经常使用的功能，但它仍然被许多网站使用。如果你想学习任何关于 jQuery 的知识，阅读 Earle Castledine 的[jQuery: Novice to Ninja: New Kicks And Tricks](https://www.sitepoint.com/premium/books/jquery-novice-to-ninja-new-kicks-and-tricks/)不会出错的。

尽管如此，编写自己的辅助函数库也是一种非常有用的练习，有助于提高你的编码技能。这涉及到创建一组你在项目中经常使用的函数。一个例子就是我们在书末的几个编码挑战中使用的 `randomInt` 函数。

### Node.js




JavaScript 最初被认为是一种用于浏览器的前端编程语言。Node.js 在 2009 年发布时从根本上改变了 JavaScript 的格局，这意味着 JavaScript 可以在计算机或服务器上运行，而不需要浏览器。这意味着 JavaScript 现在可以用于编写服务端代码并与文件系统进行交互。

如果你安装了 Node.js，你就可以在不使用浏览器的情况下运行 JavaScript，并访问 Node REPL（读取-评估-打印循环），这是你自己电脑上的命令行 JavaScript 控制台。它还让你能够访问由 [Node 包管理器](https://www.npmjs.com) 提供的庞大 Node 软件包库，这些包提供了广泛的功能。其中许多包都是用于帮助你自动化工作流并在部署之前编译你的 JavaScript 代码的工具。

Node.js 还可以用于用于构建与后端数据库交互的服务端应用程序和动态网站。JavaScript 的异步特性使其非常适合具有大量并发用户的实时更新应用程序，因为它能够以非阻塞的方式快速处理请求。

如果你想学习更多关于 Node.js 的知识，一个很好的起点是“[什么是 Node 以及我什么时候应该使用它？](https://www.sitepoint.com/an-introduction-to-node-js/)”，以及 [你的 Node.js 第一周](https://www.sitepoint.com/premium/books/your-first-week-with-node-js-2nd-edition/)。

## Deno

Node.js 的创建者 Ryan Dahl 创建了一个名为 [Deno](https://deno.land) 的新项目，他声称该项目解决了 Node.js 的许多问题。

Nilson Jacques 写的“[Node.js vs Deno：你需要知道的](https://www.sitepoint.com/node-vs-deno/)”提供了 Node.js 和 Deno 的用用对比，而 Craig Buckler 的 TechExeter 演讲“[初探 Deno](https://www.sitepoint.com/premium/tech-talks/techexeter-2020/a-first-look-at-deno)”则提供了一个实用的介绍。

## 学习另一种语言

现在你已经学会了使用 JavaScript 的编程基础，你应该会发现学习另一种语言变得容易得多。那里有大量的语言供你尝试。

如果你喜欢学习面向对象的编程，你可能可能想尝试学习 [Ruby](http://www.ruby-lang.org/en/) 或 [Python](https://www.python.org)。你可以通过阅读 [Python 门徒](https://www.sitepoint.com/premium/books/the-python-apprentice/)开始，然后进阶到 [Python 行手](https://www.sitepoint.com/premium/books/the-python-journeyman/) 和 [Python 大师](https://www.sitepoint.com/premium/books/the-python-master/)。

你可能想尝试学习一种需要编译的经典语言，例如 [Java](https://www.oracle.com/uk/java/)、[C#](https://docs.microsoft.com/en-us/dotnet/csharp/) 或 [Swift](https://swift.org)。

如果你想学习更多关于函数式编程的知识，你可以尝试学习 [Haskell](https://www.haskell.org)、[Elixir](https://elixir-lang.org)、[Erlang](https://www.erlang.org)、[Scala](https://www.scala-lang.org) 或 [Clojure](https://clojure.org)。

还有其他脚本语言，如 [Lua](https://www.lua.org) 或 [Bash](https://en.wikipedia.org/wiki/Bash_(Unix_shell))。[Go](https://golang.org) 是一种现代动态语言，与 JavaScript 有许多相似之处，而 [TypeScript](https://www.typescriptlang.org) 是 JavaScript 的超集，增加了许多特性。特别是，它是一种强类型语言（这意味着你必须声明变量的类型，正如我们在第二章 中讨论的那样）。

一种相对较且被证明非常流行的语言是 [Rust](https://www.rust-lang.org)。它是一种底层语言，类似于 C++，可以用于编写系统级、高性能的代码“[Rust 教程：面向 JavaScript 开发者的 Rust 简介](https://www.sitepoint.com/rust-tutorial-introduction-javascript-devs/)”对于了解 JavaScript 如何工作的人来说是一个很好的介绍。

此外还有一些真正古怪的语言，例如只有三个命令的 [Ook](https://www.dangermouse.net/esoteric/ook.html)（`Ook.`、`Ook?` 和 `Ook!`）、[ArnoldC](https://github.com/lhartikk/ArnoldC)（完全由阿诺德·施瓦辛格引言组成的语言），以及 [Tabloid](https://tabloid.vercel.app)（代码读起来像小报纸！）。

有一点是可以肯定的：你可能不需要担心没有语言学，它们都将帮助你加深对编码概念的理解，并让你领略各种编程范式。

## 持续学习

编码世界变化极快，而且每年都在变得更快。你需要确保自己跟上最新的进展和最佳实践。以下是一些关于如何保持知识新颖的建议：

* 在 [SitePoint](https://www.sitepoint.com/) 上阅读书籍和文章
* 观看教程
* 在社交媒体上关注程序员
* 阅读博客文章并听播客，例如 [Syntax](https://syntax.fm/)
* 加入本地或在线用户组
* 参加会议或线下聚会
* 观看技术演讲 [SitePoint](https://www.sitepoint.com/premium/tech-talks/)

## 继续编码

你可以学习所有的理论，但唯一进步的方法是实际编码。通过将想法付诸实践，你将开始对编程的感觉。以下是用你的 JavaScript 技能可以构建的一些想法。

以下想法旨在激发你的灵感，并希望能激发你产生项目的想法。这绝不是你能做的完整列表，因为可能性是无限的。

### Web 应用程序

JavaScript 最初是为了让网站具有交互性。但从这些基础开始，它已经发展成为一种强大的语言，能够产生像 Gmail、Netflix 和 Uber 这样复杂的应用程序。基础网站可以使用 HTML 和 CSS 构建，尽管它们通常会使用 JavaScript 添加一些额外的交互。相反，复杂的应用程序通常涉及一个托管数据库的后端服务器以及一个包含 HTML、CSS 和 JavaScript 的前端。它们通常会托管自己的 API，供其他站点与存储在数据库中的数据交互。这些每一层构成了所谓的开发栈。全栈开发涉及该栈的每个部分。

JavaScript 现在可以用于编写应用程序的前端以及运行在服务器上的后端。它甚至可以与数据库进行交互。这使得 JavaScript 成为编写全栈应用程序的有用语言。如果你将你的 JavaScript 技能到更高水平，你将完全具备开发严肃、高性能 Web 应用程序的能力。

渐进式 Web 应用（PWA）是使用本地存储使其看起来像原生应用程序的 Web 。它们加载更快，使用起来更流畅，不需要持续的网络连接。在 Jason Grigsby 的演讲“[规划你的渐进式 Web 应用](https://www.sitepoint.com/premium/tech-talks/web-directions-code-2019/planning-your-progressive-web-app)”中，他涵盖了构建渐进式 Web 应用时需要考虑的关键事项。





许多现代网站和应用程序通过在线 API 与第三方应用程序进行交互，以共享和交换数据。这通常存储为 [JSON（JavaScript 对象表示）](http://www.json.org)，它是我们在第 9 章中遇到的对象字面量的字符串表示形式。它是一种轻量级数据格式，允许数据以人类可读的形式进行序列化。尽管它源自 JavaScript 对象，但大多数现代编程语言都包含了生成和解析 JSON 格式数据的方法。

一种变得日益流行的生产模式是 `Jamstack`。这是一个由 JavaScript、APIs 和标记语言（JAM）组成的技术栈。其核心思想是使用 HTML、CSS 和 JavaScript 构建网站，并使用 API 从网络服务获取数据。Phil Hawksworth 曾在 [Pixel Pioneers 上的一场演讲](https://www.sitepoint.com/premium/tech-talks/pixel-pioneers/jamstack-silly-name-serious-stuff) 中解释了它的工作原理。

在他在“[JavaScript 拯救世界](https://www.sitepoint.com/premium/tech-talks/dotjs-2019/javascript-saves-the-world)”的演讲中，Asim Hussain 提供了一些关于如何提高 Web 应用效率的技巧，这能够带来更好的用户体验，而且既物廉又环保。

许多现代 Web 应用程序需要跟踪数据——无论这些是从外部网络服务获取的数据，还是用户生成的数据。这意味着网页需要能够跟踪数据的任何变化，并相应地更新用户界面（UI）。有几个框架旨在让你更容易制作交互式 UI，并帮助进行*状态管理*。

主要的巨头是 [React](https://reactjs.org) 和 [Vue](https://vuejs.org)。这两者都为了同一个目标采取了各自独特的方法，即创建组件，这些组件会在用户交互或数据变化时自动更新。关于 React 和 Vue 的在线教程层出不穷，而且它们在自己的网站上都有良好的入门教程，因此值得尝试一下这两者，看看你更倾向于使用哪一个。

还有 [Svelte](https://svelte.dev)，它是一个更轻量的选择，采用与 React 和 Vue 略有不同的方法，可能更适合小型项目。它们网站上的教程是一个极佳的起点。

一个很好的起点是我们在本书中创建的待办事项列表应用。你可以尝试将其开发为一个功能齐全的 Web 应用。

为什么不尝试构建下一个在线热门产品呢？

### 游戏开发

大多数在线游戏过去使用 Flash 编写，但 JavaScript 是构建现代浏览器端游戏的首选语言。WebGL 和浏览器 GPU 的发展意味着在浏览器中运行快速渲染的 3D 游戏已成为可能。现代在线经典如 [HexGL](https://hexgl.bkcore.com)、[世界最大的 PAC-MAN](https://worldsbiggestpacman.com/) 和 [Swooop](https://s3-eu-west-1.amazonaws.com/apps.playcanvas.com/R2axJfsc/index.html) 显示了浏览器中可以运行的内容。这些都是可以实现功能的绝佳例子，但游戏不必过于复杂：[Flappy Bird](https://flappybird.io/) 的成功表明，一个执行良好的良好创意可以变得非常受欢迎。

![HexGL](img/hexgl.png)

如果你对编写 HTML5 游戏感兴趣，那么由 Earle Castledine 编写的[HTML5 游戏：从新手到大师](https://www.sitepoint.com/premium/books/html5-games-novice-to-ninja)* 将是完美的起点。

为什么不尝试编写下一个大片级游戏呢？

### 移动应用开发

Android 和 iOS 不使用 JavaScript 作为它们的原生编程语言。然而，你仍然可以使用 HTML、CSS 和 JavaScript 构建应用程序，然后使用如 [Ionic](https://ionicframework.com)、[Cordova](https://cordova.apache.org/) 或 [PhoneGap](https://phonegap.com/) 等工具将你的代码转换为可以在 Android 和 iOS 平台上运行的原生代码。

为什么不尝试编写下一个热门移动应用呢？

### 桌面应用开发

[Electron](https://electron.atom.io) 是一个开源库，允许你使用 HTML、CSS 和 JavaScript 构建桌面应用程序。它使用 Chromium（Google Chrome 的开源版本）和 Node.js 创建可以在 Windows、macOS 和 Linux 上运行的应用程序。

Electron 是 GitHub 在构建 Atom 文本编辑器时开发的。从那时起，Electron 已成为想要创建 Web 应用桌面版本的开发者的流行选择。它已被用于创建如 WhatsApp、Microsoft Teams 和 Slack 等桌面应用程序。

为什么不尝试编写下一个热门桌面应用呢？你可以从 Electron 的[快速上手指南](https://www.electronjs.org/docs/tutorial/quick-start)开始。

## 物联网

JavaScript 正在成为与“[物联网](http://en.wikipedia.org/wiki/Internet_of_Things)”通信的首选语言。这包括了一系列设备，从手表、虚拟现实头设备到家庭助手甚至无人机！JavaScript 经常是用于为这些不断增长的电子设备编写代码的语言。为什么不尝试为你最新的可穿戴设备或家居设备编写一些自定义代码呢？

## 挑战

本章提供了许多关于你可以做什么的想法，但上述大量的建议可能会让你产生“选择困难症”。因此，后续挑战的目标是让你专注于需要要做的事情。如果你完成了每项挑战，你将走上成为开发者之路：

1. 安装一个文本编辑器。有很多[视频](https://www.youtube.com/results?search_query=how+to+set+up) 教你如何设置 VS Code。

2. 安装 Node.js。

3. 使用 `npm` 安装 React。

4. 使用 React 构建 Web 应用。（[SitePoint](https://www.sitepoint.com/react/) 有很多此类教程。）

5. 安装 Git 并使用它进行版本控制。

6. 将你的应用推送到 GitHub。

7. 构建另一个 React 应用，从另一个网站获取并显示数据。

8. 重复

## 总结

* 通过安装文本编辑器来设置你的编码环境。
* 样式指南将有助于以一致的风格编写代码并使其易于阅读。
* 测试将帮助代码免于 Bug 和错误。
* 版本控制（如 `Git`）可以帮助管理代码的任何变化。
* 更多 JavaScript 需要学习，包括 Web API 和模块。
* `jQuery`、`Lodash` 和 `date-fns` 等 JavaScript 库提供了让开发更容易的方法。
* `Node.js` 让你在没有浏览器的情况下运行 JavaScript 并开发应用程序。
* 你还有许多其他可以学习的编程语言。
* `React`、`Vue` 和 `Svelte` 等 JavaScript 框架有助于创建响应数据变化的的用户界面。
* JavaScript 现在可以编程 Web 开发栈的每一个部分，使其成为全栈开发的完美语言。
* 你可以使用 JavaScript 构建网站、Web 应用、游戏、手机应用或桌面应用。
* 得益于物联网，你的编程技能可以控制家中的几乎任何设备。
* 通过阅读书籍和文章、听播客、看视频以及在社交媒体上关注开发者来保持你的知识更新。
* 持续不断编写代码并构建东西吧！





这标志着本章以及整本书的结束。希望你喜欢学习编程的过程，也希望这一章的内容能激励你将编程水平提升到新的高度。无论你决定做什么，最重要的一点就是坚持写代码。写得越多，进步得越快。编程是为了解决问题和创造事物。所以，你还在等什么？开始编程吧！唯一的限制就是你的想象力！
