content]

# 现代 JavaScript 实用入门指南

## 引言

如果你阅读了 `zsoltnagy.eu` 上的大部分博客文章，你可能会发现，大多数文章至少需要一些关于 `JavaScript` 的基础知识。主要的例外是 [JavaScript 基础](http://www.zsoltnagy.eu/category/javascript-basics/) 分类。

我写这本书是为了弥合我那些经验较少的受众与理解我关于 `JavaScript` 更高级内容所需知识之间的鸿沟。这本书绝对不需要任何 `JavaScript` 知识。

为了在学习 `JavaScript` 时获得一些优势，重要的是明白为什么值得在2019年及以后学习这门语言：

- 为什么今天是开始学习 `JavaScript` 的最佳时机
- 你的职业前景如何
- 以及为什么 `JavaScript` 在 2019 年为你提供了近乎最佳的学习体验。

## 本书的使命

我有一个使命，那就是为初学者创建学习 `JavaScript` 编程的最佳 `JavaScript` 资源。这个使命的灵感来源于我的视频课程《ES6 实战》，该课程最初面向广泛的受众：初学者、中级和专家。虽然中级和专家开发者非常喜欢这个资源，但初学者却感到困难，因为课程节奏对他们来说太快，而且练习要求太高。

本书的使命是让 `JavaScript` 变得易于理解。我无意取代文档，仅仅因为文档的目的是追求完整。在本书配套的课程中，我的目标是转变你的编程技能。

这个使命需要很长时间才能完成，你也可以成为其中的一部分。如果你有任何反馈，请随时给我发送电子邮件至 [info@zsoltnagy.eu](mailto:info@zsoltnagy.eu)。

让我们继续介绍 `JavaScript` 的历史。

## 客户端 JavaScript

你很可能是通过像 `Google Chrome` 或 `Firefox` 这样的网络浏览器访问了本书。在浏览器中显示的网站主要使用三种语言编写：`HTML`、`CSS` 和 `JavaScript`。

`HTML`（超文本标记语言）描述网站的结构和内容。`CSS`（层叠样式表）处理展示：它决定了使用哪种字体、颜色、背景图片等来显示网站。

`JavaScript` 是一门成熟的编程语言，它不仅可以为屏幕上的元素添加动画和修改元素，还可以执行许多其他任务，例如：

- 与服务器通信，提供和存储数据
- 描述应用逻辑：例如，应用逻辑可以验证你输入的个人数据
- 可视化：例如，`JavaScript` 可以绘制一个显示谷歌股票价格的图表。

动画在计算机科学中是指在屏幕上移动或变换对象的行为。在移动过程中，对象的特征可能会发生变化，这意味着动画对象可能以不同的颜色、不同的尺寸绘制，或者在三维动画的情况下，我们可能从不同的角度看到该对象。

变换对象意味着对象的某个特征随时间变化。我们可以改变对象的许多特征，例如它的颜色、形状或方向。

在客户端开发方面，`JavaScript` 显然是首选语言。让我们暂停一下。什么是客户端，什么是服务端？

客户端开发侧重于编写在最终用户浏览器中运行的代码。服务端开发侧重于编写在服务提供商服务器上运行的代码。

当一个客户端从服务器获取谷歌的股票价格时，一个服务端程序会从数据库查询关于谷歌股票的数据。然后，这些数据通过指定的格式传输给客户端。客户端随后可以读取数据并显示历史股票价格的图表。

回到90年代和21世纪初，`JavaScript` 只是一个玩具语言，只能在静态网站上动画化元素。这些动画被称为动态行为。

在给定时间点在屏幕上显示一个对象被称为渲染。

动画也可以通过在屏幕上持续渲染一个对象来定义，同时它的特征可能会改变。

二十年前，`JavaScript` 在软件开发行业并未受到重视。许多“开发者”不知道自己在做什么，他们只是复制粘贴代码片段，为网站添加一些动态行为。通常，这些代码片段会相互冲突，因为它们使用了相同的变量。

一旦 `AJAX` 编程（异步 `JavaScript` 和 `XML`）开始流行，`JavaScript` 变得更受欢迎。2006年，`XMLHttpRequest` 对象成为标准，这意味着你可以向服务器提交请求并等待其响应。一旦响应到达，你就可以在不加载页面的情况下显示结果。这在网站上就像魔法一样，因为在这种技术普及之前，与服务器的每次交互都需要完全重新加载页面。由于页面重新加载可能需要几秒钟，消除重新加载页面的需求是一个巨大的成就。

`JavaScript` 社区在成长，但我们面临另一个问题：为了编写在所有主要浏览器中都能运行的代码，我们必须为不同的浏览器编写不同的代码。有时情况令人困惑。因此，你必须成为领域专家才能编写 `JavaScript` 代码。

不过，这种状况没持续多久。2006年，另一个重要的里程碑出现了。`jQuery` 库发布，口号是写得更少，做得更多。与其编写几十行代码来确保覆盖所有浏览器，`jQuery` 为你提供了单行命令来达到相同的效果。你不再需要成为专业的软件开发者才能编写 `JavaScript` 代码。你只需要包含 `jQuery`，问题就解决了。

不幸的是，`jQuery` 创造了另一个问题。我们可以用“蜘蛛侠”的邪恶克隆“猩红蜘蛛”的口号来形容：拥有全部力量，却无需承担责任。降低门槛意味着那些不关心软件工程的人也开始编写代码。

与此同时，单页应用程序和客户端富网络应用的想法成为主流。在 `AJAX` 和 `jQuery` 之前，几乎都发生在服务端。服务器的任务是组装一个网页并将其发送给客户端。服务器创建 `HTML`、`CSS` 和 `JavaScript` 代码，客户端只加载那一个页面。当渲染和部分应用逻辑转移到客户端时，情况发生了变化。这意味着应用程序只需加载一次，数兆字节的 `JavaScript` 代码负责渲染客户端感兴趣的应用程序部分。这一步得以实现得益于摩尔定律，因为最终用户计算机的性能每隔几年就会翻倍。

> 单页应用程序在页面加载时接收所有 `HTML`、`CSS` 和 `JavaScript`，客户端可以在不通知服务器的情况下在应用程序之间导航。通过 `AJAX` 调用服务器通信，并在不需要加载页面的情况下接收数据。这种方式变得更快，像桌面应用程序一样。从上述特征来看，可扩展性意味着应用程序给出的响应可以轻松计算。可扩展性可以在资源和开发流程上定义。例如，如果一个服务器保证每100个并发用户的响应时间为1秒，我们需要知道在10000个并发用户下的响应时间以及万行代码中的错误。

## JavaScript 的演变与框架

主要问题在于那些自称软件开发的人，利用他们的黑客技能创建了质量软件。人们很快意识到，仅有 `jQuery` 知识限制了他们开发的规模。维护性是指让软件易于开发、修改、扩展和调试。如果你写万行代码，需要不同的方法。维护性问题的答案是框架出现。框架使得以结构化的方式编写代码，而无需重新发明轮子。

框架虽然出色，但开发者还有一个问题。框架和库的功能已经超出了 `JavaScript` 能力范围。这门语言已经相当老旧，我们需要更新。这次更新就是 `ES2015`，或者它的旧名 `ES6`。许多创新从不同的来源进入 `ES6`，例如 `jQuery`、一些框架、一些函数式编程库（如 `UnderscoreJs`）以及一些语言（如 `TypeScript`）。

`ES` 代表 `ECMAScript`。`ECMA International`（ECMA = 欧洲计算机制造商协会）是一个成立于1961年的标准化组织。`ECMA International`负责描述像 `JavaScript` 和 `ActionScript` 类语言的标准。最新`JavaScript`语言的标准是 `ECMA-262`。

在 `ES6` 出现之前，像 `Internet Explorer 8` 这样的老浏览器变得如此受欢迎，以至于没有提供与它们兼容的需求。这导致了更紧凑、更统一的 `JavaScript` 代码。

自2015年以来，`JavaScript`的发展就没有回头路。每年都会有一些更新进入 `JavaScript`，这些更新也最终进入了我的课程 [ES6 in Practice](http://www.zsoltnagy.eu/es6-in-practice)。

我们可以根据 `JavaScript`的历史得出结论：现在是成为 `JavaScript` 开发者的最佳时机。在许多公司，你可以比 `C++` 开发者或 `PHP` 开发者赚得更多。只需看看 `stackoverflow.com` 的工作机会或 `payscale.com` 的数据。你每天处理的挑战很有趣，更重要的是，得益于实时加载功能，你通常可以立即在浏览器中看到修改的效果，从而获得对自己工作的反馈。

- JavaScript 最初是一种用于创建动态行为的玩具语言
- `AJAX` 使得无需重新加载应用程序页面即可更新网站成为可能
- `jQuery` 降低了 Web 编程的入门门槛
- 框架和库迫使我们使用软件工程中众所周知的设计模式
- IE8 等老式浏览器失去了流行度
- ES2015及以后：许多模式成为语言的标准组成部分

## JavaScript 在服务端

如果这些好处对你来说还不够，让我们再给这个组合加点料。

`JavaScript` 不再只是一种客户端语言。`Node.js` 使得在服务器上运行 `JavaScript` 成为可能。`Node.js`建立在 `Google Chrome` 的执行引擎 `V8` 的基础之上。回想一下，即使是迈克尔·舒马赫也是用 `V8` 引擎赢得了第一个世界冠军。`V8` 引擎像一级方程式赛车一样快。`V8`编译器将 `JavaScript` 转换为机器码，这意味着在服务器上，我们不再处理解释型代码。

> 解释型代码运行在虚拟机上，将开发者编写的一组指令翻译成可执行命令。解释型语言通常比编译型语言慢。解释型语言也是移植的，这意味着你可以获取源代码，并在任何虚拟机上执行它。机器码的好处是运行代码尽可能接近机器码，转化为更快的执行。

为什么 `Node.js` 对于某些服务端任务仍然很好的选择？原因在于 `Node.js`带有一个事件循环，可以在服务器上处理并行请求而不会阻塞。这被称为非阻塞`I/O`。当你需要读取数据库或文件时，`Node.js`不会等待`I/O`操作完成，而是继续处理其他请求。

## JavaScript 的其他场景

`JavaScript` 开发充满乐趣。最初，`JavaScript`的主要场景是为浏览器进行开发。随后出现了`node.js`，使我们能够编写服务端代码。然而，`JavaScript`在2019年提供的远不止这些。让我们看看更前沿的选择：

- JavaScript 与 VR：`React360`使得使用`JavaScript`提供VR体验
- JavaScript 可以编译成其他语言：`WebAssembly`将多种语言编译成`JavaScript`，让你能在浏览器中运行代码
- JavaScript中的机器学习与人工智能：`TensorFlow`包含了神经网络实现的机器学习库
- 移动开发：`React Native`提供了一种使用`JavaScript`进行开发的方式
- 区块链编程：`npm`上已有超过一千个区块链相关的库，`Crypto-js`提供了易使用的加密和解密算法
- 网页实时通信：`WebRTC`使得创建具有实时通信功能的应用程序可能
- 微服务：`Seneca`是在应用程序中组织微服务的例子

由于应用场景也在不断涌现，使用`JavaScript`成为一种可选方案。记住，如果一个应用场景在`JavaScript`中变得可行，很可能就会围绕它形成一个充满热情的庞大社区。获得企业支持的可能性也很高。

## JavaScript 在就业市场的主导地位

根据 [2018 年 HackerRank 调查](https://research.hackerrank.com/developer-skills/2018/)：

- `JavaScript`是雇主最需要的语言。总计有47.8%的雇主发布了`JavaScript`相关职位。
- 在`JavaScript`框架方面，雇主需求与员工知识之间存在巨大差距。差距最大的是`React`：33.2%的雇主在寻找`React`开发者，而供应量仅为19%。稀缺意味着更高的薪资、更少的竞争和更多的机会。



你可以成为一名自学成才的开发者，因为公司更看重经验（90.6%）和你的作品集（72.7%），而不是学历。如果你能正确地包装自己，经验可以通过开发个人项目来积累，并最终进入你的作品集。这意味着，在 JavaScript 开发中，只有你自己的努力才能限制你，不存在守门人、大学、实习或认证行业。例如，在柏林/德国，你可以靠自己成为自学成才的程序员，并且可以被雇用，获得比德国公民平均工资更高的薪水。对于许多城市或远程工作机会，同样的原则也适用。

尽管 JavaScript 在开发者偏好的语言中仅排名第五，落后于 Python、C、C++ 和 Java，但这可能被被那些不得不处理 JavaScript 不成熟版本的老程序员带来的负面体验所抵消。在开发者体验方面，一个重要的衡量标准是，在所有语言的所有框架中，排名前四的都是 JavaScript 框架：`Node.js`、`React`、`ExpressJs` 和 `AngularJs`。使用这些框架让开发者感到比其他任何事情都更快乐。

[2018 年 StackOverflow 调查](https://insights.stackoverflow.com/survey/2018/)¹⁵ 呈现了相同的图景：

* JavaScript 是最受欢迎的语言，占比 69.8%。在 StackOverflow 上，JavaScript 比 Python 更受欢迎。
* 三个框架位列最受欢迎框架榜单前列：`Node.js`、`Angular`、`React`。
* 在这项调查中，JavaScript 开发者的薪资被标记为低于许多其他领域的薪资水平。在我看来，这个统计数据具有误导性，因为与需要大量专业知识的语言相比，入门级开发者的薪资在更大程度上掩盖了专家的薪资。根据我的经验，在普通的 JavaScript 第一轮面试中，筛选掉 70% 的申请人并不少见。另一方面，在普通的 C++ 面试中，能进入第一轮面试的人通常更清楚自己在做什么。我鼓励你在 `payscale.com` 或 `glassdoor.com` 上进行自己的研究，以找到要求你技能的具体公司的 JavaScript 开发者薪资。

尽管受众很重要，但在今天世界，选择 JavaScript 你不会错。你也可以预期 JavaScript 会保持上升趋势。

> 总结：

- JavaScript 和 JavaScript 框架在业界广受欢迎
- 对 JavaScript 开发者的需求高于供给

# 为什么现在成为 JavaScript 开发者比以往任何时候都更容易？

我们已经探讨了成为 JavaScript 开发者在经济方面的考量。毫无疑问，无论在客户端还是服务器端，对 JavaScript 开发者的需求都非常高。

然而，世界上没有任何金钱可以弥补糟糕的开发者体验。

学习 JavaScript 比以往任何时候都更容易。多年前，许多挫折阻碍了普通开发者获得最佳的学习体验：

* 计算机资源比现在更稀缺
* 语言的标准化程度远不如现在成熟，导致 `if-else` 结构中包含针对不同浏览器的不同代码片段
* `ES5` 标准提供的开发者体验远不及 `ES2015` 及更高版本
* JavaScript 未被视为一门严肃的编程语言
* 浏览器开发者工具和调试功能尚不成熟
* 第三方库支持稀缺且不可靠
* 优秀的集成开发环境或文本编辑器尚不存在

和任何一个在十五年前编写过 JavaScript 代码的人交谈，你都会得出结论：你现在使用的已经不是同一种语言了。

如果存在问题，热情的开源社区以及 Google 或 Facebook 等科技巨头很可能会为你提供可靠的 JavaScript 解决方案。自 2015 年以来，标准化进程也开始加速。我们正处于 JavaScript 历史上最伟大的时代。而且情况只会越来越好。

# 根据科学，JavaScript 的学习体验是怎样的

第一个好消息是，你可以立即开始编写代码。第二个好消息是，你可以在几秒钟内看到自己努力的成果。你不需要经历漫长的编译过程，用 JavaScript 构建的东西通常会在屏幕上以可见的变化呈现出来。

虽然我并非声称学习 JavaScript 超容易，但我确实认为，在使用 JavaScript 时，你获得的反馈比使用大多数其他语言更直接、更即时。这为什么重要呢？

因为一切条件都已具备，让你体验到[心流](https://en.wikipedia.org/wiki/Flow_(psychology))（flow）。心流体验通常被称为最佳体验。它感觉就像你“进入了状态”。如果你处于心流状态，时间会飞逝。你全身心沉浸在一项活动中。你的学习体验就接近最佳状态了。

根据科学，心流的发生需要几个必要条件：

1. 活动的目标必须清晰
2. 任务既不太容易，也不太难
3. 你能直接获得关于行动结果的反馈

让我们逐一分析这些要点。

## 活动的目标必须清晰

关于目标，只需看看那两项开发者调查，弄清楚在 2019 年成为一名 JavaScript 开发者对你是否有意义。你真的可以作为自由职业者在海滩上工作，或者作为雇员，成为国际团队的一员。编写 JavaScript 代码常常感觉像是在玩乐高。你碰巧还能靠它赚到不错的收入。许多人在半年内就能作为初级开发者高效工作。如果你现在还不会写代码，还有什么比利用自己作为前端或全栈开发者的技能更好的体验可以想象呢？

## 任务既不太容易，也不太难

学习 JavaScript 并非显而易见的事情。你会遇到一些谜题、一些陷阱、一些需要克服的障碍。但不要因此气馁！试想一下，如果你从未面对过挑战，你会成为怎样的人？你现在的人生将没有任何值得骄傲的东西。这些障碍对你有益。这些障碍也使你的学习体验足够有挑战性，从而让你在学习 JavaScript 时能够体验到心流。

我的观点是，学习 JavaScript 并不会难到无法体验心流。显然，这个观点是有争议的，因为如果你曾是一名公交司机，从未见过编程语言，那么你需要一些基础。学习资源 [ES6 in Practice](http://www.zsolym.com/es6-in-practice) 并非为初学者设计的最佳资源，因为它假设你知道编程语言的基本原理、`if` 语句和循环等等。然而，一旦你打下了基础，你准备好学习高级资源，没有什么能阻止你。因此，你会进步，变得更好，而不会因为学习体验感到沮丧。

16 https://en.wikipedia.org/wiki/Flow_(psychology)
17 http://www.zsolym.com/es6-in-practice

## 你能直接获得行动结果的反馈

这正是 JavaScript 的光点。只要你使用客户端，并且不把工具链搞得太复杂，你就能立即获得反馈。刷新浏览器。在某些情况下，无论你做什么，都能立即看到代码运行。因此，JavaScript 是极佳的候选者。

# 总结

无论你是想学习 JavaScript 还是想选择专业方向，花时间欣赏一下。受众很重要，但在当今世界，选择 JavaScript 你不会错。你也可以预期 JavaScript 会保持上升趋势。

> 总结：
> - JavaScript 和 JavaScript 框架在业界广受欢迎
> - 对 JavaScript 开发者的需求高于供给

# 第一部分：JavaScript 基础

我相信实践应用比理论更重要。因此，在本课程中，不要期待冗长的理论让你感到无聊。通过实践理解 JavaScript 的工作原理，让你能够开始编写代码。

## 你的第一行

学习编程时，我们常常从编写并执行 `Hello World!` 程序开始。在像 Java 这样的语言中，标准输出需要很多代码。在 JavaScript 中，只需一行：

```
console.log("Hello World!");
```

分号标记语句的结束。在 JavaScript 中，分号是可选的，因为 JavaScript 解析器会自动插入它们。然而，坚持使用分号是一个习惯，因为在某些边缘情况下，解释器会将分号插入错误的位置。你可能会问，在哪里可以执行这一行代码？给你几个选择：沙盒是一个与其隔离的开发环境，你可以在其中实验代码，而无需处理繁琐的设置、导入或其他任务。它就像一个沙盒，你可以在其中玩耍，而对外界造成后果。

1. 打开 [CodePen](https://codepen.io/pen/?editors=0)。CodePen 是一个在线的 Web 开发沙盒，包含 HTML、CSS 和 JavaScript 代码框。你需要在 JavaScript 框中编写代码。你可以在控制台中看到结果。每当 JavaScript 代码进行更改时，控制台中就会出现新内容。
2. 你也可以在 CodePen 控制台底部编写代码。按下回车键后，你会看到相同的结果。

18 https://codepen.io/pen/?editors=0

## 或者在浏览器中打开一个新标签页

大多数浏览器的操作相同。本节使用的是 Google Chrome。打开 Chrome 标签页后，在标签页内右单击，从上下文菜单中选择“检查”。或者你可以在 Windows 或 Linux 系统按 `Ctrl+Shift+I`，在 Mac 系统按 `Cmd+Shift+I`。Chrome 开发者工具弹出后，你可以在工具顶部看到一个菜单栏。这个菜单栏以 Elements、Console、Network 等开头。选择 `Console`。现在你就能看到一个类似于 CodePen 控制台的界面。`>` 符号是提示符。你可以在 `>` 后面输入你的 JavaScript 代码。

本书会不时出现一些练习。请尝试自己解决。如果遇到困难，可以回顾书籍内容直到你对相关材料熟悉为止。有些练习在题目下方提供答案，另一些则需要你自己完成。

### 练习 1

尝试使用上述方法来运行 `Hello World!` 程序。在 Chrome 开发者工具的控制台中实验一下，如果用 `console.info`、`console.warn` 或 `console.error` 替代 `console.log` 会发生什么。

**解答：** 在 Chrome 开发者工具的控制台中，观察使用 `console.log`、`console.info`、`console.warn` 和 `console.error` 时，消息的颜色以及消息前面的图标。这些颜色和图标代表了日志级别，它们在各种编程语言中大体一致。日志记录是一种记录系统中发生事件的方式。日志记录对于事后发现系统错误以及精确重现发生的情况非常重要。

如果你输入了消息 `console.log("Hello World!");`，你会看到如下的求值结果：

```
"Hello World!"
undefined
```

第一个值是控制台日志，是由 `console.log` 函数写入控制台的值。第二个值是 `undefined`，表示 `console.log` 函数没有定义的返回值。在关于函数的部分之前，你不必理解这意味着什么。在那之前，只需接受 `undefined` 值会出现在你的控制台日志之后这个事实。

注意，你的语句可以跨越多行。在表达式内部按回车键可以将内容分成两行。在上面的代码编辑器中重新格式化你的代码如下：

```
console
  .log(
    "Hello world!"
  );
```



大多数编程语言帮助你创建代表数字、文本中的字符或更长文本的值。你也可以用布尔值来表示真和假的值。你还可以创建代表值缺失的值。这些值都被称为原始数据类型。

“原始”这个名字并非贬义。这些数据类型既不愚蠢，也不比我们在JavaScript中使用的其他任何数据类型差。“原始”这个名字源于它们的简单性。你稍后将学习的其他数据类型是复合类型，它们由许多原始数据类型组成。

## 为什么数据类型对我们很重要？

例如，每当你查看电子邮件、上Facebook或查看银行账户时，你总是会看到数据：你的名字、你的消息、当前的日期和时间，在设置中你还可以看到账户的其他特征。

数据有类型。我们倾向于使用整数（没有小数部分的数字）而不是文本。复选框可能有两个可能的值：真或假。这些数据类型也是独特的。对于每种数据类型，适用不同的操作，其可能的值也不同。

在JavaScript中，有六种原始类型：

- 布尔值（`true` 或 `false`）
- 数字（包括整数如 `1`、`-2`，以及浮点数如 `1.1`、`2e-3`）
- 字符串（`''` 或 `""`，`'ES6 in Practice'` 或 `"ES6 in Practice"`）
- `null` 类型（用 `null` 表示）
- `undefined`（用 `undefined` 表示）
- `Symbol`（暂时不用担心它们）

> 浮点数通常包含一个小数分隔符字符，最常见的是点号。浮点的数的是有限的，因为可用的位数是有限的。

我们很快将了解更多关于浮点数精度限制所引起的异常。

> 可以对给定类型的数据执行操作。操作由代表该操作的运算符表示。例如：`+`、`-`、`*`、`/`。运算符对称为操作数的数据执行操作。

例如，在 `2 * 3` 操作中，`*` 是代表乘法的运算符。乘法有两个操作数：`2` 和 `3`。

一些重要的运算符是：

- `+` 代表加法。例如：`2 + 3` 是 `5`。
- `-` 代表减法。例如：`2 - 3` 是 `-1`。
- 如果 `+` 或 `-` 的左边没有操作数，则 `+` 或 `-` 成为符号。例如：`+3` 或 `-2`。
- `*` 代表乘法。例如：`3 * 2` 是 `6`。
- `/` 代表除法。例如：`3 / 2` 是 `1.5`。
- `%` 代表取模运算，即一个数除以另一个按照整数除法规则得到的余数。例如：`5 % 2` 是 `1`，因为 `5` 除以 `2` 得 `2`，余数是 `1`。换句话说，`5模2的余数是1`。
- `**` 是幂运算符。例如：`2 ** 3`（2的3次方）是 `2 * 2 * 2`，即`8`。

在 [CodePen](https://codepen.io/pen/?editors=0012) 控制台底部，有一行带有 `>` 符号。这是你可以输入 JavaScript 表达式的地方。让我们试一些。输入你在 `>` 符号后面看到的表达式。然后按回车键。你可以看到结果出现在下一行。

---

# 数字类型

处理数字的操作通常很直观。你可以使用四种基本算术运算符（`+`、`-`、`*`、`/`）分别进行加法、减法、乘法和除法。

`%` 运算符称为模运算符。`a % b` 返回 `a / b` 的余数。例如，`7 / 5` 的商是 `1`，余数是 `2`。因此返回值为 `2`。

`**` 运算符称为幂运算符。`5 ** 2` 表示 `5` 的二次幂。

```
> 5
5

> 5 + 2
7

> 7 % 5
2

> 5 ** 2
25
```

运算可以通过括号进行分组。括号会覆盖运算符的执行优先级。例如，在数学中，乘法的优先级高于加法。这意味着，`1 + 2 * 3` 等同于 `1 + (2 * 3)`。

让我们看一个使用括号的例子：

```javascript
> 5 * ( 1 + 2 * ( 3 + 4 ) )
// 5 * ( 1 + 2 * 7 )
// 5 * ( 1 + 14 )
// 5 * 15
75
```

与数学不同，JavaScript 中我们不使用方括号或花括号来分组操作。括号可以嵌套使用。同时，构建有效的括号表达式也很重要，即每个右括号都应该对应一个前面的左括号。

与数学类似，不同的运算符具有不同的优先级（也称为结合性）。当一个运算必须在另一个运算之前执行时，我们说这个运算符：

- 具有更高的优先级，
- 绑定能力更强。

大多数运算符有一个或两个操作数。这意味着运算符将一个或两个值转换为一个新值。例如：

- `5 + 2` 的操作数是 `5` 和 `2`。`+` 运算符将这些操作数转换为 `7`。
- `-(2)` 的操作数是 `(2)`。我给 `2` 加上括号是为了强调 `-` 是一个运算符，而不是用来描述整数的符号。

运算符绑定其操作数。我们已经看到，有些运算符的绑定能力比其他运算符强。例如，乘法的绑定能力强于加法：

```
5 * 2 + 3 ----> 10 + 3 ----> 13
```

我们也看到，运算符可以通过括号来覆盖：

```
5 * (2 + 3) ----> 25
```

算术运算符（`+`、`-`、`*`、`/`、`**`）和符号（`+`、`-`）的优先级如下：

1. 符号 `+` 或 `-` 在数字前面首先计算。
2. 幂运算：在两个操作数中，`**` 的绑定能力最强。
3. 乘法和除法：`*` 和 `/`
4. 最后是加法和减法：`+` 和 `-`

你在 JavaScript 中使用复杂的运算并且确定它们的优先级，请使用括号。过度依赖运算求值会降低代码读性，这意味着如果你总给别人出难题。模运算没有放在上述优先级中，因为在大多数情况下你不会在表达式中用到它。极少数情况下你与其他运算符使用时，请使用括号。`%` 运算符的绑定能力与除法一样。

## 练习 5：确定以下表达式的类型。

- a. `5 + 2`
- b. `5 - 2`
- c. `5 * 2`
- d. `5 / 2`
- e. `5 ** 2`

## 练习 6：计算以下表达式：

- a. `5 - -1`
- b. `2 * 2`
- c. `2 + 3`

## 练习 7：假设你投资了十万美元。使用 JavaScript 计算利率 `2%` 的情况下，1年、2年、5年后你将拥有多少。提示：`2%` 意味着一年后将获得当前金额。`2%` 与当前金额的比值是 `02`。

## 练习 8：确定哪些表达式是有效的。

- a. `2 ** 2`
- b. `(1) + (2)`
- c. `(1 + 2) * (3)`
- d. `-(2 + 2)`

## 练习 9：将以下表达式与可能值匹配。

表达式：

- A. `5 ** 2 + 1`
- B. `11 * (-4)`
- C. `1e2 - 11`

值：`26`, `71`, `125`。

让我们看一些更惊讶的浮点数运算。

```
> 0.1 + 0.2
0.3000000000000004

> 3.1e-3
0.0031
```

关于浮点数的更多信息。由于数字的表示方式，`0.1 + 0.2` 不完全等于 `0.3`。这是正常的，并且在大多数语言中都会发生。

`3.1e-3` 是 `0.031` 的标准形式。将其理解为 `3.1` 乘以 `10` 的负幂的精确值。虽然这种形式类似于 `3.1 * (10 ** -3)`，但存在细微差别。`3.1e-3` 描述的是 `0.031` 的精确值。`3.1 * (10 ** -3)` 描述的是一个需要计算的组合表达式：

```
> 3.1 * (10 ** -3)
0.00310000000000003
```

浮点数算术无法让这个表达式精确。如果你需要精确的值，有两个选择：一个是舍入或截断结果，另一个是将浮点操作数转换为整数。例如，你可以写 `25` 分，而不是 `0.25` 元。当你总是期望小数点后有相同位数的精度时，这种方法有效。

让我们看一个舍入的例子：

```
> 0.1 + 0.2
0.3000000000000004

> Number(0.1 + 0.2).toFixed(1);
0.3
```

在上面的例子中，结果的精度被固定为一位小数。

除法 `0 / 0` 或使用不匹配的类型会创建一个非数字（not a number）或 `NaN` 的特殊数字。具有讽刺意味的是，我们很快会看到 `NaN` 值的类型是 `number`。

```
> 0 / 0
NaN

> 'ES6 in Practice' * 2
NaN
```

后者对于 Python 用户来说很有趣，因为在 Python 中，结果会是 `'ES6 in PracticeES6 in Practice'`。JavaScript 不是这样工作的。

另一个有趣的数值：`Infinity`。

```
> 1 / 0
Infinity

> Infinity * Infinity
Infinity

> -1 / 0
-Infinity

> 1e308
1e+308

> 1e309
Infinity
```

JavaScript 将非常大的数字注册为无穷大。例如，`10` 的 309 次幂被表示为无穷大。除以零也会得到无穷大。

让我们看一些字符串。

```
> 'ES6 in ' + 'Practice'
"ES6 in Practice"
```

## 练习 10：确定以下数字的类型和值：

- a. `(1 - 1) / 0`
- b. `(1 - 1) / 1`
- c. `5`
- d. `5 ** 0`
- e. `(5 / 0)`

# 布尔类型

让我们来看看布尔值。布尔值要么 `true`，要么 `false`。

`!` 运算符取反。`!true` 变成 `false`，而 `!false` 变成 `true`。

```
> !true
false

> !false
true
```

任意值都可以使用 `Boolean` 函数转换为布尔值：

```
> Boolean(0)
false

> Boolean(1)
true

> Boolean(2)
true

> Boolean(null)
false
```

`!` 运算符不仅对值取反，还会将其转换为尔值。例如：

- 空字符串 `""` 在布尔表达式中默认评估为 `false`。对该值取反得到 `true`。
- 任意长度至少为一个字符的字符串在布尔表达式中评估为 `true`。对该值取反得到 `false`。

```
> !""
true

> ! "
false
```

在 JavaScript 中我们区分真值（truthy）和假值（falsy）。这些值不一定是布尔值。它们的值只有在类型转换后才会变成 `true` 或 `false`。

真值（truthy）是使得 `Boolean(v)` 为 `true` 的 `v`。真值示例包括：非零整数、包含一个字符的字符串。假值（falsy）是使得 `Boolean(w)` 为 `false` 的 `w`。假值包括：空字符串、`0`、`null`、`undefined`。

问：为什么我们需要使用 `Boolean` 函数进行类型转换？

答：因为否则自动类型转换会产生非预期结果。例如，在表达式 `2 == true` 中，比较的两边都会转换为数字。由于 `Number(true)` 的值为 `1`，表达式 `2 == 1` 被评估为 `false`：

```
2 == true ---> 2 == Number(true) ---> 1 ---> false
2 == false ---> 2 == Number(false) ---> 0 ---> false
```

此外，`null` 和 `undefined` 既不是 `true`，也不是 `false`：

```
> null == true
false

> null == false
false

> undefined == true
false

> undefined == false
false
```

但是：

- `Boolean(null)` 和 `Boolean(undefined)` 都为 `false`
- `!null` 和 `!undefined` 都为 `true`
- `!!null` 和 `!!undefined` 都为 `false`

与 `Boolean` 函数类似，双重否定也将任意值转换为布尔值：

- 如果 `v` 是真值，则 `!v` 为 `false`，`!!v` 为 `true`。
- 如果 `w` 是假值，则 `!w` 为 `true`，`!!w` 为 `false`。

示例：

```
> !!""
false

> !!"a"
true

> !!0
false

> !!1
true

> !!NaN
false

> !!Infinity
true

> !!null
false

> !!undefined
false
```

> 一旦你开始编写复杂的软件，请使用 `Boolean` 函数而不是双重否定来将值转换为布尔值。这样，你的代码更具可读性。

我们可以使用 `>`, `>=`, `==`, `===`, `<=`, `<` 来比较两个值。加号运算符连接字符串。连接意味着两个字符串连接在一起。

# 字符串与转义序列

接下来是字符串：

`'ES6 in ' + 'Practice'` -> `"ES6 in Practice"`

加号运算符连接字符串。连接意味着两个字符串的内容连接在一起。一个常见问题是，如果引号代表字符串，那么在字符串内部写引号怎么办？有多种解决方案：

// 解决方案 1：
```javascript
console.log( 'This is a quote' );
```

// 解决方案 2：
```javascript
console.log( 'It\'s' );
```

// 解决方案 3：
```javascript
console.log( "This is a quote" );
```

在单引号内部使用双引号或在双引号内部使用单引号是最简单的方法。

如果你需要在字符串内部使用相同的引号，可以使用转义字符 `\`：

```javascript
console.log( 'It\'s a beautiful day' );
console.log( "He said \"Hello!\"" );
```

# null、undefined、symbol

null、undefined、symbol 是原始类型。

null 表示一个已定义的变量的值缺失。undefined 表示一个值未定义。我们稍后会讨论 `null` 和 `undefined` 的区别。

```
> null
null

> undefined
undefined

> void 0
undefined

> Symbol('ES6 in Practice')
[object Symbol] {}
```

Symbol 是一个唯一的值，没有关联的字面量值。它们作为唯一键非常有用，因为 `Symbol() == Symbol()` 为 false。目前阶段，只需接受 symbols 的存在。你现在还不必在任何地方使用它们。


```
Number( 2 ).toString( 2 );
// --> "10"

Number( 3 ).toString( 2 );
// --> "11"
```

**练习 17：** 不计算表达式，估算十进制值 `2 ** 24` 和十六进制值 `FFFFFFFF` 的差值。创建一个 JavaScript 表达式来计算这个差值。

**练习 18：** 你会使用哪种数据类型来建模以下数据？如果你选择了数字类型，请选择使用整数还是浮点数。

- A. 你的名字
- B. 你的银行账户号码（假设它只包含数字）
- C. 你的年龄
- D. 你是否年满 18 岁
- E. 一本书的价格是 9 美元 95 分分

# 变量：let、const 和 var

在前几节中，我们学习了如何使用数据类型以及如何对不同类型的数据执行操作。然而，根据我们目前的知识，如果我们想在代码中执行两次相同的计算，我们必须手动复制公式或结果。变量通过使我们能够在代码中访问操作的结果来帮助我们自动化并简化这个过程。

首先，在下面的示例中，你必须知道 `console.log` 可能打印由逗号分隔的任意数量的参数。在控制台中，这些值紧挨着出现，由空格分隔。

```
> console.log( 1, 2, 3 )
1 2 3
```

通过右键点击一个网站，从上下文菜单中选择“检查”，然后选择“Console` 标签页，可以打开 Google Chrome 的控制台。在控制台中，你可以输入以下表达式：

```
> 1
1

> 2 + 3
5

> 'JavaScript'
"JavaScript"

> JavaScript
Uncaught ReferenceError: JavaScript is not defined
    at <anonymous>:1:1
```

虽然前三种情况你得到两个整数和一个字符串结果，但在第四种情况下，你会得到一个引用错误。出现此错误是因为 `JavaScript` 是一个变量，并且这个变量尚未在代码中创建。

在创建这个变量之前，让我们先澄清一下变量是什么。在计算机编程中，变量就像抽屉，我们用来存储值。

## let 关键字

我们可以使用 `let` 关键字创建变量。把变量想象成一个抽屉。`let` 声明一个变量，意味着创建了一个带有把手的抽屉。声明是一个创建抽屉并将抽屉钥匙交给我们的过程，以便我们可以访问其内容。

```
let myDrawer;
```

你可以将一个值放入你的抽屉：

```
myDrawer = '$1.000';
```

要访问该值，你必须抓住抽屉的把手并打开它。在这个例子中，你有一个名为 `myDrawer` 的抽屉。它包含一个写有 '$1.000' 的字符串。要访问你的一千美元，你必须打开抽屉：

```
> myDrawer
'$1.000'
```

你可以使用 `=` 号为变量分配一个初始值。这被称为赋值，因为我们给变量分配了一个值。变量生命周期中的第一次赋值被称为定义或初始化。

声明和初始化步骤可以合并为一步。让我们创建第二个抽屉，我们同时声明并初始化一个变量：

```
let mySecondDrawer = '$1.000';
```

即使你还没有初始化一个变量，也可以访问它。它的值变成 `undefined`。

```
let declaredAndDefined = 5;
let declaredButLaterDefined;
let declaredNotDefined;

console.log(
    declaredAndDefined,
    declaredButLaterDefined,
    declaredNotDefined
);
```

- 变量 `declaredAndDefined` 在定义同一行被声明
- 变量 `declaredButLaterDefined` 仅在声明之后的行中定义
- 变量 `declaredNotDefined` 根本没有定义

让我们看看我们将 `declaredNotDefined` 这一行移到 `console.log` 语句下方会发生什么。

# 常量

常量的行为与变量类似。可以使用 `const` 关键字创建常量：

```
const PI = 34;
PI = 2;
Uncaught TypeError: Assignment to constant variable.
```

由于常量的值不变，它们必须在声明同一语句中初始化。如果我们忘记这个步骤，就会一条错误：

```
const c;
Uncaught SyntaxError: Missing initializer in const declaration
```

# 作用域

变量的作用域表示变量在哪里，在哪里可见。在 JavaScript 中，有不同的作用域供使用：

1. 全局作用域
2. 块级作用域（`let`、`const`）
3. 函数作用域（`var`）
4. 词法作用域（稍后介绍）
5. 模块作用域（此处讨论）

在大多数语言中，前两种作用域是可用的。函数作用域是 JavaScript 的一个特性。自 2015 年 JavaScript 版本（ES6）以来，函数作用域不再流行，因为块级作用域 `let` 和 `const` 出现了。关于块级作用域，代码中任何地方创建块。使用大括号（`{` 和 `}`）：

```
{
    // This is block
}
```

使用 `let` 和 `const` 创建的变量仅在块内可见：

```
{
    let box = 5;
    console.log( box );
}
```

上述代码显示 `box` 的值：

```
{
    let innerBox = 6;
}
console.log( innerBox );
```

在上面的代码段中，一旦执行到 `console.log` 语句，就会得到 `ReferenceError`：

```
VM124:4 Uncaught ReferenceError: innerBox is not defined
```

这是因为 `innerBox` 在块外部可见。

# 全局作用域

与其他语言类似，JavaScript 也有全局变量。例如，你使用全局 `console` 变量来记录消息。除了 `console`，打开 Google Chrome 开发者工具控制台，探索全局变量：

```
> document.location.href
"http://zsoltnagy.eu"

> document.location.host
"zsoltnagy.eu"

> screen.width
1920

> let globalVariable = true
true

> globalVariable
true

> secondGlobalVariable = true
true

> secondGlobalVariable
true
```

如你所见，可以在全局作用域中创建全局变量。无论是使用 `let`、`const` 还是 `var`（稍后介绍）关键字来创建这些变量，还是直接进行赋值都没有关系。在赋值的情况下，会发生以下情况：

- 程序检查同一块（`let`、`const`）或函数（`var`）中是否有局部声明的变量。
- 如果没有，程序会从内到外检查封装块的块和函数。这是访问词法作用域的过程，我们稍后将深入讨论。
- 如果在词法作用域中没有定义变量，则会访问全局作用域，创建一个全局变量并将其值设置为赋值的值。

在下面的例子中，为了简单起见，我们只使用块，因为我们还没有学习函数作用域是如何工作的。

```
// first file:

{
    let firstBox = 1;
    {
        firstBox = 2;
        secondBox = 3;
        console.log( firstBox, secondBox );
    }
}
```

如果执行上面的代码，值 `2 3` 会被打印到控制台。变量 `firstBox` 存在于封装我们当前块的块中。变量 `secondBox` 是通过赋值创建的，并且没有用此名称声明的 `var`、`let` 或 `const` 变量。因此，该变量存在于全局作用域中。

现在假设 `first file` 的内容已加载，并且我们还加载了以下名为 `second file` 的代码段：

```
// second file:

{
    let firstBox = 4;
    {
        console.log( firstBox, secondBox );
    }
}
```

执行此代码后，将打印值 `4 3`。变量 `firstBox` 定义在 `console.log` 所在块的外部块中。变量 `secondBox` 是全局的，它是在加载 `firstFile` 时创建的。从现在起，`secondBox` 变量将跨所有加载的文件共享。

```
// third file:
console.log( secondBox );
```

执行此代码也可以访问全局变量 `secondBox`。

```
// fourth file:
console.log( firstBox );
```

加载第四个文件的结果是一个 `ReferenceError`，因为 `firstBox` 在此作用域不存在：它仅存在于 `first file` 和 `second file` 中。

```
VM55:19 Uncaught ReferenceError: firstBox is not defined
    at <anonymous>:1:4
```

编写软件时经常创建数十万行代码，有时甚至百万行。随着程序增长，跟踪哪个代码以访问和修改哪些变量变得困难。因此，作为一个通用规则，建议使用局部作用域，尽可能避免全局变量。大多数时候，全局变量是由于赋值前忘记了 `let`、`const` 或 `var` 关键字创建的。

# var 关键字和函数作用域

为了完全理解 `var` 关键字的工作，你需要了解函数是什么。稍后会学习。目前只需使用 `var` 声明：

```
var globalBox = 2;
function scope() {
    var functionScopedBox = 1;
    console.log( globalBox );
}

// we call the function to execute its content
scope();
console.log( functionScopedBox );
```

`globalBox` 可以从代码中的任何地方访问。但是当在最后记录 `functionScopedBox` 时，我们得到以下错误：

```
Uncaught ReferenceError: functionScopedBox is not defined
```

`var`的作用域在 JavaScript 中是独特的，并且经常造成混乱。在大多数语言中，开发者习惯于块级作用域。因此，开发者很难适应 `var` 声明的工作方式：

```
{
    var box = true;
}
console.log( box );
```

这段代码执行没有问题，并且在块外部访问。这是 `box` 为全局作用域。

# 变量命名

变量应描述性的方式命名。我们需要使用变量名来描述它存储的数据。一个好的变量名就像一个好的注释。创建良好变量的最佳实践包括：

1. 变量以最佳方式描述其内容
2. 在所有可能的变量名中选择最短的名称

例如，在 `invoiceSum` 和 `invoiceItemSum` 之间，前者完美地抓住了变量存储内容的本质，因为很明显。通常的做法使用小写字母开头变量名。如果变量名包含多个单词，我们将它们连接成单词，并从第二个单词开始将每个单词的首字母大写。这种变量命名称为 `camelCase`。

# 在一条语句中创建多个变量

一个最佳实践是创建我们用于描述过程或函数的所有变量，然后对这些变量执行操作。例如：

```javascript
let name = "Zsolt";
let website = "zsolty.eu";

console.log( name, website );
// 其他操作...
```

我们可以通过逗号来简写变量声明：

```javascript
let name = "Zsolt",
    website = "zsolty.eu";
```

类似地，我们也可以先声明变量，稍后再定义：

```javascript
let name, website;

name = "Zsolt";
website = "zsolty.eu";
```

# 练习：let、const、var

**练习 19：** 在不运行代码的情况下，判断标准输出会写入什么：

```javascript
let a;
console.log( 'a: ' + a );
a = 5;
console.log( 'a: ' + a );
```

**练习 20：** 在不运行代码的情况下，判断标准输出会写入什么：

```javascript
let a = 5;
{
    let a = 2;
    a += 1;
    console.log( 'a: ' + a );
}
console.log( 'a: ' + a );
```

**练习 21：** 在不运行代码的情况下，判断标准输出会写入什么：

```javascript
let a = 5;
{
    console.log( 'a: ' + a );
    let a = 2;
}
```

**练习 22：** 在前面的章节中，我们计算了十六进制数 `FF` 在十进制和二进制中的值。修改下面的代码，使得我们只运行一次 `Number.parseInt( 'FF', 16 )` 计算。提示：使用变量。

```javascript
console.log(
    'FF in base 10:',
    Number.parseInt( 'FF', 16 ),
    '\nFF in base 2:',
    Number.parseInt( 'FF', 16 ).toString( 2 )
);
```

**练习 23：** 延续上一个练习，建议另一种修改方案，引入一个变量以消除重复计算。

**练习 24：** 在实际的软件中，哪些变量名遵循了良好的命名规范？

- A. `variable`
- B. `nowTimestamp`
- C. `firstParameter`
- D. `eurodollarrate`

# 数组

数组是一个有序的项目列表。项目可以是任何类型。你知道，在大多数局里，有成百千个邮箱。每个邮箱可能包含也可能不包含东西。每个邮箱都有数字把手。打开它，抓住它的把手，就可以访问其内容。

诀窍在于，在数组的情况下，这些邮箱被称为*键*（keys），通常连续的。

```javascript
let days = [ 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday' ];
```

数组不必包含相同类型的元素。我们可以将字符串、`null`、`undefined`、符号和其他数组放入数组中：

```javascript
let storage = [ 1, 'Monday', null ];
```

根据一个笑话，比尔·盖茨曾访问一个低级班级，让孩子们开始数到十……（此处省略）。

这个故事的要点是，数组的每个元素都可以使用从零开始的*索引*（index）来访问：

```
> days[0]
'Monday'
> days[4]
'Friday'
> days[5]
undefined
```

在第三个例子中，我们索引超出了数组。

数组有长度：

```
> days.length
5
```

我们经常需要访问数组的最后一个元素。例如，`days`数组的长度为5。数组的索引从0开始。因此，最后一个索引是4。*通常，最后一个元素的索引等于数组的长度减1：*

<|channel>thought
<channel|>
```javascript
> days.length - 1
4
> days[ days.length - 1]
'Friday'
```

> 注意：在其他一些语言中，例如`Python，我们可以使用索引-1来引用列表的最后一个元素。在`Python`中，`days[-1]`等同于`days[len(days) - 1]`。索引-1被解释为从列表末尾向前计数的第一个元素。在`JavaScript`中，我们不能使用这种索引方式。

你可以向数组的开头和结尾添加元素。

```javascript
> days.push( 'Saturday' );
```

```javascript
> console.log( days ); // 在末尾添加 'Saturday'
["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"]
```

```javascript
> days.unshift( 'Sunday' ); // 在开头添加 'Sunday'
["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"]
```

你也可以从数组中移除这些元素：

- `pop` 从数组末尾移除最后一个元素并返回它。

- `shift` 从数组开头移除第一个元素并返回它。

```javascript
> let element = days.pop();
> console.log( element, days );
"Saturday" ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday"]
```

```javascript
> let secondElement = days.shift();
> console.log( element, days );
"Sunday" ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"]
```

类似于对象，你可以从数组中删除任何元素。`undefined`值将被放置在该元素的位置：

```javascript
> delete days[2]
["Monday", "Tuesday", undefined, "Thursday", "Friday"]
```

数组的值可以通过使用它们的索引，并将其赋值为新值来设置。你可以覆盖现有值，或者向数组添加新值。添加的值的索引不必是连续的：

```javascript
> days[2] = 'Wednesday';
> days[9] = 'Wednesday';
> console.log( days );
["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", undefined, undefined, undefined, undefined, "Wednesday"]
```

字符串也提供了对其字符的访问方式，就像字符串是一个字符数组一样：

```javascript
const str = 'Hello';
console.log( str[1], str[4], str[5] );
// --> e o undefined
```

索引1处的元素是字符 'e'。索引4处的元素是字符串的第五个字符，'o'。如果我们尝试访问字符串索引5处的元素，我们会得到数组的第六个字符。但这会使我们索引超出数组。在`JavaScript`中，数组或字符串的索引超出是可能的：我们只会得到一个`undefined`值。

我们最后一个语言构造是`slice`方法。毫不奇怪，这个方法切片一个数组，返回一个包含连续元素子集的新数组。

我们可以如下指定切片的开始：

```javascript
let days = [ 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday' ];
> console.log( days.slice( 1 ) )
[ 'Tuesday', 'Wednesday', 'Thursday', 'Friday' ]
> console.log( days.slice( 4 ) )
[ 'Friday' ]
```

切片的开始是我们希望在切片中看到的第一个元素的索引。这个数字也可以是零，这种情况下我们创建了原始数组的浅拷贝：

```javascript
let daysCopy = days.slice( 0 );
daysCopy[0] = '???';
console.log( days );
// [ 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday' ]
console.log( daysCopy );
// [ '???', 'Tuesday', 'Wednesday', 'Thursday', 'Friday' ]
```

如果你了解浅拷贝和深拷贝的区别，请注意`slice`创建的是前者。否则，在这个阶段，只要理解`slice`总是返回一个新数组，复制其元素即可。

为了进行有用的切片操作，我们还需要一种指定切片结束的方法。在`JavaScript`中，切片的结束被指定为我们不想在数组中看到的第一个元素的索引。

```javascript
// Monday - Wednesday:
// - 我们从第0个元素开始，
// - 我们不想看到的第一个元素在索引3处
> days.slice( 0, 3 )
[ 'Monday', 'Tuesday', 'Wednesday' ]
```

```javascript
// Thursday:
// - 我们从索引3开始
// - 我们不想看到的第一个元素在索引4处
> days.slice( 3, 4 )
[ 'Thursday' ]
```

指定切片的结束是可选的。这意味着`days.slice( 1 )`等同于`days( 1, days.length )`。

> 注意：由于许多开发者学习`Python，值得注意的是`Python`在索引中使用冒号进行切片，`days[0:3]`等同于`days( 0, 3 )`。在`Python`中，只要冒号的任何一边有零，那个零就是可选的：`days[:3]`等同于`days[0:3]`，`days[2:]`等同于`JavaScript`中的`days.slice( 2 )`，而`days[:]`等同于`JavaScript`中的`days.slice( 0 )`。我们可以看到一些编程语言彼此之间是多么相似。你最好学习其思维过程，然后语法就会变得容易。

与大多数主题一样，请记住我们只是在涵盖基础知识，让你开始编写代码。关于`JavaScript`数组有多层知识。我们将在它们变得重要时揭示这些教训。

# 练习：数组

**练习 25：** 在不执行代码的情况下，判断控制台会输出什么：

```javascript
let array = [ 7, 15, 32, 9, '3', '11', 2 ];

// A.
console.log( array[3] );

// B.
console.log( array[7] );

// C.
console.log( array.pop() );
```

# 练习 26

在不执行代码的情况下，确定以下代码输出到控制台的内容：

```javascript
const days = [
  'Monday',
  'Tuesday',
  'Wednesday',
  'Thursday',
  'Friday'
];

console.log( days[2] );
console.log( days[1][2] );
console.log( days[ days.length - 1][1] );
```

# Object 类型

本节将介绍 `Object` 类型。我们在这里只学习基础知识。

对象是一种以`String` 或`Symbol`为键、以任意值为值的数据结构。可以把它想象成一台机器，接受一个键，然后给你一个值。有些人称这种数据结构为关联数组，另一些人称之为哈希表。这些名字可能听起来很哨，但本质上指的是同一回事。

> 注：我们现在只处理`String`键。`Symbol`键也用于字符串。这是一个高级主题，我们将在后面学习。关联数组就像人类记忆。为了访问一段记忆，我们需要一个关联，也就是键通过提供权限来解锁记忆。关联记忆就是内容。在`JavaScript`中，我们将使用字符串来描述内容。

```javascript
let author = {
  name: null,
  website: "zsoltan",
  age: 35
};

console.table( author );
```

在 Google Chrome开发者台中运行上述代码。你可以看到`console.table`表格形式枚举了`author`对象的键和值。同样，`console.log( author )`也会记录`author` 对象，但在日志中，我们需要更多点击查看键和值。可以通过点号访问`author`对象的成员。例如`author.name`提供了读写访问。我们可以更改`author.name`的值。

```javascript
author.name = "zsoltan";
console.log( author.name, author.website );
// 输出: zsoltan zsoltan
```

可以使用`delete`操作删除对象的成员：

```javascript
delete author.name;
console.log( "name: ", author.name );
// 输出: name: undefined
```

如果对象中的某个字段未声明，则该字段的值为`undefined`。

```javascript
let o = {};

o.name;
// undefined
```

对象包含字段。对象中的字段可以通过以下方式引用：

- 介绍过的点号法：`object.name`
- 方括号（关联数组）表示法：`object[name]`

让我们探讨一下，如果键在一个变量中，我们如何选择成员：

```javascript
let key = 'website';
// 如何选择 author.website?
```

解决方案是使用方括号法获取`author[key]`。方括号内的值转换为键。

```javascript
author[ key ];
// 输出: zsoltan
```

我们已经知道键是一个字符串。我们在方括号内提供不同类型的键，那么键会被转换为字符串：

```javascript
const key = 1;
const street = {};

street[ key ] = 'house';
```

执行上述代码后，值 `{ "1": "house" }` 会打印到控制台。对象的可以是另一个对象：

```javascript
let car = {
    size: 1,
    parking: car
};
```

这里我们可以看到`car` 有一个整数`size` 和一个名为`parking`的属性。我们通常使用花括号通过键值对构建对象。一旦对象构建，我们可以向其添加属性：

```javascript
let garage = { owner: 'zsoltan' };
```

在上面的例子中，我们将`garage.owner`的值从`undefined`更改为一个对象。我们看到两种方式引用成员：

1. 点号法：`garage.size`的值是1。
2. 方括号法：`garage['size']`是1。

这两种表示法是等效的。注意的是，在方括号法中，你需要可以转换为字符串且抛出错误。因此，如果你尝试获取`garage[nonExistingKey]`，你会得到一个错误。我们将在后面学习更多对象的知识。

# 练习：对象

**练习 27：** 创建一个对象来模拟票开奖。票开奖由其时间定义。我们使用格式为"2020-11-25 18:20"的字符串来模拟这个时间。我们还存储奖金，它也是一个格式为"$10000"的字符串。我们还存储五个数字，这些数字在1到90之间。这些值存储在一个数组中。

**练习 28：** 假设给定以下对象：

```javascript
let ticket = {
    from: {
        airport: 'HAN',
        date: '2020-11-05',
        time: '09:40'
    },
    to: {
        airport: 'AAA',
        date: '2020-11-05',
        time: '11:25'
    },
    name: 'JavaScript',
    passport: '123456XY'
};
```

使用此对象，将以下值写入控制台：

- 出发和到达的时间和日期
- 姓名
- 护照号码
- 目的地的机场代码

**练习 29：** 创建一个对象，该对象包含无限长的引用链。例如，如果你将对象命名为`tree`，请确保`tree.tree`、`tree.tree.tree`、`tree.tree.tree.tree`等都是可用的。

```javascript
let tree = { leaf: "fruit" };

// 在此处编写你的解决方案，使得下面的日志
// 都输出 "fruit"

console.log( tree.leaf );          // "fruit"
console.log( tree.tree.leaf );     // "fruit"
console.log( tree.tree.tree.leaf ); // "fruit"
// ...
```

**练习 30：** 假设有一个保险箱对象。保险箱通过一个秘密的键组合"123456"打开。创建一个引用来解锁保险箱，并提供对属于键"123456"的值的访问。

```javascript
let safe = { "123456": "$10000" };
```

**练习 31：** 我们学到对象的键可以是字符串或`Symbol`。假设有一个变量声明并定义为`let num = 5;`。考虑以下代码：

```javascript
let num = 5;
let o = {};

o[ num ] = true;

console.log( o, o[ 5 ], o[ "5" ] );
```

在你的控制台中运行上述代码。解释`o[ 5 ]`中的什么导致了你看到的。现在创建一个包含"5"字符串的变量，并运行此代码：

```javascript
let text = '5';

o[ text ] = false;

console.log( o, o[ 5 ], o[ "5" ] );
```

**练习 32：** 创建一个`map`对象，其键为数组`arr`的值。这些键对应的值为`true`。使用`console.table`函数在Chrome开发者台中检查`map` 对象。

```javascript
let arr = [1, 5, 3, 1];

let map = {};

// 在 _____ 符号位置编写有效的 JavaScript 代码，
// 以向 map 添加键对。
// map[ arr[0] ] = 0;
// map[ arr[1] ] = 1;
// map[ arr[2] ] = 2;
// map[ arr[3] ] = 3;

console.table( map );
```

**练习 33：** 修改上一个练习，使得键`arr[0]`、`arr[1]`、`arr[2]`、`arr[3]`对应的值不是`true`，而是它们各自的索引`0`、`1`、`2`、`3`。在运行代码之前，确定对象`map`中存储的键值对。

# 函数

可以把函数想象成一个数学函数，它给你输入变量和输出变量之间的关系。如果你不喜欢数学，可以把函数想象成一台自动售货机。你给它一些硬币和一个数字，它给你一瓶冷饮。

```javascript
function add( a, b ) {
    return a + b;
}
```

此函数定义描述了其输入变量 `a` 和 `b` 与函数返回值之间的关系。



`return` 语句返回函数的值。当使用参数 `a` 和 `b` 调用 `add` 函数时，它会计算 `a+b` 的值并将其返回。示例：

```
> add( 5, 2 )
7
```

尝试修改输入变量。返回值也会随之改变。尝试用一个变量调用 `add` 函数，例如 `add( 5 )`，看看会发生什么。

函数有助于创建可重用的代码块，你可以用不同的参数调用它们。一旦你掌握了控制结构的基础，我们就会编写更多实用的函数。

你也可以在不将名称放在 `function` 关键字和参数列表之间的情况下定义函数。如果你想使用变量创建对它的引用，这种结构非常合适。记住，变量 `subtract` 是一个抽屉的句柄。这一次，你的抽屉里包含一个函数。

```
let subtract = function( a, b ) {
    return a - b;
}
```

还有另一种在 ES6 中首次引入的流行表示法：胖箭头表示法。

```
let multiply = ( a, b ) => a * b;
```

胖箭头描述了参数列表和返回值之间的关系。换句话说，它期望两个值 `a` 和 `b`，并将这些值转换为 `a * b`。

箭头函数通常用于当输入可以转换为可以使用输入变量计算出的输出时：

```
function functionName( a, b, ... ) {
    return value;
}

// 转换：
var functionName = ( a, b, ... ) => value;
```

如果只有一个输入参数，你可以省略其周围的圆括号：

```
let square = a => a * a;
```

所有函数都可以使用它们的引用来调用：

```
> add( 2, 3 )
5
> subtract( 2, 3 )
-1
> multiply( 2, 3 )
6
> square( 2 )
4
```

当函数不返回任何内容时，其返回值变为 `undefined`：

```
> let empty = function() {}
> empty()
undefined
```

JavaScript 解释器总是在每个函数的末尾插入一个 `return undefined;` 语句。这是每个函数的默认返回值。开发者可以通过指定 `return` 语句来覆盖此默认值。

函数内部的变量与函数外部的变量不同：

```javascript
let coins = 5;
function addOne( coins ) {
    coins = coins + 1;
    return coins;
}

> addOne( coins )
6
> coins
5
```

函数内部的 `coins` 变量在函数的作用域内有效。它遮蔽了函数外部的 `coins` 变量。因此，给内部 `coins` 变量加一对外部值没有任何影响。要查看此代码的实际执行情况，请访问[此链接](http://pythontutor.com/javascript.html#code=let%20coins%20%3D%205%3B%0Afunction%20addOne(%20coins%20)%20%7B%0A%20%20%20%20coins%20%3D%20coins%20%2B%201%3B%0A%20%20%20%20return%20coins%3B%0A%7D%0Alet%20result%20%3D%20addOne(%20coins%20)%3B%0Aconsole.log(%20result%20)%3B%0Aconsole.log(%20coins%20)%3B&curInstr=7&mode=display&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D)。

我们之前学过，使用 `var` 声明的变量是函数作用域的。函数参数也是函数作用域的：

```
let coins = 5; // 即使使用了 var，这也是一个全局变量
function addOne( coins ) {
    // 内部的 coins 变量遮蔽了全局的 coins
    // 只能访问内部的 coins 变量
    coins = coins + 1;
}
```

当一个变量同时存在于函数内部和外部时，当我们执行函数内部的代码时，内部变量遮蔽外部变量。这就是 `coins` 变量的情况。在不改变执行的情况下，我们可以安全地重命名内部变量，说明这两个变量是不同的：

```
let coins = 5;
function addOne( innerCoins ) {
    innerCoins = innerCoins + 1;
    return innerCoins;
}
```

# 练习：函数

**练习 34：** 让我们回顾数字转换的解决方案：

```javascript
let hexadecimalValue = 'FF';
let baseTenValue = parseInt(hexadecimalValue, 16);
console.log(baseTenValue + ' in base 10:');
```

**练习 35：** 编写一个函数，它期望一个十六进制数字的字符串，将该十六进制值转换为十进制和二进制，并在控制台输出结果：

```
> convert('ACE')
ACE in base 10: 276
ACE in base 2: 10101100
```

/**
 * 函数总结
 * @param string 描述
 * @return undefined
 */

# 立即调用表达式

注意，本节包含一个常规面试。问题是：什么是 IIFE（立即调用函数表达式）？简短的回答是，创建一个函数并立即调用它。我们可以使用 `function` 关键字创建函数：

```javascript
function f() {
    console.log( "f() has executed" );
}
```

为了调用函数，我们需要在函数名后添加圆括号：

```
f();
// 输出：f() has executed
```

如果我们把 `()` 直接放在函数定义之后，就可以将函数定义和调用起来。为此，我们需要将函数定义放在圆括号内：

```javascript
(function f() {
    console.log( "f() has executed" );
})();
// 输出：f() has executed
```

不要忘记函数定义周围的圆括号。如果你省略它们会得到一条错误：

```javascript
function f() {
    console.log( "f() has executed" );
}();
// 错误：Uncaught SyntaxError: Unexpected token )
```

函数 `f` 的名称在代码中没有任何意义，它就像注释。我们可以安全地省略名称 `f`，创建一个匿名函数。

```javascript
(function() {
    console.log( "The function has executed" );
})();
```

也可以向立即调用表达式传递参数：

```javascript
(function( text ) {
    console.log( text );
})( "The function has executed" );
```

在带参数的版本中，你可以用任何值替换字符串 `"The function has executed"`。

从 ES2015（2015 年 JavaScript规范）开始，立即调用表达式可以使用箭头函数创建：

```javascript
( text => console.log( text ) )( "Done." );
```

这种格式并不意外，因为 `text => console.log( text )` 可以被 `console.log` 本身替代。它期望一个 `text` 变量，将其写入控制台，并返回 `undefined`。如果我们进行替换，会得到以下表达式：

```
( console.log )( "Done." );
```

`console.log` 周围的圆括号也可以省略，结果如下：

```
console.log( "Done."
```

# 练习：立即调用表达式

**练习 36：** 创建一个立即调用表达式，它期望两个数字参数并返回这两个参数的和。你可以假设这些参数是数字，不必检查它们的类型。

# 变量作用域与遮蔽

本节将具有挑战性，因此请多次阅读以让内容充分理解。让我们总结一下我们关于作用域所学到的内容：

```javascript
let global = true;  // 全局变量
{
    let block = true; // 块作用域
}

(function() {
    var functionScoped = true; // 函数作用域
})();
```

全局变量在任何地方都可见。

块作用域变量在创建它们的块内可见，但在该块外部不可见。

最后一个例子是立即调用函数表达式。这是一个我们使用 `( )` 符号立即调用的函数。使用 `var` 在此函数调用内部创建的变量在函数内部可见，但在外部不可见。让我们看看如果我们嵌套多个立即调用函数表达式会发生什么：

# 练习：变量作用域与遮蔽

**练习 37：** 不运行程序，判断控制台输出的值：

```javascript
// 全局作用域
let x = 1;
{
    // 代码块 A
    let x = 2;
    {
        // 代码块 B
        let x = 3;
    }
    {
        // 代码块 C
        console.log( x );
    }
}
```

**练习 38：** 重写上一练习的代码，将 `let` 替换为 `var`，并使用立即调用函数表达式替代代码块。

# typeof 运算符

在某些情况下，我们可能需要检查变量保存值的类型。为了执行任务，我们将介绍 `typeof` 运算符。回顾一下 `typeof` 运算符的概念：`typeof` 运算符接受一个值并返回字符串。例如：

```javascript
typeof ''             // "string"
typeof 0              // "number"
typeof true           // "boolean"
typeof {}             // "object"
typeof []             // "object"
typeof undefined      // "undefined"
typeof Symbol()       // "symbol"
```

只有一个问题：数组、对象和 `null` 值具有相同的类型。如果我们区分它们就好了：

```javascript
> Array.isArray([1, 2])
true
> Array.isArray({a:1})
false
```

对于 `null` 值，简单的比较：

```javascript
let name = null;
name === null
true
```

函数的类型是 `"function"`：

```javascript
function two() { return 2; }

typeof two
"function"
```

# 练习 - typeof 运算符

**练习 39：** 执行以下代码，判断变量的值：

```javascript
let a = '';
let b = typeof a;
let c = typeof x;
let d = typeof 25;
let e = typeof null;
let f = typeof NaN;
let g = typeof (NaN);
let h = typeof;
let i = '' + 1;
let j = typeof i;
```

# 从用户请求

在我刚开始编程时，主要通过 `prompt` 语句获取数据。我记得自己无法使用互联网，心中有一个问题：如何从用户那里获取？最终，我不得不去寻找答案。我发现两种从用户获取的方法是：

1. 提示窗口
2. HTML5 表单

# 提示窗口

你可以使用 `prompt` 语句创建一个文本框并从用户获取数据：

```javascript
let value = prompt( 'Enter number' );
```

一旦执行此表达式，屏幕上会出现一个窗口，显示 'Enter number' 消息、一个输入框和两个按钮：确定和取消。如果按下取消按钮，`prompt` 函数在代码中返回 `null`。如果按下确定按钮，`prompt` 函数返回用户在输入框中输入的文本。如果输入框为空，按下确定后的返回值变为空字符串（`""`）。假设用户输入了值 25。由于 `prompt` 函数返回一个字符串，此值作为字符串可用：

```
> console.log( value, typeof value);
"25" string
```

# HTML5 表单

本节仅作为介绍如何使用 JavaScript 从 HTML 页面提取数据。我们的目标不是深入理解，而是展示可能性，以便你知道 JavaScript 能做什么。在 Google Chrome 浏览器中打开一个新标签页，并打开开发者控制台。运行以下代码：

```javascript
document.body.innerHTML = `
Age: <input type="text" name="age" class="js-age">
<input type="checkbox" class="js-accept-toc" id="accept-toc">
<label for="accept-toc">Accept the terms and conditions</label>
`;
```

运行此代码后，你正在查看的网站内容被替换为一个文本框和一个复选框。别担心，更改仅在你的浏览器中生效，其他人无法从其他计算机看到这些更改。你可以从浏览器修改文本框和复选框的值。让我们学习如何使用 JavaScript 访问这些值。

我们可以按以下方式提取 Age 字段的内容：

```javascript
var var functionScoped = 'Sun';
let x = 1;
(function outer() {
    var functionScoped = 'Moon';
    (function inner() {
        console.log( '----Function----' );
        console.log( 'x: ', x );
        console.log( 'functionScoped: ', functionScoped );
    })();
})();
```

程序执行后，控制台输出以下内容：

```
----Function----
x: 1
functionScoped: Moon
```

无论变量 x 是使用 `let`、`var` 还是 `const` 声明，都没有关系。我们甚至可以省略表示作用域的关键字，因为无论哪种方式，x 都是在全局作用域中创建的，因此，它将成为全局变量。因此，x 的值在代码中处处可见，所以在 `inner` 函数中，我们可以将其值打印到控制台。

在 `inner` 函数内部，我们可以访问 `outer` 函数的所有变量，无论它们是使用 `var`、`let` 还是 `const` 声明，还是来自外部。

在 `inner` 和 `outer` 函数中，我们都可以访问*在外部函数创建的同一作用域中*创建的变量。在这种特定情况下，是全局作用域。

然而，上述解释并不完整。根据到为止的解释，在 `inner` 和 `outer` 中，我们都可以访问两个 `functionScoped` 变量。一个的值是 'Moon'，另一个的值是 'Sun'。但实际上，我们只能访问其中一个变量。


content]
如果我们从 `inner` 作用域向外移动，对于给定的名称，我们只能访问最近的变量。对于 `functionScoped`，这个变量在外层作用域中。因此，外层作用域中的 `functionScoped` 变量遮蔽了全局的 `functionScoped` 变量。

换句话说，'Moon' 遮蔽了 'Sun'，从 `inner` 和 `outer` 作用域的角度来看，这给你一个全食。这就是为什么在 `inner` 作用域的 `console.log` 语句中我们只能看到 'Moon'。

根据此解释，你可以了解函数的词法作用域是什么。词法作用域允许你访问：

- 给定函数内的所有变量，
- 包含我们正在检查的作用域的函数中的所有变量（递归地），
- 如果在词法作用域中有两个同名变量，那么定义在最靠近我们正在检查的作用域的变量会屏蔽所有在此作用域之外的同名变量。

同样的解释适用于块作用域：

```javascript
let blockScoped = 'Sun';
let x = 1;
{
    let blockScoped = 'Moon';
    {
        console.log( '----Block----' );
        console.log( 'x: ', x );
        console.log( 'blockScoped: ', blockScoped );
    }
}
```

# 更多运算符

我们很快就要编写条件和循环了。在这两种控制结构中，有几个运算符会很方便：

- `+=`、`-=`、`*=`、`/=`、`%=` 等等是给变量增加一个值的简写形式。`a += 1` 与写 `a = a + 1` 相同。
- `++x` 先将 `x` 的值增加 1，然后返回增加后的值。
- `x++` 先返回 `x` 的原始值，然后将其值增加 1。
- `--x` 先将 `x` 的值减少 1，然后返回减少后的值。
- `x--` 先返回 `x` 的原始值，然后将其值减少 1。

示例：

```
let a = 1;

a *= 2;             // a = a * 2;
console.log( a );   // 2

a += 1;             // a = a + 1;
console.log( a );   // 3

a %= 2;             // a = a % 2;
console.log( a );   // 1

++a;                // 如果 ++a 不在赋值语句的右侧，
                    // 其效果与写 a = a + 1 相同；
console.log( a );   // 2

a++;                // 如果 a++ 不在赋值语句的右侧，
                    // 其效果与写 a = a + 1 相同；
console.log( a );   // 3

--a;                // 如果 --a 不在赋值语句的右侧，
                    // 其效果与写 a = a - 1 相同；
console.log( a );   // 2

a--;                // 如果 a-- 不在赋值语句的右侧，
                    // 其效果与写 a = a - 1 相同；
console.log( a );   // 1
```

我知道，`++x` 和 `x++` 之间的区别现在对你来说可能没有意义。我认为在大多数情况下，只要你想要编写可读的代码，这甚至不应该有任何区别。

`x++` 和 `++x` 都有一个主要效果和一个副作用。作为主要效果，它们返回一个值。是 `x`，还是 `x + 1`，取决于你是将 `++` 写在 `x` 之后还是之前。

```
let a, aplusplus, plusplusa;

a = 1;
aplusplus = a++;
console.log( "a: ", a, "aplusplus: ", aplusplus );
// a:  2 aplusplus:  1

a = 1;
plusplusa = ++a;
console.log( "a: ", a, "plusplusa: ", plusplusa );
// a:  2 plusplusa:  2
```

`a++` 表达式首先返回 `a` 的原始值。这个原始值存储在 `aplusplus` 变量中。然后，作为副作用，该表达式将 `a` 的值增加 1。

`++a` 表达式首先执行其副作用，将 `a` 的值增加 1。然后执行 `++a` 的主要效果，即返回增加后的值。这个增加后的值存储在 `plusplusa` 变量中。

相同的代码可以不依赖任何副作用来编写：

```
let a, aplusplus, plusplusa;

a = 1;
aplusplus = a;
a = a + 1;       // 或者: a += 1;
console.log( "a: ", a, "aplusplus: ", aplusplus );
// a:  2 aplusplus:  1

a = 1;
a = a + 1;       // 或者: a += 1;
plusplusa = a;
console.log( "a: ", a, "plusplusa: ", plusplusa );
// a:  2 plusplusa:  2
```

下面的代码说明了这些操作的主要效果和副作用被执行的顺序：

```
y = x++;    // 首先 (主要效果):  y = x;
            // 其次 (副作用): x = x + 1;

y = ++x;    // 首先 (副作用):  x = x + 1;
            // 其次 (主要效果): y = x;

y = x--;    // 首先 (主要效果):  y = x;
            // 其次 (副作用): x = x - 1;

y = --x;    // 首先 (副作用):  x = x - 1;
            // 其次 (主要效果): y = x;
```

让我们看另一个例子：

```
let a = 1;

a *= 2;  // a = a * 2;
console.log( '2: ', a++);
console.log( '3: ', a );
```


一旦你运行`printArray( [1, 3, 5, 1] )`，你会看到结果是屏幕上打印出的 1、3、5、1，每行一个值。

如果你还记得上面 `if` 语句的工作原理，你就已经掌握了理解 `printArray` 函数所需的其他所有知识。我们首先打印索引为 0 的元素，然后从数组创建一个切片。此切片保留数组中除了打印到控制台的那个元素之外的所有元素。我们重复此过程，直到数组中没有元素为止。

不幸的是，这个解决方案不仅不方便，而且资源消耗大。当元素数量在十万左右时，程序会抛出堆栈溢出错误，因为它无法同时处理那么多递归函数调用。因此，我们将学习循环，将上述函数的迭代简化为简单易懂的形式，如下所示：

```
1 for ( let value of arr ) {
2    console.log( value );
3 }
```

不必跳跃太多，你可以这样解释这段代码：取出 `arr` 的每个值并打印出来。

我希望这种简化对你来说足够有吸引力，以便继续学习关于选择和迭代的后续章节。

# 深入探讨选择结构：if-else 和 switch

现在，我们可以将学到的知识拼凑起来了。你已经了解了不同的原始类型和复合类型。你知道如何检查这些类型。你掌握了 JavaScript 中的基本函数、算术运算（加法、减法、乘法等）和逻辑运算（真或假）。

只剩下两样东西没有学。

到目前为止，我们只能编写一系列指令来执行计算。在软件开发中，有三种类型的控制结构：

- `顺序结构`：一条接一条地编写指令
- `结构`：执行一组指令，或者执行另一组
- `迭代结构`：执行一组指令有限次或无限次

# if 语句

既然你已经知道如何顺序执行指令，现在该学习选择和迭代了。让我们从选择结构开始：

```
if ( condition ) {
    instruction1;
    instruction2;
    //...
}
```

只有当 `condition` 为真（truthy）时，`if` 分支内的指令才会执行。

注意 `if` 和左括号之间的空格。这个空格表明 `if` 是一个关键字，而不是一个函数。虽然这个空格不是必需的，但我强烈建议你为了可读性而保留它。

```
function printNumber( x ) {
    if ( typeof x === 'number' ) {
        console.log( x + ' is a number.' );
    }
}

> printNumber( 5 )
5 is a number.
undefined
```

第一个值是控制台输出。第二个值是 `printNumber` 函数的返回值。记住，如果一个函数没有指定返回值，它将返回 `undefined`。

如果我们用一个非数字值调用 `printNumber` 函数，它不会打印任何控制台日志，因为 `if` 分支内的指令只有在 `if` 语句中的条件为真时才会执行。

```
> printNumber( '' )
undefined
```

当输入不是数字时，我们什么也不打印，这有点奇怪。你已经知道编写这样一个程序所需的一切了。思考过程如下：

- 如果 `x` 是一个数字，就打印它
- 如果 `x` 不是一个数字，就打印消息 "The input has to be a number."

我们现在知道编写 `printNumber` 函数所需的一切了：

```
function printNumber( x ) {
    if ( typeof x === 'number' ) {
        console.log( x + ' is a number.' );
    }
    if ( typeof x !== 'number' ) {
        console.log( 'The input has to be a number.' );
    }
}
```

这个解决方案的第二个大问题是我们在无缘无故地写太多代码。

这个解决方案的主要问题被称为缺乏抽象。想象一下，有一天有人发现条件 `typeof x === 'number'` 需要修改。如果你忘了修改第二个条件，你的代码就会出现不一致。我们倾向于在不需要思考的时候少思考。因此，我推荐另一种只有一个条件的解决方案：

```
function printNumber( x ) {
    if ( typeof x === 'number' ) {
        console.log( x + ' is a number.' );
    } else {
        console.log( 'The input has to be a number.' );
    }
}
```

注意 `else` 关键字。`else` 分支只有在原始条件不为真时才执行。

我们可以进一步级联这种方法，因为在 `else` 之后，你可以有另一个条件：

```javascript
function logLampColor( state ) {
    if ( state === 1 ) {
        console.log( 'Red' );
    } else if ( state === 2 ) {
        console.log( 'Amber' );
    } else if ( state === 3 ) {
        console.log( 'Green' );
    } else {
        console.log( 'Wrong lamp state' );
    }
}
```

上述代码的优点是你可以像读普通英语一样阅读它。如果状态是 1，就记录红色。否则，如果状态是 2，就记录黄色。以此类推。

if-else if-else 语句的通用形式如下：

```
if ( condition1 ) {
    statements1;
} else if ( condition2 ) {
    statements2;
} else if ( condition3 ) {
    statements3;
} else {
    statements4;
}
statement_after_if_else;
```

可以有超过两个 `else if` 分支。还要注意，`statement_after_if_else;` 会在 `if-else if-else` 结构中的任何分支后立即执行。

代码解释如下：

- 如果 `condition1` 为真，则执行 `statements1`。
- 如果 `condition1` 为假但 `condition2` 为真，则执行 `statements2`。
- 如果 `condition1` 和 `condition2` 都为假但 `condition3` 为真，则执行 `statements3`。
- 如果 `condition1`、`condition2` 和 `condition3` 都为假，则执行 `statements4`。

`else` 分支不是必需的。例如：

```
if ( condition1 ) {
    statement1;
} else if ( condition2 ) {
    statement2;
}
```

当 `if` 语句只有一条语句时，使用花括号不是强制的。例如，以下有效的：

在两种情况下，`countdown` 函数中都有一个退出条件，这不仅是为了验证输入，也是为了终止无限迭代。如果我们不给自己一个退出的方法，就会永远在循环中运行。至少理论上是这样。实际上，堆栈溢出错误会在给定次数的迭代后终止。

一般来说，由于可读性的原因，强烈建议使用花括号。

关于 `if` 语句的常见学者错误：

## 1. 用六行代码代替简单赋值

让我们用一个例子来介绍这个错误。假设我们要求用户输入一个数字。由于用户输入的总是字符串，我们将此字符串转换为数字。然后我们调用一个函数来打印这个值是否大于 100。

```
let input = prompt( 'Enter a number:' );
let num = Number.parseInt( input, 10 );
console.log( isGreaterThanHundred( num ) );
```

**注意**：如果输入不是数字，则 `Number.parseInt` 返回 `NaN`。`NaN` 的值大于 100。

让我们编写 `isGreaterThanHundred` 函数。当 `num` 大于 100 时，其返回值为 `true`。否则，返回值为 `false`。

```
function isGreaterThanHundred( num ) {
    if ( num > 100 ) {
        return true;
    } else {
        return false;
    }
}
```

为了解释方便，让我们创建一个 `returnValue` 变量，并将这个值放在 `if-else` 语句之后：

```javascript
function isGreaterThanHundred( num ) {
    let returnValue;

    if ( num > 100 ) {
        returnValue = true;
    } else {
        returnValue = false;
    }

    return returnValue;
}
```

让我们检查 `returnValue` 的值：

- 当 `num > 100` 为真时，`returnValue` 为 `true`
- 当 `num > 100` 为假时，`returnValue` 为 `false`

换句话说，`returnValue` 无非布尔表达式 `num > 100` 的值：

```javascript
function isGreaterThanHundred( num ) {
    let returnValue;

    returnValue = num > 100;

    return returnValue;
}
```

这两个版本是等效的。显然，我们可以继续简化函数体中的三条语句，写成一行 `return num > 100;`。然而，本节的目的并不是进一步简化函数。关键在于，我们可以简化以下形式的 `if-else` 语句：

```javascript
let value;
if ( condition ) {
    value = true;
} else {
    value = false;
}
```

如果 `condition` 是一个布尔值，上述代码可以仅用一条赋值语句替代：

```javascript
let value = condition;
```

如果 `condition` 不是布尔值，你可以使用 `Boolean` 或双重否定。

## 2. 不必要的 if 嵌套

我们可以进一步级联这种方法，因为在 `else` 之后，你可以有其他条件：现阶段，让我们专注于第一行的退出条件。对于同样的退出条件，使用花括号可能需要三行，而我们只用了一行：

```javascript
function countdown( num ) {
    if ( typeof num !== 'number' || num <= 0 ) {
        return;
    }
    console.log( num );
    countdown( num - 1 );
}

> countdown( 3 )
3
2
1

在函数体的第一行，只要 `num` 不是正数，我们就退出函数。如果 `num` 是正数，我们就打印它的值，并使用 `num - 1` 调用 `countdown` 函数。

## 3. 避免使用花括号导致的错误

如果你正在学习 Python，这段代码可能会让你感到惊讶，因为在 Python 中，缩进可以像 JavaScript 中的花括号一样形成代码块。

以下有效的：

```javascript
function displayMessage( message ) {
    if ( message !== 'string' )
    // 显示消息
}
```

当 `if` 语句只有一条语句时，使用花括号不是强制的。例如，假设你正在编写一个在屏幕上显示：

```javascript
function displayMessage( message ) {
    if ( message !== 'string' )
        return;
}
```

当我们验证输入时，退出条件的典型形式如下：

```javascript
let value;
if ( condition ) {
    statement;
}
```


```javascript
if ( condition ) statement;
```

在这里，很难故意以软件开发人员可能认为新语句属于 `if` 语句主体的方式缩进另一个语句。

## 4. 错误的否定

假设我们有一盏红灯和一盏黄灯。我们使用布尔值来模拟它们的状态：如果灯的值为 `true`，则表示开启；如果灯的值为 `false`，则表示关闭。

任务：编写布尔表达式来模拟以下状态：

1. 红灯和黄灯都亮着。
2. 红灯或黄灯亮着。
3. 红灯和黄灯不是同时亮着。
4. 红灯熄灭，或者黄灯熄灭。
5. 红灯或黄灯亮着，这不成立。
6. 红灯和黄灯都没有亮着。

我们将分别使用变量 `red` 和 `yellow` 代表红灯和黄灯。

### 解决方案：

第 (1) 部分 很简单，因为文本可以直接翻译为 `red && yellow` 的值。如果我们在这个 `if` 语句中使用这个表达式，我们会这样写：

```javascript
if ( red && yellow ) {
    // ...
}
```

第 (2) 部分 描述了 `red || yellow` 条件。注意，或表达式包含了红灯和黄灯都亮着的情况。

为了避免歧义，将或表达式看作输入与输出之间的关系：只要至少有一个输入为真，输出就为真。该表达式可以在 `if` 语句中以以下方式编写：

```javascript
if ( red || yellow ) {
    // ...
}
```

最后四点更困难。只要你不能像反射一样写出条件，你的朋友就是一个叫做 *真值表* 的工具。真值表为你提供每种可能的输入组合所对应的结果。

例如，让我们看看 `red && yellow` 的真值表。我们稍后会用到它。为了使 `red && yellow` 为真，我们需要两个输入都为真。根据这些信息，填写以下真值表的输出：

| red | yellow | red && yellow |
|---|---|---|
| false | false | _____ |
| false | true | _____ |
| true | false | _____ |
| true | true | _____ |

你很快就会看到正确的解决方案。在那之前，让我们构建 `OR` 运算符（JavaScript 中的 `||`）的真值表。`red || yellow` 的值为真，只要两个输入 `red` 或 `yellow` 中至少有一个为真。根据这些信息，填写以下真值表的输出：

| red | yellow | red || yellow |
|---|---|---|
| false | false | ____ |
| false | true | ____ |
| true | false | ____ |
| true | true | ____ |

现在让我们看看解决方案。`and` 关系的真值表只有一行输出为 `true`：只有当两个输入都为真时，输出才为 `true`：

| red | yellow | red && yellow |
|---|---|---|
| false | false | false |
| false | true | false |
| true | false | false |
| true | true | true |

`or` 关系的真值表包含三行为 `true`，因为我们的条件是至少有一个输入为真：

| red | yellow | red || yellow |
|---|---|---|
| false | false | false |
| false | true | true |
| true | false | true |
| true | true | true |

让我们回顾一下这句话：注意，`or` 表达式包含了红灯和黄灯都亮着的情况。在英语中，`or` 这个词通常用于排他性* 的含义。例如，“我们要么吃巧克力冰淇淋，要么吃芒果冰淇淋。”如果人类听到这句话，他们可能会认为必须在两者之间做出选择，甚至不会考虑他们可以同时得到两种口味。在计算机科学中，`||` (`or`) 表达式也涵盖了两个输入都为 `true` 的可能性。

为了完全理解布尔逻辑，我们还需要一个真值表：否定。

# 输入与输出

| 输入 | 输出 |
|-------|--------|
| red | !red |

# 否定

否定很简单。如果输入是 `true`，输出就是 `false`。如果输入是 `false`，输出就是 `true`。

第 (3) 条指出“红色灯和黄色灯不会同时亮起”。由于这个陈述看起来比之前的更难建模，让我们从真值表开始。属于第 (3) 条的表达式在至少有一个输入为 `false` 时为 `true`：

| 输入 | 输出 |
|--------|--------|
| red | yellow | (3) |
| false | false | true |
| false | true | true |
| true | false | true |
| true | true | false |

让我们比较 (3) 和 (1) 的真值表：

| 输入 | (1) | (3) |
|--------|-----|-----|
| red | yellow | red && yellow |
| false | false | false | true |
| false | true | false | true |
| true | false | false | true |
| true | true | true | false |

我们可以得出结论，(3) 是 (1) 的否定：

- 当 (1) 为 `false` 时，(3) 为 `true`
- 当 (1) 为 `true` 时，(3) 为 `false`

**备注：** 让我们回顾一下否定的真值表。输出是反值。这里 (1) 可以视为输入，而 (3) 是输出。如果我们写一些 JavaScript 代码：

```javascript
let firstStatement = red && yellow;
let thirdStatement = !firstStatement;
```

我们将 `firstStatement` 的值代入 `thirdStatement`。

```javascript
let thirdStatement = !(red && yellow);
```

如果我们在这个 `if` 语句中使用这个陈述，我们将得到：

```javascript
if ( !(red && yellow) ) {
    // ...
}
```

第 (4) 条：“红色熄灭，或者黄色熄灭。”让我们先构建布尔表达式：

- `!red`：红色熄灭
- `!yellow`：黄色熄灭
- `!red || !yellow`：红色熄灭或黄色熄灭

在一个 JavaScript if 语句中：

```javascript
if ( !red || !yellow ) {
    // ...
}
```

让我们看看 (4) 的真值表：

| 输入 | 输出 (4) |
|--------|------------|
| red | yellow | !red || !yellow |
| false | false | true |
| false | true | false |
| true | false | true |
| true | true | false |

这个真值表熟悉吗？这就是表达式 (3) 的真值表。这意味着表达式 (3) 和 (4) 是等价的：

- `!(red && yellow)`
- `!red || !yellow`

一般来说，你可以参考德摩根规则：

- `!( A && B )` 变为 `!A || !B`
- `!( A || B )` 变为 `!A && !B`

记住，当你将否定移入或表达式时，`and` 会变为 `or`，而 `or` 变为 `and`。

# 示例

让我们为另一个陈述建模：“红色亮着或黄色熄灭。”

解决方案：

- “红色亮着”在 `red` 为 `true` 时真
- “黄色熄灭”在 `yellow` 为 `false` 时真，即 `!yellow` 为 `true`
- 两个陈述之间有一个 `or`，所以最终结果是 `red || !yellow`。

由于我们还没有建模过这样的陈述，因此值得填写一个真值表。首先，填写输出值：

| 输入 | 输出 |
|---|---|
| red | yellow | red || !yellow |
| false | false | true |
| false | true | false |
| true | false | true |
| true | true | false |

观察第二行，我们知道“`red` 为 false 且 `yellow` 为 true”不是真的：

```
!( !red && yellow )
```

使用德摩根规则：

- `!( A && B )` 变为 `!A || !B`
- `A` 是 `!red`
- `B` 是 `yellow`

代入 `A` 和 `B` 的值：

```javascript
!( !red && yellow ) ---> !!red || !yellow
```

将 `!!red` 替换为 `red`：

```javascript
red || !yellow
```

我们也可以从三个为 `true` 的陈述推导出相同的结果：

- `red` 和 `yellow` 都为 true
- `red` 为 true 且 `yellow` 为 false
- `red` 为 false 且 `yellow` 为 false

以上三个陈述之间是 `OR` 关系：

```javascript
(red && yellow) || (red && !yellow) || (!red && !yellow)
```

注意前两项可以简化：

```javascript
(red && yellow) || (red && !yellow)
```

变为：

```javascript
red && (yellow || !yellow)
```

由于 `(yellow || !yellow)` 普遍为真，表达式变为 `red`。

将 `red` 代入前两项，我们得到：

```javascript
red || (!red && !yellow)
```

这里，再思考一下：

- 如果 `red` 为 `true`，整个表达式为 `true`，无需评估右侧
- 如果 `red` 为 `false`，则评估右侧：`!red && !yellow` 变为 `!false && !yellow`，继变为 `!yellow`

因此，经过简化，我们得到的表达式与之前相同：`red && !yellow`。

你可能会问，这一切与编程有什么关系？为什么我必须读这些细节？这个微小但重要的差异可能是巨大错误的根源。很多初级开发人员无法区分上述陈述之间的差别，“and”和“or”这两个词会被互换。

对于，你可以参考德摩根等式：

- `!(red && yellow)` 是 `red && yellow` 的否定
- `!red || !yellow` 是 `red || yellow` 的否定

这意味着 (3) 和 (4) 是等价的：

- `!(red && yellow)`
- `!red || !yellow`

我们可以得出结论：

- `!(red && yellow)` 如果看真值表的最后一行，我们得到陈述：“红色和黄色都亮起”。
- 如果看真值表的前一行，我们得到陈述：“要么红色熄灭，要么黄色熄灭”。

第 (5) 条：“红色或黄色亮起，不是真的。”

注意，通过说“不是真的”，我们否定了其后。我们需要否定 `red || yellow`：

这是相应的真值表：

| red | yellow | red || yellow |
|---|---|---|
| false | false | false |
| false | true | true |
| true | false | true |
| true | true | true |

当没有灯亮时，条件成功。这正是 (6) 描述的内容：“红色和黄色都不亮。”

使用 JavaScript 表达式：

```javascript
if ( !red && !yellow ) {
    // ...
}
```


仍然有优化的空间。观察这个表达式的真值表。清晰地分析结果为真和结果为假的行。你能看出什么？

| 输入 | 输出 |
|---|---|
| 红 黄 | 红 XOR 黄 |
| false false | false |
| false true | true |
| true false | true |
| true true | false |

- 当输出为真时，输入是 ______。
- 当输出为假时，输入是 ______。

填空。我很快会公布答案，以便你验证自己的思路是否正确。但首先，如果你已经找到了答案，试着填空并构造一个简单的条件，当上述真值表输出为真时该条件成立：

```javascript
if ( ______ ) {
    // ...
}
```

填空答案：注意在第二行和第三行，输入是不同的。因此，当输出为真时，输入是不同的。所以第一个空格的答案是“不同的”。第二个空格应包含一个短语，表示当输入相同时输出为假。

关于第三个空格，条件应描述输入是不同的。一个简单描述此情况的条件是 `red != yellow`。

# 练习：if-else

**练习 44.** 编写一个函数，返回两个数中的最大值。

```javascript
max2( 1, 2 )
// --> 2
max2( 2, 1 )
// --> 2
```

**练习 45.** 使用以下表达式创建一个 1 到 50 之间的随机数：

```javascript
Math.trunc( Math.random() * 50 ) + 1
```

编写一个函数，请求用户输入一个 1 到 50 之间的数字。根据用户输入的值，程序打印以下消息之一：

- “你的猜测太低了。再试一次！”
- “你的猜测太高了。再试一次！”
- “正确结果是 36。”（假设 36 是正确答案）
- “你的猜测应在 1 到 50 之间。再试一次！”
- “格式无效。再试一次！”

提示：`prompt( "问题：" )` 命令会显示其参数，并要求用户在文本框中输入一个值。`prompt` 的返回值是用户输入的字符串。

# switch 语句

对于冗长的 if-else 语句链，有一个简写版本：`switch` 运算符。`switch` 就像一个电话接线员。它会根据变量中存储的正确值，将你转接到相应的代码段。还有一个 `default` 行，表示“你拨打的号码无效”。

```javascript
function logLampColor( state ) {
  switch( state ) {
    case 1:
      console.log( '红' );
      break;
    case 2:
      console.log( '黄' );
      break;
    case 3:
      console.log( '绿' );
      break;
    default:
      console.log( '错误的灯状态' );
  }
}

logLampColor( 1 );
```

尝试运行这段代码示例，摆弄一下它。看看如果移除 `break` 命令会发生什么。看看如果用其他参数调用此函数会发生什么。

现在你对 `switch` 语句有了感觉，让我来解释它。`switch` 内部有一个变量。这个变量可能具有多个值。我们跳转到 `case` 标签，其中 `state` 等于标签值。

然后我们开始执行代码。

如果属于某个标签的代码段末尾没有 `break`，执行将继续到下一行代码。即使现在它位于另一个标签下也没关系。代码只是会穿过标签执行。

这就是为什么在每个属于标签的代码段末尾我们都有一个 `break` 语句。`break` 语句会跳出最近的 `switch` 语句，你的程序将继续在 switch 语句之后执行。

我们有两个理由不在标签后包含 `break` 语句：

- 我们改用 `return` 语句。
- 我们故意落入下一个标签（不推荐）。

示例：

```javascript
function getLampColor( state ) {
    switch( state ) {
        case 0:
        case 1:
            return '红';
        case 2:
            return '黄';
        case 3:
            return '绿';
    }
}

getLampColor( 1 );
```

在此示例中，`case 0` 和 `case 1` 都返回 '红'。

注意，你已经知道另一种不使用 if-else 来返回值的方法：

```javascript
function getLampColor( state ) {
    return state == 1 ? '红' : '绿';
}
```

如果状态为 1，三元运算符返回红色，否则返回绿色。

我们可以在 '绿' 的位置放置另一个三元表达式，以添加更多灯光状态：

```javascript
function getLampColor( state ) {
    return state == 1 ? '红' :
           state == 2 ? '黄' :
           state == 3 ? '绿' :
           '错误';
}
```

有些人不喜欢这种代码编写方式。你可以在网上找到他们关于*三元运算符滥用*有多糟糕的吐槽。我个人不同意他们的观点，但这不重要。如果你认为应该使用它，就使用它。

# 练习：switch

**练习 46.** 使用 `switch` 语句和 `case` 重写以下代码：

```javascript
if ( a == 1 ) {
    console.log( '一' );
} else if ( a == 2 ) {
    console.log( '二' );
} else if ( a == 3 ) {
    console.log( '三' );
}
```

**练习 47.** 使用 `switch` 语句和 `case` 重写以下代码：

```javascript
if ( a > 0 ) {
    console.log( '正数' );
} else if ( a < 0 ) {
    console.log( '负数' );
} else {
    console.log( '零' );
}
```

**练习 48.** 将以下代码转换为使用 `switch` 的等效版本。提示：你可以使用 `if-else` 语句、三元运算符甚至函数。

```javascript
let state = 2;

switch( state ) {
    case 1:
        console.log( '一' );
        break;
    case 2:
    case 3:
        console.log( '二或三' );
    case true:
        console.log( '真' );
    default:
        console.log( '默认' );
}
console.log( '完成' );
```

# 迭代：循环与递归

现在我们了解了 `switch` 是如何工作的，让我们继续学习。

# 递归函数

让我们从一个示例开始。首先，创建一个数组：

```javascript
let numbers = [19, 65, 9, 17];
```

这些数字看起来熟悉？是的，它们是斐波那契数。

**练习：** 运用已知的知识，计算 `numbers` 元素的和。`numbers` 数组包含任意元素。

**解答：** 我们已经学习了如何编写 `if-else` 语句、运算符。问题是，我们还没学习对两个以上的数字求和。因此我们需要一些灵感来解决这个问题。

我们知道空列表的和为 0。我们也知道长度为 1 的列表元素等于唯一的元素。假设我们能以某种方式将 `numbers` 列表的前 `i` 个元素求和，并存储在变量 `S` 中。利用 `S` 的值，我们可以求出列表 `i + 1` 个元素的和：`S + numbers[i]`。

如果我们以某种方式将列表的前 `i` 个元素求和，并得到 `S`，那么列表 `i+1` 个元素的和就是 `S + numbers[i]`。

用表格形式表示：

| 索引 | `numbers[index]` | 旧和 | 新和 |
|---|---|---|---|
| 0 | 19 | 0 | 0 + 19 = 19 |
| 1 | 65 | 19 | 19 + 65 = 84 |
| 2 | 9 | 84 | 84 + 9 = 93 |
| 3 | 17 | 93 | 93 + 17 = 110 |

我们创建了第一个*循环*。循环的每次迭代都有一个索引，范围在 0 到 `numbers.length - 1` 之间。在每次迭代期间，有两个东西变化：

- 索引
- 和

我们需要做的就是在每次迭代中记录索引和的值。通过遍历数组来执行迭代。我们需要知道何时结束迭代。当 `index` 的值达到 `numbers.length` 时，我们就停止迭代。

让我们把这个想法转化为代码。我们将使用一个函数来执行循环迭代。

# 递归

为了简化，我们将采取与最初想法完全相反的方式。最初的想法是，我们取前 `i` 个元素的和，然后将 `i+1` 个元素加到和中。在这里，我们取第一个元素，将其加到列表其余部分的上。这个微小的差异决定了求和是从左向计算，还是从右向计算。这样做的好处是，我们的函数更简洁。

```javascript
function sum( array ) {
    return array.length === 0 ? 0 :
        array[0] + sum( array.slice( 1 ) );
}
```

如果列表为空，则返回零作为和。

如果列表为空，我们取它的第一个元素，将其加到剩余元素的上。例如：

步骤 1. `sum( [19, 65, 9, 17 ] )`。第一个元素是 19。
步骤 2. `19 + sum( [65, 9, 17 ] )`
步骤 3. `19 + 65 + sum( [9, 17 ] )`
步骤 4. `19 + 65 + 9 + sum( [17] )`
步骤 5. `19 + 65 + 9 + 17 + sum( [] )`
步骤 6. `19 + 65 + 9 + 17 + 0`

最后一步之后，总和变为 110。

我们成功地使用函数实现了*迭代*。迭代是一段我们反复运行的代码。尽管我们现在使用的是函数，但在后续阶段，我们将使用循环来实现迭代。

循环就像一首廉价的歌曲。这让我想起了柏林，那里每三个人就有一个声称自己是 DJ。我曾经也有个“DJ”邻居。幸运的是，物业管理部门没有容忍他的行为。我仍然记得他“研究”同一段旋律长达半年之久。一遍又一遍……直到有人报警。

取一小段旋律，重复一百次。你就得到了一首歌。很简单，不是吗？编程也类似：取一段代码，运行很多次。

虽然可以使用函数来实现迭代，但这种方案很少被推荐。在将来，我们将学习如何使用循环编写迭代。这种形式比函数形式更加简洁，更不用说性能上的优势了。

> 使用调用自身的函数来实现的迭代称为*递归*。

为了引入一个帮助函数，我们定义一个 `sumHelper` 函数：

```javascript
function sumHelper( array, index, sum ) {
    if ( index === array.length ) {
        return sum;
    }
    return sumHelper( array, index + 1, sum + array[index] );
}
```

现在我们可以调用它：

```javascript
function sum( array ) {
    return sumHelper( array, 0, 0 );
}
```


```markdown
# 练习：While 循环

**练习 51.** 让我们回顾一下之前练习中的 `map` 结构：

```javascript
let arr = [1, 5, 3, 1];

let map = {};

map[ arr[0] ] = true;
map[ arr[1] ] = true;
map[ arr[2] ] = true;
map[ arr[3] ] = true;

console.table( map );
```

编写一个函数，从任意数组构建类似的 `map` 结构。请使用 `while` 循环！

**练习 52.** 回顾一下十六进制到十进制/二进制的转换器：

```javascript
/**
 *  Prints hexadecimalValue in base 2 and base 10.
 *
 *  @param  string    hexadecimal number in correct format
 *  @return undefined
 */
function convert( hexadecimalValue ) {
    let baseTenValue = Number.parseInt( hexadecimalValue, 16 );
    console.log(
        hexadecimalValue + ' in base 10:',
        baseTenValue,
        '\n' + hexadecimalValue + ' in base  2:',
        baseTenValue.toString( 2 )
    );
}

convert( 'ACE' )
// --> ACE in base 10: 2766
//     ACE in base  2: 101011001110
```

重写数字进制转换器函数，使其可以接受一个任意的进制作为 `convert` 函数的第二个参数。确保程序只接受大于或等于 2 的整数。例如：

# do-while 循环

我们还有几个循环要讲。`do-while` 循环至少会执行一次循环体，并在结束前检查条件。

```javascript
let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {
    if ( values.length == 0 ) return 0;
    let sum = 0;
    let i = 0;
    do {
        sum += values[i];
        i += 1;
    } while ( i < values.length );
    console.log( 'The loop was executed ' + i + 'times' );
    return sum;
}

sumArray( numbers );
```

注意函数的第一行。我们必须在到达 `do-while` 循环之前退出 `sumArray` 函数，以防数组为空。否则，代码的运行方式与 `while` 循环完全相同，唯一的区别是再次运行循环的条件位于底部。

我们主要使用 `do-while` 循环进行输入验证。用户输入一个值，然后我们检查其有效性。

让我们使用 `prompt` 函数获取一个值。

`prompt('message')` 会打开一个显示 `message` 的对话框。对话框中出现一个文本框，您可以在其中输入值。按下 OK 按钮后，`prompt` 函数会返回一个字符串。

例如：

```javascript
let name = '';
do {
    name = prompt( 'Enter a name!' );
} while ( name.length == 0 );
```

这就是 `do-while` 循环有意义的地方，因为我们可以确定至少需要输入一次数据。在求和数示例中，使用 `do-while` 循环技术上是行的行的，没有意义，因为简单的 `while` 循环更容易。

# 练习：do-while 循环

**练习 53.** 您可以使用以下代码创建一个 1 到 50 之间的随机数：`Math.trunc( Math.random() * 50 ) + 1`

创建一个函数，该函数生成一个随机数，然后要求用户在 1 到 50 之间输入。(a) 使用 `do-while` 循环 (b) 使用 `while`

# for 循环

现在您将学习另一种适合迭代的 `for` 循环。这个循环将几行代码组合成一行。`for` 循环的执行与 `while` 循环相同：

```javascript
initialization_of_loop_variable;
while ( condition ) {
    statements;
}

for ( initialization_of_loop_variable; condition; increment_loop_variable ) {
    statements;
}
```

`for` 循环将您需要的一切放在一行。您不必将循环体与变量混合在一起。`for` 循环的执行过程如下：

1. `initialization_of_loop_variable`
2. 检查 `condition`。如果条件为假，则退出 `for` 循环
3. 执行循环体中的 `statements`
4. `increment_loop_variable`

使用 `for` 循环重写 `sumArray` 函数。以下是使用 `while` 循环的示例：

```javascript
let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {
    let sum = 0;
    let i = 0;
    while ( i < values.length ) {
        sum += values[i];
        i += 1;
    }
    return sum;
}

sumArray( numbers );
```

在您完成此练习之前，不要继续阅读。将 `while` 循环更改为 `for` 循环。欢迎回来！希望您喜欢这个练习。验证您的解决方案：

```javascript
for ( let i = 0; i < values.length; i += 1 ) {
    sum += values[i];
}
```

此代码应替换

```javascript
let i = 0;
while ( i < values.length ) {
    sum += values[i];
    i += 1;
}
```

注意，在 `for` 循环的初始化部分声明变量。其余代码方式与 `while` 循环相同。让我们进一步简化 `for` 循环：您可以使用 `i++` 代替 `i += 1`：

```javascript
for ( let i = 0; i < values.length; ++i ) {
    sum += values[i];
}
```

在某些编程竞赛中，人们倾向于向下计数而不是向上计数。原因是计算 `values.length` 比检查 `i` 的值是否正花费一些秒：

```javascript
for ( let i = values.length - 1; i >= 0; --i ) {
    sum += values[i];
}
```

顺便说一句，这些自作聪明的人并没有此止步。他们更进一步：

```javascript
for ( let i = values.length; i; sum += values[--i] );
```

很奇怪，不是吗？我们不是从 12 迭代到 0，而是从 13 迭代到 1。只要 `i` 的值保持非零，条件 `i` 就为真。这是计算机对整数的最简单的检查。假设 `i` 为 13。`values[--i]` 被解释为 `values[12]`，因为我们首先减少 `i` 的值，然后将表达式 `--i` 赋值给新的 `i` 值。这是一个特例，如果写成 `i--` 会不正确，因为我们的数组没有索引为 13 的元素。

如果您不理解这种优化技术，请不要担心。当您第十次阅读这篇文章时，您可能会理解它。这是正常的。哦，顺便说一句，我不鼓励使用这种优化。可读性总是胜过这些微小的优势。有时您的代码可以节省几秒，所以不要为秒而烦恼。这就像捡了芝麻丢了西瓜。

另一个避免自作聪明和优化代码的原因是，JavaScript 解释器实际上会为您优化代码。这是一个非常简单直接的优化。您不必自己费心去做。只需坚持使用这个版本的 `for` 循环：

```javascript
for ( let i = 0; i < values.length; ++i ) {
    sum += values[i];
}
```

# 练习：for 循环

练习 54 和 55。回顾 `while` 循环部分的两个练习。使用 `for` 循环重写您的解决方案。

# for..in 和 for..of 循环

我们的下一个简化是 `for..in` 循环。如果一个循环可以为我们处理迭代，为什么还要费心迭代一个 `i` 变量呢？

```javascript
let values = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];
let sum = 0;

for ( let i in values ) {
    sum += values[i];
}

console.log( sum );
```

`for..in` 循环按升序枚举 `values` 数组的所有可用索引，从 0 到 12。我还有另一个简化要告诉您：“如果我们能够枚举数组的值，为什么还要费心使用一个变量呢？”在 ES6 中，有一个叫做 `for..of` 的循环，它正是做的。

```javascript
let values = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];
let sum = 0;

for ( let value of values ) {
    sum += value;
}

console.log( sum );
```

就是这样。回到编辑器，`for..in` 和 `for..of` 结构。它的运行方式完全相同。我们快完成了。只剩两个结构。我们可以在循环中使用 `break` 或 `continue`：

- `break` 退出它所在的循环，并执行下一条命令
- `continue` 从循环体中跳出，回到循环条件处

**示例：** 求和数组每个元素：

```javascript
let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {
    let sum = 0;
    for ( let i in values ) {
        if ( i % 2 == 0 ) continue;
        sum += values[i];
    }
    return sum;
}

sumArray( numbers );
```

这个例子是人为的，因为我们可以在简单的 `for` 循环中编写 `i += 2` 来跳转到下一个值。所以我们测试 `continue` 只是举例。当 `i` 为偶数时，`continue` 将执行移到下一次迭代。注意，如果语句跟着 `if` 或循环，我们不必只使用大括号：

```javascript
if ( i % 2 == 0 ) continue;
```

与以下代码相同：

```javascript
if ( i % 2 == 0 ) {
    continue;
}
```

我们仍然倾向于使用大括号，因为格式可能许多错误。例如，有些人可能认为 `statement1` 和 `statement2` 属于循环体。

```javascript
while ( condition )
    statement1;
    statement2;
```

错误的！如果我们添加大括号，我们将得到以下代码：

```javascript
while ( condition ) {
    statement1;
}
statement2;
```

这对熟悉 Python 的人可能会困惑。`statement2` 位于循环之外。你已经知道 `break` 语句长什么样了，因为学习 `switch` 语句时接触过它。在循环中，它的作用相同。假设我们在求和超过 100 时跳出循环：

```javascript
let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {
    let sum = 0;
    for ( let i in values ) {
        sum += values[i];
        if ( sum >= 100 ) {
            break;
        }
    }
    return sum;
}

sumArray( numbers );
```

我特意把 `break` 放在花括号里，是为了向你展示 `break` 是跳出 `switch` 语句和循环，而不是 `if` 语句。当 `break` 执行时，控制权会交给循环后的语句：`return sum`。

在这个特定例子中，我们甚至不需要 `break`，因为我们可以直接返回总和，而不是跳出循环：

```javascript
let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {
    let sum = 0;
    for ( let i in values ) {
        sum += values[i];
        if ( sum >= 100 ) return sum;
    }
    return sum;
}

sumArray( numbers );
```

从技术上讲，在这个例子中，我会建议使用更灵活的 `for` 循环：

```javascript
let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {
    let sum = 0;
    for ( let i = 0; i < values.length && sum <= 100; ++i ) {
        sum += values[i];
    }
    return sum;
}

sumArray( numbers );
```

# 练习：for..in 和 for..of

**练习 56：** 创建一个函数，该函数接受一个数字数组，并返回数组中的最大数。示例：

```javascript
max([19, 65, 9, 17, -99])
// --> 65

max([])
// --> null
```

# 展开运算符、解构和剩余参数

展开运算符、解构和剩余参数是三个相关的特性。让我们通过一个例子来介绍它们。首先，通过一个例子介绍展开运算符：

# 展开运算符

我们将通过示例来介绍展开运算符。示例和练习的区别在于，你并没有解决这些示例所需的全部知识，尽管你可以尝试解决这些示例，但请务必阅读参考答案。

**示例 1：** 假设你有两个装着水果的篮子：

```javascript
const Basket1 = [ 'Apple', 'Pear', 'Strawberry' ];
const Basket2 = [ 'Banana', 'Peach' ];
```

创建一个新数组，包含 Basket1 或 Basket2 中的所有水果。

**解决方案：** 首先，我们必须创建一个新数组。

```javascript
const MergedBasket = [];
```
```


```
for ( let fruit of Basket1 ) {
    MergedBasket.push( fruit );
}
for ( let fruit of Basket2 ) {
    MergedBasket.push( fruit );
}
```

我们可以检查结果是否正确：

```
> console.log( MergedBasket )
(5) ["Apple", "Pear", "Strawberry", "Banana", "Peach"]
```

为了一次简单的合并写这么多代码不太方便。让我们介绍能帮你更快解决相同问题的展开运算符。

> 展开运算符将数组的参数展开为以逗号分隔的值。

对于对于值 `v1`、`v2`、`v3`，展开运算符的工作方式如下：`... [v1, v2, v3]` 变成 `v1`, `v2`, `v3`。

乍一看，你可能对这个结构有些疑虑，我完全理解原因。毕竟，在控制台中写 `... [1,2,3]` 会给你一个语法错误：

```
> ... [1, 2, 3]
Uncaught SyntaxError: Unexpected number
```

这意味着你不能在代码中的任何地方都写逗号分隔的值。让我们看一些可能发生逗号分隔值的基本用例：

- 数组元素：`[1, 2, 3]`,

- 函数或方法的参数列表：`Math.max(1, 2)`

```
> [...[1, 2, 3]]
[1, 2, 3]
```

我们得到了一个包含相同元素的扁平数组。如果我们更深入地研究这些行，你会看到这个操作带来了一些副作用：

```
const numbers = [1, 2, 3];
const spreadNumbers = [...numbers];

spreadNumbers[0] = 5;

console.log( spreadNumbers );  // Printed value: [5, 2, 3]
```

`numbers[0]` 的值是多少？

```
> numbers
(3) [1, 2, 3]
```

如你所见，`numbers[0]` 是 1，因为 `spreadNumbers` 与 `numbers` 不是同一个数组。在 `numbers` 的元素被复制到 `spreadNumbers` 之后，它们的元素是相同的。然而，这两个数组是不同的。我们成功使用展开运算符制作了原数组的浅拷贝。

制作浅拷贝是一种克隆。克隆在计算机科学中是一个复杂的操作，超出了本入门主题的范围。在后面的章节中，我们将重新探讨这个结构。

> 展开运算符可用于制作数组的浅拷贝。在 `B = [...A]` 中，`B` 是 `A` 的浅拷贝。

### 示例 1 的第二种解决方案：

既然我们知道了展开运算符和浅拷贝的工作原理，让我们回顾一下，我们的任务可以转化为将两个篮子的内容复制到第三个篮子。要解决这个练习，我们需要将 `Basket1` 和 `Basket2` 的浅拷贝放入同一个数组：

```
const Basket1 = [ 'Apple', 'Pear', 'Strawberry' ];
const Basket2 = [ 'Banana', 'Peach' ];

const MergedBasket = [ ...Basket1, ...Basket2 ];
```

不需要 `for...of` 循环。展开运算符解决了一切。

# 练习：展开运算符

**练习 57.** 填空，使得执行此代码的结果为 `1 7 3`。在你的解决方案中不要使用任何数字。

```
let A = [1, 2, 3];
let B = _____;
B[0] += 1;
console.log(
    A[0],
    B[0] + B[1] + B[2],
    B.length
);
```

# 解构数组

现在你知道了如何展开数组成员，让我们学习 `...` 运算符的另一个作用。

假设数组 `A` 给定为 `[1, 2, 3, 4, 5]`。我们如何逐一检索这个数组的第一、第二和第三个元素？

你已经知道可以使用方括号表示法来检索这些值：

```
const first = A[0],
      second = A[1],
      third = A[2];
```

这写起来很费劲。幸运的是，ES6 引入了一种更短的定义这些变量的方式：解构赋值。

```
const [first, second, third] = A;
```

这两种表示法是等价的。在两种情况下，`first`、`second` 和 `third` 分别从 `A` 获取第一、第二和第三个值。这三个赋值并行执行，如下所示：

```
const [first, second, third] = A;

const [first, second, third] = [1, 2, 3, 4, 5];

const first = 1, second = 2, third = 3; // 4 and 5 are thrown away.
```

解构之所以被称为解构，是因为它获取右侧的结构，并对其进行解构，以便可以将值分配给左侧的结构。

**问题 1：** 如果我们只对数组的第三个和第五个元素感兴趣，会发生什么？

**答案 1：** 我们可以使用逗号来表示需要丢弃一个值。在左侧的 `third` 变量前面放置两个逗号，描述了一个解构赋值，其中前两个值被丢弃。同样，我们可以在第三个和第五个元素之间放置两个逗号，以确保第四个值被丢弃。

```
const [,third,,fifth] = [1, 2, 3, 4, 5]

> third
3
> fifth
5
```

**问题 2：** 如果我们省略上述解构赋值前面的 `const` 关键字会发生什么？

**答案 2：** 如果 `third` 和 `fifth` 之前没有定义，解构赋值仍然有效。这种形式的缺点是 `third` 和 `fifth` 会变成全局变量。

```
[,third,,fifth] = [1, 2, 3, 4, 5]
```

（此处原文逻辑为：如果 `third` 和 `fifth` 之前没有定义，解构赋值仍然有效。这种形式的缺点是 `third` 和 `fifth` 会变成全局变量。如果你在块作用域或函数作用域中声明，这些变量不会成为全局。）

```
const third, fifth;
[,third,,fifth] = [1, 2, 3, 4, 5]
```

如果只声明了其中一个变量，使用 `const` 会抛出错误。

```
let third;

> let [,third,,] = [1, 2, 3]
Uncaught SyntaxError: Identifier 'third' has already declared
```

如果 `third` 之前被赋值，它的值会被重新赋值：

# 剩余参数

在第六个问题之前，让我们先定义列表的 `头部`和`尾部`。在计算机科学中，`头部` 是列表的第一个元素，`尾部` 是包含除第一个元素外所有元素的列表，保持与原始列表相同的顺序。在 JavaScript 中，我们将列表表示为数组 `A`。

**问题 6：** 在解构赋值的左侧使用展开运算符吗？

**答案 6：** 不能。在左侧，`...` 运算符用于定义剩余参数，因为它不是展开值，而是收集右侧数组的所有值。

```javascript
const [head, ...tail] = [1, 2, 3, 4, 5]

> head
1

> tail
[2, 3, 4, 5]
```

以下赋值是无效的：

```javascript
> [...rest,] = [1, 2, 3, 4, 5]
Uncaught SyntaxError: Rest element must be last
```

如果在到达剩余参数之前，数组的所有元素都已被消耗，那么剩余参数的值将变为 `[]`：

```javascript
[,rest] = [1, 2, 3, 4, 5]

> rest
[]
```

# 函数剩余参数与数组解构

在接下来的示例中，我们将 `...` 运算符用作剩余参数。剩余参数的行为比展开运算符将数组值展开为逗号分隔的值略受约束。这种差异可以通过两个函数来说明：

- `const invalidFunction = function( ...args, lastArgument ) { /* ... }`
- `const validFunction = function( firstArgument, ...args ) { /* ... }`

理论上，这两个函数都接受可变数量的参数。假设我们用参数列表 `1, 2, 3` 调用它们。对于 `invalidFunction`，无法确定参数值。

```javascript
> [...args, lastArgument] = [1, 2, 3]
Uncaught SyntaxError: Rest element must be last element

> const invalidFunction = function( ...args, lastArgument ) {}
Uncaught SyntaxError: Rest parameter must be last formal parameter
```

无论是在解构练习中还是在函数定义中，`...` 都象征着一个剩余参数。剩余参数只能出现在数组的末尾。因此，在函数参数列表中，`...` 剩余参数只能出现在函数参数列表的末尾。违反此规则将抛出 SyntaxError。

对于 `validFunction`，我们很容易确定参数值：

```javascript
let [ firstArgument, ...args ] = [ 1, 2, 3 ]

> firstArgument
1

> args
[2, 3]
```

注意，调用函数是一个解构赋值。解构赋值的左侧是函数定义的参数列表。右侧由调用函数使用的参数列表组成。在解构赋值的左侧，`...` 运算符用于描述一个剩余参数。

**示例：** 编写一个接受可变数量参数的函数。每个参数应该是一个数字。函数的返回值是最大和最小参数值之差。

**解决方案：** 我们将使用剩余参数来描述这个函数。

```javascript
const max = function(...args) {
    // 逻辑实现
}
```

（注：此处保留了原文中的核心逻辑结构）

```
const numbers = [1, 2, 3];
const spreadNumbers = [...numbers];

spreadNumbers[0] = 5;

console.log( spreadNumbers );  // Printed value: [5, 2, 3]
```

`numbers[0]` 的值是多少？

```
> numbers
(3) [1, 2, 3]
```

如你所见，`numbers[0]` 是 1，因为 `spreadNumbers` 与 `numbers` 不是同一个数组。在 `numbers` 的元素被复制到 `spreadNumbers` 之后，它们的元素是相同的。然而，这两个数组是不同的。我们成功使用展开运算符制作了原数组的浅拷贝。

# 练习：解构

**练习 58.** 使用一个赋值语句交换两个变量：

```javascript
let swap = 'swap';
let me = 'me';
```

**练习 59.** 在 for 循环内部创建一个构赋值，用于帮助计算第 n 个波那契数。提醒一下：
- `fib(1 ) = 1`
- `fib(2 ) = 1`
- `fib( n ) = fib( n-1 ) + fib( n-2 )`

```javascript
function fib( n ) {
  let fibCurrent = 1;
  let fibLast = 1;
  if ( n <= 2 ) return n;
  for ( let fibIndex = 1; fibIndex < n; ++fibIndex ) {
    // 逻辑
  }
  return fibCurrent;
}
```

**练习 60.** 以下表达式创建了哪些变量及其值？

```javascript
let node = { left : { left: 3, right: 4 }, right: 5 };
let { left, right : val } = node;
```


```markdown
const third = 1, fifth = 2;

[,,third,,fifth] = [1, 2, 3, 4, 5]
```

### 问题 3：如果我把常量放在解构赋值的左侧会发生什么？

**答案 3：** 会抛出一个 JavaScript 错误。解构赋值不能用于过滤。JavaScript 不是 Prolog，在 Prolog 中左侧和右侧是统一的。在解构中，我们所做的只是解构右侧，以便为左侧的值分配一个值。

```javascript
> const [1,,third,,fifth] = [1, 2, 3, 4, 5]

Uncaught SyntaxError: Invalid destructuring assignment target
```

### 问题 4：我能检索一个长度为 5 的数组的第六个元素吗？

**答案 4：** 可以。这个过程类似于检索 `A[5]`。对应的值变为 `undefined`。

```javascript
const [,,,,,sixth] = [1, 2, 3, 4, 5]

> sixth

undefined
```

### 问题 5：我能在解构赋值的右侧使用展开运算符吗？

**答案 5：** 由于数组解构赋值的右侧是一个数组，因此任何有助于构建数组的运算符都可以不受限制地使用：

```javascript
const B = [1, 2, 3];

const [first, second,, fifth] = [...B, 4, 5]
```

```html
<!doctype html>
<html lang="en">
<head>
    <title>问候</title>
</head>
<body>
    <form>
        <input type="text"
               class="tf-large js-name"
               placeholder="姓名">
        <button class="btn-large js-hello">问候</button>
    </form>
    <script src="js/form.js"></script>
</body>
</html>
```

如果你操作正确并保存了所有文件，在浏览器中打开 `greeting.html` 文件后，一旦点击“问候”按钮，姓名就不会消失。

> 请注意，将 JavaScript 代码插入 HTML 文档还有其他方式。我强烈建议坚持使用上述方法，但为求完整，你可以自由阅读[本文](https://www.w3schools.com/js/js_whereto.asp)^31。

JavaScript 在浏览器中使用 JavaScript 解释器执行。JavaScript 是一种解释型语言，这意味着它直接在文件中运行 JavaScript，而不会将其编译成中间表示形式。

# 开发者工具

每个浏览器都有开发者工具。为简单起见，本文将使用 Google Chrome，但大多数浏览器都有类似功能。

在浏览器窗口中的网站任意位置右键单击，然后从上下文菜单中选择 `检查`。你将发现自己进入开发者工具。找到 `Console` 标签页。假设你已经点击了按钮，你可以在此找到以下内容：

```
button pressed
>
```

你可以在 `>` 提示符后输入任何 JavaScript 表达式来执行它：

```
button pressed
> 2+2
4

> helloButton
    <button class="btn-large js-hello">Greet</button>
```

`helloButton` 变量存储了一个 DOM 节点，在 JavaScript 中完全可以访问。

# 向用户致意

让我们使用控制台获取在文本框中输入的姓名

```
> document.querySelector( '.js-name' )
    <input type="text" class="large-text js-name" placeholder="name">
> document.querySelector( '.js-name' ).value
    Zsolt
```

我们需要获取文本框的值并在警告框中显示问候语，而不是进行控制台日志输出：

```javascript
function helloListener( event ) {
    event.preventDefault();
    const name = document.querySelector( '.js-name' ).value;
    alert( '你好, ' + name + '!' );
}
const helloButton = document.querySelector( '.js-hello' );
helloButton.addEventListener( 'click', helloListener );
```

字符串上的 `+` 运算符用于连接字符串。`alert` 函数会创建一个警告框。如果你测试这段代码，你会看到一切正常。

# 样式

我们知道：
- 提供网站结构信息的静态标记在 HTML 文件中，
- 动态功能在 JavaScript 文件中。

许多人认为页面的外观和感觉也在 HTML 文件中定义。这种做法是错误的。样式与 HTML 是分离的。
我们在 CSS（层叠样式表）文件中描述样式。

```css
.tf-large {
    font-size: 1.5rem;
    padding: 1rem;
}
.btn-large {
    font-size: 1.5rem;
    padding: 1rem;
    font-weight: bold;
}
```

与 JavaScript 类似，我们需要从 HTML 文档中引用 CSS 文件。我们在 `head` 中使用 `<link>` 标签来完成：

```html
<!doctype html>
<html lang="en">
  <head>
    <title>问候</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <form>
      <input type="text"
             class="large-text js-name"
             placeholder="姓名">
      <button class="btn-large js-hello">问候</button>
    </form>
    <script src="js/form.js"></script>
  </body>
</html>
```

如果你重新加载页面，你可以在屏幕上看到变化。将样式插入 HTML 文档还有其他方式，但请坚持使用外部文件以便分离。HTML 应包含标记，CSS 应包含样式。如果你需要更多关于 CSS 的基础信息，请查看 w3.com。

# HTML 类：关注点

回顾按钮 `<button class="btn-large js-hello">Greet</button>`。你可以看到两个类 `btn-large` 和 `js-hello`。第一个类仅用于样式，第二个类用于 JavaScript。

这种做法强迫你以这种方式编写代码，将样式和功能分开。当多人协作同一个代码库时，这种分离会带来回报。负责样式的人添加、删除或重命名类，而不会影响功能。类应用于功能，常规类应用于样式。

# 为什么不使用 ID？

你可能从之前的工作知道，可以使用 ID 属性引用 DOM 节点：

```html
<div id="intro">这是一介绍</div>
```

如果 DOM 中上述节点，你可以使用以下方式引用它：

```javascript
document.getElementById( 'intro' )
```

ID 属性在整个文档中是唯一的。如果你违反此规则，你会得到 HTML 错误。在大型网站和应用程序中，大多数开发人员不知道他们的标记出现在什么文中。如果你使用了 ID 属性，可能其他处也使用了相同的名称。由于两个 DOM 节点不能拥有相同的 ID，因此在大多数情况下不建议使用 ID 属性。

企业主让我尝试他的插件，因为对他不起作用。当我检查了浏览器的工具，发现标记中有重复的 ID。他包含了插件，一次用于台式电脑，一次用于移动设备。不幸的是，他只是用 CSS 样式（`display: none`）隐藏了它。另一个版本完全相同的 ID：

```html
<div id="affiliate-plugin" class="desktop">
    <!-- 内容放在这里 -->
</div>
<div id="affiliate-plugin" class="mobile hidden">
    <!-- 内容放在这里 -->
</div>
```

由于重复 ID 属性，上述标记是错误的。缺乏基础知识而浪费了数小时。下次遇到类似情况时，你可以节省这些时间。

# 如何处理多个 JavaScript 和 CSS 文件？

在大型项目中，不建议将所有 JavaScript 代码放在一个文件中。因此我们经常有数百甚至千个 JavaScript 和 CSS 文件。也不建议将所有这些文件放在 HTML 标记中，因为枚举数百个文件既方便也不高效。如果你以错误的顺序包含 JavaScript 文件，可能遇到 JavaScript 错误。

对于大型项目，请使用 `Webpack` 和 `npm`（Node 包管理器）将文件捆成一个文件，然后包含在标记中。

你可以在我的文章³³ 中了解更多关于 `npm` 模块和 `Webpack` 的信息。目前阶段，其语法对你来说可能过于高级。如果你注册本文底部的 ES6 微型培训，你将理解一切。

在大型项目中，我强烈建议你学习并使用 `SASS`。`SASS` 不仅丰富你的 CSS 语法，还能帮助你更好地组织结构。请查看我的 SitePoint 文章《CSS 架构与可维护 CSS 的支柱》³⁴ 了解此主题。

³³ https://www.zsoltnagy.eu/using-es6-modules-with-webpack/
³⁴ https://www.w3schools.com/html/css.css/

# 第二部分：深入理解 JavaScript 类型

在简要介绍了 JavaScript 之后，我们现在将继续并更详细地探讨不同的 JavaScript 类型。

# 在 JavaScript 中使用字符串

在软件开发中，处理字符串是一个常见问题。我们经常读取、处理和写入文本文件，对系统活动执行日志记录，或分析用户输入。

学习如何进行字符串操作在任何编程语言中都是必不可少的。

让我们首先回顾一下你从 [JavaScript 基础文章](https://www.zsoltnagy.eu/javascript-tutorial-for-absolute-beginners/) 中已经了解的关于字符串的知识。

# 创建 JavaScript 字符串

字符串包含一系列字符。你可以使用单引号（例如 `'ES6 in Practice'`）或双引号（例如 `"ES6 in Practice"`）来创建字符串。

```javascript
let firstString = "Hugo's dog";
secondString = 'Hugo\'s dog';
```

在控制台中，字符串用双引号显示。如前一个示例所示，可以在双引号内使用单引号，也可以在单引号内使用双引号。如果你想在单引号内使用单引号，必须用反斜杠对其进行转义。

`\` 告诉 JavaScript 解释器下一个字符应被视为字面字符，而不是元字符。因此，`\'` 不表示字符串的开始或结束。补充说明：如果你想在字符串中放置一个反斜杠，必须以 `\\` 的形式进行转义。

# 字符串的相等性

当两个字符串相等时，字符串上的 `+` 运算符用于连接字符串。`alert` 函数会创建一个警告框。如果你测试这段代码，你会看到一切正常。

# 字符串的长度

字符串有一个 `length` 属性，包含了字符串中的字符数。例如，空字符串长度为 0：

```
> firstString.length
10

> ''.length
0
```

# 多行字符串

在定义字符串时，我们需要在字符串中插入换行符。解决方案如下：

```
'First line.\nSecond line.\nThird line.'
```

或者，你可以在行尾放置反斜杠使其成为多行：

```
'First line.\
Second line.\
Third line.'
```

# 模板字量

模板字量使用反引号定义：

```javascript
const html = `
    <div>
    </div>
`;
```

请注意，换行符会保留在模板字量中。也可以在模板字量中计算 JavaScript 表达式：

```javascript
const nodeText = 'This is a template';
const parametrizedHtmlTemplate = `
    <div>
        ${nodeText}
    </div>
`;
```

一旦创建，模板字量会立即求值并转换为字符串：

```
> parametrizedHtmlTemplate
"
    <div>
        This is a template
    </div>
"
```

请注意，在开发者工具控制台中，你可能会看到键盘上 ENTER 键对应的符号来表示实际的换行，而不是直接显示换行。

模板标签函数被认为是高级主题：

```javascript
(content) => `Hello, ${content}!`
```

# 修剪字符串

修剪是移除字符串第一个空白字符之前和最后一个空白字符之后的空白字符的过程。我们经常在处理模板或用户输入时移除这些不需要的空白字符。

`trim` 字符串方法执行修剪操作：

```javascript
const template = `
<div>First line</div>
<div>Second line</div>
`;
```

控制台：

```
> template
"
<div>First line</div>
<div>Second line</div>
"

> template.trim()
"<div>First line</div>
<div>Second line</div>"
```

# 访问字符串内部的字符

同样用于数组的括号表示法，可以用于访问字符串中的任意字符：
```



```
> let digits = '0123456789';
> digits[4]
"4"
```

除了使用索引，你也可以使用 `charAt` 方法：

```
> digits.charAt(4)
"4"
```

与数组相反，设置字符串内部的字符为新值是无效的。字符串的索引是严格只读的：

```
> digits[4] = 'X';
> digits
"0123456789"
```

将 `digits[4]` 设置为 `'X'` 的操作静默失败了。

通常，字符串被认为是不可变的。这意味着我们无法更改它们的内容。当在字符串末尾添加一个字符时，会创建一个新字符串。

要遍历字符串，可以使用所有 JavaScript 控制结构：`for`、`while`、`do...while`、`for...in`、`for...of`：

```javascript
let sum1 = 0;
for ( let i = 0; i < digits.length; ++i ) {
    sum1 += digits[i];
}

let sum2 = 0;
for ( let i in digits ) {
    sum2 += digits[i];
}

let sum3 = 0;
for ( let digit of digits ) {
    sum3 += digit;
}
```

# 查找子字符串在字符串中的索引

`indexOf` 和 `lastIndexOf` 字符串方法分别返回子字符串在字符串中第一次和最后一次出现的索引。

```
> let sequence = '1,2,3,4,5';

> sequence.indexOf( ',' )
1

> sequence.lastIndexOf( ',' )
7

> sequence.indexOf( ',3' )
3
```

当 `indexOf` 的参数是一个长度大于 1 的字符串时，返回值是第一个字符的位置。

此时，我们假设你没有使用长 Unicode 字符。一旦你知道会使用这些字符，请查阅我的文章 [Strings and Template Literals in ES6](http://www.zsoltnagy.eu/strings-and-template-literals-in-es6/) 以了解如何处理它们。

当字符串 `s` 不包含特定子字符串 `s0` 时，`s.indexOf(s0 )` 返回 -1：

```
> sequence.indexOf( 'abc' )
-1
```

假设你想枚举所有匹配项的索引，你可以指定第二个参数，表示从字符串的哪个索引开始搜索：

```
> sequence.indexOf( ',' )
1

> sequence.indexOf( ',', 2 )
3

> sequence.indexOf( ',', 4 )
5

> sequence.indexOf( ',', 6 )
5

> sequence.indexOf( ',', 8 )
-1
```

“字符串 `s` 是否包含子字符串 `s0`？”这个问题在编程问题中经常被问到。我们可以使用 `indexOf` 来实现答案：

```
s.indexOf( s0 ) >= 0
```

由于这行代码读起来不太直观，在 ES6 中，我们可以使用 `includes` 方法来实现同样的目的：

```
s.includes(s0 )
```

有关 ES6 构造的更多细节，请查看我的著作《ES6 in Practice》或[这篇文章](http://www.zsoltnagy.eu/strings-and-template-literals-in-es6/)。

# 分割、切片、连接和拼接字符串

字符串具有属性。一个例子是 `length` 属性。字符串上也定义了一些操作。这些操作称为方法。

在上一节中，我们了解到 `digits[4] = 'X'` 并不会设置 `digits` 字符串内的字符。

在本节结束时，我们将了解更改字符串内部字符所需的一切知识。

# 将字符串分割成子字符串数组

`split` 方法将字符串分割成子字符串数组。`split` 期望一个参数来描述应该如何进行分割。

例如，在编程世界中，我们经常处理 CSV 文件。CSV 代表逗号分隔值。让我们从一行 CSV 创建一个数组：

```
> const line = '19,65,9,17,4,1,2,6';

> line.split( ',' );
["19", "65", "9", "17", "4", "1", "2", "6"]
```

如果我们想创建一个包含字符串中每个字符的数组，可以向 `split` 方法传递一个空字符串：

```
> lines.split( '' );
["1", "9", ",", "6", "5", ",", "9", ",", "1", "7", ",", "4", ",", "1", ",", "2", ",", "6"]
```

由于数组的内容可以被更改，我们可以轻松地更改 `digits` 序列中的数字 4：

如果你想了解更多关于正则表达式的内容，请查看我的 JavaScript 正则 Udemy 视频课程<sup>41</sup>。使用优惠券 JSREGEX 可以最低价格购买。

# 连接字符串

我们可以通过两种方式连接字符串：

- 使用 `+` 运算符，
- 使用 `join` 字符串方法。

你已经在入门文章<sup>42</sup>中看到过 `+` 运算符在字符串上的工作方式：

```javascript
> 'first part' + ' second part'
"first part second part"
```

`join` 方法更有趣一些。它 接收一个字符串数组，并将它们连接成一个字符串。当 `join` 不带任何参数使用时，它通过在字符串之间插入逗号来连接它们。这是因为最常见的字符串写入功能是日志记录和创建 CSV 文件。

```javascript
> ["0", "1", "2", "3", "4", "5", "6", "7", "8", "9"].join()
"0,1,2,3,4,5,6,7,8,9"
```

如果你想在字符串之间插入任何内容，将空字符串作为 `join` 参数：

```javascript
> ["0", "1", "2", "3", "4", "5", "6", "7", "8", "9"].join( '')
"0123456789"
```

也可以指定其他字符：

```javascript
> ["0", "1", "2", "3", "4", "5", "6", "7", "8", "9"].join( ',' )
"0,1,2,3,4,5,6,7,8,9"
```

# 截取

`slice` 方法在简单和编码中常用。它返回其参数指定的子串。记忆 `slice` 参数的最简单方法是：

```javascript
str.slice( firstIndexString )
// 或
str.slice( firstIndexString, indexAfterString )
```

`slice` 参数指定第一个字符的位置。第二个参数是可选的当它缺失时，截取操作会持续到字符串末尾。

`slice` 的两个参数都是可选的：

```javascript
let hexadecimalDigits = '0123456789ABCDEF';

> hexadecimalDigits.slice( 1, 6 )
"23456"

> hexadecimalDigits.slice( 10 )
"ABC"

> hexadecimalDigits.slice( 0, 10 )
"0123456789"
```

与数组类似，`slice` 的参数可以是负数。负值从数组末尾计数：

```javascript
> hexadecimalDigits.slice( -6 )
"ABC"

> hexadecimalDigits.slice( -6, -3 )
"BCD"

> hexadecimalDigits.slice( -6, 13 )
"ABCD"
```

你也可以学习不同语法进行截取的 `substr` 和 `substring` 方法。然而，大部分时间会使用 `slice`，因此在总结中我们将省略这两个方法。`substr` 的工作方式类似 `slice`，但它允许第一个参数大于第二个参数，仍然返回索引之间的子串。`substring` 方法指定第一个字符索引和长度。

# 替换字符串中的字符

`replace` 字符串方法返回一个新字符串，其中第一个参数指定的子串被第二个参数替换：

```javascript
> const numbers = '1 2 3 4';

> numbers.replace( ' ', ',' );
"1,2,3,4"
```

注意，只有第一个空格被替换了。如果你想替换字符串中的所有，可以使用 `split` 和 `join` 方法：

```javascript
> numbers.split( ' ' ).join( ',' )
"1,2,3,4"
```

或者，你也可以将正则表达式作为 `replace` 方法的第一个参数，对其应用全局标志以替换所有匹配项。

```javascript
> numbers.replace( / /g, ',' )
"1,2,3,4"
```

这个解决方案有点高级。如果你想了解更多，请查看我的文章 [JavaScript 中的正则表达式](http://www.zsoltnagy.eu/regular-expressions-in-javascript/)。

你可以替换任意数量的字符，包括零个。在替换空字符串的情况下，第二个参数会被插入到第一个字符之前：

```javascript
> 'help'.replace( '', '--' )
"--help"

> 'help'.replace( new RegExp( '', 'g' ), '--' )
"--h--e--l--p--"

> '1 2 3 4'.replace( '2 3', 'five' )
"1 five 4"
```

# 大小写字母

`toUpperCase` 和 `toLowerCase` 字符串方法分别返回其字符串的大写和小写版本：

```
> 'aBCd'.toLowerCase()
"abcd"

> 'aBCd'.toUpperCase()
"ABCD"
```

# 在 JavaScript 中使用数组

你已经在入门部分学习了 JavaScript 数组的基础知识。现在，我们将通过学习更多数组特性来扩展你的知识。这些特性被描述为数组方法。我们将根据用例对这些特性进行分组：

- 创建和删除数组
- 检查变量是否包含数组
- 将数组转换为字符串：`toString` 方法
- 查找数组元素的位置：`indexOf`、`lastIndexOf` 和 `contains` 方法
- `split` 字符串方法和 `join` 数组方法
- 截取：`slice` 和 `splice` 数组方法
- `map`、`reduce`、`filter`、`find`、`findIndex`
- `every` 和 `some`
- 添加和删除单个元素：`push`、`pop`、`shift`、`unshift`
- 连接数组：`concat`
- 数组排序：`sort`
- 反转数组：`reverse`

# 创建数组

`new` 运算符可用于创建数组。我们可以指定要创建的数组的长度：

```javascript
const A = new Array(5);
// [empty × 5]

A[0]
// undefined

A[999]
// undefined
```

新创建的数组值为 `empty`。当访问边界之外的元素时，得到 `undefined`。数组的内容可以被更改，我们可以轻松地更改 `digits` 序列中的数字 4：

```javascript
let digits = '0123456789';
digits[4] = 'X';
digits
"0123456789"
```

将 `digits[4]` 设置为 `'X'` 的操作静默失败了。

# 数组方法

`toString` 方法工作方式：将数组每个元素转换为字符串。

`toString` 方法应用于数组：将数组每个元素用逗号连接。

```javascript
> [1, 2].toString()
"1,2"

> [1, null, {}, 's'].toString()
"1,,s"
```

# 检查变量是否包含数组

在 ES6 之前，这是一个难题。现在可以使用 `Array.isArray` 方法：

```javascript
const a = [];
const b = { 0: 'a', length: 1 };

Array.isArray(a);  // true
Array.isArray(b);  // false
```

# 分割和连接

可以使用 `split` 方法将字符串分割成子数组。`split` 参数决定如何执行分割：

```javascript
const values = 'first,second,third';

values.split( ','
["first", "second", "third"]
```

`join` 方法将值在一起形成一个字符串，并在它们之间插入分隔符：

```javascript
["first", "second", "third"].join( ';' )
"first;second;third"

[1, 2, 3, 4, 5].join( '-' )
"1-2-3-4-5"

[1, 2, 3, 4, 5].join( ',' )
"1,2,3,4,5"

[1, 2, 3, 4, 5].join()
"1,2,3,4,5"
```

# slice 方法

`slice` 方法复制数组的一个片段。片段由其参数指定。`slice` 的两个参数都是可选的：

`A.slice( begin, end )`

// begin: 切片的第一个索引
// end: 结束索引

我们来看一些例子：

```javascript
const arr = ['a', 'b', 'c', 'd', 'e'];

arr.slice( 1, 3 );
// returns: ["b", "c"] (索引 1 和 2)

arr.slice( 1 );
// returns: ["b", "c", "d", "e"] (从索引 1 开始)

arr.slice( 5 );
// returns: [] (索引 5 或以上没有元素)

arr.slice( 2, 2 );
// returns: [] (第二个参数不大于第一个参数，这意味着一个空的切片)

arr.slice();
// returns: ["a", "b", "c", "d", "e"]
```

你可能会问为什么 `slice` 可以接受零个参数。答案在于浅拷贝的本质：

```javascript
const arr = ['a', 'b', 'c', 'd', 'e'];

const shallowClone = arr.slice();

shallowClone[1] = 'X';

console.log( shallowClone );
// returns: ["a", "X", "c", "d", "e"]

console.log( arr );
// returns: ["a", "b", "c", "d", "e"]
```

浅拷贝创建一个新数组，其元素具有相同的值但属于不同的引用。在我的技术面试中，我有时会看到以下错误的解决方案：

```javascript
const A = ['a', 'b', 'c', 'd', 'e'];
const B = A;
B[1] = 'X';
console.log( A );
// returns: ["a", "X", "c", "d", "e"]
```

记住，`A` 和 `B` 是指向完全相同数组的引用。你可以通过 `A` 或 `B` 访问相同的值。一些候选人应该写 `B = A.slice()` 而不是 `B = A`。



你可能会问，为什么我们不能直接将`浅拷贝`操作称为`克隆`或`复制`？答案在于引用类型是如何被处理的。数组和对象包含引用。在浅拷贝期间，只复制了这些引用：

```
const A = [{value: 1}, {value: 2}];
const B = A.slice();
B[0] = {value: 'X'};
B[1].value = 'Y';

console.log( B )
// returns: [{value: 'X'}, {value: 'Y'}]

console.log( A )
// returns: [{value: '1'}, {value: 'Y'}]
```

在克隆过程中，我们期望保持 `A` 的内容不变。然而，`slice` 只执行浅拷贝，即仅在顶层进行克隆。因此，`B` 是用 `A` 中没有的新引用构建的，但这些引用指向相同的对象 `{value: 1}` 和 `{value: 2}`。只要你将引用重定向到新对象（如 `{value: 'X'}`），浅拷贝就不会有问题。但是，一旦你想访问这些引用内部的内容，你就会看到实际的对象内容在 `A` 和 `B` 之间是共享的。

我在一篇文章中详细介绍了浅拷贝和深拷贝：[JavaScript 中的对象克隆](http://www.zsoltnagy.eu/cloning-objects-in-javascript/)。

# splice 方法

`splice` 方法用于就地操作数组的内容。你可以使用 `splice` 添加、删除或修改元素。

`splice` 数组扩展接受可变数量的参数：

`A.splice( start, deleteCount, ...newItems )`

- `start`: 变更发生的索引。
- `deleteCount`: 从索引 `start` 开始要删除的元素数量。如果省略此参数，则从 `start` 开始的所有元素都将被删除。
- `...newItems`: 要在数组中 `start` 位置添加的可变数量的新元素。

许多 JavaScript 集成开发环境会在你忘记参数时提供帮助。

**返回值**：一个包含被删除元素的数组。

**副作用**：原始数组被修改。元素从数组中被删除和/或被添加到数组中。

### 示例 1：删除从索引 2 开始的所有元素：

```
const arr = ['a', 'b', 'c', 'd', 'e'];
arr.splice( 2 ); // returns: ["c", "d", "e"]
console.log( arr )
// prints: [ 'a', 'b' ]
```

### 示例 2：删除数组的第三个和第四个元素：

```javascript
const arr = ['a', 'b', 'c', 'd', 'e'];
arr.splice( 2, 2 ); // returns: ["c", "d"]
console.log( arr )
// prints: [ 'a', 'b', 'e' ]
```

### 示例 3：在数组的第三个元素后插入元素 'X' 和 'Y'：

```javascript
const arr = ['a', 'b', 'c', 'd', 'e'];
arr.splice( 3, 0, 'X', 'Y' ); // returns: []
console.log( arr )
// prints: ["a", "b", "c", "X", "Y", "d", "e"]
```

### 示例 4：用 'B', 'C', 'D' 替换数组的第二个、第三个和第四个元素：

```javascript
const arr = ['a', 'b', 'c', 'd', 'e'];
arr.splice( 1, 3, 'B', 'C', 'D' ); // returns: ["b", "c", "d"]
console.log( arr )
// prints: ["a", "B", "C", "D", "e"]
```

### 示例 5：使用展开运算符和解构赋值解决示例 1-4，而不改变原始数组。为每个解决方案创建一个不同的解构赋值：

```javascript
const arr = ['a', 'b', 'c', 'd', 'e'];

// 1. 删除从索引 `2` 开始的所有元素
const [a1, b1] = arr;
const solution1 = [a1, b1];

// 2. 删除数组的第三个和第四个元素
const [a2, b2,,e2] = arr;
const solution2 = [a2, b2, e2];

// 3. 在数组的第三个元素后插入 'X' 和 'Y'
const [a3, b3, c3, ...rest] = arr;
const solution3 = [a3, b3, c3, 'X', 'Y', ...rest];

// 4. 用 `'B'`, `'C'`, `'D'` 替换数组的第二个、第三个和第四个元素
const [a4,,,e4] = arr;
const solution4 = [a4, 'B', 'C', 'D', e4];
```

当数组很大且你可能需要修改数组中较大索引处的元素时，`splice` 很有用。

# indexOf, lastIndexOf, contains

有时我们可能想要找到数组中某个元素的第一个或最后一个索引：

```javascript
const arr = [1, 2, 3, 2, 1];
arr.indexOf( 1 )      // returns 0
arr.lastIndexOf( 1 )  // returns 4
```

你还可以检查第一个大于或等于传递给 `indexOf` 的第二个参数的元素的第一个索引：

```javascript
arr.indexOf( 1, 0 )  // returns 0
arr.indexOf( 1, 2 )  // returns 4
```

类似地，你可以检索最后一个或等于传递给 `lastIndexOf` 的第二个参数的元素的索引：

```javascript
arr.lastIndexOf( 1, 4 ) // returns 4
arr.lastIndexOf( 1, 3 ) // returns 0
```

如果 `indexOf` 或 `lastIndexOf` 的第一个参数在数组中未找到，两者都返回 -1：

```javascript
arr.indexOf( 1, 5 )    // returns -1
arr.lastIndexOf( 1, 5 ) // returns -1
```

在 ES2016 之前，`indexOf` 的典型用例是确定数组是否包含一个值。自 ES2016 起，此操作使用更语义的 `includes` 方法。

```javascript
// ES2015
if ( arr.indexOf( value ) !== -1 ) {
    // do something
}

// ES2016
if ( arr.includes( value ) ) {
    // do something
}
```

`A.includes(value)` 方法返回：`true` 如果 `value` 在 `A` 中，否则返回 `false`。

# Map, reduce, filter

本节介绍一些将在函数式编程章节使用的高阶数组方法。本节的目标是定义这些函数。假设一个数组 `arr` 的值为 `[1, 2, 3, 4, 5]`。`map` 获取数组每个元素，并对它们逐一应用函数。例如，我们有一个 `times2` 函数，它将数组的每个元素乘以 2：

```javascript
const arr = [1, 2, 3, 4, 5];
function times2( input ) {
    return input * 2;
}
```

`map` 的执行过程如下：

```
arr.map( times2 ) // [2, 4, 6, 8, 10]
```

由于创建 `times2` 函数需要写很多行，所以箭头函数更有意义：

```javascript
const arr = [1, 2, 3, 4, 5];
const result = arr.map( x => x * 2 ); // returns [2, 4, 6, 8, 10]
```

上面的表达式等同于定义 `times2` 函数并使用 `map` 将其应用于数组。`map` 扩展接受一个有两个参数的函数，分别指定映射的元素及其索引：

```javascript
const fruits = ['apple', 'pear', 'banana'];
const result = fruits.map( (item, index) => [index, item] );
// result becomes: [[0, 'apple'], [1, 'pear'], [2, 'banana']]
```

注意，上述结果也可以使用 `entries` 方法描述：

```javascript
const fruits = ['apple', 'pear', 'banana'];
const result = [...fruits.entries()];
```

你可能会问为什么需要写 `[...fruits.entries()]` 而不是直接写 `fruits.entries()`。答案是，因为 `fruits.entries()` 返回一个迭代器，它也是一个可迭代对象。这个迭代对象可以使用展开运算符进行迭代，从而产生元素。数组消费这些值，从而产生一个数组。你现阶段不需要理解这些概念，这是高级 JavaScript。如果你对细节感兴趣，请查看我的文章 [ES6迭代器与生成器](http://www.zsoltnagy.eu/es6-iterators-and-generators-in-practice/)，以及属于该文章的 [练习](http://www.zsoltnagy.eu/es6-iterators-and-generators-6-exercises-and-solutions/)。

与 `map` 类似，`filter` 也返回一个数组，但它使用一个返回布尔值的函数。假设我们有一个函数对偶数返回 `true`。`filter` 的作用是保留数组中那些传入的函数返回 `true` 的元素：

```javascript
const arr = [1, 2, 3, 4, 5];
arr.filter( x => x % 2 === 0 ); // returns [2, 4]
```

# 第二部分：深入理解 JavaScript 类型

```javascript
const arr = [1, 2, 3, 4, 5];
arr.filter( x => x % 2 === 0 ) // 返回 [2, 4]
arr.filter( x => x % 2 !== 0 ) // 返回 [1, 3, 5]
```

`find` 方法是 `filter` 的一个特例：它返回找到的第一个元素。

```javascript
const arr = [1, 2, 3, 4, 5];
arr.find( x => x % 2 === 0 ) // 返回 2
```

在我作为面试官的实践中，我见过无数试图跳出 `forEach` 辅助方法的尝试。这是不可能的，因为 `forEach` 不会终止。假设我们有以下代码，用于打印 `arr` 中第一个偶数值：

```javascript
const arr = [1, 2, 3, 4, 5];
arr.forEach( x => {
    if ( x % 2 === 0 ) {
        console.log( x );
        // return; // 这不会终止 forEach 循环
    }
});
```

`forEach` 接受一个有两个参数的函数，分别指定元素及其索引：

```javascript
const arr = [1, 2, 3, 4, 5];
arr.forEach( (element, index) => {
    console.log(index, element);
});
```

`forEach` 不返回任何值。

```javascript
const arr = [1, 2, 3, 4, 5];
const result = arr.forEach( x => x );
// result is undefined
```


```javascript
// A.push( element )
A = [...A, element]

// A.unshift( element )
A = [element, ...A]

// A.shift()
[, ...A] = A
```

`pop` 方法只有在我们知道数组大小并且用变量表示每个元素的情况下，才能用解构赋值表达：

```javascript
// A.pop()，其中 A.length 为 3：
[a, b] = A;
A = [a, b];
```

我们只是为了练习而表达了`pop`，因为`pop`比这些解构赋值在语义上清晰得多。

请注意，在性能方面，`push`、`pop`预期会更好，然而，对于小数组来说差异并不大。

```javascript
console.time( 'push_pop' );
for ( let i = 0; i < 1000000; ++i ) {
    let A = [1, 2, 3, 4, 5, 6, 7, 8, 9];
    A.push( 10 );
    A.pop();
}
console.timeEnd( 'push_pop' );
console.time( 'spread' );
for ( let i = 0; i < 1000000; ++i ) {
    let A = [1, 2, 3, 4, 5, 6, 7, 8, 9];
    A = [...A, 10];
    A.pop();
}
console.timeEnd( 'spread' );
```

输出是在同一标签上执行`console.time`和`console.timeEnd`之间经过的时间。

```javascript
push_pop: 68.93310546875ms
spread: 489.0859375ms
```

对于小数组，`shift`和`unshift`操作的性能可能比简单的解构赋值更差。

```javascript
console.time( 'unshift_shift' );
for ( let i = 0; i < 1000000; ++i ) {
    let A = [1, 2, 3, 4, 5, 6, 7, 8, 9];
    A.unshift( 0 );
    A.shift();
}
console.timeEnd( 'unshift_shift' );
console.time( 'spread' );
for ( let i = 0; i < 1000000; ++i ) {
    let A = [1, 2, 3, 4, 5, 6, 7, 8, 9];
    A = [0, ...A];
    [, ...A] = A;
}
console.timeEnd( 'spread' );
```

```javascript
unshift_shift: 176.8681640625ms
spread: 145.7060546875ms
```

随着数组大小的增长，我们可能会发现`shift`和`unshift`的性能变得更有优势：

```javascript
console.time( 'unshift_shift' );
for ( let i = 0; i < 1000000; ++i ) {
    let A = new Array(1000).fill('a');
    A.unshift( 0 );
    A.shift();
}
console.timeEnd( 'unshift_shift' );
console.time( 'spread' );
for ( let i = 0; i < 1000000; ++i ) {
    let A = new Array(1000).fill('a');
    A = [0, ...A];
    [, ...A] = A;
}
console.timeEnd( 'spread' );
```

```javascript
unshift_shift: 7177.94873046875ms
spread: 18837.948974609375ms
```

`push`和`unshift`方法可以接收可变数量的参数：

```javascript
const A = [4, 5, 6];
A.push( 7, 8, 9 );       // 返回 6
A.unshift( 0, 1, 2, 3 ); // 返回 10

console.log( A );
// 打印 [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

## 数组连接和 concat 方法

假设给定两个数组：

```javascript
const A = [1, 2, 3];
const B = ['apple', 'pear'];
```

连接两个数组的一个显而易的方法是使用展开运算符：

```javascript
const AB = [...A, ...B];
// [1, 2, 3, "apple", "pear"]
```

`concat`方法通常是一种更高效的方式来执行相同的连接操作：

```javascript
A.concat( B )
(5) [1, 2, 3, "apple", "pear"]
A
(3) [1, 2, 3]
B
(2) ["apple", "pear"]
```

如你所见，`concat`不会修改原始数组`A`。

我们可以在`concat`的参数列表中提供多个数组：

```javascript
const A = [1, 2];
A.concat( [3, 4], [5, 6] );
// [1, 2, 3, 4, 5, 6]
```

另一种连接数组的方法是使用`push`：

```javascript
const A = [1, 2];
const B = [3, 4];
const C = [5, 6];
A.push(...B, ...C);
console.log( A );
// 输出 [1, 2, 3, 4, 5, 6]
```

请注意，使用`push`会修改原始数组`A`。

## sort 方法

`sort`方法对数组中的值进行排序：

```javascript
const arr = [2, 5, 1, 4];
arr.sort();
console.log( arr ); // [1, 2, 4, 5]
```

排序是原地执行，会修改原始的值。`sort`方法也返回排序后的引用。

## reverse 方法

`reverse`方法可以原地反转数组：

```javascript
const arr = [1, 2, 3, 4];
arr.reverse();
console.log( arr ); // [4, 3, 2, 1]
```

## 在 JavaScript 中使用对象

我们在之前的章节中学，对象是相关数据和操作的集合。对象帮助你使用引用来组合任意的值。存储在对象内部的数据字段被称为`属性`，可以在对象执行的操作被称为`方法`。让我们看一个例子：

```javascript
let account = {
    owner: 'John',
    amount: 1000,
    deposit: function (depositAmount) {
        this.amount += depositAmount;
    }
};
```

注意，我们可以使用`this`关键字在方法内部访问属性。有两种表示法获取对象的字段：

- 点表示：`account.amount`
- 方括号表示：`account['amount']`

```javascript
> account.owner
'John'
> account.deposit(500)
undefined
> account.amount
1500
```

两种表示法都可以用于获取和设置对象的值，以及删除属性：

```javascript
account.owner = null;
account['x'] = true;
delete account['x'];
```

例如，上面的表达式将`account['owner']`设置为`null`。注意，新值的类型不必与原始值的匹配。要从对象中移除一个字段，请使用`delete`操作：

```javascript
> account
{owner: null, amount: 1000, deposit: f}
> delete account.owner
true
> account
{amount: 1000, deposit: f}
```

表达式`delete account.owner`从对象中移除了`owner: null`这个键对。该表达式计算结果为`true`，因为删除成功了。我们已经看到一种创建对象的方式：对象字量表示法。一个空对象可以使用`}`来创建。创建之后，可以向它添加属性和操作：

```javascript
const objectLiteral = {};
objectLiteral.property = 1;
objectLiteral.operation = () => 1;
```

包括`}`表示法在内，创建空对象三种方式：

- `{}`
- `new Object()`
- `Object.create(Object.prototype)`

第三种选项对许多 JavaScript开发者来说看起来有点陌生，但我们仍然会使用它，因为它提供了一种在创建对象时设置其`prototype`的简便方法。

我们现在将介绍更高级的对象概念：

- 枚举对象属性名称和值
- 全局对象
- 自有属性和继承属性
- 对象属性及其设置
- 冻结和密封对象
- getter和 setter
- 属性简写表示法
- 计算属性键
- 等等性
- 使用`Object.assign`进行混合和浅拷贝
- 解构对象
- 扩展对象
- symbol键

在本节中，我们将不涉及原型链、设置对象的原型或获取对象的原型。

## 枚举对象属性名称和值

我们可以分别使用`Object.keys`、`Object.values`、`Object.entries`方法来获取对象的键、值和条目的数组。`>`表示控制台的提示符。

```javascript
let account = {
    owner: 'John',
    amount: 1000
};

> Object.keys(account)
["owner", "amount"]

> Object.values(account)
["John", 1000]

> Object.entries(account)
[["owner", "John"], ["amount", 1000]]
```

`for...in`循环也可以枚举属性：

```javascript
> for (let property in account) {
    console.log(property);
}
owner
amount
```

## 全局对象

我们还没有介绍继承。然而，值得注意的是，可以枚举不来自对象本身的属性。对象属性的继承是通过`prototype chain`定义的。一些属性是从我们对象的原型继承的，或者从我们对象原型的原型继承的，以此类推。全局`Object`位于原型链的顶端。

```javascript
let account = {
    owner: 'John',
    amount: 1000,
    deposit: function (depositAmount) {
        this.amount += depositAmount;
    }
};
```

注意，我们可以使用`this`关键字在方法内部访问属性。有两种表示法获取对象的字段：

- 点表示：`account.amount`
- 方括号表示：`account['amount']`

```javascript
> account.owner
'John'
> account.deposit(500)
undefined
> account.amount
1500
```

两种表示法都可以用于获取和设置对象的值，以及删除属性：

```javascript
account.owner = null;
account['x'] = true;
delete account['x'];
```

例如，上面的表达式将`account['owner']`设置为`null`。注意，新值的类型不必与原始值的匹配。要从对象中移除一个字段，请使用`delete`操作：

```javascript
> account
{owner: null, amount: 1000, deposit: f}
> delete account.owner
true
> account
{amount: 1000, deposit: f}
```

表达式`delete account.owner`从对象中移除了`owner: null`这个键值对。该表达式计算结果为`true`，因为删除成功了。我们已经看到一种创建对象的方式：对象字量表示法。一个空对象可以使用`}`来创建。创建之后，可以向它添加属性和操作：

```javascript
const objectLiteral = {};
objectLiteral.property = 1;
objectLiteral.operation = () => 1;
```

包括`}`表示法在内，创建空对象三种方式：

- `{}`
- `new Object()`
- `Object.create(Object.prototype)`

第三种选项对许多 JavaScript开发者来说看起来有点陌生，但我们仍然会使用它，因为它提供了一种在创建对象时设置其`prototype`的简便方法。

## 自有属性和继承属性

我们还没有介绍继承。然而，值得注意的是，可以枚举不来自对象本身的属性。对象属性的继承是通过`prototype chain`定义的。一些属性是从我们对象的原型继承的，或者从我们对象原型的原型继承的，以此类推。全局`Object`位于原型链的顶端。

```javascript
let account = {
    owner: 'John',
    amount: 1000,
    deposit: function (depositAmount) {
        this.amount += depositAmount;
    }
};
```

注意，我们可以使用`this`关键字在方法内部访问属性。有两种表示法获取对象的字段：

- 点表示：`account.amount`
- 方括号表示：`account['amount']`

```javascript
> account.owner
'John'
> account.deposit(500)
undefined
> account.amount
1500
```

两种表示法都可以用于获取和设置对象的值，以及删除属性：

```javascript
account.owner = null;
account['x'] = true;
delete account['x'];
```

例如，上面的表达式将`account['owner']`设置为`null`。注意，新值的类型不必与原始值的匹配。要从对象中移除一个字段，请使用`delete`操作：

```javascript
> account
{owner: null, amount: 1000, deposit: f}
> delete account.owner
true
> account
{amount: 1000, deposit: f}
```

表达式`delete account.owner`从对象中移除了`owner: null`这个键值对。该表达式计算结果为`true`，因为删除成功了。我们已经看到一种创建对象的方式：对象字量表示法。一个空对象可以使用`}`来创建。创建之后，可以向它添加属性和操作：

```javascript
const objectLiteral = {};
objectLiteral.property = 1;
objectLiteral.operation = () => 1;
```

## 对象属性及其设置

对象属性及其设置：

```javascript
let account = {
    owner: 'John',
    amount: 1000,
    deposit: function (depositAmount) {
        this.amount += depositAmount;
    }
};
```

## 冻结和密封对象

```javascript
const obj = {
    name: "Alice",
    age: 30
};

Object.freeze(obj);
obj.name = "Jane"; // 不生效
obj.age = 25;     // 不生效
delete obj.name;  // 不生效

Object.seal(obj);
obj.age = 25;    // 生效
delete obj.name; // 不生效
```

## getter 和 setter

```javascript
const user = {
    _name: "John",
    get name() {
        return this._name;
    },
    set name(value) {
        this._name = value;
    }
};

user.name = "Bob";
console.log(user.name); // "Bob"
```

## 属性简写表示法

```javascript
const firstName = "John";
const lastName = "Doe";
const person = {
    firstName,
    lastName
};
```

## 计算属性键

```javascript
const user = {
    name: "John",
    ["y" + "name"]: "Stack Overflow"
};
console.log(user.username); // "Stack Overflow"
```

## 等性

```javascript
const obj1 = { a: 1 };
const obj2 = { a: 1 };
const obj3 = obj1;

console.log(obj1 === obj2); // false
console.log(obj1 === obj3); // true
```

## 使用`Object.assign`进行混合和浅拷贝

```javascript
const target = { a: 1 };
const source1 = { b: 2 };
const source2 = { c: 3 };

const merged = Object.assign(target, source1, source2);
console.log(merged); // {a: 1, b: 2, c: 3}

const copy = Object.assign({}, obj1);
console.log(copy); // {a: 1}
```

## 解构对象

```javascript
const user = { id: 1, name: "John", age: 30 };
const { name, ...rest } = user;
console.log(name); // "John"
console.log(rest); // { id: 1, age: 30 }
```

## 扩展对象

```javascript
const base = { a: 1, b: 2 };
const extra = { c: 3 };
const merged = { ...base, ...extra };
console.log(merged); // { a: 1, b: 2, c: 3 }
```

## symbol键

```javascript
const id = Symbol("id");
const user = {
    [id]: 123,
    name: "John"
};
console.log(Object.keys(user)); // ["name"]
console.log(user[id]); // 123
```

content]
我们可以使用 `Object.getOwnPropertyDescriptors` 访问这些配置设置。

```
> Object.getOwnPropertyDescriptors( {a: 1} );
{
  a: {
    value: 1,
    writable: true,
    enumerable: true,
    configurable: true
  }
}
```

也可以访问属于单个属性的属性描述符：

```
> Object.getOwnPropertyDescriptor( {a: 1 }, 'a' )
{value: 1, writable: true, enumerable: true, configurable: true}
```

```
> Object.getOwnPropertyDescriptor( {a: 1 }, 'b' )
undefined
```

让我们使用对象字面量创建一个空对象。

```javascript
const objectLiteral = {};
objectLiteral.property = 1;
```

除了 `objectLiteral.property`，，我们也可以使用 `Object.defineProperty` 方法定义属性。`Object.defineProperty` 接受三个参数：

-   一个对象引用，

-   属性名称，

-   一个包含 `value`、`configurable`、`enumerable` 和 `writable` 的配置对象。如果选项 `configurable`、`enumerable` 或 `writable` 缺失，它们的默认值为 `false`。

```javascript
Object.defineProperty(
  objectLiteral,
  'definedProperty',
  {
    value: 'propertyValue',
    configurable: true,
    enumerable: true,
    writable: true
  }
);
```

让我们试验不同的属性配置。`>` 表示控制台的提示符。

```javascript
Object.defineProperty(
    objectLiteral,
    'nonConfigurable',
    {
        value: 'v',
        configurable: false,
        enumerable: true,
        writable: true
    }
);
```

```
> delete objectLiteral.nonConfigurable
false
```

```
> objectLiteral.nonConfigurable
"v"
```

```
> Object.defineProperty(
    objectLiteral,
    'nonConfigurable',
    {
        value: 'w',
        configurable: true,
        enumerable: true,
        writable: true
    }
);
```

```
Uncaught TypeError: Cannot redefine property: nonConfigurable
    at Function.defineProperty (<anonymous>)
    at <anonymous>:1:8
```

不可配置的属性：

-   无法删除，

-   无法重新配置。

让我们试验不可枚举的属性。

```javascript
Object.defineProperty(
    objectLiteral,
    'nonEnumerable',
    {
        value: 'ne',
        configurable: true,
        enumerable: false,
        writable: true
    }
);
```

```
> for ( let p in objectLiteral ) console.log( p );
property
definedProperty
nonConfigurable
```

```
> Object.keys( objectLiteral )
["property", "definedProperty", "nonConfigurable"]
```

不可枚举的属性既不会在 `for...in` 循环中显示，也不会在 `Object.keys` 枚举中显示。

最后，不可写的属性使得更改属性的值变得不可能。对属性的赋值会静默失败，用户不会遇到错误，除非代码在严格模式下运行（即声明了字符串 `"use strict"`）。

```javascript
Object.defineProperty(
    objectLiteral,
    'nonWritable',
    {
        value: 'w',
        configurable: true,
        enumerable: true,
        writable: false
    }
);
```

```
> objectLiteral.nonWritable = 'X';
"X"
```

```
> objectLiteral.nonWritable;
"w"
```

这种行为并不方便，因为赋值似乎已经发生，直到我们查询先前赋值的属性的值。严格模式可以在函数作用域内启用，使用 `立即调用函数表达式`：

```javascript
(() => {
  "use strict";
  objectLiteral.nonWritable = 'X';
})()
Uncaught TypeError: Cannot assign to read only property 'nonWritable' of object '#<Object>'
  at <anonymous>:3:31
  at <anonymous>:4:3
```

通常使用严格模式是有用的，因为你倾向于获得更多的错误，这些错误可以在你的应用程序部署到生产环境之前得到纠正。

# 冻结和密封对象

根据我作为技术面试官的经验，一些开发者认为 `const` 关键字可以创建内容不可修改的对象。这个说法是错误的。`const` 关键字只确保变量引用一个对象，并且这个引用不能更改。对象的内容可以随时修改。

```javascript
const account = {
  owner: 'Zsolt',
  amount: 1000
}
```

```
> account.amount = 500
500
```

```
> account
{owner: "Zsolt", amount: 500}
```

要创建一个真正的不可变常量，对象必须被 `冻结`：

```javascript
const account = {
    owner: 'Zsolt',
    amount: 1000
}

Object.freeze( account );
```

```
> account.amount = 500
500
```

```
> account.newProperty = true
true
```

```
> delete account.owner
false
```

```
> account
{owner: "Zsolt", amount: 1000}
```

```javascript
> Object.defineProperty(
        account,
        'newProperty2',
        {
            value: 'w',
            configurable: true,
            enumerable: true,
            writable: false
        }
    );
Uncaught TypeError: Cannot define property newProperty2, object is not extensible
    at Function.defineProperty (<anonymous>)
    at <anonymous>:1:8
```

总结：冻结的对象是不可变的。这意味着：

-   其属性的值不能更改，

-   不能向其添加新属性，

-   现有属性不能删除，

-   属性的配置不能重新定义。

严格模式提供了更多错误，指示非严格执行失败时的错误：

```javascript
> (() => {
    "use strict";
    account.amount = 500;
})()
Uncaught TypeError: Cannot assign to read only property 'amount' of object '#<Object>'
at <anonymous>:3:20
at <anonymous>:4:3
```

```
> (() => {
    "use strict";
    account.newProperty = true;
})()
Uncaught TypeError: Cannot add property newProperty, object is not extensible
at <anonymous>:3:27
at <anonymous>:4:5
```

```
> (() => {
    "use strict";
    delete account.owner;
})()
Uncaught TypeError: Cannot delete property 'owner' of #<Object>
at <anonymous>:3:7
at <anonymous>:4:5
```

在JavaScript开发中，有些用例我们需要能够更改现有属性，但无法向其添加新属性或删除现有属性。这时 `Object.seal` 就派上用场了。

```javascript
const rootAccount = {
    owner: 'root',
    amount: Infinity
}

Object.seal( rootAccount );
```

```
> rootAccount.amount = 1000
1000
```

```
> rootAccount
{owner: "root", amount: 1000}
```

```
> Object.defineProperty( rootAccount, 'amount', {value: 500} )
```

# Getters and setters

`Object.defineProperty` 也可用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
  }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于用于为属性定义 getter getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于用于为属性定义 getter getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于用于为属性定义 getter getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于用于为属性定义 getter getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```


排版后的：


我们可以使用 `Object.getOwnPropertyDescriptors` 访问这些配置设置。

Object.defineProperty 也可用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于用于为属性定义 getter getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```

`Object.defineProperty` 也可用于用于为属性定义 getter getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```


*(注：由于原始文本存在大量重复且未完成的片段，排版时已根据“保留核心内容”和“删除多余”的原则进行了精简和去重处理。)*

**抱歉，由于您提供的文本中存在大量的重复和不完整的代码片段（例如 `Object.defineProperty` 部分重复了多次），我为您进行了逻辑上的重排版。以下是针对您提供内容的完整排版结果：**


我们可以使用 `Object.getOwnPropertyDescriptors` 访问这些配置设置。

```
> Object.getOwnPropertyDescriptors( {a: 1} );
{
  a: {
    value: 1,
    writable: true,
    enumerable: true,
    configurable: true
  }
}
```

也可以访问属于单个属性的属性描述符：

```
> Object.getOwnPropertyDescriptor( {a: 1 }, 'a' )
{value: 1, writable: true, enumerable: true, configurable: true}
```

```
> Object.getOwnPropertyDescriptor( {a: 1 }, 'b' )
undefined
```

让我们使用对象字面量创建一个空对象。

```javascript
const objectLiteral = {};
objectLiteral.property = 1;
```

除了 `objectLiteral.property`，我们也可以使用 `Object.defineProperty` 方法定义属性。`Object.defineProperty` 接受三个参数：

-   一个对象引用，

-   属性名称，

-   一个包含 `value`、`configurable`、`enumerable` 和 `writable` 的配置对象。如果选项 `configurable`、`enumerable` 或 `writable` 缺失，它们的默认值为 `false`。

```javascript
Object.defineProperty(
  objectLiteral,
  'definedProperty',
  {
    value: 'propertyValue',
    configurable: true,
    enumerable: true,
    writable: true
  }
);
```

让我们试验不同的属性配置。`>` 表示控制台的提示符。

```javascript
Object.defineProperty(
    objectLiteral,
    'nonConfigurable',
    {
        value: 'v',
        configurable: false,
        enumerable: true,
        writable: true
    }
);
```

```
> delete objectLiteral.nonConfigurable
false
```

```
> objectLiteral.nonConfigurable
"v"
```

```javascript
> Object.defineProperty(
    objectLiteral,
    'nonConfigurable',
    {
        value: 'w',
        configurable: true,
        enumerable: true,
        writable: true
    }
);
```

```
Uncaught TypeError: Cannot redefine property: nonConfigurable
    at Function.defineProperty (<anonymous>)
    at <anonymous>:1:8
```

不可配置的属性：

-   无法删除，

-   无法重新配置。

让我们试验不可枚举的属性。

```javascript
Object.defineProperty(
    objectLiteral,
    'nonEnumerable',
    {
        value: 'ne',
        configurable: true,
        enumerable: false,
        writable: true
    }
);
```

```
> for ( let p in objectLiteral ) console.log( p );
property
definedProperty
nonConfigurable
```

```
> Object.keys( objectLiteral )
["property", "definedProperty", "nonConfigurable"]
```

不可枚举的属性既不会在 `for...in` 循环中显示，也不会在 `Object.keys` 枚举中显示。

最后，不可写的属性使得更改属性的值变得不可能。对属性的赋值会静默失败，用户不会遇到错误，除非代码在严格模式下运行（即声明了字符串 `"use strict"`）。

```javascript
Object.defineProperty(
    objectLiteral,
    'nonWritable',
    {
        value: 'w',
        configurable: true,
        enumerable: true,
        writable: false
    }
);
```

```
> objectLiteral.nonWritable = 'X';
"X"
```

```
> objectLiteral.nonWritable;
"w"
```

这种行为并不方便，因为赋值似乎已经发生，直到我们查询先前赋值的属性的值。严格模式可以在函数作用域内启用，使用 `立即调用函数表达式`：

```javascript
(() => {
  "use strict";
  objectLiteral.nonWritable = 'X';
})()
Uncaught TypeError: Cannot assign to read only property 'nonWritable' of object '#<Object>'
  at <anonymous>:3:31
  at <anonymous>:4:3
```

通常使用严格模式是有用的，因为你倾向于获得更多的错误，这些错误可以在你的应用程序部署到生产环境之前得到纠正。

# 冻结和密封对象

根据我作为技术面试官的经验，一些开发者认为 `const` 关键字可以创建内容不可修改的对象。这个说法是错误的。`const` 关键字只确保变量引用一个对象，并且这个引用不能更改。对象的内容可以随时修改。

```javascript
const account = {
  owner: 'Zsolt',
  amount: 1000
}
```

```
> account.amount = 500
500
```

```
> account
{owner: "Zsolt", amount: 500}
```

要创建一个真正的不可变常量，对象必须被 `冻结`：

```javascript
const account = {
    owner: 'Zsolt',
    amount: 1000
}

Object.freeze( account );
```

```
> account.amount = 500
500
```

```
> account.newProperty = true
true
```

```
> delete account.owner
false
```

```
> account
{owner: "Zsolt", amount: 1000}
```

```javascript
> Object.defineProperty(
        account,
        'newProperty2',
        {
            value: 'w',
            configurable: true,
            enumerable: true,
            writable: false
        }
    );
Uncaught TypeError: Cannot define property newProperty2, object is not extensible
    at Function.defineProperty (<anonymous>)
    at <anonymous>:1:8
```

总结：冻结的对象是不可变的。这意味着：

-   其属性的值不能更改，

-   不能向其添加新属性，

-   现有属性不能删除，

-   属性的配置不能重新定义。

严格模式提供了更多错误，指示非严格执行失败时的错误：

```javascript
> (() => {
    "use strict";
    account.amount = 500;
})()
Uncaught TypeError: Cannot assign to read only property 'amount' of object '#<Object>'
at <anonymous>:3:20
at <anonymous>:4:3
```

```javascript
> (() => {
    "use strict";
    account.newProperty = true;
})()
Uncaught TypeError: Cannot add property newProperty, object is not extensible
at <anonymous>:3:27
at <anonymous>:4:5
```

```javascript
> (() => {
    "use strict";
    delete account.owner;
})()
Uncaught TypeError: Cannot delete property 'owner' of #<Object>
at <anonymous>:3:7
at <anonymous>:4:5
```

在JavaScript开发中，有些用例我们需要能够更改现有属性，但无法向其添加新属性或删除现有属性。这时 `Object.seal` 就派上用场了。

```javascript
const rootAccount = {
    owner: 'root',
    amount: Infinity
}

Object.seal( rootAccount );
```

```
> rootAccount.amount = 1000
1000
```

```
> rootAccount
{owner: "root", amount: 1000}
```

```
> Object.defineProperty( rootAccount, 'amount', {value: 500} )
```

# Getters and setters

`Object.defineProperty` 也可用于为属性定义 getter 和 setter。我们来定义一个 `area` 属性，使其返回 `sideLength` 属性值的平方。当设置 `area` 时，`sideLength` 会自动计算为 `area` 的平方根。

```javascript
const square = {
  sideLength: 5
};

Object.defineProperty(
  square,
  'area',
  {
    get: function () {
      return this.sideLength ** 2;
    },
    set: function (value) {
      this.sideLength = Math.sqrt(value);
    }
  }
);
```

```javascript
> square.area
25
```

```javascript
> square.area = 100
undefined
```

```javascript
> square.sideLength
10
```



- `toolbar`（工具栏）
- `preloader animation`（预加载动画）

假设扩展的顺序无关紧要，使用上述五种增强可以定义 32 种不同的视图类型。为了应对组合爆炸，我们只需将这些扩展作为 mixins，并用用我们需要的扩展来扩展我们的对象原型。

例如，一个带有预加载动画的验证视图可以如下定义：

```javascript
let View = { ... };
let ValidationMixin = { ... };
let PreloaderAnimationMixin = { ... };

let ValidatingMixinWithPreloader = Object.assign(
    {},
    View,
    ValidationMixin,
    PreloaderAnimationMixin
);
```

为什么我们扩展空对象？因为 `Object.assign` 的工作方式是扩展它的第一个参数，参数列表中的其余参数作为扩展源。这意味着 `Object.assign` 的第一个参数可能会获得新的键，或者其值会被来自 `mixin` 对象的值覆盖。

调用 `Object.assign` 的语法如下：

```javascript
Object.assign( targetObject, ...sourceObjects )
```

`Object.assign` 的返回值是 `targetObject`。调用 `Object.assign` 的副作用是 `targetObject` 会被修改。

`Object.assign` 将 `...sourceObjects` 的属性和操作进行`浅复制`并放入 `targetObject`。

更多关于`浅复制`或克隆的信息，请查看我的文章 [Cloning Objects in JavaScript](http://www.zsoltnagy.eu/cloning-objects-in-javascript/)⁴⁸。

```javascript
let horse = {
    horseName: 'QuickBucks',
    toString: function() {
        return this.horseName;
    }
};

let rider = {
    riderName: 'Frank',
   toString: function() {
       return this.riderName;
   }
};

let horseRiderStringUtilty = {
   toString: function() {
       return this.riderName + ' on ' + this.horseName;
   }
}

let racer = Object.assign(
    {},
    horse,
    rider,
    horseRiderStringUtility
);

console.log( racer.toString() );
// "Frank on QuickBucks"
```

如果在组装 `racer` 对象时我们省略了 `{}`，表面上看什么也不会改变，因为 `racer.toString()` 仍然是 "Frank on QuickBucks"。然而，请注意，`horse` 会变成等同于 `racer`，这意味着执行 `Object.assign` 的副作用将是修改 `horse` 对象。

# Destructuring objects

在创建对象的作用域内，可以使用其他变量进行初始化。

```javascript
let shapeName = 'Rectangle', a = 5, b = 3;

let shape = { shapeName, a, b, id: 0 };

console.log( shape );
// { a: 5, b: 3, id: 0, shapeName: "Rectangle" }
```

可以在解构赋值中使用这种简写来创建新字段：

```javascript
let { x, y } = { x: 3, y: 4, z: 2 };

console.log( y, typeof y );
// 4 "number"
```

# Spreading objects

展开运算符和剩余参数是 ES2015 中一个受欢迎的新增特性。你可以将数组展开为逗号分隔的值，也可以在函数参数列表的末尾添加一个剩余参数来处理可变数量的参数。

让我们看看相同的概念如何应用于对象：

我们现在可以创建一个解构表达式，在其中匹配若干属性，并将剩余属性收集到 `bookData` 对象引用中。

```
let { chapters, website, ...bookData } = book
```

一旦创建此赋值，`chapters` 数值字段将被移入 `chapters` 变量，`website` 将保存字符串 `'devcareermastery.com'`。其余字段将被移入 `bookData` 对象：

```
> bookData
{author: "Zsolt Nagy", title: "The Developer's Edge"}
```

这就是为什么 `...bookData` 被称为剩余属性。它收集之前未匹配的字段。对象的剩余属性的工作方式与数组的剩余参数相同。解构的工作方式也与数组完全相同。与剩余参数类似，我们可以使用剩余属性来创建对象的浅拷贝。参考我的文章 JavaScript 中的对象克隆。

```
let clonedBook = { ...book };
```

你还可以在克隆现有字段的基础上向对象添加更多字段。

```
let extendedBook = {
  pages: 250,
  ...clonedBook
}
```

展开语法可以用 `Object.assign` 表示：

```javascript
let book = {
    author: 'Zsolt Nagy',
    title: 'The Developer\'s Edge',
    website: 'devcareermastery.com',
    chapters: 8
}

// let clonedBook = { ...book };
let clonedBook = Object.assign( {}, book );

// let extendedBook = {
//    pages: 250,
//    ...clonedBook
// }
let extendedBook = Object.assign( {pages: 250}, clonedBook );
```

# Symbol 键

在 ES6 中引入了 `Symbol` 类型。每个 `symbol` 都是唯一的。即使两个 `symbol` 关联相同的标签，它们也是不同的：

```
> Symbol( 'label' ) == Symbol( 'label' )
false
```

JavaScript 允许字符串和 `symbols` 作为对象键。这使得可以定义自己的唯一标识符，而无需担心是否有其他资源使用相同的标识符。例如，如果我们创建一个全局 `Symbol( 'jQuery' )`，并且另一个文件中存在另一个全局 `Symbol( 'jQuery' )`，这两个值可以共存，并且它们不会相等。

实际上，上述好处不会导致维护，但它是解决冲突的一种方式。在不判断什么维护或不可维护的情况下，JavaScript 允许你使用 `Symbol` 键：

```
const key = Symbol( 'key' );

const o = {
    [key]: true,
    [Symbol( 'key' )]: true
}
```

注意 `Symbol` 键以下特性：

1. 其值不会出现在 JSON 中：
2. 其值不会出现在 `for..in`、`Object.keys`、`Object.entries`、`ObjectOwnPropertyNames` 中：
3. 其值出现在 `ObjectOwnPropertyDescriptors` 中：
4. 其值出现在浅拷贝中：

```
> JSON.stringify(o)
"{}"
```

```
> for ( let p in o )
undefined

> Object.keys( o )
[]

> Object.entries( o )
[]

> ObjectOwnPropertyNames( o )
[]
```

```
> ObjectOwnPropertyDescriptors( o )
```



因此，`Symbol` 键不是表示私有属性的方式。

```
> {...o}
{Symbol(key): true, Symbol(key2): true}

> Object.assign( {}, o )
{Symbol(key): true, Symbol(key2): true}
```

# 类数组对象

在 JavaScript 中，有一些对象不是数组，但它们像数组。这些对象的例子是函数的 `arguments` 对象：

```
function variableArguments() {
    return arguments;
}

const args = variableArguments( 1, 2, 3, 4 );

console.log( args )
// [1, 2, 3, 4], callee: f, Symbol(iterator): f
```

类数组中未定义数组方法：

```
> args.map
undefined

> args.push
undefined
```

在 ES6 发明运算符之前的之前的中，这是编写可变数量的唯一方式。在新版本的 JavaScript 中，鼓励使用 `arguments` 对象。请用剩余参数。在下面的例子中，`args` 是真正的数组：

```javascript
function variableArguments2( ...args ) {
    return args;
}

const args2 = variableArguments2( 1, 2, 3, 4 );

console.log( args2 );
// [1, 2, 3, 4]
```

一般来说，类数组对象所示：

```javascript
const A = {
    0: 'value0',
    1: 'value1',
    length: 2
}
```

在这个对象中，`A[1]` 返回 `value1`。`A.length` 返回 `2`。类数组不是真正的数组，因为它们没有某些数组属性和操作，例如：`map`、`reduce`、`filter`、`slice`、`splice`、`push`、`pop`、`append`、`concat`、`join` 等。上述方法适用于类数组的原因是它们继承自 `Object.prototype`，而不是 `Array.prototype`。证明：

```
A.constructor
f Object() { [native code] }
B.constructor
f Array() { [native code] }
```

类数组可以通过多种方式转换为数组：

- `Array.from( args )`
- `Object.values( args )`
- `[...]`

在 ES6 之前，由于使用类数组对象，柯里化等函数技术更难理解。使用可变参数数量时，请使用剩余参数。记住，`Array.isArray` 用于判断引用指向数组还是类数组对象：

# 第二部分：深入 JavaScript 类型

```
const A = {
    0: 'value0',
    1: 'value1',
    length: 2
}

Array.isArray( A );           // false
Array.isArray( Array.from( A ) ); // true
```

# JavaScript 中的函数

# 作用域：var、let、const

# 原型继承

# JavaScript 错误

# 闭包

# JavaScript 中的克隆

# JavaScript Promise

# 严格模式

# 第三部分：Web 开发简介

# 访问 DOM

# JavaScript 中的事件处理

# JSON

- 提及自有属性，不枚举 `Object.prototype.x`

# JavaScript 中的 AJAX 请求

# 使用 Cookie

# setTimeout 和 setInterval

# NodeJs 和 NPM

# Webpack

# 你的最终项目

# 第四部分：使用 JavaScript 进行函数式编程

# 函数式编程原则

# Map-Reduce-Filter

# 柯里化与部分求值

- 提及 `bind` 作为部分求值函数

# 递归

# 高阶函数

在本节中，你将学习高阶函数。函数式编程的一个重要基石是高阶函数。如果你想以函数式风格编写程序，掌握高阶函数的基础知识是不可避免的。首先，你将学习高阶函数的简单定义。我会通过展示一些你可能已经在使用高阶函数来确保你记住定义。我们将通过实现一个高阶函数示例来结束本文。

## 什么是高阶函数？

高阶函数是接受函数参数或返回函数的函数。定义中的“或”并非排他性的。我们在上一节中学到 JavaScript 函数是值。因此，函数可以传递给其他函数，也可以作为函数的返回值。

这就是你理解高阶函数所需的全部理论`高阶函数`这个名字起初可能看起来很吓人，但其实没什么好怕的：我们只是将函数作为参数传递或作为返回值返回。

请注意，你可能已经在使用高阶函数：

```javascript
setTimeout( () => console.log('done'), 1000 );
```

# 编写高阶函数

我们可能想自己编写一个高阶函数，以演示其用法。假设你的任务是将表示分的整数值格式化为货币。如果你对`模板面量`的返回值熟悉，请阅读我的文章。

```javascript
const formatCurrency = function(
    currencySymbol,
    decimalSeparator ) {
    return function( value ) {
        const wholePart = Math.trunc( value / 100 );
        let fractionalPart = value % 100;
        if ( fractionalPart < 10 ) {
            fractionalPart = '0' + fractionalPart;
        }
        return `${currencySymbol}${wholePart}${decimalSeparator}${fractionalPart}`;
    }
}
```

或者所示：

```javascript
const A = {
    0: 'value0',
    1: 'value1',
    length: 2
}
```

在这个对象中，`A[1]` 返回 `value1`。`A.length` 返回 `2`。类数组不是真正的数组，因为它们没有某些数组属性和操作，例如：`map`、`reduce`、`filter`、`slice`、`splice`、`push`、`pop`、`append`、`concat`、`join` 等。上述方法适用于类数组的原因是它们继承自 `Object.prototype`，而不是 `Array.prototype`。证明：

```
A.constructor
f Object() { [native code] }
B.constructor
f Array() { [native code] }
```

类数组可以通过多种方式转换为数组：

- `Array.from( args )`
- `Object.values( args )`
- `[...args]`

在 ES6 之前，由于使用类数组对象，柯里化等函数技术更难理解。使用可变参数数量时，请使用剩余参数。记住，`Array.isArray` 用于判断引用指向数组还是类数组对象：



一些高阶函数对于处理 JavaScript 中的数组非常有用。事实上，当主要以函数式风格编写代码时，我们经常使用这些函数而不是循环。这些函数包括：

- `map`，
- `reduce`，
- `filter`。

你可能会合理地问，为什么我没有提到 `forEach` 方法？毕竟，我们谈论的是循环，不是吗？

`forEach` 的问题在于它在函数式编程中是一个完全无用的函数。在以纯粹函数式风格编写代码时，使用 `forEach` 毫无意义。让我们看一个简单的例子：

```javascript
const values = [1, 2, 3, 3, 5];
let sum = 0;

values.forEach( v => { sum += v; } );

console.log( sum );
```

`forEach` 辅助函数遍历 `values`，并对数组中的每个值调用其第一个参数。此 `forEach` 调用的主要效果是返回 `undefined`。从这个角度来看，函数体中包含什么并不重要。当我们执行函数体 `sum += v` 时，会产生一个副作用，修改 `forEach` 辅助函数作用域之外的上下文。

纯粹的函数式编程是无副作用。数组的 `forEach` 辅助函数不返回任何可用值。因此，使用 `forEach` 的唯一原因是依赖 `forEach` 回调中的副作用。

> 在技术面试中，当候选人声称他们打算使用函数式编程，因此使用 `forEach` 辅助函数而不是 `for` 循环时，我经常表现得很困惑。不要掉入这个陷阱。

有更好的函数来操作数组。你可以使用 `reduce` 实现相同的结果：

```javascript
const values = [1, 2, 3, 3, 5];
const sum = values.reduce( (accumulator, v) => accumulator + v, 0 );
console.log( sum ); // 14
```

`reduce` 是一个带函数参数的高阶函数。这个函数参数会在数组的每个元素上执行。它接受一个累加器变量和数组中的一个值。此函数参数的返回值是累加器的新值。这个新值将在属于下一个元素的下一次调用中使用。

让我们打印每次迭代中累加器变量的状态和即将使用的数组值：

```javascript
const values = [1, 2, 3, 3, 5];
const sum = values.reduce( (accumulator, v) => {
    const result = accumulator + v;
    console.log( `accumulator, v, result: ${ accumulator }, ${ v }, ${ result }` );
    return result;
}, 0 );
```

以下值被打印到控制台：

```
accumulator, v, result: 0, 1, 1
accumulator, v, result: 1, 2, 3
accumulator, v, result: 3, 3, 6
accumulator, v, result: 6, 3, 9
accumulator, v, result: 9, 5, 14
```

这就是你需要知道的关于 `reduce` 的全部内容。你很快会有一个练习，在那里你将能够实际使用它。

我们的下一个函数是 `map`。`map` 是一个高阶函数，它接受数组的每个元素，使用回调函数对其进行转换，并返回一个转换后的值数组。

例如，我们可以使用以下表达式获取 2 的不同次幂：

```javascript
> [0, 1, 2, 3, 4].map( v => 2 ** v );
[1, 2, 4, 8, 16]
```

记住，`**` 是 ES2016 中引入的指数运算符。将 `2 ** v` 读作“2 的 v 次方”。

现在让我们构造前 51 个 2 的幂（包括 0 次方）。假设我们不想手动构造一个有 51 个元素的数组，我们可以直接取一个包含 `null` 元素的数组：

```javascript
new Array( 51 ).fill( null )
```

`map` 函数的回调可以接受第二个参数，即当前数组元素的索引：

```javascript
> new Array( 51 ).fill( null ).map( (item, index) => index )
(51) [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21,
    22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42,
    43, 44, 45, 46, 47, 48, 49, 50]
```

我们只剩下最后一步了：不返回索引，我们需要返回 `2 ** index`。

```javascript
> new Array( 51 ).fill( null ).map( (item, index) => 2 ** index )
(51) [1, 2, 4, 8, 16, 32, 64, 128, 256, 512, 1024, 2048, 4096, 8192, 16384, 32768,
    65536, 131072, 262144, 524288, 1048576, 2097152, 4194304, 8388608, 16777216, 33554432,
    67108864, 134217728, 268435456, 536870912, 1073741824, 2147483648, 4294967296, 8589934592,
    17179869184, 34359738368, 68719476736, 137438953472]
```